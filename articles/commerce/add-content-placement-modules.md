---
title: İçerik yerleştirme modülü
description: Bu konu içerik yerleştirme ve içerik yerleştirme öğesi modüllerini kapsamaktadır ve Microsoft Dynamics 365 Commerce'un site sayfalarına nasıl ekleneceğini açıklamaktadır.
author: anupamar-ms
manager: annbe
ms.date: 10/31/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 1b64e930628c969334ff6e643ba23b77445e6e4c
ms.sourcegitcommit: 3a4e137ef3a96ba0a58c5352f4a3b57467ace9ae
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/11/2019
ms.locfileid: "2785312"
---
# <a name="content-placement-module"></a><span data-ttu-id="2ae98-103">İçerik yerleştirme modülü</span><span class="sxs-lookup"><span data-stu-id="2ae98-103">Content placement module</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="2ae98-104">Bu konu içerik yerleştirme ve içerik yerleştirme öğesi modüllerini kapsamaktadır ve Microsoft Dynamics 365 Commerce'un site sayfalarına nasıl ekleneceğini açıklamaktadır.</span><span class="sxs-lookup"><span data-stu-id="2ae98-104">This topic covers content placement and content placement item modules, and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="2ae98-105">Genel Bakış</span><span class="sxs-lookup"><span data-stu-id="2ae98-105">Overview</span></span>

<span data-ttu-id="2ae98-106">İçerik yerleşim modülü, diğer modüllerin belirli bir düzene koyulacağı özel bir kapsayıcıdır.</span><span class="sxs-lookup"><span data-stu-id="2ae98-106">A content placement module is a special container that other modules can be put inside in a specific layout.</span></span> <span data-ttu-id="2ae98-107">İçerik yerleşim modülleri aşağıdaki modül türlerini alt modüller olarak destekler: içerik yerleşim öğesi, hesap karşılama öğesi, hesap sipariş maddesi, hesap istek listesi öğesi ve hesap profili öğesi.</span><span class="sxs-lookup"><span data-stu-id="2ae98-107">Content placement modules support the following types of modules as child modules: content placement item, account welcome item, account order item, account wish list item, and account profile item.</span></span>

<span data-ttu-id="2ae98-108">İçerik yerleşim modülleri, destekledikleri alt modülden veri türetin.</span><span class="sxs-lookup"><span data-stu-id="2ae98-108">Content placement modules derive data from the child modules that they support.</span></span> <span data-ttu-id="2ae98-109">Bu nedenle, içerik yerleşim modülleri, eklenen modüllere bağlı olarak çeşitli şekillerde kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="2ae98-109">Therefore, content placement modules can be used in various ways, depending on the modules that are added to it.</span></span>

<span data-ttu-id="2ae98-110">İçerik yerleşim öğesi modülleri, promosyonları, ilkeleri ve ürün özelliklerini sergilemek için hem görüntüleri hem de metni kullanır.</span><span class="sxs-lookup"><span data-stu-id="2ae98-110">Content placement item modules use both images and text to showcase promotions, policies, and product features.</span></span> <span data-ttu-id="2ae98-111">Örneğin, bir içerik yerleşim öğesi modülü, bir giriş sayfasında mağaza ilkelerini veya kargo bilgilerini göstermek için kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="2ae98-111">For example, a content placement item module can be used on a home page to show store policies or shipping information.</span></span> <span data-ttu-id="2ae98-112">İçerik yerleştirme öğesi modülleri, içerik yönetimi sistemindeki (CMS) veriler tarafından yönlendiriliyor ve herhangi bir sayfaya konabilir.</span><span class="sxs-lookup"><span data-stu-id="2ae98-112">Content placement item modules are driven by data from the content management system (CMS) and can be put on any page.</span></span> <span data-ttu-id="2ae98-113">Ancak, bunlar yalnızca bir içerik yerleşim modülü içinde kullanılabilirler.</span><span class="sxs-lookup"><span data-stu-id="2ae98-113">However, they can be used only inside a content placement module.</span></span>

## <a name="examples-of-content-placement-modules-in-e-commerce"></a><span data-ttu-id="2ae98-114">E-ticarette içerik yerleştirme modülleri örnekleri</span><span class="sxs-lookup"><span data-stu-id="2ae98-114">Examples of content placement modules in e-Commerce</span></span>

