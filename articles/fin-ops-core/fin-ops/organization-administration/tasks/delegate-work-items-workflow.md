---
title: İş akışındaki iş öğelerini devretme
description: Bir süreliğine ofis dışında olacaksanız ya da iş öğeleri ile ilgili uygulama yapamayacaksanız iş öğelerinizi diğer kullanıcılara devredebilir veya yeniden atayabilirsiniz.
author: jasongre
manager: AnnBe
ms.date: 07/01/2019
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
ms.openlocfilehash: 44dc747543e32b54729d12c89a401b0187e25a61
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/27/2019
ms.locfileid: "2189971"
---
# <a name="delegate-work-items-in-a-workflow"></a><span data-ttu-id="ee24b-103">İş akışındaki iş öğelerini devretme</span><span class="sxs-lookup"><span data-stu-id="ee24b-103">Delegate work items in a workflow</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

## <a name="manually-delegate-a-work-item"></a><span data-ttu-id="ee24b-104">Bir iş öğesini el ile devredin</span><span class="sxs-lookup"><span data-stu-id="ee24b-104">Manually delegate a work item</span></span>

<span data-ttu-id="ee24b-105">Bir tekil iş öğesini devretmek için **Devret** seçeneğini **İş akışı** menüsünde seçin ve daha sonra devredilecek kullanıcıyı bir yorum ile seçin.</span><span class="sxs-lookup"><span data-stu-id="ee24b-105">To delegate an individual work item, select the **Delegate** option in the **Workflow** menu and then enter the user to be delegated to along with a comment.</span></span> <span data-ttu-id="ee24b-106">Bu, iş öğesini tamamlayabilmeleri için bu kullanıcıya yeniden atayacaktır.</span><span class="sxs-lookup"><span data-stu-id="ee24b-106">This will reassign the work item to that user so they can complete it.</span></span>

## <a name="automatically-delegate-work-items"></a><span data-ttu-id="ee24b-107">Otomatik olarak iş öğelerini devret</span><span class="sxs-lookup"><span data-stu-id="ee24b-107">Automatically delegate work items</span></span>

<span data-ttu-id="ee24b-108">Bir süreliğine ofis dışında olmayı veya başka sebeple iş öğeleri üzerinde çalışamamayı planlıyorsanız, yeni iş öğelerini diğer kullanıcılara **Kullanıcı seçenekleri** sayfasını kullanarak otomatik olarak devredebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="ee24b-108">If you plan to be out of the office or otherwise unavailable to act on work items for a period of time, you can automatically delegate new work items to other users using the **User options** page.</span></span>

