--- 
title: "Rotalar oluşturma (yalnızca Şubat 2016)"
description: "Bu görev, tamamlanmış bir ürün ve yarı mamul bir ürün için üretim rotalarını oluşturmaya odaklanır."
author: BibiSp
manager: AnnBe
ms.date: 02/07/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.author: bis
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 273ced77a61d485426c0830556e4401e782e86c4
ms.openlocfilehash: 1ba2ae3ad92149636714701448d4dac8296d6613
ms.contentlocale: tr-tr
ms.lasthandoff: 10/24/2017

---
# <a name="create-routes-february-2016-only"></a><span data-ttu-id="0c2ee-103">Rotalar oluşturma (yalnızca Şubat 2016)</span><span class="sxs-lookup"><span data-stu-id="0c2ee-103">Create routes (February 2016 only)</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="0c2ee-104">Bu görev, tamamlanmış bir ürün ve yarı mamul bir ürün için üretim rotalarını oluşturmaya odaklanır.</span><span class="sxs-lookup"><span data-stu-id="0c2ee-104">This task focuses on creating the production routes for a finished product and a semi-finished product.</span></span> <span data-ttu-id="0c2ee-105">Ürün reçetesi hesaplaması serisindeki beşinci görevdir.</span><span class="sxs-lookup"><span data-stu-id="0c2ee-105">It is the fifth task in the BOM calculation series.</span></span> <span data-ttu-id="0c2ee-106">Bu görevi oluşturmak için kullanılan demo veri şirketi USMF'dir.</span><span class="sxs-lookup"><span data-stu-id="0c2ee-106">The demo data company used to create this task is USMF.</span></span>


## <a name="create-a-route-for-a-semi-finished-product"></a><span data-ttu-id="0c2ee-107">Yarı mamul bir ürün için rota oluşturma</span><span class="sxs-lookup"><span data-stu-id="0c2ee-107">Create a route for a semi-finished product</span></span>
1. <span data-ttu-id="0c2ee-108">Product information management > Products > Released products (Ürün bilgi yönetimi > Ürünler > Piyasaya sürülmüş ürünler) menüsüne gidin.</span><span class="sxs-lookup"><span data-stu-id="0c2ee-108">Go to Product information management > Products > Released products.</span></span>
2. <span data-ttu-id="0c2ee-109">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="0c2ee-109">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="0c2ee-110">BOM_2 madde numarasını seçin.</span><span class="sxs-lookup"><span data-stu-id="0c2ee-110">Select the item number BOM_2.</span></span>  
3. <span data-ttu-id="0c2ee-111">Eylem Bölmesinde, Mühendis öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="0c2ee-111">On the Action Pane, click Engineer.</span></span>
4. <span data-ttu-id="0c2ee-112">Rota'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="0c2ee-112">Click Route.</span></span>
5. <span data-ttu-id="0c2ee-113">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="0c2ee-113">Click New.</span></span>
6. <span data-ttu-id="0c2ee-114">Rota ve rota sürümü'ne tıklayın.</span><span class="sxs-lookup"><span data-stu-id="0c2ee-114">Click Route and route version.</span></span>
7. <span data-ttu-id="0c2ee-115">Açıklama alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="0c2ee-115">In the Description field, type a value.</span></span>
    * <span data-ttu-id="0c2ee-116">Bu örnek için, ROUTE_2 yazın.</span><span class="sxs-lookup"><span data-stu-id="0c2ee-116">For example, type ROUTE_2.</span></span>  
8. <span data-ttu-id="0c2ee-117">Tesis alanına bir değer girin veya buradan bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="0c2ee-117">In the Site field, enter or select a value.</span></span>
    * <span data-ttu-id="0c2ee-118">Bu örnek için, Tesis 1'i girin veya seçin.</span><span class="sxs-lookup"><span data-stu-id="0c2ee-118">For this example, enter or select Site 1.</span></span>  
