---
title: Derecelendirmelere ve inceleme modülleri
description: Bu konu, Microsoft Dynamics 365 Commerce'un ürün ayrıntıları sayfalarında kullanılan derecelendirmeleri ve İnceleme modüllerini kapsamaktadır.
author: gvrmohanreddy
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
ms.author: gmohanv
ms.search.validFrom: 2020-10-31
ms.dyn365.ops.version: Release 10.0.6
ms.openlocfilehash: b17e986c2e30134c334cd547a85a1dd682172a0e
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/15/2021
ms.locfileid: "4979815"
---
# <a name="ratings-and-reviews-modules"></a><span data-ttu-id="0fb33-103">Derecelendirmelere ve inceleme modülleri</span><span class="sxs-lookup"><span data-stu-id="0fb33-103">Ratings and reviews modules</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="0fb33-104">Bu konu, Microsoft Dynamics 365 Commerce'un ürün ayrıntıları sayfalarında (PDP'ler) kullanılan derecelendirmeleri ve İnceleme modüllerini kapsamaktadır.</span><span class="sxs-lookup"><span data-stu-id="0fb33-104">This topic covers ratings and reviews modules used on product details pages (PDPs) in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="0fb33-105">Genel Bakış</span><span class="sxs-lookup"><span data-stu-id="0fb33-105">Overview</span></span>

<span data-ttu-id="0fb33-106">E-ticaret web sitelerindeki derecelendirmeler ve incelemeler, müşterilere bir satın alma kararı vermeden önce ürünler hakkında bilgi edinmesine yardımcı olur ve ürünlerle ilgili müşteri geribildirimi toplama mekanizmasıdır.</span><span class="sxs-lookup"><span data-stu-id="0fb33-106">Ratings and reviews on e-Commerce websites help customers learn about products before they make a purchase decision, and are also a mechanism for collecting customer feedback about products.</span></span> 

<span data-ttu-id="0fb33-107">Derecelendirmeler, ürün listesi sayfalarında, kategori listesi sayfalarında, arama sonuçları sayfalarında ve diğer site sayfalarında gösterilir.</span><span class="sxs-lookup"><span data-stu-id="0fb33-107">Ratings are shown on product list pages, category list pages, search results pages, and other site pages.</span></span> 

<span data-ttu-id="0fb33-108">Derecelendirme çubuk grafikleri ve ürün değerlendirmeleri, PDP'ler gösterilir.</span><span class="sxs-lookup"><span data-stu-id="0fb33-108">Ratings histograms and product reviews are shown on PDPs.</span></span> <span data-ttu-id="0fb33-109">**Gözden geçirme yazma** düğmesi müşterilerin bir ürün için derecelendirme ve İnceleme göndermelerini sağlar.</span><span class="sxs-lookup"><span data-stu-id="0fb33-109">A **Write a review** button lets customers submit ratings and reviews for a product.</span></span> <span data-ttu-id="0fb33-110">Bu PDP özellikleri derecelendirmelere göre denetlenir ve modülleri gözden geçirebilir.</span><span class="sxs-lookup"><span data-stu-id="0fb33-110">These PDP features are controlled by ratings and review modules.</span></span>

## <a name="ratings-and-reviews-modules-on-pdps"></a><span data-ttu-id="0fb33-111">PDP'lerde derecelendirmelere ve inceleme modülleri</span><span class="sxs-lookup"><span data-stu-id="0fb33-111">Ratings and reviews modules on PDPs</span></span> 

<span data-ttu-id="0fb33-112">Üç modül, PDP'ler üzerinde derecelendirme ve İnceleme özetini gösterir:</span><span class="sxs-lookup"><span data-stu-id="0fb33-112">Three modules show the ratings and reviews summary on PDPs:</span></span>
- <span data-ttu-id="0fb33-113">Gözden geçirme yazma modülü</span><span class="sxs-lookup"><span data-stu-id="0fb33-113">Write review module</span></span>
- <span data-ttu-id="0fb33-114">Ürün değerlendirmeleri liste modülü</span><span class="sxs-lookup"><span data-stu-id="0fb33-114">Product reviews list module</span></span>
- <span data-ttu-id="0fb33-115">Derecelendirme çubuk grafik modülü</span><span class="sxs-lookup"><span data-stu-id="0fb33-115">Ratings histogram module</span></span>
 
