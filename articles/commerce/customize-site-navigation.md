---
title: Site gezintisini özelleştirme
description: Bu konu, Microsoft Dynamics 365 Commerce sitenizde gezinmek üzere ürünlerinizi düzenlemek için özelleştirilmiş bir çevrimiçi gezinti hiyerarşisinin nasıl oluşturulacağını açıklamaktadır.
author: bicyclingfool
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: StuHarg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 5bc50243ac3845adc60bfc173fc532fb28f3cdf6
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/31/2021
ms.locfileid: "5799361"
---
# <a name="customize-site-navigation"></a><span data-ttu-id="77403-103">Site gezintisini özelleştirme</span><span class="sxs-lookup"><span data-stu-id="77403-103">Customize site navigation</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="77403-104">Bu konu, Microsoft Dynamics 365 Commerce sitenizde gezinmek üzere ürünlerinizi düzenlemek için özelleştirilmiş bir çevrimiçi gezinti hiyerarşisinin nasıl oluşturulacağını açıklamaktadır.</span><span class="sxs-lookup"><span data-stu-id="77403-104">This topic describes how to create a customized online navigation hierarchy to organize your products for browsing on your Microsoft Dynamics 365 Commerce site.</span></span>

<span data-ttu-id="77403-105">Çevrimiçi mağazalar, genel olarak ürün kategorilerine giderek gezinerek ürünlere keşif ve göz atma sağlar.</span><span class="sxs-lookup"><span data-stu-id="77403-105">Online storefronts typically let customers discover and browse products by navigating through product categories.</span></span> <span data-ttu-id="77403-106">Bu özellik genellikle sayfanın üst kısmındaki sekmeler veya soldaki bir gezinti çubuğu ile sağlanır.</span><span class="sxs-lookup"><span data-stu-id="77403-106">This capability is usually provided by tabs at the top of the page or by a navigation bar on the left.</span></span> <span data-ttu-id="77403-107">Dynamics 365 Commerce'te, kategori gezinimin hiyerarşik yapısını ve çeşitli kategorilerde bulunan ürünleri oluşturabilir ve yönetebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="77403-107">In Dynamics 365 Commerce, you can create and manage the hierarchal structure of your category navigation and the products that are included in the various categories.</span></span>

## <a name="create-a-channel-navigation-hierarchy"></a><span data-ttu-id="77403-108">Kanal gezinme hiyerarşisi oluşturma</span><span class="sxs-lookup"><span data-stu-id="77403-108">Create a channel navigation hierarchy</span></span>

<span data-ttu-id="77403-109">Kanal gezinti hiyerarşisi oluşturmak için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="77403-109">To create a channel navigation hierarchy, follow these steps.</span></span>

1. <span data-ttu-id="77403-110">**Retail and Commerce \> Ürünler ve kategoriler \> Kategori ve ürün yönetimi**'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="77403-110">Go to **Retail and Commerce \> Products and categories \> Category and product management**.</span></span>
1. <span data-ttu-id="77403-111">**Kategori hiyerarşileri** ve ardından **Yeni** yi seçin.</span><span class="sxs-lookup"><span data-stu-id="77403-111">Select **Category hierarchies**, and then select **New**.</span></span>
1. <span data-ttu-id="77403-112">Hiyerarşiyi adlandırın.</span><span class="sxs-lookup"><span data-stu-id="77403-112">Name the hierarchy.</span></span>

    > [!NOTE]
    > <span data-ttu-id="77403-113">Oluşturduğunuz en üstteki kategori kök kategori düğümüdür.</span><span class="sxs-lookup"><span data-stu-id="77403-113">The topmost category that you create is the root category node.</span></span> <span data-ttu-id="77403-114">Sitenizde gösterilmez.</span><span class="sxs-lookup"><span data-stu-id="77403-114">It won't be shown on your site.</span></span> <span data-ttu-id="77403-115">Sitenizde tek bir üst düzey düğümün gösterildiği bir kategori hiyerarşisi oluşturmak için, kategoriyi kök kategorinin alt öğesi olarak oluşturun ve adlandırın.</span><span class="sxs-lookup"><span data-stu-id="77403-115">To create a category hierarchy where a single top-level node is shown on your site, create and name the category as a child of the root category.</span></span>

1. <span data-ttu-id="77403-116">**Yeni kategori düğümünü** seçin ve kategoriyi adlandırın.</span><span class="sxs-lookup"><span data-stu-id="77403-116">Select **New category node**, and name the category.</span></span>
1. <span data-ttu-id="77403-117">Gereksinim duyduğunuz şekilde kardeş ve alt kategori oluşturmaya devam edin.</span><span class="sxs-lookup"><span data-stu-id="77403-117">Continue to create sibling and child categories as you require.</span></span>

<span data-ttu-id="77403-118">Artık, en üst düzey kategori altında oluşturduğunuz her bir kategoriye ürün atayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="77403-118">You can now assign products to each category that you created under the top-level category.</span></span>

