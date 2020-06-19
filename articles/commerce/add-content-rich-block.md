---
title: Metin bloku modülü
description: Bu konu metin bloku modüllerini kapsamaktadır ve Microsoft Dynamics 365 Commerce'un site sayfalarına nasıl ekleneceğini açıklamaktadır.
author: anupamar-ms
manager: annbe
ms.date: 05/28/2020
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
ms.openlocfilehash: 93ad09a05d188a30b099b9a44c35e15839be80a7
ms.sourcegitcommit: b52477b7d0d52102a7ca2fb95f4ebfa30ecd9f54
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/29/2020
ms.locfileid: "3411147"
---
# <a name="text-block-module"></a><span data-ttu-id="850da-103">Metin bloku modülü</span><span class="sxs-lookup"><span data-stu-id="850da-103">Text block module</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="850da-104">Bu konu metin bloku modüllerini kapsamaktadır ve Microsoft Dynamics 365 Commerce'un site sayfalarına nasıl ekleneceğini açıklamaktadır.</span><span class="sxs-lookup"><span data-stu-id="850da-104">This topic covers text block modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="850da-105">Genel Bakış</span><span class="sxs-lookup"><span data-stu-id="850da-105">Overview</span></span>

<span data-ttu-id="850da-106">Bir metin bloğu modülü, metin içeriği eklemek için kullanılan bir modüldür.</span><span class="sxs-lookup"><span data-stu-id="850da-106">A text block module is a module that is used to add textual content.</span></span> <span data-ttu-id="850da-107">Bu içerik bilgilendirici veya promosyon olabilir.</span><span class="sxs-lookup"><span data-stu-id="850da-107">This content can be informational or promotional.</span></span>

<span data-ttu-id="850da-108">Metin bloku modülleri, içerik yönetimi sistemindeki (CMS) veriler tarafından yönlendiriliyor ve herhangi bir sayfaya konabilir.</span><span class="sxs-lookup"><span data-stu-id="850da-108">Text block modules are driven by data from the content management system (CMS) and can be put on any page.</span></span> <span data-ttu-id="850da-109">Bunlar sayfa bağlamına veya diğer modüllere bağımlı olmayan bağımsız modüllerdir.</span><span class="sxs-lookup"><span data-stu-id="850da-109">They are stand-alone modules that don't depend on page context or any other modules.</span></span>

## <a name="examples-of-text-block-modules-in-e-commerce"></a><span data-ttu-id="850da-110">E-ticarette metin bloku örnekleri</span><span class="sxs-lookup"><span data-stu-id="850da-110">Examples of text block modules in e-Commerce</span></span>

<span data-ttu-id="850da-111">Metin bloku modüller aşağıdaki yollarla kullanılabilir:</span><span class="sxs-lookup"><span data-stu-id="850da-111">Text block modules can be used in the following ways:</span></span>

* <span data-ttu-id="850da-112">Ürün ayrıntıları sayfasında ürün özelliklerini sergileme.</span><span class="sxs-lookup"><span data-stu-id="850da-112">To showcase product features on a product details page.</span></span>
* <span data-ttu-id="850da-113">Her sayfada yalnızca bilgi amacıyladır.</span><span class="sxs-lookup"><span data-stu-id="850da-113">For informational purposes on any page.</span></span> <span data-ttu-id="850da-114">Örneğin, bağlılık programlarının yararlarını açıklayabilir, Sevkiyat ve iade ilkelerini açıklayabilir, sık sorulan soruların yanıtlanması veya "Hakkımızda" içeriği sağlayabilirler.</span><span class="sxs-lookup"><span data-stu-id="850da-114">For example, they can explain the benefits of loyalty programs, describe shipping and return policies, answer frequently asked questions, or provide "about us" content.</span></span>
* <span data-ttu-id="850da-115">Ürün ayrıntıları sayfasına özel iletiler eklemek için.</span><span class="sxs-lookup"><span data-stu-id="850da-115">To add custom messages on a product details page.</span></span> <span data-ttu-id="850da-116">(örneğin, "$50 üzerinden olan siparişler için ücretsiz sevkiyat").</span><span class="sxs-lookup"><span data-stu-id="850da-116">(for example, "Free shipping for orders over $50").</span></span>
* <span data-ttu-id="850da-117">Ürün Ayrıntıları sayfaları, sepet sayfaları, kullanıma alma sayfaları ve diğer sayfalar hakkında feragatler ve ilgili kişi ayrıntıları için (örneğin, "Sevkiyat ve iadeler depolama ilkelerine tabidir").</span><span class="sxs-lookup"><span data-stu-id="850da-117">For disclaimers and contact details on product details pages, cart pages, checkout pages, and other pages (for example, "Shipping and returns are subject to store policies").</span></span>

