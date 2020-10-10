---
title: Gezinti menüsü modülleri
description: Bu konu gezinti menüsü modüllerini kapsamaktadır ve Microsoft Dynamics 365 Commerce'un site sayfalarına nasıl ekleneceğini açıklamaktadır.
author: anupamar-ms
manager: annbe
ms.date: 09/15/2020
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
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: 91239bd1db3f5819b7ad8d45ccfd8ab0d88b1b41
ms.sourcegitcommit: 8028fbc5b9585e87d3331ea02577ff82ede090af
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/16/2020
ms.locfileid: "3817886"
---
# <a name="navigation-menu-module"></a><span data-ttu-id="ae1a5-103">Gezinti menüsü modülleri</span><span class="sxs-lookup"><span data-stu-id="ae1a5-103">Navigation menu module</span></span>

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

<span data-ttu-id="ae1a5-104">Bu konu gezinti menüsü modüllerini kapsamaktadır ve Microsoft Dynamics 365 Commerce'un site sayfalarına nasıl ekleneceğini açıklamaktadır.</span><span class="sxs-lookup"><span data-stu-id="ae1a5-104">This topic covers navigation menu modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="ae1a5-105">Genel bakış</span><span class="sxs-lookup"><span data-stu-id="ae1a5-105">Overview</span></span>

<span data-ttu-id="ae1a5-106">Gezinti menüsü modüllerinin başlıca amacı, site kullanıcılarının Dynamics 365 Commerce yönetim merkezinde tanımlanan kanal gezinti hiyerarşisine göre ürün ve site sayfalarına göz atmasına olanak sağlamaktır.</span><span class="sxs-lookup"><span data-stu-id="ae1a5-106">The primary purpose of navigation menu modules is to allow site users to browse products and site pages according to the channel navigation hierarchy defined in Dynamics 365 Commerce headquarters.</span></span> <span data-ttu-id="ae1a5-107">Bir gezinti menüsü modülünde yapılandırılan öğeler site üstbilgisi gezintisi olarak görünür.</span><span class="sxs-lookup"><span data-stu-id="ae1a5-107">Items configured in a navigation menu module appear as site header navigation.</span></span> <span data-ttu-id="ae1a5-108">Gezinti menüsü modülleri, bir e-ticaret sitesindeki diğer sayfalara bağlantı sağlayan statik menü öğelerini de destekler.</span><span class="sxs-lookup"><span data-stu-id="ae1a5-108">Navigation menu modules also support static menu items that link to other pages on an e-Commerce site.</span></span>

<span data-ttu-id="ae1a5-109">Gezinti menüsü modülü bir sayfanın üst bilgi modülüne eklenebilir.</span><span class="sxs-lookup"><span data-stu-id="ae1a5-109">The navigation menu module can be added to the header module of a page.</span></span> <span data-ttu-id="ae1a5-110">Fabrikam temasında, gezinti menüsü varsayılan olarak iki düzey gösterir.</span><span class="sxs-lookup"><span data-stu-id="ae1a5-110">In the Fabrikam theme, the navigation menu shows two levels by default.</span></span> <span data-ttu-id="ae1a5-111">Starter temasında, gezinti menüsü varsayılan olarak üç düzey gösterir.</span><span class="sxs-lookup"><span data-stu-id="ae1a5-111">In the Starter theme, the navigation menu shows three levels by default.</span></span> <span data-ttu-id="ae1a5-112">Düzey sayısını değiştirmek için temada bir görünüm uzantısı gereklidir.</span><span class="sxs-lookup"><span data-stu-id="ae1a5-112">To change to the number of levels, a view extension is required on the theme.</span></span>

<span data-ttu-id="ae1a5-113">Aşağıdaki çizimde, iki düzey kategori hiyerarşisi ve bazı statik menü öğeleri bulunan Fabrikam sitesi için bir gezinti menüsü örneği gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="ae1a5-113">The following illustration shows an example of a navigation menu for the Fabrikam site with two levels of category hierarchy and some static menu items.</span></span>
<span data-ttu-id="ae1a5-114">![Gezinti menüsü modülü örneği](./media/ecommerce-header.png)</span><span class="sxs-lookup"><span data-stu-id="ae1a5-114">![Example of a navigation meu module](./media/ecommerce-header.png)</span></span>

## <a name="navigation-menu-module-properties"></a><span data-ttu-id="ae1a5-115">Gezinti menüsü modüllerinin özellikleri</span><span class="sxs-lookup"><span data-stu-id="ae1a5-115">Navigation menu module properties</span></span>

