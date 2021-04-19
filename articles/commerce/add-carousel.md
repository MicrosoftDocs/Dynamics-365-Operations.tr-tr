---
title: Döngü modülü
description: Bu konu döngü kutusu modüllerini kapsamaktadır ve Microsoft Dynamics 365 Commerce'un site sayfalarına nasıl ekleneceğini açıklamaktadır.
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
ms.dyn365.ops.version: ''
ms.openlocfilehash: 5bc2227e08dbbf5f76a37180114e5affff131658
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/31/2021
ms.locfileid: "5797899"
---
# <a name="carousel-module"></a><span data-ttu-id="cd974-103">Döngü modülü</span><span class="sxs-lookup"><span data-stu-id="cd974-103">Carousel module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="cd974-104">Bu konu döngü kutusu modüllerini kapsamaktadır ve Microsoft Dynamics 365 Commerce'un site sayfalarına nasıl ekleneceğini açıklamaktadır.</span><span class="sxs-lookup"><span data-stu-id="cd974-104">This topic covers carousel modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="cd974-105">Bir döngü modülü, müşterilerin gözatmasına olanak veren bir döner döngüde birden fazla promosyon öğesini (zengin görseller dahil) yerleştirmek için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="cd974-105">A carousel module is used to put multiple promotional items (including rich images) in a rotating carousel banner that customers can browse.</span></span> <span data-ttu-id="cd974-106">Örneğin, bir perakende birden fazla yeni ürün veya promosyonları sergileyebilecek bir giriş sayfasında döngü modülü kullanabilir.</span><span class="sxs-lookup"><span data-stu-id="cd974-106">For example, a retailer can use a carousel module on a home page to showcase multiple new products or promotions.</span></span>

<span data-ttu-id="cd974-107">Bir içerik bloku modülünü bir döngü modülüne ekleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="cd974-107">You can add content block modules inside a carousel module.</span></span> <span data-ttu-id="cd974-108">Bu şekilde, döngü modülünün özellikleri bu modüllerin nasıl işleneceğini tanımlar.</span><span class="sxs-lookup"><span data-stu-id="cd974-108">The properties of the carousel module then define how those modules are rendered.</span></span>

## <a name="examples-of-carousel-modules-in-e-commerce"></a><span data-ttu-id="cd974-109">E-ticarette döngü modülleri örnekleri</span><span class="sxs-lookup"><span data-stu-id="cd974-109">Examples of carousel modules in e-Commerce</span></span>

- <span data-ttu-id="cd974-110">İçinde birden fazla promosyon modülü bulunan bir döngü, giriş sayfasında kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="cd974-110">A carousel that has multiple promotional modules inside it can be used on a home page.</span></span>
- <span data-ttu-id="cd974-111">İçinde birden fazla promosyon modülü bulunan bir döngü, ürün ayrıntıları sayfasında kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="cd974-111">A carousel that has multiple promotional modules inside it can be used on a product details page.</span></span>
- <span data-ttu-id="cd974-112">Bir döngü, birden fazla promosyon veya ürünü yükseltmek için herhangi bir pazarlama sayfasında kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="cd974-112">A carousel can be used on any marketing page to promote multiple promotions or products.</span></span>

<span data-ttu-id="cd974-113">Aşağıdaki resimde giriş sayfasında kullanılan bir döngü modülü örneği gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="cd974-113">The following image shows an example of a carousel module that is used on a home page.</span></span> <span data-ttu-id="cd974-114">Bu döngü modülü birden çok içerik bloğu öğesi içeriyor.</span><span class="sxs-lookup"><span data-stu-id="cd974-114">This carousel module contains multiple content block items.</span></span>

![Döngü modülü örneği](./media/Hero.PNG)

## <a name="carousel-module-properties"></a><span data-ttu-id="cd974-116">Döngü modülü özellikleri</span><span class="sxs-lookup"><span data-stu-id="cd974-116">Carousel module properties</span></span>

