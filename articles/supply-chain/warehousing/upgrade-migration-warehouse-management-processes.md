---
title: "Ürün ve ambar yönetimi AX 2012'den Finance and Operations'a geçirme"
description: "Bu konu, ürün ve ambar yönetimi geçiş seçenekleri hakkında bilgi sağlar."
author: perlynne
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: InventLocationWHSProcessEnablement, WHSLocationProfile, InventTableStorageDimensionGroupChange, InventUpdateBlockedItem, WHSParameters, WHSReservationHierarchy, WHSUOMSeqGroupTable
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.custom: 1714054
ms.assetid: 79a1a3b9-3a36-4162-8839-ec39b5e26602
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 7c6d40e3b80a0974c722ad3a88a29adc8dedf585
ms.contentlocale: tr-tr
ms.lasthandoff: 11/03/2017

---

# <a name="migrate-products-and-warehouse-management-from-ax-2012-to-finance-and-operations"></a><span data-ttu-id="3ef91-103">Ürün ve ambar yönetimi AX 2012'den Finance and Operations'a geçirme</span><span class="sxs-lookup"><span data-stu-id="3ef91-103">Migrate products and warehouse management from AX 2012 to Finance and Operations</span></span>

<span data-ttu-id="3ef91-104">Bu konu Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition içindeki ürün ve ambar yönetimi taşıma seçeneklerine genel bir bakış sağlar.</span><span class="sxs-lookup"><span data-stu-id="3ef91-104">This topic provides an overview of the product and warehouse management migration options within Microsoft Dynamics 365 for Finance and Operations, Enterprise edition.</span></span>

<a name="introduction"></a><span data-ttu-id="3ef91-105">Giriş</span><span class="sxs-lookup"><span data-stu-id="3ef91-105">Introduction</span></span>
------------

<span data-ttu-id="3ef91-106">Finance and Operations'a yükseltme sırasında, ayarları Finance and Operations'daki depolama boyutu grubu ayarlarıyla eşleşmeyen bir depolama boyutu grubuyla ilişkilendirilmiş olması durumunda ürünler bloke edilir.</span><span class="sxs-lookup"><span data-stu-id="3ef91-106">During an upgrade to Finance and Operations, products are blocked if they are associated with a storage dimension group that has settings that don't match the requirements for storage dimension group settings in Finance and Operations.</span></span> <span data-ttu-id="3ef91-107">Ancak, yükseltmenin ardından, yükseltmek sırasında engellenen ürünlerin engelini kaldırmak için **Maddeler için depolama boyutu grubunu değiştir** işlemindeki geçiş seçenekleri kümesini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="3ef91-107">However, after the upgrade, you can use a set of migration options in the **Change storage dimension group for items** process to unblock products that were blocked during upgrade.</span></span> <span data-ttu-id="3ef91-108">Bu ürünler için hareketleri daha sonra işleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="3ef91-108">You can then process transactions for those products.</span></span> <span data-ttu-id="3ef91-109">Maddelerinizin bazıları zaten Tesis, Ambar ve Yerleşim stok boyutlarının etkin olduğu ve fiziksel olarak takip edildiği depolama boyutu gruplarıyla ilişkilendirilmiş olabilir.</span><span class="sxs-lookup"><span data-stu-id="3ef91-109">Some of your items might already be associated with storage dimension groups where the Site, Warehouse, and Location inventory dimensions are active and physically tracked.</span></span> <span data-ttu-id="3ef91-110">Bu durumda, **Maddeler için depolama boyutu grubunu değiştir** işlemini kullanarak bu maddeleri ambar yönetimi işlemlerinde kullanılmak üzere etkinleştirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="3ef91-110">In this case, you can use the **Change storage dimension group for items** process to enable those items to be used in warehouse management processes.</span></span> <span data-ttu-id="3ef91-111">Mevcut maddeler için ambar yönetimi işlevlerini kullanmak istiyorsanız, bu özellik yararlıdır.</span><span class="sxs-lookup"><span data-stu-id="3ef91-111">This feature is useful if you want to use the warehouse management functionality for existing items.</span></span>

