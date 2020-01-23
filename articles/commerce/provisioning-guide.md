---
title: Commerce önizleme ortamı sağlama
description: Bu konu, hazırlandıktan sonra Microsoft Dynamics 365 Commerce önizleme ortamının nasıl yapılandırılacağını açıklamaktadır.
author: psimolin
manager: annbe
ms.date: 01/06/2020
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
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: b77d2cbbc100aeae5dcd53ddbe69ff2e4435da13
ms.sourcegitcommit: 4d77d06a07ec9e7a3fcbd508afdffaa406fd3dd8
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/06/2020
ms.locfileid: "2934760"
---
# <a name="provision-a-commerce-preview-environment"></a>Commerce önizleme ortamı sağlama

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

Bu konu, hazırlandıktan sonra Microsoft Dynamics 365 Commerce önizleme ortamının nasıl yapılandırılacağını açıklamaktadır.

Başlamadan önce, işlemin ne olduğunu ve konunun neler içerdiğini öğrenmek için belgeleri en azından bir fikir almak için inclemeenizi öneririz.

> [!NOTE]
> Dynamics 365 Commerce önizleme'ye erişim izni verilmemişse, [Commerce Web sitesinden](https://aka.ms/Dynamics365CommerceWebsite) önizleme erişimi isteyebilirsiniz.

## <a name="overview"></a>Genel Bakış

Commerce önizleme ortamınızı başarıyla sağlamak için, belirli bir ürün adı ve türü olan bir proje oluşturmanız gerekir. Ortam ve Retail Cloud Scale Unit (RCSU), ayrıca, e-ticaret sağlamasının daha sonra başlatmak için kullanmanız gereken belirli parametreleri de vardır. Bu konudaki yönergeler, tamamlamanız gereken tüm gerekli adımları ve kullanmanız gereken parametreleri açıklar.

Sağlama başarılı olduktan sonra, Ticari önizleme ortamınızı hazırlamak için almanız gereken birkaç son işlem adımı vardır. Sistemin hangi yönlere göre değerlendirileceğini bağlı olarak bazı adımlar isteğe bağlıdır. İsteğe bağlı adımları istediğiniz zaman daha sonra da tamamlayabilirsiniz.

Commerce önizleme ortamını yapılandırma hakkında bilgi için bkz. [Commerce önizleme ortamı yapılandırma](cpe-post-provisioning.md). Commerce Preview ortamınızla ilgili isteğe bağlı özellikleri konfigüre etmek için, bkz. [Commerce önizleme ortamınız için isteğe bağlı özellikler yapılandırın](cpe-optional-features.md).

