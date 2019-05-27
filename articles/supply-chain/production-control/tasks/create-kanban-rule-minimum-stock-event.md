---
title: Minimum stok olayı kullanarak kanban kuralı oluşturma
description: Bu yordam, belirli bir ürünün her zaman belirli bir konumda bulunabilir olmasını sağlamak için bir minimum stok olayı kullanan bir kanban kuralı oluşturmak için gereken kuruluma odaklanır.
author: ChristianRytt
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KanbanRules, LeanProductionFlowActivityLookup, InventItemIdLookupSimple, EcoResProductInformationDialog, EcoResProductDetailsExtended, ReqItemTable, InventLocationIdLookup
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 2a9ba8ec2abb26e3b9ee7e14bdf882c1ffcb205b
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/15/2019
ms.locfileid: "1558538"
---
# <a name="create-a-kanban-rule-using-a-minimum-stock-event"></a><span data-ttu-id="b32a3-103">Minimum stok olayı kullanarak kanban kuralı oluşturma</span><span class="sxs-lookup"><span data-stu-id="b32a3-103">Create a kanban rule using a minimum stock event</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="b32a3-104">Bu yordam, belirli bir ürünün her zaman belirli bir konumda bulunabilir olmasını sağlamak için bir minimum stok olayı kullanan bir kanban kuralı oluşturmak için gereken kuruluma odaklanır.</span><span class="sxs-lookup"><span data-stu-id="b32a3-104">This procedure focuses on the setup needed to create a kanban rule using a minimum stock event to ensure that a specific product is always available at a specific location.</span></span> <span data-ttu-id="b32a3-105">Stok seviyesi 200 adedin altına düştüğünde konuma malzeme transfer etmek için bir kanban kuralı oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="b32a3-105">A kanban rule is created to transfer material to the location when the inventory level drops below 200 pieces.</span></span> <span data-ttu-id="b32a3-106">İlişkilendirme olayının işlenmesini çalıştırarak gerekli kanbanlar oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="b32a3-106">By running the Pegging event processing, the needed kanbans are created.</span></span> <span data-ttu-id="b32a3-107">Bu görevi oluşturmak için kullanılan demo veri şirketi USMF'dir.</span><span class="sxs-lookup"><span data-stu-id="b32a3-107">The demo data company used to create this task is USMF.</span></span> <span data-ttu-id="b32a3-108">Bu görev, yalın bir ortamda yeni veya değiştirilmiş bir ürünün üretimine hazırlanırken kullanılması için işlem mühendisi veya değer akışı yöneticisi için hazırlanmıştır.</span><span class="sxs-lookup"><span data-stu-id="b32a3-108">This task is intended for the process engineer or the value stream manager, as they prepare production of a new or modified product in a lean environment.</span></span>


## <a name="create-a-new-kanban-rule"></a><span data-ttu-id="b32a3-109">Yeni bir kanban kuralı oluştur</span><span class="sxs-lookup"><span data-stu-id="b32a3-109">Create a new kanban rule</span></span>
1. <span data-ttu-id="b32a3-110">Ürün bilgi yönetimi > Yalın imalat > Kanban kuralları'na gidin.</span><span class="sxs-lookup"><span data-stu-id="b32a3-110">Go to Product information management > Lean manufacturing > Kanban rules.</span></span>
2. <span data-ttu-id="b32a3-111">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="b32a3-111">Click New.</span></span>
3. <span data-ttu-id="b32a3-112">Tür alanından 'Çek' seçimini yapın.</span><span class="sxs-lookup"><span data-stu-id="b32a3-112">In the Type field, select 'Withdrawal'.</span></span>
    * <span data-ttu-id="b32a3-113">Transfer kanbanlarının oluşturulması için bu tür kullanılır.</span><span class="sxs-lookup"><span data-stu-id="b32a3-113">This type is used to create transfer kanbans.</span></span>  
4. <span data-ttu-id="b32a3-114">Yenileme stratejisi alanında 'Olay' öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="b32a3-114">In the Replenishment strategy field, select 'Event'.</span></span>
    * <span data-ttu-id="b32a3-115">Olay stratejisi, bir olaya göre kanbanların transferini oluşturmak için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="b32a3-115">The Event strategy is used to create the transfer kanbans based on an event.</span></span> <span data-ttu-id="b32a3-116">Bu yordamın sonraki bölümünde stok yenilemeyi kullanarak transfer kanbanları tetiklersiniz.</span><span class="sxs-lookup"><span data-stu-id="b32a3-116">Later in the procedure, you will trigger transfer kanbans by using stock replenishment.</span></span>  
5. <span data-ttu-id="b32a3-117">İlk plan alanında bir değer girin veya bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="b32a3-117">In the First plan activity field, enter or select a value.</span></span>
    * <span data-ttu-id="b32a3-118">ReplenishSpeakerComponents öğesini girin veya seçin.</span><span class="sxs-lookup"><span data-stu-id="b32a3-118">Enter or select ReplenishSpeakerComponents.</span></span> <span data-ttu-id="b32a3-119">Bu transfer faaliyeti, alıcı (çıkış) ambarına ve konum 12'ye sahiptir, bu da malzemelerin ambar 12'deki konum 12'ye taşınacağı anlamına gelir.</span><span class="sxs-lookup"><span data-stu-id="b32a3-119">This transfer activity has receipt (output) warehouse and location 12, which means that materials will be moved to location 12 in warehouse 12.</span></span>  
