---
title: Sabit kalan ömür amortismanı
description: Bu makale, amortismanın Sabit kalan ömür yöntemi hakkında genel bir bakış sağlar.
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
ms.custom: 13851
ms.assetid: 0fa2f71a-596c-414c-a6e6-8f7405a0bf81
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 823b2569670adfbf04038abca656e34f0199fce1
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5210107"
---
# <a name="straight-line-life-remaining-depreciation"></a><span data-ttu-id="43c4b-103">Sabit kalan ömür amortismanı</span><span class="sxs-lookup"><span data-stu-id="43c4b-103">Straight line life remaining depreciation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="43c4b-104">Bu makale, amortismanın Sabit kalan ömür yöntemi hakkında genel bir bakış sağlar.</span><span class="sxs-lookup"><span data-stu-id="43c4b-104">This article gives an overview of the Straight line life remaining method of depreciation.</span></span>

<span data-ttu-id="43c4b-105">Bir sabit kıymek amortisman profili ayarladığınızda ve **Amortisman profilleri** sayfasındaki **Yöntem** alanından **Kalan düz çizgi yaşamı** öğesini seçtiğinizde amortisman profiline atanan sabit kıymetlerin amortismanı kıymetin kalan hizmet ömrüne dayalı olacaktır.</span><span class="sxs-lookup"><span data-stu-id="43c4b-105">When you set up a fixed asset depreciation profile and select **Straight line life remaining** in the **Method** field on the **Depreciation profiles** page, the depreciation of fixed assets that are assigned to the depreciation profile is based on the remaining service life of the asset.</span></span> <span data-ttu-id="43c4b-106">Amortisman tutarı genellikle her amortisman döneminde aynı olur.</span><span class="sxs-lookup"><span data-stu-id="43c4b-106">The depreciation amount is generally the same in each depreciation period.</span></span> <span data-ttu-id="43c4b-107">Düz çizgi kalan ömür amortismanı ayarlamak için, **Amortisman profilleri** sayfasında **Amortisman yılı** alanı ve **Dönem sıklığı** alanındaki seçenekleri de belirlemeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="43c4b-107">To set up straight line life remaining depreciation, you also must select options in the **Depreciation year** field and the **Period frequency** field on the **Depreciation profiles** page.</span></span> <span data-ttu-id="43c4b-108">**Dönem sıklığı** alanındaki kullanılabilir seçenekler, **Amortisman yılı** alanında seçili değere bağlı olarak değişir.</span><span class="sxs-lookup"><span data-stu-id="43c4b-108">The options that are available in the **Period frequency** field vary, depending on the value that is selected in the **Depreciation year** field.</span></span>

## <a name="select-a-depreciation-year"></a><span data-ttu-id="43c4b-109">Bir amortisman yılı seçin</span><span class="sxs-lookup"><span data-stu-id="43c4b-109">Select a depreciation year</span></span>
<span data-ttu-id="43c4b-110">**Amortisman profilleri** sayasındaki **Amortisman yılı** alanından **Takvim** Yılı veya **Mali** Yıl seçimi yapabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="43c4b-110">You can select either **Calendar** or **Fiscal** in the **Depreciation year** field on the **Depreciation profiles** page.</span></span> <span data-ttu-id="43c4b-111">Varsayılan değer **Takvim** seçeneğidir.</span><span class="sxs-lookup"><span data-stu-id="43c4b-111">The default value is **Calendar**.</span></span> <span data-ttu-id="43c4b-112">Seçiminiz, **Dönem sıklığı** alanında bulunan seçenekleri belirler.</span><span class="sxs-lookup"><span data-stu-id="43c4b-112">Your selection determines the options that are available in the **Period frequency** field.</span></span> <span data-ttu-id="43c4b-113">Bu alan, amortisman tahakkuk deftere nakil tarihlerini ve tutarlarını takvim yılı boyunca tanımlar.</span><span class="sxs-lookup"><span data-stu-id="43c4b-113">This field defines the depreciation accrual posting dates and amounts throughout the calendar year.</span></span>

### <a name="calendar"></a><span data-ttu-id="43c4b-114">Takvim</span><span class="sxs-lookup"><span data-stu-id="43c4b-114">Calendar</span></span>

