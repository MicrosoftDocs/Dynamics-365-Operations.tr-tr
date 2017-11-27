---
title: "Satınalma harcaması analizi Power BI içeriği"
description: "Bu konu, Power BI Satınalma harcaması analizinde nelerin bulunduğunu açıklar. Bu ayrıca, içeriğe dahil edilen raporların nasıl kullanılacağını açıklar ve içeriği oluşturmakta kullanılan veri modeli ve varlıklar hakkında bilgi sağlar."
author: FrankDahl
manager: AnnBe
ms.date: 06/16/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
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
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 6485f36802fc4e327e223f47d65c4bdca11c1609
ms.contentlocale: tr-tr
ms.lasthandoff: 11/03/2017

---

# <a name="purchase-spend-analysis-power-bi-content"></a><span data-ttu-id="071a6-104">Satınalma harcaması analizi Power BI içeriği</span><span class="sxs-lookup"><span data-stu-id="071a6-104">Purchase spend analysis Power BI content</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="071a6-105">Bu konu, Power BI **Satınalma harcaması** analizinde nelerin bulunduğunu açıklar.</span><span class="sxs-lookup"><span data-stu-id="071a6-105">This topic describes what is included in the **Purchase spend analysis** Microsoft Power BI content.</span></span> <span data-ttu-id="071a6-106">Power BI raporlarına nasıl erişileceğini açıklar ve içeriği oluşturmakta kullanılan veri modeli ve varlıklar hakkında bilgi sağlar.</span><span class="sxs-lookup"><span data-stu-id="071a6-106">It explains how to access the Power BI reports, and provides information about the data model and entities that are used to build the content.</span></span>

## <a name="overview"></a><span data-ttu-id="071a6-107">Özet</span><span class="sxs-lookup"><span data-stu-id="071a6-107">Overview</span></span>

<span data-ttu-id="071a6-108">**Satınalma harcaması analizi** Power BI içeriği satınalma yöneticilerine ve bütçelerden sorumlu yöneticilere satınalma harcamalarını izleme konusunda yardımcı olmak üzere tasarlanmıştır.</span><span class="sxs-lookup"><span data-stu-id="071a6-108">The **Purchase spend analysis** Power BI content was designed to help purchasing managers and managers who are responsible for budgets keep an eye on purchase spending.</span></span> <span data-ttu-id="071a6-109">Yöneticiler satınalma harcamasını aşağıdaki şekillerde analiz edebilirler:</span><span class="sxs-lookup"><span data-stu-id="071a6-109">Managers can analyze purchase spending in the following ways:</span></span>

-   <span data-ttu-id="071a6-110">Yılbaşından bugüne satınalma (satıcı grubu ve tek tek satıcılara, tedarik kategorisine ve bireysel ürünlere ve satıcı konumuna göre)</span><span class="sxs-lookup"><span data-stu-id="071a6-110">Year-to-date purchase (by vendor group and individual vendors, procurement category and individual products, and vendor location)</span></span>
-   <span data-ttu-id="071a6-111">Yıldan yıla satınalma değişikliği (satıcı grubu ve tedarik kategorisine göre)</span><span class="sxs-lookup"><span data-stu-id="071a6-111">Year-over-year purchase change (by vendor group and procurement category)</span></span>

<span data-ttu-id="071a6-112">İçerik, alınan satınalma hareketi verilerini kullanır ve hem şirket çapında satınalma rakamlarının toplam görünümünü hem de satıcı ve ürünler için satınalma harcamasının dağılımını verir.</span><span class="sxs-lookup"><span data-stu-id="071a6-112">The content uses purchase transactional data, and provides both an aggregate view of the company-wide purchase figures and a breakdown of purchase spending by vendor and product.</span></span> <span data-ttu-id="071a6-113">Raporlar satınalma harcamalarında zaman içindeki değişiklikleri öne çıkarır.</span><span class="sxs-lookup"><span data-stu-id="071a6-113">Reports highlight changes in purchase spending over time.</span></span> <span data-ttu-id="071a6-114">Bu nedenle, raporlar yöneticileri ayrı satıcılar ve ürünlerle ilgili olarak pozitif ve negatif harcama eğilimleri hakkında uyarmak için kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="071a6-114">Therefore, the reports can be used to alert managers about positive and negative spending trends for individual vendors and products.</span></span> <span data-ttu-id="071a6-115">Ek olarak grafikler farklı tedarik kategorileri ve satıcı grupları için satınalma harcamasını gösterir.</span><span class="sxs-lookup"><span data-stu-id="071a6-115">Additionally, charts show purchase spending for different procurement categories and vendor groups.</span></span> <span data-ttu-id="071a6-116">Bu nedenle, kategori ve bölgesel yöneticiler, harcama davranışındaki değişiklikleri tanımlamaya yardımcı olması açısından bu grafikleri kullanabilirler.</span><span class="sxs-lookup"><span data-stu-id="071a6-116">Therefore, category and regional managers can use the charts to help identify changes in spending behavior.</span></span>

