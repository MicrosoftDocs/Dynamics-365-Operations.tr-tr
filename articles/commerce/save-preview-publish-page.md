---
title: Sayfa kaydetme, önizleme ve yayımlama
description: Bu konuda, Microsoft Dynamics 365 Commerce'te sayfa kaydetme, önizleme ve yayınlama yöntemi açıklanmıştır.
author: psimolin
manager: annbe
ms.date: 04/14/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 5eccf5409c41710585e3d69c7270faa4621f7715
ms.sourcegitcommit: 872600103d2a444d78963867e5e0cdc62e68c3ec
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/01/2021
ms.locfileid: "5097215"
---
# <a name="save-preview-and-publish-a-page"></a><span data-ttu-id="2c349-103">Sayfa kaydetme, önizleme ve yayımlama</span><span class="sxs-lookup"><span data-stu-id="2c349-103">Save, preview, and publish a page</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="2c349-104">Bu konuda, Microsoft Dynamics 365 Commerce'te sayfa kaydetme, önizleme ve yayınlama yöntemi açıklanmıştır.</span><span class="sxs-lookup"><span data-stu-id="2c349-104">This topic describes how to save, preview, and publish a page in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="save-a-page"></a><span data-ttu-id="2c349-105">Sayfa kaydetme</span><span class="sxs-lookup"><span data-stu-id="2c349-105">Save a page</span></span>

<span data-ttu-id="2c349-106">Sayfayı kaydetmek için, belgenizi kullanıma almış ve sayfa düzenleyicisinde açmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="2c349-106">To save a page, you must have it checked out to yourself and open in the page editor.</span></span> <span data-ttu-id="2c349-107">Bir sayfayı kullanıma almak için komut çubuğunda **Düzenle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="2c349-107">To check out a page, select **Edit** on the command bar.</span></span> <span data-ttu-id="2c349-108">Bir sayfayı düzenlemeyi bitirdikten sonra, değişikliklerinizin saklanmasını sağlamak sayfayı hemen kaydetmelisiniz.</span><span class="sxs-lookup"><span data-stu-id="2c349-108">After you've finished editing a page, you should immediately save it to ensure that your changes are stored.</span></span>

<span data-ttu-id="2c349-109">Bir sayfayı kaydettiğinizde, değişiklikler yalnızca size görünebilir.</span><span class="sxs-lookup"><span data-stu-id="2c349-109">When you save a page, the changes are visible only to you.</span></span> <span data-ttu-id="2c349-110">Kaydetme işlemi öncelikle, sayfa henüz iade edilmeye hazır olmadığı sürece değişiklikleri depolamaya yöneliktir.</span><span class="sxs-lookup"><span data-stu-id="2c349-110">The save operation is intended primarily to store changes while the page isn't yet ready to be checked in.</span></span> <span data-ttu-id="2c349-111">Sayfayı değiştirmeyi bitirdiğinizde, gözden geçirin ve böylece değişiklikler başkaları tarafından görülebilir hale gelir.</span><span class="sxs-lookup"><span data-stu-id="2c349-111">When you've finished modifying the page, we recommend that you check it in, so that the changes become visible to others.</span></span> <span data-ttu-id="2c349-112">Bu noktada, sayfa değiştirilmesi gereken diğer kullanıcılar tarafından da kullanıma açılabilir.</span><span class="sxs-lookup"><span data-stu-id="2c349-112">At that point, the page can also be checked out by other users who must modify it.</span></span>

## <a name="preview-a-page"></a><span data-ttu-id="2c349-113">Sayfayı önizleme</span><span class="sxs-lookup"><span data-stu-id="2c349-113">Preview a page</span></span>

<span data-ttu-id="2c349-114">Geliştirme aracı, iki tür önizleme özelliği sunar: Sayfa düzenleyicisinde "gördüğünüz şey aldığınız şeydir" (WYSIWYG) Önizleme bölmesi olan görsel sayfa oluşturucu ve ayrı bir önizleme penceresi.</span><span class="sxs-lookup"><span data-stu-id="2c349-114">The authoring tool offers two kinds of preview features: visual page builder, which is a "what you see is what you get" (WYSIWYG) preview pane in the page editor, and a separate preview window.</span></span>

