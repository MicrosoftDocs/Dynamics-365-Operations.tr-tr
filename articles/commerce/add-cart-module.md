---
title: Sepet modülü
description: Bu konu sepet modüllerini kapsamaktadır ve Microsoft Dynamics 365 Commerce'un site sayfalarına nasıl ekleneceğini açıklamaktadır.
author: anupamar-ms
manager: annbe
ms.date: 04/13/2020
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
ms.openlocfilehash: d91f6ff24f8f2c051ed23565983c2bc6a2c12b55
ms.sourcegitcommit: ac966ea3a6c557fb5f9634b187b0e788d3e82d4d
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/14/2020
ms.locfileid: "3261433"
---
# <a name="cart-module"></a><span data-ttu-id="fb024-103">Sepet modülü</span><span class="sxs-lookup"><span data-stu-id="fb024-103">Cart module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="fb024-104">Bu konu sepet modüllerini kapsamaktadır ve Microsoft Dynamics 365 Commerce'un site sayfalarına nasıl ekleneceğini açıklamaktadır.</span><span class="sxs-lookup"><span data-stu-id="fb024-104">This topic covers cart modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="fb024-105">Özet</span><span class="sxs-lookup"><span data-stu-id="fb024-105">Overview</span></span>

<span data-ttu-id="fb024-106">Bir sepet modülü, müşteri kullanıma devam etmeden önce alışveriş sepetine eklenen maddeleri göstermek için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="fb024-106">A cart module shows the items that have been added to the cart before the customer proceeds to checkout.</span></span> <span data-ttu-id="fb024-107">Ayrıca, modül sipariş özeti gösterir ve müşterinin promosyon kodları uygulamasını veya kaldırmasını sağlar.</span><span class="sxs-lookup"><span data-stu-id="fb024-107">The module also shows an order summary and lets the customer apply or remove promotional codes.</span></span>

<span data-ttu-id="fb024-108">Sepet modülü, oturum açan kullanıma alma ve konuk kullanıma almayı destekler.</span><span class="sxs-lookup"><span data-stu-id="fb024-108">The cart module supports signed-in checkout and guest checkout.</span></span> <span data-ttu-id="fb024-109">Ayrıca bir **Alışverişe geri git** bağlantısı da destekler.</span><span class="sxs-lookup"><span data-stu-id="fb024-109">It also supports a **Back to shopping** link.</span></span> <span data-ttu-id="fb024-110">Bu bağlantı için yolu **Site Ayarları \> Uzantılar \> Rotalar** adresinden yapılandırabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="fb024-110">You can configure the route for this link at **Site Settings \> Extensions \> Routes**.</span></span>

<span data-ttu-id="fb024-111">Sepet modülü, tüm sitede kullanılabilen bir tarayıcı tanımlama bilgisi olan sepet kimliğine göre verileri işler.</span><span class="sxs-lookup"><span data-stu-id="fb024-111">The cart module renders data based on the cart ID, which is a browser cookie available throughout the site.</span></span>

## <a name="cart-module-properties-and-slots"></a><span data-ttu-id="fb024-112">Sepet modülü özelliklerini ve yuvaları</span><span class="sxs-lookup"><span data-stu-id="fb024-112">Cart module properties and slots</span></span>

<span data-ttu-id="fb024-113">Sepet modülü bir **Başlık** özelliğine sahiptir ve bu **Alışveriş sepeti** ve **Sepetinizdeki öğeler** gibi değerlere ayarlanabilir.</span><span class="sxs-lookup"><span data-stu-id="fb024-113">The cart module has a **Heading** property that can be set to values such as **Shopping bag** and **Items in your cart**.</span></span> 

## <a name="modules-that-can-be-used-in-a-cart-module"></a><span data-ttu-id="fb024-114">Sepet modülünde kullanılabilen modüller</span><span class="sxs-lookup"><span data-stu-id="fb024-114">Modules that can be used in a cart module</span></span>

