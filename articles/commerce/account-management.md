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
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: b0f963bcf65ae622522fe52fd59996c6ec0ecf17
ms.sourcegitcommit: 8028fbc5b9585e87d3331ea02577ff82ede090af
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/16/2020
ms.locfileid: "3817170"
---
# <a name="account-management-pages-and-modules"></a><span data-ttu-id="c2105-103">Hesap yönetimi sayfaları ve modülleri</span><span class="sxs-lookup"><span data-stu-id="c2105-103">Account management pages and modules</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="c2105-104">Bu konu, Microsoft Dynamics 365 Commerce'ta hesap yönetimi sayfalarını ve modüllerini kapsamaktadır.</span><span class="sxs-lookup"><span data-stu-id="c2105-104">This topic covers account management pages and modules in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="c2105-105">Genel Bakış</span><span class="sxs-lookup"><span data-stu-id="c2105-105">Overview</span></span>

<span data-ttu-id="c2105-106">Hesap yönetimi, Dynamics 365 Commerce'teki Kullanıcı hesabı ile ilgili bilgileri yönetmek için kullanılan bir grup sayfayı gösterir.</span><span class="sxs-lookup"><span data-stu-id="c2105-106">Account management refers to a group of pages that is used to manage user account–related information in Dynamics 365 Commerce.</span></span> <span data-ttu-id="c2105-107">Hesap yönetimi sayfaları, hesap yönetimi giriş sayfası, kullanıcı profili sayfası, kullanıcı adresi sayfası, sipariş geçmişi sayfası, sipariş ayrıntıları sayfası, bağlılık programı sayfası ve istek listesi sayfasını içerir.</span><span class="sxs-lookup"><span data-stu-id="c2105-107">Account management pages include the account management landing page, user profile page, user address page, order history page, order details page, loyalty page, and wish list page.</span></span>

### <a name="account-management-landing-page"></a><span data-ttu-id="c2105-108">Hesap yönetimi giriş sayfası</span><span class="sxs-lookup"><span data-stu-id="c2105-108">Account management landing page</span></span>

<span data-ttu-id="c2105-109">Hesap yönetimi giriş sayfası aşağıdaki modülleri kullanır:</span><span class="sxs-lookup"><span data-stu-id="c2105-109">The account management landing page uses the following modules:</span></span>

