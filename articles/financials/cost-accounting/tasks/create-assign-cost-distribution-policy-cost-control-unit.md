--- 
title: "Maliyet dağıtım ilkesi oluşturma ve bir maliyet kontrol birimine atama"
description: "Maliyet dağıtım kuralları, bir maliyet merkezinde mali olarak sayılmış maliyetleri dağıtmak için kullanılır."
author: YuyuScheller
manager: AnnBe
ms.date: 06/27/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.author: yuyus
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: fbd44816fc2f2569dd477fc21f59418a575bb835
ms.contentlocale: tr-tr
ms.lasthandoff: 09/29/2017

---
# <a name="create-and-assign-a-cost-distribution-policy-to-a-cost-control-unit"></a><span data-ttu-id="da357-103">Maliyet dağıtım ilkesi oluşturma ve bir maliyet kontrol birimine atama</span><span class="sxs-lookup"><span data-stu-id="da357-103">Create and assign a cost distribution policy to a cost control unit</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="da357-104">Maliyet dağıtım kuralları, bir maliyet merkezinde mali olarak sayılmış maliyetleri dağıtmak için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="da357-104">Cost distribution rules are used to distribute costs that have been financially counted on a collective cost center.</span></span> <span data-ttu-id="da357-105">Maliyet muhasebecisi, maliyetin seçilen tahsisat tabanına dayanarak maliyet merkezlerinde dağıtıldığından emin olur.</span><span class="sxs-lookup"><span data-stu-id="da357-105">The cost accountant makes sure that the cost is distributed to the cost centers, based on the selected allocation base.</span></span> <span data-ttu-id="da357-106">Bir ilke ve karşılık gelen kurallar bir maliyet kontrol birimine atanır.</span><span class="sxs-lookup"><span data-stu-id="da357-106">A policy and the corresponding rules are assigned to a cost control unit.</span></span> <span data-ttu-id="da357-107">Bu görev kılavuzu, bir maliyet dağıtım ilkesi ve karşılık gelen kuralları oluşturmayı göstermek için bir örnek kullanır.</span><span class="sxs-lookup"><span data-stu-id="da357-107">This task guide uses an example to show how to create a cost distribution policy and the corresponding rules.</span></span>


## <a name="create-a-policy"></a><span data-ttu-id="da357-108">Bir ilke oluşturun</span><span class="sxs-lookup"><span data-stu-id="da357-108">Create a policy</span></span>
1. <span data-ttu-id="da357-109">Maliyet muhasebesi > İlkeler > Maliyet dağıtım ilkeleri'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="da357-109">Go to Cost accounting > Policies > Cost distribution policies.</span></span>
2. <span data-ttu-id="da357-110">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="da357-110">Click New.</span></span>
3. <span data-ttu-id="da357-111">İlke adı alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="da357-111">In the Policy name field, type a value.</span></span>
4. <span data-ttu-id="da357-112">Açıklama alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="da357-112">In the Description field, type a value.</span></span>
5. <span data-ttu-id="da357-113">Maliyet nesnesi boyut hiyerarşisi alanına bir değer girin veya bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="da357-113">In the Cost object dimension hierarchy field, enter or select a value.</span></span>
    * <span data-ttu-id="da357-114">Kuruluşu seçin.</span><span class="sxs-lookup"><span data-stu-id="da357-114">Select Organization.</span></span>  
6. <span data-ttu-id="da357-115">Maliyet öğesi boyut hiyerarşisi alanına bir değer girin veya bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="da357-115">In the Cost element dimension hierarchy field, enter or select a value.</span></span>
    * <span data-ttu-id="da357-116">CDS P/L seçin.</span><span class="sxs-lookup"><span data-stu-id="da357-116">Select CDS P/L.</span></span>  
7. <span data-ttu-id="da357-117">İstatistiksel boyutu alanına bir değer girin veya bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="da357-117">In the Statistical dimension field, enter or select a value.</span></span>
    * <span data-ttu-id="da357-118">İstatistiksel öğeler'i seçin.</span><span class="sxs-lookup"><span data-stu-id="da357-118">Select Statistical elements.</span></span>  
8. <span data-ttu-id="da357-119">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="da357-119">Click Save.</span></span>

