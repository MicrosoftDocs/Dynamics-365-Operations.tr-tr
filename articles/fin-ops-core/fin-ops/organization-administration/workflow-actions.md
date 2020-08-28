---
title: İş akışı onay işlemlerindeki eylemler
description: Bu makalede, onay bir iş akışı onay sürecindeki her katılımcının gerçekleştirebileceği eylemler açıklanmaktadır.
author: ChrisGarty
manager: AnnBe
ms.date: 08/23/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 56411
ms.assetid: 65fb711c-6474-42d1-81ed-ca657c29bf1f
ms.search.region: Global
ms.author: cgarty
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0796574c19fa417a8f63187b5d952b853d90e93f
ms.sourcegitcommit: e55efd2f62bf60f678108c09ad4701a76b20cc68
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/17/2020
ms.locfileid: "3698005"
---
# <a name="actions-in-workflow-approval-processes"></a><span data-ttu-id="ab52b-103">İş akışı onay işlemlerindeki eylemler</span><span class="sxs-lookup"><span data-stu-id="ab52b-103">Actions in workflow approval processes</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ab52b-104">Bu makalede, onay bir iş akışı onay sürecindeki her katılımcının gerçekleştirebileceği eylemler açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="ab52b-104">This article explains the actions that each participant in a workflow approval process can take.</span></span>

<span data-ttu-id="ab52b-105">Bir iş akışı çeşitli gruplarda kişiler içerebilir: Başlatıcı, görev alanlar, karar vericiler ve onaylayıcılar.</span><span class="sxs-lookup"><span data-stu-id="ab52b-105">A workflow can involve several groups of people: the originator, task assignees, decision makers, and approvers.</span></span> <span data-ttu-id="ab52b-106">Örneğin, aşağıdaki gider raporu iş akışında, Sam başlatandır, sıranın üyeleri görevin atananlarıdır, John karar vericidir ve Frank, Sue ve Ann de onaylayıcılardır.</span><span class="sxs-lookup"><span data-stu-id="ab52b-106">For example, in the following expense report workflow, Sam is the originator, the members of the queue are task assignees, John is a decision maker, and Frank, Sue, and Ann are approvers.</span></span>

<span data-ttu-id="ab52b-107">[![Workflow\_WithManualDecision](./media/workflow_withmanualdecision.gif)](./media/workflow_withmanualdecision.gif)</span><span class="sxs-lookup"><span data-stu-id="ab52b-107">[![Workflow\_WithManualDecision](./media/workflow_withmanualdecision.gif)](./media/workflow_withmanualdecision.gif)</span></span>

<span data-ttu-id="ab52b-108">Aşağıdaki bölümlerde her grubun gerçekleştirebileceği iş akışı eylemleri açıklanmıştır.</span><span class="sxs-lookup"><span data-stu-id="ab52b-108">The following sections explain the workflow actions that each group can perform.</span></span>

## <a name="actions-that-an-originator-can-perform"></a><span data-ttu-id="ab52b-109">Başlatanın yerine getirebileceği eylemler</span><span class="sxs-lookup"><span data-stu-id="ab52b-109">Actions that an originator can perform</span></span>

<span data-ttu-id="ab52b-110">Başlatan, işlenmek üzere bir belge göndererek bir iş akışı örneğini başlatır.</span><span class="sxs-lookup"><span data-stu-id="ab52b-110">The originator starts a workflow instance by submitting a document for processing.</span></span> <span data-ttu-id="ab52b-111">Örneğin, Sam kendi gider raporu göndermek için **Gider raporu** sayfasında **Gönder** düğmesini tıklatmalıdır.</span><span class="sxs-lookup"><span data-stu-id="ab52b-111">For example, Sam must click the **Submit** button on the **Expense report** page to submit his expense report.</span></span>

## <a name="actions-that-a-task-assignee-can-perform"></a><span data-ttu-id="ab52b-112">Görev alanın yerine getirebileceği eylemler</span><span class="sxs-lookup"><span data-stu-id="ab52b-112">Actions that a task assignee can perform</span></span>