<span data-ttu-id="43c4b-115">**_Amortisman yılı_*alanında **Takvim**'i seçerseniz, mali takvimi farklı tanımlamış olsanız bile, 1 Ocak-31 Aralık arası bir yıl varsayılır. _\* Takvim*\* seçeneği, amortisman tabanını her yıl 1 Ocak 'ta güncelleştirilir.</span><span class="sxs-lookup"><span data-stu-id="43c4b-115">If you select **Calendar** in the **_Depreciation year_*_ field, a year of January 1 through December 31 is assumed, even if you've defined the fiscal calendar differently. The _\* Calendar*\* option updates the depreciation base on January 1 of each year.</span></span> <span data-ttu-id="43c4b-116">Tipik olarak, amortisman tabanı, net defter değeri eksi hurda değeridir.</span><span class="sxs-lookup"><span data-stu-id="43c4b-116">Typically, the depreciation base is the net book value minus the salvage value.</span></span> <span data-ttu-id="43c4b-117">Bu konunun devamındaki örnekte, amortisman tabanı hesaplamalar sütunundaki yer alan ilk ifadedeki pay olur.</span><span class="sxs-lookup"><span data-stu-id="43c4b-117">In the example later in this topic, the depreciation base is the numerator in the first expression in the calculations column.</span></span> <span data-ttu-id="43c4b-118">Amortisman yılı olarak **Takvim** seçerseniz, **Dönem sıklığı** alanında şu seçenekler kullanılabilir :</span><span class="sxs-lookup"><span data-stu-id="43c4b-118">If you select **Calendar** as the depreciation year, the following options are available in the **Period frequency** field:</span></span>

-   <span data-ttu-id="43c4b-119">**Yıllık** 31 Aralık'ta bir tutarı nakleder.</span><span class="sxs-lookup"><span data-stu-id="43c4b-119">**Yearly** posts an amount on December 31.</span></span>
-   <span data-ttu-id="43c4b-120">**Aylık** seçeneği her takvim ayının sonunda bir aylık tutarı nakleder.</span><span class="sxs-lookup"><span data-stu-id="43c4b-120">**Monthly** posts a monthly amount at the end of each calendar month.</span></span>
-   <span data-ttu-id="43c4b-121">**Üç aylık** seçeneği, üç aylık takvim döneminin sonunda (31 Mart, 30 Haziran, 30 Eylül ve 31 Aralık) bir üç aylık tutar nakleder.</span><span class="sxs-lookup"><span data-stu-id="43c4b-121">**Quarterly** posts a quarterly amount at the end of each calendar quarter (March 31, June 30, September 30, and December 31).</span></span>
-   <span data-ttu-id="43c4b-122">**Altı Aylık** seçeneği, altı aylık takvim döneminde ( 30 Haziran ve 31 Aralık) bir altı aylık tutar nakleder.</span><span class="sxs-lookup"><span data-stu-id="43c4b-122">**Half-Yearly** posts a half-yearly amount at the end of each calendar half year (June 30 and December 31).</span></span>
-   <span data-ttu-id="43c4b-123">**Günlük** seçeneği her gün için bir işlem kullanarak günlük amortisman yöntemi için amortisman tutarını nakleder.</span><span class="sxs-lookup"><span data-stu-id="43c4b-123">**Daily** posts the depreciation amount for the daily depreciation method by using one transaction for each day.</span></span>

<span data-ttu-id="43c4b-124">Örneğin, **Yıllık** seçeneğini belirlerseniz yıllık amortisman her yılın 31 Aralık tarihinde yalnızca bir defa nakledilir.</span><span class="sxs-lookup"><span data-stu-id="43c4b-124">For example, if you select **Yearly**, the yearly depreciation is posted only one time, on December 31 of each year.</span></span> <span data-ttu-id="43c4b-125">**Aylık** seçeneğini belirlerseniz aylık amortisman her ayı, yıllık amortisman tutarının on ikide biri oranında nakleder</span><span class="sxs-lookup"><span data-stu-id="43c4b-125">If you select **Monthly**, the monthly depreciation is posted each month, as one-twelfth of the yearly depreciation amount.</span></span>

### <a name="fiscal"></a><span data-ttu-id="43c4b-126">Mali</span><span class="sxs-lookup"><span data-stu-id="43c4b-126">Fiscal</span></span>

