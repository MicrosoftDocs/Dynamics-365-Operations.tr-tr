--- 
title: "Kanban satır olayı kullanarak kanban kuralı oluşturma"
description: "Bu yordam, bir işlem etkinliğinden çekmeyi tetiklemek için kanban satır olayı ayarını kullanarak bir kanban kuralı oluşturur."
author: ChristianRytt
manager: AnnBe
ms.date: 08/24/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 9ef7b8e920d22cbc4f96676e68a263f2da7f232c
ms.contentlocale: tr-tr
ms.lasthandoff: 08/29/2017

---
# <a name="create-a-kanban-rule-using-a-kanban-line-event"></a><span data-ttu-id="b0b58-103">Kanban satır olayı kullanarak kanban kuralı oluşturma</span><span class="sxs-lookup"><span data-stu-id="b0b58-103">Create a kanban rule using a kanban line event</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="b0b58-104">Bu yordam, bir işlem etkinliğinden çekmeyi tetiklemek için kanban satır olayı ayarını kullanarak bir kanban kuralı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="b0b58-104">This procedure creates a kanban rule by using the kanban line event setting to trigger pull from a process activity.</span></span> <span data-ttu-id="b0b58-105">Miktarın 25'e eşit veya 25'ten daha büyük olduğu her durumda kanban kuralı, bir kanban işlem etkinliği tarafından tetiklenir.</span><span class="sxs-lookup"><span data-stu-id="b0b58-105">The kanban rule is triggered by a kanban process activity, with a quantity equal to or greater than 25 each.</span></span> <span data-ttu-id="b0b58-106">Bu görevi oluşturmak için kullanılan demo veri şirketi USMF'dir.</span><span class="sxs-lookup"><span data-stu-id="b0b58-106">The demo data company used to create this task is USMF.</span></span> <span data-ttu-id="b0b58-107">Bu görev, yalın bir ortamda yeni veya değiştirilmiş bir ürünün üretimine hazırlanırken kullanılması için işlem mühendisi veya değer akışı yöneticisi için hazırlanmıştır.</span><span class="sxs-lookup"><span data-stu-id="b0b58-107">This task is intended for the process engineer or the value stream manager, as they prepare production of a new or modified product in a lean environment.</span></span>


## <a name="create-a-kanban-rule"></a><span data-ttu-id="b0b58-108">Kanban kuralı oluşturun</span><span class="sxs-lookup"><span data-stu-id="b0b58-108">Create a kanban rule</span></span>
1. <span data-ttu-id="b0b58-109">Ürün bilgi yönetimi > Yalın imalat > Kanban kuralları'na gidin.</span><span class="sxs-lookup"><span data-stu-id="b0b58-109">Go to Product information management > Lean manufacturing > Kanban rules.</span></span>
2. <span data-ttu-id="b0b58-110">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="b0b58-110">Click New.</span></span>
3. <span data-ttu-id="b0b58-111">Yenileme stratejisi alanında 'Olay' öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="b0b58-111">In the Replenishment strategy field, select 'Event'.</span></span>
    * <span data-ttu-id="b0b58-112">Bu işlem talepten doğrudan kanbanlar oluşturur.</span><span class="sxs-lookup"><span data-stu-id="b0b58-112">This generates kanbans directly from demand.</span></span> <span data-ttu-id="b0b58-113">Siparişe göre üretim senaryosunu tanımlayan kuralları ayarlamak için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="b0b58-113">It is used to set up rules that define a make-to-order scenario.</span></span>  
