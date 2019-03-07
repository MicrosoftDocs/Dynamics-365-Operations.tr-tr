---
title: Rotalar oluşturma (Şubat 2016)
description: Bu görev, tamamlanmış bir ürün ve yarı mamul bir ürün için üretim rotalarını oluşturmaya odaklanır.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResProductDetailsExtended, RouteInventProd, RouteGroup
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a68b28c0e0ee14429a23d3241cabdae948d706d2
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2019
ms.locfileid: "354104"
---
# <a name="create-routes-february-2016"></a><span data-ttu-id="067b2-103">Rotalar oluşturma (Şubat 2016)</span><span class="sxs-lookup"><span data-stu-id="067b2-103">Create routes (February 2016)</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="067b2-104">Bu görev, tamamlanmış bir ürün ve yarı mamul bir ürün için üretim rotalarını oluşturmaya odaklanır.</span><span class="sxs-lookup"><span data-stu-id="067b2-104">This task focuses on creating the production routes for a finished product and a semi-finished product.</span></span> <span data-ttu-id="067b2-105">Ürün reçetesi hesaplaması serisindeki beşinci görevdir.</span><span class="sxs-lookup"><span data-stu-id="067b2-105">It is the fifth task in the BOM calculation series.</span></span> <span data-ttu-id="067b2-106">Bu görevi oluşturmak için kullanılan demo veri şirketi USMF'dir.</span><span class="sxs-lookup"><span data-stu-id="067b2-106">The demo data company used to create this task is USMF.</span></span>


## <a name="create-a-route-for-a-semi-finished-product"></a><span data-ttu-id="067b2-107">Yarı mamul bir ürün için rota oluşturma</span><span class="sxs-lookup"><span data-stu-id="067b2-107">Create a route for a semi-finished product</span></span>
1. <span data-ttu-id="067b2-108">Product information management > Products > Released products (Ürün bilgi yönetimi > Ürünler > Piyasaya sürülmüş ürünler) menüsüne gidin.</span><span class="sxs-lookup"><span data-stu-id="067b2-108">Go to Product information management > Products > Released products.</span></span>
2. <span data-ttu-id="067b2-109">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="067b2-109">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="067b2-110">BOM_2 madde numarasını seçin.</span><span class="sxs-lookup"><span data-stu-id="067b2-110">Select the item number BOM_2.</span></span>  
3. <span data-ttu-id="067b2-111">Eylem Bölmesinde, Mühendis öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="067b2-111">On the Action Pane, click Engineer.</span></span>
4. <span data-ttu-id="067b2-112">Rota'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="067b2-112">Click Route.</span></span>
5. <span data-ttu-id="067b2-113">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="067b2-113">Click New.</span></span>
6. <span data-ttu-id="067b2-114">Rota ve rota sürümü'ne tıklayın.</span><span class="sxs-lookup"><span data-stu-id="067b2-114">Click Route and route version.</span></span>
7. <span data-ttu-id="067b2-115">Açıklama alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="067b2-115">In the Description field, type a value.</span></span>
    * <span data-ttu-id="067b2-116">Bu örnek için, ROUTE_2 yazın.</span><span class="sxs-lookup"><span data-stu-id="067b2-116">For example, type ROUTE_2.</span></span>  
8. <span data-ttu-id="067b2-117">Tesis alanına bir değer girin veya buradan bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="067b2-117">In the Site field, enter or select a value.</span></span>
    * <span data-ttu-id="067b2-118">Bu örnek için, Tesis 1'i girin veya seçin.</span><span class="sxs-lookup"><span data-stu-id="067b2-118">For this example, enter or select Site 1.</span></span>  
9. <span data-ttu-id="067b2-119">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="067b2-119">Click OK.</span></span>
10. <span data-ttu-id="067b2-120">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="067b2-120">Click New.</span></span>
11. <span data-ttu-id="067b2-121">Operasyon alanında bir değer girin veya bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="067b2-121">In the Operation field, enter or select a value.</span></span>
    * <span data-ttu-id="067b2-122">Bu örnek için Derleme seçeneğini belirtin.</span><span class="sxs-lookup"><span data-stu-id="067b2-122">For this example, select Assembly.</span></span>  
12. <span data-ttu-id="067b2-123">Çalışma süresi alanında bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="067b2-123">In the Run time field, enter a number.</span></span>
    * <span data-ttu-id="067b2-124">Örneğin 1 yazın.</span><span class="sxs-lookup"><span data-stu-id="067b2-124">For example, type 1.</span></span> <span data-ttu-id="067b2-125">Çalışma zamanları genellikle madde için hesaplanan fiyatın parçasıdır.</span><span class="sxs-lookup"><span data-stu-id="067b2-125">Run times are often part of the price that is calculated for an item.</span></span>  
