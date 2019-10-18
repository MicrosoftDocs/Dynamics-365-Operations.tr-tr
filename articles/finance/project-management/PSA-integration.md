---
title: Project Service Automation'a genel bakış
description: Bu konu Dynamics 365 Project Service Automation ile Dynamics 365 Finance tümleştirme çözümü hakkında bilgi sağlar.
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
ms.openlocfilehash: 31d72591041f8d8cc327aa7c6578c15731ba13c5
ms.sourcegitcommit: 2460d0da812c45fce67a061386db52e0ae46b0f3
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/30/2019
ms.locfileid: "2250565"
---
# <a name="project-service-automation-overview"></a><span data-ttu-id="eaff5-103">Project Service Automation'a genel bakış</span><span class="sxs-lookup"><span data-stu-id="eaff5-103">Project Service Automation overview</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="eaff5-104">Project Service Automation'tan Finance çözümüne tümleştirme, Veri tümleştirme özelliğini Dynamics 365 Finance ve Dynamics 365 Project Service Automation arasında eşitlemek için Common Data Service aracılığıyla kullanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="eaff5-104">The Project Service Automation to Finance integration solution uses the Data integration feature to synchronize data across instances of Dynamics 365 Finance and Dynamics 365 Project Service Automation via Common Data Service.</span></span> <span data-ttu-id="eaff5-105">Veri tümleştirme özelliğiyle kullanılabilen tümleştirme şablonları, projeler, proje sözleşmeleri, proje sözleşme satırları, proje sözleşme satırı kilometre taşları, proje görevleri, gider hareketi kategorileri, saat tahminleri ve gider tahminlerinin Project Service Automation'dan Finance'a akışına olanak tanır.</span><span class="sxs-lookup"><span data-stu-id="eaff5-105">The integration templates that are available with the Data integration feature enable the flow of projects, project contracts, project contract lines, project contract line milestones, project tasks, expense transaction categories, hour estimates, and expense estimates from Project Service Automation to Finance.</span></span>

> [!NOTE]
> - <span data-ttu-id="eaff5-106">Sürüm 7.3.0 kullanıyorsanız KB 4074835'i yüklemeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="eaff5-106">If you're using version 7.3.0, you must install KB 4074835.</span></span> <span data-ttu-id="eaff5-107">Yüklemeden sonra sabit fiyatlı projeleri tümleştirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="eaff5-107">You will then be able to integrate fixed price projects.</span></span>
> - <span data-ttu-id="eaff5-108">Sürüm 7.3.0'ı kullanıyorsanız ve masraf hareketlerini Project Service Automation'dan çağırıyorsanız bu masrafları proje faturasına dahil etmek için KB 4345320'yi yüklemeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="eaff5-108">If you're using version 7.3.0, and you are bringing fee transactions over from Project Service Automation, you must install KB 4345320 in order to include those fees in the project invoice.</span></span>
> - <span data-ttu-id="eaff5-109">Sürüm 8.0 kullanıyorsanız, proje görevleri tümleştirmesini, gider hareketi kategorilerini, saat tahminlerini, gider tahminlerini ve işlev kilitlemeyi kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="eaff5-109">If you're using version 8.0, you will be able to use project task integration, expense transaction categories, hour estimates, expense estimates, and functionality locking.</span></span>
> - <span data-ttu-id="eaff5-110">Sürüm 8.0.1 kullanıyorsanız, fiili değerleri eşitleyebileceksiniz.</span><span class="sxs-lookup"><span data-stu-id="eaff5-110">If you're using version 8.0.1 or later, you will be able to synchronize actuals.</span></span>

