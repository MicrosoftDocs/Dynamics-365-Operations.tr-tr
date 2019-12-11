---
title: Giriş sayfasına genel bakış
description: Bu konu Microsoft Dynamics 365 Commerce'te giriş sayfası hakkında bilgi sağlar.
author: anupamar-ms
manager: annbe
ms.date: 10/31/2019
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
ms.openlocfilehash: 3fb42c9aa2e2ef1d620b310e9d30dbae5f84c788
ms.sourcegitcommit: 295d940a345879b3dfc5991e387b91c7257019ea
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/01/2019
ms.locfileid: "2698292"
---
# <a name="overview-of-the-home-page"></a><span data-ttu-id="6008f-103">Giriş sayfasına genel bakış</span><span class="sxs-lookup"><span data-stu-id="6008f-103">Overview of the home page</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="6008f-104">Bu konu Microsoft Dynamics 365 Commerce'te giriş sayfası hakkında bilgi sağlar.</span><span class="sxs-lookup"><span data-stu-id="6008f-104">This topic provides an overview of the home page in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="6008f-105">Genel Bakış</span><span class="sxs-lookup"><span data-stu-id="6008f-105">Overview</span></span>

<span data-ttu-id="6008f-106">Giriş sayfası, alışverişçilerin bir e-ticaret sitesini ziyaret ettiklerinde gideceği varsayılan sayfasıdır.</span><span class="sxs-lookup"><span data-stu-id="6008f-106">The home page is the default page that shoppers go to when they visit an e-Commerce site.</span></span> <span data-ttu-id="6008f-107">Tipik olarak bu sayfa, ürünler ve promosyonlar için pazarlama modüllerinin bir birleşimini kullanarak servis talebi kullanır.</span><span class="sxs-lookup"><span data-stu-id="6008f-107">Typically, this page showcases products and promotions by using a combination of marketing modules.</span></span> <span data-ttu-id="6008f-108">Alışverişçileri bağlı tutmak için ana sayfa, görüntü ve metinle zengin olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="6008f-108">The home page should be rich with images and text to keep shoppers engaged.</span></span>

<span data-ttu-id="6008f-109">Aşağıdaki çizimde, başlangıç kiti ve "Fabrikam" teması kullanılarak oluşturulmuş bir giriş sayfası örneği gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="6008f-109">The following illustration shows an example of a home page that was built by using the online starter kit and the "Fabrikam" theme.</span></span>

![Giriş sayfası örneği](./media/Homepage2.PNG)

<span data-ttu-id="6008f-111">Giriş sayfanın üst bölümünde, perakendecinin müşterilerin göz atmasını istediği tüm ürün kategorilerini ve diğer sayfaları gösteren bir başlık yer vardır.</span><span class="sxs-lookup"><span data-stu-id="6008f-111">The top of the home page has a header that shows all the product categories and other pages that the retailer wants customers to browse.</span></span> <span data-ttu-id="6008f-112">Giriş sayfanın alt bölümünde, bir müşterilerin ilgilenebileceği çeşitli konularda hızlı bağlantılar içeren bir altbilgi yer almaktadır.</span><span class="sxs-lookup"><span data-stu-id="6008f-112">The bottom of the home page has a footer that contains quick links to various topics that might interest customers.</span></span>

<span data-ttu-id="6008f-113">Giriş sayfasının ana bölümü, ürünleri, kategorileri veya yükseltmeleri çeşitli Dynamics 365 Commerce modüller kullanarak vurgulayabilir:</span><span class="sxs-lookup"><span data-stu-id="6008f-113">The main section of the home page can highlight products, categories, or promotions by using various Dynamics 365 Commerce modules:</span></span>

- <span data-ttu-id="6008f-114">**Hero** – Genel olarak, ana bölümün başındaki ilk öğe, depodaki yeni ürünleri ve promosyonları vurgulayan bir veya daha fazla "kahraman" görüntüsü gösterir.</span><span class="sxs-lookup"><span data-stu-id="6008f-114">**Hero** – Typically, the first item at the top of the main section shows one or more "hero" images that highlight new products and promotions in the store.</span></span> <span data-ttu-id="6008f-115">Birden çok Hero görüntü varsa, kullanıcıların onlara gözatabilmeleri için bir döngü modülü içinde barındırılır.</span><span class="sxs-lookup"><span data-stu-id="6008f-115">If there are multiple hero images, they are hosted in a carousel module so that users can browse them.</span></span>

    <span data-ttu-id="6008f-116">Aşağıdaki şekilde, ana bölümdeki ilk öğenin **Yeni Varış** adı adlı bir hero modülü olduğu giriş sayfası örneği gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="6008f-116">The following illustration shows an example of a home page where the first item in the main section is a hero module that is named **New Arrival**.</span></span>

    ![Hero modülü örneği](./media/Hero.PNG)

- <span data-ttu-id="6008f-118">**Özellik** - Özellik modülü, ürünleri veya promosyonları bir görüntü ve metin birleşimiyle pazarlamak için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="6008f-118">**Feature** – A feature module is used to market products or promotions by using a combination of images and text.</span></span> <span data-ttu-id="6008f-119">Özellik modülleri bağımsız olarak kullanılabilir veya bir döngü modül içinde barındırılabilir.</span><span class="sxs-lookup"><span data-stu-id="6008f-119">Feature modules can be used independently, or they can be hosted in a carousel module.</span></span>

    <span data-ttu-id="6008f-120">Aşağıdaki çizimde giriş sayfasındaki özellik modüllerinin bir örneği gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="6008f-120">The following illustration shows an example of feature modules on a home page.</span></span>

    ![Özellik modülleri örnekleri](./media/Feature.PNG)

