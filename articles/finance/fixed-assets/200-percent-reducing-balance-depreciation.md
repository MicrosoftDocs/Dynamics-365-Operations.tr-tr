---
title: Yüzde 200 azalan bakiyeli amortisman
description: Bu makalede, yüzde 200 amortisman bilanço azaltma yöntemine genel bakış sunulmuştur.
author: saraschi2
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
ms.custom: 13951
ms.assetid: 69b4e010-7683-4dc2-8a06-6d572f37e903
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0474a8cecccaf1e23874458c27e0bea991140b6c
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "4448860"
---
# <a name="200-percent-reducing-balance-depreciation"></a><span data-ttu-id="aa31e-103">Yüzde 200 azalan bakiyeli amortisman</span><span class="sxs-lookup"><span data-stu-id="aa31e-103">200 percent reducing balance depreciation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="aa31e-104">Bu makalede, yüzde 200 amortisman bilanço azaltma yöntemine genel bakış sunulmuştur.</span><span class="sxs-lookup"><span data-stu-id="aa31e-104">This article gives an overview of the 200 percent reducing balance method of depreciation.</span></span>

<span data-ttu-id="aa31e-105">Bir sabit kıymet amortisman profili ayarlayıp **Amortisman profilleri** sayfasındaki **Yöntem** alanında **%200 azalan bakiye** seçeneğini belirlediğinizde, amortisman profiline atanan sabit kıymetlerin amortismanı her amortisman döneminde aynı yüzdeyi içerir.</span><span class="sxs-lookup"><span data-stu-id="aa31e-105">When you set up a fixed asset depreciation profile and select **200% reducing balance** in the **Method** field on the **Depreciation profiles** page, fixed assets that are assigned the depreciation profile are depreciated by the same percentage in each depreciation period.</span></span> <span data-ttu-id="aa31e-106">Yüzde, sabit kıymetin servis ömrü temel alınarak hesaplanır.</span><span class="sxs-lookup"><span data-stu-id="aa31e-106">The percentage is calculated based on the service life of the asset.</span></span> <span data-ttu-id="aa31e-107">Örneğin, bir sabit kıymetin beş yıllık servis ömrü varsa, yüzde 40 (%200 ÷ 5) olarak hesaplanır.</span><span class="sxs-lookup"><span data-stu-id="aa31e-107">For example, if an asset has a service life of five years, the percentage is calculated as 40 percent (200% ÷ 5).</span></span> 

<span data-ttu-id="aa31e-108">Bu yöntem çift azalan bakiye olarak da bilinir.</span><span class="sxs-lookup"><span data-stu-id="aa31e-108">This method is also known as double declining balance.</span></span>

<span data-ttu-id="aa31e-109">%200 azalan bakiyeli amortisman ayarlamak için, **Amortisman profilleri** sayfasında **Amortisman yılı** alanı ve **Dönem sıklığı** alanındaki seçenekleri de belirlemeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="aa31e-109">To set up 200% reducing balance depreciation, you must also select options in the **Depreciation year** field and the **Period frequency** field on the **Depreciation profiles** page.</span></span> <span data-ttu-id="aa31e-110">**Dönem sıklığı** alanındaki kullanılabilir seçenekler, **Amortisman yılı** alanında seçtiğiniz değere bağlı olarak değişir.</span><span class="sxs-lookup"><span data-stu-id="aa31e-110">The options that are available in the **Period frequency** field vary, depending on the value that you select in the **Depreciation year** field.</span></span>

## <a name="select-a-depreciation-year"></a><span data-ttu-id="aa31e-111">Bir amortisman yılı seçin</span><span class="sxs-lookup"><span data-stu-id="aa31e-111">Select a depreciation year</span></span>
<span data-ttu-id="aa31e-112">**Amortisman profilleri** sayasındaki **Amortisman yılı** alanından **Takvim** Yılı veya **Mali** Yıl seçimi yapabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="aa31e-112">You can select either **Calendar** or **Fiscal** in the **Depreciation year** field on the **Depreciation profiles** page.</span></span> <span data-ttu-id="aa31e-113">Varsayılan değer **Takvim** seçeneğidir.</span><span class="sxs-lookup"><span data-stu-id="aa31e-113">The default value is **Calendar**.</span></span> 

<span data-ttu-id="aa31e-114">Seçiminiz, **Dönem sıklığı** alanında bulunan seçenekleri belirler.</span><span class="sxs-lookup"><span data-stu-id="aa31e-114">Your selection determines the options that are available in the **Period frequency** field.</span></span> <span data-ttu-id="aa31e-115">Bu alan, amortisman tahakkuk deftere nakil tarihlerini ve tutarlarını takvim yılı boyunca tanımlar.</span><span class="sxs-lookup"><span data-stu-id="aa31e-115">This field defines the depreciation accrual posting dates and amounts throughout the calendar year.</span></span>

