---
title: Satınalma ve harcama analizi Power BI içeriği
description: Bu konu, Power BI Satınalma harcaması analizinde nelerin bulunduğunu açıklar. Bu ayrıca, içeriğe dahil edilen raporların nasıl kullanılacağını açıklar ve içeriği oluşturmakta kullanılan veri modeli ve varlıklar hakkında bilgi sağlar.
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
ms.search.scope: Core, Operations
ms.custom: 265434
ms.assetid: 3cd9dfce-2687-4303-bc78-349e7cb5ea75
ms.search.region: global
ms.author: fdahl
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: d25bacc2ec1f8e13376b96e188b099a184f7f8c6
ms.sourcegitcommit: d37fb09101c30858bcb975931b3d8f947d72017b
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/10/2019
ms.locfileid: "2569144"
---
# <a name="purchase-spend-analysis-power-bi-content"></a><span data-ttu-id="f6afc-104">Satınalma ve harcama analizi Power BI içeriği</span><span class="sxs-lookup"><span data-stu-id="f6afc-104">Purchase spend analysis Power BI content</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f6afc-105">Bu konu, Microsoft Power BI **Satınalma harcaması analizinde** nelerin bulunduğunu açıklar.</span><span class="sxs-lookup"><span data-stu-id="f6afc-105">This topic describes what is included in the **Purchase spend analysis** Microsoft Power BI content.</span></span> <span data-ttu-id="f6afc-106">Bu Power BI raporlarına nasıl erişileceğini açıklar ve içeriği oluşturmakta kullanılmış olan veri modeli ve varlıklar hakkında bilgi sağlar.</span><span class="sxs-lookup"><span data-stu-id="f6afc-106">It explains how to access the Power BI reports, and provides information about the data model and entities that are used to build the content.</span></span>

## <a name="overview"></a><span data-ttu-id="f6afc-107">Genel bakış</span><span class="sxs-lookup"><span data-stu-id="f6afc-107">Overview</span></span>

<span data-ttu-id="f6afc-108">**Satınalma harcaması analizi** Power BI içeriği satınalma yöneticilerine ve bütçelerden sorumlu yöneticilere satınalma harcamalarını izleme konusunda yardımcı olmak üzere tasarlanmıştır.</span><span class="sxs-lookup"><span data-stu-id="f6afc-108">The **Purchase spend analysis** Power BI content was designed to help purchasing managers and managers who are responsible for budgets keep track of purchase spending.</span></span> <span data-ttu-id="f6afc-109">Yöneticiler satınalma harcamasını aşağıdaki şekillerde analiz edebilirler:</span><span class="sxs-lookup"><span data-stu-id="f6afc-109">Managers can analyze purchase spending in the following ways:</span></span>

- <span data-ttu-id="f6afc-110">Yılbaşından bugüne satınalma (satıcı grubu ve tek tek satıcılara, tedarik kategorisine ve bireysel ürünlere ve satıcı konumuna göre)</span><span class="sxs-lookup"><span data-stu-id="f6afc-110">Year-to-date purchase (by vendor group and individual vendors, procurement category and individual products, and vendor location)</span></span>
- <span data-ttu-id="f6afc-111">Yıldan yıla satınalma değişikliği (satıcı grubu ve tedarik kategorisine göre)</span><span class="sxs-lookup"><span data-stu-id="f6afc-111">Year-over-year purchase change (by vendor group and procurement category)</span></span>

