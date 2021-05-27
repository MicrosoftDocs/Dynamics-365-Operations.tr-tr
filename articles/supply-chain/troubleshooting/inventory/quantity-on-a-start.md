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
# <a name="quantity-on-a-started-quarantine-order-isnt-updated-when-the-order-is-split"></a><span data-ttu-id="a242c-103">Sipariş bölündüğünde, başlatılan bir karantina emrindeki miktar güncelleştirilmiyor</span><span class="sxs-lookup"><span data-stu-id="a242c-103">Quantity on a started quarantine order isn't updated when the order is split</span></span>

<span data-ttu-id="a242c-104">KB numarası: 4613113</span><span class="sxs-lookup"><span data-stu-id="a242c-104">KB number: 4613113</span></span>

## <a name="symptoms"></a><span data-ttu-id="a242c-105">Belirtiler</span><span class="sxs-lookup"><span data-stu-id="a242c-105">Symptoms</span></span>

<span data-ttu-id="a242c-106">Bir karantina siparişi oluşturup bunu bölmeyi denediğinizde, sipariş miktarı bölündükten sonra kalan tutara güncelleştirilmez.</span><span class="sxs-lookup"><span data-stu-id="a242c-106">When you create a quarantine order and try to split it, the order quantity isn't updated to the remaining quantity after the split.</span></span>

## <a name="resolution"></a><span data-ttu-id="a242c-107">Çözünürlük</span><span class="sxs-lookup"><span data-stu-id="a242c-107">Resolution</span></span>

<span data-ttu-id="a242c-108">Sistem, ilgili karantina siparişi için oluşturulan orijinal miktarı izleyebilmek için karantina emrinden gelen orijinal miktarı değiştirmez.</span><span class="sxs-lookup"><span data-stu-id="a242c-108">The system doesn't change the original quantity from a quarantine order to ensure that you can track the original quantity that was created for that quarantine order.</span></span> <span data-ttu-id="a242c-109">Ancak, sistem bir karantina emrinden bölünen miktarı izler.</span><span class="sxs-lookup"><span data-stu-id="a242c-109">However, the system does track the quantity that is split from a quarantine order.</span></span> <span data-ttu-id="a242c-110">Bu izlemeyi gerçekleştirmek için, `QuantityThatHasSplitIntoOtherQuarantineOrders` adlı bir veritabanı alanı kullanır.</span><span class="sxs-lookup"><span data-stu-id="a242c-110">To do this tracking, it uses a database field that is named `QuantityThatHasSplitIntoOtherQuarantineOrders`.</span></span> <span data-ttu-id="a242c-111">Ancak, bu alan kullanıcı arabiriminde (UI) görünmez.</span><span class="sxs-lookup"><span data-stu-id="a242c-111">However, this field isn't visible in the user interface (UI).</span></span>