<span data-ttu-id="ab52b-113">Bir görev birden fazla kişiye veya birkaç kişi tarafından izlenen bir iş öğesi sırasına atanabilir.</span><span class="sxs-lookup"><span data-stu-id="ab52b-113">A task can be assigned to multiple people or to a work item queue that is monitored by several people.</span></span> <span data-ttu-id="ab52b-114">Ancak bir görevi yalnızca bir kişi tamamlayabilir.</span><span class="sxs-lookup"><span data-stu-id="ab52b-114">However, only one person can complete a task.</span></span> <span data-ttu-id="ab52b-115">Örneğin, Sam bir gider raporu gönderdi ve kendi girişlerini kuruluşunun Gider raporları bölümünün gözden geçirmesi için yönlendirdi.</span><span class="sxs-lookup"><span data-stu-id="ab52b-115">For example, Sam has submitted an expense report and has routed his receipts to his organization's Expense Reports department for review.</span></span>

<span data-ttu-id="ab52b-116">Adventure Works gider raporları bölümünün üyeleri sırayı izler.</span><span class="sxs-lookup"><span data-stu-id="ab52b-116">The members of the Adventure Works Expense Reports department monitor the queue.</span></span> <span data-ttu-id="ab52b-117">Bu departman üyesi olan Julie, Sam'ın gider raporu ve girişlerini gözden geçirme görevini kabul etti.</span><span class="sxs-lookup"><span data-stu-id="ab52b-117">Julie, a member of that department, has accepted the task of reviewing Sam's expense report and receipts.</span></span> <span data-ttu-id="ab52b-118">Şimdi aşağıdaki eylemlerden birini gerçekleştirebilir: Tamamlama, reddetme, temsilci seçme, değişiklik talep etme, yeniden atama veya yayımlama.</span><span class="sxs-lookup"><span data-stu-id="ab52b-118">She can now perform one of the following actions: complete, reject, delegate, request change, reassign, or release.</span></span>

> [!NOTE]
> <span data-ttu-id="ab52b-119">Gerçekleştirilebilecek eylemler, yazılım geliştiricisinin görevi nasıl tasarladığına bağlı olarak değişebilir.</span><span class="sxs-lookup"><span data-stu-id="ab52b-119">The actions that are available vary, depending on how the software developer designed the task.</span></span>

### <a name="complete"></a><span data-ttu-id="ab52b-120">Tamamla</span><span class="sxs-lookup"><span data-stu-id="ab52b-120">Complete</span></span>

<span data-ttu-id="ab52b-121">Bir kullanıcı bir görevi tamamladığında, işlenmek üzere gönderilen belge, iş akışında yer alan bir sonraki kullanıcıya (eğer mevcutsa) atanır.</span><span class="sxs-lookup"><span data-stu-id="ab52b-121">When a user completes a task, the document that was submitted for processing is assigned to the next user in the workflow, if there is a next user.</span></span> <span data-ttu-id="ab52b-122">Başka işlem gerekmiyorsa, iş akışı süreci sona erer.</span><span class="sxs-lookup"><span data-stu-id="ab52b-122">If no additional processing is required, the workflow process ends.</span></span>

<span data-ttu-id="ab52b-123">Örneğin, Adventure Works Gider Raporları departmanı üyesi olan Julie, Sam'ın gider raporu ve girişlerini gözden geçirme görevini kabul etti.</span><span class="sxs-lookup"><span data-stu-id="ab52b-123">For example, Julie, a member of the Adventure Works Expense Reports department, has accepted the task of reviewing Sam's expense report and receipts.</span></span> <span data-ttu-id="ab52b-124">Julie her gözden geçirme işlemi tamamlandıktan sonra belgeyi John'a atanır.</span><span class="sxs-lookup"><span data-stu-id="ab52b-124">After Julie completes her review, the document is assigned to John.</span></span>

### <a name="reject"></a><span data-ttu-id="ab52b-125">Reddet</span><span class="sxs-lookup"><span data-stu-id="ab52b-125">Reject</span></span>

<span data-ttu-id="ab52b-126">Bir kullanıcı bir belgeyi reddettiğinde iş akışı süreci sona erer.</span><span class="sxs-lookup"><span data-stu-id="ab52b-126">When a user rejects a document, the workflow process ends.</span></span>

<span data-ttu-id="ab52b-127">Örneğin, Adventure Works Gider Raporları departmanı üyesi olan Julie, Sam'ın gider raporu ve girişlerini gözden geçirme görevini kabul etti.</span><span class="sxs-lookup"><span data-stu-id="ab52b-127">For example, Julie, a member of the Adventure Works Expense Reports department, has accepted the task of reviewing Sam's expense report and receipts.</span></span> <span data-ttu-id="ab52b-128">Eğer Julie gider raporunu reddederse, iş akışı işlemi sona erer.</span><span class="sxs-lookup"><span data-stu-id="ab52b-128">If Julie rejects the expense report, the workflow process ends.</span></span>

