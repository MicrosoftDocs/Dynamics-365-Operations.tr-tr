---
title: Maliyet dağıtım ilkesi oluşturma ve bir maliyet kontrol birimine atama
description: Maliyet dağıtım kuralları, bir maliyet merkezinde mali olarak sayılmış maliyetleri dağıtmak için kullanılır.
author: ShylaThompson
manager: AnnBe
ms.date: 06/27/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CAMCostDistributionRule
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Operations
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 66921d5eddb31ffba0946c41f634719a684e4ad1
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/10/2020
ms.locfileid: "3976199"
---
# <a name="create-and-assign-a-cost-distribution-policy-to-a-cost-control-unit"></a><span data-ttu-id="49b65-103">Maliyet dağıtım ilkesi oluşturma ve bir maliyet kontrol birimine atama</span><span class="sxs-lookup"><span data-stu-id="49b65-103">Create and assign a cost distribution policy to a cost control unit</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="49b65-104">Maliyet dağıtım kuralları, bir maliyet merkezinde mali olarak sayılmış maliyetleri dağıtmak için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="49b65-104">Cost distribution rules are used to distribute costs that have been financially counted on a collective cost center.</span></span> <span data-ttu-id="49b65-105">Maliyet muhasebecisi, maliyetin seçilen tahsisat tabanına dayanarak maliyet merkezlerinde dağıtıldığından emin olur.</span><span class="sxs-lookup"><span data-stu-id="49b65-105">The cost accountant makes sure that the cost is distributed to the cost centers, based on the selected allocation base.</span></span> <span data-ttu-id="49b65-106">Bir ilke ve karşılık gelen kurallar bir maliyet kontrol birimine atanır.</span><span class="sxs-lookup"><span data-stu-id="49b65-106">A policy and the corresponding rules are assigned to a cost control unit.</span></span> <span data-ttu-id="49b65-107">Bu görev kılavuzu, bir maliyet dağıtım ilkesi ve karşılık gelen kuralları oluşturmayı göstermek için bir örnek kullanır.</span><span class="sxs-lookup"><span data-stu-id="49b65-107">This task guide uses an example to show how to create a cost distribution policy and the corresponding rules.</span></span>


## <a name="create-a-policy"></a><span data-ttu-id="49b65-108">Bir ilke oluşturun</span><span class="sxs-lookup"><span data-stu-id="49b65-108">Create a policy</span></span>
1. <span data-ttu-id="49b65-109">Maliyet muhasebesi > İlkeler > Maliyet dağıtım ilkeleri'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="49b65-109">Go to Cost accounting > Policies > Cost distribution policies.</span></span>
2. <span data-ttu-id="49b65-110">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="49b65-110">Click New.</span></span>
3. <span data-ttu-id="49b65-111">İlke adı alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="49b65-111">In the Policy name field, type a value.</span></span>
4. <span data-ttu-id="49b65-112">Açıklama alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="49b65-112">In the Description field, type a value.</span></span>
5. <span data-ttu-id="49b65-113">Maliyet nesnesi boyut hiyerarşisi alanına bir değer girin veya bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="49b65-113">In the Cost object dimension hierarchy field, enter or select a value.</span></span>
    * <span data-ttu-id="49b65-114">Kuruluşu seçin.</span><span class="sxs-lookup"><span data-stu-id="49b65-114">Select Organization.</span></span>  
6. <span data-ttu-id="49b65-115">Maliyet öğesi boyut hiyerarşisi alanına bir değer girin veya bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="49b65-115">In the Cost element dimension hierarchy field, enter or select a value.</span></span>
    * <span data-ttu-id="49b65-116">CDS P/L seçin.</span><span class="sxs-lookup"><span data-stu-id="49b65-116">Select CDS P/L.</span></span>  
7. <span data-ttu-id="49b65-117">İstatistiksel boyutu alanına bir değer girin veya bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="49b65-117">In the Statistical dimension field, enter or select a value.</span></span>
    * <span data-ttu-id="49b65-118">İstatistiksel öğeler'i seçin.</span><span class="sxs-lookup"><span data-stu-id="49b65-118">Select Statistical elements.</span></span>  
8. <span data-ttu-id="49b65-119">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="49b65-119">Click Save.</span></span>

## <a name="create-rules-for-the-policy"></a><span data-ttu-id="49b65-120">İlke için kurallar oluşturun</span><span class="sxs-lookup"><span data-stu-id="49b65-120">Create rules for the policy</span></span>
1. <span data-ttu-id="49b65-121">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="49b65-121">Click New.</span></span>
2. <span data-ttu-id="49b65-122">Listede, seçili satırı işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="49b65-122">In the list, mark the selected row.</span></span>
3. <span data-ttu-id="49b65-123">Maliyet nesnesi boyut hiyerarşi düğümü alanına bir değer girin veya bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="49b65-123">In the Cost object dimension hierarchy node field, enter or select a value.</span></span>
    * <span data-ttu-id="49b65-124">094 seçmek için hiyerarşiyi genişletin.</span><span class="sxs-lookup"><span data-stu-id="49b65-124">Expand the hierarchy to select 094.</span></span>  