<span data-ttu-id="2c349-115">Sayfa düzenleyicisini kullanırken, Orta bölmede "aldığınız şey görüntülenir" (WYSIWYG) önizlemesi görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="2c349-115">While you're using the page editor, a "what you see is what you get" (WYSIWYG) preview appears in the center pane.</span></span> <span data-ttu-id="2c349-116">Bu önizleme, sayfayı her kaydedişinizde otomatik olarak güncelleştirilir.</span><span class="sxs-lookup"><span data-stu-id="2c349-116">This preview is automatically updated whenever you save the page.</span></span> <span data-ttu-id="2c349-117">Bunu, komut çubuğunda **Yenile** seçerek el ile de güncelleştirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="2c349-117">You can also manually update it by selecting **Refresh** on the command bar.</span></span> <span data-ttu-id="2c349-118">Önizleme, sayfayı sitenin kullanıcıları göreceği gibi işler, ancak yazma yardımcıları bunun üzerinde işlenir.</span><span class="sxs-lookup"><span data-stu-id="2c349-118">The preview renders the page just as the site's users will see it, but authoring helpers are rendered on top of it.</span></span>

<span data-ttu-id="2c349-119">Sayfayı değiştirmeyi bitirdiğinizde, hangi müşterilerin görebileceğini görmek için önizlemek isteyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="2c349-119">When you've finished modifying the page, you might want to preview it to see what customers will see.</span></span> <span data-ttu-id="2c349-120">Bir sayfayı önizlemek için, komut çubuğunda **önizleme**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="2c349-120">To preview a page, select **Preview** on the command bar.</span></span> <span data-ttu-id="2c349-121">Önizleme, ayrı bir tarayıcı penceresinde görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="2c349-121">The preview will appear in a separate browser window.</span></span> <span data-ttu-id="2c349-122">Önizleme penceresindeki sayfa, sitenin kullanıcısı tarafından göreceğiniz şekilde oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="2c349-122">The page in the preview window is rendered just as the site's user will see it.</span></span> <span data-ttu-id="2c349-123">Yanıt veren modüllerin tüm görünüm bağlantı noktalarında doğru şekilde işlendiğine emin olmak için pencereyi yeniden boyutlandırabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="2c349-123">You can resize the window to make sure that responsive modules are correctly rendered in all view ports.</span></span>

> [!NOTE]
> <span data-ttu-id="2c349-124">Yayımlanmamış içeriğin önizlemesi için kimlik doğrulama ve doğru izinler gereklidir.</span><span class="sxs-lookup"><span data-stu-id="2c349-124">Authentication and correct permissions are required to preview unpublished content.</span></span> <span data-ttu-id="2c349-125">Bu nedenle, önizlemenin URL'sini başka biriyle paylaşıyorsanız bu kişinin içeriğe erişmek için doğru izinlere sahip olması gerekir.</span><span class="sxs-lookup"><span data-stu-id="2c349-125">Therefore, if you share the URL of the preview with someone, that person must have the correct permissions to access the content.</span></span>

## <a name="publish-a-page"></a><span data-ttu-id="2c349-126">Sayfayı yayımla</span><span class="sxs-lookup"><span data-stu-id="2c349-126">Publish a page</span></span>

<span data-ttu-id="2c349-127">Sayfanız hazır olduğunda, bir sonraki adım bunu yayınlamaktır, böylece harici kullanıcılar içeriği görüntüleyebilir.</span><span class="sxs-lookup"><span data-stu-id="2c349-127">When your page is ready, the next step is to publish it, so that external users can view the content.</span></span> <span data-ttu-id="2c349-128">Bir sayfayı yayımlayabilmeniz için, komut çubuğunda **Düzenlemeyi bitir**'i seçerek sayfayı iade etmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="2c349-128">Before you can publish a page, you must check it in by selecting **Finish editing** on the command bar.</span></span>

<span data-ttu-id="2c349-129">Sayfaları sayfa denetçisinde veya sayfa düzenleyicisinden yayımlayabilir veya yayımdan kaldırabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="2c349-129">You can publish and unpublish pages from either the page inspector or the page editor.</span></span> <span data-ttu-id="2c349-130">Sayfa denetçisi, sayfaların listesini gösterir ve toplu işlemlere izin verir.</span><span class="sxs-lookup"><span data-stu-id="2c349-130">The page inspector shows a list of pages and allows for bulk operations.</span></span> <span data-ttu-id="2c349-131">Sayfa düzenleyicisi, yalnızca içinde açık olan tek bir sayfayı yayınlamak veya yayımdan kaldırmak için kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="2c349-131">The page editor can be used to publish or unpublish only the single page that is open in it.</span></span>

