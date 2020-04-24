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
ms.search.scope: Core, Operations
ms.custom: 19451
ms.assetid: ec776b98-813a-490d-848f-468452d98fac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: shylaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 50849a173e74ad88dd10c6a30ea66c91b936e165
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/02/2020
ms.locfileid: "3201790"
---
# <a name="cost-objects"></a><span data-ttu-id="f8ced-105">Maliyet nesneleri</span><span class="sxs-lookup"><span data-stu-id="f8ced-105">Cost objects</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f8ced-106">Bu makalede, maliyet nesneleri hakkında bilgiler verilmekte, maliyetlerin ve miktarların nasıl biriktirildiği açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="f8ced-106">This article provides information about costs objects, and explains how costs and quantities are accumulated.</span></span> <span data-ttu-id="f8ced-107">Maliyet nesnesi, maliyetlerin ve miktarların toplandığı bir varlıktır.</span><span class="sxs-lookup"><span data-stu-id="f8ced-107">A cost object is an entity that costs and quantities are accumulated for.</span></span> <span data-ttu-id="f8ced-108">Maliyet nesnesi varlığı, bir ürün veya ürün çeşidi (stil, renk vb.) olabilir.</span><span class="sxs-lookup"><span data-stu-id="f8ced-108">A cost object entity can be either a product or product variants, such as variants for style and color.</span></span>  

## <a name="cost-objects"></a><span data-ttu-id="f8ced-109">Maliyet nesneleri</span><span class="sxs-lookup"><span data-stu-id="f8ced-109">Cost objects</span></span>

<span data-ttu-id="f8ced-110">**Maliyet nesneleri** sayfasında, bir ürüne kayıtlı tüm maliyet nesneleri listelenir.</span><span class="sxs-lookup"><span data-stu-id="f8ced-110">The **Cost objects** page lists all cost objects that are registered on a product.</span></span> <span data-ttu-id="f8ced-111">Maliyet nesneleri aşağıdaki kaynaklardan gelen verilerle tanımlanır:</span><span class="sxs-lookup"><span data-stu-id="f8ced-111">The cost objects are defined by data from the following sources:</span></span>

-   <span data-ttu-id="f8ced-112">Ürün</span><span class="sxs-lookup"><span data-stu-id="f8ced-112">Product</span></span>
-   <span data-ttu-id="f8ced-113">Ürün boyut grubu</span><span class="sxs-lookup"><span data-stu-id="f8ced-113">Product dimension group</span></span>
-   <span data-ttu-id="f8ced-114">Depolama boyutu grubu</span><span class="sxs-lookup"><span data-stu-id="f8ced-114">Storage dimension group</span></span>
-   <span data-ttu-id="f8ced-115">İzleme boyut grubu</span><span class="sxs-lookup"><span data-stu-id="f8ced-115">Tracking dimension group</span></span>

<span data-ttu-id="f8ced-116">**Not:** Maliyet nesnesi, yalnızca **Doğrudan malzeme** türündeki bir maliyet öğesini temsil eder.</span><span class="sxs-lookup"><span data-stu-id="f8ced-116">**Note:** A cost object represents a cost element of the **Direct material** type only.</span></span> <span data-ttu-id="f8ced-117">Maliyet nesnesi ve stok nesnesi arasındaki fark, maliyet nesnesinin mali stok için seçilen stok boyutlarıyla tanımlanmasıdır.</span><span class="sxs-lookup"><span data-stu-id="f8ced-117">A cost object and an inventory object differ in the way that a cost object is defined by the inventory dimensions that are selected for financial inventory.</span></span> <span data-ttu-id="f8ced-118">Diyelim ki bir madde aşağıdaki şekilde yapılandırılmış:</span><span class="sxs-lookup"><span data-stu-id="f8ced-118">For example, an item has the following configuration:</span></span>

-   <span data-ttu-id="f8ced-119">**Tesis:** Fiziksel stok = Evet, Mali stok = Evet</span><span class="sxs-lookup"><span data-stu-id="f8ced-119">**Site:** Physical inventory = Yes, Financial inventory = Yes</span></span>
-   <span data-ttu-id="f8ced-120">**Ambar:** Fiziksel stok = Evet, Mali stok = Hayır</span><span class="sxs-lookup"><span data-stu-id="f8ced-120">**Warehouse:** Physical inventory = Yes, Financial inventory = No</span></span>
-   <span data-ttu-id="f8ced-121">**Toplu İş No:** Fiziksel stok = Evet, Mali stok = Hayır</span><span class="sxs-lookup"><span data-stu-id="f8ced-121">**Batch No.:** Physical inventory = Yes, Financial inventory = No</span></span>

<span data-ttu-id="f8ced-122">Aşağıdaki tabloda maliyet nesnesinin ve stok nesnesinin ne oldukları gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="f8ced-122">The following table shows what is a cost object and what is an inventory object.</span></span>

