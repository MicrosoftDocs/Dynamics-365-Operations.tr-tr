---
title: Finance and Operations ile Project Service Automation arasında proje gider kategorilerini eşitleme
description: Bu konu projeleri Microsoft Dynamics 365 for Finance and Operations üzerinden Microsoft Dynamics 365 for Project Service Automation üzerine proje maliyet kategorilerini doğrudan eşitlemekte kullanılan şablonu ve alttaki görevleri açıklar.
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
ms.dyn365.ops.version: AX 8.0.0
ms.openlocfilehash: c4d09fde2cf4335553243c136590f9f3135db97a
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2019
ms.locfileid: "347848"
---
# <a name="synchronize-project-expense-categories-between-finance-and-operations-and-project-service-automation"></a><span data-ttu-id="28532-103">Finance and Operations ile Project Service Automation arasında proje gider kategorilerini eşitleme</span><span class="sxs-lookup"><span data-stu-id="28532-103">Synchronize project expense categories between Finance and Operations and Project Service Automation</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="28532-104">Bu konu projeleri Microsoft Dynamics 365 for Finance and Operations üzerinden Microsoft Dynamics 365 for Project Service Automation üzerine proje maliyet kategorilerini doğrudan eşitlemekte kullanılan şablonu ve alttaki görevleri açıklar.</span><span class="sxs-lookup"><span data-stu-id="28532-104">This topic describes the templates and underlying tasks that are used to synchronize project expense categories between Microsoft Dynamics 365 for Finance and Operations and Microsoft Dynamics 365 for Project Service Automation.</span></span>

> [!NOTE]
> - <span data-ttu-id="28532-105">Proje görev tümleştirmesi, gider hareket kategorileri, saat tahminleri, gider tahminleri ve işlev kilitleme Microsoft Dynamics 365 for Finance and Operations sürüm 8.0 içinde kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="28532-105">Project task integration, expense transaction categories, hour estimates, expense estimates, and functionality locking are available in Microsoft Dynamics 365 for Finance and Operations version 8.0.</span></span>
> - <span data-ttu-id="28532-106">Fiili değerlerin tümleştirmesi Microsoft Dynamics 365 for Finance and Operations sürüm 8.0.1 veya sonrasında kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="28532-106">Actuals integration is available in Microsoft Dynamics 365 for Finance and Operations version 8.0.1 or later.</span></span>
> - <span data-ttu-id="28532-107">Microsoft Dynamics 365 for Finance and Operations, Enterprise edition 7.3.0 kullanıyorsanız, KB 4132657 ve KB 4132660 yükledikten sonra, proje görevlerini, gider hareketi kategorilerini, saat tahminlerini, gider tahminlerini ve gerçek değerleri tümleştirmek ve işlev kilitlemeyi yapılandırmak için şablonları kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="28532-107">If you're using Microsoft Dynamics 365 for Finance and Operations, Enterprise edition 7.3.0, after you install KB 4132657 and KB 4132660, you will be able to use the templates to integrate project tasks, expense transaction categories, hour estimates, expense estimates, and actuals, and to configure functionality locking.</span></span> <span data-ttu-id="28532-108">Muhasebe dağıtımlarını sıfırlamanız gerekiyorsa KB 4131710'u da yüklemenizi öneririz.</span><span class="sxs-lookup"><span data-stu-id="28532-108">If you must reset the accounting distributions, we recommend that you also install KB 4131710.</span></span>

## <a name="data-flow-for-project-service-automation-and-finance-and-operations"></a><span data-ttu-id="28532-109">Project Service Automation ve Finance and Operations için veri akışı</span><span class="sxs-lookup"><span data-stu-id="28532-109">Data flow for Project Service Automation and Finance and Operations</span></span>

<span data-ttu-id="28532-110">Project Service Automation ve Finance and Operations tümleştirme çözümünde, Project Service Automation ve Finance and Operations örnekleri arasında veri eşitlemek için Veri tümleştirme özelliği kullanılır.</span><span class="sxs-lookup"><span data-stu-id="28532-110">The Project Service Automation and Finance and Operations integration solution uses the Data integration feature to synchronize data across instances of Project Service Automation and Finance and Operations.</span></span> <span data-ttu-id="28532-111">Veri tümleştirme özelliğiyle kullanılabilen tümleştirme şablonları, proje gider hareketi kategorileri hakkındaki verilerin Project Service Automation ile Finance and Operations arasında akışına olanak tanır.</span><span class="sxs-lookup"><span data-stu-id="28532-111">The integration templates that are available with the Data integration feature enable the flow of data about project expense transaction categories between Finance and Operations and Project Service Automation.</span></span>

