---
title: Marjinal taban ve Hesaplama yöntemi temel alınarak Satış vergisi oranları
description: Bu konuda, Marjinal taban ve Hesaplama yöntemi alanlarındaki değerlerin, satış ve satınalma hareketlerindeki vergi oran(lar)ını nasıl belirlediği açıklanmaktadır.
author: ShylaThompson
manager: AnnBe
ms.date: 10/26/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxTable
audience: Application User
ms.reviewer: roschlom
ms.custom: 7171
ms.assetid: 381fc309-b32a-4927-b5b8-fa1c31b0bd72
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2dcb51c730da3f2ad155675f06f5c1cd9e8476d2
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/15/2021
ms.locfileid: "4988678"
---
# <a name="sales-tax-rates-based-on-the-marginal-base-and-calculation-methods"></a><span data-ttu-id="81c00-103">Marjinal taban ve Hesaplama yöntemi temel alınarak Satış vergisi oranları</span><span class="sxs-lookup"><span data-stu-id="81c00-103">Sales tax rates based on the Marginal base and Calculation methods</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="81c00-104">Bu konuda, Marjinal taban ve Hesaplama yöntemi alanlarındaki değerlerin, satış ve satınalma hareketlerindeki vergi oran(lar)ını nasıl belirlediği açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="81c00-104">This topic explains how the values in the fields Marginal base and Calculation method determine the tax rate(s) in sales and purchase transactions.</span></span>

<span data-ttu-id="81c00-105">Satış vergisi kodları sayfasındaki Hesaplama hızlı sekmesi üzerindeki Marjinal taban, Satış vergisi kodu değerleri sayfasından uygun vergi oranlarının seçilmesinde hangi tutarın kullanılacağını belirler.</span><span class="sxs-lookup"><span data-stu-id="81c00-105">The Marginal base on the Calculation FastTab on the Sales tax codes page determines which amount is used to pick the appropriate tax rate(s) from the rates in the Sales tax code values page.</span></span> <span data-ttu-id="81c00-106">Marjinal taban alanındaki tutar türü, Hesaplama yöntemi alanındaki yöntem ile birlikte bir hareket için doğru vergi oranı/oranlarını bulmak için mantığı belirlemekte kullanılır.</span><span class="sxs-lookup"><span data-stu-id="81c00-106">The amount type in the Marginal base field in combination with the method in the Calculation method field determines the logic to find the correct tax rate(s) for a transaction.</span></span> 

<span data-ttu-id="81c00-107">Bu alanlardaki değerlerin çeşitli birleşimleri, aşağıdaki örneklerde görüldüğü gibi çok farklı satış vergisi hesaplamaları üretir.</span><span class="sxs-lookup"><span data-stu-id="81c00-107">Various combinations of values in these fields produce very different sales tax calculations, as shown by the following examples.</span></span> <span data-ttu-id="81c00-108">Bu örnekler, her bir vergi kodu için Satış vergi kodu değerleri sayfasında ayarlananlarla aynı vergi aralığı değerlerini kullanılır.</span><span class="sxs-lookup"><span data-stu-id="81c00-108">The examples use the same tax interval values, which are set up for each tax code in the Sales tax codes values page.</span></span> <span data-ttu-id="81c00-109">Bu sayfayı açmak için Satış vergisi kodu &gt; Satış vergi kodlarındaki değerler sayfasını tıklatın.</span><span class="sxs-lookup"><span data-stu-id="81c00-109">To open this page, click Sales tax code &gt; Values in the Sales tax codes page.</span></span>

> [!Important]                                                                                                                  
> <span data-ttu-id="81c00-110">Eğer bir ya da birden fazla satış vergisi kodunuzun Marjinal tabanı tutarlar veya birimlere dayanıyorsa, Genel muhasebe defteri parametreleri sayfasındaki Hesaplama yöntemi alanı Satır olarak ayarlanmalıdır.</span><span class="sxs-lookup"><span data-stu-id="81c00-110">If the Marginal base on one or more of your sales tax codes is based on line amounts or units, the value of the Calculation method field in the General ledger parameters page must be set to Line.</span></span> |

