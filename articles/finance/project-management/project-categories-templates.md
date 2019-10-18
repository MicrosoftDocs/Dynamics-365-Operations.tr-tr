---
title: Finance and Operations ile Project Service Automation arasında proje gider kategorilerini eşitleme
description: Bu konuda proje gider kategorilerini Microsoft Dynamics 365 Finance ile Dynamics 365 Project Service Automation arasında eşitlemek için kullanılan şablon ve temel görevler açıklanmaktadır.
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
ms.dyn365.ops.version: AX 8.0.0
ms.openlocfilehash: 482febc91a04766216f9887ab59d30cc9aed5096
ms.sourcegitcommit: 2460d0da812c45fce67a061386db52e0ae46b0f3
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/30/2019
ms.locfileid: "2250519"
---
# <a name="synchronize-project-expense-categories-between-finance-and-operations-and-project-service-automation"></a><span data-ttu-id="7f3fe-103">Finance and Operations ile Project Service Automation arasında proje gider kategorilerini eşitleme</span><span class="sxs-lookup"><span data-stu-id="7f3fe-103">Synchronize project expense categories between Finance and Operations and Project Service Automation</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="7f3fe-104">Bu konu projeleri Dynamics 365 Finance üzerinden Dynamics 365 Project Service Automation üzerine proje maliyet kategorilerini doğrudan eşitlemekte kullanılan şablonu ve alttaki görevleri açıklar.</span><span class="sxs-lookup"><span data-stu-id="7f3fe-104">This topic describes the templates and underlying tasks that are used to synchronize project expense categories between Dynamics 365 Finance and Dynamics 365 Project Service Automation.</span></span>

> [!NOTE]
> - <span data-ttu-id="7f3fe-105">Proje görev tümleştirmesi, gider hareket kategorileri, saat tahminleri, gider tahminleri ve işlev kilitleme sürüm 8.0 içinde kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="7f3fe-105">Project task integration, expense transaction categories, hour estimates, expense estimates, and functionality locking are available in version 8.0.</span></span>
> - <span data-ttu-id="7f3fe-106">Fiili değerlerin tümleştirmesi sürüm 8.0.1 veya sonrasında kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="7f3fe-106">Actuals integration is available in version 8.0.1 or later.</span></span>
> - <span data-ttu-id="7f3fe-107">Enterprise Edition 7.3.0 kullanıyorsanız KB 4132657 ve KB 4132660'ı yükledikten sonra proje görevlerini, gider hareketi kategorilerini, saat tahminlerini, gider tahminlerini ve gerçek değerleri tümleştirmek ve işlev kilitlemeyi yapılandırmak için şablonları kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="7f3fe-107">If you're using Enterprise edition 7.3.0, after you install KB 4132657 and KB 4132660, you will be able to use the templates to integrate project tasks, expense transaction categories, hour estimates, expense estimates, and actuals, and to configure functionality locking.</span></span> <span data-ttu-id="7f3fe-108">Muhasebe dağıtımlarını sıfırlamanız gerekiyorsa KB 4131710'u da yüklemenizi öneririz.</span><span class="sxs-lookup"><span data-stu-id="7f3fe-108">If you must reset the accounting distributions, we recommend that you also install KB 4131710.</span></span>

## <a name="data-flow-for-project-service-automation-and-finance"></a><span data-ttu-id="7f3fe-109">Project Service Automation ve Finance için veri akışı</span><span class="sxs-lookup"><span data-stu-id="7f3fe-109">Data flow for Project Service Automation and Finance</span></span>

<span data-ttu-id="7f3fe-110">Project Service Automation ve Finance tümleştirmesi çözümünde, verileri Project Service Automation ve Finance kurulumları arasında eşitlemek için Veri tümleştirme özelliği kullanılır.</span><span class="sxs-lookup"><span data-stu-id="7f3fe-110">The Project Service Automation and Finance integration solution uses the Data integration feature to synchronize data across instances of Project Service Automation and Finance.</span></span> <span data-ttu-id="7f3fe-111">Veri tümleştirme özelliğiyle kullanılabilen tümleştirme şablonları, proje gider hareketi kategorileri hakkındaki verilerin Finance ile Project Service Automation arasında akışına olanak tanır.</span><span class="sxs-lookup"><span data-stu-id="7f3fe-111">The integration templates that are available with the Data integration feature enable the flow of data about project expense transaction categories between Finance and Project Service Automation.</span></span>