<span data-ttu-id="28532-112">Proje gider kategorilerinin ana kaydı Finance and Operations'ta üretiliyorsa tümleştirme akışı ilk olarak Finance and Operations'tan Project Service Automation'a doğru olur.</span><span class="sxs-lookup"><span data-stu-id="28532-112">If the project expense categories are mastered in Finance and Operations, the integration flow is first from Finance and Operations to Project Service Automation.</span></span> <span data-ttu-id="28532-113">Proje gider kategorilerinin tümleştirme kimlikleri Project Service Automation'dan Finance and Operations'a eşitleme aracılığıyla güncelleştirilir.</span><span class="sxs-lookup"><span data-stu-id="28532-113">The integration IDs of the project expense categories are then updated through synchronization from Project Service Automation to Finance and Operations.</span></span>

<span data-ttu-id="28532-114">Proje gider kategorilerinin ana kaydı Project Service Automation'da üretiliyorsa, tümleştirme akışı ilk olarak Project Service Automation'dan Finance and Operations'a doğru olur.</span><span class="sxs-lookup"><span data-stu-id="28532-114">If the project expense categories are mastered in Project Service Automation, the integration flow is first from Project Service Automation to Finance and Operations.</span></span> <span data-ttu-id="28532-115">Proje kategorileri, Project Service Automation'dan eşitleme yapılmadan önce Finance and Operations'ta yapılandırılmış olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="28532-115">The project categories must already be configured in Finance and Operations before the synchronization from Project Service Automation.</span></span> <span data-ttu-id="28532-116">Sonrasında, geriye, yani Finance and Operations'tan Project Service Automation'a ve ardından yine Project Service Automation'dan Finance and Operations'a eşitleme yapın.</span><span class="sxs-lookup"><span data-stu-id="28532-116">Then synchronize from Finance and Operations back to Project Service Automation, and then from Project Service Automation to Finance and Operations again.</span></span> <span data-ttu-id="28532-117">Bu şekilde kategorilerin bağlantılı olduğundan ve yinelemelerin oluşmadığından emin olursunuz.</span><span class="sxs-lookup"><span data-stu-id="28532-117">In this way, you help guarantee that the categories are linked, and that no duplicates are created.</span></span>

> [!NOTE]
> <span data-ttu-id="28532-118">Proje gider kategorilerinin ana kaydı genellikle Finance and Operations'ta üretilir.</span><span class="sxs-lookup"><span data-stu-id="28532-118">Typically, the project expense categories are mastered in Finance and Operations.</span></span> <span data-ttu-id="28532-119">Ancak Finance and Operations'ta üretilmezlerse veya gider kategorileri Project Service Automation'da zaten oluşturulmuşsa öncelikle Proje gider hareketi kategorileri (PSA'dan Fin and Ops'a) şablonunu kullanarak eşitlemeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="28532-119">However, if they aren't mastered in Finance and Operations, or if expense categories have already been created in Project Service Automation, you must first synchronize by using the Project expense transaction categories (PSA to Fin and Ops) template.</span></span> <span data-ttu-id="28532-120">Ardından Proje gider hareketi kategorileri (Fin and Ops'tan PSA'ya) şablonunu kullanarak eşitleyin.</span><span class="sxs-lookup"><span data-stu-id="28532-120">Then synchronize by using the Project expense transaction categories (Fin and Ops to PSA) template.</span></span> <span data-ttu-id="28532-121">Daha sonra Project Service Automation'dan Finance and Operations'a eşitlemeyi bir kez daha çalıştırmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="28532-121">You should then run the synchronization from Project Service Automation to Finance and Operations one more time.</span></span>
>
> <span data-ttu-id="28532-122">Öncelikle Project Service Automation'dan eşitlerseniz, eşitleme çalıştırılmadan önce Finance and Operations'ta aşağıdaki gereksinimler karşılanmalıdır:</span><span class="sxs-lookup"><span data-stu-id="28532-122">If you synchronize first from Project Service Automation, the following requirements must be met in Finance and Operations before the synchronization is run:</span></span>
>
> - <span data-ttu-id="28532-123">Project Service Automation'da ayarlanan proje kategorisiyle eşleşen paylaşılan kategori mevcut olmalı ve **Proje** ile **Gider** için etkinleştirilmiş olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="28532-123">The shared category that matches the project category that is set up in Project Service Automation must exist, and it must be enabled for both **Project** and **Expense**.</span></span>
> - <span data-ttu-id="28532-124">Tümleştirilmesi gereken her Finance and Operations tüzel kişiliği için aşağıdaki proje kategorileri mevcut olmalıdır:</span><span class="sxs-lookup"><span data-stu-id="28532-124">For each Finance and Operations legal entity that must be integrated with, the following project categories must exist:</span></span>
>
>     - <span data-ttu-id="28532-125">**Proje kategorisi** var.</span><span class="sxs-lookup"><span data-stu-id="28532-125">**Project category** exists.</span></span> 
>     - <span data-ttu-id="28532-126">**Giderde Kullan** etkinleştirildi.</span><span class="sxs-lookup"><span data-stu-id="28532-126">**Use in Expense** is enabled.</span></span>
>     - <span data-ttu-id="28532-127">**Günlüklerde etkin** etkinleştirildi.</span><span class="sxs-lookup"><span data-stu-id="28532-127">**Active in journal** is enabled.</span></span>
>     - <span data-ttu-id="28532-128">**Hareket türü** **Gider** olarak ayarlandı.</span><span class="sxs-lookup"><span data-stu-id="28532-128">**Transaction type** is set to **Expense**.</span></span>

