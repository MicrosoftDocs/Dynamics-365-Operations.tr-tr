---
title: Hızlı görüntüleme modülü
description: Bu konu hızlı görüntüleme modüllerini kapsamaktadır ve Microsoft Dynamics 365 Commerce'un site sayfalarına nasıl ekleneceğini açıklamaktadır.
author: anupamar-ms
ms.date: 01/28/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2020-01-08
ms.dyn365.ops.version: Release 10.0.17
ms.openlocfilehash: d7e88163fd9b8dc4f5636ed29e2c4248aece52bf
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/31/2021
ms.locfileid: "5792183"
---
# <a name="quick-view-module"></a><span data-ttu-id="b615e-103">Hızlı görüntüleme modülü</span><span class="sxs-lookup"><span data-stu-id="b615e-103">Quick view module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="b615e-104">Bu konu hızlı görüntüleme modüllerini kapsamaktadır ve Microsoft Dynamics 365 Commerce'un site sayfalarına nasıl ekleneceğini açıklamaktadır.</span><span class="sxs-lookup"><span data-stu-id="b615e-104">This topic covers quick view modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="b615e-105">Hızlı görüntüleme modülü, kullanıcıların bir liste sayfasındaki ürünlere göz atarken ürün bilgilerini hızlı bir şekilde görüntülemesine ve ürün ayrıntıları sayfasına (PDP) gitmeksizin liste sayfasından bir veya daha fazla ürün eklemesini sağlar.</span><span class="sxs-lookup"><span data-stu-id="b615e-105">The quick view module lets users quickly view product information when they browse products on a list page, and add one or more products to the cart from the list page, without having to go to the product details page (PDP).</span></span> <span data-ttu-id="b615e-106">Hızlı görüntüleme modülü, kullanıcıların bir "Sepete Ekle" kararı vermek için gereken ürün bilgilerine genel bakış sağlar.</span><span class="sxs-lookup"><span data-stu-id="b615e-106">The quick view module provides an overview of the product information that users require to make an "add to cart" decision.</span></span> <span data-ttu-id="b615e-107">Ayrıca, kullanıcıların ek ürün ayrıntılarını ve satın alma seçeneklerini görebilmesi için PDP'ye bir bağlantı sağlar.</span><span class="sxs-lookup"><span data-stu-id="b615e-107">It also provides a link to the PDP, so that users can view additional product details and purchase options.</span></span>

<span data-ttu-id="b615e-108">Hızlı görüntüleme modülü, [ürün koleksiyonu](product-collection-module-overview.md) ve [arama sonuçları](search-result-module.md) modülleri tarafından desteklenir.</span><span class="sxs-lookup"><span data-stu-id="b615e-108">The quick view module is supported by the [product collection](product-collection-module-overview.md) and [search results](search-result-module.md) modules.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="b615e-109">Hızlı görüntüleme modülü, Commerce 10.0.17 sürümü itibarıyla kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="b615e-109">The quick view module is available as of the Commerce version 10.0.17 release.</span></span>

<span data-ttu-id="b615e-110">Aşağıdaki şekilde ürün listesinde sayfasında kullanılan bir hızlı görüntüleme modülü örneği gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="b615e-110">The following illustration shows an example of a quick view module on a product list page.</span></span>

![Ürün listesi sayfasındaki hızlı görüntüleme modülü örneği](./media/ecommerce-quickview.PNG)

## <a name="module-properties"></a><span data-ttu-id="b615e-112">Modül özellikleri</span><span class="sxs-lookup"><span data-stu-id="b615e-112">Module properties</span></span>

<span data-ttu-id="b615e-113">Hızlı görüntüleme modülü, satın alma kutusu modülüyle aynı işlevlerden bazılarını destekler.</span><span class="sxs-lookup"><span data-stu-id="b615e-113">The quick view module supports some of the same functions as the buy box module.</span></span> <span data-ttu-id="b615e-114">Bu nedenle, Hızlı görünüm modülünün özellikleri bir satın alma kutusu modülünün özelliklerine benzer.</span><span class="sxs-lookup"><span data-stu-id="b615e-114">Therefore, the properties of a quick view module resemble the properties of a buy box module.</span></span>

