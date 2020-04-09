---
title: Üst bilgi modülü
description: Bu konu üst bilgi modüllerini kapsamakta ve Microsoft Dynamics 365 Commerce'te sayfa üst bilgilerinin nasıl oluşturacağını açıklamaktadır.
author: anupamar
manager: annbe
ms.date: 01/23/2020
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
ms.openlocfilehash: efadd19681bbb21ea5b2b469e55bc6f4b0535046
ms.sourcegitcommit: 34e543e807ac8790597f522fe3b4f0266cf4ee56
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/24/2020
ms.locfileid: "3025721"
---
# <a name="header-module"></a><span data-ttu-id="56d5b-103">Üst bilgi modülü</span><span class="sxs-lookup"><span data-stu-id="56d5b-103">Header module</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="56d5b-104">Bu konu üst bilgi modüllerini kapsamakta ve Microsoft Dynamics 365 Commerce'te sayfa üst bilgilerinin nasıl oluşturacağını açıklamaktadır.</span><span class="sxs-lookup"><span data-stu-id="56d5b-104">This topic covers header modules and describes how to create page headers in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="56d5b-105">Genel Bakış</span><span class="sxs-lookup"><span data-stu-id="56d5b-105">Overview</span></span>

<span data-ttu-id="56d5b-106">Dynamics 365 Commerce'te sayfa üst bilgisi; başlık, gezinti menüsü, arama, promosyon başlığı ve tanımlama bilgisi izin modülleri gibi birden çok modülü kapsar.</span><span class="sxs-lookup"><span data-stu-id="56d5b-106">In Dynamics 365 Commerce, a page header comprises multiple modules, such as the header, navigation menu, search, promo banner, and cookie consent modules.</span></span> 

<span data-ttu-id="56d5b-107">Üst bilgi modülü bir site logosu, gezinti hiyerarşisine bağlantılar, sitedeki diğer sayfalara bağlantılar, bir sepet sembolü, bir istek listesi sembolü, oturum açma seçenekleri ve arama çubuğu içerir.</span><span class="sxs-lookup"><span data-stu-id="56d5b-107">The header module includes a site logo, links to the navigation hierarchy, links to other pages on the site, a cart symbol, a wishlist symbol, sign-in options, and the search bar.</span></span> <span data-ttu-id="56d5b-108">Üst bilgi modülü, sitenin (yani bir masaüstü cihaz veya mobil cihaz) görüntülendiği cihaz için otomatik olarak en iyi duruma getirilir.</span><span class="sxs-lookup"><span data-stu-id="56d5b-108">A header module is automatically optimized for the device that the site is being viewed on (in other words, for a desktop device or a mobile device).</span></span> <span data-ttu-id="56d5b-109">Örneğin, bir mobil cihazda, gezinti çubuğu bir **menü** düğmesine (bazen *hamburger menüsü* olarak da adlandırılır) daraltılır.</span><span class="sxs-lookup"><span data-stu-id="56d5b-109">For example, on a mobile device, the navigation bar is collapsed into a **Menu** button (which is sometimes referred to as a *hamburger menu*).</span></span>

## <a name="properties-of-a-header-module"></a><span data-ttu-id="56d5b-110">Üst bilgi modülünün özellikleri</span><span class="sxs-lookup"><span data-stu-id="56d5b-110">Properties of a header module</span></span>

<span data-ttu-id="56d5b-111">Üst bilgi modülü **Logo resmi**, **Logo bağlantısı** ve **Hesabım bağlantıları** özelliklerini destekler.</span><span class="sxs-lookup"><span data-stu-id="56d5b-111">A header module supports **Logo image**, **Logo link**, and **My account links** properties.</span></span> 

<span data-ttu-id="56d5b-112">**Logo resmi** ve **Logo bağlantısı** özellikleri sayfada bir logo tanımlamak için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="56d5b-112">The **Logo image** and **Logo link** properties are used to define a logo on the page.</span></span> <span data-ttu-id="56d5b-113">Daha fazla bilgi için bkz. [Logo ekleme](add-logo.md).</span><span class="sxs-lookup"><span data-stu-id="56d5b-113">For more information, see [Add a logo](add-logo.md).</span></span> 

<span data-ttu-id="56d5b-114">**Hesabım bağlantıları** özelliği, site sahibinin üst bilgide hızlı bağlantıları göstermek istediği hesap sayfalarını tanımlamak için kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="56d5b-114">The **My account links** property can be used to define account pages that the site owner wants to show quick links for in the header.</span></span>

