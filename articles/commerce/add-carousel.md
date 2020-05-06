---
title: Döngü modülü
description: Bu konu döngü kutusu modüllerini kapsamaktadır ve Microsoft Dynamics 365 Commerce'un site sayfalarına nasıl ekleneceğini açıklamaktadır.
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
ms.openlocfilehash: f399e4c5618b65b781fdd3ec835e841614579313
ms.sourcegitcommit: 7a1d01122790b904e2d96a7ea9f1d003392358a6
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/17/2020
ms.locfileid: "3269740"
---
# <a name="carousel-module"></a><span data-ttu-id="bdb00-103">Döngü modülü</span><span class="sxs-lookup"><span data-stu-id="bdb00-103">Carousel module</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="bdb00-104">Bu konu döngü kutusu modüllerini kapsamaktadır ve Microsoft Dynamics 365 Commerce'un site sayfalarına nasıl ekleneceğini açıklamaktadır.</span><span class="sxs-lookup"><span data-stu-id="bdb00-104">This topic covers carousel modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="bdb00-105">Genel Bakış</span><span class="sxs-lookup"><span data-stu-id="bdb00-105">Overview</span></span>

<span data-ttu-id="bdb00-106">Bir döngü modülü, müşterilerin gözatmasına olanak veren bir döner döngüde birden fazla promosyon öğesini (zengin görseller dahil) yerleştirmek için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="bdb00-106">A carousel module is used to put multiple promotional items (including rich images) in a rotating carousel banner that customers can browse.</span></span> <span data-ttu-id="bdb00-107">Örneğin, bir perakende birden fazla yeni ürün veya promosyonları sergileyebilecek bir giriş sayfasında döngü modülü kullanabilir.</span><span class="sxs-lookup"><span data-stu-id="bdb00-107">For example, a retailer can use a carousel module on a home page to showcase multiple new products or promotions.</span></span>

<span data-ttu-id="bdb00-108">Bir içerik bloku modülünü bir döngü modülüne ekleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="bdb00-108">You can add content block modules inside a carousel module.</span></span> <span data-ttu-id="bdb00-109">Bu şekilde, döngü modülünün özellikleri bu modüllerin nasıl işleneceğini tanımlar.</span><span class="sxs-lookup"><span data-stu-id="bdb00-109">The properties of the carousel module then define how those modules are rendered.</span></span>

## <a name="examples-of-carousel-modules-in-e-commerce"></a><span data-ttu-id="bdb00-110">E-ticarette döngü modülleri örnekleri</span><span class="sxs-lookup"><span data-stu-id="bdb00-110">Examples of carousel modules in e-Commerce</span></span>

- <span data-ttu-id="bdb00-111">İçinde birden fazla promosyon modülü bulunan bir döngü, giriş sayfasında kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="bdb00-111">A carousel that has multiple promotional modules inside it can be used on a home page.</span></span>
- <span data-ttu-id="bdb00-112">İçinde birden fazla promosyon modülü bulunan bir döngü, ürün ayrıntıları sayfasında kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="bdb00-112">A carousel that has multiple promotional modules inside it can be used on a product details page.</span></span>
- <span data-ttu-id="bdb00-113">Bir döngü, birden fazla promosyon veya ürünü yükseltmek için herhangi bir pazarlama sayfasında kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="bdb00-113">A carousel can be used on any marketing page to promote multiple promotions or products.</span></span>

## <a name="carousel-module-properties"></a><span data-ttu-id="bdb00-114">Döngü modülü özellikleri</span><span class="sxs-lookup"><span data-stu-id="bdb00-114">Carousel module properties</span></span>

