---
title: Sosyal içerik paylaşım modülü
description: Bu konu sosyal içerik paylaşım modüllerini kapsamaktadır ve Microsoft Dynamics 365 Commerce'ün site sayfalarına nasıl ekleneceğini açıklamaktadır.
author: anupamar-ms
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: c34410a8c817de9fed350bf2cd2dd918a37c230f
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/31/2021
ms.locfileid: "5795369"
---
# <a name="social-share-module"></a><span data-ttu-id="179b3-103">Sosyal içerik paylaşım modülü</span><span class="sxs-lookup"><span data-stu-id="179b3-103">Social share module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="179b3-104">Bu konu sosyal içerik paylaşım modüllerini kapsamaktadır ve Microsoft Dynamics 365 Commerce'ün site sayfalarına nasıl ekleneceğini açıklamaktadır.</span><span class="sxs-lookup"><span data-stu-id="179b3-104">This topic covers social share modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="179b3-105">Sosyal içerik paylaşımı modülleri, kullanıcıların e-ticaret sitesi sayfası URL'lerini Facebook, Twitter, Pinterest ve LinkedIn gibi sosyal medya üzerinde paylaşmasına olanak tanır.</span><span class="sxs-lookup"><span data-stu-id="179b3-105">Social share modules allow users to share e-Commerce site page URLs on social media such as Facebook, Twitter, Pinterest, and LinkedIn.</span></span> <span data-ttu-id="179b3-106">Site sayfası URL'Leri e-posta yoluyla da paylaşılabilir.</span><span class="sxs-lookup"><span data-stu-id="179b3-106">Site page URLs can also be shared via email.</span></span> <span data-ttu-id="179b3-107">Sosyal içerik paylaşımı modülleri, kullanıcıların ürün bilgilerini paylaşmasına yardımcı olmak için ürün ayrıntıları sayfalarında (PDP'ler) kullanılır.</span><span class="sxs-lookup"><span data-stu-id="179b3-107">Social share modules are commonly used on product details pages (PDPs) to help users share product information.</span></span>

<span data-ttu-id="179b3-108">Her sosyal içerik paylaşım modülü sosyal içerik paylaşımı öğe modülleri için bir kapsayıcıdır.</span><span class="sxs-lookup"><span data-stu-id="179b3-108">Each social share module is a container for social share item modules.</span></span> <span data-ttu-id="179b3-109">Her sosyal içerik paylaşımı öğe modülü belirli bir sosyal medya sitesini işaret etmek üzere yapılandırılabilir.</span><span class="sxs-lookup"><span data-stu-id="179b3-109">Each social share item module can be configured to point to a specific social media site.</span></span> <span data-ttu-id="179b3-110">Facebook, Twitter, Pinterest, LinkedIn ve e-posta ile tümleştirme, hazırda desteklenmektedir.</span><span class="sxs-lookup"><span data-stu-id="179b3-110">Integration with Facebook, Twitter, Pinterest, LinkedIn, and email is supported out of the box.</span></span> <span data-ttu-id="179b3-111">Bir site kullanıcısı bir sosyal medya sembolünü seçtiğinde, ilgili sosyal medya sitesi için bir HTML iframe başlatılır.</span><span class="sxs-lookup"><span data-stu-id="179b3-111">When a site user selects a social media symbol, an HTML iframe is launched for the respective social media site.</span></span> <span data-ttu-id="179b3-112">iframe içinde kullanıcı oturum açarak, görüntüledikleri sayfa içeriğini paylaşabilir.</span><span class="sxs-lookup"><span data-stu-id="179b3-112">Within the iframe, the user can sign in and post the page content that they were viewing.</span></span>

<span data-ttu-id="179b3-113">Her sosyal medya platformu tanımlama bilgilerini izleyebilir, bu nedenle bu modül site kullanıcılarının tanımlama bilgisi onayı bildirim iletisini kabul etmesini gerektirir.</span><span class="sxs-lookup"><span data-stu-id="179b3-113">Each social media platform may track cookies, so this module requires site users to accept the cookie consent notification message.</span></span> <span data-ttu-id="179b3-114">Tanımlama bilgisi izni verilmediğinde, modül sayfada gizlenir.</span><span class="sxs-lookup"><span data-stu-id="179b3-114">When cookie consent is not accepted, the module will be hidden on the page.</span></span> <span data-ttu-id="179b3-115">Daha fazla bilgi için bkz. [Tanımlama bilgisi uyumluluğu](cookie-compliance.md).</span><span class="sxs-lookup"><span data-stu-id="179b3-115">For more information, see [Cookie compliance](cookie-compliance.md).</span></span>

<span data-ttu-id="179b3-116">Aşağıdaki çizimde, ürün ayrıntıları sayfasında kullanılan sosyal içerik paylaşım modülüne bir örnek gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="179b3-116">The following illustration highlights an example of a social share module used on a product details page.</span></span>

