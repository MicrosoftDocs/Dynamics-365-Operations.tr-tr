---
title: Kanban işleriyle malzemeleri transfer etme
description: Bu yordam, malzemelerin aktarmak için bir çekme kanban işini yürütmek üzerinde odaklanır.
author: ChristianRytt
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KanbanBoardTransferJob
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: df65ea59be29dbe4eaad30558fcff4394737158f
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5224942"
---
# <a name="transfer-materials-with-kanban-jobs"></a><span data-ttu-id="da5e0-103">Kanban işleriyle malzemeleri transfer etme</span><span class="sxs-lookup"><span data-stu-id="da5e0-103">Transfer materials with kanban jobs</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="da5e0-104">Bu yordam, malzemelerin aktarmak için bir çekme kanban işini yürütmek üzerinde odaklanır.</span><span class="sxs-lookup"><span data-stu-id="da5e0-104">This procedure focuses on executing a withdrawal kanban job to transfer materials.</span></span> <span data-ttu-id="da5e0-105">Bu yöntemi oluşturmak için kullanılan demo veri şirketi USMF'dir.</span><span class="sxs-lookup"><span data-stu-id="da5e0-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="da5e0-106">Bu yordam ambar çalışanı için hazırlanmıştır.</span><span class="sxs-lookup"><span data-stu-id="da5e0-106">This procedure is intended for the warehouse worker.</span></span>


## <a name="display-transfer-jobs"></a><span data-ttu-id="da5e0-107">Transfer işlerini görüntüler</span><span class="sxs-lookup"><span data-stu-id="da5e0-107">Display transfer jobs</span></span>
1. <span data-ttu-id="da5e0-108">Production control > Kanban > Kanban board for transfer jobs (Üretim kontrolü > Kanban > Transfer işleri için kanban panosu) menüsüne gidin.</span><span class="sxs-lookup"><span data-stu-id="da5e0-108">Go to Production control > Kanban > Kanban board for transfer jobs.</span></span>
2. <span data-ttu-id="da5e0-109">Filtreler bölümünü genişletin veya daraltın.</span><span class="sxs-lookup"><span data-stu-id="da5e0-109">Expand or collapse the Filters section.</span></span>
    * <span data-ttu-id="da5e0-110">Filtreler bölümünde üretim akışı, eylem adı, kaynak ambar ve konumu, hedef ambar ve konumu ile filtreleyerek hangi işleri görmek istediğinizi seçebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="da5e0-110">In the Filters section, you can specify what jobs you want to see by filtering on Production flow, Activity name, From warehouse and location, and To warehouse and location.</span></span>  
3. <span data-ttu-id="da5e0-111">Kaynak ambar alanına '11' yazın.</span><span class="sxs-lookup"><span data-stu-id="da5e0-111">In the From warehouse field, type '11'.</span></span>
4. <span data-ttu-id="da5e0-112">Hedef konum alanına '12' yazın.</span><span class="sxs-lookup"><span data-stu-id="da5e0-112">In the To location field, type '12'.</span></span>

## <a name="start-a-transfer-job"></a><span data-ttu-id="da5e0-113">Bir transfer işi başlat</span><span class="sxs-lookup"><span data-stu-id="da5e0-113">Start a transfer job</span></span>
1. <span data-ttu-id="da5e0-114">Listede, eğer varsa, seçili satırın işaretini kaldırın.</span><span class="sxs-lookup"><span data-stu-id="da5e0-114">In the list, deselect the selected row - if any.</span></span>
2. <span data-ttu-id="da5e0-115">Listede satır 4'ü seçin.</span><span class="sxs-lookup"><span data-stu-id="da5e0-115">In the list, select row 4.</span></span>
    * <span data-ttu-id="da5e0-116">Durumu Planlanmami; olan ilk işi seçin.</span><span class="sxs-lookup"><span data-stu-id="da5e0-116">Select the first job with status Not planned.</span></span> <span data-ttu-id="da5e0-117">Yalnız bu işin seçildiğinden emin olun.</span><span class="sxs-lookup"><span data-stu-id="da5e0-117">Make sure this is the only job selected.</span></span>  
3. <span data-ttu-id="da5e0-118">Başlat'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="da5e0-118">Click Start.</span></span>
    * <span data-ttu-id="da5e0-119">Bir simgenin işin başladığı belirttiğine dikkat edin.</span><span class="sxs-lookup"><span data-stu-id="da5e0-119">Notice that an icon indicates that the job is started.</span></span>  

