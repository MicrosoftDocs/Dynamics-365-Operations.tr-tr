---
title: Maliyet yuvarlaması ilkesi oluşturma
description: Bu yordam, bir maliyet yuvarlama ilkesini oluşturmayı ve ilke için kurallar oluşturmayı gösterir.
author: ShylaThompson
manager: AnnBe
ms.date: 06/27/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6505d658103a4c34dfe7c7eb86ad4ea41515ccfb
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5261296"
---
# <a name="create-a-cost-rollup-policy"></a><span data-ttu-id="8b221-103">Maliyet yuvarlaması ilkesi oluşturma</span><span class="sxs-lookup"><span data-stu-id="8b221-103">Create a cost rollup policy</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="8b221-104">Bu yordam, bir maliyet yuvarlama ilkesini oluşturmayı ve ilke için kurallar oluşturmayı gösterir.</span><span class="sxs-lookup"><span data-stu-id="8b221-104">This procedure shows how to create a cost rollup policy and create rules for the policy.</span></span> <span data-ttu-id="8b221-105">Bu yöntemi oluşturmak için kullanılan demo verisi USP2'dir.</span><span class="sxs-lookup"><span data-stu-id="8b221-105">The demo data used to create this procedure is USP2.</span></span>


## <a name="create-a-policy"></a><span data-ttu-id="8b221-106">Bir ilke oluşturun</span><span class="sxs-lookup"><span data-stu-id="8b221-106">Create a policy</span></span>
1. <span data-ttu-id="8b221-107">Maliyet muhasebesi > İlkeler > Maliyet yuvarlama ilkeleri'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="8b221-107">Go to Cost accounting > Policies > Cost rollup policies.</span></span>
2. <span data-ttu-id="8b221-108">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="8b221-108">Click New.</span></span>
3. <span data-ttu-id="8b221-109">İlke adı alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="8b221-109">In the Policy name field, type a value.</span></span>
4. <span data-ttu-id="8b221-110">Açıklama alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="8b221-110">In the Description field, type a value.</span></span>
5. <span data-ttu-id="8b221-111">Maliyet nesnesi boyut hiyerarşisi alanına bir değer girin veya bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="8b221-111">In the Cost object dimension hierarchy field, enter or select a value.</span></span>
    * <span data-ttu-id="8b221-112">Maliyet yuvarlama CC'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="8b221-112">Select Cost rollup CC.</span></span>  
6. <span data-ttu-id="8b221-113">Maliyet öğesi boyut hiyerarşisi alanına bir değer girin veya bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="8b221-113">In the Cost element dimension hierarchy field, enter or select a value.</span></span>
    * <span data-ttu-id="8b221-114">Maliyet yuvarlama CC'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="8b221-114">Select Cost rollup CC.</span></span>  
7. <span data-ttu-id="8b221-115">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="8b221-115">Click Save.</span></span>

## <a name="create-rules-for-the-cost-rollup-policy"></a><span data-ttu-id="8b221-116">Maliyet yuvarlama ilkesi için kurallar oluşturun</span><span class="sxs-lookup"><span data-stu-id="8b221-116">Create rules for the cost rollup policy</span></span>
1. <span data-ttu-id="8b221-117">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="8b221-117">Click New.</span></span>
2. <span data-ttu-id="8b221-118">Listede, seçili satırı işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="8b221-118">In the list, mark the selected row.</span></span>
3. <span data-ttu-id="8b221-119">Maliyet nesnesi boyut hiyerarşi düğümü alanına bir değer girin veya bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="8b221-119">In the Cost object dimension hierarchy node field, enter or select a value.</span></span>
    * <span data-ttu-id="8b221-120">007'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="8b221-120">Select 007.</span></span>  
4. <span data-ttu-id="8b221-121">Maliyet öğesi boyut hiyerarşi düğümü alanına bir değer girin veya bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="8b221-121">In the Cost element dimension hierarchy node field, enter or select a value.</span></span>
    * <span data-ttu-id="8b221-122">Maliyet yuvarlama CE'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="8b221-122">Select Cost rollup CE.</span></span>  
