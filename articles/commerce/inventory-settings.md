---
title: Stok ayarlarını uygula
description: Bu konu, stok ayarlarını kapsamaktadır ve Microsoft Dynamics 365 Commerce'ta bunların nasıl uygulanacağını açıklar .
author: anupamar-ms
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
ms.openlocfilehash: 3da447c298993794afa49a0fbaddb1c21cf6231a
ms.sourcegitcommit: dc4898aa32f381620c517bf89c7856e693563ace
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/17/2021
ms.locfileid: "6271317"
---
# <a name="apply-inventory-settings"></a><span data-ttu-id="4b82d-103">Stok ayarlarını uygula</span><span class="sxs-lookup"><span data-stu-id="4b82d-103">Apply inventory settings</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="4b82d-104">Bu konu, stok ayarlarını kapsamaktadır ve Microsoft Dynamics 365 Commerce'ta bunların nasıl uygulanacağını açıklar .</span><span class="sxs-lookup"><span data-stu-id="4b82d-104">This topic covers inventory settings and describes how to apply them in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="4b82d-105">Stok ayarları alışveriş için ürün sepetine eklenmeden önce stokun denetlenip işaretlenmeyeceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="4b82d-105">Inventory settings specify whether inventory should be checked before products are added to the cart.</span></span> <span data-ttu-id="4b82d-106">Ayrıca, "stokta" ve "yalnızca birkaç soldaki" gibi, stokla ilgili Merchandising iletileri de tanımlarlar.</span><span class="sxs-lookup"><span data-stu-id="4b82d-106">They also define inventory-related merchandising messages, such as "In stock" and "Only a few left."</span></span> <span data-ttu-id="4b82d-107">Bu ayarlar, ürünün stokta bulunduğu durumda satın alınmamasını sağlar.</span><span class="sxs-lookup"><span data-stu-id="4b82d-107">These settings ensure that a product can't be purchased if it's out of stock.</span></span>

<span data-ttu-id="4b82d-108">Dynamics 365 Commerce ürünler için eldeki kullanılabilir kullanılabilirlik tahminleri sağlar.</span><span class="sxs-lookup"><span data-stu-id="4b82d-108">Dynamics 365 Commerce provides estimates of on-hand availability for products.</span></span> <span data-ttu-id="4b82d-109">Tahmini eldeki stok kullanılabilirliğinin nasıl hesaplandığı hakkında bilgi için bkz [perakende kanalları için envanter kullanılabilirliğini hesaplama](calculated-inventory-retail-channels.md).</span><span class="sxs-lookup"><span data-stu-id="4b82d-109">For information about how estimated on-hand availability is calculated, see [Calculate inventory availability for retail channels](calculated-inventory-retail-channels.md).</span></span>

<span data-ttu-id="4b82d-110">Commerce Site Builder 'da stok eşikleri ve aralıkları bir ürün ya da kategori için tanımlanabilir.</span><span class="sxs-lookup"><span data-stu-id="4b82d-110">In Commerce site builder, inventory thresholds and ranges can be defined for a product or a category.</span></span> <span data-ttu-id="4b82d-111">Stokta, düşük stokta veya stok dışı olduğu gibi sınıflandırılabileceği belirlenir.</span><span class="sxs-lookup"><span data-stu-id="4b82d-111">They determine whether inventory can be classified as in stock, low stock, or out of stock.</span></span> <span data-ttu-id="4b82d-112">Ayrıntılar için bkz [Envanter tamponları ve envanter düzeylerini yapılandırma](inventory-buffers-levels.md).</span><span class="sxs-lookup"><span data-stu-id="4b82d-112">For details, see [Configure inventory buffers and inventory levels](inventory-buffers-levels.md).</span></span>

> [!NOTE]
> <span data-ttu-id="4b82d-113">Stok eşikleri ve aralıkları için destek Dynamics 365 Commerce 10.0.12 sürümünde bulunabilir.</span><span class="sxs-lookup"><span data-stu-id="4b82d-113">Support for inventory thresholds and ranges is available in the Dynamics 365 Commerce 10.0.12 release.</span></span>

