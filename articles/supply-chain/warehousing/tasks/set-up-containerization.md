--- 
title: "Konteyner kullanımını ayarlama"
description: "Bu yordam, Ambar yönetimindeki yüklerin konteyner kullanımının nasıl otomatikleştirileceğini açıklar."
author: YuyuScheller
manager: AnnBe
ms.date: 11/02/2017
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
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 4e7a2fde65c8dba8b16c5a87eae0ec2bbebc3388
ms.contentlocale: tr-tr
ms.lasthandoff: 05/08/2018

---
# <a name="set-up-containerization"></a><span data-ttu-id="6b753-103">Konteyner kullanımını ayarlama</span><span class="sxs-lookup"><span data-stu-id="6b753-103">Set up containerization</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="6b753-104">Bu yordam, Ambar yönetimindeki yüklerin konteyner kullanımının nasıl otomatikleştirileceğini açıklar.</span><span class="sxs-lookup"><span data-stu-id="6b753-104">This procedure describes how to automate the containerization of loads in Warehouse management.</span></span> <span data-ttu-id="6b753-105">Otomatik konteyner kullanımı, bir dalga işlendiğinde sevkiyatlar için konteynerleri ve çekme işini oluşturur ve iş satırları, konteynerlere sığacak miktarlara bölünür.</span><span class="sxs-lookup"><span data-stu-id="6b753-105">Automated containerization creates containers and the picking work for shipments when a wave is processed and work lines can be split into quantities that fit the containers.</span></span> <span data-ttu-id="6b753-106">Bu, ambar çalışanlarına, maddeleri doğrudan seçilen konteynere çekmelerine yardımcı olur.</span><span class="sxs-lookup"><span data-stu-id="6b753-106">This helps warehouse workers to pick the items directly into the chosen container.</span></span> <span data-ttu-id="6b753-107">El ile yapılan paketleme işlemi ile karşılaştırıldığında, örneğin konteynerler oluşturma, maddeler atama ve konteyner kapanışı gibi işlemler, sistem tarafından otomatikleştirilir.</span><span class="sxs-lookup"><span data-stu-id="6b753-107">Compared to the manual packing process, tasks such as creating containers, assigning items, and closing containers are automated by the system.</span></span> <span data-ttu-id="6b753-108">Bu yordam, USMF demo şirketin kullanır ve Ambar Yöneticisi tarafından gerçekleştirilir.</span><span class="sxs-lookup"><span data-stu-id="6b753-108">This procedure uses the USMF demo company and is performed by a Warehouse manager.</span></span>


## <a name="set-up-a-wave-template"></a><span data-ttu-id="6b753-109">Dalga şablonu ayarlama</span><span class="sxs-lookup"><span data-stu-id="6b753-109">Set up a wave template</span></span>
1. <span data-ttu-id="6b753-110">Ambar yönetimi > Kurulum > Dalgalar > Dalga şablonları öğesine gidin.</span><span class="sxs-lookup"><span data-stu-id="6b753-110">Go to Warehouse management > Setup > Waves > Wave templates.</span></span>
2. <span data-ttu-id="6b753-111">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="6b753-111">Click New.</span></span>
3. <span data-ttu-id="6b753-112">Dalga şablonu adı alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="6b753-112">In the Wave template name field, type a value.</span></span>
4. <span data-ttu-id="6b753-113">Dalga şablonu açıklaması alanında bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="6b753-113">In the Wave template description field, type a value.</span></span>
5. <span data-ttu-id="6b753-114">Tesis alanına bir değer girin veya buradan bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="6b753-114">In the Site field, enter or select a value.</span></span>
6. <span data-ttu-id="6b753-115">Ambar alanında bir değer girin veya bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="6b753-115">In the Warehouse field, enter or select a value.</span></span>
7. <span data-ttu-id="6b753-116">Yöntemler bölümünü genişletin.</span><span class="sxs-lookup"><span data-stu-id="6b753-116">Expand the Methods section.</span></span>
    * <span data-ttu-id="6b753-117">Seçili yöntemler bölmesi, seçili dalga şablon türü için yöntemleri listeler.</span><span class="sxs-lookup"><span data-stu-id="6b753-117">The Selected methods pane lists the methods for the selected wave template type.</span></span> <span data-ttu-id="6b753-118">Dalga şablonu, konteynerli yöntemi içermelidir.</span><span class="sxs-lookup"><span data-stu-id="6b753-118">The wave template must include the containerize method.</span></span>  
