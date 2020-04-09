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
ms.openlocfilehash: a837721db5281b0626f37b7a793349b91afa6f85
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/18/2020
ms.locfileid: "3147768"
---
# <a name="create-a-product-number-nomenclature-for-configured-product-variants"></a><span data-ttu-id="59ce2-103">Yapılandırılmış ürün çeşitleri için ürün numarası terminolojisi oluşturma</span><span class="sxs-lookup"><span data-stu-id="59ce2-103">Create a product number nomenclature for configured product variants</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="59ce2-104">Bu yordam, yapılandırılmış ürün çeşitleri için bir ürün numara terminolojisinin nasıl ayarlanacağını ve yapılandırılabilir bir ana ürüne nasıl eklenebileceğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="59ce2-104">This procedure shows you how to set up a product number nomenclature for configured product variants, and how it can be attached to a configurable product master.</span></span> <span data-ttu-id="59ce2-105">Bu yordam ayrıca bir ürün yapılandırma model bileşeni için bir yapılandırma terminolojisini nasıl oluşturabileceğinizi de gösterir.</span><span class="sxs-lookup"><span data-stu-id="59ce2-105">This procedure also demonstrates how you can build a configuration nomenclature for a product configuration model component.</span></span> <span data-ttu-id="59ce2-106">Bu yöntemi oluşturmak için kullanılan demo veri şirketi USMF'dir.</span><span class="sxs-lookup"><span data-stu-id="59ce2-106">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="59ce2-107">Yeni ürün numarası terminolojisi D0004 ana ürününe atanmıştır.</span><span class="sxs-lookup"><span data-stu-id="59ce2-107">The new product number nomenclature is assigned to the D0004 product master.</span></span> <span data-ttu-id="59ce2-108">Bu görev genellikle bir ürün tasarımcısı tarafından gerçekleştirilir.</span><span class="sxs-lookup"><span data-stu-id="59ce2-108">This task would typically be done by a product designer.</span></span>


## <a name="create-a-product-number-nomenclature"></a><span data-ttu-id="59ce2-109">Ürün numara terminolojisi oluşturma</span><span class="sxs-lookup"><span data-stu-id="59ce2-109">Create a product number nomenclature</span></span>
1. <span data-ttu-id="59ce2-110">Ürün varyantı model tanımı'na tıklayın.</span><span class="sxs-lookup"><span data-stu-id="59ce2-110">Click Product variant model definition.</span></span>
2. <span data-ttu-id="59ce2-111">Ürün terminolojisi'ne tıklayın.</span><span class="sxs-lookup"><span data-stu-id="59ce2-111">Click Product nomenclature.</span></span>
3. <span data-ttu-id="59ce2-112">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="59ce2-112">Click New.</span></span>
4. <span data-ttu-id="59ce2-113">İsim alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="59ce2-113">In the Name field, type a value.</span></span>
5. <span data-ttu-id="59ce2-114">Açıklama alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="59ce2-114">In the Description field, type a value.</span></span>
6. <span data-ttu-id="59ce2-115">Ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="59ce2-115">Click Add.</span></span>
7. <span data-ttu-id="59ce2-116">Ana ürün numarası'na tıklayın.</span><span class="sxs-lookup"><span data-stu-id="59ce2-116">Click Product master number.</span></span>
8. <span data-ttu-id="59ce2-117">Ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="59ce2-117">Click Add.</span></span>
9. <span data-ttu-id="59ce2-118">Metin sabiti'ne tıklayın.</span><span class="sxs-lookup"><span data-stu-id="59ce2-118">Click Text constant.</span></span>
10. <span data-ttu-id="59ce2-119">Listede, seçili satırı işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="59ce2-119">In the list, mark the selected row.</span></span>
11. <span data-ttu-id="59ce2-120">Metin alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="59ce2-120">In the Text field, type a value.</span></span>
12. <span data-ttu-id="59ce2-121">Ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="59ce2-121">Click Add.</span></span>
13. <span data-ttu-id="59ce2-122">Yapılandırma'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="59ce2-122">Click Configuration.</span></span>
14. <span data-ttu-id="59ce2-123">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="59ce2-123">Close the page.</span></span>

