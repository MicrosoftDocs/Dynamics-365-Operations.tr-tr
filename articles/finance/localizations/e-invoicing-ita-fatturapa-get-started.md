---
title: İtalyan FatturaPA'yı doğrudan SDI ile tümleştirmeyi ayarlama
description: Bu konu, İtalya için elektronik faturalamayı kullanmaya başlamanıza ve İtalyan FatturaPA'yı Exchange sistemi (SDI) ile doğrudan tümleştirmeyi ayarlamanıza yardımcı olacak bilgiler içerir.
author: abaryshnikov
ms.date: 12/14/2021
ms.topic: article
audience: Application User, Developer
ms.reviewer: kfend
ms.search.region: Global
ms.author: abaryshnikov
ms.search.validFrom: 2021-10-18
ms.dyn365.ops.version: AX 10.0.20
ms.openlocfilehash: 0ccc9f04e42e748b4531622a1c90559d4ca17196
ms.sourcegitcommit: b1c758ec4abfcf3bf9e50f18c1102d4a9c1316d0
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 12/15/2021
ms.locfileid: "7922459"
---
# <a name="set-up-direct-integration-of-italian-fatturapa-with-sdi"></a>İtalyan FatturaPA'yı doğrudan SDI ile tümleştirmeyi ayarlama

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

> [!IMPORTANT]
> İtalya için Elektronik faturalama Microsoft Dynamics 365 Finance ve Dynamics 365 Supply Chain Management içinden elektronik fatura için kullanılabilen tüm işlevleri şimdilik desteklemeyebilir.

Bu konu, Finance ve Supply Chain Management'ta İtalya için elektronik faturalamayı kullanmaya başlamanıza yardımcı olacak bilgiler içerir. Regulatory Configuration Services (RCS) için ülkeye/bölgeye bağlı olan yapılandırma adımlarında size kılavuzluk eder. Bu adımlar, [Elektronik faturalamayı kullanmaya başlama](e-invoicing-get-started.md) konusunda açıklanan adımları tamamlar.

## <a name="prerequisites"></a>Önkoşullar

Bu konudaki adımları tamamlayabilmek için önce aşağıdaki önkoşulları karşılamanız gerekir:

