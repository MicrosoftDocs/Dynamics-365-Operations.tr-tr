---
title: Derecelendirme ve incelemeleri yapılandırma
description: Bu konuda, e-ticaret sitenizi Microsoft Dynamics 365 Commerce'te müşteri derecelendirmelerini ve incelemelerini gösterecek şekilde konfigüre etme yöntemi açıklanmıştır.
author: gvrmohanreddy
manager: annbe
ms.date: 10/01/2019
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
ms.author: gmohanv
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 0612b32e7751b32ad851f627a53bce2ac491870f
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/06/2019
ms.locfileid: "2770493"
---
# <a name="configure-ratings-and-reviews"></a><span data-ttu-id="4d87d-103">Derecelendirme ve incelemeleri yapılandırma</span><span class="sxs-lookup"><span data-stu-id="4d87d-103">Configure ratings and reviews</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="4d87d-104">Bu konuda, e-ticaret sitenizi Microsoft Dynamics 365 Commerce'te müşteri derecelendirmelerini ve incelemelerini gösterecek şekilde konfigüre etme yöntemi açıklanmıştır.</span><span class="sxs-lookup"><span data-stu-id="4d87d-104">This topic describes how to configure your e-Commerce site to show customer ratings and reviews in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="4d87d-105">Genel Bakış</span><span class="sxs-lookup"><span data-stu-id="4d87d-105">Overview</span></span>

<span data-ttu-id="4d87d-106">E-ticaret web sitelerindeki derecelendirmeler ve incelemeler, müşterilere bir satın alma kararı vermeden önce, bu ürünler hakkındaki diğer müşterilerin ne düşündüğünü göstererek, ürünler hakkında bilgi edinmesine yardımcı olur.</span><span class="sxs-lookup"><span data-stu-id="4d87d-106">Ratings and reviews on e-Commerce websites help customers learn about products before they make a purchase decision, by showing them what other customers think about those products.</span></span> <span data-ttu-id="4d87d-107">E-ticaret web sitelerinde, derecelendirmeler ve incelemeler, ürünler hakkında müşteri geribildirimi toplamaya yönelik bir mekanizmadır.</span><span class="sxs-lookup"><span data-stu-id="4d87d-107">For e-Commerce websites, ratings and reviews are also a mechanism for collecting customer feedback about products.</span></span> 

<span data-ttu-id="4d87d-108">Derecelendirmeler, ürün listesi sayfalarında, kategori listesi sayfalarında, arama sonuçları sayfalarında ve diğer site sayfalarında gösterilir.</span><span class="sxs-lookup"><span data-stu-id="4d87d-108">Ratings are shown on product list pages, category list pages, search results pages, and other site pages.</span></span> <span data-ttu-id="4d87d-109">Derecelendirme çubuk grafikleri ve ürün değerlendirmeleri, ürün ayrıntıları sayfalarında (PDPs) gösterilir.</span><span class="sxs-lookup"><span data-stu-id="4d87d-109">Ratings histograms and product reviews are shown on product details pages (PDPs).</span></span> <span data-ttu-id="4d87d-110">**Gözden geçirme yazma** düğmesi müşterilerin bir ürün için derecelendirme ve İnceleme göndermelerini sağlar.</span><span class="sxs-lookup"><span data-stu-id="4d87d-110">A **Write a review** button lets customers submit ratings and reviews for a product.</span></span>

## <a name="ratings-and-reviews-modules-on-pdps"></a><span data-ttu-id="4d87d-111">PDP'lerde derecelendirmelere ve inceleme modülleri</span><span class="sxs-lookup"><span data-stu-id="4d87d-111">Ratings and reviews modules on PDPs</span></span> 

<span data-ttu-id="4d87d-112">Üç modül, PDP'ler üzerinde derecelendirme ve İnceleme özetini gösterir:</span><span class="sxs-lookup"><span data-stu-id="4d87d-112">Three modules show the ratings and reviews summary on PDPs:</span></span>

