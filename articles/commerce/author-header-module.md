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
ms.openlocfilehash: d393701dacb88ab03a4b56724d93c794da6bb5c8
ms.sourcegitcommit: 295d940a345879b3dfc5991e387b91c7257019ea
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/01/2019
ms.locfileid: "2697287"
---
# <a name="header-module"></a><span data-ttu-id="2c59c-103">Üst bilgi modülü</span><span class="sxs-lookup"><span data-stu-id="2c59c-103">Header module</span></span>

<span data-ttu-id="2c59c-104">[!include [banner](includes/preview-banner.md)] [!include [banner](includes/banner.md)]</span><span class="sxs-lookup"><span data-stu-id="2c59c-104">[!include [banner]includes/preview-banner.md)] [!include [banner](includes/banner.md)]</span></span>

<span data-ttu-id="2c59c-105">Bu konu üstbilgi modüllerini ve bunların nasıl Microsoft Dynamics 365 Commerce'te oluşturacağını açıklamaktadır ve kapsamaktadır.</span><span class="sxs-lookup"><span data-stu-id="2c59c-105">This topic covers header modules and describes how to create them in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="2c59c-106">Genel Bakış</span><span class="sxs-lookup"><span data-stu-id="2c59c-106">Overview</span></span>

<span data-ttu-id="2c59c-107">Üst bilgi modülü, bir sayfanın başlığında gösterilecek tüm modülleri barındırmak için kullanılan özel bir konteynerdir.</span><span class="sxs-lookup"><span data-stu-id="2c59c-107">A header module is a special container that is used to host all the modules that will be shown in a page's header.</span></span> <span data-ttu-id="2c59c-108">Örneğin, site logonuzu, gezinti hiyerarşisine bağlantıları, sitedeki diğer sayfalara bağlantıları ve arama çubuğunu içerebilir.</span><span class="sxs-lookup"><span data-stu-id="2c59c-108">For example, it can include your site logo, links to the navigation hierarchy, links to other pages on the site, and the search bar.</span></span>

<span data-ttu-id="2c59c-109">Üst bilgi modülü, sitenin (yani bir masaüstü cihazı veya mobil cihaz) üzerinde göründüğü cihaz için otomatik olarak en iyi duruma getirilmiştir.</span><span class="sxs-lookup"><span data-stu-id="2c59c-109">A header module is automatically optimized for the device that the site is being viewed on (that is, a desktop device or a mobile device).</span></span> <span data-ttu-id="2c59c-110">Örneğin, bir mobil cihazda, gezinti çubuğu bir **menü** düğmesine (bazen *hamburger menüsü* olarak da adlandırılır) daraltılır.</span><span class="sxs-lookup"><span data-stu-id="2c59c-110">For example, on a mobile device, the navigation bar is collapsed into a **Menu** button (which is sometimes referred to as a *hamburger menu*).</span></span>

## <a name="properties-of-a-header"></a><span data-ttu-id="2c59c-111">Üstbilginin özellikleri</span><span class="sxs-lookup"><span data-stu-id="2c59c-111">Properties of a header</span></span>

<span data-ttu-id="2c59c-112">Birçok konteyner gibi bir üstbilgi modülü de **başlık** ve **genişlik** için özellikleri destekler.</span><span class="sxs-lookup"><span data-stu-id="2c59c-112">Like generic containers, a header module supports the **heading** and **width** properties.</span></span>

<span data-ttu-id="2c59c-113">Üst bilgi modülü birden çok yuvaya sahip.</span><span class="sxs-lookup"><span data-stu-id="2c59c-113">A header module has multiple slots.</span></span> <span data-ttu-id="2c59c-114">Örneğin, bir bilgi iletisi, gezinme menüsü, logo, arama çubuğu, sepet simgesi, istek listesi simgesi ve hesap bilgileri için yuvalar vardır.</span><span class="sxs-lookup"><span data-stu-id="2c59c-114">For example, there are slots for an informational message, navigation menu, logo, search bar, cart icon, wish list icon, and account information.</span></span> <span data-ttu-id="2c59c-115">Her yuva, belirli bir modül kümesini destekler.</span><span class="sxs-lookup"><span data-stu-id="2c59c-115">Each slot supports a specific set of modules.</span></span>

