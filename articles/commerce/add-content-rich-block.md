---
title: Metin bloku modülü
description: Bu konu metin bloku modüllerini kapsamaktadır ve Microsoft Dynamics 365 Commerce'un site sayfalarına nasıl ekleneceğini açıklamaktadır.
author: anupamar-ms
manager: annbe
ms.date: 01/23/2020
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
ms.openlocfilehash: fc5b2fa35633b1ce7f7ffefacec318e14fa8db3f
ms.sourcegitcommit: 829329220475ed8cff5a5db92a59dd90c22b04fa
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/05/2020
ms.locfileid: "3025609"
---
# <a name="text-block-module"></a><span data-ttu-id="da43b-103">Metin bloku modülü</span><span class="sxs-lookup"><span data-stu-id="da43b-103">Text block module</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="da43b-104">Bu konu metin bloku modüllerini kapsamaktadır ve Microsoft Dynamics 365 Commerce'un site sayfalarına nasıl ekleneceğini açıklamaktadır.</span><span class="sxs-lookup"><span data-stu-id="da43b-104">This topic covers text block modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="da43b-105">Genel Bakış</span><span class="sxs-lookup"><span data-stu-id="da43b-105">Overview</span></span>

<span data-ttu-id="da43b-106">Bir metin bloğu modülü, metin içeriği eklemek için kullanılan bir modüldür.</span><span class="sxs-lookup"><span data-stu-id="da43b-106">A text block module is a module that is used to add textual content.</span></span> <span data-ttu-id="da43b-107">Bu içerik bilgilendirici veya promosyon olabilir.</span><span class="sxs-lookup"><span data-stu-id="da43b-107">This content can be informational or promotional.</span></span>

<span data-ttu-id="da43b-108">Metin bloku modülleri, içerik yönetimi sistemindeki (CMS) veriler tarafından yönlendiriliyor ve herhangi bir sayfaya konabilir.</span><span class="sxs-lookup"><span data-stu-id="da43b-108">Text block modules are driven by data from the content management system (CMS) and can be put on any page.</span></span> <span data-ttu-id="da43b-109">Bunlar sayfa bağlamına veya diğer modüllere bağımlı olmayan bağımsız modüllerdir.</span><span class="sxs-lookup"><span data-stu-id="da43b-109">They are stand-alone modules that don't depend on page context or any other modules.</span></span>

## <a name="examples-of-text-block-modules-in-e-commerce"></a><span data-ttu-id="da43b-110">E-ticarette metin bloku örnekleri</span><span class="sxs-lookup"><span data-stu-id="da43b-110">Examples of text block modules in e-Commerce</span></span>

<span data-ttu-id="da43b-111">Metin bloku modüller aşağıdaki yollarla kullanılabilir:</span><span class="sxs-lookup"><span data-stu-id="da43b-111">Text block modules can be used in the following ways:</span></span>

* <span data-ttu-id="da43b-112">Ürün ayrıntıları sayfasında ürün özelliklerini sergileme.</span><span class="sxs-lookup"><span data-stu-id="da43b-112">To showcase product features on a product details page.</span></span>
* <span data-ttu-id="da43b-113">Her sayfada yalnızca bilgi amacıyladır.</span><span class="sxs-lookup"><span data-stu-id="da43b-113">For informational purposes on any page.</span></span> <span data-ttu-id="da43b-114">Örneğin, bağlılık programlarının yararlarını açıklayabilir, Sevkiyat ve iade ilkelerini açıklayabilir, sık sorulan soruların yanıtlanması veya "Hakkımızda" içeriği sağlayabilirler.</span><span class="sxs-lookup"><span data-stu-id="da43b-114">For example, they can explain the benefits of loyalty programs, describe shipping and return policies, answer frequently asked questions, or provide "about us" content.</span></span>
* <span data-ttu-id="da43b-115">Ürün ayrıntıları sayfasına özel iletiler eklemek için.</span><span class="sxs-lookup"><span data-stu-id="da43b-115">To add custom messages on a product details page.</span></span> <span data-ttu-id="da43b-116">(örneğin, "$50 üzerinden olan siparişler için ücretsiz sevkiyat").</span><span class="sxs-lookup"><span data-stu-id="da43b-116">(for example, "Free shipping for orders over $50").</span></span>
* <span data-ttu-id="da43b-117">Ürün Ayrıntıları sayfaları, sepet sayfaları, kullanıma alma sayfaları ve diğer sayfalar hakkında feragatler ve ilgili kişi ayrıntıları için (örneğin, "Sevkiyat ve iadeler depolama ilkelerine tabidir").</span><span class="sxs-lookup"><span data-stu-id="da43b-117">For disclaimers and contact details on product details pages, cart pages, checkout pages, and other pages (for example, "Shipping and returns are subject to store policies").</span></span>

## <a name="text-block-module-properties"></a><span data-ttu-id="da43b-118">Metin bloku modülü özellikleri</span><span class="sxs-lookup"><span data-stu-id="da43b-118">Text block module properties</span></span>

