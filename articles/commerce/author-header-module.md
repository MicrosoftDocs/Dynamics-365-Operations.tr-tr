---
title: Üst bilgi modülü
description: Bu konu üstbilgi modüllerini ve bunların nasıl Microsoft Dynamics 365 Commerce'te oluşturacağını açıklamaktadır ve kapsamaktadır.
author: anupamar
manager: annbe
ms.date: 10/31/2019
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
ms.openlocfilehash: cc98419077f6f563ea2265d4e68ba809971cfbd6
ms.sourcegitcommit: ff93b8f6a11993f2cd00be2da7aa77ef0d950ab8
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 12/03/2019
ms.locfileid: "2885490"
---
# <a name="header-module"></a><span data-ttu-id="5e50d-103">Üst bilgi modülü</span><span class="sxs-lookup"><span data-stu-id="5e50d-103">Header module</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="5e50d-104">Bu konu üstbilgi modüllerini ve bunların nasıl Microsoft Dynamics 365 Commerce'te oluşturacağını açıklamaktadır ve kapsamaktadır.</span><span class="sxs-lookup"><span data-stu-id="5e50d-104">This topic covers header modules and describes how to create them in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="5e50d-105">Genel Bakış</span><span class="sxs-lookup"><span data-stu-id="5e50d-105">Overview</span></span>

<span data-ttu-id="5e50d-106">Üst bilgi modülü, bir sayfanın başlığında gösterilecek tüm modülleri barındırmak için kullanılan özel bir konteynerdir.</span><span class="sxs-lookup"><span data-stu-id="5e50d-106">A header module is a special container that is used to host all the modules that will be shown in a page's header.</span></span> <span data-ttu-id="5e50d-107">Örneğin, site logonuzu, gezinti hiyerarşisine bağlantıları, sitedeki diğer sayfalara bağlantıları ve arama çubuğunu içerebilir.</span><span class="sxs-lookup"><span data-stu-id="5e50d-107">For example, it can include your site logo, links to the navigation hierarchy, links to other pages on the site, and the search bar.</span></span>

<span data-ttu-id="5e50d-108">Üst bilgi modülü, sitenin (yani bir masaüstü cihazı veya mobil cihaz) üzerinde göründüğü cihaz için otomatik olarak en iyi duruma getirilmiştir.</span><span class="sxs-lookup"><span data-stu-id="5e50d-108">A header module is automatically optimized for the device that the site is being viewed on (that is, a desktop device or a mobile device).</span></span> <span data-ttu-id="5e50d-109">Örneğin, bir mobil cihazda, gezinti çubuğu bir **menü** düğmesine (bazen *hamburger menüsü* olarak da adlandırılır) daraltılır.</span><span class="sxs-lookup"><span data-stu-id="5e50d-109">For example, on a mobile device, the navigation bar is collapsed into a **Menu** button (which is sometimes referred to as a *hamburger menu*).</span></span>

## <a name="properties-of-a-header"></a><span data-ttu-id="5e50d-110">Üstbilginin özellikleri</span><span class="sxs-lookup"><span data-stu-id="5e50d-110">Properties of a header</span></span>

<span data-ttu-id="5e50d-111">Birçok konteyner gibi bir üstbilgi modülü de **başlık** ve **genişlik** için özellikleri destekler.</span><span class="sxs-lookup"><span data-stu-id="5e50d-111">Like generic containers, a header module supports the **heading** and **width** properties.</span></span>

<span data-ttu-id="5e50d-112">Üst bilgi modülü birden çok yuvaya sahip.</span><span class="sxs-lookup"><span data-stu-id="5e50d-112">A header module has multiple slots.</span></span> <span data-ttu-id="5e50d-113">Örneğin, bir bilgi iletisi, gezinme menüsü, logo, arama çubuğu, sepet simgesi, istek listesi simgesi ve hesap bilgileri için yuvalar vardır.</span><span class="sxs-lookup"><span data-stu-id="5e50d-113">For example, there are slots for an informational message, navigation menu, logo, search bar, cart icon, wish list icon, and account information.</span></span> <span data-ttu-id="5e50d-114">Her yuva, belirli bir modül kümesini destekler.</span><span class="sxs-lookup"><span data-stu-id="5e50d-114">Each slot supports a specific set of modules.</span></span>

