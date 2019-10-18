---
title: Proje tahminlerini doğrudan Project Service Automation'dan Finance and Operations'a eşitleme
description: Bu konuda, doğrudan Microsoft Dynamics 365 Project Service Automation'dan alınaqn proje saati tahminlerini ve proje gider tahminlerini Dynamics 365 Finance ile eşitlemek için kullanılan şablon ve temel görevler açıklanmaktadır.
author: KimANelson
manager: AnnBe
ms.date: 07/20/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.3.0
ms.openlocfilehash: 3b885610ac9ca8645358ba8ab6d46ab82143a534
ms.sourcegitcommit: 2460d0da812c45fce67a061386db52e0ae46b0f3
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/30/2019
ms.locfileid: "2250496"
---
# <a name="synchronize-project-estimates-directly-from-project-service-automation-to-finance-and-operations"></a><span data-ttu-id="1ed33-103">Proje tahminlerini doğrudan Project Service Automation'dan Finance and Operations'a eşitleme</span><span class="sxs-lookup"><span data-stu-id="1ed33-103">Synchronize project estimates directly from Project Service Automation to Finance and Operations</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="1ed33-104">Bu konu projeleri Dynamics 365 Project Service Automation üzerinden Dynamics 365 Finance üzerine proje saat tahminleri ve proje maliyet tahminlerini doğrudan eşitlemekte kullanılan şablonu ve alttaki görevleri açıklar.</span><span class="sxs-lookup"><span data-stu-id="1ed33-104">This topic describes the templates and underlying tasks that are used to synchronize project hour estimates and project expense estimates directly from Dynamics 365 Project Service Automation to Dynamics 365 Finance.</span></span>

> [!NOTE]
> - <span data-ttu-id="1ed33-105">Proje görev tümleştirmesi, gider hareket kategorileri, saat tahminleri, gider tahminleri ve işlev kilitleme gibi özellikler sürüm 8.0'da bulunmaktadır.</span><span class="sxs-lookup"><span data-stu-id="1ed33-105">Project task integration, expense transaction categories, hour estimates, expense estimates, and functionality locking is available in version 8.0.</span></span>
> - <span data-ttu-id="1ed33-106">Fiili değerlerin tümleştirmesi sürüm 8.0.1 veya sonrasında kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="1ed33-106">Actuals integration is available in version 8.0.1 or later.</span></span>

## <a name="data-flow-for-project-service-automation-to-finance"></a><span data-ttu-id="1ed33-107">Project Service Automation'dan Finance'e veri akışı</span><span class="sxs-lookup"><span data-stu-id="1ed33-107">Data flow for Project Service Automation to Finance</span></span>

<span data-ttu-id="1ed33-108">Project Service Automation ile Finance tümleştirmesi çözümünde, verileri Project Service Automation ve Finance kurulumları arasında eşitlemek için Veri tümleştirme özelliği kullanılır.</span><span class="sxs-lookup"><span data-stu-id="1ed33-108">The Project Service Automation to Finance integration solution uses the Data integration feature to synchronize data across instances of Project Service Automation and Finance.</span></span> <span data-ttu-id="1ed33-109">Veri tümleştirme özelliğiyle kullanılabilen tümleştirme şablonları, proje saat tahminleri ve proje gider tahminleri hakkındaki verilerin Project Service Automation'dan Finance'e akışına olanak tanır.</span><span class="sxs-lookup"><span data-stu-id="1ed33-109">The integration templates that are available with the Data integration feature enable the flow of data about project hour estimates and project expense estimates from Project Service Automation to Finance.</span></span>

<span data-ttu-id="1ed33-110">Aşağıdaki çizimde, verilerin Project Service Automation ile Finance arasında nasıl eşitlendiği gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="1ed33-110">The following illustration shows how the data is synchronized between Project Service Automation and Finance.</span></span>

<span data-ttu-id="1ed33-111">[![Project Service Automation ile Finance tümleştirmesi için veri akışı](./media/ProjectEstimatesFlow.png)](./media/ProjectEstimatesFlow.png)</span><span class="sxs-lookup"><span data-stu-id="1ed33-111">[![Data flow for Project Service Automation integration with Finance](./media/ProjectEstimatesFlow.png)](./media/ProjectEstimatesFlow.png)</span></span>

