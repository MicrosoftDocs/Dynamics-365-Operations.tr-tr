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
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.author: bis
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 3a33e3f7c2bdc54bab255960cebdeb3edec6d20d
ms.contentlocale: tr-tr
ms.lasthandoff: 05/08/2018

---
# <a name="create-raw-materials-february-2016-only"></a><span data-ttu-id="6f9bb-103">Hammadde oluşturma (yalnızca Şubat 2016)</span><span class="sxs-lookup"><span data-stu-id="6f9bb-103">Create raw materials (February 2016 only)</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="6f9bb-104">Bu görev, bitmiş ve yarı mamul ürünlerin bileşenlerini oluşturmaya odaklanır.</span><span class="sxs-lookup"><span data-stu-id="6f9bb-104">This task focuses on creating the components of finished and semi-finished products.</span></span> <span data-ttu-id="6f9bb-105">Ürün Reçetesi hesaplama serisindeki üçüncü görevdir.</span><span class="sxs-lookup"><span data-stu-id="6f9bb-105">It is the third task in the BOM calculation series.</span></span> <span data-ttu-id="6f9bb-106">Bu görevi oluşturmak için kullanılan demo veri şirketi USMF'dir.</span><span class="sxs-lookup"><span data-stu-id="6f9bb-106">The demo data company used to create this task is USMF.</span></span>


## <a name="create-the-first-material"></a><span data-ttu-id="6f9bb-107">İlk malzemeyi oluşturma</span><span class="sxs-lookup"><span data-stu-id="6f9bb-107">Create the first material</span></span>
1. <span data-ttu-id="6f9bb-108">Product information management > Products > Released products (Ürün bilgi yönetimi > Ürünler > Piyasaya sürülmüş ürünler) menüsüne gidin.</span><span class="sxs-lookup"><span data-stu-id="6f9bb-108">Go to Product information management > Products > Released products.</span></span>
2. <span data-ttu-id="6f9bb-109">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="6f9bb-109">Click New.</span></span>
3. <span data-ttu-id="6f9bb-110">Ürün numarası alanında bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="6f9bb-110">In the Product number field, type a value.</span></span>
    * <span data-ttu-id="6f9bb-111">Bu örnek için, ITEM_A girin.</span><span class="sxs-lookup"><span data-stu-id="6f9bb-111">For this example, enter ITEM_A.</span></span>  
4. <span data-ttu-id="6f9bb-112">Model grubu alanına bir değer girin veya bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="6f9bb-112">In the Item model group field, enter or select a value.</span></span>
    * <span data-ttu-id="6f9bb-113">STD öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="6f9bb-113">Select STD.</span></span> <span data-ttu-id="6f9bb-114">STD, standart maliyet anlamına gelir ve maliyet hesaplamalarıyla çalışırken en yaygın olarak kullanılan modeldir.</span><span class="sxs-lookup"><span data-stu-id="6f9bb-114">STD stands for standard cost and is the most commonly used model when working with cost calculations.</span></span>  
5. <span data-ttu-id="6f9bb-115">Ürün grubu alanında bir değer girin veya bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="6f9bb-115">In the Item group field, enter or select a value.</span></span>
    * <span data-ttu-id="6f9bb-116">Örneğin, Ses'i seçin.</span><span class="sxs-lookup"><span data-stu-id="6f9bb-116">For example, select Audio.</span></span> <span data-ttu-id="6f9bb-117">Bunun, maliyet hesaplamaları üzerinde hiçbir etkisi yoktur.</span><span class="sxs-lookup"><span data-stu-id="6f9bb-117">This has no impact on cost calculations.</span></span>  
