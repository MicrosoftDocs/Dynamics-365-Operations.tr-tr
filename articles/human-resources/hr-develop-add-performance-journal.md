---
title: Performans günlüğüne ekleme ve birine övgü gönderme
description: Performans günlüğü hedeflerinizi nasıl gerçekleştirdiğinizle veya bir dönem içinde nasıl performans gösterdiğinizle ilgili bilgileri içerir.
author: andreabichsel
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: EssWorkspace, HcmPerfJournal, HcmPerfJournalAddLink, HcmPerfPraise, HcmWorkerLookUpByPerson, HcmPerfJournalAdd, HcmEmployeeDevelopmentWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 94df675b02054d7a4761ea5b6edf24c6207e8fc9
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/31/2021
ms.locfileid: "5805574"
---
# <a name="add-to-your-performance-journal-and-send-praise-to-someone"></a><span data-ttu-id="d6e28-103">Performans günlüğüne ekleme ve birine övgü gönderme</span><span class="sxs-lookup"><span data-stu-id="d6e28-103">Add to your performance journal and send praise to someone</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="d6e28-104">Performans günlüğü hedeflerinizi nasıl gerçekleştirdiğinizle veya bir dönem içinde nasıl performans gösterdiğinizle ilgili bilgileri içerir.</span><span class="sxs-lookup"><span data-stu-id="d6e28-104">The performance journal holds information that relates to how you met your goals or how you performed during a period.</span></span> <span data-ttu-id="d6e28-105">Günlükten ayrıca bir çalışma arkadaşınızın faaliyetlerini de övebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="d6e28-105">You can also praise the actions of a co-worker from the journal.</span></span> <span data-ttu-id="d6e28-106">Bu yöntemi oluşturmak için kullanılan demo veri şirketi USMF'dir.</span><span class="sxs-lookup"><span data-stu-id="d6e28-106">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="d6e28-107">Bu yordam, Dynamics 365 for Operations sürüm 1611'e eklenen bir özellik içindir.</span><span class="sxs-lookup"><span data-stu-id="d6e28-107">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>

1. <span data-ttu-id="d6e28-108">Tüm çalışma alanları > Personel self servisi öğesine gidin.</span><span class="sxs-lookup"><span data-stu-id="d6e28-108">Go to All workspaces > Employee self service.</span></span>
2. <span data-ttu-id="d6e28-109">Performans günlüğü'ne tıklayın.</span><span class="sxs-lookup"><span data-stu-id="d6e28-109">Click Performance journal.</span></span>
3. <span data-ttu-id="d6e28-110">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="d6e28-110">Click New.</span></span>
4. <span data-ttu-id="d6e28-111">Başlık alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="d6e28-111">In the Title field, type a value.</span></span>
5. <span data-ttu-id="d6e28-112">Açıklama alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="d6e28-112">In the Description field, type a value.</span></span>
    * <span data-ttu-id="d6e28-113">Performans günlüğü tarihi, günlüğün oluşturulduğu tarihtir.</span><span class="sxs-lookup"><span data-stu-id="d6e28-113">The performance journal date is the date that the journal was created.</span></span>  
    * <span data-ttu-id="d6e28-114">Kaynak, performans günlüğünün geldiği yeri temsil eder.</span><span class="sxs-lookup"><span data-stu-id="d6e28-114">The source represents where the performance journal came from.</span></span> <span data-ttu-id="d6e28-115">Siz bir tane oluşturduğunuzda, Günlüğüm'den gelir.</span><span class="sxs-lookup"><span data-stu-id="d6e28-115">When you create one, it comes from My journal.</span></span> <span data-ttu-id="d6e28-116">Yöneticiniz bir tane oluşturursa Yöneticisi günlüğünden gelir.</span><span class="sxs-lookup"><span data-stu-id="d6e28-116">If your manager creates one, it comes from the Manager journal.</span></span>  
    * <span data-ttu-id="d6e28-117">Bu günlüğü yöneticiniz ile paylaşabilir veya yalnızca kendiniz için görünür yapabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="d6e28-117">You can share this journal with your manager or make it only visible to you.</span></span>  
