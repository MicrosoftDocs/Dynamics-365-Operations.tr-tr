---
title: Dynamics 365 Commerce değerlendirme ortamı sağlama
description: Bu konu, Microsoft Dynamics 365 Commerce değerlendirme ortamının nasıl sağlanacağını açıklamaktadır.
author: psimolin
manager: annbe
ms.date: 11/05/2020
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
ms.openlocfilehash: b54216a565c264dfcfe821581fee9df7b5e22323
ms.sourcegitcommit: 715508547f9a71a89a138190e8540686556c753d
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/05/2020
ms.locfileid: "4416581"
---
# <a name="provision-a-dynamics-365-commerce-evaluation-environment"></a>Dynamics 365 Commerce değerlendirme ortamı sağlama

[!include [banner](includes/banner.md)]

Bu konu, Microsoft Dynamics 365 Commerce değerlendirme ortamının nasıl sağlanacağını açıklamaktadır.

Başlamadan önce, işlemin gerek duyduğu bir fikir almak için bu konu hakkında hızlı bir tarama yapmanızı öneririz.

> [!NOTE]
> Commerce değerlendirme ortamları genel olarak kullanıma sunulmamıştır ve iş ortakları ile müşterilere istek üzerine sunulmaktadır. Daha fazla bilgi için Microsoft iş ortağı ilgili kişisine ulaşın.

## <a name="overview"></a>Özet

Commerce değerlendirme ortamını başarıyla sağlamak için, belirli bir ürün adı ve türü olan bir proje oluşturmanız gerekir. Ortam ve Commerce Scale Unit'te (CSU), ayrıca, e-Ticaret'i daha sonra sağlamayı düşündüğünüzde kullanmanız gereken belirli parametreler de vardır. Bu konudaki yönergeler, tamamlamanız gereken tüm gerekli adımları ve kullanmanız gereken parametreleri açıklar.

Sağlama başarılı olduktan sonra, Commerce değerlendirme ortamınızı kullanmak üzere hazırlamak için almanız gereken birkaç son işlem adımı vardır. Sistemin hangi yönlere göre değerlendirileceğini bağlı olarak bazı adımlar isteğe bağlıdır. İsteğe bağlı adımları istediğiniz zaman daha sonra da tamamlayabilirsiniz.

Commerce değerlendirme ortamını yapılandırma hakkında bilgi için bkz. [Commerce değerlendirme ortamı yapılandırma](cpe-post-provisioning.md). Commerce değerlendirme ortamınızla ilgili isteğe bağlı özellikleri yapılandırmak için, bkz. [Commerce değerlendirme ortamınız için isteğe bağlı özellikler yapılandırma](cpe-optional-features.md).

## <a name="prerequisites"></a>Önkoşullar

Commerce değerlendirme ortamınızı hazırlayabilmeniz için aşağıdaki önkoşulların yerinde olması gerekir:

- Değerlendirme programına katıldınız ve bir değerlendirme ortamı için kapasite verildi.
- Microsoft Dynamics Lifecycle Services (LCS) portalına erişim hakkınız var
- Varolan Microsoft Dynamics 365 ortağı veya müşterisiyseniz ve Dynamics 365 Commerce proje oluşturabilirsiniz.
- Microsoft Azure aboneliğinize yönetici erişiminiz var veya gerektiğinde size yardımcı olabilecek bir abonelik Yöneticisi ile temas kuruyorsunuz.
- Azure Active Directory (Azure AD) kiracı kimliğiniz kullanılabilir.
- E-ticaret sistem yöneticileri grubu olarak kullanılacak bir Azure AD güvenlik grubu oluşturdunuz ve kimliğiniz kullanılabilir
- Derecelendirme ve incelemeler grubu olarak kullanılacak bir Azure AD güvenlik grubu oluşturdunuz ve kimliğiniz kullanılabilir (Bu güvenlik grubu e-ticaret Sistem Yöneticisi grubuyla aynı olabilir.)

Bu listenin kapsamlı olmadığını unutmayın. Herhangi bir sorunla karşılaşırsanız, yardım için Microsoft iş ortağınıza başvurun.

## <a name="provision-your-commerce-evaluation-environment"></a>Commerce değerlendirme ortamınızı sağlama

Bu yöntemlerde, bir Commerce değerlendirme ortamının nasıl sağlanacağı açıklamaktadır. Bunları başarıyla tamamladıktan sonra, Commerce değerlendirme ortamı yapılandırma için hazır olacak. Burada açıklanan tüm etkinlikler LCS portalında yer alabilir.

