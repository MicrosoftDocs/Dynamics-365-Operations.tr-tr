---
title: İmalat için sabit miktarlı kanban kuralı oluşturma
description: Bu yordam, bir iş hücresinde, yalın bir imalat ortamında dönüşen etkinlikleri tetiklemek üzere sabit üretim oluşturmak için gereken ayarlara odaklanır.
author: ChristianRytt
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KanbanRules, LeanProductionFlowActivityLookup, InventItemIdLookupSimple, UnitOfMeasureLookup, KanbanCreate
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: fcf2aa32ee9f89649ce8ce0afaf50b0facf053ce
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/01/2019
ms.locfileid: "1838715"
---
# <a name="create-a-fixed-quantity-kanban-rule-for-manufacturing"></a><span data-ttu-id="3dca7-103">İmalat için sabit miktarlı kanban kuralı oluşturma</span><span class="sxs-lookup"><span data-stu-id="3dca7-103">Create a fixed quantity kanban rule for manufacturing</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="3dca7-104">Bu yordam, bir iş hücresinde, yalın bir imalat ortamında dönüşen etkinlikleri tetiklemek üzere sabit üretim oluşturmak için gereken ayarlara odaklanır.</span><span class="sxs-lookup"><span data-stu-id="3dca7-104">This procedure focuses on the setup needed to create a fixed manufacturing kanban rule for triggering transforming activities, at a work cell, in a lean environment.</span></span> <span data-ttu-id="3dca7-105">Bu yöntemi oluşturmak için kullanılan demo veri şirketi USMF'dir.</span><span class="sxs-lookup"><span data-stu-id="3dca7-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="3dca7-106">Bu yordam, yeni veya değiştirilmiş bir ürünün üretimine hazırlanırken kullanılması için İşlem Mühendisi veya Değer Akışı Yöneticisi için hazırlanmıştır.</span><span class="sxs-lookup"><span data-stu-id="3dca7-106">This procedure is intended for the Process Engineer or the Value Stream Manager, as they prepare production of a new or modified product.</span></span>


## <a name="create-new-kanban-rule"></a><span data-ttu-id="3dca7-107">Yeni kanban kuralı oluştur</span><span class="sxs-lookup"><span data-stu-id="3dca7-107">Create new kanban rule</span></span>
1. <span data-ttu-id="3dca7-108">Kanban kuralları'na gidin.</span><span class="sxs-lookup"><span data-stu-id="3dca7-108">Go to Kanban rules.</span></span>
2. <span data-ttu-id="3dca7-109">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="3dca7-109">Click New.</span></span>
    * <span data-ttu-id="3dca7-110">Varsayılan Tür olarak Üretim'in ve Stok yenileme stratejisi olarak Sabit ayarlandığını göz ardı etmeyin.</span><span class="sxs-lookup"><span data-stu-id="3dca7-110">Notice that the default Type is Manufacturing and Replenishment strategy is Fixed.</span></span> <span data-ttu-id="3dca7-111">Bu parametreleri değiştirmek zorunda değilsiniz.</span><span class="sxs-lookup"><span data-stu-id="3dca7-111">You do not have to change these parameters.</span></span>  
3. <span data-ttu-id="3dca7-112">İlk plan alanında bir değer girin veya bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="3dca7-112">In the First plan activity field, enter or select a value.</span></span>
    * <span data-ttu-id="3dca7-113">Bu eylem, kanban kuralına dayalı olarak oluşturulan kanbanlar için gerçekleştirilir.</span><span class="sxs-lookup"><span data-stu-id="3dca7-113">This is the activity that will be performed for kanbans created based on this kanban rule.</span></span>  <span data-ttu-id="3dca7-114">'SpeakerTestAndPackaging' öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="3dca7-114">Select 'SpeakerTestAndPackaging'.</span></span>  
4. <span data-ttu-id="3dca7-115">Ayrıntılar bölümünü genişletin.</span><span class="sxs-lookup"><span data-stu-id="3dca7-115">Expand the Details section.</span></span>
5. <span data-ttu-id="3dca7-116">Ürün alanında bir değer girin veya bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="3dca7-116">In the Product field, enter or select a value.</span></span>
    * <span data-ttu-id="3dca7-117">L0050 öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="3dca7-117">Select L0050.</span></span>  
