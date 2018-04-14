--- 
title: "Planlanmış kanban işlerini taşıma"
description: "Bu prosedür, planlanan işlem kanban işlerini farklı bir döneme taşımaya odaklanmaktadır."
author: ChristianRytt
manager: AnnBe
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: a20765f29a3d8b3bff75229ebbb1996a4d601154
ms.contentlocale: tr-tr
ms.lasthandoff: 04/13/2018

---
# <a name="move-scheduled-kanban-jobs"></a><span data-ttu-id="55267-103">Planlanmış kanban işlerini taşıma</span><span class="sxs-lookup"><span data-stu-id="55267-103">Move scheduled kanban jobs</span></span>

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="55267-104">Bu prosedür, planlanan işlem kanban işlerini farklı bir döneme taşımaya odaklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="55267-104">This procedure focuses on moving planned process kanban jobs to a different period.</span></span> <span data-ttu-id="55267-105">Bu yöntemi oluşturmak için kullanılan demo veri şirketi USMF'dir.</span><span class="sxs-lookup"><span data-stu-id="55267-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="55267-106">Bu prosedür, kanbanlarla çalışan atölye gözetmenlerine veya üretim planlayıcılarına yöneliktir.</span><span class="sxs-lookup"><span data-stu-id="55267-106">This procedure is intended for the shop floor supervisor or production planner working with kanbans.</span></span>


## <a name="select-scheduled-kanban-jobs"></a><span data-ttu-id="55267-107">Planlanmış kanban işlerini seçin</span><span class="sxs-lookup"><span data-stu-id="55267-107">Select scheduled kanban jobs</span></span>
1. <span data-ttu-id="55267-108">Üretim denetimi > Kanban > Kanban işi zamanlaması'nı gidin.</span><span class="sxs-lookup"><span data-stu-id="55267-108">Gå til Produktionsstyring > Kanban > Tidsplanlægning af kanban-job.</span></span>
2. <span data-ttu-id="55267-109">!MtCMR!İş hücresi alanında, açılır menü düğmesine tıklayarak aramayı açın.</span><span class="sxs-lookup"><span data-stu-id="55267-109">!MtCMR!In the Work cell field, click the drop-down button to open the lookup.</span></span> <span data-ttu-id="55267-110">áçêìõý !</span><span class="sxs-lookup"><span data-stu-id="55267-110">áçêìõý !</span></span>
3. <span data-ttu-id="55267-111">Listede, seçili satırı işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="55267-111">Markér den valgte række på listen.</span></span>
    * <span data-ttu-id="55267-112">İş hücresi 1250'yi seç</span><span class="sxs-lookup"><span data-stu-id="55267-112">Select work cell 1250.</span></span>  
4. <span data-ttu-id="55267-113">Seç'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="55267-113">Klik på Select.</span></span>
5. <span data-ttu-id="55267-114">İş durumunu görüntüle alanında "Planlandı"yı seçin.</span><span class="sxs-lookup"><span data-stu-id="55267-114">Vælg 'Planlagt' i feltet Display job status.</span></span>
    * <span data-ttu-id="55267-115">Bu, yalnızca zamanlanmış kanban işlerini görüntülemek üzere iş listesine filtre uygular.</span><span class="sxs-lookup"><span data-stu-id="55267-115">This filters the job list to display only the scheduled kanban jobs.</span></span>  

## <a name="move-kanban-jobs-to-a-different-period"></a><span data-ttu-id="55267-116">Kanban işlerini başka bir döneme taşıyın</span><span class="sxs-lookup"><span data-stu-id="55267-116">Move kanban jobs to a different period</span></span>
1. <span data-ttu-id="55267-117">İstediğiniz girişi bulup seçin.</span><span class="sxs-lookup"><span data-stu-id="55267-117">Find og vælg den ønskede post på listen.</span></span>
    * <span data-ttu-id="55267-118">İş durumu Planlandı olan bir iş seçin. Örneğin Planlanan dönem alanında bir iş 20 Aralık 2012  tarihine zamanlanmıştır.</span><span class="sxs-lookup"><span data-stu-id="55267-118">Select a job that has the Planned job status, for example, a job scheduled on December 20, 2012  in the Planned period field.</span></span> <span data-ttu-id="55267-119">Bu durumda işi önceki döneme taşıyın.</span><span class="sxs-lookup"><span data-stu-id="55267-119">Then move the job to the previous period.</span></span>  
