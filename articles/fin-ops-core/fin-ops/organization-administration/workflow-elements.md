---
title: İş akışı öğeleri
description: Bu konuda, bir iş akışını oluşturan çeşitli öğeler açıklanmaktadır.
author: ChrisGarty
manager: AnnBe
ms.date: 11/03/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: sericks
ms.custom: 56441
ms.assetid: de740262-6ffd-42b9-a325-540eae5cec94
ms.search.region: Global
ms.author: cgarty
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b259d733076193cda793a227bd0bb71c232339d1
ms.sourcegitcommit: b112925c389a460a98c3401cc2c67df7091b066f
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 12/19/2020
ms.locfileid: "4797588"
---
# <a name="workflow-elements"></a><span data-ttu-id="f4c47-103">İş akışı öğeleri</span><span class="sxs-lookup"><span data-stu-id="f4c47-103">Workflow elements</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f4c47-104">Bu konuda, bir iş akışını oluşturan çeşitli öğeler açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="f4c47-104">This topic describes the various elements that make up a workflow.</span></span>

<span data-ttu-id="f4c47-105">İş akışı öğelerden oluşur.</span><span class="sxs-lookup"><span data-stu-id="f4c47-105">A workflow consists of elements.</span></span> <span data-ttu-id="f4c47-106">Aşağıdaki bölümlerde her bir öğe türü tanımlanmıştır.</span><span class="sxs-lookup"><span data-stu-id="f4c47-106">The sections that follow describe each type of element.</span></span>

## <a name="tasks"></a><span data-ttu-id="f4c47-107">Görevler</span><span class="sxs-lookup"><span data-stu-id="f4c47-107">Tasks</span></span>

<span data-ttu-id="f4c47-108">*Görev*, gerçekleştirilmesi gereken bir iş birimidir.</span><span class="sxs-lookup"><span data-stu-id="f4c47-108">A *task* is a unit of work that must be performed.</span></span> <span data-ttu-id="f4c47-109">İş akışına iki tür görev eklenebilir: manuel görevler ve otomatik görevler.</span><span class="sxs-lookup"><span data-stu-id="f4c47-109">Two types of tasks can be added to a workflow: manual tasks and automated tasks.</span></span>

### <a name="manual-task"></a><span data-ttu-id="f4c47-110">Manuel görev</span><span class="sxs-lookup"><span data-stu-id="f4c47-110">Manual task</span></span>

<span data-ttu-id="f4c47-111">*Manuel görev*, kullanıcı tarafından gerçekleştirilmesi gereken bir iş birimidir.</span><span class="sxs-lookup"><span data-stu-id="f4c47-111">A *manual task* is a unit of work that must be performed by a user.</span></span> <span data-ttu-id="f4c47-112">Örneğin, bir gider raporu iş akışı, atanan kullanıcının aşağıdaki eylemleri tamamlamasını gerektiren manuel görevler içerebilir:</span><span class="sxs-lookup"><span data-stu-id="f4c47-112">For example, an expense report workflow can have manual tasks that require the assigned users to complete the following actions:</span></span>

- <span data-ttu-id="f4c47-113">Bir gider raporu ile birlikte gönderilen girişleri incelemek.</span><span class="sxs-lookup"><span data-stu-id="f4c47-113">Review the receipts that are submitted together with an expense report.</span></span>
- <span data-ttu-id="f4c47-114">Bir personel müdürünü aramak.</span><span class="sxs-lookup"><span data-stu-id="f4c47-114">Call an employee's manager.</span></span>

### <a name="automated-task"></a><span data-ttu-id="f4c47-115">Otomatik görev</span><span class="sxs-lookup"><span data-stu-id="f4c47-115">Automated task</span></span>

<span data-ttu-id="f4c47-116">*Otomatik görev*, sistem tarafından gerçekleştirilmesi gereken bir iş birimidir.</span><span class="sxs-lookup"><span data-stu-id="f4c47-116">An *automated task* is a unit of work that must be performed by the system.</span></span> <span data-ttu-id="f4c47-117">İnsan etkileşimi gerekli değildir.</span><span class="sxs-lookup"><span data-stu-id="f4c47-117">No human interaction is required.</span></span> <span data-ttu-id="f4c47-118">Örneğin, bir satış emri iş akışı, sistemin aşağıdaki eylemleri tamamlamasını gerektiren otomatik görevler içerebilir:</span><span class="sxs-lookup"><span data-stu-id="f4c47-118">For example, a sales order workflow can have automated tasks that require the system to complete the following actions:</span></span>