## <a name="project-hour-estimates"></a><span data-ttu-id="1ed33-112">Proje saat tahminleri</span><span class="sxs-lookup"><span data-stu-id="1ed33-112">Project hour estimates</span></span>

### <a name="template-and-tasks"></a><span data-ttu-id="1ed33-113">Şablon ve görevler</span><span class="sxs-lookup"><span data-stu-id="1ed33-113">Template and tasks</span></span>

<span data-ttu-id="1ed33-114">Kullanılabilecek şablonlara erişmek için, Microsoft PowerApps yönetim merkezi'nde **Projeler**'i seçin ve ardından, sağ üst köşede **Yeni proje**'yi seçerek genele açık şablonları seçin.</span><span class="sxs-lookup"><span data-stu-id="1ed33-114">To access the available templates, in the Microsoft PowerApps admin center, select **Projects**, and then, in the upper-right corner, select **New project** to select public templates.</span></span>

<span data-ttu-id="1ed33-115">Aşağıdaki şablon ve temel görevler, Project Service Automation'dan alınan proje saat tahminlerini Finance ile eşitlemek için kullanılır:</span><span class="sxs-lookup"><span data-stu-id="1ed33-115">The following template and underlying tasks are used to synchronize project hour estimates from Project Service Automation to Finance:</span></span>

- <span data-ttu-id="1ed33-116">**Veri tümleştirmedeki şablonun adı:** Proje saat tahminleri (PSA'dan Fin and Ops'a)</span><span class="sxs-lookup"><span data-stu-id="1ed33-116">**Name of the template in Data integration:** Project hour estimates (PSA to Fin and Ops)</span></span>
- <span data-ttu-id="1ed33-117">**Projedeki görevlerin adı:**</span><span class="sxs-lookup"><span data-stu-id="1ed33-117">**Name of the tasks in the project:**</span></span>

    - <span data-ttu-id="1ed33-118">Hareket ilişkileri</span><span class="sxs-lookup"><span data-stu-id="1ed33-118">Transaction relationships</span></span>
    - <span data-ttu-id="1ed33-119">Gider tahminleri</span><span class="sxs-lookup"><span data-stu-id="1ed33-119">Expense estimates</span></span>

### <a name="entity-set"></a><span data-ttu-id="1ed33-120">Varlık kümesi</span><span class="sxs-lookup"><span data-stu-id="1ed33-120">Entity set</span></span>

| <span data-ttu-id="1ed33-121">Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="1ed33-121">Project Service Automation</span></span> | <span data-ttu-id="1ed33-122">Finans</span><span class="sxs-lookup"><span data-stu-id="1ed33-122">Finance</span></span>                                       |
|----------------------------|-----------------------------------------------|
| <span data-ttu-id="1ed33-123">Proje görevleri</span><span class="sxs-lookup"><span data-stu-id="1ed33-123">Project tasks</span></span>              | <span data-ttu-id="1ed33-124">Proje saat tahminleri için tümleştirme varlığı</span><span class="sxs-lookup"><span data-stu-id="1ed33-124">Integration entity for project hour estimates</span></span> |

### <a name="entity-flow"></a><span data-ttu-id="1ed33-125">Varlık akışı</span><span class="sxs-lookup"><span data-stu-id="1ed33-125">Entity flow</span></span>

<span data-ttu-id="1ed33-126">Proje saat tahminleri, Project Service Automation'da yönetilir ve Finance ile proje saat tahminleri olarak eşitlenir.</span><span class="sxs-lookup"><span data-stu-id="1ed33-126">Project hour estimates are managed in Project Service Automation, and they are synchronized to Finance as project hour forecasts.</span></span>

### <a name="prerequisites"></a><span data-ttu-id="1ed33-127">Önkoşullar</span><span class="sxs-lookup"><span data-stu-id="1ed33-127">Prerequisites</span></span>

<span data-ttu-id="1ed33-128">Proje saat tahminlerinin eşitlemesi gerçekleşmeden önce projeleri, proje görevlerini ve proje gider hareketi kategorilerini eşitlemeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="1ed33-128">Before synchronization of project hour estimates can occur, you must synchronize projects, project tasks, and project expense transaction categories.</span></span>

### <a name="power-query"></a><span data-ttu-id="1ed33-129">Power Query</span><span class="sxs-lookup"><span data-stu-id="1ed33-129">Power Query</span></span>

