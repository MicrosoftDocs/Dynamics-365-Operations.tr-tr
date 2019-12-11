---
title: URL sayfası oluşturma
description: Bu konu, sitenizde sayfa URL'SI oluşturmaya yönelik temel kavramları ve yordamları kapsamaktadır.
author: bicyclingfool
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
ms.author: StuHarg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: ab7325dd4060392ed43e59c1ad48069d294d81c0
ms.sourcegitcommit: 295d940a345879b3dfc5991e387b91c7257019ea
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/01/2019
ms.locfileid: "2697560"
---
# <a name="create-a-page-url"></a><span data-ttu-id="cdbb1-103">URL sayfası oluşturma</span><span class="sxs-lookup"><span data-stu-id="cdbb1-103">Create a page URL</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="cdbb1-104">Bu konu, sitenizde sayfa URL'SI oluşturmaya yönelik temel kavramları ve yordamları kapsamaktadır.</span><span class="sxs-lookup"><span data-stu-id="cdbb1-104">This topic covers the basic concepts and procedures for creating a page URL on your site.</span></span>

## <a name="overview"></a><span data-ttu-id="cdbb1-105">Genel Bakış</span><span class="sxs-lookup"><span data-stu-id="cdbb1-105">Overview</span></span>

<span data-ttu-id="cdbb1-106">Sitenizdeki bir sayfaya işaret eden tam veya mutlak URL, farklı bölümlerden oluşur.</span><span class="sxs-lookup"><span data-stu-id="cdbb1-106">The full, or absolute, URL that points to a page on your site consists of distinct parts.</span></span> <span data-ttu-id="cdbb1-107">Örneğin, URL `https://www.contoso.com/en-us/contactus` aşağıdaki bölümlerden oluşur:</span><span class="sxs-lookup"><span data-stu-id="cdbb1-107">For example, the URL `https://www.contoso.com/en-us/contactus` has the following parts:</span></span>

- <span data-ttu-id="cdbb1-108">`https://www.contoso.com` – HTTP iletişim kuralı ve sitenin etki alanı.</span><span class="sxs-lookup"><span data-stu-id="cdbb1-108">`https://www.contoso.com` – The HTTP protocol and the site's domain.</span></span>
- <span data-ttu-id="cdbb1-109">`/en-us`– Sitenin dil yolu.</span><span class="sxs-lookup"><span data-stu-id="cdbb1-109">`/en-us` – The site's language path.</span></span>
- <span data-ttu-id="cdbb1-110">`/contactus` – **Bize Ulaşın** sayfasının göreli URL'si.</span><span class="sxs-lookup"><span data-stu-id="cdbb1-110">`/contactus` – The relative URL for the **Contact Us** page.</span></span> <span data-ttu-id="cdbb1-111">Göreli URL, URL *bilgi* olarak da bilinir.</span><span class="sxs-lookup"><span data-stu-id="cdbb1-111">A relative URL is also known as a URL *slug*.</span></span>

<span data-ttu-id="cdbb1-112">Siteyi kurarken sitenizin etki alanını ve isteğe bağlı dil yolunu kurarsınız.</span><span class="sxs-lookup"><span data-stu-id="cdbb1-112">You establish your site's domain and optional language path when you set up the site.</span></span> <span data-ttu-id="cdbb1-113">Sitenin ayarlarındaki çevrimiçi mağazalar sayfası yoluyla sitenize başka etki alanları ve dil yolları ekleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="cdbb1-113">You can add more domains and language paths to your site through the online stores page in the site's settings.</span></span>

<span data-ttu-id="cdbb1-114">Bir sayfanın URL adresi, site geliştirme ortamında bağımsız bir varlık olarak bulunur.</span><span class="sxs-lookup"><span data-stu-id="cdbb1-114">The URL slug for a page exists as a standalone entity in the site authoring environment.</span></span> <span data-ttu-id="cdbb1-115">Sayfa URL'si iki bölümden oluşur: URL bilgisinin temsil ettiği bir ad ve sitenizdeki veya dış sitedeki bir sayfaya işaretçi.</span><span class="sxs-lookup"><span data-stu-id="cdbb1-115">A page URL consists of two parts: a name that represents the URL slug, and a pointer to a page on either your site or an external site.</span></span> <span data-ttu-id="cdbb1-116">Sayfa URL'Si Ayrıca, sitenizdeki veya dış sitedeki başka bir sayfaya yeniden yönlendirme işlevi görecek şekilde de yapılandırılabilir.</span><span class="sxs-lookup"><span data-stu-id="cdbb1-116">A page URL can also be configured to act as a redirect to another page on either your site or an external site.</span></span>

