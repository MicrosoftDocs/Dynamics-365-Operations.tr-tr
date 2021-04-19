---
title: Kategori açılış sayfasını zenginleştirme
description: Bu konu, Dynamics 365 Commerce'deki kategori sayfalarının zenginini kapsamaktadır.
author: v-chgri
ms.date: 04/14/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: asharchw
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 5e18439fc0e91619cade33b83b87be0d5c4d1040
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/31/2021
ms.locfileid: "5799023"
---
# <a name="enrich-a-category-landing-page"></a><span data-ttu-id="a77c8-103">Kategori açılış sayfasını zenginleştirme</span><span class="sxs-lookup"><span data-stu-id="a77c8-103">Enrich a category landing page</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="a77c8-104">Bu konu, Dynamics 365 Commerce'deki kategori sayfalarının zenginini kapsamaktadır.</span><span class="sxs-lookup"><span data-stu-id="a77c8-104">This topic covers the enrichment of category pages in Dynamics 365 Commerce.</span></span>

<span data-ttu-id="a77c8-105">Commerce, kategori verileri gösterildiğinde kullanılan varsayılan bir kategori iniş sayfası sağlar.</span><span class="sxs-lookup"><span data-stu-id="a77c8-105">Commerce provides a default category landing page that is used when category data is shown.</span></span> <span data-ttu-id="a77c8-106">Varsayılan bir kategori sayfası, iyileştiriciler, kategori oluşturma, sıralama seçenekleri, seçim Özeti ve sayfalandırma denetimleri gibi gerekli öğeleri içerir.</span><span class="sxs-lookup"><span data-stu-id="a77c8-106">A default category page contains required elements, such as refiners, categorized product placement, sorting options, a choice summary, and pagination controls.</span></span> 

<span data-ttu-id="a77c8-107">Ancak, varsayılan kategori sayfasını kullanmak yerine, daha fazla içeriğe ve daha belirli öğelere sahip bir "zenginleştirilmiş" Kategori iniş sayfası kullanmak isteyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="a77c8-107">However, instead of using the default category page, you might want to use an "enriched" category landing page that has more content and more specific elements.</span></span> <span data-ttu-id="a77c8-108">Tipik bir zenginleştirme kategori sayfasına özel pazarlama içeriği eklenmesini gerektirebilir.</span><span class="sxs-lookup"><span data-stu-id="a77c8-108">A typical enrichment might involve adding category-specific marketing content to the category page.</span></span> <span data-ttu-id="a77c8-109">Bu içerik, çapraz satış amaçları, düzenleme listeleri, resimler, videolar ve diğer metinler için çapraz kategori ürün yerleştirmesi içerebilir.</span><span class="sxs-lookup"><span data-stu-id="a77c8-109">This content might include cross-category product placement for cross-sell purposes, editorial lists, images, videos, and other text.</span></span> <span data-ttu-id="a77c8-110">Varsayılan kategori sayfasını değiştirebilir veya belirli bir kategori için farklı bir kategori sayfası tanımlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="a77c8-110">You can either modify the default category page or define a different category page for a specific category.</span></span>

![Zenginleştirilmiş kategori açılış sayfası](./media/CategoryLandingPages.png)

<span data-ttu-id="a77c8-112">Commerce site oluşturucuda **Ürünler** sayfası, siteye atanan kanaldaki kategorilerin listesini içerir.</span><span class="sxs-lookup"><span data-stu-id="a77c8-112">In Commerce site builder, the **Products** page includes a list of categories from the channel that are assigned to the site.</span></span> <span data-ttu-id="a77c8-113">Bir kategori sayfası için **zenginleştirilmiş** durum seçildiyse, bu kategori sayfası zenginleştirgeçer.</span><span class="sxs-lookup"><span data-stu-id="a77c8-113">If the **Enriched** status is selected for a category page, that category page has been enriched.</span></span> <span data-ttu-id="a77c8-114">Aksi durumda, kategori için varsayılan kategori sayfası ve içerik kullanılır.</span><span class="sxs-lookup"><span data-stu-id="a77c8-114">Otherwise, the default category page and content are used for the category.</span></span> <span data-ttu-id="a77c8-115">Kategori adını seçerek, bir kategori için hem zenginleştirilmiş hem de zenginleştirilmemiş kategori sayfalarını önizleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="a77c8-115">You can preview both the enriched and non-enriched category pages for a category by selecting the category name.</span></span>

<span data-ttu-id="a77c8-116">Bir kategori sayfasını zenginleştirmek için, aşağıdakileri yapın.</span><span class="sxs-lookup"><span data-stu-id="a77c8-116">To enrich a category page, do the following.</span></span>

