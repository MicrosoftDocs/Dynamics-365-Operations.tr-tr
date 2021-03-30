---
title: Sepet ve ödeme sayfalarına genel bakış
description: Bu konu, Microsoft Dynamics 365 Commerce'ta sepet ve ödeme sayfalarına genel bakış sağlar.
author: anupamar-ms
manager: annbe
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 4f7c708aa7f1a858e78cdbda809b90b944606022
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5244804"
---
# <a name="cart-and-checkout-pages-overview"></a><span data-ttu-id="3d310-103">Sepet ve ödeme sayfalarına genel bakış</span><span class="sxs-lookup"><span data-stu-id="3d310-103">Cart and checkout pages overview</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="3d310-104">Bu konu, Microsoft Dynamics 365 Commerce'ta sepet ve ödeme sayfalarına genel bakış sağlar.</span><span class="sxs-lookup"><span data-stu-id="3d310-104">This topic provides an overview of the cart and checkout pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="3d310-105">Genel Bakış</span><span class="sxs-lookup"><span data-stu-id="3d310-105">Overview</span></span>

<span data-ttu-id="3d310-106">Bir e-ticaret web sitesinin alışveriş sayfası bir müşterinin sepete eklediği tüm maddeleri gösterir.</span><span class="sxs-lookup"><span data-stu-id="3d310-106">The cart page of an e-Commerce website shows all items that a customer has added to the cart.</span></span> <span data-ttu-id="3d310-107">Alışveriş sepeti sayfası, sepet modülü kullanılarak oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="3d310-107">The cart page is built by using the cart module.</span></span> <span data-ttu-id="3d310-108">Bir sepet modülü, sepetteki öğelerin gösterimi için gerekli olan tüm modülleri barındırmak için kullanılan bir konteynerdir.</span><span class="sxs-lookup"><span data-stu-id="3d310-108">The cart module is a container that hosts all the modules that are required to showcase items in the cart.</span></span> <span data-ttu-id="3d310-109">Sepet modülü ayrıca sipariş özetini ve müşteri emrine uygulanan promosyon kodlarını göstermek için diğer modülleri de kullanabilir.</span><span class="sxs-lookup"><span data-stu-id="3d310-109">The cart module can also use other modules to show the order summary and any promotional codes that have been applied to the customer order.</span></span>

<span data-ttu-id="3d310-110">Bir e-ticaret Web sitesinin kullanıma alma sayfası, müşterinin sipariş vermek için gereken tüm bilgileri girmesi için takip eden adım adım bir akış sunar.</span><span class="sxs-lookup"><span data-stu-id="3d310-110">The checkout page of an e-Commerce website presents a step-by-step flow that customers follow to enter all the information that is required to place an order.</span></span> <span data-ttu-id="3d310-111">Bir ödeme modülü sevkiyat adresini, Sevkiyat yöntemlerini, fatura bilgilerini, sipariş özetini ve bir müşteri emriyle ilişkili diğer bilgileri ele alan modüller içerebilir.</span><span class="sxs-lookup"><span data-stu-id="3d310-111">A checkout module can include modules that handle the shipping address, shipping methods, billing information, order summary, and other information that is related to customer orders.</span></span>

## <a name="cart-page"></a><span data-ttu-id="3d310-112">Sepet sayfası</span><span class="sxs-lookup"><span data-stu-id="3d310-112">Cart page</span></span>

<span data-ttu-id="3d310-113">Sepet sayfası, alışveriş çantası olarak hizmet görür ve sepete eklenen tüm maddeleri içerir.</span><span class="sxs-lookup"><span data-stu-id="3d310-113">The cart page serves as the shopping bag and includes all the items that have been added to the cart.</span></span>

<span data-ttu-id="3d310-114">Aşağıdaki çizimde, modül kitaplığı ve "Fabrikam" teması kullanılarak oluşturulmuş bir sepet sayfası örneği gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="3d310-114">The following illustration show an example of a cart page that was built by using the module library and the "Fabrikam" theme.</span></span>

![Sepet sayfası örneği](./media/cart2.PNG)

