---
title: Proje görevlerini doğrudan Project Service Automation'dan Finance and Operations'a eşitleme
description: Bu konu proje fiili değerlerini, doğrudan Microsoft Dynamics 365 for Project Service Automation üzerinden Microsoft Dynamics 365 for Finance and Operations üzerine eşitlemekte kullanılan şablonu ve alttaki görevi açıklar.
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
ms.openlocfilehash: f7ea5036682ad5b61fe56acd20a591cccc01f2cb
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/01/2019
ms.locfileid: "1838331"
---
# <a name="synchronize-project-tasks-directly-from-project-service-automation-to-finance-and-operations"></a><span data-ttu-id="36731-103">Proje görevlerini doğrudan Project Service Automation'dan Finance and Operations'a eşitleme</span><span class="sxs-lookup"><span data-stu-id="36731-103">Synchronize project tasks directly from Project Service Automation to Finance and Operations</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="36731-104">Bu konu proje fiili değerlerini, doğrudan Microsoft Dynamics 365 for Project Service Automation üzerinden Microsoft Dynamics 365 for Finance and Operations üzerine eşitlemekte kullanılan şablonu ve alttaki görevi açıklar.</span><span class="sxs-lookup"><span data-stu-id="36731-104">This topic describes the template and underlying task that are used to synchronize project tasks directly from Microsoft Dynamics 365 for Project Service Automation to Microsoft Dynamics 365 for Finance and Operations.</span></span>

> [!NOTE]
> - <span data-ttu-id="36731-105">Proje görev tümleştirmesi, gider hareket kategorileri, saat tahminleri, gider tahminleri ve işlev kilitleme Microsoft Dynamics 365 for Finance and Operations sürüm 8.0 içinde kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="36731-105">Project task integration, expense transaction categories, hour estimates, expense estimates, and functionality locking are available in Microsoft Dynamics 365 for Finance and Operations version 8.0.</span></span>
> - <span data-ttu-id="36731-106">Microsoft Dynamics 365 for Finance and Operations, Enterprise edition 7.3.0 kullanıyorsanız, KB 4132657 ve KB 4132660 yükledikten sonra, proje görevlerini, gider hareketi kategorilerini, saat tahminlerini, gider tahminlerini ve gerçek değerleri tümleştirmek ve işlev kilitlemeyi yapılandırmak için şablonları kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="36731-106">If you're using Microsoft Dynamics 365 for Finance and Operations, Enterprise edition 7.3.0, after you install KB 4132657 and KB 4132660, you will be able to use the templates to integrate project tasks, expense transaction categories, hour estimates, expense estimates, and actuals, and to configure functionality locking.</span></span> <span data-ttu-id="36731-107">Muhasebe dağıtımlarını sıfırlamanız gerekiyorsa KB 4131710'u da yüklemenizi öneririz.</span><span class="sxs-lookup"><span data-stu-id="36731-107">If you must reset the accounting distributions, we recommended that you also install KB 4131710.</span></span>
> - <span data-ttu-id="36731-108">Fiili değerlerin tümleştirmesi Microsoft Dynamics 365 for Finance and Operations sürüm 8.0.1 veya sonrasında kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="36731-108">Actuals integration is available in Microsoft Dynamics 365 for Finance and Operations version 8.0.1 or later.</span></span>

## <a name="data-flow-for-project-service-automation-to-finance-and-operations"></a><span data-ttu-id="36731-109">Project Service Automation'dan Finance and Operations'a veri akışı</span><span class="sxs-lookup"><span data-stu-id="36731-109">Data flow for Project Service Automation to Finance and Operations</span></span>

<span data-ttu-id="36731-110">Project Service Automation'dan Finance and Operations'a tümleştirme çözümünde, Project Service Automation ve Finance and Operations örnekleri arasında veri eşitlemek için Veri tümleştirme özelliği kullanılır.</span><span class="sxs-lookup"><span data-stu-id="36731-110">The Project Service Automation to Finance and Operations integration solution uses the Data integration feature to synchronize data across instances of Project Service Automation and Finance and Operations.</span></span> <span data-ttu-id="36731-111">Veri tümleştirme özelliğiyle kullanılabilen tümleştirme şablonu, proje görevleri hakkındaki verilerin Project Service Automation'dan Finance and Operations'a akışına olanak sağlar.</span><span class="sxs-lookup"><span data-stu-id="36731-111">The integration template that is available with the Data integration feature enables the flow of data about project tasks from Project Service Automation to Finance and Operations.</span></span>

<span data-ttu-id="36731-112">Aşağıdaki şekilde Project Service Automation ile Finance and Operations arasında verilerin nasıl eşitlendiği gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="36731-112">The following illustration shows how the data is synchronized between Project Service Automation and Finance and Operations.</span></span>

<span data-ttu-id="36731-113">[![Finance and Operations ile Project Service Automation tümleştirmesi için veri akışı](./media/ProjectTasksFlow.png)](./media/ProjectTasksFlow.png)</span><span class="sxs-lookup"><span data-stu-id="36731-113">[![Data flow for Project Service Automation integration with Finance and Operations](./media/ProjectTasksFlow.png)](./media/ProjectTasksFlow.png)</span></span>

## <a name="template-and-task"></a><span data-ttu-id="36731-114">Şablon ve görev</span><span class="sxs-lookup"><span data-stu-id="36731-114">Template and task</span></span>

<span data-ttu-id="36731-115">Şablona erişmek için, Microsoft PowerApps yönetim merkezi'nde **Projeler**'i seçin ve ardından, sağ üst köşede **Yeni proje**'yi seçerek genele açık şablonları seçin.</span><span class="sxs-lookup"><span data-stu-id="36731-115">To access the template, in the Microsoft PowerApps admin center, select **Projects**, and then, in the upper-right corner, select **New project** to select public templates.</span></span>

