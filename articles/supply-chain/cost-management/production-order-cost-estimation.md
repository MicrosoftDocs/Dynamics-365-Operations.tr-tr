---
title: "Üretim emri maliyet tahmini"
description: "Bu makalede, üretim maliyet tahmini hakkında bilgiler verilmektedir. Üretim maliyeti tahmini, bir maddeyi planlanan üretim emri miktarında üretmek için gereken tahmini malzeme ve kapasite tüketim maliyetlerini sağlar."
author: AndersGirke
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: BOMCalcTrans, InventCostTrans, ProdCalcTrans, ProdTableJour, ProdTableListPage
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 80633
ms.assetid: b4625d10-c852-4fda-b718-79df458de0d4
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: mguada
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 3ea3998014eb9ac2fd4610b5d52bd792d4f73869
ms.contentlocale: tr-tr
ms.lasthandoff: 11/03/2017

---

# <a name="production-order-cost-estimation"></a><span data-ttu-id="f83fa-104">Üretim emri maliyet tahmini</span><span class="sxs-lookup"><span data-stu-id="f83fa-104">Production order cost estimation</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="f83fa-105">Bu makalede, üretim maliyet tahmini hakkında bilgiler verilmektedir.</span><span class="sxs-lookup"><span data-stu-id="f83fa-105">This article provides information about production cost estimation.</span></span> <span data-ttu-id="f83fa-106">Üretim maliyeti tahmini, bir maddeyi planlanan üretim emri miktarında üretmek için gereken tahmini malzeme ve kapasite tüketim maliyetlerini sağlar.</span><span class="sxs-lookup"><span data-stu-id="f83fa-106">Production cost estimation provides the projected material and capacity consumption costs of producing an item in the planned production order quantity.</span></span> 

<span data-ttu-id="f83fa-107">Bir üretim emri oluşturduktan sonra üretim maliyetlerini tahmin etmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="f83fa-107">After you create a production order, you must estimate production costs.</span></span> <span data-ttu-id="f83fa-108">Bu tahminler sonraki planlama ve üretim süreçlerinde baz olarak kullanıldığı için, amaç, üretim süreci için madde ve rota tüketimini tahmin etmektir.</span><span class="sxs-lookup"><span data-stu-id="f83fa-108">The purpose is to estimate item and route consumption for the production process, because these estimates are used as the basis for subsequent scheduling and production processes.</span></span>

## <a name="production-cost-estimation"></a><span data-ttu-id="f83fa-109">Üretim maliyet tahmini</span><span class="sxs-lookup"><span data-stu-id="f83fa-109">Production cost estimation</span></span>
<span data-ttu-id="f83fa-110">Üretim maliyeti tahminlerinde aşağıdaki bilgiler temel alınır:</span><span class="sxs-lookup"><span data-stu-id="f83fa-110">Estimates of production costs are based on the following information:</span></span>

-   <span data-ttu-id="f83fa-111">Üretim emrindeki miktar</span><span class="sxs-lookup"><span data-stu-id="f83fa-111">The quantity on the production order</span></span>
-   <span data-ttu-id="f83fa-112">Üretim ürün reçetelerindeki (BOM) bileşenler</span><span class="sxs-lookup"><span data-stu-id="f83fa-112">The components on the production bills of materials (BOMs)</span></span>
-   <span data-ttu-id="f83fa-113">Üretim rotasındaki rota operasyonları</span><span class="sxs-lookup"><span data-stu-id="f83fa-113">The routing operations in the production route</span></span>
-   <span data-ttu-id="f83fa-114">Bileşenlere ve işlemlere uygulanan dolaylı maliyetler</span><span class="sxs-lookup"><span data-stu-id="f83fa-114">The indirect costs that apply to the components and operations</span></span>
-   <span data-ttu-id="f83fa-115">Hesaplama tarihi itibarıyla etkin maliyet verileri</span><span class="sxs-lookup"><span data-stu-id="f83fa-115">The active cost data as of the calculation date</span></span>

<span data-ttu-id="f83fa-116">Üretim ürün reçetelerinde bir hayali satır maddesi varsa, hesaplamalar hayali maddenin bileşenlerini ve rota operasyonlarını yansıtır.</span><span class="sxs-lookup"><span data-stu-id="f83fa-116">If there is a phantom line item on the production BOMs, the calculations reflect the phantom’s components and route operations.</span></span> <span data-ttu-id="f83fa-117">Tahmini maliyetleri, güncelleştirilen bilgileri yansıtacak şekilde yeniden hesaplamak için Tahmin görevini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="f83fa-117">You can use the estimation task to recalculate estimated costs so that they reflect updated information.</span></span> <span data-ttu-id="f83fa-118">Güncelleştirilen bilgiler, örneğin, üretim emri miktarı, üretim ürün reçetelerindeki bileşenler ve üretim rotasındaki rota operasyonları, bu bileşen ve faaliyetler için geçerli dolaylı maliyetler veya yeniden hesaplama tarihindeki etkin maliyet verilerindeki değişiklikler olabilir.</span><span class="sxs-lookup"><span data-stu-id="f83fa-118">For example, the updated information might be changes to the quantity on the production order, the components on the production BOMs, the routing operations in the production route, the indirect costs that apply to these components and operations, or the active cost data as of the recalculation date.</span></span> <span data-ttu-id="f83fa-119">Tahmini maliyet hesaplamaları, üretim maddesi için maliyet-artı-kar marjı yaklaşımına dayanan bir satış fiyatı önerir.</span><span class="sxs-lookup"><span data-stu-id="f83fa-119">The calculations of estimated cost also suggest a sales price for the production item, based on a cost-plus-markup approach.</span></span> <span data-ttu-id="f83fa-120">Tahmini maliyet hesaplamaları, isteğe bağlı olarak üretim emrine bağlı diğer üretim emirlerini yansıtan referans siparişlerine uygulanabilir.</span><span class="sxs-lookup"><span data-stu-id="f83fa-120">The calculations of estimated cost can optionally apply to reference orders that reflect other production orders that are linked to the production order.</span></span>

