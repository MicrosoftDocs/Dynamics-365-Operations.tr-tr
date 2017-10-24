---
title: "Satır maddesi iş akışı yapılandırma"
description: "Bu konu, bir satır maddesi iş akışı öğesinin nasıl yapılandırılacağını açıklar."
author: sericks007
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 195833
ms.assetid: 3237347e-71d5-4569-bc9a-0d0fc9410b78
ms.search.region: Global
ms.author: donaldc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: d888bf4285a27369b197ed66e5975cc806c640d3
ms.contentlocale: tr-tr
ms.lasthandoff: 09/29/2017

---

# <a name="configure-a-line-item-workflow"></a><span data-ttu-id="fe061-103">Satır maddesi iş akışı yapılandırma</span><span class="sxs-lookup"><span data-stu-id="fe061-103">Configure a line-item workflow</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="fe061-104">Bu konu, bir satır maddesi iş akışı öğesinin nasıl yapılandırılacağını açıklar.</span><span class="sxs-lookup"><span data-stu-id="fe061-104">This topic explains how to configure a line-item workflow element.</span></span>

<span data-ttu-id="fe061-105">Satır maddesi iş akışı öğesi yapılandırmak için öğeye sağ tıklayın ve ardından **Özellikler** sayfasını açmak için **Özellikler**'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="fe061-105">To configure a line-item workflow element, in the workflow editor, right-click the element, and then click **Properties** to open the **Properties** page.</span></span> <span data-ttu-id="fe061-106">Ardından satır maddesi iş akışı öğesinin özelliklerini yapılandırmak için aşağıdaki yordamları kullanın.</span><span class="sxs-lookup"><span data-stu-id="fe061-106">Then use the following procedures to configure the properties of the line-item workflow element.</span></span>

## <a name="name-the-lineitem-workflow-element"></a><span data-ttu-id="fe061-107">Satır maddesi iş akışı öğesini adlandırın</span><span class="sxs-lookup"><span data-stu-id="fe061-107">Name the lineitem workflow element</span></span>
<span data-ttu-id="fe061-108">Satır maddesi iş akışı öğesi için bir ad girmek için bu adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="fe061-108">Follow these steps to enter a name for the line-item workflow element.</span></span>

1.  <span data-ttu-id="fe061-109">Sol bölmede **Temel Ayarlar**'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="fe061-109">In the left pane, click **Basic Settings**.</span></span>
2.  <span data-ttu-id="fe061-110">**Ad** alanında satır maddesi iş akışı öğesi için benzersiz bir ad girin.</span><span class="sxs-lookup"><span data-stu-id="fe061-110">In the **Name** field, enter a unique name for the line-item workflow element.</span></span>

## <a name="specify-whether-the-same-workflow-is-used-to-process-all-line-items"></a><span data-ttu-id="fe061-111">Aynı iş akışının tüm satır maddelerini işlemek için kullanılıp kullanılmayacağını belirtin</span><span class="sxs-lookup"><span data-stu-id="fe061-111">Specify whether the same workflow is used to process all line items</span></span>
<span data-ttu-id="fe061-112">Aynı iş akışının bir belgedeki tüm satır maddelerini işlemek için kullanılıp kullanılmayacağını belirtmek için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="fe061-112">Follow these steps to specify whether the same workflow is used to process all the line items on a document.</span></span>

1.  <span data-ttu-id="fe061-113">Sol bölmede **Temel Ayarlar**'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="fe061-113">In the left pane, click **Basic Settings**.</span></span>
2.  <span data-ttu-id="fe061-114">Belgedeki tüm satır maddelerini aynı iş akışının işlemesi gerekiyorsa **Tüm satır maddeleri için tek bir iş akışı çağır**'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="fe061-114">If the same workflow should process all the line items on a document, click **Invoke a single workflow for all line-items**.</span></span> <span data-ttu-id="fe061-115">Ardından satır maddelerini işlemek için kullanılacak iş akışını seçin.</span><span class="sxs-lookup"><span data-stu-id="fe061-115">Then select the workflow to use to process the line items.</span></span>
3.  <span data-ttu-id="fe061-116">Belirli bir koşul kümesini karşılayan satır maddelerini belirli bir iş akışının işlemesi gerekiyorsa **Her satır maddesi için bir iş akışı çağır**'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="fe061-116">If a specific workflow should process line items that meet a specific set of conditions, click **Invoke a workflow for each line-item**.</span></span> <span data-ttu-id="fe061-117">Ardından koşul kümesini tanımlamak için bu adımları izleyin:</span><span class="sxs-lookup"><span data-stu-id="fe061-117">Then follow these steps to define the set of conditions:</span></span>
    1.  <span data-ttu-id="fe061-118">**Ekle** öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="fe061-118">Click **Add**.</span></span>
    2.  <span data-ttu-id="fe061-119">Tablodaki koşulu seçin.</span><span class="sxs-lookup"><span data-stu-id="fe061-119">Select the condition in the table.</span></span>
    3.  <span data-ttu-id="fe061-120">**Koşul adı** sekmesinde tanımlamakta olduğunuz koşul kümesi için bir ad girin.</span><span class="sxs-lookup"><span data-stu-id="fe061-120">On the **Condition name** tab, enter a name for the set of conditions that you're defining.</span></span>
    4.  <span data-ttu-id="fe061-121">Koşulu girmek için **Koşul ekle**'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="fe061-121">Click **Add condition** to enter a condition.</span></span>
    5.  <span data-ttu-id="fe061-122">Varsa, gerekli ek koşulları girin.</span><span class="sxs-lookup"><span data-stu-id="fe061-122">Enter any additional conditions that are required.</span></span>
    6.  <span data-ttu-id="fe061-123">Girdiğiniz koşul kümesinin doğru biçimde yapılandırıldığını doğrulamak için, **Sına**'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="fe061-123">To verify that the set of conditions that you entered is configured correctly, click **Test**.</span></span> <span data-ttu-id="fe061-124">**Sınama iş akışı koşulu** sayfasında, **Koşulu doğrula** alanında, bir kayıt seçin ve ardından **Sına**'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="fe061-124">On the **Test workflow condition** page, in the **Validate condition** area, select a record, and then click **Test**.</span></span> <span data-ttu-id="fe061-125">Sistem, belirtmiş olduğunuz koşullarını yerine getirip getirmediğini belirlemek için kaydı değerlendirir.</span><span class="sxs-lookup"><span data-stu-id="fe061-125">The system evaluates the record to determine whether it meets the conditions that you defined.</span></span> <span data-ttu-id="fe061-126">**Özellikler** sayfasında geri dönmek için **OK** ya da **İptal Et**'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="fe061-126">Click **OK** or **Cancel** to return to the **Properties** page.</span></span>

    <span data-ttu-id="fe061-127">**İş akışı** sekmesinde tanımladığınız koşul kümesini karşılayan satır maddelerini işlemek için kullanılacak iş akışını seçin.</span><span class="sxs-lookup"><span data-stu-id="fe061-127">On the **Workflow** tab, select the workflow select the workflow to use to process line items that meet the set of conditions that you defined.</span></span>