- <span data-ttu-id="6008f-122">**İçerik yerleşimi** – bir içerik yerleşim modülü, çok sütunlu bir düzende bir görüntü ve metin bileşimi kullanarak birden fazla ürün veya ürün kategorisini sergileyerek kullanılır.</span><span class="sxs-lookup"><span data-stu-id="6008f-122">**Content placement** – A content placement module is used to showcase multiple products or category of products by using a combination of images and text in a multicolumn layout.</span></span> <span data-ttu-id="6008f-123">Bu konunun başlarında görünen bir giriş sayfası gösterimde, **Alışveriş kadınlar**, **Alışveriş erkek** ve **Alışveriş Aksesuarları** kalemlerin üç sütunlu düzeni için içerik yerleşim modülü kullanılır.</span><span class="sxs-lookup"><span data-stu-id="6008f-123">In the illustration of a home page that appears earlier in this topic, a content placement module is used for the three-column layout of the **Shop Women**, **Shop Men**, and **Shop Accessories** items.</span></span>
- <span data-ttu-id="6008f-124">**Video oynatıcı** – Bir video oynatıcı modülü giriş sayfasındaki video içeriğini sergileyebilecek şekilde kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="6008f-124">**Video player** – A video player module can be used to showcase video content on the home page.</span></span> <span data-ttu-id="6008f-125">Bu konunun yukarısında görünen bir giriş sayfasının resmi bir video oynatıcı modülü içerir.</span><span class="sxs-lookup"><span data-stu-id="6008f-125">The illustration of a home page that appears earlier in this topic includes a video player module.</span></span>
- <span data-ttu-id="6008f-126">**İçerik zengin blok** – İçerik zengin blok modülü, giriş sayfasındaki metin içeriğini tek sütunlu veya birden çok sütunlu düzende göstermek için kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="6008f-126">**Content rich block** – A content rich block module can be used to present text content on the home page in a single-column or multicolumn layout.</span></span>
- <span data-ttu-id="6008f-127">**Ürün önerileri** – Ürün önerileri modülleri, giriş sayfasında **yeni**, **trend** ve **en iyi satış** gibi listeleri göstermek için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="6008f-127">**Product recommendations** – Product recommendations modules are used to show lists such as **New**, **Trending**, and **Best Selling** on the home page.</span></span> <span data-ttu-id="6008f-128">Bu listeler, ürünleri alışveriş eğilimlerine göre görüntüler ve bunlar algoritmik oluşturulabilir veya el ile başlatılabilir.</span><span class="sxs-lookup"><span data-stu-id="6008f-128">These lists showcase products based on shopping trends, and they can be algorithmically generated or manually curated.</span></span> <span data-ttu-id="6008f-129">Müşterilerin önde gelen ürünleri bulmasına ve alışveriş yapmaya devam etmesine yardımcı olurlar.</span><span class="sxs-lookup"><span data-stu-id="6008f-129">They help customers quickly discover top products and then continue to shop.</span></span>

    <span data-ttu-id="6008f-130">Aşağıdaki çizimde giriş sayfasındaki ürün önerileri modüllerinin bir örneği gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="6008f-130">The following illustration shows an example of product recommendations modules on a home page.</span></span>

    ![Ürün öneri modüllerine örnekler](./media/Recommendations.PNG)

> [!NOTE]
> <span data-ttu-id="6008f-132">Burada listelenen tüm modüller herhangi bir site sayfasında kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="6008f-132">All the modules that are listed here can be used on any site page.</span></span> <span data-ttu-id="6008f-133">Ancak, müşteriler siteyle ilk kez etkileşimde bulunduğu için, giriş sayfasındaki yerleşimleri önemlidir.</span><span class="sxs-lookup"><span data-stu-id="6008f-133">However, their placement on the home page is important because that page is where customers first interact with your site.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="6008f-134">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="6008f-134">Additional resources</span></span>

[<span data-ttu-id="6008f-135">Varsayılan kategori açılış sayfası ve arama sonuçları sayfasına genel bakış</span><span class="sxs-lookup"><span data-stu-id="6008f-135">Overview of default category landing page and search results page</span></span>](category-search-page-overview.md)

[<span data-ttu-id="6008f-136">Ürün ayrıntıları sayfalarına genel bakış</span><span class="sxs-lookup"><span data-stu-id="6008f-136">Overview of product details pages</span></span>](quick-tour-pdp.md)

[<span data-ttu-id="6008f-137">Sepet ve ödeme sayfalarına genel bakış</span><span class="sxs-lookup"><span data-stu-id="6008f-137">Overview of cart and checkout pages</span></span>](quick-tour-cart-checkout.md)

[<span data-ttu-id="6008f-138">Hesap yönetimi sayfalarına genel bakış</span><span class="sxs-lookup"><span data-stu-id="6008f-138">Overview of account management pages</span></span>](quick-tour-account-management.md)
