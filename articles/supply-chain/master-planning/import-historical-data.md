---
title: Talep tahminleri için geçmiş verisini içe aktar
description: Doğru talep tahminleri elde etmek için madde veya madde tahsisat anahtarı başına tarihsel talep verisine ihtiyaç duyarsınız. Bu konu herhangi bir sistemden geçmiş verisini almak için veri varlıklarının nasıl kullanılacağını ve böylece daha uzun talep tahmin verisine nasıl sahip olacağınızı açıklar.
author: roxanadiaconu
manager: AnnBe
ms.date: 05/10/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqDemPlanCreateForecastDialog
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.assetid: 59c0d269-9db0-48e7-b8c7-9a388781a9ca
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 018694c79c6dd64e19b010848aad8acd36b0a9a8
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2019
ms.locfileid: "328620"
---
# <a name="import-historical-data-for-demand-forecasts"></a><span data-ttu-id="ed2ad-104">Talep tahminleri için geçmiş verisini içe aktar</span><span class="sxs-lookup"><span data-stu-id="ed2ad-104">Import historical data for demand forecasts</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ed2ad-105">Talep tahminlerinin doğruluğunu garanti etmeye yardımcı olmak için, madde veya madde tahsisat anahtarı başına mümkün olduğunca fazla geçmiş talep verisine sahip olmalısınız.</span><span class="sxs-lookup"><span data-stu-id="ed2ad-105">To help guarantee the accuracy of demand forecasts, you must have as much historical demand data as you can get per item or item allocation key.</span></span> <span data-ttu-id="ed2ad-106">Geçmiş talep verisi halihazırda içe aktarılmamışsa, içe aktarmak için **Geçmiş harici talep** (ReqDemPlanHistoricalExternalDemandEntity) veri varlığını Microsoft Dynamics 365 for Finance and Operations içinde kullanın.</span><span class="sxs-lookup"><span data-stu-id="ed2ad-106">If the historical demand data isn't already imported, use the **Historical external demand** (ReqDemPlanHistoricalExternalDemandEntity) data entity in Microsoft Dynamics 365 for Finance and Operations to import it.</span></span>

<span data-ttu-id="ed2ad-107">**Veri yönetimi** çalışma alanı içerisinde, varlık içerisindeki tüm alanların bir genel görünümünü görürsünüz.</span><span class="sxs-lookup"><span data-stu-id="ed2ad-107">In the **Data management** workspace, you can see an overview of all the fields in the entity.</span></span>

1. <span data-ttu-id="ed2ad-108">**Veri yönetimi** çalışma alanını açın.</span><span class="sxs-lookup"><span data-stu-id="ed2ad-108">Open the **Data management** workspace.</span></span>
2. <span data-ttu-id="ed2ad-109">**Veri varlıkları** kutucuğuna tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ed2ad-109">Click the **Data entities** tile.</span></span>
3. <span data-ttu-id="ed2ad-110">Varlık listesinde **Geçmiş harici talep** arayın.</span><span class="sxs-lookup"><span data-stu-id="ed2ad-110">Search the entity list for **Historical external demand**.</span></span>
4. <span data-ttu-id="ed2ad-111">**Hedef alanları** üzerine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ed2ad-111">Click **Target fields**.</span></span> <span data-ttu-id="ed2ad-112">Aşağıdaki varlık alanları zorunludur: site (**DeliveringSiteId**), tarih (**DemandDate**), miktar (**DemandQuantity**), ve madde numarası (**ItemNumber**) veya madde tahsisat anahtarı (**ProductAllocationKeyId**).</span><span class="sxs-lookup"><span data-stu-id="ed2ad-112">The following entity fields are mandatory: site (**DeliveringSiteId**), date (**DemandDate**), quantity (**DemandQuantity**), and either item number (**ItemNumber**) or item allocation key (**ProductAllocationKeyId**).</span></span>

<span data-ttu-id="ed2ad-113">Varlık verisini kullanmak için geçmiş talep verisini içeren Microsoft Excel dosyası veya virgülle ayrılmış değerler (CSV) dosyasına sahip olmalısınız.</span><span class="sxs-lookup"><span data-stu-id="ed2ad-113">To use the data entity, you must have a Microsoft Excel file or comma-separated values (CSV) file that contains the historical demand data.</span></span> <span data-ttu-id="ed2ad-114">Aşağıdaki örnek, verinin bir CSV dosyasından nasıl alınacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="ed2ad-114">The following example shows how to import the data from a CSV file.</span></span>

