---
title: Site gezintisini özelleştirme
description: Bu konu, Microsoft Dynamics 365 Commerce sitenizde gezinmek üzere ürünlerinizi düzenlemek için özelleştirilmiş bir çevrimiçi gezinti hiyerarşisinin nasıl oluşturulacağını açıklamaktadır.
author: bicyclingfool
manager: annbe
ms.date: 12/12/2019
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
ms.author: StuHarg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: c2235510c7ef386d66fe3b137f8e791d14706379
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/01/2020
ms.locfileid: "3001841"
---
# <a name="customize-site-navigation"></a><span data-ttu-id="371ba-103">Site gezintisini özelleştirme</span><span class="sxs-lookup"><span data-stu-id="371ba-103">Customize site navigation</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="371ba-104">Bu konu, Microsoft Dynamics 365 Commerce sitenizde gezinmek üzere ürünlerinizi düzenlemek için özelleştirilmiş bir çevrimiçi gezinti hiyerarşisinin nasıl oluşturulacağını açıklamaktadır.</span><span class="sxs-lookup"><span data-stu-id="371ba-104">This topic describes how to create a customized online navigation hierarchy to organize your products for browsing on your Microsoft Dynamics 365 Commerce site.</span></span>

## <a name="overview"></a><span data-ttu-id="371ba-105">Genel Bakış</span><span class="sxs-lookup"><span data-stu-id="371ba-105">Overview</span></span>

<span data-ttu-id="371ba-106">Çevrimiçi mağazalar, genel olarak ürün kategorilerine giderek gezinerek ürünlere keşif ve göz atma sağlar.</span><span class="sxs-lookup"><span data-stu-id="371ba-106">Online storefronts typically let customers discover and browse products by navigating through product categories.</span></span> <span data-ttu-id="371ba-107">Bu özellik genellikle sayfanın üst kısmındaki sekmeler veya soldaki bir gezinti çubuğu ile sağlanır.</span><span class="sxs-lookup"><span data-stu-id="371ba-107">This capability is usually provided by tabs at the top of the page or by a navigation bar on the left.</span></span> <span data-ttu-id="371ba-108">Dynamics 365 Commerce'te, kategori gezinimin hiyerarşik yapısını ve çeşitli kategorilerde bulunan ürünleri oluşturabilir ve yönetebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="371ba-108">In Dynamics 365 Commerce, you can create and manage the hierarchal structure of your category navigation and the products that are included in the various categories.</span></span>

## <a name="create-a-channel-navigation-hierarchy"></a><span data-ttu-id="371ba-109">Kanal gezinme hiyerarşisi oluşturma</span><span class="sxs-lookup"><span data-stu-id="371ba-109">Create a channel navigation hierarchy</span></span>

<span data-ttu-id="371ba-110">Kanal gezinti hiyerarşisi oluşturmak için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="371ba-110">To create a channel navigation hierarchy, follow these steps.</span></span>

1. <span data-ttu-id="371ba-111">**Retail and Commerce \> Ürünler ve kategoriler \> Kategori ve ürün yönetimi**'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="371ba-111">Go to **Retail and Commerce \> Products and categories \> Category and product management**.</span></span>
1. <span data-ttu-id="371ba-112">**Kategori hiyerarşileri** ve ardından **Yeni**yi seçin.</span><span class="sxs-lookup"><span data-stu-id="371ba-112">Select **Category hierarchies**, and then select **New**.</span></span>
1. <span data-ttu-id="371ba-113">Hiyerarşiyi adlandırın.</span><span class="sxs-lookup"><span data-stu-id="371ba-113">Name the hierarchy.</span></span>

    > [!NOTE]
    > <span data-ttu-id="371ba-114">Oluşturduğunuz en üstteki kategori kök kategori düğümüdür.</span><span class="sxs-lookup"><span data-stu-id="371ba-114">The topmost category that you create is the root category node.</span></span> <span data-ttu-id="371ba-115">Sitenizde gösterilmez.</span><span class="sxs-lookup"><span data-stu-id="371ba-115">It won't be shown on your site.</span></span> <span data-ttu-id="371ba-116">Sitenizde tek bir üst düzey düğümün gösterildiği bir kategori hiyerarşisi oluşturmak için, kategoriyi kök kategorinin alt öğesi olarak oluşturun ve adlandırın.</span><span class="sxs-lookup"><span data-stu-id="371ba-116">To create a category hierarchy where a single top-level node is shown on your site, create and name the category as a child of the root category.</span></span>

