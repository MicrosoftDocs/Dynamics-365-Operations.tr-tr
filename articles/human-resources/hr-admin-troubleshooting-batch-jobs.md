---
title: Toplu işleri, saatler sonra çizelgelemek için performansı en iyi duruma getirme
description: Bu konu altında, saatler sonra uzun süre çalışan toplu işler planlayarak Microsoft Dynamics 365 Human Resources ile ilgili bazı performans sorunlarının nasıl çözüleceğini açıklamaktadır.
author: andreabichsel
ms.date: 06/23/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-06-23
ms.dyn365.ops.version: Platform update 24
ms.openlocfilehash: a5aeaeb7311d87a154882b7058b6da430900bd56
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/18/2021
ms.locfileid: "6053479"
---
# <a name="optimize-performance-by-scheduling-batch-jobs-after-hours"></a><span data-ttu-id="466cb-103">Toplu işleri, saatler sonra çizelgelemek için performansı en iyi duruma getirme</span><span class="sxs-lookup"><span data-stu-id="466cb-103">Optimize performance by scheduling batch jobs after hours</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

## <a name="issue"></a><span data-ttu-id="466cb-104">Çıkış</span><span class="sxs-lookup"><span data-stu-id="466cb-104">Issue</span></span>

<span data-ttu-id="466cb-105">Microsoft Dynamics 365 Human Resources, uzun süren toplu işler tipik iş saatlerinde çalışıyorsa, performans sorunlarıyla karşılaşabilir.</span><span class="sxs-lookup"><span data-stu-id="466cb-105">Microsoft Dynamics 365 Human Resources can experience performance issues if long-running batch jobs run during typical business hours.</span></span>

## <a name="resolution"></a><span data-ttu-id="466cb-106">Çözünürlük</span><span class="sxs-lookup"><span data-stu-id="466cb-106">Resolution</span></span>

<span data-ttu-id="466cb-107">Aşağıdaki toplu işleri kapalı saatlerde zamanlar.</span><span class="sxs-lookup"><span data-stu-id="466cb-107">Schedule the following batch jobs during off hours.</span></span> <span data-ttu-id="466cb-108">Ayrıca, sık çalışan toplu işlerin sıklığını gözden geçirmeyi öneririz.</span><span class="sxs-lookup"><span data-stu-id="466cb-108">We also recommend reviewing the frequency of batch jobs that run frequently.</span></span> <span data-ttu-id="466cb-109">Mümkünse, toplu işin tekrarlanma şeklini azaltın.</span><span class="sxs-lookup"><span data-stu-id="466cb-109">If possible, reduce the recurrence of the batch job.</span></span> <span data-ttu-id="466cb-110">Birçok durumda, varsayılan sıklık yeterlidir.</span><span class="sxs-lookup"><span data-stu-id="466cb-110">In many cases, the default frequency is sufficient.</span></span>

<span data-ttu-id="466cb-111">Aşağıdaki toplu işler gece veya saat tarihinden sonra çalışmalıdır.</span><span class="sxs-lookup"><span data-stu-id="466cb-111">The following batch jobs should run at night or after hours.</span></span> <span data-ttu-id="466cb-112">Bu yinelenen toplu işlerin saat dilimini kontrol edin.</span><span class="sxs-lookup"><span data-stu-id="466cb-112">Be sure to check the time zone for these recurring batch jobs.</span></span> <span data-ttu-id="466cb-113">Bazı toplu işler Pasifik Standart Saati (PST) kullanabilir.</span><span class="sxs-lookup"><span data-stu-id="466cb-113">Some batch jobs might use Pacific Standard Time (PST).</span></span>

