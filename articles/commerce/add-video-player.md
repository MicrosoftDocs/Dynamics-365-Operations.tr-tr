---
title: Video oynatıcı modülü
description: Bu konu vide oynatıcı modüllerini kapsamaktadır ve Microsoft Dynamics 365 Commerce'un site sayfalarına nasıl ekleneceğini açıklamaktadır.
author: anupamar-ms
manager: annbe
ms.date: 01/23/2020
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
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: e94658eed12b12d6666e63d2c06b86646c81a120
ms.sourcegitcommit: 829329220475ed8cff5a5db92a59dd90c22b04fa
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/05/2020
ms.locfileid: "3025698"
---
# <a name="video-player-module"></a><span data-ttu-id="b50cb-103">Video oynatıcı modülü</span><span class="sxs-lookup"><span data-stu-id="b50cb-103">Video player module</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="b50cb-104">Bu konu vide oynatıcı modüllerini kapsamaktadır ve Microsoft Dynamics 365 Commerce'un site sayfalarına nasıl ekleneceğini açıklamaktadır.</span><span class="sxs-lookup"><span data-stu-id="b50cb-104">This topic covers video player modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="b50cb-105">Genel Bakış</span><span class="sxs-lookup"><span data-stu-id="b50cb-105">Overview</span></span>

<span data-ttu-id="b50cb-106">Video oynatımını desteklemek için video oynatma modülü kullanılır.</span><span class="sxs-lookup"><span data-stu-id="b50cb-106">The video player module is used to support video playback.</span></span> <span data-ttu-id="b50cb-107">Video içeriğinin içerik yönetim sistemi ne (CMS) yüklenmesi ve kullanılabilir olması koşuluyla, herhangi bir sayfaya eklenebilir.</span><span class="sxs-lookup"><span data-stu-id="b50cb-107">It can be added to any page, provided that video content is uploaded to and available in the content management system (CMS).</span></span> <span data-ttu-id="b50cb-108">Video oynatıcı modülü .mp4 ortam türünü destekler.</span><span class="sxs-lookup"><span data-stu-id="b50cb-108">The video player module supports the .mp4 media type.</span></span>

## <a name="video-player-module"></a><span data-ttu-id="b50cb-109">Video oynatıcı modülü</span><span class="sxs-lookup"><span data-stu-id="b50cb-109">Video player module</span></span>

<span data-ttu-id="b50cb-110">Video oynatıcı modülü bir e-ticaret sitesinde videoları sergileyebilecek şekilde kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="b50cb-110">The video player module can be used to showcase videos on an e-Commerce site.</span></span> <span data-ttu-id="b50cb-111">Yürüt, Duraklat, tam boyut modu, ses açıklamaları ve kapalı açıklamalı alt yazılar gibi tüm kayıttan yürütme yeteneklerini destekler.</span><span class="sxs-lookup"><span data-stu-id="b50cb-111">It supports all playback capabilities, such as play, pause, full-size mode, audio descriptions, and closed captions.</span></span> <span data-ttu-id="b50cb-112">Video oynatıcı modülü, Microsoft erişilebilirlik standartlarını karşılamak için kapalı açıklamalı alt yazıların özelleştirmesini de destekler.</span><span class="sxs-lookup"><span data-stu-id="b50cb-112">The video player module also supports customization of closed captions to meet Microsoft accessibility standards.</span></span> <span data-ttu-id="b50cb-113">Örneğin, yazı tipi boyutunu ve arka plan rengini özelleştirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="b50cb-113">For example, you can customize the font size and background color.</span></span>

<span data-ttu-id="b50cb-114">Video oynatıcı modülü ikincil ses parçalarını da destekler.</span><span class="sxs-lookup"><span data-stu-id="b50cb-114">The video player module also supports secondary audio tracks.</span></span> <span data-ttu-id="b50cb-115">Bir video CMS'ye karşıya yüklendiğinde, ikincil bir ses parçası da karşıya yüklenebilir.</span><span class="sxs-lookup"><span data-stu-id="b50cb-115">When a video is uploaded to the CMS, a secondary audio track can also be uploaded.</span></span> <span data-ttu-id="b50cb-116">Böylece, bir kullanıcı seçerse, video oynatıcı modülü ikincil ses kanalını yürütebilir.</span><span class="sxs-lookup"><span data-stu-id="b50cb-116">The video player module can then play the secondary audio track if a user selects it.</span></span>

