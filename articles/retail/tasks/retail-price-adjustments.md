--- 
title: " Perakende fiyat ayarlamaları"
description: "Bu yordam, bir perakende fiyat ayarlaması oluşturma konusunda yol gösterir."
author: josaw1
manager: AnnBe
ms.date: 06/07/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations, Retail
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 191f48bc5b56bef9fe08c266db8cd49ce7cbc620
ms.contentlocale: tr-tr
ms.lasthandoff: 04/13/2018

---
# <a name="retail-price-adjustments"></a><span data-ttu-id="3819c-103"> Perakende fiyat ayarlamaları</span><span class="sxs-lookup"><span data-stu-id="3819c-103">Retail price adjustments</span></span>

[!INCLUDE [task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="3819c-104">Bu yordam, bir perakende fiyat ayarlaması oluşturma konusunda yol gösterir.</span><span class="sxs-lookup"><span data-stu-id="3819c-104">This procedure will walk through creating a retail price adjustment.</span></span> <span data-ttu-id="3819c-105">Perakende fiyat ayarlaması, maddenin satış fiyatı doğrudan ayarlayabilir veya taban satış fiyatını ya da ticaret anlaşması satış fiyatını değiştirebilir.</span><span class="sxs-lookup"><span data-stu-id="3819c-105">A retail price adjustment can set an item's sale price directly, or modify its base sale price or trade agreement sale price.</span></span> <span data-ttu-id="3819c-106">Bu yordam, USRT demo veri şirketini kullanır.</span><span class="sxs-lookup"><span data-stu-id="3819c-106">This procedure uses the USRT demo data company.</span></span>

1. <span data-ttu-id="3819c-107">Fiyatlandırma ve iskonto yönetimi öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="3819c-107">Click Pricing and discount management.</span></span>
2. <span data-ttu-id="3819c-108">Fiyat ayarlamaları sekmesini tıklayın.</span><span class="sxs-lookup"><span data-stu-id="3819c-108">Click the Price adjustments tab.</span></span>
3. <span data-ttu-id="3819c-109">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="3819c-109">Click New.</span></span>
    * <span data-ttu-id="3819c-110">Buradan perakende indirimler, fiyat ayarlamaları, ticari anlaşma günlükleri ve kategori fiyatlandırma kuralları dahil olmak üzere en yaygın kullanılan tüm fiyat ve iskonto kurallarını oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="3819c-110">From here you can create all of the most commonly used price and discount rules, including retail discounts, price adjustments, trade agreement journals, and category pricing rules.</span></span>  
4. <span data-ttu-id="3819c-111">Fiyat ayarlaması'nı tıklayın.</span><span class="sxs-lookup"><span data-stu-id="3819c-111">Click Price adjustment.</span></span>
5. <span data-ttu-id="3819c-112">İsim alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="3819c-112">In the Name field, type a value.</span></span>
6. <span data-ttu-id="3819c-113">Satırlar bölümünü genişletin.</span><span class="sxs-lookup"><span data-stu-id="3819c-113">Expand the Lines section.</span></span>
7. <span data-ttu-id="3819c-114">Ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="3819c-114">Click Add.</span></span>
    * <span data-ttu-id="3819c-115">Bu örnekte, Ürün alanına '81126' girin.</span><span class="sxs-lookup"><span data-stu-id="3819c-115">For this example, enter '81126' in the Product field.</span></span>    <span data-ttu-id="3819c-116">Ardından, İskonto yüzdesi alanına '10,0' yazın.</span><span class="sxs-lookup"><span data-stu-id="3819c-116">Then, enter '10.0' in the Discount percentage field.</span></span>  
    * <span data-ttu-id="3819c-117">İskonto yüzdesi türü fiyat ayarlaması, temel satış fiyatını veya ticaret anlaşması satış fiyatını düşürür.</span><span class="sxs-lookup"><span data-stu-id="3819c-117">A discount percentage type price adjustment will reduce a base sales price or trade agreement sales price.</span></span>  
8. <span data-ttu-id="3819c-118">Ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="3819c-118">Click Add.</span></span>
    * <span data-ttu-id="3819c-119">Bu örnekte, Ürün alanına '81125' girin.</span><span class="sxs-lookup"><span data-stu-id="3819c-119">For this example, enter '81125' in the Product field.</span></span>    <span data-ttu-id="3819c-120">Ardından İskonto yöntemi alanında 'Nakit iskontosu tutarı'nı seçin.</span><span class="sxs-lookup"><span data-stu-id="3819c-120">Then, select 'Cash discount amount' in the Discount method field.</span></span>    <span data-ttu-id="3819c-121">Son olarak, Nakit iskontosu tutarı alanına '5,0' girin.</span><span class="sxs-lookup"><span data-stu-id="3819c-121">Finally, enter '5.0' in the Cash discount amount field.</span></span>  
    * <span data-ttu-id="3819c-122">Nakit iskontosu tutarı iskonto türü, taban fiyat ya da ticaret anlaşmasından alınan tutardır.</span><span class="sxs-lookup"><span data-stu-id="3819c-122">A Cash discount amount discount type is an amount taken off from a base price or a trade agreement price.</span></span>  
9. <span data-ttu-id="3819c-123">Fiyat grupları'na tıklayın.</span><span class="sxs-lookup"><span data-stu-id="3819c-123">Click Price groups.</span></span>
    * <span data-ttu-id="3819c-124">Fiyat grubu alanında 'RP-Houston'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="3819c-124">Select 'RP-Houston' in the Price group field.</span></span>  
    * <span data-ttu-id="3819c-125">Bu Fiyat ayarlamasını Houston mağazasıyla ilişkilendirir.</span><span class="sxs-lookup"><span data-stu-id="3819c-125">This will associate the Price adjustment to the Houston store.</span></span>  
10. <span data-ttu-id="3819c-126">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="3819c-126">Click Save.</span></span>
11. <span data-ttu-id="3819c-127">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="3819c-127">Close the page.</span></span>
12. <span data-ttu-id="3819c-128">Durum alanında, 'Etkin'i seçin.</span><span class="sxs-lookup"><span data-stu-id="3819c-128">In the Status field, select 'Enabled'.</span></span>
13. <span data-ttu-id="3819c-129">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="3819c-129">Click Save.</span></span>
14. <span data-ttu-id="3819c-130">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="3819c-130">Close the page.</span></span>
15. <span data-ttu-id="3819c-131">Sayfayı yenileyin.</span><span class="sxs-lookup"><span data-stu-id="3819c-131">Refresh the page.</span></span>


