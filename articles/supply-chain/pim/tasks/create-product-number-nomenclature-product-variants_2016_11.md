---
title: Yapılandırılmış ürün çeşitleri için ürün numarası terminolojisi oluşturma
description: Bu yordam, yapılandırılmış ürün çeşitleri için bir ürün numara terminolojisinin nasıl ayarlanacağını ve yapılandırılabilir bir ana ürüne nasıl eklenebileceğini gösterir.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, EcoResNomenclature, EcoResProductListPage, EcoResProductDetails, PCProductConfigurationModelListPage, PCProductConfigurationModelDetails
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 22aa4823fbf43b29a8fd9661645e8563c07e437d
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/01/2019
ms.locfileid: "1844669"
---
# <a name="create-a-product-number-nomenclature-for-configured-product-variants"></a><span data-ttu-id="216e4-103">Yapılandırılmış ürün çeşitleri için ürün numarası terminolojisi oluşturma</span><span class="sxs-lookup"><span data-stu-id="216e4-103">Create a product number nomenclature for configured product variants</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="216e4-104">Bu yordam, yapılandırılmış ürün çeşitleri için bir ürün numara terminolojisinin nasıl ayarlanacağını ve yapılandırılabilir bir ana ürüne nasıl eklenebileceğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="216e4-104">This procedure shows you how to set up a product number nomenclature for configured product variants, and how it can be attached to a configurable product master.</span></span> <span data-ttu-id="216e4-105">Bu yordam ayrıca bir ürün yapılandırma model bileşeni için bir yapılandırma terminolojisini nasıl oluşturabileceğinizi de gösterir.</span><span class="sxs-lookup"><span data-stu-id="216e4-105">This procedure also demonstrates how you can build a configuration nomenclature for a product configuration model component.</span></span> <span data-ttu-id="216e4-106">Bu yöntemi oluşturmak için kullanılan demo veri şirketi USMF'dir.</span><span class="sxs-lookup"><span data-stu-id="216e4-106">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="216e4-107">Yeni ürün numarası terminolojisi D0004 ana ürününe atanmıştır.</span><span class="sxs-lookup"><span data-stu-id="216e4-107">The new product number nomenclature is assigned to the D0004 product master.</span></span> <span data-ttu-id="216e4-108">Bu görev genellikle bir ürün tasarımcısı tarafından gerçekleştirilir.</span><span class="sxs-lookup"><span data-stu-id="216e4-108">This task would typically be done by a product designer.</span></span>


## <a name="create-a-product-number-nomenclature"></a><span data-ttu-id="216e4-109">Ürün numara terminolojisi oluşturma</span><span class="sxs-lookup"><span data-stu-id="216e4-109">Create a product number nomenclature</span></span>
1. <span data-ttu-id="216e4-110">Ürün varyantı model tanımı'na tıklayın.</span><span class="sxs-lookup"><span data-stu-id="216e4-110">Click Product variant model definition.</span></span>
2. <span data-ttu-id="216e4-111">Ürün terminolojisi'ne tıklayın.</span><span class="sxs-lookup"><span data-stu-id="216e4-111">Click Product nomenclature.</span></span>
3. <span data-ttu-id="216e4-112">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="216e4-112">Click New.</span></span>
4. <span data-ttu-id="216e4-113">İsim alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="216e4-113">In the Name field, type a value.</span></span>
5. <span data-ttu-id="216e4-114">Açıklama alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="216e4-114">In the Description field, type a value.</span></span>
6. <span data-ttu-id="216e4-115">Ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="216e4-115">Click Add.</span></span>
7. <span data-ttu-id="216e4-116">Ana ürün numarası'na tıklayın.</span><span class="sxs-lookup"><span data-stu-id="216e4-116">Click Product master number.</span></span>
8. <span data-ttu-id="216e4-117">Ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="216e4-117">Click Add.</span></span>
9. <span data-ttu-id="216e4-118">Metin sabiti'ne tıklayın.</span><span class="sxs-lookup"><span data-stu-id="216e4-118">Click Text constant.</span></span>
10. <span data-ttu-id="216e4-119">Listede, seçili satırı işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="216e4-119">In the list, mark the selected row.</span></span>
11. <span data-ttu-id="216e4-120">Metin alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="216e4-120">In the Text field, type a value.</span></span>
12. <span data-ttu-id="216e4-121">Ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="216e4-121">Click Add.</span></span>
13. <span data-ttu-id="216e4-122">Yapılandırma'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="216e4-122">Click Configuration.</span></span>
14. <span data-ttu-id="216e4-123">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="216e4-123">Close the page.</span></span>

