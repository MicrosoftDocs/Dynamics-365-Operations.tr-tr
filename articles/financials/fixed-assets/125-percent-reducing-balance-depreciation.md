---
title: Yüzde 125 azalan bakiyeli amortisman
description: Bu makale, amortismanın Yüzde 125 Azalan bakiye yöntemi hakkında genel bir bakış sağlar.
author: saraschi2
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetDepreciationProfile
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 13871
ms.assetid: 3abc263e-59d6-4f1a-986d-1be388948bd3
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f7af5413376a98c3b2b7ded46c757c9156a3fadf
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/15/2019
ms.locfileid: "1555708"
---
# <a name="125-percent-reducing-balance-depreciation"></a><span data-ttu-id="ce72d-103">Yüzde 125 azalan bakiyeli amortisman</span><span class="sxs-lookup"><span data-stu-id="ce72d-103">125 percent reducing balance depreciation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ce72d-104">Bu makale, amortismanın Yüzde 125 Azalan bakiye yöntemi hakkında genel bir bakış sağlar.</span><span class="sxs-lookup"><span data-stu-id="ce72d-104">This article gives an overview of the 125 percent reducing balance method of depreciation.</span></span>

<span data-ttu-id="ce72d-105">Bir sabit kıymet amortisman profili ayarlayıp **Amortisman profilleri** sayfasındaki **Yöntem** alanında **%125 azalan bakiye** seçeneğini belirlediğinizde, amortisman profiline atanan sabit kıymetlerin amortismanı her amortisman döneminde aynı yüzdeyi içerir.</span><span class="sxs-lookup"><span data-stu-id="ce72d-105">When you set up a fixed asset depreciation profile and select **125% reducing balance** in the **Method** field on the **Depreciation profiles** page, fixed assets that are assigned to the depreciation profile are depreciated by the same percentage in each depreciation period.</span></span> <span data-ttu-id="ce72d-106">Bu yüzde, sabit kıymetin servis ömrü temel alınarak hesaplanır.</span><span class="sxs-lookup"><span data-stu-id="ce72d-106">This percentage is calculated based on the service life of the asset.</span></span> <span data-ttu-id="ce72d-107">Örneğin, bir sabit kıymetin beş yıllık servis ömrü varsa, yüzde 25 (%125 ÷ 5) olarak hesaplanır.</span><span class="sxs-lookup"><span data-stu-id="ce72d-107">For example, if an asset has a service life of five years, the percentage is calculated as 25 percent (125% ÷ 5).</span></span>

<span data-ttu-id="ce72d-108">%125 azalan bakiyeli amortisman ayarlamak için, **Amortisman profilleri** sayfasında **Amortisman yılı** alanı ve **Dönem sıklığı** alanındaki seçenekleri de belirlemeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="ce72d-108">To set up 125% reducing balance depreciation, you must also select options in the **Depreciation year** field and the **Period frequency** field on the **Depreciation profiles** page.</span></span> <span data-ttu-id="ce72d-109">**Dönem sıklığı** alanındaki kullanılabilir seçenekler, **Amortisman yılı** alanında seçili değere bağlı olarak değişir.</span><span class="sxs-lookup"><span data-stu-id="ce72d-109">The options that are available in the **Period frequency** field vary, depending on the value that is selected in the **Depreciation year** field.</span></span>

## <a name="select-a-depreciation-year"></a><span data-ttu-id="ce72d-110">Bir amortisman yılı seçin</span><span class="sxs-lookup"><span data-stu-id="ce72d-110">Select a depreciation year</span></span>
<span data-ttu-id="ce72d-111">**Amortisman profilleri** sayasındaki **Amortisman yılı** alanından **Takvim** Yılı veya **Mali** Yıl seçimi yapabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="ce72d-111">You can select either **Calendar** or **Fiscal** in the **Depreciation year** field on the **Depreciation profiles** page.</span></span> <span data-ttu-id="ce72d-112">Varsayılan değer **Takvim** seçeneğidir.</span><span class="sxs-lookup"><span data-stu-id="ce72d-112">The default value is **Calendar**.</span></span> 

<span data-ttu-id="ce72d-113">Seçiminiz, **Dönem sıklığı** alanında bulunan seçenekleri belirler.</span><span class="sxs-lookup"><span data-stu-id="ce72d-113">Your selection determines the options that are available in the **Period frequency** field.</span></span> <span data-ttu-id="ce72d-114">Bu alan, amortisman tahakkuk deftere nakil tarihlerini ve tutarlarını takvim yılı boyunca tanımlar.</span><span class="sxs-lookup"><span data-stu-id="ce72d-114">This field defines the depreciation accrual posting dates and amounts throughout the calendar year.</span></span>

