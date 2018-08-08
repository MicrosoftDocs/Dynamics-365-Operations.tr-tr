---
title: "Azaltma anahtarları"
description: "Bu makalelerde bir azaltma anahtarının nasıl ayarlanacağını gösteren örnekler verilmiştir. Çeşitli azaltma anahtarı ayarları ve her birinin sonuçları hakkında da bilgiler içerir. Bir zzaltma anahtarını, tahmin gereksinimlerinin nasıl azaltılacağını tanımlamak için kullanabilirsiniz."
author: roxanadiaconu
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ReqPlanSched
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 19251
ms.assetid: aa9e0dfb-6052-4a2e-9378-89507c02fdf2
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 1d98cbff30620256c9d13e7b4a90314db150e33e
ms.openlocfilehash: 3e62431a1fdbeb81dda68297f034ee00adece079
ms.contentlocale: tr-tr
ms.lasthandoff: 08/07/2018

---

# <a name="reduction-keys"></a><span data-ttu-id="fe7dd-105">Azaltma anahtarları</span><span class="sxs-lookup"><span data-stu-id="fe7dd-105">Reduction keys</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="fe7dd-106">Bu makalelerde bir azaltma anahtarının nasıl ayarlanacağını gösteren örnekler verilmiştir.</span><span class="sxs-lookup"><span data-stu-id="fe7dd-106">This articles provides examples that show how to set up a reduction key.</span></span> <span data-ttu-id="fe7dd-107">Çeşitli azaltma anahtarı ayarları ve her birinin sonuçları hakkında da bilgiler içerir.</span><span class="sxs-lookup"><span data-stu-id="fe7dd-107">It includes information about the various reduction key settings and the results of each.</span></span> <span data-ttu-id="fe7dd-108">Bir zzaltma anahtarını, tahmin gereksinimlerinin nasıl azaltılacağını tanımlamak için kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="fe7dd-108">You can use a reduction key to define how to reduce forecast requirements.</span></span>

<a name="example-1-percent---reduction-key-forecast-reduction-principle"></a><span data-ttu-id="fe7dd-109">Örnek 1: Yüzde - Azaltma anahtarı tahmin azaltma ilkesi</span><span class="sxs-lookup"><span data-stu-id="fe7dd-109">Example 1: Percent - reduction key forecast reduction principle</span></span>
---------------------------------------------------------------

<span data-ttu-id="fe7dd-110">Bu örnek bir azaltma anahtarının, talep tahmini gereksinimlerini azaltma anahtarı tarafından tanımlanan yüzdelere ve dönemlere göre nasıl azalttığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="fe7dd-110">This example shows how a reduction key reduces demand forecast requirements according to the percentages and periods that are defined by the reduction key.</span></span>

1. <span data-ttu-id="fe7dd-111">**Azaltma anahtarları** sayfasında aşağıdaki satırları ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="fe7dd-111">On the **Reduction keys** page, set up the following lines.</span></span>

   | <span data-ttu-id="fe7dd-112">Değiştirme</span><span class="sxs-lookup"><span data-stu-id="fe7dd-112">Change</span></span> | <span data-ttu-id="fe7dd-113">Birim</span><span class="sxs-lookup"><span data-stu-id="fe7dd-113">Unit</span></span>  | <span data-ttu-id="fe7dd-114">Yüzde</span><span class="sxs-lookup"><span data-stu-id="fe7dd-114">Percent</span></span> |
   |--------|-------|---------|
   |   <span data-ttu-id="fe7dd-115">1</span><span class="sxs-lookup"><span data-stu-id="fe7dd-115">1</span></span>    | <span data-ttu-id="fe7dd-116">Ay</span><span class="sxs-lookup"><span data-stu-id="fe7dd-116">Month</span></span> |   <span data-ttu-id="fe7dd-117">100</span><span class="sxs-lookup"><span data-stu-id="fe7dd-117">100</span></span>   |
   |   <span data-ttu-id="fe7dd-118">2</span><span class="sxs-lookup"><span data-stu-id="fe7dd-118">2</span></span>    | <span data-ttu-id="fe7dd-119">Ay</span><span class="sxs-lookup"><span data-stu-id="fe7dd-119">Month</span></span> |   <span data-ttu-id="fe7dd-120">75</span><span class="sxs-lookup"><span data-stu-id="fe7dd-120">75</span></span>    |
   |   <span data-ttu-id="fe7dd-121">3</span><span class="sxs-lookup"><span data-stu-id="fe7dd-121">3</span></span>    | <span data-ttu-id="fe7dd-122">Ay</span><span class="sxs-lookup"><span data-stu-id="fe7dd-122">Month</span></span> |   <span data-ttu-id="fe7dd-123">50</span><span class="sxs-lookup"><span data-stu-id="fe7dd-123">50</span></span>    |
   |   <span data-ttu-id="fe7dd-124">4</span><span class="sxs-lookup"><span data-stu-id="fe7dd-124">4</span></span>    | <span data-ttu-id="fe7dd-125">Ay</span><span class="sxs-lookup"><span data-stu-id="fe7dd-125">Month</span></span> |   <span data-ttu-id="fe7dd-126">25</span><span class="sxs-lookup"><span data-stu-id="fe7dd-126">25</span></span>    |


