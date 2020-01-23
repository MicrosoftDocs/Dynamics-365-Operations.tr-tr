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
ms.openlocfilehash: 642cb5c145dec68631eb9ab27d926ba8ab75c59b
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 12/20/2019
ms.locfileid: "2914922"
---
# <a name="customize-site-navigation"></a><span data-ttu-id="79b60-103">Site gezintisini özelleştirme</span><span class="sxs-lookup"><span data-stu-id="79b60-103">Customize site navigation</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="79b60-104">Bu konu, Microsoft Dynamics 365 Commerce sitenizde gezinmek üzere ürünlerinizi düzenlemek için özelleştirilmiş bir çevrimiçi gezinti hiyerarşisinin nasıl oluşturulacağını açıklamaktadır.</span><span class="sxs-lookup"><span data-stu-id="79b60-104">This topic describes how to create a customized online navigation hierarchy to organize your products for browsing on your Microsoft Dynamics 365 Commerce site.</span></span>

## <a name="overview"></a><span data-ttu-id="79b60-105">Genel Bakış</span><span class="sxs-lookup"><span data-stu-id="79b60-105">Overview</span></span>

<span data-ttu-id="79b60-106">Çevrimiçi mağazalar, genel olarak ürün kategorilerine giderek gezinerek ürünlere keşif ve göz atma sağlar.</span><span class="sxs-lookup"><span data-stu-id="79b60-106">Online storefronts typically let customers discover and browse products by navigating through product categories.</span></span> <span data-ttu-id="79b60-107">Bu özellik genellikle sayfanın üst kısmındaki sekmeler veya soldaki bir gezinti çubuğu ile sağlanır.</span><span class="sxs-lookup"><span data-stu-id="79b60-107">This capability is usually provided by tabs at the top of the page or by a navigation bar on the left.</span></span> <span data-ttu-id="79b60-108">Dynamics 365 Commerce'te, kategori gezinimin hiyerarşik yapısını ve çeşitli kategorilerde bulunan ürünleri oluşturabilir ve yönetebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="79b60-108">In Dynamics 365 Commerce, you can create and manage the hierarchal structure of your category navigation and the products that are included in the various categories.</span></span>

## <a name="create-a-retail-channel-navigation-hierarchy"></a><span data-ttu-id="79b60-109">Perakende kanalı gezinme hiyerarşisi oluştur</span><span class="sxs-lookup"><span data-stu-id="79b60-109">Create a retail channel navigation hierarchy</span></span>

<span data-ttu-id="79b60-110">Perakende kanalı gezinti hiyerarşisi oluşturmak için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="79b60-110">To create a retail channel navigation hierarchy, follow these steps.</span></span>

1. <span data-ttu-id="79b60-111">**Perakende \> Ürünler ve kategoriler \> Kategori ve ürün yönetimi**'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="79b60-111">Go to **Retail \> Products and categories \> Category and product management**.</span></span>
1. <span data-ttu-id="79b60-112">**Kategori hiyerarşileri** ve ardından **Yeni**yi seçin.</span><span class="sxs-lookup"><span data-stu-id="79b60-112">Select **Category hierarchies**, and then select **New**.</span></span>
1. <span data-ttu-id="79b60-113">Hiyerarşiyi adlandırın.</span><span class="sxs-lookup"><span data-stu-id="79b60-113">Name the hierarchy.</span></span>

    > [!NOTE]
    > <span data-ttu-id="79b60-114">Oluşturduğunuz en üstteki kategori kök kategori düğümüdür.</span><span class="sxs-lookup"><span data-stu-id="79b60-114">The topmost category that you create is the root category node.</span></span> <span data-ttu-id="79b60-115">Sitenizde gösterilmez.</span><span class="sxs-lookup"><span data-stu-id="79b60-115">It won't be shown on your site.</span></span> <span data-ttu-id="79b60-116">Sitenizde tek bir üst düzey düğümün gösterildiği bir kategori hiyerarşisi oluşturmak için, kategoriyi kök kategorinin alt öğesi olarak oluşturun ve adlandırın.</span><span class="sxs-lookup"><span data-stu-id="79b60-116">To create a category hierarchy where a single top-level node is shown on your site, create and name the category as a child of the root category.</span></span>

1. <span data-ttu-id="79b60-117">**Yeni kategori düğümünü** seçin ve kategoriyi adlandırın.</span><span class="sxs-lookup"><span data-stu-id="79b60-117">Select **New category node**, and name the category.</span></span>
1. <span data-ttu-id="79b60-118">Gereksinim duyduğunuz şekilde kardeş ve alt kategori oluşturmaya devam edin.</span><span class="sxs-lookup"><span data-stu-id="79b60-118">Continue to create sibling and child categories as you require.</span></span>

<span data-ttu-id="79b60-119">Artık, en üst düzey kategori altında oluşturduğunuz her bir kategoriye ürün atayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="79b60-119">You can now assign products to each category that you created under the top-level category.</span></span>

## <a name="customize-the-order-of-categories"></a><span data-ttu-id="79b60-120">Kategorilerin sırasını özelleştirme</span><span class="sxs-lookup"><span data-stu-id="79b60-120">Customize the order of categories</span></span>

