---
title: Arama sonuçları modülü
description: Bu konu arama sonuçları modüllerini kapsamaktadır ve Microsoft Dynamics 365 Commerce'ün site sayfalarına nasıl ekleneceğini açıklamaktadır.
author: anupamar-ms
manager: annbe
ms.date: 01/28/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 5d852fe1a81b1e42484bc49ae136ef8613a2d3a5
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5254781"
---
# <a name="search-results-module"></a><span data-ttu-id="b92dc-103">Arama sonuçları modülü</span><span class="sxs-lookup"><span data-stu-id="b92dc-103">Search results module</span></span>

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

<span data-ttu-id="b92dc-104">Bu konu arama sonuçları modüllerini kapsamaktadır ve Microsoft Dynamics 365 Commerce'ün site sayfalarına nasıl ekleneceğini açıklamaktadır.</span><span class="sxs-lookup"><span data-stu-id="b92dc-104">This topic covers search results modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="b92dc-105">rama sonuçları modülü, ürün arama sonuçlarını ve ürünler için geçerli iyileştiricilerin bir listesini döndürür.</span><span class="sxs-lookup"><span data-stu-id="b92dc-105">The search results module returns product search results and a list of applicable refiners for the products.</span></span> <span data-ttu-id="b92dc-106">Dynamics 365 Commerce sitelerindeki arama sonuçları modülleri, aşağıdaki senaryoların sayfalarını işlemek için kullanılabilir:</span><span class="sxs-lookup"><span data-stu-id="b92dc-106">Search results modules on Dynamics 365 Commerce sites can be used to render pages for the following scenarios:</span></span>

- <span data-ttu-id="b92dc-107">Kullanıcı araması tarafından başlatılan arama sonuçları</span><span class="sxs-lookup"><span data-stu-id="b92dc-107">Search results that are initiated by a user search</span></span>
- <span data-ttu-id="b92dc-108">"Benzer ürün görünümleri" gibi belirli bir ürün kümesini gösteren arama sonuçları</span><span class="sxs-lookup"><span data-stu-id="b92dc-108">Search results that show a specific set of products, such as "Shop similar looks"</span></span>
- <span data-ttu-id="b92dc-109">Belirli bir kategoriye ait olan ürün listeleri.</span><span class="sxs-lookup"><span data-stu-id="b92dc-109">Lists of products that belong to a category</span></span>

<span data-ttu-id="b92dc-110">Kategori ve arama sonuçları sayfaları hakkında daha fazla bilgi için bkz. [Varsayılan kategori açılış sayfası ve arama sonuçları sayfasına genel bakış](category-search-page-overview.md).</span><span class="sxs-lookup"><span data-stu-id="b92dc-110">For more information about category and search results pages, see [Default category landing page and search results page overview](category-search-page-overview.md).</span></span>

<span data-ttu-id="b92dc-111">Aşağıdaki resimde Fabrikam sitesindeki bir kategori için arama sonuçları sayfası örneği gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="b92dc-111">The following illustration shows an example of a search results page for a category on the Fabrikam site.</span></span>

![Fabrikam sitesindeki arama sonuçları sayfası örneği](./media/SimpleCategoryLandingDressCategory.png)

## <a name="search-results-module-properties"></a><span data-ttu-id="b92dc-113">Arama sonuçları modülü özellikleri</span><span class="sxs-lookup"><span data-stu-id="b92dc-113">Search results module properties</span></span>

<span data-ttu-id="b92dc-114">Aşağıdaki tabloda, arama sonucu modüllerinin özellikleri, değerleri ve açıklamaları ile birlikte listelenmiştir.</span><span class="sxs-lookup"><span data-stu-id="b92dc-114">The following table lists the properties of search result modules, together with their values and descriptions.</span></span>

