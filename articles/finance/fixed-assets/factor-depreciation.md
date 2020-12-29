---
title: Faktör amortisman
description: Bu makale, faktör amortisman yöntemi hakkında genel bir bakış sağlar.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetDepreciationProfile
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 13831
ms.assetid: 2b6c4fe4-02ff-4191-bcad-32f1f34c15f2
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c5c36441e926cd5a82c802a350adf6b2ed6d6387
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "4448752"
---
# <a name="factor-depreciation"></a><span data-ttu-id="d3e77-103">Faktör amortisman</span><span class="sxs-lookup"><span data-stu-id="d3e77-103">Factor depreciation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d3e77-104">Bu makale, faktör amortisman yöntemi hakkında genel bir bakış sağlar.</span><span class="sxs-lookup"><span data-stu-id="d3e77-104">This article gives an overview of the factor depreciation method.</span></span>

<span data-ttu-id="d3e77-105">Faktörler, kıymetlere amortisman uygulamak için kullanılan yüzdelerdir.</span><span class="sxs-lookup"><span data-stu-id="d3e77-105">Factors are the percentages that are used to depreciate assets.</span></span> <span data-ttu-id="d3e77-106">Bir sabit kıymet amortisman profili ayarlayıp **Amortisman profilleri** sayfasındaki **Yöntem** alanında **Faktör**'ü seçtiğinizde, artan paylı, azalan paylı, eşit paylı amortisman ayarlayabilirsiniz:</span><span class="sxs-lookup"><span data-stu-id="d3e77-106">When you set up a fixed asset depreciation profile and select **Factor** in the **Method** field on the **Depreciation profiles** page, you can set up progressive, digressive, or straight line depreciation:</span></span>

-   <span data-ttu-id="d3e77-107">Artan paylı amortismanda, amortisman tutarı her amortisman döneminde artar.</span><span class="sxs-lookup"><span data-stu-id="d3e77-107">In progressive depreciation, the amount of depreciation increases each depreciation period.</span></span>
-   <span data-ttu-id="d3e77-108">Azalan paylı amortismanda, dönem başına amortisman tutarı zaman içinde azalır.</span><span class="sxs-lookup"><span data-stu-id="d3e77-108">In digressive depreciation, the amount of depreciation per period decreases over time.</span></span>
-   <span data-ttu-id="d3e77-109">Eşit paylı amortismanda, amortisman her dönem için aynıdır.</span><span class="sxs-lookup"><span data-stu-id="d3e77-109">In straight line depreciation, the depreciation is the same in each period.</span></span>

<span data-ttu-id="d3e77-110">Aşağıdaki kurallar ve örnekler, her tip amortisman için faktörleri nasıl ayarlayacağınızı gösterir.</span><span class="sxs-lookup"><span data-stu-id="d3e77-110">The rules and examples that follow indicate how you can set up factors for each type of depreciation.</span></span> 

> [!NOTE] 
> <span data-ttu-id="d3e77-111">**Yöntem** alanında **Faktör**'ü seçtiğinizde, **Faktör** alanı ve **Aralık** alanı görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="d3e77-111">When you select **Factor** in the **Method** field, the **Factor** field and the **Interval** field are displayed.</span></span>

## <a name="progressive-depreciation"></a><span data-ttu-id="d3e77-112">Artan paylı amortisman</span><span class="sxs-lookup"><span data-stu-id="d3e77-112">Progressive depreciation</span></span>
<span data-ttu-id="d3e77-113">**Faktör** alanındaki değer **50**'den büyüktür.</span><span class="sxs-lookup"><span data-stu-id="d3e77-113">The value in the **Factor** field is more than **50**.</span></span>

### <a name="example"></a><span data-ttu-id="d3e77-114">Örnek</span><span class="sxs-lookup"><span data-stu-id="d3e77-114">Example</span></span>

