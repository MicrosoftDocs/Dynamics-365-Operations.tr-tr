---
title: İş akışı sistemi
description: Bu konuda, Microsoft Dynamics 365 for Finance and Operations'daki iş akışı sistemi açıklanmaktadır.
author: sericks007
manager: AnnBe
ms.date: 08/17/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 56381
ms.assetid: 20b78595-e1d9-439a-ae1c-a776a3438919
ms.search.region: Global
ms.author: tjvass
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a35184a48eff9e320087cb9390a0f1eed1e7ba19
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/15/2019
ms.locfileid: "1545821"
---
# <a name="workflow-system"></a><span data-ttu-id="ad5cc-103">İş akışı sistemi</span><span class="sxs-lookup"><span data-stu-id="ad5cc-103">Workflow system</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ad5cc-104">Bu konuda, Microsoft Dynamics 365 for Finance and Operations'daki iş akışı sistemi açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="ad5cc-104">This topic describes the workflow system in Microsoft Dynamics 365 for Finance and Operations.</span></span>

## <a name="what-is-workflow"></a><span data-ttu-id="ad5cc-105">İş akışı nedir?</span><span class="sxs-lookup"><span data-stu-id="ad5cc-105">What is workflow?</span></span>

<span data-ttu-id="ad5cc-106">*İş akışı* terimi, biri sistem olarak ve diğeri iş süreci olarak iki şekilde tanımlanabilir.</span><span class="sxs-lookup"><span data-stu-id="ad5cc-106">The term *workflow* can be defined in two ways: as a system and as a business process.</span></span>

### <a name="workflow-is-a-system"></a><span data-ttu-id="ad5cc-107">İş akışı bir sistemdir</span><span class="sxs-lookup"><span data-stu-id="ad5cc-107">Workflow is a system</span></span>

<span data-ttu-id="ad5cc-108">İş akışı, Finance and Operations ile yüklenen ve Uygulama Nesne Sunucusu (AOS) üzerinde çalışan bir sistemdir.</span><span class="sxs-lookup"><span data-stu-id="ad5cc-108">Workflow is a system that is installed with Finance and Operations and runs on the Application Object Server (AOS).</span></span> <span data-ttu-id="ad5cc-109">İş akışı sistemi, bağımsız iş akışları veya iş süreçleri oluşturmak için kullanabileceğiniz işlevselliği sağlar.</span><span class="sxs-lookup"><span data-stu-id="ad5cc-109">The workflow system provides functionality that you can use to create individual workflows, or business processes.</span></span>

### <a name="workflow-is-a-business-process"></a><span data-ttu-id="ad5cc-110">İş akışı bir iş sürecidir</span><span class="sxs-lookup"><span data-stu-id="ad5cc-110">Workflow is a business process</span></span>

<span data-ttu-id="ad5cc-111">İş akışı, bir iş sürecini temsil eder.</span><span class="sxs-lookup"><span data-stu-id="ad5cc-111">A workflow represents a business process.</span></span> <span data-ttu-id="ad5cc-112">Bir görevin kimin tarafından tamamlanacağını, bir kararın kimin tarafından verileceğini veya bir belgenin kimin tarafından onaylanacağını göstererek bir belgenin sistem üzerinde nasıl aktığını veya taşındığını tanımlar.</span><span class="sxs-lookup"><span data-stu-id="ad5cc-112">It defines how a document flows, or moves, through the system by showing who must complete a task, make a decision, or approve a document.</span></span> <span data-ttu-id="ad5cc-113">Örneğin, aşağıdaki görselde gider raporları için bir iş akışı gösterilmiştir.</span><span class="sxs-lookup"><span data-stu-id="ad5cc-113">For example, the following illustration shows a workflow for expense reports.</span></span>

![Kullanıcılara atanan öğelerle birlikte iş akışı](./media/workflow_user.gif)