### <a name="calendar"></a><span data-ttu-id="ce72d-115">Takvim</span><span class="sxs-lookup"><span data-stu-id="ce72d-115">Calendar</span></span>

<span data-ttu-id="ce72d-116">**Amortisman yılı** alanında varsayılan değer olan **Takvim** seçeneğini bırakabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="ce72d-116">You can keep the default value in the **Depreciation year** field, **Calendar**.</span></span> 

<span data-ttu-id="ce72d-117">**Takvim** seçeneği, amortisman tabanını her yılın Ocak 1 tarihinde günceller.</span><span class="sxs-lookup"><span data-stu-id="ce72d-117">The **Calendar** option updates the depreciation base on January 1 of each year.</span></span> <span data-ttu-id="ce72d-118">Tipik olarak, amortisman tabanı, net defter değeri eksi ıskarta değeridir.</span><span class="sxs-lookup"><span data-stu-id="ce72d-118">Typically, the depreciation base is the net book value minus the scrap value.</span></span> <span data-ttu-id="ce72d-119">Bu konunun devamındaki örneklerde, amortisman tabanı hesaplamalar sütunundaki yer alan ilk ifadedeki pay olur.</span><span class="sxs-lookup"><span data-stu-id="ce72d-119">In the examples later in this topic, the depreciation base is the numerator in the first expression in the calculations column.</span></span> 

<span data-ttu-id="ce72d-120">Amortisman yılı olarak **Takvim** seçerseniz, **Dönem sıklığı** alanında şu seçenekler kullanılabilir :</span><span class="sxs-lookup"><span data-stu-id="ce72d-120">If you select **Calendar** as the depreciation year, the following options are available in the **Period frequency** field:</span></span>

-   <span data-ttu-id="ce72d-121">**Yıllık** 31 Aralık'ta bir tutarı nakleder.</span><span class="sxs-lookup"><span data-stu-id="ce72d-121">**Yearly** posts an amount on December 31.</span></span>
-   <span data-ttu-id="ce72d-122">**Aylık** seçeneği her takvim ayının sonunda bir aylık tutarı nakleder.</span><span class="sxs-lookup"><span data-stu-id="ce72d-122">**Monthly** posts a monthly amount at the end of each calendar month.</span></span>
-   <span data-ttu-id="ce72d-123">**Üç aylık** seçeneği, üç aylık takvim döneminin sonunda (31 Mart, 30 Haziran, 30 Eylül ve 31 Aralık) bir üç aylık tutar nakleder.</span><span class="sxs-lookup"><span data-stu-id="ce72d-123">**Quarterly** posts a quarterly amount at the end of each calendar quarter (March 31, June 30, September 30, and December 31).</span></span>
-   <span data-ttu-id="ce72d-124">**Yarı yıllık** seçeneği takvim yarı yılında ( 30 Haziran ve 31 Aralık) yarı yıllık tutarı nakleder.</span><span class="sxs-lookup"><span data-stu-id="ce72d-124">**Half-Yearly** posts a half-yearly amount at the calendar half year (June 30 and December 31).</span></span>
-   <span data-ttu-id="ce72d-125">**Günlük** seçeneği her gün için bir işlem kullanarak günlük amortisman yöntemi için amortisman tutarını nakleder.</span><span class="sxs-lookup"><span data-stu-id="ce72d-125">**Daily** posts the depreciation amount for the daily depreciation method by using one transaction for each day.</span></span>

### <a name="fiscal"></a><span data-ttu-id="ce72d-126">Mali</span><span class="sxs-lookup"><span data-stu-id="ce72d-126">Fiscal</span></span>

<span data-ttu-id="ce72d-127">**Amortisman yılı** alanında **Mali** seçeneğini belirlerseniz, %125 azalan amortisman defter için belirtilen mali takvim için veya **Genel muhasebe** sayfasında seçilen mali takvim için mali yıla dayalı olarak hesaplanır.</span><span class="sxs-lookup"><span data-stu-id="ce72d-127">If you select **Fiscal** in the **Depreciation year** field, 125% reducing depreciation is calculated based on the fiscal year for the fiscal calendar that is specified for the book, or for the fiscal calendar that is selected on the **Ledger** page.</span></span> <span data-ttu-id="ce72d-128">Mali takvimler, **Mali Takvimler** sayfasında ayarlanır.</span><span class="sxs-lookup"><span data-stu-id="ce72d-128">Fiscal calendars are set up on the **Fiscal calendars** page.</span></span> 

