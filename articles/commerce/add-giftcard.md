---
title: Hediye kartı modülü
description: Bu konu hediye kartı modüllerini kapsamaktadır ve Microsoft Dynamics 365 Commerce'ın site sayfalarına nasıl ekleneceğini açıklamaktadır.
author: anupamar-ms
manager: annbe
ms.date: 08/31/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 4cc947b9d6f3cfa51bce2155170c49e9529d0f7d
ms.sourcegitcommit: 420b9e538f706178f8e1f2786e02f4f400bf2336
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/02/2020
ms.locfileid: "3761093"
---
# <a name="gift-card-module"></a><span data-ttu-id="bdbcb-103">Hediye kartı modülü</span><span class="sxs-lookup"><span data-stu-id="bdbcb-103">Gift card module</span></span>

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

<span data-ttu-id="bdbcb-104">Bu konu hediye kartı modüllerini kapsamaktadır ve Microsoft Dynamics 365 Commerce'ın site sayfalarına nasıl ekleneceğini açıklamaktadır.</span><span class="sxs-lookup"><span data-stu-id="bdbcb-104">This topic covers gift card modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="bdbcb-105">Genel bakış</span><span class="sxs-lookup"><span data-stu-id="bdbcb-105">Overview</span></span>

<span data-ttu-id="bdbcb-106">E-ticaret hareketlerinde kullanılan genel bir ödeme biçimi olarak hediye kartı kabul etmek üzere ödeme modülünde bir hediye kartı modülü kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="bdbcb-106">Gift card modules can be used in checkout modules to accept gift cards, a common form of payment used for e-Commerce transactions.</span></span> <span data-ttu-id="bdbcb-107">Hediye kartı modülü Dynamics 365, SVS ve Givex hediye kartlarını destekler.</span><span class="sxs-lookup"><span data-stu-id="bdbcb-107">The gift card module supports Dynamics 365, SVS, and Givex gift cards.</span></span> <span data-ttu-id="bdbcb-108">SVS ve Givex hediye kartları, Adyen ödeme sağlayıcısı aracılığıyla kullanılır.</span><span class="sxs-lookup"><span data-stu-id="bdbcb-108">SVS and Givex gift cards are redeemed via the Adyen payment provider.</span></span> <span data-ttu-id="bdbcb-109">SVS ve Givex gibi harici hediye kartları desteği hakkında daha fazla bilgi için bkz. [Harici hediye kartları için destek](./dev-itpro/gift-card.md).</span><span class="sxs-lookup"><span data-stu-id="bdbcb-109">For more information about support for external gift cards such as SVS and Givex, see [Support for external gift cards](./dev-itpro/gift-card.md).</span></span>

<span data-ttu-id="bdbcb-110">İki hediye kartı modülü mevcuttur:</span><span class="sxs-lookup"><span data-stu-id="bdbcb-110">There are two gift card modules available:</span></span>

- <span data-ttu-id="bdbcb-111">**Hediye kartı**: Bu modül, geçerli bir ödeme şekli olarak bir hediye kartından yararlanmak için ödeme sayfasında kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="bdbcb-111">**Gift card** - This module can be used on a checkout page to redeem a gift card as tender.</span></span> 
- <span data-ttu-id="bdbcb-112">**Hediye kartı bakiyesi denetimi**: Bu modül herhangi bir sayfada, bir hediye kartındaki bakiyeyi denetlemek için kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="bdbcb-112">**Gift card balance check** - This module can be used on any page to check the balance on a gift card.</span></span> <span data-ttu-id="bdbcb-113">Bu modül Commerce 10.0.14 sürümü ve sonrasında bulunur.</span><span class="sxs-lookup"><span data-stu-id="bdbcb-113">This module is available in Commerce release 10.0.14 and later.</span></span>

<span data-ttu-id="bdbcb-114">Aşağıdaki resimde ödeme sayfasında kullanılan bir hediye kartı modülü örneği gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="bdbcb-114">The following image shows an example of a gift card module on a checkout page.</span></span>

