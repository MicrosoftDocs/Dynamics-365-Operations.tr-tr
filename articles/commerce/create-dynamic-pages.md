---
title: URL parametrelerini temel alan dinamik e-ticaret sayfaları oluşturma
description: Bu konuda, URL parametrelerine göre dinamik içerik sunabilen bir Microsoft Dynamics 365 Commerce e-ticaret sayfasının nasıl ayarlanacağı açıklanmaktadır.
author: StuHarg
ms.date: 01/28/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ROBOTS: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.author: stuharg
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: 8f59b80880e6947e1b45c110df0e78d4bdd57c5d
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/31/2021
ms.locfileid: "5795823"
---
# <a name="create-dynamic-e-commerce-pages-based-on-url-parameters"></a><span data-ttu-id="84d96-103">URL parametrelerini temel alan dinamik e-ticaret sayfaları oluşturma</span><span class="sxs-lookup"><span data-stu-id="84d96-103">Create dynamic e-commerce pages based on URL parameters</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="84d96-104">Bu konuda, URL parametrelerine göre dinamik içerik sunabilen bir Microsoft Dynamics 365 Commerce e-ticaret sayfasının nasıl ayarlanacağı açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="84d96-104">This topic describes how to set up a Microsoft Dynamics 365 Commerce e-commerce page that can serve dynamic content, based on URL parameters.</span></span>

<span data-ttu-id="84d96-105">Bir e-ticaret sayfası, URL yolundaki bir segmente göre farklı içerikler sunmak üzere yapılandırılabilir.</span><span class="sxs-lookup"><span data-stu-id="84d96-105">An e-commerce page can be configured to serve different content, based on a segment in the URL path.</span></span> <span data-ttu-id="84d96-106">Bu nedenle, sayfa dinamik sayfa olarak bilinir.</span><span class="sxs-lookup"><span data-stu-id="84d96-106">Therefore, the page is known as a dynamic page.</span></span> <span data-ttu-id="84d96-107">Segment, sayfa içeriğini almak için parametre olarak kullanılır.</span><span class="sxs-lookup"><span data-stu-id="84d96-107">The segment is used as a parameter to retrieve the page content.</span></span> <span data-ttu-id="84d96-108">Örneğin, **blog\_görüntüleyicisi** adlı bir sayfa oluşturulur ve `https://fabrikam.com/blog` URL'si ile ilişkilendirilir.</span><span class="sxs-lookup"><span data-stu-id="84d96-108">For example, a page that is named **blog\_viewer** is created and associated with the URL `https://fabrikam.com/blog`.</span></span> <span data-ttu-id="84d96-109">Bu sayfa daha sonra URL yolundaki son segmente göre farklı içerik göstermek için kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="84d96-109">This page can then be used to show different content, based on the last segment in the URL path.</span></span> <span data-ttu-id="84d96-110">Örneğin, `https://fabrikam.com/blog/article-1` URL'sindeki son segment **makale-1**'dir.</span><span class="sxs-lookup"><span data-stu-id="84d96-110">For example, the last segment in the URL `https://fabrikam.com/blog/article-1` is **article-1**.</span></span>

<span data-ttu-id="84d96-111">Dinamik sayfayı geçersiz kılan ayrı özel sayfalar da URL yolundaki segmentlerle ilişkilendirilebilir.</span><span class="sxs-lookup"><span data-stu-id="84d96-111">Separate custom pages that override the dynamic page can also be associated with segments in the URL path.</span></span> <span data-ttu-id="84d96-112">Örneğin, **blog\_özeti** adlı bir sayfa oluşturulur ve `https://fabrikam.com/blog/about-this-blog` URL'si ile ilişkilendirilir.</span><span class="sxs-lookup"><span data-stu-id="84d96-112">For example, a page that is named **blog\_summary** is created and associated with the URL `https://fabrikam.com/blog/about-this-blog`.</span></span> <span data-ttu-id="84d96-113">Bu URL istendiğinde, **blog\_görüntüleyici** sayfası yerine **/bu-blog-hakkinda** parametresiyle ilişkili **blog\_özeti** sayfası döndürülür.</span><span class="sxs-lookup"><span data-stu-id="84d96-113">When this URL is requested, the **blog\_summary** page that is associated with the **/about-this-blog** parameter is returned instead of the **blog\_viewer** page.</span></span>

