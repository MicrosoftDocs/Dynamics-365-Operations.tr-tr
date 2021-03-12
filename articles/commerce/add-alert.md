---
title: Promosyon başlık modülü
description: Bu konu promosyon başlığı modüllerini kapsamaktadır ve Microsoft Dynamics 365 Commerce'un site sayfalarına nasıl ekleneceğini açıklamaktadır.
author: anupamar-ms
manager: annbe
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: a77196be69bb71d917bf84c633199a3af3fbf478
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/15/2021
ms.locfileid: "4986041"
---
# <a name="promo-banner-module"></a><span data-ttu-id="c8ec0-103">Promosyon başlık modülü</span><span class="sxs-lookup"><span data-stu-id="c8ec0-103">Promo banner module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="c8ec0-104">Bu konu promosyon başlığı modüllerini kapsamaktadır ve Microsoft Dynamics 365 Commerce'un site sayfalarına nasıl ekleneceğini açıklamaktadır.</span><span class="sxs-lookup"><span data-stu-id="c8ec0-104">This topic covers promo banner modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="c8ec0-105">Genel Bakış</span><span class="sxs-lookup"><span data-stu-id="c8ec0-105">Overview</span></span>

<span data-ttu-id="c8ec0-106">Promosyon başlığı modülleri, bir sayfadaki satır içi bilgilendirme iletilerini göstermekte kullanılır.</span><span class="sxs-lookup"><span data-stu-id="c8ec0-106">Promo banner modules are used to show inline informational messages on a page.</span></span> <span data-ttu-id="c8ec0-107">Bir e-ticaret sitesinin tüm sayfalarında görünen site çapında yükseltmeleri göstermek için kullanılabilirler.</span><span class="sxs-lookup"><span data-stu-id="c8ec0-107">They can be used to show site-wide promotions that appear on all pages of an e-Commerce site.</span></span> 

<span data-ttu-id="c8ec0-108">Promosyon başlığı modülleri bir metin iletisini ve bir bağlantıyı destekler.</span><span class="sxs-lookup"><span data-stu-id="c8ec0-108">Promo banner modules support a text message and a link.</span></span> <span data-ttu-id="c8ec0-109">Bir promosyon başlık modülüne birden fazla ileti eklenirse, müşterilerin tüm iletiler arasında dolaşmasına olanak veren bir döner başlığı olur.</span><span class="sxs-lookup"><span data-stu-id="c8ec0-109">If multiple messages are added to a promo banner module, it becomes a rotating carousel banner that lets customers cycle through all the messages.</span></span> 

<span data-ttu-id="c8ec0-110">Promosyon başlığı, içerik yönetimi sistemindeki (CMS) veriler tarafından yönlendiriliyor ve herhangi bir sayfaya konabilir.</span><span class="sxs-lookup"><span data-stu-id="c8ec0-110">Promo banner modules are driven by data from the content management system (CMS) and can be put on any page.</span></span>

## <a name="usage-examples-of-promo-banners-in-e-commerce"></a><span data-ttu-id="c8ec0-111">E-ticaret'daki promosyon başlık sayfaları için kullanım örnekleri</span><span class="sxs-lookup"><span data-stu-id="c8ec0-111">Usage examples of promo banners in e-Commerce</span></span>

<span data-ttu-id="c8ec0-112">Promosyon başlık sayfaları site başlığında, aşağıdaki örneklerde olduğu gibi, site çapında yükseltmeleri veya iletileri göstermek amacıyla kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="c8ec0-112">Promo banners can be used in the site header to show site-wide promotions or messages, as in the following examples.</span></span>

<span data-ttu-id="c8ec0-113">"Yıllık satış, 10 gün içinde biter"</span><span class="sxs-lookup"><span data-stu-id="c8ec0-113">"Annual sale ends in 10 days"</span></span>

