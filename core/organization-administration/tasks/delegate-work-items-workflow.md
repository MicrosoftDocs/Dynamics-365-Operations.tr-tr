--- 
title: "İş akışındaki iş öğelerini devretme"
description: "Bir süreliğine ofis dışında olacaksanız ya da iş öğeleri ile ilgili uygulama yapamayacaksanız iş öğelerinizi diğer kullanıcılara devredebilir veya yeniden atayabilirsiniz."
author: jasongre
manager: AnnBe
ms.date: 02/21/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: sericks
ms.search.scope: Operations
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 6483307ff89ce79a3ef16bb763e3124ac537a5d8
ms.contentlocale: tr-tr
ms.lasthandoff: 08/29/2017

---
# <a name="delegate-work-items-in-a-workflow"></a><span data-ttu-id="c6c75-103">İş akışındaki iş öğelerini devretme</span><span class="sxs-lookup"><span data-stu-id="c6c75-103">Delegate work items in a workflow</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="c6c75-104">Bir süreliğine ofis dışında olacaksanız ya da iş öğeleri ile ilgili uygulama yapamayacaksanız iş öğelerinizi diğer kullanıcılara devredebilir veya yeniden atayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="c6c75-104">If you plan to be out of the office or otherwise unavailable to act on work items, you can delegate, or reassign, your work items to other users.</span></span> <span data-ttu-id="c6c75-105">Bu yordam, iş öğelerinizi otomatik olarak bir başka kullanıcıya devretmeniz için sistemi yapılandırmanıza yardımcı olur.</span><span class="sxs-lookup"><span data-stu-id="c6c75-105">This procedure helps you configure the system to automatically delegate your work items to another user.</span></span>



<span data-ttu-id="c6c75-106">Bu yöntemi oluşturmak için kullanılan demo veri şirketi USMF'dir.</span><span class="sxs-lookup"><span data-stu-id="c6c75-106">The demo data company used to create this procedure is USMF.</span></span>


## <a name="set-up-automatic-delegation"></a><span data-ttu-id="c6c75-107">Otomatik temsil ayarlama</span><span class="sxs-lookup"><span data-stu-id="c6c75-107">Set up automatic delegation</span></span>
1. <span data-ttu-id="c6c75-108">Ortak > Kurulum > Kullanıcı seçenekleri'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="c6c75-108">Go to Common > Setup > User options.</span></span>
2. <span data-ttu-id="c6c75-109">İş Akışı sekmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="c6c75-109">Click the Workflow tab.</span></span>
    * <span data-ttu-id="c6c75-110">Temsilci bölümünün genişletilmiş olduğundan emin olun.</span><span class="sxs-lookup"><span data-stu-id="c6c75-110">Make sure the Delegation section is expanded.</span></span>    <span data-ttu-id="c6c75-111">Diğer kullanıcılar iş maddelerinize otomatik olarak temsilci olarak atanacak biçimde sistemi yapılandırmak için, hangi iş maddesi türlerine ne zaman temsilci atanacağını belirten temsilci kuralları oluşturmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="c6c75-111">To configure the system to automatically delegate your work items to other users, you must create delegation rules, which specify when certain types of work items are delegated.</span></span> <span data-ttu-id="c6c75-112">Temsilci kuralı oluşturmak için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="c6c75-112">Follow these steps to create a delegation rule.</span></span>  
3. <span data-ttu-id="c6c75-113">Ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="c6c75-113">Click Add.</span></span>
4. <span data-ttu-id="c6c75-114">Kapsam alanında, bir seçenek belirleyin.</span><span class="sxs-lookup"><span data-stu-id="c6c75-114">In the Scope field, select an option.</span></span>
    * <span data-ttu-id="c6c75-115">Tümü: Size atanmış olan tüm iş maddelerine temsilci seçin.</span><span class="sxs-lookup"><span data-stu-id="c6c75-115">All – Delegate all work items that are assigned to you.</span></span>    <span data-ttu-id="c6c75-116">Modül: Yalnızca belirli bir iş akışı türüyle ilişkili iş maddelerine temsilci atayın.</span><span class="sxs-lookup"><span data-stu-id="c6c75-116">Module – Delegate only the work items that are related to a specific type of workflow.</span></span> <span data-ttu-id="c6c75-117">Bu seçeneği belirlerseniz Ad alanında iş akışı türünü seçmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="c6c75-117">If you select this option, you must select the type of workflow in the Name field.</span></span>    <span data-ttu-id="c6c75-118">İş akışı: Yalnızca belirli bir iş akışıyla ilişkili iş maddelerine temsilci atayın.</span><span class="sxs-lookup"><span data-stu-id="c6c75-118">Workflow – Delegate only the work items that are related to a specific workflow.</span></span> <span data-ttu-id="c6c75-119">Bu seçeneği belirlerseniz Ad alanında iş akışını seçmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="c6c75-119">If you select this option, you must select the workflow in the Name field.</span></span>  
5. <span data-ttu-id="c6c75-120">Temsilci alanında, iş maddelerine temsilci olarak atanacak kullanıcıyı seçin.</span><span class="sxs-lookup"><span data-stu-id="c6c75-120">In the Delegate field, select the user to delegate the work items to.</span></span>
    * <span data-ttu-id="c6c75-121">İş maddelerine ne zaman otomatik olarak temsilci atanmasını istediğinizi belirtmek için Başlangıç tarihi/saati ve Bitiş tarihi/saati alanlarını kullanın.</span><span class="sxs-lookup"><span data-stu-id="c6c75-121">Use the Start date/time and End date/time fields to specify when you want the work items to be automatically delegated.</span></span>  
6. <span data-ttu-id="c6c75-122">Başlangıç tarihi/saati alanına tarih ve saati girin.</span><span class="sxs-lookup"><span data-stu-id="c6c75-122">In the Start date/time field, enter a date and time.</span></span>
7. <span data-ttu-id="c6c75-123">Bitiş tarihi/saati alanına tarih ve saati girin.</span><span class="sxs-lookup"><span data-stu-id="c6c75-123">In the End date/time field, enter a date and time.</span></span>
8. <span data-ttu-id="c6c75-124">Bu temsilci kuralını etkinleştirmek için Etkin onay kutusunu işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="c6c75-124">Select the Enabled check box to activate the delegation rule.</span></span>
    * <span data-ttu-id="c6c75-125">Kapsam olarak Modül'ü seçtiyseniz Ad alanında modülü seçmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="c6c75-125">If you selected Module as the Scope, then you must select the module in the Name field.</span></span>    <span data-ttu-id="c6c75-126">Kapsam olarak İş akışı'nı seçtiyseniz Ad alanında temsilci atamak üzere ilgili iş akışını seçmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="c6c75-126">If you selected Workflow as the Scope, then you must select the specific workflow to delegate in the Name field.</span></span>  
9. <span data-ttu-id="c6c75-127">Yorum alanına, iş maddelerine neden temsilci atadığınızı belirten bir yorum girin.</span><span class="sxs-lookup"><span data-stu-id="c6c75-127">In the Comment field, enter a comment that explains why you are delegating the work items.</span></span>


