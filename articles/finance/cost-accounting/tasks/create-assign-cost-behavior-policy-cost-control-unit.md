---
title: Maliyet davranış ilkesi oluşturma ve bir maliyet kontrol birimine atama
description: Maliyet davranışı, maliyetlerin sabit veya değişken olarak sınıflandırılmasıdır.
author: ShylaThompson
manager: AnnBe
ms.date: 06/27/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CAMCostBehaviorRule
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 110ab87586c926d719537d2c30225d1630ce7710
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/15/2021
ms.locfileid: "4969315"
---
# <a name="create-and-assign-a-cost-behavior-policy-to-a-cost-control-unit"></a><span data-ttu-id="9e7c9-103">Maliyet davranış ilkesi oluşturma ve bir maliyet kontrol birimine atama</span><span class="sxs-lookup"><span data-stu-id="9e7c9-103">Create and assign a cost behavior policy to a cost control unit</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="9e7c9-104">Maliyet davranışı, maliyetlerin sabit veya değişken olarak sınıflandırılmasıdır.</span><span class="sxs-lookup"><span data-stu-id="9e7c9-104">Cost behavior is the classification of costs as either fixed or variable.</span></span> <span data-ttu-id="9e7c9-105">İlkenin etkin hale gelmesi için bir ilke ve karşılık gelen kurallarının bir maliyet kontrol birimine atanmış olması gerekir.</span><span class="sxs-lookup"><span data-stu-id="9e7c9-105">A policy and the corresponding rules have to be assigned to a cost control unit for the policy to become effective.</span></span> <span data-ttu-id="9e7c9-106">Bu yordamı bir ilke oluşturmak ve sonra ilkeyi bir maliyet kontrol birimine atamak için kullanın.</span><span class="sxs-lookup"><span data-stu-id="9e7c9-106">Use this procedure to create a policy and then assign the policy to a cost control unit.</span></span>


## <a name="create-a-cost-behavior-hierarchy"></a><span data-ttu-id="9e7c9-107">Bir maliyet davranış hiyerarşisi oluşturun</span><span class="sxs-lookup"><span data-stu-id="9e7c9-107">Create a cost behavior hierarchy</span></span>
1. <span data-ttu-id="9e7c9-108">Maliyet muhasebesi > Boyutlar > Boyut hiyerarşileri'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="9e7c9-108">Go to Cost accounting > Dimensions > Dimension hierarchies.</span></span>
2. <span data-ttu-id="9e7c9-109">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="9e7c9-109">Click New.</span></span>
3. <span data-ttu-id="9e7c9-110">Oluştur'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="9e7c9-110">Click Create.</span></span>
4. <span data-ttu-id="9e7c9-111">Boyut hiyerarşisi adı alanında 'Maliyet davranış hiyerarşisi' yazın.</span><span class="sxs-lookup"><span data-stu-id="9e7c9-111">In the Dimension hierarchy name field, type 'Cost behavior hierarchy'.</span></span>
5. <span data-ttu-id="9e7c9-112">Boyut alanına bir değer girin veya buradan bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="9e7c9-112">In the Dimension field, enter or select a value.</span></span>
    * <span data-ttu-id="9e7c9-113">Maliyet öğelerini seçin.</span><span class="sxs-lookup"><span data-stu-id="9e7c9-113">Select Cost elements.</span></span>  
6. <span data-ttu-id="9e7c9-114">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="9e7c9-114">Click Save.</span></span>
7. <span data-ttu-id="9e7c9-115">Hiyerarşiyi görüntüle düğmesini tıklayın.</span><span class="sxs-lookup"><span data-stu-id="9e7c9-115">Click View hierarchy.</span></span>
8. <span data-ttu-id="9e7c9-116">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="9e7c9-116">Click New.</span></span>
9. <span data-ttu-id="9e7c9-117">Düğüm adı alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="9e7c9-117">In the Node name field, type a value.</span></span>
    * <span data-ttu-id="9e7c9-118">Sabit maliyet girin.</span><span class="sxs-lookup"><span data-stu-id="9e7c9-118">Enter Fixed cost.</span></span>  
