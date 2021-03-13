---
title: Satınalma ve harcama analizi Power BI içeriği
description: Bu konu, Power BI Satınalma harcaması analizinde nelerin bulunduğunu açıklar.
author: FrankDahl
manager: AnnBe
ms.date: 04/24/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: PurchaseSpendAnalysisPowerBI
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: 265434
ms.assetid: 3cd9dfce-2687-4303-bc78-349e7cb5ea75
ms.search.region: global
ms.author: fdahl
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 5914abaafab509e278d7a85441928feddb0b5164
ms.sourcegitcommit: 5192cfaedfd861faea63d8954d7bcc500608a225
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/30/2021
ms.locfileid: "5093454"
---
# <a name="purchase-spend-analysis-power-bi-content"></a><span data-ttu-id="5c4ad-103">Satınalma ve harcama analizi Power BI içeriği</span><span class="sxs-lookup"><span data-stu-id="5c4ad-103">Purchase spend analysis Power BI content</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="5c4ad-104">Bu konu, Microsoft Power BI **Satınalma harcaması analizinde** nelerin bulunduğunu açıklar.</span><span class="sxs-lookup"><span data-stu-id="5c4ad-104">This topic describes what is included in the **Purchase spend analysis** Microsoft Power BI content.</span></span> <span data-ttu-id="5c4ad-105">Bu Power BI raporlarına nasıl erişileceğini açıklar ve içeriği oluşturmakta kullanılmış olan veri modeli ve varlıklar hakkında bilgi sağlar.</span><span class="sxs-lookup"><span data-stu-id="5c4ad-105">It explains how to access the Power BI reports, and provides information about the data model and entities that are used to build the content.</span></span>

## <a name="overview"></a><span data-ttu-id="5c4ad-106">Genel bakış</span><span class="sxs-lookup"><span data-stu-id="5c4ad-106">Overview</span></span>

<span data-ttu-id="5c4ad-107">**Satınalma harcaması analizi** Power BI içeriği satınalma yöneticilerine ve bütçelerden sorumlu yöneticilere satınalma harcamalarını izleme konusunda yardımcı olmak üzere tasarlanmıştır.</span><span class="sxs-lookup"><span data-stu-id="5c4ad-107">The **Purchase spend analysis** Power BI content was designed to help purchasing managers and managers who are responsible for budgets keep track of purchase spending.</span></span> <span data-ttu-id="5c4ad-108">Yöneticiler satınalma harcamasını aşağıdaki şekillerde analiz edebilirler:</span><span class="sxs-lookup"><span data-stu-id="5c4ad-108">Managers can analyze purchase spending in the following ways:</span></span>

- <span data-ttu-id="5c4ad-109">Yılbaşından bugüne satınalma (satıcı grubu ve tek tek satıcılara, tedarik kategorisine ve bireysel ürünlere ve satıcı konumuna göre)</span><span class="sxs-lookup"><span data-stu-id="5c4ad-109">Year-to-date purchase (by vendor group and individual vendors, procurement category and individual products, and vendor location)</span></span>
- <span data-ttu-id="5c4ad-110">Yıldan yıla satınalma değişikliği (satıcı grubu ve tedarik kategorisine göre)</span><span class="sxs-lookup"><span data-stu-id="5c4ad-110">Year-over-year purchase change (by vendor group and procurement category)</span></span>

<span data-ttu-id="5c4ad-111">İçerik, alınan satınalma hareketi verilerini kullanır ve hem şirket çapında satınalma rakamlarının toplam görünümünü hem de satıcı ve ürünler için satınalma harcamasının dağılımını verir.</span><span class="sxs-lookup"><span data-stu-id="5c4ad-111">The content uses purchase transactional data, and provides both an aggregate view of the company-wide purchase figures and a breakdown of purchase spending by vendor and product.</span></span> <span data-ttu-id="5c4ad-112">Raporlar satınalma harcamalarında zaman içindeki değişiklikleri öne çıkarır.</span><span class="sxs-lookup"><span data-stu-id="5c4ad-112">Reports highlight changes in purchase spending over time.</span></span> <span data-ttu-id="5c4ad-113">Bu nedenle, raporlar yöneticileri ayrı satıcılar ve ürünlerle ilgili olarak pozitif ve negatif harcama eğilimleri hakkında uyarmak için kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="5c4ad-113">Therefore, the reports can be used to alert managers about positive and negative spending trends for individual vendors and products.</span></span> <span data-ttu-id="5c4ad-114">Ek olarak grafikler farklı tedarik kategorileri ve satıcı grupları için satınalma harcamasını gösterir.</span><span class="sxs-lookup"><span data-stu-id="5c4ad-114">Additionally, charts show purchase spending for different procurement categories and vendor groups.</span></span> <span data-ttu-id="5c4ad-115">Bu nedenle, kategori ve bölgesel yöneticiler, harcama davranışındaki değişiklikleri tanımlamaya yardımcı olması açısından bu grafikleri kullanabilirler.</span><span class="sxs-lookup"><span data-stu-id="5c4ad-115">Therefore, category and regional managers can use the charts to help identify changes in spending behavior.</span></span>