- <span data-ttu-id="c2105-110">**Konteyner** - Tüm hesap yönetimi giriş sayfası modülleri bir kapsayıcı içinde yer almalıdır.</span><span class="sxs-lookup"><span data-stu-id="c2105-110">**Container** - All account management landing page modules should be placed within a container.</span></span> 
- <span data-ttu-id="c2105-111">**Hesap karşılama kutucuğu** – bu modül, hesap yönetimi sayfasında hoş geldiniz iletisi sağlamak için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="c2105-111">**Account welcome tile** – This module is used to provide a welcome message on the account management page.</span></span> <span data-ttu-id="c2105-112">Başlığa ilişkin özellikleri içerir.</span><span class="sxs-lookup"><span data-stu-id="c2105-112">It includes properties for the heading.</span></span>
- <span data-ttu-id="c2105-113">**Hesap genel kutucuğu** -bu modül, "Sipariş geçmişi" veya "Profilim" sayfaları gibi hesap yönetimi sayfalarına başlık ve bağlantı sağlamak için kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="c2105-113">**Account generic tile** - This module can be used to provide headings and links to account management pages, such as the "Order history" or "My profile" pages.</span></span> <span data-ttu-id="c2105-114">Genel döşeme modülü herhangi bir sayfa için bir kutucuğu yapılandırmak amacıyla kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="c2105-114">The generic tile module can be used to configure a tile for any page.</span></span> <span data-ttu-id="c2105-115">Fabrikam'da, bu modül hesap yönetimi giriş sayfasındaki "Sipariş geçmişi" ve "Profilim" sayfa bağlantıları için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="c2105-115">In Fabrikam, this module is used for "Order history" and "My profile" page links on the account management landing page.</span></span>
- <span data-ttu-id="c2105-116">**Hesap istek listesi kutucuğu** – bu modül, müşterinin istek listesindeki maddelerin özetini sağlamak için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="c2105-116">**Account wishlist tile** – This module is used to provide a summary of the items on the customer's wish list.</span></span> <span data-ttu-id="c2105-117">Örneğin, "İstek listenizde 10 öğe var" olabilir.</span><span class="sxs-lookup"><span data-stu-id="c2105-117">For example, it might state, "You have 10 items in your wish list."</span></span> <span data-ttu-id="c2105-118">Başlık, başlık için özellikleri ve "Ayrıntıları görüntüle" bağlantısı özelliklerini içerir.</span><span class="sxs-lookup"><span data-stu-id="c2105-118">It includes properties for the heading and the "View details" link.</span></span> <span data-ttu-id="c2105-119">"Ayrıntıları Görüntüle" bağlantısı istek listesi sayfasına yeniden yönlendirilecek şekilde yapılandırılmalıdır.</span><span class="sxs-lookup"><span data-stu-id="c2105-119">The "View details" link should be configured to redirect to the wish list page.</span></span> 
- <span data-ttu-id="c2105-120">**Hesap adresi kutucuğu** – bu modül, Kullanıcı adreslerinin özetini sağlamak için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="c2105-120">**Account address tile** – This module is used to provide a summary of the user's addresses.</span></span> <span data-ttu-id="c2105-121">Örneğin, "Hesabınıza 2 adres eklendi" durumu olabilir.</span><span class="sxs-lookup"><span data-stu-id="c2105-121">For example, it might state, "You have 2 addresses added to your account."</span></span> <span data-ttu-id="c2105-122">Başlık, başlık için özellikleri ve "Ayrıntıları görüntüle" bağlantısı özelliklerini içerir.</span><span class="sxs-lookup"><span data-stu-id="c2105-122">It includes properties for the heading and the "View details" link.</span></span> <span data-ttu-id="c2105-123">"Ayrıntıları Görüntüle" bağlantısı kullanıcı adresi sayfasına yeniden yönlendirilecek şekilde konfigüre edilmelidir.</span><span class="sxs-lookup"><span data-stu-id="c2105-123">The "View details" link should be configured to redirect to the user address page.</span></span>
- <span data-ttu-id="c2105-124">**Hesap bağlılık kutucuğu** – Bu modül, bağlılık programı bilgilerini görüntülemek ve bağlamak için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="c2105-124">**Account loyalty tile** – This module is used to display and link to loyalty program information.</span></span> <span data-ttu-id="c2105-125">Bu kutucuğun iki durumu vardır: bir durum, bir üye değilse, bağlılık programına katılma bağlantılarını gösterir.</span><span class="sxs-lookup"><span data-stu-id="c2105-125">This tile has two states: one state shows links to join a loyalty progam if the user is not a member already.</span></span> <span data-ttu-id="c2105-126">Diğer durum, kullanıcının zaten üye olduğunda bağlılık programı ayrıntıları sayfasını görüntülemek için bağlantıları gösterir.</span><span class="sxs-lookup"><span data-stu-id="c2105-126">The other state shows links to view the loyalty details page when the user is already a member.</span></span> <span data-ttu-id="c2105-127">Özellikler başlığı, "Kaydol" bağlantısı ve "Bağlılık programını görüntüle" bağlantısını içerir.</span><span class="sxs-lookup"><span data-stu-id="c2105-127">Properties include the heading, the "Sign-up" link, and the "View loyalty" link.</span></span> <span data-ttu-id="c2105-128">"Bağlılık programını görüntüle" bağlantısı bağlılık sayfasına yeniden yönlendirilecek şekilde yapılandırılmalıdır.</span><span class="sxs-lookup"><span data-stu-id="c2105-128">The "View loyalty" link should be configured to redirect to the loyalty page.</span></span> <span data-ttu-id="c2105-129">"Üye olun" bağlantısı, kullanıcıların bağlılık programına katılabilecek bir sayfaya yeniden yönlendirilecek şekilde yapılandırılmalıdır.</span><span class="sxs-lookup"><span data-stu-id="c2105-129">The "Sign-up" link should be configured to redirect to a page where users can join the loyalty program.</span></span> 

