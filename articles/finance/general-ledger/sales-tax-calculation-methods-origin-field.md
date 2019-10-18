---
title: Kaynak alanında satış vergisi hesaplama yöntemleri
description: Bu makalede satış vergisi kodları sayfasında Başlangıç alanındaki seçenekler ve satış vergisinin bir satış vergisi kodu için belirlenen seçeneğe göre nasıl hesaplanacağı hakkında bilgiler verilmiştir.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxTable
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations, Retail
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8ec6144599e9bb74333a663a56bdbf07b1999669
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/27/2019
ms.locfileid: "2180289"
---
# <a name="sales-tax-calculation-methods-in-the-origin-field"></a><span data-ttu-id="0a423-103">Kaynak alanında satış vergisi hesaplama yöntemleri</span><span class="sxs-lookup"><span data-stu-id="0a423-103">Sales tax calculation methods in the Origin field</span></span>

[!include [banner](../includes/banner.md)]

[!include [retail name](../includes/retail-name.md)]

<span data-ttu-id="0a423-104">Bu makalede satış vergisi kodları sayfasında Başlangıç alanındaki seçenekler ve satış vergisinin bir satış vergisi kodu için belirlenen seçeneğe göre nasıl hesaplanacağı hakkında bilgiler verilmiştir.</span><span class="sxs-lookup"><span data-stu-id="0a423-104">This article explains the options in the Origin field on the sales tax codes page and how sales tax is calculated based on the selected option for a sales tax code.</span></span>

<span data-ttu-id="0a423-105">Satış vergisi kodları sayfasında oluşturduğunuz her satış vergisi kodu için, Kaynak alanında vergi tabanı tutarına uygulanacak hesaplama yöntemini seçmelisiniz.</span><span class="sxs-lookup"><span data-stu-id="0a423-105">For each sales tax code that you create in the Sales tax codes page, you must select the method of calculation to apply to the tax base amount in the Origin field.</span></span>

## <a name="percentage-of-net-amount"></a><span data-ttu-id="0a423-106">Net tutar yüzdesi</span><span class="sxs-lookup"><span data-stu-id="0a423-106">Percentage of net amount</span></span>
<span data-ttu-id="0a423-107">Net tutar hesaplama yönteminin Yüzdesi Kaynak alanındaki varsayılan değerdir.</span><span class="sxs-lookup"><span data-stu-id="0a423-107">The Percentage of net amount calculation method is the default value in the Origin field.</span></span> <span data-ttu-id="0a423-108">Satış vergisi, diğer satış vergileri hariç olarak satınalma veya satış tutarının yüzdesi olarak hesaplanır.</span><span class="sxs-lookup"><span data-stu-id="0a423-108">The sales tax is calculated as a percentage of the purchase or sales amount, excluding any other sales taxes.</span></span>
### <a name="example"></a><span data-ttu-id="0a423-109">Örnek</span><span class="sxs-lookup"><span data-stu-id="0a423-109">Example</span></span>

<span data-ttu-id="0a423-110">Vergi oranı %25.</span><span class="sxs-lookup"><span data-stu-id="0a423-110">The tax rate is 25%.</span></span> <span data-ttu-id="0a423-111">Fatura satırı, her biri 1,00 seviyesinden 10 maddelik bir miktar gösterir ve müşteriye %10'luk bir satır iskontosu izni verilir.</span><span class="sxs-lookup"><span data-stu-id="0a423-111">The invoice line shows a quantity of 10 items at 1.00 each, and the customer is allowed a 10% line discount.</span></span> <span data-ttu-id="0a423-112">Net tutar: (10 x 1,00) -%10 = 9,00 Satış vergisi: 9,00 x %25 = 2,25 Toplam miktar: 9,00 + 2,25 = 11,25</span><span class="sxs-lookup"><span data-stu-id="0a423-112">Net amount: (10 x 1.00) -10% = 9.00 Sales tax: 9.00 x 25% = 2.25 Total amount: 9.00 + 2.25 = 11.25</span></span>

