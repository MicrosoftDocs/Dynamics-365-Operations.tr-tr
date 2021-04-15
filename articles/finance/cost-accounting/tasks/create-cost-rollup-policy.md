---
title: Maliyet yuvarlaması ilkesi oluşturma
description: Bu yordam, bir maliyet yuvarlama ilkesini oluşturmayı ve ilke için kurallar oluşturmayı gösterir.
author: ShylaThompson
ms.date: 06/27/2017
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 50a50dc359dc4c2741ac4d280a9f97c6a7f2c259
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/01/2021
ms.locfileid: "5810033"
---
# <a name="create-a-cost-rollup-policy"></a><span data-ttu-id="d4a62-103">Maliyet yuvarlaması ilkesi oluşturma</span><span class="sxs-lookup"><span data-stu-id="d4a62-103">Create a cost rollup policy</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="d4a62-104">Bu yordam, bir maliyet yuvarlama ilkesini oluşturmayı ve ilke için kurallar oluşturmayı gösterir.</span><span class="sxs-lookup"><span data-stu-id="d4a62-104">This procedure shows how to create a cost rollup policy and create rules for the policy.</span></span> <span data-ttu-id="d4a62-105">Bu yöntemi oluşturmak için kullanılan demo verisi USP2'dir.</span><span class="sxs-lookup"><span data-stu-id="d4a62-105">The demo data used to create this procedure is USP2.</span></span>


## <a name="create-a-policy"></a><span data-ttu-id="d4a62-106">Bir ilke oluşturun</span><span class="sxs-lookup"><span data-stu-id="d4a62-106">Create a policy</span></span>
1. <span data-ttu-id="d4a62-107">Maliyet muhasebesi > İlkeler > Maliyet yuvarlama ilkeleri'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="d4a62-107">Go to Cost accounting > Policies > Cost rollup policies.</span></span>
2. <span data-ttu-id="d4a62-108">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="d4a62-108">Click New.</span></span>
3. <span data-ttu-id="d4a62-109">İlke adı alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="d4a62-109">In the Policy name field, type a value.</span></span>
4. <span data-ttu-id="d4a62-110">Açıklama alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="d4a62-110">In the Description field, type a value.</span></span>
5. <span data-ttu-id="d4a62-111">Maliyet nesnesi boyut hiyerarşisi alanına bir değer girin veya bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="d4a62-111">In the Cost object dimension hierarchy field, enter or select a value.</span></span>
    * <span data-ttu-id="d4a62-112">Maliyet yuvarlama CC'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="d4a62-112">Select Cost rollup CC.</span></span>  
6. <span data-ttu-id="d4a62-113">Maliyet öğesi boyut hiyerarşisi alanına bir değer girin veya bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="d4a62-113">In the Cost element dimension hierarchy field, enter or select a value.</span></span>
    * <span data-ttu-id="d4a62-114">Maliyet yuvarlama CC'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="d4a62-114">Select Cost rollup CC.</span></span>  
7. <span data-ttu-id="d4a62-115">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="d4a62-115">Click Save.</span></span>

## <a name="create-rules-for-the-cost-rollup-policy"></a><span data-ttu-id="d4a62-116">Maliyet yuvarlama ilkesi için kurallar oluşturun</span><span class="sxs-lookup"><span data-stu-id="d4a62-116">Create rules for the cost rollup policy</span></span>
1. <span data-ttu-id="d4a62-117">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="d4a62-117">Click New.</span></span>
2. <span data-ttu-id="d4a62-118">Listede, seçili satırı işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="d4a62-118">In the list, mark the selected row.</span></span>
3. <span data-ttu-id="d4a62-119">Maliyet nesnesi boyut hiyerarşi düğümü alanına bir değer girin veya bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="d4a62-119">In the Cost object dimension hierarchy node field, enter or select a value.</span></span>
    * <span data-ttu-id="d4a62-120">007'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="d4a62-120">Select 007.</span></span>  
