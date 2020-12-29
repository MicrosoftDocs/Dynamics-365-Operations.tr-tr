---
title: Üretim akışı faaliyetine bir öncel ekleme
description: Üretim akışı sürümünde, tüm faaliyetlerin sıralı olması gerekir.
author: cvocph
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LeanProductionFlow, PlanActivity, PlanActivityRelationNew, PlanActivityLookup
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: c39cef1174439b42a072bd7fc1ac29ef31ecf864
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "4439030"
---
# <a name="add-a-predecessor-to-a-production-flow-activity"></a><span data-ttu-id="e3279-103">Üretim akışı faaliyetine bir öncel ekleme</span><span class="sxs-lookup"><span data-stu-id="e3279-103">Add a predecessor to a production flow activity</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="e3279-104">Üretim akışı sürümünde, tüm faaliyetlerin sıralı olması gerekir.</span><span class="sxs-lookup"><span data-stu-id="e3279-104">In a production flow version, all activities must be sequenced.</span></span> <span data-ttu-id="e3279-105">Bir faaliyet bir veya daha fazla öncele ve ardıla sahip olabilir.</span><span class="sxs-lookup"><span data-stu-id="e3279-105">An activity can have one or multiple predecessors or successors.</span></span> 

<span data-ttu-id="e3279-106">Bu yordam bir önceli bir faaliyetle ilişkilendirmeyi gösterir.</span><span class="sxs-lookup"><span data-stu-id="e3279-106">This procedure shows how to associate a predecessor to an activity.</span></span> 

<span data-ttu-id="e3279-107">Bu görevi gerçekleştirmek için, birbirine bağlanabilen en az iki faaliyetin olduğu Taslak sürümüne sahip bir üretim akışına ihtiyacınız vardır.</span><span class="sxs-lookup"><span data-stu-id="e3279-107">To perform this task, you need a production flow that has the Draft version with at least two activities that can be connected.</span></span> 

<span data-ttu-id="e3279-108">Daha fazla bilgi için, "Üretim akışları ve yalın imalat faaliyetleri" başlıklı teknik raporu okuyun.</span><span class="sxs-lookup"><span data-stu-id="e3279-108">To learn more, read the white paper "Production flows and activities in lean manufacturing."</span></span>


## <a name="find-the-production-flow-and-version"></a><span data-ttu-id="e3279-109">Üretim akışını ve sürümünü bulma</span><span class="sxs-lookup"><span data-stu-id="e3279-109">Find the production flow and version</span></span>
1. <span data-ttu-id="e3279-110">Üretim kontrolü > Kurulum > Yalın üretim akışı > Üretim akışları seçeneğine gidin.</span><span class="sxs-lookup"><span data-stu-id="e3279-110">Go to Production control > Setup > Lean production flow > Production flows.</span></span>
2. <span data-ttu-id="e3279-111">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="e3279-111">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="e3279-112">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="e3279-112">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="e3279-113">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="e3279-113">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="e3279-114">Faaliyetler'i tıklatın.</span><span class="sxs-lookup"><span data-stu-id="e3279-114">Click Activities.</span></span>

## <a name="select-an-activity-and-add-a-predecessor"></a><span data-ttu-id="e3279-115">Faaliyet seçme ve öncel ekleme</span><span class="sxs-lookup"><span data-stu-id="e3279-115">Select an activity and add a predecessor</span></span>
1. <span data-ttu-id="e3279-116">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="e3279-116">In the list, find and select the desired record.</span></span>
2. <span data-ttu-id="e3279-117">Öncel ekle öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="e3279-117">Click Add predecessor.</span></span>
3. <span data-ttu-id="e3279-118">Faaliyet alanına bir değer girin veya buradan bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="e3279-118">In the Activity field, enter or select a value.</span></span>
4. <span data-ttu-id="e3279-119">Döngü süresi oranı alanında bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="e3279-119">In the Cycle time ratio field, enter a number.</span></span>
    * <span data-ttu-id="e3279-120">Bir faaliyet ilişkisinin varsayılan döngü süresi oranı 1'dir.</span><span class="sxs-lookup"><span data-stu-id="e3279-120">The default cycle time ratio of an activity relation is 1.</span></span> <span data-ttu-id="e3279-121">Bu her iki faaliyetin de aynı takt zamanında çalıştığını varsayar.</span><span class="sxs-lookup"><span data-stu-id="e3279-121">This assumes that both activities run at the same pace or takt time.</span></span> <span data-ttu-id="e3279-122">Öncel daha yüksek bir hızda çalışıyorsa (daha düşük takt süresi), bu oran 1'den düşük olmalıdır; öncel daha düşük bir hızda çalışıyorsa (daha yüksek takt süresi), döngü süresi oranı 1'den büyük olur.</span><span class="sxs-lookup"><span data-stu-id="e3279-122">If the predecessor runs at a higher pace (lower takt time), the ratio should be lower than 1, if the predecessor runs at a slower pace (higher takt time) the cycle time ratio is greater than 1.</span></span>  
5. <span data-ttu-id="e3279-123">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="e3279-123">Click OK.</span></span>