<span data-ttu-id="ab52b-129">Sam, daha sonra gider raporunu yeniden gönderebilir.</span><span class="sxs-lookup"><span data-stu-id="ab52b-129">Sam can then resubmit the expense report.</span></span> <span data-ttu-id="ab52b-130">Önce değişiklikler yapabilir veya ilk sürümü yeniden gönderebilir.</span><span class="sxs-lookup"><span data-stu-id="ab52b-130">He can make changes first, or he can resubmit the original version.</span></span> <span data-ttu-id="ab52b-131">Sam gider raporunu yeniden gönderirse, iş akışı işlemi el ile inceleme görevinden başlar.</span><span class="sxs-lookup"><span data-stu-id="ab52b-131">If Sam resubmits the expense report, the workflow process starts at the manual review task.</span></span>

### <a name="delegate"></a><span data-ttu-id="ab52b-132">Temsilci</span><span class="sxs-lookup"><span data-stu-id="ab52b-132">Delegate</span></span>

<span data-ttu-id="ab52b-133">Bir kullanıcı görevi devrederse, görev başka bir kullanıcıya atanır.</span><span class="sxs-lookup"><span data-stu-id="ab52b-133">When a user delegates a task, the task is assigned to another user.</span></span>

<span data-ttu-id="ab52b-134">Örneğin, Adventure Works Gider Raporları departmanı üyesi olan Julie, Sam'ın gider raporu ve girişlerini gözden geçirme görevini kabul etti.</span><span class="sxs-lookup"><span data-stu-id="ab52b-134">For example, Julie, a member of the Adventure Works Expense Reports department, has accepted the task of reviewing Sam's expense report and receipts.</span></span> <span data-ttu-id="ab52b-135">Julie, bu görevi onun yardımcısı olan Tim'e devreder.</span><span class="sxs-lookup"><span data-stu-id="ab52b-135">Julie delegates this task to Tim, who is her assistant.</span></span>

<span data-ttu-id="ab52b-136">Bunun üzerine Tim, Julie adına hareket eder.</span><span class="sxs-lookup"><span data-stu-id="ab52b-136">Tim then acts on behalf of Julie.</span></span> <span data-ttu-id="ab52b-137">Bu nedenle, Tim kendi incelemesini tamamlandığında, sanki görevi bitiren Julie gibi, gider raporu John'a atanır.</span><span class="sxs-lookup"><span data-stu-id="ab52b-137">Therefore, when Tim completes his review, the expense report is assigned to John, just as if Julie had completed the task.</span></span>

### <a name="request-change"></a><span data-ttu-id="ab52b-138">Değişiklik iste</span><span class="sxs-lookup"><span data-stu-id="ab52b-138">Request change</span></span>

<span data-ttu-id="ab52b-139">Bir kullanıcı gönderilen belgede değişiklik yapılmasını talep ederse, belge başlatana geri gönderilir.</span><span class="sxs-lookup"><span data-stu-id="ab52b-139">When a user requests a change to a document that was submitted, the document is sent back to the originator.</span></span>

<span data-ttu-id="ab52b-140">Örneğin, Adventure Works Gider Raporları departmanı üyesi olan Julie, Sam'ın gider raporu ve girişlerini gözden geçirme görevini kabul etti.</span><span class="sxs-lookup"><span data-stu-id="ab52b-140">For example, Julie, a member of the Adventure Works Expense Reports department, has accepted the task of reviewing Sam's expense report and receipts.</span></span> <span data-ttu-id="ab52b-141">Julie, gider raporunda bir kaç hata fark eder ve değişiklik talebinde bulunur.</span><span class="sxs-lookup"><span data-stu-id="ab52b-141">Julie notices some errors on the expense report and requests changes.</span></span> <span data-ttu-id="ab52b-142">Gider raporu Sam'e geri gönderilir.</span><span class="sxs-lookup"><span data-stu-id="ab52b-142">The expense report is sent back to Sam.</span></span>

