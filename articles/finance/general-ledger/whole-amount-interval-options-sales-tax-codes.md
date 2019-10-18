---
title: Satış vergisi kodları için tüm tutar ve Aralık hesaplaması seçenekleri
description: Bu makalede satış vergisi kodları için Hesaplama yöntemi alanının seçenekleri ve satış vergisinin aralıklar ve tüm tutarlar için nasıl hesaplanacağı açıklanmıştır.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxData, TaxTable
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations, Retail
ms.custom: 5624
ms.assetid: 96166db4-b7ca-470b-aeb7-0a66fe0554c4
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: fb737e6600b1812c44d6101814fc858ac27013e9
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/27/2019
ms.locfileid: "2185854"
---
# <a name="whole-amount-and-interval-calculation-options-for-sales-tax-codes"></a><span data-ttu-id="05d37-103">Satış vergisi kodları için tüm tutar ve Aralık hesaplaması seçenekleri</span><span class="sxs-lookup"><span data-stu-id="05d37-103">Whole amount and Interval calculation options for sales tax codes</span></span>

[!include [banner](../includes/banner.md)]

[!include [retail name](../includes/retail-name.md)]

<span data-ttu-id="05d37-104">Bu makalede satış vergisi kodları için Hesaplama yöntemi alanının seçenekleri ve satış vergisinin aralıklar ve tüm tutarlar için nasıl hesaplanacağı açıklanmıştır.</span><span class="sxs-lookup"><span data-stu-id="05d37-104">This article explains the options for the Calculation method field on sales tax codes and how sales tax is calculated for intervals and whole amounts.</span></span>

<span data-ttu-id="05d37-105">Tam tutar veya bir aralık tutarına dayalı olarak hesaplanacak bir satış vergisi kodu ayarlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="05d37-105">You can set up a sales tax code to be calculated based on a whole amount or an interval amount.</span></span> <span data-ttu-id="05d37-106">Satış vergisi kodları sayfasında, Hesaplama FastTab'indeki Hesaplama yöntemi alanını kullanarak satış vergisi kodunun nasıl hesaplanacağını seçin.</span><span class="sxs-lookup"><span data-stu-id="05d37-106">In the Sales tax codes page, use the Calculation method field on the Calculation FastTab to select how to calculate a sales tax code.</span></span>
- <span data-ttu-id="05d37-107">Tüm tutar – Vergi oranı tüm vergilendirilebilir tutara uygulanır.</span><span class="sxs-lookup"><span data-stu-id="05d37-107">Whole amount – The tax rate is applied to the whole taxable amount.</span></span>
- <span data-ttu-id="05d37-108">Aralık – Vergilendirilebilir tutar, her biri belirli bir satış vergisi oranına sahip bir aralıkta yer alan parçalara bölünür.</span><span class="sxs-lookup"><span data-stu-id="05d37-108">Interval – The taxable amount is divided into parts, each of which falls in a range that has a specific sales tax rate.</span></span> <span data-ttu-id="05d37-109">Belirli bir aralıkta yer alan tutarın parçası söz konusu aralığa ait vergi oranına göre vergilendirilir.</span><span class="sxs-lookup"><span data-stu-id="05d37-109">The part of the amount that falls in a given interval is taxed according to the tax rate for that interval.</span></span> <span data-ttu-id="05d37-110">Satış vergisi her tutar aralığı için hesaplanan vergi tutarlarının toplamıdır.</span><span class="sxs-lookup"><span data-stu-id="05d37-110">The sales tax is the sum of the tax amounts that are calculated for each amount interval.</span></span>
  > [!NOTE]                                                                                                                              
  > <span data-ttu-id="05d37-111">Aralık seçeneği, yalnızca Genel muhasebe parametreleri sayfasındaki Satış vergisi alanında Hesaplama yöntemi alanında Satır'ı seçtiğinizde kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="05d37-111">The Interval option is available only when you select Line in the Calculation method field in the Sales tax area of the General ledger parameters page.</span></span> 

