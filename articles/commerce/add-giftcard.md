---
title: Hediye kartı modülü
description: Bu konu hediye kartı modüllerini kapsamaktadır ve Microsoft Dynamics 365 Commerce'ın site sayfalarına nasıl ekleneceğini açıklamaktadır.
author: anupamar-ms
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: a4e4e06ab7032d68fcd36a8e80bc714ebaaac821
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/31/2021
ms.locfileid: "5797683"
---
# <a name="gift-card-module"></a><span data-ttu-id="b2669-103">Hediye kartı modülü</span><span class="sxs-lookup"><span data-stu-id="b2669-103">Gift card module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="b2669-104">Bu konu hediye kartı modüllerini kapsamaktadır ve Microsoft Dynamics 365 Commerce'ın site sayfalarına nasıl ekleneceğini açıklamaktadır.</span><span class="sxs-lookup"><span data-stu-id="b2669-104">This topic covers gift card modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="b2669-105">E-ticaret hareketlerinde kullanılan genel bir ödeme biçimi olarak hediye kartı kabul etmek üzere ödeme modülünde bir hediye kartı modülü kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="b2669-105">Gift card modules can be used in checkout modules to accept gift cards, a common form of payment used for e-Commerce transactions.</span></span> <span data-ttu-id="b2669-106">Hediye kartı modülü Dynamics 365, SVS ve Givex hediye kartlarını destekler.</span><span class="sxs-lookup"><span data-stu-id="b2669-106">The gift card module supports Dynamics 365, SVS, and Givex gift cards.</span></span> <span data-ttu-id="b2669-107">SVS ve Givex hediye kartları, Adyen ödeme sağlayıcısı aracılığıyla kullanılır.</span><span class="sxs-lookup"><span data-stu-id="b2669-107">SVS and Givex gift cards are redeemed via the Adyen payment provider.</span></span> <span data-ttu-id="b2669-108">SVS ve Givex gibi harici hediye kartları desteği hakkında daha fazla bilgi için bkz. [Harici hediye kartları için destek](./dev-itpro/gift-card.md).</span><span class="sxs-lookup"><span data-stu-id="b2669-108">For more information about support for external gift cards such as SVS and Givex, see [Support for external gift cards](./dev-itpro/gift-card.md).</span></span>

> [!NOTE]
> <span data-ttu-id="b2669-109">Dynamics 365 Commerce 10.0.11 sürümünde ödeme akışı sırasında SVS ve Givex hediye kartlarının kullanım desteği bulunur.</span><span class="sxs-lookup"><span data-stu-id="b2669-109">Support for redeeming SVS and Givex gift cards during checkout flow is available in the Dynamics 365 Commerce 10.0.11 release.</span></span> 

<span data-ttu-id="b2669-110">İki hediye kartı modülü mevcuttur:</span><span class="sxs-lookup"><span data-stu-id="b2669-110">There are two gift card modules available:</span></span>

- <span data-ttu-id="b2669-111">**Hediye kartı**: Bu modül, geçerli bir ödeme şekli olarak bir hediye kartından yararlanmak için ödeme sayfasında kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="b2669-111">**Gift card** - This module can be used on a checkout page to redeem a gift card as tender.</span></span> 
- <span data-ttu-id="b2669-112">**Hediye kartı bakiyesi denetimi**: Bu modül herhangi bir sayfada, bir hediye kartındaki bakiyeyi denetlemek için kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="b2669-112">**Gift card balance check** - This module can be used on any page to check the balance on a gift card.</span></span> <span data-ttu-id="b2669-113">Bu modül Commerce 10.0.14 sürümü ve sonrasında bulunur.</span><span class="sxs-lookup"><span data-stu-id="b2669-113">This module is available in Commerce release 10.0.14 and later.</span></span>

> [!NOTE]
> <span data-ttu-id="b2669-114">Hediye kartı bakiyesi denetleme modülü desteği Dynamics 365 Commerce 10.0.14 sürümünde mevcuttur.</span><span class="sxs-lookup"><span data-stu-id="b2669-114">Support for the gift card balance check module is available in the Dynamics 365 Commerce 10.0.14 release.</span></span>

<span data-ttu-id="b2669-115">Aşağıdaki resimde ödeme sayfasında kullanılan bir hediye kartı modülü örneği gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="b2669-115">The following image shows an example of a gift card module on a checkout page.</span></span>

![Hediye kartı modülü örneği](./media/ecommerce-giftcard.PNG)