9. <span data-ttu-id="0c2ee-119">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="0c2ee-119">Click OK.</span></span>
10. <span data-ttu-id="0c2ee-120">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="0c2ee-120">Click New.</span></span>
11. <span data-ttu-id="0c2ee-121">Operasyon alanında bir değer girin veya bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="0c2ee-121">In the Operation field, enter or select a value.</span></span>
    * <span data-ttu-id="0c2ee-122">Bu örnek için Derleme seçeneğini belirtin.</span><span class="sxs-lookup"><span data-stu-id="0c2ee-122">For this example, select Assembly.</span></span>  
12. <span data-ttu-id="0c2ee-123">Çalışma süresi alanında bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="0c2ee-123">In the Run time field, enter a number.</span></span>
    * <span data-ttu-id="0c2ee-124">Örneğin 1 yazın.</span><span class="sxs-lookup"><span data-stu-id="0c2ee-124">For example, type 1.</span></span> <span data-ttu-id="0c2ee-125">Çalışma zamanları genellikle madde için hesaplanan fiyatın parçasıdır.</span><span class="sxs-lookup"><span data-stu-id="0c2ee-125">Run times are often part of the price that is calculated for an item.</span></span>  
13. <span data-ttu-id="0c2ee-126">Rota grubu alanında bir değer girin veya bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="0c2ee-126">In the Route group field, enter or select a value.</span></span>
    * <span data-ttu-id="0c2ee-127">Bu örnek için, Std seçeneğini belirtin.</span><span class="sxs-lookup"><span data-stu-id="0c2ee-127">For this example, select Std.</span></span>  
14. <span data-ttu-id="0c2ee-128">Kurulum sekmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="0c2ee-128">Click the Setup tab.</span></span>
15. <span data-ttu-id="0c2ee-129">Kurulum kategorisi alanında bir değer girin veya seçin.</span><span class="sxs-lookup"><span data-stu-id="0c2ee-129">In the Setup category field, enter or select a value.</span></span>
    * <span data-ttu-id="0c2ee-130">Bu örnek için Derleme seçeneğini belirtin.</span><span class="sxs-lookup"><span data-stu-id="0c2ee-130">For this example, select Assembly.</span></span>  
16. <span data-ttu-id="0c2ee-131">Zaman sekmesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="0c2ee-131">Click the Times tab.</span></span>
17. <span data-ttu-id="0c2ee-132">Hazırlık süresi alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="0c2ee-132">In the Setup time field, enter a number.</span></span>
    * <span data-ttu-id="0c2ee-133">Bu örnek için, 1 yazın.</span><span class="sxs-lookup"><span data-stu-id="0c2ee-133">For this example, type 1.</span></span> <span data-ttu-id="0c2ee-134">Kurulum zamanları genellikle madde için hesaplanan fiyatın parçasıdır.</span><span class="sxs-lookup"><span data-stu-id="0c2ee-134">Setup times are often part of the price that is calculated for an item.</span></span>  
18. <span data-ttu-id="0c2ee-135">Eylem Bölmesi'nde, Rota sürümü'ne tıklayın.</span><span class="sxs-lookup"><span data-stu-id="0c2ee-135">On the Action Pane, click Route version.</span></span>
19. <span data-ttu-id="0c2ee-136">Onayla’yı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="0c2ee-136">Click Approve.</span></span>
20. <span data-ttu-id="0c2ee-137">Rotayı da onaylamak ister misiniz? sorusunu Evet olarak yanıtlayın. alanda kullandığınızda otomatik olarak işaretlenir.</span><span class="sxs-lookup"><span data-stu-id="0c2ee-137">Select Yes in the Do you also want to approve the route? field.</span></span>
21. <span data-ttu-id="0c2ee-138">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="0c2ee-138">Click OK.</span></span>
22. <span data-ttu-id="0c2ee-139">Eylem Bölmesi'nde, Rota sürümü'ne tıklayın.</span><span class="sxs-lookup"><span data-stu-id="0c2ee-139">On the Action Pane, click Route version.</span></span>
23. <span data-ttu-id="0c2ee-140">Etkinleştir'i tıklatın.</span><span class="sxs-lookup"><span data-stu-id="0c2ee-140">Click Activate.</span></span>
24. <span data-ttu-id="0c2ee-141">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="0c2ee-141">Close the page.</span></span>
25. <span data-ttu-id="0c2ee-142">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="0c2ee-142">Close the page.</span></span>

