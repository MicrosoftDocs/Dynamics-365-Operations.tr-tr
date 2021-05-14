---
title: Teslimat seçenekleri modülü
description: Bu konu teslimat seçenekleri modüllerini ve bunların Microsoft Dynamics 365 Commerce'te nasıl yapılandırılacağını açıklamaktadır.
author: anupamar-ms
manager: annbe
ms.date: 04/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.13
ms.openlocfilehash: 12b0281a27dcf5f567bcd6be5530fa8e26a4ae99
ms.sourcegitcommit: 593438a145672c55ff6a910eabce2939300b40ad
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2021
ms.locfileid: "5937494"
---
# <a name="delivery-options-module"></a><span data-ttu-id="f7f43-103">Teslimat seçenekleri modülü</span><span class="sxs-lookup"><span data-stu-id="f7f43-103">Delivery options module</span></span>

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

<span data-ttu-id="f7f43-104">Bu konu teslimat seçenekleri modüllerini ve bunların Microsoft Dynamics 365 Commerce'te nasıl yapılandırılacağını açıklamaktadır.</span><span class="sxs-lookup"><span data-stu-id="f7f43-104">This topic covers delivery options modules and explains how to configure them in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="f7f43-105">Teslimat seçenekleri modülleri, müşterilerin çevrimiçi siparişleri için sevkiyat veya çekme gibi bir teslimat şekli seçmesine olanak tanır.</span><span class="sxs-lookup"><span data-stu-id="f7f43-105">Delivery options modules let customers select a mode of delivery such as shipping or pickup for their online order.</span></span> <span data-ttu-id="f7f43-106">Teslimat şeklini belirlemek için bir sevkiyat adresi gereklidir.</span><span class="sxs-lookup"><span data-stu-id="f7f43-106">A shipping address is required to determine the mode of delivery.</span></span> <span data-ttu-id="f7f43-107">Sevkiyat adresi değiştirilirse, teslimat seçenekleri tekrar alınmalıdır.</span><span class="sxs-lookup"><span data-stu-id="f7f43-107">If the shipping address changes, the delivery options must be retrieved again.</span></span> <span data-ttu-id="f7f43-108">Siparişte yalnızca mağazadan teslim alınacak maddeler varsa, bu modül otomatik olarak gizlenir.</span><span class="sxs-lookup"><span data-stu-id="f7f43-108">If an order includes only items that will be picked up in a store, this module is automatically hidden.</span></span>

<span data-ttu-id="f7f43-109">Teslimat şekillerinin nasıl yapılandırılacağı hakkında bilgi için bkz. [Çevrimiçi kanal kurulumu](channel-setup-online.md) ve [Teslimat şekillerini ayarlama](/dynamicsax-2012/appuser-itpro/set-up-modes-of-delivery).</span><span class="sxs-lookup"><span data-stu-id="f7f43-109">For information about how to configure modes of delivery, see [Online channel setup](channel-setup-online.md) and [Set up modes of delivery](/dynamicsax-2012/appuser-itpro/set-up-modes-of-delivery).</span></span>

<span data-ttu-id="f7f43-110">Her teslimat şeklinin ilişkilendirilmiş masrafı olabilir.</span><span class="sxs-lookup"><span data-stu-id="f7f43-110">Each delivery mode can have an associated charge.</span></span> <span data-ttu-id="f7f43-111">Çevrimiçi mağaza için masrafları yapılandırma hakkında bilgi için bkz. [Çok yönlü kanal Gelişmiş otomatik masraflar](omni-auto-charges.md).</span><span class="sxs-lookup"><span data-stu-id="f7f43-111">For more information about how to configure charges for an online store, see [Omni-channel Advanced auto-charges](omni-auto-charges.md).</span></span>

