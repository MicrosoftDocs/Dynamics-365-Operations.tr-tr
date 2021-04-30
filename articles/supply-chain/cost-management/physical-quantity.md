---
title: Stok nesnesi değerleri
description: Bu makalede, stok nesnesi değerlerinin nasıl hesaplandığı hakkında bilgiler verilmektedir.
author: AndersGirke
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventCostOnhandItem
audience: Application User
ms.reviewer: kamaybac
ms.custom: 19111
ms.assetid: 56a7c8ba-bf4a-4b1d-918d-56bb96926c4f
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 543253714b3cf318ad5f6092b190e777772f956f
ms.sourcegitcommit: 34b478f175348d99df4f2f0c2f6c0c21b6b2660a
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2021
ms.locfileid: "5910149"
---
# <a name="inventory-object-values"></a><span data-ttu-id="bbb7a-103">Stok nesnesi değerleri</span><span class="sxs-lookup"><span data-stu-id="bbb7a-103">Inventory object values</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="bbb7a-104">Bu makalede, stok nesnesi değerlerinin nasıl hesaplandığı hakkında bilgiler verilmektedir.</span><span class="sxs-lookup"><span data-stu-id="bbb7a-104">This article provides information about how the values of an inventory object are calculated.</span></span> 

<span data-ttu-id="bbb7a-105">**Fiziksel miktar** adı yeni bir işlev, belirli bir stok nesnenin değerlerini görmenizi sağlıyor.</span><span class="sxs-lookup"><span data-stu-id="bbb7a-105">A new functionality that is named **physical quantity** lets you see the values of a specific inventory object.</span></span> 

<span data-ttu-id="bbb7a-106">Maliyet nesnesi, stok muhasebesinin uygulandığı varlık düzeyini temsil eder.</span><span class="sxs-lookup"><span data-stu-id="bbb7a-106">A cost object represents the entity level where inventory accounting is performed.</span></span> <span data-ttu-id="bbb7a-107">Maliyet nesneleri hakkında daha fazla bilgi için bkz. [Maliyet nesneleri](cost-object.md).</span><span class="sxs-lookup"><span data-stu-id="bbb7a-107">For more information about cost objects, see [Cost objects](cost-object.md).</span></span> 

<span data-ttu-id="bbb7a-108">Belirli stok nesnesinin değerlerini görmek için **Maliyet nesnesi** sayfasında **Fiziksel miktar**'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="bbb7a-108">To see the values of a specific inventory object, click **Physical quantity** on the **Cost object** page.</span></span> <span data-ttu-id="bbb7a-109">Bir stok nesnesinin değerinin nasıl hesaplanacağı aşağıda verilmiştir:</span><span class="sxs-lookup"><span data-stu-id="bbb7a-109">Here is how the value of an inventory object is calculated:</span></span> 

<span data-ttu-id="bbb7a-110">Stok nesnesi.Değer = Maliyet nesnesi.Ortalama birim maliyeti x Stok nesnesi.Miktar</span><span class="sxs-lookup"><span data-stu-id="bbb7a-110">Inventory object.Value = Cost object.Average unit cost × Inventory object.Quantity</span></span> 

<span data-ttu-id="bbb7a-111">Aşağıdaki örnekler, bir stok nesnesinin ve maliyet nesnesinin değerlerinin nasıl hesaplanacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="bbb7a-111">The following example shows how the values of an inventory object and a cost object are calculated.</span></span> <span data-ttu-id="bbb7a-112">A maddesinde iki ürün girişi etkinliği kayıtlıdır:</span><span class="sxs-lookup"><span data-stu-id="bbb7a-112">Two product receipt events are registered on item A:</span></span>

-   <span data-ttu-id="bbb7a-113">Ürün girişi 1: Miktar = 100 parça, Tutar = $1.000,00, Tesis = 1, Ambar = 11, Toplu İşlem No.</span><span class="sxs-lookup"><span data-stu-id="bbb7a-113">Product receipt 1: Quantity = 100 pcs., Amount = $1,000.00, Site = 1, Warehouse =11, Batch No.</span></span> <span data-ttu-id="bbb7a-114">= B1</span><span class="sxs-lookup"><span data-stu-id="bbb7a-114">= B1</span></span>
-   <span data-ttu-id="bbb7a-115">Ürün girişi 2: Miktar = 50 parça, Tutar = $800,00, Tesis = 1, Ambar = 11, Toplu İşlem No.</span><span class="sxs-lookup"><span data-stu-id="bbb7a-115">Product receipt 2: Quantity = 50 pcs., Amount = $800.00, Site = 1, Warehouse =11, Batch No.</span></span> <span data-ttu-id="bbb7a-116">= B2</span><span class="sxs-lookup"><span data-stu-id="bbb7a-116">= B2</span></span>

