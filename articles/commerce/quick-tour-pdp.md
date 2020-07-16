---
title: Ürün ayrıntıları sayfalarına genel bakış
description: Bu konu, Microsoft Dynamics 365 Commerce'ta ürün ayrıntıları sayfalarına (PDP'ler) genel bakış sağlar.
author: anupamar-ms
manager: annbe
ms.date: 01/23/2020
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
ms.openlocfilehash: c53e74204fad2960dfba972a38c511df7d6672d8
ms.sourcegitcommit: ce397c2759f642c595e30fef58a770b50360b2bd
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/01/2020
ms.locfileid: "3527551"
---
# <a name="product-details-pages-overview"></a><span data-ttu-id="2dbe9-103">Ürün ayrıntıları sayfalarına genel bakış</span><span class="sxs-lookup"><span data-stu-id="2dbe9-103">Product details pages overview</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="2dbe9-104">Bu konu, Microsoft Dynamics 365 Commerce'ta ürün ayrıntıları sayfalarına (PDP'ler) genel bakış sağlar.</span><span class="sxs-lookup"><span data-stu-id="2dbe9-104">This topic provides an overview of product details pages (PDPs) in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="2dbe9-105">Genel Bakış</span><span class="sxs-lookup"><span data-stu-id="2dbe9-105">Overview</span></span>

<span data-ttu-id="2dbe9-106">PDP bir ürünle ilgili ayrıntılı bilgi sağlar ve müşteriler boyut, stil ve renk gibi ürün seçeneklerini seçsin.</span><span class="sxs-lookup"><span data-stu-id="2dbe9-106">A PDP provides detailed information about a product, and lets customers select product options such as a size, style, and color.</span></span> <span data-ttu-id="2dbe9-107">Bir PDP, bir müşterinin satın alma kararı vermek için gerek duyduğu tüm ürün bilgilerini sergilemelidir.</span><span class="sxs-lookup"><span data-stu-id="2dbe9-107">A PDP should showcase all the product information that a customer requires to make a purchase decision.</span></span>

<span data-ttu-id="2dbe9-108">Aşağıdaki şekilde bir PDP örneği gösterilmiştir.</span><span class="sxs-lookup"><span data-stu-id="2dbe9-108">The following illustration shows an example of a PDP.</span></span>

![Ürün ayrıntıları sayfası örneği](./media/pdp.PNG)

## <a name="header-and-footer-modules"></a><span data-ttu-id="2dbe9-110">Üst bilgi ve alt bilgi modülleri</span><span class="sxs-lookup"><span data-stu-id="2dbe9-110">Header and footer modules</span></span>

<span data-ttu-id="2dbe9-111">PDP üst bölümünde, perakendecinin müşterilerin göz atmasını istediği tüm ürün kategorilerini ve diğer sayfaları gösteren bir başlık yer vardır.</span><span class="sxs-lookup"><span data-stu-id="2dbe9-111">The top of a PDP has a header that shows all the product categories and other pages that the retailer wants customers to browse.</span></span> <span data-ttu-id="2dbe9-112">Sayfanın alt bölümünde, bir müşterilerin ilgilenebileceği çeşitli konularda hızlı bağlantılar içeren bir altbilgi yer almaktadır.</span><span class="sxs-lookup"><span data-stu-id="2dbe9-112">The bottom of the page has a footer that contains quick links to various topics that might interest customers.</span></span>

## <a name="buy-box-module"></a><span data-ttu-id="2dbe9-113">Satınalma kutusu modülü</span><span class="sxs-lookup"><span data-stu-id="2dbe9-113">Buy box module</span></span>

<span data-ttu-id="2dbe9-114">Bir PDP üzerindeki en önemli modül, sayfanın ana bölümünde ilk öğe olarak görünen satın alma kutusu modülüdür.</span><span class="sxs-lookup"><span data-stu-id="2dbe9-114">The most important module on a PDP is the buy box module, which appears as the first item in the main section of the page.</span></span> <span data-ttu-id="2dbe9-115">Satınalma kutusu modülü, ürün adı, ürün açıklaması, ürün fiyatı, ürün görüntüleri ve ürün derecelendirmeleri gibi önemli ürün bilgilerini gösterir.</span><span class="sxs-lookup"><span data-stu-id="2dbe9-115">A buy box module shows important product information, such as the product name, the product description, the product price, product images, and product ratings.</span></span>

