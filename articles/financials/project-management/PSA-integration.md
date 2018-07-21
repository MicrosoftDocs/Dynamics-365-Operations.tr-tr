---
title: Project Service Automation
description: "Bu çözüm, Microsoft Dynamics 365 for Finance and Operations ve Microsoft Dynamics 365 for Project Service Automation örnekleri arasında Common Data Service (CDS) üzerinden verileri eşitlemek için Veri Tümleştirme özelliğini kullanır."
author: KimANelson
manager: AnnBe
ms.date: 11/27/2017
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
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: bd8feff598cf80ca675c7d2b5dda636799b19e29
ms.openlocfilehash: 0ad9e6ba7fe8dd915681da8e671ff210de887b1e
ms.contentlocale: tr-tr
ms.lasthandoff: 05/29/2018

---

# <a name="project-service-automation"></a><span data-ttu-id="dfa6e-103">Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="dfa6e-103">Project Service Automation</span></span>

<span data-ttu-id="dfa6e-104">Project Service Automation'dan Finance and Operations'a tümleştirme çözümü, Microsoft Dynamics 365 for Finance and Operations ve Microsoft Dynamics 365 for Project Service Automation örnekleri arasında Common Data Service (CDS) üzerinden verileri eşitlemek için Veri Tümleştirme özelliğini kullanır.</span><span class="sxs-lookup"><span data-stu-id="dfa6e-104">The Project Service Automation to Finance and Operations integration solution uses the Data Integration feature to synchronize data across instances of Microsoft Dynamics 365 for Finance and Operations and Microsoft Dynamics 365 for Project Service Automation via the Common Data Service (CDS).</span></span> <span data-ttu-id="dfa6e-105">Veri tümleştirme özelliğiyle kullanılabilen tümleştirme şablonları, projeler, proje sözleşmeleri, proje sözleşme satırları, proje sözleşme satırı kilometre taşları, proje görevleri, gider hareketi kategorileri, saat tahminleri ve gider tahminlerinin Project Service Automation'dan Finance and Operations'a akışına olanak sağlar.</span><span class="sxs-lookup"><span data-stu-id="dfa6e-105">The integration templates that are available with the Data Integration feature enable the flow of projects, project contracts, project contract lines, project contract line milestones, project tasks, expense transaction categories, hour estimates, and expense estimates from Project Service Automation to Finance and Operations.</span></span>

> [!NOTE] 
> <span data-ttu-id="dfa6e-106">Dynamics 365 for Finance and Operations, Enterprise sürüm 7.3.0 kullanıyorsanız KB 4074835'i yüklemeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="dfa6e-106">If you are using Dynamics 365 for Finance and Operations, Enterprise edition 7.3.0, you must install KB 4074835.</span></span> <span data-ttu-id="dfa6e-107">Bu, sabit fiyatlı projeleri tümleştirmenize olanak sağlar.</span><span class="sxs-lookup"><span data-stu-id="dfa6e-107">This will allow you to integrate fixed price projects.</span></span>
>
> <span data-ttu-id="dfa6e-108">Dynamics 365 for Finance and Operations sürüm 8.0 kullanıyorsanız, proje görevleri tümleştirmesini, gider hareketi kategorilerini, saat tahminlerini, gider tahminlerini ve işlev kilitlemeyi kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="dfa6e-108">If you are using Dynamics 365 for Finance and Operations version 8.0, you will be able to use project tasks integration, expense transaction categories, hour estimates, expense estimates, and functionality locking.</span></span>
>
> <span data-ttu-id="dfa6e-109">Dynamics 365 for Finance and Operations sürüm 8.0.1 kullanıyorsanız gerçek değerleri eşitleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="dfa6e-109">If you are using Dynamics 365 for Finance and Operations version 8.0.1, you will be able to synchronize actuals.</span></span>
>
> <span data-ttu-id="dfa6e-110">Dynamics 365 for Finance and Operations, Enterprise sürümü 7.3.0 kullanıyorsanız, KB 4132657 ve KB 4132660 yükledikten sonra, proje görevlerini, gider hareketi kategorilerini, saat tahminlerini, gider tahminlerini ve gerçek değerleri tümleştirmek ve işlev kilitlemeyi yapılandırmak için şablonları kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="dfa6e-110">If you are using Dynamics 365 for Finance and Operations, Enterprise edition 7.3.0, after you install KB 4132657 and KB 4132660, you will be able to use the templates to integrate project tasks, expense transaction categories, hour estimates, expense estimates, and actuals, and to configure functionality locking.</span></span> <span data-ttu-id="dfa6e-111">Muhasebe dağıtımlarını sıfırlamanız gerekiyorsa KB 4131710'u da yüklemenizi öneririz.</span><span class="sxs-lookup"><span data-stu-id="dfa6e-111">If you must reset the accounting distributions, we recommend that you also install KB 4131710.</span></span>

