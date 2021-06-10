---
title: Yedekleme planı geliştirme
description: Kuruluşunuz büyüdükçe, ardıl planlamasına başlamalısınız.
author: andreabichsel
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: HcmSkillMapping, HcmPersonnelManagementWorkspace
audience: Application User
ms.search.scope: Human Resources
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: dae4292bed986cdc53254162f1af44a75ebdf29d
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/18/2021
ms.locfileid: "6058788"
---
# <a name="develop-a-succession-plan"></a><span data-ttu-id="1f265-103">Yedekleme planı geliştirme</span><span class="sxs-lookup"><span data-stu-id="1f265-103">Develop a succession plan</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="1f265-104">Kuruluşunuz büyüdükçe, ardıl planlamasına başlamalısınız.</span><span class="sxs-lookup"><span data-stu-id="1f265-104">As your organization grows, you must begin succession planning.</span></span> <span data-ttu-id="1f265-105">Ardıl planlaması sırasında, başka bir kişiyle benzer becerilere sahip birini bulmak isteyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="1f265-105">During succession planning, you might want to find someone who has similar skills to another person.</span></span> <span data-ttu-id="1f265-106">Yetenek eşleştirmesi, mevcut çalışanlarınızı ve başvuranlarınızı analiz ederek değerli bir çalışanın becerileriyle eşleşip eşleşmediğini görmenizi sağlar.</span><span class="sxs-lookup"><span data-stu-id="1f265-106">Skill mapping allows you to analyze your existing employees and applicants to see if they match the skill set of a valued employee.</span></span> <span data-ttu-id="1f265-107">Bu yöntemi oluşturmak için kullanılan demo veri şirketi USMF'dir.</span><span class="sxs-lookup"><span data-stu-id="1f265-107">The demo data company used to create this procedure is USMF.</span></span>

