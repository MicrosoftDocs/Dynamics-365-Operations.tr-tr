---
title: Proje tahminlerini doğrudan Project Service Automation'dan Finance and Operations'a eşitleme
description: Bu konu projeleri Microsoft Dynamics 365 for Project Service Automation üzerinden Microsoft Dynamics 365 for Finance and Operations üzerine proje saat tahminleri ve proje maliyet tahminlerini doğrudan eşitlemekte kullanılan şablonu ve alttaki görevleri açıklar.
author: KimANelson
manager: AnnBe
ms.date: 07/20/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.3.0
ms.openlocfilehash: 21338b889e0377dbfd5adfd461ea81b39a75baf8
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/15/2019
ms.locfileid: "1556564"
---
# <a name="synchronize-project-estimates-directly-from-project-service-automation-to-finance-and-operations"></a><span data-ttu-id="cf08a-103">Proje tahminlerini doğrudan Project Service Automation'dan Finance and Operations'a eşitleme</span><span class="sxs-lookup"><span data-stu-id="cf08a-103">Synchronize project estimates directly from Project Service Automation to Finance and Operations</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="cf08a-104">Bu konu projeleri Microsoft Dynamics 365 for Project Service Automation üzerinden Dynamics 365 for Finance and Operations üzerine proje saat tahminleri ve proje maliyet tahminlerini doğrudan eşitlemekte kullanılan şablonu ve alttaki görevleri açıklar.</span><span class="sxs-lookup"><span data-stu-id="cf08a-104">This topic describes the templates and underlying tasks that are used to synchronize project hour estimates and project expense estimates directly from Microsoft Dynamics 365 for Project Service Automation to Dynamics 365 for Finance and Operations.</span></span>

> [!NOTE]
> - <span data-ttu-id="cf08a-105">Proje görev tümleştirmesi, gider hareket kategorileri, saat tahminleri, gider tahminleri ve işlev kilitleme Microsoft Dynamics 365 for Finance and Operations sürüm 8.0 içinde kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="cf08a-105">Project task integration, expense transaction categories, hour estimates, expense estimates, and functionality locking is available in Microsoft Dynamics 365 for Finance and Operations version 8.0.</span></span>
> - <span data-ttu-id="cf08a-106">Fiili değerlerin tümleştirmesi Microsoft Dynamics 365 for Finance and Operations sürüm 8.0.1 veya sonrasında kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="cf08a-106">Actuals integration is available in Microsoft Dynamics 365 for Finance and Operations version 8.0.1 or later.</span></span>
> - <span data-ttu-id="cf08a-107">Microsoft Dynamics 365 for Finance and Operations, Enterprise edition 7.3.0 kullanıyorsanız, KB 4132657 ve KB 4132660 yükledikten sonra, proje görevlerini, gider hareketi kategorilerini, saat tahminlerini, gider tahminlerini ve gerçek değerleri tümleştirmek ve işlev kilitlemeyi yapılandırmak için şablonları kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="cf08a-107">If you're using Microsoft Dynamics 365 for Finance and Operations, Enterprise edition 7.3.0, after you install KB 4132657 and KB 4132660, you will be able to use the templates to integrate project tasks, expense transaction categories, hour estimates, expense estimates, and actuals, and to configure functionality locking.</span></span> <span data-ttu-id="cf08a-108">Muhasebe dağıtımlarını sıfırlamanız gerekiyorsa KB 4131710'u da yüklemenizi öneririz.</span><span class="sxs-lookup"><span data-stu-id="cf08a-108">If you must reset the accounting distributions, we recommend that you also install KB 4131710.</span></span>

## <a name="data-flow-for-project-service-automation-to-finance-and-operations"></a><span data-ttu-id="cf08a-109">Project Service Automation'dan Finance and Operations'a veri akışı</span><span class="sxs-lookup"><span data-stu-id="cf08a-109">Data flow for Project Service Automation to Finance and Operations</span></span>

<span data-ttu-id="cf08a-110">Project Service Automation'dan Finance and Operations'a tümleştirme çözümünde, Project Service Automation ve Finance and Operations örnekleri arasında veri eşitlemek için Veri tümleştirme özelliği kullanılır.</span><span class="sxs-lookup"><span data-stu-id="cf08a-110">The Project Service Automation to Finance and Operations integration solution uses the Data integration feature to synchronize data across instances of Project Service Automation and Finance and Operations.</span></span> <span data-ttu-id="cf08a-111">Veri tümleştirme özelliğiyle kullanılabilen tümleştirme şablonları, proje saat tahminleri ve proje gider tahminleri hakkındaki verilerin Project Service Automation'dan Finance and Operations'a akışına olanak sağlar.</span><span class="sxs-lookup"><span data-stu-id="cf08a-111">The integration templates that are available with the Data integration feature enable the flow of data about project hour estimates and project expense estimates from Project Service Automation to Finance and Operations.</span></span>

