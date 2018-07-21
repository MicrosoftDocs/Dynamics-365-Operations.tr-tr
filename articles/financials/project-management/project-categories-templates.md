---
title: "Project Service Automation'dan proje gider kategorilerini eşitleme"
description: "Bu konu, Microsoft Dynamics 365 for Finance and Operations ile Dynamics 365 for Project Service Automation arasında proje gider kategorilerini eşitlemek için kullanılacak şablonları ve temel görevleri açıklamaktadır."
author: KimANelson
manager: AnnBe
ms.date: 04/02/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 8.0.0
ms.translationtype: HT
ms.sourcegitcommit: bd8feff598cf80ca675c7d2b5dda636799b19e29
ms.openlocfilehash: dcdb9b6ec296073d511c069cdceb1c61080b6d97
ms.contentlocale: tr-tr
ms.lasthandoff: 05/29/2018

---

# <a name="synchronize-project-expense-categories-between-finance-and-operations-and-project-service-automation"></a><span data-ttu-id="916b8-103">Finance and Operations ile Project Service Automation arasında proje gider kategorilerini eşitleme</span><span class="sxs-lookup"><span data-stu-id="916b8-103">Synchronize project expense categories between Finance and Operations and Project Service Automation</span></span>

<span data-ttu-id="916b8-104">Bu konu, Microsoft Dynamics 365 for Finance and Operations ile Dynamics 365 for Project Service Automation arasında proje gider kategorilerini eşitlemek için kullanılacak şablonları ve temel görevleri açıklamaktadır.</span><span class="sxs-lookup"><span data-stu-id="916b8-104">This topic describes the templates and underlying tasks that are used to synchronize project expense categories between Microsoft Dynamics 365 for Finance and Operations and Dynamics 365 for Project Service Automation.</span></span>

> [!NOTE]
> <span data-ttu-id="916b8-105">Proje görevleri tümleştirmesi, gider hareketi kategorileri, saat tahminleri, gider tahminleri ve işlev kilitleme, Dynamics 365 for Finance and Operations sürüm 8.0'da mevcuttur.</span><span class="sxs-lookup"><span data-stu-id="916b8-105">Project tasks integration, expense transaction categories, hour estimates, expense estimates, and functionality locking is available in Dynamics 365 for Finance and Operations version 8.0.</span></span>

## <a name="data-flow-for-project-service-automation-and-finance-and-operations"></a><span data-ttu-id="916b8-106">Project Service Automation ve Finance and Operations için veri akışı</span><span class="sxs-lookup"><span data-stu-id="916b8-106">Data flow for Project Service Automation and Finance and Operations</span></span>

<span data-ttu-id="916b8-107">Project Service Automation ve Finance and Operations tümleştirme çözümünde, Project Service Automation ve Finance and Operations örnekleri arasında veri eşitlemek için Veri tümleştirme özelliği kullanılır.</span><span class="sxs-lookup"><span data-stu-id="916b8-107">The Project Service Automation and Finance and Operations integration solution uses the Data integration feature to synchronize data across instances of Project Service Automation and Finance and Operations.</span></span> <span data-ttu-id="916b8-108">Veri tümleştirme özelliğiyle kullanılabilen tümleştirme şablonları, proje gider hareketi kategorileri hakkındaki verilerin Project Service Automation ile Finance and Operations arasında akışına olanak sağlar.</span><span class="sxs-lookup"><span data-stu-id="916b8-108">The integration templates that are available with the Data integration feature enables the flow of data about project expense transaction categories between Finance and Operations and Project Service Automation.</span></span>

<span data-ttu-id="916b8-109">Proje gider kategorilerinin ana kaydı Finance and Operations'ta üretiliyorsa, tümleştirme akışı ilk olarak Finance and Operations'tan Project Service Automation'a doğru olur ve sonra proje gider kategorilerinin tümleştirme kodları, Project Service Automation'dan Finance and Operations'a eşitlemeyle güncelleştirilir.</span><span class="sxs-lookup"><span data-stu-id="916b8-109">If the project expense categories are mastered in Finance and Operations, the integration flow is first from Finance and Operations to Project Service Automation, and then updating the project expense categories integration IDs by synchronizing from Project Service Automation to Finance and Operations.</span></span>

