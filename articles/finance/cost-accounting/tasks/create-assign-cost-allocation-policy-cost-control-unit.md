---
title: Maliyet tahsisatı ilkesi oluşturma ve bir maliyet kontrol birimine atama
description: Bu yordamı bir maliyet tahsisat ilkesini ve karşılık gelen kuralları oluşturmak ve bir maliyet kontrol birimine atamak için kullanın.
author: ShylaThompson
manager: AnnBe
ms.date: 06/28/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CAMCostAccountingLedgerPolicyAssignment
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 006310d07dfa5b75941ca248736800bbb9e8e7b7
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/15/2021
ms.locfileid: "4969340"
---
# <a name="create-and-assign-a-cost-allocation-policy-to-a-cost-control-unit"></a><span data-ttu-id="a5b0d-103">Maliyet tahsisatı ilkesi oluşturma ve bir maliyet kontrol birimine atama</span><span class="sxs-lookup"><span data-stu-id="a5b0d-103">Create and assign a cost allocation policy to a cost control unit</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="a5b0d-104">Bu yordamı bir maliyet tahsisat ilkesini ve karşılık gelen kuralları oluşturmak ve bir maliyet kontrol birimine atamak için kullanın.</span><span class="sxs-lookup"><span data-stu-id="a5b0d-104">Use this procedure to create and assign a cost allocation policy and the corresponding rules to a cost control unit.</span></span> <span data-ttu-id="a5b0d-105">Bu kayıt USP2 demo veri şirketini kullanır.</span><span class="sxs-lookup"><span data-stu-id="a5b0d-105">This recording uses the USP2 demo data company.</span></span>


## <a name="create-a-policy"></a><span data-ttu-id="a5b0d-106">Bir ilke oluşturun</span><span class="sxs-lookup"><span data-stu-id="a5b0d-106">Create a policy</span></span>
1. <span data-ttu-id="a5b0d-107">Maliyet muhasebesi > İlkeler > Maliyet tahsisat ilkeleri'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="a5b0d-107">Go to Cost accounting > Policies > Cost allocation policies.</span></span>
2. <span data-ttu-id="a5b0d-108">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="a5b0d-108">Click New.</span></span>
3. <span data-ttu-id="a5b0d-109">İlke adı alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="a5b0d-109">In the Policy name field, type a value.</span></span>
4. <span data-ttu-id="a5b0d-110">Maliyet nesnesi boyut hiyerarşisi alanına bir değer girin veya bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="a5b0d-110">In the Cost object dimension hierarchy field, enter or select a value.</span></span>
    * <span data-ttu-id="a5b0d-111">Kuruluşu seçin.</span><span class="sxs-lookup"><span data-stu-id="a5b0d-111">Select Organization.</span></span>  
5. <span data-ttu-id="a5b0d-112">İstatistiksel boyutu alanına bir değer girin veya bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="a5b0d-112">In the Statistical dimension field, enter or select a value.</span></span>
6. <span data-ttu-id="a5b0d-113">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="a5b0d-113">Click Save.</span></span>