## <a name="accessing-the-power-bi-content"></a><span data-ttu-id="071a6-117">Power BI içeriğine erişmek</span><span class="sxs-lookup"><span data-stu-id="071a6-117">Accessing the Power BI content</span></span>
<span data-ttu-id="071a6-118">Microsoft Dynamics 365 for Finance and Operations, Enterprise edition (Temmuz 2017) kullanıyorsanız, **Satınalma harcaması analizi** Power BI içeriği **Satınalma ve harcama analizi** sayfasında (**Tedarik ve kaynak atama** > **Sorgular ve raporlar** > **Satınalma performansı analizi** > **Satınalma ve harcama analizi**) gösterilir.</span><span class="sxs-lookup"><span data-stu-id="071a6-118">If you're using Microsoft Dynamics 365 for Finance and Operations, Enterprise edition (July 2017), the **Purchase spend analysis** Power BI content is shown on the **Purchase and spend analysis** page (**Procurement and sourcing** > **Inquiries and reports** > **Purchase performance analysis** > **Purchase and spend analysis**).</span></span> 

## <a name="metrics-that-are-included-in-the-power-bi-content"></a><span data-ttu-id="071a6-119">Power BI içeriğine dahil olan ölçümler</span><span class="sxs-lookup"><span data-stu-id="071a6-119">Metrics that are included in the Power BI content</span></span>
<span data-ttu-id="071a6-120">**Satın alma harcaması analizi** Power BI içeriği bir dizi ölçümden oluşan bir rapor içerir.</span><span class="sxs-lookup"><span data-stu-id="071a6-120">The **Purchase spend analysis** Power BI content includes a report that consists of a set of metrics.</span></span> <span data-ttu-id="071a6-121">Bu ölçümler grafikler, kutucuklar ve tablolar şeklinde görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="071a6-121">These metrics are visualized as charts, tiles, and tables.</span></span> <span data-ttu-id="071a6-122">Aşağıdaki tabloda, görsellere yönelik genel bakış sunulur.</span><span class="sxs-lookup"><span data-stu-id="071a6-122">The following table provides an overview of the visualizations.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="071a6-123">Rapor sayfası</span><span class="sxs-lookup"><span data-stu-id="071a6-123">Report page</span></span></th>
<th><span data-ttu-id="071a6-124">Grafikler</span><span class="sxs-lookup"><span data-stu-id="071a6-124">Charts</span></span></th>
<th><span data-ttu-id="071a6-125">Kutucuklar</span><span class="sxs-lookup"><span data-stu-id="071a6-125">Tiles</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="071a6-126">Satıcıya göre satınalma</span><span class="sxs-lookup"><span data-stu-id="071a6-126">Purchase by vendor</span></span></td>
<td><ul>
<li><span data-ttu-id="071a6-127">Satınalmaya göre en iyi 10 satıcı (yığılmış çubuk grafik)</span><span class="sxs-lookup"><span data-stu-id="071a6-127">Top 10 vendors by purchase (stacked bar chart)</span></span></li>
<li><span data-ttu-id="071a6-128">Satıcı grubuna / ülkeye / ada göre toplam satınalma (pasta grafik)</span><span class="sxs-lookup"><span data-stu-id="071a6-128">Total purchase by vendor group / country / name (pie chart)</span></span></li>
<li><span data-ttu-id="071a6-129">Satıcı grubuna / ülkeye / ada göre satınalma (sütun grafik)</span><span class="sxs-lookup"><span data-stu-id="071a6-129">Purchase by vendor group / country / name (column chart)</span></span></li>
<li><span data-ttu-id="071a6-130">Satıcı grubuna / ülkeye / ada göre ortalama satınalma (sütun grafik)</span><span class="sxs-lookup"><span data-stu-id="071a6-130">Average purchase by vendor group / country / name (column chart)</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="071a6-131">Satınalma toplamı</span><span class="sxs-lookup"><span data-stu-id="071a6-131">Total purchase</span></span></li>
<li><span data-ttu-id="071a6-132">Yıllara göre satınalmadaki büyüme</span><span class="sxs-lookup"><span data-stu-id="071a6-132">YOY purchase growth</span></span></li>
<li><span data-ttu-id="071a6-133">Toplam satıcı sayısı</span><span class="sxs-lookup"><span data-stu-id="071a6-133">Total # vendors</span></span></li>
<li><span data-ttu-id="071a6-134">Toplam etkin satıcı sayısı</span><span class="sxs-lookup"><span data-stu-id="071a6-134">Total # of active vendors</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="071a6-135">Ürüne göre satın alma</span><span class="sxs-lookup"><span data-stu-id="071a6-135">Purchase by product</span></span></td>
<td><ul>
<li><span data-ttu-id="071a6-136">Tedarik kategorisine / ürün adına göre satınalma (sütun grafiği)</span><span class="sxs-lookup"><span data-stu-id="071a6-136">Purchase by procurement category / product name (column chart)</span></span></li>
<li><span data-ttu-id="071a6-137">Tedarik kategorisine / ürün adına göre toplam satınalma (pasta grafik)</span><span class="sxs-lookup"><span data-stu-id="071a6-137">Total purchase by procurement category / product name (pie chart)</span></span></li>
<li><span data-ttu-id="071a6-138">Satınalmaya göre en iyi 10 ürün (yığılmış çubuk grafik)</span><span class="sxs-lookup"><span data-stu-id="071a6-138">Top 10 products by purchase (stacked bar chart)</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="071a6-139">Toplam ürün sayısı</span><span class="sxs-lookup"><span data-stu-id="071a6-139">Total # of products</span></span></li>
<li><span data-ttu-id="071a6-140">Etkin ürünlerin toplam sayısının toplam etkin ürünlere yüzdesi</span><span class="sxs-lookup"><span data-stu-id="071a6-140">Total active products percentage of total # of products</span></span></li>
<li><span data-ttu-id="071a6-141">Satınalmanın %80'ini oluşturan ürünlerin sayısı</span><span class="sxs-lookup"><span data-stu-id="071a6-141">Number of products accounting for 80% purchase</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="071a6-142">Döneme göre satınalma*</span><span class="sxs-lookup"><span data-stu-id="071a6-142">Purchase by period*</span></span></td>
<td><ul>
<li><span data-ttu-id="071a6-143">Aya / güne göre satınalma (sütun grafiği)</span><span class="sxs-lookup"><span data-stu-id="071a6-143">Purchase by month / day (column chart)</span></span></li>
<li><span data-ttu-id="071a6-144">Toplam satınalmanın yıllara görefarkı (şelale grafik)</span><span class="sxs-lookup"><span data-stu-id="071a6-144">Cumulative purchase YOY variance (waterfall chart)</span></span></li>
<li><span data-ttu-id="071a6-145">Toplam satınalmada yıllara göre büyüme (sütun grafik)</span><span class="sxs-lookup"><span data-stu-id="071a6-145">Total purchase YOY growth (column chart)</span></span></li>
<li><span data-ttu-id="071a6-146">Tedarik ekstresi (matriks)</span><span class="sxs-lookup"><span data-stu-id="071a6-146">Procurement statement (matrix)</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="071a6-147">Yıllara göre satınalmadaki büyüme</span><span class="sxs-lookup"><span data-stu-id="071a6-147">YOY purchase growth</span></span></li>
<li><span data-ttu-id="071a6-148">Yıllara göre satınalmadaki büyüme yüzdesi</span><span class="sxs-lookup"><span data-stu-id="071a6-148">YOY purchase growth %</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="071a6-149">Satıcı konumuna göre satınalma</span><span class="sxs-lookup"><span data-stu-id="071a6-149">Purchase by vendor location</span></span></td>
<td><ul>
<li><span data-ttu-id="071a6-150">Şehre göre satınalma</span><span class="sxs-lookup"><span data-stu-id="071a6-150">Purchase by city</span></span></li>
<li><span data-ttu-id="071a6-151">Satınalmada yıldan yıla büyüme yüzdesi</span><span class="sxs-lookup"><span data-stu-id="071a6-151">Purchase YOY growth %</span></span></li>
<li><span data-ttu-id="071a6-152">Ülkeye göre satınalma</span><span class="sxs-lookup"><span data-stu-id="071a6-152">Purchase by country</span></span></li>
</ul></td>
<td></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="071a6-153">Zaman göre satınalma harcaması analizi</span><span class="sxs-lookup"><span data-stu-id="071a6-153">Purchase spend analysis by time</span></span></td>
<td><ul>
<li><span data-ttu-id="071a6-154">Aya / güne göre geçerli yıldaki satın alma (çizgi grafiği)</span><span class="sxs-lookup"><span data-stu-id="071a6-154">Purchase current year by month / day (line chart)</span></span></li>
<li><span data-ttu-id="071a6-155">Geçerli yıl ve önceki yıldaki satınalma (satır ve sütun grafiği)</span><span class="sxs-lookup"><span data-stu-id="071a6-155">Purchase current and last year (line and column chart)</span></span></li>
</ul></td>
<td></td>
</tr>
<tr class="even">
<td><span data-ttu-id="071a6-156">Satıcıya göre satınalma harcaması analizi</span><span class="sxs-lookup"><span data-stu-id="071a6-156">Purchase spend analysis by vendor</span></span></td>
<td><ul>
<li><span data-ttu-id="071a6-157">İlk 10 satıcı satınalmanın satınalmaya göre yüzdesi (huni)</span><span class="sxs-lookup"><span data-stu-id="071a6-157">Top 10 vendor purchase % of purchase (funnel)</span></span></li>
<li><span data-ttu-id="071a6-158">Yıllara göre artan harcamayla en iyi 10 satıcı</span><span class="sxs-lookup"><span data-stu-id="071a6-158">Top 10 vendors with increased spending YOY</span></span></li>
<li><span data-ttu-id="071a6-159">Yıllara göre azalan harcamayla en iyi 10 satıcı</span><span class="sxs-lookup"><span data-stu-id="071a6-159">Top 10 vendors with decreased spending YOY</span></span></li>
</ul></td>
<td></td>
</tr>
</tbody>
</table>

