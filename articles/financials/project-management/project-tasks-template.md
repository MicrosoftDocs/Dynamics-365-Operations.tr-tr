---
title: "Project Service Automation'dan proje görevlerini eşitleme"
description: "Bu konu, proje görevlerini Microsoft Dynamics 365 for Project Service Automation'dan Dynamics 365 for Finance and Operations'a doğrudan eşitlemek için kullanılacak şablonu ve temel görevi açıklamaktadır."
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
ms.dyn365.ops.version: AX 7.3.0
ms.translationtype: HT
ms.sourcegitcommit: 399b519ab0da4de405aeb06f3e7f4bf29a6c5cc3
ms.openlocfilehash: 89df0d99d780441ad08cd6bff3e1fd203694eb8e
ms.contentlocale: tr-tr
ms.lasthandoff: 05/30/2018

---

# <a name="synchronize-project-tasks-from-project-service-automation-directly-to-project-activities-in-finance-and-operations"></a><span data-ttu-id="f6c29-103">Project Service Automation'dan proje görevlerini Finance and Operations'taki proje faaliyetlerine doğrudan eşitleme</span><span class="sxs-lookup"><span data-stu-id="f6c29-103">Synchronize project tasks from Project Service Automation directly to project activities in Finance and Operations</span></span>

<span data-ttu-id="f6c29-104">Bu konu, proje görevlerini Microsoft Dynamics 365 for Project Service Automation'dan Dynamics 365 for Finance and Operations'a doğrudan eşitlemek için kullanılacak şablonu ve temel görevi açıklamaktadır.</span><span class="sxs-lookup"><span data-stu-id="f6c29-104">This topic describes the template and underlying task that is used to synchronize project tasks directly from Microsoft Dynamics 365 for Project Service Automation to Dynamics 365 for Finance and Operations.</span></span>

> [!NOTE]
> <span data-ttu-id="f6c29-105">Proje görevleri tümleştirmesi, gider hareketi kategorileri, saat tahminleri, gider tahminleri ve işlev kilitleme, Dynamics 365 for Finance and Operations sürüm 8.0'da mevcuttur.</span><span class="sxs-lookup"><span data-stu-id="f6c29-105">Project tasks integration, expense transaction categories, hour estimates, expense estimates, and functionality locking is available in Dynamics 365 for Finance and Operations version 8.0.</span></span>

## <a name="data-flow-for-project-service-automation-to-finance-and-operations"></a><span data-ttu-id="f6c29-106">Project Service Automation'dan Finance and Operations'a veri akışı</span><span class="sxs-lookup"><span data-stu-id="f6c29-106">Data flow for Project Service Automation to Finance and Operations</span></span>

<span data-ttu-id="f6c29-107">Project Service Automation'dan Finance and Operations'a tümleştirme çözümünde, Project Service Automation ve Finance and Operations örnekleri arasında veri eşitlemek için Veri tümleştirme özelliği kullanılır.</span><span class="sxs-lookup"><span data-stu-id="f6c29-107">The Project Service Automation to Finance and Operations integration solution uses the Data integration feature to synchronize data across instances of Project Service Automation and Finance and Operations.</span></span> <span data-ttu-id="f6c29-108">Veri tümleştirme özelliğiyle kullanılabilen tümleştirme şablonu, proje görevleri hakkındaki verilerin Project Service Automation'dan Finance and Operations'a akışına olanak sağlar.</span><span class="sxs-lookup"><span data-stu-id="f6c29-108">The integration template that is available with the Data integration feature enables the flow of data about project tasks from Project Service Automation to Finance and Operations.</span></span>

<span data-ttu-id="f6c29-109">Aşağıdaki şekilde Project Service Automation ile Finance and Operations arasında verilerin nasıl eşitlendiği gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="f6c29-109">The following illustration shows how the data is synchronized between Project Service Automation and Finance and Operations.</span></span>

<span data-ttu-id="f6c29-110">[![Finance and Operations ile Project Service Automation tümleştirmesi için veri akışı](./media/ProjectTasksFlow.png)](./media/ProjectTasksFlow.png)</span><span class="sxs-lookup"><span data-stu-id="f6c29-110">[![Data flow for Project Service Automation integration with Finance and Operations](./media/ProjectTasksFlow.png)](./media/ProjectTasksFlow.png)</span></span>

## <a name="template-and-task"></a><span data-ttu-id="f6c29-111">Şablon ve görev</span><span class="sxs-lookup"><span data-stu-id="f6c29-111">Template and task</span></span>

<span data-ttu-id="f6c29-112">Şablona erişmek için, Microsoft PowerApps Yönetim Merkezi'nde **Projeler**'i seçin ve ardından, sağ üst köşede **Yeni proje**'yi seçerek genele açık şablonları seçin.</span><span class="sxs-lookup"><span data-stu-id="f6c29-112">To access the template, in the Microsoft PowerApps Admin Center, select **Projects**, and then, in the upper-right corner, select **New project** to select public templates.</span></span>

<span data-ttu-id="f6c29-113">Aşağıdaki şablon ve temel görev, proje görevlerini Project Service Automation'dan Finance and Operations'a eşitlemek için kullanılır:</span><span class="sxs-lookup"><span data-stu-id="f6c29-113">The following template and underlying task is used to synchronize project tasks from Project Service Automation to Finance and Operations:</span></span>

