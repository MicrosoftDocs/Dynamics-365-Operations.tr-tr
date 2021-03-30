---
title: Hesap yönetimi sayfalarına genel bakış
description: Bu konu, Microsoft Dynamics 365 Commerce'ta hesap yönetimi sayfalarına genel bakış sağlar.
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
ms.openlocfilehash: 4cd4ee3ef2b1c3538ec267fe12eef38d525f6a83
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5244827"
---
# <a name="account-management-pages-overview"></a><span data-ttu-id="e6088-103">Hesap yönetimi sayfalarına genel bakış</span><span class="sxs-lookup"><span data-stu-id="e6088-103">Account management pages overview</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="e6088-104">Bu konu, Microsoft Dynamics 365 Commerce'ta hesap yönetimi sayfalarına genel bakış sağlar.</span><span class="sxs-lookup"><span data-stu-id="e6088-104">This topic provides an overview of account management pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="e6088-105">Genel Bakış</span><span class="sxs-lookup"><span data-stu-id="e6088-105">Overview</span></span>

<span data-ttu-id="e6088-106">Hesap yönetimi sayfaları, müşterilerin kendi hesap ve siparişleriyle ilgili bilgileri görüntülemesine olanak tanır.</span><span class="sxs-lookup"><span data-stu-id="e6088-106">Account management pages let customers view information that is related to their account and orders.</span></span> <span data-ttu-id="e6088-107">Hesap yönetimi sayfaları, hesap yönetimi giriş sayfası, kullanıcı profili sayfaları, adresler, sipariş geçmişi sayfası, sipariş ayrıntıları sayfası, bağlılık programı puanları ve istek listesi sayfasını içerir.</span><span class="sxs-lookup"><span data-stu-id="e6088-107">Account management pages include the account management landing page, and pages for the user's profile, addresses, order history, order details, loyalty points, and wish list.</span></span>

### <a name="account-management-landing-page"></a><span data-ttu-id="e6088-108">Hesap yönetimi giriş sayfası</span><span class="sxs-lookup"><span data-stu-id="e6088-108">Account management landing page</span></span>

<span data-ttu-id="e6088-109">Bir müşteri oturum açıp **hesabımı** seçtiğinde hesap yönetimi giriş sayfası açılır.</span><span class="sxs-lookup"><span data-stu-id="e6088-109">When a customer signs in and selects **My Account**, the account management landing page is opened.</span></span> <span data-ttu-id="e6088-110">Bu sayfa, kullanıcı profili, siparişler, istek listesi, adresler, bağlılık programı puanları gibi hesapla ilgili tüm bilgilerin hızlı bir özetini sağlar.</span><span class="sxs-lookup"><span data-stu-id="e6088-110">This page provides a quick summary of all account-related information, such as the user's profile, orders, wish list, addresses, loyalty points.</span></span> <span data-ttu-id="e6088-111">Müşteri bu sayfadan, her alan için daha fazla ayrıntılara erişebilir.</span><span class="sxs-lookup"><span data-stu-id="e6088-111">From this page, the customer can access more details for each area.</span></span>

<span data-ttu-id="e6088-112">Aşağıdaki çizimde bir hesap yönetimi giriş sayfasının bir örneği gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="e6088-112">The following illustration shows an example of the account management landing page.</span></span>

![Hesap yönetimi giriş sayfası örneği](./media/Account-Management.PNG)

### <a name="my-profile-page"></a><span data-ttu-id="e6088-114">Profilim sayfası</span><span class="sxs-lookup"><span data-stu-id="e6088-114">My profile page</span></span>

<span data-ttu-id="e6088-115">**Profilim** sayfası, müşterinin adı ve telefon numarası gibi müşteri hesap bilgilerini gösterir.</span><span class="sxs-lookup"><span data-stu-id="e6088-115">The **My profile** page shows customer's account information, such as his or her name and phone number.</span></span> <span data-ttu-id="e6088-116">Müşteri bu sayfadaki kendi profil bilgilerini güncelleştirebilir.</span><span class="sxs-lookup"><span data-stu-id="e6088-116">The customer can update his or her profile information on this page.</span></span> <span data-ttu-id="e6088-117">Bu sayfa, pazarlama e-postasını tercih etme seçeneği gibi ek müşteri hesabı tercihleri içerecek şekilde özelleştirilebilir.</span><span class="sxs-lookup"><span data-stu-id="e6088-117">This page can be customized so that it includes additional customer account preferences, such as an option for opting in to marketing email.</span></span>

