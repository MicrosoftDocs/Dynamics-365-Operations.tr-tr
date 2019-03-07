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
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 92f41eb99b84bbc596e79b413971f9d92f2555b6
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2019
ms.locfileid: "324411"
---
# <a name="create-and-assign-a-cost-allocation-policy-to-a-cost-control-unit"></a><span data-ttu-id="73dc1-103">Maliyet tahsisatı ilkesi oluşturma ve bir maliyet kontrol birimine atama</span><span class="sxs-lookup"><span data-stu-id="73dc1-103">Create and assign a cost allocation policy to a cost control unit</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="73dc1-104">Bu yordamı bir maliyet tahsisat ilkesini ve karşılık gelen kuralları oluşturmak ve bir maliyet kontrol birimine atamak için kullanın.</span><span class="sxs-lookup"><span data-stu-id="73dc1-104">Use this procedure to create and assign a cost allocation policy and the corresponding rules to a cost control unit.</span></span> <span data-ttu-id="73dc1-105">Bu kayıt USP2 demo veri şirketini kullanır.</span><span class="sxs-lookup"><span data-stu-id="73dc1-105">This recording uses the USP2 demo data company.</span></span>


## <a name="create-a-policy"></a><span data-ttu-id="73dc1-106">Bir ilke oluşturun</span><span class="sxs-lookup"><span data-stu-id="73dc1-106">Create a policy</span></span>
1. <span data-ttu-id="73dc1-107">Maliyet muhasebesi > İlkeler > Maliyet tahsisat ilkeleri'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="73dc1-107">Go to Cost accounting > Policies > Cost allocation policies.</span></span>
2. <span data-ttu-id="73dc1-108">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="73dc1-108">Click New.</span></span>
3. <span data-ttu-id="73dc1-109">İlke adı alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="73dc1-109">In the Policy name field, type a value.</span></span>
4. <span data-ttu-id="73dc1-110">Maliyet nesnesi boyut hiyerarşisi alanına bir değer girin veya bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="73dc1-110">In the Cost object dimension hierarchy field, enter or select a value.</span></span>
    * <span data-ttu-id="73dc1-111">Kuruluşu seçin.</span><span class="sxs-lookup"><span data-stu-id="73dc1-111">Select Organization.</span></span>  
5. <span data-ttu-id="73dc1-112">İstatistiksel boyutu alanına bir değer girin veya bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="73dc1-112">In the Statistical dimension field, enter or select a value.</span></span>
6. <span data-ttu-id="73dc1-113">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="73dc1-113">Click Save.</span></span>

## <a name="create-allocation-rules"></a><span data-ttu-id="73dc1-114">Tahsisat kuralları oluşturun</span><span class="sxs-lookup"><span data-stu-id="73dc1-114">Create allocation rules</span></span>
1. <span data-ttu-id="73dc1-115">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="73dc1-115">Click New.</span></span>
2. <span data-ttu-id="73dc1-116">Listede, seçili satırı işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="73dc1-116">In the list, mark the selected row.</span></span>
3. <span data-ttu-id="73dc1-117">Maliyet nesnesi boyut hiyerarşi düğümü alanına bir değer girin veya bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="73dc1-117">In the Cost object dimension hierarchy node field, enter or select a value.</span></span>
4. <span data-ttu-id="73dc1-118">Maliyet davranışı alanında, 'Toplam'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="73dc1-118">In the Cost behavior field, select 'Total'.</span></span>
5. <span data-ttu-id="73dc1-119">Tahsisat tabanı alanına bir değer girin veya buradan bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="73dc1-119">In the Allocation base field, enter or select a value.</span></span>
6. <span data-ttu-id="73dc1-120">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="73dc1-120">Click New.</span></span>
7. <span data-ttu-id="73dc1-121">Listede, seçili satırı işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="73dc1-121">In the list, mark the selected row.</span></span>
8. <span data-ttu-id="73dc1-122">Maliyet nesnesi boyut hiyerarşi düğümü alanına bir değer girin veya bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="73dc1-122">In the Cost object dimension hierarchy node field, enter or select a value.</span></span>
9. <span data-ttu-id="73dc1-123">Maliyet davranışı alanında, 'Toplam'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="73dc1-123">In the Cost behavior field, select 'Total'.</span></span>
10. <span data-ttu-id="73dc1-124">Tahsisat tabanı alanına bir değer girin veya buradan bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="73dc1-124">In the Allocation base field, enter or select a value.</span></span>
11. <span data-ttu-id="73dc1-125">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="73dc1-125">Click New.</span></span>
12. <span data-ttu-id="73dc1-126">Listede, seçili satırı işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="73dc1-126">In the list, mark the selected row.</span></span>
13. <span data-ttu-id="73dc1-127">Maliyet nesnesi boyut hiyerarşi düğümü alanına bir değer girin veya bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="73dc1-127">In the Cost object dimension hierarchy node field, enter or select a value.</span></span>
14. <span data-ttu-id="73dc1-128">Maliyet davranışı alanında, 'Toplam'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="73dc1-128">In the Cost behavior field, select 'Total'.</span></span>
15. <span data-ttu-id="73dc1-129">Tahsisat tabanı alanına bir değer girin veya buradan bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="73dc1-129">In the Allocation base field, enter or select a value.</span></span>
    * <span data-ttu-id="73dc1-130">Tüm kuralları oluşturana kadar devam edin.</span><span class="sxs-lookup"><span data-stu-id="73dc1-130">Continue until you've created all the rules.</span></span>  
16. <span data-ttu-id="73dc1-131">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="73dc1-131">Click Save.</span></span>

## <a name="assign-the-policy-to-a-cost-control-unit"></a><span data-ttu-id="73dc1-132">İlkeyi bir maliyet kontrol birimine atayın</span><span class="sxs-lookup"><span data-stu-id="73dc1-132">Assign the policy to a cost control unit</span></span>
1. <span data-ttu-id="73dc1-133">Maliyet kontrol birimi için ilke atamaları'na tıklayın.</span><span class="sxs-lookup"><span data-stu-id="73dc1-133">Click Policy assignments for cost control unit.</span></span>
2. <span data-ttu-id="73dc1-134">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="73dc1-134">Click New.</span></span>
3. <span data-ttu-id="73dc1-135">Listede, seçili satırı işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="73dc1-135">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="73dc1-136">Geçerlilik tarihi muhasebe veri alanına bir tarih girin.</span><span class="sxs-lookup"><span data-stu-id="73dc1-136">In the Valid from accounting date field, enter a date.</span></span>
    * <span data-ttu-id="73dc1-137">Kuralların geçerlilik tarihi vardır.</span><span class="sxs-lookup"><span data-stu-id="73dc1-137">The rules are date-effective.</span></span> <span data-ttu-id="73dc1-138">Sistemdeki bir kullanıcı, yeni bir sürüm oluşturulmuşsa kuralların vadesini doldurabilir.</span><span class="sxs-lookup"><span data-stu-id="73dc1-138">A user or the system can expire the rules if a newer version is created.</span></span>  
5. <span data-ttu-id="73dc1-139">Maliyet kontrol birimi alanına bir değer girin veya bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="73dc1-139">In the Cost control unit field, enter or select a value.</span></span>
6. <span data-ttu-id="73dc1-140">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="73dc1-140">Click Save.</span></span>