| <span data-ttu-id="bdb00-115">Özellik adı</span><span class="sxs-lookup"><span data-stu-id="bdb00-115">Property name</span></span>             | <span data-ttu-id="bdb00-116">Değer</span><span class="sxs-lookup"><span data-stu-id="bdb00-116">Value</span></span>                 | <span data-ttu-id="bdb00-117">Tanım</span><span class="sxs-lookup"><span data-stu-id="bdb00-117">Description</span></span> |
|---------------------------|-----------------------|-------------|
| <span data-ttu-id="bdb00-118">Otomatik yürüt</span><span class="sxs-lookup"><span data-stu-id="bdb00-118">Autoplay</span></span>                  | <span data-ttu-id="bdb00-119">**Doğru** veya **yanlış**</span><span class="sxs-lookup"><span data-stu-id="bdb00-119">**True** or **False**</span></span> | <span data-ttu-id="bdb00-120">Değer **doğru** olarak ayarlanırsa, döngü içindeki öğeler arasındaki geçiş otomatik olarak gerçekleşir.</span><span class="sxs-lookup"><span data-stu-id="bdb00-120">If the value is set to **True**, the transition between items inside the carousel occurs automatically.</span></span> <span data-ttu-id="bdb00-121">Değer **yanlış** olarak ayarlanırsa, müşteri bir maddeden bir sonraki öğeye geçmek için klavyeyi veya fareyi kullanmadıkça hiçbir geçiş gerçekleşmez.</span><span class="sxs-lookup"><span data-stu-id="bdb00-121">If the value is set to **False**, no transition occurs unless the customer uses the keyboard or mouse to move from one item to the next item.</span></span> |
| <span data-ttu-id="bdb00-122">Slayt geçiş aralığı</span><span class="sxs-lookup"><span data-stu-id="bdb00-122">Slide transition interval</span></span> | <span data-ttu-id="bdb00-123">Saniye cinsinden bir değer</span><span class="sxs-lookup"><span data-stu-id="bdb00-123">A value in seconds</span></span>    | <span data-ttu-id="bdb00-124">Öğeler arasındaki geçişler için Aralık.</span><span class="sxs-lookup"><span data-stu-id="bdb00-124">The interval for transitions between items.</span></span> |
| <span data-ttu-id="bdb00-125">Geçiş türü</span><span class="sxs-lookup"><span data-stu-id="bdb00-125">Transition type</span></span>           | <span data-ttu-id="bdb00-126">**Kaydır** veya **Soldur**</span><span class="sxs-lookup"><span data-stu-id="bdb00-126">**Slide** or **Fade**</span></span> | <span data-ttu-id="bdb00-127">Öğeler arasındaki geçiş efekti.</span><span class="sxs-lookup"><span data-stu-id="bdb00-127">The transition effect between items.</span></span> |
| <span data-ttu-id="bdb00-128">Döngü yüzgecini gizle</span><span class="sxs-lookup"><span data-stu-id="bdb00-128">Hide carousel flipper</span></span>     | <span data-ttu-id="bdb00-129">**Doğru** veya **yanlış**</span><span class="sxs-lookup"><span data-stu-id="bdb00-129">**True** or **False**</span></span> | <span data-ttu-id="bdb00-130">Değer **Doğru** olarak ayarlanmışsa, döngü değiştirici ve sekans göstergesi saklanır.</span><span class="sxs-lookup"><span data-stu-id="bdb00-130">If the value is set to **True**, the carousel flipper and sequence indicator are hidden.</span></span> |
| <span data-ttu-id="bdb00-131">Döngü kapatmaya izin ver</span><span class="sxs-lookup"><span data-stu-id="bdb00-131">Allow carousel dismiss</span></span>    | <span data-ttu-id="bdb00-132">**Doğru** veya **yanlış**</span><span class="sxs-lookup"><span data-stu-id="bdb00-132">**True** or **False**</span></span> | <span data-ttu-id="bdb00-133">Değer **Doğru** olarak ayarlandıysa, kullanıcılar döngüyü kapatabilir.</span><span class="sxs-lookup"><span data-stu-id="bdb00-133">If the value is set to **True**, users can dismiss the carousel.</span></span> |

## <a name="add-a-carousel-module-to-a-page"></a><span data-ttu-id="bdb00-134">Sayfaya döngü modülü ekleme</span><span class="sxs-lookup"><span data-stu-id="bdb00-134">Add a carousel module to a page</span></span>

