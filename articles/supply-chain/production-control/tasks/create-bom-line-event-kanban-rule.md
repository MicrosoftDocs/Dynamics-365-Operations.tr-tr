---
title: Ürün reçetesi satırı olayı kanban kuralı oluşturma
description: Bu görev, karışık bir yalın ve klasik üretim ortamında üretim BOM hatları için tedarikin garanti edilmesi amacıyla bir olay kanban kuralının oluşturulması için gerekli kurulum üzerine odaklanmaktadır.
author: ChristianRytt
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KanbanRules, LeanProductionFlowActivityLookup, InventItemIdLookupSimple, ProdTableListPage, ProdTableCreate, InventItemIdLookupPurchase, ProdTable, ProdBOM, ProdParmCostEstimation
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: bcef749139635b2d8858a85154ff7619c16857d3
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/15/2021
ms.locfileid: "4998765"
---
# <a name="create-a-bom-line-event-kanban-rule"></a><span data-ttu-id="c0f6f-103">Ürün reçetesi satırı olayı kanban kuralı oluşturma</span><span class="sxs-lookup"><span data-stu-id="c0f6f-103">Create a BOM line event kanban rule</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="c0f6f-104">Bu görev, karışık bir yalın ve klasik üretim ortamında üretim BOM hatları için tedarikin garanti edilmesi amacıyla bir olay kanban kuralının oluşturulması için gerekli kurulum üzerine odaklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="c0f6f-104">This task focuses on the setup needed to create an event kanban rule to ensure supply for production BOM lines in a mixed lean and classic production environment.</span></span> <span data-ttu-id="c0f6f-105">Bu görevi oluşturmak için kullanılan demo veri şirketi USMF'dir.</span><span class="sxs-lookup"><span data-stu-id="c0f6f-105">The demo data company used to create this task is USMF.</span></span> <span data-ttu-id="c0f6f-106">Bu görev, yeni veya değiştirilmiş bir ürünün üretimine hazırlanırken kullanılması için işlem mühendisi veya değer akışı yöneticisi için hazırlanmıştır.</span><span class="sxs-lookup"><span data-stu-id="c0f6f-106">This task is intended for the process engineer or the value stream manager, as they prepare production of a new or modified product.</span></span>


## <a name="create-a-new-kanban-rule"></a><span data-ttu-id="c0f6f-107">Yeni bir kanban kuralı oluştur</span><span class="sxs-lookup"><span data-stu-id="c0f6f-107">Create a new kanban rule</span></span>
1. <span data-ttu-id="c0f6f-108">Üretim denetimi > Periyodik görevler > Kanban miktarı hesaplama > Kanban kuralları öğesine gidin.</span><span class="sxs-lookup"><span data-stu-id="c0f6f-108">Go to Production control > Periodic tasks > Kanban quantity calculation > Kanban rules.</span></span>
2. <span data-ttu-id="c0f6f-109">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="c0f6f-109">Click New.</span></span>
3. <span data-ttu-id="c0f6f-110">Tür alanından 'Çek' seçimini yapın.</span><span class="sxs-lookup"><span data-stu-id="c0f6f-110">In the Type field, select 'Withdrawal'.</span></span>
    * <span data-ttu-id="c0f6f-111">Çekme türü, transfer kanbanlarının oluşturulması için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="c0f6f-111">The Withdrawal type is used to create transfer kanbans.</span></span>  
4. <span data-ttu-id="c0f6f-112">Yenileme stratejisi alanında 'Olay' öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="c0f6f-112">In the Replenishment strategy field, select 'Event'.</span></span>
    * <span data-ttu-id="c0f6f-113">Olay stratejisi, bir olaya göre kanbanların transferinin oluşturulması için seçilir.</span><span class="sxs-lookup"><span data-stu-id="c0f6f-113">The Event strategy is selected to create the transfer of kanbans based on an event.</span></span> <span data-ttu-id="c0f6f-114">Görev kılavuzunda daha sonra bunu bir üretim emri tahmin ederek tetikleyeceğiz.</span><span class="sxs-lookup"><span data-stu-id="c0f6f-114">Later in the task guide, we will trigger it by estimating a production order.</span></span>  
