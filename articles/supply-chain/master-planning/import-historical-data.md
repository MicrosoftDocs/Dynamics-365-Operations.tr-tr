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
ms.openlocfilehash: de380113fe951f75c15f9e5526ad2f1f5cc84334
ms.sourcegitcommit: 34b478f175348d99df4f2f0c2f6c0c21b6b2660a
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2021
ms.locfileid: "5908892"
---
# <a name="import-historical-data-for-demand-forecasts"></a><span data-ttu-id="26f19-104">Talep tahminleri için geçmiş verisini içe aktar</span><span class="sxs-lookup"><span data-stu-id="26f19-104">Import historical data for demand forecasts</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="26f19-105">Talep tahminlerinin doğruluğunu garanti etmeye yardımcı olmak için, madde veya madde tahsisat anahtarı başına mümkün olduğunca fazla geçmiş talep verisine sahip olmalısınız.</span><span class="sxs-lookup"><span data-stu-id="26f19-105">To help guarantee the accuracy of demand forecasts, you must have as much historical demand data as you can get per item or item allocation key.</span></span> <span data-ttu-id="26f19-106">Geçmiş talep verisi halihazırda içe aktarılmamışsa, içe aktarmak için **Geçmiş harici talep** (ReqDemPlanHistoricalExternalDemandEntity) veri varlığını Dynamics 365 Supply Chain Management içinde kullanın.</span><span class="sxs-lookup"><span data-stu-id="26f19-106">If the historical demand data isn't already imported, use the **Historical external demand** (ReqDemPlanHistoricalExternalDemandEntity) data entity in Dynamics 365 Supply Chain Management to import it.</span></span>

<span data-ttu-id="26f19-107">**Veri yönetimi** çalışma alanı içerisinde, varlık içerisindeki tüm alanların bir genel görünümünü görürsünüz.</span><span class="sxs-lookup"><span data-stu-id="26f19-107">In the **Data management** workspace, you can see an overview of all the fields in the entity.</span></span>

1. <span data-ttu-id="26f19-108">**Veri yönetimi** çalışma alanını açın.</span><span class="sxs-lookup"><span data-stu-id="26f19-108">Open the **Data management** workspace.</span></span>
2. <span data-ttu-id="26f19-109">**Veri varlıkları** kutucuğunu seçin.</span><span class="sxs-lookup"><span data-stu-id="26f19-109">Select the **Data entities** tile.</span></span>
3. <span data-ttu-id="26f19-110">Varlık listesinde **Geçmiş harici talep** arayın.</span><span class="sxs-lookup"><span data-stu-id="26f19-110">Search the entity list for **Historical external demand**.</span></span>
4. <span data-ttu-id="26f19-111">**Hedef alanlar**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="26f19-111">Select **Target fields**.</span></span> <span data-ttu-id="26f19-112">Aşağıdaki varlık alanları zorunludur: site (**DeliveringSiteId**), tarih (**DemandDate**), miktar (**DemandQuantity**), ve madde numarası (**ItemNumber**) veya madde tahsisat anahtarı (**ProductAllocationKeyId**).</span><span class="sxs-lookup"><span data-stu-id="26f19-112">The following entity fields are mandatory: site (**DeliveringSiteId**), date (**DemandDate**), quantity (**DemandQuantity**), and either item number (**ItemNumber**) or item allocation key (**ProductAllocationKeyId**).</span></span>

<span data-ttu-id="26f19-113">Varlık verisini kullanmak için geçmiş talep verisini içeren Microsoft Excel dosyası veya virgülle ayrılmış değerler (CSV) dosyasına sahip olmalısınız.</span><span class="sxs-lookup"><span data-stu-id="26f19-113">To use the data entity, you must have a Microsoft Excel file or comma-separated values (CSV) file that contains the historical demand data.</span></span> <span data-ttu-id="26f19-114">Aşağıdaki örnek, verinin bir CSV dosyasından nasıl alınacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="26f19-114">The following example shows how to import the data from a CSV file.</span></span>

<span data-ttu-id="26f19-115">İçeei aktarma işleminden sonra verilerin nasıl temizleneceği de dahil olmak üzere verilerin nasıl içeri aktarılacağı hakkında daha fazla bilgi için [Veri içeri ve dışarı aktarma işlerine genel bakış](../../fin-ops-core/dev-itpro/data-entities/data-import-export-job.md) ve ilgili konuları inceleyin.</span><span class="sxs-lookup"><span data-stu-id="26f19-115">For more information about how to import data, including how to clean up data after an import, see [Data import and export jobs overview](../../fin-ops-core/dev-itpro/data-entities/data-import-export-job.md) and its related topics.</span></span>