![Sosyal içerik paylaşım modülü örneği](./media/ecommerce-socialshare.png)

## <a name="social-share-module-properties"></a><span data-ttu-id="179b3-118">Sosyal içerik paylaşım modülü özellikleri</span><span class="sxs-lookup"><span data-stu-id="179b3-118">Social share module properties</span></span>

| <span data-ttu-id="179b3-119">Özellik adı</span><span class="sxs-lookup"><span data-stu-id="179b3-119">Property name</span></span>             | <span data-ttu-id="179b3-120">Değer</span><span class="sxs-lookup"><span data-stu-id="179b3-120">Value</span></span>                 | <span data-ttu-id="179b3-121">Tanım</span><span class="sxs-lookup"><span data-stu-id="179b3-121">Description</span></span> |
|---------------------------|-----------------------|-------------|
| <span data-ttu-id="179b3-122">Açıklama yazısı</span><span class="sxs-lookup"><span data-stu-id="179b3-122">Caption</span></span>                  | <span data-ttu-id="179b3-123">Metin</span><span class="sxs-lookup"><span data-stu-id="179b3-123">Text</span></span> | <span data-ttu-id="179b3-124">Bu özellik modül için bir açıklamalı alt yazı belirtir.</span><span class="sxs-lookup"><span data-stu-id="179b3-124">This property specifies a caption for the module.</span></span> |
| <span data-ttu-id="179b3-125">Hizalama</span><span class="sxs-lookup"><span data-stu-id="179b3-125">Orientation</span></span> | <span data-ttu-id="179b3-126">**Yatay** veya **Dikey**</span><span class="sxs-lookup"><span data-stu-id="179b3-126">**Horizontal** or **Vertical**</span></span>  | <span data-ttu-id="179b3-127">Bu özellik, sosyal medya öğelerinin yerleşim yönünü tanımlar.</span><span class="sxs-lookup"><span data-stu-id="179b3-127">This property defines the layout orientation for the social media items.</span></span> |

## <a name="social-share-item-module-properties"></a><span data-ttu-id="179b3-128">Sosyal içerik paylaşım öğesi modülü özellikleri</span><span class="sxs-lookup"><span data-stu-id="179b3-128">Social share item module properties</span></span>
| <span data-ttu-id="179b3-129">Özellik adı</span><span class="sxs-lookup"><span data-stu-id="179b3-129">Property name</span></span>             | <span data-ttu-id="179b3-130">Değer</span><span class="sxs-lookup"><span data-stu-id="179b3-130">Value</span></span>                 | <span data-ttu-id="179b3-131">Tanım</span><span class="sxs-lookup"><span data-stu-id="179b3-131">Description</span></span> |
|---------------------------|-----------------------|-------------|
| <span data-ttu-id="179b3-132">Sosyal medya</span><span class="sxs-lookup"><span data-stu-id="179b3-132">Social media</span></span>              | <span data-ttu-id="179b3-133">**Facebook**, **Twitter**, **Pinterest**, **LinkedIn**, **Posta**</span><span class="sxs-lookup"><span data-stu-id="179b3-133">**Facebook**, **Twitter**, **Pinterest**, **LinkedIn**, **Mail**</span></span> | <span data-ttu-id="179b3-134">Sosyal medya platformlarının listesinin bulunduğu bir açılan menü.</span><span class="sxs-lookup"><span data-stu-id="179b3-134">A drop-down menu with a list of social media platforms.</span></span> |
| <span data-ttu-id="179b3-135">Simge</span><span class="sxs-lookup"><span data-stu-id="179b3-135">Icon</span></span> |<span data-ttu-id="179b3-136">Görüntü</span><span class="sxs-lookup"><span data-stu-id="179b3-136">Image</span></span>    | <span data-ttu-id="179b3-137">Bu, ilgili sosyal medyada gösterilecek resim olacaktır.</span><span class="sxs-lookup"><span data-stu-id="179b3-137">This will be the image that will be shown for the respective social media.</span></span> <span data-ttu-id="179b3-138">En iyi uygulama olarak, her bir platformda kullanılacak resim için sosyal medya platformunun SDK'sine başvurun.</span><span class="sxs-lookup"><span data-stu-id="179b3-138">As a best practice, refer to the social media platform's SDK for the recommended image to use for each platform.</span></span> |

## <a name="add-a-social-share-module-to-a-buy-box-module"></a><span data-ttu-id="179b3-139">Satın al kutusu modülüne bir sosyal içerik paylaşım modülü ekleme</span><span class="sxs-lookup"><span data-stu-id="179b3-139">Add a social share module to a buy box module</span></span>

