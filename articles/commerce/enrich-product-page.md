---
title: Ürün sayfasını zenginleştirme
description: Bu konuda, Microsoft Dynamics 365 Commerce'te ürün sayfası zenginleştirme yöntemi açıklanmıştır .
author: psimolin
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
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: fcb8eda188a6796282a7a800b87a68dfef9d7d62
ms.sourcegitcommit: 872600103d2a444d78963867e5e0cdc62e68c3ec
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/01/2021
ms.locfileid: "5097350"
---
# <a name="enrich-a-product-page"></a><span data-ttu-id="b2631-103">Ürün sayfasını zenginleştirme</span><span class="sxs-lookup"><span data-stu-id="b2631-103">Enrich a product page</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="b2631-104">Bu konuda, Microsoft Dynamics 365 Commerce'te ürün sayfası zenginleştirme yöntemi açıklanmıştır .</span><span class="sxs-lookup"><span data-stu-id="b2631-104">This topic describes how to enrich a product page in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="b2631-105">Genel Bakış</span><span class="sxs-lookup"><span data-stu-id="b2631-105">Overview</span></span>

<span data-ttu-id="b2631-106">Varsayılan olarak, siteniz ürün verilerini göstermek için genel bir sayfa kullanır.</span><span class="sxs-lookup"><span data-stu-id="b2631-106">By default, your site uses a generic page to show product data.</span></span> <span data-ttu-id="b2631-107">Bu sayfa, ürünle ilgili temel bilgileri ve bunu satmak için gerekli olan denetimleri içerir.</span><span class="sxs-lookup"><span data-stu-id="b2631-107">This page includes the basic information about the product and the controls that are required to sell it.</span></span> <span data-ttu-id="b2631-108">Ancak, Commerce Scale Unit'ten belirli bir ürünle ilgili ek resim veya metinle gelen bilgileri ekleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="b2631-108">However, you can supplement the information that comes from the Commerce Scale Unit with additional images or text for a specific product.</span></span> <span data-ttu-id="b2631-109">Bu işleme, ürün sayfasını zenginleştirme adı verilir.</span><span class="sxs-lookup"><span data-stu-id="b2631-109">This process is known as enriching the product page.</span></span>

<span data-ttu-id="b2631-110">Birçok durumda, ürünleriniz için özel ek içerik kullanmak isteyeceksiniz.</span><span class="sxs-lookup"><span data-stu-id="b2631-110">In many cases, you will want to use specific additional content for your products.</span></span> <span data-ttu-id="b2631-111">Geliştirme aracında **Retail and Commerce**'e gittiğinizde, bu siteye atanan kanaldan bir ürün listesi göreceksiniz.</span><span class="sxs-lookup"><span data-stu-id="b2631-111">When you go to **Retail and Commerce** in the authoring tool, you will see a list of products from the channel that is assigned to the site.</span></span> <span data-ttu-id="b2631-112">Bu listede, **zenginleştirilmiş** sütun, bir ürünle ilgili ürün sayfasının zenginleştirilmiş olduğunu gösterir.</span><span class="sxs-lookup"><span data-stu-id="b2631-112">In this list, the **Enriched** column indicates whether the product page for a product has been enriched.</span></span> <span data-ttu-id="b2631-113">Sütunda bir onay işareti görünürse, ürün için zenginleştirilmiş bir ürün sayfası bulunur.</span><span class="sxs-lookup"><span data-stu-id="b2631-113">If a check mark appears in the column, an enriched product page exists for the product.</span></span> <span data-ttu-id="b2631-114">Onay işareti görüntülenmezse, ürün için varsayılan ürün sayfası ve içerik kullanılır.</span><span class="sxs-lookup"><span data-stu-id="b2631-114">If no check mark appears, the default product page and content are used for the product.</span></span> <span data-ttu-id="b2631-115">Listeden ürün adını seçerek, bir kategori için hem zenginleştirilmiş hem de zenginleştirilmemiş ürün sayfalarını önizleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="b2631-115">You can preview both enriched and non-enriched product pages by selecting a product name in the list.</span></span>

## <a name="enrich-a-product-page"></a><span data-ttu-id="b2631-116">Ürün sayfasını zenginleştirme</span><span class="sxs-lookup"><span data-stu-id="b2631-116">Enrich a product page</span></span>

<span data-ttu-id="b2631-117">Ürün sayfasını zenginleştirmek için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="b2631-117">To enrich a product page, follow these steps.</span></span>