## <a name="create-a-page-url"></a><span data-ttu-id="cdbb1-117">URL sayfası oluşturma</span><span class="sxs-lookup"><span data-stu-id="cdbb1-117">Create a page URL</span></span>

<span data-ttu-id="cdbb1-118">Sayfa URL'leri oluşturmanın iki yolu vardır:</span><span class="sxs-lookup"><span data-stu-id="cdbb1-118">There are two ways to create page URLs:</span></span>

- <span data-ttu-id="cdbb1-119">Otomatik olarak, bir sayfa oluşturduğunuzda</span><span class="sxs-lookup"><span data-stu-id="cdbb1-119">Automatically, when you create a page</span></span>
- <span data-ttu-id="cdbb1-120">El ile, **URL'ler** sayfasından</span><span class="sxs-lookup"><span data-stu-id="cdbb1-120">Manually, from the **URLs** page</span></span>

### <a name="create-a-page-url-when-you-create-a-page"></a><span data-ttu-id="cdbb1-121">Sayfa oluştururken sayfa URL'Si oluşturma</span><span class="sxs-lookup"><span data-stu-id="cdbb1-121">Create a page URL when you create a page</span></span>

<span data-ttu-id="cdbb1-122">Yeni sayfa oluştururken **URL** alanında bir ad sağlarsanız, **URL'ler** sayfasında otomatik olarak bu sayfaya işaret eden bir sayfa URL'si oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="cdbb1-122">If you provide a name in the **URL** field when you create a new page, a page URL that points to that page is automatically created on the **URLs** page.</span></span> <span data-ttu-id="cdbb1-123">URL'yi ve işaret eden sayfayı yayımladıktan sonra, site kullanıcıları (müşterileriniz) URL ile ilişkilendirilmiş olan sayfaya erişebilir.</span><span class="sxs-lookup"><span data-stu-id="cdbb1-123">After you publish the URL and the page that it points to, site users (your customers) can access the page that is associated with the URL.</span></span>

> [!NOTE]
> <span data-ttu-id="cdbb1-124">İşaret ettiği sayfayı yayımlamadan bir URL'yi yayımlarsanız, site kullanıcıları sayfaya erişmeye çalıştıklarında bir 404 hatası alırlar.</span><span class="sxs-lookup"><span data-stu-id="cdbb1-124">If you publish a URL without publishing the page that it points to, site users receive a 404 error when they try to access the page.</span></span> <span data-ttu-id="cdbb1-125">Bir sayfayı üzerinde işaret eden bir URL'yi yayımlamadan yayımlarsanız, sayfaya bir URL kullanılarak erişilemez.</span><span class="sxs-lookup"><span data-stu-id="cdbb1-125">If you publish a page without publishing the URL that points to it, the page can't be accessed by using a URL.</span></span>

### <a name="manually-create-a-page-url"></a><span data-ttu-id="cdbb1-126">Manuel olarak sayfa URL'si oluşturma</span><span class="sxs-lookup"><span data-stu-id="cdbb1-126">Manually create a page URL</span></span>

<span data-ttu-id="cdbb1-127">Yeni sayfalar oluşturduğunuzda, bir sayfa URL'si belirtmeniz gerekmez.</span><span class="sxs-lookup"><span data-stu-id="cdbb1-127">When you create new pages, you aren't required to specify a page URL.</span></span> <span data-ttu-id="cdbb1-128">URL alanını boş bırakırsanız, sayfa bağlantısız durumda oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="cdbb1-128">If you leave the URL field blank, the page is created in an unlinked state.</span></span> <span data-ttu-id="cdbb1-129">Bu durumda, yayımlanmış olsa bile, müşteriler sayfaya erişemez.</span><span class="sxs-lookup"><span data-stu-id="cdbb1-129">In this case, customers won't be able to access the page, even if it's published.</span></span> <span data-ttu-id="cdbb1-130">Sayfayı erişilebilir duruma getirmek için, URL'yi el ile oluşturmanız ve sayfaya bağlamanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="cdbb1-130">To make the page accessible, you must manually create the URL and link it to the page.</span></span>

<span data-ttu-id="cdbb1-131">Bir sayfa için sayfa URL'sini manuel oluşturmak için, aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="cdbb1-131">To manually create the page URL for a page, follow these steps.</span></span>