## <a name="view-the-estimated-costs"></a><span data-ttu-id="f83fa-121">Tahmin maliyetleri görüntüleyin</span><span class="sxs-lookup"><span data-stu-id="f83fa-121">View the estimated costs</span></span>
<span data-ttu-id="f83fa-122">Tahmini çalıştırdıktan sonra sonuçları **Fiyat hesaplaması** sayfasında görüntüleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="f83fa-122">After you run estimation, you can view the results on the **Price calculation** page.</span></span> <span data-ttu-id="f83fa-123">Tahmin, aşağıdaki değerleri hesaplar:</span><span class="sxs-lookup"><span data-stu-id="f83fa-123">The estimation calculates the following values:</span></span>

-   <span data-ttu-id="f83fa-124">**Üretim maliyeti** – Üretim maliyeti, tahminin üst satırıdır.</span><span class="sxs-lookup"><span data-stu-id="f83fa-124">**Production cost** – The production cost is the top line of the estimate.</span></span> <span data-ttu-id="f83fa-125">Üretim emrini çalıştırmanın toplam maliyetini ve üretim için toplam satış fiyatını gösterir.</span><span class="sxs-lookup"><span data-stu-id="f83fa-125">It shows the complete cost of running the production order and the total sales price for the production.</span></span> <span data-ttu-id="f83fa-126">Tahmindeki tüm maliyet satırlarının toplamıdır.</span><span class="sxs-lookup"><span data-stu-id="f83fa-126">It's the sum of all the cost lines on the estimate.</span></span>
-   <span data-ttu-id="f83fa-127">**Rota veya kaynak maliyetleri** – Rota veya kaynak maliyetleri, üretim operasyonlarının maliyetleridir.</span><span class="sxs-lookup"><span data-stu-id="f83fa-127">**Route or resource costs** – Route or resource costs are the costs for the production operations.</span></span> <span data-ttu-id="f83fa-128">Bunlar, kurulum süresi, çalıştırma süresi ve genel gider gibi öğelerin maliyetlerini içerir.</span><span class="sxs-lookup"><span data-stu-id="f83fa-128">They include the cost of elements such as setup time, run time, and overhead.</span></span>
-   <span data-ttu-id="f83fa-129">**Malzeme maliyetleri** – Maddeyi üretmek için gereken ürün reçetesi bileşenlerinin maliyetleri ve fiyatlarıdır.</span><span class="sxs-lookup"><span data-stu-id="f83fa-129">**Material costs** – Material costs are the costs and prices of the BOM components that are required in order to produce the item.</span></span> <span data-ttu-id="f83fa-130">Bu maliyetler önceden belirlenmiş ve sisteme girilmiştir.</span><span class="sxs-lookup"><span data-stu-id="f83fa-130">These costs have previously been established and entered into the system.</span></span>

## <a name="other-uses-of-cost-estimation"></a><span data-ttu-id="f83fa-131">Maliyet tahmininin diğer kullanımları</span><span class="sxs-lookup"><span data-stu-id="f83fa-131">Other uses of cost estimation</span></span>
<span data-ttu-id="f83fa-132">Maliyet tahmini, aşağıdaki bilgileri de sağlar:</span><span class="sxs-lookup"><span data-stu-id="f83fa-132">A cost estimate also provides the following information:</span></span>

-   <span data-ttu-id="f83fa-133">Anlamlı fiyat teklifleri</span><span class="sxs-lookup"><span data-stu-id="f83fa-133">Meaningful price quotations</span></span>
-   <span data-ttu-id="f83fa-134">Emrin karlılık tahminleri</span><span class="sxs-lookup"><span data-stu-id="f83fa-134">Estimates of the profitability of the order</span></span>
-   <span data-ttu-id="f83fa-135">Hammadde kullanım tahminleri</span><span class="sxs-lookup"><span data-stu-id="f83fa-135">Estimates of raw material usage</span></span>
-   <span data-ttu-id="f83fa-136">Önceki üretimlerin maliyet bilgilerinin karşılaştırılması</span><span class="sxs-lookup"><span data-stu-id="f83fa-136">Comparisons of cost information from previous productions</span></span>
-   <span data-ttu-id="f83fa-137">Bütçe ve tahmin bilgileri</span><span class="sxs-lookup"><span data-stu-id="f83fa-137">Budget and forecasting information</span></span>
-   <span data-ttu-id="f83fa-138">Belirli bir maliyeti korumak için gereken üretim boyutu tahminleri</span><span class="sxs-lookup"><span data-stu-id="f83fa-138">Estimates of the production size that is required in order to maintain a particular cost</span></span>





