---
title: Yerine koyma kümeleri
description: Yerine koyma kümeleri, aynı anda birden fazla plakayı çekmek ve daha sonra farklı yerlerde yerine koymak için bir yol sunar. Bunlar, plakaların genellikle stoğun tam paletleri olmadığı perakende işletmeler için çok yararlı olabilir.
author: Mirzaab
manager: tfehr
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-10-19
ms.dyn365.ops.version: Release 10.0.7
ms.openlocfilehash: 297792e90b3d2da0d738f5cbaa14779bc17ea3c8
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/15/2021
ms.locfileid: "4996210"
---
# <a name="putaway-clusters"></a><span data-ttu-id="a77c1-104">Yerine koyma kümeleri</span><span class="sxs-lookup"><span data-stu-id="a77c1-104">Putaway clusters</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a77c1-105">Yerine koyma kümeleri, aynı anda birden fazla plakayı çekmek ve daha sonra farklı yerlerde yerine koymak için bir yol sunar.</span><span class="sxs-lookup"><span data-stu-id="a77c1-105">Putaway clusters offer a way to pick multiple license plates at the same time and then take them for putaway in different locations.</span></span> <span data-ttu-id="a77c1-106">Bu işlem genellikle bir *çoklu teslimat rotası* olarak adlandırılır.</span><span class="sxs-lookup"><span data-stu-id="a77c1-106">This process is often referred to as a *milk run*.</span></span> <span data-ttu-id="a77c1-107">Yerine koyma kümeleri, plakaların genellikle stoğun tam palet olmadığı perakende işletmeleri için çok yararlı olabilir.</span><span class="sxs-lookup"><span data-stu-id="a77c1-107">Putaway clusters can be very useful for retail businesses, where license plates typically aren't full pallets of inventory.</span></span> 

## <a name="turn-on-the-cluster-putaway-feature"></a><span data-ttu-id="a77c1-108">Küme yerine koyma özelliğini açma</span><span class="sxs-lookup"><span data-stu-id="a77c1-108">Turn on the cluster putaway feature</span></span>

<span data-ttu-id="a77c1-109">Bu özelliği kullanabilmeniz için sisteminizde etkinleştirmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="a77c1-109">Before you can use this feature, it must be turned on in your system.</span></span> <span data-ttu-id="a77c1-110">Yöneticiler özellik durumunu denetlemek ve gerekirse etkinleştirmek için [özellik yönetimi](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) çalışma alanını kullanabilir.</span><span class="sxs-lookup"><span data-stu-id="a77c1-110">Admins can use the [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) workspace to check the status of the feature and turn it on if it's required.</span></span> <span data-ttu-id="a77c1-111">Burada, özellik aşağıdaki şekilde listelenmiştir:</span><span class="sxs-lookup"><span data-stu-id="a77c1-111">There, the feature is listed in the following way:</span></span>

- <span data-ttu-id="a77c1-112">**Modül:** *Ambar yönetimi*</span><span class="sxs-lookup"><span data-stu-id="a77c1-112">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="a77c1-113">**Özellik adı:** *Küme yerine koyma özelliği*</span><span class="sxs-lookup"><span data-stu-id="a77c1-113">**Feature name:** *Cluster putaway feature*</span></span>

## <a name="setup-for-the-example-scenario"></a><span data-ttu-id="a77c1-114">Örnek senaryo için kurulum</span><span class="sxs-lookup"><span data-stu-id="a77c1-114">Setup for the example scenario</span></span>

### <a name="cluster-profiles"></a><span data-ttu-id="a77c1-115">Küme profilleri</span><span class="sxs-lookup"><span data-stu-id="a77c1-115">Cluster profiles</span></span>

<span data-ttu-id="a77c1-116">Küme yerine koyma profili, giriş sırasında maddeye atanan konuma bağlı olarak maddenin nereye gideceğini belirler.</span><span class="sxs-lookup"><span data-stu-id="a77c1-116">The putaway cluster profile determines where an item will go, based on the location that is assigned to the item at the time of receipt.</span></span> <span data-ttu-id="a77c1-117">Farklı yerine koyma kümeleri gerekiyorsa her mobil cihaz menü öğesi için farklı yerine koyma kümesi oluşturulmalıdır.</span><span class="sxs-lookup"><span data-stu-id="a77c1-117">If different clusters are required, different putaway clusters should be created, one for each mobile device menu item.</span></span>

1. <span data-ttu-id="a77c1-118">**Ambar yönetimi \> Kurulum \> Mobil cihaz \> Küme profilleri**'ne tıklayın.</span><span class="sxs-lookup"><span data-stu-id="a77c1-118">Go to **Warehouse management \> Setup \> Mobile device \> Cluster profiles**.</span></span>
1. <span data-ttu-id="a77c1-119">Eylem Bölmesinde, **Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="a77c1-119">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="a77c1-120">**Üst bilgi** görünümünde aşağıdaki değerleri ayarlayın:</span><span class="sxs-lookup"><span data-stu-id="a77c1-120">In the **Header** view, set the following values:</span></span>

    - <span data-ttu-id="a77c1-121">**Yerine koyma kümesi profil kodu:** *Küme yerine koyma*</span><span class="sxs-lookup"><span data-stu-id="a77c1-121">**Putaway cluster profile ID:** *Cluster putaway*</span></span>
    - <span data-ttu-id="a77c1-122">**Yerine koyma kümesi profil kodu adı:** *Küme yerine koyma*</span><span class="sxs-lookup"><span data-stu-id="a77c1-122">**Putaway cluster profile ID Name:** *Cluster putaway*</span></span>
    - <span data-ttu-id="a77c1-123">**Küme türü:** *Yerine koyma*</span><span class="sxs-lookup"><span data-stu-id="a77c1-123">**Cluster type:** *Putaway*</span></span>
    - <span data-ttu-id="a77c1-124">**Sıra numarası:** Varsayılan değeri kabul edin.</span><span class="sxs-lookup"><span data-stu-id="a77c1-124">**Sequence number:** Accept the default value.</span></span>

