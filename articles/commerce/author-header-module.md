---
title: Üst bilgi modülü
description: Bu konu üst bilgi modüllerini kapsamakta ve Microsoft Dynamics 365 Commerce'te sayfa üst bilgilerinin nasıl oluşturacağını açıklamaktadır.
author: anupamar-ms
manager: annbe
ms.date: 09/15/2020
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
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: 99457b2c98eae0ddd898f852630d690140a5a4c5
ms.sourcegitcommit: 8028fbc5b9585e87d3331ea02577ff82ede090af
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/16/2020
ms.locfileid: "3817022"
---
# <a name="header-module"></a><span data-ttu-id="e064d-103">Üst bilgi modülü</span><span class="sxs-lookup"><span data-stu-id="e064d-103">Header module</span></span>

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

<span data-ttu-id="e064d-104">Bu konu üst bilgi modüllerini kapsamakta ve Microsoft Dynamics 365 Commerce'te sayfa üst bilgilerinin nasıl oluşturacağını açıklamaktadır.</span><span class="sxs-lookup"><span data-stu-id="e064d-104">This topic covers header modules and describes how to create page headers in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="e064d-105">Genel bakış</span><span class="sxs-lookup"><span data-stu-id="e064d-105">Overview</span></span>

<span data-ttu-id="e064d-106">Dynamics 365 Commerce'de sayfa üstbilgisi başlık, promosyon başlığı ve tanımlama bilgisi izin modüllerini içeren bir sayfa parçası olarak yapılandırılır.</span><span class="sxs-lookup"><span data-stu-id="e064d-106">In Dynamics 365 Commerce, a page header is configured as a page fragment that includes the header, promo banner, and cookie consent modules.</span></span> 

<span data-ttu-id="e064d-107">Üst bilgi modülünde bir site logosu, gezinti hiyerarşisinin bağlantıları, sitedeki diğer sayfalara bağlantılar, bir sepet sembolü modülü, bir istek listesi sembolü, oturum açma seçenekleri ve arama çubuğu bulunur.</span><span class="sxs-lookup"><span data-stu-id="e064d-107">The header module includes a site logo, links to the navigation hierarchy, links to other pages on the site, a cart icon module, a wishlist symbol, sign-in options, and the search bar.</span></span> <span data-ttu-id="e064d-108">Üst bilgi modülü, sitenin (yani bir masaüstü cihaz veya mobil cihaz) görüntülendiği cihaz için otomatik olarak en iyi duruma getirilir.</span><span class="sxs-lookup"><span data-stu-id="e064d-108">A header module is automatically optimized for the device that the site is being viewed on (in other words, for a desktop device or a mobile device).</span></span> <span data-ttu-id="e064d-109">Örneğin, bir mobil cihazda, gezinti çubuğu bir **menü** düğmesine (bazen *hamburger menüsü* olarak da adlandırılır) daraltılır.</span><span class="sxs-lookup"><span data-stu-id="e064d-109">For example, on a mobile device, the navigation bar is collapsed into a **Menu** button (which is sometimes referred to as a *hamburger menu*).</span></span>

<span data-ttu-id="e064d-110">Aşağıdaki resimde giriş sayfasında kullanılan bir üstbilgi modülü örneği gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="e064d-110">The following image shows an example of a header module on a home page.</span></span>

![üstbilgi modülü örneği](./media/ecommerce-header.png)

## <a name="properties-of-a-header-module"></a><span data-ttu-id="e064d-112">Üst bilgi modülünün özellikleri</span><span class="sxs-lookup"><span data-stu-id="e064d-112">Properties of a header module</span></span>

<span data-ttu-id="e064d-113">Üst bilgi modülü **Logo resmi**, **Logo bağlantısı** ve **Hesabım bağlantıları** özelliklerini destekler.</span><span class="sxs-lookup"><span data-stu-id="e064d-113">A header module supports **Logo image**, **Logo link**, and **My account links** properties.</span></span> 

<span data-ttu-id="e064d-114">**Logo resmi** ve **Logo bağlantısı** özellikleri sayfada bir logo tanımlamak için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="e064d-114">The **Logo image** and **Logo link** properties are used to define a logo on the page.</span></span> <span data-ttu-id="e064d-115">Daha fazla bilgi için bkz. [Logo ekleme](add-logo.md).</span><span class="sxs-lookup"><span data-stu-id="e064d-115">For more information, see [Add a logo](add-logo.md).</span></span> 

