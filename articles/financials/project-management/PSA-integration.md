---
title: Project Service Automation'a genel bakış
description: Bu konu, Project Service Automation'dan Finance and Operations'a tümleştirme çözümü hakkında bilgiler sağlar. Bu tümleştirme çözümü Microsoft Dynamics 365 for Finance and Operations ve Microsoft Dynamics 365 for Project Service Automation arasında veri eşitleme için Veri tümleştirme özelliğini Common Data Service aracılığıyla kullanmaktadır.
author: KimANelson
manager: AnnBe
ms.date: 07/25/2019
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
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 85dde35033122ad234ec8efd1bddf64b950578ef
ms.sourcegitcommit: e286572ce94a9442a5b3076c3ff5b429be0ed512
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/06/2019
ms.locfileid: "1865640"
---
# <a name="project-service-automation-overview"></a><span data-ttu-id="8ccf2-104">Project Service Automation'a genel bakış</span><span class="sxs-lookup"><span data-stu-id="8ccf2-104">Project Service Automation overview</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="8ccf2-105">Project Service Automation'tan Finance and Operations çözümüne tümleştirme, Veri tümleştirme özelliğini Microsoft Dynamics 365 for Finance and Operations ve Microsoft Dynamics 365 for Project Service Automation arasında eşitlemek için Common Data Service aracılığıyla kullanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="8ccf2-105">The Project Service Automation to Finance and Operations integration solution uses the Data integration feature to synchronize data across instances of Microsoft Dynamics 365 for Finance and Operations and Microsoft Dynamics 365 for Project Service Automation via Common Data Service.</span></span> <span data-ttu-id="8ccf2-106">Veri tümleştirme özelliğiyle kullanılabilen tümleştirme şablonları, projeler, proje sözleşmeleri, proje sözleşme satırları, proje sözleşme satırı kilometre taşları, proje görevleri, gider hareketi kategorileri, saat tahminleri ve gider tahminlerinin Project Service Automation'dan Finance and Operations'a akışına olanak tanır.</span><span class="sxs-lookup"><span data-stu-id="8ccf2-106">The integration templates that are available with the Data integration feature enable the flow of projects, project contracts, project contract lines, project contract line milestones, project tasks, expense transaction categories, hour estimates, and expense estimates from Project Service Automation to Finance and Operations.</span></span>

> [!NOTE]
> - <span data-ttu-id="8ccf2-107">Microsoft Dynamics 365 for Finance and Operations, Enterprise edition 7.3.0 kullanıyorsanız, KB 4132657 ve KB 4132660 yükledikten sonra, proje görevlerini, gider hareketi kategorilerini, saat tahminlerini, gider tahminlerini ve gerçek değerleri tümleştirmek ve işlev kilitlemeyi yapılandırmak için şablonları kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="8ccf2-107">If you're using Microsoft Dynamics 365 for Finance and Operations, Enterprise edition 7.3.0, after you install KB 4132657 and KB 4132660, you will be able to use the templates to integrate project tasks, expense transaction categories, hour estimates, expense estimates, and actuals, and to configure functionality locking.</span></span> <span data-ttu-id="8ccf2-108">Muhasebe dağıtımlarını sıfırlamanız gerekiyorsa KB 4131710'u da yüklemenizi öneririz.</span><span class="sxs-lookup"><span data-stu-id="8ccf2-108">If you must reset the accounting distributions, we recommend that you also install KB 4131710.</span></span>
> - <span data-ttu-id="8ccf2-109">Finance and Operations 7.3.0 kullanıyorsanız KB 4074835'i yüklemeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="8ccf2-109">If you're using Finance and Operations 7.3.0, you must install KB 4074835.</span></span> <span data-ttu-id="8ccf2-110">Yüklemeden sonra sabit fiyatlı projeleri tümleştirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="8ccf2-110">You will then be able to integrate fixed price projects.</span></span>
> - <span data-ttu-id="8ccf2-111">Finance and Operations 7.3.0 kullanıyorsanız ve Project Service Automation'dan masraf hareketlerini görüntülüyorsanız bu masrafları proje faturasına dahil etmek için KB 4345320'yi yüklemeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="8ccf2-111">If you're using Finance and Operations 7.3.0, and you are bringing fee transactions over from Project Service Automation, you must install KB 4345320 in order to include those fees in the project invoice.</span></span>
> - <span data-ttu-id="8ccf2-112">Microsoft Dynamics 365 for Finance and Operations sürüm 8.0 kullanıyorsanız, proje görevleri tümleştirmesini, gider hareketi kategorilerini, saat tahminlerini, gider tahminlerini ve işlev kilitlemeyi kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="8ccf2-112">If you're using Microsoft Dynamics 365 for Finance and Operations version 8.0, you will be able to use project task integration, expense transaction categories, hour estimates, expense estimates, and functionality locking.</span></span>
> - <span data-ttu-id="8ccf2-113">Microsoft Dynamics 365 for Finance and Operations sürüm 8.0.1 kullanıyorsanız, fiili değerleri eşitleyebileceksiniz.</span><span class="sxs-lookup"><span data-stu-id="8ccf2-113">If you're using Microsoft Dynamics 365 for Finance and Operations version 8.0.1, or later, you will be able to synchronize actuals.</span></span>

