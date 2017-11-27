---
title: "Gider için iş akışlarını ayarla"
description: "Seyahat ve gider belgelerini gözden geçirmek ve onaylamakta kullanılan iş akışı işlemlerini ayarlayabilirsiniz."
author: saraschi2
manager: AnnBe
ms.date: 09/13/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi2
ms.search.validFrom:
- month/year of release that feature was introduced in
- in format yyyy-mm-dd
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 19d725f15f00afce1a2ae4b336226f1dafa94b41
ms.contentlocale: tr-tr
ms.lasthandoff: 11/03/2017

---

# <a name="set-up-workflows-for-expense"></a><span data-ttu-id="b53dc-103">Gider için iş akışlarını ayarla</span><span class="sxs-lookup"><span data-stu-id="b53dc-103">Set up workflows for expense</span></span>

[!include[banner](../includes/banner.md)]<span data-ttu-id="b53dc-104"> Seyahat ve gider belgelerini gözden geçirmek ve onaylamakta kullanılan iş akışı işlemlerini ayarlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="b53dc-104"> You can set up a workflow process that is used to review and approve travel and expense documents.</span></span> <span data-ttu-id="b53dc-105">iş akışlarının tanımlandığı belgeler gider raporları, seyahat talepleri ve nakit avans taleplerini içerebilir.</span><span class="sxs-lookup"><span data-stu-id="b53dc-105">The documents for which workflows can be defined include expense reports, travel requisitions, and cash advance requests.</span></span>

<span data-ttu-id="b53dc-106">İş akışı, bir iş sürecini temsil eder.</span><span class="sxs-lookup"><span data-stu-id="b53dc-106">A workflow represents a business process.</span></span> <span data-ttu-id="b53dc-107">Bir belgenin sistem üzerinde nasıl aktığını tanımlar ve bir görevi kimin tamamlaması veya bir belgeyi kimin onaylaması gerektiğini tanımlar.</span><span class="sxs-lookup"><span data-stu-id="b53dc-107">It defines how a document flows through the system and indicates who must complete a task or approve a document.</span></span> <span data-ttu-id="b53dc-108">İş akışı sistemini kuruluşunuzda kullanmanın bazı getirileri vardır:</span><span class="sxs-lookup"><span data-stu-id="b53dc-108">There are several benefits of using the workflow system in your organization:</span></span>

-   <span data-ttu-id="b53dc-109">**Tutarlı süreçler** — Satınalma talepleri ve gider raporları gibi belirli belgelerin onay sürecini tanımlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="b53dc-109">**Consistent processes** — You can define the approval process for specific documents, such as purchase requisitions and expense reports.</span></span> <span data-ttu-id="b53dc-110">İş akışı sistemini kullanmak, belgelerin tutarlı ve verimli şekilde işlenmesine ve onaylanmasına yardımcı olur.</span><span class="sxs-lookup"><span data-stu-id="b53dc-110">Using the workflow system helps to ensure that documents are processed and approved in a consistent and efficient manner.</span></span>

-   <span data-ttu-id="b53dc-111">Süreç görünürlüğü — Belirli bir iş akışı örneğinin durumunu, geçmişini ve performans ölçülerini takip edebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="b53dc-111">Process visibility — You can track the status, history, and performance metrics of a specific workflow instance.</span></span> <span data-ttu-id="b53dc-112">Bu da iş akışının verimliliği yükseltmesi için değişiklikler yapılması gerekli olup olmadığını belirlemenize yardımcı olur.</span><span class="sxs-lookup"><span data-stu-id="b53dc-112">This helps you determine whether changes should be made to the workflow to improve efficiency.</span></span>

-   <span data-ttu-id="b53dc-113">Merkezi çalışma listesi — Kullanıcılar, iş akışı görevlerini ve kendilerine atanmış onayları görmek için merkezi bir çalışma listesini görüntüleyebilir.</span><span class="sxs-lookup"><span data-stu-id="b53dc-113">Centralized work list — Users can view a centralized work list to view the workflow tasks and approvals assigned to them.</span></span> 