<span data-ttu-id="79b60-121">Varsayılan olarak tanımladığınız Kategoriler sitenizde alfabetik sırada görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="79b60-121">By default, the categories that you define will appear in alphabetical order on your site.</span></span> <span data-ttu-id="79b60-122">Ancak, kategorilerin görüntülenme sırasını da özelleştirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="79b60-122">However, you can also customize the display order of categories.</span></span>

## <a name="assign-a-category-hierarchy-type"></a><span data-ttu-id="79b60-123">Kategori hiyerarşisi türü atayın</span><span class="sxs-lookup"><span data-stu-id="79b60-123">Assign a category hierarchy type</span></span>

1. <span data-ttu-id="79b60-124">**Perakende \> Ürünler ve kategoriler \> Kategori ve ürün yönetimi**'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="79b60-124">Go to **Retail \> Products and categories \> Category and product management**.</span></span>
1. <span data-ttu-id="79b60-125">**Kategori hiyerarşileri** seçin.</span><span class="sxs-lookup"><span data-stu-id="79b60-125">Select **Category hierarchies**.</span></span>
1. <span data-ttu-id="79b60-126">Ardından Eylem Bölmesinde, **kategori hiyerarşisi** sekmesindeki **Ayar** gurubunda **Hiyerarşi türünü ilişkilendir**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="79b60-126">On the Action Pane, on the **Category hierarchy** tab, in the **Set up** group, select **Associate hierarchy type**.</span></span>
1. <span data-ttu-id="79b60-127">**Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="79b60-127">Select **New**.</span></span>
1. <span data-ttu-id="79b60-128">**Kategori hiyerarşisi türü** alanında **Perakende kanalı gezinme hiyerarşisi** seçin.</span><span class="sxs-lookup"><span data-stu-id="79b60-128">In the **Category hierarchy type** field, select **Retail channel navigation hierarchy**.</span></span>
1. <span data-ttu-id="79b60-129">**Kategori hiyerarşisi** alanında, daha önce oluşturduğunuz kanal gezinme hiyerarşisini seçin.</span><span class="sxs-lookup"><span data-stu-id="79b60-129">In the **Category hierarchy** field, select the channel navigation hierarchy that you created earlier.</span></span>

## <a name="publish-new-or-updated-navigation-hierarchies"></a><span data-ttu-id="79b60-130">Yeni veya güncelleştirilmiş gezinti hiyerarşileri Yayımla</span><span class="sxs-lookup"><span data-stu-id="79b60-130">Publish new or updated navigation hierarchies</span></span>

<span data-ttu-id="79b60-131">Gezinti hiyerarşinizi çevrimiçi mağaza için kullanılabilir hale getirmek için, aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="79b60-131">To make your navigation hierarchy available to your online storefront, follow these steps.</span></span>

1. <span data-ttu-id="79b60-132">**Perakende \> Kanal Kurulumu \> Kanal kategorileri ve ürün nitelikleri** seçeneğine gidin.</span><span class="sxs-lookup"><span data-stu-id="79b60-132">Go to **Retail \> Channel setup \> Channel categories and product attributes**.</span></span>
1. <span data-ttu-id="79b60-133">Soldaki ağaçta, çevrimiçi mağazayı seçin.</span><span class="sxs-lookup"><span data-stu-id="79b60-133">In the tree on the left, select your online store.</span></span>
1. <span data-ttu-id="79b60-134">**Kanal güncelleştirmelerini yayınla**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="79b60-134">Select **Publish channel updates**.</span></span>
1. <span data-ttu-id="79b60-135">**Perakende \> Perakende BT \> Dağıtım planı öğesine** gidin.</span><span class="sxs-lookup"><span data-stu-id="79b60-135">Go to **Retail \> Retail IT \> Distribution schedule**.</span></span>
1. <span data-ttu-id="79b60-136">Listede, **İş 1040** kodlu bulun ve seçin</span><span class="sxs-lookup"><span data-stu-id="79b60-136">In the list, find and select **Job 1040**.</span></span>
1. <span data-ttu-id="79b60-137">**Şimdi Çalıştır**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="79b60-137">Select **Run now**.</span></span>
1. <span data-ttu-id="79b60-138">1070 ve 1150 işleri için 5 ve 6 numaralı adımları yineleyin.</span><span class="sxs-lookup"><span data-stu-id="79b60-138">Repeat steps 5 and 6 for jobs 1070 and 1150.</span></span>

## <a name="show-categories-on-your-site"></a><span data-ttu-id="79b60-139">Sitenizde kategorileri gösterin</span><span class="sxs-lookup"><span data-stu-id="79b60-139">Show categories on your site</span></span>