| <span data-ttu-id="cd974-117">Özellik adı</span><span class="sxs-lookup"><span data-stu-id="cd974-117">Property name</span></span>             | <span data-ttu-id="cd974-118">Değer</span><span class="sxs-lookup"><span data-stu-id="cd974-118">Value</span></span>                 | <span data-ttu-id="cd974-119">Tanım</span><span class="sxs-lookup"><span data-stu-id="cd974-119">Description</span></span> |
|---------------------------|-----------------------|-------------|
| <span data-ttu-id="cd974-120">Otomatik yürüt</span><span class="sxs-lookup"><span data-stu-id="cd974-120">Autoplay</span></span>                  | <span data-ttu-id="cd974-121">**Doğru** veya **yanlış**</span><span class="sxs-lookup"><span data-stu-id="cd974-121">**True** or **False**</span></span> | <span data-ttu-id="cd974-122">Değer **doğru** olarak ayarlanırsa, döngü içindeki öğeler arasındaki geçiş otomatik olarak gerçekleşir.</span><span class="sxs-lookup"><span data-stu-id="cd974-122">If the value is set to **True**, the transition between items inside the carousel occurs automatically.</span></span> <span data-ttu-id="cd974-123">Değer **yanlış** olarak ayarlanırsa, müşteri bir maddeden bir sonraki öğeye geçmek için klavyeyi veya fareyi kullanmadıkça hiçbir geçiş gerçekleşmez.</span><span class="sxs-lookup"><span data-stu-id="cd974-123">If the value is set to **False**, no transition occurs unless the customer uses the keyboard or mouse to move from one item to the next item.</span></span> |
| <span data-ttu-id="cd974-124">Slayt geçiş aralığı</span><span class="sxs-lookup"><span data-stu-id="cd974-124">Slide transition interval</span></span> | <span data-ttu-id="cd974-125">Saniye cinsinden bir değer</span><span class="sxs-lookup"><span data-stu-id="cd974-125">A value in seconds</span></span>    | <span data-ttu-id="cd974-126">Öğeler arasındaki geçişler için Aralık.</span><span class="sxs-lookup"><span data-stu-id="cd974-126">The interval for transitions between items.</span></span> |
| <span data-ttu-id="cd974-127">Geçiş türü</span><span class="sxs-lookup"><span data-stu-id="cd974-127">Transition type</span></span>           | <span data-ttu-id="cd974-128">**Kaydır** veya **Soldur**</span><span class="sxs-lookup"><span data-stu-id="cd974-128">**Slide** or **Fade**</span></span> | <span data-ttu-id="cd974-129">Öğeler arasındaki geçiş efekti.</span><span class="sxs-lookup"><span data-stu-id="cd974-129">The transition effect between items.</span></span> |
| <span data-ttu-id="cd974-130">Döngü yüzgecini gizle</span><span class="sxs-lookup"><span data-stu-id="cd974-130">Hide carousel flipper</span></span>     | <span data-ttu-id="cd974-131">**Doğru** veya **yanlış**</span><span class="sxs-lookup"><span data-stu-id="cd974-131">**True** or **False**</span></span> | <span data-ttu-id="cd974-132">Değer **Doğru** olarak ayarlanmışsa, döngü değiştirici ve sekans göstergesi saklanır.</span><span class="sxs-lookup"><span data-stu-id="cd974-132">If the value is set to **True**, the carousel flipper and sequence indicator are hidden.</span></span> |
| <span data-ttu-id="cd974-133">Döngü kapatmaya izin ver</span><span class="sxs-lookup"><span data-stu-id="cd974-133">Allow carousel dismiss</span></span>    | <span data-ttu-id="cd974-134">**Doğru** veya **yanlış**</span><span class="sxs-lookup"><span data-stu-id="cd974-134">**True** or **False**</span></span> | <span data-ttu-id="cd974-135">Değer **Doğru** olarak ayarlandıysa, kullanıcılar döngüyü kapatabilir.</span><span class="sxs-lookup"><span data-stu-id="cd974-135">If the value is set to **True**, users can dismiss the carousel.</span></span> |

## <a name="add-a-carousel-module-to-a-page"></a><span data-ttu-id="cd974-136">Sayfaya döngü modülü ekleme</span><span class="sxs-lookup"><span data-stu-id="cd974-136">Add a carousel module to a page</span></span>