## <a name="percentage-of-gross-amount"></a><span data-ttu-id="0a423-113"> Brüt tutar yüzdesi</span><span class="sxs-lookup"><span data-stu-id="0a423-113">Percentage of gross amount</span></span>
<span data-ttu-id="0a423-114">Brüt tutar yüzdesi yöntemini seçerseniz, satış vergisi brüt satış tutarı yüzdesi olarak hesaplanır.</span><span class="sxs-lookup"><span data-stu-id="0a423-114">If you select the Percentage of gross amount method, the sales tax is calculated as a percentage of the gross sales amount.</span></span> <span data-ttu-id="0a423-115">Brüt tutar, satır net tutarı artı (Kaynak = Brüt tutar yüzdesi değerine sahip bir vergi hariç) satır için tüm vergiler ve harçlardır.</span><span class="sxs-lookup"><span data-stu-id="0a423-115">The gross amount is the line net amount plus all taxes and fees for the line except the one tax with Origin = Percentage of gross amount.</span></span>
### <a name="example"></a><span data-ttu-id="0a423-116">Örnek</span><span class="sxs-lookup"><span data-stu-id="0a423-116">Example</span></span>

<span data-ttu-id="0a423-117">Vergi dairesi bir maddeye özel vergi uygulamaktadır.</span><span class="sxs-lookup"><span data-stu-id="0a423-117">The tax authority has imposed special duties on an item.</span></span> <span data-ttu-id="0a423-118">Vergi tutarları, satış vergisi hesaplanmadan önce net tutara eklenir.</span><span class="sxs-lookup"><span data-stu-id="0a423-118">The duty amounts are added to the net amount before sales tax is calculated.</span></span> <span data-ttu-id="0a423-119">Aşağıdaki satış vergisi kodları durumunda:</span><span class="sxs-lookup"><span data-stu-id="0a423-119">Given the following sales tax codes:</span></span>
-   <span data-ttu-id="0a423-120">HARÇ 1 = %10 Net tutar yüzdesi hesaplama yöntemini kullanarak</span><span class="sxs-lookup"><span data-stu-id="0a423-120">DUTY 1 = 10%, using the Percentage of net amount calculation method</span></span>
-   <span data-ttu-id="0a423-121">HARÇ 2 = %20 Net tutar yüzdesi hesaplama yöntemini kullanarak</span><span class="sxs-lookup"><span data-stu-id="0a423-121">DUTY 2 = 20%, using the Percentage of net amount calculation method</span></span>
-   <span data-ttu-id="0a423-122">SATIŞ VERGİSİ = %25 Brüt tutar yüzdesi hesaplama yöntemini kullanarak</span><span class="sxs-lookup"><span data-stu-id="0a423-122">SALESTAX = 25%, using the Percentage of gross amount calculation method</span></span>

<span data-ttu-id="0a423-123">Net tutar 10.00 ise HARÇ 1, 1.00 (10.00 x %10) ve HARÇ 2 = 2.00'dir (10.00 x %20).</span><span class="sxs-lookup"><span data-stu-id="0a423-123">If the net amount is 10.00, then DUTY 1 is 1.00 (10.00 x 10%) and DUTY 2 = 2.00 (10.00 x 20%).</span></span> <span data-ttu-id="0a423-124">Tutarlar şu şekilde olacaktır: Brüt tutar: Net tutar + HARÇ 1 tutarı + HARÇ 2 tutarı (10.00 + 1.00 + 2.00) = 13.00 SATIŞ VERGİSİ = 13.00 x %25 = 3.25 Toplam HARÇLAR ve SATIŞ VERGİLERİ: 1.00 + 2.00 + 3.25 = 6.25 Toplam tutar: 10.00 + 6.25 = 16.25</span><span class="sxs-lookup"><span data-stu-id="0a423-124">The amounts would be as follows: Gross amount: Net amount + DUTY 1 amount + DUTY 2 amount (10.00 + 1.00 + 2.00) = 13.00 SALESTAX = 13.00 x 25% = 3.25 Total DUTIES and SALESTAX: 1.00 + 2.00 + 3.25 = 6.25 Total amount: 10.00 + 6.25 = 16.25</span></span>

