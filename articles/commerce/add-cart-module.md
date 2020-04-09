---
title: Sepet modülü
description: Bu konu sepet modüllerini kapsamaktadır ve Microsoft Dynamics 365 Commerce'un site sayfalarına nasıl ekleneceğini açıklamaktadır.
author: anupamar-ms
manager: annbe
ms.date: 03/19/2020
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
ms.openlocfilehash: 598b35b1bd365e761d8d4c5ef214935e60b971f4
ms.sourcegitcommit: de5af1912201dd70aa85fdcad0b184c42405802e
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/21/2020
ms.locfileid: "3154029"
---
# <a name="cart-module"></a><span data-ttu-id="b39f1-103">Sepet modülü</span><span class="sxs-lookup"><span data-stu-id="b39f1-103">Cart module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="b39f1-104">Bu konu sepet modüllerini kapsamaktadır ve Microsoft Dynamics 365 Commerce'un site sayfalarına nasıl ekleneceğini açıklamaktadır.</span><span class="sxs-lookup"><span data-stu-id="b39f1-104">This topic covers cart modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="b39f1-105">Özet</span><span class="sxs-lookup"><span data-stu-id="b39f1-105">Overview</span></span>

<span data-ttu-id="b39f1-106">Bir sepet modülü, müşteri kullanıma devam etmeden önce alışveriş sepetine eklenen maddeleri göstermek için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="b39f1-106">A cart module shows the items that have been added to the cart before the customer proceeds to checkout.</span></span> <span data-ttu-id="b39f1-107">Ayrıca, modül sipariş özeti gösterir ve müşterinin promosyon kodları uygulamasını veya kaldırmasını sağlar.</span><span class="sxs-lookup"><span data-stu-id="b39f1-107">The module also shows an order summary and lets the customer apply or remove promotional codes.</span></span>

<span data-ttu-id="b39f1-108">Sepet modülü, oturum açan kullanıma alma ve konuk kullanıma almayı destekler.</span><span class="sxs-lookup"><span data-stu-id="b39f1-108">The cart module supports signed-in checkout and guest checkout.</span></span> <span data-ttu-id="b39f1-109">Ayrıca bir **Alışverişe geri git** bağlantısı da destekler.</span><span class="sxs-lookup"><span data-stu-id="b39f1-109">It also supports a **Back to shopping** link.</span></span> <span data-ttu-id="b39f1-110">Bu bağlantı için yolu **Site Ayarları \> Uzantılar \> Rotalar** adresinden yapılandırabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="b39f1-110">You can configure the route for this link at **Site Settings \> Extensions \> Routes**.</span></span>

<span data-ttu-id="b39f1-111">Sepet modülü, tüm sitede kullanılabilen bir tarayıcı tanımlama bilgisi olan sepet kimliğine göre verileri işler.</span><span class="sxs-lookup"><span data-stu-id="b39f1-111">The cart module renders data based on the cart ID, which is a browser cookie available throughout the site.</span></span>

## <a name="cart-module-properties-and-slots"></a><span data-ttu-id="b39f1-112">Sepet modülü özelliklerini ve yuvaları</span><span class="sxs-lookup"><span data-stu-id="b39f1-112">Cart module properties and slots</span></span>

<span data-ttu-id="b39f1-113">Sepet modülü bir **Başlık** özelliğine sahiptir ve bu **Alışveriş sepeti** ve **Sepetinizdeki öğeler** gibi değerlere ayarlanabilir.</span><span class="sxs-lookup"><span data-stu-id="b39f1-113">The cart module has a **Heading** property that can be set to values such as **Shopping bag** and **Items in your cart**.</span></span> 

## <a name="modules-that-can-be-used-in-a-cart-module"></a><span data-ttu-id="b39f1-114">Sepet modülünde kullanılabilen modüller</span><span class="sxs-lookup"><span data-stu-id="b39f1-114">Modules that can be used in a cart module</span></span>

- <span data-ttu-id="b39f1-115">**Metin bloğu** – bu modül sepet modülündeki özel iletileri destekler.</span><span class="sxs-lookup"><span data-stu-id="b39f1-115">**Text block** – This module supports custom messaging in the cart module.</span></span> <span data-ttu-id="b39f1-116">İletiler, içerik yönetim sistemi (CMS) tarafından çalıştırılır.</span><span class="sxs-lookup"><span data-stu-id="b39f1-116">The messages are driven by the content management system (CMS).</span></span> <span data-ttu-id="b39f1-117">"Siparişinizdeki sorunları için 1-800-Fabrikam ile iletişim" gibi herhangi bir ileti eklenebilir.</span><span class="sxs-lookup"><span data-stu-id="b39f1-117">Any message can be added, such as "For issues with your order, contact 1-800-Fabrikam."</span></span>
- <span data-ttu-id="b39f1-118">**Mağaza seçici** - Bu modül bir maddenin almak için kullanılabilir olduğu yakındaki mağazaların listesini gösterir.</span><span class="sxs-lookup"><span data-stu-id="b39f1-118">**Store selector** – This module shows a list of nearby stores where an item is available for pickup.</span></span> <span data-ttu-id="b39f1-119">Kullanıcıların yakındaki mağazaları bulabilmesi için bir konum girmesini sağlar.</span><span class="sxs-lookup"><span data-stu-id="b39f1-119">It lets users enter a location to find stores that are nearby.</span></span> <span data-ttu-id="b39f1-120">Bu modülle ilgili daha fazla bilgi için bkz. [Mağaza seçme modülü](store-selector.md).</span><span class="sxs-lookup"><span data-stu-id="b39f1-120">For more information on this module, see [Store Selector module](store-selector.md).</span></span>