5. <span data-ttu-id="8b221-123">İkincil maliyet öğesi alanına bir değer girin veya bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="8b221-123">In the Secondary cost element field, enter or select a value.</span></span>
    * <span data-ttu-id="8b221-124">Bu örnek için, ikincil maliyet öğesi CC-007'yi maliyet merkezine eşleyin.</span><span class="sxs-lookup"><span data-stu-id="8b221-124">For this example, map the secondary cost element CC-007 to the cost center.</span></span>  
6. <span data-ttu-id="8b221-125">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="8b221-125">Click New.</span></span>
7. <span data-ttu-id="8b221-126">Listede, seçili satırı işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="8b221-126">In the list, mark the selected row.</span></span>
8. <span data-ttu-id="8b221-127">Maliyet nesnesi boyut hiyerarşi düğümü alanına bir değer girin veya bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="8b221-127">In the Cost object dimension hierarchy node field, enter or select a value.</span></span>
    * <span data-ttu-id="8b221-128">008'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="8b221-128">Select 008.</span></span>  
9. <span data-ttu-id="8b221-129">Maliyet öğesi boyut hiyerarşi düğümü alanına bir değer girin veya bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="8b221-129">In the Cost element dimension hierarchy node field, enter or select a value.</span></span>
    * <span data-ttu-id="8b221-130">Maliyet yuvarlama CE'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="8b221-130">Select Cost rollup CE.</span></span>  
10. <span data-ttu-id="8b221-131">İkincil maliyet öğesi alanına bir değer girin veya bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="8b221-131">In the Secondary cost element field, enter or select a value.</span></span>
    * <span data-ttu-id="8b221-132">Bu örnek için, ikincil maliyet öğesi CC-008'yi maliyet merkezine eşleyin.</span><span class="sxs-lookup"><span data-stu-id="8b221-132">For this example, map the secondary cost element CC-008 to the cost center.</span></span>  
11. <span data-ttu-id="8b221-133">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="8b221-133">Click New.</span></span>
12. <span data-ttu-id="8b221-134">Listede, seçili satırı işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="8b221-134">In the list, mark the selected row.</span></span>
13. <span data-ttu-id="8b221-135">Maliyet nesnesi boyut hiyerarşi düğümü alanına bir değer girin veya bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="8b221-135">In the Cost object dimension hierarchy node field, enter or select a value.</span></span>
    * <span data-ttu-id="8b221-136">009'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="8b221-136">Select 009.</span></span>  
14. <span data-ttu-id="8b221-137">Maliyet öğesi boyut hiyerarşi düğümü alanına bir değer girin veya bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="8b221-137">In the Cost element dimension hierarchy node field, enter or select a value.</span></span>
    * <span data-ttu-id="8b221-138">Maliyet yuvarlama CE'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="8b221-138">Select Cost rollup CE.</span></span>  
15. <span data-ttu-id="8b221-139">İkincil maliyet öğesi alanına bir değer girin veya bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="8b221-139">In the Secondary cost element field, enter or select a value.</span></span>
    * <span data-ttu-id="8b221-140">Bu örnek için, ikincil maliyet öğesi CC-009'yi maliyet merkezine eşleyin.</span><span class="sxs-lookup"><span data-stu-id="8b221-140">For this example, map the secondary cost element CC-009 to the cost center.</span></span>  
    * <span data-ttu-id="8b221-141">Tüm maliyet merkezleri karşılık gelen ikincil maliyet öğelerine eşlenene kadar devam edin.</span><span class="sxs-lookup"><span data-stu-id="8b221-141">Continue until all cost centers are mapped to their corresponding secondary cost elements.</span></span>  
16. <span data-ttu-id="8b221-142">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="8b221-142">Click Save.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]