<span data-ttu-id="916b8-110">Proje gider kategorilerinin ana kaydı Project Service Automation'da üretiliyorsa, tümleştirme akışı ilk olarak Project Service Automation'dan Finance and Operations'a doğru olur.</span><span class="sxs-lookup"><span data-stu-id="916b8-110">If the project expense categories are mastered in Project Service Automation, the integration flow is first from Project Service Automation to Finance and Operations.</span></span> <span data-ttu-id="916b8-111">Project Service Automation'dan eşitleme yapılmadan önce proje kategorileri Finance and Operations'ta yapılandırılmış olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="916b8-111">The project categories must already be configured in Finance and Operations prior to the synchronization from Project Service Automation.</span></span> <span data-ttu-id="916b8-112">Bunun ardından, geriye, yani Finance and Operations'tan Project Service Automation'a ve ardından yine Project Service Automation'dan Finance and Operations'a eşitleme yapın.</span><span class="sxs-lookup"><span data-stu-id="916b8-112">Then synchronize from Finance and Operations back to Project Service Automation and then from Project Service Automation to Finance and Operations again.</span></span> <span data-ttu-id="916b8-113">Bu, kategorilerin birbiriyle bağlantılı olmasını sağlar ve yinelemeler oluşmaz.</span><span class="sxs-lookup"><span data-stu-id="916b8-113">This ensures the categories are linked and duplicates are not created.</span></span>

> [!NOTE]
> <span data-ttu-id="916b8-114">Proje gider kategorilerinin ana kaydı genellikle Finance and Operations'ta üretilecektir.</span><span class="sxs-lookup"><span data-stu-id="916b8-114">Typically, the project expense categories will be mastered in Finance and Operations.</span></span> <span data-ttu-id="916b8-115">Durum böyle değilse veya gider kategorilerini önceden Project Service Automation'da oluşturduysanız, ilk olarak Proje gider hareketi kategorilerini kullanarak eşitleme yapmanız (PSA'dan Fin and Ops'a) ve ardından yine Proje gider hareketi kategorilerini kullanarak (Fin and Ops'tan PSA'ya) bir kez daha eşitleme yapmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="916b8-115">If that is not your situation, or you already have expense categories created in Project Service Automation, you must first sync using the Project expense transaction categories (PSA to Fin and Ops) and then sync using Project expense transaction categories (Fin and Ops to PSA).</span></span> <span data-ttu-id="916b8-116">Bunun ardından PSA'dan Fin and Ops'a eşitlemeyi bir kez daha çalıştırmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="916b8-116">You should then run the sync from PSA to Fin and Ops one more time.</span></span>

> <span data-ttu-id="916b8-117">Eşitleme ilk olarak Project Service Automation'dan yapılıyorsa, proje kategorileri önceden Finance and Operations'ta ayarlanması ve Project Service Automation hareket kategorileriyle eşitlenmesi gereken tüm proje kategorilerinin **Günlüklerde etkin** olacak şekilde ayarlanması gerekir.</span><span class="sxs-lookup"><span data-stu-id="916b8-117">If synchronizing first from Project Service Automation, the project categories must already be set up in Finance and Operations and any project categories that need to be synched with the Project Service Automation transaction categories must be set up to be **Active in journals**.</span></span>

<span data-ttu-id="916b8-118">Aşağıdaki şekilde Project Service Automation ile Finance and Operations arasında verilerin nasıl eşitlendiği gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="916b8-118">The following illustration shows how the data is synchronized between Project Service Automation and Finance and Operations.</span></span>

<span data-ttu-id="916b8-119">[![Finance and Operations ile Project Service Automation tümleştirmesi için veri akışı](./media/ProjectExpenseCategoriesFlow.png)](./media/ProjectExpenseCategoriesFlow.png)</span><span class="sxs-lookup"><span data-stu-id="916b8-119">[![Data flow for Project Service Automation integration with Finance and Operations](./media/ProjectExpenseCategoriesFlow.png)](./media/ProjectExpenseCategoriesFlow.png)</span></span>


## <a name="templates-and-tasks"></a><span data-ttu-id="916b8-120">Şablonlar ve görevler</span><span class="sxs-lookup"><span data-stu-id="916b8-120">Templates and tasks</span></span>

<span data-ttu-id="916b8-121">Kullanılabilecek şablonlara erişmek için, Microsoft PowerApps Yönetim Merkezi'nde **Projeler**'i seçin ve ardından, sağ üst köşede **Yeni proje**'yi seçerek genele açık şablonları seçin.</span><span class="sxs-lookup"><span data-stu-id="916b8-121">To access available templates, in the Microsoft PowerApps Admin Center, select **Projects**, and then, in the upper-right corner, select **New project** to select public templates.</span></span>