<span data-ttu-id="1ed33-130">Proje saat tahminleri şablonunda şu görevleri tamamlamak için Excel için Microsoft Power Query kullanmanız gerekir:</span><span class="sxs-lookup"><span data-stu-id="1ed33-130">In the project hour estimates template, you must use Microsoft Power Query for Excel to complete these tasks:</span></span>

- <span data-ttu-id="1ed33-131">Tümleştirme yeni saat tahminleri oluştururken kullanılacak varsayılan tahmin modeli kodunu ayarlamak.</span><span class="sxs-lookup"><span data-stu-id="1ed33-131">Set the default forecast model ID that will be used when the integration creates new hour forecasts.</span></span>
- <span data-ttu-id="1ed33-132">Görev içinde, tümleştirmenin saat tahminlerini başarısız kılacak olan kaynağa özgü kayıtları filtrelemek.</span><span class="sxs-lookup"><span data-stu-id="1ed33-132">Filter out any resource-specific records in the task that will fail the integration into hour forecasts.</span></span>
- <span data-ttu-id="1ed33-133">Tüm boş hareket kategorisi satırlarını filtrelemek.</span><span class="sxs-lookup"><span data-stu-id="1ed33-133">Filter out any empty transaction category rows.</span></span> <span data-ttu-id="1ed33-134">Bu görev tamamlanmadığı takdirde saat tahminleri yanlış çıkabilir.</span><span class="sxs-lookup"><span data-stu-id="1ed33-134">Failure to complete this task might result in incorrect hour forecasts.</span></span>

#### <a name="set-the-default-forecast-model-id"></a><span data-ttu-id="1ed33-135">Varsayılan tahmin modeli kodunu ayarlama</span><span class="sxs-lookup"><span data-stu-id="1ed33-135">Set the default forecast model ID</span></span>

<span data-ttu-id="1ed33-136">Şablondaki varsayılan tahmin modeli kodunu güncelleştirmek için **Eşle** okuna tıklayarak eşlemeyi açın.</span><span class="sxs-lookup"><span data-stu-id="1ed33-136">To update the default forecast model ID in the template, click the **Map** arrow to open the mapping.</span></span> <span data-ttu-id="1ed33-137">Ardından **Gelişmiş Sorgu ve Filtreleme** bağlantısını seçin.</span><span class="sxs-lookup"><span data-stu-id="1ed33-137">Then select the **Advanced Query and Filtering** link.</span></span>

- <span data-ttu-id="1ed33-138">Varsayılan Proje saat tahminleri (PSA'dan Fin and Ops'a) şablonunu kullanıyorsanız **Uygulanan Adımlar** listesindeki **Eklenen Koşul**'u seçin.</span><span class="sxs-lookup"><span data-stu-id="1ed33-138">If you're using the default Project hour estimates (PSA to Fin and Ops) template, select the **Inserted Condition** in the list of **Applied Steps**.</span></span> <span data-ttu-id="1ed33-139">**İşlev** girişinde **O\_forecast** öğesini tümleştirmeyle kullanılacak tahmin modeli kodunun adıyla değiştirin.</span><span class="sxs-lookup"><span data-stu-id="1ed33-139">In the **Function** entry, replace **O\_forecast** with the name of the forecast model ID that should be used with the integration.</span></span> <span data-ttu-id="1ed33-140">Varsayılan şablonda, tanıtım verilerinden alınan bir tahmin modeli kodu vardır.</span><span class="sxs-lookup"><span data-stu-id="1ed33-140">The default template has a forecast model ID from the demo data.</span></span>
- <span data-ttu-id="1ed33-141">Yeni bir şablon oluşturuyorsanız bu sütunu eklemeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="1ed33-141">If you're creating a new template, you must add this column.</span></span> <span data-ttu-id="1ed33-142">Power Query'de **Koşullu Sütun Ekle**'yi seçin ve sütuna bir ad verin, örneğin **ModelKodu**.</span><span class="sxs-lookup"><span data-stu-id="1ed33-142">In Power Query, select **Add Conditional Column**, and enter a name for the new column, such as **ModelID**.</span></span> <span data-ttu-id="1ed33-143">Sütun için şu koşulu girin: where, if Project task is not null, then \<tahmin modeli kodunu girin\>; else null.</span><span class="sxs-lookup"><span data-stu-id="1ed33-143">Enter the condition for the column, where, if Project task is not null, then \<enter the forecast model ID\>; else null.</span></span>

