---
title: Kategori açılış sayfasını zenginleştirme
description: Bu konu, Dynamics 365 Commerce'deki kategori sayfalarının zenginini kapsamaktadır.
author: v-chgri
manager: annbe
ms.date: 04/14/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: asharchw
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: fbcf6ec60723b726e022b4e17bbde4c903e5cb57
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5238801"
---
# <a name="enrich-a-category-landing-page"></a><span data-ttu-id="15dbb-103">Kategori açılış sayfasını zenginleştirme</span><span class="sxs-lookup"><span data-stu-id="15dbb-103">Enrich a category landing page</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="15dbb-104">Bu konu, Dynamics 365 Commerce'deki kategori sayfalarının zenginini kapsamaktadır.</span><span class="sxs-lookup"><span data-stu-id="15dbb-104">This topic covers the enrichment of category pages in Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="15dbb-105">Genel Bakış</span><span class="sxs-lookup"><span data-stu-id="15dbb-105">Overview</span></span>

<span data-ttu-id="15dbb-106">Commerce, kategori verileri gösterildiğinde kullanılan varsayılan bir kategori iniş sayfası sağlar.</span><span class="sxs-lookup"><span data-stu-id="15dbb-106">Commerce provides a default category landing page that is used when category data is shown.</span></span> <span data-ttu-id="15dbb-107">Varsayılan bir kategori sayfası, iyileştiriciler, kategori oluşturma, sıralama seçenekleri, seçim Özeti ve sayfalandırma denetimleri gibi gerekli öğeleri içerir.</span><span class="sxs-lookup"><span data-stu-id="15dbb-107">A default category page contains required elements, such as refiners, categorized product placement, sorting options, a choice summary, and pagination controls.</span></span> 

<span data-ttu-id="15dbb-108">Ancak, varsayılan kategori sayfasını kullanmak yerine, daha fazla içeriğe ve daha belirli öğelere sahip bir "zenginleştirilmiş" Kategori iniş sayfası kullanmak isteyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="15dbb-108">However, instead of using the default category page, you might want to use an "enriched" category landing page that has more content and more specific elements.</span></span> <span data-ttu-id="15dbb-109">Tipik bir zenginleştirme kategori sayfasına özel pazarlama içeriği eklenmesini gerektirebilir.</span><span class="sxs-lookup"><span data-stu-id="15dbb-109">A typical enrichment might involve adding category-specific marketing content to the category page.</span></span> <span data-ttu-id="15dbb-110">Bu içerik, çapraz satış amaçları, düzenleme listeleri, resimler, videolar ve diğer metinler için çapraz kategori ürün yerleştirmesi içerebilir.</span><span class="sxs-lookup"><span data-stu-id="15dbb-110">This content might include cross-category product placement for cross-sell purposes, editorial lists, images, videos, and other text.</span></span> <span data-ttu-id="15dbb-111">Varsayılan kategori sayfasını değiştirebilir veya belirli bir kategori için farklı bir kategori sayfası tanımlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="15dbb-111">You can either modify the default category page or define a different category page for a specific category.</span></span>

![Zenginleştirilmiş kategori açılış sayfası](./media/CategoryLandingPages.png)

<span data-ttu-id="15dbb-113">Commerce site oluşturucuda **Ürünler** sayfası, siteye atanan kanaldaki kategorilerin listesini içerir.</span><span class="sxs-lookup"><span data-stu-id="15dbb-113">In Commerce site builder, the **Products** page includes a list of categories from the channel that are assigned to the site.</span></span> <span data-ttu-id="15dbb-114">Bir kategori sayfası için **zenginleştirilmiş** durum seçildiyse, bu kategori sayfası zenginleştirgeçer.</span><span class="sxs-lookup"><span data-stu-id="15dbb-114">If the **Enriched** status is selected for a category page, that category page has been enriched.</span></span> <span data-ttu-id="15dbb-115">Aksi durumda, kategori için varsayılan kategori sayfası ve içerik kullanılır.</span><span class="sxs-lookup"><span data-stu-id="15dbb-115">Otherwise, the default category page and content are used for the category.</span></span> <span data-ttu-id="15dbb-116">Kategori adını seçerek, bir kategori için hem zenginleştirilmiş hem de zenginleştirilmemiş kategori sayfalarını önizleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="15dbb-116">You can preview both the enriched and non-enriched category pages for a category by selecting the category name.</span></span>

<span data-ttu-id="15dbb-117">Bir kategori sayfasını zenginleştirmek için, aşağıdakileri yapın.</span><span class="sxs-lookup"><span data-stu-id="15dbb-117">To enrich a category page, do the following.</span></span>

