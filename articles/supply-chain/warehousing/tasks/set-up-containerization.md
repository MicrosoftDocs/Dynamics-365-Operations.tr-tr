--- 
title: "Konteyner kullanımını ayarlama"
description: "Bu yordam, Ambar yönetimindeki yüklerin konteyner kullanımının nasıl otomatikleştirileceğini açıklar."
author: YuyuScheller
manager: AnnBe
ms.date: 06/07/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mirzaab
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: aeb7d956560c513c08d5e20dcf20989b49137a52
ms.contentlocale: tr-tr
ms.lasthandoff: 09/29/2017

---
# <a name="set-up-containerization"></a><span data-ttu-id="49eaa-103">Konteyner kullanımını ayarlama</span><span class="sxs-lookup"><span data-stu-id="49eaa-103">Set up containerization</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="49eaa-104">Bu yordam, Ambar yönetimindeki yüklerin konteyner kullanımının nasıl otomatikleştirileceğini açıklar.</span><span class="sxs-lookup"><span data-stu-id="49eaa-104">This procedure describes how to automate the containerization of loads in Warehouse management.</span></span> <span data-ttu-id="49eaa-105">Otomatik konteyner kullanımı, bir dalga işlendiğinde sevkiyatlar için konteynerleri ve çekme işini oluşturur ve iş satırları, konteynerlere sığacak miktarlara bölünür.</span><span class="sxs-lookup"><span data-stu-id="49eaa-105">Automated containerization creates containers and the picking work for shipments when a wave is processed and work lines can be split into quantities that fit the containers.</span></span> <span data-ttu-id="49eaa-106">Bu, ambar çalışanlarına, maddeleri doğrudan seçilen konteynere çekmelerine yardımcı olur.</span><span class="sxs-lookup"><span data-stu-id="49eaa-106">This helps warehouse workers to pick the items directly into the chosen container.</span></span> <span data-ttu-id="49eaa-107">El ile yapılan paketleme işlemi ile karşılaştırıldığında, örneğin konteynerler oluşturma, maddeler atama ve konteyner kapanışı gibi işlemler, sistem tarafından otomatikleştirilir.</span><span class="sxs-lookup"><span data-stu-id="49eaa-107">Compared to the manual packing process, tasks such as creating containers, assigning items, and closing containers are automated by the system.</span></span> <span data-ttu-id="49eaa-108">Bu yordam, USMF demo şirketin kullanır ve Ambar Yöneticisi tarafından gerçekleştirilir.</span><span class="sxs-lookup"><span data-stu-id="49eaa-108">This procedure uses the USMF demo company and is performed by a Warehouse manager.</span></span>


## <a name="set-up-a-wave-template"></a><span data-ttu-id="49eaa-109">Dalga şablonu ayarlama</span><span class="sxs-lookup"><span data-stu-id="49eaa-109">Set up a wave template</span></span>
1. <span data-ttu-id="49eaa-110">Ambar yönetimi > Kurulum > Dalgalar > Dalga şablonları öğesine gidin.</span><span class="sxs-lookup"><span data-stu-id="49eaa-110">Go to Warehouse management > Setup > Waves > Wave templates.</span></span>
2. <span data-ttu-id="49eaa-111">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="49eaa-111">Click New.</span></span>
3. <span data-ttu-id="49eaa-112">Dalga şablonu adı alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="49eaa-112">In the Wave template name field, type a value.</span></span>
4. <span data-ttu-id="49eaa-113">Dalga şablonu açıklaması alanında bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="49eaa-113">In the Wave template description field, type a value.</span></span>
5. <span data-ttu-id="49eaa-114">Tesis alanına bir değer girin veya buradan bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="49eaa-114">In the Site field, enter or select a value.</span></span>
6. <span data-ttu-id="49eaa-115">Ambar alanında bir değer girin veya bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="49eaa-115">In the Warehouse field, enter or select a value.</span></span>
7. <span data-ttu-id="49eaa-116">Yöntemler bölümünü genişletin.</span><span class="sxs-lookup"><span data-stu-id="49eaa-116">Expand the Methods section.</span></span>
    * <span data-ttu-id="49eaa-117">Seçili yöntemler bölmesi, seçili dalga şablon türü için yöntemleri listeler.</span><span class="sxs-lookup"><span data-stu-id="49eaa-117">The Selected methods pane lists the methods for the selected wave template type.</span></span> <span data-ttu-id="49eaa-118">Dalga şablonu, konteynerli yöntemi içermelidir.</span><span class="sxs-lookup"><span data-stu-id="49eaa-118">The wave template must include the containerize method.</span></span>  