1. <span data-ttu-id="b2631-118">**Siteler** altında, **Fabrikam**'ı seçin (veya sitenizin adını).</span><span class="sxs-lookup"><span data-stu-id="b2631-118">Under **Sites**, select **Fabrikam** (or the name of your site).</span></span>
1. <span data-ttu-id="b2631-119">Soldaki gezinti bölmesinde **Ürünler** seçin.</span><span class="sxs-lookup"><span data-stu-id="b2631-119">In the navigation pane on the left, select **Products**.</span></span>
1. <span data-ttu-id="b2631-120">Zenginleştirilmiş ürün sayfasına sahip olmayan herhangi bir ürünü seçin.</span><span class="sxs-lookup"><span data-stu-id="b2631-120">Select any product that doesn't have an enriched product page.</span></span>
1. <span data-ttu-id="b2631-121">Eylem Bölmesinde, **Ürün sayfasını zenginleştir**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="b2631-121">On the Action Pane, select **Enrich product page**.</span></span>
1. <span data-ttu-id="b2631-122">**PDP şablonu**'nu seçin ve sonra **Tamam**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="b2631-122">Select **PDP-template**, and then select **OK**.</span></span>
1. <span data-ttu-id="b2631-123">Soldaki sayfa anahat ağacında **ana** yuvayı genişletin.</span><span class="sxs-lookup"><span data-stu-id="b2631-123">In the page outline tree on the left, expand the **Main** slot.</span></span>
1. <span data-ttu-id="b2631-124">**Ana** yuvası için üç nokta (**...**) düğmesini seçin ve **Modül ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="b2631-124">Select the ellipsis button (**...**) for the **Main** slot, and then select **Add Module**.</span></span>
1. <span data-ttu-id="b2631-125">**Konteyner 2**'i seçin ve sonra **Tamam**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="b2631-125">Select **Container 2**, and then select **OK**.</span></span>
1. <span data-ttu-id="b2631-126">**konteyner 2** seçin, üç nokta düğmesini seçin ve sonra **Modül ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="b2631-126">Select the ellipsis button for **Container 2**, and then select **Add Module**.</span></span>
1. <span data-ttu-id="b2631-127">**Özellik**'i seçin ve sonra **Tamam**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="b2631-127">Select **Feature**, and then select **OK**.</span></span>
1. <span data-ttu-id="b2631-128">Sağdaki Özellikler bölmesinde, **zengin metin** alanına ürünün güncelleştirilmiş açıklamasını girin.</span><span class="sxs-lookup"><span data-stu-id="b2631-128">In the properties pane on the right, in the **Rich Text** field, enter the updated description of the product.</span></span>
1. <span data-ttu-id="b2631-129">**Başlık** alanına başlık metnini girin ve **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="b2631-129">In the **Heading** field, enter heading text, and then select **OK**.</span></span>
1. <span data-ttu-id="b2631-130">**Kaydet** i seçin ve sonra **Düzenlemeyi bitir**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="b2631-130">Select **Save**, and then select **Finish editing**.</span></span>
1. <span data-ttu-id="b2631-131">**Yorumlar** alanında **Zenginleştirilmiş ürün** seçeneğini girin ve **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="b2631-131">In the **Comments** field, enter **Enriched a product**, and then select **OK**.</span></span>
1. <span data-ttu-id="b2631-132">Zenginleştirilmiş ürün sayfasını önizlemek için **Önizleme** 'yi seçin .</span><span class="sxs-lookup"><span data-stu-id="b2631-132">Select **Preview** to preview the enriched product page.</span></span> <span data-ttu-id="b2631-133">Bitirdiğinizde, geliştirme aracına dönmek için Önizleme sekmesini kapatın.</span><span class="sxs-lookup"><span data-stu-id="b2631-133">When you've finished, close the preview tab to return to the authoring tool.</span></span>
1. <span data-ttu-id="b2631-134">**Yayımla**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="b2631-134">Select **Publish**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="b2631-135">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="b2631-135">Additional resources</span></span>

[<span data-ttu-id="b2631-136">Var olan site sayfasını değiştirme</span><span class="sxs-lookup"><span data-stu-id="b2631-136">Modify an existing site page</span></span>](modify-existing-page.md)

[<span data-ttu-id="b2631-137">Yeni site sayfası ekleme</span><span class="sxs-lookup"><span data-stu-id="b2631-137">Add a new site page</span></span>](add-new-page.md)

[<span data-ttu-id="b2631-138">Sayfa düzeni seçme</span><span class="sxs-lookup"><span data-stu-id="b2631-138">Select page layouts</span></span>](select-page-layouts.md)

[<span data-ttu-id="b2631-139">SEO meta verilerini yönetme</span><span class="sxs-lookup"><span data-stu-id="b2631-139">Manage SEO metadata</span></span>](manage-seo-metadata.md)

[<span data-ttu-id="b2631-140">Sayfa kaydetme, önizleme ve yayımlama</span><span class="sxs-lookup"><span data-stu-id="b2631-140">Save, preview, and publish a page</span></span>](save-preview-publish-page.md)

[<span data-ttu-id="b2631-141">Kategori açılış sayfasını zenginleştirme</span><span class="sxs-lookup"><span data-stu-id="b2631-141">Enrich a category landing page</span></span>](enrich-category-page.md)

[<span data-ttu-id="b2631-142">Sayfa içeriği erişilebilirliğini doğrulama</span><span class="sxs-lookup"><span data-stu-id="b2631-142">Verify page content accessibility</span></span>](verify-accessibility.md)

[<span data-ttu-id="b2631-143">URL parametrelerini temel alan dinamik e-ticaret sayfaları oluşturma</span><span class="sxs-lookup"><span data-stu-id="b2631-143">Create dynamic e-commerce pages based on URL parameters</span></span>](create-dynamic-pages.md)
