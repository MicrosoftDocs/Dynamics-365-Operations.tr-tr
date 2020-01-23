---
title: Var olan site sayfasını değiştirme
description: Bu konuda, Microsoft Dynamics 365 Commerce'te mevcut site sayfasını değiştirme yöntemi açıklanmıştır.
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
ms.openlocfilehash: 50373d3681e269bf6164b2a425bbafebdd93d64f
ms.sourcegitcommit: ef3a1d7527311d00b69a1072ae5eb021ce68034c
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/09/2020
ms.locfileid: "2945709"
---
# <a name="modify-an-existing-site-page"></a><span data-ttu-id="93c78-103">Var olan site sayfasını değiştirme</span><span class="sxs-lookup"><span data-stu-id="93c78-103">Modify an existing site page</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="93c78-104">Bu konuda, Microsoft Dynamics 365 Commerce'te mevcut site sayfasını değiştirme yöntemi açıklanmıştır.</span><span class="sxs-lookup"><span data-stu-id="93c78-104">This topic describes how to modify an existing site page in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="93c78-105">Genel Bakış</span><span class="sxs-lookup"><span data-stu-id="93c78-105">Overview</span></span>

<span data-ttu-id="93c78-106">Bir sayfayı değiştirmeniz gerektiğinde, ilk adım onu sayfa düzenleyici içinde açar.</span><span class="sxs-lookup"><span data-stu-id="93c78-106">When you must modify a page, the first step is to open it in the page editor.</span></span> <span data-ttu-id="93c78-107">Sayfanızı içeren siteye gidin ve sonra sayfa listesinde istediğiniz sayfayı bulun.</span><span class="sxs-lookup"><span data-stu-id="93c78-107">Go to the site that contains your page, and then, in the list of pages, find the page that you want.</span></span> <span data-ttu-id="93c78-108">Sayfayı bulamazsanız, yazma aracının zengin arama işlevini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="93c78-108">If you can't find the page, you can use the authoring tool's rich search functionality.</span></span> <span data-ttu-id="93c78-109">Tam sayfa adını yazın veya adın ilk birkaç harfini yazıp bir yıldız işareti (\*) yazın.</span><span class="sxs-lookup"><span data-stu-id="93c78-109">Either type the exact page name, or type the first few letters of it and then an asterisk (\*).</span></span> <span data-ttu-id="93c78-110">Süzülmüş sayfalar listesi görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="93c78-110">A filtered list of pages appears.</span></span> <span data-ttu-id="93c78-111">İstediğiniz sayfayı bulmak için bu listeyi kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="93c78-111">You can use this list to find the page that you want.</span></span> <span data-ttu-id="93c78-112">Doğru sayfayı bulduktan sonra, sayfa düzenleyicisinde sayfayı açılacak sayfa adını seçin.</span><span class="sxs-lookup"><span data-stu-id="93c78-112">After you find the correct page, select the page name to open the page in the page editor.</span></span>

> [!TIP]
> <span data-ttu-id="93c78-113">Sayfanız sayfa denetçisinde görünüyorsa, onu seçebilir ve sayfa düzenleyicisinde açılmadan önce teslim edebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="93c78-113">If your page is visible in the page inspector, you can select it and check it out before you open it in the page editor.</span></span> <span data-ttu-id="93c78-114">Böylece, aynı anda birden fazla sayfayı kullanıma alabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="93c78-114">In this way, you can check out multiple pages at the same time.</span></span>

<span data-ttu-id="93c78-115">Sayfa düzenleyicide sayfanın açık olmasını istiyorsanız, öğenin kullanımınıza alındığından emin olmalısınız.</span><span class="sxs-lookup"><span data-stu-id="93c78-115">After the page is open in the page editor, you must make sure that it's checked out to you.</span></span> <span data-ttu-id="93c78-116">Geliştirme aracındaki komut çubuğu dinamiktir, içeriğe duyarlıdır ve durum duyarlıdır.</span><span class="sxs-lookup"><span data-stu-id="93c78-116">The command bar in the authoring tool is dynamic, context-sensitive, and state-sensitive.</span></span> <span data-ttu-id="93c78-117">Bu nedenle, yalnızca sayfada gerçekleştirebileceğiniz eylemleri gösterir.</span><span class="sxs-lookup"><span data-stu-id="93c78-117">Therefore, it shows only the actions that you can curently perform on the page.</span></span> <span data-ttu-id="93c78-118">Örneğin, sayfa sizin tarafınızdan kullanıma alınmadığından, komut çubuğunda **Kaydet** ve **Giriş yap** düğmeleri görünmez.</span><span class="sxs-lookup"><span data-stu-id="93c78-118">For example, if the page isn't checked out to you, the **Save** and **Check in** buttons don't appear on the command bar.</span></span> <span data-ttu-id="93c78-119">Sayfanın durumu pencerenin sağ tarafında görünür.</span><span class="sxs-lookup"><span data-stu-id="93c78-119">The state of the page is also shown on the right side of the window.</span></span>

