---
title: Amortisman yöntemleri
description: Bu makalede, Microsoft Dynamics 365 Finance tarafından desteklenen amortisman kurallarına ve amortisman yöntemlerine bir genel bakış sunulmuştur.
author: ShylaThompson
manager: AnnBe
ms.date: 04/25/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetDepreciationProfile, AssetGroupBookSetup, AssetGroupDepBookSetup
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 3441
ms.assetid: 1d8267b1-86a8-44bf-8814-f56b5d45a0ae
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4f1320d0adaad783f856ed6404039e7954920340
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/27/2019
ms.locfileid: "2187349"
---
# <a name="depreciation-methods-and-conventions"></a><span data-ttu-id="969ba-103">Amortisman yöntemleri ve kuralları</span><span class="sxs-lookup"><span data-stu-id="969ba-103">Depreciation methods and conventions</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="969ba-104">Bu makalede, desteklenen amortisman kurallarına ve amortisman yöntemlerine bir genel bakış sunulmuştur.</span><span class="sxs-lookup"><span data-stu-id="969ba-104">This article provides an overview of the supported depreciation conventions and depreciation methods.</span></span>

<span data-ttu-id="969ba-105">Çeşitli amortisman yöntemleri ve kuralları seçebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="969ba-105">You can select various depreciation methods and conventions.</span></span> <span data-ttu-id="969ba-106">Yöntemlerin amacı, sabit kıymetin amorti edilebilir değerini mali dönemlerine tahsis etmektir.</span><span class="sxs-lookup"><span data-stu-id="969ba-106">The purpose of the methods is to allocate the depreciable value of the fixed asset into fiscal periods.</span></span> <span data-ttu-id="969ba-107">Sabit kıymetin amorti edilebilir değeri, varsa bir ıskarta değeri tarafından azaltılan alım fiyatıdır.</span><span class="sxs-lookup"><span data-stu-id="969ba-107">The depreciable value of the fixed asset is the acquisition price, reduced by a scrap value, if any.</span></span> 

<span data-ttu-id="969ba-108">Amortisman kurallarını kullanıyor ve bir kıymet için bazı amortismanları atlayan son amortisman geçerlilik tarihini değiştirirseniz, geçen yıl için amortisman beklenenden daha fazla veya daha az olabilir.</span><span class="sxs-lookup"><span data-stu-id="969ba-108">If you are using depreciation conventions and you modify the last depreciation run date for an asset, which then causes some depreciations to be skipped, the depreciation for the last year might be more than or less than is expected.</span></span> <span data-ttu-id="969ba-109">Amortisman, son amortisman geçerlilik tarihinin değiştirilmesinden etkilenen amortisman dönemlerinin sayısı tarafından ayarlanır.</span><span class="sxs-lookup"><span data-stu-id="969ba-109">The depreciation is adjusted by the number of depreciation periods affected by the modification of the last depreciation run date.</span></span>

<span data-ttu-id="969ba-110">Örneğin, üç yıl üzerinden Yarı yıl amortisman kuralını kullanıyorsanız, amortisman normalde 3 1/2 yıl üzerinden olur.</span><span class="sxs-lookup"><span data-stu-id="969ba-110">For example, if you are using the Half year depreciation convention over three years, depreciation ordinarily occurs over 3 1/2 years.</span></span> <span data-ttu-id="969ba-111">3 1/2 yıllık süre içinde son amortisman geçerlilik tarihini değiştirirseniz, amortismanın son yılı etkilenen dönem sayısın ileri atar.</span><span class="sxs-lookup"><span data-stu-id="969ba-111">If you change the last depreciation run date during the 3 1/2 years, the last year of depreciation moves out the number of periods affected.</span></span> <span data-ttu-id="969ba-112">Tarihi üç ay ileri atarsanız, son yılda dokuz ay değerinde amortisman olur, ancak normalde altı ay değerinde amortisman olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="969ba-112">If you move the date by three months, the last year will have nine months’ worth of depreciation, when ordinarily there would be six months’ worth of depreciation.</span></span>

<span data-ttu-id="969ba-113">Aşağıdaki amortisman kurallarından birini seçebilirsiniz:</span><span class="sxs-lookup"><span data-stu-id="969ba-113">You can select from the following depreciation conventions.</span></span>


