---
title: Sipariş onayı modülü
description: Bu konu sipariş onaylama modüllerini ve bunların nasıl Microsoft Dynamics 365 Commerce'te oluşturacağını açıklamaktadır ve kapsamaktadır.
author: anupamar
manager: annbe
ms.date: 10/31/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anupamar-ms
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: e339ce02bb646d0d9a68c22b24fde9b72071de6f
ms.sourcegitcommit: 295d940a345879b3dfc5991e387b91c7257019ea
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/01/2019
ms.locfileid: "2698338"
---
# <a name="order-confirmation-module"></a><span data-ttu-id="f876c-103">Sipariş onayı modülü</span><span class="sxs-lookup"><span data-stu-id="f876c-103">Order confirmation module</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="f876c-104">Bu konu sipariş onaylama modüllerini ve bunların nasıl Microsoft Dynamics 365 Commerce'te oluşturacağını açıklamaktadır ve kapsamaktadır.</span><span class="sxs-lookup"><span data-stu-id="f876c-104">This topic covers order confirmation modules and describes how to create them in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="f876c-105">Genel Bakış</span><span class="sxs-lookup"><span data-stu-id="f876c-105">Overview</span></span>

<span data-ttu-id="f876c-106">Sipariş onay modülü sipariş onay sayfasında bir sipariş yerleştirildikten sonra onay iletisi göstermek için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="f876c-106">An order confirmation module is used to show a confirmation message on an order confirmation page after an order is placed.</span></span> <span data-ttu-id="f876c-107">Sipariş teyidi modülü, teslim alma sırasında sağlanan sipariş onay numarasını ve müşteri e-posta adresini gösterir.</span><span class="sxs-lookup"><span data-stu-id="f876c-107">The order confirmation module shows the order confirmation number and the customer email address that was provided during checkout.</span></span>

<span data-ttu-id="f876c-108">Teslim alma sırasında bir sipariş verildiğinde, sipariş onay numarası ve müşteri e-posta adresi, sayfanın URL 'sinde sorgu dizesi olarak sipariş onayı sayfasına geçirilir.</span><span class="sxs-lookup"><span data-stu-id="f876c-108">When an order is placed during checkout, the order confirmation number and customer email address are passed to the order confirmation page as a query string in the page's URL.</span></span> <span data-ttu-id="f876c-109">Sipariş onayı modülü bu bilgileri alır ve sipariş onayı sayfasında sipariş durumunu işler.</span><span class="sxs-lookup"><span data-stu-id="f876c-109">The order confirmation module receives this information and renders the order status on the order confirmation page.</span></span> <span data-ttu-id="f876c-110">Sipariş teyidi modülü siparişin durumunu sağlamak için bu sayfa bağlamını gerektiriyor.</span><span class="sxs-lookup"><span data-stu-id="f876c-110">The order confirmation module requires this page context to provide the status of the order.</span></span>

## <a name="order-confirmation-module-properties"></a><span data-ttu-id="f876c-111">Sipariş onayı modülü özellikleri</span><span class="sxs-lookup"><span data-stu-id="f876c-111">Order confirmation module properties</span></span>

| <span data-ttu-id="f876c-112">Özellik adı</span><span class="sxs-lookup"><span data-stu-id="f876c-112">Property name</span></span> | <span data-ttu-id="f876c-113">Değerler</span><span class="sxs-lookup"><span data-stu-id="f876c-113">Values</span></span> | <span data-ttu-id="f876c-114">Tanım</span><span class="sxs-lookup"><span data-stu-id="f876c-114">Description</span></span> |
|---------------|--------|-------------|
| <span data-ttu-id="f876c-115">Başlık</span><span class="sxs-lookup"><span data-stu-id="f876c-115">Heading</span></span>       | <span data-ttu-id="f876c-116">Başlık metni ve başlık etiketi (**H1**, **H2**, **H3**, **H4**, **H5** veya **H6**)</span><span class="sxs-lookup"><span data-stu-id="f876c-116">Heading text and heading tag (**H1**, **H2**, **H3**, **H4**, **H5**, or **H6**)</span></span> | <span data-ttu-id="f876c-117">Sipariş teyidi modülünün başlığı olabilir.</span><span class="sxs-lookup"><span data-stu-id="f876c-117">The order confirmation module can have a heading.</span></span> <span data-ttu-id="f876c-118">Varsayılan olarak, başlık için **H2** başlık etiketi kullanılır.</span><span class="sxs-lookup"><span data-stu-id="f876c-118">By default, the **H2** heading tag is used for the heading.</span></span> <span data-ttu-id="f876c-119">Ancak, bu etiket erişilebilirlik gereksinimlerini karşılayacak şekilde değiştirilebilir.</span><span class="sxs-lookup"><span data-stu-id="f876c-119">However, the tag can be changed to meet accessibility requirements.</span></span> |

## <a name="modules-that-can-be-used-in-an-order-confirmation-page-module"></a><span data-ttu-id="f876c-120">Sipariş onayı sayfası modülünde kullanılabilen modüller</span><span class="sxs-lookup"><span data-stu-id="f876c-120">Modules that can be used in an order confirmation page module</span></span> 