| <span data-ttu-id="466cb-114">Toplu iş</span><span class="sxs-lookup"><span data-stu-id="466cb-114">Batch job</span></span> | <span data-ttu-id="466cb-115">Varsayılan oluşum</span><span class="sxs-lookup"><span data-stu-id="466cb-115">Default occurrence</span></span> |
| --- | --- |
| <span data-ttu-id="466cb-116">Toplu iş geçmişi temizleme</span><span class="sxs-lookup"><span data-stu-id="466cb-116">Batch job history cleanup</span></span> | <span data-ttu-id="466cb-117">Ayda 1 saat</span><span class="sxs-lookup"><span data-stu-id="466cb-117">1 time per month</span></span> |
| <span data-ttu-id="466cb-118">Dışa aktarma hazırlığını temizleme</span><span class="sxs-lookup"><span data-stu-id="466cb-118">Export staging cleanup</span></span> | <span data-ttu-id="466cb-119">Günde 1 saat</span><span class="sxs-lookup"><span data-stu-id="466cb-119">1 time per day</span></span> |
| <span data-ttu-id="466cb-120">Common Data Service tümleştirmesi, istek eşitlemesini atladı</span><span class="sxs-lookup"><span data-stu-id="466cb-120">Common Data Service integration missed request sync</span></span> | <span data-ttu-id="466cb-121">Günde 1 saat</span><span class="sxs-lookup"><span data-stu-id="466cb-121">1 time per day</span></span> |
| <span data-ttu-id="466cb-122">Saatler dışında düzenli olarak çalıştırılması gereken veritabanı sıkıştırma sistemi işi</span><span class="sxs-lookup"><span data-stu-id="466cb-122">Database compression system job that needs to run regularly during off hours</span></span> | <span data-ttu-id="466cb-123">Günde 1 saat</span><span class="sxs-lookup"><span data-stu-id="466cb-123">1 time per day</span></span> |
| <span data-ttu-id="466cb-124">Saatler dışında düzenli olarak çalıştırılması gereken veritabanı dizin yeniden oluşturma sistem işi</span><span class="sxs-lookup"><span data-stu-id="466cb-124">Database index rebuild system job that needs to run regularly during off hours</span></span> | <span data-ttu-id="466cb-125">Günde 1 saat</span><span class="sxs-lookup"><span data-stu-id="466cb-125">1 time per day</span></span> |

1. <span data-ttu-id="466cb-126">İnsan Kaynakları, **sistem yönetimi**'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="466cb-126">In Human Resources, select **System administration**.</span></span>

2. <span data-ttu-id="466cb-127">**Arama** çubuğunda, yukarıdaki toplu işlerden birini arayın.</span><span class="sxs-lookup"><span data-stu-id="466cb-127">In the **Search** bar, search for one of the above batch jobs.</span></span>

3. <span data-ttu-id="466cb-128">**Arka planda çalıştır**'ı ve sonra **Tekrar** ı seçin.</span><span class="sxs-lookup"><span data-stu-id="466cb-128">Select **Run in the background**, and then select **Recurrence**.</span></span>

   ![Yinelemeyi ayarlayın](media/talent-batch-history-cleanup-recurrence.png)

4. <span data-ttu-id="466cb-130">**Yineleme tanımla** altında, **Başlangıç tarihi** ve **Başlangıç saatini** mesai saatlerin dışında veya hafta sonu sırasında oluşacak şekilde ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="466cb-130">Under **Define recurrence**, set the **Start date** and **Start time** to occur during off hours or the weekend.</span></span> <span data-ttu-id="466cb-131">**Bitiş tarihi yok**'u seçin.</span><span class="sxs-lookup"><span data-stu-id="466cb-131">Select **No end date**.</span></span> 

   ![Yineleme başlangıç tarihini ve saatini tanımlayın](media/talent-batch-history-cleanup-define-recurrence.png)

5. <span data-ttu-id="466cb-133">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="466cb-133">Select **OK**.</span></span>

6. <span data-ttu-id="466cb-134">Gerekirse **Arka planda çalıştır** altındaki diğer parametreleri değiştirin ve **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="466cb-134">If needed, change any other parameters under **Run in the background**, and then select **OK**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="466cb-135">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="466cb-135">Additional resources</span></span>

[<span data-ttu-id="466cb-136">Otomatik temizleme görevleriyle performansı en iyi duruma getirme</span><span class="sxs-lookup"><span data-stu-id="466cb-136">Optimize performance with auto cleanup tasks</span></span>](hr-admin-troubleshooting-batch-history.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]