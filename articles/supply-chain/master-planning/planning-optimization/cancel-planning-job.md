---
title: Planlama işini iptal etme
description: Bu konuda, Planlamayı en iyi duruma getirme işlevini kullanan etkin bir planlama işinin nasıl iptal edileceği açıklanmaktadır.
author: ChristianRytt
ms.date: 02/18/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: AX 10.0.5
ms.openlocfilehash: e9cf4902251c3c2b93af12a8ad9bd571930ef769
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/01/2021
ms.locfileid: "5833341"
---
# <a name="cancel-a-planning-job"></a><span data-ttu-id="0d041-103">Planlama işini iptal etme</span><span class="sxs-lookup"><span data-stu-id="0d041-103">Cancel a planning job</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="0d041-104">Microsoft Dynamics 365 Supply Chain Management'ta, Planlamayı en iyi duruma getirme işlevini kullanan etkin bir planlama işini iptal edebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="0d041-104">In Microsoft Dynamics 365 Supply Chain Management, you can cancel an active planning job that uses the Planning optimization functionality.</span></span> <span data-ttu-id="0d041-105">Bir Planlama en iyi duruma getirme işi doğrudan kullanıcı arabiriminden tetiklendiğinde (arka planda değil), iletişim kutusunda **İptal**'i seçerseniz bu işlem Planlama en iyi duruma getirme işini iptal etmez.</span><span class="sxs-lookup"><span data-stu-id="0d041-105">When you select **Cancel** in the dialog box when a Planning optimization job is triggered directly from the user interface (not in the background), this will not cancel the Planning optimization job.</span></span> <span data-ttu-id="0d041-106">"İşlem iptal edildi" gibi bir uyarı alsanız bile Planlama en iyi duruma getirme işlemi ile planlama işini iptal etmek için yine de aşağıdaki adımları kullanmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="0d041-106">Even if you receive a warning such as “Operation canceled”, you will still need to use the following steps to cancel a planning job with Planning optimization.</span></span>


<span data-ttu-id="0d041-107">Etkin bir planlama işini iptal etmek için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="0d041-107">To cancel an active planning job, follow these steps.</span></span> 

> [!NOTE]
> <span data-ttu-id="0d041-108">Yalnızca etkin işler iptal edilebilir.</span><span class="sxs-lookup"><span data-stu-id="0d041-108">Only active jobs can be canceled.</span></span>

1. <span data-ttu-id="0d041-109">**Master planlama \> Ayar \> Planlar**'a gidin.</span><span class="sxs-lookup"><span data-stu-id="0d041-109">Go to **Master planning \> Setup \> Plans**.</span></span>
2. <span data-ttu-id="0d041-110">Planlama çalışması için uygun bir plan seçin.</span><span class="sxs-lookup"><span data-stu-id="0d041-110">Select an appropriate plan for the planning run.</span></span>
3. <span data-ttu-id="0d041-111">**Geçmiş**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="0d041-111">Select **History**.</span></span>
4. <span data-ttu-id="0d041-112">İptal edilecek planlama işini seçin.</span><span class="sxs-lookup"><span data-stu-id="0d041-112">Select the planning job to cancel.</span></span>
5. <span data-ttu-id="0d041-113">**İptal**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="0d041-113">Select **Cancel**.</span></span>

<span data-ttu-id="0d041-114">Planlamayı En İyi Duruma Getirme hizmeti işin iptal edilmesini onaylayana kadar iş durumu **İptal ediliyor** olur.</span><span class="sxs-lookup"><span data-stu-id="0d041-114">The job status will be **Canceling** until the Planning Optimization service confirms that the job has been canceled.</span></span> <span data-ttu-id="0d041-115">Ardından durum **İptal Edildi** olarak değiştirilir.</span><span class="sxs-lookup"><span data-stu-id="0d041-115">The status will then be changed to **Canceled**.</span></span>

> [!NOTE]
> <span data-ttu-id="0d041-116">Durum değişikliklerini görmek için **Yenile** düğmesini seçerek sayfayı yenilemeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="0d041-116">To see status changes, you must refresh the page by selecting the **Refresh** button.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="0d041-117">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="0d041-117">Additional resources</span></span>

[<span data-ttu-id="0d041-118">Planlamayı En İyi Duruma Getirmeye genel bakış</span><span class="sxs-lookup"><span data-stu-id="0d041-118">Planning Optimization overview</span></span>](planning-optimization-overview.md)

[<span data-ttu-id="0d041-119">Planlamayı En İyi Duruma Getirmeyi kullanmaya başlama</span><span class="sxs-lookup"><span data-stu-id="0d041-119">Get started with Planning Optimization</span></span>](get-started.md)

[<span data-ttu-id="0d041-120">Planlamayı En İyi Duruma Getirme uygunluk analizi</span><span class="sxs-lookup"><span data-stu-id="0d041-120">Planning Optimization fit analysis</span></span>](planning-optimization-fit-analysis.md)

[<span data-ttu-id="0d041-121">Plan geçmişini ve planlama günlüklerini görüntüleme</span><span class="sxs-lookup"><span data-stu-id="0d041-121">View plan history and planning logs</span></span>](plan-history-logs.md)

[<span data-ttu-id="0d041-122">Plana filtre uygulama</span><span class="sxs-lookup"><span data-stu-id="0d041-122">Apply filters to a plan</span></span>](plan-filters.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]