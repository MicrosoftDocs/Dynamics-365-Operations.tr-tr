---
title: Aday seçim araçlarını tanımlama ve dağıtma
description: Boş konumları doldurmak için kalifiye aday havuzu bulmak, özellikle de konum benzersiz beceri grubu gerektirdiğinde zor olabilir.
author: andreabichsel
ms.date: 11/20/2020
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: HcmSkillMapping, HcmJobLookup, HcmSkillMappingLine, HcmPersonCertificate, CCHTMLPrintPreview
audience: Application User
ms.reviewer: anbichse
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a9e0b300692d817024455c669c226a81e601366e
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/31/2021
ms.locfileid: "5751922"
---
# <a name="identify-and-deploy-candidate-selection-tools"></a><span data-ttu-id="303d9-103">Aday seçim araçlarını tanımlama ve dağıtma</span><span class="sxs-lookup"><span data-stu-id="303d9-103">Identify and deploy candidate selection tools</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="303d9-104">Boş konumları doldurmak için kalifiye aday havuzu bulmak, özellikle de konum benzersiz beceri grubu gerektirdiğinde zor olabilir.</span><span class="sxs-lookup"><span data-stu-id="303d9-104">Finding a qualified pool of candidates to fill vacancies can be difficult, especially when a position requires a unique set of skills.</span></span>  <span data-ttu-id="303d9-105">Ancak, gereksinim duyduğunuz becerilere sahip adaylar zaten kuruluşunuzda çalışıyor olabilir.</span><span class="sxs-lookup"><span data-stu-id="303d9-105">However, candidates with the skills you need might already be employed in your organization.</span></span> <span data-ttu-id="303d9-106">Mevcut çalışanlar veya yeni başvuranlar arasında belirli bir yetenek kümesi arayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="303d9-106">You can search for a specific skill set among existing employees, or new applicants.</span></span> <span data-ttu-id="303d9-107">Bu, işverene açık bir konum için geçmişte veya yeni başvuru yapanları hızlı şekilde toplama ve eleme ya da mevcut çalışan havuzundan olası adayları bulma olanağı sağlar.</span><span class="sxs-lookup"><span data-stu-id="303d9-107">This allows a recruiter to quickly gather and screen applicants who have applied for open position now or in the past, or to find potential candidates from their existing pool of employees.</span></span> <span data-ttu-id="303d9-108">Yetenek eşleme işlevinin açık bir konum için doğru kişiyi bulmanıza nasıl yardımcı olacağını öğrenmek üzere bu görev kaydını kullanın.</span><span class="sxs-lookup"><span data-stu-id="303d9-108">Use this task recording to learn how the skill mapping functionality can help you find the right person for an open position.</span></span> <span data-ttu-id="303d9-109">Bu yöntemi oluşturmak için kullanılan demo veri şirketi USMF'dir.</span><span class="sxs-lookup"><span data-stu-id="303d9-109">The demo data company used to create this procedure is USMF.</span></span>

1. <span data-ttu-id="303d9-110">İnsan Kaynakları > Yetkinlikler > Yetenek analizi > Yetenek eşleme profilleri'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="303d9-110">Go to Human resources > Competencies > Skill analysis > Skill mapping profiles.</span></span>
2. <span data-ttu-id="303d9-111">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="303d9-111">Click New.</span></span>
3. <span data-ttu-id="303d9-112">Yetenek eşleme alanına, yetenek eşleme için bir ad girin.</span><span class="sxs-lookup"><span data-stu-id="303d9-112">In the Skill mapping field, enter a name for your skill mapping.</span></span>  <span data-ttu-id="303d9-113">Örnek: Muhasebeci.</span><span class="sxs-lookup"><span data-stu-id="303d9-113">Example: Accountant.</span></span>
4. <span data-ttu-id="303d9-114">Açıklama alanına, yetenek eşleme açıklamasını girin.</span><span class="sxs-lookup"><span data-stu-id="303d9-114">In the Description field, enter a description of the skill mapping..</span></span>
5. <span data-ttu-id="303d9-115">Tarih alanına bir tarih girin.</span><span class="sxs-lookup"><span data-stu-id="303d9-115">In the Date field, enter a date.</span></span>
6. <span data-ttu-id="303d9-116">Profili al'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="303d9-116">Click Retrieve profile.</span></span>
    * <span data-ttu-id="303d9-117">Aramanın temeli olarak seçilen Kişi, İş veya Kurstan Sertifika, Beceri ve Eğitim verilerini almak için Alma profilini kullanın.</span><span class="sxs-lookup"><span data-stu-id="303d9-117">Use Retrieve profile to pull in the Certificate, Skill, and Education data from a selected Person, Job or Course as the basis for your search.</span></span>   <span data-ttu-id="303d9-118">Ardından ölçüt ekleyip kaldırabilir, ölçütün isteğe bağlı olup olmadığını belirtebilir ve ölçütün önemini derecelendirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="303d9-118">You can then add or remove criteria, state if the criteria is optional and rank the importance of the criteria.</span></span>  