## <a name="assign-the-product-number-nomenclature-to-a-product-master"></a><span data-ttu-id="59ce2-124">Ana ürüne, ürün numara terminolojisi atama</span><span class="sxs-lookup"><span data-stu-id="59ce2-124">Assign the product number nomenclature to a product master</span></span>
1. <span data-ttu-id="59ce2-125">Ana ürünler'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="59ce2-125">Click Product masters.</span></span>
2. <span data-ttu-id="59ce2-126">Kayıtları bulmak için Hızlı Filtre'yi kullanın.</span><span class="sxs-lookup"><span data-stu-id="59ce2-126">Use the Quick Filter to find records.</span></span> <span data-ttu-id="59ce2-127">Örneğin, Ürün numarası alanında "D" değeriyle filtreleyin.</span><span class="sxs-lookup"><span data-stu-id="59ce2-127">For example, filter on the Product number field with a value of 'D'.</span></span>
3. <span data-ttu-id="59ce2-128">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="59ce2-128">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="59ce2-129">Düzenle'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="59ce2-129">Click Edit.</span></span>
5. <span data-ttu-id="59ce2-130">Terminoloji kullan alanında Evet'i seçin.</span><span class="sxs-lookup"><span data-stu-id="59ce2-130">Select Yes in the Use nomenclature field.</span></span>
6. <span data-ttu-id="59ce2-131">Ürün çeşidi numara terminolojisi alanında bir değer girin veya seçin.</span><span class="sxs-lookup"><span data-stu-id="59ce2-131">In the Product variant number nomenclature field, enter or select a value.</span></span>
7. <span data-ttu-id="59ce2-132">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="59ce2-132">Close the page.</span></span>
8. <span data-ttu-id="59ce2-133">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="59ce2-133">Close the page.</span></span>

