--- 
title: "Planlanmış kanban işlerini taşıma"
description: "Bu prosedür, planlanan işlem kanban işlerini farklı bir döneme taşımaya odaklanmaktadır."
author: ChristianRytt
manager: AnnBe
ms.date: 11/07/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: KanbanJobSchedulingListPage
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: b589a6ce02cdc02436e256f9e81346fe8b766687
ms.openlocfilehash: f791c9048ef6efe1585c991f998099cd1fc12df7
ms.contentlocale: tr-tr
ms.lasthandoff: 12/04/2018

---

# <a name="move-scheduled-kanban-jobs"></a><span data-ttu-id="c20bc-103">Planlanmış kanban işlerini taşıma</span><span class="sxs-lookup"><span data-stu-id="c20bc-103">Move scheduled kanban jobs</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="c20bc-104">Bu prosedür, planlanan işlem kanban işlerini farklı bir döneme taşımaya odaklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="c20bc-104">This procedure focuses on moving planned process kanban jobs to a different period.</span></span> <span data-ttu-id="c20bc-105">Bu yöntemi oluşturmak için kullanılan demo veri şirketi USMF'dir.</span><span class="sxs-lookup"><span data-stu-id="c20bc-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="c20bc-106">Bu prosedür, kanbanlarla çalışan atölye gözetmenlerine veya üretim planlayıcılarına yöneliktir.</span><span class="sxs-lookup"><span data-stu-id="c20bc-106">This procedure is intended for the shop floor supervisor or production planner working with kanbans.</span></span>

## <a name="select-scheduled-kanban-jobs"></a><span data-ttu-id="c20bc-107">Planlanmış kanban işlerini seçin.</span><span class="sxs-lookup"><span data-stu-id="c20bc-107">Select scheduled kanban jobs.</span></span> 

1. <span data-ttu-id="c20bc-108">**Üretim denetimi > Kanban > Kanban işi planlaması**'na gidin.</span><span class="sxs-lookup"><span data-stu-id="c20bc-108">Go to **Production control > Kanban > Kanban job scheduling**.</span></span> 

2. <span data-ttu-id="c20bc-109">**İş hücresi** alanında, açılır menü düğmesine tıklayarak aramayı açın.</span><span class="sxs-lookup"><span data-stu-id="c20bc-109">In the **Work cell** field, click the drop-down button to open the lookup.</span></span> 

3. <span data-ttu-id="c20bc-110">Listede, seçili satırı işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="c20bc-110">In the list, mark the selected row.</span></span> 
   - <span data-ttu-id="c20bc-111">İş hücresi 1250'yi seç</span><span class="sxs-lookup"><span data-stu-id="c20bc-111">Select work cell 1250.</span></span> 
4. <span data-ttu-id="c20bc-112">**Seç**'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="c20bc-112">Click **Select**.</span></span> 

5. <span data-ttu-id="c20bc-113">**İş durumunu görüntüle** alanında **Planlandı**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="c20bc-113">In the **Display job status** field, select **Scheduled**.</span></span> <span data-ttu-id="c20bc-114">Bu, yalnızca zamanlanmış kanban işlerini görüntülemek üzere iş listesine filtre uygular.</span><span class="sxs-lookup"><span data-stu-id="c20bc-114">This filters the job list to display only the scheduled kanban jobs.</span></span> 

## <a name="move-kanban-jobs-to-a-different-period"></a><span data-ttu-id="c20bc-115">Kanban işlerini başka bir döneme taşıyın.</span><span class="sxs-lookup"><span data-stu-id="c20bc-115">Move kanban jobs to a different period.</span></span> 

