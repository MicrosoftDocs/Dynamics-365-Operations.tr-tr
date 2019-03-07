---
title: Kanban durumunu güncelleştirme
description: Yanlışlıkla bir kanban boşaltılırsa veya alınan bir kanbanın boşaltılması gerekiyorsa, kanban durumunu güncelleştirmeniz gerekir.
author: ChristianRytt
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: Kanban, KanbanResetEmpty
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 1d069414829518c8c952a0e7a74cd0ae4f24c450
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2019
ms.locfileid: "346284"
---
# <a name="update-kanban-status"></a><span data-ttu-id="6e841-103">Kanban durumunu güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="6e841-103">Update kanban status</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="6e841-104">Yanlışlıkla bir kanban boşaltılırsa veya alınan bir kanbanın boşaltılması gerekiyorsa, kanban durumunu güncelleştirmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="6e841-104">When a kanban is emptied by mistake or a received kanban needs to be emptied, you need to update kanban status.</span></span> <span data-ttu-id="6e841-105">Bu yöntemi oluşturmak için kullanılan demo veri şirketi USMF'dir.</span><span class="sxs-lookup"><span data-stu-id="6e841-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="6e841-106">Bu prosedür, mağaza denetleyicisi için hazırlanmıştır.</span><span class="sxs-lookup"><span data-stu-id="6e841-106">This procedure is intended for the shop supervisor.</span></span>


## <a name="find-the-kanban"></a><span data-ttu-id="6e841-107">Kanbanı bulun.</span><span class="sxs-lookup"><span data-stu-id="6e841-107">Find the kanban.</span></span>
1. <span data-ttu-id="6e841-108">Üretim denetimi > Kanban > Kanbanlar öğesine gidin.</span><span class="sxs-lookup"><span data-stu-id="6e841-108">Go to Production control > Kanban > Kanbans.</span></span>
2. <span data-ttu-id="6e841-109">İşleme ünitesi durumu sütun filtresini açın.</span><span class="sxs-lookup"><span data-stu-id="6e841-109">Open Handling unit status column filter.</span></span>
3. <span data-ttu-id="6e841-110">Temizle'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="6e841-110">Click Clear.</span></span>
    * <span data-ttu-id="6e841-111">Bu, filtreleri sıfırlar.</span><span class="sxs-lookup"><span data-stu-id="6e841-111">This resets the filters.</span></span>  
4. <span data-ttu-id="6e841-112">Kayıtları bulmak için Hızlı Filtre'yi kullanın.</span><span class="sxs-lookup"><span data-stu-id="6e841-112">Use the Quick Filter to find records.</span></span> <span data-ttu-id="6e841-113">Örneğin, Kart numarası alanını bir '000149' değeriyle filtreleyin.</span><span class="sxs-lookup"><span data-stu-id="6e841-113">For example, filter on the Card number field with a value of '000149'.</span></span>

## <a name="change-emptied-status-to-received-status"></a><span data-ttu-id="6e841-114">Boşaltıldı durumunu alındı olarak değiştirme</span><span class="sxs-lookup"><span data-stu-id="6e841-114">Change emptied status to received status</span></span>
1. <span data-ttu-id="6e841-115">Boş işleme ünitesini ters çevir düğmesini tıklayın.</span><span class="sxs-lookup"><span data-stu-id="6e841-115">Click Reverse empty handling unit.</span></span>
2. <span data-ttu-id="6e841-116">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="6e841-116">Click OK.</span></span>
    * <span data-ttu-id="6e841-117">İşlem ünitesi durumunun Alındı olduğuna dikkat edin.</span><span class="sxs-lookup"><span data-stu-id="6e841-117">Notice that the Handling unit status is Received.</span></span>  

## <a name="change-received-status-to-emptied-status"></a><span data-ttu-id="6e841-118">Alındı durumunu boşaltıldı olarak değiştirme</span><span class="sxs-lookup"><span data-stu-id="6e841-118">Change received status to emptied status</span></span>
1. <span data-ttu-id="6e841-119">Kanbanı boşaltı düğmesini tıklayın.</span><span class="sxs-lookup"><span data-stu-id="6e841-119">Click Empty kanban.</span></span>
2. <span data-ttu-id="6e841-120">Listede, seçili satırı işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="6e841-120">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="6e841-121">İşlem ünitesi durumunun Boşaltıldı olduğuna dikkat edin.</span><span class="sxs-lookup"><span data-stu-id="6e841-121">Notice that the Handling unit status is Emptied.</span></span>  

