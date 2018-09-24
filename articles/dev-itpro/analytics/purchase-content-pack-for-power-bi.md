---
title: "Satınalma harcaması analizi Power BI içeriği"
description: "Bu konu, Power BI Satınalma harcaması analizinde nelerin bulunduğunu açıklar. Bu ayrıca, içeriğe dahil edilen raporların nasıl kullanılacağını açıklar ve içeriği oluşturmakta kullanılan veri modeli ve varlıklar hakkında bilgi sağlar."
author: FrankDahl
manager: AnnBe
ms.date: 12/18/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
ms.search.form: PurchaseSpendAnalysisPowerBI
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 265434
ms.assetid: 3cd9dfce-2687-4303-bc78-349e7cb5ea75
ms.search.region: global
ms.author: fdahl
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: 821d8927211d7ac3e479848c7e7bef9f650d4340
ms.openlocfilehash: 069c4dc21959ab603ba6ca3da0ac68ef20325265
ms.contentlocale: tr-tr
ms.lasthandoff: 08/13/2018

---

# <a name="purchase-spend-analysis-power-bi-content"></a><span data-ttu-id="f7021-104">Satınalma harcaması analizi Power BI içeriği</span><span class="sxs-lookup"><span data-stu-id="f7021-104">Purchase spend analysis Power BI content</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f7021-105">Bu konu, Power BI **Satınalma harcaması** analizinde nelerin bulunduğunu açıklar.</span><span class="sxs-lookup"><span data-stu-id="f7021-105">This topic describes what is included in the **Purchase spend analysis** Microsoft Power BI content.</span></span> <span data-ttu-id="f7021-106">Power BI raporlarına nasıl erişileceğini açıklar ve içeriği oluşturmakta kullanılan veri modeli ve varlıklar hakkında bilgi sağlar.</span><span class="sxs-lookup"><span data-stu-id="f7021-106">It explains how to access the Power BI reports, and provides information about the data model and entities that are used to build the content.</span></span>

## <a name="overview"></a><span data-ttu-id="f7021-107">Özet</span><span class="sxs-lookup"><span data-stu-id="f7021-107">Overview</span></span>

<span data-ttu-id="f7021-108">**Satınalma harcaması analizi** Power BI içeriği satınalma yöneticilerine ve bütçelerden sorumlu yöneticilere satınalma harcamalarını izleme konusunda yardımcı olmak üzere tasarlanmıştır.</span><span class="sxs-lookup"><span data-stu-id="f7021-108">The **Purchase spend analysis** Power BI content was designed to help purchasing managers and managers who are responsible for budgets keep an eye on purchase spending.</span></span> <span data-ttu-id="f7021-109">Yöneticiler satınalma harcamasını aşağıdaki şekillerde analiz edebilirler:</span><span class="sxs-lookup"><span data-stu-id="f7021-109">Managers can analyze purchase spending in the following ways:</span></span>

- <span data-ttu-id="f7021-110">Yılbaşından bugüne satınalma (satıcı grubu ve tek tek satıcılara, tedarik kategorisine ve bireysel ürünlere ve satıcı konumuna göre)</span><span class="sxs-lookup"><span data-stu-id="f7021-110">Year-to-date purchase (by vendor group and individual vendors, procurement category and individual products, and vendor location)</span></span>
- <span data-ttu-id="f7021-111">Yıldan yıla satınalma değişikliği (satıcı grubu ve tedarik kategorisine göre)</span><span class="sxs-lookup"><span data-stu-id="f7021-111">Year-over-year purchase change (by vendor group and procurement category)</span></span>

