---
title: Hesap yönetimi sayfaları ve modülleri
description: Bu konu, Microsoft Dynamics 365 Commerce'ta hesap yönetimi sayfalarını ve modüllerini kapsamaktadır.
author: v-chgri
manager: annbe
ms.date: 10/01/2019
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
ms.openlocfilehash: 3986505a7e0e8d33d5b8ff2c06f493335731a8d9
ms.sourcegitcommit: 3a4e137ef3a96ba0a58c5352f4a3b57467ace9ae
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/11/2019
ms.locfileid: "2785405"
---
# <a name="account-management-pages-and-modules"></a><span data-ttu-id="801ff-103">Hesap yönetimi sayfaları ve modülleri</span><span class="sxs-lookup"><span data-stu-id="801ff-103">Account management pages and modules</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="801ff-104">Bu konu, Microsoft Dynamics 365 Commerce'ta hesap yönetimi sayfalarını ve modüllerini kapsamaktadır.</span><span class="sxs-lookup"><span data-stu-id="801ff-104">This topic covers account management pages and modules in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="801ff-105">Genel Bakış</span><span class="sxs-lookup"><span data-stu-id="801ff-105">Overview</span></span>

<span data-ttu-id="801ff-106">Hesap yönetimi, Dynamics 365 Commerce'teki Kullanıcı hesabı ile ilgili bilgileri yönetmek için kullanılan bir grup sayfayı gösterir.</span><span class="sxs-lookup"><span data-stu-id="801ff-106">Account management refers to a group of pages that is used to manage user account–related information in Dynamics 365 Commerce.</span></span> <span data-ttu-id="801ff-107">Hesap yönetimi sayfaları, hesap yönetimi giriş sayfası, kullanıcı profili sayfası, kullanıcı adresi sayfası, sipariş geçmişi sayfası, sipariş ayrıntıları sayfası, bağlılık programı sayfası ve istek listesi sayfasını içerir.</span><span class="sxs-lookup"><span data-stu-id="801ff-107">Account management pages include the account management landing page, user profile page, user address page, order history page, order details page, loyalty page, and wish list page.</span></span>

### <a name="account-management-landing-page"></a><span data-ttu-id="801ff-108">Hesap yönetimi giriş sayfası</span><span class="sxs-lookup"><span data-stu-id="801ff-108">Account management landing page</span></span>

<span data-ttu-id="801ff-109">Hesap yönetimi giriş sayfası aşağıdaki modülleri kullanır:</span><span class="sxs-lookup"><span data-stu-id="801ff-109">The account management landing page uses the following modules:</span></span>

