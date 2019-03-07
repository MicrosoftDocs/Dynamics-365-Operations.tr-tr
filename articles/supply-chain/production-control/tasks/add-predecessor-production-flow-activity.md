---
title: Üretim akışı faaliyetine bir öncel ekleme
description: Üretim akışı sürümünde, tüm faaliyetlerin sıralı olması gerekir.
author: cvocph
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LeanProductionFlow, PlanActivity, PlanActivityRelationNew, PlanActivityLookup
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: conradv
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 9acb1c2672af70f535f3dce1c8f5a97e8d479158
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2019
ms.locfileid: "343685"
---
# <a name="add-a-predecessor-to-a-production-flow-activity"></a><span data-ttu-id="12941-103">Üretim akışı faaliyetine bir öncel ekleme</span><span class="sxs-lookup"><span data-stu-id="12941-103">Add a predecessor to a production flow activity</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="12941-104">Üretim akışı sürümünde, tüm faaliyetlerin sıralı olması gerekir.</span><span class="sxs-lookup"><span data-stu-id="12941-104">In a production flow version, all activities must be sequenced.</span></span> <span data-ttu-id="12941-105">Bir faaliyet bir veya daha fazla öncele ve ardıla sahip olabilir.</span><span class="sxs-lookup"><span data-stu-id="12941-105">An activity can have one or multiple predecessors or successors.</span></span> 

<span data-ttu-id="12941-106">Bu yordam bir önceli bir faaliyetle ilişkilendirmeyi gösterir.</span><span class="sxs-lookup"><span data-stu-id="12941-106">This procedure shows how to associate a predecessor to an activity.</span></span> 

<span data-ttu-id="12941-107">Bu görevi gerçekleştirmek için, birbirine bağlanabilen en az iki faaliyetin olduğu Taslak sürümüne sahip bir üretim akışına ihtiyacınız vardır.</span><span class="sxs-lookup"><span data-stu-id="12941-107">To perform this task, you need a production flow that has the Draft version with at least two activities that can be connected.</span></span> 

<span data-ttu-id="12941-108">Daha fazla bilgi için, "Üretim akışları ve yalın imalat faaliyetleri" başlıklı teknik raporu okuyun.</span><span class="sxs-lookup"><span data-stu-id="12941-108">To learn more, read the white paper "Production flows and activities in lean manufacturing."</span></span>


## <a name="find-the-production-flow-and-version"></a><span data-ttu-id="12941-109">Üretim akışını ve sürümünü bulma</span><span class="sxs-lookup"><span data-stu-id="12941-109">Find the production flow and version</span></span>
1. <span data-ttu-id="12941-110">Üretim kontrolü > Kurulum > Yalın üretim akışı > Üretim akışları seçeneğine gidin.</span><span class="sxs-lookup"><span data-stu-id="12941-110">Go to Production control > Setup > Lean production flow > Production flows.</span></span>
2. <span data-ttu-id="12941-111">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="12941-111">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="12941-112">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="12941-112">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="12941-113">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="12941-113">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="12941-114">Faaliyetler'i tıklatın.</span><span class="sxs-lookup"><span data-stu-id="12941-114">Click Activities.</span></span>

## <a name="select-an-activity-and-add-a-predecessor"></a><span data-ttu-id="12941-115">Faaliyet seçme ve öncel ekleme</span><span class="sxs-lookup"><span data-stu-id="12941-115">Select an activity and add a predecessor</span></span>
1. <span data-ttu-id="12941-116">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="12941-116">In the list, find and select the desired record.</span></span>
2. <span data-ttu-id="12941-117">Öncel ekle öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="12941-117">Click Add predecessor.</span></span>
3. <span data-ttu-id="12941-118">Faaliyet alanına bir değer girin veya buradan bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="12941-118">In the Activity field, enter or select a value.</span></span>
4. <span data-ttu-id="12941-119">Döngü süresi oranı alanında bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="12941-119">In the Cycle time ratio field, enter a number.</span></span>
    * <span data-ttu-id="12941-120">Bir faaliyet ilişkisinin varsayılan döngü süresi oranı 1'dir.</span><span class="sxs-lookup"><span data-stu-id="12941-120">The default cycle time ratio of an activity relation is 1.</span></span> <span data-ttu-id="12941-121">Bu her iki faaliyetin de aynı takt zamanında çalıştığını varsayar.</span><span class="sxs-lookup"><span data-stu-id="12941-121">This assumes that both activities run at the same pace or takt time.</span></span> <span data-ttu-id="12941-122">Öncel daha yüksek bir hızda çalışıyorsa (daha düşük takt süresi), bu oran 1'den düşük olmalıdır; öncel daha düşük bir hızda çalışıyorsa (daha yüksek takt süresi), döngü süresi oranı 1'den büyük olur.</span><span class="sxs-lookup"><span data-stu-id="12941-122">If the predecessor runs at a higher pace (lower takt time), the ratio should be lower than 1, if the predecessor runs at a slower pace (higher takt time) the cycle time ratio is greater than 1.</span></span>  
5. <span data-ttu-id="12941-123">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="12941-123">Click OK.</span></span>

