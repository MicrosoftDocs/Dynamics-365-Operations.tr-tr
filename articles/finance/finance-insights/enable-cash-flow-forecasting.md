---
title: Nakit akışı tahminini etkinleştirme (önizleme)
description: Bu konuda, Mali İçgörüler'de Nakit akışı tahminleri özelliğinin nasıl açılacağı açıklanmaktadır.
author: ShivamPandey-msft
ms.date: 06/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2020-07-24
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: ba8acb2191291e2abed5cabf234c19fe09e6c8ff
ms.sourcegitcommit: 655b0e16c7aef6182cd58bc816b901470e1bb2ce
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/10/2021
ms.locfileid: "6222570"
---
# <a name="enable-cash-flow-forecasting-preview"></a><span data-ttu-id="5d8c5-103">Nakit akışı tahminini etkinleştirme (önizleme)</span><span class="sxs-lookup"><span data-stu-id="5d8c5-103">Enable cash flow forecasting (preview)</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="5d8c5-104">Bu konuda, Mali İçgörüler'de Nakit akışı tahminleri özelliğinin nasıl açılacağı açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="5d8c5-104">This topic explains how to turn on the Cash flow forecasts feature in Finance Insights.</span></span>

> [!NOTE]
> <span data-ttu-id="5d8c5-105">Nakit akışında ödeme tahminlerini kullanmak için [Müşteri ödeme tahminlerini etkinleştirme](enable-cust-paymnt-prediction.md) konusunda anlatılan şekilde Müşteri ödeme tahminleri özelliğini ayarlamanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="5d8c5-105">To use payment predictions in the cash flow, you must set up the Customer payment predictions feature as described in [Enable customer payment predictions](enable-cust-paymnt-prediction.md).</span></span>

1. <span data-ttu-id="5d8c5-106">Ortamın birincil Azure SQL kurulumuna bağlanmak için Microsoft Dynamics Lifecycle Services (LCS) portalındaki ortam sayfasında yer alan bilgileri kullanın.</span><span class="sxs-lookup"><span data-stu-id="5d8c5-106">Use information from the environment page in Microsoft Dynamics Lifecycle Services (LCS) to connect to the primary instance of Azure SQL for that environment.</span></span> <span data-ttu-id="5d8c5-107">Korumalı alan ortamına sınırlı dağıtımları açmak için aşağıdaki Transact-SQL (T-SQL) komutunu çalıştırın.</span><span class="sxs-lookup"><span data-stu-id="5d8c5-107">Run the following Transact-SQL (T-SQL) command to turn on flights for the sandbox environment.</span></span> <span data-ttu-id="5d8c5-108">(Uygulama Nesne Sunucusu \[AOS\] hizmetine uzaktan bağlanmadan önce IP adresinize erişimi açmanız gerekebilir.)</span><span class="sxs-lookup"><span data-stu-id="5d8c5-108">(You might have to turn on access for your IP address in LCS before you can connect remotely to Application Object Server \[AOS\].)</span></span>

    `INSERT INTO SYSFLIGHTING (FLIGHTNAME, ENABLED) VALUES ('CashflowInsightsFeature', 1)`

    > [!NOTE]
    > <span data-ttu-id="5d8c5-109">Sürüm 10.0.20 veya sonrasını kullanıyorsanız veya bir Service Fabric dağıtımı kullanıyorsanız bu adımı atlayın.</span><span class="sxs-lookup"><span data-stu-id="5d8c5-109">Skip this step if you're using version 10.0.20 or later, or if you're using a Service Fabric deployment.</span></span> <span data-ttu-id="5d8c5-110">Mali içgörüler ekibi, bu sınırlı dağıtımı sizin için açmış olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="5d8c5-110">The Finance insights team should already have turned on the flight for you.</span></span> <span data-ttu-id="5d8c5-111">Özelliği **Özellik yönetimi** çalışma alanında görmüyorsanız veya özelliği açmaya çalışırken sorun yaşıyorsanız <fiap@microsoft.com> adresiyle iletişime geçin.</span><span class="sxs-lookup"><span data-stu-id="5d8c5-111">If you don't see the feature in the **Feature management** workspace, or if you experience issues when you try to turn it on, contact <fiap@microsoft.com>.</span></span>
  