1. <span data-ttu-id="a77c1-125">Gerekli alanları **Genel** hızlı sekmesinde kullanılabilir hale getirmek için **Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="a77c1-125">Select **Save** to make the required fields on the **General** FastTab available.</span></span>
1. <span data-ttu-id="a77c1-126">**Genel** hızlı sekmesinde, aşağıdaki değerleri ayarlayın:</span><span class="sxs-lookup"><span data-stu-id="a77c1-126">On the **General** FastTab, set the following values:</span></span>

    - <span data-ttu-id="a77c1-127">**Küme atama zamanlaması:** *Giriş sırasında*</span><span class="sxs-lookup"><span data-stu-id="a77c1-127">**Cluster assignment timing:** *At receipt*</span></span>

        <span data-ttu-id="a77c1-128">Bu alan, stok alındığı zaman yerine koyma kümesinin hemen mi atanacağını, yoksa daha mı sıralanıp sıralanmaması gerektiğini tanımlar.</span><span class="sxs-lookup"><span data-stu-id="a77c1-128">This field defines whether the putaway cluster should be assigned immediately when the inventory is received, or whether it should be sorted later.</span></span>

    - <span data-ttu-id="a77c1-129">**Küme atama kuralı:** *El ile*</span><span class="sxs-lookup"><span data-stu-id="a77c1-129">**Cluster assignment rule:** *Manual*</span></span>

        <span data-ttu-id="a77c1-130">Bu alan, küme atamasının sistem tarafından mı, yoksa kullanıcı tarafından el ile mi belirleneceğini tanımlar.</span><span class="sxs-lookup"><span data-stu-id="a77c1-130">This field defines whether the cluster assignment should be determined automatically by the system or manually by the user.</span></span>

    - <span data-ttu-id="a77c1-131">**Yönerge kodu:** Boş bırakın.</span><span class="sxs-lookup"><span data-stu-id="a77c1-131">**Directive code:** Leave this field blank.</span></span>
    - <span data-ttu-id="a77c1-132">**Yerine koyma kümesi konumu:** *Giriş*</span><span class="sxs-lookup"><span data-stu-id="a77c1-132">**Putaway cluster locate:** *Receipt*</span></span>

        <span data-ttu-id="a77c1-133">Aşağıdaki değerler kullanılabilir:</span><span class="sxs-lookup"><span data-stu-id="a77c1-133">The following values are available:</span></span>

        - <span data-ttu-id="a77c1-134">**Giriş**: Hemen giriş sırasında bir konum bulunur.</span><span class="sxs-lookup"><span data-stu-id="a77c1-134">**Receipt** – A location is found immediately during receipt.</span></span>
        - <span data-ttu-id="a77c1-135">**Küme kapatma** Küme kapatıldığında bir konum bulunur.</span><span class="sxs-lookup"><span data-stu-id="a77c1-135">**Cluster close** – A location is found when the cluster is closed.</span></span>
        - <span data-ttu-id="a77c1-136">**Kullanıcı tarafından yönlendirilir**: Plaka yerine koyma amacıyla kümeden çekildiğinde bir konum bulunur.</span><span class="sxs-lookup"><span data-stu-id="a77c1-136">**User directed** – A location is found when the license plate is picked from the cluster for putaway.</span></span> <span data-ttu-id="a77c1-137">Bu durumda, yerine koyma işi oluşturulduğunda hiçbir konum belirtilmemiştir.</span><span class="sxs-lookup"><span data-stu-id="a77c1-137">In this case, no location is specified when the putaway work is created.</span></span> <span data-ttu-id="a77c1-138">Yerine koyma işlemi sırasında, kullanıcı, yerine koyma adımını başlatmak için plaka veya iş kimliğini taramalıdır.</span><span class="sxs-lookup"><span data-stu-id="a77c1-138">During the putaway itself, the user must scan the license plate or work ID to initiate the put step.</span></span> <span data-ttu-id="a77c1-139">Sistem daha sonra yerine koyma konumunu yeniden bulur ve kullanıcıya çekilen miktarın nereye koyulacağını bildirir.</span><span class="sxs-lookup"><span data-stu-id="a77c1-139">The system then finds the put location again and tells the user where to put the picked quantity.</span></span>

    - <span data-ttu-id="a77c1-140">**Kullanıcı bazında yerine koyma kümesi:** *Hayır*</span><span class="sxs-lookup"><span data-stu-id="a77c1-140">**Putaway cluster per user:** *No*</span></span>

        <span data-ttu-id="a77c1-141">Bu alan, kümeler otomatik olarak atandığında her kümenin kullanıcı bazında benzersiz olup olmayacağını tanımlar.</span><span class="sxs-lookup"><span data-stu-id="a77c1-141">This field defines whether each cluster should be unique per user when clusters are automatically assigned.</span></span> <span data-ttu-id="a77c1-142">Yalnızca **Küme atama kuralı** alanı *Otomatik* olarak ayarlandığında kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="a77c1-142">It's available only when the **Cluster assignment rule** field is set to *Automatic*.</span></span>

    - <span data-ttu-id="a77c1-143">**Birim kısıtlaması:** Bu alanı boş bırakın.</span><span class="sxs-lookup"><span data-stu-id="a77c1-143">**Unit restriction:** Leave this field blank.</span></span>

        <span data-ttu-id="a77c1-144">Bu alan, profilin geçerli olabilmesi için alınması gereken birimi tanımlar.</span><span class="sxs-lookup"><span data-stu-id="a77c1-144">This field defines the unit that must be received for the profile to be valid.</span></span> <span data-ttu-id="a77c1-145">Boş bırakılırsa tüm birimler geçerlidir.</span><span class="sxs-lookup"><span data-stu-id="a77c1-145">If it's left blank, all units are valid.</span></span>

    - <span data-ttu-id="a77c1-146">**İş birimi kırılımı:** *Bireysel*</span><span class="sxs-lookup"><span data-stu-id="a77c1-146">**Work unit break:** *Individual*</span></span>

        <span data-ttu-id="a77c1-147">Bu alan, bir küme kapatıldığında tüm stoğun tek bir plaka üzerine birleştirilip birleştirilmemesi (küme kimliği ve plaka kullanılarak) ve alınan plakalar üzerine tek bir plaka olarak mı, yoksa ayrı ayrı mı yerine konulması gerektiğini tanımlar.</span><span class="sxs-lookup"><span data-stu-id="a77c1-147">This field defines whether all inventory should be consolidated (by using the cluster ID and the license plate) onto one license plate when a cluster is closed, and whether it should be put away as a single license plate or separately on the license plates that were received.</span></span> <span data-ttu-id="a77c1-148">**Yerine koyma kümesi konumu** alanı *Giriş* olarak ayarlandığında bu alan kullanılamaz.</span><span class="sxs-lookup"><span data-stu-id="a77c1-148">This field is unavailable when the **Putaway cluster locate** field is set to *Receipt*.</span></span>

    - <span data-ttu-id="a77c1-149">**Küme, Ana Plaka olarak devam eder:** *Hayır*</span><span class="sxs-lookup"><span data-stu-id="a77c1-149">**Cluster persists as Parent License Plate:** *No*</span></span>

        <span data-ttu-id="a77c1-150">Bu seçenek *Evet* olarak ayarlanırsa yerine koyma adımı tamamlandığında küme kimliği bir üst plaka olur ve küme kimliğindeki tüm maddeler bu üst plakaya bağlanır.</span><span class="sxs-lookup"><span data-stu-id="a77c1-150">If this option is set to *Yes*, when the put step is completed, the cluster ID will become a parent license plate, and all items on the cluster ID will be linked to that parent license plate.</span></span>

