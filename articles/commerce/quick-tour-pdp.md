---
title: Ürün ayrıntıları sayfalarına genel bakış
description: Bu konu, Microsoft Dynamics 365 Commerce'ta ürün ayrıntıları sayfalarına (PDP'ler) genel bakış sağlar.
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
ms.openlocfilehash: 3b02d50adbfcda27d590bcb87fd9669d67d4a01c
ms.sourcegitcommit: 295d940a345879b3dfc5991e387b91c7257019ea
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/01/2019
ms.locfileid: "2697877"
---
# <a name="overview-of-product-details-pages"></a><span data-ttu-id="affa6-103">Ürün ayrıntıları sayfalarına genel bakış</span><span class="sxs-lookup"><span data-stu-id="affa6-103">Overview of product details pages</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="affa6-104">Bu konu, Microsoft Dynamics 365 Commerce'ta ürün ayrıntıları sayfalarına (PDP'ler) genel bakış sağlar.</span><span class="sxs-lookup"><span data-stu-id="affa6-104">This topic provides an overview of product details pages (PDPs) in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="affa6-105">Genel Bakış</span><span class="sxs-lookup"><span data-stu-id="affa6-105">Overview</span></span>

<span data-ttu-id="affa6-106">PDP bir ürünle ilgili ayrıntılı bilgi sağlar ve müşteriler boyut, stil ve renk gibi ürün seçeneklerini seçsin.</span><span class="sxs-lookup"><span data-stu-id="affa6-106">A PDP provides detailed information about a product, and lets customers select product options such as a size, style, and color.</span></span> <span data-ttu-id="affa6-107">Bir PDP, bir müşterinin satın alma kararı vermek için gerek duyduğu tüm ürün bilgilerini sergilemelidir.</span><span class="sxs-lookup"><span data-stu-id="affa6-107">A PDP should showcase all the product information that a customer requires to make a purchase decision.</span></span>

<span data-ttu-id="affa6-108">Aşağıdaki şekilde bir PDP örneği gösterilmiştir.</span><span class="sxs-lookup"><span data-stu-id="affa6-108">The following illustration shows an example of a PDP.</span></span>

![Ürün ayrıntıları sayfası örneği](./media/pdp.PNG)

## <a name="header-and-footer-modules"></a><span data-ttu-id="affa6-110">Üst bilgi ve alt bilgi modülleri</span><span class="sxs-lookup"><span data-stu-id="affa6-110">Header and footer modules</span></span>

<span data-ttu-id="affa6-111">PDP üst bölümünde, perakendecinin müşterilerin göz atmasını istediği tüm ürün kategorilerini ve diğer sayfaları gösteren bir başlık yer vardır.</span><span class="sxs-lookup"><span data-stu-id="affa6-111">The top of a PDP has a header that shows all the product categories and other pages that the retailer wants customers to browse.</span></span> <span data-ttu-id="affa6-112">Sayfanın alt bölümünde, bir müşterilerin ilgilenebileceği çeşitli konularda hızlı bağlantılar içeren bir altbilgi yer almaktadır.</span><span class="sxs-lookup"><span data-stu-id="affa6-112">The bottom of the page has a footer that contains quick links to various topics that might interest customers.</span></span>

## <a name="buy-box-module"></a><span data-ttu-id="affa6-113">Satınalma kutusu modülü</span><span class="sxs-lookup"><span data-stu-id="affa6-113">Buy box module</span></span>

<span data-ttu-id="affa6-114">Bir PDP üzerindeki en önemli modül satın alma kutusu modülüdür.</span><span class="sxs-lookup"><span data-stu-id="affa6-114">The most important module on a PDP is the buy box module.</span></span> <span data-ttu-id="affa6-115">Bu nedenle, sayfanın ana bölümündeki ilk öğe olur.</span><span class="sxs-lookup"><span data-stu-id="affa6-115">Therefore, it's the first item in the main section of the page.</span></span> <span data-ttu-id="affa6-116">Satın alma kutusu modülü bir konteyner modülüdür ve ürünle ilgili en önemli bilgileri içeren birkaç modülü barındırır.</span><span class="sxs-lookup"><span data-stu-id="affa6-116">A buy box module is a container module and hosts several modules that contain the most important information about the product.</span></span> <span data-ttu-id="affa6-117">Bu bilgiler ürün adını, ürün görüntülerini, açıklamayı, fiyatı ve ürün derecelendirmelerini içerir.</span><span class="sxs-lookup"><span data-stu-id="affa6-117">This information includes the product name, product images, the description, the price, and product ratings.</span></span>