6. <span data-ttu-id="6f9bb-118">Stok boyutu grubu alanına bir değer girin veya bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="6f9bb-118">In the Storage dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="6f9bb-119">SiteWH'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="6f9bb-119">Select SiteWH.</span></span> <span data-ttu-id="6f9bb-120">Tanıtım için yalnızca Tesis ve Ambar kullanılır.</span><span class="sxs-lookup"><span data-stu-id="6f9bb-120">Only Site and Warehouse will be used for the demonstration.</span></span>  
7. <span data-ttu-id="6f9bb-121">İzleme boyutu grubu alanına bir değer girin veya bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="6f9bb-121">In the Tracking dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="6f9bb-122">Bu örnek için izleme boyutları kullanılmaz.</span><span class="sxs-lookup"><span data-stu-id="6f9bb-122">Tracking dimensions will not be used for this example.</span></span> <span data-ttu-id="6f9bb-123">Hiçbiri'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="6f9bb-123">Select None.</span></span>  
8. <span data-ttu-id="6f9bb-124">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="6f9bb-124">Click OK.</span></span>
9. <span data-ttu-id="6f9bb-125">Eylem Bölmesinde, Stok yönetimi'ne tıklayın.</span><span class="sxs-lookup"><span data-stu-id="6f9bb-125">On the Action Pane, click Manage inventory.</span></span>
10. <span data-ttu-id="6f9bb-126">Varsayılan sipariş ayarlarına tıklayın.</span><span class="sxs-lookup"><span data-stu-id="6f9bb-126">Click Default order settings.</span></span>
11. <span data-ttu-id="6f9bb-127">Satınalma tesisi alanına bir değer girin veya buradan bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="6f9bb-127">In the Purchase site field, enter or select a value.</span></span>
    * <span data-ttu-id="6f9bb-128">Bu örnek için, Tesis 1'i seçin.</span><span class="sxs-lookup"><span data-stu-id="6f9bb-128">For this example, select Site 1.</span></span>  
12. <span data-ttu-id="6f9bb-129">Stok tesisi alanına bir değer girin veya buradan bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="6f9bb-129">In the Inventory site field, enter or select a value.</span></span>
    * <span data-ttu-id="6f9bb-130">Bu örnek için, Tesis 1'i seçin.</span><span class="sxs-lookup"><span data-stu-id="6f9bb-130">For this example, select Site 1.</span></span>  
13. <span data-ttu-id="6f9bb-131">Satış tesisi alanına bir değer girin veya buradan bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="6f9bb-131">In the Sales site field, enter or select a value.</span></span>
    * <span data-ttu-id="6f9bb-132">Bu örnek için, Tesis 1'i seçin.</span><span class="sxs-lookup"><span data-stu-id="6f9bb-132">For this example, select Site 1.</span></span>  
14. <span data-ttu-id="6f9bb-133">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="6f9bb-133">Close the page.</span></span>
15. <span data-ttu-id="6f9bb-134">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="6f9bb-134">Close the page.</span></span>
16. <span data-ttu-id="6f9bb-135">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="6f9bb-135">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="6f9bb-136">ITEM_A öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="6f9bb-136">Click ITEM_A.</span></span>  
17. <span data-ttu-id="6f9bb-137">Maliyetleri yönet bölümünü genişletin.</span><span class="sxs-lookup"><span data-stu-id="6f9bb-137">Expand the Manage costs section.</span></span>
18. <span data-ttu-id="6f9bb-138">Maliyet grubu alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="6f9bb-138">In the Cost group field, type a value.</span></span>
    * <span data-ttu-id="6f9bb-139">Bu örnek için M2 yazın.</span><span class="sxs-lookup"><span data-stu-id="6f9bb-139">For this example, type M2.</span></span>  
19. <span data-ttu-id="6f9bb-140">Eylem Bölmesinde Yönet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="6f9bb-140">On the Action Pane, click Manage costs.</span></span>
20. <span data-ttu-id="6f9bb-141">Madde fiyatı'na tıklayın.</span><span class="sxs-lookup"><span data-stu-id="6f9bb-141">Click Item price.</span></span>
21. <span data-ttu-id="6f9bb-142">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="6f9bb-142">Click New.</span></span>
22. <span data-ttu-id="6f9bb-143">Sürüm alanına bir değer girin veya buradan bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="6f9bb-143">In the Version field, enter or select a value.</span></span>
    * <span data-ttu-id="6f9bb-144">Bu örnek için, Standart maliyet maliyetlendirme türü olan 10'u seçin.</span><span class="sxs-lookup"><span data-stu-id="6f9bb-144">For this example, select 10, which is the Standard cost costing type.</span></span>  
23. <span data-ttu-id="6f9bb-145">Tesis alanına bir değer girin veya buradan bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="6f9bb-145">In the Site field, enter or select a value.</span></span>
    * <span data-ttu-id="6f9bb-146">Bu örnek için, Tesis 1'i seçin.</span><span class="sxs-lookup"><span data-stu-id="6f9bb-146">For this example, select Site 1.</span></span>  