2. <span data-ttu-id="fe7dd-127">Azaltma anahtarını ürünün kapsam grubuna bağlayın.</span><span class="sxs-lookup"><span data-stu-id="fe7dd-127">Link the reduction key to the item's coverage group.</span></span>
3. <span data-ttu-id="fe7dd-128">**Ana planlar** sayfasında, **Azaltma ilkesi** alanında **Yüzde - azaltma anahtarı**'nı seçin.</span><span class="sxs-lookup"><span data-stu-id="fe7dd-128">On the **Master plans** page, in the **Reduction principle** field, select **Percent - reduction key**.</span></span>
4. <span data-ttu-id="fe7dd-129">Aylık 1.000 parçalık bir talep tahmini oluşturun.</span><span class="sxs-lookup"><span data-stu-id="fe7dd-129">Create a demand forecast of 1,000 pieces per month.</span></span>

<span data-ttu-id="fe7dd-130">Tahmin planını 1 Ocak'ta çalıştırırsanız, talep tahmini gereksinimleri **Azaltma anahtarları** sayfasında ayarladığınız yüzdelere göre tüketilir.</span><span class="sxs-lookup"><span data-stu-id="fe7dd-130">If you run forecast scheduling on January 1, the demand forecast requirements are consumed according to the percentages that you set up on the **Reduction keys** page.</span></span> <span data-ttu-id="fe7dd-131">Aşağıdaki gereksinim miktarları ana plana transfer edilir.</span><span class="sxs-lookup"><span data-stu-id="fe7dd-131">The following requirement quantities are transferred to the master plan.</span></span>

| <span data-ttu-id="fe7dd-132">Ay</span><span class="sxs-lookup"><span data-stu-id="fe7dd-132">Month</span></span>                | <span data-ttu-id="fe7dd-133">Gerekli parça sayısı</span><span class="sxs-lookup"><span data-stu-id="fe7dd-133">Number of pieces required</span></span> |
|----------------------|---------------------------|
| <span data-ttu-id="fe7dd-134">Ocak</span><span class="sxs-lookup"><span data-stu-id="fe7dd-134">January</span></span>              | <span data-ttu-id="fe7dd-135">0</span><span class="sxs-lookup"><span data-stu-id="fe7dd-135">0</span></span>                         |
| <span data-ttu-id="fe7dd-136">Şubat</span><span class="sxs-lookup"><span data-stu-id="fe7dd-136">February</span></span>             | <span data-ttu-id="fe7dd-137">250</span><span class="sxs-lookup"><span data-stu-id="fe7dd-137">250</span></span>                       |
| <span data-ttu-id="fe7dd-138">Mart</span><span class="sxs-lookup"><span data-stu-id="fe7dd-138">March</span></span>                | <span data-ttu-id="fe7dd-139">500</span><span class="sxs-lookup"><span data-stu-id="fe7dd-139">500</span></span>                       |
| <span data-ttu-id="fe7dd-140">Nisan</span><span class="sxs-lookup"><span data-stu-id="fe7dd-140">April</span></span>                | <span data-ttu-id="fe7dd-141">750</span><span class="sxs-lookup"><span data-stu-id="fe7dd-141">750</span></span>                       |
| <span data-ttu-id="fe7dd-142">Mayıs - Aralık arası</span><span class="sxs-lookup"><span data-stu-id="fe7dd-142">May through December</span></span> | <span data-ttu-id="fe7dd-143">1.000</span><span class="sxs-lookup"><span data-stu-id="fe7dd-143">1,000</span></span>                     |