<span data-ttu-id="916b8-122">Aşağıdaki şablon ve temel görev, proje gider kategorilerini Finance and Operations'tan Project Service Automation'a eşitlemek için kullanılır:</span><span class="sxs-lookup"><span data-stu-id="916b8-122">The following template and underlying task is used to synchronize project expense categories from Finance and Operations to Project Service Automation:</span></span>

-  <span data-ttu-id="916b8-123">**Veri tümleştirmedeki şablonun adı:** Proje gider hareketi kategorileri (Fin and Ops'tan PSA'ya)</span><span class="sxs-lookup"><span data-stu-id="916b8-123">**Name of the template in Data integration:** Project expense transaction categories (Fin and Ops to PSA)</span></span>
-  <span data-ttu-id="916b8-124">**Projedeki görevin adı:** Kategorileri PSA'ya eşitleme</span><span class="sxs-lookup"><span data-stu-id="916b8-124">**Name of the task in the project:** Sync categories to PSA</span></span>

## <a name="entity-set"></a><span data-ttu-id="916b8-125">Varlık kümesi</span><span class="sxs-lookup"><span data-stu-id="916b8-125">Entity set</span></span>

| <span data-ttu-id="916b8-126">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="916b8-126">Finance and Operations</span></span>               | <span data-ttu-id="916b8-127">Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="916b8-127">Project Service Automation</span></span>    |
|--------------------------------------|-------------------------------|
| <span data-ttu-id="916b8-128">Kategoriler için tümleştirme varlığı</span><span class="sxs-lookup"><span data-stu-id="916b8-128">Integration entity for categories</span></span>    | <span data-ttu-id="916b8-129">Hareket kategorileri</span><span class="sxs-lookup"><span data-stu-id="916b8-129">Transaction categories</span></span>        |

## <a name="entity-flow"></a><span data-ttu-id="916b8-130">Varlık akışı</span><span class="sxs-lookup"><span data-stu-id="916b8-130">Entity flow</span></span>

<span data-ttu-id="916b8-131">Proje gider kategorileri Finance and Operations'ta yönetilir ve Project Service Automation'a hareket kategorileri olarak eşitlenir.</span><span class="sxs-lookup"><span data-stu-id="916b8-131">Project expense categories are managed in Finance and Operations, and they are synchronized to Project Service Automation as transaction categories.</span></span>

## <a name="power-query"></a><span data-ttu-id="916b8-132">Power Query</span><span class="sxs-lookup"><span data-stu-id="916b8-132">Power Query</span></span>

<span data-ttu-id="916b8-133">Project Service Automation'a eşitleme yaparken hareket kategorisinde faturalama türünü ayarlamak için Microsoft Power Query kullanmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="916b8-133">You must use Microsoft Power Query to set the billing type on the transaction category when synchronizing to Project Service Automation.</span></span> <span data-ttu-id="916b8-134">Proje gider hareketi kategorileri (Fin and Ops'tan PSA'ya) şablonunda bir varsayılan sütun ve eşleme zaten sağlanmıştır.</span><span class="sxs-lookup"><span data-stu-id="916b8-134">The Project expense transaction categories (Fin and Ops to PSA) template has a default column and mapping already provided.</span></span> <span data-ttu-id="916b8-135">Kendi şablonunuzu oluşturuyorsanız, Power Query'de koşullu bir sütun eklemeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="916b8-135">If you create your own template, you must add a conditional column in Power Query.</span></span>
- <span data-ttu-id="916b8-136">Proje gider kategorilerini eşleme görevinin içinden Gelişmiş Sorgu ve Filtreleme formunu açın.</span><span class="sxs-lookup"><span data-stu-id="916b8-136">Open the Advance Query and Filtering form from within the mapping of project expense categories task.</span></span>
- <span data-ttu-id="916b8-137">**Koşullu Sütun Ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="916b8-137">Select **Add Conditional Column**.</span></span>
- <span data-ttu-id="916b8-138">Yeni sütuna bir ad verin (örneğin FaturalamaTürü).</span><span class="sxs-lookup"><span data-stu-id="916b8-138">Give the new column a name, such as BillingType.</span></span>
- <span data-ttu-id="916b8-139">Şu koşulu girin: if **CATEGORYID not equal to null then 19235001, Otherwise null**.</span><span class="sxs-lookup"><span data-stu-id="916b8-139">Enter the following condition: if **CATEGORYID not equal to null then 19235001, Otherwise null**.</span></span>
- <span data-ttu-id="916b8-140">Sütunda **Tamam**'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="916b8-140">Click **OK** on the column.</span></span>
- <span data-ttu-id="916b8-141">Bu yeni sütunu Eşleme sayfasında eşlediğinizden emin olun.</span><span class="sxs-lookup"><span data-stu-id="916b8-141">Be sure to map this new column in the mapping page.</span></span>

