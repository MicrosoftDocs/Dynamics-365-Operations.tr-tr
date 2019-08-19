---
title: Maliyet nesneleri
description: Bu makalede, maliyet nesneleri hakkında bilgiler verilmekte, maliyetlerin ve miktarların nasıl biriktirildiği açıklanmaktadır. Maliyet nesnesi, maliyetlerin ve miktarların toplandığı bir varlıktır. Maliyet nesnesi varlığı, bir ürün veya ürün çeşidi (stil, renk vb.) olabilir.
author: AndersGirke
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventCostOnhandItem
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 19451
ms.assetid: ec776b98-813a-490d-848f-468452d98fac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: shylaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6501e8d809d12df421ad081662d23a6b5005f39c
ms.sourcegitcommit: 45f8cea6ac75bd2f4187380546a201c056072c59
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/12/2019
ms.locfileid: "1742149"
---
# <a name="cost-objects"></a><span data-ttu-id="f4b75-105">Maliyet nesneleri</span><span class="sxs-lookup"><span data-stu-id="f4b75-105">Cost objects</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f4b75-106">Bu makalede, maliyet nesneleri hakkında bilgiler verilmekte, maliyetlerin ve miktarların nasıl biriktirildiği açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="f4b75-106">This article provides information about costs objects, and explains how costs and quantities are accumulated.</span></span> <span data-ttu-id="f4b75-107">Maliyet nesnesi, maliyetlerin ve miktarların toplandığı bir varlıktır.</span><span class="sxs-lookup"><span data-stu-id="f4b75-107">A cost object is an entity that costs and quantities are accumulated for.</span></span> <span data-ttu-id="f4b75-108">Maliyet nesnesi varlığı, bir ürün veya ürün çeşidi (stil, renk vb.) olabilir.</span><span class="sxs-lookup"><span data-stu-id="f4b75-108">A cost object entity can be either a product or product variants, such as variants for style and color.</span></span>  

## <a name="cost-objects"></a><span data-ttu-id="f4b75-109">Maliyet nesneleri</span><span class="sxs-lookup"><span data-stu-id="f4b75-109">Cost objects</span></span>

<span data-ttu-id="f4b75-110">**Maliyet nesneleri** sayfasında, bir ürüne kayıtlı tüm maliyet nesneleri listelenir.</span><span class="sxs-lookup"><span data-stu-id="f4b75-110">The **Cost objects** page lists all cost objects that are registered on a product.</span></span> <span data-ttu-id="f4b75-111">Maliyet nesneleri aşağıdaki kaynaklardan gelen verilerle tanımlanır:</span><span class="sxs-lookup"><span data-stu-id="f4b75-111">The cost objects are defined by data from the following sources:</span></span>

-   <span data-ttu-id="f4b75-112">Ürün</span><span class="sxs-lookup"><span data-stu-id="f4b75-112">Product</span></span>
-   <span data-ttu-id="f4b75-113">Ürün boyut grubu</span><span class="sxs-lookup"><span data-stu-id="f4b75-113">Product dimension group</span></span>
-   <span data-ttu-id="f4b75-114">Depolama boyutu grubu</span><span class="sxs-lookup"><span data-stu-id="f4b75-114">Storage dimension group</span></span>
-   <span data-ttu-id="f4b75-115">İzleme boyut grubu</span><span class="sxs-lookup"><span data-stu-id="f4b75-115">Tracking dimension group</span></span>

<span data-ttu-id="f4b75-116">**Not:** Maliyet nesnesi, yalnızca **Doğrudan malzeme** türündeki bir maliyet öğesini temsil eder.</span><span class="sxs-lookup"><span data-stu-id="f4b75-116">**Note:** A cost object represents a cost element of the **Direct material** type only.</span></span> <span data-ttu-id="f4b75-117">Maliyet nesnesi ve stok nesnesi arasındaki fark, maliyet nesnesinin mali stok için seçilen stok boyutlarıyla tanımlanmasıdır.</span><span class="sxs-lookup"><span data-stu-id="f4b75-117">A cost object and an inventory object differ in the way that a cost object is defined by the inventory dimensions that are selected for financial inventory.</span></span> <span data-ttu-id="f4b75-118">Diyelim ki bir madde aşağıdaki şekilde yapılandırılmış:</span><span class="sxs-lookup"><span data-stu-id="f4b75-118">For example, an item has the following configuration:</span></span>

-   <span data-ttu-id="f4b75-119">**Tesis:** Fiziksel stok = Evet, Mali stok = Evet</span><span class="sxs-lookup"><span data-stu-id="f4b75-119">**Site:** Physical inventory = Yes, Financial inventory = Yes</span></span>
-   <span data-ttu-id="f4b75-120">**Ambar:** Fiziksel stok = Evet, Mali stok = Hayır</span><span class="sxs-lookup"><span data-stu-id="f4b75-120">**Warehouse:** Physical inventory = Yes, Financial inventory = No</span></span>
-   <span data-ttu-id="f4b75-121">**Toplu İş No:** Fiziksel stok = Evet, Mali stok = Hayır</span><span class="sxs-lookup"><span data-stu-id="f4b75-121">**Batch No.:** Physical inventory = Yes, Financial inventory = No</span></span>

<span data-ttu-id="f4b75-122">Aşağıdaki tabloda maliyet nesnesinin ve stok nesnesinin ne oldukları gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="f4b75-122">The following table shows what is a cost object and what is an inventory object.</span></span>

