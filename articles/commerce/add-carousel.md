---
title: Döngü modülü
description: Bu konu döngü kutusu modüllerini kapsamaktadır ve Microsoft Dynamics 365 Commerce'un site sayfalarına nasıl ekleneceğini açıklamaktadır.
author: anupamar-ms
manager: annbe
ms.date: 10/31/2019
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
ms.openlocfilehash: c2c5adc8ab2e0330f7b07e5153fd8332ab0203e5
ms.sourcegitcommit: 3a4e137ef3a96ba0a58c5352f4a3b57467ace9ae
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/11/2019
ms.locfileid: "2785249"
---
# <a name="carousel-module"></a><span data-ttu-id="dbe27-103">Döngü modülü</span><span class="sxs-lookup"><span data-stu-id="dbe27-103">Carousel module</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="dbe27-104">Bu konu döngü kutusu modüllerini kapsamaktadır ve Microsoft Dynamics 365 Commerce'un site sayfalarına nasıl ekleneceğini açıklamaktadır.</span><span class="sxs-lookup"><span data-stu-id="dbe27-104">This topic covers carousel modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="dbe27-105">Genel Bakış</span><span class="sxs-lookup"><span data-stu-id="dbe27-105">Overview</span></span>

<span data-ttu-id="dbe27-106">Bir döngü modülü, müşterilerin gözatmasına olanak veren bir döngüde birden fazla promosyon öğesi yerleştirmek için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="dbe27-106">A carousel module is used to put multiple promotional items in a carousel that customers can browse.</span></span> <span data-ttu-id="dbe27-107">Diğer modülleri barındıran özel konteyner modüldür.</span><span class="sxs-lookup"><span data-stu-id="dbe27-107">It's a special container module that hosts other modules.</span></span> <span data-ttu-id="dbe27-108">Örneğin, bir perakende birden fazla yeni ürün veya promosyonları sergileyebilecek bir giriş sayfasında döngü modülü kullanabilir.</span><span class="sxs-lookup"><span data-stu-id="dbe27-108">For example, a retailer can use a carousel module on a home page to showcase multiple new products or promotions.</span></span>

<span data-ttu-id="dbe27-109">Bir döngü modülü içinde Hero ve özellik modüllerini ekleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="dbe27-109">You can add hero and feature modules inside a carousel module.</span></span> <span data-ttu-id="dbe27-110">Bu şekilde, döngü modülünün özellikleri bu modüllerin nasıl işleneceğini tanımlar.</span><span class="sxs-lookup"><span data-stu-id="dbe27-110">The properties of the carousel module then define how those modules are rendered.</span></span>

## <a name="examples-of-carousel-modules-in-e-commerce"></a><span data-ttu-id="dbe27-111">E-ticarette döngü modülleri örnekleri</span><span class="sxs-lookup"><span data-stu-id="dbe27-111">Examples of carousel modules in e-Commerce</span></span>

- <span data-ttu-id="dbe27-112">İçinde birden fazla promosyon modülü bulunan bir döngü, giriş sayfasında kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="dbe27-112">A carousel that has multiple promotional modules inside it can be used on a home page.</span></span>
- <span data-ttu-id="dbe27-113">İçinde birden fazla promosyon modülü bulunan bir döngü, ürün ayrıntıları sayfasında kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="dbe27-113">A carousel that has multiple promotional modules inside it can be used on a product details page.</span></span>
- <span data-ttu-id="dbe27-114">Bir döngü, birden fazla promosyon veya ürünü yükseltmek için herhangi bir pazarlama sayfasında kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="dbe27-114">A carousel can be used on any marketing page to promote multiple promotions or products.</span></span>

## <a name="carousel-module-properties"></a><span data-ttu-id="dbe27-115">Döngü modülü özellikleri</span><span class="sxs-lookup"><span data-stu-id="dbe27-115">Carousel module properties</span></span>

