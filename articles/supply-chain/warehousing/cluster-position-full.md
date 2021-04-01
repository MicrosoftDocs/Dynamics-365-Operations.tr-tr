---
title: Küme konumu dolu
description: Bu konuda, Küme konumu dolu özelliğiyle ilgili bilgiler verilir. Bu özellik, küme malzeme çekme kullanılırken iş kesme kuralına ait daha katı zorlamaya olanak sağlayan bir alternatif sunar, çünkü konteyner ve sepetlerin hacimleri ile ilişki kısıtlamalarda daha büyük hata marjlarına olanak sağlar.
author: Mirzaab
manager: tfehr
ms.date: 08/25/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSClusterProfile
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: b6a7cad070377de58d21a8eb91ee3e1ffaf1c660
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5233019"
---
# <a name="cluster-position-full"></a><span data-ttu-id="250e9-104">Küme konumu dolu</span><span class="sxs-lookup"><span data-stu-id="250e9-104">Cluster position full</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="250e9-105">*Küme konumu dolu* özelliği, küme malzeme çekme kullanılırken iş kesme kuralına ait daha katı zorlamaya olanak sağlayan bir alternatif sunar, çünkü kapsayıcı ve sepetlerin hacimleri ile ilişki kısıtlamalarda daha büyük hata marjlarına olanak sağlar.</span><span class="sxs-lookup"><span data-stu-id="250e9-105">The *Cluster position full* feature offers an alternative to more rigid enforcement of work break rules when cluster picking is used, because it enables a larger margin of error in the volumetric constraints of containers or totes.</span></span> <span data-ttu-id="250e9-106">Ortak bir senaryoda, bir iş emrindeki tüm öğeler seçili bir kapsayıcıya sığmıyor.</span><span class="sxs-lookup"><span data-stu-id="250e9-106">In a common scenario, not all items on a work order fit into a selected container.</span></span> <span data-ttu-id="250e9-107">Küme malzeme çekme iş yapan ambar çalışanları bu senaryoda birkaç seçeneğe sahiptir: Ya daha büyük bir kapsayıcı boyutuna geçmeli ya da farklı bir çözüm bulmak için gözetmen ile çalışmalıdır.</span><span class="sxs-lookup"><span data-stu-id="250e9-107">Warehouse workers who are cluster picking have few options in this scenario: they must either change to a larger container size or work with their supervisor to come up with a different solution.</span></span>

<span data-ttu-id="250e9-108">Bu özellik, bir kümedeki çalışma birimlerinden birinde **Dolu** düğmesinin çalıştırılmasını sağlar.</span><span class="sxs-lookup"><span data-stu-id="250e9-108">This feature introduces the ability to run the **Full** button on one of the work units in a cluster.</span></span> <span data-ttu-id="250e9-109">Eski sürümlerde bu seçenek, küme çekmede değil, yalnızca normal sipariş çekmesinde kullanılabiliyordu.</span><span class="sxs-lookup"><span data-stu-id="250e9-109">In older versions, this option was available only for regular order picking, not for cluster picking.</span></span> <span data-ttu-id="250e9-110">Ancak, bu özellik kalan çalışmayı iptal eden standart **Dolu** düğmesinden farklıdır.</span><span class="sxs-lookup"><span data-stu-id="250e9-110">However, this feature differs from the standard **Full** button in that it cancels the remaining work.</span></span> <span data-ttu-id="250e9-111">Kullanıcının aynı kümeye başka bir bölme eklemesini önermez ve otomatik olarak yeni bir iş oluşturmaz.</span><span class="sxs-lookup"><span data-stu-id="250e9-111">It doesn't suggest that the user add another bin to the same cluster, and it doesn't automatically create new work.</span></span>

## <a name="turn-on-the-cluster-position-full-feature"></a><span data-ttu-id="250e9-112">Küme konumu dolu özelliğini açma</span><span class="sxs-lookup"><span data-stu-id="250e9-112">Turn on the Cluster position full feature</span></span>

<span data-ttu-id="250e9-113">Bu özelliği kullanabilmeniz için sisteminizde etkinleştirmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="250e9-113">Before you can use this feature, it must be turned on in your system.</span></span> <span data-ttu-id="250e9-114">Yöneticiler özellik durumunu denetlemek ve etkinleştirmek için [özellik yönetimi](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) ayarlarını kullanabilir.</span><span class="sxs-lookup"><span data-stu-id="250e9-114">Admins can use the [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) settings to check the status of the feature and turn it on.</span></span> <span data-ttu-id="250e9-115">**Özellik yönetimi** çalışma alanındabu özellik aşağıdaki şekilde listelenir:</span><span class="sxs-lookup"><span data-stu-id="250e9-115">In the **Feature management** workspace, the feature is listed in the following way:</span></span>

- <span data-ttu-id="250e9-116">**Modül:** *Ambar yönetimi*</span><span class="sxs-lookup"><span data-stu-id="250e9-116">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="250e9-117">**Özellik adı:** *Küme konumu dolu*</span><span class="sxs-lookup"><span data-stu-id="250e9-117">**Feature name:** *Cluster position full*</span></span>

## <a name="setup"></a><span data-ttu-id="250e9-118">Ayar</span><span class="sxs-lookup"><span data-stu-id="250e9-118">Setup</span></span>

<span data-ttu-id="250e9-119">Bu bölümde, yönergeler ile *küme konumu dolu* özelliğinin nasıl ayarlanacağını ve kullanılacağını gösteren bir örnek verilmiştir.</span><span class="sxs-lookup"><span data-stu-id="250e9-119">This section provides guidelines, and an example that shows how to set up and use the *Cluster position full* feature.</span></span>

### <a name="make-sample-data-available"></a><span data-ttu-id="250e9-120">Örnek verilerini kullanılabilir hale getirme</span><span class="sxs-lookup"><span data-stu-id="250e9-120">Make sample data available</span></span>

