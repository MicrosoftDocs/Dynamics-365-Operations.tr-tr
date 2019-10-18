---
title: Yüzde 175 azalan bakiyeli amortisman
description: Bu konu, amortismanın yüzde 175 azalan bakiye yöntemi hakkında genel bir bakış sağlar.
author: saraschi2
manager: AnnBe
ms.date: 10/30/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetDepreciationProfile
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 13911
ms.assetid: cc5d001f-bcfe-4602-9ec1-9e265e9fd188
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 3a21c315aa9a7193c20e4184da20d4d6d38386c4
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/27/2019
ms.locfileid: "2180330"
---
# <a name="175-percent-reducing-balance-depreciation"></a><span data-ttu-id="c33cf-103">Yüzde 175 azalan bakiyeli amortisman</span><span class="sxs-lookup"><span data-stu-id="c33cf-103">175 percent reducing balance depreciation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c33cf-104">Bu konu, amortismanın yüzde 175 azalan bakiye yöntemi hakkında genel bir bakış sağlar.</span><span class="sxs-lookup"><span data-stu-id="c33cf-104">This topic gives an overview of the 175 percent reducing balance method of depreciation.</span></span>

<span data-ttu-id="c33cf-105">Bir sabit kıymet amortisman profili ayarlayıp **Amortisman profilleri** sayfasındaki **Yöntem** alanında **%175 azalan bakiye** seçeneğini belirlediğinizde, amortisman profiline atanan sabit kıymetlerin amortismanı her amortisman döneminde aynı yüzdeyi içerir.</span><span class="sxs-lookup"><span data-stu-id="c33cf-105">When you set up a fixed asset depreciation profile and select **175% reducing balance** in the **Method** field on the **Depreciation profiles** page, fixed assets that are assigned the depreciation profile are depreciated by the same percentage in each depreciation period.</span></span> 

<span data-ttu-id="c33cf-106">%175 azalan bakiyeli amortisman ayarlamak için, **Amortisman profilleri** sayfasında **Amortisman yılı** alanı ve **Dönem sıklığı** alanındaki seçenekleri de belirlemeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="c33cf-106">To set up 175% reducing balance depreciation, you must also select options in the **Depreciation year** field and the **Period frequency** field on the **Depreciation profiles** page.</span></span> <span data-ttu-id="c33cf-107">**Dönem sıklığı** alanındaki kullanılabilir seçenekler, **Amortisman yılı** alanında seçili değere bağlı olarak değişir.</span><span class="sxs-lookup"><span data-stu-id="c33cf-107">The options that are available in the **Period frequency** field vary, depending on the value that is selected in the **Depreciation year** field.</span></span>

## <a name="select-a-depreciation-year"></a><span data-ttu-id="c33cf-108">Bir amortisman yılı seçin</span><span class="sxs-lookup"><span data-stu-id="c33cf-108">Select a depreciation year</span></span>
<span data-ttu-id="c33cf-109">**Amortisman profilleri** sayasındaki **Amortisman yılı** alanından **Takvim** Yılı veya **Mali** Yıl seçimi yapabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="c33cf-109">You can select either **Calendar** or **Fiscal** in the **Depreciation year** field on the **Depreciation profiles** page.</span></span> <span data-ttu-id="c33cf-110">Varsayılan değer **Takvim** seçeneğidir.</span><span class="sxs-lookup"><span data-stu-id="c33cf-110">The default value is **Calendar**.</span></span> 

<span data-ttu-id="c33cf-111">Seçiminiz, **Dönem sıklığı** alanında bulunan seçenekleri belirler.</span><span class="sxs-lookup"><span data-stu-id="c33cf-111">Your selection determines the options that are available in the **Period frequency** field.</span></span> <span data-ttu-id="c33cf-112">Bu alan, amortisman tahakkuk deftere nakil tarihlerini ve tutarlarını takvim yılı boyunca tanımlar.</span><span class="sxs-lookup"><span data-stu-id="c33cf-112">This field defines the depreciation accrual posting dates and amounts throughout the calendar year.</span></span>

### <a name="calendar"></a><span data-ttu-id="c33cf-113">Takvim</span><span class="sxs-lookup"><span data-stu-id="c33cf-113">Calendar</span></span>

<span data-ttu-id="c33cf-114">**Amortisman yılı** alanında varsayılan değer olan **Takvim** seçeneğini bırakabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="c33cf-114">You can keep the default value in the **Depreciation year** field, **Calendar**.</span></span> 

