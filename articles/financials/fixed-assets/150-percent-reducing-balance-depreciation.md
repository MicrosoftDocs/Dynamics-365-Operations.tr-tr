---
title: "Yüzde 150 azalan bakiyeli amortisman"
description: "Bu makale, amortismanın Yüzde 150 Azalan bakiye yöntemi hakkında genel bir bakış sağlar."
author: saraschi2
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
ms.custom: 13891
ms.assetid: 36d1112d-921c-4fff-abe0-0ff2429848d3
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 20572163bd32d059323cbb80e606ae344d70b7be
ms.contentlocale: tr-tr
ms.lasthandoff: 09/29/2017

---

# <a name="150-percent-reducing-balance-depreciation"></a><span data-ttu-id="41f22-103">Yüzde 150 azalan bakiyeli amortisman</span><span class="sxs-lookup"><span data-stu-id="41f22-103">150 percent reducing balance depreciation</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="41f22-104">Bu makale, amortismanın Yüzde 150 Azalan bakiye yöntemi hakkında genel bir bakış sağlar.</span><span class="sxs-lookup"><span data-stu-id="41f22-104">This article gives an overview of the 150 percent reducing balance method of depreciation.</span></span>

<span data-ttu-id="41f22-105">Bir sabit kıymet amortisman profili ayarlayıp **Amortisman profilleri** sayfasındaki **Yöntem** alanında **%150 azalan bakiye** seçeneğini belirlediğinizde, amortisman profiline atanan sabit kıymetlerin amortismanı her amortisman döneminde aynı yüzdeyi içerir.</span><span class="sxs-lookup"><span data-stu-id="41f22-105">When you set up a fixed asset depreciation profile and select **150% reducing balance** in the **Method** field on the **Depreciation profiles** page, fixed assets that are assigned the depreciation profile are depreciated by the same percentage in each depreciation period.</span></span> <span data-ttu-id="41f22-106">Bu yüzde, sabit kıymetin servis ömrü temel alınarak hesaplanır.</span><span class="sxs-lookup"><span data-stu-id="41f22-106">This percentage is calculated based on the service life of the asset.</span></span> <span data-ttu-id="41f22-107">Örneğin, bir sabit kıymetin beş yıllık servis ömrü varsa, yüzde %30 (%150 ÷ 5) olarak hesaplanır.</span><span class="sxs-lookup"><span data-stu-id="41f22-107">For example, if an asset has a service life of five years, the percentage is calculated as 30 percent (150% ÷ 5).</span></span> 

<span data-ttu-id="41f22-108">%150 azalan bakiyeli amortisman ayarlamak için, **Amortisman profilleri** sayfasında **Amortisman yılı** alanı ve **Dönem sıklığı** alanındaki seçenekleri de belirlemeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="41f22-108">To set up 150% reducing balance depreciation, you must also select options in the **Depreciation year** field and the **Period frequency** field on the **Depreciation profiles** page.</span></span> <span data-ttu-id="41f22-109">**Dönem sıklığı** alanındaki kullanılabilir seçenekler, **Amortisman yılı** alanında seçili değere bağlı olarak değişir.</span><span class="sxs-lookup"><span data-stu-id="41f22-109">The options that are available in the **Period frequency** field vary, depending on the value that is selected in the **Depreciation year** field.</span></span>

## <a name="selection-of-depreciation-year"></a><span data-ttu-id="41f22-110">Amortisman yılının seçilmesi</span><span class="sxs-lookup"><span data-stu-id="41f22-110">Selection of depreciation year</span></span>
<span data-ttu-id="41f22-111">**Amortisman profilleri** sayasındaki **Amortisman yılı** alanından **Takvim** Yılı veya **Mali** Yıl seçimi yapabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="41f22-111">You can select either **Calendar** or **Fiscal** in the **Depreciation year** field on the **Depreciation profiles** page.</span></span> 

<span data-ttu-id="41f22-112">Varsayılan değer **Takvim** seçeneğidir.</span><span class="sxs-lookup"><span data-stu-id="41f22-112">The default value is **Calendar**.</span></span> <span data-ttu-id="41f22-113">Seçiminiz, **Dönem sıklığı** alanında bulunan seçenekleri belirler.</span><span class="sxs-lookup"><span data-stu-id="41f22-113">Your selection determines the options that are available in the **Period frequency** field.</span></span> <span data-ttu-id="41f22-114">Bu alan, amortisman tahakkuk deftere nakil tarihlerini ve tutarlarını takvim yılı boyunca tanımlar.</span><span class="sxs-lookup"><span data-stu-id="41f22-114">This field defines the depreciation accrual posting dates and amounts throughout the calendar year.</span></span>