## <a name="example"></a><span data-ttu-id="26f19-116">Örnek</span><span class="sxs-lookup"><span data-stu-id="26f19-116">Example</span></span>

<span data-ttu-id="26f19-117">Aşağıdaki dosyayı bir örnek olarak kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="26f19-117">You can use the following file as an example.</span></span> <span data-ttu-id="26f19-118">[HistoricalDemandData](/dynamics/s-e/) karşıdan yükleyin.</span><span class="sxs-lookup"><span data-stu-id="26f19-118">Download the [HistoricalDemandData](/dynamics/s-e/).</span></span> <span data-ttu-id="26f19-119">Bu dosya, madde D0001 için geçmiş talep verisini içerir.</span><span class="sxs-lookup"><span data-stu-id="26f19-119">This file contains the historical demand data for item D0001.</span></span> <span data-ttu-id="26f19-120">Yalnızca aşağıdaki zorunlu alanları içerir: site, miktar ve talep tarihi.</span><span class="sxs-lookup"><span data-stu-id="26f19-120">It contains only the following mandatory fields: site, quantity, and the demand date.</span></span>

1. <span data-ttu-id="26f19-121">Geçmiş talep verisinin aktarılacağı şirketi seçin.</span><span class="sxs-lookup"><span data-stu-id="26f19-121">Select the company to import the historical demand data into.</span></span>
2. <span data-ttu-id="26f19-122">**Veri yönetimi** çalışma alanını açın.</span><span class="sxs-lookup"><span data-stu-id="26f19-122">Open the **Data management** workspace.</span></span>
3. <span data-ttu-id="26f19-123">**İçeri aktar** kutucuğunu seçin.</span><span class="sxs-lookup"><span data-stu-id="26f19-123">Select the **Import** tile.</span></span>
4. <span data-ttu-id="26f19-124">İçe aktarma projesi için bir ad seçin, örneğin **Madde D0001 için geçmiş talep verisi içe aktar**.</span><span class="sxs-lookup"><span data-stu-id="26f19-124">Enter a name for the import project, such as **Import historical demand for item D0001**.</span></span>
5. <span data-ttu-id="26f19-125">**Kaynak veri biçimi** alanında, içe aktardığınız dosyanın dosya formatını seçin.</span><span class="sxs-lookup"><span data-stu-id="26f19-125">In the **Source data format** field, select the file format of the file that you're importing.</span></span> <span data-ttu-id="26f19-126">Bu örnek için HistoricalDemandData dosyasını içe aktarmak için, **CSV** seçeneğini işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="26f19-126">To import the HistoricalDemandData file for this example, select **CSV**.</span></span>
6. <span data-ttu-id="26f19-127">**Varlık adı** alanında, **Geçmiş harici talep** seçeneğini işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="26f19-127">In the **Entity name** field, select **Historical external demand**.</span></span>
7. <span data-ttu-id="26f19-128">Dosyayı bilgisayarınıza kaydedin ve sonra karşıya yükleyin.</span><span class="sxs-lookup"><span data-stu-id="26f19-128">Save the file to your computer, and then upload it.</span></span>
8. <span data-ttu-id="26f19-129">**İçe aktar**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="26f19-129">Select **Import**.</span></span>
9. <span data-ttu-id="26f19-130">**Yürütme özeti** sayfası otomatik olarak açılır.</span><span class="sxs-lookup"><span data-stu-id="26f19-130">The **Execution summary** page is opened automatically.</span></span> <span data-ttu-id="26f19-131">İçe aktarılan veriyi sayfada doğrulayın.</span><span class="sxs-lookup"><span data-stu-id="26f19-131">Verify the imported data on the page.</span></span>

<span data-ttu-id="26f19-132">Geçmiş talep verisini içe aktardıktan sonra talep tahminleri oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="26f19-132">After you've imported the historical demand data, you can generate a demand forecast.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="26f19-133">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="26f19-133">Additional resources</span></span>

[<span data-ttu-id="26f19-134">İstatistik temel tahmini oluşturma</span><span class="sxs-lookup"><span data-stu-id="26f19-134">Generate a statistical baseline forecast</span></span>](generate-statistical-baseline-forecast.md)  
[<span data-ttu-id="26f19-135">Veri içe ve dışa aktarma işlerine genel bakış</span><span class="sxs-lookup"><span data-stu-id="26f19-135">Data import and export jobs overview</span></span>](../../fin-ops-core/dev-itpro/data-entities/data-import-export-job.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]