<span data-ttu-id="2c349-132">Sayfa denetçisinde bir veya daha fazla sayfa yayınlamak için sayfaları seçin, bunların iade edilmiş olduklarından emin olun ve sonra komut çubuğunda **Yayınla**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="2c349-132">To publish one or more pages from the page inspector, select the pages, make sure that they are checked in, and then select **Publish** on the command bar.</span></span> <span data-ttu-id="2c349-133">Sayfalar yayımlanır ve geliştirme aracında bu işlemle ilgili bir bildirim alırsınız.</span><span class="sxs-lookup"><span data-stu-id="2c349-133">The pages are published, and you receive a notification about the operation in the authoring tool.</span></span>

<span data-ttu-id="2c349-134">Sayfa düzenleyicisinden tek bir sayfa yayımlamak için, yordam benzerdir.</span><span class="sxs-lookup"><span data-stu-id="2c349-134">To publish a single page from the page editor, the procedure is similar.</span></span> <span data-ttu-id="2c349-135">Sayfa düzenleyicisinde açık olduğu sürece, iade edilmiş olduğundan emin olun ve sonra komut çubuğunda **yayınla**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="2c349-135">While the page is open in the page editor, make sure that it has been checked in, and then select **Publish** on the command bar.</span></span> <span data-ttu-id="2c349-136">Sayfa yayımlanır ve bu işlemle ilgili bir bildirim alırsınız.</span><span class="sxs-lookup"><span data-stu-id="2c349-136">The page is published, and you receive a notification about the operation.</span></span>

<span data-ttu-id="2c349-137">Bir sayfayı yayımladığınızda, yalnızca sayfa içeriği yayımlanır.</span><span class="sxs-lookup"><span data-stu-id="2c349-137">When you publish a page, just the page content is published.</span></span> <span data-ttu-id="2c349-138">Siz ve diğer kullanıcılar sayfaya gidip URL ile ilişkilendirildikten sonra görebilir.</span><span class="sxs-lookup"><span data-stu-id="2c349-138">You and other users can go to the page and view it only after a URL is associated with it.</span></span> <span data-ttu-id="2c349-139">URL'nin ayrı olarak yayımlanması gerekir.</span><span class="sxs-lookup"><span data-stu-id="2c349-139">The URL must be published separately.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="2c349-140">Bir sayfayı yayımlayabilmeniz için, sayfanın referans aldığı tüm resimler veya parçalar önceden yayımlanmış olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="2c349-140">Before you can publish a page, any images or fragments that the page references must already be published.</span></span>

## <a name="save-preview-and-publish-a-home-page"></a><span data-ttu-id="2c349-141">Giriş sayfa kaydetme, önizleme ve yayımlama</span><span class="sxs-lookup"><span data-stu-id="2c349-141">Save, preview, and publish a home page</span></span>

<span data-ttu-id="2c349-142">Bir giriş sayfasını kaydetmek, önizlemek ve yayınlamak için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="2c349-142">To save, preview, and publish a home page, follow these steps.</span></span>

