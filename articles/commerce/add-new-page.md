---
title: Yeni site sayfası ekleme
description: Bu konuda, Microsoft Dynamics 365 Commerce'e yeni bir site sayfası ekleme yöntemi açıklanmıştır .
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
ms.openlocfilehash: d5ab90343220e427a80cc4dde17c628ba64ac69e
ms.sourcegitcommit: 295d940a345879b3dfc5991e387b91c7257019ea
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/01/2019
ms.locfileid: "2696750"
---
# <a name="add-a-new-site-page"></a><span data-ttu-id="7dc72-103">Yeni site sayfası ekleme</span><span class="sxs-lookup"><span data-stu-id="7dc72-103">Add a new site page</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="7dc72-104">Bu konuda, Microsoft Dynamics 365 Commerce'e yeni bir site sayfası ekleme yöntemi açıklanmıştır .</span><span class="sxs-lookup"><span data-stu-id="7dc72-104">This topic describes how to add a new site page in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="7dc72-105">Genel Bakış</span><span class="sxs-lookup"><span data-stu-id="7dc72-105">Overview</span></span>

<span data-ttu-id="7dc72-106">Siteniz için şablonlar ve parçalar oluşturduktan sonraki adım bunları kullanan sayfalar oluşturmaya başlamak içindir.</span><span class="sxs-lookup"><span data-stu-id="7dc72-106">After you've created templates and fragments for your site, the next step is to start to create pages that use them.</span></span> <span data-ttu-id="7dc72-107">Başlamak için, bir şablon veya düzen, bir sayfa adı ve bir sayfa URL'si seçmelisiniz.</span><span class="sxs-lookup"><span data-stu-id="7dc72-107">To get started, you must select a template or layout, a page name, and a page URL.</span></span>

## <a name="template-or-layout"></a><span data-ttu-id="7dc72-108">Şablon veya düzen</span><span class="sxs-lookup"><span data-stu-id="7dc72-108">Template or layout</span></span>

<span data-ttu-id="7dc72-109">Yeni sayfanız için bir şablon ya da Düzen kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="7dc72-109">You can use either a template or a layout for your new page.</span></span> <span data-ttu-id="7dc72-110">Daha fazla bilgi için bkz. [Şablonlar ve düzenlere genel bakış](templates-layouts-overview.md).</span><span class="sxs-lookup"><span data-stu-id="7dc72-110">For more information, see [Templates and layouts overview](templates-layouts-overview.md).</span></span>

## <a name="page-name"></a><span data-ttu-id="7dc72-111">Sayfa adı</span><span class="sxs-lookup"><span data-stu-id="7dc72-111">Page name</span></span>

<span data-ttu-id="7dc72-112">Sayfa adı sayfanız için benzersiz olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="7dc72-112">The page name must be unique to your page.</span></span> <span data-ttu-id="7dc72-113">Açıklayıcı olmalıdır, böylece kolayca bulabilmeniz için ve sayfanın ne için amaçlandığı hakkında diğer kişileri de bulabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="7dc72-113">It should be descriptive, so that you can easily find it and other people know what the page is intended for.</span></span> <span data-ttu-id="7dc72-114">Sayfa adını daha sonra değiştirilemediğinden, dikkatlice seçin.</span><span class="sxs-lookup"><span data-stu-id="7dc72-114">Choose the page name carefully, because it can't be changed later.</span></span>

## <a name="page-url"></a><span data-ttu-id="7dc72-115">Sayfa URL'si</span><span class="sxs-lookup"><span data-stu-id="7dc72-115">Page URL</span></span>

