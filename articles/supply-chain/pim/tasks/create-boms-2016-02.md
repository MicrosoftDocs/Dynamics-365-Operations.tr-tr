--- 
title: "Ürün reçeteleri oluşturma (Şubat 2016)"
description: "Bu görev, tamamlanmış bir ürün ve yarı mamul bir ürün için ürün reçetesi yapısını oluşturmaya odaklanır."
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: EcoResProductDetailsExtended, BOMConsistOf, BOMTable, InventLocationIdLookup
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0312b8cfadd45f8e59225e9daba78b9e216cff51
ms.openlocfilehash: 6c5cfb8aae1a61d14f7a7969f688cb282530840d
ms.contentlocale: tr-tr
ms.lasthandoff: 09/14/2018

---
# <a name="create-boms-february-2016"></a><span data-ttu-id="c31b3-103">Ürün reçeteleri oluşturma (Şubat 2016)</span><span class="sxs-lookup"><span data-stu-id="c31b3-103">Create BOMs (February 2016)</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="c31b3-104">Bu görev, tamamlanmış bir ürün ve yarı mamul bir ürün için ürün reçetesi yapısını oluşturmaya odaklanır.</span><span class="sxs-lookup"><span data-stu-id="c31b3-104">This task focuses on creating the bill of materials structure for a finished product and a semi-finished product.</span></span> <span data-ttu-id="c31b3-105">Ürün reçetesi hesaplaması serisindeki dördüncü görevdir.</span><span class="sxs-lookup"><span data-stu-id="c31b3-105">It is the fourth task in the BOM calculation series.</span></span> <span data-ttu-id="c31b3-106">Bu görevi oluşturmak için kullanılan demo veri şirketi USMF'dir.</span><span class="sxs-lookup"><span data-stu-id="c31b3-106">The demo data company used to create this task is USMF.</span></span>


## <a name="create-bom-for-a-semi-finished-product"></a><span data-ttu-id="c31b3-107">Yarı mamul bir ürün için ürün reçetesi oluşturma</span><span class="sxs-lookup"><span data-stu-id="c31b3-107">Create BOM for a semi-finished product</span></span>
1. <span data-ttu-id="c31b3-108">Product information management > Products > Released products (Ürün bilgi yönetimi > Ürünler > Piyasaya sürülmüş ürünler) menüsüne gidin.</span><span class="sxs-lookup"><span data-stu-id="c31b3-108">Go to Product information management > Products > Released products.</span></span>
2. <span data-ttu-id="c31b3-109">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="c31b3-109">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="c31b3-110">BOM_2 madde numarasını seçin.</span><span class="sxs-lookup"><span data-stu-id="c31b3-110">Select the item number BOM_2.</span></span>  
3. <span data-ttu-id="c31b3-111">Eylem Bölmesinde, Mühendis öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="c31b3-111">On the Action Pane, click Engineer.</span></span>
4. <span data-ttu-id="c31b3-112">BOM sürümlerini tıklayın.</span><span class="sxs-lookup"><span data-stu-id="c31b3-112">Click BOM versions.</span></span>
5. <span data-ttu-id="c31b3-113">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="c31b3-113">Click New.</span></span>
6. <span data-ttu-id="c31b3-114">BOM ve BOM sürümünü tıklayın.</span><span class="sxs-lookup"><span data-stu-id="c31b3-114">Click BOM and BOM version.</span></span>
7. <span data-ttu-id="c31b3-115">İsim alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="c31b3-115">In the Name field, type a value.</span></span>
    * <span data-ttu-id="c31b3-116">Örneğin, BOM_2 yazın.</span><span class="sxs-lookup"><span data-stu-id="c31b3-116">For example, type BOM_2.</span></span>  
8. <span data-ttu-id="c31b3-117">Tesis alanına bir değer girin veya buradan bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="c31b3-117">In the Site field, enter or select a value.</span></span>
    * <span data-ttu-id="c31b3-118">Bu örnek için, Tesis 1'i girin veya seçin.</span><span class="sxs-lookup"><span data-stu-id="c31b3-118">For this example, enter or select Site 1.</span></span>  