<span data-ttu-id="f7f43-112">Commerce sürümü 10.0.13'te, teslimat seçenekleri modülü **Eşit dağıtım olmadan başlık masrafları** ve **Satır masrafı olarak sevkiyat** özelliklerini destekleyecek şekilde güncelleştirilmiştir.</span><span class="sxs-lookup"><span data-stu-id="f7f43-112">In Commerce version 10.0.13, the delivery options module has been updated to support the **Header charges without proration** and **Shipping as a line charge** features.</span></span> <span data-ttu-id="f7f43-113">Eşit dağıtma kapalıysa, beklenti e-Ticaret iş akışının sepetteki maddeler için karışık bir teslimat şekline (yani, bazı maddeler sevkiyat için seçilmiş, diğerleri teslim alma için seçilmiş) izin vermeyeceği yönündedir.</span><span class="sxs-lookup"><span data-stu-id="f7f43-113">If proration is turned off, the expectation is that the e-Commerce workflow won't allow a mixed mode of delivery for the items in the cart (that is, some items are selected for shipment, but others are selected for pickup).</span></span> <span data-ttu-id="f7f43-114">**Eşit dağıtım olmadan başlık masrafları** özelliği  Commerce Genel merkezde **Kanalda tutarlı teslimat şekli işlemeyi etkinleştir** bayrağının açık olmasını gerektirir.</span><span class="sxs-lookup"><span data-stu-id="f7f43-114">The **Header charges without proration** feature requires that the **Enable consistent delivery mode handling in channel** flag is turned on in Commerce headquarters.</span></span> <span data-ttu-id="f7f43-115">Bu özellik bayrağı açık olduğunda sevkiyat masrafları Commerce genel merkezdeki yapılandırmaya bağlı olarak başlık düzeyinde veya satır düzeyinde uygulanır.</span><span class="sxs-lookup"><span data-stu-id="f7f43-115">When the feature flag is turned on, shipping charges will be applied at either the header level or the line level, depending on the configuration in Commerce headquarters.</span></span>

<span data-ttu-id="f7f43-116">Fabrikam teması, bazı maddelerin sevkiyat için diğerlerinin tesli alma için seçildiği karma teslimat modunu destekler.</span><span class="sxs-lookup"><span data-stu-id="f7f43-116">The Fabrikam theme supports a mixed mode of delivery, where some items are selected for shipment but others are selected for pickup.</span></span> <span data-ttu-id="f7f43-117">Bu modda, sevkiyat masrafları sevkiyat şekli için seçilen tüm maddeler için eşit olarak dağıtılır.</span><span class="sxs-lookup"><span data-stu-id="f7f43-117">In this mode, shipping charges will be prorated for all items that are selected for the shipping mode of delivery.</span></span> <span data-ttu-id="f7f43-118">Bir karma teslimat şeklinin çalışması için, ilk olarak **Eşit dağıtımlı başlık masrafları** özelliğini Commerce Headquarters'ta yapılandırmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="f7f43-118">For a mixed mode of delivery to work, you must first configure the **Header charges with proration** feature in Commerce headquarters.</span></span> <span data-ttu-id="f7f43-119">Bu yapılandırma hakkında daha fazla bilgi için bkz. [Satış satırlarıyla eşleştirmek için başlık masraflarını eşit dağırma](pro-rate-charges-matching-lines.md).</span><span class="sxs-lookup"><span data-stu-id="f7f43-119">For more information about this configuration, see [Prorate header charges to match sales lines](pro-rate-charges-matching-lines.md).</span></span>

<span data-ttu-id="f7f43-120">Sevkiyat giderleri satır maddeleri için geçerliyse, her madde için sepet satırında gösterilebilir.</span><span class="sxs-lookup"><span data-stu-id="f7f43-120">If shipping charges apply to line items, they can be shown on the cart line for each item.</span></span> <span data-ttu-id="f7f43-121">Bu işlev **Sevkiyat masraflarını satır maddesinde göster** özelliğinin hem sepet modülü hem de ödeme modülü için etkinleştirilmesini gerektirir.</span><span class="sxs-lookup"><span data-stu-id="f7f43-121">This functionality requires that the **Show shipping charges on line item** property be turned on for both the cart module and the checkout module.</span></span> <span data-ttu-id="f7f43-122">Daha fazla bilgi için bkz. [Sepet modülü](add-cart-module.md) ve [Ödeme modülü](add-checkout-module.md).</span><span class="sxs-lookup"><span data-stu-id="f7f43-122">For more information, see [Cart module](add-cart-module.md) and [Checkout module](add-checkout-module.md).</span></span>