## <a name="create-nomenclature-for-a-product-configuration-model-component"></a><span data-ttu-id="59ce2-134">Ürün yapılandırma model bileşeni için terminoloji oluşturma</span><span class="sxs-lookup"><span data-stu-id="59ce2-134">Create nomenclature for a product configuration model component</span></span>
1. <span data-ttu-id="59ce2-135">Ürün yapılandırma modelleri'ne tıklayın.</span><span class="sxs-lookup"><span data-stu-id="59ce2-135">Click Product configuration models.</span></span>
2. <span data-ttu-id="59ce2-136">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="59ce2-136">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="59ce2-137">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="59ce2-137">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="59ce2-138">Düzenle'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="59ce2-138">Click Edit.</span></span>
5. <span data-ttu-id="59ce2-139">Konfigürasyon terminolojisini kullan alanında Evet'i seçin.</span><span class="sxs-lookup"><span data-stu-id="59ce2-139">Select Yes in the Use configuration nomenclature field.</span></span>
6. <span data-ttu-id="59ce2-140">Ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="59ce2-140">Click Add.</span></span>
7. <span data-ttu-id="59ce2-141">Öznitelik değeri'ne tıklayın.</span><span class="sxs-lookup"><span data-stu-id="59ce2-141">Click Attribute value.</span></span>
8. <span data-ttu-id="59ce2-142">Listede, seçili satırı işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="59ce2-142">In the list, mark the selected row.</span></span>
9. <span data-ttu-id="59ce2-143">Öznitelik alanına bir değer girin veya seçin.</span><span class="sxs-lookup"><span data-stu-id="59ce2-143">In the Attribute field, enter or select a value.</span></span>
10. <span data-ttu-id="59ce2-144">Ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="59ce2-144">Click Add.</span></span>
11. <span data-ttu-id="59ce2-145">Metin sabiti'ne tıklayın.</span><span class="sxs-lookup"><span data-stu-id="59ce2-145">Click Text constant.</span></span>
12. <span data-ttu-id="59ce2-146">Listede, seçili satırı işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="59ce2-146">In the list, mark the selected row.</span></span>
13. <span data-ttu-id="59ce2-147">Metin alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="59ce2-147">In the Text field, type a value.</span></span>
14. <span data-ttu-id="59ce2-148">Ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="59ce2-148">Click Add.</span></span>
15. <span data-ttu-id="59ce2-149">Öznitelik değeri'ne tıklayın.</span><span class="sxs-lookup"><span data-stu-id="59ce2-149">Click Attribute value.</span></span>
16. <span data-ttu-id="59ce2-150">Listede, seçili satırı işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="59ce2-150">In the list, mark the selected row.</span></span>
17. <span data-ttu-id="59ce2-151">Öznitelik alanına bir değer girin veya seçin.</span><span class="sxs-lookup"><span data-stu-id="59ce2-151">In the Attribute field, enter or select a value.</span></span>
18. <span data-ttu-id="59ce2-152">Ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="59ce2-152">Click Add.</span></span>
19. <span data-ttu-id="59ce2-153">Metin sabiti'ne tıklayın.</span><span class="sxs-lookup"><span data-stu-id="59ce2-153">Click Text constant.</span></span>
20. <span data-ttu-id="59ce2-154">Listede, seçili satırı işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="59ce2-154">In the list, mark the selected row.</span></span>
21. <span data-ttu-id="59ce2-155">Metin alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="59ce2-155">In the Text field, type a value.</span></span>
22. <span data-ttu-id="59ce2-156">Ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="59ce2-156">Click Add.</span></span>
23. <span data-ttu-id="59ce2-157">Öznitelik değeri'ne tıklayın.</span><span class="sxs-lookup"><span data-stu-id="59ce2-157">Click Attribute value.</span></span>
24. <span data-ttu-id="59ce2-158">Listede, seçili satırı işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="59ce2-158">In the list, mark the selected row.</span></span>
25. <span data-ttu-id="59ce2-159">Öznitelik alanına bir değer girin veya seçin.</span><span class="sxs-lookup"><span data-stu-id="59ce2-159">In the Attribute field, enter or select a value.</span></span>
26. <span data-ttu-id="59ce2-160">Ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="59ce2-160">Click Add.</span></span>
27. <span data-ttu-id="59ce2-161">Metin sabiti'ne tıklayın.</span><span class="sxs-lookup"><span data-stu-id="59ce2-161">Click Text constant.</span></span>
28. <span data-ttu-id="59ce2-162">Listede, seçili satırı işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="59ce2-162">In the list, mark the selected row.</span></span>
29. <span data-ttu-id="59ce2-163">Metin alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="59ce2-163">In the Text field, type a value.</span></span>
30. <span data-ttu-id="59ce2-164">Ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="59ce2-164">Click Add.</span></span>
31. <span data-ttu-id="59ce2-165">Öznitelik değeri'ne tıklayın.</span><span class="sxs-lookup"><span data-stu-id="59ce2-165">Click Attribute value.</span></span>
32. <span data-ttu-id="59ce2-166">Listede, seçili satırı işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="59ce2-166">In the list, mark the selected row.</span></span>
33. <span data-ttu-id="59ce2-167">Öznitelik alanına bir değer girin veya seçin.</span><span class="sxs-lookup"><span data-stu-id="59ce2-167">In the Attribute field, enter or select a value.</span></span>
34. <span data-ttu-id="59ce2-168">Ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="59ce2-168">Click Add.</span></span>
35. <span data-ttu-id="59ce2-169">Metin sabiti'ne tıklayın.</span><span class="sxs-lookup"><span data-stu-id="59ce2-169">Click Text constant.</span></span>
36. <span data-ttu-id="59ce2-170">Listede, seçili satırı işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="59ce2-170">In the list, mark the selected row.</span></span>
37. <span data-ttu-id="59ce2-171">Metin alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="59ce2-171">In the Text field, type a value.</span></span>
38. <span data-ttu-id="59ce2-172">Ekle öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="59ce2-172">Click Add.</span></span>
39. <span data-ttu-id="59ce2-173">Numara serisi değeri'ne tıklayın.</span><span class="sxs-lookup"><span data-stu-id="59ce2-173">Click Number sequence value.</span></span>
40. <span data-ttu-id="59ce2-174">Listede, seçili satırı işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="59ce2-174">In the list, mark the selected row.</span></span>
41. <span data-ttu-id="59ce2-175">Numara sırası alanında, bir değer girin veya seçin.</span><span class="sxs-lookup"><span data-stu-id="59ce2-175">In the Number sequence field, enter or select a value.</span></span>
42. <span data-ttu-id="59ce2-176">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="59ce2-176">Close the page.</span></span>
43. <span data-ttu-id="59ce2-177">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="59ce2-177">Close the page.</span></span>
44. <span data-ttu-id="59ce2-178">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="59ce2-178">Close the page.</span></span>

