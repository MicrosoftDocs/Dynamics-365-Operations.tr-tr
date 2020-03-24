---
title: Attract'te analitik raporları kullanma
description: Bu konuda, Microsoft Dynamics 365 Talent- Attract'ta işe alım süreci öngörülerine yönelik analitik raporları açıklanmaktadır
author: fewatson
manager: AnnBe
ms.date: 04/30/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: fewatson
ms.search.validFrom: 2019-04-30
ms.dyn365.ops.version: Talent April 2019 update
ms.openlocfilehash: 081988e8b8cfe1e2ddb533247b678ba38a07f5f1
ms.sourcegitcommit: f38302b9430f2ab3efe91d0a7beff946bc610e8f
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/28/2020
ms.locfileid: "3092235"
---
# <a name="use-analytic-reports-in-attract"></a><span data-ttu-id="889c6-103">Attract'te analitik raporları kullanma</span><span class="sxs-lookup"><span data-stu-id="889c6-103">Use analytic reports in Attract</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="889c6-104">Microsoft Dynamics 365 Talent: Attract'teki analitik raporlar, işe alım işlemi öngörüleriniz için kullanıma hazır (OOTB) bir çözüm sağlar.</span><span class="sxs-lookup"><span data-stu-id="889c6-104">Analytic reports in Microsoft Dynamics 365 Talent: Attract provide an out-of-the-box (OOTB) solution for hiring process insights.</span></span> <span data-ttu-id="889c6-105">Kullanılabilir özellikler şunları içerir:</span><span class="sxs-lookup"><span data-stu-id="889c6-105">Availabe features include:</span></span>

- <span data-ttu-id="889c6-106">**İş analizleri** İşe başvuranların ölçümleri için işin içinde **Analiz** sekmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="889c6-106">**Job analytics:** Click the **Analytics** tab within a job for metrics on the job's applicants.</span></span>
- <span data-ttu-id="889c6-107">**Analitik Hub:** İşlerdeki toplu ölçümler için sol gezinme panosunda **Analiz**'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="889c6-107">**Analytics hub:** Click **Analytics** on the left navigation for aggregated metrics across jobs.</span></span>
- <span data-ttu-id="889c6-108">**Kullanıcıya özel güvenlik:** –  Raporlara erişim Attract [rolü](security-attract.md) ve iş katılımcısı rolü tarafından denetlenir.</span><span class="sxs-lookup"><span data-stu-id="889c6-108">**User-specific security:** Access to reports is controlled by Attract [role](security-attract.md) and job participant role.</span></span>
- <span data-ttu-id="889c6-109">**Çapraz filtreleme:** Seçilen veriye göre filtrelenen diğer ölçümleri görmek için rapor içindeki görsellere tıklayın.</span><span class="sxs-lookup"><span data-stu-id="889c6-109">**Cross-filtering:** Click visuals within a report to view other metrics filtered by selected data.</span></span>

>[!NOTE] 
>- <span data-ttu-id="889c6-110">Bu özellik şu anda [önizlemededir](access-preview-feature.md).</span><span class="sxs-lookup"><span data-stu-id="889c6-110">This feature is currently in [preview](access-preview-feature.md).</span></span> <span data-ttu-id="889c6-111">Denemek için, [**Kapsamlı Aşe Alım Eklentisine**](attract-comprehensive-hiring.md) sahip olmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="889c6-111">To try it, you must have the [**Comprehensive Hiring Add-On**](attract-comprehensive-hiring.md).</span></span>
>- <span data-ttu-id="889c6-112">Genel kullanıma sunulan tüm önizleme raporları İngilizce olarak görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="889c6-112">All public preview reports are displayed in English.</span></span>
>- <span data-ttu-id="889c6-113">Raporlar 3 saatte bir yenilenir.</span><span class="sxs-lookup"><span data-stu-id="889c6-113">Reports refresh every 3 hours.</span></span> <span data-ttu-id="889c6-114">Son yenileme zamanı (yerel saat diliminde) raporun en üstünde bulunur.</span><span class="sxs-lookup"><span data-stu-id="889c6-114">The last refresh time (in the local timezone) is located at the top of the report.</span></span> <span data-ttu-id="889c6-115">Yenileme saatleri yaklaşık değerlerdir ve bölgenizdeki veri hacmine ve kaynak yüküne göre değişir.</span><span class="sxs-lookup"><span data-stu-id="889c6-115">Refresh times are an approximation and vary based on data volume and resource load in your region.</span></span>

## <a name="job-analytics"></a><span data-ttu-id="889c6-116">İş Analizi</span><span class="sxs-lookup"><span data-stu-id="889c6-116">Job Analytics</span></span>

<span data-ttu-id="889c6-117">İş Analitiği raporları, iş için işe alım sürecinin anlık görüntüleridir.</span><span class="sxs-lookup"><span data-stu-id="889c6-117">Job Analytics reports are a snapshot of the hiring process for a job.</span></span>  <span data-ttu-id="889c6-118">Temel ölçümler şunları içerir:</span><span class="sxs-lookup"><span data-stu-id="889c6-118">Key metrics include:</span></span>

