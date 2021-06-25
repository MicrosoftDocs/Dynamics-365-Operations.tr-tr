---
title: Fiyat ayarlamaları ve iskontolar
description: Bu makale, Dynamics 365 Commerce içinde fiyat ayarlaması ve iskontolar hakkında bilgi sağlar.
author: scott-tucker
ms.date: 06/11/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RetailParameters, RetailPeriodicDiscount
audience: Application User
ms.reviewer: josaw
ms.custom: 15891
ms.assetid: bab5adf3-ddf0-4c22-a2eb-b4d25b88de99
ms.search.region: global
ms.search.industry: Retail
ms.author: scotttuc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 44c03ae0a04d648e788a72d8f6dcc3671c5736c7
ms.sourcegitcommit: 7c9d6be464db058511df9cb6ba162d21dc0554e8
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/11/2021
ms.locfileid: "6240954"
---
# <a name="price-adjustments-and-discounts"></a><span data-ttu-id="3b4a2-103">Fiyat ayarlamaları ve iskontolar</span><span class="sxs-lookup"><span data-stu-id="3b4a2-103">Price adjustments and discounts</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="3b4a2-104">Bu makale, Dynamics 365 Commerce içinde fiyat ayarlaması ve iskontolar hakkında bilgi sağlar.</span><span class="sxs-lookup"><span data-stu-id="3b4a2-104">This article provides information about price adjustments and discounts in Dynamics 365 Commerce.</span></span>

<span data-ttu-id="3b4a2-105">Commerce içinde, ürünlerde fiyat ayarlamaları yapabilir ve bir satır maddesine veya satış noktası (POS), çağrı merkezi satış siparişi veya çevrimiçi siparişteki bir harekete uygulanacak iskontolar ayarlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="3b4a2-105">In Commerce, you can make price adjustments to products, and can also set up discounts that are applied to a line item or a transaction at the point of sale (POS), in a call center sales order, or in an online order.</span></span> <span data-ttu-id="3b4a2-106">Hem fiyat ayarlaması hem de iskontolar fiyat gruplarına bağlanabilir.</span><span class="sxs-lookup"><span data-stu-id="3b4a2-106">Both price adjustments and discounts can be linked to price groups.</span></span> <span data-ttu-id="3b4a2-107">Hem fiyat ayarlaması hem de iskontolar için, tek bir başlangıç tarihi ve bitiş tarihi veya bir yeniden gerçekleşme dönemi, bir iskonto kodu ve birkaç ek öznitelik belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="3b4a2-107">For both price adjustments and discounts, you can specify a single start date and end date or a reoccurring period, a discount code, and a few additional attributes.</span></span> 

<span data-ttu-id="3b4a2-108">Fiyat ayarlamaları ve iskontolar ürünlere, varyantlara veya kategorilere uygulanabilir.</span><span class="sxs-lookup"><span data-stu-id="3b4a2-108">Price adjustments and discounts can be applied to products, variants, or categories.</span></span> <span data-ttu-id="3b4a2-109">Bir ürün için birden fazla iskonto geçerliyse, bir müşteri iskontonun yapılandırmasına bağlı olarak iskontolardan ya birini ya da birleştirilmiş iskontosu alabilir.</span><span class="sxs-lookup"><span data-stu-id="3b4a2-109">If more than one discount applies to a product, a customer might receive either one of the discounts or a combined discount, depending on the configuration of the discount.</span></span> <span data-ttu-id="3b4a2-110">Commerce, iskontoyu veya iskonto kombinasyonunu müşteriye en iyi fiyatı verecek şekilde otomatik olarak uygular.</span><span class="sxs-lookup"><span data-stu-id="3b4a2-110">Commerce automatically applies the discount or combination of discounts that gives the best price to the customer.</span></span> <span data-ttu-id="3b4a2-111">Bir fiyat ayarlaması veya bir iskonto ayarladığınızda, fiyat gruplarının iskontonun geçerli olmasını istediğiniz doğru kanallara, kataloglara, ilişkilere veya sadakat programlarına atandığını doğruladığınızdan emin olun.</span><span class="sxs-lookup"><span data-stu-id="3b4a2-111">When you set up a price adjustment or a discount, be sure to confirm that price groups are assigned to the correct channels, catalogs, affiliations, or loyalty programs that you want the discount to apply to.</span></span> <span data-ttu-id="3b4a2-112">Ayrıca, iskonto kodunu otomatik olarak üretmek istiyorsanız, yeni bir fiyat ayarlaması veya iskonto tanımlamadan önce **Ticaret parametreleri** sayfasında numara sırası ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="3b4a2-112">Additionally, if you want to automatically generate the discount ID, set up number sequences on the **Commerce parameters** page before you define a new price adjustment or discount.</span></span>

