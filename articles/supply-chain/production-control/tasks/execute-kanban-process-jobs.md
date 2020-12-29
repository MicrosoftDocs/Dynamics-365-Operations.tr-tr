---
title: Kanban işlem işlerini yürütme
description: Bu prosedür, kanban proses işlerinin yürütülmesiyle ilgilidir.
author: ChristianRytt
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KanbanBoardWorkCell, KanbanJobStatusUpdate
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a1c32b577007c400f3528a110436eb97aaabefe2
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "4439345"
---
# <a name="execute-kanban-process-jobs"></a><span data-ttu-id="2aa00-103">Kanban işlem işlerini yürütme</span><span class="sxs-lookup"><span data-stu-id="2aa00-103">Execute kanban process jobs</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="2aa00-104">Bu prosedür, kanban proses işlerinin yürütülmesiyle ilgilidir.</span><span class="sxs-lookup"><span data-stu-id="2aa00-104">This procedure focuses on executing kanban process jobs.</span></span> <span data-ttu-id="2aa00-105">İlk iş, beklenen miktar ile tamamlanır ve hiçbir hata alınmaz.</span><span class="sxs-lookup"><span data-stu-id="2aa00-105">The first job is completed with the expected quantity and has no errors.</span></span> <span data-ttu-id="2aa00-106">İkinci iş bir takım hatalarla tamamlanır.</span><span class="sxs-lookup"><span data-stu-id="2aa00-106">The second job is completed with errors.</span></span> <span data-ttu-id="2aa00-107">Bu yöntemi oluşturmak için kullanılan demo veri şirketi USMF'dir.</span><span class="sxs-lookup"><span data-stu-id="2aa00-107">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="2aa00-108">Bu yordam makine operatörü için hazırlanmıştır.</span><span class="sxs-lookup"><span data-stu-id="2aa00-108">This procedure is intended for the machine operator.</span></span>


## <a name="select-a-kanban-job"></a><span data-ttu-id="2aa00-109">Bir kanban işi seçin.</span><span class="sxs-lookup"><span data-stu-id="2aa00-109">Select a kanban job</span></span>
1. <span data-ttu-id="2aa00-110">Üretim kontrolü > Kanban > İş işlemleri için kanban kartı'na gidin.</span><span class="sxs-lookup"><span data-stu-id="2aa00-110">Go to Production control > Kanban > Kanban board for process jobs.</span></span>
2. <span data-ttu-id="2aa00-111">İş hücresi alanında, açılır menü düğmesine tıklayarak aramayı açın.</span><span class="sxs-lookup"><span data-stu-id="2aa00-111">In the Work cell field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="2aa00-112">1250 kaynak grubunun bulunduğu sırayı tıklayın.</span><span class="sxs-lookup"><span data-stu-id="2aa00-112">Click the row with resource group 1250.</span></span> <span data-ttu-id="2aa00-113">Böylece, İş listesi filtrelenerek sadece 1250 iş hücresi için olan işler görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="2aa00-113">This filters the Jobs list to display only the jobs for work cell 1250.</span></span>
    * <span data-ttu-id="2aa00-114">Planlı iş durumuna sahip sırayı işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="2aa00-114">Mark the row that has the Planned job status.</span></span>  

## <a name="complete-a-job-with-expected-quantity"></a><span data-ttu-id="2aa00-115">Bir işi beklenen miktarla tamamlama</span><span class="sxs-lookup"><span data-stu-id="2aa00-115">Complete a job with expected quantity</span></span>
1. <span data-ttu-id="2aa00-116">Ayrıntılar bölümünü genişletin veya daraltın.</span><span class="sxs-lookup"><span data-stu-id="2aa00-116">Expand or collapse the Details section.</span></span>
    * <span data-ttu-id="2aa00-117">Bu bölümde kart numarası, madde numarası, sipariş edilen miktar ve etkinlik adı hakkında önemli bilgiler verilmiştir.</span><span class="sxs-lookup"><span data-stu-id="2aa00-117">This section displays important information about card number, item number, quantity ordered, and activity name.</span></span>  
2. <span data-ttu-id="2aa00-118">Üretim talimatları bölümünü genişletin veya daraltın.</span><span class="sxs-lookup"><span data-stu-id="2aa00-118">Expand or collapse the Production instructions section.</span></span>
    * <span data-ttu-id="2aa00-119">Bu bölümde etkinlik için üretim talimatları verilmiştir.</span><span class="sxs-lookup"><span data-stu-id="2aa00-119">This section displays production instructions for the activity.</span></span> <span data-ttu-id="2aa00-120">Talimatlar metin, resim, çizim ve diğer belge türlerinde olabilir.</span><span class="sxs-lookup"><span data-stu-id="2aa00-120">The instructions can be text, pictures, drawings, and other documents.</span></span>  
3. <span data-ttu-id="2aa00-121">Başlat'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="2aa00-121">Click Start.</span></span>
    * <span data-ttu-id="2aa00-122">Tamamlanmamış bir iş seçin.</span><span class="sxs-lookup"><span data-stu-id="2aa00-122">Select a job that is not completed.</span></span> <span data-ttu-id="2aa00-123">İş durumunu görüntülemek için İş durumu alanındaki durum simgelerini kullanın.</span><span class="sxs-lookup"><span data-stu-id="2aa00-123">Use status icons in the Job status field to view job status.</span></span>      
4. <span data-ttu-id="2aa00-124">Tamamla öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="2aa00-124">Click Complete.</span></span>
    * <span data-ttu-id="2aa00-125">İş, beklenen miktarla tamamlanır.</span><span class="sxs-lookup"><span data-stu-id="2aa00-125">The job is completed with the expected quality.</span></span>  

## <a name="complete-a-job-with-errors"></a><span data-ttu-id="2aa00-126">Bir işi hatalarla tamamlama</span><span class="sxs-lookup"><span data-stu-id="2aa00-126">Complete a job with errors</span></span>
1. <span data-ttu-id="2aa00-127">Başlat'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="2aa00-127">Click Start.</span></span>
    * <span data-ttu-id="2aa00-128">Bir iş tamamlandığında listedeki bir sonraki iş otomatik olarak seçilir.</span><span class="sxs-lookup"><span data-stu-id="2aa00-128">When a job is completed, the next job on the list is selected automatically.</span></span> <span data-ttu-id="2aa00-129">Bu nedenle, Başlat düğmesini tıklamadan önce bir iş seçmenize gerek yoktur.</span><span class="sxs-lookup"><span data-stu-id="2aa00-129">This is why you don't need to select a job before you click Start.</span></span>  
2. <span data-ttu-id="2aa00-130">Eylem Bölmesinde, Üretim öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="2aa00-130">On the Action Pane, click Manufacture.</span></span>
3. <span data-ttu-id="2aa00-131">Tamamla (ayrıntılar) düğmesini tıklayın.</span><span class="sxs-lookup"><span data-stu-id="2aa00-131">Click Complete (details).</span></span>
4. <span data-ttu-id="2aa00-132">Listede, seçili satırı işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="2aa00-132">In the list, mark the selected row.</span></span>
5. <span data-ttu-id="2aa00-133">Hata miktarı alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="2aa00-133">In the Error quantity field, enter a number.</span></span>
6. <span data-ttu-id="2aa00-134">İyi miktar alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="2aa00-134">In the Good quantity field, enter a number.</span></span>
7. <span data-ttu-id="2aa00-135">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="2aa00-135">Click OK.</span></span>

