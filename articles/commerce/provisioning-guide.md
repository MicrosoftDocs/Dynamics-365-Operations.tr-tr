---
title: Dynamics 365 Commerce önizleme ortamını hazırlama
description: Bu konu, hazırlandıktan sonra Microsoft Dynamics 365 Commerce önizleme ortamının nasıl yapılandırılacağını açıklamaktadır.
author: psimolin
manager: annbe
ms.date: 01/31/2020
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
ms.openlocfilehash: cbd4c118de2e91c8849461b20a01403049a07e66
ms.sourcegitcommit: 4ed1d8ad8a0206a4172dbb41cc43f7d95073059c
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/04/2020
ms.locfileid: "3024648"
---
# <a name="provision-a-dynamics-365-commerce-preview-environment"></a>Dynamics 365 Commerce önizleme ortamını hazırlama


[!include [banner](includes/banner.md)]

Bu konu, hazırlandıktan sonra Dynamics 365 Commerce önizleme ortamının nasıl yapılandırılacağını açıklamaktadır.

Başlamadan önce, işlemin gerek duyduğu bir fikir almak için bu konu hakkında hızlı bir tarama yapmanızı öneririz.

> [!NOTE]
> Dynamics 365 Commerce önizleme'ye erişim izni verilmemişse, [Dynamics 365 Commerce Web sitesinden](https://aka.ms/Dynamics365CommerceWebsite) önizleme erişimi isteyebilirsiniz.

## <a name="overview"></a>Genel Bakış

Commerce önizleme ortamınızı başarıyla sağlamak için, belirli bir ürün adı ve türü olan bir proje oluşturmanız gerekir. Ortam ve commerce scale unit (CSU), ayrıca, e-ticaret sağlamasının daha sonra başlatmak için kullanmanız gereken belirli parametreleri de vardır. Bu konudaki yönergeler, tamamlamanız gereken tüm gerekli adımları ve kullanmanız gereken parametreleri açıklar.

Sağlama başarılı olduktan sonra, Ticari önizleme ortamınızı hazırlamak için almanız gereken birkaç son işlem adımı vardır. Sistemin hangi yönlere göre değerlendirileceğini bağlı olarak bazı adımlar isteğe bağlıdır. İsteğe bağlı adımları istediğiniz zaman daha sonra da tamamlayabilirsiniz.

Commerce önizleme ortamını yapılandırma hakkında bilgi için bkz. [Commerce önizleme ortamı yapılandırma](cpe-post-provisioning.md). Commerce Preview ortamınızla ilgili isteğe bağlı özellikleri konfigüre etmek için, bkz. [Commerce önizleme ortamınız için isteğe bağlı özellikler yapılandırın](cpe-optional-features.md).

