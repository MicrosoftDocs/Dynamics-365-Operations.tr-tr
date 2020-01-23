---
title: Hesap yönetimi sayfaları ve modülleri
description: Bu konu, Microsoft Dynamics 365 Commerce'ta hesap yönetimi sayfalarını ve modüllerini kapsamaktadır.
author: v-chgri
manager: annbe
ms.date: 12/02/2019
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
ms.openlocfilehash: f9fc3731cd9d21294b0161e1d419f255096d7790
ms.sourcegitcommit: 96bfc20eb748f4090a2b5e1ff9f54997d5a5d359
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 12/04/2019
ms.locfileid: "2885821"
---
# <a name="account-management-pages-and-modules"></a><span data-ttu-id="7b150-103">Hesap yönetimi sayfaları ve modülleri</span><span class="sxs-lookup"><span data-stu-id="7b150-103">Account management pages and modules</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="7b150-104">Bu konu, Microsoft Dynamics 365 Commerce'ta hesap yönetimi sayfalarını ve modüllerini kapsamaktadır.</span><span class="sxs-lookup"><span data-stu-id="7b150-104">This topic covers account management pages and modules in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="7b150-105">Genel Bakış</span><span class="sxs-lookup"><span data-stu-id="7b150-105">Overview</span></span>

<span data-ttu-id="7b150-106">Hesap yönetimi, Dynamics 365 Commerce'teki Kullanıcı hesabı ile ilgili bilgileri yönetmek için kullanılan bir grup sayfayı gösterir.</span><span class="sxs-lookup"><span data-stu-id="7b150-106">Account management refers to a group of pages that is used to manage user account–related information in Dynamics 365 Commerce.</span></span> <span data-ttu-id="7b150-107">Hesap yönetimi sayfaları, hesap yönetimi giriş sayfası, kullanıcı profili sayfası, kullanıcı adresi sayfası, sipariş geçmişi sayfası, sipariş ayrıntıları sayfası, bağlılık programı sayfası ve istek listesi sayfasını içerir.</span><span class="sxs-lookup"><span data-stu-id="7b150-107">Account management pages include the account management landing page, user profile page, user address page, order history page, order details page, loyalty page, and wish list page.</span></span>

### <a name="account-management-landing-page"></a><span data-ttu-id="7b150-108">Hesap yönetimi giriş sayfası</span><span class="sxs-lookup"><span data-stu-id="7b150-108">Account management landing page</span></span>

<span data-ttu-id="7b150-109">Hesap yönetimi giriş sayfası aşağıdaki modülleri kullanır:</span><span class="sxs-lookup"><span data-stu-id="7b150-109">The account management landing page uses the following modules:</span></span>

