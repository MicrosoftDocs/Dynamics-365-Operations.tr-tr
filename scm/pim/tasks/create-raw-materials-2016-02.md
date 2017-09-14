--- 
title: "Hammadde oluşturma (yalnızca Şubat 2016)"
description: "Bu görev, bitmiş ve yarı mamul ürünlerin bileşenlerini oluşturmaya odaklanır."
author: YuyuScheller
manager: AnnBe
ms.date: 02/07/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: Operations
ms.search.region: Global
ms.author: bis
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 6dd2aa1ebc713287120106a9d1ec7dc15c24def9
ms.openlocfilehash: f6af7b93d8d1d9a6f7474f24177b16e5295e90d6
ms.contentlocale: tr-tr
ms.lasthandoff: 09/14/2017

---
# <a name="create-raw-materials-february-2016-only"></a><span data-ttu-id="479c1-103">Hammadde oluşturma (yalnızca Şubat 2016)</span><span class="sxs-lookup"><span data-stu-id="479c1-103">Create raw materials (February 2016 only)</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="479c1-104">Bu görev, bitmiş ve yarı mamul ürünlerin bileşenlerini oluşturmaya odaklanır.</span><span class="sxs-lookup"><span data-stu-id="479c1-104">This task focuses on creating the components of finished and semi-finished products.</span></span> <span data-ttu-id="479c1-105">Ürün Reçetesi hesaplama serisindeki üçüncü görevdir.</span><span class="sxs-lookup"><span data-stu-id="479c1-105">It is the third task in the BOM calculation series.</span></span> <span data-ttu-id="479c1-106">Bu görevi oluşturmak için kullanılan demo veri şirketi USMF'dir.</span><span class="sxs-lookup"><span data-stu-id="479c1-106">The demo data company used to create this task is USMF.</span></span>


## <a name="create-the-first-material"></a><span data-ttu-id="479c1-107">İlk malzemeyi oluşturma</span><span class="sxs-lookup"><span data-stu-id="479c1-107">Create the first material</span></span>
1. <span data-ttu-id="479c1-108">Product information management > Products > Released products (Ürün bilgi yönetimi > Ürünler > Piyasaya sürülmüş ürünler) menüsüne gidin.</span><span class="sxs-lookup"><span data-stu-id="479c1-108">Go to Product information management > Products > Released products.</span></span>
2. <span data-ttu-id="479c1-109">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="479c1-109">Click New.</span></span>
3. <span data-ttu-id="479c1-110">Ürün numarası alanında bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="479c1-110">In the Product number field, type a value.</span></span>
    * <span data-ttu-id="479c1-111">Bu örnek için, ITEM_A girin.</span><span class="sxs-lookup"><span data-stu-id="479c1-111">For this example, enter ITEM_A.</span></span>  
4. <span data-ttu-id="479c1-112">Model grubu alanına bir değer girin veya bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="479c1-112">In the Item model group field, enter or select a value.</span></span>
    * <span data-ttu-id="479c1-113">STD öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="479c1-113">Select STD.</span></span> <span data-ttu-id="479c1-114">STD, standart maliyet anlamına gelir ve maliyet hesaplamalarıyla çalışırken en yaygın olarak kullanılan modeldir.</span><span class="sxs-lookup"><span data-stu-id="479c1-114">STD stands for standard cost and is the most commonly used model when working with cost calculations.</span></span>  
5. <span data-ttu-id="479c1-115">Ürün grubu alanında bir değer girin veya bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="479c1-115">In the Item group field, enter or select a value.</span></span>
    * <span data-ttu-id="479c1-116">Örneğin, Ses'i seçin.</span><span class="sxs-lookup"><span data-stu-id="479c1-116">For example, select Audio.</span></span> <span data-ttu-id="479c1-117">Bunun, maliyet hesaplamaları üzerinde hiçbir etkisi yoktur.</span><span class="sxs-lookup"><span data-stu-id="479c1-117">This has no impact on cost calculations.</span></span>  
