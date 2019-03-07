---
title: Hammadde oluşturma (Şubat 2016)
description: Bu görev, bitmiş ve yarı mamul ürünlerin bileşenlerini oluşturmaya odaklanır.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResProductDetailsExtended, EcoResProductCreate, InventItemOrderSetup, InventItemPrice
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 091b6edaf43e86e6e3665bf79871648473e284c7
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2019
ms.locfileid: "351068"
---
# <a name="create-raw-materials-february-2016"></a><span data-ttu-id="55314-103">Hammadde oluşturma (Şubat 2016)</span><span class="sxs-lookup"><span data-stu-id="55314-103">Create raw materials (February 2016)</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="55314-104">Bu görev, bitmiş ve yarı mamul ürünlerin bileşenlerini oluşturmaya odaklanır.</span><span class="sxs-lookup"><span data-stu-id="55314-104">This task focuses on creating the components of finished and semi-finished products.</span></span> <span data-ttu-id="55314-105">Ürün Reçetesi hesaplama serisindeki üçüncü görevdir.</span><span class="sxs-lookup"><span data-stu-id="55314-105">It is the third task in the BOM calculation series.</span></span> <span data-ttu-id="55314-106">Bu görevi oluşturmak için kullanılan demo veri şirketi USMF'dir.</span><span class="sxs-lookup"><span data-stu-id="55314-106">The demo data company used to create this task is USMF.</span></span>


## <a name="create-the-first-material"></a><span data-ttu-id="55314-107">İlk malzemeyi oluşturma</span><span class="sxs-lookup"><span data-stu-id="55314-107">Create the first material</span></span>
1. <span data-ttu-id="55314-108">Product information management > Products > Released products (Ürün bilgi yönetimi > Ürünler > Piyasaya sürülmüş ürünler) menüsüne gidin.</span><span class="sxs-lookup"><span data-stu-id="55314-108">Go to Product information management > Products > Released products.</span></span>
2. <span data-ttu-id="55314-109">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="55314-109">Click New.</span></span>
3. <span data-ttu-id="55314-110">Ürün numarası alanında bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="55314-110">In the Product number field, type a value.</span></span>
    * <span data-ttu-id="55314-111">Bu örnek için, ITEM_A girin.</span><span class="sxs-lookup"><span data-stu-id="55314-111">For this example, enter ITEM_A.</span></span>  
4. <span data-ttu-id="55314-112">Model grubu alanına bir değer girin veya bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="55314-112">In the Item model group field, enter or select a value.</span></span>
    * <span data-ttu-id="55314-113">STD öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="55314-113">Select STD.</span></span> <span data-ttu-id="55314-114">STD, standart maliyet anlamına gelir ve maliyet hesaplamalarıyla çalışırken en yaygın olarak kullanılan modeldir.</span><span class="sxs-lookup"><span data-stu-id="55314-114">STD stands for standard cost and is the most commonly used model when working with cost calculations.</span></span>  
5. <span data-ttu-id="55314-115">Ürün grubu alanında bir değer girin veya bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="55314-115">In the Item group field, enter or select a value.</span></span>
    * <span data-ttu-id="55314-116">Örneğin, Ses'i seçin.</span><span class="sxs-lookup"><span data-stu-id="55314-116">For example, select Audio.</span></span> <span data-ttu-id="55314-117">Bunun, maliyet hesaplamaları üzerinde hiçbir etkisi yoktur.</span><span class="sxs-lookup"><span data-stu-id="55314-117">This has no impact on cost calculations.</span></span>  
