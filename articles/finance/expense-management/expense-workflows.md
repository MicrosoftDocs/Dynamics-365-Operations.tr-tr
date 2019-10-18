---
title: Gider için iş akışlarını ayarla
description: Seyahat ve gider belgelerini gözden geçirmek ve onaylamakta kullanılan iş akışı işlemlerini ayarlayabilirsiniz.
author: ShylaThompson
manager: AnnBe
ms.date: 09/13/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WorkflowtableListPageRnr
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 86cadf7277fbb7e08dad4b5dc2a46e1c6ce5a888
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/27/2019
ms.locfileid: "2180336"
---
# <a name="set-up-workflows-for-expense"></a><span data-ttu-id="1de42-103">Gider için iş akışlarını ayarla</span><span class="sxs-lookup"><span data-stu-id="1de42-103">Set up workflows for expense</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="1de42-104"> Seyahat ve gider belgelerini gözden geçirmek ve onaylamakta kullanılan iş akışı işlemlerini ayarlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="1de42-104">You can set up a workflow process that is used to review and approve travel and expense documents.</span></span> <span data-ttu-id="1de42-105">iş akışlarının tanımlandığı belgeler gider raporları, seyahat talepleri ve nakit avans taleplerini içerebilir.</span><span class="sxs-lookup"><span data-stu-id="1de42-105">The documents for which workflows can be defined include expense reports, travel requisitions, and cash advance requests.</span></span>

<span data-ttu-id="1de42-106">İş akışı, bir iş sürecini temsil eder.</span><span class="sxs-lookup"><span data-stu-id="1de42-106">A workflow represents a business process.</span></span> <span data-ttu-id="1de42-107">Bir belgenin sistem üzerinde nasıl aktığını tanımlar ve bir görevi kimin tamamlaması veya bir belgeyi kimin onaylaması gerektiğini tanımlar.</span><span class="sxs-lookup"><span data-stu-id="1de42-107">It defines how a document flows through the system and indicates who must complete a task or approve a document.</span></span> <span data-ttu-id="1de42-108">İş akışı sistemini kuruluşunuzda kullanmanın bazı getirileri vardır:</span><span class="sxs-lookup"><span data-stu-id="1de42-108">There are several benefits of using the workflow system in your organization:</span></span>

-   <span data-ttu-id="1de42-109">**Tutarlı süreçler** — Satınalma talepleri ve gider raporları gibi belirli belgelerin onay sürecini tanımlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="1de42-109">**Consistent processes** — You can define the approval process for specific documents, such as purchase requisitions and expense reports.</span></span> <span data-ttu-id="1de42-110">İş akışı sistemini kullanmak, belgelerin tutarlı ve verimli şekilde işlenmesine ve onaylanmasına yardımcı olur.</span><span class="sxs-lookup"><span data-stu-id="1de42-110">Using the workflow system helps to ensure that documents are processed and approved in a consistent and efficient manner.</span></span>

-   <span data-ttu-id="1de42-111">Süreç görünürlüğü — Belirli bir iş akışı örneğinin durumunu, geçmişini ve performans ölçülerini takip edebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="1de42-111">Process visibility — You can track the status, history, and performance metrics of a specific workflow instance.</span></span> <span data-ttu-id="1de42-112">Bu da iş akışının verimliliği yükseltmesi için değişiklikler yapılması gerekli olup olmadığını belirlemenize yardımcı olur.</span><span class="sxs-lookup"><span data-stu-id="1de42-112">This helps you determine whether changes should be made to the workflow to improve efficiency.</span></span>

-   <span data-ttu-id="1de42-113">Merkezi çalışma listesi — Kullanıcılar, iş akışı görevlerini ve kendilerine atanmış onayları görmek için merkezi bir çalışma listesini görüntüleyebilir.</span><span class="sxs-lookup"><span data-stu-id="1de42-113">Centralized work list — Users can view a centralized work list to view the workflow tasks and approvals assigned to them.</span></span> 

<span data-ttu-id="1de42-114">**Oluşturabileceğiniz iş akışı türleri**</span><span class="sxs-lookup"><span data-stu-id="1de42-114">**The types of workflows you can create**</span></span>

