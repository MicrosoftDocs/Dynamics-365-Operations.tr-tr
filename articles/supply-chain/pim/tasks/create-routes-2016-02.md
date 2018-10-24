--- 
title: "Rotalar oluşturma (Şubat 2016)"
description: "Bu görev, tamamlanmış bir ürün ve yarı mamul bir ürün için üretim rotalarını oluşturmaya odaklanır."
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: EcoResProductDetailsExtended, RouteInventProd, RouteGroup
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 965826f5fddc2f53f33157434929eb265979376e
ms.openlocfilehash: a68b28c0e0ee14429a23d3241cabdae948d706d2
ms.contentlocale: tr-tr
ms.lasthandoff: 09/17/2018

---
# <a name="create-routes-february-2016"></a><span data-ttu-id="e0fd4-103">Rotalar oluşturma (Şubat 2016)</span><span class="sxs-lookup"><span data-stu-id="e0fd4-103">Create routes (February 2016)</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="e0fd4-104">Bu görev, tamamlanmış bir ürün ve yarı mamul bir ürün için üretim rotalarını oluşturmaya odaklanır.</span><span class="sxs-lookup"><span data-stu-id="e0fd4-104">This task focuses on creating the production routes for a finished product and a semi-finished product.</span></span> <span data-ttu-id="e0fd4-105">Ürün reçetesi hesaplaması serisindeki beşinci görevdir.</span><span class="sxs-lookup"><span data-stu-id="e0fd4-105">It is the fifth task in the BOM calculation series.</span></span> <span data-ttu-id="e0fd4-106">Bu görevi oluşturmak için kullanılan demo veri şirketi USMF'dir.</span><span class="sxs-lookup"><span data-stu-id="e0fd4-106">The demo data company used to create this task is USMF.</span></span>


## <a name="create-a-route-for-a-semi-finished-product"></a><span data-ttu-id="e0fd4-107">Yarı mamul bir ürün için rota oluşturma</span><span class="sxs-lookup"><span data-stu-id="e0fd4-107">Create a route for a semi-finished product</span></span>
1. <span data-ttu-id="e0fd4-108">Product information management > Products > Released products (Ürün bilgi yönetimi > Ürünler > Piyasaya sürülmüş ürünler) menüsüne gidin.</span><span class="sxs-lookup"><span data-stu-id="e0fd4-108">Go to Product information management > Products > Released products.</span></span>
2. <span data-ttu-id="e0fd4-109">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="e0fd4-109">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="e0fd4-110">BOM_2 madde numarasını seçin.</span><span class="sxs-lookup"><span data-stu-id="e0fd4-110">Select the item number BOM_2.</span></span>  
3. <span data-ttu-id="e0fd4-111">Eylem Bölmesinde, Mühendis öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="e0fd4-111">On the Action Pane, click Engineer.</span></span>
4. <span data-ttu-id="e0fd4-112">Rota'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="e0fd4-112">Click Route.</span></span>
5. <span data-ttu-id="e0fd4-113">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="e0fd4-113">Click New.</span></span>
6. <span data-ttu-id="e0fd4-114">Rota ve rota sürümü'ne tıklayın.</span><span class="sxs-lookup"><span data-stu-id="e0fd4-114">Click Route and route version.</span></span>
7. <span data-ttu-id="e0fd4-115">Açıklama alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="e0fd4-115">In the Description field, type a value.</span></span>
    * <span data-ttu-id="e0fd4-116">Bu örnek için, ROUTE_2 yazın.</span><span class="sxs-lookup"><span data-stu-id="e0fd4-116">For example, type ROUTE_2.</span></span>  
8. <span data-ttu-id="e0fd4-117">Tesis alanına bir değer girin veya buradan bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="e0fd4-117">In the Site field, enter or select a value.</span></span>
    * <span data-ttu-id="e0fd4-118">Bu örnek için, Tesis 1'i girin veya seçin.</span><span class="sxs-lookup"><span data-stu-id="e0fd4-118">For this example, enter or select Site 1.</span></span>  
