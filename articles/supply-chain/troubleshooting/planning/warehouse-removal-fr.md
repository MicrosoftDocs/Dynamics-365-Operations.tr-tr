---
title: Tahmin satırlarından Ambar talebi tahmin boyutunu kaldıramazsınız
description: Tahmin satırlarından Ambar talebi tahmin boyutunu kaldıramazsınız.
author: ChristianRytt
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: ForecastSales
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 6b643c4fe51ae6ce73b34ab81d4e458dcd5032df
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026986"
---
# <a name="you-cant-remove-the-warehouse-demand-forecast-dimension-from-forecast-lines"></a><span data-ttu-id="be6d4-103">Tahmin satırlarından Ambar talebi tahmin boyutunu kaldıramazsınız</span><span class="sxs-lookup"><span data-stu-id="be6d4-103">You can't remove the Warehouse demand forecast dimension from forecast lines</span></span>

<span data-ttu-id="be6d4-104">KB numarası: 4614408</span><span class="sxs-lookup"><span data-stu-id="be6d4-104">KB number: 4614408</span></span>

## <a name="symptoms"></a><span data-ttu-id="be6d4-105">Belirtiler</span><span class="sxs-lookup"><span data-stu-id="be6d4-105">Symptoms</span></span>

<span data-ttu-id="be6d4-106">Bu sorun, **Talep tahmin parametresi** sayfasının **Tahmin boyutları** sekmesinde **Ambar** boyutu atanmamışsa oluşur.</span><span class="sxs-lookup"><span data-stu-id="be6d4-106">This issue occurs when the **Warehouse** dimension isn't assigned on the **Forecast dimensions** tab of the **Demand forecasting parameter** page.</span></span> <span data-ttu-id="be6d4-107">Bununla birlikte, **Ambar** sütunu **Talep tahmin** sayfasında gösterilir (**Master planlama \> Tahmin \>El ile tahmin varlığı \> Talep tahmin satırları**).</span><span class="sxs-lookup"><span data-stu-id="be6d4-107">Nevertheless, the **Warehouse** column is shown on the **Demand forecast** page (**Master planning \> Forecasting \> Manual forecast entity \> Demand forecast lines**).</span></span>

## <a name="resolution"></a><span data-ttu-id="be6d4-108">Çözünürlük</span><span class="sxs-lookup"><span data-stu-id="be6d4-108">Resolution</span></span>

<span data-ttu-id="be6d4-109">**Talep tahmin parametresi** sayfasının **Tahmin boyutları** sekmesindeki ayarlar, **Talep tahmin** sayfasını etkilemez.</span><span class="sxs-lookup"><span data-stu-id="be6d4-109">The settings on the **Forecast dimensions** tab of the **Demand forecasting parameter** page don't affect the **Demand forecast** page.</span></span> <span data-ttu-id="be6d4-110">Oluşturulan ve düzeltilmiş talep tahmininde gösterilen temel tahmini denetler.</span><span class="sxs-lookup"><span data-stu-id="be6d4-110">They control the baseline forecast that is generated and shown in the adjusted demand forecast.</span></span> <span data-ttu-id="be6d4-111">Ancak, "gerçek" talep tahmini için gerekli olan boyutları denetmezler.</span><span class="sxs-lookup"><span data-stu-id="be6d4-111">However, they don't control the dimensions that are required for the "real" demand forecast.</span></span> <span data-ttu-id="be6d4-112">**Düzeltilmiş talep tahmin** sayfasında gösterilen kayıtları yetkilendirerek, tahmin modeli için bunları "gerçek" tahmin girişlerine dönüştürebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="be6d4-112">By authorizing the records that are shown on the **Adjusted demand forecast** page, you can convert them to "real" forecast entries for a forecast model.</span></span> <span data-ttu-id="be6d4-113">Bu model, daha sonra master planlama için kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="be6d4-113">That model can then be used for master planning.</span></span>

<span data-ttu-id="be6d4-114">**Talep tahmin** sayfasında, talep tahmin satırlarında gösterilen "gerçek" tahminin boyutları stok boyutlarının bir parçasıdır.</span><span class="sxs-lookup"><span data-stu-id="be6d4-114">On the **Demand forecast** page, the dimensions for the "real" forecast that are shown on the demand forecast lines are part of the inventory dimensions.</span></span> <span data-ttu-id="be6d4-115">(Bu davranış satış siparişi satırlarının davranışına benzer.) Sisteminiz zorunlu stok boyutunda **Ambar** seçeneğini zorunlu olarak kullanacak şekilde ayarlanmamışsa sütunu gizlemek için sayfayı özelleştirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="be6d4-115">(This behavior resembles the behavior for sales order lines.) If your system isn't set up to use **Warehouse** as a mandatory inventory dimension, you can customize the page to hide the column.</span></span>
