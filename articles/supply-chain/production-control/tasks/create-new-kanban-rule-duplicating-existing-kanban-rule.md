---
title: Mevcut bir kuralı çoğaltarak yeni bir kanban kuralı oluşturma
description: Bu yordam, varolan bir kanban kuralının kopyasını oluşturmaya odaklanır.
author: ChristianRytt
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KanbanRules, KanbanRuleDuplicate, InventItemIdLookupSimple
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 3b89fca4e55aa852bd127eb9b1bda07c0e5bcdc0
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5255145"
---
# <a name="create-a-new-kanban-rule-by-duplicating-an-existing-kanban-rule"></a><span data-ttu-id="b4e0f-103">Mevcut bir kuralı çoğaltarak yeni bir kanban kuralı oluşturma</span><span class="sxs-lookup"><span data-stu-id="b4e0f-103">Create a new kanban rule by duplicating an existing kanban rule</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="b4e0f-104">Bu yordam, varolan bir kanban kuralının kopyasını oluşturmaya odaklanır.</span><span class="sxs-lookup"><span data-stu-id="b4e0f-104">This procedure focuses on creating a duplicate of an existing kanban rule.</span></span> <span data-ttu-id="b4e0f-105">Varolan kanban kurallara dayalı yeni kanban kurallar oluşturmak istiyorsanız yararlıdır.</span><span class="sxs-lookup"><span data-stu-id="b4e0f-105">This is useful if you want to create new kanban rules based on existing kanban rules.</span></span> <span data-ttu-id="b4e0f-106">Bu yöntemi oluşturmak için kullanılan demo veri şirketi USMF'dir.</span><span class="sxs-lookup"><span data-stu-id="b4e0f-106">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="b4e0f-107">Bu yordam, değiştirilmiş bir üretim akışı ve yeni bir yenileme kuralı hazırlanırken kullanılması için işlem mühendisi veya değer akışı yöneticisi için hazırlanmıştır.</span><span class="sxs-lookup"><span data-stu-id="b4e0f-107">This procedure is intended for the process engineer or the value stream manager as they prepare production for a changed production flow or a new replenishment rule.</span></span>


## <a name="select-a-kanban-rule"></a><span data-ttu-id="b4e0f-108">Bir kanban kuralı seç</span><span class="sxs-lookup"><span data-stu-id="b4e0f-108">Select a kanban rule</span></span>
1. <span data-ttu-id="b4e0f-109">Kanban kuralları'na gidin.</span><span class="sxs-lookup"><span data-stu-id="b4e0f-109">Go to Kanban rules.</span></span>
2. <span data-ttu-id="b4e0f-110">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="b4e0f-110">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="b4e0f-111">M0006 ürünü için 000017 kanban kuralını seçin.</span><span class="sxs-lookup"><span data-stu-id="b4e0f-111">Select kanban rule 000017 for Product M0006.</span></span>  

## <a name="duplicate-a-kanban-rule"></a><span data-ttu-id="b4e0f-112">Bir kanban kuralını çoğalt</span><span class="sxs-lookup"><span data-stu-id="b4e0f-112">Duplicate a kanban rule</span></span>
1. <span data-ttu-id="b4e0f-113">Kanban kuralını çoğalt'ı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="b4e0f-113">Click Duplicate kanban rule.</span></span>
    * <span data-ttu-id="b4e0f-114">Bir kanban kuralı çoğaltılırken türü, tarihleri, faaliyetleri ve ürün seçimini değiştirmek mümkündür.</span><span class="sxs-lookup"><span data-stu-id="b4e0f-114">When duplicating a kanban rule, it is possible to change type, dates, activities, and the product selection.</span></span> <span data-ttu-id="b4e0f-115">Sonraki adımda bu yordam için ürünü değiştirin.</span><span class="sxs-lookup"><span data-stu-id="b4e0f-115">Change the product for this procedure in the next step.</span></span>  
2. <span data-ttu-id="b4e0f-116">Ürün alanında bir değer girin veya bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="b4e0f-116">In the Product field, enter or select a value.</span></span>
    * <span data-ttu-id="b4e0f-117">M0007 öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="b4e0f-117">Select M0007.</span></span>  
3. <span data-ttu-id="b4e0f-118">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="b4e0f-118">Click OK.</span></span>
    * <span data-ttu-id="b4e0f-119">000017 kanban kuralının bir kopyasının oluşturulduğunu unutmayın.</span><span class="sxs-lookup"><span data-stu-id="b4e0f-119">Note that a duplicate of kanban rule 000017 is created.</span></span>    



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]