<span data-ttu-id="c8ec0-114">"Okul satışı ile büyük bir tasarruf yapın.</span><span class="sxs-lookup"><span data-stu-id="c8ec0-114">"Save big with back to school sale.</span></span> <span data-ttu-id="c8ec0-115">Şimdi alışveriş yap."</span><span class="sxs-lookup"><span data-stu-id="c8ec0-115">Shop Now."</span></span>

<span data-ttu-id="c8ec0-116">"Şükran günü İNDİRİM alışverişi yap!"</span><span class="sxs-lookup"><span data-stu-id="c8ec0-116">"Shop for Thanksgiving SALE!"</span></span> 

<span data-ttu-id="c8ec0-117">Aşağıdaki resimde, bir promosyon başlığı örneği gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="c8ec0-117">The following image shows an example of a promo banner.</span></span>

![Promosyon başlık modülü örneği](./media/ecommerce-Promobanner.PNG)

## <a name="promo-banner-module-properties"></a><span data-ttu-id="c8ec0-119">Promosyon başlığı modülü özellikleri</span><span class="sxs-lookup"><span data-stu-id="c8ec0-119">Promo banner module properties</span></span>

| <span data-ttu-id="c8ec0-120">Özellik adı</span><span class="sxs-lookup"><span data-stu-id="c8ec0-120">Property name</span></span>             | <span data-ttu-id="c8ec0-121">Değer</span><span class="sxs-lookup"><span data-stu-id="c8ec0-121">Value</span></span>                              | <span data-ttu-id="c8ec0-122">Tanım</span><span class="sxs-lookup"><span data-stu-id="c8ec0-122">Description</span></span> |
|---------------------------|------------------------------------|-------------|
| <span data-ttu-id="c8ec0-123">Başlık iletileri</span><span class="sxs-lookup"><span data-stu-id="c8ec0-123">Banner messages</span></span>           | <span data-ttu-id="c8ec0-124">Metin ve bağlantılar</span><span class="sxs-lookup"><span data-stu-id="c8ec0-124">Text and links</span></span>                     | <span data-ttu-id="c8ec0-125">Metin ve bağlantılar dizisi.</span><span class="sxs-lookup"><span data-stu-id="c8ec0-125">An array of text and links.</span></span> |
| <span data-ttu-id="c8ec0-126">Otomatik yürüt</span><span class="sxs-lookup"><span data-stu-id="c8ec0-126">Autoplay</span></span>                  | <span data-ttu-id="c8ec0-127">**Doğru** veya **yanlış**</span><span class="sxs-lookup"><span data-stu-id="c8ec0-127">**True** or **False**</span></span>              | <span data-ttu-id="c8ec0-128">Birden fazla ileti yapılandırılmışsa, iletilerin otomatik olarak açılıp eklenmesini belirten bir değer.</span><span class="sxs-lookup"><span data-stu-id="c8ec0-128">A value that indicates whether messages are automatically cycled through, if multiple messages are configured.</span></span> |
| <span data-ttu-id="c8ec0-129">Slayt geçiş aralığı</span><span class="sxs-lookup"><span data-stu-id="c8ec0-129">Slide transition interval</span></span> | <span data-ttu-id="c8ec0-130">Milisaniyelerin sayısı (MS)</span><span class="sxs-lookup"><span data-stu-id="c8ec0-130">A number of milliseconds (ms)</span></span>      | <span data-ttu-id="c8ec0-131">İletiler arasında geçiş yapmak için kullanılan aralık.</span><span class="sxs-lookup"><span data-stu-id="c8ec0-131">The interval that is used to cycle through messages.</span></span> |
| <span data-ttu-id="c8ec0-132">Kapatmaya izin ver</span><span class="sxs-lookup"><span data-stu-id="c8ec0-132">Allow dismiss</span></span>             | <span data-ttu-id="c8ec0-133">**Doğru** veya **yanlış**</span><span class="sxs-lookup"><span data-stu-id="c8ec0-133">**True** or **False**</span></span>              | <span data-ttu-id="c8ec0-134">Değer **doğru** olarak ayarlanırsa, müşteriler uyarıyı yok edebilir.</span><span class="sxs-lookup"><span data-stu-id="c8ec0-134">If the value is set to **True**, customers can dismiss the alert.</span></span> |
| <span data-ttu-id="c8ec0-135">Carusel kolu göster</span><span class="sxs-lookup"><span data-stu-id="c8ec0-135">Show carousel flipper</span></span>     | <span data-ttu-id="c8ec0-136">**Doğru** veya **yanlış**</span><span class="sxs-lookup"><span data-stu-id="c8ec0-136">**True** or **False**</span></span>              | <span data-ttu-id="c8ec0-137">Döner değiştiricilerin gösterilip gösterilmeyeceğini belirten ve müşterilerin birden çok Başlık öğelerini el ile dolaşabilmesi için bir değer.</span><span class="sxs-lookup"><span data-stu-id="c8ec0-137">A value that indicates whether the carousel flippers should be shown, so that customers can manually cycle through multiple banner items.</span></span> |
| <span data-ttu-id="c8ec0-138">Metin hizalama</span><span class="sxs-lookup"><span data-stu-id="c8ec0-138">Text alignment</span></span>            | <span data-ttu-id="c8ec0-139">**Sağ**, **Sol** veya **Orta**</span><span class="sxs-lookup"><span data-stu-id="c8ec0-139">**Right**, **Left**, or **Center**</span></span> | <span data-ttu-id="c8ec0-140">Promosyon başlık modülünde metin hizalaması.</span><span class="sxs-lookup"><span data-stu-id="c8ec0-140">The text alignment in the promo banner module.</span></span> |
| <span data-ttu-id="c8ec0-141">Bağla</span><span class="sxs-lookup"><span data-stu-id="c8ec0-141">Link</span></span>                      | <span data-ttu-id="c8ec0-142">Bir URL</span><span class="sxs-lookup"><span data-stu-id="c8ec0-142">A URL</span></span>                              | <span data-ttu-id="c8ec0-143">İsteğe bağlı bağlantı için URL.</span><span class="sxs-lookup"><span data-stu-id="c8ec0-143">The URL for an optional link.</span></span> |

