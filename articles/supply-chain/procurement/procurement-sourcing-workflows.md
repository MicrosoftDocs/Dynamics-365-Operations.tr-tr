---
title: Tedarik ve kaynak atama iş akışları
description: Bazı kuruluşlar satınalma taleplerinin ve satınalma siparişlerinin hareketi giren kişiden başka bir kullanıcı tarafından onaylanmasını gerektirir. Bir onay sürecini ayarlamak için iş akışı oluşturabilirsiniz.
author: mkirknel
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WorkflowTableListPageRnr
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 2074
ms.assetid: e54a1d59-b9fb-421b-821d-01f32878aa9b
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 93ceab555bf278ced13d8360956f6db65ba275f8
ms.sourcegitcommit: 57bc7e17682e2edb5e1766496b7a22f4621819dd
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/18/2019
ms.locfileid: "2813466"
---
# <a name="procurement-and-sourcing-workflows"></a><span data-ttu-id="ceea2-104">Tedarik ve kaynak atama iş akışları</span><span class="sxs-lookup"><span data-stu-id="ceea2-104">Procurement and sourcing workflows</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ceea2-105">Bazı kuruluşlar satınalma taleplerinin ve satınalma siparişlerinin hareketi giren kişiden başka bir kullanıcı tarafından onaylanmasını gerektirir.</span><span class="sxs-lookup"><span data-stu-id="ceea2-105">Some organizations require that purchase requisitions and purchase orders are approved by a user other than the person who entered the transaction.</span></span> <span data-ttu-id="ceea2-106">Bir onay sürecini ayarlamak için iş akışı oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="ceea2-106">To set up an approval process, you can create a workflow.</span></span>

<span data-ttu-id="ceea2-107">İş akışı, bir iş sürecini temsil eder.</span><span class="sxs-lookup"><span data-stu-id="ceea2-107">A workflow represents a business process.</span></span> <span data-ttu-id="ceea2-108">Bir belgenin sistem üzerinde nasıl aktığını tanımlar ve bir görevi kimin tamamlaması veya bir belgeyi kimin onaylaması gerektiğini tanımlar.</span><span class="sxs-lookup"><span data-stu-id="ceea2-108">It defines how a document flows through the system and indicates who must complete a task or approve a document.</span></span> <span data-ttu-id="ceea2-109">İş akışı sistemini kuruluşunuzda kullanmanın bazı getirileri vardır:</span><span class="sxs-lookup"><span data-stu-id="ceea2-109">There are several benefits of using the workflow system in your organization:</span></span>
-   <span data-ttu-id="ceea2-110">**Tutarlı süreçler** — Satınalma talepleri ve gider raporları gibi belirli belgelerin onay sürecini tanımlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="ceea2-110">**Consistent processes**— You can define the approval process for specific documents, such as purchase requisitions and expense reports.</span></span> <span data-ttu-id="ceea2-111">İş akışı sistemini kullanmak, belgelerin tutarlı ve verimli şekilde işlenmesine ve onaylanmasına yardımcı olur.</span><span class="sxs-lookup"><span data-stu-id="ceea2-111">Using the workflow system helps to ensure that documents are processed and approved in a consistent and efficient manner.</span></span>
-   <span data-ttu-id="ceea2-112">**Süreç görünürlüğü** — Belirli bir iş akışı örneğinin durumunu, geçmişini ve performans ölçülerini takip edebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="ceea2-112">**Process visibility** — You can track the status, history, and performance metrics of a specific workflow instance.</span></span> <span data-ttu-id="ceea2-113">Bu da iş akışının verimliliği yükseltmesi için değişiklikler yapılması gerekli olup olmadığını belirlemenize yardımcı olur.</span><span class="sxs-lookup"><span data-stu-id="ceea2-113">This helps you determine whether changes should be made to the workflow to improve efficiency.</span></span>
-   <span data-ttu-id="ceea2-114">**Merkezi iş listesi**— Kullanıcılar, iş akışı görevlerini ve katıldıkları tüm iş akışları boyunca kendilerine atanmış onayları görüntülemek için merkezi bir iş listesini görüntüleyebilirler.</span><span class="sxs-lookup"><span data-stu-id="ceea2-114">**Centralized work list** — Users can view a centralized work list to view the workflow tasks and approvals assigned to them across all workflows they participate in.</span></span> <span data-ttu-id="ceea2-115">Bu iş öğelerini sayfasında mevcuttur.</span><span class="sxs-lookup"><span data-stu-id="ceea2-115">This is available in the Work items page.</span></span>

