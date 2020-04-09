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
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 48dd5c3a878efb7413f461e76fde086030015b60
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/18/2020
ms.locfileid: "3146687"
---
# <a name="update-kanban-status"></a><span data-ttu-id="2b67c-103">Kanban durumunu güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="2b67c-103">Update kanban status</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="2b67c-104">Yanlışlıkla bir kanban boşaltılırsa veya alınan bir kanbanın boşaltılması gerekiyorsa, kanban durumunu güncelleştirmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="2b67c-104">When a kanban is emptied by mistake or a received kanban needs to be emptied, you need to update kanban status.</span></span> <span data-ttu-id="2b67c-105">Bu yöntemi oluşturmak için kullanılan demo veri şirketi USMF'dir.</span><span class="sxs-lookup"><span data-stu-id="2b67c-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="2b67c-106">Bu prosedür, mağaza denetleyicisi için hazırlanmıştır.</span><span class="sxs-lookup"><span data-stu-id="2b67c-106">This procedure is intended for the shop supervisor.</span></span>


## <a name="find-the-kanban"></a><span data-ttu-id="2b67c-107">Kanbanı bulun.</span><span class="sxs-lookup"><span data-stu-id="2b67c-107">Find the kanban.</span></span>
1. <span data-ttu-id="2b67c-108">Üretim denetimi > Kanban > Kanbanlar öğesine gidin.</span><span class="sxs-lookup"><span data-stu-id="2b67c-108">Go to Production control > Kanban > Kanbans.</span></span>
2. <span data-ttu-id="2b67c-109">İşleme ünitesi durumu sütun filtresini açın.</span><span class="sxs-lookup"><span data-stu-id="2b67c-109">Open Handling unit status column filter.</span></span>
3. <span data-ttu-id="2b67c-110">Temizle'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="2b67c-110">Click Clear.</span></span>
    * <span data-ttu-id="2b67c-111">Bu, filtreleri sıfırlar.</span><span class="sxs-lookup"><span data-stu-id="2b67c-111">This resets the filters.</span></span>  
4. <span data-ttu-id="2b67c-112">Kayıtları bulmak için Hızlı Filtre'yi kullanın.</span><span class="sxs-lookup"><span data-stu-id="2b67c-112">Use the Quick Filter to find records.</span></span> <span data-ttu-id="2b67c-113">Örneğin, Kart numarası alanını bir '000149' değeriyle filtreleyin.</span><span class="sxs-lookup"><span data-stu-id="2b67c-113">For example, filter on the Card number field with a value of '000149'.</span></span>

## <a name="change-emptied-status-to-received-status"></a><span data-ttu-id="2b67c-114">Boşaltıldı durumunu alındı olarak değiştirme</span><span class="sxs-lookup"><span data-stu-id="2b67c-114">Change emptied status to received status</span></span>
1. <span data-ttu-id="2b67c-115">Boş işleme ünitesini ters çevir düğmesini tıklayın.</span><span class="sxs-lookup"><span data-stu-id="2b67c-115">Click Reverse empty handling unit.</span></span>
2. <span data-ttu-id="2b67c-116">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="2b67c-116">Click OK.</span></span>
    * <span data-ttu-id="2b67c-117">İşlem ünitesi durumunun Alındı olduğuna dikkat edin.</span><span class="sxs-lookup"><span data-stu-id="2b67c-117">Notice that the Handling unit status is Received.</span></span>  

## <a name="change-received-status-to-emptied-status"></a><span data-ttu-id="2b67c-118">Alındı durumunu boşaltıldı olarak değiştirme</span><span class="sxs-lookup"><span data-stu-id="2b67c-118">Change received status to emptied status</span></span>
1. <span data-ttu-id="2b67c-119">Kanbanı boşaltı düğmesini tıklayın.</span><span class="sxs-lookup"><span data-stu-id="2b67c-119">Click Empty kanban.</span></span>
2. <span data-ttu-id="2b67c-120">Listede, seçili satırı işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="2b67c-120">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="2b67c-121">İşlem ünitesi durumunun Boşaltıldı olduğuna dikkat edin.</span><span class="sxs-lookup"><span data-stu-id="2b67c-121">Notice that the Handling unit status is Emptied.</span></span>  