<span data-ttu-id="ab52b-143">Sam, daha sonra gider raporunu yeniden gönderebilir.</span><span class="sxs-lookup"><span data-stu-id="ab52b-143">Sam can resubmit the expense report.</span></span> <span data-ttu-id="ab52b-144">Önce talep edilen değişiklikleri yapabilir veya ilk sürümü yeniden gönderebilir.</span><span class="sxs-lookup"><span data-stu-id="ab52b-144">He can make the requested changes first, or he can resubmit the original version.</span></span> <span data-ttu-id="ab52b-145">Sam gider raporu yeniden gönderirse, çalışma öğesini sırasının bir üyesi gider raporu ve girişleri yeniden gözden geçirmek zorundadır.</span><span class="sxs-lookup"><span data-stu-id="ab52b-145">If Sam resubmits the expense report, a member of the work item queue must review the expense report and the receipts again.</span></span>

### <a name="reassign"></a><span data-ttu-id="ab52b-146">Yeniden Ata</span><span class="sxs-lookup"><span data-stu-id="ab52b-146">Reassign</span></span>

<span data-ttu-id="ab52b-147">Bir iş öğesi sırasının üyeleri o sırada bulunan belgeleri bir başka sıraya yeniden atayabilirler.</span><span class="sxs-lookup"><span data-stu-id="ab52b-147">The members of a work item queue can reassign documents that are in that queue to another queue.</span></span>

<span data-ttu-id="ab52b-148">Örneğin, Adventure Works Gider Raporları departmanının bir üyesi olan Julie, sırayı izlemektedir.</span><span class="sxs-lookup"><span data-stu-id="ab52b-148">For example, Julie, a member of the Adventure Works Expense Reports department, is monitoring the queue.</span></span> <span data-ttu-id="ab52b-149">İş yükünü dengelemeye yardımcı olmak için, gider raporu ve ona dahil olan girişleri başka bir sıraya yeniden atayabilir.</span><span class="sxs-lookup"><span data-stu-id="ab52b-149">To help balance the workload, she can reassign the expense report, and the receipts that are included with it, to another queue.</span></span>

### <a name="release"></a><span data-ttu-id="ab52b-150">Sürüm</span><span class="sxs-lookup"><span data-stu-id="ab52b-150">Release</span></span>

<span data-ttu-id="ab52b-151">Bazen, bir iş maddesi kuyruğu üyesi görevi kabul eder, ancak daha sonra görevi tamamlayamayacağına karar verebilir.</span><span class="sxs-lookup"><span data-stu-id="ab52b-151">Occasionally, a member of a work item queue might accept a task, but then decide that he or she can't complete the task.</span></span> <span data-ttu-id="ab52b-152">Bu durumda, görevi kabul eden kişi belgeyi iş maddesi kuyruğuna geri bırakabilir.</span><span class="sxs-lookup"><span data-stu-id="ab52b-152">In this case, the person who accepted the task can release the document back to the work item queue.</span></span>

<span data-ttu-id="ab52b-153">Örneğin, Adventure Works Gider Raporları departmanı üyesi olan Julie, Sam'ın gider raporu ve girişlerini gözden geçirme görevini kabul etti.</span><span class="sxs-lookup"><span data-stu-id="ab52b-153">For example, Julie, a member of the Adventure Works Expense Reports department, has accepted the task of reviewing Sam's expense report and receipts.</span></span> <span data-ttu-id="ab52b-154">Eğer Julie, görevi tamamlayamayacağına karar verirse, belgeyi serbest bırakabilir.</span><span class="sxs-lookup"><span data-stu-id="ab52b-154">If Julie decides that she can't complete the task, she can release the document.</span></span> <span data-ttu-id="ab52b-155">Böylece Adventure Works gider raporları bölümünün diğer üyelerinin görevi tamamlayabilmesi için gider raporu sıraya döndürülür.</span><span class="sxs-lookup"><span data-stu-id="ab52b-155">The expense report is returned to the queue, so that other members of the Adventure Works Expense Reports department can complete the task.</span></span>

## <a name="actions-that-a-decision-maker-can-perform"></a><span data-ttu-id="ab52b-156">Bir karar vericinin gerçekleştirebileceği eylemler</span><span class="sxs-lookup"><span data-stu-id="ab52b-156">Actions that a decision maker can perform</span></span>

