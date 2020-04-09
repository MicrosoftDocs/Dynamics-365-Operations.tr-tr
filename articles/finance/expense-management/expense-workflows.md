---
title: Gider yönetimi için iş akışları ayarlama
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
ms.openlocfilehash: cdd4d69cb86da12e4a265f89c021c238d00cad08
ms.sourcegitcommit: de5af1912201dd70aa85fdcad0b184c42405802e
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/21/2020
ms.locfileid: "3154006"
---
# <a name="set-up-workflows-for-expense-management"></a><span data-ttu-id="ba025-103">Gider yönetimi için iş akışları ayarlama</span><span class="sxs-lookup"><span data-stu-id="ba025-103">Set up workflows for Expense management</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ba025-104">Seyahat ve gider belgelerini gözden geçirmek ve onaylamakta kullanılan iş akışı işlemlerini ayarlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="ba025-104">You can set up a workflow process that is used to review and approve travel and expense documents.</span></span> <span data-ttu-id="ba025-105">iş akışlarının tanımlandığı belgeler gider raporları, seyahat talepleri ve nakit avans taleplerini içerebilir.</span><span class="sxs-lookup"><span data-stu-id="ba025-105">The documents for which workflows can be defined include expense reports, travel requisitions, and cash advance requests.</span></span>

<span data-ttu-id="ba025-106">İş akışı, bir iş sürecini temsil eder.</span><span class="sxs-lookup"><span data-stu-id="ba025-106">A workflow represents a business process.</span></span> <span data-ttu-id="ba025-107">Bir belgenin sistem üzerinde nasıl aktığını tanımlar ve bir görevi kimin tamamlaması veya bir belgeyi kimin onaylaması gerektiğini tanımlar.</span><span class="sxs-lookup"><span data-stu-id="ba025-107">It defines how a document flows through the system and indicates who must complete a task or approve a document.</span></span> <span data-ttu-id="ba025-108">İş akışı sistemini kuruluşunuzda kullanmanın bazı getirileri vardır:</span><span class="sxs-lookup"><span data-stu-id="ba025-108">There are several benefits of using the workflow system in your organization:</span></span>

-   <span data-ttu-id="ba025-109">**Tutarlı süreçler** — Satınalma talepleri ve gider raporları gibi belirli belgelerin onay sürecini tanımlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="ba025-109">**Consistent processes** — You can define the approval process for specific documents, such as purchase requisitions and expense reports.</span></span> <span data-ttu-id="ba025-110">İş akışı sistemini kullanmak, belgelerin tutarlı ve verimli şekilde işlenmesine ve onaylanmasına yardımcı olur.</span><span class="sxs-lookup"><span data-stu-id="ba025-110">Using the workflow system helps to ensure that documents are processed and approved in a consistent and efficient manner.</span></span>

-   <span data-ttu-id="ba025-111">Süreç görünürlüğü — Belirli bir iş akışı örneğinin durumunu, geçmişini ve performans ölçülerini takip edebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="ba025-111">Process visibility — You can track the status, history, and performance metrics of a specific workflow instance.</span></span> <span data-ttu-id="ba025-112">Bu da iş akışının verimliliği yükseltmesi için değişiklikler yapılması gerekli olup olmadığını belirlemenize yardımcı olur.</span><span class="sxs-lookup"><span data-stu-id="ba025-112">This helps you determine whether changes should be made to the workflow to improve efficiency.</span></span>

-   <span data-ttu-id="ba025-113">Merkezi çalışma listesi — Kullanıcılar, iş akışı görevlerini ve kendilerine atanmış onayları görmek için merkezi bir çalışma listesini görüntüleyebilir.</span><span class="sxs-lookup"><span data-stu-id="ba025-113">Centralized work list — Users can view a centralized work list to view the workflow tasks and approvals assigned to them.</span></span> 

<span data-ttu-id="ba025-114">**Oluşturabileceğiniz iş akışı türleri**</span><span class="sxs-lookup"><span data-stu-id="ba025-114">**The types of workflows you can create**</span></span>

