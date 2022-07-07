---
title: Dynamics 365 Commerce korumalı alan ortamını hazırlama
description: Bu makalede, demo veya korumalı alan kullanımı için yerleşik demo verileriyle bir Microsoft Dynamics 365 Commerce korumalı alan ortamının nasıl sağlanacağı açıklanmaktadır.
author: psimolin
ms.date: 06/14/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: 3ada30fc9d86d236b71d018ef77f2ae8573f2285
ms.sourcegitcommit: 252cb41c3029b623354698463f7b44a29fd9f184
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/15/2022
ms.locfileid: "9013148"
---
# <a name="provision-a-dynamics-365-commerce-sandbox-environment"></a>Dynamics 365 Commerce korumalı alan ortamını hazırlama

[!include [banner](includes/banner.md)]

Bu makalede, demo kullanımı için yerleşik demo verileriyle bir Microsoft Dynamics 365 Commerce korumalı alan ortamının nasıl sağlanacağı açıklanmaktadır. Daha çok sayıda korumalı alan ortamının önkoşulları demo verilerinde zaten sağlanmış olduğundan, bir üretim ortamını ayarlama işlemi benzer ancak daha ayrıntılı bir işlemdir.

Başlamadan önce, işlemin gerek duyduğu bir fikir almak için bu makale hakkında hızlı bir tarama yapmanızı öneririz.

Bir Commerce korumalı alan ortamını başarıyla sağlamak için, daha sonra Commerce'ü sağladığınızda kullanılacak ortam ve Commerce Scale Unit (CSU) için bazı parametreler belirtmeniz gerekir. Bu makaledeki yönergeler, tamamlamanız gereken tüm gerekli adımları ve kullanmanız gereken parametreleri açıklar.

Sağlama başarılı olduktan sonra, Commerce ortamınızı kullanmak üzere hazırlamak için tamamlamanız gereken birkaç sağlama sonrası adım vardır. Sistemin hangi yönlerini kullanmak istediğinize bağlı olarak bazı adımlar isteğe bağlıdır. İsteğe bağlı adımları istediğiniz zaman daha sonra da tamamlayabilirsiniz.

Commerce ortamını yapılandırma hakkında bilgi için bkz. [Commerce korumalı alan ortamı yapılandırma](cpe-post-provisioning.md). Commerce ortamınızla ilgili isteğe bağlı özellikleri yapılandırmak için bkz. [Commerce korumalı alan ortamınız için isteğe bağlı özellikler yapılandırın](cpe-optional-features.md).

## <a name="prerequisites"></a>Ön Koşullar

Commerce ortamınızı hazırlayabilmeniz için aşağıdaki önkoşulların sağlanması gerekir:

- Microsoft Dynamics Lifecycle Services (LCS) portalına erişim hakkınız var
- Varolan bir Microsoft Dynamics 365 iş ortağı veya müşterisisiniz ve önceden oluşturulmuş ve LCS'de kullanılabilir bir uygulama projesine sahipsiniz.  
- Commerce sistem yöneticisi grubu olarak kullanılacak bir Azure Active Directory (Azure AD) güvenlik grubu oluşturdunuz ve grubun kimliğine sahipsiniz.
- Derecelendirme ve inceleme moderatörü grubu olarak kullanılacak bir Azure AD güvenlik grubu oluşturdunuz ve grubun kimliğine sahipsiniz. (Bu güvenlik grubu Commerce sistem yöneticisi grubuyla aynı olabilir.)
- LCS içinde bir Headquarters örneği dağıttınız. Daha fazla bilgi için bkz. [Yeni ortam dağıtma](/dynamics365/fin-ops-core/dev-itpro/deployment/deployenvironment-newinfrastructure).

Bu listenin kapsamlı olmadığını unutmayın. Herhangi bir sorunla karşılaşırsanız, yardım için Microsoft iş ortağınıza başvurun.

## <a name="provision-your-commerce-environment"></a>Commerce ortamınızı sağlama

Aşağıdaki yordamlarda bir Commerce ortamının nasıl sağlanacağı açıklamaktadır. Adımları başarıyla tamamladıktan sonra, Commerce ortamınız yapılandırma için hazır olacak. Aşağıda açıklanan tüm adımlar LCS portalında yer alır.

### <a name="initialize-the-commerce-scale-unit-cloud"></a>Commerce scale unit (bulut) Başlat

CSU'yu başlatmak için bu adımları izleyin.