<span data-ttu-id="f7f43-123">Aşağıdaki şekilde ödeme sayfasında kullanılan bir teslimat seçenekleri modülü örneği gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="f7f43-123">The following illustration shows an example of a delivery options module on a checkout page.</span></span>

![Ödeme sayfasındaki teslimat seçenekleri modülü örneği](./media/ecommerce-deliveryoptions.PNG)

## <a name="delivery-options-module-properties"></a><span data-ttu-id="f7f43-125">Teslimat seçenekleri modülü özellikleri</span><span class="sxs-lookup"><span data-stu-id="f7f43-125">Delivery options module properties</span></span>

| <span data-ttu-id="f7f43-126">Özellik</span><span class="sxs-lookup"><span data-stu-id="f7f43-126">Property</span></span> | <span data-ttu-id="f7f43-127">Değerler</span><span class="sxs-lookup"><span data-stu-id="f7f43-127">Values</span></span> | <span data-ttu-id="f7f43-128">Tanım</span><span class="sxs-lookup"><span data-stu-id="f7f43-128">Description</span></span> |
|----------|--------|-------------|
| <span data-ttu-id="f7f43-129">Başlık</span><span class="sxs-lookup"><span data-stu-id="f7f43-129">Heading</span></span> | <span data-ttu-id="f7f43-130">Başlık metmi ve başlık etiketi (**H1**, **H2**, **H3**, **H4**, **H5** veya **H6**)</span><span class="sxs-lookup"><span data-stu-id="f7f43-130">Heading text and a heading tag (**H1**, **H2**, **H3**, **H4**, **H5**, or **H6**)</span></span> | <span data-ttu-id="f7f43-131">Teslimar seçenekleri modülü için isteğe bağlı bir başlık.</span><span class="sxs-lookup"><span data-stu-id="f7f43-131">An optional heading for the delivery options module.</span></span> |
| <span data-ttu-id="f7f43-132">Özel CSS sınıfı adı</span><span class="sxs-lookup"><span data-stu-id="f7f43-132">Custom CSS class name</span></span> | <span data-ttu-id="f7f43-133">Metin</span><span class="sxs-lookup"><span data-stu-id="f7f43-133">Text</span></span> | <span data-ttu-id="f7f43-134">Varsa bu modülü işlemek için kullanılacak özel Geçişli Stil Sayfaları (CSS) sınıfı adı.</span><span class="sxs-lookup"><span data-stu-id="f7f43-134">A custom Cascading Style Sheets (CSS) class name that will be used to render this module, if applicable.</span></span> |
| <span data-ttu-id="f7f43-135">Teslimat Modu Seçeneğini Filtrele</span><span class="sxs-lookup"><span data-stu-id="f7f43-135">Filter Delivery Mode Option</span></span> | <span data-ttu-id="f7f43-136">**Filtreleme** veya **Sevkiyat dışı modlar**</span><span class="sxs-lookup"><span data-stu-id="f7f43-136">**Do not filter** or **Non-shipping modes**</span></span> | <span data-ttu-id="f7f43-137">Teslimat seçenekleri modülünün tüm sevkiyat dışı teslimat modlarına filtre uygulayıp uygulamayacağını belirten bir değer.</span><span class="sxs-lookup"><span data-stu-id="f7f43-137">A value that specifies whether the delivery options module should filter out all non-shipping delivery modes.</span></span> |
| <span data-ttu-id="f7f43-138">Teslimat seçeneğini otomatik olarak belirleme</span><span class="sxs-lookup"><span data-stu-id="f7f43-138">Auto select a delivery option</span></span> | <span data-ttu-id="f7f43-139">**Filtre uygulama**, **Teslimat seçeneğini otomatik olarak belirle ve özeti göster** veya **Teslimat seçeneğini otomatik olarak seç ve özet gösterme**</span><span class="sxs-lookup"><span data-stu-id="f7f43-139">**Do not filter**, **Auto select delivery option and show summary**, or **Auto select delivery option and don't show summary**</span></span> | <span data-ttu-id="f7f43-140">Bu özellik, kullanıcının seçim yapmasını gerektirmeden, ilk kullanılabilir teslimat seçeneğini ödeme için otomatik olarak uygular.</span><span class="sxs-lookup"><span data-stu-id="f7f43-140">This property automatically applies the first available delivery option to checkout without requiring the user to select it.</span></span> <span data-ttu-id="f7f43-141">Yalnızca bir kullanılabilir teslimat seçeneği varsa kullanılmalıdır.</span><span class="sxs-lookup"><span data-stu-id="f7f43-141">It should be used only if there is one available delivery option.</span></span> <span data-ttu-id="f7f43-142">Bu özellik, Commerce 10.0.19 sürümüyle birlikte desteklenmeye başlanmıştır.</span><span class="sxs-lookup"><span data-stu-id="f7f43-142">This property is supported as of the Commerce version 10.0.19 release.</span></span> |

