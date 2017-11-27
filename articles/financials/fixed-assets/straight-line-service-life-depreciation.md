---
title: "Sabit servis ömrü amortismanı"
description: "Bu makalede amortismanın Düz çigi hizmet ömrü yöntemine genel bir bakış sunulmuştur."
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: AssetDepreciationProfile
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 3341
ms.assetid: ae5ceaeb-aeb7-45cd-b835-23cf9c5cf95a
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: bb5715855c7e240cddf4fd264a4b26ca09a2f6c4
ms.contentlocale: tr-tr
ms.lasthandoff: 11/03/2017

---

# <a name="straight-line-service-life-depreciation"></a><span data-ttu-id="c0bb0-103">Sabit servis ömrü amortismanı</span><span class="sxs-lookup"><span data-stu-id="c0bb0-103">Straight line service life depreciation</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="c0bb0-104">Bu makalede amortismanın Düz çigi hizmet ömrü yöntemine genel bir bakış sunulmuştur.</span><span class="sxs-lookup"><span data-stu-id="c0bb0-104">This article gives an overview of the Straight line service life method of depreciation.</span></span>

<span data-ttu-id="c0bb0-105">Bir sabit kıymet amortisman profili ayarladığınızda ve Amortisman profilleri sayfasında Yöntem alanında Sabit servis ömrü öğesini seçtiğinizde bu amortisman profilinin atanmış olduğu kıymetlerin amortismanı kıymetin toplam servis ömrüne dayalı olarak hesaplanır.</span><span class="sxs-lookup"><span data-stu-id="c0bb0-105">When you set up a fixed asset depreciation profile and select Straight line service life in the Method field in the Depreciation profiles page, the assets that have this depreciation profile assigned to them are depreciated based on the total service life of the asset.</span></span> <span data-ttu-id="c0bb0-106">Bu, genellikle her amortisman dönemindeki aynı amortisman tutarı olur.</span><span class="sxs-lookup"><span data-stu-id="c0bb0-106">This generally is the same depreciation amount in each depreciation period.</span></span> 

<span data-ttu-id="c0bb0-107">Kalan sabit amortisman servis ömrüne ve sabit amortisman servis ömrüne göre hesaplanan amortisman tutarı arasındaki fark, sabit kıymet için deftere nakledilen bir düzeltme olduğunda ortaya çıkar .</span><span class="sxs-lookup"><span data-stu-id="c0bb0-107">The difference in the depreciation amount that is calculated between straight line service life remaining and straight line service life is when there is an adjustment posted to the asset.</span></span> 

<span data-ttu-id="c0bb0-108">Sabit servis ömrü amortismanını ayarlamak için, Amortisman profilleri sayfasında Amortisman yılı ve Dönem sıklığı alanlarındaki seçenekleri de belirlemeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="c0bb0-108">To set up straight line service life depreciation, you must also select options in the Depreciation year and Period frequency fields in the Depreciation profiles page.</span></span>

## <a name="select-a-depreciation-year"></a><span data-ttu-id="c0bb0-109">Amortisman yılının seçilmesi</span><span class="sxs-lookup"><span data-stu-id="c0bb0-109">Select a depreciation year</span></span>
<span data-ttu-id="c0bb0-110">Amortisman profilleri sayasındaki Amortisman yılı alanından Takvim Yılı veya Mali Yıl seçimi yapabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="c0bb0-110">You can select either Calendar or Fiscal in the Depreciation year field in the Depreciation profiles page.</span></span> <span data-ttu-id="c0bb0-111">Seçiminiz, Dönem sıklığı alanında bulunan seçenekleri tanımlar.</span><span class="sxs-lookup"><span data-stu-id="c0bb0-111">The selection defines the options that are available in the Period frequency field.</span></span> <span data-ttu-id="c0bb0-112">Varsayılan seçenek Takvim yılıdır.</span><span class="sxs-lookup"><span data-stu-id="c0bb0-112">The default option is Calendar.</span></span>

### <a name="calendar"></a><span data-ttu-id="c0bb0-113">Takvim</span><span class="sxs-lookup"><span data-stu-id="c0bb0-113">Calendar</span></span>