2. <span data-ttu-id="5d8c5-112">**Özellik yönetimi** çalışma alanını açın ve şu adımları izleyin:</span><span class="sxs-lookup"><span data-stu-id="5d8c5-112">Open the **Feature management** workspace, and follow these steps:</span></span>

    1. <span data-ttu-id="5d8c5-113">**Güncelleştirmeleri denetle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="5d8c5-113">Select **Check for updates**.</span></span>
    2. <span data-ttu-id="5d8c5-114">Aşağıdaki özellikleri açın:</span><span class="sxs-lookup"><span data-stu-id="5d8c5-114">Turn on the following features:</span></span>

        - <span data-ttu-id="5d8c5-115">Yeni kılavuz denetimi</span><span class="sxs-lookup"><span data-stu-id="5d8c5-115">New grid control</span></span>
        - <span data-ttu-id="5d8c5-116">Izgaralarda gruplandırma (önizleme)</span><span class="sxs-lookup"><span data-stu-id="5d8c5-116">Grouping in grids (preview)</span></span> 
        - <span data-ttu-id="5d8c5-117">Müşteriye ödeme tahminleri (önizleme)</span><span class="sxs-lookup"><span data-stu-id="5d8c5-117">Customer payment predictions (preview)</span></span>
        - <span data-ttu-id="5d8c5-118">Nakit akışı tahminleri (önizleme)</span><span class="sxs-lookup"><span data-stu-id="5d8c5-118">Cash flow forecasts (preview)</span></span>

3. <span data-ttu-id="5d8c5-119">**Nakit ve banka yönetimi \> Nakit akışı tahmin kurulumu** bölümüne gidin ve tahminlere eklenmesi gereken likidite hesaplarını ekleyin.</span><span class="sxs-lookup"><span data-stu-id="5d8c5-119">Go to **Cash and bank management \> Cash flow forecast setup**, and add the liquidity accounts that should be included in the forecasts.</span></span>

    > [!NOTE]
    > <span data-ttu-id="5d8c5-120">Likidite hesapları ayarlanmamışsa nakit akışı oluşturulamaz.</span><span class="sxs-lookup"><span data-stu-id="5d8c5-120">If liquidity accounts aren't set up, the cash flow can't be generated.</span></span>

4. <span data-ttu-id="5d8c5-121">**Nakit ve banka yönetimi \> Kurulum \> Mali İçgörüler (preview) \> Nakit akışı tahminleri (önizleme)** bölümüne gidin ve şu adımları izleyin:</span><span class="sxs-lookup"><span data-stu-id="5d8c5-121">Go to **Cash and bank management \> Setup \> Finance Insights (preview) \> Cash flow forecasts (preview)**, and follow these steps:</span></span>

    1. <span data-ttu-id="5d8c5-122">**Nakit akışı tahmini** sekmesinde, **Özelliği etkinleştir**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="5d8c5-122">On the **Cash flow forecast** tab, select **Enable feature**.</span></span>
    2. <span data-ttu-id="5d8c5-123">**Tahmin modeli oluştur** seçeneğini belirleyin.</span><span class="sxs-lookup"><span data-stu-id="5d8c5-123">Select **Create prediction model**.</span></span>

<span data-ttu-id="5d8c5-124">Nakit akışı tahmini özelliği hakkında daha fazla bilgi için bkz: [Nakit akışı tahmini](cash-flow-forecast-intro.md).</span><span class="sxs-lookup"><span data-stu-id="5d8c5-124">For more information about the cash flow forecasting capability, see [Cash flow forecasting](cash-flow-forecast-intro.md).</span></span>

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