6. <span data-ttu-id="d6e28-118">Başlangıç tarihi alanına bir tarih girin.</span><span class="sxs-lookup"><span data-stu-id="d6e28-118">In the Start date field, enter a date.</span></span>
7. <span data-ttu-id="d6e28-119">Tamamlanma tarihi alanına bir tarih girin.</span><span class="sxs-lookup"><span data-stu-id="d6e28-119">In the Date completed field, enter a date.</span></span>
8. <span data-ttu-id="d6e28-120">Geliştirme planı alanında Evet'i seçin.</span><span class="sxs-lookup"><span data-stu-id="d6e28-120">Select Yes in the Development plan field.</span></span>
9. <span data-ttu-id="d6e28-121">Anahtar sözcükler alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="d6e28-121">In the Keywords field, type a value.</span></span>
10. <span data-ttu-id="d6e28-122">Harici bağlantı ekle'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="d6e28-122">Click Add external link.</span></span>
11. <span data-ttu-id="d6e28-123">Açıklama alanına "Envision" yazın.</span><span class="sxs-lookup"><span data-stu-id="d6e28-123">In the Description field, type 'Envision'.</span></span>
12. <span data-ttu-id="d6e28-124">İnternet adresi alanına 'https://www.microsoft.com/en/envision/default' yazın.</span><span class="sxs-lookup"><span data-stu-id="d6e28-124">In the Internet address field, type 'https://www.microsoft.com/en/envision/default'.</span></span>
13. <span data-ttu-id="d6e28-125">Kılavuza dönmek için Kaydet düğmesinin altındaki "Performans günlüğü" başlığına tıklayın.</span><span class="sxs-lookup"><span data-stu-id="d6e28-125">Click on the caption below the Save button called "Performance journal" to return to the grid.</span></span>
    * <span data-ttu-id="d6e28-126">Seçilen günlük veya günlükleri bir hedefe ekleyebilirsiniz, böylece hedefi açtığınızda görünür.</span><span class="sxs-lookup"><span data-stu-id="d6e28-126">You can add the selected journal or journals to a goal so that it appears when you open the goal.</span></span> <span data-ttu-id="d6e28-127">Bağlantılar hızı sekmesine bir bağlantı eklenir.    Bir hedefe bir günlük eklerseniz ve ardından hedefi bir gözden geçirmeye eklerseniz günlük otomatik olarak gözden geçirmede görünür.</span><span class="sxs-lookup"><span data-stu-id="d6e28-127">A link will be added in the Links fast tab.    If you add a journal to a goal and then add the goal to a review, the journal will appear on the review automatically.</span></span>  
    * <span data-ttu-id="d6e28-128">Seçilen günlük veya günlükleri bir gözden geçirmeye ekleyebilirsiniz, böylece gözden geçirmeyi açtığınızda görünür.</span><span class="sxs-lookup"><span data-stu-id="d6e28-128">You can add the selected journal or journals to a review so that it appears when you open the review.</span></span>    <span data-ttu-id="d6e28-129">Bağlantılar hızı sekmesine bir bağlantı eklenir.</span><span class="sxs-lookup"><span data-stu-id="d6e28-129">A link will be added in the Links fast tab.</span></span>  
14. <span data-ttu-id="d6e28-130">Hızlı ekle'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="d6e28-130">Click Quick add.</span></span>
15. <span data-ttu-id="d6e28-131">Başlık alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="d6e28-131">In the Title field, type a value.</span></span>
16. <span data-ttu-id="d6e28-132">Açıklama alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="d6e28-132">In the Description field, type a value.</span></span>
17. <span data-ttu-id="d6e28-133">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="d6e28-133">Click Save.</span></span>
18. <span data-ttu-id="d6e28-134">Övgü gönder'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="d6e28-134">Click Send praise.</span></span>
19. <span data-ttu-id="d6e28-135">Şirketteki personel listesinden bir kişi seçin.</span><span class="sxs-lookup"><span data-stu-id="d6e28-135">Select a person from the list of employees in the company.</span></span>
20. <span data-ttu-id="d6e28-136">Açıklama alanına, "Konferanstaki yardımların için teşekkürler!" girin.</span><span class="sxs-lookup"><span data-stu-id="d6e28-136">In the Description field, enter 'Thanks for all the help at the conference!'.</span></span>
21. <span data-ttu-id="d6e28-137">Gönder'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="d6e28-137">Click Send.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]