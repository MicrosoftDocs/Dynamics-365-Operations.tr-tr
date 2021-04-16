---
title: İş akışındaki iş öğelerini devretme
description: Bir süreliğine ofis dışında olacaksanız ya da iş öğeleri ile ilgili uygulama yapamayacaksanız iş öğelerinizi diğer kullanıcılara devredebilir veya yeniden atayabilirsiniz.
author: ChrisGarty
ms.date: 07/07/2020
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: SysUserSetup, WorkflowDelegationUserListLookup
audience: Application User
ms.reviewer: sericks
ms.search.region: Global
ms.author: cgarty
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ed21f6d32cdcf74eb153daba32c20b7cef94d4e4
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/31/2021
ms.locfileid: "5747381"
---
# <a name="delegate-work-items-in-a-workflow"></a><span data-ttu-id="5675b-103">İş akışındaki iş öğelerini devretme</span><span class="sxs-lookup"><span data-stu-id="5675b-103">Delegate work items in a workflow</span></span>

[!include [banner](../../includes/banner.md)]

## <a name="manually-delegate-a-work-item"></a><span data-ttu-id="5675b-104">Bir iş öğesini el ile devredin</span><span class="sxs-lookup"><span data-stu-id="5675b-104">Manually delegate a work item</span></span>

<span data-ttu-id="5675b-105">Bir tekil iş öğesini devretmek için **Devret** seçeneğini **İş akışı** menüsünde seçin ve daha sonra devredilecek kullanıcıyı bir yorum ile seçin.</span><span class="sxs-lookup"><span data-stu-id="5675b-105">To delegate an individual work item, select the **Delegate** option in the **Workflow** menu and then enter the user to be delegated to along with a comment.</span></span> <span data-ttu-id="5675b-106">Bu, iş öğesini tamamlayabilmeleri için bu kullanıcıya yeniden atayacaktır.</span><span class="sxs-lookup"><span data-stu-id="5675b-106">This will reassign the work item to that user so they can complete it.</span></span>

## <a name="manually-delegate-multiple-work-items"></a><span data-ttu-id="5675b-107">Çoklu iş öğelerini el ile devret</span><span class="sxs-lookup"><span data-stu-id="5675b-107">Manually delegate multiple work items</span></span>

<span data-ttu-id="5675b-108">**Bana atanan iş öğeleri** sayfasından birlikte birden fazla iş öğesine temsilci atanmış olabilir.</span><span class="sxs-lookup"><span data-stu-id="5675b-108">Multiple work items can be delegated together from the **Work items assigned to me** page.</span></span> <span data-ttu-id="5675b-109">Aşağıdaki iş akışı türleri toplu temsilci seçme için uygun: Satınalma Sözleşmesi onay iş akışı, satınalma siparişi iş akışı, satınalma talebi gözden geçirme ve satıcı faturası iş akışı.</span><span class="sxs-lookup"><span data-stu-id="5675b-109">The following workflow types are eligible for mass delegation: Purchase agreement approval workflow, Purchase order workflow, Purchase requisition review, and Vendor invoice workflow.</span></span> <span data-ttu-id="5675b-110">**Çoklu iş öğeleri temsilcisi** özelliği varsayılan olarak devre dışıdır ve **çalışma alanları > özellik yönetimi** etkinleştirilebilir.</span><span class="sxs-lookup"><span data-stu-id="5675b-110">The **Delegate multiple work items** feature is disabled by default and can be enabled in **Workspaces > Feature management**.</span></span> <span data-ttu-id="5675b-111">Bu özelliği etkinleştirme konusunda yardım için sistem yöneticinize başvurun.</span><span class="sxs-lookup"><span data-stu-id="5675b-111">Contact your system administrator for help with enabling this feature.</span></span>
1.  <span data-ttu-id="5675b-112">**Ortak > Ortak > Çalışma öğeleri > Bana atanan iş öğeleri**'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="5675b-112">Go to **Common > Common > Work items > Work items assigned to me**.</span></span>
2.  <span data-ttu-id="5675b-113">Temsilci seçilecek iş öğelerini seçin.</span><span class="sxs-lookup"><span data-stu-id="5675b-113">Select the work items that will be delegated.</span></span>
3.  <span data-ttu-id="5675b-114">**Çalışma öğeleri devret** menüsüne tıklatın.</span><span class="sxs-lookup"><span data-stu-id="5675b-114">Click the **Delegate work items** menu.</span></span>
4.  <span data-ttu-id="5675b-115">**Kullanıcı** alanında, iş maddelerine temsilci olarak atanacak kullanıcıyı seçin.</span><span class="sxs-lookup"><span data-stu-id="5675b-115">In the **User** field, select the user to delegate the work items to.</span></span>
5.  <span data-ttu-id="5675b-116">**Yorum** alanına, iş maddelerine neden temsilci atadığınızı belirten bir yorum girin.</span><span class="sxs-lookup"><span data-stu-id="5675b-116">In the **Comment** field, enter a comment that explains why you're delegating the work items.</span></span>
6.  <span data-ttu-id="5675b-117">Çalışma öğesi temsilcisini tamamlamak için **iş maddelerini devret** düğmesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="5675b-117">Click the **Delegate work items** button to complete the work item delegation.</span></span>

## <a name="automatically-delegate-work-items"></a><span data-ttu-id="5675b-118">Otomatik olarak iş öğelerini devret</span><span class="sxs-lookup"><span data-stu-id="5675b-118">Automatically delegate work items</span></span>

