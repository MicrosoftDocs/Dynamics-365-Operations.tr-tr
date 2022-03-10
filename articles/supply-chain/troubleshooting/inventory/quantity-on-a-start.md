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
ms.openlocfilehash: 4625570cb706199dca78f23b1864ca1d81cc66e896cf10d6d5f16cf1a9d1dc16
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/05/2021
ms.locfileid: "6713506"
---
# <a name="quantity-on-a-started-quarantine-order-isnt-updated-when-the-order-is-split"></a>Sipariş bölündüğünde, başlatılan bir karantina emrindeki miktar güncelleştirilmiyor

KB numarası: 4613113

## <a name="symptoms"></a>Belirtiler

Bir karantina siparişi oluşturup bunu bölmeyi denediğinizde, sipariş miktarı bölündükten sonra kalan tutara güncelleştirilmez.

## <a name="resolution"></a>Çözünürlük

Sistem, ilgili karantina siparişi için oluşturulan orijinal miktarı izleyebilmek için karantina emrinden gelen orijinal miktarı değiştirmez. Ancak, sistem bir karantina emrinden bölünen miktarı izler. Bu izlemeyi gerçekleştirmek için, `QuantityThatHasSplitIntoOtherQuarantineOrders` adlı bir veritabanı alanı kullanır. Ancak, bu alan kullanıcı arabiriminde (UI) görünmez.