### <a name="examples-of-video-player-modules-in-e-commerce"></a><span data-ttu-id="b50cb-117">E-ticaret'da video oynatıcı modülleri örnekleri</span><span class="sxs-lookup"><span data-stu-id="b50cb-117">Examples of video player modules in e-Commerce</span></span>

- <span data-ttu-id="b50cb-118">Ürün Ayrıntıları sayfalarındaki veya pazarlama sayfalarındaki yönerge videoları</span><span class="sxs-lookup"><span data-stu-id="b50cb-118">Instructional videos on product details pages or marketing pages</span></span>
- <span data-ttu-id="b50cb-119">Tüm pazarlama sayfaları üzerindeki ilkelerle ilgili videolar veya promosyon videoları</span><span class="sxs-lookup"><span data-stu-id="b50cb-119">Promotional videos or videos about policies on any marketing page</span></span>
- <span data-ttu-id="b50cb-120">Ürün Ayrıntıları sayfalarındaki veya pazarlama sayfalarındaki ürün özelliklerini vurgulayan pazarlama videoları</span><span class="sxs-lookup"><span data-stu-id="b50cb-120">Marketing videos that highlight product features on product details pages or marketing pages</span></span>

### <a name="video-player-module-properties"></a><span data-ttu-id="b50cb-121">Video oynatıcı modülü özellikleri</span><span class="sxs-lookup"><span data-stu-id="b50cb-121">Video player module properties</span></span>

