---
title: "Bakiyeli amortismanı azaltma"
description: "Bu makale, amortismanın Azalan bakiye yöntemi hakkında genel bir bakış sağlar."
author: twheeloc
manager: AnnBe
ms.date: 04/25/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: AssetDepreciationProfile
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 3281
ms.assetid: 1b86763d-d47c-4a6a-a9a6-d97a736750da
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 29bc8cd02d98479197d7e5f5664b9859c03893b3
ms.contentlocale: tr-tr
ms.lasthandoff: 11/03/2017

---

# <a name="reduce-balance-depreciation"></a><span data-ttu-id="bd00a-103">Bakiyeli amortismanı azaltma</span><span class="sxs-lookup"><span data-stu-id="bd00a-103">Reduce balance depreciation</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="bd00a-104">Bu makale, amortismanın Azalan bakiye yöntemi hakkında genel bir bakış sağlar.</span><span class="sxs-lookup"><span data-stu-id="bd00a-104">This article gives an overview of the Reducing balance method of depreciation.</span></span>

<span data-ttu-id="bd00a-105">Bir sabit kıymet amortisman profili oluşturduğunuzda ve Amortisman profilleri sayfasındaki Yöntem alanından Azalan bilançoyu seçtiğinizde, bu amortisman profilinin atandığı kıymetler her amortisman döneminde aynı yüzdeyle amortismana ayrılır.</span><span class="sxs-lookup"><span data-stu-id="bd00a-105">When you set up a fixed asset depreciation profile and select Reducing balance in the Method field in the Depreciation profiles page, the assets that have this depreciation profile assigned to them are depreciated by the same percentage in each depreciation period.</span></span>

<span data-ttu-id="bd00a-106">Azalan bilanço amortismanını ayarlamak için Amortisman profilleri sayfasındaki Genel FastTab altındaki alanlardan seçimler yapmalısınız.</span><span class="sxs-lookup"><span data-stu-id="bd00a-106">To set up reducing balance depreciation, you must also make selections in fields on the General FastTab of the Depreciation profiles page.</span></span> <span data-ttu-id="bd00a-107">Öncelikle, Amortisman yılı alanından bir yıl seçin.</span><span class="sxs-lookup"><span data-stu-id="bd00a-107">First, select a year in the Depreciation year field.</span></span> <span data-ttu-id="bd00a-108">Seçiminize bağlı olarak, aşağıdaki bölümlerde anlatıldığı şekilde, Dönem sıklığı alanında farklı seçenekler görüntülenecektir.</span><span class="sxs-lookup"><span data-stu-id="bd00a-108">Depending on the selection, different options appear in the Period frequency field, as explained in the following sections.</span></span> 

<span data-ttu-id="bd00a-109">Ayrıca, amortisman profili için Yüzde alanına bir değer girmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="bd00a-109">You must also enter a value in the Percentage field for the depreciation profile.</span></span> <span data-ttu-id="bd00a-110">Tam amortisman seçeneğini belirlerseniz kalan amortisman, son amortisman dönemini temel alınır ve bu, büyük bir tutar olabilir.</span><span class="sxs-lookup"><span data-stu-id="bd00a-110">If you select the Full depreciation option, the remaining depreciation basis is taken in the last depreciation period and could be a large amount.</span></span> <span data-ttu-id="bd00a-111">Bazı ülkeler/bölgeler doğrusal amortisman yöntemine geçiş özelliğini kullanmaz.</span><span class="sxs-lookup"><span data-stu-id="bd00a-111">Some countries/regions do not use a switchover to a straight line method.</span></span> <span data-ttu-id="bd00a-112">Alternatif amortisman yönteminin tutarı birincil amortisman profili tutarına eşit veya daha büyükse değişim gerçekleştirilir ve alınan amortisman tutarı alternatif yöntemin tutarı olarak kabul edilir.</span><span class="sxs-lookup"><span data-stu-id="bd00a-112">Switchover occurs when the alternative depreciation method amount is greater than or equal to the primary depreciation profile amount, and the depreciation amount taken is the alternative method amount.</span></span> 