## <a name="customize-the-order-of-categories"></a><span data-ttu-id="77403-119">Kategorilerin sırasını özelleştirme</span><span class="sxs-lookup"><span data-stu-id="77403-119">Customize the order of categories</span></span>

<span data-ttu-id="77403-120">Varsayılan olarak tanımladığınız Kategoriler sitenizde alfabetik sırada görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="77403-120">By default, the categories that you define will appear in alphabetical order on your site.</span></span> <span data-ttu-id="77403-121">Ancak, kategorilerin görüntülenme sırasını da özelleştirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="77403-121">However, you can also customize the display order of categories.</span></span>

## <a name="assign-a-category-hierarchy-type"></a><span data-ttu-id="77403-122">Kategori hiyerarşisi türü atayın</span><span class="sxs-lookup"><span data-stu-id="77403-122">Assign a category hierarchy type</span></span>

1. <span data-ttu-id="77403-123">**Retail and Commerce \> Ürünler ve kategoriler \> Kategori ve ürün yönetimi**'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="77403-123">Go to **Retail and Commerce \> Products and categories \> Category and product management**.</span></span>
1. <span data-ttu-id="77403-124">**Kategori hiyerarşileri** seçin.</span><span class="sxs-lookup"><span data-stu-id="77403-124">Select **Category hierarchies**.</span></span>
1. <span data-ttu-id="77403-125">Ardından Eylem Bölmesinde, **kategori hiyerarşisi** sekmesindeki **Ayar** gurubunda **Hiyerarşi türünü ilişkilendir**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="77403-125">On the Action Pane, on the **Category hierarchy** tab, in the **Set up** group, select **Associate hierarchy type**.</span></span>
1. <span data-ttu-id="77403-126">**Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="77403-126">Select **New**.</span></span>
1. <span data-ttu-id="77403-127">**Kategori hiyerarşisi türü** alanında, **Kanal gezinme hiyerarşisi**'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="77403-127">In the **Category hierarchy type** field, select **Channel navigation hierarchy**.</span></span>
1. <span data-ttu-id="77403-128">**Kategori hiyerarşisi** alanında, daha önce oluşturduğunuz kanal gezinme hiyerarşisini seçin.</span><span class="sxs-lookup"><span data-stu-id="77403-128">In the **Category hierarchy** field, select the channel navigation hierarchy that you created earlier.</span></span>

## <a name="publish-new-or-updated-navigation-hierarchies"></a><span data-ttu-id="77403-129">Yeni veya güncelleştirilmiş gezinti hiyerarşileri Yayımla</span><span class="sxs-lookup"><span data-stu-id="77403-129">Publish new or updated navigation hierarchies</span></span>

<span data-ttu-id="77403-130">Gezinti hiyerarşinizi çevrimiçi mağaza için kullanılabilir hale getirmek için, aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="77403-130">To make your navigation hierarchy available to your online storefront, follow these steps.</span></span>

1. <span data-ttu-id="77403-131">**Retail and Commerce \> Kanal Kurulumu \> Kanal kategorileri ve ürün öznitelikleri**'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="77403-131">Go to **Retail and Commerce \> Channel setup \> Channel categories and product attributes**.</span></span>
1. <span data-ttu-id="77403-132">Soldaki ağaçta, çevrimiçi mağazayı seçin.</span><span class="sxs-lookup"><span data-stu-id="77403-132">In the tree on the left, select your online store.</span></span>
1. <span data-ttu-id="77403-133">**Kanal güncelleştirmelerini yayınla**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="77403-133">Select **Publish channel updates**.</span></span>
1. <span data-ttu-id="77403-134">**Retail and Commerce \> Retail and Commerce IT \> Dağıtım planı**'na gidin.</span><span class="sxs-lookup"><span data-stu-id="77403-134">Go to **Retail and Commerce \> Retail and Commerce IT \> Distribution schedule**.</span></span>
1. <span data-ttu-id="77403-135">Listede, **İş 1040** kodlu bulun ve seçin</span><span class="sxs-lookup"><span data-stu-id="77403-135">In the list, find and select **Job 1040**.</span></span>
1. <span data-ttu-id="77403-136">**Şimdi Çalıştır**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="77403-136">Select **Run now**.</span></span>
1. <span data-ttu-id="77403-137">1070 ve 1150 işleri için 5 ve 6 numaralı adımları yineleyin.</span><span class="sxs-lookup"><span data-stu-id="77403-137">Repeat steps 5 and 6 for jobs 1070 and 1150.</span></span>

## <a name="show-categories-on-your-site"></a><span data-ttu-id="77403-138">Sitenizde kategorileri gösterin</span><span class="sxs-lookup"><span data-stu-id="77403-138">Show categories on your site</span></span>