#### <a name="filter-out-resource-specific-records"></a><span data-ttu-id="1ed33-144">Kaynağa özgü kayıtları filtreleme</span><span class="sxs-lookup"><span data-stu-id="1ed33-144">Filter out resource-specific records</span></span>

<span data-ttu-id="1ed33-145">Proje saat tahminleri (PSA'dan Fin and Ops'a) şablonunda kaynağa özgü kayıtları kaldıran bir varsayılan filtre vardır.</span><span class="sxs-lookup"><span data-stu-id="1ed33-145">The Project hour estimates (PSA to Fin and Ops) template has a default filter that removes any resource-specific records.</span></span> <span data-ttu-id="1ed33-146">Kendi şablonunuzu oluşturuyorsanız bu filtreyi eklemeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="1ed33-146">If you create your own template, you must add this filter.</span></span> <span data-ttu-id="1ed33-147">**Gelişmiş Sorgu ve Filtreleme** bağlantısını seçerek **msdyn\_islinetask** sütununda yalnızca **Yanlış** kayıtları içerecek filtreyi uygulayın.</span><span class="sxs-lookup"><span data-stu-id="1ed33-147">Select the **Advanced Query and Filtering** link to filter on the **msdyn\_islinetask** column so that only **False** records are included.</span></span>

#### <a name="filter-out-empty-transaction-category-rows"></a><span data-ttu-id="1ed33-148">Boş hareket kategorisi satırlarını filtreleme</span><span class="sxs-lookup"><span data-stu-id="1ed33-148">Filter out empty transaction category rows</span></span>

<span data-ttu-id="1ed33-149">Boş hareket kategorilerine sahip tüm satırları kaldırmak için bir filtre eklemeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="1ed33-149">You must add a filter to remove any rows that have empty transaction categories.</span></span> <span data-ttu-id="1ed33-150">Bu görev, varsayılan şablon kullanmanızdan veya kendi şablonunuzu oluşturmanızdan bağımsız olarak gereklidir.</span><span class="sxs-lookup"><span data-stu-id="1ed33-150">This task is required, regardless of whether you're using the default template or creating your own template.</span></span> <span data-ttu-id="1ed33-151">Bu filtre, Project Service Automation'dan alınan ve Finance'te saat tahminlerinin yanlış çıkmasına neden olabilecek özet satırlarını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="1ed33-151">This filter removes any summary rows from Project Service Automation that might cause the hour forecasts in Finance to be incorrect.</span></span> <span data-ttu-id="1ed33-152">**Gelişmiş Sorgu ve Filtreleme** bağlantısını seçerek **msdyn\_transactioncategory\_value** sütunundaki null kayıtları filtreleyin.</span><span class="sxs-lookup"><span data-stu-id="1ed33-152">Select **Advanced Query and Filtering** link to filter out null records in the **msdyn\_transactioncategory\_value** column.</span></span>

### <a name="template-mapping-in-data-integration"></a><span data-ttu-id="1ed33-153">Veri tümleştirmede şablon eşleme</span><span class="sxs-lookup"><span data-stu-id="1ed33-153">Template mapping in Data integration</span></span>

<span data-ttu-id="1ed33-154">Aşağıdaki şekilde, Veri tümleştirmesinde şablon görev eşlemesi örneği gösteriliyor.</span><span class="sxs-lookup"><span data-stu-id="1ed33-154">The following illustration shows an example of the template task mapping in Data integration.</span></span> <span data-ttu-id="1ed33-155">Eşlemede Project Service Automation'dan Finance'e eşitlenecek alan bilgileri gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="1ed33-155">The mapping shows the field information that will be synchronized from Project Service Automation to Finance.</span></span>

<span data-ttu-id="1ed33-156">[![Şablon eşleme](./media/ProjectHourEstimatesMapping.jpg)](./media/ProjectHourEstimatesMapping.jpg)</span><span class="sxs-lookup"><span data-stu-id="1ed33-156">[![Template mapping](./media/ProjectHourEstimatesMapping.jpg)](./media/ProjectHourEstimatesMapping.jpg)</span></span>