9. <span data-ttu-id="c31b3-119">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="c31b3-119">Click OK.</span></span>
10. <span data-ttu-id="c31b3-120">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="c31b3-120">Click New.</span></span>
11. <span data-ttu-id="c31b3-121">Madde numarası alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="c31b3-121">In the Item number field, type a value.</span></span>
    * <span data-ttu-id="c31b3-122">Bu örnek için, ITEM_C yazın.</span><span class="sxs-lookup"><span data-stu-id="c31b3-122">For this example, type ITEM_C.</span></span>  
12. <span data-ttu-id="c31b3-123">Ambar alanında bir değer girin veya bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="c31b3-123">In the Warehouse field, enter or select a value.</span></span>
    * <span data-ttu-id="c31b3-124">Bu örnek için, 11'i girin veya seçin.</span><span class="sxs-lookup"><span data-stu-id="c31b3-124">For this example, enter or select 11.</span></span>  
13. <span data-ttu-id="c31b3-125">Başlık'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="c31b3-125">Click Header.</span></span>
14. <span data-ttu-id="c31b3-126">Ürün reçetelerini onaylamak için Onay'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="c31b3-126">Click Approval to approve bills of materials.</span></span>
15. <span data-ttu-id="c31b3-127">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="c31b3-127">Click OK.</span></span>
16. <span data-ttu-id="c31b3-128">Onayla’yı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="c31b3-128">Click Approve.</span></span>
    * <span data-ttu-id="c31b3-129">Onayla düğmesi Ürün reçetesi sürümleri bölümündeki Araç Çubuğu'nda yer almaktadır.</span><span class="sxs-lookup"><span data-stu-id="c31b3-129">The Approve button is on the ToolBar in the  BOM versions section.</span></span> <span data-ttu-id="c31b3-130">Görünmez ise, Onayla düğmesini görüntülemek için Ürün reçeteleri sayfasının sağ üst kısmında Başlık'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="c31b3-130">If it is invisible, click Header at the upper right of the Bills of materials page to display Approve.</span></span>  
17. <span data-ttu-id="c31b3-131">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="c31b3-131">Click OK.</span></span>
18. <span data-ttu-id="c31b3-132">Etkinleştir'i tıklatın.</span><span class="sxs-lookup"><span data-stu-id="c31b3-132">Click Activate.</span></span>
19. <span data-ttu-id="c31b3-133">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="c31b3-133">Close the page.</span></span>
20. <span data-ttu-id="c31b3-134">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="c31b3-134">Close the page.</span></span>
21. <span data-ttu-id="c31b3-135">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="c31b3-135">Close the page.</span></span>

## <a name="create-bom-for-a-finished-product"></a><span data-ttu-id="c31b3-136">Tamamlanmış bir ürün için ürün reçetesi oluşturma</span><span class="sxs-lookup"><span data-stu-id="c31b3-136">Create BOM for a finished product</span></span>
1. <span data-ttu-id="c31b3-137">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="c31b3-137">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="c31b3-138">BOM_1 madde numarasını seçin.</span><span class="sxs-lookup"><span data-stu-id="c31b3-138">Select the item number BOM_1.</span></span>  
2. <span data-ttu-id="c31b3-139">Eylem Bölmesinde, Mühendis öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="c31b3-139">On the Action Pane, click Engineer.</span></span>
3. <span data-ttu-id="c31b3-140">BOM sürümlerini tıklayın.</span><span class="sxs-lookup"><span data-stu-id="c31b3-140">Click BOM versions.</span></span>
4. <span data-ttu-id="c31b3-141">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="c31b3-141">Click New.</span></span>
5. <span data-ttu-id="c31b3-142">BOM ve BOM sürümünü tıklayın.</span><span class="sxs-lookup"><span data-stu-id="c31b3-142">Click BOM and BOM version.</span></span>
6. <span data-ttu-id="c31b3-143">İsim alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="c31b3-143">In the Name field, type a value.</span></span>
    * <span data-ttu-id="c31b3-144">Örneğin, BOM_1 yazın.</span><span class="sxs-lookup"><span data-stu-id="c31b3-144">For example, type BOM_1.</span></span>  
7. <span data-ttu-id="c31b3-145">Tesis alanına bir değer girin veya buradan bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="c31b3-145">In the Site field, enter or select a value.</span></span>
    * <span data-ttu-id="c31b3-146">Bu örnek için, Tesis 1'i girin veya seçin.</span><span class="sxs-lookup"><span data-stu-id="c31b3-146">For this example, enter or select Site 1.</span></span>  