<span data-ttu-id="ab52b-157">Genellikle, karar vericinin yanıtlaması gereken bir soru olduğundan, belge bir karar vericiye atanır.</span><span class="sxs-lookup"><span data-stu-id="ab52b-157">Typically, a document is assigned to a decision maker, because there is a question that the decision maker must answer.</span></span> <span data-ttu-id="ab52b-158">Sorunun yanıtı genellikle **Evet** veya **Hayır** ya da **Doğru** veya **Yanlış** olur.</span><span class="sxs-lookup"><span data-stu-id="ab52b-158">The answer to the question is typically **Yes** or **No**, or **True** or **False**.</span></span> <span data-ttu-id="ab52b-159">Karar verici bu seçeneklerden birini seçmezse, kararı başkasına devredebilir.</span><span class="sxs-lookup"><span data-stu-id="ab52b-159">If the decision maker doesn't select one of those choices, he or she can delegate the decision.</span></span>

### <a name="choice-1-or-choice-2"></a><span data-ttu-id="ab52b-160">\[Seçenek 1\] veya \[Seçenek 2\]</span><span class="sxs-lookup"><span data-stu-id="ab52b-160">\[Choice 1\] or \[Choice 2\]</span></span>

<span data-ttu-id="ab52b-161">Karar vericinin belgeyle ilgili bir soruyu yanıtlaması gerekir.</span><span class="sxs-lookup"><span data-stu-id="ab52b-161">A decision maker must answer a question that is related to the document.</span></span> <span data-ttu-id="ab52b-162">Sorunun yanıtı genellikle **Evet** veya **Hayır** ya da **Doğru** veya **Yanlış** olur.</span><span class="sxs-lookup"><span data-stu-id="ab52b-162">The answer to the question is typically **Yes** or **No**, or **True** or **False**.</span></span> <span data-ttu-id="ab52b-163">Karar vericinin seçtiği cevap, belgeyi işlemek için kullanılacak iş akışı dalını belirler.</span><span class="sxs-lookup"><span data-stu-id="ab52b-163">The answer that the decision maker selects determines the workflow branch that is used to process the document.</span></span>

<span data-ttu-id="ab52b-164">Örneğin, Sam'in gider raporu John'a atanır.</span><span class="sxs-lookup"><span data-stu-id="ab52b-164">For example, Sam's expense report is assigned to John.</span></span> <span data-ttu-id="ab52b-165">Belgedeki bilginin Sam'in yöneticisini aramaya gerektirip gerektirmediğine karar vermesi gerekir.</span><span class="sxs-lookup"><span data-stu-id="ab52b-165">John must decide whether the information in the document requires a call to Sam's manager.</span></span> <span data-ttu-id="ab52b-166">John çağrının gerekli olduğuna karar verirse, gider raporu Aretha'ya atanır, onun da bunun üzerine Sam'in yöneticisini araması gerekir.</span><span class="sxs-lookup"><span data-stu-id="ab52b-166">If John decides that a call is required, the expense report is assigned to Aretha, who must then call Sam's manager.</span></span> <span data-ttu-id="ab52b-167">Eğer John, aramanın gerekli olmadığına karar verirse, gider raporu onay için Frank'e atanır.</span><span class="sxs-lookup"><span data-stu-id="ab52b-167">If John decides that a call isn't required, the expense report is assigned to Frank for approval.</span></span>

### <a name="delegate"></a><span data-ttu-id="ab52b-168">Temsilci</span><span class="sxs-lookup"><span data-stu-id="ab52b-168">Delegate</span></span>

<span data-ttu-id="ab52b-169">B'r karar verici, karar vermeyi devrederse, belge kararı vermek zorunda olan başka bir kullanıcıya atanır.</span><span class="sxs-lookup"><span data-stu-id="ab52b-169">When a decision maker delegates a decision, the document is assigned to another user who must make the decision.</span></span>

<span data-ttu-id="ab52b-170">Örneğin, Sam'in gider raporu John'a atanır.</span><span class="sxs-lookup"><span data-stu-id="ab52b-170">For example, Sam's expense report is assigned to John.</span></span> <span data-ttu-id="ab52b-171">John, kararı onun asistanı olan Maria'ya devreder.</span><span class="sxs-lookup"><span data-stu-id="ab52b-171">John delegates the decision to Maria, who is his assistant.</span></span>