## <a name="accessing-the-power-bi-content"></a><span data-ttu-id="5c4ad-116">Power BI içeriğine erişim</span><span class="sxs-lookup"><span data-stu-id="5c4ad-116">Accessing the Power BI content</span></span>
<span data-ttu-id="5c4ad-117">**Satınalma ve harcama analizi** Power BI içeriği **Satın alma ve harcama analizi** sayfasında gösterilir (**Tedarik ve kaynak atama** \> **Sorgular ve raporlar** \> **Satın alma performansı analizi** \> **Satın alma ve harcama analizi**).</span><span class="sxs-lookup"><span data-stu-id="5c4ad-117">The **Purchase spend analysis** Power BI content is shown on the **Purchase and spend analysis** page (**Procurement and sourcing** \> **Inquiries and reports** \> **Purchase performance analysis** \> **Purchase and spend analysis**).</span></span>

## <a name="metrics-that-are-included-in-the-power-bi-content"></a><span data-ttu-id="5c4ad-118">Power BI içerik paketinde bulunan ölçümler</span><span class="sxs-lookup"><span data-stu-id="5c4ad-118">Metrics that are included in the Power BI content</span></span>
<span data-ttu-id="5c4ad-119">**Satın alma harcaması analizi** Power BI içeriği bir dizi ölçümden oluşan bir rapor içerir.</span><span class="sxs-lookup"><span data-stu-id="5c4ad-119">The **Purchase spend analysis** Power BI content includes a report that consists of a set of metrics.</span></span> <span data-ttu-id="5c4ad-120">Bu ölçümler grafikler, kutucuklar ve tablolar şeklinde görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="5c4ad-120">These metrics are visualized as charts, tiles, and tables.</span></span> 

<span data-ttu-id="5c4ad-121">Aşağıdaki bölümde, görsellere yönelik genel bakış sunulur.</span><span class="sxs-lookup"><span data-stu-id="5c4ad-121">The following sections provide an overview of the visualizations.</span></span>

### <a name="purchase-by-vendor-report-page"></a><span data-ttu-id="5c4ad-122">Satıcı bazında satınalma rapor sayfası</span><span class="sxs-lookup"><span data-stu-id="5c4ad-122">Purchase by vendor report page</span></span>
<span data-ttu-id="5c4ad-123">**Grafikler**</span><span class="sxs-lookup"><span data-stu-id="5c4ad-123">**Charts**</span></span>
- <span data-ttu-id="5c4ad-124">Satınalmaya göre en iyi 10 satıcı (yığılmış çubuk grafik)</span><span class="sxs-lookup"><span data-stu-id="5c4ad-124">Top 10 vendors by purchase (stacked bar chart)</span></span>
- <span data-ttu-id="5c4ad-125">Satıcı grubuna / ülkeye / ada göre toplam satınalma (pasta grafik)</span><span class="sxs-lookup"><span data-stu-id="5c4ad-125">Total purchase by vendor group / country / name (pie chart)</span></span>
- <span data-ttu-id="5c4ad-126">Satıcı grubuna / ülkeye / ada göre satınalma (sütun grafik)</span><span class="sxs-lookup"><span data-stu-id="5c4ad-126">Purchase by vendor group / country / name (column chart)</span></span>
- <span data-ttu-id="5c4ad-127">Satıcı grubuna / ülkeye / ada göre ortalama satınalma (sütun grafik)</span><span class="sxs-lookup"><span data-stu-id="5c4ad-127">Average purchase by vendor group / country / name (column chart)</span></span>