1. <span data-ttu-id="371ba-117">**Yeni kategori düğümünü** seçin ve kategoriyi adlandırın.</span><span class="sxs-lookup"><span data-stu-id="371ba-117">Select **New category node**, and name the category.</span></span>
1. <span data-ttu-id="371ba-118">Gereksinim duyduğunuz şekilde kardeş ve alt kategori oluşturmaya devam edin.</span><span class="sxs-lookup"><span data-stu-id="371ba-118">Continue to create sibling and child categories as you require.</span></span>

<span data-ttu-id="371ba-119">Artık, en üst düzey kategori altında oluşturduğunuz her bir kategoriye ürün atayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="371ba-119">You can now assign products to each category that you created under the top-level category.</span></span>

## <a name="customize-the-order-of-categories"></a><span data-ttu-id="371ba-120">Kategorilerin sırasını özelleştirme</span><span class="sxs-lookup"><span data-stu-id="371ba-120">Customize the order of categories</span></span>

<span data-ttu-id="371ba-121">Varsayılan olarak tanımladığınız Kategoriler sitenizde alfabetik sırada görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="371ba-121">By default, the categories that you define will appear in alphabetical order on your site.</span></span> <span data-ttu-id="371ba-122">Ancak, kategorilerin görüntülenme sırasını da özelleştirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="371ba-122">However, you can also customize the display order of categories.</span></span>

## <a name="assign-a-category-hierarchy-type"></a><span data-ttu-id="371ba-123">Kategori hiyerarşisi türü atayın</span><span class="sxs-lookup"><span data-stu-id="371ba-123">Assign a category hierarchy type</span></span>

1. <span data-ttu-id="371ba-124">**Retail and Commerce \> Ürünler ve kategoriler \> Kategori ve ürün yönetimi**'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="371ba-124">Go to **Retail and Commerce \> Products and categories \> Category and product management**.</span></span>
1. <span data-ttu-id="371ba-125">**Kategori hiyerarşileri** seçin.</span><span class="sxs-lookup"><span data-stu-id="371ba-125">Select **Category hierarchies**.</span></span>
1. <span data-ttu-id="371ba-126">Ardından Eylem Bölmesinde, **kategori hiyerarşisi** sekmesindeki **Ayar** gurubunda **Hiyerarşi türünü ilişkilendir**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="371ba-126">On the Action Pane, on the **Category hierarchy** tab, in the **Set up** group, select **Associate hierarchy type**.</span></span>
1. <span data-ttu-id="371ba-127">**Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="371ba-127">Select **New**.</span></span>
1. <span data-ttu-id="371ba-128">**Kategori hiyerarşisi türü** alanında, **Kanal gezinme hiyerarşisi**'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="371ba-128">In the **Category hierarchy type** field, select **Channel navigation hierarchy**.</span></span>
1. <span data-ttu-id="371ba-129">**Kategori hiyerarşisi** alanında, daha önce oluşturduğunuz kanal gezinme hiyerarşisini seçin.</span><span class="sxs-lookup"><span data-stu-id="371ba-129">In the **Category hierarchy** field, select the channel navigation hierarchy that you created earlier.</span></span>

