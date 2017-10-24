---
title: "Bütçe planlaması veri tahsisatı"
description: "Bu makale, Microsoft Dynamics 365 for Finance and Operations, Enterprise edition içerisindeki çeşitli tahsisat yöntemlerini ve bunların nasıl kullanılabileceklerini açıklar."
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: BudgetPlanningConfiguration
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 15191
ms.assetid: 89a918e8-59a4-4711-a2e9-b41989ddd0f1
ms.search.region: Global
ms.author: sigitac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: fd7ec30c8253f343b3d41d54c78696cd512b2ef7
ms.contentlocale: tr-tr
ms.lasthandoff: 09/29/2017

---

# <a name="budget-planning-data-allocation"></a><span data-ttu-id="9b2c8-103">Bütçe planlama veri tahsisatı</span><span class="sxs-lookup"><span data-stu-id="9b2c8-103">Budget planning data allocation</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="9b2c8-104">Bu makale, Microsoft Dynamics 365 for Finance and Operations, Enterprise edition içerisindeki çeşitli tahsisat yöntemlerini ve bunların nasıl kullanılabileceklerini açıklar.</span><span class="sxs-lookup"><span data-stu-id="9b2c8-104">This article describes the various allocation methods that are available in Microsoft Dynamics 365 for Finance and Operations, Enterprise edition and how they can be used.</span></span>  

<span data-ttu-id="9b2c8-105">Kestirilen tutarları doğru şekilde değerlendirebilmek için bir bütçe planındaki verileri farklı şekillerde dağıtabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="9b2c8-105">You can distribute the data in a budget plan in a number of ways to accurately portray the projected amounts.</span></span>

## <a name="allocation-methods"></a><span data-ttu-id="9b2c8-106">Tahsisat yöntemleri</span><span class="sxs-lookup"><span data-stu-id="9b2c8-106">Allocation methods</span></span>
<span data-ttu-id="9b2c8-107">Aynı bütçe planında bulunan satırlara dayalı olarak bütçe plan satırları oluşturulması için kullanılabilecek üç tahsisat yöntemi (Dönemler arasında tahsis et, Boyutlara tahsis et ve Genel muhasebe tahsisat kurallarını kullan) bulunmaktadır.</span><span class="sxs-lookup"><span data-stu-id="9b2c8-107">Three allocation methods (Allocate across periods, Allocate to dimensions, and Use ledger allocation rules) can create budget plan lines that are based on lines in the same budget plan.</span></span> <span data-ttu-id="9b2c8-108">Diğer bütçe planlarında bütçe planı satırları oluşturulması için kullanılabilecek üç yöntem (Toplama, Dağıtma ve Bütçe planından kopyalama) daha vardır.</span><span class="sxs-lookup"><span data-stu-id="9b2c8-108">Three other methods (Aggregate, Distribute, and Copy from budget plan) can create budget plan lines in other budget plans.</span></span> <span data-ttu-id="9b2c8-109">Altı tahsisat yönteminin her birinde hedef senaryoyu belirtirsiniz.</span><span class="sxs-lookup"><span data-stu-id="9b2c8-109">For all six allocation methods, you specify the destination scenario.</span></span> <span data-ttu-id="9b2c8-110">Hedef senaryo, kaynak senaryoyla aynı veya kaynak senaryodan farklı olabilir.</span><span class="sxs-lookup"><span data-stu-id="9b2c8-110">The destination scenario can be either the same as the source scenario or different from the source scenario.</span></span> <span data-ttu-id="9b2c8-111">Ek olarak, yeni satırların bütçe planına dahil mi edileceğini, yoksa bütçe planındaki mevcut satırların yerini mi alacağını tanımlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="9b2c8-111">Additionally, you can specify whether new lines are appended to the budget plan or replace the current lines in the budget plan.</span></span>