1. <span data-ttu-id="a77c1-151">**Küme sıralaması** hızlı sekmesinde, yerine koyma sıralama ölçütleri tanımlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="a77c1-151">On the **Cluster sorting** FastTab, you can define putaway sorting criteria.</span></span> <span data-ttu-id="a77c1-152">Araç çubuğundaki **Yeni**'yi seçerek bir satır ekleyin ve aşağıdaki değerleri ayarlayın:</span><span class="sxs-lookup"><span data-stu-id="a77c1-152">Select **New** on the toolbar to add a line, and then set the following values:</span></span>

    - <span data-ttu-id="a77c1-153">**Sıra numarası:** Varsayılan değeri kabul edin.</span><span class="sxs-lookup"><span data-stu-id="a77c1-153">**Sequence number:** Accept the default value.</span></span>
    - <span data-ttu-id="a77c1-154">**Alan adı:** *WMSLocationId*</span><span class="sxs-lookup"><span data-stu-id="a77c1-154">**Field name:** *WMSLocationId*</span></span>

        <span data-ttu-id="a77c1-155">Bu alan, bu satırın sıralama ölçütü olarak kullanacağı alanı belirler.</span><span class="sxs-lookup"><span data-stu-id="a77c1-155">This field defines the field that this line should use as a sorting criterion.</span></span>

    - <span data-ttu-id="a77c1-156">**Sıralama:** *Artan*</span><span class="sxs-lookup"><span data-stu-id="a77c1-156">**Sorting:** *Ascending*</span></span>

        <span data-ttu-id="a77c1-157">Bu alan, sıralamanın artan veya azalan sırada olacağını tanımlar.</span><span class="sxs-lookup"><span data-stu-id="a77c1-157">This field defines whether sorting should be done in ascending or descending order.</span></span>

1. <span data-ttu-id="a77c1-158">**Küme işi şablonu** hızlı sekmesinde, satır eklemek için **Yeni**'yi seçin ve bunun için aşağıdaki değerleri ayarlayın:</span><span class="sxs-lookup"><span data-stu-id="a77c1-158">On the **Cluster work template** FastTab, select **New** on the toolbar to add a line, and then set the following values:</span></span>

    - <span data-ttu-id="a77c1-159">**İş emri türü:** *Satın alma siparişleri*</span><span class="sxs-lookup"><span data-stu-id="a77c1-159">**Work order type:** *Purchase orders*</span></span>
    - <span data-ttu-id="a77c1-160">**İş şablonu:** *61 SAS Doğrudan*</span><span class="sxs-lookup"><span data-stu-id="a77c1-160">**Work template:** *61 PO Direct*</span></span>

1. <span data-ttu-id="a77c1-161">Eylem Bölmesinde, **Kaydet**'i ve sonra **Sorguyu düzenle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="a77c1-161">On the Action Pane, select **Save**, and then select **Edit query**.</span></span>
1. <span data-ttu-id="a77c1-162">**Küme yerine koyma** iletişim kutusundaki **Aralık** sekmesinde **Ekle**'yi seçerek sorguya ikinci bir satır ekleyin:</span><span class="sxs-lookup"><span data-stu-id="a77c1-162">In the **Cluster putaway** dialog box, on the **Range** tab, select **Add** to add a second line to the query.</span></span> <span data-ttu-id="a77c1-163">Ardından, aşağıdaki tabloda gösterildiği gibi sorgu satırlarını güncelleştirin.</span><span class="sxs-lookup"><span data-stu-id="a77c1-163">Then update the query lines as shown in the following table.</span></span>

    | <span data-ttu-id="a77c1-164">Tablo</span><span class="sxs-lookup"><span data-stu-id="a77c1-164">Table</span></span> | <span data-ttu-id="a77c1-165">Türetilen tablo</span><span class="sxs-lookup"><span data-stu-id="a77c1-165">Derived table</span></span> | <span data-ttu-id="a77c1-166">Alan</span><span class="sxs-lookup"><span data-stu-id="a77c1-166">Field</span></span> | <span data-ttu-id="a77c1-167">Ölçütler</span><span class="sxs-lookup"><span data-stu-id="a77c1-167">Criteria</span></span> |
    |---|---|---|---|
    | <span data-ttu-id="a77c1-168">Work</span><span class="sxs-lookup"><span data-stu-id="a77c1-168">Work</span></span> | <span data-ttu-id="a77c1-169">Work</span><span class="sxs-lookup"><span data-stu-id="a77c1-169">Work</span></span> | <span data-ttu-id="a77c1-170">Ambar</span><span class="sxs-lookup"><span data-stu-id="a77c1-170">Warehouse</span></span> | <span data-ttu-id="a77c1-171">*61*</span><span class="sxs-lookup"><span data-stu-id="a77c1-171">*61*</span></span> |
    | <span data-ttu-id="a77c1-172">Work</span><span class="sxs-lookup"><span data-stu-id="a77c1-172">Work</span></span> | <span data-ttu-id="a77c1-173">Work</span><span class="sxs-lookup"><span data-stu-id="a77c1-173">Work</span></span> | <span data-ttu-id="a77c1-174">İş Kodu</span><span class="sxs-lookup"><span data-stu-id="a77c1-174">Work ID</span></span> | <span data-ttu-id="a77c1-175">Bu alanı boş bırakın.</span><span class="sxs-lookup"><span data-stu-id="a77c1-175">Leave this field blank.</span></span> |