<span data-ttu-id="77403-139">Kategori hiyerarşinizi çevrimiçi mağazada göstermek için, şablon veya parçadaki uygun konuma gezinti menüsü modülünü eklemeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="77403-139">To show your category hierarchy on your online storefront, you must add the navigation menu module in the appropriate location in a template or fragment.</span></span> <span data-ttu-id="77403-140">Daha sonra gezinti menü modülü, sitenizin bağlı olduğu kanala gezinti hiyerarşinizi yayımladığınızda, gezinti hiyerarşinizi gösterecektir.</span><span class="sxs-lookup"><span data-stu-id="77403-140">The navigation menu module will then show your navigation hierarchy, provided that you've published your navigation hierarchy to the channel that your site is bound to.</span></span>

> [!NOTE]
> <span data-ttu-id="77403-141">Modül kitaplığında bulunan gezinti menü modülü, kullanıcıların yalnızca alt kategorileri olmayan kategorilere gitmesine izin verir.</span><span class="sxs-lookup"><span data-stu-id="77403-141">The navigation menu module that is included in the module library lets users navigate only to categories that don't have subcategories.</span></span> <span data-ttu-id="77403-142">Müşterilerinizin alt kategorileri olan kategorilere gidebilmesi gerekiyorsa, gezinti menü modülünü özelleştirmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="77403-142">If your customers should be able to navigate to categories that have subcategories, you must customize the navigation menu module.</span></span>

## <a name="add-custom-navigation-options"></a><span data-ttu-id="77403-143">Özel gezinti seçenekleri ekle</span><span class="sxs-lookup"><span data-stu-id="77403-143">Add custom navigation options</span></span>

<span data-ttu-id="77403-144">Gezinti menünüze, ürün kategori hiyerarşinizin parçası olmayan gezinme seçenekleri ekleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="77403-144">On your navigation menu, you can add navigation options that aren't part of your product category hierarchy.</span></span> <span data-ttu-id="77403-145">Örneğin, ürün kategorileri listesinin sonunda, siteniz için oluşturduğunuz bir kişi sayfasına işaret eden **bize ulaşın** öğesi ekleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="77403-145">For example, at the end of the list of product categories, you can add a **Contact Us** item that points to a contact page that you've built for your site.</span></span>

<span data-ttu-id="77403-146">Gezinti menünüze özel gezinti seçenekleri eklemek için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="77403-146">To add custom navigation options to your navigation menu, follow these steps.</span></span>

1. <span data-ttu-id="77403-147">Özelleştirmek istediğiniz şablonda veya parçada gezinti menü modülünü seçin.</span><span class="sxs-lookup"><span data-stu-id="77403-147">In the template or fragment that you want to customize, select the navigation menu module.</span></span>
1. <span data-ttu-id="77403-148">Özellik bölmesinde, **veri** sekmesinde, yeni bir içerik yönetim sistemi (CMS) gezinti öğesi oluşturmak için **Öğe ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="77403-148">In the property pane, on the **Data** tab, select **Add item** to create a new content management system (CMS) navigation item.</span></span>
1. <span data-ttu-id="77403-149">Bağlantı metnini ve URL'yi girin.</span><span class="sxs-lookup"><span data-stu-id="77403-149">Enter link text and a URL.</span></span>
1. <span data-ttu-id="77403-150">Daha fazla özel gezinti seçeneği eklemek için 2 ve 3. adımları tekrarlayın.</span><span class="sxs-lookup"><span data-stu-id="77403-150">Repeat steps 2 and 3 to add more custom navigation options.</span></span>
1. <span data-ttu-id="77403-151">Bitirdiğinizde, şablonu veya parçayı kaydetmek için **Kaydet**'i seçin ve sonra iade etmek için **Düzenlemeyi bitir**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="77403-151">When you've finished, select **Save** to save the template or fragment, and then select **Finish editing** to check it in.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="77403-152">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="77403-152">Additional resources</span></span>

[<span data-ttu-id="77403-153">Şablonlar ve düzenlere genel bakış</span><span class="sxs-lookup"><span data-stu-id="77403-153">Templates and layouts overview</span></span>](templates-layouts-overview.md)

[<span data-ttu-id="77403-154">Şablonlarla çalışma</span><span class="sxs-lookup"><span data-stu-id="77403-154">Work with templates</span></span>](work-with-templates.md)

[<span data-ttu-id="77403-155">Önceden ayarlanmış düzenlerle çalışma</span><span class="sxs-lookup"><span data-stu-id="77403-155">Work with preset layouts</span></span>](work-with-layouts.md)

[<span data-ttu-id="77403-156">Parçalarla çalışma</span><span class="sxs-lookup"><span data-stu-id="77403-156">Work with fragments</span></span>](work-with-fragments.md)

[<span data-ttu-id="77403-157">Modüllerle çalışma</span><span class="sxs-lookup"><span data-stu-id="77403-157">Work with modules</span></span>](work-with-modules.md)

[<span data-ttu-id="77403-158">Sayfa URL'si oluşturma</span><span class="sxs-lookup"><span data-stu-id="77403-158">Create a page URL</span></span>](create-page-url.md)

[<span data-ttu-id="77403-159">Yayınlama gruplarıyla çalışma</span><span class="sxs-lookup"><span data-stu-id="77403-159">Work with publish groups</span></span>](publish-groups.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
