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
ms.custom: 13831
ms.assetid: 2b6c4fe4-02ff-4191-bcad-32f1f34c15f2
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4920f7f90b859006ecdcd486eaa9f4449442e51a
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/15/2021
ms.locfileid: "4976153"
---
# <a name="factor-depreciation"></a><span data-ttu-id="3a57b-103">Faktör amortisman</span><span class="sxs-lookup"><span data-stu-id="3a57b-103">Factor depreciation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="3a57b-104">Bu makale, faktör amortisman yöntemi hakkında genel bir bakış sağlar.</span><span class="sxs-lookup"><span data-stu-id="3a57b-104">This article gives an overview of the factor depreciation method.</span></span>

<span data-ttu-id="3a57b-105">Faktörler, kıymetlere amortisman uygulamak için kullanılan yüzdelerdir.</span><span class="sxs-lookup"><span data-stu-id="3a57b-105">Factors are the percentages that are used to depreciate assets.</span></span> <span data-ttu-id="3a57b-106">Bir sabit kıymet amortisman profili ayarlayıp **Amortisman profilleri** sayfasındaki **Yöntem** alanında **Faktör**'ü seçtiğinizde, artan paylı, azalan paylı, eşit paylı amortisman ayarlayabilirsiniz:</span><span class="sxs-lookup"><span data-stu-id="3a57b-106">When you set up a fixed asset depreciation profile and select **Factor** in the **Method** field on the **Depreciation profiles** page, you can set up progressive, digressive, or straight line depreciation:</span></span>

-   <span data-ttu-id="3a57b-107">Artan paylı amortismanda, amortisman tutarı her amortisman döneminde artar.</span><span class="sxs-lookup"><span data-stu-id="3a57b-107">In progressive depreciation, the amount of depreciation increases each depreciation period.</span></span>
-   <span data-ttu-id="3a57b-108">Azalan paylı amortismanda, dönem başına amortisman tutarı zaman içinde azalır.</span><span class="sxs-lookup"><span data-stu-id="3a57b-108">In digressive depreciation, the amount of depreciation per period decreases over time.</span></span>
-   <span data-ttu-id="3a57b-109">Eşit paylı amortismanda, amortisman her dönem için aynıdır.</span><span class="sxs-lookup"><span data-stu-id="3a57b-109">In straight line depreciation, the depreciation is the same in each period.</span></span>

<span data-ttu-id="3a57b-110">Aşağıdaki kurallar ve örnekler, her tip amortisman için faktörleri nasıl ayarlayacağınızı gösterir.</span><span class="sxs-lookup"><span data-stu-id="3a57b-110">The rules and examples that follow indicate how you can set up factors for each type of depreciation.</span></span> 

> [!NOTE] 
> <span data-ttu-id="3a57b-111">**Yöntem** alanında **Faktör**'ü seçtiğinizde, **Faktör** alanı ve **Aralık** alanı görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="3a57b-111">When you select **Factor** in the **Method** field, the **Factor** field and the **Interval** field are displayed.</span></span>

## <a name="progressive-depreciation"></a><span data-ttu-id="3a57b-112">Artan paylı amortisman</span><span class="sxs-lookup"><span data-stu-id="3a57b-112">Progressive depreciation</span></span>
<span data-ttu-id="3a57b-113">**Faktör** alanındaki değer **50**'den büyüktür.</span><span class="sxs-lookup"><span data-stu-id="3a57b-113">The value in the **Factor** field is more than **50**.</span></span>

### <a name="example"></a><span data-ttu-id="3a57b-114">Örnek</span><span class="sxs-lookup"><span data-stu-id="3a57b-114">Example</span></span>