<span data-ttu-id="250e9-121">Burada belirtilen örnek kayıtları ve değerleri kullanarak [örnek senaryo](#example-scenario) üzerinden çalışmak için standart [demo verilerinin](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) yüklenmiş olduğu bir sistemde olmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="250e9-121">To work through the [example scenario](#example-scenario) by using the sample records and values that are specified here, you must be on a system where the standard [demo data](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) is installed.</span></span> <span data-ttu-id="250e9-122">Ek olarak, başlamadan önce **USMF** tüzel kişiliğini seçmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="250e9-122">Additionally, you must select the **USMF** legal entity before you begin.</span></span>

<span data-ttu-id="250e9-123">Örnek senaryodan, üretim sisteminde özelliği kullanmaya yönelik kılavuz olarak da yararlanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="250e9-123">You can also use the example scenario as guidance for working with this feature on a production system.</span></span> <span data-ttu-id="250e9-124">Ancak, bu durumda, burada açıklanan her ayar için kendi değerlerinizi kullanmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="250e9-124">However, in that case, you must substitute your own values for the settings that are described here.</span></span>

### <a name="cluster-profiles"></a><span data-ttu-id="250e9-125">Küme profilleri</span><span class="sxs-lookup"><span data-stu-id="250e9-125">Cluster profiles</span></span>

<span data-ttu-id="250e9-126">Küme kimliklerinin otomatik olarak oluşturulup oluşturulmayacağını, kaç pozisyonda kullanılacağını, kümelerin ne zaman kesileceğini ve malzeme çekme çalışmasının nasıl sıralandığını ve doğrulanacağını belirtmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="250e9-126">You must specify whether cluster IDs are automatically generated, how many positions are used, when clusters are broken, and how the picking work is sequenced and verified.</span></span>

1. <span data-ttu-id="250e9-127">**Ambar yönetimi \> Kurulum \> Mobil cihaz \> Küme profilleri**'ne tıklayın.</span><span class="sxs-lookup"><span data-stu-id="250e9-127">Go to **Warehouse management \> Setup \> Mobile device \> Cluster profiles**.</span></span>
1. <span data-ttu-id="250e9-128">Liste bölmesinde, **Küme Oluştur**'u seçin.</span><span class="sxs-lookup"><span data-stu-id="250e9-128">In the list pane, select the **Create Cluster** record.</span></span>
1. <span data-ttu-id="250e9-129">**Genel** hızlı sekmesinde, aşağıdaki değerleri doğrulayın:</span><span class="sxs-lookup"><span data-stu-id="250e9-129">On the **General** FastTab, verify the following values:</span></span>

    - <span data-ttu-id="250e9-130">**Küme kimliği oluştur:** *Evet*</span><span class="sxs-lookup"><span data-stu-id="250e9-130">**Generate cluster ID:** *Yes*</span></span>
    - <span data-ttu-id="250e9-131">**Pozisyonları etkinleştir:** *Evet*</span><span class="sxs-lookup"><span data-stu-id="250e9-131">**Activate positions:** *Yes*</span></span>
    - <span data-ttu-id="250e9-132">**Pozisyon sayısı:** *2*</span><span class="sxs-lookup"><span data-stu-id="250e9-132">**Number of positions:** *2*</span></span>
    - <span data-ttu-id="250e9-133">**Pozisyon adı:** *Sayısal*</span><span class="sxs-lookup"><span data-stu-id="250e9-133">**Position name:** *Numeric*</span></span>
    - <span data-ttu-id="250e9-134">**Kümeyi böl:** *Yerine koy*</span><span class="sxs-lookup"><span data-stu-id="250e9-134">**Break cluster at:** *Put*</span></span>
    - <span data-ttu-id="250e9-135">**Sıralama doğrulama türü:** *Pozisyon taraması*</span><span class="sxs-lookup"><span data-stu-id="250e9-135">**Sort verification type:** *Position scan*</span></span>

1. <span data-ttu-id="250e9-136">**Küme sıralama** hızlı sekmesinde.</span><span class="sxs-lookup"><span data-stu-id="250e9-136">In the **Cluster sorting** FastTab.</span></span> <span data-ttu-id="250e9-137">Kılavuz boş olmalıdır (başka bir deyişle, hiçbir satır içermemelidir).</span><span class="sxs-lookup"><span data-stu-id="250e9-137">The grid should be blank (that is, it should contain no lines).</span></span>

### <a name="work-templates"></a><span data-ttu-id="250e9-138">İş şablonları</span><span class="sxs-lookup"><span data-stu-id="250e9-138">Work templates</span></span>

<span data-ttu-id="250e9-139">Küme malzeme çekme için çekme işinin nasıl oluşturulacağını tanımlamanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="250e9-139">You must define how the picking work for cluster picking is created.</span></span>

1. <span data-ttu-id="250e9-140">**Ambar yönetimi \> Kurulum \> İş \> İş şablonları**'na gidin.</span><span class="sxs-lookup"><span data-stu-id="250e9-140">Go to **Warehouse management \> Setup \> Work \> Work templates**.</span></span>
1. <span data-ttu-id="250e9-141">Sayfanın üst kısmında, **İş emri türü** alanını *Satış siparişleri* olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="250e9-141">At the top of the page, set the **Work order type** field to *Sales orders*.</span></span>
1. <span data-ttu-id="250e9-142">Demo verilerinden alınan aşağıdaki çalışma şablonlarının listelendiğinden emin olun.</span><span class="sxs-lookup"><span data-stu-id="250e9-142">Make sure that the following work templates from the demo data are listed.</span></span> <span data-ttu-id="250e9-143">Kullanılabilir değillerse, senaryoyu tamamlayamazsınız.</span><span class="sxs-lookup"><span data-stu-id="250e9-143">If they aren't available, you won't be able to complete the scenario.</span></span>

    - <span data-ttu-id="250e9-144">61 Satış Siparişi Hazırlama</span><span class="sxs-lookup"><span data-stu-id="250e9-144">61 SO Stage</span></span>
    - <span data-ttu-id="250e9-145">61 Satış Siparişi Küme malzeme çekme</span><span class="sxs-lookup"><span data-stu-id="250e9-145">61 SO Cluster pick</span></span>

### <a name="location-directives"></a><span data-ttu-id="250e9-146">Konum yönergeleri</span><span class="sxs-lookup"><span data-stu-id="250e9-146">Location directives</span></span>

<span data-ttu-id="250e9-147">Maddelerin nereden çekildiklerini ve nereye koyulacağını belirtmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="250e9-147">You must specify where items are picked from and where they are put.</span></span>

1. <span data-ttu-id="250e9-148">**Ambar Yönetimi \> Kurulum \> Konum yönergeleri** seçeneğine gidin.</span><span class="sxs-lookup"><span data-stu-id="250e9-148">Go to **Warehouse management \> Setup \> Location directives**.</span></span>
1. <span data-ttu-id="250e9-149">Liste başlığında **İş emri türü** alanını *Satış siparişleri* olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="250e9-149">In the list header, set the **Work order type** field to *Sales orders*.</span></span>
1. <span data-ttu-id="250e9-150">Demo verilerinden alınan aşağıdaki satış yönergelerinin listelendiğinden emin olun.</span><span class="sxs-lookup"><span data-stu-id="250e9-150">Make sure that the following sales order directives from the demo data are listed.</span></span> <span data-ttu-id="250e9-151">Kullanılabilir değillerse, senaryoyu tamamlayamazsınız.</span><span class="sxs-lookup"><span data-stu-id="250e9-151">If they aren't available, you won't be able to complete the scenario.</span></span>

    - <span data-ttu-id="250e9-152">61 Küme malzeme çekme</span><span class="sxs-lookup"><span data-stu-id="250e9-152">61 Cluster pick</span></span>
    - <span data-ttu-id="250e9-153">61 Satış Siparişi Malzeme çekme emri</span><span class="sxs-lookup"><span data-stu-id="250e9-153">61 SO Pick order</span></span>

### <a name="mobile-device-menu-items"></a><span data-ttu-id="250e9-154">Mobil cihaz menü öğeleri</span><span class="sxs-lookup"><span data-stu-id="250e9-154">Mobile device menu items</span></span>

<span data-ttu-id="250e9-155">Küme malzeme çekme tarafından yönlendirilen mevcut işi kullanmak için bir mobil cihaz menü öğesini yapılandırmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="250e9-155">You must configure a mobile device menu item to use existing work that is directed by cluster picking.</span></span> <span data-ttu-id="250e9-156">Küme malzeme çekme işlemi için mobil cihaz menü öğesinde, **İşin bölünmesine izin ver** parametresi açık olmalıdır ve *Satış Siparişi Malzeme Çekme* iş sınıfı eklenmelidir.</span><span class="sxs-lookup"><span data-stu-id="250e9-156">In the mobile device menu item for cluster picking, the **Allow splitting of work** parameter must be turned on, and the *SO Pick* work class must be added.</span></span>

1. <span data-ttu-id="250e9-157">**Ambar yönetimi \> Kurulum \> Mobil cihaz \> Mobil cihaz menüsü öğeleri**'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="250e9-157">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu items**.</span></span>
1. <span data-ttu-id="250e9-158">Liste bölmesinde, **Küme Malzeme Çekme Oluştur** kaydını seçin.</span><span class="sxs-lookup"><span data-stu-id="250e9-158">In the list pane, select the **Cluster Pick Create** record.</span></span>
1. <span data-ttu-id="250e9-159">Eylem bölmesinde, **Düzenle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="250e9-159">Select **Edit** in the Action pane.</span></span>
1. <span data-ttu-id="250e9-160">**Genel** hızlı sekmesinde, aşağıdaki değerleri ayarlayın:</span><span class="sxs-lookup"><span data-stu-id="250e9-160">On the **General** FastTab, set the following values:</span></span>

    - <span data-ttu-id="250e9-161">**Yöneten:** *Küme malzeme çekme*</span><span class="sxs-lookup"><span data-stu-id="250e9-161">**Directed by:** *Cluster picking*</span></span>
    - <span data-ttu-id="250e9-162">**Plaka oluştur:** *Evet*</span><span class="sxs-lookup"><span data-stu-id="250e9-162">**Generate license plate:** *Yes*</span></span>
    - <span data-ttu-id="250e9-163">**İşin bölünmesine izin ver:** *Evet*</span><span class="sxs-lookup"><span data-stu-id="250e9-163">**Allow splitting of work:** *Yes*</span></span>
    - <span data-ttu-id="250e9-164">**Küme profili kimliği:** *Küme oluştur*</span><span class="sxs-lookup"><span data-stu-id="250e9-164">**Cluster profile ID:** *Create Cluster*</span></span>

    <span data-ttu-id="250e9-165">Tüm diğer alanlar için varsayılan değerleri kabul edin.</span><span class="sxs-lookup"><span data-stu-id="250e9-165">Accept the default values for all other fields.</span></span>

1. <span data-ttu-id="250e9-166">**İş sınıfları** hızlı sekmesinde, gerektiğinde aşağıdaki iki satırı ekleyin:</span><span class="sxs-lookup"><span data-stu-id="250e9-166">On the **Work classes** FastTab, add the following two lines, as required:</span></span>

    - <span data-ttu-id="250e9-167">Satır 1 (genellikle demo verilerinde vardır):</span><span class="sxs-lookup"><span data-stu-id="250e9-167">Line 1 (usually present in demo data):</span></span>

        - <span data-ttu-id="250e9-168">**İş sınıfı kodu:** *Satış*</span><span class="sxs-lookup"><span data-stu-id="250e9-168">**Work class ID:** *Sales*</span></span> 
        - <span data-ttu-id="250e9-169">**İş emri türü:** *Satış siparişleri*</span><span class="sxs-lookup"><span data-stu-id="250e9-169">**Work order type:** *Sales orders*</span></span>

    - <span data-ttu-id="250e9-170">Satır 2 (demo verilerinde olmayabilir):</span><span class="sxs-lookup"><span data-stu-id="250e9-170">Line 2 (probably not present in demo data):</span></span>

        - <span data-ttu-id="250e9-171">**İş sınıfı kodu:** *Satış Siparişi Çekme*</span><span class="sxs-lookup"><span data-stu-id="250e9-171">**Work class ID:** *SO Pick*</span></span>
        - <span data-ttu-id="250e9-172">**İş emri türü:** *Satış siparişleri*</span><span class="sxs-lookup"><span data-stu-id="250e9-172">**Work order type:** *Sales orders*</span></span>

1. <span data-ttu-id="250e9-173">Eylem bölmesinde **İş onayı kurulumu** bölümüne gidin.</span><span class="sxs-lookup"><span data-stu-id="250e9-173">Go to **Work confirmation setup** in the Action pane.</span></span>
1. <span data-ttu-id="250e9-174">**Düzenle** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="250e9-174">Select **Edit**.</span></span>
1. <span data-ttu-id="250e9-175">Kılavuzda satıra aşağıdaki değerleri girin.</span><span class="sxs-lookup"><span data-stu-id="250e9-175">Enter the following values on the line in grid.</span></span>
    - <span data-ttu-id="250e9-176">**İş türü** - *Çekme*</span><span class="sxs-lookup"><span data-stu-id="250e9-176">**Work type** - *Pick*</span></span>
    - <span data-ttu-id="250e9-177">**Ürün onayı** - *Onay kutusunu seç*</span><span class="sxs-lookup"><span data-stu-id="250e9-177">**Product confirmation** - *Select the check box*</span></span>

1. <span data-ttu-id="250e9-178">Eylem bölmesinde **Kaydet**'i seçin ve sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="250e9-178">Select **Save** in the Action pane and close the page.</span></span>

## <a name="create-picking-work"></a><span data-ttu-id="250e9-179">Malzeme çekme işi oluştur</span><span class="sxs-lookup"><span data-stu-id="250e9-179">Create picking work</span></span>

<span data-ttu-id="250e9-180">Küme çekmeyi başlatabilmeniz için önce, bazı çıkış çalışmaları oluşturmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="250e9-180">Before you can start cluster picking, you must create some outbound work.</span></span> <span data-ttu-id="250e9-181">Daha önce oluşturduğunuz küme profilinde iki küme konumu belirtilir.</span><span class="sxs-lookup"><span data-stu-id="250e9-181">The cluster profile that you created earlier specifies two cluster positions.</span></span> <span data-ttu-id="250e9-182">Bu nedenle, satış siparişi çekme için en az iki iş kodu oluşturulmalıdır.</span><span class="sxs-lookup"><span data-stu-id="250e9-182">Therefore, at least two work IDs must be created for sales order picking.</span></span> <span data-ttu-id="250e9-183">Bu senaryoda, ambar *61*'de hareketler gerçekleşir ve bunlar *L0101* ve *T0100* öğelerini kullanır.</span><span class="sxs-lookup"><span data-stu-id="250e9-183">For this scenario, transactions will occur in warehouse *61*, and they will use items *L0101* and *T0100*.</span></span> <span data-ttu-id="250e9-184">Demo verilerinde bu maddelerin elde yeterli miktarda stokunun bulunması gerekir.</span><span class="sxs-lookup"><span data-stu-id="250e9-184">The demo data should have enough on-hand inventory of these items.</span></span> <span data-ttu-id="250e9-185">Hareketleri tamamlamak için yeterli stokunuzun bulunduğundan emin olun.</span><span class="sxs-lookup"><span data-stu-id="250e9-185">Make sure that you have enough inventory to complete the transactions.</span></span>

### <a name="create-sales-order-1"></a><span data-ttu-id="250e9-186">Satış siparişi oluşturma 1</span><span class="sxs-lookup"><span data-stu-id="250e9-186">Create sales order 1</span></span>

1. <span data-ttu-id="250e9-187">**Satış ve Pazarlama \> Satış siparişleri \> Tüm satış siparişleri**'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="250e9-187">Go to **Sales and Marketing \> Sales orders \> All sales orders**.</span></span>
1. <span data-ttu-id="250e9-188">Satış siparişi 1'i oluşturmak için **Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="250e9-188">Select **New** to create sales order 1.</span></span>
1. <span data-ttu-id="250e9-189">**Satış siparişi oluştur** iletişim kutusunda, aşağıdaki değerleri ayarlayın:</span><span class="sxs-lookup"><span data-stu-id="250e9-189">In the **Create sales order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="250e9-190">**Müşteri hesabı:** *US-010*</span><span class="sxs-lookup"><span data-stu-id="250e9-190">**Customer account:** *US-010*</span></span>
    - <span data-ttu-id="250e9-191">**Ambar:** *61*</span><span class="sxs-lookup"><span data-stu-id="250e9-191">**Warehouse:** *61*</span></span>

1. <span data-ttu-id="250e9-192">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="250e9-192">Select **OK**.</span></span>
1. <span data-ttu-id="250e9-193">Yeni satış siparişi açılır.</span><span class="sxs-lookup"><span data-stu-id="250e9-193">The new sales order is opened.</span></span> <span data-ttu-id="250e9-194">**Satış siparişi satırları** hızlı sekmesinde, aşağıdaki ayarlara sahip bir satır ekleyin:</span><span class="sxs-lookup"><span data-stu-id="250e9-194">On the **Sales order lines** FastTab, add a line that has the following settings:</span></span>

    - <span data-ttu-id="250e9-195">**Madde numarası:** *T0100*</span><span class="sxs-lookup"><span data-stu-id="250e9-195">**Item number:** *T0100*</span></span>
    - <span data-ttu-id="250e9-196">**Miktar:** *5*</span><span class="sxs-lookup"><span data-stu-id="250e9-196">**Quantity:** *5*</span></span>

1. <span data-ttu-id="250e9-197">**Satır ayrıntıları** hızlı sekmesinin **Teslimat** sekmesinde **Onaylanan sevkiyat tarihi** alanını bugünün tarihine ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="250e9-197">On the **Line details** FastTab, on the **Delivery** tab, set the **Confirmed ship date** field to today's date.</span></span>
1. <span data-ttu-id="250e9-198">**Satış siparişi satırları** hızlı sekmesinde, aşağıdaki ayarlara sahip ikinci satırı ekleyin:</span><span class="sxs-lookup"><span data-stu-id="250e9-198">On the **Sales order lines** FastTab, add a second line that has the following settings:</span></span>

    - <span data-ttu-id="250e9-199">**Madde numarası:** *L0101*</span><span class="sxs-lookup"><span data-stu-id="250e9-199">**Item number:** *L0101*</span></span>
    - <span data-ttu-id="250e9-200">**Miktar:** *20*</span><span class="sxs-lookup"><span data-stu-id="250e9-200">**Quantity:** *20*</span></span>

1. <span data-ttu-id="250e9-201">**Satır ayrıntıları** hızlı sekmesinin **Teslimat** sekmesinde **Onaylanan sevkiyat tarihi** alanını bugünün tarihine ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="250e9-201">On the **Line details** FastTab, on the **Delivery** tab, set the **Confirmed ship date** field to today's date.</span></span>
1. <span data-ttu-id="250e9-202">Yeni eklediğiniz her satır için, stoku rezerve etmek üzere aşağıdaki adımları izleyin:</span><span class="sxs-lookup"><span data-stu-id="250e9-202">For each line that you just added, follow these steps to reserve inventory:</span></span>

    1. <span data-ttu-id="250e9-203">Rezerve edilecek satırı seçin.</span><span class="sxs-lookup"><span data-stu-id="250e9-203">Select the line to reserve.</span></span>
    2. <span data-ttu-id="250e9-204">**Satış siparişi satırları** hızlı sekmesinde **Stok \> Rezervasyon**'u seçin.</span><span class="sxs-lookup"><span data-stu-id="250e9-204">On the **Sales order lines** FastTab, select **Inventory \> Reservation**.</span></span>
    3. <span data-ttu-id="250e9-205">**Rezervasyon** sayfasında, Eylem Bölmesi'nde stok rezerve etmek için **Lotu rezerve et**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="250e9-205">On the **Reservation** page, on the Action Pane, select **Reserve lot** to reserve the inventory.</span></span>
    4. <span data-ttu-id="250e9-206">**Rezervasyon** sayfasını kapatın.</span><span class="sxs-lookup"><span data-stu-id="250e9-206">Close the **Reservation** page.</span></span>

1. <span data-ttu-id="250e9-207">Eylem bölmesinde, **Ambar** sekmesinde **Ambara serbest bırak**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="250e9-207">On the Action Pane, on the **Warehouse** tab, select **Release to warehouse**.</span></span>

    <span data-ttu-id="250e9-208">Serbest bırakma işlemi tamamlanınca oluşturulan dalga kimliğini ve yük kimliklerini gösteren bilgi iletileri alırsınız.</span><span class="sxs-lookup"><span data-stu-id="250e9-208">When the release is completed, you receive informational messages that show the wave and load IDs that were created.</span></span>

### <a name="create-sales-order-2"></a><span data-ttu-id="250e9-209">Satış siparişi oluşturma 2</span><span class="sxs-lookup"><span data-stu-id="250e9-209">Create sales order 2</span></span>

1. <span data-ttu-id="250e9-210">**Satış ve Pazarlama \> Satış siparişleri \> Tüm satış siparişleri**'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="250e9-210">Go to **Sales and Marketing \> Sales orders \> All sales orders**.</span></span>
1. <span data-ttu-id="250e9-211">Satış siparişi 2'i oluşturmak için **Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="250e9-211">Select **New** to create sales order 2.</span></span>
1. <span data-ttu-id="250e9-212">**Satış siparişi oluştur** iletişim kutusunda, aşağıdaki değerleri ayarlayın:</span><span class="sxs-lookup"><span data-stu-id="250e9-212">In the **Create sales order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="250e9-213">**Müşteri hesabı:** *US-011*</span><span class="sxs-lookup"><span data-stu-id="250e9-213">**Customer account:** *US-011*</span></span>
    - <span data-ttu-id="250e9-214">**Ambar:** *61*</span><span class="sxs-lookup"><span data-stu-id="250e9-214">**Warehouse:** *61*</span></span>

1. <span data-ttu-id="250e9-215">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="250e9-215">Select **OK**.</span></span>
1. <span data-ttu-id="250e9-216">Yeni satış siparişi açılır.</span><span class="sxs-lookup"><span data-stu-id="250e9-216">The new sales order is opened.</span></span> <span data-ttu-id="250e9-217">**Satış siparişi satırları** hızlı sekmesinde, aşağıdaki ayarlara sahip bir satır ekleyin:</span><span class="sxs-lookup"><span data-stu-id="250e9-217">On the **Sales order lines** FastTab, add a line that has the following settings:</span></span>

    - <span data-ttu-id="250e9-218">**Madde numarası:** *L0101*</span><span class="sxs-lookup"><span data-stu-id="250e9-218">**Item number:** *L0101*</span></span>
    - <span data-ttu-id="250e9-219">**Miktar:** *20*</span><span class="sxs-lookup"><span data-stu-id="250e9-219">**Quantity:** *20*</span></span>

1. <span data-ttu-id="250e9-220">**Satır ayrıntıları** hızlı sekmesinin **Teslimat** sekmesinde **Onaylanan sevkiyat tarihi** alanını bugünün tarihine ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="250e9-220">On the **Line details** FastTab, on the **Delivery** tab, set the **Confirmed ship date** field to today's date.</span></span>
1. <span data-ttu-id="250e9-221">**Satış siparişi satırları** hızlı sekmesinde, aşağıdaki ayarlara sahip ikinci satırı ekleyin:</span><span class="sxs-lookup"><span data-stu-id="250e9-221">On the **Sales order lines** FastTab, add a second line that has the following settings:</span></span>

    - <span data-ttu-id="250e9-222">**Madde numarası:** *T0100*</span><span class="sxs-lookup"><span data-stu-id="250e9-222">**Item number:** *T0100*</span></span>
    - <span data-ttu-id="250e9-223">**Miktar:** *2*</span><span class="sxs-lookup"><span data-stu-id="250e9-223">**Quantity:** *2*</span></span>

1. <span data-ttu-id="250e9-224">**Satır ayrıntıları** hızlı sekmesinin **Teslimat** sekmesinde **Onaylanan sevkiyat tarihi** alanını bugünün tarihine ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="250e9-224">On the **Line details** FastTab, on the **Delivery** tab, set the **Confirmed ship date** field to today's date.</span></span>
1. <span data-ttu-id="250e9-225">Yeni eklediğiniz her satır için, stoku rezerve etmek üzere aşağıdaki adımları izleyin:</span><span class="sxs-lookup"><span data-stu-id="250e9-225">For each line that you just added, follow these steps to reserve inventory:</span></span>

    1. <span data-ttu-id="250e9-226">Rezerve edilecek satırı seçin.</span><span class="sxs-lookup"><span data-stu-id="250e9-226">Select the line to reserve.</span></span>
    2. <span data-ttu-id="250e9-227">**Satış siparişi satırları** hızlı sekmesinde **Stok \> Rezervasyon**'u seçin.</span><span class="sxs-lookup"><span data-stu-id="250e9-227">On the **Sales order lines** FastTab, select **Inventory \> Reservation**.</span></span>
    3. <span data-ttu-id="250e9-228">**Rezervasyon** sayfasında, Eylem Bölmesi'nde stok rezerve etmek için **Lotu rezerve et**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="250e9-228">On the **Reservation** page, on the Action Pane, select **Reserve lot** to reserve the inventory.</span></span>
    4. <span data-ttu-id="250e9-229">**Rezervasyon** sayfasını kapatın.</span><span class="sxs-lookup"><span data-stu-id="250e9-229">Close the **Reservation** page.</span></span>

1. <span data-ttu-id="250e9-230">Eylem bölmesinde, **Ambar** sekmesinde **Ambara serbest bırak**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="250e9-230">On the Action Pane, on the **Warehouse** tab, select **Release to warehouse**.</span></span>

    <span data-ttu-id="250e9-231">Serbest bırakma işlemi tamamlanınca oluşturulan dalga kimliğini ve yük kimliklerini gösteren bilgi iletileri alırsınız.</span><span class="sxs-lookup"><span data-stu-id="250e9-231">When the release is completed, you receive informational messages that show the wave and load IDs that were created.</span></span>

### <a name="get-work-ids-and-license-plate-numbers"></a><span data-ttu-id="250e9-232">İş kimliklerini ve plaka numaralarını alma</span><span class="sxs-lookup"><span data-stu-id="250e9-232">Get work IDs and license plate numbers</span></span>

<span data-ttu-id="250e9-233">Her biri iki çekme satırı içeren iki iş kodu oluşturulmalıdır.</span><span class="sxs-lookup"><span data-stu-id="250e9-233">Two work IDs should have been created, each of which has two pick lines.</span></span> <span data-ttu-id="250e9-234">İş kimliklerini ve plaka atamalarını bulmak için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="250e9-234">Follow these steps to find the work IDs and license plate assignments.</span></span>

1. <span data-ttu-id="250e9-235">**Ambar yönetimi \> İş \> İş ayrıntıları**'na gidin.</span><span class="sxs-lookup"><span data-stu-id="250e9-235">Go to **Warehouse management \> Work \> Work details**.</span></span>
1. <span data-ttu-id="250e9-236">**Genel Bakış** kılavuzunda, az önce oluşturduğunuz iki satış siparişi için **Sipariş numarası** sütununu arayın.</span><span class="sxs-lookup"><span data-stu-id="250e9-236">In the **Overview** grid, search the **Order number** column for the two sales orders that you just created.</span></span> <span data-ttu-id="250e9-237">Her satış siparişi için ilişkili iş kodunu not edin.</span><span class="sxs-lookup"><span data-stu-id="250e9-237">For each sales order, make a note of the corresponding work ID.</span></span>
1. <span data-ttu-id="250e9-238">**Satır** kılavuzunda ilgili bilgileri göstermek üzere her satış siparişinin satırını seçin.</span><span class="sxs-lookup"><span data-stu-id="250e9-238">Select the row for each sales order to show related information in the **Lines** grid.</span></span> <span data-ttu-id="250e9-239">Her bir maddenin hangi konumdan çekileceğini not edin.</span><span class="sxs-lookup"><span data-stu-id="250e9-239">Make a note of the location that each item will be picked from.</span></span>
1. <span data-ttu-id="250e9-240">**Stok yönetimi \> Sorgular ve raporlar \>> Eldeki stok** öğesine gidin.</span><span class="sxs-lookup"><span data-stu-id="250e9-240">Go to **Inventory management \> Inquiries and reports \> On-hand list**.</span></span>
1. <span data-ttu-id="250e9-241">Eylem Bölmesi'nde, **Boyut görünümü** iletişim kutusunu açmak için **Boyutlar**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="250e9-241">On the Action Pane, select **Dimensions** to open the **Dimension display** dialog box.</span></span>
1. <span data-ttu-id="250e9-242">**Plaka**, **Ambar** ve **Madde numarası** onay kutularının işaretlendiğinden emin olun ve **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="250e9-242">Make sure that the **License plate**, **Warehouse**, and **Item number** check boxes are selected, and then select **OK**.</span></span>
1. <span data-ttu-id="250e9-243">**Filtre** bölmesinde, aşağıdaki filtreleri ayarlayın:</span><span class="sxs-lookup"><span data-stu-id="250e9-243">In the **Filter** pane, set the following filters:</span></span>

    - <span data-ttu-id="250e9-244">**Madde numarası** – **biri** - *L0101* ve *T100*</span><span class="sxs-lookup"><span data-stu-id="250e9-244">**Item number** – **is one of** – *L0101* and *T100*</span></span>
    - <span data-ttu-id="250e9-245">**Ambar** – **ile başlar** - *61*</span><span class="sxs-lookup"><span data-stu-id="250e9-245">**Warehouse** – **begins with** – *61*</span></span>

1. <span data-ttu-id="250e9-246">Gösterilen **Plaka numarası** değerlerini not edin.</span><span class="sxs-lookup"><span data-stu-id="250e9-246">Make a note of the **License plate** values that are shown.</span></span>

## <a name="example-scenario"></a><a name="example-scenario"></a><span data-ttu-id="250e9-247">Örnek senaryo</span><span class="sxs-lookup"><span data-stu-id="250e9-247">Example scenario</span></span>

### <a name="mobile-device-flow-execution--work-confirmation-setup-for-the-product"></a><span data-ttu-id="250e9-248">Mobil cihaz akışı yürütme – ürün için çalışma onayı kurulumu</span><span class="sxs-lookup"><span data-stu-id="250e9-248">Mobile device flow execution – Work confirmation setup for the product</span></span>

1. <span data-ttu-id="250e9-249">Ambar uygulamasında ambar *61*'deki bir kullanıcı olarak oturum açın.</span><span class="sxs-lookup"><span data-stu-id="250e9-249">Sign in to the warehouse app as a user in warehouse *61*.</span></span>
1. <span data-ttu-id="250e9-250">**Giden \> Küme malzeme çekme oluşturma** bölümüne gidin.</span><span class="sxs-lookup"><span data-stu-id="250e9-250">Go to **Outbound \> Cluster pick create**.</span></span>

    <span data-ttu-id="250e9-251">**GÖREV: Kümeye iş ata** sayfası görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="250e9-251">The **TASK: Assign work to Cluster** page appears.</span></span>

1. <span data-ttu-id="250e9-252">Küme konumu 1'e atamak üzere satış siparişi 1 için iş kimliği girin.</span><span class="sxs-lookup"><span data-stu-id="250e9-252">Enter the work ID for sales order 1 to assign it to cluster position 1.</span></span>
1. <span data-ttu-id="250e9-253">**Tamam**'ı (onay işareti simgesi) seçin.</span><span class="sxs-lookup"><span data-stu-id="250e9-253">Select **OK** (check mark symbol).</span></span>
1. <span data-ttu-id="250e9-254">Küme konumu 2'e atamak üzere satış siparişi 2 için iş kimliği girin.</span><span class="sxs-lookup"><span data-stu-id="250e9-254">Enter the work ID for sales order 2 to assign it to cluster position 2.</span></span>
1. <span data-ttu-id="250e9-255">**Tamam**'ı (onay işareti simgesi) seçin.</span><span class="sxs-lookup"><span data-stu-id="250e9-255">Select **OK** (check mark symbol).</span></span>

    <span data-ttu-id="250e9-256">**Görev: Küme Malzeme Çekme Oluşturma: Çekme** sayfası açılır ve *Madde L0101 2 PL* görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="250e9-256">The **TASK: Cluster Pick Create: Pick** page appears and shows *Item L0101 2 PL*.</span></span>

<span data-ttu-id="250e9-257">Küme profili pozisyon sayısını 2 olarak ayarladığından, sistem sizi otomatik olarak ilk konsolide malzeme çekmeye yönlendirir: madde *L0101* için iki palet (PL).</span><span class="sxs-lookup"><span data-stu-id="250e9-257">Because the cluster profile set the number of positions to 2, the system automatically directs you to the first consolidate pick: two pallets (PL) of item *L0101*.</span></span>

<span data-ttu-id="250e9-258">Aşağıdaki adımlarda herhangi bir zamanda, malzeme çekme konumu gibi görevle ilgili ek bilgileri görüntülemek için **Ayrıntılar** sekmesini seçebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="250e9-258">At any time during the following steps, you can select the **Details** tab to view additional information about the task, such as the picking location.</span></span>

1. <span data-ttu-id="250e9-259">**MADDE** alanını *L0101* olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="250e9-259">Set the **ITEM** field to *L0101*.</span></span> <span data-ttu-id="250e9-260">Bu menü maddesi için gerekli olan madde numarası bu şekilde onaylanır. (Bu menü öğesini oluştururken **Mobil cihaz menü öğesi** sayfasından **İş onayı kurulumunu** seçerek daha önce yapılandırabilirsiniz.)</span><span class="sxs-lookup"><span data-stu-id="250e9-260">This confirms the item number, which is required for this menu item (you configured this earlier by selecting **Work confirmation setup**  from the **Mobile device menu item** page when you created this menu item).</span></span>
1. <span data-ttu-id="250e9-261">Konumda çekilen maddeyle ilişkilendirilmiş olan plaka numarasını girin.</span><span class="sxs-lookup"><span data-stu-id="250e9-261">Enter the license plate number that is associated with the item in the location that is being picked.</span></span> <span data-ttu-id="250e9-262">İki palet çekersiniz.</span><span class="sxs-lookup"><span data-stu-id="250e9-262">You will pick two pallets.</span></span>
1. <span data-ttu-id="250e9-263">**LP** alanını *LP\_PICK\_01* olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="250e9-263">Set the **LP** field to *LP\_PICK\_01*.</span></span>
1. <span data-ttu-id="250e9-264">**Tamam**'ı (onay işareti simgesi) seçin.</span><span class="sxs-lookup"><span data-stu-id="250e9-264">Select **OK** (check mark symbol).</span></span>

    <span data-ttu-id="250e9-265">**GÖREV: Sıralama: Küme Çekme Oluşturma** sayfası görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="250e9-265">The **TASK: Sort: Cluster Pick Create** page appears.</span></span> <span data-ttu-id="250e9-266">Burada, iki çekilen paleti bir çekme konumuna sıralamanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="250e9-266">Here, you will sort the two picked pallets into a pick position.</span></span> <span data-ttu-id="250e9-267">Bu pozisyon, çekilen stoku satış siparişine göre ayırmak için kullanılan bir sepet veya kapsayıcı olabilir.</span><span class="sxs-lookup"><span data-stu-id="250e9-267">This position might be a tote or container that is used to separate the picked inventory by sales order.</span></span>

1. <span data-ttu-id="250e9-268">(Satış siparişi 1 için) pozisyon 1'e sıralanacak madde (*L0101*) ve miktar (*20* ea) için gösterilen ayrıntıları görüntüleyin.</span><span class="sxs-lookup"><span data-stu-id="250e9-268">View the details that are shown for the item (*L0101*) and quantity (*20* ea) that will be sorted into position 1 (for sales order 1).</span></span>
1. <span data-ttu-id="250e9-269">**POZİSYON NA** alanını *1* olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="250e9-269">Set the **POSITION NA** field to *1*.</span></span>
1. <span data-ttu-id="250e9-270">**Tamam**'ı (onay işareti simgesi) seçin.</span><span class="sxs-lookup"><span data-stu-id="250e9-270">Select **OK** (check mark symbol).</span></span>
1. <span data-ttu-id="250e9-271">(Satış siparişi 2 için) pozisyon 2'e sıralanacak madde (*L0101*) ve miktar (*20* ea) için gösterilen ayrıntıları görüntüleyin.</span><span class="sxs-lookup"><span data-stu-id="250e9-271">View the details that are shown for the item (*L0101*) and quantity (*20* ea) that will be sorted into position 2 (for sales order 2).</span></span>
1. <span data-ttu-id="250e9-272">**POZİSYON NA** alanını *2* olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="250e9-272">Set the **POSITION NA** field to *2*.</span></span>
1. <span data-ttu-id="250e9-273">**Tamam**'ı (onay işareti simgesi) seçin.</span><span class="sxs-lookup"><span data-stu-id="250e9-273">Select **OK** (check mark symbol).</span></span>

    <span data-ttu-id="250e9-274">**GÖREV: Küme Malzeme Çekme Oluşturma: Çekme** sayfası açılır ve *Madde T0100 7 ea* görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="250e9-274">The **TASK: Cluster Pick Create: Pick** page appears and shows *Item T0100 7 ea*.</span></span>

<span data-ttu-id="250e9-275">Bu senaryoda, pozisyon 1, satış siparişi 1'i karşılamak için çekilmesi gereken tüm madde miktarını kabul edemez.</span><span class="sxs-lookup"><span data-stu-id="250e9-275">In this scenario, position 1 can't accept the full quantity of items that must be picked to fulfill sales order 1.</span></span> <span data-ttu-id="250e9-276">Pozisyonun tam olarak işaretlenmesi gerekir.</span><span class="sxs-lookup"><span data-stu-id="250e9-276">A position must be marked as full.</span></span> <span data-ttu-id="250e9-277">Bu senaryoda, ikinci öğe kısmen çekilir.</span><span class="sxs-lookup"><span data-stu-id="250e9-277">In this scenario, you will do a partial pick of the second item.</span></span> <span data-ttu-id="250e9-278">İkinci madde pozisyon 1 için kısmen çekilir ve siparişin karşılanması için kalan miktarı çekmek üzere yeni iş oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="250e9-278">The second item will be partially picked for position 1, and new work will be created to pick the remaining quantity to fulfill the order.</span></span>

1. <span data-ttu-id="250e9-279">Menü düğmesini seçin (bazen hamburger veya hamburger düğmesi olarak da adlandırılır) ve **Pozisyon dolu** seçeneğini belirleyin.</span><span class="sxs-lookup"><span data-stu-id="250e9-279">Select the Menu button (sometimes referred to as the hamburger or the hamburger button), and then select **Position full**.</span></span>
1. <span data-ttu-id="250e9-280">Dolu olan konumu tanımlayın ve *1*'i seçin.</span><span class="sxs-lookup"><span data-stu-id="250e9-280">Identify the position that is full, and select *1*.</span></span>
1. <span data-ttu-id="250e9-281">**Tamam**'ı (onay işareti simgesi) seçin.</span><span class="sxs-lookup"><span data-stu-id="250e9-281">Select **OK** (check mark symbol).</span></span>
1. <span data-ttu-id="250e9-282">Yine de, pozisyon 1'e çekilecek malzeme çekme miktarını girin.</span><span class="sxs-lookup"><span data-stu-id="250e9-282">Enter the pick quantity that can still be picked into position 1.</span></span> <span data-ttu-id="250e9-283">Sistem hangi madde numarasının çekileceğini belirleyebilir.</span><span class="sxs-lookup"><span data-stu-id="250e9-283">The system can determine which item number is being picked.</span></span>
1. <span data-ttu-id="250e9-284">*2* girin.</span><span class="sxs-lookup"><span data-stu-id="250e9-284">Enter *2*.</span></span>
1. <span data-ttu-id="250e9-285">**Tamam**'ı (onay işareti simgesi) seçin.</span><span class="sxs-lookup"><span data-stu-id="250e9-285">Select **OK** (check mark symbol).</span></span>
1. <span data-ttu-id="250e9-286">Kalan maddenin çekme işlemini, pozisyon 2 olarak tamamlamak için madde numarasını onaylayın.</span><span class="sxs-lookup"><span data-stu-id="250e9-286">Confirm the item number to complete the pick of the remaining item into position 2.</span></span>
1. <span data-ttu-id="250e9-287">**MADDE** alanını *T0100* olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="250e9-287">Set the **ITEM** field to *T0100*.</span></span>
1. <span data-ttu-id="250e9-288">**Tamam**'ı (onay işareti simgesi) seçin.</span><span class="sxs-lookup"><span data-stu-id="250e9-288">Select **OK** (check mark symbol).</span></span>
1. <span data-ttu-id="250e9-289">**LP** alanını *LPREPL04* olarak ayarlayarak, maddenin çekildiği plaka numarasını girin.</span><span class="sxs-lookup"><span data-stu-id="250e9-289">Enter the license plate that the item is being picked from by setting the **LP** field to *LPREPL04*.</span></span>
1. <span data-ttu-id="250e9-290">**Tamam**'ı (onay işareti simgesi) seçin.</span><span class="sxs-lookup"><span data-stu-id="250e9-290">Select **OK** (check mark symbol).</span></span>
1. <span data-ttu-id="250e9-291">(Satış siparişi 2 için) pozisyon 2'e sıralanacak madde (*T0100*) ve miktar (*2* ea) için gösterilen ayrıntıları görüntüleyin.</span><span class="sxs-lookup"><span data-stu-id="250e9-291">View the details that are shown for the item (*T0100*) and quantity (*2* ea) that will be sorted into position 2 (for sales order 2).</span></span>
1. <span data-ttu-id="250e9-292">**POZİSYON NA** alanını *2* olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="250e9-292">Set the **POSITION NA** field to *2*.</span></span>
1. <span data-ttu-id="250e9-293">**Tamam**'ı (onay işareti simgesi) seçin.</span><span class="sxs-lookup"><span data-stu-id="250e9-293">Select **OK** (check mark symbol).</span></span>
1. <span data-ttu-id="250e9-294">(Satış siparişi 1 için) pozisyon 1'e sıralanacak madde (*T0100*) ve miktar (*2* ea) için gösterilen ayrıntıları görüntüleyin.</span><span class="sxs-lookup"><span data-stu-id="250e9-294">View the details that are shown for the item (*T0100*) and quantity (*2* ea) that will be sorted into position 1 (for sales order 1).</span></span>
1. <span data-ttu-id="250e9-295">**POZİSYON NA** alanını *1* olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="250e9-295">Set the **POSITION NA** field to *1*.</span></span>
1. <span data-ttu-id="250e9-296">**Tamam**'ı (onay işareti simgesi) seçin.</span><span class="sxs-lookup"><span data-stu-id="250e9-296">Select **OK** (check mark symbol).</span></span>

    <span data-ttu-id="250e9-297">**GÖREV: Küme Çekme Oluşturma: Yerine koyma** sayfası görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="250e9-297">The **TASK: Cluster Pick Create: Put** page appears.</span></span>

<span data-ttu-id="250e9-298">Bu senaryoda, küme çekme tamamlanmıştır ve kullanıcı, pozisyon 1 ve pozisyon 2'den çekilen maddeleri *STAGE1* hazırlık konumuna koymak üzere yönlendirilir.</span><span class="sxs-lookup"><span data-stu-id="250e9-298">In this scenario, the cluster pick has been completed, and the user is directed to put away the picked items from position 1 and position 2 into staging location *STAGE01*.</span></span>

1. <span data-ttu-id="250e9-299">Sayfadaki bilgileri gözden geçirin.</span><span class="sxs-lookup"><span data-stu-id="250e9-299">Review the information on the page.</span></span> <span data-ttu-id="250e9-300">Bu, toplam *44* tanesinin hazırlık konumuna koyulacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="250e9-300">It shows that a total quantity of *44* will be put to the staging location.</span></span>
1. <span data-ttu-id="250e9-301">**Tamam**'ı (onay işareti simgesi) seçin.</span><span class="sxs-lookup"><span data-stu-id="250e9-301">Select **OK** (check mark symbol).</span></span>

    <span data-ttu-id="250e9-302">Bir "Küme Tamamlandı" iletisi alırsınız.</span><span class="sxs-lookup"><span data-stu-id="250e9-302">You receive a "Cluster Completed" message.</span></span>

<span data-ttu-id="250e9-303">Artık kalan miktarı çekmek için **Satış Malzeme Çekme** menü öğesini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="250e9-303">You can now use the **Sales Picking** menu item to pick the remaining quantity.</span></span> <span data-ttu-id="250e9-304">Daha sonra, maddeleri hazırlama yerleşiminden yükleme noktasına taşımak için **Satış yükleme** menü öğesini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="250e9-304">You can then use the **Sales loading** menu item to move the items from the staging location to the loading dock.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]