<span data-ttu-id="850da-118">Aşağıdaki resimde giriş sayfasında kullanılan bir metin bloku modülü örneği gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="850da-118">The following image shows an example of a text block module that is used on a home page.</span></span>

![Metin bloku modülü örneği](./media/ecommerce-textblock.PNG)

## <a name="text-block-module-properties"></a><span data-ttu-id="850da-120">Metin bloku modülü özellikleri</span><span class="sxs-lookup"><span data-stu-id="850da-120">Text block module properties</span></span>

| <span data-ttu-id="850da-121">Özellik adı</span><span class="sxs-lookup"><span data-stu-id="850da-121">Property name</span></span>     | <span data-ttu-id="850da-122">Değer</span><span class="sxs-lookup"><span data-stu-id="850da-122">Value</span></span>                                            | <span data-ttu-id="850da-123">Tanım</span><span class="sxs-lookup"><span data-stu-id="850da-123">Description</span></span> |
|-------------------|--------------------------------------------------|-------------|
| <span data-ttu-id="850da-124">Zengin metin</span><span class="sxs-lookup"><span data-stu-id="850da-124">Rich text</span></span>         | <span data-ttu-id="850da-125">Zengin metin</span><span class="sxs-lookup"><span data-stu-id="850da-125">Rich text</span></span>                                        | <span data-ttu-id="850da-126">Paragraf metni.</span><span class="sxs-lookup"><span data-stu-id="850da-126">Paragraph text.</span></span> <span data-ttu-id="850da-127">Kalın, altı çizili, italik metin gibi bazı temel zengin metin özellikleri desteklenir.</span><span class="sxs-lookup"><span data-stu-id="850da-127">Some basic rich text capabilities are supported, such as bold, underlined, and italic text.</span></span> |
| <span data-ttu-id="850da-128">Özel sınıfı adı</span><span class="sxs-lookup"><span data-stu-id="850da-128">Custom class name</span></span> | <span data-ttu-id="850da-129">Geçişli stil sayfaları (CSS) sınıf adı</span><span class="sxs-lookup"><span data-stu-id="850da-129">A Cascading Style Sheets (CSS) class name</span></span>        | <span data-ttu-id="850da-130">Bu modülü biçimlendirmek için bir CSS geliştiricinin sağladığı özel sınıfın adı.</span><span class="sxs-lookup"><span data-stu-id="850da-130">The name of a custom CSS class that a developer provides to format this module.</span></span> <span data-ttu-id="850da-131">Sınıf adı Tema paketinde tanımlanmalıdır.</span><span class="sxs-lookup"><span data-stu-id="850da-131">The class name should be defined in the theme pack.</span></span> |
| <span data-ttu-id="850da-132">Yazı türü boyutu</span><span class="sxs-lookup"><span data-stu-id="850da-132">Font size</span></span>         | <span data-ttu-id="850da-133">**Küçük**, **orta**, **büyük** veya **Ekstra büyük**</span><span class="sxs-lookup"><span data-stu-id="850da-133">**Small**, **Medium**, **Large**, or **X-Large**</span></span> | <span data-ttu-id="850da-134">İçeriğin yazı tipi boyutu.</span><span class="sxs-lookup"><span data-stu-id="850da-134">The font size of the content.</span></span> |

## <a name="add-a-text-block-module-to-a-page"></a><span data-ttu-id="850da-135">Bir sayfaya metin bloku modülü ekleme</span><span class="sxs-lookup"><span data-stu-id="850da-135">Add a text block module to a page</span></span>

