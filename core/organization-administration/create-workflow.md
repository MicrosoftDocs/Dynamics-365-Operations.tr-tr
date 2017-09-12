---
title: "İş akışı oluşturma"
description: "Bu konular bir iş akışının nasıl oluşturulacağını açıklar."
author: sericks007
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, UnifiedOperations
ms.custom: 195583
ms.assetid: 836ddd01-cc34-45c3-a4b0-20647357dbc6
ms.search.region: Global
ms.author: donaldc
ms.search.validFrom: 2016-08-30
ms.dyn365.ops.version: Platform update 2
ms.translationtype: Human Translation
ms.sourcegitcommit: 08c38aada355583c5a6872f75b57db95d9b81786
ms.openlocfilehash: 4d57e47fe7f38a43ecfdfbdd701d7e6a7d7800d6
ms.contentlocale: tr-tr
ms.lasthandoff: 07/18/2017

---

# <a name="create-a-workflow"></a><span data-ttu-id="36eb6-103">İş akışı oluşturma</span><span class="sxs-lookup"><span data-stu-id="36eb6-103">Create a workflow</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="36eb6-104">Bu konular bir iş akışının nasıl oluşturulacağını açıklar.</span><span class="sxs-lookup"><span data-stu-id="36eb6-104">This topics explains how to create a workflow.</span></span>

<a name="open-the-workflow-editor"></a><span data-ttu-id="36eb6-105">İş akışı düzenleyicisini açma</span><span class="sxs-lookup"><span data-stu-id="36eb6-105">Open the workflow editor</span></span>
------------------------

<span data-ttu-id="36eb6-106">Oluşturabileceğiniz iş akışı türleri, çalışmakta olduğunuz Microsoft Dynamics 365 for Finance and Operations modülüne göre belirlenir.</span><span class="sxs-lookup"><span data-stu-id="36eb6-106">The Microsoft Dynamics 365 for Finance and Operations module that you're working in determines the types of workflow that you can create.</span></span> <span data-ttu-id="36eb6-107">Oluşturmak için iş akışı türünü seçmek ve iş akışı düzenleyicisini açmak için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="36eb6-107">Follow these steps to select the type of workflow to create and open the workflow editor.</span></span>

1.  <span data-ttu-id="36eb6-108">Yeni bir iş akışı oluşturmak istediğiniz modülü açın.</span><span class="sxs-lookup"><span data-stu-id="36eb6-108">Open the module that you want to create a new workflow for.</span></span> <span data-ttu-id="36eb6-109">Örneğin, satınalma talepleri için bir iş akışı oluşturmak için **Tedarik ve kaynak atama**'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="36eb6-109">For example, to create a workflow for purchase requisitions, click **Procurement and sourcing**.</span></span>
2.  <span data-ttu-id="36eb6-110">**Kurulum** &gt; **\[Modül adı\] iş akışları'na** tıklayın.</span><span class="sxs-lookup"><span data-stu-id="36eb6-110">Click **Setup** &gt; **\[Module name\] workflows**.</span></span>
3.  <span data-ttu-id="36eb6-111">Eylem Bölmesi'nde görüntülenen liste sayfasında **Yeni**'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="36eb6-111">On the list page that appears, on the Action Pane, click **New**.</span></span>
4.  <span data-ttu-id="36eb6-112">**İş akışı oluştur** sayfasında oluşturmak için iş akışı türünü seçin ve ardından **İş akışı oluştur**'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="36eb6-112">On the **Create workflow** page, select the type of workflow to create, and then click **Create workflow**.</span></span> <span data-ttu-id="36eb6-113">İş akışı düzenleyicisi görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="36eb6-113">The workflow editor appears.</span></span> <span data-ttu-id="36eb6-114">İş akışını tasarlamak için artık aşağıdaki yordamları kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="36eb6-114">You can now use the following procedures to design the workflow.</span></span>

## <a name="drag-workflow-elements-onto-the-canvas"></a><span data-ttu-id="36eb6-115">İş akışı öğelerini tuval üzerine sürükleme</span><span class="sxs-lookup"><span data-stu-id="36eb6-115">Drag workflow elements onto the canvas</span></span>
<span data-ttu-id="36eb6-116">İş akışı düzenleyicisinin **İş akışı öğeleri** alanı iş akışınıza ekleyebileceğiniz öğeler içerir.</span><span class="sxs-lookup"><span data-stu-id="36eb6-116">The **Workflow elements** area of the workflow editor contains the elements that you can add to your workflow.</span></span> <span data-ttu-id="36eb6-117">Öğeleri iş akışına eklemek için tuval üzerine sürükleyin.</span><span class="sxs-lookup"><span data-stu-id="36eb6-117">To add elements to the workflow, drag them onto the canvas.</span></span>

