---
title: Birden fazla faaliyet için kanban kuralı oluşturma
description: Bu yordam, bir üretim akışından birden fazla faaliyeti içeren bir kanban kuralının nasıl oluşturulacağını gösterir.
author: ChristianRytt
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KanbanRules, LeanProductionFlowActivityLookup, KanbanFlowSelection, InventItemIdLookupSimple, KanbanCreateScheduled, Kanban
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 3c25d47a78d1cc91ee2625ef628d7b9ba345b097
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/15/2021
ms.locfileid: "4977925"
---
# <a name="create-a-kanban-rule-for-multiple-activities"></a><span data-ttu-id="fa8ee-103">Birden fazla faaliyet için kanban kuralı oluşturma</span><span class="sxs-lookup"><span data-stu-id="fa8ee-103">Create a kanban rule for multiple activities</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="fa8ee-104">Bu yordam, bir üretim akışından birden fazla faaliyeti içeren bir kanban kuralının nasıl oluşturulacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="fa8ee-104">This procedure shows how to create a kanban rule that includes multiple activities from a production flow.</span></span> <span data-ttu-id="fa8ee-105">Bu görevi oluşturmak için kullanılan demo veri şirketi USMF'dir.</span><span class="sxs-lookup"><span data-stu-id="fa8ee-105">The demo data company used to create this task is USMF.</span></span> <span data-ttu-id="fa8ee-106">Bu görev, yalın bir ortamda yeni veya değiştirilmiş bir ürünün üretimine hazırlanırken kullanılması için işlem mühendisi veya değer akışı yöneticisi için hazırlanmıştır.</span><span class="sxs-lookup"><span data-stu-id="fa8ee-106">This task is intended for the process engineer or the value stream manager, as they prepare production of a new or modified product in a lean environment.</span></span>


## <a name="create-a-new-kanban-rule"></a><span data-ttu-id="fa8ee-107">Yeni bir kanban kuralı oluştur</span><span class="sxs-lookup"><span data-stu-id="fa8ee-107">Create a new kanban rule</span></span>
1. <span data-ttu-id="fa8ee-108">Ürün bilgi yönetimi > Yalın imalat > Kanban kuralları'na gidin.</span><span class="sxs-lookup"><span data-stu-id="fa8ee-108">Go to Product information management > Lean manufacturing > Kanban rules.</span></span>
2. <span data-ttu-id="fa8ee-109">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="fa8ee-109">Click New.</span></span>
3. <span data-ttu-id="fa8ee-110">Stok yenileme stratejisi alanında "Planlandı"yı seçin.</span><span class="sxs-lookup"><span data-stu-id="fa8ee-110">In the Replenishment strategy field, select 'Scheduled'.</span></span>
4. <span data-ttu-id="fa8ee-111">İlk plan alanında bir değer girin veya bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="fa8ee-111">In the First plan activity field, enter or select a value.</span></span>
    * <span data-ttu-id="fa8ee-112">SpeakerAssemblyAndPolish öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="fa8ee-112">Select SpeakerAssemblyAndPolish.</span></span>  
5. <span data-ttu-id="fa8ee-113">Birden çok faaliyet onay kutusunu seçin.</span><span class="sxs-lookup"><span data-stu-id="fa8ee-113">Select the Multiple activities check box.</span></span>
    * <span data-ttu-id="fa8ee-114">Amaç kanban kuralında birden fazla faaliyet içermektir.</span><span class="sxs-lookup"><span data-stu-id="fa8ee-114">The purpose is to include more than one activity in the kanban rule.</span></span> <span data-ttu-id="fa8ee-115">En son planlı faaliyeti seçtiğinizde üretim akışında bir yol seçersiniz.</span><span class="sxs-lookup"><span data-stu-id="fa8ee-115">You choose a path in the production flow when you select the last plan activity.</span></span>  
