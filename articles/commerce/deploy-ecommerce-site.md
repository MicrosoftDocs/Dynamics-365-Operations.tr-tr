---
title: Yeni bir e-ticaret kiracısını dağıtma
description: Bu konu, Microsoft Dynamics Lifecycle Services (LCS) kullanarak yeni bir Dynamics 365 Commerce e-ticaret sitesi dağıtımının nasıl dağıtılacağını açıklamaktadır.
author: psimolin
ms.date: 07/02/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 6b228babfd32a4191eeed2a6d924a8b99f1a5311
ms.sourcegitcommit: 9eadc7ca08e2db3fd208f5fc835551abe9d06dc8
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/22/2021
ms.locfileid: "5936718"
---
# <a name="deploy-a-new-e-commerce-tenant"></a>Yeni bir e-ticaret kiracısını dağıtma

[!include [banner](includes/banner.md)]

Bu konu, Microsoft Dynamics Lifecycle Services (LCS) kullanarak yeni bir Dynamics 365 Commerce e-ticaret sitesi dağıtımının nasıl dağıtılacağını açıklamaktadır.

Microsoft Dynamics Lifecycle Services (LCS), iş ortaklarının ve müşterilerin projelerini ve ortamlarını yönetmek, Microsoft Dynamics ürünlerle ve özelliklerle ilgili en son bilgileri görüntülemek ve destek olayları oluşturmak, izlemek ve bunlara gözatmak için kullanılabilecek bulut tabanlı bir ortak çalışma alanıdır. E-ticaret yönetim özellikleri LCS ile tümleşiktir.

LCS hakkında daha fazla bilgi edinmek için, [Lifecycle Services Kullanıcı Kılavuzu](/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide)'na bakın.
    
## <a name="get-started"></a>Başlayın

E-ticaretin ilk önce başlatılması için bir proje, ortam ve bir Retail Cloud Scale Unit (rcsu) başlatmalısınız. LCS'de başlatma yapmak için, proje sahibi veya ortam yöneticisi rolü için izinleriniz olmalıdır. Üretim ve korumalı alan ortam topolojileri desteklenir.

Ortamlar hakkında daha fazla bilgi için [ortam planlama](/dynamics365/unified-operations/fin-and-ops/imp-lifecycle/environment-planning) konusuna bakın. RCSU hakkında daha fazla bilgi için, bkz. [Retail Cloud Scale Unit Başlat](/dynamics365/unified-operations/dev-itpro/deployment/initialize-retail-channels).

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

> [!NOTE]
> Bu bilgiler daha sonra bir servis isteği aracılığıyla eklenebilir.

Gerekli bilgileri topladıktan sonra, e-ticaret başlatmak için aşağıdaki adımları izleyin.

1. [LCS](https://lcs.dynamics.com)'de oturum açın
1. E-ticaret başlatmak istediğiniz ortamı içeren projeyi açın.
1. **Ortamlar** bölümünde, ortamı seçin.
1. **Ortam özellikleri** altında, **perakende Yönet** bağlantısını seçin.
1. **E-ticaret** sekmesinde, **kurulum**'u seçin. Sağlama için gerekli bilgileri girmeniz gereken bir iletişim kutusu görüntülenir.
1. Gerekli bilgileri doldurun ve sonraki sayfaya gidin.
1. Sonraki sayfada, gerekli bilgileri doldurun ve formu gönderin. Başlatmanın başlatıldığını görmek istediğiniz **e-ticaret** sekmesine iade ediyorsunuz.
1. Başlatma durumunu görüntülemek için ya **Yenile** ya da **e-ticaret** sekmesine daha sonra dönün.
    
E-ticaret LCS'den başlatıldığında, sistem e-ticaret için gerekli olan birçok bileşeni sağlar ve bunları ortamla ilişkilendirir. Sağlama tamamlandıktan sonra, **Perakende yönetim** sayfasındaki **e-ticaret** sekmesi sağlama işlemini yansıtacak şekilde güncelleştirilir. Sayfa en son özelleştirme dağıtımlarını ve devam eden diğer tüm dağıtımları gösterir. Ayrıca e-ticaret sitesi ve e-ticaret sitesi oluşturucu (sitelerin içeriğinin yazıldığı araç) bağlantıları da içerir.

## <a name="access-commerce-site-builder"></a>Commerce Site oluşturucuya erişim

Commerce site oluşturucuya erişmek için, LCS'de **Retail Management** sayfasındaki **e-ticaret** sekmesine gidin ve **E-ticaret sitesi yönetim aracı** bağlantısını seçin. Site oluşturucunun giriş sayfası, kiracı düzeyinde bir ekran görüntüler. Bu sayfadan şunları yapabilirsiniz:

- Kiracı düzeyinde ayarları değiştirin.
- Oluşturduğunuz ve görüntüleme iznine sahip olduğunuz bir siteye gidin. 
- Moderasyon ve raporlama gibi İncelemeler özelliklerine erişin.
- Yeni bir site oluşturun. Yeni site oluşturma hakkında daha fazla bilgi için bkz. [Yeni e-ticaret sitesi oluşturma](create-ecommerce-site.md). 

## <a name="additional-resources"></a>Ek kaynaklar

[Etki alanı adınızı yapılandırma](configure-your-domain-name.md)

[E-ticaret sitesi oluşturma](create-ecommerce-site.md)

[Dynamics 365 Commerce sitesini çevrimiçi bir kanalla ilişkilendirme](associate-site-online-store.md)

[robots.txt dosyalarını yönetme](manage-robots-txt-files.md)

[URL yeniden yönlendirmelerini toplu olarak yükleme](upload-bulk-redirects.md)

[Commerce'ta B2C kiracısı ayarlama](set-up-B2C-tenant.md)

[Kullanıcı oturum açma işlemleri için özel sayfalar ayarlama](custom-pages-user-logins.md)

[Commerce ortamında birden fazla B2C kiracısı yapılandırma](configure-multi-B2C-tenants.md)

[İçerik teslim ağı (CDN) için destek ekleme](add-cdn-support.md)

[Konum tabanlı mağaza algılamayı etkinleştirme](enable-store-detection.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]