8. <span data-ttu-id="49eaa-119">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="49eaa-119">In the list, find and select the desired record.</span></span>
9. <span data-ttu-id="49eaa-120">Dalga adımı kodu alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="49eaa-120">In the Wave step code field, type a value.</span></span>
    * <span data-ttu-id="49eaa-121">Eklenen yöntem için herhangi bir kod olabilecek Dalga adım kodu girin.</span><span class="sxs-lookup"><span data-stu-id="49eaa-121">Enter a Wave step code for the added method, which can be any code.</span></span> <span data-ttu-id="49eaa-122">Yöntemi birden çok kez eklemek ve farklı dalga adım kodları atamak da mümkündür.</span><span class="sxs-lookup"><span data-stu-id="49eaa-122">It’s possible to add the method more than once and assign different wave step codes.</span></span> <span data-ttu-id="49eaa-123">Bunu yapmak için bu yöntemin dalga işlem yöntemleri sayfasında Tekrar edilebilir'i seçin.</span><span class="sxs-lookup"><span data-stu-id="49eaa-123">To do this, select Repeatable for this method in the Wave process methods page.</span></span>  
10. <span data-ttu-id="49eaa-124">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="49eaa-124">Click Save.</span></span>
11. <span data-ttu-id="49eaa-125">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="49eaa-125">Close the page.</span></span>

## <a name="set-up-a-container-type"></a><span data-ttu-id="49eaa-126">Konteyner türü ayarlama</span><span class="sxs-lookup"><span data-stu-id="49eaa-126">Set up a container type</span></span>
1. <span data-ttu-id="49eaa-127">Ambar yönetimi > Kurulum > Konteynerler > Konteyner türleri öğesine gidin.</span><span class="sxs-lookup"><span data-stu-id="49eaa-127">Go to Warehouse management > Setup > Containers > Container types.</span></span>
    * <span data-ttu-id="49eaa-128">Konteyner türleri sayfasında, konteynerlerinizi tanımlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="49eaa-128">You can define your containers in the Container types page.</span></span> <span data-ttu-id="49eaa-129">Konteynerlerin fiziksel boyutlarını, dara ağırlığı, maksimum ağırlık, maksimum hacim, uzunluk, genişlik ve yükseklik dahil olmak üzere yapılandırabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="49eaa-129">You can configure the physical dimensions of containers including tare weight, maximum weight, maximum volume, length, width, and height.</span></span> <span data-ttu-id="49eaa-130">Bu örnekte, üç farklı boyutta kutulara sahibiz.</span><span class="sxs-lookup"><span data-stu-id="49eaa-130">In this example, we have three different sizes of boxes.</span></span>  
