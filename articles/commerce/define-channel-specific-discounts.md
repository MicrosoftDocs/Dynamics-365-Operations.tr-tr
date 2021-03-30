---
title: Kanala özel indirimler tanımla
description: Perakendeciler sık sık farklı kanallara farklı iskontolar uygular. Bu konuda, belirli bir kanala ait bir indirim oluşturmak için bilmeniz gereken kavramlar incelenmektedir.
author: scott-tucker
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailAffiliationPriceGroup, RetailCatalogPriceGroup, RetailChannelPriceGroup, RetailDiscountPriceGroup, RetailDiscountPricingWorkspace, RetailPeriodicDiscount, RetailStoreItemPriceList, RetailStoreTable
audience: Application User
ms.reviewer: josaw
ms.custom: 16401
ms.assetid: d807fd51-86aa-47a0-8e00-6c5ddd21ff6b
ms.search.region: global
ms.search.industry: Retail
ms.author: scotttuc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 36b2d8f96f8545f9fa792e42c639b03e1e14e8ee
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5213758"
---
# <a name="define-channel-specific-discounts"></a><span data-ttu-id="b15f2-104">Kanala özel iskontolar tanımlama</span><span class="sxs-lookup"><span data-stu-id="b15f2-104">Define channel-specific discounts</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="b15f2-105">Bu konuda, belirli bir kanala ait bir indirim oluşturmak için bilmeniz gereken kavramlar incelenmektedir.</span><span class="sxs-lookup"><span data-stu-id="b15f2-105">This topic reviews the concepts you need to know to create a discount for a specific channel.</span></span>

## <a name="channel-specific-discounts"></a><span data-ttu-id="b15f2-106">Kanala özel indirimler</span><span class="sxs-lookup"><span data-stu-id="b15f2-106">Channel-specific discounts</span></span>

<span data-ttu-id="b15f2-107">Perakendeciler sık sık farklı kanallara farklı iskontolar sunar.</span><span class="sxs-lookup"><span data-stu-id="b15f2-107">Retailers often offer different discounts in different channels.</span></span> <span data-ttu-id="b15f2-108">Bunun nedeni, yerel piyasa koşullarına yanıt vermek veya rakip perakendecilerle başa çıkmaya çalışmak olabilir.</span><span class="sxs-lookup"><span data-stu-id="b15f2-108">This may be done to address local market conditions or to deal with competing retailers.</span></span>

<span data-ttu-id="b15f2-109">Commerce, fiyat gruplarını kanal özel indirimleri tanımlamak için kullanır.</span><span class="sxs-lookup"><span data-stu-id="b15f2-109">Commerce uses price groups to define channel-specific discounts.</span></span> <span data-ttu-id="b15f2-110">Aşağıdaki varlıklardan biri veya daha fazlası için fiyat grupları atanabilir: kanallar, kataloglar, ilişkiler ve bağlılık programları.</span><span class="sxs-lookup"><span data-stu-id="b15f2-110">Price groups can be assigned to one or more of the following entities: channels, catalogs, affiliations, and loyalty programs.</span></span> <span data-ttu-id="b15f2-111">Bu makalede kanallar anlatılmaktadır, ancak aynı kavramlar katalog indirimleri, ilişkiler indirimleri ve bağlılık için indirimlerde de uygulanır.</span><span class="sxs-lookup"><span data-stu-id="b15f2-111">This article discusses channels, but the same concepts apply to catalog discounts, affiliations discounts, and loyalty discounts.</span></span>

## <a name="price-groups"></a><span data-ttu-id="b15f2-112">Fiyat grupları</span><span class="sxs-lookup"><span data-stu-id="b15f2-112">Price groups</span></span>

<span data-ttu-id="b15f2-113">[![Fiyat grupları](./media/price-groups-1024x608.png)](./media/price-groups.png)</span><span class="sxs-lookup"><span data-stu-id="b15f2-113">[![Price groups](./media/price-groups-1024x608.png)](./media/price-groups.png)</span></span>

