---
title: Satış olayı kanban kuralı oluşturma
description: Bu yordam, satış siparişi oluşturma sırasında tetiklenecek bir kanban kuralı oluşturmak için gereken ayarlara odaklanır.
author: ChristianRytt
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: KanbanRules, LeanProductionFlowActivityLookup, InventItemIdLookupSimple, SalesTableListPage, SalesCreateOrder, SalesTable, LeanPeggingTree
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 9325bbb8d28587baeb60cdf1fc37121c236f1a10
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/01/2021
ms.locfileid: "5828934"
---
# <a name="create-a-sales-event-kanban-rule"></a><span data-ttu-id="ab20c-103">Satış olayı kanban kuralı oluşturma</span><span class="sxs-lookup"><span data-stu-id="ab20c-103">Create a sales event kanban rule</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="ab20c-104">Bu yordam, satış siparişi oluşturma sırasında tetiklenecek bir kanban kuralı oluşturmak için gereken ayarlara odaklanır.</span><span class="sxs-lookup"><span data-stu-id="ab20c-104">This procedure focuses on the setup needed to create a kanban rule that is triggered during sales order creation.</span></span> <span data-ttu-id="ab20c-105">Olay kanbanı kuralı, satış siparişi satırlarından kaynaklanan gereksinimleri yeniler.</span><span class="sxs-lookup"><span data-stu-id="ab20c-105">The event kanban rule replenishes requirements that originate from sales order lines.</span></span> <span data-ttu-id="ab20c-106">Bu yöntemi oluşturmak için kullanılan demo veri şirketi USMF'dir.</span><span class="sxs-lookup"><span data-stu-id="ab20c-106">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="ab20c-107">Yeni veya değiştirilmiş bir ürünün üretimine hazırlanırken kullanılması için işlem mühendisi veya değer akışı yöneticisi için hazırlanmıştır.</span><span class="sxs-lookup"><span data-stu-id="ab20c-107">It is intended for the process engineer or the value stream manager as they prepare production of a new or modified product.</span></span>




## <a name="create-a-new-kanban-rule"></a><span data-ttu-id="ab20c-108">Yeni bir kanban kuralı oluştur</span><span class="sxs-lookup"><span data-stu-id="ab20c-108">Create a new kanban rule</span></span>
1. <span data-ttu-id="ab20c-109">Kanban kuralları'na gidin.</span><span class="sxs-lookup"><span data-stu-id="ab20c-109">Go to Kanban rules.</span></span>
2. <span data-ttu-id="ab20c-110">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ab20c-110">Click New.</span></span>
3. <span data-ttu-id="ab20c-111">Yenileme stratejisi alanında 'Olay' öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="ab20c-111">In the Replenishment strategy field, select 'Event'.</span></span>
    * <span data-ttu-id="ab20c-112">Olay seçilmesi, kanban kuralının bir olay tarafından (örneğin, bir satış siparişi satırı oluşturulması) tetikleneceği anlamına gelir.</span><span class="sxs-lookup"><span data-stu-id="ab20c-112">Selecting Event means that the kanban rule is triggered by an event, for example, creation of a sales order line.</span></span>   <span data-ttu-id="ab20c-113">Bu, her bir kanbanın belirli bir isteği kapsaması gereken alanlara uygulanır.</span><span class="sxs-lookup"><span data-stu-id="ab20c-113">This is applied to areas where each kanban should cover a specific demand.</span></span>  
4. <span data-ttu-id="ab20c-114">İlk plan alanında bir değer girin veya bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="ab20c-114">In the First plan activity field, enter or select a value.</span></span>
    * <span data-ttu-id="ab20c-115">Son Derleme öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="ab20c-115">Select Final assembly.</span></span>  
5. <span data-ttu-id="ab20c-116">Ayrıntılar bölümünü genişletin.</span><span class="sxs-lookup"><span data-stu-id="ab20c-116">Expand the Details section.</span></span>
6. <span data-ttu-id="ab20c-117">Ürün alanında bir değer girin veya bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="ab20c-117">In the Product field, enter or select a value.</span></span>
    * <span data-ttu-id="ab20c-118">L0050 öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="ab20c-118">Select L0050.</span></span>  

## <a name="define-an-event"></a><span data-ttu-id="ab20c-119">Bir olay tanımla</span><span class="sxs-lookup"><span data-stu-id="ab20c-119">Define an event</span></span>
1. <span data-ttu-id="ab20c-120">Olaylat bölümünü genişletin.</span><span class="sxs-lookup"><span data-stu-id="ab20c-120">Expand the Events section.</span></span>
2. <span data-ttu-id="ab20c-121">Satış olayı alanında 'Otomatik' öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="ab20c-121">In the Sales event field, select 'Automatic'.</span></span>
    * <span data-ttu-id="ab20c-122">Satış olayı Otomatik olarak seçilerek, bir satış satırı ürün ve giriş konumuyla eşleştiğinde bu kanban kuralı otomatik olarak tetiklenir.</span><span class="sxs-lookup"><span data-stu-id="ab20c-122">By selecting the sales event Automatic, this kanban rule will be triggered automatically when a sales line matches the product and receipt location.</span></span> <span data-ttu-id="ab20c-123">Bu yordamda, ambar 13'te ürün L0050'dir.</span><span class="sxs-lookup"><span data-stu-id="ab20c-123">In this procedure, it is product L0050 on warehouse 13.</span></span>  