### <a name="calendar"></a><span data-ttu-id="41f22-115">Takvim</span><span class="sxs-lookup"><span data-stu-id="41f22-115">Calendar</span></span>

<span data-ttu-id="41f22-116">**Amortisman yılı** alanında varsayılan değer olan **Takvim** seçeneğini bırakabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="41f22-116">You can keep the default value in the **Depreciation year** field, **Calendar**.</span></span> 

<span data-ttu-id="41f22-117">**Takvim** seçeneği, amortisman tabanını her yılın Ocak 1 tarihinde günceller.</span><span class="sxs-lookup"><span data-stu-id="41f22-117">The **Calendar** option updates the depreciation base on January 1 of each year.</span></span> <span data-ttu-id="41f22-118">Tipik olarak, amortisman tabanı, net defter değeri eksi ıskarta değeridir.</span><span class="sxs-lookup"><span data-stu-id="41f22-118">Typically, the depreciation base is the net book value minus the scrap value.</span></span> <span data-ttu-id="41f22-119">Bu konunun devamındaki örneklerde, amortisman tabanı hesaplamalar sütunundaki yer alan ilk ifadedeki pay olur.</span><span class="sxs-lookup"><span data-stu-id="41f22-119">In the examples later in this topic, the depreciation base is the numerator in the first expression in the calculations column.</span></span> 

<span data-ttu-id="41f22-120">Amortisman yılı olarak **Takvim** seçerseniz, **Dönem sıklığı** alanında şu seçenekler kullanılabilir :</span><span class="sxs-lookup"><span data-stu-id="41f22-120">If you select **Calendar** as the depreciation year, the following options are available in the **Period frequency** field:</span></span>

-   <span data-ttu-id="41f22-121">**Yıllık** 31 Aralık'ta bir tutarı nakleder.</span><span class="sxs-lookup"><span data-stu-id="41f22-121">**Yearly** posts an amount on December 31.</span></span>
-   <span data-ttu-id="41f22-122">**Aylık** seçeneği her takvim ayının sonunda bir aylık tutarı nakleder.</span><span class="sxs-lookup"><span data-stu-id="41f22-122">**Monthly** posts a monthly amount at the end of each calendar month.</span></span>
-   <span data-ttu-id="41f22-123">**Üç aylık** seçeneği, üç aylık takvim döneminin sonunda (31 Mart, 30 Haziran, 30 Eylül ve 31 Aralık) bir üç aylık tutar nakleder.</span><span class="sxs-lookup"><span data-stu-id="41f22-123">**Quarterly** posts a quarterly amount at the end of each calendar quarter (March 31, June 30, September 30, and December 31).</span></span>
-   <span data-ttu-id="41f22-124">**Yarı yıllık** seçeneği takvim yarı yılında ( 30 Haziran ve 31 Aralık) yarı yıllık tutarı nakleder.</span><span class="sxs-lookup"><span data-stu-id="41f22-124">**Half-Yearly** posts a half-yearly amount at the calendar half year (June 30 and December 31).</span></span>
-   <span data-ttu-id="41f22-125">**Günlük** seçeneği her gün için bir işlem kullanarak günlük amortisman yöntemi için amortisman tutarını nakleder.</span><span class="sxs-lookup"><span data-stu-id="41f22-125">**Daily** posts the depreciation amount for the daily depreciation method by using one transaction for each day.</span></span>

### <a name="fiscal"></a><span data-ttu-id="41f22-126">Mali</span><span class="sxs-lookup"><span data-stu-id="41f22-126">Fiscal</span></span>

<span data-ttu-id="41f22-127">**Amortisman yılı** alanında **Mali** seçeneğini belirlerseniz, %150 azalan bakiyeli amortisman defter için belirtilen mali takvim için veya **Genel muhasebe** sayfasında seçilen mali takvim için mali yıla dayalı olarak hesaplanır.</span><span class="sxs-lookup"><span data-stu-id="41f22-127">If you select **Fiscal** in the **Depreciation year** field, 150% reducing balance depreciation is calculated based on the fiscal year for the fiscal calendar that is specified for the book, or for the fiscal calendar that is selected on the **Ledger** page.</span></span> <span data-ttu-id="41f22-128">Mali takvimler, **Mali Takvimler** sayfasında ayarlanır.</span><span class="sxs-lookup"><span data-stu-id="41f22-128">Fiscal calendars are set up on the **Fiscal calendars** page.</span></span> 

