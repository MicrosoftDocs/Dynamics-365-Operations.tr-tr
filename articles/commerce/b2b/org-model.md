---
title: B2B kuruluşlar için kuruluş modelleme hiyerarşileri oluşturma
description: Bu konuda, işletmeler arası (B2B) kuruluşlar için kuruluş modelleme hiyerarşileri oluşturma yöntemi açıklanmıştır.
author: josaw1
ms.date: 01/20/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RetailOperations
audience: Application User, IT Pro
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: retail
ms.author: josaw
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 487af939f92ece8bc3e543b3beeffa239baa1863
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/31/2021
ms.locfileid: "5799841"
---
# <a name="create-org-modeling-hierarchies-for-b2b-organizations"></a><span data-ttu-id="97022-103">B2B kuruluşlar için kuruluş modelleme hiyerarşileri oluşturma</span><span class="sxs-lookup"><span data-stu-id="97022-103">Create org modeling hierarchies for B2B organizations</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="97022-104">Bu konuda, Microsoft Dynamics 365 Commerce'te işletmeler arası (B2B) kuruluşlar için kuruluş modelleme hiyerarşileri oluşturma yöntemi açıklanmıştır.</span><span class="sxs-lookup"><span data-stu-id="97022-104">This topic describes how to create organizational modeling hierarchies for business-to-business (B2B) organizations in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="97022-105">Commerce Headquarters'da iş ortağı kuruluşları, müşteri ve müşteri hiyerarşisi varlıklarıyla temsil edilir.</span><span class="sxs-lookup"><span data-stu-id="97022-105">In Commerce headquarters, business partner organizations are represented by customer and customer hierarchy entities.</span></span> <span data-ttu-id="97022-106">İş ortağı kuruluş ve kullanıcıları, müşteri olarak temsil edilir ve müşteri hiyerarşileri bu müşterileri birbirleriyle ilişkilendirmek için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="97022-106">The business partner organization and its users are represented as customers, and customer hierarchies are used to associate those customers with each other.</span></span>

<span data-ttu-id="97022-107">Bir B2B e-ticaret sitesine katılmak için iş ortağı isteği onaylandığında, aşağıdaki eylemler gerçekleştirilir:</span><span class="sxs-lookup"><span data-stu-id="97022-107">When a business partner request to join a B2B e-commerce site is approved, the following actions are performed:</span></span>

- <span data-ttu-id="97022-108">Sistemde iki yeni müşteri kaydı oluşturulur: iş ortağı kuruluş için **Tür Kuruluş** müşteri kaydı ve istek sahibi (diğer bir deyişle, talebi gönderen iş ortağı kullanıcı) için **Tür Kişi** müşteri kaydı.</span><span class="sxs-lookup"><span data-stu-id="97022-108">Two new customer records are created in the system: a **Type Organization** customer record for the business partner organization and a **Type Person** customer record for the requestor (that is, the business partner user who submitted the request).</span></span>
- <span data-ttu-id="97022-109">**Müşteri\> Müşteri hiyerarşisi** altında yeni bir müşteri hiyerarşisi kaydı oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="97022-109">A new customer hierarchy record is created under **Customer \> Customer hierarchy**.</span></span> <span data-ttu-id="97022-110">Bu kayıt aşağıdaki başlık özelliklerine sahiptir:</span><span class="sxs-lookup"><span data-stu-id="97022-110">This record has the following header properties:</span></span>

    - <span data-ttu-id="97022-111">**Müşteri hiyerarşisi kimliği** – Müşteri hiyerarşisi için benzersiz bir kimlik.</span><span class="sxs-lookup"><span data-stu-id="97022-111">**Customer hierarchy ID** – A unique ID for the customer hierarchy.</span></span> <span data-ttu-id="97022-112">Bu kimlik, Commerce Headquarters'daki paylaşılan Commerce parametrelerinde tanımlanan numara serisini kullanır.</span><span class="sxs-lookup"><span data-stu-id="97022-112">This ID uses the number sequence that is defined in Commerce shared parameters in Commerce headquarters.</span></span>
    - <span data-ttu-id="97022-113">**Ad** - İş ortağının kuruluş adı ekleme isteğinde belirttiği kuruluş adı.</span><span class="sxs-lookup"><span data-stu-id="97022-113">**Name** – The organization name of the business partner, as specified in the onboarding request.</span></span>
    - <span data-ttu-id="97022-114">**Amaç** – Bu özellik önceden tanımlanmış **B2B kuruluşu** değerine ayarlanır.</span><span class="sxs-lookup"><span data-stu-id="97022-114">**Purpose** – This property is set to the predefined value **B2B organization**.</span></span>
    - <span data-ttu-id="97022-115">**Kuruluş** - İş ortağının müşteri kimliği.</span><span class="sxs-lookup"><span data-stu-id="97022-115">**Organization** – The customer ID of the business partner.</span></span>

<span data-ttu-id="97022-116">Müşteri hiyerarşisi kaydının ayrıntıları aşağıdadır:</span><span class="sxs-lookup"><span data-stu-id="97022-116">Here are the details of the customer hierarchy record:</span></span>