<span data-ttu-id="9b2c8-112">[![AllocateAcrossPeriods](./media/allocateacrossperiods-300x259.png)](./media/allocateacrossperiods.png)
**Dönemler Arasında Tahsis Et** – Bütçe planı satırlarını kaynak bütçe planı senaryosundan hedef senaryodaki dönemler arasında tahsis etmek için bir dönem tahsisat kategorisi kullanılır.</span><span class="sxs-lookup"><span data-stu-id="9b2c8-112">[![AllocateAcrossPeriods](./media/allocateacrossperiods-300x259.png)](./media/allocateacrossperiods.png)
**Allocate across periods** – A period allocation category is used to allocate the budget plan lines from the source budget plan scenario across periods in the destination scenario.</span></span> <span data-ttu-id="9b2c8-113">Kaynak tutarı, dönem tahsisat kategorisinde tanımlanan yüzdeye ve tarihe dayalı olarak hedef senaryodaki birden fazla satıra tahsis edilir.</span><span class="sxs-lookup"><span data-stu-id="9b2c8-113">The source amount is assigned to multiple lines in the destination scenario, based on the percentage and date that are defined in the period allocation category.</span></span>         

<span data-ttu-id="9b2c8-114">[![AllocateToDimensions](./media/allocatetodimensions.jpg)](./media/allocatetodimensions.jpg)
**Boyutlara tahsis et** – Bütçe planı satırları, seçilen bir bütçe tahsisat koşulunda tanımlanan yüzdelere ve mali boyutlara dayalı olarak, kaynak bütçe planlama senaryosundan hedef senaryodaki bir veya daha fazla sayıda satıra tahsis edilir.</span><span class="sxs-lookup"><span data-stu-id="9b2c8-114">[![AllocateToDimensions](./media/allocatetodimensions.jpg)](./media/allocatetodimensions.jpg)
**Allocate to dimensions** – The budget plan lines are allocated from the source budget planning scenario to one or more lines in the destination scenario, based on the percentages and financial dimensions that are defined in a selected budget allocation term.</span></span>           

<span data-ttu-id="9b2c8-115">![AggregateChart](./media/aggregatechart-300x230.png)
**Toplama** – Bütçe planı satırları, ilgili (alt) bütçe planlarındaki kaynak bütçe planı senaryodan ana bütçe planındaki hedef senaryoya toplanır.</span><span class="sxs-lookup"><span data-stu-id="9b2c8-115">![AggregateChart](./media/aggregatechart-300x230.png)
**Aggregate** – The budget plan lines are aggregated from the source budget plan scenario in the associated (child) budget plans to the destination scenario in the parent budget plan.</span></span> <span data-ttu-id="9b2c8-116">Bu yöntem, organizasyonun bir alt düzeyinde hazırlanan bütçe tutarlarının daha yüksek bir düzeyde birleştirilmesini sağlar.</span><span class="sxs-lookup"><span data-stu-id="9b2c8-116">This method enables budget amounts that are prepared at a lower level in the organization to be consolidated at a higher level.</span></span>          

<span data-ttu-id="9b2c8-117">[![DistributeChart](./media/distributechart-300x230.png)](./media/distributechart.png)
**Dağıt** – Bütçe planı satırları, ilgili planların organizasyon birimlerinin mali boyutlarına dayalı olarak, ana bütçe planındaki kaynak bütçe planlama senaryosundan ilgili (alt) bütçe planlarındaki hedef senaryoya dağıtılır.</span><span class="sxs-lookup"><span data-stu-id="9b2c8-117">[![DistributeChart](./media/distributechart-300x230.png)](./media/distributechart.png)
**Distribute** – The budget plan lines are distributed from the source budget planning scenario in the parent budget plan to the destination scenario in the associated (child) budget plans, based on the financial dimensions of the organization units of the associated plans.</span></span> <span data-ttu-id="9b2c8-118">Bu yöntem, organizasyonun bir üst düzeyinde hazırlanan bütçe tutarlarının daha lokal bir değerlendirme için dağıtılmasını sağlar.</span><span class="sxs-lookup"><span data-stu-id="9b2c8-118">This method enables budget amounts that are prepared at a higher level in the organization to be spread out for more localized review.</span></span>           

<span data-ttu-id="9b2c8-119">[![LedgerAllocationRules](./media/ledgerallocationrules-300x202.png)](./media/ledgerallocationrules.png)
**Genel muhasebe tahsisat kurallarını kullan** – Bütçe planı satırları, seçilen genel muhasebe tahsisat kuralına dayalı olarak kaynak bütçe planlama senaryosundan hedef senaryoya dağıtılır.</span><span class="sxs-lookup"><span data-stu-id="9b2c8-119">[![LedgerAllocationRules](./media/ledgerallocationrules-300x202.png)](./media/ledgerallocationrules.png)
**Use ledger allocation rules** – The budget plan lines are distributed from the source budget planning scenario to the destination scenario, based on the ledger allocation rule that is selected.</span></span> 