### <a name="calendar"></a><span data-ttu-id="aa31e-116">Takvim</span><span class="sxs-lookup"><span data-stu-id="aa31e-116">Calendar</span></span>

<span data-ttu-id="aa31e-117">**Amortisman yılı** alanında varsayılan değer olan **Takvim** seçeneğini bırakabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="aa31e-117">You can keep the default value in the **Depreciation year** field, **Calendar**.</span></span> 

<span data-ttu-id="aa31e-118">**Takvim** seçeneği, amortisman tabanını her yılın Ocak 1 tarihinde günceller.</span><span class="sxs-lookup"><span data-stu-id="aa31e-118">The **Calendar** option updates the depreciation base on January 1 of each year.</span></span> <span data-ttu-id="aa31e-119">Tipik olarak, amortisman net defter değeri eksi ıskarta değeridir.</span><span class="sxs-lookup"><span data-stu-id="aa31e-119">Typically, the depreciation is the net book value minus the scrap value.</span></span> <span data-ttu-id="aa31e-120">Bu konunun devamındaki örneklerde, amortisman tabanı hesaplamalar sütunundaki yer alan ilk ifadedeki pay olur.</span><span class="sxs-lookup"><span data-stu-id="aa31e-120">In the examples later in this topic, the depreciation base is the numerator in the first expression in the calculations column.</span></span> 

<span data-ttu-id="aa31e-121">Amortisman yılı olarak **Takvim** seçerseniz, **Dönem sıklığı** alanında şu seçenekler kullanılabilir :</span><span class="sxs-lookup"><span data-stu-id="aa31e-121">If you select **Calendar** as the depreciation year, the following options are available in the **Period frequency** field:</span></span>

-   <span data-ttu-id="aa31e-122">**Yıllık** 31 Aralık'ta bir tutarı nakleder.</span><span class="sxs-lookup"><span data-stu-id="aa31e-122">**Yearly** posts an amount on December 31.</span></span>
-   <span data-ttu-id="aa31e-123">**Aylık** seçeneği her takvim ayının sonunda bir aylık tutarı nakleder.</span><span class="sxs-lookup"><span data-stu-id="aa31e-123">**Monthly** posts a monthly amount at the end of each calendar month.</span></span>
-   <span data-ttu-id="aa31e-124">**Üç aylık** seçeneği, üç aylık takvim döneminin sonunda (31 Mart, 30 Haziran, 30 Eylül ve 31 Aralık) bir üç aylık tutar nakleder.</span><span class="sxs-lookup"><span data-stu-id="aa31e-124">**Quarterly** posts a quarterly amount at the end of each calendar quarter (March 31, June 30, September 30, and December 31).</span></span>
-   <span data-ttu-id="aa31e-125">**Yarı yıllık** seçeneği takvim yarı yılında ( 30 Haziran ve 31 Aralık) yarı yıllık tutarı nakleder.</span><span class="sxs-lookup"><span data-stu-id="aa31e-125">**Half-Yearly** posts a half-yearly amount at the calendar half year (June 30 and December 31).</span></span>
-   <span data-ttu-id="aa31e-126">**Günlük** seçeneği her gün için bir işlem kullanarak günlük amortisman yöntemi için amortisman tutarını nakleder.</span><span class="sxs-lookup"><span data-stu-id="aa31e-126">**Daily** posts the depreciation amount for the daily depreciation method by using one transaction for each day.</span></span>

### <a name="fiscal"></a><span data-ttu-id="aa31e-127">Mali</span><span class="sxs-lookup"><span data-stu-id="aa31e-127">Fiscal</span></span>

<span data-ttu-id="aa31e-128">**Amortisman** yılı alanında **Mali** seçeneğini belirlerseniz, %200 azalan bakiyeli amortisman defter için belirtilen mali takvim için veya **Genel muhasebe** sayfasında seçilen mali takvim için mali yıla dayalı olarak hesaplanır.</span><span class="sxs-lookup"><span data-stu-id="aa31e-128">If you select **Fiscal** in the **Depreciation** year field, 200% reducing balance depreciation is calculated based on the fiscal year for the fiscal calendar that is specified for the book, or for the fiscal calendar that is selected on the **Ledger** page.</span></span> <span data-ttu-id="aa31e-129">Mali takvimler, **Mali Takvimler** sayfasında ayarlanır.</span><span class="sxs-lookup"><span data-stu-id="aa31e-129">Fiscal calendars are set up on the **Fiscal calendars** page.</span></span> 

