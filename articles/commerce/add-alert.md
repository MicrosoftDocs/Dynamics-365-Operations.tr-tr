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
ms.openlocfilehash: 0b9325ef31fc61d451584930b09c2039156c0c05
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5206595"
---
# <a name="promo-banner-module"></a><span data-ttu-id="68a6e-103">Promosyon başlık modülü</span><span class="sxs-lookup"><span data-stu-id="68a6e-103">Promo banner module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="68a6e-104">Bu konu promosyon başlığı modüllerini kapsamaktadır ve Microsoft Dynamics 365 Commerce'un site sayfalarına nasıl ekleneceğini açıklamaktadır.</span><span class="sxs-lookup"><span data-stu-id="68a6e-104">This topic covers promo banner modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="68a6e-105">Promosyon başlığı modülleri, bir sayfadaki satır içi bilgilendirme iletilerini göstermekte kullanılır.</span><span class="sxs-lookup"><span data-stu-id="68a6e-105">Promo banner modules are used to show inline informational messages on a page.</span></span> <span data-ttu-id="68a6e-106">Bir e-ticaret sitesinin tüm sayfalarında görünen site çapında yükseltmeleri göstermek için kullanılabilirler.</span><span class="sxs-lookup"><span data-stu-id="68a6e-106">They can be used to show site-wide promotions that appear on all pages of an e-Commerce site.</span></span> 

<span data-ttu-id="68a6e-107">Promosyon başlığı modülleri bir metin iletisini ve bir bağlantıyı destekler.</span><span class="sxs-lookup"><span data-stu-id="68a6e-107">Promo banner modules support a text message and a link.</span></span> <span data-ttu-id="68a6e-108">Bir promosyon başlık modülüne birden fazla ileti eklenirse, müşterilerin tüm iletiler arasında dolaşmasına olanak veren bir döner başlığı olur.</span><span class="sxs-lookup"><span data-stu-id="68a6e-108">If multiple messages are added to a promo banner module, it becomes a rotating carousel banner that lets customers cycle through all the messages.</span></span> 

<span data-ttu-id="68a6e-109">Promosyon başlığı, içerik yönetimi sistemindeki (CMS) veriler tarafından yönlendiriliyor ve herhangi bir sayfaya konabilir.</span><span class="sxs-lookup"><span data-stu-id="68a6e-109">Promo banner modules are driven by data from the content management system (CMS) and can be put on any page.</span></span>

## <a name="usage-examples-of-promo-banners-in-e-commerce"></a><span data-ttu-id="68a6e-110">E-ticaret'daki promosyon başlık sayfaları için kullanım örnekleri</span><span class="sxs-lookup"><span data-stu-id="68a6e-110">Usage examples of promo banners in e-Commerce</span></span>

<span data-ttu-id="68a6e-111">Promosyon başlık sayfaları site başlığında, aşağıdaki örneklerde olduğu gibi, site çapında yükseltmeleri veya iletileri göstermek amacıyla kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="68a6e-111">Promo banners can be used in the site header to show site-wide promotions or messages, as in the following examples.</span></span>

<span data-ttu-id="68a6e-112">"Yıllık satış, 10 gün içinde biter"</span><span class="sxs-lookup"><span data-stu-id="68a6e-112">"Annual sale ends in 10 days"</span></span>

<span data-ttu-id="68a6e-113">"Okul satışı ile büyük bir tasarruf yapın.</span><span class="sxs-lookup"><span data-stu-id="68a6e-113">"Save big with back to school sale.</span></span> <span data-ttu-id="68a6e-114">Şimdi alışveriş yap."</span><span class="sxs-lookup"><span data-stu-id="68a6e-114">Shop Now."</span></span>

<span data-ttu-id="68a6e-115">"Şükran günü İNDİRİM alışverişi yap!"</span><span class="sxs-lookup"><span data-stu-id="68a6e-115">"Shop for Thanksgiving SALE!"</span></span> 

<span data-ttu-id="68a6e-116">Aşağıdaki resimde, bir promosyon başlığı örneği gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="68a6e-116">The following image shows an example of a promo banner.</span></span>

![Promosyon başlık modülü örneği](./media/ecommerce-Promobanner.PNG)

## <a name="promo-banner-module-properties"></a><span data-ttu-id="68a6e-118">Promosyon başlığı modülü özellikleri</span><span class="sxs-lookup"><span data-stu-id="68a6e-118">Promo banner module properties</span></span>

