---
title: Ödeme modülü
description: Bu konu ödeme modülünü kapsamaktadır ve bu modülün Microsoft Dynamics 365 Commerce'ta nasıl yapılandırılacağını açıklamaktadır.
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
ms.openlocfilehash: 4267391edaf70ec645933b2c5c08a72735f52894
ms.sourcegitcommit: 97ceb24f191161ca601e0889a539df665834ac3b
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/16/2020
ms.locfileid: "3818338"
---
# <a name="payment-module"></a><span data-ttu-id="3c476-103">Ödeme modülü</span><span class="sxs-lookup"><span data-stu-id="3c476-103">Payment module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="3c476-104">Bu konu ödeme modülünü kapsamaktadır ve bu modülün Microsoft Dynamics 365 Commerce'ta nasıl yapılandırılacağını açıklamaktadır.</span><span class="sxs-lookup"><span data-stu-id="3c476-104">This topic covers the payment module and explains how to configure it in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="3c476-105">Genel bakış</span><span class="sxs-lookup"><span data-stu-id="3c476-105">Overview</span></span>

<span data-ttu-id="3c476-106">Ödeme modülü, müşteriye bir kredi kartı veya banka kartı kullanarak sipariş ödemesi yapma olanağı tanır.</span><span class="sxs-lookup"><span data-stu-id="3c476-106">The payment module lets customers pay for orders by using credit or debit cards.</span></span> <span data-ttu-id="3c476-107">Bu modül için ödeme tümleştirmesi, Adyen için Dynamics 365 Ödeme Bağlayıcısı tarafından sağlanır.</span><span class="sxs-lookup"><span data-stu-id="3c476-107">Payment integration for this module is provided by the Dynamics 365 Payment Connector for Adyen.</span></span> <span data-ttu-id="3c476-108">Ödeme bağlayıcısını kurma ve yapılandırma hakkında daha fazla bilgi için bkz. [Adyen için Dynamics 365 Ödeme Bağlayıcısı](dev-itpro/adyen-connector.md).</span><span class="sxs-lookup"><span data-stu-id="3c476-108">For more information about how to set up and configure the payment connector, see [Dynamics 365 Payment Connector for Adyen](dev-itpro/adyen-connector.md).</span></span>

<span data-ttu-id="3c476-109">Ödeme modülü, Adyen aracılığıyla HTML satır içi çerçevesinde (iframe) sunulan ödeme bilgilerini barındırır.</span><span class="sxs-lookup"><span data-stu-id="3c476-109">The payment module hosts the payment information that is served via Adyen in an HTML inline frame (iframe).</span></span> <span data-ttu-id="3c476-110">Ödeme modülü, Adyen ödeme bilgilerini almak için Commerce Scale Unit ile etkileşime girer.</span><span class="sxs-lookup"><span data-stu-id="3c476-110">The payment module interacts with the Commerce Scale Unit to retrieve the Adyen payment information.</span></span> <span data-ttu-id="3c476-111">Commerce Scale Unit etkileşiminin bir parçası olarak, ödeme modülü, fatura adres bilgilerinin iframe'de veya ayrı bir modül olarak sunulmasını sağlar.</span><span class="sxs-lookup"><span data-stu-id="3c476-111">As part of the Commerce Scale Unit interaction, the payment module can allow billing address information to be served either in the iframe or as a separate module.</span></span> <span data-ttu-id="3c476-112">Fabrikam temasında, fatura adresi ayrı bir modülde gösterilir.</span><span class="sxs-lookup"><span data-stu-id="3c476-112">In the Fabrikam theme, the billing address is shown in a separate module.</span></span> <span data-ttu-id="3c476-113">Adres satırları sevkiyat adresinin satırlarına benzeyecek şekilde işlenebileceğinden, bu yaklaşım daha fazla biçimlendirme esnekliği sağlar.</span><span class="sxs-lookup"><span data-stu-id="3c476-113">This approach allows for more formatting flexibility, because the address lines can be rendered so that they resemble the lines of the shipping address.</span></span>

