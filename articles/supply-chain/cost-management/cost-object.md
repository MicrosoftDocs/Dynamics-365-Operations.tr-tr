---
title: Maliyet nesneleri
description: "Bu makalede, maliyet nesneleri hakkında bilgiler verilmekte, maliyetlerin ve miktarların nasıl biriktirildiği açıklanmaktadır. Maliyet nesnesi, maliyetlerin ve miktarların toplandığı bir varlıktır. Maliyet nesnesi varlığı, bir ürün veya ürün çeşidi (stil, renk vb.) olabilir."
author: YuyuScheller
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: InventCostOnhandItem
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 19451
ms.assetid: ec776b98-813a-490d-848f-468452d98fac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 08c38aada355583c5a6872f75b57db95d9b81786
ms.openlocfilehash: d43ea6c0d80a1602f298bbbedb88dd8f7decca4e
ms.contentlocale: tr-tr
ms.lasthandoff: 07/18/2017

---

# <a name="cost-objects"></a><span data-ttu-id="0e556-105">Maliyet nesneleri</span><span class="sxs-lookup"><span data-stu-id="0e556-105">Cost objects</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="0e556-106">Bu makalede, maliyet nesneleri hakkında bilgiler verilmekte, maliyetlerin ve miktarların nasıl biriktirildiği açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="0e556-106">This article provides information about costs objects, and explains how costs and quantities are accumulated.</span></span> <span data-ttu-id="0e556-107">Maliyet nesnesi, maliyetlerin ve miktarların toplandığı bir varlıktır.</span><span class="sxs-lookup"><span data-stu-id="0e556-107">A cost object is an entity that costs and quantities are accumulated for.</span></span> <span data-ttu-id="0e556-108">Maliyet nesnesi varlığı, bir ürün veya ürün çeşidi (stil, renk vb.) olabilir.</span><span class="sxs-lookup"><span data-stu-id="0e556-108">A cost object entity can be either a product or product variants, such as variants for style and color.</span></span>  

<a name="cost-objects"></a><span data-ttu-id="0e556-109">Maliyet nesneleri</span><span class="sxs-lookup"><span data-stu-id="0e556-109">Cost objects</span></span>
------------

<span data-ttu-id="0e556-110">**Maliyet nesneleri** sayfasında, bir ürüne kayıtlı tüm maliyet nesneleri listelenir.</span><span class="sxs-lookup"><span data-stu-id="0e556-110">The **Cost objects** page lists all cost objects that are registered on a product.</span></span> <span data-ttu-id="0e556-111">Maliyet nesneleri aşağıdaki kaynaklardan gelen verilerle tanımlanır:</span><span class="sxs-lookup"><span data-stu-id="0e556-111">The cost objects are defined by data from the following sources:</span></span>

-   <span data-ttu-id="0e556-112">Ürün</span><span class="sxs-lookup"><span data-stu-id="0e556-112">Product</span></span>
-   <span data-ttu-id="0e556-113">Ürün boyut grubu</span><span class="sxs-lookup"><span data-stu-id="0e556-113">Product dimension group</span></span>
-   <span data-ttu-id="0e556-114">Depolama boyutu grubu</span><span class="sxs-lookup"><span data-stu-id="0e556-114">Storage dimension group</span></span>
-   <span data-ttu-id="0e556-115">İzleme boyut grubu</span><span class="sxs-lookup"><span data-stu-id="0e556-115">Tracking dimension group</span></span>

<span data-ttu-id="0e556-116">**Not:** Maliyet nesnesi, yalnızca **Doğrudan malzeme** türündeki bir maliyet öğesini temsil eder.</span><span class="sxs-lookup"><span data-stu-id="0e556-116">**Note:** A cost object represents a cost element of the **Direct material** type only.</span></span> <span data-ttu-id="0e556-117">Maliyet nesnesi ve stok nesnesi arasındaki fark, maliyet nesnesinin mali stok için seçilen stok boyutlarıyla tanımlanmasıdır.</span><span class="sxs-lookup"><span data-stu-id="0e556-117">A cost object and an inventory object differ in the way that a cost object is defined by the inventory dimensions that are selected for financial inventory.</span></span> <span data-ttu-id="0e556-118">Diyelim ki bir madde aşağıdaki şekilde yapılandırılmış:</span><span class="sxs-lookup"><span data-stu-id="0e556-118">For example, an item has the following configuration:</span></span>

-   <span data-ttu-id="0e556-119">**Tesis:** Fiziksel stok = Evet, Mali stok = Evet</span><span class="sxs-lookup"><span data-stu-id="0e556-119">**Site:** Physical inventory = Yes, Financial inventory = Yes</span></span>
-   <span data-ttu-id="0e556-120">**Ambar:** Fiziksel stok = Evet, Mali stok = Hayır</span><span class="sxs-lookup"><span data-stu-id="0e556-120">**Warehouse:** Physical inventory = Yes, Financial inventory = No</span></span>
-   <span data-ttu-id="0e556-121">**Toplu İş No:** Fiziksel stok = Evet, Mali stok = Hayır</span><span class="sxs-lookup"><span data-stu-id="0e556-121">**Batch No.:** Physical inventory = Yes, Financial inventory = No</span></span>

<span data-ttu-id="0e556-122">Aşağıdaki tabloda maliyet nesnesinin ve stok nesnesinin ne oldukları gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="0e556-122">The following table shows what is a cost object and what is an inventory object.</span></span>

