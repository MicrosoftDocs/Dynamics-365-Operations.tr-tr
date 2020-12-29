---
title: Teslimat seçenekleri modülü
description: Bu konu teslimat seçenekleri modüllerini ve bunların Microsoft Dynamics 365 Commerce'te nasıl yapılandırılacağını açıklamaktadır.
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
ms.openlocfilehash: f9e8df576efd1e58fde235828823f31e87ed58bf
ms.sourcegitcommit: 12d271bb26c7490e7525d9b4bbf125cdc39fef43
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/07/2020
ms.locfileid: "4416592"
---
# <a name="delivery-options-module"></a><span data-ttu-id="f66a8-103">Teslimat seçenekleri modülü</span><span class="sxs-lookup"><span data-stu-id="f66a8-103">Delivery options module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="f66a8-104">Bu konu teslimat seçenekleri modüllerini ve bunların Microsoft Dynamics 365 Commerce'te nasıl yapılandırılacağını açıklamaktadır.</span><span class="sxs-lookup"><span data-stu-id="f66a8-104">This topic covers delivery options modules and explains how to configure them in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="f66a8-105">Genel bakış</span><span class="sxs-lookup"><span data-stu-id="f66a8-105">Overview</span></span>

<span data-ttu-id="f66a8-106">Teslimat seçenekleri modülleri, müşterilerin çevrimiçi siparişleri için sevkiyat veya çekme gibi bir teslimat şekli seçmesine olanak tanır.</span><span class="sxs-lookup"><span data-stu-id="f66a8-106">Delivery options modules let customers select a mode of delivery such as shipping or pickup for their online order.</span></span> <span data-ttu-id="f66a8-107">Teslimat şeklini belirlemek için bir sevkiyat adresi gereklidir.</span><span class="sxs-lookup"><span data-stu-id="f66a8-107">A shipping address is required to determine the mode of delivery.</span></span> <span data-ttu-id="f66a8-108">Sevkiyat adresi değiştirilirse, teslimat seçenekleri tekrar alınmalıdır.</span><span class="sxs-lookup"><span data-stu-id="f66a8-108">If the shipping address changes, the delivery options must be retrieved again.</span></span> <span data-ttu-id="f66a8-109">Siparişte yalnızca mağazadan teslim alınacak maddeler varsa, bu modül otomatik olarak gizlenir.</span><span class="sxs-lookup"><span data-stu-id="f66a8-109">If an order includes only items that will be picked up in a store, this module is automatically hidden.</span></span>

<span data-ttu-id="f66a8-110">Teslimat şekillerinin nasıl yapılandırılacağı hakkında bilgi için bkz. [Çevrimiçi kanal kurulumu](channel-setup-online.md) ve [Teslimat şekillerini ayarlama](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-up-modes-of-delivery).</span><span class="sxs-lookup"><span data-stu-id="f66a8-110">For information about how to configure modes of delivery, see [Online channel setup](channel-setup-online.md) and [Set up modes of delivery](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-up-modes-of-delivery).</span></span>

<span data-ttu-id="f66a8-111">Her teslimat şeklinin ilişkilendirilmiş masrafı olabilir.</span><span class="sxs-lookup"><span data-stu-id="f66a8-111">Each delivery mode can have an associated charge.</span></span> <span data-ttu-id="f66a8-112">Çevrimiçi mağaza için masrafları yapılandırma hakkında bilgi için bkz. [Çok yönlü kanal Gelişmiş otomatik masraflar](omni-auto-charges.md).</span><span class="sxs-lookup"><span data-stu-id="f66a8-112">For more information about how to configure charges for an online store, see [Omni-channel Advanced auto-charges](omni-auto-charges.md).</span></span>

<span data-ttu-id="f66a8-113">Commerce sürümü 10.0.13'te, teslimat seçenekleri modülü **Eşit dağıtım olmadan başlık masrafları** ve **Satır masrafı olarak sevkiyat** özelliklerini destekleyecek şekilde güncelleştirilmiştir.</span><span class="sxs-lookup"><span data-stu-id="f66a8-113">In Commerce version 10.0.13, the delivery options module has been updated to support the **Header charges without proration** and **Shipping as a line charge** features.</span></span> <span data-ttu-id="f66a8-114">Eşit dağıtma kapalıysa, beklenti e-Ticaret iş akışının sepetteki maddeler için karışık bir teslimat şekline (yani, bazı maddeler sevkiyat için seçilmiş, diğerleri teslim alma için seçilmiş) izin vermeyeceği yönündedir.</span><span class="sxs-lookup"><span data-stu-id="f66a8-114">If proration is turned off, the expectation is that the e-Commerce workflow won't allow a mixed mode of delivery for the items in the cart (that is, some items are selected for shipment, but others are selected for pickup).</span></span> <span data-ttu-id="f66a8-115">**Eşit dağıtım olmadan başlık masrafları** özelliği  Commerce Headquarters'da **Kanalda tutarlı teslimat şekli işlemeyi etkinleştir** bayrağının açık olmasını gerektirir.</span><span class="sxs-lookup"><span data-stu-id="f66a8-115">The **Header charges without proration** feature requires that the **Enable consistent delivery mode handling in channel** flag be turned on in Commerce headquarters.</span></span> <span data-ttu-id="f66a8-116">Bu bayrak açık olduğundai sevkiyat masrafları Commerce Headquarters'taki yapılandırmaya bağlı olarak başlık düzeyinde veya satır düzerinde uygulanır.</span><span class="sxs-lookup"><span data-stu-id="f66a8-116">When that flag is turned on, shipping charges will be applied at either the header level or the line level, depending on the configuration in Commerce headquarters.</span></span>