<span data-ttu-id="bbb7a-117">Aşağıdaki tabloda, bir maliyet nesnesi için yapılan hesaplamanın sonucu gösteriliyor.</span><span class="sxs-lookup"><span data-stu-id="bbb7a-117">The following table shows the calculation result for a cost object.</span></span> <span data-ttu-id="bbb7a-118">Sonucu **Maliyet nesnesi** sayfasında görüntüleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="bbb7a-118">You can view the result on the **Cost object** page.</span></span>

<table style="width:100%;">
<colgroup>
<col width="14%" />
<col width="14%" />
<col width="14%" />
<col width="14%" />
<col width="14%" />
<col width="14%" />
<col width="14%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="bbb7a-119">Nesne türü</span><span class="sxs-lookup"><span data-stu-id="bbb7a-119">Object type</span></span></th>
<th><span data-ttu-id="bbb7a-120">Madde kodu</span><span class="sxs-lookup"><span data-stu-id="bbb7a-120">Item number</span></span></th>
<th><span data-ttu-id="bbb7a-121">Tesis</span><span class="sxs-lookup"><span data-stu-id="bbb7a-121">Site</span></span></th>
<th><span data-ttu-id="bbb7a-122">Miktar</span><span class="sxs-lookup"><span data-stu-id="bbb7a-122">Quantity</span></span></th>
<th><span data-ttu-id="bbb7a-123">Stok birimi</span><span class="sxs-lookup"><span data-stu-id="bbb7a-123">Inventory unit</span></span></th>
<th><span data-ttu-id="bbb7a-124">Değer</span><span class="sxs-lookup"><span data-stu-id="bbb7a-124">Value</span></span></th>
<th><span data-ttu-id="bbb7a-125">Ortalama birim maliyeti</span><span class="sxs-lookup"><span data-stu-id="bbb7a-125">Average unit cost</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="bbb7a-126">Maliyet nesnesi</span><span class="sxs-lookup"><span data-stu-id="bbb7a-126">Cost object</span></span></td>
<td><span data-ttu-id="bbb7a-127">A:</span><span class="sxs-lookup"><span data-stu-id="bbb7a-127">A</span></span></td>
<td><span data-ttu-id="bbb7a-128">1</span><span class="sxs-lookup"><span data-stu-id="bbb7a-128">1</span></span></td>
<td><span data-ttu-id="bbb7a-129">150</span><span class="sxs-lookup"><span data-stu-id="bbb7a-129">150</span></span></td>
<td><span data-ttu-id="bbb7a-130">Prç</span><span class="sxs-lookup"><span data-stu-id="bbb7a-130">Pcs.</span></span></td>
<td><p><span data-ttu-id="bbb7a-131">1.800,00 lira</span><span class="sxs-lookup"><span data-stu-id="bbb7a-131">$1800.00</span></span></p></td>
<td><p><span data-ttu-id="bbb7a-132">12,00 lira</span><span class="sxs-lookup"><span data-stu-id="bbb7a-132">$12.00</span></span></p></td>
</tr>
</tbody>
</table>

<span data-ttu-id="bbb7a-133">Aşağıdaki tabloda, bir stok nesnesi için yapılan hesaplamanın sonucu gösteriliyor.</span><span class="sxs-lookup"><span data-stu-id="bbb7a-133">The following table shows the calculation result for an inventory object.</span></span> <span data-ttu-id="bbb7a-134">**Maliyet nesnesi** sayfasındaki **Fiziksel miktar**'a tıklayarak sonucu görüntüleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="bbb7a-134">You can view the result by clicking **Physical quantity** on the **Cost object** page.</span></span>