## <a name="modules-that-are-available-in-a-header-module"></a><span data-ttu-id="56d5b-115">Üstbilgi modülünde kullanılabilen modüller</span><span class="sxs-lookup"><span data-stu-id="56d5b-115">Modules that are available in a header module</span></span>

<span data-ttu-id="56d5b-116">Aşağıdaki modüller bir üstbilgi modülünde kullanılabilir:</span><span class="sxs-lookup"><span data-stu-id="56d5b-116">The following modules can be used in a header module:</span></span>

- <span data-ttu-id="56d5b-117">**Gezinti menüsü** – Gezinti menüsü, kanal gezinti hiyerarşisini ve diğer statik gezinti bağlantılarını temsil eder.</span><span class="sxs-lookup"><span data-stu-id="56d5b-117">**Navigation menu** – The navigation menu represents the channel navigation hierarchy and other static navigation links.</span></span> <span data-ttu-id="56d5b-118">Kanal gezinme hiyerarşisi Dynamics 365 Commerce'de yapılandırılabilir.</span><span class="sxs-lookup"><span data-stu-id="56d5b-118">The channel navigation hierarchy can be configured in Dynamics 365 Commerce.</span></span> <span data-ttu-id="56d5b-119">Gezinti menüsünde, Retail Server gezinti menüsü öğelerini ve statik menü öğelerini bir kaynak olarak belirtmek için kullanılan bir **Gezinti Kaynağı** özelliği vardır.</span><span class="sxs-lookup"><span data-stu-id="56d5b-119">The navigation menu has a **Navigation Source** property that is used to specify Retail Server navigation menu items and static menu items as a source.</span></span> <span data-ttu-id="56d5b-120">Statik menü öğeleri kaynak olarak belirtilirse, sitedeki diğer sayfalara göreli bağlantılar sağlanabilir.</span><span class="sxs-lookup"><span data-stu-id="56d5b-120">If static menu items are specified as a source, relative links to other pages on the site can be provided.</span></span> <span data-ttu-id="56d5b-121">Yapılandırılmış öğeler daha sonra üstbilgi gezintisi olarak görünür.</span><span class="sxs-lookup"><span data-stu-id="56d5b-121">Configured items then appear as header navigation.</span></span> 
- <span data-ttu-id="56d5b-122">**Arama** – Arama modülü, kullanıcıların ürün aramak için arama terimleri girmesine izin verir.</span><span class="sxs-lookup"><span data-stu-id="56d5b-122">**Search** – The search module lets users enter search terms to search for products.</span></span> <span data-ttu-id="56d5b-123">**Site Ayarları \>Uzantılar**'da, varsayılan arama sayfasının URL'si ve arama sorgusu parametreleri girilmelidir.</span><span class="sxs-lookup"><span data-stu-id="56d5b-123">The URL of the default search page and the search query parameters must be provided at **Site Settings \> Extensions**.</span></span> <span data-ttu-id="56d5b-124">Arama modülünde, arama düğmesini veya etiketi gereksinim duyduğunuz şekilde gizlemenize olanak sağlayan özellikler vardır.</span><span class="sxs-lookup"><span data-stu-id="56d5b-124">The search module has properties that let you suppress the search button or label as you require.</span></span> <span data-ttu-id="56d5b-125">Arama modülü ürün, anahtar sözcük ve kategori arama sonuçları gibi otomatik öneri seçeneklerini de destekler.</span><span class="sxs-lookup"><span data-stu-id="56d5b-125">The search module also supports auto-suggest options, such as product, keyword, and category search results.</span></span>

## <a name="create-a-header-module-for-a-page"></a><span data-ttu-id="56d5b-126">Sayfa için üst bilgi modülü oluşturma</span><span class="sxs-lookup"><span data-stu-id="56d5b-126">Create a header module for a page</span></span>

<span data-ttu-id="56d5b-127">Bir üst bilgi modülü oluşturmak için şu adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="56d5b-127">To create a header module, follow these steps.</span></span>

