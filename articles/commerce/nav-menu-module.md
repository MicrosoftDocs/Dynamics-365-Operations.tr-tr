---
title: Gezinti menüsü modülleri
description: Bu konu gezinti menüsü modüllerini kapsamaktadır ve Microsoft Dynamics 365 Commerce'un site sayfalarına nasıl ekleneceğini açıklamaktadır.
author: anupamar-ms
manager: annbe
ms.date: 01/28/2021
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
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: f3461993e2bd59d66be1640331e4ef315a078469
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5251223"
---
# <a name="navigation-menu-module"></a><span data-ttu-id="ce05b-103">Gezinti menüsü modülleri</span><span class="sxs-lookup"><span data-stu-id="ce05b-103">Navigation menu module</span></span>

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

<span data-ttu-id="ce05b-104">Bu konu gezinti menüsü modüllerini kapsamaktadır ve Microsoft Dynamics 365 Commerce'un site sayfalarına nasıl ekleneceğini açıklamaktadır.</span><span class="sxs-lookup"><span data-stu-id="ce05b-104">This topic covers navigation menu modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="ce05b-105">Gezinti menüsü modüllerinin başlıca amacı, site kullanıcılarının Dynamics 365 Commerce yönetim merkezinde tanımlanan kanal gezinti hiyerarşisine göre ürün ve site sayfalarına göz atmasına olanak sağlamaktır.</span><span class="sxs-lookup"><span data-stu-id="ce05b-105">The primary purpose of navigation menu modules is to allow site users to browse products and site pages according to the channel navigation hierarchy defined in Dynamics 365 Commerce headquarters.</span></span> <span data-ttu-id="ce05b-106">Bir gezinti menüsü modülünde yapılandırılan öğeler site üstbilgisi gezintisi olarak görünür.</span><span class="sxs-lookup"><span data-stu-id="ce05b-106">Items configured in a navigation menu module appear as site header navigation.</span></span> <span data-ttu-id="ce05b-107">Gezinti menüsü modülleri, bir e-ticaret sitesindeki diğer sayfalara bağlantı sağlayan statik menü öğelerini de destekler.</span><span class="sxs-lookup"><span data-stu-id="ce05b-107">Navigation menu modules also support static menu items that link to other pages on an e-Commerce site.</span></span>

<span data-ttu-id="ce05b-108">Gezinti menüsü modülü bir sayfanın üst bilgi modülüne eklenebilir.</span><span class="sxs-lookup"><span data-stu-id="ce05b-108">The navigation menu module can be added to the header module of a page.</span></span> <span data-ttu-id="ce05b-109">Fabrikam temasında, gezinti menüsü varsayılan olarak iki düzey gösterir.</span><span class="sxs-lookup"><span data-stu-id="ce05b-109">In the Fabrikam theme, the navigation menu shows two levels by default.</span></span> <span data-ttu-id="ce05b-110">Starter temasında, gezinti menüsü varsayılan olarak üç düzey gösterir.</span><span class="sxs-lookup"><span data-stu-id="ce05b-110">In the Starter theme, the navigation menu shows three levels by default.</span></span> <span data-ttu-id="ce05b-111">Düzey sayısını değiştirmek için temada bir görünüm uzantısı gereklidir.</span><span class="sxs-lookup"><span data-stu-id="ce05b-111">To change to the number of levels, a view extension is required on the theme.</span></span>

<span data-ttu-id="ce05b-112">Aşağıdaki çizimde, iki düzey kategori hiyerarşisi ve bazı statik menü öğeleri bulunan Fabrikam sitesi için bir gezinti menüsü örneği gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="ce05b-112">The following illustration shows an example of a navigation menu for the Fabrikam site with two levels of category hierarchy and some static menu items.</span></span>
<span data-ttu-id="ce05b-113">![Gezinti menüsü modülü örneği](./media/ecommerce-header.png)</span><span class="sxs-lookup"><span data-stu-id="ce05b-113">![Example of a navigation meu module](./media/ecommerce-header.png)</span></span>

