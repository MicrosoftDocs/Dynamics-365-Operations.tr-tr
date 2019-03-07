---
title: İş akışı geçmişini görüntüle
description: İşlenmesi ve onaylanması için iş akışı sistemine gönderilen bir belgenin durumunu görüntülemek için bu adımları kullanın.
author: jasongre
manager: AnnBe
ms.date: 08/29/2018
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
ms.openlocfilehash: a40fe377322e2d64b751f6cace3eda20736cd321
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2019
ms.locfileid: "309668"
---
# <a name="view-workflow-history"></a><span data-ttu-id="ef306-103">İş akışı geçmişini görüntüle</span><span class="sxs-lookup"><span data-stu-id="ef306-103">View workflow history</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="ef306-104">İşlenmesi ve onaylanması için iş akışı sistemine gönderilen bir belgenin durumunu görüntülemek için bu adımları kullanın.</span><span class="sxs-lookup"><span data-stu-id="ef306-104">Use these steps to view the status of a document that was submitted to the workflow system for processing and approval.</span></span> <span data-ttu-id="ef306-105">Bu yöntemi oluşturmak için kullanılan demo veri şirketi USMF'dir.</span><span class="sxs-lookup"><span data-stu-id="ef306-105">The demo data company used to create this procedure is USMF.</span></span>

1. <span data-ttu-id="ef306-106">Ortak > Sorgulamalar > İş akışı > İş akışı geçmişi'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="ef306-106">Go to Common > Inquiries > Workflow > Workflow history.</span></span>
    * <span data-ttu-id="ef306-107">İşlenmek ve onaylanmak üzere iş akışı sistemine gönderilen bir belgenin durumunu görüntülemek için bu formu kullanın.</span><span class="sxs-lookup"><span data-stu-id="ef306-107">Use this form to view the status of a document that was submitted to the workflow system for processing and approval.</span></span>  
    * <span data-ttu-id="ef306-108">Örnek kodu,      belgeyi işleyen veya işlemiş olan örneğin kimlik kodudur.</span><span class="sxs-lookup"><span data-stu-id="ef306-108">The Instance ID is      the identification code of the workflow instance that is processing, or has processed the document.</span></span>  
    * <span data-ttu-id="ef306-109">Durum, belgenin iş akışı durumudur.</span><span class="sxs-lookup"><span data-stu-id="ef306-109">The Status is the workflow status of the document.</span></span>  
    * <span data-ttu-id="ef306-110">İş akışı kodu, belgeyi işleyen veya işlemiş olan iş akışının kimlik kodudur.</span><span class="sxs-lookup"><span data-stu-id="ef306-110">The Workflow ID is the identification code of the workflow that is processing, or has processed the document.</span></span>  
    * <span data-ttu-id="ef306-111">Belge, belgenin kimlik saptama kodudur.</span><span class="sxs-lookup"><span data-stu-id="ef306-111">The Document is the identification code of the document.</span></span>  
    * <span data-ttu-id="ef306-112">Belge türü, işlenmek üzere gönderilen belgenin türüdür.</span><span class="sxs-lookup"><span data-stu-id="ef306-112">The Document type is the type of document that was submitted for processing.</span></span>  
    * <span data-ttu-id="ef306-113">İş akışı, belgeyi işleyen veya işlemiş olan iş akışının adıdır.</span><span class="sxs-lookup"><span data-stu-id="ef306-113">The Workflow is the name of the workflow that is processing, or has processed the document.</span></span>  
    * <span data-ttu-id="ef306-114">Sürüm, belgeyi işleyen veya işlemiş olan iş akışının sürüm numarasıdır.</span><span class="sxs-lookup"><span data-stu-id="ef306-114">The Version is the version number of the workflow that is processing, or has processed the document.</span></span>  
    * <span data-ttu-id="ef306-115">Oluşturulma tarihi ve saati, belgenin gönderildiği tarih ve saattir.</span><span class="sxs-lookup"><span data-stu-id="ef306-115">The Created date and time is the date and time that the document was submitted.</span></span>  
    * <span data-ttu-id="ef306-116">Geçen süre, belgenin gönderilmesinden itibaren geçen süredir.</span><span class="sxs-lookup"><span data-stu-id="ef306-116">The Elapsed time is the time that has passed since the document was submitted.</span></span>  
    * <span data-ttu-id="ef306-117">Sürdür düğmesi, seçili belge için iş akışı işleminin devam ettirmenizi sağlar.</span><span class="sxs-lookup"><span data-stu-id="ef306-117">The Resume button allows you to resume the workflow process for the selected document.</span></span>  
    * <span data-ttu-id="ef306-118">Geri çağır düğmesi, seçili belgenin işlenmemesi için belgeyi geri çağırmanızı sağlar.</span><span class="sxs-lookup"><span data-stu-id="ef306-118">The Recall button allows you to recall the selected document so that it is not processed.</span></span>   
2. <span data-ttu-id="ef306-119">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ef306-119">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="ef306-120">İş maddeleri bölümünün genişletilmiş olduğundan emin olun.</span><span class="sxs-lookup"><span data-stu-id="ef306-120">Make sure the Work items section is expanded.</span></span>    <span data-ttu-id="ef306-121">Bu bölümde, seçili belge ile ilişkili iş maddelerini görüntüleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="ef306-121">In this section you can view the work items that are associated with the selected document.</span></span> <span data-ttu-id="ef306-122">Örneğin, bir görevin tamamlanması veya belgenin onaylanması gerekiyor olabilir.</span><span class="sxs-lookup"><span data-stu-id="ef306-122">For example, a task may have to be completed, or the document may have to be approved.</span></span>  
    * <span data-ttu-id="ef306-123">Yeniden Ata düğmesi, bir iş maddesini başka bir kullanıcıya yeniden atayabileceğiniz bir iletişim kutusu açar.</span><span class="sxs-lookup"><span data-stu-id="ef306-123">The Reassign button will open a dialog box where you can reassign a work item to another user.</span></span>  
    * <span data-ttu-id="ef306-124">İzleme ayrıntıları bölümünün genişletilmiş olduğundan emin olun.</span><span class="sxs-lookup"><span data-stu-id="ef306-124">Make sure the Tracking details section is expanded.</span></span>    <span data-ttu-id="ef306-125">Bu bölümde, seçili belgenin iş akışı geçmişini görüntüleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="ef306-125">In this section you can view the workflow history of the selected document.</span></span>  