<span data-ttu-id="3a57b-115">Alım fiyatı 100.000, faktör 70, hizmet ömrü 10 yıl ve amortisman 1 Ocak'ta başlıyor.</span><span class="sxs-lookup"><span data-stu-id="3a57b-115">The acquisition price is 100,000, the factor is 70, the service life is 10 years, and depreciation starts on January 1.</span></span> <span data-ttu-id="3a57b-116">Amortisman tutarları ve net defter değeri tutarları yalnızca hizmet ömrünün ilk altı yılı için gösterilir.</span><span class="sxs-lookup"><span data-stu-id="3a57b-116">The depreciation amounts and net book value amounts are shown only for the first six years of service life.</span></span>

| <span data-ttu-id="3a57b-117">Yıl</span><span class="sxs-lookup"><span data-stu-id="3a57b-117">Year</span></span> | <span data-ttu-id="3a57b-118">Dönem</span><span class="sxs-lookup"><span data-stu-id="3a57b-118">Period</span></span>      | <span data-ttu-id="3a57b-119">Amortisman tutarı</span><span class="sxs-lookup"><span data-stu-id="3a57b-119">Depreciation amount</span></span> | <span data-ttu-id="3a57b-120">Net defter değeri tutarı</span><span class="sxs-lookup"><span data-stu-id="3a57b-120">Net book value amount</span></span> |
|------|-------------|---------------------|-----------------------|
| <span data-ttu-id="3a57b-121">1</span><span class="sxs-lookup"><span data-stu-id="3a57b-121">1</span></span>    | <span data-ttu-id="3a57b-122">31 Aralık</span><span class="sxs-lookup"><span data-stu-id="3a57b-122">December 31</span></span> | <span data-ttu-id="3a57b-123">307,69</span><span class="sxs-lookup"><span data-stu-id="3a57b-123">307.69</span></span>              | <span data-ttu-id="3a57b-124">99.692,31</span><span class="sxs-lookup"><span data-stu-id="3a57b-124">99,692.31</span></span>             |
| <span data-ttu-id="3a57b-125">2</span><span class="sxs-lookup"><span data-stu-id="3a57b-125">2</span></span>    | <span data-ttu-id="3a57b-126">31 Aralık</span><span class="sxs-lookup"><span data-stu-id="3a57b-126">December 31</span></span> | <span data-ttu-id="3a57b-127">1.447,21</span><span class="sxs-lookup"><span data-stu-id="3a57b-127">1,447.21</span></span>            | <span data-ttu-id="3a57b-128">98.245,10</span><span class="sxs-lookup"><span data-stu-id="3a57b-128">98,245.10</span></span>             |
| <span data-ttu-id="3a57b-129">3</span><span class="sxs-lookup"><span data-stu-id="3a57b-129">3</span></span>    | <span data-ttu-id="3a57b-130">31 Aralık</span><span class="sxs-lookup"><span data-stu-id="3a57b-130">December 31</span></span> | <span data-ttu-id="3a57b-131">3.104,50</span><span class="sxs-lookup"><span data-stu-id="3a57b-131">3,104.50</span></span>            | <span data-ttu-id="3a57b-132">95.140,60</span><span class="sxs-lookup"><span data-stu-id="3a57b-132">95,140.60</span></span>             |
| <span data-ttu-id="3a57b-133">4</span><span class="sxs-lookup"><span data-stu-id="3a57b-133">4</span></span>    | <span data-ttu-id="3a57b-134">31 Aralık</span><span class="sxs-lookup"><span data-stu-id="3a57b-134">December 31</span></span> | <span data-ttu-id="3a57b-135">5.150,21</span><span class="sxs-lookup"><span data-stu-id="3a57b-135">5,150.21</span></span>            | <span data-ttu-id="3a57b-136">89.990,39</span><span class="sxs-lookup"><span data-stu-id="3a57b-136">89,990.39</span></span>             |
| <span data-ttu-id="3a57b-137">5</span><span class="sxs-lookup"><span data-stu-id="3a57b-137">5</span></span>    | <span data-ttu-id="3a57b-138">31 Aralık</span><span class="sxs-lookup"><span data-stu-id="3a57b-138">December 31</span></span> | <span data-ttu-id="3a57b-139">7.522,95</span><span class="sxs-lookup"><span data-stu-id="3a57b-139">7,522.95</span></span>            | <span data-ttu-id="3a57b-140">82.467,44</span><span class="sxs-lookup"><span data-stu-id="3a57b-140">82,467.44</span></span>             |
| <span data-ttu-id="3a57b-141">6</span><span class="sxs-lookup"><span data-stu-id="3a57b-141">6</span></span>    | <span data-ttu-id="3a57b-142">31 Aralık</span><span class="sxs-lookup"><span data-stu-id="3a57b-142">December 31</span></span> | <span data-ttu-id="3a57b-143">10.184,06</span><span class="sxs-lookup"><span data-stu-id="3a57b-143">10,184.06</span></span>           | <span data-ttu-id="3a57b-144">72.283,38</span><span class="sxs-lookup"><span data-stu-id="3a57b-144">72,283.38</span></span>             |

