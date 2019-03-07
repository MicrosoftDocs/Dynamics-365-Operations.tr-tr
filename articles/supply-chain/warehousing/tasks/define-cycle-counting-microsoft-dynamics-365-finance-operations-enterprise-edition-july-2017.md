---
title: 'Döngü sayımı tanımlama '
description: Döngü sayımı eldeki stok maddelerini denetlemek için kullanabileceğiniz bir ambar işlemidir.
author: MarkusFogelberg
manager: AnnBe
ms.date: 06/23/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: mafoge
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2832547f81b0153d42ac4664184f18bd66f1acdd
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2019
ms.locfileid: "337314"
---
# <a name="define-cycle-counting"></a><span data-ttu-id="eca79-103">Döngü sayımı tanımlama </span><span class="sxs-lookup"><span data-stu-id="eca79-103">Define cycle counting</span></span> 

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="eca79-104">Döngü sayımı eldeki stok maddelerini denetlemek için kullanabileceğiniz bir ambar işlemidir.</span><span class="sxs-lookup"><span data-stu-id="eca79-104">Cycle counting is a warehouse process that you can use to audit on-hand inventory items.</span></span> <span data-ttu-id="eca79-105">Bu görev kaydı; varsayılan sayım işi önceliğinin ayarlanmasını, hem çekme hem de sayım süreçlerini işlemek için mobil cihaz menü öğesinin etkinleştirilmesini, bir konum boşaldığında sayım eşiği tetikleyicisinin etkinleştirilmesini ve belirli bir ambar içindeki belirli bir öğe için döngü sayımı planının etkinleştirilmesini kapsar.</span><span class="sxs-lookup"><span data-stu-id="eca79-105">This task recording shows how to set up the default counting work priority, enable a mobile device menu item to process both picking and counting operations, enable a counting threshold trigger when a location becomes empty, and enable a cycle counting plan for a specific item in a specific warehouse.</span></span> <span data-ttu-id="eca79-106">Bu görevler genellikle bir ambar yöneticisi tarafından yapılır.</span><span class="sxs-lookup"><span data-stu-id="eca79-106">Typically, these tasks are performed by a warehouse manager.</span></span> <span data-ttu-id="eca79-107">Bu yordamı demo verileri şirketi USMF veya kendi verilerinizi kullanarak yerine getirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="eca79-107">You can go through this procedure in the USMF demo data company or in your own data.</span></span>


## <a name="set-the-priority-of-counting-work"></a><span data-ttu-id="eca79-108">Sayım çalışma önceliğini ayarlama</span><span class="sxs-lookup"><span data-stu-id="eca79-108">Set the priority of counting work</span></span>
1. <span data-ttu-id="eca79-109">Ambar yönetimi > Kurulum > Ambar yönetimi parametreleri öğesine gidin.</span><span class="sxs-lookup"><span data-stu-id="eca79-109">Go to Warehouse management > Setup > Warehouse management parameters.</span></span>
2. <span data-ttu-id="eca79-110">Döngü sayımı sekmesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="eca79-110">Click the Cycle counting tab.</span></span>
3. <span data-ttu-id="eca79-111">Varsayılan döngü sayısı iş önceliği alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="eca79-111">In the Default cycle count work priority field, enter a number.</span></span>
    * <span data-ttu-id="eca79-112">Bu adım, ambardaki diğer iş türlerine kıyasla döngü sayımı işinin önceliğini değiştirir.</span><span class="sxs-lookup"><span data-stu-id="eca79-112">This step changes the priority of cycle counting work compared to other types of work in the warehouse.</span></span> <span data-ttu-id="eca79-113">Diğer iş türlerinden daha düşük bir sayı girerek, döngü sayımı işinin önceliğini artırırsınız.</span><span class="sxs-lookup"><span data-stu-id="eca79-113">By entering a number that is lower than the number for other types of work, you raise the priority of the cycle counting work.</span></span>  
