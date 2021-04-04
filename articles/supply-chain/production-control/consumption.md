---
title: Malzeme tüketimini hesapla
description: Bu makalede, malzeme tüketiminin hesaplanmasına ilişkin çeşitli seçenekler hakkında bilgiler sağlanmaktadır.
author: johanhoffmann
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BOMDesignerEditBOM, BOMTable, ProdBOM
audience: Application User
ms.reviewer: kamaybac
ms.custom: 53401
ms.assetid: 9cff88e4-0425-4707-9178-3c2cb10df7c2
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: fc39df69a22b90a805aa9967d52dafea27c78c2b
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5246345"
---
# <a name="calculate-material-consumption"></a><span data-ttu-id="3f082-103">Malzeme tüketimini hesapla</span><span class="sxs-lookup"><span data-stu-id="3f082-103">Calculate material consumption</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="3f082-104">Bu makalede, malzeme tüketiminin hesaplanmasına ilişkin çeşitli seçenekler hakkında bilgiler sağlanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="3f082-104">This article provides information about various options that are related to the calculation of material consumption.</span></span> 

<span data-ttu-id="3f082-105">Malzeme tüketiminin hesaplanmasına ilişkin aşağıdaki seçenekler **Ürün reçetesi** sayfasının **Satır ayrıntıları** hızlı sekmesinde bulunan **Ayar** ve **Adım tüketimi** sekmelerinde bulunur.</span><span class="sxs-lookup"><span data-stu-id="3f082-105">The following options that are related to the calculation of material consumption are available on the **Setup** and **Step consumption** tabs on the **Line details** FastTab of the **Bill of materials** page.</span></span>

## <a name="variable-and-constant-consumption"></a><span data-ttu-id="3f082-106">Değişken ve sabit tüketim</span><span class="sxs-lookup"><span data-stu-id="3f082-106">Variable and constant consumption</span></span>
<span data-ttu-id="3f082-107">**Tüketim** alanında, tüketimin bir sabit miktar mı yoksa değişken miktar olarak mı hesaplanacağını seçebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="3f082-107">In the **Consumption is** field, you can select whether consumption should be calculated as a constant quantity or a variable quantity.</span></span> <span data-ttu-id="3f082-108">Üretim için sabit miktar veya hacim gerekiyorsa **Sabit**'i seçin, üretilen miktardan bağımsız olarak.</span><span class="sxs-lookup"><span data-stu-id="3f082-108">Select **Constant** if a fixed quantity or volume is required for the production, regardless of the quantity that is produced.</span></span> <span data-ttu-id="3f082-109">Varsayılan ayar olan **Değişken** seçeneğini, mamul ürünler için gereken malzeme tutarı üretilen mamul ürün sayısına orantılı olduğunda seçin.</span><span class="sxs-lookup"><span data-stu-id="3f082-109">Select **Variable**, which is the default setting, if the required amount of material in the finished goods is proportional to the number of finished goods that are produced.</span></span>

## <a name="calculating-consumption-from-a-formula"></a><span data-ttu-id="3f082-110">Tüketimi bir formülden hesaplama</span><span class="sxs-lookup"><span data-stu-id="3f082-110">Calculating consumption from a formula</span></span>
<span data-ttu-id="3f082-111">**Formül** alanında, malzeme tüketimini hesaplamak için çeşitli formüller ayarlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="3f082-111">In the **Formula** field, you can set up various formulas for calculating material consumption.</span></span> <span data-ttu-id="3f082-112">Varsayılan değeri olan **Standart**'ı kullanırsanız, tüketim bir formülle hesaplanmaz.</span><span class="sxs-lookup"><span data-stu-id="3f082-112">If you use the default value, **Standard**, the consumption isn't calculated from a formula.</span></span> <span data-ttu-id="3f082-113">Aşağıdaki formüller **Yükseklik**, **Genişlik**, **Derinlik**, **Yoğunluk** ve **Sabit** alanlarıyla birlikte çalışır:</span><span class="sxs-lookup"><span data-stu-id="3f082-113">The following formulas work together with the **Height**, **Width**, **Depth**, **Density**, and **Constant** fields:</span></span>