2. <span data-ttu-id="55267-120">Önceki dönem'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="55267-120">Klik på Previous period.</span></span>
3. <span data-ttu-id="55267-121">Bitiş'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="55267-121">Klik på End.</span></span>
    * <span data-ttu-id="55267-122">Bu, işi önceki dönemin son işi olarak iş listesinin sonuna taşır.</span><span class="sxs-lookup"><span data-stu-id="55267-122">This will move the job to the end of the job list as the last job in the previous period.</span></span>  
4. <span data-ttu-id="55267-123">İstediğiniz girişi bulup seçin.</span><span class="sxs-lookup"><span data-stu-id="55267-123">Find og vælg den ønskede post på listen.</span></span>
    * <span data-ttu-id="55267-124">İş durumu Planlandı olan bir iş seçin. Örneğin Planlanan dönem alanında bir iş 18 Aralık 2012 tarihine zamanlanmıştır.</span><span class="sxs-lookup"><span data-stu-id="55267-124">Select a job that has the Planned job status, for example, a job scheduled on December 18, 2012 in the Planned period field.</span></span> <span data-ttu-id="55267-125">Bu durumda işi sonraki döneme taşıyın.</span><span class="sxs-lookup"><span data-stu-id="55267-125">Then move the job to the next period.</span></span>  
5. <span data-ttu-id="55267-126">Sonraki dönem'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="55267-126">Klik på Next period.</span></span>
6. <span data-ttu-id="55267-127">Başlat'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="55267-127">Klik på Start.</span></span>
    * <span data-ttu-id="55267-128">Bu, işi önceki dönemin ilk işi olarak iş listesinin başına taşır.</span><span class="sxs-lookup"><span data-stu-id="55267-128">This will move the job to the start of the job list as the first job in the previous period.</span></span>  

## <a name="task-move-a-job-within-a-period"></a><span data-ttu-id="55267-129">Görev: Bir işi dönem içinde taşıyın</span><span class="sxs-lookup"><span data-stu-id="55267-129">Task: Move a job within a period</span></span>
1. <span data-ttu-id="55267-130">İstediğiniz girişi bulup seçin.</span><span class="sxs-lookup"><span data-stu-id="55267-130">Find og vælg den ønskede post på listen.</span></span>
    * <span data-ttu-id="55267-131">İş durumu Planlandı olan bir iş seçin. Örneğin Planlanan dönem alanında ikinci iş 19 Aralık 2012 tarihine zamanlanmıştır.</span><span class="sxs-lookup"><span data-stu-id="55267-131">Select a job that has the Planned job status, for example, the second job scheduled on December 19, 2012 in the Planned period field.</span></span> <span data-ttu-id="55267-132">Bu durumda işi planlanan dönem içinde taşıyın.</span><span class="sxs-lookup"><span data-stu-id="55267-132">Then move the job within the planned period.</span></span>  
2. <span data-ttu-id="55267-133">İleri'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="55267-133">Klik på Forward.</span></span>
    * <span data-ttu-id="55267-134">İşin listede bir satır aşağıya taşındığına dikkat edin.</span><span class="sxs-lookup"><span data-stu-id="55267-134">Notice that the job is moved one line down on the list.</span></span>  
3. <span data-ttu-id="55267-135">Geri'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="55267-135">Klik på Backward.</span></span>
    * <span data-ttu-id="55267-136">İşin listede bir satır yukarıya taşındığına dikkat edin.</span><span class="sxs-lookup"><span data-stu-id="55267-136">Notice that the job is moved one line up on the list.</span></span>  