- <span data-ttu-id="7b150-110">**İçerik yerleşimi** – bu modül hesap yönetimi giriş sayfasındaki tüm modülleri tutan bir konteyner modülüdür.</span><span class="sxs-lookup"><span data-stu-id="7b150-110">**Content placement** – This module is a container module that holds all the modules on the account management landing page.</span></span>
- <span data-ttu-id="7b150-111">**Hesap karşılama öğesi** – bu modül, hesap yönetimi sayfasında hoş geldiniz iletisi sağlamak için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="7b150-111">**Account welcome item** – This module is used to provide a welcome message on the account management page.</span></span> <span data-ttu-id="7b150-112">Başlık ve döşeme boyutu özelliklerini içerir.</span><span class="sxs-lookup"><span data-stu-id="7b150-112">It includes properties for the heading and the tile size.</span></span> <span data-ttu-id="7b150-113">**Döşeme boyutu** özelliği, içerik yerleştirme modülündeki modülün genişliğini tanımlar.</span><span class="sxs-lookup"><span data-stu-id="7b150-113">The **Tile size** property defines the width of the module in the content placement module.</span></span> <span data-ttu-id="7b150-114">Değerler **1** ile **12**arasında değişir (burada **12**, içerik yerleşimi konteynerin tam genişliğini gösterir).</span><span class="sxs-lookup"><span data-stu-id="7b150-114">Values range from **1** through **12**, where **12** represents the full width of the content placement container.</span></span>
- <span data-ttu-id="7b150-115">**Hesap düzeni yerleşim maddesi** – bu modül, Kullanıcı hesabı tarafından verilen sipariş sayısının özetini sağlamak için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="7b150-115">**Account order placement item** – This module is used to provide a summary of the number of orders that have been placed by the user account.</span></span> <span data-ttu-id="7b150-116">Başlık, döşeme boyutu ve "ayrıntıları göster" bağlantısı özelliklerini içerir.</span><span class="sxs-lookup"><span data-stu-id="7b150-116">It includes properties for the heading, the tile size, and the "view details" link.</span></span> <span data-ttu-id="7b150-117">"Ayrıntıları görüntüle" bağlantısı sipariş geçmişi sayfasına yeniden yönlendirilecek şekilde konfigüre edilmelidir.</span><span class="sxs-lookup"><span data-stu-id="7b150-117">The "view details" link should be configured to redirect to the order history page.</span></span>
- <span data-ttu-id="7b150-118">**Hesap profili yerleştirme öğesi** – bu modül, Kullanıcı profilinin özetini sağlamak için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="7b150-118">**Account profile placement item** – This module is used to provide a summary of the user profile.</span></span> <span data-ttu-id="7b150-119">Başlık, döşeme boyutu ve "ayrıntıları göster" bağlantısı özelliklerini içerir.</span><span class="sxs-lookup"><span data-stu-id="7b150-119">It includes properties for the heading, the tile size, and the "view details" link.</span></span> <span data-ttu-id="7b150-120">"Ayrıntıları görüntüle" bağlantısı kullanıcı profili sayfasına yeniden yönlendirilecek şekilde konfigüre edilmelidir.</span><span class="sxs-lookup"><span data-stu-id="7b150-120">The "view details" link should be configured to redirect to the user profile page.</span></span>
- <span data-ttu-id="7b150-121">**Hesap istek listesi maddesi** – bu modül, müşterinin istek listesindeki maddelerin özetini sağlamak için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="7b150-121">**Account wishlist item** – This module is used to provide a summary of the items on the customer's wish list.</span></span> <span data-ttu-id="7b150-122">Örneğin, "İstek listenizde 10 öğe var" olabilir.</span><span class="sxs-lookup"><span data-stu-id="7b150-122">For example, it might state, "You have 10 items in your wish list."</span></span> <span data-ttu-id="7b150-123">Başlık, döşeme boyutu ve "ayrıntıları göster" bağlantısı özelliklerini içerir.</span><span class="sxs-lookup"><span data-stu-id="7b150-123">It includes properties for the heading, the tile size, and the "view details" link.</span></span> <span data-ttu-id="7b150-124">"Ayrıntıları görüntüle" bağlantısı istek listesi sayfasına yeniden yönlendirilecek şekilde konfigüre edilmelidir.</span><span class="sxs-lookup"><span data-stu-id="7b150-124">The "view details" link should be configured to redirect to the wish list page.</span></span>
- <span data-ttu-id="7b150-125">**Hesap adresi öğesi** – bu modül, Kullanıcı adreslerinin özetini sağlamak için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="7b150-125">**Account address item** – This module is used to provide a summary of the user's addresses.</span></span> <span data-ttu-id="7b150-126">Örneğin, "Hesabınıza 2 adres eklendi" durumu olabilir.</span><span class="sxs-lookup"><span data-stu-id="7b150-126">For example, it might state, "You have 2 addresses added to your account."</span></span> <span data-ttu-id="7b150-127">Başlık, döşeme boyutu ve "ayrıntıları göster" bağlantısı özelliklerini içerir.</span><span class="sxs-lookup"><span data-stu-id="7b150-127">It includes properties for the heading, the tile size, and the "view details" link.</span></span> <span data-ttu-id="7b150-128">"Ayrıntıları görüntüle" bağlantısı kullanıcı adresi sayfasına yeniden yönlendirilecek şekilde konfigüre edilmelidir.</span><span class="sxs-lookup"><span data-stu-id="7b150-128">The "view details" link should be configured to redirect to the user address page.</span></span>
- <span data-ttu-id="7b150-129">**Hesap bağlılık maddesi** – Bu modül, bağlılık programı bilgilerini göstermek ve bağlamak için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="7b150-129">**Account loyalty item** – This module is used to show and link to loyalty program information.</span></span> <span data-ttu-id="7b150-130">Başlık, döşeme boyutu, "ayrıntıları göster" ve "üye ol" bağlantısı özelliklerini içerir.</span><span class="sxs-lookup"><span data-stu-id="7b150-130">It includes properties for the heading, the tile size, the "view details" link, and the "become a member" link.</span></span> <span data-ttu-id="7b150-131">"Ayrıntıları görüntüle" bağlantısı bağlılık sayfasına yeniden yönlendirilecek şekilde konfigüre edilmelidir.</span><span class="sxs-lookup"><span data-stu-id="7b150-131">The "view details" link should be configured to redirect to the loyalty page.</span></span> <span data-ttu-id="7b150-132">"Üye olun" bağlantısı, kullanıcıların bağlılık programına katılabilecek bir sayfaya yeniden yönlendirilecek şekilde konfigüre edilmelidir.</span><span class="sxs-lookup"><span data-stu-id="7b150-132">The "become a member" link should be configured to redirect to a page where users can join the loyalty program.</span></span>

