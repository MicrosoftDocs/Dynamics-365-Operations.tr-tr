--- 
title: "Rotalar oluşturma (yalnızca Şubat 2016)"
description: "Bu görev, tamamlanmış bir ürün ve yarı mamul bir ürün için üretim rotalarını oluşturmaya odaklanır."
author: ShylaThompson
manager: AnnBe
ms.date: 02/07/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 1d98cbff30620256c9d13e7b4a90314db150e33e
ms.openlocfilehash: 63ad2cc0c41a5931750dffbfc64bc7ce965a1da4
ms.contentlocale: tr-tr
ms.lasthandoff: 08/07/2018

---
# <a name="create-routes-february-2016-only"></a><span data-ttu-id="9b44a-103">Rotalar oluşturma (yalnızca Şubat 2016)</span><span class="sxs-lookup"><span data-stu-id="9b44a-103">Create routes (February 2016 only)</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="9b44a-104">Bu görev, tamamlanmış bir ürün ve yarı mamul bir ürün için üretim rotalarını oluşturmaya odaklanır.</span><span class="sxs-lookup"><span data-stu-id="9b44a-104">This task focuses on creating the production routes for a finished product and a semi-finished product.</span></span> <span data-ttu-id="9b44a-105">Ürün reçetesi hesaplaması serisindeki beşinci görevdir.</span><span class="sxs-lookup"><span data-stu-id="9b44a-105">It is the fifth task in the BOM calculation series.</span></span> <span data-ttu-id="9b44a-106">Bu görevi oluşturmak için kullanılan demo veri şirketi USMF'dir.</span><span class="sxs-lookup"><span data-stu-id="9b44a-106">The demo data company used to create this task is USMF.</span></span>


## <a name="create-a-route-for-a-semi-finished-product"></a><span data-ttu-id="9b44a-107">Yarı mamul bir ürün için rota oluşturma</span><span class="sxs-lookup"><span data-stu-id="9b44a-107">Create a route for a semi-finished product</span></span>
1. <span data-ttu-id="9b44a-108">Product information management > Products > Released products (Ürün bilgi yönetimi > Ürünler > Piyasaya sürülmüş ürünler) menüsüne gidin.</span><span class="sxs-lookup"><span data-stu-id="9b44a-108">Go to Product information management > Products > Released products.</span></span>
2. <span data-ttu-id="9b44a-109">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="9b44a-109">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="9b44a-110">BOM_2 madde numarasını seçin.</span><span class="sxs-lookup"><span data-stu-id="9b44a-110">Select the item number BOM_2.</span></span>  
3. <span data-ttu-id="9b44a-111">Eylem Bölmesinde, Mühendis öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="9b44a-111">On the Action Pane, click Engineer.</span></span>
4. <span data-ttu-id="9b44a-112">Rota'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="9b44a-112">Click Route.</span></span>
5. <span data-ttu-id="9b44a-113">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="9b44a-113">Click New.</span></span>
6. <span data-ttu-id="9b44a-114">Rota ve rota sürümü'ne tıklayın.</span><span class="sxs-lookup"><span data-stu-id="9b44a-114">Click Route and route version.</span></span>
7. <span data-ttu-id="9b44a-115">Açıklama alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="9b44a-115">In the Description field, type a value.</span></span>
    * <span data-ttu-id="9b44a-116">Bu örnek için, ROUTE_2 yazın.</span><span class="sxs-lookup"><span data-stu-id="9b44a-116">For example, type ROUTE_2.</span></span>  
8. <span data-ttu-id="9b44a-117">Tesis alanına bir değer girin veya buradan bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="9b44a-117">In the Site field, enter or select a value.</span></span>
    * <span data-ttu-id="9b44a-118">Bu örnek için, Tesis 1'i girin veya seçin.</span><span class="sxs-lookup"><span data-stu-id="9b44a-118">For this example, enter or select Site 1.</span></span>  
9. <span data-ttu-id="9b44a-119">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="9b44a-119">Click OK.</span></span>
10. <span data-ttu-id="9b44a-120">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="9b44a-120">Click New.</span></span>
11. <span data-ttu-id="9b44a-121">Operasyon alanında bir değer girin veya bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="9b44a-121">In the Operation field, enter or select a value.</span></span>
    * <span data-ttu-id="9b44a-122">Bu örnek için Derleme seçeneğini belirtin.</span><span class="sxs-lookup"><span data-stu-id="9b44a-122">For this example, select Assembly.</span></span>  
12. <span data-ttu-id="9b44a-123">Çalışma süresi alanında bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="9b44a-123">In the Run time field, enter a number.</span></span>
    * <span data-ttu-id="9b44a-124">Örneğin 1 yazın.</span><span class="sxs-lookup"><span data-stu-id="9b44a-124">For example, type 1.</span></span> <span data-ttu-id="9b44a-125">Çalışma zamanları genellikle madde için hesaplanan fiyatın parçasıdır.</span><span class="sxs-lookup"><span data-stu-id="9b44a-125">Run times are often part of the price that is calculated for an item.</span></span>  
