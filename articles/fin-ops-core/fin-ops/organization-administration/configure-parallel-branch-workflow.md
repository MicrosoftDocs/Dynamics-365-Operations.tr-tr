---
title: İş akışında paralel dalları yapılandırma
description: Paralel dal yapılandırmak için iş akışı düzenleyicisinde aşağıdaki yordamları tamamlayın.
author: sericks007
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 196043
ms.assetid: dfdae2b8-6a4f-4760-b339-b755c66f3f89
ms.search.region: Global
ms.author: donaldc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2058eaac77282946559cae11fcec8152658fc96b
ms.sourcegitcommit: 57bc7e17682e2edb5e1766496b7a22f4621819dd
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/18/2019
ms.locfileid: "2811369"
---
# <a name="configure-parallel-branches-in-a-workflow"></a><span data-ttu-id="9b880-103">İş akışında paralel dalları yapılandırma</span><span class="sxs-lookup"><span data-stu-id="9b880-103">Configure parallel branches in a workflow</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="9b880-104">Paralel dal yapılandırmak için iş akışı düzenleyicisinde aşağıdaki yordamları tamamlayın.</span><span class="sxs-lookup"><span data-stu-id="9b880-104">To configure a parallel branch, complete the following procedures in the workflow editor.</span></span>

<span data-ttu-id="9b880-105">Paralel dal temel olarak bir ana iş akışı bağlamında çalışan bir iş akışıdır.</span><span class="sxs-lookup"><span data-stu-id="9b880-105">A parallel branch is essentially a workflow that runs in the context of a parent workflow.</span></span>

## <a name="name-a-branch"></a><span data-ttu-id="9b880-106">Dala ad verme</span><span class="sxs-lookup"><span data-stu-id="9b880-106">Name a branch</span></span>

<span data-ttu-id="9b880-107">Paralel dala bir ad vermek için aşağıdaki adımları uygulayın.</span><span class="sxs-lookup"><span data-stu-id="9b880-107">Follow these steps to enter a name for a parallel branch.</span></span>

1. <span data-ttu-id="9b880-108">Paralel dala sağ tıklayın ve ardından **Özellikler** seçeneğine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="9b880-108">Right-click the parallel branch, and then click **Properties**.</span></span> <span data-ttu-id="9b880-109">**Özellikler** formu görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="9b880-109">The **Properties** form is displayed.</span></span>
2. <span data-ttu-id="9b880-110">Sol bölmede **Temel Ayarlar**'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="9b880-110">In the left pane, click **Basic Settings**.</span></span>
3. <span data-ttu-id="9b880-111">Paralel dal için **Ad** alanına benzersiz bir ad girin.</span><span class="sxs-lookup"><span data-stu-id="9b880-111">In the **Name** field, enter a unique name for the parallel branch.</span></span>
4. <span data-ttu-id="9b880-112">**Kapat**'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="9b880-112">Click **Close**.</span></span>

## <a name="design-and-configure-the-elements-of-a-branch"></a><span data-ttu-id="9b880-113">Dalın öğelerini tasarlama ve yapılandırma</span><span class="sxs-lookup"><span data-stu-id="9b880-113">Design and configure the elements of a branch</span></span>

<span data-ttu-id="9b880-114">Paralel bir dalın öğelerini tasarlamak ve yapılandırmak için bu adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="9b880-114">Follow these steps to design and configure the elements of a parallel branch.</span></span>

1. <span data-ttu-id="9b880-115">Paralel dala çift tıklayın.</span><span class="sxs-lookup"><span data-stu-id="9b880-115">Double-click the parallel branch.</span></span>
2. <span data-ttu-id="9b880-116">İş akışı öğelerini tuvale sürükleyin ve ardından başka herhangi bir iş akışını oluşturur gibi öğeleri yapılandırın.</span><span class="sxs-lookup"><span data-stu-id="9b880-116">Drag workflow elements onto the canvas, and then configure the elements, just as you would to create any other workflow.</span></span> <span data-ttu-id="9b880-117">Daha fazla bilgi için bkz. [İş akışı oluşturmaya genel bakış](create-workflow.md).</span><span class="sxs-lookup"><span data-stu-id="9b880-117">For more information, see [Create workflows overview](create-workflow.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="9b880-118">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="9b880-118">Additional resources</span></span>

[<span data-ttu-id="9b880-119">İş akışlarına genel bakış</span><span class="sxs-lookup"><span data-stu-id="9b880-119">Create workflows overview</span></span>](create-workflow.md)