## <a name="create-allocation-rules"></a><span data-ttu-id="a5b0d-114">Tahsisat kuralları oluşturun</span><span class="sxs-lookup"><span data-stu-id="a5b0d-114">Create allocation rules</span></span>
1. <span data-ttu-id="a5b0d-115">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="a5b0d-115">Click New.</span></span>
2. <span data-ttu-id="a5b0d-116">Listede, seçili satırı işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="a5b0d-116">In the list, mark the selected row.</span></span>
3. <span data-ttu-id="a5b0d-117">Maliyet nesnesi boyut hiyerarşi düğümü alanına bir değer girin veya bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="a5b0d-117">In the Cost object dimension hierarchy node field, enter or select a value.</span></span>
4. <span data-ttu-id="a5b0d-118">Maliyet davranışı alanında, 'Toplam'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="a5b0d-118">In the Cost behavior field, select 'Total'.</span></span>
5. <span data-ttu-id="a5b0d-119">Tahsisat tabanı alanına bir değer girin veya buradan bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="a5b0d-119">In the Allocation base field, enter or select a value.</span></span>
6. <span data-ttu-id="a5b0d-120">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="a5b0d-120">Click New.</span></span>
7. <span data-ttu-id="a5b0d-121">Listede, seçili satırı işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="a5b0d-121">In the list, mark the selected row.</span></span>
8. <span data-ttu-id="a5b0d-122">Maliyet nesnesi boyut hiyerarşi düğümü alanına bir değer girin veya bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="a5b0d-122">In the Cost object dimension hierarchy node field, enter or select a value.</span></span>
9. <span data-ttu-id="a5b0d-123">Maliyet davranışı alanında, 'Toplam'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="a5b0d-123">In the Cost behavior field, select 'Total'.</span></span>
10. <span data-ttu-id="a5b0d-124">Tahsisat tabanı alanına bir değer girin veya buradan bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="a5b0d-124">In the Allocation base field, enter or select a value.</span></span>
11. <span data-ttu-id="a5b0d-125">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="a5b0d-125">Click New.</span></span>
12. <span data-ttu-id="a5b0d-126">Listede, seçili satırı işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="a5b0d-126">In the list, mark the selected row.</span></span>
13. <span data-ttu-id="a5b0d-127">Maliyet nesnesi boyut hiyerarşi düğümü alanına bir değer girin veya bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="a5b0d-127">In the Cost object dimension hierarchy node field, enter or select a value.</span></span>
14. <span data-ttu-id="a5b0d-128">Maliyet davranışı alanında, 'Toplam'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="a5b0d-128">In the Cost behavior field, select 'Total'.</span></span>
15. <span data-ttu-id="a5b0d-129">Tahsisat tabanı alanına bir değer girin veya buradan bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="a5b0d-129">In the Allocation base field, enter or select a value.</span></span>
    * <span data-ttu-id="a5b0d-130">Tüm kuralları oluşturana kadar devam edin.</span><span class="sxs-lookup"><span data-stu-id="a5b0d-130">Continue until you've created all the rules.</span></span>  
16. <span data-ttu-id="a5b0d-131">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="a5b0d-131">Click Save.</span></span>

## <a name="assign-the-policy-to-a-cost-control-unit"></a><span data-ttu-id="a5b0d-132">İlkeyi bir maliyet kontrol birimine atayın</span><span class="sxs-lookup"><span data-stu-id="a5b0d-132">Assign the policy to a cost control unit</span></span>
1. <span data-ttu-id="a5b0d-133">Maliyet kontrol birimi için ilke atamaları'na tıklayın.</span><span class="sxs-lookup"><span data-stu-id="a5b0d-133">Click Policy assignments for cost control unit.</span></span>
2. <span data-ttu-id="a5b0d-134">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="a5b0d-134">Click New.</span></span>
3. <span data-ttu-id="a5b0d-135">Listede, seçili satırı işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="a5b0d-135">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="a5b0d-136">Geçerlilik tarihi muhasebe veri alanına bir tarih girin.</span><span class="sxs-lookup"><span data-stu-id="a5b0d-136">In the Valid from accounting date field, enter a date.</span></span>
    * <span data-ttu-id="a5b0d-137">Kuralların geçerlilik tarihi vardır.</span><span class="sxs-lookup"><span data-stu-id="a5b0d-137">The rules are date-effective.</span></span> <span data-ttu-id="a5b0d-138">Sistemdeki bir kullanıcı, yeni bir sürüm oluşturulmuşsa kuralların vadesini doldurabilir.</span><span class="sxs-lookup"><span data-stu-id="a5b0d-138">A user or the system can expire the rules if a newer version is created.</span></span>  
5. <span data-ttu-id="a5b0d-139">Maliyet kontrol birimi alanına bir değer girin veya bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="a5b0d-139">In the Cost control unit field, enter or select a value.</span></span>
6. <span data-ttu-id="a5b0d-140">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="a5b0d-140">Click Save.</span></span>