<span data-ttu-id="e6088-118">Aşağıdaki çizimde, modül kitaplığı kullanılarak oluşturulmuş bir **profilim** sayfası örneği gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="e6088-118">The following illustration shows an example of a **My profile** page that was built by using the module library.</span></span>

![Profil sayfası örneği](./media/Account-Management-MyProfile.PNG)

### <a name="addresses-page"></a><span data-ttu-id="e6088-120">Adresler sayfası</span><span class="sxs-lookup"><span data-stu-id="e6088-120">Addresses page</span></span>

<span data-ttu-id="e6088-121">**Adresler** sayfası, müşterinin kendi hesabına adres eklemesini sağlar.</span><span class="sxs-lookup"><span data-stu-id="e6088-121">The **Addresses** page lets the customer add addresses to his or her account.</span></span> <span data-ttu-id="e6088-122">Ayrıca, müşterinin daha önce hesaba eklediği veya kaydettiği adreslerin listesini gösterir.</span><span class="sxs-lookup"><span data-stu-id="e6088-122">It also shows the list of addresses that the customer has previously added or saved to the account.</span></span> <span data-ttu-id="e6088-123">Bu adresler, müşterinin bu sayfada girdiği veya sipariş koyduğunda kullanılan adreslerdir.</span><span class="sxs-lookup"><span data-stu-id="e6088-123">These addresses are addresses that the customer entered either on this page or while placing an order.</span></span>

<span data-ttu-id="e6088-124">Aşağıdaki çizimde bir **Adresler** liste sayfasının bir örneği gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="e6088-124">The following illustration shows an example of the **Addresses** page.</span></span>

![Adresler sayfası örneği](./media/Account-Management-Address.png)

### <a name="order-history-and-order-details-pages"></a><span data-ttu-id="e6088-126">Sipariş geçmişi ve sipariş ayrıntıları sayfaları</span><span class="sxs-lookup"><span data-stu-id="e6088-126">Order history and Order details pages</span></span>

<span data-ttu-id="e6088-127">**Sipariş geçmişi** sayfası, müşterinin hesabını kullanarak gönderdiği tüm siparişlerin özetini gösterir.</span><span class="sxs-lookup"><span data-stu-id="e6088-127">The **Order history** page shows a summary of all orders that the customer has submitted by using his or her account.</span></span> <span data-ttu-id="e6088-128">Sipariş edilen maddelerin, onay numarasının, satış kimliğinin, izleme bilgilerinin ve diğer bilgilerin hızlı özetini verir.</span><span class="sxs-lookup"><span data-stu-id="e6088-128">It gives a quick summary of the items that were ordered, the confirmation number, sales ID, tracking information, and other information.</span></span> <span data-ttu-id="e6088-129">Müşteri her sipariş için daha ayrıntılı bir döküm görüntülemek isterse, **Sipariş ayrıntıları** sayfası vardır.</span><span class="sxs-lookup"><span data-stu-id="e6088-129">If the customer wants to view a more detailed breakdown of each order, there is an **Order details** page.</span></span> <span data-ttu-id="e6088-130">Bu sayfa, siparişin sevkiyat adresi, ödeme bilgileri, iskontolar, vergiler ve sevkiyat maliyetleri gibi bilgileri içerir.</span><span class="sxs-lookup"><span data-stu-id="e6088-130">This page includes information such as the shipping address, payment information, discounts, taxes, and shipping costs for the order.</span></span>

<span data-ttu-id="e6088-131">Aşağıdaki çizimde bir **Sipariş geçmişi** liste sayfasının bir örneği gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="e6088-131">The following illustration shows an example of the **Order history** page.</span></span>

![Sipariş geçmişi sayfası örneği](./media/Account-Management-OrderHistory.PNG)

