---
title: Hesap yönetimi sayfaları ve modülleri
description: Bu konu, Microsoft Dynamics 365 Commerce'ta hesap yönetimi sayfalarını ve modüllerini kapsamaktadır.
author: v-chgri
manager: annbe
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: 29523d03fb687684dae7d0ce08208905cce702df
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5206643"
---
# <a name="account-management-pages-and-modules"></a><span data-ttu-id="75966-103">Hesap yönetimi sayfaları ve modülleri</span><span class="sxs-lookup"><span data-stu-id="75966-103">Account management pages and modules</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="75966-104">Bu konu, Microsoft Dynamics 365 Commerce'ta hesap yönetimi sayfalarını ve modüllerini kapsamaktadır.</span><span class="sxs-lookup"><span data-stu-id="75966-104">This topic covers account management pages and modules in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="75966-105">Hesap yönetimi, Dynamics 365 Commerce'teki Kullanıcı hesabı ile ilgili bilgileri yönetmek için kullanılan bir grup sayfayı gösterir.</span><span class="sxs-lookup"><span data-stu-id="75966-105">Account management refers to a group of pages that is used to manage user account–related information in Dynamics 365 Commerce.</span></span> <span data-ttu-id="75966-106">Hesap yönetimi sayfaları, hesap yönetimi giriş sayfası, kullanıcı profili sayfası, kullanıcı adresi sayfası, sipariş geçmişi sayfası, sipariş ayrıntıları sayfası, bağlılık programı sayfası ve istek listesi sayfasını içerir.</span><span class="sxs-lookup"><span data-stu-id="75966-106">Account management pages include the account management landing page, user profile page, user address page, order history page, order details page, loyalty page, and wish list page.</span></span>

### <a name="account-management-landing-page"></a><span data-ttu-id="75966-107">Hesap yönetimi giriş sayfası</span><span class="sxs-lookup"><span data-stu-id="75966-107">Account management landing page</span></span>

<span data-ttu-id="75966-108">Hesap yönetimi giriş sayfası aşağıdaki modülleri kullanır:</span><span class="sxs-lookup"><span data-stu-id="75966-108">The account management landing page uses the following modules:</span></span>