13. <span data-ttu-id="9b44a-126">Rota grubu alanında bir değer girin veya bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="9b44a-126">In the Route group field, enter or select a value.</span></span>
    * <span data-ttu-id="9b44a-127">Bu örnek için, Std seçeneğini belirtin.</span><span class="sxs-lookup"><span data-stu-id="9b44a-127">For this example, select Std.</span></span>  
14. <span data-ttu-id="9b44a-128">Kurulum sekmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="9b44a-128">Click the Setup tab.</span></span>
15. <span data-ttu-id="9b44a-129">Kurulum kategorisi alanında bir değer girin veya seçin.</span><span class="sxs-lookup"><span data-stu-id="9b44a-129">In the Setup category field, enter or select a value.</span></span>
    * <span data-ttu-id="9b44a-130">Bu örnek için Derleme seçeneğini belirtin.</span><span class="sxs-lookup"><span data-stu-id="9b44a-130">For this example, select Assembly.</span></span>  
16. <span data-ttu-id="9b44a-131">Zaman sekmesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="9b44a-131">Click the Times tab.</span></span>
17. <span data-ttu-id="9b44a-132">Hazırlık süresi alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="9b44a-132">In the Setup time field, enter a number.</span></span>
    * <span data-ttu-id="9b44a-133">Bu örnek için, 1 yazın.</span><span class="sxs-lookup"><span data-stu-id="9b44a-133">For this example, type 1.</span></span> <span data-ttu-id="9b44a-134">Kurulum zamanları genellikle madde için hesaplanan fiyatın parçasıdır.</span><span class="sxs-lookup"><span data-stu-id="9b44a-134">Setup times are often part of the price that is calculated for an item.</span></span>  
18. <span data-ttu-id="9b44a-135">Eylem Bölmesi'nde, Rota sürümü'ne tıklayın.</span><span class="sxs-lookup"><span data-stu-id="9b44a-135">On the Action Pane, click Route version.</span></span>
19. <span data-ttu-id="9b44a-136">Onayla’yı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="9b44a-136">Click Approve.</span></span>
20. <span data-ttu-id="9b44a-137">Rotayı da onaylamak ister misiniz? sorusunu Evet olarak yanıtlayın. alanda kullandığınızda otomatik olarak işaretlenir.</span><span class="sxs-lookup"><span data-stu-id="9b44a-137">Select Yes in the Do you also want to approve the route? field.</span></span>
21. <span data-ttu-id="9b44a-138">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="9b44a-138">Click OK.</span></span>
22. <span data-ttu-id="9b44a-139">Eylem Bölmesi'nde, Rota sürümü'ne tıklayın.</span><span class="sxs-lookup"><span data-stu-id="9b44a-139">On the Action Pane, click Route version.</span></span>
23. <span data-ttu-id="9b44a-140">Etkinleştir'i tıklatın.</span><span class="sxs-lookup"><span data-stu-id="9b44a-140">Click Activate.</span></span>
24. <span data-ttu-id="9b44a-141">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="9b44a-141">Close the page.</span></span>
25. <span data-ttu-id="9b44a-142">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="9b44a-142">Close the page.</span></span>

## <a name="create-a-route-for-a-finished-product"></a><span data-ttu-id="9b44a-143">Tamamlanmış bir ürün için rota oluşturma</span><span class="sxs-lookup"><span data-stu-id="9b44a-143">Create a route for a finished product</span></span>
1. <span data-ttu-id="9b44a-144">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="9b44a-144">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="9b44a-145">BOM_1 madde numarasını seçin.</span><span class="sxs-lookup"><span data-stu-id="9b44a-145">Select the item number BOM_1.</span></span>  
2. <span data-ttu-id="9b44a-146">Eylem Bölmesinde, Mühendis öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="9b44a-146">On the Action Pane, click Engineer.</span></span>
3. <span data-ttu-id="9b44a-147">Rota'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="9b44a-147">Click Route.</span></span>
4. <span data-ttu-id="9b44a-148">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="9b44a-148">Click New.</span></span>
5. <span data-ttu-id="9b44a-149">Rota ve rota sürümü'ne tıklayın.</span><span class="sxs-lookup"><span data-stu-id="9b44a-149">Click Route and route version.</span></span>
6. <span data-ttu-id="9b44a-150">Açıklama alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="9b44a-150">In the Description field, type a value.</span></span>
    * <span data-ttu-id="9b44a-151">Bu örnek için, ROUTE_1 yazın.</span><span class="sxs-lookup"><span data-stu-id="9b44a-151">For this example, type ROUTE_1.</span></span>  
7. <span data-ttu-id="9b44a-152">Tesis alanına bir değer girin veya buradan bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="9b44a-152">In the Site field, enter or select a value.</span></span>
    * <span data-ttu-id="9b44a-153">Bu örnek için, Tesis 1'i girin veya seçin.</span><span class="sxs-lookup"><span data-stu-id="9b44a-153">For this example, enter or select Site 1.</span></span>  
