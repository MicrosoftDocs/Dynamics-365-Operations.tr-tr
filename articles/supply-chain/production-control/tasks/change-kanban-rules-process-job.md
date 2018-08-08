--- 
title: "Süreç işi için kanban kurallarını değiştirme"
description: "Bu yordam, belirli bir kanban için kullanılan kanban kuralını değiştirmeye odaklanır."
author: ChristianRytt
manager: AnnBe
ms.date: 03/02/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 1d98cbff30620256c9d13e7b4a90314db150e33e
ms.openlocfilehash: 8fc47751534af69300bf8f0bdb7424043cab7b26
ms.contentlocale: tr-tr
ms.lasthandoff: 08/07/2018

---
# <a name="change-kanban-rules-for-a-process-job"></a><span data-ttu-id="663cf-103">Süreç işi için kanban kurallarını değiştirme</span><span class="sxs-lookup"><span data-stu-id="663cf-103">Change kanban rules for a process job</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="663cf-104">Bu yordam, belirli bir kanban için kullanılan kanban kuralını değiştirmeye odaklanır.</span><span class="sxs-lookup"><span data-stu-id="663cf-104">This procedure focuses on changing the used kanban rule for a given kanban.</span></span> <span data-ttu-id="663cf-105">Bu, yük kaynaklarını eşitlemek için veya döküm sırasında yararlıdır.</span><span class="sxs-lookup"><span data-stu-id="663cf-105">This is useful to level load resources or in case of breakdown.</span></span> <span data-ttu-id="663cf-106">Bu yöntemi oluşturmak için kullanılan demo veri şirketi USMF'dir.</span><span class="sxs-lookup"><span data-stu-id="663cf-106">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="663cf-107">Bu yordam, bir yalın üretim şirketinde çalışan ve değer akışından sorumlu planlayıcı için tasarlanmıştır.</span><span class="sxs-lookup"><span data-stu-id="663cf-107">This procedure is intended for the planner, working at a lean manufacturing company, responsible for the value stream.</span></span>


## <a name="copy-kanban-rule"></a><span data-ttu-id="663cf-108">Kanban kuralını kopyalama</span><span class="sxs-lookup"><span data-stu-id="663cf-108">Copy kanban rule</span></span>
1. <span data-ttu-id="663cf-109">Kanban kuralları'na gidin.</span><span class="sxs-lookup"><span data-stu-id="663cf-109">Go to Kanban rules.</span></span>
2. <span data-ttu-id="663cf-110">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="663cf-110">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="663cf-111">L0001 için 000022 Kanban olayı kuralını seçin.</span><span class="sxs-lookup"><span data-stu-id="663cf-111">Select Event Kanban rule 000022 for L0001.</span></span>  
3. <span data-ttu-id="663cf-112">Kanban kuralını çoğalt'ı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="663cf-112">Click Duplicate kanban rule.</span></span>
4. <span data-ttu-id="663cf-113">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="663cf-113">Click OK.</span></span>

## <a name="change-kanban-rule"></a><span data-ttu-id="663cf-114">Kanban kuralını değiştirme</span><span class="sxs-lookup"><span data-stu-id="663cf-114">Change kanban rule</span></span>
1. <span data-ttu-id="663cf-115">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="663cf-115">Close the page.</span></span>
2. <span data-ttu-id="663cf-116">Kanban işi planlaması'na gidin.</span><span class="sxs-lookup"><span data-stu-id="663cf-116">Go to Kanban job scheduling.</span></span>
3. <span data-ttu-id="663cf-117">Listede, seçili satırı işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="663cf-117">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="663cf-118">Kanban 000177 içeren satırı seçin.</span><span class="sxs-lookup"><span data-stu-id="663cf-118">Select line with Kanban 000177.</span></span>  
4. <span data-ttu-id="663cf-119">Alternatif kanban kuralı kullan'ı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="663cf-119">Click Use alternative kanban rule.</span></span>
5. <span data-ttu-id="663cf-120">İleri düğmesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="663cf-120">Click Next.</span></span>
6. <span data-ttu-id="663cf-121">Kanban kuralı alanında bir değer girin veya bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="663cf-121">In the Kanban rule field, enter or select a value.</span></span>
    * <span data-ttu-id="663cf-122">Daha önce oluşturulan kanban kuralını seçin.</span><span class="sxs-lookup"><span data-stu-id="663cf-122">Select the kanban rule that was created earlier.</span></span> <span data-ttu-id="663cf-123">Bu, en büyük sayıya sahip kanban kuralıdır.</span><span class="sxs-lookup"><span data-stu-id="663cf-123">This is the kanban rule with the highest number.</span></span>  
7. <span data-ttu-id="663cf-124">Son düğmesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="663cf-124">Click Finish.</span></span>
    * <span data-ttu-id="663cf-125">Kanban işi şimdi artık başka bir kanban kuralını kullanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="663cf-125">Now the kanban job is using an another kanban rule.</span></span> <span data-ttu-id="663cf-126">Bu, yük iş hücrelerini eşitlemek için yararlı olabilir.</span><span class="sxs-lookup"><span data-stu-id="663cf-126">This can be useful to level load work cells.</span></span>  