<span data-ttu-id="1de42-115">Aşağıdaki tablo **Gider** içerisinde oluşturabileceğiniz iş akışı türlerini listeler.</span><span class="sxs-lookup"><span data-stu-id="1de42-115">The following table lists the types of workflows that you can create in **Expense**.</span></span>


|              <span data-ttu-id="1de42-116"><strong>Tip</strong></span><span class="sxs-lookup"><span data-stu-id="1de42-116"><strong>Type</strong></span></span>              |                   <span data-ttu-id="1de42-117"><strong>Bu türü aşağıdakileri gerçekleştirmek için kullanın:</strong></span><span class="sxs-lookup"><span data-stu-id="1de42-117"><strong>Use this type to</strong></span></span>                   |
|-------------------------------------------------|-----------------------------------------------------------------------|
|         <span data-ttu-id="1de42-118"><strong>Gider raporu</strong></span><span class="sxs-lookup"><span data-stu-id="1de42-118"><strong>Expense report</strong></span></span>         |            <span data-ttu-id="1de42-119">Gider raporları için onay iş akışları oluşturun.</span><span class="sxs-lookup"><span data-stu-id="1de42-119">Create approval workflows for expense reports.</span></span>             |
|  <span data-ttu-id="1de42-120"><strong>Gider raporu otomatik olarak deftere nakletme</strong></span><span class="sxs-lookup"><span data-stu-id="1de42-120"><strong>Expense report auto posting</strong></span></span>   |        <span data-ttu-id="1de42-121">Gider raporları için belge otomatik deftere nakil iş akışları oluşturun.</span><span class="sxs-lookup"><span data-stu-id="1de42-121">Create automatic posting workflows for expense reports.</span></span>        |
|       <span data-ttu-id="1de42-122"><strong>Gider satırı öğesi</strong></span><span class="sxs-lookup"><span data-stu-id="1de42-122"><strong>Expense line item</strong></span></span>        |     <span data-ttu-id="1de42-123">Gider raporları üzerinde satır maddeleri için onay iş akışları oluşturun.</span><span class="sxs-lookup"><span data-stu-id="1de42-123">Create approval workflows for line items on expense reports.</span></span>      |
| <span data-ttu-id="1de42-124"><strong>Gider satırı öğesi otomatik olarak deftere nakletme</strong></span><span class="sxs-lookup"><span data-stu-id="1de42-124"><strong>Expense line item auto posting</strong></span></span> | <span data-ttu-id="1de42-125">Gider raporları üzerinde satır maddeleri için otomatik deftere nakil iş akışları oluşturun.</span><span class="sxs-lookup"><span data-stu-id="1de42-125">Create automatic posting workflows for line items on expense reports.</span></span> |
|       <span data-ttu-id="1de42-126"><strong>Seyahat talebi</strong></span><span class="sxs-lookup"><span data-stu-id="1de42-126"><strong>Travel requisition</strong></span></span>       |          <span data-ttu-id="1de42-127">Seyahat talepleri için onay iş akışları oluşturun.</span><span class="sxs-lookup"><span data-stu-id="1de42-127">Create approval workflows for travel requisitions.</span></span>           |
|      <span data-ttu-id="1de42-128"><strong>Nakit avans isteği</strong></span><span class="sxs-lookup"><span data-stu-id="1de42-128"><strong>Cash advance request</strong></span></span>      |         <span data-ttu-id="1de42-129">Nakit avans talepleri için onay iş akışları oluşturun.</span><span class="sxs-lookup"><span data-stu-id="1de42-129">Create approval workflows for cash advance requests.</span></span>          |
|        <span data-ttu-id="1de42-130"><strong>KDV vergisinden düşme</strong></span><span class="sxs-lookup"><span data-stu-id="1de42-130"><strong>VAT tax recovery</strong></span></span>        | <span data-ttu-id="1de42-131">Katma değer vergisi (KDV) düşürme için onay iş akışları oluşturun.</span><span class="sxs-lookup"><span data-stu-id="1de42-131">Create approval workflows for the recovery of value-added tax (VAT).</span></span>  |