5. <span data-ttu-id="c0f6f-115">İlk plan alanında bir değer girin veya bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="c0f6f-115">In the First plan activity field, enter or select a value.</span></span>
    * <span data-ttu-id="c0f6f-116">ReplenishSpeakerComponents öğesini girin veya seçin.</span><span class="sxs-lookup"><span data-stu-id="c0f6f-116">Enter or select ReplenishSpeakerComponents.</span></span> <span data-ttu-id="c0f6f-117">Bu transfer faaliyeti, alıcı (çıkış) ambarına ve konum 12'ye sahiptir, bu da malzemenin ambar 12'deki konum 12'ye taşınacağı anlamına gelir.</span><span class="sxs-lookup"><span data-stu-id="c0f6f-117">This transfer activity has receipt (output) warehouse and location 12, which means that material will be moved to location 12 in warehouse 12.</span></span>  
6. <span data-ttu-id="c0f6f-118">Ayrıntılar bölümünü genişletin.</span><span class="sxs-lookup"><span data-stu-id="c0f6f-118">Expand the Details section.</span></span>
7. <span data-ttu-id="c0f6f-119">Üretim alanına M0001 değerini girin veya buradan M0001 değerini seçin.</span><span class="sxs-lookup"><span data-stu-id="c0f6f-119">In the Product field, enter or select M0001.</span></span>
8. <span data-ttu-id="c0f6f-120">Olaylat bölümünü genişletin.</span><span class="sxs-lookup"><span data-stu-id="c0f6f-120">Expand the Events section.</span></span>
9. <span data-ttu-id="c0f6f-121">BOM satır olayı alanında 'Otomatik' öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="c0f6f-121">In the BOM line event field, select 'Automatic'.</span></span>
    * <span data-ttu-id="c0f6f-122">BOM satır olayı alanı Otomatik olarak ayarlandıktan sonra, üretim emri BOM satırları için malzeme ihtiyaçlarını karşılamak üzere kanban oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="c0f6f-122">With the BOM line event field set to Automatic, kanban will be created to fulfill material needs for production order BOM lines.</span></span>  
10. <span data-ttu-id="c0f6f-123">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="c0f6f-123">Close the page.</span></span>

## <a name="create-and-modify-a-new-production-order"></a><span data-ttu-id="c0f6f-124">Yeni üretim emri oluşturma ve değiştirme</span><span class="sxs-lookup"><span data-stu-id="c0f6f-124">Create and modify a new production order</span></span>
1. <span data-ttu-id="c0f6f-125">Üretim denetimi > Üretim emirleri > Tüm üretim emirleri'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="c0f6f-125">Go to Production control > Production orders > All production orders.</span></span>
2. <span data-ttu-id="c0f6f-126">Yeni üretim emri'ne tıklayın.</span><span class="sxs-lookup"><span data-stu-id="c0f6f-126">Click New production order.</span></span>
3. <span data-ttu-id="c0f6f-127">Madde numarası alanında bir değer girin veya seçin.</span><span class="sxs-lookup"><span data-stu-id="c0f6f-127">In the Item number field, enter or select a value.</span></span>
    * <span data-ttu-id="c0f6f-128">'L0001' öğesini girin veya seçin.</span><span class="sxs-lookup"><span data-stu-id="c0f6f-128">Enter or select 'L0001'.</span></span> <span data-ttu-id="c0f6f-129">M0001, madde L0001 için BOM'a dahil edileceğinden L0001 maddesini kullanıyoruz.</span><span class="sxs-lookup"><span data-stu-id="c0f6f-129">We use item L0001 because item M0001 is included in the BOM for item L0001.</span></span>  
4. <span data-ttu-id="c0f6f-130">Oluştur'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="c0f6f-130">Click Create.</span></span>
5. <span data-ttu-id="c0f6f-131">Listede, L0001 sırasındaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="c0f6f-131">In the list, click the link in the row for L0001</span></span>
6. <span data-ttu-id="c0f6f-132">Ürün reçetesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="c0f6f-132">Click BOM.</span></span>
7. <span data-ttu-id="c0f6f-133">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="c0f6f-133">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="c0f6f-134">Düzenle öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="c0f6f-134">Click Edit.</span></span>
9. <span data-ttu-id="c0f6f-135">Satır türü alanından 'İlişkilendirilen tedarik' öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="c0f6f-135">In the Line type field, select 'Pegged supply'.</span></span>
    * <span data-ttu-id="c0f6f-136">Bir kanban tedariki oluşturma sürecinin tetiklenmesi için ilişkilendirilmiş tedarik kullanılır.</span><span class="sxs-lookup"><span data-stu-id="c0f6f-136">Pegged supply is selected to trigger the supply creation of a kanban.</span></span>  