### <a name="create-a-new-project"></a>Yeni proje oluştur

LCS'de bir yeni proje oluşturmak için şu adımları izleyin.

1. LCS giriş sayfasında, bir proje oluşturmak için artı işaretini (**+**) seçin.
1. Sağ bölmede aşağıdaki adımlardan birini izleyin:

    - Bir ortaksanız **taşı, çözüm oluştur ve öğren**'yi seçin.
    - Müşterisiyseniz, **olası ön satışlar**'ı seçin.

1. Şablon adı, açıklama ve sektör girin.
1. **Ürün adı** alanından **Dynamics 365 Commerce** seçin.
1. **Ürün sürümü** alanından **Dynamics 365 Commerce** seçin.
1. **Metodoloji** alanında **Dynamics Retail uygulama metodoloji**'ı seçin.
1. İsteğe bağlı: Roller ve kullanıcılar mevcut projeden içeri aktarabilirsiniz.
1. **Oluştur**'u seçin. Proje görünümü gösterilir.

### <a name="add-the-azure-connector"></a>Azure bağlayıcısı ekle

LCS projenize Azure Bağlayıcısı eklemek için, [Azure Resource Manager (ARM) ekleme işlemini tamamlama](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/arm-onboarding) bölümündeki adımları izleyin.

### <a name="deploy-the-environment"></a>Ortamı dağıtın

Ortamı dağıtmak için şu adımları izleyin.

> [!NOTE]
> Tek bir seçeneği olan sayfalar atlandığından 6., 7. ve/veya 8. adımı tamamlamanız gerekmez. **Ortam parametreleri** görünümünde olduğunuzda, **ortam adı** alanının metin **Dynamics 365 Commerce-demo (*xx* platform güncelleştirmesi 10.0.* x)** ile doğrudan göründüğünü onaylayın. Ayrıntılar için, 8. adımdan sonra görünen çizime bakın.

1. Üst menüden **bulut ile barındırılan ortamları** seçin.
1. Ortam eklemek için **Ekle**'yi tıklatın.
1. **Uygulama sürümü** alanında, en güncel sürümü seçin. En güncel sürümden farklı bir uygulama sürümünü seçmeniz için özel bir gereksinim duyuyorsanız, **10.0.14** önceki bir sürümü seçmeyin.
1. **Platform sürümü** alanında, seçtiğiniz uygulama sürümü için otomatik olarak seçilen platform sürümünü kullanın. 

    ![Uygulamayı ve platform sürümünü seçme](./media/project1.png)

1. **Sonraki**'yi seçin.
1. Ortam topolojisi olarak **Demo**'yu seçinç

    ![Ortam topolojisini 1 seçme](./media/project2.png)

1. **Ortam dağıt** sayfasında bir ortam adı girin. Gelişmiş ayarları olduğu gibi bırakın.

    ![Ortamı dağıtın sayfası](./media/project4.png)

1. VM boyutunu gerektiği gibi ayarlayın. (VM stok tutma birimi \[SKU\] **D13 v2**.)
1. Fiyat ve lisans koşullarını gözden geçirin ve kabul ettiğiniz onay kutusunu işaretleyin.
1. **Sonraki**'yi seçin.
1. Dağıtım onayı sayfasında, ayrıntıların doğru olduğunu doğruladıktan sonra **Dağıt**'ı seçin. **Bulut içinde barındırılan ortamlar** görünümüne geri dönersiniz ve ortamınız listede görünmelidir.

    İstediğiniz ortam kuyruğa alındı ve sonra dağıtılıyor. Ortam iş akışlarının tamamlanması biraz zaman alır. Bu nedenle, yaklaşık altı ile dokuz saatten sonra yeniden kontrol edin.

1. Devam etmeden önce, ortam durumlarınızın **dağıtıldığından** emin olun.

### <a name="initialize-the-commerce-scale-unit-cloud"></a>Commerce scale unit (bulut) Başlat

Bir CSU başlatmak için şu adımları izleyin.

