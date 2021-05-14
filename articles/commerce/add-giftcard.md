---
title: Hediye kartı modülü
description: Bu konu hediye kartı modüllerini kapsamaktadır ve Microsoft Dynamics 365 Commerce'ın site sayfalarına nasıl ekleneceğini açıklamaktadır.
author: anupamar-ms
ms.date: 04/29/2021
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
ms.openlocfilehash: 8db7e597241f1fd552f6b960c2b57b0ba83da949
ms.sourcegitcommit: efde05c758b2e02960760d875569d780d77d5550
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/29/2021
ms.locfileid: "5962775"
---
# <a name="gift-card-module"></a><span data-ttu-id="9b3c9-103">Hediye kartı modülü</span><span class="sxs-lookup"><span data-stu-id="9b3c9-103">Gift card module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="9b3c9-104">Bu konu hediye kartı modüllerini kapsamaktadır ve Microsoft Dynamics 365 Commerce'ın site sayfalarına nasıl ekleneceğini açıklamaktadır.</span><span class="sxs-lookup"><span data-stu-id="9b3c9-104">This topic covers gift card modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="9b3c9-105">E-ticaret hareketlerinde kullanılan genel bir ödeme biçimi olarak hediye kartı kabul etmek üzere ödeme modülünde bir hediye kartı modülü kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="9b3c9-105">Gift card modules can be used in checkout modules to accept gift cards, a common form of payment used for e-Commerce transactions.</span></span> <span data-ttu-id="9b3c9-106">Hediye kartı modülü Dynamics 365, SVS ve Givex hediye kartlarını destekler.</span><span class="sxs-lookup"><span data-stu-id="9b3c9-106">The gift card module supports Dynamics 365, SVS, and Givex gift cards.</span></span> <span data-ttu-id="9b3c9-107">SVS ve Givex hediye kartları, Adyen ödeme sağlayıcısı aracılığıyla kullanılır.</span><span class="sxs-lookup"><span data-stu-id="9b3c9-107">SVS and Givex gift cards are redeemed via the Adyen payment provider.</span></span> <span data-ttu-id="9b3c9-108">SVS ve Givex gibi harici hediye kartları desteği hakkında daha fazla bilgi için bkz. [Harici hediye kartları için destek](./dev-itpro/gift-card.md).</span><span class="sxs-lookup"><span data-stu-id="9b3c9-108">For more information about support for external gift cards such as SVS and Givex, see [Support for external gift cards](./dev-itpro/gift-card.md).</span></span>

> [!NOTE]
> <span data-ttu-id="9b3c9-109">Dynamics 365 Commerce 10.0.11 sürümünde ödeme akışı sırasında SVS ve Givex hediye kartlarının kullanım desteği bulunur.</span><span class="sxs-lookup"><span data-stu-id="9b3c9-109">Support for redeeming SVS and Givex gift cards during checkout flow is available in the Dynamics 365 Commerce 10.0.11 release.</span></span> 

<span data-ttu-id="9b3c9-110">İki hediye kartı modülü mevcuttur:</span><span class="sxs-lookup"><span data-stu-id="9b3c9-110">There are two gift card modules available:</span></span>

- <span data-ttu-id="9b3c9-111">**Hediye kartı** – Bu modül, geçerli bir ödeme şekli olarak bir hediye kartından yararlanmak için ödeme sayfasında kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="9b3c9-111">**Gift card** – This module can be used on a checkout page to redeem a gift card as tender.</span></span> 
- <span data-ttu-id="9b3c9-112">**Hediye kartı bakiyesi denetimi** – Bu modül herhangi bir sayfada, bir hediye kartındaki bakiyeyi denetlemek için kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="9b3c9-112">**Gift card balance check** – This module can be used on any page to check the balance on a gift card.</span></span> <span data-ttu-id="9b3c9-113">Bu modül Commerce 10.0.14 sürümü ve sonrasında bulunur.</span><span class="sxs-lookup"><span data-stu-id="9b3c9-113">This module is available in Commerce release 10.0.14 and later.</span></span>

> [!NOTE]
> <span data-ttu-id="9b3c9-114">Hediye kartı bakiyesi denetleme modülü desteği Dynamics 365 Commerce 10.0.14 sürümünde mevcuttur.</span><span class="sxs-lookup"><span data-stu-id="9b3c9-114">Support for the gift card balance check module is available in the Dynamics 365 Commerce 10.0.14 release.</span></span>

