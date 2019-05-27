---
title: İş talebi geliştir ve yönet
description: İşe alma projeleri, işe alma işleminin yönetilmesine yardımcı olur.
author: andreabichsel
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: HRMRecruitingTable, HcmWorkerLookUp, HcmJobLookup, HRMRecruitingMedia, HRMRecruitingJobAd
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 556f99d34521cce70efb64c5fbababd815e8429d
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/07/2019
ms.locfileid: "1507745"
---
# <a name="develop-and-open-job-requisition"></a><span data-ttu-id="ce084-103">İş talebi geliştir ve yönet</span><span class="sxs-lookup"><span data-stu-id="ce084-103">Develop and open job requisition</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="ce084-104">İşe alma projeleri, işe alma işleminin yönetilmesine yardımcı olur.</span><span class="sxs-lookup"><span data-stu-id="ce084-104">Recruitment projects help manage the recruiting process.</span></span> <span data-ttu-id="ce084-105">Her işe alma projesi için işe alınacak iş, işe alanın adı, projenin durumu ve işin bulunduğu departman gibi bilgileri ayarlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="ce084-105">For each recruitment project, you can set up information, such as the job that recruiting is for, the name of the recruiter, the status of the project and the department that the job will be located in.</span></span> <span data-ttu-id="ce084-106">İşe alma projesini oluşturduktan sonra proje için bir iş ilanını yazabilir, ilanı Çalışan self-servis sayfalarında yayımlayabilir, başvuruları projeyle ilişkilendirebilir ve bu projeyle ilgili etkinlikleri izleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="ce084-106">After creating a recruitment project, you can write a job advertisement for the project, publish the ad on Employee self-service pages, associate applications for employment with the project, and track activities for that project.</span></span> <span data-ttu-id="ce084-107">Bu yöntemi oluşturmak için kullanılan demo veri şirketi USMF'dir.</span><span class="sxs-lookup"><span data-stu-id="ce084-107">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="ce084-108">Yordamı başlatmak için İnsan kaynakları > İşe alma > İşe alma projeleri > İşe alma projeleri'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="ce084-108">To begin the procedure, go to Human resources > Recruitment > Recruitment projects > Recruitment projects</span></span>

1. <span data-ttu-id="ce084-109">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ce084-109">Click New.</span></span>
2. <span data-ttu-id="ce084-110">İşe alma projesi alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="ce084-110">In the Recruitment project field, type a value.</span></span>
3. <span data-ttu-id="ce084-111">Açıklama alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="ce084-111">In the Description field, type a value.</span></span>
4. <span data-ttu-id="ce084-112">İşe alan alanında, aramayı açmak için açılır menü düğmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ce084-112">In the Recruiter field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="ce084-113">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="ce084-113">In the list, find and select the desired record.</span></span>
6. <span data-ttu-id="ce084-114">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ce084-114">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="ce084-115">Seç'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ce084-115">Click Select.</span></span>
8. <span data-ttu-id="ce084-116">Departman alanında, aramayı açmak için açılır menü düğmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ce084-116">In the Department field, click the drop-down button to open the lookup.</span></span>
9. <span data-ttu-id="ce084-117">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ce084-117">In the list, click the link in the selected row.</span></span>
10. <span data-ttu-id="ce084-118">İş alanında, aramayı açmak için açılır menü düğmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ce084-118">In the Job field, click the drop-down button to open the lookup.</span></span>
11. <span data-ttu-id="ce084-119">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="ce084-119">In the list, find and select the desired record.</span></span>
12. <span data-ttu-id="ce084-120">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ce084-120">In the list, click the link in the selected row.</span></span>
13. <span data-ttu-id="ce084-121">Açık konum sayısı alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="ce084-121">In the Number of openings field, enter a number.</span></span>
14. <span data-ttu-id="ce084-122">İşe alma müdürü alanında, aramayı açmak için açılır menü düğmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ce084-122">In the Hiring manager field, click the drop-down button to open the lookup.</span></span>
15. <span data-ttu-id="ce084-123">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="ce084-123">In the list, find and select the desired record.</span></span>
16. <span data-ttu-id="ce084-124">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ce084-124">In the list, click the link in the selected row.</span></span>
17. <span data-ttu-id="ce084-125">Seç'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ce084-125">Click Select.</span></span>
18. <span data-ttu-id="ce084-126">Başvuru bitiş tarihi alanına bir tarih girin.</span><span class="sxs-lookup"><span data-stu-id="ce084-126">In the Application deadline field, enter a date.</span></span>
19. <span data-ttu-id="ce084-127">Ortam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ce084-127">Click Media.</span></span>
    * <span data-ttu-id="ce084-128">İşe alma projeleri, açık pozisyonları tanıtmak için kullanılacak medya birimlerini belirleme seçeneği içerir.</span><span class="sxs-lookup"><span data-stu-id="ce084-128">Recruitment projects include the option to specify media outlets to use to advertise open positions.</span></span>  
20. <span data-ttu-id="ce084-129">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ce084-129">Click New.</span></span>
21. <span data-ttu-id="ce084-130">Ortam alanında, aramayı açmak için açılır menü düğmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ce084-130">In the Media field, click the drop-down button to open the lookup.</span></span>
22. <span data-ttu-id="ce084-131">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ce084-131">In the list, click the link in the selected row.</span></span>
23. <span data-ttu-id="ce084-132">Başlangıç tarihi alanına bir tarih girin.</span><span class="sxs-lookup"><span data-stu-id="ce084-132">In the Start date field, enter a date.</span></span>
24. <span data-ttu-id="ce084-133">Bitiş tarihi alanına bir tarih girin.</span><span class="sxs-lookup"><span data-stu-id="ce084-133">In the End date field, enter a date.</span></span>
25. <span data-ttu-id="ce084-134">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ce084-134">Click Save.</span></span>
26. <span data-ttu-id="ce084-135">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="ce084-135">Close the page.</span></span>
27. <span data-ttu-id="ce084-136">İşi ilanları'na tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ce084-136">Click Job ads.</span></span>
28. <span data-ttu-id="ce084-137">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ce084-137">Click Save.</span></span>
29. <span data-ttu-id="ce084-138">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="ce084-138">Close the page.</span></span>
30. <span data-ttu-id="ce084-139">Çalışan self servis sayfasında görüntüle onay kutusunu işaretleyin veya işaretini kaldırın.</span><span class="sxs-lookup"><span data-stu-id="ce084-139">Check or uncheck the Display on employee self service checkbox.</span></span>
    * <span data-ttu-id="ce084-140">İşe alma projesinin çalışanlar tarafından Çalışan self servis sayfalarında görüntülenmesini sağlamak için Çalışan self serviste görüntüle onay kutusunu işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="ce084-140">Select the Display on employee self service check box to make the recruitment project visible to employees on their Employee self-service pages.</span></span>  
31. <span data-ttu-id="ce084-141">İşe alma projesi durumu'na tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ce084-141">Click Recruitment project status.</span></span>
32. <span data-ttu-id="ce084-142">Başlat'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ce084-142">Click Start.</span></span>
    * <span data-ttu-id="ce084-143">Başlatıldı durumu, projenin başvuru almaya hazır olduğunu gösterir.</span><span class="sxs-lookup"><span data-stu-id="ce084-143">The Started status means that the project is ready to receive applications.</span></span>  
33. <span data-ttu-id="ce084-144">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ce084-144">Click OK.</span></span>