<span data-ttu-id="5c4ad-128">**Kutucuklar**</span><span class="sxs-lookup"><span data-stu-id="5c4ad-128">**Tiles**</span></span>
- <span data-ttu-id="5c4ad-129">Satınalma toplamı</span><span class="sxs-lookup"><span data-stu-id="5c4ad-129">Total purchase</span></span>
- <span data-ttu-id="5c4ad-130">Yıllara göre satınalmadaki büyüme</span><span class="sxs-lookup"><span data-stu-id="5c4ad-130">YOY purchase growth</span></span>
- <span data-ttu-id="5c4ad-131">Toplam satıcı sayısı</span><span class="sxs-lookup"><span data-stu-id="5c4ad-131">Total # vendors</span></span>
- <span data-ttu-id="5c4ad-132">Toplam etkin satıcı sayısı</span><span class="sxs-lookup"><span data-stu-id="5c4ad-132">Total # of active vendors</span></span>

<span data-ttu-id="5c4ad-133">**Örnek**</span><span class="sxs-lookup"><span data-stu-id="5c4ad-133">**Example**</span></span>
<img src="media/spend1.png" alt="Purchase by vendor">

### <a name="purchase-by-product-report-page"></a><span data-ttu-id="5c4ad-134">Ürün bazında satınalma rapor sayfası</span><span class="sxs-lookup"><span data-stu-id="5c4ad-134">Purchase by product report page</span></span>

<span data-ttu-id="5c4ad-135">**Grafikler**</span><span class="sxs-lookup"><span data-stu-id="5c4ad-135">**Charts**</span></span>
- <span data-ttu-id="5c4ad-136">Tedarik kategorisine / ürün adına göre satınalma (sütun grafiği)</span><span class="sxs-lookup"><span data-stu-id="5c4ad-136">Purchase by procurement category / product name (column chart)</span></span>
- <span data-ttu-id="5c4ad-137">Tedarik kategorisine / ürün adına göre toplam satınalma (pasta grafik)</span><span class="sxs-lookup"><span data-stu-id="5c4ad-137">Total purchase by procurement category / product name (pie chart)</span></span>
- <span data-ttu-id="5c4ad-138">Satınalmaya göre en iyi 10 ürün (yığılmış çubuk grafik)</span><span class="sxs-lookup"><span data-stu-id="5c4ad-138">Top 10 products by purchase (stacked bar chart)</span></span>

<span data-ttu-id="5c4ad-139">**Kutucuklar**</span><span class="sxs-lookup"><span data-stu-id="5c4ad-139">**Tiles**</span></span>
- <span data-ttu-id="5c4ad-140">Toplam ürün sayısı</span><span class="sxs-lookup"><span data-stu-id="5c4ad-140">Total # of products</span></span></li>
- <span data-ttu-id="5c4ad-141">Etkin ürünlerin toplam sayısının toplam etkin ürünlere yüzdesi</span><span class="sxs-lookup"><span data-stu-id="5c4ad-141">Total active products percentage of total # of products</span></span>
- <span data-ttu-id="5c4ad-142">Satınalmanın %80'ini oluşturan ürünlerin sayısı</span><span class="sxs-lookup"><span data-stu-id="5c4ad-142">Number of products accounting for 80% purchase</span></span>

<span data-ttu-id="5c4ad-143">**Örnek**</span><span class="sxs-lookup"><span data-stu-id="5c4ad-143">**Example**</span></span>


<img src="media/purchaseByProduct.png" alt="Purchase by Product">

### <a name="purchase-by-period-report-page"></a><span data-ttu-id="5c4ad-144">Dönem bazında satınalma rapor sayfası</span><span class="sxs-lookup"><span data-stu-id="5c4ad-144">Purchase by period report page</span></span>
<span data-ttu-id="5c4ad-145">Bu sayfa bu yılki ve geçen yılki satınalmayı ve tedarik kategorisine göre büyümeyi gösterir.</span><span class="sxs-lookup"><span data-stu-id="5c4ad-145">This page shows purchases this year and last year, and growth by procurement category.</span></span>