### <a name="order-history-page"></a><span data-ttu-id="c2105-130">Sipariş geçmişi sayfası</span><span class="sxs-lookup"><span data-stu-id="c2105-130">Order history page</span></span>

<span data-ttu-id="c2105-131">Sipariş geçmişi sayfası, kullanıcının verdiği tüm son siparişleri göstermek için sipariş geçmişi modülünü kullanır.</span><span class="sxs-lookup"><span data-stu-id="c2105-131">The order history page uses the order history module to show all the recent orders that the user has placed.</span></span>

### <a name="order-details-page"></a><span data-ttu-id="c2105-132">Sipariş ayrıntıları sayfası</span><span class="sxs-lookup"><span data-stu-id="c2105-132">Order details page</span></span>

<span data-ttu-id="c2105-133">Sipariş Ayrıntıları sayfası her sipariş için ayrıntılı bilgi sağlar ve sipariş geçmişi sayfasından erişilir.</span><span class="sxs-lookup"><span data-stu-id="c2105-133">The order details page provides detailed information for each order and is accessed from the order history page.</span></span> <span data-ttu-id="c2105-134">Sipariş ayrıntılarını almak için satış kodu veya işlem kodunun gerekli olmasını gerektiren sipariş ayrıntıları modülünü kullanır.</span><span class="sxs-lookup"><span data-stu-id="c2105-134">It uses the order details module, which requires the sales ID or transaction ID to retrieve the order details.</span></span>

### <a name="user-profile-page"></a><span data-ttu-id="c2105-135">Kullanıcı profil sayfası</span><span class="sxs-lookup"><span data-stu-id="c2105-135">User profile page</span></span>

<span data-ttu-id="c2105-136">Kullanıcı profili sayfası kullanıcının adı ve e-posta adresi gibi kullanıcı hesabı ayrıntılarını gösterir.</span><span class="sxs-lookup"><span data-stu-id="c2105-136">The user profile page shows user account details, such as a user's name and email address.</span></span> <span data-ttu-id="c2105-137">Kullanıcı profili ayrıntılarını ve Kullanıcı profili düzenleme modüllerini kullanır.</span><span class="sxs-lookup"><span data-stu-id="c2105-137">It uses the user profile details and user profile edit modules.</span></span> <span data-ttu-id="c2105-138">Ancak e-posta adresi kaldırılamaz, düzenlenebilir.</span><span class="sxs-lookup"><span data-stu-id="c2105-138">Although the email address can't be removed, it can be edited.</span></span> <span data-ttu-id="c2105-139">Kullanıcı profili sayfası, kullanıcının öneri listelerinin kişiselleştirmesi gibi belirli özellikleri kabul etmesini veya devre dışı olmasını etkinleştiren Kullanıcı tercihlerini de gösterir.</span><span class="sxs-lookup"><span data-stu-id="c2105-139">The user profile page also shows user preferences that enable a user to opt in or opt out from certain features, such as personalization of recommendation lists.</span></span> 

### <a name="user-address-page"></a><span data-ttu-id="c2105-140">Kullanıcı adresi sayfası</span><span class="sxs-lookup"><span data-stu-id="c2105-140">User address page</span></span>

<span data-ttu-id="c2105-141">Kullanıcı adresi sayfası, kullanıcı hesabıyla ilişkili adreslerin listesini gösterir.</span><span class="sxs-lookup"><span data-stu-id="c2105-141">The user address page shows the list of addresses that are associated with the user account.</span></span> <span data-ttu-id="c2105-142">Kullanıcı bu adresleri kullanıma alma sırasında sağladı veya doğrudan bu sayfaya ekledi.</span><span class="sxs-lookup"><span data-stu-id="c2105-142">The user either provided these addresses during checkout or added them directly on  this page.</span></span> <span data-ttu-id="c2105-143">Kullanıcı Adres modülü, adres ekleme ve düzenleme, birincil adresi belirleme ve varolan adresleri sayfada işleme seçeneğini kullanır.</span><span class="sxs-lookup"><span data-stu-id="c2105-143">The user address module is used add and edit addresses, set the primary address, and render existing addresses on the page.</span></span>

