---
title: Personelin yaralanma ve hastalık bilgilerini koruma
description: Bazı ayar bilgileri burada kullanıldığından, 'Yaralanma ve hastalık ayarlama' görevini önce tamamlamanız tavsiye edilir.
author: ShielaSogge
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: HRMInjuryIncident, HcmWorkerLookUp
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shielas
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 03d1e7f7b648e65cbe628aa4ff8b39dfa03ce96b
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2019
ms.locfileid: "332622"
---
# <a name="maintain-employee-injury-and-illness-information"></a><span data-ttu-id="b81dd-103">Personelin yaralanma ve hastalık bilgilerini koruma</span><span class="sxs-lookup"><span data-stu-id="b81dd-103">Maintain employee injury and illness information</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="b81dd-104">Bazı ayar bilgileri burada kullanıldığından, 'Yaralanma ve hastalık ayarlama' görevini önce tamamlamanız tavsiye edilir.</span><span class="sxs-lookup"><span data-stu-id="b81dd-104">It is recommended to complete the 'Setup injury and illness' task guide first, as some of the setup information is used here.</span></span> 



<span data-ttu-id="b81dd-105">Bu görev, bir yaralanma veya hastalık örneği oluşturmanın temel adımlarını kapsar.</span><span class="sxs-lookup"><span data-stu-id="b81dd-105">This task recording covers the basic steps to creating an injury or illness case.</span></span> <span data-ttu-id="b81dd-106">Yaralanma veya hastalık ayrıntılarını izlemenin yanı sıra, izlenen bir servis talebi de vardır.</span><span class="sxs-lookup"><span data-stu-id="b81dd-106">Besides tracking the details of the injury or illness, there is a case status that is tracked as well.</span></span>  <span data-ttu-id="b81dd-107">Vaka varsayılan olarak 'açık' durumundadır.</span><span class="sxs-lookup"><span data-stu-id="b81dd-107">The case defaults with an 'open' status.</span></span>  <span data-ttu-id="b81dd-108">Durumlar, uygulama formun üst tarafındaki çubuğundaki 'Servis talebi' menü öğesinden yönetilebilir.</span><span class="sxs-lookup"><span data-stu-id="b81dd-108">The statuses can be managed from the 'Case status' menu item in the application bar at the top of the form.</span></span>

1. <span data-ttu-id="b81dd-109">İnsan Kaynakları > Çalışanlar > Yaralanma ve hastalık > Yaralanma veya hastalık olayları'na gidin.</span><span class="sxs-lookup"><span data-stu-id="b81dd-109">Go to Human resources > Workers > Injury and illness > Injury or illness incidents.</span></span>
2. <span data-ttu-id="b81dd-110">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="b81dd-110">Click New.</span></span>
3. <span data-ttu-id="b81dd-111">Olay açıklaması alanında bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="b81dd-111">In the Case description field, type a value.</span></span>
    * <span data-ttu-id="b81dd-112">Örnek: Bilek sakatlığı</span><span class="sxs-lookup"><span data-stu-id="b81dd-112">Example:  Wrist injury</span></span>  
4. <span data-ttu-id="b81dd-113">Çalışan alanında bir değer girin veya bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="b81dd-113">In the Worker field, enter or select a value.</span></span>
    * <span data-ttu-id="b81dd-114">Örnek: Ahmet Bora</span><span class="sxs-lookup"><span data-stu-id="b81dd-114">Example: Ahmed Barnett</span></span>  
5. <span data-ttu-id="b81dd-115">Olayın tarihi ve saati alanında bir tarih ve saat girin.</span><span class="sxs-lookup"><span data-stu-id="b81dd-115">In the Date and time of incident field, enter a date and time.</span></span>
    * <span data-ttu-id="b81dd-116">Örnek: 1/20/2016 10:00 AM</span><span class="sxs-lookup"><span data-stu-id="b81dd-116">Example:  1/20/2016 10:00 AM</span></span>  
