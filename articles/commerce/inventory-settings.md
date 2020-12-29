---
title: Stok ayarlarını uygula
description: Bu konu, stok ayarlarını kapsamaktadır ve Microsoft Dynamics 365 Commerce'ta bunların nasıl uygulanacağını açıklar .
author: anupamar-ms
manager: annbe
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: dfa8b2bdc03e3698feda26932db757421097140d
ms.sourcegitcommit: 4bf5ae2f2f144a28e431ed574c7e8438dc5935de
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/13/2020
ms.locfileid: "4517076"
---
# <a name="apply-inventory-settings"></a><span data-ttu-id="252a1-103">Stok ayarlarını uygula</span><span class="sxs-lookup"><span data-stu-id="252a1-103">Apply inventory settings</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="252a1-104">Bu konu, stok ayarlarını kapsamaktadır ve Microsoft Dynamics 365 Commerce'ta bunların nasıl uygulanacağını açıklar .</span><span class="sxs-lookup"><span data-stu-id="252a1-104">This topic covers inventory settings and describes how to apply them in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="252a1-105">Özet</span><span class="sxs-lookup"><span data-stu-id="252a1-105">Overview</span></span>

<span data-ttu-id="252a1-106">Stok ayarları alışveriş için ürün sepetine eklenmeden önce stokun denetlenip işaretlenmeyeceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="252a1-106">Inventory settings specify whether inventory should be checked before products are added to the cart.</span></span> <span data-ttu-id="252a1-107">Ayrıca, "stokta" ve "yalnızca birkaç soldaki" gibi, stokla ilgili Merchandising iletileri de tanımlarlar.</span><span class="sxs-lookup"><span data-stu-id="252a1-107">They also define inventory-related merchandising messages, such as "In stock" and "Only a few left."</span></span> <span data-ttu-id="252a1-108">Bu ayarlar, ürünün stokta bulunduğu durumda satın alınmamasını sağlar.</span><span class="sxs-lookup"><span data-stu-id="252a1-108">These settings ensure that a product can't be purchased if it's out of stock.</span></span>

<span data-ttu-id="252a1-109">Dynamics 365 Commerce ürünler için eldeki kullanılabilir kullanılabilirlik tahminleri sağlar.</span><span class="sxs-lookup"><span data-stu-id="252a1-109">Dynamics 365 Commerce provides estimates of on-hand availability for products.</span></span> <span data-ttu-id="252a1-110">Tahmini eldeki stok kullanılabilirliğinin nasıl hesaplandığı hakkında bilgi için bkz [perakende kanalları için envanter kullanılabilirliğini hesaplama](calculated-inventory-retail-channels.md).</span><span class="sxs-lookup"><span data-stu-id="252a1-110">For information about how estimated on-hand availability is calculated, see [Calculate inventory availability for retail channels](calculated-inventory-retail-channels.md).</span></span>

<span data-ttu-id="252a1-111">Commerce Site Builder 'da stok eşikleri ve aralıkları bir ürün ya da kategori için tanımlanabilir.</span><span class="sxs-lookup"><span data-stu-id="252a1-111">In Commerce site builder, inventory thresholds and ranges can be defined for a product or a category.</span></span> <span data-ttu-id="252a1-112">Stokta, düşük stokta veya stok dışı olduğu gibi sınıflandırılabileceği belirlenir.</span><span class="sxs-lookup"><span data-stu-id="252a1-112">They determine whether inventory can be classified as in stock, low stock, or out of stock.</span></span> <span data-ttu-id="252a1-113">Ayrıntılar için bkz [Envanter tamponları ve envanter düzeylerini yapılandırma](inventory-buffers-levels.md).</span><span class="sxs-lookup"><span data-stu-id="252a1-113">For details, see [Configure inventory buffers and inventory levels](inventory-buffers-levels.md).</span></span>

> [!NOTE]
> <span data-ttu-id="252a1-114">Stok eşikleri ve aralıkları için destek Dynamics 365 Commerce 10.0.12 sürümünde bulunabilir.</span><span class="sxs-lookup"><span data-stu-id="252a1-114">Support for inventory thresholds and ranges is available in the Dynamics 365 Commerce 10.0.12 release.</span></span>

