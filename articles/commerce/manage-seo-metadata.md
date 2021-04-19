---
title: SEO meta verilerini yönetme
description: Bu konuda, Microsoft Dynamics 365 Commerce'ta arama motoru optimizasyonu (SEO) meta verilerinin nasıl yönetileceği açıklanmaktadır.
author: psimolin
ms.date: 04/14/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 1e03ef346df92a94b0a403f241d0f7d1f64fd210
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/31/2021
ms.locfileid: "5794223"
---
# <a name="manage-seo-metadata"></a><span data-ttu-id="88202-103">SEO meta verilerini yönetme</span><span class="sxs-lookup"><span data-stu-id="88202-103">Manage SEO metadata</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="88202-104">Bu konuda, Microsoft Dynamics 365 Commerce'ta arama motoru optimizasyonu (SEO) meta verilerinin nasıl yönetileceği açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="88202-104">This topic describes how to manage search engine optimization (SEO) metadata in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="88202-105">Bir sitenin SEO meta verileri, site haritaları ve sayfa meta verileri kullanılarak yönetilebilir.</span><span class="sxs-lookup"><span data-stu-id="88202-105">SEO metadata for a site can be managed by using site maps and page metadata.</span></span>
    
## <a name="site-maps"></a><span data-ttu-id="88202-106">Site haritaları</span><span class="sxs-lookup"><span data-stu-id="88202-106">Site maps</span></span>

<span data-ttu-id="88202-107">Site haritası, Web sitenizdeki sayfaların, XML biçimindeki, makine tarafından okunabilen bir listesidir.</span><span class="sxs-lookup"><span data-stu-id="88202-107">A site map is a machine-readable list, in XML format, of the pages on your website.</span></span> <span data-ttu-id="88202-108">Arama motorları tarafından, sitenizde daha iyi arama sonuçları sağlayabilmeleri için tüketilmesi amaçlanmıştır.</span><span class="sxs-lookup"><span data-stu-id="88202-108">It's intended to be consumed by search engines, so that they can provide better search results from your site.</span></span> <span data-ttu-id="88202-109">Site eşlemeleri arama motorları tarafından el ile gerçekleştirilebilir veya robots. txt dosyasında yayımlanabilir.</span><span class="sxs-lookup"><span data-stu-id="88202-109">Site maps can be manually ingested by search engines or published in a robots.txt file.</span></span>

<span data-ttu-id="88202-110">Dynamics 365 Commerce Site eşlemelerinin otomatik olarak oluşturulmasını destekler.</span><span class="sxs-lookup"><span data-stu-id="88202-110">Dynamics 365 Commerce supports automatic generation of site maps.</span></span> <span data-ttu-id="88202-111">Sayfalar yayımlanana ve yayımdan kaldırılmış olduğunda, site eşleştirmeleri otomatik olarak güncelleştirilir.</span><span class="sxs-lookup"><span data-stu-id="88202-111">Site maps are automatically updated when pages are published and unpublished.</span></span>

### <a name="turn-on-site-map-generation"></a><span data-ttu-id="88202-112">Site Haritası oluşturmayı aç</span><span class="sxs-lookup"><span data-stu-id="88202-112">Turn on site map generation</span></span>

1. <span data-ttu-id="88202-113">Geliştirme aracında oturum açın.</span><span class="sxs-lookup"><span data-stu-id="88202-113">Sign in to the authoring tool.</span></span>
1. <span data-ttu-id="88202-114">**Siteler** altında, **Fabrikam**'ı seçin (veya sitenizin adını).</span><span class="sxs-lookup"><span data-stu-id="88202-114">Under **Sites**, select **Fabrikam** (or the name of your site).</span></span>
1. <span data-ttu-id="88202-115">Soldaki gezinti bölmesinde **Site Yönetimi** seçin.</span><span class="sxs-lookup"><span data-stu-id="88202-115">In the navigation pane on the left, select **Site Management**.</span></span>
1. <span data-ttu-id="88202-116">**Site haritaları etkin** seçeneğinin açık olduğundan emin olun.</span><span class="sxs-lookup"><span data-stu-id="88202-116">Make sure that the **Site maps enabled** option is turned on.</span></span>