| <span data-ttu-id="0a423-125">**Not**</span><span class="sxs-lookup"><span data-stu-id="0a423-125">**Note**</span></span>                                                                                                                                                                                                                 |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0a423-126">Hareket için Kaynak = Brüt tutar yüzdesi değerine sahip yalnızca bir vergi kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="0a423-126">Only one tax code with Origin = Percentage of gross amount can be used for a transaction.</span></span> <span data-ttu-id="0a423-127">Hareket için böyle birden fazla vergi kodu belirlenirse, satış vergisinin hesaplanamadığını bildiren bir hata iletisi görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="0a423-127">If more than one such tax code is determined for a transaction an error will be displayed that sales tax cannot be calculated.</span></span> |


<a name="percentage-of-sales-tax"></a><span data-ttu-id="0a423-128">Satış vergilerinin yüzdesi</span><span class="sxs-lookup"><span data-stu-id="0a423-128">Percentage of sales tax</span></span>
-----------------------

<span data-ttu-id="0a423-129">Köken alanında Satış vergisi yüzdesi değerini seçerseniz, satış vergisi, satış vergisi alanındaki Satış vergisi içinde seçili olan satış vergisinin yüzdesi olarak hesaplanır.</span><span class="sxs-lookup"><span data-stu-id="0a423-129">When you select Percentage of sales tax in the Origin field, sales tax is calculated as a percentage of the sales tax that is selected in the Sales tax on sales tax field.</span></span> <span data-ttu-id="0a423-130">Satış vergisi alanındaki Satış vergisi içinde seçili olan satış vergisi önce hesaplanır.</span><span class="sxs-lookup"><span data-stu-id="0a423-130">The sales tax that is selected in the Sales tax on sales tax field is calculated first.</span></span> <span data-ttu-id="0a423-131">İkinci satış vergisi daha sonra, ilk satış vergisi tutarı temel alınarak hesaplanır.</span><span class="sxs-lookup"><span data-stu-id="0a423-131">The second sales tax is then calculated based on the first sales tax amount.</span></span>
### <a name="example"></a><span data-ttu-id="0a423-132">Örnek</span><span class="sxs-lookup"><span data-stu-id="0a423-132">Example</span></span>

<span data-ttu-id="0a423-133">Aşağıdaki satış vergisi kodları durumunda:</span><span class="sxs-lookup"><span data-stu-id="0a423-133">Given the following sales tax codes:</span></span>
-   <span data-ttu-id="0a423-134">HARÇ 1 = %10 Net tutar yüzdesi yöntemini kullanarak</span><span class="sxs-lookup"><span data-stu-id="0a423-134">DUTY 1 = 10%, using the Percentage of net amount method</span></span>
-   <span data-ttu-id="0a423-135">HARÇ 2 = %20, Satış vergisi yüzdesi yöntemini kullanarak, satış vergisi alanındaki Satış vergisi içinde Harç 1 ile</span><span class="sxs-lookup"><span data-stu-id="0a423-135">DUTY 2 = 20%, using the Percentage of sales tax method, with Duty 1 in the Sales tax on sales tax field</span></span>
-   <span data-ttu-id="0a423-136">SATIŞ VERGİSİ = %25 Brüt tutar yüzdesi yöntemini kullanarak</span><span class="sxs-lookup"><span data-stu-id="0a423-136">SALESTAX = 25%, using the Percentage of gross amount method</span></span>

<span data-ttu-id="0a423-137">Net tutar: 10.00 HARÇ 1: 10.00 x %10 = 1.00 HARÇ 2: 1.00 x %20 = 0.20 Brüt tutar: 10.00 + 1.00 + 0.20 = 11.20 SATIŞ VERGİSİ: 11.20 x %25 = 2.80 Toplam HARÇLAR ve SATIŞ VERGİSİ: 1.00 + 0.20 + 2.80 = 4.00 Toplam tutar: 10.00 + 4.00 = 14.00</span><span class="sxs-lookup"><span data-stu-id="0a423-137">Net amount: 10.00 DUTY 1: 10.00 x 10% = 1.00 DUTY 2: 1.00 x 20% = 0.20 Gross amount: 10.00 + 1.00 + 0.20 = 11.20 SALESTAX: 11.20 x 25% = 2.80 Total DUTIES and SALESTAX: 1.00 + 0.20 + 2.80 = 4.00 Total amount: 10.00 + 4.00 = 14.00</span></span>