## <a name="inventory-settings"></a><span data-ttu-id="252a1-115">Envanter ayarları</span><span class="sxs-lookup"><span data-stu-id="252a1-115">Inventory settings</span></span>

<span data-ttu-id="252a1-116">Commerce'da stok ayarları, site oluşturucuda **Site Ayarlar \> Uzantılar \> Envanter yönetimi** tanımlanır .</span><span class="sxs-lookup"><span data-stu-id="252a1-116">In Commerce, inventory settings are defined at **Site Settings \> Extensions \> Inventory Management** in site builder.</span></span> <span data-ttu-id="252a1-117">Dört stok ayarı vardır; bunlardan biri eskidir (kullanım dışı):</span><span class="sxs-lookup"><span data-stu-id="252a1-117">There are four inventory settings, one of which is obsolete (deprecated):</span></span>

- <span data-ttu-id="252a1-118">**Uygulama üzerinde stok denetimini etkinleştir** – Bu ayar, ürün envanteri denetimini açar.</span><span class="sxs-lookup"><span data-stu-id="252a1-118">**Enable stock check in app** – This setting turns on a product inventory check.</span></span> <span data-ttu-id="252a1-119">Mağaza modüllerinde satın alma kutusu, alışveriş sepeti ve çekme için ürün stoğu kontrol edilir ve yalnızca stok varsa alışveriş sepetine bir ürün eklenmesine izin verilir.</span><span class="sxs-lookup"><span data-stu-id="252a1-119">Buy box, cart, and pick up in store modules will then check product inventory, and will allow a product to be added to the cart only if inventory is available.</span></span>
- <span data-ttu-id="252a1-120">**Stok düzeyi temeli** - Bu ayar, stok düzeylerinin nasıl hesaplandığını tanımlar.</span><span class="sxs-lookup"><span data-stu-id="252a1-120">**Inventory level based on** – This setting defines how inventory levels are calculated.</span></span> <span data-ttu-id="252a1-121">Kullanılabilir değerler **Toplam kullanılabilir**, **fiziksel kullanılabilir** ve **stok dışı eşikler** dir.</span><span class="sxs-lookup"><span data-stu-id="252a1-121">The available values are **Total Available**, **Physical Available**, and **Out of stock threshold**.</span></span> <span data-ttu-id="252a1-122">Commerce'da stok eşikleri ve aralıkları her ürün ya da kategori için tanımlanabilir.</span><span class="sxs-lookup"><span data-stu-id="252a1-122">In Commerce, inventory threshold and ranges can be defined for each product and category.</span></span> <span data-ttu-id="252a1-123">Stok API'Leri **Toplam kullanılabilir** özelliğin ve **fiziksel kullanılabilir** özelliğin ürün stok bilgilerini döndürür.</span><span class="sxs-lookup"><span data-stu-id="252a1-123">The inventory APIs return product inventory information for both the **Total Available** property and the **Physical Available** property.</span></span> <span data-ttu-id="252a1-124">Perakende, **kullanılabilen toplam** veya **fiziksel kullanılabilir** değerin stok sayısını ve stokta bulunmayan ve stok dışı durumları için bunlara karşılık gelen aralıkları belirlemek için kullanılabilir olup olmadığına karar verir.</span><span class="sxs-lookup"><span data-stu-id="252a1-124">The retailer decides whether the **Total Available** or **Physical Available** value should be used to determine the inventory count and the corresponding ranges for in-stock and out-of-stock statuses.</span></span>

    <span data-ttu-id="252a1-125">**Stok düzeyi ayar temel alınarak** ayarının **stokta bulunmayan eşik değeri** eski (eski), kullanımdan kalktı değeridir.</span><span class="sxs-lookup"><span data-stu-id="252a1-125">The **Out of stock threshold** value of the **Inventory level based on** setting is an old (legacy), obsolete value.</span></span> <span data-ttu-id="252a1-126">Seçildiği zaman, stok sayımı **Toplam kullanılabilir** değerin sonuçlarından belirlenir , ancak eşik, daha sonra açıklanan **stok dışı eşiği** sayısal ayarı tarafından tanımlanır.</span><span class="sxs-lookup"><span data-stu-id="252a1-126">When it's selected, the inventory count is determined from the results of the **Total Available** value, but the threshold is defined by the **Out of stock threshold** numeric setting that is described later.</span></span> <span data-ttu-id="252a1-127">Bu eşik ayarı bir e-ticaret sitesi içindeki tüm ürünlere uygulanır.</span><span class="sxs-lookup"><span data-stu-id="252a1-127">This threshold setting applies to all products across an e-commerce site.</span></span> <span data-ttu-id="252a1-128">Stok eşik numarasının altındaysa, bir ürün Stokta yer alır.</span><span class="sxs-lookup"><span data-stu-id="252a1-128">If inventory is below the threshold number, a product is considered out of stock.</span></span> <span data-ttu-id="252a1-129">Aksi takdirde stokta olduğu düşünülür.</span><span class="sxs-lookup"><span data-stu-id="252a1-129">Otherwise, it's considered in stock.</span></span> <span data-ttu-id="252a1-130">**Stok dışı eşik** değerinin yetenekleri sınırlıdır ve bunu sürüm 10.0.12 ve sonraki sürümlerde kullanmanızı önermeyiz.</span><span class="sxs-lookup"><span data-stu-id="252a1-130">The capabilities of the **Out of stock threshold** value are limited, and we don't recommend that you use it in version 10.0.12 and later.</span></span>

