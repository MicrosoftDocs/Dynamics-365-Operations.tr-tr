--- 
title: "Yapılandırılmış ürün çeşitleri için ürün numarası terminolojisi oluşturma"
description: "Bu yordam, yapılandırılmış ürün çeşitleri için bir ürün numara terminolojisinin nasıl ayarlanacağını ve yapılandırılabilir bir ana ürüne nasıl eklenebileceğini gösterir."
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, EcoResNomenclature, EcoResProductListPage, EcoResProductDetails, PCProductConfigurationModelListPage, PCProductConfigurationModelDetails
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0312b8cfadd45f8e59225e9daba78b9e216cff51
ms.openlocfilehash: 800afdf075f0675185514158f3b712a0fe7675e3
ms.contentlocale: tr-tr
ms.lasthandoff: 09/14/2018

---
# <a name="create-a-product-number-nomenclature-for-configured-product-variants"></a><span data-ttu-id="bdb3c-103">Yapılandırılmış ürün çeşitleri için ürün numarası terminolojisi oluşturma</span><span class="sxs-lookup"><span data-stu-id="bdb3c-103">Create a product number nomenclature for configured product variants</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="bdb3c-104">Bu yordam, yapılandırılmış ürün çeşitleri için bir ürün numara terminolojisinin nasıl ayarlanacağını ve yapılandırılabilir bir ana ürüne nasıl eklenebileceğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="bdb3c-104">This procedure shows you how to set up a product number nomenclature for configured product variants, and how it can be attached to a configurable product master.</span></span> <span data-ttu-id="bdb3c-105">Bu yordam ayrıca bir ürün yapılandırma model bileşeni için bir yapılandırma terminolojisini nasıl oluşturabileceğinizi de gösterir.</span><span class="sxs-lookup"><span data-stu-id="bdb3c-105">This procedure also demonstrates how you can build a configuration nomenclature for a product configuration model component.</span></span> <span data-ttu-id="bdb3c-106">Bu yöntemi oluşturmak için kullanılan demo veri şirketi USMF'dir.</span><span class="sxs-lookup"><span data-stu-id="bdb3c-106">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="bdb3c-107">Yeni ürün numarası terminolojisi D0004 ana ürününe atanmıştır.</span><span class="sxs-lookup"><span data-stu-id="bdb3c-107">The new product number nomenclature is assigned to the D0004 product master.</span></span> <span data-ttu-id="bdb3c-108">Bu görev genellikle bir ürün tasarımcısı tarafından gerçekleştirilir.</span><span class="sxs-lookup"><span data-stu-id="bdb3c-108">This task would typically be done by a product designer.</span></span>


## <a name="create-a-product-number-nomenclature"></a><span data-ttu-id="bdb3c-109">Ürün numara terminolojisi oluşturma</span><span class="sxs-lookup"><span data-stu-id="bdb3c-109">Create a product number nomenclature</span></span>
1. <span data-ttu-id="bdb3c-110">Ürün varyantı model tanımı'na tıklayın.</span><span class="sxs-lookup"><span data-stu-id="bdb3c-110">Click Product variant model definition.</span></span>
2. <span data-ttu-id="bdb3c-111">Ürün terminolojisi'ne tıklayın.</span><span class="sxs-lookup"><span data-stu-id="bdb3c-111">Click Product nomenclature.</span></span>
3. <span data-ttu-id="bdb3c-112">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="bdb3c-112">Click New.</span></span>
4. <span data-ttu-id="bdb3c-113">İsim alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="bdb3c-113">In the Name field, type a value.</span></span>
5. <span data-ttu-id="bdb3c-114">Açıklama alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="bdb3c-114">In the Description field, type a value.</span></span>
6. <span data-ttu-id="bdb3c-115">Ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="bdb3c-115">Click Add.</span></span>
7. <span data-ttu-id="bdb3c-116">Ana ürün numarası'na tıklayın.</span><span class="sxs-lookup"><span data-stu-id="bdb3c-116">Click Product master number.</span></span>
8. <span data-ttu-id="bdb3c-117">Ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="bdb3c-117">Click Add.</span></span>
9. <span data-ttu-id="bdb3c-118">Metin sabiti'ne tıklayın.</span><span class="sxs-lookup"><span data-stu-id="bdb3c-118">Click Text constant.</span></span>
10. <span data-ttu-id="bdb3c-119">Listede, seçili satırı işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="bdb3c-119">In the list, mark the selected row.</span></span>
11. <span data-ttu-id="bdb3c-120">Metin alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="bdb3c-120">In the Text field, type a value.</span></span>
12. <span data-ttu-id="bdb3c-121">Ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="bdb3c-121">Click Add.</span></span>
13. <span data-ttu-id="bdb3c-122">Yapılandırma'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="bdb3c-122">Click Configuration.</span></span>
14. <span data-ttu-id="bdb3c-123">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="bdb3c-123">Close the page.</span></span>