1. <span data-ttu-id="1f265-108">**İnsan kaynakları > Uzmanlıklar > Yetenek analizi > Yetenek eşleştirme profilleri**'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="1f265-108">Go to **Human resources > Competencies > Skill analysis > Skill mapping profiles**.</span></span>
2. <span data-ttu-id="1f265-109">**Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="1f265-109">Select **New**.</span></span>
3. <span data-ttu-id="1f265-110">**Yetenek eşleştirmesi** alanına, yetenek eşleştirmeniz için bir ad girin.</span><span class="sxs-lookup"><span data-stu-id="1f265-110">In the **Skill mapping** field, enter a name for your skill mapping.</span></span> <span data-ttu-id="1f265-111">Örnek: Çalışan.</span><span class="sxs-lookup"><span data-stu-id="1f265-111">Example: Employee.</span></span>
4. <span data-ttu-id="1f265-112">**Tanım** alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="1f265-112">In the **Description** field, type a value.</span></span>
5. <span data-ttu-id="1f265-113">**Tarih** alanına bir tarih girin.</span><span class="sxs-lookup"><span data-stu-id="1f265-113">In the **Date** field, enter a date.</span></span>
6. <span data-ttu-id="1f265-114">**Profili getir**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="1f265-114">Select **Retrieve profile**.</span></span>
7. <span data-ttu-id="1f265-115">**Kişi**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="1f265-115">Select **Person**.</span></span>
8. <span data-ttu-id="1f265-116">**Kişi** alanına bir ad yazın veya açılan alanı seçin.</span><span class="sxs-lookup"><span data-stu-id="1f265-116">In the **Person** field, type in a name, or select the drop-down.</span></span>
9. <span data-ttu-id="1f265-117">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="1f265-117">Select **OK**.</span></span>
10. <span data-ttu-id="1f265-118">Yetenek eşleştirmesinde bulunan sertifikaları görüntülemek veya düzenlemek için **Sertifikalar** hızlı sekmesini genişletin.</span><span class="sxs-lookup"><span data-stu-id="1f265-118">Expand the **Certificates** fast tab to view or edit the certificates included in the skill mapping.</span></span>
11. <span data-ttu-id="1f265-119">Dahil edilecek yetenekleri görüntülemek veya düzenlemek için **Yetenekler** hızlı sekmesini genişletin.</span><span class="sxs-lookup"><span data-stu-id="1f265-119">Expand the **Skills** fast tab to view or edit the skills to be included.</span></span>
12. <span data-ttu-id="1f265-120">Listede ilk satırı işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="1f265-120">In the list, mark the first row.</span></span> <span data-ttu-id="1f265-121">Örnek: Muhasebe.</span><span class="sxs-lookup"><span data-stu-id="1f265-121">Example:  Accounting.</span></span>
13. <span data-ttu-id="1f265-122">**İsteğe Bağlı** onay kutusunu seçin.</span><span class="sxs-lookup"><span data-stu-id="1f265-122">Select the **Optional** checkbox.</span></span>
14. <span data-ttu-id="1f265-123">**Önem** alanında bir seçenek belirleyin.</span><span class="sxs-lookup"><span data-stu-id="1f265-123">In the **Importance** field, select an option.</span></span> <span data-ttu-id="1f265-124">Bir yeteneği isteğe bağlı olarak işaretlediğinizde, yeteneğin önem düzeyini seçmelisiniz.</span><span class="sxs-lookup"><span data-stu-id="1f265-124">When you mark a skill as optional, you must select the importance level of the skill.</span></span>  
15. <span data-ttu-id="1f265-125">Listede satır 2'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="1f265-125">In the list, select row 2.</span></span>
16. <span data-ttu-id="1f265-126">**İsteğe Bağlı** onay kutusunu seçin.</span><span class="sxs-lookup"><span data-stu-id="1f265-126">Select the **Optional** checkbox.</span></span>
17. <span data-ttu-id="1f265-127">**Önem** alanında bir seçenek belirleyin.</span><span class="sxs-lookup"><span data-stu-id="1f265-127">In the **Importance** field, select an option.</span></span>
18. <span data-ttu-id="1f265-128">Listede satır 3'ü seçin.</span><span class="sxs-lookup"><span data-stu-id="1f265-128">In the list, select row 3.</span></span>
19. <span data-ttu-id="1f265-129">**İsteğe Bağlı** onay kutusunu seçin.</span><span class="sxs-lookup"><span data-stu-id="1f265-129">Select the **Optional** checkbox.</span></span>
20. <span data-ttu-id="1f265-130">**Önem** alanında bir seçenek belirleyin.</span><span class="sxs-lookup"><span data-stu-id="1f265-130">In the **Importance** field, select an option.</span></span>
21. <span data-ttu-id="1f265-131">Listede satır 4'ü seçin.</span><span class="sxs-lookup"><span data-stu-id="1f265-131">In the list, select row 4.</span></span>
22. <span data-ttu-id="1f265-132">**İsteğe Bağlı** onay kutusunu seçin.</span><span class="sxs-lookup"><span data-stu-id="1f265-132">Select the **Optional** checkbox.</span></span>
23. <span data-ttu-id="1f265-133">Önem alanında bir seçenek seçin.</span><span class="sxs-lookup"><span data-stu-id="1f265-133">In the Importance field, select an option.</span></span>
24. <span data-ttu-id="1f265-134">Yetenek eşleştirmesinde bulunan uzmanlıkları görüntülemek veya düzenlemek için **Eğitim** hızlı sekmesini genişletin.</span><span class="sxs-lookup"><span data-stu-id="1f265-134">Expand the **Education** fast tab to view or edit the education competencies to be included in the skill mapping.</span></span>
25. <span data-ttu-id="1f265-135">**Yürüt**'ü seçin.</span><span class="sxs-lookup"><span data-stu-id="1f265-135">Select **Execute**.</span></span>
26. <span data-ttu-id="1f265-136">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="1f265-136">Select **OK**.</span></span>
27. <span data-ttu-id="1f265-137">**Sonuç**'u seçin.</span><span class="sxs-lookup"><span data-stu-id="1f265-137">Select **Result**.</span></span>
28. <span data-ttu-id="1f265-138">**Rapor**'u seçin.</span><span class="sxs-lookup"><span data-stu-id="1f265-138">Select **Report**.</span></span> <span data-ttu-id="1f265-139">Rapor, raporun en üstünde en iyi eşleşmeleri listeler.</span><span class="sxs-lookup"><span data-stu-id="1f265-139">The report lists the best matches at the top of the report.</span></span> <span data-ttu-id="1f265-140">Listelenen bir fark öğesi görebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="1f265-140">You can see a gap element listed.</span></span> <span data-ttu-id="1f265-141">Fark, yetenek eşleme düzeyi ile kişinin yetenek düzeyi arasındaki farktır.</span><span class="sxs-lookup"><span data-stu-id="1f265-141">A gap is the difference between the skill-mapping level and the person's skill level.</span></span>  



[!INCLUDE[footer-include](../includes/footer-banner.md)]