4. <span data-ttu-id="49b65-125">Maliyet öğesi boyut hiyerarşi düğümü alanına bir değer girin veya bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="49b65-125">In the Cost element dimension hierarchy node field, enter or select a value.</span></span>
    * <span data-ttu-id="49b65-126">Diğer işletme giderlerini seçin ve daha sonra 605110 Temizlik öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="49b65-126">Select Other operating expenses and then select 605110 Cleaning.</span></span>  
5. <span data-ttu-id="49b65-127">Maliyet davranışı alanında, bir seçenek seçin.</span><span class="sxs-lookup"><span data-stu-id="49b65-127">In the Cost behavior field, select an option.</span></span>
    * <span data-ttu-id="49b65-128">Sabit maliyet'i seçin</span><span class="sxs-lookup"><span data-stu-id="49b65-128">Select Fixed cost.</span></span>  
6. <span data-ttu-id="49b65-129">Tahsisat tabanı alanına bir değer girin veya buradan bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="49b65-129">In the Allocation base field, enter or select a value.</span></span>
7. <span data-ttu-id="49b65-130">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="49b65-130">Click New.</span></span>
8. <span data-ttu-id="49b65-131">Listede, seçili satırı işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="49b65-131">In the list, mark the selected row.</span></span>
9. <span data-ttu-id="49b65-132">Maliyet nesnesi boyut hiyerarşi düğümü alanına bir değer girin veya bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="49b65-132">In the Cost object dimension hierarchy node field, enter or select a value.</span></span>
    * <span data-ttu-id="49b65-133">094 seçmek için hiyerarşiyi genişletin.</span><span class="sxs-lookup"><span data-stu-id="49b65-133">Expand the hierarchy to select 094.</span></span>  
10. <span data-ttu-id="49b65-134">Maliyet öğesi boyut hiyerarşi düğümü alanına bir değer girin veya bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="49b65-134">In the Cost element dimension hierarchy node field, enter or select a value.</span></span>
    * <span data-ttu-id="49b65-135">Diğer işletme giderlerini seçin ve daha sonra 605150 Kira öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="49b65-135">Select Other operating expenses and then select 605150 Rent.</span></span>  
11. <span data-ttu-id="49b65-136">Maliyet davranışı alanında, bir seçenek seçin.</span><span class="sxs-lookup"><span data-stu-id="49b65-136">In the Cost behavior field, select an option.</span></span>
    * <span data-ttu-id="49b65-137">Sabit maliyet'i seçin</span><span class="sxs-lookup"><span data-stu-id="49b65-137">Select Fixed cost.</span></span>  
12. <span data-ttu-id="49b65-138">Tahsisat tabanı alanına bir değer girin veya buradan bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="49b65-138">In the Allocation base field, enter or select a value.</span></span>
13. <span data-ttu-id="49b65-139">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="49b65-139">Click Save.</span></span>

## <a name="assign-rules-to-a-cost-control-unit"></a><span data-ttu-id="49b65-140">Bir maliyet kontrol birimine kurallar atayın</span><span class="sxs-lookup"><span data-stu-id="49b65-140">Assign rules to a cost control unit</span></span>
1. <span data-ttu-id="49b65-141">Maliyet kontrol birimi için ilke atamaları'na tıklayın.</span><span class="sxs-lookup"><span data-stu-id="49b65-141">Click Policy assignments for cost control unit.</span></span>
2. <span data-ttu-id="49b65-142">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="49b65-142">Click New.</span></span>
3. <span data-ttu-id="49b65-143">Listede, seçili satırı işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="49b65-143">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="49b65-144">Geçerlilik tarihi muhasebe veri alanına bir tarih girin.</span><span class="sxs-lookup"><span data-stu-id="49b65-144">In the Valid from accounting date field, enter a date.</span></span>
    * <span data-ttu-id="49b65-145">Geçerli mali yılda Eylül 1'i seçin.</span><span class="sxs-lookup"><span data-stu-id="49b65-145">Select September 1 in the valid fiscal year.</span></span>  
5. <span data-ttu-id="49b65-146">Maliyet kontrol birimi alanına bir değer girin veya bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="49b65-146">In the Cost control unit field, enter or select a value.</span></span>
6. <span data-ttu-id="49b65-147">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="49b65-147">Click Save.</span></span>

