--- 
title: "Malzemeleri kanban işleriyle transfer etme (yalnızca Şubat 2016)"
description: "Bu yordam, malzemelerin aktarmak için bir çekme kanban işini yürütmek üzerinde odaklanır."
author: ChristianRytt
manager: AnnBe
ms.date: 02/07/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 1d98cbff30620256c9d13e7b4a90314db150e33e
ms.openlocfilehash: a28755873cda431077c74ac8ac96061a986e55dd
ms.contentlocale: tr-tr
ms.lasthandoff: 08/07/2018

---
# <a name="transfer-materials-with-kanban-jobs-february-2016-only"></a><span data-ttu-id="546c2-103">Malzemeleri kanban işleriyle transfer etme (yalnızca Şubat 2016)</span><span class="sxs-lookup"><span data-stu-id="546c2-103">Transfer materials with kanban jobs (February 2016 only)</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="546c2-104">Bu yordam, malzemelerin aktarmak için bir çekme kanban işini yürütmek üzerinde odaklanır.</span><span class="sxs-lookup"><span data-stu-id="546c2-104">This procedure focuses on executing a withdrawal kanban job to transfer materials.</span></span> <span data-ttu-id="546c2-105">Bu yöntemi oluşturmak için kullanılan demo veri şirketi USMF'dir.</span><span class="sxs-lookup"><span data-stu-id="546c2-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="546c2-106">Bu yordam ambar çalışanı için hazırlanmıştır.</span><span class="sxs-lookup"><span data-stu-id="546c2-106">This procedure is intended for the warehouse worker.</span></span>


## <a name="display-transfer-jobs"></a><span data-ttu-id="546c2-107">Transfer işlerini görüntüler</span><span class="sxs-lookup"><span data-stu-id="546c2-107">Display transfer jobs</span></span>
1. <span data-ttu-id="546c2-108">Production control > Kanban > Kanban board for transfer jobs (Üretim kontrolü > Kanban > Transfer işleri için kanban panosu) menüsüne gidin.</span><span class="sxs-lookup"><span data-stu-id="546c2-108">Go to Production control > Kanban > Kanban board for transfer jobs.</span></span>
2. <span data-ttu-id="546c2-109">Filtreler bölümünü genişletin veya daraltın.</span><span class="sxs-lookup"><span data-stu-id="546c2-109">Expand or collapse the Filters section.</span></span>
    * <span data-ttu-id="546c2-110">Filtreler bölümünde üretim akışı, eylem adı, kaynak ambar ve konumu, hedef ambar ve konumu ile filtreleyerek hangi işleri görmek istediğinizi seçebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="546c2-110">In the Filters section, you can specify what jobs you want to see by filtering on Production flow, Activity name, From warehouse and location, and To warehouse and location.</span></span>  
3. <span data-ttu-id="546c2-111">Kaynak ambar alanına '11' yazın.</span><span class="sxs-lookup"><span data-stu-id="546c2-111">In the From warehouse field, type '11'.</span></span>
4. <span data-ttu-id="546c2-112">Hedef konum alanına '12' yazın.</span><span class="sxs-lookup"><span data-stu-id="546c2-112">In the To location field, type '12'.</span></span>

## <a name="start-a-transfer-job"></a><span data-ttu-id="546c2-113">Bir transfer işi başlat</span><span class="sxs-lookup"><span data-stu-id="546c2-113">Start a transfer job</span></span>
1. <span data-ttu-id="546c2-114">Listede, eğer varsa, seçili satırın işaretini kaldırın.</span><span class="sxs-lookup"><span data-stu-id="546c2-114">In the list, deselect the selected row - if any.</span></span>
2. <span data-ttu-id="546c2-115">Listede satır 4'ü seçin.</span><span class="sxs-lookup"><span data-stu-id="546c2-115">In the list, select row 4.</span></span>
    * <span data-ttu-id="546c2-116">Durumu Planlanmami; olan ilk işi seçin.</span><span class="sxs-lookup"><span data-stu-id="546c2-116">Select the first job with status Not planned.</span></span> <span data-ttu-id="546c2-117">Yalnız bu işin seçildiğinden emin olun.</span><span class="sxs-lookup"><span data-stu-id="546c2-117">Make sure this is the only job selected.</span></span>  