8. <span data-ttu-id="c31b3-147">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="c31b3-147">Click OK.</span></span>
9. <span data-ttu-id="c31b3-148">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="c31b3-148">Click New.</span></span>
10. <span data-ttu-id="c31b3-149">Madde numarası alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="c31b3-149">In the Item number field, type a value.</span></span>
    * <span data-ttu-id="c31b3-150">Bu örnek için, ITEM_A yazın.</span><span class="sxs-lookup"><span data-stu-id="c31b3-150">For this example, type ITEM_A.</span></span>  
11. <span data-ttu-id="c31b3-151">Ambar alanında bir değer girin veya bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="c31b3-151">In the Warehouse field, enter or select a value.</span></span>
    * <span data-ttu-id="c31b3-152">Bu örnek için, 11'i seçin.</span><span class="sxs-lookup"><span data-stu-id="c31b3-152">For this example, select 11.</span></span>  
12. <span data-ttu-id="c31b3-153">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="c31b3-153">Click New.</span></span>
13. <span data-ttu-id="c31b3-154">Madde numarası alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="c31b3-154">In the Item number field, type a value.</span></span>
    * <span data-ttu-id="c31b3-155">Bu örnek için, ITEM_B yazın.</span><span class="sxs-lookup"><span data-stu-id="c31b3-155">For this example, type ITEM_B.</span></span>  
14. <span data-ttu-id="c31b3-156">Ambar alanında bir değer girin veya bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="c31b3-156">In the Warehouse field, enter or select a value.</span></span>
    * <span data-ttu-id="c31b3-157">Bu örnek için, 11'i girin veya seçin.</span><span class="sxs-lookup"><span data-stu-id="c31b3-157">For this example, enter or select 11.</span></span>  
15. <span data-ttu-id="c31b3-158">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="c31b3-158">Click New.</span></span>
16. <span data-ttu-id="c31b3-159">Madde numarası alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="c31b3-159">In the Item number field, type a value.</span></span>
    * <span data-ttu-id="c31b3-160">Bu örnek için BOM_2 yazın.</span><span class="sxs-lookup"><span data-stu-id="c31b3-160">For this example, type BOM_2.</span></span>  
17. <span data-ttu-id="c31b3-161">Listede, seçili satırı işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="c31b3-161">In the list, mark the selected row.</span></span>
18. <span data-ttu-id="c31b3-162">Ambar alanında bir değer girin veya bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="c31b3-162">In the Warehouse field, enter or select a value.</span></span>
    * <span data-ttu-id="c31b3-163">Bu örnek için, ambar 11'i girin veya seçin.</span><span class="sxs-lookup"><span data-stu-id="c31b3-163">For this example, enter or select warehouse 11.</span></span>  
19. <span data-ttu-id="c31b3-164">Başlık'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="c31b3-164">Click Header.</span></span>
20. <span data-ttu-id="c31b3-165">Ürün reçetelerini onaylamak için Onay'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="c31b3-165">Click Approval to approve bills of materials.</span></span>
21. <span data-ttu-id="c31b3-166">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="c31b3-166">Click OK.</span></span>
22. <span data-ttu-id="c31b3-167">Onayla’yı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="c31b3-167">Click Approve.</span></span>
    * <span data-ttu-id="c31b3-168">Onayla düğmesi Ürün reçetesi sürümleri bölümündeki Araç Çubuğu'nda yer almaktadır.</span><span class="sxs-lookup"><span data-stu-id="c31b3-168">The Approve button is on the ToolBar in the  BOM versions section.</span></span> <span data-ttu-id="c31b3-169">Görünmez ise, Onayla düğmesini görüntülemek için Ürün reçeteleri sayfasının sağ üst kısmında Başlık'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="c31b3-169">If it is invisible, click Header at the upper right of the Bills of materials page to display Approve.</span></span>  
23. <span data-ttu-id="c31b3-170">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="c31b3-170">Click OK.</span></span>
24. <span data-ttu-id="c31b3-171">Etkinleştir'i tıklatın.</span><span class="sxs-lookup"><span data-stu-id="c31b3-171">Click Activate.</span></span>
25. <span data-ttu-id="c31b3-172">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="c31b3-172">Close the page.</span></span>
26. <span data-ttu-id="c31b3-173">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="c31b3-173">Close the page.</span></span>
27. <span data-ttu-id="c31b3-174">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="c31b3-174">Close the page.</span></span>


