---
title: Hero modülü
description: Bu konu hero modüllerini kapsamaktadır ve Microsoft Dynamics 365 Commerce'un site sayfalarına nasıl ekleneceğini açıklamaktadır.
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
ms.openlocfilehash: c43704992e9759e7207f1b1c9bc958449daa6d1d
ms.sourcegitcommit: 3a4e137ef3a96ba0a58c5352f4a3b57467ace9ae
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/11/2019
ms.locfileid: "2785410"
---
# <a name="hero-module"></a><span data-ttu-id="4078f-103">Hero modülü</span><span class="sxs-lookup"><span data-stu-id="4078f-103">Hero module</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="4078f-104">Bu konu hero modüllerini kapsamaktadır ve Microsoft Dynamics 365 Commerce'un site sayfalarına nasıl ekleneceğini açıklamaktadır.</span><span class="sxs-lookup"><span data-stu-id="4078f-104">This topic covers hero modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="4078f-105">Genel Bakış</span><span class="sxs-lookup"><span data-stu-id="4078f-105">Overview</span></span>

<span data-ttu-id="4078f-106">Hero modülü, ürünleri veya promosyonları bir görüntü ve metin birleşimiyle pazarlamak için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="4078f-106">A hero module is used to market products or promotions through a combination of images and text.</span></span> <span data-ttu-id="4078f-107">Örneğin, bir satıcı yeni bir ürünü yükseltmek ve müşterilerin dikkatini çekmek için bir e-ticaret sitesinin giriş sayfasına Hero modülü ekleyebilir.</span><span class="sxs-lookup"><span data-stu-id="4078f-107">For example, a retailer can add a hero module to the home page of an e-Commerce site to promote a new product and attract the attention of customers.</span></span>

<span data-ttu-id="4078f-108">Hero modülü içerik yönetimi sistemindeki (CMS) veriler tarafından yönlendiriliyor.</span><span class="sxs-lookup"><span data-stu-id="4078f-108">A hero module is driven by data from the content management system (CMS).</span></span> <span data-ttu-id="4078f-109">Bunlar sayfadaki diğer modüllere bağımlı olmayan bağımsız modüllerdir.</span><span class="sxs-lookup"><span data-stu-id="4078f-109">It's a stand-alone module that doesn't depend on any other modules on the page.</span></span> <span data-ttu-id="4078f-110">Bir Hero modülü, bir satıcıdan pazarlamak veya bir şeyi yükseltmek veya bir şeyin (örneğin, ürünler, Satışlar veya Özellikler) olmasını istediği herhangi bir site sayfasına yerleştirilebilir.</span><span class="sxs-lookup"><span data-stu-id="4078f-110">A hero module can be put on any site page where a retailer wants to market or promote something (for example, products, sales, or features).</span></span>

## <a name="examples-of-hero-module-in-e-commerce"></a><span data-ttu-id="4078f-111">E-ticarette Hero modülleri örnekleri</span><span class="sxs-lookup"><span data-stu-id="4078f-111">Examples of hero module in e-Commerce</span></span>

- <span data-ttu-id="4078f-112">Bir Hero modülü, promosyonlar ve yeni ürünleri vurgulamak için e-ticaret sitesinin giriş sayfasında kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="4078f-112">A hero module can be used on the home page of an e-Commerce site to highlight promotions and new products.</span></span>
- <span data-ttu-id="4078f-113">Hero modülü ürün bilgilerini sergilebilecek bir ürün ayrıntıları sayfasında kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="4078f-113">A hero module can be used on a product details page to showcase product information.</span></span>
- <span data-ttu-id="4078f-114">Çoklu ürünleri veya promosyonları vurgulamak için bir döngü modülü birden fazla Hero modül içinde yer alabilir.</span><span class="sxs-lookup"><span data-stu-id="4078f-114">Multiple hero modules can be put inside a carousel module to highlight multiple products or promotions.</span></span>

## <a name="hero-module-properties"></a><span data-ttu-id="4078f-115">Hero modülü özellikleri</span><span class="sxs-lookup"><span data-stu-id="4078f-115">Hero module properties</span></span>

