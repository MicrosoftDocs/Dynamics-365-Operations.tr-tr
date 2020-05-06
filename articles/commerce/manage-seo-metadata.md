---
title: SEO meta verilerini yönetme
description: Bu konuda, Microsoft Dynamics 365 Commerce'ta arama motoru optimizasyonu (SEO) meta verilerinin nasıl yönetileceği açıklanmaktadır.
author: psimolin
manager: annbe
ms.date: 04/14/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 74229628e48ffb8ac974acd868e325eeca77d91e
ms.sourcegitcommit: 7a1d01122790b904e2d96a7ea9f1d003392358a6
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/17/2020
ms.locfileid: "3270062"
---
# <a name="manage-seo-metadata"></a><span data-ttu-id="49062-103">SEO meta verilerini yönetme</span><span class="sxs-lookup"><span data-stu-id="49062-103">Manage SEO metadata</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="49062-104">Bu konuda, Microsoft Dynamics 365 Commerce'ta arama motoru optimizasyonu (SEO) meta verilerinin nasıl yönetileceği açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="49062-104">This topic describes how to manage search engine optimization (SEO) metadata in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="49062-105">Genel Bakış</span><span class="sxs-lookup"><span data-stu-id="49062-105">Overview</span></span>

<span data-ttu-id="49062-106">Bir sitenin SEO meta verileri, site haritaları ve sayfa meta verileri kullanılarak yönetilebilir.</span><span class="sxs-lookup"><span data-stu-id="49062-106">SEO metadata for a site can be managed by using site maps and page metadata.</span></span>
    
## <a name="site-maps"></a><span data-ttu-id="49062-107">Site haritaları</span><span class="sxs-lookup"><span data-stu-id="49062-107">Site maps</span></span>

<span data-ttu-id="49062-108">Site haritası, Web sitenizdeki sayfaların, XML biçimindeki, makine tarafından okunabilen bir listesidir.</span><span class="sxs-lookup"><span data-stu-id="49062-108">A site map is a machine-readable list, in XML format, of the pages on your website.</span></span> <span data-ttu-id="49062-109">Arama motorları tarafından, sitenizde daha iyi arama sonuçları sağlayabilmeleri için tüketilmesi amaçlanmıştır.</span><span class="sxs-lookup"><span data-stu-id="49062-109">It's intended to be consumed by search engines, so that they can provide better search results from your site.</span></span> <span data-ttu-id="49062-110">Site eşlemeleri arama motorları tarafından el ile gerçekleştirilebilir veya robots. txt dosyasında yayımlanabilir.</span><span class="sxs-lookup"><span data-stu-id="49062-110">Site maps can be manually ingested by search engines or published in a robots.txt file.</span></span>

<span data-ttu-id="49062-111">Dynamics 365 Commerce Site eşlemelerinin otomatik olarak oluşturulmasını destekler.</span><span class="sxs-lookup"><span data-stu-id="49062-111">Dynamics 365 Commerce supports automatic generation of site maps.</span></span> <span data-ttu-id="49062-112">Sayfalar yayımlanana ve yayımdan kaldırılmış olduğunda, site eşleştirmeleri otomatik olarak güncelleştirilir.</span><span class="sxs-lookup"><span data-stu-id="49062-112">Site maps are automatically updated when pages are published and unpublished.</span></span>

### <a name="turn-on-site-map-generation"></a><span data-ttu-id="49062-113">Site Haritası oluşturmayı aç</span><span class="sxs-lookup"><span data-stu-id="49062-113">Turn on site map generation</span></span>

