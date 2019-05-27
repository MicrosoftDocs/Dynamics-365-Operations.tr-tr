---
title: Değiştirme kanban kuralı oluşturma
description: Bu prosedürde mevcut bir kanban kuralının belirli bir tarihte yeni bir kanban kuralıyla nasıl değiştirileceği açıklanmıştır.
author: ChristianRytt
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KanbanRules, KanbanRuleDuplicate
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: c8a9367d4796999857e473bcbe36a709d534f3b0
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/15/2019
ms.locfileid: "1564075"
---
# <a name="create-a-replacement-kanban-rule"></a><span data-ttu-id="38c4c-103">Değiştirme kanban kuralı oluşturma</span><span class="sxs-lookup"><span data-stu-id="38c4c-103">Create a replacement kanban rule</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="38c4c-104">Bu prosedürde mevcut bir kanban kuralının belirli bir tarihte yeni bir kanban kuralıyla nasıl değiştirileceği açıklanmıştır.</span><span class="sxs-lookup"><span data-stu-id="38c4c-104">This procedure focuses on replacing an existing kanban rule with a new kanban rule on a specific date.</span></span> <span data-ttu-id="38c4c-105">Bu, üretim akışındaki değişikliklerin veya stok yenileme kurallarının koordine edilmesi ve zamanlanması gerektiğinde kullanışlıdır.</span><span class="sxs-lookup"><span data-stu-id="38c4c-105">This is useful when changes in the production flow or replenishment rules need to be coordinated and scheduled.</span></span> <span data-ttu-id="38c4c-106">Prosedürün oluşturulması için kullanılan demo verisi şirketi USMF'dir.</span><span class="sxs-lookup"><span data-stu-id="38c4c-106">The demo data company used to create procedure is USMF.</span></span> <span data-ttu-id="38c4c-107">Bu yordam, değiştirilmiş bir üretim akışı ve yeni bir yenileme kuralı hazırlanırken kullanılması için işlem mühendisi veya değer akışı yöneticisi için hazırlanmıştır.</span><span class="sxs-lookup"><span data-stu-id="38c4c-107">This procedure is intended for the process engineer or the value stream manager when they prepare production for a changed production flow or a new replenishment rule.</span></span> <span data-ttu-id="38c4c-108">Bu görev, 000022 kanban kuralını yeni bir kuralla değiştirir ve 48 olan maksimum miktarı yeni kural için 100'e yükseltir.</span><span class="sxs-lookup"><span data-stu-id="38c4c-108">This task replaces kanban rule 000022 with a new rule and increases the maximum quantity from 48 to 100 for the new rule.</span></span>


## <a name="select-a-kanban-rule-to-replace"></a><span data-ttu-id="38c4c-109">Değiştirilecek kanban kuralını seçme</span><span class="sxs-lookup"><span data-stu-id="38c4c-109">Select a kanban rule to replace</span></span>
1. <span data-ttu-id="38c4c-110">Kanban kuralları'na gidin.</span><span class="sxs-lookup"><span data-stu-id="38c4c-110">Go to Kanban rules.</span></span>
2. <span data-ttu-id="38c4c-111">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="38c4c-111">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="38c4c-112">000022 kanban kuralını seçin.</span><span class="sxs-lookup"><span data-stu-id="38c4c-112">Select kanban rule 000022.</span></span>  

## <a name="create-a-replacement-kanban-rule"></a><span data-ttu-id="38c4c-113">Değiştirme kanban kuralı oluşturma</span><span class="sxs-lookup"><span data-stu-id="38c4c-113">Create a replacement kanban rule</span></span>
1. <span data-ttu-id="38c4c-114">Kanban kuralını değiştir düğmesini tıklayın.</span><span class="sxs-lookup"><span data-stu-id="38c4c-114">Click Replace kanban rule.</span></span>
2. <span data-ttu-id="38c4c-115">Yürürlük tarihi alanına bir tarih ve saat girin.</span><span class="sxs-lookup"><span data-stu-id="38c4c-115">In the Effective date field, enter a date and time.</span></span>
    * <span data-ttu-id="38c4c-116">Örneğin bir hafta sonraki tarih gibi ileri bir tarih seçin.</span><span class="sxs-lookup"><span data-stu-id="38c4c-116">Select a date in the future, such as one week from now.</span></span> <span data-ttu-id="38c4c-117">Bu, yeni kanban kuralının etkin olacağı ve eski kanban kuralının yerine geçeceği tarih ve saattir.</span><span class="sxs-lookup"><span data-stu-id="38c4c-117">This is the date and time when the new kanban rule becomes active and replaces the old kanban rule.</span></span>  
    * <span data-ttu-id="38c4c-118">Kanban kuralı, üretim akışındaki yolu değiştirirse, başka bir etkinlik seçilebilir.</span><span class="sxs-lookup"><span data-stu-id="38c4c-118">If the kanban rule changes the path in the production flow,  another activity can be selected.</span></span>  <span data-ttu-id="38c4c-119">Bu prosedürde etkinliği değiştirmeden bırakacağız.</span><span class="sxs-lookup"><span data-stu-id="38c4c-119">In this procedure, we will keep the activity untouched.</span></span>  