## <a name="inventory-settings"></a><span data-ttu-id="4b82d-114">Envanter ayarları</span><span class="sxs-lookup"><span data-stu-id="4b82d-114">Inventory settings</span></span>

<span data-ttu-id="4b82d-115">Commerce'da stok ayarları, site oluşturucuda **Site Ayarlar \> Uzantılar \> Envanter yönetimi** tanımlanır .</span><span class="sxs-lookup"><span data-stu-id="4b82d-115">In Commerce, inventory settings are defined at **Site Settings \> Extensions \> Inventory Management** in site builder.</span></span> <span data-ttu-id="4b82d-116">Beş stok ayarı vardır; bunlardan biri eskidir (kullanım dışı):</span><span class="sxs-lookup"><span data-stu-id="4b82d-116">There are five inventory settings, one of which is obsolete (deprecated):</span></span>

- <span data-ttu-id="4b82d-117">**Uygulama üzerinde stok denetimini etkinleştir** – Bu ayar, ürün envanteri denetimini açar.</span><span class="sxs-lookup"><span data-stu-id="4b82d-117">**Enable stock check in app** – This setting turns on a product inventory check.</span></span> <span data-ttu-id="4b82d-118">Mağaza modüllerinde satın alma kutusu, alışveriş sepeti ve çekme için ürün stoğu kontrol edilir ve yalnızca stok varsa alışveriş sepetine bir ürün eklenmesine izin verilir.</span><span class="sxs-lookup"><span data-stu-id="4b82d-118">Buy box, cart, and pick up in store modules will then check product inventory, and will allow a product to be added to the cart only if inventory is available.</span></span>
- <span data-ttu-id="4b82d-119">**Stok düzeyi temeli** - Bu ayar, stok düzeylerinin nasıl hesaplandığını tanımlar.</span><span class="sxs-lookup"><span data-stu-id="4b82d-119">**Inventory level based on** – This setting defines how inventory levels are calculated.</span></span> <span data-ttu-id="4b82d-120">Kullanılabilir değerler **Toplam kullanılabilir**, **fiziksel kullanılabilir** ve **stok dışı eşikler** dir.</span><span class="sxs-lookup"><span data-stu-id="4b82d-120">The available values are **Total Available**, **Physical Available**, and **Out of stock threshold**.</span></span> <span data-ttu-id="4b82d-121">Commerce'da stok eşikleri ve aralıkları her ürün ya da kategori için tanımlanabilir.</span><span class="sxs-lookup"><span data-stu-id="4b82d-121">In Commerce, inventory threshold and ranges can be defined for each product and category.</span></span> <span data-ttu-id="4b82d-122">Stok API'Leri **Toplam kullanılabilir** özelliğin ve **fiziksel kullanılabilir** özelliğin ürün stok bilgilerini döndürür.</span><span class="sxs-lookup"><span data-stu-id="4b82d-122">The inventory APIs return product inventory information for both the **Total Available** property and the **Physical Available** property.</span></span> <span data-ttu-id="4b82d-123">Perakende, **kullanılabilen toplam** veya **fiziksel kullanılabilir** değerin stok sayısını ve stokta bulunmayan ve stok dışı durumları için bunlara karşılık gelen aralıkları belirlemek için kullanılabilir olup olmadığına karar verir.</span><span class="sxs-lookup"><span data-stu-id="4b82d-123">The retailer decides whether the **Total Available** or **Physical Available** value should be used to determine the inventory count and the corresponding ranges for in-stock and out-of-stock statuses.</span></span>

    <span data-ttu-id="4b82d-124">**Stok düzeyi ayar temel alınarak** ayarının **stokta bulunmayan eşik değeri** eski (eski), kullanımdan kalktı değeridir.</span><span class="sxs-lookup"><span data-stu-id="4b82d-124">The **Out of stock threshold** value of the **Inventory level based on** setting is an old (legacy), obsolete value.</span></span> <span data-ttu-id="4b82d-125">Seçildiği zaman, stok sayımı **Toplam kullanılabilir** değerin sonuçlarından belirlenir , ancak eşik, daha sonra açıklanan **stok dışı eşiği** sayısal ayarı tarafından tanımlanır.</span><span class="sxs-lookup"><span data-stu-id="4b82d-125">When it's selected, the inventory count is determined from the results of the **Total Available** value, but the threshold is defined by the **Out of stock threshold** numeric setting that is described later.</span></span> <span data-ttu-id="4b82d-126">Bu eşik ayarı bir e-ticaret sitesi içindeki tüm ürünlere uygulanır.</span><span class="sxs-lookup"><span data-stu-id="4b82d-126">This threshold setting applies to all products across an e-commerce site.</span></span> <span data-ttu-id="4b82d-127">Stok eşik numarasının altındaysa, bir ürün Stokta yer alır.</span><span class="sxs-lookup"><span data-stu-id="4b82d-127">If inventory is below the threshold number, a product is considered out of stock.</span></span> <span data-ttu-id="4b82d-128">Aksi takdirde stokta olduğu düşünülür.</span><span class="sxs-lookup"><span data-stu-id="4b82d-128">Otherwise, it's considered in stock.</span></span> <span data-ttu-id="4b82d-129">**Stok dışı eşik** değerinin yetenekleri sınırlıdır ve bunu sürüm 10.0.12 ve sonraki sürümlerde kullanmanızı önermeyiz.</span><span class="sxs-lookup"><span data-stu-id="4b82d-129">The capabilities of the **Out of stock threshold** value are limited, and we don't recommend that you use it in version 10.0.12 and later.</span></span>

