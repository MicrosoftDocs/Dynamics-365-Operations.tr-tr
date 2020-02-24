---
title: Sepet modülü
description: Bu konu sepet modüllerini kapsamaktadır ve Microsoft Dynamics 365 Commerce'un site sayfalarına nasıl ekleneceğini açıklamaktadır.
author: anupamar-ms
manager: annbe
ms.date: 01/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: f6dd8fb56f7342eb9c877eda503a92f4a31e5863
ms.sourcegitcommit: 829329220475ed8cff5a5db92a59dd90c22b04fa
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/05/2020
ms.locfileid: "3025448"
---
# <a name="cart-module"></a><span data-ttu-id="a2ff9-103">Sepet modülü</span><span class="sxs-lookup"><span data-stu-id="a2ff9-103">Cart module</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="a2ff9-104">Bu konu sepet modüllerini kapsamaktadır ve Microsoft Dynamics 365 Commerce'un site sayfalarına nasıl ekleneceğini açıklamaktadır.</span><span class="sxs-lookup"><span data-stu-id="a2ff9-104">This topic covers cart modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="a2ff9-105">Genel Bakış</span><span class="sxs-lookup"><span data-stu-id="a2ff9-105">Overview</span></span>

<span data-ttu-id="a2ff9-106">Bir sepet modülü, müşteri kullanıma devam etmeden önce alışveriş sepetine eklenen maddeleri göstermek için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="a2ff9-106">A cart module is used to show the items that have been added to the cart before the customer proceeds to checkout.</span></span> <span data-ttu-id="a2ff9-107">Örneğin, alışveriş sepetine ve bir sipariş özetine eklenen tüm maddeleri içerir.</span><span class="sxs-lookup"><span data-stu-id="a2ff9-107">For example, it includes all the items that have been added to the cart and an order summary.</span></span> <span data-ttu-id="a2ff9-108">Ayrıca, müşterinin promosyon kodları uygulaması veya kaldırmasını da sağlar.</span><span class="sxs-lookup"><span data-stu-id="a2ff9-108">It also lets the customer apply or remove promotional codes.</span></span>

<span data-ttu-id="a2ff9-109">Sepet modülü, oturum açan kullanıma alma ve konuk kullanıma almayı destekler.</span><span class="sxs-lookup"><span data-stu-id="a2ff9-109">The cart module supports signed-in checkout and guest checkout.</span></span> <span data-ttu-id="a2ff9-110">Ayrıca bir **Alışverişe geri git** bağlantısı da destekler.</span><span class="sxs-lookup"><span data-stu-id="a2ff9-110">It also supports a **Back to shopping** link.</span></span> <span data-ttu-id="a2ff9-111">Bu bağlantı için yolu **Site Ayarları \> Uzantılar \> Rotalar** adresinden yapılandırabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="a2ff9-111">You can configure the route for this link at **Site Settings \> Extensions \> Routes**.</span></span>

<span data-ttu-id="a2ff9-112">Sepet modülü, verileri sepet koduna göre işler.</span><span class="sxs-lookup"><span data-stu-id="a2ff9-112">The cart module renders data based on the cart ID.</span></span> <span data-ttu-id="a2ff9-113">Sepet kodu, tüm sitede kullanılabilen bir tarayıcı tanımlama bilgisidir.</span><span class="sxs-lookup"><span data-stu-id="a2ff9-113">The cart ID is a browser cookie that is available throughout the site.</span></span>

## <a name="cart-module-properties-and-slots"></a><span data-ttu-id="a2ff9-114">Sepet modülü özelliklerini ve yuvaları</span><span class="sxs-lookup"><span data-stu-id="a2ff9-114">Cart module properties and slots</span></span>

<span data-ttu-id="a2ff9-115">Sepet modülü bir **Başlık** özelliğine sahiptir ve bu **Alışveriş sepeti** ve **Sepetinizdeki öğeler** gibi değerlere ayarlanabilir.</span><span class="sxs-lookup"><span data-stu-id="a2ff9-115">The cart module has a **Heading** property that can be set to values such as **Shopping bag** and **Items in your cart**.</span></span> 

## <a name="modules-that-can-be-used-in-a-cart-module"></a><span data-ttu-id="a2ff9-116">Sepet modülünde kullanılabilen modüller</span><span class="sxs-lookup"><span data-stu-id="a2ff9-116">Modules that can be used in a cart module</span></span>