1. <span data-ttu-id="49062-114">Geliştirme aracında oturum açın.</span><span class="sxs-lookup"><span data-stu-id="49062-114">Sign in to the authoring tool.</span></span>
1. <span data-ttu-id="49062-115">**Siteler** altında, **Fabrikam**'ı seçin (veya sitenizin adını).</span><span class="sxs-lookup"><span data-stu-id="49062-115">Under **Sites**, select **Fabrikam** (or the name of your site).</span></span>
1. <span data-ttu-id="49062-116">Soldaki gezinti bölmesinde **Site Yönetimi** seçin.</span><span class="sxs-lookup"><span data-stu-id="49062-116">In the navigation pane on the left, select **Site Management**.</span></span>
1. <span data-ttu-id="49062-117">**Site haritaları etkin** seçeneğinin açık olduğundan emin olun.</span><span class="sxs-lookup"><span data-stu-id="49062-117">Make sure that the **Site maps enabled** option is turned on.</span></span>

## <a name="page-metadata"></a><span data-ttu-id="49062-118">Sayfa meta verileri</span><span class="sxs-lookup"><span data-stu-id="49062-118">Page metadata</span></span>

<span data-ttu-id="49062-119">Dynamics 365 Commerce Her bir sayfa için SEO meta verilerini yönetmenizi sağlar.</span><span class="sxs-lookup"><span data-stu-id="49062-119">Dynamics 365 Commerce lets you manage SEO metadata for individual pages.</span></span> <span data-ttu-id="49062-120">Bu bilgileri bir sayfa kapsayıcısının **SEO Özellikler** bölümünde görüntüleyebilir ve değiştirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="49062-120">You can view and modify this information in the **SEO Properties** section of a page container.</span></span> <span data-ttu-id="49062-121">Şu anda aşağıdaki SEO meta veri özellikleri desteklenmektedir:</span><span class="sxs-lookup"><span data-stu-id="49062-121">The following SEO metadata properties are supported:</span></span>

- <span data-ttu-id="49062-122">Ünvan</span><span class="sxs-lookup"><span data-stu-id="49062-122">Title</span></span>
- <span data-ttu-id="49062-123">Tanım</span><span class="sxs-lookup"><span data-stu-id="49062-123">Description</span></span>
- <span data-ttu-id="49062-124">SEO Anahtar sözcükler</span><span class="sxs-lookup"><span data-stu-id="49062-124">SEO keywords</span></span>
- <span data-ttu-id="49062-125">Aria etiketleri</span><span class="sxs-lookup"><span data-stu-id="49062-125">Aria labels</span></span>
- <span data-ttu-id="49062-126">noindex</span><span class="sxs-lookup"><span data-stu-id="49062-126">noindex</span></span>
- <span data-ttu-id="49062-127">nofollow</span><span class="sxs-lookup"><span data-stu-id="49062-127">nofollow</span></span>
- <span data-ttu-id="49062-128">noarchive</span><span class="sxs-lookup"><span data-stu-id="49062-128">noarchive</span></span>
- <span data-ttu-id="49062-129">nocache</span><span class="sxs-lookup"><span data-stu-id="49062-129">nocache</span></span>
- <span data-ttu-id="49062-130">noOpenDirectoryProject</span><span class="sxs-lookup"><span data-stu-id="49062-130">noOpenDirectoryProject</span></span>
- <span data-ttu-id="49062-131">nosnippet</span><span class="sxs-lookup"><span data-stu-id="49062-131">nosnippet</span></span>
- <span data-ttu-id="49062-132">noImageIndex</span><span class="sxs-lookup"><span data-stu-id="49062-132">noImageIndex</span></span>
- <span data-ttu-id="49062-133">unavailableAfter</span><span class="sxs-lookup"><span data-stu-id="49062-133">unavailableAfter</span></span>

### <a name="modify-page-metadata"></a><span data-ttu-id="49062-134">Sayfa meta verilerini Değiştir</span><span class="sxs-lookup"><span data-stu-id="49062-134">Modify page metadata</span></span>

<span data-ttu-id="49062-135">Sayfa meta verilerini değiştirmek için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="49062-135">To modify page metadata, follow these steps.</span></span>