- <span data-ttu-id="75966-109">**Konteyner** - Tüm hesap yönetimi giriş sayfası modülleri bir kapsayıcı içinde yer almalıdır.</span><span class="sxs-lookup"><span data-stu-id="75966-109">**Container** - All account management landing page modules should be placed within a container.</span></span> 
- <span data-ttu-id="75966-110">**Hesap karşılama kutucuğu** – bu modül, hesap yönetimi sayfasında hoş geldiniz iletisi sağlamak için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="75966-110">**Account welcome tile** – This module is used to provide a welcome message on the account management page.</span></span> <span data-ttu-id="75966-111">Başlığa ilişkin özellikleri içerir.</span><span class="sxs-lookup"><span data-stu-id="75966-111">It includes properties for the heading.</span></span>
- <span data-ttu-id="75966-112">**Hesap genel kutucuğu** -bu modül, "Sipariş geçmişi" veya "Profilim" sayfaları gibi hesap yönetimi sayfalarına başlık ve bağlantı sağlamak için kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="75966-112">**Account generic tile** - This module can be used to provide headings and links to account management pages, such as the "Order history" or "My profile" pages.</span></span> <span data-ttu-id="75966-113">Genel döşeme modülü herhangi bir sayfa için bir kutucuğu yapılandırmak amacıyla kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="75966-113">The generic tile module can be used to configure a tile for any page.</span></span> <span data-ttu-id="75966-114">Fabrikam'da, bu modül hesap yönetimi giriş sayfasındaki "Sipariş geçmişi" ve "Profilim" sayfa bağlantıları için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="75966-114">In Fabrikam, this module is used for "Order history" and "My profile" page links on the account management landing page.</span></span>
- <span data-ttu-id="75966-115">**Hesap istek listesi kutucuğu** – bu modül, müşterinin istek listesindeki maddelerin özetini sağlamak için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="75966-115">**Account wishlist tile** – This module is used to provide a summary of the items on the customer's wish list.</span></span> <span data-ttu-id="75966-116">Örneğin, "İstek listenizde 10 öğe var" olabilir.</span><span class="sxs-lookup"><span data-stu-id="75966-116">For example, it might state, "You have 10 items in your wish list."</span></span> <span data-ttu-id="75966-117">Başlık, başlık için özellikleri ve "Ayrıntıları görüntüle" bağlantısı özelliklerini içerir.</span><span class="sxs-lookup"><span data-stu-id="75966-117">It includes properties for the heading and the "View details" link.</span></span> <span data-ttu-id="75966-118">"Ayrıntıları Görüntüle" bağlantısı istek listesi sayfasına yeniden yönlendirilecek şekilde yapılandırılmalıdır.</span><span class="sxs-lookup"><span data-stu-id="75966-118">The "View details" link should be configured to redirect to the wish list page.</span></span> 
- <span data-ttu-id="75966-119">**Hesap adresi kutucuğu** – bu modül, Kullanıcı adreslerinin özetini sağlamak için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="75966-119">**Account address tile** – This module is used to provide a summary of the user's addresses.</span></span> <span data-ttu-id="75966-120">Örneğin, "Hesabınıza 2 adres eklendi" durumu olabilir.</span><span class="sxs-lookup"><span data-stu-id="75966-120">For example, it might state, "You have 2 addresses added to your account."</span></span> <span data-ttu-id="75966-121">Başlık, başlık için özellikleri ve "Ayrıntıları görüntüle" bağlantısı özelliklerini içerir.</span><span class="sxs-lookup"><span data-stu-id="75966-121">It includes properties for the heading and the "View details" link.</span></span> <span data-ttu-id="75966-122">"Ayrıntıları Görüntüle" bağlantısı kullanıcı adresi sayfasına yeniden yönlendirilecek şekilde konfigüre edilmelidir.</span><span class="sxs-lookup"><span data-stu-id="75966-122">The "View details" link should be configured to redirect to the user address page.</span></span>
- <span data-ttu-id="75966-123">**Hesap bağlılık kutucuğu** – Bu modül, bağlılık programı bilgilerini görüntülemek ve bağlamak için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="75966-123">**Account loyalty tile** – This module is used to display and link to loyalty program information.</span></span> <span data-ttu-id="75966-124">Bu kutucuğun iki durumu vardır: bir durum, bir üye değilse, bağlılık programına katılma bağlantılarını gösterir.</span><span class="sxs-lookup"><span data-stu-id="75966-124">This tile has two states: one state shows links to join a loyalty progam if the user is not a member already.</span></span> <span data-ttu-id="75966-125">Diğer durum, kullanıcının zaten üye olduğunda bağlılık programı ayrıntıları sayfasını görüntülemek için bağlantıları gösterir.</span><span class="sxs-lookup"><span data-stu-id="75966-125">The other state shows links to view the loyalty details page when the user is already a member.</span></span> <span data-ttu-id="75966-126">Özellikler başlığı, "Kaydol" bağlantısı ve "Bağlılık programını görüntüle" bağlantısını içerir.</span><span class="sxs-lookup"><span data-stu-id="75966-126">Properties include the heading, the "Sign-up" link, and the "View loyalty" link.</span></span> <span data-ttu-id="75966-127">"Bağlılık programını görüntüle" bağlantısı bağlılık sayfasına yeniden yönlendirilecek şekilde yapılandırılmalıdır.</span><span class="sxs-lookup"><span data-stu-id="75966-127">The "View loyalty" link should be configured to redirect to the loyalty page.</span></span> <span data-ttu-id="75966-128">"Üye olun" bağlantısı, kullanıcıların bağlılık programına katılabilecek bir sayfaya yeniden yönlendirilecek şekilde yapılandırılmalıdır.</span><span class="sxs-lookup"><span data-stu-id="75966-128">The "Sign-up" link should be configured to redirect to a page where users can join the loyalty program.</span></span> 