24. <span data-ttu-id="6f9bb-147">Fiyat alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="6f9bb-147">In the Price field, enter a number.</span></span>
    * <span data-ttu-id="6f9bb-148">Bu örnek için, 10 yazın.</span><span class="sxs-lookup"><span data-stu-id="6f9bb-148">For this example, type 10.</span></span>  
25. <span data-ttu-id="6f9bb-149">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="6f9bb-149">Click Save.</span></span>
26. <span data-ttu-id="6f9bb-150">Beklemedeki fiyatı/fiyatları etkinleştir'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="6f9bb-150">Click Activate pending price(s).</span></span>
27. <span data-ttu-id="6f9bb-151">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="6f9bb-151">Close the page.</span></span>
28. <span data-ttu-id="6f9bb-152">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="6f9bb-152">Close the page.</span></span>

## <a name="create-the-second-material"></a><span data-ttu-id="6f9bb-153">İkinci malzemeyi oluşturma</span><span class="sxs-lookup"><span data-stu-id="6f9bb-153">Create the second material</span></span>
1. <span data-ttu-id="6f9bb-154">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="6f9bb-154">Click New.</span></span>
2. <span data-ttu-id="6f9bb-155">Ürün numarası alanında bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="6f9bb-155">In the Product number field, type a value.</span></span>
    * <span data-ttu-id="6f9bb-156">Bu örnek için, ITEM_B yazın.</span><span class="sxs-lookup"><span data-stu-id="6f9bb-156">For this example, type ITEM_B.</span></span>  
3. <span data-ttu-id="6f9bb-157">Model grubu alanına bir değer girin veya bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="6f9bb-157">In the Item model group field, enter or select a value.</span></span>
    * <span data-ttu-id="6f9bb-158">STD öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="6f9bb-158">Select STD.</span></span> <span data-ttu-id="6f9bb-159">STD, standart maliyet anlamına gelir ve maliyet hesaplamalarıyla çalışırken en yaygın olarak kullanılan modeldir.</span><span class="sxs-lookup"><span data-stu-id="6f9bb-159">STD stands for standard cost and is the most commonly used model when working with cost calculations.</span></span>  
4. <span data-ttu-id="6f9bb-160">Ürün grubu alanında bir değer girin veya bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="6f9bb-160">In the Item group field, enter or select a value.</span></span>
    * <span data-ttu-id="6f9bb-161">Örneğin, Ses'i seçin.</span><span class="sxs-lookup"><span data-stu-id="6f9bb-161">For example, select Audio.</span></span> <span data-ttu-id="6f9bb-162">Bunun, maliyet hesaplamaları üzerinde hiçbir etkisi yoktur.</span><span class="sxs-lookup"><span data-stu-id="6f9bb-162">This has no impact on cost calculations.</span></span>  
5. <span data-ttu-id="6f9bb-163">Stok boyutu grubu alanına bir değer girin veya bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="6f9bb-163">In the Storage dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="6f9bb-164">SiteWH'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="6f9bb-164">Select SiteWH.</span></span> <span data-ttu-id="6f9bb-165">Bu örnek için yalnızca Tesis ve Ambar kullanılır.</span><span class="sxs-lookup"><span data-stu-id="6f9bb-165">Only Site and Warehouse will be used for this example.</span></span>  
6. <span data-ttu-id="6f9bb-166">İzleme boyutu grubu alanına bir değer girin veya bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="6f9bb-166">In the Tracking dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="6f9bb-167">Bu örnek için izleme boyutları kullanılmaz.</span><span class="sxs-lookup"><span data-stu-id="6f9bb-167">Tracking dimensions will not be used for this example.</span></span> <span data-ttu-id="6f9bb-168">Hiçbiri'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="6f9bb-168">Select None.</span></span>  
7. <span data-ttu-id="6f9bb-169">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="6f9bb-169">Click OK.</span></span>
8. <span data-ttu-id="6f9bb-170">Eylem Bölmesinde, Stok yönetimi'ne tıklayın.</span><span class="sxs-lookup"><span data-stu-id="6f9bb-170">On the Action Pane, click Manage inventory.</span></span>
9. <span data-ttu-id="6f9bb-171">Varsayılan sipariş ayarlarına tıklayın.</span><span class="sxs-lookup"><span data-stu-id="6f9bb-171">Click Default order settings.</span></span>
10. <span data-ttu-id="6f9bb-172">Satınalma tesisi alanına bir değer girin veya buradan bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="6f9bb-172">In the Purchase site field, enter or select a value.</span></span>
    * <span data-ttu-id="6f9bb-173">Bu örnek için, Tesis 1'i seçin.</span><span class="sxs-lookup"><span data-stu-id="6f9bb-173">For this example, select Site 1.</span></span>  
