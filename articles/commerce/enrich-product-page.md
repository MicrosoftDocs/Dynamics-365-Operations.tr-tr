---
title: Ürün sayfasını zenginleştirme
description: Bu konuda, Microsoft Dynamics 365 Commerce'te ürün sayfası zenginleştirme yöntemi açıklanmıştır .
author: psimolin
ms.date: 04/14/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: f6c1a9474ed514426386b1d7b4a72b62129cdb8a
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/31/2021
ms.locfileid: "5799069"
---
# <a name="enrich-a-product-page"></a><span data-ttu-id="fe90e-103">Ürün sayfasını zenginleştirme</span><span class="sxs-lookup"><span data-stu-id="fe90e-103">Enrich a product page</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="fe90e-104">Bu konuda, Microsoft Dynamics 365 Commerce'te ürün sayfası zenginleştirme yöntemi açıklanmıştır .</span><span class="sxs-lookup"><span data-stu-id="fe90e-104">This topic describes how to enrich a product page in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="fe90e-105">Varsayılan olarak, siteniz ürün verilerini göstermek için genel bir sayfa kullanır.</span><span class="sxs-lookup"><span data-stu-id="fe90e-105">By default, your site uses a generic page to show product data.</span></span> <span data-ttu-id="fe90e-106">Bu sayfa, ürünle ilgili temel bilgileri ve bunu satmak için gerekli olan denetimleri içerir.</span><span class="sxs-lookup"><span data-stu-id="fe90e-106">This page includes the basic information about the product and the controls that are required to sell it.</span></span> <span data-ttu-id="fe90e-107">Ancak, Commerce Scale Unit'ten belirli bir ürünle ilgili ek resim veya metinle gelen bilgileri ekleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="fe90e-107">However, you can supplement the information that comes from the Commerce Scale Unit with additional images or text for a specific product.</span></span> <span data-ttu-id="fe90e-108">Bu işleme, ürün sayfasını zenginleştirme adı verilir.</span><span class="sxs-lookup"><span data-stu-id="fe90e-108">This process is known as enriching the product page.</span></span>

<span data-ttu-id="fe90e-109">Birçok durumda, ürünleriniz için özel ek içerik kullanmak isteyeceksiniz.</span><span class="sxs-lookup"><span data-stu-id="fe90e-109">In many cases, you will want to use specific additional content for your products.</span></span> <span data-ttu-id="fe90e-110">Geliştirme aracında **Retail and Commerce**'e gittiğinizde, bu siteye atanan kanaldan bir ürün listesi göreceksiniz.</span><span class="sxs-lookup"><span data-stu-id="fe90e-110">When you go to **Retail and Commerce** in the authoring tool, you will see a list of products from the channel that is assigned to the site.</span></span> <span data-ttu-id="fe90e-111">Bu listede, **zenginleştirilmiş** sütun, bir ürünle ilgili ürün sayfasının zenginleştirilmiş olduğunu gösterir.</span><span class="sxs-lookup"><span data-stu-id="fe90e-111">In this list, the **Enriched** column indicates whether the product page for a product has been enriched.</span></span> <span data-ttu-id="fe90e-112">Sütunda bir onay işareti görünürse, ürün için zenginleştirilmiş bir ürün sayfası bulunur.</span><span class="sxs-lookup"><span data-stu-id="fe90e-112">If a check mark appears in the column, an enriched product page exists for the product.</span></span> <span data-ttu-id="fe90e-113">Onay işareti görüntülenmezse, ürün için varsayılan ürün sayfası ve içerik kullanılır.</span><span class="sxs-lookup"><span data-stu-id="fe90e-113">If no check mark appears, the default product page and content are used for the product.</span></span> <span data-ttu-id="fe90e-114">Listeden ürün adını seçerek, bir kategori için hem zenginleştirilmiş hem de zenginleştirilmemiş ürün sayfalarını önizleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="fe90e-114">You can preview both enriched and non-enriched product pages by selecting a product name in the list.</span></span>

## <a name="enrich-a-product-page"></a><span data-ttu-id="fe90e-115">Ürün sayfasını zenginleştirme</span><span class="sxs-lookup"><span data-stu-id="fe90e-115">Enrich a product page</span></span>

<span data-ttu-id="fe90e-116">Ürün sayfasını zenginleştirmek için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="fe90e-116">To enrich a product page, follow these steps.</span></span>