6. <span data-ttu-id="55314-118">Stok boyutu grubu alanına bir değer girin veya bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="55314-118">In the Storage dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="55314-119">SiteWH'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="55314-119">Select SiteWH.</span></span> <span data-ttu-id="55314-120">Tanıtım için yalnızca Tesis ve Ambar kullanılır.</span><span class="sxs-lookup"><span data-stu-id="55314-120">Only Site and Warehouse will be used for the demonstration.</span></span>  
7. <span data-ttu-id="55314-121">İzleme boyutu grubu alanına bir değer girin veya bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="55314-121">In the Tracking dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="55314-122">Bu örnek için izleme boyutları kullanılmaz.</span><span class="sxs-lookup"><span data-stu-id="55314-122">Tracking dimensions will not be used for this example.</span></span> <span data-ttu-id="55314-123">Hiçbiri'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="55314-123">Select None.</span></span>  
8. <span data-ttu-id="55314-124">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="55314-124">Click OK.</span></span>
9. <span data-ttu-id="55314-125">Eylem Bölmesinde, Stok yönetimi'ne tıklayın.</span><span class="sxs-lookup"><span data-stu-id="55314-125">On the Action Pane, click Manage inventory.</span></span>
10. <span data-ttu-id="55314-126">Varsayılan sipariş ayarlarına tıklayın.</span><span class="sxs-lookup"><span data-stu-id="55314-126">Click Default order settings.</span></span>
11. <span data-ttu-id="55314-127">Satınalma tesisi alanına bir değer girin veya buradan bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="55314-127">In the Purchase site field, enter or select a value.</span></span>
    * <span data-ttu-id="55314-128">Bu örnek için, Tesis 1'i seçin.</span><span class="sxs-lookup"><span data-stu-id="55314-128">For this example, select Site 1.</span></span>  
12. <span data-ttu-id="55314-129">Stok tesisi alanına bir değer girin veya buradan bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="55314-129">In the Inventory site field, enter or select a value.</span></span>
    * <span data-ttu-id="55314-130">Bu örnek için, Tesis 1'i seçin.</span><span class="sxs-lookup"><span data-stu-id="55314-130">For this example, select Site 1.</span></span>  
13. <span data-ttu-id="55314-131">Satış tesisi alanına bir değer girin veya buradan bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="55314-131">In the Sales site field, enter or select a value.</span></span>
    * <span data-ttu-id="55314-132">Bu örnek için, Tesis 1'i seçin.</span><span class="sxs-lookup"><span data-stu-id="55314-132">For this example, select Site 1.</span></span>  
14. <span data-ttu-id="55314-133">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="55314-133">Close the page.</span></span>
15. <span data-ttu-id="55314-134">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="55314-134">Close the page.</span></span>
16. <span data-ttu-id="55314-135">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="55314-135">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="55314-136">ITEM_A öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="55314-136">Click ITEM_A.</span></span>  
17. <span data-ttu-id="55314-137">Maliyetleri yönet bölümünü genişletin.</span><span class="sxs-lookup"><span data-stu-id="55314-137">Expand the Manage costs section.</span></span>
18. <span data-ttu-id="55314-138">Maliyet grubu alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="55314-138">In the Cost group field, type a value.</span></span>
    * <span data-ttu-id="55314-139">Bu örnek için M2 yazın.</span><span class="sxs-lookup"><span data-stu-id="55314-139">For this example, type M2.</span></span>  
19. <span data-ttu-id="55314-140">Eylem Bölmesinde Yönet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="55314-140">On the Action Pane, click Manage costs.</span></span>
20. <span data-ttu-id="55314-141">Madde fiyatı'na tıklayın.</span><span class="sxs-lookup"><span data-stu-id="55314-141">Click Item price.</span></span>
21. <span data-ttu-id="55314-142">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="55314-142">Click New.</span></span>
22. <span data-ttu-id="55314-143">Sürüm alanına bir değer girin veya buradan bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="55314-143">In the Version field, enter or select a value.</span></span>
    * <span data-ttu-id="55314-144">Bu örnek için, Standart maliyet maliyetlendirme türü olan 10'u seçin.</span><span class="sxs-lookup"><span data-stu-id="55314-144">For this example, select 10, which is the Standard cost costing type.</span></span>  
