---
title: Üst bilgi modülü
description: Bu konu üst bilgi modüllerini kapsamakta ve Microsoft Dynamics 365 Commerce'te sayfa üst bilgilerinin nasıl oluşturacağını açıklamaktadır.
author: anupamar-ms
manager: annbe
ms.date: 10/20/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: 569fb5ac3d30be30044ef9b928ecf1f6dde20aab
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5211436"
---
# <a name="header-module"></a><span data-ttu-id="5fe72-103">Üst bilgi modülü</span><span class="sxs-lookup"><span data-stu-id="5fe72-103">Header module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="5fe72-104">Bu konu üst bilgi modüllerini kapsamakta ve Microsoft Dynamics 365 Commerce'te sayfa üst bilgilerinin nasıl oluşturacağını açıklamaktadır.</span><span class="sxs-lookup"><span data-stu-id="5fe72-104">This topic covers header modules and describes how to create page headers in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="5fe72-105">Dynamics 365 Commerce'de sayfa üstbilgisi başlık, promosyon başlığı ve tanımlama bilgisi izin modüllerini içeren bir sayfa parçası olarak yapılandırılır.</span><span class="sxs-lookup"><span data-stu-id="5fe72-105">In Dynamics 365 Commerce, a page header is configured as a page fragment that includes the header, promo banner, and cookie consent modules.</span></span> 

<span data-ttu-id="5fe72-106">Üst bilgi modülünde bir site logosu, gezinti hiyerarşisinin bağlantıları, sitedeki diğer sayfalara bağlantılar, bir sepet sembolü modülü, bir istek listesi sembolü, oturum açma seçenekleri ve arama çubuğu bulunur.</span><span class="sxs-lookup"><span data-stu-id="5fe72-106">The header module includes a site logo, links to the navigation hierarchy, links to other pages on the site, a cart icon module, a wishlist symbol, sign-in options, and the search bar.</span></span> <span data-ttu-id="5fe72-107">Üst bilgi modülü, sitenin (yani bir masaüstü cihaz veya mobil cihaz) görüntülendiği cihaz için otomatik olarak en iyi duruma getirilir.</span><span class="sxs-lookup"><span data-stu-id="5fe72-107">A header module is automatically optimized for the device that the site is being viewed on (in other words, for a desktop device or a mobile device).</span></span> <span data-ttu-id="5fe72-108">Örneğin, bir mobil cihazda, gezinti çubuğu bir **menü** düğmesine (bazen *hamburger menüsü* olarak da adlandırılır) daraltılır.</span><span class="sxs-lookup"><span data-stu-id="5fe72-108">For example, on a mobile device, the navigation bar is collapsed into a **Menu** button (which is sometimes referred to as a *hamburger menu*).</span></span>

<span data-ttu-id="5fe72-109">Aşağıdaki resimde giriş sayfasında kullanılan bir üstbilgi modülü örneği gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="5fe72-109">The following image shows an example of a header module on a home page.</span></span>

![üstbilgi modülü örneği](./media/ecommerce-header.png)

## <a name="properties-of-a-header-module"></a><span data-ttu-id="5fe72-111">Üst bilgi modülünün özellikleri</span><span class="sxs-lookup"><span data-stu-id="5fe72-111">Properties of a header module</span></span>

<span data-ttu-id="5fe72-112">Üst bilgi modülü **Logo resmi**, **Logo bağlantısı** ve **Hesabım bağlantıları** özelliklerini destekler.</span><span class="sxs-lookup"><span data-stu-id="5fe72-112">A header module supports **Logo image**, **Logo link**, and **My account links** properties.</span></span> 

<span data-ttu-id="5fe72-113">**Logo resmi** ve **Logo bağlantısı** özellikleri sayfada bir logo tanımlamak için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="5fe72-113">The **Logo image** and **Logo link** properties are used to define a logo on the page.</span></span> <span data-ttu-id="5fe72-114">Daha fazla bilgi için bkz. [Logo ekleme](add-logo.md).</span><span class="sxs-lookup"><span data-stu-id="5fe72-114">For more information, see [Add a logo](add-logo.md).</span></span> 