6. <span data-ttu-id="479c1-118">Stok boyutu grubu alanına bir değer girin veya bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="479c1-118">In the Storage dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="479c1-119">SiteWH'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="479c1-119">Select SiteWH.</span></span> <span data-ttu-id="479c1-120">Tanıtım için yalnızca Tesis ve Ambar kullanılır.</span><span class="sxs-lookup"><span data-stu-id="479c1-120">Only Site and Warehouse will be used for the demonstration.</span></span>  
7. <span data-ttu-id="479c1-121">İzleme boyutu grubu alanına bir değer girin veya bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="479c1-121">In the Tracking dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="479c1-122">Bu örnek için izleme boyutları kullanılmaz.</span><span class="sxs-lookup"><span data-stu-id="479c1-122">Tracking dimensions will not be used for this example.</span></span> <span data-ttu-id="479c1-123">Hiçbiri'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="479c1-123">Select None.</span></span>  
8. <span data-ttu-id="479c1-124">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="479c1-124">Click OK.</span></span>
9. <span data-ttu-id="479c1-125">Eylem Bölmesinde, Stok yönetimi'ne tıklayın.</span><span class="sxs-lookup"><span data-stu-id="479c1-125">On the Action Pane, click Manage inventory.</span></span>
10. <span data-ttu-id="479c1-126">Varsayılan sipariş ayarlarına tıklayın.</span><span class="sxs-lookup"><span data-stu-id="479c1-126">Click Default order settings.</span></span>
11. <span data-ttu-id="479c1-127">Satınalma tesisi alanına bir değer girin veya buradan bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="479c1-127">In the Purchase site field, enter or select a value.</span></span>
    * <span data-ttu-id="479c1-128">Bu örnek için, Tesis 1'i seçin.</span><span class="sxs-lookup"><span data-stu-id="479c1-128">For this example, select Site 1.</span></span>  
12. <span data-ttu-id="479c1-129">Stok tesisi alanına bir değer girin veya buradan bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="479c1-129">In the Inventory site field, enter or select a value.</span></span>
    * <span data-ttu-id="479c1-130">Bu örnek için, Tesis 1'i seçin.</span><span class="sxs-lookup"><span data-stu-id="479c1-130">For this example, select Site 1.</span></span>  
13. <span data-ttu-id="479c1-131">Satış tesisi alanına bir değer girin veya buradan bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="479c1-131">In the Sales site field, enter or select a value.</span></span>
    * <span data-ttu-id="479c1-132">Bu örnek için, Tesis 1'i seçin.</span><span class="sxs-lookup"><span data-stu-id="479c1-132">For this example, select Site 1.</span></span>  
14. <span data-ttu-id="479c1-133">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="479c1-133">Close the page.</span></span>
15. <span data-ttu-id="479c1-134">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="479c1-134">Close the page.</span></span>
16. <span data-ttu-id="479c1-135">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="479c1-135">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="479c1-136">ITEM_A öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="479c1-136">Click ITEM_A.</span></span>  
17. <span data-ttu-id="479c1-137">Maliyetleri yönet bölümünü genişletin.</span><span class="sxs-lookup"><span data-stu-id="479c1-137">Expand the Manage costs section.</span></span>
18. <span data-ttu-id="479c1-138">Maliyet grubu alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="479c1-138">In the Cost group field, type a value.</span></span>
    * <span data-ttu-id="479c1-139">Bu örnek için M2 yazın.</span><span class="sxs-lookup"><span data-stu-id="479c1-139">For this example, type M2.</span></span>  
19. <span data-ttu-id="479c1-140">Eylem Bölmesinde Yönet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="479c1-140">On the Action Pane, click Manage costs.</span></span>
20. <span data-ttu-id="479c1-141">Madde fiyatı'na tıklayın.</span><span class="sxs-lookup"><span data-stu-id="479c1-141">Click Item price.</span></span>
21. <span data-ttu-id="479c1-142">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="479c1-142">Click New.</span></span>
22. <span data-ttu-id="479c1-143">Sürüm alanına bir değer girin veya buradan bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="479c1-143">In the Version field, enter or select a value.</span></span>
    * <span data-ttu-id="479c1-144">Bu örnek için, Standart maliyet maliyetlendirme türü olan 10'u seçin.</span><span class="sxs-lookup"><span data-stu-id="479c1-144">For this example, select 10, which is the Standard cost costing type.</span></span>  
