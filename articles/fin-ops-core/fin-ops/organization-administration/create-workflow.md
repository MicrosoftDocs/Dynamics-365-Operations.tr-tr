---
title: İş akışlarına genel bakış
description: Bu konu bir iş akışının nasıl oluşturulacağını açıklar.
author: ChrisGarty
manager: AnnBe
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WorkflowSelectTemplateRnr, WorkflowTableListPageRnr
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 195583
ms.assetid: 836ddd01-cc34-45c3-a4b0-20647357dbc6
ms.search.region: Global
ms.author: cgarty
ms.search.validFrom: 2016-08-30
ms.dyn365.ops.version: Platform update 2
ms.openlocfilehash: bcd548bf8e03e0e6df4d413afe8c9ae01c570899
ms.sourcegitcommit: e55efd2f62bf60f678108c09ad4701a76b20cc68
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/17/2020
ms.locfileid: "3698030"
---
# <a name="create-workflows-overview"></a><span data-ttu-id="31e4a-103">İş akışlarına genel bakış</span><span class="sxs-lookup"><span data-stu-id="31e4a-103">Create workflows overview</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="31e4a-104">Bu konu bir iş akışının nasıl oluşturulacağını açıklar.</span><span class="sxs-lookup"><span data-stu-id="31e4a-104">This topic explains how to create a workflow.</span></span>

## <a name="open-the-workflow-editor"></a><span data-ttu-id="31e4a-105">İş akışı düzenleyicisini açma</span><span class="sxs-lookup"><span data-stu-id="31e4a-105">Open the workflow editor</span></span>

<span data-ttu-id="31e4a-106">Oluşturabileceğiniz iş akışı türleri, çalışmakta olduğunuz modüle göre belirlenir.</span><span class="sxs-lookup"><span data-stu-id="31e4a-106">The module that you're working in determines the types of workflow that you can create.</span></span> <span data-ttu-id="31e4a-107">Oluşturmak için iş akışı türünü seçmek ve iş akışı düzenleyicisini açmak için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="31e4a-107">Follow these steps to select the type of workflow to create and open the workflow editor.</span></span>

1. <span data-ttu-id="31e4a-108">Yeni bir iş akışı oluşturmak istediğiniz modülü açın.</span><span class="sxs-lookup"><span data-stu-id="31e4a-108">Open the module that you want to create a new workflow for.</span></span> <span data-ttu-id="31e4a-109">Örneğin, satınalma talepleri için bir iş akışı oluşturmak için **Tedarik ve kaynak atama**'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="31e4a-109">For example, to create a workflow for purchase requisitions, click **Procurement and sourcing**.</span></span>
2. <span data-ttu-id="31e4a-110">**Kurulum** &gt; **\[Modül adı\] iş akışları'na** tıklayın.</span><span class="sxs-lookup"><span data-stu-id="31e4a-110">Click **Setup** &gt; **\[Module name\] workflows**.</span></span>
3. <span data-ttu-id="31e4a-111">Eylem Bölmesi'nde görüntülenen liste sayfasında **Yeni**'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="31e4a-111">On the list page that appears, on the Action Pane, click **New**.</span></span>
4. <span data-ttu-id="31e4a-112">**İş akışı oluştur** sayfasında oluşturmak için iş akışı türünü seçin ve ardından **İş akışı oluştur**'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="31e4a-112">On the **Create workflow** page, select the type of workflow to create, and then click **Create workflow**.</span></span> <span data-ttu-id="31e4a-113">İş akışı düzenleyicisi görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="31e4a-113">The workflow editor appears.</span></span> <span data-ttu-id="31e4a-114">İş akışını tasarlamak için artık aşağıdaki yordamları kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="31e4a-114">You can now use the following procedures to design the workflow.</span></span>

## <a name="drag-workflow-elements-onto-the-canvas"></a><span data-ttu-id="31e4a-115">İş akışı öğelerini tuval üzerine sürükleme</span><span class="sxs-lookup"><span data-stu-id="31e4a-115">Drag workflow elements onto the canvas</span></span>

<span data-ttu-id="31e4a-116">İş akışı düzenleyicisinin **İş akışı öğeleri** alanı iş akışınıza ekleyebileceğiniz öğeler içerir.</span><span class="sxs-lookup"><span data-stu-id="31e4a-116">The **Workflow elements** area of the workflow editor contains the elements that you can add to your workflow.</span></span> <span data-ttu-id="31e4a-117">Öğeleri iş akışına eklemek için tuval üzerine sürükleyin.</span><span class="sxs-lookup"><span data-stu-id="31e4a-117">To add elements to the workflow, drag them onto the canvas.</span></span>

