---
title: Sayfa kaydetme, önizleme ve yayımlama
description: Bu konuda, Microsoft Dynamics 365 Commerce'te sayfa kaydetme, önizleme ve yayınlama yöntemi açıklanmıştır.
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
ms.openlocfilehash: 8c1b82b1b8423c63d442ee581ed0cc8789ee63fd
ms.sourcegitcommit: 295d940a345879b3dfc5991e387b91c7257019ea
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/01/2019
ms.locfileid: "2697900"
---
# <a name="save-preview-and-publish-a-page"></a><span data-ttu-id="dfdf4-103">Sayfa kaydetme, önizleme ve yayımlama</span><span class="sxs-lookup"><span data-stu-id="dfdf4-103">Save, preview, and publish a page</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="dfdf4-104">Bu konuda, Microsoft Dynamics 365 Commerce'te sayfa kaydetme, önizleme ve yayınlama yöntemi açıklanmıştır.</span><span class="sxs-lookup"><span data-stu-id="dfdf4-104">This topic describes how to save, preview, and publish a page in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="save-a-page"></a><span data-ttu-id="dfdf4-105">Sayfa kaydetme</span><span class="sxs-lookup"><span data-stu-id="dfdf4-105">Save a page</span></span>

<span data-ttu-id="dfdf4-106">Sayfayı kaydetmek için, belgenizi kullanıma almış ve sayfa düzenleyicisinde açmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="dfdf4-106">To save a page, you must have it checked out to yourself and open in the page editor.</span></span> <span data-ttu-id="dfdf4-107">Bir sayfayı değiştirdikten sonra, değişikliklerinizin saklanmasını sağlamaya yardımcı olması için bir sayfaya hemen kaydetmelisiniz.</span><span class="sxs-lookup"><span data-stu-id="dfdf4-107">You should save a page immediately after you modify it, to help guarantee that your changes are stored.</span></span>

<span data-ttu-id="dfdf4-108">Bir sayfayı kaydettiğinizde, değişiklikler yalnızca size görünebilir.</span><span class="sxs-lookup"><span data-stu-id="dfdf4-108">When you save a page, the changes are visible only to you.</span></span> <span data-ttu-id="dfdf4-109">Kaydetme işlemi öncelikle, sayfa henüz iade edilmeye hazır olmadığı sürece değişiklikleri depolamaya yöneliktir.</span><span class="sxs-lookup"><span data-stu-id="dfdf4-109">The save operation is intended primarily to store changes while the page isn't yet ready to be checked in.</span></span> <span data-ttu-id="dfdf4-110">Sayfayı değiştirmeyi bitirdiğinizde, gözden geçirin ve böylece değişiklikler başkaları tarafından görülebilir hale gelir.</span><span class="sxs-lookup"><span data-stu-id="dfdf4-110">When you've finished modifying the page, we recommend that you check it in, so that the changes become visible to others.</span></span> <span data-ttu-id="dfdf4-111">Bu noktada, sayfa değiştirilmesi gereken diğer kullanıcılar tarafından da kullanıma açılabilir.</span><span class="sxs-lookup"><span data-stu-id="dfdf4-111">At that point, the page can also be checked out by other users who must modify it.</span></span>

## <a name="preview-a-page"></a><span data-ttu-id="dfdf4-112">Sayfayı önizleme</span><span class="sxs-lookup"><span data-stu-id="dfdf4-112">Preview a page</span></span>

<span data-ttu-id="dfdf4-113">Geliştirme aracı, iki tür önizleme özelliği sunar: Sayfa düzenleyicisinde "gördüğünüz şey aldığınız şeydir" (WYSIWYG) Önizleme bölmesi ve ayrı bir önizleme penceresi sağlar.</span><span class="sxs-lookup"><span data-stu-id="dfdf4-113">The authoring tool offers two kinds of preview features: a "what you see is what you get" (WYSIWYG) preview pane in the page editor and a separate preview window.</span></span>