<span data-ttu-id="5fe72-115">**Hesabım bağlantıları** özelliği, site sahibinin üst bilgide hızlı bağlantıları göstermek istediği hesap sayfalarını tanımlamak için kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="5fe72-115">The **My account links** property can be used to define account pages that the site owner wants to show quick links for in the header.</span></span>

## <a name="modules-that-are-available-within-a-header-module"></a><span data-ttu-id="5fe72-116">Üstbilgi modülünde kullanılabilen modüller</span><span class="sxs-lookup"><span data-stu-id="5fe72-116">Modules that are available within a header module</span></span>

<span data-ttu-id="5fe72-117">Aşağıdaki modüller bir üstbilgi modülünde kullanılabilir:</span><span class="sxs-lookup"><span data-stu-id="5fe72-117">The following modules can be used in a header module:</span></span>

- <span data-ttu-id="5fe72-118">**Gezinti menüsü** – Gezinti menüsü, kanal gezinti hiyerarşisini ve diğer statik gezinti bağlantılarını temsil eder.</span><span class="sxs-lookup"><span data-stu-id="5fe72-118">**Navigation menu** – The navigation menu represents the channel navigation hierarchy and other static navigation links.</span></span> <span data-ttu-id="5fe72-119">Daha fazla bilgi için bkz. [Gezinti menüsü modülleri](nav-menu-module.md).</span><span class="sxs-lookup"><span data-stu-id="5fe72-119">For more information, see [Navigation menu module](nav-menu-module.md).</span></span>

- <span data-ttu-id="5fe72-120">**Arama** – Arama modülü, kullanıcıların ürün aramak için arama terimleri girmesine izin verir.</span><span class="sxs-lookup"><span data-stu-id="5fe72-120">**Search** – The search module lets users enter search terms to search for products.</span></span> <span data-ttu-id="5fe72-121">**Site Ayarları \>Uzantılar**'da, varsayılan arama sayfasının URL'si ve arama sorgusu parametreleri girilmelidir.</span><span class="sxs-lookup"><span data-stu-id="5fe72-121">The URL of the default search page and the search query parameters must be provided at **Site Settings \> Extensions**.</span></span> <span data-ttu-id="5fe72-122">Arama modülünde, arama düğmesini veya etiketi gereksinim duyduğunuz şekilde gizlemenize olanak sağlayan özellikler vardır.</span><span class="sxs-lookup"><span data-stu-id="5fe72-122">The search module has properties that let you suppress the search button or label as you require.</span></span> <span data-ttu-id="5fe72-123">Arama modülü ürün, anahtar sözcük ve kategori arama sonuçları gibi otomatik öneri seçeneklerini de destekler.</span><span class="sxs-lookup"><span data-stu-id="5fe72-123">The search module also supports auto-suggest options, such as product, keyword, and category search results.</span></span>

- <span data-ttu-id="5fe72-124">**Sepet simgesi** - Sepet simgesi modülü, belirli bir zamanda sepetteki öğelerin sayısını gösteren sepet simgesini temsil eder.</span><span class="sxs-lookup"><span data-stu-id="5fe72-124">**Cart icon** - The cart icon module represents the cart icon, which shows the number of items in the cart at any given time.</span></span> <span data-ttu-id="5fe72-125">Daha fazla bilgi için bkz. [Sepet simgesi modülü](cart-icon-module.md).</span><span class="sxs-lookup"><span data-stu-id="5fe72-125">For more information, see [Cart icon module](cart-icon-module.md).</span></span>

- <span data-ttu-id="5fe72-126">**Site seçici** - Site seçici modülü kullanıcıların pazar, bölgeler ve yerel ayarlara göre, önceden tanımlanmış farklı sitelere göz atmasına olanak tanır.</span><span class="sxs-lookup"><span data-stu-id="5fe72-126">**Site selector** - The site selector module lets users browse across different predefined sites, based on market, regions, and locales.</span></span> <span data-ttu-id="5fe72-127">Daha fazla bilgi için bkz. [Site seçici modülü](site-selector.md).</span><span class="sxs-lookup"><span data-stu-id="5fe72-127">For more information, see [Site selector module](site-selector.md).</span></span>

