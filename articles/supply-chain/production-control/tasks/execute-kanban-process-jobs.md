---
title: Kanban işlem işlerini yürütme
description: Bu prosedür, kanban proses işlerinin yürütülmesiyle ilgilidir.
author: ChristianRytt
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KanbanBoardWorkCell, KanbanJobStatusUpdate
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 08fddd6404bf835283adaca14ad7ceb851f5a489
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/01/2019
ms.locfileid: "1837650"
---
# <a name="execute-kanban-process-jobs"></a><span data-ttu-id="a7348-103">Kanban işlem işlerini yürütme</span><span class="sxs-lookup"><span data-stu-id="a7348-103">Execute kanban process jobs</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="a7348-104">Bu prosedür, kanban proses işlerinin yürütülmesiyle ilgilidir.</span><span class="sxs-lookup"><span data-stu-id="a7348-104">This procedure focuses on executing kanban process jobs.</span></span> <span data-ttu-id="a7348-105">İlk iş, beklenen miktar ile tamamlanır ve hiçbir hata alınmaz.</span><span class="sxs-lookup"><span data-stu-id="a7348-105">The first job is completed with the expected quantity and has no errors.</span></span> <span data-ttu-id="a7348-106">İkinci iş bir takım hatalarla tamamlanır.</span><span class="sxs-lookup"><span data-stu-id="a7348-106">The second job is completed with errors.</span></span> <span data-ttu-id="a7348-107">Bu yöntemi oluşturmak için kullanılan demo veri şirketi USMF'dir.</span><span class="sxs-lookup"><span data-stu-id="a7348-107">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="a7348-108">Bu yordam makine operatörü için hazırlanmıştır.</span><span class="sxs-lookup"><span data-stu-id="a7348-108">This procedure is intended for the machine operator.</span></span>


## <a name="select-a-kanban-job"></a><span data-ttu-id="a7348-109">Bir kanban işi seçin.</span><span class="sxs-lookup"><span data-stu-id="a7348-109">Select a kanban job</span></span>
1. <span data-ttu-id="a7348-110">Üretim kontrolü > Kanban > İş işlemleri için kanban kartı'na gidin.</span><span class="sxs-lookup"><span data-stu-id="a7348-110">Go to Production control > Kanban > Kanban board for process jobs.</span></span>
2. <span data-ttu-id="a7348-111">İş hücresi alanında, açılır menü düğmesine tıklayarak aramayı açın.</span><span class="sxs-lookup"><span data-stu-id="a7348-111">In the Work cell field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="a7348-112">1250 kaynak grubunun bulunduğu sırayı tıklayın.</span><span class="sxs-lookup"><span data-stu-id="a7348-112">Click the row with resource group 1250.</span></span> <span data-ttu-id="a7348-113">Böylece, İş listesi filtrelenerek sadece 1250 iş hücresi için olan işler görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="a7348-113">This filters the Jobs list to display only the jobs for work cell 1250.</span></span>
    * <span data-ttu-id="a7348-114">Planlı iş durumuna sahip sırayı işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="a7348-114">Mark the row that has the Planned job status.</span></span>  

## <a name="complete-a-job-with-expected-quantity"></a><span data-ttu-id="a7348-115">Bir işi beklenen miktarla tamamlama</span><span class="sxs-lookup"><span data-stu-id="a7348-115">Complete a job with expected quantity</span></span>
1. <span data-ttu-id="a7348-116">Ayrıntılar bölümünü genişletin veya daraltın.</span><span class="sxs-lookup"><span data-stu-id="a7348-116">Expand or collapse the Details section.</span></span>
    * <span data-ttu-id="a7348-117">Bu bölümde kart numarası, madde numarası, sipariş edilen miktar ve etkinlik adı hakkında önemli bilgiler verilmiştir.</span><span class="sxs-lookup"><span data-stu-id="a7348-117">This section displays important information about card number, item number, quantity ordered, and activity name.</span></span>  
2. <span data-ttu-id="a7348-118">Üretim talimatları bölümünü genişletin veya daraltın.</span><span class="sxs-lookup"><span data-stu-id="a7348-118">Expand or collapse the Production instructions section.</span></span>
    * <span data-ttu-id="a7348-119">Bu bölümde etkinlik için üretim talimatları verilmiştir.</span><span class="sxs-lookup"><span data-stu-id="a7348-119">This section displays production instructions for the activity.</span></span> <span data-ttu-id="a7348-120">Talimatlar metin, resim, çizim ve diğer belge türlerinde olabilir.</span><span class="sxs-lookup"><span data-stu-id="a7348-120">The instructions can be text, pictures, drawings, and other documents.</span></span>  
3. <span data-ttu-id="a7348-121">Başlat'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="a7348-121">Click Start.</span></span>
    * <span data-ttu-id="a7348-122">Tamamlanmamış bir iş seçin.</span><span class="sxs-lookup"><span data-stu-id="a7348-122">Select a job that is not completed.</span></span> <span data-ttu-id="a7348-123">İş durumunu görüntülemek için İş durumu alanındaki durum simgelerini kullanın.</span><span class="sxs-lookup"><span data-stu-id="a7348-123">Use status icons in the Job status field to view job status.</span></span>      
4. <span data-ttu-id="a7348-124">Tamamla öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="a7348-124">Click Complete.</span></span>
    * <span data-ttu-id="a7348-125">İş, beklenen miktarla tamamlanır.</span><span class="sxs-lookup"><span data-stu-id="a7348-125">The job is completed with the expected quality.</span></span>  

## <a name="complete-a-job-with-errors"></a><span data-ttu-id="a7348-126">Bir işi hatalarla tamamlama</span><span class="sxs-lookup"><span data-stu-id="a7348-126">Complete a job with errors</span></span>
1. <span data-ttu-id="a7348-127">Başlat'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="a7348-127">Click Start.</span></span>
    * <span data-ttu-id="a7348-128">Bir iş tamamlandığında listedeki bir sonraki iş otomatik olarak seçilir.</span><span class="sxs-lookup"><span data-stu-id="a7348-128">When a job is completed, the next job on the list is selected automatically.</span></span> <span data-ttu-id="a7348-129">Bu nedenle, Başlat düğmesini tıklamadan önce bir iş seçmenize gerek yoktur.</span><span class="sxs-lookup"><span data-stu-id="a7348-129">This is why you don't need to select a job before you click Start.</span></span>  
2. <span data-ttu-id="a7348-130">Eylem Bölmesinde, Üretim öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="a7348-130">On the Action Pane, click Manufacture.</span></span>
3. <span data-ttu-id="a7348-131">Tamamla (ayrıntılar) düğmesini tıklayın.</span><span class="sxs-lookup"><span data-stu-id="a7348-131">Click Complete (details).</span></span>
4. <span data-ttu-id="a7348-132">Listede, seçili satırı işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="a7348-132">In the list, mark the selected row.</span></span>
5. <span data-ttu-id="a7348-133">Hata miktarı alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="a7348-133">In the Error quantity field, enter a number.</span></span>
6. <span data-ttu-id="a7348-134">İyi miktar alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="a7348-134">In the Good quantity field, enter a number.</span></span>
7. <span data-ttu-id="a7348-135">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="a7348-135">Click OK.</span></span>