<span data-ttu-id="cf08a-112">Aşağıdaki şekilde Project Service Automation ile Finance and Operations arasında verilerin nasıl eşitlendiği gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="cf08a-112">The following illustration shows how the data is synchronized between Project Service Automation and Finance and Operations.</span></span>

<span data-ttu-id="cf08a-113">[![Finance and Operations ile Project Service Automation tümleştirmesi için veri akışı](./media/ProjectEstimatesFlow.png)](./media/ProjectEstimatesFlow.png)</span><span class="sxs-lookup"><span data-stu-id="cf08a-113">[![Data flow for Project Service Automation integration with Finance and Operations](./media/ProjectEstimatesFlow.png)](./media/ProjectEstimatesFlow.png)</span></span>

## <a name="project-hour-estimates"></a><span data-ttu-id="cf08a-114">Proje saat tahminleri</span><span class="sxs-lookup"><span data-stu-id="cf08a-114">Project hour estimates</span></span>

### <a name="template-and-tasks"></a><span data-ttu-id="cf08a-115">Şablon ve görevler</span><span class="sxs-lookup"><span data-stu-id="cf08a-115">Template and tasks</span></span>

<span data-ttu-id="cf08a-116">Kullanılabilecek şablonlara erişmek için, Microsoft PowerApps yönetim merkezi'nde **Projeler**'i seçin ve ardından, sağ üst köşede **Yeni proje**'yi seçerek genele açık şablonları seçin.</span><span class="sxs-lookup"><span data-stu-id="cf08a-116">To access the available templates, in the Microsoft PowerApps admin center, select **Projects**, and then, in the upper-right corner, select **New project** to select public templates.</span></span>

<span data-ttu-id="cf08a-117">Aşağıdaki şablon ve temel görevler, proje saat tahminlerini Project Service Automation'dan Finance and Operations'a eşitlemek için kullanılır:</span><span class="sxs-lookup"><span data-stu-id="cf08a-117">The following template and underlying tasks are used to synchronize project hour estimates from Project Service Automation to Finance and Operations:</span></span>

- <span data-ttu-id="cf08a-118">**Veri tümleştirmedeki şablonun adı:** Proje saat tahminleri (PSA'dan Fin and Ops'a)</span><span class="sxs-lookup"><span data-stu-id="cf08a-118">**Name of the template in Data integration:** Project hour estimates (PSA to Fin and Ops)</span></span>
- <span data-ttu-id="cf08a-119">**Projedeki görevlerin adı:**</span><span class="sxs-lookup"><span data-stu-id="cf08a-119">**Name of the tasks in the project:**</span></span>

    - <span data-ttu-id="cf08a-120">Hareket ilişkileri</span><span class="sxs-lookup"><span data-stu-id="cf08a-120">Transaction relationships</span></span>
    - <span data-ttu-id="cf08a-121">Gider tahminleri</span><span class="sxs-lookup"><span data-stu-id="cf08a-121">Expense estimates</span></span>

### <a name="entity-set"></a><span data-ttu-id="cf08a-122">Varlık kümesi</span><span class="sxs-lookup"><span data-stu-id="cf08a-122">Entity set</span></span>

| <span data-ttu-id="cf08a-123">Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="cf08a-123">Project Service Automation</span></span> | <span data-ttu-id="cf08a-124">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="cf08a-124">Finance and Operations</span></span>                        |
|----------------------------|-----------------------------------------------|
| <span data-ttu-id="cf08a-125">Proje görevleri</span><span class="sxs-lookup"><span data-stu-id="cf08a-125">Project tasks</span></span>              | <span data-ttu-id="cf08a-126">Proje saat tahminleri için tümleştirme varlığı</span><span class="sxs-lookup"><span data-stu-id="cf08a-126">Integration entity for project hour estimates</span></span> |

### <a name="entity-flow"></a><span data-ttu-id="cf08a-127">Varlık akışı</span><span class="sxs-lookup"><span data-stu-id="cf08a-127">Entity flow</span></span>

