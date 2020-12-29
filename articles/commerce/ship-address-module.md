---
title: Sevkiyat adresi modülü
description: Bu konu sevkiyat adresi modülünü kapsamaktadır ve bu modülün Microsoft Dynamics 365 Commerce'ta nasıl yapılandırılacağını açıklamaktadır.
author: anupamar-ms
manager: annbe
ms.date: 08/05/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Operations, Retail, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.13
ms.openlocfilehash: aeaa410fde29b285fdbbdd6acac19b0c4e917aa5
ms.sourcegitcommit: 12d271bb26c7490e7525d9b4bbf125cdc39fef43
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/07/2020
ms.locfileid: "4416587"
---
# <a name="shipping-address-module"></a><span data-ttu-id="d617f-103">Sevkiyat adresi modülü</span><span class="sxs-lookup"><span data-stu-id="d617f-103">Shipping address module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="d617f-104">Bu konu sevkiyat adresi modülünü ele almaktadır ve bu modülün Microsoft Dynamics 365 Commerce'ta nasıl yapılandırılacağını açıklamaktadır.</span><span class="sxs-lookup"><span data-stu-id="d617f-104">This topic describes covers the shipping address module and explains how to configure it in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="d617f-105">Genel bakış</span><span class="sxs-lookup"><span data-stu-id="d617f-105">Overview</span></span>

<span data-ttu-id="d617f-106">Sevkiyat adresi modülü, müşteriye ödeme akışı sırasında bir siparişin sevkiyat adresini ekleme veya seçme olanağı verir.</span><span class="sxs-lookup"><span data-stu-id="d617f-106">The shipping address module lets customers add or select the shipping address for an order during the checkout flow.</span></span> <span data-ttu-id="d617f-107">Müşteri oturum açmışsa, o müşteri için önceden kaydedilmiş olan tüm adresler gösterilir ve müşteri bunlar arasından seçim yapabilir.</span><span class="sxs-lookup"><span data-stu-id="d617f-107">If a customer is signed in, any addresses that were previously saved for that customer are shown, and the customer can select among them.</span></span> <span data-ttu-id="d617f-108">Müşteri Ayrıca yeni bir adres ekleyebilir.</span><span class="sxs-lookup"><span data-stu-id="d617f-108">The customer can also add a new address.</span></span> <span data-ttu-id="d617f-109">Sevkiyat adresi modülü, siparişteki sevkiyat gerektiren tüm maddeler için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="d617f-109">The shipping address module is used for all items on an order that require shipping.</span></span>

<span data-ttu-id="d617f-110">Sevkiyat adresi biçimleri her ülke veya bölge için Commerce Headquarters'da tanımlanabilir ve sevkiyat adresi modülü ülkeye/bölgeye özel kurallar zorlar.</span><span class="sxs-lookup"><span data-stu-id="d617f-110">Shipping address formats can be defined in Commerce headquarters for each country or region, and the shipping address module then enforces country/region-specific rules.</span></span>

<span data-ttu-id="d617f-111">Müşteriler, ödeme akışı sırasında bir sevkiyat adresi girerken, adresi birincil adres olarak kaydetme seçeneği vardır.</span><span class="sxs-lookup"><span data-stu-id="d617f-111">When customers enter a shipping address during the checkout flow, they have the option to save the address as a primary address.</span></span> <span data-ttu-id="d617f-112">Bu seçenek yalnızca müşterinin oturum açmış olması durumunda gösterilir.</span><span class="sxs-lookup"><span data-stu-id="d617f-112">This option is shown only if a customer is signed in.</span></span>

<span data-ttu-id="d617f-113">Sevkiyat adresi modülü adres doğrulaması sağlamasa da, bu işlev özelliştirme yoluyla gerçekleştirilebilir.</span><span class="sxs-lookup"><span data-stu-id="d617f-113">Although the shipping address module doesn't provide address validation, this functionality can be implemented through customization.</span></span>

<span data-ttu-id="d617f-114">Aşağıdaki örnekte ödeme sayfasında kullanılan yeni bir teslimat adresi modülü örneği gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="d617f-114">The following illustration shows an example of a new shipping address module on a checkout page.</span></span>

![Ödeme sayfasındaki sevkiyat adresi modülü örneği](./media/ecommerce-shippingaddress.PNG)

## <a name="module-properties"></a><span data-ttu-id="d617f-116">Modül özellikleri</span><span class="sxs-lookup"><span data-stu-id="d617f-116">Module properties</span></span>