<span data-ttu-id="79b60-140">Kategori hiyerarşinizi çevrimiçi mağazada göstermek için, şablon veya parçadaki uygun konuma gezinti menüsü modülünü eklemeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="79b60-140">To show your category hierarchy on your online storefront, you must add the navigation menu module in the appropriate location in a template or fragment.</span></span> <span data-ttu-id="79b60-141">Daha sonra gezinti menü modülü, sitenizin bağlı olduğu kanala perakende gezinti hiyerarşinizi yayımladığınızda, gezinti hiyerarşinizi gösterecektir.</span><span class="sxs-lookup"><span data-stu-id="79b60-141">The navigation menu module will then show your navigation hierarchy, provided that you've published your retail navigation hierarchy to the channel that your site is bound to.</span></span>

> [!NOTE]
> <span data-ttu-id="79b60-142">Mağaza başlangıç setinde bulunan gezinti menü modülü, kullanıcıların yalnızca alt kategorileri olmayan kategorilere gitmesine izin verir.</span><span class="sxs-lookup"><span data-stu-id="79b60-142">The navigation menu module that is included in the store starter kit lets users navigate only to categories that don't have subcategories.</span></span> <span data-ttu-id="79b60-143">Müşterilerinizin alt kategorileri olan kategorilere gidebilmesi gerekiyorsa, gezinti menü modülünü özelleştirmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="79b60-143">If your customers should be able to navigate to categories that have subcategories, you must customize the navigation menu module.</span></span>

## <a name="add-custom-navigation-options"></a><span data-ttu-id="79b60-144">Özel gezinti seçenekleri ekle</span><span class="sxs-lookup"><span data-stu-id="79b60-144">Add custom navigation options</span></span>

<span data-ttu-id="79b60-145">Gezinti menünüze, ürün kategori hiyerarşinizin parçası olmayan gezinme seçenekleri ekleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="79b60-145">On your navigation menu, you can add navigation options that aren't part of your product category hierarchy.</span></span> <span data-ttu-id="79b60-146">Örneğin, ürün kategorileri listesinin sonunda, siteniz için oluşturduğunuz bir kişi sayfasına işaret eden **bize ulaşın** öğesi ekleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="79b60-146">For example, at the end of the list of product categories, you can add a **Contact Us** item that points to a contact page that you've built for your site.</span></span>

<span data-ttu-id="79b60-147">Gezinti menünüze özel gezinti seçenekleri eklemek için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="79b60-147">To add custom navigation options to your navigation menu, follow these steps.</span></span>

1. <span data-ttu-id="79b60-148">Özelleştirmek istediğiniz şablonda veya parçada gezinti menü modülünü seçin.</span><span class="sxs-lookup"><span data-stu-id="79b60-148">In the template or fragment that you want to customize, select the navigation menu module.</span></span>
1. <span data-ttu-id="79b60-149">Özellik bölmesinde, **veri** sekmesinde, yeni bir içerik yönetim sistemi (CMS) gezinti öğesi oluşturmak için **Öğe ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="79b60-149">In the property pane, on the **Data** tab, select **Add item** to create a new content management system (CMS) navigation item.</span></span>
1. <span data-ttu-id="79b60-150">Bağlantı metnini ve URL'yi girin.</span><span class="sxs-lookup"><span data-stu-id="79b60-150">Enter link text and a URL.</span></span>
1. <span data-ttu-id="79b60-151">Daha fazla özel gezinti seçeneği eklemek için 2 ve 3. adımları tekrarlayın.</span><span class="sxs-lookup"><span data-stu-id="79b60-151">Repeat steps 2 and 3 to add more custom navigation options.</span></span>
1. <span data-ttu-id="79b60-152">Bitirdiğinizde, şablonu veya parçayı kaydedin ve iade edin.</span><span class="sxs-lookup"><span data-stu-id="79b60-152">When you've finished, save the template or fragment, and check it in.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="79b60-153">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="79b60-153">Additional resources</span></span>

[<span data-ttu-id="79b60-154">Şablonlar ve düzenlere genel bakış</span><span class="sxs-lookup"><span data-stu-id="79b60-154">Templates and layouts overview</span></span>](templates-layouts-overview.md)

[<span data-ttu-id="79b60-155">Şablonlarla çalışma</span><span class="sxs-lookup"><span data-stu-id="79b60-155">Work with templates</span></span>](work-with-templates.md)

[<span data-ttu-id="79b60-156">Önceden ayarlanmış düzenlerle çalışma</span><span class="sxs-lookup"><span data-stu-id="79b60-156">Work with preset layouts</span></span>](work-with-layouts.md)

[<span data-ttu-id="79b60-157">Parçalarla çalışma</span><span class="sxs-lookup"><span data-stu-id="79b60-157">Work with fragments</span></span>](work-with-fragments.md)

[<span data-ttu-id="79b60-158">Modüllerle çalışma</span><span class="sxs-lookup"><span data-stu-id="79b60-158">Work with modules</span></span>](work-with-modules.md)

[<span data-ttu-id="79b60-159">Sayfa URL'si oluşturma</span><span class="sxs-lookup"><span data-stu-id="79b60-159">Create a page URL</span></span>](create-page-url.md)

[<span data-ttu-id="79b60-160">Yayınlama gruplarıyla çalışma</span><span class="sxs-lookup"><span data-stu-id="79b60-160">Work with publish groups</span></span>](publish-groups.md)