| <span data-ttu-id="b50cb-122">Özellik adı</span><span class="sxs-lookup"><span data-stu-id="b50cb-122">Property name</span></span>         | <span data-ttu-id="b50cb-123">Değer</span><span class="sxs-lookup"><span data-stu-id="b50cb-123">Value</span></span>                               | <span data-ttu-id="b50cb-124">Tanım</span><span class="sxs-lookup"><span data-stu-id="b50cb-124">Description</span></span> |
|-----------------------|-------------------------------------|-------------|
| <span data-ttu-id="b50cb-125">Otomatik Yürütme</span><span class="sxs-lookup"><span data-stu-id="b50cb-125">Auto play</span></span>             | <span data-ttu-id="b50cb-126">**Doğru** veya **yanlış**</span><span class="sxs-lookup"><span data-stu-id="b50cb-126">**True** or **False**</span></span>               | <span data-ttu-id="b50cb-127">Değer **doğru** olarak ayarlandığında, video otomatik olarak yürütülür.</span><span class="sxs-lookup"><span data-stu-id="b50cb-127">When the value is set to **True**, the video is automatically played.</span></span> |
| <span data-ttu-id="b50cb-128">Sesi Kapat</span><span class="sxs-lookup"><span data-stu-id="b50cb-128">Mute</span></span>                  | <span data-ttu-id="b50cb-129">**Doğru** veya **yanlış**</span><span class="sxs-lookup"><span data-stu-id="b50cb-129">**True** or **False**</span></span>               | <span data-ttu-id="b50cb-130">Değer **doğru** olarak ayarlandığında, ses kapatılır.</span><span class="sxs-lookup"><span data-stu-id="b50cb-130">When the value is set to **True**, the audio is muted.</span></span> <span data-ttu-id="b50cb-131">Bu oynatıcı için varsayılan değer **yanlış**'tır.</span><span class="sxs-lookup"><span data-stu-id="b50cb-131">For this player, the default value is **False**.</span></span> <span data-ttu-id="b50cb-132">Chrome tarayıcıda, Otomatik yürütme videoları varsayılan olarak kapalı ve ses ancak videoyu el ile oynadığında yürütülür.</span><span class="sxs-lookup"><span data-stu-id="b50cb-132">In the Chrome browser, autoplay videos are muted by default, and the audio is played only if the user manually plays the video.</span></span> |
| <span data-ttu-id="b50cb-133">Döngü</span><span class="sxs-lookup"><span data-stu-id="b50cb-133">Loop</span></span>                  | <span data-ttu-id="b50cb-134">**Doğru** veya **yanlış**</span><span class="sxs-lookup"><span data-stu-id="b50cb-134">**True** or **False**</span></span>               | <span data-ttu-id="b50cb-135">Değer **doğru** olarak ayarlandığında, video döngü olarak tekrarlanır.</span><span class="sxs-lookup"><span data-stu-id="b50cb-135">When the value is set to **True**, the video is repeated in a loop.</span></span> |
| <span data-ttu-id="b50cb-136">Ortam</span><span class="sxs-lookup"><span data-stu-id="b50cb-136">Media</span></span>                 | <span data-ttu-id="b50cb-137">Video dosya yolu ve adı.</span><span class="sxs-lookup"><span data-stu-id="b50cb-137">Video file path and name</span></span> | <span data-ttu-id="b50cb-138">Video oynatıcı tarafından oynanan video dosyası.</span><span class="sxs-lookup"><span data-stu-id="b50cb-138">The video file that is played in the video player.</span></span> |
| <span data-ttu-id="b50cb-139">Tam ekran oynat</span><span class="sxs-lookup"><span data-stu-id="b50cb-139">Play fullscreen</span></span>       | <span data-ttu-id="b50cb-140">**Doğru** veya **yanlış**</span><span class="sxs-lookup"><span data-stu-id="b50cb-140">**True** or **False**</span></span>               | <span data-ttu-id="b50cb-141">Değer **doğru** olarak ayarlandığında, video tam ekran modunda yürütülür.</span><span class="sxs-lookup"><span data-stu-id="b50cb-141">When the value is set to **True**, the video is played in full-screen mode.</span></span> |
| <span data-ttu-id="b50cb-142">Oynat/duraklat tetikleyicisi</span><span class="sxs-lookup"><span data-stu-id="b50cb-142">Play pause trigger</span></span>    | <span data-ttu-id="b50cb-143">**Doğru** veya **yanlış**</span><span class="sxs-lookup"><span data-stu-id="b50cb-143">**True** or **False**</span></span>               | <span data-ttu-id="b50cb-144">Değer **doğru** olarak ayarlandığında, videoda bir Oynat/Duraklat düğmesi görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="b50cb-144">When the value is set to **True**, a play/pause button is shown on the video.</span></span> |
| <span data-ttu-id="b50cb-145">Video oynatıcı denetimleri</span><span class="sxs-lookup"><span data-stu-id="b50cb-145">Video player controls</span></span> | <span data-ttu-id="b50cb-146">**Doğru** veya **yanlış**</span><span class="sxs-lookup"><span data-stu-id="b50cb-146">**True** or **False**</span></span>               | <span data-ttu-id="b50cb-147">Değer **Doğru** olarak ayarlandığında, tüm video oynatıcı denetimler gösterilir.</span><span class="sxs-lookup"><span data-stu-id="b50cb-147">When the value is set to **True**, all video player controls are shown.</span></span> <span data-ttu-id="b50cb-148">Bu denetimler, oynat ve Duraklat düğmelerini, ilerleme göstergesini ve açıklamalı alt yazıları seçeneklerini içerir.</span><span class="sxs-lookup"><span data-stu-id="b50cb-148">These controls include play and pause buttons, a progress indicator, and closed caption options.</span></span> |
| <span data-ttu-id="b50cb-149">Poster görüntüsünü gizle</span><span class="sxs-lookup"><span data-stu-id="b50cb-149">Hide poster image</span></span>     | <span data-ttu-id="b50cb-150">**Doğru** veya **yanlış**</span><span class="sxs-lookup"><span data-stu-id="b50cb-150">**True** or **False**</span></span>               | <span data-ttu-id="b50cb-151">Videoda poster karesi olabilir.</span><span class="sxs-lookup"><span data-stu-id="b50cb-151">A video can have a poster frame.</span></span> <span data-ttu-id="b50cb-152">Bu özelliğin değeri **doğru** olarak ayarlandığında, poster çerçevesi gizlenir.</span><span class="sxs-lookup"><span data-stu-id="b50cb-152">When the value of this property is set to **True**, the poster frame is hidden.</span></span> |
| <span data-ttu-id="b50cb-153">Maske düzeyi</span><span class="sxs-lookup"><span data-stu-id="b50cb-153">Mask level</span></span>            | <span data-ttu-id="b50cb-154">**0** ile **100** arasında bir sayı</span><span class="sxs-lookup"><span data-stu-id="b50cb-154">A number from **0** through **100**</span></span> | <span data-ttu-id="b50cb-155">Stil oluşturma için videoya uygulanan maske.</span><span class="sxs-lookup"><span data-stu-id="b50cb-155">The mask that is applied to the video for styling.</span></span> |

## <a name="add-a-video-player-module-to-a-page"></a><span data-ttu-id="b50cb-156">Sayfaya video oynatıcı modülü ekleme</span><span class="sxs-lookup"><span data-stu-id="b50cb-156">Add a video player module to a page</span></span>

