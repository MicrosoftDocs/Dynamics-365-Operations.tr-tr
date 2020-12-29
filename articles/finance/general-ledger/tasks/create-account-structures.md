---
title: Hesap yapıları oluşturma
description: Bu görev kılavuzu, hesap yapısı oluşturmayı adım adım açıklar.
author: aprilolson
manager: AnnBe
ms.date: 07/01/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DimensionConfigureAccountStructure, DimensionCreateAccountStructure, DimensionHierarchyAddLevel, DimensionHierarchyConstraintActivate
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b75ee76a1fb874652415a2174441f629955d763a
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "4448892"
---
# <a name="create-account-structures"></a><span data-ttu-id="ab92b-103">Hesap yapıları oluşturma</span><span class="sxs-lookup"><span data-stu-id="ab92b-103">Create account structures</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="ab92b-104">Bu görev kılavuzu, hesap yapısı oluşturmayı adım adım açıklar.</span><span class="sxs-lookup"><span data-stu-id="ab92b-104">This task guide steps through creating an account structure.</span></span> <span data-ttu-id="ab92b-105">Adımlarda demo veri şirketi USMF kullanılmaktadır.</span><span class="sxs-lookup"><span data-stu-id="ab92b-105">The steps use demo data company USMF.</span></span>

1. <span data-ttu-id="ab92b-106">**Gezinti bölmesi > Modüller > Genel muhasebe > Hesap planı > Yapılar > Hesap yapılarını yapılandır**'a gidin.</span><span class="sxs-lookup"><span data-stu-id="ab92b-106">Go to **Navigation pane > Modules > General ledger > Chart of accounts > Structures > Configure account structures**.</span></span>
2. <span data-ttu-id="ab92b-107">**Eylem bölmesi**'nde, bırakma iletişim kutusunu açmak için **Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="ab92b-107">On the **Action pane**, click **New** to open the drop dialog.</span></span>
3. <span data-ttu-id="ab92b-108">**Hesap yapısı** alanında, hesap yapısının amacını açıklayan bir ad girin.</span><span class="sxs-lookup"><span data-stu-id="ab92b-108">In the **Account structure** field, type a name to describe the purpose of the account structure.</span></span>
4. <span data-ttu-id="ab92b-109">**Açıklama** alanında, hesap yapısının amacını belirten bir açıklama girin.</span><span class="sxs-lookup"><span data-stu-id="ab92b-109">In the **Description** field, type a description to specify the purpose of the account structure.</span></span>
5. <span data-ttu-id="ab92b-110">**Oluştur**'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ab92b-110">Click **Create**.</span></span>
6. <span data-ttu-id="ab92b-111">**Segmentler ve izin verilen değerler**'de **Segment ekle**'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ab92b-111">In the **Segments and allowed values**, click **Add segment**.</span></span>
7. <span data-ttu-id="ab92b-112">Boyutlar listesinde, hesap yapısına eklenecek boyutu seçin.</span><span class="sxs-lookup"><span data-stu-id="ab92b-112">In the dimensions list, select the dimension to add to the account structure.</span></span>
8. <span data-ttu-id="ab92b-113">Listenin sonunda **Segment ekle**'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ab92b-113">At the end of the list, click **Add segment**.</span></span>
9. <span data-ttu-id="ab92b-114">6-9 arası adımları gerektiği şekilde yineleyin.</span><span class="sxs-lookup"><span data-stu-id="ab92b-114">Repeat step 6 to 9 as needed.</span></span>
10. <span data-ttu-id="ab92b-115">**İzin verilen değerler** bölümünde izin verilen değerlerini düzenlemek istediğiniz segmenti seçin.</span><span class="sxs-lookup"><span data-stu-id="ab92b-115">In the **Allowed value details** section, select the segment to edit the allowed values.</span></span>
    <span data-ttu-id="ab92b-116">Örneğin, **Ana Hesap** alanına tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ab92b-116">For example, click the **Main Account** field.</span></span>  