<span data-ttu-id="e064d-116">**Hesabım bağlantıları** özelliği, site sahibinin üst bilgide hızlı bağlantıları göstermek istediği hesap sayfalarını tanımlamak için kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="e064d-116">The **My account links** property can be used to define account pages that the site owner wants to show quick links for in the header.</span></span>

## <a name="modules-that-are-available-within-a-header-module"></a><span data-ttu-id="e064d-117">Üstbilgi modülünde kullanılabilen modüller</span><span class="sxs-lookup"><span data-stu-id="e064d-117">Modules that are available within a header module</span></span>

<span data-ttu-id="e064d-118">Aşağıdaki modüller bir üstbilgi modülünde kullanılabilir:</span><span class="sxs-lookup"><span data-stu-id="e064d-118">The following modules can be used in a header module:</span></span>

- <span data-ttu-id="e064d-119">**Gezinti menüsü** – Gezinti menüsü, kanal gezinti hiyerarşisini ve diğer statik gezinti bağlantılarını temsil eder.</span><span class="sxs-lookup"><span data-stu-id="e064d-119">**Navigation menu** – The navigation menu represents the channel navigation hierarchy and other static navigation links.</span></span> <span data-ttu-id="e064d-120">Daha fazla bilgi için bkz. [Gezinti menüsü modülleri](nav-menu-module.md).</span><span class="sxs-lookup"><span data-stu-id="e064d-120">For more information, see [Navigation menu module](nav-menu-module.md).</span></span>

- <span data-ttu-id="e064d-121">**Arama** – Arama modülü, kullanıcıların ürün aramak için arama terimleri girmesine izin verir.</span><span class="sxs-lookup"><span data-stu-id="e064d-121">**Search** – The search module lets users enter search terms to search for products.</span></span> <span data-ttu-id="e064d-122">**Site Ayarları \>Uzantılar**'da, varsayılan arama sayfasının URL'si ve arama sorgusu parametreleri girilmelidir.</span><span class="sxs-lookup"><span data-stu-id="e064d-122">The URL of the default search page and the search query parameters must be provided at **Site Settings \> Extensions**.</span></span> <span data-ttu-id="e064d-123">Arama modülünde, arama düğmesini veya etiketi gereksinim duyduğunuz şekilde gizlemenize olanak sağlayan özellikler vardır.</span><span class="sxs-lookup"><span data-stu-id="e064d-123">The search module has properties that let you suppress the search button or label as you require.</span></span> <span data-ttu-id="e064d-124">Arama modülü ürün, anahtar sözcük ve kategori arama sonuçları gibi otomatik öneri seçeneklerini de destekler.</span><span class="sxs-lookup"><span data-stu-id="e064d-124">The search module also supports auto-suggest options, such as product, keyword, and category search results.</span></span>

- <span data-ttu-id="e064d-125">**Sepet simgesi** - Sepet simgesi modülü, belirli bir zamanda sepetteki öğelerin sayısını gösteren sepet simgesini temsil eder.</span><span class="sxs-lookup"><span data-stu-id="e064d-125">**Cart icon** - The cart icon module represents the cart icon, which shows the number of items in the cart at any given time.</span></span> <span data-ttu-id="e064d-126">Daha fazla bilgi için bkz. [Sepet simgesi modülü](cart-icon-module.md).</span><span class="sxs-lookup"><span data-stu-id="e064d-126">For more information, see [Cart icon module](cart-icon-module.md).</span></span>

## <a name="create-a-header-fragment-for-a-page"></a><span data-ttu-id="e064d-127">Sayfa için üst bilgi parçası oluşturma</span><span class="sxs-lookup"><span data-stu-id="e064d-127">Create a header fragment for a page</span></span>

<span data-ttu-id="e064d-128">Bir üst bilgi parçası oluşturmak için şu adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="e064d-128">To create a header fragment, follow these steps.</span></span>

