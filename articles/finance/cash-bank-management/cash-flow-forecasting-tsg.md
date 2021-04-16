---
title: Nakit akışı tahmin kurulumu ile ilgili sorunları giderme
description: Bu konuda nakit akışı tahminini yapılandırdığınızda karşılaşabileceğiniz sorulara yanıtlar verilmiştir. Nakit akışı kurulumu, nakit akışı güncelleştirmeleri ve nakit akışı Power BI hakkında sık sorulan soruları (SSS) ele alır.
author: panolte
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerCovParameters
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: panolte
ms.search.validFrom: 2020-12-30
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 7b4760d7a0d0c14e2df8df20c2f81ec41e077cc0
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/01/2021
ms.locfileid: "5827326"
---
# <a name="troubleshoot-cash-flow-forecasting-setup"></a><span data-ttu-id="abe99-104">Nakit akışı tahmin kurulumu ile ilgili sorunları giderme</span><span class="sxs-lookup"><span data-stu-id="abe99-104">Troubleshoot cash flow forecasting setup</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="abe99-105">Bu konuda nakit akışı tahminini yapılandırdığınızda karşılaşabileceğiniz sorulara yanıtlar verilmiştir.</span><span class="sxs-lookup"><span data-stu-id="abe99-105">This topic provides answers to questions that you might have when you configure cash flow forecasting.</span></span> <span data-ttu-id="abe99-106">Nakit akışı kurulumu, nakit akışı güncelleştirmeleri ve nakit akışı Power BI hakkında sık sorulan soruları (SSS) ele alır.</span><span class="sxs-lookup"><span data-stu-id="abe99-106">It addresses frequently asked questions (FAQ) about the setup for cash flow, updates to cash flow, and cash flow Power BI.</span></span>

## <a name="why-is-cash-flow-shown-for-only-one-legal-entity"></a><span data-ttu-id="abe99-107">Neden yalnızca bir tüzel kişilik için nakit akışı gösteriliyor?</span><span class="sxs-lookup"><span data-stu-id="abe99-107">Why is cash flow shown for only one legal entity?</span></span>

<span data-ttu-id="abe99-108">Nakit akışı tahmini tüzel kişilik başına yapılandırılır ve hesaplanır.</span><span class="sxs-lookup"><span data-stu-id="abe99-108">Cash flow forecasting is configured and calculated per legal entity.</span></span> <span data-ttu-id="abe99-109">Finance Insights'taki Power BI raporları ve nakit akışı tahminleri özelliği sonuçları gösterir.</span><span class="sxs-lookup"><span data-stu-id="abe99-109">Power BI reports and the cash flow forecasts capability in Finance insights show the results.</span></span>

<span data-ttu-id="abe99-110">Tahmin görmek istediğiniz her tüzel kişilik için nakit akışı tahmini ayarlanmalıdır.</span><span class="sxs-lookup"><span data-stu-id="abe99-110">Cash flow forecasting must be set up for each legal entity that you want to see a forecast for.</span></span> <span data-ttu-id="abe99-111">Tüm tüzel kişiliklerinizde nakit akışı tahmini yapılandırmasını inceleyin.</span><span class="sxs-lookup"><span data-stu-id="abe99-111">Review the configuration of cash flow forecasting in all your legal entities.</span></span> <span data-ttu-id="abe99-112">Alternatif olarak, nakit akışı tahmini için tüm tüzel kişiliklerin yapılandırmasını inceleyin ve istediğiniz gibi ayarlandıklarından emin olun.</span><span class="sxs-lookup"><span data-stu-id="abe99-112">Alternatively, review the configuration of all the legal entities for cash flow forecasting, and make sure that they are set as you intended.</span></span>

## <a name="why-doesnt-power-bi-show-all-the-cash-flow-data"></a><span data-ttu-id="abe99-113">Power BI neden tüm nakit akışı verilerini göstermiyor?</span><span class="sxs-lookup"><span data-stu-id="abe99-113">Why doesn't Power BI show all the cash flow data?</span></span>