| <span data-ttu-id="0a423-138">**Not**</span><span class="sxs-lookup"><span data-stu-id="0a423-138">**Note**</span></span>                                                                                                                                                                                                                    |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0a423-139">Vergi hesaplamalarında çok düzeyli vergi mümkün değildir. </span><span class="sxs-lookup"><span data-stu-id="0a423-139">Multilevel tax on tax calculations are not possible.</span></span> <span data-ttu-id="0a423-140">Bir vergi, başka bir vergiye dayanılarak zaten hesaplanmış bir vergiye dayanılarak hesaplanamaz.</span><span class="sxs-lookup"><span data-stu-id="0a423-140">A tax cannot be calculated based on a tax which already is calculated based on another tax.</span></span> <span data-ttu-id="0a423-141">Bir harekette, vergi kodları üzerinde birden fazla tek düzeyli vergi hesaplanabilir.</span><span class="sxs-lookup"><span data-stu-id="0a423-141">Multiple single level tax on tax codes can be calculated on a transaction.</span></span> |

## <a name="amount-per-unit"></a><span data-ttu-id="0a423-142">Birim başına tutar</span><span class="sxs-lookup"><span data-stu-id="0a423-142">Amount per unit</span></span>
<span data-ttu-id="0a423-143">Kaynak alanında Birim başına tutar seçimini yaptığınızda, satış vergisi belge satırına girilen miktarla çarpılan sabit bir birim başına tutar şeklinde hesaplanır.</span><span class="sxs-lookup"><span data-stu-id="0a423-143">When you select Amount per unit in the Origin field, sales tax is calculated as a fixed amount per unit multiplied with the quantity entered on the document line.</span></span> <span data-ttu-id="0a423-144">Birim alanında bir birim seçilmelidir.</span><span class="sxs-lookup"><span data-stu-id="0a423-144">A unit has to be selected in the Unit field.</span></span> <span data-ttu-id="0a423-145">Birim başına tutar Satış vergisi kod değerleri sayfasında belirtilir.</span><span class="sxs-lookup"><span data-stu-id="0a423-145">The amount per unit is specified in the Sales tax code values page.</span></span>
### <a name="example"></a><span data-ttu-id="0a423-146">Örnek</span><span class="sxs-lookup"><span data-stu-id="0a423-146">Example</span></span>

<span data-ttu-id="0a423-147">Satış vergisi kodu şu şekilde ayarlanır: birim = kutu başına USD 1.20 Bir satış faturası satırında bir maddeden 25 kutu satılmış Satış vergisi 25 x 1.20 = 30.00 olarak hesaplanır</span><span class="sxs-lookup"><span data-stu-id="0a423-147">Sales tax code is set up as: USD 1.20 per unit = box On a sales invoice line 25 boxes of an item are sold Sales tax is calculated as 25 x 1.20 = 30.00</span></span>

| <span data-ttu-id="0a423-148">**Not**</span><span class="sxs-lookup"><span data-stu-id="0a423-148">**Note**</span></span>                                                                                                                                                                                                 |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0a423-149">Hareket satış vergisi kodunda belirtilenden farklı bir birime girilirse, Birim dönüştürme sayfasında ayarlı birim dönüştürmelerine dayanılarak otomatik olarak dönüştürülür.</span><span class="sxs-lookup"><span data-stu-id="0a423-149">If the transaction is entered in different unit than the unit specified on the sales tax code, it is converted automatically based on the unit conversions that are set up in the Unit conversions page.</span></span> |