<span data-ttu-id="f6afc-112">İçerik, alınan satınalma hareketi verilerini kullanır ve hem şirket çapında satınalma rakamlarının toplam görünümünü hem de satıcı ve ürünler için satınalma harcamasının dağılımını verir.</span><span class="sxs-lookup"><span data-stu-id="f6afc-112">The content uses purchase transactional data, and provides both an aggregate view of the company-wide purchase figures and a breakdown of purchase spending by vendor and product.</span></span> <span data-ttu-id="f6afc-113">Raporlar satınalma harcamalarında zaman içindeki değişiklikleri öne çıkarır.</span><span class="sxs-lookup"><span data-stu-id="f6afc-113">Reports highlight changes in purchase spending over time.</span></span> <span data-ttu-id="f6afc-114">Bu nedenle, raporlar yöneticileri ayrı satıcılar ve ürünlerle ilgili olarak pozitif ve negatif harcama eğilimleri hakkında uyarmak için kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="f6afc-114">Therefore, the reports can be used to alert managers about positive and negative spending trends for individual vendors and products.</span></span> <span data-ttu-id="f6afc-115">Ek olarak grafikler farklı tedarik kategorileri ve satıcı grupları için satınalma harcamasını gösterir.</span><span class="sxs-lookup"><span data-stu-id="f6afc-115">Additionally, charts show purchase spending for different procurement categories and vendor groups.</span></span> <span data-ttu-id="f6afc-116">Bu nedenle, kategori ve bölgesel yöneticiler, harcama davranışındaki değişiklikleri tanımlamaya yardımcı olması açısından bu grafikleri kullanabilirler.</span><span class="sxs-lookup"><span data-stu-id="f6afc-116">Therefore, category and regional managers can use the charts to help identify changes in spending behavior.</span></span>

## <a name="accessing-the-power-bi-content"></a><span data-ttu-id="f6afc-117">Power BI içeriğine erişim</span><span class="sxs-lookup"><span data-stu-id="f6afc-117">Accessing the Power BI content</span></span>
<span data-ttu-id="f6afc-118">**Satınalma ve harcama analizi** Power BI içeriği **Satın alma ve harcama analizi** sayfasında gösterilir (**Tedarik ve kaynak atama** \> **Sorgular ve raporlar** \> **Satın alma performansı analizi** \> **Satın alma ve harcama analizi**).</span><span class="sxs-lookup"><span data-stu-id="f6afc-118">The **Purchase spend analysis** Power BI content is shown on the **Purchase and spend analysis** page (**Procurement and sourcing** \> **Inquiries and reports** \> **Purchase performance analysis** \> **Purchase and spend analysis**).</span></span>

## <a name="metrics-that-are-included-in-the-power-bi-content"></a><span data-ttu-id="f6afc-119">Power BI içerik paketinde bulunan ölçümler</span><span class="sxs-lookup"><span data-stu-id="f6afc-119">Metrics that are included in the Power BI content</span></span>
<span data-ttu-id="f6afc-120">**Satın alma harcaması analizi** Power BI içeriği bir dizi ölçümden oluşan bir rapor içerir.</span><span class="sxs-lookup"><span data-stu-id="f6afc-120">The **Purchase spend analysis** Power BI content includes a report that consists of a set of metrics.</span></span> <span data-ttu-id="f6afc-121">Bu ölçümler grafikler, kutucuklar ve tablolar şeklinde görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="f6afc-121">These metrics are visualized as charts, tiles, and tables.</span></span> 

<span data-ttu-id="f6afc-122">Aşağıdaki bölümde, görsellere yönelik genel bakış sunulur.</span><span class="sxs-lookup"><span data-stu-id="f6afc-122">The following sections provide an overview of the visualizations.</span></span>

### <a name="purchase-by-vendor-report-page"></a><span data-ttu-id="f6afc-123">Satıcı bazında satınalma rapor sayfası</span><span class="sxs-lookup"><span data-stu-id="f6afc-123">Purchase by vendor report page</span></span>
<span data-ttu-id="f6afc-124">**Grafikler**</span><span class="sxs-lookup"><span data-stu-id="f6afc-124">**Charts**</span></span>
- <span data-ttu-id="f6afc-125">Satınalmaya göre en iyi 10 satıcı (yığılmış çubuk grafik)</span><span class="sxs-lookup"><span data-stu-id="f6afc-125">Top 10 vendors by purchase (stacked bar chart)</span></span>
- <span data-ttu-id="f6afc-126">Satıcı grubuna / ülkeye / ada göre toplam satınalma (pasta grafik)</span><span class="sxs-lookup"><span data-stu-id="f6afc-126">Total purchase by vendor group / country / name (pie chart)</span></span>
- <span data-ttu-id="f6afc-127">Satıcı grubuna / ülkeye / ada göre satınalma (sütun grafik)</span><span class="sxs-lookup"><span data-stu-id="f6afc-127">Purchase by vendor group / country / name (column chart)</span></span>
- <span data-ttu-id="f6afc-128">Satıcı grubuna / ülkeye / ada göre ortalama satınalma (sütun grafik)</span><span class="sxs-lookup"><span data-stu-id="f6afc-128">Average purchase by vendor group / country / name (column chart)</span></span>