1. <span data-ttu-id="a77c1-176">Sorguyu kaydetmek için **Tamam**'ı seçin ve iletişim kutusunu kapatın.</span><span class="sxs-lookup"><span data-stu-id="a77c1-176">Select **OK** to save the query and close the dialog box.</span></span>
1. <span data-ttu-id="a77c1-177">Eylem Bölmesi'nde **Kaydet**'i seçin ve ardından sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="a77c1-177">On the Action Pane, select **Save**, and close the page.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="a77c1-178">**Küme kimliği oluştur**, *Evet* olarak ayarlandığında soluk görünen küme profilindeki alanlar kullanılamaz ve bu özellik kullanıldığında dikkate alınmaz.</span><span class="sxs-lookup"><span data-stu-id="a77c1-178">Fields in the cluster profile that appear dimmed when **Generate cluster ID** is set to *Yes* are unavailable and won't be considered when this feature is used.</span></span>

### <a name="mobile-device-menu-items"></a><span data-ttu-id="a77c1-179">Mobil cihaz menü öğeleri</span><span class="sxs-lookup"><span data-stu-id="a77c1-179">Mobile device menu items</span></span>

<span data-ttu-id="a77c1-180">Bu özellik için iki yeni mobil cihaz menü öğesi mevcuttur.</span><span class="sxs-lookup"><span data-stu-id="a77c1-180">Two new mobile device menu items are available for this feature.</span></span> <span data-ttu-id="a77c1-181">Alınan stoğu, girişin ardından yerine koyma kümesine sıralamak için **Al ve kümeyi sırala** menü öğesi kullanılır.</span><span class="sxs-lookup"><span data-stu-id="a77c1-181">The **Receive and sort cluster** menu item is used to sort the received inventory into a putaway cluster upon receipt.</span></span> <span data-ttu-id="a77c1-182">**Küme yerine koyma** menü öğesi, küme atandıktan sonra yerine koymak için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="a77c1-182">The **Cluster putaway** menu item is used to put the cluster away after it has been assigned.</span></span>

#### <a name="receive-and-sort-cluster"></a><span data-ttu-id="a77c1-183">Al ve kümeyi sırala</span><span class="sxs-lookup"><span data-stu-id="a77c1-183">Receive and sort cluster</span></span>

<span data-ttu-id="a77c1-184">Stok almak ve kümeye sıralamak için yeni bir mobil cihaz menü öğesi oluşturun.</span><span class="sxs-lookup"><span data-stu-id="a77c1-184">Create a new mobile device menu item for receiving inventory and sorting into a cluster.</span></span> <span data-ttu-id="a77c1-185">Bu menü öğesi, stok alındıktan sonra bir gelen iş oluşturur ve bu da alıcı menü öğesinin yerine koyma kümeleri için kullanılacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="a77c1-185">This menu item will create inbound work after inventory is received, which indicates that the receiving menu item will be used for putaway clusters.</span></span>

> [!NOTE]
> <span data-ttu-id="a77c1-186">**Al ve kümeyi sırala** menü öğesi aşağıdaki alıcı menü öğeleriyle kullanılabilir:</span><span class="sxs-lookup"><span data-stu-id="a77c1-186">The **Receive and sort cluster** menu item can be used with the following receiving menu items:</span></span>
>
> - <span data-ttu-id="a77c1-187">Satınalma siparişi satırı teslim alma</span><span class="sxs-lookup"><span data-stu-id="a77c1-187">Purchase order line receiving</span></span>
> - <span data-ttu-id="a77c1-188">Satınalma siparişi madde teslim alma</span><span class="sxs-lookup"><span data-stu-id="a77c1-188">Purchase order item receiving</span></span>
> - <span data-ttu-id="a77c1-189">Yük maddesi teslim alma</span><span class="sxs-lookup"><span data-stu-id="a77c1-189">Load item receiving</span></span>

1. <span data-ttu-id="a77c1-190">**Ambar yönetimi \> Kurulum \> Mobil cihaz \> Mobil cihaz menüsü öğeleri**'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="a77c1-190">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu items**.</span></span>
1. <span data-ttu-id="a77c1-191">Eylem Bölmesinde, **Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="a77c1-191">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="a77c1-192">**Üst bilgi** görünümünde aşağıdaki değerleri ayarlayın:</span><span class="sxs-lookup"><span data-stu-id="a77c1-192">In the **Header** view, set the following values:</span></span>

    - <span data-ttu-id="a77c1-193">**Menü öğesi adı:** *Al ve kümeyi sırala*</span><span class="sxs-lookup"><span data-stu-id="a77c1-193">**Menu item name:** *Receive and sort cluster*</span></span>
    - <span data-ttu-id="a77c1-194">**Başlık:** *Al ve kümeyi sırala*</span><span class="sxs-lookup"><span data-stu-id="a77c1-194">**Title:** *Receive and sort cluster*</span></span>
    - <span data-ttu-id="a77c1-195">**Mod:** *İş*</span><span class="sxs-lookup"><span data-stu-id="a77c1-195">**Mode:** *Work*</span></span>
    - <span data-ttu-id="a77c1-196">**Varolan çalışmayı kullan:** *Hayır*</span><span class="sxs-lookup"><span data-stu-id="a77c1-196">**Use existing work:** *No*</span></span>

1. <span data-ttu-id="a77c1-197">**Genel** hızlı sekmesinde, aşağıdaki değerleri ayarlayın:</span><span class="sxs-lookup"><span data-stu-id="a77c1-197">On the **General** FastTab, set the following values:</span></span>

    - <span data-ttu-id="a77c1-198">**İş oluşturma işlemi:** *Satın alma siparişi madde teslim alma*</span><span class="sxs-lookup"><span data-stu-id="a77c1-198">**Work creation process:** *Purchase order item receiving*</span></span>
    - <span data-ttu-id="a77c1-199">**Plaka oluştur:** *Evet*</span><span class="sxs-lookup"><span data-stu-id="a77c1-199">**Generate license plate:** *Yes*</span></span>
    - <span data-ttu-id="a77c1-200">**Yerine koyma kümesini ata:** *Evet*</span><span class="sxs-lookup"><span data-stu-id="a77c1-200">**Assign putaway cluster:** *Yes*</span></span>

        > [!NOTE]
        > <span data-ttu-id="a77c1-201">**Yerine koyma kümesi ata** seçeneği teslim alma açısından yalnızca tek adımlı *İş oluşturma işlemi* etkinliği için kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="a77c1-201">The **Assign putaway cluster** option is available only for the one-step *Work creation process* activity for receiving.</span></span>

    <span data-ttu-id="a77c1-202">Kalan alanlar için varsayılan değerleri kabul edin.</span><span class="sxs-lookup"><span data-stu-id="a77c1-202">Accept the default values for the remaining fields.</span></span>