<span data-ttu-id="dfdf4-114">Sayfa düzenleyicisini kullanırken, Orta bölmede "aldığınız şey görüntülenir" (WYSIWYG) önizlemesi görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="dfdf4-114">While you're using the page editor, a "what you see is what you get" (WYSIWYG) preview appears in the center pane.</span></span> <span data-ttu-id="dfdf4-115">Bu önizleme, sayfayı her kaydedişinizde otomatik olarak güncelleştirilir.</span><span class="sxs-lookup"><span data-stu-id="dfdf4-115">This preview is automatically updated whenever you save the page.</span></span> <span data-ttu-id="dfdf4-116">Bunu, komut çubuğunda **Yenile** seçerek el ile de güncelleştirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="dfdf4-116">You can also manually update it by selecting **Refresh** on the command bar.</span></span> <span data-ttu-id="dfdf4-117">WYSIWYG önizlemesi, sayfayı sitenin kullanıcıları görer gibi işler, ancak geliştirme yardımcıları üzerinde işlenir.</span><span class="sxs-lookup"><span data-stu-id="dfdf4-117">The WYSIWYG preview renders the page just as the site's users will see it, but authoring helpers are rendered on top of it.</span></span>

<span data-ttu-id="dfdf4-118">Sayfayı değiştirmeyi bitirdiğinizde, hangi müşterilerin görebileceğini görmek için önizlemek isteyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="dfdf4-118">When you've finished modifying the page, you might want to preview it to see what customers will see.</span></span> <span data-ttu-id="dfdf4-119">Bir sayfayı önizlemek için, komut çubuğunda **önizleme**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="dfdf4-119">To preview a page, select **Preview** on the command bar.</span></span> <span data-ttu-id="dfdf4-120">Önizleme, ayrı bir tarayıcı penceresinde görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="dfdf4-120">The preview will appear in a separate browser window.</span></span> <span data-ttu-id="dfdf4-121">Önizleme penceresindeki sayfa, sitenin kullanıcısı tarafından göreceğiniz şekilde oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="dfdf4-121">The page in the preview window is rendered just as the site's user will see it.</span></span> <span data-ttu-id="dfdf4-122">Yanıt veren modüllerin tüm görünüm bağlantı noktalarında doğru şekilde işlendiğine emin olmak için pencereyi yeniden boyutlandırabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="dfdf4-122">You can resize the window to make sure that responsive modules are correctly rendered in all view ports.</span></span>

> [!NOTE]
> <span data-ttu-id="dfdf4-123">Yayımlanmamış içeriğin önizlemesi için kimlik doğrulama ve doğru izinler gereklidir.</span><span class="sxs-lookup"><span data-stu-id="dfdf4-123">Authentication and correct permissions are required to preview unpublished content.</span></span> <span data-ttu-id="dfdf4-124">Bu nedenle, önizlemenin URL'sini başka biriyle paylaşıyorsanız bu kişinin içeriğe erişmek için doğru izinlere sahip olması gerekir.</span><span class="sxs-lookup"><span data-stu-id="dfdf4-124">Therefore, if you share the URL of the preview with someone, that person must have the correct permissions to access the content.</span></span>

## <a name="publish-a-page"></a><span data-ttu-id="dfdf4-125">Sayfayı yayımla</span><span class="sxs-lookup"><span data-stu-id="dfdf4-125">Publish a page</span></span>

<span data-ttu-id="dfdf4-126">Sayfanız hazır olduğunda, bir sonraki adım bunu yayınlamaktır, böylece harici kullanıcılar içeriği görüntüleyebilir.</span><span class="sxs-lookup"><span data-stu-id="dfdf4-126">When your page is ready, the next step is to publish it, so that external users can view the content.</span></span> <span data-ttu-id="dfdf4-127">Bir sayfayı yayımlayabilmeniz için önce onu iade etmelisiniz.</span><span class="sxs-lookup"><span data-stu-id="dfdf4-127">Before you can publish a page, you must check it in.</span></span>

<span data-ttu-id="dfdf4-128">Sayfaları sayfa denetçisinde veya sayfa düzenleyicisinden yayımlayabilir veya yayımdan kaldırabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="dfdf4-128">You can publish and unpublish pages from either the page inspector or the page editor.</span></span> <span data-ttu-id="dfdf4-129">Sayfa denetçisi, sayfaların listesini gösterir ve toplu işlemlere izin verir.</span><span class="sxs-lookup"><span data-stu-id="dfdf4-129">The page inspector shows a list of pages and allows for bulk operations.</span></span> <span data-ttu-id="dfdf4-130">Sayfa düzenleyicisi, yalnızca içinde açık olan tek bir sayfayı yayınlamak veya yayımdan kaldırmak için kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="dfdf4-130">The page editor can be used to publish or unpublish only the single page that is open in it.</span></span>