<span data-ttu-id="41f22-129">Örneğin, 1 Temmuz ile 30 Haziran arasındaki mali yıl için amortisman hesaplaması 1 Temmuz'da başlar.</span><span class="sxs-lookup"><span data-stu-id="41f22-129">For example, for the fiscal year July 1 through June 30, the depreciation calculation starts on July 1.</span></span> <span data-ttu-id="41f22-130">Mali yıl 12 aydan daha uzun veya daha kısa olabilir.</span><span class="sxs-lookup"><span data-stu-id="41f22-130">The fiscal year can be longer or shorter than 12 months.</span></span> <span data-ttu-id="41f22-131">Amortisman her dönem için ayarlanır.</span><span class="sxs-lookup"><span data-stu-id="41f22-131">The depreciation is adjusted for each period.</span></span> <span data-ttu-id="41f22-132">Bir sonraki mali yılın uzunluğu, **Mali takvimler** sayfasında ayarlanan mali dönemler tarafından belirlenir.</span><span class="sxs-lookup"><span data-stu-id="41f22-132">The length of the next fiscal year is determined by the setup of periods on the **Fiscal calendars** page.</span></span> 

<span data-ttu-id="41f22-133">Amortisman yılı olarak **Mali** seçerseniz, **Dönem sıklığı** alanında şu seçenekler kullanılabilir:</span><span class="sxs-lookup"><span data-stu-id="41f22-133">If you select **Fiscal** as the depreciation year, the following options are available in the **Period frequency** field:</span></span>

-   <span data-ttu-id="41f22-134">**Yıllık** seçeneği, mali yıl için hesaplanan toplam amortisman tutarını, mali yılın son gününde nakleder.</span><span class="sxs-lookup"><span data-stu-id="41f22-134">**Yearly** posts the total amount of the depreciation that is calculated for the fiscal year on the last day of the fiscal year.</span></span>
-   <span data-ttu-id="41f22-135">**Mali dönem**, mali yıl için hesaplanan toplam amortisman tutarını nakleder.</span><span class="sxs-lookup"><span data-stu-id="41f22-135">**Fiscal period** posts the total amount of the depreciation that is calculated for the fiscal year.</span></span> <span data-ttu-id="41f22-136">Bu tutar, **Mali Takvimler** sayfası üzerinde tanımlanan mali dönemlere tahakkuk edilir.</span><span class="sxs-lookup"><span data-stu-id="41f22-136">This amount is accrued into the fiscal periods that are defined on the **Fiscal calendars** page.</span></span>

## <a name="example-of-150-reducing-balance-depreciation"></a><span data-ttu-id="41f22-137">%150 azalan bakiyeli amortisman örneği</span><span class="sxs-lookup"><span data-stu-id="41f22-137">Example of 150% reducing balance depreciation</span></span>
|                                |        |
|--------------------------------|--------|
| <span data-ttu-id="41f22-138">Alım maliyeti</span><span class="sxs-lookup"><span data-stu-id="41f22-138">Acquisition cost</span></span>               | <span data-ttu-id="41f22-139">11.000</span><span class="sxs-lookup"><span data-stu-id="41f22-139">11,000</span></span> |
| <span data-ttu-id="41f22-140">Hurda değeri</span><span class="sxs-lookup"><span data-stu-id="41f22-140">Salvage value</span></span>                  | <span data-ttu-id="41f22-141">1.000</span><span class="sxs-lookup"><span data-stu-id="41f22-141">1,000</span></span>  |
| <span data-ttu-id="41f22-142">Amortisman tabanı</span><span class="sxs-lookup"><span data-stu-id="41f22-142">Depreciation base</span></span>              | <span data-ttu-id="41f22-143">10.000</span><span class="sxs-lookup"><span data-stu-id="41f22-143">10,000</span></span> |
| <span data-ttu-id="41f22-144">Servis ömrü yıl sayısı</span><span class="sxs-lookup"><span data-stu-id="41f22-144">Service life years</span></span>             | <span data-ttu-id="41f22-145">5</span><span class="sxs-lookup"><span data-stu-id="41f22-145">5</span></span>      |
| <span data-ttu-id="41f22-146">Yıllık amortisman yüzdesi</span><span class="sxs-lookup"><span data-stu-id="41f22-146">Yearly depreciation percentage</span></span> | <span data-ttu-id="41f22-147">%30</span><span class="sxs-lookup"><span data-stu-id="41f22-147">30%</span></span>    |