3. <span data-ttu-id="546c2-118">Başlat'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="546c2-118">Click Start.</span></span>
    * <span data-ttu-id="546c2-119">Bir simgenin işin başladığı belirttiğine dikkat edin.</span><span class="sxs-lookup"><span data-stu-id="546c2-119">Notice that an icon indicates that the job is started.</span></span>  

## <a name="select-a-second-transfer-job-and-change-quantity"></a><span data-ttu-id="546c2-120">İkinci bir transfer işi seçin ve miktarı değiştirin</span><span class="sxs-lookup"><span data-stu-id="546c2-120">Select a second transfer job and change quantity</span></span>
1. <span data-ttu-id="546c2-121">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="546c2-121">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="546c2-122">Birden fazla iş seçebilirsiniz fakat şimdilik sadece satır 5'i seçin.</span><span class="sxs-lookup"><span data-stu-id="546c2-122">You can have multiple jobs selected, but for now select row 5.</span></span>  
2. <span data-ttu-id="546c2-123">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="546c2-123">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="546c2-124">Önceki adımdaki işin seçilen tek iş olduğundan emin olun.</span><span class="sxs-lookup"><span data-stu-id="546c2-124">Make sure the job in the previous step is the only one selected.</span></span> <span data-ttu-id="546c2-125">Diğer tüm işlerin seçimlerini kaldırın.</span><span class="sxs-lookup"><span data-stu-id="546c2-125">Deselect all other jobs.</span></span>  
3. <span data-ttu-id="546c2-126">İş miktarı alanındaki değeri, daha sonra başvurmak üzere not edin</span><span class="sxs-lookup"><span data-stu-id="546c2-126">Note the value in the Job quantity field to reference later</span></span>
4. <span data-ttu-id="546c2-127">İş miktarını '30' olacak şekilde ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="546c2-127">Set Job quantity to '30'.</span></span>
    * <span data-ttu-id="546c2-128">Uyarıya dikkat edin!</span><span class="sxs-lookup"><span data-stu-id="546c2-128">Notice the warning!</span></span> <span data-ttu-id="546c2-129">30 transfer etmenize izin verilmez.</span><span class="sxs-lookup"><span data-stu-id="546c2-129">You are not allowed to transfer 30.</span></span> <span data-ttu-id="546c2-130">Kanban kural ayarına göre sadece başlangıçtaki miktarı aktarabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="546c2-130">According to the setup of the kanban rule, you can only transfer the original quantity.</span></span>  
5. <span data-ttu-id="546c2-131">Daha önce not edilen değeri İş miktarı alanında kullanın</span><span class="sxs-lookup"><span data-stu-id="546c2-131">Use the value noted previously in the Job quantity field</span></span>
    * <span data-ttu-id="546c2-132">İş miktarını önceki değere ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="546c2-132">Set the Job quantity to the previous value.</span></span>  

## <a name="start-the-second-transfer-job"></a><span data-ttu-id="546c2-133">İkinci transfer işlemini başlatın</span><span class="sxs-lookup"><span data-stu-id="546c2-133">Start the second transfer job</span></span>
1. <span data-ttu-id="546c2-134">Başlat'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="546c2-134">Click Start.</span></span>
    * <span data-ttu-id="546c2-135">Bu, satır 5'deki işin transferini başlatacaktır.</span><span class="sxs-lookup"><span data-stu-id="546c2-135">This will start the transfer of the job in row 5.</span></span>  

## <a name="complete-both-transfer-jobs"></a><span data-ttu-id="546c2-136">Her iki transfer işini tamamlayın</span><span class="sxs-lookup"><span data-stu-id="546c2-136">Complete both transfer jobs</span></span>
1. <span data-ttu-id="546c2-137">Listede satır 4'ü seçin.</span><span class="sxs-lookup"><span data-stu-id="546c2-137">In the list, select row 4.</span></span>
    * <span data-ttu-id="546c2-138">Şimdi satır 4 ve 5'te iki transfer işi seçilmiştir.</span><span class="sxs-lookup"><span data-stu-id="546c2-138">Now two transfer jobs are selected on row 4 and row 5.</span></span>  
2. <span data-ttu-id="546c2-139">Tamamla öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="546c2-139">Click Complete.</span></span>
    * <span data-ttu-id="546c2-140">Bu her iki işin transferini tamamlayacaktır.</span><span class="sxs-lookup"><span data-stu-id="546c2-140">This will complete the transfer of both jobs.</span></span>  


