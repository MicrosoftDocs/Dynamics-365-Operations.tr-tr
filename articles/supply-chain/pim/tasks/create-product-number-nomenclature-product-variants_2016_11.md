--- 
title: "Yapılandırılmış ürün çeşitleri için ürün numarası oluşturma"
description: "Bu yordam, yapılandırılmış ürün çeşitleri için bir ürün numara terminolojisinin nasıl ayarlanacağını ve yapılandırılabilir bir ana ürüne nasıl eklenebileceğini gösterir."
author: BibiSp
manager: AnnBe
ms.date: 10/25/2016
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
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: e70a5f28635e75a69811085637f7e7431c0f1d40
ms.contentlocale: tr-tr
ms.lasthandoff: 09/29/2017

---
# <a name="create-a-product-number-for-configured-product-variants"></a><span data-ttu-id="69bed-103">Yapılandırılmış ürün çeşitleri için ürün numarası oluşturma</span><span class="sxs-lookup"><span data-stu-id="69bed-103">Create a product number for configured product variants</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="69bed-104">Bu yordam, yapılandırılmış ürün çeşitleri için bir ürün numara terminolojisinin nasıl ayarlanacağını ve yapılandırılabilir bir ana ürüne nasıl eklenebileceğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="69bed-104">This procedure shows you how to set up a product number nomenclature for configured product variants, and how it can be attached to a configurable product master.</span></span> <span data-ttu-id="69bed-105">Bu yordam ayrıca bir ürün yapılandırma model bileşeni için bir yapılandırma terminolojisini nasıl oluşturabileceğinizi de gösterir.</span><span class="sxs-lookup"><span data-stu-id="69bed-105">This procedure also demonstrates how you can build a configuration nomenclature for a product configuration model component.</span></span> <span data-ttu-id="69bed-106">Bu yöntemi oluşturmak için kullanılan demo veri şirketi USMF'dir.</span><span class="sxs-lookup"><span data-stu-id="69bed-106">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="69bed-107">Yeni ürün numarası terminolojisi D0004 ana ürününe atanmıştır.</span><span class="sxs-lookup"><span data-stu-id="69bed-107">The new product number nomenclature is assigned to the D0004 product master.</span></span> <span data-ttu-id="69bed-108">Bu görev genellikle bir ürün tasarımcısı tarafından gerçekleştirilir.</span><span class="sxs-lookup"><span data-stu-id="69bed-108">This task would typically be done by a product designer.</span></span>


## <a name="create-a-product-number-nomenclature"></a><span data-ttu-id="69bed-109">Ürün numara terminolojisi oluşturma</span><span class="sxs-lookup"><span data-stu-id="69bed-109">Create a product number nomenclature</span></span>
1. <span data-ttu-id="69bed-110">Ürün varyantı model tanımı'na tıklayın.</span><span class="sxs-lookup"><span data-stu-id="69bed-110">Click Product variant model definition.</span></span>
2. <span data-ttu-id="69bed-111">Ürün terminolojisi'ne tıklayın.</span><span class="sxs-lookup"><span data-stu-id="69bed-111">Click Product nomenclature.</span></span>
3. <span data-ttu-id="69bed-112">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="69bed-112">Click New.</span></span>
4. <span data-ttu-id="69bed-113">İsim alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="69bed-113">In the Name field, type a value.</span></span>
5. <span data-ttu-id="69bed-114">Açıklama alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="69bed-114">In the Description field, type a value.</span></span>
6. <span data-ttu-id="69bed-115">Ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="69bed-115">Click Add.</span></span>
7. <span data-ttu-id="69bed-116">Ana ürün numarası'na tıklayın.</span><span class="sxs-lookup"><span data-stu-id="69bed-116">Click Product master number.</span></span>
8. <span data-ttu-id="69bed-117">Ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="69bed-117">Click Add.</span></span>
9. <span data-ttu-id="69bed-118">Metin sabiti'ne tıklayın.</span><span class="sxs-lookup"><span data-stu-id="69bed-118">Click Text constant.</span></span>
10. <span data-ttu-id="69bed-119">Listede, seçili satırı işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="69bed-119">In the list, mark the selected row.</span></span>
11. <span data-ttu-id="69bed-120">Metin alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="69bed-120">In the Text field, type a value.</span></span>
12. <span data-ttu-id="69bed-121">Ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="69bed-121">Click Add.</span></span>
13. <span data-ttu-id="69bed-122">Yapılandırma'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="69bed-122">Click Configuration.</span></span>
14. <span data-ttu-id="69bed-123">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="69bed-123">Close the page.</span></span>