8. <span data-ttu-id="6b753-119">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="6b753-119">In the list, find and select the desired record.</span></span>
9. <span data-ttu-id="6b753-120">Dalga adımı kodu alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="6b753-120">In the Wave step code field, type a value.</span></span>
    * <span data-ttu-id="6b753-121">Eklenen yöntem için herhangi bir kod olabilecek Dalga adım kodu girin.</span><span class="sxs-lookup"><span data-stu-id="6b753-121">Enter a Wave step code for the added method, which can be any code.</span></span> <span data-ttu-id="6b753-122">Yöntemi birden çok kez eklemek ve farklı dalga adım kodları atamak da mümkündür.</span><span class="sxs-lookup"><span data-stu-id="6b753-122">It’s possible to add the method more than once and assign different wave step codes.</span></span> <span data-ttu-id="6b753-123">Bunu yapmak için bu yöntemin dalga işlem yöntemleri sayfasında Tekrar edilebilir'i seçin.</span><span class="sxs-lookup"><span data-stu-id="6b753-123">To do this, select Repeatable for this method in the Wave process methods page.</span></span>  
10. <span data-ttu-id="6b753-124">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="6b753-124">Click Save.</span></span>
11. <span data-ttu-id="6b753-125">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="6b753-125">Close the page.</span></span>

## <a name="set-up-a-container-type"></a><span data-ttu-id="6b753-126">Konteyner türü ayarlama</span><span class="sxs-lookup"><span data-stu-id="6b753-126">Set up a container type</span></span>
1. <span data-ttu-id="6b753-127">Ambar yönetimi > Kurulum > Konteynerler > Konteyner türleri öğesine gidin.</span><span class="sxs-lookup"><span data-stu-id="6b753-127">Go to Warehouse management > Setup > Containers > Container types.</span></span>
    * <span data-ttu-id="6b753-128">Konteyner türleri sayfasında, konteynerlerinizi tanımlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="6b753-128">You can define your containers in the Container types page.</span></span> <span data-ttu-id="6b753-129">Konteynerlerin fiziksel boyutlarını, dara ağırlığı, maksimum ağırlık, maksimum hacim, uzunluk, genişlik ve yükseklik dahil olmak üzere yapılandırabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="6b753-129">You can configure the physical dimensions of containers including tare weight, maximum weight, maximum volume, length, width, and height.</span></span> <span data-ttu-id="6b753-130">Bu örnekte, üç farklı boyutta kutulara sahibiz.</span><span class="sxs-lookup"><span data-stu-id="6b753-130">In this example, we have three different sizes of boxes.</span></span>  