## <a name="publish-new-or-updated-navigation-hierarchies"></a><span data-ttu-id="371ba-130">Yeni veya güncelleştirilmiş gezinti hiyerarşileri Yayımla</span><span class="sxs-lookup"><span data-stu-id="371ba-130">Publish new or updated navigation hierarchies</span></span>

<span data-ttu-id="371ba-131">Gezinti hiyerarşinizi çevrimiçi mağaza için kullanılabilir hale getirmek için, aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="371ba-131">To make your navigation hierarchy available to your online storefront, follow these steps.</span></span>

1. <span data-ttu-id="371ba-132">**Retail and Commerce \> Kanal Kurulumu \> Kanal kategorileri ve ürün öznitelikleri**'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="371ba-132">Go to **Retail and Commerce \> Channel setup \> Channel categories and product attributes**.</span></span>
1. <span data-ttu-id="371ba-133">Soldaki ağaçta, çevrimiçi mağazayı seçin.</span><span class="sxs-lookup"><span data-stu-id="371ba-133">In the tree on the left, select your online store.</span></span>
1. <span data-ttu-id="371ba-134">**Kanal güncelleştirmelerini yayınla**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="371ba-134">Select **Publish channel updates**.</span></span>
1. <span data-ttu-id="371ba-135">**Retail and Commerce \> Retail and Commerce IT \> Dağıtım planı**'na gidin.</span><span class="sxs-lookup"><span data-stu-id="371ba-135">Go to **Retail and Commerce \> Retail and Commerce IT \> Distribution schedule**.</span></span>
1. <span data-ttu-id="371ba-136">Listede, **İş 1040** kodlu bulun ve seçin</span><span class="sxs-lookup"><span data-stu-id="371ba-136">In the list, find and select **Job 1040**.</span></span>
1. <span data-ttu-id="371ba-137">**Şimdi Çalıştır**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="371ba-137">Select **Run now**.</span></span>
1. <span data-ttu-id="371ba-138">1070 ve 1150 işleri için 5 ve 6 numaralı adımları yineleyin.</span><span class="sxs-lookup"><span data-stu-id="371ba-138">Repeat steps 5 and 6 for jobs 1070 and 1150.</span></span>

## <a name="show-categories-on-your-site"></a><span data-ttu-id="371ba-139">Sitenizde kategorileri gösterin</span><span class="sxs-lookup"><span data-stu-id="371ba-139">Show categories on your site</span></span>

<span data-ttu-id="371ba-140">Kategori hiyerarşinizi çevrimiçi mağazada göstermek için, şablon veya parçadaki uygun konuma gezinti menüsü modülünü eklemeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="371ba-140">To show your category hierarchy on your online storefront, you must add the navigation menu module in the appropriate location in a template or fragment.</span></span> <span data-ttu-id="371ba-141">Daha sonra gezinti menü modülü, sitenizin bağlı olduğu kanala gezinti hiyerarşinizi yayımladığınızda, gezinti hiyerarşinizi gösterecektir.</span><span class="sxs-lookup"><span data-stu-id="371ba-141">The navigation menu module will then show your navigation hierarchy, provided that you've published your navigation hierarchy to the channel that your site is bound to.</span></span>

> [!NOTE]
> <span data-ttu-id="371ba-142">Mağaza başlangıç setinde bulunan gezinti menü modülü, kullanıcıların yalnızca alt kategorileri olmayan kategorilere gitmesine izin verir.</span><span class="sxs-lookup"><span data-stu-id="371ba-142">The navigation menu module that is included in the store starter kit lets users navigate only to categories that don't have subcategories.</span></span> <span data-ttu-id="371ba-143">Müşterilerinizin alt kategorileri olan kategorilere gidebilmesi gerekiyorsa, gezinti menü modülünü özelleştirmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="371ba-143">If your customers should be able to navigate to categories that have subcategories, you must customize the navigation menu module.</span></span>

