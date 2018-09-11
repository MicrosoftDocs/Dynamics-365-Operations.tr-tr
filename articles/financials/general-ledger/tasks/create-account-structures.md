--- 
title: "Hesap yapıları oluşturma"
description: "Bu görev kılavuzu, hesap yapısı oluşturmayı adım adım açıklar."
author: aprilolson
manager: AnnBe
ms.date: 8/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: DimensionConfigureAccountStructure, DimensionCreateAccountStructure, DimensionHierarchyAddLevel, DimensionHierarchyConstraintActivate
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 32d71167fdad65cb1dec37671999a497759ca484
ms.openlocfilehash: 5c8ebdd9ac0fb834e57cd192baa0675a3e66caa3
ms.contentlocale: tr-tr
ms.lasthandoff: 09/11/2018

---
# <a name="create-account-structures"></a><span data-ttu-id="552f4-103">Hesap yapıları oluşturma</span><span class="sxs-lookup"><span data-stu-id="552f4-103">Create account structures</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="552f4-104">Bu görev kılavuzu, hesap yapısı oluşturmayı adım adım açıklar.</span><span class="sxs-lookup"><span data-stu-id="552f4-104">This task guide steps through creating an account structure.</span></span> <span data-ttu-id="552f4-105">Adımlarda demo veri şirketi USMF kullanılmaktadır.</span><span class="sxs-lookup"><span data-stu-id="552f4-105">The steps use demo data company USMF.</span></span>

1. <span data-ttu-id="552f4-106">Genel muhasebe > Hesap planı > Yapılar > Hesap yapılarını yapılandır'a gidin.</span><span class="sxs-lookup"><span data-stu-id="552f4-106">Go to General ledger > Chart of accounts > Structures > Configure account structures.</span></span>
2. <span data-ttu-id="552f4-107">Açılır iletişim kutusunu açmak için Yeni öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="552f4-107">Click New to open the drop dialog.</span></span>
3. <span data-ttu-id="552f4-108">Hesap yapısı alanında, hesap yapısının amacını açıklayan bir ad girin.</span><span class="sxs-lookup"><span data-stu-id="552f4-108">In the Account structure field, type a name to describe the purpose of the account structure.</span></span>
4. <span data-ttu-id="552f4-109">Açıklama alanında, hesap yapısının amacını belirten bir açıklama girin.</span><span class="sxs-lookup"><span data-stu-id="552f4-109">In the Description field, type a description to specify the purpose of the account structure.</span></span>
5. <span data-ttu-id="552f4-110">Oluştur'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="552f4-110">Click Create.</span></span>
6. <span data-ttu-id="552f4-111">Segment ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="552f4-111">Click Add segment.</span></span>
7. <span data-ttu-id="552f4-112">Boyutlar listesinde, hesap yapısına eklenecek boyutu seçin.</span><span class="sxs-lookup"><span data-stu-id="552f4-112">In the Dimensions list, select the dimension to add to the account structure.</span></span>
8. <span data-ttu-id="552f4-113">Segment ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="552f4-113">Click Add segment.</span></span>
9. <span data-ttu-id="552f4-114">Segment ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="552f4-114">Click Add segment.</span></span>
10. <span data-ttu-id="552f4-115">Boyutlar listesinde, hesap yapısına eklenecek boyutu seçin.</span><span class="sxs-lookup"><span data-stu-id="552f4-115">In the Dimensions list, select the dimension to add to the account structure.</span></span>
11. <span data-ttu-id="552f4-116">Segment ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="552f4-116">Click Add segment.</span></span>
12. <span data-ttu-id="552f4-117">Segment ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="552f4-117">Click Add segment.</span></span>
13. <span data-ttu-id="552f4-118">Boyutlar listesinde, hesap yapısına eklenecek boyutu seçin.</span><span class="sxs-lookup"><span data-stu-id="552f4-118">In the Dimensions list, select the dimension to add to the account structure.</span></span>
14. <span data-ttu-id="552f4-119">Segment ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="552f4-119">Click Add segment.</span></span>
15. <span data-ttu-id="552f4-120">Kılavuzda, izin verilen değerleri düzenlemek istediğiniz segmenti seçin.</span><span class="sxs-lookup"><span data-stu-id="552f4-120">In the grid, select the segment to edit the allowed values.</span></span>
    * <span data-ttu-id="552f4-121">Örneğin, Ana Hesap'ı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="552f4-121">For example, click in Main Account.</span></span>  
16. <span data-ttu-id="552f4-122">İşleç alanında, arasında ve içerir gibi bir seçenek belirleyin.</span><span class="sxs-lookup"><span data-stu-id="552f4-122">In the Operator field, select an option, such as is between and includes.</span></span>
17. <span data-ttu-id="552f4-123">Değer alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="552f4-123">In the Value field, type a value.</span></span>
    * <span data-ttu-id="552f4-124">Örneğin, 600000.</span><span class="sxs-lookup"><span data-stu-id="552f4-124">For example, 600000.</span></span>  
18. <span data-ttu-id="552f4-125">Aracılığıyla alanında bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="552f4-125">In the through field, type a value.</span></span>
    * <span data-ttu-id="552f4-126">Örneğin, 699999.</span><span class="sxs-lookup"><span data-stu-id="552f4-126">For example, 699999.</span></span>  
