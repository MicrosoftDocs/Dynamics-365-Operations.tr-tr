---
title: Ölçü birimi ayarlarını uygulama
description: Bu konu, ölçü birimlerini kapsamaktadır ve Microsoft Dynamics 365 Commerce'ta bunların nasıl uygulanacağını açıklar .
author: anupamar-ms
manager: annbe
ms.date: 04/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: 2c5750ae506978dfac842eebf4ba6036322bdd7f
ms.sourcegitcommit: 593438a145672c55ff6a910eabce2939300b40ad
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2021
ms.locfileid: "5937626"
---
# <a name="apply-unit-of-measure-settings"></a><span data-ttu-id="c239d-103">Ölçü birimi ayarlarını uygulama</span><span class="sxs-lookup"><span data-stu-id="c239d-103">Apply unit of measure settings</span></span>

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

<span data-ttu-id="c239d-104">Bu konu, ölçü birimlerini kapsamaktadır ve Microsoft Dynamics 365 Commerce'ta bunların nasıl uygulanacağını açıklar .</span><span class="sxs-lookup"><span data-stu-id="c239d-104">This topic covers unit of measure settings and describes how to apply them in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="c239d-105">Bir ürün, "tekli" "çift" ve "düzine" gibi farklı birimlerde satılabilir.</span><span class="sxs-lookup"><span data-stu-id="c239d-105">A product can be sold in different units, such as "each," "pair," and "dozen."</span></span> <span data-ttu-id="c239d-106">Commerce genel merkezde bir ürünün satış ile ilgili ölçü birimi tanımlanabilir ve bir e-ticaret sitesinde görüntülenebilir.</span><span class="sxs-lookup"><span data-stu-id="c239d-106">In Commerce headquarters, the sell-by unit of measure can be defined for a product and shown on an e-commerce site.</span></span> <span data-ttu-id="c239d-107">Örneğin, bir satıcı bir ürünü tek başına ve düzineler olarak satıyorsa kullanılabilir ölçü birimleri diğer ürün bilgileriyle birlikte gösterilebilir.</span><span class="sxs-lookup"><span data-stu-id="c239d-107">For example, if a retailer sells a product both individually and in dozens, the available units of measure can be shown together with other product information.</span></span>

<span data-ttu-id="c239d-108">Aşağıdaki görseldeki örnekte, Commerce genel merkezde bir ürün için **beher** (tekli) satış ölçü birimi yapılandırılmıştır.</span><span class="sxs-lookup"><span data-stu-id="c239d-108">In the example in the following illustration, a sell-by unit of measure of **ea** (each) has been configured for a product in Commerce headquarters.</span></span>

![Commerce genel merkezde ölçü birimiyle yapılandırılmış bir ürün örneği](./media/Productunit-headquarters.PNG)

> [!NOTE]
> <span data-ttu-id="c239d-110">Ölçü birimini uygulama ve gösterme desteği, Commerce sürümü 10.0.19 itibariyle kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="c239d-110">Support for applying and showing the unit of measure is available as of the Commerce version 10.0.19 release.</span></span>

## <a name="unit-of-measure-settings"></a><span data-ttu-id="c239d-111">Ölçü birimi ayarları</span><span class="sxs-lookup"><span data-stu-id="c239d-111">Unit of measure settings</span></span>

<span data-ttu-id="c239d-112">Ölçü birimi görüntüleme ayarları, Commerce site oluşturucuda, **Site ayarları \> Uzantılar \>Ürünlerin görünüm ölçü birimleri** bölümünde belirlenir.</span><span class="sxs-lookup"><span data-stu-id="c239d-112">Unit of measure display settings are defined in Commerce site builder, at **Site settings \> Extensions \> Display unit of measure for products**.</span></span> <span data-ttu-id="c239d-113">Desteklenen üç ayar vardır:</span><span class="sxs-lookup"><span data-stu-id="c239d-113">There are three supported settings:</span></span>