## <a name="page-metadata"></a><span data-ttu-id="88202-117">Sayfa meta verileri</span><span class="sxs-lookup"><span data-stu-id="88202-117">Page metadata</span></span>

<span data-ttu-id="88202-118">Dynamics 365 Commerce Her bir sayfa için SEO meta verilerini yönetmenizi sağlar.</span><span class="sxs-lookup"><span data-stu-id="88202-118">Dynamics 365 Commerce lets you manage SEO metadata for individual pages.</span></span> <span data-ttu-id="88202-119">Bu bilgileri bir sayfa kapsayıcısının **SEO Özellikler** bölümünde görüntüleyebilir ve değiştirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="88202-119">You can view and modify this information in the **SEO Properties** section of a page container.</span></span> <span data-ttu-id="88202-120">Şu anda aşağıdaki SEO meta veri özellikleri desteklenmektedir:</span><span class="sxs-lookup"><span data-stu-id="88202-120">The following SEO metadata properties are supported:</span></span>

- <span data-ttu-id="88202-121">Ünvan</span><span class="sxs-lookup"><span data-stu-id="88202-121">Title</span></span>
- <span data-ttu-id="88202-122">Tanım</span><span class="sxs-lookup"><span data-stu-id="88202-122">Description</span></span>
- <span data-ttu-id="88202-123">SEO Anahtar sözcükler</span><span class="sxs-lookup"><span data-stu-id="88202-123">SEO keywords</span></span>
- <span data-ttu-id="88202-124">Aria etiketleri</span><span class="sxs-lookup"><span data-stu-id="88202-124">Aria labels</span></span>
- <span data-ttu-id="88202-125">noindex</span><span class="sxs-lookup"><span data-stu-id="88202-125">noindex</span></span>
- <span data-ttu-id="88202-126">nofollow</span><span class="sxs-lookup"><span data-stu-id="88202-126">nofollow</span></span>
- <span data-ttu-id="88202-127">noarchive</span><span class="sxs-lookup"><span data-stu-id="88202-127">noarchive</span></span>
- <span data-ttu-id="88202-128">nocache</span><span class="sxs-lookup"><span data-stu-id="88202-128">nocache</span></span>
- <span data-ttu-id="88202-129">noOpenDirectoryProject</span><span class="sxs-lookup"><span data-stu-id="88202-129">noOpenDirectoryProject</span></span>
- <span data-ttu-id="88202-130">nosnippet</span><span class="sxs-lookup"><span data-stu-id="88202-130">nosnippet</span></span>
- <span data-ttu-id="88202-131">noImageIndex</span><span class="sxs-lookup"><span data-stu-id="88202-131">noImageIndex</span></span>
- <span data-ttu-id="88202-132">unavailableAfter</span><span class="sxs-lookup"><span data-stu-id="88202-132">unavailableAfter</span></span>

### <a name="modify-page-metadata"></a><span data-ttu-id="88202-133">Sayfa meta verilerini Değiştir</span><span class="sxs-lookup"><span data-stu-id="88202-133">Modify page metadata</span></span>

<span data-ttu-id="88202-134">Sayfa meta verilerini değiştirmek için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="88202-134">To modify page metadata, follow these steps.</span></span>