8. <span data-ttu-id="9b44a-154">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="9b44a-154">Click OK.</span></span>
9. <span data-ttu-id="9b44a-155">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="9b44a-155">Click New.</span></span>
10. <span data-ttu-id="9b44a-156">Operasyon alanında bir değer girin veya bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="9b44a-156">In the Operation field, enter or select a value.</span></span>
    * <span data-ttu-id="9b44a-157">Bu örnek için, Ambalaj seçeneğini belirtin.</span><span class="sxs-lookup"><span data-stu-id="9b44a-157">For this example, select Packing.</span></span>  
11. <span data-ttu-id="9b44a-158">Çalışma süresi alanında bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="9b44a-158">In the Run time field, enter a number.</span></span>
    * <span data-ttu-id="9b44a-159">Bu örnek için, 1 yazın.</span><span class="sxs-lookup"><span data-stu-id="9b44a-159">For this example, type 1.</span></span>  
12. <span data-ttu-id="9b44a-160">Rota grubu alanında bir değer girin veya bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="9b44a-160">In the Route group field, enter or select a value.</span></span>
    * <span data-ttu-id="9b44a-161">Bu örnek için, Std seçeneğini belirtin.</span><span class="sxs-lookup"><span data-stu-id="9b44a-161">For this example, select Std.</span></span>  
13. <span data-ttu-id="9b44a-162">Kurulum sekmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="9b44a-162">Click the Setup tab.</span></span>
14. <span data-ttu-id="9b44a-163">Kurulum kategorisi alanında bir değer girin veya seçin.</span><span class="sxs-lookup"><span data-stu-id="9b44a-163">In the Setup category field, enter or select a value.</span></span>
    * <span data-ttu-id="9b44a-164">Bu örnek için, Ambalaj seçeneğini belirtin.</span><span class="sxs-lookup"><span data-stu-id="9b44a-164">For this example, select Packing.</span></span>  
15. <span data-ttu-id="9b44a-165">Zaman sekmesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="9b44a-165">Click the Times tab.</span></span>
16. <span data-ttu-id="9b44a-166">Hazırlık süresi alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="9b44a-166">In the Setup time field, enter a number.</span></span>
    * <span data-ttu-id="9b44a-167">Bu örnek için, 1 yazın.</span><span class="sxs-lookup"><span data-stu-id="9b44a-167">For this example, type 1.</span></span>  
17. <span data-ttu-id="9b44a-168">Eylem Bölmesi'nde, Rota sürümü'ne tıklayın.</span><span class="sxs-lookup"><span data-stu-id="9b44a-168">On the Action Pane, click Route version.</span></span>
18. <span data-ttu-id="9b44a-169">Onayla’yı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="9b44a-169">Click Approve.</span></span>
19. <span data-ttu-id="9b44a-170">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="9b44a-170">Click OK.</span></span>
20. <span data-ttu-id="9b44a-171">Eylem Bölmesi'nde, Rota sürümü'ne tıklayın.</span><span class="sxs-lookup"><span data-stu-id="9b44a-171">On the Action Pane, click Route version.</span></span>
21. <span data-ttu-id="9b44a-172">Etkinleştir'i tıklatın.</span><span class="sxs-lookup"><span data-stu-id="9b44a-172">Click Activate.</span></span>
22. <span data-ttu-id="9b44a-173">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="9b44a-173">Close the page.</span></span>
23. <span data-ttu-id="9b44a-174">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="9b44a-174">Close the page.</span></span>

## <a name="enable-automatic-consumption-of-setup-time"></a><span data-ttu-id="9b44a-175">Hazırlık süresinin otomatik tüketimini etkinleştirme</span><span class="sxs-lookup"><span data-stu-id="9b44a-175">Enable automatic consumption of setup time</span></span>
1. <span data-ttu-id="9b44a-176">Üretim denetimi > Kurulum > Rotalar > Rota grupları öğesine gidin.</span><span class="sxs-lookup"><span data-stu-id="9b44a-176">Go to Production control > Setup > Routes > Route groups.</span></span>
2. <span data-ttu-id="9b44a-177">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="9b44a-177">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="9b44a-178">Listede, Std seçeneğini belirtin.</span><span class="sxs-lookup"><span data-stu-id="9b44a-178">Select Std in the list.</span></span>  
3. <span data-ttu-id="9b44a-179">Düzenle öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="9b44a-179">Click Edit.</span></span>
4. <span data-ttu-id="9b44a-180">Hazırlık süresi alanında, Evet'i seçin.</span><span class="sxs-lookup"><span data-stu-id="9b44a-180">Select Yes in the Setup time field.</span></span>
    * <span data-ttu-id="9b44a-181">Kurulum zamanları genellikle madde için hesaplanan fiyatın parçasıdır.</span><span class="sxs-lookup"><span data-stu-id="9b44a-181">Setup times are often part of the price that is calculated for an item.</span></span>  
5. <span data-ttu-id="9b44a-182">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="9b44a-182">Click Save.</span></span>
6. <span data-ttu-id="9b44a-183">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="9b44a-183">Close the page.</span></span>