2. <span data-ttu-id="6b753-131">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="6b753-131">Click New.</span></span>
3. <span data-ttu-id="6b753-132">Konteyner türü alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="6b753-132">In the Container type code field, type a value.</span></span>
4. <span data-ttu-id="6b753-133">Dara alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="6b753-133">In the Tare weight field, enter a number.</span></span>
5. <span data-ttu-id="6b753-134">Maksimum ağırlık alanında bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="6b753-134">In the Maximum weight field, enter a number.</span></span>
6. <span data-ttu-id="6b753-135">Hacim alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="6b753-135">In the Volume field, enter a number.</span></span>
7. <span data-ttu-id="6b753-136">Uzunluk alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="6b753-136">In the Length field, enter a number.</span></span>
8. <span data-ttu-id="6b753-137">Genişlik alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="6b753-137">In the Width field, enter a number.</span></span>
9. <span data-ttu-id="6b753-138">Yükseklik alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="6b753-138">In the Height field, enter a number.</span></span>
10. <span data-ttu-id="6b753-139">Açıklama alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="6b753-139">In the Description field, type a value.</span></span>
11. <span data-ttu-id="6b753-140">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="6b753-140">Click Save.</span></span>
12. <span data-ttu-id="6b753-141">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="6b753-141">Click New.</span></span>
13. <span data-ttu-id="6b753-142">Konteyner türü alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="6b753-142">In the Container type code field, type a value.</span></span>
14. <span data-ttu-id="6b753-143">Açıklama alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="6b753-143">In the Description field, type a value.</span></span>
15. <span data-ttu-id="6b753-144">Dara alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="6b753-144">In the Tare weight field, enter a number.</span></span>
16. <span data-ttu-id="6b753-145">Maksimum ağırlık alanında bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="6b753-145">In the Maximum weight field, enter a number.</span></span>
17. <span data-ttu-id="6b753-146">Hacim alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="6b753-146">In the Volume field, enter a number.</span></span>
18. <span data-ttu-id="6b753-147">Uzunluk alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="6b753-147">In the Length field, enter a number.</span></span>
19. <span data-ttu-id="6b753-148">Genişlik alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="6b753-148">In the Width field, enter a number.</span></span>
20. <span data-ttu-id="6b753-149">Yükseklik alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="6b753-149">In the Height field, enter a number.</span></span>
21. <span data-ttu-id="6b753-150">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="6b753-150">Click Save.</span></span>
22. <span data-ttu-id="6b753-151">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="6b753-151">Click New.</span></span>
23. <span data-ttu-id="6b753-152">Konteyner türü alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="6b753-152">In the Container type code field, type a value.</span></span>
24. <span data-ttu-id="6b753-153">Açıklama alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="6b753-153">In the Description field, type a value.</span></span>
25. <span data-ttu-id="6b753-154">Dara alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="6b753-154">In the Tare weight field, enter a number.</span></span>
26. <span data-ttu-id="6b753-155">Maksimum ağırlık alanında bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="6b753-155">In the Maximum weight field, enter a number.</span></span>
27. <span data-ttu-id="6b753-156">Hacim alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="6b753-156">In the Volume field, enter a number.</span></span>
28. <span data-ttu-id="6b753-157">Uzunluk alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="6b753-157">In the Length field, enter a number.</span></span>
29. <span data-ttu-id="6b753-158">Genişlik alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="6b753-158">In the Width field, enter a number.</span></span>
30. <span data-ttu-id="6b753-159">Yükseklik alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="6b753-159">In the Height field, enter a number.</span></span>
31. <span data-ttu-id="6b753-160">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="6b753-160">Click Save.</span></span>
32. <span data-ttu-id="6b753-161">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="6b753-161">Close the page.</span></span>

## <a name="set-up-a-container-group"></a><span data-ttu-id="6b753-162">Bir konteyner grubu ayarla</span><span class="sxs-lookup"><span data-stu-id="6b753-162">Set up a container group</span></span>
1. <span data-ttu-id="6b753-163">Ambar yönetimi > Kurulum > Konteynerler > Konteyner grupları öğesine gidin.</span><span class="sxs-lookup"><span data-stu-id="6b753-163">Go to Warehouse management > Setup > Containers > Container groups.</span></span>
2. <span data-ttu-id="6b753-164">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="6b753-164">Click New.</span></span>
    * <span data-ttu-id="6b753-165">Konteyner türleri için mantıksal grupları ayarlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="6b753-165">You can set up logical groups of container types.</span></span> <span data-ttu-id="6b753-166">Her bir grup için, konteynerleri paketleyecek sıralamayı ve konteynerlerin doldurulması istediğiniz yüzdesi belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="6b753-166">For each group, you can specify the sequence in which to pack the containers and the percentage of the containers to fill.</span></span> <span data-ttu-id="6b753-167">Maddenin boyut özellikleri konteynerin içinde sığacak olup olmadığını belirlemek için kullanır.</span><span class="sxs-lookup"><span data-stu-id="6b753-167">The size dimensions of the item is used to determine whether it will fit in a container.</span></span> <span data-ttu-id="6b753-168">Maddenin ebat boyutuna en yakın olan konteyner kullanılacaktır.</span><span class="sxs-lookup"><span data-stu-id="6b753-168">The container that is closest to the size dimensions of the item is used.</span></span> <span data-ttu-id="6b753-169">Bir grup içinde birden çok konteyner türü varsa, sırayı boyuta göre düzenlemenizi öneririz, böylelikle en büyük konteyner birinci, sıralama içerisinde birinci numarada olur ve en küçük konteyner en sona kalır.</span><span class="sxs-lookup"><span data-stu-id="6b753-169">If you have multiple container types in a group, we recommend that you arrange the sequence by size, so that the largest container is first, number 1 in the sequence, and the smallest container is last.</span></span>    
