---
title: "İş akışında paralel dalları yapılandırma"
description: "Paralel dal yapılandırmak için iş akışı düzenleyicisinde aşağıdaki yordamları tamamlayın."
author: sericks007
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 196043
ms.assetid: dfdae2b8-6a4f-4760-b339-b755c66f3f89
ms.search.region: Global
ms.author: donaldc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 3ee5334c87b2b0acae2afa6882feca63e3b9cc8e
ms.openlocfilehash: 73626ad21dfe2be7400f321a3eee272c896276f3
ms.contentlocale: tr-tr
ms.lasthandoff: 12/18/2018

---

# <a name="configure-parallel-branches-in-a-workflow"></a><span data-ttu-id="c79ad-103">İş akışında paralel dalları yapılandırma</span><span class="sxs-lookup"><span data-stu-id="c79ad-103">Configure parallel branches in a workflow</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c79ad-104">Paralel dal yapılandırmak için iş akışı düzenleyicisinde aşağıdaki yordamları tamamlayın.</span><span class="sxs-lookup"><span data-stu-id="c79ad-104">To configure a parallel branch, complete the following procedures in the workflow editor.</span></span>

<span data-ttu-id="c79ad-105">Paralel dal temel olarak bir ana iş akışı bağlamında çalışan bir iş akışıdır.</span><span class="sxs-lookup"><span data-stu-id="c79ad-105">A parallel branch is essentially a workflow that runs in the context of a parent workflow.</span></span>

## <a name="name-a-branch"></a><span data-ttu-id="c79ad-106">Dala ad verme</span><span class="sxs-lookup"><span data-stu-id="c79ad-106">Name a branch</span></span>

<span data-ttu-id="c79ad-107">Paralel dala bir ad vermek için aşağıdaki adımları uygulayın.</span><span class="sxs-lookup"><span data-stu-id="c79ad-107">Follow these steps to enter a name for a parallel branch.</span></span>

1. <span data-ttu-id="c79ad-108">Paralel dala sağ tıklayın ve ardından **Özellikler** seçeneğine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="c79ad-108">Right-click the parallel branch, and then click **Properties**.</span></span> <span data-ttu-id="c79ad-109">**Özellikler** formu görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="c79ad-109">The **Properties** form is displayed.</span></span>
2. <span data-ttu-id="c79ad-110">Sol bölmede **Temel Ayarlar**'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="c79ad-110">In the left pane, click **Basic Settings**.</span></span>
3. <span data-ttu-id="c79ad-111">Paralel dal için **Ad** alanına benzersiz bir ad girin.</span><span class="sxs-lookup"><span data-stu-id="c79ad-111">In the **Name** field, enter a unique name for the parallel branch.</span></span>
4. <span data-ttu-id="c79ad-112">**Kapat**'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="c79ad-112">Click **Close**.</span></span>

## <a name="design-and-configure-the-elements-of-a-branch"></a><span data-ttu-id="c79ad-113">Dalın öğelerini tasarlama ve yapılandırma</span><span class="sxs-lookup"><span data-stu-id="c79ad-113">Design and configure the elements of a branch</span></span>

<span data-ttu-id="c79ad-114">Paralel bir dalın öğelerini tasarlamak ve yapılandırmak için bu adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="c79ad-114">Follow these steps to design and configure the elements of a parallel branch.</span></span>

1. <span data-ttu-id="c79ad-115">Paralel dala çift tıklayın.</span><span class="sxs-lookup"><span data-stu-id="c79ad-115">Double-click the parallel branch.</span></span>
2. <span data-ttu-id="c79ad-116">İş akışı öğelerini tuvale sürükleyin ve ardından başka herhangi bir iş akışını oluşturur gibi öğeleri yapılandırın.</span><span class="sxs-lookup"><span data-stu-id="c79ad-116">Drag workflow elements onto the canvas, and then configure the elements, just as you would to create any other workflow.</span></span> <span data-ttu-id="c79ad-117">Daha fazla bilgi için bkz. [İş akışı oluşturma](create-workflow.md).</span><span class="sxs-lookup"><span data-stu-id="c79ad-117">For more information, see [Create a workflow](create-workflow.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="c79ad-118">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="c79ad-118">Additional resources</span></span>

[<span data-ttu-id="c79ad-119">İş akışı oluşturma</span><span class="sxs-lookup"><span data-stu-id="c79ad-119">Create a workflow</span></span>](create-workflow.md)