<span data-ttu-id="7f3fe-112">Proje gider kategorilerinin ana kaydı Finance'te üretiliyorsa tümleştirme akışı, öncelikle Finance'ten Project Service Automation'a doğru olur.</span><span class="sxs-lookup"><span data-stu-id="7f3fe-112">If the project expense categories are mastered in Finance, the integration flow is first from Finance to Project Service Automation.</span></span> <span data-ttu-id="7f3fe-113">Proje gider kategorilerinin tümleştirme kimlikleri, Project Service Automation'dan Finance'e eşitleme yoluyla güncelleştirilir.</span><span class="sxs-lookup"><span data-stu-id="7f3fe-113">The integration IDs of the project expense categories are then updated through synchronization from Project Service Automation to Finance.</span></span>

<span data-ttu-id="7f3fe-114">Proje gider kategorilerinin ana kaydı Project Service Automation'da üretiliyorsa tümleştirme akışı, öncelikle Project Service Automation'dan Finance'e doğru olur.</span><span class="sxs-lookup"><span data-stu-id="7f3fe-114">If the project expense categories are mastered in Project Service Automation, the integration flow is first from Project Service Automation to Finance.</span></span> <span data-ttu-id="7f3fe-115">Proje kategorileri, Project Service Automation'dan eşitleme yapılmadan önce Finance'te yapılandırılmış olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="7f3fe-115">The project categories must already be configured in Finance before the synchronization from Project Service Automation.</span></span> <span data-ttu-id="7f3fe-116">Daha sonra Finance'ten Project Service Automation'a ve ardından yine Project Service Automation'dan Finance'e geri eşitleme yapın.</span><span class="sxs-lookup"><span data-stu-id="7f3fe-116">Then synchronize from Finance back to Project Service Automation, and then from Project Service Automation to Finance again.</span></span> <span data-ttu-id="7f3fe-117">Bu şekilde kategorilerin bağlantılı olduğundan ve yinelemelerin oluşmadığından emin olursunuz.</span><span class="sxs-lookup"><span data-stu-id="7f3fe-117">In this way, you help guarantee that the categories are linked, and that no duplicates are created.</span></span>

> [!NOTE]
> <span data-ttu-id="7f3fe-118">Proje gider kategorilerinin ana kaydı, genellikle Finance'te üretilir.</span><span class="sxs-lookup"><span data-stu-id="7f3fe-118">Typically, the project expense categories are mastered in Finance.</span></span> <span data-ttu-id="7f3fe-119">Ancak Finance'te üretilmezlerse veya gider kategorileri Project Service Automation'da zaten oluşturulmuşsa öncelikle Proje gider hareketi kategorileri (PSA'dan Fin and Ops'a) şablonunu kullanarak eşitlemeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="7f3fe-119">However, if they aren't, or if expense categories have already been created in Project Service Automation, you must first synchronize by using the Project expense transaction categories (PSA to Fin and Ops) template.</span></span> <span data-ttu-id="7f3fe-120">Ardından Proje gider hareketi kategorileri (Fin and Ops'tan PSA'ya) şablonunu kullanarak eşitleyin.</span><span class="sxs-lookup"><span data-stu-id="7f3fe-120">Then synchronize by using the Project expense transaction categories (Fin and Ops to PSA) template.</span></span> <span data-ttu-id="7f3fe-121">Daha sonra, Project Service Automation'dan Finance'e eşitlemeyi bir kez daha çalıştırmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="7f3fe-121">You should then run the synchronization from Project Service Automation to Finance one more time.</span></span>
>
> <span data-ttu-id="7f3fe-122">Öncelikle Project Service Automation'dan eşitleme yaparsanız eşitleme çalıştırılmadan önce Finance'te aşağıdaki gereklilikler karşılanmalıdır:</span><span class="sxs-lookup"><span data-stu-id="7f3fe-122">If you synchronize first from Project Service Automation, the following requirements must be met in Finance before the synchronization is run:</span></span>
>
> - <span data-ttu-id="7f3fe-123">Project Service Automation'da ayarlanan proje kategorisiyle eşleşen paylaşılan kategori mevcut olmalı ve **Proje** ile **Gider** için etkinleştirilmiş olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="7f3fe-123">The shared category that matches the project category that is set up in Project Service Automation must exist, and it must be enabled for both **Project** and **Expense**.</span></span>
> - <span data-ttu-id="7f3fe-124">Tümleştirilmesi gereken her Finance tüzel kişiliği için aşağıdaki proje kategorileri mevcut olmalıdır:</span><span class="sxs-lookup"><span data-stu-id="7f3fe-124">For each Finance legal entity that must be integrated with, the following project categories must exist:</span></span>
>
>     - <span data-ttu-id="7f3fe-125">**Proje kategorisi** var.</span><span class="sxs-lookup"><span data-stu-id="7f3fe-125">**Project category** exists.</span></span> 
>     - <span data-ttu-id="7f3fe-126">**Giderde Kullan** etkinleştirildi.</span><span class="sxs-lookup"><span data-stu-id="7f3fe-126">**Use in Expense** is enabled.</span></span>
>     - <span data-ttu-id="7f3fe-127">**Günlüklerde etkin** etkinleştirildi.</span><span class="sxs-lookup"><span data-stu-id="7f3fe-127">**Active in journal** is enabled.</span></span>
>     - <span data-ttu-id="7f3fe-128">**Hareket türü** **Gider** olarak ayarlandı.</span><span class="sxs-lookup"><span data-stu-id="7f3fe-128">**Transaction type** is set to **Expense**.</span></span>