2. <span data-ttu-id="49eaa-131">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="49eaa-131">Click New.</span></span>
3. <span data-ttu-id="49eaa-132">Konteyner türü alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="49eaa-132">In the Container type code field, type a value.</span></span>
4. <span data-ttu-id="49eaa-133">Dara alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="49eaa-133">In the Tare weight field, enter a number.</span></span>
5. <span data-ttu-id="49eaa-134">Maksimum ağırlık alanında bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="49eaa-134">In the Maximum weight field, enter a number.</span></span>
6. <span data-ttu-id="49eaa-135">Hacim alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="49eaa-135">In the Volume field, enter a number.</span></span>
7. <span data-ttu-id="49eaa-136">Uzunluk alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="49eaa-136">In the Length field, enter a number.</span></span>
8. <span data-ttu-id="49eaa-137">Genişlik alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="49eaa-137">In the Width field, enter a number.</span></span>
9. <span data-ttu-id="49eaa-138">Yükseklik alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="49eaa-138">In the Height field, enter a number.</span></span>
10. <span data-ttu-id="49eaa-139">Açıklama alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="49eaa-139">In the Description field, type a value.</span></span>
11. <span data-ttu-id="49eaa-140">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="49eaa-140">Click Save.</span></span>
12. <span data-ttu-id="49eaa-141">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="49eaa-141">Click New.</span></span>
13. <span data-ttu-id="49eaa-142">Konteyner türü alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="49eaa-142">In the Container type code field, type a value.</span></span>
14. <span data-ttu-id="49eaa-143">Açıklama alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="49eaa-143">In the Description field, type a value.</span></span>
15. <span data-ttu-id="49eaa-144">Dara alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="49eaa-144">In the Tare weight field, enter a number.</span></span>
16. <span data-ttu-id="49eaa-145">Maksimum ağırlık alanında bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="49eaa-145">In the Maximum weight field, enter a number.</span></span>
17. <span data-ttu-id="49eaa-146">Hacim alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="49eaa-146">In the Volume field, enter a number.</span></span>
18. <span data-ttu-id="49eaa-147">Uzunluk alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="49eaa-147">In the Length field, enter a number.</span></span>
19. <span data-ttu-id="49eaa-148">Genişlik alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="49eaa-148">In the Width field, enter a number.</span></span>
20. <span data-ttu-id="49eaa-149">Yükseklik alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="49eaa-149">In the Height field, enter a number.</span></span>
21. <span data-ttu-id="49eaa-150">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="49eaa-150">Click Save.</span></span>
22. <span data-ttu-id="49eaa-151">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="49eaa-151">Click New.</span></span>
23. <span data-ttu-id="49eaa-152">Konteyner türü alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="49eaa-152">In the Container type code field, type a value.</span></span>
24. <span data-ttu-id="49eaa-153">Açıklama alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="49eaa-153">In the Description field, type a value.</span></span>
25. <span data-ttu-id="49eaa-154">Dara alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="49eaa-154">In the Tare weight field, enter a number.</span></span>
26. <span data-ttu-id="49eaa-155">Maksimum ağırlık alanında bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="49eaa-155">In the Maximum weight field, enter a number.</span></span>
27. <span data-ttu-id="49eaa-156">Hacim alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="49eaa-156">In the Volume field, enter a number.</span></span>
28. <span data-ttu-id="49eaa-157">Uzunluk alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="49eaa-157">In the Length field, enter a number.</span></span>
29. <span data-ttu-id="49eaa-158">Genişlik alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="49eaa-158">In the Width field, enter a number.</span></span>
30. <span data-ttu-id="49eaa-159">Yükseklik alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="49eaa-159">In the Height field, enter a number.</span></span>
31. <span data-ttu-id="49eaa-160">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="49eaa-160">Click Save.</span></span>
32. <span data-ttu-id="49eaa-161">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="49eaa-161">Close the page.</span></span>

## <a name="set-up-a-container-group"></a><span data-ttu-id="49eaa-162">Bir konteyner grubu ayarla</span><span class="sxs-lookup"><span data-stu-id="49eaa-162">Set up a container group</span></span>
1. <span data-ttu-id="49eaa-163">Ambar yönetimi > Kurulum > Konteynerler > Konteyner grupları öğesine gidin.</span><span class="sxs-lookup"><span data-stu-id="49eaa-163">Go to Warehouse management > Setup > Containers > Container groups.</span></span>
2. <span data-ttu-id="49eaa-164">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="49eaa-164">Click New.</span></span>
    * <span data-ttu-id="49eaa-165">Konteyner türleri için mantıksal grupları ayarlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="49eaa-165">You can set up logical groups of container types.</span></span> <span data-ttu-id="49eaa-166">Her bir grup için, konteynerlerin paketleneceği sıralamayı ve konteynerlerin doldurulacağı yüzdeyi belirtebilirsiniz. Maddenin ebat boyutları, bir konteynere sığı sığmayacağını belirlemekte kullanılır.</span><span class="sxs-lookup"><span data-stu-id="49eaa-166">For each group, you can specify the sequence in which to pack the containers and the percentage of the containers to fill.The size dimensions of the item is used to determine whether it will fit in a container.</span></span> <span data-ttu-id="49eaa-167">Maddenin ebat boyutuna en yakın olan konteyner kullanılacaktır.</span><span class="sxs-lookup"><span data-stu-id="49eaa-167">The container that is closest to the size dimensions of the item is used.</span></span> <span data-ttu-id="49eaa-168">Bir grup içinde birden çok konteyner türü varsa, sırayı boyuta göre düzenlemenizi öneririz, böylelikle en büyük konteyner birinci, sıralama içerisinde birinci numarada olur ve en küçük konteyner en sona kalır.</span><span class="sxs-lookup"><span data-stu-id="49eaa-168">If you have multiple container types in a group, we recommend that you arrange the sequence by size, so that the largest container is first, number 1 in the sequence, and the smallest container is last.</span></span>    