10. <span data-ttu-id="9e7c9-119">Ağaçta 'Maliyet davranış hiyerarşisi' seçin.</span><span class="sxs-lookup"><span data-stu-id="9e7c9-119">In the tree, select 'Cost behavior hierarchy'.</span></span>
11. <span data-ttu-id="9e7c9-120">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="9e7c9-120">Click New.</span></span>
12. <span data-ttu-id="9e7c9-121">Düğüm adı alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="9e7c9-121">In the Node name field, type a value.</span></span>
    * <span data-ttu-id="9e7c9-122">Değişken maliyet girin.</span><span class="sxs-lookup"><span data-stu-id="9e7c9-122">Enter Variable cost.</span></span>  
13. <span data-ttu-id="9e7c9-123">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="9e7c9-123">Click Save.</span></span>
14. <span data-ttu-id="9e7c9-124">Ağaçta 'Maliyet davranış hiyerarşisi\Sabit maliyet' seçin.</span><span class="sxs-lookup"><span data-stu-id="9e7c9-124">In the tree, select 'Cost behavior hierarchy\Fixed cost'.</span></span>
15. <span data-ttu-id="9e7c9-125">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="9e7c9-125">Click New.</span></span>
16. <span data-ttu-id="9e7c9-126">Listede, seçili satırı işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="9e7c9-126">In the list, mark the selected row.</span></span>
17. <span data-ttu-id="9e7c9-127">Gelen boyutu üyesi alanına bir değer girin veya bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="9e7c9-127">In the From dimension member field, enter or select a value.</span></span>
    * <span data-ttu-id="9e7c9-128">Boyut üyelerinin aralığı boşluklar içerebilir ancak üyeler üst üste gelemez.</span><span class="sxs-lookup"><span data-stu-id="9e7c9-128">The range of dimension members can contain gaps, but the members cannot overlap.</span></span>  
18. <span data-ttu-id="9e7c9-129">Boyuta üyesi alanına bir değer girin veya bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="9e7c9-129">In the To dimension member field, enter or select a value.</span></span>
    * <span data-ttu-id="9e7c9-130">Boyut üyelerinin aralığı boşluklar içerebilir ancak üyeler üst üste gelemez.</span><span class="sxs-lookup"><span data-stu-id="9e7c9-130">The range of dimension members can contain gaps, but the members cannot overlap.</span></span>  
19. <span data-ttu-id="9e7c9-131">Ağaçta 'Maliyet davranış hiyerarşisi\Değişken maliyet' seçin.</span><span class="sxs-lookup"><span data-stu-id="9e7c9-131">In the tree, select 'Cost behavior hierarchy\Variable cost'.</span></span>
20. <span data-ttu-id="9e7c9-132">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="9e7c9-132">Click New.</span></span>
21. <span data-ttu-id="9e7c9-133">Listede, seçili satırı işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="9e7c9-133">In the list, mark the selected row.</span></span>
22. <span data-ttu-id="9e7c9-134">Gelen boyutu üyesi alanına bir değer girin veya bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="9e7c9-134">In the From dimension member field, enter or select a value.</span></span>
    * <span data-ttu-id="9e7c9-135">Boyut üyelerinin aralığı boşluklar içerebilir ancak üyeler üst üste gelemez.</span><span class="sxs-lookup"><span data-stu-id="9e7c9-135">The range of dimension members can contain gaps, but the members cannot overlap.</span></span>  
23. <span data-ttu-id="9e7c9-136">Boyuta üyesi alanına bir değer girin veya bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="9e7c9-136">In the To dimension member field, enter or select a value.</span></span>
    * <span data-ttu-id="9e7c9-137">Boyut üyelerinin aralığı boşluklar içerebilir ancak üyeler üst üste gelemez.</span><span class="sxs-lookup"><span data-stu-id="9e7c9-137">The range of dimension members can contain gaps, but the members cannot overlap.</span></span>  
24. <span data-ttu-id="9e7c9-138">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="9e7c9-138">Click Save.</span></span>