<span data-ttu-id="b53dc-114">**Oluşturabileceğiniz iş akışı türleri**</span><span class="sxs-lookup"><span data-stu-id="b53dc-114">**The types of workflows you can create**</span></span>

<span data-ttu-id="b53dc-115">Aşağıdaki tablo **Gider** içerisinde oluşturabileceğiniz iş akışı türlerini listeler.</span><span class="sxs-lookup"><span data-stu-id="b53dc-115">The following table lists the types of workflows that you can create in **Expense**.</span></span>

| <span data-ttu-id="b53dc-116">**Tip**</span><span class="sxs-lookup"><span data-stu-id="b53dc-116">**Type**</span></span>                           | <span data-ttu-id="b53dc-117">**Bu türü aşağıdakileri gerçekleştirmek için kullanın:**</span><span class="sxs-lookup"><span data-stu-id="b53dc-117">**Use this type to**</span></span>                                                 |     
|------------------------------------|----------------------------------------------------------------------|
| <span data-ttu-id="b53dc-118">**Gider raporu**</span><span class="sxs-lookup"><span data-stu-id="b53dc-118">**Expense report**</span></span>                 | <span data-ttu-id="b53dc-119">Gider raporları için onay iş akışları oluşturun.</span><span class="sxs-lookup"><span data-stu-id="b53dc-119">Create approval workflows for expense reports.</span></span>                       |      
| <span data-ttu-id="b53dc-120">**Gider raporu otomatik olarak deftere nakletme**</span><span class="sxs-lookup"><span data-stu-id="b53dc-120">**Expense report auto posting**</span></span>    | <span data-ttu-id="b53dc-121">Gider raporları için belge otomatik deftere nakil iş akışları oluşturun.</span><span class="sxs-lookup"><span data-stu-id="b53dc-121">Create automatic posting workflows for expense reports.</span></span>              |     
| <span data-ttu-id="b53dc-122">**Gider satırı öğesi**</span><span class="sxs-lookup"><span data-stu-id="b53dc-122">**Expense line item**</span></span>              | <span data-ttu-id="b53dc-123">Gider raporları üzerinde satır maddeleri için onay iş akışları oluşturun.</span><span class="sxs-lookup"><span data-stu-id="b53dc-123">Create approval workflows for line items on expense reports.</span></span>         |     
| <span data-ttu-id="b53dc-124">**Gider satırı öğesi otomatik olarak deftere nakletme**</span><span class="sxs-lookup"><span data-stu-id="b53dc-124">**Expense line item auto posting**</span></span> | <span data-ttu-id="b53dc-125">Gider raporları üzerinde satır maddeleri için otomatik deftere nakil iş akışları oluşturun.</span><span class="sxs-lookup"><span data-stu-id="b53dc-125">Create automatic posting workflows for line items on expense reports.</span></span>|
| <span data-ttu-id="b53dc-126">**Seyahat talebi**</span><span class="sxs-lookup"><span data-stu-id="b53dc-126">**Travel requisition**</span></span>             | <span data-ttu-id="b53dc-127">Seyahat talepleri için onay iş akışları oluşturun.</span><span class="sxs-lookup"><span data-stu-id="b53dc-127">Create approval workflows for travel requisitions.</span></span>                   |    
| <span data-ttu-id="b53dc-128">**Nakit avans isteği**</span><span class="sxs-lookup"><span data-stu-id="b53dc-128">**Cash advance request**</span></span>           | <span data-ttu-id="b53dc-129">Nakit avans talepleri için onay iş akışları oluşturun.</span><span class="sxs-lookup"><span data-stu-id="b53dc-129">Create approval workflows for cash advance requests.</span></span>                 |     
| <span data-ttu-id="b53dc-130">**KDV vergisinden düşme**</span><span class="sxs-lookup"><span data-stu-id="b53dc-130">**VAT tax recovery**</span></span>               | <span data-ttu-id="b53dc-131">Katma değer vergisi (KDV) düşürme için onay iş akışları oluşturun.</span><span class="sxs-lookup"><span data-stu-id="b53dc-131">Create approval workflows for the recovery of value-added tax (VAT).</span></span> |       