> [!NOTE]
> <span data-ttu-id="84d96-114">Dinamik sayfa içeriğini barındırma, alma ve gösterme işlevi özel bir modül kullanılarak uygulanır.</span><span class="sxs-lookup"><span data-stu-id="84d96-114">The functionality for hosting, retrieving, and showing dynamic page content is implemented by using a custom module.</span></span> <span data-ttu-id="84d96-115">Daha fazla bilgi için, bkz. [Çevrimiçi kanal genişletilebilirliği](e-commerce-extensibility/overview.md).</span><span class="sxs-lookup"><span data-stu-id="84d96-115">For more information, see [Online channel extensibility](e-commerce-extensibility/overview.md).</span></span>

## <a name="set-up-a-dynamic-e-commerce-page"></a><span data-ttu-id="84d96-116">Dinamik e-ticaret sayfası ayarlama</span><span class="sxs-lookup"><span data-stu-id="84d96-116">Set up a dynamic e-commerce page</span></span>

<span data-ttu-id="84d96-117">Dinamik bir e-ticaret sayfası ayarlamak için dinamik sayfayı oluşturmanız, temel URL'yi oluşturmanız ve dinamik sayfaya giden yolu yapılandırmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="84d96-117">To set up a dynamic e-commerce page, you must create the dynamic page, create the base URL, and configure the route to the dynamic page.</span></span>

### <a name="create-the-page-that-will-serve-dynamic-content"></a><span data-ttu-id="84d96-118">Dinamik içeriğe hizmet edecek sayfayı oluşturma</span><span class="sxs-lookup"><span data-stu-id="84d96-118">Create the page that will serve dynamic content</span></span>

<span data-ttu-id="84d96-119">Dinamik içerik sunacak bir sayfa oluşturmak için [Yeni site sayfası ekleme](add-new-page.md) bölümündeki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="84d96-119">To create a page that will serve dynamic content, follow the steps in [Add a new site page](add-new-page.md).</span></span> <span data-ttu-id="84d96-120">Oluşturduğunuz sayfa, dış veri kaynağından içerik almak için URL yolundaki son segmenti kullanan bir modülün uygulanmasını gerektirir.</span><span class="sxs-lookup"><span data-stu-id="84d96-120">The page that you create will require implementation of a module that uses the last segment in the URL path to retrieve content from an external data source.</span></span> <span data-ttu-id="84d96-121">Özel modül geliştirme hakkında daha fazla bilgi için bkz. [Çevrimiçi kanal genişletilebilirliği](e-commerce-extensibility/overview.md).</span><span class="sxs-lookup"><span data-stu-id="84d96-121">For more information about custom module development, see [Online channel extensibility](e-commerce-extensibility/overview.md).</span></span>

### <a name="create-the-base-url-for-the-dynamic-page"></a><span data-ttu-id="84d96-122">Dinamik sayfa için temel URL oluşturma</span><span class="sxs-lookup"><span data-stu-id="84d96-122">Create the base URL for the dynamic page</span></span>