![Hediye kartı modülü örneği](./media/ecommerce-giftcard.PNG)

## <a name="module-properties"></a><span data-ttu-id="bdbcb-116">Modül özellikleri</span><span class="sxs-lookup"><span data-stu-id="bdbcb-116">Module properties</span></span>

- <span data-ttu-id="bdbcb-117">**Ek alanları göster** - Bu özellik, her zaman varsayılan olarak görüntülenen hediye kartı numarasına ek olarak, hediye kartları için hangi alanların görüntüleneceğini tanımlar.</span><span class="sxs-lookup"><span data-stu-id="bdbcb-117">**Show additional fields** - This property defines what fields should be displayed for gift cards in addition to the gift card number, which is always displayed by default.</span></span> <span data-ttu-id="bdbcb-118">Örneğin, bazı hediye kartları bir kişisel kimlik numarası (PIN) görüntülemeyi ve başka hediye kartları PIN ve son kullanma tarihini görüntülemeyi destekler.</span><span class="sxs-lookup"><span data-stu-id="bdbcb-118">For example, some gift cards support displaying a personal identification number (PIN), and others support displaying a PIN and expiration date.</span></span> <span data-ttu-id="bdbcb-119">Alternatif olarak, bu özellik yalnızca hediye kartı numarasını görüntüleyebilen ve ek alanlar içermeyen "Hiçbiri" seçeneğine ayarlanabilir.</span><span class="sxs-lookup"><span data-stu-id="bdbcb-119">Alternatively, this property could be set to "None", which would only display the gift card number and no additional fields.</span></span>

<span data-ttu-id="bdbcb-120">Desteklenen değerler:</span><span class="sxs-lookup"><span data-stu-id="bdbcb-120">Supported values:</span></span>
-   <span data-ttu-id="bdbcb-121">PIN</span><span class="sxs-lookup"><span data-stu-id="bdbcb-121">PIN</span></span>
-   <span data-ttu-id="bdbcb-122">Son kullanma tarihi</span><span class="sxs-lookup"><span data-stu-id="bdbcb-122">Expiration date</span></span>
-   <span data-ttu-id="bdbcb-123">PIN ve son kullanma tarihi</span><span class="sxs-lookup"><span data-stu-id="bdbcb-123">PIN and expiration date</span></span> 
-   <span data-ttu-id="bdbcb-124">Hiçbiri</span><span class="sxs-lookup"><span data-stu-id="bdbcb-124">None</span></span>

## <a name="site-settings-for-gift-card-modules"></a><span data-ttu-id="bdbcb-125">Hediye kartı modülleri için site ayarları</span><span class="sxs-lookup"><span data-stu-id="bdbcb-125">Site settings for gift card modules</span></span>

