---
title: Mevcut bir kuralı çoğaltarak yeni bir kanban kuralı oluşturma
description: Bu yordam, varolan bir kanban kuralının kopyasını oluşturmaya odaklanır.
author: ChristianRytt
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: KanbanRules, KanbanRuleDuplicate, InventItemIdLookupSimple
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d80bf0318234f858e51fb461894238894e01717c
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/01/2021
ms.locfileid: "5829078"
---
# <a name="create-a-new-kanban-rule-by-duplicating-an-existing-kanban-rule"></a><span data-ttu-id="0abb7-103">Mevcut bir kuralı çoğaltarak yeni bir kanban kuralı oluşturma</span><span class="sxs-lookup"><span data-stu-id="0abb7-103">Create a new kanban rule by duplicating an existing kanban rule</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="0abb7-104">Bu yordam, varolan bir kanban kuralının kopyasını oluşturmaya odaklanır.</span><span class="sxs-lookup"><span data-stu-id="0abb7-104">This procedure focuses on creating a duplicate of an existing kanban rule.</span></span> <span data-ttu-id="0abb7-105">Varolan kanban kurallara dayalı yeni kanban kurallar oluşturmak istiyorsanız yararlıdır.</span><span class="sxs-lookup"><span data-stu-id="0abb7-105">This is useful if you want to create new kanban rules based on existing kanban rules.</span></span> <span data-ttu-id="0abb7-106">Bu yöntemi oluşturmak için kullanılan demo veri şirketi USMF'dir.</span><span class="sxs-lookup"><span data-stu-id="0abb7-106">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="0abb7-107">Bu yordam, değiştirilmiş bir üretim akışı ve yeni bir yenileme kuralı hazırlanırken kullanılması için işlem mühendisi veya değer akışı yöneticisi için hazırlanmıştır.</span><span class="sxs-lookup"><span data-stu-id="0abb7-107">This procedure is intended for the process engineer or the value stream manager as they prepare production for a changed production flow or a new replenishment rule.</span></span>


## <a name="select-a-kanban-rule"></a><span data-ttu-id="0abb7-108">Bir kanban kuralı seç</span><span class="sxs-lookup"><span data-stu-id="0abb7-108">Select a kanban rule</span></span>
1. <span data-ttu-id="0abb7-109">Kanban kuralları'na gidin.</span><span class="sxs-lookup"><span data-stu-id="0abb7-109">Go to Kanban rules.</span></span>
2. <span data-ttu-id="0abb7-110">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="0abb7-110">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="0abb7-111">M0006 ürünü için 000017 kanban kuralını seçin.</span><span class="sxs-lookup"><span data-stu-id="0abb7-111">Select kanban rule 000017 for Product M0006.</span></span>  

## <a name="duplicate-a-kanban-rule"></a><span data-ttu-id="0abb7-112">Bir kanban kuralını çoğalt</span><span class="sxs-lookup"><span data-stu-id="0abb7-112">Duplicate a kanban rule</span></span>
1. <span data-ttu-id="0abb7-113">Kanban kuralını çoğalt'ı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="0abb7-113">Click Duplicate kanban rule.</span></span>
    * <span data-ttu-id="0abb7-114">Bir kanban kuralı çoğaltılırken türü, tarihleri, faaliyetleri ve ürün seçimini değiştirmek mümkündür.</span><span class="sxs-lookup"><span data-stu-id="0abb7-114">When duplicating a kanban rule, it is possible to change type, dates, activities, and the product selection.</span></span> <span data-ttu-id="0abb7-115">Sonraki adımda bu yordam için ürünü değiştirin.</span><span class="sxs-lookup"><span data-stu-id="0abb7-115">Change the product for this procedure in the next step.</span></span>  
2. <span data-ttu-id="0abb7-116">Ürün alanında bir değer girin veya bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="0abb7-116">In the Product field, enter or select a value.</span></span>
    * <span data-ttu-id="0abb7-117">M0007 öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="0abb7-117">Select M0007.</span></span>  
3. <span data-ttu-id="0abb7-118">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="0abb7-118">Click OK.</span></span>
    * <span data-ttu-id="0abb7-119">000017 kanban kuralının bir kopyasının oluşturulduğunu unutmayın.</span><span class="sxs-lookup"><span data-stu-id="0abb7-119">Note that a duplicate of kanban rule 000017 is created.</span></span>    



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]