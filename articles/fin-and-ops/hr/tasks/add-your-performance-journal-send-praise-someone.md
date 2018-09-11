--- 
title: "Performans günlüğüne ekleme ve birine övgü gönderme"
description: "Performans günlüğü hedeflerinizi nasıl gerçekleştirdiğinizle veya bir dönem içinde nasıl performans gösterdiğinizle ilgili bilgileri içerir."
author: ShielaSogge
manager: AnnBe
ms.date: 8/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: EssWorkspace, HcmPerfJournal, HcmPerfJournalAddLink, HcmPerfPraise, HcmWorkerLookUpByPerson, HcmPerfJournalAdd
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shielas
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 32d71167fdad65cb1dec37671999a497759ca484
ms.openlocfilehash: a4595a259ecaa3cd8fea559b6f68d7f53af5f843
ms.contentlocale: tr-tr
ms.lasthandoff: 09/11/2018

---
# <a name="add-to-your-performance-journal-and-send-praise-to-someone"></a><span data-ttu-id="a90b2-103">Performans günlüğüne ekleme ve birine övgü gönderme</span><span class="sxs-lookup"><span data-stu-id="a90b2-103">Add to your performance journal and send praise to someone</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="a90b2-104">Performans günlüğü hedeflerinizi nasıl gerçekleştirdiğinizle veya bir dönem içinde nasıl performans gösterdiğinizle ilgili bilgileri içerir.</span><span class="sxs-lookup"><span data-stu-id="a90b2-104">The performance journal holds information that relates to how you met your goals or how you performed during a period.</span></span> <span data-ttu-id="a90b2-105">Günlükten ayrıca bir çalışma arkadaşınızın faaliyetlerini de övebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="a90b2-105">You can also praise the actions of a co-worker from the journal.</span></span> <span data-ttu-id="a90b2-106">Bu yöntemi oluşturmak için kullanılan demo veri şirketi USMF'dir.</span><span class="sxs-lookup"><span data-stu-id="a90b2-106">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="a90b2-107">Bu yordam, Dynamics 365 for Operations sürüm 1611'e eklenen bir özellik içindir.</span><span class="sxs-lookup"><span data-stu-id="a90b2-107">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>

1. <span data-ttu-id="a90b2-108">Tüm çalışma alanları > Personel self servisi öğesine gidin.</span><span class="sxs-lookup"><span data-stu-id="a90b2-108">Go to All workspaces > Employee self service.</span></span>
2. <span data-ttu-id="a90b2-109">Performans günlüğü'ne tıklayın.</span><span class="sxs-lookup"><span data-stu-id="a90b2-109">Click Performance journal.</span></span>
3. <span data-ttu-id="a90b2-110">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="a90b2-110">Click New.</span></span>
4. <span data-ttu-id="a90b2-111">Başlık alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="a90b2-111">In the Title field, type a value.</span></span>
5. <span data-ttu-id="a90b2-112">Açıklama alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="a90b2-112">In the Description field, type a value.</span></span>
    * <span data-ttu-id="a90b2-113">Performans günlüğü tarihi, günlüğün oluşturulduğu tarihtir.</span><span class="sxs-lookup"><span data-stu-id="a90b2-113">The performance journal date is the date that the journal was created.</span></span>  
    * <span data-ttu-id="a90b2-114">Kaynak, performans günlüğünün geldiği yeri temsil eder.</span><span class="sxs-lookup"><span data-stu-id="a90b2-114">The source represents where the performance journal came from.</span></span> <span data-ttu-id="a90b2-115">Siz bir tane oluşturduğunuzda, Günlüğüm'den gelir.</span><span class="sxs-lookup"><span data-stu-id="a90b2-115">When you create one, it comes from My journal.</span></span> <span data-ttu-id="a90b2-116">Yöneticiniz bir tane oluşturursa Yöneticisi günlüğünden gelir.</span><span class="sxs-lookup"><span data-stu-id="a90b2-116">If your manager creates one, it comes from the Manager journal.</span></span>  
    * <span data-ttu-id="a90b2-117">Bu günlüğü yöneticiniz ile paylaşabilir veya yalnızca kendiniz için görünür yapabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="a90b2-117">You can share this journal with your manager or make it only visible to you.</span></span>  