<span data-ttu-id="f6afc-129">**Kutucuklar**</span><span class="sxs-lookup"><span data-stu-id="f6afc-129">**Tiles**</span></span>
- <span data-ttu-id="f6afc-130">Satınalma toplamı</span><span class="sxs-lookup"><span data-stu-id="f6afc-130">Total purchase</span></span>
- <span data-ttu-id="f6afc-131">Yıllara göre satınalmadaki büyüme</span><span class="sxs-lookup"><span data-stu-id="f6afc-131">YOY purchase growth</span></span>
- <span data-ttu-id="f6afc-132">Toplam satıcı sayısı</span><span class="sxs-lookup"><span data-stu-id="f6afc-132">Total # vendors</span></span>
- <span data-ttu-id="f6afc-133">Toplam etkin satıcı sayısı</span><span class="sxs-lookup"><span data-stu-id="f6afc-133">Total # of active vendors</span></span>

<span data-ttu-id="f6afc-134">**Örnek**</span><span class="sxs-lookup"><span data-stu-id="f6afc-134">**Example**</span></span>
<img src="media/spend1.png" alt="Purchase by vendor">

### <a name="purchase-by-product-report-page"></a><span data-ttu-id="f6afc-135">Ürün bazında satınalma rapor sayfası</span><span class="sxs-lookup"><span data-stu-id="f6afc-135">Purchase by product report page</span></span>

<span data-ttu-id="f6afc-136">**Grafikler**</span><span class="sxs-lookup"><span data-stu-id="f6afc-136">**Charts**</span></span>
- <span data-ttu-id="f6afc-137">Tedarik kategorisine / ürün adına göre satınalma (sütun grafiği)</span><span class="sxs-lookup"><span data-stu-id="f6afc-137">Purchase by procurement category / product name (column chart)</span></span>
- <span data-ttu-id="f6afc-138">Tedarik kategorisine / ürün adına göre toplam satınalma (pasta grafik)</span><span class="sxs-lookup"><span data-stu-id="f6afc-138">Total purchase by procurement category / product name (pie chart)</span></span>
- <span data-ttu-id="f6afc-139">Satınalmaya göre en iyi 10 ürün (yığılmış çubuk grafik)</span><span class="sxs-lookup"><span data-stu-id="f6afc-139">Top 10 products by purchase (stacked bar chart)</span></span>

<span data-ttu-id="f6afc-140">**Kutucuklar**</span><span class="sxs-lookup"><span data-stu-id="f6afc-140">**Tiles**</span></span>
- <span data-ttu-id="f6afc-141">Toplam ürün sayısı</span><span class="sxs-lookup"><span data-stu-id="f6afc-141">Total # of products</span></span></li>
- <span data-ttu-id="f6afc-142">Etkin ürünlerin toplam sayısının toplam etkin ürünlere yüzdesi</span><span class="sxs-lookup"><span data-stu-id="f6afc-142">Total active products percentage of total # of products</span></span>
- <span data-ttu-id="f6afc-143">Satınalmanın %80'ini oluşturan ürünlerin sayısı</span><span class="sxs-lookup"><span data-stu-id="f6afc-143">Number of products accounting for 80% purchase</span></span>

<span data-ttu-id="f6afc-144">**Örnek**</span><span class="sxs-lookup"><span data-stu-id="f6afc-144">**Example**</span></span>


<img src="media/purchaseByProduct.png" alt="Purchase by Product">

### <a name="purchase-by-period-report-page"></a><span data-ttu-id="f6afc-145">Dönem bazında satınalma rapor sayfası</span><span class="sxs-lookup"><span data-stu-id="f6afc-145">Purchase by period report page</span></span>
<span data-ttu-id="f6afc-146">Bu sayfa bu yılki ve geçen yılki satınalmayı ve tedarik kategorisine göre büyümeyi gösterir.</span><span class="sxs-lookup"><span data-stu-id="f6afc-146">This page shows purchases this year and last year, and growth by procurement category.</span></span>

