---
title: Sepet simgesi modülü
description: Bu konu sepet simgesi modülünü kapsamaktadır ve Microsoft Dynamics 365 Commerce'ın site sayfalarına nasıl ekleneceğini açıklamaktadır.
author: anupamar-ms
ms.date: 10/20/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 5ff514f07e8b31abe79775e5011bd3f1b24b2935
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/31/2021
ms.locfileid: "5793093"
---
# <a name="cart-icon-module"></a><span data-ttu-id="fc7b4-103">Sepet simgesi modülü</span><span class="sxs-lookup"><span data-stu-id="fc7b4-103">Cart icon module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="fc7b4-104">Bu konu sepet simgesi modülünü kapsamaktadır ve Microsoft Dynamics 365 Commerce'ın site sayfalarına nasıl ekleneceğini açıklamaktadır.</span><span class="sxs-lookup"><span data-stu-id="fc7b4-104">This topic covers the cart icon module and describes how to add it to site pages in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="fc7b4-105">Sepet simgesi modülü, sayfanın başlık modülündeki sepeti temsil eder ve sepetteki öğe sayısını gösterir.</span><span class="sxs-lookup"><span data-stu-id="fc7b4-105">The cart icon module represents the cart in the header module of the page, and shows the number of items in the cart.</span></span> <span data-ttu-id="fc7b4-106">Sepet simgesi modülü, sepet simgesi üzerine gelindiğinde sepet özetini de (mini sepet olarak da bilinir) görüntüler.</span><span class="sxs-lookup"><span data-stu-id="fc7b4-106">The cart icon module also displays a cart summary (also known as a mini cart) when the cart icon is hovered over.</span></span> <span data-ttu-id="fc7b4-107">Mini sepet, sepet sayfasına gitmek zorunda kalmadan sepetteki öğelerin özetini kullanıcıya sağlar.</span><span class="sxs-lookup"><span data-stu-id="fc7b4-107">The mini cart provides the user with a summary of the items in the cart without having to navigate to the cart page.</span></span> <span data-ttu-id="fc7b4-108">Ayrıca, kullanıcının özetten memnun olması durumunda doğrudan ödeme sayfasına gitmesine olanak tanır.</span><span class="sxs-lookup"><span data-stu-id="fc7b4-108">In addition, it also allows the user to directly go to checkout page if they are happy with the summary.</span></span> <span data-ttu-id="fc7b4-109">Bu, sayfa gezinti sayısını azaltır ve ödemenin daha hızlı yapılmasını sağlar.</span><span class="sxs-lookup"><span data-stu-id="fc7b4-109">This reduces the number of page navigations and makes checkout faster.</span></span> 

> [!NOTE]
> <span data-ttu-id="fc7b4-110">Sepet simgesi modülü desteği Dynamics 365 Commerce 10.0.11 sürümünde bulunabilir.</span><span class="sxs-lookup"><span data-stu-id="fc7b4-110">Support for the cart icon module is available in the Dynamics 365 Commerce 10.0.11 release.</span></span>

<span data-ttu-id="fc7b4-111">Aşağıdaki resimde, Fabrikam üstbilgisinde mini sepet görüntüleyen bir alışveriş sepeti simge modülü örneği gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="fc7b4-111">The following image shows an example of a cart icon module that displays a mini cart in the Fabrikam header.</span></span>

![Sepet simgesi modülü örneği](./media/ecommerce-Minicart.PNG)

## <a name="module-properties"></a><span data-ttu-id="fc7b4-113">Modül özellikleri</span><span class="sxs-lookup"><span data-stu-id="fc7b4-113">Module properties</span></span>

- <span data-ttu-id="fc7b4-114">**Mini sepeti göster** – Doğru olduğunda, bu özellik sepet simgesi üzerine gelindiğinde sepet özetinin (mini sepet) görüntülenmesini sağlar.</span><span class="sxs-lookup"><span data-stu-id="fc7b4-114">**Show mini cart** – When true, this property enables a cart summary (mini cart) to be displayed when the cart icon is hovered over.</span></span> <span data-ttu-id="fc7b4-115">Bu işlev yalnızca masaüstü görünüm bağlantı noktaları için desteklenir.</span><span class="sxs-lookup"><span data-stu-id="fc7b4-115">This functionality is only supported for desktop view ports.</span></span>

## <a name="add-a-cart-icon-module-to-a-page"></a><span data-ttu-id="fc7b4-116">Sayfaya sepet simgesi modülü ekleme</span><span class="sxs-lookup"><span data-stu-id="fc7b4-116">Add a cart icon module to a page</span></span>

<span data-ttu-id="fc7b4-117">Bir sepet simgesi modülü eklemek için, bkz. [Başlık modülü](author-header-module.md).</span><span class="sxs-lookup"><span data-stu-id="fc7b4-117">To add a cart icon module, see [Header module](author-header-module.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="fc7b4-118">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="fc7b4-118">Additional resources</span></span>

[<span data-ttu-id="fc7b4-119">Sepet modülü</span><span class="sxs-lookup"><span data-stu-id="fc7b4-119">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="fc7b4-120">Ödeme modülü</span><span class="sxs-lookup"><span data-stu-id="fc7b4-120">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="fc7b4-121">Ödeme modülü</span><span class="sxs-lookup"><span data-stu-id="fc7b4-121">Payment module</span></span>](payment-module.md)

[<span data-ttu-id="fc7b4-122">Sevkiyat adresi modülü</span><span class="sxs-lookup"><span data-stu-id="fc7b4-122">Shipping address module</span></span>](ship-address-module.md)

[<span data-ttu-id="fc7b4-123">Teslimat seçenekleri modülü</span><span class="sxs-lookup"><span data-stu-id="fc7b4-123">Delivery options module</span></span>](delivery-options-module.md)

[<span data-ttu-id="fc7b4-124">Malzeme çekme bilgileri modülü</span><span class="sxs-lookup"><span data-stu-id="fc7b4-124">Pickup information module</span></span>](pickup-info-module.md)

[<span data-ttu-id="fc7b4-125">Sipariş ayrıntıları modülü</span><span class="sxs-lookup"><span data-stu-id="fc7b4-125">Order details module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="fc7b4-126">Hediye kartı modülü</span><span class="sxs-lookup"><span data-stu-id="fc7b4-126">Gift card module</span></span>](add-giftcard.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]