### <a name="order-history-page"></a><span data-ttu-id="75966-129">Sipariş geçmişi sayfası</span><span class="sxs-lookup"><span data-stu-id="75966-129">Order history page</span></span>

<span data-ttu-id="75966-130">Sipariş geçmişi sayfası, kullanıcının verdiği tüm son siparişleri göstermek için sipariş geçmişi modülünü kullanır.</span><span class="sxs-lookup"><span data-stu-id="75966-130">The order history page uses the order history module to show all the recent orders that the user has placed.</span></span>

### <a name="order-details-page"></a><span data-ttu-id="75966-131">Sipariş ayrıntıları sayfası</span><span class="sxs-lookup"><span data-stu-id="75966-131">Order details page</span></span>

<span data-ttu-id="75966-132">Sipariş Ayrıntıları sayfası her sipariş için ayrıntılı bilgi sağlar ve sipariş geçmişi sayfasından erişilir.</span><span class="sxs-lookup"><span data-stu-id="75966-132">The order details page provides detailed information for each order and is accessed from the order history page.</span></span> <span data-ttu-id="75966-133">Sipariş ayrıntılarını almak için satış kodu veya işlem kodunun gerekli olmasını gerektiren sipariş ayrıntıları modülünü kullanır.</span><span class="sxs-lookup"><span data-stu-id="75966-133">It uses the order details module, which requires the sales ID or transaction ID to retrieve the order details.</span></span>

### <a name="user-profile-page"></a><span data-ttu-id="75966-134">Kullanıcı profil sayfası</span><span class="sxs-lookup"><span data-stu-id="75966-134">User profile page</span></span>

<span data-ttu-id="75966-135">Kullanıcı profili sayfası kullanıcının adı ve e-posta adresi gibi kullanıcı hesabı ayrıntılarını gösterir.</span><span class="sxs-lookup"><span data-stu-id="75966-135">The user profile page shows user account details, such as a user's name and email address.</span></span> <span data-ttu-id="75966-136">Kullanıcı profili ayrıntılarını ve Kullanıcı profili düzenleme modüllerini kullanır.</span><span class="sxs-lookup"><span data-stu-id="75966-136">It uses the user profile details and user profile edit modules.</span></span> <span data-ttu-id="75966-137">Ancak e-posta adresi kaldırılamaz, düzenlenebilir.</span><span class="sxs-lookup"><span data-stu-id="75966-137">Although the email address can't be removed, it can be edited.</span></span> <span data-ttu-id="75966-138">Kullanıcı profili sayfası, kullanıcının öneri listelerinin kişiselleştirmesi gibi belirli özellikleri kabul etmesini veya devre dışı olmasını etkinleştiren Kullanıcı tercihlerini de gösterir.</span><span class="sxs-lookup"><span data-stu-id="75966-138">The user profile page also shows user preferences that enable a user to opt in or opt out from certain features, such as personalization of recommendation lists.</span></span> 

### <a name="user-address-page"></a><span data-ttu-id="75966-139">Kullanıcı adresi sayfası</span><span class="sxs-lookup"><span data-stu-id="75966-139">User address page</span></span>

<span data-ttu-id="75966-140">Kullanıcı adresi sayfası, kullanıcı hesabıyla ilişkili adreslerin listesini gösterir.</span><span class="sxs-lookup"><span data-stu-id="75966-140">The user address page shows the list of addresses that are associated with the user account.</span></span> <span data-ttu-id="75966-141">Kullanıcı bu adresleri kullanıma alma sırasında sağladı veya doğrudan bu sayfaya ekledi.</span><span class="sxs-lookup"><span data-stu-id="75966-141">The user either provided these addresses during checkout or added them directly on  this page.</span></span> <span data-ttu-id="75966-142">Kullanıcı Adres modülü, adres ekleme ve düzenleme, birincil adresi belirleme ve varolan adresleri sayfada işleme seçeneğini kullanır.</span><span class="sxs-lookup"><span data-stu-id="75966-142">The user address module is used add and edit addresses, set the primary address, and render existing addresses on the page.</span></span>