- <span data-ttu-id="252a1-131">**Stok aralıkları** – Bu ayar, site modüllerinde iletinin gösterildiği stok aralıklarını tanımlar.</span><span class="sxs-lookup"><span data-stu-id="252a1-131">**Inventory ranges** – This setting defines the inventory ranges that message are shown for on site modules.</span></span> <span data-ttu-id="252a1-132">Yalnızca, **Toplam kullanılabilir** değer veya **stok düzeyi ayar temel alınarak** ayarı için **fiziksel kullanılabilir** değer seçildiğinde uygulanabilir.</span><span class="sxs-lookup"><span data-stu-id="252a1-132">It's applicable only if either the **Total Available** value or the **Physical Available** value is selected for the **Inventory level based on** setting.</span></span> <span data-ttu-id="252a1-133">Kullanılabilir değerler **tümü**, **düşük ve stok dışı** ve **Stok dışında**.</span><span class="sxs-lookup"><span data-stu-id="252a1-133">The available values are **All**, **Low and out of stock**, and **Out of stock**.</span></span>

    - <span data-ttu-id="252a1-134">**Tümü** seçildiğinde, tüm stok aralıklarına ait iletiler ("kullanılabilir" iletisiyle) stokta değil ("stok dışı" iletisi) görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="252a1-134">When **All** is selected, messages for all inventory ranges, from in stock ("Available" message) to out of stock ("Out of stock" message), will be shown.</span></span>
    - <span data-ttu-id="252a1-135">**Düşük ve stok dışı** seçildiğinde, tüm stok aralıklarına ait iletiler ("kullanılabilir" iletisiyle) görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="252a1-135">When **Low and out of stock** is selected, messages for all inventory ranges except in stock ("Available" message) will be shown.</span></span>
    - <span data-ttu-id="252a1-136">**Stokta bulunmayan** seçildiğinde , yalnızca "stok dışı" iletisi gösterilir.</span><span class="sxs-lookup"><span data-stu-id="252a1-136">When **Out of stock** is selected, only the "Out of stock" message will be shown.</span></span>

- <span data-ttu-id="252a1-137">**Stok dışı eşiği** – Bu eski sayısal ayar , yalnızca **stok düzeyi ayar temel alınarak** ayarı **stok dışı eşik** değeri seçildiğinde etkili olur.</span><span class="sxs-lookup"><span data-stu-id="252a1-137">**Out of stock threshold** – This old numeric setting will take effect only if the **Out of stock threshold** value is selected for the **Inventory level based on** setting.</span></span>