## <a name="add-custom-navigation-options"></a><span data-ttu-id="371ba-144">Özel gezinti seçenekleri ekle</span><span class="sxs-lookup"><span data-stu-id="371ba-144">Add custom navigation options</span></span>

<span data-ttu-id="371ba-145">Gezinti menünüze, ürün kategori hiyerarşinizin parçası olmayan gezinme seçenekleri ekleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="371ba-145">On your navigation menu, you can add navigation options that aren't part of your product category hierarchy.</span></span> <span data-ttu-id="371ba-146">Örneğin, ürün kategorileri listesinin sonunda, siteniz için oluşturduğunuz bir kişi sayfasına işaret eden **bize ulaşın** öğesi ekleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="371ba-146">For example, at the end of the list of product categories, you can add a **Contact Us** item that points to a contact page that you've built for your site.</span></span>

<span data-ttu-id="371ba-147">Gezinti menünüze özel gezinti seçenekleri eklemek için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="371ba-147">To add custom navigation options to your navigation menu, follow these steps.</span></span>

1. <span data-ttu-id="371ba-148">Özelleştirmek istediğiniz şablonda veya parçada gezinti menü modülünü seçin.</span><span class="sxs-lookup"><span data-stu-id="371ba-148">In the template or fragment that you want to customize, select the navigation menu module.</span></span>
1. <span data-ttu-id="371ba-149">Özellik bölmesinde, **veri** sekmesinde, yeni bir içerik yönetim sistemi (CMS) gezinti öğesi oluşturmak için **Öğe ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="371ba-149">In the property pane, on the **Data** tab, select **Add item** to create a new content management system (CMS) navigation item.</span></span>
1. <span data-ttu-id="371ba-150">Bağlantı metnini ve URL'yi girin.</span><span class="sxs-lookup"><span data-stu-id="371ba-150">Enter link text and a URL.</span></span>
1. <span data-ttu-id="371ba-151">Daha fazla özel gezinti seçeneği eklemek için 2 ve 3. adımları tekrarlayın.</span><span class="sxs-lookup"><span data-stu-id="371ba-151">Repeat steps 2 and 3 to add more custom navigation options.</span></span>
1. <span data-ttu-id="371ba-152">Bitirdiğinizde, şablonu veya parçayı kaydedin ve iade edin.</span><span class="sxs-lookup"><span data-stu-id="371ba-152">When you've finished, save the template or fragment, and check it in.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="371ba-153">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="371ba-153">Additional resources</span></span>

[<span data-ttu-id="371ba-154">Şablonlar ve düzenlere genel bakış</span><span class="sxs-lookup"><span data-stu-id="371ba-154">Templates and layouts overview</span></span>](templates-layouts-overview.md)

[<span data-ttu-id="371ba-155">Şablonlarla çalışma</span><span class="sxs-lookup"><span data-stu-id="371ba-155">Work with templates</span></span>](work-with-templates.md)

[<span data-ttu-id="371ba-156">Önceden ayarlanmış düzenlerle çalışma</span><span class="sxs-lookup"><span data-stu-id="371ba-156">Work with preset layouts</span></span>](work-with-layouts.md)

[<span data-ttu-id="371ba-157">Parçalarla çalışma</span><span class="sxs-lookup"><span data-stu-id="371ba-157">Work with fragments</span></span>](work-with-fragments.md)

[<span data-ttu-id="371ba-158">Modüllerle çalışma</span><span class="sxs-lookup"><span data-stu-id="371ba-158">Work with modules</span></span>](work-with-modules.md)

[<span data-ttu-id="371ba-159">Sayfa URL'si oluşturma</span><span class="sxs-lookup"><span data-stu-id="371ba-159">Create a page URL</span></span>](create-page-url.md)

[<span data-ttu-id="371ba-160">Yayınlama gruplarıyla çalışma</span><span class="sxs-lookup"><span data-stu-id="371ba-160">Work with publish groups</span></span>](publish-groups.md)