## <a name="module-properties"></a><span data-ttu-id="b2669-117">Modül özellikleri</span><span class="sxs-lookup"><span data-stu-id="b2669-117">Module properties</span></span>

- <span data-ttu-id="b2669-118">**Ek alanları göster** - Bu özellik, her zaman varsayılan olarak görüntülenen hediye kartı numarasına ek olarak, hediye kartları için hangi alanların görüntüleneceğini tanımlar.</span><span class="sxs-lookup"><span data-stu-id="b2669-118">**Show additional fields** - This property defines what fields should be displayed for gift cards in addition to the gift card number, which is always displayed by default.</span></span> <span data-ttu-id="b2669-119">Örneğin, bazı hediye kartları bir kişisel kimlik numarası (PIN) görüntülemeyi ve başka hediye kartları PIN ve son kullanma tarihini görüntülemeyi destekler.</span><span class="sxs-lookup"><span data-stu-id="b2669-119">For example, some gift cards support displaying a personal identification number (PIN), and others support displaying a PIN and expiration date.</span></span> <span data-ttu-id="b2669-120">Alternatif olarak, bu özellik yalnızca hediye kartı numarasını görüntüleyebilen ve ek alanlar içermeyen "Hiçbiri" seçeneğine ayarlanabilir.</span><span class="sxs-lookup"><span data-stu-id="b2669-120">Alternatively, this property could be set to "None", which would only display the gift card number and no additional fields.</span></span>

<span data-ttu-id="b2669-121">Desteklenen değerler:</span><span class="sxs-lookup"><span data-stu-id="b2669-121">Supported values:</span></span>
-   <span data-ttu-id="b2669-122">PIN</span><span class="sxs-lookup"><span data-stu-id="b2669-122">PIN</span></span>
-   <span data-ttu-id="b2669-123">Son kullanma tarihi</span><span class="sxs-lookup"><span data-stu-id="b2669-123">Expiration date</span></span>
-   <span data-ttu-id="b2669-124">PIN ve son kullanma tarihi</span><span class="sxs-lookup"><span data-stu-id="b2669-124">PIN and expiration date</span></span> 
-   <span data-ttu-id="b2669-125">Hiçbiri</span><span class="sxs-lookup"><span data-stu-id="b2669-125">None</span></span>

## <a name="site-settings-for-gift-card-modules"></a><span data-ttu-id="b2669-126">Hediye kartı modülleri için site ayarları</span><span class="sxs-lookup"><span data-stu-id="b2669-126">Site settings for gift card modules</span></span>

<span data-ttu-id="b2669-127">Commerce site oluşturucuda **Site Ayarları \> Uzantılar** altında, **Desteklenen hediye kartı türü** adında bir hediye kartı modülü ayarı vardır.</span><span class="sxs-lookup"><span data-stu-id="b2669-127">In Commerce site builder under **Site Settings \> Extensions**, there is a gift card module setting called **Supported gift card type**.</span></span> <span data-ttu-id="b2669-128">Bu ayar üç değeri destekler:</span><span class="sxs-lookup"><span data-stu-id="b2669-128">This setting supports three values:</span></span>
- <span data-ttu-id="b2669-129">**Dynamics 365 hediye kartı** - Bu ayar uygulandığında, hediye kartı modülü yalnızca Dynamics 365 hediye kartlarının kullanılmasına izin verir.</span><span class="sxs-lookup"><span data-stu-id="b2669-129">**Dynamics 365 gift card** - When this setting is applied, the gift card module only allows the redemption of Dynamics 365 gift cards.</span></span> <span data-ttu-id="b2669-130">Bu ayar yalnızca e-Ticaret sitesindeki oturum açmış kullanıcılar için desteklenir.</span><span class="sxs-lookup"><span data-stu-id="b2669-130">This setting is only supported for signed-in users on the e-Commerce site.</span></span>
- <span data-ttu-id="b2669-131">**SVS ve Givex hediye kartları** - Bu ayar uygulandığında, hediye kartı modülü yalnızca Givex ve SVS hediye kartlarının kullanılmasına izin verir.</span><span class="sxs-lookup"><span data-stu-id="b2669-131">**SVS and Givex gift cards** - When this setting is applied, the gift card module only allows the redemption of Givex and SVS gift cards.</span></span> <span data-ttu-id="b2669-132">Bu ayar e-Ticaret sitesindeki oturum açmış ve anonim kullanıcılar için desteklenir.</span><span class="sxs-lookup"><span data-stu-id="b2669-132">This setting is supported for signed-in and anonymous users on the e-Commerce site.</span></span>
- <span data-ttu-id="b2669-133">**Dynamics 365, SVS ve Givex hediye kartları** - Bu ayar uygulandığında, hediye kartı modülü Dynamics 365, Givex ve SVS hediye kartlarının kullanılmasına izin verir.</span><span class="sxs-lookup"><span data-stu-id="b2669-133">**Dynamics 365, SVS, and Givex gift cards** - When this setting is applied, the gift card module allows the redemption of Dynamics 365, Givex, and SVS gift cards.</span></span> <span data-ttu-id="b2669-134">Bu ayar yalnızca e-Ticaret sitesindeki oturum açmış kullanıcılar için desteklenir.</span><span class="sxs-lookup"><span data-stu-id="b2669-134">This setting is only supported for signed-in users on the e-Commerce site.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="b2669-135">Bu ayarlar Dynamics 365 Commerce 10.0.11 sürümünde bulunur ve yalnızca SVS veya Givex hediye kartları için desteğe gereksinim duyarsanız gereklidir.</span><span class="sxs-lookup"><span data-stu-id="b2669-135">These settings are available in the Dynamics 365 Commerce 10.0.11 release and are required only if you need support for SVS or Givex gift cards.</span></span> <span data-ttu-id="b2669-136">Dynamics 365 Commerce'nin eski sürümlerinden birini güncelleştiriyorsanız, appSettings. json dosyasını el ile güncelleştirmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="b2669-136">If you are updating from an older version of Dynamics 365 Commerce, you must manually update the appsettings.json file.</span></span> <span data-ttu-id="b2669-137">AppSettings.json dosyasını güncelleştirme yönergeleri için bkz. [SDK ve modül kitaplığı güncelleştirmeleri](e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file).</span><span class="sxs-lookup"><span data-stu-id="b2669-137">For instructions on updating the appsettings.json file, see [SDK and module library updates](e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file).</span></span> 

