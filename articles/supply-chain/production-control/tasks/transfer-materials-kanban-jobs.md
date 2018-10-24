--- 
title: "Kanban işleriyle malzemeleri transfer etme"
description: "Bu yordam, malzemelerin aktarmak için bir çekme kanban işini yürütmek üzerinde odaklanır."
author: ChristianRytt
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: KanbanBoardTransferJob
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0312b8cfadd45f8e59225e9daba78b9e216cff51
ms.openlocfilehash: a2db7b9fb960beb5b4a851aabb9f28a0f9e3d3da
ms.contentlocale: tr-tr
ms.lasthandoff: 09/14/2018

---
# <a name="transfer-materials-with-kanban-jobs"></a><span data-ttu-id="6de12-103">Kanban işleriyle malzemeleri transfer etme</span><span class="sxs-lookup"><span data-stu-id="6de12-103">Transfer materials with kanban jobs</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="6de12-104">Bu yordam, malzemelerin aktarmak için bir çekme kanban işini yürütmek üzerinde odaklanır.</span><span class="sxs-lookup"><span data-stu-id="6de12-104">This procedure focuses on executing a withdrawal kanban job to transfer materials.</span></span> <span data-ttu-id="6de12-105">Bu yöntemi oluşturmak için kullanılan demo veri şirketi USMF'dir.</span><span class="sxs-lookup"><span data-stu-id="6de12-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="6de12-106">Bu yordam ambar çalışanı için hazırlanmıştır.</span><span class="sxs-lookup"><span data-stu-id="6de12-106">This procedure is intended for the warehouse worker.</span></span>


## <a name="display-transfer-jobs"></a><span data-ttu-id="6de12-107">Transfer işlerini görüntüler</span><span class="sxs-lookup"><span data-stu-id="6de12-107">Display transfer jobs</span></span>
1. <span data-ttu-id="6de12-108">Production control > Kanban > Kanban board for transfer jobs (Üretim kontrolü > Kanban > Transfer işleri için kanban panosu) menüsüne gidin.</span><span class="sxs-lookup"><span data-stu-id="6de12-108">Go to Production control > Kanban > Kanban board for transfer jobs.</span></span>
2. <span data-ttu-id="6de12-109">Filtreler bölümünü genişletin veya daraltın.</span><span class="sxs-lookup"><span data-stu-id="6de12-109">Expand or collapse the Filters section.</span></span>
    * <span data-ttu-id="6de12-110">Filtreler bölümünde üretim akışı, eylem adı, kaynak ambar ve konumu, hedef ambar ve konumu ile filtreleyerek hangi işleri görmek istediğinizi seçebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="6de12-110">In the Filters section, you can specify what jobs you want to see by filtering on Production flow, Activity name, From warehouse and location, and To warehouse and location.</span></span>  
3. <span data-ttu-id="6de12-111">Kaynak ambar alanına '11' yazın.</span><span class="sxs-lookup"><span data-stu-id="6de12-111">In the From warehouse field, type '11'.</span></span>
4. <span data-ttu-id="6de12-112">Hedef konum alanına '12' yazın.</span><span class="sxs-lookup"><span data-stu-id="6de12-112">In the To location field, type '12'.</span></span>

## <a name="start-a-transfer-job"></a><span data-ttu-id="6de12-113">Bir transfer işi başlat</span><span class="sxs-lookup"><span data-stu-id="6de12-113">Start a transfer job</span></span>
1. <span data-ttu-id="6de12-114">Listede, eğer varsa, seçili satırın işaretini kaldırın.</span><span class="sxs-lookup"><span data-stu-id="6de12-114">In the list, deselect the selected row - if any.</span></span>
2. <span data-ttu-id="6de12-115">Listede satır 4'ü seçin.</span><span class="sxs-lookup"><span data-stu-id="6de12-115">In the list, select row 4.</span></span>
    * <span data-ttu-id="6de12-116">Durumu Planlanmami; olan ilk işi seçin.</span><span class="sxs-lookup"><span data-stu-id="6de12-116">Select the first job with status Not planned.</span></span> <span data-ttu-id="6de12-117">Yalnız bu işin seçildiğinden emin olun.</span><span class="sxs-lookup"><span data-stu-id="6de12-117">Make sure this is the only job selected.</span></span>  