1. <span data-ttu-id="a77c8-117">**Ürünler** sayfasında, kategori sayfasını zenginleştirmek istediğiniz kategorinin adını seçin.</span><span class="sxs-lookup"><span data-stu-id="a77c8-117">On the **Products** page, select the name of the category for which you want to enrich the category page.</span></span> <span data-ttu-id="a77c8-118">Seçili Kategori için varsayılan kategori sayfası düzenleyicisinde açılır.</span><span class="sxs-lookup"><span data-stu-id="a77c8-118">The default category page for the selected category is opened in the page editor.</span></span>
2. <span data-ttu-id="a77c8-119">**Kategori sayfasını zenginleştir**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="a77c8-119">Select **Enrich category page**.</span></span>
3. <span data-ttu-id="a77c8-120">Zenginleştirilmiş kategori sayfası için bir şablon seçin.</span><span class="sxs-lookup"><span data-stu-id="a77c8-120">Select a template for the enriched category page.</span></span> <span data-ttu-id="a77c8-121">Yalnızca küçük değişiklikler yapıyorsanız, varsayılan kategori sayfasını seçebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="a77c8-121">If you're making only minor changes, you can select the default category page.</span></span> <span data-ttu-id="a77c8-122">Alternatif olarak, belirli bir kategori sayfası şablonu da seçebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="a77c8-122">Alternatively, you can select a specific category page template.</span></span> <span data-ttu-id="a77c8-123">Şablonu seçtiğinizde, sayfa Düzenleyicisi açılır ve seçili şablon seçili kategori için yeni bir kategori sayfası oluşturmak için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="a77c8-123">When you select the template, the page editor is opened, and the selected template is used to create a new category page for the selected category.</span></span> <span data-ttu-id="a77c8-124">Sayfa kullanımınıza alındı ve şimdi değişikliklerinizi yapabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="a77c8-124">The page is checked out to you, and you can now make your changes.</span></span>

> [!NOTE]
> <span data-ttu-id="a77c8-125">Kategori belirtim verileri kullanan modüller seçtiğiniz kategorideki verileri kullanır.</span><span class="sxs-lookup"><span data-stu-id="a77c8-125">Modules that use category specification data use the data from your selected category.</span></span> <span data-ttu-id="a77c8-126">Seçtiğiniz şablonun ayarları yapabileceğiniz değişiklikleri belirler.</span><span class="sxs-lookup"><span data-stu-id="a77c8-126">The settings of the template that you select determine the changes that you can make.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="a77c8-127">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="a77c8-127">Additional resources</span></span>

[<span data-ttu-id="a77c8-128">Var olan site sayfasını değiştirme</span><span class="sxs-lookup"><span data-stu-id="a77c8-128">Modify an existing site page</span></span>](modify-existing-page.md)

[<span data-ttu-id="a77c8-129">Yeni site sayfası ekleme</span><span class="sxs-lookup"><span data-stu-id="a77c8-129">Add a new site page</span></span>](add-new-page.md)

[<span data-ttu-id="a77c8-130">Sayfa düzeni seçme</span><span class="sxs-lookup"><span data-stu-id="a77c8-130">Select page layouts</span></span>](select-page-layouts.md)

[<span data-ttu-id="a77c8-131">SEO meta verilerini yönetme</span><span class="sxs-lookup"><span data-stu-id="a77c8-131">Manage SEO metadata</span></span>](manage-seo-metadata.md)

[<span data-ttu-id="a77c8-132">Sayfa kaydetme, önizleme ve yayımlama</span><span class="sxs-lookup"><span data-stu-id="a77c8-132">Save, preview, and publish a page</span></span>](save-preview-publish-page.md)

[<span data-ttu-id="a77c8-133">Ürün sayfasını zenginleştirme</span><span class="sxs-lookup"><span data-stu-id="a77c8-133">Enrich a product page</span></span>](enrich-product-page.md)

[<span data-ttu-id="a77c8-134">Sayfa içeriği erişilebilirliğini doğrulama</span><span class="sxs-lookup"><span data-stu-id="a77c8-134">Verify page content accessibility</span></span>](verify-accessibility.md)

[<span data-ttu-id="a77c8-135">URL parametrelerini temel alan dinamik e-ticaret sayfaları oluşturma</span><span class="sxs-lookup"><span data-stu-id="a77c8-135">Create dynamic e-commerce pages based on URL parameters</span></span>](create-dynamic-pages.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