4. <span data-ttu-id="eca79-114">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="eca79-114">Click Save.</span></span>
5. <span data-ttu-id="eca79-115">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="eca79-115">Close the page.</span></span>

## <a name="enable-the-mobile-device"></a><span data-ttu-id="eca79-116">Mobil cihazı etkinleştirin</span><span class="sxs-lookup"><span data-stu-id="eca79-116">Enable the mobile device</span></span>
1. <span data-ttu-id="eca79-117">Ambar yönetimi > Kurulum > Mobil cihaz > Mobil cihaz menüsü öğeleri seçeneğine gidin.</span><span class="sxs-lookup"><span data-stu-id="eca79-117">Go to Warehouse management > Setup > Mobile device > Mobile device menu items.</span></span>
2. <span data-ttu-id="eca79-118">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="eca79-118">Click New.</span></span>
3. <span data-ttu-id="eca79-119">Menü öğesi adı alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="eca79-119">In the Menu item name field, type a value.</span></span>
4. <span data-ttu-id="eca79-120">Başlık alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="eca79-120">In the Title field, type a value.</span></span>
5. <span data-ttu-id="eca79-121">Mod alanında, 'İş' seçin.</span><span class="sxs-lookup"><span data-stu-id="eca79-121">In the Mode field, select 'Work'.</span></span>
6. <span data-ttu-id="eca79-122">Mevcut işin kullanılması seçeneğinde Evet'i işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="eca79-122">Set the Use existing work option to Yes.</span></span>
    * <span data-ttu-id="eca79-123">Bu seçeneği Evet olarak ayarladığınızda, sistem, mobil aygıt menü öğesi kullanıldığında var olan işleri arar.</span><span class="sxs-lookup"><span data-stu-id="eca79-123">When you set this option to Yes, the system will look for existing work when the mobile device menu item is used.</span></span>  
7. <span data-ttu-id="eca79-124">Yöneten alanında Sistem'i seçin.</span><span class="sxs-lookup"><span data-stu-id="eca79-124">In the Directed by field, select 'System directed'.</span></span>
    * <span data-ttu-id="eca79-125">"Sistem tarafından yönlendirilen" seçildiğinde, ambar çalışanı iş sınıflarında tanımlanan açık işe yönlendirilir.</span><span class="sxs-lookup"><span data-stu-id="eca79-125">When "System directed" is selected, the warehouse worker will be directed to open work that is in defined work classes.</span></span> <span data-ttu-id="eca79-126">(Sırada bu iş sınıflarını oluşturacağız.)</span><span class="sxs-lookup"><span data-stu-id="eca79-126">(We will create these work classes next.)</span></span>  
8. <span data-ttu-id="eca79-127">İş sınıfları bölümünü genişletin veya daraltın.</span><span class="sxs-lookup"><span data-stu-id="eca79-127">Expand or collapse the Work classes section.</span></span>
    * <span data-ttu-id="eca79-128">Daha sonra bu mobil aygıt menü öğesi ile kullanılacak iki iş sınıfı oluşturacağız.</span><span class="sxs-lookup"><span data-stu-id="eca79-128">Next, we will create two work classes that will be used with this mobile device menu item.</span></span> <span data-ttu-id="eca79-129">Menü öğesi kullanıldığında, bu iş sınıfları sıraya konulacaktır ve en yüksek önceliğe sahip işin kullanıcıya gösterilecektir.</span><span class="sxs-lookup"><span data-stu-id="eca79-129">When the menu item is used, these work classes will be queried, and the work that has the highest priority will be shown to the user.</span></span>  
