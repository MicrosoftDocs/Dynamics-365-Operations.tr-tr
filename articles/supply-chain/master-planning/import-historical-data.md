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
ms.openlocfilehash: 9bb3c178a698bdcd46e7c596247360ba9233b398
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/01/2021
ms.locfileid: "5816496"
---
# <a name="import-historical-data-for-demand-forecasts"></a><span data-ttu-id="5e497-104">Talep tahminleri için geçmiş verisini içe aktar</span><span class="sxs-lookup"><span data-stu-id="5e497-104">Import historical data for demand forecasts</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="5e497-105">Talep tahminlerinin doğruluğunu garanti etmeye yardımcı olmak için, madde veya madde tahsisat anahtarı başına mümkün olduğunca fazla geçmiş talep verisine sahip olmalısınız.</span><span class="sxs-lookup"><span data-stu-id="5e497-105">To help guarantee the accuracy of demand forecasts, you must have as much historical demand data as you can get per item or item allocation key.</span></span> <span data-ttu-id="5e497-106">Geçmiş talep verisi halihazırda içe aktarılmamışsa, içe aktarmak için **Geçmiş harici talep** (ReqDemPlanHistoricalExternalDemandEntity) veri varlığını Dynamics 365 Supply Chain Management içinde kullanın.</span><span class="sxs-lookup"><span data-stu-id="5e497-106">If the historical demand data isn't already imported, use the **Historical external demand** (ReqDemPlanHistoricalExternalDemandEntity) data entity in Dynamics 365 Supply Chain Management to import it.</span></span>

<span data-ttu-id="5e497-107">**Veri yönetimi** çalışma alanı içerisinde, varlık içerisindeki tüm alanların bir genel görünümünü görürsünüz.</span><span class="sxs-lookup"><span data-stu-id="5e497-107">In the **Data management** workspace, you can see an overview of all the fields in the entity.</span></span>

1. <span data-ttu-id="5e497-108">**Veri yönetimi** çalışma alanını açın.</span><span class="sxs-lookup"><span data-stu-id="5e497-108">Open the **Data management** workspace.</span></span>
2. <span data-ttu-id="5e497-109">**Veri varlıkları** kutucuğunu seçin.</span><span class="sxs-lookup"><span data-stu-id="5e497-109">Select the **Data entities** tile.</span></span>
3. <span data-ttu-id="5e497-110">Varlık listesinde **Geçmiş harici talep** arayın.</span><span class="sxs-lookup"><span data-stu-id="5e497-110">Search the entity list for **Historical external demand**.</span></span>
4. <span data-ttu-id="5e497-111">**Hedef alanlar**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="5e497-111">Select **Target fields**.</span></span> <span data-ttu-id="5e497-112">Aşağıdaki varlık alanları zorunludur: site (**DeliveringSiteId**), tarih (**DemandDate**), miktar (**DemandQuantity**), ve madde numarası (**ItemNumber**) veya madde tahsisat anahtarı (**ProductAllocationKeyId**).</span><span class="sxs-lookup"><span data-stu-id="5e497-112">The following entity fields are mandatory: site (**DeliveringSiteId**), date (**DemandDate**), quantity (**DemandQuantity**), and either item number (**ItemNumber**) or item allocation key (**ProductAllocationKeyId**).</span></span>

<span data-ttu-id="5e497-113">Varlık verisini kullanmak için geçmiş talep verisini içeren Microsoft Excel dosyası veya virgülle ayrılmış değerler (CSV) dosyasına sahip olmalısınız.</span><span class="sxs-lookup"><span data-stu-id="5e497-113">To use the data entity, you must have a Microsoft Excel file or comma-separated values (CSV) file that contains the historical demand data.</span></span> <span data-ttu-id="5e497-114">Aşağıdaki örnek, verinin bir CSV dosyasından nasıl alınacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="5e497-114">The following example shows how to import the data from a CSV file.</span></span>

<span data-ttu-id="5e497-115">İçeei aktarma işleminden sonra verilerin nasıl temizleneceği de dahil olmak üzere verilerin nasıl içeri aktarılacağı hakkında daha fazla bilgi için [Veri içeri ve dışarı aktarma işlerine genel bakış](../../fin-ops-core/dev-itpro/data-entities/data-import-export-job.md) ve ilgili konuları inceleyin.</span><span class="sxs-lookup"><span data-stu-id="5e497-115">For more information about how to import data, including how to clean up data after an import, see [Data import and export jobs overview](../../fin-ops-core/dev-itpro/data-entities/data-import-export-job.md) and its related topics.</span></span>

