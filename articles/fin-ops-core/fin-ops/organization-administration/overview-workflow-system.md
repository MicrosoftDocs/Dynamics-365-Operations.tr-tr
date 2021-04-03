---
title: İş akışı sistemine genel bakış
description: Bu konuda iş akışı sistemi açıklanmaktadır.
author: ChrisGarty
manager: AnnBe
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: sericks
ms.custom: 56381
ms.assetid: 20b78595-e1d9-439a-ae1c-a776a3438919
ms.search.region: Global
ms.author: cgarty
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: dd8fba1376dc5e3dbfea888ca5ff5fdeb608fc9d
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/09/2021
ms.locfileid: "5560713"
---
# <a name="workflow-system-overview"></a><span data-ttu-id="9534c-103">İş akışı sistemine genel bakış</span><span class="sxs-lookup"><span data-stu-id="9534c-103">Workflow system overview</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="9534c-104">Bu konuda iş akışı sistemi açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="9534c-104">This topic describes the workflow system.</span></span>

## <a name="what-is-workflow"></a><span data-ttu-id="9534c-105">İş akışı nedir?</span><span class="sxs-lookup"><span data-stu-id="9534c-105">What is workflow?</span></span>

<span data-ttu-id="9534c-106">*İş akışı* terimi, biri sistem olarak ve diğeri iş süreci olarak iki şekilde tanımlanabilir.</span><span class="sxs-lookup"><span data-stu-id="9534c-106">The term *workflow* can be defined in two ways: as a system and as a business process.</span></span>

### <a name="workflow-is-a-system"></a><span data-ttu-id="9534c-107">İş akışı bir sistemdir</span><span class="sxs-lookup"><span data-stu-id="9534c-107">Workflow is a system</span></span>

<span data-ttu-id="9534c-108">İş akışı, Uygulama Nesne Sunucusu (AOS) üzerinde çalışan bir sistemdir.</span><span class="sxs-lookup"><span data-stu-id="9534c-108">Workflow is a system that runs on the Application Object Server (AOS).</span></span> <span data-ttu-id="9534c-109">İş akışı sistemi, bağımsız iş akışları veya iş süreçleri oluşturmak için kullanabileceğiniz işlevselliği sağlar.</span><span class="sxs-lookup"><span data-stu-id="9534c-109">The workflow system provides functionality that you can use to create individual workflows, or business processes.</span></span>

### <a name="workflow-is-a-business-process"></a><span data-ttu-id="9534c-110">İş akışı bir iş sürecidir</span><span class="sxs-lookup"><span data-stu-id="9534c-110">Workflow is a business process</span></span>

<span data-ttu-id="9534c-111">İş akışı, bir iş sürecini temsil eder.</span><span class="sxs-lookup"><span data-stu-id="9534c-111">A workflow represents a business process.</span></span> <span data-ttu-id="9534c-112">Bir görevin kimin tarafından tamamlanacağını, bir kararın kimin tarafından verileceğini veya bir belgenin kimin tarafından onaylanacağını göstererek bir belgenin sistem üzerinde nasıl aktığını veya taşındığını tanımlar.</span><span class="sxs-lookup"><span data-stu-id="9534c-112">It defines how a document flows, or moves, through the system by showing who must complete a task, make a decision, or approve a document.</span></span> <span data-ttu-id="9534c-113">Örneğin, aşağıdaki görselde gider raporları için bir iş akışı gösterilmiştir.</span><span class="sxs-lookup"><span data-stu-id="9534c-113">For example, the following illustration shows a workflow for expense reports.</span></span>

![Kullanıcılara atanan öğelerle birlikte iş akışı](./media/workflow_user.gif)

<span data-ttu-id="9534c-115">Bu iş akışını daha iyi anlamak için Haluk'un 7.000 ABD Doları tutarında bir gider raporu teslim ettiğini düşünün.</span><span class="sxs-lookup"><span data-stu-id="9534c-115">To better understand this workflow, suppose that Sam submits an expense report for USD 7,000.</span></span> <span data-ttu-id="9534c-116">Bu senaryoda, Barış'ın mutlaka Haluk'un kendisine yönlendirdiği makbuzları gözden geçirmesi gerekir.</span><span class="sxs-lookup"><span data-stu-id="9534c-116">In this scenario, Ivan must review the receipts that Sam routes to him.</span></span> <span data-ttu-id="9534c-117">Ardından Atilla ve Sibel'in gider raporunu onaylaması gerekir.</span><span class="sxs-lookup"><span data-stu-id="9534c-117">Then Frank and Sue must approve the expense report.</span></span> <span data-ttu-id="9534c-118">Şimdi ise Sam'in 11,000 TL tutarında bir gider raporu teslim ettiğini varsayın.</span><span class="sxs-lookup"><span data-stu-id="9534c-118">Now suppose that Sam submits an expense report for USD 11,000.</span></span> <span data-ttu-id="9534c-119">Bu senaryoda, Barış'ın makbuzları gözden geçirmesi ve Atilla, Sibel ve Ayla'nın gider raporunu onaylaması gerekir.</span><span class="sxs-lookup"><span data-stu-id="9534c-119">In this scenario, Ivan must review the receipts, and Frank, Sue, and Ann must approve the expense report.</span></span>

## <a name="benefits-of-using-the-workflow-system"></a><span data-ttu-id="9534c-120"> İş akışı sistemini kullanmanın yararları</span><span class="sxs-lookup"><span data-stu-id="9534c-120">Benefits of using the workflow system</span></span>