<span data-ttu-id="3d310-116">Sepet sayfasının ana bölümü bir müşterinin sepete eklediği tüm maddeleri gösterir.</span><span class="sxs-lookup"><span data-stu-id="3d310-116">The main body of the cart page shows all the items that the customer has added to the cart.</span></span> <span data-ttu-id="3d310-117">İlgili tüm indirimler göster.</span><span class="sxs-lookup"><span data-stu-id="3d310-117">All applicable discounts are showcased.</span></span> <span data-ttu-id="3d310-118">Bu iskontolar karmaşık iskontolar içerir.</span><span class="sxs-lookup"><span data-stu-id="3d310-118">These discounts include complex discounts.</span></span> <span data-ttu-id="3d310-119">Örneğin, "3 öğe satın alın ve %10 indirim" veya "%10 indirim için şişe ve sırt çantası satın alın" gibi örnekler verilebilir.</span><span class="sxs-lookup"><span data-stu-id="3d310-119">Examples include "Buy 3 items and get 10% off" or "Buy a bottle and a backpack to get 10% off."</span></span> <span data-ttu-id="3d310-120">Sipariş Özeti modülü iskontolar, Sevkiyat, vergiler vb. sonrasında ödenmesi gereken tutarı gösterir.</span><span class="sxs-lookup"><span data-stu-id="3d310-120">The order summary module shows the amount that is due after discounts, shipping, taxes, and so on, have been applied.</span></span> <span data-ttu-id="3d310-121">Ayrıca, müşterinin promosyon kodları uygulamasını veya kaldırmasını sağlayan bir promosyon kodu modülü de vardır.</span><span class="sxs-lookup"><span data-stu-id="3d310-121">There is also a promo code module that lets the customer apply or remove promotional codes.</span></span>

<span data-ttu-id="3d310-122">Müşteri anonim olarak veya oturum açmış bir kullanıcı olarak alışveriş yapabilir.</span><span class="sxs-lookup"><span data-stu-id="3d310-122">A customer can shop anonymously or as a signed-in user.</span></span> <span data-ttu-id="3d310-123">Bir müşteri oturum açmışsa, sepetteki öğeler oturumlar arasında korunur.</span><span class="sxs-lookup"><span data-stu-id="3d310-123">If a customer is signed in, items in the cart are preserved between sessions.</span></span> <span data-ttu-id="3d310-124">Bu şekilde, müşteri birden çok cihazda alışveriş yapmaya devam edebilir.</span><span class="sxs-lookup"><span data-stu-id="3d310-124">In this way, the customer can continue to shop from multiple devices.</span></span>

<span data-ttu-id="3d310-125">Müşteri sepetten itibaren teslim almayı devam edebilir.</span><span class="sxs-lookup"><span data-stu-id="3d310-125">From the cart, the customer can proceed to checkout.</span></span> <span data-ttu-id="3d310-126">Müşteri, konuk kullanıcı veya oturum açmış kullanıcı olarak kullanıma almayı başlatabilir.</span><span class="sxs-lookup"><span data-stu-id="3d310-126">A customer can initiate checkout as a guest user or as a signed-in user.</span></span>

<span data-ttu-id="3d310-127">Bir sepet sayfasının nasıl yazılacağıyla ilgili bilgi için, bkz. [Sayfaya sepet modülü ekleme](add-cart-module.md).</span><span class="sxs-lookup"><span data-stu-id="3d310-127">For information about how to author a cart page, see [Add a cart module to a page](add-cart-module.md).</span></span>

## <a name="checkout-page"></a><span data-ttu-id="3d310-128">Kullanıma alma sayfası</span><span class="sxs-lookup"><span data-stu-id="3d310-128">Checkout page</span></span>

<span data-ttu-id="3d310-129">Kullanıma alma sayfası, müşterinin bir siparişi yerleştirmek için gereken bilgileri girebildiği yerdir.</span><span class="sxs-lookup"><span data-stu-id="3d310-129">The checkout page is where customers enter the information that is required to place an order.</span></span>

<span data-ttu-id="3d310-130">Aşağıdaki çizimde, modül kitaplığı kullanılarak oluşturulmuş bir ödeme sayfası örneği gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="3d310-130">The following illustration show an example of a checkout page that was built by using the module library.</span></span>

![Ödeme sayfası örneği](./media/Checkout.PNG)

