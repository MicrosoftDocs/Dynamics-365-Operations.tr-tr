---
title: Nakit akışı tahminini etkinleştirme (önizleme)
description: Bu konuda, Mali İçgörüler'de Nakit akışı tahminleri özelliğinin nasıl açılacağı açıklanmaktadır.
author: ShivamPandey-msft
ms.date: 07/24/2020
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
ms.openlocfilehash: f7c06eaeb79c1a2aa319cfa3d2ad8255bf716cd0
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/01/2021
ms.locfileid: "5818740"
---
# <a name="enable-cash-flow-forecasting-preview"></a><span data-ttu-id="e21f6-103">Nakit akışı tahminini etkinleştirme (önizleme)</span><span class="sxs-lookup"><span data-stu-id="e21f6-103">Enable cash flow forecasting (preview)</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="e21f6-104">Bu konuda, Mali İçgörüler'de Nakit akışı tahminleri özelliğinin nasıl açılacağı açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="e21f6-104">This topic explains how to turn on the Cash flow forecasts feature in Finance Insights.</span></span>

> [!NOTE]
> <span data-ttu-id="e21f6-105">Nakit akışında ödeme tahminlerini kullanmak için [Müşteri ödeme tahminlerini etkinleştirme](enable-cust-paymnt-prediction.md) konusunda anlatılan şekilde Müşteri ödeme tahminleri özelliğini ayarlamanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="e21f6-105">To use payment predictions in the cash flow, you must set up the Customer payment predictions feature as described in [Enable customer payment predictions](enable-cust-paymnt-prediction.md).</span></span>

1. <span data-ttu-id="e21f6-106">Ortamın birincil Azure SQL kurulumuna bağlanmak için Microsoft Dynamics Lifecycle Services (LCS) portalındaki ortam sayfasında yer alan bilgileri kullanın.</span><span class="sxs-lookup"><span data-stu-id="e21f6-106">Use information from the environment page in Microsoft Dynamics Lifecycle Services (LCS) to connect to the primary instance of Azure SQL for that environment.</span></span> <span data-ttu-id="e21f6-107">Korumalı alan ortamına sınırlı dağıtımları açmak için aşağıdaki Transact-SQL (T-SQL) komutunu çalıştırın.</span><span class="sxs-lookup"><span data-stu-id="e21f6-107">Run the following Transact-SQL (T-SQL) command to turn on flights for the sandbox environment.</span></span> <span data-ttu-id="e21f6-108">(Uygulama Nesne Sunucusu \[AOS\] hizmetine uzaktan bağlanmadan önce IP adresinize erişimi açmanız gerekebilir.)</span><span class="sxs-lookup"><span data-stu-id="e21f6-108">(You might have to turn on access for your IP address in LCS before you can connect remotely to Application Object Server \[AOS\].)</span></span>

    `INSERT INTO SYSFLIGHTING (FLIGHTNAME, ENABLED) VALUES ('CashflowInsightsFeature', 1)`

    > [!NOTE]
    > <span data-ttu-id="e21f6-109">Microsoft Dynamics 365 Finance dağıtımınız Service Fabric dağıtımıysa bu adımı atlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="e21f6-109">If your deployment of Microsoft Dynamics 365 Finance is a Service Fabric deployment, you can skip this step.</span></span> <span data-ttu-id="e21f6-110">Mali İçgörüler ekibi, bu sınırlı dağıtımı sizin için açmış olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="e21f6-110">The Finance Insights team should already have turned on the flight for you.</span></span> <span data-ttu-id="e21f6-111">Özellikleri **Özellik yönetimi** çalışma alanında görmüyorsanız veya özellikleri açmaya çalışırken sorun yaşıyorsanız <fiap@microsoft.com> adresiyle iletişime geçin.</span><span class="sxs-lookup"><span data-stu-id="e21f6-111">If you don't see the features in the **Feature management** workspace, or if experience issues when you try to turn them on, contact <fiap@microsoft.com>.</span></span>
  