<span data-ttu-id="f6afc-147">**Grafikler**</span><span class="sxs-lookup"><span data-stu-id="f6afc-147">**Charts**</span></span> 
- <span data-ttu-id="f6afc-148">Aya / güne göre satınalma (sütun grafiği)</span><span class="sxs-lookup"><span data-stu-id="f6afc-148">Purchase by month / day (column chart)</span></span>
- <span data-ttu-id="f6afc-149">Toplam satınalmanın yıllara görefarkı (şelale grafik)</span><span class="sxs-lookup"><span data-stu-id="f6afc-149">Cumulative purchase YOY variance (waterfall chart)</span></span>
- <span data-ttu-id="f6afc-150">Toplam satınalmada yıllara göre büyüme (sütun grafik)</span><span class="sxs-lookup"><span data-stu-id="f6afc-150">Total purchase YOY growth (column chart)</span></span>
- <span data-ttu-id="f6afc-151">Tedarik ekstresi (matriks)</span><span class="sxs-lookup"><span data-stu-id="f6afc-151">Procurement statement (matrix)</span></span>

<span data-ttu-id="f6afc-152">**Kutucuklar**</span><span class="sxs-lookup"><span data-stu-id="f6afc-152">**Tiles**</span></span>
- <span data-ttu-id="f6afc-153">Yıllara göre satınalmadaki büyüme</span><span class="sxs-lookup"><span data-stu-id="f6afc-153">YOY purchase growth</span></span>
- <span data-ttu-id="f6afc-154">Yıllara göre satınalmadaki büyüme yüzdesi</span><span class="sxs-lookup"><span data-stu-id="f6afc-154">YOY purchase growth %</span></span>

<span data-ttu-id="f6afc-155">**Örnek**</span><span class="sxs-lookup"><span data-stu-id="f6afc-155">**Example**</span></span>
<img src="media/purchaseByPeriod.png" alt="Purchase by Period">

### <a name="purchase-by-vendor-location-report-page"></a><span data-ttu-id="f6afc-156">Satıcı konumu bazında satınalma rapor sayfası</span><span class="sxs-lookup"><span data-stu-id="f6afc-156">Purchase by vendor location report page</span></span>

<span data-ttu-id="f6afc-157">**Grafikler**</span><span class="sxs-lookup"><span data-stu-id="f6afc-157">**Charts**</span></span>
- <span data-ttu-id="f6afc-158">Şehre göre satınalma</span><span class="sxs-lookup"><span data-stu-id="f6afc-158">Purchase by city</span></span>
- <span data-ttu-id="f6afc-159">Satınalmada yıldan yıla büyüme yüzdesi</span><span class="sxs-lookup"><span data-stu-id="f6afc-159">Purchase YOY growth %</span></span>
- <span data-ttu-id="f6afc-160">Ülkeye göre satınalma</span><span class="sxs-lookup"><span data-stu-id="f6afc-160">Purchase by country</span></span>

<span data-ttu-id="f6afc-161">**Örnek**</span><span class="sxs-lookup"><span data-stu-id="f6afc-161">**Example**</span></span>
<img src="media/purchByVendorLocation.png" alt="Purchase by Vendor Location">

### <a name="purchase-spend-analysis-by-time-report-page"></a><span data-ttu-id="f6afc-162">Zamana göre satınalma harcaması analizi rapor sayfası</span><span class="sxs-lookup"><span data-stu-id="f6afc-162">Purchase spend analysis by time report page</span></span>

<span data-ttu-id="f6afc-163">**Grafikler**</span><span class="sxs-lookup"><span data-stu-id="f6afc-163">**Charts**</span></span> 
- <span data-ttu-id="f6afc-164">Aya / güne göre geçerli yıldaki satın alma (çizgi grafiği)</span><span class="sxs-lookup"><span data-stu-id="f6afc-164">Purchase current year by month / day (line chart)</span></span>
- <span data-ttu-id="f6afc-165">Geçerli yıl ve önceki yıldaki satınalma (satır ve sütun grafiği)</span><span class="sxs-lookup"><span data-stu-id="f6afc-165">Purchase current and last year (line and column chart)</span></span>