<span data-ttu-id="ab52b-172">Bunun üzerine Maria, John adına hareket eder.</span><span class="sxs-lookup"><span data-stu-id="ab52b-172">Maria then acts on behalf of John.</span></span> <span data-ttu-id="ab52b-173">Eğer Maria Sam'in yöneticisini aramaya gerek olduğuna karar verirse, gider raporu Aretha'ya atanır, onun da bunun üzerine Sam'in yöneticisini araması gerekir.</span><span class="sxs-lookup"><span data-stu-id="ab52b-173">If Maria decides that a call to Sam's manager is required, the expense report is assigned to Aretha, who must then call Sam's manager.</span></span> <span data-ttu-id="ab52b-174">Eğer Maria, aramanın gerekli olmadığına karar verirse, gider raporu onay için Frank'e atanır.</span><span class="sxs-lookup"><span data-stu-id="ab52b-174">If Maria decides that a call isn't required, the expense report is assigned to Frank for approval.</span></span>

## <a name="actions-that-an-approver-can-perform"></a><span data-ttu-id="ab52b-175">Onaylayanın yerine getirebileceği eylemler</span><span class="sxs-lookup"><span data-stu-id="ab52b-175">Actions that an approver can perform</span></span>

<span data-ttu-id="ab52b-176">Bir belge, bir onaylayana atandığında, onaylayan şu eylemlerden birini gerçekleştirebilir: onaylama, reddetme, devretme veya değişiklik talep etme.</span><span class="sxs-lookup"><span data-stu-id="ab52b-176">When a document is assigned to an approver, the approver can perform one of the following actions: approve, reject, delegate, or request change.</span></span>

### <a name="approve"></a><span data-ttu-id="ab52b-177">Onayla</span><span class="sxs-lookup"><span data-stu-id="ab52b-177">Approve</span></span>

<span data-ttu-id="ab52b-178">Onaylayan belgeyi onayladığında, belge iş akışında yer alan sonraki kullanıcıya (eğer mevcutsa) atanır.</span><span class="sxs-lookup"><span data-stu-id="ab52b-178">When an approver approves a document, the document is assigned to the next user in the workflow, if there is a next user.</span></span> <span data-ttu-id="ab52b-179">Başka işlem gerekmiyorsa, iş akışı süreci sona erer.</span><span class="sxs-lookup"><span data-stu-id="ab52b-179">If no additional processing is required, the workflow process ends.</span></span>

<span data-ttu-id="ab52b-180">Örneğin, Sam için 6.000 ABD Doları için bir gider raporu gönderdi ve bu belge Frank'e atandı.</span><span class="sxs-lookup"><span data-stu-id="ab52b-180">For example, Sam has submitted an expense report for USD 6,000, and this document is assigned to Frank.</span></span> <span data-ttu-id="ab52b-181">Frank belgeyi onayladığında, belge onaylanmak üzere Sue'ya atanır.</span><span class="sxs-lookup"><span data-stu-id="ab52b-181">When Frank approves the document, it's assigned to Sue for approval.</span></span> <span data-ttu-id="ab52b-182">Sue gider raporunu onayladığında, iş akışı işlemi sona erer.</span><span class="sxs-lookup"><span data-stu-id="ab52b-182">When Sue approves the expense report, the workflow process ends.</span></span>

### <a name="reject"></a><span data-ttu-id="ab52b-183">Reddet</span><span class="sxs-lookup"><span data-stu-id="ab52b-183">Reject</span></span>

<span data-ttu-id="ab52b-184">Onaylayan bir belgeyi reddettiğinde iş akışı süreci sona erer.</span><span class="sxs-lookup"><span data-stu-id="ab52b-184">When an approver rejects a document, the workflow process ends.</span></span>

<span data-ttu-id="ab52b-185">Örneğin, Sam 12.000 ABD Doları için bir gider raporu gönderdi ve bu belge Sue'ya atandı.</span><span class="sxs-lookup"><span data-stu-id="ab52b-185">For example, Sam has submitted an expense report for USD 12,000, and this document is assigned to Sue.</span></span> <span data-ttu-id="ab52b-186">Eğer Sue gider raporunu reddederse, iş akışı işlemi sona erer.</span><span class="sxs-lookup"><span data-stu-id="ab52b-186">If Sue rejects the expense report, the workflow process ends.</span></span>

<span data-ttu-id="ab52b-187">Sam, daha sonra gider raporunu yeniden gönderebilir.</span><span class="sxs-lookup"><span data-stu-id="ab52b-187">Sam can resubmit the expense report.</span></span> <span data-ttu-id="ab52b-188">Önce değişiklikleri yapabilir veya gider raporunun ilk sürümünü yeniden gönderebilir.</span><span class="sxs-lookup"><span data-stu-id="ab52b-188">He can make changes first, or he can resubmit the original version of the expense report.</span></span> <span data-ttu-id="ab52b-189">Eğer Sam gider raporunu yeniden gönderirse, iş akışı işlemi onay işleminden başlar.</span><span class="sxs-lookup"><span data-stu-id="ab52b-189">If Sam resubmits the expense report, the workflow process starts at the approval process.</span></span>