11. <span data-ttu-id="6f9bb-174">Stok tesisi alanına bir değer girin veya buradan bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="6f9bb-174">In the Inventory site field, enter or select a value.</span></span>
    * <span data-ttu-id="6f9bb-175">Bu örnek için, Tesis 1'i seçin.</span><span class="sxs-lookup"><span data-stu-id="6f9bb-175">For this example, select Site 1.</span></span>  
12. <span data-ttu-id="6f9bb-176">Satış tesisi alanına bir değer girin veya buradan bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="6f9bb-176">In the Sales site field, enter or select a value.</span></span>
    * <span data-ttu-id="6f9bb-177">Bu örnek için, Tesis 1'i seçin.</span><span class="sxs-lookup"><span data-stu-id="6f9bb-177">For this example, select Site 1.</span></span>  
13. <span data-ttu-id="6f9bb-178">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="6f9bb-178">Close the page.</span></span>
14. <span data-ttu-id="6f9bb-179">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="6f9bb-179">Close the page.</span></span>
15. <span data-ttu-id="6f9bb-180">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="6f9bb-180">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="6f9bb-181">ITEM_B öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="6f9bb-181">Click ITEM_B.</span></span>  
16. <span data-ttu-id="6f9bb-182">Maliyetleri yönet bölümünü genişletin.</span><span class="sxs-lookup"><span data-stu-id="6f9bb-182">Expand the Manage costs section.</span></span>
17. <span data-ttu-id="6f9bb-183">Maliyet grubu alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="6f9bb-183">In the Cost group field, type a value.</span></span>
    * <span data-ttu-id="6f9bb-184">Bu örnek için M2 yazın.</span><span class="sxs-lookup"><span data-stu-id="6f9bb-184">For this example, type M2.</span></span>  
18. <span data-ttu-id="6f9bb-185">Eylem Bölmesinde Yönet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="6f9bb-185">On the Action Pane, click Manage costs.</span></span>
19. <span data-ttu-id="6f9bb-186">Madde fiyatı'na tıklayın.</span><span class="sxs-lookup"><span data-stu-id="6f9bb-186">Click Item price.</span></span>
20. <span data-ttu-id="6f9bb-187">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="6f9bb-187">Click New.</span></span>
21. <span data-ttu-id="6f9bb-188">Sürüm alanına bir değer girin veya buradan bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="6f9bb-188">In the Version field, enter or select a value.</span></span>
    * <span data-ttu-id="6f9bb-189">Bu örnek için, 10'u seçin.</span><span class="sxs-lookup"><span data-stu-id="6f9bb-189">For this example, select 10.</span></span> <span data-ttu-id="6f9bb-190">Bu, Standart maliyet maliyetlendirme türüdür.</span><span class="sxs-lookup"><span data-stu-id="6f9bb-190">This is the Standard cost costing type.</span></span>  
22. <span data-ttu-id="6f9bb-191">Tesis alanına bir değer girin veya buradan bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="6f9bb-191">In the Site field, enter or select a value.</span></span>
    * <span data-ttu-id="6f9bb-192">Bu örnek için, Tesis 1'i seçin.</span><span class="sxs-lookup"><span data-stu-id="6f9bb-192">For this example, select Site 1.</span></span>  
23. <span data-ttu-id="6f9bb-193">Fiyat alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="6f9bb-193">In the Price field, enter a number.</span></span>
    * <span data-ttu-id="6f9bb-194">Tanıtım için, 10 yazın.</span><span class="sxs-lookup"><span data-stu-id="6f9bb-194">For the demonstration, type 10.</span></span>  
