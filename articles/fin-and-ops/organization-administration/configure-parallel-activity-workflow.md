---
title: İş akışında paralel etkinlikleri yapılandırma
description: Paralel faaliyet yapılandırmak için iş akışı düzenleyicisinde aşağıdaki yordamları tamamlayın.
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
ms.custom: 195753
ms.assetid: 6d0656df-b5af-4001-96e6-6f0fcc44d022
ms.search.region: Global
ms.author: donaldc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 01c1fa876dd66ba6f0e1cdcecff56f424e117bd9
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2019
ms.locfileid: "308449"
---
# <a name="configure-parallel-activities-in-a-workflow"></a><span data-ttu-id="70a2f-103">İş akışında paralel etkinlikleri yapılandırma</span><span class="sxs-lookup"><span data-stu-id="70a2f-103">Configure parallel activities in a workflow</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="70a2f-104">Paralel faaliyet yapılandırmak için iş akışı düzenleyicisinde aşağıdaki yordamları tamamlayın.</span><span class="sxs-lookup"><span data-stu-id="70a2f-104">To configure a parallel activity, complete the following procedures in the workflow editor.</span></span>

<span data-ttu-id="70a2f-105">Paralel faaliyet aynı anda çalışan iş akışı dallarından oluşur.</span><span class="sxs-lookup"><span data-stu-id="70a2f-105">A parallel activity consists of workflow branches that run at the same time.</span></span>

## <a name="name-a-parallel-activity"></a><span data-ttu-id="70a2f-106">Paralel faaliyete ad verme</span><span class="sxs-lookup"><span data-stu-id="70a2f-106">Name a parallel activity</span></span>

<span data-ttu-id="70a2f-107">Paralel faaliyete bir ad vermek için aşağıdaki adımları uygulayın.</span><span class="sxs-lookup"><span data-stu-id="70a2f-107">Follow these steps to enter a name for a parallel activity.</span></span>

1. <span data-ttu-id="70a2f-108">Paralel faaliyete sağ tıklayın ve ardından **Özellikler** formunu açmak için **Özellikler**'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="70a2f-108">Right-click the parallel activity, and then click **Properties** to open the **Properties** form.</span></span>
2. <span data-ttu-id="70a2f-109">Sol bölmede **Temel Ayarlar**'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="70a2f-109">In the left pane, click **Basic Settings**.</span></span>
3. <span data-ttu-id="70a2f-110">Paralel faaliyet için **Ad** alanına benzersiz bir ad girin.</span><span class="sxs-lookup"><span data-stu-id="70a2f-110">In the **Name** field, enter a unique name for the parallel activity.</span></span>
4. <span data-ttu-id="70a2f-111">**Kapat**'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="70a2f-111">Click **Close**.</span></span>

## <a name="configure-the-branches-of-a-parallel-activity"></a><span data-ttu-id="70a2f-112">Paralel faaliyetin dallarını yapılandırma</span><span class="sxs-lookup"><span data-stu-id="70a2f-112">Configure the branches of a parallel activity</span></span>

<span data-ttu-id="70a2f-113">Bu paralel faaliyete dal eklemek ve paralel faaliyetin dallarını yapılandırmak için bu adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="70a2f-113">Follow these steps to add and configure the branches of this parallel activity.</span></span>

1. <span data-ttu-id="70a2f-114">Paralel faaliyetin dallarını görüntülemek için paralel faaliyete çift tıklayın.</span><span class="sxs-lookup"><span data-stu-id="70a2f-114">Double-click the parallel activity to display the branches of the parallel activity.</span></span>
2. <span data-ttu-id="70a2f-115">Dal eklemek için **İş akışı öğeleri** alanından **Dal** öğesini tuval üzerinde bir ekleme noktasına sürükleyin.</span><span class="sxs-lookup"><span data-stu-id="70a2f-115">To add a branch, drag the **Branch** element from the **Workflow elements** area to an insertion point on the canvas.</span></span> <span data-ttu-id="70a2f-116">Aşağıdaki şekil bir ekleme noktasını gösterir.</span><span class="sxs-lookup"><span data-stu-id="70a2f-116">The following figure shows an insertion point.</span></span>

    ![Ekleme noktası](./media/workflow_insertionpoint.gif)

    > [!NOTE]
    > <span data-ttu-id="70a2f-118">Paralel faaliyetin tüm dalları aynı anda çalıştığından dalların sırası önemli değildir.</span><span class="sxs-lookup"><span data-stu-id="70a2f-118">The order of the branches is not important because all the branches of a parallel activity run at the same time.</span></span>

3. <span data-ttu-id="70a2f-119">Her bir dalı yapılandırmak için bkz. [Paralel dal yapılandırma](configure-parallel-branch-workflow.md).</span><span class="sxs-lookup"><span data-stu-id="70a2f-119">To configure each branch, see [Configure a parallel branch](configure-parallel-branch-workflow.md).</span></span>