## <a name="create-a-route-for-a-finished-product"></a><span data-ttu-id="0c2ee-143">Tamamlanmış bir ürün için rota oluşturma</span><span class="sxs-lookup"><span data-stu-id="0c2ee-143">Create a route for a finished product</span></span>
1. <span data-ttu-id="0c2ee-144">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="0c2ee-144">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="0c2ee-145">BOM_1 madde numarasını seçin.</span><span class="sxs-lookup"><span data-stu-id="0c2ee-145">Select the item number BOM_1.</span></span>  
2. <span data-ttu-id="0c2ee-146">Eylem Bölmesinde, Mühendis öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="0c2ee-146">On the Action Pane, click Engineer.</span></span>
3. <span data-ttu-id="0c2ee-147">Rota'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="0c2ee-147">Click Route.</span></span>
4. <span data-ttu-id="0c2ee-148">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="0c2ee-148">Click New.</span></span>
5. <span data-ttu-id="0c2ee-149">Rota ve rota sürümü'ne tıklayın.</span><span class="sxs-lookup"><span data-stu-id="0c2ee-149">Click Route and route version.</span></span>
6. <span data-ttu-id="0c2ee-150">Açıklama alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="0c2ee-150">In the Description field, type a value.</span></span>
    * <span data-ttu-id="0c2ee-151">Bu örnek için, ROUTE_1 yazın.</span><span class="sxs-lookup"><span data-stu-id="0c2ee-151">For this example, type ROUTE_1.</span></span>  
7. <span data-ttu-id="0c2ee-152">Tesis alanına bir değer girin veya buradan bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="0c2ee-152">In the Site field, enter or select a value.</span></span>
    * <span data-ttu-id="0c2ee-153">Bu örnek için, Tesis 1'i girin veya seçin.</span><span class="sxs-lookup"><span data-stu-id="0c2ee-153">For this example, enter or select Site 1.</span></span>  
8. <span data-ttu-id="0c2ee-154">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="0c2ee-154">Click OK.</span></span>
9. <span data-ttu-id="0c2ee-155">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="0c2ee-155">Click New.</span></span>
10. <span data-ttu-id="0c2ee-156">Operasyon alanında bir değer girin veya bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="0c2ee-156">In the Operation field, enter or select a value.</span></span>
    * <span data-ttu-id="0c2ee-157">Bu örnek için, Ambalaj seçeneğini belirtin.</span><span class="sxs-lookup"><span data-stu-id="0c2ee-157">For this example, select Packing.</span></span>  
11. <span data-ttu-id="0c2ee-158">Çalışma süresi alanında bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="0c2ee-158">In the Run time field, enter a number.</span></span>
    * <span data-ttu-id="0c2ee-159">Bu örnek için, 1 yazın.</span><span class="sxs-lookup"><span data-stu-id="0c2ee-159">For this example, type 1.</span></span>  
12. <span data-ttu-id="0c2ee-160">Rota grubu alanında bir değer girin veya bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="0c2ee-160">In the Route group field, enter or select a value.</span></span>
    * <span data-ttu-id="0c2ee-161">Bu örnek için, Std seçeneğini belirtin.</span><span class="sxs-lookup"><span data-stu-id="0c2ee-161">For this example, select Std.</span></span>  