-   <span data-ttu-id="3f082-114">Yükseklik \* Sabit</span><span class="sxs-lookup"><span data-stu-id="3f082-114">Height \* Constant</span></span>
-   <span data-ttu-id="3f082-115">Yükseklik \* Genişlik \* Sabit</span><span class="sxs-lookup"><span data-stu-id="3f082-115">Height \* Width \* Constant</span></span>
-   <span data-ttu-id="3f082-116">Yükseklik \* Genişlik \* Derinlik \* Sabit</span><span class="sxs-lookup"><span data-stu-id="3f082-116">Height \* Width \* Depth \* Constant</span></span>
-   <span data-ttu-id="3f082-117">(Yükseklik \* Genişlik \* Derinlik / Yoğunluk) \* Sabit</span><span class="sxs-lookup"><span data-stu-id="3f082-117">(Height \* Width \* Depth / Density) \* Constant</span></span>

## <a name="rounding-up-and-multiples"></a><span data-ttu-id="3f082-118">Yuvarlama ve katları</span><span class="sxs-lookup"><span data-stu-id="3f082-118">Rounding up and multiples</span></span>
<span data-ttu-id="3f082-119">**Yuvarlama** ve **Katları** alanları birlikte kullanıldığında, malzeme tüketim değerini yuvarlamanıza olanak tanır.</span><span class="sxs-lookup"><span data-stu-id="3f082-119">Together, the **Rounding up** and **Multiples** fields let you round up the material consumption value.</span></span> <span data-ttu-id="3f082-120">Örneğin, değeri hammaddenin üretim için çekildiği işleme birimine göre yuvarlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="3f082-120">For example, you can round up the value according to the handling unit in which the raw material is picked for production.</span></span> <span data-ttu-id="3f082-121">**Yuvarlama** alanında şu seçenekler kullanılabilir: **Miktar**, **Ölçüm** ve **Tüketim**.</span><span class="sxs-lookup"><span data-stu-id="3f082-121">The following options are available in the **Rounding up** field: **Quantity**, **Measurement**, and **Consumption**.</span></span>

### <a name="quantity"></a><span data-ttu-id="3f082-122">Miktar</span><span class="sxs-lookup"><span data-stu-id="3f082-122">Quantity</span></span>

<span data-ttu-id="3f082-123">Yuvarlama mekanizması olarak **Miktar** seçerseniz, miktarın belirtilen miktarın katı olması gerekir.</span><span class="sxs-lookup"><span data-stu-id="3f082-123">If you select **Quantity** as the rounding-up mechanism, the quantity must be a multiple of the specified quantity.</span></span> <span data-ttu-id="3f082-124">Örneğin, tam sayılar gerekiyorsa **Katları** alanına **1** yazın.</span><span class="sxs-lookup"><span data-stu-id="3f082-124">For example, if whole numbers are required, select **1** in the **Multiples** field.</span></span> <span data-ttu-id="3f082-125">Ardından sayılar 1'e bölünebilen bir miktara yuvarlanır.</span><span class="sxs-lookup"><span data-stu-id="3f082-125">Numbers are then rounded up to a quantity that is divisible by 1.</span></span>

### <a name="measurement"></a><span data-ttu-id="3f082-126">Ölçüm</span><span class="sxs-lookup"><span data-stu-id="3f082-126">Measurement</span></span>