- <span data-ttu-id="fb024-115">**Metin bloğu** – bu modül sepet modülündeki özel iletileri destekler.</span><span class="sxs-lookup"><span data-stu-id="fb024-115">**Text block** – This module supports custom messaging in the cart module.</span></span> <span data-ttu-id="fb024-116">İletiler, içerik yönetim sistemi (CMS) tarafından çalıştırılır.</span><span class="sxs-lookup"><span data-stu-id="fb024-116">The messages are driven by the content management system (CMS).</span></span> <span data-ttu-id="fb024-117">"Siparişinizdeki sorunları için 1-800-Fabrikam ile iletişim" gibi herhangi bir ileti eklenebilir.</span><span class="sxs-lookup"><span data-stu-id="fb024-117">Any message can be added, such as "For issues with your order, contact 1-800-Fabrikam."</span></span>
- <span data-ttu-id="fb024-118">**Mağaza seçici** - Bu modül bir maddenin almak için kullanılabilir olduğu yakındaki mağazaların listesini gösterir.</span><span class="sxs-lookup"><span data-stu-id="fb024-118">**Store selector** – This module shows a list of nearby stores where an item is available for pickup.</span></span> <span data-ttu-id="fb024-119">Kullanıcıların yakındaki mağazaları bulabilmesi için bir konum girmesini sağlar.</span><span class="sxs-lookup"><span data-stu-id="fb024-119">It lets users enter a location to find stores that are nearby.</span></span> <span data-ttu-id="fb024-120">Bu modülle ilgili daha fazla bilgi için bkz. [Mağaza seçme modülü](store-selector.md).</span><span class="sxs-lookup"><span data-stu-id="fb024-120">For more information on this module, see [Store selector module](store-selector.md).</span></span>


## <a name="module-properties"></a><span data-ttu-id="fb024-121">Modül özellikleri</span><span class="sxs-lookup"><span data-stu-id="fb024-121">Module properties</span></span>

<span data-ttu-id="fb024-122">Sepet modülleri, **Site Ayarları \> Uzantılar** üzerinden yapılandırılabilir:</span><span class="sxs-lookup"><span data-stu-id="fb024-122">Cart modules have the following settings that can be configured at **Site Settings \> Extensions**:</span></span>