<span data-ttu-id="9b3c9-115">Aşağıdaki resimde ödeme sayfasında kullanılan bir hediye kartı modülü örneği gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="9b3c9-115">The following image shows an example of a gift card module on a checkout page.</span></span>

![Hediye kartı modülü örneği](./media/ecommerce-giftcard.PNG)

## <a name="module-properties"></a><span data-ttu-id="9b3c9-117">Modül özellikleri</span><span class="sxs-lookup"><span data-stu-id="9b3c9-117">Module properties</span></span>

- <span data-ttu-id="9b3c9-118">**Ek alanları göster** – Bu özellik, her zaman varsayılan olarak görüntülenen hediye kartı numarasına ek olarak, hediye kartları için hangi alanların görüntüleneceğini tanımlar.</span><span class="sxs-lookup"><span data-stu-id="9b3c9-118">**Show additional fields** – This property defines what fields should be displayed for gift cards in addition to the gift card number, which is always displayed by default.</span></span> <span data-ttu-id="9b3c9-119">Örneğin, bazı hediye kartları bir kişisel kimlik numarası (PIN) görüntülemeyi ve başka hediye kartları PIN ve son kullanma tarihini görüntülemeyi destekler.</span><span class="sxs-lookup"><span data-stu-id="9b3c9-119">For example, some gift cards support displaying a personal identification number (PIN), and others support displaying a PIN and expiration date.</span></span> <span data-ttu-id="9b3c9-120">Alternatif olarak, bu özellik yalnızca hediye kartı numarasını görüntüleyebilen ve ek alanlar içermeyen "Hiçbiri" seçeneğine ayarlanabilir.</span><span class="sxs-lookup"><span data-stu-id="9b3c9-120">Alternatively, this property could be set to "None", which would only display the gift card number and no additional fields.</span></span>

<span data-ttu-id="9b3c9-121">Desteklenen değerler:</span><span class="sxs-lookup"><span data-stu-id="9b3c9-121">Supported values:</span></span>
-   <span data-ttu-id="9b3c9-122">PIN</span><span class="sxs-lookup"><span data-stu-id="9b3c9-122">PIN</span></span>
-   <span data-ttu-id="9b3c9-123">Son kullanma tarihi</span><span class="sxs-lookup"><span data-stu-id="9b3c9-123">Expiration date</span></span>
-   <span data-ttu-id="9b3c9-124">PIN ve son kullanma tarihi</span><span class="sxs-lookup"><span data-stu-id="9b3c9-124">PIN and expiration date</span></span> 
-   <span data-ttu-id="9b3c9-125">Hiçbiri</span><span class="sxs-lookup"><span data-stu-id="9b3c9-125">None</span></span>

## <a name="site-settings-for-gift-card-modules"></a><span data-ttu-id="9b3c9-126">Hediye kartı modülleri için site ayarları</span><span class="sxs-lookup"><span data-stu-id="9b3c9-126">Site settings for gift card modules</span></span>

