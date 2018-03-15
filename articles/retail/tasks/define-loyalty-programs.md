--- 
title: " Bağlılık programları tanımlama"
description: "Bu yordam, iki bağlılık katmanıyla bir bağlılık programı ayarlamayla ilgili açıklamalar içerir."
author: jashanno
manager: AnnBe
ms.date: 11/14/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations, Retail
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: ea07d8e91c94d9fdad4c2d05533981e254420188
ms.openlocfilehash: a27a2367ac41e86a3038594261c080ad2515eb94
ms.contentlocale: tr-tr
ms.lasthandoff: 02/07/2018

---
# <a name="define-loyalty-programs"></a><span data-ttu-id="a876b-103"> Bağlılık programları tanımlama</span><span class="sxs-lookup"><span data-stu-id="a876b-103">Define loyalty programs</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="a876b-104">Bu yordam, iki bağlılık katmanıyla bir bağlılık programı ayarlamayla ilgili açıklamalar içerir.</span><span class="sxs-lookup"><span data-stu-id="a876b-104">This procedure shows how to set up a loyalty program with two loyalty tiers.</span></span> <span data-ttu-id="a876b-105">Bu yordam, USRT demo veri şirketini kullanır.</span><span class="sxs-lookup"><span data-stu-id="a876b-105">This procedure uses the USRT demo data company.</span></span>

1. <span data-ttu-id="a876b-106">Perakende ve ticaret > ..</span><span class="sxs-lookup"><span data-stu-id="a876b-106">Go to Retail and commerce > ..</span></span> <span data-ttu-id="a876b-107">> Bağlılık programları.</span><span class="sxs-lookup"><span data-stu-id="a876b-107">> Loyalty programs.</span></span>
2. <span data-ttu-id="a876b-108">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="a876b-108">Click New.</span></span>
3. <span data-ttu-id="a876b-109">İsim alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="a876b-109">In the Name field, type a value.</span></span>
4. <span data-ttu-id="a876b-110">Açıklama alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="a876b-110">In the Description field, type a value.</span></span>
5. <span data-ttu-id="a876b-111">Satır ekle'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="a876b-111">Click Add line.</span></span>
6. <span data-ttu-id="a876b-112">Düzey alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="a876b-112">In the Level field, enter a number.</span></span>
7. <span data-ttu-id="a876b-113">Katman alanına bağlılık katmanı için bir ad girin.</span><span class="sxs-lookup"><span data-stu-id="a876b-113">In the Tier field, enter a name for the loyalty tier.</span></span>
8. <span data-ttu-id="a876b-114">Tanım alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="a876b-114">In the Description field, type a value.</span></span>
9. <span data-ttu-id="a876b-115">Tarih aralığı alanında, aramayı açmak için açılır menü düğmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="a876b-115">In the Date interval field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="a876b-116">Bu tarih aralığı geleceğe dönük olarak genişletilmelidir.</span><span class="sxs-lookup"><span data-stu-id="a876b-116">This date interval should extend into the future.</span></span> <span data-ttu-id="a876b-117">Örneğin, gold katmanı için seçili tarih aralığı bir yıl olduğunda, gold katmanına uygun olan tüm müşteriler gold katmanına bir yıl için atanan ödülleri alma hakkına sahip olur.</span><span class="sxs-lookup"><span data-stu-id="a876b-117">For example, if the date interval that is selected for gold tier is a one-year period, any customer who qualifies for the gold tier can receive the rewards that are assigned to the gold tier for one year.</span></span> <span data-ttu-id="a876b-118">Müşteri gold katmandayken yeniden gold katmana hak kazanırsa, katmanın sona erme tarihi yeniden hak kazanılan tarihten itibaren bir yıl daha uzatılır.</span><span class="sxs-lookup"><span data-stu-id="a876b-118">If the customer re-qualifies for the gold tier while they are in the tier, the date that the tier expires is extended by another year from the date when they re-qualify.</span></span>  
10. <span data-ttu-id="a876b-119">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="a876b-119">In the list, click the link in the selected row.</span></span>
11. <span data-ttu-id="a876b-120">Satır ekle'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="a876b-120">Click Add line.</span></span>
12. <span data-ttu-id="a876b-121">Düzey alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="a876b-121">In the Level field, enter a number.</span></span>
13. <span data-ttu-id="a876b-122">Katman alanına bağlılık katmanı için bir ad girin.</span><span class="sxs-lookup"><span data-stu-id="a876b-122">In the Tier field, enter a name for the loyalty tier.</span></span>
14. <span data-ttu-id="a876b-123">Tanım alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="a876b-123">In the Description field, type a value.</span></span>
15. <span data-ttu-id="a876b-124">Tarih aralığı alanında, aramayı açmak için açılır menü düğmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="a876b-124">In the Date interval field, click the drop-down button to open the lookup.</span></span>
16. <span data-ttu-id="a876b-125">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="a876b-125">In the list, click the link in the selected row.</span></span>
17. <span data-ttu-id="a876b-126">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="a876b-126">Click Save.</span></span>
18. <span data-ttu-id="a876b-127">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="a876b-127">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="a876b-128">Katman kuralları, katmana girmeye hak kazanmak için belirli bir süre boyunca kazanılması gereken minimum ödül puanı sayısını belirler.</span><span class="sxs-lookup"><span data-stu-id="a876b-128">Tier rules define the minimum number of a reward point needed to be earned during a time period to qualify for the tier.</span></span>  
19. <span data-ttu-id="a876b-129">Katman kuralları bölümünün genişletilmiş görünümüne geçin.</span><span class="sxs-lookup"><span data-stu-id="a876b-129">Toggle the expansion of the Tier rules section.</span></span>
20. <span data-ttu-id="a876b-130">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="a876b-130">Click New.</span></span>
    * <span data-ttu-id="a876b-131">Katman başına birden fazla katman kuralınız olabilir.</span><span class="sxs-lookup"><span data-stu-id="a876b-131">You can have more than one tier rule per tier.</span></span> <span data-ttu-id="a876b-132">Örneğin, bir katmanı kazanmak için üç farklı ölçüt belirleyebilirsiniz; bir ay içinde 500 $ harcama, bir yıl süresince 1000 $ harcama ve bir yılda 20 hareket gerçekleştirme.</span><span class="sxs-lookup"><span data-stu-id="a876b-132">For example, you could have three different criteria to earn a tier; by spending $500 in one month, by spending $1000 over one year, and by having 20 transactions in one year.</span></span> <span data-ttu-id="a876b-133">Bunu yapmak için üç katman kuralı oluşturmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="a876b-133">To do this, you would need to create three tier rules.</span></span>  