<span data-ttu-id="c33cf-115">**Takvim** seçeneği, amortisman tabanını her yılın Ocak 1 tarihinde günceller.</span><span class="sxs-lookup"><span data-stu-id="c33cf-115">The **Calendar** option updates the depreciation base on January 1 of each year.</span></span> <span data-ttu-id="c33cf-116">Tipik olarak, amortisman tabanı, net defter değeri eksi ıskarta değeridir.</span><span class="sxs-lookup"><span data-stu-id="c33cf-116">Typically, the depreciation base is the net book value minus the scrap value.</span></span> <span data-ttu-id="c33cf-117">Bu konunun devamındaki örneklerde, amortisman tabanı hesaplamalar sütunundaki yer alan ilk ifadedeki pay olur.</span><span class="sxs-lookup"><span data-stu-id="c33cf-117">In the examples later in this topic, the depreciation base is the numerator in the first expression in the calculations column.</span></span> 

<span data-ttu-id="c33cf-118">Amortisman yılı olarak **Takvim** seçerseniz, **Dönem sıklığı** alanında şu seçenekler kullanılabilir :</span><span class="sxs-lookup"><span data-stu-id="c33cf-118">If you select **Calendar** as the depreciation year, the following options are available in the **Period frequency** field:</span></span>

-   <span data-ttu-id="c33cf-119">**Yıllık** 31 Aralık'ta bir tutarı nakleder.</span><span class="sxs-lookup"><span data-stu-id="c33cf-119">**Yearly** posts an amount on December 31.</span></span>
-   <span data-ttu-id="c33cf-120">**Aylık** seçeneği her takvim ayının sonunda bir aylık tutarı nakleder.</span><span class="sxs-lookup"><span data-stu-id="c33cf-120">**Monthly** posts a monthly amount at the end of each calendar month.</span></span>
-   <span data-ttu-id="c33cf-121">**Üç aylık** seçeneği, üç aylık takvim döneminin sonunda (31 Mart, 30 Haziran, 30 Eylül ve 31 Aralık) bir üç aylık tutar nakleder.</span><span class="sxs-lookup"><span data-stu-id="c33cf-121">**Quarterly** posts a quarterly amount at the end of each calendar quarter (March 31, June 30, September 30, and December 31).</span></span>
-   <span data-ttu-id="c33cf-122">**Yarı yıllık** seçeneği takvim yarı yılında ( 30 Haziran ve 31 Aralık) yarı yıllık tutarı nakleder.</span><span class="sxs-lookup"><span data-stu-id="c33cf-122">**Half-Yearly** posts a half-yearly amount at the calendar half year (June 30 and December 31).</span></span>
-   <span data-ttu-id="c33cf-123">**Günlük** seçeneği her gün için bir işlem kullanarak günlük amortisman yöntemi için amortisman tutarını nakleder.</span><span class="sxs-lookup"><span data-stu-id="c33cf-123">**Daily** posts the depreciation amount for the daily depreciation method by using one transaction for each day.</span></span>

### <a name="fiscal"></a><span data-ttu-id="c33cf-124">Mali</span><span class="sxs-lookup"><span data-stu-id="c33cf-124">Fiscal</span></span>

<span data-ttu-id="c33cf-125">**Amortisman yılı** alanında **Mali** seçeneğini belirlerseniz, %175 azalan bakiyeli amortisman defter için belirtilen mali takvim için veya **Genel muhasebe** sayfasında seçilen mali takvim için mali yıla dayalı olarak hesaplanır.</span><span class="sxs-lookup"><span data-stu-id="c33cf-125">If you select **Fiscal** in the **Depreciation year** field, 175% reducing balance depreciation is calculated based on the fiscal year for the fiscal calendar that is specified for the book, or for the fiscal calendar that is selected on the **Ledger** page.</span></span> <span data-ttu-id="c33cf-126">Mali takvimler, **Mali Takvimler** sayfasında ayarlanır.</span><span class="sxs-lookup"><span data-stu-id="c33cf-126">Fiscal calendars are set up on the **Fiscal calendars** page.</span></span> <span data-ttu-id="c33cf-127">Daha fazla bilgi için bkz. [Mali takvimler, mali yıllar ve dönemler](../budgeting/fiscal-calendars-fiscal-years-periods.md).</span><span class="sxs-lookup"><span data-stu-id="c33cf-127">For more information, see [Fiscal calendars, fiscal years, and periods](../budgeting/fiscal-calendars-fiscal-years-periods.md).</span></span>