<span data-ttu-id="bdbcb-126">Commerce site oluşturucuda **Site Ayarları \> Uzantılar**altında, **Desteklenen hediye kartı türü** adında bir hediye kartı modülü ayarı vardır.</span><span class="sxs-lookup"><span data-stu-id="bdbcb-126">In Commerce site builder under **Site Settings \> Extensions**, there is a gift card module setting called **Supported gift card type**.</span></span> <span data-ttu-id="bdbcb-127">Bu ayar üç değeri destekler:</span><span class="sxs-lookup"><span data-stu-id="bdbcb-127">This setting supports three values:</span></span>
- <span data-ttu-id="bdbcb-128">**Dynamics 365 hediye kartı** - Bu ayar uygulandığında, hediye kartı modülü yalnızca Dynamics 365 hediye kartlarının kullanılmasına izin verir.</span><span class="sxs-lookup"><span data-stu-id="bdbcb-128">**Dynamics 365 gift card** - When this setting is applied, the gift card module only allows the redemption of Dynamics 365 gift cards.</span></span> <span data-ttu-id="bdbcb-129">Bu ayar yalnızca e-Ticaret sitesindeki oturum açmış kullanıcılar için desteklenir.</span><span class="sxs-lookup"><span data-stu-id="bdbcb-129">This setting is only supported for signed-in users on the e-Commerce site.</span></span>
- <span data-ttu-id="bdbcb-130">**SVS ve Givex hediye kartları** - Bu ayar uygulandığında, hediye kartı modülü yalnızca Givex ve SVS hediye kartlarının kullanılmasına izin verir.</span><span class="sxs-lookup"><span data-stu-id="bdbcb-130">**SVS and Givex gift cards** - When this setting is applied, the gift card module only allows the redemption of Givex and SVS gift cards.</span></span> <span data-ttu-id="bdbcb-131">Bu ayar e-Ticaret sitesindeki oturum açmış ve anonim kullanıcılar için desteklenir.</span><span class="sxs-lookup"><span data-stu-id="bdbcb-131">This setting is supported for signed-in and anonymous users on the e-Commerce site.</span></span>
- <span data-ttu-id="bdbcb-132">**Dynamics 365, SVS ve Givex hediye kartları** - Bu ayar uygulandığında, hediye kartı modülü Dynamics 365, Givex ve SVS hediye kartlarının kullanılmasına izin verir.</span><span class="sxs-lookup"><span data-stu-id="bdbcb-132">**Dynamics 365, SVS, and Givex gift cards** - When this setting is applied, the gift card module allows the redemption of Dynamics 365, Givex, and SVS gift cards.</span></span> <span data-ttu-id="bdbcb-133">Bu ayar yalnızca e-Ticaret sitesindeki oturum açmış kullanıcılar için desteklenir.</span><span class="sxs-lookup"><span data-stu-id="bdbcb-133">This setting is only supported for signed-in users on the e-Commerce site.</span></span>

## <a name="add-a-gift-card-module-to-a-page"></a><span data-ttu-id="bdbcb-134">Sayfaya hediye kartı modülü ekleme</span><span class="sxs-lookup"><span data-stu-id="bdbcb-134">Add a gift card module to a page</span></span>

<span data-ttu-id="bdbcb-135">Bir ödeme sayfasına hediye kartı modülü ekleme ve gerekli özellikleri ayarlama yönergeleri için bkz. [Ödeme modülü](add-checkout-module.md).</span><span class="sxs-lookup"><span data-stu-id="bdbcb-135">For instructions on how to add a gift card module to a checkout page and set the required properties, see [Checkout module](add-checkout-module.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="bdbcb-136">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="bdbcb-136">Additional resources</span></span>

[<span data-ttu-id="bdbcb-137">Sepet modülü</span><span class="sxs-lookup"><span data-stu-id="bdbcb-137">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="bdbcb-138">Sepet simgesi modülü</span><span class="sxs-lookup"><span data-stu-id="bdbcb-138">Cart icon module</span></span>](cart-icon-module.md)

[<span data-ttu-id="bdbcb-139">Ödeme modülü</span><span class="sxs-lookup"><span data-stu-id="bdbcb-139">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="bdbcb-140">Ödeme modülü</span><span class="sxs-lookup"><span data-stu-id="bdbcb-140">Payment module</span></span>](payment-module.md)

[<span data-ttu-id="bdbcb-141">Sevkiyat adresi modülü</span><span class="sxs-lookup"><span data-stu-id="bdbcb-141">Shipping address module</span></span>](ship-address-module.md)

[<span data-ttu-id="bdbcb-142">Teslimat seçenekleri modülü</span><span class="sxs-lookup"><span data-stu-id="bdbcb-142">Delivery options module</span></span>](delivery-options-module.md)

[<span data-ttu-id="bdbcb-143">Sipariş ayrıntıları modülü</span><span class="sxs-lookup"><span data-stu-id="bdbcb-143">Order details module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="bdbcb-144">Harici hediye kartları için destek</span><span class="sxs-lookup"><span data-stu-id="bdbcb-144">Support for external gift cards</span></span>](./dev-itpro/gift-card.md)
