--- 
title: "Üretim akışı faaliyetine bir öncel ekleme"
description: "Üretim akışı sürümünde, tüm faaliyetlerin sıralı olması gerekir."
author: cvocph
manager: AnnBe
ms.date: 10/26/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: conradv
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: d19fb20e8cc941daeaa506e4bf1cb0c7031cf2ee
ms.contentlocale: tr-tr
ms.lasthandoff: 09/29/2017

---
# <a name="add-a-predecessor-to-a-production-flow-activity"></a><span data-ttu-id="b8770-103">Üretim akışı faaliyetine bir öncel ekleme</span><span class="sxs-lookup"><span data-stu-id="b8770-103">Add a predecessor to a production flow activity</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="b8770-104">Üretim akışı sürümünde, tüm faaliyetlerin sıralı olması gerekir.</span><span class="sxs-lookup"><span data-stu-id="b8770-104">In a production flow version, all activities must be sequenced.</span></span> <span data-ttu-id="b8770-105">Bir faaliyet bir veya daha fazla öncele ve ardıla sahip olabilir.</span><span class="sxs-lookup"><span data-stu-id="b8770-105">An activity can have one or multiple predecessors or successors.</span></span> 

<span data-ttu-id="b8770-106">Bu yordam bir önceli bir faaliyetle ilişkilendirmeyi gösterir.</span><span class="sxs-lookup"><span data-stu-id="b8770-106">This procedure shows how to associate a predecessor to an activity.</span></span> 

<span data-ttu-id="b8770-107">Bu görevi gerçekleştirmek için, birbirine bağlanabilen en az iki faaliyetin olduğu Taslak sürümüne sahip bir üretim akışına ihtiyacınız vardır.</span><span class="sxs-lookup"><span data-stu-id="b8770-107">To perform this task, you need a production flow that has the Draft version with at least two activities that can be connected.</span></span> 

<span data-ttu-id="b8770-108">Daha fazla bilgi için, "Üretim akışları ve yalın imalat faaliyetleri" başlıklı teknik raporu okuyun.</span><span class="sxs-lookup"><span data-stu-id="b8770-108">To learn more, read the white paper "Production flows and activities in lean manufacturing."</span></span>


## <a name="find-the-production-flow-and-version"></a><span data-ttu-id="b8770-109">Üretim akışını ve sürümünü bulma</span><span class="sxs-lookup"><span data-stu-id="b8770-109">Find the production flow and version</span></span>
1. <span data-ttu-id="b8770-110">Üretim kontrolü > Kurulum > Yalın üretim akışı > Üretim akışları seçeneğine gidin.</span><span class="sxs-lookup"><span data-stu-id="b8770-110">Go to Production control > Setup > Lean production flow > Production flows.</span></span>
2. <span data-ttu-id="b8770-111">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="b8770-111">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="b8770-112">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="b8770-112">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="b8770-113">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="b8770-113">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="b8770-114">Faaliyetler'i tıklatın.</span><span class="sxs-lookup"><span data-stu-id="b8770-114">Click Activities.</span></span>

## <a name="select-an-activity-and-add-a-predecessor"></a><span data-ttu-id="b8770-115">Faaliyet seçme ve öncel ekleme</span><span class="sxs-lookup"><span data-stu-id="b8770-115">Select an activity and add a predecessor</span></span>
1. <span data-ttu-id="b8770-116">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="b8770-116">In the list, find and select the desired record.</span></span>
2. <span data-ttu-id="b8770-117">Öncel ekle öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="b8770-117">Click Add predecessor.</span></span>
3. <span data-ttu-id="b8770-118">Faaliyet alanına bir değer girin veya buradan bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="b8770-118">In the Activity field, enter or select a value.</span></span>
4. <span data-ttu-id="b8770-119">Döngü süresi oranı alanında bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="b8770-119">In the Cycle time ratio field, enter a number.</span></span>
    * <span data-ttu-id="b8770-120">Bir faaliyet ilişkisinin varsayılan döngü süresi oranı 1'dir.</span><span class="sxs-lookup"><span data-stu-id="b8770-120">The default cycle time ratio of an activity relation is 1.</span></span> <span data-ttu-id="b8770-121">Bu her iki faaliyetin de aynı takt zamanında çalıştığını varsayar.</span><span class="sxs-lookup"><span data-stu-id="b8770-121">This assumes that both activities run at the same pace or takt time.</span></span> <span data-ttu-id="b8770-122">Öncel daha yüksek bir hızda çalışıyorsa (daha düşük takt süresi), bu oran 1'den düşük olmalıdır; öncel daha düşük bir hızda çalışıyorsa (daha yüksek takt süresi), döngü süresi oranı 1'den büyük olur.</span><span class="sxs-lookup"><span data-stu-id="b8770-122">If the predecessor runs at a higher pace (lower takt time), the ratio should be lower than 1, if the predecessor runs at a slower pace (higher takt time) the cycle time ratio is greater than 1.</span></span>  
5. <span data-ttu-id="b8770-123">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="b8770-123">Click OK.</span></span>