7. <span data-ttu-id="303d9-119">İş'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="303d9-119">Click Job.</span></span>
8. <span data-ttu-id="303d9-120">İş alanına bir değer girin veya buradan bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="303d9-120">In the Job field, enter or select a value.</span></span>
9. <span data-ttu-id="303d9-121">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="303d9-121">Click OK.</span></span>
10. <span data-ttu-id="303d9-122">Aralık hızlı sekmesini genişletin ve departman gibi ek bilgileri ekleyin.</span><span class="sxs-lookup"><span data-stu-id="303d9-122">Expand the Range FastTab, and add any additional information, such as department.</span></span>
11. <span data-ttu-id="303d9-123">Sertifikaları görmek veya düzenlemek için Sertifikalar hızlı sekmesini genişletin.</span><span class="sxs-lookup"><span data-stu-id="303d9-123">Expand the Certificates FastTab to view or edit the certificates.</span></span>
12. <span data-ttu-id="303d9-124">Becerileri görmek veya düzenlemek için Beceriler hızlı sekmesini genişletin.</span><span class="sxs-lookup"><span data-stu-id="303d9-124">Expand the Skills FastTab to view or edit the skills.</span></span>
13. <span data-ttu-id="303d9-125">Eğitim ölçütünü görmek veya düzenlemek için Eğitim hızlı sekmesini genişletin.</span><span class="sxs-lookup"><span data-stu-id="303d9-125">Expand the Education FastTab to view or edit the education criteria.</span></span>
14. <span data-ttu-id="303d9-126">Yürüt'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="303d9-126">Click Execute.</span></span>
15. <span data-ttu-id="303d9-127">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="303d9-127">Click OK.</span></span>
16. <span data-ttu-id="303d9-128">Sonuçlar'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="303d9-128">Click Result.</span></span>
17. <span data-ttu-id="303d9-129">Sonuçlar'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="303d9-129">Click Result.</span></span>
18. <span data-ttu-id="303d9-130">Devam'ı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="303d9-130">Click Resume.</span></span>
19. <span data-ttu-id="303d9-131">Sertifikalar'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="303d9-131">Click Certificates.</span></span>
    * <span data-ttu-id="303d9-132">Listelenen her kişi için ayrıntılara inebilir ve eğitim, beceriler ve mesleki deneyim ile ilgili ayrıntıları görebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="303d9-132">You can drill further into each person listed and see details regarding their education, skills, and professional experience.</span></span>  
20. <span data-ttu-id="303d9-133">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="303d9-133">Close the page.</span></span>
21. <span data-ttu-id="303d9-134">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="303d9-134">Close the page.</span></span>
22. <span data-ttu-id="303d9-135">Sonucu yeniden seçin.</span><span class="sxs-lookup"><span data-stu-id="303d9-135">Select result again.</span></span>
23. <span data-ttu-id="303d9-136">Rapor'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="303d9-136">Click Report.</span></span>
    * <span data-ttu-id="303d9-137">Rapor, en iyi eşleşmeleri raporun üst kısmında listeler.</span><span class="sxs-lookup"><span data-stu-id="303d9-137">The report will list the best matches at the top of the report.</span></span>  <span data-ttu-id="303d9-138">Bir boşluk öğesinin listelendiğini görebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="303d9-138">You can see that a gap element is listed.</span></span>  <span data-ttu-id="303d9-139">Bu, beceri eşlemede listelenen düzey ile kişiye atanan beceri düzeyi arasındaki farktır.</span><span class="sxs-lookup"><span data-stu-id="303d9-139">This is the difference between the level that was listed on the skill mapping, and the level of the skill that is assigned to the person.</span></span>  
24. <span data-ttu-id="303d9-140">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="303d9-140">Close the page.</span></span>
25. <span data-ttu-id="303d9-141">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="303d9-141">Click Save.</span></span>



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]