- <span data-ttu-id="f876c-121">**Öneriler** – müşteriye diğer ürünleri önermek için, sipariş onayı sayfasına öneri modülü koyulamıyor.</span><span class="sxs-lookup"><span data-stu-id="f876c-121">**Recommendations** – The recommendations module can be put on the order confirmation page to suggest other products to the customer.</span></span>
- <span data-ttu-id="f876c-122">**Pazarlama** – Pazarlama modülü, pazarlama içeriğini sipariş onayı sayfasına ekleyebilir.</span><span class="sxs-lookup"><span data-stu-id="f876c-122">**Marketing** – The marketing module can add marketing content to the order confirmation page.</span></span>

## <a name="create-an-order-confirmation-page-module"></a><span data-ttu-id="f876c-123">Sipariş onayı sayfa modülü oluşturma</span><span class="sxs-lookup"><span data-stu-id="f876c-123">Create an order confirmation page module</span></span>

1. <span data-ttu-id="f876c-124">**Sipariş onayı şablonu** adlı bir sayfa şablonu oluşturun.</span><span class="sxs-lookup"><span data-stu-id="f876c-124">Create a page template that is named **order confirmation template**.</span></span>
1. <span data-ttu-id="f876c-125">Varsayılan sayfanın **ana** yuvasına bir sipariş onayı modülü ekleyin.</span><span class="sxs-lookup"><span data-stu-id="f876c-125">In the **Main** slot of the default page, add an order confirmation module.</span></span>
1. <span data-ttu-id="f876c-126">Sipariş onayı modülünde bir öneri modülü ekleyin.</span><span class="sxs-lookup"><span data-stu-id="f876c-126">In the order confirmation module, add a recommendations module.</span></span>
1. <span data-ttu-id="f876c-127">Şablonu kaydet ve önizleyin.</span><span class="sxs-lookup"><span data-stu-id="f876c-127">Save and preview the template.</span></span> <span data-ttu-id="f876c-128">Sipariş onay numarasının bağlamını gerektirdiğinden, sipariş teyidi modülü işlenmemelidir.</span><span class="sxs-lookup"><span data-stu-id="f876c-128">The order confirmation module should not be rendered, because it requires the context of the order confirmation number.</span></span>
1. <span data-ttu-id="f876c-129">Şablonu giriş yapın ve yayımlayın.</span><span class="sxs-lookup"><span data-stu-id="f876c-129">Check in the template, and publish it.</span></span>
1. <span data-ttu-id="f876c-130">**Sipariş onayı sayfası** adlı bir sayfa oluşturmak için yeni oluşturduğunuz sipariş onayı şablonunu kullanın.</span><span class="sxs-lookup"><span data-stu-id="f876c-130">Use the order confirmation template that you just created to create a page that is named **order confirmation page**.</span></span>
1. <span data-ttu-id="f876c-131">Sayfa anahattına varsayılan sayfayı ekleyin.</span><span class="sxs-lookup"><span data-stu-id="f876c-131">Add the default page to the page outline.</span></span>
1. <span data-ttu-id="f876c-132">**Üstbilgi** yuvasında bir üstbilgi parçası ekleyin.</span><span class="sxs-lookup"><span data-stu-id="f876c-132">In the **Header** slot, add a header fragment.</span></span>
1. <span data-ttu-id="f876c-133">**Altbilgi** yuvasında bir altbilgi parçası ekleyin.</span><span class="sxs-lookup"><span data-stu-id="f876c-133">In the **Footer** slot, add a footer fragment.</span></span>
1. <span data-ttu-id="f876c-134">**Ana** yuvasına bir sipariş onayı modülü ekleyin.</span><span class="sxs-lookup"><span data-stu-id="f876c-134">In the **Main** slot, add an order confirmation module.</span></span>
1. <span data-ttu-id="f876c-135">Sipariş onayı modülünün Özellik bölmesinde Başlık **Sipariş onayını** ekleyin.</span><span class="sxs-lookup"><span data-stu-id="f876c-135">In the property pane of the order confirmation module, add the heading **Order confirmation**.</span></span>
1. <span data-ttu-id="f876c-136">Sipariş onayı modülünün altında, bir öneri modülü ekleyin ve bunu **yeni** ve **en iyi satış** ayarlarını kullanacak şekilde konfigüre edin.</span><span class="sxs-lookup"><span data-stu-id="f876c-136">Below the order confirmation module, add a recommendations module, and configure it so that it uses the **New** and **Best Selling** settings.</span></span>
1. <span data-ttu-id="f876c-137">Sayfayı önizleyin ve kaydedin, giriş yapın ve yayımlayın.</span><span class="sxs-lookup"><span data-stu-id="f876c-137">Save and preview the page, check it in, and publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="f876c-138">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="f876c-138">Additional resources</span></span>

[<span data-ttu-id="f876c-139">Başlangıç paketine genel bakış</span><span class="sxs-lookup"><span data-stu-id="f876c-139">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="f876c-140">Konteyner modülü</span><span class="sxs-lookup"><span data-stu-id="f876c-140">Container module</span></span>](add-container-module.md)

[<span data-ttu-id="f876c-141">Satınalma kutusu modülü</span><span class="sxs-lookup"><span data-stu-id="f876c-141">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="f876c-142">Sepet modülü</span><span class="sxs-lookup"><span data-stu-id="f876c-142">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="f876c-143">Ödeme modülü</span><span class="sxs-lookup"><span data-stu-id="f876c-143">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="f876c-144">Üst bilgi modülü</span><span class="sxs-lookup"><span data-stu-id="f876c-144">Header module</span></span>](author-header-module.md)

[<span data-ttu-id="f876c-145">Alt bilgi modülü</span><span class="sxs-lookup"><span data-stu-id="f876c-145">Footer module</span></span>](author-footer-module.md)