11. <span data-ttu-id="ab92b-117">**İşleç** alanında, arasında ve içerir gibi bir seçenek belirleyin.</span><span class="sxs-lookup"><span data-stu-id="ab92b-117">In the **Operator** field, select an option, such as is between and includes.</span></span>
12. <span data-ttu-id="ab92b-118">**Değer** alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="ab92b-118">In the **Value** field, type a value.</span></span> <span data-ttu-id="ab92b-119">Örneğin, 600000.</span><span class="sxs-lookup"><span data-stu-id="ab92b-119">For example, 600000.</span></span>  
13. <span data-ttu-id="ab92b-120">**Aracılığıyla** alanında bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="ab92b-120">In the **through** field, type a value.</span></span> <span data-ttu-id="ab92b-121">Örneğin, 699999.</span><span class="sxs-lookup"><span data-stu-id="ab92b-121">For example, 699999.</span></span>  
14. <span data-ttu-id="ab92b-122">**İzin verilen değer ayrıntıları** bölümünde, **Uygula**'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ab92b-122">In the **Allowed value details** section, click **Apply**.</span></span>
15. <span data-ttu-id="ab92b-123">10-15 arası adımları gerektiği şekilde yineleyin.</span><span class="sxs-lookup"><span data-stu-id="ab92b-123">Repeat step 10 to 15 as needed.</span></span>  
16. <span data-ttu-id="ab92b-124">**İzin verilen değer ayrıntıları** bölümünde, **Yeni ölçüt ekle**'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ab92b-124">In the **Allowed value details** section, click **Add new criteria**.</span></span>
17. <span data-ttu-id="ab92b-125">İşleç alanında, arasında ve içerir gibi bir seçenek belirleyin.</span><span class="sxs-lookup"><span data-stu-id="ab92b-125">In the Operator field, select an option, such as is between and includes.</span></span>
18. <span data-ttu-id="ab92b-126">**Değer** alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="ab92b-126">In the **Value** field, type a value.</span></span> <span data-ttu-id="ab92b-127">Örneğin, 033.</span><span class="sxs-lookup"><span data-stu-id="ab92b-127">For example, 033.</span></span>  
19. <span data-ttu-id="ab92b-128">**Aracılığıyla** alanında bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="ab92b-128">In the **through** field, type a value.</span></span> <span data-ttu-id="ab92b-129">Örneğin, 034.</span><span class="sxs-lookup"><span data-stu-id="ab92b-129">For example, 034.</span></span>  
20. <span data-ttu-id="ab92b-130">**Uygula**'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ab92b-130">Click **Apply**.</span></span>
21. <span data-ttu-id="ab92b-131">Kılavuzda, izin verilen değerleri düzenlemek istediğiniz segmenti seçin.</span><span class="sxs-lookup"><span data-stu-id="ab92b-131">In the grid, select the segment to edit the allowed values.</span></span> <span data-ttu-id="ab92b-132">Örneğin, Maliyet Merkezi.</span><span class="sxs-lookup"><span data-stu-id="ab92b-132">For example, Cost Center.</span></span>  
22. <span data-ttu-id="ab92b-133">**Maliyet Merkezi** alanında bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="ab92b-133">In the **CostCenter field**, type a value.</span></span> <span data-ttu-id="ab92b-134">Örneğin, 007..021.</span><span class="sxs-lookup"><span data-stu-id="ab92b-134">For example, 007..021.</span></span>  
23. <span data-ttu-id="ab92b-135">**Segmentler ve izin verilen değerler**'de **Ekle**'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ab92b-135">In the **Segments and allowed values**, click **Add**.</span></span>
24. <span data-ttu-id="ab92b-136">**Ana Hesap** alanında bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="ab92b-136">In the **MainAccount** field, type a value.</span></span> <span data-ttu-id="ab92b-137">Örneğin, 600000..699999</span><span class="sxs-lookup"><span data-stu-id="ab92b-137">For example, 600000..699999</span></span>  
25. <span data-ttu-id="ab92b-138">Kılavuzda, izin verilen değerleri düzenlemek istediğiniz segmenti seçin.</span><span class="sxs-lookup"><span data-stu-id="ab92b-138">In the grid, select the segment to edit the allowed values.</span></span> <span data-ttu-id="ab92b-139">Örneğin, Departman.</span><span class="sxs-lookup"><span data-stu-id="ab92b-139">For example, Department.</span></span>  
26. <span data-ttu-id="ab92b-140">Departman alanında bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="ab92b-140">In the Department field, type a value.</span></span> <span data-ttu-id="ab92b-141">Örneğin, 032.</span><span class="sxs-lookup"><span data-stu-id="ab92b-141">For example, 032.</span></span>  
27. <span data-ttu-id="ab92b-142">Maliyet Merkezi alanında bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="ab92b-142">In the CostCenter field, type a value.</span></span> <span data-ttu-id="ab92b-143">Örneğin, 086.</span><span class="sxs-lookup"><span data-stu-id="ab92b-143">For example, 086.</span></span>  
28. <span data-ttu-id="ab92b-144">**Eylem Bölmesinde**,  **Doğrula** öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ab92b-144">On the **Action pane**, click **Validate**.</span></span>
29. <span data-ttu-id="ab92b-145">**Eylem Bölmesinde** **Etkinleştir** öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ab92b-145">On the **Action pane**, click **Activate**.</span></span>
30. <span data-ttu-id="ab92b-146">**Etkinleştir**'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ab92b-146">Click **Activate**.</span></span>