- <span data-ttu-id="4b82d-130">**Çoklu ambarlar için stok düzeyi** – Bu ayar, stok düzeyinin varsayılan ambar veya çoklu ambarlara göre hesaplanmasını sağlar.</span><span class="sxs-lookup"><span data-stu-id="4b82d-130">**Inventory level for multiple warehouses** – This setting enables the inventory level to be calculated against the default warehouse or multiple warehouses.</span></span> <span data-ttu-id="4b82d-131">**Tekli ambar seçeneğine göre** seçeneği, stok düzeylerini varsayılan ambara dayalı olarak hesaplar.</span><span class="sxs-lookup"><span data-stu-id="4b82d-131">The **Based on individual warehouse** option will calculate inventory levels based on the default warehouse.</span></span> <span data-ttu-id="4b82d-132">Alternatif olarak bir e-ticaret sitesi, karşılamayı kolaylaştırmak için birden çok ambara işaret edebilir.</span><span class="sxs-lookup"><span data-stu-id="4b82d-132">Alternatively, an e-commerce site can point to multiple warehouses to facilitate fulfillment.</span></span> <span data-ttu-id="4b82d-133">Bu durumda, **Teslimat ve Malzeme Çekme ambarları için toplamaya göre** seçeneği, stok kullanılabilirliğini belirtmek için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="4b82d-133">In that case, the **Based on aggregate for Shipping and Pickup warehouses** option is used to indicate stock availability.</span></span> <span data-ttu-id="4b82d-134">Örneğin, bir müşteri bir öğe satın aldığında ve teslimat modu olarak "sevkiyat" seçeneğini seçtiğinde, söz konusu öğe, karşılama grubundaki kullanılabilir stok bulunan herhangi bir ambardan sevk edilebilir.</span><span class="sxs-lookup"><span data-stu-id="4b82d-134">For example, when a customer purchases an item and selects "shipping" as the delivery mode, the item can be shipped from any warehouse in the fulfillment group that has available inventory.</span></span> <span data-ttu-id="4b82d-135">Ürün ayrıntıları sayfası (PDP), karşılama grubunda herhangi bir kullanılabilir sevkiyat ambarında stok varsa sevkiyat için "Stokta" iletisini gösterecektir.</span><span class="sxs-lookup"><span data-stu-id="4b82d-135">The product details page (PDP) will show an "In stock" message for shipping if any available shipping warehouse in the fulfillment group has inventory.</span></span> 