<span data-ttu-id="071a6-160">\* Bu yılki ve geçen yılki satınalma ve tedarik kategorisine göre büyüme.</span><span class="sxs-lookup"><span data-stu-id="071a6-160">\* Purchase this year and last year, and growth by procurement category</span></span>

## <a name="extending-the-power-bi-content"></a><span data-ttu-id="071a6-161">Power BI içeriğini genişletmek</span><span class="sxs-lookup"><span data-stu-id="071a6-161">Extending the Power BI content</span></span>
<span data-ttu-id="071a6-162">Microsoft Dynamics Lifecycle Services (LCS) içinde kullanılabilir durumda olan içerik paketlerini kullanarak, Microsoft Dynamics 365'e oturum açmayan kişilere harika analizler sunabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="071a6-162">By using the content packs that are available in Microsoft Dynamics Lifecycle Services (LCS), you can provide great analytics to people who don't sign in to Microsoft Dynamics 365.</span></span> <span data-ttu-id="071a6-163">Bu içerik paketlerini diğer raporları veya görsel öğeleri içerecek şekilde değiştirebilir ve içerik paketlerini analiz için Power BI.com kiracınıza yayınlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="071a6-163">You can modify these content packs so that they include other reports or visuals, and then publish the content packs to your Power BI.com tenant for analysis.</span></span> 

