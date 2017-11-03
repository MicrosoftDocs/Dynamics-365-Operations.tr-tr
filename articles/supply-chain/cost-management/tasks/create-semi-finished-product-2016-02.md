--- 
title: "Yarı mamul ürün oluşturma (yalnızca Şubat 2016)"
description: "Bu görev, yarı mamul bir ürün oluşturmaya odaklanır."
author: YuyuScheller
manager: AnnBe
ms.date: 02/07/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.author: yuyus
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 4d06f291036c656731a00fcf312e229ed9e9f3d0
ms.openlocfilehash: 038d8cd9333635d3269bb4f62a5402c2309bfd3c
ms.contentlocale: tr-tr
ms.lasthandoff: 09/29/2017

---
# <a name="create-a-semi-finished-product-february-2016-only"></a><span data-ttu-id="358cb-103">Yarı mamul ürün oluşturma (yalnızca Şubat 2016)</span><span class="sxs-lookup"><span data-stu-id="358cb-103">Create a semi-finished product (February 2016 only)</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="358cb-104">Bu görev, yarı mamul bir ürün oluşturmaya odaklanır.</span><span class="sxs-lookup"><span data-stu-id="358cb-104">This task focuses on creating a semi-finished product.</span></span> <span data-ttu-id="358cb-105">Ürün Reçetesi hesaplama serisindeki ikinci görevdir.</span><span class="sxs-lookup"><span data-stu-id="358cb-105">It is the second task in the BOM calculation series.</span></span> <span data-ttu-id="358cb-106">Bu görevi oluşturmak için kullanılan demo veri şirketi USMF'dir.</span><span class="sxs-lookup"><span data-stu-id="358cb-106">The demo data company used to create this task is USMF.</span></span>

1. <span data-ttu-id="358cb-107">Product information management > Products > Released products (Ürün bilgi yönetimi > Ürünler > Piyasaya sürülmüş ürünler) menüsüne gidin.</span><span class="sxs-lookup"><span data-stu-id="358cb-107">Go to Product information management > Products > Released products.</span></span>
2. <span data-ttu-id="358cb-108">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="358cb-108">Click New.</span></span>
3. <span data-ttu-id="358cb-109">Ürün numarası alanında bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="358cb-109">In the Product number field, type a value.</span></span>
    * <span data-ttu-id="358cb-110">Bu örnek için BOM_2 yazın.</span><span class="sxs-lookup"><span data-stu-id="358cb-110">For this example, type BOM_2.</span></span>  
4. <span data-ttu-id="358cb-111">Model grubu alanına bir değer girin veya bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="358cb-111">In the Item model group field, enter or select a value.</span></span>
    * <span data-ttu-id="358cb-112">STD öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="358cb-112">Select STD.</span></span> <span data-ttu-id="358cb-113">STD, standart maliyet anlamına gelir ve maliyet hesaplamalarıyla çalışırken en yaygın olarak kullanılan modeldir.</span><span class="sxs-lookup"><span data-stu-id="358cb-113">STD stands for standard cost and is the most commonly used model when working with cost calculations.</span></span>  
5. <span data-ttu-id="358cb-114">Ürün grubu alanında bir değer girin veya bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="358cb-114">In the Item group field, enter or select a value.</span></span>
    * <span data-ttu-id="358cb-115">Örneğin, Ses'i seçin.</span><span class="sxs-lookup"><span data-stu-id="358cb-115">For example, select Audio.</span></span> <span data-ttu-id="358cb-116">Bunun, maliyet hesaplamaları üzerinde hiçbir etkisi yoktur.</span><span class="sxs-lookup"><span data-stu-id="358cb-116">This has no impact on cost calculations.</span></span>  
6. <span data-ttu-id="358cb-117">Stok boyutu grubu alanına bir değer girin veya bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="358cb-117">In the Storage dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="358cb-118">SiteWH'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="358cb-118">Select SiteWH.</span></span> <span data-ttu-id="358cb-119">Bu örnek için yalnızca Tesis ve Ambar kullanılır.</span><span class="sxs-lookup"><span data-stu-id="358cb-119">Only Site and Warehouse will be used for this example.</span></span>  
7. <span data-ttu-id="358cb-120">İzleme boyutu grubu alanına bir değer girin veya bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="358cb-120">In the Tracking dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="358cb-121">Bu örnek için izleme boyutları kullanılmaz. Hiçbiri'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="358cb-121">Tracking dimensions will not be used for this example, select None.</span></span>  
8. <span data-ttu-id="358cb-122">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="358cb-122">Click OK.</span></span>
9. <span data-ttu-id="358cb-123">Eylem Bölmesinde, Stok yönetimi'ne tıklayın.</span><span class="sxs-lookup"><span data-stu-id="358cb-123">On the Action Pane, click Manage inventory.</span></span>
10. <span data-ttu-id="358cb-124">Varsayılan sipariş ayarlarına tıklayın.</span><span class="sxs-lookup"><span data-stu-id="358cb-124">Click Default order settings.</span></span>
11. <span data-ttu-id="358cb-125">Varsayılan sipariş türü alanında, "Üretim" öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="358cb-125">In the Default order type field, select 'Production'.</span></span>
    * <span data-ttu-id="358cb-126">Bu, üretilecek olan yarı mamul bir ürün olduğundan Üretim'i seçin.</span><span class="sxs-lookup"><span data-stu-id="358cb-126">Because this is a semi-finished product that will be produced, select Production.</span></span>  