### <a name="order-history-page"></a><span data-ttu-id="7b150-133">Sipariş geçmişi sayfası</span><span class="sxs-lookup"><span data-stu-id="7b150-133">Order history page</span></span>

<span data-ttu-id="7b150-134">Sipariş geçmişi sayfası, kullanıcının verdiği tüm son siparişleri göstermek için sipariş geçmişi modülünü kullanır.</span><span class="sxs-lookup"><span data-stu-id="7b150-134">The order history page uses the order history module to show all the recent orders that the user has placed.</span></span>

### <a name="order-details-page"></a><span data-ttu-id="7b150-135">Sipariş ayrıntıları sayfası</span><span class="sxs-lookup"><span data-stu-id="7b150-135">Order details page</span></span>

<span data-ttu-id="7b150-136">Sipariş Ayrıntıları sayfası her sipariş için ayrıntılı bilgi sağlar ve sipariş geçmişi sayfasından erişilir.</span><span class="sxs-lookup"><span data-stu-id="7b150-136">The order details page provides detailed information for each order and is accessed from the order history page.</span></span> <span data-ttu-id="7b150-137">Sipariş ayrıntılarını almak için satış kodu veya işlem kodunun gerekli olmasını gerektiren sipariş ayrıntıları modülünü kullanır.</span><span class="sxs-lookup"><span data-stu-id="7b150-137">It uses the order details module, which requires the sales ID or transaction ID to retrieve the order details.</span></span>

### <a name="user-profile-page"></a><span data-ttu-id="7b150-138">Kullanıcı profil sayfası</span><span class="sxs-lookup"><span data-stu-id="7b150-138">User profile page</span></span>

<span data-ttu-id="7b150-139">Kullanıcı profili sayfası kullanıcının adı ve e-posta adresi gibi kullanıcı hesabı ayrıntılarını gösterir.</span><span class="sxs-lookup"><span data-stu-id="7b150-139">The user profile page shows user account details, such as a user's name and email address.</span></span> <span data-ttu-id="7b150-140">Kullanıcı profili modülünü kullanır.</span><span class="sxs-lookup"><span data-stu-id="7b150-140">It uses the user profile module.</span></span> <span data-ttu-id="7b150-141">Ancak e-posta adresi kaldırılamaz, düzenlenebilir.</span><span class="sxs-lookup"><span data-stu-id="7b150-141">Although the email address can't be removed, it can be edited.</span></span> <span data-ttu-id="7b150-142">Kullanıcı profili sayfası, kullanıcının öneri listelerinin kişiselleştirmesi gibi belirli özellikleri kabul etmesini veya devre dışı olmasını etkinleştiren Kullanıcı tercihlerini de gösterir.</span><span class="sxs-lookup"><span data-stu-id="7b150-142">The user profile page also shows user preferences that enable a user to opt in or opt out from certain features such as personalization of recommendation lists.</span></span> 

