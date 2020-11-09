---
title: 'Kısmi konum döngü sayımı işlemini tanımlama '
description: Sayım işi oluştururken döngü sayımı planları kullanırsanız, gerçek sayma operasyonunu, konumda bulunan eldeki stokların yerine yalnızca çeşitli ürünler ve ürün çeşitlerinin sayılmasına yönlendirebilirsiniz.
author: ShylaThompson
manager: tfehr
ms.date: 06/23/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSRFMenuItemCycleCount, WHSCycleCountPlan, WHSCycleCountPlanListPage, WHSWorkTemplateTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Operations
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 39a256a5a88a6d70373d6e23f1f380da6791f418
ms.sourcegitcommit: a36a4f9915ae3eb36bf8220111cf1486387713d9
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4016091"
---
# <a name="define-partial-location-cycle-counting-process"></a><span data-ttu-id="bfd94-103">Kısmi konum döngü sayımı işlemini tanımlama </span><span class="sxs-lookup"><span data-stu-id="bfd94-103">Define partial location cycle counting process</span></span> 

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="bfd94-104">Sayım işi oluştururken döngü sayımı planları kullanırsanız, gerçek sayma operasyonunu, konumda bulunan eldeki stokların yerine yalnızca çeşitli ürünler ve ürün çeşitlerinin sayılmasına yönlendirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="bfd94-104">When you use cycle count plans to create counting work, you can guide the actual counting operations by requesting that only specific products and product variants be counted instead of all on-hand inventory at the location.</span></span> <span data-ttu-id="bfd94-105">Belirli ürünleri filtreleyerek, ambar yöneticisi inceleme yükünü azaltabilir, konsolidasyon hatalarının önlemeye yardımcı olabilir ve zaman tasarruf edebilir.</span><span class="sxs-lookup"><span data-stu-id="bfd94-105">By filtering on specific products, the warehouse manager can reduce review overhead, help prevent consolidation mistakes, and save time.</span></span> <span data-ttu-id="bfd94-106">Bir ambar yöneticisi tipik olarak kurulum görevlerini gerçekleştirir.</span><span class="sxs-lookup"><span data-stu-id="bfd94-106">Typically, a warehouse manager performs the setup tasks.</span></span> <span data-ttu-id="bfd94-107">Bu yordamı demo verileri şirketi USMF veya kendi verilerinizi kullanarak yerine getirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="bfd94-107">You can go through this procedure in the USMF demo data company or in your own data.</span></span>


## <a name="create-a-cycle-counting-work-template"></a><span data-ttu-id="bfd94-108">Bir döngü sayımı iş şablonu oluşturun</span><span class="sxs-lookup"><span data-stu-id="bfd94-108">Create a cycle counting work template</span></span>
1. <span data-ttu-id="bfd94-109">Ambar yönetimi > Kurulum > İş > İş şablonları öğesine gidin.</span><span class="sxs-lookup"><span data-stu-id="bfd94-109">Go to Warehouse management > Setup > Work > Work templates.</span></span>
2. <span data-ttu-id="bfd94-110">İş siparişi türü alanında 'Döngü sayımı' seçin.</span><span class="sxs-lookup"><span data-stu-id="bfd94-110">In the Work order type field, select 'Cycle counting'.</span></span>
3. <span data-ttu-id="bfd94-111">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="bfd94-111">Click New.</span></span>
4. <span data-ttu-id="bfd94-112">Sıra numarası alanına bir numara girin.</span><span class="sxs-lookup"><span data-stu-id="bfd94-112">In the Sequence number field, enter a number.</span></span>
    * <span data-ttu-id="bfd94-113">Sıralama düzeni en küçük sayıdan en büyük sayıyadır.</span><span class="sxs-lookup"><span data-stu-id="bfd94-113">The sort order is from the smallest number to the largest number.</span></span> <span data-ttu-id="bfd94-114">Değer 0'dan (sıfır) fazla olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="bfd94-114">The value must be more than 0 (zero).</span></span>  