<span data-ttu-id="5c4ad-146">**Grafikler**</span><span class="sxs-lookup"><span data-stu-id="5c4ad-146">**Charts**</span></span> 
- <span data-ttu-id="5c4ad-147">Aya / güne göre satınalma (sütun grafiği)</span><span class="sxs-lookup"><span data-stu-id="5c4ad-147">Purchase by month / day (column chart)</span></span>
- <span data-ttu-id="5c4ad-148">Toplam satınalmanın yıllara görefarkı (şelale grafik)</span><span class="sxs-lookup"><span data-stu-id="5c4ad-148">Cumulative purchase YOY variance (waterfall chart)</span></span>
- <span data-ttu-id="5c4ad-149">Toplam satınalmada yıllara göre büyüme (sütun grafik)</span><span class="sxs-lookup"><span data-stu-id="5c4ad-149">Total purchase YOY growth (column chart)</span></span>
- <span data-ttu-id="5c4ad-150">Tedarik ekstresi (matriks)</span><span class="sxs-lookup"><span data-stu-id="5c4ad-150">Procurement statement (matrix)</span></span>

<span data-ttu-id="5c4ad-151">**Kutucuklar**</span><span class="sxs-lookup"><span data-stu-id="5c4ad-151">**Tiles**</span></span>
- <span data-ttu-id="5c4ad-152">Yıllara göre satınalmadaki büyüme</span><span class="sxs-lookup"><span data-stu-id="5c4ad-152">YOY purchase growth</span></span>
- <span data-ttu-id="5c4ad-153">Yıllara göre satınalmadaki büyüme yüzdesi</span><span class="sxs-lookup"><span data-stu-id="5c4ad-153">YOY purchase growth %</span></span>

<span data-ttu-id="5c4ad-154">**Örnek**</span><span class="sxs-lookup"><span data-stu-id="5c4ad-154">**Example**</span></span>
<img src="media/purchaseByPeriod.png" alt="Purchase by Period">

### <a name="purchase-by-vendor-location-report-page"></a><span data-ttu-id="5c4ad-155">Satıcı konumu bazında satınalma rapor sayfası</span><span class="sxs-lookup"><span data-stu-id="5c4ad-155">Purchase by vendor location report page</span></span>

<span data-ttu-id="5c4ad-156">**Grafikler**</span><span class="sxs-lookup"><span data-stu-id="5c4ad-156">**Charts**</span></span>
- <span data-ttu-id="5c4ad-157">Şehre göre satınalma</span><span class="sxs-lookup"><span data-stu-id="5c4ad-157">Purchase by city</span></span>
- <span data-ttu-id="5c4ad-158">Satınalmada yıldan yıla büyüme yüzdesi</span><span class="sxs-lookup"><span data-stu-id="5c4ad-158">Purchase YOY growth %</span></span>
- <span data-ttu-id="5c4ad-159">Ülkeye göre satınalma</span><span class="sxs-lookup"><span data-stu-id="5c4ad-159">Purchase by country</span></span>

<span data-ttu-id="5c4ad-160">**Örnek**</span><span class="sxs-lookup"><span data-stu-id="5c4ad-160">**Example**</span></span>
<img src="media/purchByVendorLocation.png" alt="Purchase by Vendor Location">

### <a name="purchase-spend-analysis-by-time-report-page"></a><span data-ttu-id="5c4ad-161">Zamana göre satınalma harcaması analizi rapor sayfası</span><span class="sxs-lookup"><span data-stu-id="5c4ad-161">Purchase spend analysis by time report page</span></span>

<span data-ttu-id="5c4ad-162">**Grafikler**</span><span class="sxs-lookup"><span data-stu-id="5c4ad-162">**Charts**</span></span> 
- <span data-ttu-id="5c4ad-163">Aya / güne göre geçerli yıldaki satın alma (çizgi grafiği)</span><span class="sxs-lookup"><span data-stu-id="5c4ad-163">Purchase current year by month / day (line chart)</span></span>
- <span data-ttu-id="5c4ad-164">Geçerli yıl ve önceki yıldaki satınalma (satır ve sütun grafiği)</span><span class="sxs-lookup"><span data-stu-id="5c4ad-164">Purchase current and last year (line and column chart)</span></span>