- <span data-ttu-id="801ff-110">**İçerik yerleşimi** – bu modül hesap yönetimi giriş sayfasındaki tüm modülleri tutan bir konteyner modülüdür.</span><span class="sxs-lookup"><span data-stu-id="801ff-110">**Content placement** – This module is a container module that holds all the modules on the account management landing page.</span></span>
- <span data-ttu-id="801ff-111">**Hesap karşılama öğesi** – bu modül, hesap yönetimi sayfasında hoş geldiniz iletisi sağlamak için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="801ff-111">**Account welcome item** – This module is used to provide a welcome message on the account management page.</span></span> <span data-ttu-id="801ff-112">Başlık ve döşeme boyutu özelliklerini içerir.</span><span class="sxs-lookup"><span data-stu-id="801ff-112">It includes properties for the heading and the tile size.</span></span> <span data-ttu-id="801ff-113">**Döşeme boyutu** özelliği, içerik yerleştirme modülündeki modülün genişliğini tanımlar.</span><span class="sxs-lookup"><span data-stu-id="801ff-113">The **Tile size** property defines the width of the module in the content placement module.</span></span> <span data-ttu-id="801ff-114">Değerler **1** ile **12**arasında değişir (burada **12**, içerik yerleşimi konteynerin tam genişliğini gösterir).</span><span class="sxs-lookup"><span data-stu-id="801ff-114">Values range from **1** through **12**, where **12** represents the full width of the content placement container.</span></span>
- <span data-ttu-id="801ff-115">**Hesap düzeni yerleşim maddesi** – bu modül, Kullanıcı hesabı tarafından verilen sipariş sayısının özetini sağlamak için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="801ff-115">**Account order placement item** – This module is used to provide a summary of the number of orders that have been placed by the user account.</span></span> <span data-ttu-id="801ff-116">Başlık, döşeme boyutu ve "ayrıntıları göster" bağlantısı özelliklerini içerir.</span><span class="sxs-lookup"><span data-stu-id="801ff-116">It includes properties for the heading, the tile size, and the "view details" link.</span></span> <span data-ttu-id="801ff-117">"Ayrıntıları görüntüle" bağlantısı sipariş geçmişi sayfasına yeniden yönlendirilecek şekilde konfigüre edilmelidir.</span><span class="sxs-lookup"><span data-stu-id="801ff-117">The "view details" link should be configured to redirect to the order history page.</span></span>
- <span data-ttu-id="801ff-118">**Hesap profili yerleştirme öğesi** – bu modül, Kullanıcı profilinin özetini sağlamak için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="801ff-118">**Account profile placement item** – This module is used to provide a summary of the user profile.</span></span> <span data-ttu-id="801ff-119">Başlık, döşeme boyutu ve "ayrıntıları göster" bağlantısı özelliklerini içerir.</span><span class="sxs-lookup"><span data-stu-id="801ff-119">It includes properties for the heading, the tile size, and the "view details" link.</span></span> <span data-ttu-id="801ff-120">"Ayrıntıları görüntüle" bağlantısı kullanıcı profili sayfasına yeniden yönlendirilecek şekilde konfigüre edilmelidir.</span><span class="sxs-lookup"><span data-stu-id="801ff-120">The "view details" link should be configured to redirect to the user profile page.</span></span>
- <span data-ttu-id="801ff-121">**Hesap istek listesi maddesi** – bu modül, müşterinin istek listesindeki maddelerin özetini sağlamak için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="801ff-121">**Account wishlist item** – This module is used to provide a summary of the items on the customer's wish list.</span></span> <span data-ttu-id="801ff-122">Örneğin, "İstek listenizde 10 öğe var" olabilir.</span><span class="sxs-lookup"><span data-stu-id="801ff-122">For example, it might state, "You have 10 items in your wish list."</span></span> <span data-ttu-id="801ff-123">Başlık, döşeme boyutu ve "ayrıntıları göster" bağlantısı özelliklerini içerir.</span><span class="sxs-lookup"><span data-stu-id="801ff-123">It includes properties for the heading, the tile size, and the "view details" link.</span></span> <span data-ttu-id="801ff-124">"Ayrıntıları görüntüle" bağlantısı istek listesi sayfasına yeniden yönlendirilecek şekilde konfigüre edilmelidir.</span><span class="sxs-lookup"><span data-stu-id="801ff-124">The "view details" link should be configured to redirect to the wish list page.</span></span>
- <span data-ttu-id="801ff-125">**Hesap adresi öğesi** – bu modül, Kullanıcı adreslerinin özetini sağlamak için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="801ff-125">**Account address item** – This module is used to provide a summary of the user's addresses.</span></span> <span data-ttu-id="801ff-126">Örneğin, "Hesabınıza 2 adres eklendi" durumu olabilir.</span><span class="sxs-lookup"><span data-stu-id="801ff-126">For example, it might state, "You have 2 addresses added to your account."</span></span> <span data-ttu-id="801ff-127">Başlık, döşeme boyutu ve "ayrıntıları göster" bağlantısı özelliklerini içerir.</span><span class="sxs-lookup"><span data-stu-id="801ff-127">It includes properties for the heading, the tile size, and the "view details" link.</span></span> <span data-ttu-id="801ff-128">"Ayrıntıları görüntüle" bağlantısı kullanıcı adresi sayfasına yeniden yönlendirilecek şekilde konfigüre edilmelidir.</span><span class="sxs-lookup"><span data-stu-id="801ff-128">The "view details" link should be configured to redirect to the user address page.</span></span>
- <span data-ttu-id="801ff-129">**Hesap bağlılık maddesi** – Bu modül, bağlılık programı bilgilerini göstermek ve bağlamak için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="801ff-129">**Account loyalty item** – This module is used to show and link to loyalty program information.</span></span> <span data-ttu-id="801ff-130">Başlık, döşeme boyutu, "ayrıntıları göster" ve "üye ol" bağlantısı özelliklerini içerir.</span><span class="sxs-lookup"><span data-stu-id="801ff-130">It includes properties for the heading, the tile size, the "view details" link, and the "become a member" link.</span></span> <span data-ttu-id="801ff-131">"Ayrıntıları görüntüle" bağlantısı bağlılık sayfasına yeniden yönlendirilecek şekilde konfigüre edilmelidir.</span><span class="sxs-lookup"><span data-stu-id="801ff-131">The "view details" link should be configured to redirect to the loyalty page.</span></span> <span data-ttu-id="801ff-132">"Üye olun" bağlantısı, kullanıcıların bağlılık programına katılabilecek bir sayfaya yeniden yönlendirilecek şekilde konfigüre edilmelidir.</span><span class="sxs-lookup"><span data-stu-id="801ff-132">The "become a member" link should be configured to redirect to a page where users can join the loyalty program.</span></span>