3. <span data-ttu-id="49eaa-169">Konteyner grubu numarası alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="49eaa-169">In the Container group ID field, type a value.</span></span>
4. <span data-ttu-id="49eaa-170">Açıklama alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="49eaa-170">In the Description field, type a value.</span></span>
5. <span data-ttu-id="49eaa-171">Yeni'yi tıklatın.</span><span class="sxs-lookup"><span data-stu-id="49eaa-171">Click New.</span></span>
6. <span data-ttu-id="49eaa-172">Listede, seçili satırı işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="49eaa-172">In the list, mark the selected row.</span></span>
7. <span data-ttu-id="49eaa-173">Konteyner türü alanında bir değer girin veya seçin.</span><span class="sxs-lookup"><span data-stu-id="49eaa-173">In the Container type field, enter or select a value.</span></span>
8. <span data-ttu-id="49eaa-174">Yeni'yi tıklatın.</span><span class="sxs-lookup"><span data-stu-id="49eaa-174">Click New.</span></span>
9. <span data-ttu-id="49eaa-175">Listede, seçili satırı işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="49eaa-175">In the list, mark the selected row.</span></span>
10. <span data-ttu-id="49eaa-176">Konteyner türü alanında bir değer girin veya seçin.</span><span class="sxs-lookup"><span data-stu-id="49eaa-176">In the Container type field, enter or select a value.</span></span>
11. <span data-ttu-id="49eaa-177">Yeni'yi tıklatın.</span><span class="sxs-lookup"><span data-stu-id="49eaa-177">Click New.</span></span>
12. <span data-ttu-id="49eaa-178">Listede, seçili satırı işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="49eaa-178">In the list, mark the selected row.</span></span>
13. <span data-ttu-id="49eaa-179">Konteyner türü alanında bir değer girin veya seçin.</span><span class="sxs-lookup"><span data-stu-id="49eaa-179">In the Container type field, enter or select a value.</span></span>
14. <span data-ttu-id="49eaa-180">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="49eaa-180">Click Save.</span></span>
15. <span data-ttu-id="49eaa-181">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="49eaa-181">Close the page.</span></span>