<span data-ttu-id="c33cf-128">Örneğin, 1 Temmuz ile 30 Haziran arasındaki mali yıl için amortisman hesaplaması 1 Temmuz'da başlar.</span><span class="sxs-lookup"><span data-stu-id="c33cf-128">For example, for the fiscal year July 1 through June 30, the depreciation calculation starts on July 1.</span></span> <span data-ttu-id="c33cf-129">Mali yıl 12 aydan daha uzun veya daha kısa olabilir.</span><span class="sxs-lookup"><span data-stu-id="c33cf-129">The fiscal year can be longer or shorter than 12 months.</span></span> <span data-ttu-id="c33cf-130">Amortisman, her mali dönem için otomatik olarak düzeltilir ve bir sonraki mali yılın uzunluğu, **Mali takvimler** sayfasındaki dönem ayarları tarafından belirlenir.</span><span class="sxs-lookup"><span data-stu-id="c33cf-130">The depreciation is automatically adjusted for each period, and the length of the next fiscal year is determined by the setup of periods on the **Fiscal calendars** page.</span></span> 

<span data-ttu-id="c33cf-131">Amortisman yılı olarak **Mali** seçerseniz, **Dönem sıklığı** alanında şu seçenekler kullanılabilir:</span><span class="sxs-lookup"><span data-stu-id="c33cf-131">If you select **Fiscal** as the depreciation year, the following options are available in the **Period frequency** field:</span></span>

-   <span data-ttu-id="c33cf-132">**Yıllık** seçeneği, mali yıl için hesaplanan toplam amortisman tutarını, mali yılın son gününde nakleder.</span><span class="sxs-lookup"><span data-stu-id="c33cf-132">**Yearly** posts the total amount of the depreciation that is calculated for the fiscal year on the last day of the fiscal year.</span></span>
-   <span data-ttu-id="c33cf-133">**Mali dönem** seçeneği, mali yılın amortismanının toplam tutarını hesaplar.</span><span class="sxs-lookup"><span data-stu-id="c33cf-133">**Fiscal period** calculates the total amount of the depreciation for the fiscal year.</span></span> <span data-ttu-id="c33cf-134">Bu tutar, **Mali Takvimler** sayfası üzerinde tanımlanan mali dönemlere tahakkuk edilir.</span><span class="sxs-lookup"><span data-stu-id="c33cf-134">This amount is accrued into the fiscal periods that are defined on the **Fiscal calendars** page.</span></span>

## <a name="example-of-175-reducing-balance-depreciation"></a><span data-ttu-id="c33cf-135">%175 azalan bakiyeli amortisman örneği</span><span class="sxs-lookup"><span data-stu-id="c33cf-135">Example of 175% reducing balance depreciation</span></span>

|                                |        |
|--------------------------------|--------|
| <span data-ttu-id="c33cf-136">Alım maliyeti</span><span class="sxs-lookup"><span data-stu-id="c33cf-136">Acquisition cost</span></span>               | <span data-ttu-id="c33cf-137">11.000</span><span class="sxs-lookup"><span data-stu-id="c33cf-137">11,000</span></span> |
| <span data-ttu-id="c33cf-138">Hurda değeri</span><span class="sxs-lookup"><span data-stu-id="c33cf-138">Salvage value</span></span>                  | <span data-ttu-id="c33cf-139">1.000</span><span class="sxs-lookup"><span data-stu-id="c33cf-139">1,000</span></span>  |
| <span data-ttu-id="c33cf-140">Amortisman tabanı</span><span class="sxs-lookup"><span data-stu-id="c33cf-140">Depreciation base</span></span>              | <span data-ttu-id="c33cf-141">10.000</span><span class="sxs-lookup"><span data-stu-id="c33cf-141">10,000</span></span> |
| <span data-ttu-id="c33cf-142">Servis ömrü yıl sayısı</span><span class="sxs-lookup"><span data-stu-id="c33cf-142">Service life years</span></span>             | <span data-ttu-id="c33cf-143">5</span><span class="sxs-lookup"><span data-stu-id="c33cf-143">5</span></span>      |
| <span data-ttu-id="c33cf-144">Yıllık amortisman yüzdesi</span><span class="sxs-lookup"><span data-stu-id="c33cf-144">Yearly depreciation percentage</span></span> | <span data-ttu-id="c33cf-145">%35</span><span class="sxs-lookup"><span data-stu-id="c33cf-145">35%</span></span>    |

