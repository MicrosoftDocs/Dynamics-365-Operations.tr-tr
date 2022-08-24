---
title: Derecelendirmeleri ve değerlendirmeleri içe ve dışa aktarma
description: Bu makale, Microsoft Dynamics 365 Commerce'de ürün derecelendirmelerinin ve incelerinin nasıl alınacağını ve verileceğini açıklar.
author: gvrmohanreddy
ms.date: 01/12/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2017-06-20
ms.openlocfilehash: f369e3cd208cdfba816f817ead75374ee6982912
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/12/2022
ms.locfileid: "9271948"
---
# <a name="import-and-export-ratings-and-reviews"></a>Derecelendirmeleri ve değerlendirmeleri içe ve dışa aktarma

[!include [banner](includes/banner.md)]

Bu makale, Microsoft Dynamics 365 Commerce'de ürün derecelendirmelerinin ve incelerinin nasıl alınacağını ve verileceğini açıklar.

Dynamics 365 Commerce, çok kanallı çözüm olarak [derecelendirmeler ve incelemeler](ratings-reviews-overview.md) sunar. Dynamics 365 Commerce derecelendirmeler ve incelemeler çözümüne geçtiğinizde, varolan derecelendirme ve inceleme verilerini Commerce platformuna taşımak isteyebilirsiniz. İş gereksinimlerinize göre, Commerce'den derecelendirme ve inceleme verilerini dışa aktarmak da isteyebilirsiniz. Power Automate bağlayıcısı, derecelendirmeleri ve incelemeleri Commerce'e ve Commerce'den aktarmanıza olanak tanır.

> [!NOTE]
> Power Automate'teki mantık akışlarını kullanmaya başlama hakkında bilgi edinmek için bkz. [Power Automate'te bulut akışı oluşturma](/power-automate/get-started-logic-flow).

## <a name="prerequisites"></a>Önkoşullar

Derecelendirmeleri ve incelemeleri içe ve dışa aktarmadan önce aşağıdaki ön koşulları yerine getirmelisiniz:

- Derecelendirmeler ve inceleme çözümünün Commerce platformunda e-Ticaret siteniz için etkinleştirilmiş olması gerekir. Daha fazla bilgi için bkz. [Derecelendirme ve incelemeleri kullanmak için etkinleştirme](opt-in-ratings-reviews.md).
- Dynamics 365 Derecelendirmeler ve İncelemeler Power App Bağlayıcısının, Power Automate'te "incelemeleri gönder" veya "incelemeleri dışa aktar" eylemlerini etkinleştirecek şekilde yapılandırılmış olması gerekir. Daha fazla bilgi için bkz. [Dynamics 365 Commerce - Derecelendirmeler ve İncelemeler (Önizleme)](/connectors/dynamics365ratingsre/).
- Hizmetten Hizmete (S2S) kimlik doğrulamasının, derecelendirme ve incelemeler uygulama programlama arabirimini (API) Commerce dışından güvenli bir şekilde çağıracak şekilde yapılandırılmış olması gerekir. Daha fazla bilgi için bkz. [Hizmetten Hizmete kimlik doğrulamasını yapılandırma](service-to-service-auth.md).

## <a name="import-ratings-and-reviews"></a>Derecelendirme ve incelemeleri içe aktarma

Mevcut sisteminizden derecelendirme ve inceleme verilerini Commerce'e aktarmak için Dynamics 365 Derecelendirmeler ve İnceleme Power Automate bağlayıcısını, mevcut veya yeni bir Power Automate akışına eklemeniz gerekir. Daha fazla bilgi için bkz. [Dynamics 365 Commerce - Derecelendirmeler ve İncelemeler (Önizleme)](/connectors/dynamics365ratingsre/).

> [!IMPORTANT]
> Bu prosedürü tamamlamadan önce de [S2S kimlik doğrulama yapılandırmasını](service-to-service-auth.md) yapmanız gerekir.

Dynamics 365 Derecelendirmeler ve İncelemeler Power Automate bağlayıcısını kullanarak derecelendirme ve incelemeleri Commerce'e aktarmak için aşağıdaki adımları izleyin.

1. **Kullanıcı İncelemesi Gönder** eylemini seçin.
1. S2S kimlik doğrulamasını yapılandırdığınızda oluşturulan Azure Active Directory (Azure AD) uygulamasını kullanarak bir bağlantı kurun. Daha fazla bilgi için bkz. [Hizmetten hizmete kimlik doğrulamasını yapılandırma](service-to-service-auth.md).
1. **Kullanıcı İncelemesi Gönder** eylemi, bir seferde bir inceleme alır. Bu nedenle eylemi yineleyin. İncelemeleri toplu olarak göndermek için kaynak incelemelerini liste olarak kullanın.
    
## <a name="export-ratings-and-reviews"></a>Derecelendirme ve incelemeleri dışa aktarma

Derecelendirme ve inceleme verilerini Commerce'den aktarmak için Dynamics 365 Derecelendirmeler ve İnceleme Power Automate bağlayıcısını, mevcut veya yeni bir Power Automate akışına eklemeniz gerekir. Daha fazla bilgi için bkz. [Dynamics 365 Commerce - Derecelendirmeler ve İncelemeler (Önizleme)](/connectors/dynamics365ratingsre/).

Dynamics 365 Derecelendirmeler ve İncelemeler Power Automate bağlayıcısını kullanarak derecelendirme ve incelemeleri Commerce'den aktarmak için aşağıdaki adımları izleyin.

1. **Tüm İncelemeleri Dışa Aktar** eylemini seçin.
1. Eylemi tamamlayın. 

## <a name="additional-resources"></a>Ek kaynaklar

[Derecelendirmelere ve incelemelere genel bakış](ratings-reviews-overview.md)

[Derecelendirme ve incelemeleri kullanmayı kabul etme](opt-in-ratings-reviews.md)

[Derecelendirme ve incelemeleri yönetme](manage-reviews.md)

[Derecelendirme ve incelemeleri yapılandırma](configure-ratings-reviews.md)

[Ürün derecelendirmelerini eşitleme](sync-product-ratings.md)

[Derecelendirmelerin ve incelemelerin moderatör tarafından el ile yayımlanmasını etkinleştirme](manual-publish-rating-reviews.md)

[Hizmetten hizmete kimlik doğrulamasını yapılandırma](service-to-service-auth.md)

[Derecelendirmeler ve incelemelerle ilgili SSS](ratings-reviews-faq.md)
