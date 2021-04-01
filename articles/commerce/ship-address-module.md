---
title: Sevkiyat adresi modülü
description: Bu konu sevkiyat adresi modülünü kapsamaktadır ve bu modülün Microsoft Dynamics 365 Commerce'ta nasıl yapılandırılacağını açıklamaktadır.
author: anupamar-ms
manager: annbe
ms.date: 02/11/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.13
ms.openlocfilehash: e590c966ca6bd8111df5f91cbac0485afaa45c78
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5234425"
---
# <a name="shipping-address-module"></a><span data-ttu-id="768f6-103">Sevkiyat adresi modülü</span><span class="sxs-lookup"><span data-stu-id="768f6-103">Shipping address module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="768f6-104">Bu konu sevkiyat adresi modülünü ele almaktadır ve bu modülün Microsoft Dynamics 365 Commerce'ta nasıl yapılandırılacağını açıklamaktadır.</span><span class="sxs-lookup"><span data-stu-id="768f6-104">This topic describes covers the shipping address module and explains how to configure it in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="768f6-105">Sevkiyat adresi modülü, müşteriye ödeme akışı sırasında bir siparişin sevkiyat adresini ekleme veya seçme olanağı verir.</span><span class="sxs-lookup"><span data-stu-id="768f6-105">The shipping address module lets customers add or select the shipping address for an order during the checkout flow.</span></span> <span data-ttu-id="768f6-106">Müşteri oturum açmışsa, o müşteri için önceden kaydedilmiş olan tüm adresler gösterilir ve müşteri bunlar arasından seçim yapabilir.</span><span class="sxs-lookup"><span data-stu-id="768f6-106">If a customer is signed in, any addresses that were previously saved for that customer are shown, and the customer can select among them.</span></span> <span data-ttu-id="768f6-107">Müşteri Ayrıca yeni bir adres ekleyebilir.</span><span class="sxs-lookup"><span data-stu-id="768f6-107">The customer can also add a new address.</span></span> <span data-ttu-id="768f6-108">Sevkiyat adresi modülü, siparişteki sevkiyat gerektiren tüm maddeler için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="768f6-108">The shipping address module is used for all items on an order that require shipping.</span></span>

<span data-ttu-id="768f6-109">Sevkiyat adresi biçimleri her ülke veya bölge için Commerce Headquarters'da tanımlanabilir ve sevkiyat adresi modülü ülkeye/bölgeye özel kurallar zorlar.</span><span class="sxs-lookup"><span data-stu-id="768f6-109">Shipping address formats can be defined in Commerce headquarters for each country or region, and the shipping address module then enforces country/region-specific rules.</span></span>

<span data-ttu-id="768f6-110">Müşteriler, ödeme akışı sırasında bir sevkiyat adresi girerken, adresi birincil adres olarak kaydetme seçeneği vardır.</span><span class="sxs-lookup"><span data-stu-id="768f6-110">When customers enter a shipping address during the checkout flow, they have the option to save the address as a primary address.</span></span> <span data-ttu-id="768f6-111">Bu seçenek yalnızca müşterinin oturum açmış olması durumunda gösterilir.</span><span class="sxs-lookup"><span data-stu-id="768f6-111">This option is shown only if a customer is signed in.</span></span>

<span data-ttu-id="768f6-112">Sevkiyat adresi modülü adres doğrulaması sağlamasa da, bu işlev özelliştirme yoluyla gerçekleştirilebilir.</span><span class="sxs-lookup"><span data-stu-id="768f6-112">Although the shipping address module doesn't provide address validation, this functionality can be implemented through customization.</span></span>

<span data-ttu-id="768f6-113">Aşağıdaki örnekte ödeme sayfasında kullanılan yeni bir teslimat adresi modülü örneği gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="768f6-113">The following illustration shows an example of a new shipping address module on a checkout page.</span></span>

![Ödeme sayfasındaki sevkiyat adresi modülü örneği](./media/ecommerce-shippingaddress.PNG)

## <a name="module-properties"></a><span data-ttu-id="768f6-115">Modül özellikleri</span><span class="sxs-lookup"><span data-stu-id="768f6-115">Module properties</span></span>