6. <span data-ttu-id="3dca7-118">Ölçü birimi alanında bir değer girin veya bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="3dca7-118">In the Unit of measure field, enter or select a value.</span></span>
    * <span data-ttu-id="3dca7-119">Dakika'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="3dca7-119">Select minutes.</span></span>  
7. <span data-ttu-id="3dca7-120">Sağlama süresi alanında bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="3dca7-120">In the Lead time field, enter a number.</span></span>
    * <span data-ttu-id="3dca7-121">5 girin.</span><span class="sxs-lookup"><span data-stu-id="3dca7-121">Enter 5.</span></span>  

## <a name="set-quantities"></a><span data-ttu-id="3dca7-122">Miktarları ayarla</span><span class="sxs-lookup"><span data-stu-id="3dca7-122">Set quantities</span></span>
1. <span data-ttu-id="3dca7-123">Miktarlar bölümünü genişletin.</span><span class="sxs-lookup"><span data-stu-id="3dca7-123">Expand the Quantities section.</span></span>
2. <span data-ttu-id="3dca7-124">Varsayılan mktarı '10' olacak şekilde ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="3dca7-124">Set Default quantity to '10'.</span></span>
    * <span data-ttu-id="3dca7-125">Bu, her kanban için transfer edilecek miktardır.</span><span class="sxs-lookup"><span data-stu-id="3dca7-125">This is the quantity that will be transferred for each kanban.</span></span>  
3. <span data-ttu-id="3dca7-126">Ürün miktar farkı onay kutusunu işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="3dca7-126">Select the Product quantity variance check box.</span></span>
    * <span data-ttu-id="3dca7-127">Bununla, seçili kanbanlar varsayılan miktardan bir sapmayla tamamlanabilir.</span><span class="sxs-lookup"><span data-stu-id="3dca7-127">With this, selected kanbans can be completed with a variance from the default quantity.</span></span>  <span data-ttu-id="3dca7-128">Kanbanların 8-12 miktarıyla tamamlanmasını sağlamak için her iki sapmayı da 2 olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="3dca7-128">To allow kanbans to be completed with a quantity from 8 to 12, set both variances to 2.</span></span>  
4. <span data-ttu-id="3dca7-129">Aşağıdaki Fark değerini '2' olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="3dca7-129">Set Variance below to '2'.</span></span>
    * <span data-ttu-id="3dca7-130">Bu, daha düşük şekilde 10 - 2 = 8 olarak tamamlanmasını sağlar.</span><span class="sxs-lookup"><span data-stu-id="3dca7-130">This will allow completing down to 10 - 2 = 8</span></span>  
5. <span data-ttu-id="3dca7-131">Yukarıdaki Fark değerini'2' olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="3dca7-131">Set Variance above to '2'.</span></span>
    * <span data-ttu-id="3dca7-132">Bu, daha yüksek şekilde 10 + 2 = 12 olarak tamamlanmasını sağlar.</span><span class="sxs-lookup"><span data-stu-id="3dca7-132">This will allow completing up to 10 + 2 = 12</span></span>  
6. <span data-ttu-id="3dca7-133">Sabit kanban miktarı alanında bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="3dca7-133">In the Fixed kanban quantity field, enter a number.</span></span>
    * <span data-ttu-id="3dca7-134">Bu, kanbanların etkin olması gereken tutardır.</span><span class="sxs-lookup"><span data-stu-id="3dca7-134">This is the amount of kanbans that should be active.</span></span> <span data-ttu-id="3dca7-135">Bu durumda, her 10 tane için 5 kanban işlenir.</span><span class="sxs-lookup"><span data-stu-id="3dca7-135">In this case, 5 kanbans processing 10 each.</span></span>  
7. <span data-ttu-id="3dca7-136">Uyarı sınırı minimumı alanında '2' girin.</span><span class="sxs-lookup"><span data-stu-id="3dca7-136">In the Alert boundary minimum field, enter '2'.</span></span>
    * <span data-ttu-id="3dca7-137">Hedefte olması gereken tam kanbanların minimum tutarını izlemek için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="3dca7-137">Used to keep track of the minimum amount of full kanbans that should be at the destination.</span></span> <span data-ttu-id="3dca7-138">Örneğin, bu kanban tutarının genel görünümüne ilişkin kullanılır.</span><span class="sxs-lookup"><span data-stu-id="3dca7-138">For example, this is used on the kanban quantity overview.</span></span>  
