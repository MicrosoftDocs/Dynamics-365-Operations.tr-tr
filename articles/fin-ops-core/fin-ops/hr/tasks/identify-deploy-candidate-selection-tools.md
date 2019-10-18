---
title: Aday seçim araçlarını tanımlama ve dağıtma
description: Boş konumları doldurmak için kalifiye aday havuzu bulmak, özellikle de konum benzersiz beceri grubu gerektirdiğinde zor olabilir.
author: andreabichsel
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: HcmSkillMapping, HcmJobLookup, HcmSkillMappingLine, HcmPersonCertificate, CCHTMLPrintPreview
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 51200a67a51097c438370866cb9d0ccbebe8392c
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/27/2019
ms.locfileid: "2190385"
---
# <a name="identify-and-deploy-candidate-selection-tools"></a><span data-ttu-id="76051-103">Aday seçim araçlarını tanımlama ve dağıtma</span><span class="sxs-lookup"><span data-stu-id="76051-103">Identify and deploy candidate selection tools</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="76051-104">Boş konumları doldurmak için kalifiye aday havuzu bulmak, özellikle de konum benzersiz beceri grubu gerektirdiğinde zor olabilir.</span><span class="sxs-lookup"><span data-stu-id="76051-104">Finding a qualified pool of candidates to fill vacancies can be difficult, especially when a position requires a unique set of skills.</span></span>  <span data-ttu-id="76051-105">Ancak, gereksinim duyduğunuz becerilere sahip adaylar zaten kuruluşunuzda çalışıyor olabilir.</span><span class="sxs-lookup"><span data-stu-id="76051-105">However, candidates with the skills you need might already be employed in your organization.</span></span> <span data-ttu-id="76051-106">Mevcut çalışanlar veya yeni başvuranlar arasında belirli bir yetenek kümesi arayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="76051-106">You can search for a specific skill set among existing employees, or new applicants.</span></span> <span data-ttu-id="76051-107">Bu, işverene açık bir konum için geçmişte veya yeni başvuru yapanları hızlı şekilde toplama ve eleme ya da mevcut çalışan havuzundan olası adayları bulma olanağı sağlar.</span><span class="sxs-lookup"><span data-stu-id="76051-107">This allows a recruiter to quickly gather and screen applicants who have applied for open position now or in the past, or to find potential candidates from their existing pool of employees.</span></span> <span data-ttu-id="76051-108">Yetenek eşleme işlevinin açık bir konum için doğru kişiyi bulmanıza nasıl yardımcı olacağını öğrenmek üzere bu görev kaydını kullanın.</span><span class="sxs-lookup"><span data-stu-id="76051-108">Use this task recording to learn how the skill mapping functionality can help you find the right person for an open position.</span></span> <span data-ttu-id="76051-109">Bu yöntemi oluşturmak için kullanılan demo veri şirketi USMF'dir.</span><span class="sxs-lookup"><span data-stu-id="76051-109">The demo data company used to create this procedure is USMF.</span></span>

1. <span data-ttu-id="76051-110">İnsan Kaynakları > Yetkinlikler > Yetenek analizi > Yetenek eşleme profilleri'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="76051-110">Go to Human resources > Competencies > Skill analysis > Skill mapping profiles.</span></span>
2. <span data-ttu-id="76051-111">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="76051-111">Click New.</span></span>
3. <span data-ttu-id="76051-112">Yetenek eşleme alanına, yetenek eşleme için bir ad girin.</span><span class="sxs-lookup"><span data-stu-id="76051-112">In the Skill mapping field, enter a name for your skill mapping.</span></span>  <span data-ttu-id="76051-113">Örnek: Muhasebeci.</span><span class="sxs-lookup"><span data-stu-id="76051-113">Example: Accountant.</span></span>
4. <span data-ttu-id="76051-114">Açıklama alanına, yetenek eşleme açıklamasını girin.</span><span class="sxs-lookup"><span data-stu-id="76051-114">In the Description field, enter a description of the skill mapping..</span></span>
5. <span data-ttu-id="76051-115">Tarih alanına bir tarih girin.</span><span class="sxs-lookup"><span data-stu-id="76051-115">In the Date field, enter a date.</span></span>
6. <span data-ttu-id="76051-116">Profili al'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="76051-116">Click Retrieve profile.</span></span>
    * <span data-ttu-id="76051-117">Aramanın temeli olarak seçilen Kişi, İş veya Kurstan Sertifika, Beceri ve Eğitim verilerini almak için Alma profilini kullanın.</span><span class="sxs-lookup"><span data-stu-id="76051-117">Use Retrieve profile to pull in the Certificate, Skill, and Education data from a selected Person, Job or Course as the basis for your search.</span></span>   <span data-ttu-id="76051-118">Ardından ölçüt ekleyip kaldırabilir, ölçütün isteğe bağlı olup olmadığını belirtebilir ve ölçütün önemini derecelendirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="76051-118">You can then add or remove criteria, state if the criteria is optional and rank the importance of the criteria.</span></span>  