## <a name="project-expense-estimates"></a><span data-ttu-id="1ed33-157">Proje gideri tahminleri</span><span class="sxs-lookup"><span data-stu-id="1ed33-157">Project expense estimates</span></span>

### <a name="template-and-tasks"></a><span data-ttu-id="1ed33-158">Şablon ve görevler</span><span class="sxs-lookup"><span data-stu-id="1ed33-158">Template and tasks</span></span>

<span data-ttu-id="1ed33-159">Aşağıdaki şablon ve temel görevler, Project Service Automation'dan alınan proje gider tahminlerini Finance ile eşitlemek için kullanılır:</span><span class="sxs-lookup"><span data-stu-id="1ed33-159">The following template and underlying tasks are used to synchronize project expense estimates from Project Service Automation to Finance:</span></span>

- <span data-ttu-id="1ed33-160">**Veri tümleştirmedeki şablonun adı:** Proje gider tahminleri (PSA'dan Fin and Ops'a)</span><span class="sxs-lookup"><span data-stu-id="1ed33-160">**Name of the template in Data integration:** Project expense estimates (PSA to Fin and Ops)</span></span>
- <span data-ttu-id="1ed33-161">**Projedeki görevlerin adı:**</span><span class="sxs-lookup"><span data-stu-id="1ed33-161">**Name of the tasks in the project:**</span></span>

    - <span data-ttu-id="1ed33-162">Hareket ilişkileri</span><span class="sxs-lookup"><span data-stu-id="1ed33-162">Transaction relationships</span></span> 
    - <span data-ttu-id="1ed33-163">Gider tahminleri</span><span class="sxs-lookup"><span data-stu-id="1ed33-163">Expense estimates</span></span>

### <a name="entity-set"></a><span data-ttu-id="1ed33-164">Varlık kümesi</span><span class="sxs-lookup"><span data-stu-id="1ed33-164">Entity set</span></span>

| <span data-ttu-id="1ed33-165">Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="1ed33-165">Project Service Automation</span></span> | <span data-ttu-id="1ed33-166">Finans</span><span class="sxs-lookup"><span data-stu-id="1ed33-166">Finance</span></span>                                                  |
|----------------------------|----------------------------------------------------------|
| <span data-ttu-id="1ed33-167">Hareket Bağlantıları</span><span class="sxs-lookup"><span data-stu-id="1ed33-167">Transaction Connections</span></span>    | <span data-ttu-id="1ed33-168">Proje hareketi ilişkileri için tümleştirme varlığı</span><span class="sxs-lookup"><span data-stu-id="1ed33-168">Integration entity for project transaction relationships</span></span> |
| <span data-ttu-id="1ed33-169">Tahmin Satırları</span><span class="sxs-lookup"><span data-stu-id="1ed33-169">Estimate Lines</span></span>             | <span data-ttu-id="1ed33-170">Proje gider tahminleri için tümleştirme varlığı</span><span class="sxs-lookup"><span data-stu-id="1ed33-170">Integration entity for project expense estimates</span></span>         |

### <a name="entity-flow"></a><span data-ttu-id="1ed33-171">Varlık akışı</span><span class="sxs-lookup"><span data-stu-id="1ed33-171">Entity flow</span></span>

<span data-ttu-id="1ed33-172">Proje gider tahminleri, Project Service Automation'da yönetilir ve Finance ile proje gider tahminleri olarak eşitlenir.</span><span class="sxs-lookup"><span data-stu-id="1ed33-172">Project expense estimates are managed in Project Service Automation, and they are synchronized to Finance as project expense forecasts.</span></span>

### <a name="prerequisites"></a><span data-ttu-id="1ed33-173">Önkoşullar</span><span class="sxs-lookup"><span data-stu-id="1ed33-173">Prerequisites</span></span>

<span data-ttu-id="1ed33-174">Proje gider tahminleri eşitlenmeden önce projeleri, proje görevlerini ve proje gider hareketi kategorilerini eşitlemeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="1ed33-174">Before synchronization of project expense estimates can occur, you must synchronize projects, project tasks, and project expense transaction categories.</span></span>

### <a name="power-query"></a><span data-ttu-id="1ed33-175">Power Query</span><span class="sxs-lookup"><span data-stu-id="1ed33-175">Power Query</span></span>

