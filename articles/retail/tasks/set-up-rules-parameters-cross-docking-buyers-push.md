---
title: " Çapraz sevk ve merkezi alım için kurallar ve parametreler ayarlama"
description: Bu yordam, Stok yenileme kuralları oluşturmak için gereken adımları gösterir.
author: josaw1
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: RetailReplenishmentRuleTable, RetailReplenishmentTreeLookup
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a22756279ba316a7efd4d09c48c55e8cc98ba29d
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2019
ms.locfileid: "366340"
---
# <a name="set-up-rules-and-parameters-for-cross-docking-and-buyers-push"></a><span data-ttu-id="42a95-103"> Çapraz sevk ve merkezi alım için kurallar ve parametreler ayarlama</span><span class="sxs-lookup"><span data-stu-id="42a95-103">Set up rules and parameters for cross docking and buyer's push</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="42a95-104">Bu yordam, Stok yenileme kuralları oluşturmak için gereken adımları gösterir.</span><span class="sxs-lookup"><span data-stu-id="42a95-104">This procedure demonstrates the steps to create Replenishment rules.</span></span> <span data-ttu-id="42a95-105">Stok yenileme kuralları, Çapraz sevk ve Merkezi alım kullanırken ürünlerin mağazalara nasıl dağıtıldığını denetlemek için kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="42a95-105">Replenishment rules can be used to control how products are distributed to stores when using Cross-docking and Buyer´s push.</span></span> <span data-ttu-id="42a95-106">Stok yenileme kuralları, mağazalar veya mağaza grupları için ayarlanabilir.</span><span class="sxs-lookup"><span data-stu-id="42a95-106">Replenishment rules can be set up for stores or store groups.</span></span> <span data-ttu-id="42a95-107">Kuraldaki her satır için tanımlanan ağırlık, Çapraz sevk veya Merkezi alımda dağıtım yöntemi olarak Stok yenilene kuralları kullanıldığında ürünlerin mağazalar arasında nasıl dağıtılacağını kontrol eder.</span><span class="sxs-lookup"><span data-stu-id="42a95-107">The weight defined for each line in a rule will control how the quantities of products will get distributed between the stores when using Replenishment rules as the distribution method in Cross-docking or Buyer´s push.</span></span> <span data-ttu-id="42a95-108">Bu yordam, USRT demo şirketini kullanır.</span><span class="sxs-lookup"><span data-stu-id="42a95-108">This procedure uses the USRT demo company.</span></span>

1. <span data-ttu-id="42a95-109">Stok Yenileme kuralları'na gidin.</span><span class="sxs-lookup"><span data-stu-id="42a95-109">Go to Replenishment rules.</span></span>
2. <span data-ttu-id="42a95-110">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="42a95-110">Click New.</span></span>
3. <span data-ttu-id="42a95-111">Stok yenilene kuralı alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="42a95-111">In the Replenishment rule field, type a value.</span></span>
4. <span data-ttu-id="42a95-112">Açıklama alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="42a95-112">In the Description field, type a value.</span></span>
5. <span data-ttu-id="42a95-113">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="42a95-113">Click Save.</span></span>
6. <span data-ttu-id="42a95-114">Ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="42a95-114">Click Add.</span></span>
7. <span data-ttu-id="42a95-115">Listede, seçili satırı işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="42a95-115">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="42a95-116">Tür için Stok yenileme hiyerarşisini veya Kanalı seçebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="42a95-116">You can choose Replenishment hierarchy or Channel for the type.</span></span> <span data-ttu-id="42a95-117">Değer, Ad bölümündeki seçimin kanallar hiyerarşisi mi yoksa belirli bir kanal mı olacağını denetler.</span><span class="sxs-lookup"><span data-stu-id="42a95-117">The value controls whether the selection in Name will be a hierarchy of channels or a specific channel.</span></span>  <span data-ttu-id="42a95-118">Bu örnekte, Stok yenileme hiyerarşisi ayarlanmış olarak bırakın.</span><span class="sxs-lookup"><span data-stu-id="42a95-118">For this example, leave it set as Replenishment hierarchy.</span></span>  
8. <span data-ttu-id="42a95-119">Ad alanından bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="42a95-119">In the Name field, select a value.</span></span>
    * <span data-ttu-id="42a95-120">Varsayılan ağırlık değeri ambar tanımlanan ağırlıkla doldurulur.</span><span class="sxs-lookup"><span data-stu-id="42a95-120">The default weight value is populated from the weight defined on the warehouse.</span></span>  <span data-ttu-id="42a95-121">Bu ağırlık Stok yenileme kuralı için kullanılabilir veya Ağırlık alanına yeni bir ağırlık girebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="42a95-121">This weight can be used for the Replenishment rule or you can enter a new weight in the Weight field.</span></span>  
9. <span data-ttu-id="42a95-122">Ağırlık alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="42a95-122">In the Weight field, enter a number.</span></span>
10. <span data-ttu-id="42a95-123">Ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="42a95-123">Click Add.</span></span>
11. <span data-ttu-id="42a95-124">Listede, seçili satırı işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="42a95-124">In the list, mark the selected row.</span></span>
12. <span data-ttu-id="42a95-125">Tür alanında 'Kanal'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="42a95-125">In the Type field, select 'Channel'.</span></span>
13. <span data-ttu-id="42a95-126">Ad alanına bir değer girin veya buradan bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="42a95-126">In the Name field, enter or select a value.</span></span>
14. <span data-ttu-id="42a95-127">Ağırlık alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="42a95-127">In the Weight field, enter a number.</span></span>
15. <span data-ttu-id="42a95-128">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="42a95-128">Click Save.</span></span>