## <a name="example-2-transactions--reduction-key-forecast-reduction-principle"></a><span data-ttu-id="fe7dd-144">Örnek 2: Hareketler azaltma anahtarı tahmini azaltma ilkesi</span><span class="sxs-lookup"><span data-stu-id="fe7dd-144">Example 2: Transactions  reduction key forecast reduction principle</span></span>
<span data-ttu-id="fe7dd-145">Bu örnek, azaltma anahtarı tarafından tanımlanan dönemler boyunca gerçekleşen fiili siparişlerin talep tahmini gereksinimlerini nasıl azalttığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="fe7dd-145">This example shows how actual orders that occur during the periods that are defined by the reduction key reduce demand forecast requirements.</span></span>

-   <span data-ttu-id="fe7dd-146">**Ana planlar** sayfasında, **Azaltma ilkesi** alanında **Hareketler - azaltma anahtarı**'nı seçin.</span><span class="sxs-lookup"><span data-stu-id="fe7dd-146">On the **Master plans** page, in the **Reduction principle** field, select **Transactions - reduction key**.</span></span>

<span data-ttu-id="fe7dd-147">Aşağıdaki satış siparişleri 1 Ocak'tadır.</span><span class="sxs-lookup"><span data-stu-id="fe7dd-147">The following sales orders exist on January 1.</span></span>

| <span data-ttu-id="fe7dd-148">Ay</span><span class="sxs-lookup"><span data-stu-id="fe7dd-148">Month</span></span>    | <span data-ttu-id="fe7dd-149">Gerekli parça sayısı</span><span class="sxs-lookup"><span data-stu-id="fe7dd-149">Number of pieces ordered</span></span> |
|----------|--------------------------|
| <span data-ttu-id="fe7dd-150">Ocak</span><span class="sxs-lookup"><span data-stu-id="fe7dd-150">January</span></span>  | <span data-ttu-id="fe7dd-151">956</span><span class="sxs-lookup"><span data-stu-id="fe7dd-151">956</span></span>                      |
| <span data-ttu-id="fe7dd-152">Şubat</span><span class="sxs-lookup"><span data-stu-id="fe7dd-152">February</span></span> | <span data-ttu-id="fe7dd-153">1.176</span><span class="sxs-lookup"><span data-stu-id="fe7dd-153">1,176</span></span>                    |
| <span data-ttu-id="fe7dd-154">Mart</span><span class="sxs-lookup"><span data-stu-id="fe7dd-154">March</span></span>    | <span data-ttu-id="fe7dd-155">451</span><span class="sxs-lookup"><span data-stu-id="fe7dd-155">451</span></span>                      |
| <span data-ttu-id="fe7dd-156">Nisan</span><span class="sxs-lookup"><span data-stu-id="fe7dd-156">April</span></span>    | <span data-ttu-id="fe7dd-157">119</span><span class="sxs-lookup"><span data-stu-id="fe7dd-157">119</span></span>                      |

<span data-ttu-id="fe7dd-158">Aylık 1.000 parçalık aynı talep tahminini kullanıyorsanız, aşağıdaki gereksinim miktarları ana planlamaya aktarılır.</span><span class="sxs-lookup"><span data-stu-id="fe7dd-158">If you use the same demand forecast of 1,000 pieces per month, the following requirement quantities are transferred to the master plan.</span></span>