1. <span data-ttu-id="a77c1-203">Eylem bölmesinde, **Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="a77c1-203">On the Action Pane, select **Save**.</span></span>

#### <a name="cluster-putaway"></a><span data-ttu-id="a77c1-204">Küme yerine koyma</span><span class="sxs-lookup"><span data-stu-id="a77c1-204">Cluster putaway</span></span>

<span data-ttu-id="a77c1-205">Küme atandıktan sonra kümeyi yerine koymak için yeni bir mobil cihaz menü öğesi oluşturun.</span><span class="sxs-lookup"><span data-stu-id="a77c1-205">Create a new mobile device menu item for putting the cluster away after it has been assigned.</span></span>

1. <span data-ttu-id="a77c1-206">**Ambar yönetimi \> Kurulum \> Mobil cihaz \> Mobil cihaz menüsü öğeleri**'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="a77c1-206">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu items**.</span></span>
1. <span data-ttu-id="a77c1-207">Eylem Bölmesinde, **Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="a77c1-207">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="a77c1-208">**Üst bilgi** görünümünde aşağıdaki değerleri ayarlayın:</span><span class="sxs-lookup"><span data-stu-id="a77c1-208">In the **Header** view, set the following values:</span></span>

    - <span data-ttu-id="a77c1-209">**Menü öğesi adı:** *Küme yerine koyma*</span><span class="sxs-lookup"><span data-stu-id="a77c1-209">**Menu item name:** *Cluster putaway*</span></span>
    - <span data-ttu-id="a77c1-210">**Başlık:** *Küme yerine koyma*</span><span class="sxs-lookup"><span data-stu-id="a77c1-210">**Title:** *Cluster putaway*</span></span>
    - <span data-ttu-id="a77c1-211">**Mod:** *İş*</span><span class="sxs-lookup"><span data-stu-id="a77c1-211">**Mode:** *Work*</span></span>
    - <span data-ttu-id="a77c1-212">**Mevcut işi kullan:** *Evet*</span><span class="sxs-lookup"><span data-stu-id="a77c1-212">**Use existing work:** *Yes*</span></span>

1. <span data-ttu-id="a77c1-213">**Genel** hızlı sekmesinde **Yöneten** alanı *Küme yerine koyma* olarak ayarlanmalıdır.</span><span class="sxs-lookup"><span data-stu-id="a77c1-213">On the **General** FastTab, set the **Directed by** field to *Cluster putaway*.</span></span> <span data-ttu-id="a77c1-214">Kalan alanlar için varsayılan değerleri kabul edin.</span><span class="sxs-lookup"><span data-stu-id="a77c1-214">Accept the default values for the remaining fields.</span></span>
1. <span data-ttu-id="a77c1-215">**İş sınıfları** hızlı sekmesinde, mobil cihaz menü öğesi için geçerli iş sınıfını ayarlayın:</span><span class="sxs-lookup"><span data-stu-id="a77c1-215">On the **Work classes** FastTab, set up the valid work class for this mobile device menu item:</span></span>

    - <span data-ttu-id="a77c1-216">**İş sınıfı kodu:** *Purchase*</span><span class="sxs-lookup"><span data-stu-id="a77c1-216">**Work class ID:** *Purchase*</span></span>
    - <span data-ttu-id="a77c1-217">**İş emri türü:** *Satın alma siparişleri*</span><span class="sxs-lookup"><span data-stu-id="a77c1-217">**Work order type:** *Purchase orders*</span></span>

1. <span data-ttu-id="a77c1-218">Eylem bölmesinde, **Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="a77c1-218">On the Action Pane, select **Save**.</span></span>

### <a name="mobile-device-menu"></a><span data-ttu-id="a77c1-219">Mobil cihaz menüsü</span><span class="sxs-lookup"><span data-stu-id="a77c1-219">Mobile device menu</span></span>

<span data-ttu-id="a77c1-220">Yeni oluşturduğunuz menü öğelerini mobil uygulamanın gelen menüsüne ekleyin.</span><span class="sxs-lookup"><span data-stu-id="a77c1-220">Add the menu items that you just created to the inbound menu of the mobile app.</span></span>

1. <span data-ttu-id="a77c1-221">**Ambar yönetimi \> Kurulum \> Mobil cihaz \> Mobil cihaz menüsü**'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="a77c1-221">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu**.</span></span>
1. <span data-ttu-id="a77c1-222">Eylem Bölmesi'nde, **Düzenle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="a77c1-222">On the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="a77c1-223">Menü listesinde **Gelen**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="a77c1-223">In the menu list, select **Inbound**.</span></span>
1. <span data-ttu-id="a77c1-224">**Mevcut menüler ve menü öğeleri** listesinde, **Kümeyi teslim al ve sırala**'yı bulup seçin.</span><span class="sxs-lookup"><span data-stu-id="a77c1-224">In the **Available menus and menu items** list, find and select **Receive and sort cluster**.</span></span>
1. <span data-ttu-id="a77c1-225">Seçilen menü öğesini **Menü yapısı** listesine taşımak için sağ ok düğmesini seçin.</span><span class="sxs-lookup"><span data-stu-id="a77c1-225">Select the right arrow button to move the selected menu item to the **Menu structure** list.</span></span>
1. <span data-ttu-id="a77c1-226">Menü öğesini menüde istenen konuma taşımak için yukarı ok ve aşağı ok düğmelerini kullanın.</span><span class="sxs-lookup"><span data-stu-id="a77c1-226">Use the up arrow or down arrow button to move the menu item into the desired position in the menu.</span></span>
1. <span data-ttu-id="a77c1-227">Eylem bölmesinde, **Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="a77c1-227">On the Action Pane, select **Save**.</span></span>
1. <span data-ttu-id="a77c1-228">Kalan menü öğelerini eklemek için 4 ile 7. adımlar arasındaki işlemleri tekrarlayın.</span><span class="sxs-lookup"><span data-stu-id="a77c1-228">Repeat steps 4 through 7 to add the remaining menu items:</span></span>

    - <span data-ttu-id="a77c1-229">Küme atama</span><span class="sxs-lookup"><span data-stu-id="a77c1-229">Assign cluster</span></span>
    - <span data-ttu-id="a77c1-230">Küme yerine koyma</span><span class="sxs-lookup"><span data-stu-id="a77c1-230">Cluster putaway</span></span>

