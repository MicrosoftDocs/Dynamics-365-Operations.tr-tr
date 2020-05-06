---
title: Promosyon başlık modülü
description: Bu konu promosyon başlığı modüllerini kapsamaktadır ve Microsoft Dynamics 365 Commerce'un site sayfalarına nasıl ekleneceğini açıklamaktadır.
author: anupamar-ms
manager: annbe
ms.date: 04/14/2020
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
ms.openlocfilehash: 12cabbf0b8d9f337f15a8cd6cb1f2a85100b75f7
ms.sourcegitcommit: 7a1d01122790b904e2d96a7ea9f1d003392358a6
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/17/2020
ms.locfileid: "3269786"
---
# <a name="promo-banner-module"></a><span data-ttu-id="83216-103">Promosyon başlık modülü</span><span class="sxs-lookup"><span data-stu-id="83216-103">Promo banner module</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="83216-104">Bu konu promosyon başlığı modüllerini kapsamaktadır ve Microsoft Dynamics 365 Commerce'un site sayfalarına nasıl ekleneceğini açıklamaktadır.</span><span class="sxs-lookup"><span data-stu-id="83216-104">This topic covers promo banner modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="83216-105">Genel Bakış</span><span class="sxs-lookup"><span data-stu-id="83216-105">Overview</span></span>

<span data-ttu-id="83216-106">Promosyon başlığı modülleri, bir sayfadaki satır içi bilgilendirme iletilerini göstermekte kullanılır.</span><span class="sxs-lookup"><span data-stu-id="83216-106">Promo banner modules are used to show inline informational messages on a page.</span></span> <span data-ttu-id="83216-107">Bir e-ticaret sitesinin tüm sayfalarında görünen site çapında yükseltmeleri göstermek için kullanılabilirler.</span><span class="sxs-lookup"><span data-stu-id="83216-107">They can be used to show site-wide promotions that appear on all pages of an e-Commerce site.</span></span> 

<span data-ttu-id="83216-108">Promosyon başlığı modülleri bir metin iletisini ve bir bağlantıyı destekler.</span><span class="sxs-lookup"><span data-stu-id="83216-108">Promo banner modules support a text message and a link.</span></span> <span data-ttu-id="83216-109">Bir promosyon başlık modülüne birden fazla ileti eklenirse, müşterilerin tüm iletiler arasında dolaşmasına olanak veren bir döner başlığı olur.</span><span class="sxs-lookup"><span data-stu-id="83216-109">If multiple messages are added to a promo banner module, it becomes a rotating carousel banner that lets customers cycle through all the messages.</span></span> 

<span data-ttu-id="83216-110">Promosyon başlığı, içerik yönetimi sistemindeki (CMS) veriler tarafından yönlendiriliyor ve herhangi bir sayfaya konabilir.</span><span class="sxs-lookup"><span data-stu-id="83216-110">Promo banner modules are driven by data from the content management system (CMS) and can be put on any page.</span></span>

## <a name="usage-examples-of-promo-banners-in-e-commerce"></a><span data-ttu-id="83216-111">E-ticaret'daki promosyon başlık sayfaları için kullanım örnekleri</span><span class="sxs-lookup"><span data-stu-id="83216-111">Usage examples of promo banners in e-Commerce</span></span>

<span data-ttu-id="83216-112">Promosyon başlık sayfaları site başlığında, aşağıdaki örneklerde olduğu gibi, site çapında yükseltmeleri veya iletileri göstermek amacıyla kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="83216-112">Promo banners can be used in the site header to show site-wide promotions or messages, as in the following examples.</span></span>

<span data-ttu-id="83216-113">"Yıllık satış, 10 gün içinde biter"</span><span class="sxs-lookup"><span data-stu-id="83216-113">"Annual sale ends in 10 days"</span></span>

<span data-ttu-id="83216-114">"Okul satışı ile büyük bir tasarruf yapın.</span><span class="sxs-lookup"><span data-stu-id="83216-114">"Save big with back to school sale.</span></span> <span data-ttu-id="83216-115">Şimdi alışveriş yap."</span><span class="sxs-lookup"><span data-stu-id="83216-115">Shop Now."</span></span>

## <a name="promo-banner-module-properties"></a><span data-ttu-id="83216-116">Promosyon başlığı modülü özellikleri</span><span class="sxs-lookup"><span data-stu-id="83216-116">Promo banner module properties</span></span>