| <span data-ttu-id="fe7dd-159">Ay</span><span class="sxs-lookup"><span data-stu-id="fe7dd-159">Month</span></span>                | <span data-ttu-id="fe7dd-160">Gerekli parça sayısı</span><span class="sxs-lookup"><span data-stu-id="fe7dd-160">Number of pieces required</span></span> |
|----------------------|---------------------------|
| <span data-ttu-id="fe7dd-161">Ocak</span><span class="sxs-lookup"><span data-stu-id="fe7dd-161">January</span></span>              | <span data-ttu-id="fe7dd-162">44</span><span class="sxs-lookup"><span data-stu-id="fe7dd-162">44</span></span>                        |
| <span data-ttu-id="fe7dd-163">Şubat</span><span class="sxs-lookup"><span data-stu-id="fe7dd-163">February</span></span>             | <span data-ttu-id="fe7dd-164">0</span><span class="sxs-lookup"><span data-stu-id="fe7dd-164">0</span></span>                         |
| <span data-ttu-id="fe7dd-165">Mart</span><span class="sxs-lookup"><span data-stu-id="fe7dd-165">March</span></span>                | <span data-ttu-id="fe7dd-166">549</span><span class="sxs-lookup"><span data-stu-id="fe7dd-166">549</span></span>                       |
| <span data-ttu-id="fe7dd-167">Nisan</span><span class="sxs-lookup"><span data-stu-id="fe7dd-167">April</span></span>                | <span data-ttu-id="fe7dd-168">881</span><span class="sxs-lookup"><span data-stu-id="fe7dd-168">881</span></span>                       |
| <span data-ttu-id="fe7dd-169">Mayıs - Aralık arası</span><span class="sxs-lookup"><span data-stu-id="fe7dd-169">May through December</span></span> | <span data-ttu-id="fe7dd-170">1.000</span><span class="sxs-lookup"><span data-stu-id="fe7dd-170">1,000</span></span>                     |

## <a name="example-3-transactions--dynamic-period-forecast-reduction-principle"></a><span data-ttu-id="fe7dd-171">Örnek 3: Hareketler dinamik dönem tahmini azaltma ilkesi</span><span class="sxs-lookup"><span data-stu-id="fe7dd-171">Example 3: Transactions  dynamic period forecast reduction principle</span></span>
<span data-ttu-id="fe7dd-172">Çoğu durumda, hareketlerin haftalık, aylık ve benzeri tahmin dönemlerinde talep tahminini azaltabilmesi için sistemler ayarlanır.</span><span class="sxs-lookup"><span data-stu-id="fe7dd-172">In most cases, systems are set up so that transactions reduce demand forecast within specific forecast periods: weeks, months, and so on.</span></span> <span data-ttu-id="fe7dd-173">Bu dönemler azaltma anahtarında tanımlanır.</span><span class="sxs-lookup"><span data-stu-id="fe7dd-173">These periods are defined in the reduction key.</span></span> <span data-ttu-id="fe7dd-174">Ancak, iki tahmin satırı arasındaki süre bir dönemi*gösterebilir*.</span><span class="sxs-lookup"><span data-stu-id="fe7dd-174">However, the time between two demand forecast lines can also *imply* a period.</span></span>

1. <span data-ttu-id="fe7dd-175">Aşağıdaki tarihler ve miktarlar için bir talep tahmin oluşturun.</span><span class="sxs-lookup"><span data-stu-id="fe7dd-175">Create a demand forecast for the following dates and quantities.</span></span>

   | <span data-ttu-id="fe7dd-176">Tarih</span><span class="sxs-lookup"><span data-stu-id="fe7dd-176">Date</span></span>       | <span data-ttu-id="fe7dd-177">Talep tahmini</span><span class="sxs-lookup"><span data-stu-id="fe7dd-177">Demand forecast</span></span> |
   |------------|-----------------|
   | <span data-ttu-id="fe7dd-178">1 Ocak</span><span class="sxs-lookup"><span data-stu-id="fe7dd-178">January 1</span></span>  | <span data-ttu-id="fe7dd-179">1.000</span><span class="sxs-lookup"><span data-stu-id="fe7dd-179">1,000</span></span>           |
   | <span data-ttu-id="fe7dd-180">5 Ocak</span><span class="sxs-lookup"><span data-stu-id="fe7dd-180">January 5</span></span>  | <span data-ttu-id="fe7dd-181">500</span><span class="sxs-lookup"><span data-stu-id="fe7dd-181">500</span></span>             |
   | <span data-ttu-id="fe7dd-182">12 Ocak</span><span class="sxs-lookup"><span data-stu-id="fe7dd-182">January 12</span></span> | <span data-ttu-id="fe7dd-183">1.000</span><span class="sxs-lookup"><span data-stu-id="fe7dd-183">1,000</span></span>           |

   <span data-ttu-id="fe7dd-184">Bu tahminde, tahmin tarihleri arasında açıkça bir dönem yoktur: birinci ve ikinci tarihler arasında dört günlük bir süre; ikinci ve üçüncü tarihler arasında yedi günlük bir süre vardır.</span><span class="sxs-lookup"><span data-stu-id="fe7dd-184">In this forecast, there isn't a clear period between the forecast dates: between the first and second dates there is a four-day span, and between the second and third dates there is a seven-day span.</span></span> <span data-ttu-id="fe7dd-185">Bu süre çeşitliliği dinamik periyotları oluşturur.</span><span class="sxs-lookup"><span data-stu-id="fe7dd-185">These various spans are the dynamic periods.</span></span>
