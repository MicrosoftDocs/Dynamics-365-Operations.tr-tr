---
title: Polonya için yazar kasa tümleştirme örneği
description: Bu makale, Microsoft Dynamics 365 Commerce'taki Polonya'ya yönelik mali tümleştirme örneğine genel bakış sağlar.
author: EvgenyPopovMBS
ms.date: 08/18/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2019-02-01.
ms.openlocfilehash: d4e99854f5e3ab9a6ae802f4f6bcde7918f72e6d
ms.sourcegitcommit: b1df4db7facb5e7094138836c41a65c4a158f01d
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/13/2022
ms.locfileid: "9473794"
---
# <a name="fiscal-printer-integration-sample-for-poland"></a>Polonya için yazar kasa tümleştirme örneği

[!include [banner](../includes/banner.md)]

Bu makale, Microsoft Dynamics 365 Commerce'taki Polonya'ya yönelik mali tümleştirme örneğine genel bakış sağlar.

Polonya için Dynamics 365 Commerce işlevi, satış noktasının (POS) mali bir yazıcıyla örnek tümleştirmesini içerir. Örnek, [mali tümleştirme işlevini](fiscal-integration-for-retail-channel.md) genişletir ve [Posnet Polska S.A.](https://www.posnet.com.pl)'nın mali yazıcıları için POSNET THERMAL HD 2.02 protokolünü destekler. Örnek, yerel yazılım sürücüsü kullanılarak COM bağlantı noktası üzerinden bağlanmış bir mali yazıcıyla iletişimi sağlar. Örnek, Posnet Thermal HD FV EJ mali yazıcısı için Posnet tarafından sağlanan bir yazılım öykünücüsü kullanılarak uygulanmış ve sınanmıştır. Örnek, kaynak kodu biçiminde sağlanır ve Commerce yazılım geliştirme setinin (SDK) bir parçasıdır.

Microsoft, Posnet'ten herhangi bir donanım, yazılım veya belge yayınlamaz. Mali yazıcının nasıl edinileceği ve çalıştırılacağı hakkında bilgi için [Posnet Polska S.A.](https://www.posnet.com.pl) ile iletişime geçin.

## <a name="scenarios"></a>Senaryolar

Aşağıdaki senaryolar, Polonya için mali yazıcı tümleştirme örneğinde ele alınmıştır:

- Satış senaryoları:

    - Peşin satış ve iadeler için mali makbuz yazdırma.
    - Mali yazıcıdan gelen yanıtı kaydetme ve kanal veritabanında saklama.
    - Vergiler:

        - Mali yazıcının vergi kodlarıyla (departmanlar) eşleme.
        - Eşlenen vergi verilerini mali yazıcıya aktarma.

    - Ödemeler:

        - Mali yazıcının ödeme yöntemleriyle eşleme.
        - Mali makbuza ödemeleri yazdırma.
        - Para üstü bilgilerini yazdırma.

    - Satır iskontolarını yazdırma.
    - Hediye kartları:

        - Verilen/yeniden ücretlendirilen hediye kartı satırını, satışa yönelik mali makbuzdan hariç tutma.
        - Hediye kartının normal ödeme yöntemi olarak kullanıldığı bir ödemeyi yazdırma.

    - Müşteri sipariş işlemleri için mali makbuzları yazdırma:

        - Müşteri siparişi havaleleri için mali makbuz yazdırılmaz.
        - Bir karma müşteri siparişine ait teslim alım satırları için mali makbuz yazdırma.
        - Bir müşteri siparişine ait teslim işlemi için mali makbuz yazdırma.
        - İade siparişi için mali makbuz yazdırma.

    - Mali makbuza bir satış hareketi için belirtilen [müşteri bilgilerini](emea-pol-customer-information.md) yazdırma. Bu bilgilere örnek olarak müşterinin KDV numarası verilebilir.

- Gün sonu bildirimleri (mali X ve mali Z raporları).
- Aşağıdaki seçenekler gibi hata işleme özellikleri:

    - Yeniden deneme mümkünse mali kaydı yeniden deneme (örneğin, mali yazıcı bağlı değilse, hazır değilse veya yanıt vermiyorsa, yazıcının kağıdı bittiyse ya da kağıt sıkışması yaşandıysa).
    - Mali kaydı erteleme.
    - Mali kaydı atlama veya hareketi kayıtlı olarak işaretleme ve hatanın nedenini ve ek bilgileri kaydetmek için bilgi kodlarını dahil etme.
    - Yeni bir satış hareketi açılmadan veya bir satış hareketi sonlandırılmadan önce mali yazıcının kullanılabilir durumda olup olmadığını denetleme.

### <a name="gift-cards"></a>Hediye kartları

Mali yazıcı tümleştirme örneği, hediye kartlarıyla ilişkili aşağıdaki kuralları uygular:

- *Hediye kartı ver* ve *Hediye kartına ekle* işlemleriyle ilgili satış satırları, mali makbuzdan hariç tutulur.
- Yalnızca hediye kartı satırlarından oluşan mali makbuzlar yazdırılmaz.
- Bir harekette verilen veya yeniden ücretlendirilen toplam hediye kartı tutarı, mali makbuzun ödeme satırlarından düşülür.
- Ödeme satırlarının hesaplanmış düzeltmeleri, ilgili mali harekete başvuru içerecek şekilde kanal veritabanına kaydedilir.
- Hediye kartı ile ödeme, normal bir ödeme olarak kabul edilir.

### <a name="customer-deposits-and-customer-order-deposits"></a>Müşteri havaleleri ve müşteri siparişi havaleleri

Mali yazıcı tümleştirme örneği, müşteri havaleleri ve müşteri siparişi havaleleri ile ilişkili aşağıdaki kuralları uygular:

- Hareketin müşteri havalesi olması durumunda mali makbuz yazdırılmaz.
- Bir harekette yalnızca müşteri siparişi havalesi veya müşteri siparişi havale iadesi varsa mali makbuz yazdırılmaz.
- Müşteri siparişi teslim alım işlemlerinde, daha önce ödenen havale tutarı mali makbuz üzerine yazdırılır.
- Karma müşteri siparişi oluşturulduğunda, müşteri siparişi havale tutarını ödeme satırlarından düşme.
- Ödeme satırlarının hesaplanmış düzeltmelerini, karma müşteri siparişine yönelik mali harekete başvuru içerecek şekilde kanal veritabanına kaydetme.

### <a name="limitations-of-the-sample"></a>Örneğin sınırlamaları

- Mali yazıcı yalnızca satış vergisinin fiyata dahil edildiği senaryoları destekler. Bu nedenle, **Fiyatlara satış vergisi dahildir** seçeneği hem mağazalar hem de müşteriler için **Evet** olarak ayarlanmalıdır.
- Günlük raporlar (mali X ve mali Z), katıştırılmış *Vardiya raporu* biçimi kullanılarak yazdırılır.
- Mali makbuzlara barkod yazdırma işlemi potansiyel bir özelleştirme olarak kabul edilir çünkü bu özellik, katıştırılmış biçimlerde desteklenmez ve yalnızca özelleştirilebilir **Super-format** raporu kullanılarak uygulanabilir.
- Mali yazıcı, karma hareketleri desteklemez. POS işlev profillerinde **Satış ve iadeleri bir makbuzda birleştirmeyi engelle** seçeneği **Evet** olarak ayarlanmalıdır.

## <a name="set-up-fiscal-integration-for-poland"></a>Polonya için mali tümleştirmeyi ayarlama

Polonya için mali yazıcı tümleştirme örneği, [mali tümleştirme işlevine](fiscal-integration-for-retail-channel.md) dayanır ve Commerce SDK'nin bir parçasıdır. Örnek, [Dynamics 365 Commerce Çözümleri](https://github.com/microsoft/Dynamics365Commerce.Solutions/) deposunun **src\\FiscalIntegration\\Posnet** klasöründe bulunur. [Örnek](fiscal-integration-for-retail-channel.md#fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices-and-services), Commerce Runtime'ın (CRT) uzantısı olan bir mali belge sağlayıcısından ve Commerce Hardware Station'ın uzantısı olan bir mali bağlayıcıdan oluşur. Commerce SDK'yı kullanma hakkında dah afazla bilgi için bkz. [GitHub ve NuGet'ten Retail SDK örnekleri ve başvuru paketleri indirme](../dev-itpro/retail-sdk/sdk-github.md) ve [Bağımsız paketleme SDK'sı için derleme işlem hattı ayarlama](../dev-itpro/build-pipeline.md).

> [!NOTE]
> Polonya için mali yazıcı hizmeti tümleştirme örneği, Commerce SDK 10.0.29 sürümü itibarıyla Commerce SDK'da bulunur. Commerce 10.0.28 veya öncesi sürümlerde, Microsoft Dynamics Lifecycle Services'taki (LCS) bir geliştirici sanal makinesinde (VM) Retail SDK'nin önceki sürümünü kullanmalısınız. Daha fazla bilgi için bkz. [Polonya için mali yazıcı tümleştirme örneğine ilişkin dağıtım kılavuzları (eski)](emea-pol-fpi-sample-sdk.md).

[Commerce kanalları için mali tümleştirmeyi ayarlama](setting-up-fiscal-integration-for-retail-channel.md) konusunda açıklandığı şekilde mali tümleştirme ayarlama adımlarını tamamlayın.

1. [Bir mali kayıt işlemi ayarlayın](setting-up-fiscal-integration-for-retail-channel.md#set-up-a-fiscal-registration-process). Ayrıca, [bu mali yazıcı tümleştirme örneğine özgü](#set-up-the-registration-process) mali kayıt işlemi ayarlarını da not edin.
1. [Hata işleme ayarlarını belirleyin](setting-up-fiscal-integration-for-retail-channel.md#set-error-handling-settings).
1. [POS'tan X/Z raporlarını ayarlayın](setting-up-fiscal-integration-for-retail-channel.md#set-up-fiscal-xz-reports-from-the-pos).
1. [Ertelenen mali kaydın el ile yürütülmesini etkinleştirin](setting-up-fiscal-integration-for-retail-channel.md#enable-manual-execution-of-postponed-fiscal-registration).
1. [Kanal bileşenlerini yapılandırın](#configure-channel-components).

### <a name="set-up-the-registration-process"></a>Mali kayıt işlemini ayarlama

Kayıt işlemini etkinleştirmek üzere Commerce Headquarters'ı ayarlamak için aşağıdaki adımları izleyin. Mali tümleştirme hakkında daha fazla bilgi için bkz. [Commerce kanalları için mali tümleştirmeyi ayarlama](setting-up-fiscal-integration-for-retail-channel.md#set-up-a-fiscal-registration-process).

1. Mali belge sağlayıcısı ve mali bağlayıcı için yapılandırma dosyalarını indirin:

    1. [Dynamics 365 Commerce Çözümleri](https://github.com/microsoft/Dynamics365Commerce.Solutions/) deposunu açın.
    1. SDK/uygulama sürümünüze göre doğru dal sürümünü seçin.
    1. **src \> FiscalIntegration \> Posnet**'i açın.
    1. Mali belge sağlayıcısı yapılandırma dosyasını **CommerceRuntime \> DocumentProvider.PosnetSample \> Configuration \> DocumentProviderPosnetSample.xml** kısmından indirin.
    1. Mali bağlayıcı yapılandırma dosyasını **HardwareStation \> ThermalDeviceSample \> Configuration \> ConnectorPosnetThermalFVEJ.xml** kısmından indirin.

    > [!NOTE]
    > Commerce 10.0.28 veya öncesi sürümlerde, LCS'de bir geliştirici sanal makinesinde Retail SDK'nin önceki sürümünü kullanmalısınız. Bu mali tümleştirme örneğinin yapılandırma dosyaları, LCS'deki bir geliştirici VM'sinde Retail SDK'nin aşağıdaki klasörlerinde bulunur:
    >
    > - **Mali belge sağlayıcısı yapılandırma dosyası:** RetailSdk\\SampleExtensions\\CommerceRuntime\\Extension.DocumentProvider.PosnetSample\\Configuration\\DocumentProviderPosnetSample.xml
    > - **Mali bağlayıcı yapılandırma dosyası:** RetailSdk\\SampleExtensions\\HardwareStation\\Extension.Posnet.ThermalDeviceSample\\Configuration\\ConnectorPosnetThermalFVEJ.xml

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

- **Katma değer vergisi (KDV) oranlarının eşlemesi** – Satış vergisi kodları için ayarlanan vergi yüzdesi değerlerinin, mali yazıcıya özgü KDV oranlarıyla eşlenmesi. Varsayılan eşleme şöyledir:

    ```
    0 : 23.00 ; 1 : 8.00 ; 2 : 5.00 ; 3 : 0.00
    ```

    Her bir çiftin ilk bileşeni, mali yazıcıda yapılandırılan bir KDV oranı numarasını gösterir. İkinci bileşen, karşılık gelen KDV oranını temsil eder. Mali yazıcı KDV oranı yapılandırması hakkında daha fazla bilgi için POSNET sürücü belgelerine bakın.

- **Ödeme türü eşlemesi** – Mağaza için yapılandırılan ödeme yöntemlerinin, mali yazıcı tarafından desteklenen ödeme formlarıyla eşlenmesi. Varsayılan eşleme şöyledir:

    ```
    0 : 0 ; 1 : 0 ; 2 : 2 ; 3 : 2 ; 4 : 0 ; 5 : 0 ; 6 : 0 ; 7 : 2 ; 8 : 0
    ```

    Her bir çiftin ilk bileşeni, mağaza için ayarlanan bir ödeme yöntemini gösterir. İkinci bileşen, mali yazıcı tarafından desteklenen ilgili ödeme formunu temsil eder. Mali yazıcı tarafından desteklenen ödeme formları hakkında daha fazla bilgi için POSNET sürücü belgelerine bakın. Örnek eşlemeyi uygulamanızda yapılandırılan ödeme yöntemlerine göre değiştirmeniz gerekir.

#### <a name="fiscal-connector-settings"></a>Mali bağlayıcı ayarları

Aşağıdaki ayarlar, mali tümleştirme örneğinin bir parçası olarak sağlanan mali bağlayıcı yapılandırmasına dahil edilmiştir:

- **Bağlantı dizesi** – Cihaz bağlantısının ayrıntılarını sürücü tarafından desteklenen bir biçimde açıklayan bir dize. Daha fazla bilgi için POSNET sürücü belgelerine bakın.
- **Tarih ve saat eşitleme** – Yazıcının tarih ve saatinin bağlı Hardware station ile eşitlenip eşitlenmeyeceğini belirten bir değer.
- **Cihaz zaman aşımı** – Sürücünün cihazdan yanıt gelmesini bekleyeceği süre (milisaniye cinsinden). Daha fazla bilgi için POSNET sürücü belgelerine bakın.

### <a name="configure-channel-components"></a>Kanal bileşenlerini yapılandırma

> [!NOTE]
> - Polonya için mali yazıcı hizmeti tümleştirme örneği, Commerce SDK 10.0.29 sürümü itibarıyla Commerce SDK'da bulunur. Commerce 10.0.28 veya öncesi sürümlerde, LCS'de bir geliştirici sanal makinesinde Retail SDK'nin önceki sürümünü kullanmalısınız. Daha fazla bilgi için bkz. [Polonya için mali yazıcı tümleştirme örneğine ilişkin dağıtım kılavuzları (eski)](emea-pol-fpi-sample-sdk.md).
> - Commerce bileşenlerine hizmet veya kalite güncelleştirmeleri uyguladığınızda, ortamınızda dağıtılan Commerce kurulumları otomatik olarak güncelleştirilmez. Gerekli örnekleri el ile güncelleştirmeniz gerekir.

#### <a name="set-up-the-development-environment"></a>Geliştirme ortamını ayarlama

Örneği test etmek ve genişletmek üzere bir geliştirme ortamı ayarlamak için aşağıdaki adımları izleyin.

1. [Dynamics 365 Commerce Çözümleri](https://github.com/microsoft/Dynamics365Commerce.Solutions) deposunu klonlayın veya indirin. SDK/uygulama sürümünüze göre doğru dal sürümünü seçin. Daha fazla bilgi için bkz. [GitHub ve NuGet'ten Commerce SDK örnekleri ve başvuru paketleri indirme](../dev-itpro/retail-sdk/sdk-github.md).
1. **Dynamics365Commerce.Solutions\\FiscalIntegration\\Posnet\\Posnet.sln** kısmından mali yazıcı tümleştirme çözümünü açın ve derleyin.
1. CRT uzantılarını yükleyin:

    1. CRT uzantı yükleyicisini bulun:

        - **Commerce Scale Unit:** **Posnet\\ScaleUnit\\ScaleUnit.Posnet.Installer\\bin\\Debug\\net461** klasöründe **ScaleUnit.Posnet.Installer** yükleyicisini bulun.
        - **Modern POS'taki yerel CRT:** **Posnet\\ModernPOS\\ModernPOS.Posnet.Installer\\bin\\Debug\\net461** klasöründe **ModernPOS.Posnet.Installer** yükleyicisini bulun.

    1. CRT uzantısı yükleyicisini komut satırından başlatın:

        - **Commerce Scale Unit:**

            ```Console
            ScaleUnit.Posnet.Installer.exe install --verbosity 0
            ```

        - **Modern POS'taki yerel CRT:**

            ```Console
            ModernPOS.Posnet.Installer.exe install --verbosity 0
            ```

1. Hardware station uzantılarını yükleyin:

    1. **Posnet\\HardwareStation\\HardwareStation.PosnetThermalFVFiscalPrinter.Installer\\bin\\Debug\\net461** klasöründe **HardwareStation.PosnetThermalFVFiscalPrinter.Installer** yükleyicisini bulun.
    1. Uzantı yükleyicisini komut satırından başlatın:

        ```Console
        HardwareStation.PosnetThermalFVFiscalPrinter.Installer.exe install --verbosity 0
        ```

#### <a name="production-environment"></a>Üretim ortamı

Mali tümleştirme örneği için Cloud Scale Unit'i ve self servis dağıtılabilir paketleri oluşturup yayınlamak için [Mali tümleştirme örneği için derleme işlem hattı ayarlama](fiscal-integration-sample-build-pipeline.md) konusundaki adımları izleyin. **Posnet build-pipeline.yml** şablon YAML dosyası, [Dynamics 365 Commerce Çözümleri](https://github.com/microsoft/Dynamics365Commerce.Solutions) deposunun **Pipeline\\YAML_Files** klasöründe bulunabilir.

## <a name="design-of-extensions"></a>Uzantıların tasarımı

Polonya için mali yazıcı tümleştirme örneği, [mali tümleştirme işlevine](fiscal-integration-for-retail-channel.md) dayanır ve Commerce SDK'nin bir parçasıdır. Örnek, [Dynamics 365 Commerce Çözümleri](https://github.com/microsoft/Dynamics365Commerce.Solutions/) deposunun **src\\FiscalIntegration\\Posnet** klasöründe bulunur. [Örnek](fiscal-integration-for-retail-channel.md#fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices-and-services), CRT'nin uzantısı olan bir mali belge sağlayıcısından ve Commerce Hardware Station'ın uzantısı olan bir mali bağlayıcıdan oluşur. Commerce SDK'yı kullanma hakkında dah afazla bilgi için bkz. [GitHub ve NuGet'ten Retail SDK örnekleri ve başvuru paketleri indirme](../dev-itpro/retail-sdk/sdk-github.md) ve [Bağımsız paketleme SDK'sı için derleme işlem hattı ayarlama](../dev-itpro/build-pipeline.md).

> [!NOTE]
> Polonya için mali yazıcı hizmeti tümleştirme örneği, Commerce SDK 10.0.29 sürümü itibarıyla Commerce SDK'da bulunur. Commerce 10.0.28 veya öncesi sürümlerde, LCS'de bir geliştirici sanal makinesinde Retail SDK'nin önceki sürümünü kullanmalısınız. Daha fazla bilgi için bkz. [Polonya için mali yazıcı tümleştirme örneğine ilişkin dağıtım kılavuzları (eski)](emea-pol-fpi-sample-sdk.md).

### <a name="commerce-runtime-extension-design"></a>Commerce Runtime uzantı tasarımı

Bir mali belge sağlayıcısı olan uzantının amacı, yazıcıya özgü belgeler oluşturmak ve mali yazıcıdan gelen yanıtları işlemektir. Bu uzantı, JavaScript Nesne Gösterimi (JSON) biçiminde olmak üzere, POSNET Specification 19-3678 tarafından tanımlanan yazıcıya özgü bir komut grubu oluşturur.

#### <a name="request-handler"></a>İstek işleyicisi

**DocumentProviderPosnetProtocol** istek işleyicisi, mali yazıcıdan belge oluşturma isteğinin giriş noktasıdır.

İşleyici **INamedRequestHandler** arabiriminden devralınır. **HandlerName** yöntemi, işleyicinin adını döndürmekten sorumludur. İşleyicinin adı, Commerce Headquarters'da belirtilen bağlayıcı belge sağlayıcı adıyla eşleşmelidir.

Bağlayıcı aşağıdaki istekleri destekler:

- **GetFiscalDocumentDocumentProviderRequest** – Bu istek, hangi belgelerin oluşturulması gerektiği bilgisini içerir. Mali yazıcıya kaydedilmesi gereken, yazıcıya özgü bir belgeyi döndürür.
- **GetSupportedRegistrableEventsDocumentProviderRequest** – Bu istek, abone olunacak olay listesini döndürür. Şu anda şu olaylar desteklenmektedir: satış, X raporu yazdırma ve Z raporu yazdırma.

#### <a name="configuration"></a>Yapılandırma

Mali belge sağlayıcısına ait yapılandırma dosyası, [Dynamics 365 Commerce Çözümleri](https://github.com/microsoft/Dynamics365Commerce.Solutions/) deposundaki **src\\FiscalIntegration\\Posnet\\CommerceRuntime\\DocumentProvider.PosnetSample\\Configuration\\DocumentProviderPosnetSample.xml** kısmında bulunur. Dosyanın amacı, mali belge sağlayıcısı ayarlarının Commerce Headquarters'dan yapılandırılmasını etkinleştirmektir. Dosya biçimi, mali tümleştirme yapılandırmasıyla ilgili gereksinimlere uygundur.

### <a name="hardware-station-extension-design"></a>Hardware station uzantı tasarımı

Bir mali bağlayıcı olan uzantının amacı, mali yazıcı ile iletişim kurmaktır. Bu uzantı, CRT uzantısının ürettiği komutları mali yazıcıya göndermek için POSNET sürücüsünün işlevlerini çağırır. Ayrıca cihaz hatalarını işler.

#### <a name="request-handler"></a>İstek işleyicisi

**FiscalPrinterHandler** istek işleyicisi, mali çevre birimi cihazına giden isteklerin işlenmesi için giriş noktasıdır.

İşleyici **INamedRequestHandler** arabiriminden devralınır. **HandlerName** yöntemi, işleyicinin adını döndürmekten sorumludur. İşleyicinin adı, Commerce Headquarters'da belirtilen mali bağlayıcı adıyla eşleşmelidir.

Bağlayıcı aşağıdaki istekleri destekler:

- **SubmitDocumentFiscalDeviceRequest** – Bu istek, belgeleri yazıcılara gönderir ve mali yazıcıdan yanıt döndürür.
- **IsReadyFiscalDeviceRequest** – Bu istek, cihazın sistem durumu denetimi için kullanılır.
- **InitializeFiscalDeviceRequest** – Bu istek, yazıcıyı başlatmak için kullanılır.

#### <a name="configuration"></a>Yapılandırma

Mali bağlayıcıya ait yapılandırma dosyası, [Dynamics 365 Commerce Çözümleri](https://github.com/microsoft/Dynamics365Commerce.Solutions/) deposundaki **src\\FiscalIntegration\\Posnet\\HardwareStation\\ThermalDeviceSample\\Configuration\\ConnectorPosnetThermalFVEJ.xml** kısmında bulunur. Dosyanın amacı, mali bağlayıcı ayarlarının Commerce Headquarters'dan yapılandırılmasını etkinleştirmektir. Dosya biçimi, mali tümleştirme yapılandırmasıyla ilgili gereksinimlere uygundur.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