6. <span data-ttu-id="b81dd-117">Yaralanma veya hastalık türü alanında bir değer girin veya seçin.</span><span class="sxs-lookup"><span data-stu-id="b81dd-117">In the Injury or illness type field, enter or select a value.</span></span>
    * <span data-ttu-id="b81dd-118">Örnek: Kırık</span><span class="sxs-lookup"><span data-stu-id="b81dd-118">Example:  Fracture</span></span>  
7. <span data-ttu-id="b81dd-119">Vücut bölümü alanında bir değer girin veya bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="b81dd-119">In the Body part field, enter or select a value.</span></span>
    * <span data-ttu-id="b81dd-120">Örnek: Bilek</span><span class="sxs-lookup"><span data-stu-id="b81dd-120">Example:  Wrist</span></span>  
8. <span data-ttu-id="b81dd-121">Sonuç türü alanında bir değer girin veya bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="b81dd-121">In the Outcome type field, enter or select a value.</span></span>
    * <span data-ttu-id="b81dd-122">Örnek: Terapi</span><span class="sxs-lookup"><span data-stu-id="b81dd-122">Example:  Therapy</span></span>  
9. <span data-ttu-id="b81dd-123">Raporlanma tarihi ve saati alanında bir tarih ve saat girin.</span><span class="sxs-lookup"><span data-stu-id="b81dd-123">In the Date and time reported field, enter a date and time.</span></span>
    * <span data-ttu-id="b81dd-124">Raporlanan tarih ve saat, olayın tarih ve saatinden sonra olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="b81dd-124">The date and time reported must be later than the date and time of incident.</span></span>  
10. <span data-ttu-id="b81dd-125">Servis talebini rapor eden kişi alanında bir değer girin veya seçin.</span><span class="sxs-lookup"><span data-stu-id="b81dd-125">In the Person who reported case field, enter or select a value.</span></span>
    * <span data-ttu-id="b81dd-126">Bu, olaya tanık bir çalışan veya başka bir şahit olabilir.</span><span class="sxs-lookup"><span data-stu-id="b81dd-126">This could be the employee or another witness to the incident.</span></span>  <span data-ttu-id="b81dd-127">Örnek: Ahmet Bora</span><span class="sxs-lookup"><span data-stu-id="b81dd-127">Example: Ahmed Barnett</span></span>  
11. <span data-ttu-id="b81dd-128">Olay bölümünü genişletin.</span><span class="sxs-lookup"><span data-stu-id="b81dd-128">Expand the Incident section.</span></span>
12. <span data-ttu-id="b81dd-129">Olayın oluştuğu yer alanında bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="b81dd-129">In the Where incident occurred field, type a value.</span></span>
    * <span data-ttu-id="b81dd-130">Örnek: Ambar</span><span class="sxs-lookup"><span data-stu-id="b81dd-130">Example:  Warehouse</span></span>  
13. <span data-ttu-id="b81dd-131">Çalışılan yerde alanında Evet'i seçin.</span><span class="sxs-lookup"><span data-stu-id="b81dd-131">Select Yes in the On work premises field.</span></span>
    * <span data-ttu-id="b81dd-132">Olay çalışılan yerde meydana geldiyse, evet'i seçin.</span><span class="sxs-lookup"><span data-stu-id="b81dd-132">If the incident occurred on work premises, select yes.</span></span>  
14. <span data-ttu-id="b81dd-133">İşe başladığı tarih ve saat alanında bir tarih ve saat girin.</span><span class="sxs-lookup"><span data-stu-id="b81dd-133">In the Date and time began work field, enter a date and time.</span></span>
    * <span data-ttu-id="b81dd-134">Olay gerçekleşmeden önce bireyin çalışmaya başlamasını etkileyen tarih ve saati girin.</span><span class="sxs-lookup"><span data-stu-id="b81dd-134">Enter the date and time that affected individual started working, prior to the incident occurring.</span></span>  