<span data-ttu-id="071a6-164">**Satınalma harcaması analizi** Power BI içeriğini LCS'deki Paylaşılan varlıklar kitaplığında bulabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="071a6-164">You can find the **Purchase spend analysis** Power BI content in the Shared assets library in LCS.</span></span> <span data-ttu-id="071a6-165">İçeriği indirmek ve kuruluşunuzda tümleştirmek hakkında daha fazla bilgi için bkz. [Microsoft LCS ve iş ortaklarınızdan Power BI içeriği](power-bi-content-microsoft-partners.md).</span><span class="sxs-lookup"><span data-stu-id="071a6-165">For more information about how to download the content and implement it in your organization, see [Power BI content in LCS from Microsoft and your partners](power-bi-content-microsoft-partners.md).</span></span> <span data-ttu-id="071a6-166">Power BI içeriğinin nasıl uygulanacağını gösteren bir demo izlemek için bakınız [Microsoft ve Dynamics Lifecycle Services ortaklarınızdan Power BI içeriği](https://mix.office.com/watch/9puyb1b2xs1w) Office Mix.</span><span class="sxs-lookup"><span data-stu-id="071a6-166">To watch a demo that shows how to implement the Power BI content, see the [Power BI content from Microsoft and your partners in Dynamics Lifecycle Services](https://mix.office.com/watch/9puyb1b2xs1w) Office Mix.</span></span>