> [!IMPORTANT] 
> <span data-ttu-id="252a1-138">Bu ayarlar Dynamics 365 Commerce 10.0.12 sürümünde bulunmaktadır.</span><span class="sxs-lookup"><span data-stu-id="252a1-138">These settings are available in the Dynamics 365 Commerce 10.0.12 release.</span></span> <span data-ttu-id="252a1-139">Dynamics 365 Commerce'nin eski sürümlerinden birini güncelleştiriyorsanız, appSettings. json dosyasını el ile güncelleştirmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="252a1-139">If you are updating from an older version of Dynamics 365 Commerce, you must manually update the appsettings.json file.</span></span> <span data-ttu-id="252a1-140">AppSettings.json dosyasını güncelleştirme yönergeleri için bkz. [SDK ve modül kitaplığı güncelleştirmeleri](e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file).</span><span class="sxs-lookup"><span data-stu-id="252a1-140">For instructions on updating the appsettings.json file, see [SDK and module library updates](e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file).</span></span>

## <a name="modules-that-use-inventory-settings"></a><span data-ttu-id="252a1-141">Stok ayarlarını kullanan modüller</span><span class="sxs-lookup"><span data-stu-id="252a1-141">Modules that use inventory settings</span></span>

<span data-ttu-id="252a1-142">Satınalma kutusu, istek listesi, mağaza Seçicisi, sepet ve sepet simgesi modülleri stok aralıklarını ve iletilerini göstermek için stok ayarlarını kullanır.</span><span class="sxs-lookup"><span data-stu-id="252a1-142">Buy box, wishlist, store selector, cart, and cart icon modules use inventory settings to show the inventory ranges and messages.</span></span>

<span data-ttu-id="252a1-143">Aşağıdaki resimde, stok içi ("kullanılabilir") iletiyi gösteren ürün ayrıntıları sayfası (PDP) örneği gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="252a1-143">The following image shows an example of a product details page (PDP) that is showing an in-stock ("Available") message.</span></span>

![Stokta bir ileti bulunan PDP modülü örneği](./media/pdp-InStock.png)

<span data-ttu-id="252a1-145">Aşağıdaki resimde, "stok dışı" iletiyi gösteren PDP örneği gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="252a1-145">The following image shows an example of a PDP that is showing an "Out of stock" message.</span></span>

![Stok dışı bir ileti bulunan PDP modülü örneği](./media/pdp-outofstock.png)

<span data-ttu-id="252a1-147">Aşağıdaki resimde, stokta ("kullanılabilir") iletiyi gösteren sepet örneği gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="252a1-147">The following image shows an example of a cart that is showing an in-stock ("Available") message.</span></span>

![Stokta bir ileti bulunan sepet modülü örneği](./media/cart-instock.png)

## <a name="additional-resources"></a><span data-ttu-id="252a1-149">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="252a1-149">Additional resources</span></span>

[<span data-ttu-id="252a1-150">Modül kitaplığına genel bakış</span><span class="sxs-lookup"><span data-stu-id="252a1-150">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="252a1-151">Stok arabellekleri ve stok düzeyleri yapılandırma</span><span class="sxs-lookup"><span data-stu-id="252a1-151">Configure inventory buffers and inventory levels</span></span>](inventory-buffers-levels.md)

[<span data-ttu-id="252a1-152">Sepet modülü</span><span class="sxs-lookup"><span data-stu-id="252a1-152">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="252a1-153">Satınalma kutusu modülü</span><span class="sxs-lookup"><span data-stu-id="252a1-153">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="252a1-154">Hesap yönetimi sayfaları ve modülleri</span><span class="sxs-lookup"><span data-stu-id="252a1-154">Account management pages and modules</span></span>](account-management.md)

[<span data-ttu-id="252a1-155">Mağaza seçicisi modülü</span><span class="sxs-lookup"><span data-stu-id="252a1-155">Store selector module</span></span>](store-selector.md)

[<span data-ttu-id="252a1-156">SDK ve modül kitaplığı güncelleştirmeleri</span><span class="sxs-lookup"><span data-stu-id="252a1-156">SDK and module library updates</span></span>](e-commerce-extensibility/sdk-updates.md)