<span data-ttu-id="dfa6e-112">Project Service Automation'ı Finance and Operations'la tümleştirebilmeniz için Project Service Automation tümleştirme parametrelerini yapılandırmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="dfa6e-112">Before you can integrate Project Service Automation with Finance and Operations, you must configure the Project Service Automation integration parameters.</span></span> <span data-ttu-id="dfa6e-113">Daha fazla bilgi için bkz: Project Service Automation tümleştirme parametreleri.</span><span class="sxs-lookup"><span data-stu-id="dfa6e-113">For more information, see Project Service Automation integration parameters.</span></span>

<span data-ttu-id="dfa6e-114">Bu tümleştirme çözümü aşağıdaki senaryolarda doğrudan eşitlemeyi etkinleştirir:</span><span class="sxs-lookup"><span data-stu-id="dfa6e-114">This integration solution enables direct synchronization in the following scenarios:</span></span>

- <span data-ttu-id="dfa6e-115">Proje sözleşmelerini Project Service Automation'da yönetme ve Project Service Automation'dan Finance and Operations'a doğrudan eşitleme.</span><span class="sxs-lookup"><span data-stu-id="dfa6e-115">Maintain project contracts in Project Service Automation, and synchronize them directly from Project Service Automation to Finance and Operations.</span></span>
- <span data-ttu-id="dfa6e-116">Project Service Automation'da projeler oluşturma ve bu projeleri Project Service Automation'dan Finance and Operations'a doğrudan eşitleme.</span><span class="sxs-lookup"><span data-stu-id="dfa6e-116">Create projects in Project Service Automation, and synchronize them directly from Project Service Automation to Finance and Operations.</span></span>
- <span data-ttu-id="dfa6e-117">Proje sözleşme satırlarını Project Service Automation'da yönetme ve Project Service Automation'dan Finance and Operations'a doğrudan eşitleme.</span><span class="sxs-lookup"><span data-stu-id="dfa6e-117">Maintain project contract lines in Project Service Automation, and synchronize them directly from Project Service Automation to Finance and Operations.</span></span>
- <span data-ttu-id="dfa6e-118">Proje sözleşme satırı kilometre taşlarını Project Service Automation'da yönetme ve Project Service Automation'dan Finance and Operations'a doğrudan eşitleme.</span><span class="sxs-lookup"><span data-stu-id="dfa6e-118">Maintain project contract line milestones in Project Service Automation, and synchronize them directly from Project Service Automation to Finance and Operations.</span></span>
- <span data-ttu-id="dfa6e-119">Proje görevlerini Project Service Automation'da yönetme ve Project Service Automation'dan Finance and Operations'a doğrudan eşitleme.</span><span class="sxs-lookup"><span data-stu-id="dfa6e-119">Maintain project tasks in Project Service Automation, and synchronize them directly from Project Service Automation to Finance and Operations.</span></span>
- <span data-ttu-id="dfa6e-120">Gider hareketi kategorilerini Finance and Operations'ta yönetme ve Finance and Operations'tan Project Service Automation'a doğrudan eşitleme.</span><span class="sxs-lookup"><span data-stu-id="dfa6e-120">Maintain expense transaction categories in Finance and Operations, and synchronize them directly from Finance and Operations to Project Service Automation.</span></span>
- <span data-ttu-id="dfa6e-121">Project Service Automation'da proje saat tahminleri oluşturma ve bunları Project Service Automation'dan Finance and Operations'a doğrudan eşitleme.</span><span class="sxs-lookup"><span data-stu-id="dfa6e-121">Create project hour estimates in Project Service Automation, and synchronize them directly from Project Service Automation to Finance and Operations.</span></span>
- <span data-ttu-id="dfa6e-122">Project Service Automation'da proje gider tahminleri oluşturma ve bunları Project Service Automation'dan Finance and Operations'a doğrudan eşitleme.</span><span class="sxs-lookup"><span data-stu-id="dfa6e-122">Create project expense estimates in Project Service Automation, and synchronize them directly from Project Service Automation to Finance and Operations.</span></span>