## <a name="upgrading-to-finance-and-operations-when-ax-2012-r3-wmsii-is-used"></a><span data-ttu-id="3ef91-112">AX 2012 R3 WMSII kullanıldığında, Finance and Operations'a yükseltme</span><span class="sxs-lookup"><span data-stu-id="3ef91-112">Upgrading to Finance and Operations, when AX 2012 R3 WMSII is used</span></span>
<span data-ttu-id="3ef91-113">Finance and Operations, artık Microsoft Dynamics AX 2012'deki eski **WMSII** modülünü desteklememektedir.</span><span class="sxs-lookup"><span data-stu-id="3ef91-113">Finance and Operations, no longer supports the legacy **WMSII** module from Microsoft Dynamics AX 2012.</span></span> <span data-ttu-id="3ef91-114">Bunun yerine, yeni **Ambar yönetimi** modülünü kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="3ef91-114">Instead, you can use the new **Warehouse management** module.</span></span> <span data-ttu-id="3ef91-115">Önceki sürümlerde, mali stok için Yerleşim ve Palet kodu stok boyutları seçilebilirdi.</span><span class="sxs-lookup"><span data-stu-id="3ef91-115">In previous versions, the Location and Pallet ID inventory dimensions could be selected for financial inventory.</span></span> <span data-ttu-id="3ef91-116">Bununla birlikte, yükseltme işleminin bir parçası olarak, Paket kodu stok boyutu artık mali stok için etkinleştirilemez.</span><span class="sxs-lookup"><span data-stu-id="3ef91-116">However, as part of the upgrade process, the Pallet ID inventory dimension can no longer be enabled for financial inventory.</span></span> <span data-ttu-id="3ef91-117">Palet Kodu stok boyutunu kullanan depolama boyut grubuyla ilişkilendirilmiş tüm ürünleri engellenir ve işlenmez.</span><span class="sxs-lookup"><span data-stu-id="3ef91-117">All products that are associated with a storage dimension group that uses the Pallet ID inventory dimension will be blocked and won't be processed.</span></span>

### <a name="enabling-items-in-finance-and-operations"></a><span data-ttu-id="3ef91-118">Finance and Operations'da maddeleri etkinleştirme</span><span class="sxs-lookup"><span data-stu-id="3ef91-118">Enabling items in Finance and Operations</span></span>

<span data-ttu-id="3ef91-119">Finance and Operations'da, ambar yönetimi işlemlerinin parçası olarak kullanılacak maddelerin **Ambar yönetimi işlemlerini kullan** parametresinin seçili olduğu bir depolama boyutu grubuyla ilişkilendirilmiş olması gerekir.</span><span class="sxs-lookup"><span data-stu-id="3ef91-119">In Finance and Operations, items that will be used as part of warehouse management processes must be associated with a storage dimension group where the **Use warehouse management processes** parameter is selected.</span></span> <span data-ttu-id="3ef91-120">Bu ayar seçildiğinde Tesis, Ambar, Stok durumunu, Yerleşim ve Plaka stok boyutları etkinleşir.</span><span class="sxs-lookup"><span data-stu-id="3ef91-120">When this setting is selected, the Site, Warehouse, Inventory status, Location, and License plate inventory dimensions become active.</span></span> <span data-ttu-id="3ef91-121">Bu tür depolama boyutu grubunu yalnızca zaten Yerleşim stok boyutu etkinleştirilmiş olan depolama boyutu gruplarıyla ilişkilendirilmiş olan maddeler için kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="3ef91-121">You can change to this type of storage dimension group only for items that are already associated with storage dimension groups where the Location inventory dimension is active.</span></span>

