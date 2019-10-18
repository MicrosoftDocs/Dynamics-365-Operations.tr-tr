---
title: Temel tahminde manüel ayarlamalar yapma
description: Bu konuda bir temel tahminde manüel ayarlamalar yapma ve tahminin ayrıntılarını görüntüleme yolları açıklanmıştır.
author: roxanadiaconu
manager: AnnBe
ms.date: 11/02/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqDemPlanForecastViewer
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 72704
ms.assetid: e7c5d44e-07bc-40b1-a4b3-8ba46483ef9e
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: df9692dc168e9efb653b20c677cd6e3bb0bd8756
ms.sourcegitcommit: 2460d0da812c45fce67a061386db52e0ae46b0f3
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/30/2019
ms.locfileid: "2250726"
---
# <a name="make-manual-adjustments-to-the-baseline-forecast"></a><span data-ttu-id="b1736-103">Temel tahminde manüel ayarlamalar yapma</span><span class="sxs-lookup"><span data-stu-id="b1736-103">Make manual adjustments to the baseline forecast</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b1736-104">Bu konuda bir temel tahminde manüel ayarlamalar yapma ve tahminin ayrıntılarını görüntüleme yolları açıklanmıştır.</span><span class="sxs-lookup"><span data-stu-id="b1736-104">This topic explains how you can make manual adjustments to a baseline forecast and view details of the forecast.</span></span> 

<span data-ttu-id="b1736-105">Manüel ayarlamalar yapmadan önce, çeşitli sayfalarda bulunan birkaç kavramı anlamanız önemlidir.</span><span class="sxs-lookup"><span data-stu-id="b1736-105">Before you make manual adjustments, it's important that you understand a few concepts on various pages.</span></span>

## <a name="grid-on-the-adjusted-demand-forecast-page"></a><span data-ttu-id="b1736-106">Ayarlanan talep tahmini sayfası kılavuzu</span><span class="sxs-lookup"><span data-stu-id="b1736-106">Grid on the Adjusted demand forecast page</span></span>
<span data-ttu-id="b1736-107">**Ayarlanmış talep tahmini** sayfası aşağıdaki yapıya sahip bir kılavuz içerir:</span><span class="sxs-lookup"><span data-stu-id="b1736-107">The **Adjusted demand forecast** page includes a grid that has the following structure:</span></span>

-   <span data-ttu-id="b1736-108">İlk sütunda tahminin oluşturulma amacı olan maddeler, madde tahsisat anahtarları, şirketler vb. gösterilir.</span><span class="sxs-lookup"><span data-stu-id="b1736-108">The first column shows the items, item allocation keys, companies, and so on, that the forecast has been generated for.</span></span> <span data-ttu-id="b1736-109">Sayfanın alt başlığı kılavuzda gösterilen geçerli tahmin boyutları için bir açıklama sağlar.</span><span class="sxs-lookup"><span data-stu-id="b1736-109">The subtitle of the page provides a description of the current forecast dimensions that are shown in the grid.</span></span> <span data-ttu-id="b1736-110">Örneğin, sayfanın alt başlığı **Şirket / Tesis / Madde tahsisat anahtarı** ve kılavuzdaki satır başlıklarından biri **USMF / 1 / D\_Alloc** ise, bu satır USMF şirketi, 1. tesis ve **D\_Alloc** madde tahsisat anahtarına ilişkin tahmini gösterir.</span><span class="sxs-lookup"><span data-stu-id="b1736-110">For example, if the subtitle of the page is **Company / Site / Item allocation key**, and one of the row headers in the grid is **USMF / 1 / D\_Alloc**, that row shows the forecast for the USMF company, site 1, and the **D\_Alloc** item allocation key.</span></span>
-   <span data-ttu-id="b1736-111">Sonraki sütunlar tahminin oluşturulma amacı olan tahmin aralıklarını temsil eder.</span><span class="sxs-lookup"><span data-stu-id="b1736-111">Subsequent columns represent the forecast buckets that the forecast has been generated for.</span></span> <span data-ttu-id="b1736-112">Her sütun başlığı sütunun gösterdiği tahmin aralığının ilk tarihidir.</span><span class="sxs-lookup"><span data-stu-id="b1736-112">Each column header is the first date of the forecast bucket that the column shows.</span></span>
-   <span data-ttu-id="b1736-113">Hücrelerdeki değerler, o özel tahmin aralığında bir maddeyi, madde tahsisat anahtarını, vb. temsil eder.</span><span class="sxs-lookup"><span data-stu-id="b1736-113">The values in the cells represent the forecast for one item, item allocation key, and so on, for that specific forecast bucket.</span></span>