- <span data-ttu-id="f4c47-119">Bir kredi denetimi gerçekleştirmek.</span><span class="sxs-lookup"><span data-stu-id="f4c47-119">Perform a credit check.</span></span>
- <span data-ttu-id="f4c47-120">Bir kayıt yoksa müşteri için bir müşteri kaydı oluşturmak.</span><span class="sxs-lookup"><span data-stu-id="f4c47-120">Create a customer record for the customer, if a record doesn't already exist.</span></span>

## <a name="approval-processes"></a><span data-ttu-id="f4c47-121">Onay işlemleri</span><span class="sxs-lookup"><span data-stu-id="f4c47-121">Approval processes</span></span>

<span data-ttu-id="f4c47-122">*Onay işlemi*, ayrı adımlardan oluşan bir işlemdir.</span><span class="sxs-lookup"><span data-stu-id="f4c47-122">An *approval process* is a process that consists of separate steps.</span></span> <span data-ttu-id="f4c47-123">Her onay adımında, kullanıcı aşağıdaki eylemleri gerçekleştirebilir:</span><span class="sxs-lookup"><span data-stu-id="f4c47-123">At each approval step, the user can perform the following actions:</span></span>

- <span data-ttu-id="f4c47-124">Belgeyi onaylama.</span><span class="sxs-lookup"><span data-stu-id="f4c47-124">Approve the document.</span></span>
- <span data-ttu-id="f4c47-125">Belgeyi reddetme.</span><span class="sxs-lookup"><span data-stu-id="f4c47-125">Reject the document.</span></span>
- <span data-ttu-id="f4c47-126">Belgede değişiklik talep etme.</span><span class="sxs-lookup"><span data-stu-id="f4c47-126">Request a change to the document.</span></span>
- <span data-ttu-id="f4c47-127">Belgeyi onay için başka bir kullanıcıya atama.</span><span class="sxs-lookup"><span data-stu-id="f4c47-127">Assign the document to another user for approval.</span></span>

## <a name="line-item-workflow-elements"></a><span data-ttu-id="f4c47-128">Satır maddesi iş akışı öğeleri</span><span class="sxs-lookup"><span data-stu-id="f4c47-128">Line-item workflow elements</span></span>

<span data-ttu-id="f4c47-129">Belgeleri veya bir belgedeki satır maddelerini işlemek için bir iş akışı oluşturulabilir.</span><span class="sxs-lookup"><span data-stu-id="f4c47-129">A workflow can be created to process either documents or the line items on a document.</span></span> <span data-ttu-id="f4c47-130">Örneğin, zaman çizelgeleri için onay iş akışı hazırladınız.</span><span class="sxs-lookup"><span data-stu-id="f4c47-130">For example, you've created an approval workflow for timesheets.</span></span> <span data-ttu-id="f4c47-131">(Biz bu iş akışına *belge iş akışı* diyeceğiz.) Bu belge iş akışına bir *satır öğesi iş akışı* öğesi ekleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="f4c47-131">(We will refer to this workflow as the *document workflow*.) You can add a *line-item workflow* element to that document workflow.</span></span> <span data-ttu-id="f4c47-132">Satır maddesi öğesi çalıştırıldığında, belgedeki her satır maddesi işlenmek üzere gönderilir.</span><span class="sxs-lookup"><span data-stu-id="f4c47-132">When the line-item element is run, each line item on the document is submitted for processing.</span></span> <span data-ttu-id="f4c47-133">Tüm satır maddelerinin aynı satır maddesi iş akışı tarafından işlenmesini isteyebilirsiniz veya her bir satır maddesinin farklı bir satır maddesi iş akışı tarafından işlenmesini isteyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="f4c47-133">You might want all the line items to be processed by the same line-item workflow, or you might want each line item to be processed by a different line-item workflow.</span></span> <span data-ttu-id="f4c47-134">Bir işçinin aşağıdaki şekle benzer bir zaman çizelgesi gönderdiğini düşünün.</span><span class="sxs-lookup"><span data-stu-id="f4c47-134">Imagine that an employee has submitted a timesheet that resembles the following figure.</span></span>

![Satır öğeleri ile iş akışı](./media/workflow_lineitemworkflow.gif)

<span data-ttu-id="f4c47-136">Bu senaryoda, aşağıdaki satır maddesi iş akışlarını oluşturmak isteyebilirsiniz:</span><span class="sxs-lookup"><span data-stu-id="f4c47-136">In this scenario, you might want to create the following line-item workflows:</span></span>

