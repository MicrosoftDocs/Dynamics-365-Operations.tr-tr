---
title: İçerik blok modülü
description: Bu konu içerik blok modüllerini kapsamaktadır ve Microsoft Dynamics 365 Commerce'un site sayfalarına nasıl ekleneceğini açıklamaktadır.
author: anupamar-ms
manager: annbe
ms.date: 09/15/2020
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
ms.openlocfilehash: 7a8b1c214ba31b7c47cecbe67bef493f5fa450fc
ms.sourcegitcommit: 8028fbc5b9585e87d3331ea02577ff82ede090af
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/16/2020
ms.locfileid: "3817366"
---
# <a name="content-block-module"></a><span data-ttu-id="156e1-103">İçerik blok modülü</span><span class="sxs-lookup"><span data-stu-id="156e1-103">Content block module</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="156e1-104">Bu konu içerik blok modüllerini kapsamaktadır ve Microsoft Dynamics 365 Commerce'un site sayfalarına nasıl ekleneceğini açıklamaktadır.</span><span class="sxs-lookup"><span data-stu-id="156e1-104">This topic covers content block modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="156e1-105">Genel Bakış</span><span class="sxs-lookup"><span data-stu-id="156e1-105">Overview</span></span>

<span data-ttu-id="156e1-106">Bir içerik bloku modülü, ürünleri veya promosyonları bir görüntü ve metin birleşimiyle pazarlamak için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="156e1-106">A content block module is used to market products or promotions through a combination of images and text.</span></span> <span data-ttu-id="156e1-107">Örneğin, bir satıcı yeni bir ürünü yükseltmek ve müşterilerin dikkatini çekmek için bir e-ticaret sitesinin giriş sayfasına içerik bloku modülü ekleyebilir.</span><span class="sxs-lookup"><span data-stu-id="156e1-107">For example, a retailer can add a content block module to the home page of an e-Commerce site to promote a new product and attract the attention of customers.</span></span>

<span data-ttu-id="156e1-108">İçerik bloku modülü içerik yönetimi sistemindeki (CMS) veriler tarafından yönlendiriliyor.</span><span class="sxs-lookup"><span data-stu-id="156e1-108">A content block module is driven by data from the content management system (CMS).</span></span> <span data-ttu-id="156e1-109">Bunlar sayfadaki diğer modüllere bağımlı olmayan bağımsız modüllerdir.</span><span class="sxs-lookup"><span data-stu-id="156e1-109">It's a stand-alone module that doesn't depend on any other modules on the page.</span></span> <span data-ttu-id="156e1-110">Bir içerik bloku modülü, bir satıcıdan pazarlamak veya bir şeyi yükseltmek veya bir şeyin (örneğin, ürünler, Satışlar veya Özellikler) olmasını istediği herhangi bir site sayfasına yerleştirilebilir.</span><span class="sxs-lookup"><span data-stu-id="156e1-110">A content block module can be put on any site page where a retailer wants to market or promote something (for example, products, sales, or features).</span></span>

## <a name="examples-of-content-block-module-in-e-commerce"></a><span data-ttu-id="156e1-111">E-ticarette içerik bloku modülü örnekleri</span><span class="sxs-lookup"><span data-stu-id="156e1-111">Examples of content block module in e-Commerce</span></span>

- <span data-ttu-id="156e1-112">Bir içerik bloku modülü, promosyonlar ve yeni ürünleri vurgulamak için e-ticaret sitesinin giriş sayfasında kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="156e1-112">A content block module can be used on the home page of an e-Commerce site to highlight promotions and new products.</span></span>
- <span data-ttu-id="156e1-113">Bir içerik bloku modülü ürün bilgilerini sergilebilecek bir ürün ayrıntıları sayfasında kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="156e1-113">A content block module can be used on a product details page to showcase product information.</span></span>
- <span data-ttu-id="156e1-114">Çoklu ürünleri veya promosyonları vurgulamak için bir döngü modülü birden fazla içerik bloku modül içinde yer alabilir.</span><span class="sxs-lookup"><span data-stu-id="156e1-114">Multiple content block modules can be put inside a carousel module to highlight multiple products or promotions.</span></span>

## <a name="content-block-modules-and-themes"></a><span data-ttu-id="156e1-115">İçerik bloğu modülleri ve temaları</span><span class="sxs-lookup"><span data-stu-id="156e1-115">Content block modules and themes</span></span>

