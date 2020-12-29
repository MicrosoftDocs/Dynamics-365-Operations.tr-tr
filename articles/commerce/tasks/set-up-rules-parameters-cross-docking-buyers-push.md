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
ms.openlocfilehash: 9bccd92946783628dce37c3fd018e4dd927efd49
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "4416456"
---
# <a name="set-up-rules-and-parameters-for-cross-docking-and-buyers-push"></a><span data-ttu-id="10a17-103"> Çapraz sevk ve merkezi alım için kurallar ve parametreler ayarlama</span><span class="sxs-lookup"><span data-stu-id="10a17-103">Set up rules and parameters for cross docking and buyer's push</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="10a17-104">Bu yordam, Stok yenileme kuralları oluşturmak için gereken adımları gösterir.</span><span class="sxs-lookup"><span data-stu-id="10a17-104">This procedure demonstrates the steps to create Replenishment rules.</span></span> <span data-ttu-id="10a17-105">Stok yenileme kuralları, Çapraz sevk ve Merkezi alım kullanırken ürünlerin mağazalara nasıl dağıtıldığını denetlemek için kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="10a17-105">Replenishment rules can be used to control how products are distributed to stores when using Cross-docking and Buyer´s push.</span></span> <span data-ttu-id="10a17-106">Stok yenileme kuralları, mağazalar veya mağaza grupları için ayarlanabilir.</span><span class="sxs-lookup"><span data-stu-id="10a17-106">Replenishment rules can be set up for stores or store groups.</span></span> <span data-ttu-id="10a17-107">Kuraldaki her satır için tanımlanan ağırlık, Çapraz sevk veya Merkezi alımda dağıtım yöntemi olarak Stok yenilene kuralları kullanıldığında ürünlerin mağazalar arasında nasıl dağıtılacağını kontrol eder.</span><span class="sxs-lookup"><span data-stu-id="10a17-107">The weight defined for each line in a rule will control how the quantities of products will get distributed between the stores when using Replenishment rules as the distribution method in Cross-docking or Buyer´s push.</span></span> <span data-ttu-id="10a17-108">Bu yordam, USRT demo şirketini kullanır.</span><span class="sxs-lookup"><span data-stu-id="10a17-108">This procedure uses the USRT demo company.</span></span>

1. <span data-ttu-id="10a17-109">Stok Yenileme kuralları'na gidin.</span><span class="sxs-lookup"><span data-stu-id="10a17-109">Go to Replenishment rules.</span></span>
2. <span data-ttu-id="10a17-110">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="10a17-110">Click New.</span></span>
3. <span data-ttu-id="10a17-111">Stok yenilene kuralı alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="10a17-111">In the Replenishment rule field, type a value.</span></span>
4. <span data-ttu-id="10a17-112">Açıklama alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="10a17-112">In the Description field, type a value.</span></span>
5. <span data-ttu-id="10a17-113">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="10a17-113">Click Save.</span></span>
6. <span data-ttu-id="10a17-114">Ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="10a17-114">Click Add.</span></span>
7. <span data-ttu-id="10a17-115">Listede, seçili satırı işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="10a17-115">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="10a17-116">Tür için Stok yenileme hiyerarşisini veya Kanalı seçebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="10a17-116">You can choose Replenishment hierarchy or Channel for the type.</span></span> <span data-ttu-id="10a17-117">Değer, Ad bölümündeki seçimin kanallar hiyerarşisi mi yoksa belirli bir kanal mı olacağını denetler.</span><span class="sxs-lookup"><span data-stu-id="10a17-117">The value controls whether the selection in Name will be a hierarchy of channels or a specific channel.</span></span>  <span data-ttu-id="10a17-118">Bu örnekte, Stok yenileme hiyerarşisi ayarlanmış olarak bırakın.</span><span class="sxs-lookup"><span data-stu-id="10a17-118">For this example, leave it set as Replenishment hierarchy.</span></span>  
8. <span data-ttu-id="10a17-119">Ad alanından bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="10a17-119">In the Name field, select a value.</span></span>
    * <span data-ttu-id="10a17-120">Varsayılan ağırlık değeri ambar tanımlanan ağırlıkla doldurulur.</span><span class="sxs-lookup"><span data-stu-id="10a17-120">The default weight value is populated from the weight defined on the warehouse.</span></span>  <span data-ttu-id="10a17-121">Bu ağırlık Stok yenileme kuralı için kullanılabilir veya Ağırlık alanına yeni bir ağırlık girebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="10a17-121">This weight can be used for the Replenishment rule or you can enter a new weight in the Weight field.</span></span>  
9. <span data-ttu-id="10a17-122">Ağırlık alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="10a17-122">In the Weight field, enter a number.</span></span>
10. <span data-ttu-id="10a17-123">Ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="10a17-123">Click Add.</span></span>
11. <span data-ttu-id="10a17-124">Listede, seçili satırı işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="10a17-124">In the list, mark the selected row.</span></span>
12. <span data-ttu-id="10a17-125">Tür alanında 'Kanal'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="10a17-125">In the Type field, select 'Channel'.</span></span>
13. <span data-ttu-id="10a17-126">Ad alanına bir değer girin veya buradan bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="10a17-126">In the Name field, enter or select a value.</span></span>
14. <span data-ttu-id="10a17-127">Ağırlık alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="10a17-127">In the Weight field, enter a number.</span></span>
15. <span data-ttu-id="10a17-128">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="10a17-128">Click Save.</span></span>