- <span data-ttu-id="97022-117">İstek sahibinin müşteri kaydı, müşteri hiyerarşisiyle ilişkilidir.</span><span class="sxs-lookup"><span data-stu-id="97022-117">The customer record of the requestor is associated with the customer hierarchy.</span></span>
- <span data-ttu-id="97022-118">Yönetici rolü istek sahibi ile ilişkilendirilir.</span><span class="sxs-lookup"><span data-stu-id="97022-118">The administrator role is associated with the requestor.</span></span>

<span data-ttu-id="97022-119">Yönetici, bir B2B sitesinde iş ortağı kuruluşuna daha fazla kullanıcı eklediğinde, Commerce Headquarters'da her bir kullanıcı için yeni bir müşteri kaydı oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="97022-119">When the administrator adds more users are to the business partner organization on a B2B site, a new customer record for each user is created in Commerce headquarters.</span></span> <span data-ttu-id="97022-120">Bu müşteri kaydı aynı zamanda iş ortağı için ilgili müşteri hiyerarşisi kaydına eklenir ve bir "Kullanıcı" rolüne sahip olur.</span><span class="sxs-lookup"><span data-stu-id="97022-120">This customer record is also added to the relevant customer hierarchy record for the business partner and has the role of a "user."</span></span>

> [!NOTE]
> <span data-ttu-id="97022-121">Çoğu durumda, bir hiyerarşideki tüm müşteri kayıtlarının karşılık gelen özellik değerleri eşleşmelidir.</span><span class="sxs-lookup"><span data-stu-id="97022-121">In most cases, the corresponding property values of all customer records in a hierarchy should match.</span></span> <span data-ttu-id="97022-122">Örneğin, tüm iş ortağı kullanıcıların ürünlerle ilgili benzer fiyatları alması gerektiğinden, fiyat grubu ve ilişkili yapılandırmaların eşleşmesi gerekir.</span><span class="sxs-lookup"><span data-stu-id="97022-122">For example, because all business partner users should get similar prices for products, their price group and associated configurations should match.</span></span> <span data-ttu-id="97022-123">Ancak, sistem bu tutarlılığı zorunlu kılmaz.</span><span class="sxs-lookup"><span data-stu-id="97022-123">However, the system doesn't enforce this consistency.</span></span> <span data-ttu-id="97022-124">Bu nedenle, ilgili Commerce Headquarters kullanıcıları belirli bir hiyerarşideki tüm müşteriler için özellik değerlerinin ve yapılandırmaların eşleşmesini sağlamaya karşı sorumludur.</span><span class="sxs-lookup"><span data-stu-id="97022-124">Therefore, the relevant Commerce headquarters users are responsible for ensuring that the property values and configurations match for all customers in a given hierarchy.</span></span>

<span data-ttu-id="97022-125">Commerce Headquarters kullanıcıları, hiyerarşideki tüm müşteri kayıtlarının özellik değerlerine yan yana görünümde bakabilir.</span><span class="sxs-lookup"><span data-stu-id="97022-125">Commerce headquarters users can look at the property values for all customer records in the hierarchy in a side-by-side view.</span></span> <span data-ttu-id="97022-126">Açılan menüden sekme adlarını seçerek ilgili müşteri kaydı özelliklerini seçin.</span><span class="sxs-lookup"><span data-stu-id="97022-126">Select the relevant customer record properties by selecting the tab names on the drop-down menu.</span></span> <span data-ttu-id="97022-127">Kullanıcılar bu görünümdeki özellik değerlerini doğrudan görüntüleyebilir ve düzenleyebilir.</span><span class="sxs-lookup"><span data-stu-id="97022-127">Users can directly view and edit the property values from this view.</span></span> <span data-ttu-id="97022-128">Alternatif olarak, yöneticinin müşteri kaydındaki tüm değerleri tüm kullanıcı müşteri kayıtlarına uygulamak istiyorsanız, Müşteri hiyerarşisi ayrıntılarında **Geçersiz kıl**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="97022-128">Alternatively, if you want to apply all the values from the administrator customer record to all the user customer records, select **Override** in the customer hierarchy details.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="97022-129">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="97022-129">Additional resources</span></span>

[<span data-ttu-id="97022-130">B2B e-ticaret sitesi ayarlama</span><span class="sxs-lookup"><span data-stu-id="97022-130">Set up a B2B e-commerce site</span></span>](set-up-b2b-site.md)

[<span data-ttu-id="97022-131">B2B e-ticaret sitelerindeki iş ortağı kullanıcılarını yönetme</span><span class="sxs-lookup"><span data-stu-id="97022-131">Manage business partner users on B2B e-commerce sites</span></span>](manage-b2b-users.md)

[<span data-ttu-id="97022-132">B2B e-ticaret siteleri için müşteri hesabı ödeme yöntemini yapılandırma</span><span class="sxs-lookup"><span data-stu-id="97022-132">Configure the customer account payment method for B2B e-commerce sites</span></span>](payment-method.md)

[<span data-ttu-id="97022-133">B2B e-ticaret siteleri için ürün miktarı sınırlarını ayarlama</span><span class="sxs-lookup"><span data-stu-id="97022-133">Set product quantity limits for B2B e-commerce sites</span></span>](quantity-limits.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]