---
title: Bütçe planlama veri tahsisatı
description: Bu konu, Microsoft Dynamics 365 Finance içerisindeki tahsisat yöntemlerini ve bunların nasıl kullanılabileceklerini açıklar.
author: ShylaThompson
ms.date: 03/05/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BudgetPlanningConfiguration
audience: Application User
ms.reviewer: roschlom
ms.custom: 15191
ms.assetid: 89a918e8-59a4-4711-a2e9-b41989ddd0f1
ms.search.region: Global
ms.author: sigitac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: bef79df8d9806771f87a6f77a0c9094887050646
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/01/2021
ms.locfileid: "5822215"
---
# <a name="budget-planning-data-allocation"></a><span data-ttu-id="01a72-103">Bütçe planlama veri tahsisatı</span><span class="sxs-lookup"><span data-stu-id="01a72-103">Budget planning data allocation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="01a72-104">Bu konu, Microsoft Dynamics 365 Finance içerisindeki tahsisat yöntemlerini ve bunların nasıl kullanılabileceklerini açıklar.</span><span class="sxs-lookup"><span data-stu-id="01a72-104">This topic describes the allocation methods that are available in Microsoft Dynamics 365 Finance and how they can be used.</span></span>  

<span data-ttu-id="01a72-105">Kestirilen tutarları doğru şekilde değerlendirebilmek için bir bütçe planındaki verileri farklı şekillerde dağıtabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="01a72-105">You can distribute the data in a budget plan in a number of ways to accurately portray the projected amounts.</span></span>

## <a name="allocation-methods"></a><span data-ttu-id="01a72-106">Tahsisat yöntemleri</span><span class="sxs-lookup"><span data-stu-id="01a72-106">Allocation methods</span></span>
<span data-ttu-id="01a72-107">Aynı bütçe planında bulunan satırlara dayalı olarak bütçe plan satırları oluşturulması için kullanılabilecek üç tahsisat yöntemi (Dönemler arasında tahsis et, Boyutlara tahsis et ve Genel muhasebe tahsisat kurallarını kullan) bulunmaktadır.</span><span class="sxs-lookup"><span data-stu-id="01a72-107">Three allocation methods (Allocate across periods, Allocate to dimensions, and Use ledger allocation rules) can create budget plan lines that are based on lines in the same budget plan.</span></span> <span data-ttu-id="01a72-108">Diğer bütçe planlarında bütçe planı satırları oluşturulması için kullanılabilecek üç yöntem (Toplama, Dağıtma ve Bütçe planından kopyalama) daha vardır.</span><span class="sxs-lookup"><span data-stu-id="01a72-108">Three other methods (Aggregate, Distribute, and Copy from budget plan) can create budget plan lines in other budget plans.</span></span> <span data-ttu-id="01a72-109">Altı tahsisat yönteminin her birinde hedef senaryoyu belirtirsiniz.</span><span class="sxs-lookup"><span data-stu-id="01a72-109">For all six allocation methods, you specify the destination scenario.</span></span> <span data-ttu-id="01a72-110">Hedef senaryo, kaynak senaryoyla aynı veya kaynak senaryodan farklı olabilir.</span><span class="sxs-lookup"><span data-stu-id="01a72-110">The destination scenario can be either the same as the source scenario or different from the source scenario.</span></span> <span data-ttu-id="01a72-111">Ek olarak, yeni satırların bütçe planına dahil mi edileceğini, yoksa bütçe planındaki mevcut satırların yerini mi alacağını tanımlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="01a72-111">Additionally, you can specify whether new lines are appended to the budget plan or replace the current lines in the budget plan.</span></span>

> [!NOTE] 
> <span data-ttu-id="01a72-112">Dağıtım veya daha önce ana planda gerçekleştirilen diğer değişiklikler için kullanılan senaryodan farklı bir toplam için benzersiz bir senaryo kullanılmalıdır.</span><span class="sxs-lookup"><span data-stu-id="01a72-112">A unique scenario should be used for aggregation that is different from the scenario that was used for distribution or other modifications that were previously performed  in the parent plan.</span></span>  