<span data-ttu-id="071a6-167">Kullanmakta olduğunuz Dynamics 365 sürümü için geçerli **Satınalma harcaması analizi** içeriğini indirdiğinizden emin olun.</span><span class="sxs-lookup"><span data-stu-id="071a6-167">Be sure to download the **Purchase spend analysis** content that applies to the version of Dynamics 365 that you're using.</span></span>

> [!NOTE]
> <span data-ttu-id="071a6-168">Microsoft Dynamics 365 for Operations, 1611 sürümünü kullanıyorsanız, bu Power BI içeriği için KB 4011327 bir önkoşuldur:</span><span class="sxs-lookup"><span data-stu-id="071a6-168">If you're using Microsoft Dynamics 365 for Operations version 1611, KB 4011327 is a prerequisite for this Power BI content.</span></span> <span data-ttu-id="071a6-169">LCS'de oturum açtıktan sonra KB'ye buradan erişebilirsiniz: https://fix.lcs.dynamics.com/issue/results/?q=kb4011327.</span><span class="sxs-lookup"><span data-stu-id="071a6-169">After you sign in to LCS, you can access the KB at https://fix.lcs.dynamics.com/issue/results/?q=kb4011327.</span></span>

## <a name="data-model-and-entities"></a><span data-ttu-id="071a6-170">Veri modeli ve varlıklar</span><span class="sxs-lookup"><span data-stu-id="071a6-170">Data model and entities</span></span>
<span data-ttu-id="071a6-171">Aşağıdaki veriler **Satınalma harcaması analizi** Power BI içeriğindeki rapor sayfalarını doldurmak için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="071a6-171">The following data is used to fill the report pages in the **Purchase spend analysis** Power BI content.</span></span> <span data-ttu-id="071a6-172">Bu veri, Varlık mağazasında hazırlanan toplam ölçümler olarak sunulur.</span><span class="sxs-lookup"><span data-stu-id="071a6-172">This data is represented as aggregate measurements that are staged in the Entity store.</span></span> <span data-ttu-id="071a6-173">Varlık mağazası, analizler için en iyi duruma getirilmiş bir Microsoft SQL Sunucu veritabanıdır.</span><span class="sxs-lookup"><span data-stu-id="071a6-173">The Entity store is a Microsoft SQL Server database that is optimized for analytics.</span></span> <span data-ttu-id="071a6-174">Daha fazla bilgi için, bkz. [Varlık mağazası ile Power BI tümleştirmesine genel bakış](power-bi-integration-entity-store.md).</span><span class="sxs-lookup"><span data-stu-id="071a6-174">For more information, see [Overview of Power BI integration with Entity store](power-bi-integration-entity-store.md).</span></span>

