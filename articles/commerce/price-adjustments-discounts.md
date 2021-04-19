---
title: Fiyat ayarlamaları ve iskontolar
description: Bu makale, Dynamics 365 Commerce içinde fiyat ayarlaması ve iskontolar hakkında bilgi sağlar.
author: scott-tucker
ms.date: 11/16/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RetailParameters, RetailPeriodicDiscount
audience: Application User
ms.reviewer: josaw
ms.custom: 15891
ms.assetid: bab5adf3-ddf0-4c22-a2eb-b4d25b88de99
ms.search.region: global
ms.search.industry: Retail
ms.author: scotttuc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 2d3e8025c5ab28296713634094694156f9addf62
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/31/2021
ms.locfileid: "5802803"
---
# <a name="price-adjustments-and-discounts"></a>Fiyat ayarlamaları ve iskontolar

[!include [banner](includes/banner.md)]

Bu makale, Dynamics 365 Commerce içinde fiyat ayarlaması ve iskontolar hakkında bilgi sağlar.

Commerce içinde, ürünlerde fiyat ayarlamaları yapabilir ve bir satır maddesine veya satış noktası (POS), çağrı merkezi satış siparişi veya çevrimiçi siparişteki bir harekete uygulanacak iskontolar ayarlayabilirsiniz. Hem fiyat ayarlaması hem de iskontolar fiyat gruplarına bağlanabilir. Hem fiyat ayarlaması hem de iskontolar için, tek bir başlangıç tarihi ve bitiş tarihi veya bir yeniden gerçekleşme dönemi, bir iskonto kodu ve birkaç ek öznitelik belirtebilirsiniz. 

Fiyat ayarlamaları ve iskontolar ürünlere, varyantlara veya kategorilere uygulanabilir. Bir ürün için birden fazla iskonto geçerliyse, bir müşteri iskontonun yapılandırmasına bağlı olarak iskontolardan ya birini ya da birleştirilmiş iskontosu alabilir. Commerce, iskontoyu veya iskonto kombinasyonunu müşteriye en iyi fiyatı verecek şekilde otomatik olarak uygular. Bir fiyat ayarlaması veya bir iskonto ayarladığınızda, fiyat gruplarının iskontonun geçerli olmasını istediğiniz doğru kanallara, kataloglara, ilişkilere veya sadakat programlarına atandığını doğruladığınızdan emin olun. Ayrıca, iskonto kodunu otomatik olarak üretmek istiyorsanız, yeni bir fiyat ayarlaması veya iskonto tanımlamadan önce **Ticaret parametreleri** sayfasında numara sırası ayarlayın.

> [!NOTE]
> Bir fiyat ayarlamasını veya iskontosu silebilirsiniz. Ancak, istatistiksel bilgiler kaybolacaktır.

## <a name="types-of-discounts"></a>İskonto türleri

İskontolarının birçok türü vardır:

- **Basit iskonto** – Tek bir yüzde veya tutar.
- **Miktar iskontosu** – İki veya daha fazla ürün satın alındığında bir iskonto uygulanır.
- **Karıştır ve eşle iskontosu** – Belirli bir ürün kombinasyonu satın alındığında uygulanan iskonto.
- **Eşik iskontosu** – Hareket toplamı belirli bir tutardan fazlayken uygulanan iskonto.
- **Ödeme tabanlı iskonto** – Ödeme için hareket toplamı belirtilen bir tutardan fazla olduğunda ve belirli bir ödeme türü (örneğin, nakit, alacak veya borç kartı) kullanıldığında uygulanan iskonto.
- **Sevkiyat iskontosu** – siparişte, hareket toplamı belirtilen tutardan fazla olduğunda uygulanan iskonto (örneğin, iki günlük sevkiyat veya bir gecede nakliye gibi) sipariş için kullanılır.

Hem fiyat ayarlaması hem de iskontolar fiyat gruplarına bağlanabilir. Fiyat grupları daha sonra kanallar, kataloglar, ilişkiler ve sadakat programları ile ilişkilendirilebilir.


[!INCLUDE[footer-include](../includes/footer-banner.md)]