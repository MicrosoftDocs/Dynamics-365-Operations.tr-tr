---
title: Üst bilgi modülü
description: Bu konu üst bilgi modüllerini kapsamakta ve Microsoft Dynamics 365 Commerce'te sayfa üst bilgilerinin nasıl oluşturacağını açıklamaktadır.
author: anupamar
manager: annbe
ms.date: 04/13/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anupamar-ms
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: cec138ebefbd2beb2f1cf6302ce58d8bbc5c4bbd
ms.sourcegitcommit: ac966ea3a6c557fb5f9634b187b0e788d3e82d4d
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/14/2020
ms.locfileid: "3261456"
---
# <a name="header-module"></a><span data-ttu-id="c0369-103">Üst bilgi modülü</span><span class="sxs-lookup"><span data-stu-id="c0369-103">Header module</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="c0369-104">Bu konu üst bilgi modüllerini kapsamakta ve Microsoft Dynamics 365 Commerce'te sayfa üst bilgilerinin nasıl oluşturacağını açıklamaktadır.</span><span class="sxs-lookup"><span data-stu-id="c0369-104">This topic covers header modules and describes how to create page headers in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="c0369-105">Genel Bakış</span><span class="sxs-lookup"><span data-stu-id="c0369-105">Overview</span></span>

<span data-ttu-id="c0369-106">Dynamics 365 Commerce'te sayfa üst bilgisi; başlık, gezinti menüsü, arama, promosyon başlığı ve tanımlama bilgisi izin modülleri gibi birden çok modülü kapsar.</span><span class="sxs-lookup"><span data-stu-id="c0369-106">In Dynamics 365 Commerce, a page header comprises multiple modules, such as the header, navigation menu, search, promo banner, and cookie consent modules.</span></span> 

<span data-ttu-id="c0369-107">Üst bilgi modülü bir site logosu, gezinti hiyerarşisine bağlantılar, sitedeki diğer sayfalara bağlantılar, bir sepet sembolü, bir istek listesi sembolü, oturum açma seçenekleri ve arama çubuğu içerir.</span><span class="sxs-lookup"><span data-stu-id="c0369-107">The header module includes a site logo, links to the navigation hierarchy, links to other pages on the site, a cart symbol, a wishlist symbol, sign-in options, and the search bar.</span></span> <span data-ttu-id="c0369-108">Üst bilgi modülü, sitenin (yani bir masaüstü cihaz veya mobil cihaz) görüntülendiği cihaz için otomatik olarak en iyi duruma getirilir.</span><span class="sxs-lookup"><span data-stu-id="c0369-108">A header module is automatically optimized for the device that the site is being viewed on (in other words, for a desktop device or a mobile device).</span></span> <span data-ttu-id="c0369-109">Örneğin, bir mobil cihazda, gezinti çubuğu bir **menü** düğmesine (bazen *hamburger menüsü* olarak da adlandırılır) daraltılır.</span><span class="sxs-lookup"><span data-stu-id="c0369-109">For example, on a mobile device, the navigation bar is collapsed into a **Menu** button (which is sometimes referred to as a *hamburger menu*).</span></span>

## <a name="properties-of-a-header-module"></a><span data-ttu-id="c0369-110">Üst bilgi modülünün özellikleri</span><span class="sxs-lookup"><span data-stu-id="c0369-110">Properties of a header module</span></span>

<span data-ttu-id="c0369-111">Üst bilgi modülü **Logo resmi**, **Logo bağlantısı** ve **Hesabım bağlantıları** özelliklerini destekler.</span><span class="sxs-lookup"><span data-stu-id="c0369-111">A header module supports **Logo image**, **Logo link**, and **My account links** properties.</span></span> 

<span data-ttu-id="c0369-112">**Logo resmi** ve **Logo bağlantısı** özellikleri sayfada bir logo tanımlamak için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="c0369-112">The **Logo image** and **Logo link** properties are used to define a logo on the page.</span></span> <span data-ttu-id="c0369-113">Daha fazla bilgi için bkz. [Logo ekleme](add-logo.md).</span><span class="sxs-lookup"><span data-stu-id="c0369-113">For more information, see [Add a logo](add-logo.md).</span></span> 

<span data-ttu-id="c0369-114">**Hesabım bağlantıları** özelliği, site sahibinin üst bilgide hızlı bağlantıları göstermek istediği hesap sayfalarını tanımlamak için kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="c0369-114">The **My account links** property can be used to define account pages that the site owner wants to show quick links for in the header.</span></span>

## <a name="modules-that-are-available-in-a-header-module"></a><span data-ttu-id="c0369-115">Üstbilgi modülünde kullanılabilen modüller</span><span class="sxs-lookup"><span data-stu-id="c0369-115">Modules that are available in a header module</span></span>

<span data-ttu-id="c0369-116">Aşağıdaki modüller bir üstbilgi modülünde kullanılabilir:</span><span class="sxs-lookup"><span data-stu-id="c0369-116">The following modules can be used in a header module:</span></span>