<span data-ttu-id="d3e77-115">Alım fiyatı 100.000, faktör 70, hizmet ömrü 10 yıl ve amortisman 1 Ocak'ta başlıyor.</span><span class="sxs-lookup"><span data-stu-id="d3e77-115">The acquisition price is 100,000, the factor is 70, the service life is 10 years, and depreciation starts on January 1.</span></span> <span data-ttu-id="d3e77-116">Amortisman tutarları ve net defter değeri tutarları yalnızca hizmet ömrünün ilk altı yılı için gösterilir.</span><span class="sxs-lookup"><span data-stu-id="d3e77-116">The depreciation amounts and net book value amounts are shown only for the first six years of service life.</span></span>

| <span data-ttu-id="d3e77-117">Yıl</span><span class="sxs-lookup"><span data-stu-id="d3e77-117">Year</span></span> | <span data-ttu-id="d3e77-118">Dönem</span><span class="sxs-lookup"><span data-stu-id="d3e77-118">Period</span></span>      | <span data-ttu-id="d3e77-119">Amortisman tutarı</span><span class="sxs-lookup"><span data-stu-id="d3e77-119">Depreciation amount</span></span> | <span data-ttu-id="d3e77-120">Net defter değeri tutarı</span><span class="sxs-lookup"><span data-stu-id="d3e77-120">Net book value amount</span></span> |
|------|-------------|---------------------|-----------------------|
| <span data-ttu-id="d3e77-121">1</span><span class="sxs-lookup"><span data-stu-id="d3e77-121">1</span></span>    | <span data-ttu-id="d3e77-122">31 Aralık</span><span class="sxs-lookup"><span data-stu-id="d3e77-122">December 31</span></span> | <span data-ttu-id="d3e77-123">307,69</span><span class="sxs-lookup"><span data-stu-id="d3e77-123">307.69</span></span>              | <span data-ttu-id="d3e77-124">99.692,31</span><span class="sxs-lookup"><span data-stu-id="d3e77-124">99,692.31</span></span>             |
| <span data-ttu-id="d3e77-125">2</span><span class="sxs-lookup"><span data-stu-id="d3e77-125">2</span></span>    | <span data-ttu-id="d3e77-126">31 Aralık</span><span class="sxs-lookup"><span data-stu-id="d3e77-126">December 31</span></span> | <span data-ttu-id="d3e77-127">1.447,21</span><span class="sxs-lookup"><span data-stu-id="d3e77-127">1,447.21</span></span>            | <span data-ttu-id="d3e77-128">98.245,10</span><span class="sxs-lookup"><span data-stu-id="d3e77-128">98,245.10</span></span>             |
| <span data-ttu-id="d3e77-129">3</span><span class="sxs-lookup"><span data-stu-id="d3e77-129">3</span></span>    | <span data-ttu-id="d3e77-130">31 Aralık</span><span class="sxs-lookup"><span data-stu-id="d3e77-130">December 31</span></span> | <span data-ttu-id="d3e77-131">3.104,50</span><span class="sxs-lookup"><span data-stu-id="d3e77-131">3,104.50</span></span>            | <span data-ttu-id="d3e77-132">95.140,60</span><span class="sxs-lookup"><span data-stu-id="d3e77-132">95,140.60</span></span>             |
| <span data-ttu-id="d3e77-133">4</span><span class="sxs-lookup"><span data-stu-id="d3e77-133">4</span></span>    | <span data-ttu-id="d3e77-134">31 Aralık</span><span class="sxs-lookup"><span data-stu-id="d3e77-134">December 31</span></span> | <span data-ttu-id="d3e77-135">5.150,21</span><span class="sxs-lookup"><span data-stu-id="d3e77-135">5,150.21</span></span>            | <span data-ttu-id="d3e77-136">89.990,39</span><span class="sxs-lookup"><span data-stu-id="d3e77-136">89,990.39</span></span>             |
| <span data-ttu-id="d3e77-137">5</span><span class="sxs-lookup"><span data-stu-id="d3e77-137">5</span></span>    | <span data-ttu-id="d3e77-138">31 Aralık</span><span class="sxs-lookup"><span data-stu-id="d3e77-138">December 31</span></span> | <span data-ttu-id="d3e77-139">7.522,95</span><span class="sxs-lookup"><span data-stu-id="d3e77-139">7,522.95</span></span>            | <span data-ttu-id="d3e77-140">82.467,44</span><span class="sxs-lookup"><span data-stu-id="d3e77-140">82,467.44</span></span>             |
| <span data-ttu-id="d3e77-141">6</span><span class="sxs-lookup"><span data-stu-id="d3e77-141">6</span></span>    | <span data-ttu-id="d3e77-142">31 Aralık</span><span class="sxs-lookup"><span data-stu-id="d3e77-142">December 31</span></span> | <span data-ttu-id="d3e77-143">10.184,06</span><span class="sxs-lookup"><span data-stu-id="d3e77-143">10,184.06</span></span>           | <span data-ttu-id="d3e77-144">72.283,38</span><span class="sxs-lookup"><span data-stu-id="d3e77-144">72,283.38</span></span>             |