24. <span data-ttu-id="6f9bb-195">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="6f9bb-195">Click Save.</span></span>
25. <span data-ttu-id="6f9bb-196">Beklemedeki fiyatı/fiyatları etkinleştir'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="6f9bb-196">Click Activate pending price(s).</span></span>
26. <span data-ttu-id="6f9bb-197">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="6f9bb-197">Close the page.</span></span>
27. <span data-ttu-id="6f9bb-198">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="6f9bb-198">Close the page.</span></span>

## <a name="create-the-third-material"></a><span data-ttu-id="6f9bb-199">Üçüncü malzemeyi oluşturma</span><span class="sxs-lookup"><span data-stu-id="6f9bb-199">Create the third material</span></span>
1. <span data-ttu-id="6f9bb-200">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="6f9bb-200">Click New.</span></span>
2. <span data-ttu-id="6f9bb-201">Ürün numarası alanında bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="6f9bb-201">In the Product number field, type a value.</span></span>
    * <span data-ttu-id="6f9bb-202">Tanıtım için, ITEM_C yazın.</span><span class="sxs-lookup"><span data-stu-id="6f9bb-202">For the demonstration, type ITEM_C</span></span>  
3. <span data-ttu-id="6f9bb-203">Model grubu alanına bir değer girin veya bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="6f9bb-203">In the Item model group field, enter or select a value.</span></span>
    * <span data-ttu-id="6f9bb-204">STD öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="6f9bb-204">Select STD.</span></span> <span data-ttu-id="6f9bb-205">STD, standart maliyet anlamına gelir ve maliyet hesaplamalarıyla çalışırken en yaygın olarak kullanılan modeldir.</span><span class="sxs-lookup"><span data-stu-id="6f9bb-205">STD stands for standard cost and is the most commonly used model when working with cost calculations.</span></span>  
4. <span data-ttu-id="6f9bb-206">Ürün grubu alanında bir değer girin veya bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="6f9bb-206">In the Item group field, enter or select a value.</span></span>
    * <span data-ttu-id="6f9bb-207">Örneğin, Ses'i seçin.</span><span class="sxs-lookup"><span data-stu-id="6f9bb-207">For example, select Audio.</span></span> <span data-ttu-id="6f9bb-208">Bunun, maliyet hesaplamaları üzerinde hiçbir etkisi yoktur.</span><span class="sxs-lookup"><span data-stu-id="6f9bb-208">This has no impact on cost calculations.</span></span>  
5. <span data-ttu-id="6f9bb-209">Stok boyutu grubu alanına bir değer girin veya bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="6f9bb-209">In the Storage dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="6f9bb-210">SiteWH'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="6f9bb-210">Select SiteWH.</span></span> <span data-ttu-id="6f9bb-211">Tanıtım için yalnızca Tesis ve Ambar kullanılır.</span><span class="sxs-lookup"><span data-stu-id="6f9bb-211">Only Site and Warehouse will be used for the demonstration.</span></span>  
6. <span data-ttu-id="6f9bb-212">İzleme boyutu grubu alanına bir değer girin veya bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="6f9bb-212">In the Tracking dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="6f9bb-213">Bu örnek için izleme boyutları kullanılmaz.</span><span class="sxs-lookup"><span data-stu-id="6f9bb-213">Tracking dimensions will not be used for this example.</span></span> <span data-ttu-id="6f9bb-214">Hiçbiri'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="6f9bb-214">Select None.</span></span>  
7. <span data-ttu-id="6f9bb-215">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="6f9bb-215">Click OK.</span></span>
8. <span data-ttu-id="6f9bb-216">Eylem Bölmesinde, Stok yönetimi'ne tıklayın.</span><span class="sxs-lookup"><span data-stu-id="6f9bb-216">On the Action Pane, click Manage inventory.</span></span>
9. <span data-ttu-id="6f9bb-217">Varsayılan sipariş ayarlarına tıklayın.</span><span class="sxs-lookup"><span data-stu-id="6f9bb-217">Click Default order settings.</span></span>
10. <span data-ttu-id="6f9bb-218">Satınalma tesisi alanına bir değer girin veya buradan bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="6f9bb-218">In the Purchase site field, enter or select a value.</span></span>
    * <span data-ttu-id="6f9bb-219">Bu örnek için, Tesis 1'i seçin.</span><span class="sxs-lookup"><span data-stu-id="6f9bb-219">For this example, select Site 1.</span></span>  