<span data-ttu-id="bd00a-113">Bir kıymet yüzde hesaplamasına dayanarak tamamen amortismana ayrılmayacağından, bir kıymeti tamamen amortismana ayırmak için Tam amortisman seçeneği belirlemelisiniz.</span><span class="sxs-lookup"><span data-stu-id="bd00a-113">Because an asset will never be fully depreciated based on a percentage calculation, you must select the Full depreciation option to fully depreciate an asset.</span></span>

## <a name="select-a-depreciation-year"></a><span data-ttu-id="bd00a-114">Amortisman yılının seçilmesi</span><span class="sxs-lookup"><span data-stu-id="bd00a-114">Select a depreciation year</span></span>
<span data-ttu-id="bd00a-115">Amortisman profilleri sayasındaki Amortisman yılı alanından Takvim Yılı veya Mali Yıl seçimi yapabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="bd00a-115">You can select either Calendar or Fiscal in the Depreciation year field in the Depreciation profiles page.</span></span> <span data-ttu-id="bd00a-116">Seçiminiz, Dönem sıklığı alanında bulunan seçenekleri tanımlar.</span><span class="sxs-lookup"><span data-stu-id="bd00a-116">The selection defines the options that are available in the Period frequency field.</span></span> <span data-ttu-id="bd00a-117">Varsayılan seçenek Takvim yılıdır.</span><span class="sxs-lookup"><span data-stu-id="bd00a-117">The default option is Calendar.</span></span>

### <a name="calendar"></a><span data-ttu-id="bd00a-118">Takvim</span><span class="sxs-lookup"><span data-stu-id="bd00a-118">Calendar</span></span>

<span data-ttu-id="bd00a-119">Takvim seçeneği tipik olarak her yıl 1 Ocak itibariyle net defter değerinden hurda değeri çıkarılarak hesaplanan amortisman temelini günceller.</span><span class="sxs-lookup"><span data-stu-id="bd00a-119">The Calendar option updates the depreciation base, which is typically the net book value minus the scrap value, on January 1 of each year.</span></span> <span data-ttu-id="bd00a-120">Bu konunun ilerleyen bölümlerinde verilen azalan bilanço amortismanı örneğinde, amortismana esas olan değer, hesaplama sütunundaki ilk ifadenin payıdır.</span><span class="sxs-lookup"><span data-stu-id="bd00a-120">In the reducing balance depreciation example later in this topic, the depreciation base is the numerator in the first expression in the calculations column.</span></span> 

<span data-ttu-id="bd00a-121">Takvim seçimini yaparsanız, amortisman artışı nakil tarihleri ve takvim yılı genelindeki tutarları belirleyen Dönem sıklığı alanında şu seçenekler mevcut olacaktır:</span><span class="sxs-lookup"><span data-stu-id="bd00a-121">If you select Calendar, the following options are available in the Period frequency field, which defines the depreciation accrual posting dates and amounts throughout the calendar year:</span></span>

-   <span data-ttu-id="bd00a-122">31 Aralık tarihindeki yıllık nakiller.</span><span class="sxs-lookup"><span data-stu-id="bd00a-122">Yearly posts on December 31.</span></span>
-   <span data-ttu-id="bd00a-123">Aylık seçeneği her takvim ayının sonunda bir aylık tutarı nakleder.</span><span class="sxs-lookup"><span data-stu-id="bd00a-123">Monthly posts a monthly amount at the end of each calendar month.</span></span>
-   <span data-ttu-id="bd00a-124">Üç aylık seçeneği, üç aylık takvim döneminin sonunda (31 Mart, 30 Haziran, 30 Eylül ve 31 Aralık) bir üç aylık tutar nakleder.</span><span class="sxs-lookup"><span data-stu-id="bd00a-124">Quarterly posts a quarterly amount at the end of each calendar quarter (March 31, June 30, September 30, and December 31).</span></span>
-   <span data-ttu-id="bd00a-125">Altı Aylık seçeneği, altı aylık takvim döneminde ( 30 Haziran ve 31 Aralık) bir altı aylık tutar nakleder.</span><span class="sxs-lookup"><span data-stu-id="bd00a-125">Half-Yearly posts a half-yearly amount at the end of each calendar half-year (June 30 and December 31).</span></span>
-   <span data-ttu-id="bd00a-126">Günlük seçeneği her gün için bir işlem kullanarak günlük amortisman yöntemi için amortisman tutarını nakleder.</span><span class="sxs-lookup"><span data-stu-id="bd00a-126">Daily posts the depreciation amount for the daily depreciation method using one transaction for each day.</span></span>

