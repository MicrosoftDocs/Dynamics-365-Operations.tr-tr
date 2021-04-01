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
ms.openlocfilehash: a6df9632d6e2798fad2b3462055a9495394583f6
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5255289"
---
# <a name="create-a-bom-line-event-kanban-rule"></a><span data-ttu-id="41f15-103">Ürün reçetesi satırı olayı kanban kuralı oluşturma</span><span class="sxs-lookup"><span data-stu-id="41f15-103">Create a BOM line event kanban rule</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="41f15-104">Bu görev, karışık bir yalın ve klasik üretim ortamında üretim BOM hatları için tedarikin garanti edilmesi amacıyla bir olay kanban kuralının oluşturulması için gerekli kurulum üzerine odaklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="41f15-104">This task focuses on the setup needed to create an event kanban rule to ensure supply for production BOM lines in a mixed lean and classic production environment.</span></span> <span data-ttu-id="41f15-105">Bu görevi oluşturmak için kullanılan demo veri şirketi USMF'dir.</span><span class="sxs-lookup"><span data-stu-id="41f15-105">The demo data company used to create this task is USMF.</span></span> <span data-ttu-id="41f15-106">Bu görev, yeni veya değiştirilmiş bir ürünün üretimine hazırlanırken kullanılması için işlem mühendisi veya değer akışı yöneticisi için hazırlanmıştır.</span><span class="sxs-lookup"><span data-stu-id="41f15-106">This task is intended for the process engineer or the value stream manager, as they prepare production of a new or modified product.</span></span>


## <a name="create-a-new-kanban-rule"></a><span data-ttu-id="41f15-107">Yeni bir kanban kuralı oluştur</span><span class="sxs-lookup"><span data-stu-id="41f15-107">Create a new kanban rule</span></span>
1. <span data-ttu-id="41f15-108">Üretim denetimi > Periyodik görevler > Kanban miktarı hesaplama > Kanban kuralları öğesine gidin.</span><span class="sxs-lookup"><span data-stu-id="41f15-108">Go to Production control > Periodic tasks > Kanban quantity calculation > Kanban rules.</span></span>
2. <span data-ttu-id="41f15-109">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="41f15-109">Click New.</span></span>
3. <span data-ttu-id="41f15-110">Tür alanından 'Çek' seçimini yapın.</span><span class="sxs-lookup"><span data-stu-id="41f15-110">In the Type field, select 'Withdrawal'.</span></span>
    * <span data-ttu-id="41f15-111">Çekme türü, transfer kanbanlarının oluşturulması için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="41f15-111">The Withdrawal type is used to create transfer kanbans.</span></span>  
4. <span data-ttu-id="41f15-112">Yenileme stratejisi alanında 'Olay' öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="41f15-112">In the Replenishment strategy field, select 'Event'.</span></span>
    * <span data-ttu-id="41f15-113">Olay stratejisi, bir olaya göre kanbanların transferinin oluşturulması için seçilir.</span><span class="sxs-lookup"><span data-stu-id="41f15-113">The Event strategy is selected to create the transfer of kanbans based on an event.</span></span> <span data-ttu-id="41f15-114">Görev kılavuzunda daha sonra bunu bir üretim emri tahmin ederek tetikleyeceğiz.</span><span class="sxs-lookup"><span data-stu-id="41f15-114">Later in the task guide, we will trigger it by estimating a production order.</span></span>  
5. <span data-ttu-id="41f15-115">İlk plan alanında bir değer girin veya bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="41f15-115">In the First plan activity field, enter or select a value.</span></span>
    * <span data-ttu-id="41f15-116">ReplenishSpeakerComponents öğesini girin veya seçin.</span><span class="sxs-lookup"><span data-stu-id="41f15-116">Enter or select ReplenishSpeakerComponents.</span></span> <span data-ttu-id="41f15-117">Bu transfer faaliyeti, alıcı (çıkış) ambarına ve konum 12'ye sahiptir, bu da malzemenin ambar 12'deki konum 12'ye taşınacağı anlamına gelir.</span><span class="sxs-lookup"><span data-stu-id="41f15-117">This transfer activity has receipt (output) warehouse and location 12, which means that material will be moved to location 12 in warehouse 12.</span></span>  