- <span data-ttu-id="f4c47-137">**Satır maddesi iş akışı 1** – Bu iş akışı proje kodunun 1111 olduğu satır maddelerini işlemek için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="f4c47-137">**Line-item workflow 1** – This workflow is used to process line items where the project ID is 1111.</span></span>
- <span data-ttu-id="f4c47-138">**Satır maddesi iş akışı 2** – Bu iş akışı proje kodunun 2222 olduğu satır maddelerini işlemek için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="f4c47-138">**Line-item workflow 2** – This workflow is used to process line items where the project ID is 2222.</span></span>
- <span data-ttu-id="f4c47-139">**Satır maddesi iş akışı 3** – Bu iş akışı proje kodunun 3333 olduğu satır maddelerini işlemek için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="f4c47-139">**Line-item workflow 3** – This workflow is used to process line items where the project ID is 3333.</span></span>

## <a name="flow-control-elements"></a><span data-ttu-id="f4c47-140">Akış kontrolü öğeleri</span><span class="sxs-lookup"><span data-stu-id="f4c47-140">Flow-control elements</span></span>

<span data-ttu-id="f4c47-141">Aşağıdaki öğeler, alternatif dalları veya aynı anda çalışan dalları olan iş akışları tasarlamanıza imkan verir.</span><span class="sxs-lookup"><span data-stu-id="f4c47-141">The following elements let you design workflows that have alternate branches or branches that run at the same time.</span></span>

### <a name="manual-decision"></a><span data-ttu-id="f4c47-142">El ile karar</span><span class="sxs-lookup"><span data-stu-id="f4c47-142">Manual decision</span></span>

<span data-ttu-id="f4c47-143">*Manuel karar*, bir iş akışının iki dala ayrıldığı bir noktadır.</span><span class="sxs-lookup"><span data-stu-id="f4c47-143">A *manual decision* is a point where a workflow divides into two branches.</span></span> <span data-ttu-id="f4c47-144">Bir kullanıcı bir karar almalıdır ve bu karar gönderilen belgeyi işlemek için hangi dalın kullanılacağını belirler.</span><span class="sxs-lookup"><span data-stu-id="f4c47-144">A user must make a decision, and this decision determines which branch is used to process the document that was submitted.</span></span>

### <a name="conditional-decision"></a><span data-ttu-id="f4c47-145">Koşullu karar</span><span class="sxs-lookup"><span data-stu-id="f4c47-145">Conditional decision</span></span>

<span data-ttu-id="f4c47-146">*Koşullu karar* da bir iş akışının iki dala ayrıldığı bir noktadır.</span><span class="sxs-lookup"><span data-stu-id="f4c47-146">A *conditional decision* is also a point where a workflow divides into two branches.</span></span> <span data-ttu-id="f4c47-147">Ancak, gönderilen belgeyi işlemek için hangi dalın kullanılacağına sistem karar verir.</span><span class="sxs-lookup"><span data-stu-id="f4c47-147">However, the system decides which branch is used to process the document that was submitted.</span></span> <span data-ttu-id="f4c47-148">Bu kararı vermek için, sistem belgeyi değerlendirerek belirtilen koşulları karşılayıp karşılamadığını belirler.</span><span class="sxs-lookup"><span data-stu-id="f4c47-148">To make this decision, the system evaluates the document to determine whether it meets specified conditions.</span></span>

### <a name="parallel-activity"></a><span data-ttu-id="f4c47-149">Paralel faaliyet</span><span class="sxs-lookup"><span data-stu-id="f4c47-149">Parallel activity</span></span>

<span data-ttu-id="f4c47-150">*Paralel etkinlik*, aynı anda çalışan iki veya daha fazla iş akışı dalı içeren bir iş akışı öğesidir.</span><span class="sxs-lookup"><span data-stu-id="f4c47-150">A *parallel activity* is a workflow element that includes two or more workflow branches that run at the same time.</span></span>

### <a name="subworkflow"></a><span data-ttu-id="f4c47-151">Alt iş akışı</span><span class="sxs-lookup"><span data-stu-id="f4c47-151">Subworkflow</span></span>

<span data-ttu-id="f4c47-152">*Alt iş akışı*, başka bir iş akışının bağlamında çalışan bir iş akışıdır</span><span class="sxs-lookup"><span data-stu-id="f4c47-152">A *subworkflow* is a workflow that runs in the context of another workflow.</span></span>
