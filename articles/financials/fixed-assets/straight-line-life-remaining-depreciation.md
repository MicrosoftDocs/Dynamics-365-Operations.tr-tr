---
title: "Sabit kalan ömür amortismanı"
description: "Bu makale, amortismanın Sabit kalan ömür yöntemi hakkında genel bir bakış sağlar."
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
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 13851
ms.assetid: 0fa2f71a-596c-414c-a6e6-8f7405a0bf81
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 4ad82f3177e4abb7b9cb575b910aabc69901f475
ms.contentlocale: tr-tr
ms.lasthandoff: 09/29/2017

---

# <a name="straight-line-life-remaining-depreciation"></a><span data-ttu-id="45872-103">Sabit kalan ömür amortismanı</span><span class="sxs-lookup"><span data-stu-id="45872-103">Straight line life remaining depreciation</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="45872-104">Bu makale, amortismanın Sabit kalan ömür yöntemi hakkında genel bir bakış sağlar.</span><span class="sxs-lookup"><span data-stu-id="45872-104">This article gives an overview of the Straight line life remaining method of depreciation.</span></span>

<span data-ttu-id="45872-105">Bir sabit kıymek amortisman profili ayarladığınızda ve **Amortisman profilleri** sayfasındaki **Yöntem** alanından **Kalan düz çizgi yaşamı** öğesini seçtiğinizde amortisman profiline atanan sabit kıymetlerin amortismanı kıymetin kalan hizmet ömrüne dayalı olacaktır.</span><span class="sxs-lookup"><span data-stu-id="45872-105">When you set up a fixed asset depreciation profile and select **Straight line life remaining** in the **Method** field on the **Depreciation profiles** page, the depreciation of fixed assets that are assigned to the depreciation profile is based on the remaining service life of the asset.</span></span> <span data-ttu-id="45872-106">Amortisman tutarı genellikle her amortisman döneminde aynı olur.</span><span class="sxs-lookup"><span data-stu-id="45872-106">The depreciation amount is generally the same in each depreciation period.</span></span> <span data-ttu-id="45872-107">Düz çizgi kalan ömür amortismanı ayarlamak için, **Amortisman profilleri** sayfasında **Amortisman yılı** alanı ve **Dönem sıklığı** alanındaki seçenekleri de belirlemeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="45872-107">To set up straight line life remaining depreciation, you also must select options in the **Depreciation year** field and the **Period frequency** field on the **Depreciation profiles** page.</span></span> <span data-ttu-id="45872-108">**Dönem sıklığı** alanındaki kullanılabilir seçenekler, **Amortisman yılı** alanında seçili değere bağlı olarak değişir.</span><span class="sxs-lookup"><span data-stu-id="45872-108">The options that are available in the **Period frequency** field vary, depending on the value that is selected in the **Depreciation year** field.</span></span>

## <a name="select-a-depreciation-year"></a><span data-ttu-id="45872-109">Bir amortisman yılı seçin</span><span class="sxs-lookup"><span data-stu-id="45872-109">Select a depreciation year</span></span>
<span data-ttu-id="45872-110">**Amortisman profilleri** sayasındaki **Amortisman yılı** alanından **Takvim** Yılı veya **Mali** Yıl seçimi yapabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="45872-110">You can select either **Calendar** or **Fiscal** in the **Depreciation year** field on the **Depreciation profiles** page.</span></span> <span data-ttu-id="45872-111">Varsayılan değer **Takvim** seçeneğidir.</span><span class="sxs-lookup"><span data-stu-id="45872-111">The default value is **Calendar**.</span></span> <span data-ttu-id="45872-112">Seçiminiz, **Dönem sıklığı** alanında bulunan seçenekleri belirler.</span><span class="sxs-lookup"><span data-stu-id="45872-112">Your selection determines the options that are available in the **Period frequency** field.</span></span> <span data-ttu-id="45872-113">Bu alan, amortisman tahakkuk deftere nakil tarihlerini ve tutarlarını takvim yılı boyunca tanımlar.</span><span class="sxs-lookup"><span data-stu-id="45872-113">This field defines the depreciation accrual posting dates and amounts throughout the calendar year.</span></span>

### <a name="calendar"></a><span data-ttu-id="45872-114">Takvim</span><span class="sxs-lookup"><span data-stu-id="45872-114">Calendar</span></span>