## <a name="modules-that-are-available-in-a-header-module"></a><span data-ttu-id="5e50d-115">Üstbilgi modülünde kullanılabilen modüller</span><span class="sxs-lookup"><span data-stu-id="5e50d-115">Modules that are available in a header module</span></span>

<span data-ttu-id="5e50d-116">Aşağıdaki modüller bir üstbilgi modülünde kullanılabilir:</span><span class="sxs-lookup"><span data-stu-id="5e50d-116">The following modules can be used in a header module:</span></span>

- <span data-ttu-id="5e50d-117">**Gezinti menüsü** – Gezinti menüsü, kanal gezinti hiyerarşisini ve diğer statik gezinti bağlantılarını temsil eder.</span><span class="sxs-lookup"><span data-stu-id="5e50d-117">**Navigation menu** – The navigation menu represents the channel navigation hierarchy and other static navigation links.</span></span> <span data-ttu-id="5e50d-118">Kanal gezinme hiyerarşisi Dynamics 365 Retail'de yapılandırılabilir.</span><span class="sxs-lookup"><span data-stu-id="5e50d-118">The channel navigation hierarchy can be configured in Dynamics 365 Retail.</span></span> <span data-ttu-id="5e50d-119">Yapılandırılmış öğeler daha sonra üstbilgi gezintisi olarak görünür.</span><span class="sxs-lookup"><span data-stu-id="5e50d-119">Configured items then appear as header navigation.</span></span> <span data-ttu-id="5e50d-120">Ek olarak, statik gezinti bağlantıları yapılandırılabilir ve e-ticaret sitesindeki diğer sayfalara göreli bağlantılar sağlanabilir.</span><span class="sxs-lookup"><span data-stu-id="5e50d-120">In addition, static navigation links can be configured, and relative links to other pages on the e-Commerce site can be provided.</span></span> <span data-ttu-id="5e50d-121">Üstbilginin kendisi sola, sağa veya ortaya hizalanabilir.</span><span class="sxs-lookup"><span data-stu-id="5e50d-121">The header itself can be aligned left, right, or center.</span></span>
- <span data-ttu-id="5e50d-122">**Sepet simgesi** – Sepet simgesi sepeti temsil eden özel bir simgedir.</span><span class="sxs-lookup"><span data-stu-id="5e50d-122">**Cart icon** – The cart icon is a special icon that represents the cart.</span></span> <span data-ttu-id="5e50d-123">Başlıkta gösterilir ve sepetteki öğelerin sayısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="5e50d-123">It's shown in the header and indicates the number of items in the cart.</span></span> <span data-ttu-id="5e50d-124">Sepet sayfasına bir bağlantı, bir simgenin simgesiyle etkileşimde bulunduklarında sepet sayfasına yönlendirilebilmeleri için, sepet simgesine eşlik etmelidir.</span><span class="sxs-lookup"><span data-stu-id="5e50d-124">A link to the cart page should accompany the cart icon, so that customers can be redirected to the cart page when they interact with the icon.</span></span>
- <span data-ttu-id="5e50d-125">**İstek listesi simgesi** – Son giriş listesi simgesi başlıkta gösterilir ve müşterinin istek listesine eklenen maddelerin sayısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="5e50d-125">**Wish list icon** – The wish list icon is shown in the header and indicates the number of items that have been added to the customer's wish list.</span></span> <span data-ttu-id="5e50d-126">İstek listesi sayfasına bir bağlantı, bu simgesiyle etkileşimde bulunduklarında istek listesi sayfasına yönlendirilebilmeleri için, sepet simgesine eşlik etmelidir.</span><span class="sxs-lookup"><span data-stu-id="5e50d-126">A link to the wish list page should accompany this icon, so that customers can be redirected to the wish list page when they interact with the icon.</span></span>
- <span data-ttu-id="5e50d-127">**Oturum açma modülü** - Üstbilgide oturum açma modülü gösteriliyor.</span><span class="sxs-lookup"><span data-stu-id="5e50d-127">**Sign-in module** – The sign-in module is shown in the header.</span></span> <span data-ttu-id="5e50d-128">Müşterilerimiz, hesaplarına oturum açmalarını veya bir hesap için kaydolmasına olanak tanır.</span><span class="sxs-lookup"><span data-stu-id="5e50d-128">It lets customers either sign in to their account or sign up for an account.</span></span> <span data-ttu-id="5e50d-129">Müşteri önceden oturum açmışsa modül hesap sayfası, sipariş geçmişi sayfası veya başka bir sayfaya olan bağlantıları gösterecek şekilde konfigüre edilebilir.</span><span class="sxs-lookup"><span data-stu-id="5e50d-129">If the customer is already signed in, the module can be configured to show links to the account page, order history page, or another page.</span></span>
- <span data-ttu-id="5e50d-130">**Logo modülü** – Bu modül, perakendecileri ve markayı temsil eden logoyu gösterir.</span><span class="sxs-lookup"><span data-stu-id="5e50d-130">**Logo module** – This module shows the logo that represents the retailer and brand.</span></span> <span data-ttu-id="5e50d-131">Bağlantısı olan bir görüntüdür.</span><span class="sxs-lookup"><span data-stu-id="5e50d-131">It's an image that has a link.</span></span> <span data-ttu-id="5e50d-132">Bağlantı genellikle giriş sayfasına yeniden yönlendirilecek şekilde yapılandırılır, böylece müşteriler sitedeki herhangi bir sayfadan giriş sayfasına hızla dönebilir.</span><span class="sxs-lookup"><span data-stu-id="5e50d-132">The link is typically configured so that it has a redirect to the home page, Therefore, customers can quickly return to the home page from any page on the site.</span></span>
- <span data-ttu-id="5e50d-133">**Uyarı** – Başlıkta bir uyarı görünür ve sitedeki tüm sayfalar için geçerli olan bir satır içi iletiyi göstermek için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="5e50d-133">**Alert** – An alert appears in the header and is used to show an inline message that applies to all pages on the site.</span></span> <span data-ttu-id="5e50d-134">Örneğin, bir uyarı "Yıllık satış 2 günde bitiyor" gibi bir mesaj gösterebilir.</span><span class="sxs-lookup"><span data-stu-id="5e50d-134">For example, an alert might show a message such as "Annual sale ends in 2 days."</span></span>
- <span data-ttu-id="5e50d-135">**Arama çubuğu** – Arama çubuğu kullanıcıların ürün arayabilmeleri için arama terimleri girmesine izin verir.</span><span class="sxs-lookup"><span data-stu-id="5e50d-135">**Search bar** – The search bar lets users enter search terms so that they can search for products.</span></span> <span data-ttu-id="5e50d-136">Modül, arama sonuçları sayfasının URL'siyle konfigüre edilmelidir.</span><span class="sxs-lookup"><span data-stu-id="5e50d-136">The module must be configured with the URL of the search results page.</span></span> <span data-ttu-id="5e50d-137">Sorgu dizesi parametresi yapılandırılabilir (varsayılan değer **"q"** dir).</span><span class="sxs-lookup"><span data-stu-id="5e50d-137">The query string parameter can be configured (the default value is **"q"**).</span></span> <span data-ttu-id="5e50d-138">Arama çubuğu, otomatik önerme modülünün eklenmesi gereken bir autoönerme yuvasına sahiptir.</span><span class="sxs-lookup"><span data-stu-id="5e50d-138">The search bar has an autosuggest slot where the autosuggest module should be added.</span></span>
- <span data-ttu-id="5e50d-139">**Otomatik öner** – otomatik öner modülü otomatik olarak önerilen sonuçları gösterir.</span><span class="sxs-lookup"><span data-stu-id="5e50d-139">**Autosuggest** – The autosuggest module shows automatically suggested results.</span></span> <span data-ttu-id="5e50d-140">Bu sonuçlar anahtar sözcükler, ürünler veya arama teriminin bulunduğu kategoriler olabilir.</span><span class="sxs-lookup"><span data-stu-id="5e50d-140">These results can be keywords, products, or categories where the search term is found.</span></span>

