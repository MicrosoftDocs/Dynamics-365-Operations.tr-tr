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
ms.openlocfilehash: 380d268ec0ba64367f090c31408eac1c54d0ff17
ms.sourcegitcommit: ae0843763a8b6b232bb71db326fab28605ac6c53
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/05/2020
ms.locfileid: "3661453"
---
# <a name="shipping-address-module"></a><span data-ttu-id="bc219-103">Sevkiyat adresi modülü</span><span class="sxs-lookup"><span data-stu-id="bc219-103">Shipping address module</span></span>

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

<span data-ttu-id="bc219-104">Bu konu sevkiyat adresi modülünü ele almaktadır ve bu modülün Microsoft Dynamics 365 Commerce'ta nasıl yapılandırılacağını açıklamaktadır.</span><span class="sxs-lookup"><span data-stu-id="bc219-104">This topic describes covers the shipping address module and explains how to configure it in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="bc219-105">Genel bakış</span><span class="sxs-lookup"><span data-stu-id="bc219-105">Overview</span></span>

<span data-ttu-id="bc219-106">Sevkiyat adresi modülü, müşteriye ödeme akışı sırasında bir siparişin sevkiyat adresini ekleme veya seçme olanağı verir.</span><span class="sxs-lookup"><span data-stu-id="bc219-106">The shipping address module lets customers add or select the shipping address for an order during the checkout flow.</span></span> <span data-ttu-id="bc219-107">Müşteri oturum açmışsa, o müşteri için önceden kaydedilmiş olan tüm adresler gösterilir ve müşteri bunlar arasından seçim yapabilir.</span><span class="sxs-lookup"><span data-stu-id="bc219-107">If a customer is signed in, any addresses that were previously saved for that customer are shown, and the customer can select among them.</span></span> <span data-ttu-id="bc219-108">Müşteri Ayrıca yeni bir adres ekleyebilir.</span><span class="sxs-lookup"><span data-stu-id="bc219-108">The customer can also add a new address.</span></span> <span data-ttu-id="bc219-109">Sevkiyat adresi modülü, siparişteki sevkiyat gerektiren tüm maddeler için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="bc219-109">The shipping address module is used for all items on an order that require shipping.</span></span>

<span data-ttu-id="bc219-110">Sevkiyat adresi biçimleri her ülke veya bölge için Commerce Headquarters'da tanımlanabilir ve sevkiyat adresi modülü ülkeye/bölgeye özel kurallar zorlar.</span><span class="sxs-lookup"><span data-stu-id="bc219-110">Shipping address formats can be defined in Commerce headquarters for each country or region, and the shipping address module then enforces country/region-specific rules.</span></span>

<span data-ttu-id="bc219-111">Müşteriler, ödeme akışı sırasında bir sevkiyat adresi girerken, adresi birincil adres olarak kaydetme seçeneği vardır.</span><span class="sxs-lookup"><span data-stu-id="bc219-111">When customers enter a shipping address during the checkout flow, they have the option to save the address as a primary address.</span></span> <span data-ttu-id="bc219-112">Bu seçenek yalnızca müşterinin oturum açmış olması durumunda gösterilir.</span><span class="sxs-lookup"><span data-stu-id="bc219-112">This option is shown only if a customer is signed in.</span></span>

<span data-ttu-id="bc219-113">Sevkiyat adresi modülü adres doğrulaması sağlamasa da, bu işlev özelliştirme yoluyla gerçekleştirilebilir.</span><span class="sxs-lookup"><span data-stu-id="bc219-113">Although the shipping address module doesn't provide address validation, this functionality can be implemented through customization.</span></span>

<span data-ttu-id="bc219-114">Aşağıdaki örnekte ödeme sayfasında kullanılan yeni bir teslimat adresi modülü örneği gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="bc219-114">The following illustration shows an example of a new shipping address module on a checkout page.</span></span>

![Ödeme sayfasındaki sevkiyat adresi modülü örneği](./media/ecommerce-shippingaddress.PNG)

## <a name="module-properties"></a><span data-ttu-id="bc219-116">Modül özellikleri</span><span class="sxs-lookup"><span data-stu-id="bc219-116">Module properties</span></span>