<span data-ttu-id="ad5cc-115">Bu iş akışını daha iyi anlamak için Haluk'un 7.000 ABD Doları tutarında bir gider raporu teslim ettiğini düşünün.</span><span class="sxs-lookup"><span data-stu-id="ad5cc-115">To better understand this workflow, suppose that Sam submits an expense report for USD 7,000.</span></span> <span data-ttu-id="ad5cc-116">Bu senaryoda, Barış'ın mutlaka Haluk'un kendisine yönlendirdiği makbuzları gözden geçirmesi gerekir.</span><span class="sxs-lookup"><span data-stu-id="ad5cc-116">In this scenario, Ivan must review the receipts that Sam routes to him.</span></span> <span data-ttu-id="ad5cc-117">Ardından Atilla ve Sibel'in gider raporunu onaylaması gerekir.</span><span class="sxs-lookup"><span data-stu-id="ad5cc-117">Then Frank and Sue must approve the expense report.</span></span> <span data-ttu-id="ad5cc-118">Şimdi ise Sam'in 11,000 TL tutarında bir gider raporu teslim ettiğini varsayın.</span><span class="sxs-lookup"><span data-stu-id="ad5cc-118">Now suppose that Sam submits an expense report for USD 11,000.</span></span> <span data-ttu-id="ad5cc-119">Bu senaryoda, Barış'ın makbuzları gözden geçirmesi ve Atilla, Sibel ve Ayla'nın gider raporunu onaylaması gerekir.</span><span class="sxs-lookup"><span data-stu-id="ad5cc-119">In this scenario, Ivan must review the receipts, and Frank, Sue, and Ann must approve the expense report.</span></span>

## <a name="benefits-of-using-the-workflow-system"></a><span data-ttu-id="ad5cc-120"> İş akışı sistemini kullanmanın yararları</span><span class="sxs-lookup"><span data-stu-id="ad5cc-120">Benefits of using the workflow system</span></span>

<span data-ttu-id="ad5cc-121">İş akışı sistemini kuruluşunuzda kullanmanın bazı getirileri vardır:</span><span class="sxs-lookup"><span data-stu-id="ad5cc-121">There are several benefits of using the workflow system in your organization:</span></span>

- <span data-ttu-id="ad5cc-122">**Tutarlı süreçler** – Satın alma talepleri ve gider raporları gibi belirli belgelerin nasıl işlendiğini tanımlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="ad5cc-122">**Consistent processes** – You can define how specific documents, such as purchase requisitions and expense reports, are processed.</span></span> <span data-ttu-id="ad5cc-123">İş akışı sistemini kullanarak, belgelerin tutarlı ve verimli şekilde işlenmesini ve onaylanmasını sağlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="ad5cc-123">By using the workflow system, you ensure that documents are processed and approved in a consistent and efficient manner.</span></span>
- <span data-ttu-id="ad5cc-124">**Süreç görünürlüğü** – İş akışı örneklerinin durumunu, geçmişini ve performans ölçülerini takip edebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="ad5cc-124">**Process visibility** – You can track the status, history, and performance metrics of workflow instances.</span></span> <span data-ttu-id="ad5cc-125">Bu da iş akışının verimliliği yükseltmesi için değişiklikler yapılması gerekli olup olmadığını belirlemenize yardımcı olur.</span><span class="sxs-lookup"><span data-stu-id="ad5cc-125">This helps you determine whether changes should be made to the workflow to improve efficiency.</span></span>
- <span data-ttu-id="ad5cc-126">**Merkezi iş listesi** – Kullanıcılar, İş akışı görevlerini ve kendilerine atanmış onayları görmek için merkezi bir çalışma listesini görüntüleyebilir.</span><span class="sxs-lookup"><span data-stu-id="ad5cc-126">**Centralized work list** – Users can view a centralized work list that displays the workflow tasks and approvals that are assigned to them.</span></span>