<span data-ttu-id="ce72d-129">Örneğin, 1 Temmuz ile 30 Haziran arasındaki mali yıl için amortisman hesaplaması 1 Temmuz'da başlar.</span><span class="sxs-lookup"><span data-stu-id="ce72d-129">For example, for the fiscal year July 1 through June 30, the depreciation calculation starts on July 1.</span></span> <span data-ttu-id="ce72d-130">Mali yıl 12 aydan daha uzun veya daha kısa olabilir.</span><span class="sxs-lookup"><span data-stu-id="ce72d-130">The fiscal year can be longer or shorter than 12 months.</span></span> <span data-ttu-id="ce72d-131">Amortisman, her mali dönem için otomatik olarak düzeltilir ve bir sonraki mali yılın uzunluğu, **Mali takvimler** sayfasındaki dönem ayarları tarafından belirlenir.</span><span class="sxs-lookup"><span data-stu-id="ce72d-131">The depreciation is automatically adjusted for each period, and the length of the next fiscal year is determined by the setup of periods on the **Fiscal calendars** page.</span></span> 

<span data-ttu-id="ce72d-132">Amortisman yılı olarak **Mali** seçerseniz, **Dönem sıklığı** alanında şu seçenekler kullanılabilir:</span><span class="sxs-lookup"><span data-stu-id="ce72d-132">If you select **Fiscal** as the depreciation year, the following options are available in the **Period frequency** field:</span></span>

-   <span data-ttu-id="ce72d-133">**Yıllık**, mali yıl için hesaplanan toplam amortisman tutarını tek tutar olarak, mali yılın son gününde nakleder.</span><span class="sxs-lookup"><span data-stu-id="ce72d-133">**Yearly** posts the total amount of the depreciation that is calculated for the fiscal year as one amount, on the last day of the fiscal year.</span></span>
-   <span data-ttu-id="ce72d-134">**Mali dönem**, mali yıl için hesaplanan toplam amortisman tutarını nakleder.</span><span class="sxs-lookup"><span data-stu-id="ce72d-134">**Fiscal period** posts the total amount of the depreciation that is calculated for the fiscal year.</span></span> <span data-ttu-id="ce72d-135">Bu tutar, **Mali Takvimler** sayfası üzerinde tanımlanan mali dönemlere tahakkuk edilir.</span><span class="sxs-lookup"><span data-stu-id="ce72d-135">This amount is accrued into the fiscal periods that are defined on the **Fiscal calendars** page.</span></span>

## <a name="example-of-125-reducing-balance-depreciation"></a><span data-ttu-id="ce72d-136">%125 azalan bakiyeli amortisman örneği</span><span class="sxs-lookup"><span data-stu-id="ce72d-136">Example of 125% reducing balance depreciation</span></span>

|                                |        |
|--------------------------------|--------|
| <span data-ttu-id="ce72d-137">Alım maliyeti</span><span class="sxs-lookup"><span data-stu-id="ce72d-137">Acquisition cost</span></span>               | <span data-ttu-id="ce72d-138">11.000</span><span class="sxs-lookup"><span data-stu-id="ce72d-138">11,000</span></span> |
| <span data-ttu-id="ce72d-139">Hurda değeri</span><span class="sxs-lookup"><span data-stu-id="ce72d-139">Salvage value</span></span>                  | <span data-ttu-id="ce72d-140">1.000</span><span class="sxs-lookup"><span data-stu-id="ce72d-140">1,000</span></span>  |
| <span data-ttu-id="ce72d-141">Amortisman tabanı</span><span class="sxs-lookup"><span data-stu-id="ce72d-141">Depreciation base</span></span>              | <span data-ttu-id="ce72d-142">10.000</span><span class="sxs-lookup"><span data-stu-id="ce72d-142">10,000</span></span> |
| <span data-ttu-id="ce72d-143">Servis ömrü yıl sayısı</span><span class="sxs-lookup"><span data-stu-id="ce72d-143">Service life years</span></span>             | <span data-ttu-id="ce72d-144">5</span><span class="sxs-lookup"><span data-stu-id="ce72d-144">5</span></span>      |
| <span data-ttu-id="ce72d-145">Yıllık amortisman yüzdesi</span><span class="sxs-lookup"><span data-stu-id="ce72d-145">Yearly depreciation percentage</span></span> | <span data-ttu-id="ce72d-146">% 25</span><span class="sxs-lookup"><span data-stu-id="ce72d-146">25%</span></span>    |