## <a name="add-a-gift-card-module-to-a-page"></a><span data-ttu-id="b2669-138">Sayfaya hediye kartı modülü ekleme</span><span class="sxs-lookup"><span data-stu-id="b2669-138">Add a gift card module to a page</span></span>

<span data-ttu-id="b2669-139">Bir ödeme sayfasına hediye kartı modülü ekleme ve gerekli özellikleri ayarlama yönergeleri için bkz. [Ödeme modülü](add-checkout-module.md).</span><span class="sxs-lookup"><span data-stu-id="b2669-139">For instructions on how to add a gift card module to a checkout page and set the required properties, see [Checkout module](add-checkout-module.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="b2669-140">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="b2669-140">Additional resources</span></span>

[<span data-ttu-id="b2669-141">Sepet modülü</span><span class="sxs-lookup"><span data-stu-id="b2669-141">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="b2669-142">Sepet simgesi modülü</span><span class="sxs-lookup"><span data-stu-id="b2669-142">Cart icon module</span></span>](cart-icon-module.md)

[<span data-ttu-id="b2669-143">Ödeme modülü</span><span class="sxs-lookup"><span data-stu-id="b2669-143">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="b2669-144">Ödeme modülü</span><span class="sxs-lookup"><span data-stu-id="b2669-144">Payment module</span></span>](payment-module.md)

[<span data-ttu-id="b2669-145">Sevkiyat adresi modülü</span><span class="sxs-lookup"><span data-stu-id="b2669-145">Shipping address module</span></span>](ship-address-module.md)

[<span data-ttu-id="b2669-146">Teslimat seçenekleri modülü</span><span class="sxs-lookup"><span data-stu-id="b2669-146">Delivery options module</span></span>](delivery-options-module.md)

[<span data-ttu-id="b2669-147">Malzeme çekme bilgileri modülü</span><span class="sxs-lookup"><span data-stu-id="b2669-147">Pickup information module</span></span>](pickup-info-module.md)

[<span data-ttu-id="b2669-148">Sipariş ayrıntıları modülü</span><span class="sxs-lookup"><span data-stu-id="b2669-148">Order details module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="b2669-149">Harici hediye kartları için destek</span><span class="sxs-lookup"><span data-stu-id="b2669-149">Support for external gift cards</span></span>](./dev-itpro/gift-card.md)

[<span data-ttu-id="b2669-150">SDK ve modül kitaplığı güncelleştirmeleri</span><span class="sxs-lookup"><span data-stu-id="b2669-150">SDK and module library updates</span></span>](e-commerce-extensibility/sdk-updates.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]