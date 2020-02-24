---
title: Mağazanın ürün çeşidinden olmayan ürünleri satma ve iade etme
description: Dynamics 365 Commerce ile, çeşitler dışında ürünler satabilir ve iade alabilirsiniz.
author: pdp1207
manager: AnnBe
ms.date: 05/24/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailAssortmentDetails
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.search.region: Global
ms.search.industry: retail
ms.author: prabhup
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: 86c6ecf9ef67ca3ac4ed3c44d930acaa965112b6
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/01/2020
ms.locfileid: "3024351"
---
# <a name="sell-and-return-products-that-arent-part-of-a-stores-assortment"></a><span data-ttu-id="13baf-103">Mağazanın ürün çeşidinden olmayan ürünleri satma ve iade etme</span><span class="sxs-lookup"><span data-stu-id="13baf-103">Sell and return products that aren't part of a store's assortment</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="13baf-104">Tüm Perakendeciler için genel bir senaryo, mağazalarında belirli ürünleri bulundurmasalar bile (diğer bir deyişle, ürünler mağazadaki çeşitler arasında olmasa bile) kendi müşterilerine ürünleri satmak veya müşterilerden gelen iadeleri kabul etmektir.</span><span class="sxs-lookup"><span data-stu-id="13baf-104">A common scenario for any retailer is to sell products to their customers or accept returns from their customers even if they don't carry the specific products in their store (in other words, the products are not assorted to the store).</span></span>

<span data-ttu-id="13baf-105">Burada bazı tipik senaryolar vardır:</span><span class="sxs-lookup"><span data-stu-id="13baf-105">Here are some typical scenarios:</span></span>

+ <span data-ttu-id="13baf-106">Bir perakendeci tüm ürünlerini belirli bir mağazada bulundurmaz.</span><span class="sxs-lookup"><span data-stu-id="13baf-106">A retailer doesn't carry all its products in a specific store.</span></span> <span data-ttu-id="13baf-107">Kalan ürünler ambarda depolanır.</span><span class="sxs-lookup"><span data-stu-id="13baf-107">The remaining products are stored in the warehouse.</span></span> <span data-ttu-id="13baf-108">Mağaza çalışanı depodaki ürünleri arayarak veya bunlara göz atarak müşteriye yardımcı olabilir, ürünleri sepete ekleyebilir ve depodan adrese teslim gibi bir teslimat yöntemi seçerek veya müşterinin ürünü geçerli mağazadan veya başka bir mağazadan çekmesini sağlayarak işlemi tamamlayabilir.</span><span class="sxs-lookup"><span data-stu-id="13baf-108">The store associate can assist the customer by searching or browsing for the products in the warehouse, add them to the cart, and complete the checkout by selecting a delivery method, such as shipping to an address from the warehouse or letting the customer pick up the product from the current store or from another store.</span></span>
+ <span data-ttu-id="13baf-109">Perakendeci belirli ürünleri mağaza bulundurmaz veya ürünler müşterinin ziyaret ettiği mağazanın stoğunda bulunmayabilir ancak ürünler diğer mağazalarda olabilir.</span><span class="sxs-lookup"><span data-stu-id="13baf-109">A retailer doesn't carry specific products in the store or doesn't have them in stock at the store the customer visited, but the products are available in other stores.</span></span> <span data-ttu-id="13baf-110">Mağaza çalışanı ürünleri diğer bir mağazada arayarak veya göz atarak müşterinin bunları sepete eklemesine ve bir teslimat yöntemi seçerek satınalma işlemini tamamlamaya yardımcı olabilir.</span><span class="sxs-lookup"><span data-stu-id="13baf-110">The store associate can assist the customer by searching or browsing the products in the other store, add them to the cart, and complete the checkout by selecting a delivery method.</span></span>
+ <span data-ttu-id="13baf-111">Perakendecinin belirli bir şehir veya bölgede birçok mağazası vardır ve müşteriyi iade edeceği ürünü satın aldığı mağazaya iade etmek konusunda zorlamak istemez.</span><span class="sxs-lookup"><span data-stu-id="13baf-111">A retailer has many stores in and around a specific city or zip code and doesn't want to force the customers to return products to the same store they were purchased in.</span></span> <span data-ttu-id="13baf-112">Bunun yerine, müşteri ürünleri herhangi bir mağazaya iade edebilir.</span><span class="sxs-lookup"><span data-stu-id="13baf-112">Instead, customers can return products to any store.</span></span>

<span data-ttu-id="13baf-113">Bu ortak senaryolar Commerce kullanan perakendeciler için kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="13baf-113">Those common scenarios are available for retailers using Commerce.</span></span> <span data-ttu-id="13baf-114">Commerce ile şunları yapabilirsiniz:</span><span class="sxs-lookup"><span data-stu-id="13baf-114">With Commerce, you can:</span></span>

+ <span data-ttu-id="13baf-115">Diğer mağazalarda ürünleri aramak veya diğer mağazalardaki ürünlere göz atmak.</span><span class="sxs-lookup"><span data-stu-id="13baf-115">Search or browse products at other stores.</span></span>
+ <span data-ttu-id="13baf-116">Tüm serbest bırakılan ürünleri aramak veya göz atmak.</span><span class="sxs-lookup"><span data-stu-id="13baf-116">Search or browse all released products.</span></span>
+ <span data-ttu-id="13baf-117">peşin alış veriş hareketleri veya müşteri siparişleri oluşturmak.</span><span class="sxs-lookup"><span data-stu-id="13baf-117">Create cash-and-carry transactions or customer orders.</span></span>
+ <span data-ttu-id="13baf-118">Müşteri siparişleri için teslim seçeneklerini belirlemek.</span><span class="sxs-lookup"><span data-stu-id="13baf-118">Select delivery options for customer orders.</span></span>
+ <span data-ttu-id="13baf-119">Ürünleri geçerli mağazadan veya başka mağazadan seçmek.</span><span class="sxs-lookup"><span data-stu-id="13baf-119">Pick up products at the current store or another store.</span></span>
+ <span data-ttu-id="13baf-120">Geçerli mağazadaki veya başka mağazadaki siparişi iptal etmek.</span><span class="sxs-lookup"><span data-stu-id="13baf-120">Cancel an order at the current store or another store.</span></span>
+ <span data-ttu-id="13baf-121">Bir siparişi makbuzla veya makbuz olmadan geçerli mağazaya veya başka bir mağazaya iade etmek.</span><span class="sxs-lookup"><span data-stu-id="13baf-121">Return an order with or without the receipt at the current store or another store.</span></span>
