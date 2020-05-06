---
title: Var olan site sayfasını değiştirme
description: Bu konuda, Microsoft Dynamics 365 Commerce'te mevcut site sayfasını değiştirme yöntemi açıklanmıştır.
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
ms.openlocfilehash: 87c90ed6ee62a094fe44f549c827cf9de2bf5b2f
ms.sourcegitcommit: 7a1d01122790b904e2d96a7ea9f1d003392358a6
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/17/2020
ms.locfileid: "3270016"
---
# <a name="modify-an-existing-site-page"></a><span data-ttu-id="2424b-103">Var olan site sayfasını değiştirme</span><span class="sxs-lookup"><span data-stu-id="2424b-103">Modify an existing site page</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="2424b-104">Bu konuda, Microsoft Dynamics 365 Commerce'te mevcut site sayfasını değiştirme yöntemi açıklanmıştır.</span><span class="sxs-lookup"><span data-stu-id="2424b-104">This topic describes how to modify an existing site page in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="2424b-105">Genel Bakış</span><span class="sxs-lookup"><span data-stu-id="2424b-105">Overview</span></span>

<span data-ttu-id="2424b-106">Bir sayfayı değiştirmeniz gerektiğinde, ilk adım onu sayfa düzenleyici içinde açar.</span><span class="sxs-lookup"><span data-stu-id="2424b-106">When you must modify a page, the first step is to open it in the page editor.</span></span> <span data-ttu-id="2424b-107">Sayfanızı içeren siteye gidin ve sonra sayfa listesinde istediğiniz sayfayı bulun.</span><span class="sxs-lookup"><span data-stu-id="2424b-107">Go to the site that contains your page, and then, in the list of pages, find the page that you want.</span></span> <span data-ttu-id="2424b-108">Sayfayı bulamazsanız, yazma aracının zengin arama işlevini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="2424b-108">If you can't find the page, you can use the authoring tool's rich search functionality.</span></span> <span data-ttu-id="2424b-109">Tam sayfa adını yazın veya adın ilk birkaç harfini yazıp bir yıldız işareti (\*) yazın.</span><span class="sxs-lookup"><span data-stu-id="2424b-109">Either type the exact page name, or type the first few letters of it and then an asterisk (\*).</span></span> <span data-ttu-id="2424b-110">Süzülmüş sayfalar listesi görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="2424b-110">A filtered list of pages appears.</span></span> <span data-ttu-id="2424b-111">İstediğiniz sayfayı bulmak için bu listeyi kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="2424b-111">You can use this list to find the page that you want.</span></span> <span data-ttu-id="2424b-112">Doğru sayfayı bulduktan sonra, sayfa düzenleyicisinde sayfayı açılacak sayfa adını seçin.</span><span class="sxs-lookup"><span data-stu-id="2424b-112">After you find the correct page, select the page name to open the page in the page editor.</span></span>

> [!TIP]
> <span data-ttu-id="2424b-113">Sayfanız sayfa denetçisinde görünüyorsa, **Düzenle**'yi seçebilir ve sayfayı sayfa düzenleyicisinde açılmadan önce kullanıma alabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="2424b-113">If your page is visible in the page inspector, you can select **Edit** and check the page out before you open it in the page editor.</span></span> <span data-ttu-id="2424b-114">Böylece, aynı anda birden fazla sayfayı kullanıma alabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="2424b-114">In this way, you can check out multiple pages at the same time.</span></span>

<span data-ttu-id="2424b-115">Sayfa düzenleyicide sayfanın açık olmasını istiyorsanız, öğenin kullanımınıza alındığından emin olmalısınız.</span><span class="sxs-lookup"><span data-stu-id="2424b-115">After the page is open in the page editor, you must make sure that it's checked out to you.</span></span> <span data-ttu-id="2424b-116">Geliştirme aracındaki komut çubuğu dinamiktir, içeriğe duyarlıdır ve durum duyarlıdır.</span><span class="sxs-lookup"><span data-stu-id="2424b-116">The command bar in the authoring tool is dynamic, context-sensitive, and state-sensitive.</span></span> <span data-ttu-id="2424b-117">Bu nedenle, yalnızca sayfada gerçekleştirebileceğiniz eylemleri gösterir.</span><span class="sxs-lookup"><span data-stu-id="2424b-117">Therefore, it shows only the actions that you can currently perform on the page.</span></span> <span data-ttu-id="2424b-118">Örneğin, sayfa sizin tarafınızdan kullanıma alınmadığından, komut çubuğunda **Kaydet** ve **Düzenlemeyi bitir** düğmeleri görünmez.</span><span class="sxs-lookup"><span data-stu-id="2424b-118">For example, if the page isn't checked out to you, the **Save** and **Finish editing** buttons don't appear on the command bar.</span></span> <span data-ttu-id="2424b-119">Sayfanın durumu pencerenin sağ tarafında görünür.</span><span class="sxs-lookup"><span data-stu-id="2424b-119">The state of the page is also shown on the right side of the window.</span></span>

