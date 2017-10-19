--- 
title: "Ürün reçeteleri oluşturma (yalnızca Şubat 2016)"
description: "Bu görev, tamamlanmış bir ürün ve yarı mamul bir ürün için ürün reçetesi yapısını oluşturmaya odaklanır."
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
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: f8ad4b0e230fb0f018355e486e3b898895a61f28
ms.contentlocale: tr-tr
ms.lasthandoff: 08/29/2017

---
# <a name="create-boms-february-2016-only"></a><span data-ttu-id="96905-103">Ürün reçeteleri oluşturma (yalnızca Şubat 2016)</span><span class="sxs-lookup"><span data-stu-id="96905-103">Create BOMs (February 2016 only)</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="96905-104">Bu görev, tamamlanmış bir ürün ve yarı mamul bir ürün için ürün reçetesi yapısını oluşturmaya odaklanır.</span><span class="sxs-lookup"><span data-stu-id="96905-104">This task focuses on creating the bill of materials structure for a finished product and a semi-finished product.</span></span> <span data-ttu-id="96905-105">Ürün reçetesi hesaplaması serisindeki dördüncü görevdir.</span><span class="sxs-lookup"><span data-stu-id="96905-105">It is the fourth task in the BOM calculation series.</span></span> <span data-ttu-id="96905-106">Bu görevi oluşturmak için kullanılan demo veri şirketi USMF'dir.</span><span class="sxs-lookup"><span data-stu-id="96905-106">The demo data company used to create this task is USMF.</span></span>


## <a name="create-bom-for-a-semi-finished-product"></a><span data-ttu-id="96905-107">Yarı mamul bir ürün için ürün reçetesi oluşturma</span><span class="sxs-lookup"><span data-stu-id="96905-107">Create BOM for a semi-finished product</span></span>
1. <span data-ttu-id="96905-108">Product information management > Products > Released products (Ürün bilgi yönetimi > Ürünler > Piyasaya sürülmüş ürünler) menüsüne gidin.</span><span class="sxs-lookup"><span data-stu-id="96905-108">Go to Product information management > Products > Released products.</span></span>
2. <span data-ttu-id="96905-109">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="96905-109">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="96905-110">BOM_2 madde numarasını seçin.</span><span class="sxs-lookup"><span data-stu-id="96905-110">Select the item number BOM_2.</span></span>  
3. <span data-ttu-id="96905-111">Eylem Bölmesinde, Mühendis öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="96905-111">On the Action Pane, click Engineer.</span></span>
4. <span data-ttu-id="96905-112">BOM sürümlerini tıklayın.</span><span class="sxs-lookup"><span data-stu-id="96905-112">Click BOM versions.</span></span>
5. <span data-ttu-id="96905-113">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="96905-113">Click New.</span></span>
6. <span data-ttu-id="96905-114">BOM ve BOM sürümünü tıklayın.</span><span class="sxs-lookup"><span data-stu-id="96905-114">Click BOM and BOM version.</span></span>
7. <span data-ttu-id="96905-115">İsim alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="96905-115">In the Name field, type a value.</span></span>
    * <span data-ttu-id="96905-116">Örneğin, BOM_2 yazın.</span><span class="sxs-lookup"><span data-stu-id="96905-116">For example, type BOM_2.</span></span>  
8. <span data-ttu-id="96905-117">Tesis alanına bir değer girin veya buradan bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="96905-117">In the Site field, enter or select a value.</span></span>
    * <span data-ttu-id="96905-118">Bu örnek için, Tesis 1'i girin veya seçin.</span><span class="sxs-lookup"><span data-stu-id="96905-118">For this example, enter or select Site 1.</span></span>  
9. <span data-ttu-id="96905-119">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="96905-119">Click OK.</span></span>
10. <span data-ttu-id="96905-120">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="96905-120">Click New.</span></span>
11. <span data-ttu-id="96905-121">Madde numarası alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="96905-121">In the Item number field, type a value.</span></span>
    * <span data-ttu-id="96905-122">Bu örnek için, ITEM_C yazın.</span><span class="sxs-lookup"><span data-stu-id="96905-122">For this example, type ITEM_C.</span></span>  