<span data-ttu-id="3d310-132">Kullanıma alma sayfasının ana gövdesi tüm sipariş bilgilerinin toplandığı yerdir.</span><span class="sxs-lookup"><span data-stu-id="3d310-132">The main body of the checkout page is where all the order information is collected.</span></span> <span data-ttu-id="3d310-133">Bu bilgiler sevkiyat adresi, teslimat seçenekleri ve ödeme bilgilerini içerir.</span><span class="sxs-lookup"><span data-stu-id="3d310-133">This information includes the shipping address, delivery options, and payment information.</span></span> <span data-ttu-id="3d310-134">Bilgilerin işlenmesi için belirli bir sırada girilmesi gerektiğinden, teslim alma sırasında adım adım bir akış vardır.</span><span class="sxs-lookup"><span data-stu-id="3d310-134">Checkout has a step-by-step flow, because the information must be entered in a specific order to be processed.</span></span> <span data-ttu-id="3d310-135">Örneğin, Sevkiyat maliyetleri hesaplanmadan ödeme yetkilendirilebileceği şekilde, sevkiyat adresi girilmelidir.</span><span class="sxs-lookup"><span data-stu-id="3d310-135">For example, the shipping address must be entered before the shipping costs can be calculated and the payment can be authorized.</span></span>

### <a name="shipping-address"></a><span data-ttu-id="3d310-136">Sevkiyat adresi</span><span class="sxs-lookup"><span data-stu-id="3d310-136">Shipping address</span></span>

<span data-ttu-id="3d310-137">Maddelerin sevk edilmesi gerekiyorsa sevkiyat adresi gereklidir.</span><span class="sxs-lookup"><span data-stu-id="3d310-137">A shipping address is required if items must be shipped.</span></span> <span data-ttu-id="3d310-138">Her bir yerel ayarın sevkiyat adreslerinin biçimi Dynamics 365 Commerce'de yapılandırılabilir.</span><span class="sxs-lookup"><span data-stu-id="3d310-138">The format of shipping addresses for each locale can be configured in Dynamics 365 Commerce.</span></span> <span data-ttu-id="3d310-139">Örneğin, maddeler Amerika Birleşik Devletleri sevk edilecekse, sevkiyat adresi bir sokak adresi, il ve Posta Kodu içermelidir.</span><span class="sxs-lookup"><span data-stu-id="3d310-139">For example, if the items will be shipped to the United States, the shipping address must include a street address, state, and ZIP Code.</span></span> <span data-ttu-id="3d310-140">Bazı temel giriş doğrulamaları, alfasayısal karakterler, maksimum uzunluk ve sayıların doğrulaması gibi adres alanlarının sevkiyatı için yapılır.</span><span class="sxs-lookup"><span data-stu-id="3d310-140">Some basic input validation is done for shipping address fields, such as validation for alphanumeric characters, maximum length, and numbers.</span></span> <span data-ttu-id="3d310-141">Adresin geçerliliği doğrulanmasa da, bu doğrulama özelleştirilmiş üçüncü taraf hizmetler kullanılarak yapılabilir.</span><span class="sxs-lookup"><span data-stu-id="3d310-141">Although the validity of the address itself isn't verified, this verification can be done by using customized third-party services.</span></span>

<span data-ttu-id="3d310-142">Sevkiyat adresi, "sevk et" seçeneğinin işaretli olduğu sepetteki tüm maddelere uygulanır.</span><span class="sxs-lookup"><span data-stu-id="3d310-142">The shipping address is applied to all items in the cart that the "ship" option is selected for.</span></span> <span data-ttu-id="3d310-143">Çevrimiçi modül kitaplığı içinde sağlanan kullanıma alma akışını kullanırsanız, bireysel alışveriş maddeleri farklı adreslere sevk edilebilir.</span><span class="sxs-lookup"><span data-stu-id="3d310-143">If you use the checkout flow that is provided in the module library, individual cart items can't be shipped to different addresses.</span></span> <span data-ttu-id="3d310-144">Bu yeteneğe gereksinim duyarsanız, kullanıma alma modülleri özelleştirilmesiyle gerçekleştirilebilir.</span><span class="sxs-lookup"><span data-stu-id="3d310-144">If you require this capability, it can be implemented through customization of the checkout modules.</span></span>

<span data-ttu-id="3d310-145">Sevkiyat Adresi sağlandığında, Dynamics 365 Commerce çevrimiçi mağazadan kullanılabilen Sevkiyat Yöntemleri gösterilir.</span><span class="sxs-lookup"><span data-stu-id="3d310-145">After the shipping address is provided, the shipping methods that are available from the Dynamics 365 Commerce online store are shown.</span></span> <span data-ttu-id="3d310-146">Sevkiyat Yöntemleri ve destekledikleri adresler Commerce'de konfigüre edilebilir.</span><span class="sxs-lookup"><span data-stu-id="3d310-146">The shipping methods and the addresses that they support can be configured in Commerce.</span></span>

### <a name="payment"></a><span data-ttu-id="3d310-147">Ödeme</span><span class="sxs-lookup"><span data-stu-id="3d310-147">Payment</span></span>