<span data-ttu-id="9b2c8-120">[![CopyFromBudgetPlan](./media/copyfrombudgetplan-187x300.png)](./media/copyfrombudgetplan.png)
**Bütçe planından kopyala** – Dağıtma tahsisat yönteminde olduğu gibi, ilgili bir bütçe planındaki satırlara dayalı olarak, hedefte bütçe planı satırları oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="9b2c8-120">[![CopyFromBudgetPlan](./media/copyfrombudgetplan-187x300.png)](./media/copyfrombudgetplan.png)
**Copy from budget plan** – As in the Distribute allocation method, budget plan lines are created in the destination, based on lines in a related budget plan.</span></span> <span data-ttu-id="9b2c8-121">Ancak, bu yöntem için, kaynak bütçe planının ana plan olması zorunlu değildir, bütçe planı hiyerarşisinde daha yüksek bir düzeyde bulunabilir.</span><span class="sxs-lookup"><span data-stu-id="9b2c8-121">However, for this method, the source budget plan doesn't have to be the parent but can be at any higher level in the budget plan hierarchy.</span></span> <span data-ttu-id="9b2c8-122">Bu tahsisat yöntemi, konsolide tutarların orijinal olarak çok yüksek bir düzeyde bütçelendiği ve daha üst düzeyde bir onay almadan önce ayrıntılı şekilde gözden geçirilmesi ve düzenlenmesi için organizasyonun daha alt bir düzeyine transfer edilmesinin gerektiği durumlarda kullanışlıdır.</span><span class="sxs-lookup"><span data-stu-id="9b2c8-122">This allocation method is useful if consolidated amounts are originally budgeted at a much higher level, and must be transferred to a lower level of the organization for detailed review and adjustment before they can receive upper-level approval.</span></span>          

## <a name="using-allocation-methods-in-a-budget-plan"></a><span data-ttu-id="9b2c8-123">Bir bütçe planında tahsisat yöntemlerini kullanma</span><span class="sxs-lookup"><span data-stu-id="9b2c8-123">Using allocation methods in a budget plan</span></span>
<span data-ttu-id="9b2c8-124">Bütçe planı sayfasında tahsisatlar gerçekleştirmek için, tahsis edilecek satırları seçin ve ardından **Bütçeyi tahsis et** öğesini tıklayın.</span><span class="sxs-lookup"><span data-stu-id="9b2c8-124">To perform allocations on the budget plan page, select the lines to allocate, and then click **Allocate budget**.</span></span>

<span data-ttu-id="9b2c8-125">[![AllocateBudgetButton](./media/allocatebudgetbutton-300x84.png)](./media/allocatebudgetbutton.png)</span><span class="sxs-lookup"><span data-stu-id="9b2c8-125">[![AllocateBudgetButton](./media/allocatebudgetbutton-300x84.png)](./media/allocatebudgetbutton.png)</span></span> 

<span data-ttu-id="9b2c8-126">Ardından, bir tahsisat yöntemi seçin.</span><span class="sxs-lookup"><span data-stu-id="9b2c8-126">Next, select an allocation method.</span></span> <span data-ttu-id="9b2c8-127">Kalan alanlar, seçtiğiniz yönteme dayalı olarak ayarlanır.</span><span class="sxs-lookup"><span data-stu-id="9b2c8-127">The remaining fields are then set, based on the method that you selected.</span></span> <span data-ttu-id="9b2c8-128">Bu alanlara bütçe planı verilerinin kaynağı ve hedefi ve ayrıca toplu iş ayarının kolaylaşması açısından hedef tutarları oluşturulduğunda kaynağı belirtilen bir faktörle çarpmanıza izin veren bir seçenek dahildir.</span><span class="sxs-lookup"><span data-stu-id="9b2c8-128">These fields include the source and destination of the budget plan data, and an option that lets you multiply the source by a specified factor when the destination amounts are created, to simplify bulk adjustment.</span></span> <span data-ttu-id="9b2c8-129">Ayrıca, **Planla ekle** seçeneğini de kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="9b2c8-129">You can also set the **Append to plan** option.</span></span> <span data-ttu-id="9b2c8-130">Mevcut bütçe planı satırlarını değiştirmek için **Hayır** öğesini veya mevcut bütçe planı satırlarını tutmak ve tahsis edilen tutarlar için yeni satırlar eklemek için **Evet** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="9b2c8-130">Select **No** to replace the existing budget plan lines, or select **Yes** to retain the existing budget plan lines and add new lines for the allocated amounts.</span></span>