1. <span data-ttu-id="e064d-129">**Parçalar**'a gidin ve yeni parça oluşturmak için **Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="e064d-129">Go to **Fragments**, and select **New** to create a new fragment.</span></span>
1. <span data-ttu-id="e064d-130">**Yeni parça** iletişim kutusunda **Kapsayıcı** modülünü seçin, parça için bir ad girin ve sonra **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="e064d-130">In the **New fragment** dialog box, select the **Container** module, enter a name for the fragment, and then select **OK**.</span></span>
1. <span data-ttu-id="e064d-131">**Varsayılan kapsayıcı** yuvasını seçin ve sağ tarafta bulunan Özellikler bölmesinde, **genişlik** özelliğini **Ekranı doldur** olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="e064d-131">Select the **Default container** slot, and then, in the properties pane on the right, set the **Width** property to **Fill Screen**.</span></span>
1. <span data-ttu-id="e064d-132">**Varsayılan Konteyner** yuvası için üç nokta (**...**) düğmesini seçin ve **Modül Ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="e064d-132">In the **Default container** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="e064d-133">**Modül Ekle** iletişim kutusunda **Tanımlama bilgisi izni**, **Üst bilgi** ve **Promosyon başlığı** modüllerini seçin ve **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="e064d-133">In the **Add Module** dialog box, select the **Cookie consent**, **Header**, and **Promo banner** modules, and then select **OK**.</span></span>
1. <span data-ttu-id="e064d-134">**Promosyon başlığı** modülünün özellikler bölmesinde, **İleti ekle**'yi seçin ve sonra **İleti**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="e064d-134">In the properties pane of the **Promo banner** module, select **Add Message**, and then select **Message**.</span></span>
1. <span data-ttu-id="e064d-135">**İleti** iletişim kutusunda promosyon içeriği için metin ve bağlantı ekleyin ve **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="e064d-135">In the **Message** dialog box, add text and links for the promotional content, and then select **OK**.</span></span>
1. <span data-ttu-id="e064d-136">**Tanımlama bilgisi izni** modülünün özellikler bölmesinde, bir metin ve site gizlilik sayfasına bağlantı ekleyin ve yapılandırın.</span><span class="sxs-lookup"><span data-stu-id="e064d-136">In the properties pane of the **Cookie consent** module, add and configure text and a link to the site privacy page.</span></span>
1. <span data-ttu-id="e064d-137">Başlık modülünü içeren **Gezinti menüsü** yuvasında üç noktayı (**...**) seçin ve sonra **Modül Ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="e064d-137">In the **Navigation menu** slot of the header module, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="e064d-138">**Modül Ekle** iletişim kutusunda **Gezinti meüsü** modülünü seçin ve **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="e064d-138">In the **Add Module** dialog box, select the **Navigation menu** module, and then select **OK**.</span></span>
1. <span data-ttu-id="e064d-139">Gezinti menü modülünün özellik bölmesinde, **Gezinme menüsü kaynağı** altında, **Retail Server** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="e064d-139">In the property pane for the navigation menu module, under **Source for navigation menu**, select **Retail Server**.</span></span>
1. <span data-ttu-id="e064d-140">Gezinti menüsü modülünün özellik bölmesinde, **Statik menü öğeleri** altında, **Menü öğesi ekle**'yi seçin ve sonra **Menü öğesini** seçin.</span><span class="sxs-lookup"><span data-stu-id="e064d-140">In the property pane for the navigation menu module, under **Static menu items**, select **Add Menu item**, and then select **Menu item**.</span></span> 
1. <span data-ttu-id="e064d-141">**Menü öğesi** iletişim kutusunda **Menü Öğesi Metni** altında "İletişim"i girin.</span><span class="sxs-lookup"><span data-stu-id="e064d-141">In the **Menu item** dialog box, under **Menu Item Text** enter "Contact."</span></span>
1. <span data-ttu-id="e064d-142">**Menü öğesi** iletişim kutusunda **Menü Öğesi Bağlantı hedefi** altından **Bağlantı ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="e064d-142">In the **Menu item** dialog box, under **Menu Item Link target** select **Add a link**.</span></span>
1. <span data-ttu-id="e064d-143">**Bağlantı ekle** iletişim kutusunda sitenin "İletişim" sayfası için URL seçin ve **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="e064d-143">In the **Add a link** dialog box, select the URL for the site's "Contact" page, and then select **OK**.</span></span>  
1. <span data-ttu-id="e064d-144">**Menü öğesi** iletişim kutusunda **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="e064d-144">In the **Menu item** dialog box, select **OK**.</span></span>
1. <span data-ttu-id="e064d-145">Başlık modülünü içeren **Ara** yuvasında üç noktayı (**...**) seçin ve sonra **Modül Ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="e064d-145">In the **Search** slot of the header module, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="e064d-146">**Modül Ekle** iletişim kutusunda **Ara** modülünü seçin ve **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="e064d-146">In the **Add Module** dialog box, select the **Search** module, and then select **OK**.</span></span>
1. <span data-ttu-id="e064d-147">Arama modülünün özellik bölmesinde, özelliklerini yapılandırın.</span><span class="sxs-lookup"><span data-stu-id="e064d-147">In the property pane for the search module, configure the properties as needed.</span></span>
1. <span data-ttu-id="e064d-148">Başlık modülünü içeren **Sepet simgesi** yuvasında üç noktayı (**...**) seçin ve sonra **Modül Ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="e064d-148">In the **Cart icon** slot of the header module, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="e064d-149">**Modül Ekle** iletişim kutusunda **Sepet simgesi** modülünü seçin ve **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="e064d-149">In the **Add Module** dialog box, select the **Cart icon** module, and then select **OK**.</span></span>
1. <span data-ttu-id="e064d-150">Sepet simgesi modülünün özellik bölmesinde, özelliklerini yapılandırın.</span><span class="sxs-lookup"><span data-stu-id="e064d-150">In the property pane for the cart icon module, configure the properties as needed.</span></span> <span data-ttu-id="e064d-151">Kullanıcılar üzerinde gezinirken, sepet simgesinin bir sepet Özeti (mini sepet olarak da bilinir) göstermesini istiyorsanız, **mini sepeti göster**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="e064d-151">If you want the cart icon to display a cart summary (also known as a mini cart) when users hover over it, select **Show mini cart**.</span></span>
1. <span data-ttu-id="e064d-152">**Kaydet**'i seçin, parçayı iade etmek için **Düzenlemeyi bitir**'i ve ardından yayımlamak için **Yayımla**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="e064d-152">Select **Save**, select **Finish editing** to check in the fragment, and then select **Publish** to publish it.</span></span>