<span data-ttu-id="05d37-112">Aralıklar, Satış vergisi kodu değerlerinde vergi oranı başına Minimum ve Maksimum sınır miktarlarını girerek ayarlanır.</span><span class="sxs-lookup"><span data-stu-id="05d37-112">Intervals are set up in the Sales tax code values page by entering Minimum and Maximum limit amounts per tax rate.</span></span> <span data-ttu-id="05d37-113">Seçilen hesaplama yönteminden bağımsız olarak, tüm vergilendirilebilir tutarlarda hesaplanacak vergiler için aralıkların aşağıdaki kurallara uygun olması gerekir:</span><span class="sxs-lookup"><span data-stu-id="05d37-113">For taxes to be calculated on all taxable amounts, regardless of which calculation method is selected, intervals must follow these rules:</span></span>
-   <span data-ttu-id="05d37-114">İlk aralık sıfır şeklinde bir Minimum sınıra sahip olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="05d37-114">The first interval must have a Minimum limit of zero.</span></span>
-   <span data-ttu-id="05d37-115">Son aralıkta, sonsuzluğu belirtecek şekilde sıfır değerinde bir Maksimum sınır olması gerekir.</span><span class="sxs-lookup"><span data-stu-id="05d37-115">The last interval must have a Maximum limit of zero, which indicates infinity.</span></span>
-   <span data-ttu-id="05d37-116">Bir aralığın Maksimum sınırı sonraki aralığın Minimum sınırı olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="05d37-116">The Maximum limit of an interval must be the Minimum limit of the next interval.</span></span>

<span data-ttu-id="05d37-117">Bir tutarın önceki bir aralığın Maksimum sınırı ve sonraki aralığın Minimum sınırı olması durumunda, birinci aralığın satış vergisi oranı tutar için geçerli olacaktır.</span><span class="sxs-lookup"><span data-stu-id="05d37-117">If an amount is the Maximum limit of the previous interval and the Minimum limit of the next interval, the sales tax rate of the first interval will be applied to the amount.</span></span> <span data-ttu-id="05d37-118">Bir tutarın üst ve alt limitlerle tanımlanan aralıkların dışında kalması durumunda, sıfıra karşılık gelen bir satış vergisi oranı uygulanır.</span><span class="sxs-lookup"><span data-stu-id="05d37-118">If an amount falls outside the intervals that are defined by upper and lower limits, a sales tax rate of zero will be applied.</span></span>

## <a name="example-whole-amount-method-of-calculation"></a><span data-ttu-id="05d37-119">Örnek: Tüm tutar hesaplama yöntemi</span><span class="sxs-lookup"><span data-stu-id="05d37-119">Example: Whole amount method of calculation</span></span>
<span data-ttu-id="05d37-120">Satış vergisi kod değerleri sayfasında, satış vergisi oranları aşağıdaki aralıklarda ayarlanır:</span><span class="sxs-lookup"><span data-stu-id="05d37-120">In the Sales tax code values page, sales tax rates are set up in the following intervals:</span></span>

|                   |                   |              |
|-------------------|-------------------|--------------|
| <span data-ttu-id="05d37-121">**Minimum sınır**</span><span class="sxs-lookup"><span data-stu-id="05d37-121">**Minimum limit**</span></span> | <span data-ttu-id="05d37-122">**Maksimum sınır**</span><span class="sxs-lookup"><span data-stu-id="05d37-122">**Maximum limit**</span></span> | <span data-ttu-id="05d37-123">**Vergi oranı**</span><span class="sxs-lookup"><span data-stu-id="05d37-123">**Tax rate**</span></span> |
| <span data-ttu-id="05d37-124">0,00</span><span class="sxs-lookup"><span data-stu-id="05d37-124">0.00</span></span>              | <span data-ttu-id="05d37-125">50,00</span><span class="sxs-lookup"><span data-stu-id="05d37-125">50.00</span></span>             | <span data-ttu-id="05d37-126">%30</span><span class="sxs-lookup"><span data-stu-id="05d37-126">30%</span></span>          |
| <span data-ttu-id="05d37-127">50,00</span><span class="sxs-lookup"><span data-stu-id="05d37-127">50.00</span></span>             | <span data-ttu-id="05d37-128">100,00</span><span class="sxs-lookup"><span data-stu-id="05d37-128">100.00</span></span>            | <span data-ttu-id="05d37-129">%20</span><span class="sxs-lookup"><span data-stu-id="05d37-129">20%</span></span>          |
| <span data-ttu-id="05d37-130">100,00</span><span class="sxs-lookup"><span data-stu-id="05d37-130">100.00</span></span>            | <span data-ttu-id="05d37-131">0,00</span><span class="sxs-lookup"><span data-stu-id="05d37-131">0.00</span></span>              | <span data-ttu-id="05d37-132">%10</span><span class="sxs-lookup"><span data-stu-id="05d37-132">10%</span></span>          |

