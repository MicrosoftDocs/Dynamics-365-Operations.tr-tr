---
title: Promosyon başlık modülü
description: Bu konu promosyon başlığı modüllerini kapsamaktadır ve Microsoft Dynamics 365 Commerce'un site sayfalarına nasıl ekleneceğini açıklamaktadır.
author: anupamar-ms
manager: annbe
ms.date: 01/23/2020
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
ms.openlocfilehash: da5e220e4578d1064eb7b627b441d3f585b3c095
ms.sourcegitcommit: 829329220475ed8cff5a5db92a59dd90c22b04fa
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/05/2020
ms.locfileid: "3025632"
---
# <a name="promo-banner-module"></a><span data-ttu-id="60fc6-103">Promosyon başlık modülü</span><span class="sxs-lookup"><span data-stu-id="60fc6-103">Promo banner module</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="60fc6-104">Bu konu promosyon başlığı modüllerini kapsamaktadır ve Microsoft Dynamics 365 Commerce'un site sayfalarına nasıl ekleneceğini açıklamaktadır.</span><span class="sxs-lookup"><span data-stu-id="60fc6-104">This topic covers promo banner modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="60fc6-105">Genel Bakış</span><span class="sxs-lookup"><span data-stu-id="60fc6-105">Overview</span></span>

<span data-ttu-id="60fc6-106">Promosyon başlığı modülleri, bir sayfadaki satır içi bilgilendirme iletilerini göstermekte kullanılır.</span><span class="sxs-lookup"><span data-stu-id="60fc6-106">Promo banner modules are used to show inline informational messages on a page.</span></span> <span data-ttu-id="60fc6-107">Bir e-ticaret sitesinin tüm sayfalarında görünen site çapında yükseltmeleri göstermek için kullanılabilirler.</span><span class="sxs-lookup"><span data-stu-id="60fc6-107">They can be used to show site-wide promotions that appear on all pages of an e-Commerce site.</span></span> 

<span data-ttu-id="60fc6-108">Promosyon başlığı modülleri bir metin iletisini ve bir bağlantıyı destekler.</span><span class="sxs-lookup"><span data-stu-id="60fc6-108">Promo banner modules support a text message and a link.</span></span> <span data-ttu-id="60fc6-109">Bir promosyon başlık modülüne birden fazla ileti eklenirse, müşterilerin tüm iletiler arasında dolaşmasına olanak veren bir döner başlığı olur.</span><span class="sxs-lookup"><span data-stu-id="60fc6-109">If multiple messages are added to a promo banner module, it becomes a rotating carousel banner that lets customers cycle through all the messages.</span></span> 

<span data-ttu-id="60fc6-110">Promosyon başlığı, içerik yönetimi sistemindeki (CMS) veriler tarafından yönlendiriliyor ve herhangi bir sayfaya konabilir.</span><span class="sxs-lookup"><span data-stu-id="60fc6-110">Promo banner modules are driven by data from the content management system (CMS) and can be put on any page.</span></span>

## <a name="usage-examples-of-promo-banners-in-e-commerce"></a><span data-ttu-id="60fc6-111">E-ticaret'daki promosyon başlık sayfaları için kullanım örnekleri</span><span class="sxs-lookup"><span data-stu-id="60fc6-111">Usage examples of promo banners in e-Commerce</span></span>

<span data-ttu-id="60fc6-112">Promosyon başlık sayfaları site başlığında, aşağıdaki örneklerde olduğu gibi, site çapında yükseltmeleri veya iletileri göstermek amacıyla kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="60fc6-112">Promo banners can be used in the site header to show site-wide promotions or messages, as in the following examples.</span></span>

<span data-ttu-id="60fc6-113">"Yıllık satış, 10 gün içinde biter"</span><span class="sxs-lookup"><span data-stu-id="60fc6-113">"Annual sale ends in 10 days"</span></span>

<span data-ttu-id="60fc6-114">"Okul satışı ile büyük bir tasarruf yapın.</span><span class="sxs-lookup"><span data-stu-id="60fc6-114">"Save big with back to school sale.</span></span> <span data-ttu-id="60fc6-115">Şimdi alışveriş yap."</span><span class="sxs-lookup"><span data-stu-id="60fc6-115">Shop Now."</span></span>

## <a name="promo-banner-module-properties"></a><span data-ttu-id="60fc6-116">Promosyon başlığı modülü özellikleri</span><span class="sxs-lookup"><span data-stu-id="60fc6-116">Promo banner module properties</span></span>