<span data-ttu-id="dfdf4-131">Sayfa denetçisinde bir veya daha fazla sayfa yayınlamak için sayfaları seçin, bunların iade edilmiş olduklarından emin olun ve sonra komut çubuğunda **Yayınla**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="dfdf4-131">To publish one or more pages from the page inspector, select the pages, make sure that they are checked in, and then select **Publish** on the command bar.</span></span> <span data-ttu-id="dfdf4-132">Sayfalar yayımlanır ve geliştirme aracında bu işlemle ilgili bir bildirim alırsınız.</span><span class="sxs-lookup"><span data-stu-id="dfdf4-132">The pages are published, and you receive a notification about the operation in the authoring tool.</span></span>

<span data-ttu-id="dfdf4-133">Sayfa düzenleyicisinden tek bir sayfa yayımlamak için, yordam benzerdir.</span><span class="sxs-lookup"><span data-stu-id="dfdf4-133">To publish a single page from the page editor, the procedure is similar.</span></span> <span data-ttu-id="dfdf4-134">Sayfa düzenleyicisinde açık olduğu sürece, iade edilmiş olduğundan emin olun ve sonra komut çubuğunda **yayınla**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="dfdf4-134">While the page is open in the page editor, make sure that it has been checked in, and then select **Publish** on the command bar.</span></span> <span data-ttu-id="dfdf4-135">Sayfa yayımlanır ve bu işlemle ilgili bir bildirim alırsınız.</span><span class="sxs-lookup"><span data-stu-id="dfdf4-135">The page is published, and you receive a notification about the operation.</span></span>

<span data-ttu-id="dfdf4-136">Bir sayfayı yayımladığınızda, yalnızca sayfa içeriği yayımlanır.</span><span class="sxs-lookup"><span data-stu-id="dfdf4-136">When you publish a page, just the page content is published.</span></span> <span data-ttu-id="dfdf4-137">Siz ve diğer kullanıcılar sayfaya gidip URL ile ilişkilendirildikten sonra görebilir.</span><span class="sxs-lookup"><span data-stu-id="dfdf4-137">You and other users can go to the page and view it only after a URL is associated with it.</span></span> <span data-ttu-id="dfdf4-138">URL'nin ayrı olarak yayımlanması gerekir.</span><span class="sxs-lookup"><span data-stu-id="dfdf4-138">The URL must be published separately.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="dfdf4-139">Bir sayfayı yayımlayabilmeniz için, sayfanın referans aldığı tüm resimler veya parçalar önceden yayımlanmış olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="dfdf4-139">Before you can publish a page, any images or fragments that the page references must already be published.</span></span>

## <a name="save-preview-and-publish-a-home-page"></a><span data-ttu-id="dfdf4-140">Giriş sayfa kaydetme, önizleme ve yayımlama</span><span class="sxs-lookup"><span data-stu-id="dfdf4-140">Save, preview, and publish a home page</span></span>

<span data-ttu-id="dfdf4-141">Bir giriş sayfasını kaydetmek, önizlemek ve yayınlamak için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="dfdf4-141">To save, preview, and publish a home page, follow these steps.</span></span>