## <a name="net-amount-per-line"></a><span data-ttu-id="81c00-111"> Satır başına net tutar</span><span class="sxs-lookup"><span data-stu-id="81c00-111">Net amount per line</span></span>
<span data-ttu-id="81c00-112">Bu seçeneği işaretleyip satış vergisi oranını, fatura satırlarının net tutarına dayanarak, diğer vergileri hariç bırakarak belirleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="81c00-112">Select this option to determine sales tax rates based on the net amount for the invoice lines, excluding any other taxes.</span></span>

### <a name="example"></a><span data-ttu-id="81c00-113">Örnek</span><span class="sxs-lookup"><span data-stu-id="81c00-113">Example</span></span>

<span data-ttu-id="81c00-114">Satış vergisi oranları aşağıdaki aralıklarda belirlenir.</span><span class="sxs-lookup"><span data-stu-id="81c00-114">The sales tax rates are set up in the following intervals.</span></span>

| <span data-ttu-id="81c00-115">Tutar aralığı</span><span class="sxs-lookup"><span data-stu-id="81c00-115">Amount interval</span></span>    | <span data-ttu-id="81c00-116">Vergi oranı</span><span class="sxs-lookup"><span data-stu-id="81c00-116">Tax rate</span></span> |
|--------------------|----------|
| <span data-ttu-id="81c00-117">0 - 50</span><span class="sxs-lookup"><span data-stu-id="81c00-117">0 - 50</span></span>             | <span data-ttu-id="81c00-118">%30</span><span class="sxs-lookup"><span data-stu-id="81c00-118">30%</span></span>      |
| <span data-ttu-id="81c00-119">50 - 100</span><span class="sxs-lookup"><span data-stu-id="81c00-119">50 - 100</span></span>           | <span data-ttu-id="81c00-120">%20</span><span class="sxs-lookup"><span data-stu-id="81c00-120">20%</span></span>      |
| <span data-ttu-id="81c00-121">100 - 0 (&gt; 100)</span><span class="sxs-lookup"><span data-stu-id="81c00-121">100 - 0 (&gt; 100)</span></span> | <span data-ttu-id="81c00-122">%10</span><span class="sxs-lookup"><span data-stu-id="81c00-122">10%</span></span>      |

> [!NOTE]                                                                                                             
> <span data-ttu-id="81c00-123">Son aralıktaki sıfır (0) üst sınırı, 100'ü geçen tüm miktarların aralığa dahil edileceği anlamına gelir.</span><span class="sxs-lookup"><span data-stu-id="81c00-123">The upper limit of zero (0) in the last interval means that all amounts that exceed 100 are included in the interval.</span></span>

<span data-ttu-id="81c00-124">Marjinal taban: **Satır başına net tutar**</span><span class="sxs-lookup"><span data-stu-id="81c00-124">Marginal base: **Net amount per line**</span></span> 

<span data-ttu-id="81c00-125">Hesaplama Yöntemi: **Aralık**</span><span class="sxs-lookup"><span data-stu-id="81c00-125">Calculation method: **Interval**</span></span> 

<span data-ttu-id="81c00-126">Her biri 25,00 olan 8 lamba satın alırsınız.</span><span class="sxs-lookup"><span data-stu-id="81c00-126">You buy 8 lamps that cost 25.00 each.</span></span> 

<span data-ttu-id="81c00-127">Fatura satırının net tutarı 200,00 olur.</span><span class="sxs-lookup"><span data-stu-id="81c00-127">The net amount for the invoice line is 200.00.</span></span> 

<span data-ttu-id="81c00-128">Vergi aşağıdaki gibi hesaplanır:</span><span class="sxs-lookup"><span data-stu-id="81c00-128">The tax is calculated as follows:</span></span> 

<span data-ttu-id="81c00-129">Toplam satış vergisi = 50 x %30 + 50 x %20 + 100 x %10 = 15 + 10 + 10 = 35,00</span><span class="sxs-lookup"><span data-stu-id="81c00-129">Total sales tax = 50 x 30% + 50 x 20% + 100 x 10% = 15 + 10 + 10 = 35.00</span></span> 

<span data-ttu-id="81c00-130">Toplam fatura tutarı = 200,00 + 35,00 = 235,00</span><span class="sxs-lookup"><span data-stu-id="81c00-130">Total invoice amount = 200.00 + 35.00 = 235.00</span></span> 

<span data-ttu-id="81c00-131">**Fark**</span><span class="sxs-lookup"><span data-stu-id="81c00-131">**Variation**</span></span> 