| <span data-ttu-id="ae1a5-116">Özellik adı</span><span class="sxs-lookup"><span data-stu-id="ae1a5-116">Property name</span></span>             | <span data-ttu-id="ae1a5-117">Değer</span><span class="sxs-lookup"><span data-stu-id="ae1a5-117">Value</span></span>                 | <span data-ttu-id="ae1a5-118">Tanım</span><span class="sxs-lookup"><span data-stu-id="ae1a5-118">Description</span></span> |
|---------------------------|-----------------------|-------------|
| <span data-ttu-id="ae1a5-119">Kaynak</span><span class="sxs-lookup"><span data-stu-id="ae1a5-119">Source</span></span>                  | <span data-ttu-id="ae1a5-120">**Perakende**, **El ile yazma**, **Perakende ve el ile yazma**</span><span class="sxs-lookup"><span data-stu-id="ae1a5-120">**Retail**, **Manual authoring**, **Retail and manual authoring**</span></span> | <span data-ttu-id="ae1a5-121">**Perakende** değeri, Commerce yönetim merkezinde kanal gezinme hiyerarşisinin gezinti menüsünde görüntülenmesini sağlar.</span><span class="sxs-lookup"><span data-stu-id="ae1a5-121">The **Retail** value allows the channel navigation hierarchy from Commerce headquarters to be displayed on the navigation menu.</span></span> <span data-ttu-id="ae1a5-122">**El ile yazma** değeri statik menü öğelerinin oluşturulmasına izin verir.</span><span class="sxs-lookup"><span data-stu-id="ae1a5-122">The **Manual authoring** value allows static menu items to be curated.</span></span> <span data-ttu-id="ae1a5-123">**Perakende ve el ile yazma** değeri, her ikisinin karışımına izin verir.</span><span class="sxs-lookup"><span data-stu-id="ae1a5-123">The **Retail and manual authoring** value allows a mix of both.</span></span> |
| <span data-ttu-id="ae1a5-124">Kategori resimlerini göster</span><span class="sxs-lookup"><span data-stu-id="ae1a5-124">Show category images</span></span> | <span data-ttu-id="ae1a5-125">**Doğru** veya **yanlış**</span><span class="sxs-lookup"><span data-stu-id="ae1a5-125">**True** or **False**</span></span>    | <span data-ttu-id="ae1a5-126">Etkinleştirildiğinde, bu özellik gezinti menüsündeki kategori resimlerini her kategori için Commerce yönetim merkezinde tanımlandığı şekilde görüntüler.</span><span class="sxs-lookup"><span data-stu-id="ae1a5-126">When enabled, this property displays category images on the navigation menu as defined in Commerce headquarters for each category.</span></span> <span data-ttu-id="ae1a5-127">Commerce sürüm 10.0.14'e eklendi.</span><span class="sxs-lookup"><span data-stu-id="ae1a5-127">Added in Commerce release 10.0.14.</span></span> |
| <span data-ttu-id="ae1a5-128">Statik menü öğesi</span><span class="sxs-lookup"><span data-stu-id="ae1a5-128">Static menu item</span></span>| <span data-ttu-id="ae1a5-129">Değerler dizisi</span><span class="sxs-lookup"><span data-stu-id="ae1a5-129">Array of values</span></span>| <span data-ttu-id="ae1a5-130">Bir menü öğesi adını statik site sayfasının bağlantısıyla ilişkilendiren statik menü öğeleri.</span><span class="sxs-lookup"><span data-stu-id="ae1a5-130">Static menu items that associate a menu item name with a link to a static site page.</span></span> <span data-ttu-id="ae1a5-131">Menü öğelerini diğer menü öğelerinin altında oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="ae1a5-131">You can create menu items below other menu items.</span></span> <span data-ttu-id="ae1a5-132">Varsayılan olarak, statik menüler kök düzeyinde görünür ve varsa kanal gezinme hiyerarşisine eklenir.</span><span class="sxs-lookup"><span data-stu-id="ae1a5-132">By default, static menus appear at the root level and will be appended to the channel navigation hierarchy if it exists.</span></span> |

<span data-ttu-id="ae1a5-133">Aşağıdaki çizimde, Fabrikam sitesinin gezinti menüsünde görüntülenen kategori resmi örneği gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="ae1a5-133">The following illustration shows an example of a category image displayed on the navigation menu for the Fabrikam site.</span></span>
<span data-ttu-id="ae1a5-134">![Kategori resimlerine sahip bir gezinti menüsü modülü örneği](./media/ecommerce-categoryimages.PNG)</span><span class="sxs-lookup"><span data-stu-id="ae1a5-134">![Example of a navigation meu module with category images](./media/ecommerce-categoryimages.PNG)</span></span>

## <a name="add-a-navigation-menu-module-to-a-header-module"></a><span data-ttu-id="ae1a5-135">Üstbilgi modülüne gezinti menüsü modülü ekleme</span><span class="sxs-lookup"><span data-stu-id="ae1a5-135">Add a navigation menu module to a header module</span></span>

<span data-ttu-id="ae1a5-136">Bir üstbilgi modülüne gezinti menüsü modülü ekleme hakkında ayrıntılar için, bkz. [Üstbilgi modülü](author-header-module.md).</span><span class="sxs-lookup"><span data-stu-id="ae1a5-136">For details about how to add a navigation menu module to a header module, see [Header module](author-header-module.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="ae1a5-137">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="ae1a5-137">Additional resources</span></span>

[<span data-ttu-id="ae1a5-138">Modül kitaplığına genel bakış</span><span class="sxs-lookup"><span data-stu-id="ae1a5-138">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="ae1a5-139">Satın alma kutusu modülü</span><span class="sxs-lookup"><span data-stu-id="ae1a5-139">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="ae1a5-140">Tanımlama bilgisi uyumluluğu</span><span class="sxs-lookup"><span data-stu-id="ae1a5-140">Cookie compliance</span></span>](cookie-compliance.md)

[<span data-ttu-id="ae1a5-141">Üst bilgi modülü</span><span class="sxs-lookup"><span data-stu-id="ae1a5-141">Header module</span></span>](author-header-module.md)
