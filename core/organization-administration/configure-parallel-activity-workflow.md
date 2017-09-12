---
title: "Bir iş akışında bir paralel etkinlik yapılandırma"
description: "Paralel faaliyet yapılandırmak için iş akışı düzenleyicisinde aşağıdaki yordamları tamamlayın."
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
ms.custom: 195753
ms.assetid: 6d0656df-b5af-4001-96e6-6f0fcc44d022
ms.search.region: Global
ms.author: donaldc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 08c38aada355583c5a6872f75b57db95d9b81786
ms.openlocfilehash: 5473327c0665c9183746eb8125c7a368fbedc21e
ms.contentlocale: tr-tr
ms.lasthandoff: 07/18/2017

---

# <a name="configure-a-parallel-activity-in-a-workflow"></a><span data-ttu-id="d80f9-103">Bir iş akışında bir paralel etkinlik yapılandırma</span><span class="sxs-lookup"><span data-stu-id="d80f9-103">Configure a parallel activity in a workflow</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="d80f9-104">Paralel faaliyet yapılandırmak için iş akışı düzenleyicisinde aşağıdaki yordamları tamamlayın.</span><span class="sxs-lookup"><span data-stu-id="d80f9-104">To configure a parallel activity, complete the following procedures in the workflow editor.</span></span>

<span data-ttu-id="d80f9-105">Paralel faaliyet aynı anda çalışan iş akışı dallarından oluşur.</span><span class="sxs-lookup"><span data-stu-id="d80f9-105">A parallel activity consists of workflow branches that run at the same time.</span></span>

## <a name="name-a-parallel-activity"></a><span data-ttu-id="d80f9-106">Paralel faaliyete ad verme</span><span class="sxs-lookup"><span data-stu-id="d80f9-106">Name a parallel activity</span></span>
<span data-ttu-id="d80f9-107">Paralel faaliyete bir ad vermek için aşağıdaki adımları uygulayın.</span><span class="sxs-lookup"><span data-stu-id="d80f9-107">Follow these steps to enter a name for a parallel activity.</span></span>
1.  <span data-ttu-id="d80f9-108">Paralel faaliyete sağ tıklayın ve ardından **Özellikler** formunu açmak için **Özellikler**'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="d80f9-108">Right-click the parallel activity, and then click **Properties** to open the **Properties** form.</span></span>
2.  <span data-ttu-id="d80f9-109">Sol bölmede **Temel Ayarlar**'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="d80f9-109">In the left pane, click **Basic Settings**.</span></span>
3.  <span data-ttu-id="d80f9-110">Paralel faaliyet için **Ad** alanına benzersiz bir ad girin.</span><span class="sxs-lookup"><span data-stu-id="d80f9-110">In the **Name** field, enter a unique name for the parallel activity.</span></span>
4.  <span data-ttu-id="d80f9-111">**Kapat**'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="d80f9-111">Click **Close**.</span></span>

## <a name="configure-the-branches-of-a-parallel-activity"></a><span data-ttu-id="d80f9-112">Paralel faaliyetin dallarını yapılandırma</span><span class="sxs-lookup"><span data-stu-id="d80f9-112">Configure the branches of a parallel activity</span></span>
<span data-ttu-id="d80f9-113">Bu paralel faaliyete dal eklemek ve paralel faaliyetin dallarını yapılandırmak için bu adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="d80f9-113">Follow these steps to add and configure the branches of this parallel activity.</span></span>
1.  <span data-ttu-id="d80f9-114">Paralel faaliyetin dallarını görüntülemek için paralel faaliyete çift tıklayın.</span><span class="sxs-lookup"><span data-stu-id="d80f9-114">Double-click the parallel activity to display the branches of the parallel activity.</span></span>
2.  <span data-ttu-id="d80f9-115">Dal eklemek için **İş akışı öğeleri** alanından **Dal** öğesini tuval üzerinde bir ekleme noktasına sürükleyin.</span><span class="sxs-lookup"><span data-stu-id="d80f9-115">To add a branch, drag the **Branch** element from the **Workflow elements** area to an insertion point on the canvas.</span></span> <span data-ttu-id="d80f9-116">Aşağıdaki şekil bir ekleme noktasını gösterir.![Ekleme noktası](./media/workflow_insertionpoint.gif)</span><span class="sxs-lookup"><span data-stu-id="d80f9-116">The following figure shows an insertion point.![Insertion point](./media/workflow_insertionpoint.gif)</span></span>
    | <span data-ttu-id="d80f9-117">**Not**</span><span class="sxs-lookup"><span data-stu-id="d80f9-117">**Note**</span></span>                                                                                                         |
    |------------------------------------------------------------------------------------------------------------------|
    | <span data-ttu-id="d80f9-118">Paralel faaliyetin tüm dalları aynı anda çalıştığından dalların sırası önemli değildir.</span><span class="sxs-lookup"><span data-stu-id="d80f9-118">The order of the branches is not important because all the branches of a parallel activity run at the same time.</span></span> |

3.  <span data-ttu-id="d80f9-119">Her bir dalı yapılandırmak için bkz. [Paralel dal yapılandırma](configure-parallel-branch-workflow.md).</span><span class="sxs-lookup"><span data-stu-id="d80f9-119">To configure each branch, see [Configure a parallel branch](configure-parallel-branch-workflow.md).</span></span>