## <a name="navigation-menu-module-properties"></a><span data-ttu-id="ce05b-114">Gezinti menüsü modüllerinin özellikleri</span><span class="sxs-lookup"><span data-stu-id="ce05b-114">Navigation menu module properties</span></span>

| <span data-ttu-id="ce05b-115">Özellik adı</span><span class="sxs-lookup"><span data-stu-id="ce05b-115">Property name</span></span>             | <span data-ttu-id="ce05b-116">Değer</span><span class="sxs-lookup"><span data-stu-id="ce05b-116">Value</span></span>                 | <span data-ttu-id="ce05b-117">Tanım</span><span class="sxs-lookup"><span data-stu-id="ce05b-117">Description</span></span> |
|---------------------------|-----------------------|-------------|
| <span data-ttu-id="ce05b-118">Kaynak</span><span class="sxs-lookup"><span data-stu-id="ce05b-118">Source</span></span>                  | <span data-ttu-id="ce05b-119">**Perakende**, **El ile yazma**, **Perakende ve el ile yazma**</span><span class="sxs-lookup"><span data-stu-id="ce05b-119">**Retail**, **Manual authoring**, **Retail and manual authoring**</span></span> | <span data-ttu-id="ce05b-120">**Perakende** değeri, Commerce yönetim merkezinde kanal gezinme hiyerarşisinin gezinti menüsünde görüntülenmesini sağlar.</span><span class="sxs-lookup"><span data-stu-id="ce05b-120">The **Retail** value allows the channel navigation hierarchy from Commerce headquarters to be displayed on the navigation menu.</span></span> <span data-ttu-id="ce05b-121">**El ile yazma** değeri statik menü öğelerinin oluşturulmasına izin verir.</span><span class="sxs-lookup"><span data-stu-id="ce05b-121">The **Manual authoring** value allows static menu items to be curated.</span></span> <span data-ttu-id="ce05b-122">**Perakende ve el ile yazma** değeri, her ikisinin karışımına izin verir.</span><span class="sxs-lookup"><span data-stu-id="ce05b-122">The **Retail and manual authoring** value allows a mix of both.</span></span> |
| <span data-ttu-id="ce05b-123">Kategori resimlerini göster</span><span class="sxs-lookup"><span data-stu-id="ce05b-123">Show category images</span></span> | <span data-ttu-id="ce05b-124">**Doğru** veya **yanlış**</span><span class="sxs-lookup"><span data-stu-id="ce05b-124">**True** or **False**</span></span>    | <span data-ttu-id="ce05b-125">Etkinleştirildiğinde, bu özellik gezinti menüsündeki kategori resimlerini her kategori için Commerce yönetim merkezinde tanımlandığı şekilde görüntüler.</span><span class="sxs-lookup"><span data-stu-id="ce05b-125">When enabled, this property displays category images on the navigation menu as defined in Commerce headquarters for each category.</span></span> <span data-ttu-id="ce05b-126">Commerce sürüm 10.0.14'e eklendi.</span><span class="sxs-lookup"><span data-stu-id="ce05b-126">Added in Commerce release 10.0.14.</span></span> |
| <span data-ttu-id="ce05b-127">Promosyonları gösterme</span><span class="sxs-lookup"><span data-stu-id="ce05b-127">Show promotions</span></span> | <span data-ttu-id="ce05b-128">**Doğru** veya **yanlış**</span><span class="sxs-lookup"><span data-stu-id="ce05b-128">**True** or **False**</span></span> | <span data-ttu-id="ce05b-129">Bu özellik etkinleştirildiğinde, promosyonlar resimler, bağlantılar ve metin kullanılarak yapılandırılabilir.</span><span class="sxs-lookup"><span data-stu-id="ce05b-129">When this property is enabled, promotions can be configured by using images, links, and text.</span></span> <span data-ttu-id="ce05b-130">Bu özellik, Commerce 10.0.17 sürümüne eklenmiştir.</span><span class="sxs-lookup"><span data-stu-id="ce05b-130">This property was added in the Commerce version 10.0.17 release.</span></span> |
| <span data-ttu-id="ce05b-131">Promosyon ekleme</span><span class="sxs-lookup"><span data-stu-id="ce05b-131">Add promotions</span></span> | <span data-ttu-id="ce05b-132">Metin görüntü veya bağlantı</span><span class="sxs-lookup"><span data-stu-id="ce05b-132">Text, image, or link</span></span> | <span data-ttu-id="ce05b-133">**Promosyonları göster** özelliği etkinleştirildiğinde, gezinti menüsünde promosyon içeriği olarak metin, görüntü veya bağlantı ekleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="ce05b-133">When the **Show promotions** property is enabled, you can add text, an image, or a link as promotional content on the navigation menu.</span></span> |
| <span data-ttu-id="ce05b-134">Çok düzeyli gezinti menüsünü etkinleştir</span><span class="sxs-lookup"><span data-stu-id="ce05b-134">Enable multi-level navigation menu</span></span> | <span data-ttu-id="ce05b-135">**Doğru** veya **yanlış**</span><span class="sxs-lookup"><span data-stu-id="ce05b-135">**True** or **False**</span></span> | <span data-ttu-id="ce05b-136">Bu özellik etkinleştirildiğinde, gezinti menüsü gezinti hiyerarşisinin birden çok düzeyini gösterebilir.</span><span class="sxs-lookup"><span data-stu-id="ce05b-136">When this property is enabled, the navigation menu can show multiple levels of the navigation hierarchy.</span></span> <span data-ttu-id="ce05b-137">Bu özellik Commerce 10.0.15 sürümünde bulunur.</span><span class="sxs-lookup"><span data-stu-id="ce05b-137">This feature is available in the Commerce version 10.0.15 release.</span></span> |
| <span data-ttu-id="ce05b-138">Düzey sayısı</span><span class="sxs-lookup"><span data-stu-id="ce05b-138">Number of levels</span></span> | <span data-ttu-id="ce05b-139">tamsayı</span><span class="sxs-lookup"><span data-stu-id="ce05b-139">integer</span></span> | <span data-ttu-id="ce05b-140">Bu özellik, **çok düzeyli gezinti menüsünü etkinleştir** özelliği **true** olarak ayarlandığında gösterilmesi gereken düzey sayısını tanımlar.</span><span class="sxs-lookup"><span data-stu-id="ce05b-140">This property defines the numbers of levels that should be shown if the **Enable multilevel navigation menu** property is set to **True**.</span></span> |
| <span data-ttu-id="ce05b-141">Statik menü öğesi</span><span class="sxs-lookup"><span data-stu-id="ce05b-141">Static menu item</span></span>| <span data-ttu-id="ce05b-142">Değerler dizisi</span><span class="sxs-lookup"><span data-stu-id="ce05b-142">Array of values</span></span>| <span data-ttu-id="ce05b-143">Bir menü öğesi adını statik site sayfasının bağlantısıyla ilişkilendiren statik menü öğeleri.</span><span class="sxs-lookup"><span data-stu-id="ce05b-143">Static menu items that associate a menu item name with a link to a static site page.</span></span> <span data-ttu-id="ce05b-144">Menü öğelerini diğer menü öğelerinin altında oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="ce05b-144">You can create menu items below other menu items.</span></span> <span data-ttu-id="ce05b-145">Varsayılan olarak, statik menüler kök düzeyinde görünür ve varsa kanal gezinme hiyerarşisine eklenir.</span><span class="sxs-lookup"><span data-stu-id="ce05b-145">By default, static menus appear at the root level and will be appended to the channel navigation hierarchy if it exists.</span></span> |
| <span data-ttu-id="ce05b-146">Kök menüyü göster</span><span class="sxs-lookup"><span data-stu-id="ce05b-146">Show root menu</span></span> | <span data-ttu-id="ce05b-147">**Doğru** veya **yanlış**</span><span class="sxs-lookup"><span data-stu-id="ce05b-147">**True** or **False**</span></span> | <span data-ttu-id="ce05b-148">Bu özellik etkinleştirildiğinde, gezinti menüsü özel bir kök altında tanımlanabilir (örneğin, **Şimdi alışveriş yap**).</span><span class="sxs-lookup"><span data-stu-id="ce05b-148">When this property is enabled, the navigation menu can be defined under a custom root (for example, **Shop now**).</span></span> <span data-ttu-id="ce05b-149">Bu özellik Dynamics 365 Commerce sürüm 10.0.15'de kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="ce05b-149">This feature is available in the Dynamics 365 Commerce 10.0.15 release.</span></span> |
| <span data-ttu-id="ce05b-150">Kök menü</span><span class="sxs-lookup"><span data-stu-id="ce05b-150">Root menu</span></span> | <span data-ttu-id="ce05b-151">dize</span><span class="sxs-lookup"><span data-stu-id="ce05b-151">string</span></span> | <span data-ttu-id="ce05b-152">Bu özellik, **kök menüyü göster** özelliği **true** olarak ayarlandığında özel bir köke ait metni tanımlamak için kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="ce05b-152">This property can be used to define text for a custom root if the **Show root menu** property is set to **True**.</span></span> |

