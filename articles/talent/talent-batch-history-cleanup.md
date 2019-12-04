---
title: Otomatik temizleme görevleriyle performansı en iyi duruma getirme
description: Bu konu altında, toplu iş geçmişini temizleyerek Microsoft Dynamics 365 Talent ile ilgili bazı performans sorunlarının nasıl çözüleceğini açıklamaktadır.
author: andreabichsel
manager: AnnBe
ms.date: 09/23/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2019-09-23
ms.dyn365.ops.version: Platform update 24
ms.openlocfilehash: a053c9094151f4e12e4aadc533dd272258779540
ms.sourcegitcommit: 9cc6a011bfdd1b0fe505760b6bf429eb6c65862a
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/25/2019
ms.locfileid: "2832594"
---
# <a name="optimize-performance-with-auto-cleanup-tasks"></a><span data-ttu-id="7167e-103">Otomatik temizleme görevleriyle performansı en iyi duruma getirme</span><span class="sxs-lookup"><span data-stu-id="7167e-103">Optimize performance with auto cleanup tasks</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="7167e-104">**Çıkış**</span><span class="sxs-lookup"><span data-stu-id="7167e-104">**Issue**</span></span>

<span data-ttu-id="7167e-105">Toplu iş geçmişi çok fazla büyürse Microsoft Dynamics 365 Talent performans sorunlarıyla karşılaşabilir.</span><span class="sxs-lookup"><span data-stu-id="7167e-105">Microsoft Dynamics 365 Talent can experience performance issues if the batch job history grows too large.</span></span>

<span data-ttu-id="7167e-106">**Nedeni**</span><span class="sxs-lookup"><span data-stu-id="7167e-106">**Cause**</span></span>

<span data-ttu-id="7167e-107">Sık çalıştırılan toplu işler, toplu iş geçmişinin bozulmasına neden olabilecek büyümeye yol açabilir.</span><span class="sxs-lookup"><span data-stu-id="7167e-107">Batch jobs that run frequently can lead to unsustainable growth of the batch job history.</span></span> <span data-ttu-id="7167e-108">Bu durum performans sorunlarına neden olabilir.</span><span class="sxs-lookup"><span data-stu-id="7167e-108">This can cause performance issues.</span></span> 

<span data-ttu-id="7167e-109">**Çözünürlük**</span><span class="sxs-lookup"><span data-stu-id="7167e-109">**Resolution**</span></span>

<span data-ttu-id="7167e-110">Toplu iş geçmişinizi temizlemek için bir otomatik görev zamanlayın.</span><span class="sxs-lookup"><span data-stu-id="7167e-110">Schedule an automatic task to clean up your batch job history.</span></span> <span data-ttu-id="7167e-111">Görevi haftalık çalışacak şekilde ayarlamanız önerilir ancak çalışma ortamınıza bağlı olarak temizleme işlemini daha çok veya daha sık çalıştırmanız gerekebilir.</span><span class="sxs-lookup"><span data-stu-id="7167e-111">We recommend setting up the task to run weekly, but you might need to run the cleanup more or less frequently, depending on your environment.</span></span> <span data-ttu-id="7167e-112">Aşağıdaki yordamda önerdiğimiz ayarlar vardır ancak bunları gereksinimlerinize göre değiştirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="7167e-112">The following procedure contains our recommended settings, but you can change these according to your needs.</span></span>

1. <span data-ttu-id="7167e-113">Talent'ta **Sistem yönetimi**'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="7167e-113">In Talent, select **System administration**.</span></span>

2. <span data-ttu-id="7167e-114">**Arama** çubuğunda, **Toplu iş geçmişi temizleme**'yi girin.</span><span class="sxs-lookup"><span data-stu-id="7167e-114">In the **Search** bar, enter **Batch job history clean-up**.</span></span>

   ![Toplu iş geçmişi temizlemeyi arayın](media/talent-batch-history-cleanup-search-bar.png)

3. <span data-ttu-id="7167e-116">**Geçmiş sınırı (gün)** bölümüne **30** girin.</span><span class="sxs-lookup"><span data-stu-id="7167e-116">In **History limit (days)**, enter **30**.</span></span>

   ![Geçmiş sınırı ayarını 30 yapın](media/talent-batch-history-cleanup-history-limit.png)

4. <span data-ttu-id="7167e-118">**Arka planda çalıştır**'ı ve sonra **Tekrar**ı seçin.</span><span class="sxs-lookup"><span data-stu-id="7167e-118">Select **Run in the background** and then select **Recurrence**.</span></span>

   ![Yinelemeyi ayarlayın](media/talent-batch-history-cleanup-recurrence.png)

5. <span data-ttu-id="7167e-120">**Yineleme tanımla** altında, **Başlangıç tarihini** ve **Başlangıç saatini** mesai saatlerin dışında veya hafta sonu sırasında oluşacak şekilde ayarlayın ve **BİTİŞ TARİHİ YOK**'u seçin.</span><span class="sxs-lookup"><span data-stu-id="7167e-120">Under **Define recurrence**, set the **Start date** and **Start time** to occur during off-hours or the weekend, and then select **NO END DATE**.</span></span> 

   ![Yineleme başlangıç tarihini ve saatini tanımlayın](media/talent-batch-history-cleanup-define-recurrence.png)

6. <span data-ttu-id="7167e-122">**YİNELEME DÜZENİ** altında, **Günler**'i seçin ve **BELİRTİLEN ARALIKTAN SONRA TEKRARLA** ayarını **7** yapın.</span><span class="sxs-lookup"><span data-stu-id="7167e-122">Under **RECURRENCE PATTERN**, select **Days** and set **REPEAT AFTER SPECIFIED INTERVAL** to **7**.</span></span>

   ![Temizleme tekrarını haftalık yapın](media/talent-batch-history-cleanup-recurrence-pattern.png)

7. <span data-ttu-id="7167e-124">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="7167e-124">Select **OK**.</span></span>

8. <span data-ttu-id="7167e-125">**Arka planda çalıştır** altındaki diğer gerekli parametreleri değiştirin ve **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="7167e-125">Change any other parameters under **Run in the background** as necessary, and then select **OK**.</span></span>