<span data-ttu-id="e064d-153">Üstbilginin her sayfada göründüğünden emin olmak için, site için oluşturulan her sayfa şablonunda aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="e064d-153">To help ensure that a header appears on every page, follow these steps on every page template that is created for the site.</span></span>

1. <span data-ttu-id="e064d-154">**Varsayılan sayfanın** **üstbilgi** yuvasında, altbilgi modülünde, oluşturduğunuz altbilgi parçasını ekleyin.</span><span class="sxs-lookup"><span data-stu-id="e064d-154">In the **Header** slot of the **Default page** module, add the footer fragment that you created.</span></span>
1. <span data-ttu-id="e064d-155">**Kaydet**'i seçin, şablonu iade etmek için **Düzenlemeyi bitir**'i ve ardından yayımlamak için **Yayımla**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="e064d-155">Select **Save**, select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="e064d-156">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="e064d-156">Additional resources</span></span>

[<span data-ttu-id="e064d-157">Modül kitaplığına genel bakış</span><span class="sxs-lookup"><span data-stu-id="e064d-157">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="e064d-158">Kapsayıcı modülü</span><span class="sxs-lookup"><span data-stu-id="e064d-158">Container module</span></span>](add-container-module.md)

[<span data-ttu-id="e064d-159">Sepet simgesi modülü</span><span class="sxs-lookup"><span data-stu-id="e064d-159">Cart icon module</span></span>](cart-icon-module.md)

[<span data-ttu-id="e064d-160">Promosyon başlığı modülü</span><span class="sxs-lookup"><span data-stu-id="e064d-160">Promo banner module</span></span>](add-alert.md)

[<span data-ttu-id="e064d-161">Gezinti Menüsü modülleri</span><span class="sxs-lookup"><span data-stu-id="e064d-161">Navigation Menu module</span></span>](nav-menu-module.md) 

[<span data-ttu-id="e064d-162">Tanımlama bilgisi izni</span><span class="sxs-lookup"><span data-stu-id="e064d-162">Cookie consent</span></span>](cookie-consent-module.md)

[<span data-ttu-id="e064d-163">Alt bilgi modülü</span><span class="sxs-lookup"><span data-stu-id="e064d-163">Footer module</span></span>](author-footer-module.md)