## <a name="example-scenario"></a><span data-ttu-id="a77c1-231">Örnek senaryo</span><span class="sxs-lookup"><span data-stu-id="a77c1-231">Example scenario</span></span>

<span data-ttu-id="a77c1-232">Bu senaryo, küme küme yerine koymayı işlemeyi simüle eder.</span><span class="sxs-lookup"><span data-stu-id="a77c1-232">This scenario simulates putaway cluster processing.</span></span>

### <a name="create-a-purchase-order"></a><span data-ttu-id="a77c1-233">Satınalma siparişi oluşturma</span><span class="sxs-lookup"><span data-stu-id="a77c1-233">Create a purchase order</span></span>

1. <span data-ttu-id="a77c1-234">**Borç hesapları \> Satın alma siparişleri \> Tüm satınalma siparişleri**'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="a77c1-234">Go to **Accounts payable \> Purchase orders \> All purchase orders**.</span></span>
1. <span data-ttu-id="a77c1-235">Eylem Bölmesinde, **Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="a77c1-235">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="a77c1-236">**Satın alma siparişi oluştur** iletişim kutusunda, aşağıdaki değerleri ayarlayın:</span><span class="sxs-lookup"><span data-stu-id="a77c1-236">In the **Create purchase order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="a77c1-237">**Satıcı hesabı:** *1001*</span><span class="sxs-lookup"><span data-stu-id="a77c1-237">**Vendor account:** *1001*</span></span>
    - <span data-ttu-id="a77c1-238">**Ambar:** *61*</span><span class="sxs-lookup"><span data-stu-id="a77c1-238">**Warehouse:** *61*</span></span>

1. <span data-ttu-id="a77c1-239">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="a77c1-239">Select **OK**.</span></span>

    <span data-ttu-id="a77c1-240">**Tüm satın alma siparişleri** sayfası görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="a77c1-240">The **All purchase orders** page appears.</span></span>

1. <span data-ttu-id="a77c1-241">**Tüm satın alma siparişleri** sayfasında, **Satın alma siparişi satırları** hızlı sekmesinde aşağıdaki satırları eklemek için **Satır ekle**'yi kullanın:</span><span class="sxs-lookup"><span data-stu-id="a77c1-241">On the **All purchase orders** page, on the **Purchase order lines** FastTab, use the **Add line** button to add the following lines:</span></span>

    - <span data-ttu-id="a77c1-242">Satın alma siparişi satırı 1:</span><span class="sxs-lookup"><span data-stu-id="a77c1-242">Purchase order line 1:</span></span>

        - <span data-ttu-id="a77c1-243">**Madde numarası:** *A0001*</span><span class="sxs-lookup"><span data-stu-id="a77c1-243">**Item number:** *A0001*</span></span>
        - <span data-ttu-id="a77c1-244">**Miktar:** *10*</span><span class="sxs-lookup"><span data-stu-id="a77c1-244">**Quantity:** *10*</span></span>

    - <span data-ttu-id="a77c1-245">Satın alma siparişi satırı 2:</span><span class="sxs-lookup"><span data-stu-id="a77c1-245">Purchase order line 2:</span></span>

        - <span data-ttu-id="a77c1-246">**Madde numarası:** *A0002*</span><span class="sxs-lookup"><span data-stu-id="a77c1-246">**Item number:** *A0002*</span></span>
        - <span data-ttu-id="a77c1-247">**Miktar:** *20*</span><span class="sxs-lookup"><span data-stu-id="a77c1-247">**Quantity:** *20*</span></span>

    - <span data-ttu-id="a77c1-248">Satın alma siparişi satırı 3:</span><span class="sxs-lookup"><span data-stu-id="a77c1-248">Purchase order line 3:</span></span>

        - <span data-ttu-id="a77c1-249">**Madde numarası:** *M9215*</span><span class="sxs-lookup"><span data-stu-id="a77c1-249">**Item number:** *M9215*</span></span>
        - <span data-ttu-id="a77c1-250">**Miktar:** *30*</span><span class="sxs-lookup"><span data-stu-id="a77c1-250">**Quantity:** *30*</span></span>

1. <span data-ttu-id="a77c1-251">Eylem bölmesinde, **Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="a77c1-251">On the Action Pane, select **Save**.</span></span>
1. <span data-ttu-id="a77c1-252">Satın alma siparişi numarasını not edin.</span><span class="sxs-lookup"><span data-stu-id="a77c1-252">Make a note of the purchase order number.</span></span>

### <a name="receive-inventory-and-put-it-away-from-the-mobile-device"></a><span data-ttu-id="a77c1-253">Mobil cihazdan stoğu teslim alma ve yerine koyma</span><span class="sxs-lookup"><span data-stu-id="a77c1-253">Receive inventory and put it away from the mobile device</span></span>

#### <a name="receive-and-sort-the-inventory-into-a-cluster"></a><span data-ttu-id="a77c1-254">Stoğu bir kümeye teslim alma ve sıralama</span><span class="sxs-lookup"><span data-stu-id="a77c1-254">Receive and sort the inventory into a cluster</span></span>

