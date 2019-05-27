---
title: El ile amortisman
description: Bu makalede, el ile amortisman yöntemi hakkında genel bir bakış verilmektedir.
author: ShylaThompson
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
ms.custom: 13811
ms.assetid: b0e837c9-515a-4aed-9060-5ec94f37edeb
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 14e385e60e10146a0855a467af57a0a31fcc53bd
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/15/2019
ms.locfileid: "1558747"
---
# <a name="manual-depreciation"></a><span data-ttu-id="3c2df-103">El ile amortisman</span><span class="sxs-lookup"><span data-stu-id="3c2df-103">Manual depreciation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="3c2df-104">Bu makalede, el ile amortisman yöntemi hakkında genel bir bakış verilmektedir.</span><span class="sxs-lookup"><span data-stu-id="3c2df-104">This article gives an overview of the manual depreciation method.</span></span>

<span data-ttu-id="3c2df-105">Sabit kıymet amortisman profilini ayarlayıp **Amortisman profilleri** sayfasının **Yöntem** alanındaki **El ile** seçeneğini işaretlediğinize, amortisman profiline atanan sabit kıymetlerin amortismanı, takvim yılında her aralık için girdiğiniz yüzdeyle saptanır.</span><span class="sxs-lookup"><span data-stu-id="3c2df-105">When you set up a fixed asset depreciation profile and select **Manual** in the **Method** field on the **Depreciation profiles** page, the depreciation of fixed assets that are assigned to the depreciation profile is determined by the percentage that you enter for each interval in the calendar year.</span></span> <span data-ttu-id="3c2df-106">Yüzdeler ayarladığını aralıklar **Amortisman profilleri** sayfasının **Dönem sıklığı** alanındaki **Genel** hızlı sekmesinde seçtiğiniz değere göre deftere nakledilir.</span><span class="sxs-lookup"><span data-stu-id="3c2df-106">The intervals that you set up percentages for are posted according to the value that you select in the **Period frequency** field on the **General** FastTab of the **Depreciation profiles** page.</span></span> <span data-ttu-id="3c2df-107">Seçebileceğiniz değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="3c2df-107">Here are the values that you can select:</span></span>

-   <span data-ttu-id="3c2df-108">Yıllık</span><span class="sxs-lookup"><span data-stu-id="3c2df-108">Yearly</span></span>
-   <span data-ttu-id="3c2df-109">Aylık</span><span class="sxs-lookup"><span data-stu-id="3c2df-109">Monthly</span></span>
-   <span data-ttu-id="3c2df-110">Üç aylık</span><span class="sxs-lookup"><span data-stu-id="3c2df-110">Quarterly</span></span>
-   <span data-ttu-id="3c2df-111">Yarım yıllık</span><span class="sxs-lookup"><span data-stu-id="3c2df-111">Half-Yearly</span></span>
-   <span data-ttu-id="3c2df-112">Günlük</span><span class="sxs-lookup"><span data-stu-id="3c2df-112">Daily</span></span>

<span data-ttu-id="3c2df-113">Dönem sıklığını seçtikten sonra, **El ile girilen planlar**'ı seçin ve her bir deftere nakletme sıklığı için yüzdeler ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="3c2df-113">After you select the period frequency, click **Manual schedules**, and set up percentages for each posting interval.</span></span> <span data-ttu-id="3c2df-114">El ile yapılan planlamalar ve deftere nakledilen aralıklar, bu makalenin devamında aşağıdaki örneklerde gösterildiği gibi amortisman tutarını tanımlar.</span><span class="sxs-lookup"><span data-stu-id="3c2df-114">Together, the manual schedules and the posting intervals define the depreciation amount, as shown in the examples later in this article.</span></span> <span data-ttu-id="3c2df-115">El ile amortisman her zaman alım fiyatının bir yüzdesi olarak hesaplanır.</span><span class="sxs-lookup"><span data-stu-id="3c2df-115">Manual depreciation is always calculated as a percentage of the acquisition price.</span></span> <span data-ttu-id="3c2df-116">El ile amortisman için, amortismanın aralıklarına girdiğiniz yüzdeler, toplam yüzde 100'e tamamlanmak zorunda değildir.</span><span class="sxs-lookup"><span data-stu-id="3c2df-116">For manual depreciation, the percentages that you enter in the intervals of the depreciation don't have to add up to 100 percent.</span></span> <span data-ttu-id="3c2df-117">El ile amortisman, **Defterler**'de genellikle özel amaçlar için (örneğin, vergi) periyodik olmayan amortismanları belirlemek için kullanılan, esnek bir amortisman yöntemidir.</span><span class="sxs-lookup"><span data-stu-id="3c2df-117">Manual depreciation is a flexible depreciation method that is often used to define an extraordinary depreciation profile on the **Books** page, such as a non-periodic depreciation for special purposes (for example, tax).</span></span>