<span data-ttu-id="05d37-133">Satış vergisi, vergiye tabi tüm tutar üzerinde hesaplanır.</span><span class="sxs-lookup"><span data-stu-id="05d37-133">The sales tax is calculated on the whole taxable amount.</span></span>

| <span data-ttu-id="05d37-134">Vergiye tabi tutar (fiyat)</span><span class="sxs-lookup"><span data-stu-id="05d37-134">Taxable amount (price)</span></span> | <span data-ttu-id="05d37-135">Hesaplama</span><span class="sxs-lookup"><span data-stu-id="05d37-135">Calculation</span></span>    | <span data-ttu-id="05d37-136">Satış vergisi</span><span class="sxs-lookup"><span data-stu-id="05d37-136">Sales tax</span></span> |
|------------------------|----------------|-----------|
| <span data-ttu-id="05d37-137">35,00</span><span class="sxs-lookup"><span data-stu-id="05d37-137">35.00</span></span>                  | <span data-ttu-id="05d37-138">35,00 \* 0,30</span><span class="sxs-lookup"><span data-stu-id="05d37-138">35.00 \* 0.30</span></span>  | <span data-ttu-id="05d37-139">10,50</span><span class="sxs-lookup"><span data-stu-id="05d37-139">10.50</span></span>     |
| <span data-ttu-id="05d37-140">50,00</span><span class="sxs-lookup"><span data-stu-id="05d37-140">50.00</span></span>                  | <span data-ttu-id="05d37-141">50,00 \* 0,30</span><span class="sxs-lookup"><span data-stu-id="05d37-141">50.00 \* 0.30</span></span>  | <span data-ttu-id="05d37-142">15,00</span><span class="sxs-lookup"><span data-stu-id="05d37-142">15.00</span></span>     |
| <span data-ttu-id="05d37-143">85,00</span><span class="sxs-lookup"><span data-stu-id="05d37-143">85.00</span></span>                  | <span data-ttu-id="05d37-144">85,00 \* 0,20</span><span class="sxs-lookup"><span data-stu-id="05d37-144">85.00 \* 0.20</span></span>  | <span data-ttu-id="05d37-145">17,00</span><span class="sxs-lookup"><span data-stu-id="05d37-145">17.00</span></span>     |
| <span data-ttu-id="05d37-146">305,00</span><span class="sxs-lookup"><span data-stu-id="05d37-146">305.00</span></span>                 | <span data-ttu-id="05d37-147">305,00 \* 0,10</span><span class="sxs-lookup"><span data-stu-id="05d37-147">305.00 \* 0.10</span></span> | <span data-ttu-id="05d37-148">30,50</span><span class="sxs-lookup"><span data-stu-id="05d37-148">30.50</span></span>     |

## <a name="example-interval-method-of-calculation"></a><span data-ttu-id="05d37-149"> Örnek: Aralık hesaplama yöntemi</span><span class="sxs-lookup"><span data-stu-id="05d37-149">Example: Interval method of calculation</span></span>
<span data-ttu-id="05d37-150">Değerler sayfasında, satış vergisi oranları aşağıdaki aralıklarda belirlenir:</span><span class="sxs-lookup"><span data-stu-id="05d37-150">In the Values page, sales tax rates are set up in the following intervals:</span></span>

|                   |                   |              |
|-------------------|-------------------|--------------|
| <span data-ttu-id="05d37-151">**Minimum sınır**</span><span class="sxs-lookup"><span data-stu-id="05d37-151">**Minimum limit**</span></span> | <span data-ttu-id="05d37-152">**Maksimum sınır**</span><span class="sxs-lookup"><span data-stu-id="05d37-152">**Maximum limit**</span></span> | <span data-ttu-id="05d37-153">**Vergi oranı**</span><span class="sxs-lookup"><span data-stu-id="05d37-153">**Tax rate**</span></span> |
| <span data-ttu-id="05d37-154">0,00</span><span class="sxs-lookup"><span data-stu-id="05d37-154">0.00</span></span>              | <span data-ttu-id="05d37-155">50,00</span><span class="sxs-lookup"><span data-stu-id="05d37-155">50.00</span></span>             | <span data-ttu-id="05d37-156">%30</span><span class="sxs-lookup"><span data-stu-id="05d37-156">30%</span></span>          |
| <span data-ttu-id="05d37-157">50,00</span><span class="sxs-lookup"><span data-stu-id="05d37-157">50.00</span></span>             | <span data-ttu-id="05d37-158">100,00</span><span class="sxs-lookup"><span data-stu-id="05d37-158">100.00</span></span>            | <span data-ttu-id="05d37-159">%20</span><span class="sxs-lookup"><span data-stu-id="05d37-159">20%</span></span>          |
| <span data-ttu-id="05d37-160">100,00</span><span class="sxs-lookup"><span data-stu-id="05d37-160">100.00</span></span>            | <span data-ttu-id="05d37-161">0,00</span><span class="sxs-lookup"><span data-stu-id="05d37-161">0.00</span></span>              | <span data-ttu-id="05d37-162">%10</span><span class="sxs-lookup"><span data-stu-id="05d37-162">10%</span></span>          |