<span data-ttu-id="3c476-114">Ayrıca ödeme modülü de oturum açmış müşterilerin ödeme bilgilerini kaydetmesine olanak tanır.</span><span class="sxs-lookup"><span data-stu-id="3c476-114">The payment module also lets signed-in customers save their payment information.</span></span> <span data-ttu-id="3c476-115">Ödeme bilgileri ve faturalama adresi, Adyen ödeme bağlayıcısı aracılığıyla kaydedilir ve yönetilir.</span><span class="sxs-lookup"><span data-stu-id="3c476-115">The payment information and billing address are saved and managed via the Adyen payment connector.</span></span>

<span data-ttu-id="3c476-116">Ödeme modülü, bağlılık programı puanları veya hediye kartı tarafından henüz kapsanmayan sipariş giderlerini kapsar.</span><span class="sxs-lookup"><span data-stu-id="3c476-116">The payment module covers any order charges that aren't already covered by loyalty points or a gift card.</span></span> <span data-ttu-id="3c476-117">Bir siparişin toplamı bağlılık programı veya hediye kartı kredileri tarafından karşılanacaksa, ödeme modülü gizlenir ve müşteri siparişi bu modül olmadan verebilir.</span><span class="sxs-lookup"><span data-stu-id="3c476-117">If the total for an order is fully covered by loyalty points or gift card credits, the payment module will be hidden, and the customer will be able to place the order without it.</span></span>

<span data-ttu-id="3c476-118">Adyen ödeme bağlayıcısı güçlü müşteri kimlik doğrulamasını (SCA) da destekler.</span><span class="sxs-lookup"><span data-stu-id="3c476-118">The Adyen payment connector also supports strong customer authentication (SCA).</span></span> <span data-ttu-id="3c476-119">Avrupa Birliği (AB) Ödeme Hizmetleri Yönergesi 2.0 (PSD2.0), çevrimiçi alışverişçilerin elektronik ödeme yöntemi kullandıklarında çevrimiçi alışveriş deneyimlerinin dışında kimlik doğrulamasının yapılmasını gerektirir.</span><span class="sxs-lookup"><span data-stu-id="3c476-119">Part of the European Union (EU) Payment Services Directive 2.0 (PSD2.0) requires that online shoppers be authenticated outside their online shopping experience when they use an electronic payment method.</span></span> <span data-ttu-id="3c476-120">Ödeme akışı sırasında, müşteriler kendi bankacılık sitesine yönlendirilir.</span><span class="sxs-lookup"><span data-stu-id="3c476-120">During the checkout flow,  customers are redirected to their banking site.</span></span> <span data-ttu-id="3c476-121">Ardından, kimlik doğrulamasından sonra yeniden Commerce ödeme akışına yönlendirilir.</span><span class="sxs-lookup"><span data-stu-id="3c476-121">Then, after authentication, they are redirected back to the Commerce checkout flow.</span></span> <span data-ttu-id="3c476-122">Bu yeniden yönlendirme sırasında, bir müşterinin ödeme akışına girdiği bilgiler (örneğin, sevkiyat adresi, teslimat seçenekleri, hediye kartı bilgileri ve bağlılık programı bilgileri) kalır.</span><span class="sxs-lookup"><span data-stu-id="3c476-122">During this redirection, the information that a customer entered in the checkout flow (for example, the shipping address, delivery options, gift card information, and loyalty information) will persist.</span></span> <span data-ttu-id="3c476-123">Bu özelliği etkinleştirmeden önce, SCA için ödeme bağlayıcısının Commerce Headquarters'da yapılandırılması gerekir.</span><span class="sxs-lookup"><span data-stu-id="3c476-123">Before you can turn on this feature, the payment connector must be configured for SCA in Commerce headquarters.</span></span> <span data-ttu-id="3c476-124">Daha fazla bilgi için bkz. [Adyen kullanarak Güçlü Müşteri Kimlik Doğrulaması](adyen_redirect.md).</span><span class="sxs-lookup"><span data-stu-id="3c476-124">For more information, see [Strong Customer Authentication using Adyen](adyen_redirect.md).</span></span>

<span data-ttu-id="3c476-125">Aşağıdaki resimde, ödeme sayfasındaki hediye kartı, bağlılık ve ödeme modülleri gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="3c476-125">The following illustration shows an example of gift card, loyalty, and payment modules on a checkout page.</span></span>

![Ödeme sayfasındaki hediye kartı, bağlılık ve ödeme modüllerini gösteren örnek](./media/ecommerce-payments.PNG)

