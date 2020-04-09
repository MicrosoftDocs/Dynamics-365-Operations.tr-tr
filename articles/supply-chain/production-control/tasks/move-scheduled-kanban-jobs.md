---
title: Planlanmış kanban işlerini taşıma
description: Bu prosedür, planlanan işlem kanban işlerini farklı bir döneme taşımaya odaklanmaktadır.
author: ChristianRytt
manager: AnnBe
ms.date: 11/07/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KanbanJobSchedulingListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: cad61ad292f80d6092ecea679645f729469b8a8f
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/18/2020
ms.locfileid: "3149010"
---
# <a name="move-scheduled-kanban-jobs"></a><span data-ttu-id="a326a-103">Planlanmış kanban işlerini taşıma</span><span class="sxs-lookup"><span data-stu-id="a326a-103">Move scheduled kanban jobs</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="a326a-104">Bu prosedür, planlanan işlem kanban işlerini farklı bir döneme taşımaya odaklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="a326a-104">This procedure focuses on moving planned process kanban jobs to a different period.</span></span> <span data-ttu-id="a326a-105">Bu yöntemi oluşturmak için kullanılan demo veri şirketi USMF'dir.</span><span class="sxs-lookup"><span data-stu-id="a326a-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="a326a-106">Bu prosedür, kanbanlarla çalışan atölye gözetmenlerine veya üretim planlayıcılarına yöneliktir.</span><span class="sxs-lookup"><span data-stu-id="a326a-106">This procedure is intended for the shop floor supervisor or production planner working with kanbans.</span></span>

## <a name="select-scheduled-kanban-jobs"></a><span data-ttu-id="a326a-107">Planlanmış kanban işlerini seçin.</span><span class="sxs-lookup"><span data-stu-id="a326a-107">Select scheduled kanban jobs.</span></span> 

1. <span data-ttu-id="a326a-108">**Üretim denetimi > Kanban > Kanban işi planlaması**'na gidin.</span><span class="sxs-lookup"><span data-stu-id="a326a-108">Go to **Production control > Kanban > Kanban job scheduling**.</span></span> 

2. <span data-ttu-id="a326a-109">**İş hücresi** alanında, açılır menü düğmesine tıklayarak aramayı açın.</span><span class="sxs-lookup"><span data-stu-id="a326a-109">In the **Work cell** field, click the drop-down button to open the lookup.</span></span> 

3. <span data-ttu-id="a326a-110">Listede, seçili satırı işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="a326a-110">In the list, mark the selected row.</span></span> 
   - <span data-ttu-id="a326a-111">İş hücresi 1250'yi seç</span><span class="sxs-lookup"><span data-stu-id="a326a-111">Select work cell 1250.</span></span> 
4. <span data-ttu-id="a326a-112">**Seç**'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="a326a-112">Click **Select**.</span></span> 

5. <span data-ttu-id="a326a-113">**İş durumunu görüntüle** alanında **Planlandı**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="a326a-113">In the **Display job status** field, select **Scheduled**.</span></span> <span data-ttu-id="a326a-114">Bu, yalnızca zamanlanmış kanban işlerini görüntülemek üzere iş listesine filtre uygular.</span><span class="sxs-lookup"><span data-stu-id="a326a-114">This filters the job list to display only the scheduled kanban jobs.</span></span> 

## <a name="move-kanban-jobs-to-a-different-period"></a><span data-ttu-id="a326a-115">Kanban işlerini başka bir döneme taşıyın.</span><span class="sxs-lookup"><span data-stu-id="a326a-115">Move kanban jobs to a different period.</span></span> 

1. <span data-ttu-id="a326a-116">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="a326a-116">In the list, find and select the desired record.</span></span> <span data-ttu-id="a326a-117">İş durumu **Planlanan iş** olan bir iş seçin. Örneğin **Planlanan dönem** alanında bir iş 20 Aralık 2012 tarihine zamanlanmıştır.</span><span class="sxs-lookup"><span data-stu-id="a326a-117">Select a job that has the **Planned job** status, for example, a job scheduled on December 20, 2012 in the **Planned period** field.</span></span> <span data-ttu-id="a326a-118">Bu durumda işi önceki döneme taşıyın.</span><span class="sxs-lookup"><span data-stu-id="a326a-118">Then move the job to the previous period.</span></span> 

2. <span data-ttu-id="a326a-119">**Önceki dönem**'i tıklayın.</span><span class="sxs-lookup"><span data-stu-id="a326a-119">Click **Previous period**.</span></span> 

3. <span data-ttu-id="a326a-120">İşi önceki dönemin son işi olarak iş listesinin sonuna taşımak için **Sonlandır** üzerine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="a326a-120">Click **End** to move the job to the end of the job list as the last job in the previous period.</span></span> 

4. <span data-ttu-id="a326a-121">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="a326a-121">In the list, find and select the desired record.</span></span> <span data-ttu-id="a326a-122">İş durumu **Planlanan iş** olan bir iş seçin. Örneğin **Planlanan dönem** alanında bir iş 18 Aralık 2012 tarihine zamanlanmıştır.</span><span class="sxs-lookup"><span data-stu-id="a326a-122">Select a job that has the **Planned job** status, for example, a job scheduled on December 18, 2012 in the **Planned period** field.</span></span> <span data-ttu-id="a326a-123">Bu durumda işi sonraki döneme taşıyın.</span><span class="sxs-lookup"><span data-stu-id="a326a-123">Then move the job to the next period.</span></span> 

5. <span data-ttu-id="a326a-124">**Sonraki dönem**'i tıklayın.</span><span class="sxs-lookup"><span data-stu-id="a326a-124">Click **Next period**.</span></span> 

6. <span data-ttu-id="a326a-125">İşi önceki dönemin işi olarak iş listesinin başına taşımak için **Başlat** üzerine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="a326a-125">Click **Start** to move the job to the start of the job list as the first job in the previous period.</span></span> 

## <a name="move-a-job-within-a-period"></a><span data-ttu-id="a326a-126">Bir işi dönem içinde taşıyın.</span><span class="sxs-lookup"><span data-stu-id="a326a-126">Move a job within a period.</span></span> 

1. <span data-ttu-id="a326a-127">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="a326a-127">In the list, find and select the desired record.</span></span> <span data-ttu-id="a326a-128">İş durumu Planlandı olan bir iş seçin. Örneğin **Planlanan dönem** alanında ikinci iş 19 Aralık 2012 tarihine zamanlanmıştır.</span><span class="sxs-lookup"><span data-stu-id="a326a-128">Select a job that has the Planned job status, for example, the second job scheduled on December 19, 2012 in the **Planned period** field.</span></span> <span data-ttu-id="a326a-129">Bu durumda işi planlanan dönem içinde taşıyın.</span><span class="sxs-lookup"><span data-stu-id="a326a-129">Then move the job within the planned period.</span></span> 

2. <span data-ttu-id="a326a-130">**İleri**'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="a326a-130">Click **Forward**.</span></span> <span data-ttu-id="a326a-131">İşin listede bir satır aşağıya taşındığına dikkat edin.</span><span class="sxs-lookup"><span data-stu-id="a326a-131">Notice that the job is moved one line down on the list.</span></span> 

3. <span data-ttu-id="a326a-132">**Geri**'yi tıklatın.</span><span class="sxs-lookup"><span data-stu-id="a326a-132">Click **Backward**.</span></span> <span data-ttu-id="a326a-133">İşin listede bir satır yukarıya taşındığına dikkat edin.</span><span class="sxs-lookup"><span data-stu-id="a326a-133">Notice that the job is moved one line up on the list.</span></span>