> [!NOTE]
> <span data-ttu-id="3b4a2-113">Bir fiyat ayarlamasını veya iskontosu silebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="3b4a2-113">You can delete a price adjustment or a discount.</span></span> <span data-ttu-id="3b4a2-114">Ancak, istatistiksel bilgiler kaybolacaktır.</span><span class="sxs-lookup"><span data-stu-id="3b4a2-114">However, statistical information will be lost.</span></span>

## <a name="types-of-discounts"></a><span data-ttu-id="3b4a2-115">İskonto türleri</span><span class="sxs-lookup"><span data-stu-id="3b4a2-115">Types of discounts</span></span>

<span data-ttu-id="3b4a2-116">İskontolarının birçok türü vardır:</span><span class="sxs-lookup"><span data-stu-id="3b4a2-116">There are many types of discounts:</span></span>

- <span data-ttu-id="3b4a2-117">**Basit iskonto** – Tek bir yüzde veya tutar.</span><span class="sxs-lookup"><span data-stu-id="3b4a2-117">**Simple discount** – A single percentage or amount.</span></span>
- <span data-ttu-id="3b4a2-118">**Miktar iskontosu** – İki veya daha fazla ürün satın alındığında bir iskonto uygulanır.</span><span class="sxs-lookup"><span data-stu-id="3b4a2-118">**Quantity discount** – A discount that is applied when two or more products are purchased.</span></span>
- <span data-ttu-id="3b4a2-119">**Karıştır ve eşle iskontosu** – Belirli bir ürün kombinasyonu satın alındığında uygulanan iskonto.</span><span class="sxs-lookup"><span data-stu-id="3b4a2-119">**Mix and match discount** – A discount that is applied when a specific combination of products is purchased.</span></span>
- <span data-ttu-id="3b4a2-120">**Eşik iskontosu** – Hareket toplamı belirli bir tutardan fazlayken uygulanan iskonto.</span><span class="sxs-lookup"><span data-stu-id="3b4a2-120">**Threshold discount** – A discount that is applied when the transaction total is more than a specified amount.</span></span>
- <span data-ttu-id="3b4a2-121">**Ödeme tabanlı iskonto** – Ödeme için hareket toplamı belirtilen bir tutardan fazla olduğunda ve belirli bir ödeme türü (örneğin, nakit, alacak veya borç kartı) kullanıldığında uygulanan iskonto.</span><span class="sxs-lookup"><span data-stu-id="3b4a2-121">**Tender-based discount** – A discount that is applied when the transaction total is more than a specified amount and a specific payment type (for example, cash, credit, or debit card) is used for payment.</span></span>
- <span data-ttu-id="3b4a2-122">**Sevkiyat iskontosu** – siparişte, hareket toplamı belirtilen tutardan fazla olduğunda uygulanan iskonto (örneğin, iki günlük sevkiyat veya bir gecede nakliye gibi) sipariş için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="3b4a2-122">**Shipping discount** – A discount that is applied when the transaction total is more than a specified amount and a specific mode of delivery (for example, two day shipping or overnight shipping) is used on the order.</span></span>