<span data-ttu-id="156e1-116">İçerik bloğu modülleri, bir temaya dayalı olarak çeşitli düzen ve stilleri destekleyebilir.</span><span class="sxs-lookup"><span data-stu-id="156e1-116">Content block modules can support various layouts and styles based on a theme.</span></span> <span data-ttu-id="156e1-117">Örneğin, Fabrikam teması bir içerik bloğu modülünün üç düzen çeşitlemelerini destekler: Hero, özellik ve döşeme.</span><span class="sxs-lookup"><span data-stu-id="156e1-117">For example, the Fabrikam theme supports three layout variations of a content block module: hero, feature, and tile.</span></span> <span data-ttu-id="156e1-118">Hero düzeni arka planda metin kaplaması olan bir resim gösterir.</span><span class="sxs-lookup"><span data-stu-id="156e1-118">The hero layout shows an image on the background with text overlay.</span></span> <span data-ttu-id="156e1-119">Özellik mizanpajı bir resmi ve bir metni yan yana gösterir.</span><span class="sxs-lookup"><span data-stu-id="156e1-119">The feature layout shows an image and text side by side.</span></span> <span data-ttu-id="156e1-120">Kutucuk düzeni, kutucuk biçiminde birden çok içerik bloklarına izin verir.</span><span class="sxs-lookup"><span data-stu-id="156e1-120">The tile layout allows multiple content blocks in a tile format.</span></span>

<span data-ttu-id="156e1-121">Ek olarak, tema her düzen için farklı özellikler sergileyebilir.</span><span class="sxs-lookup"><span data-stu-id="156e1-121">In addition, the theme can expose different properties for each layout.</span></span> <span data-ttu-id="156e1-122">Bir tema geliştiricisi, içerik bloğu modülünü kullanarak daha fazla stil ile daha fazla düzen oluşturabilir.</span><span class="sxs-lookup"><span data-stu-id="156e1-122">A theme developer can build more layouts with more styles using the content block module.</span></span>

<span data-ttu-id="156e1-123">Aşağıdaki resimde, Hero düzenine sahip bir içerik bloğu modülü örneği gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="156e1-123">The following image shows an example of a content block module with a hero layout.</span></span>

![Hero modülü örneği](./media/Hero.PNG)

<span data-ttu-id="156e1-125">Aşağıdaki resimde, özellik düzenine sahip bir içerik bloğu modülü örneği gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="156e1-125">The following image shows an example of a content block module with a feature layout.</span></span>

![Özellik modülleri örnekleri](./media/Feature.PNG)

## <a name="content-block-module-properties"></a><span data-ttu-id="156e1-127">İçerik blok modülü özellikleri</span><span class="sxs-lookup"><span data-stu-id="156e1-127">Content block module properties</span></span>