## <a name="assign-the-product-number-nomenclature-to-a-product-master"></a><span data-ttu-id="216e4-124">Ana ürüne, ürün numara terminolojisi atama</span><span class="sxs-lookup"><span data-stu-id="216e4-124">Assign the product number nomenclature to a product master</span></span>
1. <span data-ttu-id="216e4-125">Ana ürünler'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="216e4-125">Click Product masters.</span></span>
2. <span data-ttu-id="216e4-126">Kayıtları bulmak için Hızlı Filtre'yi kullanın.</span><span class="sxs-lookup"><span data-stu-id="216e4-126">Use the Quick Filter to find records.</span></span> <span data-ttu-id="216e4-127">Örneğin, Ürün numarası alanında "D" değeriyle filtreleyin.</span><span class="sxs-lookup"><span data-stu-id="216e4-127">For example, filter on the Product number field with a value of 'D'.</span></span>
3. <span data-ttu-id="216e4-128">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="216e4-128">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="216e4-129">Düzenle'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="216e4-129">Click Edit.</span></span>
5. <span data-ttu-id="216e4-130">Terminoloji kullan alanında Evet'i seçin.</span><span class="sxs-lookup"><span data-stu-id="216e4-130">Select Yes in the Use nomenclature field.</span></span>
6. <span data-ttu-id="216e4-131">Ürün çeşidi numara terminolojisi alanında bir değer girin veya seçin.</span><span class="sxs-lookup"><span data-stu-id="216e4-131">In the Product variant number nomenclature field, enter or select a value.</span></span>
7. <span data-ttu-id="216e4-132">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="216e4-132">Close the page.</span></span>
8. <span data-ttu-id="216e4-133">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="216e4-133">Close the page.</span></span>