<span data-ttu-id="81c00-132">Faturada her satırda dört madde olan iki satır varsa, her satırdaki net tutar 100,00 olur ve satış vergisi şu şekilde hesaplanır:</span><span class="sxs-lookup"><span data-stu-id="81c00-132">If the invoice has two lines with four items on each line, the net amount on each line is 100.00 and the sales tax is calculated as follows:</span></span> 

<span data-ttu-id="81c00-133">Satış vergisi satırı 1 = 50 x %30 + 50 x %20 = 15 + 10 = 25,00</span><span class="sxs-lookup"><span data-stu-id="81c00-133">Sales tax line 1 = 50 x 30% + 50 x 20% = 15 + 10 = 25.00</span></span> 

<span data-ttu-id="81c00-134">Satış vergisi satırı 2 = 50 x %30 + 50 x %20 = 15 + 10 = 25,00</span><span class="sxs-lookup"><span data-stu-id="81c00-134">Sales tax line 2 = 50 x 30% + 50 x 20% = 15 + 10 = 25.00</span></span> 

<span data-ttu-id="81c00-135">Toplam satış vergisi = 25,00 + 25,00 = 50,00</span><span class="sxs-lookup"><span data-stu-id="81c00-135">Total sales tax = 25.00 + 25.00 = 50.00</span></span> 

<span data-ttu-id="81c00-136">Toplam fatura tutarı = 200,00 + 50,00 = 250,00</span><span class="sxs-lookup"><span data-stu-id="81c00-136">Total invoice amount = 200.00 + 50.00 = 250.00</span></span>

## <a name="net-amount-per-unit"></a><span data-ttu-id="81c00-137"> Birim başına net tutar</span><span class="sxs-lookup"><span data-stu-id="81c00-137">Net amount per unit</span></span>
<span data-ttu-id="81c00-138">Bu seçeneği, satış vergisi oranlarını, diğer vergiler hariç her birimin değerini esas alarak belirlemek için.</span><span class="sxs-lookup"><span data-stu-id="81c00-138">Select this option to determine sales tax rates based on the value of each unit, excluding any other taxes.</span></span> <span data-ttu-id="81c00-139">Birime dayalı bir marjinal taban seçilirse, satış vergisi kodu için bir Birim'in de belirlenmesi gereklidir.</span><span class="sxs-lookup"><span data-stu-id="81c00-139">When a unit based Marginal base is selected then also a Unit has to be specified for the Sales tax code.</span></span>

### <a name="example"></a><span data-ttu-id="81c00-140">Örnek</span><span class="sxs-lookup"><span data-stu-id="81c00-140">Example</span></span>

<span data-ttu-id="81c00-141">Satış vergisi oranları aşağıdaki aralıklarda belirlenir.</span><span class="sxs-lookup"><span data-stu-id="81c00-141">The sales tax rates are set up in the following intervals.</span></span>

| <span data-ttu-id="81c00-142">Tutar</span><span class="sxs-lookup"><span data-stu-id="81c00-142">Amount</span></span>             | <span data-ttu-id="81c00-143">Vergi oranı</span><span class="sxs-lookup"><span data-stu-id="81c00-143">Tax rate</span></span> |
|--------------------|----------|
| <span data-ttu-id="81c00-144">0 - 50</span><span class="sxs-lookup"><span data-stu-id="81c00-144">0 - 50</span></span>             | <span data-ttu-id="81c00-145">%30</span><span class="sxs-lookup"><span data-stu-id="81c00-145">30%</span></span>      |
| <span data-ttu-id="81c00-146">50 - 100</span><span class="sxs-lookup"><span data-stu-id="81c00-146">50 - 100</span></span>           | <span data-ttu-id="81c00-147">%20</span><span class="sxs-lookup"><span data-stu-id="81c00-147">20%</span></span>      |
| <span data-ttu-id="81c00-148">100 - 0 (&gt; 100)</span><span class="sxs-lookup"><span data-stu-id="81c00-148">100 - 0 (&gt; 100)</span></span> | <span data-ttu-id="81c00-149">%10</span><span class="sxs-lookup"><span data-stu-id="81c00-149">10%</span></span>      |

<span data-ttu-id="81c00-150">Marjinal taban: **Birim başına net tutar**</span><span class="sxs-lookup"><span data-stu-id="81c00-150">Marginal base: **Net amount per unit**</span></span> 

