---
title: SEO meta verilerini yönetme
description: Bu konuda, Microsoft Dynamics 365 Commerce'ta arama motoru optimizasyonu (SEO) meta verilerinin nasıl yönetileceği açıklanmaktadır.
author: psimolin
manager: annbe
ms.date: 10/01/2019
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
ms.openlocfilehash: 1e7da7bf5c473746413e92babfa943f546b7724d
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/01/2020
ms.locfileid: "3003476"
---
# <a name="manage-seo-metadata"></a><span data-ttu-id="f0d41-103">SEO meta verilerini yönetme</span><span class="sxs-lookup"><span data-stu-id="f0d41-103">Manage SEO metadata</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="f0d41-104">Bu konuda, Microsoft Dynamics 365 Commerce'ta arama motoru optimizasyonu (SEO) meta verilerinin nasıl yönetileceği açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="f0d41-104">This topic describes how to manage search engine optimization (SEO) metadata in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="f0d41-105">Genel Bakış</span><span class="sxs-lookup"><span data-stu-id="f0d41-105">Overview</span></span>

<span data-ttu-id="f0d41-106">Bir sitenin SEO meta verileri, site haritaları ve sayfa meta verileri kullanılarak yönetilebilir.</span><span class="sxs-lookup"><span data-stu-id="f0d41-106">SEO metadata for a site can be managed by using site maps and page metadata.</span></span>
    
## <a name="site-maps"></a><span data-ttu-id="f0d41-107">Site haritaları</span><span class="sxs-lookup"><span data-stu-id="f0d41-107">Site maps</span></span>

<span data-ttu-id="f0d41-108">Site haritası, Web sitenizdeki sayfaların, XML biçimindeki, makine tarafından okunabilen bir listesidir.</span><span class="sxs-lookup"><span data-stu-id="f0d41-108">A site map is a machine-readable list, in XML format, of the pages on your website.</span></span> <span data-ttu-id="f0d41-109">Arama motorları tarafından, sitenizde daha iyi arama sonuçları sağlayabilmeleri için tüketilmesi amaçlanmıştır.</span><span class="sxs-lookup"><span data-stu-id="f0d41-109">It's intended to be consumed by search engines, so that they can provide better search results from your site.</span></span> <span data-ttu-id="f0d41-110">Site eşlemeleri arama motorları tarafından el ile gerçekleştirilebilir veya robots. txt dosyasında yayımlanabilir.</span><span class="sxs-lookup"><span data-stu-id="f0d41-110">Site maps can be manually ingested by search engines or published in a robots.txt file.</span></span>

<span data-ttu-id="f0d41-111">Dynamics 365 Commerce Site eşlemelerinin otomatik olarak oluşturulmasını destekler.</span><span class="sxs-lookup"><span data-stu-id="f0d41-111">Dynamics 365 Commerce supports automatic generation of site maps.</span></span> <span data-ttu-id="f0d41-112">Sayfalar yayımlanana ve yayımdan kaldırılmış olduğunda, site eşleştirmeleri otomatik olarak güncelleştirilir.</span><span class="sxs-lookup"><span data-stu-id="f0d41-112">Site maps are automatically updated when pages are published and unpublished.</span></span>

### <a name="turn-on-site-map-generation"></a><span data-ttu-id="f0d41-113">Site Haritası oluşturmayı aç</span><span class="sxs-lookup"><span data-stu-id="f0d41-113">Turn on site map generation</span></span>

1. <span data-ttu-id="f0d41-114">Geliştirme aracında oturum açın.</span><span class="sxs-lookup"><span data-stu-id="f0d41-114">Sign in to the authoring tool.</span></span>
1. <span data-ttu-id="f0d41-115">**Siteler** altında, **Fabrikam**'ı seçin (veya sitenizin adını).</span><span class="sxs-lookup"><span data-stu-id="f0d41-115">Under **Sites**, select **Fabrikam** (or the name of your site).</span></span>
1. <span data-ttu-id="f0d41-116">Soldaki gezinti bölmesinde **Site Yönetimi** seçin.</span><span class="sxs-lookup"><span data-stu-id="f0d41-116">In the navigation pane on the left, select **Site Management**.</span></span>
1. <span data-ttu-id="f0d41-117">**Site haritaları etkin** seçeneğinin açık olduğundan emin olun.</span><span class="sxs-lookup"><span data-stu-id="f0d41-117">Make sure that the **Site maps enabled** option is turned on.</span></span>