### <a name="items-that-are-blocked-for-inventory-updates"></a><span data-ttu-id="3ef91-122">Stok güncelleştirmeleri için engellenen maddeler</span><span class="sxs-lookup"><span data-stu-id="3ef91-122">Items that are blocked for inventory updates</span></span>

<span data-ttu-id="3ef91-123">Yükseltme sırasında engellenen ve işlenemeyen serbest bırakılan ürünlerin listesini görüntülemek için **Stok Yönetimi** &gt; **Kurulum** &gt; **Stok** &gt; **Stok güncelleştirmeleri için engellenen maddeler**'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="3ef91-123">To view the list of released products that were blocked during upgrade and can't be processed, click **Inventory management** &gt; **Setup** &gt; **Inventory** &gt; **Items blocked for inventory updates**.</span></span>

### <a name="reapplying-blocked-products"></a><span data-ttu-id="3ef91-124">Engellenen ürünleri yeniden uygulama</span><span class="sxs-lookup"><span data-stu-id="3ef91-124">Reapplying blocked products</span></span>

<span data-ttu-id="3ef91-125">Yükseltme sırasında engellenen ürünlerin engelini kaldırmak üzere ürünler için yeni bir depolama boyut grubunu seçmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="3ef91-125">To unblock products that were blocked during upgrade, you must select a new storage dimension group for the products.</span></span> <span data-ttu-id="3ef91-126">Açık stok hareketleri olsa bile depolama boyutu grubunu değiştirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="3ef91-126">Note that you can change the storage dimension group even if open inventory transactions exist.</span></span> <span data-ttu-id="3ef91-127">Yükseltme sırasında engellenen öğeleri kullanmak için iki seçeneğiniz vardır:</span><span class="sxs-lookup"><span data-stu-id="3ef91-127">To use items that were blocked during upgrade, you have two options:</span></span>

-   <span data-ttu-id="3ef91-128">Madde için depolama boyut grubunu yalnızca Tesis, Ambar ve Yerleşim stok boyutlarını kullanan bir depolama boyutu grubuyla değiştirin.</span><span class="sxs-lookup"><span data-stu-id="3ef91-128">Change the storage dimension group for the item to a storage dimension group that uses only the Site, Warehouse, and Location inventory dimensions.</span></span> <span data-ttu-id="3ef91-129">Bu değişikliğin bir sonucu olarak Palet Kodu stok boyutu artık kullanılmamaktadır.</span><span class="sxs-lookup"><span data-stu-id="3ef91-129">As a result of this change, the Pallet ID inventory dimension is no longer used.</span></span>
-   <span data-ttu-id="3ef91-130">Madde için depolama boyut grubunu ambar yönetimi işlemlerini kullanan bir depolama boyutu grubuyla değiştirin.</span><span class="sxs-lookup"><span data-stu-id="3ef91-130">Change the storage dimension group for the item to a storage dimension group that uses the warehouse management processes.</span></span> <span data-ttu-id="3ef91-131">Bu değişikliğin bir sonucu olarak artık Plaka stok boyutu kullanılmaktadır.</span><span class="sxs-lookup"><span data-stu-id="3ef91-131">As a result of this change, the License plate inventory dimension is now used.</span></span>

### <a name="migration-processes"></a><span data-ttu-id="3ef91-132">Taşıma işlemleri</span><span class="sxs-lookup"><span data-stu-id="3ef91-132">Migration processes</span></span>

<span data-ttu-id="3ef91-133">Finance and Operations'da madde izleme ambar yönetimi işlemlerinin bir parçasıdır.</span><span class="sxs-lookup"><span data-stu-id="3ef91-133">In Finance and Operations, item tracking is part of the warehouse management processes.</span></span> <span data-ttu-id="3ef91-134">Bu işlemler için tüm ambarların ve yerleşimlerinin bir yerleşim profiliyle eşleştirilmesi gerekir.</span><span class="sxs-lookup"><span data-stu-id="3ef91-134">For these processes, all warehouses and their locations must be associated with a location profile.</span></span> <span data-ttu-id="3ef91-135">Ambar yönetimi işlemlerini kullanmak istiyorsanız, kavramsal olarak, iki işlemin ele alınması gerekir:</span><span class="sxs-lookup"><span data-stu-id="3ef91-135">Conceptually, if you want to use warehouse management processes, two processes must be handled:</span></span>

