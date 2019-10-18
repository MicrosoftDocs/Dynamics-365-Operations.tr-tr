---
title: Periyodik günlükleri deftere nakletme
description: Tutar, metin ve diğer bilgiler periyodik günlük her alındığında tekrarlandığından, periyodik günlüklere bazen yinelenen günlükler de denir.
author: aprilolson
manager: AnnBe
ms.date: 06/26/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalTable, LedgerJournalTransPeriodic, LedgerJournalTransDaily
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 4fdf630e9d292d0e016b6624a82b047d32bab898
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/27/2019
ms.locfileid: "2175672"
---
# <a name="post-periodic-journals"></a><span data-ttu-id="6be93-103">Periyodik günlükleri deftere nakletme</span><span class="sxs-lookup"><span data-stu-id="6be93-103">Post periodic journals</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="6be93-104">Tutar, metin ve diğer bilgiler periyodik günlük her alındığında tekrarlandığından, periyodik günlüklere bazen yinelenen günlükler de denir.</span><span class="sxs-lookup"><span data-stu-id="6be93-104">Periodic journals are sometimes called recurring journals because the amount, text, and other information are repeated each time that the periodic journal is retrieved.</span></span> <span data-ttu-id="6be93-105">Periyodik günlük oluştururken, yineleme için dönem aralığını gün veya ay olarak belirtirsiniz.</span><span class="sxs-lookup"><span data-stu-id="6be93-105">When you create the periodic journal, you specify the period interval for the recurrence, such as days or months.</span></span> <span data-ttu-id="6be93-106">Bu görev kılavuzu, aylık yinelenen bir periyodik günlük oluşturur.</span><span class="sxs-lookup"><span data-stu-id="6be93-106">This task guide will create a periodic journal with a monthly recurrence.</span></span>