11. <span data-ttu-id="6f9bb-220">Stok tesisi alanına bir değer girin veya buradan bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="6f9bb-220">In the Inventory site field, enter or select a value.</span></span>
    * <span data-ttu-id="6f9bb-221">Bu örnek için, Tesis 1'i seçin.</span><span class="sxs-lookup"><span data-stu-id="6f9bb-221">For this example, select Site 1.</span></span>  
12. <span data-ttu-id="6f9bb-222">Satış tesisi alanına bir değer girin veya buradan bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="6f9bb-222">In the Sales site field, enter or select a value.</span></span>
    * <span data-ttu-id="6f9bb-223">Bu örnek için, Tesis 1'i seçin.</span><span class="sxs-lookup"><span data-stu-id="6f9bb-223">For this example, select Site 1.</span></span>  
13. <span data-ttu-id="6f9bb-224">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="6f9bb-224">Close the page.</span></span>
14. <span data-ttu-id="6f9bb-225">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="6f9bb-225">Close the page.</span></span>
15. <span data-ttu-id="6f9bb-226">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="6f9bb-226">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="6f9bb-227">ITEM_C öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="6f9bb-227">Click ITEM_C.</span></span>  
16. <span data-ttu-id="6f9bb-228">Maliyetleri yönet bölümünü genişletin.</span><span class="sxs-lookup"><span data-stu-id="6f9bb-228">Expand the Manage costs section.</span></span>
17. <span data-ttu-id="6f9bb-229">Maliyet grubu alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="6f9bb-229">In the Cost group field, type a value.</span></span>
    * <span data-ttu-id="6f9bb-230">Bu örnek için M1 yazın.</span><span class="sxs-lookup"><span data-stu-id="6f9bb-230">For this example, type M1.</span></span>  
18. <span data-ttu-id="6f9bb-231">Eylem Bölmesinde Yönet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="6f9bb-231">On the Action Pane, click Manage costs.</span></span>
19. <span data-ttu-id="6f9bb-232">Madde fiyatı'na tıklayın.</span><span class="sxs-lookup"><span data-stu-id="6f9bb-232">Click Item price.</span></span>
20. <span data-ttu-id="6f9bb-233">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="6f9bb-233">Click New.</span></span>
21. <span data-ttu-id="6f9bb-234">Sürüm alanına bir değer girin veya buradan bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="6f9bb-234">In the Version field, enter or select a value.</span></span>
    * <span data-ttu-id="6f9bb-235">Bu örnek için, 10'u seçin.</span><span class="sxs-lookup"><span data-stu-id="6f9bb-235">For this example, select 10.</span></span> <span data-ttu-id="6f9bb-236">Bu, Standart maliyet maliyetlendirme türüdür.</span><span class="sxs-lookup"><span data-stu-id="6f9bb-236">This is the Standard cost costing type.</span></span>  
22. <span data-ttu-id="6f9bb-237">Tesis alanına bir değer girin veya buradan bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="6f9bb-237">In the Site field, enter or select a value.</span></span>
    * <span data-ttu-id="6f9bb-238">Bu örnek için, Tesis 1'i seçin.</span><span class="sxs-lookup"><span data-stu-id="6f9bb-238">For this example, select Site 1.</span></span>  
23. <span data-ttu-id="6f9bb-239">Fiyat alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="6f9bb-239">In the Price field, enter a number.</span></span>
    * <span data-ttu-id="6f9bb-240">Bu örnek için, 10 yazın.</span><span class="sxs-lookup"><span data-stu-id="6f9bb-240">For this example, type 10.</span></span>  
24. <span data-ttu-id="6f9bb-241">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="6f9bb-241">Click Save.</span></span>
25. <span data-ttu-id="6f9bb-242">Beklemedeki fiyatı/fiyatları etkinleştir'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="6f9bb-242">Click Activate pending price(s).</span></span>
26. <span data-ttu-id="6f9bb-243">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="6f9bb-243">Close the page.</span></span>
27. <span data-ttu-id="6f9bb-244">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="6f9bb-244">Close the page.</span></span>


