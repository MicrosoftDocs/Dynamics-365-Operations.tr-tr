---
title: Metin bloku modülü
description: Bu konu metin bloku modüllerini kapsamaktadır ve Microsoft Dynamics 365 Commerce'un site sayfalarına nasıl ekleneceğini açıklamaktadır.
author: anupamar-ms
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 7dbeb8785641960cc2680335436aea10775759d3
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/31/2021
ms.locfileid: "5797779"
---
# <a name="text-block-module"></a><span data-ttu-id="e5b5b-103">Metin bloku modülü</span><span class="sxs-lookup"><span data-stu-id="e5b5b-103">Text block module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="e5b5b-104">Bu konu metin bloku modüllerini kapsamaktadır ve Microsoft Dynamics 365 Commerce'un site sayfalarına nasıl ekleneceğini açıklamaktadır.</span><span class="sxs-lookup"><span data-stu-id="e5b5b-104">This topic covers text block modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="e5b5b-105">Bir metin bloğu modülü, metin içeriği eklemek için kullanılan bir modüldür.</span><span class="sxs-lookup"><span data-stu-id="e5b5b-105">A text block module is a module that is used to add textual content.</span></span> <span data-ttu-id="e5b5b-106">Bu içerik bilgilendirici veya promosyon olabilir.</span><span class="sxs-lookup"><span data-stu-id="e5b5b-106">This content can be informational or promotional.</span></span>

<span data-ttu-id="e5b5b-107">Metin bloku modülleri, içerik yönetimi sistemindeki (CMS) veriler tarafından yönlendiriliyor ve herhangi bir sayfaya konabilir.</span><span class="sxs-lookup"><span data-stu-id="e5b5b-107">Text block modules are driven by data from the content management system (CMS) and can be put on any page.</span></span> <span data-ttu-id="e5b5b-108">Bunlar sayfa bağlamına veya diğer modüllere bağımlı olmayan bağımsız modüllerdir.</span><span class="sxs-lookup"><span data-stu-id="e5b5b-108">They are stand-alone modules that don't depend on page context or any other modules.</span></span>

## <a name="examples-of-text-block-modules-in-e-commerce"></a><span data-ttu-id="e5b5b-109">E-ticarette metin bloku örnekleri</span><span class="sxs-lookup"><span data-stu-id="e5b5b-109">Examples of text block modules in e-Commerce</span></span>

<span data-ttu-id="e5b5b-110">Metin bloku modüller aşağıdaki yollarla kullanılabilir:</span><span class="sxs-lookup"><span data-stu-id="e5b5b-110">Text block modules can be used in the following ways:</span></span>

* <span data-ttu-id="e5b5b-111">Ürün ayrıntıları sayfasında ürün özelliklerini sergileme.</span><span class="sxs-lookup"><span data-stu-id="e5b5b-111">To showcase product features on a product details page.</span></span>
* <span data-ttu-id="e5b5b-112">Her sayfada yalnızca bilgi amacıyladır.</span><span class="sxs-lookup"><span data-stu-id="e5b5b-112">For informational purposes on any page.</span></span> <span data-ttu-id="e5b5b-113">Örneğin, bağlılık programlarının yararlarını açıklayabilir, Sevkiyat ve iade ilkelerini açıklayabilir, sık sorulan soruların yanıtlanması veya "Hakkımızda" içeriği sağlayabilirler.</span><span class="sxs-lookup"><span data-stu-id="e5b5b-113">For example, they can explain the benefits of loyalty programs, describe shipping and return policies, answer frequently asked questions, or provide "about us" content.</span></span>
* <span data-ttu-id="e5b5b-114">Ürün ayrıntıları sayfasına özel iletiler eklemek için.</span><span class="sxs-lookup"><span data-stu-id="e5b5b-114">To add custom messages on a product details page.</span></span> <span data-ttu-id="e5b5b-115">(örneğin, "$50 üzerinden olan siparişler için ücretsiz sevkiyat").</span><span class="sxs-lookup"><span data-stu-id="e5b5b-115">(for example, "Free shipping for orders over $50").</span></span>
* <span data-ttu-id="e5b5b-116">Ürün Ayrıntıları sayfaları, sepet sayfaları, kullanıma alma sayfaları ve diğer sayfalar hakkında feragatler ve ilgili kişi ayrıntıları için (örneğin, "Sevkiyat ve iadeler depolama ilkelerine tabidir").</span><span class="sxs-lookup"><span data-stu-id="e5b5b-116">For disclaimers and contact details on product details pages, cart pages, checkout pages, and other pages (for example, "Shipping and returns are subject to store policies").</span></span>