<span data-ttu-id="2424b-120">Sayfa sizin tarafınızdan kullanıma alınmış durumda değilse, komut çubuğundan **Düzenle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="2424b-120">If the page isn't already checked out to you, select **Edit** on the command bar.</span></span> <span data-ttu-id="2424b-121">Komut çubuğu, sayfanın yeni durumunu yansıtacak şekilde değişir.</span><span class="sxs-lookup"><span data-stu-id="2424b-121">The command bar changes to reflect the new state of the page.</span></span> <span data-ttu-id="2424b-122">Ayrıca, sayfanın size teslim edilmiş olduğunu bildiren bir bildirim alırsınız.</span><span class="sxs-lookup"><span data-stu-id="2424b-122">You also receive a notification that states that the page was checked out to you.</span></span>

<span data-ttu-id="2424b-123">Sonraki adım, gerçek değişikliklerinizi yapmak içindir.</span><span class="sxs-lookup"><span data-stu-id="2424b-123">The next step is to make your actual changes.</span></span> <span data-ttu-id="2424b-124">Genellikle, sol taraftaki sayfa anahat ağacını kullanarak değiştirmek istediğiniz modülü bulun ve seçin ve sonra sağdaki Özellikler bölmesinde değişiklikleri yapın.</span><span class="sxs-lookup"><span data-stu-id="2424b-124">Often, you will use the page outline tree on the left to find and select the module that you want to change, and then make changes in the properties pane on the right.</span></span> 

<span data-ttu-id="2424b-125">Ancak, yaptığınız değişiklikler bazen model veya parçacık eklemeyi veya kaldırmayı içerebilir.</span><span class="sxs-lookup"><span data-stu-id="2424b-125">However, your change might sometimes involve adding or removing models or fragments.</span></span> <span data-ttu-id="2424b-126">Parça veya modül eklemek için, modül veya parçayı eklemek istediğiniz yuvayı bulmak amacıyla sayfa anahattı ağacını ve sonra o yuva için üç nokta düğmesini (**...**) kullanın.</span><span class="sxs-lookup"><span data-stu-id="2424b-126">To add a fragment or module, use the page outline tree to find the slot that you want to add the module or fragment to, and then select the ellipsis button (**...**) for that slot.</span></span> <span data-ttu-id="2424b-127">Modül veya parça eklemek için kullanılan komutları içeren bir menü görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="2424b-127">A menu appears that includes commands for adding a module or fragment.</span></span> <span data-ttu-id="2424b-128">Bir modül veya parçayı kaldırmak için sayfa anahat ağacında bunu bulun ve seçin, üç nokta düğmesini seçin ve sonra modülü veya parçayı silmek için komutu seçin.</span><span class="sxs-lookup"><span data-stu-id="2424b-128">To remove a module or fragment, find and select it in the page outline tree, select the ellipsis button, and then select the command to delete the module or fragment.</span></span>

> [!TIP]
> <span data-ttu-id="2424b-129">Ayrıca, doğrudan seçerek "aldığınız şey gördüğünüz şeydir" (WYSIWYG) önizlemesi görünür olan herhangi bir modülün özelliklerini görüntüleyebilir ve düzenleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="2424b-129">You can also view and edit the properties for any module that is visible in the "what you see is what you get" (WYSIWYG) preview by selecting it directly.</span></span>

<span data-ttu-id="2424b-130">Değişikliklerinizi yapmayı bitirdikten ve etkilerini önizledikten sonra, komut çubuğunda **Düzenlemeyi bitir**'i seçerek sayfayı iade etmelisiniz.</span><span class="sxs-lookup"><span data-stu-id="2424b-130">After you've finished making your changes and previewing their effect, you should check in the page by selecting **Finish editing** on the command bar.</span></span> 

<span data-ttu-id="2424b-131">Değişikliklerinizi hemen yayımlamak için, komut çubuğunda **yayınla** 'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="2424b-131">To publish your changes immediately, select **Publish** on the command bar.</span></span> <span data-ttu-id="2424b-132">Değiştirdiğiniz sayfanın en son iade edilen sürümü yayımlanır ve sitenizi görüntüleyen harici kullanıcılar tarafından kullanılabilir duruma gelir.</span><span class="sxs-lookup"><span data-stu-id="2424b-132">The latest checked-in version of the page that you modified is published and becomes available to external users who view your site.</span></span> 

## <a name="example-change-the-video-on-the-home-page"></a><span data-ttu-id="2424b-133">Örnek: giriş sayfasındaki videoyu değiştirme</span><span class="sxs-lookup"><span data-stu-id="2424b-133">Example: Change the video on the home page</span></span>

<span data-ttu-id="2424b-134">Aşağıdaki örnek, video oynatıcı modülünde görünen videoyu değiştirerek giriş sayfasının nasıl değiştirileceğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="2424b-134">The following example shows how to modify the home page by changing the video that appears in the video player module.</span></span>

