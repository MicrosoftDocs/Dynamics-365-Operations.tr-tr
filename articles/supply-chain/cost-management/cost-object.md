---
title: Maliyet nesneleri
description: Bu makalede, maliyet nesneleri hakkında bilgiler verilmekte, maliyetlerin ve miktarların nasıl biriktirildiği açıklanmaktadır. Maliyet nesnesi, maliyetlerin ve miktarların toplandığı bir varlıktır. Maliyet nesnesi varlığı, bir ürün veya ürün çeşidi (stil, renk vb.) olabilir.
author: AndersGirke
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventCostOnhandItem
audience: Application User
ms.reviewer: kamaybac
ms.custom: 19451
ms.assetid: ec776b98-813a-490d-848f-468452d98fac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8ee7c170d5a330c0080931a67c1548eb0d3522bb
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5232410"
---
# <a name="cost-objects"></a><span data-ttu-id="1262b-105">Maliyet nesneleri</span><span class="sxs-lookup"><span data-stu-id="1262b-105">Cost objects</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="1262b-106">Bu makalede, maliyet nesneleri hakkında bilgiler verilmekte, maliyetlerin ve miktarların nasıl biriktirildiği açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="1262b-106">This article provides information about costs objects, and explains how costs and quantities are accumulated.</span></span> <span data-ttu-id="1262b-107">Maliyet nesnesi, maliyetlerin ve miktarların toplandığı bir varlıktır.</span><span class="sxs-lookup"><span data-stu-id="1262b-107">A cost object is an entity that costs and quantities are accumulated for.</span></span> <span data-ttu-id="1262b-108">Maliyet nesnesi varlığı, bir ürün veya ürün çeşidi (stil, renk vb.) olabilir.</span><span class="sxs-lookup"><span data-stu-id="1262b-108">A cost object entity can be either a product or product variants, such as variants for style and color.</span></span>  

## <a name="cost-objects"></a><span data-ttu-id="1262b-109">Maliyet nesneleri</span><span class="sxs-lookup"><span data-stu-id="1262b-109">Cost objects</span></span>

<span data-ttu-id="1262b-110">**Maliyet nesneleri** sayfasında, bir ürüne kayıtlı tüm maliyet nesneleri listelenir.</span><span class="sxs-lookup"><span data-stu-id="1262b-110">The **Cost objects** page lists all cost objects that are registered on a product.</span></span> <span data-ttu-id="1262b-111">Maliyet nesneleri aşağıdaki kaynaklardan gelen verilerle tanımlanır:</span><span class="sxs-lookup"><span data-stu-id="1262b-111">The cost objects are defined by data from the following sources:</span></span>

-   <span data-ttu-id="1262b-112">Ürün</span><span class="sxs-lookup"><span data-stu-id="1262b-112">Product</span></span>
-   <span data-ttu-id="1262b-113">Ürün boyut grubu</span><span class="sxs-lookup"><span data-stu-id="1262b-113">Product dimension group</span></span>
-   <span data-ttu-id="1262b-114">Depolama boyutu grubu</span><span class="sxs-lookup"><span data-stu-id="1262b-114">Storage dimension group</span></span>
-   <span data-ttu-id="1262b-115">İzleme boyut grubu</span><span class="sxs-lookup"><span data-stu-id="1262b-115">Tracking dimension group</span></span>

<span data-ttu-id="1262b-116">**Not:** Maliyet nesnesi, yalnızca **Doğrudan malzeme** türündeki bir maliyet öğesini temsil eder.</span><span class="sxs-lookup"><span data-stu-id="1262b-116">**Note:** A cost object represents a cost element of the **Direct material** type only.</span></span> <span data-ttu-id="1262b-117">Maliyet nesnesi ve stok nesnesi arasındaki fark, maliyet nesnesinin mali stok için seçilen stok boyutlarıyla tanımlanmasıdır.</span><span class="sxs-lookup"><span data-stu-id="1262b-117">A cost object and an inventory object differ in the way that a cost object is defined by the inventory dimensions that are selected for financial inventory.</span></span> <span data-ttu-id="1262b-118">Diyelim ki bir madde aşağıdaki şekilde yapılandırılmış:</span><span class="sxs-lookup"><span data-stu-id="1262b-118">For example, an item has the following configuration:</span></span>

-   <span data-ttu-id="1262b-119">**Tesis:** Fiziksel stok = Evet, Mali stok = Evet</span><span class="sxs-lookup"><span data-stu-id="1262b-119">**Site:** Physical inventory = Yes, Financial inventory = Yes</span></span>
-   <span data-ttu-id="1262b-120">**Ambar:** Fiziksel stok = Evet, Mali stok = Hayır</span><span class="sxs-lookup"><span data-stu-id="1262b-120">**Warehouse:** Physical inventory = Yes, Financial inventory = No</span></span>
-   <span data-ttu-id="1262b-121">**Toplu İş No:** Fiziksel stok = Evet, Mali stok = Hayır</span><span class="sxs-lookup"><span data-stu-id="1262b-121">**Batch No.:** Physical inventory = Yes, Financial inventory = No</span></span>

<span data-ttu-id="1262b-122">Aşağıdaki tabloda maliyet nesnesinin ve stok nesnesinin ne oldukları gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="1262b-122">The following table shows what is a cost object and what is an inventory object.</span></span>