| <span data-ttu-id="156e1-128">Özellik adı</span><span class="sxs-lookup"><span data-stu-id="156e1-128">Property name</span></span>  | <span data-ttu-id="156e1-129">Değerler</span><span class="sxs-lookup"><span data-stu-id="156e1-129">Values</span></span> | <span data-ttu-id="156e1-130">Tanım</span><span class="sxs-lookup"><span data-stu-id="156e1-130">Description</span></span> |
|----------------|--------|-------------|
| <span data-ttu-id="156e1-131">Görüntü</span><span class="sxs-lookup"><span data-stu-id="156e1-131">Image</span></span>          | <span data-ttu-id="156e1-132">Resim dosyası</span><span class="sxs-lookup"><span data-stu-id="156e1-132">Image file</span></span> | <span data-ttu-id="156e1-133">Bir görüntü, bir ürünü veya promosyonu sergilemede kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="156e1-133">An image can be used to showcase a product or a promotion.</span></span> <span data-ttu-id="156e1-134">Görüntü Galerisine bir resim yüklenebilir veya varolan bir görüntü kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="156e1-134">An image can be uploaded to the image gallery, or an existing image can be used.</span></span> |
| <span data-ttu-id="156e1-135">Başlık</span><span class="sxs-lookup"><span data-stu-id="156e1-135">Heading</span></span>        | <span data-ttu-id="156e1-136">Başlık metni ve başlık etiketi (**H1**, **H2**, **H3**, **H4**, **H5** veya **H6**)</span><span class="sxs-lookup"><span data-stu-id="156e1-136">Heading text and heading tag (**H1**, **H2**, **H3**, **H4**, **H5**, or **H6**)</span></span> | <span data-ttu-id="156e1-137">Tüm Hero modülü bir başlığa sahip olabilir.</span><span class="sxs-lookup"><span data-stu-id="156e1-137">Every hero module can have a heading.</span></span> <span data-ttu-id="156e1-138">Varsayılan olarak, başlık için **H2** başlık etiketi kullanılır.</span><span class="sxs-lookup"><span data-stu-id="156e1-138">By default, the **H2** heading tag is used for the heading.</span></span> <span data-ttu-id="156e1-139">Ancak, bu etiket erişilebilirlik gereksinimlerini karşılayacak şekilde değiştirilebilir.</span><span class="sxs-lookup"><span data-stu-id="156e1-139">However, the tag can be changed to meet accessibility requirements.</span></span> |
| <span data-ttu-id="156e1-140">Paragraf</span><span class="sxs-lookup"><span data-stu-id="156e1-140">Paragraph</span></span>      | <span data-ttu-id="156e1-141">Paragraf metni</span><span class="sxs-lookup"><span data-stu-id="156e1-141">Paragraph text</span></span> | <span data-ttu-id="156e1-142">Hero modülleri zengin metin biçimindeki paragraf metnini destekler.</span><span class="sxs-lookup"><span data-stu-id="156e1-142">Hero modules support paragraph text in rich text format.</span></span> <span data-ttu-id="156e1-143">Kalın, altı çizili, italik metin ve köprüler gibi bazı temel zengin metin özellikleri desteklenir.</span><span class="sxs-lookup"><span data-stu-id="156e1-143">Some basic rich text capabilities are supported, such as bold, underlined, and italic text, and hyperlinks.</span></span> <span data-ttu-id="156e1-144">Bu yeteneklerden bazıları, modüle uygulanan sayfa teması tarafından geçersiz kılınabilir.</span><span class="sxs-lookup"><span data-stu-id="156e1-144">Some of these capabilities can be overridden by the page theme that is applied to the module.</span></span> |
| <span data-ttu-id="156e1-145">Bağla</span><span class="sxs-lookup"><span data-stu-id="156e1-145">Link</span></span>           | <span data-ttu-id="156e1-146">Bağlantı metni, bağlantı URL'si, erişilebilir zengin internet uygulamaları (ARIA) etiketi ve **bağlantıyı yeni sekmede aç**</span><span class="sxs-lookup"><span data-stu-id="156e1-146">Link text, link URL, Accessible Rich Internet Applications (ARIA) label, and **Open link in new tab**</span></span> | <span data-ttu-id="156e1-147">Hero modülü bir veya daha fazla "eyleme çağrı" bağlantıları destekler.</span><span class="sxs-lookup"><span data-stu-id="156e1-147">Hero modules support one or more "call to action" links.</span></span> <span data-ttu-id="156e1-148">Bir bağlantı eklenirse, bağlantı metni, bir URL ve bir ARIA etiketi gereklidir.</span><span class="sxs-lookup"><span data-stu-id="156e1-148">If a link is added, link text, a URL, and an ARIA label are required.</span></span> <span data-ttu-id="156e1-149">ARIA etiketleri erişilebilirlik gereksinimlerini karşılayacak şekilde açıklayıcı olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="156e1-149">ARIA labels should be descriptive to meet accessibility requirements.</span></span> <span data-ttu-id="156e1-150">Bağlantılar yeni bir sekmede açılacak şekilde konfigüre edilebilir.</span><span class="sxs-lookup"><span data-stu-id="156e1-150">Links can be configured so that they are opened on a new tab.</span></span> |

## <a name="content-block-module-properties-exposed-by-the-fabrikam-theme"></a><span data-ttu-id="156e1-151">Fabrikam teması tarafından gösterilen içerik bloğu modülü özellikleri</span><span class="sxs-lookup"><span data-stu-id="156e1-151">Content block module properties exposed by the Fabrikam theme</span></span> 