<span data-ttu-id="c0bb0-114">Takvim seçersiniz, mali dönem takvimini farklı şekilde tanımlamış olsanız bile, bir yılın 1 Ocak ile 31 Aralık arasındaki süre olduğu varsayılacaktır.</span><span class="sxs-lookup"><span data-stu-id="c0bb0-114">If you select Calendar, a year of January 1 to December 31 is assumed, even if you have defined the fiscal calendar differently.</span></span> 

<span data-ttu-id="c0bb0-115">Takvim seçeneği tipik olarak her yıl 1 Ocak itibariyle net defter değerinden hurda değeri çıkarılarak hesaplanan amortisman temelini günceller.</span><span class="sxs-lookup"><span data-stu-id="c0bb0-115">The Calendar option updates the depreciation base, which is typically the net book value minus the salvage value, on January 1 of each year.</span></span> <span data-ttu-id="c0bb0-116">Bu konunun devamındaki örneklerde, amortisman tabanı hesaplamalar sütunundaki yer alan ilk ifadedeki pay olur.</span><span class="sxs-lookup"><span data-stu-id="c0bb0-116">In the examples later in this topic, the depreciation base is the numerator in the first expression in the calculations column.</span></span> 

<span data-ttu-id="c0bb0-117">Takvim seçimini yaparsanız, amortisman artışı nakil tarihleri ve takvim yılı genelindeki tutarları belirleyen Dönem sıklığı alanında şu seçenekler mevcut olacaktır:</span><span class="sxs-lookup"><span data-stu-id="c0bb0-117">If you select Calendar, the following options are available in the Period frequency field, which defines the depreciation accrual posting dates and amounts throughout the calendar year:</span></span>
-   <span data-ttu-id="c0bb0-118">Yıllık 31 Aralık'ta bir tutarı nakleder.</span><span class="sxs-lookup"><span data-stu-id="c0bb0-118">Yearly posts an amount on December 31.</span></span>
-   <span data-ttu-id="c0bb0-119">Aylık seçeneği her takvim ayının sonunda bir aylık tutarı nakleder.</span><span class="sxs-lookup"><span data-stu-id="c0bb0-119">Monthly posts a monthly amount at the end of each calendar month.</span></span>
-   <span data-ttu-id="c0bb0-120">Üç aylık seçeneği, üç aylık takvim döneminin sonunda (31 Mart, 30 Haziran, 30 Eylül ve 31 Aralık) bir üç aylık tutar nakleder.</span><span class="sxs-lookup"><span data-stu-id="c0bb0-120">Quarterly posts a quarterly amount at the end of each calendar quarter (March 31, June 30, September 30, and December 31).</span></span>
-   <span data-ttu-id="c0bb0-121">Altı Aylık seçeneği, altı aylık takvim döneminde ( 30 Haziran ve 31 Aralık) bir altı aylık tutar nakleder.</span><span class="sxs-lookup"><span data-stu-id="c0bb0-121">Half-Yearly posts a half-yearly amount at the end of each calendar half year (June 30 and December 31).</span></span>
-   <span data-ttu-id="c0bb0-122">Günlük seçeneği her gün için bir işlem kullanarak günlük amortisman yöntemi için amortisman tutarını nakleder.</span><span class="sxs-lookup"><span data-stu-id="c0bb0-122">Daily posts the depreciation amount for the daily depreciation method using one transaction for each day.</span></span>

<span data-ttu-id="c0bb0-123">Örneğin, Yıllık seçeneğini belirlerseniz yıllık amortisman her yılın 31 Aralık tarihinde yalnızca bir defa nakledilir.</span><span class="sxs-lookup"><span data-stu-id="c0bb0-123">For example, if you select Yearly, the yearly depreciation is posted only one time, on December 31 of each year.</span></span> <span data-ttu-id="c0bb0-124">Aylık seçeneğini belirlerseniz aylık amortisman her ayı, yıllık amortisman tutarının 1/12'si oranında nakleder</span><span class="sxs-lookup"><span data-stu-id="c0bb0-124">If you select Monthly, the monthly depreciation is posted each month as 1/12 of the yearly depreciation amount.</span></span>

### <a name="fiscal"></a><span data-ttu-id="c0bb0-125">Mali</span><span class="sxs-lookup"><span data-stu-id="c0bb0-125">Fiscal</span></span>