<span data-ttu-id="f66a8-117">Fabrikam teması, bazı maddelerin sevkiyat için diğerlerinin tesli alma için seçildiği karma teslimat modunu destekler.</span><span class="sxs-lookup"><span data-stu-id="f66a8-117">The Fabrikam theme supports a mixed mode of delivery, where some items are selected for shipment but others are selected for pickup.</span></span> <span data-ttu-id="f66a8-118">Bu modda, sevkiyat masrafları sevkiyat şekli için seçilen tüm maddeler için eşit olarak dağıtılır.</span><span class="sxs-lookup"><span data-stu-id="f66a8-118">In this mode, shipping charges will be prorated for all items that are selected for the shipping mode of delivery.</span></span> <span data-ttu-id="f66a8-119">Bir karma teslimat şeklinin çalışması için, ilk olarak **Eşit dağıtımlı başlık masrafları** özelliğini Commerce Headquarters'ta yapılandırmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="f66a8-119">For a mixed mode of delivery to work, you must first configure the **Header charges with proration** feature in Commerce headquarters.</span></span> <span data-ttu-id="f66a8-120">Bu yapılandırma hakkında daha fazla bilgi için bkz. [Satış satırlarıyla eşleştirmek için başlık masraflarını eşit dağırma](pro-rate-charges-matching-lines.md).</span><span class="sxs-lookup"><span data-stu-id="f66a8-120">For more information about this configuration, see [Prorate header charges to match sales lines](pro-rate-charges-matching-lines.md).</span></span>

<span data-ttu-id="f66a8-121">Sevkiyat giderleri satır maddeleri için geçerliyse, her madde için sepet satırında gösterilebilir.</span><span class="sxs-lookup"><span data-stu-id="f66a8-121">If shipping charges apply to line items, they can be shown on the cart line for each item.</span></span> <span data-ttu-id="f66a8-122">Bu işlev **Sevkiyat masraflarını satır maddesinde göster** özelliğinin hem sepet modülü hem de ödeme modülü için etkinleştirilmesini gerektirir.</span><span class="sxs-lookup"><span data-stu-id="f66a8-122">This functionality requires that the **Show shipping charges on line item** property be turned on for both the cart module and the checkout module.</span></span> <span data-ttu-id="f66a8-123">Daha fazla bilgi için bkz. [Sepet modülü](add-cart-module.md) ve [Ödeme modülü](add-checkout-module.md).</span><span class="sxs-lookup"><span data-stu-id="f66a8-123">For more information, see [Cart module](add-cart-module.md) and [Checkout module](add-checkout-module.md).</span></span>

<span data-ttu-id="f66a8-124">Aşağıdaki şekilde ödeme sayfasında kullanılan bir teslimat seçenekleri modülü örneği gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="f66a8-124">The following illustration shows an example of a delivery options module on a checkout page.</span></span>

![Ödeme sayfasındaki teslimat seçenekleri modülü örneği](./media/ecommerce-deliveryoptions.PNG)

## <a name="delivery-options-module-properties"></a><span data-ttu-id="f66a8-126">Teslimat seçenekleri modülü özellikleri</span><span class="sxs-lookup"><span data-stu-id="f66a8-126">Delivery options module properties</span></span>