<span data-ttu-id="81c00-151">Hesaplama yöntemi = **Tam tutar**</span><span class="sxs-lookup"><span data-stu-id="81c00-151">Calculation method: **Whole amount**</span></span> 

<span data-ttu-id="81c00-152">Her biri 25,00 olan 8 lamba satın alırsınız.</span><span class="sxs-lookup"><span data-stu-id="81c00-152">You buy 8 lamps that cost 25.00 each.</span></span> 

<span data-ttu-id="81c00-153">Fatura satırının net tutarı 200,00 olur.</span><span class="sxs-lookup"><span data-stu-id="81c00-153">The net amount for the invoice line is 200.00.</span></span> 

<span data-ttu-id="81c00-154">Vergi aşağıdaki gibi hesaplanır: Birim başına satış vergisi = 25,00 x %30 = 7.50 Toplam satış vergisi = 8 birim x 7,50 = 60,00 Toplam fatura tutarı = 200,00 + 60,00 = 260,00</span><span class="sxs-lookup"><span data-stu-id="81c00-154">The tax is calculated as follows: Sales tax per unit = 25.00 x 30% = 7.50 Total sales tax = 7.50 x 8 units = 60.00 Total invoice amount = 200.00 + 60.00 = 260.00</span></span>

## <a name="net-amount-of-invoice-balance"></a><span data-ttu-id="81c00-155"> Fatura bakiyesinin net tutarı</span><span class="sxs-lookup"><span data-stu-id="81c00-155">Net amount of invoice balance</span></span>

<span data-ttu-id="81c00-156">Bu seçeneği işaretleyip satış vergisi oranını, fatura satırlarının toplam değerine dayanarak, diğer vergileri hariç bırakarak belirleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="81c00-156">Select this option to determine sales tax rates based on the total value for the invoice, excluding any other taxes.</span></span>

### <a name="example"></a><span data-ttu-id="81c00-157">Örnek</span><span class="sxs-lookup"><span data-stu-id="81c00-157">Example</span></span>

<span data-ttu-id="81c00-158">Satış vergisi oranları aşağıdaki aralıklarda belirlenir.</span><span class="sxs-lookup"><span data-stu-id="81c00-158">The sales tax rates are set up in the following intervals.</span></span>

| <span data-ttu-id="81c00-159">Tutar</span><span class="sxs-lookup"><span data-stu-id="81c00-159">Amount</span></span>            | <span data-ttu-id="81c00-160">Vergi oranı</span><span class="sxs-lookup"><span data-stu-id="81c00-160">Tax rate</span></span> |
|-------------------|----------|
| <span data-ttu-id="81c00-161">0 - 50</span><span class="sxs-lookup"><span data-stu-id="81c00-161">0 - 50</span></span>            | <span data-ttu-id="81c00-162">%30</span><span class="sxs-lookup"><span data-stu-id="81c00-162">30%</span></span>      |
| <span data-ttu-id="81c00-163">50 - 100</span><span class="sxs-lookup"><span data-stu-id="81c00-163">50 - 100</span></span>          | <span data-ttu-id="81c00-164">%20</span><span class="sxs-lookup"><span data-stu-id="81c00-164">20%</span></span>      |
| <span data-ttu-id="81c00-165">100 -0 (&gt; 100)</span><span class="sxs-lookup"><span data-stu-id="81c00-165">100 -0 (&gt; 100)</span></span> | <span data-ttu-id="81c00-166">%10</span><span class="sxs-lookup"><span data-stu-id="81c00-166">10%</span></span>      |

<span data-ttu-id="81c00-167">Marjinal taban: **Fatura bakiyesinin net tutarı**</span><span class="sxs-lookup"><span data-stu-id="81c00-167">Marginal base: **Net amount of invoice balance**</span></span> 

<span data-ttu-id="81c00-168">Hesaplama yöntemi: **Aralık** Satış faturasının 2 satırı ve her satırda tanesi 25,00 olan 4 lambası vardır.</span><span class="sxs-lookup"><span data-stu-id="81c00-168">Calculation method: **Interval** A sales invoice has 2 lines with 4 lamps on each lines for 25.00 each.</span></span> <span data-ttu-id="81c00-169">Fatura bakiyesinin net tutarı 4 x 25,00 + 4 x 25,00 = 200,00 olur.</span><span class="sxs-lookup"><span data-stu-id="81c00-169">The net amount of invoice balance is 4 x 25.00 + 4 x 25.00 = 200.00.</span></span> <span data-ttu-id="81c00-170">Vergi aşağıdaki gibi hesaplanır: Toplam satış vergisi = 50 x 0,30 + 50 x 0,20 + 100 x 0,10 = 15 + 10 + 10 = 35,00 Toplam fatura tutarı = 200,00 + 35,00 = 235,00</span><span class="sxs-lookup"><span data-stu-id="81c00-170">The tax is calculated as follows: Total sales tax = 50 x 0.30 + 50 x 0.20 + 100 x 0.10 = 15 + 10 + 10 = 35.00 Total invoice amount = 200.00 + 35.00 = 235.00</span></span>