<span data-ttu-id="43c4b-127">**Amortisman yılı** alanından **Mali Yıl** seçimini yaparsanız düz çizgi kalan yaşam amortismanı kullanılır</span><span class="sxs-lookup"><span data-stu-id="43c4b-127">If you select **Fiscal** in the **Depreciation year** field, straight line life remaining depreciation is used.</span></span> <span data-ttu-id="43c4b-128">Amortisman, kalan mali yıllar temel alınarak hesaplanır.</span><span class="sxs-lookup"><span data-stu-id="43c4b-128">Depreciation is calculated based on the fiscal years remaining.</span></span> <span data-ttu-id="43c4b-129">Örneğin, 1 Temmuz 2015 ile 30 Haziran 2016 arasındaki mali yıl için amortisman hesaplaması 1 Temmuz'da başlar.</span><span class="sxs-lookup"><span data-stu-id="43c4b-129">For example, for the fiscal year July 1, 2015, through June 30, 2016, the depreciation calculation starts on July 1.</span></span> <span data-ttu-id="43c4b-130">Mali yıl 12 aydan daha uzun veya daha kısa olabilir.</span><span class="sxs-lookup"><span data-stu-id="43c4b-130">The fiscal year can be longer or shorter than 12 months.</span></span> <span data-ttu-id="43c4b-131">Amortisman her mali dönem için ayarlanır.</span><span class="sxs-lookup"><span data-stu-id="43c4b-131">The depreciation is adjusted for each fiscal period.</span></span> <span data-ttu-id="43c4b-132">Bir sonraki mali yılın uzunluğu, **Mali takvimler** sayfasında ayarlanan mali dönemler tarafından belirlenir.</span><span class="sxs-lookup"><span data-stu-id="43c4b-132">The length of the next fiscal year is determined by the fiscal periods that are set up on the **Fiscal calendars** page.</span></span> <span data-ttu-id="43c4b-133">Amortisman yılı olarak **Mali** seçerseniz, **Dönem sıklığı** alanında şu seçenekler kullanılabilir:</span><span class="sxs-lookup"><span data-stu-id="43c4b-133">If you select **Fiscal** as the depreciation year, the following options are available in the **Period frequency** field:</span></span>

-   <span data-ttu-id="43c4b-134">**Yıllık**, mali yıl için hesaplanan toplam amortisman tutarını tek tutar olarak, mali yılın son gününde nakleder.</span><span class="sxs-lookup"><span data-stu-id="43c4b-134">**Yearly** posts the total amount of the depreciation that is calculated for the fiscal year as one amount, on the last day of the fiscal year.</span></span>
-   <span data-ttu-id="43c4b-135">**Mali dönem** seçeneği, mali yılın amortismanının toplam tutarını hesaplar.</span><span class="sxs-lookup"><span data-stu-id="43c4b-135">**Fiscal period** calculates the total amount of the depreciation for the fiscal year.</span></span> <span data-ttu-id="43c4b-136">Bu tutar daha sonra, defter için belirtilen mali takvim için **Mali takvimler** sayfasında tanımlanan mali dönemlere aktarılır.</span><span class="sxs-lookup"><span data-stu-id="43c4b-136">This amount is then accrued into the fiscal periods that are defined on the **Fiscal calendars** page for the fiscal calendar that is specified for the book.</span></span>

## <a name="example-of-straight-line-depreciation-of-an-unchanged-fixed-asset"></a><span data-ttu-id="43c4b-137">Değişmeyen bir sabit kıymet için düz çizgi amortisman örneği</span><span class="sxs-lookup"><span data-stu-id="43c4b-137">Example of straight line depreciation of an unchanged fixed asset</span></span>
<span data-ttu-id="43c4b-138">Bir sabit kıymet aşağıdaki özelliklere sahiptir.</span><span class="sxs-lookup"><span data-stu-id="43c4b-138">A fixed asset has the following characteristics.</span></span>

|                     |        |
|---------------------|--------|
| <span data-ttu-id="43c4b-139">Alım maliyeti</span><span class="sxs-lookup"><span data-stu-id="43c4b-139">Acquisition cost</span></span>    | <span data-ttu-id="43c4b-140">11.000</span><span class="sxs-lookup"><span data-stu-id="43c4b-140">11,000</span></span> |
| <span data-ttu-id="43c4b-141">Hurda değeri</span><span class="sxs-lookup"><span data-stu-id="43c4b-141">Salvage value</span></span>       | <span data-ttu-id="43c4b-142">1.000</span><span class="sxs-lookup"><span data-stu-id="43c4b-142">1,000</span></span>  |
| <span data-ttu-id="43c4b-143">Amortisman tabanı</span><span class="sxs-lookup"><span data-stu-id="43c4b-143">Depreciation base</span></span>   | <span data-ttu-id="43c4b-144">10.000</span><span class="sxs-lookup"><span data-stu-id="43c4b-144">10,000</span></span> |
| <span data-ttu-id="43c4b-145">Servis ömrü yıl sayısı</span><span class="sxs-lookup"><span data-stu-id="43c4b-145">Service life years</span></span>  | <span data-ttu-id="43c4b-146">5</span><span class="sxs-lookup"><span data-stu-id="43c4b-146">5</span></span>      |
| <span data-ttu-id="43c4b-147">Yıllık amortisman</span><span class="sxs-lookup"><span data-stu-id="43c4b-147">Yearly depreciation</span></span> | <span data-ttu-id="43c4b-148">2.000</span><span class="sxs-lookup"><span data-stu-id="43c4b-148">2,000</span></span>  |