<span data-ttu-id="41f22-148">%150 azalan bakiye yöntemi, yüzde 150'ü servis ömrü yıl sayısına böler.</span><span class="sxs-lookup"><span data-stu-id="41f22-148">The 150% reducing balance method divides 150 percent by the service life years.</span></span> <span data-ttu-id="41f22-149">Elde edilen yüzde, yıla ait amortisman tutarını belirlemek üzere, sabit kıymetin net defter değeriyle çarpılacaktır.</span><span class="sxs-lookup"><span data-stu-id="41f22-149">That percentage will be multiplied by the net book value of the asset to determine the depreciation amount for the year.</span></span>

| <span data-ttu-id="41f22-150">Dönem</span><span class="sxs-lookup"><span data-stu-id="41f22-150">Period</span></span> | <span data-ttu-id="41f22-151">Yıllık amortisman miktarının hesaplaması</span><span class="sxs-lookup"><span data-stu-id="41f22-151">Calculation of the yearly depreciation amount</span></span> | <span data-ttu-id="41f22-152">Defter değeri</span><span class="sxs-lookup"><span data-stu-id="41f22-152">Book value</span></span>             | <span data-ttu-id="41f22-153">Yıl sonunda net defter değeri</span><span class="sxs-lookup"><span data-stu-id="41f22-153">Net book value at the end of the year</span></span> |
|--------|-----------------------------------------------|------------------------|---------------------------------------|
| <span data-ttu-id="41f22-154">Yıl 1</span><span class="sxs-lookup"><span data-stu-id="41f22-154">Year 1</span></span> | <span data-ttu-id="41f22-155">(11.000 – 1.000) × 30% = 3.000</span><span class="sxs-lookup"><span data-stu-id="41f22-155">(11,000 – 1,000) × 30% = 3,000</span></span>                | <span data-ttu-id="41f22-156">11.000 – 3.000 = 8.000</span><span class="sxs-lookup"><span data-stu-id="41f22-156">11,000 – 3,000 = 8,000</span></span> | <span data-ttu-id="41f22-157">11.000 – 1.000 – 3.000 = 7.000</span><span class="sxs-lookup"><span data-stu-id="41f22-157">11,000 – 1,000 – 3,000 = 7,000</span></span>        |
| <span data-ttu-id="41f22-158">2. yıl</span><span class="sxs-lookup"><span data-stu-id="41f22-158">Year 2</span></span> | <span data-ttu-id="41f22-159">7.000 × 30% = 2.100</span><span class="sxs-lookup"><span data-stu-id="41f22-159">7,000 × 30% = 2,100</span></span>                           | <span data-ttu-id="41f22-160">8.000 – 2.100 = 5.900</span><span class="sxs-lookup"><span data-stu-id="41f22-160">8,000 – 2,100 = 5,900</span></span>  | <span data-ttu-id="41f22-161">7.000 – 2.100 = 4.900</span><span class="sxs-lookup"><span data-stu-id="41f22-161">7,000 – 2,100 = 4,900</span></span>                 |
| <span data-ttu-id="41f22-162">3. yıl</span><span class="sxs-lookup"><span data-stu-id="41f22-162">Year 3</span></span> | <span data-ttu-id="41f22-163">4.900 × 30% = 1.470</span><span class="sxs-lookup"><span data-stu-id="41f22-163">4,900 × 30% = 1,470</span></span>                           | <span data-ttu-id="41f22-164">5.900 – 1.470 = 4.430</span><span class="sxs-lookup"><span data-stu-id="41f22-164">5,900 – 1,470 = 4,430</span></span>  | <span data-ttu-id="41f22-165">4.900 – 1.470 = 3.430</span><span class="sxs-lookup"><span data-stu-id="41f22-165">4,900 – 1,470 = 3,430</span></span>                 |

> [!NOTE]
> <span data-ttu-id="41f22-166">Tipik olarak, %150 azalan bakiye amortismanı yöntemi kullanılarak hesaplanan tutar sabit amortisman yöntemi kullanılarak hesaplanacak yöntemden daha az olduğunda, kalan ömür için sabit amortisman yöntemine bir dönüş olur.</span><span class="sxs-lookup"><span data-stu-id="41f22-166">Typically, when the amount that is calculated by using the 150% reducing balance depreciation method becomes less than the amount that would be calculated by using the straight line method, there is a conversion to the straight line method for the remaining life.</span></span>