1. <span data-ttu-id="15dbb-118">**Ürünler** sayfasında, kategori sayfasını zenginleştirmek istediğiniz kategorinin adını seçin.</span><span class="sxs-lookup"><span data-stu-id="15dbb-118">On the **Products** page, select the name of the category for which you want to enrich the category page.</span></span> <span data-ttu-id="15dbb-119">Seçili Kategori için varsayılan kategori sayfası düzenleyicisinde açılır.</span><span class="sxs-lookup"><span data-stu-id="15dbb-119">The default category page for the selected category is opened in the page editor.</span></span>
2. <span data-ttu-id="15dbb-120">**Kategori sayfasını zenginleştir**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="15dbb-120">Select **Enrich category page**.</span></span>
3. <span data-ttu-id="15dbb-121">Zenginleştirilmiş kategori sayfası için bir şablon seçin.</span><span class="sxs-lookup"><span data-stu-id="15dbb-121">Select a template for the enriched category page.</span></span> <span data-ttu-id="15dbb-122">Yalnızca küçük değişiklikler yapıyorsanız, varsayılan kategori sayfasını seçebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="15dbb-122">If you're making only minor changes, you can select the default category page.</span></span> <span data-ttu-id="15dbb-123">Alternatif olarak, belirli bir kategori sayfası şablonu da seçebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="15dbb-123">Alternatively, you can select a specific category page template.</span></span> <span data-ttu-id="15dbb-124">Şablonu seçtiğinizde, sayfa Düzenleyicisi açılır ve seçili şablon seçili kategori için yeni bir kategori sayfası oluşturmak için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="15dbb-124">When you select the template, the page editor is opened, and the selected template is used to create a new category page for the selected category.</span></span> <span data-ttu-id="15dbb-125">Sayfa kullanımınıza alındı ve şimdi değişikliklerinizi yapabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="15dbb-125">The page is checked out to you, and you can now make your changes.</span></span>

> [!NOTE]
> <span data-ttu-id="15dbb-126">Kategori belirtim verileri kullanan modüller seçtiğiniz kategorideki verileri kullanır.</span><span class="sxs-lookup"><span data-stu-id="15dbb-126">Modules that use category specification data use the data from your selected category.</span></span> <span data-ttu-id="15dbb-127">Seçtiğiniz şablonun ayarları yapabileceğiniz değişiklikleri belirler.</span><span class="sxs-lookup"><span data-stu-id="15dbb-127">The settings of the template that you select determine the changes that you can make.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="15dbb-128">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="15dbb-128">Additional resources</span></span>

[<span data-ttu-id="15dbb-129">Var olan site sayfasını değiştirme</span><span class="sxs-lookup"><span data-stu-id="15dbb-129">Modify an existing site page</span></span>](modify-existing-page.md)

[<span data-ttu-id="15dbb-130">Yeni site sayfası ekleme</span><span class="sxs-lookup"><span data-stu-id="15dbb-130">Add a new site page</span></span>](add-new-page.md)

[<span data-ttu-id="15dbb-131">Sayfa düzeni seçme</span><span class="sxs-lookup"><span data-stu-id="15dbb-131">Select page layouts</span></span>](select-page-layouts.md)

[<span data-ttu-id="15dbb-132">SEO meta verilerini yönetme</span><span class="sxs-lookup"><span data-stu-id="15dbb-132">Manage SEO metadata</span></span>](manage-seo-metadata.md)

[<span data-ttu-id="15dbb-133">Sayfa kaydetme, önizleme ve yayımlama</span><span class="sxs-lookup"><span data-stu-id="15dbb-133">Save, preview, and publish a page</span></span>](save-preview-publish-page.md)

[<span data-ttu-id="15dbb-134">Ürün sayfasını zenginleştirme</span><span class="sxs-lookup"><span data-stu-id="15dbb-134">Enrich a product page</span></span>](enrich-product-page.md)

[<span data-ttu-id="15dbb-135">Sayfa içeriği erişilebilirliğini doğrulama</span><span class="sxs-lookup"><span data-stu-id="15dbb-135">Verify page content accessibility</span></span>](verify-accessibility.md)

[<span data-ttu-id="15dbb-136">URL parametrelerini temel alan dinamik e-ticaret sayfaları oluşturma</span><span class="sxs-lookup"><span data-stu-id="15dbb-136">Create dynamic e-commerce pages based on URL parameters</span></span>](create-dynamic-pages.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]