23. <span data-ttu-id="479c1-145">Tesis alanına bir değer girin veya buradan bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="479c1-145">In the Site field, enter or select a value.</span></span>
    * <span data-ttu-id="479c1-146">Bu örnek için, Tesis 1'i seçin.</span><span class="sxs-lookup"><span data-stu-id="479c1-146">For this example, select Site 1.</span></span>  
24. <span data-ttu-id="479c1-147">Fiyat alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="479c1-147">In the Price field, enter a number.</span></span>
    * <span data-ttu-id="479c1-148">Bu örnek için, 10 yazın.</span><span class="sxs-lookup"><span data-stu-id="479c1-148">For this example, type 10.</span></span>  
25. <span data-ttu-id="479c1-149">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="479c1-149">Click Save.</span></span>
26. <span data-ttu-id="479c1-150">Beklemedeki fiyatı/fiyatları etkinleştir'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="479c1-150">Click Activate pending price(s).</span></span>
27. <span data-ttu-id="479c1-151">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="479c1-151">Close the page.</span></span>
28. <span data-ttu-id="479c1-152">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="479c1-152">Close the page.</span></span>

## <a name="create-the-second-material"></a><span data-ttu-id="479c1-153">İkinci malzemeyi oluşturma</span><span class="sxs-lookup"><span data-stu-id="479c1-153">Create the second material</span></span>
1. <span data-ttu-id="479c1-154">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="479c1-154">Click New.</span></span>
2. <span data-ttu-id="479c1-155">Ürün numarası alanında bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="479c1-155">In the Product number field, type a value.</span></span>
    * <span data-ttu-id="479c1-156">Bu örnek için, ITEM_B yazın.</span><span class="sxs-lookup"><span data-stu-id="479c1-156">For this example, type ITEM_B.</span></span>  
3. <span data-ttu-id="479c1-157">Model grubu alanına bir değer girin veya bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="479c1-157">In the Item model group field, enter or select a value.</span></span>
    * <span data-ttu-id="479c1-158">STD öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="479c1-158">Select STD.</span></span> <span data-ttu-id="479c1-159">STD, standart maliyet anlamına gelir ve maliyet hesaplamalarıyla çalışırken en yaygın olarak kullanılan modeldir.</span><span class="sxs-lookup"><span data-stu-id="479c1-159">STD stands for standard cost and is the most commonly used model when working with cost calculations.</span></span>  
4. <span data-ttu-id="479c1-160">Ürün grubu alanında bir değer girin veya bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="479c1-160">In the Item group field, enter or select a value.</span></span>
    * <span data-ttu-id="479c1-161">Örneğin, Ses'i seçin.</span><span class="sxs-lookup"><span data-stu-id="479c1-161">For example, select Audio.</span></span> <span data-ttu-id="479c1-162">Bunun, maliyet hesaplamaları üzerinde hiçbir etkisi yoktur.</span><span class="sxs-lookup"><span data-stu-id="479c1-162">This has no impact on cost calculations.</span></span>  