| <span data-ttu-id="f66a8-127">Özellik</span><span class="sxs-lookup"><span data-stu-id="f66a8-127">Property</span></span> | <span data-ttu-id="f66a8-128">Değerler</span><span class="sxs-lookup"><span data-stu-id="f66a8-128">Values</span></span> | <span data-ttu-id="f66a8-129">Tanım</span><span class="sxs-lookup"><span data-stu-id="f66a8-129">Description</span></span> |
|----------|--------|-------------|
| <span data-ttu-id="f66a8-130">Başlık</span><span class="sxs-lookup"><span data-stu-id="f66a8-130">Heading</span></span> | <span data-ttu-id="f66a8-131">Başlık metmi ve başlık etiketi (**H1**, **H2**, **H3**, **H4**, **H5** veya **H6**)</span><span class="sxs-lookup"><span data-stu-id="f66a8-131">Heading text and a heading tag (**H1**, **H2**, **H3**, **H4**, **H5**, or **H6**)</span></span> | <span data-ttu-id="f66a8-132">Teslimar seçenekleri modülü için isteğe bağlı bir başlık.</span><span class="sxs-lookup"><span data-stu-id="f66a8-132">An optional heading for the delivery options module.</span></span> |
| <span data-ttu-id="f66a8-133">Özel CSS sınıfı adı</span><span class="sxs-lookup"><span data-stu-id="f66a8-133">Custom CSS class name</span></span> | <span data-ttu-id="f66a8-134">Metin</span><span class="sxs-lookup"><span data-stu-id="f66a8-134">Text</span></span> | <span data-ttu-id="f66a8-135">Varsa bu modülü işlemek için kullanılacak özel Geçişli Stil Sayfaları (CSS) sınıfı adı.</span><span class="sxs-lookup"><span data-stu-id="f66a8-135">A custom Cascading Style Sheets (CSS) class name that will be used to render this module, if applicable.</span></span> |
| <span data-ttu-id="f66a8-136">Teslimat Modu Seçeneğini Filtrele</span><span class="sxs-lookup"><span data-stu-id="f66a8-136">Filter Delivery Mode Option</span></span> | <span data-ttu-id="f66a8-137">**Filtreleme** veya **Sevkiyat dışı modlar**</span><span class="sxs-lookup"><span data-stu-id="f66a8-137">**Do not filter** or **Non-shipping modes**</span></span> | <span data-ttu-id="f66a8-138">Teslimat seçenekleri modülünün tüm sevkiyat dışı teslimat modlarına filtre uygulayıp uygulamayacağını belirten bir değer.</span><span class="sxs-lookup"><span data-stu-id="f66a8-138">A value that specifies whether the delivery options module should filter out all non-shipping delivery modes.</span></span> |

## <a name="add-a-delivery-options-module-to-a-checkout-page-and-set-the-required-properties"></a><span data-ttu-id="f66a8-139">Ödeme sayfasına teslimat seçenekleri modülü ekleme ve gerekli özellikleri ayarlama</span><span class="sxs-lookup"><span data-stu-id="f66a8-139">Add a delivery options module to a checkout page and set the required properties</span></span>

<span data-ttu-id="f66a8-140">Teslimat seçenekleri modülü yalnızca bir ödeme modülüne eklenebilir.</span><span class="sxs-lookup"><span data-stu-id="f66a8-140">A delivery options module can be added only to a checkout module.</span></span> <span data-ttu-id="f66a8-141">Teslimat seçenekleri modülünü yapılandırma ve ödeme sayfasına ekleme hakkında daha fazla bilgi için bkz. [Ödeme modülü](add-checkout-module.md).</span><span class="sxs-lookup"><span data-stu-id="f66a8-141">For more information about how to configure the delivery options module and add it to a checkout page, see [Checkout module](add-checkout-module.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="f66a8-142">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="f66a8-142">Additional resources</span></span>

[<span data-ttu-id="f66a8-143">Alışveriş sepeti modülü</span><span class="sxs-lookup"><span data-stu-id="f66a8-143">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="f66a8-144">Ödeme yapma modülü</span><span class="sxs-lookup"><span data-stu-id="f66a8-144">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="f66a8-145">Ödeme modülü</span><span class="sxs-lookup"><span data-stu-id="f66a8-145">Payment module</span></span>](payment-module.md)

[<span data-ttu-id="f66a8-146">Sevkiyat adresi modülü</span><span class="sxs-lookup"><span data-stu-id="f66a8-146">Shipping address module</span></span>](ship-address-module.md)

[<span data-ttu-id="f66a8-147">Malzeme çekme bilgileri modülü</span><span class="sxs-lookup"><span data-stu-id="f66a8-147">Pickup information module</span></span>](pickup-info-module.md)

[<span data-ttu-id="f66a8-148">Sipariş ayrıntıları modülü</span><span class="sxs-lookup"><span data-stu-id="f66a8-148">Order details module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="f66a8-149">Hediye kartı modülü</span><span class="sxs-lookup"><span data-stu-id="f66a8-149">Gift card module</span></span>](add-giftcard.md)

[<span data-ttu-id="f66a8-150">Çevrimiçi kanal kurulumu</span><span class="sxs-lookup"><span data-stu-id="f66a8-150">Online channel setup</span></span>](channel-setup-online.md)

[<span data-ttu-id="f66a8-151">Çok yönlü kanal Gelişmiş otomatik masraflar</span><span class="sxs-lookup"><span data-stu-id="f66a8-151">Omni-channel Advanced auto-charges</span></span>](omni-auto-charges.md)

[<span data-ttu-id="f66a8-152">Başlık masraflarını satış satırlarıyla eşleştirmek için eşit dağıtma</span><span class="sxs-lookup"><span data-stu-id="f66a8-152">Prorate header charges to match sales lines</span></span>](pro-rate-charges-matching-lines.md)

[<span data-ttu-id="f66a8-153">Teslimat şekillerini ayarla</span><span class="sxs-lookup"><span data-stu-id="f66a8-153">Set up modes of delivery</span></span>](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-up-modes-of-delivery)