<span data-ttu-id="179b3-140">Satın al kutusu modülüne bir sosyal içerik paylaşım modülü eklemek için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="179b3-140">To add a social share module to a buy box module, follow these steps.</span></span>

1. <span data-ttu-id="179b3-141">Fabrikam sitesinde, **Sayfalar**'ı seçin ve sonra ürün ayrıntıları sayfasını açmak için **DefaultPDP** sayfasını seçin.</span><span class="sxs-lookup"><span data-stu-id="179b3-141">In the Fabrikam site, select **Pages**, and then select the **DefaultPDP** page to open the product details page.</span></span> 
1. <span data-ttu-id="179b3-142">**Buybox (gerekli)** yuvasında üç nokta (**...**) düğmesini seçin ve **Modül Ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="179b3-142">In the **Buybox (required)** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="179b3-143">**Modül Ekle** iletişim kutusunda **Sosyal İçerik Paylaşım** modülünü seçin ve **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="179b3-143">In the **Add Module** dialog box, select the **Social Share** module, and then select **OK**.</span></span>
1. <span data-ttu-id="179b3-144">**Sosyal İçerik Paylaşım** yuvasında üç nokta (**...**) düğmesini seçin ve **Modül Ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="179b3-144">In the **Social Share** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="179b3-145">**Modül Ekle** iletişim kutusunda **SocialShare** modülünü seçin ve **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="179b3-145">In the **Add Module** dialog box, select the **SocialShare** module, and then select **OK**.</span></span>
1. <span data-ttu-id="179b3-146">**Socialshare** modülünün özellikler bölmesinde, **Yönlendirme** altında **Yatay**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="179b3-146">In the properties pane of the **SocialShare** module, under **Orientation**, select **Horizontal**.</span></span> <span data-ttu-id="179b3-147">Gerektiğinde bir açıklamalı alt yazı ekleyin.</span><span class="sxs-lookup"><span data-stu-id="179b3-147">Add a caption as needed.</span></span>
1. <span data-ttu-id="179b3-148">**SocialShare** yuvasında üç nokta (**...**) düğmesini seçin ve **Modül Ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="179b3-148">In the **SocialShare** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="179b3-149">**Modül Ekle** iletişim kutusunda **SocialShareItem** modülünü seçin ve **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="179b3-149">In the **Add Module** dialog box, select the **SocialShareItem** module, and then select **OK**.</span></span>
1. <span data-ttu-id="179b3-150">**SocialShareItem** modülünün özellikler bölmesinde, **Sosyal Medya** altında **Facebook** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="179b3-150">In the properties pane of the **SocialShareItem** module, under **Social Media**, select **Facebook**.</span></span>
1. <span data-ttu-id="179b3-151">**SocialShareItem** modülünün özellikler bölmesinde, **Simge** altında **+Resim ekleyin** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="179b3-151">In the properties pane of the **SocialShareItem** module, under **Icon**, select **+ Add an image**.</span></span>
1. <span data-ttu-id="179b3-152">**Ortam Seçicisi** iletişim kutusunda Facebook logo resmini seçin ve **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="179b3-152">In the **Media Picker** dialog box, select the Facebook logo image, and then select **OK**.</span></span> <span data-ttu-id="179b3-153">Herhangi bir Facebook logo resmi yoksa karşıya yüklemek için **Yeni ortam öğesini karşıya yükle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="179b3-153">If no Facebook logo image is present, select **Upload new media item** to upload one.</span></span>
1. <span data-ttu-id="179b3-154">Gerektiğinde ek **SocialShareItem** modülleri ekleyin ve yapılandırın.</span><span class="sxs-lookup"><span data-stu-id="179b3-154">Add and configure additional **SocialShareItem** modules as needed.</span></span>
1. <span data-ttu-id="179b3-155">**Kaydet**'i seçin ve ardından sayfayı önizlemek için **Önizleme**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="179b3-155">Select **Save**, and then select **Preview** to preview the page.</span></span> <span data-ttu-id="179b3-156">Sayfada sosyal içerik paylaşım modülü gösterilir.</span><span class="sxs-lookup"><span data-stu-id="179b3-156">The page will show the social share module.</span></span>
1. <span data-ttu-id="179b3-157">Sayfayı iade etmek için **Düzenlemeyi bitir**'i seçin, ardından yayımlamak için **Yayımla**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="179b3-157">Select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="179b3-158">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="179b3-158">Additional resources</span></span>

[<span data-ttu-id="179b3-159">Modül kitaplığına genel bakış</span><span class="sxs-lookup"><span data-stu-id="179b3-159">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="179b3-160">Satın alma kutusu modülü</span><span class="sxs-lookup"><span data-stu-id="179b3-160">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="179b3-161">Tanımlama bilgisi uyumluluğu</span><span class="sxs-lookup"><span data-stu-id="179b3-161">Cookie compliance</span></span>](cookie-compliance.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]