5. <span data-ttu-id="479c1-163">Stok boyutu grubu alanına bir değer girin veya bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="479c1-163">In the Storage dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="479c1-164">SiteWH'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="479c1-164">Select SiteWH.</span></span> <span data-ttu-id="479c1-165">Bu örnek için yalnızca Tesis ve Ambar kullanılır.</span><span class="sxs-lookup"><span data-stu-id="479c1-165">Only Site and Warehouse will be used for this example.</span></span>  
6. <span data-ttu-id="479c1-166">İzleme boyutu grubu alanına bir değer girin veya bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="479c1-166">In the Tracking dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="479c1-167">Bu örnek için izleme boyutları kullanılmaz.</span><span class="sxs-lookup"><span data-stu-id="479c1-167">Tracking dimensions will not be used for this example.</span></span> <span data-ttu-id="479c1-168">Hiçbiri'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="479c1-168">Select None.</span></span>  
7. <span data-ttu-id="479c1-169">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="479c1-169">Click OK.</span></span>
8. <span data-ttu-id="479c1-170">Eylem Bölmesinde, Stok yönetimi'ne tıklayın.</span><span class="sxs-lookup"><span data-stu-id="479c1-170">On the Action Pane, click Manage inventory.</span></span>
9. <span data-ttu-id="479c1-171">Varsayılan sipariş ayarlarına tıklayın.</span><span class="sxs-lookup"><span data-stu-id="479c1-171">Click Default order settings.</span></span>
10. <span data-ttu-id="479c1-172">Satınalma tesisi alanına bir değer girin veya buradan bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="479c1-172">In the Purchase site field, enter or select a value.</span></span>
    * <span data-ttu-id="479c1-173">Bu örnek için, Tesis 1'i seçin.</span><span class="sxs-lookup"><span data-stu-id="479c1-173">For this example, select Site 1.</span></span>  
11. <span data-ttu-id="479c1-174">Stok tesisi alanına bir değer girin veya buradan bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="479c1-174">In the Inventory site field, enter or select a value.</span></span>
    * <span data-ttu-id="479c1-175">Bu örnek için, Tesis 1'i seçin.</span><span class="sxs-lookup"><span data-stu-id="479c1-175">For this example, select Site 1.</span></span>  
12. <span data-ttu-id="479c1-176">Satış tesisi alanına bir değer girin veya buradan bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="479c1-176">In the Sales site field, enter or select a value.</span></span>
    * <span data-ttu-id="479c1-177">Bu örnek için, Tesis 1'i seçin.</span><span class="sxs-lookup"><span data-stu-id="479c1-177">For this example, select Site 1.</span></span>  
13. <span data-ttu-id="479c1-178">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="479c1-178">Close the page.</span></span>
14. <span data-ttu-id="479c1-179">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="479c1-179">Close the page.</span></span>
15. <span data-ttu-id="479c1-180">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="479c1-180">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="479c1-181">ITEM_B öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="479c1-181">Click ITEM_B.</span></span>  
16. <span data-ttu-id="479c1-182">Maliyetleri yönet bölümünü genişletin.</span><span class="sxs-lookup"><span data-stu-id="479c1-182">Expand the Manage costs section.</span></span>
17. <span data-ttu-id="479c1-183">Maliyet grubu alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="479c1-183">In the Cost group field, type a value.</span></span>
    * <span data-ttu-id="479c1-184">Bu örnek için M2 yazın.</span><span class="sxs-lookup"><span data-stu-id="479c1-184">For this example, type M2.</span></span>  
18. <span data-ttu-id="479c1-185">Eylem Bölmesinde Yönet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="479c1-185">On the Action Pane, click Manage costs.</span></span>
19. <span data-ttu-id="479c1-186">Madde fiyatı'na tıklayın.</span><span class="sxs-lookup"><span data-stu-id="479c1-186">Click Item price.</span></span>
20. <span data-ttu-id="479c1-187">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="479c1-187">Click New.</span></span>
21. <span data-ttu-id="479c1-188">Sürüm alanına bir değer girin veya buradan bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="479c1-188">In the Version field, enter or select a value.</span></span>
    * <span data-ttu-id="479c1-189">Bu örnek için, 10'u seçin.</span><span class="sxs-lookup"><span data-stu-id="479c1-189">For this example, select 10.</span></span> <span data-ttu-id="479c1-190">Bu, Standart maliyet maliyetlendirme türüdür.</span><span class="sxs-lookup"><span data-stu-id="479c1-190">This is the Standard cost costing type.</span></span>  
22. <span data-ttu-id="479c1-191">Tesis alanına bir değer girin veya buradan bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="479c1-191">In the Site field, enter or select a value.</span></span>
    * <span data-ttu-id="479c1-192">Bu örnek için, Tesis 1'i seçin.</span><span class="sxs-lookup"><span data-stu-id="479c1-192">For this example, select Site 1.</span></span>  