12. <span data-ttu-id="358cb-127">Satınalma tesisi alanına bir değer girin veya buradan bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="358cb-127">In the Purchase site field, enter or select a value.</span></span>
    * <span data-ttu-id="358cb-128">Bu örnek için, Tesis 1'i seçin.</span><span class="sxs-lookup"><span data-stu-id="358cb-128">For this example, select Site 1.</span></span>  
13. <span data-ttu-id="358cb-129">Stok tesisi alanına bir değer girin veya buradan bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="358cb-129">In the Inventory site field, enter or select a value.</span></span>
    * <span data-ttu-id="358cb-130">Bu örnek için, Tesis 1'i seçin.</span><span class="sxs-lookup"><span data-stu-id="358cb-130">For this example, select Site 1.</span></span>  
14. <span data-ttu-id="358cb-131">Satış tesisi alanına bir değer girin veya buradan bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="358cb-131">In the Sales site field, enter or select a value.</span></span>
    * <span data-ttu-id="358cb-132">Bu örnek için, Tesis 1'i seçin.</span><span class="sxs-lookup"><span data-stu-id="358cb-132">For this example, select Site 1.</span></span>  
15. <span data-ttu-id="358cb-133">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="358cb-133">Close the page.</span></span>
16. <span data-ttu-id="358cb-134">Eylem Bölmesinde Yönet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="358cb-134">On the Action Pane, click Manage costs.</span></span>
17. <span data-ttu-id="358cb-135">Madde fiyatı'na tıklayın.</span><span class="sxs-lookup"><span data-stu-id="358cb-135">Click Item price.</span></span>
18. <span data-ttu-id="358cb-136">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="358cb-136">Click New.</span></span>
19. <span data-ttu-id="358cb-137">Listede, seçili satırı işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="358cb-137">In the list, mark the selected row.</span></span>
20. <span data-ttu-id="358cb-138">Sürüm alanına bir değer girin veya buradan bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="358cb-138">In the Version field, enter or select a value.</span></span>
    * <span data-ttu-id="358cb-139">Bu örnek için, Sürüm 10'u seçin.</span><span class="sxs-lookup"><span data-stu-id="358cb-139">For this example, select Version 10.</span></span>  
21. <span data-ttu-id="358cb-140">Tesis alanına bir değer girin veya buradan bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="358cb-140">In the Site field, enter or select a value.</span></span>
    * <span data-ttu-id="358cb-141">Bu örnek için, Tesis 1'i seçin.</span><span class="sxs-lookup"><span data-stu-id="358cb-141">For this example, select Site 1.</span></span>  
22. <span data-ttu-id="358cb-142">Fiyatı "10" olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="358cb-142">Set Price to '10'.</span></span>
    * <span data-ttu-id="358cb-143">Bu örnek için maliyet fiyatı olarak 10 yazın.</span><span class="sxs-lookup"><span data-stu-id="358cb-143">For this example, type a cost price of 10.</span></span>  
23. <span data-ttu-id="358cb-144">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="358cb-144">Click Save.</span></span>
24. <span data-ttu-id="358cb-145">Beklemedeki fiyatı/fiyatları etkinleştir'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="358cb-145">Click Activate pending price(s).</span></span>
25. <span data-ttu-id="358cb-146">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="358cb-146">Close the page.</span></span>
26. <span data-ttu-id="358cb-147">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="358cb-147">Close the page.</span></span>
27. <span data-ttu-id="358cb-148">Açmak için BOM_2'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="358cb-148">Click BOM_2 to open it.</span></span>
28. <span data-ttu-id="358cb-149">Maliyetleri yönet bölümünü genişletin.</span><span class="sxs-lookup"><span data-stu-id="358cb-149">Expand the Manage costs section.</span></span>
29. <span data-ttu-id="358cb-150">Maliyet grubu alanına bir değer girin veya buradan bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="358cb-150">In the Cost group field, enter or select a value.</span></span>
    * <span data-ttu-id="358cb-151">Bu örnek için Maliyet grubu M1'i seçin.</span><span class="sxs-lookup"><span data-stu-id="358cb-151">For this example, select Cost group M1.</span></span>  
30. <span data-ttu-id="358cb-152">Bir kaydı kaydetmek için kısayolu kullanın.</span><span class="sxs-lookup"><span data-stu-id="358cb-152">Use the shortcut for saving a record.</span></span>
31. <span data-ttu-id="358cb-153">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="358cb-153">Close the page.</span></span>

