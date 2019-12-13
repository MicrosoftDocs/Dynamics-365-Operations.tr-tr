---
title: Yeni bir e-Ticaret kiracısını dağıtma
description: Bu konu, Microsoft Dynamics Lifecycle Services (LCS) kullanarak yeni bir e-ticaret kiracısı dağıtımının nasıl dağıtılacağını açıklamaktadır.
author: psimolin
manager: annbe
ms.date: 10/31/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: c2632632b9b21dd3a88e9a4df0e65cfd28e579d2
ms.sourcegitcommit: 295d940a345879b3dfc5991e387b91c7257019ea
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/01/2019
ms.locfileid: "2697463"
---
# <a name="deploy-a-new-e-commerce-tenant"></a>Yeni bir e-Ticaret kiracısını dağıtma

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

Bu konu, Microsoft Dynamics Lifecycle Services (LCS) kullanarak yeni bir e-ticaret sitesi dağıtımının nasıl dağıtılacağını açıklamaktadır.

## <a name="overview"></a>Genel Bakış
    
Microsoft Dynamics Lifecycle Services (LCS), iş ortaklarının ve müşterilerin projelerini ve ortamlarını yönetmek, Microsoft Dynamics ürünlerle ve özelliklerle ilgili en son bilgileri görüntülemek ve destek olayları oluşturmak, izlemek ve bunlara gözatmak için kullanılabilecek bulut tabanlı bir ortak çalışma alanıdır. E-ticaret yönetim özellikleri LCS ile tümleşiktir.

LCS hakkında daha fazla bilgi edinmek için, [Lifecycle Services Kullanıcı Kılavuzu](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide)'na bakın.
    
## <a name="get-started"></a>Başlayın

E-ticaretin ilk önce başlatılması için bir proje, ortam ve bir Retail Cloud Scale Unit (rcsu) başlatmalısınız. LCS'de başlatma yapmak için, proje sahibi veya ortam yöneticisi rolü için izinleriniz olmalıdır. Üretim ve korumalı alan ortam topolojileri desteklenir.

Ortamlar hakkında daha fazla bilgi için [ortam planlama](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/imp-lifecycle/environment-planning) konusuna bakın. RCSU hakkında daha fazla bilgi için, bkz. [Retail Cloud Scale Unit Başlat](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/deployment/initialize-retail-channels).

## <a name="initialize-e-commerce"></a>e-Ticaret başlat

Varolan bir ortamdaki e-ticaret özelliğini başlatmak için bu yordamı kullanın.

Başlamadan önce, aşağıdaki gerekli bilgilere sahip olduğunuzdan emin olun:

- Kullanılacak RCSU.
- E-ticaret sistem yöneticileri Için kullanılacak Microsoft Azure Active Directory güvenlik grubu.
- Derecelendirme v inceleme moderatörleri için kullanılacak Microsoft Azure Active Directory güvenlik grubu.
- Ortam ile ilişkilendirilecek etki alanları.

Ek olarak, aşağıdaki isteğe bağlı bilgileri toplayabilirsiniz:

- Azure AD işletme-müşteri arası (B2C) bilgiler:

    - Kiracı adı.
    - İstemci kodu.
    - Özel Etki Alanında Oturum Aç.
    - URL yanıtı.
    - Kaydolma Oturum Açma İlkesi Kodu.
    - Parola sıfırlama ilkesi kodu.
    - Profil İlkesi Kodunu Düzenle.

[!NOTE]
Bu bilgiler daha sonra bir servis isteği aracılığıyla eklenebilir.

Gerekli bilgileri topladıktan sonra, e-ticaret başlatmak için aşağıdaki adımları izleyin.

1. [LCS](https://lcs.dynamics.com)'de oturum açın
1. E-ticaret başlatmak istediğiniz ortamı içeren projeyi açın.
1. **Ortamlar** bölümünde, ortamı seçin.
1. **Ortam özellikleri**altında, **perakende Yönet** bağlantısını seçin.
1. **E-ticaret** sekmesinde, **kurulum**'u seçin. Sağlama için gerekli bilgileri girmeniz gereken bir iletişim kutusu görüntülenir.
1. Gerekli bilgileri doldurun ve sonraki sayfaya gidin.
1. Sonraki sayfada, gerekli bilgileri doldurun ve formu gönderin. Başlatmanın başlatıldığını görmek istediğiniz **e-ticaret** sekmesine iade ediyorsunuz.
1. Başlatma durumunu görüntülemek için ya **Yenile** ya da **e-ticaret** sekmesine daha sonra dönün.
    
E-ticaret LCS'den başlatıldığında, sistem e-ticaret için gerekli olan birçok bileşeni sağlar ve bunları ortamla ilişkilendirir. Sağlama tamamlandıktan sonra, **Perakende yönetim** sayfasındaki **e-ticaret** sekmesi sağlama işlemini yansıtacak şekilde güncelleştirilir. Sayfa en son özelleştirme dağıtımlarını ve devam eden diğer tüm dağıtımları gösterir. Ayrıca e-ticaret sitesi ve e-ticaret sitesi yönetim aracı (geliştirme aracı) bağlantıları da içerir.

## <a name="access-the-authoring-environment"></a>Yazma ortamına erişim

Geliştirme ortamına erişmek için, **Perakende yönetimi** sayfasındaki **e-ticaret** sekmesine gidin. Burada e-ticaret sitenize ve site yönetim aracına bağlantılar bulacaksınız.

## <a name="additional-resources"></a>Ek kaynaklar

[Çevrimiçi mağazaya genel bakış](online-store-overview.md)

[e-Ticaret sitesi oluşturma](create-ecommerce-site.md)

[Çevrimiçi siteyi bir kanalla ilişkilendirme](associate-site-online-store.md)

[Etki alanı adınızı yapılandırma](configure-your-domain-name.md)

[İçerik teslim ağı (CDN) için destek ekleme](add-cdn-support.md)

[Konum tabanlı mağaza algılamayı etkinleştirme](enable-store-detection.md)

[Kullanıcı oturum açma işlemleri için özel sayfalar ayarlama](custom-pages-user-logins.md)