- <span data-ttu-id="5fe72-128">**Mağaza Seçici** - Mağaza seçici modülü, bir üstbilgi modülünün mağaza seçici yuvasına dahil edilebilir.</span><span class="sxs-lookup"><span data-stu-id="5fe72-128">**Store selector** - The store selector module can be included in a header module's store selector slot.</span></span> <span data-ttu-id="5fe72-129">Kullanıcıların yakındaki mağazalara göz atmasına ve onları bulmasına olanak tanır.</span><span class="sxs-lookup"><span data-stu-id="5fe72-129">It lets users browse and find nearby stores.</span></span> <span data-ttu-id="5fe72-130">Kullanıcılar tercih edilen bir mağaza da belirtebilirler.</span><span class="sxs-lookup"><span data-stu-id="5fe72-130">Users can also specify a preferred store.</span></span> <span data-ttu-id="5fe72-131">Bu mağaza üst bilgide görüntülenecektir.</span><span class="sxs-lookup"><span data-stu-id="5fe72-131">That store will then be shown in the header.</span></span> <span data-ttu-id="5fe72-132">Mağaza seçici modülü üst bilgi modülüne dahil edildiğinde, **Mod** özelliği **Mağaza bul** olarak ayarlanmalıdır.</span><span class="sxs-lookup"><span data-stu-id="5fe72-132">When the store selector module is included in the header module, its **Mode** property must be set to **Find stores**.</span></span> <span data-ttu-id="5fe72-133">Daha fazla bilgi için bkz. [Mağaza seçici modülü](store-selector.md).</span><span class="sxs-lookup"><span data-stu-id="5fe72-133">For more information, see [Store selector module](store-selector.md).</span></span>

> [!NOTE]
> - <span data-ttu-id="5fe72-134">Üst bilgi modüllerinde sepet simgesi modülünü kullanma desteği Dynamics 365 Commerce 10.0.11 sürümünde bulunabilir.</span><span class="sxs-lookup"><span data-stu-id="5fe72-134">Support for using the cart icon module in header modules is available in the Dynamics 365 Commerce 10.0.11 release.</span></span>
> - <span data-ttu-id="5fe72-135">Üst bilgi modüllerinde site seçici modülünü kullanma desteği Dynamics 365 Commerce 10.0.14 sürümünde bulunabilir.</span><span class="sxs-lookup"><span data-stu-id="5fe72-135">Support for using the site selector module in header modules is available in the Dynamics 365 Commerce 10.0.14 release.</span></span>
> - <span data-ttu-id="5fe72-136">Üst bilgi modüllerinde mağaza seçici modülünü kullanma desteği Dynamics 365 Commerce 10.0.15 sürümünde bulunabilir.</span><span class="sxs-lookup"><span data-stu-id="5fe72-136">Support for using the store selector module in header modules is available in the Dynamics 365 Commerce 10.0.15 release.</span></span>

## <a name="create-a-header-fragment-for-a-page"></a><span data-ttu-id="5fe72-137">Sayfa için üst bilgi parçası oluşturma</span><span class="sxs-lookup"><span data-stu-id="5fe72-137">Create a header fragment for a page</span></span>

<span data-ttu-id="5fe72-138">Bir üst bilgi parçası oluşturmak için şu adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="5fe72-138">To create a header fragment, follow these steps.</span></span>