<span data-ttu-id="36731-116">Aşağıdaki şablon ve temel görev, proje görevlerini Project Service Automation'dan Finance and Operations'a eşitlemek için kullanılır:</span><span class="sxs-lookup"><span data-stu-id="36731-116">The following template and underlying task are used to synchronize project tasks from Project Service Automation to Finance and Operations:</span></span>

- <span data-ttu-id="36731-117">**Veri tümleştirmedeki şablonun adı:** Proje görevleri (PSA'dan Fin and Ops'a)</span><span class="sxs-lookup"><span data-stu-id="36731-117">**Name of the template in Data integration:** Project tasks (PSA to Fin and Ops)</span></span>
- <span data-ttu-id="36731-118">**Projedeki görevin adı:** Proje görevleri</span><span class="sxs-lookup"><span data-stu-id="36731-118">**Name of the task in the project:** Project tasks</span></span>

<span data-ttu-id="36731-119">Proje görevlerinin eşitlemesinin yapılabilmesi için proje sözleşmelerini ve projeleri eşitlemeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="36731-119">Before synchronization of project tasks can occur, you must synchronize project contracts and projects.</span></span>

## <a name="entity-set"></a><span data-ttu-id="36731-120">Varlık kümesi</span><span class="sxs-lookup"><span data-stu-id="36731-120">Entity set</span></span>

| <span data-ttu-id="36731-121">Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="36731-121">Project Service Automation</span></span> | <span data-ttu-id="36731-122">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="36731-122">Finance and Operations</span></span>              |
|----------------------------|-------------------------------------|
| <span data-ttu-id="36731-123">Proje Görevleri</span><span class="sxs-lookup"><span data-stu-id="36731-123">Project Tasks</span></span>              | <span data-ttu-id="36731-124">Proje görevi için tümleştirme varlığı</span><span class="sxs-lookup"><span data-stu-id="36731-124">Integration entity for project task</span></span> |

## <a name="entity-flow"></a><span data-ttu-id="36731-125">Varlık akışı</span><span class="sxs-lookup"><span data-stu-id="36731-125">Entity flow</span></span>

<span data-ttu-id="36731-126">Proje görevleri Project Service Automation'da yönetilir ve Finance and Operations'a proje faaliyetleri olarak eşitlenir.</span><span class="sxs-lookup"><span data-stu-id="36731-126">Project tasks are managed in Project Service Automation, and they are synchronized to Finance and Operations as project activities.</span></span>

## <a name="prerequisites-and-mapping-setup"></a><span data-ttu-id="36731-127">Önkoşullar ve eşleme kurulumu</span><span class="sxs-lookup"><span data-stu-id="36731-127">Prerequisites and mapping setup</span></span>

<span data-ttu-id="36731-128">Proje görevlerinin eşitlemesinin yapılabilmesi için proje sözleşmelerini ve projeleri eşitlemeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="36731-128">Before synchronization of project tasks can occur, you must synchronize project contracts and projects.</span></span>

## <a name="power-query"></a><span data-ttu-id="36731-129">Power Query</span><span class="sxs-lookup"><span data-stu-id="36731-129">Power Query</span></span>

<span data-ttu-id="36731-130">Bu koşul karşılanırsa verilere filtre uygularken Excel için Microsoft Power Query kullanmanız gerekir:</span><span class="sxs-lookup"><span data-stu-id="36731-130">You must use Microsoft Power Query for Excel to filter data if this condition is met:</span></span>

- <span data-ttu-id="36731-131">Proje görevinde kaynağa özgü kayıtlarınız vardır.</span><span class="sxs-lookup"><span data-stu-id="36731-131">You have resource-specific records in a project task.</span></span>

<span data-ttu-id="36731-132">Power Query kullanmanız gerekiyorsa şu yönergeyi takip edin:</span><span class="sxs-lookup"><span data-stu-id="36731-132">If you must use Power Query, follow this guideline:</span></span>

- <span data-ttu-id="36731-133">Project görevleri (PSA'dan Fin and Ops) şablonunda, bir proje görevi içinden **IsLineTask** filtresini **Yanlış** olarak ayarlayarak kaynağa özgü kayıtları hariç tutan bir varsayılan filtre vardır.</span><span class="sxs-lookup"><span data-stu-id="36731-133">The Project tasks (PSA to Fin and Ops) template has a default filter that excludes resource-specific records from a project task by setting the filter on **IsLineTask** to **False**.</span></span> <span data-ttu-id="36731-134">Kendi şablonunuzu oluşturuyorsanız bu filtreyi eklemeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="36731-134">If you create your own template, you must add this filter.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="36731-135">Veri tümleştirmede şablon eşleme</span><span class="sxs-lookup"><span data-stu-id="36731-135">Template mapping in Data integration</span></span>

<span data-ttu-id="36731-136">Aşağıdaki şekilde, Veri tümleştirmesinde bir şablon görev eşlemeleri örneği gösteriliyor.</span><span class="sxs-lookup"><span data-stu-id="36731-136">The following illustration shows an example of the template task mappings in Data integration.</span></span> <span data-ttu-id="36731-137">Eşleme, Project Service Automation'dan Finance and Operations'a eşitlenecek alan bilgilerini gösterir.</span><span class="sxs-lookup"><span data-stu-id="36731-137">The mapping shows the field information that will be synchronized from Project Service Automation to Finance and Operations.</span></span>

<span data-ttu-id="36731-138">[![Şablon eşleme](./media/ProjectTasksMapping.png)](./media/ProjectTasksMapping.png)</span><span class="sxs-lookup"><span data-stu-id="36731-138">[![Template mapping](./media/ProjectTasksMapping.png)](./media/ProjectTasksMapping.png)</span></span>