<span data-ttu-id="c0bb0-126">Amortisman yılı alanında Mali yıl seçimini yaparsanız, sabit servis ömrü amortismanı kullanılır.</span><span class="sxs-lookup"><span data-stu-id="c0bb0-126">If you select Fiscal in the Depreciation year field, the straight line service life depreciation is used.</span></span> <span data-ttu-id="c0bb0-127">Defterin mali takvimine ya da Genel muhasebe sayfasında seçilen mali takvime göre tanımlanan mali yıl temel alınarak hesaplanır.</span><span class="sxs-lookup"><span data-stu-id="c0bb0-127">It is calculated based on the fiscal year, which is defined by the fiscal calendar that is specified for the book, or by the fiscal calendar that is selected in the Ledger page.</span></span> <span data-ttu-id="c0bb0-128">Mali takvimler, Mali takvimler sayfasında ayarlanır.</span><span class="sxs-lookup"><span data-stu-id="c0bb0-128">Fiscal calendars are set up in the Fiscal calendars page.</span></span>

<span data-ttu-id="c0bb0-129">Örneğin, 1 Temmuz ile 30 Haziran arasındaki mali yıl için amortisman hesaplaması 1 Temmuz'da başlar.</span><span class="sxs-lookup"><span data-stu-id="c0bb0-129">For example, for fiscal year July 1 through June 30, the depreciation calculation starts on July 1.</span></span> <span data-ttu-id="c0bb0-130">Mali yıl 12 aydan daha uzun veya daha kısa olabilir.</span><span class="sxs-lookup"><span data-stu-id="c0bb0-130">The fiscal year can be longer or shorter than 12 months.</span></span> <span data-ttu-id="c0bb0-131">Amortisman her mali dönem için otomatik olarak ayarlanır.</span><span class="sxs-lookup"><span data-stu-id="c0bb0-131">The depreciation automatically is adjusted for each fiscal period.</span></span> <span data-ttu-id="c0bb0-132">Bir sonraki mali yılın uzunluğu, Mali takvimler formunda yeni bir mali yıl oluşturduğunuzda belirlenen mali dönemlere dayalı olacaktır.</span><span class="sxs-lookup"><span data-stu-id="c0bb0-132">The length of the next fiscal year is based on the fiscal periods that you set up when you create a new fiscal year in the Fiscal calendars form.</span></span> 

<span data-ttu-id="c0bb0-133">Mali yıl seçimini yaparsanız Dönem sıklığı alanında şu seçenekler kullanılabilir:</span><span class="sxs-lookup"><span data-stu-id="c0bb0-133">If you select Fiscal, the following options are available in the Period frequency field:</span></span>
-   <span data-ttu-id="c0bb0-134">Yıllık, mali yıl için hesaplanan toplam amortisman tutarını tek tutar olarak, mali yılın son gününde nakleder.</span><span class="sxs-lookup"><span data-stu-id="c0bb0-134">Yearly posts the total amount of the depreciation that is calculated for the fiscal year as one amount on the last day of the fiscal year.</span></span>
-   <span data-ttu-id="c0bb0-135">Mali dönem, mali takvimin Mali takvimler formunda tanımlanan dönemlere tahakkuk edilen mali yıla ilişkin toplam amortisman tutarını hesaplar.</span><span class="sxs-lookup"><span data-stu-id="c0bb0-135">Fiscal period calculates the total amount of the depreciation for the fiscal year, which is accrued into the periods that are defined in the Fiscal calendars form for the fiscal calendar.</span></span>

## <a name="example-straight-line-depreciation-of-an-unchanged-fixed-asset"></a><span data-ttu-id="c0bb0-136">Örnek: Değişmeyen bir sabit kıymet için sabit amortisman</span><span class="sxs-lookup"><span data-stu-id="c0bb0-136">Example: Straight line depreciation of an unchanged fixed asset</span></span>
<span data-ttu-id="c0bb0-137">Bir sabit kıymetin aşağıdaki özelliklere sahip olduğunu düşünelim.</span><span class="sxs-lookup"><span data-stu-id="c0bb0-137">Suppose that a fixed asset has the following characteristics.</span></span>