- <span data-ttu-id="a2ff9-117">**Metin bloğu** – bu modül sepet modülündeki özel iletileri destekler.</span><span class="sxs-lookup"><span data-stu-id="a2ff9-117">**Text block** – This module supports custom messaging in the cart module.</span></span> <span data-ttu-id="a2ff9-118">İletiler, içerik yönetim sistemi (CMS) tarafından çalıştırılır.</span><span class="sxs-lookup"><span data-stu-id="a2ff9-118">The messages are driven by the content management system (CMS).</span></span> <span data-ttu-id="a2ff9-119">"Siparişinizdeki sorunları için 1-800-Fabrikam ile iletişim" gibi herhangi bir ileti eklenebilir.</span><span class="sxs-lookup"><span data-stu-id="a2ff9-119">Any message can be added, such as "For issues with your order, contact 1-800-Fabrikam."</span></span>
- <span data-ttu-id="a2ff9-120">**Mağaza seçici** - Bu modül bir maddenin almak için kullanılabilir olduğu yakındaki mağazaların listesini gösterir.</span><span class="sxs-lookup"><span data-stu-id="a2ff9-120">**Store selector** – This module shows a list of nearby stores where an item is available for pickup.</span></span> <span data-ttu-id="a2ff9-121">Kullanıcıların yakındaki mağazaları bulabilmesi için bir konum girmesini sağlar.</span><span class="sxs-lookup"><span data-stu-id="a2ff9-121">It lets users enter a location to find stores that are nearby.</span></span> <span data-ttu-id="a2ff9-122">Mağaza seçici modülü Bing Haritalar Coğrafi kodlama uygulama programlama arayüzü (API) ile tümleştirilmiştir ve bu sayede konumu bir enlem ve boylama dönüştürür.</span><span class="sxs-lookup"><span data-stu-id="a2ff9-122">The store selector module is integrated with the Bing Maps Geocoding application programming interface (API) to convert the location to a latitude and longitude.</span></span> <span data-ttu-id="a2ff9-123">Bir Bing Haritalar API anahtarı gereklidir ve Dynamics 365 Retail içinde Retail paylaşılan parametreler sayfasına eklenmelidir.</span><span class="sxs-lookup"><span data-stu-id="a2ff9-123">A Bing Maps API key is required and must be added to the Retail shared parameters page in Dynamics 365 Retail.</span></span> <span data-ttu-id="a2ff9-124">Bu modül iki özelliği destekler, **Arama yarıçapı** ve **Hizmet koşulları bağlantısı**.</span><span class="sxs-lookup"><span data-stu-id="a2ff9-124">This module supports two properties, **Search radius** and **Terms of service link**.</span></span> <span data-ttu-id="a2ff9-125">**Arama yarıçapı** özelliği, depolar için, mil olarak arama yarıçapını tanımlar.</span><span class="sxs-lookup"><span data-stu-id="a2ff9-125">The **Search radius** property defines the search radius for stores, in miles.</span></span> <span data-ttu-id="a2ff9-126">Herhangi bir değer belirtilmezse, varsayılan arama yarıçapı olan 50 mil değeri kullanılır.</span><span class="sxs-lookup"><span data-stu-id="a2ff9-126">If no value is specified, the default search radius, 50 miles, is used.</span></span> <span data-ttu-id="a2ff9-127">Bing Haritalar veya herhangi bir harici hizmet kullanılırsa, **Hizmet koşulları bağlantısı** özelliği, hizmet koşullarına bir bağlantı sağlamak için kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="a2ff9-127">If Bings Maps or any external service is used, the **Terms of service link** property can be used to provide a link to the terms of service.</span></span> <span data-ttu-id="a2ff9-128">Bing Haritalar hizmeti için bir hizmet koşulları bağlantısı gereklidir.</span><span class="sxs-lookup"><span data-stu-id="a2ff9-128">A terms of service link is required for the Bing Maps service.</span></span> 

## <a name="cart-module-settings"></a><span data-ttu-id="a2ff9-129">Sepet modülü ayarları</span><span class="sxs-lookup"><span data-stu-id="a2ff9-129">Cart module settings</span></span>

<span data-ttu-id="a2ff9-130">Sepet modülleri, **Site Ayarları \> Uzantılar** üzerinden yapılandırılabilir:</span><span class="sxs-lookup"><span data-stu-id="a2ff9-130">Cart modules have the following settings that can be configured at **Site Settings \> Extensions**:</span></span>