23. <span data-ttu-id="55314-145">Tesis alanına bir değer girin veya buradan bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="55314-145">In the Site field, enter or select a value.</span></span>
    * <span data-ttu-id="55314-146">Bu örnek için, Tesis 1'i seçin.</span><span class="sxs-lookup"><span data-stu-id="55314-146">For this example, select Site 1.</span></span>  
24. <span data-ttu-id="55314-147">Fiyat alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="55314-147">In the Price field, enter a number.</span></span>
    * <span data-ttu-id="55314-148">Bu örnek için, 10 yazın.</span><span class="sxs-lookup"><span data-stu-id="55314-148">For this example, type 10.</span></span>  
25. <span data-ttu-id="55314-149">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="55314-149">Click Save.</span></span>
26. <span data-ttu-id="55314-150">Beklemedeki fiyatı/fiyatları etkinleştir'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="55314-150">Click Activate pending price(s).</span></span>
27. <span data-ttu-id="55314-151">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="55314-151">Close the page.</span></span>
28. <span data-ttu-id="55314-152">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="55314-152">Close the page.</span></span>

## <a name="create-the-second-material"></a><span data-ttu-id="55314-153">İkinci malzemeyi oluşturma</span><span class="sxs-lookup"><span data-stu-id="55314-153">Create the second material</span></span>
1. <span data-ttu-id="55314-154">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="55314-154">Click New.</span></span>
2. <span data-ttu-id="55314-155">Ürün numarası alanında bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="55314-155">In the Product number field, type a value.</span></span>
    * <span data-ttu-id="55314-156">Bu örnek için, ITEM_B yazın.</span><span class="sxs-lookup"><span data-stu-id="55314-156">For this example, type ITEM_B.</span></span>  
3. <span data-ttu-id="55314-157">Model grubu alanına bir değer girin veya bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="55314-157">In the Item model group field, enter or select a value.</span></span>
    * <span data-ttu-id="55314-158">STD öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="55314-158">Select STD.</span></span> <span data-ttu-id="55314-159">STD, standart maliyet anlamına gelir ve maliyet hesaplamalarıyla çalışırken en yaygın olarak kullanılan modeldir.</span><span class="sxs-lookup"><span data-stu-id="55314-159">STD stands for standard cost and is the most commonly used model when working with cost calculations.</span></span>  
4. <span data-ttu-id="55314-160">Ürün grubu alanında bir değer girin veya bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="55314-160">In the Item group field, enter or select a value.</span></span>
    * <span data-ttu-id="55314-161">Örneğin, Ses'i seçin.</span><span class="sxs-lookup"><span data-stu-id="55314-161">For example, select Audio.</span></span> <span data-ttu-id="55314-162">Bunun, maliyet hesaplamaları üzerinde hiçbir etkisi yoktur.</span><span class="sxs-lookup"><span data-stu-id="55314-162">This has no impact on cost calculations.</span></span>  
5. <span data-ttu-id="55314-163">Stok boyutu grubu alanına bir değer girin veya bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="55314-163">In the Storage dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="55314-164">SiteWH'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="55314-164">Select SiteWH.</span></span> <span data-ttu-id="55314-165">Bu örnek için yalnızca Tesis ve Ambar kullanılır.</span><span class="sxs-lookup"><span data-stu-id="55314-165">Only Site and Warehouse will be used for this example.</span></span>  
6. <span data-ttu-id="55314-166">İzleme boyutu grubu alanına bir değer girin veya bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="55314-166">In the Tracking dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="55314-167">Bu örnek için izleme boyutları kullanılmaz.</span><span class="sxs-lookup"><span data-stu-id="55314-167">Tracking dimensions will not be used for this example.</span></span> <span data-ttu-id="55314-168">Hiçbiri'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="55314-168">Select None.</span></span>  
7. <span data-ttu-id="55314-169">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="55314-169">Click OK.</span></span>
8. <span data-ttu-id="55314-170">Eylem Bölmesinde, Stok yönetimi'ne tıklayın.</span><span class="sxs-lookup"><span data-stu-id="55314-170">On the Action Pane, click Manage inventory.</span></span>
9. <span data-ttu-id="55314-171">Varsayılan sipariş ayarlarına tıklayın.</span><span class="sxs-lookup"><span data-stu-id="55314-171">Click Default order settings.</span></span>
10. <span data-ttu-id="55314-172">Satınalma tesisi alanına bir değer girin veya buradan bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="55314-172">In the Purchase site field, enter or select a value.</span></span>
    * <span data-ttu-id="55314-173">Bu örnek için, Tesis 1'i seçin.</span><span class="sxs-lookup"><span data-stu-id="55314-173">For this example, select Site 1.</span></span>  
