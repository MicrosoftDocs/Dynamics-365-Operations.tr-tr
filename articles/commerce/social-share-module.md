---
title: Sosyal içerik paylaşım modülü
description: Bu konu sosyal içerik paylaşım modüllerini kapsamaktadır ve Microsoft Dynamics 365 Commerce'ün site sayfalarına nasıl ekleneceğini açıklamaktadır.
author: anupamar-ms
manager: annbe
ms.date: 08/31/2020
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
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: 0fd81aa1f4b1358528f0135c1334dc7b4ac4461f
ms.sourcegitcommit: 420b9e538f706178f8e1f2786e02f4f400bf2336
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/02/2020
ms.locfileid: "3761431"
---
# <a name="social-share-module"></a><span data-ttu-id="28fc2-103">Sosyal içerik paylaşım modülü</span><span class="sxs-lookup"><span data-stu-id="28fc2-103">Social share module</span></span>

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

<span data-ttu-id="28fc2-104">Bu konu sosyal içerik paylaşım modüllerini kapsamaktadır ve Microsoft Dynamics 365 Commerce'ün site sayfalarına nasıl ekleneceğini açıklamaktadır.</span><span class="sxs-lookup"><span data-stu-id="28fc2-104">This topic covers social share modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="28fc2-105">Genel bakış</span><span class="sxs-lookup"><span data-stu-id="28fc2-105">Overview</span></span>