<span data-ttu-id="affa6-118">Satın alma kutusu modülü müşterinin ürün seçeneklerini (örneğin, boyut, stil ve renk) seçmesini ve ürünü sepete eklemenizi sağlar.</span><span class="sxs-lookup"><span data-stu-id="affa6-118">The buy box module lets the customer select product options (for example, a size, style, and color) and add the product to the cart.</span></span> <span data-ttu-id="affa6-119">Ayrıca, müşterinin ürünü çevrimiçi olarak satın alıp bir mağaza içinde çekmesini sağlar.</span><span class="sxs-lookup"><span data-stu-id="affa6-119">It also lets the customer buy the product online and pick it up in a store.</span></span> <span data-ttu-id="affa6-120">Çevrimiçi satın al ve kayıt depo modülünde, müşterinin belirttiği başka bir konumda yakındaki mağazaların veya mağazaların bulunması için Bing Haritalar uygulama programlama arabirimleriyle (API) tümleştirme kullanılır.</span><span class="sxs-lookup"><span data-stu-id="affa6-120">The buy online and pick up in store module uses integration with Bing Maps application programming interfaces (APIs) to find nearby stores or stores in another location that the customer specifies.</span></span>

<span data-ttu-id="affa6-121">Satın alma kutusu modülü bir ürün kimliği gerektirir.</span><span class="sxs-lookup"><span data-stu-id="affa6-121">A buy box module requires a product ID.</span></span> <span data-ttu-id="affa6-122">Bu kod sayfa bağlamından türetilir.</span><span class="sxs-lookup"><span data-stu-id="affa6-122">This ID is derived from the page context.</span></span> <span data-ttu-id="affa6-123">Bir satın alma kutusu modülü, sayfa içeriğinin ürün kimliği içerdiği bir sayfaya eklenirse, bilgileri doğru işlemez.</span><span class="sxs-lookup"><span data-stu-id="affa6-123">If a buy box module is added to a page where the page context doesn't include a product ID, it won't render the information correctly.</span></span>

## <a name="product-specifications-module"></a><span data-ttu-id="affa6-124">Ürün özellikleri modülü</span><span class="sxs-lookup"><span data-stu-id="affa6-124">Product specifications module</span></span>

<span data-ttu-id="affa6-125">Ürün belirtimleri modülü, ürünle ilgili ek ayrıntıları sergileyebilecek şekilde kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="affa6-125">The product specifications module can be used to showcase additional details about the product.</span></span> <span data-ttu-id="affa6-126">Bu Ayrıntılar Dynamics 365 Retail'deki ürün özniteliklerinden alınmıştır.</span><span class="sxs-lookup"><span data-stu-id="affa6-126">These details are taken from product attributes in Dynamics 365 Retail.</span></span> <span data-ttu-id="affa6-127">Ürün belirtimleri modülü, **görünür** özelliğinin **doğru** olarak ayarlandığı her özniteliği gösterir.</span><span class="sxs-lookup"><span data-stu-id="affa6-127">The product specifications module shows every attribute where the **visible** property is set to **true**.</span></span> <span data-ttu-id="affa6-128">Ürün özniteliklerini almak için ürün kodu gerekir.</span><span class="sxs-lookup"><span data-stu-id="affa6-128">It requires a product ID to retrieve the product attributes.</span></span>

## <a name="recommendations-module"></a><span data-ttu-id="affa6-129">Ürün modülü</span><span class="sxs-lookup"><span data-stu-id="affa6-129">Recommendations module</span></span>