<span data-ttu-id="f7021-112">İçerik, alınan satınalma hareketi verilerini kullanır ve hem şirket çapında satınalma rakamlarının toplam görünümünü hem de satıcı ve ürünler için satınalma harcamasının dağılımını verir.</span><span class="sxs-lookup"><span data-stu-id="f7021-112">The content uses purchase transactional data, and provides both an aggregate view of the company-wide purchase figures and a breakdown of purchase spending by vendor and product.</span></span> <span data-ttu-id="f7021-113">Raporlar satınalma harcamalarında zaman içindeki değişiklikleri öne çıkarır.</span><span class="sxs-lookup"><span data-stu-id="f7021-113">Reports highlight changes in purchase spending over time.</span></span> <span data-ttu-id="f7021-114">Bu nedenle, raporlar yöneticileri ayrı satıcılar ve ürünlerle ilgili olarak pozitif ve negatif harcama eğilimleri hakkında uyarmak için kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="f7021-114">Therefore, the reports can be used to alert managers about positive and negative spending trends for individual vendors and products.</span></span> <span data-ttu-id="f7021-115">Ek olarak grafikler farklı tedarik kategorileri ve satıcı grupları için satınalma harcamasını gösterir.</span><span class="sxs-lookup"><span data-stu-id="f7021-115">Additionally, charts show purchase spending for different procurement categories and vendor groups.</span></span> <span data-ttu-id="f7021-116">Bu nedenle, kategori ve bölgesel yöneticiler, harcama davranışındaki değişiklikleri tanımlamaya yardımcı olması açısından bu grafikleri kullanabilirler.</span><span class="sxs-lookup"><span data-stu-id="f7021-116">Therefore, category and regional managers can use the charts to help identify changes in spending behavior.</span></span>

## <a name="accessing-the-power-bi-content"></a><span data-ttu-id="f7021-117">Power BI içeriğine erişmek</span><span class="sxs-lookup"><span data-stu-id="f7021-117">Accessing the Power BI content</span></span>
<span data-ttu-id="f7021-118">**Satınalma ve harcama analizi** Power BI içeriği **Satın alma ve harcama analizi** sayfasında gösterilir (**Tedarik ve kaynak atama** \> **Sorgular ve raporlar** \> **Satın alma performansı analizi** \> **Satın alma ve harcama analizi**).</span><span class="sxs-lookup"><span data-stu-id="f7021-118">The **Purchase spend analysis** Power BI content is shown on the **Purchase and spend analysis** page (**Procurement and sourcing** \> **Inquiries and reports** \> **Purchase performance analysis** \> **Purchase and spend analysis**).</span></span>

