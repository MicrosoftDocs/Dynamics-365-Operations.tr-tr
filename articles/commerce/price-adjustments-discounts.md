---
title: Fiyat ayarlamaları ve iskontolar
description: Bu makale, Dynamics 365 Commerce içinde fiyat ayarlaması ve iskontolar hakkında bilgi sağlar.
author: scott-tucker
ms.date: 11/16/2020
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
ms.openlocfilehash: 2d3e8025c5ab28296713634094694156f9addf62
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/31/2021
ms.locfileid: "5802803"
---
# <a name="price-adjustments-and-discounts"></a><span data-ttu-id="ce7ed-103">Fiyat ayarlamaları ve iskontolar</span><span class="sxs-lookup"><span data-stu-id="ce7ed-103">Price adjustments and discounts</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="ce7ed-104">Bu makale, Dynamics 365 Commerce içinde fiyat ayarlaması ve iskontolar hakkında bilgi sağlar.</span><span class="sxs-lookup"><span data-stu-id="ce7ed-104">This article provides information about price adjustments and discounts in Dynamics 365 Commerce.</span></span>

<span data-ttu-id="ce7ed-105">Commerce içinde, ürünlerde fiyat ayarlamaları yapabilir ve bir satır maddesine veya satış noktası (POS), çağrı merkezi satış siparişi veya çevrimiçi siparişteki bir harekete uygulanacak iskontolar ayarlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="ce7ed-105">In Commerce, you can make price adjustments to products, and can also set up discounts that are applied to a line item or a transaction at the point of sale (POS), in a call center sales order, or in an online order.</span></span> <span data-ttu-id="ce7ed-106">Hem fiyat ayarlaması hem de iskontolar fiyat gruplarına bağlanabilir.</span><span class="sxs-lookup"><span data-stu-id="ce7ed-106">Both price adjustments and discounts can be linked to price groups.</span></span> <span data-ttu-id="ce7ed-107">Hem fiyat ayarlaması hem de iskontolar için, tek bir başlangıç tarihi ve bitiş tarihi veya bir yeniden gerçekleşme dönemi, bir iskonto kodu ve birkaç ek öznitelik belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="ce7ed-107">For both price adjustments and discounts, you can specify a single start date and end date or a reoccurring period, a discount code, and a few additional attributes.</span></span> 

<span data-ttu-id="ce7ed-108">Fiyat ayarlamaları ve iskontolar ürünlere, varyantlara veya kategorilere uygulanabilir.</span><span class="sxs-lookup"><span data-stu-id="ce7ed-108">Price adjustments and discounts can be applied to products, variants, or categories.</span></span> <span data-ttu-id="ce7ed-109">Bir ürün için birden fazla iskonto geçerliyse, bir müşteri iskontonun yapılandırmasına bağlı olarak iskontolardan ya birini ya da birleştirilmiş iskontosu alabilir.</span><span class="sxs-lookup"><span data-stu-id="ce7ed-109">If more than one discount applies to a product, a customer might receive either one of the discounts or a combined discount, depending on the configuration of the discount.</span></span> <span data-ttu-id="ce7ed-110">Commerce, iskontoyu veya iskonto kombinasyonunu müşteriye en iyi fiyatı verecek şekilde otomatik olarak uygular.</span><span class="sxs-lookup"><span data-stu-id="ce7ed-110">Commerce automatically applies the discount or combination of discounts that gives the best price to the customer.</span></span> <span data-ttu-id="ce7ed-111">Bir fiyat ayarlaması veya bir iskonto ayarladığınızda, fiyat gruplarının iskontonun geçerli olmasını istediğiniz doğru kanallara, kataloglara, ilişkilere veya sadakat programlarına atandığını doğruladığınızdan emin olun.</span><span class="sxs-lookup"><span data-stu-id="ce7ed-111">When you set up a price adjustment or a discount, be sure to confirm that price groups are assigned to the correct channels, catalogs, affiliations, or loyalty programs that you want the discount to apply to.</span></span> <span data-ttu-id="ce7ed-112">Ayrıca, iskonto kodunu otomatik olarak üretmek istiyorsanız, yeni bir fiyat ayarlaması veya iskonto tanımlamadan önce **Ticaret parametreleri** sayfasında numara sırası ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="ce7ed-112">Additionally, if you want to automatically generate the discount ID, set up number sequences on the **Commerce parameters** page before you define a new price adjustment or discount.</span></span>