1. <span data-ttu-id="dfdf4-142">**Siteler** altında, **Fabrikam**'ı seçin (veya sitenizin adını).</span><span class="sxs-lookup"><span data-stu-id="dfdf4-142">Under **Sites**, select **Fabrikam** (or the name of your site).</span></span>
1. <span data-ttu-id="dfdf4-143">Soldaki gezinti bölmesinde **Sayfalar** seçin.</span><span class="sxs-lookup"><span data-stu-id="dfdf4-143">In the navigation pane on the left, select **Pages**.</span></span>
1. <span data-ttu-id="dfdf4-144">Sayfa düzenleyicisinde açmak için giriş sayfasını bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="dfdf4-144">Find and select the home page to open it in the page editor.</span></span>
1. <span data-ttu-id="dfdf4-145">**Ödeme yap** seçin.</span><span class="sxs-lookup"><span data-stu-id="dfdf4-145">Select **Check Out**.</span></span>
1. <span data-ttu-id="dfdf4-146">Sayfayı gerektiği gibi değiştirin.</span><span class="sxs-lookup"><span data-stu-id="dfdf4-146">Modify the page as you require.</span></span>
1. <span data-ttu-id="dfdf4-147">**Kaydet**i seçin ve sonra **Giriş**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="dfdf4-147">Select **Save**, and then select **Check In**.</span></span>
1. <span data-ttu-id="dfdf4-148">**Yorumlar** alanına yaptığınız değişikliklerle ilgili bir not girin ve **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="dfdf4-148">In the **Comments** field, enter a note about the changes that you made, and then select **OK**.</span></span>
1. <span data-ttu-id="dfdf4-149">Sayfanızın önizlemesini görüntülemek için **Önizleme**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="dfdf4-149">Select **Preview** to preview your page.</span></span> <span data-ttu-id="dfdf4-150">Bitirdiğinizde, geliştirme aracına dönmek için Önizleme sekmesini kapatın.</span><span class="sxs-lookup"><span data-stu-id="dfdf4-150">When you've finished, close the preview tab to return to the authoring tool.</span></span>
1. <span data-ttu-id="dfdf4-151">**Yayımla**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="dfdf4-151">Select **Publish**.</span></span>

## <a name="publish-a-url"></a><span data-ttu-id="dfdf4-152">URL Yayımla</span><span class="sxs-lookup"><span data-stu-id="dfdf4-152">Publish a URL</span></span>

<span data-ttu-id="dfdf4-153">Bir URL yayımlamak için şu adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="dfdf4-153">To publish a URL, follow these steps.</span></span>

1. <span data-ttu-id="dfdf4-154">**Siteler** altında, **Fabrikam**'ı seçin (veya sitenizin adını).</span><span class="sxs-lookup"><span data-stu-id="dfdf4-154">Under **Sites**, select **Fabrikam** (or the name of your site).</span></span>
1. <span data-ttu-id="dfdf4-155">Soldaki gezinti bölmesinde **URL'leri** seçin.</span><span class="sxs-lookup"><span data-stu-id="dfdf4-155">In the navigation pane on the left, select **URLs**.</span></span>
1. <span data-ttu-id="dfdf4-156">Yayınlamak için URL bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="dfdf4-156">Find and select the URL to publish.</span></span>
1. <span data-ttu-id="dfdf4-157">Komut çubuğunda, **Yayınla** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="dfdf4-157">On the command bar, select **Publish**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="dfdf4-158">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="dfdf4-158">Additional resources</span></span>

[<span data-ttu-id="dfdf4-159">Var olan site sayfasını değiştirme</span><span class="sxs-lookup"><span data-stu-id="dfdf4-159">Modify an existing site page</span></span>](modify-existing-page.md)

[<span data-ttu-id="dfdf4-160">Yeni site sayfası ekleme</span><span class="sxs-lookup"><span data-stu-id="dfdf4-160">Add a new site page</span></span>](add-new-page.md)

[<span data-ttu-id="dfdf4-161">Sayfa düzeni seçme</span><span class="sxs-lookup"><span data-stu-id="dfdf4-161">Select page layouts</span></span>](select-page-layouts.md)

[<span data-ttu-id="dfdf4-162">SEO meta verilerini yönetme</span><span class="sxs-lookup"><span data-stu-id="dfdf4-162">Manage SEO metadata</span></span>](manage-seo-metadata.md)

[<span data-ttu-id="dfdf4-163">Ürün sayfasını zenginleştirme</span><span class="sxs-lookup"><span data-stu-id="dfdf4-163">Enrich a product page</span></span>](enrich-product-page.md)

[<span data-ttu-id="dfdf4-164">Kategori açılış sayfasını zenginleştirme</span><span class="sxs-lookup"><span data-stu-id="dfdf4-164">Enrich a category landing page</span></span>](enrich-category-page.md)

