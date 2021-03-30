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
ms.openlocfilehash: 58f888a373af33832c24518fbb5483c3de2d1a58
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5208715"
---
# <a name="create-and-assign-a-cost-behavior-policy-to-a-cost-control-unit"></a><span data-ttu-id="fc3e3-103">Maliyet davranış ilkesi oluşturma ve bir maliyet kontrol birimine atama</span><span class="sxs-lookup"><span data-stu-id="fc3e3-103">Create and assign a cost behavior policy to a cost control unit</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="fc3e3-104">Maliyet davranışı, maliyetlerin sabit veya değişken olarak sınıflandırılmasıdır.</span><span class="sxs-lookup"><span data-stu-id="fc3e3-104">Cost behavior is the classification of costs as either fixed or variable.</span></span> <span data-ttu-id="fc3e3-105">İlkenin etkin hale gelmesi için bir ilke ve karşılık gelen kurallarının bir maliyet kontrol birimine atanmış olması gerekir.</span><span class="sxs-lookup"><span data-stu-id="fc3e3-105">A policy and the corresponding rules have to be assigned to a cost control unit for the policy to become effective.</span></span> <span data-ttu-id="fc3e3-106">Bu yordamı bir ilke oluşturmak ve sonra ilkeyi bir maliyet kontrol birimine atamak için kullanın.</span><span class="sxs-lookup"><span data-stu-id="fc3e3-106">Use this procedure to create a policy and then assign the policy to a cost control unit.</span></span>


## <a name="create-a-cost-behavior-hierarchy"></a><span data-ttu-id="fc3e3-107">Bir maliyet davranış hiyerarşisi oluşturun</span><span class="sxs-lookup"><span data-stu-id="fc3e3-107">Create a cost behavior hierarchy</span></span>
1. <span data-ttu-id="fc3e3-108">Maliyet muhasebesi > Boyutlar > Boyut hiyerarşileri'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="fc3e3-108">Go to Cost accounting > Dimensions > Dimension hierarchies.</span></span>
2. <span data-ttu-id="fc3e3-109">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="fc3e3-109">Click New.</span></span>
3. <span data-ttu-id="fc3e3-110">Oluştur'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="fc3e3-110">Click Create.</span></span>
4. <span data-ttu-id="fc3e3-111">Boyut hiyerarşisi adı alanında 'Maliyet davranış hiyerarşisi' yazın.</span><span class="sxs-lookup"><span data-stu-id="fc3e3-111">In the Dimension hierarchy name field, type 'Cost behavior hierarchy'.</span></span>
5. <span data-ttu-id="fc3e3-112">Boyut alanına bir değer girin veya buradan bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="fc3e3-112">In the Dimension field, enter or select a value.</span></span>
    * <span data-ttu-id="fc3e3-113">Maliyet öğelerini seçin.</span><span class="sxs-lookup"><span data-stu-id="fc3e3-113">Select Cost elements.</span></span>  
6. <span data-ttu-id="fc3e3-114">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="fc3e3-114">Click Save.</span></span>
7. <span data-ttu-id="fc3e3-115">Hiyerarşiyi görüntüle düğmesini tıklayın.</span><span class="sxs-lookup"><span data-stu-id="fc3e3-115">Click View hierarchy.</span></span>
8. <span data-ttu-id="fc3e3-116">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="fc3e3-116">Click New.</span></span>
9. <span data-ttu-id="fc3e3-117">Düğüm adı alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="fc3e3-117">In the Node name field, type a value.</span></span>
    * <span data-ttu-id="fc3e3-118">Sabit maliyet girin.</span><span class="sxs-lookup"><span data-stu-id="fc3e3-118">Enter Fixed cost.</span></span>  