> [!IMPORTANT] 
> <span data-ttu-id="4b82d-136">**Birden çok ambar için stok düzeyi**, Commerce sürüm 10.0.19'dan itibaren mevcuttur.</span><span class="sxs-lookup"><span data-stu-id="4b82d-136">The **Inventory level for multiple warehouses** setting is available as of the Commerce version 10.0.19 release.</span></span> <span data-ttu-id="4b82d-137">Commerce'ün eski sürümlerinden birini güncelleştiriyorsanız, appsettings.json dosyasını el ile güncelleştirmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="4b82d-137">If you're updating from an older version of Commerce, you must manually update the appsettings.json file.</span></span> <span data-ttu-id="4b82d-138">Talimatlar için bkz. [SDK ve modül kitaplığı güncelleştirmeleri](e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file).</span><span class="sxs-lookup"><span data-stu-id="4b82d-138">For instructions, see [SDK and module library updates](e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file).</span></span>

- <span data-ttu-id="4b82d-139">**Stok aralıkları** – Bu ayar, site modüllerinde iletinin gösterildiği stok aralıklarını tanımlar.</span><span class="sxs-lookup"><span data-stu-id="4b82d-139">**Inventory ranges** – This setting defines the inventory ranges that message are shown for on site modules.</span></span> <span data-ttu-id="4b82d-140">Yalnızca, **Toplam kullanılabilir** değer veya **stok düzeyi ayar temel alınarak** ayarı için **fiziksel kullanılabilir** değer seçildiğinde uygulanabilir.</span><span class="sxs-lookup"><span data-stu-id="4b82d-140">It's applicable only if either the **Total Available** value or the **Physical Available** value is selected for the **Inventory level based on** setting.</span></span> <span data-ttu-id="4b82d-141">Kullanılabilir değerler **tümü**, **düşük ve stok dışı** ve **Stok dışında**.</span><span class="sxs-lookup"><span data-stu-id="4b82d-141">The available values are **All**, **Low and out of stock**, and **Out of stock**.</span></span>

    - <span data-ttu-id="4b82d-142">**Tümü** seçildiğinde, tüm stok aralıklarına ait iletiler ("kullanılabilir" iletisiyle) stokta değil ("stok dışı" iletisi) görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="4b82d-142">When **All** is selected, messages for all inventory ranges, from in stock ("Available" message) to out of stock ("Out of stock" message), will be shown.</span></span>
    - <span data-ttu-id="4b82d-143">**Düşük ve stok dışı** seçildiğinde, tüm stok aralıklarına ait iletiler ("kullanılabilir" iletisiyle) görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="4b82d-143">When **Low and out of stock** is selected, messages for all inventory ranges except in stock ("Available" message) will be shown.</span></span>
    - <span data-ttu-id="4b82d-144">**Stokta bulunmayan** seçildiğinde , yalnızca "stok dışı" iletisi gösterilir.</span><span class="sxs-lookup"><span data-stu-id="4b82d-144">When **Out of stock** is selected, only the "Out of stock" message will be shown.</span></span>

- <span data-ttu-id="4b82d-145">**Stok dışı eşiği** – Bu eski sayısal ayar , yalnızca **stok düzeyi ayar temel alınarak** ayarı **stok dışı eşik** değeri seçildiğinde etkili olur.</span><span class="sxs-lookup"><span data-stu-id="4b82d-145">**Out of stock threshold** – This old numeric setting will take effect only if the **Out of stock threshold** value is selected for the **Inventory level based on** setting.</span></span>