## <a name="gross-amount-per-line"></a><span data-ttu-id="81c00-171"> Satır başına brüt tutar</span><span class="sxs-lookup"><span data-stu-id="81c00-171">Gross amount per line</span></span>

<span data-ttu-id="81c00-172">Bu seçeneği işaretleyip satış vergisi oranını, satırın değeri için, bu satırın tüm diğer vergiler dahil olmak üzere belirleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="81c00-172">Select this option to determine sales tax rates based on the value of the line including all other taxes for that line.</span></span>

> [!NOTE]
> <span data-ttu-id="81c00-173">Bir satış vergisi grubunda, Marjinal taban alanında bu seçime sahip yalnızca bir satış vergisi kodunuz olabilir.</span><span class="sxs-lookup"><span data-stu-id="81c00-173">In a sales tax group, you can only have one sales tax code with this selection in the Marginal base field.</span></span>

### <a name="example"></a><span data-ttu-id="81c00-174">Örnek</span><span class="sxs-lookup"><span data-stu-id="81c00-174">Example</span></span>

<span data-ttu-id="81c00-175">Satış vergisi oranları aşağıdaki aralıklarda belirlenir.</span><span class="sxs-lookup"><span data-stu-id="81c00-175">The sales tax rates are set up in the following intervals.</span></span>

| <span data-ttu-id="81c00-176">Tutar</span><span class="sxs-lookup"><span data-stu-id="81c00-176">Amount</span></span>             | <span data-ttu-id="81c00-177">Vergi oranı</span><span class="sxs-lookup"><span data-stu-id="81c00-177">Tax rate</span></span> |
|--------------------|----------|
| <span data-ttu-id="81c00-178">0 - 50</span><span class="sxs-lookup"><span data-stu-id="81c00-178">0 - 50</span></span>             | <span data-ttu-id="81c00-179">%30</span><span class="sxs-lookup"><span data-stu-id="81c00-179">30%</span></span>      |
| <span data-ttu-id="81c00-180">50 - 100</span><span class="sxs-lookup"><span data-stu-id="81c00-180">50 - 100</span></span>           | <span data-ttu-id="81c00-181">%20</span><span class="sxs-lookup"><span data-stu-id="81c00-181">20%</span></span>      |
| <span data-ttu-id="81c00-182">100 - 0 (&gt; 100)</span><span class="sxs-lookup"><span data-stu-id="81c00-182">100 - 0 (&gt; 100)</span></span> | <span data-ttu-id="81c00-183">%10</span><span class="sxs-lookup"><span data-stu-id="81c00-183">10%</span></span>      |