###  <a name="amount-per-unit-additional-option"></a><span data-ttu-id="0a423-150">Birim başına tutar, ek seçenek</span><span class="sxs-lookup"><span data-stu-id="0a423-150">Amount per unit, additional option</span></span>

<span data-ttu-id="0a423-151">Hesaplama sekmesinde, bir birim başına tutar hesaplanmış verginin diğer vergi kodlarından önce hesaplanıp, Kaynak = Net tutar yüzdesi hesaplanmış diğer vergi kodlarından önce net tutara eklenip eklenmeyeceğini belirleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="0a423-151">On the Calculation tab, you can select whether an amount per unit calculated tax is calculated before other tax codes and added to the net amount before other tax codes with Origin = Percentage of net amount are calculated.</span></span>

### <a name="examples"></a><span data-ttu-id="0a423-152">Örnekler</span><span class="sxs-lookup"><span data-stu-id="0a423-152">Examples</span></span>

<span data-ttu-id="0a423-153">Bir harekette 2 vergi kodu hesapladığımızı düşünelim:</span><span class="sxs-lookup"><span data-stu-id="0a423-153">Assume we calculate 2 tax codes on a transaction:</span></span>

-   <span data-ttu-id="0a423-154">HARÇ: Kaynak = Birim başına tutar ve bir satış vergisi, değer birim başına 5.00 olarak ayarlanır = pcs</span><span class="sxs-lookup"><span data-stu-id="0a423-154">DUTY: Origin = Amount per unit and a sales tax, the value is set to 5.00 per unit = pcs</span></span>
-   <span data-ttu-id="0a423-155">SATIŞ VERGİSİ: Kaynak = aşağıdaki örnekte gösterildiği gibi, değer %25 olarak ayarlanır</span><span class="sxs-lookup"><span data-stu-id="0a423-155">SALESTAX: Origin = as shown in the examples below, the value is set to 25%</span></span>

<span data-ttu-id="0a423-156">Bir maddenin 1 parçasını birim fiyatı 10,00'dan satıyoruz</span><span class="sxs-lookup"><span data-stu-id="0a423-156">We sell 1 piece of an item at a unit price of 10.00</span></span>
#### <a name="example-1"></a><span data-ttu-id="0a423-157">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="0a423-157">Example 1</span></span>

<span data-ttu-id="0a423-158">SATIŞ VERGİSİ: Kaynak = Brüt tutar yüzdesi yöntemi Satış vergisinden önce hesapla seçeneği etkisizdir çünkü SATIŞ VERGİSİ brüt tutarın yüzdesi olarak hesaplanır.</span><span class="sxs-lookup"><span data-stu-id="0a423-158">SALESTAX: Origin = Percentage of gross amount method The Calculate before sales tax option has no effect, because SALESTAX is calculated as a percentage of the gross amount.</span></span> <span data-ttu-id="0a423-159">HAR: 1 x 5,00 = 5,00 Brüt tutar: 10,00 + 5,00 = 15,00 SATIŞ VERGİSİ: 15,00 x %25 = 3,75 Toplam satış vergisi: 5,00 + 3,75 = 8,75 Toplam tutar: 10,00 + 8,75 = 18,75</span><span class="sxs-lookup"><span data-stu-id="0a423-159">DUTY: 1 x 5.00 = 5.00 Gross amount: 10.00 + 5.00 = 15.00 SALESTAX: 15.00 x 25% = 3.75 Total sales tax: 5.00 + 3.75 = 8.75 Total amount: 10.00 + 8.75 = 18.75</span></span>

#### <a name="example-2"></a><span data-ttu-id="0a423-160">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="0a423-160">Example 2</span></span>