<span data-ttu-id="01a72-113">[![Dönemler genelinde tahsis etme tahsisat yöntemi](./media/allocateacrossperiods-300x259.png)](./media/allocateacrossperiods.png)
**Dönemler genelinde tahsis et**: Bütçe planı satırlarını kaynak bütçe planı senaryosundan hedef senaryodaki dönemler genelinde tahsis etmek için bir dönem tahsisat kategorisi kullanılır.</span><span class="sxs-lookup"><span data-stu-id="01a72-113">[![Allocate across Periods allocation method](./media/allocateacrossperiods-300x259.png)](./media/allocateacrossperiods.png)
**Allocate across periods** – A period allocation category is used to allocate the budget plan lines from the source budget plan scenario across periods in the destination scenario.</span></span> <span data-ttu-id="01a72-114">Kaynak tutarı, dönem tahsisat kategorisinde tanımlanan yüzdeye ve tarihe dayalı olarak hedef senaryodaki birden fazla satıra tahsis edilir.</span><span class="sxs-lookup"><span data-stu-id="01a72-114">The source amount is assigned to multiple lines in the destination scenario, based on the percentage and date that are defined in the period allocation category.</span></span>         

<span data-ttu-id="01a72-115">[![Boyutlara tahsis etme tahsisat yöntemi](./media/allocatetodimensions.jpg)](./media/allocatetodimensions.jpg)
**Boyutlara tahsis et**: Bütçe planı satırları, seçilen bir bütçe tahsisat koşulunda tanımlanan yüzdelere ve mali boyutlara göre kaynak bütçe planlama senaryosundan hedef senaryodaki bir veya daha fazla satıra tahsis edilir.</span><span class="sxs-lookup"><span data-stu-id="01a72-115">[![Allocate to Dimensions allocation method](./media/allocatetodimensions.jpg)](./media/allocatetodimensions.jpg)
**Allocate to dimensions** – The budget plan lines are allocated from the source budget planning scenario to one or more lines in the destination scenario, based on the percentages and financial dimensions that are defined in a selected budget allocation term.</span></span>           

<span data-ttu-id="01a72-116">![Grafiği toplama](./media/aggregatechart-300x230.png)
**Toplama**: Bütçe planı satırları, ilişkili (alt) bütçe planlarındaki kaynak bütçe planı senaryosundan ana bütçe planındaki hedef senaryoya toplanır.</span><span class="sxs-lookup"><span data-stu-id="01a72-116">![Aggregate chart](./media/aggregatechart-300x230.png)
**Aggregate** – The budget plan lines are aggregated from the source budget plan scenario in the associated (child) budget plans to the destination scenario in the parent budget plan.</span></span> <span data-ttu-id="01a72-117">Bu yöntem, organizasyonun bir alt düzeyinde hazırlanan bütçe tutarlarının daha yüksek bir düzeyde birleştirilmesini sağlar.</span><span class="sxs-lookup"><span data-stu-id="01a72-117">This method enables budget amounts that are prepared at a lower level in the organization to be consolidated at a higher level.</span></span>          

<span data-ttu-id="01a72-118">[![Grafiği dağıtma](./media/distributechart-300x230.png)](./media/distributechart.png)
**Dağıt**: Bütçe planı satırları, ilişkili planların organizasyon birimlerinin mali boyutlarına göre ana bütçe planındaki kaynak bütçe planlama senaryosundan ilişkili (alt) bütçe planlarındaki hedef senaryoya dağıtılır.</span><span class="sxs-lookup"><span data-stu-id="01a72-118">[![Distribute chart](./media/distributechart-300x230.png)](./media/distributechart.png)
**Distribute** – The budget plan lines are distributed from the source budget planning scenario in the parent budget plan to the destination scenario in the associated (child) budget plans, based on the financial dimensions of the organization units of the associated plans.</span></span> <span data-ttu-id="01a72-119">Bu yöntem, organizasyonun bir üst düzeyinde hazırlanan bütçe tutarlarının daha lokal bir değerlendirme için dağıtılmasını sağlar.</span><span class="sxs-lookup"><span data-stu-id="01a72-119">This method enables budget amounts that are prepared at a higher level in the organization to be spread out for more localized review.</span></span>           