<span data-ttu-id="eaff5-111">Project Service Automation'ı Finance'la tümleştirebilmeniz için Project Service Automation tümleştirme parametrelerini yapılandırmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="eaff5-111">Before you can integrate Project Service Automation Finance, you must configure the Project Service Automation integration parameters.</span></span> <span data-ttu-id="eaff5-112">Daha fazla bilgi için bkz. [Project Service Automation tümleştirme parametreleri](PSA-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="eaff5-112">For more information, see [Project Service Automation integration parameters](PSA-parameters.md).</span></span>

<span data-ttu-id="eaff5-113">Bu tümleştirme çözümü aşağıdaki senaryolarda doğrudan eşitlemeyi etkinleştirir:</span><span class="sxs-lookup"><span data-stu-id="eaff5-113">This integration solution enables direct synchronization in the following scenarios:</span></span>

- <span data-ttu-id="eaff5-114">Proje sözleşmelerini Project Service Automation'da yönetme ve Project Service Automation'dan Finance'a doğrudan eşitleme.</span><span class="sxs-lookup"><span data-stu-id="eaff5-114">Maintain project contracts in Project Service Automation, and synchronize them directly from Project Service Automation to Finance.</span></span>
- <span data-ttu-id="eaff5-115">Project Service Automation'da projeler oluşturma ve bu projeleri Project Service Automation'dan Finance'a doğrudan eşitleme.</span><span class="sxs-lookup"><span data-stu-id="eaff5-115">Create projects in Project Service Automation, and synchronize them directly from Project Service Automation to Finance.</span></span>
- <span data-ttu-id="eaff5-116">Proje sözleşme satırları Project Service Automation'da yönetme ve Project Service Automation'dan Finance'a doğrudan eşitleme.</span><span class="sxs-lookup"><span data-stu-id="eaff5-116">Maintain project contract lines in Project Service Automation, and synchronize them directly from Project Service Automation to Finance.</span></span>
- <span data-ttu-id="eaff5-117">Proje sözleşme satırı kilometre taşları Project Service Automation'da yönetme ve Project Service Automation'dan Finance'a doğrudan eşitleme.</span><span class="sxs-lookup"><span data-stu-id="eaff5-117">Maintain project contract line milestones in Project Service Automation, and synchronize them directly from Project Service Automation to Finance.</span></span>
- <span data-ttu-id="eaff5-118">Proje görevlerini Project Service Automation'da yönetme ve Project Service Automation'dan Finance'a doğrudan eşitleme.</span><span class="sxs-lookup"><span data-stu-id="eaff5-118">Maintain project tasks in Project Service Automation, and synchronize them directly from Project Service Automation to Finance.</span></span>
- <span data-ttu-id="eaff5-119">Gider hareketi kategorilerini Finance'ta yönetme ve Finance'tan Project Service Automation'a doğrudan eşitleme.</span><span class="sxs-lookup"><span data-stu-id="eaff5-119">Maintain expense transaction categories in Finance, and synchronize them directly from Finance to Project Service Automation.</span></span>
- <span data-ttu-id="eaff5-120">Project Service Automation'da proje saat tahminleri oluşturma ve bunları Project Service Automation'dan Finance'a doğrudan eşitleme.</span><span class="sxs-lookup"><span data-stu-id="eaff5-120">Create project hour estimates in Project Service Automation, and synchronize them directly from Project Service Automation to Finance.</span></span>
- <span data-ttu-id="eaff5-121">Project Service Automation'da proje gider tahminleri oluşturma ve bunları Project Service Automation'dan Finance'a doğrudan eşitleme.</span><span class="sxs-lookup"><span data-stu-id="eaff5-121">Create project expense estimates in Project Service Automation, and synchronize them directly from Project Service Automation to Finance.</span></span>
- <span data-ttu-id="eaff5-122">Finance'a nakledilebilmeleri için Project Service Automation'da proje süresi, gider ve ücret gerçek değerleri ile Project Service Automation tümleştirme günlüğünde proje hareketleri oluşturun.</span><span class="sxs-lookup"><span data-stu-id="eaff5-122">Create project time, expense, and fee actuals in Project Service Automation, and create project transactions in the Project Service Automation integration journal so that they can be posted in Finance.</span></span>

## <a name="data-synchronization"></a><span data-ttu-id="eaff5-123">Veri eşitleme</span><span class="sxs-lookup"><span data-stu-id="eaff5-123">Data synchronization</span></span>

<span data-ttu-id="eaff5-124">Aşağıdaki şekilde, Project Service Automation ile Finance arasında verilerin tümleştirmenin bir parçası olarak nasıl eşitlendiği gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="eaff5-124">The following illustration shows how data is synchronized as part of the integration between Project Service Automation and Finance.</span></span>

> [!NOTE]
> <span data-ttu-id="eaff5-125">Şu anda tüm şablonlar kullanımda değil.</span><span class="sxs-lookup"><span data-stu-id="eaff5-125">Not all templates are currently available.</span></span> <span data-ttu-id="eaff5-126">Şablonlar tamamlandıkça yayınlanacaktır.</span><span class="sxs-lookup"><span data-stu-id="eaff5-126">Templates will be released as they are completed.</span></span>

<span data-ttu-id="eaff5-127">[![Project Service Automation ile Finance tümleştirmesi](./media/PSA-integration.png)](./media/PSA-integration.png)</span><span class="sxs-lookup"><span data-stu-id="eaff5-127">[![Project Service Automation integration with Finance](./media/PSA-integration.png)](./media/PSA-integration.png)</span></span>

## <a name="system-requirements-for-finance"></a><span data-ttu-id="eaff5-128">Finance için sistem gereksinimleri</span><span class="sxs-lookup"><span data-stu-id="eaff5-128">System requirements for Finance</span></span>

<span data-ttu-id="eaff5-129">Project Service Automation'dan Finance'a tümleştirme çözümünü kullanmak için , Enterprise edition 7.3'ü Platform güncelleştirmesi 12 veya daha ileri bir platform güncelleştirmesiyle birlikte yüklemeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="eaff5-129">To use the Project Service Automation to Finance integration solution, you must install Enterprise edition 7.3 with Platform update 12 or later.</span></span>

## <a name="system-requirements-for-project-service-automation"></a><span data-ttu-id="eaff5-130">Project Service Automation için sistem gereksinimleri</span><span class="sxs-lookup"><span data-stu-id="eaff5-130">System requirements for Project Service Automation</span></span>

<span data-ttu-id="eaff5-131">Project Service Automation'dan Finance'a tümleştirme çözümünü kullanmak için aşağıdaki bileşenleri yüklemeniz gerekir:</span><span class="sxs-lookup"><span data-stu-id="eaff5-131">To use the Project Service Automation to Finance integration solution, you must install the following components:</span></span>

- <span data-ttu-id="eaff5-132">Dynamics 365 Project Service Automation sürüm 9.0.0.0 veya üstü</span><span class="sxs-lookup"><span data-stu-id="eaff5-132">Dynamics 365 Project Service Automation version 9.0.0.0 or later</span></span>
- <span data-ttu-id="eaff5-133">Dynamics 365 Sales için Aday müşteriden nakde çözümü, sürüm 1.14.0.0 (v14) veya sonrası</span><span class="sxs-lookup"><span data-stu-id="eaff5-133">Prospect to cash solution for Dynamics 365 Sales, version 1.14.0.0 (v14) or later</span></span>
- <span data-ttu-id="eaff5-134">Project Service Automation'tan Finance'a çözümü, Dynamics 365 Project Service Automation sürüm 1.0.0.0 veya sonrası için</span><span class="sxs-lookup"><span data-stu-id="eaff5-134">Project Service Automation to Finance solution for Dynamics 365 Project Service Automation version 1.0.0.0 or later</span></span>

## <a name="install-the-project-service-automation-to-finance-integration-solution-in-your-project-service-automation-instance"></a><span data-ttu-id="eaff5-135">Project Service Automation'dan Finance'a tümleştirme çözümünü Project Service Automation örneğinize yükleme</span><span class="sxs-lookup"><span data-stu-id="eaff5-135">Install the Project Service Automation to Finance integration solution in your Project Service Automation instance</span></span>

<span data-ttu-id="eaff5-136">[Microsoft Download Center](https://www.microsoft.com/download/details.aspx?id=57016)'dan Project Service Automation'dan Finance'a tümleştirme çözümünü indirin ve çözümün içinde verilen yönergeleri izleyin.</span><span class="sxs-lookup"><span data-stu-id="eaff5-136">Download the Project Service Automation to Finance integration solution from [Microsoft Download Center](https://www.microsoft.com/download/details.aspx?id=57016), and follow the instructions that are included with the solution.</span></span>