<span data-ttu-id="0a423-161">SATIŞ VERGİSİ: Kaynak = Net tutar yüzdesi HARÇ hesaplaması için satış vergisinden önce hesapla seçeneği seçilmez.</span><span class="sxs-lookup"><span data-stu-id="0a423-161">SALESTAX: Origin = Percentage of net amount The Calculate before sales tax option is not selected for the DUTY calculation.</span></span> <span data-ttu-id="0a423-162">Net tutar: 10,00 HARÇ: 1 x 5,00 = 5,00 SATIŞ VERGİSİ: 10,00 x %25 = 2,50 Toplam satış vergisi: 5,00 + 2,50 = 7,50 Toplam tutar: 10,00 + 7,50 = 17,50</span><span class="sxs-lookup"><span data-stu-id="0a423-162">Net amount: 10.00 DUTY: 1 x 5.00 = 5.00 SALESTAX: 10.00 x 25% = 2.50 Total sales tax: 5.00 + 2.50 = 7.50 Total amount: 10.00 + 7.50 = 17.50</span></span>

#### <a name="example-3"></a><span data-ttu-id="0a423-163">Örnek 3</span><span class="sxs-lookup"><span data-stu-id="0a423-163">Example 3</span></span>

<span data-ttu-id="0a423-164">SATIŞ VERGİSİ: Kaynak = Net tutar yüzdesi HARÇ hesaplaması için satış vergisinden önce hesapla seçeneği seçilir.</span><span class="sxs-lookup"><span data-stu-id="0a423-164">SALESTAX: Origin = Percentage of net amount The Calculate before sales tax option is selected for the DUTY calculation.</span></span> <span data-ttu-id="0a423-165">Net tutar: 10,00 HARÇ: 1 x 5,00 = 5,00 SATIŞ VERGİSİ: (10,00 + 5,00) x %25 = 3,75 Toplam satış vergisi: 5,00 + 3,75 = 8,75 Toplam tutar: 10,00 + 8,75 = 18,75</span><span class="sxs-lookup"><span data-stu-id="0a423-165">Net amount: 10.00 DUTY: 1 x 5.00 = 5.00 SALESTAX: (10.00 + 5.00) x 25% = 3.75 Total sales tax: 5.00 + 3.75 = 8.75 Total amount: 10.00 + 8.75 = 18.75</span></span>

#### <a name="example-4"></a><span data-ttu-id="0a423-166">Örnek 4</span><span class="sxs-lookup"><span data-stu-id="0a423-166">Example 4</span></span>

<span data-ttu-id="0a423-167">Yalnızca bir vergi olduğu için, Örnek 3 ile Örnek 1'in sonucu aynıdır.</span><span class="sxs-lookup"><span data-stu-id="0a423-167">The result of Example 3 and Example 1 is the same, because there is only one duty.</span></span> <span data-ttu-id="0a423-168">İki HARCINIZ olduğunu ve bunlardan yalnızca birinin satış vergisi hesaplaması için net tutara dahil olduğunu varsayın: HARÇ 1: 5,00, Birim başına tutar yöntemi kullanılarak ve Satış vergisinden önce hesapla seçeneği seçilidir HARÇ 2: 2,50, Birim başına tutar yöntemi kullanılarak ve Satış vergisinden önce hesapla seçeneği seçili değildir Satış vergisi: %25, Net tutar yüzdesi yöntemi kullanılarak Net tutar: 10,00 HARÇ 1: 1 x 5,00 = 5,00 HARÇ 2: 1 x 2,50 = 2,50 Satıl vergisine tabi net tutar: 10,00 + 5,00 = 15,00 SATIŞ VERGİSİ: 15,00 x %25 = 3,75 Toplam satış vergileri, harçlar dahil: 5,00 + 2,50 + 3,75 = 11,25 Toplam tutar: 10,00 + 11,25 = 21,25 %25 SATIŞ VERGİSİ net tutarın toplamı için hesaplanır (10,00) + HARÇ 1 (5,00) = 15,00.</span><span class="sxs-lookup"><span data-stu-id="0a423-168">Assume that you have two DUTIES, and only one of them is included in the net amount for the sales tax calculation: DUTY 1: 5.00, using the Amount per unit method, and the Calculate before sales tax option is selected DUTY 2: 2.50, using the Amount per unit method, and the Calculate before sales tax option is not selected Sales tax: 25%, using the Percentage of net amount method Net amount: 10.00 DUTY 1: 1 x 5.00 = 5.00 DUTY 2: 1 x 2.50 = 2.50 Net amount subject to sales tax: 10.00 + 5.00 = 15.00 SALESTAX: 15.00 x 25% = 3.75 Total sales taxes, including duties: 5.00 + 2.50 + 3.75 = 11.25 Total amount: 10.00 + 11.25 = 21.25 The 25% SALESTAX is calculated for the sum of the net amount (10.00) + DUTY 1 (5.00) = 15.00.</span></span> <span data-ttu-id="0a423-169">HARÇ 2, satış vergisi hesaplandıktan sonra vergi tutarına eklenir.</span><span class="sxs-lookup"><span data-stu-id="0a423-169">DUTY 2 is added to the tax amount after the sales tax is calculated.</span></span>

