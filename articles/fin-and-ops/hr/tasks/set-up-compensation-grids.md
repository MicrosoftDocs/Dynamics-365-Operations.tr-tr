---
title: Ücreti kademeleri ayarlama
description: Ücret kılavuzları, sabit ücret planları için ödeme yapıları tanımlamak ve sağlamak için kullanılır.
author: andreabichsel
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: HRCCompGrid, HRCCompGridView
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f0caebb2dfbff12545610aa6438dccbec84db3f9
ms.sourcegitcommit: 608e68b603afef9eb98d8fb25e90109c2473ef87
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/19/2019
ms.locfileid: "856773"
---
# <a name="set-up-compensation-grids"></a><span data-ttu-id="073cb-103">Ücreti kademeleri ayarlama</span><span class="sxs-lookup"><span data-stu-id="073cb-103">Set up compensation grids</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="073cb-104">Ücret kılavuzları, sabit ücret planları için ödeme yapıları tanımlamak ve sağlamak için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="073cb-104">Compensation grids are used to define and maintain the pay structures for fixed compensation plans.</span></span> <span data-ttu-id="073cb-105">Ücret kılavuzları, birden çok plan arasında paylaşılır veya yeni bir ücret planı oluştururken kopyalanabilir.</span><span class="sxs-lookup"><span data-stu-id="073cb-105">Compensation grids can be shared between multiple plans or copied when creating a new compensation plan.</span></span>  <span data-ttu-id="073cb-106">Bir ücret kılavuzu oluşturmadan önce Düzeyler ve Referans noktaları ayarlanmalıdır.</span><span class="sxs-lookup"><span data-stu-id="073cb-106">Before creating a compensation grid, Levels and Reference points must be set up.</span></span> <span data-ttu-id="073cb-107">Bu örnek, Düzeyler ve Referans noktaları için demo verilerini kullanarak yeni bir ücret Derece türü oluşturur.</span><span class="sxs-lookup"><span data-stu-id="073cb-107">This example will create a new Grade type of compensation grid using demo data for the Levels and Reference points.</span></span> <span data-ttu-id="073cb-108">Bu yöntemi oluşturmak için kullanılan demo veri şirketi USMF'dir.</span><span class="sxs-lookup"><span data-stu-id="073cb-108">The demo data company used to create this procedure is USMF.</span></span>


## <a name="set-up-information-about-the-compensation-grid"></a><span data-ttu-id="073cb-109">Ücret kılavuzuyla ilgili bilgileri ayarlama</span><span class="sxs-lookup"><span data-stu-id="073cb-109">Set up information about the compensation grid</span></span>
1. <span data-ttu-id="073cb-110">İnsan kaynakları > Ücret > Sabit ücret > Ücret kılavuzları'na gidin.</span><span class="sxs-lookup"><span data-stu-id="073cb-110">Go to Human resources > Compensation > Fixed compensation > Compensation grids.</span></span>
2. <span data-ttu-id="073cb-111">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="073cb-111">Click New.</span></span>
3. <span data-ttu-id="073cb-112">Kılavuz alanında bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="073cb-112">In the Grid field, type a value.</span></span>
4. <span data-ttu-id="073cb-113">Açıklama alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="073cb-113">In the Description field, type a value.</span></span>
5. <span data-ttu-id="073cb-114">Tür alanında, bir seçenek seçin.</span><span class="sxs-lookup"><span data-stu-id="073cb-114">In the Type field, select an option.</span></span>
6. <span data-ttu-id="073cb-115">Referans ayarı alanında bir değer girin veya bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="073cb-115">In the Reference setup field, enter or select a value.</span></span>
7. <span data-ttu-id="073cb-116">Para birimi alanında bir değer girin veya bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="073cb-116">In the Currency field, enter or select a value.</span></span>
8. <span data-ttu-id="073cb-117">Para birimi alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="073cb-117">In the Currency field, type a value.</span></span>
9. <span data-ttu-id="073cb-118">Yürürlük tarihi alanına bir tarih girin.</span><span class="sxs-lookup"><span data-stu-id="073cb-118">In the Effective date field, enter a date.</span></span>