## <a name="add-a-promo-banner-module-to-a-page"></a><span data-ttu-id="c8ec0-144">Bir sayfaya bir promosyon başlığı ekle</span><span class="sxs-lookup"><span data-stu-id="c8ec0-144">Add a promo banner module to a page</span></span> 

<span data-ttu-id="c8ec0-145">Bir sayfaya bir promosyon başlığı modülü eklemek ve gerekli özellikleri ayarlamak için şu adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="c8ec0-145">To add a promo banner module to a page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="c8ec0-146">Bir yeni şablonu oluşturmak için **Şablonlar**'a gidin ve **Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="c8ec0-146">Go to **Templates**, and select **New** to create a new template.</span></span>
1. <span data-ttu-id="c8ec0-147">**Yeni Şablon** iletişim kutusunda **Şablon adı** altında, **Promosyon başlığı şablonu**'nu girin ve **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="c8ec0-147">In the **New Template** dialog box, under **Template Name**, enter **Promo banner template**, and then select **OK**.</span></span>
1. <span data-ttu-id="c8ec0-148">**Sayfa Anahattı** altında, bir **Varsayılan sayfa** modülünü **Gövde** yuvasına ekleyin.</span><span class="sxs-lookup"><span data-stu-id="c8ec0-148">Under **Page Outline**, add a **Default page** module to the **Body** slot.</span></span> 
1. <span data-ttu-id="c8ec0-149">Şablonu iade etmek için **Düzenlemeyi bitir**'i seçin, ardından yayımlamak için **Yayımla**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="c8ec0-149">Select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span> 
1. <span data-ttu-id="c8ec0-150">**Promosyon başlığı sayfası** adlı bir sayfa oluşturmak için yeni oluşturduğunuz uyarı şablonunu kullanın.</span><span class="sxs-lookup"><span data-stu-id="c8ec0-150">Use the template that you just created to create a page that is named **Promo banner page**.</span></span> 
1. <span data-ttu-id="c8ec0-151">Yeni sayfanın **ana** yuvasına bir konteyner modülü ekleyin.</span><span class="sxs-lookup"><span data-stu-id="c8ec0-151">In the **Main** slot of the new page, add a container module.</span></span> 
1. <span data-ttu-id="c8ec0-152">Sağdaki panoda, **Genişlik** değerini **Konteyneri doldur**'a ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="c8ec0-152">In the pane on the right, set the **Width** value to **Fill Container**.</span></span>
1. <span data-ttu-id="c8ec0-153">**Sayfa Anahattı** altında, bir promosyon başlığı modlünü konteyner modülüne ekleyin.</span><span class="sxs-lookup"><span data-stu-id="c8ec0-153">Under **Page Outline**, add a promo banner module to the container module.</span></span>
1. <span data-ttu-id="c8ec0-154">Başlık modülünün ayarlarında bir veya daha fazla başlık ekleyin.</span><span class="sxs-lookup"><span data-stu-id="c8ec0-154">In the settings for the banner module, add one or more banner messages.</span></span> <span data-ttu-id="c8ec0-155">Her iletinin bir bağlantı ile birlikte bir metni olabilir.</span><span class="sxs-lookup"><span data-stu-id="c8ec0-155">Each message can have text together with a link.</span></span> <span data-ttu-id="c8ec0-156">Modülü daha fazla özelleştirmek için diğer özellikleri düzenleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="c8ec0-156">You can edit the other properties to customize the module further.</span></span>
1. <span data-ttu-id="c8ec0-157">**Kaydet**'i seçin ve ardından sayfayı önizlemek için **Önizleme**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="c8ec0-157">Select **Save**, and then select **Preview** to preview the page.</span></span> <span data-ttu-id="c8ec0-158">Sayfanın üst kısmında, eklediğiniz metni içeren bir uyarı görmelisiniz.</span><span class="sxs-lookup"><span data-stu-id="c8ec0-158">At the top of the page, you should see an alert that shows the text that you added.</span></span>
1. <span data-ttu-id="c8ec0-159">Sayfayı iade etmek için **Düzenlemeyi bitir**'i seçin, ardından yayımlamak için **Yayımla**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="c8ec0-159">Select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span>