## <a name="create-rules-for-the-policy"></a><span data-ttu-id="da357-120">İlke için kurallar oluşturun</span><span class="sxs-lookup"><span data-stu-id="da357-120">Create rules for the policy</span></span>
1. <span data-ttu-id="da357-121">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="da357-121">Click New.</span></span>
2. <span data-ttu-id="da357-122">Listede, seçili satırı işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="da357-122">In the list, mark the selected row.</span></span>
3. <span data-ttu-id="da357-123">Maliyet nesnesi boyut hiyerarşi düğümü alanına bir değer girin veya bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="da357-123">In the Cost object dimension hierarchy node field, enter or select a value.</span></span>
    * <span data-ttu-id="da357-124">094 seçmek için hiyerarşiyi genişletin.</span><span class="sxs-lookup"><span data-stu-id="da357-124">Expand the hierarchy to select 094.</span></span>  
4. <span data-ttu-id="da357-125">Maliyet öğesi boyut hiyerarşi düğümü alanına bir değer girin veya bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="da357-125">In the Cost element dimension hierarchy node field, enter or select a value.</span></span>
    * <span data-ttu-id="da357-126">Diğer işletme giderlerini seçin ve daha sonra 605110 Temizlik öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="da357-126">Select Other operating expenses and then select 605110 Cleaning.</span></span>  
5. <span data-ttu-id="da357-127">Maliyet davranışı alanında, bir seçenek seçin.</span><span class="sxs-lookup"><span data-stu-id="da357-127">In the Cost behavior field, select an option.</span></span>
    * <span data-ttu-id="da357-128">Sabit maliyet'i seçin</span><span class="sxs-lookup"><span data-stu-id="da357-128">Select Fixed cost.</span></span>  
6. <span data-ttu-id="da357-129">Tahsisat tabanı alanına bir değer girin veya buradan bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="da357-129">In the Allocation base field, enter or select a value.</span></span>
7. <span data-ttu-id="da357-130">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="da357-130">Click New.</span></span>
8. <span data-ttu-id="da357-131">Listede, seçili satırı işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="da357-131">In the list, mark the selected row.</span></span>
9. <span data-ttu-id="da357-132">Maliyet nesnesi boyut hiyerarşi düğümü alanına bir değer girin veya bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="da357-132">In the Cost object dimension hierarchy node field, enter or select a value.</span></span>
    * <span data-ttu-id="da357-133">094 seçmek için hiyerarşiyi genişletin.</span><span class="sxs-lookup"><span data-stu-id="da357-133">Expand the hierarchy to select 094.</span></span>  
10. <span data-ttu-id="da357-134">Maliyet öğesi boyut hiyerarşi düğümü alanına bir değer girin veya bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="da357-134">In the Cost element dimension hierarchy node field, enter or select a value.</span></span>
    * <span data-ttu-id="da357-135">Diğer işletme giderlerini seçin ve daha sonra 605150 Kira öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="da357-135">Select Other operating expenses and then select 605150 Rent.</span></span>  
11. <span data-ttu-id="da357-136">Maliyet davranışı alanında, bir seçenek seçin.</span><span class="sxs-lookup"><span data-stu-id="da357-136">In the Cost behavior field, select an option.</span></span>
    * <span data-ttu-id="da357-137">Sabit maliyet'i seçin</span><span class="sxs-lookup"><span data-stu-id="da357-137">Select Fixed cost.</span></span>  
12. <span data-ttu-id="da357-138">Tahsisat tabanı alanına bir değer girin veya buradan bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="da357-138">In the Allocation base field, enter or select a value.</span></span>
13. <span data-ttu-id="da357-139">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="da357-139">Click Save.</span></span>

## <a name="assign-rules-to-a-cost-control-unit"></a><span data-ttu-id="da357-140">Bir maliyet kontrol birimine kurallar atayın</span><span class="sxs-lookup"><span data-stu-id="da357-140">Assign rules to a cost control unit</span></span>
1. <span data-ttu-id="da357-141">Maliyet kontrol birimi için ilke atamaları'na tıklayın.</span><span class="sxs-lookup"><span data-stu-id="da357-141">Click Policy assignments for cost control unit.</span></span>
2. <span data-ttu-id="da357-142">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="da357-142">Click New.</span></span>
3. <span data-ttu-id="da357-143">Listede, seçili satırı işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="da357-143">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="da357-144">Geçerlilik tarihi muhasebe veri alanına bir tarih girin.</span><span class="sxs-lookup"><span data-stu-id="da357-144">In the Valid from accounting date field, enter a date.</span></span>
    * <span data-ttu-id="da357-145">Geçerli mali yılda Eylül 1'i seçin.</span><span class="sxs-lookup"><span data-stu-id="da357-145">Select September 1 in the valid fiscal year.</span></span>  
5. <span data-ttu-id="da357-146">Maliyet kontrol birimi alanına bir değer girin veya bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="da357-146">In the Cost control unit field, enter or select a value.</span></span>
6. <span data-ttu-id="da357-147">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="da357-147">Click Save.</span></span>