## <a name="modules-that-are-available-in-a-header-module"></a><span data-ttu-id="2c59c-116">Üstbilgi modülünde kullanılabilen modüller</span><span class="sxs-lookup"><span data-stu-id="2c59c-116">Modules that are available in a header module</span></span>

<span data-ttu-id="2c59c-117">Aşağıdaki modüller bir üstbilgi modülünde kullanılabilir:</span><span class="sxs-lookup"><span data-stu-id="2c59c-117">The following modules can be used in a header module:</span></span>

- <span data-ttu-id="2c59c-118">**Gezinti menüsü** – Gezinti menüsü, kanal gezinti hiyerarşisini ve diğer statik gezinti bağlantılarını temsil eder.</span><span class="sxs-lookup"><span data-stu-id="2c59c-118">**Navigation menu** – The navigation menu represents the channel navigation hierarchy and other static navigation links.</span></span> <span data-ttu-id="2c59c-119">Kanal gezinme hiyerarşisi Dynamics 365 Retail'de yapılandırılabilir.</span><span class="sxs-lookup"><span data-stu-id="2c59c-119">The channel navigation hierarchy can be configured in Dynamics 365 Retail.</span></span> <span data-ttu-id="2c59c-120">Yapılandırılmış öğeler daha sonra üstbilgi gezintisi olarak görünür.</span><span class="sxs-lookup"><span data-stu-id="2c59c-120">Configured items then appear as header navigation.</span></span> <span data-ttu-id="2c59c-121">Ek olarak, statik gezinti bağlantıları yapılandırılabilir ve e-ticaret sitesindeki diğer sayfalara göreli bağlantılar sağlanabilir.</span><span class="sxs-lookup"><span data-stu-id="2c59c-121">In addition, static navigation links can be configured, and relative links to other pages on the e-Commerce site can be provided.</span></span> <span data-ttu-id="2c59c-122">Üstbilginin kendisi sola, sağa veya ortaya hizalanabilir.</span><span class="sxs-lookup"><span data-stu-id="2c59c-122">The header itself can be aligned left, right, or center.</span></span>
- <span data-ttu-id="2c59c-123">**Sepet simgesi** – Sepet simgesi sepeti temsil eden özel bir simgedir.</span><span class="sxs-lookup"><span data-stu-id="2c59c-123">**Cart icon** – The cart icon is a special icon that represents the cart.</span></span> <span data-ttu-id="2c59c-124">Başlıkta gösterilir ve sepetteki öğelerin sayısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="2c59c-124">It's shown in the header and indicates the number of items in the cart.</span></span> <span data-ttu-id="2c59c-125">Sepet sayfasına bir bağlantı, bir simgenin simgesiyle etkileşimde bulunduklarında sepet sayfasına yönlendirilebilmeleri için, sepet simgesine eşlik etmelidir.</span><span class="sxs-lookup"><span data-stu-id="2c59c-125">A link to the cart page should accompany the cart icon, so that customers can be redirected to the cart page when they interact with the icon.</span></span>
- <span data-ttu-id="2c59c-126">**İstek listesi simgesi** – Son giriş listesi simgesi başlıkta gösterilir ve müşterinin istek listesine eklenen maddelerin sayısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="2c59c-126">**Wish list icon** – The wish list icon is shown in the header and indicates the number of items that have been added to the customer's wish list.</span></span> <span data-ttu-id="2c59c-127">İstek listesi sayfasına bir bağlantı, bu simgesiyle etkileşimde bulunduklarında istek listesi sayfasına yönlendirilebilmeleri için, sepet simgesine eşlik etmelidir.</span><span class="sxs-lookup"><span data-stu-id="2c59c-127">A link to the wish list page should accompany this icon, so that customers can be redirected to the wish list page when they interact with the icon.</span></span>
- <span data-ttu-id="2c59c-128">**Oturum açma modülü** - Üstbilgide oturum açma modülü gösteriliyor.</span><span class="sxs-lookup"><span data-stu-id="2c59c-128">**Sign-in module** – The sign-in module is shown in the header.</span></span> <span data-ttu-id="2c59c-129">Müşterilerimiz, hesaplarına oturum açmalarını veya bir hesap için kaydolmasına olanak tanır.</span><span class="sxs-lookup"><span data-stu-id="2c59c-129">It lets customers either sign in to their account or sign up for an account.</span></span> <span data-ttu-id="2c59c-130">Müşteri önceden oturum açmışsa modül hesap sayfası, sipariş geçmişi sayfası veya başka bir sayfaya olan bağlantıları gösterecek şekilde konfigüre edilebilir.</span><span class="sxs-lookup"><span data-stu-id="2c59c-130">If the customer is already signed in, the module can be configured to show links to the account page, order history page, or another page.</span></span>
- <span data-ttu-id="2c59c-131">**Logo modülü** – Bu modül, perakendecileri ve markayı temsil eden logoyu gösterir.</span><span class="sxs-lookup"><span data-stu-id="2c59c-131">**Logo module** – This module shows the logo that represents the retailer and brand.</span></span> <span data-ttu-id="2c59c-132">Bağlantısı olan bir görüntüdür.</span><span class="sxs-lookup"><span data-stu-id="2c59c-132">It's an image that has a link.</span></span> <span data-ttu-id="2c59c-133">Bağlantı genellikle giriş sayfasına yeniden yönlendirilecek şekilde yapılandırılır, böylece müşteriler sitedeki herhangi bir sayfadan giriş sayfasına hızla dönebilir.</span><span class="sxs-lookup"><span data-stu-id="2c59c-133">The link is typically configured so that it has a redirect to the home page, Therefore, customers can quickly return to the home page from any page on the site.</span></span>
- <span data-ttu-id="2c59c-134">**Uyarı** – Başlıkta bir uyarı görünür ve sitedeki tüm sayfalar için geçerli olan bir satır içi iletiyi göstermek için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="2c59c-134">**Alert** – An alert appears in the header and is used to show an inline message that applies to all pages on the site.</span></span> <span data-ttu-id="2c59c-135">Örneğin, bir uyarı "Yıllık satış 2 günde bitiyor" gibi bir mesaj gösterebilir.</span><span class="sxs-lookup"><span data-stu-id="2c59c-135">For example, an alert might show a message such as "Annual sale ends in 2 days."</span></span>
- <span data-ttu-id="2c59c-136">**Arama çubuğu** – Arama çubuğu kullanıcıların ürün arayabilmeleri için arama terimleri girmesine izin verir.</span><span class="sxs-lookup"><span data-stu-id="2c59c-136">**Search bar** – The search bar lets users enter search terms so that they can search for products.</span></span> <span data-ttu-id="2c59c-137">Modül, arama sonuçları sayfasının URL'siyle konfigüre edilmelidir.</span><span class="sxs-lookup"><span data-stu-id="2c59c-137">The module must be configured with the URL of the search results page.</span></span> <span data-ttu-id="2c59c-138">Sorgu dizesi parametresi yapılandırılabilir (varsayılan değer **"q"** dir).</span><span class="sxs-lookup"><span data-stu-id="2c59c-138">The query string parameter can be configured (the default value is **"q"**).</span></span> <span data-ttu-id="2c59c-139">Arama çubuğu, otomatik önerme modülünün eklenmesi gereken bir autoönerme yuvasına sahiptir.</span><span class="sxs-lookup"><span data-stu-id="2c59c-139">The search bar has an autosuggest slot where the autosuggest module should be added.</span></span>
- <span data-ttu-id="2c59c-140">**Otomatik öner** – otomatik öner modülü otomatik olarak önerilen sonuçları gösterir.</span><span class="sxs-lookup"><span data-stu-id="2c59c-140">**Autosuggest** – The autosuggest module shows automatically suggested results.</span></span> <span data-ttu-id="2c59c-141">Bu sonuçlar anahtar sözcükler, ürünler veya arama teriminin bulunduğu kategoriler olabilir.</span><span class="sxs-lookup"><span data-stu-id="2c59c-141">These results can be keywords, products, or categories where the search term is found.</span></span>

