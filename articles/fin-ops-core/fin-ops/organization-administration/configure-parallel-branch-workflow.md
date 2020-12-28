---
title: İş akışında paralel dalları yapılandırma
description: Paralel dal yapılandırmak için iş akışı düzenleyicisinde aşağıdaki yordamları tamamlayın.
author: ChrisGarty
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: sericks
ms.custom: 196043
ms.assetid: dfdae2b8-6a4f-4760-b339-b755c66f3f89
ms.search.region: Global
ms.author: cgarty
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e67a2c7cde3a3b6d1dcfcc2ccdd3255d30ac40b8
ms.sourcegitcommit: f5e31c34640add6d40308ac1365cc0ee60e60e24
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 12/08/2020
ms.locfileid: "4693342"
---
# <a name="configure-parallel-branches-in-a-workflow"></a><span data-ttu-id="3adc6-103">İş akışında paralel dalları yapılandırma</span><span class="sxs-lookup"><span data-stu-id="3adc6-103">Configure parallel branches in a workflow</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="3adc6-104">Paralel dal yapılandırmak için iş akışı düzenleyicisinde aşağıdaki yordamları tamamlayın.</span><span class="sxs-lookup"><span data-stu-id="3adc6-104">To configure a parallel branch, complete the following procedures in the workflow editor.</span></span>

<span data-ttu-id="3adc6-105">Paralel dal temel olarak bir ana iş akışı bağlamında çalışan bir iş akışıdır.</span><span class="sxs-lookup"><span data-stu-id="3adc6-105">A parallel branch is essentially a workflow that runs in the context of a parent workflow.</span></span>

## <a name="name-a-branch"></a><span data-ttu-id="3adc6-106">Dala ad verme</span><span class="sxs-lookup"><span data-stu-id="3adc6-106">Name a branch</span></span>

<span data-ttu-id="3adc6-107">Paralel dala bir ad vermek için aşağıdaki adımları uygulayın.</span><span class="sxs-lookup"><span data-stu-id="3adc6-107">Follow these steps to enter a name for a parallel branch.</span></span>

1. <span data-ttu-id="3adc6-108">Paralel dala sağ tıklayın ve ardından **Özellikler** seçeneğine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="3adc6-108">Right-click the parallel branch, and then click **Properties**.</span></span> <span data-ttu-id="3adc6-109">**Özellikler** formu görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="3adc6-109">The **Properties** form is displayed.</span></span>
2. <span data-ttu-id="3adc6-110">Sol bölmede **Temel Ayarlar**'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="3adc6-110">In the left pane, click **Basic Settings**.</span></span>
3. <span data-ttu-id="3adc6-111">Paralel dal için **Ad** alanına benzersiz bir ad girin.</span><span class="sxs-lookup"><span data-stu-id="3adc6-111">In the **Name** field, enter a unique name for the parallel branch.</span></span>
4. <span data-ttu-id="3adc6-112">**Kapat**'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="3adc6-112">Click **Close**.</span></span>

## <a name="design-and-configure-the-elements-of-a-branch"></a><span data-ttu-id="3adc6-113">Dalın öğelerini tasarlama ve yapılandırma</span><span class="sxs-lookup"><span data-stu-id="3adc6-113">Design and configure the elements of a branch</span></span>

<span data-ttu-id="3adc6-114">Paralel bir dalın öğelerini tasarlamak ve yapılandırmak için bu adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="3adc6-114">Follow these steps to design and configure the elements of a parallel branch.</span></span>

1. <span data-ttu-id="3adc6-115">Paralel dala çift tıklayın.</span><span class="sxs-lookup"><span data-stu-id="3adc6-115">Double-click the parallel branch.</span></span>
2. <span data-ttu-id="3adc6-116">İş akışı öğelerini tuvale sürükleyin ve ardından başka herhangi bir iş akışını oluşturur gibi öğeleri yapılandırın.</span><span class="sxs-lookup"><span data-stu-id="3adc6-116">Drag workflow elements onto the canvas, and then configure the elements, just as you would to create any other workflow.</span></span> <span data-ttu-id="3adc6-117">Daha fazla bilgi için bkz. [İş akışı oluşturmaya genel bakış](create-workflow.md).</span><span class="sxs-lookup"><span data-stu-id="3adc6-117">For more information, see [Create workflows overview](create-workflow.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="3adc6-118">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="3adc6-118">Additional resources</span></span>

[<span data-ttu-id="3adc6-119">İş akışlarına genel bakış</span><span class="sxs-lookup"><span data-stu-id="3adc6-119">Create workflows overview</span></span>](create-workflow.md)