12. <span data-ttu-id="96905-123">Ambar alanında bir değer girin veya bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="96905-123">In the Warehouse field, enter or select a value.</span></span>
    * <span data-ttu-id="96905-124">Bu örnek için, 11'i girin veya seçin.</span><span class="sxs-lookup"><span data-stu-id="96905-124">For this example, enter or select 11.</span></span>  
13. <span data-ttu-id="96905-125">Başlık'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="96905-125">Click Header.</span></span>
14. <span data-ttu-id="96905-126">Ürün reçetelerini onaylamak için Onay'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="96905-126">Click Approval to approve bills of materials.</span></span>
15. <span data-ttu-id="96905-127">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="96905-127">Click OK.</span></span>
16. <span data-ttu-id="96905-128">Onayla’yı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="96905-128">Click Approve.</span></span>
    * <span data-ttu-id="96905-129">Onayla düğmesi Ürün reçetesi sürümleri bölümündeki Araç Çubuğu'nda yer almaktadır.</span><span class="sxs-lookup"><span data-stu-id="96905-129">The Approve button is on the ToolBar in the  BOM versions section.</span></span> <span data-ttu-id="96905-130">Görünmez ise, Onayla düğmesini görüntülemek için Ürün reçeteleri sayfasının sağ üst kısmında Başlık'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="96905-130">If it is invisible, click Header at the upper right of the Bills of materials page to display Approve.</span></span>  
17. <span data-ttu-id="96905-131">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="96905-131">Click OK.</span></span>
18. <span data-ttu-id="96905-132">Etkinleştir'i tıklatın.</span><span class="sxs-lookup"><span data-stu-id="96905-132">Click Activate.</span></span>
19. <span data-ttu-id="96905-133">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="96905-133">Close the page.</span></span>
20. <span data-ttu-id="96905-134">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="96905-134">Close the page.</span></span>
21. <span data-ttu-id="96905-135">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="96905-135">Close the page.</span></span>

## <a name="create-bom-for-a-finished-product"></a><span data-ttu-id="96905-136">Tamamlanmış bir ürün için ürün reçetesi oluşturma</span><span class="sxs-lookup"><span data-stu-id="96905-136">Create BOM for a finished product</span></span>
1. <span data-ttu-id="96905-137">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="96905-137">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="96905-138">BOM_1 madde numarasını seçin.</span><span class="sxs-lookup"><span data-stu-id="96905-138">Select the item number BOM_1.</span></span>  
2. <span data-ttu-id="96905-139">Eylem Bölmesinde, Mühendis öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="96905-139">On the Action Pane, click Engineer.</span></span>
3. <span data-ttu-id="96905-140">BOM sürümlerini tıklayın.</span><span class="sxs-lookup"><span data-stu-id="96905-140">Click BOM versions.</span></span>
4. <span data-ttu-id="96905-141">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="96905-141">Click New.</span></span>
5. <span data-ttu-id="96905-142">BOM ve BOM sürümünü tıklayın.</span><span class="sxs-lookup"><span data-stu-id="96905-142">Click BOM and BOM version.</span></span>
6. <span data-ttu-id="96905-143">İsim alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="96905-143">In the Name field, type a value.</span></span>
    * <span data-ttu-id="96905-144">Örneğin, BOM_1 yazın.</span><span class="sxs-lookup"><span data-stu-id="96905-144">For example, type BOM_1.</span></span>  
7. <span data-ttu-id="96905-145">Tesis alanına bir değer girin veya buradan bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="96905-145">In the Site field, enter or select a value.</span></span>
    * <span data-ttu-id="96905-146">Bu örnek için, Tesis 1'i girin veya seçin.</span><span class="sxs-lookup"><span data-stu-id="96905-146">For this example, enter or select Site 1.</span></span>  