| <span data-ttu-id="f8ced-123">Nesne türü</span><span class="sxs-lookup"><span data-stu-id="f8ced-123">Object type</span></span>      | <span data-ttu-id="f8ced-124">Madde kodu</span><span class="sxs-lookup"><span data-stu-id="f8ced-124">Item number</span></span> | <span data-ttu-id="f8ced-125">Tesis</span><span class="sxs-lookup"><span data-stu-id="f8ced-125">Site</span></span> | <span data-ttu-id="f8ced-126">Ambar</span><span class="sxs-lookup"><span data-stu-id="f8ced-126">Warehouse</span></span> | <span data-ttu-id="f8ced-127">Bordro Numarası</span><span class="sxs-lookup"><span data-stu-id="f8ced-127">Batch No.</span></span> |
|------------------|-------------|------|-----------|-----------|
| <span data-ttu-id="f8ced-128">Maliyet nesnesi</span><span class="sxs-lookup"><span data-stu-id="f8ced-128">Cost object</span></span>      | <span data-ttu-id="f8ced-129">x</span><span class="sxs-lookup"><span data-stu-id="f8ced-129">x</span></span>           | <span data-ttu-id="f8ced-130">x</span><span class="sxs-lookup"><span data-stu-id="f8ced-130">x</span></span>    |           |           |
| <span data-ttu-id="f8ced-131">Stok nesnesi</span><span class="sxs-lookup"><span data-stu-id="f8ced-131">Inventory object</span></span> | <span data-ttu-id="f8ced-132">x</span><span class="sxs-lookup"><span data-stu-id="f8ced-132">x</span></span>           | <span data-ttu-id="f8ced-133">x</span><span class="sxs-lookup"><span data-stu-id="f8ced-133">x</span></span>    |  <span data-ttu-id="f8ced-134">x</span><span class="sxs-lookup"><span data-stu-id="f8ced-134">x</span></span>        | <span data-ttu-id="f8ced-135">x</span><span class="sxs-lookup"><span data-stu-id="f8ced-135">x</span></span>         |

## <a name="accumulation-of-costs-and-quantities"></a><span data-ttu-id="f8ced-136">Maliyetlerin ve miktarların toplamı</span><span class="sxs-lookup"><span data-stu-id="f8ced-136">Accumulation of costs and quantities</span></span>
-   <span data-ttu-id="f8ced-137">**Değer** alanındaki değer, aşağıdaki değerlerin toplamıdır:</span><span class="sxs-lookup"><span data-stu-id="f8ced-137">The value in the **Value** fieldis a sum of the following values:</span></span>
    -   <span data-ttu-id="f8ced-138">Fiziksel maliyet tutarı</span><span class="sxs-lookup"><span data-stu-id="f8ced-138">Physical cost amount</span></span>
    -   <span data-ttu-id="f8ced-139">Mali maliyet tutarı</span><span class="sxs-lookup"><span data-stu-id="f8ced-139">Financial cost amount</span></span>
    -   <span data-ttu-id="f8ced-140">Ayarlamalar</span><span class="sxs-lookup"><span data-stu-id="f8ced-140">Adjustments</span></span>
-   <span data-ttu-id="f8ced-141">**Miktar** alanındaki değer, aşağıdaki değerlerin toplamıdır:</span><span class="sxs-lookup"><span data-stu-id="f8ced-141">The value in the **Quantity** field is a sum of the following values:</span></span>
    -   <span data-ttu-id="f8ced-142">Alınan</span><span class="sxs-lookup"><span data-stu-id="f8ced-142">Received</span></span>
    -   <span data-ttu-id="f8ced-143">Düşülen</span><span class="sxs-lookup"><span data-stu-id="f8ced-143">Deducted</span></span>
    -   <span data-ttu-id="f8ced-144">Deftere nakledilen miktar</span><span class="sxs-lookup"><span data-stu-id="f8ced-144">Posted quantity</span></span>
-   <span data-ttu-id="f8ced-145">**Ortalama birim maliyeti** alanı, hesaplanan bir alandır.</span><span class="sxs-lookup"><span data-stu-id="f8ced-145">The **Average unit cost** field is a calculated field.</span></span> <span data-ttu-id="f8ced-146">Değer, **Değer** değerinin **Miktar** değerine bölünmesiyle bulunur.</span><span class="sxs-lookup"><span data-stu-id="f8ced-146">The value is calculated by dividing the **Value** value by the **Quantity** value.</span></span>

<span data-ttu-id="f8ced-147">**Not:** **Fiziksel değeri dahil** et parametresinin, önceki hesaplamalar üzerinde etkisi yoktur.</span><span class="sxs-lookup"><span data-stu-id="f8ced-147">**Note:** The \*\*Include physical value \*\*parameter has no effect on the preceding calculations.</span></span>

<a name="additional-resources"></a><span data-ttu-id="f8ced-148">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="f8ced-148">Additional resources</span></span>
--------

[<span data-ttu-id="f8ced-149">Ürün boyut grubu</span><span class="sxs-lookup"><span data-stu-id="f8ced-149">Product dimension group</span></span>](https://technet.microsoft.com/library/aa499382.aspx)

[<span data-ttu-id="f8ced-150">Depolama boyutu grubu</span><span class="sxs-lookup"><span data-stu-id="f8ced-150">Storage dimension group</span></span>](https://technet.microsoft.com/library/hh209317.aspx)

[<span data-ttu-id="f8ced-151">İzleme boyutu grubu</span><span class="sxs-lookup"><span data-stu-id="f8ced-151">Tracking dimension group</span></span>](https://technet.microsoft.com/library/hh209465.aspx)

[<span data-ttu-id="f8ced-152">Yenilikler veya değişenler</span><span class="sxs-lookup"><span data-stu-id="f8ced-152">What's new or changed</span></span>](../../fin-and-ops/get-started/whats-new-changed.md)

[<span data-ttu-id="f8ced-153">Maliyet girişleri</span><span class="sxs-lookup"><span data-stu-id="f8ced-153">Cost entries</span></span>](cost-entries.md)