| <span data-ttu-id="dbe27-116">Özellik adı</span><span class="sxs-lookup"><span data-stu-id="dbe27-116">Property name</span></span>             | <span data-ttu-id="dbe27-117">Değer</span><span class="sxs-lookup"><span data-stu-id="dbe27-117">Value</span></span>                                | <span data-ttu-id="dbe27-118">Tanım</span><span class="sxs-lookup"><span data-stu-id="dbe27-118">Description</span></span> |
|---------------------------|--------------------------------------|-------------|
| <span data-ttu-id="dbe27-119">Otomatik yürüt</span><span class="sxs-lookup"><span data-stu-id="dbe27-119">Autoplay</span></span>                  | <span data-ttu-id="dbe27-120">**Doğru** veya **yanlış**</span><span class="sxs-lookup"><span data-stu-id="dbe27-120">**True** or **False**</span></span>                | <span data-ttu-id="dbe27-121">Değer **doğru** olarak ayarlanırsa, döngü içindeki öğeler arasındaki geçiş otomatik olarak gerçekleşir.</span><span class="sxs-lookup"><span data-stu-id="dbe27-121">If the value is set to **True**, the transition between items inside the carousel occurs automatically.</span></span> <span data-ttu-id="dbe27-122">Değer **yanlış** olarak ayarlanırsa, müşteri bir maddeden bir sonraki öğeye geçmek için klavyeyi veya fareyi kullanmadıkça hiçbir geçiş gerçekleşmez.</span><span class="sxs-lookup"><span data-stu-id="dbe27-122">If the value is set to **False**, no transition occurs unless the customer uses the keyboard or mouse to move from one item to the next item.</span></span> |
| <span data-ttu-id="dbe27-123">Slayt geçiş aralığı</span><span class="sxs-lookup"><span data-stu-id="dbe27-123">Slide transition interval</span></span> | <span data-ttu-id="dbe27-124">Saniye cinsinden bir değer</span><span class="sxs-lookup"><span data-stu-id="dbe27-124">A value in seconds</span></span>                   | <span data-ttu-id="dbe27-125">Öğeler arasındaki geçişler için Aralık.</span><span class="sxs-lookup"><span data-stu-id="dbe27-125">The interval for transitions between items.</span></span> |
| <span data-ttu-id="dbe27-126">Geçiş animasyonu</span><span class="sxs-lookup"><span data-stu-id="dbe27-126">Transition animation</span></span>      | <span data-ttu-id="dbe27-127">**Kaydır** veya **Soldur**</span><span class="sxs-lookup"><span data-stu-id="dbe27-127">**Slide** or **Fade**</span></span>                | <span data-ttu-id="dbe27-128">Geçiş efekti.</span><span class="sxs-lookup"><span data-stu-id="dbe27-128">The transition effect.</span></span> |
| <span data-ttu-id="dbe27-129">Genişlik</span><span class="sxs-lookup"><span data-stu-id="dbe27-129">Width</span></span>                     | <span data-ttu-id="dbe27-130">**Kapsayıcıya sığdır** veya **Ekrana doldur**</span><span class="sxs-lookup"><span data-stu-id="dbe27-130">**Fit container** or **Fill screen**</span></span> | <span data-ttu-id="dbe27-131">Değer **konteynere sığdır** şekilde ayarlandıysa, döngü içindeki öğeler döngünün genişliğiyle sınırlandırılır.</span><span class="sxs-lookup"><span data-stu-id="dbe27-131">If the value is set to **Fit container**, the items inside the carousel are restricted to the width of the carousel.</span></span> <span data-ttu-id="dbe27-132">Değer, **ekranı doldur**'a ayarlanmışsa, öğeler döngü genişliğiyle sınırlandırılmaz ancak tam ekran moduna geçebilir.</span><span class="sxs-lookup"><span data-stu-id="dbe27-132">If the value is set to **Fill screen**, the items aren't restricted to the carousel width but can go into full-screen mode.</span></span> <span data-ttu-id="dbe27-133">İstenen düzene ulaşmak için değeri değiştirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="dbe27-133">You can change the value to achieve the desired layout.</span></span> |

## <a name="add-a-carousel-module-to-a-page"></a><span data-ttu-id="dbe27-134">Sayfaya döngü modülü ekleme</span><span class="sxs-lookup"><span data-stu-id="dbe27-134">Add a carousel module to a page</span></span>