### <a name="user-address-page"></a><span data-ttu-id="7b150-143">Kullanıcı adresi sayfası</span><span class="sxs-lookup"><span data-stu-id="7b150-143">User address page</span></span>

<span data-ttu-id="7b150-144">Kullanıcı adresi sayfası, kullanıcı hesabıyla ilişkili adreslerin listesini gösterir.</span><span class="sxs-lookup"><span data-stu-id="7b150-144">The user address page shows the list of addresses that are associated with the user account.</span></span> <span data-ttu-id="7b150-145">Kullanıcı bu adresleri kullanıma alma sırasında sağladı veya doğrudan bu sayfaya ekledi.</span><span class="sxs-lookup"><span data-stu-id="7b150-145">The user either provided these addresses during checkout or added them directly on  this page.</span></span> <span data-ttu-id="7b150-146">Kullanıcı Adres modülü, adres ekleme ve düzenleme, birincil adresi belirleme ve varolan adresleri sayfada işleme seçeneğini kullanır.</span><span class="sxs-lookup"><span data-stu-id="7b150-146">The user address module is used add and edit addresses, set the primary address, and render existing addresses on the page.</span></span>

### <a name="wish-list-page"></a><span data-ttu-id="7b150-147">İstek listesi sayfası</span><span class="sxs-lookup"><span data-stu-id="7b150-147">Wish list page</span></span>

<span data-ttu-id="7b150-148">İstek listesi sayfası, müşterinin istek listesine eklenen maddeleri gösterir.</span><span class="sxs-lookup"><span data-stu-id="7b150-148">The wish list page shows the items that have been added to the customer's wish list.</span></span> <span data-ttu-id="7b150-149">Liste öğelerini oluşturmak için, istek listesi modülünü kullanır.</span><span class="sxs-lookup"><span data-stu-id="7b150-149">It uses the wish list module to render wish list items.</span></span>

### <a name="loyalty-page"></a><span data-ttu-id="7b150-150">Bağlılık programı sayfası</span><span class="sxs-lookup"><span data-stu-id="7b150-150">Loyalty page</span></span>

<span data-ttu-id="7b150-151">Bağlılık programı, müşterilerinin bir bağlılık programına katılmasına veya zaten bağlılık programı üyesi olduklarında Program ayrıntılarını görüntülemesine olanak tanır.</span><span class="sxs-lookup"><span data-stu-id="7b150-151">The loyalty page lets customers join a loyalty program or, if they are already loyalty program members, view their program details.</span></span> <span data-ttu-id="7b150-152">Ayrıca, son hareketlerde kazanılan ve bunlar tarafından kullanılan puanları de görüntüleyebilirler.</span><span class="sxs-lookup"><span data-stu-id="7b150-152">They can also view the points that they have earned and redeemed in recent transactions.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="7b150-153">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="7b150-153">Additional resources</span></span>

[<span data-ttu-id="7b150-154">Başlangıç paketine genel bakış</span><span class="sxs-lookup"><span data-stu-id="7b150-154">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="7b150-155">Konteyner modülü</span><span class="sxs-lookup"><span data-stu-id="7b150-155">Container module</span></span>](add-container-module.md)

[<span data-ttu-id="7b150-156">Satın alma kutusu modülü</span><span class="sxs-lookup"><span data-stu-id="7b150-156">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="7b150-157">Sepet modülü</span><span class="sxs-lookup"><span data-stu-id="7b150-157">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="7b150-158">Ödeme modülü</span><span class="sxs-lookup"><span data-stu-id="7b150-158">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="7b150-159">Sipariş onayı modülü</span><span class="sxs-lookup"><span data-stu-id="7b150-159">Order confirmation module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="7b150-160">Üst bilgi modülü</span><span class="sxs-lookup"><span data-stu-id="7b150-160">Header module</span></span>](author-header-module.md)

[<span data-ttu-id="7b150-161">Alt bilgi modülü</span><span class="sxs-lookup"><span data-stu-id="7b150-161">Footer module</span></span>](author-footer-module.md)
