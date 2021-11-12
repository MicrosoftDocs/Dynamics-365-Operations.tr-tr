---
title: Derecelendirmelerin ve incelemelerin moderatör tarafından el ile yayımlanmasını etkinleştirme
description: Bu konuda, derecelendirmelerin ve incelemelerin Microsoft Dynamics 365 Commerce uygulamasında moderatör tarafından el ile yayımlanmasının nasıl etkinleştirileceği ve derecelendirmelerin ve incelemelerin el ile nasıl yayımlanacağı açıklanmaktadır.
author: gvrmohanreddy
manager: annbe
ms.date: 09/03/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2021-09-03
ms.dyn365.ops.version: 10.0.22
ms.openlocfilehash: 25ae7074fcf39bf4408ea1fa0acfc334281bb254
ms.sourcegitcommit: 1707cf45217db6801df260ff60f4648bd9a4bb68
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/23/2021
ms.locfileid: "7675061"
---
# <a name="enable-manual-publishing-of-ratings-and-reviews-by-a-moderator"></a>Derecelendirmelerin ve incelemelerin moderatör tarafından el ile yayımlanmasını etkinleştirme

[!include [banner](includes/banner.md)]

Bu konuda, derecelendirmelerin ve incelemelerin Microsoft Dynamics 365 Commerce uygulamasında moderatör tarafından el ile yayımlanmasının nasıl etkinleştirileceği ve derecelendirmelerin ve incelemelerin el ile nasıl yayımlanacağı açıklanmaktadır.

Dynamics 365 Commerce uygulamasının derecelendirmeler ve incelemeler çözümü, inceleme başlıklarında ve içeriğinde yer alan kötü sözcükleri otomatik olarak düzenlemek ve derecelendirmeleri ve incelemeleri yayımlamak için Azure Cognitive Services'i kullanır. Bu nedenle, e-ticaret sitenizde derecelendirmeleri ve incelemeleri gözden geçirmek ve yayımlamak için el ile müdahale gerekmez.

Ancak bazı işletmeler, moderatörlerin incelemeleri yayımlanmadan önce el ile gözden geçirmelerini ve onaylamalarını tercih edebilir. Derecelendirmelerin ve incelemelerin moderatör tarafından el ile yayımlanmasını etkinleştirmek için Commerce site oluşturucuda **Derecelendirmeler ve incelemeler için moderatör gerektir** özelliğini etkinleştirmelisiniz.

## <a name="enable-the-require-moderator-for-ratings-and-reviews-feature-in-commerce-site-builder"></a>Commerce site oluşturucuda Derecelendirmeler ve incelemeler için moderatör gerektir özelliğini etkinleştirme

Commerce site oluşturucuda **Derecelendirmeler ve incelemeler için moderatör gerektir** özelliğini etkinleştirmek için aşağıdaki adımları izleyin.

1. **Giriş \> İncelemeler \> Ayarlar**'a gidin.
1. **Derecelendirmeler ve incelemeler için moderatör gerektir** seçeneğini **Açık** olarak ayarlayın.

> [!NOTE]
> **Derecelendirmeler ve incelemeler için moderatör gerektir** özelliğini etkinleştirerek derecelendirmelerin ve incelemelerin otomatik olarak yayımlanmasını durdurursunuz; böylece artık el ile yayımlanmaları gerekir. Ancak Azure Cognitive Services, inceleme başlıklarında ve içeriklerinde kötü sözcükleri düzenlemeye devam eder.

<!--![Require moderator for ratings and reviews setting in Commerce site builder.](media/Ratings-reviews-settings-human-moderation.png)-->

## <a name="publish-ratings-and-reviews"></a>Derecelendirmeleri ve incelemeleri yayımlama

**Derecelendirmeler ve incelemeler için moderatör gerektir** özelliğini etkinleştirdiğinizde e-ticaret sitenizde görünmeleri için derecelendirmeleri ve incelemeleri moderatörün el ile incelemesi ve yayımlaması gerekir.

Derecelendirmeleri ve incelemeleri Commerce site oluşturucuda incelemek ve yayımlamak için aşağıdaki adımları izleyin.

1. **İncelemeler \> Düzenleme**'ye gidin.
1. Izgarada, bir satırın **Durum** alanı **Yayımlanmadı** olarak ayarlanmışsa o satırdaki derecelendirme ve inceleme henüz yayımlanmamıştır. Yalnızca yayımlanmamış derecelendirmeleri ve incelemeleri görüntülemek için ızgaranın üzerindeki durum filtresinde **Durum: İnceleme gerekiyor**'u seçin.
1. Durumu **Yayımlanmadı** olan bir veya daha fazla derecelendirme ve inceleme seçin ve ardından komut çubuğunda **Yayımla**'yı seçin. Seçilen derecelendirme ve incelemeler yayım kuyruğuna eklenir ve yayımlandıktan sonra e-ticaret sitesinde görünür.

> [!NOTE]
> - Derecelendirme ve inceleme yayımlandıktan sonra **Yayımlanmadı** olan durum değeri boş bir değere (boş alan) dönüşür.
> - Farklı durumlara sahip birden fazla derecelendirme ve inceleme seçip ardından **Yayımla**'yı seçerseniz henüz yayımlanmayan derecelendirmeler ve incelemeler yayımlanır. Ancak daha önce yayımlanmış derecelendirmeler ve incelemeler tekrar yayımlanmaz.

Aşağıdaki şekilde, Commerce site oluşturucudaki **Düzenleme** sayfasında seçili durumdaki yayımlanmamış üç derecelendirme ve incelemenin gösterildiği bir örnek yer almaktadır.

![Commerce site oluşturucudaki Düzenleme sayfasında seçilen yayımlanmamış üç derecelendirme ve inceleme.](media/Ratings-reviews-publishing-reviews.png)

<!--![Dynamics 365 Commerce - Ratings and Review configuration 2](media/Ratings-reviews-published-reviews.png)-->
<!--![Status filter](media/Ratings-reviews-published-reviews-status-filter.png)-->

## <a name="additional-resources"></a>Ek kaynaklar

[Derecelendirmelere ve incelemelere genel bakış](ratings-reviews-overview.md)