<span data-ttu-id="05d37-163">Satış vergisi her tutar aralığı için hesaplanan vergi tutarlarının toplamıdır.</span><span class="sxs-lookup"><span data-stu-id="05d37-163">The sales tax is the sum of the tax amounts that are calculated for each amount interval.</span></span>

| <span data-ttu-id="05d37-164">Vergiye tabi tutar (fiyat)</span><span class="sxs-lookup"><span data-stu-id="05d37-164">Taxable amount (price)</span></span> | <span data-ttu-id="05d37-165">Hesaplama</span><span class="sxs-lookup"><span data-stu-id="05d37-165">Calculation</span></span>                                                               | <span data-ttu-id="05d37-166">Satış vergisi</span><span class="sxs-lookup"><span data-stu-id="05d37-166">Sales tax</span></span> |
|------------------------|---------------------------------------------------------------------------|-----------|
| <span data-ttu-id="05d37-167">35,00</span><span class="sxs-lookup"><span data-stu-id="05d37-167">35.00</span></span>                  | <span data-ttu-id="05d37-168">35,00 \* 0,30</span><span class="sxs-lookup"><span data-stu-id="05d37-168">35.00 \* 0.30</span></span>                                                             | <span data-ttu-id="05d37-169">10,50</span><span class="sxs-lookup"><span data-stu-id="05d37-169">10.50</span></span>     |
| <span data-ttu-id="05d37-170">50,00</span><span class="sxs-lookup"><span data-stu-id="05d37-170">50.00</span></span>                  | <span data-ttu-id="05d37-171">50,00 \* 0,30</span><span class="sxs-lookup"><span data-stu-id="05d37-171">50.00 \* 0.30</span></span>                                                             | <span data-ttu-id="05d37-172">15,00</span><span class="sxs-lookup"><span data-stu-id="05d37-172">15.00</span></span>     |
| <span data-ttu-id="05d37-173">85,00</span><span class="sxs-lookup"><span data-stu-id="05d37-173">85.00</span></span>                  | <span data-ttu-id="05d37-174">(50,00 \* 0,30 = 15,00) + (35,00 \* 0,20 = 7,00)</span><span class="sxs-lookup"><span data-stu-id="05d37-174">(50.00 \* 0.30 = 15.00) + (35.00 \* 0.20 = 7.00)</span></span>                          | <span data-ttu-id="05d37-175">22,00</span><span class="sxs-lookup"><span data-stu-id="05d37-175">22.00</span></span>     |
| <span data-ttu-id="05d37-176">305,00</span><span class="sxs-lookup"><span data-stu-id="05d37-176">305.00</span></span>                 | <span data-ttu-id="05d37-177">(50,00 \* 0,30 = 15,00) + (50,00 \* 0,20 = 10,00) + (205 \* 0,10 = 20,50)</span><span class="sxs-lookup"><span data-stu-id="05d37-177">(50.00 \* 0.30 = 15.00) + (50.00 \* 0.20 = 10.00) + (205 \* 0.10 = 20.50)</span></span> | <span data-ttu-id="05d37-178">45,50</span><span class="sxs-lookup"><span data-stu-id="05d37-178">45.50</span></span>     |



<span data-ttu-id="05d37-179">Daha fazla bilgi için bkz. [Marjinal taban ve hesaplama yöntemi alanları temel alınarak satış vergisi oranlarını belirleme](marginal-base-field.md).</span><span class="sxs-lookup"><span data-stu-id="05d37-179">For more information, see [Determining sale tax rates based on the Marginal base and Calculation method fields](marginal-base-field.md).</span></span>





