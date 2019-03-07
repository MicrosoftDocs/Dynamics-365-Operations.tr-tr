---
title: İş akışındaki iş öğelerini devretme
description: Bir süreliğine ofis dışında olacaksanız ya da iş öğeleri ile ilgili uygulama yapamayacaksanız iş öğelerinizi diğer kullanıcılara devredebilir veya yeniden atayabilirsiniz.
author: jasongre
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysUserSetup, WorkflowDelegationUserListLookup
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f85a1318822ceaf829134bf2eb3581e350d5bea4
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2019
ms.locfileid: "346261"
---
# <a name="delegate-work-items-in-a-workflow"></a><span data-ttu-id="a9631-103">İş akışındaki iş öğelerini devretme</span><span class="sxs-lookup"><span data-stu-id="a9631-103">Delegate work items in a workflow</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="a9631-104">Bir süreliğine ofis dışında olacaksanız ya da iş öğeleri ile ilgili uygulama yapamayacaksanız iş öğelerinizi diğer kullanıcılara devredebilir veya yeniden atayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="a9631-104">If you plan to be out of the office or otherwise unavailable to act on work items, you can delegate, or reassign, your work items to other users.</span></span> <span data-ttu-id="a9631-105">Bu yordam, iş öğelerinizi otomatik olarak bir başka kullanıcıya devretmeniz için sistemi yapılandırmanıza yardımcı olur.</span><span class="sxs-lookup"><span data-stu-id="a9631-105">This procedure helps you configure the system to automatically delegate your work items to another user.</span></span>



<span data-ttu-id="a9631-106">Bu yöntemi oluşturmak için kullanılan demo veri şirketi USMF'dir.</span><span class="sxs-lookup"><span data-stu-id="a9631-106">The demo data company used to create this procedure is USMF.</span></span>


## <a name="set-up-automatic-delegation"></a><span data-ttu-id="a9631-107">Otomatik temsil ayarlama</span><span class="sxs-lookup"><span data-stu-id="a9631-107">Set up automatic delegation</span></span>
1. <span data-ttu-id="a9631-108">Ortak > Kurulum > Kullanıcı seçenekleri'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="a9631-108">Go to Common > Setup > User options.</span></span>
2. <span data-ttu-id="a9631-109">İş Akışı sekmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="a9631-109">Click the Workflow tab.</span></span>
    * <span data-ttu-id="a9631-110">Temsilci bölümünün genişletilmiş olduğundan emin olun.</span><span class="sxs-lookup"><span data-stu-id="a9631-110">Make sure the Delegation section is expanded.</span></span>    <span data-ttu-id="a9631-111">Diğer kullanıcılar iş maddelerinize otomatik olarak temsilci olarak atanacak biçimde sistemi yapılandırmak için, hangi iş maddesi türlerine ne zaman temsilci atanacağını belirten temsilci kuralları oluşturmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="a9631-111">To configure the system to automatically delegate your work items to other users, you must create delegation rules, which specify when certain types of work items are delegated.</span></span> <span data-ttu-id="a9631-112">Temsilci kuralı oluşturmak için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="a9631-112">Follow these steps to create a delegation rule.</span></span>  
3. <span data-ttu-id="a9631-113">Ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="a9631-113">Click Add.</span></span>
4. <span data-ttu-id="a9631-114">Kapsam alanında, bir seçenek belirleyin.</span><span class="sxs-lookup"><span data-stu-id="a9631-114">In the Scope field, select an option.</span></span>
    * <span data-ttu-id="a9631-115">Tümü: Size atanmış olan tüm iş maddelerine temsilci seçin.</span><span class="sxs-lookup"><span data-stu-id="a9631-115">All – Delegate all work items that are assigned to you.</span></span>    <span data-ttu-id="a9631-116">Modül: Yalnızca belirli bir iş akışı türüyle ilişkili iş maddelerine temsilci atayın.</span><span class="sxs-lookup"><span data-stu-id="a9631-116">Module – Delegate only the work items that are related to a specific type of workflow.</span></span> <span data-ttu-id="a9631-117">Bu seçeneği belirlerseniz Ad alanında iş akışı türünü seçmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="a9631-117">If you select this option, you must select the type of workflow in the Name field.</span></span>    <span data-ttu-id="a9631-118">İş akışı: Yalnızca belirli bir iş akışıyla ilişkili iş maddelerine temsilci atayın.</span><span class="sxs-lookup"><span data-stu-id="a9631-118">Workflow – Delegate only the work items that are related to a specific workflow.</span></span> <span data-ttu-id="a9631-119">Bu seçeneği belirlerseniz Ad alanında iş akışını seçmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="a9631-119">If you select this option, you must select the workflow in the Name field.</span></span>  
5. <span data-ttu-id="a9631-120">Temsilci alanında, iş maddelerine temsilci olarak atanacak kullanıcıyı seçin.</span><span class="sxs-lookup"><span data-stu-id="a9631-120">In the Delegate field, select the user to delegate the work items to.</span></span>
    * <span data-ttu-id="a9631-121">İş maddelerine ne zaman otomatik olarak temsilci atanmasını istediğinizi belirtmek için Başlangıç tarihi/saati ve Bitiş tarihi/saati alanlarını kullanın.</span><span class="sxs-lookup"><span data-stu-id="a9631-121">Use the Start date/time and End date/time fields to specify when you want the work items to be automatically delegated.</span></span>  
6. <span data-ttu-id="a9631-122">Başlangıç tarihi/saati alanına tarih ve saati girin.</span><span class="sxs-lookup"><span data-stu-id="a9631-122">In the Start date/time field, enter a date and time.</span></span>
7. <span data-ttu-id="a9631-123">Bitiş tarihi/saati alanına tarih ve saati girin.</span><span class="sxs-lookup"><span data-stu-id="a9631-123">In the End date/time field, enter a date and time.</span></span>
8. <span data-ttu-id="a9631-124">Bu temsilci kuralını etkinleştirmek için Etkin onay kutusunu işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="a9631-124">Select the Enabled check box to activate the delegation rule.</span></span>
    * <span data-ttu-id="a9631-125">Kapsam olarak Modül'ü seçtiyseniz Ad alanında modülü seçmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="a9631-125">If you selected Module as the Scope, then you must select the module in the Name field.</span></span>    <span data-ttu-id="a9631-126">Kapsam olarak İş akışı'nı seçtiyseniz Ad alanında temsilci atamak üzere ilgili iş akışını seçmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="a9631-126">If you selected Workflow as the Scope, then you must select the specific workflow to delegate in the Name field.</span></span>  
9. <span data-ttu-id="a9631-127">Yorum alanına, iş maddelerine neden temsilci atadığınızı belirten bir yorum girin.</span><span class="sxs-lookup"><span data-stu-id="a9631-127">In the Comment field, enter a comment that explains why you are delegating the work items.</span></span>

