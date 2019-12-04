---
title: Plana filtre uygulama
description: Bu konuda, Planlamayı En İyi Duruma Getirme işlevi kullanıldığında bir planda filtrelerin nasıl kullanılacağı açıklanmaktadır.
author: ChristianRytt
manager: AnnBe
ms.date: 10/30/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: AX 10.0.5
ms.openlocfilehash: ff9c9f875368fcc4dd62b9c188d489e20a5c7960
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/06/2019
ms.locfileid: "2774071"
---
[!include [banner](../../includes/preview-banner.md)]
[!include [banner](../../includes/banner.md)]

# <a name="apply-filters-to-a-plan"></a><span data-ttu-id="f8d9f-103">Plana filtre uygulama</span><span class="sxs-lookup"><span data-stu-id="f8d9f-103">Apply filters to a plan</span></span>

<span data-ttu-id="f8d9f-104">Planlamayı En İyi Duruma Getirme işlevi kullanıldığında plana bir filtre uygulayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="f8d9f-104">When the Planning Optimization functionality is used, you can apply a filter to a plan.</span></span> <span data-ttu-id="f8d9f-105">Plan filtresi, her zaman master planlama çalışması sırasında uygulanır.</span><span class="sxs-lookup"><span data-stu-id="f8d9f-105">The plan filter will always be applied during a master planning run.</span></span> <span data-ttu-id="f8d9f-106">Plan filtresi, bir planı belirli bir madde grubuyla sınırlamak ve ortaya çıkan master planlamanın bir parçası olarak başka hiçbir maddenin dahil edilmediğinden emin olmak istediğinizde yararlıdır.</span><span class="sxs-lookup"><span data-stu-id="f8d9f-106">A plan filter is useful when you want to limit a plan to a specific group of items and make sure that no other items are included as part of the resulting master planning.</span></span>

<span data-ttu-id="f8d9f-107">Plan filtresi uygulanırsa ve master planlama çalışması sırasında bir çalışma zamanı filtresi de uygulanırsa planlama çalışmasına yalnızca iki filtrenin kesişimi dahil edilir.</span><span class="sxs-lookup"><span data-stu-id="f8d9f-107">If a plan filter is applied, and a runtime filter is also applied during the master planning run, only the intersection of the two filters is included in the planning run.</span></span>

## <a name="example-scenario"></a><span data-ttu-id="f8d9f-108">Örnek senaryo</span><span class="sxs-lookup"><span data-stu-id="f8d9f-108">Example scenario</span></span>

<span data-ttu-id="f8d9f-109">A, B ve C maddelerini içeren bir plan filtresi ayarlanır. Ardından master planlama çalışmaları aynı plan için çalıştırılır ancak farklı çalışma zamanı filtreleri uygulanır:</span><span class="sxs-lookup"><span data-stu-id="f8d9f-109">A plan filter is set up that includes items A, B, and C. Master planning runs are then run for the same plan, but different runtime filters are applied:</span></span>

- <span data-ttu-id="f8d9f-110">**D maddesini içeren çalışma zamanı filtresi:** Plan filtresi ile çalışma zamanı filtresi kesişmediğinden hiçbir madde planlanmaz.</span><span class="sxs-lookup"><span data-stu-id="f8d9f-110">**Runtime filter that includes item D:** No items are planned, because there is no intersection between the plan filter and the runtime filter.</span></span>
- <span data-ttu-id="f8d9f-111">**A ve D maddelerini içeren çalışma zamanı filtresi:** D maddesi plan filtresinin parçası olmadığından yalnızca A maddesi planlama çalışmasına dahil edilir.</span><span class="sxs-lookup"><span data-stu-id="f8d9f-111">**Runtime filter that includes item A and D:** Only item A is included in the planning run, because item D isn't part of the plan filter.</span></span>
- <span data-ttu-id="f8d9f-112">**B maddesini içeren çalışma zamanı filtresi:** Yalnızca B maddesi planlama çalışmasına dahil edilir ve A maddesinin önceki planlama çıktısı tutulur.</span><span class="sxs-lookup"><span data-stu-id="f8d9f-112">**Runtime filter that includes item B:** Only item B is included in the planning run, and the previous planning output for item A is kept.</span></span>
- <span data-ttu-id="f8d9f-113">**Tüm maddeleri içeren çalışma zamanı filtresi (boş filtre):** A, B ve C maddeleri planlama çalışmasına dahil edilir ve A ve B maddelerinin önceki planlama çıktısı üzerine yazılır.</span><span class="sxs-lookup"><span data-stu-id="f8d9f-113">**Runtime filter that includes all items (blank filter):** Items A, B, and C are included in the planning run, and the previous planning output for items A and B is overwritten.</span></span>

> [!NOTE]
> <span data-ttu-id="f8d9f-114">**Master planlama parametreleri** sayfasında **Geçerli dinamik master plan** olarak seçilen planda bir plan filtresi ayarlamaktan kaçınmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="f8d9f-114">You should avoid setting a plan filter on the plan that is selected as **Current dynamic master plan** on the **Master planning parameters** page.</span></span> <span data-ttu-id="f8d9f-115">Aksi takdirde, dinamik master plan işlevleri filtrelenen maddelerle sınırlandırılır.</span><span class="sxs-lookup"><span data-stu-id="f8d9f-115">Otherwise, the dynamic master plan functionality will be limited to the filtered items.</span></span> <span data-ttu-id="f8d9f-116">Örneğin, net gereksinimler, plan filtresinin parçası olmayan bir madde için güncelleştirilirse hiçbir sonuç oluşturulmaz.</span><span class="sxs-lookup"><span data-stu-id="f8d9f-116">For example, if the net requirements are updated for an item that isn't part of the plan filter, no result will be generated.</span></span>

## <a name="related-resources"></a><span data-ttu-id="f8d9f-117">İlgili kaynaklar</span><span class="sxs-lookup"><span data-stu-id="f8d9f-117">Related resources</span></span>

[<span data-ttu-id="f8d9f-118">Planlamayı En İyi Duruma Getirmeye genel bakış</span><span class="sxs-lookup"><span data-stu-id="f8d9f-118">Planning Optimization overview</span></span>](planning-optimization-overview.md)

[<span data-ttu-id="f8d9f-119">Planlamayı En İyi Duruma Getirmeye başlayın</span><span class="sxs-lookup"><span data-stu-id="f8d9f-119">Get started with Planning Optimization</span></span>](get-started.md)

[<span data-ttu-id="f8d9f-120">Planlamayı En İyi Duruma Getirme uygunluk analizi</span><span class="sxs-lookup"><span data-stu-id="f8d9f-120">Planning Optimization fit analysis</span></span>](planning-optimization-fit-analysis.md)

[<span data-ttu-id="f8d9f-121">Plan geçmişini ve planlama günlüklerini görüntüleme</span><span class="sxs-lookup"><span data-stu-id="f8d9f-121">View plan history and planning logs</span></span>](plan-history-logs.md)

[<span data-ttu-id="f8d9f-122">Planlama işini iptal etme</span><span class="sxs-lookup"><span data-stu-id="f8d9f-122">Cancel a planning job</span></span>](cancel-planning-job.md)
