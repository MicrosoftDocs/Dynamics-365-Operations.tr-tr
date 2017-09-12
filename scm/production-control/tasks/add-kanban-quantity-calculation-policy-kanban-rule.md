--- 
title: "Kanban kuralına kanban miktarı hesaplama ilkesi ekleme"
description: "Bu yordam, kanban miktarı hesaplama ilkesi oluşturma ve miktarları ve kanban boyutunu en iyi duruma getirmek için kanban kuralına eklemeye odaklanır."
author: ChristianRytt
manager: AnnBe
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 6a947d4a5302c6ed1848396d50cfbfcb78aabf97
ms.contentlocale: tr-tr
ms.lasthandoff: 08/29/2017

---
# <a name="add-a-kanban-quantity-calculation-policy-to-a-kanban-rule"></a><span data-ttu-id="de06c-103">Kanban kuralına kanban miktarı hesaplama ilkesi ekleme</span><span class="sxs-lookup"><span data-stu-id="de06c-103">Add a kanban quantity calculation policy to a kanban rule</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="de06c-104">Bu yordam, kanban miktarı hesaplama ilkesi oluşturma ve miktarları ve kanban boyutunu en iyi duruma getirmek için kanban kuralına eklemeye odaklanır.</span><span class="sxs-lookup"><span data-stu-id="de06c-104">This procedure focuses on creating a kanban quantity calculation policy and adding it to a kanban rule to optimize the kanban size and quantities.</span></span> <span data-ttu-id="de06c-105">Bu yöntemi oluşturmak için kullanılan demo veri şirketi USMF'dir.</span><span class="sxs-lookup"><span data-stu-id="de06c-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="de06c-106">Bu yordam değer akışı yöneticisi için hazırlanmıştır.</span><span class="sxs-lookup"><span data-stu-id="de06c-106">This procedure is intended for the value stream manager.</span></span> <span data-ttu-id="de06c-107">Bu yordam kanban miktarı önerilerini hesapla yordamını oluşturmak için bir önkoşuldur.</span><span class="sxs-lookup"><span data-stu-id="de06c-107">This procedure is a prerequisite for creating the procedure Calculate kanban quantity suggestions.</span></span> 


## <a name="create-a-kanban-quantity-calculation-policy"></a><span data-ttu-id="de06c-108">Bir kanban miktar hesaplama ilkesi oluştur</span><span class="sxs-lookup"><span data-stu-id="de06c-108">Create a kanban quantity calculation policy</span></span>
1. <span data-ttu-id="de06c-109">Üretim kontrol > Periyodik görevler > Kanban miktarı hesaplama > Kanban miktarı hesaplama ilkeleri'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="de06c-109">Go to Production control > Periodic tasks > Kanban quantity calculation > Kanban quantity calculation policies.</span></span>
2. <span data-ttu-id="de06c-110">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="de06c-110">Click New.</span></span>
3. <span data-ttu-id="de06c-111">İsim alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="de06c-111">In the Name field, type a value.</span></span>
    * <span data-ttu-id="de06c-112">Örneğin, Speaker2016 yazın.</span><span class="sxs-lookup"><span data-stu-id="de06c-112">For example, type Speaker2016.</span></span>  
4. <span data-ttu-id="de06c-113">Master plan alanında, aramayı açmak için açılır menü düğmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="de06c-113">In the Master plan field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="de06c-114">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="de06c-114">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="de06c-115">Talep hesaplamak için StaticPlan seçin.</span><span class="sxs-lookup"><span data-stu-id="de06c-115">Select StaticPlan to calculate demand.</span></span>  
6. <span data-ttu-id="de06c-116">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="de06c-116">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="de06c-117">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="de06c-117">Click Save.</span></span>
8. <span data-ttu-id="de06c-118">Minimum kanban miktarı alanında '1' girin.</span><span class="sxs-lookup"><span data-stu-id="de06c-118">In the Minimum kanban quantity field, enter '1'.</span></span>
    * <span data-ttu-id="de06c-119">Bu, Kanban miktarı hesaplamasına dahil edilen ek kanban sayısıdır.</span><span class="sxs-lookup"><span data-stu-id="de06c-119">This is the additional number of kanbans that is included in the kanban quantity calculation.</span></span>  