- <span data-ttu-id="a2ff9-131">**Maksimum miktar** - Bu özellik, alışveriş sepetine eklenebilecek maksimum madde sayısını belirtmekte kullanılır.</span><span class="sxs-lookup"><span data-stu-id="a2ff9-131">**Maximum quantity** – This property is used to specify the maximum number of each item that can be added to the cart.</span></span> <span data-ttu-id="a2ff9-132">Örneğin, bir perakende satılan her ürünün yalnızca 10 tanesi tek bir harekette satılabilir olduğuna karar verebilir.</span><span class="sxs-lookup"><span data-stu-id="a2ff9-132">For example, a retailer might decide that only 10 of each product can be sold in a single transaction.</span></span>
- <span data-ttu-id="a2ff9-133">**Stok denetimi** – değer **doğru** olarak ayarlandığında, yalnızca satın alma kutusu modülü stokta olduğundan emin olduktan sonra alışveriş sepetine bir madde eklenir.</span><span class="sxs-lookup"><span data-stu-id="a2ff9-133">**Inventory check** – When the value is set to **True**, an item is added to the cart only after the buy box module makes sure that it's in stock.</span></span> <span data-ttu-id="a2ff9-134">Bu stok denetimi hem maddenin sevk edileceği senaryolar için, hem de mağazada yer alacak senaryolar için gerçekleştirilir.</span><span class="sxs-lookup"><span data-stu-id="a2ff9-134">This inventory check is done both for scenarios where the item will be shipped and for scenarios where it will be picked up in the store.</span></span> <span data-ttu-id="a2ff9-135">Değer **yanlış** olarak ayarlandığında, bir madde alışveriş sepetine eklenmeden önce hiçbir stok denetimi yapılmaz ve sipariş yerleştirilir.</span><span class="sxs-lookup"><span data-stu-id="a2ff9-135">If the value is set to **False**, no inventory check is done before an item is added to the cart and the order is placed.</span></span>
- <span data-ttu-id="a2ff9-136">**Stok tamponu** – Bu özellik, stok için bir tampon numarası belirtmek için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="a2ff9-136">**Inventory buffer** – This property is used to specify a buffer number for inventory.</span></span> <span data-ttu-id="a2ff9-137">Gerçek zamanlı olarak sürdürülür ve birçok müşteri sipariş yerleştirirken, doğru stok sayımının korunması zor olabilir.</span><span class="sxs-lookup"><span data-stu-id="a2ff9-137">Inventory is maintained in real time, and when many customers place orders, it can be difficult to maintain an accurate inventory count.</span></span> <span data-ttu-id="a2ff9-138">Bir stok denetimi yapıldığında, stok tampon tutardan azsa, ürün Stokta tükenmiş olarak kabul edilir.</span><span class="sxs-lookup"><span data-stu-id="a2ff9-138">When an inventory check is done, if the inventory is less than the buffer amount, the product is treated as out of stock.</span></span> <span data-ttu-id="a2ff9-139">Bu nedenle, stok sayımı tam olarak eşitlenmemesi için çeşitli kanallarda hızlı şekilde satış gerçekleştiğinde, stokta olmayan bir maddenin satılması için daha az risk vardır.</span><span class="sxs-lookup"><span data-stu-id="a2ff9-139">Therefore, when sales occur quickly through several channels, and the inventory count isn't fully synced, there is less risk that an item that is out of stock will be sold.</span></span>
- <span data-ttu-id="a2ff9-140">**Alışverişe dön** – Bu özellik, **alışverişe geri dön** bağlantısına ait rotayı belirtmek için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="a2ff9-140">**Back to shopping** – This property is used to specify the route for the **Back to shopping** link.</span></span> <span data-ttu-id="a2ff9-141">Bu rota site düzeyinde yapılandırılabilir.</span><span class="sxs-lookup"><span data-stu-id="a2ff9-141">This route can be configured at the site level.</span></span> <span data-ttu-id="a2ff9-142">Bu yapılandırmanın perakendeciler müşteriyi giriş sayfasına veya sitedeki herhangi bir sayfaya geri götürür.</span><span class="sxs-lookup"><span data-stu-id="a2ff9-142">This configuration lets retailers take the customer back to the home page or any other page on the site.</span></span>

## <a name="commerce-scale-unit-interaction"></a><span data-ttu-id="a2ff9-143">Ticari ölçek birim etkileşimi</span><span class="sxs-lookup"><span data-stu-id="a2ff9-143">Commerce Scale Unit interaction</span></span>