<span data-ttu-id="28532-129">Aşağıdaki şekilde Project Service Automation ile Finance and Operations arasında verilerin nasıl eşitlendiği gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="28532-129">The following illustration shows how the data is synchronized between Project Service Automation and Finance and Operations.</span></span>

<span data-ttu-id="28532-130">[![Finance and Operations ile Project Service Automation tümleştirmesi için veri akışı](./media/ProjectExpenseCategoriesFlow.png)](./media/ProjectExpenseCategoriesFlow.png)</span><span class="sxs-lookup"><span data-stu-id="28532-130">[![Data flow for Project Service Automation integration with Finance and Operations](./media/ProjectExpenseCategoriesFlow.png)](./media/ProjectExpenseCategoriesFlow.png)</span></span>

## <a name="project-expense-category-synchronization-from-finance-and-operations-to-project-service-automation"></a><span data-ttu-id="28532-131">Finance and Operations'tan Project Service Automation'a proje gider kategorisi eşitlemesi</span><span class="sxs-lookup"><span data-stu-id="28532-131">Project expense category synchronization from Finance and Operations to Project Service Automation</span></span>

### <a name="template-and-task"></a><span data-ttu-id="28532-132">Şablon ve görev</span><span class="sxs-lookup"><span data-stu-id="28532-132">Template and task</span></span>

<span data-ttu-id="28532-133">Şablona erişmek için, Microsoft PowerApps yönetim merkezi'nde **Projeler**'i seçin ve ardından, sağ üst köşede **Yeni proje**'yi seçerek genele açık şablonları seçin.</span><span class="sxs-lookup"><span data-stu-id="28532-133">To access the template, in the Microsoft PowerApps admin center, select **Projects**, and then, in the upper-right corner, select **New project** to select public templates.</span></span>

<span data-ttu-id="28532-134">Aşağıdaki şablon ve temel görev, proje gider kategorilerini Finance and Operations'tan Project Service Automation'a eşitlemek için kullanılır:</span><span class="sxs-lookup"><span data-stu-id="28532-134">The following template and underlying task are used to synchronize project expense categories from Finance and Operations to Project Service Automation:</span></span>

- <span data-ttu-id="28532-135">**Veri tümleştirmedeki şablonun adı:** Proje gider hareketi kategorileri (Fin and Ops'tan PSA'ya)</span><span class="sxs-lookup"><span data-stu-id="28532-135">**Name of the template in Data integration:** Project expense transaction categories (Fin and Ops to PSA)</span></span>
- <span data-ttu-id="28532-136">**Projedeki görevin adı:** Kategorileri PSA'ya eşitleme</span><span class="sxs-lookup"><span data-stu-id="28532-136">**Name of the task in the project:** Sync categories to PSA</span></span>

### <a name="entity-set"></a><span data-ttu-id="28532-137">Varlık kümesi</span><span class="sxs-lookup"><span data-stu-id="28532-137">Entity set</span></span>

| <span data-ttu-id="28532-138">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="28532-138">Finance and Operations</span></span>            | <span data-ttu-id="28532-139">Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="28532-139">Project Service Automation</span></span> |
|-----------------------------------|----------------------------|
| <span data-ttu-id="28532-140">Kategoriler için tümleştirme varlığı</span><span class="sxs-lookup"><span data-stu-id="28532-140">Integration entity for categories</span></span> | <span data-ttu-id="28532-141">Hareket kategorileri</span><span class="sxs-lookup"><span data-stu-id="28532-141">Transaction categories</span></span>     |