<span data-ttu-id="9b3c9-127">Commerce site oluşturucuda **Site Ayarları \> Uzantılar** altında, **Desteklenen hediye kartı türü** adında bir hediye kartı modülü ayarı vardır.</span><span class="sxs-lookup"><span data-stu-id="9b3c9-127">In Commerce site builder under **Site Settings \> Extensions**, there is a gift card module setting called **Supported gift card type**.</span></span> <span data-ttu-id="9b3c9-128">Bu ayar üç değeri destekler:</span><span class="sxs-lookup"><span data-stu-id="9b3c9-128">This setting supports three values:</span></span>
- <span data-ttu-id="9b3c9-129">**Dynamics 365 hediye kartı** – Bu ayar uygulandığında, hediye kartı modülü yalnızca Dynamics 365 hediye kartlarının kullanılmasına izin verir.</span><span class="sxs-lookup"><span data-stu-id="9b3c9-129">**Dynamics 365 gift card** – When this setting is applied, the gift card module only allows the redemption of Dynamics 365 gift cards.</span></span> <span data-ttu-id="9b3c9-130">Bu ayar yalnızca e-Ticaret sitesindeki oturum açmış kullanıcılar için desteklenir.</span><span class="sxs-lookup"><span data-stu-id="9b3c9-130">This setting is only supported for signed-in users on the e-Commerce site.</span></span>
- <span data-ttu-id="9b3c9-131">**SVS ve Givex hediye kartları** – Bu ayar uygulandığında, hediye kartı modülü yalnızca Givex ve SVS hediye kartlarının kullanılmasına izin verir.</span><span class="sxs-lookup"><span data-stu-id="9b3c9-131">**SVS and Givex gift cards** – When this setting is applied, the gift card module only allows the redemption of Givex and SVS gift cards.</span></span> <span data-ttu-id="9b3c9-132">Bu ayar e-Ticaret sitesindeki oturum açmış ve anonim kullanıcılar için desteklenir.</span><span class="sxs-lookup"><span data-stu-id="9b3c9-132">This setting is supported for signed-in and anonymous users on the e-Commerce site.</span></span>
- <span data-ttu-id="9b3c9-133">**Dynamics 365, SVS ve Givex hediye kartları** – Bu ayar uygulandığında, hediye kartı modülü Dynamics 365, Givex ve SVS hediye kartlarının kullanılmasına izin verir.</span><span class="sxs-lookup"><span data-stu-id="9b3c9-133">**Dynamics 365, SVS, and Givex gift cards** – When this setting is applied, the gift card module allows the redemption of Dynamics 365, Givex, and SVS gift cards.</span></span> <span data-ttu-id="9b3c9-134">Bu ayar yalnızca e-Ticaret sitesindeki oturum açmış kullanıcılar için desteklenir.</span><span class="sxs-lookup"><span data-stu-id="9b3c9-134">This setting is only supported for signed-in users on the e-Commerce site.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="9b3c9-135">Bu ayarlar Dynamics 365 Commerce 10.0.11 sürümünde bulunur ve yalnızca SVS veya Givex hediye kartları için desteğe gereksinim duyarsanız gereklidir.</span><span class="sxs-lookup"><span data-stu-id="9b3c9-135">These settings are available in the Dynamics 365 Commerce 10.0.11 release and are required only if you need support for SVS or Givex gift cards.</span></span> <span data-ttu-id="9b3c9-136">Dynamics 365 Commerce'nin eski sürümlerinden birini güncelleştiriyorsanız, appSettings. json dosyasını el ile güncelleştirmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="9b3c9-136">If you are updating from an older version of Dynamics 365 Commerce, you must manually update the appsettings.json file.</span></span> <span data-ttu-id="9b3c9-137">AppSettings.json dosyasını güncelleştirme yönergeleri için bkz. [SDK ve modül kitaplığı güncelleştirmeleri](e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file).</span><span class="sxs-lookup"><span data-stu-id="9b3c9-137">For instructions on updating the appsettings.json file, see [SDK and module library updates](e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file).</span></span> 

## <a name="extend-internal-gift-cards-for-use-in-e-commerce-storefronts"></a><span data-ttu-id="9b3c9-138">E-ticaret mağazasında kullanmak üzere dahili hediye kartlarını uzatın</span><span class="sxs-lookup"><span data-stu-id="9b3c9-138">Extend internal gift cards for use in e-commerce storefronts</span></span>

<span data-ttu-id="9b3c9-139">Varsayılan olarak, dahili hediye kartları e-ticaret mağazalarında kullanım için optimize edilmez.</span><span class="sxs-lookup"><span data-stu-id="9b3c9-139">By default, internal gift cards aren't optimized for use in e-commerce storefronts.</span></span> <span data-ttu-id="9b3c9-140">Bu nedenle, dahili hediye kartlarının ödeme için kullanılmasına izin vermeden önce, onları daha güvenli hale getirmek amacıyla kartları uzantılarla yapılandırmalısınız.</span><span class="sxs-lookup"><span data-stu-id="9b3c9-140">Therefore, before you allow internal gift cards to be used for payment, you should configure them with extensions that help make them more secure.</span></span> <span data-ttu-id="9b3c9-141">Dahili hediye kartlarının üretimde kullanılmasına izin vermeden önce, genişletmeniz gereken hediye kartı alanları şunlardır:</span><span class="sxs-lookup"><span data-stu-id="9b3c9-141">Here are the gift card areas that you should extend before you allow internal gift cards to be used in production:</span></span>