<span data-ttu-id="b15f2-114">Yukarıdaki diyagram, bir hareket üzerinde bulunabilen varlıklar (kanal, katalog, ilişki, müşteri, bağlılık programı kartı) arasındaki ilişkiyi ve yapılandırılabilen çeşitli iskonto türlerini gösterir.</span><span class="sxs-lookup"><span data-stu-id="b15f2-114">The diagram above illustrates the relationship between entities that may be on a transaction (channel, catalog, affiliation, customer, loyalty card) and the various discount types that can be configured.</span></span> <span data-ttu-id="b15f2-115">Tüm hareketler bir kanal içerisinde gerçekleşir, böylece kanalın hareket üzerinde bulunması garanti edilir.</span><span class="sxs-lookup"><span data-stu-id="b15f2-115">All transactions occur in a channel, so the channel is guaranteed to be present on a transaction.</span></span> <span data-ttu-id="b15f2-116">Kalan varlıklar isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="b15f2-116">The remaining entities are optional.</span></span> <span data-ttu-id="b15f2-117">Her ana veri sayfalarında ilgili fiyat grupları sayfasına gerektiği gibi fiyat grupları girebileceğiniz veya görüntüleyebileceğiniz bir bağlantı vardır.</span><span class="sxs-lookup"><span data-stu-id="b15f2-117">On each master data pages there is a link to a related price groups page where you can view and add price groups as needed.</span></span> <span data-ttu-id="b15f2-118">Bir fiyat grubu, dört farklı tipte varlığı iskontolara, fiyat ayarlamalarına ve ticari anlaşmalara ilişkilendirmek için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="b15f2-118">A price group is used to relate four different types of entities to discounts, price adjustments, and trade agreements.</span></span> <span data-ttu-id="b15f2-119">Fiyat gruplarınızı organize etmek için onları nasıl adlandıracağınıza dair bir strateji planlamanızı öneririz.</span><span class="sxs-lookup"><span data-stu-id="b15f2-119">We recommend that you plan a strategy for how you will name your price groups to keep them organized.</span></span> <span data-ttu-id="b15f2-120">Bir seçenek, farklı türler arasında ayrım yapabilmek için bir harf veya sayı ön veya son eki kullanmak olabilir.</span><span class="sxs-lookup"><span data-stu-id="b15f2-120">One option would be to use a letter or number prefix or suffix to distinguish between the different types.</span></span> <span data-ttu-id="b15f2-121">Örneğin, kanal fiyat grupları için 1-xxxxx ve katalog fiyat grupları için 2-xxxxx.</span><span class="sxs-lookup"><span data-stu-id="b15f2-121">For example, 1-xxxxx for channel price groups and 2-xxxxx for catalog price groups.</span></span> <span data-ttu-id="b15f2-122">Her birine iskonto ilişkilendirilmiş olabilecek her bir Commerce varlığına odaklanan dört farklı sorgulama sayfası mevcuttur.</span><span class="sxs-lookup"><span data-stu-id="b15f2-122">There are four inquiry pages that focus on each of the commerce entities that can have discounts associated to them.</span></span>