1. <span data-ttu-id="a77c1-255">Ambar *61* için ayarlanan bir kullanıcı olarak ambarı uygulamasına oturum açın.</span><span class="sxs-lookup"><span data-stu-id="a77c1-255">Sign in to the warehouse app as a user who is set up for warehouse *61*.</span></span>
1. <span data-ttu-id="a77c1-256">Ana menüde **Gelen**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="a77c1-256">On the main menu, select **Inbound**.</span></span>
1. <span data-ttu-id="a77c1-257">**Gelen** menüsünde **Teslim al ve kümeyi sırala**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="a77c1-257">On the **Inbound** menu, select **Receive and sort cluster**.</span></span>
1. <span data-ttu-id="a77c1-258">**SAS No** alanına satın alma siparişi numaranızı girin.</span><span class="sxs-lookup"><span data-stu-id="a77c1-258">In the **Ponum** field, enter the purchase order number.</span></span>
1. <span data-ttu-id="a77c1-259">**Tamam**'ı (onay işareti düğmesi) seçin.</span><span class="sxs-lookup"><span data-stu-id="a77c1-259">Select **OK** (the check mark button).</span></span>
1. <span data-ttu-id="a77c1-260">**Madde** alanını seçin, *A0001* madde numarasını girin ve ardından **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="a77c1-260">Select the **Item** field, enter item number *A0001*, and then select **OK**.</span></span>
1. <span data-ttu-id="a77c1-261">**Miktar** alanını seçin, sayısal tuş takımını kullanarak *10* girin ve ardından onay işareti düğmesini seçin.</span><span class="sxs-lookup"><span data-stu-id="a77c1-261">Select the **Qty** field, enter *10* by using the number pad, and then select the check mark button.</span></span>
1. <span data-ttu-id="a77c1-262">**Miktar** görev sayfasında, girdiğiniz miktarı onaylamak için **Tamam**'ı (onay işareti düğmesi) seçin.</span><span class="sxs-lookup"><span data-stu-id="a77c1-262">On the **Qty** task page, select **OK** (the check mark button) to confirm the quantity that you entered.</span></span>
1. <span data-ttu-id="a77c1-263">**Madde** görev sayfasında, *A0001* maddesinin girildiğini onaylamak için **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="a77c1-263">On the **Item** task page, select **OK** to confirm that item *A0001* was entered.</span></span>
1. <span data-ttu-id="a77c1-264">**Küme Kimliği** alanını seçin ve oluşturmakta olduğunuz küme için kimlik atamak üzere bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="a77c1-264">Select the **Cluster ID** field, and enter a value to assign an ID for the cluster that you're creating.</span></span>

    <span data-ttu-id="a77c1-265">Buraya girdiğiniz kimlik, satın alma siparişinde kalan iki madde teslim alındığı zaman kullanılacaktır.</span><span class="sxs-lookup"><span data-stu-id="a77c1-265">The ID that you enter here will be used when the two remaining items on the purchase order are received.</span></span>

1. <span data-ttu-id="a77c1-266">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="a77c1-266">Select **OK**.</span></span>

    <span data-ttu-id="a77c1-267">**SAS numarası** görev sayfası görüntülenir ve "İş tamamlandı" iletisini gösterir.</span><span class="sxs-lookup"><span data-stu-id="a77c1-267">The **Ponum** task page appears and shows a "Work completed" message.</span></span>

    <span data-ttu-id="a77c1-268">*A0001* maddesi artık *RECV* konumuna alınmıştır ve adım 10'da girdiğiniz küme kimliğine atanmıştır.</span><span class="sxs-lookup"><span data-stu-id="a77c1-268">Item *A0001* has now been received into the *RECV* location and assigned to the cluster ID that you entered in step 10.</span></span>

1. <span data-ttu-id="a77c1-269">Satın alma siparişindeki kalan iki maddeyi teslim almak ve küme kimliğine atamak için 4 ile 11 arası adımları yineleyin:</span><span class="sxs-lookup"><span data-stu-id="a77c1-269">Repeat steps 4 through 11 to receive the remaining two items from the purchase order and assign them to the cluster ID:</span></span>

    - <span data-ttu-id="a77c1-270">*A0002* maddesi için *20* miktar</span><span class="sxs-lookup"><span data-stu-id="a77c1-270">A quantity of *20* for item *A0002*</span></span>
    - <span data-ttu-id="a77c1-271">*M9215* maddesi için *30* miktar</span><span class="sxs-lookup"><span data-stu-id="a77c1-271">A quantity of *30* for item *M9215*</span></span>

#### <a name="close-the-cluster"></a><span data-ttu-id="a77c1-272">Kümeyi kapatma</span><span class="sxs-lookup"><span data-stu-id="a77c1-272">Close the cluster</span></span>

<span data-ttu-id="a77c1-273">Kümedeki maddelerin kaldırılabilmeleri için kümenin kapatılması gerekir.</span><span class="sxs-lookup"><span data-stu-id="a77c1-273">Before the items in the cluster can be put away, the cluster must be closed.</span></span>