## <a name="digressive-depreciation"></a><span data-ttu-id="3a57b-145">Azalan paylı amortisman</span><span class="sxs-lookup"><span data-stu-id="3a57b-145">Digressive depreciation</span></span>
<span data-ttu-id="3a57b-146">**Faktör** alanındaki değer **50**'den küçüktür.</span><span class="sxs-lookup"><span data-stu-id="3a57b-146">The value in the **Factor** field is less than **50**.</span></span>

### <a name="example"></a><span data-ttu-id="3a57b-147">Örnek</span><span class="sxs-lookup"><span data-stu-id="3a57b-147">Example</span></span>

<span data-ttu-id="3a57b-148">Alım fiyatı 100.000, faktör 20, hizmet ömrü 10 yıl ve amortisman 1 Ocak'ta başlıyor.</span><span class="sxs-lookup"><span data-stu-id="3a57b-148">The acquisition price is 100,000, the factor is 20, the service life is 10 years, and depreciation starts on January 1.</span></span> <span data-ttu-id="3a57b-149">Amortisman tutarları ve net defter değeri tutarları yalnızca hizmet ömrünün ilk altı yılı için gösterilir.</span><span class="sxs-lookup"><span data-stu-id="3a57b-149">The depreciation amounts and net book value amounts are shown only for the first six years of service life.</span></span>

