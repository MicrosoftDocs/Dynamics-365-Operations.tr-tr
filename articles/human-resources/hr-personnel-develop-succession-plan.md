---
title: Yedekleme planı geliştirme
description: Kuruluşunuz büyüdükçe, ardıl planlamasına başlamalısınız.
author: andreabichsel
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: HcmSkillMapping, HcmPersonnelManagementWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 203dbc5463bfcc4249e9ed73802a9a1fc153f260
ms.sourcegitcommit: f8bac7ca2803913fd236adbc3806259a17a110f4
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/06/2021
ms.locfileid: "5130217"
---
# <a name="develop-a-succession-plan"></a><span data-ttu-id="5b083-103">Yedekleme planı geliştirme</span><span class="sxs-lookup"><span data-stu-id="5b083-103">Develop a succession plan</span></span>

<span data-ttu-id="5b083-104">Kuruluşunuz büyüdükçe, ardıl planlamasına başlamalısınız.</span><span class="sxs-lookup"><span data-stu-id="5b083-104">As your organization grows, you must begin succession planning.</span></span> <span data-ttu-id="5b083-105">Ardıl planlaması sırasında, başka bir kişiyle benzer becerilere sahip birini bulmak isteyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="5b083-105">During succession planning, you might want to find someone who has similar skills to another person.</span></span> <span data-ttu-id="5b083-106">Yetenek eşleştirmesi, mevcut çalışanlarınızı ve başvuranlarınızı analiz ederek değerli bir çalışanın becerileriyle eşleşip eşleşmediğini görmenizi sağlar.</span><span class="sxs-lookup"><span data-stu-id="5b083-106">Skill mapping allows you to analyze your existing employees and applicants to see if they match the skill set of a valued employee.</span></span> <span data-ttu-id="5b083-107">Bu yöntemi oluşturmak için kullanılan demo veri şirketi USMF'dir.</span><span class="sxs-lookup"><span data-stu-id="5b083-107">The demo data company used to create this procedure is USMF.</span></span>