## <a name="page-metadata"></a><span data-ttu-id="f0d41-118">Sayfa meta verileri</span><span class="sxs-lookup"><span data-stu-id="f0d41-118">Page metadata</span></span>

<span data-ttu-id="f0d41-119">Dynamics 365 Commerce Her bir sayfa için SEO meta verilerini yönetmenizi sağlar.</span><span class="sxs-lookup"><span data-stu-id="f0d41-119">Dynamics 365 Commerce lets you manage SEO metadata for individual pages.</span></span> <span data-ttu-id="f0d41-120">Bu bilgileri bir sayfa kapsayıcısının **SEO Özellikler** bölümünde görüntüleyebilir ve değiştirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="f0d41-120">You can view and modify this information in the **SEO Properties** section of a page container.</span></span> <span data-ttu-id="f0d41-121">Şu anda aşağıdaki SEO meta veri özellikleri desteklenmektedir:</span><span class="sxs-lookup"><span data-stu-id="f0d41-121">The following SEO metadata properties are supported:</span></span>

- <span data-ttu-id="f0d41-122">Ünvan</span><span class="sxs-lookup"><span data-stu-id="f0d41-122">Title</span></span>
- <span data-ttu-id="f0d41-123">Tanım</span><span class="sxs-lookup"><span data-stu-id="f0d41-123">Description</span></span>
- <span data-ttu-id="f0d41-124">SEO Anahtar sözcükler</span><span class="sxs-lookup"><span data-stu-id="f0d41-124">SEO keywords</span></span>
- <span data-ttu-id="f0d41-125">Aria etiketleri</span><span class="sxs-lookup"><span data-stu-id="f0d41-125">Aria labels</span></span>
- <span data-ttu-id="f0d41-126">noindex</span><span class="sxs-lookup"><span data-stu-id="f0d41-126">noindex</span></span>
- <span data-ttu-id="f0d41-127">nofollow</span><span class="sxs-lookup"><span data-stu-id="f0d41-127">nofollow</span></span>
- <span data-ttu-id="f0d41-128">noarchive</span><span class="sxs-lookup"><span data-stu-id="f0d41-128">noarchive</span></span>
- <span data-ttu-id="f0d41-129">nocache</span><span class="sxs-lookup"><span data-stu-id="f0d41-129">nocache</span></span>
- <span data-ttu-id="f0d41-130">noOpenDirectoryProject</span><span class="sxs-lookup"><span data-stu-id="f0d41-130">noOpenDirectoryProject</span></span>
- <span data-ttu-id="f0d41-131">nosnippet</span><span class="sxs-lookup"><span data-stu-id="f0d41-131">nosnippet</span></span>
- <span data-ttu-id="f0d41-132">noImageIndex</span><span class="sxs-lookup"><span data-stu-id="f0d41-132">noImageIndex</span></span>
- <span data-ttu-id="f0d41-133">unavailableAfter</span><span class="sxs-lookup"><span data-stu-id="f0d41-133">unavailableAfter</span></span>

### <a name="modify-page-metadata"></a><span data-ttu-id="f0d41-134">Sayfa meta verilerini Değiştir</span><span class="sxs-lookup"><span data-stu-id="f0d41-134">Modify page metadata</span></span>

<span data-ttu-id="f0d41-135">Sayfa meta verilerini değiştirmek için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="f0d41-135">To modify page metadata, follow these steps.</span></span>

