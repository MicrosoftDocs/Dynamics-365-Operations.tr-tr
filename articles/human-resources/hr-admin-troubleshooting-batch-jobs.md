---
title: Toplu işleri, saatler sonra çizelgelemek için performansı en iyi duruma getirme
description: Bu konu altında, saatler sonra uzun süre çalışan toplu işler planlayarak Microsoft Dynamics 365 Human Resources ile ilgili bazı performans sorunlarının nasıl çözüleceğini açıklamaktadır.
author: andreabichsel
manager: tfehr
ms.date: 06/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-06-23
ms.dyn365.ops.version: Platform update 24
ms.openlocfilehash: 219537aab2015469b6ca6ebed5c00af0190c5187
ms.sourcegitcommit: ea2d652867b9b83ce6e5e8d6a97d2f9460a84c52
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/03/2021
ms.locfileid: "5114624"
---
# <a name="optimize-performance-by-scheduling-batch-jobs-after-hours"></a><span data-ttu-id="6421a-103">Toplu işleri, saatler sonra çizelgelemek için performansı en iyi duruma getirme</span><span class="sxs-lookup"><span data-stu-id="6421a-103">Optimize performance by scheduling batch jobs after hours</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

## <a name="issue"></a><span data-ttu-id="6421a-104">Çıkış</span><span class="sxs-lookup"><span data-stu-id="6421a-104">Issue</span></span>

<span data-ttu-id="6421a-105">Microsoft Dynamics 365 Human Resources, uzun süren toplu işler tipik iş saatlerinde çalışıyorsa, performans sorunlarıyla karşılaşabilir.</span><span class="sxs-lookup"><span data-stu-id="6421a-105">Microsoft Dynamics 365 Human Resources can experience performance issues if long-running batch jobs run during typical business hours.</span></span>

## <a name="resolution"></a><span data-ttu-id="6421a-106">Çözünürlük</span><span class="sxs-lookup"><span data-stu-id="6421a-106">Resolution</span></span>

<span data-ttu-id="6421a-107">Aşağıdaki toplu işleri kapalı saatlerde zamanlar.</span><span class="sxs-lookup"><span data-stu-id="6421a-107">Schedule the following batch jobs during off hours.</span></span> <span data-ttu-id="6421a-108">Ayrıca, sık çalışan toplu işlerin sıklığını gözden geçirmeyi öneririz.</span><span class="sxs-lookup"><span data-stu-id="6421a-108">We also recommend reviewing the frequency of batch jobs that run frequently.</span></span> <span data-ttu-id="6421a-109">Mümkünse, toplu işin tekrarlanma şeklini azaltın.</span><span class="sxs-lookup"><span data-stu-id="6421a-109">If possible, reduce the recurrence of the batch job.</span></span> <span data-ttu-id="6421a-110">Birçok durumda, varsayılan sıklık yeterlidir.</span><span class="sxs-lookup"><span data-stu-id="6421a-110">In many cases, the default frequency is sufficient.</span></span>

<span data-ttu-id="6421a-111">Aşağıdaki toplu işler gece veya saat tarihinden sonra çalışmalıdır.</span><span class="sxs-lookup"><span data-stu-id="6421a-111">The following batch jobs should run at night or after hours.</span></span> <span data-ttu-id="6421a-112">Bu yinelenen toplu işlerin saat dilimini kontrol edin.</span><span class="sxs-lookup"><span data-stu-id="6421a-112">Be sure to check the time zone for these recurring batch jobs.</span></span> <span data-ttu-id="6421a-113">Bazı toplu işler Pasifik Standart Saati (PST) kullanabilir.</span><span class="sxs-lookup"><span data-stu-id="6421a-113">Some batch jobs might use Pacific Standard Time (PST).</span></span>