<span data-ttu-id="0fb33-116">Aşağıdaki şekil, bir PDP'de derecelendirmelerin ve gözden geçirme modüllerinin nasıl göründüğünü gösterir.</span><span class="sxs-lookup"><span data-stu-id="0fb33-116">The following illustration shows what the ratings and reviews modules look like on a PDP.</span></span>

![PDP'de derecelendirmelere ve inceleme modülleri](media/rnr-eCommerce-pdp-reviews-modules_design.png)

> [!TIP] 
> <span data-ttu-id="0fb33-118">PDP şablonlarını ve düzenlerini en iyi duruma getirme hakkında bilgi için (böylece e-ticaret sitenizde birden çok PDC arasındaki derecelendirme ve değerlendirme modülleriyle ilgili yapılandırmaları paylaşabilirsiniz) [şablonlar ve mizanpajlara genel bakış](templates-layouts-overview.md) konularına bakın.</span><span class="sxs-lookup"><span data-stu-id="0fb33-118">For information about how to optimize PDP templates and layouts so that you can share the configurations for ratings and reviews modules among multiple PDPs on your e-Commerce site, see [Templates and layouts overview](templates-layouts-overview.md).</span></span>

<span data-ttu-id="0fb33-119">Aşağıdaki şekil, **Modül Ekle** iletişim kutusunun Dynamics 365 Commerce'te derecelendirmeyi ve İnceleme modüllerini nasıl sunduğunu gösterir.</span><span class="sxs-lookup"><span data-stu-id="0fb33-119">The following illustration shows how the **Add module** dialog box presents ratings and reviews modules in Dynamics 365 Commerce.</span></span>
<span data-ttu-id="0fb33-120">![Modül Ekle iletişim kutusu](media/rnr-eCommerce-pdp-adding-rnr-modules.png)</span><span class="sxs-lookup"><span data-stu-id="0fb33-120">![Add module dialog box](media/rnr-eCommerce-pdp-adding-rnr-modules.png)</span></span>

### <a name="write-review-module"></a><span data-ttu-id="0fb33-121">Gözden geçirme yazma modülü</span><span class="sxs-lookup"><span data-stu-id="0fb33-121">Write review module</span></span>

<span data-ttu-id="0fb33-122">İnceleme yazma modülü, kullanıcıların bir ürünü oturum açmalarını, derecelendirmesine ve bir ürün incelemesi yazmalarına olanak tanıyan bir **inceleme yaz** düğmesi içerir.</span><span class="sxs-lookup"><span data-stu-id="0fb33-122">The write review module includes a **Write a review** button that lets users sign in, assign a rating, and write a review of a product.</span></span> <span data-ttu-id="0fb33-123">Bu modül ayrıca kullanıcıların daha önceden gönderdikleri bir derecelendirme veya gözden geçirmelerini sağlar.</span><span class="sxs-lookup"><span data-stu-id="0fb33-123">This module also lets users edit a rating or review that they previously submitted.</span></span> <span data-ttu-id="0fb33-124">Bu modül, bir PDP üzerinde genellikle derecelendirme çubuk grafiği ve ürün incelemeleri liste modüllerinin üzerinde görünür.</span><span class="sxs-lookup"><span data-stu-id="0fb33-124">This module typically appears above the ratings histogram and product reviews list modules on a PDP.</span></span>
<span data-ttu-id="0fb33-125">Aşağıdaki şekil, bir müşteri **gözden geçirme yaz** 'ı seçtiğinde beliren bir **gözden geçirme yazma** iletişim kutusunu göstermektedir.</span><span class="sxs-lookup"><span data-stu-id="0fb33-125">The following illustration shows the **Write a review** dialog box that appears when a customer selects **Write a review**.</span></span> <span data-ttu-id="0fb33-126">Müşteri bu iletişim kutusunu, bir derecelendirme ve İnceleme göndermek için kullanabilir.</span><span class="sxs-lookup"><span data-stu-id="0fb33-126">The customer can use this dialog box to submit a rating and a review.</span></span>
<span data-ttu-id="0fb33-127">![İnceleme yaz iletişim kutusu](media/rnr-eCommerce-write-review-module.png) Aşağıdaki tablo, geliştirme aracında konfigüre etmek için gereken yazma İnceleme modülünü gösterir.</span><span class="sxs-lookup"><span data-stu-id="0fb33-127">![Write a review dialog box](media/rnr-eCommerce-write-review-module.png) The following table shows the write review module property that needs to be configured in the authoring tool.</span></span>
| <span data-ttu-id="0fb33-128">Özellik adı</span><span class="sxs-lookup"><span data-stu-id="0fb33-128">Property name</span></span> | <span data-ttu-id="0fb33-129">Değer</span><span class="sxs-lookup"><span data-stu-id="0fb33-129">Value</span></span>        | <span data-ttu-id="0fb33-130">Özellik açıklaması</span><span class="sxs-lookup"><span data-stu-id="0fb33-130">Property description</span></span>                 |
|---------------|--------------|--------------------------------------|
| <span data-ttu-id="0fb33-131">Dosya Adı</span><span class="sxs-lookup"><span data-stu-id="0fb33-131">Name</span></span>          | <span data-ttu-id="0fb33-132">İnceleme yaz</span><span class="sxs-lookup"><span data-stu-id="0fb33-132">Write review</span></span> | <span data-ttu-id="0fb33-133">İnceleme yazma modülünün adı.</span><span class="sxs-lookup"><span data-stu-id="0fb33-133">The name of the write review module.</span></span> |

### <a name="ratings-histogram-module"></a><span data-ttu-id="0fb33-134">Derecelendirme çubuk grafik modülü</span><span class="sxs-lookup"><span data-stu-id="0fb33-134">Ratings histogram module</span></span>

<span data-ttu-id="0fb33-135">Derecelendirmeler çubuk grafik modülü bir derecelendirme çubuk grafik gösterir.</span><span class="sxs-lookup"><span data-stu-id="0fb33-135">The ratings histogram module shows a ratings histogram.</span></span> <span data-ttu-id="0fb33-136">Bu modül tipik olarak, bir PDP üzerindeki İnceleme yazma modülü ile ürün değerlendirmeleri listesi modülü arasında görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="0fb33-136">This module typically appears between the write review module and the product reviews list module on a PDP.</span></span>
<span data-ttu-id="0fb33-137">Derecelendirme çubuk grafiği modülü için konfigürasyon gerekmez.</span><span class="sxs-lookup"><span data-stu-id="0fb33-137">The ratings histogram module requires no configuration.</span></span> <span data-ttu-id="0fb33-138">Modülü PDP şablonuna eklemeniz yeterlidir.</span><span class="sxs-lookup"><span data-stu-id="0fb33-138">You just have to add the module in the PDP template.</span></span> <span data-ttu-id="0fb33-139">Aşağıdaki çizimler, PDP'lerde görüntülenmek üzere derecelendirmeler ve incelemeler modülleri yapılandırıldığında bir PDP şablonunun Dynamics 365 Commerce içinde nasıl göründüğünü gösterir.</span><span class="sxs-lookup"><span data-stu-id="0fb33-139">The following illustrations shows what a PDP template looks like in Dynamics 365 Commerce when ratings and reviews modules are configured for display on PDPs.</span></span>
<span data-ttu-id="0fb33-140">![PDP'lerde görüntülenmek üzere derecelendirme ve İncelemeler yapılandırıldığında PDP şablonu](media/rnr-eCommerce-pdp-reviews-modules.png)</span><span class="sxs-lookup"><span data-stu-id="0fb33-140">![PDP template when ratings and reviews are configured for display on PDPs](media/rnr-eCommerce-pdp-reviews-modules.png)</span></span>

### <a name="product-reviews-list-module"></a><span data-ttu-id="0fb33-141">Ürün değerlendirmeleri liste modülü</span><span class="sxs-lookup"><span data-stu-id="0fb33-141">Product reviews list module</span></span>

<span data-ttu-id="0fb33-142">Ürün gözden geçirme listesi modülü sıralama, filtre ve sayfalandırma seçenekleriyle birlikte ürün incelemelerinin listesini gösterir.</span><span class="sxs-lookup"><span data-stu-id="0fb33-142">The product reviews list module shows a list of product reviews together with sort, filter, and pagination options.</span></span> <span data-ttu-id="0fb33-143">Bu modül, genel olarak bir PDP üzerindeki derecelendirme çubuk grafik modülünden sonra görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="0fb33-143">This module typically appears after the ratings histogram module on a PDP.</span></span>
<span data-ttu-id="0fb33-144">Aşağıdaki tablo, geliştirme aracında konfigüre etmek için gereken ürün değerlendirmeleri listesi modülü özelliklerini gösterir.</span><span class="sxs-lookup"><span data-stu-id="0fb33-144">The following table shows the product reviews list module properties that need to be configured in the authoring tool.</span></span>

| <span data-ttu-id="0fb33-145">Özellik adı</span><span class="sxs-lookup"><span data-stu-id="0fb33-145">Property name</span></span>              | <span data-ttu-id="0fb33-146">Değer</span><span class="sxs-lookup"><span data-stu-id="0fb33-146">Value</span></span> | <span data-ttu-id="0fb33-147">Özellik açıklaması</span><span class="sxs-lookup"><span data-stu-id="0fb33-147">Property description</span></span> |
|----------------------------|-------| ---------------------|
| <span data-ttu-id="0fb33-148">her sayfada gösterilen incelemeler</span><span class="sxs-lookup"><span data-stu-id="0fb33-148">Reviews shown on each page</span></span> | <span data-ttu-id="0fb33-149">10</span><span class="sxs-lookup"><span data-stu-id="0fb33-149">10</span></span>    | <span data-ttu-id="0fb33-150">PDP'de bir seferde gösterilmesi gereken gözden geçirme sayısı.</span><span class="sxs-lookup"><span data-stu-id="0fb33-150">The number of reviews that should be shown at a time on a PDP.</span></span> <span data-ttu-id="0fb33-151">Kullanıcıların gözden geçirme sayfalarında hareket edebilmesi için **sonraki** ve **önceki** düğmeler eklenmiştir.</span><span class="sxs-lookup"><span data-stu-id="0fb33-151">**Next** and **Previous** buttons are included, so that users can move through the pages of reviews.</span></span> |

#### <a name="ratings-histogram--summary-view"></a><span data-ttu-id="0fb33-152">Derecelendirme çubuk grafiği – Özet görünümü</span><span class="sxs-lookup"><span data-stu-id="0fb33-152">Ratings histogram – Summary view</span></span>

<span data-ttu-id="0fb33-153">Ürün değerlendirmeleri listesi modülü, bir derecelendirme çubuk grafiği modülü ekleyebileceğiniz bir yuva içerir.</span><span class="sxs-lookup"><span data-stu-id="0fb33-153">The product reviews list module includes a slot where you can add a ratings histogram module.</span></span> <span data-ttu-id="0fb33-154">Aşağıdaki şekil, Dynamics 365 Commerce'teki Ürün İncelemeleri listesi modülünde bir derecelendirme çubuk grafiği modülünü nasıl ekleyekullanabileceğinizi gösterir .</span><span class="sxs-lookup"><span data-stu-id="0fb33-154">The following illustration shows how you can add a ratings histogram module in the product reviews list module in Dynamics 365 Commerce.</span></span>

![Ürün eleştiriler listesi modülünde derecelendirme çubuk grafiği modülü ekleme](media/rnr-eCommerce-pdp-rating-histogram-summary.png)

## <a name="additional-resources"></a><span data-ttu-id="0fb33-156">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="0fb33-156">Additional resources</span></span>

[<span data-ttu-id="0fb33-157">Modül kitaplığına genel bakış</span><span class="sxs-lookup"><span data-stu-id="0fb33-157">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="0fb33-158">Kapsayıcı modülü</span><span class="sxs-lookup"><span data-stu-id="0fb33-158">Container module</span></span>](add-container-module.md)

[<span data-ttu-id="0fb33-159">Alışveriş sepeti modülü</span><span class="sxs-lookup"><span data-stu-id="0fb33-159">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="0fb33-160">Ödeme yapma modülü</span><span class="sxs-lookup"><span data-stu-id="0fb33-160">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="0fb33-161">Sipariş onayı modülü</span><span class="sxs-lookup"><span data-stu-id="0fb33-161">Order confirmation module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="0fb33-162">Üst bilgi modülü</span><span class="sxs-lookup"><span data-stu-id="0fb33-162">Header module</span></span>](author-header-module.md)

[<span data-ttu-id="0fb33-163">Alt bilgi modülü</span><span class="sxs-lookup"><span data-stu-id="0fb33-163">Footer module</span></span>](author-footer-module.md)