6. <span data-ttu-id="41f15-118">Ayrıntılar bölümünü genişletin.</span><span class="sxs-lookup"><span data-stu-id="41f15-118">Expand the Details section.</span></span>
7. <span data-ttu-id="41f15-119">Üretim alanına M0001 değerini girin veya buradan M0001 değerini seçin.</span><span class="sxs-lookup"><span data-stu-id="41f15-119">In the Product field, enter or select M0001.</span></span>
8. <span data-ttu-id="41f15-120">Olaylat bölümünü genişletin.</span><span class="sxs-lookup"><span data-stu-id="41f15-120">Expand the Events section.</span></span>
9. <span data-ttu-id="41f15-121">BOM satır olayı alanında 'Otomatik' öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="41f15-121">In the BOM line event field, select 'Automatic'.</span></span>
    * <span data-ttu-id="41f15-122">BOM satır olayı alanı Otomatik olarak ayarlandıktan sonra, üretim emri BOM satırları için malzeme ihtiyaçlarını karşılamak üzere kanban oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="41f15-122">With the BOM line event field set to Automatic, kanban will be created to fulfill material needs for production order BOM lines.</span></span>  
10. <span data-ttu-id="41f15-123">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="41f15-123">Close the page.</span></span>

## <a name="create-and-modify-a-new-production-order"></a><span data-ttu-id="41f15-124">Yeni üretim emri oluşturma ve değiştirme</span><span class="sxs-lookup"><span data-stu-id="41f15-124">Create and modify a new production order</span></span>
1. <span data-ttu-id="41f15-125">Üretim denetimi > Üretim emirleri > Tüm üretim emirleri'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="41f15-125">Go to Production control > Production orders > All production orders.</span></span>
2. <span data-ttu-id="41f15-126">Yeni üretim emri'ne tıklayın.</span><span class="sxs-lookup"><span data-stu-id="41f15-126">Click New production order.</span></span>
3. <span data-ttu-id="41f15-127">Madde numarası alanında bir değer girin veya seçin.</span><span class="sxs-lookup"><span data-stu-id="41f15-127">In the Item number field, enter or select a value.</span></span>
    * <span data-ttu-id="41f15-128">'L0001' öğesini girin veya seçin.</span><span class="sxs-lookup"><span data-stu-id="41f15-128">Enter or select 'L0001'.</span></span> <span data-ttu-id="41f15-129">M0001, madde L0001 için BOM'a dahil edileceğinden L0001 maddesini kullanıyoruz.</span><span class="sxs-lookup"><span data-stu-id="41f15-129">We use item L0001 because item M0001 is included in the BOM for item L0001.</span></span>  
4. <span data-ttu-id="41f15-130">Oluştur'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="41f15-130">Click Create.</span></span>
5. <span data-ttu-id="41f15-131">Listede, L0001 sırasındaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="41f15-131">In the list, click the link in the row for L0001</span></span>
6. <span data-ttu-id="41f15-132">Ürün reçetesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="41f15-132">Click BOM.</span></span>
7. <span data-ttu-id="41f15-133">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="41f15-133">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="41f15-134">Düzenle öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="41f15-134">Click Edit.</span></span>
9. <span data-ttu-id="41f15-135">Satır türü alanından 'İlişkilendirilen tedarik' öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="41f15-135">In the Line type field, select 'Pegged supply'.</span></span>
    * <span data-ttu-id="41f15-136">Bir kanban tedariki oluşturma sürecinin tetiklenmesi için ilişkilendirilmiş tedarik kullanılır.</span><span class="sxs-lookup"><span data-stu-id="41f15-136">Pegged supply is selected to trigger the supply creation of a kanban.</span></span>  