## <a name="digressive-depreciation"></a><span data-ttu-id="d3e77-145">Azalan paylı amortisman</span><span class="sxs-lookup"><span data-stu-id="d3e77-145">Digressive depreciation</span></span>
<span data-ttu-id="d3e77-146">**Faktör** alanındaki değer **50**'den küçüktür.</span><span class="sxs-lookup"><span data-stu-id="d3e77-146">The value in the **Factor** field is less than **50**.</span></span>

### <a name="example"></a><span data-ttu-id="d3e77-147">Örnek</span><span class="sxs-lookup"><span data-stu-id="d3e77-147">Example</span></span>

<span data-ttu-id="d3e77-148">Alım fiyatı 100.000, faktör 20, hizmet ömrü 10 yıl ve amortisman 1 Ocak'ta başlıyor.</span><span class="sxs-lookup"><span data-stu-id="d3e77-148">The acquisition price is 100,000, the factor is 20, the service life is 10 years, and depreciation starts on January 1.</span></span> <span data-ttu-id="d3e77-149">Amortisman tutarları ve net defter değeri tutarları yalnızca hizmet ömrünün ilk altı yılı için gösterilir.</span><span class="sxs-lookup"><span data-stu-id="d3e77-149">The depreciation amounts and net book value amounts are shown only for the first six years of service life.</span></span>