1. **Bulut barındırılan ortamlar** görünümünde, listeden ortamınızı seçin.
1. Sağdaki ortam görünümünde **tam ayrıntılar** 'ı tıklatın. Ortam ayrıntıları görünümü görüntülenir.
1. **Ortam özellikleri** altında, **Yönet**'i tıklatın.
1. **Commerce** sekmesinde, **Başlat**'ı seçin. CSU başlatma parametreleri görünümü görüntülenir.
1. **Bölge** alanında, ortamı dağıttığınız bölgeyle aynı veya buna yakın bir bölgeyi seçin.
1. **Sürüm** alanını olduğu gibi bırakın.
1. **Başlat**'ı seçin.
1. Dağıtım onayı sayfasında, ayrıntıların doğru olduğunu doğruladıktan sonra **Evet**'i seçin. **Ticaret yönetimi** görünümü, **Commerce** sekmesinin seçildiği yerde tekrar görüntülenir. CSU kaynak ayırma işlemi için sıraya alındı.
1. Devam etmeden önce, CSU durumlarınız **Başarılı** olur. Başlatma yaklaşık iki ile beş saat arasında sürer.

Ortam ayrıntıları görünümünde **Yönet** bağlantısını bulamazsanız, yardım için Microsoft ilgili kişinize başvurun.

### <a name="initialize-e-commerce"></a>e-Ticaret başlat

Bir e-Ticaret başlatmak için şu adımları izleyin.

1. **E-ticaret** sekmesinde, değerlendirme onayını gözden geçirip **Kurulum**'u seçin.
1. **E-ticaret ortamı adı** için bir ad girin. e-Ticaret kurulumunuzu gösteren bazı URL'lerde bu dosyanın görülebileceğini unutmayın.
1. **Commerce Scale Unit adı** alanında, listesindeki CSU alanını seçin. (Listede yalnızca bir seçenek bulunmalıdır.)

    **E-ticaret coğrafi bölgesi** alanı otomatik olarak ayarlanır.

1. Devam etmek için **İleri**'yi seçin.
1. **Desteklenen ana bilgisayar adları** alanında, `www.fabrikam.com` gibi geçerli herhangi bir etki alanını girin.
1. **Sistem yöneticisi için AAD güvenlik grubu** alanına, kullanmak istediğiniz güvenlik grubunun adının ilk birkaç harfini girin ve sonra arama sonuçlarını görmek için büyüteç simgesini seçin. Listede doğru güvenlik grubunu seçin.
1.  **Derecelendirmeler ve inceleme moderatörü için AAD güvenlik grubu** alanına, kullanmak istediğiniz güvenlik grubunun adının ilk birkaç harfini girin ve sonra arama sonuçlarını görmek için büyüteç simgesini seçin. Listede doğru güvenlik grubunu seçin.
1. **Derecelendirmeler ve gözden geçirme hizmetini etkinleştir** seçeneğini **Evet**'e ayarlanmış olarak bırakın.
1. **Başlat**'ı seçin. **Ticaret yönetimi** görünümü, **e-Commerce** sekmesinin seçildiği yerde tekrar görüntülenir. E-ticaret başlatma işlemi başlatıldı.
1. Devam etmeden önce, e-ticaret başlatma durumunuz **başlatma başarılı** olana kadar bekleyin.
1. Alt sağdaki **bağlantılar** altında, aşağıdaki bağlantıların URL 'lerini not alın:

    * **e-ticaret sitesi** – E-ticaret sitenizin köküne olan bağlantı.
    * **Commerce site oluşturucu** – Site yönetimi aracına bağlantı.

## <a name="next-steps"></a>Sonraki adımlar

Commerce değerlendirme ortamını sağlama ve yapılandırma işlemine devam etmek için bkz. [Commerce değerlendirme ortamı yapılandırma](cpe-post-provisioning.md).

## <a name="additional-resources"></a>Ek kaynaklar

[Dynamics 365 Commerce değerlendirme ortamına genel bakış](cpe-overview.md)

[Dynamics 365 Commerce değerlendirme ortamı yapılandırma](cpe-post-provisioning.md)

[Dynamics 365 Commerce değerlendirme ortamında BOPIS yapılandırma](cpe-bopis.md)

[Dynamics 365 Commerce değerlendirme ortamı için isteğe bağlı özellikleri yapılandırma](cpe-optional-features.md)

[Dynamics 365 Commerce değerlendirme ortamıyla ilgili SSS](cpe-faq.md)

[Microsoft Lifecycle Services (LCS)](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide)

[Commerce Scale Unit (bulut)](https://docs.microsoft.com/business-applications-release-notes/october18/dynamics365-retail/retail-cloud-scale-unit)

[Microsoft Azure portalı](https://azure.microsoft.com/features/azure-portal)

[Dynamics 365 Commerce web sitesi](https://aka.ms/Dynamics365CommerceWebsite)


[!INCLUDE[footer-include](../includes/footer-banner.md)]