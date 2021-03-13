---
title: Planlama işini iptal etme
description: Bu konuda, Planlamayı en iyi duruma getirme işlevini kullanan etkin bir planlama işinin nasıl iptal edileceği açıklanmaktadır.
author: ChristianRytt
manager: tfehr
ms.date: 02/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
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
ms.openlocfilehash: 7cee11e6d9e8bc2fe83f5369554ae9ff9ee2b741
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/15/2021
ms.locfileid: "5008228"
---
# <a name="cancel-a-planning-job"></a><span data-ttu-id="8097d-103">Planlama işini iptal etme</span><span class="sxs-lookup"><span data-stu-id="8097d-103">Cancel a planning job</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="8097d-104">Microsoft Dynamics 365 Supply Chain Management'ta, Planlamayı en iyi duruma getirme işlevini kullanan etkin bir planlama işini iptal edebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="8097d-104">In Microsoft Dynamics 365 Supply Chain Management, you can cancel an active planning job that uses the Planning optimization functionality.</span></span> <span data-ttu-id="8097d-105">Bir Planlama en iyi duruma getirme işi doğrudan kullanıcı arabiriminden tetiklendiğinde (arka planda değil), iletişim kutusunda **İptal**'i seçerseniz bu işlem Planlama en iyi duruma getirme işini iptal etmez.</span><span class="sxs-lookup"><span data-stu-id="8097d-105">When you select **Cancel** in the dialog box when a Planning optimization job is triggered directly from the user interface (not in the background), this will not cancel the Planning optimization job.</span></span> <span data-ttu-id="8097d-106">"İşlem iptal edildi" gibi bir uyarı alsanız bile Planlama en iyi duruma getirme işlemi ile planlama işini iptal etmek için yine de aşağıdaki adımları kullanmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="8097d-106">Even if you receive a warning such as “Operation canceled”, you will still need to use the following steps to cancel a planning job with Planning optimization.</span></span>


<span data-ttu-id="8097d-107">Etkin bir planlama işini iptal etmek için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="8097d-107">To cancel an active planning job, follow these steps.</span></span> 

> [!NOTE]
> <span data-ttu-id="8097d-108">Yalnızca etkin işler iptal edilebilir.</span><span class="sxs-lookup"><span data-stu-id="8097d-108">Only active jobs can be canceled.</span></span>

1. <span data-ttu-id="8097d-109">**Master planlama \> Ayar \> Planlar**'a gidin.</span><span class="sxs-lookup"><span data-stu-id="8097d-109">Go to **Master planning \> Setup \> Plans**.</span></span>
2. <span data-ttu-id="8097d-110">Planlama çalışması için uygun bir plan seçin.</span><span class="sxs-lookup"><span data-stu-id="8097d-110">Select an appropriate plan for the planning run.</span></span>
3. <span data-ttu-id="8097d-111">**Geçmiş**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="8097d-111">Select **History**.</span></span>
4. <span data-ttu-id="8097d-112">İptal edilecek planlama işini seçin.</span><span class="sxs-lookup"><span data-stu-id="8097d-112">Select the planning job to cancel.</span></span>
5. <span data-ttu-id="8097d-113">**İptal**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="8097d-113">Select **Cancel**.</span></span>

<span data-ttu-id="8097d-114">Planlamayı En İyi Duruma Getirme hizmeti işin iptal edilmesini onaylayana kadar iş durumu **İptal ediliyor** olur.</span><span class="sxs-lookup"><span data-stu-id="8097d-114">The job status will be **Canceling** until the Planning Optimization service confirms that the job has been canceled.</span></span> <span data-ttu-id="8097d-115">Ardından durum **İptal Edildi** olarak değiştirilir.</span><span class="sxs-lookup"><span data-stu-id="8097d-115">The status will then be changed to **Canceled**.</span></span>

> [!NOTE]
> <span data-ttu-id="8097d-116">Durum değişikliklerini görmek için **Yenile** düğmesini seçerek sayfayı yenilemeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="8097d-116">To see status changes, you must refresh the page by selecting the **Refresh** button.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="8097d-117">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="8097d-117">Additional resources</span></span>

[<span data-ttu-id="8097d-118">Planlamayı En İyi Duruma Getirmeye genel bakış</span><span class="sxs-lookup"><span data-stu-id="8097d-118">Planning Optimization overview</span></span>](planning-optimization-overview.md)

[<span data-ttu-id="8097d-119">Planlamayı En İyi Duruma Getirmeyi kullanmaya başlama</span><span class="sxs-lookup"><span data-stu-id="8097d-119">Get started with Planning Optimization</span></span>](get-started.md)

[<span data-ttu-id="8097d-120">Planlamayı En İyi Duruma Getirme uygunluk analizi</span><span class="sxs-lookup"><span data-stu-id="8097d-120">Planning Optimization fit analysis</span></span>](planning-optimization-fit-analysis.md)

[<span data-ttu-id="8097d-121">Plan geçmişini ve planlama günlüklerini görüntüleme</span><span class="sxs-lookup"><span data-stu-id="8097d-121">View plan history and planning logs</span></span>](plan-history-logs.md)

[<span data-ttu-id="8097d-122">Plana filtre uygulama</span><span class="sxs-lookup"><span data-stu-id="8097d-122">Apply filters to a plan</span></span>](plan-filters.md)