<span data-ttu-id="071a6-175">Bu içerikteki toplam ölçümleri, Microsoft Dynamics AX 2012 ve Microsoft Dynamics AX 2012 R3'teki Satınalma Küpü'nde bulunan toplama ölçümlerin alt kümesidir.</span><span class="sxs-lookup"><span data-stu-id="071a6-175">The aggregate measurements in this content are the subset of aggregate measurements that were available in the Purchase Cube in Microsoft Dynamics AX 2012 and Microsoft Dynamics AX 2012 R3.</span></span> <span data-ttu-id="071a6-176">Varlık deposundaki küpün toplama ölçülerini hazırlamak için bu ölçümleri dağıtılabilir yapmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="071a6-176">To stage the cube’s aggregate measurements in the Entity store, you must make them deployable.</span></span> <span data-ttu-id="071a6-177">Daha fazla bilgi için, [Power BI ile Varlık deposu tümleştirmesine genel bakış](power-bi-integration-entity-store.md) bölümündeki toplanan ölçümleri Varlık Deposuna ekleme yordamına bakın.</span><span class="sxs-lookup"><span data-stu-id="071a6-177">For more information, see the procedure for staging aggregate measurements in the Entity store in [Overview of Power BI integration with Entity store](power-bi-integration-entity-store.md).</span></span> <span data-ttu-id="071a6-178">Aşağıda verilen önemli toplanan ölçümleri doğrudan Fatura satırları varlığından kullanılabilir ve içeriğin temeli olarak kullanılır.</span><span class="sxs-lookup"><span data-stu-id="071a6-178">The following key aggregate measurements are available directly from the Invoice lines entity and are used as the basis of the content.</span></span>

| <span data-ttu-id="071a6-179">Varlık</span><span class="sxs-lookup"><span data-stu-id="071a6-179">Entity</span></span>        | <span data-ttu-id="071a6-180">Önemli toplam ölçümler</span><span class="sxs-lookup"><span data-stu-id="071a6-180">Key aggregate measurements</span></span> | <span data-ttu-id="071a6-181">Veri kaynağı</span><span class="sxs-lookup"><span data-stu-id="071a6-181">Data source</span></span>                                 | <span data-ttu-id="071a6-182">Alan</span><span class="sxs-lookup"><span data-stu-id="071a6-182">Field</span></span>              | <span data-ttu-id="071a6-183">Açıklama</span><span class="sxs-lookup"><span data-stu-id="071a6-183">Description</span></span>                            |
|---------------|----------------------------|---------------------------------------------|--------------------|----------------------------------------|
| <span data-ttu-id="071a6-184">Fatura satırları</span><span class="sxs-lookup"><span data-stu-id="071a6-184">Invoice lines</span></span> | <span data-ttu-id="071a6-185">Satınalma</span><span class="sxs-lookup"><span data-stu-id="071a6-185">Purchase</span></span>                   | <span data-ttu-id="071a6-186">VendInvoiceTrans</span><span class="sxs-lookup"><span data-stu-id="071a6-186">VendInvoiceTrans</span></span>                            | <span data-ttu-id="071a6-187">SUM(LineAmountMST)</span><span class="sxs-lookup"><span data-stu-id="071a6-187">SUM(LineAmountMST)</span></span> | <span data-ttu-id="071a6-188">Muhasebe para birimi cinsinden tutar.</span><span class="sxs-lookup"><span data-stu-id="071a6-188">The amount in the accounting currency.</span></span> |

<span data-ttu-id="071a6-189">Aşağıdaki tablo içerikte Fatura satırları varlığından hesaplanan anahtar ölçümleri gösterir.</span><span class="sxs-lookup"><span data-stu-id="071a6-189">The following table shows the key measurements in the content that are calculated from the Invoice lines entity.</span></span>