13. <span data-ttu-id="067b2-126">Rota grubu alanında bir değer girin veya bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="067b2-126">In the Route group field, enter or select a value.</span></span>
    * <span data-ttu-id="067b2-127">Bu örnek için, Std seçeneğini belirtin.</span><span class="sxs-lookup"><span data-stu-id="067b2-127">For this example, select Std.</span></span>  
14. <span data-ttu-id="067b2-128">Kurulum sekmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="067b2-128">Click the Setup tab.</span></span>
15. <span data-ttu-id="067b2-129">Kurulum kategorisi alanında bir değer girin veya seçin.</span><span class="sxs-lookup"><span data-stu-id="067b2-129">In the Setup category field, enter or select a value.</span></span>
    * <span data-ttu-id="067b2-130">Bu örnek için Derleme seçeneğini belirtin.</span><span class="sxs-lookup"><span data-stu-id="067b2-130">For this example, select Assembly.</span></span>  
16. <span data-ttu-id="067b2-131">Zaman sekmesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="067b2-131">Click the Times tab.</span></span>
17. <span data-ttu-id="067b2-132">Hazırlık süresi alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="067b2-132">In the Setup time field, enter a number.</span></span>
    * <span data-ttu-id="067b2-133">Bu örnek için, 1 yazın.</span><span class="sxs-lookup"><span data-stu-id="067b2-133">For this example, type 1.</span></span> <span data-ttu-id="067b2-134">Kurulum zamanları genellikle madde için hesaplanan fiyatın parçasıdır.</span><span class="sxs-lookup"><span data-stu-id="067b2-134">Setup times are often part of the price that is calculated for an item.</span></span>  
18. <span data-ttu-id="067b2-135">Eylem Bölmesi'nde, Rota sürümü'ne tıklayın.</span><span class="sxs-lookup"><span data-stu-id="067b2-135">On the Action Pane, click Route version.</span></span>
19. <span data-ttu-id="067b2-136">Onayla’yı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="067b2-136">Click Approve.</span></span>
20. <span data-ttu-id="067b2-137">Rotayı da onaylamak ister misiniz? sorusunu Evet olarak yanıtlayın. alanda kullandığınızda otomatik olarak işaretlenir.</span><span class="sxs-lookup"><span data-stu-id="067b2-137">Select Yes in the Do you also want to approve the route? field.</span></span>
21. <span data-ttu-id="067b2-138">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="067b2-138">Click OK.</span></span>
22. <span data-ttu-id="067b2-139">Eylem Bölmesi'nde, Rota sürümü'ne tıklayın.</span><span class="sxs-lookup"><span data-stu-id="067b2-139">On the Action Pane, click Route version.</span></span>
23. <span data-ttu-id="067b2-140">Etkinleştir'i tıklatın.</span><span class="sxs-lookup"><span data-stu-id="067b2-140">Click Activate.</span></span>
24. <span data-ttu-id="067b2-141">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="067b2-141">Close the page.</span></span>
25. <span data-ttu-id="067b2-142">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="067b2-142">Close the page.</span></span>

## <a name="create-a-route-for-a-finished-product"></a><span data-ttu-id="067b2-143">Tamamlanmış bir ürün için rota oluşturma</span><span class="sxs-lookup"><span data-stu-id="067b2-143">Create a route for a finished product</span></span>
1. <span data-ttu-id="067b2-144">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="067b2-144">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="067b2-145">BOM_1 madde numarasını seçin.</span><span class="sxs-lookup"><span data-stu-id="067b2-145">Select the item number BOM_1.</span></span>  
2. <span data-ttu-id="067b2-146">Eylem Bölmesinde, Mühendis öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="067b2-146">On the Action Pane, click Engineer.</span></span>
3. <span data-ttu-id="067b2-147">Rota'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="067b2-147">Click Route.</span></span>
4. <span data-ttu-id="067b2-148">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="067b2-148">Click New.</span></span>
5. <span data-ttu-id="067b2-149">Rota ve rota sürümü'ne tıklayın.</span><span class="sxs-lookup"><span data-stu-id="067b2-149">Click Route and route version.</span></span>
6. <span data-ttu-id="067b2-150">Açıklama alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="067b2-150">In the Description field, type a value.</span></span>
    * <span data-ttu-id="067b2-151">Bu örnek için, ROUTE_1 yazın.</span><span class="sxs-lookup"><span data-stu-id="067b2-151">For this example, type ROUTE_1.</span></span>  
7. <span data-ttu-id="067b2-152">Tesis alanına bir değer girin veya buradan bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="067b2-152">In the Site field, enter or select a value.</span></span>
    * <span data-ttu-id="067b2-153">Bu örnek için, Tesis 1'i girin veya seçin.</span><span class="sxs-lookup"><span data-stu-id="067b2-153">For this example, enter or select Site 1.</span></span>  