## <a name="forecast-aggregation-and-de-aggregation"></a><span data-ttu-id="b1736-114">Tahmin toplama ve toplamayı kaldırma</span><span class="sxs-lookup"><span data-stu-id="b1736-114">Forecast aggregation and de-aggregation</span></span>
<span data-ttu-id="b1736-115">Sayfanın alt başlığı tahmin toplama düzeyini gösterir.</span><span class="sxs-lookup"><span data-stu-id="b1736-115">The subtitle of the page shows the level of forecast aggregation.</span></span> 

<span data-ttu-id="b1736-116">Örneğin, sayfanın alt başlığı **Şirket / Tesis / Tahsisat anahtarı / Madde numarası / Renk / Boyut / Yapılandırma / Stil** ise, hiç tahmin toplama yoktur ve tahmin madde ve boyutları düzeyinde gösterilir.</span><span class="sxs-lookup"><span data-stu-id="b1736-116">For example, if the subtitle of the page is **Company / Site / Allocation key / Item number / Color / Size / Configuration / Style**, there is no forecast aggregation, and the forecast is shown at the level of the item and its dimensions.</span></span> <span data-ttu-id="b1736-117">Toplamı değiştirmek için, uygulama menüsünden açabileceğiniz **Tahmin boyutlarını değiştir** sayfasını kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="b1736-117">To change the aggregation, use the **Change forecast dimensions** page, which you can open from the application menu.</span></span> 

<span data-ttu-id="b1736-118">Tahmini değiştirmek için, kullanılabilen hücrelerden birine tıklayın ve ayarlanmış tahmin değeri yazın.</span><span class="sxs-lookup"><span data-stu-id="b1736-118">To modify the forecast, click in any of the cells that are available, and type the adjusted forecast value.</span></span> <span data-ttu-id="b1736-119">Düzenlenen hücre, gösterilen tahminin talep tahmini hizmetinin oluşturduğu tahmin olmadığını, ancak manüel olarak ayarlandığını gösterecek şekilde kalınlaşır.</span><span class="sxs-lookup"><span data-stu-id="b1736-119">The edited cell immediately becomes bold to indicate that the forecast that it shows isn't the forecast that the demand forecasting service created, but has been manually adjusted.</span></span> 

<span data-ttu-id="b1736-120">Sayfanın daha toplanmış veriler göstermesini sağlamak için toplamı değiştirirseniz, toplanmış tahmini oluşturan ayrı ayrı tahmin satırlarını görmek üzere , **Talep tahmin satırları** sayfasını kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="b1736-120">If you change the aggregation to make the page show more aggregated data, you can use the **Demand forecast lines** page to see the individual forecast lines that make up the aggregated forecast.</span></span> 