| <span data-ttu-id="d3e77-150">Yıl</span><span class="sxs-lookup"><span data-stu-id="d3e77-150">Year</span></span> | <span data-ttu-id="d3e77-151">Dönem</span><span class="sxs-lookup"><span data-stu-id="d3e77-151">Period</span></span>      | <span data-ttu-id="d3e77-152">Amortisman tutarı</span><span class="sxs-lookup"><span data-stu-id="d3e77-152">Depreciation amount</span></span> | <span data-ttu-id="d3e77-153">Net defter değeri tutarı</span><span class="sxs-lookup"><span data-stu-id="d3e77-153">Net book value amount</span></span> |
|------|-------------|---------------------|-----------------------|
| <span data-ttu-id="d3e77-154">1</span><span class="sxs-lookup"><span data-stu-id="d3e77-154">1</span></span>    | <span data-ttu-id="d3e77-155">31 Aralık</span><span class="sxs-lookup"><span data-stu-id="d3e77-155">December 31</span></span> | <span data-ttu-id="d3e77-156">56.080,43</span><span class="sxs-lookup"><span data-stu-id="d3e77-156">56,080.43</span></span>           | <span data-ttu-id="d3e77-157">43.919,57</span><span class="sxs-lookup"><span data-stu-id="d3e77-157">43,919.57</span></span>             |
| <span data-ttu-id="d3e77-158">2</span><span class="sxs-lookup"><span data-stu-id="d3e77-158">2</span></span>    | <span data-ttu-id="d3e77-159">31 Aralık</span><span class="sxs-lookup"><span data-stu-id="d3e77-159">December 31</span></span> | <span data-ttu-id="d3e77-160">10.665,70</span><span class="sxs-lookup"><span data-stu-id="d3e77-160">10,665.70</span></span>           | <span data-ttu-id="d3e77-161">33.253,87</span><span class="sxs-lookup"><span data-stu-id="d3e77-161">33,253.87</span></span>             |
| <span data-ttu-id="d3e77-162">3</span><span class="sxs-lookup"><span data-stu-id="d3e77-162">3</span></span>    | <span data-ttu-id="d3e77-163">31 Aralık</span><span class="sxs-lookup"><span data-stu-id="d3e77-163">December 31</span></span> | <span data-ttu-id="d3e77-164">7.156,22</span><span class="sxs-lookup"><span data-stu-id="d3e77-164">7,156.22</span></span>            | <span data-ttu-id="d3e77-165">26.097,65</span><span class="sxs-lookup"><span data-stu-id="d3e77-165">26,097.65</span></span>             |
| <span data-ttu-id="d3e77-166">4</span><span class="sxs-lookup"><span data-stu-id="d3e77-166">4</span></span>    | <span data-ttu-id="d3e77-167">31 Aralık</span><span class="sxs-lookup"><span data-stu-id="d3e77-167">December 31</span></span> | <span data-ttu-id="d3e77-168">5.538,06</span><span class="sxs-lookup"><span data-stu-id="d3e77-168">5,538.06</span></span>            | <span data-ttu-id="d3e77-169">20.559,59</span><span class="sxs-lookup"><span data-stu-id="d3e77-169">20,559.59</span></span>             |
| <span data-ttu-id="d3e77-170">5</span><span class="sxs-lookup"><span data-stu-id="d3e77-170">5</span></span>    | <span data-ttu-id="d3e77-171">31 Aralık</span><span class="sxs-lookup"><span data-stu-id="d3e77-171">December 31</span></span> | <span data-ttu-id="d3e77-172">4.579,89</span><span class="sxs-lookup"><span data-stu-id="d3e77-172">4,579.89</span></span>            | <span data-ttu-id="d3e77-173">15.979,70</span><span class="sxs-lookup"><span data-stu-id="d3e77-173">15,979.70</span></span>             |
| <span data-ttu-id="d3e77-174">6</span><span class="sxs-lookup"><span data-stu-id="d3e77-174">6</span></span>    | <span data-ttu-id="d3e77-175">31 Aralık</span><span class="sxs-lookup"><span data-stu-id="d3e77-175">December 31</span></span> | <span data-ttu-id="d3e77-176">3.937,36</span><span class="sxs-lookup"><span data-stu-id="d3e77-176">3,937.36</span></span>            | <span data-ttu-id="d3e77-177">12.042,34</span><span class="sxs-lookup"><span data-stu-id="d3e77-177">12,042.34</span></span>             |

## <a name="straight-line-depreciation"></a><span data-ttu-id="d3e77-178">Eşit paylı amortisman</span><span class="sxs-lookup"><span data-stu-id="d3e77-178">Straight line depreciation</span></span>
<span data-ttu-id="d3e77-179">**Faktör** alanındaki değer **50**'ye eşittir.</span><span class="sxs-lookup"><span data-stu-id="d3e77-179">The value in the **Factor** field is equal to **50**.</span></span> <span data-ttu-id="d3e77-180">Bu durumda, amortisman her dönemde aynıdır ve [Sabit servis ömrü amortismanı](straight-line-service-life-depreciation.md) içinde açıklandığı gibi, diğer alanlarda belirttiğiniz değerlerin etkilerini değerlendirmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="d3e77-180">In this case, the depreciation is the same in each period, and you should consider the implications of the values that you have specified in other fields, as described in [Straight line service life depreciation](straight-line-service-life-depreciation.md).</span></span>