<span data-ttu-id="dbe27-135">Bir yeni sayfaya döngü modülü eklemek ve gerekli özellikleri ayarlamak için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="dbe27-135">To add a carousel module to a new page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="dbe27-136">**Döngü şablonu** adlı bir sayfa şablonu oluşturun.</span><span class="sxs-lookup"><span data-stu-id="dbe27-136">Create a page template that is named **carousel template**.</span></span>
1. <span data-ttu-id="dbe27-137">Varsayılan sayfanın **ana** yuvasına bir döngü modülü ekleyin.</span><span class="sxs-lookup"><span data-stu-id="dbe27-137">In the **Main** slot of the default page, add a carousel module.</span></span>
1. <span data-ttu-id="dbe27-138">Döngü modülüne bir Hero modülü ekleyin.</span><span class="sxs-lookup"><span data-stu-id="dbe27-138">Add a hero module to the carousel module.</span></span>
1. <span data-ttu-id="dbe27-139">Döngü modülüne bir özellik modülü ekleyin.</span><span class="sxs-lookup"><span data-stu-id="dbe27-139">Add a feature module to the carousel module.</span></span>
1. <span data-ttu-id="dbe27-140">Şablonu giriş yapın ve yayımlayın.</span><span class="sxs-lookup"><span data-stu-id="dbe27-140">Check in the template, and publish it.</span></span> 
1. <span data-ttu-id="dbe27-141">**Döngü sayfası** adlı bir sayfa oluşturmak için yeni oluşturduğunuz döngü şablonunu kullanın.</span><span class="sxs-lookup"><span data-stu-id="dbe27-141">Use the carousel template that you just created to create a page that is named **carousel page**.</span></span>
1. <span data-ttu-id="dbe27-142">Yeni sayfanın **ana** yuvasına bir döngü modülü ekleyin.</span><span class="sxs-lookup"><span data-stu-id="dbe27-142">In the **Main** slot of the new page, add a carousel module.</span></span>
1. <span data-ttu-id="dbe27-143">Döngü modülünün **genişlik** özelliğini **ekranı doldur** ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="dbe27-143">Set the **Width** property of the carousel module to **Fill screen**.</span></span> 
1. <span data-ttu-id="dbe27-144">**Geçiş animasyon** özelliğini **slayda**ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="dbe27-144">Set the **Transition animation** property to **Slide**.</span></span>
1. <span data-ttu-id="dbe27-145">Döngü modülüne bir Hero modülü ekleyin.</span><span class="sxs-lookup"><span data-stu-id="dbe27-145">Add a hero module to the carousel module.</span></span>
1. <span data-ttu-id="dbe27-146">Hero modülünde bir resim ve bir başlık ekleyin ve sonra da Save'i (**Kaydet**) seçin.</span><span class="sxs-lookup"><span data-stu-id="dbe27-146">In the hero module, add an image and a heading, and then select **Save**.</span></span>
1. <span data-ttu-id="dbe27-147">Döngü modülüne bir özellik modülü ekleyin.</span><span class="sxs-lookup"><span data-stu-id="dbe27-147">Add a feature module to the carousel module.</span></span>
1. <span data-ttu-id="dbe27-148">Özellik modülünde bir resim, başlık ve bir metin paragrafı ekleyin.</span><span class="sxs-lookup"><span data-stu-id="dbe27-148">In the feature module, add an image, a heading, and a paragraph of text.</span></span>
1. <span data-ttu-id="dbe27-149">Sayfayı kaydet ve önizleyin.</span><span class="sxs-lookup"><span data-stu-id="dbe27-149">Save and preview the page.</span></span> <span data-ttu-id="dbe27-150">Sayfa, içinde iki modül bulunan bir döngüyü göstermelidir (Hero modülü ve bir özellik modülü).</span><span class="sxs-lookup"><span data-stu-id="dbe27-150">The page should show a carousel that has two modules inside it (a hero module and a feature module).</span></span> <span data-ttu-id="dbe27-151">İstenen etkiyi elde etmek için döngü, Hero ve özellik modüllerinin ek özelliklerini değiştirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="dbe27-151">You can change additional properties for the carousel, hero, and feature modules to achieve the desired effect.</span></span>
1. <span data-ttu-id="dbe27-152">Sayfayı giriş yapın ve yayımlayın.</span><span class="sxs-lookup"><span data-stu-id="dbe27-152">Check in the page, and publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="dbe27-153">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="dbe27-153">Additional resources</span></span>

[<span data-ttu-id="dbe27-154">Başlangıç paketine genel bakış</span><span class="sxs-lookup"><span data-stu-id="dbe27-154">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="dbe27-155">Uyarı modülü</span><span class="sxs-lookup"><span data-stu-id="dbe27-155">Alert module</span></span>](add-alert.md)

[<span data-ttu-id="dbe27-156">İçerik zengin blok modülü</span><span class="sxs-lookup"><span data-stu-id="dbe27-156">Content rich block module</span></span>](add-content-rich-block.md)

[<span data-ttu-id="dbe27-157">İçerik yerleştirme modülü</span><span class="sxs-lookup"><span data-stu-id="dbe27-157">Content placement module</span></span>](add-content-placement-modules.md)

[<span data-ttu-id="dbe27-158">Özellik modülü</span><span class="sxs-lookup"><span data-stu-id="dbe27-158">Feature module</span></span>](add-feature-module.md)

[<span data-ttu-id="dbe27-159">Hero modülü</span><span class="sxs-lookup"><span data-stu-id="dbe27-159">Hero module</span></span>](add-hero-module.md)

[<span data-ttu-id="dbe27-160">Video oynatıcı modülü</span><span class="sxs-lookup"><span data-stu-id="dbe27-160">Video player module</span></span>](add-video-player.md)
