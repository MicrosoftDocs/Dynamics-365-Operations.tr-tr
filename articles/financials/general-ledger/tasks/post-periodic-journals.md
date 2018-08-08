--- 
title: "Periyodik günlükleri deftere nakletme"
description: "Tutar, metin ve diğer bilgiler periyodik günlük her alındığında tekrarlandığından, periyodik günlüklere bazen yinelenen günlükler de denir."
author: aprilolson
manager: AnnBe
ms.date: 02/24/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 1d98cbff30620256c9d13e7b4a90314db150e33e
ms.openlocfilehash: 4132f647d8fa225b402a006f0da2347ac9660fa0
ms.contentlocale: tr-tr
ms.lasthandoff: 08/07/2018

---
# <a name="post-periodic-journals"></a><span data-ttu-id="3478a-103">Periyodik günlükleri deftere nakletme</span><span class="sxs-lookup"><span data-stu-id="3478a-103">Post periodic journals</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="3478a-104">Tutar, metin ve diğer bilgiler periyodik günlük her alındığında tekrarlandığından, periyodik günlüklere bazen yinelenen günlükler de denir.</span><span class="sxs-lookup"><span data-stu-id="3478a-104">Periodic journals are sometimes called recurring journals because the amount, text, and other information are repeated each time that the periodic journal is retrieved.</span></span> <span data-ttu-id="3478a-105">Periyodik günlük oluştururken, yineleme için dönem aralığını gün veya ay olarak belirtirsiniz.</span><span class="sxs-lookup"><span data-stu-id="3478a-105">When you create the periodic journal, you specify the period interval for the recurrence, such as days or months.</span></span> <span data-ttu-id="3478a-106">Bu görev kılavuzu, aylık yinelenen bir periyodik günlük oluşturur.</span><span class="sxs-lookup"><span data-stu-id="3478a-106">This task guide will create a periodic journal with a monthly recurrence.</span></span>



1. <span data-ttu-id="3478a-107">Genel muhasebe > Periyodik görevler > Periyodik günlükler'e gidin.</span><span class="sxs-lookup"><span data-stu-id="3478a-107">Go to General ledger > Periodic tasks > Periodic journals.</span></span>
2. <span data-ttu-id="3478a-108">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="3478a-108">Click New.</span></span>
3. <span data-ttu-id="3478a-109">Ad alanına bir değer girin veya buradan bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="3478a-109">In the Name field, enter or select a value.</span></span>
4. <span data-ttu-id="3478a-110">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="3478a-110">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="3478a-111">Açıklama alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="3478a-111">In the Description field, type a value.</span></span>
    * <span data-ttu-id="3478a-112">Açıklama, daha sonra alındığında Periyodik günlüğün adı olacaktır. Bu yüzden ilgili bir ad verdiğinizden emin olun.</span><span class="sxs-lookup"><span data-stu-id="3478a-112">The description will be the name of the Periodic journal when retrieved later so make sure to give it a relevant name.</span></span>  
6. <span data-ttu-id="3478a-113">Satırlar seçeneğine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="3478a-113">Click Lines.</span></span>
    * <span data-ttu-id="3478a-114">Periyodik günlük genellikle birkaç günlük satırı içerir.</span><span class="sxs-lookup"><span data-stu-id="3478a-114">A periodic journal will typically include several journal lines.</span></span> <span data-ttu-id="3478a-115">bu görev kılavuzu ise yalnızca bir satır ekler.</span><span class="sxs-lookup"><span data-stu-id="3478a-115">this task guide will however only add one line.</span></span>  
7. <span data-ttu-id="3478a-116">Tarih alanına bir tarih girin.</span><span class="sxs-lookup"><span data-stu-id="3478a-116">In the Date field, enter a date.</span></span>
    * <span data-ttu-id="3478a-117">Tarih alanı günlük deftere bir sonraki transfer için nakil tarihini içerir.</span><span class="sxs-lookup"><span data-stu-id="3478a-117">The Date field contains the posting date for the next transfer to the daily journal.</span></span> <span data-ttu-id="3478a-118">Her ay alınacak günlükler için, deftere nakledileceği tarihi kullanmanız önerilir; bu genel olarak dönemin ilk veya son tarihidir.</span><span class="sxs-lookup"><span data-stu-id="3478a-118">For journals that will be retrieved each month it is recommended to use the date in the month when it will be posted, typically the first or last date in the period.</span></span> <span data-ttu-id="3478a-119">Tarih alanını boş bırakıp günlük alındığında Boş tarih alanını kullanarak bir tarih vermek de mümkündür.</span><span class="sxs-lookup"><span data-stu-id="3478a-119">It is possible to leave the Date field blank and to give a date when the journal is retrieved, using the Empty date field.</span></span>    <span data-ttu-id="3478a-120">Alan, hareketler alındığında sonraki yinelenen tarih için otomatik olarak güncelleştirilir.</span><span class="sxs-lookup"><span data-stu-id="3478a-120">The field is automatically updated to the next recurring date when transactions are retrieved.</span></span>  