## <a name="create-a-header-module"></a><span data-ttu-id="5e50d-141">Başlık modülü oluşturma</span><span class="sxs-lookup"><span data-stu-id="5e50d-141">Create a header module</span></span>

<span data-ttu-id="5e50d-142">Bir üst bilgi modülü oluşturmak için şu adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="5e50d-142">To create a header module, follow these steps.</span></span>

1. <span data-ttu-id="5e50d-143">Üstbilgi modülü içeren bir sayfa parçası oluşturun.</span><span class="sxs-lookup"><span data-stu-id="5e50d-143">Create a page fragment that includes a header module.</span></span>
1. <span data-ttu-id="5e50d-144">Üstbilgi modülündeki yuvalara modüller ekleyin.</span><span class="sxs-lookup"><span data-stu-id="5e50d-144">Add modules to the slots in the header module.</span></span>
1. <span data-ttu-id="5e50d-145">Her modülün ayarlarını güncelleştirin.</span><span class="sxs-lookup"><span data-stu-id="5e50d-145">Update the settings for each module.</span></span>
1. <span data-ttu-id="5e50d-146">Sayfa parçasını kaydedin.</span><span class="sxs-lookup"><span data-stu-id="5e50d-146">Save the page fragment.</span></span> 
1. <span data-ttu-id="5e50d-147">Sayfayı giriş yapın ve yayımlayın.</span><span class="sxs-lookup"><span data-stu-id="5e50d-147">Check in the page, and publish it.</span></span>

