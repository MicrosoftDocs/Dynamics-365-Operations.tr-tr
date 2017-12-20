---
title: "Gerçek ve bütçe karşılaştırması Power BI içeriği"
description: "Bu konu, Gerçek ve bütçe karşılaştırması Power BI içeriğini açıklar. Bu ayrıca, içeriğe dahil edilen raporların nasıl kullanılacağını açıklar ve içeriği oluşturmakta kullanılmış olan veri modeli ve varlıklar hakkında bilgi sağlar."
author: ryansandness
manager: AnnBe
ms.date: 12/01/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application user, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: ryansand
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 6e64337f19600b18320550d91c134949c33af7b0
ms.openlocfilehash: 2a0ad5af4e4d7da09690331dc9d1a51d2e97a664
ms.contentlocale: tr-tr
ms.lasthandoff: 12/01/2017

---

# <a name="actual-vs-budget-power-bi-content"></a><span data-ttu-id="213be-104">Gerçek ve bütçe karşılaştırması Power BI içeriği</span><span class="sxs-lookup"><span data-stu-id="213be-104">Actual vs budget Power BI content</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="213be-105">Bu konu, **Gerçek ve bütçe karşılaştırması** Microsoft Power BI içeriğini açıklar.</span><span class="sxs-lookup"><span data-stu-id="213be-105">This topic describes the **Actual vs budget** Microsoft Power BI content.</span></span> <span data-ttu-id="213be-106">Power BI raporlarına nasıl erişileceğini açıklar ve içeriği oluşturmakta kullanılmış olan veri modeli ve varlıklar hakkında bilgi sağlar.</span><span class="sxs-lookup"><span data-stu-id="213be-106">It explains how to access the Power BI reports, and provides information about the data model and entities that were used to build the content.</span></span> 

# <a name="overview"></a><span data-ttu-id="213be-107">Özet</span><span class="sxs-lookup"><span data-stu-id="213be-107">Overview</span></span>

<span data-ttu-id="213be-108">**Gerçek ve bütçe karşılaştırması** Power BI içeriği, gerçek ve bütçe performansı karşılaştırmasını kuruluşları içinde izlemekten sorumlu kişiler için oluşturulmuştur.</span><span class="sxs-lookup"><span data-stu-id="213be-108">The **Actual vs budget** Power BI content was created for individuals who are responsible for monitoring actual versus budget performance in their organization.</span></span> <span data-ttu-id="213be-109">**Gerçek ve bütçe karşılaştırması** Power BI içeriği, bütçe farklılıklarınıza görünürlük sağlar.</span><span class="sxs-lookup"><span data-stu-id="213be-109">The **Actual vs budget** Power BI content provides visibility into your budget variances.</span></span> <span data-ttu-id="213be-110">Farkların sebebini daha iyi anlayabilmek için geçerli yıl için bütçeyi hesap kategorisi, bütçe kodu, ana hesap, ana hesap açıklamaları veya mali dönem için analiz edebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="213be-110">You can analyze budget for the current year by account category, budget code, main account, main account descriptions, or fiscal period to get a better understanding of the cause of any variances.</span></span> 

# <a name="accessing-the-power-bi-content"></a><span data-ttu-id="213be-111">Power BI içeriğine erişmek</span><span class="sxs-lookup"><span data-stu-id="213be-111">Accessing the Power BI content</span></span>
<span data-ttu-id="213be-112">**Fiili - bütçe karşılaştırması** Power BI içeriğindeki raporlar **Genel muhasebe bütçesi ve tahminleri** ile **CFO** çalışma alanlarında gösterilir.</span><span class="sxs-lookup"><span data-stu-id="213be-112">Reports from the **Actual vs budget** Power BI content are shown in the **Ledger budget and forecasts** and **CFO** workspaces.</span></span>

# <a name="reports-that-are-included-in-the-power-bi-content"></a><span data-ttu-id="213be-113">Power BI içeriğine dahil olan raporlar</span><span class="sxs-lookup"><span data-stu-id="213be-113">Reports that are included in the Power BI content</span></span>
<span data-ttu-id="213be-114">Aşağı tablo, **Gerçek ve bütçe karşılaştırması** Power BI içeriğinin her bir rapor sayfasında bulunan ölçümler hakkında ayrıntılar sağlar.</span><span class="sxs-lookup"><span data-stu-id="213be-114">The following table provides details about the metrics that are found on each report page in the **Actual vs budget** Power BI content.</span></span>