| <span data-ttu-id="b615e-115">Özellik</span><span class="sxs-lookup"><span data-stu-id="b615e-115">Property</span></span> | <span data-ttu-id="b615e-116">Değerler</span><span class="sxs-lookup"><span data-stu-id="b615e-116">Values</span></span> | <span data-ttu-id="b615e-117">Tanım</span><span class="sxs-lookup"><span data-stu-id="b615e-117">Description</span></span> |
|----------------|--------|-------------|
| <span data-ttu-id="b615e-118">Başlık etiketi</span><span class="sxs-lookup"><span data-stu-id="b615e-118">Heading tag</span></span> | <span data-ttu-id="b615e-119">**H1**, **H2**, **H3**, **H4**, **H5** veya **H6**</span><span class="sxs-lookup"><span data-stu-id="b615e-119">**H1**, **H2**, **H3**, **H4**, **H5**, or **H6**</span></span> | <span data-ttu-id="b615e-120">Bu özellik, ürün başlığının başlık etiketini tanımlar.</span><span class="sxs-lookup"><span data-stu-id="b615e-120">This property defines the heading tag for the product title.</span></span> <span data-ttu-id="b615e-121">Hızlı görüntüleme modülü sayfanın en üstünde ise, erişilebilirlik standartlarını karşılamak için bu özelliğin **H1** olarak ayarlanması gerekir.</span><span class="sxs-lookup"><span data-stu-id="b615e-121">If the quick view module is at the top of the page, this property should be set to **H1** to meet accessibility standards.</span></span> |
| <span data-ttu-id="b615e-122">Özel fiyata izin ver</span><span class="sxs-lookup"><span data-stu-id="b615e-122">Allow custom price</span></span> | <span data-ttu-id="b615e-123">**Doğru** veya **yanlış**</span><span class="sxs-lookup"><span data-stu-id="b615e-123">**True** or **False**</span></span> | <span data-ttu-id="b615e-124">Bu özellik **Doğru** olarak ayarlanırsa, kullanıcı özel bir fiyat girebilir.</span><span class="sxs-lookup"><span data-stu-id="b615e-124">If this property is set to **True**, the user can enter a custom price.</span></span> |
| <span data-ttu-id="b615e-125">Minimum fiyat</span><span class="sxs-lookup"><span data-stu-id="b615e-125">Minimum price</span></span> | <span data-ttu-id="b615e-126">Tamsayı</span><span class="sxs-lookup"><span data-stu-id="b615e-126">Integer</span></span> | <span data-ttu-id="b615e-127">Bu özellik yalnızca **Özel fiyata izin ver** özelliği **Doğru** olarak ayarlandığında uygulanabilir.</span><span class="sxs-lookup"><span data-stu-id="b615e-127">This property is applicable only if the **Allow custom price** property is set to **True**.</span></span> <span data-ttu-id="b615e-128">Kullanıcının girebileceği minimum fiyatı tanımlar (örneğin, $1).</span><span class="sxs-lookup"><span data-stu-id="b615e-128">It defines the minimum price that the user can enter (for example, $1).</span></span> |
| <span data-ttu-id="b615e-129">Maksimum fiyat</span><span class="sxs-lookup"><span data-stu-id="b615e-129">Maximum price</span></span> | <span data-ttu-id="b615e-130">Tamsayı</span><span class="sxs-lookup"><span data-stu-id="b615e-130">Integer</span></span> | <span data-ttu-id="b615e-131">Bu özellik yalnızca **Özel fiyata izin ver** özelliği **Doğru** olarak ayarlandığında uygulanabilir.</span><span class="sxs-lookup"><span data-stu-id="b615e-131">This property is applicable only if the **Allow custom price** property is set to **True**.</span></span> <span data-ttu-id="b615e-132">Kullanıcının girebileceği maksimum fiyatı tanımlar (örneğin, $1000).</span><span class="sxs-lookup"><span data-stu-id="b615e-132">It defines the maximum price that the user can enter (for example, $1,000).</span></span> |

## <a name="commerce-site-builder-settings"></a><span data-ttu-id="b615e-133">Commerce site oluşturucu ayarları</span><span class="sxs-lookup"><span data-stu-id="b615e-133">Commerce site builder settings</span></span>