7. <span data-ttu-id="76051-119">İş'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="76051-119">Click Job.</span></span>
8. <span data-ttu-id="76051-120">İş alanına bir değer girin veya buradan bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="76051-120">In the Job field, enter or select a value.</span></span>
9. <span data-ttu-id="76051-121">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="76051-121">Click OK.</span></span>
10. <span data-ttu-id="76051-122">Aralık hızlı sekmesini genişletin ve departman gibi ek bilgileri ekleyin.</span><span class="sxs-lookup"><span data-stu-id="76051-122">Expand the range fast tab, and add any additional information, such as department.</span></span>
11. <span data-ttu-id="76051-123">Sertifikaları görmek veya düzenlemek için sertifikalar hızlı sekmesini genişletin.</span><span class="sxs-lookup"><span data-stu-id="76051-123">Expand the certificates fast tab to view or edit the certificates.</span></span>
12. <span data-ttu-id="76051-124">Yetenekleri görmek veya düzenlemek için Yetenekler hızlı sekmesini genişletin.</span><span class="sxs-lookup"><span data-stu-id="76051-124">Expand the Skills fast tab to view or edit the skills.</span></span>
13. <span data-ttu-id="76051-125">Eğitim ölçütünü görmek veya düzenlemek için Eğitim hızlı sekmesini genişletin.</span><span class="sxs-lookup"><span data-stu-id="76051-125">Expand the Education fast tab to view or edit the education criteria.</span></span>
14. <span data-ttu-id="76051-126">Yürüt'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="76051-126">Click Execute.</span></span>
15. <span data-ttu-id="76051-127">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="76051-127">Click OK.</span></span>
16. <span data-ttu-id="76051-128">Sonuçlar'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="76051-128">Click Result.</span></span>
17. <span data-ttu-id="76051-129">Sonuçlar'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="76051-129">Click Result.</span></span>
18. <span data-ttu-id="76051-130">Devam'ı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="76051-130">Click Resume.</span></span>
19. <span data-ttu-id="76051-131">Sertifikalar'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="76051-131">Click Certificates.</span></span>
    * <span data-ttu-id="76051-132">Listelenen her kişi için ayrıntılara inebilir ve eğitim, beceriler, mesleki deneyim vb. ile ilgili ayrıntıları görebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="76051-132">You can drill further into each person listed and see details regarding their education, skills, professional experience etc.</span></span>  
20. <span data-ttu-id="76051-133">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="76051-133">Close the page.</span></span>
21. <span data-ttu-id="76051-134">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="76051-134">Close the page.</span></span>
22. <span data-ttu-id="76051-135">Sonucu yeniden seçin.</span><span class="sxs-lookup"><span data-stu-id="76051-135">Select result again.</span></span>
23. <span data-ttu-id="76051-136">Rapor'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="76051-136">Click Report.</span></span>
    * <span data-ttu-id="76051-137">Rapor, en iyi eşleşmeleri raporun üst kısmında listeler.</span><span class="sxs-lookup"><span data-stu-id="76051-137">The report will list the best matches at the top of the report.</span></span>  <span data-ttu-id="76051-138">Listede bir boşluk öğesi olduğunu görebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="76051-138">You can see that there is a gap element listed.</span></span>  <span data-ttu-id="76051-139">Bu, beceri eşlemede listelenen düzey ile kişiye atanan beceri düzeyi arasındaki farktır.</span><span class="sxs-lookup"><span data-stu-id="76051-139">This is the difference between the level that was listed on the skill mapping, and the level of the skill that is assigned to the person.</span></span>  
24. <span data-ttu-id="76051-140">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="76051-140">Close the page.</span></span>
25. <span data-ttu-id="76051-141">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="76051-141">Click Save.</span></span>