<span data-ttu-id="45872-115">***Amortisman yılı*** alanından **Takvim** öğesini seçerseniz, takvim yılını farklı tanımlasanız dahi yılın 1 Ocak ile 31 Aralık arasında olduğu kabul edilir.</span><span class="sxs-lookup"><span data-stu-id="45872-115">If you select **Calendar** in the ***Depreciation year*** field, a year of January 1 through December 31 is assumed, even if you've defined the fiscal calendar differently.</span></span> <span data-ttu-id="45872-116">**Takvim** seçeneği, amortisman tabanını her yılın Ocak 1 tarihinde günceller.</span><span class="sxs-lookup"><span data-stu-id="45872-116">The **Calendar** option updates the depreciation base on January 1 of each year.</span></span> <span data-ttu-id="45872-117">Tipik olarak, amortisman tabanı, net defter değeri eksi hurda değeridir.</span><span class="sxs-lookup"><span data-stu-id="45872-117">Typically, the depreciation base is the net book value minus the salvage value.</span></span> <span data-ttu-id="45872-118">Bu konunun devamındaki örnekte, amortisman tabanı hesaplamalar sütunundaki yer alan ilk ifadedeki pay olur.</span><span class="sxs-lookup"><span data-stu-id="45872-118">In the example later in this topic, the depreciation base is the numerator in the first expression in the calculations column.</span></span> <span data-ttu-id="45872-119">Amortisman yılı olarak **Takvim** seçerseniz, **Dönem sıklığı** alanında şu seçenekler kullanılabilir :</span><span class="sxs-lookup"><span data-stu-id="45872-119">If you select **Calendar** as the depreciation year, the following options are available in the **Period frequency** field:</span></span>

-   <span data-ttu-id="45872-120">**Yıllık** 31 Aralık'ta bir tutarı nakleder.</span><span class="sxs-lookup"><span data-stu-id="45872-120">**Yearly** posts an amount on December 31.</span></span>
-   <span data-ttu-id="45872-121">**Aylık** seçeneği her takvim ayının sonunda bir aylık tutarı nakleder.</span><span class="sxs-lookup"><span data-stu-id="45872-121">**Monthly** posts a monthly amount at the end of each calendar month.</span></span>
-   <span data-ttu-id="45872-122">**Üç aylık** seçeneği, üç aylık takvim döneminin sonunda (31 Mart, 30 Haziran, 30 Eylül ve 31 Aralık) bir üç aylık tutar nakleder.</span><span class="sxs-lookup"><span data-stu-id="45872-122">**Quarterly** posts a quarterly amount at the end of each calendar quarter (March 31, June 30, September 30, and December 31).</span></span>
-   <span data-ttu-id="45872-123">**Altı Aylık** seçeneği, altı aylık takvim döneminde ( 30 Haziran ve 31 Aralık) bir altı aylık tutar nakleder.</span><span class="sxs-lookup"><span data-stu-id="45872-123">**Half-Yearly** posts a half-yearly amount at the end of each calendar half year (June 30 and December 31).</span></span>
-   <span data-ttu-id="45872-124">**Günlük** seçeneği her gün için bir işlem kullanarak günlük amortisman yöntemi için amortisman tutarını nakleder.</span><span class="sxs-lookup"><span data-stu-id="45872-124">**Daily** posts the depreciation amount for the daily depreciation method by using one transaction for each day.</span></span>

<span data-ttu-id="45872-125">Örneğin, **Yıllık** seçeneğini belirlerseniz yıllık amortisman her yılın 31 Aralık tarihinde yalnızca bir defa nakledilir.</span><span class="sxs-lookup"><span data-stu-id="45872-125">For example, if you select **Yearly**, the yearly depreciation is posted only one time, on December 31 of each year.</span></span> <span data-ttu-id="45872-126">**Aylık** seçeneğini belirlerseniz aylık amortisman her ayı, yıllık amortisman tutarının on ikide biri oranında nakleder</span><span class="sxs-lookup"><span data-stu-id="45872-126">If you select **Monthly**, the monthly depreciation is posted each month, as one-twelfth of the yearly depreciation amount.</span></span>

### <a name="fiscal"></a><span data-ttu-id="45872-127">Mali</span><span class="sxs-lookup"><span data-stu-id="45872-127">Fiscal</span></span>