<span data-ttu-id="e6088-133">Aşağıdaki çizimde bir **Sipariş ayrıntıları** liste sayfasının bir örneği gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="e6088-133">The following illustration shows an example of the **Order details** page.</span></span>

![Sipariş ayrıntıları sayfası örneği](./media/Account-Management-OrderDetails.PNG)

### <a name="loyalty-program-page"></a><span data-ttu-id="e6088-135">Bağlılık programı sayfası</span><span class="sxs-lookup"><span data-stu-id="e6088-135">Loyalty program page</span></span>

<span data-ttu-id="e6088-136">**Bağlılık programı** sayfası, müşterinin bir bağlılık programı üyesi olmasına olanak tanır.</span><span class="sxs-lookup"><span data-stu-id="e6088-136">The **Loyalty program** page lets the customer become a member of a loyalty program.</span></span> <span data-ttu-id="e6088-137">Müşteri bir bağlılık programı için kaydolduktan sonra, **bağlılık programı** sayfası, kazanılan puan sayısı ve kullanılmış puan sayısı gibi ayrıntıları içerir.</span><span class="sxs-lookup"><span data-stu-id="e6088-137">After a customer has signed up for a loyalty program, the **Loyalty program** page include details such as the number of points that have been earned and the number of points that have been redeemed.</span></span>

<span data-ttu-id="e6088-138">Aşağıdaki şekilde bir **bağlılık programı** sayfası örneği gösterilmiştir.</span><span class="sxs-lookup"><span data-stu-id="e6088-138">The following illustration shows an example of a **Loyalty program** page.</span></span>

![Bağlılık programı sayfası örneği](./media/Account-Management-Loyalty.PNG)

### <a name="wishlist-page"></a><span data-ttu-id="e6088-140">İstek listesi sayfası</span><span class="sxs-lookup"><span data-stu-id="e6088-140">Wishlist page</span></span>

<span data-ttu-id="e6088-141">**İstek listesi** sayfası, müşterinin kendi istek listesine eklediği maddelerin listesini gösterir.</span><span class="sxs-lookup"><span data-stu-id="e6088-141">The **Wishlist** page shows a list of the items that the customer has added to his or her wish list.</span></span> <span data-ttu-id="e6088-142">Ürün ve ürün çeşitleri istek listesine eklenebilir.</span><span class="sxs-lookup"><span data-stu-id="e6088-142">Both products and product variants can be added to the wish list.</span></span> <span data-ttu-id="e6088-143">Müşteri bu sayfadan, bir maddeyi istek listesinden kaldırabilir veya doğrudan sepete madde ekleyebilir.</span><span class="sxs-lookup"><span data-stu-id="e6088-143">From this page, the customer can remove an item from the wish list or add an item directly to the cart.</span></span>

<span data-ttu-id="e6088-144">Aşağıdaki şekilde bir **İstek listesi** sayfası örneği gösterilmiştir.</span><span class="sxs-lookup"><span data-stu-id="e6088-144">The following illustration shows an example of a **Wishlist** page.</span></span>

![İstek listesi sayfası örneği](./media/Account-Management-Wishlist.PNG)

<span data-ttu-id="e6088-146">Hesap yönetimi modülleri ve bunların nasıl yazılacağıyla ilgili daha fazla bilgi için [hesap yönetimi](account-management.md)'ne bakın.</span><span class="sxs-lookup"><span data-stu-id="e6088-146">For more information about account management modules and how to author them, see [Account Management](account-management.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="e6088-147">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="e6088-147">Additional resources</span></span>

[<span data-ttu-id="e6088-148">Giriş sayfasına genel bakış</span><span class="sxs-lookup"><span data-stu-id="e6088-148">Home page overview</span></span>](quick-tour-home-page.md)

[<span data-ttu-id="e6088-149">Ürün ayrıntıları sayfalarına genel bakış</span><span class="sxs-lookup"><span data-stu-id="e6088-149">Product details pages overview</span></span>](quick-tour-pdp.md)

[<span data-ttu-id="e6088-150">Sepet ve ödeme sayfalarına genel bakış</span><span class="sxs-lookup"><span data-stu-id="e6088-150">Cart and checkout pages overview</span></span>](quick-tour-cart-checkout.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]