5. <span data-ttu-id="bfd94-115">Listede, seçili satırı işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="bfd94-115">In the list, mark the selected row.</span></span>
6. <span data-ttu-id="bfd94-116">İş şablonu alanında bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="bfd94-116">In the Work template field, type a value.</span></span>
7. <span data-ttu-id="bfd94-117">İş şablonu açıklaması alanında bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="bfd94-117">In the Work template description field, type a value.</span></span>
8. <span data-ttu-id="bfd94-118">İş havuz kodu alanında bir değer girin veya bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="bfd94-118">In the Work pool ID field, enter or select a value.</span></span>
9. <span data-ttu-id="bfd94-119">İş önceliği alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="bfd94-119">In the Work priority field, enter a number.</span></span>
10. <span data-ttu-id="bfd94-120">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="bfd94-120">Click Save.</span></span>
11. <span data-ttu-id="bfd94-121">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="bfd94-121">Click New.</span></span>
12. <span data-ttu-id="bfd94-122">Listede, seçili satırı işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="bfd94-122">In the list, mark the selected row.</span></span>
13. <span data-ttu-id="bfd94-123">İş türü alanında 'Sayım'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="bfd94-123">In the Work type field, select 'Counting'.</span></span>
14. <span data-ttu-id="bfd94-124">İş sınıfı kodu alanına bir değer girin veya buradan bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="bfd94-124">In the Work class ID field, enter or select a value.</span></span>
15. <span data-ttu-id="bfd94-125">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="bfd94-125">Click Save.</span></span>
16. <span data-ttu-id="bfd94-126">İş satırı molaları'na tıklayın.</span><span class="sxs-lookup"><span data-stu-id="bfd94-126">Click Work line breaks.</span></span>
17. <span data-ttu-id="bfd94-127">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="bfd94-127">Click New.</span></span>
18. <span data-ttu-id="bfd94-128">Sıra numarası alanına bir numara girin.</span><span class="sxs-lookup"><span data-stu-id="bfd94-128">In the Sequence number field, enter a number.</span></span>
    * <span data-ttu-id="bfd94-129">Sıralama düzeni en küçük sayıdan en büyük sayıyadır.</span><span class="sxs-lookup"><span data-stu-id="bfd94-129">The sort order is from the smallest number to the largest number.</span></span> <span data-ttu-id="bfd94-130">Değer 0'dan (sıfır) fazla olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="bfd94-130">The value must be more than 0 (zero).</span></span>  
19. <span data-ttu-id="bfd94-131">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="bfd94-131">Click Save.</span></span>
20. <span data-ttu-id="bfd94-132">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="bfd94-132">Close the page.</span></span>
21. <span data-ttu-id="bfd94-133">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="bfd94-133">Close the page.</span></span>

## <a name="create-a-cycle-counting-plan"></a><span data-ttu-id="bfd94-134">Bir döngü sayımı planı oluşturun</span><span class="sxs-lookup"><span data-stu-id="bfd94-134">Create a cycle counting plan</span></span>
1. <span data-ttu-id="bfd94-135">Ambar yönetimi > Kurulum > Döngü sayımı > Döngü sayımı planları öğesine gidin.</span><span class="sxs-lookup"><span data-stu-id="bfd94-135">Go to Warehouse management > Setup > Cycle counting > Cycle count plans.</span></span>
2. <span data-ttu-id="bfd94-136">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="bfd94-136">Click New.</span></span>
3. <span data-ttu-id="bfd94-137">Döngü sayımı planı numarası alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="bfd94-137">In the Cycle counting plan ID field, type a value.</span></span>
4. <span data-ttu-id="bfd94-138">Tanım alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="bfd94-138">In the Description field, type a value.</span></span>
5. <span data-ttu-id="bfd94-139">Maksimum döngü sayımı miktarı alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="bfd94-139">In the Maximum number of cycle counts field, enter a number.</span></span>
6. <span data-ttu-id="bfd94-140">İş şablonu alanında bir değer girin veya bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="bfd94-140">In the Work template field, enter or select a value.</span></span>
7. <span data-ttu-id="bfd94-141">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="bfd94-141">Click New.</span></span>
8. <span data-ttu-id="bfd94-142">Sıra numarası alanına bir numara girin.</span><span class="sxs-lookup"><span data-stu-id="bfd94-142">In the Sequence number field, enter a number.</span></span>
    * <span data-ttu-id="bfd94-143">Sıralama düzeni en küçük sayıdan en büyük sayıyadır.</span><span class="sxs-lookup"><span data-stu-id="bfd94-143">The sort order is from the smallest number to the largest number.</span></span> <span data-ttu-id="bfd94-144">Değer 0'dan (sıfır) fazla olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="bfd94-144">The value must be more than 0 (zero).</span></span>  
9. <span data-ttu-id="bfd94-145">Açıklama alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="bfd94-145">In the Description field, type a value.</span></span>
10. <span data-ttu-id="bfd94-146">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="bfd94-146">Click Save.</span></span>
11. <span data-ttu-id="bfd94-147">Ürün sorgusu tanımla'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="bfd94-147">Click Define product query.</span></span>
12. <span data-ttu-id="bfd94-148">Listede, seçili satırı işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="bfd94-148">In the list, mark the selected row.</span></span>
13. <span data-ttu-id="bfd94-149">Ölçütler alanında bir değer girin veya seçin.</span><span class="sxs-lookup"><span data-stu-id="bfd94-149">In the Criteria field, enter or select a value.</span></span>
14. <span data-ttu-id="bfd94-150">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="bfd94-150">Click OK.</span></span>
15. <span data-ttu-id="bfd94-151">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="bfd94-151">Close the page.</span></span>