<span data-ttu-id="2dbe9-116">Satın alma kutusu modülü müşterinin ürün seçeneklerini (örneğin, boyut, stil ve renk) seçmesini ve ürünü sepete eklemenizi sağlar.</span><span class="sxs-lookup"><span data-stu-id="2dbe9-116">The buy box module lets the customer select product options (for example, a size, style, and color) and add the product to the cart.</span></span> <span data-ttu-id="2dbe9-117">Ayrıca, müşterinin ürünü çevrimiçi olarak satın alıp bir mağaza içinde çekmesini sağlar.</span><span class="sxs-lookup"><span data-stu-id="2dbe9-117">It also lets the customer buy the product online and pick it up in a store.</span></span> <span data-ttu-id="2dbe9-118">Çevrimiçi satın al ve kayıt depo modülünde, müşterinin belirttiği başka bir konumda yakındaki mağazaların veya mağazaların bulunması için Bing Haritalar uygulama programlama arabirimleriyle (API) tümleştirme kullanılır.</span><span class="sxs-lookup"><span data-stu-id="2dbe9-118">The buy online and pick up in store module uses integration with Bing Maps application programming interfaces (APIs) to find nearby stores or stores in another location that the customer specifies.</span></span>

<span data-ttu-id="2dbe9-119">Satın alma kutusu modülü bir ürün kimliği gerektirir.</span><span class="sxs-lookup"><span data-stu-id="2dbe9-119">A buy box module requires a product ID.</span></span> <span data-ttu-id="2dbe9-120">Bu kod sayfa bağlamından türetilir.</span><span class="sxs-lookup"><span data-stu-id="2dbe9-120">This ID is derived from the page context.</span></span> <span data-ttu-id="2dbe9-121">Bir satın alma kutusu modülü, sayfa içeriğinin ürün kimliği içerdiği bir sayfaya eklenirse, bilgileri doğru işlemez.</span><span class="sxs-lookup"><span data-stu-id="2dbe9-121">If a buy box module is added to a page where the page context doesn't include a product ID, it won't render the information correctly.</span></span>

## <a name="product-specifications-module"></a><span data-ttu-id="2dbe9-122">Ürün özellikleri modülü</span><span class="sxs-lookup"><span data-stu-id="2dbe9-122">Product specifications module</span></span>

<span data-ttu-id="2dbe9-123">Ürün belirtimleri modülü, ürünle ilgili ek ayrıntıları sergileyebilecek şekilde kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="2dbe9-123">The product specifications module can be used to showcase additional details about the product.</span></span> <span data-ttu-id="2dbe9-124">Bu Ayrıntılar Commerce'deki ürün özniteliklerinden alınmıştır.</span><span class="sxs-lookup"><span data-stu-id="2dbe9-124">These details are taken from product attributes in Commerce.</span></span> <span data-ttu-id="2dbe9-125">Ürün belirtimleri modülü, **görünür** özelliğinin **doğru** olarak ayarlandığı her özniteliği gösterir.</span><span class="sxs-lookup"><span data-stu-id="2dbe9-125">The product specifications module shows every attribute where the **visible** property is set to **true**.</span></span> <span data-ttu-id="2dbe9-126">Ürün özniteliklerini almak için ürün kodu gerekir.</span><span class="sxs-lookup"><span data-stu-id="2dbe9-126">It requires a product ID to retrieve the product attributes.</span></span>

## <a name="recommendations-module"></a><span data-ttu-id="2dbe9-127">Ürün modülü</span><span class="sxs-lookup"><span data-stu-id="2dbe9-127">Recommendations module</span></span>

<span data-ttu-id="2dbe9-128">Öneriler modülü, PDP'de önemli modüldür.</span><span class="sxs-lookup"><span data-stu-id="2dbe9-128">The recommendations module is an important module on a PDP.</span></span> <span data-ttu-id="2dbe9-129">Müşteriler ürünlere göz atarken, doğru ürünü bulabilmeleri ve satın almak için daha fazla ürün seçeneği sunulmalıdır.</span><span class="sxs-lookup"><span data-stu-id="2dbe9-129">While customers browse for products, more product options should be presented to them, so that they can find the correct product and make a purchase.</span></span> <span data-ttu-id="2dbe9-130">Öneriler, müşterilerin ilgili içeriği kolayca bulmasına ve alışveriş yapmaya devam etmesine yardımcı olur.</span><span class="sxs-lookup"><span data-stu-id="2dbe9-130">Recommendations help customers easily discover related content and continue to shop.</span></span>

<span data-ttu-id="2dbe9-131">Farklı öneri listesi türleri mevcuttur:</span><span class="sxs-lookup"><span data-stu-id="2dbe9-131">Different types of recommendation lists are available:</span></span>