<span data-ttu-id="1ed33-176">Proje gider tahminleri şablonunda aşağıdaki görevleri tamamlamak için Power Query kullanmanız gerekir:</span><span class="sxs-lookup"><span data-stu-id="1ed33-176">In the project expense estimates template, you must use Power Query to complete the following tasks:</span></span>

- <span data-ttu-id="1ed33-177">Yalnızca gider tahmini satır kayıtlarını içerecek şekilde filtreleyin.</span><span class="sxs-lookup"><span data-stu-id="1ed33-177">Filter to include only expense estimate line records.</span></span>
- <span data-ttu-id="1ed33-178">Tümleştirme yeni saat tahminleri oluştururken kullanılacak varsayılan tahmin modeli kodunu ayarlamak.</span><span class="sxs-lookup"><span data-stu-id="1ed33-178">Set the default forecast model ID that will be used when the integration creates new hour forecasts.</span></span>
- <span data-ttu-id="1ed33-179">Faturalama türlerini dönüştürmek.</span><span class="sxs-lookup"><span data-stu-id="1ed33-179">Transform the billing types.</span></span>
- <span data-ttu-id="1ed33-180">Hareket türlerini dönüştürmek.</span><span class="sxs-lookup"><span data-stu-id="1ed33-180">Transform the transaction types.</span></span>

#### <a name="filter-to-include-only-expense-estimate-lines"></a><span data-ttu-id="1ed33-181">Yalnızca gider tahmini satırlarını içerecek filtre uygulama</span><span class="sxs-lookup"><span data-stu-id="1ed33-181">Filter to include only expense estimate lines</span></span>

<span data-ttu-id="1ed33-182">Project gider tahminleri (PSA'dan Fin and Ops'a) şablonunda, tümleştirmede yalnızca gider satırlarını içeren bir varsayılan filtre vardır.</span><span class="sxs-lookup"><span data-stu-id="1ed33-182">The Project expense estimates (PSA to Fin and Ops) template has a default filter that includes only expense lines in the integration.</span></span> <span data-ttu-id="1ed33-183">Kendi şablonunuzu oluşturuyorsanız bu filtreyi eklemeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="1ed33-183">If you create your own template, you must add this filter.</span></span> <span data-ttu-id="1ed33-184">**Hareket ilişkileri** görevini seçin ve ardından eşlemeyi açmak için **Eşle** okuna tıklayın.</span><span class="sxs-lookup"><span data-stu-id="1ed33-184">Select the **Transaction relationships** task, and then click the **Map** arrow to open the mapping.</span></span> <span data-ttu-id="1ed33-185">**Gelişmiş Sorgu ve Filtreleme** bağlantısını seçin.</span><span class="sxs-lookup"><span data-stu-id="1ed33-185">Select the **Advanced Query and Filtering** link.</span></span> <span data-ttu-id="1ed33-186">**msdyn\_transactiontype1** sütununu yalnızca **msdyn\_estimateline** öğesini içerecek şekilde filtreleyin.</span><span class="sxs-lookup"><span data-stu-id="1ed33-186">Filter the **msdyn\_transactiontype1** column so that it includes only **msdyn\_estimateline**.</span></span>

#### <a name="set-the-default-forecast-model-id"></a><span data-ttu-id="1ed33-187">Varsayılan tahmin modeli kodunu ayarlama</span><span class="sxs-lookup"><span data-stu-id="1ed33-187">Set the default forecast model ID</span></span>

<span data-ttu-id="1ed33-188">Şablondaki varsayılan tahmin modeli kodunu güncelleştirmek için **Gider tahminleri** görevini seçin ve ardından eşlemeyi açmak için **Eşle** okuna tıklayın.</span><span class="sxs-lookup"><span data-stu-id="1ed33-188">To update the default forecast model ID in the template, select the **Expense estimates** task, and then click the **Map** arrow to open the mapping.</span></span> <span data-ttu-id="1ed33-189">**Gelişmiş Sorgu ve Filtreleme** bağlantısını seçin.</span><span class="sxs-lookup"><span data-stu-id="1ed33-189">Select the **Advanced Query and Filtering** link.</span></span>