* <span data-ttu-id="2ae98-115">İçerik yerleştirme öğesi modülleri içeren içerik yerleşim modülleri, ürün özelliklerini, yükseltmeleri, mağaza ilkelerini, sevkiyat bilgilerini ve diğer bilgileri hem görüntü hem de metinden sergilebilecek bir giriş sayfasında veya pazarlama sayfalarında kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="2ae98-115">Content placement modules that contain content placement item modules can be used on a home page or marketing pages to showcase product features, promotions, store policies, shipping information, and other information through both images and text.</span></span>
* <span data-ttu-id="2ae98-116">İçerik yerleştirme öğesi modülleri içeren içerik yerleşim modülleri, ürün özelliklerini sergilebilecek ürün ayrıntıları sayfalarında kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="2ae98-116">Content placement modules that contain content placement item modules can be used on product details pages to showcase product features.</span></span>
* <span data-ttu-id="2ae98-117">Hesap karşılama öğesi veya hesap sipariş öğesi modülleri içeren içerik yerleşim modülleri Hesap Yönetimi sayfalarında kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="2ae98-117">Content placement modules that contain account welcome item or account order item modules can be used on account management pages.</span></span>

## <a name="content-placement-module-properties"></a><span data-ttu-id="2ae98-118">İçerik yerleştirme modülü özellikleri</span><span class="sxs-lookup"><span data-stu-id="2ae98-118">Content placement module properties</span></span>

| <span data-ttu-id="2ae98-119">Özellik adı</span><span class="sxs-lookup"><span data-stu-id="2ae98-119">Property name</span></span> | <span data-ttu-id="2ae98-120">Değer</span><span class="sxs-lookup"><span data-stu-id="2ae98-120">Value</span></span> | <span data-ttu-id="2ae98-121">Tanım</span><span class="sxs-lookup"><span data-stu-id="2ae98-121">Description</span></span> |
|---------------|-------|-------------|
| <span data-ttu-id="2ae98-122">Genişlik</span><span class="sxs-lookup"><span data-stu-id="2ae98-122">Width</span></span>         | <span data-ttu-id="2ae98-123">**Kapsayıcıya sığdır** veya **Ekrana doldur**</span><span class="sxs-lookup"><span data-stu-id="2ae98-123">**Fit container** or **Fill screen**</span></span> | <span data-ttu-id="2ae98-124">Değer **konteynere sığdır** şekilde ayarlandıysa, içerik yerleştirme modülü içindeki öğeler içerik yerleştirme modülü genişliğiyle sınırlandırılır.</span><span class="sxs-lookup"><span data-stu-id="2ae98-124">If the value is set to **Fit container**, the items inside the content placement module are restricted to the width of the content placement module.</span></span> <span data-ttu-id="2ae98-125">Değer, **ekranı doldur**'a ayarlanmışsa, öğeler içerik yerleştirme modülü genişliğiyle sınırlandırılmaz ancak tam ekran moduna geçebilir.</span><span class="sxs-lookup"><span data-stu-id="2ae98-125">If the value is set to **Fill screen**, the items aren't restricted to the width of the content placement module but can go into full-screen mode.</span></span> |

## <a name="content-placement-item-module-properties"></a><span data-ttu-id="2ae98-126">İçerik yerleştirme öğesi modülü özellikleri</span><span class="sxs-lookup"><span data-stu-id="2ae98-126">Content placement item module properties</span></span>