<span data-ttu-id="3f082-127">Genellikle, hammaddenin belirli boyutlarda gelmesi durumunda yuvarlama mekanizması olarak **Ölçüm** seçilir.</span><span class="sxs-lookup"><span data-stu-id="3f082-127">Typically, you select **Measurement** as the rounding-up mechanism when the raw material comes in specific dimensions.</span></span> <span data-ttu-id="3f082-128">Örneğin, bir mamul ürün için 2 metre uzunluğunda metal boru parçası gereklidir ve metal boru 4,5 metre uzunluğunda depolanmıştır.</span><span class="sxs-lookup"><span data-stu-id="3f082-128">For example, a piece of 2-meter metal tube is required for a finished good, and the metal tube is stored in 4.5-meter lengths.</span></span> <span data-ttu-id="3f082-129">Bu durumda, mamul üründen belirli sayıda üretmek için ne kadar metal boru gerektiğini hesaplamak için **Ölçüm** yuvarlama mekanizması kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="3f082-129">In this case, the **Measurement** rounding-up mechanism can be used to calculate how many metal tubes are required to produce a specific number of pieces of the finished good.</span></span> <span data-ttu-id="3f082-130">Bu örnek için **Formül** alanı **Yükseklik \* Sabit** olarak ayarlanır.</span><span class="sxs-lookup"><span data-stu-id="3f082-130">For this example, the **Formula** field is set to **Height \* Constant**.</span></span> <span data-ttu-id="3f082-131">**Yükseklik** alanı, tamamlanmış mal için gerekli olan borunun boru uzunluğunu belirtmek için **2** olarak ayarlanmıştır.</span><span class="sxs-lookup"><span data-stu-id="3f082-131">The **Height** field is set to **2** to indicate the length of the tube that is required for the finished good.</span></span> <span data-ttu-id="3f082-132">Borunun 4,5 metre uzunluğunda alındığını belirtmek için **Katı** alanı **4,5** olarak ayarlanır.</span><span class="sxs-lookup"><span data-stu-id="3f082-132">The **Multiple** field is set to **4.5** to indicate that the tube is picked in lengths of 4.5 meters.</span></span> <span data-ttu-id="3f082-133">Hesaplama aşağıdaki gibidir:</span><span class="sxs-lookup"><span data-stu-id="3f082-133">Here is the calculation:</span></span>

1.  <span data-ttu-id="3f082-134">10 adet mamul için gereken katları sayısı: 10 ÷ 2 = 5 parça</span><span class="sxs-lookup"><span data-stu-id="3f082-134">Number of multiples that are required for 10 pieces of the finished good: 10 ÷ 2 = 5 pieces</span></span>
2.  <span data-ttu-id="3f082-135">Toplam tüketim: 4,5 × 5 = 22,5 metre metal boru</span><span class="sxs-lookup"><span data-stu-id="3f082-135">Total consumption:  4.5 × 5 = 22.5 meters of metal tube</span></span>

<span data-ttu-id="3f082-136">Tüketilen her beş adet boru için 0,5 metre borunun hurdaya çıktığı varsayılır.</span><span class="sxs-lookup"><span data-stu-id="3f082-136">It's assumed that 0.5 meter of tube is scrapped for every five pieces of tube that are consumed.</span></span>

### <a name="consumption"></a><span data-ttu-id="3f082-137">Tüketim</span><span class="sxs-lookup"><span data-stu-id="3f082-137">Consumption</span></span>

<span data-ttu-id="3f082-138">Genellikle, hammaddenin üretimin belirli bir işleme birimi için toptan miktarlarda çekilmesi gerekiyorsa yuvarlama mekanizması olarak **Tüketim** seçilir.</span><span class="sxs-lookup"><span data-stu-id="3f082-138">Typically, you select **Consumption** as the rounding-up mechanism when raw material must be picked in whole quantities of a specific handling unit of the product.</span></span> <span data-ttu-id="3f082-139">Örneğin, bir mamul ürünü üretmek için 2 litre boya gerekmektedir ve boya 25 litrelik kutularda alınmıştır.</span><span class="sxs-lookup"><span data-stu-id="3f082-139">For example, 2 quarts of paint are used to produce one piece of a finished good, and the paint is picked in 25-quart cans.</span></span> <span data-ttu-id="3f082-140">Bu durumda, tüketimi 25 litrelik kutuların tam sayılarına yuvarlamak için **Tüketim** yuvarlama mekanizması kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="3f082-140">In this case, the **Consumption** rounding-up mechanism can be used to round up consumption to whole numbers of 25-quart cans.</span></span> <span data-ttu-id="3f082-141">180 adet mamul ürün üretilecekse gerekli boya miktarı aşağıdaki şekilde hesaplanır:</span><span class="sxs-lookup"><span data-stu-id="3f082-141">Here is the calculation for the amount of paint that is required if 180 pieces of the finished good must be produced:</span></span>