### <a name="order-history-page"></a><span data-ttu-id="801ff-133">Sipariş geçmişi sayfası</span><span class="sxs-lookup"><span data-stu-id="801ff-133">Order history page</span></span>

<span data-ttu-id="801ff-134">Sipariş geçmişi sayfası, kullanıcının verdiği tüm son siparişleri göstermek için sipariş geçmişi modülünü kullanır.</span><span class="sxs-lookup"><span data-stu-id="801ff-134">The order history page uses the order history module to show all the recent orders that the user has placed.</span></span>

### <a name="order-details-page"></a><span data-ttu-id="801ff-135">Sipariş ayrıntıları sayfası</span><span class="sxs-lookup"><span data-stu-id="801ff-135">Order details page</span></span>

<span data-ttu-id="801ff-136">Sipariş Ayrıntıları sayfası her sipariş için ayrıntılı bilgi sağlar ve sipariş geçmişi sayfasından erişilir.</span><span class="sxs-lookup"><span data-stu-id="801ff-136">The order details page provides detailed information for each order and is accessed from the order history page.</span></span> <span data-ttu-id="801ff-137">Sipariş ayrıntılarını almak için satış kodu veya işlem kodunun gerekli olmasını gerektiren sipariş ayrıntıları modülünü kullanır.</span><span class="sxs-lookup"><span data-stu-id="801ff-137">It uses the order details module, which requires the sales ID or transaction ID to retrieve the order details.</span></span>

### <a name="user-profile-page"></a><span data-ttu-id="801ff-138">Kullanıcı profil sayfası</span><span class="sxs-lookup"><span data-stu-id="801ff-138">User profile page</span></span>

<span data-ttu-id="801ff-139">Kullanıcı profili sayfası kullanıcının adı ve e-posta adresi gibi kullanıcı hesabı ayrıntılarını gösterir.</span><span class="sxs-lookup"><span data-stu-id="801ff-139">The user profile page shows user account details, such as user's name and email address.</span></span> <span data-ttu-id="801ff-140">Kullanıcı profili modülünü kullanır.</span><span class="sxs-lookup"><span data-stu-id="801ff-140">It uses the user profile module.</span></span> <span data-ttu-id="801ff-141">Ancak e-posta adresi kaldırılamaz, düzenlenebilir.</span><span class="sxs-lookup"><span data-stu-id="801ff-141">Although the email address can't be removed, it can be edited.</span></span>