3. <span data-ttu-id="6b753-170">Konteyner grubu numarası alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="6b753-170">In the Container group ID field, type a value.</span></span>
4. <span data-ttu-id="6b753-171">Açıklama alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="6b753-171">In the Description field, type a value.</span></span>
5. <span data-ttu-id="6b753-172">Yeni'yi tıklatın.</span><span class="sxs-lookup"><span data-stu-id="6b753-172">Click New.</span></span>
6. <span data-ttu-id="6b753-173">Listede, seçili satırı işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="6b753-173">In the list, mark the selected row.</span></span>
7. <span data-ttu-id="6b753-174">Konteyner türü alanında bir değer girin veya seçin.</span><span class="sxs-lookup"><span data-stu-id="6b753-174">In the Container type field, enter or select a value.</span></span>
8. <span data-ttu-id="6b753-175">Yeni'yi tıklatın.</span><span class="sxs-lookup"><span data-stu-id="6b753-175">Click New.</span></span>
9. <span data-ttu-id="6b753-176">Listede, seçili satırı işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="6b753-176">In the list, mark the selected row.</span></span>
10. <span data-ttu-id="6b753-177">Konteyner türü alanında bir değer girin veya seçin.</span><span class="sxs-lookup"><span data-stu-id="6b753-177">In the Container type field, enter or select a value.</span></span>
11. <span data-ttu-id="6b753-178">Yeni'yi tıklatın.</span><span class="sxs-lookup"><span data-stu-id="6b753-178">Click New.</span></span>
12. <span data-ttu-id="6b753-179">Listede, seçili satırı işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="6b753-179">In the list, mark the selected row.</span></span>
13. <span data-ttu-id="6b753-180">Konteyner türü alanında bir değer girin veya seçin.</span><span class="sxs-lookup"><span data-stu-id="6b753-180">In the Container type field, enter or select a value.</span></span>
14. <span data-ttu-id="6b753-181">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="6b753-181">Click Save.</span></span>
15. <span data-ttu-id="6b753-182">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="6b753-182">Close the page.</span></span>