9. <span data-ttu-id="e0fd4-119">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="e0fd4-119">Click OK.</span></span>
10. <span data-ttu-id="e0fd4-120">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="e0fd4-120">Click New.</span></span>
11. <span data-ttu-id="e0fd4-121">Operasyon alanında bir değer girin veya bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="e0fd4-121">In the Operation field, enter or select a value.</span></span>
    * <span data-ttu-id="e0fd4-122">Bu örnek için Derleme seçeneğini belirtin.</span><span class="sxs-lookup"><span data-stu-id="e0fd4-122">For this example, select Assembly.</span></span>  
12. <span data-ttu-id="e0fd4-123">Çalışma süresi alanında bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="e0fd4-123">In the Run time field, enter a number.</span></span>
    * <span data-ttu-id="e0fd4-124">Örneğin 1 yazın.</span><span class="sxs-lookup"><span data-stu-id="e0fd4-124">For example, type 1.</span></span> <span data-ttu-id="e0fd4-125">Çalışma zamanları genellikle madde için hesaplanan fiyatın parçasıdır.</span><span class="sxs-lookup"><span data-stu-id="e0fd4-125">Run times are often part of the price that is calculated for an item.</span></span>  
13. <span data-ttu-id="e0fd4-126">Rota grubu alanında bir değer girin veya bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="e0fd4-126">In the Route group field, enter or select a value.</span></span>
    * <span data-ttu-id="e0fd4-127">Bu örnek için, Std seçeneğini belirtin.</span><span class="sxs-lookup"><span data-stu-id="e0fd4-127">For this example, select Std.</span></span>  
14. <span data-ttu-id="e0fd4-128">Kurulum sekmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="e0fd4-128">Click the Setup tab.</span></span>
15. <span data-ttu-id="e0fd4-129">Kurulum kategorisi alanında bir değer girin veya seçin.</span><span class="sxs-lookup"><span data-stu-id="e0fd4-129">In the Setup category field, enter or select a value.</span></span>
    * <span data-ttu-id="e0fd4-130">Bu örnek için Derleme seçeneğini belirtin.</span><span class="sxs-lookup"><span data-stu-id="e0fd4-130">For this example, select Assembly.</span></span>  
16. <span data-ttu-id="e0fd4-131">Zaman sekmesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="e0fd4-131">Click the Times tab.</span></span>
17. <span data-ttu-id="e0fd4-132">Hazırlık süresi alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="e0fd4-132">In the Setup time field, enter a number.</span></span>
    * <span data-ttu-id="e0fd4-133">Bu örnek için, 1 yazın.</span><span class="sxs-lookup"><span data-stu-id="e0fd4-133">For this example, type 1.</span></span> <span data-ttu-id="e0fd4-134">Kurulum zamanları genellikle madde için hesaplanan fiyatın parçasıdır.</span><span class="sxs-lookup"><span data-stu-id="e0fd4-134">Setup times are often part of the price that is calculated for an item.</span></span>  
18. <span data-ttu-id="e0fd4-135">Eylem Bölmesi'nde, Rota sürümü'ne tıklayın.</span><span class="sxs-lookup"><span data-stu-id="e0fd4-135">On the Action Pane, click Route version.</span></span>
19. <span data-ttu-id="e0fd4-136">Onayla’yı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="e0fd4-136">Click Approve.</span></span>
20. <span data-ttu-id="e0fd4-137">Rotayı da onaylamak ister misiniz? sorusunu Evet olarak yanıtlayın. alanda kullandığınızda otomatik olarak işaretlenir.</span><span class="sxs-lookup"><span data-stu-id="e0fd4-137">Select Yes in the Do you also want to approve the route? field.</span></span>
21. <span data-ttu-id="e0fd4-138">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="e0fd4-138">Click OK.</span></span>
22. <span data-ttu-id="e0fd4-139">Eylem Bölmesi'nde, Rota sürümü'ne tıklayın.</span><span class="sxs-lookup"><span data-stu-id="e0fd4-139">On the Action Pane, click Route version.</span></span>
23. <span data-ttu-id="e0fd4-140">Etkinleştir'i tıklatın.</span><span class="sxs-lookup"><span data-stu-id="e0fd4-140">Click Activate.</span></span>
24. <span data-ttu-id="e0fd4-141">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="e0fd4-141">Close the page.</span></span>
25. <span data-ttu-id="e0fd4-142">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="e0fd4-142">Close the page.</span></span>