- <span data-ttu-id="2dbe9-132">**Bunları da sevdiler** listesi makine öğrenmeyi temel alır.</span><span class="sxs-lookup"><span data-stu-id="2dbe9-132">The **People also like** list is based on machine learning.</span></span> <span data-ttu-id="2dbe9-133">Öneri sağlamak için diğer müşterilerin hareket geçmişini kullanır.</span><span class="sxs-lookup"><span data-stu-id="2dbe9-133">It uses the transaction history of other customers to provide recommendations.</span></span> <span data-ttu-id="2dbe9-134">Bu liste öneriler Servisi tarafından oluşturuldu ve "Bunu satın alan müşteriler de satın alınır..." gibi listelere benzer.</span><span class="sxs-lookup"><span data-stu-id="2dbe9-134">This list is generated by the recommendations service and resembles "Customers who bought this also bought..." lists.</span></span> <span data-ttu-id="2dbe9-135">Bu listeyi oluşturmak için bir ürün kimliği gereklidir.</span><span class="sxs-lookup"><span data-stu-id="2dbe9-135">A product ID is required to generate this list.</span></span>
- <span data-ttu-id="2dbe9-136">Commerce'de satılan bir ürün için **ilgili** bir liste konfigüre edilebilir.</span><span class="sxs-lookup"><span data-stu-id="2dbe9-136">A **Related** list can be configured for a product in Commerce.</span></span> <span data-ttu-id="2dbe9-137">Örneğin, kahverengi bir deri yolculuğu el çantası için, deri temelli veya seyahat amacıyla tasarlanan diğer el çantaları ilgili liste için konfigüre edilebilir.</span><span class="sxs-lookup"><span data-stu-id="2dbe9-137">For example, for a brown leather travel handbag, more handbags that are leather-based or designed for travel purposes can be configured for the related list.</span></span> <span data-ttu-id="2dbe9-138">Tıpkı **aksesuarlar** ve **Bunun gibi daha fazla** gibi diğer ilgili liste türleri de Commerce olarak konfigüre edilebilir.</span><span class="sxs-lookup"><span data-stu-id="2dbe9-138">Other types of related lists, such as **Accessories** and **More like this**, can also be configured in Commerce.</span></span> <span data-ttu-id="2dbe9-139">Bu listeyi oluşturmak için bir ürün kimliği gereklidir.</span><span class="sxs-lookup"><span data-stu-id="2dbe9-139">A product ID is required to generate this list.</span></span> <span data-ttu-id="2dbe9-140">Bu nedenle, sayfa içeriğinin bir ürün kimliği içerdiği bir giriş sayfasına eklenirse, liste boş olacaktır.</span><span class="sxs-lookup"><span data-stu-id="2dbe9-140">Therefore, if it's added to a home page, where the page context doesn't include a product ID, the list will be empty.</span></span>
- <span data-ttu-id="2dbe9-141">Algoritmik oluşturulan öneri listeleri (örneğin, **Trend**, **en iyi satış** ve **yeni**), PDP'lerde kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="2dbe9-141">Algorithmically generated recommendation lists, such as **Trending**, **Best Selling**, and **New**, can be used on PDPs.</span></span> <span data-ttu-id="2dbe9-142">Bu listeler PDP üzerindeki ürünle doğrudan ilişkili olmasa da, müşterileri ilgilendirebilecek ürünler bulmasına yardımcı olmanın başka bir yoludur.</span><span class="sxs-lookup"><span data-stu-id="2dbe9-142">Although these lists might not be directly related to the product on the PDP, they are another way to help customers find products that might interest them.</span></span> <span data-ttu-id="2dbe9-143">Bu tür listeler bir ürün kimliği gerektirmez.</span><span class="sxs-lookup"><span data-stu-id="2dbe9-143">These types of lists don't require a product ID.</span></span> <span data-ttu-id="2dbe9-144">Bunlar, site genelinde alışveriş desenleri temel alınarak oluşturulan genel listelerdir.</span><span class="sxs-lookup"><span data-stu-id="2dbe9-144">They are generic lists that are generated based on shopping patterns across the site.</span></span>
- <span data-ttu-id="2dbe9-145">Düzenleme listeleri manue eklenen listelerdir.</span><span class="sxs-lookup"><span data-stu-id="2dbe9-145">Editorial lists are manually curated lists.</span></span> <span data-ttu-id="2dbe9-146">Örneğin, bir perakende, sergilemek istediği ürünlerin listesini el ile seçmeye karar verebilir.</span><span class="sxs-lookup"><span data-stu-id="2dbe9-146">For example, a retailer might decide to manually curate lists of products that it wants to showcase.</span></span>

