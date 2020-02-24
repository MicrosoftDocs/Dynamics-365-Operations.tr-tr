---
title: Taban fiyat ve ticari sözleşmeler
description: Bu yordam kanala özel bir satış fiyatı ticari anlaşmaları oluşturma sürecini gösterir.
author: josaw1
manager: AnnBe
ms.date: 08/12/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PriceDiscGroup, RetailStoreTable, RetailChannelPriceGroup, EcoResProductDetailsExtended, PriceDiscAdmTable, PriceDiscAdm
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 7576c4218118724562ff739ff9805a06b7ba22d5
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/01/2020
ms.locfileid: "3024336"
---
# <a name="base-price-and-trade-agreements"></a><span data-ttu-id="5ddc7-103">Taban fiyat ve ticari sözleşmeler</span><span class="sxs-lookup"><span data-stu-id="5ddc7-103">Base price and trade agreements</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="5ddc7-104">Bu yordam kanala özel bir satış fiyatı ticari anlaşmaları oluşturma sürecini gösterir.</span><span class="sxs-lookup"><span data-stu-id="5ddc7-104">This procedure walks through creating channel-specific sales price trade agreements.</span></span> <span data-ttu-id="5ddc7-105">Bu yordam, USRT demo veri şirketini kullanır.</span><span class="sxs-lookup"><span data-stu-id="5ddc7-105">This procedure uses the USRT demo data company.</span></span>