8. <span data-ttu-id="3dca7-139">Uyarı sınırı maksimumu alanında '4' girin.</span><span class="sxs-lookup"><span data-stu-id="3dca7-139">In the Alert boundary maximum field, enter '4'.</span></span>
    * <span data-ttu-id="3dca7-140">Hedefte olması gereken tam kanbanların maksimum tutarını izlemek için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="3dca7-140">Used to keep track of the maximum amount of full kanbans that should be at the destination.</span></span> <span data-ttu-id="3dca7-141">Örneğin, bu kanban tutarının genel görünümüne ilişkin kullanılır.</span><span class="sxs-lookup"><span data-stu-id="3dca7-141">For example, this is used on the kanban quantity overview.</span></span>  
9. <span data-ttu-id="3dca7-142">Otomatik planlama miktarı alanında '1' girin.</span><span class="sxs-lookup"><span data-stu-id="3dca7-142">In the Automatic planning quantity field, enter '1'.</span></span>
    * <span data-ttu-id="3dca7-143">Bunun 1 olarak ayarlanması her bir kanbanın otomatik olarak planlanacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="3dca7-143">Setting this to 1 means that every kanban will be automatically planned.</span></span>   <span data-ttu-id="3dca7-144">3 girildiyse, 3 boş kanban planlama için hazır olana kadar kanbanlar planlanmaz.</span><span class="sxs-lookup"><span data-stu-id="3dca7-144">If we entered 3, the kanbans would not be planned until 3 empty kanbans are ready for planning.</span></span> <span data-ttu-id="3dca7-145">Bu, işleri gruplamak ve çok fazla ayar yapmanın önüne geçmek için yararlıdır.</span><span class="sxs-lookup"><span data-stu-id="3dca7-145">This is useful for grouping work and avoiding too much setup.</span></span>  

## <a name="create-kanbans"></a><span data-ttu-id="3dca7-146">Kanban Oluştur</span><span class="sxs-lookup"><span data-stu-id="3dca7-146">Create Kanbans</span></span>
1. <span data-ttu-id="3dca7-147">Kanbanlar bölümünü genişletin.</span><span class="sxs-lookup"><span data-stu-id="3dca7-147">Expand the Kanbans section.</span></span>
2. <span data-ttu-id="3dca7-148">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="3dca7-148">Click Save.</span></span>
    * <span data-ttu-id="3dca7-149">Kanbanlar oluşturulmadan önce kanban kuralının kaydedilmesi gerekir.</span><span class="sxs-lookup"><span data-stu-id="3dca7-149">The kanban rule needs to be saved before kanbans can be created.</span></span>  
3. <span data-ttu-id="3dca7-150">Ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="3dca7-150">Click Add.</span></span>
    * <span data-ttu-id="3dca7-151">Etkin kanban olmadığını, bu nedenle de 'Önerilen yeni kanban sayısı'nın 5 olduğuna dikkat edin.</span><span class="sxs-lookup"><span data-stu-id="3dca7-151">Note that there are no active kanbans, due to this the suggested 'Number of new kanbans' are 5.</span></span> <span data-ttu-id="3dca7-152">Bu, 'Sabit kanban miktarı'na eşittir.</span><span class="sxs-lookup"><span data-stu-id="3dca7-152">This is equal to the 'Fixed kanban quantity'.</span></span>  
4. <span data-ttu-id="3dca7-153">Oluştur'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="3dca7-153">Click Create.</span></span>
    * <span data-ttu-id="3dca7-154">Bu, 5 kanban oluşturur.</span><span class="sxs-lookup"><span data-stu-id="3dca7-154">This will create 5 kanbans.</span></span>  
    * <span data-ttu-id="3dca7-155">Bu üretim kanbanı kuralı için her 10 başına 5 kanban oluşturulduğunu unutmayın.</span><span class="sxs-lookup"><span data-stu-id="3dca7-155">Note that 5 kanbans, for 10 each, was created for this manufacturing kanban rule.</span></span> <span data-ttu-id="3dca7-156">Bu yordamın son aşamasıdır.</span><span class="sxs-lookup"><span data-stu-id="3dca7-156">This is the last step in this procedure.</span></span>  