1.  <span data-ttu-id="3f082-142">Hurdaya ayrılan hariç gereken boya miktarı: 180 × 2 = 360 litre</span><span class="sxs-lookup"><span data-stu-id="3f082-142">Paint that is required, excluding scrap: 180 × 2 = 360 quarts</span></span>
2.  <span data-ttu-id="3f082-143">Kutu sayısı: 360 ÷ 25 = 14.4; 15'e yuvarlanır</span><span class="sxs-lookup"><span data-stu-id="3f082-143">Number of cans: 360 ÷ 25 = 14.4, which is rounded up to 15</span></span>
3.  <span data-ttu-id="3f082-144">Hurdaya gidecek miktar dahil gereken boya: 15 × 25 = 375 litre</span><span class="sxs-lookup"><span data-stu-id="3f082-144">Paint that is required, including scrap: 15 × 25 = 375 quarts</span></span>

## <a name="step-consumption"></a><span data-ttu-id="3f082-145">Adım tüketimi</span><span class="sxs-lookup"><span data-stu-id="3f082-145">Step consumption</span></span>
<span data-ttu-id="3f082-146">Adım tüketimi, miktar aralıklarındaki sabit tüketimi hesaplamak için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="3f082-146">Step consumption is used to calculate constant consumption in quantity intervals.</span></span> <span data-ttu-id="3f082-147">**Kurulum** sekmesinde **Formül** alanında **Adım tüketimi** seçerseniz, **Adım tüketimi** sekmesindeki adımlar hakkında bilgi girebilirsiniz. Sabit tüketilen miktar, üretilen miktarın aralıkları olarak ayarlanabilir.</span><span class="sxs-lookup"><span data-stu-id="3f082-147">If you select **Step consumption** in the **Formula** field on the **Setup** tab, you can add information about the steps on the **Step consumption** tab. The fixed consumed quantity can be set up in intervals of the produced quantity.</span></span> <span data-ttu-id="3f082-148">Örneğin, adım tüketimi aşağıdaki tabloda gösterildiği şekilde ayarlanır.</span><span class="sxs-lookup"><span data-stu-id="3f082-148">For example, step consumption is set up as shown in the following table.</span></span>

| <span data-ttu-id="3f082-149">Başlangıç serisi</span><span class="sxs-lookup"><span data-stu-id="3f082-149">From series</span></span> | <span data-ttu-id="3f082-150">Miktar</span><span class="sxs-lookup"><span data-stu-id="3f082-150">Quantity</span></span> |
|-------------|----------|
| <span data-ttu-id="3f082-151">0,00</span><span class="sxs-lookup"><span data-stu-id="3f082-151">0.00</span></span>        | <span data-ttu-id="3f082-152">10,0000</span><span class="sxs-lookup"><span data-stu-id="3f082-152">10.0000</span></span>  |
| <span data-ttu-id="3f082-153">100,00</span><span class="sxs-lookup"><span data-stu-id="3f082-153">100.00</span></span>      | <span data-ttu-id="3f082-154">20,0000</span><span class="sxs-lookup"><span data-stu-id="3f082-154">20.0000</span></span>  |
| <span data-ttu-id="3f082-155">200,00</span><span class="sxs-lookup"><span data-stu-id="3f082-155">200.00</span></span>      | <span data-ttu-id="3f082-156">40,0000</span><span class="sxs-lookup"><span data-stu-id="3f082-156">40.0000</span></span>  |

<span data-ttu-id="3f082-157">Ürün reçetesi (BOM) miktarı 1 ve üretim miktarı 110'dur.</span><span class="sxs-lookup"><span data-stu-id="3f082-157">The bill of materials (BOM) quantity is 1, and the production quantity is 110.</span></span> <span data-ttu-id="3f082-158">Tüketim formülü Başlangıç serisi (Miktar) = Tüketim'dir.</span><span class="sxs-lookup"><span data-stu-id="3f082-158">The formula for the consumption is From series (Quantity) = Consumption.</span></span> <span data-ttu-id="3f082-159">Ürün miktarı 110 olduğundan, "100 seriden başlayarak" ayarına düşer.</span><span class="sxs-lookup"><span data-stu-id="3f082-159">Because the production quantity is 110, it falls into the "From 100 series."</span></span> <span data-ttu-id="3f082-160">Bu nedenle miktar 20'dir.</span><span class="sxs-lookup"><span data-stu-id="3f082-160">Therefore, the quantity is 20.</span></span>





[!INCLUDE[footer-include](../../includes/footer-banner.md)]