3. <span data-ttu-id="ab20c-124">Minimum olay miktarını '50' olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="ab20c-124">Set Minimum event quantity to '50'.</span></span>
    * <span data-ttu-id="ab20c-125">50 minimum olay miktarı ile, kanban kuralı yalnızca 50 veya daha fazla bir miktarda olay olduğunda tetiklenir.</span><span class="sxs-lookup"><span data-stu-id="ab20c-125">With a minimum event quantity of 50, the kanban rule will only be triggered by events with a quantity of 50 or more.</span></span>  
4. <span data-ttu-id="ab20c-126">Üretim akışı bölümünü genişletin.</span><span class="sxs-lookup"><span data-stu-id="ab20c-126">Expand the Production flow section.</span></span>
    * <span data-ttu-id="ab20c-127">Giriş konumunun ambar 13 olduğuna dikkat edin.</span><span class="sxs-lookup"><span data-stu-id="ab20c-127">Notice that the Receipt location is warehouse 13.</span></span> <span data-ttu-id="ab20c-128">Bunun anlamı kanban kuralın bu konum için tetikleneceğidir.</span><span class="sxs-lookup"><span data-stu-id="ab20c-128">This means that this kanban rule will be triggered for this location.</span></span>  
    * <span data-ttu-id="ab20c-129">Bu örnekte, ambar 13'te bulunan 50 veya daha fazla miktardaki L0050 ürünü bu kanban kuralını tetikler.</span><span class="sxs-lookup"><span data-stu-id="ab20c-129">In this example, a sales line for product L0050, with a quantity of 50 or more, on warehouse 13, will trigger this kanban rule.</span></span>  

## <a name="create-sales-line-to-trigger-event-kanban-rule"></a><span data-ttu-id="ab20c-130">Olay kanbanı kuralı tetiklemek için satış satırı oluştur</span><span class="sxs-lookup"><span data-stu-id="ab20c-130">Create sales line to trigger event kanban rule</span></span>
1. <span data-ttu-id="ab20c-131">Tüm satış siparişleri'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="ab20c-131">Go to All sales orders.</span></span>
    * <span data-ttu-id="ab20c-132">Kanban kuralı kaydedildiğinde bir uyarı gösterilir, bunun anlamı kanbanların satış siparişi oluşturma sırasında gerçek zamanlı oluşturulacağıdır.</span><span class="sxs-lookup"><span data-stu-id="ab20c-132">A warning is shown when the kanban rule is saved, which means that kanbans will be created in real-time during sales order creation.</span></span>  
2. <span data-ttu-id="ab20c-133">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ab20c-133">Click New.</span></span>
3. <span data-ttu-id="ab20c-134">Müşteri hesabı alanında bir değer girin veya seçin.</span><span class="sxs-lookup"><span data-stu-id="ab20c-134">In the Customer account field, enter or select a value.</span></span>
    * <span data-ttu-id="ab20c-135">Örneğin, ABD-003 öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="ab20c-135">For example, select US-003.</span></span>  
4. <span data-ttu-id="ab20c-136">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ab20c-136">Click OK.</span></span>
5. <span data-ttu-id="ab20c-137">Madde numarası alanına 'L0050' girin.</span><span class="sxs-lookup"><span data-stu-id="ab20c-137">In the Item number field, type 'L0050'.</span></span>
6. <span data-ttu-id="ab20c-138">Tesis alanında '1' girin.</span><span class="sxs-lookup"><span data-stu-id="ab20c-138">In the Site field, type '1'.</span></span>
    * <span data-ttu-id="ab20c-139">Ambar 13 Site 1'de olduğundan Site 1'i seçin.</span><span class="sxs-lookup"><span data-stu-id="ab20c-139">Select Site 1 because Warehouse 13 is on Site 1.</span></span>  
7. <span data-ttu-id="ab20c-140">Ambar alanında bir değer girin veya bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="ab20c-140">In the Warehouse field, enter or select a value.</span></span>
    * <span data-ttu-id="ab20c-141">Ambar'ı 13 olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="ab20c-141">Set Warehouse to 13.</span></span>  
8. <span data-ttu-id="ab20c-142">Miktarı '75' olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="ab20c-142">Set Quantity to '75'.</span></span>
    * <span data-ttu-id="ab20c-143">Oluşturulan kanban kuralını tetiklemek için 50 veya daha yüksek değerde miktar girin.</span><span class="sxs-lookup"><span data-stu-id="ab20c-143">Enter a quantity of 50 or greater, to trigger the created kanban rule.</span></span>  

## <a name="verify-that-kanban-is-created"></a><span data-ttu-id="ab20c-144">Kanbanın oluşturulduğunu doğrula</span><span class="sxs-lookup"><span data-stu-id="ab20c-144">Verify that kanban is created</span></span>
1. <span data-ttu-id="ab20c-145">Ürün ve tedarik seçeneğine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ab20c-145">Click Product and supply.</span></span>
2. <span data-ttu-id="ab20c-146">İlişkilendirme ağacını görüntüle'yi tıklatın.</span><span class="sxs-lookup"><span data-stu-id="ab20c-146">Click View pegging tree.</span></span>
    * <span data-ttu-id="ab20c-147">Satış satırıyla aynı miktara sahip bir kanban oluşturulduğuna dikkat edin.</span><span class="sxs-lookup"><span data-stu-id="ab20c-147">Notice that a kanban with the same quantity as the sales line is created.</span></span> <span data-ttu-id="ab20c-148">L0050 üretmek için gereken malzeme sorunlarını da görebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="ab20c-148">You can also see the material issues needed to produce L0050.</span></span> <span data-ttu-id="ab20c-149">Bu yordamın son aşamasıdır.</span><span class="sxs-lookup"><span data-stu-id="ab20c-149">This is the last step in this procedure.</span></span>  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]