3. <span data-ttu-id="6de12-118">Başlat'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="6de12-118">Click Start.</span></span>
    * <span data-ttu-id="6de12-119">Bir simgenin işin başladığı belirttiğine dikkat edin.</span><span class="sxs-lookup"><span data-stu-id="6de12-119">Notice that an icon indicates that the job is started.</span></span>  

## <a name="select-a-second-transfer-job-and-change-quantity"></a><span data-ttu-id="6de12-120">İkinci bir transfer işi seçin ve miktarı değiştirin</span><span class="sxs-lookup"><span data-stu-id="6de12-120">Select a second transfer job and change quantity</span></span>
1. <span data-ttu-id="6de12-121">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="6de12-121">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="6de12-122">Birden fazla iş seçebilirsiniz fakat şimdilik sadece satır 5'i seçin.</span><span class="sxs-lookup"><span data-stu-id="6de12-122">You can have multiple jobs selected, but for now select row 5.</span></span>  
2. <span data-ttu-id="6de12-123">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="6de12-123">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="6de12-124">Önceki adımdaki işin seçilen tek iş olduğundan emin olun.</span><span class="sxs-lookup"><span data-stu-id="6de12-124">Make sure the job in the previous step is the only one selected.</span></span> <span data-ttu-id="6de12-125">Diğer tüm işlerin seçimlerini kaldırın.</span><span class="sxs-lookup"><span data-stu-id="6de12-125">Deselect all other jobs.</span></span>  
3. <span data-ttu-id="6de12-126">İş miktarı alanındaki değeri, daha sonra başvurmak üzere not edin</span><span class="sxs-lookup"><span data-stu-id="6de12-126">Note the value in the Job quantity field to reference later</span></span>
4. <span data-ttu-id="6de12-127">İş miktarını '30' olacak şekilde ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="6de12-127">Set Job quantity to '30'.</span></span>
    * <span data-ttu-id="6de12-128">Uyarıya dikkat edin!</span><span class="sxs-lookup"><span data-stu-id="6de12-128">Notice the warning!</span></span> <span data-ttu-id="6de12-129">30 transfer etmenize izin verilmez.</span><span class="sxs-lookup"><span data-stu-id="6de12-129">You are not allowed to transfer 30.</span></span> <span data-ttu-id="6de12-130">Kanban kural ayarına göre sadece başlangıçtaki miktarı aktarabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="6de12-130">According to the setup of the kanban rule, you can only transfer the original quantity.</span></span>  
5. <span data-ttu-id="6de12-131">Daha önce not edilen değeri İş miktarı alanında kullanın</span><span class="sxs-lookup"><span data-stu-id="6de12-131">Use the value noted previously in the Job quantity field</span></span>
    * <span data-ttu-id="6de12-132">İş miktarını önceki değere ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="6de12-132">Set the Job quantity to the previous value.</span></span>  

## <a name="start-the-second-transfer-job"></a><span data-ttu-id="6de12-133">İkinci transfer işlemini başlatın</span><span class="sxs-lookup"><span data-stu-id="6de12-133">Start the second transfer job</span></span>
1. <span data-ttu-id="6de12-134">Başlat'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="6de12-134">Click Start.</span></span>
    * <span data-ttu-id="6de12-135">Bu, satır 5'deki işin transferini başlatacaktır.</span><span class="sxs-lookup"><span data-stu-id="6de12-135">This will start the transfer of the job in row 5.</span></span>  

## <a name="complete-both-transfer-jobs"></a><span data-ttu-id="6de12-136">Her iki transfer işini tamamlayın</span><span class="sxs-lookup"><span data-stu-id="6de12-136">Complete both transfer jobs</span></span>
1. <span data-ttu-id="6de12-137">Listede satır 4'ü seçin.</span><span class="sxs-lookup"><span data-stu-id="6de12-137">In the list, select row 4.</span></span>
    * <span data-ttu-id="6de12-138">Şimdi satır 4 ve 5'te iki transfer işi seçilmiştir.</span><span class="sxs-lookup"><span data-stu-id="6de12-138">Now two transfer jobs are selected on row 4 and row 5.</span></span>  
2. <span data-ttu-id="6de12-139">Tamamla öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="6de12-139">Click Complete.</span></span>
    * <span data-ttu-id="6de12-140">Bu her iki işin transferini tamamlayacaktır.</span><span class="sxs-lookup"><span data-stu-id="6de12-140">This will complete the transfer of both jobs.</span></span>  