3. <span data-ttu-id="38c4c-120">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="38c4c-120">Click OK.</span></span>
    * <span data-ttu-id="38c4c-121">Kanban kural 000022'nin değiştirilmesi için yeni bir kanban kuralının oluşturulacağına dikkat edin.</span><span class="sxs-lookup"><span data-stu-id="38c4c-121">Notice that a new kanban rule is created to replace kanban rule 000022.</span></span>  
    * <span data-ttu-id="38c4c-122">Geçerlilik tarihi, kanban kuralı değiştirildiğinde seçilen tarihe göre ayarlanır.</span><span class="sxs-lookup"><span data-stu-id="38c4c-122">The effective date is set according to the date chosen when you replace the kanban rule.</span></span>  
4. <span data-ttu-id="38c4c-123">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="38c4c-123">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="38c4c-124">000022 değiştirilen kanban kuralını seçin.</span><span class="sxs-lookup"><span data-stu-id="38c4c-124">Select the replaced kanban rule 000022.</span></span>  
    * <span data-ttu-id="38c4c-125">Değiştirilen kanban kuralının, geçerliliğin biteceği tarih olduğundan Bitiş tarihi ile aynı tarihe sahip olacağına dikkat edin.</span><span class="sxs-lookup"><span data-stu-id="38c4c-125">Notice that the replaced kanban rule has the same date as the Expiration date because this is the date when it will expire.</span></span>  
5. <span data-ttu-id="38c4c-126">Listede satır 1'i seçin.</span><span class="sxs-lookup"><span data-stu-id="38c4c-126">In the list, select row 1.</span></span>
    * <span data-ttu-id="38c4c-127">Listenin başından yeni kanban kuralını seçin.</span><span class="sxs-lookup"><span data-stu-id="38c4c-127">Select the new kanban rule on top of the list.</span></span> <span data-ttu-id="38c4c-128">Bu, en büyük kanban kuralı numarasına sahip kanban kuralıdır.</span><span class="sxs-lookup"><span data-stu-id="38c4c-128">This is the kanban rule with the highest kanban rule number.</span></span>  
6. <span data-ttu-id="38c4c-129">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="38c4c-129">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="38c4c-130">Kanban kuralını açmak için kanban kuralı numarasını tıklatın.</span><span class="sxs-lookup"><span data-stu-id="38c4c-130">Click the kanban rule number to open the kanban rule.</span></span>  

## <a name="modify-maximum-quantity-for-the-replacement-kanban-rule"></a><span data-ttu-id="38c4c-131">Kanban değiştirme kuralı için maksimum miktarı değiştirin</span><span class="sxs-lookup"><span data-stu-id="38c4c-131">Modify maximum quantity for the replacement kanban rule</span></span>
1. <span data-ttu-id="38c4c-132">Maksimum miktarı '100' olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="38c4c-132">Set Maximum quantity to '100'.</span></span>
    * <span data-ttu-id="38c4c-133">Maksimum miktar alanını görüntülemek için Miktarlar Hızlı Sekmesini genişletin.</span><span class="sxs-lookup"><span data-stu-id="38c4c-133">Expand the Quantities FastTab to see the Maximum quantity field.</span></span> <span data-ttu-id="38c4c-134">Maksimum miktarın 100 olarak değiştirilmesi 100 kanban'a kadar işlenmesine izin verir.</span><span class="sxs-lookup"><span data-stu-id="38c4c-134">Changing the maximum quantity to 100 will allow up to 100 kanbans to be processed.</span></span>    <span data-ttu-id="38c4c-135">Bu, bu görevdeki son adımdır.</span><span class="sxs-lookup"><span data-stu-id="38c4c-135">This is the last step in this task.</span></span>  