<span data-ttu-id="84d96-123">Commerce Site Builder'da dinamik sayfa için temel oluşturmak üzere aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="84d96-123">To create the base URL for the dynamic page in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="84d96-124">**URL'ler** bölümüne gidin ve **Yeni \> Yeni URL**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="84d96-124">Go to **URLs**, and select **New \> New URL**.</span></span>
1. <span data-ttu-id="84d96-125">**Yeni URL oluştur** iletişim kutusunda **Dahili sayfalar**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="84d96-125">In the **Create new URL** dialog box, select **Internal page**.</span></span> <span data-ttu-id="84d96-126">**URL yolu** altında, dinamik sayfa için kök olarak kullanılacak yolu girin (bu örnekte, **/blog**).</span><span class="sxs-lookup"><span data-stu-id="84d96-126">Under **URL path**, enter the path that will serve as the root for the dynamic page (in this example, **/blog**).</span></span> <span data-ttu-id="84d96-127">Sonra **İleri**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="84d96-127">Then select **Next**.</span></span>
1. <span data-ttu-id="84d96-128">**Sayfa seçin** iletişim kutusunda dinamik sayfa olarak kullanılması için oluşturduğunuz sayfayı ve sonra **Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="84d96-128">In the **Select a page** dialog box, select the page that you created to serve as the dynamic page, and then select **Save**.</span></span>
1. <span data-ttu-id="84d96-129">**Yayımla**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="84d96-129">Select **Publish**.</span></span>

### <a name="configure-the-route-to-the-dynamic-page"></a><span data-ttu-id="84d96-130">Dinamik sayfa yolunu yapılandırma</span><span class="sxs-lookup"><span data-stu-id="84d96-130">Configure the route to the dynamic page</span></span>

<span data-ttu-id="84d96-131">Commerce Site Builder'da dinamik sayfa yolunu yapılandırmak için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="84d96-131">To configure the route to the dynamic page in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="84d96-132">**Site Ayarları \> Uzantılar**'a gidin.</span><span class="sxs-lookup"><span data-stu-id="84d96-132">Go to **Site Settings \> Extensions**.</span></span>
1. <span data-ttu-id="84d96-133">**Parametreli URL yolları** altında, **Ekle**'yi seçin ve URL'yi oluştururken girdiğiniz URL yolunu girin (bu örnekte, **/blog**).</span><span class="sxs-lookup"><span data-stu-id="84d96-133">Under **Parameterized URL paths**, select **Add**, and then enter the URL path that you entered when you created the URL (in this example, **/blog**).</span></span>
1. <span data-ttu-id="84d96-134">**Kaydet ve yayınla** yı seçin.</span><span class="sxs-lookup"><span data-stu-id="84d96-134">Select **Save and publish**.</span></span>

<span data-ttu-id="84d96-135">Yol yapılandırıldıktan sonra, parametreli URL yoluna yapılan tüm istekler bu URL ile ilişkilendirilmiş sayfayı döndürür.</span><span class="sxs-lookup"><span data-stu-id="84d96-135">After the route is configured, all requests to the parameterized URL path will return the page that is associated with that URL.</span></span> <span data-ttu-id="84d96-136">Herhangi bir istekte ek bir segment varsa, ilişkili sayfa döndürülür ve sayfa içeriği segment parametresi olarak kullanılarak alınır.</span><span class="sxs-lookup"><span data-stu-id="84d96-136">If any requests contain an additional segment, the associated page will be returned, and the page content will be retrieved by using the segment as a parameter.</span></span> <span data-ttu-id="84d96-137">Örneğin, `https://fabrikam.com/blog/article-1`, **blog\_özeti** sayfasını döndürür ve sayfa içeriği **/makale-1** parametresi kullanılarak getirilir.</span><span class="sxs-lookup"><span data-stu-id="84d96-137">For example, `https://fabrikam.com/blog/article-1` will return the **blog\_summary** page, and the page content will be retrieved by using the **/article-1** parameter.</span></span>

## <a name="override-a-parameterized-url-with-a-custom-page"></a><span data-ttu-id="84d96-138">Parametreli URL'yi özel bir sayfayla geçersiz kılma</span><span class="sxs-lookup"><span data-stu-id="84d96-138">Override a parameterized URL with a custom page</span></span>