11. <span data-ttu-id="55314-174">Stok tesisi alanına bir değer girin veya buradan bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="55314-174">In the Inventory site field, enter or select a value.</span></span>
    * <span data-ttu-id="55314-175">Bu örnek için, Tesis 1'i seçin.</span><span class="sxs-lookup"><span data-stu-id="55314-175">For this example, select Site 1.</span></span>  
12. <span data-ttu-id="55314-176">Satış tesisi alanına bir değer girin veya buradan bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="55314-176">In the Sales site field, enter or select a value.</span></span>
    * <span data-ttu-id="55314-177">Bu örnek için, Tesis 1'i seçin.</span><span class="sxs-lookup"><span data-stu-id="55314-177">For this example, select Site 1.</span></span>  
13. <span data-ttu-id="55314-178">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="55314-178">Close the page.</span></span>
14. <span data-ttu-id="55314-179">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="55314-179">Close the page.</span></span>
15. <span data-ttu-id="55314-180">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="55314-180">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="55314-181">ITEM_B öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="55314-181">Click ITEM_B.</span></span>  
16. <span data-ttu-id="55314-182">Maliyetleri yönet bölümünü genişletin.</span><span class="sxs-lookup"><span data-stu-id="55314-182">Expand the Manage costs section.</span></span>
17. <span data-ttu-id="55314-183">Maliyet grubu alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="55314-183">In the Cost group field, type a value.</span></span>
    * <span data-ttu-id="55314-184">Bu örnek için M2 yazın.</span><span class="sxs-lookup"><span data-stu-id="55314-184">For this example, type M2.</span></span>  
18. <span data-ttu-id="55314-185">Eylem Bölmesinde Yönet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="55314-185">On the Action Pane, click Manage costs.</span></span>
19. <span data-ttu-id="55314-186">Madde fiyatı'na tıklayın.</span><span class="sxs-lookup"><span data-stu-id="55314-186">Click Item price.</span></span>
20. <span data-ttu-id="55314-187">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="55314-187">Click New.</span></span>
21. <span data-ttu-id="55314-188">Sürüm alanına bir değer girin veya buradan bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="55314-188">In the Version field, enter or select a value.</span></span>
    * <span data-ttu-id="55314-189">Bu örnek için, 10'u seçin.</span><span class="sxs-lookup"><span data-stu-id="55314-189">For this example, select 10.</span></span> <span data-ttu-id="55314-190">Bu, Standart maliyet maliyetlendirme türüdür.</span><span class="sxs-lookup"><span data-stu-id="55314-190">This is the Standard cost costing type.</span></span>  
22. <span data-ttu-id="55314-191">Tesis alanına bir değer girin veya buradan bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="55314-191">In the Site field, enter or select a value.</span></span>
    * <span data-ttu-id="55314-192">Bu örnek için, Tesis 1'i seçin.</span><span class="sxs-lookup"><span data-stu-id="55314-192">For this example, select Site 1.</span></span>  
23. <span data-ttu-id="55314-193">Fiyat alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="55314-193">In the Price field, enter a number.</span></span>
    * <span data-ttu-id="55314-194">Tanıtım için, 10 yazın.</span><span class="sxs-lookup"><span data-stu-id="55314-194">For the demonstration, type 10.</span></span>  