| <span data-ttu-id="213be-115">Rapor</span><span class="sxs-lookup"><span data-stu-id="213be-115">Report</span></span>                      | <span data-ttu-id="213be-116">Ölçümler</span><span class="sxs-lookup"><span data-stu-id="213be-116">Metrics</span></span> |
|-----------------------------|---------|
| <span data-ttu-id="213be-117">Giderler - Gerçek ve bütçe karşılaştırması</span><span class="sxs-lookup"><span data-stu-id="213be-117">Expenses - Actual vs budget</span></span> | <ul><li><span data-ttu-id="213be-118">Bu yılki toplam giderler</span><span class="sxs-lookup"><span data-stu-id="213be-118">Total expenses this year</span></span></li><li><span data-ttu-id="213be-119">Bu yılki bütçe toplam giderleri</span><span class="sxs-lookup"><span data-stu-id="213be-119">Budget total expenses this year</span></span></li></ul> |
| <span data-ttu-id="213be-120">Gelirler - Gerçek ve bütçe karşılaştırması</span><span class="sxs-lookup"><span data-stu-id="213be-120">Revenue - Actual vs budget</span></span>  | <ul><li><span data-ttu-id="213be-121">Bu yılki toplam gelir</span><span class="sxs-lookup"><span data-stu-id="213be-121">Total revenue this year</span></span></li><li><span data-ttu-id="213be-122">Bu yılki bütçe toplam gelirler</span><span class="sxs-lookup"><span data-stu-id="213be-122">Budget total revenue this year</span></span></li><ul> |
| <span data-ttu-id="213be-123">Gider</span><span class="sxs-lookup"><span data-stu-id="213be-123">Expense</span></span>                     | <ul><li><span data-ttu-id="213be-124">Bu yılki toplam giderler</span><span class="sxs-lookup"><span data-stu-id="213be-124">Total expenses this year</span></span></li><li><span data-ttu-id="213be-125">Bütçeye dayalı gider hedefleri</span><span class="sxs-lookup"><span data-stu-id="213be-125">Goal for expenses based on budget</span></span> </li><ul> |
| <span data-ttu-id="213be-126">Gelir</span><span class="sxs-lookup"><span data-stu-id="213be-126">Revenue</span></span>                     | <ul><li><span data-ttu-id="213be-127">Bu yılki toplam gelir</span><span class="sxs-lookup"><span data-stu-id="213be-127">Total revenue this year</span></span></li><li><span data-ttu-id="213be-128">Bütçeye dayalı gelir hedefleri</span><span class="sxs-lookup"><span data-stu-id="213be-128">Goal for revenue based on budget</span></span> </li><ul> |
| <span data-ttu-id="213be-129">Net gelir</span><span class="sxs-lookup"><span data-stu-id="213be-129">Net income</span></span>                  | <ul><li><span data-ttu-id="213be-130">Bu yılki net gelir</span><span class="sxs-lookup"><span data-stu-id="213be-130">Net income this year</span></span></li><li><span data-ttu-id="213be-131">Bütçeye dayalı net gelir hedefleri</span><span class="sxs-lookup"><span data-stu-id="213be-131">Goal for net income based on budget</span></span> </li><ul> |

## <a name="extending-the-power-bi-content"></a><span data-ttu-id="213be-132">Power BI içeriğini genişletmek</span><span class="sxs-lookup"><span data-stu-id="213be-132">Extending the Power BI content</span></span>
<span data-ttu-id="213be-133">Microsoft Dynamics Lifecycle Services (LCS) içinde kullanılabilir durumda olan içerik paketlerini kullanarak, Microsoft Dynamics 365'e oturum açmayan kişilere harika analizler sunabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="213be-133">By using the content packs that are available in Microsoft Dynamics Lifecycle Services (LCS), you can provide great analytics to people who don't sign in to Microsoft Dynamics 365.</span></span> <span data-ttu-id="213be-134">Bu içerik paketlerini diğer raporları veya görsel öğeleri içerecek şekilde değiştirebilir ve içerik paketlerini analiz için Power BI.com kiracınıza yayınlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="213be-134">You can modify these content packs so that they include other reports or visuals, and then publish the content packs to your Power BI.com tenant for analysis.</span></span> 

