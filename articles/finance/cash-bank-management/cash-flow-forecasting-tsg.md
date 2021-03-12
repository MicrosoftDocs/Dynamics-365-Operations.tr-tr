---
title: Nakit akışı tahmin kurulumu ile ilgili sorunları giderme
description: Bu konuda nakit akışı tahminini yapılandırdığınızda karşılaşabileceğiniz sorulara yanıtlar verilmiştir. Nakit akışı kurulumu, nakit akışı güncelleştirmeleri ve nakit akışı Power BI hakkında sık sorulan soruları (SSS) ele alır.
author: panolte
manager: AnnBe
ms.date: 12/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerCovParameters
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: panolte
ms.search.validFrom: 2020-12-30
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 89eb2f1bcfc73a6a7171a275532b2356e858e87c
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/15/2021
ms.locfileid: "4985299"
---
# <a name="troubleshoot-cash-flow-forecasting-setup"></a><span data-ttu-id="4c242-104">Nakit akışı tahmin kurulumu ile ilgili sorunları giderme</span><span class="sxs-lookup"><span data-stu-id="4c242-104">Troubleshoot cash flow forecasting setup</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="4c242-105">Bu konuda nakit akışı tahminini yapılandırdığınızda karşılaşabileceğiniz sorulara yanıtlar verilmiştir.</span><span class="sxs-lookup"><span data-stu-id="4c242-105">This topic provides answers to questions that you might have when you configure cash flow forecasting.</span></span> <span data-ttu-id="4c242-106">Nakit akışı kurulumu, nakit akışı güncelleştirmeleri ve nakit akışı Power BI hakkında sık sorulan soruları (SSS) ele alır.</span><span class="sxs-lookup"><span data-stu-id="4c242-106">It addresses frequently asked questions (FAQ) about the setup for cash flow, updates to cash flow, and cash flow Power BI.</span></span>

## <a name="why-is-cash-flow-shown-for-only-one-legal-entity"></a><span data-ttu-id="4c242-107">Neden yalnızca bir tüzel kişilik için nakit akışı gösteriliyor?</span><span class="sxs-lookup"><span data-stu-id="4c242-107">Why is cash flow shown for only one legal entity?</span></span>

<span data-ttu-id="4c242-108">Nakit akışı tahmini tüzel kişilik başına yapılandırılır ve hesaplanır.</span><span class="sxs-lookup"><span data-stu-id="4c242-108">Cash flow forecasting is configured and calculated per legal entity.</span></span> <span data-ttu-id="4c242-109">Finance Insights'taki Power BI raporları ve nakit akışı tahminleri özelliği sonuçları gösterir.</span><span class="sxs-lookup"><span data-stu-id="4c242-109">Power BI reports and the cash flow forecasts capability in Finance insights show the results.</span></span>

<span data-ttu-id="4c242-110">Tahmin görmek istediğiniz her tüzel kişilik için nakit akışı tahmini ayarlanmalıdır.</span><span class="sxs-lookup"><span data-stu-id="4c242-110">Cash flow forecasting must be set up for each legal entity that you want to see a forecast for.</span></span> <span data-ttu-id="4c242-111">Tüm tüzel kişiliklerinizde nakit akışı tahmini yapılandırmasını inceleyin.</span><span class="sxs-lookup"><span data-stu-id="4c242-111">Review the configuration of cash flow forecasting in all your legal entities.</span></span> <span data-ttu-id="4c242-112">Alternatif olarak, nakit akışı tahmini için tüm tüzel kişiliklerin yapılandırmasını inceleyin ve istediğiniz gibi ayarlandıklarından emin olun.</span><span class="sxs-lookup"><span data-stu-id="4c242-112">Alternatively, review the configuration of all the legal entities for cash flow forecasting, and make sure that they are set as you intended.</span></span>

## <a name="why-doesnt-power-bi-show-all-the-cash-flow-data"></a><span data-ttu-id="4c242-113">Power BI neden tüm nakit akışı verilerini göstermiyor?</span><span class="sxs-lookup"><span data-stu-id="4c242-113">Why doesn't Power BI show all the cash flow data?</span></span>

<span data-ttu-id="4c242-114">Nakit akışı tahminlerinin Power BI görünümlerinde görünebilmesi için birkaç adımın tamamlanması gerekir.</span><span class="sxs-lookup"><span data-stu-id="4c242-114">Several steps must be completed before cash flow forecasts can appear in Power BI views.</span></span> <span data-ttu-id="4c242-115">Aşağıdaki denetim listesini inceleyin ve her adımın tamamlandığından emin olun:</span><span class="sxs-lookup"><span data-stu-id="4c242-115">Review the following checklist, and make sure that every step has been completed:</span></span>