<span data-ttu-id="bdb00-135">Bir yeni sayfaya döngü modülü eklemek ve gerekli özellikleri ayarlamak için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="bdb00-135">To add a carousel module to a new page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="bdb00-136">Yeni sayfa şablonu oluşturmak için **Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="bdb00-136">Select **New** to create a page template.</span></span>
1. <span data-ttu-id="bdb00-137">**Yeni Şablon** iletişim kutusunda **Şablon adı** altında, **Döngü şablonu**'nu girin ve **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="bdb00-137">In the **New Template** dialog box, under **Template Name**, enter **Carousel template**, and then select **OK**.</span></span>
1. <span data-ttu-id="bdb00-138">**Gövde** yuvasında bir **Varsayılan sayfa** modülü ekleyin.</span><span class="sxs-lookup"><span data-stu-id="bdb00-138">In the **Body** slot, add a **Default page** module.</span></span>
1. <span data-ttu-id="bdb00-139">Şablonu iade etmek için **Düzenlemeyi bitir**'i seçin, ardından yayımlamak için **Yayımla**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="bdb00-139">Select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span>  
1. <span data-ttu-id="bdb00-140">**Döngü sayfası** adlı bir sayfa oluşturmak için yeni oluşturduğunuz döngü şablonunu kullanın.</span><span class="sxs-lookup"><span data-stu-id="bdb00-140">Use the carousel template that you just created to create a page that is named **Carousel page**.</span></span>
1. <span data-ttu-id="bdb00-141">Yeni sayfanın **ana** yuvasına bir konteyner modülü ekleyin.</span><span class="sxs-lookup"><span data-stu-id="bdb00-141">In the **Main** slot of the new page, add a container module.</span></span> 
1. <span data-ttu-id="bdb00-142">Sağdaki panoda, **Genişlik** değerini **Ekranı doldur**'a ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="bdb00-142">In the pane on the right, set the **Width** value to **Fill Screen**.</span></span>
1. <span data-ttu-id="bdb00-143">**Sayfa Anahattı** altında, bir döngü modlünü konteyner modülüne ekleyin.</span><span class="sxs-lookup"><span data-stu-id="bdb00-143">Under **Page Outline**, add a carousel module to the container module.</span></span>
1. <span data-ttu-id="bdb00-144">Döngü modülüne bir içerik bloku modülü ekle.</span><span class="sxs-lookup"><span data-stu-id="bdb00-144">Add a content block module to the carousel module.</span></span> <span data-ttu-id="bdb00-145">**Başlık**, **bağlantı**, **yerleşim** ve diğer özellikleri sağlayarak içerik bloğu modülünün özelliklerini ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="bdb00-145">Set the properties of the content block module by providing **Heading**, **Link**, **Layout**, and other properties.</span></span>
1. <span data-ttu-id="bdb00-146">Başka bir içerik bloğu modülü ekleyin ve konfigüre edin.</span><span class="sxs-lookup"><span data-stu-id="bdb00-146">Add and configure another content block module.</span></span>
1. <span data-ttu-id="bdb00-147">Döngü Modülü için gerekli olan ek özellikleri ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="bdb00-147">Set additional properties for the carousel module as you require.</span></span>
1. <span data-ttu-id="bdb00-148">**Kaydet**'i seçin ve ardından sayfayı önizlemek için **Önizleme**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="bdb00-148">Select **Save**, and then select **Preview** to preview the page.</span></span> <span data-ttu-id="bdb00-149">Sayfa, içinde iki modül bulunan bir döngüyü göstermelidir (Hero modülü ve bir özellik modülü).</span><span class="sxs-lookup"><span data-stu-id="bdb00-149">The page should show a carousel that has two modules inside it (a hero module and a feature module).</span></span> <span data-ttu-id="bdb00-150">İstenen etkiyi elde etmek için döngü, Hero ve özellik modüllerinin ek özelliklerini değiştirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="bdb00-150">You can change additional properties for the carousel, hero, and feature modules to achieve the desired effect.</span></span>
1. <span data-ttu-id="bdb00-151">Sayfayı iade etmek için **Düzenlemeyi bitir**'i seçin, ardından yayımlamak için **Yayımla**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="bdb00-151">Select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="bdb00-152">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="bdb00-152">Additional resources</span></span>

[<span data-ttu-id="bdb00-153">Başlangıç paketine genel bakış</span><span class="sxs-lookup"><span data-stu-id="bdb00-153">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="bdb00-154">Promosyon başlığı modülü</span><span class="sxs-lookup"><span data-stu-id="bdb00-154">Promo banner module</span></span>](add-alert.md)

[<span data-ttu-id="bdb00-155">Metin bloku modülü</span><span class="sxs-lookup"><span data-stu-id="bdb00-155">Text block module</span></span>](add-content-rich-block.md)

[<span data-ttu-id="bdb00-156">İçerik blok modülü</span><span class="sxs-lookup"><span data-stu-id="bdb00-156">Content block module</span></span>](add-hero-module.md)

[<span data-ttu-id="bdb00-157">Video oynatıcı modülü</span><span class="sxs-lookup"><span data-stu-id="bdb00-157">Video player module</span></span>](add-video-player.md)