<span data-ttu-id="affa6-130">Öneriler modülü, PDP'de önemli modüldür.</span><span class="sxs-lookup"><span data-stu-id="affa6-130">The recommendations module is an important module on a PDP.</span></span> <span data-ttu-id="affa6-131">Müşteriler ürünlere göz atarken, doğru ürünü bulabilmeleri ve satın almak için daha fazla ürün seçeneği sunulmalıdır.</span><span class="sxs-lookup"><span data-stu-id="affa6-131">While customers browse for products, more product options should be presented to them, so that they can find the correct product and make a purchase.</span></span> <span data-ttu-id="affa6-132">Öneriler, müşterilerin ilgili içeriği kolayca bulmasına ve alışveriş yapmaya devam etmesine yardımcı olur.</span><span class="sxs-lookup"><span data-stu-id="affa6-132">Recommendations help customers easily discover related content and continue to shop.</span></span>

<span data-ttu-id="affa6-133">Farklı öneri listesi türleri mevcuttur:</span><span class="sxs-lookup"><span data-stu-id="affa6-133">Different types of recommendation lists are available:</span></span>

- <span data-ttu-id="affa6-134">**Bunları da sevdiler** listesi makine öğrenmeyi temel alır.</span><span class="sxs-lookup"><span data-stu-id="affa6-134">The **People also like** list is based on machine learning.</span></span> <span data-ttu-id="affa6-135">Öneri sağlamak için diğer müşterilerin hareket geçmişini kullanır.</span><span class="sxs-lookup"><span data-stu-id="affa6-135">It uses the transaction history of other customers to provide recommendations.</span></span> <span data-ttu-id="affa6-136">Bu liste öneriler Servisi tarafından oluşturuldu ve "Bunu satın alan müşteriler de satın alınır..." gibi listelere benzer.</span><span class="sxs-lookup"><span data-stu-id="affa6-136">This list is generated by the recommendations service and resembles "Customers who bought this also bought..." lists.</span></span> <span data-ttu-id="affa6-137">Bu listeyi oluşturmak için bir ürün kimliği gereklidir.</span><span class="sxs-lookup"><span data-stu-id="affa6-137">A product ID is required to generate this list.</span></span>
- <span data-ttu-id="affa6-138">Perakende satılan bir ürün için **ilgili** bir liste konfigüre edilebilir.</span><span class="sxs-lookup"><span data-stu-id="affa6-138">A **Related** list can be configured for a product in Retail.</span></span> <span data-ttu-id="affa6-139">Örneğin, kahverengi bir deri yolculuğu el çantası için, deri temelli veya seyahat amacıyla tasarlanan diğer el çantaları ilgili liste için konfigüre edilebilir.</span><span class="sxs-lookup"><span data-stu-id="affa6-139">For example, for a brown leather travel handbag, more handbags that are leather-based or designed for travel purposes can be configured for the related list.</span></span> <span data-ttu-id="affa6-140">Tıpkı **aksesuarlar** ve **Bunun gibi daha fazla** gibi diğer ilgili liste türleri de perakende olarak konfigüre edilebilir.</span><span class="sxs-lookup"><span data-stu-id="affa6-140">Other types of related lists, such as **Accessories** and **More like this**, can also be configured in Retail.</span></span> <span data-ttu-id="affa6-141">Bu listeyi oluşturmak için bir ürün kimliği gereklidir.</span><span class="sxs-lookup"><span data-stu-id="affa6-141">A product ID is required to generate this list.</span></span> <span data-ttu-id="affa6-142">Bu nedenle, sayfa içeriğinin bir ürün kimliği içerdiği bir giriş sayfasına eklenirse, liste boş olacaktır.</span><span class="sxs-lookup"><span data-stu-id="affa6-142">Therefore, if it's added to a home page, where the page context doesn't include a product ID, the list will be empty.</span></span>
- <span data-ttu-id="affa6-143">Algoritmik oluşturulan öneri listeleri (örneğin, **Trend**, **en iyi satış** ve **yeni**), PDP'lerde kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="affa6-143">Algorithmically generated recommendation lists, such as **Trending**, **Best Selling**, and **New**, can be used on PDPs.</span></span> <span data-ttu-id="affa6-144">Bu listeler PDP üzerindeki ürünle doğrudan ilişkili olmasa da, müşterileri ilgilendirebilecek ürünler bulmasına yardımcı olmanın başka bir yoludur.</span><span class="sxs-lookup"><span data-stu-id="affa6-144">Although these lists might not be directly related to the product on the PDP, they are another way to help customers find products that might interest them.</span></span> <span data-ttu-id="affa6-145">Bu tür listeler bir ürün kimliği gerektirmez.</span><span class="sxs-lookup"><span data-stu-id="affa6-145">These types of lists don't require a product ID.</span></span> <span data-ttu-id="affa6-146">Bunlar, site genelinde alışveriş desenleri temel alınarak oluşturulan genel listelerdir.</span><span class="sxs-lookup"><span data-stu-id="affa6-146">They are generic lists that are generated based on shopping patterns across the site.</span></span>
- <span data-ttu-id="affa6-147">Düzenleme listeleri manue eklenen listelerdir.</span><span class="sxs-lookup"><span data-stu-id="affa6-147">Editorial lists are manually curated lists.</span></span> <span data-ttu-id="affa6-148">Örneğin, bir perakende, sergilemek istediği ürünlerin listesini el ile seçmeye karar verebilir.</span><span class="sxs-lookup"><span data-stu-id="affa6-148">For example, a retailer might decide to manually curate lists of products that it wants to showcase.</span></span>

