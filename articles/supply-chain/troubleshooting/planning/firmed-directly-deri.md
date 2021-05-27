---
title: Doğrudan türetilen kesinleştirilmiş siparişler inceleme iş akışı tarafından işlenir
description: Doğrudan türetilen kesinleştirilmiş siparişler, durumu İncelemede olan bir iş akışı tarafından işlenir.
author: ChristianRytt
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: ReqTransPo
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: ilebedev
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: d54985707d82df2b947a7cb615fc25f90aa31702
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026991"
---
# <a name="directly-derived-firmed-orders-are-processed-by-an-in-review-workflow"></a><span data-ttu-id="4e998-103">Doğrudan türetilen kesinleştirilmiş siparişler inceleme iş akışı tarafından işlenir</span><span class="sxs-lookup"><span data-stu-id="4e998-103">Directly derived firmed orders are processed by an in-review workflow</span></span>

<span data-ttu-id="4e998-104">KB numarası: 4612450</span><span class="sxs-lookup"><span data-stu-id="4e998-104">KB number: 4612450</span></span>

## <a name="symptoms"></a><span data-ttu-id="4e998-105">Belirtiler</span><span class="sxs-lookup"><span data-stu-id="4e998-105">Symptoms</span></span>

<span data-ttu-id="4e998-106">Doğrudan türetilen kesinleştirilmiş siparişler, durumu *İncelemede* olan bir iş akışı tarafından işlenir.</span><span class="sxs-lookup"><span data-stu-id="4e998-106">Directly derived firmed orders are processed by a workflow that has a status of *In-review*.</span></span>

## <a name="resolution"></a><span data-ttu-id="4e998-107">Çözünürlük</span><span class="sxs-lookup"><span data-stu-id="4e998-107">Resolution</span></span>

<span data-ttu-id="4e998-108">Değişiklik izleme etkinleştirildiğinde, kesinleştirilmiş türetilmiş siparişlere (alt yüklenici satınalma siparişleri) *İncelemede* durumu atanır.</span><span class="sxs-lookup"><span data-stu-id="4e998-108">When change tracking is enabled, a status of *In-review* is assigned to firmed derived orders (subcontract purchase orders).</span></span> <span data-ttu-id="4e998-109">Bu nedenle, bir satınalma siparişi türetilmişse (bir alt yüklenici satınalma siparişi), bu yalnızca bir iş akışına gönderilir.</span><span class="sxs-lookup"><span data-stu-id="4e998-109">Therefore, if a purchase order is derived (a subcontract purchase order), it's only submitted to a workflow.</span></span> <span data-ttu-id="4e998-110">Satınalma siparişi, kesinleştirilmemiş bir planlı satınalma siparişiyse satınalma siparişi hala *Taslak* durumunda olduğu sürece planlama altyapısının yeni planlı siparişler oluşturmamasını sağlamak için otomatik olarak onaylanır.</span><span class="sxs-lookup"><span data-stu-id="4e998-110">If a purchase order is a firmed planned purchase order, it's automatically approved to ensure that the planning engine doesn't create new planned orders while the purchase order is still in *Draft* status.</span></span>
