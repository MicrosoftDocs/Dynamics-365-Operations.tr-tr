---
title: Varsayılan kategori açılış sayfası ve arama sonuçları sayfasına genel bakış
description: Bu konu, Dynamics 365 Commerce'te varsayılan kategori açılış sayfası ve arama sonuçları sayfasına genel bakış sağlar.
author: v-chgri
manager: annbe
ms.date: 10/31/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Operations, Retail, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: asharchw
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 17746d2923ab84311253c47647c0020807bdb75c
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/01/2020
ms.locfileid: "3002508"
---
# <a name="overview-of-default-category-landing-page-and-search-results-page"></a><span data-ttu-id="9ef51-103">Varsayılan kategori açılış sayfası ve arama sonuçları sayfasına genel bakış</span><span class="sxs-lookup"><span data-stu-id="9ef51-103">Overview of default category landing page and search results page</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="9ef51-104">Bu konu, Microsoft Dynamics 365 Commerce e-Ticaret'te varsayılan kategori açılış sayfası ve arama sonuçları sayfasına genel bakış sağlar.</span><span class="sxs-lookup"><span data-stu-id="9ef51-104">This topic provides an overview of the default category landing page and search results page in Microsoft Dynamics 365 Commerce e-Commerce.</span></span>

## <a name="default-category-landing-page"></a><span data-ttu-id="9ef51-105">Varsyılan kategori açılış sayfası</span><span class="sxs-lookup"><span data-stu-id="9ef51-105">Default category landing page</span></span>

<span data-ttu-id="9ef51-106">Varsayılan kategori giriş sayfası, Web sitesi kullanıcılarının gezinti hiyerarşisinde bir kategori seçdiklerinde aldığı bir sayfa.</span><span class="sxs-lookup"><span data-stu-id="9ef51-106">The default category landing page is the page that website users typically are taken to when they select a category in the navigation hierarchy.</span></span> <span data-ttu-id="9ef51-107">Kategori sayfası gözatmanıza olanak tanır ve ayrıca kategorilere ayrılmış ürünleri sıralayabilir ve bunları iyileştirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="9ef51-107">The category page lets you browse, and you can also sort and refine the categorized products.</span></span>

![Varsyılan kategori açılış sayfası](./media/SimpleCategoryLandingDressCategory.png)

<span data-ttu-id="9ef51-109">Sayfanın üst bölümünde, ticaret yöneticisinin kategorilere ayrılmış tüm ürün kategorilerini ve diğer sayfaları gösteren bir başlık yer vardır.</span><span class="sxs-lookup"><span data-stu-id="9ef51-109">At the top of the page is a header that shows all the product categories and other pages that the merchandising manager has categorized.</span></span> <span data-ttu-id="9ef51-110">Konfigürasyon, kanal gezinme hiyerarşisinin konfigürasyonunun bir parçası olarak gerçekleştirilir.</span><span class="sxs-lookup"><span data-stu-id="9ef51-110">Configuration is done as part of the configuration of the channel navigation hierarchy.</span></span> <span data-ttu-id="9ef51-111">Sayfanın alt bölümünde, bir alışverişçinin ilgilenebileceği çeşitli konularda hızlı bağlantılar içeren bir altbilgi yer almaktadır.</span><span class="sxs-lookup"><span data-stu-id="9ef51-111">At the bottom of the page is a footer that includes quick links to various topics that a shopper might be interested in.</span></span>

<span data-ttu-id="9ef51-112">Kategori için aşağıdaki bileşenler gereklidir:</span><span class="sxs-lookup"><span data-stu-id="9ef51-112">The following components are essential for a category:</span></span>

