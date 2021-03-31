---
title: Tedarik ve kaynak atama iş akışları
description: Bazı kuruluşlar satınalma taleplerinin ve satınalma siparişlerinin hareketi giren kişiden başka bir kullanıcı tarafından onaylanmasını gerektirir. Bir onay sürecini ayarlamak için iş akışı oluşturabilirsiniz.
author: RichardLuan
manager: tfehr
ms.date: 12/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WorkflowTableListPageRnr
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2074
ms.assetid: e54a1d59-b9fb-421b-821d-01f32878aa9b
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e591007a1330fe11b3f586185f9daca845798908
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5218477"
---
# <a name="procurement-and-sourcing-workflows"></a><span data-ttu-id="0724c-104">Tedarik ve kaynak atama iş akışları</span><span class="sxs-lookup"><span data-stu-id="0724c-104">Procurement and sourcing workflows</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="0724c-105">Bazı kuruluşlar satınalma taleplerinin ve satınalma siparişlerinin hareketi giren kişiden başka bir kullanıcı tarafından onaylanmasını gerektirir.</span><span class="sxs-lookup"><span data-stu-id="0724c-105">Some organizations require that purchase requisitions and purchase orders are approved by a user other than the person who entered the transaction.</span></span> <span data-ttu-id="0724c-106">Bir onay sürecini ayarlamak için iş akışı oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="0724c-106">To set up an approval process, you can create a workflow.</span></span>

<span data-ttu-id="0724c-107">İş akışı, bir iş sürecini temsil eder.</span><span class="sxs-lookup"><span data-stu-id="0724c-107">A workflow represents a business process.</span></span> <span data-ttu-id="0724c-108">Bir belgenin sistem üzerinde nasıl aktığını tanımlar ve bir görevi kimin tamamlaması veya bir belgeyi kimin onaylaması gerektiğini tanımlar.</span><span class="sxs-lookup"><span data-stu-id="0724c-108">It defines how a document flows through the system and indicates who must complete a task or approve a document.</span></span> <span data-ttu-id="0724c-109">İş akışı sistemini kuruluşunuzda kullanmanın bazı getirileri vardır:</span><span class="sxs-lookup"><span data-stu-id="0724c-109">There are several benefits of using the workflow system in your organization:</span></span>

- <span data-ttu-id="0724c-110">**Tutarlı süreçler** — Satınalma talepleri ve gider raporları gibi belirli belgelerin onay sürecini tanımlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="0724c-110">**Consistent processes** — You can define the approval process for specific documents, such as purchase requisitions and expense reports.</span></span> <span data-ttu-id="0724c-111">İş akışı sistemini kullanmak, belgelerin tutarlı ve verimli şekilde işlenmesine ve onaylanmasına yardımcı olur.</span><span class="sxs-lookup"><span data-stu-id="0724c-111">Using the workflow system helps to ensure that documents are processed and approved in a consistent and efficient manner.</span></span>
- <span data-ttu-id="0724c-112">**Süreç görünürlüğü** — Belirli bir iş akışı örneğinin durumunu, geçmişini ve performans ölçülerini takip edebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="0724c-112">**Process visibility** — You can track the status, history, and performance metrics of a specific workflow instance.</span></span> <span data-ttu-id="0724c-113">Bu da iş akışının verimliliği yükseltmesi için değişiklikler yapılması gerekli olup olmadığını belirlemenize yardımcı olur.</span><span class="sxs-lookup"><span data-stu-id="0724c-113">This helps you determine whether changes should be made to the workflow to improve efficiency.</span></span>
- <span data-ttu-id="0724c-114">**Merkezi iş listesi**— Kullanıcılar, iş akışı görevlerini ve katıldıkları tüm iş akışları boyunca kendilerine atanmış onayları görüntülemek için merkezi bir iş listesini görüntüleyebilirler.</span><span class="sxs-lookup"><span data-stu-id="0724c-114">**Centralized work list** — Users can view a centralized work list to view the workflow tasks and approvals assigned to them across all workflows they participate in.</span></span> <span data-ttu-id="0724c-115">Bu iş öğelerini sayfasında mevcuttur.</span><span class="sxs-lookup"><span data-stu-id="0724c-115">This is available in the Work items page.</span></span>

## <a name="the-types-of-workflows-that-you-can-create"></a><span data-ttu-id="0724c-116">Oluşturabileceğiniz iş akışı türleri</span><span class="sxs-lookup"><span data-stu-id="0724c-116">The types of workflows that you can create</span></span>

<span data-ttu-id="0724c-117">Aşağıdaki iş akışı türleri, Tedarik ve kaynak atama için kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="0724c-117">The following workflow types are available for Procurement and sourcing.</span></span>

