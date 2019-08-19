---
title: Gelir tablosu mali raporu
description: Bu makale varsayılan rapor için gelir tablolarını açıklar. Ayrıca, bu raporla ilişkili olan yapı taşlarını açıklar.
author: jcart1106
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: FinancialReports
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 12294
ms.assetid: 30820be0-d943-4f8b-8c25-6414ec393b3d
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b7c5d27d43b287aef87f5ead7f469d5465dd2dcb
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/01/2019
ms.locfileid: "1839099"
---
# <a name="income-statement-financial-report"></a><span data-ttu-id="7cbfa-104">Gelir tablosu mali raporu</span><span class="sxs-lookup"><span data-stu-id="7cbfa-104">Income statement financial report</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="7cbfa-105">Bu makale varsayılan rapor için gelir tablolarını açıklar.</span><span class="sxs-lookup"><span data-stu-id="7cbfa-105">This article describes the default report for income statements.</span></span> <span data-ttu-id="7cbfa-106">Ayrıca, bu raporla ilişkili olan yapı taşlarını açıklar.</span><span class="sxs-lookup"><span data-stu-id="7cbfa-106">It also describes the building blocks that are associated with this report.</span></span> 

<a name="default-income-statement-report"></a><span data-ttu-id="7cbfa-107">Varsayılan gelir tablosu raporu</span><span class="sxs-lookup"><span data-stu-id="7cbfa-107">Default income statement report</span></span>
-------------------------------

| <span data-ttu-id="7cbfa-108">Varsayılan rapor</span><span class="sxs-lookup"><span data-stu-id="7cbfa-108">Default report</span></span>             | <span data-ttu-id="7cbfa-109">Ne yapar</span><span class="sxs-lookup"><span data-stu-id="7cbfa-109">What it does</span></span>                                                                                              |
|----------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7cbfa-110">Gelir Beyanı – Varsayılan</span><span class="sxs-lookup"><span data-stu-id="7cbfa-110">Income Statement – Default</span></span> | <span data-ttu-id="7cbfa-111">Geçerli dönem ve ayrıca yılbaşından bugüne kadar olan süre için organizasyonun karlılığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="7cbfa-111">Provides a view of the organization’s profitability for the current period and also for the year to date.</span></span> |

## <a name="building-blocks"></a><span data-ttu-id="7cbfa-112">Yapı taşları</span><span class="sxs-lookup"><span data-stu-id="7cbfa-112">Building blocks</span></span>
<span data-ttu-id="7cbfa-113">Gelir tablosu mali raporu aşağıdaki yapı taşlarını kullanır.</span><span class="sxs-lookup"><span data-stu-id="7cbfa-113">The income statement financial report uses the following building blocks.</span></span>

| <span data-ttu-id="7cbfa-114">Varsayılan rapor</span><span class="sxs-lookup"><span data-stu-id="7cbfa-114">Default report</span></span>             | <span data-ttu-id="7cbfa-115">Satır tanımı</span><span class="sxs-lookup"><span data-stu-id="7cbfa-115">Row definition</span></span>                     | <span data-ttu-id="7cbfa-116">Sütun tanımı</span><span class="sxs-lookup"><span data-stu-id="7cbfa-116">Column definition</span></span>          |
|----------------------------|------------------------------------|----------------------------|
| <span data-ttu-id="7cbfa-117">Gelir Tablosu - Varsayılan</span><span class="sxs-lookup"><span data-stu-id="7cbfa-117">Income Statement - Default</span></span> | <span data-ttu-id="7cbfa-118">Özet Gelir Tablosu - Varsayılan</span><span class="sxs-lookup"><span data-stu-id="7cbfa-118">Summary Income Statement - Default</span></span> | <span data-ttu-id="7cbfa-119">Dönemsel ve YTD - Varsayılan</span><span class="sxs-lookup"><span data-stu-id="7cbfa-119">Periodic and YTD - Default</span></span> |

### <a name="row-definition"></a><span data-ttu-id="7cbfa-120">Satır tanımı</span><span class="sxs-lookup"><span data-stu-id="7cbfa-120">Row definition</span></span>

<span data-ttu-id="7cbfa-121">Satır tanımı, Özeti Gelir Tablosu – Varsayılan, klasik bir gelir tablosunun her bir kısmı için bir bölüm içerir.</span><span class="sxs-lookup"><span data-stu-id="7cbfa-121">The row definition, Summary Income Statement – Default, contains a section for each part of a traditional income statement.</span></span> <span data-ttu-id="7cbfa-122">Ana Hesap Kategorisi boyutu bu satır tanımının oluşturulması için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="7cbfa-122">The Main Account Category dimension is used to build this row definition.</span></span> <span data-ttu-id="7cbfa-123">Bu nedenle, herhangi biri hiçbir değişiklik yapmasına gerek kalmadan rapor oluşturabilir.</span><span class="sxs-lookup"><span data-stu-id="7cbfa-123">Therefore, anyone can generate the report without having to make any modifications.</span></span>

### <a name="column-definition"></a><span data-ttu-id="7cbfa-124">Sütun Tanımı</span><span class="sxs-lookup"><span data-stu-id="7cbfa-124">Column Definition</span></span>

<span data-ttu-id="7cbfa-125">Sütun tanımları, farklı ayrıntı ve mali veri düzeyleri sunmak üzere farklı türlerde sütunlar içerir.</span><span class="sxs-lookup"><span data-stu-id="7cbfa-125">The column definitions contain different types of columns to provide different levels of detail and financial data.</span></span>

-   <span data-ttu-id="7cbfa-126">**Dönemsel ve YTD – Varsayılan sütun türleri:**</span><span class="sxs-lookup"><span data-stu-id="7cbfa-126">**Periodic and YTD – Default column types:**</span></span>
    -   <span data-ttu-id="7cbfa-127">**DESC** – Satır tanımının açıklaması</span><span class="sxs-lookup"><span data-stu-id="7cbfa-127">**DESC** – The description from the row definition</span></span>
    -   <span data-ttu-id="7cbfa-128">**FD** – Mevcut dönem için mali veriler</span><span class="sxs-lookup"><span data-stu-id="7cbfa-128">**FD** – Financial data for the current period</span></span>
    -   <span data-ttu-id="7cbfa-129">**FD** – Yılbaşından bugüne kadar olan süre için mali veriler</span><span class="sxs-lookup"><span data-stu-id="7cbfa-129">**FD** – Financial data for the year to date</span></span>



<a name="additional-resources"></a><span data-ttu-id="7cbfa-130">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="7cbfa-130">Additional resources</span></span>
--------

[<span data-ttu-id="7cbfa-131">Mali raporlama</span><span class="sxs-lookup"><span data-stu-id="7cbfa-131">Financial reporting</span></span>](financial-reporting-getting-started.md)

[<span data-ttu-id="7cbfa-132">Mali raporları görüntüleme</span><span class="sxs-lookup"><span data-stu-id="7cbfa-132">View financial reports</span></span>](view-financial-reports.md)

[<span data-ttu-id="7cbfa-133">Dynamics Mali Raporlama Blogu</span><span class="sxs-lookup"><span data-stu-id="7cbfa-133">Dynamics Financial Reporting Blog</span></span>](https://blogs.msdn.com/b/dynamics_financial_reporting/)