## <a name="set-up-a-container-build-template"></a><span data-ttu-id="49eaa-182">Bir konteyner yapılandırma şablonu</span><span class="sxs-lookup"><span data-stu-id="49eaa-182">Set up a container build template</span></span>
1. <span data-ttu-id="49eaa-183">Ambar yönetimi > Kurulum > Konteynerler > Konteyner yapı şablonu öğesine gidin.</span><span class="sxs-lookup"><span data-stu-id="49eaa-183">Go to Warehouse management > Setup > Containers > Container build templates.</span></span>
2. <span data-ttu-id="49eaa-184">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="49eaa-184">Click New.</span></span>
    * <span data-ttu-id="49eaa-185">Konteyner yapılandırma şablonu, hangi konteyner kullanım işleminin gerçekleştirildiğine dayalıdır.</span><span class="sxs-lookup"><span data-stu-id="49eaa-185">The container build template is based on which of the containerization processes are performed.</span></span> <span data-ttu-id="49eaa-186">Her bir konteyner yapılandırma şablonu, bir dalga şablonu tarafından kullanılacak bir konteyner kullanım işlemini tanımlar.</span><span class="sxs-lookup"><span data-stu-id="49eaa-186">Each container build template defines one containerization process that will be used by a wave template.</span></span> <span data-ttu-id="49eaa-187">Sorguyu düzenle seçeneği, seçili şablonun işleneceği koşulları tanımlamanızı sağlar.</span><span class="sxs-lookup"><span data-stu-id="49eaa-187">The Edit query option allows you to define the conditions on which the selected template will be processed.</span></span> <span data-ttu-id="49eaa-188">Örneğin, yalnızca belirli müşteriler, ürünler veya ambarlar için konteyner kullanmayı çalıştırmak isteyebilirsiniz veya karşılık gelen sorgu aralıklarını şablona ekleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="49eaa-188">For example, you may want to only run containerization for specific customers, products, or warehouses or you can add the corresponding query ranges to the template.</span></span> <span data-ttu-id="49eaa-189">Dalga adım kodu alanı, konteyner yapılandırma şablonunun dalga şablonundaki adımlara nasıl bağlandığını gösteren alandır.</span><span class="sxs-lookup"><span data-stu-id="49eaa-189">The Wave step code field is how a container build template is linked to steps in a wave template.</span></span> <span data-ttu-id="49eaa-190">Bir dalga yürütüldüğünde hangi kapsayıcı yapı şablonunun konteyner kullanımını başlatmak için kullanılacağını belirler.</span><span class="sxs-lookup"><span data-stu-id="49eaa-190">When a wave is executed, it determines which container build template(s) are used to initiate containerization.</span></span> <span data-ttu-id="49eaa-191">Taban sorgu türü alanı, neyin paketleneceğini ve filtre sorgusunun neye dayandırılacağını belirler.</span><span class="sxs-lookup"><span data-stu-id="49eaa-191">The Base query type field determines what to pack and what to base the filter query on.</span></span>  
3. <span data-ttu-id="49eaa-192">Listede, seçili satırı işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="49eaa-192">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="49eaa-193">Konteyner şablonu kimliği alanında bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="49eaa-193">In the Container template ID field, type a value.</span></span>
5. <span data-ttu-id="49eaa-194">Konteyner grup kimliği alanında bir değer girin veya bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="49eaa-194">In the Container group ID field, enter or select a value.</span></span>
6. <span data-ttu-id="49eaa-195">Dalga adımı kodu alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="49eaa-195">In the Wave step code field, type a value.</span></span>
7. <span data-ttu-id="49eaa-196">Bölünmüş çekmelere izin ver onay kutusunu işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="49eaa-196">Select the Allow split picks check box.</span></span>
8. <span data-ttu-id="49eaa-197">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="49eaa-197">Click Save.</span></span>
9. <span data-ttu-id="49eaa-198">Konteyner karıştırma sınırlamalarına tıklayın.</span><span class="sxs-lookup"><span data-stu-id="49eaa-198">Click Containier mixing constraints.</span></span>
    * <span data-ttu-id="49eaa-199">Mantık bölümlerini karıştırmak, konteynerler içindeki paketleme tahsisat satırları için kurallar eklemenize olanak sağlar.</span><span class="sxs-lookup"><span data-stu-id="49eaa-199">Mixing logic breaks allows you to set up rules for packing allocation lines in containers.</span></span> <span data-ttu-id="49eaa-200">Örneğin, maddeler konteynerlere atandığında Madde numarası alanını eklerseniz, yeni bir madde numarası olduğunda, yeni bir konteyner oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="49eaa-200">For example, if you add the Item number field, when items are assigned to containers, a new container will be created when there is a new item number.</span></span> <span data-ttu-id="49eaa-201">Bu, çalışanların aynı konteyner içerisindeki iki farklı müşteri için tahsisat satırlarını paketlemelerinin önüne geçer.</span><span class="sxs-lookup"><span data-stu-id="49eaa-201">This is will prevent workers from packing allocations lines for two different customers in the same container.</span></span>  
10. <span data-ttu-id="49eaa-202">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="49eaa-202">Click New.</span></span>
11. <span data-ttu-id="49eaa-203">Tablo alanında, bir seçenek seçin.</span><span class="sxs-lookup"><span data-stu-id="49eaa-203">In the Table field, select an option.</span></span>
12. <span data-ttu-id="49eaa-204">Alan Seç alanına bir değer girin veya buradan bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="49eaa-204">In the Field Select field, enter or select a value.</span></span>
13. <span data-ttu-id="49eaa-205">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="49eaa-205">Click OK.</span></span>