13. <span data-ttu-id="0c2ee-162">Kurulum sekmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="0c2ee-162">Click the Setup tab.</span></span>
14. <span data-ttu-id="0c2ee-163">Kurulum kategorisi alanında bir değer girin veya seçin.</span><span class="sxs-lookup"><span data-stu-id="0c2ee-163">In the Setup category field, enter or select a value.</span></span>
    * <span data-ttu-id="0c2ee-164">Bu örnek için, Ambalaj seçeneğini belirtin.</span><span class="sxs-lookup"><span data-stu-id="0c2ee-164">For this example, select Packing.</span></span>  
15. <span data-ttu-id="0c2ee-165">Zaman sekmesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="0c2ee-165">Click the Times tab.</span></span>
16. <span data-ttu-id="0c2ee-166">Hazırlık süresi alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="0c2ee-166">In the Setup time field, enter a number.</span></span>
    * <span data-ttu-id="0c2ee-167">Bu örnek için, 1 yazın.</span><span class="sxs-lookup"><span data-stu-id="0c2ee-167">For this example, type 1.</span></span>  
17. <span data-ttu-id="0c2ee-168">Eylem Bölmesi'nde, Rota sürümü'ne tıklayın.</span><span class="sxs-lookup"><span data-stu-id="0c2ee-168">On the Action Pane, click Route version.</span></span>
18. <span data-ttu-id="0c2ee-169">Onayla’yı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="0c2ee-169">Click Approve.</span></span>
19. <span data-ttu-id="0c2ee-170">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="0c2ee-170">Click OK.</span></span>
20. <span data-ttu-id="0c2ee-171">Eylem Bölmesi'nde, Rota sürümü'ne tıklayın.</span><span class="sxs-lookup"><span data-stu-id="0c2ee-171">On the Action Pane, click Route version.</span></span>
21. <span data-ttu-id="0c2ee-172">Etkinleştir'i tıklatın.</span><span class="sxs-lookup"><span data-stu-id="0c2ee-172">Click Activate.</span></span>
22. <span data-ttu-id="0c2ee-173">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="0c2ee-173">Close the page.</span></span>
23. <span data-ttu-id="0c2ee-174">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="0c2ee-174">Close the page.</span></span>

## <a name="enable-automatic-consumption-of-setup-time"></a><span data-ttu-id="0c2ee-175">Hazırlık süresinin otomatik tüketimini etkinleştirme</span><span class="sxs-lookup"><span data-stu-id="0c2ee-175">Enable automatic consumption of setup time</span></span>
1. <span data-ttu-id="0c2ee-176">Üretim denetimi > Kurulum > Rotalar > Rota grupları öğesine gidin.</span><span class="sxs-lookup"><span data-stu-id="0c2ee-176">Go to Production control > Setup > Routes > Route groups.</span></span>
2. <span data-ttu-id="0c2ee-177">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="0c2ee-177">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="0c2ee-178">Listede, Std seçeneğini belirtin.</span><span class="sxs-lookup"><span data-stu-id="0c2ee-178">Select Std in the list.</span></span>  
3. <span data-ttu-id="0c2ee-179">Düzenle öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="0c2ee-179">Click Edit.</span></span>
4. <span data-ttu-id="0c2ee-180">Hazırlık süresi alanında, Evet'i seçin.</span><span class="sxs-lookup"><span data-stu-id="0c2ee-180">Select Yes in the Setup time field.</span></span>
    * <span data-ttu-id="0c2ee-181">Kurulum zamanları genellikle madde için hesaplanan fiyatın parçasıdır.</span><span class="sxs-lookup"><span data-stu-id="0c2ee-181">Setup times are often part of the price that is calculated for an item.</span></span>  
5. <span data-ttu-id="0c2ee-182">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="0c2ee-182">Click Save.</span></span>
6. <span data-ttu-id="0c2ee-183">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="0c2ee-183">Close the page.</span></span>