- <span data-ttu-id="9b3c9-142">**Hediye kartı numarası** – Numara serileri, dahili hediye kartları için hediye kartı numaraları oluşturmak amacıyla kullanılır.</span><span class="sxs-lookup"><span data-stu-id="9b3c9-142">**Gift card number** – Number sequences are used to generate gift card numbers for internal gift cards.</span></span> <span data-ttu-id="9b3c9-143">Numara serileri kolayca tahmin edilebileceği için, hediye kartı numaralarının oluşumunu, verilen hediye kartı numaraları için rasgele, kriptografik olarak güvenli dizeler kullanılacak şekilde genişletmelisiniz.</span><span class="sxs-lookup"><span data-stu-id="9b3c9-143">Because number sequences can easily be predicted, you should extend the generation of gift card numbers so that random, cryptographically secure strings are used for the gift card numbers that are issued.</span></span>
- <span data-ttu-id="9b3c9-144">**GetBalance** – **GetBalance** API, hediye kartı bakiyelerini aramak için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="9b3c9-144">**GetBalance** – The **GetBalance** API is used to look up gift card balances.</span></span> <span data-ttu-id="9b3c9-145">Varsayılan olarak, bu API herkesin kullanımına açıktır.</span><span class="sxs-lookup"><span data-stu-id="9b3c9-145">By default, this API public.</span></span> <span data-ttu-id="9b3c9-146">Hediye kartı bakiyelerini aramak için PIN gerekli değilse deneme yanılma saldırılarının **GetBalance** API'yi kullanarak bakiyeleri olan hediye kartı numaralarını arama riski olur.</span><span class="sxs-lookup"><span data-stu-id="9b3c9-146">If a PIN isn't required to look up gift card balances, there is a risk that brute force attacks could use the **GetBalance** API to try to look up gift card numbers that have balances.</span></span> <span data-ttu-id="9b3c9-147">Dahili hediye kartları ve API azaltma için PIN gereksinimlerinin her ikisini de uygulayarak, bu riski hafifletebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="9b3c9-147">By implementing both PIN requirements for internal gift cards and API throttling, you can help mitigate the risk.</span></span>
- <span data-ttu-id="9b3c9-148">**PIN** – Varsayılan olarak, dahili hediye kartları PIN'leri desteklemez.</span><span class="sxs-lookup"><span data-stu-id="9b3c9-148">**PIN** – By default, internal gift cards don't support PINs.</span></span> <span data-ttu-id="9b3c9-149">Bakiyeleri aramak için bir PIN gerekli olacak şekilde dahili hediye kartlarını genişletmelisiniz.</span><span class="sxs-lookup"><span data-stu-id="9b3c9-149">You should extend internal gift cards so that a PIN is required to look up balances.</span></span> <span data-ttu-id="9b3c9-150">Bu işlev ayrıca peş peşe yanlış PIN girme denemelerinden sonra hediye kartlarını kilitlemek için de kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="9b3c9-150">This functionality can also be used to lock gift cards after consecutive incorrect attempts to enter the PIN.</span></span>

## <a name="enable-gift-card-payments-for-guest-checkout"></a><span data-ttu-id="9b3c9-151">Konuk ödemeleri için hediye kartı ödemelerini etkinleştirme</span><span class="sxs-lookup"><span data-stu-id="9b3c9-151">Enable gift card payments for guest checkout</span></span>

<span data-ttu-id="9b3c9-152">Varsayılan olarak, hediye kartı ödemeleri konuk (anonim) ödeme için etkin değildir.</span><span class="sxs-lookup"><span data-stu-id="9b3c9-152">By default, gift card payments aren't enabled for guest (anonymous) checkout.</span></span> <span data-ttu-id="9b3c9-153">Bunu etkinleştirmek için şu adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="9b3c9-153">To enable them, follow these steps.</span></span>