- <span data-ttu-id="889c6-119">Aşamaya göre etkin başvuranlar</span><span class="sxs-lookup"><span data-stu-id="889c6-119">Active applicants by stage</span></span>
- <span data-ttu-id="889c6-120">Başvuran kaynağı</span><span class="sxs-lookup"><span data-stu-id="889c6-120">Applicant source</span></span>
- <span data-ttu-id="889c6-121">Başvuran türü (dahili veya harici)</span><span class="sxs-lookup"><span data-stu-id="889c6-121">Applicant type (internal or external)</span></span>

## <a name="analytics-hub"></a><span data-ttu-id="889c6-122">Analiz Merkezi</span><span class="sxs-lookup"><span data-stu-id="889c6-122">Analytics Hub</span></span>

<span data-ttu-id="889c6-123">Analiz Merkezi raporları, işe alma sürecindeki eğilimleri ortaya çıkarmak için işlerden veri toplar.</span><span class="sxs-lookup"><span data-stu-id="889c6-123">Analytics Hub reports aggregate data across jobs to surface trends in the hiring process.</span></span> <span data-ttu-id="889c6-124">Attract'te iki OOTB rapor bulunur: İşlem Hattı Özeti ve Huni Analizi.</span><span class="sxs-lookup"><span data-stu-id="889c6-124">Attract includes two OOTB reports: Pipeline Summary and Funnel Analysis.</span></span>

### <a name="pipeline-summary"></a><span data-ttu-id="889c6-125">Potansiyel Satış Özeti</span><span class="sxs-lookup"><span data-stu-id="889c6-125">Pipeline Summary</span></span>

<span data-ttu-id="889c6-126">İşlem Hattı Özeti raporu açık işlerle ilgili verileri toplar.</span><span class="sxs-lookup"><span data-stu-id="889c6-126">The Pipeline Summary report aggregates data for open jobs.</span></span> <span data-ttu-id="889c6-127">Temel ölçümler şunları içerir:</span><span class="sxs-lookup"><span data-stu-id="889c6-127">Key metrics include:</span></span>

- <span data-ttu-id="889c6-128">Aşamaya göre tüm işlerdeki başvuranlar</span><span class="sxs-lookup"><span data-stu-id="889c6-128">Applicants across all jobs by stage</span></span>
- <span data-ttu-id="889c6-129">Başvuran kaynağı</span><span class="sxs-lookup"><span data-stu-id="889c6-129">Applicant source</span></span>
- <span data-ttu-id="889c6-130">Kıdem düzeyine göre açık işler</span><span class="sxs-lookup"><span data-stu-id="889c6-130">Open jobs by seniority level</span></span>

### <a name="funnel-analysis"></a><span data-ttu-id="889c6-131">Huni Analizi</span><span class="sxs-lookup"><span data-stu-id="889c6-131">Funnel Analysis</span></span>

<span data-ttu-id="889c6-132">Huni Analizi raporu, dolduruldu olarak kapatılan işler için veri toplar.</span><span class="sxs-lookup"><span data-stu-id="889c6-132">The Funnel Analysis report aggregates data for jobs that have been closed as filled.</span></span> <span data-ttu-id="889c6-133">Temel ölçümler şunları içerir:</span><span class="sxs-lookup"><span data-stu-id="889c6-133">Key metrics include:</span></span>

- <span data-ttu-id="889c6-134">İşe alım zamanı</span><span class="sxs-lookup"><span data-stu-id="889c6-134">Time to hire</span></span>
- <span data-ttu-id="889c6-135">Dönüştürme ölçümleri (üzerine gidildiğinde)</span><span class="sxs-lookup"><span data-stu-id="889c6-135">Conversion metrics (on hover)</span></span>
- <span data-ttu-id="889c6-136">Teklif kabul oranı</span><span class="sxs-lookup"><span data-stu-id="889c6-136">Offer acceptance rate</span></span>

<span data-ttu-id="889c6-137">Not: İşe alım raporlamasında en doğru zaman için Kapsamlı İşe Alım Eklentisinin bir parçası olarak sunulan [Teklif yönetimini](offer-setup.md) kullanmanız önerilir.</span><span class="sxs-lookup"><span data-stu-id="889c6-137">Note: For the most accurate time to hire reporting, it is recommended that you use [Offer management](offer-setup.md), a feature available as part of the Comprehensive Hiring Add-On.</span></span>

>[!TIP] 
><span data-ttu-id="889c6-138">Ek bilgi için görsellerin üzerine gelmeyi deneyin.</span><span class="sxs-lookup"><span data-stu-id="889c6-138">Try hovering over visuals for additional information.</span></span> <span data-ttu-id="889c6-139">Örneğin, **Etkin başvuranlar**'ın üzerine geldiğinizde görseller aşamadaki ortalama gün sayısını gösterir.</span><span class="sxs-lookup"><span data-stu-id="889c6-139">For example, hovering over **Active applicants** visuals will display the average days in stage.</span></span> <span data-ttu-id="889c6-140">Bu bilgileri analiz etmek, işe alım için sürenin kısaltılması açısından önemli öngörüler sağlayabilir ve işe alım görevlilerinin her aşamada harcanan süreyi kısaltma yöntemlerine odaklanmasını sağlar.</span><span class="sxs-lookup"><span data-stu-id="889c6-140">Analyzing this information can provide insights critical to reducing time to hire and enable recruiters to focus on ways to reduce the time spent in each stage.</span></span>