<span data-ttu-id="45872-128">**Amortisman yılı** alanından **Mali Yıl** seçimini yaparsanız düz çizgi kalan yaşam amortismanı kullanılır</span><span class="sxs-lookup"><span data-stu-id="45872-128">If you select **Fiscal** in the **Depreciation year** field, straight line life remaining depreciation is used.</span></span> <span data-ttu-id="45872-129">Amortisman, kalan mali yıllar temel alınarak hesaplanır.</span><span class="sxs-lookup"><span data-stu-id="45872-129">Depreciation is calculated based on the fiscal years remaining.</span></span> <span data-ttu-id="45872-130">Örneğin, 1 Temmuz 2015 ile 30 Haziran 2016 arasındaki mali yıl için amortisman hesaplaması 1 Temmuz'da başlar.</span><span class="sxs-lookup"><span data-stu-id="45872-130">For example, for the fiscal year July 1, 2015, through June 30, 2016, the depreciation calculation starts on July 1.</span></span> <span data-ttu-id="45872-131">Mali yıl 12 aydan daha uzun veya daha kısa olabilir.</span><span class="sxs-lookup"><span data-stu-id="45872-131">The fiscal year can be longer or shorter than 12 months.</span></span> <span data-ttu-id="45872-132">Amortisman her mali dönem için ayarlanır.</span><span class="sxs-lookup"><span data-stu-id="45872-132">The depreciation is adjusted for each fiscal period.</span></span> <span data-ttu-id="45872-133">Bir sonraki mali yılın uzunluğu, **Mali takvimler** sayfasında ayarlanan mali dönemler tarafından belirlenir.</span><span class="sxs-lookup"><span data-stu-id="45872-133">The length of the next fiscal year is determined by the fiscal periods that are set up on the **Fiscal calendars** page.</span></span> <span data-ttu-id="45872-134">Amortisman yılı olarak **Mali** seçerseniz, **Dönem sıklığı** alanında şu seçenekler kullanılabilir:</span><span class="sxs-lookup"><span data-stu-id="45872-134">If you select **Fiscal** as the depreciation year, the following options are available in the **Period frequency** field:</span></span>

-   <span data-ttu-id="45872-135">**Yıllık**, mali yıl için hesaplanan toplam amortisman tutarını tek tutar olarak, mali yılın son gününde nakleder.</span><span class="sxs-lookup"><span data-stu-id="45872-135">**Yearly** posts the total amount of the depreciation that is calculated for the fiscal year as one amount, on the last day of the fiscal year.</span></span>
-   <span data-ttu-id="45872-136">**Mali dönem** seçeneği, mali yılın amortismanının toplam tutarını hesaplar.</span><span class="sxs-lookup"><span data-stu-id="45872-136">**Fiscal period** calculates the total amount of the depreciation for the fiscal year.</span></span> <span data-ttu-id="45872-137">Bu tutar daha sonra, defter için belirtilen mali takvim için **Mali takvimler** sayfasında tanımlanan mali dönemlere aktarılır.</span><span class="sxs-lookup"><span data-stu-id="45872-137">This amount is then accrued into the fiscal periods that are defined on the **Fiscal calendars** page for the fiscal calendar that is specified for the book.</span></span>

## <a name="example-of-straight-line-depreciation-of-an-unchanged-fixed-asset"></a><span data-ttu-id="45872-138">Değişmeyen bir sabit kıymet için düz çizgi amortisman örneği</span><span class="sxs-lookup"><span data-stu-id="45872-138">Example of straight line depreciation of an unchanged fixed asset</span></span>
<span data-ttu-id="45872-139">Bir sabit kıymet aşağıdaki özelliklere sahiptir.</span><span class="sxs-lookup"><span data-stu-id="45872-139">A fixed asset has the following characteristics.</span></span>

|                     |        |
|---------------------|--------|
| <span data-ttu-id="45872-140">Alım maliyeti</span><span class="sxs-lookup"><span data-stu-id="45872-140">Acquisition cost</span></span>    | <span data-ttu-id="45872-141">11.000</span><span class="sxs-lookup"><span data-stu-id="45872-141">11,000</span></span> |
| <span data-ttu-id="45872-142">Hurda değeri</span><span class="sxs-lookup"><span data-stu-id="45872-142">Salvage value</span></span>       | <span data-ttu-id="45872-143">1.000</span><span class="sxs-lookup"><span data-stu-id="45872-143">1,000</span></span>  |
| <span data-ttu-id="45872-144">Amortisman tabanı</span><span class="sxs-lookup"><span data-stu-id="45872-144">Depreciation base</span></span>   | <span data-ttu-id="45872-145">10.000</span><span class="sxs-lookup"><span data-stu-id="45872-145">10,000</span></span> |
| <span data-ttu-id="45872-146">Servis ömrü yıl sayısı</span><span class="sxs-lookup"><span data-stu-id="45872-146">Service life years</span></span>  | <span data-ttu-id="45872-147">5</span><span class="sxs-lookup"><span data-stu-id="45872-147">5</span></span>      |
| <span data-ttu-id="45872-148">Yıllık amortisman</span><span class="sxs-lookup"><span data-stu-id="45872-148">Yearly depreciation</span></span> | <span data-ttu-id="45872-149">2.000</span><span class="sxs-lookup"><span data-stu-id="45872-149">2,000</span></span>  |