| <span data-ttu-id="b92dc-115">Özellik</span><span class="sxs-lookup"><span data-stu-id="b92dc-115">Property</span></span> | <span data-ttu-id="b92dc-116">Değerler</span><span class="sxs-lookup"><span data-stu-id="b92dc-116">Values</span></span> | <span data-ttu-id="b92dc-117">Tanım</span><span class="sxs-lookup"><span data-stu-id="b92dc-117">Description</span></span> |
|----------|--------|-------------|
| <span data-ttu-id="b92dc-118">Sayfa başına öğe sayısı</span><span class="sxs-lookup"><span data-stu-id="b92dc-118">Items per page</span></span> | <span data-ttu-id="b92dc-119">Tamsayı</span><span class="sxs-lookup"><span data-stu-id="b92dc-119">Integer</span></span> | <span data-ttu-id="b92dc-120">Her sayfada gösterilen maddelerin sayısı.</span><span class="sxs-lookup"><span data-stu-id="b92dc-120">The number of items that should be shown on each page.</span></span> |
| <span data-ttu-id="b92dc-121">PDP üzerinde yeniden izin ver</span><span class="sxs-lookup"><span data-stu-id="b92dc-121">Allow back on PDP</span></span> | <span data-ttu-id="b92dc-122">**Doğru** veya **yanlış**</span><span class="sxs-lookup"><span data-stu-id="b92dc-122">**True** or **False**</span></span> | <span data-ttu-id="b92dc-123">Bu özellik **Doğru** olarak ayarlanırsa, kullanıcı arama sonuçları sayfasında bir ürün seçtiğinde, açılan ürün ayrıntıları sayfasındaki (PDP) içerik haritası gezintisi "Sonuçlara geri dön" bağlantısını gösterir.</span><span class="sxs-lookup"><span data-stu-id="b92dc-123">If this property is set to **True**, when a user selects a product on the search results page, the breadcrumb navigation on the product details page (PDP) that is opened will show a "Back to results" link.</span></span> |
| <span data-ttu-id="b92dc-124">İyileştiricileri genişlet</span><span class="sxs-lookup"><span data-stu-id="b92dc-124">Expand Refiners</span></span> | <span data-ttu-id="b92dc-125">**Tümü**, **1**, **2**, **3** veya **4**</span><span class="sxs-lookup"><span data-stu-id="b92dc-125">**All**, **1**, **2**, **3**, or **4**</span></span> | <span data-ttu-id="b92dc-126">Bir sayfa yüklendiğinde genişletilmesi gereken en iyi iyileştiricilerin sayısı.</span><span class="sxs-lookup"><span data-stu-id="b92dc-126">The number of top refiners that should be expanded when a page is loaded.</span></span> <span data-ttu-id="b92dc-127">Örneğin, bu özellik **3** olarak ayarlanırsa, sayfadaki ilk üç iyileştirici genişletilir.</span><span class="sxs-lookup"><span data-stu-id="b92dc-127">For example, if this property is set to **3**, the first three refiners on the page will be expanded.</span></span> |
| <span data-ttu-id="b92dc-128">Kategori hiyerarşisi görüntüsünü gizle</span><span class="sxs-lookup"><span data-stu-id="b92dc-128">Hide category hierarchy display</span></span> | <span data-ttu-id="b92dc-129">**Doğru** veya **yanlış**</span><span class="sxs-lookup"><span data-stu-id="b92dc-129">**True** or **False**</span></span> | <span data-ttu-id="b92dc-130">Bu özellik **Doğru** olarak ayarlanırsa, sayfadaki kategori hiyerarşisi ekranı gizlenir.</span><span class="sxs-lookup"><span data-stu-id="b92dc-130">If this property is set to **True**, the category hierarchy display on the page will be hidden.</span></span> <span data-ttu-id="b92dc-131">Kategori hiyerarşisini göstermek için [içerik haritası modülünü](add-breadcrumb.md) kullanıyorsanız bu özellik **Doğru** olarak ayarlanmalıdır.</span><span class="sxs-lookup"><span data-stu-id="b92dc-131">This property should be set to **True** if you're using the [breadcrumb module](add-breadcrumb.md) to show the category hierarchy.</span></span>|
| <span data-ttu-id="b92dc-132">Ürün özniteliklerini arama sonuçlarına dahil et</span><span class="sxs-lookup"><span data-stu-id="b92dc-132">Include product attributes in search results</span></span> | <span data-ttu-id="b92dc-133">**Doğru** veya **yanlış**</span><span class="sxs-lookup"><span data-stu-id="b92dc-133">**True** or **False**</span></span> | <span data-ttu-id="b92dc-134">Bu özellik **Doğru** olarak ayarlanırsa, arama sonuçlarındaki ürünler için öznitelikler döndürülür.</span><span class="sxs-lookup"><span data-stu-id="b92dc-134">If this property is set to **True**, attributes will be returned for the products in the search results.</span></span> <span data-ttu-id="b92dc-135">Bu öznitelikler bir Ticaret sitesinde gösterilebilse de, bir uzantı gereklidir.</span><span class="sxs-lookup"><span data-stu-id="b92dc-135">Although these attributes can be shown on a Commerce site, an extension is required.</span></span>|
| <span data-ttu-id="b92dc-136">İlişki fiyatlarını göster</span><span class="sxs-lookup"><span data-stu-id="b92dc-136">Show affiliation prices</span></span> | <span data-ttu-id="b92dc-137">**Doğru** veya **yanlış**</span><span class="sxs-lookup"><span data-stu-id="b92dc-137">**True** or **False**</span></span> | <span data-ttu-id="b92dc-138">Bu özellik **Doğru** olarak ayarlanırsa, oturum açmış bir kullanıcı sayfaya göz attığında, ürünlerin bağlı kuruluş fiyatları arama sonuçlarında gösterilir.</span><span class="sxs-lookup"><span data-stu-id="b92dc-138">If this property is set to **True**, affiliation prices for products will be shown in the search results when a signed-in user browses the page.</span></span> |