15. <span data-ttu-id="b81dd-135">Çalışanın işi veya görevi alanında bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="b81dd-135">In the Employee job or task field, type a value.</span></span>
    * <span data-ttu-id="b81dd-136">Olay meydana geldiğinde çalışanın yapmakta olduğu işi veya görevi girin.</span><span class="sxs-lookup"><span data-stu-id="b81dd-136">Enter the job or task the worker was performing when the incident occurred.</span></span>  <span data-ttu-id="b81dd-137">Örnek: Kutuları yükleme</span><span class="sxs-lookup"><span data-stu-id="b81dd-137">Example:  Loading boxes</span></span>  
16. <span data-ttu-id="b81dd-138">Olayın nedeni alanında bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="b81dd-138">In the Cause of incident field, type a value.</span></span>
    * <span data-ttu-id="b81dd-139">Olayın nedenini girin.</span><span class="sxs-lookup"><span data-stu-id="b81dd-139">Enter the cause of the incident.</span></span>  <span data-ttu-id="b81dd-140">Örnek: Islak zeminde kayma</span><span class="sxs-lookup"><span data-stu-id="b81dd-140">Example:  Slipped on wet floor</span></span>  
17. <span data-ttu-id="b81dd-141">Önem düzeyi alanında bir değer girin veya bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="b81dd-141">In the Severity level field, enter or select a value.</span></span>
18. <span data-ttu-id="b81dd-142">Gerçekleştirilecek eylem alanında bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="b81dd-142">In the Action to be taken field, type a value.</span></span>
    * <span data-ttu-id="b81dd-143">Örnek: Dökülen sıvıları hemen temizleme</span><span class="sxs-lookup"><span data-stu-id="b81dd-143">Example:  Clean up spills promptly</span></span>  
19. <span data-ttu-id="b81dd-144">İşbaşı yapmadan geçirmesi beklenen gün sayısı alanında bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="b81dd-144">In the Expected days away from work field, enter a number.</span></span>
    * <span data-ttu-id="b81dd-145">Bireyin işten uzak kalması beklenen gün sayısını girin.</span><span class="sxs-lookup"><span data-stu-id="b81dd-145">Enter the number of days that the individual is expected to be away from work.</span></span>  <span data-ttu-id="b81dd-146">Birey işe döndüğünde, 'İşten uzakta geçen gün sayısı' alanını gelmediği gerçek gün sayısıyla güncelleştirin.</span><span class="sxs-lookup"><span data-stu-id="b81dd-146">Once the individual returns to work, update the 'Days away from work' field with the actual number of days away.</span></span>  
20. <span data-ttu-id="b81dd-147">Yaralanma veya hastalık maliyetleri bölümünü genişletin.</span><span class="sxs-lookup"><span data-stu-id="b81dd-147">Expand the Injury or illness costs section.</span></span>
21. <span data-ttu-id="b81dd-148">Ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="b81dd-148">Click Add.</span></span>
22. <span data-ttu-id="b81dd-149">Tarih alanına bir tarih girin.</span><span class="sxs-lookup"><span data-stu-id="b81dd-149">In the Date field, enter a date.</span></span>
23. <span data-ttu-id="b81dd-150">Maliyet türü alanında bir değer girin veya bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="b81dd-150">In the Cost type field, enter or select a value.</span></span>
    * <span data-ttu-id="b81dd-151">Örnek:  Terapi    Bir tutar girebilir ve faturalar veya doktorun notları gibi destekleyici belgeleri maliyete ekleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="b81dd-151">Example:  Therapy    You can also enter in an amount, and attach any supporting documentation such as invoices or doctor's notes to the cost.</span></span>  
24. <span data-ttu-id="b81dd-152">Ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="b81dd-152">Click Add.</span></span>
25. <span data-ttu-id="b81dd-153">Tarih alanına bir tarih girin.</span><span class="sxs-lookup"><span data-stu-id="b81dd-153">In the Date field, enter a date.</span></span>
26. <span data-ttu-id="b81dd-154">Maliyet türü alanında bir değer girin veya bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="b81dd-154">In the Cost type field, enter or select a value.</span></span>
    * <span data-ttu-id="b81dd-155">Örnek: Doktor</span><span class="sxs-lookup"><span data-stu-id="b81dd-155">Example: Doctor</span></span>  
