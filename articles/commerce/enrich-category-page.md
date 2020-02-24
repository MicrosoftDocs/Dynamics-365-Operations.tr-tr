---
title: Kategori açılış sayfasını zenginleştirme
description: Bu konu, Dynamics 365 Commerce'deki kategori sayfalarının zenginini kapsamaktadır.
author: v-chgri
manager: annbe
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Operations, Retail, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: asharchw
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 71348efba9fc1374b9e6599eb23f198d3851036e
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/01/2020
ms.locfileid: "3003062"
---
# <a name="enrich-a-category-landing-page"></a><span data-ttu-id="19a48-103">Kategori açılış sayfasını zenginleştirme</span><span class="sxs-lookup"><span data-stu-id="19a48-103">Enrich a category landing page</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="19a48-104">Bu konu, Dynamics 365 Commerce'deki kategori sayfalarının zenginini kapsamaktadır.</span><span class="sxs-lookup"><span data-stu-id="19a48-104">This topic covers the enrichment of category pages in Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="19a48-105">Genel Bakış</span><span class="sxs-lookup"><span data-stu-id="19a48-105">Overview</span></span>

<span data-ttu-id="19a48-106">Commerce, kategori verileri gösterildiğinde kullanılan varsayılan bir kategori iniş sayfası sağlar.</span><span class="sxs-lookup"><span data-stu-id="19a48-106">Commerce provides a default category landing page that is used when category data is shown.</span></span> <span data-ttu-id="19a48-107">Varsayılan bir kategori sayfası, iyileştiriciler, kategori oluşturma, sıralama seçenekleri, seçim Özeti ve sayfalandırma denetimleri gibi gerekli öğeleri içerir.</span><span class="sxs-lookup"><span data-stu-id="19a48-107">A default category page contains required elements, such as refiners, categorized product placement, sorting options, a choice summary, and pagination controls.</span></span> 

<span data-ttu-id="19a48-108">Ancak, varsayılan kategori sayfasını kullanmak yerine, daha fazla içeriğe ve daha belirli öğelere sahip bir "zenginleştirilmiş" Kategori iniş sayfası kullanmak isteyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="19a48-108">However, instead of using the default category page, you might want to use an "enriched" category landing page that has more content and more specific elements.</span></span> <span data-ttu-id="19a48-109">Tipik bir zenginleştirme kategori sayfasına özel pazarlama içeriği eklenmesini gerektirebilir.</span><span class="sxs-lookup"><span data-stu-id="19a48-109">A typical enrichment might involve adding category-specific marketing content to the category page.</span></span> <span data-ttu-id="19a48-110">Bu içerik, çapraz satış amaçları, düzenleme listeleri, resimler, videolar ve diğer metinler için çapraz kategori ürün yerleştirmesi içerebilir.</span><span class="sxs-lookup"><span data-stu-id="19a48-110">This content might include cross-category product placement for cross-sell purposes, editorial lists, images, videos, and other text.</span></span> <span data-ttu-id="19a48-111">Varsayılan kategori sayfasını değiştirebilir veya belirli bir kategori için farklı bir kategori sayfası tanımlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="19a48-111">You can either modify the default category page or define a different category page for a specific category.</span></span>

![Zenginleştirilmiş kategori açılış sayfası](./media/CategoryLandingPages.png)

<span data-ttu-id="19a48-113">Geliştirme aracında, **ürün** sayfası, siteye atanan kanaldan bir kategori listesi içerir.</span><span class="sxs-lookup"><span data-stu-id="19a48-113">In the authoring tool, the **Product** page includes a list of categories from the channel that are assigned to the site.</span></span> <span data-ttu-id="19a48-114">Bir kategori sayfası için **zenginleştirilmiş** durum seçildiyse, bu kategori sayfası zenginleştirgeçer.</span><span class="sxs-lookup"><span data-stu-id="19a48-114">If the **Enriched** status is selected for a category page, that category page has been enriched.</span></span> <span data-ttu-id="19a48-115">Aksi durumda, kategori için varsayılan kategori sayfası ve içerik kullanılır.</span><span class="sxs-lookup"><span data-stu-id="19a48-115">Otherwise, the default category page and content are used for the category.</span></span> <span data-ttu-id="19a48-116">Kategori adını seçerek, bir kategori için hem zenginleştirilmiş hem de zenginleştirilmemiş kategori sayfalarını önizleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="19a48-116">You can preview both the enriched and non-enriched category pages for a category by selecting the category name.</span></span>