- <span data-ttu-id="4c242-116">Her tüzel kişilik için nakit akışını ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="4c242-116">Set up cash flow for each legal entity.</span></span>
- <span data-ttu-id="4c242-117">Genel muhasebe parametrelerinde, sistem para birimini ve sistem döviz kuru türünü ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="4c242-117">In General ledger parameters, set the system currency and the system exchange rate type.</span></span>
- <span data-ttu-id="4c242-118">Genel muhasebe muhasebe para birimini ve döviz kuru türünü ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="4c242-118">Set the ledger accounting currency and the exchange rate type.</span></span>
- <span data-ttu-id="4c242-119">Hareket para birimi ile muhasebe para birimi arasında döviz kurları girin.</span><span class="sxs-lookup"><span data-stu-id="4c242-119">Enter exchange rates between the transaction currency and the accounting currency.</span></span>
- <span data-ttu-id="4c242-120">Muhasebe para birimi ile sistem para birimi arasında döviz kurları girin.</span><span class="sxs-lookup"><span data-stu-id="4c242-120">Enter exchange rates between the accounting currency and the system currency.</span></span>
- <span data-ttu-id="4c242-121">Muhasebe para birimi ile her banka para birimi arasında döviz kurları girin.</span><span class="sxs-lookup"><span data-stu-id="4c242-121">Enter exchange rates between the accounting currency and each bank currency.</span></span>

## <a name="why-did-cash-flow-power-bi-work-in-previous-versions-but-is-now-blank"></a><span data-ttu-id="4c242-122">Nakit akışı Power BI neden önceki sürümlerde çalışıyordu ancak şimdi boş?</span><span class="sxs-lookup"><span data-stu-id="4c242-122">Why did cash flow Power BI work in previous versions but is now blank?</span></span>

<span data-ttu-id="4c242-123">Varlık deposundaki "Nakit akışı ölçümü V2" ve "LedgerCovLiquidityMeasurement" ölçümlerinin yapılandırıldığını doğrulayın.</span><span class="sxs-lookup"><span data-stu-id="4c242-123">Verify that the "Cash flow measure V2" and "LedgerCovLiquidityMeasurement" measurements from Entity store have been configured.</span></span> <span data-ttu-id="4c242-124">Varlık deposundaki verilerle çalışma hakkında daha fazla bilgi için bkz. [Varlık deposuyla Power BI tümleştirmesi](../../fin-ops-core/dev-itpro/analytics/power-bi-integration-entity-store.md) Power BI içeriğini görüntülemek için gereken tüm adımların tamamlandığını doğrulayın.</span><span class="sxs-lookup"><span data-stu-id="4c242-124">For more information about how to work with data in Entity store, see [Power BI integration with Entity store](../../fin-ops-core/dev-itpro/analytics/power-bi-integration-entity-store.md) Verify that all the steps that are required to view Power BI content have been completed.</span></span> <span data-ttu-id="4c242-125">Daha fazla bilgi için bkz. [Nakde genel bakış Power BI içeriği](Cash-Overview-Power-BI-content.md).</span><span class="sxs-lookup"><span data-stu-id="4c242-125">For more information, see [Cash overview Power BI content](Cash-Overview-Power-BI-content.md).</span></span>

## <a name="have-the-entity-store-entities-been-refreshed"></a><span data-ttu-id="4c242-126">Varlık deposu varlıkları yenilendi mi?</span><span class="sxs-lookup"><span data-stu-id="4c242-126">Have the Entity store entities been refreshed?</span></span>

<span data-ttu-id="4c242-127">Verilerin güncel ve doğru olduğundan emin olmak için varlıklarınızı düzenli aralıklarla yenilemeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="4c242-127">You must periodically refresh your entities to ensure that the data is current and accurate.</span></span> <span data-ttu-id="4c242-128">Belirli bir varlığı el ile yenilemek için **Sistem yönetimi \> Kurulum \> Varlık deposu**'na gidin, varlığı seçin ve sonra **Yenile**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="4c242-128">To manually refresh a specific entity, go to **System administration \> Setup \> Entity store**, select the entity, and then select **Refresh**.</span></span> <span data-ttu-id="4c242-129">Veriler otomatik olarak da güncelleştirilebilir.</span><span class="sxs-lookup"><span data-stu-id="4c242-129">The data can also be updated automatically.</span></span> <span data-ttu-id="4c242-130">**Varlık deposu** sayfasında, **Otomatik yenileme etkin** seçeneğini **Evet** olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="4c242-130">On the **Entity store** page, set the **Automatic refresh enabled** option to **Yes**.</span></span>