<span data-ttu-id="43c4b-149">Amortisman tutarı her yıl aynıdır: (Edinme maliyeti – Hurda değeri) ÷ Servis ömrü yıl</span><span class="sxs-lookup"><span data-stu-id="43c4b-149">The depreciation amount is the same every year: (Acquisition cost – Salvage value) ÷ Service life years</span></span>

| <span data-ttu-id="43c4b-150">Dönem</span><span class="sxs-lookup"><span data-stu-id="43c4b-150">Period</span></span> | <span data-ttu-id="43c4b-151">Yıllık amortisman miktarının hesaplaması</span><span class="sxs-lookup"><span data-stu-id="43c4b-151">Calculation of the yearly depreciation amount</span></span> | <span data-ttu-id="43c4b-152">Yıl sonunda net defter değeri</span><span class="sxs-lookup"><span data-stu-id="43c4b-152">Net book value at the end of the year</span></span> |
|--------|-----------------------------------------------|---------------------------------------|
| <span data-ttu-id="43c4b-153">Yıl 1</span><span class="sxs-lookup"><span data-stu-id="43c4b-153">Year 1</span></span> | <span data-ttu-id="43c4b-154">(11.000 – 1.000) ÷ 5 = 2.000</span><span class="sxs-lookup"><span data-stu-id="43c4b-154">(11,000 – 1,000) ÷ 5 = 2,000</span></span>                  | <span data-ttu-id="43c4b-155">9.000</span><span class="sxs-lookup"><span data-stu-id="43c4b-155">9,000</span></span>                                 |
| <span data-ttu-id="43c4b-156">2. yıl</span><span class="sxs-lookup"><span data-stu-id="43c4b-156">Year 2</span></span> | <span data-ttu-id="43c4b-157">(9.000 – 1.000) ÷ 4 = 2.000</span><span class="sxs-lookup"><span data-stu-id="43c4b-157">(9,000 – 1,000) ÷ 4 = 2,000</span></span>                   | <span data-ttu-id="43c4b-158">7.000</span><span class="sxs-lookup"><span data-stu-id="43c4b-158">7,000</span></span>                                 |
| <span data-ttu-id="43c4b-159">3. yıl</span><span class="sxs-lookup"><span data-stu-id="43c4b-159">Year 3</span></span> | <span data-ttu-id="43c4b-160">(7.000 – 1.000) ÷ 3 = 2.000</span><span class="sxs-lookup"><span data-stu-id="43c4b-160">(7,000 – 1,000) ÷ 3 = 2,000</span></span>                   | <span data-ttu-id="43c4b-161">5.000</span><span class="sxs-lookup"><span data-stu-id="43c4b-161">5,000</span></span>                                 |
| <span data-ttu-id="43c4b-162">Yıl 4</span><span class="sxs-lookup"><span data-stu-id="43c4b-162">Year 4</span></span> | <span data-ttu-id="43c4b-163">(5.000 – 1.000) ÷ 2 = 2.000</span><span class="sxs-lookup"><span data-stu-id="43c4b-163">(5,000 – 1,000) ÷ 2 = 2,000</span></span>                   | <span data-ttu-id="43c4b-164">3.000</span><span class="sxs-lookup"><span data-stu-id="43c4b-164">3,000</span></span>                                 |
| <span data-ttu-id="43c4b-165">Yıl 5</span><span class="sxs-lookup"><span data-stu-id="43c4b-165">Year 5</span></span> | <span data-ttu-id="43c4b-166">(3.000 – 1.000) ÷ 1 = 2.000</span><span class="sxs-lookup"><span data-stu-id="43c4b-166">(3,000 – 1,000) ÷ 1 = 2,000</span></span>                   | <span data-ttu-id="43c4b-167">1.000</span><span class="sxs-lookup"><span data-stu-id="43c4b-167">1,000</span></span>                                 |







[!INCLUDE[footer-include](../../includes/footer-banner.md)]