<span data-ttu-id="f6c29-114">-**Veri tümleştirmedeki şablonun adı:** Proje görevleri (PSA'dan Fin and Ops'a) -**Projedeki görevin adı:** Proje görevleri</span><span class="sxs-lookup"><span data-stu-id="f6c29-114">-**Name of the template in Data integration:** Project tasks (PSA to Fin and Ops) -**Name of the task in the project:** Project tasks</span></span>

<span data-ttu-id="f6c29-115">Proje görevlerinin eşitlemesinin yapılabilmesi için proje sözleşmelerini ve projeleri eşitlemeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="f6c29-115">Before synchronization of project tasks can occur, you must synchronize project contracts and projects.</span></span>

## <a name="entity-set"></a><span data-ttu-id="f6c29-116">Varlık kümesi</span><span class="sxs-lookup"><span data-stu-id="f6c29-116">Entity set</span></span>

|<span data-ttu-id="f6c29-117">Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="f6c29-117">Project Service Automation</span></span>               | <span data-ttu-id="f6c29-118">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="f6c29-118">Finance and Operations</span></span>                |
|-----------------------------------------|---------------------------------------|
| <span data-ttu-id="f6c29-119">Proje Görevleri</span><span class="sxs-lookup"><span data-stu-id="f6c29-119">Project Tasks</span></span>                           | <span data-ttu-id="f6c29-120">Proje görevi için tümleştirme varlığı.</span><span class="sxs-lookup"><span data-stu-id="f6c29-120">Integration entity for project task.</span></span>   |

## <a name="entity-flow"></a><span data-ttu-id="f6c29-121">Varlık akışı</span><span class="sxs-lookup"><span data-stu-id="f6c29-121">Entity flow</span></span>

<span data-ttu-id="f6c29-122">Proje görevleri Project Service Automation'da yönetilir ve Finance and Operations'a proje faaliyetleri olarak eşitlenir.</span><span class="sxs-lookup"><span data-stu-id="f6c29-122">Project tasks are managed in Project Service Automation, and they are synchronized to Finance and Operations as project activities.</span></span>

## <a name="prerequisites-and-mapping-setup"></a><span data-ttu-id="f6c29-123">Önkoşullar ve eşleme kurulumu</span><span class="sxs-lookup"><span data-stu-id="f6c29-123">Prerequisites and mapping setup</span></span>

<span data-ttu-id="f6c29-124">Proje görevlerinin eşitlemesinin yapılabilmesi için proje sözleşmelerini ve projeleri eşitlemeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="f6c29-124">Before synchronization of project tasks can occur, you must synchronize project contracts and projects.</span></span>

## <a name="power-query"></a><span data-ttu-id="f6c29-125">Power Query</span><span class="sxs-lookup"><span data-stu-id="f6c29-125">Power Query</span></span>

<span data-ttu-id="f6c29-126">Şu koşullar karşılanırsa, verilere filtre uygulamak için Microsoft Power Query kullanmanız gerekir:</span><span class="sxs-lookup"><span data-stu-id="f6c29-126">You must use Microsoft Power Query to filter data if these conditions are met:</span></span>

- <span data-ttu-id="f6c29-127">Bir proje görevinde kaynağa özgü kayıtlarınız vardır.</span><span class="sxs-lookup"><span data-stu-id="f6c29-127">You have resource specific records within a project task.</span></span>

<span data-ttu-id="f6c29-128">Power Query kullanmanız gerekiyorsa şu yönergeleri takip edin:</span><span class="sxs-lookup"><span data-stu-id="f6c29-128">If you must use Power Query, follow these guidelines:</span></span>

- <span data-ttu-id="f6c29-129">Project görevleri (PSA'dan Fin and Ops) şablonunda, bir proje görevi içinden, **IsLineTask**'taki filtreyi **Yanlış**'a ayarlayarak kaynağa özgü kayıtları hariç tutmak için kullanılan bir varsayılan filtre vardır.</span><span class="sxs-lookup"><span data-stu-id="f6c29-129">The Project tasks (PSA to Fin and Ops) template has a default filter to exclude resource specific records from within a project task by setting the filter on the **IsLineTask** to **False**.</span></span> <span data-ttu-id="f6c29-130">Kendi şablonunuzu oluşturuyorsanız bu filtreyi eklemeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="f6c29-130">If you create your own template, you must add this filter.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="f6c29-131">Veri tümleştirmede şablon eşleme</span><span class="sxs-lookup"><span data-stu-id="f6c29-131">Template mapping in Data integration</span></span>

<span data-ttu-id="f6c29-132">Aşağıdaki şekilde, Veri tümleştirmesinde bir şablon görev eşlemeleri örneği gösteriliyor.</span><span class="sxs-lookup"><span data-stu-id="f6c29-132">The following illustration shows an example of the template task mappings in Data integration.</span></span> <span data-ttu-id="f6c29-133">Eşleme, Project Service Automation'dan Finance and Operations'a eşitlenecek alan bilgilerini gösterir.</span><span class="sxs-lookup"><span data-stu-id="f6c29-133">The mapping shows the field information that will be synchronized from Project Service Automation to Finance and Operations.</span></span>

<span data-ttu-id="f6c29-134">[![Şablon eşleme](./media/ProjectTasksMapping.png)](./media/ProjectTasksMapping.png)</span><span class="sxs-lookup"><span data-stu-id="f6c29-134">[![Template mapping](./media/ProjectTasksMapping.png)](./media/ProjectTasksMapping.png)</span></span>