<span data-ttu-id="84d96-139">Commerce Site Builder'da özel bir sayfayla parametreli URL'yi geçersiz kılmak için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="84d96-139">To override a parameterized URL with a custom page in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="84d96-140">**URL'ler** bölümüne gidin ve **Yeni \> Yeni URL**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="84d96-140">Go to **URLs**, and select **New \> New URL**.</span></span>
1. <span data-ttu-id="84d96-141">**Yeni URL oluştur** iletişim kutusunda **Dahili sayfalar**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="84d96-141">In the **Create new URL** dialog box, select **Internal page**.</span></span> <span data-ttu-id="84d96-142">**URL yolu** altında, geçersiz kılınacak segmenti içeren yolu girin (bu örnekte, **/blog/bu-blog-hakkinda**) girin.</span><span class="sxs-lookup"><span data-stu-id="84d96-142">Under **URL path**, enter the path that includes the segment to override (in this example, **/blog/about-this-blog**).</span></span> <span data-ttu-id="84d96-143">Sonra **İleri**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="84d96-143">Then select **Next**.</span></span>
1. <span data-ttu-id="84d96-144">**Bir sayfa seçin** iletişim kutusunda özel sayfayı seçin ve sonra **Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="84d96-144">In the **Select a page** dialog box, select the custom page, and then select **Save**.</span></span>
1. <span data-ttu-id="84d96-145">**Yayımla**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="84d96-145">Select **Publish**.</span></span>
1. <span data-ttu-id="84d96-146">Özel sayfa henüz yayılanmadıysa, **Sayfalar**'a gidin, özel sayfayı seçin ve sonra **Yayınla**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="84d96-146">If the custom page hasn't yet been published, go to **Pages**, select the custom page, and then select **Publish**.</span></span>

<span data-ttu-id="84d96-147">Özel sayfa yayınlandıktan sonra, üzerinde parametreli içerik bulunan dinamik sayfa yerine hizmet sunulur.</span><span class="sxs-lookup"><span data-stu-id="84d96-147">After the custom page is published, it will be served instead of the dynamic page that has parameterized content.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="84d96-148">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="84d96-148">Additional resources</span></span>

[<span data-ttu-id="84d96-149">Var olan site sayfasını değiştirme</span><span class="sxs-lookup"><span data-stu-id="84d96-149">Modify an existing site page</span></span>](modify-existing-page.md)

[<span data-ttu-id="84d96-150">Yeni site sayfası ekleme</span><span class="sxs-lookup"><span data-stu-id="84d96-150">Add a new site page</span></span>](add-new-page.md)

[<span data-ttu-id="84d96-151">Sayfa düzeni seçme</span><span class="sxs-lookup"><span data-stu-id="84d96-151">Select page layouts</span></span>](select-page-layouts.md)

[<span data-ttu-id="84d96-152">SEO meta verilerini yönetme</span><span class="sxs-lookup"><span data-stu-id="84d96-152">Manage SEO metadata</span></span>](manage-seo-metadata.md)

[<span data-ttu-id="84d96-153">Sayfa kaydetme, önizleme ve yayımlama</span><span class="sxs-lookup"><span data-stu-id="84d96-153">Save, preview, and publish a page</span></span>](save-preview-publish-page.md)

[<span data-ttu-id="84d96-154">Ürün sayfasını zenginleştirme</span><span class="sxs-lookup"><span data-stu-id="84d96-154">Enrich a product page</span></span>](enrich-product-page.md)

[<span data-ttu-id="84d96-155">Kategori açılış sayfasını zenginleştirme</span><span class="sxs-lookup"><span data-stu-id="84d96-155">Enrich a category landing page</span></span>](enrich-category-page.md)

[<span data-ttu-id="84d96-156">Sayfa içeriği erişilebilirliğini doğrulama</span><span class="sxs-lookup"><span data-stu-id="84d96-156">Verify page content accessibility</span></span>](verify-accessibility.md)

[<span data-ttu-id="84d96-157">Çevrimiçi kanal genişletilebilirliği</span><span class="sxs-lookup"><span data-stu-id="84d96-157">Online channel extensibility</span></span>](e-commerce-extensibility/overview.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
