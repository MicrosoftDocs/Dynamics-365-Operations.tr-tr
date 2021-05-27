---
title: Negatif günler içinde bir satınalma varken planlı satınalma siparişi oluşturuluyor
description: Karşılama kodu Min/maks ise, satınalma işlemi negatif günler içinde olduğunda Planlama Optimizasyonu planlı bir satınalma siparişi oluşturur.
author: ChristianRytt
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: ReqTransPo,MpsIntegrationParameters
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: ilebedev
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 826496c2de956ff949dd79ab8aa643053719bf75
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026989"
---
# <a name="planned-purchase-order-is-created-when-a-purchase-exists-within-negative-days"></a><span data-ttu-id="12c9d-103">Negatif günler içinde bir satınalma varken planlı satınalma siparişi oluşturuluyor</span><span class="sxs-lookup"><span data-stu-id="12c9d-103">Planned purchase order is created when a purchase exists within negative days</span></span>

<span data-ttu-id="12c9d-104">KB numarası: 4614298</span><span class="sxs-lookup"><span data-stu-id="12c9d-104">KB number: 4614298</span></span>

## <a name="symptoms"></a><span data-ttu-id="12c9d-105">Belirtiler</span><span class="sxs-lookup"><span data-stu-id="12c9d-105">Symptoms</span></span>

<span data-ttu-id="12c9d-106">Karşılama kodu *Min/maks* ise, satınalma işlemi negatif günler içinde olduğunda Planlama Optimizasyonu planlı bir satınalma siparişi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="12c9d-106">If the coverage code is *Min/max*, Planning Optimization creates a planned purchase order when a purchase exists within negative days.</span></span>

## <a name="resolution"></a><span data-ttu-id="12c9d-107">Çözünürlük</span><span class="sxs-lookup"><span data-stu-id="12c9d-107">Resolution</span></span>

<span data-ttu-id="12c9d-108">Planlama Optimizasyonu, negatif günleri desteklemiyor.</span><span class="sxs-lookup"><span data-stu-id="12c9d-108">Planning Optimization doesn't support negative days.</span></span> <span data-ttu-id="12c9d-109">Ancak, her zaman planlı siparişlerin geçerli tarihe göre sağlama süresi içinde zamanlanmamasını sağlar.</span><span class="sxs-lookup"><span data-stu-id="12c9d-109">However, it always ensures that planned orders won't be scheduled within the lead time relative to the current date.</span></span> <span data-ttu-id="12c9d-110">Örneğin, satınalma sağlama süresi 10 gün ve bir satınalma siparişinin bugünden itibaren sekiz gün sonra gelmesi bekleniyor.</span><span class="sxs-lookup"><span data-stu-id="12c9d-110">For example, the purchase lead time is 10 days, and a purchase order is expected to arrive eight days from today.</span></span> <span data-ttu-id="12c9d-111">Bu durumda, satınalma siparişi bugünden beş gün sonra yapılacak bir talep için tedarik olarak kullanılır.</span><span class="sxs-lookup"><span data-stu-id="12c9d-111">In this case, the purchase order will be used as supply for demand that is five days from today.</span></span>

<span data-ttu-id="12c9d-112">Bu nedenle, sağlama sürelerini senaryoların tümünü (veya neredeyse tümünü) kapsayacak şekilde ayarlamanızı öneririz.</span><span class="sxs-lookup"><span data-stu-id="12c9d-112">Therefore, we recommend that you adjust your lead times to cover all (or almost all) of your scenarios.</span></span>