<span data-ttu-id="5c4ad-165">**Örnek**</span><span class="sxs-lookup"><span data-stu-id="5c4ad-165">**Example**</span></span>
<img src="media/PurchByTIme.png" alt="Purchase by Time">

### <a name="purchase-spend-analysis-by-vendor-report-page"></a><span data-ttu-id="5c4ad-166">Satıcıya göre satınalma harcaması analizi rapor sayfası</span><span class="sxs-lookup"><span data-stu-id="5c4ad-166">Purchase spend analysis by vendor report page</span></span>

<span data-ttu-id="5c4ad-167">**Grafikler**</span><span class="sxs-lookup"><span data-stu-id="5c4ad-167">**Charts**</span></span> 
- <span data-ttu-id="5c4ad-168">İlk 10 satıcı satınalmanın satınalmaya göre yüzdesi (huni)</span><span class="sxs-lookup"><span data-stu-id="5c4ad-168">Top 10 vendor purchase % of purchase (funnel)</span></span>
- <span data-ttu-id="5c4ad-169">Yıllara göre artan harcamayla en iyi 10 satıcı</span><span class="sxs-lookup"><span data-stu-id="5c4ad-169">Top 10 vendors with increased spending YOY</span></span>
- <span data-ttu-id="5c4ad-170">Yıllara göre azalan harcamayla en iyi 10 satıcı</span><span class="sxs-lookup"><span data-stu-id="5c4ad-170">Top 10 vendors with decreased spending YOY</span></span>

<span data-ttu-id="5c4ad-171">**Örnek** 
</span><span class="sxs-lookup"><span data-stu-id="5c4ad-171">**Example** 
</span></span><img src="media/PurchSpendAnalysisByVendor.png" alt="Purchase spend by vendor">


## <a name="data-model-and-entities"></a><span data-ttu-id="5c4ad-172">Veri modeli ve varlıklar</span><span class="sxs-lookup"><span data-stu-id="5c4ad-172">Data model and entities</span></span>
<span data-ttu-id="5c4ad-173">Aşağıdaki veriler **Satınalma harcaması analizi** Power BI içeriğindeki rapor sayfalarını doldurmak için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="5c4ad-173">The following data is used to fill the report pages in the **Purchase spend analysis** Power BI content.</span></span> <span data-ttu-id="5c4ad-174">Bu veri, Varlık mağazasında hazırlanan toplam ölçümler olarak sunulur.</span><span class="sxs-lookup"><span data-stu-id="5c4ad-174">This data is represented as aggregate measurements that are staged in the Entity store.</span></span> <span data-ttu-id="5c4ad-175">Varlık mağazası, analizler için en iyi duruma getirilmiş bir Microsoft SQL Server veritabanıdır.</span><span class="sxs-lookup"><span data-stu-id="5c4ad-175">The Entity store is a Microsoft SQL Server database that is optimized for analytics.</span></span> <span data-ttu-id="5c4ad-176">Daha fazla bilgi için, bkz. [Varlık mağazası ile Power BI tümleştirmesi](power-bi-integration-entity-store.md).</span><span class="sxs-lookup"><span data-stu-id="5c4ad-176">For more information, see [Power BI integration with Entity store](power-bi-integration-entity-store.md).</span></span>

<span data-ttu-id="5c4ad-177">Bu içerik paketindeki toplama ölçümler, Microsoft Dynamics AX 2012 ve Microsoft Dynamics AX 2012 R3'teki Satınalma Küpü'nde bulunan toplama ölçümlerin alt kümesidir.</span><span class="sxs-lookup"><span data-stu-id="5c4ad-177">The aggregate measurements in this content are the subset of aggregate measurements that were available in the Purchase Cube in Microsoft Dynamics AX 2012 and Microsoft Dynamics AX 2012 R3.</span></span> <span data-ttu-id="5c4ad-178">Varlık deposundaki küpün toplama ölçülerini hazırlamak için bu ölçümleri dağıtılabilir yapmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="5c4ad-178">To stage the cube's aggregate measurements in the Entity store, you must make them deployable.</span></span> <span data-ttu-id="5c4ad-179">Daha fazla bilgi için [Power BI ile Varlık deposu tümleştirmesi](power-bi-integration-entity-store.md) bölümündeki toplanan ölçümleri Varlık Deposuna ekleme prosedürüne bakın.</span><span class="sxs-lookup"><span data-stu-id="5c4ad-179">For more information, see the procedure for staging aggregate measurements in the Entity store in [Power BI integration with Entity store](power-bi-integration-entity-store.md).</span></span> <span data-ttu-id="5c4ad-180">Aşağıda verilen önemli toplanan ölçümleri doğrudan Fatura satırları varlığından kullanılabilir ve içeriğin temeli olarak kullanılır.</span><span class="sxs-lookup"><span data-stu-id="5c4ad-180">The following key aggregate measurements are available directly from the Invoice lines entity and are used as the basis of the content.</span></span>