1. <span data-ttu-id="9b3c9-154">Commerce genel merkezinde **Retail ve Commerce \> Kanal ayarı \> POS ayarı \> POS \> POS İşlemleri**'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="9b3c9-154">In Commerce headquarters, go to **Retail and Commerce \> Channel setup \> POS setup \> POS \> POS Operations**.</span></span>
1. <span data-ttu-id="9b3c9-155">Kılavuz üstbilgisini seçin ve tutun (veya sağ tıklayın) ve sonra **Sütun ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="9b3c9-155">Select and hold (or right-click) the header of the grid, and then select **Insert columns**.</span></span>
1. <span data-ttu-id="9b3c9-156">**Sütun ekle** iletişim kutusunda, **AllowAnonymousAccess** onay kutusunu seçin.</span><span class="sxs-lookup"><span data-stu-id="9b3c9-156">In the **Insert columns** dialog box, select the **AllowAnonymousAccess** check box.</span></span>
1. <span data-ttu-id="9b3c9-157">**Güncelleştir**'i seçin</span><span class="sxs-lookup"><span data-stu-id="9b3c9-157">Select **Update**.</span></span>
1. <span data-ttu-id="9b3c9-158">**520** (Hediye kartı bakiyesi) ve **214** işlemleri için **AllowAnonymousAccess** değerini **1** olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="9b3c9-158">For operations **520** (Gift card balance) and **214**, set the **AllowAnonymousAccess** value to **1**.</span></span>
1. <span data-ttu-id="9b3c9-159">**Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="9b3c9-159">Select **Save**.</span></span>
1. <span data-ttu-id="9b3c9-160">Değişiklikleri kanal veritabanıyla eşitlemek için **1090** zamanlayıcı işini yürütün.</span><span class="sxs-lookup"><span data-stu-id="9b3c9-160">Run the **1090** scheduler job to sync changes to the channel database.</span></span> 

## <a name="add-a-gift-card-module-to-a-page"></a><span data-ttu-id="9b3c9-161">Sayfaya hediye kartı modülü ekleme</span><span class="sxs-lookup"><span data-stu-id="9b3c9-161">Add a gift card module to a page</span></span>

<span data-ttu-id="9b3c9-162">Bir ödeme sayfasına hediye kartı modülü ekleme ve gerekli özellikleri ayarlama yönergeleri için bkz. [Ödeme modülü](add-checkout-module.md).</span><span class="sxs-lookup"><span data-stu-id="9b3c9-162">For instructions on how to add a gift card module to a checkout page and set the required properties, see [Checkout module](add-checkout-module.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="9b3c9-163">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="9b3c9-163">Additional resources</span></span>

[<span data-ttu-id="9b3c9-164">Sepet modülü</span><span class="sxs-lookup"><span data-stu-id="9b3c9-164">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="9b3c9-165">Sepet simgesi modülü</span><span class="sxs-lookup"><span data-stu-id="9b3c9-165">Cart icon module</span></span>](cart-icon-module.md)

[<span data-ttu-id="9b3c9-166">Ödeme modülü</span><span class="sxs-lookup"><span data-stu-id="9b3c9-166">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="9b3c9-167">Ödeme modülü</span><span class="sxs-lookup"><span data-stu-id="9b3c9-167">Payment module</span></span>](payment-module.md)

[<span data-ttu-id="9b3c9-168">Sevkiyat adresi modülü</span><span class="sxs-lookup"><span data-stu-id="9b3c9-168">Shipping address module</span></span>](ship-address-module.md)

[<span data-ttu-id="9b3c9-169">Teslimat seçenekleri modülü</span><span class="sxs-lookup"><span data-stu-id="9b3c9-169">Delivery options module</span></span>](delivery-options-module.md)

[<span data-ttu-id="9b3c9-170">Malzeme çekme bilgileri modülü</span><span class="sxs-lookup"><span data-stu-id="9b3c9-170">Pickup information module</span></span>](pickup-info-module.md)

[<span data-ttu-id="9b3c9-171">Sipariş ayrıntıları modülü</span><span class="sxs-lookup"><span data-stu-id="9b3c9-171">Order details module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="9b3c9-172">Harici hediye kartları için destek</span><span class="sxs-lookup"><span data-stu-id="9b3c9-172">Support for external gift cards</span></span>](./dev-itpro/gift-card.md)

[<span data-ttu-id="9b3c9-173">SDK ve modül kitaplığı güncelleştirmeleri</span><span class="sxs-lookup"><span data-stu-id="9b3c9-173">SDK and module library updates</span></span>](e-commerce-extensibility/sdk-updates.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