### <a name="wish-list-page"></a><span data-ttu-id="75966-143">İstek listesi sayfası</span><span class="sxs-lookup"><span data-stu-id="75966-143">Wish list page</span></span>

<span data-ttu-id="75966-144">İstek listesi sayfası, müşterinin istek listesine eklenen maddeleri gösterir.</span><span class="sxs-lookup"><span data-stu-id="75966-144">The wish list page shows the items that have been added to the customer's wish list.</span></span> <span data-ttu-id="75966-145">Liste öğelerini oluşturmak için, istek listesi modülünü kullanır.</span><span class="sxs-lookup"><span data-stu-id="75966-145">It uses the wish list module to render wish list items.</span></span>

### <a name="loyalty-page"></a><span data-ttu-id="75966-146">Bağlılık programı sayfası</span><span class="sxs-lookup"><span data-stu-id="75966-146">Loyalty page</span></span>

<span data-ttu-id="75966-147">Bağlılık programı sayfası müşterilerin, eğer halihazırda üyelerse, bağlılık programı ayrıntılarını görmelerini sağlar.</span><span class="sxs-lookup"><span data-stu-id="75966-147">The loyalty page lets customers view their loyalty details if they are already loyalty program members.</span></span> <span data-ttu-id="75966-148">Ayrıca, son hareketlerde kazanılan ve bunlar tarafından kullanılan puanları de görüntüleyebilirler.</span><span class="sxs-lookup"><span data-stu-id="75966-148">They can also view the points that they have earned and redeemed in recent transactions.</span></span> <span data-ttu-id="75966-149">Sayfa bağlılık programı ayrıntılarını gösterimi için bağlılık programı Ayrıntılar modülünü kullanır.</span><span class="sxs-lookup"><span data-stu-id="75966-149">The page uses the loyalty details module to showcase the loyalty details.</span></span> 

<span data-ttu-id="75966-150">Bağlılık programı programına katılmak için, bağlılık programı kayıt ve bağlılık programı şartları modülleriyle bir pazarlama sayfası oluşturulabilir.</span><span class="sxs-lookup"><span data-stu-id="75966-150">To join loyalty program, a marketing page can be created with loyalty sign up and loyalty terms modules.</span></span> <span data-ttu-id="75966-151">Kullanıcı bir bağlılık programı üyesi değilse, bu modüller kullanıcının kaydolmasını sağlayacaktır.</span><span class="sxs-lookup"><span data-stu-id="75966-151">If the user is not a member of a loyalty program, these modules will enable the user to sign up.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="75966-152">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="75966-152">Additional resources</span></span>

[<span data-ttu-id="75966-153">Modül kitaplığına genel bakış</span><span class="sxs-lookup"><span data-stu-id="75966-153">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="75966-154">Kapsayıcı modülü</span><span class="sxs-lookup"><span data-stu-id="75966-154">Container module</span></span>](add-container-module.md)

[<span data-ttu-id="75966-155">Satın alma kutusu modülü</span><span class="sxs-lookup"><span data-stu-id="75966-155">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="75966-156">Alışveriş sepeti modülü</span><span class="sxs-lookup"><span data-stu-id="75966-156">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="75966-157">Ödeme yapma modülü</span><span class="sxs-lookup"><span data-stu-id="75966-157">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="75966-158">Sipariş onayı modülü</span><span class="sxs-lookup"><span data-stu-id="75966-158">Order confirmation module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="75966-159">Üst bilgi modülü</span><span class="sxs-lookup"><span data-stu-id="75966-159">Header module</span></span>](author-header-module.md)

[<span data-ttu-id="75966-160">Alt bilgi modülü</span><span class="sxs-lookup"><span data-stu-id="75966-160">Footer module</span></span>](author-footer-module.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]