2. <span data-ttu-id="fe7dd-186">Aşağıdaki satış siparişi satırlarını oluşturun.</span><span class="sxs-lookup"><span data-stu-id="fe7dd-186">Create sales order lines as follows.</span></span>
   | <span data-ttu-id="fe7dd-187">Tarih</span><span class="sxs-lookup"><span data-stu-id="fe7dd-187">Date</span></span>                             | <span data-ttu-id="fe7dd-188">Satış siparişi miktarı</span><span class="sxs-lookup"><span data-stu-id="fe7dd-188">Sales order quantity</span></span> |
   |----------------------------------|----------------------|
   | <span data-ttu-id="fe7dd-189">Önceki yılın 15 Aralık tarihi</span><span class="sxs-lookup"><span data-stu-id="fe7dd-189">December 15 in the previous year</span></span> | <span data-ttu-id="fe7dd-190">500</span><span class="sxs-lookup"><span data-stu-id="fe7dd-190">500</span></span>                  |
   | <span data-ttu-id="fe7dd-191">3 Ocak</span><span class="sxs-lookup"><span data-stu-id="fe7dd-191">January 3</span></span>                        | <span data-ttu-id="fe7dd-192">100</span><span class="sxs-lookup"><span data-stu-id="fe7dd-192">100</span></span>                  |
   | <span data-ttu-id="fe7dd-193">10 Ocak</span><span class="sxs-lookup"><span data-stu-id="fe7dd-193">January 10</span></span>                       | <span data-ttu-id="fe7dd-194">200</span><span class="sxs-lookup"><span data-stu-id="fe7dd-194">200</span></span>                  |

<span data-ttu-id="fe7dd-195">Tahmin aşağıdaki gibi azaltılır:</span><span class="sxs-lookup"><span data-stu-id="fe7dd-195">The forecast will be reduced as follows:</span></span>

-   <span data-ttu-id="fe7dd-196">İlk satış siparişi dönem içinde değildir, böylece hiçbir tahmini azaltmaz.</span><span class="sxs-lookup"><span data-stu-id="fe7dd-196">The first sales order isn't within any period, so it won't reduce any forecast.</span></span>
-   <span data-ttu-id="fe7dd-197">İkinci satış siparişi 1 Ocak - 5 Ocak aralığındadır, böylece 1 Ocak için tahmini 100 azaltır.</span><span class="sxs-lookup"><span data-stu-id="fe7dd-197">The second sales order is between January 1 and January 5, so it will reduce the forecast for January 1 by 100.</span></span>
-   <span data-ttu-id="fe7dd-198">Üçüncü satış siparişi 5 Ocak - 12 Ocak aralığındadır, böylece 5 Ocak için tahmini 200 azaltır.</span><span class="sxs-lookup"><span data-stu-id="fe7dd-198">The third sales order is between January 5 and January 12, so it will reduce the forecast for January 5 by 200.</span></span>

<span data-ttu-id="fe7dd-199">Aşağıdaki planlı sipariş tahmini karşılamak için oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="fe7dd-199">The following planned order will be created to fulfill the forecast.</span></span>

