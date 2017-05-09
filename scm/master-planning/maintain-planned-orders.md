---
title: "Planlı siparişleri koru"
description: "Bu maddede planlı siparişleri yönetme yöntemleri hakkında bilgiler yer alır. Planlı siparişlerin durumunun nasıl güncelleştirileceğini, kesinleştirileceğini ve seçilen planlı sipariş ile aynı duruma sahip planlı siparişlerin nasıl filtreleneceğini açıklar."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: ReqTransPo
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 19151
ms.assetid: 54123f4c-b4ca-4ce4-9358-b067aa04c968
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9ccbe5815ebb54e00265e130be9c82491aebabce
ms.openlocfilehash: c01a192e637bfe74a60370290db72c439faf40d0
ms.lasthandoff: 03/31/2017


---

# <a name="maintain-planned-orders"></a>Planlı siparişleri koru

[!include[banner](../includes/banner.md)]


Bu maddede planlı siparişleri yönetme yöntemleri hakkında bilgiler yer alır. Planlı siparişlerin durumunun nasıl güncelleştirileceğini, kesinleştirileceğini ve seçilen planlı sipariş ile aynı duruma sahip planlı siparişlerin nasıl filtreleneceğini açıklar.

Planlı siparişleri **Master planlama** çalışma alanından, **Planlı sipariş** listesinden veya **Planlı üretim emirleri**, **Planlı satınalma emirleri** ve **Planlı transfer** listelerinden yönetebilirsiniz. İlerlemenizi takip etmeye yardımcı olan **Durum** alanını kullanabilirsiniz. Aşağıdaki değerler kullanılır:

-   Master planlama planlı siparişler ürettiğinde, planlı siparişler **İşlem görmedi** durumunda olur.
-   Planlı bir siparişi kesinleştirmemeye karar vermeniz halinde, durumunu **Tamamlandı** olarak ayarlayabilirsiniz.
-   Planlı bir siparişi kesinleştirmeye karar verdiğinizde, durumunu **Onaylandı** olarak ayarlayabilirsiniz. Bu durum, planlı siparişin kesinleştirilmesini onayladığınızı ama henüz kesinleştirmediğinizi gösterilir.

**Not:** Onaylanan bir planlı sipariş geçerli durumunda sonraki master planlama hesaplamasına transfer edilir. Planlı siparişleri **Kesinleştir** seçeneğine tıklayarak kesinleştirebilirsiniz. Aşağıdaki planlı siparişleri kesinleştirebilirsiniz:

-   Seçilen planlı sipariş.
-   Birden çok planlı sipariş.
-   **Açılım** sayfasından bir açılımla üretilen planlı siparişler. **Planlı siparişler** seçeneğine tıklayın, planlı siparişi seçin, sonra da **Kesinleştir** seçeneğine tıklayın.

Planlı bir sipariş kesinleştirildiğinde, ilgili modülün siparişler bölümüne taşınır. **Not:** Özel durumu olan planlı siparişi sağ tıklatıp, aynı durumda olan planlı siparişlere filtre uygulayabilirsiniz. Bu işlevsellik örneğin **Onaylandı** durumundaki tüm siparişleri filtrelemek istediğinizde kullanışlıdır, böylece bunları daha sonra kesinleştirebilirsiniz.

<a name="see-also"></a>Ayrıca bkz.
--------

[Master planlar](master-plans.md)