## <a name="examples"></a><span data-ttu-id="3c2df-118">Örnekler</span><span class="sxs-lookup"><span data-stu-id="3c2df-118">Examples</span></span>
<span data-ttu-id="3c2df-119">Alım fiyatı: 11.000,00 Beklenen ıskarta değeri: 1.000,00 Aşağıdaki tablo, **Sabit kıymet amortisman profili planları** sayfasında ayarlamış olduğunuz aralıklar ve yüzdeleri gösterir.</span><span class="sxs-lookup"><span data-stu-id="3c2df-119">Acquisition price: 11,000.00 Expected scrap value: 1,000.00 The following table shows the intervals and percentages that you set up on the **Fixed asset depreciation profile schedules** page.</span></span>

| <span data-ttu-id="3c2df-120">Aralık numarası</span><span class="sxs-lookup"><span data-stu-id="3c2df-120">Interval number</span></span> | <span data-ttu-id="3c2df-121">Yüzde</span><span class="sxs-lookup"><span data-stu-id="3c2df-121">Percentage</span></span> |
|-----------------|------------|
| <span data-ttu-id="3c2df-122">1</span><span class="sxs-lookup"><span data-stu-id="3c2df-122">1</span></span>               | <span data-ttu-id="3c2df-123">10,00</span><span class="sxs-lookup"><span data-stu-id="3c2df-123">10.00</span></span>      |
| <span data-ttu-id="3c2df-124">2</span><span class="sxs-lookup"><span data-stu-id="3c2df-124">2</span></span>               | <span data-ttu-id="3c2df-125">50,00</span><span class="sxs-lookup"><span data-stu-id="3c2df-125">50.00</span></span>      |
| <span data-ttu-id="3c2df-126">3</span><span class="sxs-lookup"><span data-stu-id="3c2df-126">3</span></span>               | <span data-ttu-id="3c2df-127">8,00</span><span class="sxs-lookup"><span data-stu-id="3c2df-127">8.00</span></span>       |

<span data-ttu-id="3c2df-128">Aşağıdaki tablo, her aralık için amortismanın nasıl hesaplandığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="3c2df-128">The following table shows how the depreciation for each interval is calculated.</span></span>

|  <span data-ttu-id="3c2df-129">Aralık numarası</span><span class="sxs-lookup"><span data-stu-id="3c2df-129">Interval number</span></span> | <span data-ttu-id="3c2df-130">Yıllık amortisman miktarının hesaplaması</span><span class="sxs-lookup"><span data-stu-id="3c2df-130">Calculation of the yearly depreciation amount</span></span> | <span data-ttu-id="3c2df-131">Aralık sonunda net defter değeri</span><span class="sxs-lookup"><span data-stu-id="3c2df-131">Net book value at the end of the interval</span></span> |
|------------------|-----------------------------------------------|-------------------------------------------|
| <span data-ttu-id="3c2df-132">1</span><span class="sxs-lookup"><span data-stu-id="3c2df-132">1</span></span>                | <span data-ttu-id="3c2df-133">(11.000 – 1.000) × %10 = 1.000</span><span class="sxs-lookup"><span data-stu-id="3c2df-133">(11,000 – 1,000) × 10% = 1,000</span></span>                | <span data-ttu-id="3c2df-134">10.000 (11.000 – 1.000)</span><span class="sxs-lookup"><span data-stu-id="3c2df-134">10,000 (11,000 – 1,000)</span></span>                   |
| <span data-ttu-id="3c2df-135">2</span><span class="sxs-lookup"><span data-stu-id="3c2df-135">2</span></span>                | <span data-ttu-id="3c2df-136">(11.000 – 1.000) × %50 = 5.000</span><span class="sxs-lookup"><span data-stu-id="3c2df-136">(11,000 – 1,000) × 50% = 5,000</span></span>                | <span data-ttu-id="3c2df-137">5.000 (10.000 – 5.000)</span><span class="sxs-lookup"><span data-stu-id="3c2df-137">5,000 (10,000 – 5,000)</span></span>                    |
| <span data-ttu-id="3c2df-138">3</span><span class="sxs-lookup"><span data-stu-id="3c2df-138">3</span></span>                | <span data-ttu-id="3c2df-139">(11.000 – 1.000) × %8 = 800</span><span class="sxs-lookup"><span data-stu-id="3c2df-139">(11,000 – 1,000) × 8% = 800</span></span>                   | <span data-ttu-id="3c2df-140">4.200 (5.000 – 800)</span><span class="sxs-lookup"><span data-stu-id="3c2df-140">4,200 (5,000 – 800)</span></span>                       |