<span data-ttu-id="cf08a-128">Proje saat tahminleri Project Service Automation'da yönetilir ve Finance and Operations'a proje saat tahminleri olarak eşitlenir.</span><span class="sxs-lookup"><span data-stu-id="cf08a-128">Project hour estimates are managed in Project Service Automation, and they are synchronized to Finance and Operations as project hour forecasts.</span></span>

### <a name="prerequisites"></a><span data-ttu-id="cf08a-129">Ön koşullar</span><span class="sxs-lookup"><span data-stu-id="cf08a-129">Prerequisites</span></span>

<span data-ttu-id="cf08a-130">Proje saat tahminlerinin eşitlemesi gerçekleşmeden önce projeleri, proje görevlerini ve proje gider hareketi kategorilerini eşitlemeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="cf08a-130">Before synchronization of project hour estimates can occur, you must synchronize projects, project tasks, and project expense transaction categories.</span></span>

### <a name="power-query"></a><span data-ttu-id="cf08a-131">Power Query</span><span class="sxs-lookup"><span data-stu-id="cf08a-131">Power Query</span></span>

<span data-ttu-id="cf08a-132">Proje saat tahminleri şablonunda şu görevleri tamamlamak için Excel için Microsoft Power Query kullanmanız gerekir:</span><span class="sxs-lookup"><span data-stu-id="cf08a-132">In the project hour estimates template, you must use Microsoft Power Query for Excel to complete these tasks:</span></span>

- <span data-ttu-id="cf08a-133">Tümleştirme yeni saat tahminleri oluştururken kullanılacak varsayılan tahmin modeli kodunu ayarlamak.</span><span class="sxs-lookup"><span data-stu-id="cf08a-133">Set the default forecast model ID that will be used when the integration creates new hour forecasts.</span></span>
- <span data-ttu-id="cf08a-134">Görev içinde, tümleştirmenin saat tahminlerini başarısız kılacak olan kaynağa özgü kayıtları filtrelemek.</span><span class="sxs-lookup"><span data-stu-id="cf08a-134">Filter out any resource-specific records in the task that will fail the integration into hour forecasts.</span></span>
- <span data-ttu-id="cf08a-135">Tüm boş hareket kategorisi satırlarını filtrelemek.</span><span class="sxs-lookup"><span data-stu-id="cf08a-135">Filter out any empty transaction category rows.</span></span> <span data-ttu-id="cf08a-136">Bu görev tamamlanmadığı takdirde saat tahminleri yanlış çıkabilir.</span><span class="sxs-lookup"><span data-stu-id="cf08a-136">Failure to complete this task might result in incorrect hour forecasts.</span></span>

#### <a name="set-the-default-forecast-model-id"></a><span data-ttu-id="cf08a-137">Varsayılan tahmin modeli kodunu ayarlama</span><span class="sxs-lookup"><span data-stu-id="cf08a-137">Set the default forecast model ID</span></span>

<span data-ttu-id="cf08a-138">Şablondaki varsayılan tahmin modeli kodunu güncelleştirmek için **Eşle** okuna tıklayarak eşlemeyi açın.</span><span class="sxs-lookup"><span data-stu-id="cf08a-138">To update the default forecast model ID in the template, click the **Map** arrow to open the mapping.</span></span> <span data-ttu-id="cf08a-139">Ardından **Gelişmiş Sorgu ve Filtreleme** bağlantısını seçin.</span><span class="sxs-lookup"><span data-stu-id="cf08a-139">Then select the **Advanced Query and Filtering** link.</span></span>

- <span data-ttu-id="cf08a-140">Varsayılan Proje saat tahminleri (PSA'dan Fin and Ops'a) şablonunu kullanıyorsanız **Uygulanan Adımlar** listesindeki **Eklenen Koşul**'u seçin.</span><span class="sxs-lookup"><span data-stu-id="cf08a-140">If you're using the default Project hour estimates (PSA to Fin and Ops) template, select the **Inserted Condition** in the list of **Applied Steps**.</span></span> <span data-ttu-id="cf08a-141">**İşlev** girişinde **O\_forecast** öğesini tümleştirmeyle kullanılacak tahmin modeli kodunun adıyla değiştirin.</span><span class="sxs-lookup"><span data-stu-id="cf08a-141">In the **Function** entry, replace **O\_forecast** with the name of the forecast model ID that should be used with the integration.</span></span> <span data-ttu-id="cf08a-142">Varsayılan şablonda, tanıtım verilerinden alınan bir tahmin modeli kodu vardır.</span><span class="sxs-lookup"><span data-stu-id="cf08a-142">The default template has a forecast model ID from the demo data.</span></span>
- <span data-ttu-id="cf08a-143">Yeni bir şablon oluşturuyorsanız bu sütunu eklemeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="cf08a-143">If you're creating a new template, you must add this column.</span></span> <span data-ttu-id="cf08a-144">Power Query'de **Koşullu Sütun Ekle**'yi seçin ve sütuna bir ad verin, örneğin **ModelKodu**.</span><span class="sxs-lookup"><span data-stu-id="cf08a-144">In Power Query, select **Add Conditional Column**, and enter a name for the new column, such as **ModelID**.</span></span> <span data-ttu-id="cf08a-145">Sütun için şu koşulu girin: where, if Project task is not null, then \<tahmin modeli kodunu girin\>; else null.</span><span class="sxs-lookup"><span data-stu-id="cf08a-145">Enter the condition for the column, where, if Project task is not null, then \<enter the forecast model ID\>; else null.</span></span>