<span data-ttu-id="01a72-120">[![Genel muhasebe tahsisat kuralları](./media/ledgerallocationrules-300x202.png)](./media/ledgerallocationrules.png)
**Genel muhasebe tahsisat kurallarını kullan**: Bütçe planı satırları, seçilen genel muhasebe tahsisat kuralına göre kaynak bütçe planlama senaryosundan hedef senaryoya dağıtılır.</span><span class="sxs-lookup"><span data-stu-id="01a72-120">[![Ledger allocation rules](./media/ledgerallocationrules-300x202.png)](./media/ledgerallocationrules.png)
**Use ledger allocation rules** – The budget plan lines are distributed from the source budget planning scenario to the destination scenario, based on the ledger allocation rule that is selected.</span></span> 

<span data-ttu-id="01a72-121">[![Bütçe planından kopyalama](./media/copyfrombudgetplan-187x300.png)](./media/copyfrombudgetplan.png)
**Bütçe planından kopyala**: Dağıtma tahsisat yönteminde olduğu gibi, ilgili bir bütçe planındaki satırlara göre hedefte bütçe planı satırları oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="01a72-121">[![Copy from budget plan](./media/copyfrombudgetplan-187x300.png)](./media/copyfrombudgetplan.png)
**Copy from budget plan** – As in the Distribute allocation method, budget plan lines are created in the destination, based on lines in a related budget plan.</span></span> <span data-ttu-id="01a72-122">Ancak, bu yöntem için, kaynak bütçe planının ana plan olması zorunlu değildir, bütçe planı hiyerarşisinde daha yüksek bir düzeyde bulunabilir.</span><span class="sxs-lookup"><span data-stu-id="01a72-122">However, for this method, the source budget plan doesn't have to be the parent but can be at any higher level in the budget plan hierarchy.</span></span> <span data-ttu-id="01a72-123">Bu tahsisat yöntemi, konsolide tutarların orijinal olarak çok yüksek bir düzeyde bütçelendiği ve daha üst düzeyde bir onay almadan önce ayrıntılı şekilde gözden geçirilmesi ve düzenlenmesi için organizasyonun daha alt bir düzeyine transfer edilmesinin gerektiği durumlarda kullanışlıdır.</span><span class="sxs-lookup"><span data-stu-id="01a72-123">This allocation method is useful if consolidated amounts are originally budgeted at a much higher level, and must be transferred to a lower level of the organization for detailed review and adjustment before they can receive upper-level approval.</span></span>          

## <a name="using-allocation-methods-in-a-budget-plan"></a><span data-ttu-id="01a72-124">Bir bütçe planında tahsisat yöntemlerini kullanma</span><span class="sxs-lookup"><span data-stu-id="01a72-124">Using allocation methods in a budget plan</span></span>
<span data-ttu-id="01a72-125">Bütçe planı sayfasında tahsisatlar gerçekleştirmek için, tahsis edilecek satırları seçin ve ardından **Bütçeyi tahsis et** öğesini tıklayın.</span><span class="sxs-lookup"><span data-stu-id="01a72-125">To perform allocations on the budget plan page, select the lines to allocate, and then click **Allocate budget**.</span></span>

<span data-ttu-id="01a72-126">[![Bütçe tahsis et düğmesi](./media/allocatebudgetbutton-300x84.png)](./media/allocatebudgetbutton.png)</span><span class="sxs-lookup"><span data-stu-id="01a72-126">[![Allocate budget button](./media/allocatebudgetbutton-300x84.png)](./media/allocatebudgetbutton.png)</span></span> 

<span data-ttu-id="01a72-127">Ardından, bir tahsisat yöntemi seçin.</span><span class="sxs-lookup"><span data-stu-id="01a72-127">Next, select an allocation method.</span></span> <span data-ttu-id="01a72-128">Kalan alanlar, seçtiğiniz yönteme dayalı olarak ayarlanır.</span><span class="sxs-lookup"><span data-stu-id="01a72-128">The remaining fields are then set, based on the method that you selected.</span></span> <span data-ttu-id="01a72-129">Bu alanlara bütçe planı verilerinin kaynağı ve hedefi ve ayrıca toplu iş ayarının kolaylaşması açısından hedef tutarları oluşturulduğunda kaynağı belirtilen bir faktörle çarpmanıza izin veren bir seçenek dahildir.</span><span class="sxs-lookup"><span data-stu-id="01a72-129">These fields include the source and destination of the budget plan data, and an option that lets you multiply the source by a specified factor when the destination amounts are created, to simplify bulk adjustment.</span></span> <span data-ttu-id="01a72-130">Ayrıca, **Planla ekle** seçeneğini de kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="01a72-130">You can also set the **Append to plan** option.</span></span> <span data-ttu-id="01a72-131">Mevcut bütçe planı satırlarını değiştirmek için **Hayır** öğesini veya mevcut bütçe planı satırlarını tutmak ve tahsis edilen tutarlar için yeni satırlar eklemek için **Evet** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="01a72-131">Select **No** to replace the existing budget plan lines, or select **Yes** to retain the existing budget plan lines and add new lines for the allocated amounts.</span></span>

