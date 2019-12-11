---
title: İçerik zengin blok modülü
description: Bu konu içerik zengin blok modüllerini kapsamaktadır ve Microsoft Dynamics 365 Commerce'un site sayfalarına nasıl ekleneceğini açıklamaktadır.
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
ms.openlocfilehash: 27dabb425b3c9a3015ffc54ff3c0e50b7ee11749
ms.sourcegitcommit: 3a4e137ef3a96ba0a58c5352f4a3b57467ace9ae
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/11/2019
ms.locfileid: "2785433"
---
# <a name="content-rich-block-module"></a><span data-ttu-id="e7035-103">İçerik zengin blok modülü</span><span class="sxs-lookup"><span data-stu-id="e7035-103">Content rich block module</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="e7035-104">Bu konu içerik zengin blok modüllerini kapsamaktadır ve Microsoft Dynamics 365 Commerce'un site sayfalarına nasıl ekleneceğini açıklamaktadır.</span><span class="sxs-lookup"><span data-stu-id="e7035-104">This topic covers content rich block modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="e7035-105">Genel Bakış</span><span class="sxs-lookup"><span data-stu-id="e7035-105">Overview</span></span>

<span data-ttu-id="e7035-106">İçerik zengin blok modülü, bir veya daha fazla içerik zengin blok öğenin içine koyulacağı özel bir konteynerdir.</span><span class="sxs-lookup"><span data-stu-id="e7035-106">A content rich block module is a special container that one or more content rich block items can be put inside.</span></span> <span data-ttu-id="e7035-107">İçerik zengin blok modülleri, bir sayfadaki metin içeriği için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="e7035-107">Content rich block modules are used for textual content on a page.</span></span> <span data-ttu-id="e7035-108">Bu içerik bilgilendirici veya promosyon olabilir.</span><span class="sxs-lookup"><span data-stu-id="e7035-108">This content can be either informational or promotional.</span></span>

<span data-ttu-id="e7035-109">İçerik zengin blok modülleri, içerik yönetimi sistemindeki (CMS) veriler tarafından yönlendiriliyor ve herhangi bir sayfaya konabilir.</span><span class="sxs-lookup"><span data-stu-id="e7035-109">Content rich block modules are driven by data from the content management system (CMS) and can be put on any page.</span></span> <span data-ttu-id="e7035-110">Bunlar sayfa bağlamına veya diğer modüllere bağımlı olmayan bağımsız modüllerdir.</span><span class="sxs-lookup"><span data-stu-id="e7035-110">They are stand-alone modules that don't depend on page context or any other modules.</span></span>

## <a name="examples-of-content-rich-block-modules-in-e-commerce"></a><span data-ttu-id="e7035-111">E-ticarette içerik zengin blok modülleri örnekleri</span><span class="sxs-lookup"><span data-stu-id="e7035-111">Examples of content rich block modules in e-Commerce</span></span>

<span data-ttu-id="e7035-112">İçerik zengin blok modüller aşağıdaki yollarla kullanılabilir:</span><span class="sxs-lookup"><span data-stu-id="e7035-112">Content rich block modules can be used in the following ways:</span></span>

* <span data-ttu-id="e7035-113">Ürün ayrıntıları sayfasında ürün özelliklerini sergileme.</span><span class="sxs-lookup"><span data-stu-id="e7035-113">To showcase product features on a product details page.</span></span>
* <span data-ttu-id="e7035-114">Her sayfada yalnızca bilgi amacıyladır.</span><span class="sxs-lookup"><span data-stu-id="e7035-114">For informational purposes on any page.</span></span> <span data-ttu-id="e7035-115">Örneğin, bağlılık programlarının yararlarını açıklayabilir, Sevkiyat ve iade ilkelerini açıklayabilir, sık sorulan soruların yanıtlanması veya "Hakkımızda" içeriği sağlayabilirler.</span><span class="sxs-lookup"><span data-stu-id="e7035-115">For example, they can explain the benefits of loyalty programs, describe shipping and return policies, answer frequently asked questions, or provide "about us" content.</span></span>
* <span data-ttu-id="e7035-116">Ürün ayrıntıları sayfasına özel iletiler eklemek için.</span><span class="sxs-lookup"><span data-stu-id="e7035-116">To add custom messages on a product details page.</span></span> <span data-ttu-id="e7035-117">(örneğin, "$50 üzerinden olan siparişler için ücretsiz sevkiyat").</span><span class="sxs-lookup"><span data-stu-id="e7035-117">(for example, "Free shipping for orders over $50").</span></span>
* <span data-ttu-id="e7035-118">Ürün Ayrıntıları sayfaları, sepet sayfaları, kullanıma alma sayfaları ve diğer sayfalar hakkında feragatler ve ilgili kişi ayrıntıları için (örneğin, "Sevkiyat ve iadeler depolama ilkelerine tabidir").</span><span class="sxs-lookup"><span data-stu-id="e7035-118">For disclaimers and contact details on product details pages, cart pages, checkout pages, and other pages (for example, "Shipping and returns are subject to store policies").</span></span>

