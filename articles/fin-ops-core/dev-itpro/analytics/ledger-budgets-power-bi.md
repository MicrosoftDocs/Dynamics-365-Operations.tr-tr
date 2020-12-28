---
title: Gerçek - bütçe Power BI içeriği
description: Bu konu, Gerçek ve bütçe karşılaştırması Power BI içeriğini açıklar. Bu ayrıca, içeriğe dahil edilen raporların nasıl kullanılacağını açıklar ve içeriği oluşturmakta kullanılmış olan veri modeli ve varlıklar hakkında bilgi sağlar.
author: ryansandness
manager: AnnBe
ms.date: 12/18/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BudgetTrackingWorkspace
audience: Application user, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: ryansand
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: 6a185da5055741ac30c7e237ef72d07084644651
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 12/05/2020
ms.locfileid: "4685285"
---
# <a name="actual-vs-budget-power-bi-content"></a><span data-ttu-id="7d17e-104">Gerçek - bütçe Power BI içeriği</span><span class="sxs-lookup"><span data-stu-id="7d17e-104">Actual vs budget Power BI content</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="7d17e-105">Bu konu, **Gerçek ve bütçe** karşılaştırması Microsoft Power BI içeriğini açıklar.</span><span class="sxs-lookup"><span data-stu-id="7d17e-105">This topic describes the **Actual vs budget** Microsoft Power BI content.</span></span> <span data-ttu-id="7d17e-106">Bu Power BI raporlarına nasıl erişileceğini açıklar ve içeriği oluşturmakta kullanılmış olan veri modeli ve varlıklar hakkında bilgi sağlar.</span><span class="sxs-lookup"><span data-stu-id="7d17e-106">It explains how to access the Power BI reports, and provides information about the data model and entities that were used to build the content.</span></span>

## <a name="overview"></a><span data-ttu-id="7d17e-107">Genel bakış</span><span class="sxs-lookup"><span data-stu-id="7d17e-107">Overview</span></span>

<span data-ttu-id="7d17e-108">**Gerçek ve bütçe** karşılaştırması Power BI içeriği, gerçek ve bütçe performansı karşılaştırmasını kuruluşları içinde izlemekten sorumlu kişiler için oluşturulmuştur.</span><span class="sxs-lookup"><span data-stu-id="7d17e-108">The **Actual vs budget** Power BI content was created for individuals who are responsible for monitoring actual versus budget performance in their organization.</span></span> <span data-ttu-id="7d17e-109">**Gerçek ve bütçe** karşılaştırması Power BI içeriği, bütçe farklılıklarınıza görünürlük sağlar.</span><span class="sxs-lookup"><span data-stu-id="7d17e-109">The **Actual vs budget** Power BI content provides visibility into your budget variances.</span></span> <span data-ttu-id="7d17e-110">Farkların sebebini daha iyi anlayabilmek için geçerli yıl için bütçeyi hesap kategorisi, bütçe kodu, ana hesap, ana hesap açıklamaları veya mali dönem için analiz edebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="7d17e-110">You can analyze budget for the current year by account category, budget code, main account, main account descriptions, or fiscal period to get a better understanding of the cause of any variances.</span></span>

## <a name="accessing-the-power-bi-content"></a><span data-ttu-id="7d17e-111">Power BI içeriğine erişim</span><span class="sxs-lookup"><span data-stu-id="7d17e-111">Accessing the Power BI content</span></span>
<span data-ttu-id="7d17e-112">**Fiili - bütçe** karşılaştırması Power BI içeriğindeki raporlar **Genel muhasebe bütçesi ve tahminleri** ile **CFO** çalışma alanlarında gösterilir.</span><span class="sxs-lookup"><span data-stu-id="7d17e-112">Reports from the **Actual vs budget** Power BI content are shown in the **Ledger budget and forecasts** and **CFO** workspaces.</span></span>

## <a name="reports-that-are-included-in-the-power-bi-content"></a><span data-ttu-id="7d17e-113">Power BI içerik paketinde bulunan raporlar</span><span class="sxs-lookup"><span data-stu-id="7d17e-113">Reports that are included in the Power BI content</span></span>
<span data-ttu-id="7d17e-114">Aşağı tablo, **Gerçek ve bütçe** karşılaştırması Power BI içeriğinin her bir rapor sayfasında bulunan ölçümler hakkında ayrıntılar sağlar.</span><span class="sxs-lookup"><span data-stu-id="7d17e-114">The following table provides details about the metrics that are found on each report page in the **Actual vs budget** Power BI content.</span></span>