<span data-ttu-id="bd00a-127">Örneğin, Yıllık seçeneğini belirlerseniz yıllık amortisman her yılın 31 Aralık tarihinde yalnızca bir defa nakledilir.</span><span class="sxs-lookup"><span data-stu-id="bd00a-127">For example, if you select Yearly, the yearly depreciation is posted only one time, on December 31 of each year.</span></span> <span data-ttu-id="bd00a-128">Aylık seçeneğini belirlerseniz aylık amortisman her ayı, yıllık amortisman tutarının 1/12'si oranında nakleder</span><span class="sxs-lookup"><span data-stu-id="bd00a-128">If you select Monthly, the monthly depreciation is posted each month as 1/12 of the yearly depreciation amount.</span></span>

### <a name="fiscal"></a><span data-ttu-id="bd00a-129">Mali</span><span class="sxs-lookup"><span data-stu-id="bd00a-129">Fiscal</span></span>

<span data-ttu-id="bd00a-130">Amortisman yılı alanından Mali Yıl seçimini yaparsanız düz çizgi amortisman yöntemi kullanılır.</span><span class="sxs-lookup"><span data-stu-id="bd00a-130">If you select Fiscal in the Depreciation year field, the straight line depreciation method is used.</span></span> <span data-ttu-id="bd00a-131">Defter sayfasında seçilen mali takvim için Mali takvimler sayfasında ayarlanan mali yıl temel alınarak hesaplanır.</span><span class="sxs-lookup"><span data-stu-id="bd00a-131">It is calculated based on the fiscal year, which is set up in the Fiscal calendars page for the fiscal calendar that is selected in the Ledger page.</span></span> <span data-ttu-id="bd00a-132">Örneğin, 1 Temmuz ile 30 Haziran arasındaki mali yıl için amortisman hesaplaması 1 Temmuz'da başlar.</span><span class="sxs-lookup"><span data-stu-id="bd00a-132">For example, for fiscal year July 1 through June 30, the depreciation calculation starts on July 1.</span></span> <span data-ttu-id="bd00a-133">Mali yıl 12 aydan daha uzun veya daha kısa olabilir.</span><span class="sxs-lookup"><span data-stu-id="bd00a-133">The fiscal year can be longer or shorter than 12 months.</span></span> <span data-ttu-id="bd00a-134">Amortisman her mali dönem için ayarlanır.</span><span class="sxs-lookup"><span data-stu-id="bd00a-134">The depreciation is adjusted for each fiscal period.</span></span> <span data-ttu-id="bd00a-135">Bir sonraki mali yılın uzunluğu, Mali takvimler sayfasında yeni bir mali yıl oluşturduğunuzda belirlenen mali dönemlere dayalı olacaktır.</span><span class="sxs-lookup"><span data-stu-id="bd00a-135">The length of the next fiscal year is based on the fiscal periods that you set up when you create a new fiscal year in the Fiscal calendars page.</span></span>


<span data-ttu-id="bd00a-136">Mali yıl seçimini yaparsanız Dönem sıklığı alanında şu seçenekler kullanılabilir:</span><span class="sxs-lookup"><span data-stu-id="bd00a-136">If you select Fiscal, the following options are available in the Period frequency field:</span></span>

-   <span data-ttu-id="bd00a-137">Yıllık seçeneği, mali yılın son gününde mali yıl için tek bir tutar olarak hesaplanan toplam amortisman tutarını nakleder.</span><span class="sxs-lookup"><span data-stu-id="bd00a-137">Yearly posts the total amount of the depreciation calculated for the fiscal year as one amount on the last day of the fiscal year.</span></span>
-   <span data-ttu-id="bd00a-138">Mali dönem, Defter sayfasında seçilen mali takvim için veya bir sabit kıymet defteri için seçilen mali takvim için tanımlanan mali dönemlere aktarılan mali yıl için hesaplanan toplam amortisman tutarını nakleder.</span><span class="sxs-lookup"><span data-stu-id="bd00a-138">Fiscal period posts the total amount of the depreciation calculated for the fiscal year, which is accrued into the fiscal periods that are defined for the fiscal calendar that is selected in the Ledger page, or for the fiscal calendar that is selected for the book for a fixed asset.</span></span>