## <a name="payment-module-properties"></a><span data-ttu-id="3c476-127">Ödeme modülü özellikleri</span><span class="sxs-lookup"><span data-stu-id="3c476-127">Payment module properties</span></span>

| <span data-ttu-id="3c476-128">Özellik adı</span><span class="sxs-lookup"><span data-stu-id="3c476-128">Property name</span></span> | <span data-ttu-id="3c476-129">Değerler</span><span class="sxs-lookup"><span data-stu-id="3c476-129">Values</span></span> | <span data-ttu-id="3c476-130">Tanım</span><span class="sxs-lookup"><span data-stu-id="3c476-130">Description</span></span> |
|---------------|--------|-------------|
| <span data-ttu-id="3c476-131">Başlık</span><span class="sxs-lookup"><span data-stu-id="3c476-131">Heading</span></span> | <span data-ttu-id="3c476-132">Başlık metni</span><span class="sxs-lookup"><span data-stu-id="3c476-132">Heading text</span></span> | <span data-ttu-id="3c476-133">Ödeme modülü için isteğe bağlı bir başlık.</span><span class="sxs-lookup"><span data-stu-id="3c476-133">An optional heading for the payment module.</span></span> |
| <span data-ttu-id="3c476-134">iframe yüksekliği.</span><span class="sxs-lookup"><span data-stu-id="3c476-134">Height of the iframe</span></span> | <span data-ttu-id="3c476-135">Piksel</span><span class="sxs-lookup"><span data-stu-id="3c476-135">Pixels</span></span> | <span data-ttu-id="3c476-136">Piksel cinsinden iframe yüksekliği.</span><span class="sxs-lookup"><span data-stu-id="3c476-136">The iframe height, in pixels.</span></span> <span data-ttu-id="3c476-137">Yükseklik gerektiği gibi ayarlanabilir.</span><span class="sxs-lookup"><span data-stu-id="3c476-137">The height can be adjusted as required.</span></span> |
| <span data-ttu-id="3c476-138">Fatura adresini göster</span><span class="sxs-lookup"><span data-stu-id="3c476-138">Show billing address</span></span> | <span data-ttu-id="3c476-139">**Doğru** veya **yanlış**</span><span class="sxs-lookup"><span data-stu-id="3c476-139">**True** or **False**</span></span> | <span data-ttu-id="3c476-140">Bu özellik **Doğru** olarak ayarlanırsa, faturalama adresi ödeme modülü iframe içinde Adyen tarafından sunulur.</span><span class="sxs-lookup"><span data-stu-id="3c476-140">If this property is set to **True**, the billing address will be served by Adyen inside the payment module iframe.</span></span> <span data-ttu-id="3c476-141">**Yanlış** olarak ayarlanırsa, faturalama adresi Adyen tarafından işlenmez ve Commerce kullanıcısının ödeme sayfasında fatura adresini göstermek için bir modül yapılandırması gerekir.</span><span class="sxs-lookup"><span data-stu-id="3c476-141">If it's set to **False**, the billing address won't be served by Adyen, and a Commerce user will have to configure a module to show the billing address on the checkout page.</span></span> |
| <span data-ttu-id="3c476-142">Ödeme stilini geçersiz kıl</span><span class="sxs-lookup"><span data-stu-id="3c476-142">Payment style override</span></span> | <span data-ttu-id="3c476-143">Geçişli Stil Sayfaları (CSS) kodu</span><span class="sxs-lookup"><span data-stu-id="3c476-143">Cascading Style Sheets (CSS) code</span></span> | <span data-ttu-id="3c476-144">Ödeme modülü bir iframe içinde barındırıldığından, sınırlı stil oluşturma yeteneği vardır.</span><span class="sxs-lookup"><span data-stu-id="3c476-144">Because the payment module is hosted in an iframe, there is limited styling capability.</span></span> <span data-ttu-id="3c476-145">Bu özelliği kullanarak bazı stil özellikleri elde edebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="3c476-145">You can achieve some styling by using this property.</span></span> <span data-ttu-id="3c476-146">Site stillerini geçersiz kılmak için CSS kodunu bu özelliğin değeri olarak yapıştırmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="3c476-146">To override site styles, you must paste the CSS code as the value of this property.</span></span> <span data-ttu-id="3c476-147">Site oluşturucu CSS geçersiz kılmaları ve stilleri bu modüle uygulanamaz.</span><span class="sxs-lookup"><span data-stu-id="3c476-147">Site builder CSS overrides and styles don't apply to this module.</span></span> |