|                     |        |
|---------------------|--------|
| <span data-ttu-id="c0bb0-138">Alım maliyeti</span><span class="sxs-lookup"><span data-stu-id="c0bb0-138">Acquisition cost</span></span>    | <span data-ttu-id="c0bb0-139">11.000</span><span class="sxs-lookup"><span data-stu-id="c0bb0-139">11,000</span></span> |
| <span data-ttu-id="c0bb0-140">Hurda değeri</span><span class="sxs-lookup"><span data-stu-id="c0bb0-140">Salvage value</span></span>       | <span data-ttu-id="c0bb0-141">1.000</span><span class="sxs-lookup"><span data-stu-id="c0bb0-141">1,000</span></span>  |
| <span data-ttu-id="c0bb0-142">Amortisman tabanı</span><span class="sxs-lookup"><span data-stu-id="c0bb0-142">Depreciation base</span></span>   | <span data-ttu-id="c0bb0-143">10.000</span><span class="sxs-lookup"><span data-stu-id="c0bb0-143">10,000</span></span> |
| <span data-ttu-id="c0bb0-144">Servis ömrü yıl sayısı</span><span class="sxs-lookup"><span data-stu-id="c0bb0-144">Service life years</span></span>  | <span data-ttu-id="c0bb0-145">5</span><span class="sxs-lookup"><span data-stu-id="c0bb0-145">5</span></span>      |
| <span data-ttu-id="c0bb0-146">Yıllık amortisman</span><span class="sxs-lookup"><span data-stu-id="c0bb0-146">Yearly depreciation</span></span> | <span data-ttu-id="c0bb0-147">2.000</span><span class="sxs-lookup"><span data-stu-id="c0bb0-147">2,000</span></span>  |

<span data-ttu-id="c0bb0-148">Her yıl aynı amortisman tutarını elde edersiniz.</span><span class="sxs-lookup"><span data-stu-id="c0bb0-148">You get the same depreciation amount each year.</span></span> <span data-ttu-id="c0bb0-149">(Alım maliyeti - Hurda değeri) / Servis ömrü yıl sayısı</span><span class="sxs-lookup"><span data-stu-id="c0bb0-149">(Acquisition cost - Salvage value) / Service life years</span></span>

| <span data-ttu-id="c0bb0-150">Dönem</span><span class="sxs-lookup"><span data-stu-id="c0bb0-150">Period</span></span> | <span data-ttu-id="c0bb0-151">Yıllık amortisman miktarı hesaplaması</span><span class="sxs-lookup"><span data-stu-id="c0bb0-151">Calculation of yearly depreciation amount</span></span> | <span data-ttu-id="c0bb0-152">Yılın sonundaki net defter değeri</span><span class="sxs-lookup"><span data-stu-id="c0bb0-152">Net book value at the end of the year</span></span> |
|--------|-------------------------------------------|---------------------------------------|
| <span data-ttu-id="c0bb0-153">Yıl 1</span><span class="sxs-lookup"><span data-stu-id="c0bb0-153">Year 1</span></span> | <span data-ttu-id="c0bb0-154">(11.000 - 1.000) / 5 = 2.000</span><span class="sxs-lookup"><span data-stu-id="c0bb0-154">(11,000 - 1,000) / 5 = 2,000</span></span>              | <span data-ttu-id="c0bb0-155">9.000</span><span class="sxs-lookup"><span data-stu-id="c0bb0-155">9,000</span></span>                                 |
| <span data-ttu-id="c0bb0-156">Yıl 2</span><span class="sxs-lookup"><span data-stu-id="c0bb0-156">Year 2</span></span> | <span data-ttu-id="c0bb0-157">(11.000 - 1.000) / 5 = 2.000</span><span class="sxs-lookup"><span data-stu-id="c0bb0-157">(11,000 - 1,000) / 5 = 2,000</span></span>              | <span data-ttu-id="c0bb0-158">7.000</span><span class="sxs-lookup"><span data-stu-id="c0bb0-158">7,000</span></span>                                 |
| <span data-ttu-id="c0bb0-159">Yıl 3</span><span class="sxs-lookup"><span data-stu-id="c0bb0-159">Year 3</span></span> | <span data-ttu-id="c0bb0-160">(11.000 - 1.000) / 5 = 2.000</span><span class="sxs-lookup"><span data-stu-id="c0bb0-160">(11,000 - 1,000) / 5 = 2,000</span></span>              | <span data-ttu-id="c0bb0-161">5.000</span><span class="sxs-lookup"><span data-stu-id="c0bb0-161">5,000</span></span>                                 |
| <span data-ttu-id="c0bb0-162">Yıl 4</span><span class="sxs-lookup"><span data-stu-id="c0bb0-162">Year 4</span></span> | <span data-ttu-id="c0bb0-163">(11.000 - 1.000) / 5 = 2.000</span><span class="sxs-lookup"><span data-stu-id="c0bb0-163">(11,000 - 1,000) / 5 = 2,000</span></span>              | <span data-ttu-id="c0bb0-164">3.000</span><span class="sxs-lookup"><span data-stu-id="c0bb0-164">3,000</span></span>                                 |
| <span data-ttu-id="c0bb0-165">Yıl 5</span><span class="sxs-lookup"><span data-stu-id="c0bb0-165">Year 5</span></span> | <span data-ttu-id="c0bb0-166">(11.000 - 1.000) / 5 = 2.000</span><span class="sxs-lookup"><span data-stu-id="c0bb0-166">(11,000 - 1,000) / 5 = 2,000</span></span>              | <span data-ttu-id="c0bb0-167">1.000</span><span class="sxs-lookup"><span data-stu-id="c0bb0-167">1,000</span></span>                                 |