1. <span data-ttu-id="2424b-135">**Siteler** altında, **Fabrikam**'ı seçin (veya sitenizin adını).</span><span class="sxs-lookup"><span data-stu-id="2424b-135">Under **Sites**, select **Fabrikam** (or the name of your site).</span></span>
1. <span data-ttu-id="2424b-136">Soldaki gezinti bölmesinde **Sayfalar** seçin.</span><span class="sxs-lookup"><span data-stu-id="2424b-136">In the navigation pane on the left, select **Pages**.</span></span>
1. <span data-ttu-id="2424b-137">Sayfa düzenleyicisinde açmak için giriş sayfasını bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="2424b-137">Find and select the home page to open it in the page editor.</span></span>
1. <span data-ttu-id="2424b-138">Komut çubuğunda, **Düzenle** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="2424b-138">On the command bar, select **Edit**.</span></span>
1. <span data-ttu-id="2424b-139">Sayfa anahattında **ana** yuvayı seçin.</span><span class="sxs-lookup"><span data-stu-id="2424b-139">In the page outline, select the **Main** slot.</span></span>
1. <span data-ttu-id="2424b-140">**Ana** yuvanın altında, tüm akışkan konteyneri modüllerini genişletin.</span><span class="sxs-lookup"><span data-stu-id="2424b-140">Under the **Main** slot, expand all the fluid container modules.</span></span>
1. <span data-ttu-id="2424b-141">Video oynatıcı modülünü bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="2424b-141">Find and select the video player module.</span></span>
1. <span data-ttu-id="2424b-142">Sağdaki özellikler bölmesinde, **video** özelliğini seçin.</span><span class="sxs-lookup"><span data-stu-id="2424b-142">In the properties pane on the right, select the **video** property.</span></span> <span data-ttu-id="2424b-143">Varlık seçici görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="2424b-143">The asset picker appears.</span></span>
1. <span data-ttu-id="2424b-144">Varlık seçicisinde, uygun bir video varlığı seçin veya yeni bir video varlığı yüklemek için **yeni varlığı yükle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="2424b-144">In the asset picker, select an available video asset, or select **Upload new asset** to upload a new video asset.</span></span>
1. <span data-ttu-id="2424b-145">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="2424b-145">Select **OK**.</span></span>
1. <span data-ttu-id="2424b-146">**Kaydet**i seçin ve sonra **Düzenlemeyi bitir**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="2424b-146">Select **Save**, and then select **Finish editing**.</span></span>
1. <span data-ttu-id="2424b-147">**Yorumlar** alanında **Videoyu değiştir** seçeneğini girin ve **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="2424b-147">In the **Comments** field, enter **Changed the video**, and then select **OK**.</span></span>
1. <span data-ttu-id="2424b-148">Güncellenen sayfasını önizlemek için **Önizleme** 'yi seçin .</span><span class="sxs-lookup"><span data-stu-id="2424b-148">Select **Preview** to preview the updated page.</span></span> <span data-ttu-id="2424b-149">Bitirdiğinizde, geliştirme aracına dönmek için Önizleme sekmesini kapatın.</span><span class="sxs-lookup"><span data-stu-id="2424b-149">When you've finished, close the preview tab to return to the authoring tool.</span></span>
1. <span data-ttu-id="2424b-150">**Yayımla**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="2424b-150">Select **Publish**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="2424b-151">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="2424b-151">Additional resources</span></span>

[<span data-ttu-id="2424b-152">Yeni site sayfası ekleme</span><span class="sxs-lookup"><span data-stu-id="2424b-152">Add a new site page</span></span>](add-new-page.md)

[<span data-ttu-id="2424b-153">Sayfa düzeni seçme</span><span class="sxs-lookup"><span data-stu-id="2424b-153">Select page layouts</span></span>](select-page-layouts.md)

[<span data-ttu-id="2424b-154">SEO meta verilerini yönetme</span><span class="sxs-lookup"><span data-stu-id="2424b-154">Manage SEO metadata</span></span>](manage-seo-metadata.md)

[<span data-ttu-id="2424b-155">Sayfa kaydetme, önizleme ve yayımlama</span><span class="sxs-lookup"><span data-stu-id="2424b-155">Save, preview, and publish a page</span></span>](save-preview-publish-page.md)

[<span data-ttu-id="2424b-156">Ürün sayfasını zenginleştirme</span><span class="sxs-lookup"><span data-stu-id="2424b-156">Enrich a product page</span></span>](enrich-product-page.md)

[<span data-ttu-id="2424b-157">Kategori açılış sayfasını zenginleştirme</span><span class="sxs-lookup"><span data-stu-id="2424b-157">Enrich a category landing page</span></span>](enrich-category-page.md)

[<span data-ttu-id="2424b-158">Sayfa içeriği erişilebilirliğini doğrula</span><span class="sxs-lookup"><span data-stu-id="2424b-158">Verify page content accessibility</span></span>](verify-accessibility.md)