4. <span data-ttu-id="d4a62-121">Maliyet öğesi boyut hiyerarşi düğümü alanına bir değer girin veya bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="d4a62-121">In the Cost element dimension hierarchy node field, enter or select a value.</span></span>
    * <span data-ttu-id="d4a62-122">Maliyet yuvarlama CE'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="d4a62-122">Select Cost rollup CE.</span></span>  
5. <span data-ttu-id="d4a62-123">İkincil maliyet öğesi alanına bir değer girin veya bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="d4a62-123">In the Secondary cost element field, enter or select a value.</span></span>
    * <span data-ttu-id="d4a62-124">Bu örnek için, ikincil maliyet öğesi CC-007'yi maliyet merkezine eşleyin.</span><span class="sxs-lookup"><span data-stu-id="d4a62-124">For this example, map the secondary cost element CC-007 to the cost center.</span></span>  
6. <span data-ttu-id="d4a62-125">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="d4a62-125">Click New.</span></span>
7. <span data-ttu-id="d4a62-126">Listede, seçili satırı işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="d4a62-126">In the list, mark the selected row.</span></span>
8. <span data-ttu-id="d4a62-127">Maliyet nesnesi boyut hiyerarşi düğümü alanına bir değer girin veya bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="d4a62-127">In the Cost object dimension hierarchy node field, enter or select a value.</span></span>
    * <span data-ttu-id="d4a62-128">008'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="d4a62-128">Select 008.</span></span>  
9. <span data-ttu-id="d4a62-129">Maliyet öğesi boyut hiyerarşi düğümü alanına bir değer girin veya bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="d4a62-129">In the Cost element dimension hierarchy node field, enter or select a value.</span></span>
    * <span data-ttu-id="d4a62-130">Maliyet yuvarlama CE'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="d4a62-130">Select Cost rollup CE.</span></span>  
10. <span data-ttu-id="d4a62-131">İkincil maliyet öğesi alanına bir değer girin veya bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="d4a62-131">In the Secondary cost element field, enter or select a value.</span></span>
    * <span data-ttu-id="d4a62-132">Bu örnek için, ikincil maliyet öğesi CC-008'yi maliyet merkezine eşleyin.</span><span class="sxs-lookup"><span data-stu-id="d4a62-132">For this example, map the secondary cost element CC-008 to the cost center.</span></span>  
11. <span data-ttu-id="d4a62-133">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="d4a62-133">Click New.</span></span>
12. <span data-ttu-id="d4a62-134">Listede, seçili satırı işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="d4a62-134">In the list, mark the selected row.</span></span>
13. <span data-ttu-id="d4a62-135">Maliyet nesnesi boyut hiyerarşi düğümü alanına bir değer girin veya bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="d4a62-135">In the Cost object dimension hierarchy node field, enter or select a value.</span></span>
    * <span data-ttu-id="d4a62-136">009'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="d4a62-136">Select 009.</span></span>  
14. <span data-ttu-id="d4a62-137">Maliyet öğesi boyut hiyerarşi düğümü alanına bir değer girin veya bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="d4a62-137">In the Cost element dimension hierarchy node field, enter or select a value.</span></span>
    * <span data-ttu-id="d4a62-138">Maliyet yuvarlama CE'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="d4a62-138">Select Cost rollup CE.</span></span>  
15. <span data-ttu-id="d4a62-139">İkincil maliyet öğesi alanına bir değer girin veya bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="d4a62-139">In the Secondary cost element field, enter or select a value.</span></span>
    * <span data-ttu-id="d4a62-140">Bu örnek için, ikincil maliyet öğesi CC-009'yi maliyet merkezine eşleyin.</span><span class="sxs-lookup"><span data-stu-id="d4a62-140">For this example, map the secondary cost element CC-009 to the cost center.</span></span>  
    * <span data-ttu-id="d4a62-141">Tüm maliyet merkezleri karşılık gelen ikincil maliyet öğelerine eşlenene kadar devam edin.</span><span class="sxs-lookup"><span data-stu-id="d4a62-141">Continue until all cost centers are mapped to their corresponding secondary cost elements.</span></span>  
16. <span data-ttu-id="d4a62-142">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="d4a62-142">Click Save.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]