<span data-ttu-id="81c00-184">Marjinal taban: **Satır başına brüt tutar** Hesaplama yöntemi: **Aralık** Ayrıca her lamba için hesaplanan 5,00 tutarında vergi kodu özel harç mevcuttur.</span><span class="sxs-lookup"><span data-stu-id="81c00-184">Marginal base: **Gross amount per line** Calculation method: **Interval** Additionally there is another tax code calculated for a special duty of 5.00 on each lamp.</span></span> <span data-ttu-id="81c00-185">Bu harç, satış vergisi hesaplamasından önce net tutara eklenir.</span><span class="sxs-lookup"><span data-stu-id="81c00-185">The duty is added to the net amount before the sales tax calculation.</span></span> <span data-ttu-id="81c00-186">Her biri 25,00 olan 8 lamba satın alırsınız.</span><span class="sxs-lookup"><span data-stu-id="81c00-186">You buy 8 lamps that cost 25.00 each.</span></span> <span data-ttu-id="81c00-187">Fatura satırının net tutarı 200,00 olur.</span><span class="sxs-lookup"><span data-stu-id="81c00-187">The net amount for the invoice line is 200.00.</span></span> <span data-ttu-id="81c00-188">Fatura satırının brüt tutarı 8 x 25,00 + 8 x 5,00 = 240,00 olur.</span><span class="sxs-lookup"><span data-stu-id="81c00-188">The gross amount for the invoice line is 8 x 25.00 + 8 x 5.00 = 240.00.</span></span> <span data-ttu-id="81c00-189">Vergi aşağıdaki gibi hesaplanır: Toplam satış vergisi = 50 x 0,30 + 50 x 0,20 + 140 x 0,10 = 15 + 20 + 14 = 39,00 Toplam vergi 5,00 x 8 = 40,00 = Toplam fatura tutarı 200,00 + 39,00 + 40,00 = 279,00</span><span class="sxs-lookup"><span data-stu-id="81c00-189">The tax is calculated as follows: Total sales tax = 50 x 0.30 + 50 x 0.20 + 140 x 0.10 = 15 + 20 + 14 = 39.00 Total duty = 5.00 x 8 = 40.00 Total invoice amount = 200.00 + 39.00 + 40.00 = 279.00</span></span>

<span data-ttu-id="81c00-190">**Fark**</span><span class="sxs-lookup"><span data-stu-id="81c00-190">**Variation**</span></span> 

<span data-ttu-id="81c00-191">Fatura her satırda 4 madde olan 2 fatura satırı kullanılarak oluşturulursa, fatura satırı başına net tutar 100,00 olur.</span><span class="sxs-lookup"><span data-stu-id="81c00-191">If the invoice is created by using 2 invoice lines with 4 items on each line, the net amount per invoice line is 100.00.</span></span> <span data-ttu-id="81c00-192">Fatura satırı bazında (4 x 5.00 harcı dahil) brüt tutarı 120,00 olur ve satış vergisi aşağıdaki gibi oluşturulur: Satış vergisi fatura satırı 1 = 50 x 0,30 + 50 x 0,20 + 20 x 0,10 = 15 + 10 + 2 = 27,00 Satış vergisi fatura satırı 2 = 50 x 0,30 + 50 x 0,20 + 20 x 0,10 = 15 + 10 + 2 = 27,00 Toplam satış vergisi 27,00 + 27,00 = 54,00 Toplam vergi 5,00 x 8 = 40,00 Toplam fatura tutarı 200,00 + 54,00 + 40,00 = 294,00</span><span class="sxs-lookup"><span data-stu-id="81c00-192">The gross amount (including the duty of 4 x 5.00) per invoice line would be 120.00, and the sales tax is created as follows: Sales tax invoice line 1 = 50 x 0.30 + 50 x 0.20 + 20 x 0.10 = 15 + 10 + 2 = 27.00 Sales tax invoice line 2 = 50 x 0.30 + 50 x 0.20 + 20 x 0.10 = 15 + 10 + 2 = 27.00 Total sales tax = 27.00 + 27.00 = 54.00 Total duty = 5.00 x 8 = 40.00 Total invoice amount = 200.00 + 54.00 + 40.00 = 294.00</span></span>

## <a name="gross-amount-per-unit"></a><span data-ttu-id="81c00-193"> Birim başına brüt tutar</span><span class="sxs-lookup"><span data-stu-id="81c00-193">Gross amount per unit</span></span>

<span data-ttu-id="81c00-194">Bu seçeneği, satış vergisi oranlarını, diğer vergiler dahil, birimin değerini esas alarak belirlemek için.</span><span class="sxs-lookup"><span data-stu-id="81c00-194">Select this option to determine sales tax rates based on the value of the unit including any other taxes.</span></span>

> [!NOTE]
> <span data-ttu-id="81c00-195">Bir satış vergisi grubunda, Marjinal taban alanında bu seçime sahip yalnızca bir satış vergisi kodunuz olabilir.</span><span class="sxs-lookup"><span data-stu-id="81c00-195">In a sales tax group, you can only have one sales tax code with this selection in the Marginal base field.</span></span>

### <a name="example"></a><span data-ttu-id="81c00-196">Örnek</span><span class="sxs-lookup"><span data-stu-id="81c00-196">Example</span></span>

<span data-ttu-id="81c00-197">Satış vergisi oranları aşağıdaki aralıklarda belirlenir.</span><span class="sxs-lookup"><span data-stu-id="81c00-197">The sales tax rates are set up in the following intervals.</span></span>