## <a name="connect-the-elements"></a><span data-ttu-id="31e4a-118">Öğeleri bağlama</span><span class="sxs-lookup"><span data-stu-id="31e4a-118">Connect the elements</span></span>

<span data-ttu-id="31e4a-119">İş akışı öğesini bir başkasına bağlamak için işaretçiyi bağlantı noktaları görünene kadar öğenin üstünde tutun.</span><span class="sxs-lookup"><span data-stu-id="31e4a-119">To connect one workflow element to another, hold the pointer over an element until connection points appear.</span></span> <span data-ttu-id="31e4a-120">Bağlantı noktasına tıklayın ve bir başka öğeye sürükleyin.</span><span class="sxs-lookup"><span data-stu-id="31e4a-120">Click a connection point, and drag it to another element.</span></span> <span data-ttu-id="31e4a-121">Tüm öğeleri bağladığınızdan emin olun.</span><span class="sxs-lookup"><span data-stu-id="31e4a-121">Be sure to connect all the elements.</span></span>

## <a name="configure-the-properties-of-the-workflow"></a><span data-ttu-id="31e4a-122">İş akışının özelliklerini yapılandırma</span><span class="sxs-lookup"><span data-stu-id="31e4a-122">Configure the properties of the workflow</span></span>

<span data-ttu-id="31e4a-123">İş akışının özelliklerini yapılandırmak için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="31e4a-123">Follow these steps to configure the properties of the workflow.</span></span>

1. <span data-ttu-id="31e4a-124">Herhangi bir iş akışı öğesinin seçili olmadığından emin olmak için tuvale tıklayın.</span><span class="sxs-lookup"><span data-stu-id="31e4a-124">Click the canvas to make sure that no workflow element is selected.</span></span>
2. <span data-ttu-id="31e4a-125">İş akışı için **Özellikler** sayfasını açmak için **Özellikler**'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="31e4a-125">Click **Properties** to open the **Properties** page for the workflow.</span></span>
3. <span data-ttu-id="31e4a-126">[İş akışı özelliklerini yapılandırma](configure-workflow-properties.md) konusundaki prosedürleri uygulayın.</span><span class="sxs-lookup"><span data-stu-id="31e4a-126">Follow the procedures in the [Configure workflow properties](configure-workflow-properties.md) topic.</span></span>

## <a name="configure-the-elements-of-the-workflow"></a><span data-ttu-id="31e4a-127">İş akışının öğelerini yapılandırma</span><span class="sxs-lookup"><span data-stu-id="31e4a-127">Configure the elements of the workflow</span></span>

<span data-ttu-id="31e4a-128">Tuvalin üzerine sürüklediğiniz tüm öğeleri yapılandırın.</span><span class="sxs-lookup"><span data-stu-id="31e4a-128">Configure each element that you dragged onto the canvas.</span></span> <span data-ttu-id="31e4a-129">Tüm iş akışı öğelerini nasıl yapılandıracağınız hakkında daha fazla bilgi için aşağıdaki konulara bakın:</span><span class="sxs-lookup"><span data-stu-id="31e4a-129">For information about how to configure each workflow element, see the following topics:</span></span>

- [<span data-ttu-id="31e4a-130">İş akışında el ile girilen görevleri yapılandırma</span><span class="sxs-lookup"><span data-stu-id="31e4a-130">Configure manual tasks in a workflow</span></span>](configure-manual-task-workflow.md)
- [<span data-ttu-id="31e4a-131">İş akışında otomatikleştirilmiş görevleri yapılandırma</span><span class="sxs-lookup"><span data-stu-id="31e4a-131">Configure automated tasks in a workflow</span></span>](configure-automated-task-workflow.md)
- [<span data-ttu-id="31e4a-132">İş akışında onay işlemlerini yapılandırma</span><span class="sxs-lookup"><span data-stu-id="31e4a-132">Configure approval processes in a workflow</span></span>](configure-approval-process-workflow.md)
- [<span data-ttu-id="31e4a-133">İş akışında onay adımlarını yapılandırma</span><span class="sxs-lookup"><span data-stu-id="31e4a-133">Configure approval steps in a workflow</span></span>](configure-approval-step-workflow.md)
- [<span data-ttu-id="31e4a-134">İş akışında el ile girilen kararları yapılandırma</span><span class="sxs-lookup"><span data-stu-id="31e4a-134">Configure manual decisions in a workflow</span></span>](configure-manual-decision-workflow.md)
- [<span data-ttu-id="31e4a-135">İş akışında koşullu kararları yapılandırma</span><span class="sxs-lookup"><span data-stu-id="31e4a-135">Configure conditional decisions in a workflow</span></span>](configure-conditional-decision-workflow.md)
- [<span data-ttu-id="31e4a-136">İş akışında paralel dalları yapılandırma</span><span class="sxs-lookup"><span data-stu-id="31e4a-136">Configure parallel branches in a workflow</span></span>](configure-parallel-activity-workflow.md)
- [<span data-ttu-id="31e4a-137">Paralel dalı yapılandırma</span><span class="sxs-lookup"><span data-stu-id="31e4a-137">Configure a parallel branch</span></span>](configure-parallel-branch-workflow.md)
- [<span data-ttu-id="31e4a-138">Satır maddesi iş akışlarını yapılandırma</span><span class="sxs-lookup"><span data-stu-id="31e4a-138">Configure line-item workflows</span></span>](configure-line-item-workflow.md)