1. <span data-ttu-id="5fe72-139">**Parçalar**'a gidin ve yeni parça oluşturmak için **Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="5fe72-139">Go to **Fragments**, and select **New** to create a new fragment.</span></span>
1. <span data-ttu-id="5fe72-140">**Yeni parça** iletişim kutusunda **Kapsayıcı** modülünü seçin, parça için bir ad girin ve sonra **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="5fe72-140">In the **New fragment** dialog box, select the **Container** module, enter a name for the fragment, and then select **OK**.</span></span>
1. <span data-ttu-id="5fe72-141">**Varsayılan kapsayıcı** yuvasını seçin ve sağ tarafta bulunan Özellikler bölmesinde, **genişlik** özelliğini **Ekranı doldur** olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="5fe72-141">Select the **Default container** slot, and then, in the properties pane on the right, set the **Width** property to **Fill Screen**.</span></span>
1. <span data-ttu-id="5fe72-142">**Varsayılan Konteyner** yuvası için üç nokta (**...**) düğmesini seçin ve **Modül Ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="5fe72-142">In the **Default container** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="5fe72-143">**Modül Ekle** iletişim kutusunda **Tanımlama bilgisi izni**, **Üst bilgi** ve **Promosyon başlığı** modüllerini seçin ve **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="5fe72-143">In the **Add Module** dialog box, select the **Cookie consent**, **Header**, and **Promo banner** modules, and then select **OK**.</span></span>
1. <span data-ttu-id="5fe72-144">**Promosyon başlığı** modülünün özellikler bölmesinde, **İleti ekle**'yi seçin ve sonra **İleti**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="5fe72-144">In the properties pane of the **Promo banner** module, select **Add Message**, and then select **Message**.</span></span>
1. <span data-ttu-id="5fe72-145">**İleti** iletişim kutusunda promosyon içeriği için metin ve bağlantı ekleyin ve **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="5fe72-145">In the **Message** dialog box, add text and links for the promotional content, and then select **OK**.</span></span>
1. <span data-ttu-id="5fe72-146">**Tanımlama bilgisi izni** modülünün özellikler bölmesinde, bir metin ve site gizlilik sayfasına bağlantı ekleyin ve yapılandırın.</span><span class="sxs-lookup"><span data-stu-id="5fe72-146">In the properties pane of the **Cookie consent** module, add and configure text and a link to the site privacy page.</span></span>
1. <span data-ttu-id="5fe72-147">Başlık modülünü içeren **Gezinti menüsü** yuvasında üç noktayı (**...**) seçin ve sonra **Modül Ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="5fe72-147">In the **Navigation menu** slot of the header module, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="5fe72-148">**Modül Ekle** iletişim kutusunda **Gezinti meüsü** modülünü seçin ve **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="5fe72-148">In the **Add Module** dialog box, select the **Navigation menu** module, and then select **OK**.</span></span>
1. <span data-ttu-id="5fe72-149">Gezinti menü modülünün özellik bölmesinde, **Gezinme menüsü kaynağı** altında, **Retail Server** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="5fe72-149">In the property pane for the navigation menu module, under **Source for navigation menu**, select **Retail Server**.</span></span>
1. <span data-ttu-id="5fe72-150">Gezinti menüsü modülünün özellik bölmesinde, **Statik menü öğeleri** altında, **Menü öğesi ekle**'yi seçin ve sonra **Menü öğesini** seçin.</span><span class="sxs-lookup"><span data-stu-id="5fe72-150">In the property pane for the navigation menu module, under **Static menu items**, select **Add Menu item**, and then select **Menu item**.</span></span> 
1. <span data-ttu-id="5fe72-151">**Menü öğesi** iletişim kutusunda **Menü Öğesi Metni** altında "İletişim"i girin.</span><span class="sxs-lookup"><span data-stu-id="5fe72-151">In the **Menu item** dialog box, under **Menu Item Text** enter "Contact."</span></span>
1. <span data-ttu-id="5fe72-152">**Menü öğesi** iletişim kutusunda **Menü Öğesi Bağlantı hedefi** altından **Bağlantı ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="5fe72-152">In the **Menu item** dialog box, under **Menu Item Link target** select **Add a link**.</span></span>
1. <span data-ttu-id="5fe72-153">**Bağlantı ekle** iletişim kutusunda sitenin "İletişim" sayfası için URL seçin ve **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="5fe72-153">In the **Add a link** dialog box, select the URL for the site's "Contact" page, and then select **OK**.</span></span>  
1. <span data-ttu-id="5fe72-154">**Menü öğesi** iletişim kutusunda **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="5fe72-154">In the **Menu item** dialog box, select **OK**.</span></span>
1. <span data-ttu-id="5fe72-155">Başlık modülünü içeren **Ara** yuvasında üç noktayı (**...**) seçin ve sonra **Modül Ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="5fe72-155">In the **Search** slot of the header module, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="5fe72-156">**Modül Ekle** iletişim kutusunda **Ara** modülünü seçin ve **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="5fe72-156">In the **Add Module** dialog box, select the **Search** module, and then select **OK**.</span></span>
1. <span data-ttu-id="5fe72-157">Arama modülünün özellik bölmesinde, özelliklerini yapılandırın.</span><span class="sxs-lookup"><span data-stu-id="5fe72-157">In the property pane for the search module, configure the properties as needed.</span></span>
1. <span data-ttu-id="5fe72-158">Başlık modülünü içeren **Sepet simgesi** yuvasında üç noktayı (**...**) seçin ve sonra **Modül Ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="5fe72-158">In the **Cart icon** slot of the header module, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="5fe72-159">**Modül Ekle** iletişim kutusunda **Sepet simgesi** modülünü seçin ve **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="5fe72-159">In the **Add Module** dialog box, select the **Cart icon** module, and then select **OK**.</span></span>
1. <span data-ttu-id="5fe72-160">Sepet simgesi modülünün özellik bölmesinde, özelliklerini yapılandırın.</span><span class="sxs-lookup"><span data-stu-id="5fe72-160">In the property pane for the cart icon module, configure the properties as needed.</span></span> <span data-ttu-id="5fe72-161">Kullanıcılar üzerinde gezinirken, sepet simgesinin bir sepet Özeti (mini sepet olarak da bilinir) göstermesini istiyorsanız, **mini sepeti göster**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="5fe72-161">If you want the cart icon to display a cart summary (also known as a mini cart) when users hover over it, select **Show mini cart**.</span></span>
1. <span data-ttu-id="5fe72-162">**Kaydet**'i seçin, parçayı iade etmek için **Düzenlemeyi bitir**'i ve ardından yayımlamak için **Yayımla**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="5fe72-162">Select **Save**, select **Finish editing** to check in the fragment, and then select **Publish** to publish it.</span></span>