-   <span data-ttu-id="3ef91-136">Mevcut ambarlar ambar yönetimi süreçlerini kullanmak üzere etkinleştirilmelidir.</span><span class="sxs-lookup"><span data-stu-id="3ef91-136">Existing warehouses must be enabled to use warehouse management processes.</span></span>
-   <span data-ttu-id="3ef91-137">Mevcut serbest bırakılan ürünler, ambar yönetimi işlemlerini kullanan yeni bir depolama boyutu grubu ile ilişkilendirilmelidir.</span><span class="sxs-lookup"><span data-stu-id="3ef91-137">Existing released products must be associated with a new storage dimension group that uses warehouse management processes.</span></span>

<span data-ttu-id="3ef91-138">Kaynak depolama boyut grupları Palet Kodu stok boyutunu kullanıyorsa, Palet Kodu stok boyutunu kullanan mevcut eldeki stokların konumları **Plaka izlemeyi kullan** parametresinin seçili olduğu bir yerleşim profiliyle ilişkilendirilmelidir.</span><span class="sxs-lookup"><span data-stu-id="3ef91-138">If the source storage dimension groups use the Pallet ID inventory dimension, the locations of existing on-hand inventory that used the Pallet ID inventory dimension must be associated with a location profile where the **Use license plate tracking** parameter is selected.</span></span> <span data-ttu-id="3ef91-139">Mevcut ambarların ambar yönetimi işlemlerini kullanmak üzere etkinleştirilmemesi gerekiyorsa, mevcut eldeki stok depolama boyutu gruplarını yalnızca Tesis, Ambar ve Yerleşim stok boyutlarını işleyen gruplarla değiştirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="3ef91-139">If the existing warehouses should not be enabled to use warehouse management processes, you can change the storage dimension groups of the existing on-hand inventory to groups that handle only the Site, Warehouse, and Location inventory dimensions.</span></span>

### <a name="using-the-warehouse-management-processes"></a><span data-ttu-id="3ef91-140">Ambar yönetimi süreçlerini kullanma</span><span class="sxs-lookup"><span data-stu-id="3ef91-140">Using the warehouse management processes</span></span>

<span data-ttu-id="3ef91-141">**Ambar yönetimi** modülünde serbest bırakılan ürünleri kullanabilmeniz için ürünlerin **Ambar yönetimi işlemlerini kullan** parametresinin seçili olduğu bir depolama boyutu kullanması gerekir.</span><span class="sxs-lookup"><span data-stu-id="3ef91-141">Before you can use released products in the **Warehouse management** module, the products must use a storage dimension group where the **Use warehouse management processes** parameter is selected.</span></span>

#### <a name="enable-warehouses-to-use-warehouse-management-processes"></a><span data-ttu-id="3ef91-142">Ambarları ambar yönetimi süreçlerini kullanmak üzere etkinleştirme</span><span class="sxs-lookup"><span data-stu-id="3ef91-142">Enable warehouses to use warehouse management processes</span></span>

