---
title: Madde indirim grupları kullanıldığında müşteri indirimlerinin toplamı başarısız olur
description: Madde indirim gruplarıyla birlikte müşteri indirim anlaşmaları kullandığınızda indirimler hesaplanır ancak toplama başarısız olur.
author: sherry-zheng
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: PdsRebateTableListPage
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 5222d5a52a34ecfa4a1eac96a2cb561f257f17ea
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026973"
---
# <a name="cumulation-of-customer-rebates-fails-when-item-rebate-groups-are-used"></a><span data-ttu-id="218c8-103">Madde indirim grupları kullanıldığında müşteri indirimlerinin toplamı başarısız olur</span><span class="sxs-lookup"><span data-stu-id="218c8-103">Cumulation of customer rebates fails when item rebate groups are used</span></span>

<span data-ttu-id="218c8-104">KB numarası: 4611372</span><span class="sxs-lookup"><span data-stu-id="218c8-104">KB number: 4611372</span></span>

## <a name="symptoms"></a><span data-ttu-id="218c8-105">Belirtiler</span><span class="sxs-lookup"><span data-stu-id="218c8-105">Symptoms</span></span>

<span data-ttu-id="218c8-106">Madde indirim gruplarıyla birlikte müşteri indirim anlaşmaları (*tutar* türünden) kullandığınızda indirimler hesaplanır ancak toplama başarısız olur.</span><span class="sxs-lookup"><span data-stu-id="218c8-106">When you use customer rebate agreements (of the *amount* type) in combination with item rebate groups, rebates are calculated, but cumulation fails.</span></span>

## <a name="resolution"></a><span data-ttu-id="218c8-107">Çözünürlük</span><span class="sxs-lookup"><span data-stu-id="218c8-107">Resolution</span></span>

<span data-ttu-id="218c8-108">Sistem, beklendiği şekilde davranıyordur.</span><span class="sxs-lookup"><span data-stu-id="218c8-108">The system is behaving as designed.</span></span> <span data-ttu-id="218c8-109">Madde grupları, yalnızca eşik koşulu aynı olan maddeleri gruplandırır.</span><span class="sxs-lookup"><span data-stu-id="218c8-109">Item groups group only items that have the same threshold condition.</span></span> <span data-ttu-id="218c8-110">İndirim koşulu (eşik), madde grubundaki her bir maddenin tutarı için belirlenir, madde grubundaki tüm maddelerin toplam tutarı için değil.</span><span class="sxs-lookup"><span data-stu-id="218c8-110">The rebate condition (threshold) is set against the amount for each item, not against the cumulated amount for any item in the item group.</span></span>