24. <span data-ttu-id="55314-195">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="55314-195">Click Save.</span></span>
25. <span data-ttu-id="55314-196">Beklemedeki fiyatı/fiyatları etkinleştir'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="55314-196">Click Activate pending price(s).</span></span>
26. <span data-ttu-id="55314-197">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="55314-197">Close the page.</span></span>
27. <span data-ttu-id="55314-198">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="55314-198">Close the page.</span></span>

## <a name="create-the-third-material"></a><span data-ttu-id="55314-199">Üçüncü malzemeyi oluşturma</span><span class="sxs-lookup"><span data-stu-id="55314-199">Create the third material</span></span>
1. <span data-ttu-id="55314-200">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="55314-200">Click New.</span></span>
2. <span data-ttu-id="55314-201">Ürün numarası alanında bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="55314-201">In the Product number field, type a value.</span></span>
    * <span data-ttu-id="55314-202">Tanıtım için, ITEM_C yazın.</span><span class="sxs-lookup"><span data-stu-id="55314-202">For the demonstration, type ITEM_C</span></span>  
3. <span data-ttu-id="55314-203">Model grubu alanına bir değer girin veya bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="55314-203">In the Item model group field, enter or select a value.</span></span>
    * <span data-ttu-id="55314-204">STD öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="55314-204">Select STD.</span></span> <span data-ttu-id="55314-205">STD, standart maliyet anlamına gelir ve maliyet hesaplamalarıyla çalışırken en yaygın olarak kullanılan modeldir.</span><span class="sxs-lookup"><span data-stu-id="55314-205">STD stands for standard cost and is the most commonly used model when working with cost calculations.</span></span>  
4. <span data-ttu-id="55314-206">Ürün grubu alanında bir değer girin veya bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="55314-206">In the Item group field, enter or select a value.</span></span>
    * <span data-ttu-id="55314-207">Örneğin, Ses'i seçin.</span><span class="sxs-lookup"><span data-stu-id="55314-207">For example, select Audio.</span></span> <span data-ttu-id="55314-208">Bunun, maliyet hesaplamaları üzerinde hiçbir etkisi yoktur.</span><span class="sxs-lookup"><span data-stu-id="55314-208">This has no impact on cost calculations.</span></span>  
5. <span data-ttu-id="55314-209">Stok boyutu grubu alanına bir değer girin veya bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="55314-209">In the Storage dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="55314-210">SiteWH'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="55314-210">Select SiteWH.</span></span> <span data-ttu-id="55314-211">Tanıtım için yalnızca Tesis ve Ambar kullanılır.</span><span class="sxs-lookup"><span data-stu-id="55314-211">Only Site and Warehouse will be used for the demonstration.</span></span>  
6. <span data-ttu-id="55314-212">İzleme boyutu grubu alanına bir değer girin veya bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="55314-212">In the Tracking dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="55314-213">Bu örnek için izleme boyutları kullanılmaz.</span><span class="sxs-lookup"><span data-stu-id="55314-213">Tracking dimensions will not be used for this example.</span></span> <span data-ttu-id="55314-214">Hiçbiri'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="55314-214">Select None.</span></span>  
7. <span data-ttu-id="55314-215">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="55314-215">Click OK.</span></span>
8. <span data-ttu-id="55314-216">Eylem Bölmesinde, Stok yönetimi'ne tıklayın.</span><span class="sxs-lookup"><span data-stu-id="55314-216">On the Action Pane, click Manage inventory.</span></span>
9. <span data-ttu-id="55314-217">Varsayılan sipariş ayarlarına tıklayın.</span><span class="sxs-lookup"><span data-stu-id="55314-217">Click Default order settings.</span></span>
10. <span data-ttu-id="55314-218">Satınalma tesisi alanına bir değer girin veya buradan bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="55314-218">In the Purchase site field, enter or select a value.</span></span>
    * <span data-ttu-id="55314-219">Bu örnek için, Tesis 1'i seçin.</span><span class="sxs-lookup"><span data-stu-id="55314-219">For this example, select Site 1.</span></span>  