## <a name="create-a-route-for-a-finished-product"></a><span data-ttu-id="e0fd4-143">Tamamlanmış bir ürün için rota oluşturma</span><span class="sxs-lookup"><span data-stu-id="e0fd4-143">Create a route for a finished product</span></span>
1. <span data-ttu-id="e0fd4-144">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="e0fd4-144">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="e0fd4-145">BOM_1 madde numarasını seçin.</span><span class="sxs-lookup"><span data-stu-id="e0fd4-145">Select the item number BOM_1.</span></span>  
2. <span data-ttu-id="e0fd4-146">Eylem Bölmesinde, Mühendis öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="e0fd4-146">On the Action Pane, click Engineer.</span></span>
3. <span data-ttu-id="e0fd4-147">Rota'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="e0fd4-147">Click Route.</span></span>
4. <span data-ttu-id="e0fd4-148">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="e0fd4-148">Click New.</span></span>
5. <span data-ttu-id="e0fd4-149">Rota ve rota sürümü'ne tıklayın.</span><span class="sxs-lookup"><span data-stu-id="e0fd4-149">Click Route and route version.</span></span>
6. <span data-ttu-id="e0fd4-150">Açıklama alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="e0fd4-150">In the Description field, type a value.</span></span>
    * <span data-ttu-id="e0fd4-151">Bu örnek için, ROUTE_1 yazın.</span><span class="sxs-lookup"><span data-stu-id="e0fd4-151">For this example, type ROUTE_1.</span></span>  
7. <span data-ttu-id="e0fd4-152">Tesis alanına bir değer girin veya buradan bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="e0fd4-152">In the Site field, enter or select a value.</span></span>
    * <span data-ttu-id="e0fd4-153">Bu örnek için, Tesis 1'i girin veya seçin.</span><span class="sxs-lookup"><span data-stu-id="e0fd4-153">For this example, enter or select Site 1.</span></span>  
8. <span data-ttu-id="e0fd4-154">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="e0fd4-154">Click OK.</span></span>
9. <span data-ttu-id="e0fd4-155">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="e0fd4-155">Click New.</span></span>
10. <span data-ttu-id="e0fd4-156">Operasyon alanında bir değer girin veya bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="e0fd4-156">In the Operation field, enter or select a value.</span></span>
    * <span data-ttu-id="e0fd4-157">Bu örnek için, Ambalaj seçeneğini belirtin.</span><span class="sxs-lookup"><span data-stu-id="e0fd4-157">For this example, select Packing.</span></span>  
11. <span data-ttu-id="e0fd4-158">Çalışma süresi alanında bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="e0fd4-158">In the Run time field, enter a number.</span></span>
    * <span data-ttu-id="e0fd4-159">Bu örnek için, 1 yazın.</span><span class="sxs-lookup"><span data-stu-id="e0fd4-159">For this example, type 1.</span></span>  
12. <span data-ttu-id="e0fd4-160">Rota grubu alanında bir değer girin veya bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="e0fd4-160">In the Route group field, enter or select a value.</span></span>
    * <span data-ttu-id="e0fd4-161">Bu örnek için, Std seçeneğini belirtin.</span><span class="sxs-lookup"><span data-stu-id="e0fd4-161">For this example, select Std.</span></span>  