| <span data-ttu-id="fe7dd-200">Talep tahmini tarihi</span><span class="sxs-lookup"><span data-stu-id="fe7dd-200">Demand forecast date</span></span> | <span data-ttu-id="fe7dd-201">Azaltılmış miktar</span><span class="sxs-lookup"><span data-stu-id="fe7dd-201">Reduced quantity</span></span> |
|----------------------|------------------|
| <span data-ttu-id="fe7dd-202">1 Ocak</span><span class="sxs-lookup"><span data-stu-id="fe7dd-202">January 1</span></span>            | <span data-ttu-id="fe7dd-203">900</span><span class="sxs-lookup"><span data-stu-id="fe7dd-203">900</span></span>              |
| <span data-ttu-id="fe7dd-204">5 Ocak</span><span class="sxs-lookup"><span data-stu-id="fe7dd-204">January 5</span></span>            | <span data-ttu-id="fe7dd-205">300</span><span class="sxs-lookup"><span data-stu-id="fe7dd-205">300</span></span>              |
| <span data-ttu-id="fe7dd-206">12 Ocak</span><span class="sxs-lookup"><span data-stu-id="fe7dd-206">January 12</span></span>           | <span data-ttu-id="fe7dd-207">1.000</span><span class="sxs-lookup"><span data-stu-id="fe7dd-207">1,000</span></span>            |

<span data-ttu-id="fe7dd-208">**Hareketler - dinamik dönem** azaltmasına ilişkin bir örnek şöyledir:</span><span class="sxs-lookup"><span data-stu-id="fe7dd-208">Here is a summary of **Transactions - dynamic period** reduction:</span></span>

-   <span data-ttu-id="fe7dd-209">Tahmin gereksinimleri, dinamik dönem sırasında gerçekleşen fiili sipariş hareketleriyle azaltılır.</span><span class="sxs-lookup"><span data-stu-id="fe7dd-209">Forecast requirements are reduced by the actual order transactions that occur during the dynamic period.</span></span> <span data-ttu-id="fe7dd-210">Dinamik dönem, geçerli tahmin tarihlerini kapsar ve bir sonraki tahmin başlangıcında sona erer.</span><span class="sxs-lookup"><span data-stu-id="fe7dd-210">The dynamic period covers the current forecast dates and ends at the start of the next forecast.</span></span>
-   <span data-ttu-id="fe7dd-211">Bu yöntem bir azaltma anahtarı kullanmaz.</span><span class="sxs-lookup"><span data-stu-id="fe7dd-211">This method doesn't use or require a reduction key.</span></span>
-   <span data-ttu-id="fe7dd-212">Bu seçenek kullanıldığında, aşağıdaki davranış ortaya çıkar:</span><span class="sxs-lookup"><span data-stu-id="fe7dd-212">When this option is used, the following behavior occurs:</span></span>
    -   <span data-ttu-id="fe7dd-213">Tahmin tümüyle azaltıldıysa, geçerli tahminin tahmin gereksinimleri 0 (sıfır) olur.</span><span class="sxs-lookup"><span data-stu-id="fe7dd-213">If the forecast is reduced completely, the forecast requirements for the current forecast become 0 (zero).</span></span>
    -   <span data-ttu-id="fe7dd-214">Gelecekte başka bir tahmin yoksa, girilen son tahmindeki tahmin gereksinimleri azaltılır.</span><span class="sxs-lookup"><span data-stu-id="fe7dd-214">If there is no future forecast, forecast requirements from the last forecast that was entered are reduced.</span></span>
    -   <span data-ttu-id="fe7dd-215">Zaman dilimleri, tahmin azaltma hesaplamasına eklenir.</span><span class="sxs-lookup"><span data-stu-id="fe7dd-215">Time fences are included in the forecast reduction calculation.</span></span>
    -   <span data-ttu-id="fe7dd-216">Artı günler, tahmin azaltma hesaplamasına eklenir.</span><span class="sxs-lookup"><span data-stu-id="fe7dd-216">Positive days are included in the forecast reduction calculation.</span></span>
    -   <span data-ttu-id="fe7dd-217">Fiili sipariş hareketlerinin tahmin gereksinimlerini aşması durumunda, kalan hareketler sonraki tahmin dönemine iletilmez.</span><span class="sxs-lookup"><span data-stu-id="fe7dd-217">If actual order transactions exceed the forecasted requirements, the remaining transactions aren't forwarded to the next forecast period.</span></span>


<a name="additional-resources"></a><span data-ttu-id="fe7dd-218">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="fe7dd-218">Additional resources</span></span>
--------

[<span data-ttu-id="fe7dd-219">Master planlar</span><span class="sxs-lookup"><span data-stu-id="fe7dd-219">Master plans</span></span>](master-plans.md)




