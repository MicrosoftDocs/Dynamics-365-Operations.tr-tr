---
title: İş akışı geçmişini görüntüleme
description: Bu konuda işlenmesi ve onaylanması için iş akışı sistemine gönderilen bir belgenin durumunu görüntüleme adımları açıklanmaktadır.
author: jasongre
manager: AnnBe
ms.date: 07/09/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WorkflowStatus
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 16c6594161f1fecd36183a6b8f2c798f52d70a9c
ms.sourcegitcommit: 81e6eaa2178fda7f7d086ad978f4c891bc4ec10a
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/10/2019
ms.locfileid: "1738800"
---
# <a name="view-workflow-history"></a><span data-ttu-id="bb3dd-103">İş akışı geçmişini görüntüleme</span><span class="sxs-lookup"><span data-stu-id="bb3dd-103">View workflow history</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="bb3dd-104">Bu konuda işlenmesi ve onaylanması için iş akışı sistemine gönderilen bir belgenin durumunu görüntüleme adımları açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="bb3dd-104">This topic describes the steps to view the status of a document that was submitted to the workflow system for processing and approval.</span></span> <span data-ttu-id="bb3dd-105">Bu yöntemi oluşturmak için kullanılan demo veri şirketi USMF'dir.</span><span class="sxs-lookup"><span data-stu-id="bb3dd-105">The demo data company used to create this procedure is USMF.</span></span>

1. <span data-ttu-id="bb3dd-106">**Gezinti bölmesi > Modüller > Ortak > Sorgular > İş akışı > İş akışı geçmişi**'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="bb3dd-106">Go to **Navigation pane > Modules > Common > Inquiries > Workflow > Workflow history**.</span></span>
    - <span data-ttu-id="bb3dd-107">İşlenmek ve onaylanmak üzere iş akışı sistemine gönderilen bir belgenin durumunu görüntülemek için bu formu kullanın.</span><span class="sxs-lookup"><span data-stu-id="bb3dd-107">Use this form to view the status of a document that was submitted to the workflow system for processing and approval.</span></span>  
    - <span data-ttu-id="bb3dd-108">**Örnek Kodu** belgeyi işleyen veya işlemiş olan iş akışı örneğinin kimlik kodudur.</span><span class="sxs-lookup"><span data-stu-id="bb3dd-108">The **Instance ID** is the identification code of the workflow instance that is processing, or has processed the document.</span></span>  
    - <span data-ttu-id="bb3dd-109">**Durum**, belgenin iş akışı durumudur.</span><span class="sxs-lookup"><span data-stu-id="bb3dd-109">The **Status** is the workflow status of the document.</span></span>  
    - <span data-ttu-id="bb3dd-110">**İş Akışı Kodu**, belgeyi işleyen veya işlemiş olan iş akışının kimlik kodudur.</span><span class="sxs-lookup"><span data-stu-id="bb3dd-110">The **Workflow ID** is the identification code of the workflow that is processing, or has processed the document.</span></span>  
    - <span data-ttu-id="bb3dd-111">**Belge**, belgenin kimlik kodudur.</span><span class="sxs-lookup"><span data-stu-id="bb3dd-111">The **Document** is the identification code of the document.</span></span>  
    - <span data-ttu-id="bb3dd-112">**Belge türü**, işlenmek üzere gönderilen belgenin türüdür.</span><span class="sxs-lookup"><span data-stu-id="bb3dd-112">The **Document type** is the type of document that was submitted for processing.</span></span>  
    - <span data-ttu-id="bb3dd-113">**İş akışı**, belgeyi işleyen veya işlemiş olan iş akışının adıdır.</span><span class="sxs-lookup"><span data-stu-id="bb3dd-113">The **Workflow** is the name of the workflow that is processing, or has processed the document.</span></span>  
    - <span data-ttu-id="bb3dd-114">**Sürüm**, belgeyi işleyen veya işlemiş olan iş akışının sürüm numarasıdır.</span><span class="sxs-lookup"><span data-stu-id="bb3dd-114">The **Version** is the version number of the workflow that is processing, or has processed the document.</span></span>  
    - <span data-ttu-id="bb3dd-115">**Oluşturulma tarihi ve saati**, belgenin gönderildiği tarih ve saattir.</span><span class="sxs-lookup"><span data-stu-id="bb3dd-115">The **Created date and time** is the date and time that the document was submitted.</span></span>  
    - <span data-ttu-id="bb3dd-116">**Geçen süre**, belgenin gönderilmesinden itibaren geçen süredir.</span><span class="sxs-lookup"><span data-stu-id="bb3dd-116">The **Elapsed time** is the time that has passed since the document was submitted.</span></span>  
    - <span data-ttu-id="bb3dd-117">**Sürdür** düğmesi, seçili belge için iş akışı işlemini devam ettirmenizi sağlar.</span><span class="sxs-lookup"><span data-stu-id="bb3dd-117">The **Resume** button allows you to resume the workflow process for the selected document.</span></span>  
    - <span data-ttu-id="bb3dd-118">**Geri çağır** düğmesi, seçili belgenin işlenmemesi için belgeyi geri çağırmanızı sağlar.</span><span class="sxs-lookup"><span data-stu-id="bb3dd-118">The **Recall** button allows you to recall the selected document so that it is not processed.</span></span>   
2. <span data-ttu-id="bb3dd-119">Listede, istenen satırdaki bağlantıyı seçin.</span><span class="sxs-lookup"><span data-stu-id="bb3dd-119">In the list, select the link in the desired row.</span></span>
    - <span data-ttu-id="bb3dd-120">**İş maddeleri** bölümünün genişletildiğinden emin olun.</span><span class="sxs-lookup"><span data-stu-id="bb3dd-120">Make sure the **Work items** section is expanded.</span></span> <span data-ttu-id="bb3dd-121">Bu bölümde, seçili belge ile ilişkili iş maddelerini görüntüleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="bb3dd-121">In this section you can view the work items that are associated with the selected document.</span></span> <span data-ttu-id="bb3dd-122">Örneğin, bir görevin tamamlanması veya belgenin onaylanması gerekiyor olabilir.</span><span class="sxs-lookup"><span data-stu-id="bb3dd-122">For example, a task may have to be completed, or the document may have to be approved.</span></span>  
    - <span data-ttu-id="bb3dd-123">**Yeniden Ata** düğmesi, bir iş maddesini başka bir kullanıcıya yeniden atayabileceğiniz bir iletişim kutusu açar.</span><span class="sxs-lookup"><span data-stu-id="bb3dd-123">The **Reassign** button will open a dialog box where you can reassign a work item to another user.</span></span>  
    - <span data-ttu-id="bb3dd-124">**İzleme ayrıntıları** bölümünün genişletildiğinden emin olun.</span><span class="sxs-lookup"><span data-stu-id="bb3dd-124">Make sure the **Tracking details** section is expanded.</span></span> <span data-ttu-id="bb3dd-125">Bu bölümde, seçili belgenin iş akışı geçmişini görüntüleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="bb3dd-125">In this section you can view the workflow history of the selected document.</span></span>  