> [!IMPORTANT]
> <span data-ttu-id="b92dc-139">Dynamics 365 Commerce 10.0.16 sürümünde ve sonrasında, **Bağlı kuruluş fiyatlarını göster** yapılandırması, sayfada bağlı kuruluş fiyatlarını göstermek için kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="b92dc-139">In the Dynamics 365 Commerce 10.0.16 release and later, the **Show affiliation prices** configuration can be used to show affiliation prices on the page.</span></span>

## <a name="supported-modules"></a><span data-ttu-id="b92dc-140">Desteklenen modüller</span><span class="sxs-lookup"><span data-stu-id="b92dc-140">Supported modules</span></span>

<span data-ttu-id="b92dc-141">Arama sonuçları modülü, kullanıcıların ürün bilgilerini görüntülemesine ve bir arama sonuçları sayfasından alışveriş sepetine ürün eklemesine olanak veren [hızlı görüntüleme modülünü](quick-view-module.md) destekler.</span><span class="sxs-lookup"><span data-stu-id="b92dc-141">The search results module supports the [quick view module](quick-view-module.md), which lets users view product information and add items to the cart from the search results page.</span></span>

## <a name="add-a-search-results-module-to-a-category-page"></a><span data-ttu-id="b92dc-142">Kategori sayfasına arama sonuçları modülü ekleme</span><span class="sxs-lookup"><span data-stu-id="b92dc-142">Add a search results module to a category page</span></span>

<span data-ttu-id="b92dc-143">Kategori sayfasına arama sonuçları modülü eklemek için bu adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="b92dc-143">To add a search results module to a category page, follow these steps.</span></span>