## <a name="ratings-and-reviews-module"></a><span data-ttu-id="affa6-149">Derecelendirmelere ve inceleme modülleri</span><span class="sxs-lookup"><span data-stu-id="affa6-149">Ratings and reviews module</span></span>

<span data-ttu-id="affa6-150">Derecelendirmeler ve İncelemeler modülü, diğer müşteriler tarafından sağlanan derecelendirmeleri ve incelemeleri gösterir.</span><span class="sxs-lookup"><span data-stu-id="affa6-150">The ratings and reviews module shows ratings and reviews that have been provided by other customers.</span></span> <span data-ttu-id="affa6-151">Ayrıca, bir müşterinin ürünün incelemesini kendi başına yazması da sağlar.</span><span class="sxs-lookup"><span data-stu-id="affa6-151">It also lets a customer write his or her own review of the product.</span></span> <span data-ttu-id="affa6-152">Ek olarak, ürünle ilgili derecelendirme eğilimini gösteren bir histogram da içerir.</span><span class="sxs-lookup"><span data-stu-id="affa6-152">Additionally, it includes a histogram that shows the ratings trend for the product.</span></span> <span data-ttu-id="affa6-153">Daha fazla bilgi için bkz: [Derecelendirme ve incelemeler genel bakışı](ratings-reviews-overview.md).</span><span class="sxs-lookup"><span data-stu-id="affa6-153">For more details, see [Ratings and reviews overview](ratings-reviews-overview.md).</span></span>

## <a name="marketing-modules"></a><span data-ttu-id="affa6-154">Pazarlama modülleri</span><span class="sxs-lookup"><span data-stu-id="affa6-154">Marketing modules</span></span>

<span data-ttu-id="affa6-155">Belirli bir ürünle ilgili pazarlama içeriği benzersiz ise, tüm pazarlama modülleri PDP'ye eklenebilir.</span><span class="sxs-lookup"><span data-stu-id="affa6-155">If marketing content is unique to a specific product, any marketing module can be added to the PDP.</span></span> <span data-ttu-id="affa6-156">Bir PDC'ye, sayfaya "zenginleştirme" uygulayarak pazarlama modülleri ekleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="affa6-156">You can add marketing modules to a PDP by "enriching" the page.</span></span> 

## <a name="additional-resources"></a><span data-ttu-id="affa6-157">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="affa6-157">Additional resources</span></span>

[<span data-ttu-id="affa6-158">Giriş sayfasına genel bakış</span><span class="sxs-lookup"><span data-stu-id="affa6-158">Overview of the home page</span></span>](quick-tour-home-page.md)

[<span data-ttu-id="affa6-159">Varsayılan kategori açılış sayfası ve arama sonuçları sayfasına genel bakış</span><span class="sxs-lookup"><span data-stu-id="affa6-159">Overview of default category landing page and search results page</span></span>](category-search-page-overview.md)

[<span data-ttu-id="affa6-160">Sepet ve ödeme sayfalarına genel bakış</span><span class="sxs-lookup"><span data-stu-id="affa6-160">Overview of cart and checkout pages</span></span>](quick-tour-cart-checkout.md)

[<span data-ttu-id="affa6-161">Hesap yönetimi sayfalarına genel bakış</span><span class="sxs-lookup"><span data-stu-id="affa6-161">Overview of account management pages</span></span>](quick-tour-account-management.md)