| <span data-ttu-id="4078f-116">Özellik adı</span><span class="sxs-lookup"><span data-stu-id="4078f-116">Property name</span></span>  | <span data-ttu-id="4078f-117">Değerler</span><span class="sxs-lookup"><span data-stu-id="4078f-117">Values</span></span> | <span data-ttu-id="4078f-118">Tanım</span><span class="sxs-lookup"><span data-stu-id="4078f-118">Description</span></span> |
|----------------|--------|-------------|
| <span data-ttu-id="4078f-119">Görüntü</span><span class="sxs-lookup"><span data-stu-id="4078f-119">Image</span></span>          | <span data-ttu-id="4078f-120">Resim dosyası</span><span class="sxs-lookup"><span data-stu-id="4078f-120">Image file</span></span> | <span data-ttu-id="4078f-121">Bir görüntü, bir ürünü veya promosyonu sergilemede kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="4078f-121">An image can be used to showcase a product or a promotion.</span></span> <span data-ttu-id="4078f-122">Görüntü Galerisine bir resim yüklenebilir veya varolan bir görüntü kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="4078f-122">An image can be uploaded to the image gallery, or an existing image can be used.</span></span> |
| <span data-ttu-id="4078f-123">Başlık</span><span class="sxs-lookup"><span data-stu-id="4078f-123">Heading</span></span>        | <span data-ttu-id="4078f-124">Başlık metni ve başlık etiketi (**H1**, **H2**, **H3**, **H4**, **H5** veya **H6**)</span><span class="sxs-lookup"><span data-stu-id="4078f-124">Heading text and heading tag (**H1**, **H2**, **H3**, **H4**, **H5**, or **H6**)</span></span> | <span data-ttu-id="4078f-125">Tüm Hero modülü bir başlığa sahip olabilir.</span><span class="sxs-lookup"><span data-stu-id="4078f-125">Every hero module can have a heading.</span></span> <span data-ttu-id="4078f-126">Varsayılan olarak, başlık için **H2** başlık etiketi kullanılır.</span><span class="sxs-lookup"><span data-stu-id="4078f-126">By default, the **H2** heading tag is used for the heading.</span></span> <span data-ttu-id="4078f-127">Ancak, bu etiket erişilebilirlik gereksinimlerini karşılayacak şekilde değiştirilebilir.</span><span class="sxs-lookup"><span data-stu-id="4078f-127">However, the tag can be changed to meet accessibility requirements.</span></span> |
| <span data-ttu-id="4078f-128">Paragraf</span><span class="sxs-lookup"><span data-stu-id="4078f-128">Paragraph</span></span>      | <span data-ttu-id="4078f-129">Paragraf metni</span><span class="sxs-lookup"><span data-stu-id="4078f-129">Paragraph text</span></span> | <span data-ttu-id="4078f-130">Hero modülleri zengin metin biçimindeki paragraf metnini destekler.</span><span class="sxs-lookup"><span data-stu-id="4078f-130">Hero modules support paragraph text in rich text format.</span></span> <span data-ttu-id="4078f-131">Kalın, altı çizili, italik metin ve köprüler gibi bazı temel zengin metin özellikleri desteklenir.</span><span class="sxs-lookup"><span data-stu-id="4078f-131">Some basic rich text capabilities are supported, such as bold, underlined, and italic text, and hyperlinks.</span></span> <span data-ttu-id="4078f-132">Bu yeteneklerden bazıları, modüle uygulanan sayfa teması tarafından geçersiz kılınabilir.</span><span class="sxs-lookup"><span data-stu-id="4078f-132">Some of these capabilities can be overridden by the page theme that is applied to the module.</span></span> |
| <span data-ttu-id="4078f-133">Bağla</span><span class="sxs-lookup"><span data-stu-id="4078f-133">Link</span></span>           | <span data-ttu-id="4078f-134">Bağlantı metni, bağlantı URL'si, erişilebilir zengin internet uygulamaları (ARIA) etiketi ve **bağlantıyı yeni sekmede aç**</span><span class="sxs-lookup"><span data-stu-id="4078f-134">Link text, link URL, Accessible Rich Internet Applications (ARIA) label, and **Open link in new tab**</span></span> | <span data-ttu-id="4078f-135">Hero modülü bir veya daha fazla "eyleme çağrı" bağlantıları destekler.</span><span class="sxs-lookup"><span data-stu-id="4078f-135">Hero modules support one or more "call to action" links.</span></span> <span data-ttu-id="4078f-136">Bir bağlantı eklenirse, bağlantı metni, bir URL ve bir ARIA etiketi gereklidir.</span><span class="sxs-lookup"><span data-stu-id="4078f-136">If a link is added, link text, a URL, and an ARIA label are required.</span></span> <span data-ttu-id="4078f-137">ARIA etiketleri erişilebilirlik gereksinimlerini karşılayacak şekilde açıklayıcı olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="4078f-137">ARIA labels should be descriptive to meet accessibility requirements.</span></span> <span data-ttu-id="4078f-138">Bağlantılar yeni bir sekmede açılacak şekilde konfigüre edilebilir.</span><span class="sxs-lookup"><span data-stu-id="4078f-138">Links can be configured so that they are opened on a new tab.</span></span> |
| <span data-ttu-id="4078f-139">Metin yerleştirme</span><span class="sxs-lookup"><span data-stu-id="4078f-139">Text placement</span></span> | <span data-ttu-id="4078f-140">**Üst sola**, **üst sağa**, **üst orta**, **alt sola**, **alt sağa**, **alt orta**, **orta sola**, **Merkez sağa** veya **Merkez Merkezi**</span><span class="sxs-lookup"><span data-stu-id="4078f-140">**Top Left**, **Top Right**, **Top Center**, **Bottom Left**, **Bottom Right**, **Bottom Center**, **Center Left**, **Center Right**, or **Center Center**</span></span> | <span data-ttu-id="4078f-141">Bu özellik resmin metne göre konumunu tanımlar.</span><span class="sxs-lookup"><span data-stu-id="4078f-141">This property defines the position of the image relative to the text.</span></span> <span data-ttu-id="4078f-142">Örneğin, **Sağ** seçilirse görüntü metnin sağında görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="4078f-142">For example, if **Right** is selected, the image appears to the right of the text.</span></span> |
| <span data-ttu-id="4078f-143">Metin teması</span><span class="sxs-lookup"><span data-stu-id="4078f-143">Text theme</span></span>     | <span data-ttu-id="4078f-144">**Açık** veya **Koyu**</span><span class="sxs-lookup"><span data-stu-id="4078f-144">**Light** or **Dark**</span></span> | <span data-ttu-id="4078f-145">Arka plan resmine dayalı olarak metin için bir renk düzeni tanımlanabilir.</span><span class="sxs-lookup"><span data-stu-id="4078f-145">A color scheme can be defined for the text, based on the background image.</span></span> <span data-ttu-id="4078f-146">Örneğin, görüntüde koyu renkli bir arka plan varsa, metin görünür hale getirmek ve erişilebilirlik amacıyla renk karşıtlığı oranlarını karşılamak için açık bir tema uygulanabilir.</span><span class="sxs-lookup"><span data-stu-id="4078f-146">For example, if the image has a dark background, a light theme can be applied to make the text more visible and to meet color contrast ratios for accessibility purposes.</span></span> |
| <span data-ttu-id="4078f-147">Gradyan</span><span class="sxs-lookup"><span data-stu-id="4078f-147">Gradient</span></span>       | <span data-ttu-id="4078f-148">**Doğru** veya **yanlış**</span><span class="sxs-lookup"><span data-stu-id="4078f-148">**True** or **False**</span></span> | <span data-ttu-id="4078f-149">Bir gradyan, erişilebilirlik amacıyla renk karşıtlığı oranlarını karşılamak üzere görüntüye uygulanabilir.</span><span class="sxs-lookup"><span data-stu-id="4078f-149">A gradient can be applied to the image to meet color contrast ratios for accessibility purposes.</span></span> |