## <a name="metrics-that-are-included-in-the-power-bi-content"></a><span data-ttu-id="f7021-119">Power BI içeriğine dahil olan ölçümler</span><span class="sxs-lookup"><span data-stu-id="f7021-119">Metrics that are included in the Power BI content</span></span>
<span data-ttu-id="f7021-120">**Satın alma harcaması analizi** Power BI içeriği bir dizi ölçümden oluşan bir rapor içerir.</span><span class="sxs-lookup"><span data-stu-id="f7021-120">The **Purchase spend analysis** Power BI content includes a report that consists of a set of metrics.</span></span> <span data-ttu-id="f7021-121">Bu ölçümler grafikler, kutucuklar ve tablolar şeklinde görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="f7021-121">These metrics are visualized as charts, tiles, and tables.</span></span> <span data-ttu-id="f7021-122">Aşağıdaki tabloda, görsellere yönelik genel bakış sunulur.</span><span class="sxs-lookup"><span data-stu-id="f7021-122">The following table provides an overview of the visualizations.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="f7021-123">Rapor sayfası</span><span class="sxs-lookup"><span data-stu-id="f7021-123">Report page</span></span></th>
<th><span data-ttu-id="f7021-124">Grafikler</span><span class="sxs-lookup"><span data-stu-id="f7021-124">Charts</span></span></th>
<th><span data-ttu-id="f7021-125">Kutucuklar</span><span class="sxs-lookup"><span data-stu-id="f7021-125">Tiles</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="f7021-126">Satıcıya göre satınalma</span><span class="sxs-lookup"><span data-stu-id="f7021-126">Purchase by vendor</span></span></td>
<td><ul>
<li><span data-ttu-id="f7021-127">Satınalmaya göre en iyi 10 satıcı (yığılmış çubuk grafik)</span><span class="sxs-lookup"><span data-stu-id="f7021-127">Top 10 vendors by purchase (stacked bar chart)</span></span></li>
<li><span data-ttu-id="f7021-128">Satıcı grubuna / ülkeye / ada göre toplam satınalma (pasta grafik)</span><span class="sxs-lookup"><span data-stu-id="f7021-128">Total purchase by vendor group / country / name (pie chart)</span></span></li>
<li><span data-ttu-id="f7021-129">Satıcı grubuna / ülkeye / ada göre satınalma (sütun grafik)</span><span class="sxs-lookup"><span data-stu-id="f7021-129">Purchase by vendor group / country / name (column chart)</span></span></li>
<li><span data-ttu-id="f7021-130">Satıcı grubuna / ülkeye / ada göre ortalama satınalma (sütun grafik)</span><span class="sxs-lookup"><span data-stu-id="f7021-130">Average purchase by vendor group / country / name (column chart)</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="f7021-131">Satınalma toplamı</span><span class="sxs-lookup"><span data-stu-id="f7021-131">Total purchase</span></span></li>
<li><span data-ttu-id="f7021-132">Yıllara göre satınalmadaki büyüme</span><span class="sxs-lookup"><span data-stu-id="f7021-132">YOY purchase growth</span></span></li>
<li><span data-ttu-id="f7021-133">Toplam satıcı sayısı</span><span class="sxs-lookup"><span data-stu-id="f7021-133">Total # vendors</span></span></li>
<li><span data-ttu-id="f7021-134">Toplam etkin satıcı sayısı</span><span class="sxs-lookup"><span data-stu-id="f7021-134">Total # of active vendors</span></span></li>
</ul></td>
</tr>
<tr>
<td><span data-ttu-id="f7021-135">Ürüne göre satın alma</span><span class="sxs-lookup"><span data-stu-id="f7021-135">Purchase by product</span></span></td>
<td><ul>
<li><span data-ttu-id="f7021-136">Tedarik kategorisine / ürün adına göre satınalma (sütun grafiği)</span><span class="sxs-lookup"><span data-stu-id="f7021-136">Purchase by procurement category / product name (column chart)</span></span></li>
<li><span data-ttu-id="f7021-137">Tedarik kategorisine / ürün adına göre toplam satınalma (pasta grafik)</span><span class="sxs-lookup"><span data-stu-id="f7021-137">Total purchase by procurement category / product name (pie chart)</span></span></li>
<li><span data-ttu-id="f7021-138">Satınalmaya göre en iyi 10 ürün (yığılmış çubuk grafik)</span><span class="sxs-lookup"><span data-stu-id="f7021-138">Top 10 products by purchase (stacked bar chart)</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="f7021-139">Toplam ürün sayısı</span><span class="sxs-lookup"><span data-stu-id="f7021-139">Total # of products</span></span></li>
<li><span data-ttu-id="f7021-140">Etkin ürünlerin toplam sayısının toplam etkin ürünlere yüzdesi</span><span class="sxs-lookup"><span data-stu-id="f7021-140">Total active products percentage of total # of products</span></span></li>
<li><span data-ttu-id="f7021-141">Satınalmanın %80'ini oluşturan ürünlerin sayısı</span><span class="sxs-lookup"><span data-stu-id="f7021-141">Number of products accounting for 80% purchase</span></span></li>
</ul></td>
</tr>
<tr>
<td><span data-ttu-id="f7021-142">Döneme göre satınalma\*</span><span class="sxs-lookup"><span data-stu-id="f7021-142">Purchase by period\*</span></span></td>
<td><ul>
<li><span data-ttu-id="f7021-143">Aya / güne göre satınalma (sütun grafiği)</span><span class="sxs-lookup"><span data-stu-id="f7021-143">Purchase by month / day (column chart)</span></span></li>
<li><span data-ttu-id="f7021-144">Toplam satınalmanın yıllara görefarkı (şelale grafik)</span><span class="sxs-lookup"><span data-stu-id="f7021-144">Cumulative purchase YOY variance (waterfall chart)</span></span></li>
<li><span data-ttu-id="f7021-145">Toplam satınalmada yıllara göre büyüme (sütun grafik)</span><span class="sxs-lookup"><span data-stu-id="f7021-145">Total purchase YOY growth (column chart)</span></span></li>
<li><span data-ttu-id="f7021-146">Tedarik ekstresi (matriks)</span><span class="sxs-lookup"><span data-stu-id="f7021-146">Procurement statement (matrix)</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="f7021-147">Yıllara göre satınalmadaki büyüme</span><span class="sxs-lookup"><span data-stu-id="f7021-147">YOY purchase growth</span></span></li>
<li><span data-ttu-id="f7021-148">Yıllara göre satınalmadaki büyüme yüzdesi</span><span class="sxs-lookup"><span data-stu-id="f7021-148">YOY purchase growth %</span></span></li>
</ul></td>
</tr>
<tr>
<td><span data-ttu-id="f7021-149">Satıcı konumuna göre satınalma</span><span class="sxs-lookup"><span data-stu-id="f7021-149">Purchase by vendor location</span></span></td>
<td><ul>
<li><span data-ttu-id="f7021-150">Şehre göre satınalma</span><span class="sxs-lookup"><span data-stu-id="f7021-150">Purchase by city</span></span></li>
<li><span data-ttu-id="f7021-151">Satınalmada yıldan yıla büyüme yüzdesi</span><span class="sxs-lookup"><span data-stu-id="f7021-151">Purchase YOY growth %</span></span></li>
<li><span data-ttu-id="f7021-152">Ülkeye göre satınalma</span><span class="sxs-lookup"><span data-stu-id="f7021-152">Purchase by country</span></span></li>
</ul></td>
<td></td>
</tr>
<tr>
<td><span data-ttu-id="f7021-153">Zaman göre satınalma harcaması analizi</span><span class="sxs-lookup"><span data-stu-id="f7021-153">Purchase spend analysis by time</span></span></td>
<td><ul>
<li><span data-ttu-id="f7021-154">Aya / güne göre geçerli yıldaki satın alma (çizgi grafiği)</span><span class="sxs-lookup"><span data-stu-id="f7021-154">Purchase current year by month / day (line chart)</span></span></li>
<li><span data-ttu-id="f7021-155">Geçerli yıl ve önceki yıldaki satınalma (satır ve sütun grafiği)</span><span class="sxs-lookup"><span data-stu-id="f7021-155">Purchase current and last year (line and column chart)</span></span></li>
</ul></td>
<td></td>
</tr>
<tr>
<td><span data-ttu-id="f7021-156">Satıcıya göre satınalma harcaması analizi</span><span class="sxs-lookup"><span data-stu-id="f7021-156">Purchase spend analysis by vendor</span></span></td>
<td><ul>
<li><span data-ttu-id="f7021-157">İlk 10 satıcı satınalmanın satınalmaya göre yüzdesi (huni)</span><span class="sxs-lookup"><span data-stu-id="f7021-157">Top 10 vendor purchase % of purchase (funnel)</span></span></li>
<li><span data-ttu-id="f7021-158">Yıllara göre artan harcamayla en iyi 10 satıcı</span><span class="sxs-lookup"><span data-stu-id="f7021-158">Top 10 vendors with increased spending YOY</span></span></li>
<li><span data-ttu-id="f7021-159">Yıllara göre azalan harcamayla en iyi 10 satıcı</span><span class="sxs-lookup"><span data-stu-id="f7021-159">Top 10 vendors with decreased spending YOY</span></span></li>
</ul></td>
<td></td>
</tr>
</tbody>
</table>