#### <a name="filter-out-resource-specific-records"></a><span data-ttu-id="cf08a-146">Kaynağa özgü kayıtları filtreleme</span><span class="sxs-lookup"><span data-stu-id="cf08a-146">Filter out resource-specific records</span></span>

<span data-ttu-id="cf08a-147">Proje saat tahminleri (PSA'dan Fin and Ops'a) şablonunda kaynağa özgü kayıtları kaldıran bir varsayılan filtre vardır.</span><span class="sxs-lookup"><span data-stu-id="cf08a-147">The Project hour estimates (PSA to Fin and Ops) template has a default filter that removes any resource-specific records.</span></span> <span data-ttu-id="cf08a-148">Kendi şablonunuzu oluşturuyorsanız bu filtreyi eklemeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="cf08a-148">If you create your own template, you must add this filter.</span></span> <span data-ttu-id="cf08a-149">**Gelişmiş Sorgu ve Filtreleme** bağlantısını seçerek **msdyn\_islinetask** sütununda yalnızca **Yanlış** kayıtları içerecek filtreyi uygulayın.</span><span class="sxs-lookup"><span data-stu-id="cf08a-149">Select the **Advanced Query and Filtering** link to filter on the **msdyn\_islinetask** column so that only **False** records are included.</span></span>

#### <a name="filter-out-empty-transaction-category-rows"></a><span data-ttu-id="cf08a-150">Boş hareket kategorisi satırlarını filtreleme</span><span class="sxs-lookup"><span data-stu-id="cf08a-150">Filter out empty transaction category rows</span></span>

<span data-ttu-id="cf08a-151">Boş hareket kategorilerine sahip tüm satırları kaldırmak için bir filtre eklemeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="cf08a-151">You must add a filter to remove any rows that have empty transaction categories.</span></span> <span data-ttu-id="cf08a-152">Bu görev, varsayılan şablon kullanmanızdan veya kendi şablonunuzu oluşturmanızdan bağımsız olarak gereklidir.</span><span class="sxs-lookup"><span data-stu-id="cf08a-152">This task is required, regardless of whether you're using the default template or creating your own template.</span></span> <span data-ttu-id="cf08a-153">Bu filtre, Project Service Automation'dan gelen ve Finance and Operations'ta saat tahminlerinin yanlış çıkmasına neden olabilecek özet satırlarını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="cf08a-153">This filter removes any summary rows from Project Service Automation that might cause the hour forecasts in Finance and Operations to be incorrect.</span></span> <span data-ttu-id="cf08a-154">**Gelişmiş Sorgu ve Filtreleme** bağlantısını seçerek **msdyn\_transactioncategory\_value** sütunundaki null kayıtları filtreleyin.</span><span class="sxs-lookup"><span data-stu-id="cf08a-154">Select **Advanced Query and Filtering** link to filter out null records in the **msdyn\_transactioncategory\_value** column.</span></span>

### <a name="template-mapping-in-data-integration"></a><span data-ttu-id="cf08a-155">Veri tümleştirmede şablon eşleme</span><span class="sxs-lookup"><span data-stu-id="cf08a-155">Template mapping in Data integration</span></span>

<span data-ttu-id="cf08a-156">Aşağıdaki şekilde, Veri tümleştirmesinde şablon görev eşlemesi örneği gösteriliyor.</span><span class="sxs-lookup"><span data-stu-id="cf08a-156">The following illustration shows an example of the template task mapping in Data integration.</span></span> <span data-ttu-id="cf08a-157">Eşleme, Project Service Automation'dan Finance and Operations'a eşitlenecek alan bilgilerini gösterir.</span><span class="sxs-lookup"><span data-stu-id="cf08a-157">The mapping shows the field information that will be synchronized from Project Service Automation to Finance and Operations.</span></span>

