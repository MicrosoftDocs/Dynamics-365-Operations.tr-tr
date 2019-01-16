---
title: "Fiyat ayarlamaları ve iskontolar"
description: "Bu makalede, Microsoft Dynamics 365 for Retail'deki fiyat ayarlamaları ve indirimler hakkında bilgiler sağlanmıştır."
author: scott-tucker
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
ms.search.form: RetailParameters, RetailPeriodicDiscount
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 15891
ms.assetid: bab5adf3-ddf0-4c22-a2eb-b4d25b88de99
ms.search.region: global
ms.search.industry: Retail
ms.author: scotttuc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 190d0b59ad2e232b33b3c0d1700cbaf95c45aeca
ms.openlocfilehash: 61ac8e5fbdc4d91bb5bc5372a7fb96633043473a
ms.contentlocale: tr-tr
ms.lasthandoff: 01/04/2019

---

# <a name="price-adjustments-and-discounts"></a><span data-ttu-id="cc04b-103">Fiyat ayarlamaları ve iskontolar</span><span class="sxs-lookup"><span data-stu-id="cc04b-103">Price adjustments and discounts</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="cc04b-104">Bu makalede, Microsoft Dynamics 365 for Retail'deki fiyat ayarlamaları ve indirimler hakkında bilgiler sağlanmıştır.</span><span class="sxs-lookup"><span data-stu-id="cc04b-104">This article provides information about price adjustments and discounts in Microsoft Dynamics 365 for Retail.</span></span>

<span data-ttu-id="cc04b-105">Dynamics 365 for Retail'de ürüne yönelik fiyat ayarlamaları yapabilir ve ayrıca bir çağrı merkezi satış emrinde ya da bir çevrimiçi emirde bir satır maddesine veya satış noktasındaki bir harekete uygulanan iskontolar ayarlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="cc04b-105">In Dynamics 365 for Retail, you can make price adjustments to products, and can also set up discounts that are applied to a line item or a transaction at the point of sale (POS), in a call center sales order, or in an online order.</span></span> <span data-ttu-id="cc04b-106">Hem fiyat ayarlaması hem de iskontolar fiyat gruplarına bağlanabilir.</span><span class="sxs-lookup"><span data-stu-id="cc04b-106">Both price adjustments and discounts can be linked to price groups.</span></span> <span data-ttu-id="cc04b-107">Hem fiyat ayarlaması hem de iskontolar için, tek bir başlangıç tarihi ve bitiş tarihi veya bir yeniden gerçekleşme dönemi, bir iskonto kodu ve birkaç ek öznitelik belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="cc04b-107">For both price adjustments and discounts, you can specify a single start date and end date or a reoccurring period, a discount code, and a few additional attributes.</span></span> <span data-ttu-id="cc04b-108">Fiyat ayarlamaları ve iskontolar ürünlere, varyantlara veya kategorilere uygulanabilir.</span><span class="sxs-lookup"><span data-stu-id="cc04b-108">Price adjustments and discounts can be applied to products, variants, or categories.</span></span> <span data-ttu-id="cc04b-109">Bir ürün için birden fazla iskonto geçerliyse, bir müşteri iskontonun yapılandırmasına bağlı olarak iskontolardan ya birini ya da birleştirilmiş iskontosu alabilir.</span><span class="sxs-lookup"><span data-stu-id="cc04b-109">If more than one discount applies to a product, a customer might receive either one of the discounts or a combined discount, depending on the configuration of the discount.</span></span> <span data-ttu-id="cc04b-110">Dynamics 365 for Retail iskontoyu veya iskonto kombinasyonunu müşteriye en iyi fiyatı verecek şekilde otomatik olarak uygular.</span><span class="sxs-lookup"><span data-stu-id="cc04b-110">Dynamics 365 for Retail automatically applies the discount or combination of discounts that gives the best price to the customer.</span></span> <span data-ttu-id="cc04b-111">Bir fiyat ayarlaması veya bir iskonto ayarladığınızda, fiyat gruplarının iskontonun geçerli olmasını istediğiniz doğru kanallara, kataloglara, ilişkilere veya sadakat programlarına atandığını doğruladığınızdan emin olun.</span><span class="sxs-lookup"><span data-stu-id="cc04b-111">When you set up a price adjustment or a discount, be sure to confirm that price groups are assigned to the correct channels, catalogs, affiliations, or loyalty programs that you want the discount to apply to.</span></span> <span data-ttu-id="cc04b-112">Ayrıca, iskonto kodunu otomatik olarak üretmek istiyorsanız, yeni bir fiyat ayarlaması veya iskonto tanımlamadan önce **Perakende parametreleri** sayfasında numara sırası ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="cc04b-112">Additionally, if you want to automatically generate the discount ID, set up number sequences on the **Retail parameters** page before you define a new price adjustment or discount.</span></span>

> [!NOTE]
> <span data-ttu-id="cc04b-113">Bir fiyat ayarlamasını veya iskontosu silebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="cc04b-113">You can delete a price adjustment or a discount.</span></span> <span data-ttu-id="cc04b-114">Ancak, istatistiksel bilgiler kaybolacaktır.</span><span class="sxs-lookup"><span data-stu-id="cc04b-114">However, statistical information will be lost.</span></span>

## <a name="types-of-discounts"></a><span data-ttu-id="cc04b-115">İskonto türleri</span><span class="sxs-lookup"><span data-stu-id="cc04b-115">Types of discounts</span></span>

<span data-ttu-id="cc04b-116">Perakende iskontolarının dört türü vardır:</span><span class="sxs-lookup"><span data-stu-id="cc04b-116">There are four types of retail discounts:</span></span>

- <span data-ttu-id="cc04b-117">**Basit iskonto** – Tek bir yüzde veya tutar.</span><span class="sxs-lookup"><span data-stu-id="cc04b-117">**Simple discount** – A single percentage or amount.</span></span>
- <span data-ttu-id="cc04b-118">**Miktar iskontosu** – İki veya daha fazla ürün satın alındığında bir iskonto uygulanır.</span><span class="sxs-lookup"><span data-stu-id="cc04b-118">**Quantity discount** – A discount that is applied when two or more products are purchased.</span></span>
- <span data-ttu-id="cc04b-119">**Karıştır ve eşle iskontosu** – Belirli bir ürün kombinasyonu satın alındığında uygulanan iskonto.</span><span class="sxs-lookup"><span data-stu-id="cc04b-119">**Mix and match discount** – A discount that is applied when a specific combination of products is purchased.</span></span>
- <span data-ttu-id="cc04b-120">**Eşik iskontosu** – Hareket toplamı belirli bir tutardan fazlayken uygulanan iskonto.</span><span class="sxs-lookup"><span data-stu-id="cc04b-120">**Threshold discount** – A discount that is applied when the transaction total is more than a specified amount.</span></span>

<span data-ttu-id="cc04b-121">Hem fiyat ayarlaması hem de iskontolar fiyat gruplarına bağlanabilir.</span><span class="sxs-lookup"><span data-stu-id="cc04b-121">Both price adjustments and discounts can be associated with price groups.</span></span> <span data-ttu-id="cc04b-122">Fiyat grupları daha sonra kanallar, kataloglar, ilişkiler ve sadakat programları ile ilişkilendirilebilir.</span><span class="sxs-lookup"><span data-stu-id="cc04b-122">Price groups can then be associated with channels, catalogs, affiliations, and loyalty programs.</span></span>