| <span data-ttu-id="60fc6-117">Özellik adı</span><span class="sxs-lookup"><span data-stu-id="60fc6-117">Property name</span></span>             | <span data-ttu-id="60fc6-118">Value</span><span class="sxs-lookup"><span data-stu-id="60fc6-118">Value</span></span>                              | <span data-ttu-id="60fc6-119">Tanım</span><span class="sxs-lookup"><span data-stu-id="60fc6-119">Description</span></span> |
|---------------------------|------------------------------------|-------------|
| <span data-ttu-id="60fc6-120">Başlık iletileri</span><span class="sxs-lookup"><span data-stu-id="60fc6-120">Banner messages</span></span>           | <span data-ttu-id="60fc6-121">Metin ve bağlantılar</span><span class="sxs-lookup"><span data-stu-id="60fc6-121">Text and links</span></span>                     | <span data-ttu-id="60fc6-122">Metin ve bağlantılar dizisi.</span><span class="sxs-lookup"><span data-stu-id="60fc6-122">An array of text and links.</span></span> |
| <span data-ttu-id="60fc6-123">Otomatik yürüt</span><span class="sxs-lookup"><span data-stu-id="60fc6-123">Autoplay</span></span>                  | <span data-ttu-id="60fc6-124">**Doğru** veya **yanlış**</span><span class="sxs-lookup"><span data-stu-id="60fc6-124">**True** or **False**</span></span>              | <span data-ttu-id="60fc6-125">Birden fazla ileti yapılandırılmışsa, iletilerin otomatik olarak açılıp eklenmesini belirten bir değer.</span><span class="sxs-lookup"><span data-stu-id="60fc6-125">A value that indicates whether messages are automatically cycled through, if multiple messages are configured.</span></span> |
| <span data-ttu-id="60fc6-126">Slayt geçiş aralığı</span><span class="sxs-lookup"><span data-stu-id="60fc6-126">Slide transition interval</span></span> | <span data-ttu-id="60fc6-127">Milisaniyelerin sayısı (MS)</span><span class="sxs-lookup"><span data-stu-id="60fc6-127">A number of milliseconds (ms)</span></span>      | <span data-ttu-id="60fc6-128">İletiler arasında geçiş yapmak için kullanılan aralık.</span><span class="sxs-lookup"><span data-stu-id="60fc6-128">The interval that is used to cycle through messages.</span></span> |
| <span data-ttu-id="60fc6-129">Kapatmaya izin ver</span><span class="sxs-lookup"><span data-stu-id="60fc6-129">Allow dismiss</span></span>             | <span data-ttu-id="60fc6-130">**Doğru** veya **yanlış**</span><span class="sxs-lookup"><span data-stu-id="60fc6-130">**True** or **False**</span></span>              | <span data-ttu-id="60fc6-131">Değer **doğru** olarak ayarlanırsa, müşteriler uyarıyı yok edebilir.</span><span class="sxs-lookup"><span data-stu-id="60fc6-131">If the value is set to **True**, customers can dismiss the alert.</span></span> |
| <span data-ttu-id="60fc6-132">Carusel kolu göster</span><span class="sxs-lookup"><span data-stu-id="60fc6-132">Show carousel flipper</span></span>     | <span data-ttu-id="60fc6-133">**Doğru** veya **yanlış**</span><span class="sxs-lookup"><span data-stu-id="60fc6-133">**True** or **False**</span></span>              | <span data-ttu-id="60fc6-134">Döner değiştiricilerin gösterilip gösterilmeyeceğini belirten ve müşterilerin birden çok Başlık öğelerini el ile dolaşabilmesi için bir değer.</span><span class="sxs-lookup"><span data-stu-id="60fc6-134">A value that indicates whether the carousel flippers should be shown, so that customers can manually cycle through multiple banner items.</span></span> |
| <span data-ttu-id="60fc6-135">Metin hizalama</span><span class="sxs-lookup"><span data-stu-id="60fc6-135">Text alignment</span></span>            | <span data-ttu-id="60fc6-136">**Sağ**, **Sol** veya **Orta**</span><span class="sxs-lookup"><span data-stu-id="60fc6-136">**Right**, **Left**, or **Center**</span></span> | <span data-ttu-id="60fc6-137">Promosyon başlık modülünde metin hizalaması.</span><span class="sxs-lookup"><span data-stu-id="60fc6-137">The text alignment in the promo banner module.</span></span> |
| <span data-ttu-id="60fc6-138">Bağla</span><span class="sxs-lookup"><span data-stu-id="60fc6-138">Link</span></span>                      | <span data-ttu-id="60fc6-139">Bir URL</span><span class="sxs-lookup"><span data-stu-id="60fc6-139">A URL</span></span>                              | <span data-ttu-id="60fc6-140">İsteğe bağlı bağlantı için URL.</span><span class="sxs-lookup"><span data-stu-id="60fc6-140">The URL for an optional link.</span></span> |

## <a name="add-a-promo-banner-module-to-a-page"></a><span data-ttu-id="60fc6-141">Bir sayfaya bir promosyon başlığı ekle</span><span class="sxs-lookup"><span data-stu-id="60fc6-141">Add a promo banner module to a page</span></span> 