### <a name="set-up-automatic-delegation"></a><span data-ttu-id="ee24b-109">Otomatik temsil ayarlama</span><span class="sxs-lookup"><span data-stu-id="ee24b-109">Set up automatic delegation</span></span>
1. <span data-ttu-id="ee24b-110">**Ortak > Kurulum > Kullanıcı** seçenekleri'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="ee24b-110">Go to **Common > Setup > User options**.</span></span>
2. <span data-ttu-id="ee24b-111">**İş akışı** sekmesine tıklayın. Temsilci bölümünün genişletilmiş olduğundan emin olun.</span><span class="sxs-lookup"><span data-stu-id="ee24b-111">Click the **Workflow** tab. Make sure the Delegation section is expanded.</span></span> <span data-ttu-id="ee24b-112">Diğer kullanıcılar iş maddelerinize otomatik olarak temsilci olarak atanacak biçimde sistemi yapılandırmak için, hangi iş maddesi türlerine ne zaman temsilci atanacağını belirten temsilci kuralları oluşturmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="ee24b-112">To configure the system to automatically delegate your work items to other users, you must create delegation rules, which specify when certain types of work items are delegated.</span></span> <span data-ttu-id="ee24b-113">Temsilci kuralı oluşturmak için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="ee24b-113">Follow these steps to create a delegation rule.</span></span>  
3. <span data-ttu-id="ee24b-114">**Ekle** öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ee24b-114">Click **Add**.</span></span>
4. <span data-ttu-id="ee24b-115">**Kapsam** alanında, bir seçenek belirleyin.</span><span class="sxs-lookup"><span data-stu-id="ee24b-115">In the **Scope** field, select an option.</span></span>
    - <span data-ttu-id="ee24b-116">Tümü: Size atanmış olan tüm iş maddelerine temsilci seçin.</span><span class="sxs-lookup"><span data-stu-id="ee24b-116">All – Delegate all work items that are assigned to you.</span></span>
    - <span data-ttu-id="ee24b-117">Modül: Yalnızca belirli bir iş akışı türüyle ilişkili iş maddelerine temsilci atayın.</span><span class="sxs-lookup"><span data-stu-id="ee24b-117">Module – Delegate only the work items that are related to a specific type of workflow.</span></span> <span data-ttu-id="ee24b-118">Bu seçeneği belirlerseniz Ad alanında iş akışı türünü seçmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="ee24b-118">If you select this option, you must select the type of workflow in the Name field.</span></span>
    - <span data-ttu-id="ee24b-119">İş akışı: Yalnızca belirli bir iş akışıyla ilişkili iş maddelerine temsilci atayın.</span><span class="sxs-lookup"><span data-stu-id="ee24b-119">Workflow – Delegate only the work items that are related to a specific workflow.</span></span> <span data-ttu-id="ee24b-120">Bu seçeneği belirlerseniz Ad alanında iş akışını seçmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="ee24b-120">If you select this option, you must select the workflow in the Name field.</span></span>  
5. <span data-ttu-id="ee24b-121">**Temsilci** alanında, iş maddelerine temsilci olarak atanacak kullanıcıyı seçin.</span><span class="sxs-lookup"><span data-stu-id="ee24b-121">In the **Delegate** field, select the user to delegate the work items to.</span></span> <span data-ttu-id="ee24b-122">İş maddelerine ne zaman otomatik olarak temsilci atanmasını istediğinizi belirtmek için Başlangıç tarihi/saati ve Bitiş tarihi/saati alanlarını kullanın.</span><span class="sxs-lookup"><span data-stu-id="ee24b-122">Use the Start date/time and End date/time fields to specify when you want the work items to be automatically delegated.</span></span>  
6. <span data-ttu-id="ee24b-123">**Başlangıç tarihi/saati** alanına tarih ve saati girin.</span><span class="sxs-lookup"><span data-stu-id="ee24b-123">In the **Start date/time** field, enter a date and time.</span></span>
7. <span data-ttu-id="ee24b-124">**Bitiş tarihi/saati** alanına tarih ve saati girin.</span><span class="sxs-lookup"><span data-stu-id="ee24b-124">In the **End date/time** field, enter a date and time.</span></span>
8. <span data-ttu-id="ee24b-125">Bu temsilci kuralını etkinleştirmek için **Etkin** onay kutusunu işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="ee24b-125">Select the **Enabled** check box to activate the delegation rule.</span></span> <span data-ttu-id="ee24b-126">Kapsam olarak **Modül**'ü seçtiyseniz Ad alanında modülü seçmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="ee24b-126">If you selected **Module** as the Scope, then you must select the module in the Name field.</span></span> <span data-ttu-id="ee24b-127">Kapsam olarak **İş akışı**'nı seçtiyseniz Ad alanında temsilci atamak üzere ilgili iş akışını seçmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="ee24b-127">If you selected **Workflow** as the Scope, then you must select the specific workflow to delegate in the Name field.</span></span>  
9. <span data-ttu-id="ee24b-128">**Yorum** alanına, iş maddelerine neden temsilci atadığınızı belirten bir yorum girin.</span><span class="sxs-lookup"><span data-stu-id="ee24b-128">In the **Comment** field, enter a comment that explains why you are delegating the work items.</span></span>

