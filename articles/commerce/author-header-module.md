---
title: Üst bilgi modülü
description: Bu konu üst bilgi modüllerini kapsamakta ve Microsoft Dynamics 365 Commerce'te sayfa üst bilgilerinin nasıl oluşturacağını açıklamaktadır.
author: anupamar
manager: annbe
ms.date: 05/28/2020
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
ms.openlocfilehash: e7dde3ba1ad375b309ae66cc6d31ccad85615e45
ms.sourcegitcommit: 81f162f2d50557d7afe292c8d326618ba0bc3259
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/11/2020
ms.locfileid: "3686634"
---
# <a name="header-module"></a><span data-ttu-id="f4ced-103">Üst bilgi modülü</span><span class="sxs-lookup"><span data-stu-id="f4ced-103">Header module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="f4ced-104">Bu konu üst bilgi modüllerini kapsamakta ve Microsoft Dynamics 365 Commerce'te sayfa üst bilgilerinin nasıl oluşturacağını açıklamaktadır.</span><span class="sxs-lookup"><span data-stu-id="f4ced-104">This topic covers header modules and describes how to create page headers in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="f4ced-105">Genel Bakış</span><span class="sxs-lookup"><span data-stu-id="f4ced-105">Overview</span></span>

<span data-ttu-id="f4ced-106">Dynamics 365 Commerce'te sayfa üst bilgisi; başlık, gezinti menüsü, arama, promosyon başlığı ve tanımlama bilgisi izin modülleri gibi birden çok modülü kapsar.</span><span class="sxs-lookup"><span data-stu-id="f4ced-106">In Dynamics 365 Commerce, a page header comprises multiple modules, such as the header, navigation menu, search, promo banner, and cookie consent modules.</span></span> 

<span data-ttu-id="f4ced-107">Üst bilgi modülü bir site logosu, gezinti hiyerarşisine bağlantılar, sitedeki diğer sayfalara bağlantılar, bir sepet sembolü, bir istek listesi sembolü, oturum açma seçenekleri ve arama çubuğu içerir.</span><span class="sxs-lookup"><span data-stu-id="f4ced-107">The header module includes a site logo, links to the navigation hierarchy, links to other pages on the site, a cart symbol, a wishlist symbol, sign-in options, and the search bar.</span></span> <span data-ttu-id="f4ced-108">Üst bilgi modülü, sitenin (yani bir masaüstü cihaz veya mobil cihaz) görüntülendiği cihaz için otomatik olarak en iyi duruma getirilir.</span><span class="sxs-lookup"><span data-stu-id="f4ced-108">A header module is automatically optimized for the device that the site is being viewed on (in other words, for a desktop device or a mobile device).</span></span> <span data-ttu-id="f4ced-109">Örneğin, bir mobil cihazda, gezinti çubuğu bir **menü** düğmesine (bazen *hamburger menüsü* olarak da adlandırılır) daraltılır.</span><span class="sxs-lookup"><span data-stu-id="f4ced-109">For example, on a mobile device, the navigation bar is collapsed into a **Menu** button (which is sometimes referred to as a *hamburger menu*).</span></span>

<span data-ttu-id="f4ced-110">Aşağıdaki resimde giriş sayfasında kullanılan bir üstbilgi modülü örneği gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="f4ced-110">The following image shows an example of a header module on a home page.</span></span>

![üstbilgi modülü örneği](./media/ecommerce-header.png)

## <a name="properties-of-a-header-module"></a><span data-ttu-id="f4ced-112">Üst bilgi modülünün özellikleri</span><span class="sxs-lookup"><span data-stu-id="f4ced-112">Properties of a header module</span></span>

<span data-ttu-id="f4ced-113">Üst bilgi modülü **Logo resmi**, **Logo bağlantısı** ve **Hesabım bağlantıları** özelliklerini destekler.</span><span class="sxs-lookup"><span data-stu-id="f4ced-113">A header module supports **Logo image**, **Logo link**, and **My account links** properties.</span></span> 

<span data-ttu-id="f4ced-114">**Logo resmi** ve **Logo bağlantısı** özellikleri sayfada bir logo tanımlamak için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="f4ced-114">The **Logo image** and **Logo link** properties are used to define a logo on the page.</span></span> <span data-ttu-id="f4ced-115">Daha fazla bilgi için bkz. [Logo ekleme](add-logo.md).</span><span class="sxs-lookup"><span data-stu-id="f4ced-115">For more information, see [Add a logo](add-logo.md).</span></span> 

