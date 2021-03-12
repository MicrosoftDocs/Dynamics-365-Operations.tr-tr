---
title: İçerik haritası modülü
description: Bu konu içerik haritası modüllerini kapsamaktadır ve Microsoft Dynamics 365 Commerce'un site sayfalarına nasıl ekleneceğini açıklamaktadır.
author: anupamar-ms
manager: annbe
ms.date: 10/20/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: 1883281c62575ae0b48b6e584876185bb179b4f4
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/15/2021
ms.locfileid: "4986091"
---
# <a name="breadcrumb-module"></a><span data-ttu-id="bd7ff-103">İçerik haritası modülü</span><span class="sxs-lookup"><span data-stu-id="bd7ff-103">Breadcrumb module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="bd7ff-104">Bu konu içerik haritası modüllerini kapsamaktadır ve Microsoft Dynamics 365 Commerce'un site sayfalarına nasıl ekleneceğini açıklamaktadır.</span><span class="sxs-lookup"><span data-stu-id="bd7ff-104">This topic covers breadcrumb modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="bd7ff-105">Özet</span><span class="sxs-lookup"><span data-stu-id="bd7ff-105">Overview</span></span>

<span data-ttu-id="bd7ff-106">İçerik haritası modülleri, site sayfalarında ikincil gezinti sağlamak için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="bd7ff-106">Breadcrumb modules are used to provide secondary navigation on site pages.</span></span> <span data-ttu-id="bd7ff-107">Bunlar genellikle sayfanın üst bölümünde, başlığın altında gösterilir.</span><span class="sxs-lookup"><span data-stu-id="bd7ff-107">They are typically shown at the top of a page, below the header.</span></span> <span data-ttu-id="bd7ff-108">Herhangi bir sayfaya içerik haritası modülleri eklenebilse de, bunlar genellikle ürün kategori hiyerarşisini göstermek ve bir sitede dolaşmak için hızlı bir yol sağlamak amacıyla Ürün Ayrıntılar sayfalarında (PDPs) kullanılır.</span><span class="sxs-lookup"><span data-stu-id="bd7ff-108">Although breadcrumb modules can be added to any page, they are most often used on product details pages (PDPs), to show the product category hierarchy and provide a quick way to move around a site.</span></span> <span data-ttu-id="bd7ff-109">Bir içerik haritası modülü, kullanıcılar arama veya liste sayfasından bir PDP açtıklarında "sonuçları geri dön" bağlantısını göstermek için de kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="bd7ff-109">A breadcrumb module can also be used to show a "Back to results" link when users open a PDP from a search or list page.</span></span> <span data-ttu-id="bd7ff-110">Böylece, kullanıcılar alışverişe devam etmek için filtre uygulanmış liste sayfasına hızlıca dönebilir.</span><span class="sxs-lookup"><span data-stu-id="bd7ff-110">In this way, users can quickly return to their filtered list page to continue shopping.</span></span>

<span data-ttu-id="bd7ff-111">PDPs ve kategori sayfaları gibi ürün kategorisi bağlamı bulunan sayfalarda, içerik haritası modülleri kategori hiyerarşisini gösterir.</span><span class="sxs-lookup"><span data-stu-id="bd7ff-111">On pages that have product category context, such as PDPs and category pages, breadcrumb modules show the category hierarchy.</span></span> <span data-ttu-id="bd7ff-112">Kategori bağlamına sahip olmayan sayfalarda, içerik haritası modülleri Varsayılan olarak **&lt;site kökü&gt; / &lt;Geçerli sayfasını&gt;** gösterir.</span><span class="sxs-lookup"><span data-stu-id="bd7ff-112">On pages that don't have category context, breadcrumb modules show **&lt;Site root&gt; / &lt;Current page&gt;** by default.</span></span> <span data-ttu-id="bd7ff-113">İçerik haritası modülleri, sitedeki belirli sayfalara yönelik bağlantıları göstermek üzere diğer site sayfası türlerinde da el ile yapılandırılabilir.</span><span class="sxs-lookup"><span data-stu-id="bd7ff-113">Breadcrumb modules can also be manually configured on other types of site pages to show links to specific pages on the site.</span></span>

> [!NOTE]
> <span data-ttu-id="bd7ff-114">İçerik haritası modülü Dynamics 365 Commerce 10.0.12 sürümünde bulunur.</span><span class="sxs-lookup"><span data-stu-id="bd7ff-114">The breadcrumb module is available in the Dynamics 365 Commerce 10.0.12 release.</span></span>