## <a name="example-straight-line-depreciation-of-a-modified-fixed-asset"></a><span data-ttu-id="c0bb0-168"> Örnek: Değiştirilmiş bir sabit kıymet için sabit amortisman</span><span class="sxs-lookup"><span data-stu-id="c0bb0-168">Example: Straight line depreciation of a modified fixed asset</span></span>

<span data-ttu-id="c0bb0-169">2. yılda aynı sabit kıymete 4.000 tutarında bir alım düzeltmesi eklediğinizi varsayalım.</span><span class="sxs-lookup"><span data-stu-id="c0bb0-169">Suppose that you add an acquisition adjustment of 4,000 in year 2 to the same fixed asset.</span></span> 

<span data-ttu-id="c0bb0-170">Alım düzeltmesinin servis ömrü, sabit kıymetinkiyle aynıdır ve alım anında başlar.</span><span class="sxs-lookup"><span data-stu-id="c0bb0-170">The service life of the acquisition adjustment is the same as that of the fixed asset and starts at the time of its acquisition.</span></span> <span data-ttu-id="c0bb0-171">5.yılın sonunda bir net defter değeri varlığını sürdürür; bu, alım düzeltmesinin net defter değerine karşılık gelir.</span><span class="sxs-lookup"><span data-stu-id="c0bb0-171">A net book value remains at the end of year 5, corresponding to the net book value of the acquisition adjustment.</span></span> <span data-ttu-id="c0bb0-172">Döneme göre amortisman aşağıdaki tabloda gösterildiği şekilde hesaplanır.</span><span class="sxs-lookup"><span data-stu-id="c0bb0-172">The depreciation by period is calculated as shown in the following table.</span></span>