<span data-ttu-id="e5b5b-117">Aşağıdaki resimde giriş sayfasında kullanılan bir metin bloku modülü örneği gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="e5b5b-117">The following image shows an example of a text block module that is used on a home page.</span></span>

![Metin bloku modülü örneği](./media/ecommerce-textblock.PNG)

## <a name="text-block-module-properties"></a><span data-ttu-id="e5b5b-119">Metin bloku modülü özellikleri</span><span class="sxs-lookup"><span data-stu-id="e5b5b-119">Text block module properties</span></span>

| <span data-ttu-id="e5b5b-120">Özellik adı</span><span class="sxs-lookup"><span data-stu-id="e5b5b-120">Property name</span></span>     | <span data-ttu-id="e5b5b-121">Değer</span><span class="sxs-lookup"><span data-stu-id="e5b5b-121">Value</span></span>                                            | <span data-ttu-id="e5b5b-122">Tanım</span><span class="sxs-lookup"><span data-stu-id="e5b5b-122">Description</span></span> |
|-------------------|--------------------------------------------------|-------------|
| <span data-ttu-id="e5b5b-123">Zengin metin</span><span class="sxs-lookup"><span data-stu-id="e5b5b-123">Rich text</span></span>         | <span data-ttu-id="e5b5b-124">Zengin metin</span><span class="sxs-lookup"><span data-stu-id="e5b5b-124">Rich text</span></span>                                        | <span data-ttu-id="e5b5b-125">Paragraf metni.</span><span class="sxs-lookup"><span data-stu-id="e5b5b-125">Paragraph text.</span></span> <span data-ttu-id="e5b5b-126">Kalın, altı çizili, italik metin gibi bazı temel zengin metin özellikleri desteklenir.</span><span class="sxs-lookup"><span data-stu-id="e5b5b-126">Some basic rich text capabilities are supported, such as bold, underlined, and italic text.</span></span> |
| <span data-ttu-id="e5b5b-127">Özel sınıfı adı</span><span class="sxs-lookup"><span data-stu-id="e5b5b-127">Custom class name</span></span> | <span data-ttu-id="e5b5b-128">Geçişli stil sayfaları (CSS) sınıf adı</span><span class="sxs-lookup"><span data-stu-id="e5b5b-128">A Cascading Style Sheets (CSS) class name</span></span>        | <span data-ttu-id="e5b5b-129">Bu modülü biçimlendirmek için bir CSS geliştiricinin sağladığı özel sınıfın adı.</span><span class="sxs-lookup"><span data-stu-id="e5b5b-129">The name of a custom CSS class that a developer provides to format this module.</span></span> <span data-ttu-id="e5b5b-130">Sınıf adı Tema paketinde tanımlanmalıdır.</span><span class="sxs-lookup"><span data-stu-id="e5b5b-130">The class name should be defined in the theme pack.</span></span> |
| <span data-ttu-id="e5b5b-131">Yazı türü boyutu</span><span class="sxs-lookup"><span data-stu-id="e5b5b-131">Font size</span></span>         | <span data-ttu-id="e5b5b-132">**Küçük**, **orta**, **büyük** veya **Ekstra büyük**</span><span class="sxs-lookup"><span data-stu-id="e5b5b-132">**Small**, **Medium**, **Large**, or **X-Large**</span></span> | <span data-ttu-id="e5b5b-133">İçeriğin yazı tipi boyutu.</span><span class="sxs-lookup"><span data-stu-id="e5b5b-133">The font size of the content.</span></span> |

## <a name="add-a-text-block-module-to-a-page"></a><span data-ttu-id="e5b5b-134">Bir sayfaya metin bloku modülü ekleme</span><span class="sxs-lookup"><span data-stu-id="e5b5b-134">Add a text block module to a page</span></span>