<span data-ttu-id="7dc72-116">Yeni sayfanız için bir URL girme seçeneğiniz olabilir.</span><span class="sxs-lookup"><span data-stu-id="7dc72-116">You can have the option to enter a URL for your new page.</span></span> <span data-ttu-id="7dc72-117">Sayfa oluşturduğunuzda, tam bir URL oluşturmak için kullanılacak bir dize girebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="7dc72-117">When you create a page, you can enter a string that will be used to form a complete URL.</span></span> <span data-ttu-id="7dc72-118">Bu dize göreli bir URL veya URL bilgi olarak bilinir.</span><span class="sxs-lookup"><span data-stu-id="7dc72-118">This string is known as a relative URL or a URL slug.</span></span> <span data-ttu-id="7dc72-119">URL bilgisinin temel alınarak tam bir URL oluşturulur ve yeni sayfa buna atanır.</span><span class="sxs-lookup"><span data-stu-id="7dc72-119">A complete URL is then generated based on the URL slug, and the new page is assigned to it.</span></span> <span data-ttu-id="7dc72-120">Sayfayı yayımlamadan önce URL başlık bilgisinin değiştirilmesini sağlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="7dc72-120">You can change the URL slug later, before you publish the page.</span></span> <span data-ttu-id="7dc72-121">Daha fazla bilgi için bkz. [Sayfa URL'si oluşturma](create-page-URL.md).</span><span class="sxs-lookup"><span data-stu-id="7dc72-121">For more information, see [Create a page URL](create-page-URL.md).</span></span>

> [!NOTE]
> <span data-ttu-id="7dc72-122">Dynamics 365 Commerce URL'leri ve içeriği ayrıştırır.</span><span class="sxs-lookup"><span data-stu-id="7dc72-122">Dynamics 365 Commerce decouples URLs and content.</span></span> <span data-ttu-id="7dc72-123">Başka bir deyişle, bir URL ile ilişkili olmayan bir sayfa oluşturulabilir ve bir sayfayla ilişkili olmayan bir URL oluşturulabilir.</span><span class="sxs-lookup"><span data-stu-id="7dc72-123">In other words, a page can be created that isn't associated with an URL, and a URL can be created that isn't associated with a page.</span></span> <span data-ttu-id="7dc72-124">Bu nedenle, bir URL için içerik takası yapılabilir; kesinti süresi gerekmez ve yeniden yönlendirmeler daha kolay yönetilebilir.</span><span class="sxs-lookup"><span data-stu-id="7dc72-124">Therefore, content swapping can be done for a URL and doesn't require downtime, and redirects are easier to manage.</span></span>

## <a name="add-a-new-page"></a><span data-ttu-id="7dc72-125">Yeni sayfa ekleme</span><span class="sxs-lookup"><span data-stu-id="7dc72-125">Add a new page</span></span>

<span data-ttu-id="7dc72-126">Sitenize yeni site sayfası eklemek için şu adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="7dc72-126">To add a new site page to your site, follow these steps.</span></span>

1. <span data-ttu-id="7dc72-127">**Siteler** altında, **Fabrikam**'ı seçin (veya sitenizin adını).</span><span class="sxs-lookup"><span data-stu-id="7dc72-127">Under **Sites**, select **Fabrikam** (or the name of your site).</span></span>
1. <span data-ttu-id="7dc72-128">**Yeni Sayfa**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="7dc72-128">Select **New Page**.</span></span>
1. <span data-ttu-id="7dc72-129">**Yeni Sayfa** iletişim kutusunda , bir şablon ürün reçetesi seçin ve **Tamam**'ı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="7dc72-129">In the **New Page** dialog box, select a template, and then select **OK**.</span></span>
1. <span data-ttu-id="7dc72-130">**Sayfa Adı** alanına bir sayfa adı girin (örneğin, **Yeni Sayfam**).</span><span class="sxs-lookup"><span data-stu-id="7dc72-130">In the **Page Name** field, enter a page name (for example, **My New Page**).</span></span>
1. <span data-ttu-id="7dc72-131">**URL** alanına URL'yi tamamlamak için bir dize (URL bilgi) girin (örneğin, **mynewpage**).</span><span class="sxs-lookup"><span data-stu-id="7dc72-131">In the **URL** field, enter a string (URL slug) to complete the URL (for example, **mynewpage**).</span></span>
1. <span data-ttu-id="7dc72-132">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="7dc72-132">Select **OK**.</span></span> <span data-ttu-id="7dc72-133">Sayfa düzenleyici görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="7dc72-133">The page editor appears.</span></span> <span data-ttu-id="7dc72-134">Seçtiğiniz şablona göre bir üstbilgi ve altbilgi sayfaya otomatik olarak eklendiğine dikkat edin.</span><span class="sxs-lookup"><span data-stu-id="7dc72-134">Notice that a header and a footer are automatically added to the page, based on the template that you selected.</span></span>
1. <span data-ttu-id="7dc72-135">Sayfa anahattında **ana** yuvayı seçin, üç nokta düğmesini (**...**) ve sonra **Modül ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="7dc72-135">In the page outline, select the **Main** slot, select the ellipsis button (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="7dc72-136">**Konteyner**'i seçin ve sonra **Tamam**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="7dc72-136">Select **Container**, and then select **OK**</span></span>
1. <span data-ttu-id="7dc72-137">**Sıvı kabı**seçin, üç nokta düğmesini seçin ve sonra **Modül ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="7dc72-137">Select **Fluid Container**, select the ellipsis button, and then select **Add Module**.</span></span>
1. <span data-ttu-id="7dc72-138">**İçerik zengin bloğu**seçeneğini belirleyin ve **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="7dc72-138">Select **Content Rich block**, and then select **OK**.</span></span>
1. <span data-ttu-id="7dc72-139">**İçerik Zengin Blok** seçin, üç nokta düğmesini seçin ve sonra **Modül ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="7dc72-139">Select **Content Rich Block**, select the ellipsis button, and then select **Add Module**.</span></span>
1. <span data-ttu-id="7dc72-140">**İçerik zengin bloğu öğesi**seçeneğini belirleyin ve **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="7dc72-140">Select **Content rich block item**, and then select **OK**.</span></span>
1. <span data-ttu-id="7dc72-141">Sağdaki Özellikler bölmesinde, **paragraf**'ı seçin ve sonra alanına **test metnimi** girin.</span><span class="sxs-lookup"><span data-stu-id="7dc72-141">In the properties pane on the right, select **Paragraph**, and then, in the field, enter **My test text**.</span></span>
1. <span data-ttu-id="7dc72-142">**Kaydet**i seçin ve sonra **Giriş**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="7dc72-142">Select **Save**, and then select **Check In**.</span></span>
1. <span data-ttu-id="7dc72-143">**Yorumlar** alanında **yeni sayfa eklendi** seçeneğini girin ve **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="7dc72-143">In the **Comments** field, enter **Added new page**, and then select **OK**.</span></span>
1. <span data-ttu-id="7dc72-144">Sayfanızın önizlemesini görüntülemek için **Önizleme**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="7dc72-144">Select **Preview** to preview your page.</span></span> <span data-ttu-id="7dc72-145">Bitirdiğinizde, geliştirme aracına dönmek için Önizleme sekmesini kapatın.</span><span class="sxs-lookup"><span data-stu-id="7dc72-145">When you've finished, close the preview tab to return to the authoring tool.</span></span>
1. <span data-ttu-id="7dc72-146">**Yayımla**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="7dc72-146">Select **Publish**.</span></span>
1. <span data-ttu-id="7dc72-147">Gezinti yolunda (Breadcrumbs), **Fabrikam**'ı (veya sitenizin adını) seçin.</span><span class="sxs-lookup"><span data-stu-id="7dc72-147">In the navigation path (breadcrumbs), select **Fabrikam** (or the name of your site).</span></span>
1. <span data-ttu-id="7dc72-148">Soldaki gezinti bölmesinde **URL'leri** seçin.</span><span class="sxs-lookup"><span data-stu-id="7dc72-148">In the navigation pane on the left, select **URLs**.</span></span>
1. <span data-ttu-id="7dc72-149">Listede (**mynewpage**) öğesini bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="7dc72-149">Find and select your URL (**mynewpage**) in the list.</span></span>
1. <span data-ttu-id="7dc72-150">**Yayımla**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="7dc72-150">Select **Publish**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="7dc72-151">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="7dc72-151">Additional resources</span></span>

[<span data-ttu-id="7dc72-152">Var olan site sayfasını değiştirme</span><span class="sxs-lookup"><span data-stu-id="7dc72-152">Modify an existing site page</span></span>](modify-existing-page.md)

[<span data-ttu-id="7dc72-153">Sayfa düzeni seçme</span><span class="sxs-lookup"><span data-stu-id="7dc72-153">Select page layouts</span></span>](select-page-layouts.md)

[<span data-ttu-id="7dc72-154">SEO meta verilerini yönetme</span><span class="sxs-lookup"><span data-stu-id="7dc72-154">Manage SEO metadata</span></span>](manage-seo-metadata.md)

[<span data-ttu-id="7dc72-155">Sayfa kaydetme, önizleme ve yayımlama</span><span class="sxs-lookup"><span data-stu-id="7dc72-155">Save, preview, and publish a page</span></span>](save-preview-publish-page.md)

[<span data-ttu-id="7dc72-156">Ürün sayfasını zenginleştirme</span><span class="sxs-lookup"><span data-stu-id="7dc72-156">Enrich a product page</span></span>](enrich-product-page.md)

[<span data-ttu-id="7dc72-157">Kategori açılış sayfasını zenginleştirme</span><span class="sxs-lookup"><span data-stu-id="7dc72-157">Enrich a category landing page</span></span>](enrich-category-page.md)