Sağlama adımlarıyla ilgili sorularınız varsa veya herhangi bir sorunla karşılaşırsanız, lütfen [Microsoft Dynamics 365 Commerce önizleme Yammer grubunda](https://aka.ms/Dynamics365CommercePreviewYammer) Microsoft'a bildirin.

## <a name="prerequisites"></a>Önkoşullar

Commerce önizleme ortamınızı hazırlayabilmeniz için aşağıdaki önkoşulların yerinde olması gerekir:

- Microsoft Dynamics Lifecycle Services (LCS) portalına erişim hakkınız var
- Dynamics 365 Commerce Önizleme programına kabul edilmiş olabilirsiniz.
- **Olası ön satışlar** için bir proje oluşturmak veya **geçiş yapmak, çözüm oluşturmak ve daha fazla bilgi** edinmek için gerekli izinleriniz vardır.
- Ortamı sağlamak istediğiniz **Ortam yöneticisi** veya **Proje sahibi** rolünün bir üyesisinizdir.
- Microsoft Azure aboneliğinize yönetici erişiminiz var veya sizin adınıza yönetici izinleri gerektiren iki adımı gerçekleştirebilecek bir abonelik Yöneticisi ile ilişki kurun.
- Azure Active Directory (Azure AD) kiracı kimliğiniz kullanılabilir.
- E-ticaret sistem yöneticileri grubu olarak kullanılacak bir Azure AD güvenlik grubu oluşturdunuz ve kimliğiniz kullanılabilir
- Derecelendirme ve incelemeler grubu olarak kullanılacak bir Azure AD güvenlik grubu oluşturdunuz ve kimliğiniz kullanılabilir (Bu güvenlik grubu e-ticaret Sistem Yöneticisi grubuyla aynı olabilir.)

### <a name="find-your-azure-ad-tenant-id"></a>Azure AD kiracı kimliğinizi bulun

Azure AD kiracı kimliğiniz, bu örneğe benzeyen bir genel benzersiz tanımlayıcıdır (GUID): **72f988bf-86f1-41af-91ab-2d7cd011db47**.

#### <a name="find-your-azure-ad-tenant-id-by-using-the-azure-portal"></a>Azure portalını kullanarak Azure AD kiracı kimliğinizi bulun

1. [Azure portalında](https://portal.azure.com/) adresinden oturum açın.
1. Doğru dizin seçimi yaptığınızdan emin olun.
1. Soldaki menüden **Azure Active Directory** seçin.
1. **Yönet** altında **Özellikler**'i seçin. Azure AD kiracı kimliğiniz **dizin kimliği** altında görünür.

#### <a name="find-your-azure-ad-tenant-id-by-using-openid-connect-metadata"></a>OpenID bağlantı meta verilerini kullanarak Azure AD kiracı kimliğinizi bulun

Etki alanınızı `microsoft.com` gibi **\{ETKİ\_ALANI\}** ile değiştirerek bir OpenID URL'si oluşturun. Örneğin, `https://login.microsoftonline.com/{YOUR_DOMAIN}/.well-known/openid-configuration`, `https://login.microsoftonline.com/microsoft.com/.well-known/openid-configuration` olur.

1. Etki alanınızı içeren OpenID URL'sine gidin.

    Azure AD kiracı kimliğinizi birden çok özellik değerlerinde bulabilirsiniz.

1. **yetkilendirme\_bitişnoktası**'nı bulun, hemen `login.microsoftonline.com/` sonrasında görünen GUID'i çıkarın.

### <a name="find-your-azure-ad-security-group-id"></a>Azure AD güvenlik grubu kimliğinizi bulun

Azure AD güvenlik grubunuzun kodu aşağıdaki örneğe benzer bir GUID'dir: **436ea7f5-ee6c-40c1-9f08-825c5811066a**.

Bu yordam, kimliğini bulmaya çalıştığınız grubun bir üyesi olduğunuzu varsayar.

1. [Grafik Gezginini](https://developer.microsoft.com/graph/graph-explorer#) açın.
1. **Microsoft ile oturum aç**'ı tıklatın ve kimlik bilgilerinizi kullanarak oturum açın.
1. Solda, **diğer örnekleri göster**'i seçin.
1. **Grupları** sağ bölmeden etkinleştirin.
1. Sağ bölmeyi kapatın.
1. **Ait olduğum tüm grupları** seçin.
1. **Yanıt Önizleme** alanında, grubunu bulun. Güvenlik grubu kodu, **ID** özelliği altında görünür.

## <a name="provision-your-commerce-preview-environment"></a>Commerce önizleme ortamınızı sağlama

Bu yöntemlerde, bir Commerce Preview ortamının nasıl sağlanacağı açıklamaktadır. Bunları başarıyla tamamladıktan sonra, Commerce Preview ortamı konfigürasyon için hazır olacak. Burada açıklanan tüm etkinlikler LCS portalında yer alabilir.

> [!IMPORTANT]
> Önizleme erişimi, önizleme uygulamanızda belirttiğiniz LCS hesabına ve kuruluşa bağlıdır. Commerce Preview ortamını sağlamak için aynı hesabı kullanmanız gerekir. Commerce Preview ortamı için farklı bir LCS hesabı veya kiracı kullanmanız gerekiyorsa, bu ayrıntıları Microsoft'a sağlamanız gerekir. Başvuru bilgileri için bu konudaki [Commerce önizleme ortam desteği](#commerce-preview-environment-support) başlıklı bölüme bakın.

### <a name="grant-access-to-e-commerce-applications"></a>E-ticaret uygulamalarına erişim ver

> [!IMPORTANT]
> Oturum açan kişinin Azure AD kiracı kimliğine sahip bir Azure AD kiracı yöneticisi olması gerekir. Bu adım başarılı bir şekilde tamamlanmazsa, kalan sağlama adımları başarısız olur.

E-ticaret uygulamalarına Azure aboneliğinize erişim yetkisi vermek için aşağıdaki adımları izleyin.

1. URL'yi aşağıdaki biçimde birleştirin:

    `https://login.windows.net/{AAD_TENANT_ID}/oauth2/authorize?client_id=fbcbf727-cd18-4422-a723-f8274075331a&response_type=code&redirect_uri=https://sb.manage.commerce.dynamics.com/_commerce/Consent&response_mode=query&prompt=admin_consent&state=12345`

1. URL'yi kopyalayıp tarayıcınıza veya metin düzenleyicisine yapıştırın ve **\{AAD\_KİRACI\_KİMLİĞİ\}** Azure AD kiracı kimliğiniz ile değiştirin. URL'yi açın.
1. Azure AD oturum aç iletişim kutusunda oturum açın ve aboneliğinize **Dynamics 365 Commerce** erişimi vermek istediğinizi doğrulayın. İşlemin başarılı olduğunu gösteren bir sayfaya gönderilecektir.

### <a name="confirm-that-preview-features-are-available-and-turned-on-in-lcs"></a>Önizleme özelliklerinin kullanılabilir ve LCS'de açık olduğunu onaylayın

Önizleme özelliklerinin kullanılabilir ve LCS'de açık olduğunu onaylamak için bu adımları izleyin.

1. Bu önizlemeye erişim istemek için kullandığınız LCS hesabını kullanarak [LCS portalında](https://lcs.dynamics.com) oturum açın.
1. LCS ana sayfasında, tüm yolu sağa kaydırın ve **önizleme özelliği yönetim** kutucuğunu tıklatın.

    ![Önizleme yönetimi kutucuğu](./media/preview1.png)

1. **ÖZEL ÖNİZLEME ÖZELLİKLERİ**'ne gidin ve aşağıdaki özelliklerin kullanılabilir ve açık olduğundan emin olun:

    - e-Ticaret değerlendirmesi
    - Ticaret Önizleme Programı Ortamları

    ![Özel önizleme özellikleri](./media/preview2.png)

1. Listede bu özellikler görüntülenmiyorsa, Microsoft'a başvurun ve iş e-posta adresiniz, LCS hesabı ve kiracı ayrıntılarını sağlayın. Başvuru bilgileri için [Commerce önizleme ortam desteği](#commerce-preview-environment-support) başlıklı bölüme bakın.

### <a name="create-a-new-project"></a>Yeni proje oluştur

LCS'de bir yeni proje oluşturmak için şu adımları izleyin.

1. LCS giriş sayfasında, bir proje oluşturmak için artı işaretini (**+**) seçin.
1. Sağ bölmede aşağıdaki adımlardan birini izleyin:

    - Bir ortaksanız **taşı, çözüm oluştur ve öğren**'yi seçin.
    - Müşterisiyseniz, **olası ön satışlar**'ı seçin.

1. Şablon adı, açıklama ve sektör girin.
1. **Ürün adı** alanından **Dynamics 365 Retail** seçin.
1. **Ürün sürümü** alanından **Dynamics 365 Retail** seçin.
1. **Metodoloji** alanında **Dynamics Retail uygulama metodoloji**'ı seçin.
1. İsteğe bağlı: Roller ve kullanıcılar mevcut projeden içeri aktarabilirsiniz.
1. **Oluştur**'u seçin. Proje görünümü gösterilir.

### <a name="add-the-azure-connector"></a>Azure bağlayıcısı ekle

Bir Azure Connector'ı LCS projenize eklemek için aşağıdaki adımları izleyin.

1. Şu adımlardan birini izleyin:

    - Ortak iseniz, en sağdaki **proje ayarları** kutucuğunu seçin.
    - Müşterisiyseniz, üst menüden **proje ayarları**'nı seçin.

1. **Azure bağlayıcısı** seçin.
1. Bir Azure bağlayıcısı eklemek için, **Ekle**'ye tıklayın.
1. Bir ad girin.
1. Azure abonelik kimliğinizi girin.
1. **Azure Resource Manager (ARM) kullanmak için yapılandırın** seçeneğini açın.
1. **Azure aboneliği AAD kiracı etki alanının (veya kimlik)** değerinin doğru olduğundan emin olun. Gerekiyorsa, Azure abonelik yöneticinize başvurun.
1. **Sonraki**'yi seçin.
1. Gerekli uygulamaların aboneliğinize erişim izni vermek için sayfadaki yönergeleri izleyin. Gerekiyorsa, Azure abonelik yöneticinize başvurun.

    1. [Azure portalında](https://portal.azure.com/) adresinden oturum açın.
    1. Doğru dizinin seçildiğinden emin olun ve soldaki menüde **Abonelikler**'i seçin.
    1. Listeden doğru aboneliği bulun ve seçin. Gerektiğinde arama işlevini kullanın.
    1. Menüde, **erişim denetimi (IAM)** seçeneğini belirleyin.
    1. Sağ tarafta **rol ataması eklemek** için **Ekle**'yi tıklatın. **Role atama ekle** bölmesi görünür.
    1. **Rol** alanında **Katkı sağlayan**'i seçin.
    1. **Erişimi ata** alanında, varsayılan değeri, **Azure AD kullanıcıyı, grubu veya servis sorumlusunu** bırakın.
    1. **Seç** altında, **b96b7e94-b82e-4e71-99a0-cf7fb188acea** girin.
    1. Listeden **Dynamics dağıtım hizmetlerini \[wsfed-etkin\]** seçin.
    1. **Kaydet**'i seçin.

1. **Sonraki**'yi seçin.
1. Gerekli uygulamaların aboneliğinize erişim izni vermek için sayfadaki yönergeleri izleyin. Gerekiyorsa, Azure abonelik yöneticinize başvurun.
1. **Sonraki**'yi seçin.
1. **Azure bölgesi** alanında, **Doğu ABD**, **Doğu ABD 2**, **Batı ABD** veya **Batı ABD 2** seçeneklerinden birini belirleyin.
1. **Bağlan**'ı seçin. Azure Bağlayıcınız listede görünmelidir.

### <a name="import-the-commerce-preview-demo-base-extension"></a>Commerce önizleme demo temel uzantısını içe aktar

Commerce Önizleme demo temel uzantısını projenize içe aktarmak için aşağıdaki adımları izleyin.

1. En üstte proje adını seçerek projenizin giriş sayfasını açın.
1. Şu adımlardan birini izleyin:

    - Ortak iseniz, en sağdaki **Varlık kitaplığı** kutucuğunu seçin.
    - Müşterisiyseniz, üst menüden **Varlık kitaplığı**'nı seçin.

1. Soldaki listeden **yazılımla dağıtılabilir paket**'i seçin.
1. **İçe aktar**'ı seçin.
1. **Paylaşılan varlık kitaplığı**'nın altındaki kıymetler listesinden **Commerce önizleme demo temel uzantıyı** seçin.
1. **Çek**'i seçin. Varlık kitaplığına iade edilecek ve listede uzantıyı görmelisiniz.

Aşağıdaki şekilde, LCS **varlık Kitaplığı** sayfasında yapılması gereken eylemler gösterilmektedir.

![Commerce önizleme demo temel uzantısını içe aktarma](./media/import.png)

### <a name="deploy-the-environment"></a>Ortamı dağıtın

Ortamı dağıtmak için şu adımları izleyin.

> [!NOTE]
> Tek bir seçeneği olan sayfalar atlandığından 6., 7. ve/veya 8. adımı tamamlamanız gerekmez. **Ortam parametreleri** görünümünde olduğunuzda, **Dynamics 365 Commerce**'in **ortam adı** alanının metin (Önizleme)-demo (30 platform güncelleştirmesi 10.0.6) ile doğrudan göründüğünü onaylayın. 8. adımdan sonra görünen çizime bakın.

1. Üst menüden **bulut ile barındırılan ortamları** seçin.
1. Ortam eklemek için **Ekle**'yi tıklatın.
1. **Uygulama sürümü** alanından **10.0.6** seçin.
1. **Platform sürümü** alanında **Platform Update 30**'i seçin.

    ![Uygulamayı ve platform sürümünü seçme](./media/project1.png)

1. **Sonraki**'yi seçin.
1. Ortam topolojisi olarak **Demo**'yu seçinç

    ![Ortam topolojisini 1 seçme](./media/project2.png)

1. Ortam topolojisi olarak **Dynamics 365 Commerce (Önizleme) - Demo**'yu seçin. Daha önce tek bir Azure Bağlayıcısı yapılandırdıysanız bu ortam için kullanılacak. Birden fazla Azure Bağlayıcısı konfigüre ediyorsanız, hangi bağlayıcının kullanılacağını seçebilirsiniz: **Doğu ABD**, **Doğu ABD 2**, **Batı ABD** veya **Batı ABD 2**. (En iyi uçtan uca performans için, **Batı ABD 2**'yi seçmeniz önerilir.)

    ![Ortam topolojisini 2 seçme](./media/project3.png)

1. **Ortam dağıt** sayfasında bir ortam adı girin. Gelişmiş ayarları olduğu gibi bırakın.

    ![Ortamı dağıtın sayfası](./media/project4.png)

1. VM boyutunu gerektiği gibi ayarlayın. (VM stok tutma birimi \[SKU\] **D13 v2**.)
1. Fiyat ve lisans koşullarını gözden geçirin ve kabul ettiğiniz onay kutusunu işaretleyin.
1. **Sonraki**'yi seçin.
1. Dağıtım onayı sayfasında, ayrıntıların doğru olduğunu doğruladıktan sonra **Dağıt**'ı seçin. **Bulut içinde barındırılan ortamlar** görünümüne geri dönersiniz ve ortamınız listede görünmelidir.

    İstediğiniz ortam kuyruğa alındı ve sonra dağıtılıyor. Ortam iş akışlarının tamamlanması biraz zaman alır. Bu nedenle, yaklaşık altı ile dokuz saatten sonra yeniden kontrol edin.

1. Devam etmeden önce, ortam durumlarınızın **dağıtıldığından** emin olun.

### <a name="initialize-rcsu"></a>RCSU başlatma

Bir RCSU başlatmak için şu adımları izleyin.

1. **Bulut barındırılan ortamlar** görünümünde, listeden ortamınızı seçin.
1. Sağdaki ortam görünümünde **tam ayrıntılar** 'ı tıklatın. Ortam ayrıntıları görünümü görüntülenir.
1. **Ortam özellikleri** altında, **Yönet**'i tıklatın.
1. **Perakende** sekmesinde, **Başlat**'ı seçin. RCSU başlatma parametreleri görünümü görüntülenir.
1. **Bölge** alanında, **Doğu ABD**, **Doğu ABD 2**, **Batı ABD** veya **Batı ABD 2** seçeneklerinden birini belirleyin.
1. **Sürüm** alanında, listeden bir **sürüm belirtin** ve sonra görüntülenen alanda **9.16.19262.5** belirtin. Burada belirtilen sürümü tam olarak belirttiğinizden emin olun. Aksi durumda, RCSU öğesini daha sonra doğru sürüme güncelleştirmeniz gerekir.
1. **Uzantıyı Uygula** seçeneğini açın.
1. Uzantılar listesinden, **Commerce Önizleme demo temel uzantısını** seçin.
1. **Başlat**'ı seçin.
1. Dağıtım onayı sayfasında, ayrıntıların doğru olduğunu doğruladıktan sonra **Evet**'i seçin. **Perakende** sekmesi etkinleştirildiğinde, **Perakende Yönetim** görünümüne iade edilir. RCSU kaynak ayırma işlemi için sıraya alındı.
1. Devam etmeden önce, RCSU durumlarınız **Başarılı** olur. Başlatma yaklaşık iki ile beş saat arasında sürer.

### <a name="initialize-e-commerce"></a>e-Ticaret başlat

Bir e-Ticaret başlatmak için şu adımları izleyin.

1. **E-ticaret (Önizleme)** sekmesinde, önizleme onayını gözden geçirip **kurulum**'u seçin.
1. **E-ticaret kiracı adı** için bir ad girin. Ancak, e-ticaret örneğinizi gösteren bazı URL'lerde bu dosyanın görülebileceğini unutmayın.
1. **Retail Cloud Scale Unit adı** alanında, listesindeki RCSU alanını seçin. (Listede yalnızca bir seçenek bulunmalıdır.)

    **E-ticaret coğrafyası** alanı otomatik olarak ayarlanır ve değer değiştirilemez.

1. Devam etmek için **İleri**'yi seçin.
1. **Desteklenen ana bilgisayar adları** alanında, `www.fabrikam.com` gibi geçerli herhangi bir etki alanını girin.
1.  **Sistem Yöneticisi için AAD güvenlik grubunda** alanına, kullanmak istediğiniz güvenlik grubunun adının ilk birkaç harfini girin. Arama sonuçlarını görüntülemek için büyüteç simgesini seçin. Listeden bir güvenlik grubunu seçin.
2.  **Derecelendirme ve inceleme moderatörü için AAD güvenlik grubunda** alanına, kullanmak istediğiniz güvenlik grubunun adının ilk birkaç harfini girin. Arama sonuçlarını görüntülemek için büyüteç simgesini seçin. Listeden bir güvenlik grubunu seçin.
1. **Derecelendirmeleri etkinleştir ve gözden geçirme hizmeti** seçeneğini açık olarak bırakın.
1. "E-ticaret uygulamalarına erişim izni verme" bölümünde açıklandığı gibi Microsoft Azure Active Directory (Azure AD) onay adımını önceden tamamladıysanız, onayınızı onaylamak için onay kutusunu seçin. Bu adımı henüz tamamlamadınız, başlatma işlemine devam etmeden önce bunu yapmanız gerekir. Kabul iletişim kutusunu açmak ve adımı tamamlamak için onay kutusunun yanındaki metinde bulunan bağlantıyı seçin.
1. **Başlat**'ı seçin. **e-Ticaret (önizleme) sekmesi** seçildiğinde, **Perakende Yönetim** görünümüne iade edilir. E-ticaret başlatma işlemi başlatıldı.
1. Devam etmeden önce, e-ticaret başlatma durumunuz **başlatma başarılı** olana kadar bekleyin.
1. Alt sağdaki **bağlantılar** altında, aşağıdaki bağlantıların URL 'lerini not alın:

    * **e-ticaret sitesi** – E-ticaret sitenizin köküne olan bağlantı.
    * **e-ticaret site yönetimi aracı** – site yönetimi aracına bağlantı.

## <a name="commerce-preview-environment-support"></a>Commerce önizleme ortamı desteği

Sağlama adımlarını gerçekleştirirken sorunlarla karşılaşırsanız, yardım için lütfen [Microsoft Dynamics 365 Commerce Önizleme Yammer grubunu](https://aka.ms/Dynamics365CommercePreviewYammer) ziyaret edin.

Yammer Gruba erişmeye çalıştığınızda sorunlarla karşılaşırsanız, Microsoft'a e-posta ile başvurabilirsiniz:  <Dynamics365Commerce@microsoft.com>. Bu e-posta adresi etkin şekilde izlenmiyor. Bu nedenle, yanıtta bir gecikme olmasını bekler.

## <a name="next-steps"></a>Sonraki adımlar

Commerce önizleme ortamını hazırlam ve yapılandırma işlemine devam etmek için bkz. [Commerce önizleme ortamı yapılandırma](cpe-post-provisioning.md).

## <a name="additional-resources"></a>Ek kaynaklar

[Ticaret önizleme ortamına genel bakış](cpe-overview.md)

[Ticaret önizleme ortamı yapılandırma](cpe-post-provisioning.md)

[Bir Commerce Preview ortamı için isteğe bağlı özellikleri konfigüre edin](cpe-optional-features.md)

[Ticaret önizleme ortamı SSS](cpe-faq.md)

[Microsoft Lifecycle Services (LCS)](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide)

[Retail Cloud Scale Unit (RCSU)](https://docs.microsoft.com/business-applications-release-notes/october18/dynamics365-retail/retail-cloud-scale-unit)

[Microsoft Azure portalı](https://azure.microsoft.com/features/azure-portal)

[Dynamics 365 Commerce web sitesi](https://aka.ms/Dynamics365CommerceWebsite)

[Dynamics 365 Retail için yardım kaynakları](../retail/index.md)
