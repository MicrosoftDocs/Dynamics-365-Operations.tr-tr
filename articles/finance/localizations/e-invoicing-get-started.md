---
title: Elektronik faturalama eklentisini kullanmaya başlangıç
description: Bu konu, Microsoft Dynamics 365 Finance ve Dynamics 365 Supply Chain Management ile Elektronik faturalama eklentisini kullanmaya başlamanıza yardımcı olacak bilgiler içerir.
author: gionoder
manager: AnnBe
ms.date: 10/08/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: e7f58b8a449e056c4718ac6db30dcd0f0623d2a4
ms.sourcegitcommit: 6e0d6d291d4881b16a677373f712a235e129b632
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/08/2020
ms.locfileid: "3971484"
---
# <a name="get-started-with-the-electronic-invoicing-add-on"></a>Elektronik faturalama eklentisini kullanmaya başlangıç

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]

Bu konu, Elektronik faturalama eklentisini kullanmaya başlamanıza yardımcı olacak bilgiler içerir. Öncelikle, Microsoft Dynamics Lifecycle Services (LCS), Regulatory Configuration Services (RCS) ve Dynamics 365 Finance içindeki yapılandırma adımlarını izlemeniz konusunda yol gösterir. Daha sonra, Dynamics 365 Finance veya Dynamics 365 Supply Chain Management kullanarak servis üzerinden belge gönderme işlemini açıklar. Ayrıca, gönderme günlüklerinin nasıl yorumlanacağını da öğreneceksiniz.

## <a name="availability"></a>Kullanılabilirlik

Elektronik faturalama eklentisi öncelikle bazı ülkede kullanılabilir. Eklenti elektronik fatura oluşturmayı ve aşağıdaki işle ilgili belgeleri göndermeyi destekler:

| Ülke/Bölge  | İş belgesi                          |
|-----------------|--------------------------------------------|
| Avusturya         | Satış ve Proje faturaları                 |
| Belçika         | Satış ve Proje faturaları                 |
| Brezilya          | Elektronik mali belge modeli 55 (NF-e) |
| Danimarka         | Satış ve Proje faturaları                 |
| Estonya         | Satış ve Proje faturaları                 |
| Finlandiya         | Satış ve Proje faturaları                 |
| Fransa          | Satış ve Proje faturaları                 |
| Almanya         | Satış ve Proje faturaları                 |
| İtalya           | Satış ve Proje faturaları                 |
| Meksika          | CFDI faturası                               |
| Hollanda     | Satış ve Proje faturaları                 |
| Norveç          | Satış ve Proje faturaları                 |
| İspanya           | Satış ve Proje faturaları                 |
| Avrupa          | PEPPOL Satış ve Proje faturaları          |
    
## <a name="licensing"></a>Lisans

Elektronik faturalama eklentisini geçerli lisansınızla kullanabilirsiniz. Hizmeti kullanmak için ek lisans gerekmez.

## <a name="prerequisites"></a>Önkoşullar

Bu konudaki adımları tamamlayabilmek için önce aşağıdaki ön koşullara sahip olmanız gerekir:

- LCS hesabınıza erişim.
- Finance veya Supply Chain Management sürüm 10.0.13 veya sonrasını içeren bir LCS dağıtım projesi.
- RCS hesabınıza erişim.
- **Özellik yönetimi** modülü aracılığıyla RCS hesabınızın Genelleştirme özelliğini açın. Daha fazla bilgi için, bkz. [Regulatory Configuration Services (RCS) - Genelleştirme özellikleri](rcs-globalization-feature.md)
- Azure'da bir anahtar kasası kaynağı ve bir depolama hesabı oluşturun. Daha fazla bilgi için bkz. [Azure Depolama Hesabı ve Anahtar Kasası oluşturma](e-invoicing-create-azure-storage-account-key-vault.md).

## <a name="overview"></a>Genel bakış

Aşağıdaki şekil bu konuda tamamlayacağınız beş ana adımı göstermektedir.

![Bu konudaki beş adıma genel bakış](media/e-invoicing-services-get-started-overview-5-steps.png)