## <a name="ratings-and-reviews-modules"></a><span data-ttu-id="2dbe9-147">Derecelendirmelere ve inceleme modülleri</span><span class="sxs-lookup"><span data-stu-id="2dbe9-147">Ratings and reviews modules</span></span>

<span data-ttu-id="2dbe9-148">İncelemeleri göstermek ve eklemek için üç modül kullanılabilir:</span><span class="sxs-lookup"><span data-stu-id="2dbe9-148">Three modules can be used to show and add reviews:</span></span>

- <span data-ttu-id="2dbe9-149">**İncelemeler** - Bu modülü, diğer müşteriler tarafından sağlanan derecelendirmeleri ve incelemeleri gösterir.</span><span class="sxs-lookup"><span data-stu-id="2dbe9-149">**Reviews** – This module lists ratings and reviews that have been provided by other customers.</span></span> <span data-ttu-id="2dbe9-150">Müşteriler İncelemeleri sıralayabilir ve süzebilir.</span><span class="sxs-lookup"><span data-stu-id="2dbe9-150">Customers can sort and filter the reviews.</span></span> <span data-ttu-id="2dbe9-151">Bu modül aynı zamanda müşterileri gözden geçirsin veya bunları beğenmediğiniz gibi sorunları rapor edin.</span><span class="sxs-lookup"><span data-stu-id="2dbe9-151">This module also lets customers like or dislike reviews, and report issues.</span></span>
- <span data-ttu-id="2dbe9-152">**Derecelendirme yazma** – bu modül, müşterilerinin bir ürünle ilgili incelemeleri yazalım.</span><span class="sxs-lookup"><span data-stu-id="2dbe9-152">**Write review** – This module lets customers write their own reviews of a product.</span></span>
- <span data-ttu-id="2dbe9-153">**Derecelendirme histogramı** – bu modül, bir ürünle ilgili derecelendirme eğilimini gösteren bir histogram içerir.</span><span class="sxs-lookup"><span data-stu-id="2dbe9-153">**Ratings histogram** – This module includes a histogram that shows the ratings trend for a product.</span></span>

<span data-ttu-id="2dbe9-154">Daha fazla bilgi için bkz: [Derecelendirme ve incelemeler genel bakışı](ratings-reviews-overview.md).</span><span class="sxs-lookup"><span data-stu-id="2dbe9-154">For more details, see [Ratings and reviews overview](ratings-reviews-overview.md).</span></span>

## <a name="marketing-modules"></a><span data-ttu-id="2dbe9-155">Pazarlama modülleri</span><span class="sxs-lookup"><span data-stu-id="2dbe9-155">Marketing modules</span></span>

<span data-ttu-id="2dbe9-156">Belirli bir ürünle ilgili pazarlama içeriği benzersiz ise, tüm pazarlama modülleri PDP'ye eklenebilir.</span><span class="sxs-lookup"><span data-stu-id="2dbe9-156">If marketing content is unique to a specific product, any marketing module can be added to the PDP.</span></span> <span data-ttu-id="2dbe9-157">Bir PDC'ye, sayfaya "zenginleştirme" uygulayarak pazarlama modülleri ekleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="2dbe9-157">You can add marketing modules to a PDP by "enriching" the page.</span></span> <span data-ttu-id="2dbe9-158">Daha fazla ayrıntı için, bkz. [ürün sayfası zenginleştirme](enrich-product-page.md).</span><span class="sxs-lookup"><span data-stu-id="2dbe9-158">For more details, see [Enrich a product page](enrich-product-page.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="2dbe9-159">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="2dbe9-159">Additional resources</span></span>

[<span data-ttu-id="2dbe9-160">Giriş sayfasına genel bakış</span><span class="sxs-lookup"><span data-stu-id="2dbe9-160">Home page overview</span></span>](quick-tour-home-page.md)

[<span data-ttu-id="2dbe9-161">Sepet ve ödeme sayfalarına genel bakış</span><span class="sxs-lookup"><span data-stu-id="2dbe9-161">Cart and checkout pages overview</span></span>](quick-tour-cart-checkout.md)

[<span data-ttu-id="2dbe9-162">Hesap yönetimi sayfalarına genel bakış</span><span class="sxs-lookup"><span data-stu-id="2dbe9-162">Account management pages overview</span></span>](quick-tour-account-management.md)

[<span data-ttu-id="2dbe9-163">Ürün ayrıntıları sayfasını zenginleştirme</span><span class="sxs-lookup"><span data-stu-id="2dbe9-163">Enrich a product details page</span></span>](enrich-product-page.md)