| <span data-ttu-id="83216-117">Özellik adı</span><span class="sxs-lookup"><span data-stu-id="83216-117">Property name</span></span>             | <span data-ttu-id="83216-118">Value</span><span class="sxs-lookup"><span data-stu-id="83216-118">Value</span></span>                              | <span data-ttu-id="83216-119">Tanım</span><span class="sxs-lookup"><span data-stu-id="83216-119">Description</span></span> |
|---------------------------|------------------------------------|-------------|
| <span data-ttu-id="83216-120">Başlık iletileri</span><span class="sxs-lookup"><span data-stu-id="83216-120">Banner messages</span></span>           | <span data-ttu-id="83216-121">Metin ve bağlantılar</span><span class="sxs-lookup"><span data-stu-id="83216-121">Text and links</span></span>                     | <span data-ttu-id="83216-122">Metin ve bağlantılar dizisi.</span><span class="sxs-lookup"><span data-stu-id="83216-122">An array of text and links.</span></span> |
| <span data-ttu-id="83216-123">Otomatik yürüt</span><span class="sxs-lookup"><span data-stu-id="83216-123">Autoplay</span></span>                  | <span data-ttu-id="83216-124">**Doğru** veya **yanlış**</span><span class="sxs-lookup"><span data-stu-id="83216-124">**True** or **False**</span></span>              | <span data-ttu-id="83216-125">Birden fazla ileti yapılandırılmışsa, iletilerin otomatik olarak açılıp eklenmesini belirten bir değer.</span><span class="sxs-lookup"><span data-stu-id="83216-125">A value that indicates whether messages are automatically cycled through, if multiple messages are configured.</span></span> |
| <span data-ttu-id="83216-126">Slayt geçiş aralığı</span><span class="sxs-lookup"><span data-stu-id="83216-126">Slide transition interval</span></span> | <span data-ttu-id="83216-127">Milisaniyelerin sayısı (MS)</span><span class="sxs-lookup"><span data-stu-id="83216-127">A number of milliseconds (ms)</span></span>      | <span data-ttu-id="83216-128">İletiler arasında geçiş yapmak için kullanılan aralık.</span><span class="sxs-lookup"><span data-stu-id="83216-128">The interval that is used to cycle through messages.</span></span> |
| <span data-ttu-id="83216-129">Kapatmaya izin ver</span><span class="sxs-lookup"><span data-stu-id="83216-129">Allow dismiss</span></span>             | <span data-ttu-id="83216-130">**Doğru** veya **yanlış**</span><span class="sxs-lookup"><span data-stu-id="83216-130">**True** or **False**</span></span>              | <span data-ttu-id="83216-131">Değer **doğru** olarak ayarlanırsa, müşteriler uyarıyı yok edebilir.</span><span class="sxs-lookup"><span data-stu-id="83216-131">If the value is set to **True**, customers can dismiss the alert.</span></span> |
| <span data-ttu-id="83216-132">Carusel kolu göster</span><span class="sxs-lookup"><span data-stu-id="83216-132">Show carousel flipper</span></span>     | <span data-ttu-id="83216-133">**Doğru** veya **yanlış**</span><span class="sxs-lookup"><span data-stu-id="83216-133">**True** or **False**</span></span>              | <span data-ttu-id="83216-134">Döner değiştiricilerin gösterilip gösterilmeyeceğini belirten ve müşterilerin birden çok Başlık öğelerini el ile dolaşabilmesi için bir değer.</span><span class="sxs-lookup"><span data-stu-id="83216-134">A value that indicates whether the carousel flippers should be shown, so that customers can manually cycle through multiple banner items.</span></span> |
| <span data-ttu-id="83216-135">Metin hizalama</span><span class="sxs-lookup"><span data-stu-id="83216-135">Text alignment</span></span>            | <span data-ttu-id="83216-136">**Sağ**, **Sol** veya **Orta**</span><span class="sxs-lookup"><span data-stu-id="83216-136">**Right**, **Left**, or **Center**</span></span> | <span data-ttu-id="83216-137">Promosyon başlık modülünde metin hizalaması.</span><span class="sxs-lookup"><span data-stu-id="83216-137">The text alignment in the promo banner module.</span></span> |
| <span data-ttu-id="83216-138">Bağla</span><span class="sxs-lookup"><span data-stu-id="83216-138">Link</span></span>                      | <span data-ttu-id="83216-139">Bir URL</span><span class="sxs-lookup"><span data-stu-id="83216-139">A URL</span></span>                              | <span data-ttu-id="83216-140">İsteğe bağlı bağlantı için URL.</span><span class="sxs-lookup"><span data-stu-id="83216-140">The URL for an optional link.</span></span> |

## <a name="add-a-promo-banner-module-to-a-page"></a><span data-ttu-id="83216-141">Bir sayfaya bir promosyon başlığı ekle</span><span class="sxs-lookup"><span data-stu-id="83216-141">Add a promo banner module to a page</span></span> 