| <span data-ttu-id="f4b75-123">Nesne türü</span><span class="sxs-lookup"><span data-stu-id="f4b75-123">Object type</span></span>      | <span data-ttu-id="f4b75-124">Madde kodu</span><span class="sxs-lookup"><span data-stu-id="f4b75-124">Item number</span></span> | <span data-ttu-id="f4b75-125">Tesis</span><span class="sxs-lookup"><span data-stu-id="f4b75-125">Site</span></span> | <span data-ttu-id="f4b75-126">Ambar</span><span class="sxs-lookup"><span data-stu-id="f4b75-126">Warehouse</span></span> | <span data-ttu-id="f4b75-127">Bordro Numarası</span><span class="sxs-lookup"><span data-stu-id="f4b75-127">Batch No.</span></span> |
|------------------|-------------|------|-----------|-----------|
| <span data-ttu-id="f4b75-128">Maliyet nesnesi</span><span class="sxs-lookup"><span data-stu-id="f4b75-128">Cost object</span></span>      | <span data-ttu-id="f4b75-129">x</span><span class="sxs-lookup"><span data-stu-id="f4b75-129">x</span></span>           | <span data-ttu-id="f4b75-130">x</span><span class="sxs-lookup"><span data-stu-id="f4b75-130">x</span></span>    |           |           |
| <span data-ttu-id="f4b75-131">Stok nesnesi</span><span class="sxs-lookup"><span data-stu-id="f4b75-131">Inventory object</span></span> | <span data-ttu-id="f4b75-132">x</span><span class="sxs-lookup"><span data-stu-id="f4b75-132">x</span></span>           | <span data-ttu-id="f4b75-133">x</span><span class="sxs-lookup"><span data-stu-id="f4b75-133">x</span></span>    |  <span data-ttu-id="f4b75-134">x</span><span class="sxs-lookup"><span data-stu-id="f4b75-134">x</span></span>        | <span data-ttu-id="f4b75-135">x</span><span class="sxs-lookup"><span data-stu-id="f4b75-135">x</span></span>         |

## <a name="accumulation-of-costs-and-quantities"></a><span data-ttu-id="f4b75-136">Maliyetlerin ve miktarların toplamı</span><span class="sxs-lookup"><span data-stu-id="f4b75-136">Accumulation of costs and quantities</span></span>
-   <span data-ttu-id="f4b75-137">**Değer** alanındaki değer, aşağıdaki değerlerin toplamıdır:</span><span class="sxs-lookup"><span data-stu-id="f4b75-137">The value in the **Value** fieldis a sum of the following values:</span></span>
    -   <span data-ttu-id="f4b75-138">Fiziksel maliyet tutarı</span><span class="sxs-lookup"><span data-stu-id="f4b75-138">Physical cost amount</span></span>
    -   <span data-ttu-id="f4b75-139">Mali maliyet tutarı</span><span class="sxs-lookup"><span data-stu-id="f4b75-139">Financial cost amount</span></span>
    -   <span data-ttu-id="f4b75-140">Ayarlamalar</span><span class="sxs-lookup"><span data-stu-id="f4b75-140">Adjustments</span></span>
-   <span data-ttu-id="f4b75-141">**Miktar** alanındaki değer, aşağıdaki değerlerin toplamıdır:</span><span class="sxs-lookup"><span data-stu-id="f4b75-141">The value in the **Quantity** field is a sum of the following values:</span></span>
    -   <span data-ttu-id="f4b75-142">Alınan</span><span class="sxs-lookup"><span data-stu-id="f4b75-142">Received</span></span>
    -   <span data-ttu-id="f4b75-143">Düşülen</span><span class="sxs-lookup"><span data-stu-id="f4b75-143">Deducted</span></span>
    -   <span data-ttu-id="f4b75-144">Deftere nakledilen miktar</span><span class="sxs-lookup"><span data-stu-id="f4b75-144">Posted quantity</span></span>
-   <span data-ttu-id="f4b75-145">**Ortalama birim maliyeti** alanı, hesaplanan bir alandır.</span><span class="sxs-lookup"><span data-stu-id="f4b75-145">The **Average unit cost** field is a calculated field.</span></span> <span data-ttu-id="f4b75-146">Değer, **Değer** değerinin **Miktar** değerine bölünmesiyle bulunur.</span><span class="sxs-lookup"><span data-stu-id="f4b75-146">The value is calculated by dividing the **Value** value by the **Quantity** value.</span></span>

<span data-ttu-id="f4b75-147">**Not:** **Fiziksel değeri dahil** et parametresinin, önceki hesaplamalar üzerinde etkisi yoktur.</span><span class="sxs-lookup"><span data-stu-id="f4b75-147">**Note:** The \*\*Include physical value \*\*parameter has no effect on the preceding calculations.</span></span>

<a name="additional-resources"></a><span data-ttu-id="f4b75-148">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="f4b75-148">Additional resources</span></span>
--------

[<span data-ttu-id="f4b75-149">Ürün boyut grubu</span><span class="sxs-lookup"><span data-stu-id="f4b75-149">Product dimension group</span></span>](https://technet.microsoft.com/library/aa499382.aspx)

[<span data-ttu-id="f4b75-150">Depolama boyutu grubu</span><span class="sxs-lookup"><span data-stu-id="f4b75-150">Storage dimension group</span></span>](https://technet.microsoft.com/library/hh209317.aspx)

[<span data-ttu-id="f4b75-151">İzleme boyutu grubu</span><span class="sxs-lookup"><span data-stu-id="f4b75-151">Tracking dimension group</span></span>](https://technet.microsoft.com/library/hh209465.aspx)

[<span data-ttu-id="f4b75-152">Yenilikler veya değişenler</span><span class="sxs-lookup"><span data-stu-id="f4b75-152">What's new or changed</span></span>](../../fin-and-ops/get-started/whats-new-changed.md)

[<span data-ttu-id="f4b75-153">Maliyet girişleri</span><span class="sxs-lookup"><span data-stu-id="f4b75-153">Cost entries</span></span>](cost-entries.md)



