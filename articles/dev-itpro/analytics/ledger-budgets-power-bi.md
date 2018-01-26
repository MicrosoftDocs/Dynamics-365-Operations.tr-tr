---
title: "Gerçek ve bütçe karşılaştırması Power BI içeriği"
description: "Bu konu, Gerçek ve bütçe karşılaştırması Power BI içeriğini açıklar. Bu ayrıca, içeriğe dahil edilen raporların nasıl kullanılacağını açıklar ve içeriği oluşturmakta kullanılmış olan veri modeli ve varlıklar hakkında bilgi sağlar."
author: ryansandness
manager: AnnBe
ms.date: 12/18/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: BudgetTrackingWorkspace
audience: Application user, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: ryansand
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 8075abccdcdde21df967dcc9948a738895f35cef
ms.openlocfilehash: 13f7cfa8776436ed2c73fc588948ce88fee93326
ms.contentlocale: tr-tr
ms.lasthandoff: 01/25/2018

---

# <a name="actual-vs-budget-power-bi-content"></a><span data-ttu-id="696c1-104">Gerçek ve bütçe karşılaştırması Power BI içeriği</span><span class="sxs-lookup"><span data-stu-id="696c1-104">Actual vs budget Power BI content</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="696c1-105">Bu konu, **Gerçek ve bütçe karşılaştırması** Microsoft Power BI içeriğini açıklar.</span><span class="sxs-lookup"><span data-stu-id="696c1-105">This topic describes the **Actual vs budget** Microsoft Power BI content.</span></span> <span data-ttu-id="696c1-106">Power BI raporlarına nasıl erişileceğini açıklar ve içeriği oluşturmakta kullanılmış olan veri modeli ve varlıklar hakkında bilgi sağlar.</span><span class="sxs-lookup"><span data-stu-id="696c1-106">It explains how to access the Power BI reports, and provides information about the data model and entities that were used to build the content.</span></span> 

## <a name="overview"></a><span data-ttu-id="696c1-107">Özet</span><span class="sxs-lookup"><span data-stu-id="696c1-107">Overview</span></span>

<span data-ttu-id="696c1-108">**Gerçek ve bütçe karşılaştırması** Power BI içeriği, gerçek ve bütçe performansı karşılaştırmasını kuruluşları içinde izlemekten sorumlu kişiler için oluşturulmuştur.</span><span class="sxs-lookup"><span data-stu-id="696c1-108">The **Actual vs budget** Power BI content was created for individuals who are responsible for monitoring actual versus budget performance in their organization.</span></span> <span data-ttu-id="696c1-109">**Gerçek ve bütçe karşılaştırması** Power BI içeriği, bütçe farklılıklarınıza görünürlük sağlar.</span><span class="sxs-lookup"><span data-stu-id="696c1-109">The **Actual vs budget** Power BI content provides visibility into your budget variances.</span></span> <span data-ttu-id="696c1-110">Farkların sebebini daha iyi anlayabilmek için geçerli yıl için bütçeyi hesap kategorisi, bütçe kodu, ana hesap, ana hesap açıklamaları veya mali dönem için analiz edebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="696c1-110">You can analyze budget for the current year by account category, budget code, main account, main account descriptions, or fiscal period to get a better understanding of the cause of any variances.</span></span> 

## <a name="accessing-the-power-bi-content"></a><span data-ttu-id="696c1-111">Power BI içeriğine erişmek</span><span class="sxs-lookup"><span data-stu-id="696c1-111">Accessing the Power BI content</span></span>
<span data-ttu-id="696c1-112">**Fiili - bütçe karşılaştırması** Power BI içeriğindeki raporlar **Genel muhasebe bütçesi ve tahminleri** ile **CFO** çalışma alanlarında gösterilir.</span><span class="sxs-lookup"><span data-stu-id="696c1-112">Reports from the **Actual vs budget** Power BI content are shown in the **Ledger budget and forecasts** and **CFO** workspaces.</span></span>

## <a name="reports-that-are-included-in-the-power-bi-content"></a><span data-ttu-id="696c1-113">Power BI içeriğine dahil olan raporlar</span><span class="sxs-lookup"><span data-stu-id="696c1-113">Reports that are included in the Power BI content</span></span>
<span data-ttu-id="696c1-114">Aşağı tablo, **Gerçek ve bütçe karşılaştırması** Power BI içeriğinin her bir rapor sayfasında bulunan ölçümler hakkında ayrıntılar sağlar.</span><span class="sxs-lookup"><span data-stu-id="696c1-114">The following table provides details about the metrics that are found on each report page in the **Actual vs budget** Power BI content.</span></span>