- [Elektronik faturalamayı kullanmaya başlama](e-invoicing-get-started.md) konusundaki adımları tamamlayın.
- **İtalyan FatturaPA (IT)** elektronik faturalama özelliğini genel depodan RCS'ye aktarın. Daha fazla bilgi için daha önce belirtilen "Elektronik faturalamayı kullanmaya başlama" konusunun [Microsoft yapılandırma sağlayıcısından elektronik faturalama özelliğini içe aktarma](e-invoicing-get-started.md#import-an-electronic-invoicing-feature-from-the-microsoft-configuration-provider) bölümüne bakın.
- Gerekli sertifikalardaki bağlantıları hizmet ortamına ekleyin. Gerekli sertifikalara Dijital imza sertifikası, Sertifika yetkilisi (CA) sertifikası ve İstemciler sertifikası dahildir. Daha fazla bilgi için "Elektronik faturalama hizmeti yönetimini kullanmaya başlama" konusunun [Dijital sertifika gizli dizisi oluşturma](e-invoicing-get-started-service-administration.md#create-a-digital-certificate-secret) bölümüne bakın.

## <a name="country-specific-configuration-for-the-italian-fatturapa-it-electronic-invoicing-feature"></a>İtalyan FatturaPA (IT) elektronik faturalama özelliği için ülkeye özel yapılandırma

Uygulama kurulumunu bağlı Finance veya Supply Chain Management uygulamanıza dağıtmadan önce aşağıdaki yordamları tamamlayın.

Bu bölüm, "Elektronik faturalamayı kullanmaya başlama" konusunun [Uygulama kurulumunun ülkeye özel yapılandırması](e-invoicing-get-started.md#country-specific-configuration-of-application-setup) bölümünü tamamlayıcı niteliktedir.

### <a name="create-a-new-feature"></a>Yeni özellik oluşturma

1. RCS'de oturum açın
2. **Elektronik raporlama** çalışma alanındaki **Yapılandırma sağlayıcıları** bölümünde, şirketinizin yapılandırma sağlayıcısını etkin olarak işaretleyin.
3. **Genelleştirme özelliği** çalışma alanında, **Özellikler** bölümünde, **Elektronik faturalama** kutucuğunu seçin.
4. **Elektronik faturalama özellikleri** sayfasında, **Ekle** \> **Varolan özelliğe dayalı**'yı seçin.
5. **Microsoft yapılandırma sağlayıcısı** altında, temel özellik olarak **İtalyan FatturaPA (IT)**'yi seçin, bir ad girin ve ardından **Özellik oluştur**'u seçin.

### <a name="set-up-application-specific-parameters"></a>Uygulamaya özgü parametreleri ayarlama

1. **Elektronik faturalama özellikleri** sayfasında, düzenlenecek özelliği seçin.
2. **Sürümler** sekmesinde **Taslak** sürümünün seçili olduğunu doğrulayın.
3. **Yapılandırmalar** sekmesinde bir yapılandırma seçin ve ardından **Uygulamaya özgü parametreler**'i seçin.
4. **Aramalar** bölümünde, **Natura tersine çevirme masrafı alt kategorileri listesi** aramasının seçili olduğundan emin olun.
5. **Koşullar** bölümünde **Ekle**'yi seçin.
6. Sistemde tanımlanan her bir alt kategori için özel koşullar ekleyin ve sonra değişikliklerinizi kaydedin.

    > [!NOTE]
    > **Ad** sütununda, belirli bir değer yerine **\*Boş\*** veya **\*Boş değil\*** yer tutucu değerini seçebilirsiniz.

### <a name="configure-a-processing-pipeline-for-export"></a>Dışa aktarma için işleme ardışık düzenini yapılandırma

1. **Elektronik faturalama özellikleri** sayfasında, düzenlenecek özelliği seçin.
2. **Kurulumlar** sekmesinde, **Satış faturaları** ve ardından **Düzenle**'yi seçin.
3. **İşleme ardışık düzeni** bölümünde, eylemlerde ilerleyin ve gerekli tüm alanları ayarlayın:

    - **Belgeyi imzala** eylemi için **Sertifika adı** alanında Dijital imza sertifikasını belirtin.
    - **Gönder** eylemi için **URL adresi** ve **Sertifikalar** alanlarını ayarlayın. **Sertifikalar** alanının değeri, birincisi kök CA sertifikası (caentrate.cer) ve ikincisi İstemciler sertifikası olan bir sertifika zinciridir.

4. Gerekli tüm alanların ayarlandığından emin olmak için **Doğrula**'yı seçin.
5. Değişikliklerinizi kaydedin ve sayfayı kapatın.
6. **Kurulumlar** sekmesinde, **Proje faturaları** ve ardından **Düzenle**'yi seçin.
7. Proje faturaları için 3 ile 5 arasındaki adımları tekrarlayın.

### <a name="configure-the-processing-pipeline-for-import"></a>İçe aktarma için işleme ardışık düzenini yapılandırma

1. **Elektronik faturalama özellikleri** sayfasında, düzenlenecek özelliği seçin.
2. **Kurulumlar** sekmesinde, **Faturaları içe aktar** ve ardından **Düzenle**'yi seçin.
3. **Veri kanalı** bölümündeki **Parametreler** sekmesinde, **Veri kanalı** alanına bir dize değeri girin.
4. **Uygulanabilirlik kuralları** sekmesinde, kurulum için alanları ayarlayın. Önceki adımdaki **Veri kanalı** alanı için ayarladığınız değeri **Değer** alanına geçirerek varsayılan **Kanal** yan tümcesini kullanabilirsiniz.

    ![Uygulanabilirlik kurallarını ayarlama.](media/e-invoicing-ita-fatturapa-get-started-apprules-setup.png)

5. Gerekli tüm alanların ayarlandığından emin olmak için **Doğrula**'yı seçin.

### <a name="deploy-the-feature"></a>Özelliği dağıtma

1. Özelliği tamamlayın, yayımlayın ve hizmet ortamında dağıtın. Daha fazla bilgi için "Elektronik faturalamayı kullanmaya başlama" konusunun [Elektronik faturalama özelliğini hizmet ortamında dağıtma](e-invoicing-get-started.md#deploy-the-electronic-invoicing-feature-to-service-environment) bölümüne bakın.
2. Özelliği bağlı uygulamada dağıtın. Daha fazla bilgi için "Elektronik faturalamayı kullanmaya başlama" konusunun [Elektronik faturalama özelliğini bağlı uygulamada dağıtma](e-invoicing-get-started.md#deploy-the-electronic-invoicing-feature-to-connected-application) bölümüne bakın.

### <a name="set-up-finance"></a>Finance'i ayarlama

1. Finance ortamınızda oturum açın.
2. **Elektronik raporlama** çalışma alanında, **Yapılandırma sağlayıcıları** bölümünde, **Microsoft**'u seçin.
3. **Depolar** \> **Genel** \> **Aç**'ı seçin.
4. **Müşteri faturası bağlam modeli** ve **Satıcı faturasını içe aktarma (IT)** yapılandırmalarını seçin ve içe aktarın.
5. **Kuruluş yönetimi** \> **Kurulum** \> **Elektronik belge parametreleri** bölümüne gidin.
6. **Özellikler** sekmesinde **İtalyan elektronik faturası** özelliğini bulup seçin ve ardından **Etkinleştir** onay kutusunu seçin.
7. **Elektronik belge** sekmesinde, **Müşteri fatura günlüğü** ve **Proje faturası** alanlarının [Uygulama kurulumunu yapılandırma](e-invoicing-get-started.md#configure-the-application-setup) konusundaki bilgilere göre ayarlandığından emin olun.

### <a name="set-up-vendor-invoice-import"></a>Satıcı faturasını içe aktarmayı ayarlama 

1. Finance'te, **Elektronik raporlama** çalışma alanındaki **Yapılandırma sağlayıcıları** bölümünde, şirketinizin yapılandırma sağlayıcısını etkin olarak işaretleyin.
2. **Raporlama yapılandırmaları**'nı seçin.
3. **Müşteri faturası bağlam modeli**'ni seçin ve ardından **Yapılandırma oluştur**'u seçin.
4. Türetilmiş bir yapılandırma oluşturmak için **İsimden Türet: Müşteri faturası bağlam modeli, Microsoft**'u seçin.
5. **Taslak** sürümünde, **Tasarımcı**'yı seçin.
6. **Veri modeli** ağacında, **Modeli veri kaynağına eşle**'yi seçin.
7. **Tanımlar** ağacında, **DataChannel**'ı ve ardından **Tasarımcı**'yı seçin.
8. **Veri kaynakları** ağacında, **\$Context\_Channel** kapsayıcısını genişletin.
9. **Değer** alanında, **Düzenle**'yi seçin. 
10. Veri kanalının adını girin. Ad en fazla 10 karakter uzunluğunda olmalıdır. RCS'deki elektronik faturalama özelliğinin **Veri kanalı** parametresi değeriyle eşleşmelidir.
11. Değişikliklerinizi kaydedin ve sonra **Raporlama yapılandırmaları** \> **Tam yapılandırma sürümü**'ne gidin.
12. **Harici kanallar** sekmesinde, **Kanallar** bölümünde **Ekle**'yi seçin.
13. **Kanal** alanında, **\$Context Channel** değerini girin.
14. **Açıklama** ve **Şirket** alanlarına değer girin.
15. **Belge bağlamı** alanında, **Müşteri faturası bağlam modeli**'nden türettiğiniz yeni yapılandırmayı seçin. Eşleme açıklaması **Veri kanalı bağlamı** olmalıdır.
16. **Kaynakları içe aktar** sekmesinde **Ekle**'yi seçin ve sonra aşağıdaki değerleri ayarlayın:

    - **Ad:** OutputFile
    - **Veri varlığı adı:** Satıcı faturası başlığı (**Veri varlığı:** VendorInvoiceHeaderEntity)
    - **Model eşleme:** Satıcı faturasını içe aktarma (IT)

> [!NOTE]
> Satıcı faturalarını farklı kaynaklardan içe aktardıysanız farklı **\$Context Channel** değerlerine sahip çok sayıda harici kanal ve türetilmiş yapılandırma oluşturabilirsiniz. Örneğin, farklı tüzel kişilikler için satıcı faturalarını içe aktarmak isteyebilirsiniz.

## <a name="proxy-server-setup"></a>Ara sunucu kurulumu

Bu bölümde, Exchange sistemi (SDI) ile elektronik faturalama hizmeti arasındaki iletişim için ara sunucu hizmetini kurup yapılandırmanıza yardımcı olacak bilgiler sağlanmaktadır.

### <a name="create-an-app-registration"></a>Uygulama kaydı oluşturma

1. Servisten servise (S2S) kimlik doğrulaması için otomatik olarak imzalanan bir sertifika oluşturmak üzere aşağıdaki Windows PowerShell betiğini kullanın.

    ```powershell
    $certOutputLocation = "C:\certs\proxytest"
    $certName = "sdiProxyClientS2SCert"
    $certPassword = "123"

    $certCerFile = Join-Path $certOutputLocation "$certName.cer"
    $certPfxFile = Join-Path $certOutputLocation "$certName.pfx"

    $securePassword = ConvertTo-SecureString $certPassword -AsPlainText -Force

    $cert = New-SelfSignedCertificate -KeyLength 2048 -KeyExportPolicy Exportable -FriendlyName "CN=$certName" -CertStoreLocation Cert:\CurrentUser\My -Subject $certName -Provider "Microsoft Enhanced RSA and AES Cryptographic Provider"

    Export-Certificate -Cert $cert -FilePath $certCerFile -type CERT | Out-Null
    Export-PfxCertificate -Cert $cert -FilePath $certPfxFile -Password $securePassword | Out-Null
    ```

2. .pfx sertifika dosyasını anahtar kasasına kaydedin ve sonra yerel kopyayı silin.
3. [Azure portalında](https://portal.azure.com) yönetici olarak oturum açın.
4. SDI ara sunucu hizmeti için bir uygulama kaydı oluşturun.

    1. **Uygulama kayıtları**'na gidin, bir kayıt oluşturun ve sonra bu kayıt için aşağıdaki değerleri ayarlayın:

        - **Ad:** SDI Proxy Client
        - **Desteklenen hesap türleri:** Yalnızca bu kuruluş dizinindeki hesaplar (Tek kiracılı)

    2. **Kaydet**'i seçin ve sonra yeni oluşturduğunuz uygulama kaydını seçin.
    3. **API izinleri**'ne gidin ve **Yönetici izni ver**'i seçin.
    4. **Sertifikalar ve gizli diziler**'e gidin, **Sertifikayı karşıya yükle**'yi seçin ve S2S kimlik doğrulaması için .cer sertifika dosyasını karşıya yükleyin.
    5. **Kurumsal uygulamalar**'a gidin ve oluşturduğunuz uygulamayı seçin.
    6. Uygulamaya ait **Uygulama Kimliği** (istemci kimliği) ve **Nesne Kimliği** değerlerini kaydedin.
    7. Faturalama hizmeti ekibi, uygulamanın hizmete erişmesi için izin vermelidir. Aşağıdaki parametrelerin değerlerini <D365EInvoiceSupport@microsoft.com> adresine gönderin:

        - AAD Kiracı Kimliği
        - LCS Ortam Kimliği
        - Başvuru kodu
        - Nesne kodu

5. RCS'de, hizmet ortamınız için uygulamayı uygulamaya listesine ekleyin.

    1. **Genelleştirme özellikleri** \> **Ortamlar** \> **Elektronik Faturalama** \> **Hizmet ortamları**'na gidin ve ortamınızı seçin.
    2. **Uygulamalar** bölümünde kılavuza bir satır ekleyin ve uygulamanın adı ile nesne kimliğini girin.

        ![Uygulamayı hizmet ortamına ekleme.](media/e-invoicing-ita-fatturapa-get-started-add-app-to-env.png)

    3. **Kaydet**'i ve sonra **Yayımla**'yı seçin.

### <a name="create-an-azure-virtual-machine"></a>Azure sanal makinesi oluşturma

1. [Azure portalında](https://portal.azure.com) **Sanal makineler**'e gidin ve **Yeni oluştur**'u seçin.
2. **Temeller** sekmesinde, aboneliğinizi ve kaynak grubunuzu seçin. Değerler, anahtar kasası ve Blob depolamanızın bulunduğu abonelik ve kaynak grubuna ait olmalıdır.
3. Bölgeyi seçin. Bu değer, Finance ortamınızın dağıtıldığı bölge olmalıdır.
4. Yöneticinin kullanıcı adı ile parolasını ekleyin ve bunları anahtar kasasına kaydedin.
5. **Gelen bağlantı noktalarını seç** alanında **HTTPS (443)** ve **RPD (3389)** bağlantı noktalarını seçin.

    > [!NOTE]
    > Sistem üretime girdiğinde **RDP (3389)** bağlantı noktasını devre dışı bırakmanız önerilir. Sorun giderme amaçlarıyla sanal makineye (VM) bağlanmanız gerekirse bunu yeniden etkinleştirebilirsiniz.

    ![Azure VM oluşturmak için Temeller sekmesindeki alanları ayarlama.](media/e-invoicing-ita-fatturapa-get-started-create-vm-1.png)

6. **Diskler** sekmesindeki **Gelişmiş** hızlı sekmesinde, **Yönetilen diskleri kullan** onay kutusunu seçin. **Kısa süreli işletim sistemi diski** onay kutusunu boş bırakın.

    ![Azure VM oluşturmak için Diskler sekmesindeki alanları ayarlama.](media/e-invoicing-ita-fatturapa-get-started-create-vm-2.png)

7. **Ağ** sekmesindeki **Genel IP** alanı altında, **Yeni oluştur**'u seçin.

    ![Azure VM oluşturmak için Ağ sekmesindeki alanları ayarlama.](media/e-invoicing-ita-fatturapa-get-started-create-vm-3.png)

8. **Genel IP adresi oluştur** iletişim kutusunda, **SKU** alan grubunda **Standart** seçeneğini belirleyin. **Atama** alan grubunda, **Statik** seçeneğini belirleyin.

    ![Genel bir IP adresi oluşturma.](media/e-invoicing-ita-fatturapa-get-started-create-vm-4.png)

9. **Yönetim** sekmesinde, otomatik kapatmayı devre dışı bırakmak için **Otomatik kapatma** onay kutusunu temizleyin.
10. **Konuk işletim sistemi güncelleştirmeleri** alanını **El ile** olarak ayarlayın ve sonra da diğer tüm ilkeleri ayarlayın.
11. VM'yi inceleyin ve oluşturun.
12. Yeni VM'de, **Kimlik** \> **Sistem tarafından atanan**'a gidin ve **Durum** seçeneğini **Açık** olarak ayarlayın.
13. VM'ye anahtar kasasına erişim izni verin.

    1. Anahtar kasasında, **Erişim denetimi (IAM)** \> **Rol atamaları**'na gidin.
    2. **Rol ataması ekle**'yi seçin ve ardından aşağıdaki alanları ayarlayın:

        1. **Rol** alanında, **Key Vault Gizli Dizileri Kullanıcısı**'nı belirtin.
        2. **Erişim ata** alanında, **Sanal makine**'yi belirtin.
        3. **Abonelik** alanında, aboneliğinizi belirtin.
        4. **Seç** alanında, VM'nizi belirtin.

    3. **Erişim ilkeleri**'ne gidin.
    4. **Erişim İlkesi Ekle**'yi seçin ve ardından aşağıdaki alanları ayarlayın:

        1. **Sorumlu Seç** alanında, VM'nizi seçin.
        2. **Sertifika** bölümünde, **List** ve **Get** izinlerini seçin.

14. [Azure portalında](https://portal.azure.com), **Genel IP adresleri**'ne gidin ve VM'de oluşturulan IP adresini seçin.
15. **Yapılandırma**'ya gidin ve Etki Alanı Adı Sistemi (DNS) adını ayarlayın.

### <a name="prepare-the-proxy-service-environment"></a>Ara sunucu hizmet ortamını hazırlama

Ara sunucu hizmetinin barındırıldığı makinede aşağıdaki adımları izleyin.

1. Uzak masaüstü bağlantısını kullanarak VM'ye bağlanın.
2. Yerel Makine sertifikası ek bileşenini açın. Daha fazla bilgi için bkz. [Nasıl yapılır: MMC ek bileşeniyle sertifikaları görüntüleme](/dotnet/framework/wcf/feature-details/how-to-view-certificates-with-the-mmc-snap-in).
3. Üretime yönelik **caentrate.cer** sertifikasını ve teste yönelik **CAEntratetest.cer** sertifikasını [Güvenilen Kök Sertifika Yetkilileri mağazasına](/dotnet/framework/wcf/feature-details/working-with-certificates#certificate-stores) aktarın. (**CAEntratetest.cer**, yetkili tarafından sağlanan kök CA sertifikasıdır.)
4. Denetim Masası'nda **Windows özelliklerini aç veya kapat**'ı açın ya da sunucu işletim sistemi (OS) için **Sunucu Yöneticisi** \> **Rol ve Özellik Ekle**'ye gidin ve Internet Information Services (IIS) özelliklerini etkinleştirin:

    - Web Yönetimi Araçları
        - IIS Yönetim Konsolu
    - World Wide Web Hizmetleri
        - Uygulama Geliştirme Özellikleri
            - .NET Genişletilebilirliği 4.7 (veya 4.8)
            - ASP
            - ASP.NET 4.7 (veya 4.8)
            - CGI
            - ISAPI Uzantıları
            - ISAPI Filtreleri
        - Ortak HTTP Özellikleri
            - Varsayılan Belge
            - Dizin Tarama
            - HTTP Hataları
            - Statik İçerik
        - Durum ve Tanılama
            - HTTP Günlüğü
            - İzleme
        - Performans Özellikleri
            - Statik İçerik Sıkıştırma
        - Güvenlik
            - İstek Filtreleme

    ![IIS özelliklerini etkinleştirme.](media/e-invoicing-ita-fatturapa-get-started-turnon-features.png)

### <a name="set-up-the-sdi-proxy-service-in-iis"></a>IIS'de SDI Ara Sunucu hizmetini ayarlama

1. Microsoft Dynamics Lifecycle Services (LCS)'ta, Paylaşılan varlık kitaplığına gidin ve varlık türü olarak **Veri paketi**'ni seçin.
2. **Electronic Invoicing Service Sdi Proxy** öğesini bulun ve VM'ye indirin.
3. Hizmeti yapılandırın.

    1. İndirdiğiniz **Electronic Invoicing Service Sdi Proxy** arşiv klasörünü açın.
    2. **src\\FattureService** klasöründeki **appsettings.json** dosyasını açın ve aşağıdaki parametreleri ayarlayın:

        - **KeyVaultUri** – Faturalama hizmeti için istemci sertifikasının depolandığı anahtar kasası adresini belirtin.
        - **TenantId** – Müşterinin kiracısının genel benzersiz tanımlayıcısını (GUID) belirtin.
        - **EnvironmentId** – LCS ortamının kimliğini belirtin.
        - **ClientId** – Müşterinin kiracısındaki ara hizmetler uygulama kaydının uygulama kimliğini belirtin.
        - **ClientCertificateName** – Anahtar kasasındaki S2S sertifikasının adını belirtin.
        - **SecurityServiceClientOptions.Endpoint** – Güvenlik hizmetinin URL'sini belirtin.
        - **SecurityServiceClientOptions.Resource** – Belirtecin alınacağı kapsamı belirtin.
        - **InvoicingServiceClientOptions.Endpoint** – Faturalama hizmetinin uç noktasını belirtin. Bu değer, RCS ve Finance için kullanılan uç noktayla aynı olmalıdır.
        - **InvoicingServiceClientOptions.ServiceEnvironmentId** – Hizmet ortamının adını belirtin. Bu değer, Finance ortamınızın adı olmalıdır.
        - **NotificationsFolder** – Gelen bildirim dosyalarının kaydedileceği klasörü belirtin.

    3. **web.config** dosyasında aşağıdaki satırı bulun ve ara sunucu sertifikasının parmak izini ekleyin.

        `<serviceCertificate findValue="[certificate thumbprint]" storeLocation="LocalMachine" storeName="My" x509FindType="FindByThumbprint">`

        > [!TIP]
        > Sistem üretime girdiğinde, toplanan günlük bilgilerinin miktarını azaltmaya yardımcı olmak ve disk alanından tasarruf etmek için web.config dosyasındaki bazı değerleri değiştirebilirsiniz. **\<system.diagnostics\>\<source\>** düğümünde, **switchValue** değerini **Critical,Error** olarak değiştirin. Daha fazla bilgi için bkz. [MS Hizmet İzleme Görüntüleyicisi](/dotnet/framework/wcf/service-trace-viewer-tool-svctraceviewer-exe).

4. IIS Yöneticisi'ni açın. Soldaki ağaçta, kök düğümünde kalın. Sağda, **Sunucu Sertifikaları**'nı seçin.

    ![IIS Yöneticisi'nde Hizmet Sertifikalarını seçme.](media/e-invoicing-ita-fatturapa-get-started-proxy-cert-1.png)

5. Menüyü açın ve **İçe Aktar**'ı seçin.
6. **Sertifikayı İçe Aktar** iletişim kutusunda, **Sertifika dosyası (.pfx)** alanında, ara sunucu sertifikası için .pfx dosyasının yolunu belirtin.

    ![Ara sunucu hizmet sertifikası dosyasını belirtme.](media/e-invoicing-ita-fatturapa-get-started-proxy-cert-2.png)

7. **Siteler**'i seçin ve basılı tutun (veya sağ tıklayın), ardından **Web sitesi ekle**'yi seçin.
8. **Web sitesi ekle** iletişim kutusunda, **Site adı** alanına site için bir ad girin.
9. **Fiziksel yol** alanında **src\\FattureService** klasörünü belirtin.
10. **Bağlama türü** alanında **https**'yi seçin.
11. **Ana bilgisayar adı** alanında, ana bilgisayar adını belirtin.
12. **IP adresi** ve **Bağlantı noktası** alanlarını varsayılan değerlere ayarlanmış olarak bırakın.
13. SDI, Sunucu Adı Belirtme teknolojisini desteklemediğinden **Sunucu Adı Belirtme İste** onay kutusunun işaretinin kaldırıldığından emin olun.
14. **SSL sertifikası** alanında, içe aktardığınız ara sunucu sertifikasını seçin.
15. **Uygulama havuzu** alanında, site için bir havuz belirtin ve havuzun adını not alın (örneğin, **SdiAppPool**).

    ![Web sitesi ekleme.](media/e-invoicing-ita-fatturapa-get-started-proxy-iis-setup-1.png)

16. Web sitesini oluşturmayı bitirdikten sonra **SSL Ayarları** menüsünü açın.

    ![SSL Ayarları menüsünü açma.](media/e-invoicing-ita-fatturapa-get-started-proxy-iis-setup-2.png)

17. **SSL İste** onay kutusunu seçin ve ardından, **İstemci sertifikaları** alan grubunda **Gerekli kıl** seçeneğini belirleyin.

    ![SSL Ayarlarını yapılandırma.](media/e-invoicing-ita-fatturapa-get-started-proxy-iis-setup-3.png)

18. **Dizin Tarama**'yı açın ve **Etkinleştir**'i seçin.
19. Herhangi bir web tarayıcısında **serverDNS/TrasmissioneFatture.svc** adresine gidin. Hizmetle ilgili standart bir sayfa görünecektir.

    ![Hizmeti tarayıcıda kontrol etme.](media/e-invoicing-ita-fatturapa-get-started-proxy-open-browser.png)

20. Günlükleri ve dosyaları depolamak için aşağıdaki klasörleri oluşturun:

    - **C:\\Logs\\** – Günlük dosyaları burada depolanır. Bu dosyalar [MS Hizmet İzleme Görüntüleyicisi](/dotnet/framework/wcf/service-trace-viewer-tool-svctraceviewer-exe) ile görüntülenebilir.
    - **C:\\Files\\** – Tüm yanıt dosyaları burada depolanır.

21. Dosya Gezgini'nde, **NETWORK SERVICE** ve **IIS AppPool\\SdiAppPool** (veya varsayılan havuzu kullanıyorsanız **IIS AppPool\\DefaultAppPool**) öğelerine **Logs** ve **Files** klasörleri için erişim verin.

    1. Klasörlerden birini seçin ve basılı tutun (veya sağ tıklayın) ve ardından **Özellikler**'i seçin.
    2. **Özellikler** iletişim kutusunda, **Güvenlik** sekmesinde **Düzenle**'yi seçin.
    3. Listede yoksa kullanıcıları ekleyin.
    4. Diğer klasör için 1 ile 3 arasındaki adımları tekrarlayın.

    ![Hizmet kullanıcısına izinler ekleme.](media/e-invoicing-ita-fatturapa-get-started-proxy-add-user.png)

## <a name="privacy-notice"></a>Gizlilik bildirimi 

**İtalyan elektronik fatura** özelliğini etkinleştirmek, sınırlı verilerin gönderilmesini gerektirebilir. Bu verilere kuruluşun vergi kayıt kodu dahildir. Bir yönetici İtalya elektronik fatura özelliğini etkinleştirip devre dışı bırakabilir. Özelliği devre dışı bırakmak için şu adımları izleyin.

1. **Kuruluş yönetimi** \> **Kurulum** \> **Elektronik belge parametreleri** bölümüne gidin.
2. **Özellikler** sekmesinde, **İtalyan elektronik faturası** özelliğini içeren satırları seçin ve ardından **Şimdi devre dışı bırak**'ı seçin.

Bu harici sistemlerden alınan verilerin bu Dynamics 365 çevrimiçi hizmetine aktarılması [gizlilik bildirimimize](https://go.microsoft.com/fwlink/?LinkId=512132) tabidir. Daha fazla bilgi için ülkeye/bölgeye özel özellik belgelerindeki "Gizlilik bildirimi" bölümüne bakın.

## <a name="additional-resources"></a>Ek kaynaklar

- [Elektronik faturalamaya genel bakış](e-invoicing-service-overview.md)
- [Elektronik faturalama hizmet yönetimini kullanmaya başlama](e-invoicing-get-started-service-administration.md)
- [Elektronik faturalamayı kullanmaya başlama](e-invoicing-get-started.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