<span data-ttu-id="3d310-148">Ödeme akışındaki sonraki adım ödemedir.</span><span class="sxs-lookup"><span data-stu-id="3d310-148">The next step in the checkout flow is payment.</span></span> <span data-ttu-id="3d310-149">E-ticaret'te kredi kartları, hediye kartları ve bağlılık programı puanları gibi siparişler yerleştirmek için çoklu ödeme yöntemleri kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="3d310-149">In e-Commerce, multiple methods of payment can be used to place orders, such as credit cards, gift cards, and loyalty points.</span></span> <span data-ttu-id="3d310-150">Bu ödeme yöntemlerinin bir birleşimi de kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="3d310-150">A combination of these payment methods can also be used.</span></span> <span data-ttu-id="3d310-151">Kullanılan ödeme yöntemlerine bağlı olarak ek bilgiler gerekebilir.</span><span class="sxs-lookup"><span data-stu-id="3d310-151">Depending on the payment methods that are used, additional information might be required.</span></span> <span data-ttu-id="3d310-152">Örneğin, kredi kartı ödemesi bir faturalama adresi gerektirir.</span><span class="sxs-lookup"><span data-stu-id="3d310-152">For example, a credit card payment requires a billing address.</span></span> <span data-ttu-id="3d310-153">Kredi kartı ödemeleri, Adyen ödeme bağlayıcısı kullanılarak işlenir.</span><span class="sxs-lookup"><span data-stu-id="3d310-153">Credit card payments are processed by using the Adyen Payment Connector.</span></span>

#### <a name="loyalty-points"></a><span data-ttu-id="3d310-154">Bağlılık programı puanları</span><span class="sxs-lookup"><span data-stu-id="3d310-154">Loyalty points</span></span>

<span data-ttu-id="3d310-155">Sağlama akışı sırasında, bir bağlılık programına üye olan ve tahakkuk eden bağlılık programı puanları olan bir müşteri bir sipariş için bu bağlılık programı puanlarını kullanmaya çalışabilir.</span><span class="sxs-lookup"><span data-stu-id="3d310-155">During the checkout flow, a customer who is a member of a loyalty program and who has accrued loyalty points can redeem those loyalty points for an order.</span></span> <span data-ttu-id="3d310-156">Bağlılık programı puanları modülü yalnızca müşterinin varolan bağlılık programı üyeliği varsa görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="3d310-156">The loyalty points module is shown only if the customer has an existing loyalty membership.</span></span> <span data-ttu-id="3d310-157">Üye olmayanlar ve Konuk kullanıcılar için bu modül gizlenir.</span><span class="sxs-lookup"><span data-stu-id="3d310-157">For non-members and guest users, this module is hidden.</span></span>

#### <a name="gift-cards"></a><span data-ttu-id="3d310-158">Hediye kartları</span><span class="sxs-lookup"><span data-stu-id="3d310-158">Gift cards</span></span>

<span data-ttu-id="3d310-159">Çevrimiçi modül kitaplığı, bir sipariş için dahili hediye kartlarından daha fazla kullanılabilir olmasını sağlar.</span><span class="sxs-lookup"><span data-stu-id="3d310-159">The module library lets internal gift cards be redeemed for an order.</span></span> <span data-ttu-id="3d310-160">Dahili bir hediye kartı uygulamak için, müşterinin oturum açmış olması gerekir.</span><span class="sxs-lookup"><span data-stu-id="3d310-160">To apply an internal gift card, the customer must be signed in.</span></span> <span data-ttu-id="3d310-161">Ek güvenlik için, dahili hediye kartları için bir kişisel kimlik numarası (PIN) kullanarak akışı özelleştirmenizi öneririz.</span><span class="sxs-lookup"><span data-stu-id="3d310-161">For additional security, we recommend that you customize the flow by using a personal identification number (PIN) for internal gift cards.</span></span>

### <a name="signed-in-and-guest-users"></a><span data-ttu-id="3d310-162">Oturum açmış ve konuk kullanıcılar</span><span class="sxs-lookup"><span data-stu-id="3d310-162">Signed-in and guest users</span></span>