- <span data-ttu-id="c0369-117">**Gezinti menüsü** – Gezinti menüsü, kanal gezinti hiyerarşisini ve diğer statik gezinti bağlantılarını temsil eder.</span><span class="sxs-lookup"><span data-stu-id="c0369-117">**Navigation menu** – The navigation menu represents the channel navigation hierarchy and other static navigation links.</span></span> <span data-ttu-id="c0369-118">Kanal gezinme hiyerarşisi Dynamics 365 Commerce'de yapılandırılabilir.</span><span class="sxs-lookup"><span data-stu-id="c0369-118">The channel navigation hierarchy can be configured in Dynamics 365 Commerce.</span></span> <span data-ttu-id="c0369-119">Gezinti menüsünde, Retail Server gezinti menüsü öğelerini ve statik menü öğelerini bir kaynak olarak belirtmek için kullanılan bir **Gezinti Kaynağı** özelliği vardır.</span><span class="sxs-lookup"><span data-stu-id="c0369-119">The navigation menu has a **Navigation Source** property that is used to specify Retail Server navigation menu items and static menu items as a source.</span></span> <span data-ttu-id="c0369-120">Statik menü öğeleri kaynak olarak belirtilirse, sitedeki diğer sayfalara göreli bağlantılar sağlanabilir.</span><span class="sxs-lookup"><span data-stu-id="c0369-120">If static menu items are specified as a source, relative links to other pages on the site can be provided.</span></span> <span data-ttu-id="c0369-121">Yapılandırılmış öğeler daha sonra üstbilgi gezintisi olarak görünür.</span><span class="sxs-lookup"><span data-stu-id="c0369-121">Configured items then appear as header navigation.</span></span> 
- <span data-ttu-id="c0369-122">**Arama** – Arama modülü, kullanıcıların ürün aramak için arama terimleri girmesine izin verir.</span><span class="sxs-lookup"><span data-stu-id="c0369-122">**Search** – The search module lets users enter search terms to search for products.</span></span> <span data-ttu-id="c0369-123">**Site Ayarları \>Uzantılar**'da, varsayılan arama sayfasının URL'si ve arama sorgusu parametreleri girilmelidir.</span><span class="sxs-lookup"><span data-stu-id="c0369-123">The URL of the default search page and the search query parameters must be provided at **Site Settings \> Extensions**.</span></span> <span data-ttu-id="c0369-124">Arama modülünde, arama düğmesini veya etiketi gereksinim duyduğunuz şekilde gizlemenize olanak sağlayan özellikler vardır.</span><span class="sxs-lookup"><span data-stu-id="c0369-124">The search module has properties that let you suppress the search button or label as you require.</span></span> <span data-ttu-id="c0369-125">Arama modülü ürün, anahtar sözcük ve kategori arama sonuçları gibi otomatik öneri seçeneklerini de destekler.</span><span class="sxs-lookup"><span data-stu-id="c0369-125">The search module also supports auto-suggest options, such as product, keyword, and category search results.</span></span>
- <span data-ttu-id="c0369-126">**Sepet simgesi** - Sepet simgesi modülü, belirli bir zamanda sepetteki öğelerin sayısını gösteren sepet simgesini temsil eder.</span><span class="sxs-lookup"><span data-stu-id="c0369-126">**Cart icon** - The cart icon module represents the cart icon, which shows the number of items in the cart at any given time.</span></span> <span data-ttu-id="c0369-127">Daha fazla bilgi için bkz. [Sepet simgesi modülü](cart-icon-module.md).</span><span class="sxs-lookup"><span data-stu-id="c0369-127">For more information, see [Cart icon module](cart-icon-module.md).</span></span>

## <a name="create-a-header-module-for-a-page"></a><span data-ttu-id="c0369-128">Sayfa için üst bilgi modülü oluşturma</span><span class="sxs-lookup"><span data-stu-id="c0369-128">Create a header module for a page</span></span>

<span data-ttu-id="c0369-129">Bir üst bilgi modülü oluşturmak için şu adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="c0369-129">To create a header module, follow these steps.</span></span>