1. <span data-ttu-id="5b083-108">**İnsan kaynakları > Uzmanlıklar > Yetenek analizi > Yetenek eşleştirme profilleri**'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="5b083-108">Go to **Human resources > Competencies > Skill analysis > Skill mapping profiles**.</span></span>
2. <span data-ttu-id="5b083-109">**Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="5b083-109">Select **New**.</span></span>
3. <span data-ttu-id="5b083-110">**Yetenek eşleştirmesi** alanına, yetenek eşleştirmeniz için bir ad girin.</span><span class="sxs-lookup"><span data-stu-id="5b083-110">In the **Skill mapping** field, enter a name for your skill mapping.</span></span> <span data-ttu-id="5b083-111">Örnek: Çalışan.</span><span class="sxs-lookup"><span data-stu-id="5b083-111">Example: Employee.</span></span>
4. <span data-ttu-id="5b083-112">**Tanım** alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="5b083-112">In the **Description** field, type a value.</span></span>
5. <span data-ttu-id="5b083-113">**Tarih** alanına bir tarih girin.</span><span class="sxs-lookup"><span data-stu-id="5b083-113">In the **Date** field, enter a date.</span></span>
6. <span data-ttu-id="5b083-114">**Profili getir**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="5b083-114">Select **Retrieve profile**.</span></span>
7. <span data-ttu-id="5b083-115">**Kişi**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="5b083-115">Select **Person**.</span></span>
8. <span data-ttu-id="5b083-116">**Kişi** alanına bir ad yazın veya açılan alanı seçin.</span><span class="sxs-lookup"><span data-stu-id="5b083-116">In the **Person** field, type in a name, or select the drop-down.</span></span>
9. <span data-ttu-id="5b083-117">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="5b083-117">Select **OK**.</span></span>
10. <span data-ttu-id="5b083-118">Yetenek eşleştirmesinde bulunan sertifikaları görüntülemek veya düzenlemek için **Sertifikalar** hızlı sekmesini genişletin.</span><span class="sxs-lookup"><span data-stu-id="5b083-118">Expand the **Certificates** fast tab to view or edit the certificates included in the skill mapping.</span></span>
11. <span data-ttu-id="5b083-119">Dahil edilecek yetenekleri görüntülemek veya düzenlemek için **Yetenekler** hızlı sekmesini genişletin.</span><span class="sxs-lookup"><span data-stu-id="5b083-119">Expand the **Skills** fast tab to view or edit the skills to be included.</span></span>
12. <span data-ttu-id="5b083-120">Listede ilk satırı işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="5b083-120">In the list, mark the first row.</span></span> <span data-ttu-id="5b083-121">Örnek: Muhasebe.</span><span class="sxs-lookup"><span data-stu-id="5b083-121">Example:  Accounting.</span></span>
13. <span data-ttu-id="5b083-122">**İsteğe Bağlı** onay kutusunu seçin.</span><span class="sxs-lookup"><span data-stu-id="5b083-122">Select the **Optional** checkbox.</span></span>
14. <span data-ttu-id="5b083-123">**Önem** alanında bir seçenek belirleyin.</span><span class="sxs-lookup"><span data-stu-id="5b083-123">In the **Importance** field, select an option.</span></span> <span data-ttu-id="5b083-124">Bir yeteneği isteğe bağlı olarak işaretlediğinizde, yeteneğin önem düzeyini seçmelisiniz.</span><span class="sxs-lookup"><span data-stu-id="5b083-124">When you mark a skill as optional, you must select the importance level of the skill.</span></span>  
15. <span data-ttu-id="5b083-125">Listede satır 2'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="5b083-125">In the list, select row 2.</span></span>
16. <span data-ttu-id="5b083-126">**İsteğe Bağlı** onay kutusunu seçin.</span><span class="sxs-lookup"><span data-stu-id="5b083-126">Select the **Optional** checkbox.</span></span>
17. <span data-ttu-id="5b083-127">**Önem** alanında bir seçenek belirleyin.</span><span class="sxs-lookup"><span data-stu-id="5b083-127">In the **Importance** field, select an option.</span></span>
18. <span data-ttu-id="5b083-128">Listede satır 3'ü seçin.</span><span class="sxs-lookup"><span data-stu-id="5b083-128">In the list, select row 3.</span></span>
19. <span data-ttu-id="5b083-129">**İsteğe Bağlı** onay kutusunu seçin.</span><span class="sxs-lookup"><span data-stu-id="5b083-129">Select the **Optional** checkbox.</span></span>
20. <span data-ttu-id="5b083-130">**Önem** alanında bir seçenek belirleyin.</span><span class="sxs-lookup"><span data-stu-id="5b083-130">In the **Importance** field, select an option.</span></span>
21. <span data-ttu-id="5b083-131">Listede satır 4'ü seçin.</span><span class="sxs-lookup"><span data-stu-id="5b083-131">In the list, select row 4.</span></span>
22. <span data-ttu-id="5b083-132">**İsteğe Bağlı** onay kutusunu seçin.</span><span class="sxs-lookup"><span data-stu-id="5b083-132">Select the **Optional** checkbox.</span></span>
23. <span data-ttu-id="5b083-133">Önem alanında bir seçenek seçin.</span><span class="sxs-lookup"><span data-stu-id="5b083-133">In the Importance field, select an option.</span></span>
24. <span data-ttu-id="5b083-134">Yetenek eşleştirmesinde bulunan uzmanlıkları görüntülemek veya düzenlemek için **Eğitim** hızlı sekmesini genişletin.</span><span class="sxs-lookup"><span data-stu-id="5b083-134">Expand the **Education** fast tab to view or edit the education competencies to be included in the skill mapping.</span></span>
25. <span data-ttu-id="5b083-135">**Yürüt**'ü seçin.</span><span class="sxs-lookup"><span data-stu-id="5b083-135">Select **Execute**.</span></span>
26. <span data-ttu-id="5b083-136">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="5b083-136">Select **OK**.</span></span>
27. <span data-ttu-id="5b083-137">**Sonuç**'u seçin.</span><span class="sxs-lookup"><span data-stu-id="5b083-137">Select **Result**.</span></span>
28. <span data-ttu-id="5b083-138">**Rapor**'u seçin.</span><span class="sxs-lookup"><span data-stu-id="5b083-138">Select **Report**.</span></span> <span data-ttu-id="5b083-139">Rapor, raporun en üstünde en iyi eşleşmeleri listeler.</span><span class="sxs-lookup"><span data-stu-id="5b083-139">The report lists the best matches at the top of the report.</span></span> <span data-ttu-id="5b083-140">Listelenen bir fark öğesi görebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="5b083-140">You can see a gap element listed.</span></span> <span data-ttu-id="5b083-141">Fark, yetenek eşleme düzeyi ile kişinin yetenek düzeyi arasındaki farktır.</span><span class="sxs-lookup"><span data-stu-id="5b083-141">A gap is the difference between the skill-mapping level and the person's skill level.</span></span>  

