---
title: "Fiyat ayarlamaları ve iskontolar"
description: "Bu makalede, fiyat ayarlamaları ve iskontoların açıklamasına perakende ve ticaret işlemleri için Microsoft Dynamics 365 hakkında bilgi sağlar."
author: josaw1
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.reviewer: annbe
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 15891
ms.assetid: bab5adf3-ddf0-4c22-a2eb-b4d25b88de99
ms.search.region: global
ms.search.industry: Retail
ms.author: scotttuc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: 01f249cbdabc6febf23dcd7103d4587cecdaad08
ms.lasthandoff: 03/31/2017


---

# <a name="price-adjustments-and-discounts"></a>Fiyat ayarlamaları ve iskontolar

Bu makalede, fiyat ayarlamaları ve iskontoların açıklamasına perakende ve ticaret işlemleri için Microsoft Dynamics 365 hakkında bilgi sağlar.

Dynamics 365 - işlemleri için perakende, yapabilirsiniz fiyat ayarlamaları ürünleri ve can da bir kalem veya bir hareketi (POS) satış noktasında uygulanan iskontolar ayarlamak için bir çağrı merkezi satış siparişi veya çevrimiçi sipariş. Hem fiyat ayarlaması hem de iskontolar fiyat gruplarına bağlanabilir. Hem fiyat ayarlaması hem de iskontolar için, tek bir başlangıç tarihi ve bitiş tarihi veya bir yeniden gerçekleşme dönemi, bir iskonto kodu ve birkaç ek öznitelik belirtebilirsiniz. Fiyat ayarlamaları ve iskontolar ürünlere, varyantlara veya kategorilere uygulanabilir. Bir ürün için birden fazla iskonto geçerliyse, bir müşteri iskontonun yapılandırmasına bağlı olarak iskontolardan ya birini ya da birleştirilmiş iskontosu alabilir. İşlemler için Dynamics 365 indirimi veya müşteriye en iyi fiyat veren indirimler birleşimi otomatik olarak uygular. Bir fiyat ayarlaması veya bir iskonto ayarladığınızda, fiyat gruplarının iskontonun geçerli olmasını istediğiniz doğru kanallara, kataloglara, ilişkilere veya sadakat programlarına atandığını doğruladığınızdan emin olun. Ayrıca, iskonto kodunu otomatik olarak üretmek istiyorsanız, yeni bir fiyat ayarlaması veya iskonto tanımlamadan önce **Perakende parametreleri** sayfasında numara sırası ayarlayın. **Not:** Bir fiyat ayarlamasını veya iskontosu silebilirsiniz. Ancak, istatistiksel bilgiler kaybolacaktır.

### <a name="types-of-discounts"></a>İskonto türleri

Perakende iskontolarının dört türü vardır:

-   **Basit iskonto** – Tek bir yüzde veya tutar.
-   **Miktar iskontosu** – İki veya daha fazla ürün satın alındığında bir iskonto uygulanır.
-   **Karıştır ve eşle iskontosu** – Belirli bir ürün kombinasyonu satın alındığında uygulanan iskonto.
-   **Eşik iskontosu** – Hareket toplamı belirli bir tutardan fazlayken uygulanan iskonto.

Hem fiyat ayarlaması hem de iskontolar fiyat gruplarına bağlanabilir. Fiyat grupları daha sonra kanallar, kataloglar, ilişkiler ve sadakat programları ile ilişkilendirilebilir.