1. **Azure kaynakları kurulumu:** Azure depolama alanını ve Azure Anahtar Kasası'nda dijital sertifikaların karşıya yüklenmesini yapılandırın.
2. **LCS kurulumu:** Mikro hizmetler için eklentiyi yükleyin.
3. **RCS Kurulum:** Ortam, kullanıcı erişimi ve e-faturalama özelliklerini ayarlayın.
4. **İstemci kurulumu:** İstemciyle elektronik faturalama eklentisi arasındaki bağlantıyı kurun ve elektronik belgelere yanıt göndermek ve almak için eski özellikleri kapatın.
5. **Faturaları gönder:** Elektronik Faturalama eklentisini kullanarak elektronik belge gönderin ve yanıtları alın.

> [!NOTE]
> Bu konudaki bazı yapılandırma adımları ortak ve ülke/bölge belirsizdir. Ülkeye/bölgeye özgü adımlar ve kurulum yordamları ülkeye/bölgeye özel konularda açıklanmaktadır.

## <a name="lcs-setup"></a>LCS kurulumu

1. LCS hesabınızda oturum açın.
2. **Önizleme özelliği yönetimi** kutucuğunu seçin ve **Genel Önizleme özellikleri** alanı grubunda, **BusinessDocumentSubmission**'ı seçin.
3. **Önizleme özelliği etkin** alanını işaretleyin.
4. LCS dağıtım projesini seçin. Projeyi seçmeden önce, çalışır durumda olmalıdır.
5. **Ortam eklentileri** hızlı sekmesinde, **Yeni eklenti yükle**'yi seçin.
6. **İş Belgesi Gönderme**'yi seçin.
7. **Kurulum eklentisi** iletişim kutusunda, **AAD uygulama kimliği** alanına **091c98b0-a1c9-4b02-b62c-7753395ccabe** değerini girin. Bu değer sabit bir değerdir.
8. **AAD kiracı kimliği** alanında, Azure abonelik hesabınızın kimliğini girin.

    ![LCS 'de eklenti iletişim kutusunu ayarlama](media/e-invoicing-services-get-started-lcs-addin-setup.png)

9. Hüküm ve koşulları kabul etmek için onay kutusunu seçin.
10. **Yükle**'yi seçin.

## <a name="rcs-setup"></a>RCS kurulumu

RCS kurulumu sırasında şu görevleri tamamlayacaksınız:

1. RCS 'de anahtar kasasını ayarlayın.
2. Elektronik faturalama eklentisi sunucusu ile RCS bütünleştirmesini kurun.
3. Kuruluşunuz için Elektronik bir faturalama eklenti ortamı oluşturun.

### <a name="set-up-the-key-vault-in-rcs"></a>RCS'de anahtar kasasını ayarlama

1. RCS hesabınızda oturum açın.
2. **Genelleştirme özellikleri** çalışma alanında **Ortamlar** bölmesinde **E-faturalama** kutucuğunu seçin.
3. **Servis ortamları**'nı seçin.

    ![Servis ortamlarını seçme](media/e-invoicing-services-get-started-select-service-environments.png)

> [!NOTE]
> **Bağlı uygulamalar** seçeneği, RCS aracılığıyla Finance veya Supply Management uygulamalarında Elektronik faturalama eklentisinin otomatik yapılandırılmasına erişim izni verir. Ancak şimdilik bu özellik hala geliştirilme aşamasındadır.

4. Eylem Bölmesi'nde, **Anahtar Kasası parametreleri**'ni seçin.

    ![Anahtar Kasası parametresini seçme](media/e-invoicing-services-get-started-select-key-vault-parameters.png)

5. Eylem Bölmesi'nde, bir anahtar kasası oluşturmak için **Yeni**'yi seçin.
6. **Anahtar Kasası URI'si** alanında, Azure 'da yapılandırdığınız anahtar kasa kaynağının **DNS adı** öznitelik değerini girin. **DNS adı** değerinin nerede bulunacağı hakkında bilgi için, bkz. [Azure Depolama Hesabı ve Anahtar Kasası oluşturma](e-invoicing-create-azure-storage-account-key-vault.md).

    ![Anahtar Kasası URI alanı](media/e-invoicing-services-get-started-enter-key-vault-uri.png)

7. Tüm dijital sertifika adlarını ve güvenilir bağlantılarını kurmak için gereken anahtar kasası gizli anahtarlarını girmek için **Sertifikalar** hızlı sekmesinde **Ekle**'yi seçin. **Tür** sütununda, bunun bir Sertifika mı yoksa Gizli anahtar mı olduğunu belirtebilirsiniz. Her iki değer kümesi de Azure'daki anahtar kasası kaynağı üzerinde yapılandırılır.

    ![Sertifikaları ekleme](media/e-invoicing-services-get-started-add-digital-certificates.png)

8. Ülkeye/bölgeye özel faturanızda dijital imza uygulamak için bir sertifika zinciri gerekiyorsa, Eylem Bölmesi'nde **Sertifika zinciri**'ni seçin ve sonra da zinciri oluşturan sertifikaların veya anahtar kasa gizli anahtarlarının sırasını girin.

### <a name="set-up-the-rcs-integration-with-the-electronic-invoicing-add-on-server"></a>Elektronik faturalama eklentisi sunucusu ile RCS bütünleştirmesini kurma

1. **Genelleştirme özellikleri** çalışma alanında, **İlgili ayarlar** bölümünde, **Elektronik raporlama parametreleri** bağlantısını seçin.
2. **Lifecycle Service hizmetine bağlanmak için burayı tıklayın** seçeneğini belirleyin. LCS'ye bağlanmak istemiyorsanız **İptal**'i seçin.
3. **E-faturalama Hizmetleri** sekmesinde, **Hizmet uç nokta URI'si** alanına, kullanılabilir coğrafi bölgelere uygun değeri girin: `https://businessdocumentsubmission.us.operations365.dynamics.com/` veya `https://businessdocumentsubmission.eu.operations365.dynamics.com/`.
4. **Uygulama kimliği** alanında, **0cdb527f-a8d1-4bf8-9436-b352c68682b2** kimliğinin gösterildiğini doğrulayın. Bu değer sabit bir değerdir.
5. **LCS Ortam Kimliği** alanına, LCS abonelik hesabınızın kimliğini girin.

![Elektronik faturalama eklenti parametreleri girme](media/e-invoicing-services-get-started-enter-e-invoicing-parameters.png)

### <a name="add-an-electronic-invoicing-add-on-environment"></a>Elektronik faturalama eklentisi ortamı ekleme

Elektronik faturalama eklentisi için Geliştirici, Test veya Üretim ortamları gibi farklı ortamlar oluşturabilirsiniz.

1. **Genelleştirme özellikleri** çalışma alanında **Ortamlar** bölmesinde **E-faturalama** kutucuğunu seçin.
2. Bir ortam oluşturmak için **Yeni**'yi seçin.
3. **Depolama SAS belirteç hesabı** alanında, RCS'de anahtar kasasında yapılandırdığınız anahtar kasa gizli anahtarının adını girin.

    ![Depolama SAS belirteç hesabı alanı](media/e-invoicing-services-get-started-enter-sas-token-secret.png)

4. **Kullanıcılar** hızlı sekmesinde, ortamdaki kullanıcılara erişim vermek için **Yeni**'yi seçin.

    ![Servis kullanıcılarını ekleme](media/e-invoicing-services-get-started-enter-service-users.png)

5. Eylem Bölmesi'nde, ortamı elektronik faturalama eklentisi sunucusunda yayınlamak için **Yayınla**'yı seçin.

    ![Yayınla düğmesi](media/e-invoicing-services-get-started-publish-service-environment.png)

### <a name="e-invoicing-feature-setup"></a>E-faturalama özellik kurulumu

"E-faturala özelliği", Elektronik faturalama eklenti sunucusunu kullanmak üzere yapılandırılmış ve yayımlanmış olan kaynağın genel adıdır. E-fatura özellik kurulumu, başka şeylerin yanı sıra, yapılandırılabilir dışarı aktarma ve içe aktarma dosyaları oluşturmak için Elektronik raporlama (ER) yapılandırma biçimlerinin kullanılmasına ve isteklerin gönderilmesine, yanıtları içe aktarmaya ve yanıt içeriğini ayrıştırmaya olanak tanıyan eylemleri ve eylem akışlarının kullanımını birleştirir.

Fatura biçimlerindeki ve eylem akışlarındaki çeşitlilikler nedeniyle, E-faturalama özelliği kurulumu ülkeye/bölgeye bağlıdır.

## <a name="set-up-electronic-invoicing-add-on-integration-in-finance-or-supply-chain-management"></a>Finance ve Supply Chain Management uygulamalarında Elektronik faturalama eklenti kurulumu 

Bu kurulum sırasında şu görevleri tamamlayacaksınız:

1. Deneme özelliğini açma
2. Finance ile tümleştirmeyi etkinleştirmek için Elektronik faturalama eklentisi tümleştirme özelliğini açın.
3. Elektronik faturalama eklentisi uç noktasının URL'sini kurun.
4. Ülkeye/bölgeye özel E-faturalama özelliğiyle ilgili olan ER yapılandırmalarını içe aktarın.
5. Geçerli ülkeye/bölgeye özel E-faturalama özelliğini açın.
6. ER yapılandırmalarını içe aktarın ve gönderme işleminin sonucu olarak ülkeye/bölgeye özel fatura belgenizi güncelleştirmek için gerekli olan yanıt tiplerini ayarlayın.

### <a name="open-flighted-feature"></a>Deneme özelliğini açma
Elektronik fatura tümleştirme özelliği deneme yoluyla etkinleştirildi. Deneme varsayılan olarak bir özelliğin AÇIK veya KAPALI olmasını sağlayan bir kavramdır. Aşağıdaki adımlar üretim dışı bir ortamda bir deneme sağlar. 

1. Aşağıdaki SQL komutunu çalıştırın:

    INSERT INTO SYSFLIGHTING (FLIGHTNAME, ENABLED) VALUES ('BusinessDocumentSubmissionServiceEnabled', 1)
    
    INSERT INTO SYSFLIGHTING (FLIGHTNAME, ENABLED) VALUES ('ElectronicInvoicingServiceIntegrationFeature', 1)
    
2. Yukarıdaki değişikliği yaptıktan sonra, tüm AOS'de IISReset işlemi gerçekleştirin

### <a name="turn-on-the-electronic-invoicing-add-on-integration-feature"></a>Elektronik faturalama eklenti tümleştirme özelliğini açma

1. Finance veya Supply Chain Management'ta oturun açın.
2. **Özellik yönetimi** çalışma alanında, yeni bir özellik olan **Yapılandırılabilir Elektronik faturalama eklenti tümleştirmesi**'ni arayın. Özellik yönetim sayfasında hala böyle bir özellikle gösterilmezse, **Güncelleştirmeleri denetle** işlevini çalıştırın
3. Özelliği seçin ve **Şimdi etkinleştir** düğmesini seçin.

### <a name="set-up-the-service-endpoint-url"></a>Servis uç noktası URL'sini ayarlama

1. **Kuruluş yönetimi \> Kurulum \> Elektronik belge parametreleri** bölümüne gidin.
2. **Gönderme hizmeti** sekmesinde, **Servis uç noktası URL'si** alanına `https://businessdocumentsubmission.us.operations365.dynamics.com/` değerini girin.
3. **Ortam** alanına, RCS kurulumu sırasında oluşturduğunuz Elektronik faturalama eklenti ortamının adını girin.

![Servis parametrelerini girme](media/e-invoicing-services-get-started-enter-service-endpoint.png)

### <a name="import-the-er-configurations"></a>ER yapılandırmalarını içe aktarma

İş verilerinin toplanmasına ve Elektronik faturalama eklentisine gönderilmesine olanak tanımak için, kullanmak istediğiniz ülkeye/bölgeye özgü E-faturalama özelliğiyle ilgili olan ER veri modelini ve ER veri modeli yapılandırmasını içe aktarmanız gerekir.

1. **Elektronik raporlama** çalışma alanında, **Yapılandırma sağlayıcıları** bölümünde, **Microsoft**'u seçin. Bu yapılandırma sağlayıcısının **Etkin** olarak ayarlandığından emin olun. Sağlayıcının **Etkin** olarak nasıl ayarlanacağı hakkında daha fazla bilgi için bkz. [Yapılandırma sağlayıcıları oluşturma ve etkin olarak işaretleme](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11).
3. **Depolar**'ı seçin.
4. **Genel kaynak**'ı seçin ve **Aç**'ı seçin.
5. **Lifecycle Services'a Bağlan** iletişim kutusunda **Lifecycle hizmetine bağlanmak için burayı tıklayın** öğesini seçin.
6. E-faturalama özelliğini kullanmak istediğiniz ülkeye veya bölgeye bağlı olarak, ilgili veri modelini, veri modeli eşlemesini ve biçimleri içe aktarmanız gerekir. Almanız gereken ER yapılandırmalarla ilgili bilgi için ülkeye/bölgeye özel "Elektronik faturalama eklentisini kullanmaya başlangıç" konusuna bakın.
7. **Müşteri faturası bağlam modeli**'ni içe aktarın. Bu model, diğer şeylerin yanı sıra, iş verilerinin gönderilmesi sırasında Elektronik faturalama eklentisi için kullanılan Finance'deki ortamı açıklayan ek parametreler içerir.

### <a name="turn-on-countryregion-specific-e-invoicing-features"></a><a name="region-specific"></a>Ülkeye/bölgeye özel E-faturalama özelliklerini açma

Elektronik faturalama eklentisi ile çalışacak şekilde ülkeye/bölgeye özel E-faturalama özelliklerini etkinleştirmek için, kullanmak istediğiniz tüm yasal varlıklarda özelliği etkinleştirmelisiniz. Daha sonra, eski elektronik faturalama tümleştirmesi artık kullanılamaz ve yeni Elektronik faturalama eklentisi ile tümleştirme açılır.

1. **Kuruluş yönetimi \> Kurulum \> Elektronik belge parametreleri** bölümüne gidin.
2. **Özellikler** sekmesinde, ülkeye/bölgeye özgü E-faturalama özelliğiyle ilgili özelliğin satırında, **Etkin** sütunundaki onay kutusunu işaretleyin. Açmanız gereken özellikle ilgili bilgi için ülkeye/bölgeye özel "Elektronik faturalama eklentisini kullanmaya başlangıç" konusuna bakın.

![E-faturalama özelliğini açma](media/e-invoicing-services-get-started-enable-invoicing-feature.png)

> [!NOTE]
> Farklı ülkeler veya bölgeler için yapılandırılmış birden fazla yasal varlıklar varsa, her yasal varlık için ülkeye/bölgeye özgü E-faturalama özelliğini açabilirsiniz.

### <a name="import-er-configurations-and-set-up-the-response-types-to-update-your-countryregion-specific-invoice-document"></a>ER yapılandırmalarını içe aktarma ve yanıtlama tiplerini, ülkeye/bölgeye özel fatura belgenizi güncelleştirmek için ayarlama

Gönderilen fatura belgesi, resmi yetkilendirme hizmetlerine gönderim yanıtı sonrasında bir güncelleştirme gerektiriyorsa, fatura belgesinin veya güncelleştirilecek başka bir alanın durumunu etkinleştirmek üzere özel bir ER veri modeli ve yapılandırma içe aktarmanız gerekir.

1. **Elektronik raporlama** çalışma alanında, **Yapılandırma sağlayıcıları** bölümünde, **Microsoft**'u seçin.
2. **Depolar**'ı seçin.
3. **Genel kaynak**'ı seçin ve **Aç**'ı seçin.
4. **Yanıt iletisi modeli**, **Yanıt iletisi alma biçimi**, **Yanıt iletisi modeli hedefe eşleştirme** ve **Dosya içeriği içe aktarma biçimi** alanlarını içe aktarın.
5. **Kuruluş yönetimi \> Kurulum \> Elektronik belge parametreleri** bölümüne gidin.
6. **Elektronik belge** sekmesinde, ülkeye/bölgeye özgü fatura belgenize ilişkin tablonun adını girmek için **Ekle**'yi seçin. Seçmeniz gereken özellikle ilgili bilgi için ülkeye/bölgeye özel "Elektronik faturalama eklentisini kullanmaya başlangıç" konusuna bakın.
7. **Yanıt türlerini** yapılandırmak için yanıt türlerini seçin. Seçmeniz gereken özellikle ilgili bilgi için ülkeye/bölgeye özel "Elektronik faturalama eklentisini kullanmaya başlangıç" konusuna bakın.

![Yanıt türlerini ayarlama](media/e-invoicing-services-get-started-set-up-response-types.png)

## <a name="e-invoicing-feature-names-by-country"></a>Ülkeye göre E-faturalama özellik adları 
Aşağıdaki tabloda Elektronik raporlama Genel havuzundan yüklenebilen diğer E-fatura özellikleri, elektronik faturalar oluşturmak üzere açıklanmaktadır.
RCS'de, bu tabloda listelenen E-faturalama özelliklerini, ER yapılandırmalarını ve kullanılabilir E-faturalama özelliği kurulumlarını yükleyebilirsiniz.
Finance'de, bu ülkelere elektronik faturalar hazırlamak için **Elektronik belge parametreleri** sayfasında ilişkili özellik referanslarını etkinleştirebilirsiniz. Daha fazla bilgi için, bu konunun üst kısımlarında yer alan [Ülkeye/bölgeye özel e-faturalama özelliklerini açma](#region-specific) konusuna bakın.

| Özellik adı                      | Tanım                                 | ER yapılandırmaları                                                                                                  | Kurulumlar                                                                                                                                                         | Ülke/Bölge  | Özellik referansı      |
|-----------------------------------|---------------------------------------------|--------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------|------------------------|
| Avusturya elektronik faturaları (AT) | Avusturya Satış ve Proje faturaları      | - OIOUBL Satış faturası <br>- OIOUBL Proje faturası <br>- OIOUBL Satışlar kredi notu <br>- OIOUBL Proje kredi notu | - Satış faturası oluşturma (AT) <br>- Proje faturası oluşturma (AT) <br>- Satış kredi notu oluşturma (AT) <br>- Proje kredi notu oluşturma (AT)         | Avusturya         | EUR-00023              |
| Belçika elektronik faturası (BE)   | Belçika Satış ve Proje faturaları      | - UBL Satış faturası BE <br>- UBL Proje faturası BE <br>- UBL Proje kredi notu BE <br>- UBL Satış kredi notu BE | - Satış faturası oluşturma (BE)<br>- Proje faturası oluşturma (BE) <br>- Satış kredi notu oluşturma (BE) <br>- Proje kredi notu oluşturma (BE)         | Belçika         | EUR-00023              |
| Danimarka elektronik faturası (DK)    | Danimarka Satış ve Proje faturaları      | - OIOUBL Satış faturası <br>- OIOUBL Proje faturası <br>- OIOUBL Satışlar kredi notu <br>- OIOUBL Proje kredi notu | - Satış faturası oluşturma (DK) <br>- Proje faturası oluşturma (DK) <br>- Satış kredi notu oluşturma (DK)<br>- Proje kredi notu oluşturma (DK)         | Danimarka         | EUR-00023<br> DK-00001 |
| Hollanda elektronik faturası (NL)     | Hollanda Satış ve Proje faturaları  | - UBL Satış faturası NL <br>- UBL Proje faturası NL <br>- UBL Satış kredi notu NL <br>- UBL Proje kredi notu NL | - Satış faturası oluşturma (NL) <br> - Proje faturası oluşturma (NL) <br> - Satış kredi notu oluşturma (NL) <br>- Proje kredi notu oluşturma (NL)          | Hollanda | EUR-00023              |
| Estonya elektronik faturası (EE)  | Estonya Satış ve Proje faturaları      | - Satış faturası (EE) <br> - Proje faturası (EE)                                                                     | - Satış faturası oluşturma (EE) <br>- Proje faturası oluşturma (EE)                                                                                           | Estonya         | EUR-00023              |
| Finlandiya elektronik faturası (FI)   | Finlandiya Satış ve Proje faturaları      | - Satış faturası (FI) <br>- Proje faturası oluşturma (FI)                                                          | - Satış faturası oluşturma (FI) <br>- Proje faturası oluşturma (FI)                                                                                           | Finlandiya         | EUR-00023              |
| Fransa elektronik faturası (FR)    | Fransa Satış ve Proje faturaları    | - UBL Satış faturası (FR) <br> - UBL Proje faturası FR <br> - UBL Satış kredi notu FR <br>- UBL Proje kredi notu FR | - Satış faturası oluşturma (FR) <br> - Proje faturası oluşturma (FR) <br>- Satış kredi notu oluşturma (FR) <br>- Proje kredi notu oluşturma (FR)         | Fransa          | EUR-00023              |
| Alman elektronik faturası (DE)    | Almanya Satış ve Proje faturaları      |- Satış faturası (DE) <br> - Proje faturası <DE>                                                                     | - Satış faturası oluşturma (DE) <br>- Proje faturası oluşturma (DE)                                                                                           | Almanya         | EUR-00023              |
| Norveç elektronik faturası (NO) | Norveç Satış ve Proje faturaları       | - OIOUBL Satış faturası <br>- OIOUBL Proje faturası <br>- OIOUBL Satışlar kredi notu <br>- OIOUBL Proje kredi notu | - Satış faturası oluşturma (NO) <br>- Proje faturası oluşturma (NO) <br>- Satış kredi notu oluşturma (NO) <br>- Proje kredi notu oluşturma (NO)          | Norveç          | EUR-00023<br> NO-00010 |
| İspanya elektronik faturası (ES)   | İspanya Satış ve Proje faturaları        | - Satış faturası (ES) <br>- Proje faturası (ES)                                                                     | - Satış faturası oluşturma (ES) <br>- Proje faturası oluşturma (ES)                                                                                           | İspanya           | EUR-00023 <br>ES-00025 |
| İtalyan elektronik faturası (IT)   | İtalya Satış ve Proje faturaları        | - (Önizleme) Satış faturası (IT) <br> - Proje faturası (IT)                                                           | - Satış faturası <br> - Proje faturası                                                                                                                           | İtalya           | EUR-00023 <br>IT-00036 |
| PEPPEOL elektronik faturası         | PEPPOL Satış ve Proje faturası oluşturma | - PEPPOL Satış faturası <br>- PEPPOL Proje faturası <br>- PEPPOL Satış kredi notu <br> - PEPPOL Proje kredi notu | - PEPPOL Satış faturası oluşturma <br>- PEPPOL Proje faturası oluşturma <br>- PEPPOL Satış kredi notu oluşturma <br>- PEPPOL Proje kredi notu oluşturma |                 | EUR-00023              |


## <a name="electronic-invoice-processing-in-finance-and-supply-chain-management"></a>Finance ve Supply Chain Management'te elektronik fatura işlemleri

İşlem sırasında şu görevleri tamamlayacaksınız:

1. Elektronik faturalama eklentisi aracılığıyla iş belgesi (fatura) gönderin.
2. Gönderme yürütme günlüklerine bakın.

### <a name="submit-business-documents"></a>İş belgeleri gönderme

Normal gönderme işlemi sırasında, istemci ve Elektronik faturalama eklentisi arasındaki iletişim iki yönlü bir işlemdir. Amaç, elektronik belgelerin gönderilmesi sırasında iki ana görevi gerçekleştir:

1. Finance'den gönderilmeyi bekleyen ve gönderme durumu doğru olan ve seçim ölçütlerini karşılayan tüm elektronik belgeleri gönderin.
2. Elektronik faturalama eklentisinin önceden gönderilen elektronik belgeler için döndürdüğü yanıtı Finance içine aktarır. İçe aktarma işleminden sonra, yanıtlar ayrıştırılır ve iş belgelerinin durumu buna göre güncelleştirilir.

İş belgelerini el ile veya zamanlama gereksinimlerinize göre gönderebilirsiniz.

1. **Kuruluş Yönetimi \> Dönemlik \> Elektronik belgeler \> Elektronik belgeleri gönder** sayfasına gidin.
2. Herhangi bir belgenin ilk gönderimi için, **Belgeyi yeniden gönder** seçeneğini her zaman **Hayır** olarak ayarlayın. Belgeyi servis aracılığıyla yeniden göndermeniz gerekiyorsa, bu seçeneği **Evet** olarak ayarlayın.
3. **Dahil edilecek kayıtlar** hızlı sekmesinde, gönderilecek belgeleri seçmek üzere bir sorgu oluşturabileceğiniz **Sorgulama** iletişim kutusunu açmak için **Filtre**'yi seçin.

![Elektronik belgeleri gönder iletişim kutusu](media/e-invoicing-services-get-started-submission-form.png)

### <a name="filter-query"></a>Filtre sorgusu

1. **Sorgulama** iletişim kutusunda, **Aralık** sekmesinde, **Tablo**, **Türetilmiş tablo**, **Alan** ve **Ölçüt** alanlarını kullanarak filtre ölçütü girin.
2. İş belgelerini seçmeniz için gereken sayıda ek ölçüt eklemek için **Ekle**'yi seçin.

    ![Gönderme filtresi ölçütlerini ayarlama](media/e-invoicing-services-get-started-set-up-submission-filter-criteria.png)

3. **Sorgulama** iletişim kutusunu kapatmak için **Tamam**'ı seçin.
4. Seçili iş belgelerini Elektronik faturalama eklentisine göndermek için **Tamam**'ı seçin.

    > [!NOTE]
    > Servis aracılığıyla ilk belgeyi gönderme denemeniz sırasında, Elektronik faturalama eklentisi ile bağlantıyı onaylamanız istenecektir. **Elektronik Belge Gönderme Hizmetine bağlanmak için burayı tıklayın** ögesini seçin.
    >
    > ![Elektronik Belge Gönderme Hizmeti ileti kutusuna bağlanma](media/e-invoicing-services-get-started-dialog-form-connect-e-Invoicing-services.png)
    >
    > Bağlantı başarılıysa, bir onay iletisi alırsınız.
    >
    > ![Elektronik faturalama eklentisi ile bağlantının onaylanması](media/e-invoicing-services-get-started-confirmation-connection-e-invoicing-services.png)

5. İletişim kutusunu kapatın.

> [!NOTE]
> Her bir gönderimden sonra, Eylem merkezi gönderilen belge sayısını gösterir.
>
> ![Eylem merkezi iletileri](media/e-invoicing-services-get-started-view-action-center-messages.png)

### <a name="submission-by-batch"></a>Toplu olarak gönderme

Belgeleri el ile göndermek yerine, toplu iş yürütme sıklığının yapılandırılmış sıklığına göre gönderme işlemini otomatikleştirebilir ve arka planda çalıştırabilirsiniz.

1. **Elektronik belgeleri gönder** iletişim kutusunda **Arka planda çalıştır** hızlı sekmesinde, **Toplu işleme** seçeneğini **Evet** olarak ayarlayın.
2. **Tekrarlama** sekmesinde toplu işleme sıklığını yapılandırın.

![Toplu olarak gönderimi ayarlama](media/e-invoicing-services-get-started-set-up-submission-batch.png)

### <a name="view-all-submission-logs"></a>Bütün gönderme günlüklerini görüntüleme

1. **Kuruluş Yönetimi \> Dönemlik \> Elektronik belgeler \> Elektronik belgeleri gönderme günlüğü** sayfasına gidin.
2. **Belge türü** alanında, filtre ölçütü olarak kullanılacak belge türünü seçin.

    ![Gönderme günlüklerinin görüntülemek üzere belge türünü seçme](media/e-invoicing-services-get-started-select-document-type-for-viewing-submission-log.png)

    > [!IMPORTANT]
    > **Gönderim durumu** sütununda gösterilen değer, gönderme işleminin kendisinin tamamlanmasıyla ilgili durumu temsil eder. Elektronik belgenin onaylanmış veya reddedilmiş olmasından bağımsız olarak, RCS'de yapılandırılan eylemlerin akışının sona erene kadar çalıştırılmış olup olmadığını gösterir. **Gönderim durumu** sütunundaki değer, gönderilen belgenin durumunu temsil etmez. Gönderme günlüğü ayrıntılarında **İşlem eylem günlüğü** hızlı sekmesinde, sonraki konularda açıklandığı gibi gönderilen belgenin durumunu yani onaylanmış ya da reddedilmiş olup olmadığını görüntüleyebilirsiniz.

3. Eylem Bölmesi'nde, **Sorgular \> Gönderme**'yi seçin.
4. Gönderme günlüğü ayrıntılarını görüntüleyin.

    ![Gönderme günlüğü ayrıntıları](media/e-invoicing-services-get-started-view-submission-log-form.png)

Gönderme günlüğünde gösterilen sonuçlar E-faturalama özelliğinin RCS'de nasıl ayarlandığına bağlıdır. Ancak, kurulum ne olursa olsun, gönderme günlüğünde her zaman üç hızlı sekme bulunur:

- **İşleme eylemleri**: Bu hızlı sekmede, RCS'de ayarlanan özellik sürümünde yapılandırılan eylemler için yürütme günlükleri gösterilmektedir. **Durum** sütunu eylemin başarıyla çalıştırılıp çalıştırılmadığını gösterir.
- **Eylem dosyaları**: Bu hızlı sekme, eylemlerin yürütülmesi sırasında oluşturulan ara dosyaları gösterir. Dosyayı indirmek ve içeriğini görüntülemek için **Görünüm** öğesini seçebilirsiniz.
- **İşleme eylem günlüğü**: Bu hızlı sekmede, elektronik faturalama eklentisi ve hedef Web servisi arasındaki iletişimin sonuçları gösterilir. Ayrıca Web servis işlemi tarafından döndürülen işlemi de gösterir.

## <a name="related-topics"></a>İlgili konular

- [Elektronik faturalama eklentisine genel bakış](e-invoicing-service-overview.md)
- [Brezilya için Elektronik faturalama eklentisini kullanmaya başlangıç](e-invoicing-bra-get-started.md)
- [Meksika için Elektronik faturalama eklentisini kullanmaya başlangıç](e-invoicing-mex-get-started.md)
- [İtalya için Elektronik faturalama eklentisini kullanmaya başlangıç](e-invoicing-ita-get-started.md)
- [Elektronik faturalamayı eklentisini kurma](e-invoicing-setup.md)
