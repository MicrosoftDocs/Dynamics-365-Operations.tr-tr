---
title: "Satış vergisi kodları için tüm tutar ve Aralık hesaplaması seçenekleri"
description: "Bu makalede satış vergisi kodları için Hesaplama yöntemi alanının seçenekleri ve satış vergisinin aralıklar ve tüm tutarlar için nasıl hesaplanacağı açıklanmıştır."
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: TaxData, TaxTable
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations, Retail
ms.custom: 5624
ms.assetid: 96166db4-b7ca-470b-aeb7-0a66fe0554c4
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: bab0f6ca21f4216b70cccf24f5781e0dbf48b7f8
ms.contentlocale: tr-tr
ms.lasthandoff: 09/29/2017

---

# <a name="whole-amount-and-interval-calculation-options-for-sales-tax-codes"></a><span data-ttu-id="ec014-103">Satış vergisi kodları için tüm tutar ve Aralık hesaplaması seçenekleri</span><span class="sxs-lookup"><span data-stu-id="ec014-103">Whole amount and Interval calculation options for sales tax codes</span></span>

[!include[banner](../includes/banner.md)]

[!include[retail name](../includes/retail-name.md)]



<span data-ttu-id="ec014-104">Bu makalede satış vergisi kodları için Hesaplama yöntemi alanının seçenekleri ve satış vergisinin aralıklar ve tüm tutarlar için nasıl hesaplanacağı açıklanmıştır.</span><span class="sxs-lookup"><span data-stu-id="ec014-104">This article explains the options for the Calculation method field on sales tax codes and how sales tax is calculated for intervals and whole amounts.</span></span>

<span data-ttu-id="ec014-105">Tam tutar veya bir aralık tutarına dayalı olarak hesaplanacak bir satış vergisi kodu ayarlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="ec014-105">You can set up a sales tax code to be calculated based on a whole amount or an interval amount.</span></span> <span data-ttu-id="ec014-106">Satış vergisi kodları sayfasında, Hesaplama FastTab'indeki Hesaplama yöntemi alanını kullanarak satış vergisi kodunun nasıl hesaplanacağını seçin.</span><span class="sxs-lookup"><span data-stu-id="ec014-106">In the Sales tax codes page, use the Calculation method field on the Calculation FastTab to select how to calculate a sales tax code.</span></span>
-   <span data-ttu-id="ec014-107">Tüm tutar – Vergi oranı tüm vergilendirilebilir tutara uygulanır.</span><span class="sxs-lookup"><span data-stu-id="ec014-107">Whole amount – The tax rate is applied to the whole taxable amount.</span></span>
-   <span data-ttu-id="ec014-108">Aralık – Vergilendirilebilir tutar, her biri belirli bir satış vergisi oranına sahip bir aralıkta yer alan parçalara bölünür.</span><span class="sxs-lookup"><span data-stu-id="ec014-108">Interval – The taxable amount is divided into parts, each of which falls in a range that has a specific sales tax rate.</span></span> <span data-ttu-id="ec014-109">Belirli bir aralıkta yer alan tutarın parçası söz konusu aralığa ait vergi oranına göre vergilendirilir.</span><span class="sxs-lookup"><span data-stu-id="ec014-109">The part of the amount that falls in a given interval is taxed according to the tax rate for that interval.</span></span> <span data-ttu-id="ec014-110">Satış vergisi her tutar aralığı için hesaplanan vergi tutarlarının toplamıdır.</span><span class="sxs-lookup"><span data-stu-id="ec014-110">The sales tax is the sum of the tax amounts that are calculated for each amount interval.</span></span>
> [!NOTE]                                                                                                                              
> <span data-ttu-id="ec014-111">Aralık seçeneği, yalnızca Genel muhasebe parametreleri sayfasındaki Satış vergisi alanında Hesaplama yöntemi alanında Satır'ı seçtiğinizde kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="ec014-111">The Interval option is available only when you select Line in the Calculation method field in the Sales tax area of the General ledger parameters page.</span></span> 