<span data-ttu-id="a2ff9-144">Sepet modülü, ürün bilgilerini Commerce Scale Unit API'leri kullanarak alır.</span><span class="sxs-lookup"><span data-stu-id="a2ff9-144">The cart module retrieves product information by using Commerce Scale Unit APIs.</span></span> <span data-ttu-id="a2ff9-145">Commerce Scale Unit'deki tüm ürün bilgilerini almak için, tarayıcı tanımlama bilgisinden alışveriş sepetinin kodu kullanılır.</span><span class="sxs-lookup"><span data-stu-id="a2ff9-145">The cart ID from the browser cookie is used to retrieve all the product information from Commerce Scale Unit.</span></span>

## <a name="add-a-cart-module-to-a-page"></a><span data-ttu-id="a2ff9-146">Sayfaya sepet modülü ekleme</span><span class="sxs-lookup"><span data-stu-id="a2ff9-146">Add a cart module to a page</span></span>

<span data-ttu-id="a2ff9-147">Bir yeni sayfaya sepet modülü eklemek ve gerekli özellikleri ayarlamak için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="a2ff9-147">To add a cart module to a new page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="a2ff9-148">**Sepet parçası** olarak adlandırılan bir parça oluşturun ve buna sepet birimi ekleyin.</span><span class="sxs-lookup"><span data-stu-id="a2ff9-148">Create a fragment that is named **Cart fragment**, and add a cart module to it.</span></span>
1. <span data-ttu-id="a2ff9-149">Sepet modülüne başlık ekleyin.</span><span class="sxs-lookup"><span data-stu-id="a2ff9-149">Add a heading to the cart module.</span></span>
1. <span data-ttu-id="a2ff9-150">Sepet modülüne bir depo seçici modülü ekleyin.</span><span class="sxs-lookup"><span data-stu-id="a2ff9-150">Add a store selector module to the cart module.</span></span>
1. <span data-ttu-id="a2ff9-151">Parçayı kaydedin, düzenlemeyi bitirin ve sonra yayınlayın.</span><span class="sxs-lookup"><span data-stu-id="a2ff9-151">Save the fragment, finish editing it, and publish it.</span></span>
1. <span data-ttu-id="a2ff9-152">**Sepet şablonu** adlı bir şablon oluşturun ve yeni oluşturduğunuz sepet parçasını ekleyin.</span><span class="sxs-lookup"><span data-stu-id="a2ff9-152">Create a template that is named **Cart template**, and add the cart fragment that you just created to it.</span></span>
1. <span data-ttu-id="a2ff9-153">Şablonu kaydedin, düzenlemeyi bitirin ve sonra yayınlayın.</span><span class="sxs-lookup"><span data-stu-id="a2ff9-153">Save the template, finish editing it, and publish it.</span></span>
1. <span data-ttu-id="a2ff9-154">Yeni şablonu kullanan bir sayfa oluşturun.</span><span class="sxs-lookup"><span data-stu-id="a2ff9-154">Create a page that uses the new template.</span></span>
1. <span data-ttu-id="a2ff9-155">Sayfayı kaydet ve önizleyin.</span><span class="sxs-lookup"><span data-stu-id="a2ff9-155">Save and preview the page.</span></span>
1. <span data-ttu-id="a2ff9-156">Sayfayı düzenlemeyi tamamlayın ve sonra yayımlayın.</span><span class="sxs-lookup"><span data-stu-id="a2ff9-156">Finish editing the page, and publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="a2ff9-157">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="a2ff9-157">Additional resources</span></span>

[<span data-ttu-id="a2ff9-158">Başlangıç paketine genel bakış</span><span class="sxs-lookup"><span data-stu-id="a2ff9-158">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="a2ff9-159">Konteyner modülü</span><span class="sxs-lookup"><span data-stu-id="a2ff9-159">Container module</span></span>](add-container-module.md)

[<span data-ttu-id="a2ff9-160">Satın alma kutusu modülü</span><span class="sxs-lookup"><span data-stu-id="a2ff9-160">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="a2ff9-161">Ödeme modülü</span><span class="sxs-lookup"><span data-stu-id="a2ff9-161">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="a2ff9-162">Sipariş onayı modülü</span><span class="sxs-lookup"><span data-stu-id="a2ff9-162">Order confirmation module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="a2ff9-163">Üst bilgi modülü</span><span class="sxs-lookup"><span data-stu-id="a2ff9-163">Header module</span></span>](author-header-module.md)

[<span data-ttu-id="a2ff9-164">Alt bilgi modülü</span><span class="sxs-lookup"><span data-stu-id="a2ff9-164">Footer module</span></span>](author-footer-module.md)
