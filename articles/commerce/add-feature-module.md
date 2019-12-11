---
title: Özellik modülü
description: Bu konu özellik modüllerini kapsamaktadır ve Microsoft Dynamics 365 Commerce'un site sayfalarına nasıl ekleneceğini açıklamaktadır.
author: anupamar-ms
manager: annbe
ms.date: 10/31/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: 76b59681d0bda11446f6db8b2685d1a0656f8f55
ms.sourcegitcommit: 3a4e137ef3a96ba0a58c5352f4a3b57467ace9ae
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/11/2019
ms.locfileid: "2785318"
---
# <a name="feature-module"></a><span data-ttu-id="3501f-103">Özellik modülü</span><span class="sxs-lookup"><span data-stu-id="3501f-103">Feature module</span></span> 

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="3501f-104">Bu konu özellik modüllerini kapsamaktadır ve Microsoft Dynamics 365 Commerce'un site sayfalarına nasıl ekleneceğini açıklamaktadır.</span><span class="sxs-lookup"><span data-stu-id="3501f-104">This topic covers feature modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="3501f-105">Genel Bakış</span><span class="sxs-lookup"><span data-stu-id="3501f-105">Overview</span></span>

<span data-ttu-id="3501f-106">Özellik modülü, ürünleri veya promosyonları bir görüntü ve metin birleşimiyle pazarlamak için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="3501f-106">A feature module is used to market products or promotions through a combination of images and text.</span></span> <span data-ttu-id="3501f-107">Örneğin, bir satıcı ürün ayrıntıları sayfasına, ürünün özelliklerini vurgulamak için özellik modülü ekleyebilir.</span><span class="sxs-lookup"><span data-stu-id="3501f-107">For example, a retailer can add a feature module to a product details page to highlight the features of the product.</span></span>

<span data-ttu-id="3501f-108">Özellik modülü içerik yönetimi sistemindeki (CMS) veriler tarafından yönlendiriliyor.</span><span class="sxs-lookup"><span data-stu-id="3501f-108">A feature module is driven by data from the content management system (CMS).</span></span> <span data-ttu-id="3501f-109">Bunlar sayfadaki diğer modüllere bağımlı olmayan bağımsız modüllerdir.</span><span class="sxs-lookup"><span data-stu-id="3501f-109">It's a stand-alone module that doesn't depend on any other modules on the page.</span></span> <span data-ttu-id="3501f-110">Bir özellik modülü, bir satıcıdan pazarlamak veya bir şeyi yükseltmek veya bir şeyin (örneğin, ürünler, Satışlar veya Özellikler) olmasını istediği herhangi bir site sayfasına yerleştirilebilir.</span><span class="sxs-lookup"><span data-stu-id="3501f-110">A feature module can be put on any site page where a retailer wants to market or promote something (for example products, sales, or features).</span></span>

## <a name="examples-of-feature-modules-in-e-commerce"></a><span data-ttu-id="3501f-111">E-ticarette özellik modülleri örnekleri</span><span class="sxs-lookup"><span data-stu-id="3501f-111">Examples of feature modules in e-Commerce</span></span>

<span data-ttu-id="3501f-112">Bir özellik modülü aşağıdaki sayfalarda kullanılabilir:</span><span class="sxs-lookup"><span data-stu-id="3501f-112">A feature module can used on the following pages:</span></span>

- <span data-ttu-id="3501f-113">Ürün özelliklerini göstermek için ürün ayrıntıları sayfası</span><span class="sxs-lookup"><span data-stu-id="3501f-113">A product details page, to showcase product features</span></span>
- <span data-ttu-id="3501f-114">Ürünleri yükseltmek için giriş sayfası</span><span class="sxs-lookup"><span data-stu-id="3501f-114">The home page, to promote products</span></span>
- <span data-ttu-id="3501f-115">Bir ürün kategorisini vurgulamak için kategori sayfası</span><span class="sxs-lookup"><span data-stu-id="3501f-115">A category page, to highlight a category of products</span></span>

## <a name="feature-module-properties"></a><span data-ttu-id="3501f-116">Özellik modülü özellikleri</span><span class="sxs-lookup"><span data-stu-id="3501f-116">Feature module properties</span></span>