<span data-ttu-id="e5b5b-135">Bir yeni sayfaya metin bloku modülü eklemek ve gerekli özellikleri ayarlamak için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="e5b5b-135">To add a text block module to a new page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="e5b5b-136">Bir yeni şablonu oluşturmak için **Şablonlar**'a gidin ve **Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="e5b5b-136">Go to **Templates**, and select **New** to create a new template.</span></span>
1. <span data-ttu-id="e5b5b-137">**Yeni Şablon** iletişim kutusunda **Şablon adı** altında, **İçerik şablonu** girin.</span><span class="sxs-lookup"><span data-stu-id="e5b5b-137">In the **New Template** dialog box, under **Template name**, enter **Content template**.</span></span>
1. <span data-ttu-id="e5b5b-138">**Gövde** yuvası için üç nokta (**...**) düğmesini seçin ve **Modül Ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="e5b5b-138">In the **Body** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="e5b5b-139">**Modül Ekle** iletişim kutusunda **Varsayılan sayfa** modülünü seçin ve **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="e5b5b-139">In the **Add Module** dialog box, select the **Default page** module, and then select **OK**.</span></span>
1. <span data-ttu-id="e5b5b-140">**Kaydet**'i seçin, şablonu iade etmek için **Düzenlemeyi bitir**'i ve ardından yayımlamak için **Yayımla**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="e5b5b-140">Select **Save**, select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span>
1. <span data-ttu-id="e5b5b-141">**Sayfalar**'a gidin ve yeni sayfa oluşturmak için **Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="e5b5b-141">Go to **Pages**, and select **New** to create a new page.</span></span>
1. <span data-ttu-id="e5b5b-142">**Şablon seç** iletişim kutusunda **İçerik şablonu** seçin.</span><span class="sxs-lookup"><span data-stu-id="e5b5b-142">In the **Choose a template** dialog box, select **Content template**.</span></span> <span data-ttu-id="e5b5b-143">Bir **sayfa adı** ve sayfa **İçerik sayfası** girin ve **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="e5b5b-143">Under **Page name**, enter **Content page**, and then select **OK**.</span></span>
1. <span data-ttu-id="e5b5b-144">Yeni sayfada **ana** yuvayı seçin, üç nokta düğmesini (**...**) ve sonra **Modül ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="e5b5b-144">In the **Main** slot of the new page, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="e5b5b-145">**Modül Ekle** iletişim kutusunda **Konteyner** modülünü seçin ve **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="e5b5b-145">In the **Add Module** dialog box, select the **Container** module, and then select **OK**.</span></span>
1. <span data-ttu-id="e5b5b-146">Konteyner modülü için özellik panosunda **Genişlik** özelliğini **Konteyneri doldur**'a ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="e5b5b-146">In the property pane for the container module, set the **Width** property to **Fill container**.</span></span>
1. <span data-ttu-id="e5b5b-147">**Konteyner** yuvası için üç nokta (**...**) düğmesini seçin ve **Modül Ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="e5b5b-147">In the **Container** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="e5b5b-148">**Modül Ekle** iletişim kutusunda **Metin bloku** modülünü seçin ve **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="e5b5b-148">In the **Add Module** dialog box, select the **Text block** module, and then select **OK**.</span></span> 
1. <span data-ttu-id="e5b5b-149">Metin bloku modülünün özellik panosunda, **Zengin metin** alanına bir metin ekleyin.</span><span class="sxs-lookup"><span data-stu-id="e5b5b-149">In the property pane of the text block module, add text to the **Rich text** field.</span></span>
1. <span data-ttu-id="e5b5b-150">**Kaydet**'i seçin ve ardından sayfayı önizlemek için **Önizleme**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="e5b5b-150">Select **Save**, and then select **Preview** to preview the page.</span></span>
1. <span data-ttu-id="e5b5b-151">Sayfayı iade etmek için **Düzenlemeyi bitir**'i seçin, ardından yayımlamak için **Yayımla**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="e5b5b-151">Select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="e5b5b-152">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="e5b5b-152">Additional resources</span></span>

[<span data-ttu-id="e5b5b-153">Modül kitaplığına genel bakış</span><span class="sxs-lookup"><span data-stu-id="e5b5b-153">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="e5b5b-154">Promosyon başlığı modülü</span><span class="sxs-lookup"><span data-stu-id="e5b5b-154">Promo banner module</span></span>](add-alert.md)

[<span data-ttu-id="e5b5b-155">Döngü modülü</span><span class="sxs-lookup"><span data-stu-id="e5b5b-155">Carousel module</span></span>](add-carousel.md)

[<span data-ttu-id="e5b5b-156">İçerik bloğu modülü</span><span class="sxs-lookup"><span data-stu-id="e5b5b-156">Content block module</span></span>](add-hero-module.md)

[<span data-ttu-id="e5b5b-157">Video oynatıcı modülü</span><span class="sxs-lookup"><span data-stu-id="e5b5b-157">Video player module</span></span>](add-video-player.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]