<span data-ttu-id="93c78-120">Sayfa sizin tarafınızdan kullanıma alınmış durumda değilse, komut çubuğundan **kullanıma alma** 'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="93c78-120">If the page isn't already checked out to you, select **Check out** on the command bar.</span></span> <span data-ttu-id="93c78-121">Komut çubuğu, sayfanın yeni durumunu yansıtacak şekilde değişir.</span><span class="sxs-lookup"><span data-stu-id="93c78-121">The command bar changes to reflect the new state of the page.</span></span> <span data-ttu-id="93c78-122">Ayrıca, sayfanın size teslim edilmiş olduğunu bildiren bir bildirim alırsınız.</span><span class="sxs-lookup"><span data-stu-id="93c78-122">You also receive a notification that states that the page was checked out to you.</span></span>

<span data-ttu-id="93c78-123">Sonraki adım, gerçek değişikliklerinizi yapmak içindir.</span><span class="sxs-lookup"><span data-stu-id="93c78-123">The next step is to make your actual changes.</span></span> <span data-ttu-id="93c78-124">Genellikle, sol taraftaki sayfa anahat ağacını kullanarak değiştirmek istediğiniz modülü bulun ve seçin ve sonra sağdaki Özellikler bölmesinde değişiklikleri yapın.</span><span class="sxs-lookup"><span data-stu-id="93c78-124">Often, you will use the page outline tree on the left to find and select the module that you want to change, and then make changes in the properties pane on the right.</span></span> 

<span data-ttu-id="93c78-125">Ancak, yaptığınız değişiklikler bazen model veya parçacık eklemeyi veya kaldırmayı içerebilir.</span><span class="sxs-lookup"><span data-stu-id="93c78-125">However, your change might sometimes involve adding or removing models or fragments.</span></span> <span data-ttu-id="93c78-126">Parça veya modül eklemek için, modül veya parçayı eklemek istediğiniz yuvayı bulmak amacıyla sayfa anahattı ağacını ve sonra o yuva için üç nokta düğmesini (**...**) kullanın.</span><span class="sxs-lookup"><span data-stu-id="93c78-126">To add a fragment or module, use the page outline tree to find the slot that you want to add the module or fragment to, and then select the ellipsis button (**...**) for that slot.</span></span> <span data-ttu-id="93c78-127">Modül veya parça eklemek için kullanılan komutları içeren bir menü görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="93c78-127">A menu appears that includes commands for adding a module or fragment.</span></span> <span data-ttu-id="93c78-128">Bir modül veya parçayı kaldırmak için sayfa anahat ağacında bunu bulun ve seçin, üç nokta düğmesini seçin ve sonra modülü veya parçayı silmek için komutu seçin.</span><span class="sxs-lookup"><span data-stu-id="93c78-128">To remove a module or fragment, find and select it in the page outline tree, select the ellipsis button, and then select the command to delete the module or fragment.</span></span>

> [!TIP]
> <span data-ttu-id="93c78-129">Ayrıca, doğrudan seçerek "aldığınız şey gördüğünüz şeydir" (WYSIWYG) önizlemesi görünür olan herhangi bir modülün özelliklerini görüntüleyebilir ve düzenleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="93c78-129">You can also view and edit the properties for any module that is visible in the "what you see is what you get" (WYSIWYG) preview by selecting it directly.</span></span>

<span data-ttu-id="93c78-130">Değişikliklerinizi yapmayı bitirdikten ve etkilerini önizledikten sonra, komut çubuğunda **iade et**'i seçerek sayfayı iade etmelisiniz.</span><span class="sxs-lookup"><span data-stu-id="93c78-130">After you've finished making your changes and previewing their effect, you should check in the page by selecting **Check in** on the command bar.</span></span> 

<span data-ttu-id="93c78-131">Değişikliklerinizi hemen yayımlamak için, komut çubuğunda **yayınla** 'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="93c78-131">To publish your changes immediately, select **Publish** on the command bar.</span></span> <span data-ttu-id="93c78-132">Değiştirdiğiniz sayfanın en son iade edilen sürümü yayımlanır ve sitenizi görüntüleyen harici kullanıcılar tarafından kullanılabilir duruma gelir.</span><span class="sxs-lookup"><span data-stu-id="93c78-132">The latest checked-in version of the page that you modified is published and becomes available to external users who view your site.</span></span> 

## <a name="example-change-the-video-on-the-home-page"></a><span data-ttu-id="93c78-133">Örnek: giriş sayfasındaki videoyu değiştirme</span><span class="sxs-lookup"><span data-stu-id="93c78-133">Example: Change the video on the home page</span></span>

<span data-ttu-id="93c78-134">Aşağıdaki örnek, video oynatıcı modülünde görünen videoyu değiştirerek giriş sayfasının nasıl değiştirileceğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="93c78-134">The following example shows how to modify the home page by changing the video that appears in the video player module.</span></span>