### <a name="delegate"></a><span data-ttu-id="ab52b-190">Temsilci</span><span class="sxs-lookup"><span data-stu-id="ab52b-190">Delegate</span></span>

<span data-ttu-id="ab52b-191">Onaylayan bir belgeyi devrettiğinde, belge onay için başka bir kullanıcıya atanır.</span><span class="sxs-lookup"><span data-stu-id="ab52b-191">When an approver delegates a document, the document is assigned to another user for approval.</span></span>

<span data-ttu-id="ab52b-192">Örneğin, Sam için 12.000 ABD Doları için bir gider raporu gönderdi ve bu belge Frank'e atandı.</span><span class="sxs-lookup"><span data-stu-id="ab52b-192">For example, Sam has submitted an expense report for USD 12,000, and this document is assigned to Frank.</span></span> <span data-ttu-id="ab52b-193">Mete gider raporu için temsilci olarak Ayla'yı atar.</span><span class="sxs-lookup"><span data-stu-id="ab52b-193">Frank delegates the expense report to Ann.</span></span>

<span data-ttu-id="ab52b-194">Ann böylece Frank adına hareket eder.</span><span class="sxs-lookup"><span data-stu-id="ab52b-194">Ann then acts on behalf of Frank.</span></span> <span data-ttu-id="ab52b-195">Bu sebeple, Ann belgeyi onayladığında, belge sanki Frank tarafından onaylanmış gibi, onaylanmak üzere Sue'ya atanır.</span><span class="sxs-lookup"><span data-stu-id="ab52b-195">Therefore, when Ann approves the document, it's assigned to Sue for approval, just as if Frank had approved it.</span></span> <span data-ttu-id="ab52b-196">Sue belgeyi onayladıktan sonra, onaylanmak üzere Ann'e gönderilir.</span><span class="sxs-lookup"><span data-stu-id="ab52b-196">After Sue approves the document, it's sent to Ann for approval.</span></span>

### <a name="request-change"></a><span data-ttu-id="ab52b-197">Değişiklik iste</span><span class="sxs-lookup"><span data-stu-id="ab52b-197">Request change</span></span>

<span data-ttu-id="ab52b-198">Onaylayan bir belgede değişiklik yapılmasını talep ederse, belge başlatana geri gönderilir.</span><span class="sxs-lookup"><span data-stu-id="ab52b-198">When an approver requests a change to a document, the document is sent back to the originator.</span></span>

<span data-ttu-id="ab52b-199">Örneğin, Sam 12.000 ABD Doları için bir gider raporu gönderdi ve bu belge Sue'ya atandı.</span><span class="sxs-lookup"><span data-stu-id="ab52b-199">For example, Sam has submitted an expense report for USD 12,000, and this document is assigned to Sue.</span></span> <span data-ttu-id="ab52b-200">Eğer Sue bir değişiklik isteğinde bulunursa, gider raporu Sam'e geri gönderilir.</span><span class="sxs-lookup"><span data-stu-id="ab52b-200">If Sue requests a change, the expense report is sent back to Sam.</span></span>

<span data-ttu-id="ab52b-201">Sam, daha sonra gider raporunu yeniden gönderebilir.</span><span class="sxs-lookup"><span data-stu-id="ab52b-201">Sam can resubmit the expense report.</span></span> <span data-ttu-id="ab52b-202">Önce talep edilen değişiklikleri yapabilir veya gider raporunun ilk sürümünü yeniden gönderebilir.</span><span class="sxs-lookup"><span data-stu-id="ab52b-202">He can make the requested changes first, or he can resubmit the original version of the expense report.</span></span> <span data-ttu-id="ab52b-203">Sam gider raporunu yeniden gönderirse, onaylama işleminde ilk onaylayan Frank olduğu için belge onaylanmak üzere Frank'e gönderilir.</span><span class="sxs-lookup"><span data-stu-id="ab52b-203">If Sam resubmits the expense report, it's sent to Frank for approval, because Frank is the first approver in the approval process.</span></span>