| <span data-ttu-id="2ae98-127">Özellik adı</span><span class="sxs-lookup"><span data-stu-id="2ae98-127">Property name</span></span> | <span data-ttu-id="2ae98-128">Değer</span><span class="sxs-lookup"><span data-stu-id="2ae98-128">Value</span></span> | <span data-ttu-id="2ae98-129">Tanım</span><span class="sxs-lookup"><span data-stu-id="2ae98-129">Description</span></span> |
|---------------|-------|-------------|
| <span data-ttu-id="2ae98-130">Başlık</span><span class="sxs-lookup"><span data-stu-id="2ae98-130">Heading</span></span>       | <span data-ttu-id="2ae98-131">Başlık metni ve başlık etiketleri (**H1**, **H2**, **H3**, **H4**, **H5** veya **H6**)</span><span class="sxs-lookup"><span data-stu-id="2ae98-131">Heading text and heading tags (**H1**, **H2**, **H3**, **H4**, **H5**, or **H6**)</span></span> | <span data-ttu-id="2ae98-132">Her içerik yerleşim öğesi modülünün bir başlığı olabilir.</span><span class="sxs-lookup"><span data-stu-id="2ae98-132">Every content placement item module can have a heading.</span></span> <span data-ttu-id="2ae98-133">**Başlık** özelliği Başlık etiketlerini destekler.</span><span class="sxs-lookup"><span data-stu-id="2ae98-133">The **Heading** property supports heading tags.</span></span> <span data-ttu-id="2ae98-134">Varsayılan olarak **H2** başlık etiketi kullanılır, ancak başlık etiketi erişilebilirlik gereksinimlerini karşılamak için değiştirilebilir.</span><span class="sxs-lookup"><span data-stu-id="2ae98-134">By default, the **H2** heading tag is used, but the heading tag can be changed to meet accessibility requirements.</span></span> |
| <span data-ttu-id="2ae98-135">Paragraf</span><span class="sxs-lookup"><span data-stu-id="2ae98-135">Paragraph</span></span>     | <span data-ttu-id="2ae98-136">Paragraf metni</span><span class="sxs-lookup"><span data-stu-id="2ae98-136">Paragraph text</span></span> | <span data-ttu-id="2ae98-137">İçerik yerleşim öğesi modülleri zengin metin biçimindeki paragraf metnini destekler.</span><span class="sxs-lookup"><span data-stu-id="2ae98-137">Content placement item modules support paragraph text in rich text format.</span></span> <span data-ttu-id="2ae98-138">Kalın, altı çizili, italik metin ve köprüler gibi bazı temel zengin metin özellikleri desteklenir.</span><span class="sxs-lookup"><span data-stu-id="2ae98-138">Some basic rich text capabilities are supported, such as bold, underlined, and italic text, and hyperlinks.</span></span> <span data-ttu-id="2ae98-139">Bu yeteneklerden bazıları, modüle uygulanan sayfa teması tarafından geçersiz kılınabilir.</span><span class="sxs-lookup"><span data-stu-id="2ae98-139">Some of these capabilities can be overridden by the page theme that is applied to the module.</span></span> |
| <span data-ttu-id="2ae98-140">Görüntü</span><span class="sxs-lookup"><span data-stu-id="2ae98-140">Image</span></span>         | <span data-ttu-id="2ae98-141">Resim dosyası</span><span class="sxs-lookup"><span data-stu-id="2ae98-141">Image file</span></span> | <span data-ttu-id="2ae98-142">Bir resim metinle ilişkilendirilebilir.</span><span class="sxs-lookup"><span data-stu-id="2ae98-142">An image can be associated with the text.</span></span> |
| <span data-ttu-id="2ae98-143">Bağla</span><span class="sxs-lookup"><span data-stu-id="2ae98-143">Link</span></span>          | <span data-ttu-id="2ae98-144">URL'ye bağlantı ve bağlantı metni</span><span class="sxs-lookup"><span data-stu-id="2ae98-144">Link URL and link text</span></span> | <span data-ttu-id="2ae98-145">Kullanıcıları belirli bir sayfaya yeniden yönlendirmek için metne bir bağlantı eklenebilir.</span><span class="sxs-lookup"><span data-stu-id="2ae98-145">A link can be added to the text to redirect users to a specific page.</span></span> |
| <span data-ttu-id="2ae98-146">Kutucuk boyutu</span><span class="sxs-lookup"><span data-stu-id="2ae98-146">Tile size</span></span>     | <span data-ttu-id="2ae98-147">**1** ile **12** arasında bir sayı</span><span class="sxs-lookup"><span data-stu-id="2ae98-147">A number from **1** through **12**</span></span> | <span data-ttu-id="2ae98-148">Her içerik yerleşim öğesi için bu özellik, öğenin içerik yerleşim modülüne doldurması gereken yuva sayısını tanımlar.</span><span class="sxs-lookup"><span data-stu-id="2ae98-148">For each content placement item, this property defines the number of slots that the item should fill in the content placement module.</span></span> <span data-ttu-id="2ae98-149">İçerik yerleşim modülünün en büyük boyutu 12 yuvadır.</span><span class="sxs-lookup"><span data-stu-id="2ae98-149">The maximum size of the content placement module is 12 slots.</span></span> <span data-ttu-id="2ae98-150">İçerik yerleştirme modülündeki ilk *n* öğe için toplam döşeme boyutu 12 yuvayı geçerse, öğeler bir sonraki satıra kaydırılır.</span><span class="sxs-lookup"><span data-stu-id="2ae98-150">If the total tile size for the first *n* items in the content placement module exceeds 12 slots, the items are wrapped to the next row.</span></span> |

## <a name="add-a-content-placement-module-that-contains-a-content-placement-item-module-to-a-page"></a><span data-ttu-id="2ae98-151">Sayfaya içerik yerleşim öğesi modülü içeren bir içerik yerleşim modülü ekler</span><span class="sxs-lookup"><span data-stu-id="2ae98-151">Add a content placement module that contains a content placement item module to a page</span></span>