<span data-ttu-id="cd974-137">Bir yeni sayfaya döngü modülü eklemek ve gerekli özellikleri ayarlamak için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="cd974-137">To add a carousel module to a new page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="cd974-138">Bir yeni şablonu oluşturmak için **Şablonlar**'a gidin ve **Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="cd974-138">Go to **Templates**, and select **New** to create a new template.</span></span>
1. <span data-ttu-id="cd974-139">**Yeni Şablon** iletişim kutusunda **Şablon adı** altında, **Döngü şablonu**'nu girin ve **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="cd974-139">In the **New Template** dialog box, under **Template Name**, enter **Carousel template**, and then select **OK**.</span></span>
1. <span data-ttu-id="cd974-140">**Gövde** yuvasında bir **Varsayılan sayfa** modülü ekleyin.</span><span class="sxs-lookup"><span data-stu-id="cd974-140">In the **Body** slot, add a **Default page** module.</span></span>
1. <span data-ttu-id="cd974-141">Şablonu iade etmek için **Düzenlemeyi bitir**'i seçin, ardından yayımlamak için **Yayımla**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="cd974-141">Select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span>  
1. <span data-ttu-id="cd974-142">**Döngü sayfası** adlı bir sayfa oluşturmak için yeni oluşturduğunuz döngü şablonunu kullanın.</span><span class="sxs-lookup"><span data-stu-id="cd974-142">Use the carousel template that you just created to create a page that is named **Carousel page**.</span></span>
1. <span data-ttu-id="cd974-143">Yeni sayfanın **ana** yuvasına bir konteyner modülü ekleyin.</span><span class="sxs-lookup"><span data-stu-id="cd974-143">In the **Main** slot of the new page, add a container module.</span></span> 
1. <span data-ttu-id="cd974-144">Sağdaki panoda, **Genişlik** değerini **Ekranı doldur**'a ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="cd974-144">In the pane on the right, set the **Width** value to **Fill Screen**.</span></span>
1. <span data-ttu-id="cd974-145">**Sayfa Anahattı** altında, bir döngü modlünü konteyner modülüne ekleyin.</span><span class="sxs-lookup"><span data-stu-id="cd974-145">Under **Page Outline**, add a carousel module to the container module.</span></span>
1. <span data-ttu-id="cd974-146">Döngü modülüne bir içerik bloku modülü ekle.</span><span class="sxs-lookup"><span data-stu-id="cd974-146">Add a content block module to the carousel module.</span></span> <span data-ttu-id="cd974-147">**Başlık**, **bağlantı**, **yerleşim** ve diğer özellikleri sağlayarak içerik bloğu modülünün özelliklerini ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="cd974-147">Set the properties of the content block module by providing **Heading**, **Link**, **Layout**, and other properties.</span></span>
1. <span data-ttu-id="cd974-148">Başka bir içerik bloğu modülü ekleyin ve konfigüre edin.</span><span class="sxs-lookup"><span data-stu-id="cd974-148">Add and configure another content block module.</span></span>
1. <span data-ttu-id="cd974-149">Döngü Modülü için gerekli olan ek özellikleri ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="cd974-149">Set additional properties for the carousel module as you require.</span></span>
1. <span data-ttu-id="cd974-150">**Kaydet**'i seçin ve ardından sayfayı önizlemek için **Önizleme**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="cd974-150">Select **Save**, and then select **Preview** to preview the page.</span></span> <span data-ttu-id="cd974-151">Sayfa, içinde iki modül bulunan bir döngüyü göstermelidir (Hero modülü ve bir özellik modülü).</span><span class="sxs-lookup"><span data-stu-id="cd974-151">The page should show a carousel that has two modules inside it (a hero module and a feature module).</span></span> <span data-ttu-id="cd974-152">İstenen etkiyi elde etmek için döngü, Hero ve özellik modüllerinin ek özelliklerini değiştirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="cd974-152">You can change additional properties for the carousel, hero, and feature modules to achieve the desired effect.</span></span>
1. <span data-ttu-id="cd974-153">Sayfayı iade etmek için **Düzenlemeyi bitir**'i seçin, ardından yayımlamak için **Yayımla**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="cd974-153">Select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="cd974-154">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="cd974-154">Additional resources</span></span>

[<span data-ttu-id="cd974-155">Modül kitaplığına genel bakış</span><span class="sxs-lookup"><span data-stu-id="cd974-155">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="cd974-156">Promosyon başlığı modülü</span><span class="sxs-lookup"><span data-stu-id="cd974-156">Promo banner module</span></span>](add-alert.md)

[<span data-ttu-id="cd974-157">Metin bloğu modülü</span><span class="sxs-lookup"><span data-stu-id="cd974-157">Text block module</span></span>](add-content-rich-block.md)

[<span data-ttu-id="cd974-158">İçerik bloğu modülü</span><span class="sxs-lookup"><span data-stu-id="cd974-158">Content block module</span></span>](add-hero-module.md)

[<span data-ttu-id="cd974-159">Video oynatıcı modülü</span><span class="sxs-lookup"><span data-stu-id="cd974-159">Video player module</span></span>](add-video-player.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]