<span data-ttu-id="aa31e-130">Örneğin, 1 Temmuz ile 30 Haziran arasındaki mali yıl için amortisman hesaplaması 1 Temmuz'da başlar.</span><span class="sxs-lookup"><span data-stu-id="aa31e-130">For example, for the fiscal year July 1 through June 30, the depreciation calculation starts on July 1.</span></span> <span data-ttu-id="aa31e-131">Mali yıl 12 aydan daha uzun veya daha kısa olabilir.</span><span class="sxs-lookup"><span data-stu-id="aa31e-131">The fiscal year can be longer or shorter than 12 months.</span></span> <span data-ttu-id="aa31e-132">Amortisman her dönem için ayarlanır.</span><span class="sxs-lookup"><span data-stu-id="aa31e-132">The depreciation is adjusted for each period.</span></span> <span data-ttu-id="aa31e-133">Bir sonraki mali yılın uzunluğu, **Mali takvimler** sayfasında ayarlanan mali dönemler tarafından belirlenir.</span><span class="sxs-lookup"><span data-stu-id="aa31e-133">The length of the next fiscal year is determined by the setup of periods on the **Fiscal calendars** page.</span></span> 

<span data-ttu-id="aa31e-134">Amortisman yılı olarak **Mali** seçildiğinde, **Dönem sıklığı** alanında şu seçenekler kullanılabilir:</span><span class="sxs-lookup"><span data-stu-id="aa31e-134">When **Fiscal** is selected as the depreciation year, the following options are available in the **Period frequency** field:</span></span>

-   <span data-ttu-id="aa31e-135">**Yıllık**, mali yıl için hesaplanan toplam amortisman tutarını tek tutar olarak, mali yılın son gününde nakleder.</span><span class="sxs-lookup"><span data-stu-id="aa31e-135">**Yearly** posts the total amount of the depreciation that is calculated for the fiscal year as one amount, on the last day of the fiscal year.</span></span>
-   <span data-ttu-id="aa31e-136">**Mali dönem**, mali yıl için hesaplanan toplam amortisman tutarını nakleder.</span><span class="sxs-lookup"><span data-stu-id="aa31e-136">**Fiscal period** posts the total amount of the depreciation that is calculated for the fiscal year.</span></span> <span data-ttu-id="aa31e-137">Bu tutar, **Mali Takvimler** sayfası üzerinde tanımlanan mali dönemlere tahakkuk edilir.</span><span class="sxs-lookup"><span data-stu-id="aa31e-137">This amount is accrued into the fiscal periods that are defined on the **Fiscal calendars** page.</span></span>

## <a name="example-of-200-reducing-balance-depreciation"></a><span data-ttu-id="aa31e-138">%200 azalan bakiyeli amortisman örneği</span><span class="sxs-lookup"><span data-stu-id="aa31e-138">Example of 200% reducing balance depreciation</span></span>

|                                |        |
|--------------------------------|--------|
| <span data-ttu-id="aa31e-139">Alım maliyeti</span><span class="sxs-lookup"><span data-stu-id="aa31e-139">Acquisition cost</span></span>               | <span data-ttu-id="aa31e-140">11.000</span><span class="sxs-lookup"><span data-stu-id="aa31e-140">11,000</span></span> |
| <span data-ttu-id="aa31e-141">Hurda değeri</span><span class="sxs-lookup"><span data-stu-id="aa31e-141">Salvage value</span></span>                  | <span data-ttu-id="aa31e-142">1.000</span><span class="sxs-lookup"><span data-stu-id="aa31e-142">1, 000</span></span> |
| <span data-ttu-id="aa31e-143">Amortisman tabanı</span><span class="sxs-lookup"><span data-stu-id="aa31e-143">Depreciation base</span></span>              | <span data-ttu-id="aa31e-144">10.000</span><span class="sxs-lookup"><span data-stu-id="aa31e-144">10,000</span></span> |
| <span data-ttu-id="aa31e-145">Servis ömrü yıl sayısı</span><span class="sxs-lookup"><span data-stu-id="aa31e-145">Service life years</span></span>             | <span data-ttu-id="aa31e-146">5</span><span class="sxs-lookup"><span data-stu-id="aa31e-146">5</span></span>      |
| <span data-ttu-id="aa31e-147">Yıllık amortisman yüzdesi</span><span class="sxs-lookup"><span data-stu-id="aa31e-147">Yearly depreciation percentage</span></span> | <span data-ttu-id="aa31e-148">%40</span><span class="sxs-lookup"><span data-stu-id="aa31e-148">40%</span></span>    |