> [!NOTE]
> <span data-ttu-id="c8ec0-160">Bir promosyon başlığı genellikle sayfa üstbilgisi yuvasında veya alt başlık yuvasında kullanılır.</span><span class="sxs-lookup"><span data-stu-id="c8ec0-160">A promo banner is typically used in the page header slot or a subheader slot.</span></span>


## <a name="additional-resources"></a><span data-ttu-id="c8ec0-161">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="c8ec0-161">Additional resources</span></span>

[<span data-ttu-id="c8ec0-162">Modül kitaplığına genel bakış</span><span class="sxs-lookup"><span data-stu-id="c8ec0-162">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="c8ec0-163">Döngü modülü</span><span class="sxs-lookup"><span data-stu-id="c8ec0-163">Carousel module</span></span>](add-carousel.md)

[<span data-ttu-id="c8ec0-164">Metin bloğu modülü</span><span class="sxs-lookup"><span data-stu-id="c8ec0-164">Text block module</span></span>](add-content-rich-block.md)

[<span data-ttu-id="c8ec0-165">İçerik bloğu modülü</span><span class="sxs-lookup"><span data-stu-id="c8ec0-165">Content block module</span></span>](add-hero-module.md)

[<span data-ttu-id="c8ec0-166">Video oynatıcı modülü</span><span class="sxs-lookup"><span data-stu-id="c8ec0-166">Video player module</span></span>](add-video-player.md)