| <span data-ttu-id="3a57b-150">Yıl</span><span class="sxs-lookup"><span data-stu-id="3a57b-150">Year</span></span> | <span data-ttu-id="3a57b-151">Dönem</span><span class="sxs-lookup"><span data-stu-id="3a57b-151">Period</span></span>      | <span data-ttu-id="3a57b-152">Amortisman tutarı</span><span class="sxs-lookup"><span data-stu-id="3a57b-152">Depreciation amount</span></span> | <span data-ttu-id="3a57b-153">Net defter değeri tutarı</span><span class="sxs-lookup"><span data-stu-id="3a57b-153">Net book value amount</span></span> |
|------|-------------|---------------------|-----------------------|
| <span data-ttu-id="3a57b-154">1</span><span class="sxs-lookup"><span data-stu-id="3a57b-154">1</span></span>    | <span data-ttu-id="3a57b-155">31 Aralık</span><span class="sxs-lookup"><span data-stu-id="3a57b-155">December 31</span></span> | <span data-ttu-id="3a57b-156">56.080,43</span><span class="sxs-lookup"><span data-stu-id="3a57b-156">56,080.43</span></span>           | <span data-ttu-id="3a57b-157">43.919,57</span><span class="sxs-lookup"><span data-stu-id="3a57b-157">43,919.57</span></span>             |
| <span data-ttu-id="3a57b-158">2</span><span class="sxs-lookup"><span data-stu-id="3a57b-158">2</span></span>    | <span data-ttu-id="3a57b-159">31 Aralık</span><span class="sxs-lookup"><span data-stu-id="3a57b-159">December 31</span></span> | <span data-ttu-id="3a57b-160">10.665,70</span><span class="sxs-lookup"><span data-stu-id="3a57b-160">10,665.70</span></span>           | <span data-ttu-id="3a57b-161">33.253,87</span><span class="sxs-lookup"><span data-stu-id="3a57b-161">33,253.87</span></span>             |
| <span data-ttu-id="3a57b-162">3</span><span class="sxs-lookup"><span data-stu-id="3a57b-162">3</span></span>    | <span data-ttu-id="3a57b-163">31 Aralık</span><span class="sxs-lookup"><span data-stu-id="3a57b-163">December 31</span></span> | <span data-ttu-id="3a57b-164">7.156,22</span><span class="sxs-lookup"><span data-stu-id="3a57b-164">7,156.22</span></span>            | <span data-ttu-id="3a57b-165">26.097,65</span><span class="sxs-lookup"><span data-stu-id="3a57b-165">26,097.65</span></span>             |
| <span data-ttu-id="3a57b-166">4</span><span class="sxs-lookup"><span data-stu-id="3a57b-166">4</span></span>    | <span data-ttu-id="3a57b-167">31 Aralık</span><span class="sxs-lookup"><span data-stu-id="3a57b-167">December 31</span></span> | <span data-ttu-id="3a57b-168">5.538,06</span><span class="sxs-lookup"><span data-stu-id="3a57b-168">5,538.06</span></span>            | <span data-ttu-id="3a57b-169">20.559,59</span><span class="sxs-lookup"><span data-stu-id="3a57b-169">20,559.59</span></span>             |
| <span data-ttu-id="3a57b-170">5</span><span class="sxs-lookup"><span data-stu-id="3a57b-170">5</span></span>    | <span data-ttu-id="3a57b-171">31 Aralık</span><span class="sxs-lookup"><span data-stu-id="3a57b-171">December 31</span></span> | <span data-ttu-id="3a57b-172">4.579,89</span><span class="sxs-lookup"><span data-stu-id="3a57b-172">4,579.89</span></span>            | <span data-ttu-id="3a57b-173">15.979,70</span><span class="sxs-lookup"><span data-stu-id="3a57b-173">15,979.70</span></span>             |
| <span data-ttu-id="3a57b-174">6</span><span class="sxs-lookup"><span data-stu-id="3a57b-174">6</span></span>    | <span data-ttu-id="3a57b-175">31 Aralık</span><span class="sxs-lookup"><span data-stu-id="3a57b-175">December 31</span></span> | <span data-ttu-id="3a57b-176">3.937,36</span><span class="sxs-lookup"><span data-stu-id="3a57b-176">3,937.36</span></span>            | <span data-ttu-id="3a57b-177">12.042,34</span><span class="sxs-lookup"><span data-stu-id="3a57b-177">12,042.34</span></span>             |

## <a name="straight-line-depreciation"></a><span data-ttu-id="3a57b-178">Eşit paylı amortisman</span><span class="sxs-lookup"><span data-stu-id="3a57b-178">Straight line depreciation</span></span>
<span data-ttu-id="3a57b-179">**Faktör** alanındaki değer **50**'ye eşittir.</span><span class="sxs-lookup"><span data-stu-id="3a57b-179">The value in the **Factor** field is equal to **50**.</span></span> <span data-ttu-id="3a57b-180">Bu durumda, amortisman her dönemde aynıdır ve [Sabit servis ömrü amortismanı](straight-line-service-life-depreciation.md) içinde açıklandığı gibi, diğer alanlarda belirttiğiniz değerlerin etkilerini değerlendirmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="3a57b-180">In this case, the depreciation is the same in each period, and you should consider the implications of the values that you have specified in other fields, as described in [Straight line service life depreciation](straight-line-service-life-depreciation.md).</span></span>