Sağlama adımlarıyla ilgili sorularınız varsa veya herhangi bir sorunla karşılaşırsanız, lütfen [Microsoft Dynamics 365 Commerce önizleme Yammer grubunda](https://aka.ms/Dynamics365CommercePreviewYammer) Microsoft'a bildirin.

## <a name="prerequisites"></a>Önkoşullar

Commerce önizleme ortamınızı hazırlayabilmeniz için aşağıdaki önkoşulların yerinde olması gerekir:

- Microsoft Dynamics Lifecycle Services (LCS) portalına erişim hakkınız var
- Varolan Microsoft Dynamics 365 ortağı veya müşterisiyseniz ve Dynamics 365 Commerce proje oluşturabilirsiniz.
- Dynamics 365 Commerce Önizleme programına kabul edilmiş olabilirsiniz.
- **Geçiş yapmak, çözüm oluşturmak ve daha fazla bilgi edinmek** için bir proje oluşturmaya gerekli izinleriniz vardır.
- Ortamı sağlamak istediğiniz **Ortam yöneticisi** veya **Proje sahibi** rolünün bir üyesisinizdir.
- Microsoft Azure aboneliğinize yönetici erişiminiz var veya sizin adınıza yönetici izinleri gerektiren iki adımı gerçekleştirebilecek bir abonelik Yöneticisi ile ilişki kurun.
- Azure Active Directory (Azure AD) kiracı kimliğiniz kullanılabilir.
- E-ticaret sistem yöneticileri grubu olarak kullanılacak bir Azure AD güvenlik grubu oluşturdunuz ve kimliğiniz kullanılabilir
- Derecelendirme ve incelemeler grubu olarak kullanılacak bir Azure AD güvenlik grubu oluşturdunuz ve kimliğiniz kullanılabilir (Bu güvenlik grubu e-ticaret Sistem Yöneticisi grubuyla aynı olabilir.)

## <a name="provision-your-commerce-preview-environment"></a>Commerce önizleme ortamınızı sağlama

Bu yöntemlerde, bir Commerce Preview ortamının nasıl sağlanacağı açıklamaktadır. Bunları başarıyla tamamladıktan sonra, Commerce Preview ortamı konfigürasyon için hazır olacak. Burada açıklanan tüm etkinlikler LCS portalında yer alabilir.

> [!IMPORTANT]
> Önizleme erişimi, Commerce önizleme uygulamanızda belirttiğiniz LCS hesabına ve kuruluşa bağlıdır. Commerce Preview ortamını sağlamak için aynı hesabı kullanmanız gerekir. Commerce Preview ortamı için farklı bir LCS hesabı veya kiracı kullanmanız gerekiyorsa, bu ayrıntıları Microsoft'a sağlamanız gerekir. Başvuru bilgileri için bu konudaki [Commerce önizleme ortam desteği](#commerce-preview-environment-support) başlıklı bölüme bakın.

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
> Tek bir seçeneği olan sayfalar atlandığından 6., 7. ve/veya 8. adımı tamamlamanız gerekmez. **Ortam parametreleri** görünümünde olduğunuzda, **ortam adı** alanının metin **Dynamics 365 Commerce-demo (*xx* platform güncelleştirmesi 10.0.* x)** ile doğrudan göründüğünü onaylayın. Ayrıntılar için, 8. adımdan sonra görünen çizime bakın.

1. Üst menüden **bulut ile barındırılan ortamları** seçin.
1. Ortam eklemek için **Ekle**'yi tıklatın.
1. **Uygulama sürümü** alanında, en güncel sürümü seçin. En güncel sürümden farklı bir uygulama sürümünü seçmeniz için özel bir gereksinim duyuyorsanız, **10.0.8** önceki bir sürümü seçmeyin.
1. **Platform sürümü** alanında, seçtiğiniz uygulama sürümü için otomatik olarak seçilen platform sürümünü kullanın. 

    ![Uygulamayı ve platform sürümünü seçme](./media/project1.png)

1. **Sonraki**'yi seçin.
1. Ortam topolojisi olarak **Demo**'yu seçinç

    ![Ortam topolojisini 1 seçme](./media/project2.png)

1. Ortam topolojisi olarak **Dynamics 365 Commerce - Demo**'yu seçinç Daha önce tek bir Azure Bağlayıcısı yapılandırdıysanız bu ortam için kullanılacak. Birden fazla Azure Bağlayıcısı konfigüre ediyorsanız, hangi bağlayıcının kullanılacağını seçebilirsiniz: **Doğu ABD**, **Doğu ABD 2**, **Batı ABD** veya **Batı ABD 2**. (En iyi uçtan uca performans için, **Batı ABD 2**'yi seçmeniz önerilir.)

    ![Ortam topolojisini 2 seçme](./media/project3.png)

1. **Ortam dağıt** sayfasında bir ortam adı girin. Gelişmiş ayarları olduğu gibi bırakın.

    ![Ortamı dağıtın sayfası](./media/project4.png)

1. VM boyutunu gerektiği gibi ayarlayın. (VM stok tutma birimi \[SKU\] **D13 v2**.)
1. Fiyat ve lisans koşullarını gözden geçirin ve kabul ettiğiniz onay kutusunu işaretleyin.
1. **Sonraki**'yi seçin.
1. Dağıtım onayı sayfasında, ayrıntıların doğru olduğunu doğruladıktan sonra **Dağıt**'ı seçin. **Bulut içinde barındırılan ortamlar** görünümüne geri dönersiniz ve ortamınız listede görünmelidir.

    İstediğiniz ortam kuyruğa alındı ve sonra dağıtılıyor. Ortam iş akışlarının tamamlanması biraz zaman alır. Bu nedenle, yaklaşık altı ile dokuz saatten sonra yeniden kontrol edin.

1. Devam etmeden önce, ortam durumlarınızın **dağıtıldığından** emin olun.

### <a name="initialize-the-commerce-scale-unit-csu"></a>Commerce scale unit (CSU) Başlat

Bir CSU başlatmak için şu adımları izleyin.

