---
title: "Ürünleri bir çeşit dışında satma ve iade etme"
description: "Dynamics 365 for Retail ile, ürünleri çeşitler dışında satabilir ve iade edebilirsiniz."
author: pdp1207
manager: AnnBe
ms.date: 05/24/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
ms.search.form: RetailAssortmentDetails
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 
ms.search.region: Global
ms.search.industry: retail
ms.author: prabhup
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 8d2188ddac937ab373315759b89ecf85c0b7e007
ms.contentlocale: tr-tr
ms.lasthandoff: 04/13/2018

---

# <a name="sell-and-return-products-outside-of-an-assortment"></a><span data-ttu-id="96b21-103">Ürünleri bir çeşit dışında satma ve iade etme</span><span class="sxs-lookup"><span data-stu-id="96b21-103">Sell and return products outside of an assortment</span></span>

[!INCLUDE [banner](includes/banner.md)]

<span data-ttu-id="96b21-104">Tüm Perakendeciler için genel bir senaryo, mağazalarında belirli ürünleri bulundurmasalar bile (diğer bir deyişle, ürünler mağazadaki çeşitler arasında olmasa bile) kendi müşterilerine ürünleri satmak veya müşterilerden gelen iadeleri kabul etmektir.</span><span class="sxs-lookup"><span data-stu-id="96b21-104">A common scenario for any retailer is to sell products to their customers or accept returns from their customers even if they don’t carry the specific products in their store (in other words, the products are not assorted to the store).</span></span>
<span data-ttu-id="96b21-105">Burada bazı tipik senaryolar vardır:</span><span class="sxs-lookup"><span data-stu-id="96b21-105">Here are some typical scenarios:</span></span>

+ <span data-ttu-id="96b21-106">Bir perakendeci tüm ürünlerini belirli bir mağazada bulundurmaz.</span><span class="sxs-lookup"><span data-stu-id="96b21-106">A retailer doesn’t carry all its products in a specific store.</span></span> <span data-ttu-id="96b21-107">Kalan ürünler ambarda depolanır.</span><span class="sxs-lookup"><span data-stu-id="96b21-107">The remaining products are stored in the warehouse.</span></span> <span data-ttu-id="96b21-108">Mağaza çalışanı depodaki ürünleri arayarak veya bunlara göz atarak müşteriye yardımcı olabilir, ürünleri sepete ekleyebilir ve depodan adrese teslim gibi bir teslimat yöntemi seçerek veya müşterinin ürünü geçerli mağazadan veya başka bir mağazadan çekmesini sağlayarak işlemi tamamlayabilir.</span><span class="sxs-lookup"><span data-stu-id="96b21-108">The store associate can assist the customer by searching or browsing for the products in the warehouse, add them to the cart, and complete the checkout by selecting a delivery method, such as shipping to an address from the warehouse or letting the customer pick up the product from the current store or from another store.</span></span>
+ <span data-ttu-id="96b21-109">Perakendeci belirli ürünleri mağaza bulundurmaz veya ürünler müşterinin ziyaret ettiği mağazanın stoğunda bulunmayabilir ancak ürünler diğer mağazalarda olabilir.</span><span class="sxs-lookup"><span data-stu-id="96b21-109">A retailer doesn’t carry specific products in the store or doesn’t have them in stock at the store the customer visited, but the products are available in other stores.</span></span> <span data-ttu-id="96b21-110">Mağaza çalışanı ürünleri diğer bir mağazada arayarak veya göz atarak müşterinin bunları sepete eklemesine ve bir teslimat yöntemi seçerek satınalma işlemini tamamlamaya yardımcı olabilir.</span><span class="sxs-lookup"><span data-stu-id="96b21-110">The store associate can assist the customer by searching or browsing the products in the other store, add them to the cart, and complete the checkout by selecting a delivery method.</span></span>
+ <span data-ttu-id="96b21-111">Perakendecinin belirli bir şehir veya bölgede birçok mağazası vardır ve müşteriyi iade edeceği ürünü satın aldığı mağazaya iade etmek konusunda zorlamak istemez.</span><span class="sxs-lookup"><span data-stu-id="96b21-111">A retailer has many stores in and around a specific city or zip code and doesn’t want to force the customers to return products to the same store they were purchased in.</span></span> <span data-ttu-id="96b21-112">Bunun yerine, müşteri ürünleri herhangi bir mağazaya iade edebilir.</span><span class="sxs-lookup"><span data-stu-id="96b21-112">Instead, customers can return products to any store.</span></span>


<span data-ttu-id="96b21-113">Bu ortak senaryolar Dynamics 365 for Retail kullanan perakendeciler için kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="96b21-113">Those common scenarios are available for retailers using Dynamics 365 for Retail.</span></span> <span data-ttu-id="96b21-114">Retail ile şunları yapabilirsiniz:</span><span class="sxs-lookup"><span data-stu-id="96b21-114">With Retail, you can:</span></span>
+ <span data-ttu-id="96b21-115">Diğer mağazalarda ürünleri aramak veya diğer mağazalardaki ürünlere göz atmak.</span><span class="sxs-lookup"><span data-stu-id="96b21-115">Search or browse products at other stores.</span></span>
+ <span data-ttu-id="96b21-116">Tüm serbest bırakılan ürünleri aramak veya göz atmak.</span><span class="sxs-lookup"><span data-stu-id="96b21-116">Search or browse all released products.</span></span>
+ <span data-ttu-id="96b21-117">peşin alış veriş hareketleri veya müşteri siparişleri oluşturmak.</span><span class="sxs-lookup"><span data-stu-id="96b21-117">Create cash-and-carry transactions or customer orders.</span></span>
+ <span data-ttu-id="96b21-118">Müşteri siparişleri için teslim seçeneklerini belirlemek.</span><span class="sxs-lookup"><span data-stu-id="96b21-118">Select delivery options for customer orders.</span></span>
+ <span data-ttu-id="96b21-119">Ürünleri geçerli mağazadan veya başka mağazadan seçmek.</span><span class="sxs-lookup"><span data-stu-id="96b21-119">Pick up products at the current store or another store.</span></span>
+ <span data-ttu-id="96b21-120">Geçerli mağazadaki veya başka mağazadaki siparişi iptal etmek.</span><span class="sxs-lookup"><span data-stu-id="96b21-120">Cancel an order at the current store or another store.</span></span>
+ <span data-ttu-id="96b21-121">Bir siparişi makbuzla veya makbuz olmadan geçerli mağazaya veya başka bir mağazaya iade etmek.</span><span class="sxs-lookup"><span data-stu-id="96b21-121">Return an order with or without the receipt at the current store or another store.</span></span>