-   <span data-ttu-id="969ba-114">Yarıyıl</span><span class="sxs-lookup"><span data-stu-id="969ba-114">Half year</span></span>
-   <span data-ttu-id="969ba-115">Tam ay</span><span class="sxs-lookup"><span data-stu-id="969ba-115">Full month</span></span>
-   <span data-ttu-id="969ba-116">Üç aylık dönemin ortası</span><span class="sxs-lookup"><span data-stu-id="969ba-116">Mid quarter</span></span>
-   <span data-ttu-id="969ba-117">Ayın ortası (Ayın 1'i)</span><span class="sxs-lookup"><span data-stu-id="969ba-117">Mid month (1st of month)</span></span>
-   <span data-ttu-id="969ba-118">Ayın ortası (Ayın 15'i)</span><span class="sxs-lookup"><span data-stu-id="969ba-118">Mid month (15th of month)</span></span>
-   <span data-ttu-id="969ba-119">Yarı yıl (yılın başlangıcı)</span><span class="sxs-lookup"><span data-stu-id="969ba-119">Half year (start of year)</span></span>
-   <span data-ttu-id="969ba-120">Yarı yıl (sonraki yıl)</span><span class="sxs-lookup"><span data-stu-id="969ba-120">Half year (next year)</span></span>

<span data-ttu-id="969ba-121">Aşağıdaki amortisman yöntemlerinden birini seçebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="969ba-121">You can select from the following depreciation methods.</span></span>
-   <span data-ttu-id="969ba-122">Sabit servis ömrü</span><span class="sxs-lookup"><span data-stu-id="969ba-122">Straight line service life</span></span>
-   <span data-ttu-id="969ba-123">Azalan bakiye</span><span class="sxs-lookup"><span data-stu-id="969ba-123">Reducing balance</span></span>
-   <span data-ttu-id="969ba-124">El ile</span><span class="sxs-lookup"><span data-stu-id="969ba-124">Manual</span></span>
-   <span data-ttu-id="969ba-125">Faktör</span><span class="sxs-lookup"><span data-stu-id="969ba-125">Factor</span></span>
-   <span data-ttu-id="969ba-126">Tüketim</span><span class="sxs-lookup"><span data-stu-id="969ba-126">Consumption</span></span>
-   <span data-ttu-id="969ba-127">Sabit kalan ömür</span><span class="sxs-lookup"><span data-stu-id="969ba-127">Straight line life remaining</span></span>
-   <span data-ttu-id="969ba-128">%200 azalan bakiye</span><span class="sxs-lookup"><span data-stu-id="969ba-128">200% reducing balance</span></span>
-   <span data-ttu-id="969ba-129">%175 azalan bakiye</span><span class="sxs-lookup"><span data-stu-id="969ba-129">175% reducing balance</span></span>
-   <span data-ttu-id="969ba-130">%150 azalan bakiye</span><span class="sxs-lookup"><span data-stu-id="969ba-130">150% reducing balance</span></span>
-   <span data-ttu-id="969ba-131">%125 azalan bakiye</span><span class="sxs-lookup"><span data-stu-id="969ba-131">125% reducing balance</span></span>





<a name="additional-resources"></a><span data-ttu-id="969ba-132">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="969ba-132">Additional resources</span></span>
--------

[<span data-ttu-id="969ba-133">Sabit kıymet amortismanı</span><span class="sxs-lookup"><span data-stu-id="969ba-133">Fixed asset depreciation</span></span>](fixed-asset-depreciation.md)

[<span data-ttu-id="969ba-134">Sabit servis ömrü amortismanı</span><span class="sxs-lookup"><span data-stu-id="969ba-134">Straight line service life depreciation</span></span>](Straight-line-service-life-depreciation.md)

[<span data-ttu-id="969ba-135">Azalan bakiyeli amortisman</span><span class="sxs-lookup"><span data-stu-id="969ba-135">Reducing balance depreciation</span></span>](reduce-balance-depreciation.md)

[<span data-ttu-id="969ba-136">El ile amortisman</span><span class="sxs-lookup"><span data-stu-id="969ba-136">Manual depreciation</span></span>](manual-depreciation.md)

[<span data-ttu-id="969ba-137">Faktör amortisman</span><span class="sxs-lookup"><span data-stu-id="969ba-137">Factor depreciation</span></span>](factor-depreciation.md)

[<span data-ttu-id="969ba-138">Tüketim esasına göre amortisman</span><span class="sxs-lookup"><span data-stu-id="969ba-138">Consumption depreciation</span></span>](consumption-depreciation.md)

[<span data-ttu-id="969ba-139">Sabit kalan ömür amortismanı</span><span class="sxs-lookup"><span data-stu-id="969ba-139">Straight line life remaining depreciation</span></span>](straight-line-life-remaining-depreciation.md)

[<span data-ttu-id="969ba-140">Yüzde 125 azalan bakiyeli amortisman</span><span class="sxs-lookup"><span data-stu-id="969ba-140">125 percent reducing balance depreciation</span></span>](125-percent-reducing-balance-depreciation.md)

[<span data-ttu-id="969ba-141">Yüzde 150 azalan bakiyeli amortisman</span><span class="sxs-lookup"><span data-stu-id="969ba-141">150 percent reducing balance depreciation</span></span>](150-percent-reducing-balance-depreciation.md)

[<span data-ttu-id="969ba-142">Yüzde 175 azalan bakiyeli amortisman</span><span class="sxs-lookup"><span data-stu-id="969ba-142">175 percent reducing balance depreciation</span></span>](175-percent-reducing-balance-depreciation.md)

[<span data-ttu-id="969ba-143">Yüzde 200 azalan bakiyeli amortisman</span><span class="sxs-lookup"><span data-stu-id="969ba-143">200 percent reducing balance depreciation</span></span>](200-percent-reducing-balance-depreciation.md)