| <span data-ttu-id="5c4ad-181">Varlık</span><span class="sxs-lookup"><span data-stu-id="5c4ad-181">Entity</span></span>        | <span data-ttu-id="5c4ad-182">Önemli toplam ölçümler</span><span class="sxs-lookup"><span data-stu-id="5c4ad-182">Key aggregate measurements</span></span> | <span data-ttu-id="5c4ad-183">Veri kaynağı</span><span class="sxs-lookup"><span data-stu-id="5c4ad-183">Data source</span></span>                                 | <span data-ttu-id="5c4ad-184">Alan</span><span class="sxs-lookup"><span data-stu-id="5c4ad-184">Field</span></span>              | <span data-ttu-id="5c4ad-185">Açıklama</span><span class="sxs-lookup"><span data-stu-id="5c4ad-185">Description</span></span>                            |
|---------------|----------------------------|---------------------------------------------|--------------------|----------------------------------------|
| <span data-ttu-id="5c4ad-186">Fatura satırları</span><span class="sxs-lookup"><span data-stu-id="5c4ad-186">Invoice lines</span></span> | <span data-ttu-id="5c4ad-187">Satınalma</span><span class="sxs-lookup"><span data-stu-id="5c4ad-187">Purchase</span></span>                   | <span data-ttu-id="5c4ad-188">VendInvoiceTrans</span><span class="sxs-lookup"><span data-stu-id="5c4ad-188">VendInvoiceTrans</span></span>                            | <span data-ttu-id="5c4ad-189">SUM(LineAmountMST)</span><span class="sxs-lookup"><span data-stu-id="5c4ad-189">SUM(LineAmountMST)</span></span> | <span data-ttu-id="5c4ad-190">Muhasebe para birimi cinsinden tutar.</span><span class="sxs-lookup"><span data-stu-id="5c4ad-190">The amount in the accounting currency.</span></span> |

<span data-ttu-id="5c4ad-191">Aşağıdaki tablo içerikte Fatura satırları varlığından hesaplanan anahtar ölçümleri gösterir.</span><span class="sxs-lookup"><span data-stu-id="5c4ad-191">The following table shows the key measurements in the content that are calculated from the Invoice lines entity.</span></span>

| <span data-ttu-id="5c4ad-192">Ölçü</span><span class="sxs-lookup"><span data-stu-id="5c4ad-192">Measure</span></span>               | <span data-ttu-id="5c4ad-193">Hesaplama</span><span class="sxs-lookup"><span data-stu-id="5c4ad-193">Calculation</span></span>                                                                                         |
|-----------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5c4ad-194">Geçerli yıldaki satınalma</span><span class="sxs-lookup"><span data-stu-id="5c4ad-194">Purchase current year</span></span> | <span data-ttu-id="5c4ad-195">Geçerli yıldaki satınalma = TOPLA('Fatura satırları'\[Satınalma\])</span><span class="sxs-lookup"><span data-stu-id="5c4ad-195">Purchase current year = SUM('Invoice lines'\[Purchase\])</span></span>                                            |
| <span data-ttu-id="5c4ad-196">Geçen yılki satınalma</span><span class="sxs-lookup"><span data-stu-id="5c4ad-196">Purchase last year</span></span>    | <span data-ttu-id="5c4ad-197">Geçen yılki satınalma = HESAPLA(TOPLA('Fatura satırları'\[Satınalma\]), SAMEPERIODLASTYEAR (Tarihler\[Tarih\]))</span><span class="sxs-lookup"><span data-stu-id="5c4ad-197">Purchase last year = CALCULATE(SUM('Invoice lines'\[Purchase\]), SAMEPERIODLASTYEAR(Dates\[Date\]))</span></span> |
| <span data-ttu-id="5c4ad-198">Yıllara göre satınalmadaki büyüme</span><span class="sxs-lookup"><span data-stu-id="5c4ad-198">YOY purchase growth</span></span>   | <span data-ttu-id="5c4ad-199">Yıllara göre satınalmadaki büyüme = \[Geçerli yıldaki satınalma\]: \[Geçen yıldaki satınalma\]</span><span class="sxs-lookup"><span data-stu-id="5c4ad-199">YOY purchase growth = \[Purchase current year\] – \[Purchase last year\]</span></span>                            |