10. <span data-ttu-id="fc3e3-119">Ağaçta 'Maliyet davranış hiyerarşisi' seçin.</span><span class="sxs-lookup"><span data-stu-id="fc3e3-119">In the tree, select 'Cost behavior hierarchy'.</span></span>
11. <span data-ttu-id="fc3e3-120">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="fc3e3-120">Click New.</span></span>
12. <span data-ttu-id="fc3e3-121">Düğüm adı alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="fc3e3-121">In the Node name field, type a value.</span></span>
    * <span data-ttu-id="fc3e3-122">Değişken maliyet girin.</span><span class="sxs-lookup"><span data-stu-id="fc3e3-122">Enter Variable cost.</span></span>  
13. <span data-ttu-id="fc3e3-123">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="fc3e3-123">Click Save.</span></span>
14. <span data-ttu-id="fc3e3-124">Ağaçta 'Maliyet davranış hiyerarşisi\Sabit maliyet' seçin.</span><span class="sxs-lookup"><span data-stu-id="fc3e3-124">In the tree, select 'Cost behavior hierarchy\Fixed cost'.</span></span>
15. <span data-ttu-id="fc3e3-125">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="fc3e3-125">Click New.</span></span>
16. <span data-ttu-id="fc3e3-126">Listede, seçili satırı işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="fc3e3-126">In the list, mark the selected row.</span></span>
17. <span data-ttu-id="fc3e3-127">Gelen boyutu üyesi alanına bir değer girin veya bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="fc3e3-127">In the From dimension member field, enter or select a value.</span></span>
    * <span data-ttu-id="fc3e3-128">Boyut üyelerinin aralığı boşluklar içerebilir ancak üyeler üst üste gelemez.</span><span class="sxs-lookup"><span data-stu-id="fc3e3-128">The range of dimension members can contain gaps, but the members cannot overlap.</span></span>  
18. <span data-ttu-id="fc3e3-129">Boyuta üyesi alanına bir değer girin veya bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="fc3e3-129">In the To dimension member field, enter or select a value.</span></span>
    * <span data-ttu-id="fc3e3-130">Boyut üyelerinin aralığı boşluklar içerebilir ancak üyeler üst üste gelemez.</span><span class="sxs-lookup"><span data-stu-id="fc3e3-130">The range of dimension members can contain gaps, but the members cannot overlap.</span></span>  
19. <span data-ttu-id="fc3e3-131">Ağaçta 'Maliyet davranış hiyerarşisi\Değişken maliyet' seçin.</span><span class="sxs-lookup"><span data-stu-id="fc3e3-131">In the tree, select 'Cost behavior hierarchy\Variable cost'.</span></span>
20. <span data-ttu-id="fc3e3-132">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="fc3e3-132">Click New.</span></span>
21. <span data-ttu-id="fc3e3-133">Listede, seçili satırı işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="fc3e3-133">In the list, mark the selected row.</span></span>
22. <span data-ttu-id="fc3e3-134">Gelen boyutu üyesi alanına bir değer girin veya bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="fc3e3-134">In the From dimension member field, enter or select a value.</span></span>
    * <span data-ttu-id="fc3e3-135">Boyut üyelerinin aralığı boşluklar içerebilir ancak üyeler üst üste gelemez.</span><span class="sxs-lookup"><span data-stu-id="fc3e3-135">The range of dimension members can contain gaps, but the members cannot overlap.</span></span>  
23. <span data-ttu-id="fc3e3-136">Boyuta üyesi alanına bir değer girin veya bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="fc3e3-136">In the To dimension member field, enter or select a value.</span></span>
    * <span data-ttu-id="fc3e3-137">Boyut üyelerinin aralığı boşluklar içerebilir ancak üyeler üst üste gelemez.</span><span class="sxs-lookup"><span data-stu-id="fc3e3-137">The range of dimension members can contain gaps, but the members cannot overlap.</span></span>  
24. <span data-ttu-id="fc3e3-138">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="fc3e3-138">Click Save.</span></span>