## <a name="user-specific-security"></a><span data-ttu-id="889c6-141">Kullanıcıya özel güvenlik</span><span class="sxs-lookup"><span data-stu-id="889c6-141">User-specific security</span></span>

<span data-ttu-id="889c6-142">Attract raporlarına Yönetici, Tümünü Oku, İşe Alma Görevlisi ve İşe Alım Müdürü [rolleri](security-attract.md) tarafından erişilebilir.</span><span class="sxs-lookup"><span data-stu-id="889c6-142">Attract reports are accessible for Admin, Read All, Recruiter, and Hiring Manager [roles](security-attract.md).</span></span> <span data-ttu-id="889c6-143">Atanmamış kullanıcılar analitik rapor sayfalarına (İş analizi veya Analiz merkezi) erişime sahip değildir.</span><span class="sxs-lookup"><span data-stu-id="889c6-143">Unassigned users do not have access to either of the analytic report pages (Job Analytics or Analytics Hub).</span></span>

<span data-ttu-id="889c6-144">İş Analizi raporları, seçili iş için verileri gösterir.</span><span class="sxs-lookup"><span data-stu-id="889c6-144">Job Analytics reports display data for the selected job.</span></span> <span data-ttu-id="889c6-145">Analiz Merkezi bir kullanıcının görüntüleyebileceği tüm işlerden toplanan verileri bildirir.</span><span class="sxs-lookup"><span data-stu-id="889c6-145">Analytics Hub reports aggregate data across all jobs a user can view.</span></span> <span data-ttu-id="889c6-146">İşler sayfasında hem İşlerim hem de Tüm işleri görebilen kullanıcılar aynı öğeleri Analiz Merkezinde de görebilir.</span><span class="sxs-lookup"><span data-stu-id="889c6-146">Users that can view both My jobs and All jobs on the Jobs page have the same views available in the Analytics Hub.</span></span>

## <a name="cross-filter"></a><span data-ttu-id="889c6-147">Çapraz filtreleme</span><span class="sxs-lookup"><span data-stu-id="889c6-147">Cross-filter</span></span>

<span data-ttu-id="889c6-148">Power BI'nin harika özelliklerinden biri, bir rapor sayfasındaki tüm görsellerin birbirlerine bağlı olma şeklidir.</span><span class="sxs-lookup"><span data-stu-id="889c6-148">One of the great features of Power BI is the way all visuals on a report page are interconnected.</span></span> <span data-ttu-id="889c6-149">Görsellerin birinde bir veri noktası seçerseniz, seçimi temel alarak bu veriyi içeren sayfadaki tüm görseller değişir.</span><span class="sxs-lookup"><span data-stu-id="889c6-149">If you select a data point on one of the visuals, all the other visuals on the page that contain that data change, based on that selection.</span></span> <span data-ttu-id="889c6-150">Daha fazla bilgi edinmek ve bir örnek görüntülemek için bkz. [Power BI raporunda görseller birbirlerine nasıl çapraz filtre uygular](https://docs.microsoft.com/power-bi/consumer/end-user-interactions).</span><span class="sxs-lookup"><span data-stu-id="889c6-150">Find out more and see an example in [How visuals cross-filter each other in a Power BI report](https://docs.microsoft.com/power-bi/consumer/end-user-interactions).</span></span>

## <a name="export-to-excel"></a><span data-ttu-id="889c6-151">Excel'e aktar</span><span class="sxs-lookup"><span data-stu-id="889c6-151">Export to Excel</span></span>

<span data-ttu-id="889c6-152">Rapor verilerini Excel'de görüntülemek için görseldeki seçenekler menüsüne (üç nokta) tıklayıp **Temel alınan verileri dışa aktar**'ı seçebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="889c6-152">To view report data in Excel, you can click the options menu (three dots) on a visual and select **Export underlying data**.</span></span> <span data-ttu-id="889c6-153">Dışa aktarılan veriler Attract'teki kullanıcı izinleri dikkate alınarak filtrelenmiş aktarılır.</span><span class="sxs-lookup"><span data-stu-id="889c6-153">Exported data will export as filtered, respecting user permissions in Attract.</span></span> <span data-ttu-id="889c6-154">Daha fazla bilgi için bkz. [Görselleştirmelerden dışa veri aktarma](https://docs.microsoft.com/power-bi/visuals/power-bi-visualization-export-data).</span><span class="sxs-lookup"><span data-stu-id="889c6-154">For more information, see [Export data from visualizations](https://docs.microsoft.com/power-bi/visuals/power-bi-visualization-export-data).</span></span>