- <span data-ttu-id="1ed33-190">Power Query'de varsayılan Proje gider tahminleri (PSA'dan Fin and Ops'a) şablonunu kullanıyorsanız **Uygulanan Adımlar** bölümünden ilk **Eklenen Koşul**'u seçin.</span><span class="sxs-lookup"><span data-stu-id="1ed33-190">If you're using the default Project expense estimates (PSA to Fin and Ops) template, in Power Query, select the first **Inserted Condition** from the **Applied Steps** section.</span></span> <span data-ttu-id="1ed33-191">**İşlev** girişinde **O\_forecast** öğesini tümleştirmeyle kullanılacak tahmin modeli kodunun adıyla değiştirin.</span><span class="sxs-lookup"><span data-stu-id="1ed33-191">In the **Function** entry, replace **O\_forecast** with the name of the forecast model ID that should be used with the integration.</span></span> <span data-ttu-id="1ed33-192">Varsayılan şablonda, tanıtım verilerinden alınan bir tahmin modeli kodu vardır.</span><span class="sxs-lookup"><span data-stu-id="1ed33-192">The default template has a forecast model ID from the demo data.</span></span>
- <span data-ttu-id="1ed33-193">Yeni bir şablon oluşturuyorsanız bu sütunu eklemeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="1ed33-193">If you're creating a new template, you must add this column.</span></span> <span data-ttu-id="1ed33-194">Power Query'de **Koşullu Sütun Ekle**'yi seçin ve sütuna bir ad verin, örneğin **ModelKodu**.</span><span class="sxs-lookup"><span data-stu-id="1ed33-194">In Power Query, select **Add Conditional Column**, and enter a name for the new column, such as **ModelID**.</span></span> <span data-ttu-id="1ed33-195">Sütun için şu koşulu girin: where, if Estimate line ID is not null, then \<tahmin modeli kodunu girin\>; else null.</span><span class="sxs-lookup"><span data-stu-id="1ed33-195">Enter the condition for the column, where, if Estimate line ID is not null, then \<enter the forecast model ID\>; else null.</span></span>

#### <a name="transform-the-billing-types"></a><span data-ttu-id="1ed33-196">Faturalama türlerini dönüştürme</span><span class="sxs-lookup"><span data-stu-id="1ed33-196">Transform the billing types</span></span>

<span data-ttu-id="1ed33-197">Proje gider tahminleri (PSA'dan Fin and Ops'a) şablonunda, tümleştirme sırasında Project Service Automation'dan alınan faturalama türlerini dönüştürmek için kullanılan bir koşullu sütun vardır.</span><span class="sxs-lookup"><span data-stu-id="1ed33-197">The Project expense estimates (PSA to Fin and Ops) template includes a conditional column that is used to transform the billing types that are received from Project Service Automation during the integration.</span></span> <span data-ttu-id="1ed33-198">Kendi şablonunuzu oluşturuyorsanız bu koşullu sütunu eklemeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="1ed33-198">If you create your own template, you must add this conditional column.</span></span> <span data-ttu-id="1ed33-199">**Gelişmiş Sorgu ve Filtreleme** bağlantısını seçin ve ardından **Koşullu Sütun Ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="1ed33-199">Select the **Advanced Query and Filtering** link and then select **Add Conditional Column**.</span></span> <span data-ttu-id="1ed33-200">Yeni sütun için **Faturalama Türü** gibi bir ad girin.</span><span class="sxs-lookup"><span data-stu-id="1ed33-200">Enter a name for the new column, such as **BillingType**.</span></span> <span data-ttu-id="1ed33-201">Ardından aşağıdaki koşulu girin:</span><span class="sxs-lookup"><span data-stu-id="1ed33-201">Then enter the following condition:</span></span>

<span data-ttu-id="1ed33-202">If **msdyn\_billingtype** = 192350000, then **Masraflandırılamaz**</span><span class="sxs-lookup"><span data-stu-id="1ed33-202">If **msdyn\_billingtype** = 192350000, then **NonChargeable**</span></span>  
<span data-ttu-id="1ed33-203">else if **msdyn\_billingtype** = 192350001, then **Masraflandırılabilir**</span><span class="sxs-lookup"><span data-stu-id="1ed33-203">else if **msdyn\_billingtype** = 192350001, then **Chargeable**</span></span>  
<span data-ttu-id="1ed33-204">else if **msdyn\_billingtype** = 192350002, then **Karşılıksız**</span><span class="sxs-lookup"><span data-stu-id="1ed33-204">else if **msdyn\_billingtype** = 192350002, then **Complimentary**</span></span>  
<span data-ttu-id="1ed33-205">else **Yok**</span><span class="sxs-lookup"><span data-stu-id="1ed33-205">else **NotAvailable**</span></span>