1.  <span data-ttu-id="3ef91-143">En az bir yeni konum profili oluşturun.</span><span class="sxs-lookup"><span data-stu-id="3ef91-143">Create at least one new location profile.</span></span>
2.  <span data-ttu-id="3ef91-144">**Ambar yönetimi** &gt; **Kurulum** &gt; **Ambar yönetimi işlemlerini etkinleştir** &gt; **Ambar kurulumunu etkinleştir**'i tıklayın.</span><span class="sxs-lookup"><span data-stu-id="3ef91-144">Click **Warehouse management** &gt; **Setup** &gt; **Enable warehouse management processes** &gt; **Enable warehouse setup**.</span></span>
3.  <span data-ttu-id="3ef91-145">**Ambar kurulumunu etkinleştir** sayfasında, etkinleştirilmesi gereken ambarları ekleyin.</span><span class="sxs-lookup"><span data-stu-id="3ef91-145">On the **Enable warehouse setup** page, add the warehouses that should be enabled.</span></span> <span data-ttu-id="3ef91-146">Bu adımı doğrudan sayfadan veya Microsoft Office tümleştirme kullanarak gerçekleştirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="3ef91-146">You can complete this step either directly on the page or by using the Microsoft Office integration.</span></span>
4.  <span data-ttu-id="3ef91-147">Tüm yerleşimlere yerleşim profili atayın.</span><span class="sxs-lookup"><span data-stu-id="3ef91-147">Assign a location profile to all the locations.</span></span> <span data-ttu-id="3ef91-148">Bu adımı kolaylıkla Microsoft Office tümleştirmeyi doğrudan sayfadan kullanarak gerçekleştirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="3ef91-148">You can easily complete this step by using the Microsoft Office integration directly from the page.</span></span> <span data-ttu-id="3ef91-149">Verileri dışa veya içe aktarabilir veya [Veri yönetimi](../../dev-itpro/data-entities/data-entities.md) içindeki veri varlığı işlemeyi kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="3ef91-149">You can either export and import the data, or use the data entity processing in [Data management](../../dev-itpro/data-entities/data-entities.md).</span></span>
5.  <span data-ttu-id="3ef91-150">Değişiklikleri doğrulayın.</span><span class="sxs-lookup"><span data-stu-id="3ef91-150">Validate the changes.</span></span> <span data-ttu-id="3ef91-151">Doğrulama işleminin bir parçası olarak çeşitli veri bütünlüğünü doğrulamaları oluşur.</span><span class="sxs-lookup"><span data-stu-id="3ef91-151">As part of the validation process, various validations of data integrity occur.</span></span> <span data-ttu-id="3ef91-152">Daha büyük bir yükseltme işleminin bir parçası olarak, oluşan sorunların kaynak uygulamasında düzeltilmesi gerekebilir.</span><span class="sxs-lookup"><span data-stu-id="3ef91-152">As part of a larger upgrade process, issues that occur might have to be adjusted on the source implementation.</span></span> <span data-ttu-id="3ef91-153">Bu durumda, ek veri yükseltme gerekir.</span><span class="sxs-lookup"><span data-stu-id="3ef91-153">In this case, an additional data upgrade will be required.</span></span>
6.  <span data-ttu-id="3ef91-154">Değişiklikleri işleyin.</span><span class="sxs-lookup"><span data-stu-id="3ef91-154">Process the changes.</span></span>

#### <a name="change-the-storage-dimension-group-for-items-so-that-it-uses-warehouse-management-processes"></a><span data-ttu-id="3ef91-155">Maddeler için depolama boyutu grubunu, ambar yönetimi işlemlerini kullanacak şekilde değiştirin.</span><span class="sxs-lookup"><span data-stu-id="3ef91-155">Change the storage dimension group for items, so that it uses warehouse management processes</span></span>