21. <span data-ttu-id="a876b-134">Ödül puanı alanında, aramayı açmak için açılır menü düğmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="a876b-134">In the Reward point field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="a876b-135">Bunun kullanılamayan bir bağlılık ödül puanı olması gerekir.</span><span class="sxs-lookup"><span data-stu-id="a876b-135">This should be a non-redeemable loyalty reward point.</span></span>  
22. <span data-ttu-id="a876b-136">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="a876b-136">In the list, click the link in the selected row.</span></span>
23. <span data-ttu-id="a876b-137">Minimum verilen puan alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="a876b-137">In the Minimum issued points field, enter a number.</span></span>
    * <span data-ttu-id="a876b-138">En düşük katman seviyesinde, tüm müşteriler programa katılarak katmana hak kazanacaksa '0' değerini girin.</span><span class="sxs-lookup"><span data-stu-id="a876b-138">For the lowest level tier, if all customers qualify simply by participating in the program, enter '0'.</span></span>  
24. <span data-ttu-id="a876b-139">Değerlendirme tarih aralığı alanında, aramayı açmak için açılır menü düğmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="a876b-139">In the Evaluation date interval field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="a876b-140">Bu tarih aralığını geçmişe dönük olarak genişletilmelidir.</span><span class="sxs-lookup"><span data-stu-id="a876b-140">This date interval should extend into the past.</span></span> <span data-ttu-id="a876b-141">Yalnızca bu tarih aralığında kazanılan puanlar verilen minimum puan değerine ulaşmak için geçerli sayılır.</span><span class="sxs-lookup"><span data-stu-id="a876b-141">Only points earned during this date interval will be counted towards reaching the minimum issued points value.</span></span>  
25. <span data-ttu-id="a876b-142">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="a876b-142">In the list, click the link in the selected row.</span></span>
26. <span data-ttu-id="a876b-143">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="a876b-143">Click Save.</span></span>
27. <span data-ttu-id="a876b-144">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="a876b-144">In the list, find and select the desired record.</span></span>
28. <span data-ttu-id="a876b-145">Yeni'yi tıklatın.</span><span class="sxs-lookup"><span data-stu-id="a876b-145">Click New.</span></span>
29. <span data-ttu-id="a876b-146">Ödül puanı alanında, aramayı açmak için açılır menü düğmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="a876b-146">In the Reward point field, click the drop-down button to open the lookup.</span></span>
30. <span data-ttu-id="a876b-147">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="a876b-147">In the list, click the link in the selected row.</span></span>
31. <span data-ttu-id="a876b-148">Minimum verilen puan alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="a876b-148">In the Minimum issued points field, enter a number.</span></span>
32. <span data-ttu-id="a876b-149">Değerlendirme tarih aralığı alanında, aramayı açmak için açılır menü düğmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="a876b-149">In the Evaluation date interval field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="a876b-150">Bu tarih aralığını geçmişe dönük olarak genişletilmelidir.</span><span class="sxs-lookup"><span data-stu-id="a876b-150">This date interval should extend into the past.</span></span>  
33. <span data-ttu-id="a876b-151">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="a876b-151">In the list, click the link in the selected row.</span></span>
34. <span data-ttu-id="a876b-152">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="a876b-152">Click Save.</span></span>
35. <span data-ttu-id="a876b-153">Fiyat grupları'na tıklayın.</span><span class="sxs-lookup"><span data-stu-id="a876b-153">Click Price groups.</span></span>
    * <span data-ttu-id="a876b-154">Bağlı müşterilere indirimler vermek istiyorsanız.</span><span class="sxs-lookup"><span data-stu-id="a876b-154">If you want to give loyalty customers discounts.</span></span> <span data-ttu-id="a876b-155">bir veya birden fazla fiyat grubun bağlılık programına atamalı ve fiyat gruplarını indirimlere atamalısınız.</span><span class="sxs-lookup"><span data-stu-id="a876b-155">you'll need to assign one or more price groups to the loyalty program and assign the price groups to discounts.</span></span> <span data-ttu-id="a876b-156">En iyi uygulama, farklı türdeki iskonto varlıkları üzerinde fiyat gruplarını karıştırmamaktır.</span><span class="sxs-lookup"><span data-stu-id="a876b-156">It is a best practice to not mix price groups across different types of discounting entities.</span></span>  <span data-ttu-id="a876b-157">Örneğin, aynı fiyat grubunu bir bağlılık iskontosu ve kanal iskontosu için kullanmayın.</span><span class="sxs-lookup"><span data-stu-id="a876b-157">For example, don't use the same price group for a loyalty discount and a channel discount.</span></span>  
36. <span data-ttu-id="a876b-158">Fiyat grubu alanında, aramayı açmak için açılır menü düğmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="a876b-158">In the Price group field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="a876b-159">Sayfanın üst kısmındaki fiyat grupları bağlantısı bağlılık programı içindir.</span><span class="sxs-lookup"><span data-stu-id="a876b-159">The Price groups link at the top of the page is for the loyalty program.</span></span> <span data-ttu-id="a876b-160">Program katmanları hızlı sekmesindeki Fiyat grupları bağlantısı yalnızca belirli bir bağlılık katmanı için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="a876b-160">The Price groups link in the Program tiers fasttab is for a specific loyalty tier only.</span></span>  
37. <span data-ttu-id="a876b-161">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="a876b-161">In the list, click the link in the selected row.</span></span>
38. <span data-ttu-id="a876b-162">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="a876b-162">Click Save.</span></span>
39. <span data-ttu-id="a876b-163">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="a876b-163">Close the page.</span></span>
40. <span data-ttu-id="a876b-164">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="a876b-164">Click Save.</span></span>


