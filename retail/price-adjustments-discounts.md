---
title: "Fiyat ayarlamaları ve iskontolar"
description: "Bu makalede, Microsoft Dynamics 365 for Operations&quot;da Perakende ve ticaret içinde fiyat ayarlamaları ve indirimler hakkında bilgiler sağlanmıştır."
author: josaw1
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.reviewer: annbe
ms.search.scope: AX 7.0.0, Operations, Core, Retail
ms.custom: 15891
ms.assetid: bab5adf3-ddf0-4c22-a2eb-b4d25b88de99
ms.search.region: global
ms.search.industry: Retail
ms.author: scotttuc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 6b1f91f863c8da35362ebb3036e76aa10d95ba65
ms.openlocfilehash: cb4f189b1f51788dea84702e4410cfaf8f570865
ms.contentlocale: tr-tr
ms.lasthandoff: 04/26/2017


---

# <a name="price-adjustments-and-discounts"></a>Fiyat ayarlamaları ve iskontolar

[!include[banner](includes/banner.md)]


Bu makalede, Microsoft Dynamics 365 for Operations'da Perakende ve ticaret içinde fiyat ayarlamaları ve indirimler hakkında bilgiler sağlanmıştır.

Dynamics 365 for Operations - Perakende içinde, ürüne yönelik fiyat ayarlamaları yapabilir ve ayrıca bir çağrı merkezi satış emrinde ya da bir çevrimiçi emirde bir satır maddesine veya satış noktasındaki bir harekete uygulanan iskontolar ayarlayabilirsiniz. Hem fiyat ayarlaması hem de iskontolar fiyat gruplarına bağlanabilir. Hem fiyat ayarlaması hem de iskontolar için, tek bir başlangıç tarihi ve bitiş tarihi veya bir yeniden gerçekleşme dönemi, bir iskonto kodu ve birkaç ek öznitelik belirtebilirsiniz. Fiyat ayarlamaları ve iskontolar ürünlere, varyantlara veya kategorilere uygulanabilir. Bir ürün için birden fazla iskonto geçerliyse, bir müşteri iskontonun yapılandırmasına bağlı olarak iskontolardan ya birini ya da birleştirilmiş iskontosu alabilir. Dynamics 365 for Operations iskontoyu veya iskonto kombinasyonunu müşteriye en iyi fiyatı verecek şekilde otomatik olarak uygular. Bir fiyat ayarlaması veya bir iskonto ayarladığınızda, fiyat gruplarının iskontonun geçerli olmasını istediğiniz doğru kanallara, kataloglara, ilişkilere veya sadakat programlarına atandığını doğruladığınızdan emin olun. Ayrıca, iskonto kodunu otomatik olarak üretmek istiyorsanız, yeni bir fiyat ayarlaması veya iskonto tanımlamadan önce **Perakende parametreleri** sayfasında numara sırası ayarlayın. **Not:** Bir fiyat ayarlamasını veya iskontosu silebilirsiniz. Ancak, istatistiksel bilgiler kaybolacaktır.

### <a name="types-of-discounts"></a>İskonto türleri

Perakende iskontolarının dört türü vardır:

-   **Basit iskonto** – Tek bir yüzde veya tutar.
-   **Miktar iskontosu** – İki veya daha fazla ürün satın alındığında bir iskonto uygulanır.
-   **Karıştır ve eşle iskontosu** – Belirli bir ürün kombinasyonu satın alındığında uygulanan iskonto.
-   **Eşik iskontosu** – Hareket toplamı belirli bir tutardan fazlayken uygulanan iskonto.

Hem fiyat ayarlaması hem de iskontolar fiyat gruplarına bağlanabilir. Fiyat grupları daha sonra kanallar, kataloglar, ilişkiler ve sadakat programları ile ilişkilendirilebilir.




