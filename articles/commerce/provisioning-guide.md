---
title: e-Ticaret değerlendirme ortamı yapılandırma
description: Bu kılavuz, Microsoft Dynamics 365 Commerce önizleme ortamınızı sağlama ve konfigüre etme konusunda adım adım yönergeler sağlar.
author: v-chgri
manager: annbe
ms.date: 10/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: b0dce2796e69cd8dee87cba176a521c26c81eb1a
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/06/2019
ms.locfileid: "2771692"
---
# <a name="configure-an-e-commerce-evaluation-environment"></a>e-Ticaret değerlendirme ortamı yapılandırma

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

Bu kılavuz, Microsoft Dynamics 365 Commerce önizleme ortamınızı sağlama ve konfigüre etme konusunda adım adım yönergeler sağlar. Başlamadan önce, işlemin ne olduğunu ve kılavuzun neler içerdiğini öğrenmek için belgeleri en azından bir fikir almak için inclemeenizi öneririz.

*Not: Microsoft Dynamics 365 Commerce önizleme'ye erişim izni verilmemişse, [Commerce Web sitesinden](https://aka.ms/Dynamics365CommerceWebsite) önizleme erişimi isteyebilirsiniz.*

## <a name="summary"></a>Özet
Ortamı başarıyla sağlamak için, projenin belirli bir ürün adı ve türle oluşturulması gerekir. Ortam ve Retail Cloud Scale Unit, ayrıca, e-ticaret sağlamasının daha sonra başlatmak için kullanmanız gereken belirli parametreleri de vardır. Bu kılavuzdaki yönergeler gerçekleştirmeniz gereken tüm gerekli adımları ve kullanmanız gereken parametreleri içerir.

Sağlama başarılı olduktan sonra, önizleme ortamınızı hazırlamak için almanız gereken birkaç son işlem adımı vardır. Sistemin hangi yönlere göre değerlendirileceğini bağlı olarak bazı adımlar isteğe bağlıdır. Daha sonra fikrinizi değiştirirseniz, isteğe bağlı adımları daha sonra da çalıştırabilirsiniz.