9. <span data-ttu-id="eca79-130">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="eca79-130">Click New.</span></span>
10. <span data-ttu-id="eca79-131">İş sınıfı numarası alanına bir değer girin veya buradan bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="eca79-131">In the Work class ID field, select a value.</span></span>
11. <span data-ttu-id="eca79-132">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="eca79-132">Click New.</span></span>
12. <span data-ttu-id="eca79-133">İş sınıfı numarası alanına bir değer girin veya buradan bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="eca79-133">In the Work class ID field, select a value.</span></span>
13. <span data-ttu-id="eca79-134">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="eca79-134">Click Save.</span></span>
14. <span data-ttu-id="eca79-135">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="eca79-135">Close the page.</span></span>
15. <span data-ttu-id="eca79-136">Ambar yönetimi > Kurulum > Mobil cihaz > Mobil cihaz menüsü öğesine gidin.</span><span class="sxs-lookup"><span data-stu-id="eca79-136">Go to Warehouse management > Setup > Mobile device > Mobile device menu.</span></span>
16. <span data-ttu-id="eca79-137">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="eca79-137">In the list, find and select the desired record.</span></span>
17. <span data-ttu-id="eca79-138">Ağaçta, 'oluşturmuş olduğunuz menü öğesini seçin'.</span><span class="sxs-lookup"><span data-stu-id="eca79-138">In the tree, select 'the menu item that you just created'.</span></span>
18. <span data-ttu-id="eca79-139">Düzenle öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="eca79-139">Click Edit.</span></span>
19. <span data-ttu-id="eca79-140">Menüye menü öğesi eklemek için oku tıklatın.</span><span class="sxs-lookup"><span data-stu-id="eca79-140">Click the arrow to add the menu item to the menu.</span></span>
20. <span data-ttu-id="eca79-141">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="eca79-141">Click Save.</span></span>

## <a name="create-a-counting-threshold"></a><span data-ttu-id="eca79-142">Bir sayım eşiği yaratın</span><span class="sxs-lookup"><span data-stu-id="eca79-142">Create a counting threshold</span></span>
1. <span data-ttu-id="eca79-143">Ambar yönetimi > Kurulum > Döngü sayımı > Döngü sayımı eşikleri öğesine gidin.</span><span class="sxs-lookup"><span data-stu-id="eca79-143">Go to Warehouse management > Setup > Cycle counting > Cycle count thresholds.</span></span>
2. <span data-ttu-id="eca79-144">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="eca79-144">Click New.</span></span>
3. <span data-ttu-id="eca79-145">Döngü sayımı eşiği numarası alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="eca79-145">In the Cycle counting threshold ID field, type a value.</span></span>
4. <span data-ttu-id="eca79-146">Döngü sayımını hemen işleme seçeneğinde Evet'i seçin.</span><span class="sxs-lookup"><span data-stu-id="eca79-146">Set the Process cycle counting immediately option to Yes.</span></span>
5. <span data-ttu-id="eca79-147">Açıklama alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="eca79-147">In the Description field, type a value.</span></span>
6. <span data-ttu-id="eca79-148">Kaydet'i tıklatın.</span><span class="sxs-lookup"><span data-stu-id="eca79-148">Click Save.</span></span>
7. <span data-ttu-id="eca79-149">Konumları Seç'i tıklatın.</span><span class="sxs-lookup"><span data-stu-id="eca79-149">Click Select locations.</span></span>
8. <span data-ttu-id="eca79-150">Listede, seçili satırı işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="eca79-150">In the list, mark the selected row.</span></span>
9. <span data-ttu-id="eca79-151">Ölçütler alanından bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="eca79-151">In the Criteria field, select a value.</span></span>
10. <span data-ttu-id="eca79-152">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="eca79-152">Click OK.</span></span>
11. <span data-ttu-id="eca79-153">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="eca79-153">Close the page.</span></span>