- <span data-ttu-id="4d87d-113">Gözden geçirme yazma modülü</span><span class="sxs-lookup"><span data-stu-id="4d87d-113">Write review module</span></span>
- <span data-ttu-id="4d87d-114">Ürün değerlendirmeleri liste modülü</span><span class="sxs-lookup"><span data-stu-id="4d87d-114">Product reviews list module</span></span>
- <span data-ttu-id="4d87d-115">Derecelendirme çubuk grafik modülü</span><span class="sxs-lookup"><span data-stu-id="4d87d-115">Ratings histogram module</span></span>
 
<span data-ttu-id="4d87d-116">Aşağıdaki şekil, bir PDP'de derecelendirmelerin ve gözden geçirme modüllerinin nasıl göründüğünü gösterir.</span><span class="sxs-lookup"><span data-stu-id="4d87d-116">The following illustration shows what the ratings and reviews modules look like on a PDP.</span></span>

![PDP'de derecelendirmelere ve inceleme modülleri](media/rnr-eCommerce-pdp-reviews-modules_design.png)

> [!TIP] 
> <span data-ttu-id="4d87d-118">PDP şablonlarını ve düzenlerini en iyi duruma getirme hakkında bilgi için (böylece e-ticaret sitenizde birden çok PDC arasındaki derecelendirme ve değerlendirme modülleriyle ilgili yapılandırmaları paylaşabilirsiniz) [şablonlar ve mizanpajlara genel bakış](templates-layouts-overview.md) konularına bakın.</span><span class="sxs-lookup"><span data-stu-id="4d87d-118">For information about how to optimize PDP templates and layouts so that you can share the configurations for ratings and reviews modules among multiple PDPs on your e-Commerce site, see [Templates and layouts overview](templates-layouts-overview.md).</span></span>

<span data-ttu-id="4d87d-119">Aşağıdaki şekil, **Modül Ekle** iletişim kutusunun Dynamics 365 Commerce'te derecelendirmeyi ve İnceleme modüllerini nasıl sunduğunu gösterir.</span><span class="sxs-lookup"><span data-stu-id="4d87d-119">The following illustration shows how the **Add module** dialog box presents ratings and reviews modules in Dynamics 365 Commerce.</span></span>

![Modül Ekle iletişim kutusu](media/rnr-eCommerce-pdp-adding-rnr-modules.png)

### <a name="write-review-module"></a><span data-ttu-id="4d87d-121">Gözden geçirme yazma modülü</span><span class="sxs-lookup"><span data-stu-id="4d87d-121">Write review module</span></span>

<span data-ttu-id="4d87d-122">İnceleme yazma modülü, kullanıcıların bir ürünü oturum açmalarını, derecelendirmesine ve bir ürün incelemesi yazmalarına olanak tanıyan bir **inceleme yaz** düğmesi içerir.</span><span class="sxs-lookup"><span data-stu-id="4d87d-122">The write review module includes a **Write a review** button that lets users sign in, assign a rating, and write a review of a product.</span></span> <span data-ttu-id="4d87d-123">Bu modül ayrıca kullanıcıların daha önceden gönderdikleri bir derecelendirme veya gözden geçirmelerini sağlar.</span><span class="sxs-lookup"><span data-stu-id="4d87d-123">This module also lets users edit a rating or review that they previously submitted.</span></span> <span data-ttu-id="4d87d-124">Bu modül, bir PDP üzerinde genellikle derecelendirme çubuk grafiği ve ürün incelemeleri liste modüllerinin üzerinde görünür.</span><span class="sxs-lookup"><span data-stu-id="4d87d-124">This module typically appears above the ratings histogram and product reviews list modules on a PDP.</span></span>

<span data-ttu-id="4d87d-125">Aşağıdaki şekil, bir müşteri **gözden geçirme yaz** 'ı seçtiğinde beliren bir **gözden geçirme yazma** iletişim kutusunu göstermektedir.</span><span class="sxs-lookup"><span data-stu-id="4d87d-125">The following illustration shows the **Write a review** dialog box that appears when a customer selects **Write a review**.</span></span> <span data-ttu-id="4d87d-126">Müşteri bu iletişim kutusunu, bir derecelendirme ve İnceleme göndermek için kullanabilir.</span><span class="sxs-lookup"><span data-stu-id="4d87d-126">The customer can use this dialog box to submit a rating and a review.</span></span>

![Gözden geçirme iletişim kutusu yazma](media/rnr-eCommerce-write-review-module.png)

<span data-ttu-id="4d87d-128">Aşağıdaki tablo, geliştirme aracında konfigüre etmek için gereken yazma İnceleme modülünü gösterir.</span><span class="sxs-lookup"><span data-stu-id="4d87d-128">The following table shows the write review module property that needs to be configured in the authoring tool.</span></span>

| <span data-ttu-id="4d87d-129">Özellik adı</span><span class="sxs-lookup"><span data-stu-id="4d87d-129">Property name</span></span> | <span data-ttu-id="4d87d-130">Değer</span><span class="sxs-lookup"><span data-stu-id="4d87d-130">Value</span></span>        | <span data-ttu-id="4d87d-131">Özellik açıklaması</span><span class="sxs-lookup"><span data-stu-id="4d87d-131">Property description</span></span>                 |
|---------------|--------------|--------------------------------------|
| <span data-ttu-id="4d87d-132">Dosya Adı</span><span class="sxs-lookup"><span data-stu-id="4d87d-132">Name</span></span>          | <span data-ttu-id="4d87d-133">İnceleme yaz</span><span class="sxs-lookup"><span data-stu-id="4d87d-133">Write review</span></span> | <span data-ttu-id="4d87d-134">İnceleme yazma modülünün adı.</span><span class="sxs-lookup"><span data-stu-id="4d87d-134">The name of the write review module.</span></span> |

### <a name="ratings-histogram-module"></a><span data-ttu-id="4d87d-135">Derecelendirme çubuk grafik modülü</span><span class="sxs-lookup"><span data-stu-id="4d87d-135">Ratings histogram module</span></span>

<span data-ttu-id="4d87d-136">Derecelendirmeler çubuk grafik modülü bir derecelendirme çubuk grafik gösterir.</span><span class="sxs-lookup"><span data-stu-id="4d87d-136">The ratings histogram module shows a ratings histogram.</span></span> <span data-ttu-id="4d87d-137">Bu modül tipik olarak, bir PDP üzerindeki İnceleme yazma modülü ile ürün değerlendirmeleri listesi modülü arasında görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="4d87d-137">This module typically appears between the write review module and the product reviews list module on a PDP.</span></span>

<span data-ttu-id="4d87d-138">Derecelendirme çubuk grafiği modülü için konfigürasyon gerekmez.</span><span class="sxs-lookup"><span data-stu-id="4d87d-138">The ratings histogram module requires no configuration.</span></span> <span data-ttu-id="4d87d-139">Modülü PDP şablonuna eklemeniz yeterlidir.</span><span class="sxs-lookup"><span data-stu-id="4d87d-139">You just have to add the module in the PDP template.</span></span> 

<span data-ttu-id="4d87d-140">Aşağıdaki çizimler, PDP'lerde görüntülenmek üzere derecelendirmeler ve incelemeler modülleri yapılandırıldığında bir PDP şablonunun Dynamics 365 Commerce içinde nasıl göründüğünü gösterir.</span><span class="sxs-lookup"><span data-stu-id="4d87d-140">The following illustrations shows what a PDP template looks like in Dynamics 365 Commerce when ratings and reviews modules are configured for display on PDPs.</span></span>

![PDP'lerde görüntülenmek üzere derecelendirme ve İncelemeler yapılandırıldığında PDP şablonu](media/rnr-eCommerce-pdp-reviews-modules.png)

### <a name="product-reviews-list-module"></a><span data-ttu-id="4d87d-142">Ürün değerlendirmeleri liste modülü</span><span class="sxs-lookup"><span data-stu-id="4d87d-142">Product reviews list module</span></span>

<span data-ttu-id="4d87d-143">Ürün gözden geçirme listesi modülü sıralama, filtre ve sayfalandırma seçenekleriyle birlikte ürün incelemelerinin listesini gösterir.</span><span class="sxs-lookup"><span data-stu-id="4d87d-143">The product reviews list module shows a list of product reviews together with sort, filter, and pagination options.</span></span> <span data-ttu-id="4d87d-144">Bu modül, genel olarak bir PDP üzerindeki derecelendirme çubuk grafik modülünden sonra görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="4d87d-144">This module typically appears after the ratings histogram module on a PDP.</span></span>

<span data-ttu-id="4d87d-145">Aşağıdaki tablo, geliştirme aracında konfigüre etmek için gereken ürün değerlendirmeleri listesi modülü özelliklerini gösterir.</span><span class="sxs-lookup"><span data-stu-id="4d87d-145">The following table shows the product reviews list module properties that need to be configured in the authoring tool.</span></span>

| <span data-ttu-id="4d87d-146">Özellik adı</span><span class="sxs-lookup"><span data-stu-id="4d87d-146">Property name</span></span>              | <span data-ttu-id="4d87d-147">Değer</span><span class="sxs-lookup"><span data-stu-id="4d87d-147">Value</span></span> | <span data-ttu-id="4d87d-148">Özellik açıklaması</span><span class="sxs-lookup"><span data-stu-id="4d87d-148">Property description</span></span> |
|----------------------------|-------| ---------------------|
| <span data-ttu-id="4d87d-149">her sayfada gösterilen incelemeler</span><span class="sxs-lookup"><span data-stu-id="4d87d-149">Reviews shown on each page</span></span> | <span data-ttu-id="4d87d-150">10</span><span class="sxs-lookup"><span data-stu-id="4d87d-150">10</span></span>    | <span data-ttu-id="4d87d-151">PDP'de bir seferde gösterilmesi gereken gözden geçirme sayısı.</span><span class="sxs-lookup"><span data-stu-id="4d87d-151">The number of reviews that should be shown at a time on a PDP.</span></span> <span data-ttu-id="4d87d-152">Kullanıcıların gözden geçirme sayfalarında hareket edebilmesi için **sonraki** ve **önceki** düğmeler eklenmiştir.</span><span class="sxs-lookup"><span data-stu-id="4d87d-152">**Next** and **Previous** buttons are included, so that users can move through the pages of reviews.</span></span> |

#### <a name="ratings-histogram--summary-view"></a><span data-ttu-id="4d87d-153">Derecelendirme çubuk grafiği – Özet görünümü</span><span class="sxs-lookup"><span data-stu-id="4d87d-153">Ratings histogram – Summary view</span></span>

<span data-ttu-id="4d87d-154">Ürün değerlendirmeleri listesi modülü, bir derecelendirme çubuk grafiği modülü ekleyebileceğiniz bir yuva içerir.</span><span class="sxs-lookup"><span data-stu-id="4d87d-154">The product reviews list module includes a slot where you can add a ratings histogram module.</span></span> <span data-ttu-id="4d87d-155">Aşağıdaki şekil, Dynamics 365 Commerce'teki Ürün İncelemeleri listesi modülünde bir derecelendirme çubuk grafiği modülünü nasıl ekleyekullanabileceğinizi gösterir .</span><span class="sxs-lookup"><span data-stu-id="4d87d-155">The following illustration shows how you can add a ratings histogram module in the product reviews list module in Dynamics 365 Commerce.</span></span>

![Ürün eleştiriler listesi modülünde derecelendirme çubuk grafiği modülü ekleme](media/rnr-eCommerce-pdp-rating-histogram-summary.png)

## <a name="configure-a-site-to-show-ratings-and-reviews"></a><span data-ttu-id="4d87d-157">Derecelendirme ve incelemeleri gösterecek site yapılandırma</span><span class="sxs-lookup"><span data-stu-id="4d87d-157">Configure a site to show ratings and reviews</span></span>

<span data-ttu-id="4d87d-158">Kiracı kimliği, metin uzunluğunu gözden geçirme ve Başlık uzunluğunu gözden geçirme gibi derecelendirmeler ve incelemelerde ilgili konfigürasyon değerleri site düzeyinde yapılandırılır.</span><span class="sxs-lookup"><span data-stu-id="4d87d-158">Configuration values for ratings and reviews, such as the tenant ID, review text length, and review title length, are configured at the site level.</span></span> 

<span data-ttu-id="4d87d-159">Derecelendirmeleri ve değerlendirmeleri göstermek üzere bir site yapılandırmak için, aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="4d87d-159">To configure a site to show ratings and reviews, follow these steps.</span></span> 

1. <span data-ttu-id="4d87d-160">**Ev \> Siteler**e gidin.</span><span class="sxs-lookup"><span data-stu-id="4d87d-160">Go to **Home \> Sites**.</span></span>
1. <span data-ttu-id="4d87d-161">Sitenizin adını belirtin.</span><span class="sxs-lookup"><span data-stu-id="4d87d-161">Select the name of your site.</span></span> 
1. <span data-ttu-id="4d87d-162">**Site yönetimi \> Genişletilebilirliği** bölümüne gidin.</span><span class="sxs-lookup"><span data-stu-id="4d87d-162">Go to **Site management \> Extensibility**.</span></span> 
1. <span data-ttu-id="4d87d-163">**En fazla metni gözden geçir** alanına, metni İnceleme için gereken maksimum karakter sayısını (örneğin, **1000**) girin.</span><span class="sxs-lookup"><span data-stu-id="4d87d-163">In the **Review Text Max Length** field, enter the maximum number of characters that review text can have (for example, **1000**).</span></span> 
1. <span data-ttu-id="4d87d-164">**En fazla başlık gözden geçir** alanına, başlık İnceleme için gereken maksimum karakter sayısını (örneğin, **55**) girin.</span><span class="sxs-lookup"><span data-stu-id="4d87d-164">In the **Review Title Max Length** field, enter the maximum number of characters that review titles can have (for example, **55**).</span></span> 
1. <span data-ttu-id="4d87d-165">**kaydet ve yayınla**yı seçin.</span><span class="sxs-lookup"><span data-stu-id="4d87d-165">Select **Save and Publish**.</span></span> 

<span data-ttu-id="4d87d-166">Aşağıdaki çizim, bu yapılandırmasının Dynamics 365 Commerce'te nasıl gözükeceğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="4d87d-166">The following illustration shows what this configuration looks like in Dynamics 365 Commerce.</span></span>

![Derecelendirme ve incelemeleri gösterecek site yapılandırma](media/rnr-eCommerce-site-appsettings.png)

## <a name="link-a-product-rating-to-the-reviews-section-of-a-pdp"></a><span data-ttu-id="4d87d-168">Bir ürün derecelendirmesini PDP'nin incelemeler bölümüne bağlama</span><span class="sxs-lookup"><span data-stu-id="4d87d-168">Link a product rating to the Reviews section of a PDP</span></span>

<span data-ttu-id="4d87d-169">Ürün derecelendirmesi, PDP'nin en üstünde ürün başlığının altında gösterilir.</span><span class="sxs-lookup"><span data-stu-id="4d87d-169">A product rating is shown below the product title at the top of PDP.</span></span> <span data-ttu-id="4d87d-170">Ürün derecelendirmesi, aynı PDP'nin **incelemeler** bölümüyle bağlantılı olacak şekilde konfigüre edilebilir.</span><span class="sxs-lookup"><span data-stu-id="4d87d-170">The product rating can be configured so that it's linked to the **Reviews** section of the same PDP.</span></span> 

<span data-ttu-id="4d87d-171">Bir ürün derecelendirmesini PDP 'nin **incelemeler** bölümüne bağlamak için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="4d87d-171">To link a product rating to the **Reviews** section of the PDP, follow these steps.</span></span>

1. <span data-ttu-id="4d87d-172">PDP şablonu açın.</span><span class="sxs-lookup"><span data-stu-id="4d87d-172">Open the PDP template.</span></span> 
1. <span data-ttu-id="4d87d-173">**Satın alma kutusu konteyner modülü ayarlarına** git.</span><span class="sxs-lookup"><span data-stu-id="4d87d-173">Go to **Buy box container module settings**.</span></span>
1. <span data-ttu-id="4d87d-174">**Satınalma kutusu** altında, **ürün derecelendirmeleri**'ni seçin ve sonra **bağlantıyı tam gözden geçirme modülü için tıklatın** onay kutusunu seçin.</span><span class="sxs-lookup"><span data-stu-id="4d87d-174">Under **Buy box**, select **Product ratings**, and then select the **Link the click to full reviews module** check box.</span></span>

<span data-ttu-id="4d87d-175">Aşağıdaki çizim, bu yapılandırmasının Dynamics 365 Commerce'te nasıl gözükeceğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="4d87d-175">The following illustration shows what this configuration looks like in Dynamics 365 Commerce.</span></span>

![Bir ürün derecelendirmesini PDP'nin incelemeler bölümüne bağlama](media/rnr-eCommerce-buy-box-rating-summary.png)

## <a name="configure-the-link-for-the-privacy-and-policy-page"></a><span data-ttu-id="4d87d-177">Gizlilik ve ilke sayfası için bağlantıyı yapılandırın</span><span class="sxs-lookup"><span data-stu-id="4d87d-177">Configure the link for the privacy and policy page</span></span>

<span data-ttu-id="4d87d-178">Gizlilik ve ilke sayfası için bağlantıyı yapılandırmak için şu adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="4d87d-178">To configure the link for the privacy and policy page, follow these steps.</span></span>

1. <span data-ttu-id="4d87d-179">**Ev \> Siteler**e gidin.</span><span class="sxs-lookup"><span data-stu-id="4d87d-179">Go to **Home \> Sites**.</span></span>
1. <span data-ttu-id="4d87d-180">Sitenizin adını belirtin.</span><span class="sxs-lookup"><span data-stu-id="4d87d-180">Select the name of your site.</span></span> 
1. <span data-ttu-id="4d87d-181">**Site yönetimi \> Genişletilebilirliği** bölümüne gidin</span><span class="sxs-lookup"><span data-stu-id="4d87d-181">Go to **Site management \> Extensibility**</span></span>
1. <span data-ttu-id="4d87d-182">**Rotalar** sekmesinde, **RNR Gizlilik ve ilke** altında **bağlantı ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="4d87d-182">On the **Routes** tab, under **RNR Privacy and Policy**, select **Add a link**.</span></span> <span data-ttu-id="4d87d-183">Zaten bir bağlantı girilmiş ve bunu değiştirmek istiyorsanız, bağlantıyı seçin.</span><span class="sxs-lookup"><span data-stu-id="4d87d-183">If a link is already entered, and you want to replace it, select the link.</span></span> 
1. <span data-ttu-id="4d87d-184">**Bağlantı ekle** iletişim kutusunda gizlilik ve ilke sayfası bağlantısını seçin ve **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="4d87d-184">In the **Add a link** dialog box, select the link for the privacy and policy page, and then select **OK**.</span></span> 
1. <span data-ttu-id="4d87d-185">**kaydet ve yayınla**yı seçin.</span><span class="sxs-lookup"><span data-stu-id="4d87d-185">Select **Save and Publish**.</span></span> 

<span data-ttu-id="4d87d-186">Aşağıdaki çizim, bu yapılandırmasının Dynamics 365 Commerce'te nasıl gözükeceğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="4d87d-186">The following illustration shows what this configuration looks like in Dynamics 365 Commerce.</span></span>

![Gizlilik ve ilke sayfası için bağlantıyı yapılandırın](media/rnr-eCommerce-rnr-privacy-policy-link.png)

## <a name="additional-resources"></a><span data-ttu-id="4d87d-188">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="4d87d-188">Additional resources</span></span>

[<span data-ttu-id="4d87d-189">Derecelendirme ve incelemelere genel bakış</span><span class="sxs-lookup"><span data-stu-id="4d87d-189">Ratings and reviews overview</span></span>](ratings-reviews-overview.md)

[<span data-ttu-id="4d87d-190">Derecelendirme ve incelemeleri kullanmayı kabul etme</span><span class="sxs-lookup"><span data-stu-id="4d87d-190">Opt in to use ratings and reviews</span></span>](opt-in-ratings-reviews.md)

[<span data-ttu-id="4d87d-191">Derecelendirme ve incelemeleri yönetme</span><span class="sxs-lookup"><span data-stu-id="4d87d-191">Manage ratings and reviews</span></span>](manage-reviews.md)

[<span data-ttu-id="4d87d-192">Dynamics 365 Retail'de ürün derecelendirmelerini eşitleme</span><span class="sxs-lookup"><span data-stu-id="4d87d-192">Sync product ratings in Dynamics 365 Retail</span></span>](sync-product-ratings.md)