<span data-ttu-id="ce72d-147">%125 azalan bakiye yöntemi, yüzde 125'i servis ömrü yıl sayısına böler.</span><span class="sxs-lookup"><span data-stu-id="ce72d-147">The 125% reducing balance method divides 125 percent by the service life years.</span></span> <span data-ttu-id="ce72d-148">Elde edilen yüzde, yıla ait amortisman tutarını belirlemek üzere, sabit kıymetin net defter değeriyle çarpılacaktır.</span><span class="sxs-lookup"><span data-stu-id="ce72d-148">That percentage will be multiplied by the net book value of the asset to determine the depreciation amount for the year.</span></span>

| <span data-ttu-id="ce72d-149">Dönem</span><span class="sxs-lookup"><span data-stu-id="ce72d-149">Period</span></span> | <span data-ttu-id="ce72d-150">Yıllık amortisman miktarının hesaplaması</span><span class="sxs-lookup"><span data-stu-id="ce72d-150">Calculation of the yearly depreciation amount</span></span> | <span data-ttu-id="ce72d-151">Defter değeri</span><span class="sxs-lookup"><span data-stu-id="ce72d-151">Book value</span></span>                    | <span data-ttu-id="ce72d-152">Yıl sonunda net defter değeri</span><span class="sxs-lookup"><span data-stu-id="ce72d-152">Net book value at the end of the year</span></span> |
|--------|-----------------------------------------------|-------------------------------|---------------------------------------|
| <span data-ttu-id="ce72d-153">Yıl 1</span><span class="sxs-lookup"><span data-stu-id="ce72d-153">Year 1</span></span> | <span data-ttu-id="ce72d-154">(11.000 – 1.000) × %25 = 2.500</span><span class="sxs-lookup"><span data-stu-id="ce72d-154">(11,000 – 1,000) × 25% = 2,500</span></span>                | <span data-ttu-id="ce72d-155">(11.000 – 2.500) = 8.500</span><span class="sxs-lookup"><span data-stu-id="ce72d-155">(11,000 – 2,500) = 8,500</span></span>      | <span data-ttu-id="ce72d-156">(11.000 – 1.000 – 2.500) = 7.500</span><span class="sxs-lookup"><span data-stu-id="ce72d-156">(11,000 – 1,000 – 2,500) = 7,500</span></span>      |
| <span data-ttu-id="ce72d-157">2. yıl</span><span class="sxs-lookup"><span data-stu-id="ce72d-157">Year 2</span></span> | <span data-ttu-id="ce72d-158">7.500 × %25 = 1.875</span><span class="sxs-lookup"><span data-stu-id="ce72d-158">7,500 × 25% = 1,875</span></span>                           | <span data-ttu-id="ce72d-159">(8.500 – 1.875) = 6.625</span><span class="sxs-lookup"><span data-stu-id="ce72d-159">(8,500 – 1,875) = 6,625</span></span>       | <span data-ttu-id="ce72d-160">(7.500 – 1.875) = 5.625</span><span class="sxs-lookup"><span data-stu-id="ce72d-160">(7,500 – 1,875) = 5,625</span></span>               |
| <span data-ttu-id="ce72d-161">3. yıl</span><span class="sxs-lookup"><span data-stu-id="ce72d-161">Year 3</span></span> | <span data-ttu-id="ce72d-162">5.625 × %25 = 1.406,25</span><span class="sxs-lookup"><span data-stu-id="ce72d-162">5,625 × 25% = 1,406.25</span></span>                        | <span data-ttu-id="ce72d-163">(6.625 – 1.406,25) = 5.218,75</span><span class="sxs-lookup"><span data-stu-id="ce72d-163">(6,625 – 1,406.25) = 5,218.75</span></span> | <span data-ttu-id="ce72d-164">(5.625 – 1.406,25) = 4.218,75</span><span class="sxs-lookup"><span data-stu-id="ce72d-164">(5,625 – 1,406.25) = 4,218.75</span></span>         |

> [!NOTE] 
> <span data-ttu-id="ce72d-165">Tipik olarak, %125 azalan bakiye amortismanı yöntemi kullanılarak hesaplanan tutar sabit amortisman yöntemi kullanılarak hesaplanacak yöntemden daha az olduğunda, kalan ömür için sabit amortisman yöntemine bir dönüş olur.</span><span class="sxs-lookup"><span data-stu-id="ce72d-165">Typically, when the amount that is calculated by using the 125% reducing balance depreciation method becomes less than the amount that would be calculated by using the straight line method, there is a conversion to the straight line method for the remaining life.</span></span>