## <a name="example"></a><span data-ttu-id="ed2ad-115">Örnek</span><span class="sxs-lookup"><span data-stu-id="ed2ad-115">Example</span></span>

<span data-ttu-id="ed2ad-116">Aşağıdaki dosyayı bir örnek olarak kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="ed2ad-116">You can use the following file as an example.</span></span> <span data-ttu-id="ed2ad-117">[HistoricalDemandData](https://mbs.microsoft.com/customersource/northamerica/AX/learning/documentation/how-to-articles/365OperationsDemandForecast) karşıdan yükleyin.</span><span class="sxs-lookup"><span data-stu-id="ed2ad-117">Download the [HistoricalDemandData](https://mbs.microsoft.com/customersource/northamerica/AX/learning/documentation/how-to-articles/365OperationsDemandForecast).</span></span> <span data-ttu-id="ed2ad-118">Bu dosya, madde D0001 için geçmiş talep verisini içerir.</span><span class="sxs-lookup"><span data-stu-id="ed2ad-118">This file contains the historical demand data for item D0001.</span></span> <span data-ttu-id="ed2ad-119">Yalnızca aşağıdaki zorunlu alanları içerir: site, miktar ve talep tarihi.</span><span class="sxs-lookup"><span data-stu-id="ed2ad-119">It contains only the following mandatory fields: site, quantity, and the demand date.</span></span>

1. <span data-ttu-id="ed2ad-120">Geçmiş talep verisinin aktarılacağı şirketi seçin.</span><span class="sxs-lookup"><span data-stu-id="ed2ad-120">Select the company to import the historical demand data into.</span></span>
2. <span data-ttu-id="ed2ad-121">**Veri yönetimi** çalışma alanını açın.</span><span class="sxs-lookup"><span data-stu-id="ed2ad-121">Open the **Data management** workspace.</span></span>
3. <span data-ttu-id="ed2ad-122">**İçe aktar** kutusunu tıklatın.</span><span class="sxs-lookup"><span data-stu-id="ed2ad-122">Click the **Import** tile.</span></span>
4. <span data-ttu-id="ed2ad-123">İçe aktarma projesi için bir ad seçin, örneğin **Madde D0001 için geçmiş talep verisi içe aktar**.</span><span class="sxs-lookup"><span data-stu-id="ed2ad-123">Enter a name for the import project, such as **Import historical demand for item D0001**.</span></span>
5. <span data-ttu-id="ed2ad-124">**Kaynak veri biçimi** alanında, içe aktardığınız dosyanın dosya formatını seçin.</span><span class="sxs-lookup"><span data-stu-id="ed2ad-124">In the **Source data format** field, select the file format of the file that you're importing.</span></span> <span data-ttu-id="ed2ad-125">Bu örnek için HistoricalDemandData dosyasını içe aktarmak için, **CSV** seçeneğini işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="ed2ad-125">To import the HistoricalDemandData file for this example, select **CSV**.</span></span>
6. <span data-ttu-id="ed2ad-126">**Varlık adı** alanında, **Geçmiş harici talep** seçeneğini işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="ed2ad-126">In the **Entity name** field, select **Historical external demand**.</span></span>
7. <span data-ttu-id="ed2ad-127">Dosyayı bilgisayarınıza kaydedin ve sonra karşıya yükleyin.</span><span class="sxs-lookup"><span data-stu-id="ed2ad-127">Save the file to your computer, and then upload it.</span></span>
8. <span data-ttu-id="ed2ad-128">**İçe aktar**'ı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="ed2ad-128">Click **Import**.</span></span>
9. <span data-ttu-id="ed2ad-129">**Yürütme özeti** sayfası otomatik olarak açılır.</span><span class="sxs-lookup"><span data-stu-id="ed2ad-129">The **Execution summary** page is opened automatically.</span></span> <span data-ttu-id="ed2ad-130">İçe aktarılan veriyi sayfada doğrulayın.</span><span class="sxs-lookup"><span data-stu-id="ed2ad-130">Verify the imported data on the page.</span></span>

<span data-ttu-id="ed2ad-131">Geçmiş talep verisini içe aktardıktan sonra talep tahminleri oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="ed2ad-131">After you've imported the historical demand data, you can generate a demand forecast.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="ed2ad-132">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="ed2ad-132">Additional resources</span></span>

[<span data-ttu-id="ed2ad-133">İstatistiksel temel tahmin oluşturma</span><span class="sxs-lookup"><span data-stu-id="ed2ad-133">Generate a statistical baseline forecast</span></span>](generate-statistical-baseline-forecast.md)