Sağlama adımlarıyla ilgili sorularınız varsa veya herhangi bir sorunla karşılaşırsanız, lütfen [Microsoft Dynamics 365 Commerce önizleme Yammer grubunda](https://aka.ms/Dynamics365CommercePreviewYammer)bize bildirin. 

## <a name="prerequisites"></a>Önkoşullar
Aşağıda, Dynamics 365 önizleme ortamınızı sağlama önkoşulları verilmiştir:
* **Lifecycle Services portalına (LCS)** erişim hakkınız var
* **Önizleme programına Dynamics 365 Commerce kabul edilmiş** olabilirsiniz
* **Olası ön satışlar** için bir proje oluşturmak veya **geçiş yapmak, çözüm oluşturmak ve daha fazla bilgi** edinmek için gerekli izinleriniz vardır
* Ortamı sağlamak istediğiniz **Ortam yöneticisi** veya **Proje Sahibi** rolünün bir üyesisinizdir
* Azure aboneliğinize yönetici erişiminiz var veya sizin adınıza yönetici izinleri gerektiren iki adımı gerçekleştirebilecek bir abonelik Yöneticisi ile ilişki kurun
* **AAD kiracı kimliğiniz** kullanılabilir
* **E-ticaret sistem yöneticileri grubu** olarak kullanılacak bir **AAD güvenlik grubu** oluşturdunuz ve kimliğiniz kullanılabilir
* **Derecelendirme veya inceleme grubu** olarak kullanılacak bir **AAD güvenlik grubu** oluşturdunuz ve bunun kodu mevcut (yukarıdaki sistem admin grubuyla aynı SG olabilir)
## <a name="provisioning-preview-environment"></a>Önizleme ortamı sağlanıyor
Bu yönergelerde, bir Microsoft Dynamics 365 Commerce önizleme ortamının sağlanmakta olduğu ele alınıyor. Bu adımları başarıyla tamamladıktan sonra, konfigüre edilmeye hazır bir önizleme ortamına sahip olursunuz. Burada açıklanan tüm etkinlikler LCS portalında yer alabilir.

*Lütfen önizleme uygulamasının önizleme uygulamanızda belirttiğiniz LCS hesabına ve kuruluşa bağlı olduğunu unutmayın. Sağlama için bu hesabı kullanmanız gerekir. Önizleme ortamı için farklı LCS hesabı veya kiracı kullanmanız gerekiyorsa, bize bu ayrıntıları girmeniz gerekir. İlgili kişi bilgileri için lütfen aşağıdaki "ek kaynaklar" başlığına bakın.*
### <a name="before-starting"></a>Başlatmadan önce
##### <a name="grant-access-to-e-commerce-applications"></a>E-ticaret uygulamalarına erişim ver

*Not: **Oturum açan kişinin AAD kiracı yöneticisiolması gerekir**. Bu adımı başarıyla tamamlamadan, sağlama adımlarının geri kalanı başarısız olacak.*

1. Bu adım için, **AAD kiracı kimliğiniz**gereklidir. Azure aboneliğinize erişmek için e-ticaret uygulamalarına yetki vermeniz gerekiyor. Bunu gerçekleştirmenin en kolay yolu URL'YI şöyle kullanmaktır:

https://login.windows.net/{AAD_TENANT_ID}/oauth2/authorize?client_id=fbcbf727-cd18-4422-a723-f8274075331a&response_type=code&redirect_uri=https://sb.manage.commerce.dynamics.com/_commerce/Consent&response_mode=query&prompt=admin_consent&state=12345

2. **Doğrudan URL 'yi tıklatmayın**, bunun yerine kopyalayıp tarayıcınıza veya metin düzenleyicisine yapıştırın ve url'ye gitmeden önce **\{AAD_TENANT_ID\}**'yi **AAD kiracı kimliğiniz** ile değiştirin.
3. Aboneliğinize "Dynamics 365 Commerce (Önizleme)" erişim vermek istediğinizi onaylamanız gereken Microsoft AAD Login iletişim kutusu görüntülenir.
4. İşlemin başarılı olduğunu doğrulayan bir sayfaya gönderilecektir.

##### <a name="log-in-to-the-lcs"></a>LCS'ta oturum açın
1. LCS portalda oturum açın: https://lcs.dynamics.com
1. Önizlemeye erişim istemek için kullandığınız LCS hesabıyla oturum açmış olduğunuzdan emin olun.
##### <a name="confirm-that-preview-features-are-available-and-enabled"></a>Önizleme özelliklerinin kullanılabilir ve etkin olduğunu onaylayın
1. LCS ön sayfasında, tüm yolu sağa kaydırın ve **önizleme özelliği yönetim** kutucuğunu tıklatın.
1. "ÖZEL ÖNİZLEME ÖZELLİKLERİ"ne gidin ve aşağıdaki özelliklerin kullanılabilir ve etkin olduğundan emin olun:
    1. **e-Ticaret değerlendirmesi**
    1. **Ticaret Önizleme Programı Ortamları**
1. Listede bu özellikleri göremiyorsanız, lütfen iş e-postanız, LCS hesabı ve kiracı ayrıntılarınız ile ilgili olarak bize başvurun. Bizimle bağlantı kurma hakkında bilgi için lütfen aşağıdaki **ek kaynaklara** bakın.

![Önizleme yönetimi kutucuğu](./media/preview1.png)

![Önizleme özellikleri](./media/preview2.png)
### <a name="create-project"></a>Proje oluştur
##### <a name="creating-new-project"></a>Yeni proje oluşturma
1. yeni bir proje oluşturmak için **+**'ya tıklayın.
1. Bir ortaksanız **taşı, çözüm oluştur ve öğren**'yi seçin.
1. Müşterisiyseniz, **olası ön satışlar**'ı seçin.
1. Uygun gördüğünüz şekilde bir ad, açıklama ve sektör girin.
1. **Ürün adı** olarak **Dynamics 365 Retail** seçeneğini belirleyin.
1. **Ürün sürümü** olarak **Dynamics 365 Retail** seçeneğini belirleyin.
1. **Metodoloji** için **Dynamics Retail uygulama metodoloji**'ı seçin.
1. İsterseniz varolan bir projedeki rolleri ve kullanıcıları içe aktarabilirsiniz.
1. **Oluştur**'a tıklayın.
1. Proje görünümüne gönderilecektir.
##### <a name="add-azure-connector"></a>Azure bağlayıcısı ekle
1. Ortaksanız, Araçlar kutucuklarındaki **proje ayarları** 'nı en sağa tıklatın.
1. Müşterisiyseniz, üst menüden **proje ayarları**  'nı seçin.
1. **Azure bağlayıcısı** seçin.
1. Bir Azure bağlayıcısı eklemek için, **+ Ekle**'ye tıklayın.
1. Bir ad girin.
1. **Azure abonelik kimliğinizi** girin.
1. **Azure Resource Manager (ARM) kullanmak için yapılandırı** etkinleştirin.
1. **Azure aboneliği AAD kiracı etki alanının (veya kimlik)** doğru olduğundan emin olun. Gerekiyorsa, Azure abonelik yöneticinize başvurun.
1. **İleri** düğmesini tıklatın.
1. Gerekli uygulamaların aboneliğinize erişim izni vermek için ekrandaki yönergeleri izleyin. Gerekiyorsa, Azure abonelik yöneticinize başvurun:
    1. Azure portalda oturum açın: https://portal.azure.com/
    1. Doğru dizin seçimi yaptığınızdan emin olun.
    1. Soldaki menüden **abonelikler**'i tıklatın.
    1. Listeden doğru aboneliği bulun ve seçin. Gerekiyorsa aramayı kullanın.
    1. Menüden **erişim denetimini (IAM)** seçin.
    1. Sağ tarafta **rol ataması eklemek** için **Ekle**'yi tıklatın. **Role atama ekle** bölmesi açılır.
    1. **Rol** için **katılımcı**'ı seçin.
    1. **Erişim atama** için **Azure AD kullanıcı, Grup veya hizmet sorumlusu** olarak bırakın.
    1. **Seç** altında, **b96b7e94-b82e-4e71-99a0-cf7fb188acea** girin.
    1. Listeden **Dynamics dağıtım hizmetlerini [wsfed-etkin]** seçin.
    1. **Kaydet**'e tıklayın.
1. **İleri** düğmesini tıklatın.
1. Gerekli uygulamaların aboneliğinize erişim izni vermek için ekrandaki yönergeleri izleyin. Gerekiyorsa, Azure abonelik yöneticinize başvurun.
1. **İleri** düğmesini tıklatın.
1. **Azure bölgesi** için, **Doğu ABD**, **Doğu ABD 2**, **Batı ABD** veya **Batı ABD 2** seçeneklerinden birini belirleyin.
1. **Bağlan** üzerine tıklayın.
1. Azure Bağlayıcınız listede görünmelidir.
### <a name="import-extension"></a>İçe aktarma uzantısı
1. En üstteki proje adını tıklatarak proje ön sayfasına geri dönün.
1. Ortaksanız, Araçlar kutucuklarındaki **Varlık kitaplığı** 'nı en sağa tıklatın.
1. Müşterisiyseniz, üst menüden **Varlık kitaplığı**'nı seçin.
1. Soldaki listeden **yazılımla dağıtılabilir paket** 'i seçin.
1. Eylem Bölmesinde, **İçeri Al**'a tıklayın.
1. **Paylaşılan varlık Kitaplığı**'nın altındaki kıymetler listesinden **Commerce Preview demo temel uzantıyı** seçin.
1. **Çekme** üzerine tıklayın.
1. Varlık kitaplığına iade edilecek ve listede uzantıyı görmelisiniz.

![Proje oluşturma - sürümler](./media/import.png)
### <a name="deploy-environment"></a>Ortamı dağıtın

*Not: tek seçeneği olan ekranlar atlandığından, 6, 7 ve/veya 8 numaralı adımlar gösterilmeyecektir. **Ortam parametreleri** görünümünde olduğunuzda, **ortam adı** alanının hemen üstündeki "Dynamics 365 Commerce (Önizleme) gösterisi (platform güncelleştirmesi 30 ile 10.0.6)" metnini kullandığınızı onaylayın. Aşağıdaki ekran görüntüsünde bakın.*

1. Üst menüden **bulut ile barındırılan ortamları** seçin.
1. Ortam eklemek için **+ Ekle**'yi tıklatın.
1. **Başvuru sürümü** için **10.0.6**'yi seçin.
1. **Platform sürümü** için **Platform Update 30**'i seçin.
1. **İleri** düğmesini tıklatın.
1. Ortam topolojisi için **demo** seçin.
1. Ortam topolojisi için, ( **Dynamics 365 Commerce Önizleme) - demo**'yu seçin.
1. Daha önce tek bir Azure Bağlayıcısı yapılandırdıysanız bu ortam için kullanılacak. Birden çok Azure Bağlayıcısı yapılandırdıysanız, kullanmak istediğiniz bağlayıcıyı seçebilirsiniz: **Doğu ABD**, **Doğu ABD 2**, **Batı ABD** veya **Batı ABD 2** (en iyi uçtan uca performans için önerilir)
1. Bir **ortam adı** girin.
1. Uygun gördüğünüz gibi VM boyutunu ayarlayın. (VM SKU **D13 v2** önerilir.)
1. **Gelişmiş ayarları** olduğu gibi bırakın.
1. Ekrandaki fiyat ve lisans koşullarını inceledikten sonra, sözleşmeyi belirtmek için kutusunu işaretleyin.
1. **İleri** düğmesini tıklatın.
1. Dağıtım onayı ekranında, ayrıntıların doğru olduğunu doğruladıktan sonra **Dağıt**'ı tıklatın.
1. **Bulut içinde barındırılan ortamlar** görünümüne geri dönersiniz ve ortamınız listede görünmelidir.
1. İstediğiniz ortam kuyruğa alındı ve sonra dağıtılıyor. Tüm ortam iş akışlarının tamamlanması biraz zaman alacaktır, bu nedenle lütfen birkaç saat sonra tekrar kontrol edin (yaklaşık 6 – 9 saat).
1. Devam etmeden önce, ortam durumlarınızın **dağıtıldığından** emin olun.

![Proje oluşturma - sürümler](./media/project1.png)

![Proje oluşturma - topoloji 1](./media/project2.png)

![Proje oluşturma - topoloji 2](./media/project3.png)

![Proje oluşturma - ortam parametreleri](./media/project4.png)
### <a name="initialize-rcsu"></a>RCSU başlatma
1. **Bulut barındırılan ortamlar** görünümünde, listeden ortamınızı seçin.
1. Ekranın sağ tarafındaki ortam görünümünden **tüm ayrıntılar**'ı tıklatın. Ortam ayrıntıları görünümü görüntülenir.
1. **Ortam özellikleri** altında, **Yönet**'i tıklatın.
1. **Perakende** sekmesinde, **Başlat**'ı tıklatın. RCSU başlatma parametreleri görünümü görüntülenir.
1. **BÖLGE** için, **Doğu ABD**, **Doğu ABD 2**, **Batı ABD** veya **Batı ABD 2** seçeneklerinden birini belirleyin.
1. **SÜRÜM** için, önce açılan listeden **bir sürüm belirtin**, sonra da aşağıda gösterilen metin alanında **9.16.19262.5** belirtin. *Not: Lütfen, RCSU'yu doğru sürüme güncelleştirmek için burada listelenen **sürümün aynısını belirttiğinizden** emin olun.*
1. **Uzantıyı uygula**'yı etkinleştirin.
1. Uzantılar listesinden, **Commerce Preview demo temel uzantısını** seçin.
1. **Başlat** öğesine tıklayın.
1. Dağıtım onayı ekranında, ayrıntıların doğru olduğunu doğruladıktan sonra **Evet**'i tıklatın.
1. **Perakende sekmesi** etkinleştirildiğinde, **Perakende** Yönetim görünümüne iade edilir. RCSU kaynak ayırma işlemi için sıraya alındı.
1. Devam etmeden önce RCSU durumunuz **başarılana** kadar bekleyin (yaklaşık olarak 2-5 saat sürer).
### <a name="initialize-e-commerce"></a>e-Ticaret başlat
1. **E-ticaret (Önizleme)** sekmesine geçin.
1. Önizleme onayını inceledikten sonra **kurulum**'u tıklatın.
1. **E-ticaret kiracı adı** için bir ad girin. Ancak, e-ticaret örneğinizi gösteren bazı URL'lerde bu dosyanın görülebileceğini unutmayın.
1. **Retail Cloud Scale Unit adı** için listeden RCSU seçin (listede yalnızca bir seçenek olmalıdır).
1. **e-ticaret coğrafya** otomatik olarak doldurulur ve değiştirilemez.
1. Devam etmek için **İleri**'yi tıklatın.
1. **Desteklenen ana bilgisayar adları** için geçerli bir etki alanı (örneğin, www.fabrikam.com) girin.
1. **AAD güvenlik grubu için sistem yöneticisine** ait, e-ticaret sistem yönetim grubu olarak kullanmak istediğiniz AAD SG kodunu girin.
1. **AAD güvenlik grubu için derecelendirmeler ve inceleme aracı** için, derecelendirme olarak kullanmak istediğiniz AAD SG kodunu girin ve denetleyici grubunu gözden geçirin.
1. **B2C** değerlerini boş bırakın (B2C ile başlayan 7 alan).
1. **Derecelendirmeleri ve inceleme hizmetini etkinleştiri** etkin durumda bırak.
1. **Başlat** öğesine tıklayın.
1. **Perakende sekmesi** etkinleştirildiğinde, **e-Ticaret (önizleme)** Yönetim görünümüne iade edilir. E-ticaret başlatma işlemi başlatıldı.
1. Devam etmeden önce, e-ticaret başlatma durumunuz **başlatma başarılı**olana kadar bekleyin.
1. Sağ altta **bağlantıların** altında.
    * **E-ticaret sitesine** bağlantıyı alın. Bu, C2 sitenizin köküne bağlantıdır.
    * **E-ticaret sitesi yönetim aracı** bağlantıyı alın. Bu, site yönetim aracı (C1 yazma aracı) bağlantıdır.
## <a name="post-provisioning-steps"></a>Sağlama sonrası adımlar
Bu aşamada, ortama uçtan uca sağlanacak, ancak ortamı değerlendirmeye başlamadan önce dikkate alınması gereken bazı yapılandırma adımları vardır.
### <a name="before-starting"></a>Başlatmadan önce
1. Üst menüden **bulut ile barındırılan ortamları** seçin.
1. Listeden ortamınızı seçin.
1. Sağdaki ortam bilgilerinden **tam ayrıntılar** 'ı tıklatın.
1. **Oturum aç**'ı tıklatın bir menü açmak için **ortamdaoturum aç**'ı seçin.

**USRT** hukuk varlığının seçildiğinden emin olun (sağ üst köşe).

### <a name="configure-pos"></a>POS konfigüre et
##### <a name="associate-worker-with-your-identity"></a>Çalışanı kimlikle ilişkilendir
1. Soldaki menüyü kullanarak, **Modüller > perakende > çalışanlar > İşçiler**'e gidin.
1. Listede, **000713 - Andrew Collette** kaydı bulun ve seçin.
1. Eylem Bölmesinde, **Perakende**'yi tıklayın.
1. **Var olan kimliği ilişkilendir**'i seçin.
1. **E-posta** alanında (**E-posta kullanarak arama**'nın sağındaki) e-posta adresinizi yazın.
1. **Ara**'ya tıklayın.
1. Adınızı taşıyan kaydı seçin.
1. **Tamam**'a tıklayın.
1. **Kaydet**'e tıklayın.
##### <a name="activate-cloud-pos"></a>Bulut POS'u etkinleştirme
1. LCS portalda oturum açın.
1. Projenize gidin.
1. Üst menüden **bulut ile barındırılan ortamları** seçin.
1. Listeden ortamınızı seçin.
1. Sağdaki ortam bilgilerinden **tam ayrıntılar** 'ı tıklatın.
1. **Oturum aç**'ı tıklatın bir menü açmak için **bulut satış noktasında oturum aç**'ı seçin, POS'un yüklenmesi gerekir.
1. **İleri** düğmesini tıklatın.
1. AAD hesabınızı bağlamak için oturum açın
1. **Mağaza adı** altında, **San Francisco**'yu seçin.
1. **İleri** düğmesini tıklatın.
1. **Kayıt ve aygıt** altında, **SANFRAN-1** seçin.
1. **Etkinleştir**'e tıklayın.
1. POS oturum açma ekranında oturumunuzu kapatıp açmanız gerekir.
1. Şimdi Operatör Kodu **000713** ve parola **123** kullanarak Cloud POS deneyimlerinde oturum açabilirsiniz.
### <a name="site-setup"></a>Site kurulumu
1. Daha önce not ettiğiniz URL'yi kullanarak **site yönetimi aracında** oturum açın.
1. Site kurulum iletişim kutusunu açmak için **Fabrikam** sitesine tıklayın.
1. Etki alanı için, e-ticaret başlatırken daha önce girdiğiniz etki alanını seçin.
1. Varsayılan kanal için, **Fabrikam genişletilmiş çevrimiçi mağaza**'yı seçin. *Not: **genişletilmiş** çevrimiçi mağazayı seçtiğinizden emin olun*
1. Varsayılan dil için **tr-tr** seçeneğini belirleyin.
1. **Yolu** olduğu gibi bırak.
1. **Tamam**'a tıklayın.
1. Sitedeki sayfalar listesine gönderilecektir.
### <a name="enable-jobs"></a>İşleri etkinleştir
1. Ortama oturum açın (HQ).
1. Soldaki menüyü kullanarak **perakende > Sorgulamalar ve raporlar > toplu işler**'e gidin.
1. Aşağıdaki listede bulunan her iş için aşağıdaki adımları gerçekleştirin:
    * **Perakende siparişi e-posta bildirimini işle**.
    * **Ürün bulunabilirliği**.
    * **P-0001**.
    * **Sipariş işlerini eşitle**.
1. Yukarıdaki adı (yukarıda belirtilen) kullanarak işi aramak için hızlı filtre'yi kullanın.
1. İşin durumu **stopaj** ise, aşağıdaki adımları gerçekleştirin:
    1. Etkin kaydı seçin.
    1. Eylem bölmesinden **toplu iş** şeridini açın ve **Durumu değiştir**'i tıklatın.
    1. **Bekleyen** seçeneğini belirleyin ve **Tamam** düğmesini tıklatın.
### <a name="run-full-data-sync"></a>Tam veri eşitlemeyi çalıştır
1. Soldaki menüyü kullanarak, **Modüller > Perakende > Genel merkez ayarı > Perakende planlayıcısı > Kanal veritabanı** gidin.
1. **Varsayılan** kanal, soldaki listeden seçilir. *Diğer kullanılabilir kanalı seçin (**scxxxxxxxxx**)*.
1. Eylem bölmesinden **tam veri eşitleme**'yi tıklatın.
1. Dağıtım planı olarak **9999**'ı seçin.
1. **Tamam**'a tıklayın.
1. **Tamam**'a tıklayın.
### <a name="after-these-steps-you-are-ready-to-start-evaluating-your-preview-environment"></a>Bu adımlardan sonra, önizleme ortamınızı değerlendirmeye başlamaya hazırsınız!
C2 tesis deneyimine gitmek için C1 yazma deneyimine ve **e-ticaret sitesi** URL'sine gitmek için **e-ticaret site yönetimi aracı** URL'sini kullanın.

## <a name="additional-resources"></a>Ek kaynaklar
### <a name="how-to-find-your-aad-tenant-id"></a>AAD kiracı kimliğiniz nasıl bulunur
AAD Kiracı kimliği bir GUID ve aşağıdaki örnekte olduğu gibi görünüyor: **72f988bf-86f1-41af-91ab-2d7cd011db47**
##### <a name="from-azure-portal"></a>Azure Portalından
1. Azure portalda oturum açın: https://portal.azure.com/
1. Doğru dizin seçimi yaptığınızdan emin olun.
1. Soldaki menüden **Azure Active Directory**'i tıklatın.
1. **Yönet** altında **Özellikler**'i seçin.
1. AAD Kiracı kimliği **dizin kimliği** altında gösteriliyor.
##### <a name="from-openid-connect-metadata"></a>OpenID bağlantı meta verileri
**\{YOUR_DOMAIN\}**'i etki alanınıza değiştirerek bir **openıd URL**'si oluşturun; örneğin, microsoft.com: https://login.microsoftonline.com/{YOUR_DOMAIN}/.well-known/openid-configuration; https://login.microsoftonline.com/microsoft.com/.well-known/openid-configuration olur

1. Etki alanınıza sahip **OpenID URL** 'sine gidin.
1. AAD Kiracı kimliği birden çok özellik değerlerinde görünebilir.
1. **login.microsoftonline.com/** sonra **authorization_endpoint** bulun ve GUID'yi doğrudan ayıklayın.
### <a name="how-to-find-the-id-of-your-aad-security-group"></a>AAD güvenlik grubunuzun kimliği nasıl bulunur
AAD güvenlik grup kimliği bir GUID ve aşağıdaki örnekte olduğu gibi görünüyor: **436ea7f5-ee6c-40c1-9f08-825c5811066a**

Bu adım, kullanıcının kimliği bulmaya çalıştığı grubun üyesi olduğunu varsayar.
1. Grafik Gezgini'ne gidin: https://developer.microsoft.com/en-us/graph/graph-explorer#
1. **Microsoft ile oturum aç**'ı tıklatın ve kimlik bilgilerinizi kullanarak oturum açın.
1. Oturum açtıktan sonra, soldan **daha fazla örnek göster**'i tıklatın.
1. **Grupları** sağ bölmeden etkinleştirin.
1. Sağ bölmeyi kapatın.
1. **Ait olduğum tüm grupları** tıklatın.
1. **Yanıt Önizleme** metin kutusundan grubunuzun yerini belirleyin.
1. Özellik **kimliği** altında güvenlik grubu kodu belirtiliyor.
### <a name="test-credit-card-information-to-perform-test-purchases"></a>Test satın almaları gerçekleştirmek için kredi kartı bilgilerini sına
Sitede test hareketleri gerçekleştirmek için, aşağıdaki test kredi kartı bilgilerini kullanabilirsiniz:

Kart numarası: 4111-1111-1111-1111, bitiş tarihi: 10/20, CVV: 737

*Not: herhangi bir koşulda test sitesinde gerçek kredi kartı bilgilerini kullanmaya çalışmayın!*
### <a name="useful-links"></a>Faydalı bağlantıları
* [LCS (Lifecycle services)](https://docs.microsoft.com/en-us/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide)
* [RCSU (Retail Cloud Scale Unit)](https://docs.microsoft.com/en-us/business-applications-release-notes/october18/dynamics365-retail/retail-cloud-scale-unit)
* [Microsoft Azure portalı](https://azure.microsoft.com/en-us/features/azure-portal)
* [Dynamics 365 Commerce web sitesi](https://aka.ms/Dynamics365CommerceWebsite)
* [Dynamics 365 Retail için yardım kaynakları](../retail/index.md)
### <a name="microsoft-dynamics-365-commerce-preview-support"></a>Microsoft Dynamics 365 Commerce Önizleme desteği
Sağlama adımlarını gerçekleştirirken sorunlarla karşılaşırsanız, yardım için lütfen [Microsoft Dynamics 365 Commerce Önizleme Yammer grubunu](https://aka.ms/Dynamics365CommercePreviewYammer) ziyaret edin. 

Yammer Gruba erişim sorunlarınız varsa, **Dynamics365Commerce@microsoft.com** adresinden e-posta yoluyla da bize ulaşabilirsiniz. Bu e-posta adresi etkin olarak izlenmedi; bu nedenle yanıt olarak bir gecikme beklenir.
***
## <a name="prerequisites-for-optional-features"></a>İsteğe bağlı özellikler için Önkoşullar
İşlem e-posta özelliklerini değerlendirmek istiyorsanız, aşağıdaki önkoşulların karşılanması gerekir:
* Kullanılabilir bir e-posta sunucunuz var (SMTP sunucusu); Bunlar, önizleme ortamını temin ettiğiniz Azure aboneliğinden kullanılabilir.
* Sunucunun FQDN/IP, SMTP bağlantı noktası numaranız ve kullanılabilir kimlik doğrulama detayları vardır.

Yeni çok yönlü kanal görüntülerini özellikle en iyi şekilde karşılayan dijital varlık yönetimi özelliklerini değerlendirmek istiyorsanız, aşağıdaki önkoşulların karşılanması gerekir:
* **CMS kiracı adınızın** kullanılabilir olması gerekir. Bu adı bulma yönergeleri aşağıdadır.
### <a name="configure-image-backend-optional"></a>Görüntü arka uç Yapılandır (isteğe bağlı)
##### <a name="finding-your-media-base-url"></a>Medya taban URL 'niz bulunuyor
*Not: Bu adımı tamamlayabilmek için, önce **site kurulumunu** tamamlamanız gerekir.*
1. Daha önce not ettiğiniz URL'yi kullanarak site yönetimi aracında oturum açın.
1. **Fabrikam** sitesini açın.
1. Soldaki menüden **Varlıkları** seçin.
1. Herhangi bir tek resim varlığı seçin.
1. Sağdaki Özellik denetçisinden **ortak URL** 'yi bulun. İçinde bir URL var.
    * Örnek URL: https://images-us-sb.cms.commerce.dynamics.com/cms/api/fabrikam/imageFileData/MA1nQC
1. URL'deki son tanımlayıcıyı (Yukarıdaki örnek URL'de MA1nQC) aşağıdaki dizeyle Değiştirin: **search?fileName=**
    * Değiştirmeden sonraki örnek URL: https://images-us-sb.cms.commerce.dynamics.com/cms/api/fabrikam/imageFileData/search?fileName=
    * Bu, **ortam taban URL'sidir** - bunu not alın.
##### <a name="updating-the-media-base-url"></a>Ortam temel URL'si güncelleştiriliyor
1. Ortama oturum açın (HQ).
1. Soldaki menüyü kullanarak, **Modüller > Perakende > Kanal ayarı > Kanal profilleri** gidin.
1. **Düzenle**'yi tıklatın.
1. **Profil özelliklerinden**, **ortam sunucusu temel URL'sinin** özellik değerini daha önce oluşturduğunuz **ortam taban URL**'siyle değiştirin.
1. Soldaki listeden, **varsayılan** kanal altında diğer kanalı seçin.
1. **Profil özellikleri** altında, **+ Ekle**'yi tıklatın.
1. Eklenen özellik için, **ortam sunucusu temel URL**'yi Özellik anahtarı olarak ve özellik değeri için, önceden oluşturduğunuz **ortam taban URL'sini** girin.
1. **Kaydet**'e tıklayın.

### <a name="configure-email-server-optional"></a>E-posta sunucusunu yapılandır (isteğe bağlı)
Burada girdiğiniz SMTP sunucusu ya da e-posta hizmetinin, ortam için kullandığınız Azure aboneliği içinden erişilebilir olması gerektiğini unutmayın.
1. Ortama oturum açın (HQ).
1. Soldaki menüyü kullanarak, **Modüller > Perakende > Genel merkez ayarı > Parametreler > E-posta parametreleri** gidin.
1. **SMTP ayarları** sekmesine tıklayın.
1. **Giden posta sunucusu alanında**, SMTP sunucunuzun veya e-posta hizmetinizin FQDN'sini veya IP adresini yazın.
1. **SMTP bağlantı noktası numarası** alanına, bağlantı noktası numarasını girin (varsayılan, SSL kullanırken 25'tir).
1. **Kullanıcı adı** alanına bir değer yazın (kimlik doğrulama gerekliyse).
1. **Parola** alanına bir değer yazın (kimlik doğrulama gerekliyse).
1. **Kaydet**'e tıklayın.
1. **Yenile**'yi tıklatın.
1. **Test epostası** sekmesine tıklayın.
1. E-posta sağlayıcısı alanında **SMTP** 'yi seçin.
1. **Gönder** alanına, test e-adresinin teslim edilmesini istediğiniz e-posta adresini girin.
1. **Test e-postası gönder**'i tıklayın.
### <a name="configure-email-templates-optional"></a>E-posta şablonlarını yapılandır (isteğe bağlı)
E-postalarını göndermek istediğiniz her işlemsel olay için e-posta şablonunun geçerli bir gönderen e-posta adresiyle güncelleştirilmesi gerekir.
1. Soldaki menüyü kullanarak, **Modüller > Kuruluş yönetimi > Kurulum > Kuruluş e-posta şablonları** gidin.
1. **Listeyi göster**'i tıklatın.
1. Listedeki her şablon için:
    1. **Gönderen e-postası** alanına bu e-posta şablonunun gönderen e-posta adresini yazın.
    1. İsteğe bağlı **Gönderen adı** alanına bu e-posta şablonu için gönderen olarak kullanılacak bir ad yazın.
1. **Kaydet**'e tıklayın.
### <a name="customizing-email-templates-optional"></a>E-posta şablonlarını özelleştirme (isteğe bağlı)
E-posta şablonlarını farklı görüntüler kullanmak üzere özelleştirmek veya önizleme ortamınıza geri bağlantı sağlamak için şablondaki bağlantıları güncelleştirmek isteyebilirsiniz. Aşağıdaki adımlar varsayılan şablonların nasıl karşıdan yükleneceğini açıklar, bunları özelleştirin ve sistemdeki şablonları güncelleştirir.
1. Tarayıcı kullanarak, aşağıdaki HTML belgelerini yerel bilgisayarınıza içeren [Microsoft Dynamics 365 Commerce Preview varsayılan e-posta şablonları. zip dosyasını](https://download.microsoft.com/download/d/7/b/d7b6c4d4-fe09-4922-9551-46bbb29d202d/Commerce.Preview.Default.Email.Templates.zip) karşıdan yükleyin.
    1. Sipariş onayı şablonu
    1. Hediye kartı şablonu
    1. Yeni sipariş şablonu
    1. Paket sipariş şablonu
    1. Sipariş şablonu al
1. Metin veya HTML Düzenleyicisi kullanarak şablonları özelleştirin. Lütfen aşağıdaki desteklenen belirteçlerin listesine bakın.
1. Ortama oturum açın (HQ).
1. Soldaki menüyü kullanarak, **Modüller > Perakende > Genel merkez ayarı > Parametreler > Kuruluş e-posta şablonları** gidin.
1. Tüm şablonları görmek için soldaki listeyi genişletin.
1. Özelleştirmek istediğiniz şablonların her biri için aşağıdaki adımları uygulayın:
    1. Listeden şablonunu seçin.
    1. **E -posta iletisi içeriği** altında, listeden uygun dil sürümünü seçin (varsayılan **en-US**).
    1. **E-posta iletisi içeriği** altında **Düzenle**'i tıklatın, sonra **e-posta şablonu yükle** bölmesini açma konusuna bakın.
    1. **Gözat**'ı tıklatın ve özelleştirilmiş içeriğe sahip HTML dosyasını bulun.
    1. **Yükle**'yi tıklatın, şablonunuz sisteme yüklenir ve bir önizleme gösterilir.
    1. **Tamam**'a tıklayın.
    1. İsteğe bağlı Şablonun **konu** özelliğini özelleştirin.
    1. **Kaydet**'e tıklayın.

#### <a name="supported-tokens-in-the-email-template"></a>E-posta şablonunda desteklenen belirteçler
Bu belirteçler, müşteriye uygulanan gerçek değerlerle e-posta işleme zamanında değiştirilecek.

**Satış siparişi** - Aşağıdaki belirteçler genel satış siparişi için geçerlidir.

|Belirtecin adı|Belirteç|
|---|---|
|Sipariş numarası|%salesid%|
|Müşteri adı|%customername%|
|Teslimat adresi|%deliveryaddress%|
|Fatura adresi|%customeraddress%|
|Sipariş tarihi|%shipdate%|
|Teslimat şekli|%modeofdelivery%|
|İskonto|%discount%|
|Satış vergisi|%tax%|
|Sipariş toplamı|%total%|

**Satış satırı** - aşağıdaki belirteçler siparişteki her ürün için doldurulur.

*Not: **ürün listesi - başlangıç** ve **ürün listesi - bitiş** belirteçlerini, her ürün için yinelenen HTML bloğunun başına ve sonuna yerleştirin.*

|Belirtecin adı|Belirteç|
|---|---|
|Ürün listesi - başlangıç|\<!--%tablebegin.salesline% -->|
|Ürün listesi - bitiş|\<!--%tableend.salesline%-->|
|Ürün adı|%lineproductname%|
|Tanım|%lineproductdescription%|
|Miktar|%linequantity%|
|Satır birim fiyatı|%lineprice% (doğrula)|
|satır maddesi toplamı|%linenetamount%|
|satır iskontosu|%linediscount%|
|Sevk tarihi|%lineshipdate%|
|Tedarik yöntemi|%linedeliverymode%|
|teslimat adresi|%linedeliveryaddress%|
|Satırın satış birimi|%lineunit%|