| <span data-ttu-id="0e556-123">Nesne türü</span><span class="sxs-lookup"><span data-stu-id="0e556-123">Object type</span></span>      | <span data-ttu-id="0e556-124">Madde kodu</span><span class="sxs-lookup"><span data-stu-id="0e556-124">Item number</span></span> | <span data-ttu-id="0e556-125">Tesis</span><span class="sxs-lookup"><span data-stu-id="0e556-125">Site</span></span> | <span data-ttu-id="0e556-126">Ambar</span><span class="sxs-lookup"><span data-stu-id="0e556-126">Warehouse</span></span> | <span data-ttu-id="0e556-127">Bordro Numarası</span><span class="sxs-lookup"><span data-stu-id="0e556-127">Batch No.</span></span> |
|------------------|-------------|------|-----------|-----------|
| <span data-ttu-id="0e556-128">Maliyet nesnesi</span><span class="sxs-lookup"><span data-stu-id="0e556-128">Cost object</span></span>      | <span data-ttu-id="0e556-129">x</span><span class="sxs-lookup"><span data-stu-id="0e556-129">x</span></span>           | <span data-ttu-id="0e556-130">x</span><span class="sxs-lookup"><span data-stu-id="0e556-130">x</span></span>    |           |           |
| <span data-ttu-id="0e556-131">Stok nesnesi</span><span class="sxs-lookup"><span data-stu-id="0e556-131">Inventory object</span></span> | <span data-ttu-id="0e556-132">x</span><span class="sxs-lookup"><span data-stu-id="0e556-132">x</span></span>           | <span data-ttu-id="0e556-133">x</span><span class="sxs-lookup"><span data-stu-id="0e556-133">x</span></span>    |  <span data-ttu-id="0e556-134">x</span><span class="sxs-lookup"><span data-stu-id="0e556-134">x</span></span>        | <span data-ttu-id="0e556-135">x</span><span class="sxs-lookup"><span data-stu-id="0e556-135">x</span></span>         |

## <a name="accumulation-of-costs-and-quantities"></a><span data-ttu-id="0e556-136">Maliyetlerin ve miktarların toplamı</span><span class="sxs-lookup"><span data-stu-id="0e556-136">Accumulation of costs and quantities</span></span>
-   <span data-ttu-id="0e556-137">**Değer** alanındaki değer, aşağıdaki değerlerin toplamıdır:</span><span class="sxs-lookup"><span data-stu-id="0e556-137">The value in the **Value** fieldis a sum of the following values:</span></span>
    -   <span data-ttu-id="0e556-138">Fiziksel maliyet tutarı</span><span class="sxs-lookup"><span data-stu-id="0e556-138">Physical cost amount</span></span>
    -   <span data-ttu-id="0e556-139">Mali maliyet tutarı</span><span class="sxs-lookup"><span data-stu-id="0e556-139">Financial cost amount</span></span>
    -   <span data-ttu-id="0e556-140">Ayarlamalar</span><span class="sxs-lookup"><span data-stu-id="0e556-140">Adjustments</span></span>
-   <span data-ttu-id="0e556-141">**Miktar** alanındaki değer, aşağıdaki değerlerin toplamıdır:</span><span class="sxs-lookup"><span data-stu-id="0e556-141">The value in the **Quantity** field is a sum of the following values:</span></span>
    -   <span data-ttu-id="0e556-142">Alınan</span><span class="sxs-lookup"><span data-stu-id="0e556-142">Received</span></span>
    -   <span data-ttu-id="0e556-143">Düşülen</span><span class="sxs-lookup"><span data-stu-id="0e556-143">Deducted</span></span>
    -   <span data-ttu-id="0e556-144">Deftere nakledilen miktar</span><span class="sxs-lookup"><span data-stu-id="0e556-144">Posted quantity</span></span>
-   <span data-ttu-id="0e556-145">**Ortalama birim maliyeti** alanı, hesaplanan bir alandır.</span><span class="sxs-lookup"><span data-stu-id="0e556-145">The **Average unit cost** field is a calculated field.</span></span> <span data-ttu-id="0e556-146">Değer, **Değer** değerinin **Miktar** değerine bölünmesiyle bulunur.</span><span class="sxs-lookup"><span data-stu-id="0e556-146">The value is calculated by dividing the **Value** value by the **Quantity** value.</span></span>

<span data-ttu-id="0e556-147">**Not:** **Fiziksel değeri dahil ** et parametresinin, önceki hesaplamalar üzerinde etkisi yoktur.</span><span class="sxs-lookup"><span data-stu-id="0e556-147">**Note:** The **Include physical value **parameter has no effect on the preceding calculations.</span></span>

<a name="see-also"></a><span data-ttu-id="0e556-148">Ayrıca bkz.</span><span class="sxs-lookup"><span data-stu-id="0e556-148">See also</span></span>
--------

[<span data-ttu-id="0e556-149">Ürün boyut grubu</span><span class="sxs-lookup"><span data-stu-id="0e556-149">Product dimension group</span></span>](https://technet.microsoft.com/en-us/library/aa499382.aspx)

[<span data-ttu-id="0e556-150">Depolama boyutu grubu</span><span class="sxs-lookup"><span data-stu-id="0e556-150">Storage dimension group</span></span>](https://technet.microsoft.com/en-us/library/hh209317.aspx)

[<span data-ttu-id="0e556-151">İzleme boyutu grubu</span><span class="sxs-lookup"><span data-stu-id="0e556-151">Tracking dimension group</span></span>](https://technet.microsoft.com/en-us/library/hh209465.aspx)

[<span data-ttu-id="0e556-152">Yenilikler veya değişenler</span><span class="sxs-lookup"><span data-stu-id="0e556-152">What's new or changed</span></span>](/dynamics365/unified-operations/dev-itpro/get-started/whats-new-changed)

[<span data-ttu-id="0e556-153">Maliyet girişleri</span><span class="sxs-lookup"><span data-stu-id="0e556-153">Cost entries</span></span>](cost-entries.md)