<span data-ttu-id="cf08a-158">[![Şablon eşleme](./media/ProjectHourEstimatesMapping.jpg)](./media/ProjectHourEstimatesMapping.jpg)</span><span class="sxs-lookup"><span data-stu-id="cf08a-158">[![Template mapping](./media/ProjectHourEstimatesMapping.jpg)](./media/ProjectHourEstimatesMapping.jpg)</span></span>

## <a name="project-expense-estimates"></a><span data-ttu-id="cf08a-159">Proje gideri tahminleri</span><span class="sxs-lookup"><span data-stu-id="cf08a-159">Project expense estimates</span></span>

### <a name="template-and-tasks"></a><span data-ttu-id="cf08a-160">Şablon ve görevler</span><span class="sxs-lookup"><span data-stu-id="cf08a-160">Template and tasks</span></span>

<span data-ttu-id="cf08a-161">Aşağıdaki şablon ve temel görevler, proje gider tahminlerini Project Service Automation'dan Finance and Operations'a eşitlemek için kullanılır:</span><span class="sxs-lookup"><span data-stu-id="cf08a-161">The following template and underlying tasks are used to synchronize project expense estimates from Project Service Automation to Finance and Operations:</span></span>

- <span data-ttu-id="cf08a-162">**Veri tümleştirmedeki şablonun adı:** Proje gider tahminleri (PSA'dan Fin and Ops'a)</span><span class="sxs-lookup"><span data-stu-id="cf08a-162">**Name of the template in Data integration:** Project expense estimates (PSA to Fin and Ops)</span></span>
- <span data-ttu-id="cf08a-163">**Projedeki görevlerin adı:**</span><span class="sxs-lookup"><span data-stu-id="cf08a-163">**Name of the tasks in the project:**</span></span>

    - <span data-ttu-id="cf08a-164">Hareket ilişkileri</span><span class="sxs-lookup"><span data-stu-id="cf08a-164">Transaction relationships</span></span> 
    - <span data-ttu-id="cf08a-165">Gider tahminleri</span><span class="sxs-lookup"><span data-stu-id="cf08a-165">Expense estimates</span></span>

### <a name="entity-set"></a><span data-ttu-id="cf08a-166">Varlık kümesi</span><span class="sxs-lookup"><span data-stu-id="cf08a-166">Entity set</span></span>

| <span data-ttu-id="cf08a-167">Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="cf08a-167">Project Service Automation</span></span> | <span data-ttu-id="cf08a-168">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="cf08a-168">Finance and Operations</span></span>                                   |
|----------------------------|----------------------------------------------------------|
| <span data-ttu-id="cf08a-169">Hareket Bağlantıları</span><span class="sxs-lookup"><span data-stu-id="cf08a-169">Transaction Connections</span></span>    | <span data-ttu-id="cf08a-170">Proje hareketi ilişkileri için tümleştirme varlığı</span><span class="sxs-lookup"><span data-stu-id="cf08a-170">Integration entity for project transaction relationships</span></span> |
| <span data-ttu-id="cf08a-171">Tahmin Satırları</span><span class="sxs-lookup"><span data-stu-id="cf08a-171">Estimate Lines</span></span>             | <span data-ttu-id="cf08a-172">Proje gider tahminleri için tümleştirme varlığı</span><span class="sxs-lookup"><span data-stu-id="cf08a-172">Integration entity for project expense estimates</span></span>         |

### <a name="entity-flow"></a><span data-ttu-id="cf08a-173">Varlık akışı</span><span class="sxs-lookup"><span data-stu-id="cf08a-173">Entity flow</span></span>

<span data-ttu-id="cf08a-174">Proje gider tahminleri Project Service Automation'da yönetilir ve Finance and Operations'a proje gider tahminleri olarak eşitlenir.</span><span class="sxs-lookup"><span data-stu-id="cf08a-174">Project expense estimates are managed in Project Service Automation, and they are synchronized to Finance and Operations as project expense forecasts.</span></span>

### <a name="prerequisites"></a><span data-ttu-id="cf08a-175">Ön koşullar</span><span class="sxs-lookup"><span data-stu-id="cf08a-175">Prerequisites</span></span>