1. <span data-ttu-id="cdbb1-132">**URL'ler** sayfasında, **Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="cdbb1-132">On the **URLs** page, select **New**.</span></span>
1. <span data-ttu-id="cdbb1-133">URL ile ilişkilendirileceği site sayfasını seçin.</span><span class="sxs-lookup"><span data-stu-id="cdbb1-133">Select the site page to associate with the URL.</span></span>
1. <span data-ttu-id="cdbb1-134">Bir URL bilgisi girin ve **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="cdbb1-134">Enter the URL slug, and then select **OK**.</span></span>

<span data-ttu-id="cdbb1-135">Bu noktada, URL Taslak durumundadır.</span><span class="sxs-lookup"><span data-stu-id="cdbb1-135">At this point, the URL is in a draft state.</span></span> <span data-ttu-id="cdbb1-136">Site kullanıcılarının ilişkili sayfaya erişebilmesi için önce bu sitenin yayımlanması gerekir.</span><span class="sxs-lookup"><span data-stu-id="cdbb1-136">It must be published before site users can access the associated page.</span></span>

## <a name="update-a-page-url"></a><span data-ttu-id="cdbb1-137">Sayfa URL'si güncelleme</span><span class="sxs-lookup"><span data-stu-id="cdbb1-137">Update a page URL</span></span>

<span data-ttu-id="cdbb1-138">Sayfa URL'sinin hedef sayfasını güncelleştirmek için, aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="cdbb1-138">To update the target page of a page URL, follow these steps.</span></span>

1. <span data-ttu-id="cdbb1-139">**URL'ler** sayfasında güncelleştirilecek URL'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="cdbb1-139">On the **URLs** page, select the URL to update.</span></span>
1. <span data-ttu-id="cdbb1-140">Sağdaki özellik bölmesinde hedef sayfa alanının yanında üç nokta düğmesini (**...**) seçin.</span><span class="sxs-lookup"><span data-stu-id="cdbb1-140">In the property pane on the right, select the ellipsis button (**...**) next to the target page field.</span></span>
1. <span data-ttu-id="cdbb1-141">İletişim kutusunda , farklı bir sayfa seçin ve **Tamam**'ı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="cdbb1-141">In the dialog box, select a different page, and then select **OK**.</span></span>
1. <span data-ttu-id="cdbb1-142">URL'yi kaydet ve yayınlayın.</span><span class="sxs-lookup"><span data-stu-id="cdbb1-142">Save and publish the URL.</span></span>

## <a name="redirect-a-page-url"></a><span data-ttu-id="cdbb1-143">Sayfa URL'sini yeniden yönlendir</span><span class="sxs-lookup"><span data-stu-id="cdbb1-143">Redirect a page URL</span></span>

<span data-ttu-id="cdbb1-144">Bazen, belirli bir URL'yi istediklerinde müşterilerinizin farklı sayfaları görüntülemesini isteyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="cdbb1-144">Sometimes, you might want your customers to view a different page when they request a specific URL.</span></span> <span data-ttu-id="cdbb1-145">Bu durumlarda, en iyi ve en kolay yaklaşım genellikle sayfa URL'sinin işaret ettiği sayfayı değiştirir.</span><span class="sxs-lookup"><span data-stu-id="cdbb1-145">In these cases, the best and easiest approach is often to change the page that the page URL points to.</span></span> <span data-ttu-id="cdbb1-146">Ancak, HTTP 301 veya 3023 isteklerinin bir URL'yi farklı bir URL'ye yeniden yönlendirmek için yasal sebeplere sahip olabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="cdbb1-146">However, you might have legitimate reasons for using HTTP 301 or 3023 redirects to redirect requests for a URL to a different URL.</span></span>

<span data-ttu-id="cdbb1-147">Bir URL'Yi farklı bir URL'ye yeniden yönlendirmek için, aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="cdbb1-147">To redirect a URL to a different URL, follow these steps.</span></span>