<span data-ttu-id="ec014-112">Aralıklar, Satış vergisi kodu değerlerinde vergi oranı başına Minimum ve Maksimum sınır miktarlarını girerek ayarlanır.</span><span class="sxs-lookup"><span data-stu-id="ec014-112">Intervals are set up in the Sales tax code values page by entering Minimum and Maximum limit amounts per tax rate.</span></span> <span data-ttu-id="ec014-113">Seçilen hesaplama yönteminden bağımsız olarak, tüm vergilendirilebilir tutarlarda hesaplanacak vergiler için aralıkların aşağıdaki kurallara uygun olması gerekir:</span><span class="sxs-lookup"><span data-stu-id="ec014-113">For taxes to be calculated on all taxable amounts, regardless of which calculation method is selected, intervals must follow these rules:</span></span>
-   <span data-ttu-id="ec014-114">İlk aralık sıfır şeklinde bir Minimum sınıra sahip olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="ec014-114">The first interval must have a Minimum limit of zero.</span></span>
-   <span data-ttu-id="ec014-115">Son aralıkta, sonsuzluğu belirtecek şekilde sıfır değerinde bir Maksimum sınır olması gerekir.</span><span class="sxs-lookup"><span data-stu-id="ec014-115">The last interval must have a Maximum limit of zero, which indicates infinity.</span></span>
-   <span data-ttu-id="ec014-116">Bir aralığın Maksimum sınırı sonraki aralığın Minimum sınırı olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="ec014-116">The Maximum limit of an interval must be the Minimum limit of the next interval.</span></span>

<span data-ttu-id="ec014-117">Bir tutarın önceki bir aralığın Maksimum sınırı ve sonraki aralığın Minimum sınırı olması durumunda, birinci aralığın satış vergisi oranı tutar için geçerli olacaktır.</span><span class="sxs-lookup"><span data-stu-id="ec014-117">If an amount is the Maximum limit of the previous interval and the Minimum limit of the next interval, the sales tax rate of the first interval will be applied to the amount.</span></span> <span data-ttu-id="ec014-118">Bir tutarın üst ve alt limitlerle tanımlanan aralıkların dışında kalması durumunda, sıfıra karşılık gelen bir satış vergisi oranı uygulanır.</span><span class="sxs-lookup"><span data-stu-id="ec014-118">If an amount falls outside the intervals that are defined by upper and lower limits, a sales tax rate of zero will be applied.</span></span>

## <a name="example-whole-amount-method-of-calculation"></a><span data-ttu-id="ec014-119">Örnek: Tüm tutar hesaplama yöntemi</span><span class="sxs-lookup"><span data-stu-id="ec014-119">Example: Whole amount method of calculation</span></span>
<span data-ttu-id="ec014-120">Satış vergisi kod değerleri sayfasında, satış vergisi oranları aşağıdaki aralıklarda ayarlanır:</span><span class="sxs-lookup"><span data-stu-id="ec014-120">In the Sales tax code values page, sales tax rates are set up in the following intervals:</span></span>
|                   |                   |              |
|-------------------|-------------------|--------------|
| <span data-ttu-id="ec014-121">**Minimum sınır**</span><span class="sxs-lookup"><span data-stu-id="ec014-121">**Minimum limit**</span></span> | <span data-ttu-id="ec014-122">**Maksimum sınır**</span><span class="sxs-lookup"><span data-stu-id="ec014-122">**Maximum limit**</span></span> | <span data-ttu-id="ec014-123">**Vergi oranı**</span><span class="sxs-lookup"><span data-stu-id="ec014-123">**Tax rate**</span></span> |
| <span data-ttu-id="ec014-124">0,00</span><span class="sxs-lookup"><span data-stu-id="ec014-124">0.00</span></span>              | <span data-ttu-id="ec014-125">50,00</span><span class="sxs-lookup"><span data-stu-id="ec014-125">50.00</span></span>             | <span data-ttu-id="ec014-126">%30</span><span class="sxs-lookup"><span data-stu-id="ec014-126">30%</span></span>          |
| <span data-ttu-id="ec014-127">50,00</span><span class="sxs-lookup"><span data-stu-id="ec014-127">50.00</span></span>             | <span data-ttu-id="ec014-128">100,00</span><span class="sxs-lookup"><span data-stu-id="ec014-128">100.00</span></span>            | <span data-ttu-id="ec014-129">%20</span><span class="sxs-lookup"><span data-stu-id="ec014-129">20%</span></span>          |
| <span data-ttu-id="ec014-130">100,00</span><span class="sxs-lookup"><span data-stu-id="ec014-130">100.00</span></span>            | <span data-ttu-id="ec014-131">0,00</span><span class="sxs-lookup"><span data-stu-id="ec014-131">0.00</span></span>              | <span data-ttu-id="ec014-132">%10</span><span class="sxs-lookup"><span data-stu-id="ec014-132">10%</span></span>          |