| <span data-ttu-id="da43b-119">Özellik adı</span><span class="sxs-lookup"><span data-stu-id="da43b-119">Property name</span></span>     | <span data-ttu-id="da43b-120">Value</span><span class="sxs-lookup"><span data-stu-id="da43b-120">Value</span></span>                                            | <span data-ttu-id="da43b-121">Tanım</span><span class="sxs-lookup"><span data-stu-id="da43b-121">Description</span></span> |
|-------------------|--------------------------------------------------|-------------|
| <span data-ttu-id="da43b-122">Zengin metin</span><span class="sxs-lookup"><span data-stu-id="da43b-122">Rich text</span></span>         | <span data-ttu-id="da43b-123">Zengin metin</span><span class="sxs-lookup"><span data-stu-id="da43b-123">Rich text</span></span>                                        | <span data-ttu-id="da43b-124">Paragraf metni.</span><span class="sxs-lookup"><span data-stu-id="da43b-124">Paragraph text.</span></span> <span data-ttu-id="da43b-125">Kalın, altı çizili, italik metin gibi bazı temel zengin metin özellikleri desteklenir.</span><span class="sxs-lookup"><span data-stu-id="da43b-125">Some basic rich text capabilities are supported, such as bold, underlined, and italic text.</span></span> |
| <span data-ttu-id="da43b-126">Özel sınıfı adı</span><span class="sxs-lookup"><span data-stu-id="da43b-126">Custom class name</span></span> | <span data-ttu-id="da43b-127">Geçişli stil sayfaları (CSS) sınıf adı</span><span class="sxs-lookup"><span data-stu-id="da43b-127">A Cascading Style Sheets (CSS) class name</span></span>        | <span data-ttu-id="da43b-128">Bu modülü biçimlendirmek için bir CSS geliştiricinin sağladığı özel sınıfın adı.</span><span class="sxs-lookup"><span data-stu-id="da43b-128">The name of a custom CSS class that a developer provides to format this module.</span></span> <span data-ttu-id="da43b-129">Sınıf adı Tema paketinde tanımlanmalıdır.</span><span class="sxs-lookup"><span data-stu-id="da43b-129">The class name should be defined in the theme pack.</span></span> |
| <span data-ttu-id="da43b-130">Yazı türü boyutu</span><span class="sxs-lookup"><span data-stu-id="da43b-130">Font size</span></span>         | <span data-ttu-id="da43b-131">**Küçük**, **orta**, **büyük** veya **Ekstra büyük**</span><span class="sxs-lookup"><span data-stu-id="da43b-131">**Small**, **Medium**, **Large**, or **X-Large**</span></span> | <span data-ttu-id="da43b-132">İçeriğin yazı tipi boyutu.</span><span class="sxs-lookup"><span data-stu-id="da43b-132">The font size of the content.</span></span> |

## <a name="add-a-text-block-module-to-a-page"></a><span data-ttu-id="da43b-133">Bir sayfaya metin bloku modülü ekleme</span><span class="sxs-lookup"><span data-stu-id="da43b-133">Add a text block module to a page</span></span>

<span data-ttu-id="da43b-134">Bir yeni sayfaya metin bloku modülü eklemek ve gerekli özellikleri ayarlamak için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="da43b-134">To add a text block module to a new page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="da43b-135">**İçerik şablonu** adlı bir sayfa şablonu oluşturun.</span><span class="sxs-lookup"><span data-stu-id="da43b-135">Create a page template that is named **Content template**.</span></span> 
1. <span data-ttu-id="da43b-136">**Gövde** yuvasında bir **Varsayılan sayfa** modülü ekleyin.</span><span class="sxs-lookup"><span data-stu-id="da43b-136">In the **Body** slot, add a **Default page** module.</span></span>
1. <span data-ttu-id="da43b-137">Şablon düzenlemeyi tamamlayın ve sonra yayımlayın.</span><span class="sxs-lookup"><span data-stu-id="da43b-137">Finish editing the template, and publish it.</span></span>
1. <span data-ttu-id="da43b-138">**İçerik sayfası** adlı bir sayfa oluşturmak için yeni oluşturduğunuz içerik şablonunu kullanın.</span><span class="sxs-lookup"><span data-stu-id="da43b-138">Use the content template that you just created to create a page that is named **Content page**.</span></span>
1. <span data-ttu-id="da43b-139">Yeni sayfanın **ana** yuvasına bir konteyner modülü ekleyin.</span><span class="sxs-lookup"><span data-stu-id="da43b-139">In the **Main** slot of the new page, add a container module.</span></span>
1. <span data-ttu-id="da43b-140">Konteyner modülü için özellik panosunda **Genişlik** özelliğini **Konteyneri doldur**'a ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="da43b-140">In the property pane for the container module, set the **Width** property to **Fill container**.</span></span>
1. <span data-ttu-id="da43b-141">Kapsayıcı modülüne bir metin bloku modülü ekleyin.</span><span class="sxs-lookup"><span data-stu-id="da43b-141">Add a text block module to the container module.</span></span> 
1. <span data-ttu-id="da43b-142">Metin bloku modülünün özellik panosunda, **Zengin metin** alanına bir metin ekleyin.</span><span class="sxs-lookup"><span data-stu-id="da43b-142">In the property pane of the text block module, add text to the **Rich text** field.</span></span>
1. <span data-ttu-id="da43b-143">Sayfayı düzenlemeyi tamamlayın ve sonra yayımlayın.</span><span class="sxs-lookup"><span data-stu-id="da43b-143">Finish editing the page, and publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="da43b-144">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="da43b-144">Additional resources</span></span>

[<span data-ttu-id="da43b-145">Başlangıç paketine genel bakış</span><span class="sxs-lookup"><span data-stu-id="da43b-145">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="da43b-146">Promosyon başlık modülü</span><span class="sxs-lookup"><span data-stu-id="da43b-146">Promo banner module</span></span>](add-alert.md)

[<span data-ttu-id="da43b-147">Döngü modülü</span><span class="sxs-lookup"><span data-stu-id="da43b-147">Carousel module</span></span>](add-carousel.md)

[<span data-ttu-id="da43b-148">İçerik blok modülü</span><span class="sxs-lookup"><span data-stu-id="da43b-148">Content block module</span></span>](add-hero-module.md)

[<span data-ttu-id="da43b-149">Video oynatıcı modülü</span><span class="sxs-lookup"><span data-stu-id="da43b-149">Video player module</span></span>](add-video-player.md)