6. <span data-ttu-id="a90b2-118">Başlangıç tarihi alanına bir tarih girin.</span><span class="sxs-lookup"><span data-stu-id="a90b2-118">In the Start date field, enter a date.</span></span>
7. <span data-ttu-id="a90b2-119">Tamamlanma tarihi alanına bir tarih girin.</span><span class="sxs-lookup"><span data-stu-id="a90b2-119">In the Date completed field, enter a date.</span></span>
8. <span data-ttu-id="a90b2-120">Geliştirme planı alanında Evet'i seçin.</span><span class="sxs-lookup"><span data-stu-id="a90b2-120">Select Yes in the Development plan field.</span></span>
9. <span data-ttu-id="a90b2-121">Anahtar sözcükler alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="a90b2-121">In the Keywords field, type a value.</span></span>
10. <span data-ttu-id="a90b2-122">Harici bağlantı ekle'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="a90b2-122">Click Add external link.</span></span>
11. <span data-ttu-id="a90b2-123">Açıklama alanına "Envision" yazın.</span><span class="sxs-lookup"><span data-stu-id="a90b2-123">In the Description field, type 'Envision'.</span></span>
12. <span data-ttu-id="a90b2-124">Internet adresi alanına "https://www.microsoft.com/tr/envision/default" yazın.</span><span class="sxs-lookup"><span data-stu-id="a90b2-124">In the Internet address field, type 'https://www.microsoft.com/en/envision/default'.</span></span>
13. <span data-ttu-id="a90b2-125">Kılavuza dönmek için Kaydet düğmesinin altındaki "Performans günlüğü" başlığına tıklayın.</span><span class="sxs-lookup"><span data-stu-id="a90b2-125">Click on the caption below the Save button called "Performance journal" to return to the grid.</span></span>
    * <span data-ttu-id="a90b2-126">Seçilen günlük veya günlükleri bir hedefe ekleyebilirsiniz, böylece hedefi açtığınızda görünür.</span><span class="sxs-lookup"><span data-stu-id="a90b2-126">You can add the selected journal or journals to a goal so that it appears when you open the goal.</span></span> <span data-ttu-id="a90b2-127">Bağlantılar hızı sekmesine bir bağlantı eklenir.    Bir hedefe bir günlük eklerseniz ve ardından hedefi bir gözden geçirmeye eklerseniz günlük otomatik olarak gözden geçirmede görünür.</span><span class="sxs-lookup"><span data-stu-id="a90b2-127">A link will be added in the Links fast tab.    If you add a journal to a goal and then add the goal to a review, the journal will appear on the review automatically.</span></span>  
    * <span data-ttu-id="a90b2-128">Seçilen günlük veya günlükleri bir gözden geçirmeye ekleyebilirsiniz, böylece gözden geçirmeyi açtığınızda görünür.</span><span class="sxs-lookup"><span data-stu-id="a90b2-128">You can add the selected journal or journals to a review so that it appears when you open the review.</span></span>    <span data-ttu-id="a90b2-129">Bağlantılar hızı sekmesine bir bağlantı eklenir.</span><span class="sxs-lookup"><span data-stu-id="a90b2-129">A link will be added in the Links fast tab.</span></span>  
14. <span data-ttu-id="a90b2-130">Hızlı ekle'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="a90b2-130">Click Quick add.</span></span>
15. <span data-ttu-id="a90b2-131">Başlık alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="a90b2-131">In the Title field, type a value.</span></span>
16. <span data-ttu-id="a90b2-132">Açıklama alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="a90b2-132">In the Description field, type a value.</span></span>
17. <span data-ttu-id="a90b2-133">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="a90b2-133">Click Save.</span></span>
18. <span data-ttu-id="a90b2-134">Övgü gönder'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="a90b2-134">Click Send praise.</span></span>
19. <span data-ttu-id="a90b2-135">Şirketteki personel listesinden bir kişi seçin.</span><span class="sxs-lookup"><span data-stu-id="a90b2-135">Select a person from the list of employees in the company.</span></span>
20. <span data-ttu-id="a90b2-136">Açıklama alanına, "Konferanstaki yardımların için teşekkürler!" girin.</span><span class="sxs-lookup"><span data-stu-id="a90b2-136">In the Description field, enter 'Thanks for all the help at the conference!'.</span></span>
21. <span data-ttu-id="a90b2-137">Gönder'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="a90b2-137">Click Send.</span></span>


