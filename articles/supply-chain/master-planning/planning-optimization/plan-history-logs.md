---
title: Plan geçmişini ve planlama günlüklerini görüntüleme
description: Bu konu, Planlamayı En İyi Duruma Getirme işlevi tarafından tetiklenen planlama işlerinin geçmişini nasıl görüntüleyeceğinizi açıklar.
author: ChristianRytt
ms.date: 10/30/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: MPSPlanRegenerationJobList, MPSPlanRegenerationJobLogs
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: AX 10.0.5
ms.openlocfilehash: d7bba084b03f8698c8bf31d171d5e4e486ed06ad
ms.sourcegitcommit: a7649b361ec54b49c0e9ee1c1c63a8815f320225
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/04/2021
ms.locfileid: "6187259"
---
# <a name="view-plan-history-and-planning-logs"></a><span data-ttu-id="84474-103">Plan geçmişini ve planlama günlüklerini görüntüleme</span><span class="sxs-lookup"><span data-stu-id="84474-103">View plan history and planning logs</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="84474-104">Bu konu, Microsoft Dynamics 365 Supply Chain Management'ta Planlamayı En İyi Duruma Getirme işlevi tarafından tetiklenen planlama işlerinin geçmişini nasıl görüntüleyeceğinizi açıklar.</span><span class="sxs-lookup"><span data-stu-id="84474-104">This topic explains how to view the history of planning jobs that are triggered by the Planning Optimization functionality in Microsoft Dynamics 365 Supply Chain Management.</span></span>

<span data-ttu-id="84474-105">Planın geçmişini görüntülemek için **Master planlama** \> **Ayar** \> **Planlar** \> **Master planlar**'a gidip **Geçmiş**'i seçerek planı açın.</span><span class="sxs-lookup"><span data-stu-id="84474-105">To view the history for a plan, open the plan by going to **Master planning** \> **Setup** \> **Plans** \> **Master plans** and selecting **History**.</span></span> <span data-ttu-id="84474-106">Geçmiş, seçilen plan için tüm işleri listeler.</span><span class="sxs-lookup"><span data-stu-id="84474-106">The history lists all the jobs for the selected plan.</span></span> <span data-ttu-id="84474-107">Liste, tamamlanmış ve etkin işleri içerir.</span><span class="sxs-lookup"><span data-stu-id="84474-107">The list includes completed and active jobs.</span></span>

<span data-ttu-id="84474-108">Planlama Optimizasyonu master planlama çalıştırma işlerinin geçmişi, master plan başına yalnızca 60'a kadar kayıt saklar.</span><span class="sxs-lookup"><span data-stu-id="84474-108">The history of jobs for Planning Optimization master planning runs keeps only up to 60 records per master plan.</span></span> <span data-ttu-id="84474-109">Yeni bir master planlama hesaplaması çalıştırdığınızda, ilgili planın en eski geçmiş kaydı silinir.</span><span class="sxs-lookup"><span data-stu-id="84474-109">Whenever you run a new master planning calculation, that plan's earliest history record is deleted.</span></span>

<span data-ttu-id="84474-110">İşlerin başlama zamanını ve durumunu görmeye ek olarak, belirli bir iş için günlüğü de görüntüleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="84474-110">In addition to seeing the start time and status of jobs, you can view the log for a specific job.</span></span> <span data-ttu-id="84474-111">Günlük, ek bilgiler ve uyarılar içerir.</span><span class="sxs-lookup"><span data-stu-id="84474-111">The log includes additional information and warnings.</span></span> <span data-ttu-id="84474-112">Tüm işlerin günlüğü olmayabilir.</span><span class="sxs-lookup"><span data-stu-id="84474-112">Not all jobs have a log.</span></span> <span data-ttu-id="84474-113">İşin günlüğünü görüntülemek için **Günlük** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="84474-113">To view the log for a job, select **Log**.</span></span> <span data-ttu-id="84474-114">Günlük girişleri, iş tamamlandıktan sonra yalnızca 30 gün saklanır. Bu tarihten sonra otomatik olarak silinirler.</span><span class="sxs-lookup"><span data-stu-id="84474-114">Log entries are only stored for 30 days after the date the job finished, after that they are automatically deleted.</span></span>

## <a name="related-resources"></a><span data-ttu-id="84474-115">İlgili kaynaklar</span><span class="sxs-lookup"><span data-stu-id="84474-115">Related resources</span></span>

- [<span data-ttu-id="84474-116">Planlama Optimizasyonuna genel bakış</span><span class="sxs-lookup"><span data-stu-id="84474-116">Planning Optimization overview</span></span>](planning-optimization-overview.md)
- [<span data-ttu-id="84474-117">Planlama Optimizasyonunu kullanmaya başlama</span><span class="sxs-lookup"><span data-stu-id="84474-117">Get started with Planning Optimization</span></span>](get-started.md)
- [<span data-ttu-id="84474-118">Planlamayı En İyi Duruma Getirme uygunluk analizi</span><span class="sxs-lookup"><span data-stu-id="84474-118">Planning Optimization fit analysis</span></span>](planning-optimization-fit-analysis.md)
- [<span data-ttu-id="84474-119">Plana filtre uygulama</span><span class="sxs-lookup"><span data-stu-id="84474-119">Apply filters to a plan</span></span>](plan-filters.md)
- [<span data-ttu-id="84474-120">Planlama işini iptal etme</span><span class="sxs-lookup"><span data-stu-id="84474-120">Cancel a planning job</span></span>](cancel-planning-job.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]