| <span data-ttu-id="156e1-152">Özellik adı</span><span class="sxs-lookup"><span data-stu-id="156e1-152">Property name</span></span>  | <span data-ttu-id="156e1-153">Değerler</span><span class="sxs-lookup"><span data-stu-id="156e1-153">Values</span></span> | <span data-ttu-id="156e1-154">Tanım</span><span class="sxs-lookup"><span data-stu-id="156e1-154">Description</span></span> |
|----------------|--------|-------------|
| <span data-ttu-id="156e1-155">Metin yerleştirme</span><span class="sxs-lookup"><span data-stu-id="156e1-155">Text placement</span></span> | <span data-ttu-id="156e1-156">**Sol**, **Sağ**, **Orta**</span><span class="sxs-lookup"><span data-stu-id="156e1-156">**Left**, **Right**, **Center**</span></span> | <span data-ttu-id="156e1-157">Bu özellik, resmin üzerinde metnin konumunu belirler.</span><span class="sxs-lookup"><span data-stu-id="156e1-157">This property defines the position of the text on the image.</span></span> <span data-ttu-id="156e1-158">Yalnızca hero düzenine uygulanır.</span><span class="sxs-lookup"><span data-stu-id="156e1-158">It only applies to the hero layout.</span></span> |
| <span data-ttu-id="156e1-159">Metin teması</span><span class="sxs-lookup"><span data-stu-id="156e1-159">Text theme</span></span>     | <span data-ttu-id="156e1-160">**Açık** veya **Koyu**</span><span class="sxs-lookup"><span data-stu-id="156e1-160">**Light** or **Dark**</span></span> | <span data-ttu-id="156e1-161">Arka plan resmine dayalı olarak metin için bir renk düzeni tanımlanabilir.</span><span class="sxs-lookup"><span data-stu-id="156e1-161">A color scheme can be defined for the text, based on the background image.</span></span> <span data-ttu-id="156e1-162">Örneğin, görüntüde koyu renkli bir arka plan varsa, metin görünür hale getirmek ve erişilebilirlik amacıyla renk karşıtlığı oranlarını karşılamak için açık bir tema uygulanabilir.</span><span class="sxs-lookup"><span data-stu-id="156e1-162">For example, if the image has a dark background, a light theme can be applied to make the text more visible and to meet color contrast ratios for accessibility purposes.</span></span> <span data-ttu-id="156e1-163">Yalnızca hero düzenine uygulanır.</span><span class="sxs-lookup"><span data-stu-id="156e1-163">It only applies to the hero layout.</span></span>|
| <span data-ttu-id="156e1-164">Görüntü yerleştirme</span><span class="sxs-lookup"><span data-stu-id="156e1-164">Image placement</span></span>       | <span data-ttu-id="156e1-165">**Sol**,  **Sağ**</span><span class="sxs-lookup"><span data-stu-id="156e1-165">**Left**,  **Right**</span></span> | <span data-ttu-id="156e1-166">Bu özellik, resmin metnin solunda mı yoksa sağda mı olması gerektiğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="156e1-166">This property specifies if the image should be to the left or right of the text.</span></span> <span data-ttu-id="156e1-167">Yalnızca özellik düzenine uygulanır.</span><span class="sxs-lookup"><span data-stu-id="156e1-167">It only applies to the feature layout.</span></span>  |

## <a name="add-a-content-block-module-to-a-new-page"></a><span data-ttu-id="156e1-168">Yeni bir sayfaya içerik blok modülü ekleme</span><span class="sxs-lookup"><span data-stu-id="156e1-168">Add a content block module to a new page</span></span>