## <a name="assign-the-product-number-nomenclature-to-a-product-master"></a><span data-ttu-id="bdb3c-124">Ana ürüne, ürün numara terminolojisi atama</span><span class="sxs-lookup"><span data-stu-id="bdb3c-124">Assign the product number nomenclature to a product master</span></span>
1. <span data-ttu-id="bdb3c-125">Ana ürünler'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="bdb3c-125">Click Product masters.</span></span>
2. <span data-ttu-id="bdb3c-126">Kayıtları bulmak için Hızlı Filtre'yi kullanın.</span><span class="sxs-lookup"><span data-stu-id="bdb3c-126">Use the Quick Filter to find records.</span></span> <span data-ttu-id="bdb3c-127">Örneğin, Ürün numarası alanında "D" değeriyle filtreleyin.</span><span class="sxs-lookup"><span data-stu-id="bdb3c-127">For example, filter on the Product number field with a value of 'D'.</span></span>
3. <span data-ttu-id="bdb3c-128">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="bdb3c-128">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="bdb3c-129">Düzenle'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="bdb3c-129">Click Edit.</span></span>
5. <span data-ttu-id="bdb3c-130">Terminoloji kullan alanında Evet'i seçin.</span><span class="sxs-lookup"><span data-stu-id="bdb3c-130">Select Yes in the Use nomenclature field.</span></span>
6. <span data-ttu-id="bdb3c-131">Ürün çeşidi numara terminolojisi alanında bir değer girin veya seçin.</span><span class="sxs-lookup"><span data-stu-id="bdb3c-131">In the Product variant number nomenclature field, enter or select a value.</span></span>
7. <span data-ttu-id="bdb3c-132">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="bdb3c-132">Close the page.</span></span>
8. <span data-ttu-id="bdb3c-133">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="bdb3c-133">Close the page.</span></span>