10. <span data-ttu-id="c0f6f-137">Kaynak tüketimi alanında Hayır'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="c0f6f-137">Select No in the Resource consumption field.</span></span>
    * <span data-ttu-id="c0f6f-138">Kaynak tüketimi onay kutusundaki işaret kaldırıldığında ambar değiştirilebilir.</span><span class="sxs-lookup"><span data-stu-id="c0f6f-138">Clearing the check box of Resource consumption lets us change the warehouse.</span></span>  
11. <span data-ttu-id="c0f6f-139">Stok boyutları bölümünü genişletin.</span><span class="sxs-lookup"><span data-stu-id="c0f6f-139">Expand the Inventory dimensions section.</span></span>
12. <span data-ttu-id="c0f6f-140">Ambar alanına '12' yazın.</span><span class="sxs-lookup"><span data-stu-id="c0f6f-140">In the Warehouse field, type '12'.</span></span>
    * <span data-ttu-id="c0f6f-141">Çekme faaliyeti için çıkış ambarı olduğundan ambar, 12 olarak ayarlanır.</span><span class="sxs-lookup"><span data-stu-id="c0f6f-141">Warehouse is set to 12 because this is the output warehouse for the withdrawal activity.</span></span>  
13. <span data-ttu-id="c0f6f-142">Konum alanına '12' yazın.</span><span class="sxs-lookup"><span data-stu-id="c0f6f-142">In the Location field, type '12'.</span></span>
    * <span data-ttu-id="c0f6f-143">Çekme faaliyeti için çıkış konumu olduğundan konum, 12 olarak ayarlanır.</span><span class="sxs-lookup"><span data-stu-id="c0f6f-143">Location is set to 12 because this is the output location of the withdrawal activity.</span></span>  
14. <span data-ttu-id="c0f6f-144">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="c0f6f-144">Close the page.</span></span>
15. <span data-ttu-id="c0f6f-145">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="c0f6f-145">Close the page.</span></span>

## <a name="estimate-the-production-order-and-view-the-kanban-created"></a><span data-ttu-id="c0f6f-146">Üretim emrini tahin etme ve oluşturulan kanbanı görüntüleme</span><span class="sxs-lookup"><span data-stu-id="c0f6f-146">Estimate the production order and view the kanban created</span></span>
1. <span data-ttu-id="c0f6f-147">Tahmin seçeneğine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="c0f6f-147">Click Estimate.</span></span>
    * <span data-ttu-id="c0f6f-148">Üretim emrinin tahmin edilmesi, ilişkili kanbanın M0001 tedarik maddesine oluşturulması tetiklenir.</span><span class="sxs-lookup"><span data-stu-id="c0f6f-148">Estimating the production order will trigger the creation of the associated kanban to supply item M0001.</span></span>  
2. <span data-ttu-id="c0f6f-149">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="c0f6f-149">Click OK.</span></span>
3. <span data-ttu-id="c0f6f-150">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="c0f6f-150">Close the page.</span></span>
4. <span data-ttu-id="c0f6f-151">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="c0f6f-151">Close the page.</span></span>
5. <span data-ttu-id="c0f6f-152">Ürün bilgi yönetimi > Yalın imalat > Kanban kuralları'na gidin.</span><span class="sxs-lookup"><span data-stu-id="c0f6f-152">Go to Product information management > Lean manufacturing > Kanban rules.</span></span>
6. <span data-ttu-id="c0f6f-153">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="c0f6f-153">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="c0f6f-154">Madde M0001 için oluşturulan olay kanban kuralını seçin.</span><span class="sxs-lookup"><span data-stu-id="c0f6f-154">Select the event kanban rule created for item M0001.</span></span>  
7. <span data-ttu-id="c0f6f-155">Kanbanlar bölümünü genişletin.</span><span class="sxs-lookup"><span data-stu-id="c0f6f-155">Expand the Kanbans section.</span></span>
8. <span data-ttu-id="c0f6f-156">Listede, seçili satırı işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="c0f6f-156">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="c0f6f-157">Kanbanın, tahmini üretim emri için M0001 tedarik edilmesi amacıyla oluşturulduğuna dikkat edin.</span><span class="sxs-lookup"><span data-stu-id="c0f6f-157">Notice the kanban created to supply M0001 for the estimated production order.</span></span>  
    * <span data-ttu-id="c0f6f-158">Bu son adımdır!</span><span class="sxs-lookup"><span data-stu-id="c0f6f-158">This is the last step!</span></span>  