1. <span data-ttu-id="49062-136">**Siteler** altında, **Fabrikam**'ı seçin (veya sitenizin adını).</span><span class="sxs-lookup"><span data-stu-id="49062-136">Under **Sites**, select the **Fabrikam** (or the name of your site).</span></span>
1. <span data-ttu-id="49062-137">Soldaki gezinti bölmesinde **Sayfalar** seçin.</span><span class="sxs-lookup"><span data-stu-id="49062-137">In the navigation pane on the left, select **Pages**.</span></span>
1. <span data-ttu-id="49062-138">Sayfa düzenleyicisinde açmak için giriş sayfasını seçin.</span><span class="sxs-lookup"><span data-stu-id="49062-138">Select the home page to open it in the page editor.</span></span>
1. <span data-ttu-id="49062-139">Komut çubuğunda, **Düzenle** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="49062-139">On the command bar, select **Edit**.</span></span>
1. <span data-ttu-id="49062-140">Sağdaki özellikler bölmesinde, **Varsayılan meta verileri** genişletin.</span><span class="sxs-lookup"><span data-stu-id="49062-140">In the properties pane on the right, expand **Default metatags**.</span></span>
1. <span data-ttu-id="49062-141">Yeni bir metaetiketi eklemek için, **Ekle**'yi seçin ve alana etiketi girin.</span><span class="sxs-lookup"><span data-stu-id="49062-141">To add a new metatag, select **Add**, and then enter the tag in the field.</span></span> <span data-ttu-id="49062-142">Varolan bir meta etiketi kaldırmak için, sağ tarafta bulunan çöp tenekesi sembolünü seçin.</span><span class="sxs-lookup"><span data-stu-id="49062-142">To remove an existing metatag, select the trash can symbol to the right of it.</span></span>
1. <span data-ttu-id="49062-143">**Kaydet**i seçin ve sonra **Düzenlemeyi bitir**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="49062-143">Select **Save**, and then select **Finish editing**.</span></span>
1. <span data-ttu-id="49062-144">**Yorumlar** alanında **Güncellenen meta etiketler** seçeneğini girin ve **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="49062-144">In the **Comments** field, enter **Updated metatags**, and then select **OK**.</span></span>
1. <span data-ttu-id="49062-145">Sayfanızın önizlemesini görüntülemek için **Önizleme**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="49062-145">Select **Preview** to preview your page.</span></span> <span data-ttu-id="49062-146">Bitirdiğinizde, geliştirme aracına dönmek için Önizleme sekmesini kapatın.</span><span class="sxs-lookup"><span data-stu-id="49062-146">When you've finished, close the preview tab to return to the authoring tool.</span></span>
1. <span data-ttu-id="49062-147">**Yayımla**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="49062-147">Select **Publish**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="49062-148">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="49062-148">Additional resources</span></span>

[<span data-ttu-id="49062-149">Var olan site sayfasını değiştirme</span><span class="sxs-lookup"><span data-stu-id="49062-149">Modify an existing site page</span></span>](modify-existing-page.md)

[<span data-ttu-id="49062-150">Yeni site sayfası ekleme</span><span class="sxs-lookup"><span data-stu-id="49062-150">Add a new site page</span></span>](add-new-page.md)

[<span data-ttu-id="49062-151">Sayfa düzeni seçme</span><span class="sxs-lookup"><span data-stu-id="49062-151">Select page layouts</span></span>](select-page-layouts.md)

[<span data-ttu-id="49062-152">Sayfa kaydetme, önizleme ve yayımlama</span><span class="sxs-lookup"><span data-stu-id="49062-152">Save, preview, and publish a page</span></span>](save-preview-publish-page.md)

[<span data-ttu-id="49062-153">Ürün sayfasını zenginleştirme</span><span class="sxs-lookup"><span data-stu-id="49062-153">Enrich a product page</span></span>](enrich-product-page.md)

[<span data-ttu-id="49062-154">Kategori açılış sayfasını zenginleştirme</span><span class="sxs-lookup"><span data-stu-id="49062-154">Enrich a category landing page</span></span>](enrich-category-page.md)

[<span data-ttu-id="49062-155">Sayfa içeriği erişilebilirliğini doğrula</span><span class="sxs-lookup"><span data-stu-id="49062-155">Verify page content accessibility</span></span>](verify-accessibility.md)