| <span data-ttu-id="d617f-117">Özellik adı</span><span class="sxs-lookup"><span data-stu-id="d617f-117">Property name</span></span> | <span data-ttu-id="d617f-118">Değerler</span><span class="sxs-lookup"><span data-stu-id="d617f-118">Values</span></span> | <span data-ttu-id="d617f-119">Tanım</span><span class="sxs-lookup"><span data-stu-id="d617f-119">Description</span></span> |
|---------------|--------|-------------|
| <span data-ttu-id="d617f-120">Başlık</span><span class="sxs-lookup"><span data-stu-id="d617f-120">Heading</span></span> | <span data-ttu-id="d617f-121">Başlık metmi ve başlık etiketi (**H1**, **H2**, **H3**, **H4**, **H5** veya **H6**)</span><span class="sxs-lookup"><span data-stu-id="d617f-121">Heading text and a heading tag (**H1**, **H2**, **H3**, **H4**, **H5**, or **H6**)</span></span> | <span data-ttu-id="d617f-122">Sevkiyat adresi modülü için isteğe bağlı bir başlık.</span><span class="sxs-lookup"><span data-stu-id="d617f-122">An optional heading for the shipping address module.</span></span> |
| <span data-ttu-id="d617f-123">Adres türünü göster</span><span class="sxs-lookup"><span data-stu-id="d617f-123">Show address type</span></span> | <span data-ttu-id="d617f-124">**Doğru** veya **yanlış**</span><span class="sxs-lookup"><span data-stu-id="d617f-124">**True** or **False**</span></span> | <span data-ttu-id="d617f-125">Bu isteğe bağlı özellik **Doğru** olarak ayarlanırsa, **Ev** veya **İş** gibi bir adres türü gösterilir.</span><span class="sxs-lookup"><span data-stu-id="d617f-125">If this optional property is set to **True**, an address type, such as **Home** or **Business**, will be shown.</span></span> <span data-ttu-id="d617f-126">Herhangi bir adres türü belirtilmezse, adres otomatik olarak **Tür**=**Diğer** olarak kaydedilir.</span><span class="sxs-lookup"><span data-stu-id="d617f-126">If no address type is specified, the address will automatically be saved as **Type**=**Other**.</span></span> |

## <a name="add-a-shipping-address-module-to-a-checkout-page-and-set-the-required-properties"></a><span data-ttu-id="d617f-127">Ödeme sayfasına sevkiyat adresi modülü ekleme ve gerekli özellikleri ayarlama</span><span class="sxs-lookup"><span data-stu-id="d617f-127">Add a shipping address module to a checkout page and set the required properties</span></span>

<span data-ttu-id="d617f-128">Sevkiyat adresi modülü yalnızca bir ödeme modülüne eklenebilir.</span><span class="sxs-lookup"><span data-stu-id="d617f-128">A shipping address module can be added only to a checkout module.</span></span> <span data-ttu-id="d617f-129">Sevkiyat adresi modülünü yapılandırma ve ödeme sayfasına ekleme hakkında daha fazla bilgi için bkz. [Ödeme modülü](add-checkout-module.md).</span><span class="sxs-lookup"><span data-stu-id="d617f-129">For more information about how to configure the shipping address module and add it to a checkout page, see [Checkout module](add-checkout-module.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="d617f-130">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="d617f-130">Additional resources</span></span>

[<span data-ttu-id="d617f-131">Sepet modülü</span><span class="sxs-lookup"><span data-stu-id="d617f-131">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="d617f-132">Sepet simgesi modülü</span><span class="sxs-lookup"><span data-stu-id="d617f-132">Cart icon module</span></span>](cart-icon-module.md)

[<span data-ttu-id="d617f-133">Ödeme yapma modülü</span><span class="sxs-lookup"><span data-stu-id="d617f-133">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="d617f-134">Ödeme modülü</span><span class="sxs-lookup"><span data-stu-id="d617f-134">Payment module</span></span>](payment-module.md)

[<span data-ttu-id="d617f-135">Teslimat seçenekleri modülü</span><span class="sxs-lookup"><span data-stu-id="d617f-135">Delivery options module</span></span>](delivery-options-module.md)

[<span data-ttu-id="d617f-136">Malzeme çekme bilgileri modülü</span><span class="sxs-lookup"><span data-stu-id="d617f-136">Pickup information module</span></span>](pickup-info-module.md)

[<span data-ttu-id="d617f-137">Sipariş ayrıntıları modülü</span><span class="sxs-lookup"><span data-stu-id="d617f-137">Order details module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="d617f-138">Hediye kartı modülü</span><span class="sxs-lookup"><span data-stu-id="d617f-138">Gift card module</span></span>](add-giftcard.md)