<span data-ttu-id="5e50d-148">Üstbilginin her sayfada göründüğünü garantilemek için, site için oluşturulan her sayfa şablonunda aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="5e50d-148">To help guarantee that a header appears on every page, follow these steps on every page template that is created for the site.</span></span>

1. <span data-ttu-id="5e50d-149">Varsayılan sayfada üstbilgi modülünü içeren sayfa parçasını ana yuvadaki üstbilgiye ekleyin.</span><span class="sxs-lookup"><span data-stu-id="5e50d-149">On the default page, add the page fragment containing the header module to the header in the main slot.</span></span>
1. <span data-ttu-id="5e50d-150">Şablonu kaydedin.</span><span class="sxs-lookup"><span data-stu-id="5e50d-150">Save the template.</span></span> 
1. <span data-ttu-id="5e50d-151">Şablonu giriş yapın ve yayımlayın.</span><span class="sxs-lookup"><span data-stu-id="5e50d-151">Check in the template, and publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="5e50d-152">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="5e50d-152">Additional resources</span></span>

[<span data-ttu-id="5e50d-153">Başlangıç paketine genel bakış</span><span class="sxs-lookup"><span data-stu-id="5e50d-153">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="5e50d-154">Konteyner modülü</span><span class="sxs-lookup"><span data-stu-id="5e50d-154">Container module</span></span>](add-container-module.md)

[<span data-ttu-id="5e50d-155">Satın alma kutusu modülü</span><span class="sxs-lookup"><span data-stu-id="5e50d-155">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="5e50d-156">Sepet modülü</span><span class="sxs-lookup"><span data-stu-id="5e50d-156">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="5e50d-157">Ödeme modülü</span><span class="sxs-lookup"><span data-stu-id="5e50d-157">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="5e50d-158">Sipariş onayı modülü</span><span class="sxs-lookup"><span data-stu-id="5e50d-158">Order confirmation module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="5e50d-159">Üst bilgi modülü</span><span class="sxs-lookup"><span data-stu-id="5e50d-159">Header module</span></span>](author-header-module.md)

[<span data-ttu-id="5e50d-160">Alt bilgi modülü</span><span class="sxs-lookup"><span data-stu-id="5e50d-160">Footer module</span></span>](author-footer-module.md)
