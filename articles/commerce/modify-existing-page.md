---
title: Var olan site sayfasını değiştirme
description: Bu konuda, Microsoft Dynamics 365 Commerce'te mevcut site sayfasını değiştirme yöntemi açıklanmıştır.
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
ms.openlocfilehash: b633965e45c16cb4e5991fab67783b867223f6ec
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/31/2021
ms.locfileid: "5803741"
---
# <a name="modify-an-existing-site-page"></a><span data-ttu-id="47547-103">Var olan site sayfasını değiştirme</span><span class="sxs-lookup"><span data-stu-id="47547-103">Modify an existing site page</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="47547-104">Bu konuda, Microsoft Dynamics 365 Commerce'te mevcut site sayfasını değiştirme yöntemi açıklanmıştır.</span><span class="sxs-lookup"><span data-stu-id="47547-104">This topic describes how to modify an existing site page in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="47547-105">Bir sayfayı değiştirmeniz gerektiğinde, ilk adım onu sayfa düzenleyici içinde açar.</span><span class="sxs-lookup"><span data-stu-id="47547-105">When you must modify a page, the first step is to open it in the page editor.</span></span> <span data-ttu-id="47547-106">Sayfanızı içeren siteye gidin ve sonra sayfa listesinde istediğiniz sayfayı bulun.</span><span class="sxs-lookup"><span data-stu-id="47547-106">Go to the site that contains your page, and then, in the list of pages, find the page that you want.</span></span> <span data-ttu-id="47547-107">Sayfayı bulamazsanız, yazma aracının zengin arama işlevini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="47547-107">If you can't find the page, you can use the authoring tool's rich search functionality.</span></span> <span data-ttu-id="47547-108">Tam sayfa adını yazın veya adın ilk birkaç harfini yazıp bir yıldız işareti (\*) yazın.</span><span class="sxs-lookup"><span data-stu-id="47547-108">Either type the exact page name, or type the first few letters of it and then an asterisk (\*).</span></span> <span data-ttu-id="47547-109">Süzülmüş sayfalar listesi görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="47547-109">A filtered list of pages appears.</span></span> <span data-ttu-id="47547-110">İstediğiniz sayfayı bulmak için bu listeyi kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="47547-110">You can use this list to find the page that you want.</span></span> <span data-ttu-id="47547-111">Doğru sayfayı bulduktan sonra, sayfa düzenleyicisinde sayfayı açılacak sayfa adını seçin.</span><span class="sxs-lookup"><span data-stu-id="47547-111">After you find the correct page, select the page name to open the page in the page editor.</span></span>

> [!TIP]
> <span data-ttu-id="47547-112">Sayfanız sayfa denetçisinde görünüyorsa, **Düzenle**'yi seçebilir ve sayfayı sayfa düzenleyicisinde açılmadan önce kullanıma alabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="47547-112">If your page is visible in the page inspector, you can select **Edit** and check the page out before you open it in the page editor.</span></span> <span data-ttu-id="47547-113">Böylece, aynı anda birden fazla sayfayı kullanıma alabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="47547-113">In this way, you can check out multiple pages at the same time.</span></span>

<span data-ttu-id="47547-114">Sayfa düzenleyicide sayfanın açık olmasını istiyorsanız, öğenin kullanımınıza alındığından emin olmalısınız.</span><span class="sxs-lookup"><span data-stu-id="47547-114">After the page is open in the page editor, you must make sure that it's checked out to you.</span></span> <span data-ttu-id="47547-115">Geliştirme aracındaki komut çubuğu dinamiktir, içeriğe duyarlıdır ve durum duyarlıdır.</span><span class="sxs-lookup"><span data-stu-id="47547-115">The command bar in the authoring tool is dynamic, context-sensitive, and state-sensitive.</span></span> <span data-ttu-id="47547-116">Bu nedenle, yalnızca sayfada gerçekleştirebileceğiniz eylemleri gösterir.</span><span class="sxs-lookup"><span data-stu-id="47547-116">Therefore, it shows only the actions that you can currently perform on the page.</span></span> <span data-ttu-id="47547-117">Örneğin, sayfa sizin tarafınızdan kullanıma alınmadığından, komut çubuğunda **Kaydet** ve **Düzenlemeyi bitir** düğmeleri görünmez.</span><span class="sxs-lookup"><span data-stu-id="47547-117">For example, if the page isn't checked out to you, the **Save** and **Finish editing** buttons don't appear on the command bar.</span></span> <span data-ttu-id="47547-118">Sayfanın durumu pencerenin sağ tarafında görünür.</span><span class="sxs-lookup"><span data-stu-id="47547-118">The state of the page is also shown on the right side of the window.</span></span>