1. **Bulut barındırılan ortamlar** görünümünde, listeden ortamınızı seçin.
1. Sağdaki ortam görünümünde **tam ayrıntılar** 'ı tıklatın. Ortam ayrıntıları görünümü görüntülenir.
1. **Ortam özellikleri** altında, **Yönet**'i tıklatın.
1. **Commerce** sekmesinde, **Başlat**'ı seçin. CSU başlatma parametreleri görünümü görüntülenir.
1. **Bölge** alanında, **Doğu ABD**, **Doğu ABD 2**, **Batı ABD** veya **Batı ABD 2** seçeneklerinden birini belirleyin.
1. **Sürüm** alanında, listeden bir **sürüm belirtin** ve sonra görüntülenen alanda **9.18.20014.4** belirtin. Burada belirtilen sürümü tam olarak belirttiğinizden emin olun. Aksi durumda, RCSU öğesini daha sonra doğru sürüme güncelleştirmeniz gerekir.
1. **Uzantıyı Uygula** seçeneğini açın.
1. Uzantılar listesinden, **Commerce Önizleme demo temel uzantısını** seçin.
1. **Başlat**'ı seçin.
1. Dağıtım onayı sayfasında, ayrıntıların doğru olduğunu doğruladıktan sonra **Evet**'i seçin. **Ticaret yönetimi** görünümü, **Commerce** sekmesinin seçildiği yerde tekrar görüntülenir. CSU kaynak ayırma işlemi için sıraya alındı.
1. Devam etmeden önce, CSU durumlarınız **Başarılı** olur. Başlatma yaklaşık iki ile beş saat arasında sürer.

### <a name="initialize-e-commerce"></a>e-Ticaret başlat

Bir e-Ticaret başlatmak için şu adımları izleyin.

1. **E-ticaret** sekmesinde, önizleme onayını gözden geçirip **kurulum**'u seçin.
1. **E-ticaret kiracı adı** için bir ad girin. Ancak, e-ticaret örneğinizi gösteren bazı URL'lerde bu dosyanın görülebileceğini unutmayın.
1. **Commerce Scale Unit adı** alanında, listesindeki CSU alanını seçin. (Listede yalnızca bir seçenek bulunmalıdır.)

    **E-ticaret coğrafyası** alanı otomatik olarak ayarlanır ve değer değiştirilemez.

1. Devam etmek için **İleri**'yi seçin.
1. **Desteklenen ana bilgisayar adları** alanında, `www.fabrikam.com` gibi geçerli herhangi bir etki alanını girin.
1.  **Sistem Yöneticisi için AAD güvenlik grubunda** alanına, kullanmak istediğiniz güvenlik grubunun adının ilk birkaç harfini girin. Arama sonuçlarını görüntülemek için büyüteç simgesini seçin. Listeden doğru bir güvenlik grubunu seçin.
2.  **Derecelendirme ve inceleme moderatörü için AAD güvenlik grubunda** alanına, kullanmak istediğiniz güvenlik grubunun adının ilk birkaç harfini girin. Arama sonuçlarını görüntülemek için büyüteç simgesini seçin. Listeden doğru bir güvenlik grubunu seçin.
1. **Derecelendirmeleri etkinleştir ve gözden geçirme hizmeti** seçeneğini açık olarak bırakın.
1. **Başlat**'ı seçin. **Ticaret yönetimi** görünümü, **e-Commerce** sekmesinin seçildiği yerde tekrar görüntülenir. E-ticaret başlatma işlemi başlatıldı.
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

[Dynamics 365 Commerce önizleme ortamına genel bakış](cpe-overview.md)

[Dynamics 365 Commerce önizleme ortamını yapılandırma](cpe-post-provisioning.md)

[Dynamics 365 Commerce önizleme ortamı için isteğe bağlı özellikleri yapılandırma](cpe-optional-features.md)

[Dynamics 365 Commerce önizleme ortamıyla ilgili SSS](cpe-faq.md)

[Microsoft Lifecycle Services (LCS)](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide)

[Retail Cloud Scale Unit (RCSU)](https://docs.microsoft.com/business-applications-release-notes/october18/dynamics365-retail/retail-cloud-scale-unit)

[Microsoft Azure portalı](https://azure.microsoft.com/features/azure-portal)

[Dynamics 365 Commerce web sitesi](https://aka.ms/Dynamics365CommerceWebsite)