1. <span data-ttu-id="c0369-130">**Üst bilgi parçası** olarak adlandırılan bir parça oluşturun ve buna bir kapsayıcı modülü ekleyin.</span><span class="sxs-lookup"><span data-stu-id="c0369-130">Create a fragment that is named **Header fragment**, and add a container module to it.</span></span>
1. <span data-ttu-id="c0369-131">Konteyner modülü için özellik panosunda **Genişlik** özelliğini **Konteyneri doldur**'a ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="c0369-131">In the property pane for the container module, set the **Width** property to **Fill container**.</span></span>
1. <span data-ttu-id="c0369-132">Kapsayıcı modülüne promosyon başlığı ve tanımlama bilgisi izin modülleri ekleyin.</span><span class="sxs-lookup"><span data-stu-id="c0369-132">Add a promo banner and cookie consent modules to the container module.</span></span>
1. <span data-ttu-id="c0369-133">Parçaya başka bir kapsayıcı modülü ekleyin ve **Genişlik** özelliğinin ayarını **Kapsayıcıya sığdır** yapın.</span><span class="sxs-lookup"><span data-stu-id="c0369-133">Add another container module to the fragment, and set the **Width** property to **Fill container**.</span></span>
1. <span data-ttu-id="c0369-134">İkinci kapsayıcı modülüne bir üst bilgi modülü ekleyin.</span><span class="sxs-lookup"><span data-stu-id="c0369-134">Add a header module to the second container module.</span></span>
1. <span data-ttu-id="c0369-135">Üst bilgi modülünün **Gezinti menüsü** yuvasında bir gezinti menüsü modülü ekleyin.</span><span class="sxs-lookup"><span data-stu-id="c0369-135">In the **Navigation menu** slot of the header module, add a navigation menu module.</span></span> 
1. <span data-ttu-id="c0369-136">Gezinti menüsü modülünün özellik bölmesinde, gezinti menüsü modülünün özelliklerini yapılandırın.</span><span class="sxs-lookup"><span data-stu-id="c0369-136">In the property pane for the navigation menu module, configure the properties of the navigation menu module.</span></span>
1. <span data-ttu-id="c0369-137">Üst bilgi modülünün **Arama** yuvasında bir arama modülü ekleyin.</span><span class="sxs-lookup"><span data-stu-id="c0369-137">In the **Search** slot of the header module, add a search module.</span></span> 
1. <span data-ttu-id="c0369-138">Arama modülünün özellik bölmesinde, arama modülünün özelliklerini yapılandırın.</span><span class="sxs-lookup"><span data-stu-id="c0369-138">In the property pane for the search module, configure the properties of the search module.</span></span> 
1. <span data-ttu-id="c0369-139">Başlık modülünün **Sepet simgesi** yuvasında, bir sepet simgesi modülü ekleyin.</span><span class="sxs-lookup"><span data-stu-id="c0369-139">In the **Cart icon** slot of the header module, add a cart icon module.</span></span> 
1. <span data-ttu-id="c0369-140">Sepet simgesi modülünün özellik bölmesinde, sepet simgesi modülünün özelliklerini yapılandırın.</span><span class="sxs-lookup"><span data-stu-id="c0369-140">In the property pane for the cart icon module, configure the properties of the cart icon module.</span></span> <span data-ttu-id="c0369-141">Üzerine gelindiğinde alışveriş sepeti simgesinin bir mini sepet görüntülenmesini istiyorsanız **Mini sepeti göster** için **Doğru** değerini seçin.</span><span class="sxs-lookup"><span data-stu-id="c0369-141">If you want the cart icon to display a mini cart when hovered over, select **True** for **Show mini cart**.</span></span>
1. <span data-ttu-id="c0369-142">Sayfa parçasını kaydedin, düzenlemeyi bitirin ve yayımlayın.</span><span class="sxs-lookup"><span data-stu-id="c0369-142">Save the page fragment, finish editing, and publish it.</span></span> 


<span data-ttu-id="c0369-143">Üstbilginin her sayfada göründüğünü garantilemek için, site için oluşturulan her sayfa şablonunda aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="c0369-143">To help guarantee that a header appears on every page, follow these steps on every page template that is created for the site.</span></span>

1. <span data-ttu-id="c0369-144">Varsayılan sayfanın **Ana** yuvasında, üst bilgi modülünü içeren üst bilgi sayfa parçasını üst bilgiye ekleyin.</span><span class="sxs-lookup"><span data-stu-id="c0369-144">In the **Main** slot of the default page, add the header page fragment that contains the header module to the header.</span></span>
1. <span data-ttu-id="c0369-145">Şablonu kaydedin, düzenlemeyi bitirin ve sonra yayımlayın.</span><span class="sxs-lookup"><span data-stu-id="c0369-145">Save the template, finish editing, and publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="c0369-146">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="c0369-146">Additional resources</span></span>

[<span data-ttu-id="c0369-147">Başlangıç paketine genel bakış</span><span class="sxs-lookup"><span data-stu-id="c0369-147">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="c0369-148">Konteyner modülü</span><span class="sxs-lookup"><span data-stu-id="c0369-148">Container module</span></span>](add-container-module.md)

[<span data-ttu-id="c0369-149">Satınalma kutusu modülü</span><span class="sxs-lookup"><span data-stu-id="c0369-149">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="c0369-150">Sepet modülü</span><span class="sxs-lookup"><span data-stu-id="c0369-150">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="c0369-151">Sepet simgesi modülü</span><span class="sxs-lookup"><span data-stu-id="c0369-151">Cart icon module</span></span>](cart-icon-module.md)

[<span data-ttu-id="c0369-152">Ödeme modülü</span><span class="sxs-lookup"><span data-stu-id="c0369-152">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="c0369-153">Sipariş onayı modülü</span><span class="sxs-lookup"><span data-stu-id="c0369-153">Order confirmation module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="c0369-154">Üst bilgi modülü</span><span class="sxs-lookup"><span data-stu-id="c0369-154">Header module</span></span>](author-header-module.md)

[<span data-ttu-id="c0369-155">Alt bilgi modülü</span><span class="sxs-lookup"><span data-stu-id="c0369-155">Footer module</span></span>](author-footer-module.md)