- <span data-ttu-id="b15f2-123">**Commerce kanalı fiyat grupları** – Bu sayfa her fiyat grubu için birbirine bağlı kanalların ve indirimlerin listesini gösterir.</span><span class="sxs-lookup"><span data-stu-id="b15f2-123">**Channel channel price groups** – This page shows a list of channels and discounts linked together for each price group.</span></span>
- <span data-ttu-id="b15f2-124">**Katalog fiyat grupları** – Bu sayfa her fiyat grubu için birbirine bağlı katalogların ve indirimlerin listesini gösterir.</span><span class="sxs-lookup"><span data-stu-id="b15f2-124">**Catalog price groups** – This page shows a list of catalogs and discounts linked together for each price group.</span></span>
- <span data-ttu-id="b15f2-125">**Bağlılık fiyat grupları** – Bu sayfa her bağlılık programı için birbirine bağlı kanalların ve indirimlerin listesini gösterir.</span><span class="sxs-lookup"><span data-stu-id="b15f2-125">**Loyalty price groups** – This page shows a list of loyalty programs and discounts linked together for each price group.</span></span>
- <span data-ttu-id="b15f2-126">**İlişki fiyat grupları** – Bu sayfa her bir ilişki için birbirine bağlı kanalların ve indirimlerin listesini gösterir.</span><span class="sxs-lookup"><span data-stu-id="b15f2-126">**Affiliation price groups** – This page shows a list of affiliations and discounts linked together for each price group.</span></span>

## <a name="example-channel-discount-set-up"></a><span data-ttu-id="b15f2-127">Örnek kanal indirim ayarlama</span><span class="sxs-lookup"><span data-stu-id="b15f2-127">Example channel discount set up</span></span>

<span data-ttu-id="b15f2-128">Aşağıdaki örnek bir kanal iskonto ayarının kurulmasıyla ilgili görevleri gösterir.</span><span class="sxs-lookup"><span data-stu-id="b15f2-128">The following example illustrates the tasks involved in setting up a channel discount.</span></span>

1. <span data-ttu-id="b15f2-129">Bu örnekte **Houston** adlı bir kanal mevcuttur ve **Okula dönüş** adlı yeni bir indirim oluşturacaksınız.</span><span class="sxs-lookup"><span data-stu-id="b15f2-129">For this example, you have a channel called **Houston**, and you're going to create a new discount called **Back-to-School**.</span></span>
2. <span data-ttu-id="b15f2-130">Fiyat ve iskonto stratejisi kanal indirimleri ihtimalini içerdiği için, bir kanal oluşturduğunuzda her zaman kanala özel bir fiyat grubu oluşturursunuz.</span><span class="sxs-lookup"><span data-stu-id="b15f2-130">Because the pricing and discount strategy includes the possibility of channel discounts, you always create a channel-specific price group when you create a channel.</span></span>
3. <span data-ttu-id="b15f2-131">Fiyat grubu **Houston-PG** mevcuttur ve bu, **Houston** kanalına atanmıştır.</span><span class="sxs-lookup"><span data-stu-id="b15f2-131">You have the price group **Houston-PG** and it is assigned to the **Houston** channel.</span></span>
4. <span data-ttu-id="b15f2-132">**Okula dönüş** yeni iskontosunu oluşturduktan sonra, **İndirim** sayfasının tepesindeki **Fiyat grupları** tıklamanız lazım.</span><span class="sxs-lookup"><span data-stu-id="b15f2-132">After you create the new **Back-to-School** discount, you need to click **Price groups** on the top of the **Discount** page.</span></span> <span data-ttu-id="b15f2-133">**İndirim fiyat grupları** sayfası açılacaktır.</span><span class="sxs-lookup"><span data-stu-id="b15f2-133">The **Discount price groups** page will open.</span></span> <span data-ttu-id="b15f2-134">Bundan sonra **Yeni**'ye tıklayın ve **Houston-PG** fiyat grubunu seçin.</span><span class="sxs-lookup"><span data-stu-id="b15f2-134">Next, click **New** and select the **Houston-PG** price group.</span></span>
5. <span data-ttu-id="b15f2-135">Şimdi iskontoyu etkinleştirebilir ve kanala itebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="b15f2-135">Now you can enable the discount and push it to the channel.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="b15f2-136">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="b15f2-136">Additional resources</span></span>

[<span data-ttu-id="b15f2-137">Fiyat ayarlamaları ve iskontolar</span><span class="sxs-lookup"><span data-stu-id="b15f2-137">Price adjustments and discounts</span></span>](price-adjustments-discounts.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]