### <a name="entity-flow"></a><span data-ttu-id="28532-142">Varlık akışı</span><span class="sxs-lookup"><span data-stu-id="28532-142">Entity flow</span></span>

<span data-ttu-id="28532-143">Proje gider kategorileri Finance and Operations'ta yönetilir ve Project Service Automation'a hareket kategorileri olarak eşitlenir.</span><span class="sxs-lookup"><span data-stu-id="28532-143">Project expense categories are managed in Finance and Operations, and they are synchronized to Project Service Automation as transaction categories.</span></span>

### <a name="power-query"></a><span data-ttu-id="28532-144">Power Query</span><span class="sxs-lookup"><span data-stu-id="28532-144">Power Query</span></span>

<span data-ttu-id="28532-145">Project Service Automation'a eşitleme yaparken Excel'de hareket kategorisinde faturalama türünü ayarlamak için Microsoft Power Query kullanmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="28532-145">When you're synchronizing to Project Service Automation, you must use Microsoft Power Query for Excel to set the billing type on the transaction category.</span></span> <span data-ttu-id="28532-146">Proje gider hareketi kategorileri (Fin and Ops'tan PSA'ya) şablonu bir varsayılan sütun ve eşleme sunar.</span><span class="sxs-lookup"><span data-stu-id="28532-146">The Project expense transaction categories (Fin and Ops to PSA) template provides a default column and mapping.</span></span> <span data-ttu-id="28532-147">Kendi şablonunuzu oluşturuyorsanız, Power Query'de koşullu bir sütun eklemeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="28532-147">If you create your own template, you must add a conditional column in Power Query.</span></span> <span data-ttu-id="28532-148">Aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="28532-148">Follow these steps.</span></span>

1. <span data-ttu-id="28532-149">Proje gider hareketi kategorileri (Fin and Ops'tan PSA'ya) şablonundaki proje gideri kategorileri görevini açmak için oka tıklayın.</span><span class="sxs-lookup"><span data-stu-id="28532-149">Click the arrow to open the mapping of the project expense categories task in the Project expense transaction categories (Fin and Ops to PSA) template.</span></span>
2. <span data-ttu-id="28532-150">Power Query'yi açmak için **Gelişmiş Sorgu ve Filtreleme** bağlantısına tıklayın.</span><span class="sxs-lookup"><span data-stu-id="28532-150">Click the **Advance Query and Filtering** link to open Power Query.</span></span>
2. <span data-ttu-id="28532-151">**Koşullu Sütun Ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="28532-151">Select **Add Conditional Column**.</span></span>
3. <span data-ttu-id="28532-152">Yeni sütun için **Faturalama Türü** gibi bir ad girin.</span><span class="sxs-lookup"><span data-stu-id="28532-152">Enter a name for the new column, such as **BillingType**.</span></span>
4. <span data-ttu-id="28532-153">Şu koşulu girin: **if CATEGORYID not equal to null then 19235001, Otherwise null**.</span><span class="sxs-lookup"><span data-stu-id="28532-153">Enter the following condition: **if CATEGORYID not equal to null then 19235001, Otherwise null**.</span></span>
5. <span data-ttu-id="28532-154">Sütunda **Tamam**'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="28532-154">Click **OK** on the column.</span></span>
6. <span data-ttu-id="28532-155">Bu yeni sütunu eşleme sayfasında eşlediğinizden emin olun.</span><span class="sxs-lookup"><span data-stu-id="28532-155">Be sure to map this new column on the mapping page.</span></span>

<span data-ttu-id="28532-156">Aşağıdaki şekilde, Veri tümleştirmesinde şablon görev eşlemesi örneği gösteriliyor.</span><span class="sxs-lookup"><span data-stu-id="28532-156">The following illustration shows an example of the template task mapping in Data integration.</span></span> <span data-ttu-id="28532-157">Eşleme, Finance and Operations'tan Project Service Automation'a eşitlenecek alan bilgilerini gösterir.</span><span class="sxs-lookup"><span data-stu-id="28532-157">The mapping shows the field information that will be synchronized from Finance and Operations to Project Service Automation.</span></span>