| <span data-ttu-id="68a6e-119">Özellik adı</span><span class="sxs-lookup"><span data-stu-id="68a6e-119">Property name</span></span>             | <span data-ttu-id="68a6e-120">Değer</span><span class="sxs-lookup"><span data-stu-id="68a6e-120">Value</span></span>                              | <span data-ttu-id="68a6e-121">Tanım</span><span class="sxs-lookup"><span data-stu-id="68a6e-121">Description</span></span> |
|---------------------------|------------------------------------|-------------|
| <span data-ttu-id="68a6e-122">Başlık iletileri</span><span class="sxs-lookup"><span data-stu-id="68a6e-122">Banner messages</span></span>           | <span data-ttu-id="68a6e-123">Metin ve bağlantılar</span><span class="sxs-lookup"><span data-stu-id="68a6e-123">Text and links</span></span>                     | <span data-ttu-id="68a6e-124">Metin ve bağlantılar dizisi.</span><span class="sxs-lookup"><span data-stu-id="68a6e-124">An array of text and links.</span></span> |
| <span data-ttu-id="68a6e-125">Otomatik yürüt</span><span class="sxs-lookup"><span data-stu-id="68a6e-125">Autoplay</span></span>                  | <span data-ttu-id="68a6e-126">**Doğru** veya **yanlış**</span><span class="sxs-lookup"><span data-stu-id="68a6e-126">**True** or **False**</span></span>              | <span data-ttu-id="68a6e-127">Birden fazla ileti yapılandırılmışsa, iletilerin otomatik olarak açılıp eklenmesini belirten bir değer.</span><span class="sxs-lookup"><span data-stu-id="68a6e-127">A value that indicates whether messages are automatically cycled through, if multiple messages are configured.</span></span> |
| <span data-ttu-id="68a6e-128">Slayt geçiş aralığı</span><span class="sxs-lookup"><span data-stu-id="68a6e-128">Slide transition interval</span></span> | <span data-ttu-id="68a6e-129">Milisaniyelerin sayısı (MS)</span><span class="sxs-lookup"><span data-stu-id="68a6e-129">A number of milliseconds (ms)</span></span>      | <span data-ttu-id="68a6e-130">İletiler arasında geçiş yapmak için kullanılan aralık.</span><span class="sxs-lookup"><span data-stu-id="68a6e-130">The interval that is used to cycle through messages.</span></span> |
| <span data-ttu-id="68a6e-131">Kapatmaya izin ver</span><span class="sxs-lookup"><span data-stu-id="68a6e-131">Allow dismiss</span></span>             | <span data-ttu-id="68a6e-132">**Doğru** veya **yanlış**</span><span class="sxs-lookup"><span data-stu-id="68a6e-132">**True** or **False**</span></span>              | <span data-ttu-id="68a6e-133">Değer **doğru** olarak ayarlanırsa, müşteriler uyarıyı yok edebilir.</span><span class="sxs-lookup"><span data-stu-id="68a6e-133">If the value is set to **True**, customers can dismiss the alert.</span></span> |
| <span data-ttu-id="68a6e-134">Carusel kolu göster</span><span class="sxs-lookup"><span data-stu-id="68a6e-134">Show carousel flipper</span></span>     | <span data-ttu-id="68a6e-135">**Doğru** veya **yanlış**</span><span class="sxs-lookup"><span data-stu-id="68a6e-135">**True** or **False**</span></span>              | <span data-ttu-id="68a6e-136">Döner değiştiricilerin gösterilip gösterilmeyeceğini belirten ve müşterilerin birden çok Başlık öğelerini el ile dolaşabilmesi için bir değer.</span><span class="sxs-lookup"><span data-stu-id="68a6e-136">A value that indicates whether the carousel flippers should be shown, so that customers can manually cycle through multiple banner items.</span></span> |
| <span data-ttu-id="68a6e-137">Metin hizalama</span><span class="sxs-lookup"><span data-stu-id="68a6e-137">Text alignment</span></span>            | <span data-ttu-id="68a6e-138">**Sağ**, **Sol** veya **Orta**</span><span class="sxs-lookup"><span data-stu-id="68a6e-138">**Right**, **Left**, or **Center**</span></span> | <span data-ttu-id="68a6e-139">Promosyon başlık modülünde metin hizalaması.</span><span class="sxs-lookup"><span data-stu-id="68a6e-139">The text alignment in the promo banner module.</span></span> |
| <span data-ttu-id="68a6e-140">Bağla</span><span class="sxs-lookup"><span data-stu-id="68a6e-140">Link</span></span>                      | <span data-ttu-id="68a6e-141">Bir URL</span><span class="sxs-lookup"><span data-stu-id="68a6e-141">A URL</span></span>                              | <span data-ttu-id="68a6e-142">İsteğe bağlı bağlantı için URL.</span><span class="sxs-lookup"><span data-stu-id="68a6e-142">The URL for an optional link.</span></span> |

## <a name="add-a-promo-banner-module-to-a-page"></a><span data-ttu-id="68a6e-143">Bir sayfaya bir promosyon başlığı ekle</span><span class="sxs-lookup"><span data-stu-id="68a6e-143">Add a promo banner module to a page</span></span> 

