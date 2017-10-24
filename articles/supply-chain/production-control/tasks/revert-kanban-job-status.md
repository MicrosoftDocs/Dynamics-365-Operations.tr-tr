--- 
title: "Kanban iş durumu geri al"
description: "Bu yordam, yanlış bir kanban iş durumunun geri alınması üzerinde odaklanır."
author: YuyuScheller
manager: AnnBe
ms.date: 03/02/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 55d359232da5f3087b1e6baed182a20da09aeff7
ms.contentlocale: tr-tr
ms.lasthandoff: 09/29/2017

---
# <a name="revert-kanban-job-status"></a><span data-ttu-id="a8bde-103">Kanban iş durumu geri al</span><span class="sxs-lookup"><span data-stu-id="a8bde-103">Revert kanban job status</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="a8bde-104">Bu yordam, yanlış bir kanban iş durumunun geri alınması üzerinde odaklanır.</span><span class="sxs-lookup"><span data-stu-id="a8bde-104">This procedure focuses on reverting an incorrect kanban job status.</span></span> <span data-ttu-id="a8bde-105">Bu, makine operatörünün yanlış işi güncelleştirmesi veya yanlışlıkla hatalı bir durum ayarı girmesi durumunda yararlıdır.</span><span class="sxs-lookup"><span data-stu-id="a8bde-105">This is useful in case the machine operator updates the wrong job, or sets the wrong status by mistake.</span></span> <span data-ttu-id="a8bde-106">Bu yordamda, bir kanban işi yanlışlıkla hazırlandı olarak kaydedilmiştir ve durumu daha sonra döndürülmüştür.</span><span class="sxs-lookup"><span data-stu-id="a8bde-106">In this procedure, a kanban job is registered as prepared by mistake, and the status is reverted.</span></span> <span data-ttu-id="a8bde-107">Bu yöntemi oluşturmak için kullanılan demo veri şirketi USMF'dir.</span><span class="sxs-lookup"><span data-stu-id="a8bde-107">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="a8bde-108">Bu yordam mağaza idarecisine veya yalın üretim şirketinde çalışan makine operatörüne yöneliktir.</span><span class="sxs-lookup"><span data-stu-id="a8bde-108">This procedure is intended for the shop supervisor or machine operator working in a lean manufacturing company.</span></span>


## <a name="open-process-board-for-the-work-cell"></a><span data-ttu-id="a8bde-109">İş hücresi için işleme panosunu açın</span><span class="sxs-lookup"><span data-stu-id="a8bde-109">Open process board for the work cell</span></span>
1. <span data-ttu-id="a8bde-110">İşleme işleri için kanban panosuna gidin.</span><span class="sxs-lookup"><span data-stu-id="a8bde-110">Go to Kanban board for process jobs.</span></span>
2. <span data-ttu-id="a8bde-111">İş hücresi alanına bir değer girin veya buradan bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="a8bde-111">In the Work cell field, enter or select a value.</span></span>
    * <span data-ttu-id="a8bde-112">İş hücresi 1260'yi seç</span><span class="sxs-lookup"><span data-stu-id="a8bde-112">Select work cell 1260.</span></span>  

## <a name="prepare-kanban-job"></a><span data-ttu-id="a8bde-113">Kanban işini hazırla</span><span class="sxs-lookup"><span data-stu-id="a8bde-113">Prepare kanban job</span></span>
1. <span data-ttu-id="a8bde-114">Hazırla'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="a8bde-114">Click Prepare.</span></span>
    * <span data-ttu-id="a8bde-115">Hazırla'yı üzeri gir olduğu için tıklatamıyorsanız, kanban simgesinin boş olmasıyla anlaşılabilecek şekilde, seçili kanban'ın iş durumunun Planlı olduğundan emin olun.</span><span class="sxs-lookup"><span data-stu-id="a8bde-115">If you can't click Prepare because it is grayed out, make sure that the selected kanban job has status Planned, which is indicated by the empty kanban icon.</span></span> <span data-ttu-id="a8bde-116">Hazırla başarısız olursa, tüm malzemelerin, malzeme çekme listesinde mevcut olduğundan emin olun.</span><span class="sxs-lookup"><span data-stu-id="a8bde-116">If Prepare fails, make sure that all materials in the Picking list are available.</span></span>  
