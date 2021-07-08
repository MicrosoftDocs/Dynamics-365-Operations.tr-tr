---
title: Talep tahminleri için geçmiş verisini içe aktar
description: Doğru talep tahminleri elde etmek için madde veya madde tahsisat anahtarı başına tarihsel talep verisine ihtiyaç duyarsınız. Bu konu herhangi bir sistemden geçmiş verisini almak için veri varlıklarının nasıl kullanılacağını ve böylece daha uzun talep tahmin verisine nasıl sahip olacağınızı açıklar.
author: roxanadiaconu
ms.date: 05/10/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ReqDemPlanCreateForecastDialog
audience: Application User
ms.reviewer: kamaybac
ms.assetid: 59c0d269-9db0-48e7-b8c7-9a388781a9ca
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0b04ee246d4c28e934407ccb92d792692cc4347d
ms.sourcegitcommit: cbbb35c71ab4ff1ae08fa4f7cc97019b207246be
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/23/2021
ms.locfileid: "6301662"
---
# <a name="import-historical-data-for-demand-forecasts"></a><span data-ttu-id="1a99b-104">Talep tahminleri için geçmiş verisini içe aktar</span><span class="sxs-lookup"><span data-stu-id="1a99b-104">Import historical data for demand forecasts</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="1a99b-105">Talep tahminlerinin doğruluğunu garanti etmeye yardımcı olmak için, madde veya madde tahsisat anahtarı başına mümkün olduğunca fazla geçmiş talep verisine sahip olmalısınız.</span><span class="sxs-lookup"><span data-stu-id="1a99b-105">To help guarantee the accuracy of demand forecasts, you must have as much historical demand data as you can get per item or item allocation key.</span></span> <span data-ttu-id="1a99b-106">Geçmiş talep verisi halihazırda içe aktarılmamışsa, içe aktarmak için **Geçmiş harici talep** (ReqDemPlanHistoricalExternalDemandEntity) veri varlığını Dynamics 365 Supply Chain Management içinde kullanın.</span><span class="sxs-lookup"><span data-stu-id="1a99b-106">If the historical demand data isn't already imported, use the **Historical external demand** (ReqDemPlanHistoricalExternalDemandEntity) data entity in Dynamics 365 Supply Chain Management to import it.</span></span>

<span data-ttu-id="1a99b-107">**Veri yönetimi** çalışma alanı içerisinde, varlık içerisindeki tüm alanların bir genel görünümünü görürsünüz.</span><span class="sxs-lookup"><span data-stu-id="1a99b-107">In the **Data management** workspace, you can see an overview of all the fields in the entity.</span></span>

1. <span data-ttu-id="1a99b-108">**Veri yönetimi** çalışma alanını açın.</span><span class="sxs-lookup"><span data-stu-id="1a99b-108">Open the **Data management** workspace.</span></span>
2. <span data-ttu-id="1a99b-109">**Veri varlıkları** kutucuğunu seçin.</span><span class="sxs-lookup"><span data-stu-id="1a99b-109">Select the **Data entities** tile.</span></span>
3. <span data-ttu-id="1a99b-110">Varlık listesinde **Geçmiş harici talep** arayın.</span><span class="sxs-lookup"><span data-stu-id="1a99b-110">Search the entity list for **Historical external demand**.</span></span>
4. <span data-ttu-id="1a99b-111">**Hedef alanlar**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="1a99b-111">Select **Target fields**.</span></span> <span data-ttu-id="1a99b-112">Aşağıdaki varlık alanları zorunludur: site (**DeliveringSiteId**), tarih (**DemandDate**), miktar (**DemandQuantity**), ve madde numarası (**ItemNumber**) veya madde tahsisat anahtarı (**ProductAllocationKeyId**).</span><span class="sxs-lookup"><span data-stu-id="1a99b-112">The following entity fields are mandatory: site (**DeliveringSiteId**), date (**DemandDate**), quantity (**DemandQuantity**), and either item number (**ItemNumber**) or item allocation key (**ProductAllocationKeyId**).</span></span>

<span data-ttu-id="1a99b-113">Varlık verisini kullanmak için geçmiş talep verisini içeren Microsoft Excel dosyası veya virgülle ayrılmış değerler (CSV) dosyasına sahip olmalısınız.</span><span class="sxs-lookup"><span data-stu-id="1a99b-113">To use the data entity, you must have a Microsoft Excel file or comma-separated values (CSV) file that contains the historical demand data.</span></span> <span data-ttu-id="1a99b-114">Aşağıdaki örnek, verinin bir CSV dosyasından nasıl alınacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="1a99b-114">The following example shows how to import the data from a CSV file.</span></span>

<span data-ttu-id="1a99b-115">İçeei aktarma işleminden sonra verilerin nasıl temizleneceği de dahil olmak üzere verilerin nasıl içeri aktarılacağı hakkında daha fazla bilgi için [Veri içeri ve dışarı aktarma işlerine genel bakış](../../fin-ops-core/dev-itpro/data-entities/data-import-export-job.md) ve ilgili konuları inceleyin.</span><span class="sxs-lookup"><span data-stu-id="1a99b-115">For more information about how to import data, including how to clean up data after an import, see [Data import and export jobs overview](../../fin-ops-core/dev-itpro/data-entities/data-import-export-job.md) and its related topics.</span></span>

<span data-ttu-id="1a99b-116">Ayrıca bkz. [İstatistik temel tahmini oluşturma](generate-statistical-baseline-forecast.md).</span><span class="sxs-lookup"><span data-stu-id="1a99b-116">See also [Generate a statistical baseline forecast](generate-statistical-baseline-forecast.md).</span></span>

[!INCLUDE[footer-include](../../includes/footer-banner.md)]