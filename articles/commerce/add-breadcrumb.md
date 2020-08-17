---
title: İçerik haritası modülü
description: Bu konu içerik haritası modüllerini kapsamaktadır ve Microsoft Dynamics 365 Commerce'un site sayfalarına nasıl ekleneceğini açıklamaktadır.
author: anupamar-ms
manager: annbe
ms.date: 06/01/2020
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
ms.openlocfilehash: 38efc3a60ae0ba49db2036dc84c49e4896727d94
ms.sourcegitcommit: 4a981ee4be6d7e6c0e55541535d386bce2565cba
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/27/2020
ms.locfileid: "3621072"
---
# <a name="breadcrumb-module"></a><span data-ttu-id="f76a9-103">İçerik haritası modülü</span><span class="sxs-lookup"><span data-stu-id="f76a9-103">Breadcrumb module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="f76a9-104">Bu konu içerik haritası modüllerini kapsamaktadır ve Microsoft Dynamics 365 Commerce'un site sayfalarına nasıl ekleneceğini açıklamaktadır.</span><span class="sxs-lookup"><span data-stu-id="f76a9-104">This topic covers breadcrumb modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="f76a9-105">Özet</span><span class="sxs-lookup"><span data-stu-id="f76a9-105">Overview</span></span>

<span data-ttu-id="f76a9-106">İçerik haritası modülleri, site sayfalarında ikincil gezinti sağlamak için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="f76a9-106">Breadcrumb modules are used to provide secondary navigation on site pages.</span></span> <span data-ttu-id="f76a9-107">Bunlar genellikle sayfanın üst bölümünde, başlığın altında gösterilir.</span><span class="sxs-lookup"><span data-stu-id="f76a9-107">They are typically shown at the top of a page, below the header.</span></span> <span data-ttu-id="f76a9-108">Herhangi bir sayfaya içerik haritası modülleri eklenebilse de, bunlar genellikle ürün kategori hiyerarşisini göstermek ve bir sitede dolaşmak için hızlı bir yol sağlamak amacıyla Ürün Ayrıntılar sayfalarında (PDPs) kullanılır.</span><span class="sxs-lookup"><span data-stu-id="f76a9-108">Although breadcrumb modules can be added to any page, they are most often used on product details pages (PDPs), to show the product category hierarchy and provide a quick way to move around a site.</span></span> <span data-ttu-id="f76a9-109">Bir içerik haritası modülü, kullanıcılar arama veya liste sayfasından bir PDP açtıklarında "sonuçları geri dön" bağlantısını göstermek için de kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="f76a9-109">A breadcrumb module can also be used to show a "Back to results" link when users open a PDP from a search or list page.</span></span> <span data-ttu-id="f76a9-110">Böylece, kullanıcılar alışverişe devam etmek için filtre uygulanmış liste sayfasına hızlıca dönebilir.</span><span class="sxs-lookup"><span data-stu-id="f76a9-110">In this way, users can quickly return to their filtered list page to continue shopping.</span></span>

<span data-ttu-id="f76a9-111">PDPs ve kategori sayfaları gibi ürün kategorisi bağlamı bulunan sayfalarda, içerik haritası modülleri kategori hiyerarşisini gösterir.</span><span class="sxs-lookup"><span data-stu-id="f76a9-111">On pages that have product category context, such as PDPs and category pages, breadcrumb modules show the category hierarchy.</span></span> <span data-ttu-id="f76a9-112">Kategori bağlamına sahip olmayan sayfalarda, içerik haritası modülleri Varsayılan olarak **&lt;site kökü&gt; / &lt;Geçerli sayfasını&gt;** gösterir.</span><span class="sxs-lookup"><span data-stu-id="f76a9-112">On pages that don't have category context, breadcrumb modules show **&lt;Site root&gt; / &lt;Current page&gt;** by default.</span></span> <span data-ttu-id="f76a9-113">İçerik haritası modülleri, sitedeki belirli sayfalara yönelik bağlantıları göstermek üzere diğer site sayfası türlerinde da el ile yapılandırılabilir.</span><span class="sxs-lookup"><span data-stu-id="f76a9-113">Breadcrumb modules can also be manually configured on other types of site pages to show links to specific pages on the site.</span></span>