## <a name="billing-address"></a><span data-ttu-id="3c476-148">Fatura adresi</span><span class="sxs-lookup"><span data-stu-id="3c476-148">Billing address</span></span>

<span data-ttu-id="3c476-149">Ödeme modülü müşterilerinin ödeme bilgileri için faturalama adresi sağlamasına olanak tanır.</span><span class="sxs-lookup"><span data-stu-id="3c476-149">The payment module lets customers provide a billing address for their payment information.</span></span> <span data-ttu-id="3c476-150">Ayrıca, fatura adresi olarak sevkiyat adresini kullanma olanağı sunarak ödeme akışının daha kolay ve hızlı olmasını sağlar.</span><span class="sxs-lookup"><span data-stu-id="3c476-150">It also lets them  use their shipping address as the billing address, to make the checkout flow easier and faster.</span></span> <span data-ttu-id="3c476-151">**Fatura adresini göster** özelliği **Yanlış** olarak ayarlanırsa, ödeme modülü ödeme sayfasında yapılandırılmalıdır.</span><span class="sxs-lookup"><span data-stu-id="3c476-151">If the **Show billing address** property is set to **False**, the payment module should be configured on the checkout page.</span></span>

## <a name="add-a-payment-module-to-a-checkout-page-and-set-the-required-properties"></a><span data-ttu-id="3c476-152">Bir ödeme sayfasına ödeme modülü ekleme ve gerekli özellikleri ayarlama</span><span class="sxs-lookup"><span data-stu-id="3c476-152">Add a payment module to a checkout page and set the required properties</span></span>

<span data-ttu-id="3c476-153">Ödeme modülü yalnızca bir ödeme modülüne eklenebilir.</span><span class="sxs-lookup"><span data-stu-id="3c476-153">A payment module can be added only to a checkout module.</span></span> <span data-ttu-id="3c476-154">Bir ödeme sayfası için ödeme modülü yapılandırmayla ilgili daha fazla bilgi için bkz. [Ödeme modülü](add-checkout-module.md).</span><span class="sxs-lookup"><span data-stu-id="3c476-154">For more information about how to configure a payment module for a checkout page, see [Checkout module](add-checkout-module.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="3c476-155">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="3c476-155">Additional resources</span></span>

[<span data-ttu-id="3c476-156">Sepet modülü</span><span class="sxs-lookup"><span data-stu-id="3c476-156">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="3c476-157">Sepet simgesi modülü</span><span class="sxs-lookup"><span data-stu-id="3c476-157">Cart icon module</span></span>](cart-icon-module.md)

[<span data-ttu-id="3c476-158">Ödeme modülü</span><span class="sxs-lookup"><span data-stu-id="3c476-158">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="3c476-159">Sevkiyat adresi modülü</span><span class="sxs-lookup"><span data-stu-id="3c476-159">Shipping address module</span></span>](ship-address-module.md)

[<span data-ttu-id="3c476-160">Teslimat seçenekleri modülü</span><span class="sxs-lookup"><span data-stu-id="3c476-160">Delivery options module</span></span>](delivery-options-module.md)

[<span data-ttu-id="3c476-161">Sipariş ayrıntıları modülü</span><span class="sxs-lookup"><span data-stu-id="3c476-161">Order details module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="3c476-162">Hediye kartı modülü</span><span class="sxs-lookup"><span data-stu-id="3c476-162">Gift card module</span></span>](add-giftcard.md)

[<span data-ttu-id="3c476-163">Adyen için Dynamics 365 Ödeme Bağlayıcısı</span><span class="sxs-lookup"><span data-stu-id="3c476-163">Dynamics 365 Payment Connector for Adyen</span></span>](dev-itpro/adyen-connector.md)

[<span data-ttu-id="3c476-164">Adyen bağlayıcısı kullanan Güçlü Müşteri Kimlik Doğrulaması</span><span class="sxs-lookup"><span data-stu-id="3c476-164">Strong Customer Authentication using Adyen</span></span>](adyen_redirect.md)