## <a name="workflow-content"></a><span data-ttu-id="ad5cc-127">İş akışı içeriği</span><span class="sxs-lookup"><span data-stu-id="ad5cc-127">Workflow content</span></span>

+ [<span data-ttu-id="ad5cc-128">İş akışı mimarisi</span><span class="sxs-lookup"><span data-stu-id="ad5cc-128">Workflow architecture</span></span>](workflow-system-architecture.md)
+ [<span data-ttu-id="ad5cc-129">İş akışı öğeleri</span><span class="sxs-lookup"><span data-stu-id="ad5cc-129">Workflow elements</span></span>](workflow-elements.md)
+ [<span data-ttu-id="ad5cc-130">İş akışı eylemleri</span><span class="sxs-lookup"><span data-stu-id="ad5cc-130">Workflow actions</span></span>](workflow-actions.md)
+ [<span data-ttu-id="ad5cc-131">İş akışı oluşturma</span><span class="sxs-lookup"><span data-stu-id="ad5cc-131">Create a workflow</span></span>](create-workflow.md)
+ [<span data-ttu-id="ad5cc-132">İş akışı özelliklerini yapılandırma</span><span class="sxs-lookup"><span data-stu-id="ad5cc-132">Configure workflow properties</span></span>](configure-workflow-properties.md)
+ [<span data-ttu-id="ad5cc-133">Bir görev akışında el ile yapılan görevi yapılandır</span><span class="sxs-lookup"><span data-stu-id="ad5cc-133">Configure a manual task in a workflow</span></span>](configure-manual-task-workflow.md)
+ [<span data-ttu-id="ad5cc-134">Bir görev akışında otomatikleştirilmiş görev yapılandır</span><span class="sxs-lookup"><span data-stu-id="ad5cc-134">Configure an automated task in a workflow</span></span>](configure-automated-task-workflow.md)
+ [<span data-ttu-id="ad5cc-135">Bir onay işlemini bir iş akışında yapılandır</span><span class="sxs-lookup"><span data-stu-id="ad5cc-135">Configure an approval process in a workflow</span></span>](configure-approval-process-workflow.md)
+ [<span data-ttu-id="ad5cc-136">Bir onay adımını bir iş akışında yapılandır</span><span class="sxs-lookup"><span data-stu-id="ad5cc-136">Configure an approval step in a workflow</span></span>](configure-approval-step-workflow.md)
+ [<span data-ttu-id="ad5cc-137">Bir iş akışında bir el ile kararı yapılandırma</span><span class="sxs-lookup"><span data-stu-id="ad5cc-137">Configure a manual decision in a workflow</span></span>](configure-manual-decision-workflow.md)
+ [<span data-ttu-id="ad5cc-138">Bir iş akışında koşullu bir kararı yapılandırma</span><span class="sxs-lookup"><span data-stu-id="ad5cc-138">Configure a conditional decision in a workflow</span></span>](configure-conditional-decision-workflow.md)
+ [<span data-ttu-id="ad5cc-139">Bir iş akışında bir paralel etkinlik yapılandırma</span><span class="sxs-lookup"><span data-stu-id="ad5cc-139">Configure a parallel activity in a workflow</span></span>](configure-parallel-activity-workflow.md)
+ [<span data-ttu-id="ad5cc-140">Paralel dalı iş akışında yapılandırma</span><span class="sxs-lookup"><span data-stu-id="ad5cc-140">Configure a parallel branch in a workflow</span></span>](configure-parallel-branch-workflow.md)
+ [<span data-ttu-id="ad5cc-141">Satır maddesi iş akışını yapılandırma</span><span class="sxs-lookup"><span data-stu-id="ad5cc-141">Configure a line-item workflow</span></span>](configure-line-item-workflow.md)
+ [<span data-ttu-id="ad5cc-142">İş akışı SSS</span><span class="sxs-lookup"><span data-stu-id="ad5cc-142">Workflow FAQ</span></span>](workflow-FAQ.md)
