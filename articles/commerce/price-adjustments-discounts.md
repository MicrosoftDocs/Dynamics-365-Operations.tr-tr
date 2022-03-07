---
title: Fiyat ayarlamaları ve iskontolar
description: Bu makale, Dynamics 365 Commerce içinde fiyat ayarlaması ve iskontolar hakkında bilgi sağlar.
author: scott-tucker
ms.date: 06/11/2021
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
ms.openlocfilehash: 96a695df250cda514b7bd8b9716c0f03fb2bfd28d3af4daedaf1335c3099fbb6
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/05/2021
ms.locfileid: "6748510"
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

> [!NOTE]
> Karıştır ve eşle iskontosu ve eşik iskontosu, sırasıyla "Sayılamayan ürünleri say" ve "Sayılamayan ürünleri eşiğe doğru say" adlı özelliklere sahiptir. Bu özellikler etkinleştirilirse, herhangi bir iskonto için uygun olmayan bir madde, bir hareketi iskontoya uygun olarak saymaya yardımcı olabilir ancak yeterli madde iskontosu alamaz. 
> 
> Örneğin, her iki maddede de bir müşterinin %10 iskonto alması gereken iki satırı (A ve B) olan bir karıştır ve eşle iskontosu oluşturursanız, ancak madde A'nın "Tüm iskontoları engelle" yapılandırması varsa bu durum genellikle A maddesinin iskontoya dahil edilmesini engeller. Ancak, "Sayılamayan ürünleri say" özelliği etkinse karıştır ve eşle iskontosuna uygun olacak şekilde madde A kullanılabilir ancak %10 iskonto yalnızca B maddesine uygulanır. Benzer bir mantık eşik iskontosuna da uygulanır. 
>
> Ancak, karıştır ve eşle iskontolarında "Sayılamayan ürünleri say" özelliğiyle karşılaştırıldığında "Sayılamayan ürünleri eşiğe doğru say" özelliği ek bir özelliğe sahiptir. Eşik iskontosu etkinleştirilmişse ve maddenin başka bir iskonto almasını önleyen mevcut iskonto içeren bir madde varsa, bu madde için ödenen fiyat eşiğe yaklaşma hakkı kazanır ancak bu maddeye ek iskonto uygulanmaz.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
