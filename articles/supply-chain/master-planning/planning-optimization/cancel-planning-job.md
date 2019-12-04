---
title: Planlama işini iptal etme
description: Bu konuda, Planlamayı En İyi Duruma Getirme işlevini kullanan etkin bir planlama işinin nasıl iptal edileceği açıklanmaktadır.
author: ChristianRytt
manager: AnnBe
ms.date: 10/26/2019
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
ms.openlocfilehash: a2d90f04985fdd66ca83582ee676100fffb26981
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/06/2019
ms.locfileid: "2774072"
---
[!include [banner](../../includes/banner.md)]
[!include [banner](../../includes/preview-banner.md)]

# <a name="cancel-a-planning-job"></a><span data-ttu-id="5cde3-103">Planlama işini iptal etme</span><span class="sxs-lookup"><span data-stu-id="5cde3-103">Cancel a planning job</span></span>

<span data-ttu-id="5cde3-104">Microsoft Dynamics 365 Supply Chain Management'ta, Planlamayı En İyi Duruma Getirme işlevini kullanan etkin bir planlama işini iptal edebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="5cde3-104">In Microsoft Dynamics 365 Supply Chain Management, you can cancel an active planning job that uses the Planning Optimization functionality.</span></span>

<span data-ttu-id="5cde3-105">Etkin bir planlama işini iptal etmek için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="5cde3-105">To cancel an active planning job, follow these steps.</span></span>

> [!NOTE]
> <span data-ttu-id="5cde3-106">Yalnızca etkin işler iptal edilebilir.</span><span class="sxs-lookup"><span data-stu-id="5cde3-106">Only active jobs can be canceled.</span></span>

1. <span data-ttu-id="5cde3-107">**Master planlama \> Ayar \> Planlar**'a gidin.</span><span class="sxs-lookup"><span data-stu-id="5cde3-107">Go to **Master planning \> Setup \> Plans**.</span></span>
2. <span data-ttu-id="5cde3-108">Planlama çalışması için uygun bir plan seçin.</span><span class="sxs-lookup"><span data-stu-id="5cde3-108">Select an appropriate plan for the planning run.</span></span>
3. <span data-ttu-id="5cde3-109">**Geçmiş**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="5cde3-109">Select **History**.</span></span>
4. <span data-ttu-id="5cde3-110">İptal edilecek planlama işini seçin.</span><span class="sxs-lookup"><span data-stu-id="5cde3-110">Select the planning job to cancel.</span></span>
5. <span data-ttu-id="5cde3-111">**İptal**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="5cde3-111">Select **Cancel**.</span></span>

<span data-ttu-id="5cde3-112">Planlamayı En İyi Duruma Getirme hizmeti işin iptal edilmesini onaylayana kadar iş durumu **İptal ediliyor** olur.</span><span class="sxs-lookup"><span data-stu-id="5cde3-112">The job status will be **Canceling** until the Planning Optimization service confirms that the job has been canceled.</span></span> <span data-ttu-id="5cde3-113">Ardından durum **İptal Edildi** olarak değiştirilir.</span><span class="sxs-lookup"><span data-stu-id="5cde3-113">The status will then be changed to **Canceled**.</span></span>

> [!NOTE]
> <span data-ttu-id="5cde3-114">Durum değişikliklerini görmek için **Yenile** düğmesini seçerek sayfayı yenilemeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="5cde3-114">To see status changes, you must refresh the page by selecting the **Refresh** button.</span></span>

## <a name="related-resources"></a><span data-ttu-id="5cde3-115">İlgili kaynaklar</span><span class="sxs-lookup"><span data-stu-id="5cde3-115">Related resources</span></span>

[<span data-ttu-id="5cde3-116">Planlamayı En İyi Duruma Getirmeye genel bakış</span><span class="sxs-lookup"><span data-stu-id="5cde3-116">Planning Optimization overview</span></span>](planning-optimization-overview.md)

[<span data-ttu-id="5cde3-117">Planlamayı En İyi Duruma Getirmeye başlayın</span><span class="sxs-lookup"><span data-stu-id="5cde3-117">Get started with Planning Optimization</span></span>](get-started.md)

[<span data-ttu-id="5cde3-118">Planlamayı En İyi Duruma Getirme uygunluk analizi</span><span class="sxs-lookup"><span data-stu-id="5cde3-118">Planning Optimization fit analysis</span></span>](planning-optimization-fit-analysis.md)

[<span data-ttu-id="5cde3-119">Plan geçmişini ve planlama günlüklerini görüntüleme</span><span class="sxs-lookup"><span data-stu-id="5cde3-119">View plan history and planning logs</span></span>](plan-history-logs.md)

[<span data-ttu-id="5cde3-120">Plana filtre uygulama</span><span class="sxs-lookup"><span data-stu-id="5cde3-120">Apply filters to a plan</span></span>](plan-filters.md)