#### <a name="transform-the-transaction-types"></a><span data-ttu-id="1ed33-206">Hareket türlerini dönüştürme</span><span class="sxs-lookup"><span data-stu-id="1ed33-206">Transform the transaction types</span></span>

<span data-ttu-id="1ed33-207">Proje gider tahminleri (PSA'dan Fin and Ops'a) şablonunda, tümleştirme sırasında Project Service Automation'dan alınan hareket türlerini dönüştürmek için kullanılan bir koşullu sütun vardır.</span><span class="sxs-lookup"><span data-stu-id="1ed33-207">The Project expense estimates (PSA to Fin and Ops) template includes a conditional column that is used to transform the transaction types that are received from Project Service Automation during the integration.</span></span> <span data-ttu-id="1ed33-208">Kendi şablonunuzu oluşturuyorsanız bu koşullu sütunu eklemeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="1ed33-208">If you create your own template, you must add this conditional column.</span></span> <span data-ttu-id="1ed33-209">**Gelişmiş Sorgu ve Filtreleme** bağlantısını seçin ve ardından **Koşullu Sütun Ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="1ed33-209">Select the **Advanced Query and Filtering** link and then select **Add Conditional Column**.</span></span> <span data-ttu-id="1ed33-210">Yeni sütun için **Hareket Türü** gibi bir ad girin.</span><span class="sxs-lookup"><span data-stu-id="1ed33-210">Enter a name for the new column, such as **TransactionType**.</span></span> <span data-ttu-id="1ed33-211">Ardından aşağıdaki koşulu girin:</span><span class="sxs-lookup"><span data-stu-id="1ed33-211">Then enter the following condition:</span></span>

<span data-ttu-id="1ed33-212">If **msdyn\_transactiontypecode** = 192350000, then **Maliyet**</span><span class="sxs-lookup"><span data-stu-id="1ed33-212">If **msdyn\_transactiontypecode** = 192350000, then **Cost**</span></span>  
<span data-ttu-id="1ed33-213">else if **msdyn\_transactiontypecode** = 192350005, then **Satış**</span><span class="sxs-lookup"><span data-stu-id="1ed33-213">else if **msdyn\_transactiontypecode** = 192350005, then **Sales**</span></span>  
<span data-ttu-id="1ed33-214">else **null**</span><span class="sxs-lookup"><span data-stu-id="1ed33-214">else **null**</span></span>

### <a name="template-mapping-in-data-integration"></a><span data-ttu-id="1ed33-215">Veri tümleştirmede şablon eşleme</span><span class="sxs-lookup"><span data-stu-id="1ed33-215">Template mapping in Data integration</span></span>

<span data-ttu-id="1ed33-216">Aşağıdaki şekillerde, Veri tümleştirmesinde şablon görevi eşleşmelerine örnekler gösteriliyor.</span><span class="sxs-lookup"><span data-stu-id="1ed33-216">The following illustrations show examples of the template task mappings in Data integration.</span></span> <span data-ttu-id="1ed33-217">Eşlemede Project Service Automation'dan Finance'e eşitlenecek alan bilgileri gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="1ed33-217">The mapping shows the field information that will be synchronized from Project Service Automation to Finance.</span></span>

<span data-ttu-id="1ed33-218">[![Şablon eşleme](./media/ExpenseEstimateTransactionRelationshipsMapping.jpg)](./media/ExpenseEstimateTransactionRelationshipsMapping.jpg)</span><span class="sxs-lookup"><span data-stu-id="1ed33-218">[![Template mapping](./media/ExpenseEstimateTransactionRelationshipsMapping.jpg)](./media/ExpenseEstimateTransactionRelationshipsMapping.jpg)</span></span>

<span data-ttu-id="1ed33-219">[![Şablon eşleme](./media/ExpenseEstimatesMapping.jpg)](./media/ExpenseEstimatesMapping.jpg)</span><span class="sxs-lookup"><span data-stu-id="1ed33-219">[![Template mapping](./media/ExpenseEstimatesMapping.jpg)](./media/ExpenseEstimatesMapping.jpg)</span></span>