<span data-ttu-id="5fe72-163">Üstbilginin her sayfada göründüğünden emin olmak için, site için oluşturulan her sayfa şablonunda aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="5fe72-163">To help ensure that a header appears on every page, follow these steps on every page template that is created for the site.</span></span>

1. <span data-ttu-id="5fe72-164">**Varsayılan sayfanın** **üstbilgi** yuvasında, altbilgi modülünde, oluşturduğunuz altbilgi parçasını ekleyin.</span><span class="sxs-lookup"><span data-stu-id="5fe72-164">In the **Header** slot of the **Default page** module, add the footer fragment that you created.</span></span>
1. <span data-ttu-id="5fe72-165">**Kaydet**'i seçin, şablonu iade etmek için **Düzenlemeyi bitir**'i ve ardından yayımlamak için **Yayımla**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="5fe72-165">Select **Save**, select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="5fe72-166">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="5fe72-166">Additional resources</span></span>

[<span data-ttu-id="5fe72-167">Modül kitaplığına genel bakış</span><span class="sxs-lookup"><span data-stu-id="5fe72-167">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="5fe72-168">Kapsayıcı modülü</span><span class="sxs-lookup"><span data-stu-id="5fe72-168">Container module</span></span>](add-container-module.md)

[<span data-ttu-id="5fe72-169">Sepet simgesi modülü</span><span class="sxs-lookup"><span data-stu-id="5fe72-169">Cart icon module</span></span>](cart-icon-module.md)

[<span data-ttu-id="5fe72-170">Promosyon başlığı modülü</span><span class="sxs-lookup"><span data-stu-id="5fe72-170">Promo banner module</span></span>](add-alert.md)

[<span data-ttu-id="5fe72-171">Gezinti Menüsü modülleri</span><span class="sxs-lookup"><span data-stu-id="5fe72-171">Navigation Menu module</span></span>](nav-menu-module.md) 

[<span data-ttu-id="5fe72-172">Tanımlama bilgisi izni</span><span class="sxs-lookup"><span data-stu-id="5fe72-172">Cookie consent</span></span>](cookie-consent-module.md)

[<span data-ttu-id="5fe72-173">Alt bilgi modülü</span><span class="sxs-lookup"><span data-stu-id="5fe72-173">Footer module</span></span>](author-footer-module.md)

[<span data-ttu-id="5fe72-174">Site seçici modülü</span><span class="sxs-lookup"><span data-stu-id="5fe72-174">Site selector module</span></span>](site-selector.md)

[<span data-ttu-id="5fe72-175">Mağaza seçicisi modülü</span><span class="sxs-lookup"><span data-stu-id="5fe72-175">Store selector module</span></span>](store-selector.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]