1. <span data-ttu-id="f0d41-136">**Siteler** altında, **Fabrikam**'ı seçin (veya sitenizin adını).</span><span class="sxs-lookup"><span data-stu-id="f0d41-136">Under **Sites**, select the **Fabrikam** (or the name of your site).</span></span>
1. <span data-ttu-id="f0d41-137">Soldaki gezinti bölmesinde **Sayfalar** seçin.</span><span class="sxs-lookup"><span data-stu-id="f0d41-137">In the navigation pane on the left, select **Pages**.</span></span>
1. <span data-ttu-id="f0d41-138">Sayfa düzenleyicisinde açmak için giriş sayfasını seçin.</span><span class="sxs-lookup"><span data-stu-id="f0d41-138">Select the home page to open it in the page editor.</span></span>
1. <span data-ttu-id="f0d41-139">Eylem Bölmesinde, **Çıkış yap** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="f0d41-139">On the Action Pane, select **Check Out**.</span></span>
1. <span data-ttu-id="f0d41-140">Sağdaki özellikler bölmesinde, **Varsayılan meta verileri** genişletin.</span><span class="sxs-lookup"><span data-stu-id="f0d41-140">In the properties pane on the right, expand **Default metatags**.</span></span>
1. <span data-ttu-id="f0d41-141">Yeni bir metaetiketi eklemek için, **Ekle**'yi seçin ve alana etiketi girin.</span><span class="sxs-lookup"><span data-stu-id="f0d41-141">To add a new metatag, select **Add**, and then enter the tag in the field.</span></span>

    <span data-ttu-id="f0d41-142">Varolan bir meta etiketi kaldırmak için, sağ tarafta bulunan çöp tenekesi sembolünü seçin.</span><span class="sxs-lookup"><span data-stu-id="f0d41-142">To remove an existing metatag, select the trash can symbol to the right of it.</span></span>

1. <span data-ttu-id="f0d41-143">**Kaydet**i seçin ve sonra **Giriş**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="f0d41-143">Select **Save**, and then select **Check In**.</span></span>
1. <span data-ttu-id="f0d41-144">**Yorumlar** alanında **Güncellenen meta etiketler** seçeneğini girin ve **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="f0d41-144">In the **Comments** field, enter **Updated metatags**, and then select **OK**.</span></span>
1. <span data-ttu-id="f0d41-145">Sayfanızın önizlemesini görüntülemek için **Önizleme**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="f0d41-145">Select **Preview** to preview your page.</span></span> <span data-ttu-id="f0d41-146">Bitirdiğinizde, geliştirme aracına dönmek için Önizleme sekmesini kapatın.</span><span class="sxs-lookup"><span data-stu-id="f0d41-146">When you've finished, close the preview tab to return to the authoring tool.</span></span>
1. <span data-ttu-id="f0d41-147">**Yayımla**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="f0d41-147">Select **Publish**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="f0d41-148">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="f0d41-148">Additional resources</span></span>

[<span data-ttu-id="f0d41-149">Var olan site sayfasını değiştirme</span><span class="sxs-lookup"><span data-stu-id="f0d41-149">Modify an existing site page</span></span>](modify-existing-page.md)

[<span data-ttu-id="f0d41-150">Yeni site sayfası ekleme</span><span class="sxs-lookup"><span data-stu-id="f0d41-150">Add a new site page</span></span>](add-new-page.md)

[<span data-ttu-id="f0d41-151">Sayfa düzeni seçme</span><span class="sxs-lookup"><span data-stu-id="f0d41-151">Select page layouts</span></span>](select-page-layouts.md)

[<span data-ttu-id="f0d41-152">Sayfa kaydetme, önizleme ve yayımlama</span><span class="sxs-lookup"><span data-stu-id="f0d41-152">Save, preview, and publish a page</span></span>](save-preview-publish-page.md)

[<span data-ttu-id="f0d41-153">Ürün sayfasını zenginleştirme</span><span class="sxs-lookup"><span data-stu-id="f0d41-153">Enrich a product page</span></span>](enrich-product-page.md)

[<span data-ttu-id="f0d41-154">Kategori açılış sayfasını zenginleştirme</span><span class="sxs-lookup"><span data-stu-id="f0d41-154">Enrich a category landing page</span></span>](enrich-category-page.md)

[<span data-ttu-id="f0d41-155">Sayfa içeriği erişilebilirliğini doğrula</span><span class="sxs-lookup"><span data-stu-id="f0d41-155">Verify page content accessibility</span></span>](verify-accessibility.md)