2. <span data-ttu-id="e21f6-112">**Özellik yönetimi** çalışma alanını açın ve şu adımları izleyin:</span><span class="sxs-lookup"><span data-stu-id="e21f6-112">Open the **Feature management** workspace, and follow these steps:</span></span>

    1. <span data-ttu-id="e21f6-113">**Güncelleştirmeleri denetle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="e21f6-113">Select **Check for updates**.</span></span>
    2. <span data-ttu-id="e21f6-114">Aşağıdaki özellikleri açın:</span><span class="sxs-lookup"><span data-stu-id="e21f6-114">Turn on the following features:</span></span>

        - <span data-ttu-id="e21f6-115">Yeni kılavuz denetimi</span><span class="sxs-lookup"><span data-stu-id="e21f6-115">New grid control</span></span>
        - <span data-ttu-id="e21f6-116">Izgaralarda gruplandırma (önizleme)</span><span class="sxs-lookup"><span data-stu-id="e21f6-116">Grouping in grids (preview)</span></span> 
        - <span data-ttu-id="e21f6-117">Müşteriye ödeme tahminleri (önizleme)</span><span class="sxs-lookup"><span data-stu-id="e21f6-117">Customer payment predictions (preview)</span></span>
        - <span data-ttu-id="e21f6-118">Nakit akışı tahminleri (önizleme)</span><span class="sxs-lookup"><span data-stu-id="e21f6-118">Cash flow forecasts (preview)</span></span>

3. <span data-ttu-id="e21f6-119">**Nakit ve banka yönetimi \> Nakit akışı tahmin kurulumu** bölümüne gidin ve tahminlere eklenmesi gereken likidite hesaplarını ekleyin.</span><span class="sxs-lookup"><span data-stu-id="e21f6-119">Go to **Cash and bank management \> Cash flow forecast setup**, and add the liquidity accounts that should be included in the forecasts.</span></span>

    > [!NOTE]
    > <span data-ttu-id="e21f6-120">Likidite hesapları ayarlanmamışsa nakit akışı oluşturulamaz.</span><span class="sxs-lookup"><span data-stu-id="e21f6-120">If liquidity accounts aren't set up, the cash flow can't be generated.</span></span>

4. <span data-ttu-id="e21f6-121">**Nakit ve banka yönetimi \> Kurulum \> Mali İçgörüler (preview) \> Nakit akışı tahminleri (önizleme)** bölümüne gidin ve şu adımları izleyin:</span><span class="sxs-lookup"><span data-stu-id="e21f6-121">Go to **Cash and bank management \> Setup \> Finance Insights (preview) \> Cash flow forecasts (preview)**, and follow these steps:</span></span>

    1. <span data-ttu-id="e21f6-122">**Nakit akışı tahmini** sekmesinde, **Özelliği etkinleştir**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="e21f6-122">On the **Cash flow forecast** tab, select **Enable feature**.</span></span>
    2. <span data-ttu-id="e21f6-123">**Tahmin modeli oluştur** seçeneğini belirleyin.</span><span class="sxs-lookup"><span data-stu-id="e21f6-123">Select **Create prediction model**.</span></span>

<span data-ttu-id="e21f6-124">Nakit akışı tahmini özelliği hakkında daha fazla bilgi için bkz: [Nakit akışı tahmini](cash-flow-forecast-intro.md).</span><span class="sxs-lookup"><span data-stu-id="e21f6-124">For more information about the cash flow forecasting capability, see [Cash flow forecasting](cash-flow-forecast-intro.md).</span></span>

## <a name="privacy-notice"></a><span data-ttu-id="e21f6-125">Gizlilik bildirimi</span><span class="sxs-lookup"><span data-stu-id="e21f6-125">Privacy notice</span></span>

<span data-ttu-id="e21f6-126">Önizlemeler (1), Dynamics 365 Finance and Operations hizmetinden daha az gizlilik ve güvenlik önlemleri kullanabilir, (2) bu hizmet için hizmet düzeyi sözleşmesine (SLA) dahil edilmez, (3) kişisel verileri veya yasal ya da mevzuat uyumluluğu gereksinimlerine tabi olan diğer verileri işlemek için kullanılmamalıdır ve (4) sınırlı desteğe sahiptir.</span><span class="sxs-lookup"><span data-stu-id="e21f6-126">Previews (1) might use less privacy and fewer security measures than the Dynamics 365 Finance and Operations service, (2) aren't included in the service level agreement (SLA) for this service, (3) should not be used to process personal data or other data that is subject to legal or regulatory compliance requirements, and (4) have limited support.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]