<span data-ttu-id="9534c-121">İş akışı sistemini kuruluşunuzda kullanmanın bazı getirileri vardır:</span><span class="sxs-lookup"><span data-stu-id="9534c-121">There are several benefits of using the workflow system in your organization:</span></span>

- <span data-ttu-id="9534c-122">**Tutarlı süreçler** – Satın alma talepleri ve gider raporları gibi belirli belgelerin nasıl işlendiğini tanımlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="9534c-122">**Consistent processes** – You can define how specific documents, such as purchase requisitions and expense reports, are processed.</span></span> <span data-ttu-id="9534c-123">İş akışı sistemini kullanarak, belgelerin tutarlı ve verimli şekilde işlenmesini ve onaylanmasını sağlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="9534c-123">By using the workflow system, you ensure that documents are processed and approved in a consistent and efficient manner.</span></span>
- <span data-ttu-id="9534c-124">**Süreç görünürlüğü** – İş akışı örneklerinin durumunu, geçmişini ve performans ölçülerini takip edebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="9534c-124">**Process visibility** – You can track the status, history, and performance metrics of workflow instances.</span></span> <span data-ttu-id="9534c-125">Bu da iş akışının verimliliği yükseltmesi için değişiklikler yapılması gerekli olup olmadığını belirlemenize yardımcı olur.</span><span class="sxs-lookup"><span data-stu-id="9534c-125">This helps you determine whether changes should be made to the workflow to improve efficiency.</span></span>
- <span data-ttu-id="9534c-126">**Merkezi iş listesi** – Kullanıcılar, İş akışı görevlerini ve kendilerine atanmış onayları görmek için merkezi bir çalışma listesini görüntüleyebilir.</span><span class="sxs-lookup"><span data-stu-id="9534c-126">**Centralized work list** – Users can view a centralized work list that displays the workflow tasks and approvals that are assigned to them.</span></span>


## <a name="workflow-content"></a><span data-ttu-id="9534c-127">İş akışı içeriği</span><span class="sxs-lookup"><span data-stu-id="9534c-127">Workflow content</span></span>

+ [<span data-ttu-id="9534c-128">İş akışı sistemi mimarisi</span><span class="sxs-lookup"><span data-stu-id="9534c-128">Workflow system architecture</span></span>](workflow-system-architecture.md)
+ [<span data-ttu-id="9534c-129">İş akışı öğeleri</span><span class="sxs-lookup"><span data-stu-id="9534c-129">Workflow elements</span></span>](workflow-elements.md)
+ [<span data-ttu-id="9534c-130">İş akışı onay süreçlerindeki eylemler</span><span class="sxs-lookup"><span data-stu-id="9534c-130">Actions in workflow approval processes</span></span>](workflow-actions.md)
+ [<span data-ttu-id="9534c-131">İş akışlarına genel bakış</span><span class="sxs-lookup"><span data-stu-id="9534c-131">Create workflows overview</span></span>](create-workflow.md)
+ [<span data-ttu-id="9534c-132">İş akışı özelliklerini yapılandırma</span><span class="sxs-lookup"><span data-stu-id="9534c-132">Configure workflow properties</span></span>](configure-workflow-properties.md)
+ [<span data-ttu-id="9534c-133">İş akışında el ile girilen görevleri yapılandırma</span><span class="sxs-lookup"><span data-stu-id="9534c-133">Configure manual tasks in a workflow</span></span>](configure-manual-task-workflow.md)
+ [<span data-ttu-id="9534c-134">İş akışında otomatikleştirilmiş görevleri yapılandırma</span><span class="sxs-lookup"><span data-stu-id="9534c-134">Configure automated tasks in a workflow</span></span>](configure-automated-task-workflow.md)
+ [<span data-ttu-id="9534c-135">İş akışında onay işlemlerini yapılandırma</span><span class="sxs-lookup"><span data-stu-id="9534c-135">Configure approval processes in a workflow</span></span>](configure-approval-process-workflow.md)
+ [<span data-ttu-id="9534c-136">İş akışında onay adımlarını yapılandırma</span><span class="sxs-lookup"><span data-stu-id="9534c-136">Configure approval steps in a workflow</span></span>](configure-approval-step-workflow.md)
+ [<span data-ttu-id="9534c-137">İş akışında el ile girilen kararları yapılandırma</span><span class="sxs-lookup"><span data-stu-id="9534c-137">Configure manual decisions in a workflow</span></span>](configure-manual-decision-workflow.md)
+ [<span data-ttu-id="9534c-138">İş akışında koşullu kararları yapılandırma</span><span class="sxs-lookup"><span data-stu-id="9534c-138">Configure conditional decisions in a workflow</span></span>](configure-conditional-decision-workflow.md)
+ [<span data-ttu-id="9534c-139">İş akışında paralel etkinlikleri yapılandırma</span><span class="sxs-lookup"><span data-stu-id="9534c-139">Configure parallel activities in a workflow</span></span>](configure-parallel-activity-workflow.md)
+ [<span data-ttu-id="9534c-140">İş akışında paralel dalları yapılandırma</span><span class="sxs-lookup"><span data-stu-id="9534c-140">Configure parallel branches in a workflow</span></span>](configure-parallel-branch-workflow.md)
+ [<span data-ttu-id="9534c-141">Satır maddesi iş akışlarını yapılandırma</span><span class="sxs-lookup"><span data-stu-id="9534c-141">Configure line-item workflows</span></span>](configure-line-item-workflow.md)
+ [<span data-ttu-id="9534c-142">İş akışıyla ilgili SSS</span><span class="sxs-lookup"><span data-stu-id="9534c-142">Workflow FAQ</span></span>](workflow-FAQ.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]