<span data-ttu-id="f76a9-114">Aşağıdaki resimde, bir PDP üzerinde kategori hiyerarşisini gösteren bir içerik haritası modülü örneği gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="f76a9-114">The following image shows an example of a breadcrumb module that shows the category hierarchy on a PDP.</span></span>

![içerik haritası modülü örneği](./media/ecommerce-breadcrumb.PNG)

## <a name="breadcrumb-module-settings"></a><span data-ttu-id="f76a9-116">İçerik haritası modülü ayarları</span><span class="sxs-lookup"><span data-stu-id="f76a9-116">Breadcrumb module settings</span></span>

<span data-ttu-id="f76a9-117">İçerik haritası modülü, Site oluşturucuda **site ayarları \> Uzantılarda** tanımlanan **PDP ayarında içerik haritası görüntüleme** türüne dayanır.</span><span class="sxs-lookup"><span data-stu-id="f76a9-117">The breadcrumb module relies on the **Breadcrumb display type on PDP** setting, which is defined at **Site Settings \> Extensions** in site builder.</span></span> <span data-ttu-id="f76a9-118">Bu seçenek üç olası değer vardır:</span><span class="sxs-lookup"><span data-stu-id="f76a9-118">This setting has three possible values:</span></span>

- <span data-ttu-id="f76a9-119">**Kategori hiyerarşisini göster** – Bu değer seçildiğinde, içerik haritası modülü PDP 'de görüntülenen ürünün tam kategori hiyerarşisini gösterir.</span><span class="sxs-lookup"><span data-stu-id="f76a9-119">**Show category hierarchy** – When this value is selected, the breadcrumb module will show the full category hierarchy of the product that is viewed on the PDP.</span></span>
- <span data-ttu-id="f76a9-120">**Sonuçlara geri dön** – Bu değer seçildiğinde, içerik haritası modülü, Kullanıcı PDP'yi "geri dön" bağlantısına izin veren bir modülden açarsa bir PDP'de "sonuçları geri dön" bağlantısını gösterecektir.</span><span class="sxs-lookup"><span data-stu-id="f76a9-120">**Show back to results** – When this value is selected, the breadcrumb module will show a "Back to results" link on a PDP if the user opened the PDP from a module that allows for a "Back to results" link.</span></span> <span data-ttu-id="f76a9-121">Kullanıcılar kategori, arama, liste ve öneri listeleri sayfalarından gezindiğinizde bu işlev kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="f76a9-121">This functionality is available when users navigate from category, search, list, and recommendation lists pages.</span></span> <span data-ttu-id="f76a9-122">Bu işlevi desteklemek için, ürün koleksiyonu ve arama sonuçları modülleri, **PDP 'deki sonuçlara yeniden izin ver** adında bir özelliğe sahiptir.</span><span class="sxs-lookup"><span data-stu-id="f76a9-122">To support this functionality, product collection and search results modules have a property that is named **Allow back to results on PDP**.</span></span> <span data-ttu-id="f76a9-123">Bu özellik, PDP 'deki "sonuçlara dön" bağlantı işlevini desteklemesi gereken modülleri tanımlama esnekliği sağlar.</span><span class="sxs-lookup"><span data-stu-id="f76a9-123">This property gives you the flexibility to define which modules should support the "Back to results" link functionality on the PDP.</span></span> <span data-ttu-id="f76a9-124">Örneğin, **içerik haritası modülünün PDP** ayarında içerik haritası görüntüleme türü için **sonuçlara geri döndüğünüzde** seçilir ve **arama sayfası arama sonuçları modülü için** PDP ile ilgili sonuçlara geri dönme olanağı varsa , kullanıcılar arama sayfasından bir PDP 'ye gezinirse "sonuçlara dön" bağlantısı görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="f76a9-124">For example, when **Show back to results** is selected for the **Breadcrumb display type on PDP** setting of the breadcrumb module, and **Allow back to results on PDP** is selected for the search page search results module, a "Back to results" link will be shown when users navigate from the search page to a PDP.</span></span>
- <span data-ttu-id="f76a9-125">**Kategori hiyerarşisini göster ve sonuçlara dön** – Bu değer önceki iki değerin birleşimidir.</span><span class="sxs-lookup"><span data-stu-id="f76a9-125">**Show category hierarchy and back to results** – This value is a combination of the previous two.</span></span> <span data-ttu-id="f76a9-126">Bu değer seçildiğinde, içerik haritası modülü bir PDP üzerinde hem tam kategori hiyerarşisini hem de "sonuçları geri" bağlantısı (yapılandırılmışsa) gösterir.</span><span class="sxs-lookup"><span data-stu-id="f76a9-126">When this value is selected, the breadcrumb module will show both the full category hierarchy and a "Back to results" link (if it's configured) on a PDP.</span></span>

## <a name="breadcrumb-module-properties"></a><span data-ttu-id="f76a9-127">İçerik haritası modülü özellikleri</span><span class="sxs-lookup"><span data-stu-id="f76a9-127">Breadcrumb module properties</span></span>

| <span data-ttu-id="f76a9-128">Özellik adı</span><span class="sxs-lookup"><span data-stu-id="f76a9-128">Property name</span></span> | <span data-ttu-id="f76a9-129">Değerler</span><span class="sxs-lookup"><span data-stu-id="f76a9-129">Values</span></span> | <span data-ttu-id="f76a9-130">Tanım</span><span class="sxs-lookup"><span data-stu-id="f76a9-130">Description</span></span> |
|---------------|--------|-------------|
| <span data-ttu-id="f76a9-131">Kök</span><span class="sxs-lookup"><span data-stu-id="f76a9-131">Root</span></span> | <span data-ttu-id="f76a9-132">Metin veya bağlantı</span><span class="sxs-lookup"><span data-stu-id="f76a9-132">Text or link</span></span>| <span data-ttu-id="f76a9-133">Bu isteğe bağlı özellik, içerik haritası site kökünün bağlantı metnini ve bağlantı hedefini belirtir.</span><span class="sxs-lookup"><span data-stu-id="f76a9-133">This optional property specifies link text and a link target for the breadcrumb site root.</span></span> <span data-ttu-id="f76a9-134">Bu özellik yapılandırılmazsa, kök tanımlanmayacaktır.</span><span class="sxs-lookup"><span data-stu-id="f76a9-134">If this property isn't configured, no root will be defined.</span></span> |
| <span data-ttu-id="f76a9-135">İçerik haritası bağlantısı</span><span class="sxs-lookup"><span data-stu-id="f76a9-135">Breadcrumb link</span></span> | <span data-ttu-id="f76a9-136">Bağla</span><span class="sxs-lookup"><span data-stu-id="f76a9-136">Link</span></span> | <span data-ttu-id="f76a9-137">Bu isteğe bağlı özellik, el ile konfigüre edilmiş bir içerik haritası için bağlantıları belirtir.</span><span class="sxs-lookup"><span data-stu-id="f76a9-137">This optional property specifies links for a manually configured breadcrumb, if these links are required.</span></span> <span data-ttu-id="f76a9-138">Bağlantılar listelendikleri sırada görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="f76a9-138">Links appear in the order that they are listed in.</span></span> |

## <a name="add-a-breadcrumb-module-to-a-new-page"></a><span data-ttu-id="f76a9-139">Yeni sayfaya içerik haritası modülü ekleme</span><span class="sxs-lookup"><span data-stu-id="f76a9-139">Add a breadcrumb module to a new page</span></span>

<span data-ttu-id="f76a9-140">Bir PDP'ye içerik haritası modülü eklemek ve gerekli özellikleri ayarlamak için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="f76a9-140">To add a breadcrumb module to a PDP and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="f76a9-141">**Site ayarları /> uzantılarına** gidin ve **PDP ayarında içerik haritası görüntüleme türü** için **Kategori hiyerarşisini göster**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="f76a9-141">Go to **Site Settings /> Extensions**, and then, for the **Breadcrumb display type on PDP** setting, select **Show category hierarchy**.</span></span>
1. <span data-ttu-id="f76a9-142">**Şablonlara** gidin ve PDP şablonunu seçin.</span><span class="sxs-lookup"><span data-stu-id="f76a9-142">Go to **Templates**, and select the PDP template.</span></span>
1. <span data-ttu-id="f76a9-143">**Konteyner** modülünü içeren kapsayıcı yuvasında üç noktayı (**...**) seçin ve sonra **Modül Ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="f76a9-143">In the **Container** slot that contains the buy box module, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="f76a9-144">**Modül Ekle** iletişim kutusunda **İçerik haritası** modülünü seçin ve **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="f76a9-144">In the **Add Module** dialog box, select the **Breadcrumb** module, and then select **OK**.</span></span>
1. <span data-ttu-id="f76a9-145">**Kaydet**'i seçin, şablonu iade etmek için **Düzenlemeyi bitir**'i ve ardından yayımlamak için **Yayımla**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="f76a9-145">Select **Save**, select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span>
1. <span data-ttu-id="f76a9-146">**Sayfalara** gidin ve PDP şablonunu kullanan bir PDP açın.</span><span class="sxs-lookup"><span data-stu-id="f76a9-146">Go to **Pages**, and open a PDP that uses the PDP template.</span></span> <span data-ttu-id="f76a9-147">Bir PDP henüz oluşturulmamışsa, bir tane oluşturun.</span><span class="sxs-lookup"><span data-stu-id="f76a9-147">If a PDP doesn't yet exist, create one.</span></span>
1. <span data-ttu-id="f76a9-148">**Konteyner** modülünü içeren kapsayıcı yuvasında üç noktayı (**...**) seçin ve sonra **Modül Ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="f76a9-148">In the **Container** slot that contains the buy box module, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="f76a9-149">**Modül Ekle** iletişim kutusunda **İçerik haritası** modülünü seçin ve **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="f76a9-149">In the **Add Module** dialog box, select the **Breadcrumb** module, and then select **OK**.</span></span>
1. <span data-ttu-id="f76a9-150">**İçerik haritası** yuvasının Özellikler bölmesinde , **kök** altında **bağlantı metni** 'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="f76a9-150">In the properties pane of the **Breadcrumb** slot, under **Root**, select **Link text**.</span></span>
1. <span data-ttu-id="f76a9-151">**Bağlantı metni** iletişim kutusunda **giriş**'ı girin ve sonra **bağlantı hedefi** altında **bağlantı Ekle** 'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="f76a9-151">In the **Link text** dialog box, enter **Home**, and then, under **Link target**, select **Add a link**.</span></span>
1. <span data-ttu-id="f76a9-152">**Bağlantı ekle** iletişim kutusunda içerik haritası kökü bağlantısını seçin ve **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="f76a9-152">In the **Add a link** dialog box, select a link for the breadcrumb root, and then select **OK**.</span></span>
1. <span data-ttu-id="f76a9-153">**Kaydet**'i seçin ve ardından sayfayı önizlemek için **Önizleme**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="f76a9-153">Select **Save**, and then select **Preview** to preview the page.</span></span>
1. <span data-ttu-id="f76a9-154">Şablonu iade etmek için **Düzenlemeyi bitir**'i seçin, ardından yayımlamak için **Yayımla**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="f76a9-154">Select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="f76a9-155">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="f76a9-155">Additional resources</span></span>

[<span data-ttu-id="f76a9-156">Başlangıç paketine genel bakış</span><span class="sxs-lookup"><span data-stu-id="f76a9-156">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="f76a9-157">Varsayılan kategori açılış sayfası ve arama sonuçları sayfasına genel bakış</span><span class="sxs-lookup"><span data-stu-id="f76a9-157">Overview of default category landing page and search results page</span></span>](category-search-page-overview.md)

[<span data-ttu-id="f76a9-158">Ürün topluluğu modülleri</span><span class="sxs-lookup"><span data-stu-id="f76a9-158">Product collection modules</span></span>](product-collection-module-overview.md)

[<span data-ttu-id="f76a9-159">Satınalma kutusu modülü</span><span class="sxs-lookup"><span data-stu-id="f76a9-159">Buy box module</span></span>](add-buy-box.md)