## <a name="automating-allocations-during-a-workflow"></a><span data-ttu-id="9b2c8-131">Bir iş akışı sırasında tahsisatları otomatik hale getirme</span><span class="sxs-lookup"><span data-stu-id="9b2c8-131">Automating allocations during a workflow</span></span>
<span data-ttu-id="9b2c8-132">Tahsisatların bir bütçe planlama iş akışının bir parçası olarak otomatik şekilde gerçekleştirilmesini sağlayan önemli bir özelliktir.</span><span class="sxs-lookup"><span data-stu-id="9b2c8-132">One powerful feature enables allocations to be performed automatically as part of a budget planning workflow.</span></span> <span data-ttu-id="9b2c8-133">Bir bütçe planı, iş akışından geçerken, otomatik hale getirilmiş görevler, belirtilen bir bütçe planlama aşamasında tahsisatı etkinleştirebilir.</span><span class="sxs-lookup"><span data-stu-id="9b2c8-133">As a budget plan moves through its workflow, automated tasks can invoke an allocation at a specified budget planning stage.</span></span> 

<span data-ttu-id="9b2c8-134">Otomatik tahsisatı ayarlamak için öncelikle **Bütçe planlama yapılandırma** sayfasından bir tahsisat programı oluşturmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="9b2c8-134">To set up automated allocation, you must first create an allocation schedule on the **Budget planning configuration** page.</span></span> <span data-ttu-id="9b2c8-135">Tahsisat programı, otomatik tahsisat çalıştırıldığında kullanılacak tahsisat yöntemini ve çeşitli tahsisat seçeneklerinin (açıklamalar için önceki bölüme bakın) değerlerini tanımlar.</span><span class="sxs-lookup"><span data-stu-id="9b2c8-135">The allocation schedule defines the allocation method that will be used when the automated allocation is run, and the values of the various allocation options (see the previous section for descriptions).</span></span> 

<span data-ttu-id="9b2c8-136">Ardından, **Bütçe Planlama Yapılandırma** sayfasından bir aşama tahsisatı oluşturursunuz.</span><span class="sxs-lookup"><span data-stu-id="9b2c8-136">Next, you create a stage allocation on the **Budget planning configuration** page.</span></span> <span data-ttu-id="9b2c8-137">Aşama tahsisatı, bütçe planlama iş akışına ve aşamasına bir tahsisat programı atar.</span><span class="sxs-lookup"><span data-stu-id="9b2c8-137">The stage allocation assigns an allocation schedule to the budget planning workflow and stage.</span></span> 

<span data-ttu-id="9b2c8-138">Son olarak, istediğiniz iş akışı aşamasında bütçe planlama aşama tahsisatı için bir otomatik görev ekleyin.</span><span class="sxs-lookup"><span data-stu-id="9b2c8-138">Finally, add an automated task for budget planning stage allocation at the desired workflow stage.</span></span> <span data-ttu-id="9b2c8-139">Aşağıdaki örnekte, iş akışına iki adet bütçe planlama aşaması tahsisatı (kırmızı çerçeve içine alınmıştır) eklenmiştir.</span><span class="sxs-lookup"><span data-stu-id="9b2c8-139">In the following example, two budget planning stage allocations (outlined in red) have been inserted into the workflow.</span></span>

<span data-ttu-id="9b2c8-140">[![BudgetPlanningStageAllocations](./media/budgetplanningstageallocations-300x300.png)](./media/budgetplanningstageallocations.png)</span><span class="sxs-lookup"><span data-stu-id="9b2c8-140">[![BudgetPlanningStageAllocations](./media/budgetplanningstageallocations-300x300.png)](./media/budgetplanningstageallocations.png)</span></span>