<span data-ttu-id="ec014-133">Satış vergisi, vergiye tabi tüm tutar üzerinde hesaplanır.</span><span class="sxs-lookup"><span data-stu-id="ec014-133">The sales tax is calculated on the whole taxable amount.</span></span>

| <span data-ttu-id="ec014-134">Vergiye tabi tutar (fiyat)</span><span class="sxs-lookup"><span data-stu-id="ec014-134">Taxable amount (price)</span></span> | <span data-ttu-id="ec014-135">Hesaplama</span><span class="sxs-lookup"><span data-stu-id="ec014-135">Calculation</span></span>    | <span data-ttu-id="ec014-136">Satış vergisi</span><span class="sxs-lookup"><span data-stu-id="ec014-136">Sales tax</span></span> |
|------------------------|----------------|-----------|
| <span data-ttu-id="ec014-137">35,00</span><span class="sxs-lookup"><span data-stu-id="ec014-137">35.00</span></span>                  | <span data-ttu-id="ec014-138">35,00 \* 0,30</span><span class="sxs-lookup"><span data-stu-id="ec014-138">35.00 \* 0.30</span></span>  | <span data-ttu-id="ec014-139">10,50</span><span class="sxs-lookup"><span data-stu-id="ec014-139">10.50</span></span>     |
| <span data-ttu-id="ec014-140">50,00</span><span class="sxs-lookup"><span data-stu-id="ec014-140">50.00</span></span>                  | <span data-ttu-id="ec014-141">50,00 \* 0,30</span><span class="sxs-lookup"><span data-stu-id="ec014-141">50.00 \* 0.30</span></span>  | <span data-ttu-id="ec014-142">15,00</span><span class="sxs-lookup"><span data-stu-id="ec014-142">15.00</span></span>     |
| <span data-ttu-id="ec014-143">85,00</span><span class="sxs-lookup"><span data-stu-id="ec014-143">85.00</span></span>                  | <span data-ttu-id="ec014-144">85,00 \* 0,20</span><span class="sxs-lookup"><span data-stu-id="ec014-144">85.00 \* 0.20</span></span>  | <span data-ttu-id="ec014-145">17,00</span><span class="sxs-lookup"><span data-stu-id="ec014-145">17.00</span></span>     |
| <span data-ttu-id="ec014-146">305,00</span><span class="sxs-lookup"><span data-stu-id="ec014-146">305.00</span></span>                 | <span data-ttu-id="ec014-147">305,00 \* 0,10</span><span class="sxs-lookup"><span data-stu-id="ec014-147">305.00 \* 0.10</span></span> | <span data-ttu-id="ec014-148">30,50</span><span class="sxs-lookup"><span data-stu-id="ec014-148">30.50</span></span>     |

## <a name="example-interval-method-of-calculation"></a><span data-ttu-id="ec014-149"> Örnek: Aralık hesaplama yöntemi</span><span class="sxs-lookup"><span data-stu-id="ec014-149">Example: Interval method of calculation</span></span>
<span data-ttu-id="ec014-150">Değerler sayfasında, satış vergisi oranları aşağıdaki aralıklarda belirlenir:</span><span class="sxs-lookup"><span data-stu-id="ec014-150">In the Values page, sales tax rates are set up in the following intervals:</span></span>

|                   |                   |              |
|-------------------|-------------------|--------------|
| <span data-ttu-id="ec014-151">**Minimum sınır**</span><span class="sxs-lookup"><span data-stu-id="ec014-151">**Minimum limit**</span></span> | <span data-ttu-id="ec014-152">**Maksimum sınır**</span><span class="sxs-lookup"><span data-stu-id="ec014-152">**Maximum limit**</span></span> | <span data-ttu-id="ec014-153">**Vergi oranı**</span><span class="sxs-lookup"><span data-stu-id="ec014-153">**Tax rate**</span></span> |
| <span data-ttu-id="ec014-154">0,00</span><span class="sxs-lookup"><span data-stu-id="ec014-154">0.00</span></span>              | <span data-ttu-id="ec014-155">50,00</span><span class="sxs-lookup"><span data-stu-id="ec014-155">50.00</span></span>             | <span data-ttu-id="ec014-156">%30</span><span class="sxs-lookup"><span data-stu-id="ec014-156">30%</span></span>          |
| <span data-ttu-id="ec014-157">50,00</span><span class="sxs-lookup"><span data-stu-id="ec014-157">50.00</span></span>             | <span data-ttu-id="ec014-158">100,00</span><span class="sxs-lookup"><span data-stu-id="ec014-158">100.00</span></span>            | <span data-ttu-id="ec014-159">%20</span><span class="sxs-lookup"><span data-stu-id="ec014-159">20%</span></span>          |
| <span data-ttu-id="ec014-160">100,00</span><span class="sxs-lookup"><span data-stu-id="ec014-160">100.00</span></span>            | <span data-ttu-id="ec014-161">0,00</span><span class="sxs-lookup"><span data-stu-id="ec014-161">0.00</span></span>              | <span data-ttu-id="ec014-162">%10</span><span class="sxs-lookup"><span data-stu-id="ec014-162">10%</span></span>          |