1. <span data-ttu-id="c20bc-116">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="c20bc-116">In the list, find and select the desired record.</span></span> <span data-ttu-id="c20bc-117">İş durumu **Planlanan iş** olan bir iş seçin. Örneğin **Planlanan dönem** alanında bir iş 20 Aralık 2012 tarihine zamanlanmıştır.</span><span class="sxs-lookup"><span data-stu-id="c20bc-117">Select a job that has the **Planned job** status, for example, a job scheduled on December 20, 2012 in the **Planned period** field.</span></span> <span data-ttu-id="c20bc-118">Bu durumda işi önceki döneme taşıyın.</span><span class="sxs-lookup"><span data-stu-id="c20bc-118">Then move the job to the previous period.</span></span> 

2. <span data-ttu-id="c20bc-119">**Önceki dönem**'i tıklayın.</span><span class="sxs-lookup"><span data-stu-id="c20bc-119">Click **Previous period**.</span></span> 

3. <span data-ttu-id="c20bc-120">İşi önceki dönemin son işi olarak iş listesinin sonuna taşımak için **Sonlandır** üzerine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="c20bc-120">Click **End** to move the job to the end of the job list as the last job in the previous period.</span></span> 

4. <span data-ttu-id="c20bc-121">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="c20bc-121">In the list, find and select the desired record.</span></span> <span data-ttu-id="c20bc-122">İş durumu **Planlanan iş** olan bir iş seçin. Örneğin **Planlanan dönem** alanında bir iş 18 Aralık 2012 tarihine zamanlanmıştır.</span><span class="sxs-lookup"><span data-stu-id="c20bc-122">Select a job that has the **Planned job** status, for example, a job scheduled on December 18, 2012 in the **Planned period** field.</span></span> <span data-ttu-id="c20bc-123">Bu durumda işi sonraki döneme taşıyın.</span><span class="sxs-lookup"><span data-stu-id="c20bc-123">Then move the job to the next period.</span></span> 

5. <span data-ttu-id="c20bc-124">**Sonraki dönem**'i tıklayın.</span><span class="sxs-lookup"><span data-stu-id="c20bc-124">Click **Next period**.</span></span> 

6. <span data-ttu-id="c20bc-125">İşi önceki dönemin işi olarak iş listesinin başına taşımak için **Başlat** üzerine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="c20bc-125">Click **Start** to move the job to the start of the job list as the first job in the previous period.</span></span> 

## <a name="move-a-job-within-a-period"></a><span data-ttu-id="c20bc-126">Bir işi dönem içinde taşıyın.</span><span class="sxs-lookup"><span data-stu-id="c20bc-126">Move a job within a period.</span></span> 

1. <span data-ttu-id="c20bc-127">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="c20bc-127">In the list, find and select the desired record.</span></span> <span data-ttu-id="c20bc-128">İş durumu Planlandı olan bir iş seçin. Örneğin **Planlanan dönem** alanında ikinci iş 19 Aralık 2012 tarihine zamanlanmıştır.</span><span class="sxs-lookup"><span data-stu-id="c20bc-128">Select a job that has the Planned job status, for example, the second job scheduled on December 19, 2012 in the **Planned period** field.</span></span> <span data-ttu-id="c20bc-129">Bu durumda işi planlanan dönem içinde taşıyın.</span><span class="sxs-lookup"><span data-stu-id="c20bc-129">Then move the job within the planned period.</span></span> 

2. <span data-ttu-id="c20bc-130">**İleri**'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="c20bc-130">Click **Forward**.</span></span> <span data-ttu-id="c20bc-131">İşin listede bir satır aşağıya taşındığına dikkat edin.</span><span class="sxs-lookup"><span data-stu-id="c20bc-131">Notice that the job is moved one line down on the list.</span></span> 

3. <span data-ttu-id="c20bc-132">**Geri**'yi tıklatın.</span><span class="sxs-lookup"><span data-stu-id="c20bc-132">Click **Backward**.</span></span> <span data-ttu-id="c20bc-133">İşin listede bir satır yukarıya taşındığına dikkat edin.</span><span class="sxs-lookup"><span data-stu-id="c20bc-133">Notice that the job is moved one line up on the list.</span></span>