<span data-ttu-id="3c2df-141">**Dönem sıklığı** alanında **Aylık** seçeneğini işaretlerseniz , el ile 12 planlama aralığı ayarlarsınız.</span><span class="sxs-lookup"><span data-stu-id="3c2df-141">If you select **Monthly** in the **Period frequency** field, you set up 12 manual schedule intervals.</span></span> <span data-ttu-id="3c2df-142">Aşağıdaki tablo, ilk iki aralık için amortisman tutarlarını gösterir.</span><span class="sxs-lookup"><span data-stu-id="3c2df-142">The following table shows the depreciation amounts for the first two intervals.</span></span>

| <span data-ttu-id="3c2df-143">Aralık</span><span class="sxs-lookup"><span data-stu-id="3c2df-143">Interval</span></span> | <span data-ttu-id="3c2df-144">Amortisman tutarı</span><span class="sxs-lookup"><span data-stu-id="3c2df-144">Depreciation amount</span></span>            |
|----------|--------------------------------|
| <span data-ttu-id="3c2df-145">Ocak</span><span class="sxs-lookup"><span data-stu-id="3c2df-145">January</span></span>  | <span data-ttu-id="3c2df-146">(11.000 – 1.000) × %10 = 1.000</span><span class="sxs-lookup"><span data-stu-id="3c2df-146">(11,000 – 1,000) × 10% = 1,000</span></span> |
| <span data-ttu-id="3c2df-147">Şubat</span><span class="sxs-lookup"><span data-stu-id="3c2df-147">February</span></span> | <span data-ttu-id="3c2df-148">(11.000 – 1.000) × %50 = 5.000</span><span class="sxs-lookup"><span data-stu-id="3c2df-148">(11,000 – 1,000) × 50% = 5,000</span></span> |

<span data-ttu-id="3c2df-149">*<strong><em>Dönem sıklığı</em>* alanında </strong> <strong>Yarım Yıllık</strong> seçeneğini işaretlerseniz , el ile en fazla iki planlama aralığı ayarlarsınız.</span><span class="sxs-lookup"><span data-stu-id="3c2df-149">If you select <strong>Half-Yearly</strong> in the *<strong><em>Period frequency</em>* field</strong>, you set up two manual schedule intervals.</span></span> <span data-ttu-id="3c2df-150">Aşağıdaki tablo, bu iki aralık için amortisman tutarlarını gösterir.</span><span class="sxs-lookup"><span data-stu-id="3c2df-150">The following table shows the depreciation amounts for those two intervals.</span></span>

| <span data-ttu-id="3c2df-151">Aralık</span><span class="sxs-lookup"><span data-stu-id="3c2df-151">Interval</span></span>    | <span data-ttu-id="3c2df-152">Amortisman tutarı</span><span class="sxs-lookup"><span data-stu-id="3c2df-152">Depreciation amount</span></span>            |
|-------------|--------------------------------|
| <span data-ttu-id="3c2df-153">30 Haziran</span><span class="sxs-lookup"><span data-stu-id="3c2df-153">June 30</span></span>     | <span data-ttu-id="3c2df-154">(11.000 – 1.000) × %10 = 1.000</span><span class="sxs-lookup"><span data-stu-id="3c2df-154">(11,000 – 1,000) × 10% = 1,000</span></span> |
| <span data-ttu-id="3c2df-155">31 Aralık</span><span class="sxs-lookup"><span data-stu-id="3c2df-155">December 31</span></span> | <span data-ttu-id="3c2df-156">(11.000 – 1.000) × %50 = 5.000</span><span class="sxs-lookup"><span data-stu-id="3c2df-156">(11,000 – 1,000) × 50% = 5,000</span></span> |

<span data-ttu-id="3c2df-157">Tüm aralıkların yüzde toplamı 100 olmak zorunda değildir.</span><span class="sxs-lookup"><span data-stu-id="3c2df-157">The total of percentages for all intervals doesn't have to be 100.</span></span> <span data-ttu-id="3c2df-158">Ancak, **Sabit kıymet amortisman profili planları** sayfasındaki **Toplam yüzde** alanındaki değer **100** değilse bir ileti alırsınız.</span><span class="sxs-lookup"><span data-stu-id="3c2df-158">However, you receive a message if the value in the **Cumulative percentage** field on the **Fixed asset depreciation profile schedules** page isn't **100**.</span></span>