| <span data-ttu-id="81c00-198">Tutar</span><span class="sxs-lookup"><span data-stu-id="81c00-198">Amount</span></span>             | <span data-ttu-id="81c00-199">Vergi oranı</span><span class="sxs-lookup"><span data-stu-id="81c00-199">Tax rate</span></span> |
|--------------------|----------|
| <span data-ttu-id="81c00-200">0 - 50</span><span class="sxs-lookup"><span data-stu-id="81c00-200">0 - 50</span></span>             | <span data-ttu-id="81c00-201">%30</span><span class="sxs-lookup"><span data-stu-id="81c00-201">30%</span></span>      |
| <span data-ttu-id="81c00-202">50 - 100</span><span class="sxs-lookup"><span data-stu-id="81c00-202">50 - 100</span></span>           | <span data-ttu-id="81c00-203">%20</span><span class="sxs-lookup"><span data-stu-id="81c00-203">20%</span></span>      |
| <span data-ttu-id="81c00-204">100 - 0 (&gt; 100)</span><span class="sxs-lookup"><span data-stu-id="81c00-204">100 - 0 (&gt; 100)</span></span> | <span data-ttu-id="81c00-205">%10</span><span class="sxs-lookup"><span data-stu-id="81c00-205">10%</span></span>      |

<span data-ttu-id="81c00-206">Marjinal taban: **Birim başına brüt tutar** Her lamba üzerinde 5,00 özel vergi var.</span><span class="sxs-lookup"><span data-stu-id="81c00-206">Marginal base: **Gross amount per unit** There is a special duty of 5.00 on each lamp.</span></span> <span data-ttu-id="81c00-207">Bu harç, satış vergisi hesaplamasından önce net tutara eklenir.</span><span class="sxs-lookup"><span data-stu-id="81c00-207">The duty is added to the net amount before the sales tax calculation.</span></span> <span data-ttu-id="81c00-208">Her biri 25,00 olan 8 lamba satın alırsınız.</span><span class="sxs-lookup"><span data-stu-id="81c00-208">You buy 8 lamps that cost 25.00 each.</span></span> <span data-ttu-id="81c00-209">Birim başına brüt tutarı 30,00 olur.</span><span class="sxs-lookup"><span data-stu-id="81c00-209">The gross amount per unit is 30.00.</span></span> <span data-ttu-id="81c00-210">Vergi aşağıdaki gibi hesaplanır: Birim başına satış vergisi = 30 x %30 = 9,00 Toplam satış vergisi 9,00 x 8 = 72,00 Toplam harç = 5,00 x 8 = 40,00 Toplam fatura miktarı = 200,00 + 72,00 + 40,00 = 312,00</span><span class="sxs-lookup"><span data-stu-id="81c00-210">The tax is calculated as follows: Sales tax per unit = 30 x 30% = 9.00 Total sales tax = 9.00 x 8 = 72.00 Total duty = 5.00 x 8 = 40.00 Total invoice amount = 200.00 + 72.00 + 40.00 = 312.00</span></span>

## <a name="invoice-total-incl-other-sales-tax-amounts"></a><span data-ttu-id="81c00-211"> Diğer satış vergilerinin tutarları dahil fatura toplamı</span><span class="sxs-lookup"><span data-stu-id="81c00-211">Invoice total incl. other sales tax amounts</span></span>

<span data-ttu-id="81c00-212">Bu seçeneği işaretleyip satış vergisi oranını, fatura satırlarının toplam değerine dayanarak, diğer vergiler dahil olarak belirleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="81c00-212">Select this option to determine sales tax rates based on the total value for the invoice including any other taxes.</span></span>
> [!NOTE]
> <span data-ttu-id="81c00-213">Bir satış vergisi grubunda, Marjinal taban alanında bu seçime sahip yalnızca bir satış vergisi kodunuz olabilir</span><span class="sxs-lookup"><span data-stu-id="81c00-213">In a sales tax group, you can only have one sales tax code with this selection in the Marginal base field</span></span>

### <a name="example"></a><span data-ttu-id="81c00-214">Örnek</span><span class="sxs-lookup"><span data-stu-id="81c00-214">Example</span></span>

<span data-ttu-id="81c00-215">Satış vergisi oranları aşağıdaki aralıklarda belirlenir.</span><span class="sxs-lookup"><span data-stu-id="81c00-215">The sales tax rates are set up in the following intervals.</span></span>