## <a name="add-levels-to-the-compensation-structure"></a><span data-ttu-id="073cb-119">Ücret yapısına düzey ekleme</span><span class="sxs-lookup"><span data-stu-id="073cb-119">Add levels to the compensation structure</span></span>
1. <span data-ttu-id="073cb-120">Ücret yapısı'nı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="073cb-120">Click Compensation structure.</span></span>
2. <span data-ttu-id="073cb-121">Listede, seçili satırı işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="073cb-121">In the list, mark the selected row.</span></span>
3. <span data-ttu-id="073cb-122">Düzey alanında bir değer girin veya bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="073cb-122">In the Level field, enter or select a value.</span></span>
4. <span data-ttu-id="073cb-123">Yeni'yi tıklatın.</span><span class="sxs-lookup"><span data-stu-id="073cb-123">Click New.</span></span>
5. <span data-ttu-id="073cb-124">Listede, seçili satırı işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="073cb-124">In the list, mark the selected row.</span></span>
6. <span data-ttu-id="073cb-125">Düzey alanında bir değer girin veya bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="073cb-125">In the Level field, enter or select a value.</span></span>
7. <span data-ttu-id="073cb-126">Yeni'yi tıklatın.</span><span class="sxs-lookup"><span data-stu-id="073cb-126">Click New.</span></span>
8. <span data-ttu-id="073cb-127">Listede, seçili satırı işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="073cb-127">In the list, mark the selected row.</span></span>
9. <span data-ttu-id="073cb-128">Düzey alanında bir değer girin veya bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="073cb-128">In the Level field, enter or select a value.</span></span>
10. <span data-ttu-id="073cb-129">Yeni'yi tıklatın.</span><span class="sxs-lookup"><span data-stu-id="073cb-129">Click New.</span></span>
11. <span data-ttu-id="073cb-130">Listede, seçili satırı işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="073cb-130">In the list, mark the selected row.</span></span>
12. <span data-ttu-id="073cb-131">Düzey alanında bir değer girin veya bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="073cb-131">In the Level field, enter or select a value.</span></span>
13. <span data-ttu-id="073cb-132">Yeni'yi tıklatın.</span><span class="sxs-lookup"><span data-stu-id="073cb-132">Click New.</span></span>
14. <span data-ttu-id="073cb-133">Listede, seçili satırı işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="073cb-133">In the list, mark the selected row.</span></span>
15. <span data-ttu-id="073cb-134">Düzey alanında bir değer girin veya bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="073cb-134">In the Level field, enter or select a value.</span></span>

## <a name="fill-in-the-compensation-structure-with-values"></a><span data-ttu-id="073cb-135">Ücret yapısını değerlerle doldurma</span><span class="sxs-lookup"><span data-stu-id="073cb-135">Fill in the compensation structure with values</span></span>
1. <span data-ttu-id="073cb-136">Listede, seçili satırı işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="073cb-136">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="073cb-137">Bu noktada, ücret değerleri tablodaki her bir alanda el ile girilebilir ya da Toplu değiştirme işlevi kullanılarak birden fazla alan kolayca doldurabilir ve temel hesaplamalar gerçekleştirilebilir.</span><span class="sxs-lookup"><span data-stu-id="073cb-137">At this point, compensation values can manually be entered into each field in the table, or the Mass change functionality can be used to easily fill in multiple fields and perform basic calculations.</span></span>  
2. <span data-ttu-id="073cb-138">Toplu değişiklik seçeneğine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="073cb-138">Click Mass change.</span></span>
    * <span data-ttu-id="073cb-139">Bu kılavuz için, ilk önce birinci düzeyin orta noktasının değeri tablodaki tüm alanlara uygulanır.</span><span class="sxs-lookup"><span data-stu-id="073cb-139">For this grid, we'll first apply the value for the midpoint of the first level's to all the fields in the table.</span></span> <span data-ttu-id="073cb-140">Bu, ücret matrisi için esas alınacaktır.</span><span class="sxs-lookup"><span data-stu-id="073cb-140">This will be the basis for the compensation matrix.</span></span>  
3. <span data-ttu-id="073cb-141">Ayarlama türü alanında bir seçenek belirleyin.</span><span class="sxs-lookup"><span data-stu-id="073cb-141">In the Adjustment type field, select an option.</span></span>
4. <span data-ttu-id="073cb-142">Ayarlama tutarı alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="073cb-142">In the Adjustment amount field, enter a number.</span></span>
5. <span data-ttu-id="073cb-143">Listede, tüm satırları işaretleyin veya tüm satırların işaretlerini kaldırın.</span><span class="sxs-lookup"><span data-stu-id="073cb-143">In the list, mark or unmark all rows.</span></span>
6. <span data-ttu-id="073cb-144">Kılavuza uygula'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="073cb-144">Click Apply to grid.</span></span>
    * <span data-ttu-id="073cb-145">Ardından, miktarları sonraki her düzeyde belirli bir yüzde veya miktarda artırmak için toplu değiştirme işlevi kullanılır.</span><span class="sxs-lookup"><span data-stu-id="073cb-145">Now we'll use the mass change function to increment the amounts in each subsequent level by a certain percentage or amount.</span></span> <span data-ttu-id="073cb-146">Bu örnekte, her derecenin kendi orta noktaları arasında %12,5'luk bir fark olacaktır.</span><span class="sxs-lookup"><span data-stu-id="073cb-146">In this example, each grade will have a 12.5% spread between their midpoints.</span></span>  