4. <span data-ttu-id="b0b58-114">İlk plan alanında bir değer girin veya bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="b0b58-114">In the First plan activity field, enter or select a value.</span></span>
    * <span data-ttu-id="b0b58-115">SpeakerAssemblyAndPolish öğesini girin veya seçin.</span><span class="sxs-lookup"><span data-stu-id="b0b58-115">Enter or select SpeakerAssemblyAndPolish.</span></span> <span data-ttu-id="b0b58-116">Üretim kanban kuralının ilk etkinliği üretim akışında bir işleme etkinliğidir.</span><span class="sxs-lookup"><span data-stu-id="b0b58-116">The first activity of a manufacturing kanban rule is a process activity in the production flow.</span></span> <span data-ttu-id="b0b58-117">Bir etkinlik seçtiğinizde, etkinliğin geçerlilik tarihleri kanban kuralının geçerlilik tarihlerine kopyalanır.</span><span class="sxs-lookup"><span data-stu-id="b0b58-117">When you select the activity, the validity dates of the activity are copied to the validity dates of the kanban rule.</span></span>  
5. <span data-ttu-id="b0b58-118">Ayrıntılar bölümünü genişletin.</span><span class="sxs-lookup"><span data-stu-id="b0b58-118">Expand the Details section.</span></span>
6. <span data-ttu-id="b0b58-119">Ürün alanına "L0001" yazın.</span><span class="sxs-lookup"><span data-stu-id="b0b58-119">In the Product field, type 'L0001'.</span></span>
7. <span data-ttu-id="b0b58-120">Olaylat bölümünü genişletin.</span><span class="sxs-lookup"><span data-stu-id="b0b58-120">Expand the Events section.</span></span>
8. <span data-ttu-id="b0b58-121">Kanban satır olayı alanında "Otomatik" öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="b0b58-121">In the Kanban line event field, select 'Automatic'.</span></span>
    * <span data-ttu-id="b0b58-122">Bu işlem istek üzerinde olay kanbanları oluşturur.</span><span class="sxs-lookup"><span data-stu-id="b0b58-122">This generates event kanbans on demand.</span></span>  <span data-ttu-id="b0b58-123">Aşağı doğru işleme etkinliği için gerekli olan malzemeyi yenileyen kanban kurallarını yapılandırmak için bu alan kullanılır.</span><span class="sxs-lookup"><span data-stu-id="b0b58-123">The field is used to configure kanban rules that replenish material that is required for a downstream process activity.</span></span> <span data-ttu-id="b0b58-124">Otomatik'i seçtiğinizde taleple birlikte olay kanbanları oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="b0b58-124">When you select Automatic, the event kanbans are created with the demand.</span></span> <span data-ttu-id="b0b58-125">Üretimi aynı gün gerçekleştirmeyi bekliyorsanız bu ayar önerilir.</span><span class="sxs-lookup"><span data-stu-id="b0b58-125">This setting is recommended if you expect to execute production on the same day.</span></span>  
9. <span data-ttu-id="b0b58-126">Minimum olay miktarını '25' olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="b0b58-126">Set Minimum event quantity to '25'.</span></span>
    * <span data-ttu-id="b0b58-127">Olay kanbanları, talep miktarı bu alana eşit veya bu alandan fazla olduğunda oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="b0b58-127">Event kanbans are generated when the demand quantity is equal to or more than this field.</span></span> <span data-ttu-id="b0b58-128">Bu özellik, bir makinede bu alandan daha az sipariş miktarı ve başka bir makinede bu alandan daha fazla sipariş miktarı üretmek istediğinizde kullanışlıdır.</span><span class="sxs-lookup"><span data-stu-id="b0b58-128">This is useful if you want to produce an order quantity less than this field on one machine and more than this field on another machine.</span></span>  
10. <span data-ttu-id="b0b58-129">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="b0b58-129">Click Save.</span></span>