## <a name="create-a-header-module"></a><span data-ttu-id="2c59c-142">Başlık modülü oluşturma</span><span class="sxs-lookup"><span data-stu-id="2c59c-142">Create a header module</span></span>

<span data-ttu-id="2c59c-143">Bir üst bilgi modülü oluşturmak için şu adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="2c59c-143">To create a header module, follow these steps.</span></span>

1. <span data-ttu-id="2c59c-144">Üstbilgi modülü içeren bir sayfa parçası oluşturun.</span><span class="sxs-lookup"><span data-stu-id="2c59c-144">Create a page fragment that includes a header module.</span></span>
1. <span data-ttu-id="2c59c-145">Üstbilgi modülündeki yuvalara modüller ekleyin.</span><span class="sxs-lookup"><span data-stu-id="2c59c-145">Add modules to the slots in the header module.</span></span>
1. <span data-ttu-id="2c59c-146">Her modülün ayarlarını güncelleştirin.</span><span class="sxs-lookup"><span data-stu-id="2c59c-146">Update the settings for each module.</span></span>
1. <span data-ttu-id="2c59c-147">Sayfa parçasını kaydedin.</span><span class="sxs-lookup"><span data-stu-id="2c59c-147">Save the page fragment.</span></span> 
1. <span data-ttu-id="2c59c-148">Sayfayı giriş yapın ve yayımlayın.</span><span class="sxs-lookup"><span data-stu-id="2c59c-148">Check in the page, and publish it.</span></span>