<span data-ttu-id="5675b-119">Bir süreliğine ofis dışında olmayı veya başka sebeple iş öğeleri üzerinde çalışamamayı planlıyorsanız, yeni iş öğelerini diğer kullanıcılara **Kullanıcı seçenekleri** sayfasını kullanarak otomatik olarak devredebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="5675b-119">If you plan to be out of the office or otherwise unavailable to act on work items for a period of time, you can automatically delegate new work items to other users using the **User options** page.</span></span>

### <a name="set-up-automatic-delegation"></a><span data-ttu-id="5675b-120">Otomatik temsil ayarlama</span><span class="sxs-lookup"><span data-stu-id="5675b-120">Set up automatic delegation</span></span>
1. <span data-ttu-id="5675b-121">**Ortak > Kurulum > Kullanıcı** seçenekleri'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="5675b-121">Go to **Common > Setup > User options**.</span></span>
2. <span data-ttu-id="5675b-122">**İş akışı** sekmesine tıklayın. Temsilci bölümünün genişletilmiş olduğundan emin olun.</span><span class="sxs-lookup"><span data-stu-id="5675b-122">Click the **Workflow** tab. Make sure the Delegation section is expanded.</span></span> <span data-ttu-id="5675b-123">Diğer kullanıcılar iş maddelerinize otomatik olarak temsilci olarak atanacak biçimde sistemi yapılandırmak için, hangi iş maddesi türlerine ne zaman temsilci atanacağını belirten temsilci kuralları oluşturmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="5675b-123">To configure the system to automatically delegate your work items to other users, you must create delegation rules, which specify when certain types of work items are delegated.</span></span> <span data-ttu-id="5675b-124">Temsilci kuralı oluşturmak için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="5675b-124">Follow these steps to create a delegation rule.</span></span>  
3. <span data-ttu-id="5675b-125">**Ekle** öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="5675b-125">Click **Add**.</span></span>
4. <span data-ttu-id="5675b-126">**Kapsam** alanında, bir seçenek belirleyin:</span><span class="sxs-lookup"><span data-stu-id="5675b-126">In the **Scope** field, select an option:</span></span>
    - <span data-ttu-id="5675b-127">Tümü: Size atanmış olan tüm iş maddelerine temsilci seçin.</span><span class="sxs-lookup"><span data-stu-id="5675b-127">All – Delegate all work items that are assigned to you.</span></span>
    - <span data-ttu-id="5675b-128">Modül: Yalnızca belirli bir iş akışı türüyle ilişkili iş maddelerine temsilci atayın.</span><span class="sxs-lookup"><span data-stu-id="5675b-128">Module – Delegate only the work items that are related to a specific type of workflow.</span></span> <span data-ttu-id="5675b-129">Bu seçeneği belirlerseniz **Ad** alanında iş akışı türünü seçmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="5675b-129">If you select this option, you must select the type of workflow in the **Name** field.</span></span>
    - <span data-ttu-id="5675b-130">İş akışı: Yalnızca belirli bir iş akışıyla ilişkili iş maddelerine temsilci atayın.</span><span class="sxs-lookup"><span data-stu-id="5675b-130">Workflow – Delegate only the work items that are related to a specific workflow.</span></span> <span data-ttu-id="5675b-131">Bu seçeneği belirlerseniz **Ad** alanında iş akışını seçmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="5675b-131">If you select this option, you must select the workflow in the **Name** field.</span></span>  
5. <span data-ttu-id="5675b-132">**Ad** alanını doldurun:</span><span class="sxs-lookup"><span data-stu-id="5675b-132">In the **Name** field:</span></span>
    - <span data-ttu-id="5675b-133">**Modül** kapsamı için hedef modülü seçin.</span><span class="sxs-lookup"><span data-stu-id="5675b-133">For **Module** scope, select the target module.</span></span>
    - <span data-ttu-id="5675b-134">**İş akışı** kapsamı için hedef iş akışını seçin.</span><span class="sxs-lookup"><span data-stu-id="5675b-134">For **Workflow** scope, select the target workflow.</span></span>
6. <span data-ttu-id="5675b-135">**Temsilci** alanında, iş maddelerine temsilci olarak atanacak kullanıcıyı seçin.</span><span class="sxs-lookup"><span data-stu-id="5675b-135">In the **Delegate** field, select the user to delegate the work items to.</span></span> <span data-ttu-id="5675b-136">İş öğelerine ne zaman otomatik olarak temsilci atanmasını istediğinizi belirtmek için **Başlangıç tarihi/saati** ve **Bitiş tarihi/saati** alanlarını kullanın.</span><span class="sxs-lookup"><span data-stu-id="5675b-136">Use the **Start date/time** and **End date/time** fields to specify when you want the work items to be automatically delegated.</span></span>  
7. <span data-ttu-id="5675b-137">**Başlangıç tarihi/saati** alanına tarih ve saati girin.</span><span class="sxs-lookup"><span data-stu-id="5675b-137">In the **Start date/time** field, enter a date and time.</span></span>
8. <span data-ttu-id="5675b-138">**Bitiş tarihi/saati** alanına tarih ve saati girin.</span><span class="sxs-lookup"><span data-stu-id="5675b-138">In the **End date/time** field, enter a date and time.</span></span>
9. <span data-ttu-id="5675b-139">Bu temsilci kuralını etkinleştirmek için **Etkin** onay kutusunu işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="5675b-139">Select the **Enabled** check box to activate the delegation rule.</span></span> 
10. <span data-ttu-id="5675b-140">**Yorum** alanına, iş maddelerine neden temsilci atadığınızı belirten bir yorum girin.</span><span class="sxs-lookup"><span data-stu-id="5675b-140">In the **Comment** field, enter a comment that explains why you're delegating the work items.</span></span>


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]