1. LCS'de, listeden ortamınızı seçin.
1. Sağdaki **ORTAMLAR** görünümünde **Tam ayrıntılar**'ı seçin. Ortam ayrıntıları görünümü görüntülenir.
1. **ORTAM ÖZELLİKLERİ** altındaki **Ortamı yönet** bölümünde **Yönet**'i seçin.
1. **Commerce Scale Units** sekmesinde, **Başlat**'ı seçin. **Ölçek birimi ekle** görünümü görüntülenir.
1. **BÖLGE** alanında, ortamı dağıttığınız bölgeyle aynı veya buna yakın bir bölgeyi seçin.
1. **Sürüm** açılan listesinde, kullanılabilir en son sürümü seçin.
1. **Başlat**'ı seçin.
1. Commerce Scale Unit başlatma işlemini onaylamanızı isteyen uyarı iletişim kutusunda **Evet**'i seçin. CSU, hazırlama işlemi için artık sıraya alınmıştır.
1. Devam etmeden önce, CSU'nuzun durumunun **BAŞARILI** olduğundan emin olun. Başlatma yaklaşık iki ile beş saat arasında sürer.

Ortam ayrıntıları görünümünde **Yönet** bağlantısını bulamazsanız, yardım için Microsoft ilgili kişinize başvurun.

### <a name="initialize-e-commerce"></a>e-Ticaret başlat

Commerce'ü başlatmak için şu adımları izleyin.

1. **E-ticaret** sekmesinde, **kurulum**'u seçin.
1. **E-ticaret ortamı adı** için bir ad girin. e-Ticaret kurulumunuzu gösteren bazı URL'lerde bu dosyanın görülebileceğini unutmayın.
1. **Commerce Scale Unit adı** alanında, listesindeki CSU alanını seçin. (Listede yalnızca bir seçenek bulunmalıdır.)

    **E-ticaret coğrafi bölgesi** alanı otomatik olarak ayarlanır.

1. Devam etmek için **İleri**'yi seçin.
1. **Desteklenen ana bilgisayar adları** alanında, `www.fabrikam.com` gibi geçerli herhangi bir etki alanını girin.
1. **Sistem yöneticisi için AAD güvenlik grubu** alanına, kullanmak istediğiniz güvenlik grubunun adının ilk birkaç harfini girin ve sonra arama sonuçlarını görmek için büyüteç simgesini seçin. Listede doğru güvenlik grubunu seçin.
1.  **Derecelendirmeler ve inceleme moderatörü için AAD güvenlik grubu** alanına, kullanmak istediğiniz güvenlik grubunun adının ilk birkaç harfini girin ve sonra arama sonuçlarını görmek için büyüteç simgesini seçin. Listede doğru güvenlik grubunu seçin.
1. **Derecelendirmeler ve gözden geçirme hizmetini etkinleştir** seçeneğini **Evet**'e ayarlanmış olarak bırakın.
1. **Başlat**'ı seçin. **Ticaret yönetimi** görünümü, **e-Commerce** sekmesinin seçildiği yerde tekrar görüntülenir. E-ticaret başlatma işlemi başlatıldı.
1. Devam etmeden önce, Commerce başlatma durumunuz **BAŞLATMA BAŞARILI** olana kadar bekleyin.
1. Alt sağdaki **bağlantılar** altında, aşağıdaki bağlantıların URL 'lerini not alın:

    * **e-ticaret sitesi** – E-ticaret sitenizin köküne olan bağlantı.
    * **Commerce site oluşturucu** – Site yönetimi aracına bağlantı.

## <a name="next-steps"></a>Sonraki adımlar

Commerce ortamını hazırlama ve yapılandırma işlemine devam etmek için bkz. [Commerce korumalı alan ortamı yapılandırma](cpe-post-provisioning.md).

## <a name="additional-resources"></a>Ek kaynaklar

[Dynamics 365 Commerce korumalı alan ortamı yapılandırma](cpe-post-provisioning.md)

[Dynamics 365 Commerce korumalı alan ortamında BOPIS'i yapılandırma](cpe-bopis.md)

[Dynamics 365 Commerce korumalı alan ortamı için isteğe bağlı özellikleri yapılandırma](cpe-optional-features.md)

[Microsoft Lifecycle Services (LCS)](/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide)

[Commerce Scale Unit (bulut)](/business-applications-release-notes/october18/dynamics365-retail/retail-cloud-scale-unit)

[Microsoft Azure portalı](https://azure.microsoft.com/features/azure-portal)

[Dynamics 365 Commerce web sitesi](https://aka.ms/Dynamics365CommerceWebsite)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