## <a name="add-a-hero-module-to-a-new-page"></a><span data-ttu-id="4078f-150">Yeni sayfaya Hero modülü ekleme</span><span class="sxs-lookup"><span data-stu-id="4078f-150">Add a hero module to a new page</span></span>

<span data-ttu-id="4078f-151">Bir yeni sayfaya Hero modülü eklemek ve gerekli özellikleri ayarlamak için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="4078f-151">To add a hero module to a new page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="4078f-152">**Şablonlara** gidin ve **Hero şablonu** adlı bir sayfa şablonu oluşturun.</span><span class="sxs-lookup"><span data-stu-id="4078f-152">Go to **Templates**, and create a page template that is named **hero template**.</span></span>
1. <span data-ttu-id="4078f-153">Varsayılan sayfanın **ana** yuvasına bir Hero modülü ekleyin.</span><span class="sxs-lookup"><span data-stu-id="4078f-153">In the **Main** slot of the default page, add a hero module.</span></span>
1. <span data-ttu-id="4078f-154">Şablonu giriş yapın ve yayımlayın.</span><span class="sxs-lookup"><span data-stu-id="4078f-154">Check in the template, and publish it.</span></span>
1. <span data-ttu-id="4078f-155">**Hero sayfası** adlı bir sayfa oluşturmak için yeni oluşturduğunuz hero şablonunu kullanın.</span><span class="sxs-lookup"><span data-stu-id="4078f-155">Use the hero template that you just created to create a page that is named **hero page**.</span></span>
1. <span data-ttu-id="4078f-156">Varsayılan sayfada **ana** yuvayı seçin, üç nokta düğmesini (**...**) ve sonra **Modül ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="4078f-156">In the **Main** slot of the default page, select the ellipsis button (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="4078f-157">**Modül Ekle** iletişim kutusunda **modüller'i seçin**, Hero modülünü seçin ve **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="4078f-157">In the **Add Module** dialog box, under **Select Modules**, select the hero module, and then select **OK**.</span></span>
1. <span data-ttu-id="4078f-158">Soldaki anahat ağacında, Hero modülünü seçin.</span><span class="sxs-lookup"><span data-stu-id="4078f-158">In the outline tree on the left, select the hero module.</span></span>
1. <span data-ttu-id="4078f-159">Sağdaki özellikler bölmesinde, **Resim Ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="4078f-159">In the properties pane on the right, select **Add an image**.</span></span> <span data-ttu-id="4078f-160">Sonra da varolan bir görüntüyü seçin veya yeni bir görüntü yükleyin.</span><span class="sxs-lookup"><span data-stu-id="4078f-160">Then either select an existing image or upload a new image.</span></span>
1. <span data-ttu-id="4078f-161">**Başlık** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="4078f-161">Select **Heading**.</span></span>
1. <span data-ttu-id="4078f-162">**Başlık** iletişim kutusunda başlık metnini ekleyin, başlık düzeyini seçin ve **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="4078f-162">In the **Heading** dialog box, add the heading text, select the heading level, and then select **OK**.</span></span>
1. <span data-ttu-id="4078f-163">**Zengin metin**altında, istediğiniz metni ekleyin.</span><span class="sxs-lookup"><span data-stu-id="4078f-163">Under **Rich Text**, add text as you require.</span></span>
1. <span data-ttu-id="4078f-164">**Eylem bağlantısı ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="4078f-164">Select **Add Action Link**.</span></span>
1. <span data-ttu-id="4078f-165">**Eylem bağlantısı** iletişim kutusunda bağlantı metni, bağlantı URL 'si ve bağlantı için bir Aria etiketi ekleyin ve **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="4078f-165">In the **Action Link** dialog box, add link text, a link URL, and an ARIA label for the link, and then select **OK**.</span></span>
1. <span data-ttu-id="4078f-166">Sayfayı kaydedin ve değişikliklerinizi önizleyin.</span><span class="sxs-lookup"><span data-stu-id="4078f-166">Save the page, and preview your changes.</span></span>
1. <span data-ttu-id="4078f-167">Sayfayı giriş yapın ve yayımlayın.</span><span class="sxs-lookup"><span data-stu-id="4078f-167">Check in the page, and publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="4078f-168">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="4078f-168">Additional resources</span></span>

[<span data-ttu-id="4078f-169">Başlangıç paketine genel bakış</span><span class="sxs-lookup"><span data-stu-id="4078f-169">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="4078f-170">Uyarı modülü</span><span class="sxs-lookup"><span data-stu-id="4078f-170">Alert module</span></span>](add-alert.md)

[<span data-ttu-id="4078f-171">Döngü modülü</span><span class="sxs-lookup"><span data-stu-id="4078f-171">Carousel module</span></span>](add-carousel.md)

[<span data-ttu-id="4078f-172">İçerik zengin blok modülü</span><span class="sxs-lookup"><span data-stu-id="4078f-172">Content rich block module</span></span>](add-content-rich-block.md)

[<span data-ttu-id="4078f-173">İçerik yerleştirme modülü</span><span class="sxs-lookup"><span data-stu-id="4078f-173">Content placement module</span></span>](add-content-placement-modules.md)

[<span data-ttu-id="4078f-174">Özellik modülü</span><span class="sxs-lookup"><span data-stu-id="4078f-174">Feature module</span></span>](add-feature-module.md)

[<span data-ttu-id="4078f-175">Video oynatıcı modülü</span><span class="sxs-lookup"><span data-stu-id="4078f-175">Video player module</span></span>](add-video-player.md)