| <span data-ttu-id="6421a-114">Toplu iş</span><span class="sxs-lookup"><span data-stu-id="6421a-114">Batch job</span></span> | <span data-ttu-id="6421a-115">Varsayılan oluşum</span><span class="sxs-lookup"><span data-stu-id="6421a-115">Default occurrence</span></span> |
| --- | --- |
| <span data-ttu-id="6421a-116">Toplu iş geçmişi temizleme</span><span class="sxs-lookup"><span data-stu-id="6421a-116">Batch job history cleanup</span></span> | <span data-ttu-id="6421a-117">Ayda 1 saat</span><span class="sxs-lookup"><span data-stu-id="6421a-117">1 time per month</span></span> |
| <span data-ttu-id="6421a-118">Dışa aktarma hazırlığını temizleme</span><span class="sxs-lookup"><span data-stu-id="6421a-118">Export staging cleanup</span></span> | <span data-ttu-id="6421a-119">Günde 1 saat</span><span class="sxs-lookup"><span data-stu-id="6421a-119">1 time per day</span></span> |
| <span data-ttu-id="6421a-120">Common Data Service tümleştirmesi, istek eşitlemesini atladı</span><span class="sxs-lookup"><span data-stu-id="6421a-120">Common Data Service integration missed request sync</span></span> | <span data-ttu-id="6421a-121">Günde 1 saat</span><span class="sxs-lookup"><span data-stu-id="6421a-121">1 time per day</span></span> |
| <span data-ttu-id="6421a-122">Saatler dışında düzenli olarak çalıştırılması gereken veritabanı sıkıştırma sistemi işi</span><span class="sxs-lookup"><span data-stu-id="6421a-122">Database compression system job that needs to run regularly during off hours</span></span> | <span data-ttu-id="6421a-123">Günde 1 saat</span><span class="sxs-lookup"><span data-stu-id="6421a-123">1 time per day</span></span> |
| <span data-ttu-id="6421a-124">Saatler dışında düzenli olarak çalıştırılması gereken veritabanı dizin yeniden oluşturma sistem işi</span><span class="sxs-lookup"><span data-stu-id="6421a-124">Database index rebuild system job that needs to run regularly during off hours</span></span> | <span data-ttu-id="6421a-125">Günde 1 saat</span><span class="sxs-lookup"><span data-stu-id="6421a-125">1 time per day</span></span> |

1. <span data-ttu-id="6421a-126">İnsan Kaynakları, **sistem yönetimi**'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="6421a-126">In Human Resources, select **System administration**.</span></span>

2. <span data-ttu-id="6421a-127">**Arama** çubuğunda, yukarıdaki toplu işlerden birini arayın.</span><span class="sxs-lookup"><span data-stu-id="6421a-127">In the **Search** bar, search for one of the above batch jobs.</span></span>

3. <span data-ttu-id="6421a-128">**Arka planda çalıştır**'ı ve sonra **Tekrar** ı seçin.</span><span class="sxs-lookup"><span data-stu-id="6421a-128">Select **Run in the background**, and then select **Recurrence**.</span></span>

   ![Yinelemeyi ayarlayın](media/talent-batch-history-cleanup-recurrence.png)

4. <span data-ttu-id="6421a-130">**Yineleme tanımla** altında, **Başlangıç tarihi** ve **Başlangıç saatini** mesai saatlerin dışında veya hafta sonu sırasında oluşacak şekilde ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="6421a-130">Under **Define recurrence**, set the **Start date** and **Start time** to occur during off hours or the weekend.</span></span> <span data-ttu-id="6421a-131">**Bitiş tarihi yok**'u seçin.</span><span class="sxs-lookup"><span data-stu-id="6421a-131">Select **No end date**.</span></span> 

   ![Yineleme başlangıç tarihini ve saatini tanımlayın](media/talent-batch-history-cleanup-define-recurrence.png)

5. <span data-ttu-id="6421a-133">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="6421a-133">Select **OK**.</span></span>

6. <span data-ttu-id="6421a-134">Gerekirse **Arka planda çalıştır** altındaki diğer parametreleri değiştirin ve **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="6421a-134">If needed, change any other parameters under **Run in the background**, and then select **OK**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="6421a-135">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="6421a-135">Additional resources</span></span>

[<span data-ttu-id="6421a-136">Otomatik temizleme görevleriyle performansı en iyi duruma getirme</span><span class="sxs-lookup"><span data-stu-id="6421a-136">Optimize performance with auto cleanup tasks</span></span>](hr-admin-troubleshooting-batch-history.md)