9. <span data-ttu-id="de06c-120">Güvenlik faktörü'nü '1'e ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="de06c-120">Set Safety factor to '1'.</span></span>
    * <span data-ttu-id="de06c-121">Bu, ek emniyet stoğu miktarını hesaplamak için kullanılan faktördür.</span><span class="sxs-lookup"><span data-stu-id="de06c-121">This is the factor that is used to calculate additional quantity of safety stock.</span></span>  
10. <span data-ttu-id="de06c-122">Gün sonra alanına, '30' girin.</span><span class="sxs-lookup"><span data-stu-id="de06c-122">In the Days ahead field, enter '30'.</span></span>
    * <span data-ttu-id="de06c-123">Bu, talebin hesaplamaya dahil edildiği kanban miktarı hesaplama tarihinden geriye doğru gün sayısıdır.</span><span class="sxs-lookup"><span data-stu-id="de06c-123">This is the number of days prior to the kanban quantity calculation date that is included in the demand calculation.</span></span>  
11. <span data-ttu-id="de06c-124">Geride kalan gün alanına '30' girin.</span><span class="sxs-lookup"><span data-stu-id="de06c-124">In the Days behind field, enter '30'.</span></span>
    * <span data-ttu-id="de06c-125">Bu, talebin hesaplamaya dahil edildiği kanban miktarı hesaplama tarihinden ileriye doğru gün sayısıdır.</span><span class="sxs-lookup"><span data-stu-id="de06c-125">This is the number of days forward from the kanban quantity calculation date that is included in the demand calculation.</span></span>  <span data-ttu-id="de06c-126">Hesaplanmada kullanılan formül gerçek değerlerle gösterilir.</span><span class="sxs-lookup"><span data-stu-id="de06c-126">The formula used for the calculation is shown with the actual values.</span></span> <span data-ttu-id="de06c-127">Örneğin, Kanban miktarı = ((Ortalama günlük talep x bekleme süresi x 2,00) / Malzeme işleme birimi başına ürün miktarı) + 1</span><span class="sxs-lookup"><span data-stu-id="de06c-127">For example,  Kanban quantity = ((Average daily demand x lead time x 2.00) / Product quantity per handling unit) + 1</span></span>  
12. <span data-ttu-id="de06c-128">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="de06c-128">Close the page.</span></span>

## <a name="add-the-kanban-quantity-calculation-policy-to-a-kanban-rule"></a><span data-ttu-id="de06c-129">Kanban miktar hesaplama ilkesini bir kanban kuralına ekleyin.</span><span class="sxs-lookup"><span data-stu-id="de06c-129">Add the kanban quantity calculation policy to a kanban rule</span></span>
1. <span data-ttu-id="de06c-130">Ürün bilgi yönetimi > Yalın imalat > Kanban kuralları'na gidin.</span><span class="sxs-lookup"><span data-stu-id="de06c-130">Go to Product information management > Lean manufacturing > Kanban rules.</span></span>
2. <span data-ttu-id="de06c-131">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="de06c-131">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="de06c-132">Bu yordam için kanban kuralı 000020'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="de06c-132">Select kanban rule 000020 for this procedure.</span></span>  
3. <span data-ttu-id="de06c-133">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="de06c-133">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="de06c-134">Kanban miktarı hesaplama ilkeleri bölümün genişlemesini değiştirin.</span><span class="sxs-lookup"><span data-stu-id="de06c-134">Toggle the expansion of the Kanban quantity calculation policies section.</span></span>
5. <span data-ttu-id="de06c-135">Ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="de06c-135">Click Add.</span></span>
    * <span data-ttu-id="de06c-136">Önceki alt görevde oluşturduğunuz kanban miktarı hesaplama ilkesini ekleyin.</span><span class="sxs-lookup"><span data-stu-id="de06c-136">Add the kanban quantity calculation policy that you have just created in the previous sub-task.</span></span>  
6. <span data-ttu-id="de06c-137">Listede, seçili satırı işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="de06c-137">In the list, mark the selected row.</span></span>
7. <span data-ttu-id="de06c-138">Ad alanında, açılır menü düğmesine tıklayarak aramayı açın.</span><span class="sxs-lookup"><span data-stu-id="de06c-138">In the Name field, click the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="de06c-139">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="de06c-139">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="de06c-140">Önceki alt görev oluşturduğunuz Speaker2016 ilkesini seçin.</span><span class="sxs-lookup"><span data-stu-id="de06c-140">Select the policy Speaker2016 that you have just created in the previous sub-task.</span></span>  