<span data-ttu-id="aa31e-149">%200 azalan bakiye yöntemi, yüzde 200'ü servis ömrü yıl sayısına böler.</span><span class="sxs-lookup"><span data-stu-id="aa31e-149">The 200% reducing balance method divides 200 percent by the service life years.</span></span> <span data-ttu-id="aa31e-150">Elde edilen yüzde, yıla ait amortisman tutarını belirlemek üzere, sabit kıymetin net defter değeriyle çarpılacaktır.</span><span class="sxs-lookup"><span data-stu-id="aa31e-150">That percentage will be multiplied by the net book value of the asset to determine the depreciation amount for the year.</span></span>

| <span data-ttu-id="aa31e-151">Dönem</span><span class="sxs-lookup"><span data-stu-id="aa31e-151">Period</span></span> | <span data-ttu-id="aa31e-152">Yıllık amortisman miktarının hesaplaması</span><span class="sxs-lookup"><span data-stu-id="aa31e-152">Calculation of the yearly depreciation amount</span></span> | <span data-ttu-id="aa31e-153">Defter değeri</span><span class="sxs-lookup"><span data-stu-id="aa31e-153">Book value</span></span>             | <span data-ttu-id="aa31e-154">Yıl sonunda net defter değeri</span><span class="sxs-lookup"><span data-stu-id="aa31e-154">Net book value at the end of the year</span></span> |
|--------|-----------------------------------------------|------------------------|---------------------------------------|
| <span data-ttu-id="aa31e-155">Yıl 1</span><span class="sxs-lookup"><span data-stu-id="aa31e-155">Year 1</span></span> | <span data-ttu-id="aa31e-156">(11.000 – 1.000) × %40 = 4.000</span><span class="sxs-lookup"><span data-stu-id="aa31e-156">(11,000 – 1,000) × 40% = 4,000</span></span>                | <span data-ttu-id="aa31e-157">11.000 – 4.000 = 7.000</span><span class="sxs-lookup"><span data-stu-id="aa31e-157">11,000 – 4,000 = 7,000</span></span> | <span data-ttu-id="aa31e-158">11.000 – 1.000 – 4.000 = 6.000</span><span class="sxs-lookup"><span data-stu-id="aa31e-158">11,000 – 1,000 – 4,000 = 6,000</span></span>        |
| <span data-ttu-id="aa31e-159">2. yıl</span><span class="sxs-lookup"><span data-stu-id="aa31e-159">Year 2</span></span> | <span data-ttu-id="aa31e-160">6.000 × %40 = 2.400</span><span class="sxs-lookup"><span data-stu-id="aa31e-160">6,000 × 40% = 2,400</span></span>                           | <span data-ttu-id="aa31e-161">7.000 – 2.400 = 4.600</span><span class="sxs-lookup"><span data-stu-id="aa31e-161">7,000 – 2,400 = 4,600</span></span>  | <span data-ttu-id="aa31e-162">6.000 – 2.400 = 3.600</span><span class="sxs-lookup"><span data-stu-id="aa31e-162">6,000 – 2,400 = 3,600</span></span>                 |
| <span data-ttu-id="aa31e-163">3. yıl</span><span class="sxs-lookup"><span data-stu-id="aa31e-163">Year 3</span></span> | <span data-ttu-id="aa31e-164">3.600 × %40 = 1.440</span><span class="sxs-lookup"><span data-stu-id="aa31e-164">3,600 × 40% = 1,440</span></span>                           | <span data-ttu-id="aa31e-165">4.600 – 1.440 = 3.160</span><span class="sxs-lookup"><span data-stu-id="aa31e-165">4,600 – 1,440 = 3,160</span></span>  | <span data-ttu-id="aa31e-166">3.600 – 1.440 = 2.160</span><span class="sxs-lookup"><span data-stu-id="aa31e-166">3,600 – 1,440 = 2,160</span></span>                 |

> [!NOTE] 
> <span data-ttu-id="aa31e-167">Tipik olarak, %200 azalan bakiye amortismanı yöntemi kullanılarak hesaplanan tutar sabit amortisman yöntemi kullanılarak hesaplanacak yöntemden daha az olduğunda, kalan ömür için sabit amortisman yöntemine bir dönüş olur.</span><span class="sxs-lookup"><span data-stu-id="aa31e-167">Typically, when the amount that is calculated by using the 200% reducing balance depreciation method becomes less than the amount that would be calculated by using the straight line method, there is a conversion to the straight line method for the remaining life.</span></span>