- <span data-ttu-id="9ef51-113">**Ürün yerleştirme döşemeleri**, ticaret yöneticisinin, gezinti hiyerarşisi konfigürasyonunun bir parçası olarak bir kategoride tanımladığı ürünleri gösterir.</span><span class="sxs-lookup"><span data-stu-id="9ef51-113">**Product placement tiles** show the products that the merchandising manager has defined in a category as part of the configuration of the navigation hierarchy.</span></span>
- <span data-ttu-id="9ef51-114">**İyileştiriciler ve seçim özeti**, sayıları sağlayan ve öğeleri iyileştirmek için kullanılabilecek filtrelerdir.</span><span class="sxs-lookup"><span data-stu-id="9ef51-114">**Refiners and choice summary** are filters that provide counts and that can be used to refine items.</span></span> <span data-ttu-id="9ef51-115">Ticaret yöneticisi, kanal kategorileri ve ürün öznitelikleriyle ilgili meta verilerin konfigürasyonunun bir parçası olarak bunları yapılandırır.</span><span class="sxs-lookup"><span data-stu-id="9ef51-115">The merchandising manager configures them as part of the configuration of the metadata related to channel categories and product attributes.</span></span>
- <span data-ttu-id="9ef51-116">**Sıralama seçenekleri**, Web sitesi ziyaretçileri tarafından ürünleri sıralamak amacıyla kullanılır.</span><span class="sxs-lookup"><span data-stu-id="9ef51-116">**Sorting options** are used by website visitors to sort the products.</span></span> <span data-ttu-id="9ef51-117">Varsayılan olarak aşağıdaki sıralama seçenekleri kullanılabilir:</span><span class="sxs-lookup"><span data-stu-id="9ef51-117">By default, the following sorting options are available:</span></span>

    - <span data-ttu-id="9ef51-118">Fiyat: düşükten yükseğe</span><span class="sxs-lookup"><span data-stu-id="9ef51-118">Price – low to high</span></span>
    - <span data-ttu-id="9ef51-119">Fiyat: yüksekten düşüğe</span><span class="sxs-lookup"><span data-stu-id="9ef51-119">Price – high to low</span></span>
    - <span data-ttu-id="9ef51-120">Ürün adı - \[A-Z\]</span><span class="sxs-lookup"><span data-stu-id="9ef51-120">Product name – \[A-Z\]</span></span>
    - <span data-ttu-id="9ef51-121">Ürün adı - \[Z-A\]</span><span class="sxs-lookup"><span data-stu-id="9ef51-121">Product name – \[Z-A\]</span></span>
    - <span data-ttu-id="9ef51-122">Puanlar - düşükten yükseğe</span><span class="sxs-lookup"><span data-stu-id="9ef51-122">Ratings – low to high</span></span>
    - <span data-ttu-id="9ef51-123">Puanlar - yüksekten düşüğe</span><span class="sxs-lookup"><span data-stu-id="9ef51-123">Ratings – high to low</span></span>

- <span data-ttu-id="9ef51-124">**Sayfalandırma**, web sitesi ziyaretçileri, kategorilere ayrılmış bir ürün sonuçları sayfasından başka bir sayfaya gitmesini sağlar.</span><span class="sxs-lookup"><span data-stu-id="9ef51-124">**Pagination** lets website visitors move from one page of categorized product results to another page.</span></span>
- <span data-ttu-id="9ef51-125">**Toplam sayı**, bir kategoride tanımlanan toplam ürün sayısını sağlar.</span><span class="sxs-lookup"><span data-stu-id="9ef51-125">**Total count** provides the total number of products that are defined in a category.</span></span>

## <a name="enrich-a-category-landing-page"></a><span data-ttu-id="9ef51-126">Kategori açılış sayfasını zenginleştirme</span><span class="sxs-lookup"><span data-stu-id="9ef51-126">Enrich a category landing page</span></span>

<span data-ttu-id="9ef51-127">Kategori giriş sayfasının belirli bir kategori için daha özel bir deneyim olmasını istiyorsanız, o kategori için kategori giriş sayfasını "zenginleştirebilirsiniz".</span><span class="sxs-lookup"><span data-stu-id="9ef51-127">If you want a category landing page to have a more tailored experience for a specific category, you can "enrich" the category landing page for that category.</span></span> <span data-ttu-id="9ef51-128">Örneğin, alışverişçinin dikkatini çekmek için pazarlama videosu ve bazı kategori öykülerinde bir hikaye ekleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="9ef51-128">For example, you can add a marketing video and some category storytelling to get the shopper's attention.</span></span> <span data-ttu-id="9ef51-129">Daha fazla bilgi için bkz. [Kategori giriş sayfasını zenginleştirme](enrich-category-page.md).</span><span class="sxs-lookup"><span data-stu-id="9ef51-129">For more information, see [Enrich a category landing page](enrich-category-page.md).</span></span>