<span data-ttu-id="3b4a2-123">Hem fiyat ayarlaması hem de iskontolar fiyat gruplarına bağlanabilir.</span><span class="sxs-lookup"><span data-stu-id="3b4a2-123">Both price adjustments and discounts can be associated with price groups.</span></span> <span data-ttu-id="3b4a2-124">Fiyat grupları daha sonra kanallar, kataloglar, ilişkiler ve sadakat programları ile ilişkilendirilebilir.</span><span class="sxs-lookup"><span data-stu-id="3b4a2-124">Price groups can then be associated with channels, catalogs, affiliations, and loyalty programs.</span></span>

> [!NOTE]
> <span data-ttu-id="3b4a2-125">Karıştır ve eşle iskontosu ve eşik iskontosu, sırasıyla "Sayılamayan ürünleri say" ve "Sayılamayan ürünleri eşiğe doğru say" adlı özelliklere sahiptir.</span><span class="sxs-lookup"><span data-stu-id="3b4a2-125">The mix and match discount and the threshold discount have properties named "Count non-discountable products" and "Count non-discountable products towards threshold", respectively.</span></span> <span data-ttu-id="3b4a2-126">Bu özellikler etkinleştirilirse, herhangi bir iskonto için uygun olmayan bir madde, bir hareketi iskontoya uygun olarak saymaya yardımcı olabilir ancak yeterli madde iskontosu alamaz.</span><span class="sxs-lookup"><span data-stu-id="3b4a2-126">If these properties are enabled, an item that is not eligible for any discount can still help qualify a transaction for the discount, but the ineligible item will not get the discount.</span></span> 
> 
> <span data-ttu-id="3b4a2-127">Örneğin, her iki maddede de bir müşterinin %10 iskonto alması gereken iki satırı (A ve B) olan bir karıştır ve eşle iskontosu oluşturursanız, ancak madde A'nın "Tüm iskontoları engelle" yapılandırması varsa bu durum genellikle A maddesinin iskontoya dahil edilmesini engeller.</span><span class="sxs-lookup"><span data-stu-id="3b4a2-127">For example, if you create a mix and match discount with two lines, A and B, where a customer should get 10% off on both items, but item A has the configuration "Prevent all discounts" checked, then this would typically stop item A from being included in the discount.</span></span> <span data-ttu-id="3b4a2-128">Ancak, "Sayılamayan ürünleri say" özelliği etkinse karıştır ve eşle iskontosuna uygun olacak şekilde madde A kullanılabilir ancak %10 iskonto yalnızca B maddesine uygulanır. Benzer bir mantık eşik iskontosuna da uygulanır.</span><span class="sxs-lookup"><span data-stu-id="3b4a2-128">However, if the "Count non-discountable products" property is enabled, then item A can be used to qualify for the mix and match discount, but the 10% discount will only be applied to item B. Similar logic applies to the threshold discount.</span></span> 
>
> <span data-ttu-id="3b4a2-129">Ancak, karıştır ve eşle iskontolarında "Sayılamayan ürünleri say" özelliğiyle karşılaştırıldığında "Sayılamayan ürünleri eşiğe doğru say" özelliği ek bir özelliğe sahiptir.</span><span class="sxs-lookup"><span data-stu-id="3b4a2-129">However, the property "Count non-discountable products towards threshold" has an additional capability when compared to the "Count non-discountable products" property of the mix and match discounts.</span></span> <span data-ttu-id="3b4a2-130">Eşik iskontosu etkinleştirilmişse ve maddenin başka bir iskonto almasını önleyen mevcut iskonto içeren bir madde varsa, bu madde için ödenen fiyat eşiğe yaklaşma hakkı kazanır ancak bu maddeye ek iskonto uygulanmaz.</span><span class="sxs-lookup"><span data-stu-id="3b4a2-130">If the threshold discount is enabled, and if there is an item that has an existing discount which would prevent the item from any other discounts, then  the price paid for this item would qualify towards meeting the threshold, but this item will not get the additional discount.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