## <a name="content-rich-block-module-properties"></a><span data-ttu-id="e7035-119">İçerik zengin blok modülü özellikleri</span><span class="sxs-lookup"><span data-stu-id="e7035-119">Content rich block module properties</span></span>

| <span data-ttu-id="e7035-120">Özellik adı</span><span class="sxs-lookup"><span data-stu-id="e7035-120">Property name</span></span>     | <span data-ttu-id="e7035-121">Değer</span><span class="sxs-lookup"><span data-stu-id="e7035-121">Value</span></span>                                 | <span data-ttu-id="e7035-122">Özellik</span><span class="sxs-lookup"><span data-stu-id="e7035-122">Property</span></span> |
|-------------------|---------------------------------------|----------|
| <span data-ttu-id="e7035-123">Sütun sayısı</span><span class="sxs-lookup"><span data-stu-id="e7035-123">Number of columns</span></span> | <span data-ttu-id="e7035-124">**1** ile **4** arasında bir sayı</span><span class="sxs-lookup"><span data-stu-id="e7035-124">A number from **1** through **4**</span></span>     | <span data-ttu-id="e7035-125">İçerik zengin bloğundaki sütunların sayısı.</span><span class="sxs-lookup"><span data-stu-id="e7035-125">The number of columns in the content rich block.</span></span> <span data-ttu-id="e7035-126">En çok dört sütun olabilir.</span><span class="sxs-lookup"><span data-stu-id="e7035-126">There can be up to four columns.</span></span> |
| <span data-ttu-id="e7035-127">Genişlik</span><span class="sxs-lookup"><span data-stu-id="e7035-127">Width</span></span>             | <span data-ttu-id="e7035-128">**Kapsayıcıya sığdır** veya **Ekrana doldur**</span><span class="sxs-lookup"><span data-stu-id="e7035-128">**Fill container** or **Fill screen**</span></span> | <span data-ttu-id="e7035-129">Değer **konteynere doldur** şekilde ayarlandıysa, konteyner içindeki öğeler konteyner genişliğiyle sınırlandırılır.</span><span class="sxs-lookup"><span data-stu-id="e7035-129">If the value is set to **Fill container**, the items inside the container are restricted to the width of the container.</span></span> <span data-ttu-id="e7035-130">Değer, **ekranı doldur**'a ayarlanmışsa, öğeler konteyner genişliğiyle sınırlandırılmaz ancak tam ekran moduna geçebilir.</span><span class="sxs-lookup"><span data-stu-id="e7035-130">If the value is set to **Fill screen**, the items aren't restricted to the container width but can go into full-screen mode.</span></span> <span data-ttu-id="e7035-131">İstenen düzene ulaşmak için değeri değiştirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="e7035-131">You can change the value to achieve the desired layout.</span></span> |

## <a name="content-rich-block-item-module-properties"></a><span data-ttu-id="e7035-132">İçerik zengin blok öğesi modülü özellikleri</span><span class="sxs-lookup"><span data-stu-id="e7035-132">Content rich block item module properties</span></span>

| <span data-ttu-id="e7035-133">Özellik adı</span><span class="sxs-lookup"><span data-stu-id="e7035-133">Property name</span></span> | <span data-ttu-id="e7035-134">Değer</span><span class="sxs-lookup"><span data-stu-id="e7035-134">Value</span></span>          | <span data-ttu-id="e7035-135">Tanım</span><span class="sxs-lookup"><span data-stu-id="e7035-135">Description</span></span> |
|---------------|----------------|-------------|
| <span data-ttu-id="e7035-136">Paragraf</span><span class="sxs-lookup"><span data-stu-id="e7035-136">Paragraph</span></span>     | <span data-ttu-id="e7035-137">Paragraf metni</span><span class="sxs-lookup"><span data-stu-id="e7035-137">Paragraph text</span></span> | <span data-ttu-id="e7035-138">Her içerik zengin blok öğesine eşlik eden metin.</span><span class="sxs-lookup"><span data-stu-id="e7035-138">The text that accompanies each content rich block item.</span></span> <span data-ttu-id="e7035-139">Kalın, altı çizili, italik metin gibi bazı temel zengin metin özellikleri desteklenir.</span><span class="sxs-lookup"><span data-stu-id="e7035-139">Some basic rich text capabilities are supported, such as bold, underlined, and italic text.</span></span> |

## <a name="add-a-content-rich-block-module-to-a-page"></a><span data-ttu-id="e7035-140">Sayfaya içerik zengin blok modülü ekleme</span><span class="sxs-lookup"><span data-stu-id="e7035-140">Add a content rich block module to a page</span></span>