1. <span data-ttu-id="93c78-135">**Siteler** altında, **Fabrikam**'ı seçin (veya sitenizin adını).</span><span class="sxs-lookup"><span data-stu-id="93c78-135">Under **Sites**, select **Fabrikam** (or the name of your site).</span></span>
1. <span data-ttu-id="93c78-136">Soldaki gezinti bölmesinde **Sayfalar** seçin.</span><span class="sxs-lookup"><span data-stu-id="93c78-136">In the navigation pane on the left, select **Pages**.</span></span>
1. <span data-ttu-id="93c78-137">Sayfa düzenleyicisinde açmak için giriş sayfasını bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="93c78-137">Find and select the home page to open it in the page editor.</span></span>
1. <span data-ttu-id="93c78-138">Komut çubuğunda, **Çıkış yap** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="93c78-138">On the command bar, select **Check Out**.</span></span>
1. <span data-ttu-id="93c78-139">Sayfa anahattında **ana** yuvayı seçin.</span><span class="sxs-lookup"><span data-stu-id="93c78-139">In the page outline, select the **Main** slot.</span></span>
1. <span data-ttu-id="93c78-140">**Ana** yuvanın altında, tüm akışkan konteyneri modüllerini genişletin.</span><span class="sxs-lookup"><span data-stu-id="93c78-140">Under the **Main** slot, expand all the fluid container modules.</span></span>
1. <span data-ttu-id="93c78-141">Video oynatıcı modülünü bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="93c78-141">Find and select the video player module.</span></span>
1. <span data-ttu-id="93c78-142">Sağdaki özellikler bölmesinde, **video** özelliğini seçin.</span><span class="sxs-lookup"><span data-stu-id="93c78-142">In the properties pane on the right, select the **video** property.</span></span> <span data-ttu-id="93c78-143">Varlık seçici görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="93c78-143">The asset picker appears.</span></span>
1. <span data-ttu-id="93c78-144">Varlık seçicisinde, uygun bir video varlığı seçin veya yeni bir video varlığı yüklemek için **yeni varlığı yükle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="93c78-144">In the asset picker, select an available video asset, or select **Upload new asset** to upload a new video asset.</span></span>
1. <span data-ttu-id="93c78-145">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="93c78-145">Select **OK**.</span></span>
1. <span data-ttu-id="93c78-146">**Kaydet**i seçin ve sonra **Giriş**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="93c78-146">Select **Save**, and then select **Check In**.</span></span>
1. <span data-ttu-id="93c78-147">**Yorumlar** alanında **Videoyu değiştir** seçeneğini girin ve **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="93c78-147">In the **Comments** field, enter **Changed the video**, and then select **OK**.</span></span>
1. <span data-ttu-id="93c78-148">Güncellenen sayfasını önizlemek için **Önizleme** 'yi seçin .</span><span class="sxs-lookup"><span data-stu-id="93c78-148">Select **Preview** to preview the updated page.</span></span> <span data-ttu-id="93c78-149">Bitirdiğinizde, geliştirme aracına dönmek için Önizleme sekmesini kapatın.</span><span class="sxs-lookup"><span data-stu-id="93c78-149">When you've finished, close the preview tab to return to the authoring tool.</span></span>
1. <span data-ttu-id="93c78-150">**Yayımla**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="93c78-150">Select **Publish**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="93c78-151">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="93c78-151">Additional resources</span></span>

[<span data-ttu-id="93c78-152">Yeni site sayfası ekleme</span><span class="sxs-lookup"><span data-stu-id="93c78-152">Add a new site page</span></span>](add-new-page.md)

[<span data-ttu-id="93c78-153">Sayfa düzeni seçme</span><span class="sxs-lookup"><span data-stu-id="93c78-153">Select page layouts</span></span>](select-page-layouts.md)

[<span data-ttu-id="93c78-154">SEO meta verilerini yönetme</span><span class="sxs-lookup"><span data-stu-id="93c78-154">Manage SEO metadata</span></span>](manage-seo-metadata.md)

[<span data-ttu-id="93c78-155">Sayfa kaydetme, önizleme ve yayımlama</span><span class="sxs-lookup"><span data-stu-id="93c78-155">Save, preview, and publish a page</span></span>](save-preview-publish-page.md)

[<span data-ttu-id="93c78-156">Ürün sayfasını zenginleştirme</span><span class="sxs-lookup"><span data-stu-id="93c78-156">Enrich a product page</span></span>](enrich-product-page.md)

[<span data-ttu-id="93c78-157">Kategori açılış sayfasını zenginleştirme</span><span class="sxs-lookup"><span data-stu-id="93c78-157">Enrich a category landing page</span></span>](enrich-category-page.md)

[<span data-ttu-id="93c78-158">Sayfa içeriği erişilebilirliğini doğrula</span><span class="sxs-lookup"><span data-stu-id="93c78-158">Verify page content accessibility</span></span>](verify-accessibility.md)