> [!NOTE] 
> <span data-ttu-id="b50cb-157">Video oynatıcı modülü oluşturmadan önce, ortam kitaplığı 'na bir video yüklemeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="b50cb-157">Before you create a video player module, you must first upload a video to the Media Library.</span></span>

<span data-ttu-id="b50cb-158">Bir yeni sayfaya video oynatma modülü eklemek ve gerekli özellikleri ayarlamak için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="b50cb-158">To add a video player module to a new page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="b50cb-159">**Video oynatıcı şablonu** adlı bir sayfa şablonu oluşturun.</span><span class="sxs-lookup"><span data-stu-id="b50cb-159">Create a page template that is named **video player template**.</span></span>
1. <span data-ttu-id="b50cb-160">Varsayılan sayfanın **ana** yuvasına bir konteyner modülü ekleyin.</span><span class="sxs-lookup"><span data-stu-id="b50cb-160">In the **Main** slot of the default page, add a container module.</span></span>
1. <span data-ttu-id="b50cb-161">Konteyner modülünde, video oynatıcı ve ortam video oynatıcı modülleri ekleyin.</span><span class="sxs-lookup"><span data-stu-id="b50cb-161">In the container module, add video player and ambient video player modules.</span></span>
1. <span data-ttu-id="b50cb-162">Şablon düzenlemeyi tamamlayın ve sonra yayımlayın.</span><span class="sxs-lookup"><span data-stu-id="b50cb-162">Finish editing the template, and publish it.</span></span>
1. <span data-ttu-id="b50cb-163">**Video oynatıcı sayfası** adlı bir sayfa oluşturmak için yeni oluşturduğunuz video oynatıcı şablonunu kullanın.</span><span class="sxs-lookup"><span data-stu-id="b50cb-163">Use the video player template that you created to create a page that is named **video player page**.</span></span>
1. <span data-ttu-id="b50cb-164">Yeni sayfanın **ana** yuvasına bir video oynatıcı modülü ekleyin.</span><span class="sxs-lookup"><span data-stu-id="b50cb-164">In the **Main** slot of the new page, add a video player module.</span></span>
1. <span data-ttu-id="b50cb-165">Video oynatıcı modülüyle ilgili Özellik bölmesinde **video Ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="b50cb-165">In the property pane for the video player module, select **Add a video**.</span></span>
1. <span data-ttu-id="b50cb-166">**Ortam Seçicisi** iletişim kutusunda bir video seçin ve sonra **yeni ortam öğesiniyükle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="b50cb-166">In the **Media Picker** dialog box, select a video, and then select **Upload new media item**.</span></span>
1. <span data-ttu-id="b50cb-167">Sayfayı kaydet ve önizleyin.</span><span class="sxs-lookup"><span data-stu-id="b50cb-167">Save and preview the page.</span></span> <span data-ttu-id="b50cb-168">Sayfada video modülünü görmelisiniz.</span><span class="sxs-lookup"><span data-stu-id="b50cb-168">You should see the video module on the page.</span></span> <span data-ttu-id="b50cb-169">Modülün davranışını özelleştirmek için ek ayarları değiştirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="b50cb-169">You can change additional settings to customize the behavior of the module.</span></span>
1. <span data-ttu-id="b50cb-170">Sayfayı düzenlemeyi tamamlayın ve sonra yayımlayın.</span><span class="sxs-lookup"><span data-stu-id="b50cb-170">Finish editing the page, and publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="b50cb-171">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="b50cb-171">Additional resources</span></span>

[<span data-ttu-id="b50cb-172">Başlangıç paketine genel bakış</span><span class="sxs-lookup"><span data-stu-id="b50cb-172">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="b50cb-173">Promosyon başlık modülü</span><span class="sxs-lookup"><span data-stu-id="b50cb-173">Promo banner module</span></span>](add-alert.md)

[<span data-ttu-id="b50cb-174">Döngü modülü</span><span class="sxs-lookup"><span data-stu-id="b50cb-174">Carousel module</span></span>](add-carousel.md)

[<span data-ttu-id="b50cb-175">Metin bloku modülü</span><span class="sxs-lookup"><span data-stu-id="b50cb-175">Text block module</span></span>](add-content-rich-block.md)

[<span data-ttu-id="b50cb-176">İçerik blok modülü</span><span class="sxs-lookup"><span data-stu-id="b50cb-176">Content block module</span></span>](add-hero-module.md)