<span data-ttu-id="7f3fe-129">Aşağıdaki çizimde, verilerin Project Service Automation ile Finance arasında nasıl eşitlendiği gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="7f3fe-129">The following illustration shows how the data is synchronized between Project Service Automation and Finance.</span></span>

<span data-ttu-id="7f3fe-130">[![Project Service Automation ile Finance tümleştirmesi için veri akışı](./media/ProjectExpenseCategoriesFlow.png)](./media/ProjectExpenseCategoriesFlow.png)</span><span class="sxs-lookup"><span data-stu-id="7f3fe-130">[![Data flow for Project Service Automation integration with Finance](./media/ProjectExpenseCategoriesFlow.png)](./media/ProjectExpenseCategoriesFlow.png)</span></span>

## <a name="project-expense-category-synchronization-from-finance-to-project-service-automation"></a><span data-ttu-id="7f3fe-131">Finance'ten Project Service Automation'a proje gider kategorisi eşitlemesi</span><span class="sxs-lookup"><span data-stu-id="7f3fe-131">Project expense category synchronization from Finance to Project Service Automation</span></span>

### <a name="template-and-task"></a><span data-ttu-id="7f3fe-132">Şablon ve görev</span><span class="sxs-lookup"><span data-stu-id="7f3fe-132">Template and task</span></span>

<span data-ttu-id="7f3fe-133">Şablona erişmek için, Microsoft PowerApps yönetim merkezi'nde **Projeler**'i seçin ve ardından, sağ üst köşede **Yeni proje**'yi seçerek genele açık şablonları seçin.</span><span class="sxs-lookup"><span data-stu-id="7f3fe-133">To access the template, in the Microsoft PowerApps admin center, select **Projects**, and then, in the upper-right corner, select **New project** to select public templates.</span></span>

<span data-ttu-id="7f3fe-134">Aşağıdaki şablon ve temel görev, proje gider kategorilerini Finance'ten Project Service Automation'a eşitlemek için kullanılır:</span><span class="sxs-lookup"><span data-stu-id="7f3fe-134">The following template and underlying task are used to synchronize project expense categories from Finance to Project Service Automation:</span></span>

- <span data-ttu-id="7f3fe-135">**Veri tümleştirmedeki şablonun adı:** Proje gider hareketi kategorileri (Fin and Ops'tan PSA'ya)</span><span class="sxs-lookup"><span data-stu-id="7f3fe-135">**Name of the template in Data integration:** Project expense transaction categories (Fin and Ops to PSA)</span></span>
- <span data-ttu-id="7f3fe-136">**Projedeki görevin adı:** Kategorileri PSA'ya eşitleme</span><span class="sxs-lookup"><span data-stu-id="7f3fe-136">**Name of the task in the project:** Sync categories to PSA</span></span>

### <a name="entity-set"></a><span data-ttu-id="7f3fe-137">Varlık kümesi</span><span class="sxs-lookup"><span data-stu-id="7f3fe-137">Entity set</span></span>

| <span data-ttu-id="7f3fe-138">Finans</span><span class="sxs-lookup"><span data-stu-id="7f3fe-138">Finance</span></span>                           | <span data-ttu-id="7f3fe-139">Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="7f3fe-139">Project Service Automation</span></span> |
|-----------------------------------|----------------------------|
| <span data-ttu-id="7f3fe-140">Kategoriler için tümleştirme varlığı</span><span class="sxs-lookup"><span data-stu-id="7f3fe-140">Integration entity for categories</span></span> | <span data-ttu-id="7f3fe-141">Hareket kategorileri</span><span class="sxs-lookup"><span data-stu-id="7f3fe-141">Transaction categories</span></span>     |