<span data-ttu-id="e7035-141">Bir yeni sayfaya içerik zengin blok modülü eklemek ve gerekli özellikleri ayarlamak için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="e7035-141">To add a content rich block module to a new page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="e7035-142">**İçerik şablonu** adlı bir sayfa şablonu oluşturun.</span><span class="sxs-lookup"><span data-stu-id="e7035-142">Create a page template that is named **Content template**.</span></span>
1. <span data-ttu-id="e7035-143">Varsayılan sayfanın **ana** yuvasına bir içerik zengin blok modülü ekleyin.</span><span class="sxs-lookup"><span data-stu-id="e7035-143">In the **Main** slot of the default page, add a content rich block module.</span></span>
1. <span data-ttu-id="e7035-144">Şablonu giriş yapın ve yayımlayın.</span><span class="sxs-lookup"><span data-stu-id="e7035-144">Check in the template, and publish it.</span></span>
1. <span data-ttu-id="e7035-145">**İçerik sayfası** adlı bir sayfa oluşturmak için yeni oluşturduğunuz içerik şablonunu kullanın.</span><span class="sxs-lookup"><span data-stu-id="e7035-145">Use the content template that you just created to create a page that is named **Content page**.</span></span>
1. <span data-ttu-id="e7035-146">Yeni sayfanın **ana** yuvasına bir içerik zengin blok modülü ekleyin.</span><span class="sxs-lookup"><span data-stu-id="e7035-146">In the **Main** slot of the new page, add a content rich block module.</span></span>
1. <span data-ttu-id="e7035-147">İçerik zengin blok modülünün özelliklerinde, sütun sayısını **2** olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="e7035-147">In the properties of the content rich block module, set number of columns to **2**.</span></span>
1. <span data-ttu-id="e7035-148">İçerik zengin blok modülünde **modül ekle**'yi seçin ve içerik zengin blok bir öğe ekleyin (örneğin, **item1**).</span><span class="sxs-lookup"><span data-stu-id="e7035-148">In the content rich block module, select **Add a module**, and add a content rich block item (for example, **item1**).</span></span>
1. <span data-ttu-id="e7035-149">Yeni içerik zengin blok öğesinde paragraf metni ekleyin.</span><span class="sxs-lookup"><span data-stu-id="e7035-149">In the new content rich block item, add paragraph text.</span></span>
1. <span data-ttu-id="e7035-150">İçerik zengin blok modülünde **modül ekle**'yi seçin ve içerik zengin blok bir öğe ekleyin (örneğin, **item2**).</span><span class="sxs-lookup"><span data-stu-id="e7035-150">In the content rich block module, select **Add a module**, and add a content rich block item (for example, **item2**).</span></span>
1. <span data-ttu-id="e7035-151">Yeni içerik zengin blok öğesinde paragraf metni ekleyin.</span><span class="sxs-lookup"><span data-stu-id="e7035-151">In the new content rich block item, add paragraph text.</span></span>
1. <span data-ttu-id="e7035-152">Sayfayı kaydedin ve değişiklikleri önizleyin.</span><span class="sxs-lookup"><span data-stu-id="e7035-152">Save the page, and preview the changes.</span></span> <span data-ttu-id="e7035-153">İki sütunlu görünümde iki zengin metin bloğu görmelisiniz.</span><span class="sxs-lookup"><span data-stu-id="e7035-153">You should see two rich text blocks in a two-column view.</span></span>
1. <span data-ttu-id="e7035-154">Sayfayı giriş yapın ve yayımlayın.</span><span class="sxs-lookup"><span data-stu-id="e7035-154">Check in the page, and publish it.</span></span>

> [!NOTE]
> <span data-ttu-id="e7035-155">Üçüncü içerikli bir zengin blok öğesi eklerseniz, bu öğe daha önce eklediğiniz iki öğenin altına yığılır.</span><span class="sxs-lookup"><span data-stu-id="e7035-155">If you add a third content rich block item, it will be stacked below the two items that you previously added.</span></span> <span data-ttu-id="e7035-156">Konteynerdeki sütunların ve öğelerin sayısını değiştirerek metin içeriği için farklı düzenler elde edebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="e7035-156">By changing the number of columns and items in the container, you can achieve different layouts for textual content.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="e7035-157">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="e7035-157">Additional resources</span></span>

[<span data-ttu-id="e7035-158">Başlangıç paketine genel bakış</span><span class="sxs-lookup"><span data-stu-id="e7035-158">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="e7035-159">Uyarı modülü</span><span class="sxs-lookup"><span data-stu-id="e7035-159">Alert module</span></span>](add-alert.md)

[<span data-ttu-id="e7035-160">Döngü modülü</span><span class="sxs-lookup"><span data-stu-id="e7035-160">Carousel module</span></span>](add-carousel.md)

[<span data-ttu-id="e7035-161">İçerik yerleştirme modülü</span><span class="sxs-lookup"><span data-stu-id="e7035-161">Content placement module</span></span>](add-content-placement-modules.md)

[<span data-ttu-id="e7035-162">Özellik modülü</span><span class="sxs-lookup"><span data-stu-id="e7035-162">Feature module</span></span>](add-feature-module.md)

[<span data-ttu-id="e7035-163">Hero modülü</span><span class="sxs-lookup"><span data-stu-id="e7035-163">Hero module</span></span>](add-hero-module.md)

[<span data-ttu-id="e7035-164">Video oynatıcı modülü</span><span class="sxs-lookup"><span data-stu-id="e7035-164">Video player module</span></span>](add-video-player.md)