<span data-ttu-id="bd7ff-115">Aşağıdaki resimde, bir PDP üzerinde kategori hiyerarşisini gösteren bir içerik haritası modülü örneği gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="bd7ff-115">The following image shows an example of a breadcrumb module that shows the category hierarchy on a PDP.</span></span>

![içerik haritası modülü örneği](./media/ecommerce-breadcrumb.PNG)

## <a name="breadcrumb-module-settings"></a><span data-ttu-id="bd7ff-117">İçerik haritası modülü ayarları</span><span class="sxs-lookup"><span data-stu-id="bd7ff-117">Breadcrumb module settings</span></span>

<span data-ttu-id="bd7ff-118">İçerik haritası modülü, Site oluşturucuda **site ayarları \> Uzantılarda** tanımlanan **PDP ayarında içerik haritası görüntüleme** türüne dayanır.</span><span class="sxs-lookup"><span data-stu-id="bd7ff-118">The breadcrumb module relies on the **Breadcrumb display type on PDP** setting, which is defined at **Site Settings \> Extensions** in site builder.</span></span> <span data-ttu-id="bd7ff-119">Bu seçenek üç olası değer vardır:</span><span class="sxs-lookup"><span data-stu-id="bd7ff-119">This setting has three possible values:</span></span>

- <span data-ttu-id="bd7ff-120">**Kategori hiyerarşisini göster** – Bu değer seçildiğinde, içerik haritası modülü PDP 'de görüntülenen ürünün tam kategori hiyerarşisini gösterir.</span><span class="sxs-lookup"><span data-stu-id="bd7ff-120">**Show category hierarchy** – When this value is selected, the breadcrumb module will show the full category hierarchy of the product that is viewed on the PDP.</span></span>
- <span data-ttu-id="bd7ff-121">**Sonuçlara geri dön** – Bu değer seçildiğinde, içerik haritası modülü, Kullanıcı PDP'yi "geri dön" bağlantısına izin veren bir modülden açarsa bir PDP'de "sonuçları geri dön" bağlantısını gösterecektir.</span><span class="sxs-lookup"><span data-stu-id="bd7ff-121">**Show back to results** – When this value is selected, the breadcrumb module will show a "Back to results" link on a PDP if the user opened the PDP from a module that allows for a "Back to results" link.</span></span> <span data-ttu-id="bd7ff-122">Kullanıcılar kategori, arama, liste ve öneri listeleri sayfalarından gezindiğinizde bu işlev kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="bd7ff-122">This functionality is available when users navigate from category, search, list, and recommendation lists pages.</span></span> <span data-ttu-id="bd7ff-123">Bu işlevi desteklemek için, ürün koleksiyonu ve arama sonuçları modülleri, **PDP 'deki sonuçlara yeniden izin ver** adında bir özelliğe sahiptir.</span><span class="sxs-lookup"><span data-stu-id="bd7ff-123">To support this functionality, product collection and search results modules have a property that is named **Allow back to results on PDP**.</span></span> <span data-ttu-id="bd7ff-124">Bu özellik, PDP 'deki "sonuçlara dön" bağlantı işlevini desteklemesi gereken modülleri tanımlama esnekliği sağlar.</span><span class="sxs-lookup"><span data-stu-id="bd7ff-124">This property gives you the flexibility to define which modules should support the "Back to results" link functionality on the PDP.</span></span> <span data-ttu-id="bd7ff-125">Örneğin, **içerik haritası modülünün PDP** ayarında içerik haritası görüntüleme türü için **sonuçlara geri döndüğünüzde** seçilir ve **arama sayfası arama sonuçları modülü için** PDP ile ilgili sonuçlara geri dönme olanağı varsa , kullanıcılar arama sayfasından bir PDP 'ye gezinirse "sonuçlara dön" bağlantısı görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="bd7ff-125">For example, when **Show back to results** is selected for the **Breadcrumb display type on PDP** setting of the breadcrumb module, and **Allow back to results on PDP** is selected for the search page search results module, a "Back to results" link will be shown when users navigate from the search page to a PDP.</span></span>
- <span data-ttu-id="bd7ff-126">**Kategori hiyerarşisini göster ve sonuçlara dön** – Bu değer önceki iki değerin birleşimidir.</span><span class="sxs-lookup"><span data-stu-id="bd7ff-126">**Show category hierarchy and back to results** – This value is a combination of the previous two.</span></span> <span data-ttu-id="bd7ff-127">Bu değer seçildiğinde, içerik haritası modülü bir PDP üzerinde hem tam kategori hiyerarşisini hem de "sonuçları geri" bağlantısı (yapılandırılmışsa) gösterir.</span><span class="sxs-lookup"><span data-stu-id="bd7ff-127">When this value is selected, the breadcrumb module will show both the full category hierarchy and a "Back to results" link (if it's configured) on a PDP.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="bd7ff-128">Bu ayarlar Dynamics 365 Commerce 10.0.12 sürümünde bulunmaktadır.</span><span class="sxs-lookup"><span data-stu-id="bd7ff-128">These settings are available in the Dynamics 365 Commerce 10.0.12 release.</span></span> <span data-ttu-id="bd7ff-129">Dynamics 365 Commerce'nin eski sürümlerinden birini güncelleştiriyorsanız, appSettings. json dosyasını el ile güncelleştirmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="bd7ff-129">If you are updating from an older version of Dynamics 365 Commerce, you must manually update the appsettings.json file.</span></span> <span data-ttu-id="bd7ff-130">AppSettings.json dosyasını güncelleştirme yönergeleri için bkz. [SDK ve modül kitaplığı güncelleştirmeleri](e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file).</span><span class="sxs-lookup"><span data-stu-id="bd7ff-130">For instructions on updating the appsettings.json file, see [SDK and module library updates](e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file).</span></span>

## <a name="breadcrumb-module-properties"></a><span data-ttu-id="bd7ff-131">İçerik haritası modülü özellikleri</span><span class="sxs-lookup"><span data-stu-id="bd7ff-131">Breadcrumb module properties</span></span>

| <span data-ttu-id="bd7ff-132">Özellik adı</span><span class="sxs-lookup"><span data-stu-id="bd7ff-132">Property name</span></span> | <span data-ttu-id="bd7ff-133">Değerler</span><span class="sxs-lookup"><span data-stu-id="bd7ff-133">Values</span></span> | <span data-ttu-id="bd7ff-134">Tanım</span><span class="sxs-lookup"><span data-stu-id="bd7ff-134">Description</span></span> |
|---------------|--------|-------------|
| <span data-ttu-id="bd7ff-135">Kök</span><span class="sxs-lookup"><span data-stu-id="bd7ff-135">Root</span></span> | <span data-ttu-id="bd7ff-136">Metin veya bağlantı</span><span class="sxs-lookup"><span data-stu-id="bd7ff-136">Text or link</span></span>| <span data-ttu-id="bd7ff-137">Bu isteğe bağlı özellik, içerik haritası site kökünün bağlantı metnini ve bağlantı hedefini belirtir.</span><span class="sxs-lookup"><span data-stu-id="bd7ff-137">This optional property specifies link text and a link target for the breadcrumb site root.</span></span> <span data-ttu-id="bd7ff-138">Bu özellik yapılandırılmazsa, kök tanımlanmayacaktır.</span><span class="sxs-lookup"><span data-stu-id="bd7ff-138">If this property isn't configured, no root will be defined.</span></span> |
| <span data-ttu-id="bd7ff-139">İçerik haritası bağlantısı</span><span class="sxs-lookup"><span data-stu-id="bd7ff-139">Breadcrumb link</span></span> | <span data-ttu-id="bd7ff-140">Bağla</span><span class="sxs-lookup"><span data-stu-id="bd7ff-140">Link</span></span> | <span data-ttu-id="bd7ff-141">Bu isteğe bağlı özellik, el ile konfigüre edilmiş bir içerik haritası için bağlantıları belirtir.</span><span class="sxs-lookup"><span data-stu-id="bd7ff-141">This optional property specifies links for a manually configured breadcrumb, if these links are required.</span></span> <span data-ttu-id="bd7ff-142">Bağlantılar listelendikleri sırada görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="bd7ff-142">Links appear in the order that they are listed in.</span></span> |

## <a name="add-a-breadcrumb-module-to-a-new-page"></a><span data-ttu-id="bd7ff-143">Yeni sayfaya içerik haritası modülü ekleme</span><span class="sxs-lookup"><span data-stu-id="bd7ff-143">Add a breadcrumb module to a new page</span></span>

<span data-ttu-id="bd7ff-144">Bir PDP'ye içerik haritası modülü eklemek ve gerekli özellikleri ayarlamak için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="bd7ff-144">To add a breadcrumb module to a PDP and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="bd7ff-145">**Site ayarları \> uzantılarına** gidin ve **PDP ayarında içerik haritası** görüntüleme türü için **Kategori hiyerarşisini göster**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="bd7ff-145">Go to **Site Settings \> Extensions**, and then, for the **Breadcrumb display type on PDP** setting, select **Show category hierarchy**.</span></span>
1. <span data-ttu-id="bd7ff-146">**Şablonlara** gidin ve PDP şablonunu seçin.</span><span class="sxs-lookup"><span data-stu-id="bd7ff-146">Go to **Templates**, and select the PDP template.</span></span>
1. <span data-ttu-id="bd7ff-147">**Konteyner** modülünü içeren kapsayıcı yuvasında üç noktayı (**...**) seçin ve sonra **Modül Ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="bd7ff-147">In the **Container** slot that contains the buy box module, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="bd7ff-148">**Modül Ekle** iletişim kutusunda **İçerik haritası** modülünü seçin ve **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="bd7ff-148">In the **Add Module** dialog box, select the **Breadcrumb** module, and then select **OK**.</span></span>
1. <span data-ttu-id="bd7ff-149">**Kaydet**'i seçin, şablonu iade etmek için **Düzenlemeyi bitir**'i ve ardından yayımlamak için **Yayımla**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="bd7ff-149">Select **Save**, select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span>
1. <span data-ttu-id="bd7ff-150">**Sayfalara** gidin ve PDP şablonunu kullanan bir PDP açın.</span><span class="sxs-lookup"><span data-stu-id="bd7ff-150">Go to **Pages**, and open a PDP that uses the PDP template.</span></span> <span data-ttu-id="bd7ff-151">Bir PDP henüz oluşturulmamışsa, bir tane oluşturun.</span><span class="sxs-lookup"><span data-stu-id="bd7ff-151">If a PDP doesn't yet exist, create one.</span></span>
1. <span data-ttu-id="bd7ff-152">**Konteyner** modülünü içeren kapsayıcı yuvasında üç noktayı (**...**) seçin ve sonra **Modül Ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="bd7ff-152">In the **Container** slot that contains the buy box module, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="bd7ff-153">**Modül Ekle** iletişim kutusunda **İçerik haritası** modülünü seçin ve **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="bd7ff-153">In the **Add Module** dialog box, select the **Breadcrumb** module, and then select **OK**.</span></span>
1. <span data-ttu-id="bd7ff-154">**İçerik haritası** yuvasının Özellikler bölmesinde , **kök** altında **bağlantı metni** 'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="bd7ff-154">In the properties pane of the **Breadcrumb** slot, under **Root**, select **Link text**.</span></span>
1. <span data-ttu-id="bd7ff-155">**Bağlantı metni** iletişim kutusunda **giriş**'ı girin ve sonra **bağlantı hedefi** altında **bağlantı Ekle** 'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="bd7ff-155">In the **Link text** dialog box, enter **Home**, and then, under **Link target**, select **Add a link**.</span></span>
1. <span data-ttu-id="bd7ff-156">**Bağlantı ekle** iletişim kutusunda içerik haritası kökü bağlantısını seçin ve **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="bd7ff-156">In the **Add a link** dialog box, select a link for the breadcrumb root, and then select **OK**.</span></span>
1. <span data-ttu-id="bd7ff-157">**Kaydet**'i seçin ve ardından sayfayı önizlemek için **Önizleme**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="bd7ff-157">Select **Save**, and then select **Preview** to preview the page.</span></span>
1. <span data-ttu-id="bd7ff-158">Şablonu iade etmek için **Düzenlemeyi bitir**'i seçin, ardından yayımlamak için **Yayımla**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="bd7ff-158">Select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="bd7ff-159">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="bd7ff-159">Additional resources</span></span>

[<span data-ttu-id="bd7ff-160">Modül kitaplığına genel bakış</span><span class="sxs-lookup"><span data-stu-id="bd7ff-160">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="bd7ff-161">Gezinti menüsü modülü</span><span class="sxs-lookup"><span data-stu-id="bd7ff-161">Navigation menu module</span></span>](nav-menu-module.md)

[<span data-ttu-id="bd7ff-162">Site seçicisi modülü</span><span class="sxs-lookup"><span data-stu-id="bd7ff-162">Site selector module</span></span>](site-selector.md)

[<span data-ttu-id="bd7ff-163">Varsayılan kategori açılış sayfası ve arama sonuçları sayfasına genel bakış</span><span class="sxs-lookup"><span data-stu-id="bd7ff-163">Overview of default category landing page and search results page</span></span>](category-search-page-overview.md)

[<span data-ttu-id="bd7ff-164">Ürün topluluğu modülleri</span><span class="sxs-lookup"><span data-stu-id="bd7ff-164">Product collection modules</span></span>](product-collection-module-overview.md)

[<span data-ttu-id="bd7ff-165">Satın alma kutusu modülü</span><span class="sxs-lookup"><span data-stu-id="bd7ff-165">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="bd7ff-166">SDK ve modül kitaplığı güncelleştirmeleri</span><span class="sxs-lookup"><span data-stu-id="bd7ff-166">SDK and module library updates</span></span>](e-commerce-extensibility/sdk-updates.md)
