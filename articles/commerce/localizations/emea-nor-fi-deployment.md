---
title: Norveç için yazar kasalara ilişkin dağıtım kılavuzları
description: Bu konu, Norveç için Microsoft Dynamics 365 Commerce yerelleştirmesine yönelik yazar kasa işlevini etkinleştirme ile ilgili yönergeler sağlar.
author: EvgenyPopovMBS
ms.date: 12/20/2021
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: epopov
ms.search.validFrom: 2019-3-1
ms.openlocfilehash: f0744b18ed59c692ae336c92e488d339ae158368
ms.sourcegitcommit: 5cefe7d2a71c6f220190afc3293e33e2b9119685
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/01/2022
ms.locfileid: "8077152"
---
# <a name="deployment-guidelines-for-cash-registers-for-norway"></a>Norveç için yazar kasalara ilişkin dağıtım kılavuzları

[!include[banner](../includes/banner.md)]

Bu konu, Norveç için Microsoft Dynamics 365 Commerce yerelleştirmesine yönelik yazar kasa işlevini etkinleştirme ile ilgili yönergeler sağlar. Yerelleştirme, çeşitli bileşen uzantılarından oluşur. Bu uzantılar; makbuzlara özel alanlar yazdırma, satış noktasına (POS) ek denetim olayları, satış hareketleri ve ödeme hareketleri kaydetme, satış hareketlerini dijital olarak imzalama ve raporları yerel biçimlerde yazdırma gibi eylemleri gerçekleştirmenize olanak sağlar. Norveç yerelleştirmesi hakkında daha fazla bilgi için bkz. [Norveç için yazar kasa işlevi](./emea-nor-cash-registers.md). Norveç için Commerce'ı ayarlama hakkında daha fazla bilgi için bkz. [Norveç için Commerce'ı ayarlama](./emea-nor-cash-registers.md#setting-up-commerce-for-norway).

> [!WARNING]
> [Yeni bağımsız paketleme ve uzantı modelinin](../dev-itpro/build-pipeline.md) sınırlamaları nedeniyle bu yerelleştirme örneği için şu anda kullanılamaz. Norveç için dijital imzalama örneği sürümünü, Microsoft Dynamics Lifecycle Services'taki (LCS) bir geliştirici sanal makinesinde (VM) bulunan Retail yazılım geliştirme setinin (SDK) önceki sürümünde kullanmanız gerekir. Daha fazla bilgi için bkz. [Norveç için yazar kasalara ilişkin dağıtım kılavuzları (eski)](./emea-nor-loc-deployment-guidelines.md).
>
> Mali tümleştirme örnekleri için yeni bağımsız paketleme ve uzantı modeli desteği, sonraki sürümler için planlanmaktadır.

## <a name="set-up-fiscal-registration-for-norway"></a>Norveç için mali kaydı ayarlama

Norveç için mali kayıt örneği, [mali tümleştirme işlevine](fiscal-integration-for-retail-channel.md) dayanır ve Retail SDK'nin bir parçasıdır. Örnek, [Dynamics 365 Commerce Çözümleri](https://github.com/microsoft/Dynamics365Commerce.Solutions/) deposunun **src\\FiscalIntegration\\SequentialSignatureNorway** klasöründe bulunur (örneğin, [sürüm/9.34'teki örnek](https://github.com/microsoft/Dynamics365Commerce.Solutions/tree/release/9.34/src/FiscalIntegration/SequentialSignatureNorway)). Örnek, Commerce Runtime'ın (CRT) uzantıları olan bir mali belge sağlayıcısı ve mali bağlayıcıdan [oluşur](fiscal-integration-for-retail-channel.md#fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices-and-services). Retail SDK'yi kullanma hakkında daha fazla bilgi için [Retail SDK mimarisi](../dev-itpro/retail-sdk/retail-sdk-overview.md) ve [Bağımsız paketleme SDK'si için derleme işlem hattı ayarlama](../dev-itpro/build-pipeline.md) konularına bakın.

[Commerce kanalları için mali tümleştirmeyi ayarlama](./setting-up-fiscal-integration-for-retail-channel.md) konusunda açıklanan mali kayıt ayarlama adımlarını tamamlayın:

1. [Bir mali kayıt işlemi ayarlayın](./setting-up-fiscal-integration-for-retail-channel.md#set-up-a-fiscal-registration-process). [Norveç'e özgü](#configure-the-fiscal-registration-process) mali kayıt işleminin ayarlarını not aldığınızdan emin olun.
1. [Hata işleme ayarlarını belirleyin](./setting-up-fiscal-integration-for-retail-channel.md#set-error-handling-settings).
1. [Ertelenen mali kaydın el ile yürütülmesini etkinleştirin](./setting-up-fiscal-integration-for-retail-channel.md#enable-manual-execution-of-postponed-fiscal-registration).
1. [Kanal bileşenlerini yapılandırın](#configure-channel-components).

### <a name="configure-the-fiscal-registration-process"></a>Mali kayıt işlemini yapılandırma

Norveç için Commerce Headquarters'daki kayıt işlemini etkinleştirmek üzere aşağıdaki adımları izleyin.

1. Commerce SDK'den mali belge sağlayıcısı ve mali bağlayıcı için yapılandırma dosyalarını indirin:

    1. [Dynamics 365 Commerce Çözümleri](https://github.com/microsoft/Dynamics365Commerce.Solutions/) deposunu açın.
    1. Kullanılabilir en son sürüm dalını (örneğin, **[sürüm/9.34](https://github.com/microsoft/Dynamics365Commerce.Solutions/tree/release/9.34)**) açın.
    1. **src \> FiscalIntegration \> SequentialSignatureNorway \> CommerceRuntime**'ı açın.
    1. Mali belge sağlayıcısı yapılandırma dosyasını **DocumentProvider.SequentialSignNorway \> Configuration \> DocumentProviderSequentialSignatureNorwaySample.xml** (örneğin, [sürüm/9.34 dosyası](https://github.com/microsoft/Dynamics365Commerce.Solutions/blob/release/9.34/src/FiscalIntegration/SequentialSignatureNorway/CommerceRuntime/DocumentProvider.SequentialSignNorway/Configuration/DocumentProviderSequentialSignatureNorwaySample.xml)) kısmından indirin.
    1. Mali bağlayıcı yapılandırma dosyasını **Connector.SequentialSignNorway \> Configuration \> ConnectorSequentialSignatureNorwaySample.xml** (örneğin, [sürüm/9.34 dosyası](https://github.com/microsoft/Dynamics365Commerce.Solutions/blob/release/9.34/src/FiscalIntegration/SequentialSignatureNorway/CommerceRuntime/Connector.SequentialSignNorway/Configuration/ConnectorSequentialSignatureNorwaySample.xml)) kısmından indirin.

1. **Retail ve Commerce \> Headquarters kurulumu \> Parametreler \> Paylaşılan parametreler**'e gidin. **Genel** hızlı sekmesinde, **Mali tümleştirmeyi etkinleştir** seçeneğini **Evet** olarak ayarlayın.
1. **Retail ve Commerce \> Kanal kurulumu \> Mali tümleştirme \> Mali bağlayıcılar**'a gidin ve daha önce indirdiğiniz mali bağlayıcı yapılandırma dosyasını yükleyin.
1. **Retail ve Commerce \> Kanal kurulumu \> Mali tümleştirme \> Mali belge sağlayıcıları**'na gidin ve daha önce indirdiğiniz mali belge sağlayıcısı yapılandırma dosyasını yükleyin.
1. **Retail ve Commerce \> Kanal kurulumu \> Mali tümleştirme \> Bağlayıcı işlevi profilleri**'ne gidin. Yeni bir bağlayıcı işlev profili oluşturun ve daha önce yüklediğiniz belge sağlayıcısını ve bağlayıcıyı seçin.
1. **Retail ve Commerce \> Kanal kurulumu \> Mali tümleştirme \> Bağlayıcı teknik profilleri**'ne gidin. Yeni bir bağlayıcı teknik profili oluşturun ve daha önce yüklediğiniz bağlayıcıyı seçin. Bağlayıcı türünü **Dahili** olarak ayarlayın.
1. **Retail ve Commerce \> Kanal kurulumu \> Mali tümleştirme \> Mali bağlayıcı grupları**'na gidin ve daha önce oluşturduğunuz bağlayıcı işlev profili için yeni bir mali bağlayıcı grubu oluşturun.
1. **Retail ve Commerce \> Kanal kurulumu \> Mali tümleştirme \> Mali kayıt işlemleri**'ne gidin. Yeni bir mali kayıt işlemi ve mali kayıt işlem adımı oluşturun, ardından daha önce oluşturduğunuz mali bağlayıcı grubunu seçin.
1. **Retail ve Commerce \> Kanal kurulumu \> POS kurulumu \> POS profilleri \> İşlevsellik profilleri** öğesine tıklayın. Kayıt işleminin etkinleştirilmesi gereken mağazaya bağlı bir işlev profili seçin. **Mali kayıt işlemi** hızlı sekmesinde, daha önce oluşturduğunuz mali kayıt işlemini seçin. **Mali hizmetler** hızlı sekmesinde, daha önce oluşturduğunuz bağlayıcı teknik profilini seçin. 
1. **Retail ve Commerce \> Retail ve Commerce BT \> Dağıtım planı**'na gidin. Dağıtım planını açın ve verileri kanal veritabanına aktarmak için **1070** ile **1090** işlerini seçin.

### <a name="configure-the-digital-signature-parameters"></a>Dijital imza parametrelerini yapılandırma

Bir mağazadaki satış hareketlerinin dijital olarak imzalanması için kullanılacak sertifikaları yapılandırmanız gerekir. Azure Key Vault'ta depolanan bir dijital sertifika, imzalama işlemini yapmak için kullanılır. Modern POS'un çevrimdışı modunda imzalama, Modern POS'un yüklü olduğu makinenin yerel depolama alanında depolanan bir dijital sertifika kullanılarak da yapılabilir.

Key Vault depolama alanında depolanan bir dijital sertifikayı kullanabilmeniz için aşağıdaki adımların tamamlanması gerekir.

1. Key Vault depolama alanı oluşturulmalıdır. Depolama alanını Commerce Scale Unit ile aynı coğrafi bölgede dağıtmanız önerilir.
1. Sertifikanın, base64 dize gizli dizisi olarak Key Vault depolama alanına yüklenmesi gerekir.
1. Uygulama Nesne Sunucusu (AOS) uygulamasına, Key Vault depolama alanındaki gizli dizileri okuma yetkisi verilmelidir.

Key Vault ile nasıl çalışılacağı hakkında daha fazla bilgi için bkz. [Azure Key Vault'u kullanmaya başlama](/azure/key-vault/key-vault-get-started).

Ardından **Key Vault parametreleri** sayfasında, Key Vault depolama alanına erişmeye yönelik parametreleri belirtmeniz gerekir:

- **Ad** ve **Açıklama** – Key Vault depolama alanının adı ve açıklaması.
- **Key Vault URL'si** – Key Vault depolama alanının URL'si.
- **Key Vault istemcisi** – Kimlik doğrulaması amaçlarıyla, Key Vault depolama alanıyla ilişkili Azure Active Directory (Azure AD) uygulamasının etkileşimli istemci kimliği. Bu istemcinin, depolama alanındaki gizli dizileri okuma erişimine sahip olması gerekir.
- **Key Vault gizli anahtarı** – Key Vault depolama alanında kimlik doğrulaması için kullanılan Azure AD uygulamasıyla ilişkili gizli anahtar.
- **Ad**, **Açıklama** ve **Gizli dizi başvurusu** – Sertifikanın adı, açıklaması ve gizli dizi başvurusu.

Daha sonra, Key Vault veya yerel sertifika depolama alanında depolanan sertifikalarınız için bir bağlayıcı yapılandırmanız gerekir. Bu bağlayıcı, kanal tarafında imzalama için kullanılır.

1. **Retail ve Commerce \> Kanal kurulumu \> Mali tümleştirme \> Bağlayıcı teknik profilleri**'ne gidin.
1. **Ayarlar** hızlı sekmesinde, dijital imzalar için aşağıdaki parametreleri belirtin:

    - **Gizli dizi adı** – Daha önce **Key Vault parametreleri** sayfasında yapılandırdığınız gizli dizi adını seçin.
    - **Yerel sertifika parmak izi** – Yerel olarak depolanan bir sertifika için parmak izi sağlayın.
    - **Karma algoritması** – Microsoft .NET. tarafından desteklenen kriprografik karma algoritmalarından birini (**SHA1** gibi) belirtin.
    - **Sertifika depolama alanı adı** – Bu alan isteğe bağlıdır. Yerel sertifikaları aramak için kullanılacak varsayılan bir mağaza adı belirtmek için bunu kullanın.
    - **Sertifika depolama alanı konumu** – Bu alan isteğe bağlıdır. Yerel sertifikaları aramak için kullanılacak varsayılan bir mağaza konumu belirtmek için bunu kullanın.
    - **Önce yerel sertifikayı dene** – Verileri imzalamak için, Key Vault sertifikası yerine varsayılan olarak yerel depolama alanındaki sertifika kullanmak isterseniz bu seçeneği belirleyin.
    - **Sistem durumu denetimini etkinleştir** – Sistem durumu denetimi özelliği hakkında daha fazla bilgi için bkz. [Mali kayıt sistem durumu denetimi](./fiscal-integration-for-retail-channel.md#fiscal-registration-health-check).

> [!NOTE]
> - Şu anda Norveç için yalnızca **SHA1** kriptografik karma algoritması kabul edilmektedir.
> - Varsayılan mağaza adı ve mağaza konumu, CRT'deki yerel sertifikaları arama işlemini kolaylaştırmak için eklenmiştir. X509StoreProvider, sertifikaların depolandığı klasörlerin listesine sahiptir. Varsayılan mağaza adı ve varsayılan mağaza konumu belirtilmezse X509StoreProvider, kendi listesindeki tüm klasörlerde bir sertifika bulmaya çalışır.

### <a name="configure-channel-components"></a>Kanal bileşenlerini yapılandırma

### <a name="development-environment"></a>Geliştirme ortamı

Örneği sınayabilmeniz ve genişletebilmeniz için bir geliştirme ortamı ayarlamak amacıyla bu adımları izleyin.

1. [Dynamics 365 Commerce Çözümleri](https://github.com/microsoft/Dynamics365Commerce.Solutions) deposunu klonlayın veya indirin. SDK/uygulama sürümünüze göre doğru dal sürümünü seçin. Daha fazla bilgi için bkz. [GitHub ve NuGet'ten Retail SDK örnekleri ve başvuru paketleri indirme](../dev-itpro/retail-sdk/sdk-github.md).
1. **Dynamics365Commerce.Solutions\\FiscalIntegration\\SequentialSignatureNorway** kısmındaki **SequentialSignatureNorway.sln** çözümünü açın ve derleyin.
1. CRT uzantılarını yükleyin:

    1. CRT uzantı yükleyicisini bulun:

        - **Commerce Scale Unit:** **SequentialSignatureNorway\\ScaleUnit\\ScaleUnit.SequentialSignNorway.Installer\\bin\\Debug\\net461** klasöründe **ScaleUnit.SequentialSignNorway.Installer** yükleyicisini bulun.
        - **Modern POS'taki yerel CRT:** **SequentialSignatureNorway\\ModernPOS\\ModernPos.SequentialSignNorway.Installer\\bin\\Debug\\net461** klasöründe **ModernPos.SequentialSignNorway.Installer** yükleyicisini bulun.

    1. CRT uzantısı yükleyicisini komut satırından başlatın:

        - **Commerce Scale Unit:**

            ```Console
            ScaleUnit.SequentialSignNorway.Installer.exe install --verbosity 0
            ```

        - **Modern POS'taki yerel CRT:**

            ```Console
            ModernPOS.SequentialSignNorway.Installer.exe install --verbosity 0
            ```

### <a name="production-environment"></a>Üretim ortamı

Mali tümleştirme örneği için Cloud Scale Unit'i ve self servis dağıtılabilir paketleri oluşturup yayınlamak için [Mali tümleştirme örneği için derleme işlem hattı ayarlama](fiscal-integration-sample-build-pipeline.md) konusundaki adımları izleyin. **SequentialSignatureNorway build-pipeline.yaml** şablon YAML dosyası, [Dynamics 365 Commerce Çözümleri](https://github.com/microsoft/Dynamics365Commerce.Solutions) deposunun **Pipeline\\YAML_Files** klasöründe bulunabilir.

### <a name="enable-the-digital-signature-in-offline-mode-for-modern-pos"></a>Modern POS için çevrimdışı modda dijital imzayı etkinleştirme

Modern POS'un çevrimdışı modunda dijital imzayı etkinleştirmek için, yeni bir cihazda Modern POS'u etkinleştirdikten sonra aşağıdaki adımları izlemeniz gerekir.

1. POS'de oturum açın
1. **Veritabanı bağlantı durumu** sayfasında, çevrimdışı veritabanının tamamen eşitlendiğinden emin olun. **Bekleyen indirmeler** alanının değeri **0** (zero) olduğunda veritabanı tamamen eşitlenmiş demektir.
1. POS oturumunu kapatın.
1. Çevrimdışı veritabanının tamamen eşitlenmesini bekleyin.
1. POS'de oturum açın
1. **Veritabanı bağlantı durumu** sayfasında, çevrimdışı veritabanının tamamen eşitlendiğinden emin olun. **Çevrimdışı veritabanında bekleyen hareketler** alanının değeri **0** (zero) olduğunda veritabanı tamamen eşitlenmiş demektir.
1. Modern POS'u yeniden açın.