| <span data-ttu-id="1262b-123">Nesne türü</span><span class="sxs-lookup"><span data-stu-id="1262b-123">Object type</span></span>      | <span data-ttu-id="1262b-124">Madde kodu</span><span class="sxs-lookup"><span data-stu-id="1262b-124">Item number</span></span> | <span data-ttu-id="1262b-125">Tesis</span><span class="sxs-lookup"><span data-stu-id="1262b-125">Site</span></span> | <span data-ttu-id="1262b-126">Ambar</span><span class="sxs-lookup"><span data-stu-id="1262b-126">Warehouse</span></span> | <span data-ttu-id="1262b-127">Bordro Numarası</span><span class="sxs-lookup"><span data-stu-id="1262b-127">Batch No.</span></span> |
|------------------|-------------|------|-----------|-----------|
| <span data-ttu-id="1262b-128">Maliyet nesnesi</span><span class="sxs-lookup"><span data-stu-id="1262b-128">Cost object</span></span>      | <span data-ttu-id="1262b-129">x</span><span class="sxs-lookup"><span data-stu-id="1262b-129">x</span></span>           | <span data-ttu-id="1262b-130">x</span><span class="sxs-lookup"><span data-stu-id="1262b-130">x</span></span>    |           |           |
| <span data-ttu-id="1262b-131">Stok nesnesi</span><span class="sxs-lookup"><span data-stu-id="1262b-131">Inventory object</span></span> | <span data-ttu-id="1262b-132">x</span><span class="sxs-lookup"><span data-stu-id="1262b-132">x</span></span>           | <span data-ttu-id="1262b-133">x</span><span class="sxs-lookup"><span data-stu-id="1262b-133">x</span></span>    |  <span data-ttu-id="1262b-134">x</span><span class="sxs-lookup"><span data-stu-id="1262b-134">x</span></span>        | <span data-ttu-id="1262b-135">x</span><span class="sxs-lookup"><span data-stu-id="1262b-135">x</span></span>         |

## <a name="accumulation-of-costs-and-quantities"></a><span data-ttu-id="1262b-136">Maliyetlerin ve miktarların toplamı</span><span class="sxs-lookup"><span data-stu-id="1262b-136">Accumulation of costs and quantities</span></span>
-   <span data-ttu-id="1262b-137">**Değer** alanındaki değer, aşağıdaki değerlerin toplamıdır:</span><span class="sxs-lookup"><span data-stu-id="1262b-137">The value in the **Value** fieldis a sum of the following values:</span></span>
    -   <span data-ttu-id="1262b-138">Fiziksel maliyet tutarı</span><span class="sxs-lookup"><span data-stu-id="1262b-138">Physical cost amount</span></span>
    -   <span data-ttu-id="1262b-139">Mali maliyet tutarı</span><span class="sxs-lookup"><span data-stu-id="1262b-139">Financial cost amount</span></span>
    -   <span data-ttu-id="1262b-140">Ayarlamalar</span><span class="sxs-lookup"><span data-stu-id="1262b-140">Adjustments</span></span>
-   <span data-ttu-id="1262b-141">**Miktar** alanındaki değer, aşağıdaki değerlerin toplamıdır:</span><span class="sxs-lookup"><span data-stu-id="1262b-141">The value in the **Quantity** field is a sum of the following values:</span></span>
    -   <span data-ttu-id="1262b-142">Alınan</span><span class="sxs-lookup"><span data-stu-id="1262b-142">Received</span></span>
    -   <span data-ttu-id="1262b-143">Düşülen</span><span class="sxs-lookup"><span data-stu-id="1262b-143">Deducted</span></span>
    -   <span data-ttu-id="1262b-144">Deftere nakledilen miktar</span><span class="sxs-lookup"><span data-stu-id="1262b-144">Posted quantity</span></span>
-   <span data-ttu-id="1262b-145">**Ortalama birim maliyeti** alanı, hesaplanan bir alandır.</span><span class="sxs-lookup"><span data-stu-id="1262b-145">The **Average unit cost** field is a calculated field.</span></span> <span data-ttu-id="1262b-146">Değer, **Değer** değerinin **Miktar** değerine bölünmesiyle bulunur.</span><span class="sxs-lookup"><span data-stu-id="1262b-146">The value is calculated by dividing the **Value** value by the **Quantity** value.</span></span>

<span data-ttu-id="1262b-147">**Not:** **Fiziksel değeri dahil** et parametresinin, önceki hesaplamalar üzerinde etkisi yoktur.</span><span class="sxs-lookup"><span data-stu-id="1262b-147">**Note:** The \*\*Include physical value \*\*parameter has no effect on the preceding calculations.</span></span>

<a name="additional-resources"></a><span data-ttu-id="1262b-148">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="1262b-148">Additional resources</span></span>
--------

[<span data-ttu-id="1262b-149">Ürün boyut grubu</span><span class="sxs-lookup"><span data-stu-id="1262b-149">Product dimension group</span></span>](https://technet.microsoft.com/library/aa499382.aspx)

[<span data-ttu-id="1262b-150">Depolama boyutu grubu</span><span class="sxs-lookup"><span data-stu-id="1262b-150">Storage dimension group</span></span>](https://technet.microsoft.com/library/hh209317.aspx)

[<span data-ttu-id="1262b-151">İzleme boyutu grubu</span><span class="sxs-lookup"><span data-stu-id="1262b-151">Tracking dimension group</span></span>](https://technet.microsoft.com/library/hh209465.aspx)

[<span data-ttu-id="1262b-152">Yenilikler veya değişenler</span><span class="sxs-lookup"><span data-stu-id="1262b-152">What's new or changed</span></span>](../../fin-and-ops/get-started/whats-new-changed.md)

[<span data-ttu-id="1262b-153">Maliyet girişleri</span><span class="sxs-lookup"><span data-stu-id="1262b-153">Cost entries</span></span>](cost-entries.md)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]