<span data-ttu-id="68a6e-144">Bir sayfaya bir promosyon başlığı modülü eklemek ve gerekli özellikleri ayarlamak için şu adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="68a6e-144">To add a promo banner module to a page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="68a6e-145">Bir yeni şablonu oluşturmak için **Şablonlar**'a gidin ve **Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="68a6e-145">Go to **Templates**, and select **New** to create a new template.</span></span>
1. <span data-ttu-id="68a6e-146">**Yeni Şablon** iletişim kutusunda **Şablon adı** altında, **Promosyon başlığı şablonu**'nu girin ve **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="68a6e-146">In the **New Template** dialog box, under **Template Name**, enter **Promo banner template**, and then select **OK**.</span></span>
1. <span data-ttu-id="68a6e-147">**Sayfa Anahattı** altında, bir **Varsayılan sayfa** modülünü **Gövde** yuvasına ekleyin.</span><span class="sxs-lookup"><span data-stu-id="68a6e-147">Under **Page Outline**, add a **Default page** module to the **Body** slot.</span></span> 
1. <span data-ttu-id="68a6e-148">Şablonu iade etmek için **Düzenlemeyi bitir**'i seçin, ardından yayımlamak için **Yayımla**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="68a6e-148">Select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span> 
1. <span data-ttu-id="68a6e-149">**Promosyon başlığı sayfası** adlı bir sayfa oluşturmak için yeni oluşturduğunuz uyarı şablonunu kullanın.</span><span class="sxs-lookup"><span data-stu-id="68a6e-149">Use the template that you just created to create a page that is named **Promo banner page**.</span></span> 
1. <span data-ttu-id="68a6e-150">Yeni sayfanın **ana** yuvasına bir konteyner modülü ekleyin.</span><span class="sxs-lookup"><span data-stu-id="68a6e-150">In the **Main** slot of the new page, add a container module.</span></span> 
1. <span data-ttu-id="68a6e-151">Sağdaki panoda, **Genişlik** değerini **Konteyneri doldur**'a ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="68a6e-151">In the pane on the right, set the **Width** value to **Fill Container**.</span></span>
1. <span data-ttu-id="68a6e-152">**Sayfa Anahattı** altında, bir promosyon başlığı modlünü konteyner modülüne ekleyin.</span><span class="sxs-lookup"><span data-stu-id="68a6e-152">Under **Page Outline**, add a promo banner module to the container module.</span></span>
1. <span data-ttu-id="68a6e-153">Başlık modülünün ayarlarında bir veya daha fazla başlık ekleyin.</span><span class="sxs-lookup"><span data-stu-id="68a6e-153">In the settings for the banner module, add one or more banner messages.</span></span> <span data-ttu-id="68a6e-154">Her iletinin bir bağlantı ile birlikte bir metni olabilir.</span><span class="sxs-lookup"><span data-stu-id="68a6e-154">Each message can have text together with a link.</span></span> <span data-ttu-id="68a6e-155">Modülü daha fazla özelleştirmek için diğer özellikleri düzenleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="68a6e-155">You can edit the other properties to customize the module further.</span></span>
1. <span data-ttu-id="68a6e-156">**Kaydet**'i seçin ve ardından sayfayı önizlemek için **Önizleme**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="68a6e-156">Select **Save**, and then select **Preview** to preview the page.</span></span> <span data-ttu-id="68a6e-157">Sayfanın üst kısmında, eklediğiniz metni içeren bir uyarı görmelisiniz.</span><span class="sxs-lookup"><span data-stu-id="68a6e-157">At the top of the page, you should see an alert that shows the text that you added.</span></span>
1. <span data-ttu-id="68a6e-158">Sayfayı iade etmek için **Düzenlemeyi bitir**'i seçin, ardından yayımlamak için **Yayımla**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="68a6e-158">Select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span>

> [!NOTE]
> <span data-ttu-id="68a6e-159">Bir promosyon başlığı genellikle sayfa üstbilgisi yuvasında veya alt başlık yuvasında kullanılır.</span><span class="sxs-lookup"><span data-stu-id="68a6e-159">A promo banner is typically used in the page header slot or a subheader slot.</span></span>


## <a name="additional-resources"></a><span data-ttu-id="68a6e-160">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="68a6e-160">Additional resources</span></span>

[<span data-ttu-id="68a6e-161">Modül kitaplığına genel bakış</span><span class="sxs-lookup"><span data-stu-id="68a6e-161">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="68a6e-162">Döngü modülü</span><span class="sxs-lookup"><span data-stu-id="68a6e-162">Carousel module</span></span>](add-carousel.md)

[<span data-ttu-id="68a6e-163">Metin bloğu modülü</span><span class="sxs-lookup"><span data-stu-id="68a6e-163">Text block module</span></span>](add-content-rich-block.md)

[<span data-ttu-id="68a6e-164">İçerik bloğu modülü</span><span class="sxs-lookup"><span data-stu-id="68a6e-164">Content block module</span></span>](add-hero-module.md)

[<span data-ttu-id="68a6e-165">Video oynatıcı modülü</span><span class="sxs-lookup"><span data-stu-id="68a6e-165">Video player module</span></span>](add-video-player.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]