## <a name="automating-allocations-during-a-workflow"></a><span data-ttu-id="01a72-132">Bir iş akışı sırasında tahsisatları otomatik hale getirme</span><span class="sxs-lookup"><span data-stu-id="01a72-132">Automating allocations during a workflow</span></span>
<span data-ttu-id="01a72-133">Tahsisatların bir bütçe planlama iş akışının bir parçası olarak otomatik şekilde gerçekleştirilmesini sağlayan önemli bir özelliktir.</span><span class="sxs-lookup"><span data-stu-id="01a72-133">One powerful feature enables allocations to be performed automatically as part of a budget planning workflow.</span></span> <span data-ttu-id="01a72-134">Bir bütçe planı, iş akışından geçerken, otomatik hale getirilmiş görevler, belirtilen bir bütçe planlama aşamasında tahsisatı etkinleştirebilir.</span><span class="sxs-lookup"><span data-stu-id="01a72-134">As a budget plan moves through its workflow, automated tasks can invoke an allocation at a specified budget planning stage.</span></span> 

<span data-ttu-id="01a72-135">Otomatik tahsisatı ayarlamak için öncelikle **Bütçe planlama yapılandırma** sayfasından bir tahsisat programı oluşturmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="01a72-135">To set up automated allocation, you must first create an allocation schedule on the **Budget planning configuration** page.</span></span> <span data-ttu-id="01a72-136">Tahsisat programı, otomatik tahsisat çalıştırıldığında kullanılacak tahsisat yöntemini ve çeşitli tahsisat seçeneklerinin (açıklamalar için önceki bölüme bakın) değerlerini tanımlar.</span><span class="sxs-lookup"><span data-stu-id="01a72-136">The allocation schedule defines the allocation method that will be used when the automated allocation is run, and the values of the various allocation options (see the previous section for descriptions).</span></span> 

<span data-ttu-id="01a72-137">Ardından, **Bütçe Planlama Yapılandırma** sayfasından bir aşama tahsisatı oluşturursunuz.</span><span class="sxs-lookup"><span data-stu-id="01a72-137">Next, you create a stage allocation on the **Budget planning configuration** page.</span></span> <span data-ttu-id="01a72-138">Aşama tahsisatı, bütçe planlama iş akışına ve aşamasına bir tahsisat programı atar.</span><span class="sxs-lookup"><span data-stu-id="01a72-138">The stage allocation assigns an allocation schedule to the budget planning workflow and stage.</span></span> 

<span data-ttu-id="01a72-139">Son olarak, istediğiniz iş akışı aşamasında bütçe planlama aşama tahsisatı için bir otomatik görev ekleyin.</span><span class="sxs-lookup"><span data-stu-id="01a72-139">Finally, add an automated task for budget planning stage allocation at the desired workflow stage.</span></span> <span data-ttu-id="01a72-140">Aşağıdaki örnekte, iş akışına iki adet bütçe planlama aşaması tahsisatı (kırmızı çerçeve içine alınmıştır) eklenmiştir.</span><span class="sxs-lookup"><span data-stu-id="01a72-140">In the following example, two budget planning stage allocations (outlined in red) have been inserted into the workflow.</span></span>

<span data-ttu-id="01a72-141">[![Bütçe planlaması aşama tahsisatları](./media/budgetplanningstageallocations-300x300.png)](./media/budgetplanningstageallocations.png)</span><span class="sxs-lookup"><span data-stu-id="01a72-141">[![Budget planning stage allocations](./media/budgetplanningstageallocations-300x300.png)](./media/budgetplanningstageallocations.png)</span></span>





[!INCLUDE[footer-include](../../includes/footer-banner.md)]