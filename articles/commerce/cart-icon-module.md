---
title: Sepet simgesi modülü
description: Bu konu sepet simgesi modülünü kapsamaktadır ve Microsoft Dynamics 365 Commerce'ın site sayfalarına nasıl ekleneceğini açıklamaktadır.
author: anupamar-ms
manager: annbe
ms.date: 10/20/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: ebc5cfa490a4c8538fd081aced0844ed01d63a26
ms.sourcegitcommit: 12d271bb26c7490e7525d9b4bbf125cdc39fef43
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/07/2020
ms.locfileid: "4416585"
---
# <a name="cart-icon-module"></a><span data-ttu-id="4f3c5-103">Sepet simgesi modülü</span><span class="sxs-lookup"><span data-stu-id="4f3c5-103">Cart icon module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="4f3c5-104">Bu konu sepet simgesi modülünü kapsamaktadır ve Microsoft Dynamics 365 Commerce'ın site sayfalarına nasıl ekleneceğini açıklamaktadır.</span><span class="sxs-lookup"><span data-stu-id="4f3c5-104">This topic covers the cart icon module and describes how to add it to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="4f3c5-105">Özet</span><span class="sxs-lookup"><span data-stu-id="4f3c5-105">Overview</span></span>

<span data-ttu-id="4f3c5-106">Sepet simgesi modülü, sayfanın başlık modülündeki sepeti temsil eder ve sepetteki öğe sayısını gösterir.</span><span class="sxs-lookup"><span data-stu-id="4f3c5-106">The cart icon module represents the cart in the header module of the page, and shows the number of items in the cart.</span></span> <span data-ttu-id="4f3c5-107">Sepet simgesi modülü, sepet simgesi üzerine gelindiğinde sepet özetini de (mini sepet olarak da bilinir) görüntüler.</span><span class="sxs-lookup"><span data-stu-id="4f3c5-107">The cart icon module also displays a cart summary (also known as a mini cart) when the cart icon is hovered over.</span></span> <span data-ttu-id="4f3c5-108">Mini sepet, sepet sayfasına gitmek zorunda kalmadan sepetteki öğelerin özetini kullanıcıya sağlar.</span><span class="sxs-lookup"><span data-stu-id="4f3c5-108">The mini cart provides the user with a summary of the items in the cart without having to navigate to the cart page.</span></span> <span data-ttu-id="4f3c5-109">Ayrıca, kullanıcının özetten memnun olması durumunda doğrudan ödeme sayfasına gitmesine olanak tanır.</span><span class="sxs-lookup"><span data-stu-id="4f3c5-109">In addition, it also allows the user to directly go to checkout page if they are happy with the summary.</span></span> <span data-ttu-id="4f3c5-110">Bu, sayfa gezinti sayısını azaltır ve ödemenin daha hızlı yapılmasını sağlar.</span><span class="sxs-lookup"><span data-stu-id="4f3c5-110">This reduces the number of page navigations and makes checkout faster.</span></span> 

> [!NOTE]
> <span data-ttu-id="4f3c5-111">Sepet simgesi modülü desteği Dynamics 365 Commerce 10.0.11 sürümünde bulunabilir.</span><span class="sxs-lookup"><span data-stu-id="4f3c5-111">Support for the cart icon module is available in the Dynamics 365 Commerce 10.0.11 release.</span></span>

<span data-ttu-id="4f3c5-112">Aşağıdaki resimde, Fabrikam üstbilgisinde mini sepet görüntüleyen bir alışveriş sepeti simge modülü örneği gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="4f3c5-112">The following image shows an example of a cart icon module that displays a mini cart in the Fabrikam header.</span></span>

![Sepet simgesi modülü örneği](./media/ecommerce-Minicart.PNG)

## <a name="module-properties"></a><span data-ttu-id="4f3c5-114">Modül özellikleri</span><span class="sxs-lookup"><span data-stu-id="4f3c5-114">Module properties</span></span>

- <span data-ttu-id="4f3c5-115">**Mini sepeti göster** – Doğru olduğunda, bu özellik sepet simgesi üzerine gelindiğinde sepet özetinin (mini sepet) görüntülenmesini sağlar.</span><span class="sxs-lookup"><span data-stu-id="4f3c5-115">**Show mini cart** – When true, this property enables a cart summary (mini cart) to be displayed when the cart icon is hovered over.</span></span> <span data-ttu-id="4f3c5-116">Bu işlev yalnızca masaüstü görünüm bağlantı noktaları için desteklenir.</span><span class="sxs-lookup"><span data-stu-id="4f3c5-116">This functionality is only supported for desktop view ports.</span></span>

## <a name="add-a-cart-icon-module-to-a-page"></a><span data-ttu-id="4f3c5-117">Sayfaya sepet simgesi modülü ekleme</span><span class="sxs-lookup"><span data-stu-id="4f3c5-117">Add a cart icon module to a page</span></span>

<span data-ttu-id="4f3c5-118">Bir sepet simgesi modülü eklemek için, bkz. [Başlık modülü](author-header-module.md).</span><span class="sxs-lookup"><span data-stu-id="4f3c5-118">To add a cart icon module, see [Header module](author-header-module.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="4f3c5-119">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="4f3c5-119">Additional resources</span></span>

[<span data-ttu-id="4f3c5-120">Sepet modülü</span><span class="sxs-lookup"><span data-stu-id="4f3c5-120">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="4f3c5-121">Ödeme modülü</span><span class="sxs-lookup"><span data-stu-id="4f3c5-121">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="4f3c5-122">Ödeme modülü</span><span class="sxs-lookup"><span data-stu-id="4f3c5-122">Payment module</span></span>](payment-module.md)

[<span data-ttu-id="4f3c5-123">Sevkiyat adresi modülü</span><span class="sxs-lookup"><span data-stu-id="4f3c5-123">Shipping address module</span></span>](ship-address-module.md)

[<span data-ttu-id="4f3c5-124">Teslimat seçenekleri modülü</span><span class="sxs-lookup"><span data-stu-id="4f3c5-124">Delivery options module</span></span>](delivery-options-module.md)

[<span data-ttu-id="4f3c5-125">Malzeme çekme bilgileri modülü</span><span class="sxs-lookup"><span data-stu-id="4f3c5-125">Pickup information module</span></span>](pickup-info-module.md)

[<span data-ttu-id="4f3c5-126">Sipariş ayrıntıları modülü</span><span class="sxs-lookup"><span data-stu-id="4f3c5-126">Order details module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="4f3c5-127">Hediye kartı modülü</span><span class="sxs-lookup"><span data-stu-id="4f3c5-127">Gift card module</span></span>](add-giftcard.md)