<span data-ttu-id="f4ced-116">**Hesabım bağlantıları** özelliği, site sahibinin üst bilgide hızlı bağlantıları göstermek istediği hesap sayfalarını tanımlamak için kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="f4ced-116">The **My account links** property can be used to define account pages that the site owner wants to show quick links for in the header.</span></span>

## <a name="modules-that-are-available-in-a-header-module"></a><span data-ttu-id="f4ced-117">Üstbilgi modülünde kullanılabilen modüller</span><span class="sxs-lookup"><span data-stu-id="f4ced-117">Modules that are available in a header module</span></span>

<span data-ttu-id="f4ced-118">Aşağıdaki modüller bir üstbilgi modülünde kullanılabilir:</span><span class="sxs-lookup"><span data-stu-id="f4ced-118">The following modules can be used in a header module:</span></span>

- <span data-ttu-id="f4ced-119">**Gezinti menüsü** – Gezinti menüsü, kanal gezinti hiyerarşisini ve diğer statik gezinti bağlantılarını temsil eder.</span><span class="sxs-lookup"><span data-stu-id="f4ced-119">**Navigation menu** – The navigation menu represents the channel navigation hierarchy and other static navigation links.</span></span> <span data-ttu-id="f4ced-120">Kanal gezinme hiyerarşisi Dynamics 365 Commerce'de yapılandırılabilir.</span><span class="sxs-lookup"><span data-stu-id="f4ced-120">The channel navigation hierarchy can be configured in Dynamics 365 Commerce.</span></span> <span data-ttu-id="f4ced-121">Gezinti menüsünde, Retail Server gezinti menüsü öğelerini ve statik menü öğelerini bir kaynak olarak belirtmek için kullanılan bir **Gezinti Kaynağı** özelliği vardır.</span><span class="sxs-lookup"><span data-stu-id="f4ced-121">The navigation menu has a **Navigation Source** property that is used to specify Retail Server navigation menu items and static menu items as a source.</span></span> <span data-ttu-id="f4ced-122">Statik menü öğeleri kaynak olarak belirtilirse, sitedeki diğer sayfalara göreli bağlantılar sağlanabilir.</span><span class="sxs-lookup"><span data-stu-id="f4ced-122">If static menu items are specified as a source, relative links to other pages on the site can be provided.</span></span> <span data-ttu-id="f4ced-123">Yapılandırılmış öğeler daha sonra üstbilgi gezintisi olarak görünür.</span><span class="sxs-lookup"><span data-stu-id="f4ced-123">Configured items then appear as header navigation.</span></span> 

- <span data-ttu-id="f4ced-124">**Arama** – Arama modülü, kullanıcıların ürün aramak için arama terimleri girmesine izin verir.</span><span class="sxs-lookup"><span data-stu-id="f4ced-124">**Search** – The search module lets users enter search terms to search for products.</span></span> <span data-ttu-id="f4ced-125">**Site Ayarları \>Uzantılar**'da, varsayılan arama sayfasının URL'si ve arama sorgusu parametreleri girilmelidir.</span><span class="sxs-lookup"><span data-stu-id="f4ced-125">The URL of the default search page and the search query parameters must be provided at **Site Settings \> Extensions**.</span></span> <span data-ttu-id="f4ced-126">Arama modülünde, arama düğmesini veya etiketi gereksinim duyduğunuz şekilde gizlemenize olanak sağlayan özellikler vardır.</span><span class="sxs-lookup"><span data-stu-id="f4ced-126">The search module has properties that let you suppress the search button or label as you require.</span></span> <span data-ttu-id="f4ced-127">Arama modülü ürün, anahtar sözcük ve kategori arama sonuçları gibi otomatik öneri seçeneklerini de destekler.</span><span class="sxs-lookup"><span data-stu-id="f4ced-127">The search module also supports auto-suggest options, such as product, keyword, and category search results.</span></span>