| <span data-ttu-id="696c1-115">Rapor</span><span class="sxs-lookup"><span data-stu-id="696c1-115">Report</span></span>                      | <span data-ttu-id="696c1-116">Ölçümler</span><span class="sxs-lookup"><span data-stu-id="696c1-116">Metrics</span></span> |
|-----------------------------|---------|
| <span data-ttu-id="696c1-117">Giderler - Gerçek ve bütçe karşılaştırması</span><span class="sxs-lookup"><span data-stu-id="696c1-117">Expenses - Actual vs budget</span></span> | <ul><li><span data-ttu-id="696c1-118">Bu yılki toplam giderler</span><span class="sxs-lookup"><span data-stu-id="696c1-118">Total expenses this year</span></span></li><li><span data-ttu-id="696c1-119">Bu yılki bütçe toplam giderleri</span><span class="sxs-lookup"><span data-stu-id="696c1-119">Budget total expenses this year</span></span></li></ul> |
| <span data-ttu-id="696c1-120">Gelirler - Gerçek ve bütçe karşılaştırması</span><span class="sxs-lookup"><span data-stu-id="696c1-120">Revenue - Actual vs budget</span></span>  | <ul><li><span data-ttu-id="696c1-121">Bu yılki toplam gelir</span><span class="sxs-lookup"><span data-stu-id="696c1-121">Total revenue this year</span></span></li><li><span data-ttu-id="696c1-122">Bu yılki bütçe toplam gelirler</span><span class="sxs-lookup"><span data-stu-id="696c1-122">Budget total revenue this year</span></span></li><ul> |
| <span data-ttu-id="696c1-123">Gider</span><span class="sxs-lookup"><span data-stu-id="696c1-123">Expense</span></span>                     | <ul><li><span data-ttu-id="696c1-124">Bu yılki toplam giderler</span><span class="sxs-lookup"><span data-stu-id="696c1-124">Total expenses this year</span></span></li><li><span data-ttu-id="696c1-125">Bütçeye dayalı gider hedefleri</span><span class="sxs-lookup"><span data-stu-id="696c1-125">Goal for expenses based on budget</span></span> </li><ul> |
| <span data-ttu-id="696c1-126">Gelir</span><span class="sxs-lookup"><span data-stu-id="696c1-126">Revenue</span></span>                     | <ul><li><span data-ttu-id="696c1-127">Bu yılki toplam gelir</span><span class="sxs-lookup"><span data-stu-id="696c1-127">Total revenue this year</span></span></li><li><span data-ttu-id="696c1-128">Bütçeye dayalı gelir hedefleri</span><span class="sxs-lookup"><span data-stu-id="696c1-128">Goal for revenue based on budget</span></span> </li><ul> |
| <span data-ttu-id="696c1-129">Net gelir</span><span class="sxs-lookup"><span data-stu-id="696c1-129">Net income</span></span>                  | <ul><li><span data-ttu-id="696c1-130">Bu yılki net gelir</span><span class="sxs-lookup"><span data-stu-id="696c1-130">Net income this year</span></span></li><li><span data-ttu-id="696c1-131">Bütçeye dayalı net gelir hedefleri</span><span class="sxs-lookup"><span data-stu-id="696c1-131">Goal for net income based on budget</span></span> </li><ul> |


## <a name="understanding-the-data-model-and-entities"></a><span data-ttu-id="696c1-132">Veri modellerini ve varlıklarını anlama</span><span class="sxs-lookup"><span data-stu-id="696c1-132">Understanding the data model and entities</span></span>

| <span data-ttu-id="696c1-133">Varlık</span><span class="sxs-lookup"><span data-stu-id="696c1-133">Entity</span></span>                    | <span data-ttu-id="696c1-134">İçindekiler</span><span class="sxs-lookup"><span data-stu-id="696c1-134">Contents</span></span> |
|---------------------------|----------|
| <span data-ttu-id="696c1-135">Genel Muhasebe Etkinlikleri</span><span class="sxs-lookup"><span data-stu-id="696c1-135">General Ledger Activities</span></span> | <span data-ttu-id="696c1-136">Genel muhasebe için hareket tutarları</span><span class="sxs-lookup"><span data-stu-id="696c1-136">Transaction amounts for the general ledger</span></span> |
| <span data-ttu-id="696c1-137">Bütçe Etkinlikleri</span><span class="sxs-lookup"><span data-stu-id="696c1-137">Budget Activities</span></span>         | <span data-ttu-id="696c1-138">Bütçe kaydı için hareket tutarları</span><span class="sxs-lookup"><span data-stu-id="696c1-138">Transaction amounts for the budget register</span></span> |
| <span data-ttu-id="696c1-139">Ana Hesaplar</span><span class="sxs-lookup"><span data-stu-id="696c1-139">Main Accounts</span></span>             | <span data-ttu-id="696c1-140">Raporların filtreleneceği ana hesaplar</span><span class="sxs-lookup"><span data-stu-id="696c1-140">Main accounts to filter reports by</span></span> |
| <span data-ttu-id="696c1-141">Mali Takvimler</span><span class="sxs-lookup"><span data-stu-id="696c1-141">Fiscal Calendars</span></span>          | <span data-ttu-id="696c1-142">Raporların filtreleneceği mali takvimler</span><span class="sxs-lookup"><span data-stu-id="696c1-142">Fiscal calendars to filter reports by</span></span> |
| <span data-ttu-id="696c1-143">Genel muhasebe defterleri</span><span class="sxs-lookup"><span data-stu-id="696c1-143">Ledgers</span></span>                   | <span data-ttu-id="696c1-144">Genel muhasebeler, geçerli genel muhasebe için raporları filtrelemek için kullanılabilir</span><span class="sxs-lookup"><span data-stu-id="696c1-144">Ledgers that can be used to filter the report to the current ledger</span></span> |
| <span data-ttu-id="696c1-145">Bütçe Kodları</span><span class="sxs-lookup"><span data-stu-id="696c1-145">Budget Codes</span></span>              | <span data-ttu-id="696c1-146">Raporların filtreleneceği bütçe kodları</span><span class="sxs-lookup"><span data-stu-id="696c1-146">Budget codes to filter reports by</span></span> |
| <span data-ttu-id="696c1-147">Tüzel Kişilikler</span><span class="sxs-lookup"><span data-stu-id="696c1-147">Legal Entities</span></span>            | <span data-ttu-id="696c1-148">Tüzel kişilikler, geçerli tüzel kişilikler için raporları filtrelemek için kullanılabilir</span><span class="sxs-lookup"><span data-stu-id="696c1-148">Legal entities that can be used to filter the report to the current legal entity</span></span> |