## <a name="connect-the-elements"></a><span data-ttu-id="36eb6-118">Öğeleri bağlama</span><span class="sxs-lookup"><span data-stu-id="36eb6-118">Connect the elements</span></span>
<span data-ttu-id="36eb6-119">İş akışı öğesini bir başkasına bağlamak için işaretçiyi bağlantı noktaları görünene kadar öğenin üstünde tutun.</span><span class="sxs-lookup"><span data-stu-id="36eb6-119">To connect one workflow element to another, hold the pointer over an element until connection points appear.</span></span> <span data-ttu-id="36eb6-120">Bağlantı noktasına tıklayın ve bir başka öğeye sürükleyin.</span><span class="sxs-lookup"><span data-stu-id="36eb6-120">Click a connection point, and drag it to another element.</span></span> <span data-ttu-id="36eb6-121">Tüm öğeleri bağladığınızdan emin olun.</span><span class="sxs-lookup"><span data-stu-id="36eb6-121">Be sure to connect all the elements.</span></span>

## <a name="configure-the-properties-of-the-workflow"></a><span data-ttu-id="36eb6-122">İş akışının özelliklerini yapılandırma</span><span class="sxs-lookup"><span data-stu-id="36eb6-122">Configure the properties of the workflow</span></span>
<span data-ttu-id="36eb6-123">İş akışının özelliklerini yapılandırmak için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="36eb6-123">Follow these steps to configure the properties of the workflow.</span></span>

1.  <span data-ttu-id="36eb6-124">Herhangi bir iş akışı öğesinin seçili olmadığından emin olmak için tuvale tıklayın.</span><span class="sxs-lookup"><span data-stu-id="36eb6-124">Click the canvas to make sure that no workflow element is selected.</span></span>
2.  <span data-ttu-id="36eb6-125">İş akışı için **Özellikler** sayfasını açmak için **Özellikler**'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="36eb6-125">Click **Properties** to open the **Properties** page for the workflow.</span></span>
3.  <span data-ttu-id="36eb6-126">[İş akışının özelliklerini yapılandırma](configure-workflow-properties.md) konusundaki yordamları uygulayın.</span><span class="sxs-lookup"><span data-stu-id="36eb6-126">Follow the procedures in the [Configure the properties of a workflow](configure-workflow-properties.md) topic.</span></span>

## <a name="configure-the-elements-of-the-workflow"></a><span data-ttu-id="36eb6-127">İş akışının öğelerini yapılandırma</span><span class="sxs-lookup"><span data-stu-id="36eb6-127">Configure the elements of the workflow</span></span>
<span data-ttu-id="36eb6-128">Tuvalin üzerine sürüklediğiniz tüm öğeleri yapılandırın.</span><span class="sxs-lookup"><span data-stu-id="36eb6-128">Configure each element that you dragged onto the canvas.</span></span> <span data-ttu-id="36eb6-129">Tüm iş akışı öğelerini nasıl yapılandıracağınız hakkında daha fazla bilgi için aşağıdaki konulara bakın:</span><span class="sxs-lookup"><span data-stu-id="36eb6-129">For information about how to configure each workflow element, see the following topics:</span></span>

-   [<span data-ttu-id="36eb6-130">El ile girilen bir görev yapılandırma</span><span class="sxs-lookup"><span data-stu-id="36eb6-130">Configure a manual task</span></span>](configure-manual-task-workflow.md)
-   [<span data-ttu-id="36eb6-131">Otomatik bir görev yapılandırma</span><span class="sxs-lookup"><span data-stu-id="36eb6-131">Configure an automated task</span></span>](configure-automated-task-workflow.md)
-   [<span data-ttu-id="36eb6-132">Onay süreci konfigüre etme</span><span class="sxs-lookup"><span data-stu-id="36eb6-132">Configure an approval process</span></span>](configure-approval-process-workflow.md)
-   [<span data-ttu-id="36eb6-133">Onay adımı konfigüre etme</span><span class="sxs-lookup"><span data-stu-id="36eb6-133">Configure an approval step</span></span>](configure-approval-step-workflow.md)
-   [<span data-ttu-id="36eb6-134">El ile girilen bir karar yapılandırma</span><span class="sxs-lookup"><span data-stu-id="36eb6-134">Configure a manual decision</span></span>](configure-manual-decision-workflow.md)
-   [<span data-ttu-id="36eb6-135">Koşullu bir kararı yapılandırma</span><span class="sxs-lookup"><span data-stu-id="36eb6-135">Configure a conditional decision</span></span>](configure-conditional-decision-workflow.md)
-   [<span data-ttu-id="36eb6-136">Paralel faaliyet yapılandırma</span><span class="sxs-lookup"><span data-stu-id="36eb6-136">Configure a parallel activity</span></span>](configure-parallel-activity-workflow.md)
-   [<span data-ttu-id="36eb6-137">Paralel dal yapılandırma</span><span class="sxs-lookup"><span data-stu-id="36eb6-137">Configure a parallel branch</span></span>](configure-parallel-branch-workflow.md)
-   [<span data-ttu-id="36eb6-138">Satır maddesi iş akışı yapılandırma</span><span class="sxs-lookup"><span data-stu-id="36eb6-138">Configure a line-item workflow</span></span>](configure-line-item-workflow.md)