<span data-ttu-id="f7021-160">\* Bu yılki ve geçen yılki satınalma ve tedarik kategorisine göre büyüme.</span><span class="sxs-lookup"><span data-stu-id="f7021-160">\* Purchase this year and last year, and growth by procurement category</span></span>

## <a name="data-model-and-entities"></a><span data-ttu-id="f7021-161">Veri modeli ve varlıklar</span><span class="sxs-lookup"><span data-stu-id="f7021-161">Data model and entities</span></span>
<span data-ttu-id="f7021-162">Aşağıdaki veriler **Satınalma harcaması analizi** Power BI içeriğindeki rapor sayfalarını doldurmak için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="f7021-162">The following data is used to fill the report pages in the **Purchase spend analysis** Power BI content.</span></span> <span data-ttu-id="f7021-163">Bu veri, Varlık mağazasında hazırlanan toplam ölçümler olarak sunulur.</span><span class="sxs-lookup"><span data-stu-id="f7021-163">This data is represented as aggregate measurements that are staged in the Entity store.</span></span> <span data-ttu-id="f7021-164">Varlık mağazası, analizler için en iyi duruma getirilmiş bir Microsoft SQL Sunucu veritabanıdır.</span><span class="sxs-lookup"><span data-stu-id="f7021-164">The Entity store is a Microsoft SQL Server database that is optimized for analytics.</span></span> <span data-ttu-id="f7021-165">Daha fazla bilgi için, bkz. [Varlık mağazası ile Power BI tümleştirmesine genel bakış](power-bi-integration-entity-store.md).</span><span class="sxs-lookup"><span data-stu-id="f7021-165">For more information, see [Overview of Power BI integration with Entity store](power-bi-integration-entity-store.md).</span></span>