<span data-ttu-id="b1736-121">Örneğin, tahmini madde düzeyinde oluşturdunuz, ancak bu maddeye talebin bir promosyon veya başka benzer bir etkinlik nedeniyle tüm tesiste artacağını biliyorsunuz.</span><span class="sxs-lookup"><span data-stu-id="b1736-121">For example, you've generated the forecast at the item level, but you know that the demand for this item will increase across all sites because of a promotion or another similar event.</span></span> <span data-ttu-id="b1736-122">Bu durumda, toplamı **Tahmin boyutlarını değiştir** sayfasındaki **Şirket / Madde tahsisat anahtarı / Madde** seçeneğine ayarlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="b1736-122">In this case, you can set the aggregation to **Company / Item allocation key / Item** on the **Change forecast dimensions** page.</span></span> <span data-ttu-id="b1736-123">Tüm tesislerde maddeye ilişkin global tahmini **Ayarlanmış talep tahmini** kılavuzunda ayarlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="b1736-123">You can adjust the global forecast for the item across all sites in the **Adjusted demand forecast** grid.</span></span> <span data-ttu-id="b1736-124">Tüm tesisler arasında yaptığınız değişikliğin etkisini görmek için, **Talep tahmin satırları** sayfasını açın.</span><span class="sxs-lookup"><span data-stu-id="b1736-124">To see the effect of your change across all sites, open the **Demand forecast lines** page.</span></span> <span data-ttu-id="b1736-125">Bu sayfada, her tesise ait madde, ayarlanan tahmin miktarı ve orijinal tahmin miktarı için bir satır görürsünüz.</span><span class="sxs-lookup"><span data-stu-id="b1736-125">On this page, you will see one line for the item for each site, the adjusted forecast quantity, and the original forecast quantity.</span></span> 

<span data-ttu-id="b1736-126">Tahmin edilen miktar ayarlaması toplanmış bir düzeyde yapıldığında, sistem değişikliği toplamı oluşturan satırlar arasında dağıtmak için ağırlıklı tahsisatı kullanır.</span><span class="sxs-lookup"><span data-stu-id="b1736-126">When the adjustment of the forecasted quantity is made at an aggregated level, the system uses weighted allocation to distribute the change among the lines that create the aggregation.</span></span> 

<span data-ttu-id="b1736-127">Ayrıca manüel ayarlamaları **Talep tahmin satırları** sayfasında, toplamı kaldırma kılavuzundaki **Toplam miktar** değerini veya **Miktar** hücrelerini değiştirerek de yapabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="b1736-127">You can also make manual adjustments on the **Demand forecast lines** page, by modifying either the **Total quantity** value or the **Quantity** cells in the de-aggregation grid.</span></span>

## <a name="viewing-details-of-the-forecast"></a><span data-ttu-id="b1736-128">Tahminin ayrıntılarını görüntüleme</span><span class="sxs-lookup"><span data-stu-id="b1736-128">Viewing details of the forecast</span></span>
<span data-ttu-id="b1736-129">Tahmin hakkında daha fazla bilgi görüntülemek için **Talep tahmini ayrıntıları** sayfasını açabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="b1736-129">You can open the **Demand forecast details** page to view more information about the forecast.</span></span> 

<span data-ttu-id="b1736-130">**Talep tahmini ayrıntıları** sayfası aşağıdaki bilgileri grafik ve tablo biçimlerinde gösterir:</span><span class="sxs-lookup"><span data-stu-id="b1736-130">The **Demand forecast details** page shows the following information in graphical and tabular formats:</span></span>

-   <span data-ttu-id="b1736-131">Tahmin öngörülerinin temel alındığı geçmiş talep.</span><span class="sxs-lookup"><span data-stu-id="b1736-131">The historical demand that the forecast predictions are based on.</span></span>
-   <span data-ttu-id="b1736-132">Master planlama tarafından kullanılan geçerli tahmin.</span><span class="sxs-lookup"><span data-stu-id="b1736-132">The current forecast that is used by Master planning.</span></span>
-   <span data-ttu-id="b1736-133">Yeni talep tahmin değerleri ve bu değerlerin manüel olarak ayarlandığı tutarlar.</span><span class="sxs-lookup"><span data-stu-id="b1736-133">The new demand forecast values and the amounts they have been manually adjusted by.</span></span>
-   <span data-ttu-id="b1736-134">Tahmin edilen değerler için güven aralığı.</span><span class="sxs-lookup"><span data-stu-id="b1736-134">The confidence interval for the forecasted values.</span></span>
-   <span data-ttu-id="b1736-135">Tahmin oluşturmak için kullanılan tahmin modeli.</span><span class="sxs-lookup"><span data-stu-id="b1736-135">The forecast model that was used to generate the forecast.</span></span> <span data-ttu-id="b1736-136">Toplanan verileri görüntülüyorsanız, toplanan saat dizisi için kullanılan tüm yöntemlerin listesini görürsünüz.</span><span class="sxs-lookup"><span data-stu-id="b1736-136">If you're viewing aggregated data, you will see the list of all the methods that were used for all the aggregated time series.</span></span>
-   <span data-ttu-id="b1736-137">Dahili model doğruluğu (MAPE).</span><span class="sxs-lookup"><span data-stu-id="b1736-137">The internal model accuracy (MAPE).</span></span> <span data-ttu-id="b1736-138">Tahmin doğruluğu hakkında daha fazla bilgi için, bkz. [Tahmin doğruluğunu izleme](monitor-forecast-accuracy.md).</span><span class="sxs-lookup"><span data-stu-id="b1736-138">For more information about forecast accuracy, see [Monitoring forecast accuracy](monitor-forecast-accuracy.md).</span></span>