<span data-ttu-id="916b8-142">Aşağıdaki şekilde, Veri tümleştirmesinde şablon görev eşlemesi örneği gösteriliyor.</span><span class="sxs-lookup"><span data-stu-id="916b8-142">The following illustration shows an example of the template task mapping in Data integration.</span></span> <span data-ttu-id="916b8-143">Eşleme, Finance and Operations'tan Project Service Automation'a eşitlenecek alan bilgilerini gösterir.</span><span class="sxs-lookup"><span data-stu-id="916b8-143">The mapping shows the field information that will be synchronized from Finance and Operations to Project Service Automation.</span></span>

<span data-ttu-id="916b8-144">[![Şablon eşleme](./media/ProjectExpenseCategoriesToPSAMapping.jpg)](./media/ProjectExpenseCategoriesToPSAMapping.jpg)</span><span class="sxs-lookup"><span data-stu-id="916b8-144">[![Template mapping](./media/ProjectExpenseCategoriesToPSAMapping.jpg)](./media/ProjectExpenseCategoriesToPSAMapping.jpg)</span></span>

<span data-ttu-id="916b8-145">Aşağıdaki şablon ve temel görev, proje gider kategorilerini Project Service Automation'dan Finance and Operations'a eşitlemek için kullanılır:</span><span class="sxs-lookup"><span data-stu-id="916b8-145">The following template and underlying task is used to synchronize project expense categories from Project Service Automation to Finance and Operations:</span></span>

<span data-ttu-id="916b8-146">-**Veri tümleştirmedeki şablonun adı:** Proje gider hareketi kategorileri (PSA'dan Fin and Ops'a) -**Projedeki görevin adı:** Kategorileri Fin Ops'a eşitleme</span><span class="sxs-lookup"><span data-stu-id="916b8-146">-**Name of the template in Data integration:** Project expense transaction categories (PSA to Fin and Ops) -**Name of the task in the project:** Sync categories to Fin Ops</span></span>

## <a name="entity-set"></a><span data-ttu-id="916b8-147">Varlık kümesi</span><span class="sxs-lookup"><span data-stu-id="916b8-147">Entity set</span></span>

| <span data-ttu-id="916b8-148">Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="916b8-148">Project Service Automation</span></span>      | <span data-ttu-id="916b8-149">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="916b8-149">Finance and Operations</span></span>             |
|---------------------------------|------------------------------------|
| <span data-ttu-id="916b8-150">Hareket kategorileri</span><span class="sxs-lookup"><span data-stu-id="916b8-150">Transaction categories</span></span>          | <span data-ttu-id="916b8-151">Kategoriler için tümleştirme varlığı</span><span class="sxs-lookup"><span data-stu-id="916b8-151">Integration entity for categories</span></span>  | 

## <a name="entity-flow"></a><span data-ttu-id="916b8-152">Varlık akışı</span><span class="sxs-lookup"><span data-stu-id="916b8-152">Entity flow</span></span>

<span data-ttu-id="916b8-153">Proje gider kategorileri Finance and Operations'ta yönetilir ve Project Service Automation'a hareket kategorileri olarak eşitlenir.</span><span class="sxs-lookup"><span data-stu-id="916b8-153">Project expense categories are managed in Finance and Operations, and they are synchronized to Project Service Automation as transaction categories.</span></span> <span data-ttu-id="916b8-154">Geriye, yani Finance and Operations'a eşitleme, Project Service Automation'dan tümleştirme kodunu Finance and Operations proje kategorisinde güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="916b8-154">The synchronization back to Finance and Operations updates the integration ID from Project Service Automation on the Finance and Operations project category.</span></span>

<span data-ttu-id="916b8-155">Aşağıdaki şekilde, Veri tümleştirmesinde şablon görev eşlemesi örneği gösteriliyor.</span><span class="sxs-lookup"><span data-stu-id="916b8-155">The following illustration shows an example of the template task mapping in Data integration.</span></span>

> [!NOTE]
> <span data-ttu-id="916b8-156">Eşleme, Project Service Automation'dan Finance and Operations'a eşitlenecek alan bilgilerini gösterir.</span><span class="sxs-lookup"><span data-stu-id="916b8-156">The mapping shows the field information that will be synchronized from Project Service Automation to Finance and Operations.</span></span>

<span data-ttu-id="916b8-157">[![Şablon eşleme](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)</span><span class="sxs-lookup"><span data-stu-id="916b8-157">[![Template mapping](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)</span></span>