| <span data-ttu-id="bc219-117">Özellik adı</span><span class="sxs-lookup"><span data-stu-id="bc219-117">Property name</span></span> | <span data-ttu-id="bc219-118">Değerler</span><span class="sxs-lookup"><span data-stu-id="bc219-118">Values</span></span> | <span data-ttu-id="bc219-119">Tanım</span><span class="sxs-lookup"><span data-stu-id="bc219-119">Description</span></span> |
|---------------|--------|-------------|
| <span data-ttu-id="bc219-120">Başlık</span><span class="sxs-lookup"><span data-stu-id="bc219-120">Heading</span></span> | <span data-ttu-id="bc219-121">Başlık metmi ve başlık etiketi (**H1**, **H2**, **H3**, **H4**, **H5** veya **H6**)</span><span class="sxs-lookup"><span data-stu-id="bc219-121">Heading text and a heading tag (**H1**, **H2**, **H3**, **H4**, **H5**, or **H6**)</span></span> | <span data-ttu-id="bc219-122">Sevkiyat adresi modülü için isteğe bağlı bir başlık.</span><span class="sxs-lookup"><span data-stu-id="bc219-122">An optional heading for the shipping address module.</span></span> |
| <span data-ttu-id="bc219-123">Adres türünü göster</span><span class="sxs-lookup"><span data-stu-id="bc219-123">Show address type</span></span> | <span data-ttu-id="bc219-124">**Doğru** veya **yanlış**</span><span class="sxs-lookup"><span data-stu-id="bc219-124">**True** or **False**</span></span> | <span data-ttu-id="bc219-125">Bu isteğe bağlı özellik **Doğru** olarak ayarlanırsa, **Ev** veya **İş** gibi bir adres türü gösterilir.</span><span class="sxs-lookup"><span data-stu-id="bc219-125">If this optional property is set to **True**, an address type, such as **Home** or **Business**, will be shown.</span></span> <span data-ttu-id="bc219-126">Herhangi bir adres türü belirtilmezse, adres otomatik olarak **Tür**=**Diğer** olarak kaydedilir.</span><span class="sxs-lookup"><span data-stu-id="bc219-126">If no address type is specified, the address will automatically be saved as **Type**=**Other**.</span></span> |

## <a name="add-a-shipping-address-module-to-a-checkout-page-and-set-the-required-properties"></a><span data-ttu-id="bc219-127">Ödeme sayfasına sevkiyat adresi modülü ekleme ve gerekli özellikleri ayarlama</span><span class="sxs-lookup"><span data-stu-id="bc219-127">Add a shipping address module to a checkout page and set the required properties</span></span>

<span data-ttu-id="bc219-128">Sevkiyat adresi modülü yalnızca bir ödeme modülüne eklenebilir.</span><span class="sxs-lookup"><span data-stu-id="bc219-128">A shipping address module can be added only to a checkout module.</span></span> <span data-ttu-id="bc219-129">Sevkiyat adresi modülünü yapılandırma ve ödeme sayfasına ekleme hakkında daha fazla bilgi için bkz. [Ödeme modülü](add-checkout-module.md).</span><span class="sxs-lookup"><span data-stu-id="bc219-129">For more information about how to configure the shipping address module and add it to a checkout page, see [Checkout module](add-checkout-module.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="bc219-130">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="bc219-130">Additional resources</span></span>

[<span data-ttu-id="bc219-131">Sepet modülü</span><span class="sxs-lookup"><span data-stu-id="bc219-131">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="bc219-132">Sepet simgesi modülü</span><span class="sxs-lookup"><span data-stu-id="bc219-132">Cart icon module</span></span>](cart-icon-module.md)

[<span data-ttu-id="bc219-133">Ödeme modülü</span><span class="sxs-lookup"><span data-stu-id="bc219-133">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="bc219-134">Ödeme modülü</span><span class="sxs-lookup"><span data-stu-id="bc219-134">Payment module</span></span>](payment-module.md)

[<span data-ttu-id="bc219-135">Teslimat seçenekleri modülü</span><span class="sxs-lookup"><span data-stu-id="bc219-135">Delivery options module</span></span>](delivery-options-module.md)

[<span data-ttu-id="bc219-136">Sipariş ayrıntıları modülü</span><span class="sxs-lookup"><span data-stu-id="bc219-136">Order details module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="bc219-137">Hediye kartı modülü</span><span class="sxs-lookup"><span data-stu-id="bc219-137">Gift card module</span></span>](add-giftcard.md)