## <a name="create-the-policy-and-rules"></a><span data-ttu-id="9e7c9-139">İlkeyi ve kuralları oluşturun</span><span class="sxs-lookup"><span data-stu-id="9e7c9-139">Create the policy and rules</span></span>
1. <span data-ttu-id="9e7c9-140">Maliyet muhasebesi > İlkeler > Maliyet davranış ilkeleri'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="9e7c9-140">Go to Cost accounting > Policies > Cost behavior policies.</span></span>
2. <span data-ttu-id="9e7c9-141">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="9e7c9-141">Click New.</span></span>
3. <span data-ttu-id="9e7c9-142">İlke adı alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="9e7c9-142">In the Policy name field, type a value.</span></span>
4. <span data-ttu-id="9e7c9-143">Maliyet öğesi boyut hiyerarşisi alanına bir değer girin veya bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="9e7c9-143">In the Cost element dimension hierarchy field, enter or select a value.</span></span>
    * <span data-ttu-id="9e7c9-144">Yeni oluşturduğunuz ilke hiyerarşisini seçin.</span><span class="sxs-lookup"><span data-stu-id="9e7c9-144">Select the policy hierarchy that you just created.</span></span>  
5. <span data-ttu-id="9e7c9-145">Maliyet nesnesi boyut hiyerarşisi alanına bir değer girin veya bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="9e7c9-145">In the Cost object dimension hierarchy field, enter or select a value.</span></span>
    * <span data-ttu-id="9e7c9-146">Kuruluşu seçin.</span><span class="sxs-lookup"><span data-stu-id="9e7c9-146">Select Organization.</span></span>  
6. <span data-ttu-id="9e7c9-147">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="9e7c9-147">Click Save.</span></span>
7. <span data-ttu-id="9e7c9-148">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="9e7c9-148">Click New.</span></span>
8. <span data-ttu-id="9e7c9-149">Listede, seçili satırı işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="9e7c9-149">In the list, mark the selected row.</span></span>
9. <span data-ttu-id="9e7c9-150">Maliyet öğesi boyut hiyerarşi düğümü alanına bir değer girin veya bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="9e7c9-150">In the Cost element dimension hierarchy node field, enter or select a value.</span></span>
    * <span data-ttu-id="9e7c9-151">Değişken maliyeti seçmek için hiyerarşiyi genişletin.</span><span class="sxs-lookup"><span data-stu-id="9e7c9-151">Expand the hierarchy to select Variable cost.</span></span>  
10. <span data-ttu-id="9e7c9-152">Maliyet nesnesi boyut hiyerarşi düğümü alanına bir değer girin veya bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="9e7c9-152">In the Cost object dimension hierarchy node field, enter or select a value.</span></span>
    * <span data-ttu-id="9e7c9-153">Varsayılan olarak, değişken yüzdesi 100'dür.</span><span class="sxs-lookup"><span data-stu-id="9e7c9-153">By default, the variable percentage is 100 percent.</span></span>  
11. <span data-ttu-id="9e7c9-154">Maliyet kontrol birimi için ilke atamaları'na tıklayın.</span><span class="sxs-lookup"><span data-stu-id="9e7c9-154">Click Policy assignments for cost control unit.</span></span>
12. <span data-ttu-id="9e7c9-155">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="9e7c9-155">Click New.</span></span>
13. <span data-ttu-id="9e7c9-156">Listede, seçili satırı işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="9e7c9-156">In the list, mark the selected row.</span></span>
14. <span data-ttu-id="9e7c9-157">Geçerlilik tarihi muhasebe veri alanına bir tarih girin.</span><span class="sxs-lookup"><span data-stu-id="9e7c9-157">In the Valid from accounting date field, enter a date.</span></span>
    * <span data-ttu-id="9e7c9-158">Kurallar tarihe dayalıdır ve kullanıcı veya sistem kuralın süresini, daha yeni bir sürüm oluşturulursa doldurulabilir.</span><span class="sxs-lookup"><span data-stu-id="9e7c9-158">The rules are date-effective, and a user or the system can expire a rule if a newer version is created.</span></span>  
15. <span data-ttu-id="9e7c9-159">Maliyet kontrol birimi alanına bir değer girin veya bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="9e7c9-159">In the Cost control unit field, enter or select a value.</span></span>
16. <span data-ttu-id="9e7c9-160">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="9e7c9-160">Click Save.</span></span>