1. <span data-ttu-id="fe90e-117">**Siteler** altında, **Fabrikam**'ı seçin (veya sitenizin adını).</span><span class="sxs-lookup"><span data-stu-id="fe90e-117">Under **Sites**, select **Fabrikam** (or the name of your site).</span></span>
1. <span data-ttu-id="fe90e-118">Soldaki gezinti bölmesinde **Ürünler** seçin.</span><span class="sxs-lookup"><span data-stu-id="fe90e-118">In the navigation pane on the left, select **Products**.</span></span>
1. <span data-ttu-id="fe90e-119">Zenginleştirilmiş ürün sayfasına sahip olmayan herhangi bir ürünü seçin.</span><span class="sxs-lookup"><span data-stu-id="fe90e-119">Select any product that doesn't have an enriched product page.</span></span>
1. <span data-ttu-id="fe90e-120">Eylem Bölmesinde, **Ürün sayfasını zenginleştir**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="fe90e-120">On the Action Pane, select **Enrich product page**.</span></span>
1. <span data-ttu-id="fe90e-121">**PDP şablonu**'nu seçin ve sonra **Tamam**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="fe90e-121">Select **PDP-template**, and then select **OK**.</span></span>
1. <span data-ttu-id="fe90e-122">Soldaki sayfa anahat ağacında **ana** yuvayı genişletin.</span><span class="sxs-lookup"><span data-stu-id="fe90e-122">In the page outline tree on the left, expand the **Main** slot.</span></span>
1. <span data-ttu-id="fe90e-123">**Ana** yuvası için üç nokta (**...**) düğmesini seçin ve **Modül ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="fe90e-123">Select the ellipsis button (**...**) for the **Main** slot, and then select **Add Module**.</span></span>
1. <span data-ttu-id="fe90e-124">**Konteyner 2**'i seçin ve sonra **Tamam**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="fe90e-124">Select **Container 2**, and then select **OK**.</span></span>
1. <span data-ttu-id="fe90e-125">**konteyner 2** seçin, üç nokta düğmesini seçin ve sonra **Modül ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="fe90e-125">Select the ellipsis button for **Container 2**, and then select **Add Module**.</span></span>
1. <span data-ttu-id="fe90e-126">**Özellik**'i seçin ve sonra **Tamam**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="fe90e-126">Select **Feature**, and then select **OK**.</span></span>
1. <span data-ttu-id="fe90e-127">Sağdaki Özellikler bölmesinde, **zengin metin** alanına ürünün güncelleştirilmiş açıklamasını girin.</span><span class="sxs-lookup"><span data-stu-id="fe90e-127">In the properties pane on the right, in the **Rich Text** field, enter the updated description of the product.</span></span>
1. <span data-ttu-id="fe90e-128">**Başlık** alanına başlık metnini girin ve **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="fe90e-128">In the **Heading** field, enter heading text, and then select **OK**.</span></span>
1. <span data-ttu-id="fe90e-129">**Kaydet** i seçin ve sonra **Düzenlemeyi bitir**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="fe90e-129">Select **Save**, and then select **Finish editing**.</span></span>
1. <span data-ttu-id="fe90e-130">**Yorumlar** alanında **Zenginleştirilmiş ürün** seçeneğini girin ve **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="fe90e-130">In the **Comments** field, enter **Enriched a product**, and then select **OK**.</span></span>
1. <span data-ttu-id="fe90e-131">Zenginleştirilmiş ürün sayfasını önizlemek için **Önizleme** 'yi seçin .</span><span class="sxs-lookup"><span data-stu-id="fe90e-131">Select **Preview** to preview the enriched product page.</span></span> <span data-ttu-id="fe90e-132">Bitirdiğinizde, geliştirme aracına dönmek için Önizleme sekmesini kapatın.</span><span class="sxs-lookup"><span data-stu-id="fe90e-132">When you've finished, close the preview tab to return to the authoring tool.</span></span>
1. <span data-ttu-id="fe90e-133">**Yayımla**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="fe90e-133">Select **Publish**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="fe90e-134">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="fe90e-134">Additional resources</span></span>

[<span data-ttu-id="fe90e-135">Var olan site sayfasını değiştirme</span><span class="sxs-lookup"><span data-stu-id="fe90e-135">Modify an existing site page</span></span>](modify-existing-page.md)

[<span data-ttu-id="fe90e-136">Yeni site sayfası ekleme</span><span class="sxs-lookup"><span data-stu-id="fe90e-136">Add a new site page</span></span>](add-new-page.md)

[<span data-ttu-id="fe90e-137">Sayfa düzeni seçme</span><span class="sxs-lookup"><span data-stu-id="fe90e-137">Select page layouts</span></span>](select-page-layouts.md)

[<span data-ttu-id="fe90e-138">SEO meta verilerini yönetme</span><span class="sxs-lookup"><span data-stu-id="fe90e-138">Manage SEO metadata</span></span>](manage-seo-metadata.md)

[<span data-ttu-id="fe90e-139">Sayfa kaydetme, önizleme ve yayımlama</span><span class="sxs-lookup"><span data-stu-id="fe90e-139">Save, preview, and publish a page</span></span>](save-preview-publish-page.md)

[<span data-ttu-id="fe90e-140">Kategori açılış sayfasını zenginleştirme</span><span class="sxs-lookup"><span data-stu-id="fe90e-140">Enrich a category landing page</span></span>](enrich-category-page.md)

[<span data-ttu-id="fe90e-141">Sayfa içeriği erişilebilirliğini doğrulama</span><span class="sxs-lookup"><span data-stu-id="fe90e-141">Verify page content accessibility</span></span>](verify-accessibility.md)

[<span data-ttu-id="fe90e-142">URL parametrelerini temel alan dinamik e-ticaret sayfaları oluşturma</span><span class="sxs-lookup"><span data-stu-id="fe90e-142">Create dynamic e-commerce pages based on URL parameters</span></span>](create-dynamic-pages.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