1. <span data-ttu-id="b92dc-144">Bir yeni şablonu oluşturmak için **Şablonlar**'a gidin ve **Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="b92dc-144">Go to **Templates**, and select **New** to create a new template.</span></span>
1. <span data-ttu-id="b92dc-145">**Yeni şablon** iletişim kutusuna **Arama sonuçları** adını girin ve **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="b92dc-145">In the **New template** dialog box, enter the name **Search results**, and then select **OK**.</span></span>
1. <span data-ttu-id="b92dc-146">**Gövde** bölmesi için üç nokta (...) düğmesini seçin ve **Modül Ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="b92dc-146">In the **Body** slot, select the ellipsis (...), and then select **Add Module**.</span></span>
1. <span data-ttu-id="b92dc-147">**Modül Ekle** iletişim kutusunda **Varsayılan sayfa** modülünü seçin ve **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="b92dc-147">In the **Add Module** dialog box, select the **Default Page** module, and then select **OK**.</span></span>
1. <span data-ttu-id="b92dc-148">**Varsayılan sayfa** modülünde **Ana** bölmeyi seçin, üç nokta düğmesini (...) ve sonra **Modül ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="b92dc-148">In the **Main** slot of the **Default Page** module, select the ellipsis (...), and then select **Add Module**.</span></span>
1. <span data-ttu-id="b92dc-149">**Modül Ekle** iletişim kutusunda **Konteyner** modülünü seçin ve **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="b92dc-149">In the **Add Module** dialog box, select the **Container** module, and then select **OK**.</span></span>
1. <span data-ttu-id="b92dc-150">**Konteyner** yuvası için üç nokta (...) düğmesini seçin ve **Modül Ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="b92dc-150">In the **Container** slot, select the ellipsis (...), and then select **Add Module**.</span></span>
1. <span data-ttu-id="b92dc-151">**Modül Ekle** iletişim kutusunda **İçerik haritası** modülünü seçin ve **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="b92dc-151">In the **Add Module** dialog box, select the **Breadcrumb** module, and then select **OK**.</span></span>
1. <span data-ttu-id="b92dc-152">**İçerik haritası** özellikleri bölmesinde, **Min Gerçekleşme** için **1** değerini girin.</span><span class="sxs-lookup"><span data-stu-id="b92dc-152">In the **Breadcrumb** properties pane, enter the value **1** for **Min Occurs**.</span></span>
1. <span data-ttu-id="b92dc-153">**Konteyner** yuvası için üç nokta (...) düğmesini seçin ve **Modül Ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="b92dc-153">In the **Container** slot, select the ellipsis (...), and then select **Add Module**.</span></span>
1. <span data-ttu-id="b92dc-154">**Modül Ekle** iletişim kutusunda, **Arama sonuçları** modülünü seçin ve **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="b92dc-154">In the **Add Module** dialog box, select the **Search results** module, and then select **OK**.</span></span>
1. <span data-ttu-id="b92dc-155">**Arama sonuçları** özellikleri bölmesinde, **Min Gerçekleşme** için **1** değerini girin ve arama sonuçları modülü için gerekli diğer özellikleri ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="b92dc-155">In the **Search results** properties pane, enter the value **1** for **Min Occurs**, and then set any other required properties for the search results module.</span></span> <span data-ttu-id="b92dc-156">Şablonda bu özellikleri ayarlayarak, belirli bir kategori sayfasındaki özelleştirmelerin bu ayarları otomatik olarak içermesini sağlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="b92dc-156">By setting these properties in the template, you ensure that any customizations to a specific category page will automatically include these settings.</span></span>
1. <span data-ttu-id="b92dc-157">**Düzenlemeyi bitir**'i seçin, ardından şablonu yayımlamak için **Yayımla**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="b92dc-157">Select **Finish editing**, and then select **Publish** to publish the template.</span></span>
1. <span data-ttu-id="b92dc-158">**Sayfalar**'a gidin ve yeni sayfa oluşturmak için **Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="b92dc-158">Go to **Pages**, and select **New** to create a new page.</span></span>
1. <span data-ttu-id="b92dc-159">**Şablon seçin** iletişim kutusunda, oluşturduğunuz **Arama sonuçları** şablonunu seçin, **Sayfa adı** için **Kategori sayfası** girin ve sonra **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="b92dc-159">In the **Choose a template** dialog box, select the **Search results** template that you created, enter **Category page** for **Page name**, and then select **OK**.</span></span> <span data-ttu-id="b92dc-160">Tüm değerler şablonda ayarlandığı için sayfa yayınlanmaya hazırdır.</span><span class="sxs-lookup"><span data-stu-id="b92dc-160">Because all the values are set in the template, the page is ready to be published.</span></span>
1. <span data-ttu-id="b92dc-161">Sayfayı iade etmek için **Düzenlemeyi bitir**'i seçin, ardından yayımlamak için **Yayımla**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="b92dc-161">Select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="b92dc-162">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="b92dc-162">Additional resources</span></span>

[<span data-ttu-id="b92dc-163">Varsayılan kategori açılış sayfası ve arama sonuçları sayfasına genel bakış</span><span class="sxs-lookup"><span data-stu-id="b92dc-163">Default category landing page and search results page overview</span></span>](category-search-page-overview.md)

[<span data-ttu-id="b92dc-164">Modül kitaplığına genel bakış</span><span class="sxs-lookup"><span data-stu-id="b92dc-164">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="b92dc-165">Hızlı görünüm modülü</span><span class="sxs-lookup"><span data-stu-id="b92dc-165">Quick view module</span></span>](quick-view-module.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]