<span data-ttu-id="f6afc-166">**Örnek**</span><span class="sxs-lookup"><span data-stu-id="f6afc-166">**Example**</span></span>
<img src="media/PurchByTIme.png" alt="Purchase by Time">

### <a name="purchase-spend-analysis-by-vendor-report-page"></a><span data-ttu-id="f6afc-167">Satıcıya göre satınalma harcaması analizi rapor sayfası</span><span class="sxs-lookup"><span data-stu-id="f6afc-167">Purchase spend analysis by vendor report page</span></span>

<span data-ttu-id="f6afc-168">**Grafikler**</span><span class="sxs-lookup"><span data-stu-id="f6afc-168">**Charts**</span></span> 
- <span data-ttu-id="f6afc-169">İlk 10 satıcı satınalmanın satınalmaya göre yüzdesi (huni)</span><span class="sxs-lookup"><span data-stu-id="f6afc-169">Top 10 vendor purchase % of purchase (funnel)</span></span>
- <span data-ttu-id="f6afc-170">Yıllara göre artan harcamayla en iyi 10 satıcı</span><span class="sxs-lookup"><span data-stu-id="f6afc-170">Top 10 vendors with increased spending YOY</span></span>
- <span data-ttu-id="f6afc-171">Yıllara göre azalan harcamayla en iyi 10 satıcı</span><span class="sxs-lookup"><span data-stu-id="f6afc-171">Top 10 vendors with decreased spending YOY</span></span>

<span data-ttu-id="f6afc-172">**Örnek** 
</span><span class="sxs-lookup"><span data-stu-id="f6afc-172">**Example** 
</span></span><img src="media/PurchSpendAnalysisByVendor.png" alt="Purchase spend by vendor">


## <a name="data-model-and-entities"></a><span data-ttu-id="f6afc-173">Veri modeli ve varlıklar</span><span class="sxs-lookup"><span data-stu-id="f6afc-173">Data model and entities</span></span>
<span data-ttu-id="f6afc-174">Aşağıdaki veriler **Satınalma harcaması analizi** Power BI içeriğindeki rapor sayfalarını doldurmak için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="f6afc-174">The following data is used to fill the report pages in the **Purchase spend analysis** Power BI content.</span></span> <span data-ttu-id="f6afc-175">Bu veri, Varlık mağazasında hazırlanan toplam ölçümler olarak sunulur.</span><span class="sxs-lookup"><span data-stu-id="f6afc-175">This data is represented as aggregate measurements that are staged in the Entity store.</span></span> <span data-ttu-id="f6afc-176">Varlık mağazası, analizler için en iyi duruma getirilmiş bir Microsoft SQL Server veritabanıdır.</span><span class="sxs-lookup"><span data-stu-id="f6afc-176">The Entity store is a Microsoft SQL Server database that is optimized for analytics.</span></span> <span data-ttu-id="f6afc-177">Daha fazla bilgi için, bkz. [Varlık mağazası ile Power BI tümleştirmesine genel bakış](power-bi-integration-entity-store.md).</span><span class="sxs-lookup"><span data-stu-id="f6afc-177">For more information, see [Overview of Power BI integration with Entity store](power-bi-integration-entity-store.md).</span></span>

<span data-ttu-id="f6afc-178">Bu içerik paketindeki toplama ölçümler, Microsoft Dynamics AX 2012 ve Microsoft Dynamics AX 2012 R3'teki Satınalma Küpü'nde bulunan toplama ölçümlerin alt kümesidir.</span><span class="sxs-lookup"><span data-stu-id="f6afc-178">The aggregate measurements in this content are the subset of aggregate measurements that were available in the Purchase Cube in Microsoft Dynamics AX 2012 and Microsoft Dynamics AX 2012 R3.</span></span> <span data-ttu-id="f6afc-179">Varlık deposundaki küpün toplama ölçülerini hazırlamak için bu ölçümleri dağıtılabilir yapmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="f6afc-179">To stage the cube's aggregate measurements in the Entity store, you must make them deployable.</span></span> <span data-ttu-id="f6afc-180">Daha fazla bilgi için, [Power BI ile Varlık deposu tümleştirmesine genel bakış bölümündeki toplanan ölçümleri Varlık Deposuna ekleme yordamına](power-bi-integration-entity-store.md) bakın.</span><span class="sxs-lookup"><span data-stu-id="f6afc-180">For more information, see the procedure for staging aggregate measurements in the Entity store in [Overview of Power BI integration with Entity store](power-bi-integration-entity-store.md).</span></span> <span data-ttu-id="f6afc-181">Aşağıda verilen önemli toplanan ölçümleri doğrudan Fatura satırları varlığından kullanılabilir ve içeriğin temeli olarak kullanılır.</span><span class="sxs-lookup"><span data-stu-id="f6afc-181">The following key aggregate measurements are available directly from the Invoice lines entity and are used as the basis of the content.</span></span>