## <a name="add-a-delivery-options-module-to-a-checkout-page-and-set-the-required-properties"></a><span data-ttu-id="f7f43-143">Ödeme sayfasına teslimat seçenekleri modülü ekleme ve gerekli özellikleri ayarlama</span><span class="sxs-lookup"><span data-stu-id="f7f43-143">Add a delivery options module to a checkout page and set the required properties</span></span>

<span data-ttu-id="f7f43-144">Teslimat seçenekleri modülü yalnızca bir ödeme modülüne eklenebilir.</span><span class="sxs-lookup"><span data-stu-id="f7f43-144">A delivery options module can be added only to a checkout module.</span></span> <span data-ttu-id="f7f43-145">Teslimat seçenekleri modülünü yapılandırma ve ödeme sayfasına ekleme hakkında daha fazla bilgi için bkz. [Ödeme modülü](add-checkout-module.md).</span><span class="sxs-lookup"><span data-stu-id="f7f43-145">For more information about how to configure the delivery options module and add it to a checkout page, see [Checkout module](add-checkout-module.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="f7f43-146">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="f7f43-146">Additional resources</span></span>

[<span data-ttu-id="f7f43-147">Alışveriş sepeti modülü</span><span class="sxs-lookup"><span data-stu-id="f7f43-147">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="f7f43-148">Ödeme yapma modülü</span><span class="sxs-lookup"><span data-stu-id="f7f43-148">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="f7f43-149">Ödeme modülü</span><span class="sxs-lookup"><span data-stu-id="f7f43-149">Payment module</span></span>](payment-module.md)

[<span data-ttu-id="f7f43-150">Sevkiyat adresi modülü</span><span class="sxs-lookup"><span data-stu-id="f7f43-150">Shipping address module</span></span>](ship-address-module.md)

[<span data-ttu-id="f7f43-151">Malzeme çekme bilgileri modülü</span><span class="sxs-lookup"><span data-stu-id="f7f43-151">Pickup information module</span></span>](pickup-info-module.md)

[<span data-ttu-id="f7f43-152">Sipariş ayrıntıları modülü</span><span class="sxs-lookup"><span data-stu-id="f7f43-152">Order details module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="f7f43-153">Hediye kartı modülü</span><span class="sxs-lookup"><span data-stu-id="f7f43-153">Gift card module</span></span>](add-giftcard.md)

[<span data-ttu-id="f7f43-154">Çevrimiçi kanal kurulumu</span><span class="sxs-lookup"><span data-stu-id="f7f43-154">Online channel setup</span></span>](channel-setup-online.md)

[<span data-ttu-id="f7f43-155">Çok yönlü kanal Gelişmiş otomatik masraflar</span><span class="sxs-lookup"><span data-stu-id="f7f43-155">Omni-channel Advanced auto-charges</span></span>](omni-auto-charges.md)

[<span data-ttu-id="f7f43-156">Başlık masraflarını satış satırlarıyla eşleştirmek için eşit dağıtma</span><span class="sxs-lookup"><span data-stu-id="f7f43-156">Prorate header charges to match sales lines</span></span>](pro-rate-charges-matching-lines.md)

[<span data-ttu-id="f7f43-157">Teslimat şekillerini ayarla</span><span class="sxs-lookup"><span data-stu-id="f7f43-157">Set up modes of delivery</span></span>](/dynamicsax-2012/appuser-itpro/set-up-modes-of-delivery)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