<span data-ttu-id="45872-150">Amortisman tutarı her yıl aynıdır: (Edinme maliyeti – Hurda değeri) ÷ Servis ömrü yıl</span><span class="sxs-lookup"><span data-stu-id="45872-150">The depreciation amount is the same every year: (Acquisition cost – Salvage value) ÷ Service life years</span></span>

| <span data-ttu-id="45872-151">Dönem</span><span class="sxs-lookup"><span data-stu-id="45872-151">Period</span></span> | <span data-ttu-id="45872-152">Yıllık amortisman miktarının hesaplaması</span><span class="sxs-lookup"><span data-stu-id="45872-152">Calculation of the yearly depreciation amount</span></span> | <span data-ttu-id="45872-153">Yıl sonunda net defter değeri</span><span class="sxs-lookup"><span data-stu-id="45872-153">Net book value at the end of the year</span></span> |
|--------|-----------------------------------------------|---------------------------------------|
| <span data-ttu-id="45872-154">Yıl 1</span><span class="sxs-lookup"><span data-stu-id="45872-154">Year 1</span></span> | <span data-ttu-id="45872-155">(11.000 – 1.000) ÷ 5 = 2.000</span><span class="sxs-lookup"><span data-stu-id="45872-155">(11,000 – 1,000) ÷ 5 = 2,000</span></span>                  | <span data-ttu-id="45872-156">9.000</span><span class="sxs-lookup"><span data-stu-id="45872-156">9,000</span></span>                                 |
| <span data-ttu-id="45872-157">2. yıl</span><span class="sxs-lookup"><span data-stu-id="45872-157">Year 2</span></span> | <span data-ttu-id="45872-158">(9.000 – 1.000) ÷ 4 = 2.000</span><span class="sxs-lookup"><span data-stu-id="45872-158">(9,000 – 1,000) ÷ 4 = 2,000</span></span>                   | <span data-ttu-id="45872-159">7.000</span><span class="sxs-lookup"><span data-stu-id="45872-159">7,000</span></span>                                 |
| <span data-ttu-id="45872-160">3. yıl</span><span class="sxs-lookup"><span data-stu-id="45872-160">Year 3</span></span> | <span data-ttu-id="45872-161">(7.000 – 1.000) ÷ 3 = 2.000</span><span class="sxs-lookup"><span data-stu-id="45872-161">(7,000 – 1,000) ÷ 3 = 2,000</span></span>                   | <span data-ttu-id="45872-162">5.000</span><span class="sxs-lookup"><span data-stu-id="45872-162">5,000</span></span>                                 |
| <span data-ttu-id="45872-163">Yıl 4</span><span class="sxs-lookup"><span data-stu-id="45872-163">Year 4</span></span> | <span data-ttu-id="45872-164">(5.000 – 1.000) ÷ 2 = 2.000</span><span class="sxs-lookup"><span data-stu-id="45872-164">(5,000 – 1,000) ÷ 2 = 2,000</span></span>                   | <span data-ttu-id="45872-165">3.000</span><span class="sxs-lookup"><span data-stu-id="45872-165">3,000</span></span>                                 |
| <span data-ttu-id="45872-166">Yıl 5</span><span class="sxs-lookup"><span data-stu-id="45872-166">Year 5</span></span> | <span data-ttu-id="45872-167">(3.000 – 1.000) ÷ 1 = 2.000</span><span class="sxs-lookup"><span data-stu-id="45872-167">(3,000 – 1,000) ÷ 1 = 2,000</span></span>                   | <span data-ttu-id="45872-168">1.000</span><span class="sxs-lookup"><span data-stu-id="45872-168">1,000</span></span>                                 |