| <span data-ttu-id="f6afc-182">Varlık</span><span class="sxs-lookup"><span data-stu-id="f6afc-182">Entity</span></span>        | <span data-ttu-id="f6afc-183">Önemli toplam ölçümler</span><span class="sxs-lookup"><span data-stu-id="f6afc-183">Key aggregate measurements</span></span> | <span data-ttu-id="f6afc-184">Veri kaynağı</span><span class="sxs-lookup"><span data-stu-id="f6afc-184">Data source</span></span>                                 | <span data-ttu-id="f6afc-185">Alan</span><span class="sxs-lookup"><span data-stu-id="f6afc-185">Field</span></span>              | <span data-ttu-id="f6afc-186">Açıklama</span><span class="sxs-lookup"><span data-stu-id="f6afc-186">Description</span></span>                            |
|---------------|----------------------------|---------------------------------------------|--------------------|----------------------------------------|
| <span data-ttu-id="f6afc-187">Fatura satırları</span><span class="sxs-lookup"><span data-stu-id="f6afc-187">Invoice lines</span></span> | <span data-ttu-id="f6afc-188">Satınalma</span><span class="sxs-lookup"><span data-stu-id="f6afc-188">Purchase</span></span>                   | <span data-ttu-id="f6afc-189">VendInvoiceTrans</span><span class="sxs-lookup"><span data-stu-id="f6afc-189">VendInvoiceTrans</span></span>                            | <span data-ttu-id="f6afc-190">SUM(LineAmountMST)</span><span class="sxs-lookup"><span data-stu-id="f6afc-190">SUM(LineAmountMST)</span></span> | <span data-ttu-id="f6afc-191">Muhasebe para birimi cinsinden tutar.</span><span class="sxs-lookup"><span data-stu-id="f6afc-191">The amount in the accounting currency.</span></span> |

<span data-ttu-id="f6afc-192">Aşağıdaki tablo içerikte Fatura satırları varlığından hesaplanan anahtar ölçümleri gösterir.</span><span class="sxs-lookup"><span data-stu-id="f6afc-192">The following table shows the key measurements in the content that are calculated from the Invoice lines entity.</span></span>