<span data-ttu-id="c33cf-146">%175 azalan amortisman yöntemi, yüzde 175'ü servis ömrü yıl sayısına böler.</span><span class="sxs-lookup"><span data-stu-id="c33cf-146">The 175% reducing balance depreciation method divides 175 percent by the service life years.</span></span> <span data-ttu-id="c33cf-147">Elde edilen yüzde, yıla ait amortisman tutarını belirlemek üzere, sabit kıymetin net defter değeriyle çarpılacaktır.</span><span class="sxs-lookup"><span data-stu-id="c33cf-147">That percentage will be multiplied by the net book value of the asset to determine the depreciation amount for the year.</span></span>

| <span data-ttu-id="c33cf-148">Dönem</span><span class="sxs-lookup"><span data-stu-id="c33cf-148">Period</span></span> | <span data-ttu-id="c33cf-149">Yıllık amortisman miktarının hesaplaması</span><span class="sxs-lookup"><span data-stu-id="c33cf-149">Calculation of the yearly depreciation amount</span></span> | <span data-ttu-id="c33cf-150">Defter değeri</span><span class="sxs-lookup"><span data-stu-id="c33cf-150">Book value</span></span>                  | <span data-ttu-id="c33cf-151">Yıl sonunda net defter değeri</span><span class="sxs-lookup"><span data-stu-id="c33cf-151">Net book value at the end of the year</span></span> |
|--------|-----------------------------------------------|-----------------------------|---------------------------------------|
| <span data-ttu-id="c33cf-152">Yıl 1</span><span class="sxs-lookup"><span data-stu-id="c33cf-152">Year 1</span></span> | <span data-ttu-id="c33cf-153">(11.000 – 1.000) × %35 = 3.500</span><span class="sxs-lookup"><span data-stu-id="c33cf-153">(11,000 – 1,000) × 35% = 3,500</span></span>                | <span data-ttu-id="c33cf-154">11.000 - 3.500 = 7.500</span><span class="sxs-lookup"><span data-stu-id="c33cf-154">11,000 – 3,500 = 7,500</span></span>      | <span data-ttu-id="c33cf-155">11.000 – 1.000 – 3.500 = 6.500</span><span class="sxs-lookup"><span data-stu-id="c33cf-155">11,000 – 1,000 – 3,500 = 6,500</span></span>        |
| <span data-ttu-id="c33cf-156">2. yıl</span><span class="sxs-lookup"><span data-stu-id="c33cf-156">Year 2</span></span> | <span data-ttu-id="c33cf-157">6.500 × %35 = 2.275</span><span class="sxs-lookup"><span data-stu-id="c33cf-157">6,500 × 35% = 2,275</span></span>                           | <span data-ttu-id="c33cf-158">7.500 - 2.275 = 5.225</span><span class="sxs-lookup"><span data-stu-id="c33cf-158">7,500 – 2,275 = 5,225</span></span>       | <span data-ttu-id="c33cf-159">6.500 - 2.275 = 4.225</span><span class="sxs-lookup"><span data-stu-id="c33cf-159">6,500 – 2,275 = 4,225</span></span>                 |
| <span data-ttu-id="c33cf-160">3. yıl</span><span class="sxs-lookup"><span data-stu-id="c33cf-160">Year 3</span></span> | <span data-ttu-id="c33cf-161">4.225 × %35 = 1.478,75</span><span class="sxs-lookup"><span data-stu-id="c33cf-161">4,225 × 35% = 1,478.75</span></span>                        | <span data-ttu-id="c33cf-162">5.225 - 1.478,75 = 3.746,25</span><span class="sxs-lookup"><span data-stu-id="c33cf-162">5,225 – 1,478.75 = 3,746.25</span></span> | <span data-ttu-id="c33cf-163">4.225 - 1.478,75 = 2.746,25</span><span class="sxs-lookup"><span data-stu-id="c33cf-163">4,225 – 1,478.75 = 2,746.25</span></span>           |

> [!NOTE] 
> <span data-ttu-id="c33cf-164">Tipik olarak, %175 azalan bakiye amortismanı yöntemi kullanılarak hesaplanan tutar sabit amortisman yöntemi kullanılarak hesaplanacak yöntemden daha az olduğunda, kalan ömür için sabit amortisman yöntemine bir dönüş olur.</span><span class="sxs-lookup"><span data-stu-id="c33cf-164">Typically, when the amount that is calculated by using the 175% reducing balance depreciation method becomes less than the amount that would be calculated by using the straight line method, there is a conversion to the straight line method for the remaining life.</span></span>



