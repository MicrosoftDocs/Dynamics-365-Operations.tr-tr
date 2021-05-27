---
title: Sipariş bölündüğünde, başlatılan bir karantina emrindeki miktar güncelleştirilmiyor
description: Bir karantina siparişi oluşturup bunu bölmeyi denediğinizde, sipariş miktarı bölünmüş kalan tutara güncelleştirilmez.
author: niwang
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: InventQuarantineOrder
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: shawan
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: a8af535257ce217629d5ba92e624623c3ea39345
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026996"
---
# <a name="quantity-on-a-started-quarantine-order-isnt-updated-when-the-order-is-split"></a>Sipariş bölündüğünde, başlatılan bir karantina emrindeki miktar güncelleştirilmiyor

KB numarası: 4613113

## <a name="symptoms"></a>Belirtiler

Bir karantina siparişi oluşturup bunu bölmeyi denediğinizde, sipariş miktarı bölündükten sonra kalan tutara güncelleştirilmez.

## <a name="resolution"></a>Çözünürlük

Sistem, ilgili karantina siparişi için oluşturulan orijinal miktarı izleyebilmek için karantina emrinden gelen orijinal miktarı değiştirmez. Ancak, sistem bir karantina emrinden bölünen miktarı izler. Bu izlemeyi gerçekleştirmek için, `QuantityThatHasSplitIntoOtherQuarantineOrders` adlı bir veritabanı alanı kullanır. Ancak, bu alan kullanıcı arabiriminde (UI) görünmez.