27. <span data-ttu-id="b81dd-156">Yaralanma veya hastalık tedavileri bölümünü genişletin.</span><span class="sxs-lookup"><span data-stu-id="b81dd-156">Expand the Injury or illness treatments section.</span></span>
28. <span data-ttu-id="b81dd-157">Ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="b81dd-157">Click Add.</span></span>
29. <span data-ttu-id="b81dd-158">Tedavi tarihi alanında bir tarih ve saat girin.</span><span class="sxs-lookup"><span data-stu-id="b81dd-158">In the Treatment date field, enter a date and time.</span></span>
30. <span data-ttu-id="b81dd-159">Tedavi türü alanında bir değer girin veya seçin.</span><span class="sxs-lookup"><span data-stu-id="b81dd-159">In the Treatment type field, enter or select a value.</span></span>
    * <span data-ttu-id="b81dd-160">Örnek: Atel</span><span class="sxs-lookup"><span data-stu-id="b81dd-160">Example:  Splint</span></span>  
31. <span data-ttu-id="b81dd-161">İsteğe bağlı olarak, acil servis hastane ziyareti bölümünü Evet olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="b81dd-161">Optionally, set the emergency room hospital visit section to Yes.</span></span>
32. <span data-ttu-id="b81dd-162">Tedavi açıklamaları alanında bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="b81dd-162">In the Treatment comments field, type a value.</span></span>
    * <span data-ttu-id="b81dd-163">Örnek: 2 hafta süresince atel</span><span class="sxs-lookup"><span data-stu-id="b81dd-163">Example:  Splint for 2 weeks</span></span>  
33. <span data-ttu-id="b81dd-164">Doktorun adı alanında bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="b81dd-164">In the Physician name field, type a value.</span></span>
    * <span data-ttu-id="b81dd-165">Örnek: Dr. Yılmaz</span><span class="sxs-lookup"><span data-stu-id="b81dd-165">Example:  Dr. Anderson</span></span>  
34. <span data-ttu-id="b81dd-166">Tedavi tesisi ve yeri alanında bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="b81dd-166">In the Treatment facility and location field, type a value.</span></span>
    * <span data-ttu-id="b81dd-167">Örnek: Vatan Cad. Acil Servis</span><span class="sxs-lookup"><span data-stu-id="b81dd-167">Example:  Elm St. Emergency</span></span>  
35. <span data-ttu-id="b81dd-168">Tedavi ayrıntıları alanında bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="b81dd-168">In the Treatment details field, type a value.</span></span>
    * <span data-ttu-id="b81dd-169">Örnek: Kırık röntgende görünüyor, atel takıldı</span><span class="sxs-lookup"><span data-stu-id="b81dd-169">Example:  Xray confirms fracture, wear splint</span></span>  
36. <span data-ttu-id="b81dd-170">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="b81dd-170">Click Save.</span></span>
    * <span data-ttu-id="b81dd-171">Servis talebi her zaman güncelleştirilebilir.</span><span class="sxs-lookup"><span data-stu-id="b81dd-171">The case status can be updated at any time.</span></span>  <span data-ttu-id="b81dd-172">Yaralanma veya hastalığın işlenmesini sürüyorsa vakayı 'süren iş' olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="b81dd-172">Set the case to in process, if the processing of the injury or illness is in process.</span></span>  <span data-ttu-id="b81dd-173">Olayı bir defa kapattığınızda, yalnızca maliyet, tedavi ekleyip kaldırabilir veya olayla ilgili dosyalamalar yapabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="b81dd-173">Once you close the incident you can only add or remove costs, treatments or filings related to the incident.</span></span>  <span data-ttu-id="b81dd-174">Diğer bilgileri değiştirmek için olayı yeniden açın.</span><span class="sxs-lookup"><span data-stu-id="b81dd-174">To modify other information, reopen the case.</span></span>  