### <a name="wish-list-page"></a><span data-ttu-id="c2105-144">İstek listesi sayfası</span><span class="sxs-lookup"><span data-stu-id="c2105-144">Wish list page</span></span>

<span data-ttu-id="c2105-145">İstek listesi sayfası, müşterinin istek listesine eklenen maddeleri gösterir.</span><span class="sxs-lookup"><span data-stu-id="c2105-145">The wish list page shows the items that have been added to the customer's wish list.</span></span> <span data-ttu-id="c2105-146">Liste öğelerini oluşturmak için, istek listesi modülünü kullanır.</span><span class="sxs-lookup"><span data-stu-id="c2105-146">It uses the wish list module to render wish list items.</span></span>

### <a name="loyalty-page"></a><span data-ttu-id="c2105-147">Bağlılık programı sayfası</span><span class="sxs-lookup"><span data-stu-id="c2105-147">Loyalty page</span></span>

<span data-ttu-id="c2105-148">Bağlılık programı sayfası müşterilerin, eğer halihazırda üyelerse, bağlılık programı ayrıntılarını görmelerini sağlar.</span><span class="sxs-lookup"><span data-stu-id="c2105-148">The loyalty page lets customers view their loyalty details if they are already loyalty program members.</span></span> <span data-ttu-id="c2105-149">Ayrıca, son hareketlerde kazanılan ve bunlar tarafından kullanılan puanları de görüntüleyebilirler.</span><span class="sxs-lookup"><span data-stu-id="c2105-149">They can also view the points that they have earned and redeemed in recent transactions.</span></span> <span data-ttu-id="c2105-150">Sayfa bağlılık programı ayrıntılarını gösterimi için bağlılık programı Ayrıntılar modülünü kullanır.</span><span class="sxs-lookup"><span data-stu-id="c2105-150">The page uses the loyalty details module to showcase the loyalty details.</span></span> 

<span data-ttu-id="c2105-151">Bağlılık programı programına katılmak için, bağlılık programı kayıt ve bağlılık programı şartları modülleriyle bir pazarlama sayfası oluşturulabilir.</span><span class="sxs-lookup"><span data-stu-id="c2105-151">To join loyalty program, a marketing page can be created with loyalty sign up and loyalty terms modules.</span></span> <span data-ttu-id="c2105-152">Kullanıcı bir bağlılık programı üyesi değilse, bu modüller kullanıcının kaydolmasını sağlayacaktır.</span><span class="sxs-lookup"><span data-stu-id="c2105-152">If the user is not a member of a loyalty program, these modules will enable the user to sign up.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="c2105-153">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="c2105-153">Additional resources</span></span>

[<span data-ttu-id="c2105-154">Modül kitaplığına genel bakış</span><span class="sxs-lookup"><span data-stu-id="c2105-154">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="c2105-155">Kapsayıcı modülü</span><span class="sxs-lookup"><span data-stu-id="c2105-155">Container module</span></span>](add-container-module.md)

[<span data-ttu-id="c2105-156">Satın alma kutusu modülü</span><span class="sxs-lookup"><span data-stu-id="c2105-156">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="c2105-157">Alışveriş sepeti modülü</span><span class="sxs-lookup"><span data-stu-id="c2105-157">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="c2105-158">Ödeme yapma modülü</span><span class="sxs-lookup"><span data-stu-id="c2105-158">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="c2105-159">Sipariş onayı modülü</span><span class="sxs-lookup"><span data-stu-id="c2105-159">Order confirmation module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="c2105-160">Üst bilgi modülü</span><span class="sxs-lookup"><span data-stu-id="c2105-160">Header module</span></span>](author-header-module.md)

[<span data-ttu-id="c2105-161">Alt bilgi modülü</span><span class="sxs-lookup"><span data-stu-id="c2105-161">Footer module</span></span>](author-footer-module.md)