<span data-ttu-id="2c59c-149">Üstbilginin her sayfada göründüğünü garantilemek için, site için oluşturulan her sayfa şablonunda aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="2c59c-149">To help guarantee that a header appears on every page, follow these steps on every page template that is created for the site.</span></span>

1. <span data-ttu-id="2c59c-150">Varsayılan sayfada üstbilgi modülünü içeren sayfa parçasını ana yuvadaki üstbilgiye ekleyin.</span><span class="sxs-lookup"><span data-stu-id="2c59c-150">On the default page, add the page fragment containing the header module to the header in the main slot.</span></span>
1. <span data-ttu-id="2c59c-151">Şablonu kaydedin.</span><span class="sxs-lookup"><span data-stu-id="2c59c-151">Save the template.</span></span> 
1. <span data-ttu-id="2c59c-152">Şablonu giriş yapın ve yayımlayın.</span><span class="sxs-lookup"><span data-stu-id="2c59c-152">Check in the template, and publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="2c59c-153">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="2c59c-153">Additional resources</span></span>

[<span data-ttu-id="2c59c-154">Başlangıç paketine genel bakış</span><span class="sxs-lookup"><span data-stu-id="2c59c-154">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="2c59c-155">Konteyner modülü</span><span class="sxs-lookup"><span data-stu-id="2c59c-155">Container module</span></span>](add-container-module.md)

[<span data-ttu-id="2c59c-156">Satın alma kutusu modülü</span><span class="sxs-lookup"><span data-stu-id="2c59c-156">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="2c59c-157">Sepet modülü</span><span class="sxs-lookup"><span data-stu-id="2c59c-157">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="2c59c-158">Ödeme modülü</span><span class="sxs-lookup"><span data-stu-id="2c59c-158">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="2c59c-159">Sipariş onayı modülü</span><span class="sxs-lookup"><span data-stu-id="2c59c-159">Order confirmation module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="2c59c-160">Üst bilgi modülü</span><span class="sxs-lookup"><span data-stu-id="2c59c-160">Header module</span></span>](author-header-module.md)

[<span data-ttu-id="2c59c-161">Alt bilgi modülü</span><span class="sxs-lookup"><span data-stu-id="2c59c-161">Footer module</span></span>](author-footer-module.md)