8. <span data-ttu-id="067b2-154">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="067b2-154">Click OK.</span></span>
9. <span data-ttu-id="067b2-155">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="067b2-155">Click New.</span></span>
10. <span data-ttu-id="067b2-156">Operasyon alanında bir değer girin veya bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="067b2-156">In the Operation field, enter or select a value.</span></span>
    * <span data-ttu-id="067b2-157">Bu örnek için, Ambalaj seçeneğini belirtin.</span><span class="sxs-lookup"><span data-stu-id="067b2-157">For this example, select Packing.</span></span>  
11. <span data-ttu-id="067b2-158">Çalışma süresi alanında bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="067b2-158">In the Run time field, enter a number.</span></span>
    * <span data-ttu-id="067b2-159">Bu örnek için, 1 yazın.</span><span class="sxs-lookup"><span data-stu-id="067b2-159">For this example, type 1.</span></span>  
12. <span data-ttu-id="067b2-160">Rota grubu alanında bir değer girin veya bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="067b2-160">In the Route group field, enter or select a value.</span></span>
    * <span data-ttu-id="067b2-161">Bu örnek için, Std seçeneğini belirtin.</span><span class="sxs-lookup"><span data-stu-id="067b2-161">For this example, select Std.</span></span>  
13. <span data-ttu-id="067b2-162">Kurulum sekmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="067b2-162">Click the Setup tab.</span></span>
14. <span data-ttu-id="067b2-163">Kurulum kategorisi alanında bir değer girin veya seçin.</span><span class="sxs-lookup"><span data-stu-id="067b2-163">In the Setup category field, enter or select a value.</span></span>
    * <span data-ttu-id="067b2-164">Bu örnek için, Ambalaj seçeneğini belirtin.</span><span class="sxs-lookup"><span data-stu-id="067b2-164">For this example, select Packing.</span></span>  
15. <span data-ttu-id="067b2-165">Zaman sekmesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="067b2-165">Click the Times tab.</span></span>
16. <span data-ttu-id="067b2-166">Hazırlık süresi alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="067b2-166">In the Setup time field, enter a number.</span></span>
    * <span data-ttu-id="067b2-167">Bu örnek için, 1 yazın.</span><span class="sxs-lookup"><span data-stu-id="067b2-167">For this example, type 1.</span></span>  
17. <span data-ttu-id="067b2-168">Eylem Bölmesi'nde, Rota sürümü'ne tıklayın.</span><span class="sxs-lookup"><span data-stu-id="067b2-168">On the Action Pane, click Route version.</span></span>
18. <span data-ttu-id="067b2-169">Onayla’yı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="067b2-169">Click Approve.</span></span>
19. <span data-ttu-id="067b2-170">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="067b2-170">Click OK.</span></span>
20. <span data-ttu-id="067b2-171">Eylem Bölmesi'nde, Rota sürümü'ne tıklayın.</span><span class="sxs-lookup"><span data-stu-id="067b2-171">On the Action Pane, click Route version.</span></span>
21. <span data-ttu-id="067b2-172">Etkinleştir'i tıklatın.</span><span class="sxs-lookup"><span data-stu-id="067b2-172">Click Activate.</span></span>
22. <span data-ttu-id="067b2-173">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="067b2-173">Close the page.</span></span>
23. <span data-ttu-id="067b2-174">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="067b2-174">Close the page.</span></span>

## <a name="enable-automatic-consumption-of-setup-time"></a><span data-ttu-id="067b2-175">Hazırlık süresinin otomatik tüketimini etkinleştirme</span><span class="sxs-lookup"><span data-stu-id="067b2-175">Enable automatic consumption of setup time</span></span>
1. <span data-ttu-id="067b2-176">Üretim denetimi > Kurulum > Rotalar > Rota grupları öğesine gidin.</span><span class="sxs-lookup"><span data-stu-id="067b2-176">Go to Production control > Setup > Routes > Route groups.</span></span>
2. <span data-ttu-id="067b2-177">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="067b2-177">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="067b2-178">Listede, Std seçeneğini belirtin.</span><span class="sxs-lookup"><span data-stu-id="067b2-178">Select Std in the list.</span></span>  
3. <span data-ttu-id="067b2-179">Düzenle öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="067b2-179">Click Edit.</span></span>
4. <span data-ttu-id="067b2-180">Hazırlık süresi alanında, Evet'i seçin.</span><span class="sxs-lookup"><span data-stu-id="067b2-180">Select Yes in the Setup time field.</span></span>
    * <span data-ttu-id="067b2-181">Kurulum zamanları genellikle madde için hesaplanan fiyatın parçasıdır.</span><span class="sxs-lookup"><span data-stu-id="067b2-181">Setup times are often part of the price that is calculated for an item.</span></span>  
5. <span data-ttu-id="067b2-182">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="067b2-182">Click Save.</span></span>
6. <span data-ttu-id="067b2-183">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="067b2-183">Close the page.</span></span>