<span data-ttu-id="2ae98-152">Yeni bir sayfaya içerik yerleşim öğesi modülü içeren bir içerik yerleşim modülü eklemek ve gerekli özellikleri ayarlamak için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="2ae98-152">To add a content placement module that contains a content placement item module to a new page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="2ae98-153">**İçerik yerleşim şablonu** adlı bir şablonu oluşturun.</span><span class="sxs-lookup"><span data-stu-id="2ae98-153">Create a template that is named **content placement template**.</span></span>
1. <span data-ttu-id="2ae98-154">Varsayılan sayfanın **ana** yuvasına bir içerik yerleşim modülü ekleyin.</span><span class="sxs-lookup"><span data-stu-id="2ae98-154">In the **Main** slot of the default page, add a content placement module.</span></span>
1. <span data-ttu-id="2ae98-155">İçerik yerleşim öğesi modülünü bir içerik yerleşim modülüne ekleyin.</span><span class="sxs-lookup"><span data-stu-id="2ae98-155">In the content placement module, add a content placement item module.</span></span>
1. <span data-ttu-id="2ae98-156">Şablonu giriş yapın ve yayımlayın.</span><span class="sxs-lookup"><span data-stu-id="2ae98-156">Check in the template, and publish it.</span></span>
1. <span data-ttu-id="2ae98-157">**İçerik yerleştirme sayfası** adlı bir sayfa oluşturmak için yeni oluşturduğunuz içerik yerleştirme şablonunu kullanın.</span><span class="sxs-lookup"><span data-stu-id="2ae98-157">Use the content placement template that you just created to create a page that is named **Content placement page**.</span></span>
1. <span data-ttu-id="2ae98-158">Yeni sayfanın **ana** yuvasına bir içerik yerleşim modülü ekleyin.</span><span class="sxs-lookup"><span data-stu-id="2ae98-158">In the **Main** slot of the new page, add a content placement module.</span></span>
1. <span data-ttu-id="2ae98-159">İçerik yerleşim öğesi modülünü bir içerik yerleşim modülüne ekleyin.</span><span class="sxs-lookup"><span data-stu-id="2ae98-159">In the content placement module, add a content placement item module.</span></span>
1. <span data-ttu-id="2ae98-160">İçerik yerleşim öğesi modülünün Özellik bölmesinde bir resim seçin, başlık ekleyin, paragraf ekleyin, bağlantı ekleyin, bağlantı URL'sini ayarlayın ve döşeme boyutunu **6** olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="2ae98-160">In the property pane for the content placement item module, select an image, add a heading, add a paragraph, add a link, set the link URL, and set the tile size to **6**.</span></span>
1. <span data-ttu-id="2ae98-161">Aynı döşeme boyutuna sahip başka bir içerik yerleşim öğesi modülü eklemek için 7. ve 8. adımlarını yineleyin.</span><span class="sxs-lookup"><span data-stu-id="2ae98-161">Repeat steps 7 and 8 to add another content placement item module that has the same tile size.</span></span>
1. <span data-ttu-id="2ae98-162">Sayfayı kaydet ve önizleyin.</span><span class="sxs-lookup"><span data-stu-id="2ae98-162">Save and preview the page.</span></span> <span data-ttu-id="2ae98-163">Yan yana görünen iki içerik yerleşimi öğesi görmelisiniz.</span><span class="sxs-lookup"><span data-stu-id="2ae98-163">You should see two content placement items that appear side by side.</span></span> <span data-ttu-id="2ae98-164">Her bir içerik yerleşim öğesi modülünün **döşeme boyutu** özelliğini ayarlayabilir veya istenen mizanpajı elde etmek için daha fazla modül ekleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="2ae98-164">You can adjust the **Tile size** property of each content placement item module or add more modules to achieve the desired layout.</span></span>
1. <span data-ttu-id="2ae98-165">Sayfayı giriş yapın ve yayımlayın.</span><span class="sxs-lookup"><span data-stu-id="2ae98-165">Check in the page, and publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="2ae98-166">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="2ae98-166">Additional resources</span></span>

[<span data-ttu-id="2ae98-167">Başlangıç paketine genel bakış</span><span class="sxs-lookup"><span data-stu-id="2ae98-167">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="2ae98-168">Uyarı modülü</span><span class="sxs-lookup"><span data-stu-id="2ae98-168">Alert module</span></span>](add-alert.md)

[<span data-ttu-id="2ae98-169">Döngü modülü</span><span class="sxs-lookup"><span data-stu-id="2ae98-169">Carousel module</span></span>](add-carousel.md)

[<span data-ttu-id="2ae98-170">İçerik zengin blok modülü</span><span class="sxs-lookup"><span data-stu-id="2ae98-170">Content rich block module</span></span>](add-content-rich-block.md)

[<span data-ttu-id="2ae98-171">Özellik modülü</span><span class="sxs-lookup"><span data-stu-id="2ae98-171">Feature module</span></span>](add-feature-module.md)

[<span data-ttu-id="2ae98-172">Hero modülü</span><span class="sxs-lookup"><span data-stu-id="2ae98-172">Hero module</span></span>](add-hero-module.md)

[<span data-ttu-id="2ae98-173">Video oynatıcı modülü</span><span class="sxs-lookup"><span data-stu-id="2ae98-173">Video player module</span></span>](add-video-player.md)