<span data-ttu-id="cf08a-176">Proje gider tahminleri eşitlenmeden önce projeleri, proje görevlerini ve proje gider hareketi kategorilerini eşitlemeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="cf08a-176">Before synchronization of project expense estimates can occur, you must synchronize projects, project tasks, and project expense transaction categories.</span></span>

### <a name="power-query"></a><span data-ttu-id="cf08a-177">Power Query</span><span class="sxs-lookup"><span data-stu-id="cf08a-177">Power Query</span></span>

<span data-ttu-id="cf08a-178">Proje gider tahminleri şablonunda aşağıdaki görevleri tamamlamak için Power Query kullanmanız gerekir:</span><span class="sxs-lookup"><span data-stu-id="cf08a-178">In the project expense estimates template, you must use Power Query to complete the following tasks:</span></span>

- <span data-ttu-id="cf08a-179">Yalnızca gider tahmini satır kayıtlarını içerecek şekilde filtreleyin.</span><span class="sxs-lookup"><span data-stu-id="cf08a-179">Filter to include only expense estimate line records.</span></span>
- <span data-ttu-id="cf08a-180">Tümleştirme yeni saat tahminleri oluştururken kullanılacak varsayılan tahmin modeli kodunu ayarlamak.</span><span class="sxs-lookup"><span data-stu-id="cf08a-180">Set the default forecast model ID that will be used when the integration creates new hour forecasts.</span></span>
- <span data-ttu-id="cf08a-181">Faturalama türlerini dönüştürmek.</span><span class="sxs-lookup"><span data-stu-id="cf08a-181">Transform the billing types.</span></span>
- <span data-ttu-id="cf08a-182">Hareket türlerini dönüştürmek.</span><span class="sxs-lookup"><span data-stu-id="cf08a-182">Transform the transaction types.</span></span>

#### <a name="filter-to-include-only-expense-estimate-lines"></a><span data-ttu-id="cf08a-183">Yalnızca gider tahmini satırlarını içerecek filtre uygulama</span><span class="sxs-lookup"><span data-stu-id="cf08a-183">Filter to include only expense estimate lines</span></span>

<span data-ttu-id="cf08a-184">Project gider tahminleri (PSA'dan Fin and Ops'a) şablonunda, tümleştirmede yalnızca gider satırlarını içeren bir varsayılan filtre vardır.</span><span class="sxs-lookup"><span data-stu-id="cf08a-184">The Project expense estimates (PSA to Fin and Ops) template has a default filter that includes only expense lines in the integration.</span></span> <span data-ttu-id="cf08a-185">Kendi şablonunuzu oluşturuyorsanız bu filtreyi eklemeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="cf08a-185">If you create your own template, you must add this filter.</span></span> <span data-ttu-id="cf08a-186">**Hareket ilişkileri** görevini seçin ve ardından eşlemeyi açmak için **Eşle** okuna tıklayın.</span><span class="sxs-lookup"><span data-stu-id="cf08a-186">Select the **Transaction relationships** task, and then click the **Map** arrow to open the mapping.</span></span> <span data-ttu-id="cf08a-187">**Gelişmiş Sorgu ve Filtreleme** bağlantısını seçin.</span><span class="sxs-lookup"><span data-stu-id="cf08a-187">Select the **Advanced Query and Filtering** link.</span></span> <span data-ttu-id="cf08a-188">**msdyn\_transactiontype1** sütununu yalnızca **msdyn\_estimateline** öğesini içerecek şekilde filtreleyin.</span><span class="sxs-lookup"><span data-stu-id="cf08a-188">Filter the **msdyn\_transactiontype1** column so that it includes only **msdyn\_estimateline**.</span></span>

#### <a name="set-the-default-forecast-model-id"></a><span data-ttu-id="cf08a-189">Varsayılan tahmin modeli kodunu ayarlama</span><span class="sxs-lookup"><span data-stu-id="cf08a-189">Set the default forecast model ID</span></span>

<span data-ttu-id="cf08a-190">Şablondaki varsayılan tahmin modeli kodunu güncelleştirmek için **Gider tahminleri** görevini seçin ve ardından eşlemeyi açmak için **Eşle** okuna tıklayın.</span><span class="sxs-lookup"><span data-stu-id="cf08a-190">To update the default forecast model ID in the template, select the **Expense estimates** task, and then click the **Map** arrow to open the mapping.</span></span> <span data-ttu-id="cf08a-191">**Gelişmiş Sorgu ve Filtreleme** bağlantısını seçin.</span><span class="sxs-lookup"><span data-stu-id="cf08a-191">Select the **Advanced Query and Filtering** link.</span></span>