<span data-ttu-id="8ccf2-114">Project Service Automation'ı Finance and Operations'la tümleştirebilmeniz için Project Service Automation tümleştirme parametrelerini yapılandırmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="8ccf2-114">Before you can integrate Project Service Automation with Finance and Operations, you must configure the Project Service Automation integration parameters.</span></span> <span data-ttu-id="8ccf2-115">Daha fazla bilgi için bkz. [Project Service Automation tümleştirme parametreleri](PSA-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="8ccf2-115">For more information, see [Project Service Automation integration parameters](PSA-parameters.md).</span></span>

<span data-ttu-id="8ccf2-116">Bu tümleştirme çözümü aşağıdaki senaryolarda doğrudan eşitlemeyi etkinleştirir:</span><span class="sxs-lookup"><span data-stu-id="8ccf2-116">This integration solution enables direct synchronization in the following scenarios:</span></span>

- <span data-ttu-id="8ccf2-117">Proje sözleşmelerini Project Service Automation'da yönetme ve Project Service Automation'dan Finance and Operations'a doğrudan eşitleme.</span><span class="sxs-lookup"><span data-stu-id="8ccf2-117">Maintain project contracts in Project Service Automation, and synchronize them directly from Project Service Automation to Finance and Operations.</span></span>
- <span data-ttu-id="8ccf2-118">Project Service Automation'da projeler oluşturma ve bu projeleri Project Service Automation'dan Finance and Operations'a doğrudan eşitleme.</span><span class="sxs-lookup"><span data-stu-id="8ccf2-118">Create projects in Project Service Automation, and synchronize them directly from Project Service Automation to Finance and Operations.</span></span>
- <span data-ttu-id="8ccf2-119">Proje sözleşme satırlarını Project Service Automation'da yönetme ve Project Service Automation'dan Finance and Operations'a doğrudan eşitleme.</span><span class="sxs-lookup"><span data-stu-id="8ccf2-119">Maintain project contract lines in Project Service Automation, and synchronize them directly from Project Service Automation to Finance and Operations.</span></span>
- <span data-ttu-id="8ccf2-120">Proje sözleşme satırı kilometre taşlarını Project Service Automation'da yönetme ve Project Service Automation'dan Finance and Operations'a doğrudan eşitleme.</span><span class="sxs-lookup"><span data-stu-id="8ccf2-120">Maintain project contract line milestones in Project Service Automation, and synchronize them directly from Project Service Automation to Finance and Operations.</span></span>
- <span data-ttu-id="8ccf2-121">Proje görevlerini Project Service Automation'da yönetme ve Project Service Automation'dan Finance and Operations'a doğrudan eşitleme.</span><span class="sxs-lookup"><span data-stu-id="8ccf2-121">Maintain project tasks in Project Service Automation, and synchronize them directly from Project Service Automation to Finance and Operations.</span></span>
- <span data-ttu-id="8ccf2-122">Gider hareketi kategorilerini Finance and Operations'ta yönetme ve Finance and Operations'tan Project Service Automation'a doğrudan eşitleme.</span><span class="sxs-lookup"><span data-stu-id="8ccf2-122">Maintain expense transaction categories in Finance and Operations, and synchronize them directly from Finance and Operations to Project Service Automation.</span></span>
- <span data-ttu-id="8ccf2-123">Project Service Automation'da proje saat tahminleri oluşturma ve bunları Project Service Automation'dan Finance and Operations'a doğrudan eşitleme.</span><span class="sxs-lookup"><span data-stu-id="8ccf2-123">Create project hour estimates in Project Service Automation, and synchronize them directly from Project Service Automation to Finance and Operations.</span></span>
- <span data-ttu-id="8ccf2-124">Project Service Automation'da proje gider tahminleri oluşturma ve bunları Project Service Automation'dan Finance and Operations'a doğrudan eşitleme.</span><span class="sxs-lookup"><span data-stu-id="8ccf2-124">Create project expense estimates in Project Service Automation, and synchronize them directly from Project Service Automation to Finance and Operations.</span></span>
- <span data-ttu-id="8ccf2-125">Finance and Operations'a nakledilebilmeleri için Project Service Automation'da proje süresi, gider ve ücret gerçek değerleri ile Project Service Automation tümleştirme günlüğünde proje hareketleri oluşturun.</span><span class="sxs-lookup"><span data-stu-id="8ccf2-125">Create project time, expense, and fee actuals in Project Service Automation, and create project transactions in the Project Service Automation integration journal so that they can be posted in Finance and Operations.</span></span>

## <a name="data-synchronization"></a><span data-ttu-id="8ccf2-126">Veri eşitleme</span><span class="sxs-lookup"><span data-stu-id="8ccf2-126">Data synchronization</span></span>

<span data-ttu-id="8ccf2-127">Aşağıdaki şekilde, Project Service Automation ile Finance and Operations arasında verilerin tümleştirmenin bir parçası olarak nasıl eşitlendiği gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="8ccf2-127">The following illustration shows how data is synchronized as part of the integration between Project Service Automation and Finance and Operations.</span></span>

> [!NOTE]
> <span data-ttu-id="8ccf2-128">Şu anda tüm şablonlar kullanımda değil.</span><span class="sxs-lookup"><span data-stu-id="8ccf2-128">Not all templates are currently available.</span></span> <span data-ttu-id="8ccf2-129">Şablonlar tamamlandıkça yayınlanacaktır.</span><span class="sxs-lookup"><span data-stu-id="8ccf2-129">Templates will be released as they are completed.</span></span>

<span data-ttu-id="8ccf2-130">[![Finance and Operations ile Project Service Automation tümleştirmesi](./media/PSA-integration.png)](./media/PSA-integration.png)</span><span class="sxs-lookup"><span data-stu-id="8ccf2-130">[![Project Service Automation integration with Finance and Operations](./media/PSA-integration.png)](./media/PSA-integration.png)</span></span>

## <a name="system-requirements-for-finance-and-operations"></a><span data-ttu-id="8ccf2-131">Finance and Operations için sistem gereksinimleri</span><span class="sxs-lookup"><span data-stu-id="8ccf2-131">System requirements for Finance and Operations</span></span>

<span data-ttu-id="8ccf2-132">Project Service Automation'dan Finance and Operations'a tümleştirme çözümünü kullanmak için Microsoft Dynamics 365 for Finance and Operations, Enterprise edition 7.3'ü platform güncelleştirmesi 12 veya daha ileri bir platform güncelleştirmesiyle birlikte yüklemeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="8ccf2-132">To use the Project Service Automation to Finance and Operations integration solution, you must install Microsoft Dynamics 365 for Finance and Operations, Enterprise edition 7.3 with platform update 12 or later.</span></span>

## <a name="system-requirements-for-project-service-automation"></a><span data-ttu-id="8ccf2-133">Project Service Automation için sistem gereksinimleri</span><span class="sxs-lookup"><span data-stu-id="8ccf2-133">System requirements for Project Service Automation</span></span>

<span data-ttu-id="8ccf2-134">Project Service Automation'dan Finance and Operations'a tümleştirme çözümünü kullanmak için aşağıdaki bileşenleri yüklemeniz gerekir:</span><span class="sxs-lookup"><span data-stu-id="8ccf2-134">To use the Project Service Automation to Finance and Operations integration solution, you must install the following components:</span></span>

- <span data-ttu-id="8ccf2-135">Microsoft Dynamics 365 for Project Service Automation sürüm 9.0.0.0 veya üstü</span><span class="sxs-lookup"><span data-stu-id="8ccf2-135">Microsoft Dynamics 365 for Project Service Automation version 9.0.0.0 or later</span></span>
- <span data-ttu-id="8ccf2-136">Microsoft Dynamics 365 for Sales, sürüm 1.14.0.0 (v14) veya sonraki sürüm için Aday'dan nakite çözüm.</span><span class="sxs-lookup"><span data-stu-id="8ccf2-136">Prospect to cash solution for Microsoft Dynamics 365 for Sales, version 1.14.0.0 (v14) or later</span></span>
- <span data-ttu-id="8ccf2-137">Project Service Automation'tan Finance and Operations'a çözümü, Microsoft Dynamics 365 for Project Service Automation sürüm 1.0.0.0 veya sonrası için</span><span class="sxs-lookup"><span data-stu-id="8ccf2-137">Project Service Automation to Finance and Operations solution for Microsoft Dynamics 365 for Project Service Automation version 1.0.0.0 or later</span></span>

## <a name="install-the-project-service-automation-to-finance-and-operations-integration-solution-in-your-project-service-automation-instance"></a><span data-ttu-id="8ccf2-138">Project Service Automation'dan Finance and Operations'a tümleştirme çözümünü Project Service Automation örneğinize yükleme</span><span class="sxs-lookup"><span data-stu-id="8ccf2-138">Install the Project Service Automation to Finance and Operations integration solution in your Project Service Automation instance</span></span>

<span data-ttu-id="8ccf2-139">[Microsoft Download Center](https://www.microsoft.com/download/details.aspx?id=57016)'dan Project Service Automation'dan Finance and Operations'a tümleştirme çözümünü indirin ve çözümün içinde verilen yönergeleri izleyin.</span><span class="sxs-lookup"><span data-stu-id="8ccf2-139">Download the Project Service Automation to Finance and Operations integration solution from [Microsoft Download Center](https://www.microsoft.com/download/details.aspx?id=57016), and follow the instructions that are included with the solution.</span></span>