### <a name="user-address-page"></a><span data-ttu-id="801ff-142">Kullanıcı adresi sayfası</span><span class="sxs-lookup"><span data-stu-id="801ff-142">User address page</span></span>

<span data-ttu-id="801ff-143">Kullanıcı adresi sayfası, kullanıcı hesabıyla ilişkili adreslerin listesini gösterir.</span><span class="sxs-lookup"><span data-stu-id="801ff-143">The user address page shows the list of addresses that are associated with the user account.</span></span> <span data-ttu-id="801ff-144">Kullanıcı bu adresleri kullanıma alma sırasında sağladı veya doğrudan bu sayfaya ekledi.</span><span class="sxs-lookup"><span data-stu-id="801ff-144">The user either provided these addresses during checkout or added them directly on  this page.</span></span> <span data-ttu-id="801ff-145">Kullanıcı Adres modülü, adres ekleme ve düzenleme, birincil adresi belirleme ve varolan adresleri sayfada işleme seçeneğini kullanır.</span><span class="sxs-lookup"><span data-stu-id="801ff-145">The user address module is used add and edit addresses, set the primary address, and render existing addresses on the page.</span></span>

### <a name="wish-list-page"></a><span data-ttu-id="801ff-146">İstek listesi sayfası</span><span class="sxs-lookup"><span data-stu-id="801ff-146">Wish list page</span></span>

<span data-ttu-id="801ff-147">İstek listesi sayfası, müşterinin istek listesine eklenen maddeleri gösterir.</span><span class="sxs-lookup"><span data-stu-id="801ff-147">The wish list page shows the items that have been added to the customer's wish list.</span></span> <span data-ttu-id="801ff-148">Liste öğelerini oluşturmak için, istek listesi modülünü kullanır.</span><span class="sxs-lookup"><span data-stu-id="801ff-148">It uses the wish list module to render wish list items.</span></span>

### <a name="loyalty-page"></a><span data-ttu-id="801ff-149">Bağlılık programı sayfası</span><span class="sxs-lookup"><span data-stu-id="801ff-149">Loyalty page</span></span>

<span data-ttu-id="801ff-150">Bağlılık programı, müşterilerinin bir bağlılık programına katılmasına veya zaten bağlılık programı üyesi olduklarında Program ayrıntılarını görüntülemesine olanak tanır.</span><span class="sxs-lookup"><span data-stu-id="801ff-150">The loyalty page lets customers join a loyalty program or, if they are already loyalty program members, view their program details.</span></span> <span data-ttu-id="801ff-151">Ayrıca, son hareketlerde kazanılan ve bunlar tarafından kullanılan puanları de görüntüleyebilirler.</span><span class="sxs-lookup"><span data-stu-id="801ff-151">They can also view the points that they have earned and redeemed in recent transactions.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="801ff-152">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="801ff-152">Additional resources</span></span>

[<span data-ttu-id="801ff-153">Başlangıç paketine genel bakış</span><span class="sxs-lookup"><span data-stu-id="801ff-153">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="801ff-154">Konteyner modülü</span><span class="sxs-lookup"><span data-stu-id="801ff-154">Container module</span></span>](add-container-module.md)

[<span data-ttu-id="801ff-155">Satın alma kutusu modülü</span><span class="sxs-lookup"><span data-stu-id="801ff-155">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="801ff-156">Sepet modülü</span><span class="sxs-lookup"><span data-stu-id="801ff-156">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="801ff-157">Ödeme modülü</span><span class="sxs-lookup"><span data-stu-id="801ff-157">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="801ff-158">Sipariş onayı modülü</span><span class="sxs-lookup"><span data-stu-id="801ff-158">Order confirmation module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="801ff-159">Üst bilgi modülü</span><span class="sxs-lookup"><span data-stu-id="801ff-159">Header module</span></span>](author-header-module.md)

[<span data-ttu-id="801ff-160">Alt bilgi modülü</span><span class="sxs-lookup"><span data-stu-id="801ff-160">Footer module</span></span>](author-footer-module.md)