> [!IMPORTANT] 
> <span data-ttu-id="4b82d-146">Bu ayarlar Dynamics 365 Commerce 10.0.12 sürümünde bulunmaktadır.</span><span class="sxs-lookup"><span data-stu-id="4b82d-146">These settings are available in the Dynamics 365 Commerce 10.0.12 release.</span></span> <span data-ttu-id="4b82d-147">Dynamics 365 Commerce'nin eski sürümlerinden birini güncelleştiriyorsanız, appSettings. json dosyasını el ile güncelleştirmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="4b82d-147">If you are updating from an older version of Dynamics 365 Commerce, you must manually update the appsettings.json file.</span></span> <span data-ttu-id="4b82d-148">AppSettings.json dosyasını güncelleştirme yönergeleri için bkz. [SDK ve modül kitaplığı güncelleştirmeleri](e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file).</span><span class="sxs-lookup"><span data-stu-id="4b82d-148">For instructions on updating the appsettings.json file, see [SDK and module library updates](e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file).</span></span>

## <a name="modules-that-use-inventory-settings"></a><span data-ttu-id="4b82d-149">Stok ayarlarını kullanan modüller</span><span class="sxs-lookup"><span data-stu-id="4b82d-149">Modules that use inventory settings</span></span>

<span data-ttu-id="4b82d-150">Satınalma kutusu, istek listesi, mağaza Seçicisi, sepet ve sepet simgesi modülleri stok aralıklarını ve iletilerini göstermek için stok ayarlarını kullanır.</span><span class="sxs-lookup"><span data-stu-id="4b82d-150">Buy box, wishlist, store selector, cart, and cart icon modules use inventory settings to show the inventory ranges and messages.</span></span>

<span data-ttu-id="4b82d-151">Aşağıdaki resimde yer alan örnekte, bir PDP stokta ("Kullanılabilir") iletisini göstermektedir.</span><span class="sxs-lookup"><span data-stu-id="4b82d-151">In the example in the following illustration, a PDP is showing an in-stock ("Available") message.</span></span>

![Stokta bir ileti bulunan PDP modülü örneği](./media/pdp-InStock.png)

<span data-ttu-id="4b82d-153">Aşağıdaki resimde yer alan örnekte, bir PDP "Stokta yok" iletisini göstermektedir.</span><span class="sxs-lookup"><span data-stu-id="4b82d-153">In the example in the following illustration, a PDP is showing an "Out of stock" message.</span></span>

![Stok dışı bir ileti bulunan PDP modülü örneği](./media/pdp-outofstock.png)

<span data-ttu-id="4b82d-155&quot;>Aşağıdaki resimde yer alan örnekte, bir sepet stokta (&quot;Kullanılabilir") iletisini göstermektedir.</span><span class="sxs-lookup"><span data-stu-id="4b82d-155">In the example in the following illustration, a cart is showing an in-stock ("Available") message.</span></span>

![Stokta bir ileti bulunan sepet modülü örneği](./media/cart-instock.png)

## <a name="additional-resources"></a><span data-ttu-id="4b82d-157">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="4b82d-157">Additional resources</span></span>

[<span data-ttu-id="4b82d-158">Modül kitaplığına genel bakış</span><span class="sxs-lookup"><span data-stu-id="4b82d-158">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="4b82d-159">Stok arabellekleri ve stok düzeyleri yapılandırma</span><span class="sxs-lookup"><span data-stu-id="4b82d-159">Configure inventory buffers and inventory levels</span></span>](inventory-buffers-levels.md)

[<span data-ttu-id="4b82d-160">Sepet modülü</span><span class="sxs-lookup"><span data-stu-id="4b82d-160">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="4b82d-161">Satınalma kutusu modülü</span><span class="sxs-lookup"><span data-stu-id="4b82d-161">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="4b82d-162">Hesap yönetimi sayfaları ve modülleri</span><span class="sxs-lookup"><span data-stu-id="4b82d-162">Account management pages and modules</span></span>](account-management.md)

[<span data-ttu-id="4b82d-163">Mağaza seçicisi modülü</span><span class="sxs-lookup"><span data-stu-id="4b82d-163">Store selector module</span></span>](store-selector.md)

[<span data-ttu-id="4b82d-164">SDK ve modül kitaplığı güncelleştirmeleri</span><span class="sxs-lookup"><span data-stu-id="4b82d-164">SDK and module library updates</span></span>](e-commerce-extensibility/sdk-updates.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