## <a name="example"></a><span data-ttu-id="5e497-116">Örnek</span><span class="sxs-lookup"><span data-stu-id="5e497-116">Example</span></span>

<span data-ttu-id="5e497-117">Aşağıdaki dosyayı bir örnek olarak kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="5e497-117">You can use the following file as an example.</span></span> <span data-ttu-id="5e497-118">[HistoricalDemandData](https://docs.microsoft.com/dynamics/s-e/) karşıdan yükleyin.</span><span class="sxs-lookup"><span data-stu-id="5e497-118">Download the [HistoricalDemandData](https://docs.microsoft.com/dynamics/s-e/).</span></span> <span data-ttu-id="5e497-119">Bu dosya, madde D0001 için geçmiş talep verisini içerir.</span><span class="sxs-lookup"><span data-stu-id="5e497-119">This file contains the historical demand data for item D0001.</span></span> <span data-ttu-id="5e497-120">Yalnızca aşağıdaki zorunlu alanları içerir: site, miktar ve talep tarihi.</span><span class="sxs-lookup"><span data-stu-id="5e497-120">It contains only the following mandatory fields: site, quantity, and the demand date.</span></span>

1. <span data-ttu-id="5e497-121">Geçmiş talep verisinin aktarılacağı şirketi seçin.</span><span class="sxs-lookup"><span data-stu-id="5e497-121">Select the company to import the historical demand data into.</span></span>
2. <span data-ttu-id="5e497-122">**Veri yönetimi** çalışma alanını açın.</span><span class="sxs-lookup"><span data-stu-id="5e497-122">Open the **Data management** workspace.</span></span>
3. <span data-ttu-id="5e497-123">**İçeri aktar** kutucuğunu seçin.</span><span class="sxs-lookup"><span data-stu-id="5e497-123">Select the **Import** tile.</span></span>
4. <span data-ttu-id="5e497-124">İçe aktarma projesi için bir ad seçin, örneğin **Madde D0001 için geçmiş talep verisi içe aktar**.</span><span class="sxs-lookup"><span data-stu-id="5e497-124">Enter a name for the import project, such as **Import historical demand for item D0001**.</span></span>
5. <span data-ttu-id="5e497-125">**Kaynak veri biçimi** alanında, içe aktardığınız dosyanın dosya formatını seçin.</span><span class="sxs-lookup"><span data-stu-id="5e497-125">In the **Source data format** field, select the file format of the file that you're importing.</span></span> <span data-ttu-id="5e497-126">Bu örnek için HistoricalDemandData dosyasını içe aktarmak için, **CSV** seçeneğini işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="5e497-126">To import the HistoricalDemandData file for this example, select **CSV**.</span></span>
6. <span data-ttu-id="5e497-127">**Varlık adı** alanında, **Geçmiş harici talep** seçeneğini işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="5e497-127">In the **Entity name** field, select **Historical external demand**.</span></span>
7. <span data-ttu-id="5e497-128">Dosyayı bilgisayarınıza kaydedin ve sonra karşıya yükleyin.</span><span class="sxs-lookup"><span data-stu-id="5e497-128">Save the file to your computer, and then upload it.</span></span>
8. <span data-ttu-id="5e497-129">**İçe aktar**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="5e497-129">Select **Import**.</span></span>
9. <span data-ttu-id="5e497-130">**Yürütme özeti** sayfası otomatik olarak açılır.</span><span class="sxs-lookup"><span data-stu-id="5e497-130">The **Execution summary** page is opened automatically.</span></span> <span data-ttu-id="5e497-131">İçe aktarılan veriyi sayfada doğrulayın.</span><span class="sxs-lookup"><span data-stu-id="5e497-131">Verify the imported data on the page.</span></span>

<span data-ttu-id="5e497-132">Geçmiş talep verisini içe aktardıktan sonra talep tahminleri oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="5e497-132">After you've imported the historical demand data, you can generate a demand forecast.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="5e497-133">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="5e497-133">Additional resources</span></span>

[<span data-ttu-id="5e497-134">İstatistik temel tahmini oluşturma</span><span class="sxs-lookup"><span data-stu-id="5e497-134">Generate a statistical baseline forecast</span></span>](generate-statistical-baseline-forecast.md)  
[<span data-ttu-id="5e497-135">Veri içe ve dışa aktarma işlerine genel bakış</span><span class="sxs-lookup"><span data-stu-id="5e497-135">Data import and export jobs overview</span></span>](../../fin-ops-core/dev-itpro/data-entities/data-import-export-job.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]