| <span data-ttu-id="7d17e-115">Rapor</span><span class="sxs-lookup"><span data-stu-id="7d17e-115">Report</span></span>                      | <span data-ttu-id="7d17e-116">Ölçümler</span><span class="sxs-lookup"><span data-stu-id="7d17e-116">Metrics</span></span>                                                                             |
|-----------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="7d17e-117">Giderler - Gerçek ve bütçe karşılaştırması</span><span class="sxs-lookup"><span data-stu-id="7d17e-117">Expenses - Actual vs budget</span></span> | <ul><li><span data-ttu-id="7d17e-118">Bu yılki toplam giderler</span><span class="sxs-lookup"><span data-stu-id="7d17e-118">Total expenses this year</span></span></li><li><span data-ttu-id="7d17e-119">Bu yılki bütçe toplam giderleri</span><span class="sxs-lookup"><span data-stu-id="7d17e-119">Budget total expenses this year</span></span></li></ul>  |
| <span data-ttu-id="7d17e-120">Gelirler - Gerçek ve bütçe karşılaştırması</span><span class="sxs-lookup"><span data-stu-id="7d17e-120">Revenue - Actual vs budget</span></span>  | <ul><li><span data-ttu-id="7d17e-121">Bu yılki toplam gelir</span><span class="sxs-lookup"><span data-stu-id="7d17e-121">Total revenue this year</span></span></li><li><span data-ttu-id="7d17e-122">Bu yılki bütçe toplam gelirler</span><span class="sxs-lookup"><span data-stu-id="7d17e-122">Budget total revenue this year</span></span></li><ul>     |
| <span data-ttu-id="7d17e-123">Gider</span><span class="sxs-lookup"><span data-stu-id="7d17e-123">Expense</span></span>                     | <ul><li><span data-ttu-id="7d17e-124">Bu yılki toplam giderler</span><span class="sxs-lookup"><span data-stu-id="7d17e-124">Total expenses this year</span></span></li><li><span data-ttu-id="7d17e-125">Bütçeye dayalı gider hedefleri</span><span class="sxs-lookup"><span data-stu-id="7d17e-125">Goal for expenses based on budget</span></span></li><ul> |
| <span data-ttu-id="7d17e-126">Gelir</span><span class="sxs-lookup"><span data-stu-id="7d17e-126">Revenue</span></span>                     | <ul><li><span data-ttu-id="7d17e-127">Bu yılki toplam gelir</span><span class="sxs-lookup"><span data-stu-id="7d17e-127">Total revenue this year</span></span></li><li><span data-ttu-id="7d17e-128">Bütçeye dayalı gelir hedefleri</span><span class="sxs-lookup"><span data-stu-id="7d17e-128">Goal for revenue based on budget</span></span></li><ul>   |
| <span data-ttu-id="7d17e-129">Net gelir</span><span class="sxs-lookup"><span data-stu-id="7d17e-129">Net income</span></span>                  | <ul><li><span data-ttu-id="7d17e-130">Bu yılki net gelir</span><span class="sxs-lookup"><span data-stu-id="7d17e-130">Net income this year</span></span></li><li><span data-ttu-id="7d17e-131">Bütçeye dayalı net gelir hedefleri</span><span class="sxs-lookup"><span data-stu-id="7d17e-131">Goal for net income based on budget</span></span></li><ul>   |

## <a name="understanding-the-data-model-and-entities"></a><span data-ttu-id="7d17e-132">Veri modellerini ve varlıklarını anlama</span><span class="sxs-lookup"><span data-stu-id="7d17e-132">Understanding the data model and entities</span></span>

| <span data-ttu-id="7d17e-133">Varlık</span><span class="sxs-lookup"><span data-stu-id="7d17e-133">Entity</span></span>                    | <span data-ttu-id="7d17e-134">İçindekiler</span><span class="sxs-lookup"><span data-stu-id="7d17e-134">Contents</span></span>                                                                         |
|---------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="7d17e-135">Genel Muhasebe Etkinlikleri</span><span class="sxs-lookup"><span data-stu-id="7d17e-135">General Ledger Activities</span></span> | <span data-ttu-id="7d17e-136">Genel muhasebe için hareket tutarları</span><span class="sxs-lookup"><span data-stu-id="7d17e-136">Transaction amounts for the general ledger</span></span>                                       |
| <span data-ttu-id="7d17e-137">Bütçe Etkinlikleri</span><span class="sxs-lookup"><span data-stu-id="7d17e-137">Budget Activities</span></span>         | <span data-ttu-id="7d17e-138">Bütçe kaydı için hareket tutarları</span><span class="sxs-lookup"><span data-stu-id="7d17e-138">Transaction amounts for the budget register</span></span>                                      |
| <span data-ttu-id="7d17e-139">Ana Hesaplar</span><span class="sxs-lookup"><span data-stu-id="7d17e-139">Main Accounts</span></span>             | <span data-ttu-id="7d17e-140">Raporların filtreleneceği ana hesaplar</span><span class="sxs-lookup"><span data-stu-id="7d17e-140">Main accounts to filter reports by</span></span>                                               |
| <span data-ttu-id="7d17e-141">Mali Takvimler</span><span class="sxs-lookup"><span data-stu-id="7d17e-141">Fiscal Calendars</span></span>          | <span data-ttu-id="7d17e-142">Raporların filtreleneceği mali takvimler</span><span class="sxs-lookup"><span data-stu-id="7d17e-142">Fiscal calendars to filter reports by</span></span>                                            |
| <span data-ttu-id="7d17e-143">Genel muhasebe defterleri</span><span class="sxs-lookup"><span data-stu-id="7d17e-143">Ledgers</span></span>                   | <span data-ttu-id="7d17e-144">Genel muhasebeler, geçerli genel muhasebe için raporları filtrelemek için kullanılabilir</span><span class="sxs-lookup"><span data-stu-id="7d17e-144">Ledgers that can be used to filter the report to the current ledger</span></span>              |
| <span data-ttu-id="7d17e-145">Bütçe Kodları</span><span class="sxs-lookup"><span data-stu-id="7d17e-145">Budget Codes</span></span>              | <span data-ttu-id="7d17e-146">Raporların filtreleneceği bütçe kodları</span><span class="sxs-lookup"><span data-stu-id="7d17e-146">Budget codes to filter reports by</span></span>                                                |
| <span data-ttu-id="7d17e-147">Tüzel Kişilikler</span><span class="sxs-lookup"><span data-stu-id="7d17e-147">Legal Entities</span></span>            | <span data-ttu-id="7d17e-148">Tüzel kişilikler, geçerli tüzel kişilikler için raporları filtrelemek için kullanılabilir</span><span class="sxs-lookup"><span data-stu-id="7d17e-148">Legal entities that can be used to filter the report to the current legal entity</span></span> |