<span data-ttu-id="5c4ad-200">İçerikte bulunan aşağıdaki temel boyutları, daha büyük hassasiyet ve daha derin analiz bilgileri elde edebilmeniz amacıyla toplama ölçümlerini bölmek üzere filtre olarak kullanılır.</span><span class="sxs-lookup"><span data-stu-id="5c4ad-200">The following key dimensions in the content are used as filters to slice the aggregate measurements, so that you can achieve more granularity and gain deeper analytical insights.</span></span>

| <span data-ttu-id="5c4ad-201">Varlık</span><span class="sxs-lookup"><span data-stu-id="5c4ad-201">Entity</span></span>                 | <span data-ttu-id="5c4ad-202">Öznitelik örnekleri</span><span class="sxs-lookup"><span data-stu-id="5c4ad-202">Examples of attributes</span></span>                                |
|------------------------|-------------------------------------------------------|
| <span data-ttu-id="5c4ad-203">Satıcılar</span><span class="sxs-lookup"><span data-stu-id="5c4ad-203">Vendors</span></span>                | <span data-ttu-id="5c4ad-204">Satıcı grupları, Satıcı ülkesi veya bölgeleri, Satıcı adı</span><span class="sxs-lookup"><span data-stu-id="5c4ad-204">Vendor groups, Vendor country or regions, Vendor name</span></span> |
| <span data-ttu-id="5c4ad-205">Ürünler</span><span class="sxs-lookup"><span data-stu-id="5c4ad-205">Products</span></span>               | <span data-ttu-id="5c4ad-206">Ürün numarası, Ürün adı, Madde grupları adı</span><span class="sxs-lookup"><span data-stu-id="5c4ad-206">Product number, Product name, Item groups name</span></span>        |
| <span data-ttu-id="5c4ad-207">Tedarik kategorileri</span><span class="sxs-lookup"><span data-stu-id="5c4ad-207">Procurement categories</span></span> | <span data-ttu-id="5c4ad-208">Tedarik kategorisi, Tedarik kategorisi adları</span><span class="sxs-lookup"><span data-stu-id="5c4ad-208">Procurement category, Procurement category names</span></span>      |
| <span data-ttu-id="5c4ad-209">Tüzel kişilikler</span><span class="sxs-lookup"><span data-stu-id="5c4ad-209">Legal entities</span></span>         | <span data-ttu-id="5c4ad-210">Tüzel kişiliğin adı</span><span class="sxs-lookup"><span data-stu-id="5c4ad-210">Legal entity name</span></span>                                     |
| <span data-ttu-id="5c4ad-211">Tarihler</span><span class="sxs-lookup"><span data-stu-id="5c4ad-211">Dates</span></span>                  | <span data-ttu-id="5c4ad-212">Tarihler, Yıl denkleştirme</span><span class="sxs-lookup"><span data-stu-id="5c4ad-212">Dates, Year offset</span></span>                                    |

<span data-ttu-id="5c4ad-213">Varsayılan olarak, içerik geçerli takvim yılına ilişkin verileri gösterir.</span><span class="sxs-lookup"><span data-stu-id="5c4ad-213">By default, the content shows data for the current calendar year.</span></span> <span data-ttu-id="5c4ad-214">Ancak, rapor filtreleri bölümünden tarih filtresini değiştirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="5c4ad-214">However, you can change the date filter in the report filters section.</span></span> <span data-ttu-id="5c4ad-215">Şirket filtresini de değiştirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="5c4ad-215">You can also change the company filter.</span></span>