13. <span data-ttu-id="e0fd4-162">Kurulum sekmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="e0fd4-162">Click the Setup tab.</span></span>
14. <span data-ttu-id="e0fd4-163">Kurulum kategorisi alanında bir değer girin veya seçin.</span><span class="sxs-lookup"><span data-stu-id="e0fd4-163">In the Setup category field, enter or select a value.</span></span>
    * <span data-ttu-id="e0fd4-164">Bu örnek için, Ambalaj seçeneğini belirtin.</span><span class="sxs-lookup"><span data-stu-id="e0fd4-164">For this example, select Packing.</span></span>  
15. <span data-ttu-id="e0fd4-165">Zaman sekmesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="e0fd4-165">Click the Times tab.</span></span>
16. <span data-ttu-id="e0fd4-166">Hazırlık süresi alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="e0fd4-166">In the Setup time field, enter a number.</span></span>
    * <span data-ttu-id="e0fd4-167">Bu örnek için, 1 yazın.</span><span class="sxs-lookup"><span data-stu-id="e0fd4-167">For this example, type 1.</span></span>  
17. <span data-ttu-id="e0fd4-168">Eylem Bölmesi'nde, Rota sürümü'ne tıklayın.</span><span class="sxs-lookup"><span data-stu-id="e0fd4-168">On the Action Pane, click Route version.</span></span>
18. <span data-ttu-id="e0fd4-169">Onayla’yı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="e0fd4-169">Click Approve.</span></span>
19. <span data-ttu-id="e0fd4-170">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="e0fd4-170">Click OK.</span></span>
20. <span data-ttu-id="e0fd4-171">Eylem Bölmesi'nde, Rota sürümü'ne tıklayın.</span><span class="sxs-lookup"><span data-stu-id="e0fd4-171">On the Action Pane, click Route version.</span></span>
21. <span data-ttu-id="e0fd4-172">Etkinleştir'i tıklatın.</span><span class="sxs-lookup"><span data-stu-id="e0fd4-172">Click Activate.</span></span>
22. <span data-ttu-id="e0fd4-173">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="e0fd4-173">Close the page.</span></span>
23. <span data-ttu-id="e0fd4-174">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="e0fd4-174">Close the page.</span></span>

## <a name="enable-automatic-consumption-of-setup-time"></a><span data-ttu-id="e0fd4-175">Hazırlık süresinin otomatik tüketimini etkinleştirme</span><span class="sxs-lookup"><span data-stu-id="e0fd4-175">Enable automatic consumption of setup time</span></span>
1. <span data-ttu-id="e0fd4-176">Üretim denetimi > Kurulum > Rotalar > Rota grupları öğesine gidin.</span><span class="sxs-lookup"><span data-stu-id="e0fd4-176">Go to Production control > Setup > Routes > Route groups.</span></span>
2. <span data-ttu-id="e0fd4-177">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="e0fd4-177">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="e0fd4-178">Listede, Std seçeneğini belirtin.</span><span class="sxs-lookup"><span data-stu-id="e0fd4-178">Select Std in the list.</span></span>  
3. <span data-ttu-id="e0fd4-179">Düzenle öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="e0fd4-179">Click Edit.</span></span>
4. <span data-ttu-id="e0fd4-180">Hazırlık süresi alanında, Evet'i seçin.</span><span class="sxs-lookup"><span data-stu-id="e0fd4-180">Select Yes in the Setup time field.</span></span>
    * <span data-ttu-id="e0fd4-181">Kurulum zamanları genellikle madde için hesaplanan fiyatın parçasıdır.</span><span class="sxs-lookup"><span data-stu-id="e0fd4-181">Setup times are often part of the price that is calculated for an item.</span></span>  
5. <span data-ttu-id="e0fd4-182">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="e0fd4-182">Click Save.</span></span>
6. <span data-ttu-id="e0fd4-183">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="e0fd4-183">Close the page.</span></span>