### <a name="entity-flow"></a><span data-ttu-id="7f3fe-142">Varlık akışı</span><span class="sxs-lookup"><span data-stu-id="7f3fe-142">Entity flow</span></span>

<span data-ttu-id="7f3fe-143">Proje gider kategorileri, Finance'te yönetilir ve Project Service Automation'a hareket kategorileri olarak eşitlenir.</span><span class="sxs-lookup"><span data-stu-id="7f3fe-143">Project expense categories are managed in Finance, and they are synchronized to Project Service Automation as transaction categories.</span></span>

### <a name="power-query"></a><span data-ttu-id="7f3fe-144">Power Query</span><span class="sxs-lookup"><span data-stu-id="7f3fe-144">Power Query</span></span>

<span data-ttu-id="7f3fe-145">Project Service Automation'a eşitleme yaparken Excel'de hareket kategorisinde faturalama türünü ayarlamak için Microsoft Power Query kullanmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="7f3fe-145">When you're synchronizing to Project Service Automation, you must use Microsoft Power Query for Excel to set the billing type on the transaction category.</span></span> <span data-ttu-id="7f3fe-146">Proje gider hareketi kategorileri (Fin and Ops'tan PSA'ya) şablonu bir varsayılan sütun ve eşleme sunar.</span><span class="sxs-lookup"><span data-stu-id="7f3fe-146">The Project expense transaction categories (Fin and Ops to PSA) template provides a default column and mapping.</span></span> <span data-ttu-id="7f3fe-147">Kendi şablonunuzu oluşturuyorsanız, Power Query'de koşullu bir sütun eklemeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="7f3fe-147">If you create your own template, you must add a conditional column in Power Query.</span></span> <span data-ttu-id="7f3fe-148">Aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="7f3fe-148">Follow these steps.</span></span>

1. <span data-ttu-id="7f3fe-149">Proje gider hareketi kategorileri (Fin and Ops'tan PSA'ya) şablonundaki proje gideri kategorileri görevini açmak için oka tıklayın.</span><span class="sxs-lookup"><span data-stu-id="7f3fe-149">Click the arrow to open the mapping of the project expense categories task in the Project expense transaction categories (Fin and Ops to PSA) template.</span></span>
2. <span data-ttu-id="7f3fe-150">Power Query'yi açmak için **Gelişmiş Sorgu ve Filtreleme** bağlantısına tıklayın.</span><span class="sxs-lookup"><span data-stu-id="7f3fe-150">Click the **Advance Query and Filtering** link to open Power Query.</span></span>
2. <span data-ttu-id="7f3fe-151">**Koşullu Sütun Ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="7f3fe-151">Select **Add Conditional Column**.</span></span>
3. <span data-ttu-id="7f3fe-152">Yeni sütun için **Faturalama Türü** gibi bir ad girin.</span><span class="sxs-lookup"><span data-stu-id="7f3fe-152">Enter a name for the new column, such as **BillingType**.</span></span>
4. <span data-ttu-id="7f3fe-153">Şu koşulu girin: **if CATEGORYID not equal to null then 19235001, Otherwise null**.</span><span class="sxs-lookup"><span data-stu-id="7f3fe-153">Enter the following condition: **if CATEGORYID not equal to null then 19235001, Otherwise null**.</span></span>
5. <span data-ttu-id="7f3fe-154">Sütunda **Tamam**'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="7f3fe-154">Click **OK** on the column.</span></span>
6. <span data-ttu-id="7f3fe-155">Bu yeni sütunu eşleme sayfasında eşlediğinizden emin olun.</span><span class="sxs-lookup"><span data-stu-id="7f3fe-155">Be sure to map this new column on the mapping page.</span></span>

<span data-ttu-id="7f3fe-156">Aşağıdaki şekilde, Veri tümleştirmesinde şablon görev eşlemesi örneği gösteriliyor.</span><span class="sxs-lookup"><span data-stu-id="7f3fe-156">The following illustration shows an example of the template task mapping in Data integration.</span></span> <span data-ttu-id="7f3fe-157">Eşlemede Finance'ten Project Service Automation'a eşitlenecek alan bilgileri gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="7f3fe-157">The mapping shows the field information that will be synchronized from Finance to Project Service Automation.</span></span>

<span data-ttu-id="7f3fe-158">[![Şablon eşleme](./media/ProjectExpenseCategoriesToPSAMapping.jpg)](./media/ProjectExpenseCategoriesToPSAMapping.jpg)</span><span class="sxs-lookup"><span data-stu-id="7f3fe-158">[![Template mapping](./media/ProjectExpenseCategoriesToPSAMapping.jpg)](./media/ProjectExpenseCategoriesToPSAMapping.jpg)</span></span>