<span data-ttu-id="ce05b-153">Aşağıdaki çizimde, Fabrikam sitesinin gezinti menüsünde görüntülenen kategori resmi örneği gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="ce05b-153">The following illustration shows an example of a category image displayed on the navigation menu for the Fabrikam site.</span></span>
<span data-ttu-id="ce05b-154">![Kategori resimlerine sahip bir gezinti menüsü modülü örneği](./media/ecommerce-categoryimages.PNG)</span><span class="sxs-lookup"><span data-stu-id="ce05b-154">![Example of a navigation meu module with category images](./media/ecommerce-categoryimages.PNG)</span></span>

## <a name="add-a-navigation-menu-module-to-a-header-module"></a><span data-ttu-id="ce05b-155">Üstbilgi modülüne gezinti menüsü modülü ekleme</span><span class="sxs-lookup"><span data-stu-id="ce05b-155">Add a navigation menu module to a header module</span></span>

<span data-ttu-id="ce05b-156">Bir üstbilgi modülüne gezinti menüsü modülü ekleme hakkında ayrıntılar için, bkz. [Üstbilgi modülü](author-header-module.md).</span><span class="sxs-lookup"><span data-stu-id="ce05b-156">For details about how to add a navigation menu module to a header module, see [Header module](author-header-module.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="ce05b-157">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="ce05b-157">Additional resources</span></span>

[<span data-ttu-id="ce05b-158">Modül kitaplığına genel bakış</span><span class="sxs-lookup"><span data-stu-id="ce05b-158">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="ce05b-159">İçerik haritası modülü</span><span class="sxs-lookup"><span data-stu-id="ce05b-159">Breadcrumb module</span></span>](add-breadcrumb.md)

[<span data-ttu-id="ce05b-160">Site seçicisi modülü</span><span class="sxs-lookup"><span data-stu-id="ce05b-160">Site selector module</span></span>](site-selector.md)

[<span data-ttu-id="ce05b-161">Satın alma kutusu modülü</span><span class="sxs-lookup"><span data-stu-id="ce05b-161">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="ce05b-162">Tanımlama bilgisi uyumluluğu</span><span class="sxs-lookup"><span data-stu-id="ce05b-162">Cookie compliance</span></span>](cookie-compliance.md)

[<span data-ttu-id="ce05b-163">Üst bilgi modülü</span><span class="sxs-lookup"><span data-stu-id="ce05b-163">Header module</span></span>](author-header-module.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]