- <span data-ttu-id="fb024-123">**Maksimum miktar** - Bu özellik, alışveriş sepetine eklenebilecek maksimum madde sayısını belirtmekte kullanılır.</span><span class="sxs-lookup"><span data-stu-id="fb024-123">**Maximum quantity** – This property is used to specify the maximum number of each item that can be added to the cart.</span></span> <span data-ttu-id="fb024-124">Örneğin, bir perakende satılan her ürünün yalnızca 10 tanesi tek bir harekette satılabilir olduğuna karar verebilir.</span><span class="sxs-lookup"><span data-stu-id="fb024-124">For example, a retailer might decide that only 10 of each product can be sold in a single transaction.</span></span>
- <span data-ttu-id="fb024-125">**Stok denetimi** – değer **doğru** olarak ayarlandığında, yalnızca satın alma kutusu modülü stokta olduğundan emin olduktan sonra alışveriş sepetine bir madde eklenir.</span><span class="sxs-lookup"><span data-stu-id="fb024-125">**Inventory check** – When the value is set to **True**, an item is added to the cart only after the buy box module makes sure that it's in stock.</span></span> <span data-ttu-id="fb024-126">Bu stok denetimi hem maddenin sevk edileceği senaryolar için, hem de mağazada yer alacak senaryolar için gerçekleştirilir.</span><span class="sxs-lookup"><span data-stu-id="fb024-126">This inventory check is done for scenarios where the item will be shipped and for scenarios where it will be picked up in the store.</span></span> <span data-ttu-id="fb024-127">Değer **yanlış** olarak ayarlandığında, bir madde alışveriş sepetine eklenmeden önce hiçbir stok denetimi yapılmaz ve sipariş yerleştirilir.</span><span class="sxs-lookup"><span data-stu-id="fb024-127">If the value is set to **False**, no inventory check is done before an item is added to the cart and the order is placed.</span></span> <span data-ttu-id="fb024-128">Arka ofiste stok ayarlarının yapılandırılması hakkında bilgi için bkz. [Perakende kanalları için stok kullanılabilirliğini yapılandırma](calculated-inventory-retail-channels.md).</span><span class="sxs-lookup"><span data-stu-id="fb024-128">For information on how to configure inventory settings in back office, see [Calculate inventory availability for retail channels](calculated-inventory-retail-channels.md).</span></span>
- <span data-ttu-id="fb024-129">**Stok tamponu** – Bu özellik, stok için bir tampon numarası belirtmek için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="fb024-129">**Inventory buffer** – This property is used to specify a buffer number for inventory.</span></span> <span data-ttu-id="fb024-130">Gerçek zamanlı olarak sürdürülür ve birçok müşteri sipariş yerleştirirken, doğru stok sayımının korunması zor olabilir.</span><span class="sxs-lookup"><span data-stu-id="fb024-130">Inventory is maintained in real time, and when many customers place orders, it can be difficult to maintain an accurate inventory count.</span></span> <span data-ttu-id="fb024-131">Bir stok denetimi yapıldığında, stok tampon tutardan azsa, ürün Stokta tükenmiş olarak kabul edilir.</span><span class="sxs-lookup"><span data-stu-id="fb024-131">When an inventory check is done, if the inventory is less than the buffer amount, the product is treated as out of stock.</span></span> <span data-ttu-id="fb024-132">Bu nedenle, stok sayımı tam olarak eşitlenmemesi için çeşitli kanallarda hızlı şekilde satış gerçekleştiğinde, stokta olmayan bir maddenin satılması için daha az risk vardır.</span><span class="sxs-lookup"><span data-stu-id="fb024-132">Therefore, when sales occur quickly through several channels, and the inventory count isn't fully synced, there is less risk that an item that is out of stock will be sold.</span></span>
- <span data-ttu-id="fb024-133">**Alışverişe dön** – Bu özellik, **alışverişe geri dön** bağlantısına ait rotayı belirtmek için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="fb024-133">**Back to shopping** – This property is used to specify the route for the **Back to shopping** link.</span></span> <span data-ttu-id="fb024-134">Rota, Tesis düzeyinde konfigüre edilebilir ve perakendeciler müşteriyi giriş sayfasına veya sitedeki herhangi bir sayfaya geri geçirmesine olanak sağlar.</span><span class="sxs-lookup"><span data-stu-id="fb024-134">The route can be configured at the site level, allowing retailers to take the customer back to the home page or any other page on the site.</span></span>

## <a name="commerce-scale-unit-interaction"></a><span data-ttu-id="fb024-135">Ticari ölçek birim etkileşimi</span><span class="sxs-lookup"><span data-stu-id="fb024-135">Commerce Scale Unit interaction</span></span>

<span data-ttu-id="fb024-136">Sepet modülü, ürün bilgilerini Commerce Scale Unit API'leri kullanarak alır.</span><span class="sxs-lookup"><span data-stu-id="fb024-136">The cart module retrieves product information by using Commerce Scale Unit APIs.</span></span> <span data-ttu-id="fb024-137">Commerce Scale Unit'deki tüm ürün bilgilerini almak için, tarayıcı tanımlama bilgisinden alışveriş sepetinin kodu kullanılır.</span><span class="sxs-lookup"><span data-stu-id="fb024-137">The cart ID from the browser cookie is used to retrieve all the product information from Commerce Scale Unit.</span></span>

## <a name="add-a-cart-module-to-a-page"></a><span data-ttu-id="fb024-138">Sayfaya sepet modülü ekleme</span><span class="sxs-lookup"><span data-stu-id="fb024-138">Add a cart module to a page</span></span>