1. <span data-ttu-id="2c349-143">**Siteler** altında, **Fabrikam**'ı seçin (veya sitenizin adını).</span><span class="sxs-lookup"><span data-stu-id="2c349-143">Under **Sites**, select **Fabrikam** (or the name of your site).</span></span>
1. <span data-ttu-id="2c349-144">Soldaki gezinti bölmesinde **Sayfalar** seçin.</span><span class="sxs-lookup"><span data-stu-id="2c349-144">In the navigation pane on the left, select **Pages**.</span></span>
1. <span data-ttu-id="2c349-145">Sayfa düzenleyicisinde açmak için giriş sayfasını bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="2c349-145">Find and select the home page to open it in the page editor.</span></span>
1. <span data-ttu-id="2c349-146">**Düzenle** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="2c349-146">Select **Edit**.</span></span>
1. <span data-ttu-id="2c349-147">Sayfayı gerektiği gibi değiştirin.</span><span class="sxs-lookup"><span data-stu-id="2c349-147">Modify the page as you require.</span></span>
1. <span data-ttu-id="2c349-148">**Kaydet** i seçin ve sonra **Düzenlemeyi bitir**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="2c349-148">Select **Save**, and then select **Finish editing**.</span></span>
1. <span data-ttu-id="2c349-149">**Yorumlar** alanına yaptığınız değişikliklerle ilgili bir not girin ve **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="2c349-149">In the **Comments** field, enter a note about the changes that you made, and then select **OK**.</span></span>
1. <span data-ttu-id="2c349-150">Sayfanızın önizlemesini görüntülemek için **Önizleme**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="2c349-150">Select **Preview** to preview your page.</span></span> <span data-ttu-id="2c349-151">Bitirdiğinizde, geliştirme aracına dönmek için Önizleme sekmesini kapatın.</span><span class="sxs-lookup"><span data-stu-id="2c349-151">When you've finished, close the preview tab to return to the authoring tool.</span></span>
1. <span data-ttu-id="2c349-152">**Yayımla**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="2c349-152">Select **Publish**.</span></span>

## <a name="publish-a-url"></a><span data-ttu-id="2c349-153">URL Yayımla</span><span class="sxs-lookup"><span data-stu-id="2c349-153">Publish a URL</span></span>

<span data-ttu-id="2c349-154">Bir URL yayımlamak için şu adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="2c349-154">To publish a URL, follow these steps.</span></span>

1. <span data-ttu-id="2c349-155">**Siteler** altında, **Fabrikam**'ı seçin (veya sitenizin adını).</span><span class="sxs-lookup"><span data-stu-id="2c349-155">Under **Sites**, select **Fabrikam** (or the name of your site).</span></span>
1. <span data-ttu-id="2c349-156">Soldaki gezinti bölmesinde **URL'leri** seçin.</span><span class="sxs-lookup"><span data-stu-id="2c349-156">In the navigation pane on the left, select **URLs**.</span></span>
1. <span data-ttu-id="2c349-157">Yayınlamak için URL bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="2c349-157">Find and select the URL to publish.</span></span>
1. <span data-ttu-id="2c349-158">Komut çubuğunda, **Yayınla** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="2c349-158">On the command bar, select **Publish**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="2c349-159">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="2c349-159">Additional resources</span></span>

[<span data-ttu-id="2c349-160">Var olan site sayfasını değiştirme</span><span class="sxs-lookup"><span data-stu-id="2c349-160">Modify an existing site page</span></span>](modify-existing-page.md)

[<span data-ttu-id="2c349-161">Yeni site sayfası ekleme</span><span class="sxs-lookup"><span data-stu-id="2c349-161">Add a new site page</span></span>](add-new-page.md)

[<span data-ttu-id="2c349-162">Sayfa düzeni seçme</span><span class="sxs-lookup"><span data-stu-id="2c349-162">Select page layouts</span></span>](select-page-layouts.md)

[<span data-ttu-id="2c349-163">SEO meta verilerini yönetme</span><span class="sxs-lookup"><span data-stu-id="2c349-163">Manage SEO metadata</span></span>](manage-seo-metadata.md)

[<span data-ttu-id="2c349-164">Ürün sayfasını zenginleştirme</span><span class="sxs-lookup"><span data-stu-id="2c349-164">Enrich a product page</span></span>](enrich-product-page.md)

[<span data-ttu-id="2c349-165">Kategori açılış sayfasını zenginleştirme</span><span class="sxs-lookup"><span data-stu-id="2c349-165">Enrich a category landing page</span></span>](enrich-category-page.md)

[<span data-ttu-id="2c349-166">Sayfa içeriği erişilebilirliğini doğrulama</span><span class="sxs-lookup"><span data-stu-id="2c349-166">Verify page content accessibility</span></span>](verify-accessibility.md)

[<span data-ttu-id="2c349-167">URL parametrelerini temel alan dinamik e-ticaret sayfaları oluşturma</span><span class="sxs-lookup"><span data-stu-id="2c349-167">Create dynamic e-commerce pages based on URL parameters</span></span>](create-dynamic-pages.md)