## <a name="calculated-percentage-of-net-amount"></a><span data-ttu-id="0a423-170">Net tutar için hesaplanan yüzde</span><span class="sxs-lookup"><span data-stu-id="0a423-170">Calculated percentage of net amount</span></span>
<span data-ttu-id="0a423-171">Net tutarın hesaplanan yüzdesi, vergi hesaplamalarını belge veya günlük için satış vergisi parametresi içeren Tutarların ayarına bağlı olarak farklı şekilde ele alır.</span><span class="sxs-lookup"><span data-stu-id="0a423-171">The Calculated percentage of net amount handles tax calculation differently depending on the setting of the Amounts include sales tax parameter for the document or journal.</span></span>
### <a name="example-1"></a><span data-ttu-id="0a423-172">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="0a423-172">Example 1</span></span>

<span data-ttu-id="0a423-173">Belge / günlük Satış vergisi içeren tutarlar = Evet olarak ayarlanır Hareket satırı tutarı: 10,00 Vergi oranı: %25 Satış vergisi: Hareket satırı tutarı x vergi oranı (10,00 x %25) = 2,50 Vergi taban tutarı (kaynak tutar): Hareket satırı tutarı - Satış vergisi (10,00 - 2,50) = 7,50</span><span class="sxs-lookup"><span data-stu-id="0a423-173">Document / journal is set to Amounts include sales tax = Yes Transaction line amount: 10.00 Tax rate: 25% Sales tax: Transaction line amount x tax rate (10.00 x 25%) = 2.50 Tax base amount (origin amount): Transaction line amount - Sales tax (10.00 - 2.50) = 7.50</span></span>

### <a name="example-2"></a><span data-ttu-id="0a423-174">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="0a423-174">Example 2</span></span>

<span data-ttu-id="0a423-175">Belge / günlük Satış vergisi içeren tutarlar = Hayır olarak ayarlanır Hareket satırı tutarı: 10,00 Vergi oranı: %25 Satış vergisi: (Hareket satırı tutarı x vergi oranı) / (100 - vergi oranı) (10,00 x %25) / (%100 - %25) = 3,33 Vergi taban tutarı (kaynak tutar): Hareket satırı tutarı = 10,00</span><span class="sxs-lookup"><span data-stu-id="0a423-175">Document / journal is set to Amounts include sales tax = No Transaction line amount: 10.00 Tax rate: 25% Sales tax: (Transaction line amount x tax rate) / (100 - tax rate) (10.00 x 25%) / (100% - 25%) = 3.33 Tax base amount (origin amount): Transaction line amount = 10.00</span></span>



<a name="additional-resources"></a><span data-ttu-id="0a423-176">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="0a423-176">Additional resources</span></span>
--------

[<span data-ttu-id="0a423-177">Marjinal taban ve hesaplama yöntemi alanları temel alınarak satış vergisi oranlarını belirleme</span><span class="sxs-lookup"><span data-stu-id="0a423-177">Determining sale tax rates based on the Marginal base and Calculation method fields</span></span>](marginal-base-field.md)

[<span data-ttu-id="0a423-178">Satış vergisi kodları için tüm tutar ve Aralık hesaplaması seçenekleri</span><span class="sxs-lookup"><span data-stu-id="0a423-178">Whole amount and Interval calculation options for sales tax codes</span></span>](whole-amount-interval-options-sales-tax-codes.md)