- <span data-ttu-id="cf08a-192">Power Query'de varsayılan Proje gider tahminleri (PSA'dan Fin and Ops'a) şablonunu kullanıyorsanız **Uygulanan Adımlar** bölümünden ilk **Eklenen Koşul**'u seçin.</span><span class="sxs-lookup"><span data-stu-id="cf08a-192">If you're using the default Project expense estimates (PSA to Fin and Ops) template, in Power Query, select the first **Inserted Condition** from the **Applied Steps** section.</span></span> <span data-ttu-id="cf08a-193">**İşlev** girişinde **O\_forecast** öğesini tümleştirmeyle kullanılacak tahmin modeli kodunun adıyla değiştirin.</span><span class="sxs-lookup"><span data-stu-id="cf08a-193">In the **Function** entry, replace **O\_forecast** with the name of the forecast model ID that should be used with the integration.</span></span> <span data-ttu-id="cf08a-194">Varsayılan şablonda, tanıtım verilerinden alınan bir tahmin modeli kodu vardır.</span><span class="sxs-lookup"><span data-stu-id="cf08a-194">The default template has a forecast model ID from the demo data.</span></span>
- <span data-ttu-id="cf08a-195">Yeni bir şablon oluşturuyorsanız bu sütunu eklemeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="cf08a-195">If you're creating a new template, you must add this column.</span></span> <span data-ttu-id="cf08a-196">Power Query'de **Koşullu Sütun Ekle**'yi seçin ve sütuna bir ad verin, örneğin **ModelKodu**.</span><span class="sxs-lookup"><span data-stu-id="cf08a-196">In Power Query, select **Add Conditional Column**, and enter a name for the new column, such as **ModelID**.</span></span> <span data-ttu-id="cf08a-197">Sütun için şu koşulu girin: where, if Estimate line ID is not null, then \<tahmin modeli kodunu girin\>; else null.</span><span class="sxs-lookup"><span data-stu-id="cf08a-197">Enter the condition for the column, where, if Estimate line ID is not null, then \<enter the forecast model ID\>; else null.</span></span>

#### <a name="transform-the-billing-types"></a><span data-ttu-id="cf08a-198">Faturalama türlerini dönüştürme</span><span class="sxs-lookup"><span data-stu-id="cf08a-198">Transform the billing types</span></span>

<span data-ttu-id="cf08a-199">Proje gider tahminleri (PSA'dan Fin and Ops'a) şablonunda, tümleştirme sırasında Project Service Automation'dan alınan faturalama türlerini dönüştürmek için kullanılan bir koşullu sütun vardır.</span><span class="sxs-lookup"><span data-stu-id="cf08a-199">The Project expense estimates (PSA to Fin and Ops) template includes a conditional column that is used to transform the billing types that are received from Project Service Automation during the integration.</span></span> <span data-ttu-id="cf08a-200">Kendi şablonunuzu oluşturuyorsanız bu koşullu sütunu eklemeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="cf08a-200">If you create your own template, you must add this conditional column.</span></span> <span data-ttu-id="cf08a-201">**Gelişmiş Sorgu ve Filtreleme** bağlantısını seçin ve ardından **Koşullu Sütun Ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="cf08a-201">Select the **Advanced Query and Filtering** link and then select **Add Conditional Column**.</span></span> <span data-ttu-id="cf08a-202">Yeni sütun için **Faturalama Türü** gibi bir ad girin.</span><span class="sxs-lookup"><span data-stu-id="cf08a-202">Enter a name for the new column, such as **BillingType**.</span></span> <span data-ttu-id="cf08a-203">Ardından aşağıdaki koşulu girin:</span><span class="sxs-lookup"><span data-stu-id="cf08a-203">Then enter the following condition:</span></span>

<span data-ttu-id="cf08a-204">If **msdyn\_billingtype** = 192350000, then **Masraflandırılamaz**</span><span class="sxs-lookup"><span data-stu-id="cf08a-204">If **msdyn\_billingtype** = 192350000, then **NonChargeable**</span></span>  
<span data-ttu-id="cf08a-205">else if **msdyn\_billingtype** = 192350001, then **Masraflandırılabilir**</span><span class="sxs-lookup"><span data-stu-id="cf08a-205">else if **msdyn\_billingtype** = 192350001, then **Chargeable**</span></span>  
<span data-ttu-id="cf08a-206">else if **msdyn\_billingtype** = 192350002, then **Karşılıksız**</span><span class="sxs-lookup"><span data-stu-id="cf08a-206">else if **msdyn\_billingtype** = 192350002, then **Complimentary**</span></span>  
<span data-ttu-id="cf08a-207">else **Yok**</span><span class="sxs-lookup"><span data-stu-id="cf08a-207">else **NotAvailable**</span></span>