23. <span data-ttu-id="479c1-193">Fiyat alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="479c1-193">In the Price field, enter a number.</span></span>
    * <span data-ttu-id="479c1-194">Tanıtım için, 10 yazın.</span><span class="sxs-lookup"><span data-stu-id="479c1-194">For the demonstration, type 10.</span></span>  
24. <span data-ttu-id="479c1-195">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="479c1-195">Click Save.</span></span>
25. <span data-ttu-id="479c1-196">Beklemedeki fiyatı/fiyatları etkinleştir'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="479c1-196">Click Activate pending price(s).</span></span>
26. <span data-ttu-id="479c1-197">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="479c1-197">Close the page.</span></span>
27. <span data-ttu-id="479c1-198">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="479c1-198">Close the page.</span></span>

## <a name="create-the-third-material"></a><span data-ttu-id="479c1-199">Üçüncü malzemeyi oluşturma</span><span class="sxs-lookup"><span data-stu-id="479c1-199">Create the third material</span></span>
1. <span data-ttu-id="479c1-200">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="479c1-200">Click New.</span></span>
2. <span data-ttu-id="479c1-201">Ürün numarası alanında bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="479c1-201">In the Product number field, type a value.</span></span>
    * <span data-ttu-id="479c1-202">Tanıtım için, ITEM_C yazın.</span><span class="sxs-lookup"><span data-stu-id="479c1-202">For the demonstration, type ITEM_C</span></span>  
3. <span data-ttu-id="479c1-203">Model grubu alanına bir değer girin veya bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="479c1-203">In the Item model group field, enter or select a value.</span></span>
    * <span data-ttu-id="479c1-204">STD öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="479c1-204">Select STD.</span></span> <span data-ttu-id="479c1-205">STD, standart maliyet anlamına gelir ve maliyet hesaplamalarıyla çalışırken en yaygın olarak kullanılan modeldir.</span><span class="sxs-lookup"><span data-stu-id="479c1-205">STD stands for standard cost and is the most commonly used model when working with cost calculations.</span></span>  
4. <span data-ttu-id="479c1-206">Ürün grubu alanında bir değer girin veya bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="479c1-206">In the Item group field, enter or select a value.</span></span>
    * <span data-ttu-id="479c1-207">Örneğin, Ses'i seçin.</span><span class="sxs-lookup"><span data-stu-id="479c1-207">For example, select Audio.</span></span> <span data-ttu-id="479c1-208">Bunun, maliyet hesaplamaları üzerinde hiçbir etkisi yoktur.</span><span class="sxs-lookup"><span data-stu-id="479c1-208">This has no impact on cost calculations.</span></span>  
5. <span data-ttu-id="479c1-209">Stok boyutu grubu alanına bir değer girin veya bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="479c1-209">In the Storage dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="479c1-210">SiteWH'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="479c1-210">Select SiteWH.</span></span> <span data-ttu-id="479c1-211">Tanıtım için yalnızca Tesis ve Ambar kullanılır.</span><span class="sxs-lookup"><span data-stu-id="479c1-211">Only Site and Warehouse will be used for the demonstration.</span></span>  
6. <span data-ttu-id="479c1-212">İzleme boyutu grubu alanına bir değer girin veya bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="479c1-212">In the Tracking dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="479c1-213">Bu örnek için izleme boyutları kullanılmaz.</span><span class="sxs-lookup"><span data-stu-id="479c1-213">Tracking dimensions will not be used for this example.</span></span> <span data-ttu-id="479c1-214">Hiçbiri'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="479c1-214">Select None.</span></span>  
7. <span data-ttu-id="479c1-215">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="479c1-215">Click OK.</span></span>
8. <span data-ttu-id="479c1-216">Eylem Bölmesinde, Stok yönetimi'ne tıklayın.</span><span class="sxs-lookup"><span data-stu-id="479c1-216">On the Action Pane, click Manage inventory.</span></span>
9. <span data-ttu-id="479c1-217">Varsayılan sipariş ayarlarına tıklayın.</span><span class="sxs-lookup"><span data-stu-id="479c1-217">Click Default order settings.</span></span>
10. <span data-ttu-id="479c1-218">Satınalma tesisi alanına bir değer girin veya buradan bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="479c1-218">In the Purchase site field, enter or select a value.</span></span>
    * <span data-ttu-id="479c1-219">Bu örnek için, Tesis 1'i seçin.</span><span class="sxs-lookup"><span data-stu-id="479c1-219">For this example, select Site 1.</span></span>  