1. <span data-ttu-id="88202-135">**Siteler** altında, **Fabrikam**'ı seçin (veya sitenizin adını).</span><span class="sxs-lookup"><span data-stu-id="88202-135">Under **Sites**, select the **Fabrikam** (or the name of your site).</span></span>
1. <span data-ttu-id="88202-136">Soldaki gezinti bölmesinde **Sayfalar** seçin.</span><span class="sxs-lookup"><span data-stu-id="88202-136">In the navigation pane on the left, select **Pages**.</span></span>
1. <span data-ttu-id="88202-137">Sayfa düzenleyicisinde açmak için giriş sayfasını seçin.</span><span class="sxs-lookup"><span data-stu-id="88202-137">Select the home page to open it in the page editor.</span></span>
1. <span data-ttu-id="88202-138">Komut çubuğunda, **Düzenle** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="88202-138">On the command bar, select **Edit**.</span></span>
1. <span data-ttu-id="88202-139">Sağdaki özellikler bölmesinde, **Varsayılan meta verileri** genişletin.</span><span class="sxs-lookup"><span data-stu-id="88202-139">In the properties pane on the right, expand **Default metatags**.</span></span>
1. <span data-ttu-id="88202-140">Yeni bir metaetiketi eklemek için, **Ekle**'yi seçin ve alana etiketi girin.</span><span class="sxs-lookup"><span data-stu-id="88202-140">To add a new metatag, select **Add**, and then enter the tag in the field.</span></span> <span data-ttu-id="88202-141">Varolan bir meta etiketi kaldırmak için, sağ tarafta bulunan çöp tenekesi sembolünü seçin.</span><span class="sxs-lookup"><span data-stu-id="88202-141">To remove an existing metatag, select the trash can symbol to the right of it.</span></span>
1. <span data-ttu-id="88202-142">**Kaydet** i seçin ve sonra **Düzenlemeyi bitir**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="88202-142">Select **Save**, and then select **Finish editing**.</span></span>
1. <span data-ttu-id="88202-143">**Yorumlar** alanında **Güncellenen meta etiketler** seçeneğini girin ve **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="88202-143">In the **Comments** field, enter **Updated metatags**, and then select **OK**.</span></span>
1. <span data-ttu-id="88202-144">Sayfanızın önizlemesini görüntülemek için **Önizleme**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="88202-144">Select **Preview** to preview your page.</span></span> <span data-ttu-id="88202-145">Bitirdiğinizde, geliştirme aracına dönmek için Önizleme sekmesini kapatın.</span><span class="sxs-lookup"><span data-stu-id="88202-145">When you've finished, close the preview tab to return to the authoring tool.</span></span>
1. <span data-ttu-id="88202-146">**Yayımla**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="88202-146">Select **Publish**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="88202-147">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="88202-147">Additional resources</span></span>

[<span data-ttu-id="88202-148">Var olan site sayfasını değiştirme</span><span class="sxs-lookup"><span data-stu-id="88202-148">Modify an existing site page</span></span>](modify-existing-page.md)

[<span data-ttu-id="88202-149">Yeni site sayfası ekleme</span><span class="sxs-lookup"><span data-stu-id="88202-149">Add a new site page</span></span>](add-new-page.md)

[<span data-ttu-id="88202-150">Sayfa düzeni seçme</span><span class="sxs-lookup"><span data-stu-id="88202-150">Select page layouts</span></span>](select-page-layouts.md)

[<span data-ttu-id="88202-151">Sayfa kaydetme, önizleme ve yayımlama</span><span class="sxs-lookup"><span data-stu-id="88202-151">Save, preview, and publish a page</span></span>](save-preview-publish-page.md)

[<span data-ttu-id="88202-152">Ürün sayfasını zenginleştirme</span><span class="sxs-lookup"><span data-stu-id="88202-152">Enrich a product page</span></span>](enrich-product-page.md)

[<span data-ttu-id="88202-153">Kategori açılış sayfasını zenginleştirme</span><span class="sxs-lookup"><span data-stu-id="88202-153">Enrich a category landing page</span></span>](enrich-category-page.md)

[<span data-ttu-id="88202-154">Sayfa içeriği erişilebilirliğini doğrulama</span><span class="sxs-lookup"><span data-stu-id="88202-154">Verify page content accessibility</span></span>](verify-accessibility.md)

[<span data-ttu-id="88202-155">URL parametrelerini temel alan dinamik e-ticaret sayfaları oluşturma</span><span class="sxs-lookup"><span data-stu-id="88202-155">Create dynamic e-commerce pages based on URL parameters</span></span>](create-dynamic-pages.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