1. <span data-ttu-id="cdbb1-148">**URL'ler** sayfasında güncelleştirilecek URL'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="cdbb1-148">On the **URLs** page, select the URL to update.</span></span>
1. <span data-ttu-id="cdbb1-149">Sağdaki Özellik bölmesinde **yeniden yönlendir**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="cdbb1-149">In the property pane on the right, select **Redirect**.</span></span>
1. <span data-ttu-id="cdbb1-150">Yeniden yönlendirme için hedef seçin:</span><span class="sxs-lookup"><span data-stu-id="cdbb1-150">Select a destination for the redirect:</span></span>

    - <span data-ttu-id="cdbb1-151">Sitenizdeki başka bir sayfayı işaret etmek için, **Dahili URL** seçin, üç nokta düğmesini (**...**) ve sonra yeniden yönlendirilecek URL 'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="cdbb1-151">To point to another page on your site, select **Internal URL**, select the ellipsis button (**...**), and then select the URL to redirect to.</span></span>
    - <span data-ttu-id="cdbb1-152">Harici bir sitesindeki sayfayı işaret etmek için **Harici URL** seçeneğini belirleyin ve sonra o sayfanın tam URL'sini girin.</span><span class="sxs-lookup"><span data-stu-id="cdbb1-152">To point to a page on an external site, select **External URL**, and then enter the full URL for that page.</span></span> <span data-ttu-id="cdbb1-153">İletişim kuralını eklediğinizden emin olun.</span><span class="sxs-lookup"><span data-stu-id="cdbb1-153">Be sure to include the protocol.</span></span> <span data-ttu-id="cdbb1-154">Örneğin `https://domain.com/new/page` yazın.</span><span class="sxs-lookup"><span data-stu-id="cdbb1-154">For example, enter `https://domain.com/new/page`.</span></span> <span data-ttu-id="cdbb1-155">URL zaten dahili bir URL'ye yeniden yönlendiriyorsa, harici bir URL girmek için **seçimi temizle**'yi seçmelisiniz.</span><span class="sxs-lookup"><span data-stu-id="cdbb1-155">If the URL already redirects to an internal URL, you must select **Clear selection** before you can enter an external URL.</span></span>

1. <span data-ttu-id="cdbb1-156">Bir yeniden yönlendirme türü seçin:</span><span class="sxs-lookup"><span data-stu-id="cdbb1-156">Select a redirect type:</span></span>

    - <span data-ttu-id="cdbb1-157">**Kalıcı yeniden yönlendirme (301)** – içeriğinizin kalıcı olarak taşınmakta olduğunu ve önceki URL'sini geri döndürmeyinizi biliyorsanız bu seçeneği belirleyin.</span><span class="sxs-lookup"><span data-stu-id="cdbb1-157">**Permanent redirect (301)** – Select this option when you know that your content is moving permanently and won't revert to its previous URL.</span></span> <span data-ttu-id="cdbb1-158">Arama motorları, yeniden yönlendirme URL'sinin arama motoru iyileştirme (SEO) değerini, yeni URL'yi göstermek üzere kendi kayıtlarını yönlendirmekte olan URL'ye atayacaktır.</span><span class="sxs-lookup"><span data-stu-id="cdbb1-158">Search engines will assign the search engine optimization (SEO) value of the redirecting URL to the URL that is being redirected to and update their record to show the new URL.</span></span> 
    - <span data-ttu-id="cdbb1-159">**Geçici yeniden yönlendirme (302)** – akışı, arama altyapılarını güncelleştirmeden yeniden yönlendirmek için bu seçeneği belirleyin.</span><span class="sxs-lookup"><span data-stu-id="cdbb1-159">**Temporary redirect (302)** – Select this option to redirect traffic without updating search engines.</span></span> <span data-ttu-id="cdbb1-160">Bu yaklaşım genellikle içerik önceki URL'sine geri dönürseniz kullanılır.</span><span class="sxs-lookup"><span data-stu-id="cdbb1-160">This approach is typically used if the content will soon revert to its previous URL.</span></span>

1. <span data-ttu-id="cdbb1-161">Yeniden yönlendirmeyi uygulamaya hazır olduğunuzda, URL'yi kaydedin ve yayınlayın.</span><span class="sxs-lookup"><span data-stu-id="cdbb1-161">When you're ready to implement the redirect, save and publish the URL.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="cdbb1-162">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="cdbb1-162">Additional resources</span></span>

[<span data-ttu-id="cdbb1-163">Site gezintisini özelleştirme</span><span class="sxs-lookup"><span data-stu-id="cdbb1-163">Customize site navigation</span></span>](customize-site-navigation.md)

[<span data-ttu-id="cdbb1-164">Yeni site sayfası ekleme</span><span class="sxs-lookup"><span data-stu-id="cdbb1-164">Add a new site page</span></span>](add-new-page.md)

[<span data-ttu-id="cdbb1-165">Etki alanı adınızı yapılandırma</span><span class="sxs-lookup"><span data-stu-id="cdbb1-165">Configure your domain name</span></span>](configure-your-domain-name.md)

[<span data-ttu-id="cdbb1-166">Sitenize dil ekleme</span><span class="sxs-lookup"><span data-stu-id="cdbb1-166">Add languages to your site</span></span>](add-languages-to-site.md)