8. <span data-ttu-id="3478a-121">Hesap alanında istediğiniz değerleri belirtin.</span><span class="sxs-lookup"><span data-stu-id="3478a-121">In the Account field, specify the desired values.</span></span>
9. <span data-ttu-id="3478a-122">Açıklama alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="3478a-122">In the Description field, type a value.</span></span>
10. <span data-ttu-id="3478a-123">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="3478a-123">Close the page.</span></span>
11. <span data-ttu-id="3478a-124">Borç alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="3478a-124">In the Debit field, enter a number.</span></span>
12. <span data-ttu-id="3478a-125">Mahsup hesap alanında istediğiniz değerleri belirtin.</span><span class="sxs-lookup"><span data-stu-id="3478a-125">In the Offset account field, specify the desired values.</span></span>
13. <span data-ttu-id="3478a-126">Birim alanında 'Aylar'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="3478a-126">In the Unit field, select 'Months'.</span></span>
14. <span data-ttu-id="3478a-127">Birim sayısı alanına '1' girin.</span><span class="sxs-lookup"><span data-stu-id="3478a-127">In the Number of units field, enter '1'.</span></span>
15. <span data-ttu-id="3478a-128">Son tarih alanına bir tarih girin.</span><span class="sxs-lookup"><span data-stu-id="3478a-128">In the Last date field, enter a date.</span></span>
    * <span data-ttu-id="3478a-129">Önceki dönemin son tarihini girmek, yanlış başlatma döneminde yanlışlıkla yinelenen günlük oluşturulmasını engeller.</span><span class="sxs-lookup"><span data-stu-id="3478a-129">Entering last date in the preceding period will prevent that the recurring journal by mistake is created in the wrong starting period.</span></span> <span data-ttu-id="3478a-130">Son tarih, daha sonra periyodik her alındığında güncelleştirilir.</span><span class="sxs-lookup"><span data-stu-id="3478a-130">Last date will later on be updated each time the periodic journal is retrieved.</span></span>  
16. <span data-ttu-id="3478a-131">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="3478a-131">Click Save.</span></span>
17. <span data-ttu-id="3478a-132">Varsayılan panoya gidin.</span><span class="sxs-lookup"><span data-stu-id="3478a-132">Go to Default dashboard.</span></span>
18. <span data-ttu-id="3478a-133">Genel muhasebe > Günlük girişleri > Genel günlükler'e gidin.</span><span class="sxs-lookup"><span data-stu-id="3478a-133">Go to General ledger > Journal entries > General journals.</span></span>
19. <span data-ttu-id="3478a-134">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="3478a-134">Click New.</span></span>
20. <span data-ttu-id="3478a-135">Ad alanına bir değer girin veya buradan bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="3478a-135">In the Name field, enter or select a value.</span></span>
21. <span data-ttu-id="3478a-136">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="3478a-136">In the list, find and select the desired record.</span></span>
22. <span data-ttu-id="3478a-137">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="3478a-137">In the list, click the link in the selected row.</span></span>
23. <span data-ttu-id="3478a-138">Açıklama alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="3478a-138">In the Description field, type a value.</span></span>
24. <span data-ttu-id="3478a-139">Satırlar seçeneğine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="3478a-139">Click Lines.</span></span>
25. <span data-ttu-id="3478a-140">Periyodik günlük öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="3478a-140">Click Period journal.</span></span>
26. <span data-ttu-id="3478a-141">Günlüğü al'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="3478a-141">Click Retrieve journal.</span></span>
27. <span data-ttu-id="3478a-142">Bitiş tarihi alanına bir tarih girin.</span><span class="sxs-lookup"><span data-stu-id="3478a-142">In the To date field, enter a date.</span></span>
    * <span data-ttu-id="3478a-143">Bitiş tarihi, periyodik fiş satırları için kesme tarihi görevi görür.</span><span class="sxs-lookup"><span data-stu-id="3478a-143">The To date serves as the cutoff date for the periodic voucher lines.</span></span> <span data-ttu-id="3478a-144">Yineleme ayarına bağlı olarak, sonuç olarak oluşturulan günlüğe Son tarih ve Bitiş tarihi için aynı satır bir kereden fazla eklenebilir.</span><span class="sxs-lookup"><span data-stu-id="3478a-144">Based on the recurrence setting, the Last date and To date the same line might be included more than once in the resulting journal.</span></span> <span data-ttu-id="3478a-145">Bitiş tarihi, periyodik satırın günlüğe son kez aktarıldığını oturumun tarihine göre otomatik olarak güncelleştirilir.</span><span class="sxs-lookup"><span data-stu-id="3478a-145">To date is automatically updated based on  session date of the last time the periodic line was transferred to a journal.</span></span>  
28. <span data-ttu-id="3478a-146">Periyodik günlük numarası alanına bir değer girin veya buradan bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="3478a-146">In the Periodic journal number field, enter or select a value.</span></span>
29. <span data-ttu-id="3478a-147">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="3478a-147">In the list, click the link in the selected row.</span></span>
30. <span data-ttu-id="3478a-148">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="3478a-148">Click OK.</span></span>
    * <span data-ttu-id="3478a-149">Dönem günlüğü artık gözden geçirilebilir, onaylanabilir veya gereklilik ve ayara bağlı olarak deftere nakledilebilir.</span><span class="sxs-lookup"><span data-stu-id="3478a-149">The period journal can now be reviewed, approved or posted depending on requirement and setup.</span></span>  