1. <span data-ttu-id="5ddc7-106">**Gezinti bölmesinde**, **Modüller > Retail and Commerce > Fiyatlandırma ve indirim yönetimi > Fiyat grupları > Tüm fiyat grupları**'na gidin.</span><span class="sxs-lookup"><span data-stu-id="5ddc7-106">In the **Navigation pane**, go to **Modules > Retail and Commerce > Pricing and discounts management > Price groups > All price groups**.</span></span> <span data-ttu-id="5ddc7-107">Fiyat grupları, ticari anlaşmaların belirli kanallara nasıl atandığıyla ilgilidir.</span><span class="sxs-lookup"><span data-stu-id="5ddc7-107">Price groups are how trade agreements are assigned to specific channels.</span></span> <span data-ttu-id="5ddc7-108">Ticari anlaşmaları bir kanala atamak için fiyat grupları kullanmak kanala özel fiyatlandırma sağlar.</span><span class="sxs-lookup"><span data-stu-id="5ddc7-108">Using price groups to assign trade agreements to a channel enables channel-specific pricing.</span></span>  
2. <span data-ttu-id="5ddc7-109">**Yeni**'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="5ddc7-109">Click **New**.</span></span>
3. <span data-ttu-id="5ddc7-110">**Fiyat grupları** alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="5ddc7-110">In the **Price groups** field, type a value.</span></span>
4. <span data-ttu-id="5ddc7-111">**Ad** alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="5ddc7-111">In the **Name** field, type a value.</span></span>
5. <span data-ttu-id="5ddc7-112">**Kaydet**'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="5ddc7-112">Click **Save**.</span></span>
6. <span data-ttu-id="5ddc7-113">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="5ddc7-113">Close the page.</span></span>
7. <span data-ttu-id="5ddc7-114">**Gezinti bölmesinde**, **Modüller > Retail and Commerce > Kanallar > Mağazaları > Tüm mağazalar**'a gidin.</span><span class="sxs-lookup"><span data-stu-id="5ddc7-114">In the **Navigation pane**, go to **Modules > Retail and Commerce > Channels > Stores > All stores**.</span></span>
8. <span data-ttu-id="5ddc7-115">Listeden 'New York'u seçin.</span><span class="sxs-lookup"><span data-stu-id="5ddc7-115">In the list, select 'New York'</span></span>
9. <span data-ttu-id="5ddc7-116">Eylem Bölmesinde **Mağaza**'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="5ddc7-116">On the Action Pane, click **Store**.</span></span>
10. <span data-ttu-id="5ddc7-117">**Fiyat grupları**'na tıklayın.</span><span class="sxs-lookup"><span data-stu-id="5ddc7-117">Click **Price groups**.</span></span>
11. <span data-ttu-id="5ddc7-118">**Yeni**'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="5ddc7-118">Click **New**.</span></span>
12. <span data-ttu-id="5ddc7-119">**Fiyat grupları** alanında, aramayı açmak için açılır menü düğmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="5ddc7-119">In the **Price groups** field, click the drop-down button to open the lookup.</span></span>
13. <span data-ttu-id="5ddc7-120">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="5ddc7-120">In the list, find and select the desired record.</span></span>
14. <span data-ttu-id="5ddc7-121">**Kaydet**'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="5ddc7-121">Click **Save**.</span></span>
15. <span data-ttu-id="5ddc7-122">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="5ddc7-122">Close the page.</span></span>
16. <span data-ttu-id="5ddc7-123">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="5ddc7-123">Close the page.</span></span>
17. <span data-ttu-id="5ddc7-124">**Gezinti bölmesinde**, **Modüller > Retail and Commerce > Ürünler ve kategoriler > Kategoriye göre serbest bırakılan ürünler**'e gidin.</span><span class="sxs-lookup"><span data-stu-id="5ddc7-124">In the **Navigation pane**, go to **Modules > Retail and Commerce > Products and categories > Released products by category**.</span></span>
18. <span data-ttu-id="5ddc7-125">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="5ddc7-125">In the list, click the link in the selected row.</span></span>
19. <span data-ttu-id="5ddc7-126">**Düzenle**'yi tıklatın.</span><span class="sxs-lookup"><span data-stu-id="5ddc7-126">Click **Edit**.</span></span>
20. <span data-ttu-id="5ddc7-127">**Satış** hızlı sekmesini genişletin.</span><span class="sxs-lookup"><span data-stu-id="5ddc7-127">Expand the **Sell** fastTab.</span></span>
21. <span data-ttu-id="5ddc7-128">**Fiyat** alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="5ddc7-128">In the **Price** field, enter a number.</span></span> <span data-ttu-id="5ddc7-129">Geçerli herhangi bir ticari anlaşma bulunamazsa bu fiyat kullanılır.</span><span class="sxs-lookup"><span data-stu-id="5ddc7-129">This price is used if no applicable trade agreements are found.</span></span>  
22. <span data-ttu-id="5ddc7-130">**Kaydet**'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="5ddc7-130">Click **Save**.</span></span>
23. <span data-ttu-id="5ddc7-131">**Eylem bölmesi**'nde, **Satış**'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="5ddc7-131">On the **Action Pane**, click **Sell**.</span></span>
24. <span data-ttu-id="5ddc7-132">**Ticari anlaşmalar oluştur**'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="5ddc7-132">Click **Create trade agreements**.</span></span>
25. <span data-ttu-id="5ddc7-133">**Yeni**'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="5ddc7-133">Click **New**.</span></span>
26. <span data-ttu-id="5ddc7-134">**Ad** alanında, açılır menü düğmesine tıklayarak aramayı açın.</span><span class="sxs-lookup"><span data-stu-id="5ddc7-134">In the **Name** field, click the drop-down button to open the lookup.</span></span>
27. <span data-ttu-id="5ddc7-135">Listede, **Commerce**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="5ddc7-135">In the list, select **Commerce**.</span></span> <span data-ttu-id="5ddc7-136">Tanıtım verilerinde **Commerce** günlük adının varsayılan ilişkisi **Fiyat (satış)**'tır.</span><span class="sxs-lookup"><span data-stu-id="5ddc7-136">In the demo data, the **Commerce** journal name has the default relation of **Price (sales)**.</span></span> <span data-ttu-id="5ddc7-137">Bu, yeni oluşturulan tüm satırların varsayılan olarak satış fiyatı ticari anlaşmalarına ayarlanır.</span><span class="sxs-lookup"><span data-stu-id="5ddc7-137">That means all new lines created will default to sales price trade agreements.</span></span>  
28. <span data-ttu-id="5ddc7-138">**Eylem Bölmesi**'nde, **Satırlar** öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="5ddc7-138">On the **Action pane**, click **Lines**.</span></span>
29. <span data-ttu-id="5ddc7-139">**Hesap kodu** alanında 'Grup'u seçin.</span><span class="sxs-lookup"><span data-stu-id="5ddc7-139">In the **Account code** field, select 'Group'.</span></span>
30. <span data-ttu-id="5ddc7-140">**Hesap seçimi** alanında, aramayı açmak için açılır menü düğmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="5ddc7-140">In the **Account selection** field, click the drop-down button to open the lookup.</span></span>
31. <span data-ttu-id="5ddc7-141">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="5ddc7-141">In the list, find and select the desired record.</span></span> <span data-ttu-id="5ddc7-142">Kanaldan Fiyat grubuna, Fiyat grubundan Ticari anlaşmalara bağlantıyı tamamlar.</span><span class="sxs-lookup"><span data-stu-id="5ddc7-142">This will complete the link from Channel to Price group to Trade agreement.</span></span>  
32. <span data-ttu-id="5ddc7-143">**Madde ilişkisi** alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="5ddc7-143">In the **Item relation** field, type a value.</span></span>
33. <span data-ttu-id="5ddc7-144">**Para birimi miktarı** alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="5ddc7-144">In the **Amount in currency** field, enter a number.</span></span>
34. <span data-ttu-id="5ddc7-145">**Ayrıntılar** hızlı sekmesinde **Sonrakini bul** onay kutusunu işaretleyin veya işaretini kaldırın.</span><span class="sxs-lookup"><span data-stu-id="5ddc7-145">In the **Details** fastTab, check or uncheck the **Find next** checkbox.</span></span> <span data-ttu-id="5ddc7-146">**Sonrakini bul** 'Evet' olarak ayarlandığında, fiyatlandırma altyapısı, daha düşük satış fiyatına sahip ilgili ticari anlaşmaları aramaya devam edecektir.</span><span class="sxs-lookup"><span data-stu-id="5ddc7-146">When **Find next** is set to 'Yes', the pricing engine will continue to search for applicable trade agreements with a lower sale price.</span></span> <span data-ttu-id="5ddc7-147">**Sonrakini Bul** 'Hayır' olarak ayarlandığında, fiyat altyapısı aramayı durdurur ve ticaret anlaşmasını kullanır.</span><span class="sxs-lookup"><span data-stu-id="5ddc7-147">When **Find next** is set to 'No', the price engine stops searching and uses the trade agreement.</span></span>  
35. <span data-ttu-id="5ddc7-148">**Naklet**'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="5ddc7-148">Click **Post**.</span></span>
36. <span data-ttu-id="5ddc7-149">**Tamam**'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="5ddc7-149">Click **OK**.</span></span>
37. <span data-ttu-id="5ddc7-150">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="5ddc7-150">Close the page.</span></span>
38. <span data-ttu-id="5ddc7-151">**Eylem Bölmesi**'nde, Satış'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="5ddc7-151">On the **Action Pane**, click Sell.</span></span>
39. <span data-ttu-id="5ddc7-152">**Satış fiyatı**'na tıklayın.</span><span class="sxs-lookup"><span data-stu-id="5ddc7-152">Click **Sales price**.</span></span>