6. <span data-ttu-id="b32a3-120">Ayrıntılar bölümünü genişletin.</span><span class="sxs-lookup"><span data-stu-id="b32a3-120">Expand the Details section.</span></span>
7. <span data-ttu-id="b32a3-121">Ürün alanında bir değer girin veya bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="b32a3-121">In the Product field, enter or select a value.</span></span>
    * <span data-ttu-id="b32a3-122">M0007 öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="b32a3-122">Select M0007.</span></span>  
8. <span data-ttu-id="b32a3-123">Olaylat bölümünü genişletin.</span><span class="sxs-lookup"><span data-stu-id="b32a3-123">Expand the Events section.</span></span>
9. <span data-ttu-id="b32a3-124">Stok yenileme olayı alanında "Toplu İş" öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="b32a3-124">In the Stock replenishment event field, select 'Batch'.</span></span>
    * <span data-ttu-id="b32a3-125">Bu, İlişkilendirme olayının işlenmesi sırasında ilgili konumda gereken malzemenin karşılanması için kanbanlar oluşturur.</span><span class="sxs-lookup"><span data-stu-id="b32a3-125">This creates kanbans to fulfill material needs at the related location during Pegging event processing.</span></span>  

## <a name="set-the-minimum-quantity-for-the-item"></a><span data-ttu-id="b32a3-126">Madde için minimum miktarı ayarlayın</span><span class="sxs-lookup"><span data-stu-id="b32a3-126">Set the minimum quantity for the item</span></span>
1. <span data-ttu-id="b32a3-127">Ürün alanındaki bağlantıyı izlemek için tıklayın.</span><span class="sxs-lookup"><span data-stu-id="b32a3-127">Click to follow the link in the Product field.</span></span>
2. <span data-ttu-id="b32a3-128">Madde numarası alanındaki bağlantıyı izlemek için tıklayın.</span><span class="sxs-lookup"><span data-stu-id="b32a3-128">Click to follow the link in the Item number field.</span></span>
3. <span data-ttu-id="b32a3-129">Ürün resmi bilgi kutusunu genişletin.</span><span class="sxs-lookup"><span data-stu-id="b32a3-129">Expand the Product image FactBox.</span></span>
4. <span data-ttu-id="b32a3-130">Eylem Bölmesinde, Planla öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="b32a3-130">On the Action Pane, click Plan.</span></span>
5. <span data-ttu-id="b32a3-131">Madde kapsamı'na tıklayın.</span><span class="sxs-lookup"><span data-stu-id="b32a3-131">Click Item coverage.</span></span>
6. <span data-ttu-id="b32a3-132">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="b32a3-132">Click New.</span></span>
7. <span data-ttu-id="b32a3-133">Listede, seçili satırı işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="b32a3-133">In the list, mark the selected row.</span></span>
8. <span data-ttu-id="b32a3-134">Ambar alanında bir değer girin veya bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="b32a3-134">In the Warehouse field, enter or select a value.</span></span>
    * <span data-ttu-id="b32a3-135">Ambar'ı 12 olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="b32a3-135">Set Warehouse to 12.</span></span>  
9. <span data-ttu-id="b32a3-136">Minimumu "200" olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="b32a3-136">Set Minimum to '200'.</span></span>

## <a name="run-the-batch-event-creation-job"></a><span data-ttu-id="b32a3-137">Toplu olay oluşturma işini çalıştırın</span><span class="sxs-lookup"><span data-stu-id="b32a3-137">Run the batch event creation job</span></span>
1. <span data-ttu-id="b32a3-138">Üretim kontrolü > Dönemsel görevler > Kanban işi toplu işlemi > İlişkilendirme olayının işlenmesi'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="b32a3-138">Go to Production control > Periodic tasks > Kanban job batch processing > Pegging event processing.</span></span>
2. <span data-ttu-id="b32a3-139">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="b32a3-139">Click OK.</span></span>
3. <span data-ttu-id="b32a3-140">Ürün bilgi yönetimi > Yalın imalat > Kanban kuralları'na gidin.</span><span class="sxs-lookup"><span data-stu-id="b32a3-140">Go to Product information management > Lean manufacturing > Kanban rules.</span></span>
4. <span data-ttu-id="b32a3-141">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="b32a3-141">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="b32a3-142">Daha önce oluşturduğunuz kanban kuralını seçin.</span><span class="sxs-lookup"><span data-stu-id="b32a3-142">Select the kanban rule that you created earlier.</span></span>  
5. <span data-ttu-id="b32a3-143">Kanbanlar bölümünü genişletin.</span><span class="sxs-lookup"><span data-stu-id="b32a3-143">Expand the Kanbans section.</span></span>
    * <span data-ttu-id="b32a3-144">Gerekli malzemeyi ambar 12'ye transfer etmek için bir kanban oluşturulduğuna dikkat edin.</span><span class="sxs-lookup"><span data-stu-id="b32a3-144">Notice that a kanban was created to transfer the needed material to warehouse 12.</span></span>  