1. <span data-ttu-id="56d5b-128">**Üst bilgi parçası** olarak adlandırılan bir parça oluşturun ve buna bir kapsayıcı modülü ekleyin.</span><span class="sxs-lookup"><span data-stu-id="56d5b-128">Create a fragment that is named **Header fragment**, and add a container module to it.</span></span>
1. <span data-ttu-id="56d5b-129">Konteyner modülü için özellik panosunda **Genişlik** özelliğini **Konteyneri doldur**'a ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="56d5b-129">In the property pane for the container module, set the **Width** property to **Fill container**.</span></span>
1. <span data-ttu-id="56d5b-130">Kapsayıcı modülüne promosyon başlığı ve tanımlama bilgisi izin modülleri ekleyin.</span><span class="sxs-lookup"><span data-stu-id="56d5b-130">Add promo banner and cookie consent modules to the container module.</span></span>
1. <span data-ttu-id="56d5b-131">Parçaya başka bir kapsayıcı modülü ekleyin ve **Genişlik** özelliğinin ayarını **Kapsayıcıya sığdır** yapın.</span><span class="sxs-lookup"><span data-stu-id="56d5b-131">Add another container module to the fragment, and set the **Width** property to **Fill container**.</span></span>
1. <span data-ttu-id="56d5b-132">İkinci kapsayıcı modülüne bir üst bilgi modülü ekleyin.</span><span class="sxs-lookup"><span data-stu-id="56d5b-132">Add a header module to the second container module.</span></span>
1. <span data-ttu-id="56d5b-133">Üst bilgi modülünün **Gezinti menüsü** yuvasında bir gezinti menüsü modülü ekleyin.</span><span class="sxs-lookup"><span data-stu-id="56d5b-133">In the **Navigation menu** slot of the header module, add a navigation menu module.</span></span> 
1. <span data-ttu-id="56d5b-134">Gezinti menüsü modülünün özellik bölmesinde, gezinti menüsü modülünün özelliklerini yapılandırın.</span><span class="sxs-lookup"><span data-stu-id="56d5b-134">In the property pane for the navigation menu module, configure the properties of the navigation menu module.</span></span>
1. <span data-ttu-id="56d5b-135">Üst bilgi modülünün **Arama** yuvasında bir arama modülü ekleyin.</span><span class="sxs-lookup"><span data-stu-id="56d5b-135">In the **Search** slot of the header module, add a search module.</span></span> 
1. <span data-ttu-id="56d5b-136">Arama modülünün özellik bölmesinde, arama modülünün özelliklerini yapılandırın.</span><span class="sxs-lookup"><span data-stu-id="56d5b-136">In the property pane for the search module, configure the properties of the search module.</span></span> 
1. <span data-ttu-id="56d5b-137">Sayfa parçasını kaydedin, düzenlemeyi bitirin ve yayımlayın.</span><span class="sxs-lookup"><span data-stu-id="56d5b-137">Save the page fragment, finish editing it, and publish it.</span></span> 

<span data-ttu-id="56d5b-138">Üstbilginin her sayfada göründüğünü garantilemek için, site için oluşturulan her sayfa şablonunda aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="56d5b-138">To help guarantee that a header appears on every page, follow these steps on every page template that is created for the site.</span></span>

1. <span data-ttu-id="56d5b-139">Varsayılan sayfanın **Ana** yuvasında, üst bilgi modülünü içeren üst bilgi sayfa parçasını üst bilgiye ekleyin.</span><span class="sxs-lookup"><span data-stu-id="56d5b-139">In the **Main** slot of the default page, add the header page fragment that contains the header module to the header.</span></span>
1. <span data-ttu-id="56d5b-140">Şablonu kaydedin, düzenlemeyi bitirin ve sonra yayınlayın.</span><span class="sxs-lookup"><span data-stu-id="56d5b-140">Save the template, finish editing it, and publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="56d5b-141">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="56d5b-141">Additional resources</span></span>

[<span data-ttu-id="56d5b-142">Başlangıç paketine genel bakış</span><span class="sxs-lookup"><span data-stu-id="56d5b-142">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="56d5b-143">Konteyner modülü</span><span class="sxs-lookup"><span data-stu-id="56d5b-143">Container module</span></span>](add-container-module.md)

[<span data-ttu-id="56d5b-144">Satın alma kutusu modülü</span><span class="sxs-lookup"><span data-stu-id="56d5b-144">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="56d5b-145">Sepet modülü</span><span class="sxs-lookup"><span data-stu-id="56d5b-145">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="56d5b-146">Ödeme modülü</span><span class="sxs-lookup"><span data-stu-id="56d5b-146">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="56d5b-147">Sipariş onayı modülü</span><span class="sxs-lookup"><span data-stu-id="56d5b-147">Order confirmation module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="56d5b-148">Üst bilgi modülü</span><span class="sxs-lookup"><span data-stu-id="56d5b-148">Header module</span></span>](author-header-module.md)

[<span data-ttu-id="56d5b-149">Alt bilgi modülü</span><span class="sxs-lookup"><span data-stu-id="56d5b-149">Footer module</span></span>](author-footer-module.md)