<span data-ttu-id="abe99-114">Nakit akışı tahminlerinin Power BI görünümlerinde görünebilmesi için birkaç adımın tamamlanması gerekir.</span><span class="sxs-lookup"><span data-stu-id="abe99-114">Several steps must be completed before cash flow forecasts can appear in Power BI views.</span></span> <span data-ttu-id="abe99-115">Aşağıdaki denetim listesini inceleyin ve her adımın tamamlandığından emin olun:</span><span class="sxs-lookup"><span data-stu-id="abe99-115">Review the following checklist, and make sure that every step has been completed:</span></span>

- <span data-ttu-id="abe99-116">Her tüzel kişilik için nakit akışını ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="abe99-116">Set up cash flow for each legal entity.</span></span>
- <span data-ttu-id="abe99-117">Genel muhasebe parametrelerinde, sistem para birimini ve sistem döviz kuru türünü ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="abe99-117">In General ledger parameters, set the system currency and the system exchange rate type.</span></span>
- <span data-ttu-id="abe99-118">Genel muhasebe muhasebe para birimini ve döviz kuru türünü ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="abe99-118">Set the ledger accounting currency and the exchange rate type.</span></span>
- <span data-ttu-id="abe99-119">Hareket para birimi ile muhasebe para birimi arasında döviz kurları girin.</span><span class="sxs-lookup"><span data-stu-id="abe99-119">Enter exchange rates between the transaction currency and the accounting currency.</span></span>
- <span data-ttu-id="abe99-120">Muhasebe para birimi ile sistem para birimi arasında döviz kurları girin.</span><span class="sxs-lookup"><span data-stu-id="abe99-120">Enter exchange rates between the accounting currency and the system currency.</span></span>
- <span data-ttu-id="abe99-121">Muhasebe para birimi ile her banka para birimi arasında döviz kurları girin.</span><span class="sxs-lookup"><span data-stu-id="abe99-121">Enter exchange rates between the accounting currency and each bank currency.</span></span>

## <a name="why-did-cash-flow-power-bi-work-in-previous-versions-but-is-now-blank"></a><span data-ttu-id="abe99-122">Nakit akışı Power BI neden önceki sürümlerde çalışıyordu ancak şimdi boş?</span><span class="sxs-lookup"><span data-stu-id="abe99-122">Why did cash flow Power BI work in previous versions but is now blank?</span></span>

<span data-ttu-id="abe99-123">Varlık deposundaki "Nakit akışı ölçümü V2" ve "LedgerCovLiquidityMeasurement" ölçümlerinin yapılandırıldığını doğrulayın.</span><span class="sxs-lookup"><span data-stu-id="abe99-123">Verify that the "Cash flow measure V2" and "LedgerCovLiquidityMeasurement" measurements from Entity store have been configured.</span></span> <span data-ttu-id="abe99-124">Bir varlık deposuyla nasıl çalışılacağı hakkında daha fazla bilgi için bkz. [Varlık deposu ile Power BI tümleştirmesi](../../fin-ops-core/dev-itpro/analytics/power-bi-integration-entity-store.md).</span><span class="sxs-lookup"><span data-stu-id="abe99-124">For more information about how to work with data in Entity store, see [Power BI integration with Entity store](../../fin-ops-core/dev-itpro/analytics/power-bi-integration-entity-store.md).</span></span> <span data-ttu-id="abe99-125">Power BI içeriğini görüntülemek için gerekli tüm adımların tamamlandığını doğrulayın.</span><span class="sxs-lookup"><span data-stu-id="abe99-125">Verify that all the steps that are required to view Power BI content have been completed.</span></span> <span data-ttu-id="abe99-126">Daha fazla bilgi için bkz. [Nakde genel bakış Power BI içeriği](Cash-Overview-Power-BI-content.md).</span><span class="sxs-lookup"><span data-stu-id="abe99-126">For more information, see [Cash overview Power BI content](Cash-Overview-Power-BI-content.md).</span></span>

## <a name="have-the-entity-store-entities-been-refreshed"></a><span data-ttu-id="abe99-127">Varlık deposu varlıkları yenilendi mi?</span><span class="sxs-lookup"><span data-stu-id="abe99-127">Have the Entity store entities been refreshed?</span></span>