<span data-ttu-id="b1736-139">**Notlar:**</span><span class="sxs-lookup"><span data-stu-id="b1736-139">**Notes:**</span></span>

-   <span data-ttu-id="b1736-140">Sayfanın **tahmin** bölümünde görülen güven aralığı, güven aralığı üst sınırı ile güven aralığı alt sınırı arasındaki farkı temsil eder.</span><span class="sxs-lookup"><span data-stu-id="b1736-140">The confidence interval that appears in the **Forecast** section of the page represents the difference between the confidence interval upper limit and the confidence interval lower limit.</span></span> <span data-ttu-id="b1736-141">Üst ve alt sınırların değerlerini görmek için, **Grafiksel olarak geçmiş talep ve tahmin** bölümündeki grafikte gezinin.</span><span class="sxs-lookup"><span data-stu-id="b1736-141">To see the values for the upper and lower limits, hover over the chart in the **Historical demand and forecast graphically** section.</span></span>
-   <span data-ttu-id="b1736-142">Talep tahmini Microsoft Azure Machine Learning hizmetini kullanırsanız oluşturulan tahminde olması gereken güven düzeyi yüzdesini belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="b1736-142">If you use the Demand forecasting Microsoft Azure Machine Learning service, you can specify the confidence level percentage that the forecast that is generated should have.</span></span> <span data-ttu-id="b1736-143">Güven aralığı talep tahmini için iyi tahminler olarak hareket eden bir değerler aralığından oluşur.</span><span class="sxs-lookup"><span data-stu-id="b1736-143">A confidence interval consists of a range of values that act as good estimates for the demand forecast.</span></span> <span data-ttu-id="b1736-144">Yüzde 95'lik bir güven düzeyi yüzdesi, talep tahmininin güven aralığı sınırlarının dışına çıkma konusunda yüzde 5'lik bir risk bulunduğunu gösterir.</span><span class="sxs-lookup"><span data-stu-id="b1736-144">A 95-percent confidence level percentage indicates that there is a 5-percent risk that the demand forecast falls outside the confidence interval range.</span></span>

<span data-ttu-id="b1736-145">Manüel ayarlamaları, **Talep tahmini ayrıntıları** sayfasında, **Tahmin** bölümündeki **Tahmin** satırında belirtilen değerleri değiştirerek de yapabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="b1736-145">You can also make manual adjustments to the forecast on the **Demand forecast details** page, by modifying the values in the **Forecast** row in the **Forecast** section.</span></span>

<a name="additional-resources"></a><span data-ttu-id="b1736-146">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="b1736-146">Additional resources</span></span>
--------

[<span data-ttu-id="b1736-147">Tahmin doğruluğunu izleme</span><span class="sxs-lookup"><span data-stu-id="b1736-147">Monitoring forecast accuracy</span></span>](monitor-forecast-accuracy.md)

[<span data-ttu-id="b1736-148">İstatistik temel tahmin oluşturma</span><span class="sxs-lookup"><span data-stu-id="b1736-148">Generating a statistical baseline forecast</span></span>](generate-statistical-baseline-forecast.md)