| <span data-ttu-id="0724c-118">Türü</span><span class="sxs-lookup"><span data-stu-id="0724c-118">Type</span></span> | <span data-ttu-id="0724c-119">Bu türü aşağıdakileri gerçekleştirmek için kullanın:</span><span class="sxs-lookup"><span data-stu-id="0724c-119">Use this type to</span></span> |
|---|---|
| <span data-ttu-id="0724c-120">Satınalma talebi incelemesi</span><span class="sxs-lookup"><span data-stu-id="0724c-120">Purchase requisition review</span></span> | <span data-ttu-id="0724c-121">Satınalma talepleri için gözden geçirme ve onay iş akışları oluşturun.</span><span class="sxs-lookup"><span data-stu-id="0724c-121">Create review and approval workflows for purchase requisitions.</span></span> |
| <span data-ttu-id="0724c-122">Satınalma talep satırı gözden geçir</span><span class="sxs-lookup"><span data-stu-id="0724c-122">Purchase requisition line review</span></span> | <span data-ttu-id="0724c-123">Satınalma talebi satırları için gözden geçirme ve onay iş akışları oluşturun.</span><span class="sxs-lookup"><span data-stu-id="0724c-123">Create review and approval workflows for purchase requisition lines.</span></span> |
| <span data-ttu-id="0724c-124">Satınalma siparişi iş akışı</span><span class="sxs-lookup"><span data-stu-id="0724c-124">Purchase order workflow</span></span> | <span data-ttu-id="0724c-125">Satınalma siparişleri için gözden geçirme ve onay iş akışları oluşturun.</span><span class="sxs-lookup"><span data-stu-id="0724c-125">Create review and approval workflows for purchase orders.</span></span> |
| <span data-ttu-id="0724c-126">Satınalma sipariş satırı iş akışı</span><span class="sxs-lookup"><span data-stu-id="0724c-126">Purchase order line workflow</span></span> | <span data-ttu-id="0724c-127">Satınalma siparişi satırları için gözden geçirme ve onaylama iş akışları oluşturun.</span><span class="sxs-lookup"><span data-stu-id="0724c-127">Create review and approve workflows for purchase order lines.</span></span> |
| <span data-ttu-id="0724c-128">Satıcı uygulama ekleme iş akışı</span><span class="sxs-lookup"><span data-stu-id="0724c-128">Vendor add application workflow</span></span> | <span data-ttu-id="0724c-129">Satıcı talepleri aracılığıyla yeni satıcılar eklemek için gözden geçirme ve onay iş akışları oluşturun.</span><span class="sxs-lookup"><span data-stu-id="0724c-129">Create review and approval workflows for adding new vendors via vendor requests.</span></span> |

> [!IMPORTANT]
> <span data-ttu-id="0724c-130">Yeni bir iş akışı eklerken, **İş akışı oluştur** iletişim kutusunda listelenmiş olan aşağıdaki geçersiz iş akışlarını da görebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="0724c-130">When you are adding a new workflow, you might also see the following obsolete workflows listed in the **Create workflow** dialog box.</span></span> <span data-ttu-id="0724c-131">Bunlar, [Dynamics AX 2012](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-up-procurement-and-sourcing-workflows)'de bulunan fakat artık kullanımdan kaldırılan *giriş onayı* işleviyle ilgilidir.</span><span class="sxs-lookup"><span data-stu-id="0724c-131">These are related to the *confirmation of receipt* functionality that was available in [Dynamics AX 2012](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-up-procurement-and-sourcing-workflows), but which has now been deprecated.</span></span> <span data-ttu-id="0724c-132">Bu iş akışları şu anda desteklenmemektedir.</span><span class="sxs-lookup"><span data-stu-id="0724c-132">These workflows are currently unsupported.</span></span>
> 
> - <span data-ttu-id="0724c-133">Teslimat tarihi bildirimi iş akışı</span><span class="sxs-lookup"><span data-stu-id="0724c-133">Delivery due date notification workflow</span></span>
> - <span data-ttu-id="0724c-134">Fatura alındı bildirimi iş akışı</span><span class="sxs-lookup"><span data-stu-id="0724c-134">Invoice received notification workflow</span></span>
> - <span data-ttu-id="0724c-135">İş akışı bildirim ürün bilgisi başarısız oldu</span><span class="sxs-lookup"><span data-stu-id="0724c-135">Product receipt failed notification workflow</span></span>
> - <span data-ttu-id="0724c-136">Onaylanmayan ürün giriş ret bildirimi iş akışı</span><span class="sxs-lookup"><span data-stu-id="0724c-136">Unconfirmed product receipt rejection notification workflow</span></span>

## <a name="creating-a-workflow"></a><span data-ttu-id="0724c-137">İş akışı oluşturma</span><span class="sxs-lookup"><span data-stu-id="0724c-137">Creating a workflow</span></span>