## <a name="project-expense-category-synchronization-from-project-service-automation-to-finance"></a><span data-ttu-id="7f3fe-159">Project Service Automation'dan Finance'e proje gider kategorisi eşitlemesi</span><span class="sxs-lookup"><span data-stu-id="7f3fe-159">Project expense category synchronization from Project Service Automation to Finance</span></span>

### <a name="template-and-task"></a><span data-ttu-id="7f3fe-160">Şablon ve görev</span><span class="sxs-lookup"><span data-stu-id="7f3fe-160">Template and task</span></span>

<span data-ttu-id="7f3fe-161">Aşağıdaki şablon ve temel görev, proje gider kategorilerini Project Service Automation'dan Finance'e eşitlemek için kullanılır:</span><span class="sxs-lookup"><span data-stu-id="7f3fe-161">The following template and underlying task are used to synchronize project expense categories from Project Service Automation to Finance:</span></span>

- <span data-ttu-id="7f3fe-162">**Veri tümleştirmedeki şablonun adı:** Proje gider hareketi kategorileri (PSA'dan Fin and Ops'a)</span><span class="sxs-lookup"><span data-stu-id="7f3fe-162">**Name of the template in Data integration:** Project expense transaction categories (PSA to Fin and Ops)</span></span>
- <span data-ttu-id="7f3fe-163">**Projedeki görevin adı:** Kategorileri Fin Ops'a eşitleme</span><span class="sxs-lookup"><span data-stu-id="7f3fe-163">**Name of the task in the project:** Sync categories to Fin Ops</span></span>

### <a name="entity-set"></a><span data-ttu-id="7f3fe-164">Varlık kümesi</span><span class="sxs-lookup"><span data-stu-id="7f3fe-164">Entity set</span></span>

| <span data-ttu-id="7f3fe-165">Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="7f3fe-165">Project Service Automation</span></span> | <span data-ttu-id="7f3fe-166">Finans</span><span class="sxs-lookup"><span data-stu-id="7f3fe-166">Finance</span></span>                           |
|----------------------------|-----------------------------------|
| <span data-ttu-id="7f3fe-167">Hareket kategorileri</span><span class="sxs-lookup"><span data-stu-id="7f3fe-167">Transaction categories</span></span>     | <span data-ttu-id="7f3fe-168">Kategoriler için tümleştirme varlığı</span><span class="sxs-lookup"><span data-stu-id="7f3fe-168">Integration entity for categories</span></span> |

### <a name="entity-flow"></a><span data-ttu-id="7f3fe-169">Varlık akışı</span><span class="sxs-lookup"><span data-stu-id="7f3fe-169">Entity flow</span></span>

<span data-ttu-id="7f3fe-170">Proje gider kategorileri, Finance'te yönetilir ve Project Service Automation'a hareket kategorileri olarak eşitlenir.</span><span class="sxs-lookup"><span data-stu-id="7f3fe-170">Project expense categories are managed in Finance, and they are synchronized to Project Service Automation as transaction categories.</span></span> <span data-ttu-id="7f3fe-171">Finance'e geri eşitleme, Finance'teki proje kategorisini Project Service Automation'daki tümleştirme kimliği ile güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="7f3fe-171">The synchronization back to Finance updates the project category in Finance with the integration ID from Project Service Automation.</span></span>

### <a name="template-mapping-in-data-integration"></a><span data-ttu-id="7f3fe-172">Veri tümleştirmede şablon eşleme</span><span class="sxs-lookup"><span data-stu-id="7f3fe-172">Template mapping in Data integration</span></span>

<span data-ttu-id="7f3fe-173">Aşağıdaki şekilde, Veri tümleştirmesinde şablon görev eşlemesi örneği gösteriliyor.</span><span class="sxs-lookup"><span data-stu-id="7f3fe-173">The following illustration shows an example of the template task mapping in Data integration.</span></span>

> [!NOTE]
> <span data-ttu-id="7f3fe-174">Eşlemede Project Service Automation'dan Finance'e eşitlenecek alan bilgileri gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="7f3fe-174">The mapping shows the field information that will be synchronized from Project Service Automation to Finance.</span></span>

<span data-ttu-id="7f3fe-175">[![Şablon eşleme](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)</span><span class="sxs-lookup"><span data-stu-id="7f3fe-175">[![Template mapping](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)</span></span>