<span data-ttu-id="28fc2-106">Sosyal içerik paylaşımı modülleri, kullanıcıların e-ticaret sitesi sayfası URL'lerini Facebook, Twitter, Pinterest ve LinkedIn gibi sosyal medya üzerinde paylaşmasına olanak tanır.</span><span class="sxs-lookup"><span data-stu-id="28fc2-106">Social share modules allow users to share e-Commerce site page URLs on social media such as Facebook, Twitter, Pinterest, and LinkedIn.</span></span> <span data-ttu-id="28fc2-107">Site sayfası URL'Leri e-posta yoluyla da paylaşılabilir.</span><span class="sxs-lookup"><span data-stu-id="28fc2-107">Site page URLs can also be shared via email.</span></span> <span data-ttu-id="28fc2-108">Sosyal içerik paylaşımı modülleri, kullanıcıların ürün bilgilerini paylaşmasına yardımcı olmak için ürün ayrıntıları sayfalarında (PDP'ler) kullanılır.</span><span class="sxs-lookup"><span data-stu-id="28fc2-108">Social share modules are commonly used on product details pages (PDPs) to help users share product information.</span></span>

<span data-ttu-id="28fc2-109">Her sosyal içerik paylaşım modülü sosyal içerik paylaşımı öğe modülleri için bir kapsayıcıdır.</span><span class="sxs-lookup"><span data-stu-id="28fc2-109">Each social share module is a container for social share item modules.</span></span> <span data-ttu-id="28fc2-110">Her sosyal içerik paylaşımı öğe modülü belirli bir sosyal medya sitesini işaret etmek üzere yapılandırılabilir.</span><span class="sxs-lookup"><span data-stu-id="28fc2-110">Each social share item module can be configured to point to a specific social media site.</span></span> <span data-ttu-id="28fc2-111">Facebook, Twitter, Pinterest, LinkedIn ve e-posta ile tümleştirme, hazırda desteklenmektedir.</span><span class="sxs-lookup"><span data-stu-id="28fc2-111">Integration with Facebook, Twitter, Pinterest, LinkedIn, and email is supported out of the box.</span></span> <span data-ttu-id="28fc2-112">Bir site kullanıcısı bir sosyal medya sembolünü seçtiğinde, ilgili sosyal medya sitesi için bir HTML iFrame başlatılır.</span><span class="sxs-lookup"><span data-stu-id="28fc2-112">When a site user selects a social media symbol, an HTML iframe is launched for the respective social media site.</span></span> <span data-ttu-id="28fc2-113">iFrame içinde kullanıcı oturum açarak, görüntüledikleri sayfa içeriğini paylaşabilir.</span><span class="sxs-lookup"><span data-stu-id="28fc2-113">Within the iframe, the user can sign in and post the page content that they were viewing.</span></span>

<span data-ttu-id="28fc2-114">Her sosyal medya platformu tanımlama bilgilerini izleyebilir, bu nedenle bu modül site kullanıcılarının tanımlama bilgisi onayı bildirim iletisini kabul etmesini gerektirir.</span><span class="sxs-lookup"><span data-stu-id="28fc2-114">Each social media platform may track cookies, so this module requires site users to accept the cookie consent notification message.</span></span> <span data-ttu-id="28fc2-115">Tanımlama bilgisi izni verilmediğinde, modül sayfada gizlenir.</span><span class="sxs-lookup"><span data-stu-id="28fc2-115">When cookie consent is not accepted, the module will be hidden on the page.</span></span> <span data-ttu-id="28fc2-116">Daha fazla bilgi için bkz. [Tanımlama bilgisi uyumluluğu](cookie-compliance.md).</span><span class="sxs-lookup"><span data-stu-id="28fc2-116">For more information, see [Cookie compliance](cookie-compliance.md).</span></span>

<span data-ttu-id="28fc2-117">Aşağıdaki çizimde, ürün ayrıntıları sayfasında kullanılan sosyal içerik paylaşım modülüne bir örnek gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="28fc2-117">The following illustration highlights an example of a social share module used on a product details page.</span></span>

![Sosyal içerik paylaşım modülü örneği](./media/ecommerce-socialshare.png)

## <a name="social-share-module-properties"></a><span data-ttu-id="28fc2-119">Sosyal içerik paylaşım modülü özellikleri</span><span class="sxs-lookup"><span data-stu-id="28fc2-119">Social share module properties</span></span>

| <span data-ttu-id="28fc2-120">Özellik adı</span><span class="sxs-lookup"><span data-stu-id="28fc2-120">Property name</span></span>             | <span data-ttu-id="28fc2-121">Değer</span><span class="sxs-lookup"><span data-stu-id="28fc2-121">Value</span></span>                 | <span data-ttu-id="28fc2-122">Tanım</span><span class="sxs-lookup"><span data-stu-id="28fc2-122">Description</span></span> |
|---------------------------|-----------------------|-------------|
| <span data-ttu-id="28fc2-123">Açıklama yazısı</span><span class="sxs-lookup"><span data-stu-id="28fc2-123">Caption</span></span>                  | <span data-ttu-id="28fc2-124">Metin</span><span class="sxs-lookup"><span data-stu-id="28fc2-124">Text</span></span> | <span data-ttu-id="28fc2-125">Bu özellik modül için bir açıklamalı alt yazı belirtir.</span><span class="sxs-lookup"><span data-stu-id="28fc2-125">This property specifies a caption for the module.</span></span> |
| <span data-ttu-id="28fc2-126">Hizalama</span><span class="sxs-lookup"><span data-stu-id="28fc2-126">Orientation</span></span> | <span data-ttu-id="28fc2-127">**Yatay** veya **Dikey**</span><span class="sxs-lookup"><span data-stu-id="28fc2-127">**Horizontal** or **Vertical**</span></span>  | <span data-ttu-id="28fc2-128">Bu özellik, sosyal medya öğelerinin yerleşim yönünü tanımlar.</span><span class="sxs-lookup"><span data-stu-id="28fc2-128">This property defines the layout orientation for the social media items.</span></span> |

## <a name="social-share-item-module-properties"></a><span data-ttu-id="28fc2-129">Sosyal içerik paylaşım öğesi modülü özellikleri</span><span class="sxs-lookup"><span data-stu-id="28fc2-129">Social share item module properties</span></span>
| <span data-ttu-id="28fc2-130">Özellik adı</span><span class="sxs-lookup"><span data-stu-id="28fc2-130">Property name</span></span>             | <span data-ttu-id="28fc2-131">Değer</span><span class="sxs-lookup"><span data-stu-id="28fc2-131">Value</span></span>                 | <span data-ttu-id="28fc2-132">Tanım</span><span class="sxs-lookup"><span data-stu-id="28fc2-132">Description</span></span> |
|---------------------------|-----------------------|-------------|
| <span data-ttu-id="28fc2-133">Sosyal medya</span><span class="sxs-lookup"><span data-stu-id="28fc2-133">Social media</span></span>              | <span data-ttu-id="28fc2-134">**Facebook**, **Twitter**, **Pinterest**, **LinkedIn**, **Posta**</span><span class="sxs-lookup"><span data-stu-id="28fc2-134">**Facebook**, **Twitter**, **Pinterest**, **LinkedIn**, **Mail**</span></span> | <span data-ttu-id="28fc2-135">Sosyal medya platformlarının listesinin bulunduğu bir açılan menü.</span><span class="sxs-lookup"><span data-stu-id="28fc2-135">A drop-down menu with a list of social media platforms.</span></span> |
| <span data-ttu-id="28fc2-136">Simge</span><span class="sxs-lookup"><span data-stu-id="28fc2-136">Icon</span></span> |<span data-ttu-id="28fc2-137">Görüntü</span><span class="sxs-lookup"><span data-stu-id="28fc2-137">Image</span></span>    | <span data-ttu-id="28fc2-138">Bu, ilgili sosyal medyada gösterilecek resim olacaktır.</span><span class="sxs-lookup"><span data-stu-id="28fc2-138">This will be the image that will be shown for the respective social media.</span></span> <span data-ttu-id="28fc2-139">En iyi uygulama olarak, her bir platformda kullanılacak resim için sosyal medya platformunun SDK'sine başvurun.</span><span class="sxs-lookup"><span data-stu-id="28fc2-139">As a best practice, refer to the social media platform's SDK for the recommended image to use for each platform.</span></span> |

## <a name="add-a-social-share-module-to-a-buy-box-module"></a><span data-ttu-id="28fc2-140">Satın al kutusu modülüne bir sosyal içerik paylaşım modülü ekleme</span><span class="sxs-lookup"><span data-stu-id="28fc2-140">Add a social share module to a buy box module</span></span>

<span data-ttu-id="28fc2-141">Satın al kutusu modülüne bir sosyal içerik paylaşım modülü eklemek için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="28fc2-141">To add a social share module to a buy box module, follow these steps.</span></span>

1. <span data-ttu-id="28fc2-142">Fabrikam sitesinde, **Sayfalar**'ı seçin ve sonra ürün ayrıntıları sayfasını açmak için **DefaultPDP** sayfasını seçin.</span><span class="sxs-lookup"><span data-stu-id="28fc2-142">In the Fabrikam site, select **Pages**, and then select the **DefaultPDP** page to open the product details page.</span></span> 
1. <span data-ttu-id="28fc2-143">**Buybox (gerekli)** yuvasında üç nokta (**...**) düğmesini seçin ve **Modül Ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="28fc2-143">In the **Buybox (required)** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="28fc2-144">**Modül Ekle** iletişim kutusunda **Sosyal İçerik Paylaşım** modülünü seçin ve **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="28fc2-144">In the **Add Module** dialog box, select the **Social Share** module, and then select **OK**.</span></span>
1. <span data-ttu-id="28fc2-145">**Sosyal İçerik Paylaşım** yuvasında üç nokta (**...**) düğmesini seçin ve **Modül Ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="28fc2-145">In the **Social Share** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="28fc2-146">**Modül Ekle** iletişim kutusunda **SocialShare** modülünü seçin ve **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="28fc2-146">In the **Add Module** dialog box, select the **SocialShare** module, and then select **OK**.</span></span>
1. <span data-ttu-id="28fc2-147">**Socialshare** modülünün özellikler bölmesinde, **Yönlendirme** altında **Yatay**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="28fc2-147">In the properties pane of the **SocialShare** module, under **Orientation**, select **Horizontal**.</span></span> <span data-ttu-id="28fc2-148">Gerektiğinde bir açıklamalı alt yazı ekleyin.</span><span class="sxs-lookup"><span data-stu-id="28fc2-148">Add a caption as needed.</span></span>
1. <span data-ttu-id="28fc2-149">**SocialShare** yuvasında üç nokta (**...**) düğmesini seçin ve **Modül Ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="28fc2-149">In the **SocialShare** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="28fc2-150">**Modül Ekle** iletişim kutusunda **SocialShareItem** modülünü seçin ve **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="28fc2-150">In the **Add Module** dialog box, select the **SocialShareItem** module, and then select **OK**.</span></span>
1. <span data-ttu-id="28fc2-151">**SocialShareItem** modülünün özellikler bölmesinde, **Sosyal Medya** altında **Facebook** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="28fc2-151">In the properties pane of the **SocialShareItem** module, under **Social Media**, select **Facebook**.</span></span>
1. <span data-ttu-id="28fc2-152">**SocialShareItem** modülünün özellikler bölmesinde, **Simge** altında **+Resim ekleyin** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="28fc2-152">In the properties pane of the **SocialShareItem** module, under **Icon**, select **+ Add an image**.</span></span>
1. <span data-ttu-id="28fc2-153">**Ortam Seçicisi** iletişim kutusunda Facebook logo resmini seçin ve **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="28fc2-153">In the **Media Picker** dialog box, select the Facebook logo image, and then select **OK**.</span></span> <span data-ttu-id="28fc2-154">Herhangi bir Facebook logo resmi yoksa karşıya yüklemek için **Yeni ortam öğesini karşıya yükle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="28fc2-154">If no Facebook logo image is present, select **Upload new media item** to upload one.</span></span>
1. <span data-ttu-id="28fc2-155">Gerektiğinde ek **SocialShareItem** modülleri ekleyin ve yapılandırın.</span><span class="sxs-lookup"><span data-stu-id="28fc2-155">Add and configure additional **SocialShareItem** modules as needed.</span></span>
1. <span data-ttu-id="28fc2-156">**Kaydet**'i seçin ve ardından sayfayı önizlemek için **Önizleme**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="28fc2-156">Select **Save**, and then select **Preview** to preview the page.</span></span> <span data-ttu-id="28fc2-157">Sayfada sosyal içerik paylaşım modülü gösterilir.</span><span class="sxs-lookup"><span data-stu-id="28fc2-157">The page will show the social share module.</span></span>
1. <span data-ttu-id="28fc2-158">Sayfayı iade etmek için **Düzenlemeyi bitir**'i seçin, ardından yayımlamak için **Yayımla**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="28fc2-158">Select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="28fc2-159">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="28fc2-159">Additional resources</span></span>

[<span data-ttu-id="28fc2-160">Başlangıç paketine genel bakış</span><span class="sxs-lookup"><span data-stu-id="28fc2-160">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="28fc2-161">Satın alma kutusu modülü</span><span class="sxs-lookup"><span data-stu-id="28fc2-161">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="28fc2-162">Tanımlama bilgisi uyumluluğu</span><span class="sxs-lookup"><span data-stu-id="28fc2-162">Cookie compliance</span></span>](cookie-compliance.md)