7. <span data-ttu-id="073cb-147">Ayarlama türü alanında bir seçenek belirleyin.</span><span class="sxs-lookup"><span data-stu-id="073cb-147">In the Adjustment type field, select an option.</span></span>
8. <span data-ttu-id="073cb-148">Ayarlama tutarı alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="073cb-148">In the Adjustment amount field, enter a number.</span></span>
9. <span data-ttu-id="073cb-149">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="073cb-149">In the list, find and select the desired record.</span></span>
10. <span data-ttu-id="073cb-150">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="073cb-150">In the list, find and select the desired record.</span></span>
11. <span data-ttu-id="073cb-151">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="073cb-151">In the list, find and select the desired record.</span></span>
12. <span data-ttu-id="073cb-152">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="073cb-152">In the list, find and select the desired record.</span></span>
13. <span data-ttu-id="073cb-153">Kılavuza uygula'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="073cb-153">Click Apply to grid.</span></span>
14. <span data-ttu-id="073cb-154">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="073cb-154">In the list, find and select the desired record.</span></span>
15. <span data-ttu-id="073cb-155">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="073cb-155">In the list, find and select the desired record.</span></span>
16. <span data-ttu-id="073cb-156">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="073cb-156">In the list, find and select the desired record.</span></span>
17. <span data-ttu-id="073cb-157">Kılavuza uygula'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="073cb-157">Click Apply to grid.</span></span>
18. <span data-ttu-id="073cb-158">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="073cb-158">In the list, find and select the desired record.</span></span>
19. <span data-ttu-id="073cb-159">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="073cb-159">In the list, find and select the desired record.</span></span>
20. <span data-ttu-id="073cb-160">Kılavuza uygula'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="073cb-160">Click Apply to grid.</span></span>
21. <span data-ttu-id="073cb-161">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="073cb-161">In the list, find and select the desired record.</span></span>
22. <span data-ttu-id="073cb-162">Kılavuza uygula'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="073cb-162">Click Apply to grid.</span></span>
    * <span data-ttu-id="073cb-163">Her düzey için Minimum ve Maksimum referans noktaları ayarlamak üzere toplu değiştirme işlevi kullanılır.</span><span class="sxs-lookup"><span data-stu-id="073cb-163">Now we'll use the mass change function to adjust the Minimum and Maximum reference points for each level.</span></span> <span data-ttu-id="073cb-164">Bu örnek %50 fark değeri kullanır, böylece Minimum referans noktası - %20 ve Maksimum referans noktası olarak +%20 olarak ayarlanır.</span><span class="sxs-lookup"><span data-stu-id="073cb-164">This example will use a 50% spread so the Minimum reference point will be adjusted -20% and the Maximum will be adjusted +20%.</span></span>  
23. <span data-ttu-id="073cb-165">Ayarlama tutarı alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="073cb-165">In the Adjustment amount field, enter a number.</span></span>
24. <span data-ttu-id="073cb-166">Referans noktası alanında bir değer girin veya bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="073cb-166">In the Reference point field, enter or select a value.</span></span>
25. <span data-ttu-id="073cb-167">Listede, tüm satırları işaretleyin veya tüm satırların işaretlerini kaldırın.</span><span class="sxs-lookup"><span data-stu-id="073cb-167">In the list, mark or unmark all rows.</span></span>
26. <span data-ttu-id="073cb-168">Kılavuza uygula'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="073cb-168">Click Apply to grid.</span></span>
27. <span data-ttu-id="073cb-169">Ayarlama tutarı alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="073cb-169">In the Adjustment amount field, enter a number.</span></span>
28. <span data-ttu-id="073cb-170">Referans noktası alanında bir değer girin veya bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="073cb-170">In the Reference point field, enter or select a value.</span></span>
29. <span data-ttu-id="073cb-171">Listede, tüm satırları işaretleyin veya tüm satırların işaretlerini kaldırın.</span><span class="sxs-lookup"><span data-stu-id="073cb-171">In the list, mark or unmark all rows.</span></span>
30. <span data-ttu-id="073cb-172">Kılavuza uygula'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="073cb-172">Click Apply to grid.</span></span>