2. <span data-ttu-id="a8bde-117">Listeden hazırlanmış işi seç.</span><span class="sxs-lookup"><span data-stu-id="a8bde-117">In the list, select the prepared job.</span></span>
    * <span data-ttu-id="a8bde-118">Şu an hazırlamış olduğunuz ilk projeyi seçin.</span><span class="sxs-lookup"><span data-stu-id="a8bde-118">Select the first job that you have just prepared.</span></span>  
    * <span data-ttu-id="a8bde-119">İş durumunun hazırlanmış olduğuna, kanban simgesi içindeki üçgen ile gösterildiği şekilde, dikkat edin.</span><span class="sxs-lookup"><span data-stu-id="a8bde-119">Notice that the jobs status is prepared, which is indicated with a triangle inside the kanban icon.</span></span>  

## <a name="revert-the-status-of-the-prepared-kanban-job"></a><span data-ttu-id="a8bde-120">Hazırlanan kanban işinin durumunu geri döndür</span><span class="sxs-lookup"><span data-stu-id="a8bde-120">Revert the status of the prepared kanban job</span></span>
1. <span data-ttu-id="a8bde-121">Listede, seçili satırı işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="a8bde-121">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="a8bde-122">Önceden hazırlanmış ilk projeyi seçin.</span><span class="sxs-lookup"><span data-stu-id="a8bde-122">Select the first job that was prepared.</span></span>  
2. <span data-ttu-id="a8bde-123">Eylem Bölmesinde, Üretim öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="a8bde-123">On the Action Pane, click Manufacture.</span></span>
3. <span data-ttu-id="a8bde-124">Durumu geri al'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="a8bde-124">Click Revert status.</span></span>
    * <span data-ttu-id="a8bde-125">Aşağıdaki koşullar doğru olduğunda bir alternatif kanban kuralı kullanabilirsiniz:  - Stok yenileme stratejisi her iki kural için de aynıdır.</span><span class="sxs-lookup"><span data-stu-id="a8bde-125">You can use an alternative kanban rule when the following conditions are true:  - The replenishment strategy is the same for both rules.</span></span>  <span data-ttu-id="a8bde-126">- Her iki kural için de üretim akışı sürümü aynıdır.</span><span class="sxs-lookup"><span data-stu-id="a8bde-126">- The version of the production flow is the same for both rules.</span></span>  <span data-ttu-id="a8bde-127">- Sağlanan ürün her iki kural için de aynıdır.</span><span class="sxs-lookup"><span data-stu-id="a8bde-127">- The product that is supplied is the same for both rules.</span></span>  <span data-ttu-id="a8bde-128">- Kanban kurallarının son aktivitesi için yapılandırılmış olan tüm akış faaliyetlerinin her iki kural için de aynı olması gerekir.</span><span class="sxs-lookup"><span data-stu-id="a8bde-128">- Any downstream activities that are configured for the last activity of the kanban rules must be the same for both rules.</span></span>  <span data-ttu-id="a8bde-129">- Sağlanan stok boyutları her iki kural için de yapılandırılmış olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="a8bde-129">- The same supplied inventory dimensions must be configured for both rules.</span></span>  <span data-ttu-id="a8bde-130">- İşleme birimi durumunun Atanmamış olması gerekir.</span><span class="sxs-lookup"><span data-stu-id="a8bde-130">- The status of the handling unit must be Not assigned.</span></span>  <span data-ttu-id="a8bde-131">- Olay kanbanları yapılandırmaları da aynı olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="a8bde-131">- The configuration for event kanbans must be the same.</span></span>  
    * <span data-ttu-id="a8bde-132">Yeni durumun Planlı olduğundan emin olun.</span><span class="sxs-lookup"><span data-stu-id="a8bde-132">Ensure that the new status is Planned.</span></span>  
4. <span data-ttu-id="a8bde-133">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="a8bde-133">Click OK.</span></span>
5. <span data-ttu-id="a8bde-134">Listede, seçili satırın işaretini kaldırın.</span><span class="sxs-lookup"><span data-stu-id="a8bde-134">In the list, unmark the selected row.</span></span>
    * <span data-ttu-id="a8bde-135">Aynı işi seçin.</span><span class="sxs-lookup"><span data-stu-id="a8bde-135">Select the same job.</span></span>  
    * <span data-ttu-id="a8bde-136">Kanban işi için iş durumunun bir boş kanban simgesiyle gösterildiği üzere, Planlı'ya dönüştürüldüğüne dikkat edin.</span><span class="sxs-lookup"><span data-stu-id="a8bde-136">Notice that the job status for the kanban job is reverted to Planned, which is indicated by an empty kanban icon.</span></span>  