## <a name="create-nomenclature-for-a-product-configuration-model-component"></a><span data-ttu-id="bdb3c-134">Ürün yapılandırma model bileşeni için terminoloji oluşturma</span><span class="sxs-lookup"><span data-stu-id="bdb3c-134">Create nomenclature for a product configuration model component</span></span>
1. <span data-ttu-id="bdb3c-135">Ürün yapılandırma modelleri'ne tıklayın.</span><span class="sxs-lookup"><span data-stu-id="bdb3c-135">Click Product configuration models.</span></span>
2. <span data-ttu-id="bdb3c-136">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="bdb3c-136">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="bdb3c-137">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="bdb3c-137">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="bdb3c-138">Düzenle'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="bdb3c-138">Click Edit.</span></span>
5. <span data-ttu-id="bdb3c-139">Konfigürasyon terminolojisini kullan alanında Evet'i seçin.</span><span class="sxs-lookup"><span data-stu-id="bdb3c-139">Select Yes in the Use configuration nomenclature field.</span></span>
6. <span data-ttu-id="bdb3c-140">Ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="bdb3c-140">Click Add.</span></span>
7. <span data-ttu-id="bdb3c-141">Öznitelik değeri'ne tıklayın.</span><span class="sxs-lookup"><span data-stu-id="bdb3c-141">Click Attribute value.</span></span>
8. <span data-ttu-id="bdb3c-142">Listede, seçili satırı işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="bdb3c-142">In the list, mark the selected row.</span></span>
9. <span data-ttu-id="bdb3c-143">Öznitelik alanına bir değer girin veya seçin.</span><span class="sxs-lookup"><span data-stu-id="bdb3c-143">In the Attribute field, enter or select a value.</span></span>
10. <span data-ttu-id="bdb3c-144">Ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="bdb3c-144">Click Add.</span></span>
11. <span data-ttu-id="bdb3c-145">Metin sabiti'ne tıklayın.</span><span class="sxs-lookup"><span data-stu-id="bdb3c-145">Click Text constant.</span></span>
12. <span data-ttu-id="bdb3c-146">Listede, seçili satırı işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="bdb3c-146">In the list, mark the selected row.</span></span>
13. <span data-ttu-id="bdb3c-147">Metin alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="bdb3c-147">In the Text field, type a value.</span></span>
14. <span data-ttu-id="bdb3c-148">Ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="bdb3c-148">Click Add.</span></span>
15. <span data-ttu-id="bdb3c-149">Öznitelik değeri'ne tıklayın.</span><span class="sxs-lookup"><span data-stu-id="bdb3c-149">Click Attribute value.</span></span>
16. <span data-ttu-id="bdb3c-150">Listede, seçili satırı işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="bdb3c-150">In the list, mark the selected row.</span></span>
17. <span data-ttu-id="bdb3c-151">Öznitelik alanına bir değer girin veya seçin.</span><span class="sxs-lookup"><span data-stu-id="bdb3c-151">In the Attribute field, enter or select a value.</span></span>
18. <span data-ttu-id="bdb3c-152">Ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="bdb3c-152">Click Add.</span></span>
19. <span data-ttu-id="bdb3c-153">Metin sabiti'ne tıklayın.</span><span class="sxs-lookup"><span data-stu-id="bdb3c-153">Click Text constant.</span></span>
20. <span data-ttu-id="bdb3c-154">Listede, seçili satırı işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="bdb3c-154">In the list, mark the selected row.</span></span>
21. <span data-ttu-id="bdb3c-155">Metin alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="bdb3c-155">In the Text field, type a value.</span></span>
22. <span data-ttu-id="bdb3c-156">Ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="bdb3c-156">Click Add.</span></span>
23. <span data-ttu-id="bdb3c-157">Öznitelik değeri'ne tıklayın.</span><span class="sxs-lookup"><span data-stu-id="bdb3c-157">Click Attribute value.</span></span>
24. <span data-ttu-id="bdb3c-158">Listede, seçili satırı işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="bdb3c-158">In the list, mark the selected row.</span></span>
25. <span data-ttu-id="bdb3c-159">Öznitelik alanına bir değer girin veya seçin.</span><span class="sxs-lookup"><span data-stu-id="bdb3c-159">In the Attribute field, enter or select a value.</span></span>
26. <span data-ttu-id="bdb3c-160">Ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="bdb3c-160">Click Add.</span></span>
27. <span data-ttu-id="bdb3c-161">Metin sabiti'ne tıklayın.</span><span class="sxs-lookup"><span data-stu-id="bdb3c-161">Click Text constant.</span></span>
28. <span data-ttu-id="bdb3c-162">Listede, seçili satırı işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="bdb3c-162">In the list, mark the selected row.</span></span>
29. <span data-ttu-id="bdb3c-163">Metin alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="bdb3c-163">In the Text field, type a value.</span></span>
30. <span data-ttu-id="bdb3c-164">Ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="bdb3c-164">Click Add.</span></span>
31. <span data-ttu-id="bdb3c-165">Öznitelik değeri'ne tıklayın.</span><span class="sxs-lookup"><span data-stu-id="bdb3c-165">Click Attribute value.</span></span>
32. <span data-ttu-id="bdb3c-166">Listede, seçili satırı işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="bdb3c-166">In the list, mark the selected row.</span></span>
33. <span data-ttu-id="bdb3c-167">Öznitelik alanına bir değer girin veya seçin.</span><span class="sxs-lookup"><span data-stu-id="bdb3c-167">In the Attribute field, enter or select a value.</span></span>
34. <span data-ttu-id="bdb3c-168">Ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="bdb3c-168">Click Add.</span></span>
35. <span data-ttu-id="bdb3c-169">Metin sabiti'ne tıklayın.</span><span class="sxs-lookup"><span data-stu-id="bdb3c-169">Click Text constant.</span></span>
36. <span data-ttu-id="bdb3c-170">Listede, seçili satırı işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="bdb3c-170">In the list, mark the selected row.</span></span>
37. <span data-ttu-id="bdb3c-171">Metin alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="bdb3c-171">In the Text field, type a value.</span></span>
38. <span data-ttu-id="bdb3c-172">Ekle öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="bdb3c-172">Click Add.</span></span>
39. <span data-ttu-id="bdb3c-173">Numara serisi değeri'ne tıklayın.</span><span class="sxs-lookup"><span data-stu-id="bdb3c-173">Click Number sequence value.</span></span>
40. <span data-ttu-id="bdb3c-174">Listede, seçili satırı işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="bdb3c-174">In the list, mark the selected row.</span></span>
41. <span data-ttu-id="bdb3c-175">Numara sırası alanında, bir değer girin veya seçin.</span><span class="sxs-lookup"><span data-stu-id="bdb3c-175">In the Number sequence field, enter or select a value.</span></span>
42. <span data-ttu-id="bdb3c-176">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="bdb3c-176">Close the page.</span></span>
43. <span data-ttu-id="bdb3c-177">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="bdb3c-177">Close the page.</span></span>
44. <span data-ttu-id="bdb3c-178">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="bdb3c-178">Close the page.</span></span>


