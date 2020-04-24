---
title: Sepet simgesi modülü
description: Bu konu sepet simgesi modülünü kapsamaktadır ve Microsoft Dynamics 365 Commerce'ın site sayfalarına nasıl ekleneceğini açıklamaktadır.
author: anupamar-ms
manager: annbe
ms.date: 04/13/2020
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
ms.openlocfilehash: 8cc96e0476a9d8a46aed7011359dc65fbc678fbf
ms.sourcegitcommit: ac966ea3a6c557fb5f9634b187b0e788d3e82d4d
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/14/2020
ms.locfileid: "3261594"
---
# <a name="cart-icon-module"></a><span data-ttu-id="2f6cc-103">Sepet simgesi modülü</span><span class="sxs-lookup"><span data-stu-id="2f6cc-103">Cart icon module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="2f6cc-104">Bu konu sepet simgesi modülünü kapsamaktadır ve Microsoft Dynamics 365 Commerce'ın site sayfalarına nasıl ekleneceğini açıklamaktadır.</span><span class="sxs-lookup"><span data-stu-id="2f6cc-104">This topic covers the cart icon module and describes how to add it to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="2f6cc-105">Özet</span><span class="sxs-lookup"><span data-stu-id="2f6cc-105">Overview</span></span>

<span data-ttu-id="2f6cc-106">Sepet simgesi modülü, sayfanın başlık modülündeki sepeti temsil eder ve sepetteki öğe sayısını gösterir.</span><span class="sxs-lookup"><span data-stu-id="2f6cc-106">The cart icon module represents the cart in the header module of the page, and shows the number of items in the cart.</span></span> <span data-ttu-id="2f6cc-107">Sepet simgesi modülü, sepet simgesi üzerine gelindiğinde sepet özetini de (mini sepet olarak da bilinir) görüntüler.</span><span class="sxs-lookup"><span data-stu-id="2f6cc-107">The cart icon module also displays a cart summary (also known as a mini cart) when the cart icon is hovered over.</span></span> <span data-ttu-id="2f6cc-108">Mini sepet, sepet sayfasına gitmek zorunda kalmadan sepetteki öğelerin özetini kullanıcıya sağlar.</span><span class="sxs-lookup"><span data-stu-id="2f6cc-108">The mini cart provides the user with a summary of the items in the cart without having to navigate to the cart page.</span></span> <span data-ttu-id="2f6cc-109">Ayrıca, kullanıcının özetten memnun olması durumunda doğrudan ödeme sayfasına gitmesine olanak tanır.</span><span class="sxs-lookup"><span data-stu-id="2f6cc-109">In addition, it also allows the user to directly go to checkout page if they are happy with the summary.</span></span> <span data-ttu-id="2f6cc-110">Bu, sayfa gezinti sayısını azaltır ve ödemenin daha hızlı yapılmasını sağlar.</span><span class="sxs-lookup"><span data-stu-id="2f6cc-110">This reduces the number of page navigations and makes checkout faster.</span></span> 

## <a name="module-properties"></a><span data-ttu-id="2f6cc-111">Modül özellikleri</span><span class="sxs-lookup"><span data-stu-id="2f6cc-111">Module properties</span></span>

- <span data-ttu-id="2f6cc-112">**Mini sepeti göster** – Doğru olduğunda, bu özellik sepet simgesi üzerine gelindiğinde sepet özetinin (mini sepet) görüntülenmesini sağlar.</span><span class="sxs-lookup"><span data-stu-id="2f6cc-112">**Show mini cart** – When true, this property enables a cart summary (mini cart) to be displayed when the cart icon is hovered over.</span></span> <span data-ttu-id="2f6cc-113">Bu işlev yalnızca masaüstü görünüm bağlantı noktaları için desteklenir.</span><span class="sxs-lookup"><span data-stu-id="2f6cc-113">This functionality is only supported for desktop view ports.</span></span>


## <a name="add-a-cart-icon-module-to-a-page"></a><span data-ttu-id="2f6cc-114">Sayfaya sepet simgesi modülü ekleme</span><span class="sxs-lookup"><span data-stu-id="2f6cc-114">Add a cart icon module to a page</span></span>

<span data-ttu-id="2f6cc-115">Bir sepet simgesi modülü eklemek için, bkz. [Başlık modülü](author-header-module.md).</span><span class="sxs-lookup"><span data-stu-id="2f6cc-115">To add a cart icon module, see [Header module](author-header-module.md).</span></span>


## <a name="additional-resources"></a><span data-ttu-id="2f6cc-116">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="2f6cc-116">Additional resources</span></span>

[<span data-ttu-id="2f6cc-117">Satınalma kutusu modülü</span><span class="sxs-lookup"><span data-stu-id="2f6cc-117">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="2f6cc-118">Sepet modülü</span><span class="sxs-lookup"><span data-stu-id="2f6cc-118">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="2f6cc-119">Ödeme modülü</span><span class="sxs-lookup"><span data-stu-id="2f6cc-119">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="2f6cc-120">Sipariş onayı modülü</span><span class="sxs-lookup"><span data-stu-id="2f6cc-120">Order confirmation module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="2f6cc-121">Üst bilgi modülü</span><span class="sxs-lookup"><span data-stu-id="2f6cc-121">Header module</span></span>](author-header-module.md)

[<span data-ttu-id="2f6cc-122">Alt bilgi modülü</span><span class="sxs-lookup"><span data-stu-id="2f6cc-122">Footer module</span></span>](author-footer-module.md)
