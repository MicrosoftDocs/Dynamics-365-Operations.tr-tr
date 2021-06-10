---
title: Otomatik temizleme görevleriyle performansı en iyi duruma getirme
description: Bu konu altında, toplu iş geçmişini temizleyerek Microsoft Dynamics 365 Human Resources ile ilgili bazı performans sorunlarının nasıl çözüleceğini açıklamaktadır.
author: andreabichsel
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Platform update 24
ms.openlocfilehash: 6a9e94e282aa8f101b42c1378ef21c6c1fe0477e
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/18/2021
ms.locfileid: "6053503"
---
# <a name="optimize-performance-with-auto-cleanup-tasks"></a><span data-ttu-id="d3921-103">Otomatik temizleme görevleriyle performansı en iyi duruma getirme</span><span class="sxs-lookup"><span data-stu-id="d3921-103">Optimize performance with auto cleanup tasks</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="d3921-104">**Çıkış**</span><span class="sxs-lookup"><span data-stu-id="d3921-104">**Issue**</span></span>

<span data-ttu-id="d3921-105">Toplu iş geçmişi çok fazla büyürse Microsoft Dynamics 365 Human Resources performans sorunlarıyla karşılaşabilir.</span><span class="sxs-lookup"><span data-stu-id="d3921-105">Microsoft Dynamics 365 Human Resources can experience performance issues if the batch job history grows too large.</span></span>

<span data-ttu-id="d3921-106">**Nedeni**</span><span class="sxs-lookup"><span data-stu-id="d3921-106">**Cause**</span></span>

<span data-ttu-id="d3921-107">Sık çalıştırılan toplu işler, toplu iş geçmişinin bozulmasına neden olabilecek büyümeye yol açabilir.</span><span class="sxs-lookup"><span data-stu-id="d3921-107">Batch jobs that run frequently can lead to unsustainable growth of the batch job history.</span></span> <span data-ttu-id="d3921-108">Bu durum performans sorunlarına neden olabilir.</span><span class="sxs-lookup"><span data-stu-id="d3921-108">This can cause performance issues.</span></span> 

<span data-ttu-id="d3921-109">**Çözünürlük**</span><span class="sxs-lookup"><span data-stu-id="d3921-109">**Resolution**</span></span>

<span data-ttu-id="d3921-110">Toplu iş geçmişinizi temizlemek için bir otomatik görev zamanlayın.</span><span class="sxs-lookup"><span data-stu-id="d3921-110">Schedule an automatic task to clean up your batch job history.</span></span> <span data-ttu-id="d3921-111">Görevi haftalık çalışacak şekilde ayarlamanız önerilir ancak çalışma ortamınıza bağlı olarak temizleme işlemini daha çok veya daha sık çalıştırmanız gerekebilir.</span><span class="sxs-lookup"><span data-stu-id="d3921-111">We recommend setting up the task to run weekly, but you might need to run the cleanup more or less frequently, depending on your environment.</span></span> <span data-ttu-id="d3921-112">Aşağıdaki yordamda önerdiğimiz ayarlar vardır ancak bunları gereksinimlerinize göre değiştirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="d3921-112">The following procedure contains our recommended settings, but you can change these according to your needs.</span></span>

1. <span data-ttu-id="d3921-113">İnsan Kaynakları, **sistem yönetimi**'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="d3921-113">In Human Resources, select **System administration**.</span></span>

2. <span data-ttu-id="d3921-114">**Arama** çubuğunda, **Toplu iş geçmişi temizleme**'yi girin.</span><span class="sxs-lookup"><span data-stu-id="d3921-114">In the **Search** bar, enter **Batch job history clean-up**.</span></span>

   ![Toplu iş geçmişi temizlemeyi arayın](media/talent-batch-history-cleanup-search-bar.png)

3. <span data-ttu-id="d3921-116">**Geçmiş sınırı (gün)** bölümüne **30** girin.</span><span class="sxs-lookup"><span data-stu-id="d3921-116">In **History limit (days)**, enter **30**.</span></span>

   ![Geçmiş sınırı ayarını 30 yapın](media/talent-batch-history-cleanup-history-limit.png)

4. <span data-ttu-id="d3921-118">**Arka planda çalıştır**'ı ve sonra **Tekrar** ı seçin.</span><span class="sxs-lookup"><span data-stu-id="d3921-118">Select **Run in the background** and then select **Recurrence**.</span></span>

   ![Yinelemeyi ayarlayın](media/talent-batch-history-cleanup-recurrence.png)

5. <span data-ttu-id="d3921-120">**Yineleme tanımla** altında, **Başlangıç tarihini** ve **Başlangıç saatini** mesai saatlerin dışında veya hafta sonu sırasında oluşacak şekilde ayarlayın ve **BİTİŞ TARİHİ YOK**'u seçin.</span><span class="sxs-lookup"><span data-stu-id="d3921-120">Under **Define recurrence**, set the **Start date** and **Start time** to occur during off-hours or the weekend, and then select **NO END DATE**.</span></span> 

   ![Yineleme başlangıç tarihini ve saatini tanımlayın](media/talent-batch-history-cleanup-define-recurrence.png)

6. <span data-ttu-id="d3921-122">**YİNELEME DÜZENİ** altında, **Günler**'i seçin ve **BELİRTİLEN ARALIKTAN SONRA TEKRARLA** ayarını **7** yapın.</span><span class="sxs-lookup"><span data-stu-id="d3921-122">Under **RECURRENCE PATTERN**, select **Days** and set **REPEAT AFTER SPECIFIED INTERVAL** to **7**.</span></span>

   ![Temizleme tekrarını haftalık yapın](media/talent-batch-history-cleanup-recurrence-pattern.png)

7. <span data-ttu-id="d3921-124">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="d3921-124">Select **OK**.</span></span>

8. <span data-ttu-id="d3921-125">**Arka planda çalıştır** altındaki diğer gerekli parametreleri değiştirin ve **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="d3921-125">Change any other parameters under **Run in the background** as necessary, and then select **OK**.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]