11. <span data-ttu-id="55314-220">Stok tesisi alanına bir değer girin veya buradan bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="55314-220">In the Inventory site field, enter or select a value.</span></span>
    * <span data-ttu-id="55314-221">Bu örnek için, Tesis 1'i seçin.</span><span class="sxs-lookup"><span data-stu-id="55314-221">For this example, select Site 1.</span></span>  
12. <span data-ttu-id="55314-222">Satış tesisi alanına bir değer girin veya buradan bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="55314-222">In the Sales site field, enter or select a value.</span></span>
    * <span data-ttu-id="55314-223">Bu örnek için, Tesis 1'i seçin.</span><span class="sxs-lookup"><span data-stu-id="55314-223">For this example, select Site 1.</span></span>  
13. <span data-ttu-id="55314-224">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="55314-224">Close the page.</span></span>
14. <span data-ttu-id="55314-225">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="55314-225">Close the page.</span></span>
15. <span data-ttu-id="55314-226">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="55314-226">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="55314-227">ITEM_C öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="55314-227">Click ITEM_C.</span></span>  
16. <span data-ttu-id="55314-228">Maliyetleri yönet bölümünü genişletin.</span><span class="sxs-lookup"><span data-stu-id="55314-228">Expand the Manage costs section.</span></span>
17. <span data-ttu-id="55314-229">Maliyet grubu alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="55314-229">In the Cost group field, type a value.</span></span>
    * <span data-ttu-id="55314-230">Bu örnek için M1 yazın.</span><span class="sxs-lookup"><span data-stu-id="55314-230">For this example, type M1.</span></span>  
18. <span data-ttu-id="55314-231">Eylem Bölmesinde Yönet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="55314-231">On the Action Pane, click Manage costs.</span></span>
19. <span data-ttu-id="55314-232">Madde fiyatı'na tıklayın.</span><span class="sxs-lookup"><span data-stu-id="55314-232">Click Item price.</span></span>
20. <span data-ttu-id="55314-233">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="55314-233">Click New.</span></span>
21. <span data-ttu-id="55314-234">Sürüm alanına bir değer girin veya buradan bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="55314-234">In the Version field, enter or select a value.</span></span>
    * <span data-ttu-id="55314-235">Bu örnek için, 10'u seçin.</span><span class="sxs-lookup"><span data-stu-id="55314-235">For this example, select 10.</span></span> <span data-ttu-id="55314-236">Bu, Standart maliyet maliyetlendirme türüdür.</span><span class="sxs-lookup"><span data-stu-id="55314-236">This is the Standard cost costing type.</span></span>  
22. <span data-ttu-id="55314-237">Tesis alanına bir değer girin veya buradan bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="55314-237">In the Site field, enter or select a value.</span></span>
    * <span data-ttu-id="55314-238">Bu örnek için, Tesis 1'i seçin.</span><span class="sxs-lookup"><span data-stu-id="55314-238">For this example, select Site 1.</span></span>  
23. <span data-ttu-id="55314-239">Fiyat alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="55314-239">In the Price field, enter a number.</span></span>
    * <span data-ttu-id="55314-240">Bu örnek için, 10 yazın.</span><span class="sxs-lookup"><span data-stu-id="55314-240">For this example, type 10.</span></span>  
24. <span data-ttu-id="55314-241">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="55314-241">Click Save.</span></span>
25. <span data-ttu-id="55314-242">Beklemedeki fiyatı/fiyatları etkinleştir'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="55314-242">Click Activate pending price(s).</span></span>
26. <span data-ttu-id="55314-243">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="55314-243">Close the page.</span></span>
27. <span data-ttu-id="55314-244">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="55314-244">Close the page.</span></span>