| <span data-ttu-id="768f6-116">Özellik adı</span><span class="sxs-lookup"><span data-stu-id="768f6-116">Property name</span></span> | <span data-ttu-id="768f6-117">Değerler</span><span class="sxs-lookup"><span data-stu-id="768f6-117">Values</span></span> | <span data-ttu-id="768f6-118">Tanım</span><span class="sxs-lookup"><span data-stu-id="768f6-118">Description</span></span> |
|---------------|--------|-------------|
| <span data-ttu-id="768f6-119">Başlık</span><span class="sxs-lookup"><span data-stu-id="768f6-119">Heading</span></span> | <span data-ttu-id="768f6-120">Başlık metmi ve başlık etiketi (**H1**, **H2**, **H3**, **H4**, **H5** veya **H6**)</span><span class="sxs-lookup"><span data-stu-id="768f6-120">Heading text and a heading tag (**H1**, **H2**, **H3**, **H4**, **H5**, or **H6**)</span></span> | <span data-ttu-id="768f6-121">Sevkiyat adresi modülü için isteğe bağlı bir başlık.</span><span class="sxs-lookup"><span data-stu-id="768f6-121">An optional heading for the shipping address module.</span></span> |
| <span data-ttu-id="768f6-122">Adres türünü göster</span><span class="sxs-lookup"><span data-stu-id="768f6-122">Show address type</span></span> | <span data-ttu-id="768f6-123">**Doğru** veya **yanlış**</span><span class="sxs-lookup"><span data-stu-id="768f6-123">**True** or **False**</span></span> | <span data-ttu-id="768f6-124">Bu isteğe bağlı özellik **Doğru** olarak ayarlanırsa, **Ev** veya **İş** gibi bir adres türü gösterilir.</span><span class="sxs-lookup"><span data-stu-id="768f6-124">If this optional property is set to **True**, an address type, such as **Home** or **Business**, will be shown.</span></span> <span data-ttu-id="768f6-125">Herhangi bir adres türü belirtilmezse, adres otomatik olarak **Tür**=**Diğer** olarak kaydedilir.</span><span class="sxs-lookup"><span data-stu-id="768f6-125">If no address type is specified, the address will automatically be saved as **Type**=**Other**.</span></span> |
| <span data-ttu-id="768f6-126">Otomatik öneriyi etkinleştir</span><span class="sxs-lookup"><span data-stu-id="768f6-126">Enable auto suggestion</span></span>| <span data-ttu-id="768f6-127">**Doğru** veya **yanlış**</span><span class="sxs-lookup"><span data-stu-id="768f6-127">**True** or **False**</span></span> | <span data-ttu-id="768f6-128">Bu isteğe bağlı özellik **Doğru** olarak ayarlanırsa otomatik adres önerileri sağlanacaktır.</span><span class="sxs-lookup"><span data-stu-id="768f6-128">If this optional property is set to **True**, automatic address suggestions will be provided.</span></span> <span data-ttu-id="768f6-129">Bu öneriler Bing Haritalar tarafından desteklenmektedir.</span><span class="sxs-lookup"><span data-stu-id="768f6-129">These suggestions are powered by Bing Maps.</span></span> <span data-ttu-id="768f6-130">Sitenizde Bing Haritalar tümleştirmesini ayarlama hakkında bilgi için, bkz [Mağaza seçicisi modülü](store-selector.md).</span><span class="sxs-lookup"><span data-stu-id="768f6-130">For information about how to set up Bing Maps integration for your site, see [Store selector module](store-selector.md).</span></span> <span data-ttu-id="768f6-131">Bu özellik Commerce 10.0.15 sürümünden itibaren mevcuttur.</span><span class="sxs-lookup"><span data-stu-id="768f6-131">This feature is available as of the Commerce version 10.0.15 release.</span></span>|
|<span data-ttu-id="768f6-132">Otomatik öneri seçenekleri</span><span class="sxs-lookup"><span data-stu-id="768f6-132">Auto suggest options</span></span>| <span data-ttu-id="768f6-133">Bir sayı</span><span class="sxs-lookup"><span data-stu-id="768f6-133">A number</span></span>| <span data-ttu-id="768f6-134">Otomatik adres önerileri etkinse, sağlanacak maksimum öneri sayısı gibi ek seçenekler belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="768f6-134">If automatic address suggestions are enabled, you can specify additional options, such as the maximum number of suggestions that should be provided.</span></span>|

## <a name="add-a-shipping-address-module-to-a-checkout-page-and-set-the-required-properties"></a><span data-ttu-id="768f6-135">Ödeme sayfasına sevkiyat adresi modülü ekleme ve gerekli özellikleri ayarlama</span><span class="sxs-lookup"><span data-stu-id="768f6-135">Add a shipping address module to a checkout page and set the required properties</span></span>

<span data-ttu-id="768f6-136">Sevkiyat adresi modülü yalnızca bir ödeme modülüne eklenebilir.</span><span class="sxs-lookup"><span data-stu-id="768f6-136">A shipping address module can be added only to a checkout module.</span></span> <span data-ttu-id="768f6-137">Sevkiyat adresi modülünü yapılandırma ve ödeme sayfasına ekleme hakkında daha fazla bilgi için bkz. [Ödeme modülü](add-checkout-module.md).</span><span class="sxs-lookup"><span data-stu-id="768f6-137">For more information about how to configure the shipping address module and add it to a checkout page, see [Checkout module](add-checkout-module.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="768f6-138">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="768f6-138">Additional resources</span></span>

[<span data-ttu-id="768f6-139">Sepet modülü</span><span class="sxs-lookup"><span data-stu-id="768f6-139">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="768f6-140">Sepet simgesi modülü</span><span class="sxs-lookup"><span data-stu-id="768f6-140">Cart icon module</span></span>](cart-icon-module.md)

[<span data-ttu-id="768f6-141">Ödeme yapma modülü</span><span class="sxs-lookup"><span data-stu-id="768f6-141">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="768f6-142">Ödeme modülü</span><span class="sxs-lookup"><span data-stu-id="768f6-142">Payment module</span></span>](payment-module.md)

[<span data-ttu-id="768f6-143">Teslimat seçenekleri modülü</span><span class="sxs-lookup"><span data-stu-id="768f6-143">Delivery options module</span></span>](delivery-options-module.md)

[<span data-ttu-id="768f6-144">Malzeme çekme bilgileri modülü</span><span class="sxs-lookup"><span data-stu-id="768f6-144">Pickup information module</span></span>](pickup-info-module.md)

[<span data-ttu-id="768f6-145">Sipariş ayrıntıları modülü</span><span class="sxs-lookup"><span data-stu-id="768f6-145">Order details module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="768f6-146">Hediye kartı modülü</span><span class="sxs-lookup"><span data-stu-id="768f6-146">Gift card module</span></span>](add-giftcard.md)

[<span data-ttu-id="768f6-147">Mağaza seçicisi modülü</span><span class="sxs-lookup"><span data-stu-id="768f6-147">Store selector module</span></span>](store-selector.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]