![Zenginleştirilmiş kategori açılış sayfası](./media/CategoryLandingPages.png)

## <a name="auto-suggest-and-search-results-pages"></a><span data-ttu-id="9ef51-131">Otomatik önerme ve arama sonuçları sayfaları</span><span class="sxs-lookup"><span data-stu-id="9ef51-131">Auto-suggest and search results pages</span></span>

<span data-ttu-id="9ef51-132">Web sitesi kullanıcıları, gezinti hiyerarşisindeki bir kategoriye giderek veya arama alanına bir arama terimi girerek siteyi keşfeden bulabilir.</span><span class="sxs-lookup"><span data-stu-id="9ef51-132">Website users can explore a site either by going to a category from the navigation hierarchy or by entering a search term in the search field.</span></span>

<span data-ttu-id="9ef51-133">Kullanıcılar arama alanını yazma işlemi başladığında, arama terimlerini öneren derinlikli otomatik önerme işleviyle karşılaşır.</span><span class="sxs-lookup"><span data-stu-id="9ef51-133">As soon as users start to type in the search field, they experience the immersive auto-suggest functionality that suggests search terms.</span></span>

<span data-ttu-id="9ef51-134">Aşağıda, gösterilebilecek öneri türleri yer verilmektedir:</span><span class="sxs-lookup"><span data-stu-id="9ef51-134">Here are some of the types of suggestions that might be shown:</span></span>

- <span data-ttu-id="9ef51-135">**Anahtar sözcükler**, kanala göre sıralanan tüm ürünlerin içinde öğe bulmak için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="9ef51-135">**Keywords** are used to find items across all products that are assorted to the channel.</span></span>
- <span data-ttu-id="9ef51-136">**Ürünler**, ürün ayrıntıları sayfasına doğrudan bağlantılar sağlar.</span><span class="sxs-lookup"><span data-stu-id="9ef51-136">**Products** provide direct links to the product details page.</span></span>
- <span data-ttu-id="9ef51-137">**Kapsamlı kategori arama önerileri**, çeşitli kategorileri listeler ve kullanıcıların anahtar sözcüğü belirli bir kategoride aramasını sağlar.</span><span class="sxs-lookup"><span data-stu-id="9ef51-137">**Scoped category search suggestions** list various categories and let users search for the keyword in a specific category.</span></span>

![Derinlikli otomatik önerme](./media/ImmersiveAutoSuggestUX.png)

<span data-ttu-id="9ef51-139">Kullanıcılar anahtar sözcük veya kapsamlı kategori arama önerinden birini seçtiklerinde veya girdikleri arama terimi için hiçbir öneri olmadığında, bunlar arama sonuçları sayfasına yönlendirilir.</span><span class="sxs-lookup"><span data-stu-id="9ef51-139">When users select one of the keyword or scoped category search suggestions, or when there are no suggestions for the search term that they enter, they are redirected to a search results page.</span></span> <span data-ttu-id="9ef51-140">Kullanıcılar daha sonra, istenen maddeyi bulmak için arama sonuçları listesine göz atabilir, sıralayabilir ve belirginleştirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="9ef51-140">The users can then browse, sort, and refine the list of search results to find the desired item.</span></span>

![Arama giriş sayfası](./media/SearchLanding.png)

<span data-ttu-id="9ef51-142">Arama sonuçları sayfası için aşağıdaki bileşenler gereklidir:</span><span class="sxs-lookup"><span data-stu-id="9ef51-142">The following components are essential for a search results page:</span></span>