<span data-ttu-id="156e1-169">Bir yeni sayfaya Hero modülü eklemek ve gerekli özellikleri ayarlamak için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="156e1-169">To add a hero module to a new page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="156e1-170">**Şablonlara** gidin ve **İçerik bloğu şablonu** adlı bir sayfa şablonu oluşturun.</span><span class="sxs-lookup"><span data-stu-id="156e1-170">Go to **Templates**, and create a page template that is named **Content block template**.</span></span>
1. <span data-ttu-id="156e1-171">Varsayılan sayfanın **ana** yuvasına bir Hero modülü ekleyin.</span><span class="sxs-lookup"><span data-stu-id="156e1-171">In the **Main** slot of the default page, add a hero module.</span></span>
1. <span data-ttu-id="156e1-172">**Kaydet**'i seçin, şablonu iade etmek için **Düzenlemeyi bitir**'i ve ardından yayımlamak için **Yayımla**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="156e1-172">Select **Save**, select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span>
1. <span data-ttu-id="156e1-173">**İçerik bloğu sayfası** adlı bir sayfa oluşturmak için yeni oluşturduğunuz hero şablonunu kullanın.</span><span class="sxs-lookup"><span data-stu-id="156e1-173">Use the hero template that you just created to create a page that is named **Content block page**.</span></span>
1. <span data-ttu-id="156e1-174">Varsayılan sayfada **ana** yuvayı seçin, üç nokta düğmesini (**...**) ve sonra **Modül ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="156e1-174">In the **Main** slot of the default page, select the ellipsis button (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="156e1-175">**Modül Ekle** iletişim kutusunda **modüller'i seçin**, Hero modülünü seçin ve **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="156e1-175">In the **Add Module** dialog box, under **Select Modules**, select the hero module, and then select **OK**.</span></span>
1. <span data-ttu-id="156e1-176">Soldaki anahat ağacında, içerik bloku modülünü seçin.</span><span class="sxs-lookup"><span data-stu-id="156e1-176">In the outline tree on the left, select the content block module.</span></span>
1. <span data-ttu-id="156e1-177">Sağdaki özellikler bölmesinde, **Resim Ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="156e1-177">In the properties pane on the right, select **Add an image**.</span></span> <span data-ttu-id="156e1-178">Sonra da varolan bir görüntüyü seçin veya yeni bir görüntü yükleyin.</span><span class="sxs-lookup"><span data-stu-id="156e1-178">Then either select an existing image or upload a new image.</span></span>
1. <span data-ttu-id="156e1-179">**Başlık** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="156e1-179">Select **Heading**.</span></span>
1. <span data-ttu-id="156e1-180">**Başlık** iletişim kutusunda başlık metnini ekleyin, başlık düzeyini seçin ve **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="156e1-180">In the **Heading** dialog box, add the heading text, select the heading level, and then select **OK**.</span></span>
1. <span data-ttu-id="156e1-181">**Zengin metin**altında, istediğiniz metni ekleyin.</span><span class="sxs-lookup"><span data-stu-id="156e1-181">Under **Rich Text**, add text as you require.</span></span>
1. <span data-ttu-id="156e1-182">**Bağlantı Ekle**'yi seç.</span><span class="sxs-lookup"><span data-stu-id="156e1-182">Select **Add Link**.</span></span>
1. <span data-ttu-id="156e1-183">**Bağlantı** iletişim kutusunda bağlantı metni, bağlantı URL 'si ve bağlantı için bir Aria etiketi ekleyin ve **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="156e1-183">In the **Link** dialog box, add link text, a link URL, and an ARIA label for the link, and then select **OK**.</span></span>
1. <span data-ttu-id="156e1-184">**Hero** düzenini seçin.</span><span class="sxs-lookup"><span data-stu-id="156e1-184">Select the **Hero** layout.</span></span>
1. <span data-ttu-id="156e1-185">**Kaydet**'i seçin ve ardından sayfayı önizlemek için **Önizleme**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="156e1-185">Select **Save**, and then select **Preview** to preview the page.</span></span>
1. <span data-ttu-id="156e1-186">Şablonu iade etmek için **Düzenlemeyi bitir**'i seçin, ardından yayımlamak için **Yayımla**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="156e1-186">Select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span> 

## <a name="additional-resources"></a><span data-ttu-id="156e1-187">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="156e1-187">Additional resources</span></span>

[<span data-ttu-id="156e1-188">Modül kitaplığına genel bakış</span><span class="sxs-lookup"><span data-stu-id="156e1-188">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="156e1-189">Promosyon başlığı modülü</span><span class="sxs-lookup"><span data-stu-id="156e1-189">Promo banner module</span></span>](add-alert.md)

[<span data-ttu-id="156e1-190">Döngü modülü</span><span class="sxs-lookup"><span data-stu-id="156e1-190">Carousel module</span></span>](add-carousel.md)

[<span data-ttu-id="156e1-191">Metin bloğu modülü</span><span class="sxs-lookup"><span data-stu-id="156e1-191">Text block module</span></span>](add-content-rich-block.md)

[<span data-ttu-id="156e1-192">Video oynatıcı modülü</span><span class="sxs-lookup"><span data-stu-id="156e1-192">Video player module</span></span>](add-video-player.md)