<span data-ttu-id="fb024-139">Bir yeni sayfaya sepet modülü eklemek ve gerekli özellikleri ayarlamak için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="fb024-139">To add a cart module to a new page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="fb024-140">**Sepet parçası** olarak adlandırılan bir parça oluşturun ve yeni parçaya sepet birimi ekleyin.</span><span class="sxs-lookup"><span data-stu-id="fb024-140">Create a fragment named **Cart fragment**, and add a cart module to the new fragment.</span></span>
1. <span data-ttu-id="fb024-141">Sepet modülüne başlık ekleyin.</span><span class="sxs-lookup"><span data-stu-id="fb024-141">Add a heading to the cart module.</span></span>
1. <span data-ttu-id="fb024-142">Sepet modülüne bir depo seçici modülü ekleyin.</span><span class="sxs-lookup"><span data-stu-id="fb024-142">Add a store selector module to the cart module.</span></span>
1. <span data-ttu-id="fb024-143">Başlık parçasını kaydedin, düzenlemeyi bitirin ve yayımlayın.</span><span class="sxs-lookup"><span data-stu-id="fb024-143">Save the fragment, finish editing, and then publish the fragment.</span></span>
1. <span data-ttu-id="fb024-144">**Sepet şablonu** adlı bir şablon oluşturun ve yeni oluşturduğunuz sepet parçasını ekleyin.</span><span class="sxs-lookup"><span data-stu-id="fb024-144">Create a template named **Cart template**, and add the cart fragment that you just created.</span></span>
1. <span data-ttu-id="fb024-145">Şablonu kaydedin, düzenlemeyi bitirin ve yayımlayın.</span><span class="sxs-lookup"><span data-stu-id="fb024-145">Save the template, finish editing, and then publish the template.</span></span>
1. <span data-ttu-id="fb024-146">Yeni şablonu kullanan bir sayfa oluşturun.</span><span class="sxs-lookup"><span data-stu-id="fb024-146">Create a page that uses the new template.</span></span>
1. <span data-ttu-id="fb024-147">Sayfayı kaydet ve önizleyin.</span><span class="sxs-lookup"><span data-stu-id="fb024-147">Save and preview the page.</span></span>
1. <span data-ttu-id="fb024-148">Sayfayı düzenlemeyi bitirin ve yayımlayın.</span><span class="sxs-lookup"><span data-stu-id="fb024-148">Finish editing the page, and then publish the page.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="fb024-149">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="fb024-149">Additional resources</span></span>

[<span data-ttu-id="fb024-150">Başlangıç paketine genel bakış</span><span class="sxs-lookup"><span data-stu-id="fb024-150">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="fb024-151">Konteyner modülü</span><span class="sxs-lookup"><span data-stu-id="fb024-151">Container module</span></span>](add-container-module.md)

[<span data-ttu-id="fb024-152">Mağaza seçicisi modülü</span><span class="sxs-lookup"><span data-stu-id="fb024-152">Store selector module</span></span>](store-selector.md)

[<span data-ttu-id="fb024-153">Satınalma kutusu modülü</span><span class="sxs-lookup"><span data-stu-id="fb024-153">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="fb024-154">Sepet simgesi modülü</span><span class="sxs-lookup"><span data-stu-id="fb024-154">Cart icon module</span></span>](cart-icon-module.md)

[<span data-ttu-id="fb024-155">Ödeme modülü</span><span class="sxs-lookup"><span data-stu-id="fb024-155">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="fb024-156">Sipariş onayı modülü</span><span class="sxs-lookup"><span data-stu-id="fb024-156">Order confirmation module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="fb024-157">Üst bilgi modülü</span><span class="sxs-lookup"><span data-stu-id="fb024-157">Header module</span></span>](author-header-module.md)

[<span data-ttu-id="fb024-158">Alt bilgi modülü</span><span class="sxs-lookup"><span data-stu-id="fb024-158">Footer module</span></span>](author-footer-module.md)

[<span data-ttu-id="fb024-159">Perakende kanalları için stok kullanılabilirliğini hesaplama</span><span class="sxs-lookup"><span data-stu-id="fb024-159">Calculate inventory availability for retail channels</span></span>](calculated-inventory-retail-channels.md)