1. <span data-ttu-id="a77c1-274">Supply Chain Management'ta, **Ambar yönetimi \> İş \> Giden İş \> İş kümeleri**'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="a77c1-274">In Supply Chain Management, go to **Warehouse management \> Work \> Outbound \> Work clusters**.</span></span>
1. <span data-ttu-id="a77c1-275">**İş kümeleri** sayfasında, **İş kümesi** bölümünde, daha önce girdiğiniz küme kimliği için **Küme Kimliği** alanında arama yapın.</span><span class="sxs-lookup"><span data-stu-id="a77c1-275">On the **Work clusters** page, in the **Work cluster** section, search the **Cluster ID** field for the cluster ID that you entered earlier.</span></span>
1. <span data-ttu-id="a77c1-276">Küme gösterilmezse, zaten kapatılmış olabilir.</span><span class="sxs-lookup"><span data-stu-id="a77c1-276">If the cluster isn't shown, it might already have been closed.</span></span> <span data-ttu-id="a77c1-277">Kümenin kapalı olup olmadığını belirlemek için **Kapalı işleri göster** onay kutusunu seçin ve daha önce girdiğiniz küme kimliğini arayın.</span><span class="sxs-lookup"><span data-stu-id="a77c1-277">To determine whether the cluster was closed, select the **Show closed work** check box, and search for the cluster ID that you entered earlier.</span></span> <span data-ttu-id="a77c1-278">Ardından şu adımlardan birini izleyin:</span><span class="sxs-lookup"><span data-stu-id="a77c1-278">Then follow one of these steps:</span></span>

    - <span data-ttu-id="a77c1-279">Küme kapatıldıysa, bu prosedürün kalan adımlarını atlayın ve bir sonraki prosedüre geçin: [Kümeyi yerine koyma](#put-the-cluster-away).</span><span class="sxs-lookup"><span data-stu-id="a77c1-279">If the cluster has been closed, skip the remaining steps of this procedure, and move on to the next procedure, [Put the cluster away](#put-the-cluster-away).</span></span>
    - <span data-ttu-id="a77c1-280">Küme kapatılmadıysa kümeyi el ile kapatmak için bu prosedürün kalan adımlarını izleyin.</span><span class="sxs-lookup"><span data-stu-id="a77c1-280">If the cluster hasn't been closed, follow the remaining steps of this procedure to manually close the cluster.</span></span> <span data-ttu-id="a77c1-281">Ardından sonraki prosedüre geçin.</span><span class="sxs-lookup"><span data-stu-id="a77c1-281">Then move on to the next procedure.</span></span>

1. <span data-ttu-id="a77c1-282">**İş kümesi** bölümünde, daha önce girdiğiniz küme kimliğini seçin.</span><span class="sxs-lookup"><span data-stu-id="a77c1-282">In the **Work cluster** section, select the cluster ID that you entered earlier.</span></span>
1. <span data-ttu-id="a77c1-283">Eylem Bölmesinde **Kümeyi kapat**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="a77c1-283">On the Action Pane, select **Close cluster**.</span></span>

    <span data-ttu-id="a77c1-284">Küme kapatıldıktan sonra, artık **İş kümesi** bölümünde gösterilmez (**Kapalı işleri göster** onay kutusu seçili değilse).</span><span class="sxs-lookup"><span data-stu-id="a77c1-284">After the cluster has been closed, it's no longer shown in the **Work cluster** section (unless the **Show closed work** check box is selected).</span></span>

#### <a name="put-the-cluster-away"></a><span data-ttu-id="a77c1-285">Kümeyi yerine koyma</span><span class="sxs-lookup"><span data-stu-id="a77c1-285">Put the cluster away</span></span>

1. <span data-ttu-id="a77c1-286">Ambar *61* için ayarlanan bir kullanıcı olarak ambarı uygulamasına oturum açın.</span><span class="sxs-lookup"><span data-stu-id="a77c1-286">Sign in to the warehouse app as a user who is set up for warehouse *61*.</span></span>
1. <span data-ttu-id="a77c1-287">Ana menüde **Gelen**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="a77c1-287">On the main menu, select **Inbound**.</span></span>
1. <span data-ttu-id="a77c1-288">**Gelen** menüsünden **Küme yerine koyma**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="a77c1-288">On the **Inbound** menu, select **Cluster putaway**.</span></span>
1. <span data-ttu-id="a77c1-289">**Küme Kimliği**'ni seçin ve kapalı küme için daha önce girdiğiniz küme kimliğini girin.</span><span class="sxs-lookup"><span data-stu-id="a77c1-289">Select **Cluster ID**, and enter the cluster ID that you entered earlier for the closed cluster.</span></span>
1. <span data-ttu-id="a77c1-290">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="a77c1-290">Select **OK**.</span></span>

    <span data-ttu-id="a77c1-291">**Küme yerine koyma: Malzeme çekme** sayfası görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="a77c1-291">The **Cluster putaway: Pick** page appears.</span></span> <span data-ttu-id="a77c1-292">Küme kimliğini, malzeme çekme konumunu, maddeleri (*Çoklu* değeri gösterilecek) ve kümedeki çekilmesi gereken toplam miktarı gösterir.</span><span class="sxs-lookup"><span data-stu-id="a77c1-292">It shows the cluster ID, the picking location, the items (the value *Multiple* will be shown), and the total quantity in the cluster that must be picked.</span></span>

1. <span data-ttu-id="a77c1-293">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="a77c1-293">Select **OK**.</span></span>

    <span data-ttu-id="a77c1-294">**Küme yerine koyma: Yerine koy** sayfası görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="a77c1-294">The **Cluster putaway: Put** page appears.</span></span> <span data-ttu-id="a77c1-295">**Yerine koy** yönergeleri küme kimliğini, yerine koyma konumunu, maddeleri, toplam miktarı ve kümede teslim alınan maddelerin plaka kimliklerini tanımlar.</span><span class="sxs-lookup"><span data-stu-id="a77c1-295">The **Put** instructions identify the cluster ID, the put location, the items, the total quantity, and the license plate IDs for the items that have been received on the cluster.</span></span>

    <span data-ttu-id="a77c1-296">Bu adımı geçersiz kılmak veya atlamak için standart seçeneklere sahipsiniz.</span><span class="sxs-lookup"><span data-stu-id="a77c1-296">You have the standard options to override or pass this step.</span></span>

    <span data-ttu-id="a77c1-297">![Küme yerine koyma: Sayfayı yerine koyma](media/Cluster_putaway-Put.png "Küme yerine koyma: Sayfayı yerine koyma")</span><span class="sxs-lookup"><span data-stu-id="a77c1-297">![Cluster putaway: Put page](media/Cluster_putaway-Put.png "Cluster putaway: Put page")</span></span>

1. <span data-ttu-id="a77c1-298">Kümenin yerine konmasını onaylamak için **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="a77c1-298">Select **OK** to confirm the putaway of the cluster.</span></span>

    <span data-ttu-id="a77c1-299">"Küme tamamlandı" iletisi gösterilir.</span><span class="sxs-lookup"><span data-stu-id="a77c1-299">A "Cluster completed" message is shown.</span></span>

## <a name="notes-and-tips"></a><span data-ttu-id="a77c1-300">Notlar ve ipuçları</span><span class="sxs-lookup"><span data-stu-id="a77c1-300">Notes and tips</span></span>

<span data-ttu-id="a77c1-301">Küme kimliğinin iç içe geçmiş palet için üst plaka olduğu durumlarda, küme kimliği tarandığında yerine koyma konumu otomatik olarak verilir.</span><span class="sxs-lookup"><span data-stu-id="a77c1-301">For cases where the cluster ID becomes the parent license plate for a nested pallet, the put position is automatically given when the cluster ID is scanned.</span></span> <span data-ttu-id="a77c1-302">Plaka üretimi el ile olarak ayarlansa bile başka bir plaka taranmamalıdır.</span><span class="sxs-lookup"><span data-stu-id="a77c1-302">No further license plate must be scanned, even if license plate generation is set to manual.</span></span>