## <a name="create-a-cycle-count-plan"></a><span data-ttu-id="eca79-154">Bir döngü sayım planı yaratın</span><span class="sxs-lookup"><span data-stu-id="eca79-154">Create a cycle count plan</span></span>
1. <span data-ttu-id="eca79-155">Ambar yönetimi > Kurulum > Döngü sayımı > Döngü sayımı planları öğesine gidin.</span><span class="sxs-lookup"><span data-stu-id="eca79-155">Go to Warehouse management > Setup > Cycle counting > Cycle count plans.</span></span>
2. <span data-ttu-id="eca79-156">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="eca79-156">Click New.</span></span>
3. <span data-ttu-id="eca79-157">Döngü sayımı planı numarası alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="eca79-157">In the Cycle counting plan ID field, type a value.</span></span>
4. <span data-ttu-id="eca79-158">Tanım alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="eca79-158">In the Description field, type a value.</span></span>
5. <span data-ttu-id="eca79-159">Maksimum döngü sayımı miktarı alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="eca79-159">In the Maximum number of cycle counts field, enter a number.</span></span>
6. <span data-ttu-id="eca79-160">Kaydet'i tıklatın.</span><span class="sxs-lookup"><span data-stu-id="eca79-160">Click Save.</span></span>
7. <span data-ttu-id="eca79-161">Konumları Seç'i tıklatın.</span><span class="sxs-lookup"><span data-stu-id="eca79-161">Click Select locations.</span></span>
8. <span data-ttu-id="eca79-162">Listede, seçili satırı işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="eca79-162">In the list, mark the selected row.</span></span>
9. <span data-ttu-id="eca79-163">Ölçütler alanından bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="eca79-163">In the Criteria field, select a value.</span></span>
10. <span data-ttu-id="eca79-164">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="eca79-164">Click OK.</span></span>
11. <span data-ttu-id="eca79-165">Döngü sayımları arasındaki günler alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="eca79-165">In the Days between cycle counting field, enter a number.</span></span>
    * <span data-ttu-id="eca79-166">Örneğin, döngü sayımı alanında gün olarak belirtilen değer 5 olarak ayarlanmışsa, her beş günde oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="eca79-166">For example, if the Days between cycle counting field is set to 5, cycle counting work will be created every five days.</span></span> <span data-ttu-id="eca79-167">Ancak, döngü sayımı işi üçüncü günde işleniyorsa, bir sonraki döngü sayımı işi son döngü sayımı işlendikten beş gün sonra, 8. gün içinde oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="eca79-167">However, if cycle counting work is processed on day three, the next cycle counting work will be created five days after the last cycle counting was processed, on day 8.</span></span>  
12. <span data-ttu-id="eca79-168">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="eca79-168">Click Save.</span></span>
13. <span data-ttu-id="eca79-169">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="eca79-169">Click New.</span></span>
14. <span data-ttu-id="eca79-170">Sıra numarası alanına bir numara girin.</span><span class="sxs-lookup"><span data-stu-id="eca79-170">In the Sequence number field, enter a number.</span></span>
    * <span data-ttu-id="eca79-171">Sıralama en küçük sayıdan en büyük sayıyadır.</span><span class="sxs-lookup"><span data-stu-id="eca79-171">The sort is from the smallest number to the largest number.</span></span> <span data-ttu-id="eca79-172">Değer 0'dan (sıfır) fazla olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="eca79-172">The value must be more than 0 (zero).</span></span>  
15. <span data-ttu-id="eca79-173">Listede, seçili satırı işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="eca79-173">In the list, mark the selected row.</span></span>
16. <span data-ttu-id="eca79-174">Açıklama alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="eca79-174">In the Description field, type a value.</span></span>
17. <span data-ttu-id="eca79-175">Kaydet'i tıklatın.</span><span class="sxs-lookup"><span data-stu-id="eca79-175">Click Save.</span></span>
18. <span data-ttu-id="eca79-176">Ürün sorgusu tanımla'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="eca79-176">Click Define product query.</span></span>
19. <span data-ttu-id="eca79-177">Listede, seçili satırı işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="eca79-177">In the list, mark the selected row.</span></span>
20. <span data-ttu-id="eca79-178">Ölçütler alanında bir değer girin veya seçin.</span><span class="sxs-lookup"><span data-stu-id="eca79-178">In the Criteria field, enter or select a value.</span></span>
21. <span data-ttu-id="eca79-179">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="eca79-179">Click OK.</span></span>
22. <span data-ttu-id="eca79-180">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="eca79-180">Close the page.</span></span>