10. <span data-ttu-id="41f15-137">Kaynak tüketimi alanında Hayır'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="41f15-137">Select No in the Resource consumption field.</span></span>
    * <span data-ttu-id="41f15-138">Kaynak tüketimi onay kutusundaki işaret kaldırıldığında ambar değiştirilebilir.</span><span class="sxs-lookup"><span data-stu-id="41f15-138">Clearing the check box of Resource consumption lets us change the warehouse.</span></span>  
11. <span data-ttu-id="41f15-139">Stok boyutları bölümünü genişletin.</span><span class="sxs-lookup"><span data-stu-id="41f15-139">Expand the Inventory dimensions section.</span></span>
12. <span data-ttu-id="41f15-140">Ambar alanına '12' yazın.</span><span class="sxs-lookup"><span data-stu-id="41f15-140">In the Warehouse field, type '12'.</span></span>
    * <span data-ttu-id="41f15-141">Çekme faaliyeti için çıkış ambarı olduğundan ambar, 12 olarak ayarlanır.</span><span class="sxs-lookup"><span data-stu-id="41f15-141">Warehouse is set to 12 because this is the output warehouse for the withdrawal activity.</span></span>  
13. <span data-ttu-id="41f15-142">Konum alanına '12' yazın.</span><span class="sxs-lookup"><span data-stu-id="41f15-142">In the Location field, type '12'.</span></span>
    * <span data-ttu-id="41f15-143">Çekme faaliyeti için çıkış konumu olduğundan konum, 12 olarak ayarlanır.</span><span class="sxs-lookup"><span data-stu-id="41f15-143">Location is set to 12 because this is the output location of the withdrawal activity.</span></span>  
14. <span data-ttu-id="41f15-144">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="41f15-144">Close the page.</span></span>
15. <span data-ttu-id="41f15-145">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="41f15-145">Close the page.</span></span>

## <a name="estimate-the-production-order-and-view-the-kanban-created"></a><span data-ttu-id="41f15-146">Üretim emrini tahin etme ve oluşturulan kanbanı görüntüleme</span><span class="sxs-lookup"><span data-stu-id="41f15-146">Estimate the production order and view the kanban created</span></span>
1. <span data-ttu-id="41f15-147">Tahmin seçeneğine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="41f15-147">Click Estimate.</span></span>
    * <span data-ttu-id="41f15-148">Üretim emrinin tahmin edilmesi, ilişkili kanbanın M0001 tedarik maddesine oluşturulması tetiklenir.</span><span class="sxs-lookup"><span data-stu-id="41f15-148">Estimating the production order will trigger the creation of the associated kanban to supply item M0001.</span></span>  
2. <span data-ttu-id="41f15-149">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="41f15-149">Click OK.</span></span>
3. <span data-ttu-id="41f15-150">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="41f15-150">Close the page.</span></span>
4. <span data-ttu-id="41f15-151">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="41f15-151">Close the page.</span></span>
5. <span data-ttu-id="41f15-152">Ürün bilgi yönetimi > Yalın imalat > Kanban kuralları'na gidin.</span><span class="sxs-lookup"><span data-stu-id="41f15-152">Go to Product information management > Lean manufacturing > Kanban rules.</span></span>
6. <span data-ttu-id="41f15-153">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="41f15-153">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="41f15-154">Madde M0001 için oluşturulan olay kanban kuralını seçin.</span><span class="sxs-lookup"><span data-stu-id="41f15-154">Select the event kanban rule created for item M0001.</span></span>  
7. <span data-ttu-id="41f15-155">Kanbanlar bölümünü genişletin.</span><span class="sxs-lookup"><span data-stu-id="41f15-155">Expand the Kanbans section.</span></span>
8. <span data-ttu-id="41f15-156">Listede, seçili satırı işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="41f15-156">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="41f15-157">Kanbanın, tahmini üretim emri için M0001 tedarik edilmesi amacıyla oluşturulduğuna dikkat edin.</span><span class="sxs-lookup"><span data-stu-id="41f15-157">Notice the kanban created to supply M0001 for the estimated production order.</span></span>  
    * <span data-ttu-id="41f15-158">Bu son adımdır!</span><span class="sxs-lookup"><span data-stu-id="41f15-158">This is the last step!</span></span>  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]