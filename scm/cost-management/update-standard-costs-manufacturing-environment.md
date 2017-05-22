---
title: "Bir üretim ortamındaki standart maliyetleri güncelleştirme"
description: "Bu makale, bir üretim ortamındaki standart maliyetleri güncelleştirme konusunda rehberlik sağlar."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: CostingVersion, InventStdCostConv
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 79663
ms.assetid: 3a7c3d13-8dbc-442d-a281-ac0ebe99ec83
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: mguada
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: 564251038b9bdd836857f177e996ab17433e8000
ms.contentlocale: tr-tr
ms.lasthandoff: 04/25/2017


---

# <a name="update-standard-costs-in-a-manufacturing-environment"></a>Bir üretim ortamındaki standart maliyetleri güncelleştirme

[!include[banner](../includes/banner.md)]


Bu makale, bir üretim ortamındaki standart maliyetleri güncelleştirme konusunda rehberlik sağlar. 

Güncelleştirmeler yeni maddeler, maliyet kategorileri veya dolaylı maliyet hesaplama formüllerini yansıtabilir. Ayrıca, düzeltmeleri ve maliyet değişikliklerini yansıtabilir. Güncelleştirme tipi, aşağıdaki durumlarda gösterildiği gibi standart maliyetleri güncelleştirmek için yerine getirmeniz gereken adımları etkiler:

-   Satın alınan maddeler için beklenen standart maliyet değişikliklerini girin ve madde maliyeti kayıtlarının ilgili tarihteki durumunu **Etkin** olarak değiştirin. Ancak satın alınan maddeleri kullanan üretilmiş maddelerin maliyetlerini yeniden hesaplamayın.
-   Yeni satın alınan bir madde için standart maliyetleri girin ancak üretilmiş maddelerin maliyetlerini, yeni satın alınan maddeyi bir bileşen olarak içeren bir ürün reçetesiyle (BOM) yeniden hesaplamayın.
-   Satın alınan bir maddenin maliyetini düzeltin veya değiştirin veya bir satınalma maddesine atanmış maliyet grubunu değiştirin ve tüm üretilmiş maddelerin maliyetini, satın alınan maddeyi bir bileşen olarak içeren bir ürün reçetesi ile hesaplayın.
-   Bir maliyet kategorisinin maliyetini değiştirin ve tüm üretilmiş maddelerin maliyetini, maliyet kategorisini kullanan rota faaliyetlerine sahip olan bir rota versiyonuyla hesaplayın.
-   Rota operasyonlarına atanmış olan maliyet kategorilerini veya maliyet kategorilerine atanmış olan maliyet grubunu değiştirin. Daha sonra, maliyet kategorisi kullanan bir rota operasyonuna sahip bir rota versiyonuna sahip tüm üretilmiş maddeler için maliyeti hesaplayın.
-   Dolaylı maliyet hesaplama formülünü değiştirin ve değişiklikten etkilenen tüm üretilmiş maddelerin maliyetini hesaplayın.
-   Üretilmiş bir madde için üretim tesisini değiştirin veya ekleyin ve maddenin tesis için üretilmiş maliyetini hesaplayın.
-   Üretilmiş bir madde için maliyeti hesaplayın veya yeniden hesaplayın ve tüm üretilmiş maddelerin maliyetini, üretilmiş maddeyi bir bileşen olarak içeren bir ürün reçetesi versiyonuna sahip tüm maddeler için yeniden hesaplayın.
-   Yeni üretilmiş maddenin maliyetlerini tanımlı, onaylı ve etkin ürün reçetesi ve rota bilgilerine dayanarak hesaplayın.

Her durumda, standart maliyetlerin nasıl güncelleştirileceği dikkatle ele alınmalıdır.