<span data-ttu-id="28532-158">[![Şablon eşleme](./media/ProjectExpenseCategoriesToPSAMapping.jpg)](./media/ProjectExpenseCategoriesToPSAMapping.jpg)</span><span class="sxs-lookup"><span data-stu-id="28532-158">[![Template mapping](./media/ProjectExpenseCategoriesToPSAMapping.jpg)](./media/ProjectExpenseCategoriesToPSAMapping.jpg)</span></span>

## <a name="project-expense-category-synchronization-from-project-service-automation-to-finance-and-operations"></a><span data-ttu-id="28532-159">Project Service Automation'dan Finance and Operations'a proje gider kategorisi eşitlemesi</span><span class="sxs-lookup"><span data-stu-id="28532-159">Project expense category synchronization from Project Service Automation to Finance and Operations</span></span>

### <a name="template-and-task"></a><span data-ttu-id="28532-160">Şablon ve görev</span><span class="sxs-lookup"><span data-stu-id="28532-160">Template and task</span></span>

<span data-ttu-id="28532-161">Aşağıdaki şablon ve temel görev, proje gider kategorilerini Project Service Automation'dan Finance and Operations'a eşitlemek için kullanılır:</span><span class="sxs-lookup"><span data-stu-id="28532-161">The following template and underlying task are used to synchronize project expense categories from Project Service Automation to Finance and Operations:</span></span>

- <span data-ttu-id="28532-162">**Veri tümleştirmedeki şablonun adı:** Proje gider hareketi kategorileri (PSA'dan Fin and Ops'a)</span><span class="sxs-lookup"><span data-stu-id="28532-162">**Name of the template in Data integration:** Project expense transaction categories (PSA to Fin and Ops)</span></span>
- <span data-ttu-id="28532-163">**Projedeki görevin adı:** Kategorileri Fin Ops'a eşitleme</span><span class="sxs-lookup"><span data-stu-id="28532-163">**Name of the task in the project:** Sync categories to Fin Ops</span></span>

### <a name="entity-set"></a><span data-ttu-id="28532-164">Varlık kümesi</span><span class="sxs-lookup"><span data-stu-id="28532-164">Entity set</span></span>

| <span data-ttu-id="28532-165">Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="28532-165">Project Service Automation</span></span> | <span data-ttu-id="28532-166">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="28532-166">Finance and Operations</span></span>            |
|----------------------------|-----------------------------------|
| <span data-ttu-id="28532-167">Hareket kategorileri</span><span class="sxs-lookup"><span data-stu-id="28532-167">Transaction categories</span></span>     | <span data-ttu-id="28532-168">Kategoriler için tümleştirme varlığı</span><span class="sxs-lookup"><span data-stu-id="28532-168">Integration entity for categories</span></span> |

### <a name="entity-flow"></a><span data-ttu-id="28532-169">Varlık akışı</span><span class="sxs-lookup"><span data-stu-id="28532-169">Entity flow</span></span>

<span data-ttu-id="28532-170">Proje gider kategorileri Finance and Operations'ta yönetilir ve Project Service Automation'a hareket kategorileri olarak eşitlenir.</span><span class="sxs-lookup"><span data-stu-id="28532-170">Project expense categories are managed in Finance and Operations, and they are synchronized to Project Service Automation as transaction categories.</span></span> <span data-ttu-id="28532-171">Geriye, yani Finance and Operations'a eşitleme, Finance and Operations'taki proje kategorisini Project Service Automation'dan tümleştirme kodu ile güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="28532-171">The synchronization back to Finance and Operations updates the project category in Finance and Operations with the integration ID from Project Service Automation.</span></span>

### <a name="template-mapping-in-data-integration"></a><span data-ttu-id="28532-172">Veri tümleştirmede şablon eşleme</span><span class="sxs-lookup"><span data-stu-id="28532-172">Template mapping in Data integration</span></span>

<span data-ttu-id="28532-173">Aşağıdaki şekilde, Veri tümleştirmesinde şablon görev eşlemesi örneği gösteriliyor.</span><span class="sxs-lookup"><span data-stu-id="28532-173">The following illustration shows an example of the template task mapping in Data integration.</span></span>

> [!NOTE]
> <span data-ttu-id="28532-174">Eşleme, Project Service Automation'dan Finance and Operations'a eşitlenecek alan bilgilerini gösterir.</span><span class="sxs-lookup"><span data-stu-id="28532-174">The mapping shows the field information that will be synchronized from Project Service Automation to Finance and Operations.</span></span>

<span data-ttu-id="28532-175">[![Şablon eşleme](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)</span><span class="sxs-lookup"><span data-stu-id="28532-175">[![Template mapping](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)</span></span>