## <a name="resolve-any-errors-or-warnings"></a><span data-ttu-id="36eb6-139">Hatalar veya uyarıları çözümleme</span><span class="sxs-lookup"><span data-stu-id="36eb6-139">Resolve any errors or warnings</span></span>
<span data-ttu-id="36eb6-140">İş akışı düzenleyicisinin altındaki **Hatalar ve uyarılar** bölmesi iş akışı için oluşturulan iletileri gösterir.</span><span class="sxs-lookup"><span data-stu-id="36eb6-140">The **Errors and warnings** pane at the bottom of the workflow editor shows messages that have been generated for the workflow.</span></span> <span data-ttu-id="36eb6-141">Hatanın veya uyarının nerede oluştuğunu bulmak için hata veya uyarı iletisine çift tıklayın.</span><span class="sxs-lookup"><span data-stu-id="36eb6-141">To find the element where an error or warning occurred, double-click the error or warning message.</span></span> <span data-ttu-id="36eb6-142">İş akışını etkin hale getirmeden önce tüm hataları ve uyarıları çözümlemeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="36eb6-142">You must resolve all errors and warnings before you can make the workflow active.</span></span>

## <a name="save-and-activate-the-workflow"></a><span data-ttu-id="36eb6-143">İş akışını kaydetme ve etkinleştirme</span><span class="sxs-lookup"><span data-stu-id="36eb6-143">Save and activate the workflow</span></span>
<span data-ttu-id="36eb6-144">İş akışını kaydetmek ve etkinleştirmek için hazır olduğunuzda bu adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="36eb6-144">When you're ready to save and activate the workflow, follow these steps.</span></span>

1.  <span data-ttu-id="36eb6-145">İş akışı düzenleyicisini kapatmak için **Kaydet ve kapat**'a tıklayın ve **İş akışını kaydet** sayfasını açın.</span><span class="sxs-lookup"><span data-stu-id="36eb6-145">Click **Save and close** to close the workflow editor and open the **Save workflow** page.</span></span>
2.  <span data-ttu-id="36eb6-146">İş akışında yaptığınız değişiklikler hakkında yorumlar girin ve ardından **Tamam**'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="36eb6-146">Enter comments about the changes that you've made to the workflow, and then click **OK**.</span></span>
3.  <span data-ttu-id="36eb6-147">Tüm hatalar ve uyarılar çözümlenirse **İş akışını etkinleştir** sayfası görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="36eb6-147">If all errors and warnings have been resolved, the **Activate workflow** page appears.</span></span> <span data-ttu-id="36eb6-148">Aşağıdaki seçeneklerden birini belirleyin:</span><span class="sxs-lookup"><span data-stu-id="36eb6-148">Select one of the following options:</span></span>
    -   <span data-ttu-id="36eb6-149">İş akışının bu sürümünü etkinleştirmek için **Yeni sürümü etkinleştir**'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="36eb6-149">To activate this version of the workflow, click **Activate the new version**.</span></span> <span data-ttu-id="36eb6-150">İş akışı etkinken kullanıcılar işlenmesi için iş akışına belgeler gönderebilir.</span><span class="sxs-lookup"><span data-stu-id="36eb6-150">When a workflow is active, users can submit documents to it for processing.</span></span>
    -   <span data-ttu-id="36eb6-151">Bu sürümü etkinleştirmek istemiyorsanız **Yeni sürümü etkinleştirme**'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="36eb6-151">If you don't want to activate this version, click **Do not activate the new version**.</span></span> <span data-ttu-id="36eb6-152">İş akışını daha sonra etkinleştirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="36eb6-152">You can activate the workflow later.</span></span>