| <span data-ttu-id="071a6-190">Ölçü</span><span class="sxs-lookup"><span data-stu-id="071a6-190">Measure</span></span>               | <span data-ttu-id="071a6-191">Hesaplama</span><span class="sxs-lookup"><span data-stu-id="071a6-191">Calculation</span></span>                                                                                         |
|-----------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="071a6-192">Geçerli yıldaki satınalma</span><span class="sxs-lookup"><span data-stu-id="071a6-192">Purchase current year</span></span> | <span data-ttu-id="071a6-193">Geçerli yıldaki satınalma = TOPLA('Fatura satırları'\[Satınalma\])</span><span class="sxs-lookup"><span data-stu-id="071a6-193">Purchase current year = SUM('Invoice lines'\[Purchase\])</span></span>                                            |
| <span data-ttu-id="071a6-194">Geçen yılki satınalma</span><span class="sxs-lookup"><span data-stu-id="071a6-194">Purchase last year</span></span>    | <span data-ttu-id="071a6-195">Geçen yılki satınalma = HESAPLA(TOPLA('Fatura satırları'\[Satınalma\]), SAMEPERIODLASTYEAR (Tarihler\[Tarih\])</span><span class="sxs-lookup"><span data-stu-id="071a6-195">Purchase last year = CALCULATE(SUM('Invoice lines'\[Purchase\]), SAMEPERIODLASTYEAR(Dates\[Date\]))</span></span> |
| <span data-ttu-id="071a6-196">Yıllara göre satınalmadaki büyüme</span><span class="sxs-lookup"><span data-stu-id="071a6-196">YOY purchase growth</span></span>   | <span data-ttu-id="071a6-197">Yıllara göre satınalmadaki büyüme = \[Geçerli yıldaki satınalma\] – \[Geçen yıldaki satınalma\]</span><span class="sxs-lookup"><span data-stu-id="071a6-197">YOY purchase growth = \[Purchase current year\] – \[Purchase last year\]</span></span>                            |

<span data-ttu-id="071a6-198">İçerikte bulunan aşağıdaki temel boyutları, daha büyük hassasiyet ve daha derin analiz bilgileri elde edebilmeniz amacıyla toplama ölçümlerini bölmek üzere filtre olarak kullanılır.</span><span class="sxs-lookup"><span data-stu-id="071a6-198">The following key dimensions in the content are used as filters to slice the aggregate measurements, so that you can achieve more granularity and gain deeper analytical insights.</span></span>

| <span data-ttu-id="071a6-199">Varlık</span><span class="sxs-lookup"><span data-stu-id="071a6-199">Entity</span></span>                 | <span data-ttu-id="071a6-200">Öznitelik örnekleri</span><span class="sxs-lookup"><span data-stu-id="071a6-200">Examples of attributes</span></span>                                |
|------------------------|-------------------------------------------------------|
| <span data-ttu-id="071a6-201">Satıcılar</span><span class="sxs-lookup"><span data-stu-id="071a6-201">Vendors</span></span>                | <span data-ttu-id="071a6-202">Satıcı grupları, Satıcı ülkesi veya bölgeleri, Satıcı adı</span><span class="sxs-lookup"><span data-stu-id="071a6-202">Vendor groups, Vendor country or regions, Vendor name</span></span> |
| <span data-ttu-id="071a6-203">Ürünler</span><span class="sxs-lookup"><span data-stu-id="071a6-203">Products</span></span>               | <span data-ttu-id="071a6-204">Ürün numarası, Ürün adı, Madde grupları adı</span><span class="sxs-lookup"><span data-stu-id="071a6-204">Product number, Product name, Item groups name</span></span>        |
| <span data-ttu-id="071a6-205">Tedarik kategorileri</span><span class="sxs-lookup"><span data-stu-id="071a6-205">Procurement categories</span></span> | <span data-ttu-id="071a6-206">Tedarik kategorisi, Tedarik kategorisi adları</span><span class="sxs-lookup"><span data-stu-id="071a6-206">Procurement category, Procurement category names</span></span>      |
| <span data-ttu-id="071a6-207">Tüzel kişilikler</span><span class="sxs-lookup"><span data-stu-id="071a6-207">Legal entities</span></span>         | <span data-ttu-id="071a6-208">Tüzel kişiliğin adı</span><span class="sxs-lookup"><span data-stu-id="071a6-208">Legal entity name</span></span>                                     |
| <span data-ttu-id="071a6-209">Tarihler</span><span class="sxs-lookup"><span data-stu-id="071a6-209">Dates</span></span>                  | <span data-ttu-id="071a6-210">Tarihler, Yıl denkleştirme</span><span class="sxs-lookup"><span data-stu-id="071a6-210">Dates, Year offset</span></span>                                    |

<span data-ttu-id="071a6-211">Varsayılan olarak, içerik geçerli takvim yılına ilişkin verileri gösterir.</span><span class="sxs-lookup"><span data-stu-id="071a6-211">By default, the content shows data for the current calendar year.</span></span> <span data-ttu-id="071a6-212">Ancak, rapor filtreleri bölümünden tarih filtresini değiştirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="071a6-212">However, you can change the date filter in the report filters section.</span></span> <span data-ttu-id="071a6-213">Şirket filtresini de değiştirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="071a6-213">You can also change the company filter.</span></span>