| <span data-ttu-id="f6afc-193">Ölçü</span><span class="sxs-lookup"><span data-stu-id="f6afc-193">Measure</span></span>               | <span data-ttu-id="f6afc-194">Hesaplama</span><span class="sxs-lookup"><span data-stu-id="f6afc-194">Calculation</span></span>                                                                                         |
|-----------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f6afc-195">Geçerli yıldaki satınalma</span><span class="sxs-lookup"><span data-stu-id="f6afc-195">Purchase current year</span></span> | <span data-ttu-id="f6afc-196">Geçerli yıldaki satınalma = TOPLA('Fatura satırları'\[Satınalma\])</span><span class="sxs-lookup"><span data-stu-id="f6afc-196">Purchase current year = SUM('Invoice lines'\[Purchase\])</span></span>                                            |
| <span data-ttu-id="f6afc-197">Geçen yılki satınalma</span><span class="sxs-lookup"><span data-stu-id="f6afc-197">Purchase last year</span></span>    | <span data-ttu-id="f6afc-198">Geçen yılki satınalma = HESAPLA(TOPLA('Fatura satırları'\[Satınalma\]), SAMEPERIODLASTYEAR (Tarihler\[Tarih\])</span><span class="sxs-lookup"><span data-stu-id="f6afc-198">Purchase last year = CALCULATE(SUM('Invoice lines'\[Purchase\]), SAMEPERIODLASTYEAR(Dates\[Date\]))</span></span> |
| <span data-ttu-id="f6afc-199">Yıllara göre satınalmadaki büyüme</span><span class="sxs-lookup"><span data-stu-id="f6afc-199">YOY purchase growth</span></span>   | <span data-ttu-id="f6afc-200">Yıllara göre satınalmadaki büyüme = \[Geçerli yıldaki satınalma\]: \[Geçen yıldaki satınalma\]</span><span class="sxs-lookup"><span data-stu-id="f6afc-200">YOY purchase growth = \[Purchase current year\] – \[Purchase last year\]</span></span>                            |

<span data-ttu-id="f6afc-201">İçerikte bulunan aşağıdaki temel boyutları, daha büyük hassasiyet ve daha derin analiz bilgileri elde edebilmeniz amacıyla toplama ölçümlerini bölmek üzere filtre olarak kullanılır.</span><span class="sxs-lookup"><span data-stu-id="f6afc-201">The following key dimensions in the content are used as filters to slice the aggregate measurements, so that you can achieve more granularity and gain deeper analytical insights.</span></span>

| <span data-ttu-id="f6afc-202">Varlık</span><span class="sxs-lookup"><span data-stu-id="f6afc-202">Entity</span></span>                 | <span data-ttu-id="f6afc-203">Öznitelik örnekleri</span><span class="sxs-lookup"><span data-stu-id="f6afc-203">Examples of attributes</span></span>                                |
|------------------------|-------------------------------------------------------|
| <span data-ttu-id="f6afc-204">Satıcılar</span><span class="sxs-lookup"><span data-stu-id="f6afc-204">Vendors</span></span>                | <span data-ttu-id="f6afc-205">Satıcı grupları, Satıcı ülkesi veya bölgeleri, Satıcı adı</span><span class="sxs-lookup"><span data-stu-id="f6afc-205">Vendor groups, Vendor country or regions, Vendor name</span></span> |
| <span data-ttu-id="f6afc-206">Ürünler</span><span class="sxs-lookup"><span data-stu-id="f6afc-206">Products</span></span>               | <span data-ttu-id="f6afc-207">Ürün numarası, Ürün adı, Madde grupları adı</span><span class="sxs-lookup"><span data-stu-id="f6afc-207">Product number, Product name, Item groups name</span></span>        |
| <span data-ttu-id="f6afc-208">Tedarik kategorileri</span><span class="sxs-lookup"><span data-stu-id="f6afc-208">Procurement categories</span></span> | <span data-ttu-id="f6afc-209">Tedarik kategorisi, Tedarik kategorisi adları</span><span class="sxs-lookup"><span data-stu-id="f6afc-209">Procurement category, Procurement category names</span></span>      |
| <span data-ttu-id="f6afc-210">Tüzel kişilikler</span><span class="sxs-lookup"><span data-stu-id="f6afc-210">Legal entities</span></span>         | <span data-ttu-id="f6afc-211">Tüzel kişiliğin adı</span><span class="sxs-lookup"><span data-stu-id="f6afc-211">Legal entity name</span></span>                                     |
| <span data-ttu-id="f6afc-212">Tarihler</span><span class="sxs-lookup"><span data-stu-id="f6afc-212">Dates</span></span>                  | <span data-ttu-id="f6afc-213">Tarihler, Yıl denkleştirme</span><span class="sxs-lookup"><span data-stu-id="f6afc-213">Dates, Year offset</span></span>                                    |

<span data-ttu-id="f6afc-214">Varsayılan olarak, içerik geçerli takvim yılına ilişkin verileri gösterir.</span><span class="sxs-lookup"><span data-stu-id="f6afc-214">By default, the content shows data for the current calendar year.</span></span> <span data-ttu-id="f6afc-215">Ancak, rapor filtreleri bölümünden tarih filtresini değiştirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="f6afc-215">However, you can change the date filter in the report filters section.</span></span> <span data-ttu-id="f6afc-216">Şirket filtresini de değiştirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="f6afc-216">You can also change the company filter.</span></span>