<span data-ttu-id="83216-142">Bir sayfaya bir promosyon başlığı modülü eklemek ve gerekli özellikleri ayarlamak için şu adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="83216-142">To add a promo banner module to a page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="83216-143">Yeni sayfa şablonu oluşturmak için **Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="83216-143">Select **New** to create a page template.</span></span>
1. <span data-ttu-id="83216-144">**Yeni Şablon** iletişim kutusunda **Şablon adı** altında, **Promosyon başlığı şablonu**'nu girin ve **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="83216-144">In the **New Template** dialog box, under **Template Name**, enter **Promo banner template**, and then select **OK**.</span></span>
1. <span data-ttu-id="83216-145">**Sayfa Anahattı** altında, bir **Varsayılan sayfa** modülünü **Gövde** yuvasına ekleyin.</span><span class="sxs-lookup"><span data-stu-id="83216-145">Under **Page Outline**, add a **Default page** module to the **Body** slot.</span></span> 
1. <span data-ttu-id="83216-146">Şablonu iade etmek için **Düzenlemeyi bitir**'i seçin, ardından yayımlamak için **Yayımla**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="83216-146">Select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span> 
1. <span data-ttu-id="83216-147">**Promosyon başlığı sayfası** adlı bir sayfa oluşturmak için yeni oluşturduğunuz uyarı şablonunu kullanın.</span><span class="sxs-lookup"><span data-stu-id="83216-147">Use the template that you just created to create a page that is named **Promo banner page**.</span></span> 
1. <span data-ttu-id="83216-148">Yeni sayfanın **ana** yuvasına bir konteyner modülü ekleyin.</span><span class="sxs-lookup"><span data-stu-id="83216-148">In the **Main** slot of the new page, add a container module.</span></span> 
1. <span data-ttu-id="83216-149">Sağdaki panoda, **Genişlik** değerini **Konteyneri doldur**'a ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="83216-149">In the pane on the right, set the **Width** value to **Fill Container**.</span></span>
1. <span data-ttu-id="83216-150">**Sayfa Anahattı** altında, bir promosyon başlığı modlünü konteyner modülüne ekleyin.</span><span class="sxs-lookup"><span data-stu-id="83216-150">Under **Page Outline**, add a promo banner module to the container module.</span></span>
1. <span data-ttu-id="83216-151">Başlık modülünün ayarlarında bir veya daha fazla başlık ekleyin.</span><span class="sxs-lookup"><span data-stu-id="83216-151">In the settings for the banner module, add one or more banner messages.</span></span> <span data-ttu-id="83216-152">Her iletinin bir bağlantı ile birlikte bir metni olabilir.</span><span class="sxs-lookup"><span data-stu-id="83216-152">Each message can have text together with a link.</span></span> <span data-ttu-id="83216-153">Modülü daha fazla özelleştirmek için diğer özellikleri düzenleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="83216-153">You can edit the other properties to customize the module further.</span></span>
1. <span data-ttu-id="83216-154">**Kaydet**'i seçin ve ardından sayfayı önizlemek için **Önizleme**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="83216-154">Select **Save**, and then select **Preview** to preview the page.</span></span> <span data-ttu-id="83216-155">Sayfanın üst kısmında, eklediğiniz metni içeren bir uyarı görmelisiniz.</span><span class="sxs-lookup"><span data-stu-id="83216-155">At the top of the page, you should see an alert that shows the text that you added.</span></span>
1. <span data-ttu-id="83216-156">Sayfayı iade etmek için **Düzenlemeyi bitir**'i seçin, ardından yayımlamak için **Yayımla**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="83216-156">Select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span> 

> [!NOTE]
> <span data-ttu-id="83216-157">Bir promosyon başlığı genellikle sayfa üstbilgisi yuvasında veya alt başlık yuvasında kullanılır.</span><span class="sxs-lookup"><span data-stu-id="83216-157">A promo banner is typically used in the page header slot or a subheader slot.</span></span>


## <a name="additional-resources"></a><span data-ttu-id="83216-158">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="83216-158">Additional resources</span></span>

[<span data-ttu-id="83216-159">Başlangıç paketine genel bakış</span><span class="sxs-lookup"><span data-stu-id="83216-159">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="83216-160">Döngü modülü</span><span class="sxs-lookup"><span data-stu-id="83216-160">Carousel module</span></span>](add-carousel.md)

[<span data-ttu-id="83216-161">Metin bloku modülü</span><span class="sxs-lookup"><span data-stu-id="83216-161">Text block module</span></span>](add-content-rich-block.md)

[<span data-ttu-id="83216-162">İçerik blok modülü</span><span class="sxs-lookup"><span data-stu-id="83216-162">Content block module</span></span>](add-hero-module.md)

[<span data-ttu-id="83216-163">Video oynatıcı modülü</span><span class="sxs-lookup"><span data-stu-id="83216-163">Video player module</span></span>](add-video-player.md)
