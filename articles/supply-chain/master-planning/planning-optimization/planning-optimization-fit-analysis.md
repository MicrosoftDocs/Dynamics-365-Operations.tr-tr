---
title: Planlamayı En İyi Duruma Getirme uygunluk analizi
description: Bu konuda, geçerli ayar ve verilerinizi Planlamayı En İyi Duruma Getirme işlevinin özelliklerine göre nasıl doğrulayacağınız açıklanmaktadır.
author: ChristianRytt
manager: AnnBe
ms.date: 1030/2019
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
ms.openlocfilehash: 26b067f8526df16474c0ab52d0abf816170ff5cb
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/06/2019
ms.locfileid: "2774070"
---
[!include [banner](../../includes/preview-banner.md)]
[!include [banner](../../includes/banner.md)]

# <a name="planning-optimization-fit-analysis"></a><span data-ttu-id="0f038-103">Planlamayı En İyi Duruma Getirme uygunluk analizi</span><span class="sxs-lookup"><span data-stu-id="0f038-103">Planning Optimization fit analysis</span></span>

<span data-ttu-id="0f038-104">Geçerli ayar ve verilerinizin Planlamayı En İyi Duruma Getirme işleviyle nasıl uyumlu olduğunu görmek için **Master planlama** \> **Ayar** \> **Planlamayı En İyi Duruma Getirme uygunluk analizi** bölümüne gidin ve ardından **Analizi çalıştır**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="0f038-104">To see how compatible your current setup and data are with the Planning Optimization functionality, go to **Master planning** \> **Setup** \> **Planning Optimization fit analysis**, and then select **Run analysis**.</span></span> <span data-ttu-id="0f038-105">Analizde tutarsızlıklar bulunursa bunlar aynı sayfada listelenir.</span><span class="sxs-lookup"><span data-stu-id="0f038-105">If the analysis finds any inconsistencies, they are listed on the same page.</span></span> <span data-ttu-id="0f038-106">(Analizin çalıştırılması birkaç dakika sürebilir.)</span><span class="sxs-lookup"><span data-stu-id="0f038-106">(The analysis can take a few minutes to run.)</span></span>

> [!NOTE]
> <span data-ttu-id="0f038-107">Tutarsızlıklar varsa yine de Planlamayı En İyi Duruma Getirmeye özelliğini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="0f038-107">If inconsistencies are found, you can still use Planning Optimization.</span></span> <span data-ttu-id="0f038-108">Uygunluk analizinin sonuçları yalnızca planlama servisinin geçerli ayarınızı dikkate almadığı yerleri gösterir.</span><span class="sxs-lookup"><span data-stu-id="0f038-108">The results of the fit analysis just show places where the planning service won't honor your current setup.</span></span> <span data-ttu-id="0f038-109">Başka bir deyişle, bazı işlemlerin yok sayılabileceği veya desteklenmeyebileceği yerleri gösterir.</span><span class="sxs-lookup"><span data-stu-id="0f038-109">In other words, they show places where some processes might be ignored or might not be supported.</span></span>

## <a name="analysis-results-example-1"></a><span data-ttu-id="0f038-110">Analiz sonuçları: Örnek 1</span><span class="sxs-lookup"><span data-stu-id="0f038-110">Analysis results: Example 1</span></span>

- <span data-ttu-id="0f038-111">**Özellik:** Üretim</span><span class="sxs-lookup"><span data-stu-id="0f038-111">**Feature:** Production</span></span>
- <span data-ttu-id="0f038-112">**Sorun:** Ürün reçetesi düzeyi sıfırdan büyük olan maddeler: 56</span><span class="sxs-lookup"><span data-stu-id="0f038-112">**Issue:** Items with BOM level greater than zero: 56</span></span>
- <span data-ttu-id="0f038-113">**Açıklama:** Uygunluk analizi üretim için ürün reçetesi (BOM) ayarı olan 56 madde buldu.</span><span class="sxs-lookup"><span data-stu-id="0f038-113">**Explanation:** The fit analysis found 56 items that have a bill of materials (BOM) setup for production.</span></span> <span data-ttu-id="0f038-114">Planlamayı En İyi Duruma Getirme özelliğinin geçerli sürümü üretimi desteklemediğinden Planlamayı En İyi Duruma Getirme, planlı üretim emirleri yerine planlı satın alma emirleri oluşturur.</span><span class="sxs-lookup"><span data-stu-id="0f038-114">Because the current version of Planning Optimization doesn't support production, Planning Optimization will generate planned purchase orders instead of planned production orders.</span></span> <span data-ttu-id="0f038-115">Ayrıca etkilenen maddelerin listelendiği bir uyarı da gösterir.</span><span class="sxs-lookup"><span data-stu-id="0f038-115">It will also show a warning that lists the affected items.</span></span>

### <a name="analysis-results-example-2"></a><span data-ttu-id="0f038-116">Analiz sonuçları: Örnek 2</span><span class="sxs-lookup"><span data-stu-id="0f038-116">Analysis results: Example 2</span></span>

- <span data-ttu-id="0f038-117">**Özellik:** Eylemler</span><span class="sxs-lookup"><span data-stu-id="0f038-117">**Feature:** Actions</span></span>
- <span data-ttu-id="0f038-118">**Sorun:** Eylem hesaplaması etkinleştirilen karşılama grupları: 6</span><span class="sxs-lookup"><span data-stu-id="0f038-118">**Issue:** Coverage groups with actions calculation enabled: 6</span></span>
- <span data-ttu-id="0f038-119">**Açıklama:** Uygunluk analizi, eylem hesaplamasının açık olduğu altı karşılama grubu buldu.</span><span class="sxs-lookup"><span data-stu-id="0f038-119">**Explanation:** The fit analysis found six coverage groups where action calculation is turned on.</span></span> <span data-ttu-id="0f038-120">Planlamayı En İyi Duruma Getirme özelliğinin geçerli sürümü eylemleri desteklemediğinden eylemler master planlama sırasında oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="0f038-120">Because the current version of Planning Optimization doesn't support actions, no actions will be generated during master planning.</span></span>

## <a name="related-resources"></a><span data-ttu-id="0f038-121">İlgili kaynaklar</span><span class="sxs-lookup"><span data-stu-id="0f038-121">Related resources</span></span>

[<span data-ttu-id="0f038-122">Planlamayı En İyi Duruma Getirmeye genel bakış</span><span class="sxs-lookup"><span data-stu-id="0f038-122">Planning Optimization overview</span></span>](planning-optimization-overview.md)

[<span data-ttu-id="0f038-123">Planlamayı En İyi Duruma Getirmeye başlayın</span><span class="sxs-lookup"><span data-stu-id="0f038-123">Get started with Planning Optimization</span></span>](get-started.md)

[<span data-ttu-id="0f038-124">Plan geçmişini ve planlama günlüklerini görüntüleme</span><span class="sxs-lookup"><span data-stu-id="0f038-124">View plan history and planning logs</span></span>](plan-history-logs.md)

[<span data-ttu-id="0f038-125">Plana filtre uygulama</span><span class="sxs-lookup"><span data-stu-id="0f038-125">Apply filters to a plan</span></span>](plan-filters.md)

[<span data-ttu-id="0f038-126">Planlama işini iptal etme</span><span class="sxs-lookup"><span data-stu-id="0f038-126">Cancel a planning job</span></span>](cancel-planning-job.md)