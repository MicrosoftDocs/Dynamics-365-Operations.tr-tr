---
title: Planlı siparişleri onayla
description: Bu konu, planlama optimizasyonu sırasında desteklenen planlı siparişlerin onayını açıklar.
author: ChristianRytt
manager: tfehr
ms.date: 08/21/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2020-08-21
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: b7975088be898ccecceb1f7be009cecff107f6e6
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "4439271"
---
# <a name="approve-planned-orders"></a>Planlı siparişleri onayla

[!include [banner](../../includes/banner.md)]

Bu konu, planlama optimizasyonunda planlı siparişlerin durumunun nasıl güncelleştirileceği hakkında bilgi sağlar.

Planlı siparişlerden kesinleştirilmiş sipariş oluşturmak üzere planlı siparişler onayının isteğe bağlı adımı olduğunu unutmayın. Değiştirilmiş Planlı siparişlerin onaylanması önerilir, aksi durumda sonraki planlama çalışması sırasında düzenlemeler yok sayılır ve üzerine yazılır.

![Planlı sipariş akışı](media/approved-planned-orders-1.png)

**Durum** alanı, aşağıdaki değerleri kullanarak ilerlemenizi izlemenize yardımcı olur:

- **İşlem görmedi:** Master planlama, planlı siparişler ürettiğinde, planlı siparişler *İşlem görmedi* durumunda olur. Bu durumdaki planlı siparişler sonraki planlama çalışmasında silinir.
- **Tamamlandı:** Planlı siparişi kesinleştirmemeye karar verirseniz, durumu *Tamamlandı* olarak değiştirerek bu planlı siparişin değerlendirilmesini tamamladığınızı belirtebilirsiniz. *İşlenmemiş* ve *Tamamlandı* durumlarının sistem tarafından aynı kabul edildiğini unutmayın.
- **Onaylandı:** Düzenlemeleri korumak istiyorsanız veya planlı bir siparişi kesinleştirmeyi planlıyorsanız, durumunu *Onaylandı* olarak değiştirin. Sonraki bir master planlama çalışması sırasında değiştirilmemeleri veya silinmemeleri için *Onaylandı* durumundaki planlı siparişler sabit olarak kabul edilerek master planlama tarafından tedarik edilmesi beklenir. Bunu başarmak için, planlama mantığı, Master planlama sırasında eski plan versiyonundaki *onaylanan* planlı siparişleri yeni plan sürümüne kopyalar. *Onaylandı* durumundaki planlı siparişlerinin yalnızca belirli master plan içinde tedarik edildiğini unutmayın.

Planlı siparişleri **Master planlama** çalışma alanından, **Planlı sipariş** listesinden veya **Planlı üretim emirleri**, **Planlı satınalma emirleri** ve **Planlı transfer** listelerinden yönetebilirsiniz.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]