- <span data-ttu-id="f4ced-128">**Sepet simgesi** - Sepet simgesi modülü, belirli bir zamanda sepetteki öğelerin sayısını gösteren sepet simgesini temsil eder.</span><span class="sxs-lookup"><span data-stu-id="f4ced-128">**Cart icon** - The cart icon module represents the cart icon, which shows the number of items in the cart at any given time.</span></span> <span data-ttu-id="f4ced-129">Daha fazla bilgi için bkz. [Sepet simgesi modülü](cart-icon-module.md).</span><span class="sxs-lookup"><span data-stu-id="f4ced-129">For more information, see [Cart icon module](cart-icon-module.md).</span></span>

## <a name="create-a-header-module-for-a-page"></a><span data-ttu-id="f4ced-130">Sayfa için üst bilgi modülü oluşturma</span><span class="sxs-lookup"><span data-stu-id="f4ced-130">Create a header module for a page</span></span>

<span data-ttu-id="f4ced-131">Bir üst bilgi modülü oluşturmak için şu adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="f4ced-131">To create a header module, follow these steps.</span></span>

1. <span data-ttu-id="f4ced-132">**Parçalar**'a gidin ve yeni parça oluşturmak için **Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="f4ced-132">Go to **Fragments**, and select **New** to create a new fragment.</span></span>
1. <span data-ttu-id="f4ced-133">**Yeni sayfa parçası** iletişim kutusunda **Kapsayıcı** modülünü seçin, sayfa parçası için bir ad girin ve sonra **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="f4ced-133">In the **New page fragment** dialog box, select the **Container** module, enter a name for the page fragment, and then select **OK**.</span></span>
1. <span data-ttu-id="f4ced-134">**Varsayılan kapsayıcı** yuvasını seçin ve sağ tarafta bulunan Özellikler bölmesinde, **genişlik** özelliğini **Konteyneri doldur** olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="f4ced-134">Select the **Default container** slot, and then, in the properties pane on the right, set the **Width** property to **Fill container**.</span></span>
1. <span data-ttu-id="f4ced-135">**Varsayılan Konteyner** yuvası için üç nokta (**...**) düğmesini seçin ve **Modül Ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="f4ced-135">In the **Default container** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="f4ced-136">**Modül Ekle** iletişim kutusunda **Promosyon başlığı** ve **Çerez izni** modüller'i seçin, ve **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="f4ced-136">In the **Add Module** dialog box, select the **Promo banner** and **Cookie consent** modules, and then select **OK**.</span></span>
1. <span data-ttu-id="f4ced-137">**Varsayılan Konteyner** yuvası için üç nokta (**...**) düğmesini seçin ve **Modül Ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="f4ced-137">In the **Default container** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="f4ced-138">**Modül Ekle** iletişim kutusunda **Konteyner** modülünü seçin ve **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="f4ced-138">In the **Add Module** dialog box, select the **Container** module, and then select **OK**.</span></span>
1. <span data-ttu-id="f4ced-139">**Konteyner** yuvasını seçin ve sağ tarafta bulunan Özellikler bölmesinde, **genişlik** özelliğini **Konteyneri doldur** olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="f4ced-139">Select the **Container** slot, and then, in the properties pane on the right, set the **Width** property to **Fill container**.</span></span>
1. <span data-ttu-id="f4ced-140">**Konteyner** yuvası için üç nokta (**...**) düğmesini seçin ve **Modül Ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="f4ced-140">In the **Container** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="f4ced-141">**Modül Ekle** iletişim kutusunda **Başlık** modülünü seçin ve **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="f4ced-141">In the **Add Module** dialog box, select the **Header** module, and then select **OK**.</span></span>
1. <span data-ttu-id="f4ced-142">Başlık modülünü içeren **Gezinti menüsü** yuvasında üç noktayı (**...**) seçin ve sonra **Modül Ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="f4ced-142">In the **Navigation menu** slot of the header module, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="f4ced-143">**Modül Ekle** iletişim kutusunda **Gezinti meüsü** modülünü seçin ve **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="f4ced-143">In the **Add Module** dialog box, select the **Navigation menu** module, and then select **OK**.</span></span>
1. <span data-ttu-id="f4ced-144">Gezinti menüsü modülünün özellik bölmesinde, özelliklerini yapılandırın.</span><span class="sxs-lookup"><span data-stu-id="f4ced-144">In the property pane for the navigation menu module, configure the properties as needed.</span></span>
1. <span data-ttu-id="f4ced-145">Başlık modülünü içeren **Ara** yuvasında üç noktayı (**...**) seçin ve sonra **Modül Ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="f4ced-145">In the **Search** slot of the header module, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="f4ced-146">**Modül Ekle** iletişim kutusunda **Ara** modülünü seçin ve **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="f4ced-146">In the **Add Module** dialog box, select the **Search** module, and then select **OK**.</span></span>
1. <span data-ttu-id="f4ced-147">Arama modülünün özellik bölmesinde, özelliklerini yapılandırın.</span><span class="sxs-lookup"><span data-stu-id="f4ced-147">In the property pane for the search module, configure the properties as needed.</span></span>
1. <span data-ttu-id="f4ced-148">Başlık modülünü içeren **Sepet simgesi** yuvasında üç noktayı (**...**) seçin ve sonra **Modül Ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="f4ced-148">In the **Cart icon** slot of the header module, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="f4ced-149">**Modül Ekle** iletişim kutusunda **Sepet simgesi** modülünü seçin ve **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="f4ced-149">In the **Add Module** dialog box, select the **Cart icon** module, and then select **OK**.</span></span>
1. <span data-ttu-id="f4ced-150">Sepet simgesi modülünün özellik bölmesinde, özelliklerini yapılandırın.</span><span class="sxs-lookup"><span data-stu-id="f4ced-150">In the property pane for the cart icon module, configure the properties as needed.</span></span> <span data-ttu-id="f4ced-151">Kullanıcılar üzerinde gezinirken, sepet simgesinin bir sepet Özeti (mini sepet olarak da bilinir) göstermesini istiyorsanız, **mini sepeti göster**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="f4ced-151">If you want the cart icon to display a cart summary (also known as a mini cart) when users hover over it, select **Show mini cart**.</span></span>
1. <span data-ttu-id="f4ced-152">**Kaydet**'i seçin, parçayı iade etmek için **Düzenlemeyi bitir**'i ve ardından yayımlamak için **Yayımla**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="f4ced-152">Select **Save**, select **Finish editing** to check in the fragment, and then select **Publish** to publish it.</span></span>