## <a name="select-a-second-transfer-job-and-change-quantity"></a><span data-ttu-id="da5e0-120">İkinci bir transfer işi seçin ve miktarı değiştirin</span><span class="sxs-lookup"><span data-stu-id="da5e0-120">Select a second transfer job and change quantity</span></span>
1. <span data-ttu-id="da5e0-121">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="da5e0-121">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="da5e0-122">Birden fazla iş seçebilirsiniz fakat şimdilik sadece satır 5'i seçin.</span><span class="sxs-lookup"><span data-stu-id="da5e0-122">You can have multiple jobs selected, but for now select row 5.</span></span>  
2. <span data-ttu-id="da5e0-123">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="da5e0-123">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="da5e0-124">Önceki adımdaki işin seçilen tek iş olduğundan emin olun.</span><span class="sxs-lookup"><span data-stu-id="da5e0-124">Make sure the job in the previous step is the only one selected.</span></span> <span data-ttu-id="da5e0-125">Diğer tüm işlerin seçimlerini kaldırın.</span><span class="sxs-lookup"><span data-stu-id="da5e0-125">Deselect all other jobs.</span></span>  
3. <span data-ttu-id="da5e0-126">İş miktarı alanındaki değeri, daha sonra başvurmak üzere not edin</span><span class="sxs-lookup"><span data-stu-id="da5e0-126">Note the value in the Job quantity field to reference later</span></span>
4. <span data-ttu-id="da5e0-127">İş miktarını '30' olacak şekilde ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="da5e0-127">Set Job quantity to '30'.</span></span>
    * <span data-ttu-id="da5e0-128">Uyarıya dikkat edin!</span><span class="sxs-lookup"><span data-stu-id="da5e0-128">Notice the warning!</span></span> <span data-ttu-id="da5e0-129">30 transfer etmenize izin verilmez.</span><span class="sxs-lookup"><span data-stu-id="da5e0-129">You are not allowed to transfer 30.</span></span> <span data-ttu-id="da5e0-130">Kanban kural ayarına göre sadece başlangıçtaki miktarı aktarabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="da5e0-130">According to the setup of the kanban rule, you can only transfer the original quantity.</span></span>  
5. <span data-ttu-id="da5e0-131">Daha önce not edilen değeri İş miktarı alanında kullanın</span><span class="sxs-lookup"><span data-stu-id="da5e0-131">Use the value noted previously in the Job quantity field</span></span>
    * <span data-ttu-id="da5e0-132">İş miktarını önceki değere ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="da5e0-132">Set the Job quantity to the previous value.</span></span>  

## <a name="start-the-second-transfer-job"></a><span data-ttu-id="da5e0-133">İkinci transfer işlemini başlatın</span><span class="sxs-lookup"><span data-stu-id="da5e0-133">Start the second transfer job</span></span>
1. <span data-ttu-id="da5e0-134">Başlat'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="da5e0-134">Click Start.</span></span>
    * <span data-ttu-id="da5e0-135">Bu, satır 5'deki işin transferini başlatacaktır.</span><span class="sxs-lookup"><span data-stu-id="da5e0-135">This will start the transfer of the job in row 5.</span></span>  

## <a name="complete-both-transfer-jobs"></a><span data-ttu-id="da5e0-136">Her iki transfer işini tamamlayın</span><span class="sxs-lookup"><span data-stu-id="da5e0-136">Complete both transfer jobs</span></span>
1. <span data-ttu-id="da5e0-137">Listede satır 4'ü seçin.</span><span class="sxs-lookup"><span data-stu-id="da5e0-137">In the list, select row 4.</span></span>
    * <span data-ttu-id="da5e0-138">Şimdi satır 4 ve 5'te iki transfer işi seçilmiştir.</span><span class="sxs-lookup"><span data-stu-id="da5e0-138">Now two transfer jobs are selected on row 4 and row 5.</span></span>  
2. <span data-ttu-id="da5e0-139">Tamamla öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="da5e0-139">Click Complete.</span></span>
    * <span data-ttu-id="da5e0-140">Bu her iki işin transferini tamamlayacaktır.</span><span class="sxs-lookup"><span data-stu-id="da5e0-140">This will complete the transfer of both jobs.</span></span>  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]