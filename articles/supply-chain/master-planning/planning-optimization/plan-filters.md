---
title: Plana filtre uygulama
description: Bu konuda, Planlamayı En İyi Duruma Getirme işlevi kullanıldığında bir planda filtrelerin nasıl kullanılacağı açıklanmaktadır.
author: ChristianRytt
manager: tfehr
ms.date: 01/08/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: AX 10.0.5
ms.openlocfilehash: 73e4a045ff5a9912b898a7115d3d8f530846ebdd
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/02/2020
ms.locfileid: "3209801"
---
# <a name="apply-filters-to-a-plan"></a><span data-ttu-id="16dec-103">Plana filtre uygulama</span><span class="sxs-lookup"><span data-stu-id="16dec-103">Apply filters to a plan</span></span>

[!include [banner](../../includes/preview-banner.md)]
[!include [banner](../../includes/banner.md)]

<span data-ttu-id="16dec-104">Planlamayı En İyi Duruma Getirme işlevi kullanıldığında plana bir filtre uygulayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="16dec-104">When the Planning Optimization functionality is used, you can apply a filter to a plan.</span></span> <span data-ttu-id="16dec-105">**Plan filtresi**, her zaman master planlama çalışması sırasında uygulanır.</span><span class="sxs-lookup"><span data-stu-id="16dec-105">The **Plan filter** will always be applied during a master planning run.</span></span> <span data-ttu-id="16dec-106">**Plan filtresi**, bir planı belirli bir madde grubuyla sınırlamak ve ortaya çıkan master planlamanın bir parçası olarak başka hiçbir maddenin dahil edilmediğinden emin olmak istediğinizde yararlıdır.</span><span class="sxs-lookup"><span data-stu-id="16dec-106">A **Plan filter** is useful when you want to limit a plan to a specific group of items and make sure that no other items are included as part of the resulting master planning.</span></span>

<span data-ttu-id="16dec-107">**Plan filtresi** uygulanırsa ve master planlama çalışması sırasında bir çalışma zamanı filtresi de uygulanırsa planlama çalışmasına yalnızca iki filtrenin kesişimi dahil edilir.</span><span class="sxs-lookup"><span data-stu-id="16dec-107">If a **Plan filter** is applied, and a runtime filter is also applied during the master planning run, only the intersection of the two filters is included in the planning run.</span></span>

<span data-ttu-id="16dec-108">**Plan filtresi**, en iyi duruma getirme işlemi kullanılırken **ana planlardan** erişilebilir.</span><span class="sxs-lookup"><span data-stu-id="16dec-108">The **Plan filter** can be accessed from **Master plans** when Planning Optimization is used.</span></span>

## <a name="example-scenario"></a><span data-ttu-id="16dec-109">Örnek senaryo</span><span class="sxs-lookup"><span data-stu-id="16dec-109">Example scenario</span></span>

<span data-ttu-id="16dec-110">A, B ve C maddelerini içeren bir plan filtresi ayarlanır. Ardından master planlama çalışmaları aynı plan için çalıştırılır ancak farklı çalışma zamanı filtreleri uygulanır:</span><span class="sxs-lookup"><span data-stu-id="16dec-110">A plan filter is set up that includes items A, B, and C. Master planning runs are then run for the same plan, but different runtime filters are applied:</span></span>

- <span data-ttu-id="16dec-111">**D maddesini içeren çalışma zamanı filtresi:** Plan filtresi ile çalışma zamanı filtresi kesişmediğinden hiçbir madde planlanmaz.</span><span class="sxs-lookup"><span data-stu-id="16dec-111">**Runtime filter that includes item D:** No items are planned, because there is no intersection between the plan filter and the runtime filter.</span></span>
- <span data-ttu-id="16dec-112">**A ve D maddelerini içeren çalışma zamanı filtresi:** D maddesi plan filtresinin parçası olmadığından yalnızca A maddesi planlama çalışmasına dahil edilir.</span><span class="sxs-lookup"><span data-stu-id="16dec-112">**Runtime filter that includes item A and D:** Only item A is included in the planning run, because item D isn't part of the plan filter.</span></span>
- <span data-ttu-id="16dec-113">**B maddesini içeren çalışma zamanı filtresi:** Yalnızca B maddesi planlama çalışmasına dahil edilir ve A maddesinin önceki planlama çıktısı tutulur.</span><span class="sxs-lookup"><span data-stu-id="16dec-113">**Runtime filter that includes item B:** Only item B is included in the planning run, and the previous planning output for item A is kept.</span></span>
- <span data-ttu-id="16dec-114">**Tüm maddeleri içeren çalışma zamanı filtresi (boş filtre):** A, B ve C maddeleri planlama çalışmasına dahil edilir ve A ve B maddelerinin önceki planlama çıktısı üzerine yazılır.</span><span class="sxs-lookup"><span data-stu-id="16dec-114">**Runtime filter that includes all items (blank filter):** Items A, B, and C are included in the planning run, and the previous planning output for items A and B is overwritten.</span></span>

> [!NOTE]
> <span data-ttu-id="16dec-115">**Master planlama parametreleri** sayfasında **Geçerli dinamik master plan** olarak seçilen planda bir plan filtresi ayarlamaktan kaçınmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="16dec-115">You should avoid setting a plan filter on the plan that is selected as **Current dynamic master plan** on the **Master planning parameters** page.</span></span> <span data-ttu-id="16dec-116">Aksi takdirde, dinamik master plan işlevleri filtrelenen maddelerle sınırlandırılır.</span><span class="sxs-lookup"><span data-stu-id="16dec-116">Otherwise, the dynamic master plan functionality will be limited to the filtered items.</span></span> <span data-ttu-id="16dec-117">Örneğin, net gereksinimler, plan filtresinin parçası olmayan bir madde için güncelleştirilirse hiçbir sonuç oluşturulmaz.</span><span class="sxs-lookup"><span data-stu-id="16dec-117">For example, if the net requirements are updated for an item that isn't part of the plan filter, no result will be generated.</span></span>

## <a name="related-resources"></a><span data-ttu-id="16dec-118">İlgili kaynaklar</span><span class="sxs-lookup"><span data-stu-id="16dec-118">Related resources</span></span>

[<span data-ttu-id="16dec-119">Planlamayı En İyi Duruma Getirmeye genel bakış</span><span class="sxs-lookup"><span data-stu-id="16dec-119">Planning Optimization overview</span></span>](planning-optimization-overview.md)

[<span data-ttu-id="16dec-120">Planlamayı En İyi Duruma Getirmeye başlayın</span><span class="sxs-lookup"><span data-stu-id="16dec-120">Get started with Planning Optimization</span></span>](get-started.md)

[<span data-ttu-id="16dec-121">Planlamayı En İyi Duruma Getirme uygunluk analizi</span><span class="sxs-lookup"><span data-stu-id="16dec-121">Planning Optimization fit analysis</span></span>](planning-optimization-fit-analysis.md)

[<span data-ttu-id="16dec-122">Plan geçmişini ve planlama günlüklerini görüntüleme</span><span class="sxs-lookup"><span data-stu-id="16dec-122">View plan history and planning logs</span></span>](plan-history-logs.md)

[<span data-ttu-id="16dec-123">Planlama işini iptal etme</span><span class="sxs-lookup"><span data-stu-id="16dec-123">Cancel a planning job</span></span>](cancel-planning-job.md)