<span data-ttu-id="60fc6-142">Bir sayfaya bir promosyon başlığı modülü eklemek ve gerekli özellikleri ayarlamak için şu adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="60fc6-142">To add a promo banner module to a page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="60fc6-143">**Promosyon şablonu** adlı bir sayfa şablonu oluşturun.</span><span class="sxs-lookup"><span data-stu-id="60fc6-143">Create a page template that is named **Promo banner template**.</span></span>
1. <span data-ttu-id="60fc6-144">**Sayfa Anahattı** altında, bir **Varsayılan sayfa** modülünü **Gövde** yuvasına ekleyin.</span><span class="sxs-lookup"><span data-stu-id="60fc6-144">Under **Page Outline**, add a **Default page** module to the **Body** slot.</span></span> 
1. <span data-ttu-id="60fc6-145">Şablonu giriş yapın ve yayımlayın.</span><span class="sxs-lookup"><span data-stu-id="60fc6-145">Check in the template, and publish it.</span></span> 
1. <span data-ttu-id="60fc6-146">**Promosyon başlığı sayfası** adlı bir sayfa oluşturmak için yeni oluşturduğunuz uyarı şablonunu kullanın.</span><span class="sxs-lookup"><span data-stu-id="60fc6-146">Use the template that you just created to create a page that is named **Promo banner page**.</span></span> 
1. <span data-ttu-id="60fc6-147">Yeni sayfanın **ana** yuvasına bir konteyner modülü ekleyin.</span><span class="sxs-lookup"><span data-stu-id="60fc6-147">In the **Main** slot of the new page, add a container module.</span></span> 
1. <span data-ttu-id="60fc6-148">Sağdaki panoda, **Genişlik** değerini **Konteyneri doldur**'a ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="60fc6-148">In the pane on the right, set the **Width** value to **Fill Container**.</span></span>
1. <span data-ttu-id="60fc6-149">**Sayfa Anahattı** altında, bir promosyon başlığı modlünü konteyner modülüne ekleyin.</span><span class="sxs-lookup"><span data-stu-id="60fc6-149">Under **Page Outline**, add a promo banner module to the container module.</span></span>
1. <span data-ttu-id="60fc6-150">Başlık modülünün ayarlarında bir veya daha fazla başlık ekleyin.</span><span class="sxs-lookup"><span data-stu-id="60fc6-150">In the settings for the banner module, add one or more banner messages.</span></span> <span data-ttu-id="60fc6-151">Her iletinin bir bağlantı ile birlikte bir metni olabilir.</span><span class="sxs-lookup"><span data-stu-id="60fc6-151">Each message can have text together with a link.</span></span> <span data-ttu-id="60fc6-152">Modülü daha fazla özelleştirmek için diğer özellikleri düzenleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="60fc6-152">You can edit the other properties to customize the module further.</span></span>
1. <span data-ttu-id="60fc6-153">Sayfayı kaydet ve önizleyin.</span><span class="sxs-lookup"><span data-stu-id="60fc6-153">Save and preview the page.</span></span> <span data-ttu-id="60fc6-154">Sayfanın üst kısmında, eklediğiniz metni içeren bir uyarı görmelisiniz.</span><span class="sxs-lookup"><span data-stu-id="60fc6-154">At the top of the page, you should see an alert that shows the text that you added.</span></span>
1. <span data-ttu-id="60fc6-155">Sayfayı düzenlemeyi tamamlayın ve sonra yayımlayın.</span><span class="sxs-lookup"><span data-stu-id="60fc6-155">Finish editing the page, and publish it.</span></span> 

> [!NOTE]
> <span data-ttu-id="60fc6-156">Bir promosyon başlığı genellikle sayfa üstbilgisi yuvasında veya alt başlık yuvasında kullanılır.</span><span class="sxs-lookup"><span data-stu-id="60fc6-156">A promo banner is typically used in the page header slot or a subheader slot.</span></span>


## <a name="additional-resources"></a><span data-ttu-id="60fc6-157">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="60fc6-157">Additional resources</span></span>

[<span data-ttu-id="60fc6-158">Başlangıç paketine genel bakış</span><span class="sxs-lookup"><span data-stu-id="60fc6-158">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="60fc6-159">Döngü modülü</span><span class="sxs-lookup"><span data-stu-id="60fc6-159">Carousel module</span></span>](add-carousel.md)

[<span data-ttu-id="60fc6-160">Metin bloku modülü</span><span class="sxs-lookup"><span data-stu-id="60fc6-160">Text block module</span></span>](add-content-rich-block.md)

[<span data-ttu-id="60fc6-161">İçerik blok modülü</span><span class="sxs-lookup"><span data-stu-id="60fc6-161">Content block module</span></span>](add-hero-module.md)

[<span data-ttu-id="60fc6-162">Video oynatıcı modülü</span><span class="sxs-lookup"><span data-stu-id="60fc6-162">Video player module</span></span>](add-video-player.md)