<span data-ttu-id="ba025-115">Aşağıdaki tablo **Gider** içerisinde oluşturabileceğiniz iş akışı türlerini listeler.</span><span class="sxs-lookup"><span data-stu-id="ba025-115">The following table lists the types of workflows that you can create in **Expense**.</span></span>


|              <span data-ttu-id="ba025-116"><strong>Tip</strong></span><span class="sxs-lookup"><span data-stu-id="ba025-116"><strong>Type</strong></span></span>              |                   <span data-ttu-id="ba025-117"><strong>Bu türü aşağıdakileri gerçekleştirmek için kullanın:</strong></span><span class="sxs-lookup"><span data-stu-id="ba025-117"><strong>Use this type to</strong></span></span>                   |
|-------------------------------------------------|-----------------------------------------------------------------------|
|         <span data-ttu-id="ba025-118"><strong>Gider raporu</strong></span><span class="sxs-lookup"><span data-stu-id="ba025-118"><strong>Expense report</strong></span></span>         |            <span data-ttu-id="ba025-119">Gider raporları için onay iş akışları oluşturun.</span><span class="sxs-lookup"><span data-stu-id="ba025-119">Create approval workflows for expense reports.</span></span>             |
|  <span data-ttu-id="ba025-120"><strong>Gider raporu otomatik olarak deftere nakletme</strong></span><span class="sxs-lookup"><span data-stu-id="ba025-120"><strong>Expense report auto posting</strong></span></span>   |        <span data-ttu-id="ba025-121">Gider raporları için belge otomatik deftere nakil iş akışları oluşturun.</span><span class="sxs-lookup"><span data-stu-id="ba025-121">Create automatic posting workflows for expense reports.</span></span>        |
|       <span data-ttu-id="ba025-122"><strong>Gider satırı öğesi</strong></span><span class="sxs-lookup"><span data-stu-id="ba025-122"><strong>Expense line item</strong></span></span>        |     <span data-ttu-id="ba025-123">Gider raporları üzerinde satır maddeleri için onay iş akışları oluşturun.</span><span class="sxs-lookup"><span data-stu-id="ba025-123">Create approval workflows for line items on expense reports.</span></span>      |
| <span data-ttu-id="ba025-124"><strong>Gider satırı öğesi otomatik olarak deftere nakletme</strong></span><span class="sxs-lookup"><span data-stu-id="ba025-124"><strong>Expense line item auto posting</strong></span></span> | <span data-ttu-id="ba025-125">Gider raporları üzerinde satır maddeleri için otomatik deftere nakil iş akışları oluşturun.</span><span class="sxs-lookup"><span data-stu-id="ba025-125">Create automatic posting workflows for line items on expense reports.</span></span> |
|       <span data-ttu-id="ba025-126"><strong>Seyahat talebi</strong></span><span class="sxs-lookup"><span data-stu-id="ba025-126"><strong>Travel requisition</strong></span></span>       |          <span data-ttu-id="ba025-127">Seyahat talepleri için onay iş akışları oluşturun.</span><span class="sxs-lookup"><span data-stu-id="ba025-127">Create approval workflows for travel requisitions.</span></span>           |
|      <span data-ttu-id="ba025-128"><strong>Nakit avans isteği</strong></span><span class="sxs-lookup"><span data-stu-id="ba025-128"><strong>Cash advance request</strong></span></span>      |         <span data-ttu-id="ba025-129">Nakit avans talepleri için onay iş akışları oluşturun.</span><span class="sxs-lookup"><span data-stu-id="ba025-129">Create approval workflows for cash advance requests.</span></span>          |
|        <span data-ttu-id="ba025-130"><strong>KDV vergisinden düşme</strong></span><span class="sxs-lookup"><span data-stu-id="ba025-130"><strong>VAT tax recovery</strong></span></span>        | <span data-ttu-id="ba025-131">Katma değer vergisi (KDV) düşürme için onay iş akışları oluşturun.</span><span class="sxs-lookup"><span data-stu-id="ba025-131">Create approval workflows for the recovery of value-added tax (VAT).</span></span>  |