## <a name="data-synchronization"></a><span data-ttu-id="dfa6e-123">Veri eşitleme</span><span class="sxs-lookup"><span data-stu-id="dfa6e-123">Data synchronization</span></span>
<span data-ttu-id="dfa6e-124">Aşağıdaki şekilde, Project Service Automation ile Finance and Operations arasında verilerin tümleştirmenin bir parçası olarak nasıl eşitlendiği gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="dfa6e-124">The following illustration shows how data is synchronized as part of the integration between Project Service Automation and Finance and Operations.</span></span>

> [!NOTE]
> <span data-ttu-id="dfa6e-125">Şu anda tüm şablonlar kullanımda değil.</span><span class="sxs-lookup"><span data-stu-id="dfa6e-125">Not all templates are currently available.</span></span> <span data-ttu-id="dfa6e-126">Şablonlar tamamlandıkça yayınlanacaktır.</span><span class="sxs-lookup"><span data-stu-id="dfa6e-126">Templates will be released as they are completed.</span></span>

<span data-ttu-id="dfa6e-127">[![Finance and Operations ile Project Service Automation tümleştirmesi](./media/PSA-integration.png)](./media/PSA-integration.png)</span><span class="sxs-lookup"><span data-stu-id="dfa6e-127">[![Project Service Automation integration with Finance and Operations](./media/PSA-integration.png)](./media/PSA-integration.png)</span></span>

## <a name="system-requirements-for-finance-and-operations"></a><span data-ttu-id="dfa6e-128">Finance and Operations için sistem gereksinimleri</span><span class="sxs-lookup"><span data-stu-id="dfa6e-128">System requirements for Finance and Operations</span></span>

<span data-ttu-id="dfa6e-129">Project Service Automation'dan Finance and Operations'a tümleştirme çözümünü kullanmak için Microsoft Dynamics 365 for Finance and Operations, Enterprise sürümü 7.3'ü platform güncelleştirmesi 12 veya daha ileri bir platform güncelleştirmesiyle birlikte yüklemeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="dfa6e-129">To use the Project Service Automation to Finance and Operations integration solution, you must install Microsoft Dynamics 365 for Finance and Operations, Enterprise edition 7.3 with platform update 12 or later.</span></span>

## <a name="system-requirements-for-project-service-automation"></a><span data-ttu-id="dfa6e-130">Project Service Automation için sistem gereksinimleri</span><span class="sxs-lookup"><span data-stu-id="dfa6e-130">System requirements for Project Service Automation</span></span>

<span data-ttu-id="dfa6e-131">Project Service Automation'dan Finance and Operations'a tümleştirme çözümünü kullanmak için aşağıdaki bileşenleri yüklemeniz gerekir:</span><span class="sxs-lookup"><span data-stu-id="dfa6e-131">To use the Project Service Automation to Finance and Operations integration solution, you must install the following components:</span></span>

- <span data-ttu-id="dfa6e-132">Microsoft Dynamics 365 for Project Service Automation 9.0.0.0 veya daha ileri bir sürüm.</span><span class="sxs-lookup"><span data-stu-id="dfa6e-132">Microsoft Dynamics 365 for Project Service Automation version 9.0.0.0 or later.</span></span>
- <span data-ttu-id="dfa6e-133">Dynamics 365 for Sales için Aday müşteriden nakde çözümü, sürüm 1.14.0.0 (v14) veya sonrası.</span><span class="sxs-lookup"><span data-stu-id="dfa6e-133">Prospect to cash solution for Dynamics 365 for Sales, version 1.14.0.0 (v14) or later.</span></span>
- <span data-ttu-id="dfa6e-134">Dynamics 365 for Project Service Automation 1.0.0.0 veya daha ileri bir sürüm için Project Service Automation'dan Finance and Operations'a çözümü.</span><span class="sxs-lookup"><span data-stu-id="dfa6e-134">Project Service Automation to Operations solution for Dynamics 365 for Project Service Automation version 1.0.0.0 or later.</span></span>

## <a name="install-the-project-service-automation-to-finance-and-operations-integration-solution-in-your-project-service-automation-instance"></a><span data-ttu-id="dfa6e-135">Project Service Automation'dan Finance and Operations'a tümleştirme çözümünü Project Service Automation örneğinize yükleme</span><span class="sxs-lookup"><span data-stu-id="dfa6e-135">Install the Project Service Automation to Finance and Operations integration solution in your Project Service Automation instance</span></span>