## <a name="create-nomenclature-for-a-product-configuration-model-component"></a><span data-ttu-id="216e4-134">Ürün yapılandırma model bileşeni için terminoloji oluşturma</span><span class="sxs-lookup"><span data-stu-id="216e4-134">Create nomenclature for a product configuration model component</span></span>
1. <span data-ttu-id="216e4-135">Ürün yapılandırma modelleri'ne tıklayın.</span><span class="sxs-lookup"><span data-stu-id="216e4-135">Click Product configuration models.</span></span>
2. <span data-ttu-id="216e4-136">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="216e4-136">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="216e4-137">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="216e4-137">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="216e4-138">Düzenle'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="216e4-138">Click Edit.</span></span>
5. <span data-ttu-id="216e4-139">Konfigürasyon terminolojisini kullan alanında Evet'i seçin.</span><span class="sxs-lookup"><span data-stu-id="216e4-139">Select Yes in the Use configuration nomenclature field.</span></span>
6. <span data-ttu-id="216e4-140">Ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="216e4-140">Click Add.</span></span>
7. <span data-ttu-id="216e4-141">Öznitelik değeri'ne tıklayın.</span><span class="sxs-lookup"><span data-stu-id="216e4-141">Click Attribute value.</span></span>
8. <span data-ttu-id="216e4-142">Listede, seçili satırı işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="216e4-142">In the list, mark the selected row.</span></span>
9. <span data-ttu-id="216e4-143">Öznitelik alanına bir değer girin veya seçin.</span><span class="sxs-lookup"><span data-stu-id="216e4-143">In the Attribute field, enter or select a value.</span></span>
10. <span data-ttu-id="216e4-144">Ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="216e4-144">Click Add.</span></span>
11. <span data-ttu-id="216e4-145">Metin sabiti'ne tıklayın.</span><span class="sxs-lookup"><span data-stu-id="216e4-145">Click Text constant.</span></span>
12. <span data-ttu-id="216e4-146">Listede, seçili satırı işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="216e4-146">In the list, mark the selected row.</span></span>
13. <span data-ttu-id="216e4-147">Metin alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="216e4-147">In the Text field, type a value.</span></span>
14. <span data-ttu-id="216e4-148">Ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="216e4-148">Click Add.</span></span>
15. <span data-ttu-id="216e4-149">Öznitelik değeri'ne tıklayın.</span><span class="sxs-lookup"><span data-stu-id="216e4-149">Click Attribute value.</span></span>
16. <span data-ttu-id="216e4-150">Listede, seçili satırı işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="216e4-150">In the list, mark the selected row.</span></span>
17. <span data-ttu-id="216e4-151">Öznitelik alanına bir değer girin veya seçin.</span><span class="sxs-lookup"><span data-stu-id="216e4-151">In the Attribute field, enter or select a value.</span></span>
18. <span data-ttu-id="216e4-152">Ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="216e4-152">Click Add.</span></span>
19. <span data-ttu-id="216e4-153">Metin sabiti'ne tıklayın.</span><span class="sxs-lookup"><span data-stu-id="216e4-153">Click Text constant.</span></span>
20. <span data-ttu-id="216e4-154">Listede, seçili satırı işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="216e4-154">In the list, mark the selected row.</span></span>
21. <span data-ttu-id="216e4-155">Metin alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="216e4-155">In the Text field, type a value.</span></span>
22. <span data-ttu-id="216e4-156">Ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="216e4-156">Click Add.</span></span>
23. <span data-ttu-id="216e4-157">Öznitelik değeri'ne tıklayın.</span><span class="sxs-lookup"><span data-stu-id="216e4-157">Click Attribute value.</span></span>
24. <span data-ttu-id="216e4-158">Listede, seçili satırı işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="216e4-158">In the list, mark the selected row.</span></span>
25. <span data-ttu-id="216e4-159">Öznitelik alanına bir değer girin veya seçin.</span><span class="sxs-lookup"><span data-stu-id="216e4-159">In the Attribute field, enter or select a value.</span></span>
26. <span data-ttu-id="216e4-160">Ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="216e4-160">Click Add.</span></span>
27. <span data-ttu-id="216e4-161">Metin sabiti'ne tıklayın.</span><span class="sxs-lookup"><span data-stu-id="216e4-161">Click Text constant.</span></span>
28. <span data-ttu-id="216e4-162">Listede, seçili satırı işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="216e4-162">In the list, mark the selected row.</span></span>
29. <span data-ttu-id="216e4-163">Metin alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="216e4-163">In the Text field, type a value.</span></span>
30. <span data-ttu-id="216e4-164">Ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="216e4-164">Click Add.</span></span>
31. <span data-ttu-id="216e4-165">Öznitelik değeri'ne tıklayın.</span><span class="sxs-lookup"><span data-stu-id="216e4-165">Click Attribute value.</span></span>
32. <span data-ttu-id="216e4-166">Listede, seçili satırı işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="216e4-166">In the list, mark the selected row.</span></span>
33. <span data-ttu-id="216e4-167">Öznitelik alanına bir değer girin veya seçin.</span><span class="sxs-lookup"><span data-stu-id="216e4-167">In the Attribute field, enter or select a value.</span></span>
34. <span data-ttu-id="216e4-168">Ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="216e4-168">Click Add.</span></span>
35. <span data-ttu-id="216e4-169">Metin sabiti'ne tıklayın.</span><span class="sxs-lookup"><span data-stu-id="216e4-169">Click Text constant.</span></span>
36. <span data-ttu-id="216e4-170">Listede, seçili satırı işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="216e4-170">In the list, mark the selected row.</span></span>
37. <span data-ttu-id="216e4-171">Metin alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="216e4-171">In the Text field, type a value.</span></span>
38. <span data-ttu-id="216e4-172">Ekle öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="216e4-172">Click Add.</span></span>
39. <span data-ttu-id="216e4-173">Numara serisi değeri'ne tıklayın.</span><span class="sxs-lookup"><span data-stu-id="216e4-173">Click Number sequence value.</span></span>
40. <span data-ttu-id="216e4-174">Listede, seçili satırı işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="216e4-174">In the list, mark the selected row.</span></span>
41. <span data-ttu-id="216e4-175">Numara sırası alanında, bir değer girin veya seçin.</span><span class="sxs-lookup"><span data-stu-id="216e4-175">In the Number sequence field, enter or select a value.</span></span>
42. <span data-ttu-id="216e4-176">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="216e4-176">Close the page.</span></span>
43. <span data-ttu-id="216e4-177">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="216e4-177">Close the page.</span></span>
44. <span data-ttu-id="216e4-178">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="216e4-178">Close the page.</span></span>