<table style="width:100%;">
<colgroup>
<col width="11%" />
<col width="11%" />
<col width="11%" />
<col width="11%" />
<col width="11%" />
<col width="11%" />
<col width="11%" />
<col width="11%" />
<col width="11%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="bbb7a-135">Nesne türü</span><span class="sxs-lookup"><span data-stu-id="bbb7a-135">Object type</span></span></th>
<th><span data-ttu-id="bbb7a-136">Madde kodu</span><span class="sxs-lookup"><span data-stu-id="bbb7a-136">Item number</span></span></th>
<th><span data-ttu-id="bbb7a-137">Tesis</span><span class="sxs-lookup"><span data-stu-id="bbb7a-137">Site</span></span></th>
<th><span data-ttu-id="bbb7a-138">Ambar</span><span class="sxs-lookup"><span data-stu-id="bbb7a-138">Warehouse</span></span></th>
<th><span data-ttu-id="bbb7a-139">Bordro Numarası</span><span class="sxs-lookup"><span data-stu-id="bbb7a-139">Batch No.</span></span></th>
<th><span data-ttu-id="bbb7a-140">Miktar</span><span class="sxs-lookup"><span data-stu-id="bbb7a-140">Quantity</span></span></th>
<th><span data-ttu-id="bbb7a-141">Stok birimi</span><span class="sxs-lookup"><span data-stu-id="bbb7a-141">Inventory unit</span></span></th>
<th><span data-ttu-id="bbb7a-142">Değer</span><span class="sxs-lookup"><span data-stu-id="bbb7a-142">Value</span></span></th>
<th><span data-ttu-id="bbb7a-143">Ortalama birim maliyeti</span><span class="sxs-lookup"><span data-stu-id="bbb7a-143">Average unit cost</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="bbb7a-144">Stok nesnesi</span><span class="sxs-lookup"><span data-stu-id="bbb7a-144">Inventory object</span></span></td>
<td><span data-ttu-id="bbb7a-145">A:</span><span class="sxs-lookup"><span data-stu-id="bbb7a-145">A</span></span></td>
<td><span data-ttu-id="bbb7a-146">1</span><span class="sxs-lookup"><span data-stu-id="bbb7a-146">1</span></span></td>
<td><span data-ttu-id="bbb7a-147">11</span><span class="sxs-lookup"><span data-stu-id="bbb7a-147">11</span></span></td>
<td><span data-ttu-id="bbb7a-148">B1</span><span class="sxs-lookup"><span data-stu-id="bbb7a-148">B1</span></span></td>
<td><span data-ttu-id="bbb7a-149">100</span><span class="sxs-lookup"><span data-stu-id="bbb7a-149">100</span></span></td>
<td><span data-ttu-id="bbb7a-150">Prç</span><span class="sxs-lookup"><span data-stu-id="bbb7a-150">Pcs.</span></span></td>
<td><p><span data-ttu-id="bbb7a-151">1.200,00 lira</span><span class="sxs-lookup"><span data-stu-id="bbb7a-151">$1200.00</span></span></p></td>
<td><p><span data-ttu-id="bbb7a-152">12,00 lira</span><span class="sxs-lookup"><span data-stu-id="bbb7a-152">$12.00</span></span></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="bbb7a-153">Stok nesnesi</span><span class="sxs-lookup"><span data-stu-id="bbb7a-153">Inventory object</span></span></td>
<td><span data-ttu-id="bbb7a-154">A</span><span class="sxs-lookup"><span data-stu-id="bbb7a-154">A</span></span></td>
<td><span data-ttu-id="bbb7a-155">1</span><span class="sxs-lookup"><span data-stu-id="bbb7a-155">1</span></span></td>
<td><span data-ttu-id="bbb7a-156">11</span><span class="sxs-lookup"><span data-stu-id="bbb7a-156">11</span></span></td>
<td><span data-ttu-id="bbb7a-157">B2</span><span class="sxs-lookup"><span data-stu-id="bbb7a-157">B2</span></span></td>
<td><span data-ttu-id="bbb7a-158">50</span><span class="sxs-lookup"><span data-stu-id="bbb7a-158">50</span></span></td>
<td><span data-ttu-id="bbb7a-159">Prç</span><span class="sxs-lookup"><span data-stu-id="bbb7a-159">Pcs.</span></span></td>
<td><p><span data-ttu-id="bbb7a-160">600,00 lira.</span><span class="sxs-lookup"><span data-stu-id="bbb7a-160">$600.00</span></span></p></td>
<td><p><span data-ttu-id="bbb7a-161">12,00 lira</span><span class="sxs-lookup"><span data-stu-id="bbb7a-161">$12.00</span></span></p></td>
</tr>
</tbody>
</table>



<a name="additional-resources"></a><span data-ttu-id="bbb7a-162">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="bbb7a-162">Additional resources</span></span>
--------

[<span data-ttu-id="bbb7a-163">Maliyet nesneleri</span><span class="sxs-lookup"><span data-stu-id="bbb7a-163">Cost objects</span></span>](cost-object.md)

[<span data-ttu-id="bbb7a-164">Maliyet girişleri</span><span class="sxs-lookup"><span data-stu-id="bbb7a-164">Cost entries</span></span>](cost-entries.md)

[<span data-ttu-id="bbb7a-165">Yenilikler ve değişiklikler</span><span class="sxs-lookup"><span data-stu-id="bbb7a-165">What's new and changed</span></span>](../../fin-ops-core/fin-ops/get-started/whats-new-changed.md)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]