<span data-ttu-id="f7021-166">Bu içerikteki toplam ölçümleri, Microsoft Dynamics AX 2012 ve Microsoft Dynamics AX 2012 R3'teki Satınalma Küpü'nde bulunan toplama ölçümlerin alt kümesidir.</span><span class="sxs-lookup"><span data-stu-id="f7021-166">The aggregate measurements in this content are the subset of aggregate measurements that were available in the Purchase Cube in Microsoft Dynamics AX 2012 and Microsoft Dynamics AX 2012 R3.</span></span> <span data-ttu-id="f7021-167">Varlık deposundaki küpün toplama ölçülerini hazırlamak için bu ölçümleri dağıtılabilir yapmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="f7021-167">To stage the cube's aggregate measurements in the Entity store, you must make them deployable.</span></span> <span data-ttu-id="f7021-168">Daha fazla bilgi için, [Power BI ile Varlık deposu tümleştirmesine genel bakış](power-bi-integration-entity-store.md) bölümündeki toplanan ölçümleri Varlık Deposuna ekleme yordamına bakın.</span><span class="sxs-lookup"><span data-stu-id="f7021-168">For more information, see the procedure for staging aggregate measurements in the Entity store in [Overview of Power BI integration with Entity store](power-bi-integration-entity-store.md).</span></span> <span data-ttu-id="f7021-169">Aşağıda verilen önemli toplanan ölçümleri doğrudan Fatura satırları varlığından kullanılabilir ve içeriğin temeli olarak kullanılır.</span><span class="sxs-lookup"><span data-stu-id="f7021-169">The following key aggregate measurements are available directly from the Invoice lines entity and are used as the basis of the content.</span></span>

| <span data-ttu-id="f7021-170">Varlık</span><span class="sxs-lookup"><span data-stu-id="f7021-170">Entity</span></span>        | <span data-ttu-id="f7021-171">Önemli toplam ölçümler</span><span class="sxs-lookup"><span data-stu-id="f7021-171">Key aggregate measurements</span></span> | <span data-ttu-id="f7021-172">Veri kaynağı</span><span class="sxs-lookup"><span data-stu-id="f7021-172">Data source</span></span>                                 | <span data-ttu-id="f7021-173">Alan</span><span class="sxs-lookup"><span data-stu-id="f7021-173">Field</span></span>              | <span data-ttu-id="f7021-174">Açıklama</span><span class="sxs-lookup"><span data-stu-id="f7021-174">Description</span></span>                            |
|---------------|----------------------------|---------------------------------------------|--------------------|----------------------------------------|
| <span data-ttu-id="f7021-175">Fatura satırları</span><span class="sxs-lookup"><span data-stu-id="f7021-175">Invoice lines</span></span> | <span data-ttu-id="f7021-176">Satınalma</span><span class="sxs-lookup"><span data-stu-id="f7021-176">Purchase</span></span>                   | <span data-ttu-id="f7021-177">VendInvoiceTrans</span><span class="sxs-lookup"><span data-stu-id="f7021-177">VendInvoiceTrans</span></span>                            | <span data-ttu-id="f7021-178">SUM(LineAmountMST)</span><span class="sxs-lookup"><span data-stu-id="f7021-178">SUM(LineAmountMST)</span></span> | <span data-ttu-id="f7021-179">Muhasebe para birimi cinsinden tutar.</span><span class="sxs-lookup"><span data-stu-id="f7021-179">The amount in the accounting currency.</span></span> |

<span data-ttu-id="f7021-180">Aşağıdaki tablo içerikte Fatura satırları varlığından hesaplanan anahtar ölçümleri gösterir.</span><span class="sxs-lookup"><span data-stu-id="f7021-180">The following table shows the key measurements in the content that are calculated from the Invoice lines entity.</span></span>