<span data-ttu-id="f4ced-153">Üstbilginin her sayfada göründüğünü garantilemek için, site için oluşturulan her sayfa şablonunda aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="f4ced-153">To help guarantee that a header appears on every page, follow these steps on every page template that is created for the site.</span></span>

1. <span data-ttu-id="f4ced-154">**Varsayılan sayfanın** **üstbilgi** yuvasında, altbilgi modülünde, oluşturduğunuz altbilgi parçasını ekleyin.</span><span class="sxs-lookup"><span data-stu-id="f4ced-154">In the **Header** slot of the **Default page** module, add the footer fragment that you created.</span></span>
1. <span data-ttu-id="f4ced-155">**Kaydet**'i seçin, şablonu iade etmek için **Düzenlemeyi bitir**'i ve ardından yayımlamak için **Yayımla**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="f4ced-155">Select **Save**, select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="f4ced-156">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="f4ced-156">Additional resources</span></span>

[<span data-ttu-id="f4ced-157">Başlangıç paketine genel bakış</span><span class="sxs-lookup"><span data-stu-id="f4ced-157">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="f4ced-158">Konteyner modülü</span><span class="sxs-lookup"><span data-stu-id="f4ced-158">Container module</span></span>](add-container-module.md)

[<span data-ttu-id="f4ced-159">Satınalma kutusu modülü</span><span class="sxs-lookup"><span data-stu-id="f4ced-159">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="f4ced-160">Sepet modülü</span><span class="sxs-lookup"><span data-stu-id="f4ced-160">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="f4ced-161">Sepet simgesi modülü</span><span class="sxs-lookup"><span data-stu-id="f4ced-161">Cart icon module</span></span>](cart-icon-module.md)

[<span data-ttu-id="f4ced-162">Ödeme modülü</span><span class="sxs-lookup"><span data-stu-id="f4ced-162">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="f4ced-163">Sipariş onayı modülü</span><span class="sxs-lookup"><span data-stu-id="f4ced-163">Order confirmation module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="f4ced-164">Üst bilgi modülü</span><span class="sxs-lookup"><span data-stu-id="f4ced-164">Header module</span></span>](author-header-module.md)

[<span data-ttu-id="f4ced-165">Alt bilgi modülü</span><span class="sxs-lookup"><span data-stu-id="f4ced-165">Footer module</span></span>](author-footer-module.md)