| <span data-ttu-id="81c00-216">Tutar</span><span class="sxs-lookup"><span data-stu-id="81c00-216">Amount</span></span>             | <span data-ttu-id="81c00-217">Vergi oranı</span><span class="sxs-lookup"><span data-stu-id="81c00-217">Tax rate</span></span> |
|--------------------|----------|
| <span data-ttu-id="81c00-218">0 - 50</span><span class="sxs-lookup"><span data-stu-id="81c00-218">0 - 50</span></span>             | <span data-ttu-id="81c00-219">%30</span><span class="sxs-lookup"><span data-stu-id="81c00-219">30%</span></span>      |
| <span data-ttu-id="81c00-220">50 - 100</span><span class="sxs-lookup"><span data-stu-id="81c00-220">50 - 100</span></span>           | <span data-ttu-id="81c00-221">%20</span><span class="sxs-lookup"><span data-stu-id="81c00-221">20%</span></span>      |
| <span data-ttu-id="81c00-222">100 - 0 (&gt; 100)</span><span class="sxs-lookup"><span data-stu-id="81c00-222">100 - 0 (&gt; 100)</span></span> | <span data-ttu-id="81c00-223">%10</span><span class="sxs-lookup"><span data-stu-id="81c00-223">10%</span></span>      |

<span data-ttu-id="81c00-224">Marjinal taban: **Diğer satış vergisi tutarları dahil fatura toplamı** Hesaplama yöntemi: **Aralık** </span><span class="sxs-lookup"><span data-stu-id="81c00-224">Marginal base: **Invoice total incl. other sales tax amounts** Calculation method: **Interval** </span></span>  
<span data-ttu-id="81c00-225">Her lambada 5,00 değerinde özel bir harç vardır.</span><span class="sxs-lookup"><span data-stu-id="81c00-225">There is a special duty of 5.00 on each lamp.</span></span> <span data-ttu-id="81c00-226">Bu harç, satış vergisi hesaplamasından önce net tutara eklenir.</span><span class="sxs-lookup"><span data-stu-id="81c00-226">The duty is added to the net amount before the sales tax calculation.</span></span> <span data-ttu-id="81c00-227">Her biri 25,00 olan 8 lamba satın alırsınız.</span><span class="sxs-lookup"><span data-stu-id="81c00-227">You buy 8 lamps that cost 25.00 each.</span></span> <span data-ttu-id="81c00-228">Faturanın net tutarı 200,00 olur.</span><span class="sxs-lookup"><span data-stu-id="81c00-228">The net amount for the invoice is 200.00.</span></span> <span data-ttu-id="81c00-229">Faturanın brüt tutarı 200,00 + (8 x 5,00) = 240,00 olur.</span><span class="sxs-lookup"><span data-stu-id="81c00-229">The gross amount for the invoice is 200.00 + (8 x 5.00) = 240.00.</span></span> <span data-ttu-id="81c00-230">Vergi aşağıdaki gibi hesaplanır: Toplam satış vergisi = 50 x 0,30 + 50 x 0,20 + 140 x 0,10 = 15 + 10 + 14 = 39,00 Toplam vergi 5,00 x 8 = 40,00 = Toplam fatura tutarı 200,00 + 39,00 + 40,00 = 279,00</span><span class="sxs-lookup"><span data-stu-id="81c00-230">The tax is calculated as follows: Total sales tax = 50 x 0.30 + 50 x 0.20 + 140 x 0.10 = 15 + 10 + 14 = 39.00 Total duty = 5.00 x 8 = 40.00 Total invoice amount = 200.00 + 39.00 + 40.00 = 279.00</span></span>

<span data-ttu-id="81c00-231">Daha fazla bilgi için bkz. [Satış vergisi kodları için tam tutar ve Aralık hesaplaması seçenekleri](whole-amount-interval-options-sales-tax-codes.md) ve [Kaynak alanında satış vergisi hesaplama yöntemleri](sales-tax-calculation-methods-origin-field.md)</span><span class="sxs-lookup"><span data-stu-id="81c00-231">For more information, see [Whole amount and Interval calculation options for sales tax codes](whole-amount-interval-options-sales-tax-codes.md) and [Sales tax calculation methods in the Origin field](sales-tax-calculation-methods-origin-field.md).</span></span>