<span data-ttu-id="213be-135">**Gerçek ve bütçe karşılaştırması** Power BI içeriğini LCS'deki Paylaşılan varlıklar kitaplığında bulabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="213be-135">You can find the **Actual vs budget** Power BI content in the Shared assets library in LCS.</span></span> <span data-ttu-id="213be-136">İçeriği indirmek ve kuruluşunuzda tümleştirmek hakkında daha fazla bilgi için bkz. [Microsoft LCS ve iş ortaklarınızdan Power BI içeriği](power-bi-content-microsoft-partners.md).</span><span class="sxs-lookup"><span data-stu-id="213be-136">For more information about how to download the content and implement it in your organization, see [Power BI content in LCS from Microsoft and your partners](power-bi-content-microsoft-partners.md).</span></span> <span data-ttu-id="213be-137">Power BI içeriğinin nasıl uygulanacağını gösteren bir demo izlemek için bakınız [Microsoft ve Dynamics Lifecycle Services ortaklarınızdan Power BI içeriği](https://mix.office.com/watch/9puyb1b2xs1w) Office Mix.</span><span class="sxs-lookup"><span data-stu-id="213be-137">To watch a demo that shows how to implement the Power BI content, see the [Power BI content from Microsoft and your partners in Dynamics Lifecycle Services](https://mix.office.com/watch/9puyb1b2xs1w) Office Mix.</span></span>

# <a name="understanding-the-data-model-and-entities"></a><span data-ttu-id="213be-138">Veri modellerini ve varlıklarını anlama</span><span class="sxs-lookup"><span data-stu-id="213be-138">Understanding the data model and entities</span></span>

| <span data-ttu-id="213be-139">Varlık</span><span class="sxs-lookup"><span data-stu-id="213be-139">Entity</span></span>                    | <span data-ttu-id="213be-140">İçindekiler</span><span class="sxs-lookup"><span data-stu-id="213be-140">Contents</span></span> |
|---------------------------|----------|
| <span data-ttu-id="213be-141">Genel Muhasebe Etkinlikleri</span><span class="sxs-lookup"><span data-stu-id="213be-141">General Ledger Activities</span></span> | <span data-ttu-id="213be-142">Genel muhasebe için hareket tutarları</span><span class="sxs-lookup"><span data-stu-id="213be-142">Transaction amounts for the general ledger</span></span> |
| <span data-ttu-id="213be-143">Bütçe Etkinlikleri</span><span class="sxs-lookup"><span data-stu-id="213be-143">Budget Activities</span></span>         | <span data-ttu-id="213be-144">Bütçe kaydı için hareket tutarları</span><span class="sxs-lookup"><span data-stu-id="213be-144">Transaction amounts for the budget register</span></span> |
| <span data-ttu-id="213be-145">Ana Hesaplar</span><span class="sxs-lookup"><span data-stu-id="213be-145">Main Accounts</span></span>             | <span data-ttu-id="213be-146">Raporların filtreleneceği ana hesaplar</span><span class="sxs-lookup"><span data-stu-id="213be-146">Main accounts to filter reports by</span></span> |
| <span data-ttu-id="213be-147">Mali Takvimler</span><span class="sxs-lookup"><span data-stu-id="213be-147">Fiscal Calendars</span></span>          | <span data-ttu-id="213be-148">Raporların filtreleneceği mali takvimler</span><span class="sxs-lookup"><span data-stu-id="213be-148">Fiscal calendars to filter reports by</span></span> |
| <span data-ttu-id="213be-149">Genel muhasebe defterleri</span><span class="sxs-lookup"><span data-stu-id="213be-149">Ledgers</span></span>                   | <span data-ttu-id="213be-150">Genel muhasebeler, geçerli genel muhasebe için raporları filtrelemek için kullanılabilir</span><span class="sxs-lookup"><span data-stu-id="213be-150">Ledgers that can be used to filter the report to the current ledger</span></span> |
| <span data-ttu-id="213be-151">Bütçe Kodları</span><span class="sxs-lookup"><span data-stu-id="213be-151">Budget Codes</span></span>              | <span data-ttu-id="213be-152">Raporların filtreleneceği bütçe kodları</span><span class="sxs-lookup"><span data-stu-id="213be-152">Budget codes to filter reports by</span></span> |
| <span data-ttu-id="213be-153">Tüzel Kişilikler</span><span class="sxs-lookup"><span data-stu-id="213be-153">Legal Entities</span></span>            | <span data-ttu-id="213be-154">Tüzel kişilikler, geçerli tüzel kişilikler için raporları filtrelemek için kullanılabilir</span><span class="sxs-lookup"><span data-stu-id="213be-154">Legal entities that can be used to filter the report to the current legal entity</span></span> |