<span data-ttu-id="ec014-163">Satış vergisi her tutar aralığı için hesaplanan vergi tutarlarının toplamıdır.</span><span class="sxs-lookup"><span data-stu-id="ec014-163">The sales tax is the sum of the tax amounts that are calculated for each amount interval.</span></span>

| <span data-ttu-id="ec014-164">Vergiye tabi tutar (fiyat)</span><span class="sxs-lookup"><span data-stu-id="ec014-164">Taxable amount (price)</span></span> | <span data-ttu-id="ec014-165">Hesaplama</span><span class="sxs-lookup"><span data-stu-id="ec014-165">Calculation</span></span>                                                               | <span data-ttu-id="ec014-166">Satış vergisi</span><span class="sxs-lookup"><span data-stu-id="ec014-166">Sales tax</span></span> |
|------------------------|---------------------------------------------------------------------------|-----------|
| <span data-ttu-id="ec014-167">35,00</span><span class="sxs-lookup"><span data-stu-id="ec014-167">35.00</span></span>                  | <span data-ttu-id="ec014-168">35,00 \* 0,30</span><span class="sxs-lookup"><span data-stu-id="ec014-168">35.00 \* 0.30</span></span>                                                             | <span data-ttu-id="ec014-169">10,50</span><span class="sxs-lookup"><span data-stu-id="ec014-169">10.50</span></span>     |
| <span data-ttu-id="ec014-170">50,00</span><span class="sxs-lookup"><span data-stu-id="ec014-170">50.00</span></span>                  | <span data-ttu-id="ec014-171">50,00 \* 0,30</span><span class="sxs-lookup"><span data-stu-id="ec014-171">50.00 \* 0.30</span></span>                                                             | <span data-ttu-id="ec014-172">15,00</span><span class="sxs-lookup"><span data-stu-id="ec014-172">15.00</span></span>     |
| <span data-ttu-id="ec014-173">85,00</span><span class="sxs-lookup"><span data-stu-id="ec014-173">85.00</span></span>                  | <span data-ttu-id="ec014-174">(50,00 \* 0,30 = 15,00) + (35,00 \* 0,20 = 7,00)</span><span class="sxs-lookup"><span data-stu-id="ec014-174">(50.00 \* 0.30 = 15.00) + (35.00 \* 0.20 = 7.00)</span></span>                          | <span data-ttu-id="ec014-175">22,00</span><span class="sxs-lookup"><span data-stu-id="ec014-175">22.00</span></span>     |
| <span data-ttu-id="ec014-176">305,00</span><span class="sxs-lookup"><span data-stu-id="ec014-176">305.00</span></span>                 | <span data-ttu-id="ec014-177">(50,00 \* 0,30 = 15,00) + (50,00 \* 0,20 = 10,00) + (205 \* 0,10 = 20,50)</span><span class="sxs-lookup"><span data-stu-id="ec014-177">(50.00 \* 0.30 = 15.00) + (50.00 \* 0.20 = 10.00) + (205 \* 0.10 = 20.50)</span></span> | <span data-ttu-id="ec014-178">45,50</span><span class="sxs-lookup"><span data-stu-id="ec014-178">45.50</span></span>     |

 

<span data-ttu-id="ec014-179">Daha fazla bilgi için bkz. [Marjinal taban ve hesaplama yöntemi alanları temel alınarak satış vergisi oranlarını belirleme](marginal-base-field.md).</span><span class="sxs-lookup"><span data-stu-id="ec014-179">For more information, see [Determining sale tax rates based on the Marginal base and Calculation method fields](marginal-base-field.md).</span></span>