<span data-ttu-id="0724c-138">Bir iş akışı oluşturmak için, Tedarik ve kaynak atama &gt; Kurulum &gt; Tedarik ve kaynak atama iş akışları menüsüne gidin ve oluşturmak istediğiniz iş akışı türünü seçerek yeni bir iş akışı oluşturun.</span><span class="sxs-lookup"><span data-stu-id="0724c-138">To create a workflow, go to Procurement and sourcing &gt; Setup &gt; Procurement and sourcing workflows and create a new workflow by selecting the type of workflow you want to create.</span></span> 

<span data-ttu-id="0724c-139">İş akışı tuvallerinde, iş akışı öğelerini tasarımcıya sürükleyebilir ve öğeleri bir akışa bağlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="0724c-139">In the workflow canvas you can drag workflow elements into the designer and link the elements into a flow.</span></span> <span data-ttu-id="0724c-140">İş akışı öğeleri yapılandırılmalıdır.</span><span class="sxs-lookup"><span data-stu-id="0724c-140">The workflow elements should be configured.</span></span> <span data-ttu-id="0724c-141">Onay ve görev iş akışı öğeleri için hangi katılımcının eylemi gerçekleştirmesi gerektiğini yapılandırabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="0724c-141">For approval and task workflow elements you can configure which participant should take action.</span></span>

## <a name="types-of-participants"></a><span data-ttu-id="0724c-142">Katılımcı türleri</span><span class="sxs-lookup"><span data-stu-id="0724c-142">Types of participants</span></span>

<span data-ttu-id="0724c-143">Aşağıdaki katımcı gruplarına bir onay adımı atayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="0724c-143">You can assign an approval step to the following groups of participants.</span></span>

| <span data-ttu-id="0724c-144">Kullanıcı grubu</span><span class="sxs-lookup"><span data-stu-id="0724c-144">User group</span></span> | <span data-ttu-id="0724c-145">Açıklama</span><span class="sxs-lookup"><span data-stu-id="0724c-145">Description</span></span> |
|---|---|
| <span data-ttu-id="0724c-146">Katılımcı</span><span class="sxs-lookup"><span data-stu-id="0724c-146">Participant</span></span> | <span data-ttu-id="0724c-147">Bir grubun veya rolün üyelerine onay adımı atayın.</span><span class="sxs-lookup"><span data-stu-id="0724c-147">Assign the approval step to members of a group or role.</span></span> |
| <span data-ttu-id="0724c-148">Hiyerarşi</span><span class="sxs-lookup"><span data-stu-id="0724c-148">Hierarchy</span></span> | <span data-ttu-id="0724c-149">Belirli bir organizasyonel hiyerarşideki kullanıcılara onay adımı atayın.</span><span class="sxs-lookup"><span data-stu-id="0724c-149">Assign the approval step to users in a specific organizational hierarchy.</span></span> |
| <span data-ttu-id="0724c-150">İş akışı kullanıcısı</span><span class="sxs-lookup"><span data-stu-id="0724c-150">Workflow user</span></span> | <span data-ttu-id="0724c-151">Bu iş akışının kullanıcılarına onay adımı atayın.</span><span class="sxs-lookup"><span data-stu-id="0724c-151">Assign the approval step to users of this workflow.</span></span> |
| <span data-ttu-id="0724c-152">Kuyruk</span><span class="sxs-lookup"><span data-stu-id="0724c-152">Queue</span></span> | <span data-ttu-id="0724c-153">Onay adımını bir çalışma öğesi kuyruğa atayın.</span><span class="sxs-lookup"><span data-stu-id="0724c-153">Assign the approval step to a work item queue.</span></span> |
| <span data-ttu-id="0724c-154">Kullanıcı</span><span class="sxs-lookup"><span data-stu-id="0724c-154">User</span></span> | <span data-ttu-id="0724c-155">Onay adımını belirli kullanıcılara atayın.</span><span class="sxs-lookup"><span data-stu-id="0724c-155">Assign the approval step to specific users.</span></span> |

## <a name="additional-resources"></a><span data-ttu-id="0724c-156">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="0724c-156">Additional resources</span></span>

- [<span data-ttu-id="0724c-157">Satınalma talepleri için iş süreci iş akışları tanımlama</span><span class="sxs-lookup"><span data-stu-id="0724c-157">Defining business process workflows for purchase requisitions</span></span>](https://www.microsoft.com/download/details.aspx?id=101821)
- [<span data-ttu-id="0724c-158">Satınalma talebi iş akışı</span><span class="sxs-lookup"><span data-stu-id="0724c-158">Purchase requisition workflow</span></span>](purchase-requisitions-workflow.md)
- [<span data-ttu-id="0724c-159">Satıcıları işe alma</span><span class="sxs-lookup"><span data-stu-id="0724c-159">Onboard vendors</span></span>](vendor-onboarding.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]