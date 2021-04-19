---
title: " Merkezi alım kullanarak ürünleri dağıtım merkezinden mağazaya gönderme"
description: Bu yordam, ürünleri bir konumundan bir veya daha fazla mağazaya dağıtmak için Merkezi Alım oluşturma ve işleme konusunda kılavuzluk sağlar.
author: rubencdelgado
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: RetailBuyersPush, InventLocationIdLookup, InventItemIdLookupSimple, RetailReplenishmentTreeLookup
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.search.industry: Retail
ms.author: rubendel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a0fa48d7cd1af289cf455ebd0e0c14b047b4f1a4
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/31/2021
ms.locfileid: "5802659"
---
# <a name="push-products-from-distribution-center-to-store-using-buyers-push"></a><span data-ttu-id="efa5f-103"> Merkezi alım kullanarak ürünleri dağıtım merkezinden mağazaya gönderme</span><span class="sxs-lookup"><span data-stu-id="efa5f-103">Push products from distribution center to store using buyer's push</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="efa5f-104">Bu yordam, ürünleri bir konumundan bir veya daha fazla mağazaya dağıtmak için Merkezi Alım oluşturma ve işleme konusunda kılavuzluk sağlar.</span><span class="sxs-lookup"><span data-stu-id="efa5f-104">This procedure walks through the steps to create and process a Buyer´s push to distribute products from one location to one or many stores.</span></span> <span data-ttu-id="efa5f-105">Kullanıcı birden çok yapılandırmalar tanımlayabilir ve ürünlerin nasıl dağıtılacağını sistemin önermesini isteyebilir ya da ürünlerin nereye dağıtılacağını ve her mağazaya ne kadar dağıtım yapılacağını el ile girebilir.</span><span class="sxs-lookup"><span data-stu-id="efa5f-105">The user can define multiple configurations and have the system suggest how to distribute the products, or manually enter where the products are distributed to and how much gets distributed to each store.</span></span> <span data-ttu-id="efa5f-106">Bu yordam Merkezi Alımda kullanılabilecek stok yenileme kuralları, kuruluş hiyerarşileri ve mağaza ağırlıkları gibi verilerin ayarlanmasını kapsamaz.</span><span class="sxs-lookup"><span data-stu-id="efa5f-106">This procedure doesn't include setup of data that can be used in the Buyer´s push, such as replenishment rules, organizational hierarchies, and store weights.</span></span> <span data-ttu-id="efa5f-107">Bu yordam, USRT demo şirketini kullanır.</span><span class="sxs-lookup"><span data-stu-id="efa5f-107">This procedure uses the USRT demo company.</span></span>

1. <span data-ttu-id="efa5f-108">Merkezi alım'a gidin.</span><span class="sxs-lookup"><span data-stu-id="efa5f-108">Go to Buyer's push.</span></span>
2. <span data-ttu-id="efa5f-109">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="efa5f-109">Click New.</span></span>
3. <span data-ttu-id="efa5f-110">Açıklama alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="efa5f-110">In the Description field, type a value.</span></span>
4. <span data-ttu-id="efa5f-111">Tesis alanına bir değer girin veya buradan bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="efa5f-111">In the Site field, enter or select a value.</span></span>
5. <span data-ttu-id="efa5f-112">Ambar alanında, eldeki miktarları içeren ürünlerin bulunduğu bir mağaza girin veya seçin.</span><span class="sxs-lookup"><span data-stu-id="efa5f-112">In the Warehouse field, enter or select a warehouse that has products with on-hand quantities.</span></span>
6. <span data-ttu-id="efa5f-113">Ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="efa5f-113">Click Add.</span></span>
7. <span data-ttu-id="efa5f-114">Listede, seçili satırı işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="efa5f-114">In the list, mark the selected row.</span></span>
8. <span data-ttu-id="efa5f-115">Madde numarası alanına bir ürün girin veya bir ürün seçin.</span><span class="sxs-lookup"><span data-stu-id="efa5f-115">In the Item number field, enter or select a product.</span></span>
9. <span data-ttu-id="efa5f-116">Ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="efa5f-116">Click Add.</span></span>
10. <span data-ttu-id="efa5f-117">Listede, seçili satırı işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="efa5f-117">In the list, mark the selected row.</span></span>
11. <span data-ttu-id="efa5f-118">Madde numarası alanına bir varyant ürün girin veya seçin.</span><span class="sxs-lookup"><span data-stu-id="efa5f-118">In the Item number field, enter or select a variant product.</span></span>
    * <span data-ttu-id="efa5f-119">Bir varyant ürün girerken, her varyant için satırlar oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="efa5f-119">When entering a variant product, lines will be created for each variant.</span></span>  
12. <span data-ttu-id="efa5f-120">Listede, bir satırı işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="efa5f-120">In the list, mark a row.</span></span>
13. <span data-ttu-id="efa5f-121">Verilen miktar alanına, seçilen ürün için dağıtmak istediğiniz miktarı girin.</span><span class="sxs-lookup"><span data-stu-id="efa5f-121">In the Pushed quantity field, type how many of the selected product you want to distribute.</span></span>
14. <span data-ttu-id="efa5f-122">Verilecek ek miktar alanına, dağıtmak için kullanılabilir miktarı bulunan ürünlerin miktarını girin.</span><span class="sxs-lookup"><span data-stu-id="efa5f-122">In the Additional quantity to push field, enter the quantity of the products that have available quantity to distribute.</span></span>
15. <span data-ttu-id="efa5f-123">Dağıtım alanına 'Yerleşim ağırlığı' girin.</span><span class="sxs-lookup"><span data-stu-id="efa5f-123">In the Distribution field, enter 'Location weight'.</span></span>
    * <span data-ttu-id="efa5f-124">Dağıtım için diğer kuralları kullanmak üzere diğer türleri seçebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="efa5f-124">You can select the other types to use other rules for the distribution.</span></span>  
16. <span data-ttu-id="efa5f-125">Atok yenileme hiyerarşisi alanında bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="efa5f-125">In the Replenishment hierarchy field, select a value.</span></span>
17. <span data-ttu-id="efa5f-126">Ürün çeşitlerini dikkate al alanında Evet'i seçin.</span><span class="sxs-lookup"><span data-stu-id="efa5f-126">Select Yes in the Respect assortments field.</span></span>
18. <span data-ttu-id="efa5f-127">Miktarları hesapla'yı tıklayın ve Ambar bölümündeki satırlara eklenen miktarları gözden geçirin.</span><span class="sxs-lookup"><span data-stu-id="efa5f-127">Click Calculate quantities and review the quantities that are added to the rows in the Warehouse section.</span></span>
19. <span data-ttu-id="efa5f-128">Sipariş oluştur'u tıklayın.</span><span class="sxs-lookup"><span data-stu-id="efa5f-128">Click Create order.</span></span>
20. <span data-ttu-id="efa5f-129">Evet'i tıklatın.</span><span class="sxs-lookup"><span data-stu-id="efa5f-129">Click Yes.</span></span>



[!INCLUDE[footer-include](../../includes/footer-banner.md)]