## <a name="create-the-policy-and-rules"></a><span data-ttu-id="fc3e3-139">İlkeyi ve kuralları oluşturun</span><span class="sxs-lookup"><span data-stu-id="fc3e3-139">Create the policy and rules</span></span>
1. <span data-ttu-id="fc3e3-140">Maliyet muhasebesi > İlkeler > Maliyet davranış ilkeleri'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="fc3e3-140">Go to Cost accounting > Policies > Cost behavior policies.</span></span>
2. <span data-ttu-id="fc3e3-141">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="fc3e3-141">Click New.</span></span>
3. <span data-ttu-id="fc3e3-142">İlke adı alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="fc3e3-142">In the Policy name field, type a value.</span></span>
4. <span data-ttu-id="fc3e3-143">Maliyet öğesi boyut hiyerarşisi alanına bir değer girin veya bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="fc3e3-143">In the Cost element dimension hierarchy field, enter or select a value.</span></span>
    * <span data-ttu-id="fc3e3-144">Yeni oluşturduğunuz ilke hiyerarşisini seçin.</span><span class="sxs-lookup"><span data-stu-id="fc3e3-144">Select the policy hierarchy that you just created.</span></span>  
5. <span data-ttu-id="fc3e3-145">Maliyet nesnesi boyut hiyerarşisi alanına bir değer girin veya bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="fc3e3-145">In the Cost object dimension hierarchy field, enter or select a value.</span></span>
    * <span data-ttu-id="fc3e3-146">Kuruluşu seçin.</span><span class="sxs-lookup"><span data-stu-id="fc3e3-146">Select Organization.</span></span>  
6. <span data-ttu-id="fc3e3-147">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="fc3e3-147">Click Save.</span></span>
7. <span data-ttu-id="fc3e3-148">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="fc3e3-148">Click New.</span></span>
8. <span data-ttu-id="fc3e3-149">Listede, seçili satırı işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="fc3e3-149">In the list, mark the selected row.</span></span>
9. <span data-ttu-id="fc3e3-150">Maliyet öğesi boyut hiyerarşi düğümü alanına bir değer girin veya bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="fc3e3-150">In the Cost element dimension hierarchy node field, enter or select a value.</span></span>
    * <span data-ttu-id="fc3e3-151">Değişken maliyeti seçmek için hiyerarşiyi genişletin.</span><span class="sxs-lookup"><span data-stu-id="fc3e3-151">Expand the hierarchy to select Variable cost.</span></span>  
10. <span data-ttu-id="fc3e3-152">Maliyet nesnesi boyut hiyerarşi düğümü alanına bir değer girin veya bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="fc3e3-152">In the Cost object dimension hierarchy node field, enter or select a value.</span></span>
    * <span data-ttu-id="fc3e3-153">Varsayılan olarak, değişken yüzdesi 100'dür.</span><span class="sxs-lookup"><span data-stu-id="fc3e3-153">By default, the variable percentage is 100 percent.</span></span>  
11. <span data-ttu-id="fc3e3-154">Maliyet kontrol birimi için ilke atamaları'na tıklayın.</span><span class="sxs-lookup"><span data-stu-id="fc3e3-154">Click Policy assignments for cost control unit.</span></span>
12. <span data-ttu-id="fc3e3-155">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="fc3e3-155">Click New.</span></span>
13. <span data-ttu-id="fc3e3-156">Listede, seçili satırı işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="fc3e3-156">In the list, mark the selected row.</span></span>
14. <span data-ttu-id="fc3e3-157">Geçerlilik tarihi muhasebe veri alanına bir tarih girin.</span><span class="sxs-lookup"><span data-stu-id="fc3e3-157">In the Valid from accounting date field, enter a date.</span></span>
    * <span data-ttu-id="fc3e3-158">Kurallar tarihe dayalıdır ve kullanıcı veya sistem kuralın süresini, daha yeni bir sürüm oluşturulursa doldurulabilir.</span><span class="sxs-lookup"><span data-stu-id="fc3e3-158">The rules are date-effective, and a user or the system can expire a rule if a newer version is created.</span></span>  
15. <span data-ttu-id="fc3e3-159">Maliyet kontrol birimi alanına bir değer girin veya bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="fc3e3-159">In the Cost control unit field, enter or select a value.</span></span>
16. <span data-ttu-id="fc3e3-160">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="fc3e3-160">Click Save.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]