## <a name="assign-the-product-number-nomenclature-to-a-product-master"></a><span data-ttu-id="69bed-124">Ana ürüne, ürün numara terminolojisi atama</span><span class="sxs-lookup"><span data-stu-id="69bed-124">Assign the product number nomenclature to a product master</span></span>
1. <span data-ttu-id="69bed-125">Ana ürünler'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="69bed-125">Click Product masters.</span></span>
2. <span data-ttu-id="69bed-126">Kayıtları bulmak için Hızlı Filtre'yi kullanın.</span><span class="sxs-lookup"><span data-stu-id="69bed-126">Use the Quick Filter to find records.</span></span> <span data-ttu-id="69bed-127">Örneğin, Ürün numarası alanında "D" değeriyle filtreleyin.</span><span class="sxs-lookup"><span data-stu-id="69bed-127">For example, filter on the Product number field with a value of 'D'.</span></span>
3. <span data-ttu-id="69bed-128">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="69bed-128">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="69bed-129">Düzenle'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="69bed-129">Click Edit.</span></span>
5. <span data-ttu-id="69bed-130">Terminoloji kullan alanında Evet'i seçin.</span><span class="sxs-lookup"><span data-stu-id="69bed-130">Select Yes in the Use nomenclature field.</span></span>
6. <span data-ttu-id="69bed-131">Ürün çeşidi numara terminolojisi alanında bir değer girin veya seçin.</span><span class="sxs-lookup"><span data-stu-id="69bed-131">In the Product variant number nomenclature field, enter or select a value.</span></span>
7. <span data-ttu-id="69bed-132">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="69bed-132">Close the page.</span></span>
8. <span data-ttu-id="69bed-133">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="69bed-133">Close the page.</span></span>

