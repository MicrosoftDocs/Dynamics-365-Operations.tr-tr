---
title: Süreç işi için kanban kurallarını değiştirme
description: Bu yordam, belirli bir kanban için kullanılan kanban kuralını değiştirmeye odaklanır.
author: ChristianRytt
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KanbanRules, KanbanRuleDuplicate, KanbanJobSchedulingListPage, LeanRuleReassignmentWizard, KanbanReassignRuleLookup
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 485afff3747a87a6e36f0249b146a39361d81b23
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/18/2020
ms.locfileid: "3147147"
---
# <a name="change-kanban-rules-for-a-process-job"></a><span data-ttu-id="d576f-103">Süreç işi için kanban kurallarını değiştirme</span><span class="sxs-lookup"><span data-stu-id="d576f-103">Change kanban rules for a process job</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="d576f-104">Bu yordam, belirli bir kanban için kullanılan kanban kuralını değiştirmeye odaklanır.</span><span class="sxs-lookup"><span data-stu-id="d576f-104">This procedure focuses on changing the used kanban rule for a given kanban.</span></span> <span data-ttu-id="d576f-105">Bu, yük kaynaklarını eşitlemek için veya döküm sırasında yararlıdır.</span><span class="sxs-lookup"><span data-stu-id="d576f-105">This is useful to level load resources or in case of breakdown.</span></span> <span data-ttu-id="d576f-106">Bu yöntemi oluşturmak için kullanılan demo veri şirketi USMF'dir.</span><span class="sxs-lookup"><span data-stu-id="d576f-106">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="d576f-107">Bu yordam, bir yalın üretim şirketinde çalışan ve değer akışından sorumlu planlayıcı için tasarlanmıştır.</span><span class="sxs-lookup"><span data-stu-id="d576f-107">This procedure is intended for the planner, working at a lean manufacturing company, responsible for the value stream.</span></span>


## <a name="copy-kanban-rule"></a><span data-ttu-id="d576f-108">Kanban kuralını kopyalama</span><span class="sxs-lookup"><span data-stu-id="d576f-108">Copy kanban rule</span></span>
1. <span data-ttu-id="d576f-109">Kanban kuralları'na gidin.</span><span class="sxs-lookup"><span data-stu-id="d576f-109">Go to Kanban rules.</span></span>
2. <span data-ttu-id="d576f-110">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="d576f-110">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="d576f-111">L0001 için 000022 Kanban olayı kuralını seçin.</span><span class="sxs-lookup"><span data-stu-id="d576f-111">Select Event Kanban rule 000022 for L0001.</span></span>  
3. <span data-ttu-id="d576f-112">Kanban kuralını çoğalt'ı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="d576f-112">Click Duplicate kanban rule.</span></span>
4. <span data-ttu-id="d576f-113">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="d576f-113">Click OK.</span></span>

## <a name="change-kanban-rule"></a><span data-ttu-id="d576f-114">Kanban kuralını değiştirme</span><span class="sxs-lookup"><span data-stu-id="d576f-114">Change kanban rule</span></span>
1. <span data-ttu-id="d576f-115">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="d576f-115">Close the page.</span></span>
2. <span data-ttu-id="d576f-116">Kanban işi planlaması'na gidin.</span><span class="sxs-lookup"><span data-stu-id="d576f-116">Go to Kanban job scheduling.</span></span>
3. <span data-ttu-id="d576f-117">Listede, seçili satırı işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="d576f-117">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="d576f-118">Kanban 000177 içeren satırı seçin.</span><span class="sxs-lookup"><span data-stu-id="d576f-118">Select line with Kanban 000177.</span></span>  
4. <span data-ttu-id="d576f-119">Alternatif kanban kuralı kullan'ı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="d576f-119">Click Use alternative kanban rule.</span></span>
5. <span data-ttu-id="d576f-120">İleri düğmesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="d576f-120">Click Next.</span></span>
6. <span data-ttu-id="d576f-121">Kanban kuralı alanında bir değer girin veya bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="d576f-121">In the Kanban rule field, enter or select a value.</span></span>
    * <span data-ttu-id="d576f-122">Daha önce oluşturulan kanban kuralını seçin.</span><span class="sxs-lookup"><span data-stu-id="d576f-122">Select the kanban rule that was created earlier.</span></span> <span data-ttu-id="d576f-123">Bu, en büyük sayıya sahip kanban kuralıdır.</span><span class="sxs-lookup"><span data-stu-id="d576f-123">This is the kanban rule with the highest number.</span></span>  
7. <span data-ttu-id="d576f-124">Son düğmesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="d576f-124">Click Finish.</span></span>
    * <span data-ttu-id="d576f-125">Kanban işi şimdi artık başka bir kanban kuralını kullanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="d576f-125">Now the kanban job is using an another kanban rule.</span></span> <span data-ttu-id="d576f-126">Bu, yük iş hücrelerini eşitlemek için yararlı olabilir.</span><span class="sxs-lookup"><span data-stu-id="d576f-126">This can be useful to level load work cells.</span></span>  