<span data-ttu-id="b615e-134">Satın alma kutusu modülü gibi, hızlı görünüm modülü de **Site Ayarları \> Uzantılar \> Alışveriş sepetine ürün ekle** ayarlarına uyar.</span><span class="sxs-lookup"><span data-stu-id="b615e-134">Like the buy box module, the quick view module respects the settings at **Site Settings \> Extensions \> Add product to cart**.</span></span> <span data-ttu-id="b615e-135">Ancak kullanıcıların bir liste sayfasında birden fazla ürüne göz atmasına ve liste sayfasından çıkmaksızın alışveriş sepetine eklemesine olanak tanımak olan, hızlı görüntüleme modülü amacıyla uyumlu olmadığından **Sepet sayfasına git** ayarı yoksayılır.</span><span class="sxs-lookup"><span data-stu-id="b615e-135">However, the **Navigate to cart page** setting is ignored, because it's inconsistent with the purpose of the quick view module, which is to enable users to browse multiple products on a list page and add them to the cart without moving away from the list page.</span></span>

## <a name="add-a-quick-view-module-to-a-product-collection-module"></a><span data-ttu-id="b615e-136">Ürün koleksiyonu modülüne hızlı görüntüleme modülü ekleme</span><span class="sxs-lookup"><span data-stu-id="b615e-136">Add a quick view module to a product collection module</span></span>

<span data-ttu-id="b615e-137">Ürün koleksiyonu ve arama sonuçları modüllerine hızlı görünüm modülü eklenebilir.</span><span class="sxs-lookup"><span data-stu-id="b615e-137">A quick view module can be added to the product collection and search results modules.</span></span>

<span data-ttu-id="b615e-138">Commerce site oluşturucuda bir ürün koleksiyonu modülüne hızlı görüntüleme modülü eklemek için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="b615e-138">To add a quick view module to a product collection module in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="b615e-139">**Sayfalar**'a gidin ve Fabrikam sitesi için giriş sayfasını seçin.</span><span class="sxs-lookup"><span data-stu-id="b615e-139">Go to **Pages**, and then select the home page for the Fabrikam site.</span></span>
1. <span data-ttu-id="b615e-140">Giriş sayfasındaki herhangi bir **Ürün Koleksiyonu** modülüne gidin, üç noktayı (**...**) seçin ve sonra **Modül Ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="b615e-140">Go to any **Product Collection** module on the homepage, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="b615e-141">**Modül Ekle** iletişim kutusunda **Hızlı Görüntüleme** modülünü seçin ve **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="b615e-141">In the **Add Module** dialog box, select the **Quick View** module, and then select **OK**.</span></span>
1. <span data-ttu-id="b615e-142">**Hızlı Görünüm** modülünün özellikler bölmesinde **Başlık**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="b615e-142">In the properties pane of the **Quick View** module, select **Heading**.</span></span> <span data-ttu-id="b615e-143">**Başlık** iletişim kutusunda, **Başlık düzeyi** alanını **H** 2 olarak ayarlayın ve **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="b615e-143">In the **Heading** dialog box, set the **Heading Level** field to **H2**, and then select **OK**.</span></span>
1. <span data-ttu-id="b615e-144">**Kaydet**'i seçin, sayfayı iade etmek için **Düzenlemeyi bitir**'i ve ardından yayımlamak için **Yayımla**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="b615e-144">Select **Save**, select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="b615e-145">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="b615e-145">Additional resources</span></span>

[<span data-ttu-id="b615e-146">Modül kitaplığına genel bakış</span><span class="sxs-lookup"><span data-stu-id="b615e-146">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="b615e-147">Satın alma kutusu modülü</span><span class="sxs-lookup"><span data-stu-id="b615e-147">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="b615e-148">Ürün topluluğu modülü</span><span class="sxs-lookup"><span data-stu-id="b615e-148">Product collection module</span></span>](product-collection-module-overview.md)

[<span data-ttu-id="b615e-149">Arama sonuçları modülü</span><span class="sxs-lookup"><span data-stu-id="b615e-149">Search results module</span></span>](search-result-module.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