## <a name="create-nomenclature-for-a-product-configuration-model-component"></a><span data-ttu-id="69bed-134">Ürün yapılandırma model bileşeni için terminoloji oluşturma</span><span class="sxs-lookup"><span data-stu-id="69bed-134">Create nomenclature for a product configuration model component</span></span>
1. <span data-ttu-id="69bed-135">Ürün yapılandırma modelleri'ne tıklayın.</span><span class="sxs-lookup"><span data-stu-id="69bed-135">Click Product configuration models.</span></span>
2. <span data-ttu-id="69bed-136">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="69bed-136">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="69bed-137">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="69bed-137">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="69bed-138">Düzenle'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="69bed-138">Click Edit.</span></span>
5. <span data-ttu-id="69bed-139">Konfigürasyon terminolojisini kullan alanında Evet'i seçin.</span><span class="sxs-lookup"><span data-stu-id="69bed-139">Select Yes in the Use configuration nomenclature field.</span></span>
6. <span data-ttu-id="69bed-140">Ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="69bed-140">Click Add.</span></span>
7. <span data-ttu-id="69bed-141">Öznitelik değeri'ne tıklayın.</span><span class="sxs-lookup"><span data-stu-id="69bed-141">Click Attribute value.</span></span>
8. <span data-ttu-id="69bed-142">Listede, seçili satırı işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="69bed-142">In the list, mark the selected row.</span></span>
9. <span data-ttu-id="69bed-143">Öznitelik alanına bir değer girin veya seçin.</span><span class="sxs-lookup"><span data-stu-id="69bed-143">In the Attribute field, enter or select a value.</span></span>
10. <span data-ttu-id="69bed-144">Ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="69bed-144">Click Add.</span></span>
11. <span data-ttu-id="69bed-145">Metin sabiti'ne tıklayın.</span><span class="sxs-lookup"><span data-stu-id="69bed-145">Click Text constant.</span></span>
12. <span data-ttu-id="69bed-146">Listede, seçili satırı işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="69bed-146">In the list, mark the selected row.</span></span>
13. <span data-ttu-id="69bed-147">Metin alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="69bed-147">In the Text field, type a value.</span></span>
14. <span data-ttu-id="69bed-148">Ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="69bed-148">Click Add.</span></span>
15. <span data-ttu-id="69bed-149">Öznitelik değeri'ne tıklayın.</span><span class="sxs-lookup"><span data-stu-id="69bed-149">Click Attribute value.</span></span>
16. <span data-ttu-id="69bed-150">Listede, seçili satırı işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="69bed-150">In the list, mark the selected row.</span></span>
17. <span data-ttu-id="69bed-151">Öznitelik alanına bir değer girin veya seçin.</span><span class="sxs-lookup"><span data-stu-id="69bed-151">In the Attribute field, enter or select a value.</span></span>
18. <span data-ttu-id="69bed-152">Ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="69bed-152">Click Add.</span></span>
19. <span data-ttu-id="69bed-153">Metin sabiti'ne tıklayın.</span><span class="sxs-lookup"><span data-stu-id="69bed-153">Click Text constant.</span></span>
20. <span data-ttu-id="69bed-154">Listede, seçili satırı işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="69bed-154">In the list, mark the selected row.</span></span>
21. <span data-ttu-id="69bed-155">Metin alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="69bed-155">In the Text field, type a value.</span></span>
22. <span data-ttu-id="69bed-156">Ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="69bed-156">Click Add.</span></span>
23. <span data-ttu-id="69bed-157">Öznitelik değeri'ne tıklayın.</span><span class="sxs-lookup"><span data-stu-id="69bed-157">Click Attribute value.</span></span>
24. <span data-ttu-id="69bed-158">Listede, seçili satırı işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="69bed-158">In the list, mark the selected row.</span></span>
25. <span data-ttu-id="69bed-159">Öznitelik alanına bir değer girin veya seçin.</span><span class="sxs-lookup"><span data-stu-id="69bed-159">In the Attribute field, enter or select a value.</span></span>
26. <span data-ttu-id="69bed-160">Ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="69bed-160">Click Add.</span></span>
27. <span data-ttu-id="69bed-161">Metin sabiti'ne tıklayın.</span><span class="sxs-lookup"><span data-stu-id="69bed-161">Click Text constant.</span></span>
28. <span data-ttu-id="69bed-162">Listede, seçili satırı işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="69bed-162">In the list, mark the selected row.</span></span>
29. <span data-ttu-id="69bed-163">Metin alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="69bed-163">In the Text field, type a value.</span></span>
30. <span data-ttu-id="69bed-164">Ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="69bed-164">Click Add.</span></span>
31. <span data-ttu-id="69bed-165">Öznitelik değeri'ne tıklayın.</span><span class="sxs-lookup"><span data-stu-id="69bed-165">Click Attribute value.</span></span>
32. <span data-ttu-id="69bed-166">Listede, seçili satırı işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="69bed-166">In the list, mark the selected row.</span></span>
33. <span data-ttu-id="69bed-167">Öznitelik alanına bir değer girin veya seçin.</span><span class="sxs-lookup"><span data-stu-id="69bed-167">In the Attribute field, enter or select a value.</span></span>
34. <span data-ttu-id="69bed-168">Ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="69bed-168">Click Add.</span></span>
35. <span data-ttu-id="69bed-169">Metin sabiti'ne tıklayın.</span><span class="sxs-lookup"><span data-stu-id="69bed-169">Click Text constant.</span></span>
36. <span data-ttu-id="69bed-170">Listede, seçili satırı işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="69bed-170">In the list, mark the selected row.</span></span>
37. <span data-ttu-id="69bed-171">Metin alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="69bed-171">In the Text field, type a value.</span></span>
38. <span data-ttu-id="69bed-172">Ekle öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="69bed-172">Click Add.</span></span>
39. <span data-ttu-id="69bed-173">Numara serisi değeri'ne tıklayın.</span><span class="sxs-lookup"><span data-stu-id="69bed-173">Click Number sequence value.</span></span>
40. <span data-ttu-id="69bed-174">Listede, seçili satırı işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="69bed-174">In the list, mark the selected row.</span></span>
41. <span data-ttu-id="69bed-175">Numara sırası alanında, bir değer girin veya seçin.</span><span class="sxs-lookup"><span data-stu-id="69bed-175">In the Number sequence field, enter or select a value.</span></span>
42. <span data-ttu-id="69bed-176">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="69bed-176">Close the page.</span></span>
43. <span data-ttu-id="69bed-177">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="69bed-177">Close the page.</span></span>
44. <span data-ttu-id="69bed-178">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="69bed-178">Close the page.</span></span>