## <a name="cart-module-settings"></a><span data-ttu-id="b39f1-121">Sepet modülü ayarları</span><span class="sxs-lookup"><span data-stu-id="b39f1-121">Cart module settings</span></span>

<span data-ttu-id="b39f1-122">Sepet modülleri, **Site Ayarları \> Uzantılar** üzerinden yapılandırılabilir:</span><span class="sxs-lookup"><span data-stu-id="b39f1-122">Cart modules have the following settings that can be configured at **Site Settings \> Extensions**:</span></span>

- <span data-ttu-id="b39f1-123">**Maksimum miktar** - Bu özellik, alışveriş sepetine eklenebilecek maksimum madde sayısını belirtmekte kullanılır.</span><span class="sxs-lookup"><span data-stu-id="b39f1-123">**Maximum quantity** – This property is used to specify the maximum number of each item that can be added to the cart.</span></span> <span data-ttu-id="b39f1-124">Örneğin, bir perakende satılan her ürünün yalnızca 10 tanesi tek bir harekette satılabilir olduğuna karar verebilir.</span><span class="sxs-lookup"><span data-stu-id="b39f1-124">For example, a retailer might decide that only 10 of each product can be sold in a single transaction.</span></span>
- <span data-ttu-id="b39f1-125">**Stok denetimi** – değer **doğru** olarak ayarlandığında, yalnızca satın alma kutusu modülü stokta olduğundan emin olduktan sonra alışveriş sepetine bir madde eklenir.</span><span class="sxs-lookup"><span data-stu-id="b39f1-125">**Inventory check** – When the value is set to **True**, an item is added to the cart only after the buy box module makes sure that it's in stock.</span></span> <span data-ttu-id="b39f1-126">Bu stok denetimi hem maddenin sevk edileceği senaryolar için, hem de mağazada yer alacak senaryolar için gerçekleştirilir.</span><span class="sxs-lookup"><span data-stu-id="b39f1-126">This inventory check is done for scenarios where the item will be shipped and for scenarios where it will be picked up in the store.</span></span> <span data-ttu-id="b39f1-127">Değer **yanlış** olarak ayarlandığında, bir madde alışveriş sepetine eklenmeden önce hiçbir stok denetimi yapılmaz ve sipariş yerleştirilir.</span><span class="sxs-lookup"><span data-stu-id="b39f1-127">If the value is set to **False**, no inventory check is done before an item is added to the cart and the order is placed.</span></span>
- <span data-ttu-id="b39f1-128">**Stok tamponu** – Bu özellik, stok için bir tampon numarası belirtmek için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="b39f1-128">**Inventory buffer** – This property is used to specify a buffer number for inventory.</span></span> <span data-ttu-id="b39f1-129">Gerçek zamanlı olarak sürdürülür ve birçok müşteri sipariş yerleştirirken, doğru stok sayımının korunması zor olabilir.</span><span class="sxs-lookup"><span data-stu-id="b39f1-129">Inventory is maintained in real time, and when many customers place orders, it can be difficult to maintain an accurate inventory count.</span></span> <span data-ttu-id="b39f1-130">Bir stok denetimi yapıldığında, stok tampon tutardan azsa, ürün Stokta tükenmiş olarak kabul edilir.</span><span class="sxs-lookup"><span data-stu-id="b39f1-130">When an inventory check is done, if the inventory is less than the buffer amount, the product is treated as out of stock.</span></span> <span data-ttu-id="b39f1-131">Bu nedenle, stok sayımı tam olarak eşitlenmemesi için çeşitli kanallarda hızlı şekilde satış gerçekleştiğinde, stokta olmayan bir maddenin satılması için daha az risk vardır.</span><span class="sxs-lookup"><span data-stu-id="b39f1-131">Therefore, when sales occur quickly through several channels, and the inventory count isn't fully synced, there is less risk that an item that is out of stock will be sold.</span></span>
- <span data-ttu-id="b39f1-132">**Alışverişe dön** – Bu özellik, **alışverişe geri dön** bağlantısına ait rotayı belirtmek için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="b39f1-132">**Back to shopping** – This property is used to specify the route for the **Back to shopping** link.</span></span> <span data-ttu-id="b39f1-133">Rota, Tesis düzeyinde konfigüre edilebilir ve perakendeciler müşteriyi giriş sayfasına veya sitedeki herhangi bir sayfaya geri geçirmesine olanak sağlar.</span><span class="sxs-lookup"><span data-stu-id="b39f1-133">The route can be configured at the site level, allowing retailers to take the customer back to the home page or any other page on the site.</span></span>