## <a name="create-sales-order-and-trigger-kanban-chain"></a><span data-ttu-id="b0b58-130">Satış siparişi oluşturun ve kanban zincirini tetikleyin</span><span class="sxs-lookup"><span data-stu-id="b0b58-130">Create sales order and trigger kanban chain</span></span>
1. <span data-ttu-id="b0b58-131">Sales and marketing > Sales orders > All sales orders (Satış ve pazarlama > Satış siparişleri > Tüm satış siparişleri) menüsüne gidin.</span><span class="sxs-lookup"><span data-stu-id="b0b58-131">Go to Sales and marketing > Sales orders > All sales orders.</span></span>
2. <span data-ttu-id="b0b58-132">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="b0b58-132">Click New.</span></span>
3. <span data-ttu-id="b0b58-133">Müşteri hesabı alanında bir değer girin veya seçin.</span><span class="sxs-lookup"><span data-stu-id="b0b58-133">In the Customer account field, enter or select a value.</span></span>
    * <span data-ttu-id="b0b58-134">US-003, Forest Wholesales Müşteri hesabını seçin.</span><span class="sxs-lookup"><span data-stu-id="b0b58-134">Select Customer account US-003, Forest Wholesales.</span></span>  
4. <span data-ttu-id="b0b58-135">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="b0b58-135">Click OK.</span></span>
5. <span data-ttu-id="b0b58-136">Madde numarası alanına 'L0001' girin.</span><span class="sxs-lookup"><span data-stu-id="b0b58-136">In the Item number field, type 'L0001'.</span></span>
    * <span data-ttu-id="b0b58-137">L0001, kanban kuralını oluşturduğunuz maddedir.</span><span class="sxs-lookup"><span data-stu-id="b0b58-137">L0001 is the item for which you created the kanban rule.</span></span>  
6. <span data-ttu-id="b0b58-138">Miktarı '27' olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="b0b58-138">Set Quantity to '27'.</span></span>
    * <span data-ttu-id="b0b58-139">Kanban kuralında 27, minimum miktar olan 25'ten daha büyük olduğundan bu bir olay kanbanını tetikler.</span><span class="sxs-lookup"><span data-stu-id="b0b58-139">Because 27 is higher than the minimum quantity of 25 on the kanban rule, this will trigger an event kanban.</span></span>  
7. <span data-ttu-id="b0b58-140">Tesis alanında '1' girin.</span><span class="sxs-lookup"><span data-stu-id="b0b58-140">In the Site field, type '1'.</span></span>
8. <span data-ttu-id="b0b58-141">Ambar alanında bir değer girin veya bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="b0b58-141">In the Warehouse field, enter or select a value.</span></span>
    * <span data-ttu-id="b0b58-142">Ambar 13'ü seçin.</span><span class="sxs-lookup"><span data-stu-id="b0b58-142">Select warehouse 13.</span></span>  
9. <span data-ttu-id="b0b58-143">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="b0b58-143">Click Save.</span></span>

## <a name="view-the-kanban-generated-by-the-kanban-rule"></a><span data-ttu-id="b0b58-144">Kanban kuralı tarafından oluşturulan kanbanı görüntüleyin</span><span class="sxs-lookup"><span data-stu-id="b0b58-144">View the kanban generated by the kanban rule</span></span>
1. <span data-ttu-id="b0b58-145">Ürün bilgi yönetimi > Yalın imalat > Kanban kuralları'na gidin.</span><span class="sxs-lookup"><span data-stu-id="b0b58-145">Go to Product information management > Lean manufacturing > Kanban rules.</span></span>
2. <span data-ttu-id="b0b58-146">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="b0b58-146">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="b0b58-147">Kanbanlar bölümünü genişletin.</span><span class="sxs-lookup"><span data-stu-id="b0b58-147">Expand the Kanbans section.</span></span>
    * <span data-ttu-id="b0b58-148">Oluşturulan kanban kuralına bağlı olarak etkinliği işlemek amacıyla 27 için bir kanban oluşturulduğuna dikkat edin.</span><span class="sxs-lookup"><span data-stu-id="b0b58-148">Notice that a kanban for 27 was created to process the  activity based on the created kanban rule.</span></span>  
    * <span data-ttu-id="b0b58-149">Bu son adımdır.</span><span class="sxs-lookup"><span data-stu-id="b0b58-149">This is the last step.</span></span>  