8. <span data-ttu-id="96905-147">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="96905-147">Click OK.</span></span>
9. <span data-ttu-id="96905-148">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="96905-148">Click New.</span></span>
10. <span data-ttu-id="96905-149">Madde numarası alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="96905-149">In the Item number field, type a value.</span></span>
    * <span data-ttu-id="96905-150">Bu örnek için, ITEM_A yazın.</span><span class="sxs-lookup"><span data-stu-id="96905-150">For this example, type ITEM_A.</span></span>  
11. <span data-ttu-id="96905-151">Ambar alanında bir değer girin veya bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="96905-151">In the Warehouse field, enter or select a value.</span></span>
    * <span data-ttu-id="96905-152">Bu örnek için, 11'i seçin.</span><span class="sxs-lookup"><span data-stu-id="96905-152">For this example, select 11.</span></span>  
12. <span data-ttu-id="96905-153">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="96905-153">Click New.</span></span>
13. <span data-ttu-id="96905-154">Madde numarası alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="96905-154">In the Item number field, type a value.</span></span>
    * <span data-ttu-id="96905-155">Bu örnek için, ITEM_B yazın.</span><span class="sxs-lookup"><span data-stu-id="96905-155">For this example, type ITEM_B.</span></span>  
14. <span data-ttu-id="96905-156">Ambar alanında bir değer girin veya bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="96905-156">In the Warehouse field, enter or select a value.</span></span>
    * <span data-ttu-id="96905-157">Bu örnek için, 11'i girin veya seçin.</span><span class="sxs-lookup"><span data-stu-id="96905-157">For this example, enter or select 11.</span></span>  
15. <span data-ttu-id="96905-158">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="96905-158">Click New.</span></span>
16. <span data-ttu-id="96905-159">Madde numarası alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="96905-159">In the Item number field, type a value.</span></span>
    * <span data-ttu-id="96905-160">Bu örnek için BOM_2 yazın.</span><span class="sxs-lookup"><span data-stu-id="96905-160">For this example, type BOM_2.</span></span>  
17. <span data-ttu-id="96905-161">Listede, seçili satırı işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="96905-161">In the list, mark the selected row.</span></span>
18. <span data-ttu-id="96905-162">Ambar alanında bir değer girin veya bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="96905-162">In the Warehouse field, enter or select a value.</span></span>
    * <span data-ttu-id="96905-163">Bu örnek için, ambar 11'i girin veya seçin.</span><span class="sxs-lookup"><span data-stu-id="96905-163">For this example, enter or select warehouse 11.</span></span>  
19. <span data-ttu-id="96905-164">Başlık'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="96905-164">Click Header.</span></span>
20. <span data-ttu-id="96905-165">Ürün reçetelerini onaylamak için Onay'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="96905-165">Click Approval to approve bills of materials.</span></span>
21. <span data-ttu-id="96905-166">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="96905-166">Click OK.</span></span>
22. <span data-ttu-id="96905-167">Onayla’yı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="96905-167">Click Approve.</span></span>
    * <span data-ttu-id="96905-168">Onayla düğmesi Ürün reçetesi sürümleri bölümündeki Araç Çubuğu'nda yer almaktadır.</span><span class="sxs-lookup"><span data-stu-id="96905-168">The Approve button is on the ToolBar in the  BOM versions section.</span></span> <span data-ttu-id="96905-169">Görünmez ise, Onayla düğmesini görüntülemek için Ürün reçeteleri sayfasının sağ üst kısmında Başlık'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="96905-169">If it is invisible, click Header at the upper right of the Bills of materials page to display Approve.</span></span>  
23. <span data-ttu-id="96905-170">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="96905-170">Click OK.</span></span>
24. <span data-ttu-id="96905-171">Etkinleştir'i tıklatın.</span><span class="sxs-lookup"><span data-stu-id="96905-171">Click Activate.</span></span>
25. <span data-ttu-id="96905-172">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="96905-172">Close the page.</span></span>
26. <span data-ttu-id="96905-173">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="96905-173">Close the page.</span></span>
27. <span data-ttu-id="96905-174">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="96905-174">Close the page.</span></span>


