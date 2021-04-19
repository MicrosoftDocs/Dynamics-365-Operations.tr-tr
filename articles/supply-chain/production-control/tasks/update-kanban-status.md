---
title: Kanban durumunu güncelleştirme
description: Yanlışlıkla bir kanban boşaltılırsa veya alınan bir kanbanın boşaltılması gerekiyorsa, kanban durumunu güncelleştirmeniz gerekir.
author: ChristianRytt
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: Kanban, KanbanResetEmpty
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 5a0e03da4671ffec4ecf4835b20a00ef87971c94
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/01/2021
ms.locfileid: "5831830"
---
# <a name="update-kanban-status"></a><span data-ttu-id="d96d7-103">Kanban durumunu güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="d96d7-103">Update kanban status</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="d96d7-104">Yanlışlıkla bir kanban boşaltılırsa veya alınan bir kanbanın boşaltılması gerekiyorsa, kanban durumunu güncelleştirmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="d96d7-104">When a kanban is emptied by mistake or a received kanban needs to be emptied, you need to update kanban status.</span></span> <span data-ttu-id="d96d7-105">Bu yöntemi oluşturmak için kullanılan demo veri şirketi USMF'dir.</span><span class="sxs-lookup"><span data-stu-id="d96d7-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="d96d7-106">Bu prosedür, mağaza denetleyicisi için hazırlanmıştır.</span><span class="sxs-lookup"><span data-stu-id="d96d7-106">This procedure is intended for the shop supervisor.</span></span>


## <a name="find-the-kanban"></a><span data-ttu-id="d96d7-107">Kanbanı bulun.</span><span class="sxs-lookup"><span data-stu-id="d96d7-107">Find the kanban.</span></span>
1. <span data-ttu-id="d96d7-108">Üretim denetimi > Kanban > Kanbanlar öğesine gidin.</span><span class="sxs-lookup"><span data-stu-id="d96d7-108">Go to Production control > Kanban > Kanbans.</span></span>
2. <span data-ttu-id="d96d7-109">İşleme ünitesi durumu sütun filtresini açın.</span><span class="sxs-lookup"><span data-stu-id="d96d7-109">Open Handling unit status column filter.</span></span>
3. <span data-ttu-id="d96d7-110">Temizle'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="d96d7-110">Click Clear.</span></span>
    * <span data-ttu-id="d96d7-111">Bu, filtreleri sıfırlar.</span><span class="sxs-lookup"><span data-stu-id="d96d7-111">This resets the filters.</span></span>  
4. <span data-ttu-id="d96d7-112">Kayıtları bulmak için Hızlı Filtre'yi kullanın.</span><span class="sxs-lookup"><span data-stu-id="d96d7-112">Use the Quick Filter to find records.</span></span> <span data-ttu-id="d96d7-113">Örneğin, Kart numarası alanını bir '000149' değeriyle filtreleyin.</span><span class="sxs-lookup"><span data-stu-id="d96d7-113">For example, filter on the Card number field with a value of '000149'.</span></span>

## <a name="change-emptied-status-to-received-status"></a><span data-ttu-id="d96d7-114">Boşaltıldı durumunu alındı olarak değiştirme</span><span class="sxs-lookup"><span data-stu-id="d96d7-114">Change emptied status to received status</span></span>
1. <span data-ttu-id="d96d7-115">Boş işleme ünitesini ters çevir düğmesini tıklayın.</span><span class="sxs-lookup"><span data-stu-id="d96d7-115">Click Reverse empty handling unit.</span></span>
2. <span data-ttu-id="d96d7-116">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="d96d7-116">Click OK.</span></span>
    * <span data-ttu-id="d96d7-117">İşlem ünitesi durumunun Alındı olduğuna dikkat edin.</span><span class="sxs-lookup"><span data-stu-id="d96d7-117">Notice that the Handling unit status is Received.</span></span>  

## <a name="change-received-status-to-emptied-status"></a><span data-ttu-id="d96d7-118">Alındı durumunu boşaltıldı olarak değiştirme</span><span class="sxs-lookup"><span data-stu-id="d96d7-118">Change received status to emptied status</span></span>
1. <span data-ttu-id="d96d7-119">Kanbanı boşaltı düğmesini tıklayın.</span><span class="sxs-lookup"><span data-stu-id="d96d7-119">Click Empty kanban.</span></span>
2. <span data-ttu-id="d96d7-120">Listede, seçili satırı işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="d96d7-120">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="d96d7-121">İşlem ünitesi durumunun Boşaltıldı olduğuna dikkat edin.</span><span class="sxs-lookup"><span data-stu-id="d96d7-121">Notice that the Handling unit status is Emptied.</span></span>  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]