19. <span data-ttu-id="552f4-127">Uygula düğmesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="552f4-127">Click Apply.</span></span>
20. <span data-ttu-id="552f4-128">Kılavuzda, izin verilen değerleri düzenlemek istediğiniz segmenti seçin.</span><span class="sxs-lookup"><span data-stu-id="552f4-128">In the grid, select the segment to edit the allowed values.</span></span>
    * <span data-ttu-id="552f4-129">Örneğin, Departman.</span><span class="sxs-lookup"><span data-stu-id="552f4-129">For example, Department.</span></span>  
21. <span data-ttu-id="552f4-130">İşleç alanında, arasında ve içerir gibi bir seçenek belirleyin.</span><span class="sxs-lookup"><span data-stu-id="552f4-130">In the Operator field, select an option, such as is between and includes.</span></span>
22. <span data-ttu-id="552f4-131">Değer alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="552f4-131">In the Value field, type a value.</span></span>
    * <span data-ttu-id="552f4-132">Örneğin, 022.</span><span class="sxs-lookup"><span data-stu-id="552f4-132">For example, 022.</span></span>  
23. <span data-ttu-id="552f4-133">Aracılığıyla alanında bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="552f4-133">In the through field, type a value.</span></span>
    * <span data-ttu-id="552f4-134">Örneğin, 031.</span><span class="sxs-lookup"><span data-stu-id="552f4-134">For example, 031.</span></span>  
24. <span data-ttu-id="552f4-135">Yeni ölçüt ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="552f4-135">Click Add new criteria.</span></span>
25. <span data-ttu-id="552f4-136">İşleç alanında, arasında ve içerir gibi bir seçenek belirleyin.</span><span class="sxs-lookup"><span data-stu-id="552f4-136">In the Operator field, select an option, such as is between and includes.</span></span>
26. <span data-ttu-id="552f4-137">Değer alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="552f4-137">In the Value field, type a value.</span></span>
    * <span data-ttu-id="552f4-138">Örneğin, 033.</span><span class="sxs-lookup"><span data-stu-id="552f4-138">For example, 033.</span></span>  
27. <span data-ttu-id="552f4-139">Aracılığıyla alanında bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="552f4-139">In the through field, type a value.</span></span>
    * <span data-ttu-id="552f4-140">Örneğin, 034.</span><span class="sxs-lookup"><span data-stu-id="552f4-140">For example, 034.</span></span>  
28. <span data-ttu-id="552f4-141">Uygula düğmesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="552f4-141">Click Apply.</span></span>
29. <span data-ttu-id="552f4-142">Kılavuzda, izin verilen değerleri düzenlemek istediğiniz segmenti seçin.</span><span class="sxs-lookup"><span data-stu-id="552f4-142">In the grid, select the segment to edit the allowed values.</span></span>
    * <span data-ttu-id="552f4-143">Örneğin, Maliyet Merkezi.</span><span class="sxs-lookup"><span data-stu-id="552f4-143">For example, Cost Center.</span></span>  
30. <span data-ttu-id="552f4-144">Maliyet Merkezi alanında bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="552f4-144">In the CostCenter field, type a value.</span></span>
    * <span data-ttu-id="552f4-145">Örneğin, 007..021.</span><span class="sxs-lookup"><span data-stu-id="552f4-145">For example, 007..021.</span></span>  
31. <span data-ttu-id="552f4-146">Ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="552f4-146">Click Add.</span></span>
32. <span data-ttu-id="552f4-147">Ana Hesap alanında bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="552f4-147">In the MainAccount field, type a value.</span></span>
    * <span data-ttu-id="552f4-148">Örneğin, 600000..699999</span><span class="sxs-lookup"><span data-stu-id="552f4-148">For example, 600000..699999</span></span>  
33. <span data-ttu-id="552f4-149">Kılavuzda, izin verilen değerleri düzenlemek istediğiniz segmenti seçin.</span><span class="sxs-lookup"><span data-stu-id="552f4-149">In the grid, select the segment to edit the allowed values.</span></span>
    * <span data-ttu-id="552f4-150">Örneğin, Departman.</span><span class="sxs-lookup"><span data-stu-id="552f4-150">For example, Department.</span></span>  
34. <span data-ttu-id="552f4-151">Departman alanında bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="552f4-151">In the Department field, type a value.</span></span>
    * <span data-ttu-id="552f4-152">Örneğin, 032.</span><span class="sxs-lookup"><span data-stu-id="552f4-152">For example, 032.</span></span>  
35. <span data-ttu-id="552f4-153">Maliyet Merkezi alanında bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="552f4-153">In the CostCenter field, type a value.</span></span>
    * <span data-ttu-id="552f4-154">Örneğin, 086.</span><span class="sxs-lookup"><span data-stu-id="552f4-154">For example, 086.</span></span>  
36. <span data-ttu-id="552f4-155">Doğrula'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="552f4-155">Click Validate.</span></span>
37. <span data-ttu-id="552f4-156">Etkinleştir'i tıklatın.</span><span class="sxs-lookup"><span data-stu-id="552f4-156">Click Activate.</span></span>
38. <span data-ttu-id="552f4-157">Etkinleştir'i tıklatın.</span><span class="sxs-lookup"><span data-stu-id="552f4-157">Click Activate.</span></span>