<span data-ttu-id="19a48-117">Bir kategori sayfasını zenginleştirmek için, aşağıdakileri yapın.</span><span class="sxs-lookup"><span data-stu-id="19a48-117">To enrich a category page, do the following.</span></span>

1. <span data-ttu-id="19a48-118">**Ürünler** sayfasında, kategori sayfasını zenginleştirmek istediğiniz kategorinin adını seçin.</span><span class="sxs-lookup"><span data-stu-id="19a48-118">On the **Products** page, select the name of the category that you want to enrich the category page for.</span></span> <span data-ttu-id="19a48-119">Seçili Kategori için varsayılan kategori sayfası düzenleyicisinde açılır.</span><span class="sxs-lookup"><span data-stu-id="19a48-119">The default category page for the selected category is opened in the page editor.</span></span>
2. <span data-ttu-id="19a48-120">**Kategori sayfasını zenginleştir**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="19a48-120">Select **Enrich category page**.</span></span>
3. <span data-ttu-id="19a48-121">Zenginleştirilmiş kategori sayfası için bir şablon seçin.</span><span class="sxs-lookup"><span data-stu-id="19a48-121">Select a template for the enriched category page.</span></span> <span data-ttu-id="19a48-122">Yalnızca küçük değişiklikler yapıyorsanız, varsayılan kategori sayfasını seçebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="19a48-122">If you're making only minor changes, you can select the default category page.</span></span> <span data-ttu-id="19a48-123">Alternatif olarak, belirli bir kategori sayfası şablonu da seçebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="19a48-123">Alternatively, you can select a specific category page template.</span></span> <span data-ttu-id="19a48-124">Şablonu seçtiğinizde, sayfa Düzenleyicisi açılır ve seçili şablon seçili kategori için yeni bir kategori sayfası oluşturmak için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="19a48-124">When you select the template, the page editor is opened, and the selected template is used to create a new category page for the selected category.</span></span> <span data-ttu-id="19a48-125">Sayfa kullanımınıza alındı ve şimdi değişikliklerinizi yapabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="19a48-125">The page is checked out to you, and you can now make your changes.</span></span>

> [!NOTE]
> <span data-ttu-id="19a48-126">Kategori belirtim verileri kullanan modüller seçtiğiniz kategorideki verileri kullanır.</span><span class="sxs-lookup"><span data-stu-id="19a48-126">Modules that use category specification data use the data from your selected category.</span></span>
>
> <span data-ttu-id="19a48-127">Seçtiğiniz şablonun ayarları yapabileceğiniz değişiklikleri belirler.</span><span class="sxs-lookup"><span data-stu-id="19a48-127">The settings of the template that you select determine the changes that you can make.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="19a48-128">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="19a48-128">Additional resources</span></span>

[<span data-ttu-id="19a48-129">Var olan site sayfasını değiştirme</span><span class="sxs-lookup"><span data-stu-id="19a48-129">Modify an existing site page</span></span>](modify-existing-page.md)

[<span data-ttu-id="19a48-130">Yeni site sayfası ekleme</span><span class="sxs-lookup"><span data-stu-id="19a48-130">Add a new site page</span></span>](add-new-page.md)

[<span data-ttu-id="19a48-131">Sayfa düzeni seçme</span><span class="sxs-lookup"><span data-stu-id="19a48-131">Select page layouts</span></span>](select-page-layouts.md)

[<span data-ttu-id="19a48-132">SEO meta verilerini yönetme</span><span class="sxs-lookup"><span data-stu-id="19a48-132">Manage SEO metadata</span></span>](manage-seo-metadata.md)

[<span data-ttu-id="19a48-133">Sayfa kaydetme, önizleme ve yayımlama</span><span class="sxs-lookup"><span data-stu-id="19a48-133">Save, preview, and publish a page</span></span>](save-preview-publish-page.md)

[<span data-ttu-id="19a48-134">Ürün sayfasını zenginleştirme</span><span class="sxs-lookup"><span data-stu-id="19a48-134">Enrich a product page</span></span>](enrich-product-page.md)

[<span data-ttu-id="19a48-135">Sayfa içeriği erişilebilirliğini doğrula</span><span class="sxs-lookup"><span data-stu-id="19a48-135">Verify page content accessibility</span></span>](verify-accessibility.md)