## <a name="commerce-scale-unit-interaction"></a><span data-ttu-id="b39f1-134">Ticari ölçek birim etkileşimi</span><span class="sxs-lookup"><span data-stu-id="b39f1-134">Commerce Scale Unit interaction</span></span>

<span data-ttu-id="b39f1-135">Sepet modülü, ürün bilgilerini Commerce Scale Unit API'leri kullanarak alır.</span><span class="sxs-lookup"><span data-stu-id="b39f1-135">The cart module retrieves product information by using Commerce Scale Unit APIs.</span></span> <span data-ttu-id="b39f1-136">Commerce Scale Unit'deki tüm ürün bilgilerini almak için, tarayıcı tanımlama bilgisinden alışveriş sepetinin kodu kullanılır.</span><span class="sxs-lookup"><span data-stu-id="b39f1-136">The cart ID from the browser cookie is used to retrieve all the product information from Commerce Scale Unit.</span></span>

## <a name="add-a-cart-module-to-a-page"></a><span data-ttu-id="b39f1-137">Sayfaya sepet modülü ekleme</span><span class="sxs-lookup"><span data-stu-id="b39f1-137">Add a cart module to a page</span></span>

<span data-ttu-id="b39f1-138">Bir yeni sayfaya sepet modülü eklemek ve gerekli özellikleri ayarlamak için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="b39f1-138">To add a cart module to a new page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="b39f1-139">**Sepet parçası** olarak adlandırılan bir parça oluşturun ve yeni parçaya sepet birimi ekleyin.</span><span class="sxs-lookup"><span data-stu-id="b39f1-139">Create a fragment named **Cart fragment**, and add a cart module to the new fragment.</span></span>
1. <span data-ttu-id="b39f1-140">Sepet modülüne başlık ekleyin.</span><span class="sxs-lookup"><span data-stu-id="b39f1-140">Add a heading to the cart module.</span></span>
1. <span data-ttu-id="b39f1-141">Sepet modülüne bir depo seçici modülü ekleyin.</span><span class="sxs-lookup"><span data-stu-id="b39f1-141">Add a store selector module to the cart module.</span></span>
1. <span data-ttu-id="b39f1-142">Başlık parçasını kaydedin, düzenlemeyi bitirin ve yayımlayın.</span><span class="sxs-lookup"><span data-stu-id="b39f1-142">Save the fragment, finish editing, and then publish the fragment.</span></span>
1. <span data-ttu-id="b39f1-143">**Sepet şablonu** adlı bir şablon oluşturun ve yeni oluşturduğunuz sepet parçasını ekleyin.</span><span class="sxs-lookup"><span data-stu-id="b39f1-143">Create a template named **Cart template**, and add the cart fragment that you just created.</span></span>
1. <span data-ttu-id="b39f1-144">Şablonu kaydedin, düzenlemeyi bitirin ve yayımlayın.</span><span class="sxs-lookup"><span data-stu-id="b39f1-144">Save the template, finish editing, and then publish the template.</span></span>
1. <span data-ttu-id="b39f1-145">Yeni şablonu kullanan bir sayfa oluşturun.</span><span class="sxs-lookup"><span data-stu-id="b39f1-145">Create a page that uses the new template.</span></span>
1. <span data-ttu-id="b39f1-146">Sayfayı kaydet ve önizleyin.</span><span class="sxs-lookup"><span data-stu-id="b39f1-146">Save and preview the page.</span></span>
1. <span data-ttu-id="b39f1-147">Sayfayı düzenlemeyi bitirin ve yayımlayın.</span><span class="sxs-lookup"><span data-stu-id="b39f1-147">Finish editing the page, and then publish the page.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="b39f1-148">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="b39f1-148">Additional resources</span></span>

[<span data-ttu-id="b39f1-149">Başlangıç paketine genel bakış</span><span class="sxs-lookup"><span data-stu-id="b39f1-149">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="b39f1-150">Konteyner modülü</span><span class="sxs-lookup"><span data-stu-id="b39f1-150">Container module</span></span>](add-container-module.md)

[<span data-ttu-id="b39f1-151">Mağaza seçicisi modülü</span><span class="sxs-lookup"><span data-stu-id="b39f1-151">Store selector module</span></span>](store-selector.md)

[<span data-ttu-id="b39f1-152">Satınalma kutusu modülü</span><span class="sxs-lookup"><span data-stu-id="b39f1-152">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="b39f1-153">Ödeme modülü</span><span class="sxs-lookup"><span data-stu-id="b39f1-153">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="b39f1-154">Sipariş onayı modülü</span><span class="sxs-lookup"><span data-stu-id="b39f1-154">Order confirmation module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="b39f1-155">Üst bilgi modülü</span><span class="sxs-lookup"><span data-stu-id="b39f1-155">Header module</span></span>](author-header-module.md)

[<span data-ttu-id="b39f1-156">Alt bilgi modülü</span><span class="sxs-lookup"><span data-stu-id="b39f1-156">Footer module</span></span>](author-footer-module.md)