- <span data-ttu-id="9ef51-143">**Ürün yerleştirme döşemeleri** kullanıcının araması için ürünleri gösterir.</span><span class="sxs-lookup"><span data-stu-id="9ef51-143">**Product placement tiles** show the products for the user's search.</span></span> <span data-ttu-id="9ef51-144">Varsayılan olarak, bu döşemeler kullanıcı aramasının bulut destekli arama puanı tarafından sıralanır.</span><span class="sxs-lookup"><span data-stu-id="9ef51-144">By default, these tiles are sorted by the cloud-powered search relevancy score for the user search.</span></span>
- <span data-ttu-id="9ef51-145">**İyileştiriciler ve seçim özeti**, sayıları sağlayan ve öğeleri iyileştirmek için kullanılabilecek filtrelerdir.</span><span class="sxs-lookup"><span data-stu-id="9ef51-145">**Refiners and choice summary** are filters that provide counts and that can be used to refine items.</span></span> <span data-ttu-id="9ef51-146">Ticaret yöneticisi, kanal kategorileri ve ürün öznitelikleriyle ilgili meta verilerin konfigürasyonunun bir parçası olarak bunları yapılandırır.</span><span class="sxs-lookup"><span data-stu-id="9ef51-146">The merchandising manager configures them as part of the configuration of the "channel categories and product attributes" metadata.</span></span>
- <span data-ttu-id="9ef51-147">**Sıralama seçenekleri**, Web sitesi ziyaretçileri tarafından ürünleri sıralamak amacıyla kullanılır.</span><span class="sxs-lookup"><span data-stu-id="9ef51-147">**Sorting options** are used by website visitors to sort the products.</span></span> <span data-ttu-id="9ef51-148">Varsayılan olarak aşağıdaki sıralama seçenekleri kullanılabilir:</span><span class="sxs-lookup"><span data-stu-id="9ef51-148">By default, the following sorting options are available:</span></span>

    - <span data-ttu-id="9ef51-149">Fiyat: düşükten yükseğe</span><span class="sxs-lookup"><span data-stu-id="9ef51-149">Price – low to high</span></span>
    - <span data-ttu-id="9ef51-150">Fiyat: yüksekten düşüğe</span><span class="sxs-lookup"><span data-stu-id="9ef51-150">Price – high to low</span></span>
    - <span data-ttu-id="9ef51-151">Ürün adı - \[A-Z\]</span><span class="sxs-lookup"><span data-stu-id="9ef51-151">Product name – \[A-Z\]</span></span>
    - <span data-ttu-id="9ef51-152">Ürün adı - \[Z-A\]</span><span class="sxs-lookup"><span data-stu-id="9ef51-152">Product name – \[Z-A\]</span></span>
    - <span data-ttu-id="9ef51-153">Puanlar - düşükten yükseğe</span><span class="sxs-lookup"><span data-stu-id="9ef51-153">Ratings – low to high</span></span>
    - <span data-ttu-id="9ef51-154">Puanlar - yüksekten düşüğe</span><span class="sxs-lookup"><span data-stu-id="9ef51-154">Ratings – high to low</span></span>
    - <span data-ttu-id="9ef51-155">Varsayılan</span><span class="sxs-lookup"><span data-stu-id="9ef51-155">Default</span></span>

- <span data-ttu-id="9ef51-156">**Sayfalandırma**, web sitesi ziyaretçileri, kategorilere ayrılmış bir ürün sonuçları sayfasından başka bir sayfaya gitmesini sağlar.</span><span class="sxs-lookup"><span data-stu-id="9ef51-156">**Pagination** lets website visitors move from one page of categorized product results to another page.</span></span>
- <span data-ttu-id="9ef51-157">**Toplam sayı**, bir kategoride tanımlanan ve arama kriterlerine uyan toplam ürün sayısını sağlar.</span><span class="sxs-lookup"><span data-stu-id="9ef51-157">**Total count** provides the total number of products that are defined in a category and that match the search criteria.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="9ef51-158">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="9ef51-158">Additional resources</span></span>

[<span data-ttu-id="9ef51-159">Giriş sayfasına genel bakış</span><span class="sxs-lookup"><span data-stu-id="9ef51-159">Overview of the home page</span></span>](quick-tour-home-page.md)

[<span data-ttu-id="9ef51-160">Ürün ayrıntıları sayfalarına genel bakış</span><span class="sxs-lookup"><span data-stu-id="9ef51-160">Overview of product details pages</span></span>](quick-tour-pdp.md)

[<span data-ttu-id="9ef51-161">Sepet ve ödeme sayfalarına genel bakış</span><span class="sxs-lookup"><span data-stu-id="9ef51-161">Overview of cart and checkout pages</span></span>](quick-tour-cart-checkout.md)

[<span data-ttu-id="9ef51-162">Hesap yönetimi sayfalarına genel bakış</span><span class="sxs-lookup"><span data-stu-id="9ef51-162">Overview of account management pages</span></span>](quick-tour-account-management.md)