6. <span data-ttu-id="fa8ee-116">Son plan faaliyeti alanına bir değer girin veya bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="fa8ee-116">In the Last plan activity field, enter or select a value.</span></span>
    * <span data-ttu-id="fa8ee-117">SpeakerTestAndPackaging öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="fa8ee-117">Select SpeakerTestAndPackaging.</span></span> <span data-ttu-id="fa8ee-118">Değeri seçtikten sonra otomatik olarak bir sayfa açılır.</span><span class="sxs-lookup"><span data-stu-id="fa8ee-118">After you select the value, a page automatically opens.</span></span> <span data-ttu-id="fa8ee-119">Kanban akışı SpeakerAssemblyAndPolish > SpeakerTestAndPackaging öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="fa8ee-119">Select the kanban flow SpeakerAssemblyAndPolish > SpeakerTestAndPackaging.</span></span> <span data-ttu-id="fa8ee-120">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="fa8ee-120">Click OK.</span></span>  
7. <span data-ttu-id="fa8ee-121">Ayrıntılar bölümünü genişletin.</span><span class="sxs-lookup"><span data-stu-id="fa8ee-121">Expand the Details section.</span></span>
8. <span data-ttu-id="fa8ee-122">Ürün alanında bir değer girin veya bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="fa8ee-122">In the Product field, enter or select a value.</span></span>
    * <span data-ttu-id="fa8ee-123">Madde L0006'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="fa8ee-123">Select Item L0006.</span></span>  

## <a name="create-kanban-and-view-jobs"></a><span data-ttu-id="fa8ee-124">Kanban oluşturun ve işleri görüntüleyin</span><span class="sxs-lookup"><span data-stu-id="fa8ee-124">Create kanban and view jobs</span></span>
1. <span data-ttu-id="fa8ee-125">Kanbanlar bölümünü genişletin.</span><span class="sxs-lookup"><span data-stu-id="fa8ee-125">Expand the Kanbans section.</span></span>
2. <span data-ttu-id="fa8ee-126">Ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="fa8ee-126">Click Add.</span></span>
3. <span data-ttu-id="fa8ee-127">Yeni kanbanların sayısı alanına "1" girin.</span><span class="sxs-lookup"><span data-stu-id="fa8ee-127">In the Number of new kanbans field, enter '1'.</span></span>
    * <span data-ttu-id="fa8ee-128">Bu, bir kanban oluşturur.</span><span class="sxs-lookup"><span data-stu-id="fa8ee-128">This will create one kanban.</span></span>  
4. <span data-ttu-id="fa8ee-129">Toplam ürün miktarını '3'e ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="fa8ee-129">Set Product quantity to '3'.</span></span>
    * <span data-ttu-id="fa8ee-130">Kanban, 3 ürünü işler.</span><span class="sxs-lookup"><span data-stu-id="fa8ee-130">Kanban will process 3 products.</span></span>  
5. <span data-ttu-id="fa8ee-131">Vade tarihi/saati alanına bir tarih ve saat girin.</span><span class="sxs-lookup"><span data-stu-id="fa8ee-131">In the Due date/time field, enter a date and time.</span></span>
    * <span data-ttu-id="fa8ee-132">Bugün girebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="fa8ee-132">You can enter Today.</span></span>  
6. <span data-ttu-id="fa8ee-133">Oluştur'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="fa8ee-133">Click Create.</span></span>
7. <span data-ttu-id="fa8ee-134">Ayrıntılar seçeneğini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="fa8ee-134">Click Details.</span></span>
    * <span data-ttu-id="fa8ee-135">Kanbanın, üretim akışından iki işlem işi olduğuna dikkat edin.</span><span class="sxs-lookup"><span data-stu-id="fa8ee-135">Notice that the kanban has two process jobs from the production flow.</span></span> <span data-ttu-id="fa8ee-136">Birincisi SpeakerAssemblyAndPolish ve ikincisi de SpeakerTestAndPackaging öğeleridir.</span><span class="sxs-lookup"><span data-stu-id="fa8ee-136">The first one is SpeakerAssemblyAndPolish, and the second one is SpeakerTestAndPackaging.</span></span>  
    * <span data-ttu-id="fa8ee-137">Bu son adımdır!</span><span class="sxs-lookup"><span data-stu-id="fa8ee-137">This is the last step!</span></span>  