| <span data-ttu-id="c0bb0-173">Dönem</span><span class="sxs-lookup"><span data-stu-id="c0bb0-173">Period</span></span> | <span data-ttu-id="c0bb0-174">Yıllık amortisman miktarı hesaplaması</span><span class="sxs-lookup"><span data-stu-id="c0bb0-174">Calculation of yearly depreciation amount</span></span> | <span data-ttu-id="c0bb0-175">Yıl sonunda net defter değeri</span><span class="sxs-lookup"><span data-stu-id="c0bb0-175">Net book value at the end of the year</span></span> |
|--------|-------------------------------------------|---------------------------------------|
| <span data-ttu-id="c0bb0-176">Yıl 1</span><span class="sxs-lookup"><span data-stu-id="c0bb0-176">Year 1</span></span> | <span data-ttu-id="c0bb0-177">10.000 / 5 = 2.000</span><span class="sxs-lookup"><span data-stu-id="c0bb0-177">10,000 / 5 = 2,000</span></span>                        | <span data-ttu-id="c0bb0-178">11.000 - 2.000 = 9.000</span><span class="sxs-lookup"><span data-stu-id="c0bb0-178">11,000 - 2,000 = 9,000</span></span>                |
| <span data-ttu-id="c0bb0-179">2. yıl</span><span class="sxs-lookup"><span data-stu-id="c0bb0-179">Year 2</span></span> | <span data-ttu-id="c0bb0-180">4.000 (alım düzeltmeleri)</span><span class="sxs-lookup"><span data-stu-id="c0bb0-180">4,000 (acquisition adjustment)</span></span>            | <span data-ttu-id="c0bb0-181">9.000 + 4.000 =13.000</span><span class="sxs-lookup"><span data-stu-id="c0bb0-181">9,000 + 4,000 =13,000</span></span>                 |
| <span data-ttu-id="c0bb0-182">2. yıl</span><span class="sxs-lookup"><span data-stu-id="c0bb0-182">Year 2</span></span> | <span data-ttu-id="c0bb0-183">14.000 / 5 = 2.800</span><span class="sxs-lookup"><span data-stu-id="c0bb0-183">14,000 / 5 = 2,800</span></span>                        | <span data-ttu-id="c0bb0-184">13.000 - 2.800 = 10.200</span><span class="sxs-lookup"><span data-stu-id="c0bb0-184">13,000 - 2,800 = 10,200</span></span>               |
| <span data-ttu-id="c0bb0-185">3. yıl</span><span class="sxs-lookup"><span data-stu-id="c0bb0-185">Year 3</span></span> | <span data-ttu-id="c0bb0-186">14.000 / 5 = 2.800</span><span class="sxs-lookup"><span data-stu-id="c0bb0-186">14,000 / 5 = 2,800</span></span>                        | <span data-ttu-id="c0bb0-187">10.200 - 2.800 = 7.400</span><span class="sxs-lookup"><span data-stu-id="c0bb0-187">10,200 - 2,800 = 7,400</span></span>                |
| <span data-ttu-id="c0bb0-188">Yıl 4</span><span class="sxs-lookup"><span data-stu-id="c0bb0-188">Year 4</span></span> | <span data-ttu-id="c0bb0-189">14.000 / 5 = 2.800</span><span class="sxs-lookup"><span data-stu-id="c0bb0-189">14,000 / 5 = 2,800</span></span>                        | <span data-ttu-id="c0bb0-190">7.400 - 2.800 = 4.600</span><span class="sxs-lookup"><span data-stu-id="c0bb0-190">7,400 - 2,800 = 4,600</span></span>                 |
| <span data-ttu-id="c0bb0-191">Yıl 5</span><span class="sxs-lookup"><span data-stu-id="c0bb0-191">Year 5</span></span> | <span data-ttu-id="c0bb0-192">14.000 / 5 = 2.800</span><span class="sxs-lookup"><span data-stu-id="c0bb0-192">14,000 / 5 = 2,800</span></span>                        | <span data-ttu-id="c0bb0-193">4.600 - 2.800 = 1.800</span><span class="sxs-lookup"><span data-stu-id="c0bb0-193">4,600 - 2,800 = 1,800</span></span>                 |
| <span data-ttu-id="c0bb0-194">Yıl 6</span><span class="sxs-lookup"><span data-stu-id="c0bb0-194">Year 6</span></span> | <span data-ttu-id="c0bb0-195">Kalan 800\*</span><span class="sxs-lookup"><span data-stu-id="c0bb0-195">Remaining 800\*</span></span>                           | <span data-ttu-id="c0bb0-196">1.800 – 800 = 1.000</span><span class="sxs-lookup"><span data-stu-id="c0bb0-196">1,800 – 800 = 1,000</span></span>                   |

<span data-ttu-id="c0bb0-197">\*Kalan tutar amortisman miktarından az olduğundan, yalnızca kalan tutar eksi hurda değeri alınmıştır.</span><span class="sxs-lookup"><span data-stu-id="c0bb0-197">\*Because the remaining amount is less than the depreciation amount, only the remaining amount minus the salvage value is taken.</span></span>