<span data-ttu-id="47547-119">Sayfa sizin tarafınızdan kullanıma alınmış durumda değilse, komut çubuğundan **Düzenle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="47547-119">If the page isn't already checked out to you, select **Edit** on the command bar.</span></span> <span data-ttu-id="47547-120">Komut çubuğu, sayfanın yeni durumunu yansıtacak şekilde değişir.</span><span class="sxs-lookup"><span data-stu-id="47547-120">The command bar changes to reflect the new state of the page.</span></span> <span data-ttu-id="47547-121">Ayrıca, sayfanın size teslim edilmiş olduğunu bildiren bir bildirim alırsınız.</span><span class="sxs-lookup"><span data-stu-id="47547-121">You also receive a notification that states that the page was checked out to you.</span></span>

<span data-ttu-id="47547-122">Sonraki adım, gerçek değişikliklerinizi yapmak içindir.</span><span class="sxs-lookup"><span data-stu-id="47547-122">The next step is to make your actual changes.</span></span> <span data-ttu-id="47547-123">Genellikle, sol taraftaki sayfa anahat ağacını kullanarak değiştirmek istediğiniz modülü bulun ve seçin ve sonra sağdaki Özellikler bölmesinde değişiklikleri yapın.</span><span class="sxs-lookup"><span data-stu-id="47547-123">Often, you will use the page outline tree on the left to find and select the module that you want to change, and then make changes in the properties pane on the right.</span></span> 

<span data-ttu-id="47547-124">Ancak, yaptığınız değişiklikler bazen model veya parçacık eklemeyi veya kaldırmayı içerebilir.</span><span class="sxs-lookup"><span data-stu-id="47547-124">However, your change might sometimes involve adding or removing models or fragments.</span></span> <span data-ttu-id="47547-125">Parça veya modül eklemek için, modül veya parçayı eklemek istediğiniz yuvayı bulmak amacıyla sayfa anahattı ağacını ve sonra o yuva için üç nokta düğmesini (**...**) kullanın.</span><span class="sxs-lookup"><span data-stu-id="47547-125">To add a fragment or module, use the page outline tree to find the slot that you want to add the module or fragment to, and then select the ellipsis button (**...**) for that slot.</span></span> <span data-ttu-id="47547-126">Modül veya parça eklemek için kullanılan komutları içeren bir menü görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="47547-126">A menu appears that includes commands for adding a module or fragment.</span></span> <span data-ttu-id="47547-127">Bir modül veya parçayı kaldırmak için sayfa anahat ağacında bunu bulun ve seçin, üç nokta düğmesini seçin ve sonra modülü veya parçayı silmek için komutu seçin.</span><span class="sxs-lookup"><span data-stu-id="47547-127">To remove a module or fragment, find and select it in the page outline tree, select the ellipsis button, and then select the command to delete the module or fragment.</span></span>

> [!TIP]
> <span data-ttu-id="47547-128">Ayrıca, doğrudan seçerek görsel sayfa oluşturucu önizlemesinde görünür olan herhangi bir modülün özelliklerini görüntüleyebilir ve düzenleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="47547-128">You can also view and edit the properties for any module that is visible in the visual page builder preview by selecting it directly.</span></span>

<span data-ttu-id="47547-129">Değişikliklerinizi yapmayı bitirdikten ve etkilerini önizledikten sonra, komut çubuğunda **Düzenlemeyi bitir**'i seçerek sayfayı iade etmelisiniz.</span><span class="sxs-lookup"><span data-stu-id="47547-129">After you've finished making your changes and previewing their effect, you should check in the page by selecting **Finish editing** on the command bar.</span></span> 

<span data-ttu-id="47547-130">Değişikliklerinizi hemen yayımlamak için, komut çubuğunda **yayınla** 'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="47547-130">To publish your changes immediately, select **Publish** on the command bar.</span></span> <span data-ttu-id="47547-131">Değiştirdiğiniz sayfanın en son iade edilen sürümü yayımlanır ve sitenizi görüntüleyen harici kullanıcılar tarafından kullanılabilir duruma gelir.</span><span class="sxs-lookup"><span data-stu-id="47547-131">The latest checked-in version of the page that you modified is published and becomes available to external users who view your site.</span></span> 

## <a name="example-change-the-video-on-the-home-page"></a><span data-ttu-id="47547-132">Örnek: giriş sayfasındaki videoyu değiştirme</span><span class="sxs-lookup"><span data-stu-id="47547-132">Example: Change the video on the home page</span></span>

<span data-ttu-id="47547-133">Aşağıdaki örnek, video oynatıcı modülünde görünen videoyu değiştirerek giriş sayfasının nasıl değiştirileceğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="47547-133">The following example shows how to modify the home page by changing the video that appears in the video player module.</span></span>