- <span data-ttu-id="c239d-114">**Görüntüleme** – Bu ayar seçildiğinde, e-ticaret sitesi ürünün ölçü birimini göstermez.</span><span class="sxs-lookup"><span data-stu-id="c239d-114">**Do not display** – When this setting is selected, the e-commerce site won't show the unit of measure for the product.</span></span> <span data-ttu-id="c239d-115">Bu davranış, varsayılan davranıştır.</span><span class="sxs-lookup"><span data-stu-id="c239d-115">This behavior is the default behavior.</span></span>
- <span data-ttu-id="c239d-116">**Ürün satın alma deneyiminde görüntüle** - Bu ayar seçildiğinde, ölçü birimi; ürün detayları, sepet, ödeme, sipariş geçmişi ve sipariş ayrıntıları sayfalarında gösterilir.</span><span class="sxs-lookup"><span data-stu-id="c239d-116">**Display in the product buying experience** – When this setting is selected, the unit of measure is shown on product details, cart, checkout, order history, and order details pages.</span></span>
- <span data-ttu-id="c239d-117">**Ürün tarama ve satın alma deneyiminde görüntüle** - Bu ayar seçildiğinde, ölçü birimi ürün satın alma deneyimi sayfalarında ve ayrıca ürün tarama deneyimi sırasında gösterilir.</span><span class="sxs-lookup"><span data-stu-id="c239d-117">**Display in the product browsing and buying experience** – When this setting is selected, the unit of measure is shown on the product buying experience pages and also during the product browsing experience.</span></span> <span data-ttu-id="c239d-118">Bu davranışın bir parçası olarak, arama sonuçlarında ve ürün koleksiyonu modüllerinde ölçü birimleri gösterilir.</span><span class="sxs-lookup"><span data-stu-id="c239d-118">As part of this behavior, units of measure are shown in search results and product collection modules.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="c239d-119">Ölçü birimi görüntüleme ayarları Commerce sürüm 10.0.19'dan itibaren mevcuttur.</span><span class="sxs-lookup"><span data-stu-id="c239d-119">Unit of measure display settings are available as of the Commerce version 10.0.19 release.</span></span> <span data-ttu-id="c239d-120">Commerce'ün eski sürümlerinden birini güncelleştiriyorsanız, appsettings.json dosyasını el ile güncelleştirmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="c239d-120">If you're updating from an older version of Commerce, you must manually update the appsettings.json file.</span></span> <span data-ttu-id="c239d-121">Talimatlar için bkz. [SDK ve modül kitaplığı güncelleştirmeleri](e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file).</span><span class="sxs-lookup"><span data-stu-id="c239d-121">For instructions, see [SDK and module library updates](e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file).</span></span>

## <a name="modules-that-use-unit-of-measure-settings"></a><span data-ttu-id="c239d-122">Ölçü birimi ayarlarını kullanan modüller</span><span class="sxs-lookup"><span data-stu-id="c239d-122">Modules that use unit of measure settings</span></span>

<span data-ttu-id="c239d-123">Ölçü birimi ayarlarını kullanan modüllere satınalma kutusu, istek listesi, sepet, sepet simgesi, arama sonuçları konteyneri, ürün koleksiyonu, ödeme ve sipariş ayrıntıları dahildir.</span><span class="sxs-lookup"><span data-stu-id="c239d-123">Modules that use the unit of measure settings include the buy box, wishlist, cart, cart icon, search results container, product collection, checkout, and order details modules.</span></span>

<span data-ttu-id="c239d-124">Aşağıdaki görselde yer alan örnekte, bir ürün ayrıntıları sayfası (PDP) bir ürünün ölçü birimini (**beher**) gösterir.</span><span class="sxs-lookup"><span data-stu-id="c239d-124">In the example in the following illustration, a product details page (PDP) shows the unit of measure (**ea**) for a product.</span></span>

![Ölçü birimini gösteren bir PDP örneği](./media/Productunit-PDP.png)

<span data-ttu-id="c239d-126">Aşağıdaki görselde yer alan örnekte, bir ürün koleksiyon modülü bir ürünün ölçü birimini (**beher**) gösterir.</span><span class="sxs-lookup"><span data-stu-id="c239d-126">In the example in the following illustration, a product collection module shows the unit of measure (**ea**) for a product.</span></span>

![Ölçü birimini gösteren bir ürün koleksiyon modülü örneği](./media/Productunit-productcollection.png)

## <a name="additional-resources"></a><span data-ttu-id="c239d-128">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="c239d-128">Additional resources</span></span>

[<span data-ttu-id="c239d-129">Modül kitaplığına genel bakış</span><span class="sxs-lookup"><span data-stu-id="c239d-129">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="c239d-130">Alışveriş sepeti modülü</span><span class="sxs-lookup"><span data-stu-id="c239d-130">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="c239d-131">Satın alma kutusu modülü</span><span class="sxs-lookup"><span data-stu-id="c239d-131">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="c239d-132">Hesap yönetimi sayfaları ve modülleri</span><span class="sxs-lookup"><span data-stu-id="c239d-132">Account management pages and modules</span></span>](account-management.md)

[<span data-ttu-id="c239d-133">SDK ve modül kitaplığı güncelleştirmeleri</span><span class="sxs-lookup"><span data-stu-id="c239d-133">SDK and module library updates</span></span>](e-commerce-extensibility/sdk-updates.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