## <a name="resolve-any-errors-or-warnings"></a><span data-ttu-id="31e4a-139">Hatalar veya uyarıları çözümleme</span><span class="sxs-lookup"><span data-stu-id="31e4a-139">Resolve any errors or warnings</span></span>

<span data-ttu-id="31e4a-140">İş akışı düzenleyicisinin altındaki **Hatalar ve uyarılar** bölmesi iş akışı için oluşturulan iletileri gösterir.</span><span class="sxs-lookup"><span data-stu-id="31e4a-140">The **Errors and warnings** pane at the bottom of the workflow editor shows messages that have been generated for the workflow.</span></span> <span data-ttu-id="31e4a-141">Hatanın veya uyarının nerede oluştuğunu bulmak için hata veya uyarı iletisine çift tıklayın.</span><span class="sxs-lookup"><span data-stu-id="31e4a-141">To find the element where an error or warning occurred, double-click the error or warning message.</span></span> <span data-ttu-id="31e4a-142">İş akışını etkin hale getirmeden önce tüm hataları ve uyarıları çözümlemeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="31e4a-142">You must resolve all errors and warnings before you can make the workflow active.</span></span>

## <a name="save-and-activate-the-workflow"></a><span data-ttu-id="31e4a-143">İş akışını kaydetme ve etkinleştirme</span><span class="sxs-lookup"><span data-stu-id="31e4a-143">Save and activate the workflow</span></span>

<span data-ttu-id="31e4a-144">İş akışını kaydetmek ve etkinleştirmek için hazır olduğunuzda bu adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="31e4a-144">When you're ready to save and activate the workflow, follow these steps.</span></span>

1. <span data-ttu-id="31e4a-145">İş akışı düzenleyicisini kapatmak için **Kaydet ve kapat**'a tıklayın ve **İş akışını kaydet** sayfasını açın.</span><span class="sxs-lookup"><span data-stu-id="31e4a-145">Click **Save and close** to close the workflow editor and open the **Save workflow** page.</span></span>
2. <span data-ttu-id="31e4a-146">İş akışında yaptığınız değişiklikler hakkında yorumlar girin ve ardından **Tamam**'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="31e4a-146">Enter comments about the changes that you've made to the workflow, and then click **OK**.</span></span>
3. <span data-ttu-id="31e4a-147">Tüm hatalar ve uyarılar çözümlenirse **İş akışını etkinleştir** sayfası görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="31e4a-147">If all errors and warnings have been resolved, the **Activate workflow** page appears.</span></span> <span data-ttu-id="31e4a-148">Aşağıdaki seçeneklerden birini belirleyin:</span><span class="sxs-lookup"><span data-stu-id="31e4a-148">Select one of the following options:</span></span>

    - <span data-ttu-id="31e4a-149">İş akışının bu sürümünü etkinleştirmek için **Yeni sürümü etkinleştir**'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="31e4a-149">To activate this version of the workflow, click **Activate the new version**.</span></span> <span data-ttu-id="31e4a-150">İş akışı etkinken kullanıcılar işlenmesi için iş akışına belgeler gönderebilir.</span><span class="sxs-lookup"><span data-stu-id="31e4a-150">When a workflow is active, users can submit documents to it for processing.</span></span>
    - <span data-ttu-id="31e4a-151">Bu sürümü etkinleştirmek istemiyorsanız **Yeni sürümü etkinleştirme**'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="31e4a-151">If you don't want to activate this version, click **Do not activate the new version**.</span></span> <span data-ttu-id="31e4a-152">İş akışını daha sonra etkinleştirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="31e4a-152">You can activate the workflow later.</span></span>