1. <span data-ttu-id="47547-134">**Siteler** altında, **Fabrikam**'ı seçin (veya sitenizin adını).</span><span class="sxs-lookup"><span data-stu-id="47547-134">Under **Sites**, select **Fabrikam** (or the name of your site).</span></span>
1. <span data-ttu-id="47547-135">Soldaki gezinti bölmesinde **Sayfalar** seçin.</span><span class="sxs-lookup"><span data-stu-id="47547-135">In the navigation pane on the left, select **Pages**.</span></span>
1. <span data-ttu-id="47547-136">Sayfa düzenleyicisinde açmak için giriş sayfasını bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="47547-136">Find and select the home page to open it in the page editor.</span></span>
1. <span data-ttu-id="47547-137">Komut çubuğunda, **Düzenle** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="47547-137">On the command bar, select **Edit**.</span></span>
1. <span data-ttu-id="47547-138">Sayfa anahattında **ana** yuvayı seçin.</span><span class="sxs-lookup"><span data-stu-id="47547-138">In the page outline, select the **Main** slot.</span></span>
1. <span data-ttu-id="47547-139">**Ana** yuvanın altında, tüm akışkan konteyneri modüllerini genişletin.</span><span class="sxs-lookup"><span data-stu-id="47547-139">Under the **Main** slot, expand all the fluid container modules.</span></span>
1. <span data-ttu-id="47547-140">Video oynatıcı modülünü bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="47547-140">Find and select the video player module.</span></span>
1. <span data-ttu-id="47547-141">Sağdaki özellikler bölmesinde, **video** özelliğini seçin.</span><span class="sxs-lookup"><span data-stu-id="47547-141">In the properties pane on the right, select the **video** property.</span></span> <span data-ttu-id="47547-142">Varlık seçici görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="47547-142">The asset picker appears.</span></span>
1. <span data-ttu-id="47547-143">Varlık seçicisinde, uygun bir video varlığı seçin veya yeni bir video varlığı yüklemek için **yeni varlığı yükle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="47547-143">In the asset picker, select an available video asset, or select **Upload new asset** to upload a new video asset.</span></span>
1. <span data-ttu-id="47547-144">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="47547-144">Select **OK**.</span></span>
1. <span data-ttu-id="47547-145">**Kaydet** i seçin ve sonra **Düzenlemeyi bitir**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="47547-145">Select **Save**, and then select **Finish editing**.</span></span>
1. <span data-ttu-id="47547-146">**Yorumlar** alanında **Videoyu değiştir** seçeneğini girin ve **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="47547-146">In the **Comments** field, enter **Changed the video**, and then select **OK**.</span></span>
1. <span data-ttu-id="47547-147">Güncellenen sayfasını önizlemek için **Önizleme** 'yi seçin .</span><span class="sxs-lookup"><span data-stu-id="47547-147">Select **Preview** to preview the updated page.</span></span> <span data-ttu-id="47547-148">Bitirdiğinizde, geliştirme aracına dönmek için Önizleme sekmesini kapatın.</span><span class="sxs-lookup"><span data-stu-id="47547-148">When you've finished, close the preview tab to return to the authoring tool.</span></span>
1. <span data-ttu-id="47547-149">**Yayımla**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="47547-149">Select **Publish**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="47547-150">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="47547-150">Additional resources</span></span>

[<span data-ttu-id="47547-151">Yeni site sayfası ekleme</span><span class="sxs-lookup"><span data-stu-id="47547-151">Add a new site page</span></span>](add-new-page.md)

[<span data-ttu-id="47547-152">Sayfa düzeni seçme</span><span class="sxs-lookup"><span data-stu-id="47547-152">Select page layouts</span></span>](select-page-layouts.md)

[<span data-ttu-id="47547-153">SEO meta verilerini yönetme</span><span class="sxs-lookup"><span data-stu-id="47547-153">Manage SEO metadata</span></span>](manage-seo-metadata.md)

[<span data-ttu-id="47547-154">Sayfa kaydetme, önizleme ve yayımlama</span><span class="sxs-lookup"><span data-stu-id="47547-154">Save, preview, and publish a page</span></span>](save-preview-publish-page.md)

[<span data-ttu-id="47547-155">Ürün sayfasını zenginleştirme</span><span class="sxs-lookup"><span data-stu-id="47547-155">Enrich a product page</span></span>](enrich-product-page.md)

[<span data-ttu-id="47547-156">Kategori açılış sayfasını zenginleştirme</span><span class="sxs-lookup"><span data-stu-id="47547-156">Enrich a category landing page</span></span>](enrich-category-page.md)

[<span data-ttu-id="47547-157">Sayfa içeriği erişilebilirliğini doğrulama</span><span class="sxs-lookup"><span data-stu-id="47547-157">Verify page content accessibility</span></span>](verify-accessibility.md)

[<span data-ttu-id="47547-158">URL parametrelerini temel alan dinamik e-ticaret sayfaları oluşturma</span><span class="sxs-lookup"><span data-stu-id="47547-158">Create dynamic e-commerce pages based on URL parameters</span></span>](create-dynamic-pages.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