| <span data-ttu-id="f7021-181">Ölçü</span><span class="sxs-lookup"><span data-stu-id="f7021-181">Measure</span></span>               | <span data-ttu-id="f7021-182">Hesaplama</span><span class="sxs-lookup"><span data-stu-id="f7021-182">Calculation</span></span>                                                                                         |
|-----------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f7021-183">Geçerli yıldaki satınalma</span><span class="sxs-lookup"><span data-stu-id="f7021-183">Purchase current year</span></span> | <span data-ttu-id="f7021-184">Geçerli yıldaki satınalma = TOPLA('Fatura satırları'\[Satınalma\])</span><span class="sxs-lookup"><span data-stu-id="f7021-184">Purchase current year = SUM('Invoice lines'\[Purchase\])</span></span>                                            |
| <span data-ttu-id="f7021-185">Geçen yılki satınalma</span><span class="sxs-lookup"><span data-stu-id="f7021-185">Purchase last year</span></span>    | <span data-ttu-id="f7021-186">Geçen yılki satınalma = HESAPLA(TOPLA('Fatura satırları'\[Satınalma\]), SAMEPERIODLASTYEAR (Tarihler\[Tarih\])</span><span class="sxs-lookup"><span data-stu-id="f7021-186">Purchase last year = CALCULATE(SUM('Invoice lines'\[Purchase\]), SAMEPERIODLASTYEAR(Dates\[Date\]))</span></span> |
| <span data-ttu-id="f7021-187">Yıllara göre satınalmadaki büyüme</span><span class="sxs-lookup"><span data-stu-id="f7021-187">YOY purchase growth</span></span>   | <span data-ttu-id="f7021-188">Yıllara göre satınalmadaki büyüme = \[Geçerli yıldaki satınalma\]: \[Geçen yıldaki satınalma\]</span><span class="sxs-lookup"><span data-stu-id="f7021-188">YOY purchase growth = \[Purchase current year\] – \[Purchase last year\]</span></span>                            |

<span data-ttu-id="f7021-189">İçerikte bulunan aşağıdaki temel boyutları, daha büyük hassasiyet ve daha derin analiz bilgileri elde edebilmeniz amacıyla toplama ölçümlerini bölmek üzere filtre olarak kullanılır.</span><span class="sxs-lookup"><span data-stu-id="f7021-189">The following key dimensions in the content are used as filters to slice the aggregate measurements, so that you can achieve more granularity and gain deeper analytical insights.</span></span>

| <span data-ttu-id="f7021-190">Varlık</span><span class="sxs-lookup"><span data-stu-id="f7021-190">Entity</span></span>                 | <span data-ttu-id="f7021-191">Öznitelik örnekleri</span><span class="sxs-lookup"><span data-stu-id="f7021-191">Examples of attributes</span></span>                                |
|------------------------|-------------------------------------------------------|
| <span data-ttu-id="f7021-192">Satıcılar</span><span class="sxs-lookup"><span data-stu-id="f7021-192">Vendors</span></span>                | <span data-ttu-id="f7021-193">Satıcı grupları, Satıcı ülkesi veya bölgeleri, Satıcı adı</span><span class="sxs-lookup"><span data-stu-id="f7021-193">Vendor groups, Vendor country or regions, Vendor name</span></span> |
| <span data-ttu-id="f7021-194">Ürünler</span><span class="sxs-lookup"><span data-stu-id="f7021-194">Products</span></span>               | <span data-ttu-id="f7021-195">Ürün numarası, Ürün adı, Madde grupları adı</span><span class="sxs-lookup"><span data-stu-id="f7021-195">Product number, Product name, Item groups name</span></span>        |
| <span data-ttu-id="f7021-196">Tedarik kategorileri</span><span class="sxs-lookup"><span data-stu-id="f7021-196">Procurement categories</span></span> | <span data-ttu-id="f7021-197">Tedarik kategorisi, Tedarik kategorisi adları</span><span class="sxs-lookup"><span data-stu-id="f7021-197">Procurement category, Procurement category names</span></span>      |
| <span data-ttu-id="f7021-198">Tüzel kişilikler</span><span class="sxs-lookup"><span data-stu-id="f7021-198">Legal entities</span></span>         | <span data-ttu-id="f7021-199">Tüzel kişiliğin adı</span><span class="sxs-lookup"><span data-stu-id="f7021-199">Legal entity name</span></span>                                     |
| <span data-ttu-id="f7021-200">Tarihler</span><span class="sxs-lookup"><span data-stu-id="f7021-200">Dates</span></span>                  | <span data-ttu-id="f7021-201">Tarihler, Yıl denkleştirme</span><span class="sxs-lookup"><span data-stu-id="f7021-201">Dates, Year offset</span></span>                                    |

<span data-ttu-id="f7021-202">Varsayılan olarak, içerik geçerli takvim yılına ilişkin verileri gösterir.</span><span class="sxs-lookup"><span data-stu-id="f7021-202">By default, the content shows data for the current calendar year.</span></span> <span data-ttu-id="f7021-203">Ancak, rapor filtreleri bölümünden tarih filtresini değiştirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="f7021-203">However, you can change the date filter in the report filters section.</span></span> <span data-ttu-id="f7021-204">Şirket filtresini de değiştirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="f7021-204">You can also change the company filter.</span></span>