<span data-ttu-id="850da-136">Bir yeni sayfaya metin bloku modülü eklemek ve gerekli özellikleri ayarlamak için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="850da-136">To add a text block module to a new page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="850da-137">Bir yeni şablonu oluşturmak için **Şablonlar**'a gidin ve **Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="850da-137">Go to **Templates**, and select **New** to create a new template.</span></span>
1. <span data-ttu-id="850da-138">**Yeni Şablon** iletişim kutusunda **Şablon adı** altında, **İçerik şablonu** girin.</span><span class="sxs-lookup"><span data-stu-id="850da-138">In the **New Template** dialog box, under **Template name**, enter **Content template**.</span></span>
1. <span data-ttu-id="850da-139">**Gövde** yuvası için üç nokta (**...**) düğmesini seçin ve **Modül Ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="850da-139">In the **Body** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="850da-140">**Modül Ekle** iletişim kutusunda **Varsayılan sayfa** modülünü seçin ve **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="850da-140">In the **Add Module** dialog box, select the **Default page** module, and then select **OK**.</span></span>
1. <span data-ttu-id="850da-141">**Kaydet**'i seçin, şablonu iade etmek için **Düzenlemeyi bitir**'i ve ardından yayımlamak için **Yayımla**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="850da-141">Select **Save**, select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span>
1. <span data-ttu-id="850da-142">**Sayfalar**'a gidin ve yeni sayfa oluşturmak için **Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="850da-142">Go to **Pages**, and select **New** to create a new page.</span></span>
1. <span data-ttu-id="850da-143">**Şablon seç** iletişim kutusunda **İçerik şablonu** seçin.</span><span class="sxs-lookup"><span data-stu-id="850da-143">In the **Choose a template** dialog box, select **Content template**.</span></span> <span data-ttu-id="850da-144">Bir **sayfa adı** ve sayfa **İçerik sayfası** girin ve **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="850da-144">Under **Page name**, enter **Content page**, and then select **OK**.</span></span>
1. <span data-ttu-id="850da-145">Yeni sayfada **ana** yuvayı seçin, üç nokta düğmesini (**...**) ve sonra **Modül ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="850da-145">In the **Main** slot of the new page, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="850da-146">**Modül Ekle** iletişim kutusunda **Konteyner** modülünü seçin ve **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="850da-146">In the **Add Module** dialog box, select the **Container** module, and then select **OK**.</span></span>
1. <span data-ttu-id="850da-147">Konteyner modülü için özellik panosunda **Genişlik** özelliğini **Konteyneri doldur**'a ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="850da-147">In the property pane for the container module, set the **Width** property to **Fill container**.</span></span>
1. <span data-ttu-id="850da-148">**Konteyner** yuvası için üç nokta (**...**) düğmesini seçin ve **Modül Ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="850da-148">In the **Container** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="850da-149">**Modül Ekle** iletişim kutusunda **Metin bloku** modülünü seçin ve **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="850da-149">In the **Add Module** dialog box, select the **Text block** module, and then select **OK**.</span></span> 
1. <span data-ttu-id="850da-150">Metin bloku modülünün özellik panosunda, **Zengin metin** alanına bir metin ekleyin.</span><span class="sxs-lookup"><span data-stu-id="850da-150">In the property pane of the text block module, add text to the **Rich text** field.</span></span>
1. <span data-ttu-id="850da-151">**Kaydet**'i seçin ve ardından sayfayı önizlemek için **Önizleme**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="850da-151">Select **Save**, and then select **Preview** to preview the page.</span></span>
1. <span data-ttu-id="850da-152">Sayfayı iade etmek için **Düzenlemeyi bitir**'i seçin, ardından yayımlamak için **Yayımla**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="850da-152">Select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="850da-153">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="850da-153">Additional resources</span></span>

[<span data-ttu-id="850da-154">Başlangıç paketine genel bakış</span><span class="sxs-lookup"><span data-stu-id="850da-154">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="850da-155">Promosyon başlığı modülü</span><span class="sxs-lookup"><span data-stu-id="850da-155">Promo banner module</span></span>](add-alert.md)

[<span data-ttu-id="850da-156">Döngü modülü</span><span class="sxs-lookup"><span data-stu-id="850da-156">Carousel module</span></span>](add-carousel.md)

[<span data-ttu-id="850da-157">İçerik blok modülü</span><span class="sxs-lookup"><span data-stu-id="850da-157">Content block module</span></span>](add-hero-module.md)

[<span data-ttu-id="850da-158">Video oynatıcı modülü</span><span class="sxs-lookup"><span data-stu-id="850da-158">Video player module</span></span>](add-video-player.md)