## <a name="the-types-of-workflows-that-you-can-create"></a><span data-ttu-id="ceea2-116"> Oluşturabileceğiniz iş akışı türleri</span><span class="sxs-lookup"><span data-stu-id="ceea2-116">The types of workflows that you can create</span></span>
<span data-ttu-id="ceea2-117">Aşağıdaki iş akışı türleri, Tedarik ve kaynak atama için kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="ceea2-117">The following workflow types are available for Procurement and sourcing.</span></span>

|                                  |                                                               |
|----------------------------------|---------------------------------------------------------------|
| <span data-ttu-id="ceea2-118">**Tip**</span><span class="sxs-lookup"><span data-stu-id="ceea2-118">**Type**</span></span>                         | <span data-ttu-id="ceea2-119">**Bu türü aşağıdakileri gerçekleştirmek için kullanın:**</span><span class="sxs-lookup"><span data-stu-id="ceea2-119">**Use this type to**</span></span>                                          |
| <span data-ttu-id="ceea2-120">Satınalma talebi incelemesi</span><span class="sxs-lookup"><span data-stu-id="ceea2-120">Purchase requisition review</span></span>      | <span data-ttu-id="ceea2-121">Satınalma talepleri için gözden geçirme ve onay iş akışları oluşturun.</span><span class="sxs-lookup"><span data-stu-id="ceea2-121">Create review and approval workflows for purchase requisitions.</span></span>            |
| <span data-ttu-id="ceea2-122">Satınalma talep satırı gözden geçir</span><span class="sxs-lookup"><span data-stu-id="ceea2-122">Purchase requisition line review</span></span> | <span data-ttu-id="ceea2-123">Satınalma talebi satırları için gözden geçirme ve onay iş akışları oluşturun.</span><span class="sxs-lookup"><span data-stu-id="ceea2-123">Create review and approval workflows for purchase requisition lines.</span></span>       |
| <span data-ttu-id="ceea2-124">Satınalma siparişi iş akışı</span><span class="sxs-lookup"><span data-stu-id="ceea2-124">Purchase order workflow</span></span>          | <span data-ttu-id="ceea2-125">Satınalma siparişleri için gözden geçirme ve onay iş akışları oluşturun.</span><span class="sxs-lookup"><span data-stu-id="ceea2-125">Create review and approval workflows for purchase orders.</span></span>     |
| <span data-ttu-id="ceea2-126">Satınalma sipariş satırı iş akışı</span><span class="sxs-lookup"><span data-stu-id="ceea2-126">Purchase order line workflow</span></span>     | <span data-ttu-id="ceea2-127">Satınalma siparişi satırları için gözden geçirme ve onaylama iş akışları oluşturun.</span><span class="sxs-lookup"><span data-stu-id="ceea2-127">Create review and approve workflows for purchase order lines.</span></span> |
| <span data-ttu-id="ceea2-128">Satıcı uygulama ekleme iş akışı</span><span class="sxs-lookup"><span data-stu-id="ceea2-128">Vendor add application workflow</span></span>  | <span data-ttu-id="ceea2-129">Satıcı talepleri aracılığıyla yeni satıcılar eklemek için gözden geçirme ve onay iş akışları oluşturun.</span><span class="sxs-lookup"><span data-stu-id="ceea2-129">Create review and approval workflows for adding new vendors via vendor requests.</span></span> |

## <a name="creating-a-workflow"></a><span data-ttu-id="ceea2-130">İş akışı oluşturma</span><span class="sxs-lookup"><span data-stu-id="ceea2-130">Creating a workflow</span></span>

<span data-ttu-id="ceea2-131">Bir iş akışı oluşturmak için, Tedarik ve kaynak atama &gt; Kurulum &gt; Tedarik ve kaynak atama iş akışları menüsüne gidin ve oluşturmak istediğiniz iş akışı türünü seçerek yeni bir iş akışı oluşturun.</span><span class="sxs-lookup"><span data-stu-id="ceea2-131">To create a workflow, go to Procurement and sourcing &gt; Setup &gt; Procurement and sourcing workflows and create a new workflow by selecting the type of workflow you want to create.</span></span>  