#### <a name="transform-the-transaction-types"></a><span data-ttu-id="cf08a-208">Hareket türlerini dönüştürme</span><span class="sxs-lookup"><span data-stu-id="cf08a-208">Transform the transaction types</span></span>

<span data-ttu-id="cf08a-209">Proje gider tahminleri (PSA'dan Fin and Ops'a) şablonunda, tümleştirme sırasında Project Service Automation'dan alınan hareket türlerini dönüştürmek için kullanılan bir koşullu sütun vardır.</span><span class="sxs-lookup"><span data-stu-id="cf08a-209">The Project expense estimates (PSA to Fin and Ops) template includes a conditional column that is used to transform the transaction types that are received from Project Service Automation during the integration.</span></span> <span data-ttu-id="cf08a-210">Kendi şablonunuzu oluşturuyorsanız bu koşullu sütunu eklemeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="cf08a-210">If you create your own template, you must add this conditional column.</span></span> <span data-ttu-id="cf08a-211">**Gelişmiş Sorgu ve Filtreleme** bağlantısını seçin ve ardından **Koşullu Sütun Ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="cf08a-211">Select the **Advanced Query and Filtering** link and then select **Add Conditional Column**.</span></span> <span data-ttu-id="cf08a-212">Yeni sütun için **Hareket Türü** gibi bir ad girin.</span><span class="sxs-lookup"><span data-stu-id="cf08a-212">Enter a name for the new column, such as **TransactionType**.</span></span> <span data-ttu-id="cf08a-213">Ardından aşağıdaki koşulu girin:</span><span class="sxs-lookup"><span data-stu-id="cf08a-213">Then enter the following condition:</span></span>

<span data-ttu-id="cf08a-214">If **msdyn\_transactiontypecode** = 192350000, then **Maliyet**</span><span class="sxs-lookup"><span data-stu-id="cf08a-214">If **msdyn\_transactiontypecode** = 192350000, then **Cost**</span></span>  
<span data-ttu-id="cf08a-215">else if **msdyn\_transactiontypecode** = 192350005, then **Satış**</span><span class="sxs-lookup"><span data-stu-id="cf08a-215">else if **msdyn\_transactiontypecode** = 192350005, then **Sales**</span></span>  
<span data-ttu-id="cf08a-216">else **null**</span><span class="sxs-lookup"><span data-stu-id="cf08a-216">else **null**</span></span>

### <a name="template-mapping-in-data-integration"></a><span data-ttu-id="cf08a-217">Veri tümleştirmede şablon eşleme</span><span class="sxs-lookup"><span data-stu-id="cf08a-217">Template mapping in Data integration</span></span>

<span data-ttu-id="cf08a-218">Aşağıdaki şekillerde, Veri tümleştirmesinde şablon görevi eşleşmelerine örnekler gösteriliyor.</span><span class="sxs-lookup"><span data-stu-id="cf08a-218">The following illustrations show examples of the template task mappings in Data integration.</span></span> <span data-ttu-id="cf08a-219">Eşleme, Project Service Automation'dan Finance and Operations'a eşitlenecek alan bilgilerini gösterir.</span><span class="sxs-lookup"><span data-stu-id="cf08a-219">The mapping shows the field information that will be synchronized from Project Service Automation to Finance and Operations.</span></span>

<span data-ttu-id="cf08a-220">[![Şablon eşleme](./media/ExpenseEstimateTransactionRelationshipsMapping.jpg)](./media/ExpenseEstimateTransactionRelationshipsMapping.jpg)</span><span class="sxs-lookup"><span data-stu-id="cf08a-220">[![Template mapping](./media/ExpenseEstimateTransactionRelationshipsMapping.jpg)](./media/ExpenseEstimateTransactionRelationshipsMapping.jpg)</span></span>

<span data-ttu-id="cf08a-221">[![Şablon eşleme](./media/ExpenseEstimatesMapping.jpg)](./media/ExpenseEstimatesMapping.jpg)</span><span class="sxs-lookup"><span data-stu-id="cf08a-221">[![Template mapping](./media/ExpenseEstimatesMapping.jpg)](./media/ExpenseEstimatesMapping.jpg)</span></span>