## <a name="example-of-reducing-balance-depreciation"></a><span data-ttu-id="bd00a-139">Azalan bakiye amortismanı örneği</span><span class="sxs-lookup"><span data-stu-id="bd00a-139">Example of reducing balance depreciation</span></span>

<span data-ttu-id="bd00a-140">Sabit kıymet alım fiyatının 11.000, ıskarta değerinin 1.000 ve amortisman yüzde faktörünün 30 olduğunu varsayalım.</span><span class="sxs-lookup"><span data-stu-id="bd00a-140">Suppose that the fixed asset acquisition price is 11,000, the scrap value is 1,000, and the depreciation percentage factor is 30.</span></span> 

<span data-ttu-id="bd00a-141">Amortismana esas olan değerin yüzde 30'u (net defter değeri eksi hurda değeri), Azalan bakiye yöntemini kullanılarak önceki amortisman döneminin sonunda hesaplanır.</span><span class="sxs-lookup"><span data-stu-id="bd00a-141">Using the Reducing balance method, 30 percent of the depreciation base (net book value minus scrap value) is calculated at the end of the previous depreciation period.</span></span> <span data-ttu-id="bd00a-142">İlk üç yıla yönelik amortisman aşağıdaki tabloda gösterilmiştir.</span><span class="sxs-lookup"><span data-stu-id="bd00a-142">Depreciation for the first three years is shown in the following table.</span></span>

| <span data-ttu-id="bd00a-143">Dönem</span><span class="sxs-lookup"><span data-stu-id="bd00a-143">Period</span></span> | <span data-ttu-id="bd00a-144">Yıllık amortisman miktarı hesaplaması</span><span class="sxs-lookup"><span data-stu-id="bd00a-144">Calculation of yearly depreciation amount</span></span> | <span data-ttu-id="bd00a-145">Yıl sonunda net defter değeri</span><span class="sxs-lookup"><span data-stu-id="bd00a-145">Net book value at the end of the year</span></span> |
|--------|-------------------------------------------|---------------------------------------|
| <span data-ttu-id="bd00a-146">Yıl 1</span><span class="sxs-lookup"><span data-stu-id="bd00a-146">Year 1</span></span> | <span data-ttu-id="bd00a-147">(11.000 - 1.000) \* %30 = 3.000</span><span class="sxs-lookup"><span data-stu-id="bd00a-147">(11,000 - 1,000) \* 30% = 3,000</span></span>           | <span data-ttu-id="bd00a-148">(11.000 - 1.000) - 3.000 = 7.000</span><span class="sxs-lookup"><span data-stu-id="bd00a-148">(11,000 - 1,000) - 3,000 = 7,000</span></span>      |
| <span data-ttu-id="bd00a-149">2. yıl</span><span class="sxs-lookup"><span data-stu-id="bd00a-149">Year 2</span></span> | <span data-ttu-id="bd00a-150">(7.000 - 1.000) \* %30 = 1.800</span><span class="sxs-lookup"><span data-stu-id="bd00a-150">(7,000 - 1,000) \* 30% = 1,800</span></span>            | <span data-ttu-id="bd00a-151">(7.000 -1.800) = 5.200</span><span class="sxs-lookup"><span data-stu-id="bd00a-151">(7,000 -1,800) = 5,200</span></span>                |
| <span data-ttu-id="bd00a-152">3. yıl</span><span class="sxs-lookup"><span data-stu-id="bd00a-152">Year 3</span></span> | <span data-ttu-id="bd00a-153">(5.200 - 1.000) \* %30 = 1.260</span><span class="sxs-lookup"><span data-stu-id="bd00a-153">(5,200 - 1,000) \* 30% = 1,260</span></span>            | <span data-ttu-id="bd00a-154">(5.200 - 1.260) = 3.940</span><span class="sxs-lookup"><span data-stu-id="bd00a-154">(5,200 - 1,260) = 3,940</span></span>               |

 
-