## <a name="set-up-a-container-build-template"></a><span data-ttu-id="6b753-183">Bir konteyner yapılandırma şablonu</span><span class="sxs-lookup"><span data-stu-id="6b753-183">Set up a container build template</span></span>
1. <span data-ttu-id="6b753-184">Ambar yönetimi > Kurulum > Konteynerler > Konteyner yapı şablonu öğesine gidin.</span><span class="sxs-lookup"><span data-stu-id="6b753-184">Go to Warehouse management > Setup > Containers > Container build templates.</span></span>
2. <span data-ttu-id="6b753-185">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="6b753-185">Click New.</span></span>
    * <span data-ttu-id="6b753-186">Konteyner yapılandırma şablonu, hangi konteyner kullanım işleminin gerçekleştirildiğine dayalıdır.</span><span class="sxs-lookup"><span data-stu-id="6b753-186">The container build template is based on which of the containerization processes are performed.</span></span> <span data-ttu-id="6b753-187">Her bir konteyner yapılandırma şablonu, bir dalga şablonu tarafından kullanılacak bir konteyner kullanım işlemini tanımlar.</span><span class="sxs-lookup"><span data-stu-id="6b753-187">Each container build template defines one containerization process that will be used by a wave template.</span></span> <span data-ttu-id="6b753-188">Sorguyu düzenle seçeneği, seçili şablonun işleneceği koşulları tanımlamanızı sağlar.</span><span class="sxs-lookup"><span data-stu-id="6b753-188">The Edit query option allows you to define the conditions on which the selected template will be processed.</span></span> <span data-ttu-id="6b753-189">Örneğin, yalnızca belirli müşteriler, ürünler veya ambarlar için konteyner kullanmayı çalıştırmak isteyebilirsiniz veya karşılık gelen sorgu aralıklarını şablona ekleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="6b753-189">For example, you may want to only run containerization for specific customers, products, or warehouses or you can add the corresponding query ranges to the template.</span></span> <span data-ttu-id="6b753-190">Dalga adım kodu alanı, konteyner yapılandırma şablonunun dalga şablonundaki adımlara nasıl bağlandığını gösteren alandır.</span><span class="sxs-lookup"><span data-stu-id="6b753-190">The Wave step code field is how a container build template is linked to steps in a wave template.</span></span> <span data-ttu-id="6b753-191">Bir dalga yürütüldüğünde hangi kapsayıcı yapı şablonunun konteyner kullanımını başlatmak için kullanılacağını belirler.</span><span class="sxs-lookup"><span data-stu-id="6b753-191">When a wave is executed, it determines which container build template(s) are used to initiate containerization.</span></span> <span data-ttu-id="6b753-192">Taban sorgu türü alanı, neyin paketleneceğini ve filtre sorgusunun neye dayandırılacağını belirler.</span><span class="sxs-lookup"><span data-stu-id="6b753-192">The Base query type field determines what to pack and what to base the filter query on.</span></span>  
3. <span data-ttu-id="6b753-193">Listede, seçili satırı işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="6b753-193">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="6b753-194">Konteyner şablonu kimliği alanında bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="6b753-194">In the Container template ID field, type a value.</span></span>
5. <span data-ttu-id="6b753-195">Konteyner grup kimliği alanında bir değer girin veya bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="6b753-195">In the Container group ID field, enter or select a value.</span></span>
6. <span data-ttu-id="6b753-196">Dalga adımı kodu alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="6b753-196">In the Wave step code field, type a value.</span></span>
7. <span data-ttu-id="6b753-197">Bölünmüş çekmelere izin ver onay kutusunu işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="6b753-197">Select the Allow split picks check box.</span></span>
8. <span data-ttu-id="6b753-198">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="6b753-198">Click Save.</span></span>
9. <span data-ttu-id="6b753-199">Konteyner karıştırma sınırlamalarına tıklayın.</span><span class="sxs-lookup"><span data-stu-id="6b753-199">Click Container mixing constraints.</span></span>
    * <span data-ttu-id="6b753-200">Mantık bölümlerini karıştırmak, konteynerler içindeki paketleme tahsisat satırları için kurallar eklemenize olanak sağlar.</span><span class="sxs-lookup"><span data-stu-id="6b753-200">Mixing logic breaks allows you to set up rules for packing allocation lines in containers.</span></span> <span data-ttu-id="6b753-201">Örneğin, maddeler konteynerlere atandığında Madde numarası alanını eklerseniz, yeni bir madde numarası olduğunda, yeni bir konteyner oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="6b753-201">For example, if you add the Item number field, when items are assigned to containers, a new container will be created when there is a new item number.</span></span> <span data-ttu-id="6b753-202">Bu, çalışanların aynı konteyner içerisindeki iki farklı müşteri için tahsisat satırlarını paketlemelerinin önüne geçer.</span><span class="sxs-lookup"><span data-stu-id="6b753-202">This is will prevent workers from packing allocations lines for two different customers in the same container.</span></span>  
10. <span data-ttu-id="6b753-203">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="6b753-203">Click New.</span></span>
11. <span data-ttu-id="6b753-204">Tablo alanında, bir seçenek seçin.</span><span class="sxs-lookup"><span data-stu-id="6b753-204">In the Table field, select an option.</span></span>
12. <span data-ttu-id="6b753-205">Alan Seç alanına bir değer girin veya buradan bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="6b753-205">In the Field Select field, enter or select a value.</span></span>
13. <span data-ttu-id="6b753-206">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="6b753-206">Click OK.</span></span>