<span data-ttu-id="ceea2-132">İş akışı tuvallerinde, iş akışı öğelerini tasarımcıya sürükleyebilir ve öğeleri bir akışa bağlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="ceea2-132">In the workflow canvas you can drag workflow elements into the designer and link the elements into a flow.</span></span> <span data-ttu-id="ceea2-133">İş akışı öğeleri yapılandırılmalıdır.</span><span class="sxs-lookup"><span data-stu-id="ceea2-133">The workflow elements should be configured.</span></span> <span data-ttu-id="ceea2-134">Onay ve görev iş akışı öğeleri için hangi katılımcının eylemi gerçekleştirmesi gerektiğini yapılandırabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="ceea2-134">For approval and task workflow elements you can configure which participant should take action.</span></span>

## <a name="types-of-participants"></a><span data-ttu-id="ceea2-135"> Katılımcı türleri</span><span class="sxs-lookup"><span data-stu-id="ceea2-135">Types of participants</span></span>

<span data-ttu-id="ceea2-136">Aşağıdaki katımcı gruplarına bir onay adımı atayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="ceea2-136">You can assign an approval step to the following groups of participants.</span></span>

| <span data-ttu-id="ceea2-137">Kullanıcı grubu</span><span class="sxs-lookup"><span data-stu-id="ceea2-137">User group</span></span>    | <span data-ttu-id="ceea2-138">Açıklama</span><span class="sxs-lookup"><span data-stu-id="ceea2-138">Description</span></span>                                                               |
|---------------|---------------------------------------------------------------------------|
| <span data-ttu-id="ceea2-139">Katılımcı</span><span class="sxs-lookup"><span data-stu-id="ceea2-139">Participant</span></span>   | <span data-ttu-id="ceea2-140">Bir grubun veya rolün üyelerine onay adımı atayın.</span><span class="sxs-lookup"><span data-stu-id="ceea2-140">Assign the approval step to members of a group or role.</span></span>                   |
| <span data-ttu-id="ceea2-141">Hiyerarşi</span><span class="sxs-lookup"><span data-stu-id="ceea2-141">Hierarchy</span></span>     | <span data-ttu-id="ceea2-142">Belirli bir organizasyonel hiyerarşideki kullanıcılara onay adımı atayın.</span><span class="sxs-lookup"><span data-stu-id="ceea2-142">Assign the approval step to users in a specific organizational hierarchy.</span></span> |
| <span data-ttu-id="ceea2-143">İş akışı kullanıcısı</span><span class="sxs-lookup"><span data-stu-id="ceea2-143">Workflow user</span></span> | <span data-ttu-id="ceea2-144">Bu iş akışının kullanıcılarına onay adımı atayın.</span><span class="sxs-lookup"><span data-stu-id="ceea2-144">Assign the approval step to users of this workflow.</span></span>                       |
| <span data-ttu-id="ceea2-145">Kuyruk</span><span class="sxs-lookup"><span data-stu-id="ceea2-145">Queue</span></span>         | <span data-ttu-id="ceea2-146">Onay adımını bir çalışma öğesi kuyruğa atayın.</span><span class="sxs-lookup"><span data-stu-id="ceea2-146">Assign the approval step to a work item queue.</span></span>                            |
| <span data-ttu-id="ceea2-147">Kullanıcı</span><span class="sxs-lookup"><span data-stu-id="ceea2-147">User</span></span>          | <span data-ttu-id="ceea2-148">Onay adımını belirli kullanıcılara atayın.</span><span class="sxs-lookup"><span data-stu-id="ceea2-148">Assign the approval step to specific users.</span></span>                               |



## <a name="additional-resources"></a><span data-ttu-id="ceea2-149">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="ceea2-149">Additional resources</span></span>

- [<span data-ttu-id="ceea2-150">Satınalma talepleri için iş süreci iş akışları tanımlama</span><span class="sxs-lookup"><span data-stu-id="ceea2-150">Defining business process workflows for purchase requisitions</span></span>](https://mbs.microsoft.com/customersource/Global/AX/learning/documentation/white-papers/Defining_business_process_workflows_for_purchase_requisitions)

- [<span data-ttu-id="ceea2-151">Satınalma talebi iş akışı</span><span class="sxs-lookup"><span data-stu-id="ceea2-151">Purchase requisition workflow</span></span>](purchase-requisitions-workflow.md)

- [<span data-ttu-id="ceea2-152">Satıcıları işe alma</span><span class="sxs-lookup"><span data-stu-id="ceea2-152">Onboard vendors</span></span>](vendor-onboarding.md)