1. <span data-ttu-id="6be93-107">**Gezinti bölmesi > Modüller > Genel muhasebe > Periyodik görevler > Periyodik günlükler**'e gidin.</span><span class="sxs-lookup"><span data-stu-id="6be93-107">Go to **Navigation pane > Modules > General ledger > Periodic tasks > Periodic journals**.</span></span>
2. <span data-ttu-id="6be93-108">**Yeni**'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="6be93-108">Click **New**.</span></span>
3. <span data-ttu-id="6be93-109">**Ad** alanına bir değer girin veya buradan bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="6be93-109">In the **Name** field, enter or select a value.</span></span>
4. <span data-ttu-id="6be93-110">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="6be93-110">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="6be93-111">**Tanım** alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="6be93-111">In the **Description** field, type a value.</span></span> <span data-ttu-id="6be93-112">Açıklama, daha sonra alındığında Periyodik günlüğün adı olacaktır. Bu yüzden ilgili bir ad verdiğinizden emin olun.</span><span class="sxs-lookup"><span data-stu-id="6be93-112">The description will be the name of the Periodic journal when retrieved later so make sure to give it a relevant name.</span></span>
6. <span data-ttu-id="6be93-113">**Eylem Bölmesi**'nde, **Satırlar** öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="6be93-113">On the **Action pane**, click **Lines**.</span></span> <span data-ttu-id="6be93-114">Periyodik günlük genellikle birkaç günlük satırı içerir.</span><span class="sxs-lookup"><span data-stu-id="6be93-114">A periodic journal will typically include several journal lines.</span></span> <span data-ttu-id="6be93-115">bu görev kılavuzu ise yalnızca bir satır ekler.</span><span class="sxs-lookup"><span data-stu-id="6be93-115">this task guide will however only add one line.</span></span>
7. <span data-ttu-id="6be93-116">**Tarih** alanına bir tarih girin.</span><span class="sxs-lookup"><span data-stu-id="6be93-116">In the **Date** field, enter a date.</span></span> <span data-ttu-id="6be93-117">**Tarih** alanı, günlük deftere bir sonraki transfer için nakil tarihini içerir.</span><span class="sxs-lookup"><span data-stu-id="6be93-117">The **Date** field contains the posting date for the next transfer to the daily journal.</span></span> <span data-ttu-id="6be93-118">Her ay alınacak günlükler için, deftere nakledileceği tarihi kullanmanız önerilir; bu genel olarak dönemin ilk veya son tarihidir.</span><span class="sxs-lookup"><span data-stu-id="6be93-118">For journals that will be retrieved each month it is recommended to use the date in the month when it will be posted, typically the first or last date in the period.</span></span> <span data-ttu-id="6be93-119">Tarih alanını boş bırakıp günlük alındığında Boş tarih alanını kullanarak bir tarih vermek de mümkündür.</span><span class="sxs-lookup"><span data-stu-id="6be93-119">It is possible to leave the Date field blank and to give a date when the journal is retrieved, using the Empty date field.</span></span> <span data-ttu-id="6be93-120">Alan, hareketler alındığında sonraki yinelenen tarih için otomatik olarak güncelleştirilir.</span><span class="sxs-lookup"><span data-stu-id="6be93-120">The field is automatically updated to the next recurring date when transactions are retrieved.</span></span> 
8. <span data-ttu-id="6be93-121">**Hesap** alanında istediğiniz değerleri belirtin.</span><span class="sxs-lookup"><span data-stu-id="6be93-121">In the **Account** field, specify the desired values.</span></span>
9. <span data-ttu-id="6be93-122">**Açıklama** alanında bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="6be93-122">In the **Description** field, select a value.</span></span>
10. <span data-ttu-id="6be93-123">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="6be93-123">Close the page.</span></span>
11. <span data-ttu-id="6be93-124">**Borç** alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="6be93-124">In the **Debit** field, enter a number.</span></span>
12. <span data-ttu-id="6be93-125">**Mahsup hesap** alanında istediğiniz değerleri belirtin.</span><span class="sxs-lookup"><span data-stu-id="6be93-125">In the **Offset account** field, specify the desired values.</span></span>
13. <span data-ttu-id="6be93-126">**Birim** alanında "Aylar"ı seçin.</span><span class="sxs-lookup"><span data-stu-id="6be93-126">In the **Unit** field, select 'Months'.</span></span>
14. <span data-ttu-id="6be93-127">**Birim sayısı** alanına "1" girin.</span><span class="sxs-lookup"><span data-stu-id="6be93-127">In the **Number of units** field, enter '1'.</span></span>
15. <span data-ttu-id="6be93-128">**Son tarih** alanına bir tarih girin.</span><span class="sxs-lookup"><span data-stu-id="6be93-128">In the **Last date** field, enter a date.</span></span> <span data-ttu-id="6be93-129">Önceki dönemin son tarihini girmek, yanlış başlatma döneminde yanlışlıkla yinelenen günlük oluşturulmasını engeller.</span><span class="sxs-lookup"><span data-stu-id="6be93-129">Entering last date in the preceding period will prevent that the recurring journal by mistake is created in the wrong starting period.</span></span> <span data-ttu-id="6be93-130">Son tarih, daha sonra periyodik her alındığında güncelleştirilir.</span><span class="sxs-lookup"><span data-stu-id="6be93-130">Last date will later on be updated each time the periodic journal is retrieved.</span></span> 
16. <span data-ttu-id="6be93-131">**Kaydet**'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="6be93-131">Click **Save**.</span></span>
17. <span data-ttu-id="6be93-132">**Gezinti bölmesi > Modüller > Genel muhasebe > Günlük girişleri > Genel günlükler**'e gidin.</span><span class="sxs-lookup"><span data-stu-id="6be93-132">Go to **Navigation pane > Modules > General ledger > Journal entries > General journals**.</span></span>
18. <span data-ttu-id="6be93-133">**Yeni**'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="6be93-133">Click **New**.</span></span>
19. <span data-ttu-id="6be93-134">**Ad** alanına bir değer girin veya buradan bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="6be93-134">In the **Name** field, enter or select a value.</span></span>
20. <span data-ttu-id="6be93-135">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="6be93-135">In the list, find and select the desired record.</span></span>
21. <span data-ttu-id="6be93-136">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="6be93-136">In the list, click the link in the selected row.</span></span>
22. <span data-ttu-id="6be93-137">**Tanım** alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="6be93-137">In the **Description** field, type a value.</span></span>
23. <span data-ttu-id="6be93-138">**Eylem Bölmesi**'nde, **Satırlar** öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="6be93-138">On the **Action pane**, click **Lines**.</span></span>
24. <span data-ttu-id="6be93-139">**Eylem bölmesi**'nde **Periyodik günlük**'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="6be93-139">On the **Action pane**, click **Period journal**.</span></span>
25. <span data-ttu-id="6be93-140">**Günlüğü al**'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="6be93-140">Click **Retrieve journal**.</span></span>
26. <span data-ttu-id="6be93-141">**Bitiş tarihi** alanına bir tarih girin.</span><span class="sxs-lookup"><span data-stu-id="6be93-141">In the **To date** field, enter a date.</span></span> <span data-ttu-id="6be93-142">**Bitiş tarihi**, periyodik fiş satırları için kesme tarihi görevi görür.</span><span class="sxs-lookup"><span data-stu-id="6be93-142">The **To date** serves as the cutoff date for the periodic voucher lines.</span></span> <span data-ttu-id="6be93-143">Yineleme ayarına bağlı olarak, sonuç olarak oluşturulan günlüğe Son tarih ve Bitiş tarihi için aynı satır bir kereden fazla eklenebilir.</span><span class="sxs-lookup"><span data-stu-id="6be93-143">Based on the recurrence setting, the Last date and To date the same line might be included more than once in the resulting journal.</span></span> <span data-ttu-id="6be93-144">Bitiş tarihi, periyodik satırın günlüğe son kez aktarıldığını oturumun tarihine göre otomatik olarak güncelleştirilir.</span><span class="sxs-lookup"><span data-stu-id="6be93-144">To date is automatically updated based on  session date of the last time the periodic line was transferred to a journal.</span></span> 
27. <span data-ttu-id="6be93-145">**Periyodik günlük numarası** alanına bir değer girin veya buradan bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="6be93-145">In the **Periodic journal number** field, enter or select a value.</span></span>
28. <span data-ttu-id="6be93-146">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="6be93-146">In the list, click the link in the selected row.</span></span>
29. <span data-ttu-id="6be93-147">**Tamam**'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="6be93-147">Click **OK**.</span></span> <span data-ttu-id="6be93-148">Dönem günlüğü artık gözden geçirilebilir, onaylanabilir veya gereklilik ve ayara bağlı olarak deftere nakledilebilir.</span><span class="sxs-lookup"><span data-stu-id="6be93-148">The period journal can now be reviewed, approved or posted depending on requirement and setup.</span></span>   