<span data-ttu-id="abe99-128">Verilerin güncel ve doğru olduğundan emin olmak için varlıklarınızı düzenli aralıklarla yenilemeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="abe99-128">You must periodically refresh your entities to ensure that the data is current and accurate.</span></span> <span data-ttu-id="abe99-129">Belirli bir varlığı el ile yenilemek için **Sistem yönetimi \> Kurulum \> Varlık deposu**'na gidin, varlığı seçin ve sonra **Yenile**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="abe99-129">To manually refresh a specific entity, go to **System administration \> Setup \> Entity store**, select the entity, and then select **Refresh**.</span></span> <span data-ttu-id="abe99-130">Veriler otomatik olarak da güncelleştirilebilir.</span><span class="sxs-lookup"><span data-stu-id="abe99-130">The data can also be updated automatically.</span></span> <span data-ttu-id="abe99-131">**Varlık deposu** sayfasında, **Otomatik yenileme etkin** seçeneğini **Evet** olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="abe99-131">On the **Entity store** page, set the **Automatic refresh enabled** option to **Yes**.</span></span>

## <a name="which-calculation-method-should-be-used-when-calculating-cash-flow-forecasts"></a><span data-ttu-id="abe99-132">Nakit akışı tahminleri hesaplanırken hangi hesaplama yöntemi kullanılmalıdır?</span><span class="sxs-lookup"><span data-stu-id="abe99-132">Which calculation method should be used when calculating cash flow forecasts?</span></span>

<span data-ttu-id="abe99-133">Nakit akışı tahmin hesaplama yönteminde iki önemli seçim seçeneği vardır.</span><span class="sxs-lookup"><span data-stu-id="abe99-133">The Cash flow forecast calculation method has two important selection options.</span></span> <span data-ttu-id="abe99-134">**Yeni** seçeneği, yeni belgeler ve son toplu işin çalıştırılmasından bu yana değişen belgeler için nakit akışı tahminlerini hesaplayacaktır.</span><span class="sxs-lookup"><span data-stu-id="abe99-134">The **New** option will calculate cash flow forecasts for new documents and documents that have changed since the last batch job ran.</span></span> <span data-ttu-id="abe99-135">Bu seçenek, belgelerin daha küçük bir alt kümesini işlediği için daha hızlı çalışma eğilimindedir.</span><span class="sxs-lookup"><span data-stu-id="abe99-135">This option tends to run faster because it processes a smaller subset of documents.</span></span> <span data-ttu-id="abe99-136">**Toplam** seçeneği, sistemdeki her belge için nakit akışı tahminlerini yeniden hesaplar.</span><span class="sxs-lookup"><span data-stu-id="abe99-136">The **Total** option will recalculate cash flow forecasts for every document in the system.</span></span> <span data-ttu-id="abe99-137">Bu seçenekte daha fazla iş olduğundan tamamlanması daha fazla zaman alır.</span><span class="sxs-lookup"><span data-stu-id="abe99-137">This option takes more time because it has more work to complete.</span></span>

### <a name="how-do-i-improve-the-performance-of-the-cash-flow-forecasting-recurring-batch-job"></a><span data-ttu-id="abe99-138">Nakit akışı tahmini yinelenen toplu iş ile ilgili performansı nasıl artırabilirim?</span><span class="sxs-lookup"><span data-stu-id="abe99-138">How do I improve the performance of the cash flow forecasting recurring batch job?</span></span>

<span data-ttu-id="abe99-139">Nakit akışı tahmininizi her gün, **yeni** hesaplama yöntemini kullanarak, yoğun olmayan saatlerde bir kez çalıştırmanız önerilir.</span><span class="sxs-lookup"><span data-stu-id="abe99-139">We recommend running your cash flow forecast once each day during the off-peak hours using the **New** calculation method.</span></span> <span data-ttu-id="abe99-140">Bu yaklaşımı, haftada altı gün kullanmanızı öneririz.</span><span class="sxs-lookup"><span data-stu-id="abe99-140">We recommend using this approach six days per week.</span></span> <span data-ttu-id="abe99-141">Daha sonra, haftada bir en az faaliyet bulunan günde **toplam** hesaplama yöntemini kullanarak bir nakit akışı tahmini çalıştırın.</span><span class="sxs-lookup"><span data-stu-id="abe99-141">Then run a cash flow forecast once each week using the **Total** calculation method on the day with the least amount of activity.</span></span>

[!INCLUDE[footer-include](../../includes/footer-banner.md)]

