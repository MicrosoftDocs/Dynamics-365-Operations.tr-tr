---
title: İsveç için kontrol birimi tümleştirmesi örneği
description: Bu konu, Microsoft Dynamics 365 Commerce'taki İsveç'e yönelik mali tümleştirme örneğine genel bakış sağlar.
author: EvgenyPopovMBS
ms.date: 12/20/2021
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: epopov
ms.search.validFrom: 2019-10-08
ms.openlocfilehash: 32c2cf31d82d17d3391536e7a9f1722e1462c336
ms.sourcegitcommit: 0d2de52e12fdb9928556d37a4813a67b303695dc
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 12/21/2021
ms.locfileid: "7944802"
---
# <a name="control-unit-integration-sample-for-sweden"></a>İsveç için kontrol birimi tümleştirmesi örneği

[!include [banner](../includes/banner.md)]

Bu konu, Microsoft Dynamics 365 Commerce'taki İsveç'e yönelik mali tümleştirme örneğine genel bakış sağlar.

> [!NOTE]
> Bu örnek mali tümleştirme işlevi, önceki [İsveç için kontrol birimleriyle POS tümleştirmesi örneğinin](retail-sdk-control-unit-sample.md) yerine geçer. Önceki örnek [mali tümleştirme çerçevesinden](./fiscal-integration-for-retail-channel.md) yararlanmaz ve sonraki güncelleştirmelerde artık kullanılmayacaktır. Önceki örnekten Dynamics 365 Commerce sürüm **10.0.22 ve öncesine** karşılık gelen örneğe nasıl geçileceği hakkında bilgi için bkz. [Önceki tümleştirme örneğinden geçiş yapma](emea-swe-fi-sample-sdk.md#migrating-from-the-earlier-integration-sample).

İsveç için Commerce işlevi, satış noktasının (POS) *kontrol birimleri* olarak bilinen İsveç'e özgü mali cihazlarla örnek tümleştirmesini içerir. Bu örnek, [mali tümleştirme işlevini](fiscal-integration-for-retail-channel.md) genişletir. Bir kontrol biriminin, POS'un eşlendiği bir Hardware station'a fiziksel olarak bağlı olduğu varsayılır. Örneğin bu örnekte, Retail Innovation HTT AB tarafından sunulan [CleanCash Type A](https://www.retailinnovation.se/produkter) kontrol biriminin uygulama programlama arabirimi (API) kullanılmaktadır. CleanCash API'nın 1.1.4 sürümü kullanılır.

Örnek, kaynak kodu biçiminde sağlanır ve Commerce yazılım geliştirme setinin (SDK) bir parçasıdır.

Microsoft, Retail Innovation HTT AB'den herhangi bir donanım, yazılım veya belge yayınlamaz. Kontrol biriminin nasıl edinileceği ve çalıştırılacağı hakkında bilgi için [Retail Innovation HTT AB](https://www.retailinnovation.se/) ile iletişime geçin.

## <a name="scenarios"></a>Senaryolar

İsveç için kontrol birimi tümleştirme örneği aşağıdaki özellikleri içerir:

- Satış, iadeler ve makbuz kopyaları, POS ile eşleştirilmiş Hardware station'a bağlı bir kontrol birimine otomatik olarak kaydedilir.
- Kaydedilen bir harekete ait kontrol birimi için kontrol kodu ve üretim numarası, kontrol biriminden alınır ve harekette kaydedilir. Bu verilere *mali yanıt* da denir. Mali yanıt, **Mağaza hareketleri** sayfasında görüntülenebilir.
- Kontrol koduna ait özel alanlar ve kontrol biriminin üretim numarası, makbuz düzenine eklenebilir. Bu şekilde, makbuzdaki bir hareketin mali yanıtını yazdırabilirsiniz.
- Bir hareketin mali yanıtı **Elektronik günlük (İsveç)** kanal raporunda gösterilir.
- Birkaç hata işleme seçeneği kullanılabilir. Burada bazı örnekler verilmiştir:

    - Yeniden deneme mümkünse mali kaydı yeniden deneme. Örneğin, kontrol birimi bağlı değilse, hazır değilse veya yanıt vermiyorsa mali kaydı yeniden deneyebilirsiniz.
    - Mali kaydı erteleme.
    - Mali kaydı atlama veya hareketi kayıtlı olarak işaretleme ve hatanın nedenini ve ek bilgileri kaydetmek için bilgi kodlarını dahil etme.
    - Yeni bir satış hareketi açılmadan veya bir satış hareketi sonlandırılmadan önce kontrol biriminin kullanılabilir durumda olup olmadığını doğrulama.

### <a name="limitations-of-the-sample"></a>Örneğin sınırlamaları

İsveç için kontrol birimi tümleştirme örneği şu anda müşteri siparişi senaryolarını desteklememektedir.

## <a name="setting-up-the-integration-with-control-units"></a>Kontrol birimleriyle tümleştirmeyi ayarlama

İsveç için gerekli kurulum hakkında daha fazla bilgi için bkz. [İsveç için Commerce'ı ayarlama](./emea-swe-cash-registers.md#setting-up-commerce-for-sweden).

### <a name="configuring-swedenspecific-receipts"></a>İsveç'e özgü makbuzları yapılandırma

#### <a name="configure-custom-fields-so-that-they-can-be-used-in-receipt-formats-for-sales-receipts"></a>Özel alanları, satış makbuzlarına yönelik makbuz biçimlerinde kullanılabilecek şekilde yapılandırma

POS makbuz biçimlerinde kullanılan dil metnini ve özel alanları yapılandırabilirsiniz. Makbuz kurulumunu oluşturan kullanıcının varsayılan şirketi, dil metni kurulumunun oluşturulduğu tüzel kişilikle aynı olmalıdır. Alternatif olarak, aynı dil metinleri hem kullanıcının varsayılan şirketinde hem de kurulumun oluşturulduğu mağazanın tüzel kişiliğinde oluşturulmalıdır.

**Dil metni** sayfasında, makbuz düzenlerine yönelik özel alanların etiketlerine aşağıdaki kayıtları ekleyin. Tabloda gösterilen **Dil Kodu**, **Metin Kodu** ve **Metin** değerlerinin yalnızca örnek olduğunu unutmayın. Bunları gereksinimlerinizi karşılayacak şekilde değiştirebilirsiniz. Ancak kullandığınız **Metin Kodu** değerleri benzersiz ve 900001'e eşit veya bundan daha büyük olmalıdır.

Aşağıdaki POS etiketlerini tablodaki **Dil metni** sayfasının **POS** bölümüne ekleyin.

| Dil kodu | Metin Kodu | Metin                  |
|-------------|---------|-----------------------|
| tr-TR       | 900001  | Kontrol kodunu yazdırma |
| tr-TR       | 900002  | Cihazı kaydetme       |

**Özel alanlar** sayfasında, makbuz düzenlerine yönelik özel alanlara aşağıdaki kayıtları ekleyin. **Açıklamalı alt yazı metni kodu** değerlerinin, **Dil metni** sayfasında belirttiğiniz **Metin Kodu** değerlerine karşılık gelmesi gerektiğini unutmayın.

| Ad                         | Tür    | Altyazı metni kodu |
|------------------------------|---------|-----------------|
| SE_FISCALREGISTERCONTROLCODE | Giriş | 900001          |
| SE_FISCALREGISTERID          | Giriş | 900002          |

> [!NOTE]
> Yukarıdaki tabloda listelendiği gibi, doğru özel alan adlarını belirtmeniz önemlidir. Yanlış bir özel alan adı, makbuzlardaki verilerin eksik olmasına neden olur.

#### <a name="configure-receipt-formats"></a>Makbuz biçimlerini yapılandırma

Gerekli her makbuz biçimi için **Yazdırma davranışı** alanının değerini **Her zaman yazdır** olarak değiştirin.

Makbuz biçimi tasarımcısında, aşağıdaki özel alanları **Alt bilgi** bölümüne ekleyin. Alan adlarının bu konunun önceki bölümünde tanımladığınız dil metinlerine karşılık geldiğini unutmayın.

- **Kayıt kontrol kodu** – Bu alan, kontrol kodunu yazdırır.
- **Cihazı kaydet** – Bu alan, kontrol biriminin üretim numarasını yazdırır.

Makbuz biçimleri ile nasıl çalışılacağı hakkında daha fazla bilgi için bkz. [Makbuz şablonları ve yazdırma](../receipt-templates-printing.md).

### <a name="set-up-fiscal-integration-for-sweden"></a>İsveç için mali tümleştirmeyi ayarlama

İsveç için kontrol birimi tümleştirme örneği, [mali tümleştirme işlevine](fiscal-integration-for-retail-channel.md) dayanır ve Retail SDK'nin bir parçasıdır. Örnek, [Dynamics 365 Commerce Çözümleri](https://github.com/microsoft/Dynamics365Commerce.Solutions/) deposunun **src\\FiscalIntegration\\CleanCash** klasöründe bulunur (örneğin, [sürüm/9.33'teki örnek](https://github.com/microsoft/Dynamics365Commerce.Solutions/tree/release/9.33/src/FiscalIntegration/CleanCash)). Örnek, Commerce Runtime'ın (CRT) uzantısı olan bir mali belge sağlayıcısından ve Commerce Hardware Station'ın uzantısı olan bir mali bağlayıcıdan [oluşur](fiscal-integration-for-retail-channel.md#fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices). Retail SDK'yi kullanma hakkında daha fazla bilgi için [Retail SDK mimarisi](../dev-itpro/retail-sdk/retail-sdk-overview.md) ve [Bağımsız paketleme SDK'si için derleme işlem hattı ayarlama](../dev-itpro/build-pipeline.md) konularına bakın.

> [!WARNING]
> [Yeni bağımsız paketleme ve uzantı modelinin](../dev-itpro/build-pipeline.md) sınırlamaları nedeniyle bu mali tümleştirme örneği için şu anda kullanılamaz. Microsoft Dynamics Lifecycle Services'taki (LCS) bir geliştirici sanal makinesinde (VM) Retail SDK'nin önceki sürümünü kullanmalısınız. Daha fazla bilgi için bkz. [İsveç için kontrol birimi tümleştirme örneğine ilişkin dağıtım kılavuzları (eski)](emea-swe-fi-sample-sdk.md).
>
> Mali tümleştirme örnekleri için yeni bağımsız paketleme ve uzantı modeli desteği, sonraki sürümler için planlanmaktadır.

[Commerce kanalları için mali tümleştirmeyi ayarlama](setting-up-fiscal-integration-for-retail-channel.md) konusunda açıklandığı şekilde mali tümleştirme ayarlama adımlarını tamamlayın.

1. [Bir mali kayıt işlemi ayarlayın](setting-up-fiscal-integration-for-retail-channel.md#set-up-a-fiscal-registration-process). Ayrıca, [bu kontrol birimi tümleştirme örneğine özgü](#set-up-the-registration-process) mali kayıt işlemi ayarlarını da not edin.
1. [Hata işleme ayarlarını belirleyin](setting-up-fiscal-integration-for-retail-channel.md#set-error-handling-settings).
1. [Ertelenen mali kaydın el ile yürütülmesini etkinleştirin](setting-up-fiscal-integration-for-retail-channel.md#enable-manual-execution-of-postponed-fiscal-registration).
1. [Kanal bileşenlerini yapılandırın](#configure-channel-components).

### <a name="set-up-the-registration-process"></a>Mali kayıt işlemini ayarlama

Kayıt işlemini etkinleştirmek üzere Commerce Headquarters'ı ayarlamak için aşağıdaki adımları izleyin. Mali tümleştirme hakkında daha fazla bilgi için bkz. [Commerce kanalları için mali tümleştirmeyi ayarlama](setting-up-fiscal-integration-for-retail-channel.md#set-up-a-fiscal-registration-process).

1. Mali belge sağlayıcısı ve mali bağlayıcı için yapılandırma dosyalarını indirin:

    1. [Dynamics 365 Commerce Çözümleri](https://github.com/microsoft/Dynamics365Commerce.Solutions/) deposunu açın.
    1. SDK/uygulama sürümünüze göre doğru dal sürümünü seçin (örneğin, **[sürüm/9.33](https://github.com/microsoft/Dynamics365Commerce.Solutions/tree/release/9.33)**).
    1. **src \> FiscalIntegration \> CleanCash**'i açın.
    1. Mali belge sağlayıcısı yapılandırma dosyasını **CommerceRuntime \> DocumentProvider.CleanCashSample \> Configuration \> DocumentProviderFiscalCleanCashSample.xml** (örneğin, [sürüm/9.33 dosyası](https://github.com/microsoft/Dynamics365Commerce.Solutions/blob/release/9.33/src/FiscalIntegration/CleanCash/CommerceRuntime/DocumentProvider.CleanCashSample/Configuration/DocumentProviderFiscalCleanCashSample.xml)) kısmından indirin.
    1. Mali bağlayıcı yapılandırma dosyasını **HardwareStation \> Connector.CleanCashSample \> Configuration \> ConnectorCleanCashSample.xml** (örneğin, [sürüm/9.33 dosyası](https://github.com/microsoft/Dynamics365Commerce.Solutions/blob/release/9.33/src/FiscalIntegration/CleanCash/HardwareStation/Connector.CleanCashSample/Configuration/ConnectorCleanCashSample.xml)) kısmından indirin.

    > [!WARNING]
    > [Yeni bağımsız paketleme ve uzantı modelinin](../dev-itpro/build-pipeline.md) sınırlamaları nedeniyle bu mali tümleştirme örneği için şu anda kullanılamaz. LCS'deki bir geliştirici VM'sinde Retail SDK'nin önceki sürümünü kullanmalısınız. Bu mali tümleştirme örneğinin yapılandırma dosyaları, LCS'deki bir geliştirici VM'sinde Retail SDK'nin aşağıdaki klasörlerinde bulunur:
    >
    > - **Mali belge sağlayıcısı yapılandırma dosyası:** RetailSdk\\SampleExtensions\\CommerceRuntime\\Extensions.DocumentProvider.CleanCashSample\\Configuration\\DocumentProviderFiscalCleanCashSample.xml
    > - **Mali bağlayıcı yapılandırma dosyası:** RetailSdk\\SampleExtensions\\HardwareStation\\Extension.CleanCashSample\\Configuration\\ConnectorCleanCashSample.xml
    > 
    > Mali tümleştirme örnekleri için yeni bağımsız paketleme ve uzantı modeli desteği, sonraki sürümler için planlanmaktadır.

1. **Retail ve Commerce \> Headquarters ayarı \> Parametreler \> Paylaşılan Commerce parametreleri**'ne gidin. **Genel** hızlı sekmesinde, **Mali tümleştirmeyi etkinleştir** seçeneğini **Evet** olarak ayarlayın.
1. **Retail ve Commerce \> Kanal kurulumu \> Mali tümleştirme \> Mali belge sağlayıcıları**'na gidin ve daha önce indirdiğiniz mali belge sağlayıcısı yapılandırma dosyasını yükleyin.
1. **Retail ve Commerce \> Kanal kurulumu \> Mali tümleştirme \> Mali bağlayıcılar**'a gidin ve daha önce indirdiğiniz mali bağlayıcı yapılandırma dosyasını yükleyin.
1. **Retail ve Commerce \> Kanal kurulumu \> Mali tümleştirme \> Bağlayıcı işlevi profilleri**'ne gidin. Yeni bir bağlayıcı işlev profili oluşturun. Daha önce yüklediğiniz belge sağlayıcıyı ve bağlayıcıyı seçin. [Veri eşleme ayarlarını](#default-data-mapping) gerektiği gibi güncelleştirin.
1. **Retail ve Commerce \> Kanal kurulumu \> Mali tümleştirme \> Bağlayıcı teknik profilleri**'ne gidin. Yeni bir bağlayıcı teknik profili oluşturun ve daha önce yüklediğiniz mali bağlayıcıyı seçin. [Bağlayıcı ayarlarını](#fiscal-connector-settings) gerektiği gibi güncelleştirin.
6. **Retail ve Commerce \> Kanal kurulumu \> Mali tümleştirme \> Mali bağlayıcı grupları**'na gidin. Daha önce oluşturduğunuz bağlayıcı işlev profili için yeni bir mali bağlayıcı grubu oluşturun.
7. **Retail ve Commerce \> Kanal kurulumu \> Mali tümleştirme \> Mali kayıt işlemleri**'ne gidin. Yeni bir mali kayıt işlemi ve mali kayıt işlem adımı oluşturun, ardından daha önce oluşturduğunuz mali bağlayıcı grubunu seçin.
8. **Retail ve Commerce \> Kanal kurulumu \> POS kurulumu \> POS profilleri \> İşlevsellik profilleri** öğesine tıklayın. Kayıt işleminin etkinleştirilmesi gereken mağazaya bağlı bir işlev profili seçin. **Mali kayıt işlemi** hızlı sekmesinde, daha önce oluşturduğunuz mali kayıt işlemini seçin.
9. **Retail ve Commerce \> Kanal kurulumu \> POS kurulumu \> POS profilleri \> Donanım profilleri**'ne gidin. Mali yazıcının bağlanacağı Hardware station'a bağlı bir donanım profili seçin. **Mali çevre birimleri** hızlı sekmesinde, daha önce oluşturduğunuz bağlayıcı teknik profilini seçin.
10. Kanal veritabanına verileri aktarmak için dağıtım planını (**Retail ve Commerce \> Retail ve Commerce IT \> Dağıtım planı**) açın ve **1070** ile **1090** işlerini seçin.

#### <a name="default-data-mapping"></a>Varsayılan veri eşlemesi

Aşağıdaki varsayılan veri eşlemesi, mali tümleştirme örneğinin bir parçası olarak sağlanan mali belge sağlayıcısı yapılandırmasına dahil edilmiştir:

- **Katma değer vergisi (KDV) kod eşlemesi** – Bu eşleme, ilgili satış vergisi kodlarına cihaza özgü katma değer vergisi (KDV) kodlarını ayarlar. KDV kodu eşlemesinde aşağıdaki biçim kullanılmalıdır:

    ```
    1 : code1 ; 2 : code2
    ```

    Bu biçim için bir açıklama aşağıda verilmiştir:

    - *1* ve *2*, cihaza özgü KDV kodlarıdır.
    - Noktalı virgül (;) ayırıcı olarak kullanılır.
    - *code1* ve *code2*, Commerce Headquarters'da yapılandırılan satış vergisi kodlarıdır. Örnek eşlemeyi uygulamanızda yapılandırılan veri kodlarına göre değiştirmeniz gerekir.

    Dört adede kadar farklı KDV kodunu destekleyen kontrol birimleri. Bu nedenle, KDV kodu eşlemesi aşağıdaki şekilde ayarlanabilir:

    ```
    1 : code1 ; 2 : code2 ; 3 : code3 ; 4 : code4
    ```

    > [!NOTE]
    > Birden fazla satış vergisi kodu, aynı cihaza özgü KDV koduyla eşlenebilir.

#### <a name="fiscal-connector-settings"></a>Mali bağlayıcı ayarları

Aşağıdaki ayarlar, mali tümleştirme örneğinin bir parçası olarak sağlanan mali bağlayıcı yapılandırmasına dahil edilmiştir:

- **Bağlantı dizesi** – Kontrol birimi bağlantı ayarları.
- **Zaman aşımı** – Sürücünün kontrol biriminden yanıt gelmesini bekleyeceği süre (milisaniye cinsinden).

### <a name="configure-channel-components"></a>Kanal bileşenlerini yapılandırma

> [!WARNING]
> [Yeni bağımsız paketleme ve uzantı modelinin](../dev-itpro/build-pipeline.md) sınırlamaları nedeniyle bu mali tümleştirme örneği için şu anda kullanılamaz. LCS'deki bir geliştirici VM'sinde Retail SDK'nin önceki sürümünü kullanmalısınız. Daha fazla bilgi için bkz. [İsveç için kontrol birimi tümleştirme örneğine ilişkin dağıtım kılavuzları (eski)](emea-swe-fi-sample-sdk.md).
>
> Mali tümleştirme örnekleri için yeni bağımsız paketleme ve uzantı modeli desteği, sonraki sürümler için planlanmaktadır.

#### <a name="set-up-the-development-environment"></a>Geliştirme ortamını ayarlama

Örneği test etmek ve genişletmek üzere bir geliştirme ortamı ayarlamak için aşağıdaki adımları izleyin.

1. [Dynamics 365 Commerce Çözümleri](https://github.com/microsoft/Dynamics365Commerce.Solutions) deposunu klonlayın veya indirin. SDK/uygulama sürümünüze göre doğru dal sürümünü seçin. Daha fazla bilgi için bkz. [GitHub ve NuGet'ten Retail SDK örnekleri ve başvuru paketleri indirme](../dev-itpro/retail-sdk/sdk-github.md).
1. **Dynamics365Commerce.Solutions\\FiscalIntegration\\CleanCash\\CleanCash.sln** kısmından kontrol birimi tümleştirme çözümünü açın ve derleyin.
1. CRT uzantılarını yükleyin:

    1. CRT uzantı yükleyicisini bulun:

        - **Commerce Scale Unit:** **CleanCash\\ScaleUnit\\ScaleUnit.CleanCash.Installer\\bin\\Debug\\net461** klasöründe **ScaleUnit.CleanCash.Installer** yükleyicisini bulun.
        - **Modern POS'taki yerel CRT:** **CleanCash\\ModernPOS\\ModernPOS.CleanCash.Installer\\bin\\Debug\\net461** klasöründe **ModernPOS.CleanCash.Installer** yükleyicisini bulun.

    2. CRT uzantısı yükleyicisini komut satırından başlatın:

        - **Commerce Scale Unit:**

            ```Console
            ScaleUnit.CleanCash.Installer.exe install --verbosity 0
            ```

        - **Modern POS'taki yerel CRT:**

            ```Console
            ModernPOS.CleanCash.Installer.exe install --verbosity 0
            ```

1. Hardware station uzantılarını yükleyin:

    1. **CleanCash\\HardwareStation\\HardwareStation.CleanCash.Installer\\bin\\Debug\\net461** klasöründe **HardwareStation.CleanCash.Installer** yükleyicisini bulun.
    1. Uzantı yükleyicisini komut satırından başlatın:

        ```Console
        HardwareStation.CleanCash.Installer.exe install --verbosity 0
        ```

#### <a name="production-environment"></a>Üretim ortamı

Mali tümleştirme örneği için Cloud Scale Unit'i ve self servis dağıtılabilir paketleri oluşturup yayınlamak için [Mali tümleştirme örneği için derleme işlem hattı ayarlama](fiscal-integration-sample-build-pipeline.md) konusundaki adımları izleyin. **CleanCash build-pipeline.yml** şablon YAML dosyası, [Dynamics 365 Commerce Çözümleri](https://github.com/microsoft/Dynamics365Commerce.Solutions) deposunun **Pipeline\\YAML_Files** klasöründe bulunabilir.

## <a name="design-of-the-extensions"></a>Uzantıların tasarımı

İsveç için kontrol birimi tümleştirme örneği, [mali tümleştirme işlevine](fiscal-integration-for-retail-channel.md) dayanır ve Retail SDK'nin bir parçasıdır. Örnek, [Dynamics 365 Commerce Çözümleri](https://github.com/microsoft/Dynamics365Commerce.Solutions/) deposunun **src\\FiscalIntegration\\CleanCash** klasöründe bulunur (örneğin, [sürüm/9.33'teki örnek](https://github.com/microsoft/Dynamics365Commerce.Solutions/tree/release/9.33/src/FiscalIntegration/CleanCash)). Örnek, CRT'nin uzantısı olan bir mali belge sağlayıcısından ve Commerce Hardware Station'ın uzantısı olan bir mali bağlayıcıdan [oluşur](fiscal-integration-for-retail-channel.md#fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices). Retail SDK'yi kullanma hakkında daha fazla bilgi için [Retail SDK mimarisi](../dev-itpro/retail-sdk/retail-sdk-overview.md) ve [Bağımsız paketleme SDK'si için derleme işlem hattı ayarlama](../dev-itpro/build-pipeline.md) konularına bakın.

> [!WARNING]
> [Yeni bağımsız paketleme ve uzantı modelinin](../dev-itpro/build-pipeline.md) sınırlamaları nedeniyle bu mali tümleştirme örneği için şu anda kullanılamaz. LCS'deki bir geliştirici VM'sinde Retail SDK'nin önceki sürümünü kullanmalısınız. Daha fazla bilgi için bkz. [İsveç için kontrol birimi tümleştirme örneğine ilişkin dağıtım kılavuzları (eski)](emea-swe-fi-sample-sdk.md). Mali tümleştirme örnekleri için yeni bağımsız paketleme ve uzantı modeli desteği, sonraki sürümler için planlanmaktadır.

### <a name="crt-extension-design"></a>CRT uzantısı tasarımı

Bir mali belge sağlayıcısı olan uzantının amacı, hizmete özel belgeler oluşturmak ve kontrol biriminden gelen yanıtları işlemektir.

#### <a name="request-handler"></a>İstek işleyicisi

Belge sağlayıcısı için tek bir **DocumentProviderCleanCash** istek işleyicisi vardır. Bu işleyici, kontrol birimi için mali belgeler oluşturmak üzere kullanılır.

Bu işleyici **INamedRequestHandler** arabiriminden devralınır. **HandlerName** yöntemi, işleyicinin adını döndürmekten sorumludur. İşleyicinin adı, Commerce Headquarters'da belirtilen bağlayıcı belge sağlayıcı adıyla eşleşmelidir.

Bağlayıcı aşağıdaki istekleri destekler:

- **GetFiscalDocumentDocumentProviderRequest** – Bu istek, hangi belgelerin oluşturulması gerektiği bilgisini içerir. Kontrol birimine kaydedilmesi gereken, hizmete özgü bir belgeyi döndürür.
- **GetSupportedRegistrableEventsDocumentProviderRequest** – Bu istek, abone olunacak olay listesini döndürür. Şu anda satış olayları ve denetim olayları desteklenmektedir.

#### <a name="configuration"></a>Yapılandırma

Mali belge sağlayıcısına ait yapılandırma dosyası, [Dynamics 365 Commerce Çözümleri](https://github.com/microsoft/Dynamics365Commerce.Solutions/) deposundaki **src\\FiscalIntegration\\CleanCash\\CommerceRuntime\\DocumentProvider.CleanCashSample\\Configuration\\DocumentProviderFiscalCleanCashSample.xml** kısmında bulunur. Bu dosyanın amacı, belge sağlayıcısı ayarlarının Commerce Headquarters'dan yapılandırılmasını etkinleştirmektir. Dosya biçimi, mali tümleştirme yapılandırmasıyla ilgili gereksinimlere uygundur.

### <a name="hardware-station-extension-design"></a>Hardware station uzantı tasarımı

Bir mali bağlayıcı olan uzantının amacı, kontrol birimi ile iletişim kurmaktır. CRT uzantısının oluşturduğu belgeleri kontrol birimine göndermek için HTTP protokolünü kullanır. Ayrıca, kontrol biriminden alınan yanıtları da işler.

#### <a name="request-handler"></a>İstek işleyicisi

**CleanCashHandler** istek işleyicisi, kontrol birimine giden isteklerin işlenmesi için giriş noktasıdır.

İşleyici **INamedRequestHandler** arabiriminden devralınır. **HandlerName** yöntemi, işleyicinin adını döndürmekten sorumludur. İşleyicinin adı, Commerce Headquarters'da belirtilen mali bağlayıcı adıyla eşleşmelidir.

Bağlayıcı aşağıdaki istekleri destekler:

- **SubmitDocumentFiscalDeviceRequest** – Bu istek, belgeleri kontrol birimine gönderir ve hizmetten bir yanıt döndürür.
- **IsReadyFiscalDeviceRequest** – Bu istek, kontrol biriminin sistem durumu denetimi için kullanılır.
- **InitializeFiscalDeviceRequest** – Bu istek, kontrol birimini başlatmak için kullanılır.

#### <a name="configuration"></a>Yapılandırma

Mali bağlayıcıya ait yapılandırma dosyası, [Dynamics 365 Commerce Çözümleri](https://github.com/microsoft/Dynamics365Commerce.Solutions/) deposundaki **src\\FiscalIntegration\\CleanCash\\HardwareStation\\Connector.CleanCashSample\\Configuration\\ConnectorCleanCashSample.xml** kısmında bulunur. Dosyanın amacı, mali bağlayıcı ayarlarının Commerce Headquarters'dan yapılandırılmasını etkinleştirmektir. Dosya biçimi, mali tümleştirme yapılandırmasıyla ilgili gereksinimlere uygundur.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
