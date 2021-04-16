---
title: Maliyet tahsisatı ilkesi oluşturma ve bir maliyet kontrol birimine atama
description: Bu yordamı bir maliyet tahsisat ilkesini ve karşılık gelen kuralları oluşturmak ve bir maliyet kontrol birimine atamak için kullanın.
author: ShylaThompson
ms.date: 06/28/2017
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: CAMCostAccountingLedgerPolicyAssignment
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1cff10132e8007be885e9c69d97cf96c30d69f50
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/01/2021
ms.locfileid: "5822867"
---
# <a name="create-and-assign-a-cost-allocation-policy-to-a-cost-control-unit"></a><span data-ttu-id="7c191-103">Maliyet tahsisatı ilkesi oluşturma ve bir maliyet kontrol birimine atama</span><span class="sxs-lookup"><span data-stu-id="7c191-103">Create and assign a cost allocation policy to a cost control unit</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="7c191-104">Bu yordamı bir maliyet tahsisat ilkesini ve karşılık gelen kuralları oluşturmak ve bir maliyet kontrol birimine atamak için kullanın.</span><span class="sxs-lookup"><span data-stu-id="7c191-104">Use this procedure to create and assign a cost allocation policy and the corresponding rules to a cost control unit.</span></span> <span data-ttu-id="7c191-105">Bu kayıt USP2 demo veri şirketini kullanır.</span><span class="sxs-lookup"><span data-stu-id="7c191-105">This recording uses the USP2 demo data company.</span></span>


## <a name="create-a-policy"></a><span data-ttu-id="7c191-106">Bir ilke oluşturun</span><span class="sxs-lookup"><span data-stu-id="7c191-106">Create a policy</span></span>
1. <span data-ttu-id="7c191-107">Maliyet muhasebesi > İlkeler > Maliyet tahsisat ilkeleri'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="7c191-107">Go to Cost accounting > Policies > Cost allocation policies.</span></span>
2. <span data-ttu-id="7c191-108">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="7c191-108">Click New.</span></span>
3. <span data-ttu-id="7c191-109">İlke adı alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="7c191-109">In the Policy name field, type a value.</span></span>
4. <span data-ttu-id="7c191-110">Maliyet nesnesi boyut hiyerarşisi alanına bir değer girin veya bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="7c191-110">In the Cost object dimension hierarchy field, enter or select a value.</span></span>
    * <span data-ttu-id="7c191-111">Kuruluşu seçin.</span><span class="sxs-lookup"><span data-stu-id="7c191-111">Select Organization.</span></span>  
5. <span data-ttu-id="7c191-112">İstatistiksel boyutu alanına bir değer girin veya bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="7c191-112">In the Statistical dimension field, enter or select a value.</span></span>
6. <span data-ttu-id="7c191-113">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="7c191-113">Click Save.</span></span>

## <a name="create-allocation-rules"></a><span data-ttu-id="7c191-114">Tahsisat kuralları oluşturun</span><span class="sxs-lookup"><span data-stu-id="7c191-114">Create allocation rules</span></span>
1. <span data-ttu-id="7c191-115">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="7c191-115">Click New.</span></span>
2. <span data-ttu-id="7c191-116">Listede, seçili satırı işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="7c191-116">In the list, mark the selected row.</span></span>
3. <span data-ttu-id="7c191-117">Maliyet nesnesi boyut hiyerarşi düğümü alanına bir değer girin veya bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="7c191-117">In the Cost object dimension hierarchy node field, enter or select a value.</span></span>
4. <span data-ttu-id="7c191-118">Maliyet davranışı alanında, 'Toplam'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="7c191-118">In the Cost behavior field, select 'Total'.</span></span>
5. <span data-ttu-id="7c191-119">Tahsisat tabanı alanına bir değer girin veya buradan bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="7c191-119">In the Allocation base field, enter or select a value.</span></span>
6. <span data-ttu-id="7c191-120">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="7c191-120">Click New.</span></span>
7. <span data-ttu-id="7c191-121">Listede, seçili satırı işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="7c191-121">In the list, mark the selected row.</span></span>
8. <span data-ttu-id="7c191-122">Maliyet nesnesi boyut hiyerarşi düğümü alanına bir değer girin veya bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="7c191-122">In the Cost object dimension hierarchy node field, enter or select a value.</span></span>
9. <span data-ttu-id="7c191-123">Maliyet davranışı alanında, 'Toplam'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="7c191-123">In the Cost behavior field, select 'Total'.</span></span>
10. <span data-ttu-id="7c191-124">Tahsisat tabanı alanına bir değer girin veya buradan bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="7c191-124">In the Allocation base field, enter or select a value.</span></span>
11. <span data-ttu-id="7c191-125">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="7c191-125">Click New.</span></span>
12. <span data-ttu-id="7c191-126">Listede, seçili satırı işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="7c191-126">In the list, mark the selected row.</span></span>
13. <span data-ttu-id="7c191-127">Maliyet nesnesi boyut hiyerarşi düğümü alanına bir değer girin veya bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="7c191-127">In the Cost object dimension hierarchy node field, enter or select a value.</span></span>
14. <span data-ttu-id="7c191-128">Maliyet davranışı alanında, 'Toplam'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="7c191-128">In the Cost behavior field, select 'Total'.</span></span>
15. <span data-ttu-id="7c191-129">Tahsisat tabanı alanına bir değer girin veya buradan bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="7c191-129">In the Allocation base field, enter or select a value.</span></span>
    * <span data-ttu-id="7c191-130">Tüm kuralları oluşturana kadar devam edin.</span><span class="sxs-lookup"><span data-stu-id="7c191-130">Continue until you've created all the rules.</span></span>  
16. <span data-ttu-id="7c191-131">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="7c191-131">Click Save.</span></span>

## <a name="assign-the-policy-to-a-cost-control-unit"></a><span data-ttu-id="7c191-132">İlkeyi bir maliyet kontrol birimine atayın</span><span class="sxs-lookup"><span data-stu-id="7c191-132">Assign the policy to a cost control unit</span></span>
1. <span data-ttu-id="7c191-133">Maliyet kontrol birimi için ilke atamaları'na tıklayın.</span><span class="sxs-lookup"><span data-stu-id="7c191-133">Click Policy assignments for cost control unit.</span></span>
2. <span data-ttu-id="7c191-134">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="7c191-134">Click New.</span></span>
3. <span data-ttu-id="7c191-135">Listede, seçili satırı işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="7c191-135">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="7c191-136">Geçerlilik tarihi muhasebe veri alanına bir tarih girin.</span><span class="sxs-lookup"><span data-stu-id="7c191-136">In the Valid from accounting date field, enter a date.</span></span>
    * <span data-ttu-id="7c191-137">Kuralların geçerlilik tarihi vardır.</span><span class="sxs-lookup"><span data-stu-id="7c191-137">The rules are date-effective.</span></span> <span data-ttu-id="7c191-138">Sistemdeki bir kullanıcı, yeni bir sürüm oluşturulmuşsa kuralların vadesini doldurabilir.</span><span class="sxs-lookup"><span data-stu-id="7c191-138">A user or the system can expire the rules if a newer version is created.</span></span>  
5. <span data-ttu-id="7c191-139">Maliyet kontrol birimi alanına bir değer girin veya bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="7c191-139">In the Cost control unit field, enter or select a value.</span></span>
6. <span data-ttu-id="7c191-140">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="7c191-140">Click Save.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]