<span data-ttu-id="3d310-163">Müşteri, konuk kullanıcı veya oturum açmış kullanıcı olarak kullanıma almayı tamamlayabilir.</span><span class="sxs-lookup"><span data-stu-id="3d310-163">The customer can complete the checkout process as a guest user or a signed-in user.</span></span> <span data-ttu-id="3d310-164">Müşteri oturum açtığında, kaydedilen sevkiyat adresleri ve kaydedilmiş kredi kartı ayrıntıları gibi hesap bilgileri otomatik olarak alınır.</span><span class="sxs-lookup"><span data-stu-id="3d310-164">If the customer signs in, account information such as saved shipping addresses and saved credit card details is automatically retrieved.</span></span>

### <a name="order-summary"></a><span data-ttu-id="3d310-165">Sipariş özeti</span><span class="sxs-lookup"><span data-stu-id="3d310-165">Order summary</span></span>

<span data-ttu-id="3d310-166">Ödeme, müşteriye siparişi vermeden önce bir sipariş doğrulayabilmesi için sepetteki satır maddelerinin bir özetini gösterir.</span><span class="sxs-lookup"><span data-stu-id="3d310-166">Checkout shows a summary of the line items in the cart, so that the customer can verify the order before he or she places it.</span></span> <span data-ttu-id="3d310-167">Satır maddeleri, kullanıma alma akışı sırasında düzenlenemez.</span><span class="sxs-lookup"><span data-stu-id="3d310-167">The line items can't be edited during the checkout flow.</span></span> <span data-ttu-id="3d310-168">Ancak, kullanıcının geri gitmek ve satır öğelerini düzenlemek istediği durumda alışveriş sepetine bir bağlantı sağlanır.</span><span class="sxs-lookup"><span data-stu-id="3d310-168">However, a link to the cart is provided in case the user wants to go back and edit line items.</span></span>

<span data-ttu-id="3d310-169">Müşteri sevkiyat ve faturalama bilgilerini girdikten sonra, bağlılık programı noktaları, hediye kartları ve diğer ödemeler uygulandıktan sonra ödenmesi gereken tutarı yansıtır.</span><span class="sxs-lookup"><span data-stu-id="3d310-169">After the customer provides shipping and billing information, the order summary reflects the amount that is due after loyalty points, gift cards, and other payments have been applied.</span></span>

### <a name="order-confirmation-and-email"></a><span data-ttu-id="3d310-170">Satış onayı ve e-postası</span><span class="sxs-lookup"><span data-stu-id="3d310-170">Order confirmation and email</span></span>

<span data-ttu-id="3d310-171">Müşteri bir sipariş yerleştirdiğinde, bir onay numarası sağlanır.</span><span class="sxs-lookup"><span data-stu-id="3d310-171">When the customer places an order, a confirmation number is provided.</span></span> <span data-ttu-id="3d310-172">Bu aşamada, ödeme yetkilendirilemez, ancak ücretlendirilmemiştir.</span><span class="sxs-lookup"><span data-stu-id="3d310-172">At this point, the payment has been authorized but not charged.</span></span> <span data-ttu-id="3d310-173">Ödeme, yalnızca sipariş yerine getirilmişse (yani, sevk edildiğinde veya çekildiğinde) ücretlendirilecektir.</span><span class="sxs-lookup"><span data-stu-id="3d310-173">The payment will be charged only when the order is fulfilled (that is, when it's either shipped or picked up).</span></span>

<span data-ttu-id="3d310-174">Bir sipariş oluşturulduktan sonra, müşteriye bir sipariş teyidi e-postası gönderilir.</span><span class="sxs-lookup"><span data-stu-id="3d310-174">After an order is created, an order confirmation email is sent to the customer.</span></span>

<span data-ttu-id="3d310-175">Bir ödeme sayfasının nasıl yazılacağıyla ilgili daha fazla bilgi için, bkz. [Sayfaya ödeme modülü ekleme](add-checkout-module.md).</span><span class="sxs-lookup"><span data-stu-id="3d310-175">For more information about how to author a checkout page, see [Add a checkout module to a page](add-checkout-module.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="3d310-176">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="3d310-176">Additional resources</span></span>

[<span data-ttu-id="3d310-177">Giriş sayfasına genel bakış</span><span class="sxs-lookup"><span data-stu-id="3d310-177">Home page overview</span></span>](quick-tour-home-page.md)

[<span data-ttu-id="3d310-178">Ürün ayrıntıları sayfalarına genel bakış</span><span class="sxs-lookup"><span data-stu-id="3d310-178">Product details pages overview</span></span>](quick-tour-pdp.md)

[<span data-ttu-id="3d310-179">Hesap yönetimi sayfalarına genel bakış</span><span class="sxs-lookup"><span data-stu-id="3d310-179">Account management pages overview</span></span>](quick-tour-account-management.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]