| <span data-ttu-id="3501f-117">Özellik adı</span><span class="sxs-lookup"><span data-stu-id="3501f-117">Property name</span></span>     | <span data-ttu-id="3501f-118">Değerler</span><span class="sxs-lookup"><span data-stu-id="3501f-118">Values</span></span> | <span data-ttu-id="3501f-119">Tanım</span><span class="sxs-lookup"><span data-stu-id="3501f-119">Description</span></span> |
|-------------------|--------|-------------|
| <span data-ttu-id="3501f-120">Görüntü</span><span class="sxs-lookup"><span data-stu-id="3501f-120">Image</span></span>             | <span data-ttu-id="3501f-121">Resim dosyası</span><span class="sxs-lookup"><span data-stu-id="3501f-121">Image file</span></span> | <span data-ttu-id="3501f-122">Bir görüntü, bir ürünü veya promosyonu pazarlamada kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="3501f-122">An image can be used to market the product or promotion.</span></span> <span data-ttu-id="3501f-123">Görüntü Galerisine bir resim yüklenebilir veya varolan bir görüntü kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="3501f-123">An image can be uploaded to the image gallery, or an existing image can be used.</span></span> |
| <span data-ttu-id="3501f-124">Başlık</span><span class="sxs-lookup"><span data-stu-id="3501f-124">Heading</span></span>           | <span data-ttu-id="3501f-125">Başlık metni ve başlık etiketi (**H1**, **H2**, **H3**, **H4**, **H5** veya **H6**)</span><span class="sxs-lookup"><span data-stu-id="3501f-125">Heading text and heading tag (**H1**, **H2**, **H3**, **H4**, **H5**, or **H6**)</span></span> | <span data-ttu-id="3501f-126">Tüm özellik modülü bir başlığa sahip olabilir.</span><span class="sxs-lookup"><span data-stu-id="3501f-126">Every feature module can have a heading.</span></span> <span data-ttu-id="3501f-127">Varsayılan olarak, başlık için **H2** başlık etiketi kullanılır.</span><span class="sxs-lookup"><span data-stu-id="3501f-127">By default, the **H2** heading tag is used for the heading.</span></span> <span data-ttu-id="3501f-128">Ancak, bu etiket erişilebilirlik gereksinimlerini karşılayacak şekilde değiştirilebilir.</span><span class="sxs-lookup"><span data-stu-id="3501f-128">However, the tag can be changed to meet accessibility requirements.</span></span> |
| <span data-ttu-id="3501f-129">Paragraf</span><span class="sxs-lookup"><span data-stu-id="3501f-129">Paragraph</span></span>         | <span data-ttu-id="3501f-130">Paragraf metni</span><span class="sxs-lookup"><span data-stu-id="3501f-130">Paragraph text</span></span> | <span data-ttu-id="3501f-131">Özellik modülleri zengin metin biçimindeki paragraf metnini destekler.</span><span class="sxs-lookup"><span data-stu-id="3501f-131">Feature modules support paragraph text in rich text format.</span></span> <span data-ttu-id="3501f-132">Kalın, altı çizili, italik metin ve köprüler gibi bazı temel zengin metin özellikleri desteklenir.</span><span class="sxs-lookup"><span data-stu-id="3501f-132">Some basic rich text capabilities are supported, such as bold, underlined, and italic text, and hyperlinks.</span></span> <span data-ttu-id="3501f-133">Bu yeteneklerden bazıları, modüle uygulanan sayfa teması tarafından geçersiz kılınabilir.</span><span class="sxs-lookup"><span data-stu-id="3501f-133">Some of these capabilities can be overridden by the page theme that is applied to the module.</span></span> |
| <span data-ttu-id="3501f-134">Bağla</span><span class="sxs-lookup"><span data-stu-id="3501f-134">Link</span></span>              | <span data-ttu-id="3501f-135">Bağlantı metni, bağlantı URL'si, erişilebilir zengin internet uygulamaları (ARIA) etiketi ve **bağlantıyı yeni sekmede aç**</span><span class="sxs-lookup"><span data-stu-id="3501f-135">Link text, link URL, Accessible Rich Internet Applications (ARIA) label, and **Open link in new tab**</span></span> | <span data-ttu-id="3501f-136">Özellik modülü bir veya daha fazla "eyleme çağrı" bağlantıları destekler.</span><span class="sxs-lookup"><span data-stu-id="3501f-136">Feature modules support one or more "call to action" links.</span></span> <span data-ttu-id="3501f-137">Bir bağlantı eklenirse, bağlantı metni, bir URL ve bir ARIA etiketi gereklidir.</span><span class="sxs-lookup"><span data-stu-id="3501f-137">If a link is added, link text, a URL, and an ARIA label are required.</span></span> <span data-ttu-id="3501f-138">ARIA etiketleri erişilebilirlik gereksinimlerini karşılayacak şekilde açıklayıcı olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="3501f-138">ARIA labels should be descriptive to meet accessibility requirements.</span></span> <span data-ttu-id="3501f-139">Bağlantılar yeni bir sekmede açılacak şekilde konfigüre edilebilir.</span><span class="sxs-lookup"><span data-stu-id="3501f-139">Links can be configured so that they are opened on a new tab.</span></span> |
| <span data-ttu-id="3501f-140">Görüntü yerleştirme</span><span class="sxs-lookup"><span data-stu-id="3501f-140">Image placement</span></span>   | <span data-ttu-id="3501f-141">**Sağ**, **Sol**, **Üst** veya **Alt**</span><span class="sxs-lookup"><span data-stu-id="3501f-141">**Right**, **Left**, **Top**, or **Bottom**</span></span> | <span data-ttu-id="3501f-142">Bu özellik resmin metne göre konumunu tanımlar.</span><span class="sxs-lookup"><span data-stu-id="3501f-142">This property defines the position of the image relative to the text.</span></span> <span data-ttu-id="3501f-143">Örneğin, **Sağ** seçilirse görüntü metnin sağında görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="3501f-143">For example, if **Right** is selected, the image appears to the right of the text.</span></span> |
| <span data-ttu-id="3501f-144">Görüntü sütunu boyutu</span><span class="sxs-lookup"><span data-stu-id="3501f-144">Image column size</span></span> | <span data-ttu-id="3501f-145">**1** ile **12** arasında bir değer</span><span class="sxs-lookup"><span data-stu-id="3501f-145">A value from **1** through **12**</span></span> | <span data-ttu-id="3501f-146">Bu özellik resmin metne göre boyutunu tanımlar.</span><span class="sxs-lookup"><span data-stu-id="3501f-146">This property defines the size of the image relative to the text.</span></span> <span data-ttu-id="3501f-147">Boyut, sayfada bir dizi sütun olarak ifade edilir.</span><span class="sxs-lookup"><span data-stu-id="3501f-147">Size is expressed as a number of columns on the page.</span></span> <span data-ttu-id="3501f-148">Sayfada 12 sütun vardır.</span><span class="sxs-lookup"><span data-stu-id="3501f-148">There are 12 columns on a page.</span></span> <span data-ttu-id="3501f-149">Varsayılan olarak resmin ve metnin boyutu aynı (her biri altı sütun) olacaktır.</span><span class="sxs-lookup"><span data-stu-id="3501f-149">By default, the image and text have equal size (six columns each).</span></span> <span data-ttu-id="3501f-150">Ancak, boyut gerektiği gibi ayarlanabilir.</span><span class="sxs-lookup"><span data-stu-id="3501f-150">However, the size can be adjusted as required.</span></span> |