1.  <span data-ttu-id="3ef91-156">Yeni **Stok durumu** değeri oluşturun ve değeri **Ambar yönetimi parametreleri** ayarlarında **Varsayılan stok durum kodu** değeri olarak atayın.</span><span class="sxs-lookup"><span data-stu-id="3ef91-156">Create a new **Inventory status** value, and assign it as the **Default inventory status ID** value in the **Warehouse management parameters** settings.</span></span>
2.  <span data-ttu-id="3ef91-157">**Ambar yönetimi işlemleri kullan** parametresinin seçili olduğu yeni depolama boyut grubu oluşturun.</span><span class="sxs-lookup"><span data-stu-id="3ef91-157">Create a new storage dimension group where the **Use warehouse management processes** parameter is selected.</span></span>
3.  <span data-ttu-id="3ef91-158">**Rezervasyon hiyerarşisi** sayfasında, maddenin depolama ve izleme boyut gruplarına göre yeni bir ayırma hiyerarşisi tanımlayın.</span><span class="sxs-lookup"><span data-stu-id="3ef91-158">On the **Reservation hierarchy** page, define a new reservation hierarchy according to the item’s storage and tracking dimension groups.</span></span>
4.  <span data-ttu-id="3ef91-159">En azından maddenin stok birimleri için kullanılanlarla aynı birimleri içeren bir veya daha fazla birim sırası grupları oluşturun.</span><span class="sxs-lookup"><span data-stu-id="3ef91-159">Create one or more unit sequence groups that include at least the same units that are used for the items' inventory units.</span></span>
5.  <span data-ttu-id="3ef91-160">**Ambar yönetimi** &gt; **Kurulum** &gt; **Ambar yönetimi işlemlerini etkinleştir** &gt; **Maddeler için depolama boyutu grubunu değiştir**'i tıklayın.</span><span class="sxs-lookup"><span data-stu-id="3ef91-160">Click **Warehouse management** &gt; **Setup** &gt; **Enable warehouse management processes** &gt; **Change storage dimension group for items**.</span></span>
6.  <span data-ttu-id="3ef91-161">**Maddeler için depolama boyutu grubunu değiştir** sayfasında madde numaraları, depolama boyut grupları ve birim sıra grupları ekleyin.</span><span class="sxs-lookup"><span data-stu-id="3ef91-161">On the **Change storage dimension group for items** page, add the item numbers, storage dimension groups, and unit sequence groups.</span></span> <span data-ttu-id="3ef91-162">Bu adımı Microsoft Office tümleştirmesi kullanarak doğrudan sayfa üzerinde veya [Veri yönetimi](../../dev-itpro/data-entities/data-entities.md) içindeki veri varlığı işlemini kullanarak tamamlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="3ef91-162">You can complete this step directly on the page, by using the Microsoft Office integration, or by using the data entity process in [Data management](../../dev-itpro/data-entities/data-entities.md).</span></span>
7.  <span data-ttu-id="3ef91-163">Değişiklikleri doğrulayın.</span><span class="sxs-lookup"><span data-stu-id="3ef91-163">Validate the changes.</span></span> <span data-ttu-id="3ef91-164">Doğrulama işleminin bir parçası olarak çeşitli veri bütünlüğünü doğrulamaları oluşur.</span><span class="sxs-lookup"><span data-stu-id="3ef91-164">As part of the validation process, various validations of data integrity occur.</span></span> <span data-ttu-id="3ef91-165">Daha büyük bir yükseltme işleminin bir parçası olarak, oluşan sorunların kaynak uygulamasında düzeltilmesi gerekebilir.</span><span class="sxs-lookup"><span data-stu-id="3ef91-165">As part of a larger upgrade process, issues that occur might have to be adjusted on the source implementation.</span></span> <span data-ttu-id="3ef91-166">Bu durumda, ek veri yükseltme gerekir.</span><span class="sxs-lookup"><span data-stu-id="3ef91-166">In this case, additional data upgrade will be required.</span></span>
8.  <span data-ttu-id="3ef91-167">Değişiklikleri işleyin.</span><span class="sxs-lookup"><span data-stu-id="3ef91-167">Process the changes.</span></span> <span data-ttu-id="3ef91-168">Stok boyutlarının güncelleştirilmesi biraz zaman alabilir.</span><span class="sxs-lookup"><span data-stu-id="3ef91-168">An update of all the inventory dimensions can take a while.</span></span> <span data-ttu-id="3ef91-169">İlerlemeyi toplu iş görevlerini kullanarak izleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="3ef91-169">You can monitor the progress by using the batch jobs tasks.</span></span>