> [!NOTE]
> <span data-ttu-id="ce7ed-113">Bir fiyat ayarlamasını veya iskontosu silebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="ce7ed-113">You can delete a price adjustment or a discount.</span></span> <span data-ttu-id="ce7ed-114">Ancak, istatistiksel bilgiler kaybolacaktır.</span><span class="sxs-lookup"><span data-stu-id="ce7ed-114">However, statistical information will be lost.</span></span>

## <a name="types-of-discounts"></a><span data-ttu-id="ce7ed-115">İskonto türleri</span><span class="sxs-lookup"><span data-stu-id="ce7ed-115">Types of discounts</span></span>

<span data-ttu-id="ce7ed-116">İskontolarının birçok türü vardır:</span><span class="sxs-lookup"><span data-stu-id="ce7ed-116">There are many types of discounts:</span></span>

- <span data-ttu-id="ce7ed-117">**Basit iskonto** – Tek bir yüzde veya tutar.</span><span class="sxs-lookup"><span data-stu-id="ce7ed-117">**Simple discount** – A single percentage or amount.</span></span>
- <span data-ttu-id="ce7ed-118">**Miktar iskontosu** – İki veya daha fazla ürün satın alındığında bir iskonto uygulanır.</span><span class="sxs-lookup"><span data-stu-id="ce7ed-118">**Quantity discount** – A discount that is applied when two or more products are purchased.</span></span>
- <span data-ttu-id="ce7ed-119">**Karıştır ve eşle iskontosu** – Belirli bir ürün kombinasyonu satın alındığında uygulanan iskonto.</span><span class="sxs-lookup"><span data-stu-id="ce7ed-119">**Mix and match discount** – A discount that is applied when a specific combination of products is purchased.</span></span>
- <span data-ttu-id="ce7ed-120">**Eşik iskontosu** – Hareket toplamı belirli bir tutardan fazlayken uygulanan iskonto.</span><span class="sxs-lookup"><span data-stu-id="ce7ed-120">**Threshold discount** – A discount that is applied when the transaction total is more than a specified amount.</span></span>
- <span data-ttu-id="ce7ed-121">**Ödeme tabanlı iskonto** – Ödeme için hareket toplamı belirtilen bir tutardan fazla olduğunda ve belirli bir ödeme türü (örneğin, nakit, alacak veya borç kartı) kullanıldığında uygulanan iskonto.</span><span class="sxs-lookup"><span data-stu-id="ce7ed-121">**Tender-based discount** – A discount that is applied when the transaction total is more than a specified amount and a specific payment type (for example, cash, credit, or debit card) is used for payment.</span></span>
- <span data-ttu-id="ce7ed-122">**Sevkiyat iskontosu** – siparişte, hareket toplamı belirtilen tutardan fazla olduğunda uygulanan iskonto (örneğin, iki günlük sevkiyat veya bir gecede nakliye gibi) sipariş için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="ce7ed-122">**Shipping discount** – A discount that is applied when the transaction total is more than a specified amount and a specific mode of delivery (for example, two day shipping or overnight shipping) is used on the order.</span></span>

<span data-ttu-id="ce7ed-123">Hem fiyat ayarlaması hem de iskontolar fiyat gruplarına bağlanabilir.</span><span class="sxs-lookup"><span data-stu-id="ce7ed-123">Both price adjustments and discounts can be associated with price groups.</span></span> <span data-ttu-id="ce7ed-124">Fiyat grupları daha sonra kanallar, kataloglar, ilişkiler ve sadakat programları ile ilişkilendirilebilir.</span><span class="sxs-lookup"><span data-stu-id="ce7ed-124">Price groups can then be associated with channels, catalogs, affiliations, and loyalty programs.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]