## <a name="add-a-feature-module-to-a-new-page"></a><span data-ttu-id="3501f-151">Yeni sayfaya özellik modülü ekleme</span><span class="sxs-lookup"><span data-stu-id="3501f-151">Add a feature module to a new page</span></span> 

<span data-ttu-id="3501f-152">Bir yeni sayfaya özellik modülü eklemek ve gerekli özellikleri ayarlamak için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="3501f-152">To add a feature module to a new page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="3501f-153">**Şablonlara** gidin ve **özellik şablonu** adlı bir sayfa şablonu oluşturun.</span><span class="sxs-lookup"><span data-stu-id="3501f-153">Go to **Templates**, and create a page template that is named **feature template**.</span></span>
1. <span data-ttu-id="3501f-154">Varsayılan sayfanın **ana** yuvasına bir özellik modülü ekleyin.</span><span class="sxs-lookup"><span data-stu-id="3501f-154">In the **Main** slot of the default page, add a feature module.</span></span>
1. <span data-ttu-id="3501f-155">Şablonu giriş yapın ve yayımlayın.</span><span class="sxs-lookup"><span data-stu-id="3501f-155">Check in the template, and publish it.</span></span>
1. <span data-ttu-id="3501f-156">**Özellik sayfası** adlı bir sayfa oluşturmak için yeni oluşturduğunuz özellik şablonunu kullanın.</span><span class="sxs-lookup"><span data-stu-id="3501f-156">Use the feature template that you just created to create a page that is named **feature page**.</span></span>
1. <span data-ttu-id="3501f-157">Varsayılan sayfada **ana** yuvayı seçin, üç nokta düğmesini (**...**) ve sonra **Modül ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="3501f-157">In the **Main** slot of the default page, select the ellipsis button (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="3501f-158">**Modül Ekle** iletişim kutusunda **modüller'i seçin**, özellik modülünü seçin ve **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="3501f-158">In the **Add Module** dialog box, under **Select Modules**, select a feature module, and then select **OK**.</span></span>
1. <span data-ttu-id="3501f-159">Soldaki anahat ağacında, özellik modülünü seçin.</span><span class="sxs-lookup"><span data-stu-id="3501f-159">In the outline tree on the left, select the feature module.</span></span>
1. <span data-ttu-id="3501f-160">Sağdaki özellikler bölmesinde, **Resim Ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="3501f-160">In the properties pane on the right, select **Add an image**.</span></span> <span data-ttu-id="3501f-161">Sonra da varolan bir görüntüyü seçin veya yeni bir görüntü yükleyin.</span><span class="sxs-lookup"><span data-stu-id="3501f-161">Then either select an existing image or upload a new image.</span></span>
1. <span data-ttu-id="3501f-162">**Başlık** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="3501f-162">Select **Heading**.</span></span>
1. <span data-ttu-id="3501f-163">**Başlık** iletişim kutusunda başlık metnini ekleyin, başlık düzeyini seçin ve **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="3501f-163">In the **Heading** dialog box, add the heading text, select the heading level, and then select **OK**.</span></span>
1. <span data-ttu-id="3501f-164">**Zengin metin**altında, istediğiniz metni ekleyin.</span><span class="sxs-lookup"><span data-stu-id="3501f-164">Under **Rich Text**, add text as you require.</span></span>
1. <span data-ttu-id="3501f-165">**Eylem bağlantısı ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="3501f-165">Select **Add Action Link**.</span></span>
1. <span data-ttu-id="3501f-166">**Eylem bağlantısı** iletişim kutusunda bağlantı metni, bağlantı URL 'si ve bağlantı için bir Aria etiketi ekleyin ve **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="3501f-166">In the **Action Link** dialog box, add link text, a link URL, and an ARIA label for the link, and then select **OK**.</span></span>
1. <span data-ttu-id="3501f-167">Sayfayı kaydedin ve değişikliklerinizi önizleyin.</span><span class="sxs-lookup"><span data-stu-id="3501f-167">Save the page, and preview your changes.</span></span>
1. <span data-ttu-id="3501f-168">Sayfayı giriş yapın ve yayımlayın.</span><span class="sxs-lookup"><span data-stu-id="3501f-168">Check in the page, and publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="3501f-169">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="3501f-169">Additional resources</span></span>

[<span data-ttu-id="3501f-170">Başlangıç paketine genel bakış</span><span class="sxs-lookup"><span data-stu-id="3501f-170">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="3501f-171">Uyarı modülü</span><span class="sxs-lookup"><span data-stu-id="3501f-171">Alert module</span></span>](add-alert.md)

[<span data-ttu-id="3501f-172">Döngü modülü</span><span class="sxs-lookup"><span data-stu-id="3501f-172">Carousel module</span></span>](add-carousel.md)

[<span data-ttu-id="3501f-173">İçerik zengin blok modülü</span><span class="sxs-lookup"><span data-stu-id="3501f-173">Content rich block module</span></span>](add-content-rich-block.md)

[<span data-ttu-id="3501f-174">İçerik yerleşimi modülü</span><span class="sxs-lookup"><span data-stu-id="3501f-174">Content placement module</span></span>](add-content-placement-modules.md)

[<span data-ttu-id="3501f-175">Hero modülü</span><span class="sxs-lookup"><span data-stu-id="3501f-175">Hero module</span></span>](add-hero-module.md)

[<span data-ttu-id="3501f-176">Video oynatıcı modülü</span><span class="sxs-lookup"><span data-stu-id="3501f-176">Video player module</span></span>](add-video-player.md)