11. <span data-ttu-id="479c1-220">Stok tesisi alanına bir değer girin veya buradan bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="479c1-220">In the Inventory site field, enter or select a value.</span></span>
    * <span data-ttu-id="479c1-221">Bu örnek için, Tesis 1'i seçin.</span><span class="sxs-lookup"><span data-stu-id="479c1-221">For this example, select Site 1.</span></span>  
12. <span data-ttu-id="479c1-222">Satış tesisi alanına bir değer girin veya buradan bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="479c1-222">In the Sales site field, enter or select a value.</span></span>
    * <span data-ttu-id="479c1-223">Bu örnek için, Tesis 1'i seçin.</span><span class="sxs-lookup"><span data-stu-id="479c1-223">For this example, select Site 1.</span></span>  
13. <span data-ttu-id="479c1-224">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="479c1-224">Close the page.</span></span>
14. <span data-ttu-id="479c1-225">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="479c1-225">Close the page.</span></span>
15. <span data-ttu-id="479c1-226">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="479c1-226">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="479c1-227">ITEM_C öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="479c1-227">Click ITEM_C.</span></span>  
16. <span data-ttu-id="479c1-228">Maliyetleri yönet bölümünü genişletin.</span><span class="sxs-lookup"><span data-stu-id="479c1-228">Expand the Manage costs section.</span></span>
17. <span data-ttu-id="479c1-229">Maliyet grubu alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="479c1-229">In the Cost group field, type a value.</span></span>
    * <span data-ttu-id="479c1-230">Bu örnek için M1 yazın.</span><span class="sxs-lookup"><span data-stu-id="479c1-230">For this example, type M1.</span></span>  
18. <span data-ttu-id="479c1-231">Eylem Bölmesinde Yönet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="479c1-231">On the Action Pane, click Manage costs.</span></span>
19. <span data-ttu-id="479c1-232">Madde fiyatı'na tıklayın.</span><span class="sxs-lookup"><span data-stu-id="479c1-232">Click Item price.</span></span>
20. <span data-ttu-id="479c1-233">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="479c1-233">Click New.</span></span>
21. <span data-ttu-id="479c1-234">Sürüm alanına bir değer girin veya buradan bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="479c1-234">In the Version field, enter or select a value.</span></span>
    * <span data-ttu-id="479c1-235">Bu örnek için, 10'u seçin.</span><span class="sxs-lookup"><span data-stu-id="479c1-235">For this example, select 10.</span></span> <span data-ttu-id="479c1-236">Bu, Standart maliyet maliyetlendirme türüdür.</span><span class="sxs-lookup"><span data-stu-id="479c1-236">This is the Standard cost costing type.</span></span>  
22. <span data-ttu-id="479c1-237">Tesis alanına bir değer girin veya buradan bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="479c1-237">In the Site field, enter or select a value.</span></span>
    * <span data-ttu-id="479c1-238">Bu örnek için, Tesis 1'i seçin.</span><span class="sxs-lookup"><span data-stu-id="479c1-238">For this example, select Site 1.</span></span>  
23. <span data-ttu-id="479c1-239">Fiyat alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="479c1-239">In the Price field, enter a number.</span></span>
    * <span data-ttu-id="479c1-240">Bu örnek için, 10 yazın.</span><span class="sxs-lookup"><span data-stu-id="479c1-240">For this example, type 10.</span></span>  
24. <span data-ttu-id="479c1-241">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="479c1-241">Click Save.</span></span>
25. <span data-ttu-id="479c1-242">Beklemedeki fiyatı/fiyatları etkinleştir'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="479c1-242">Click Activate pending price(s).</span></span>
26. <span data-ttu-id="479c1-243">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="479c1-243">Close the page.</span></span>
27. <span data-ttu-id="479c1-244">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="479c1-244">Close the page.</span></span>


