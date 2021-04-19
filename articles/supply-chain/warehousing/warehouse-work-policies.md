---
title: İş ilkeleri
description: Bu konuda, iş ilkelerinin nasıl ayarlanacağını açıklanmaktadır.
author: perlynne
ms.date: 07/31/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSWorkPolicy
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-07-31
ms.dyn365.ops.version: Release 10.0.13
ms.openlocfilehash: 39a9ba00763fac220eff16bdd42aa07cc8e35ba4
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/01/2021
ms.locfileid: "5838142"
---
# <a name="work-policies"></a><span data-ttu-id="510ee-103">İş ilkeleri</span><span class="sxs-lookup"><span data-stu-id="510ee-103">Work policies</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="510ee-104">Bu konu, sistemin ve Ambar Yönetimi mobil uygulamasının iş ilkelerini destekleyecek şekilde nasıl ayarlanacağını açıklar.</span><span class="sxs-lookup"><span data-stu-id="510ee-104">This topic explains how to set up the system and the Warehouse Management mobile app so that they support work policies.</span></span> <span data-ttu-id="510ee-105">Bu işlevi, satın alma veya transfer emirleri aldığınızda ya da üretim sürecini tamamladığınızda, yerine koyma işi oluşturmadan stoku hızlı bir şekilde kaydetmek için kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="510ee-105">You can use this functionality to quickly register inventory without creating putaway work when you receive purchase or transfer orders, or when you complete manufacturing processes.</span></span> <span data-ttu-id="510ee-106">Bu konu genel bilgileri sağlar.</span><span class="sxs-lookup"><span data-stu-id="510ee-106">This topic provides general information.</span></span> <span data-ttu-id="510ee-107">Plaka alma ile ilgili ayrıntılı bilgi için bkz. [Ambar Yönetimi mobil uygulaması üzerinden plaka alma](warehousing-mobile-device-app-license-plate-receiving.md).</span><span class="sxs-lookup"><span data-stu-id="510ee-107">For detailed information that is related to license plate receiving, see [License plate receiving via the Warehouse Management mobile app](warehousing-mobile-device-app-license-plate-receiving.md).</span></span>

<span data-ttu-id="510ee-108">İş ilkesi, üretilen bir kalem tamamlandı olarak bildirildiğinde veya Ambar Yönetimi mobil uygulaması kullanılarak mal alındığında ambar işi oluşturulup oluşturulmayacağını denetler.</span><span class="sxs-lookup"><span data-stu-id="510ee-108">A work policy controls whether warehouse work is created when a manufactured item is reported as finished, or when goods are received by using the Warehouse Management mobile app.</span></span> <span data-ttu-id="510ee-109">Her iş ilkesini, uygulandığı koşulları tanımlayarak ayarlayabilirsiniz: iş emri türleri ve süreçleri, stok konumu ve (isteğe bağlı olarak) ürünler.</span><span class="sxs-lookup"><span data-stu-id="510ee-109">You set up each work policy by defining the conditions where it applies: the work order types and processes, the inventory location, and (optionally) the products.</span></span> <span data-ttu-id="510ee-110">Örneğin, A *0001* ürününün satın alma siparişi ambar *24*'te *RECV* konumuna alınmalıdır.</span><span class="sxs-lookup"><span data-stu-id="510ee-110">For example, a purchase order for product *A0001* must be received in location *RECV* in warehouse *24*.</span></span> <span data-ttu-id="510ee-111">Daha sonra, ürün, *RECV* konumunda başka bir işlemde kullanılır.</span><span class="sxs-lookup"><span data-stu-id="510ee-111">Later, the product is consumed in another process at location *RECV*.</span></span> <span data-ttu-id="510ee-112">Bu durumda, bir çalışan *A0001* ürününün *RECV* konumuna alındığını bildirdiğinde yerine koyma işi oluşturmayı önleyecek bir iş ilkesi ayarlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="510ee-112">In this case, you can set up a work policy to prevent putaway work from being created when a worker reports product *A0001* as received in location *RECV*.</span></span>

> [!NOTE]
> - <span data-ttu-id="510ee-113">Bir iş ilkesinin etkin olması için **İş ilkeleri** sayfasının **Stok konumları** hızlı sekmesinde en az bir konum tanımlamanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="510ee-113">For a work policy to be active, you must define at least one location for it on the **Inventory locations** FastTab of the **Work policies** page.</span></span> 
> - <span data-ttu-id="510ee-114">Birden fazla iş ilkesi için aynı konumu belirtemezsiniz.</span><span class="sxs-lookup"><span data-stu-id="510ee-114">You can't specify the same location for multiple work policies.</span></span>
> - <span data-ttu-id="510ee-115">Mobil cihaz menüsü öğelerinin **yazdırma etiketi** seçeneği, iş oluşturulmadıysa plaka etiketi yazdırmayacaktır.</span><span class="sxs-lookup"><span data-stu-id="510ee-115">The **Print label** option for mobile device menu items won't print a license plate label unless work was created.</span></span>

## <a name="activate-the-features-in-your-system"></a><span data-ttu-id="510ee-116">Sisteminizde özellikleri etkinleştirme</span><span class="sxs-lookup"><span data-stu-id="510ee-116">Activate the features in your system</span></span>

<span data-ttu-id="510ee-117">Bu konuda açıklanan tüm işlevleri sisteminizde kullanılabilir hale getirmek için [Özellik yönetimi](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)'nde aşağıdaki iki özelliği etkinleştirin:</span><span class="sxs-lookup"><span data-stu-id="510ee-117">To make all the functionality that is described in this topic available in your system, turn on the following two features in [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md):</span></span>

- <span data-ttu-id="510ee-118">Plaka teslim alma geliştirmeleri</span><span class="sxs-lookup"><span data-stu-id="510ee-118">License plate receiving enhancements</span></span>
- <span data-ttu-id="510ee-119">Gelen iş için iş ilkesi geliştirmeleri</span><span class="sxs-lookup"><span data-stu-id="510ee-119">Work policy enhancements for inbound work</span></span>

## <a name="the-work-policies-page"></a><span data-ttu-id="510ee-120">İş ilkeleri sayfası</span><span class="sxs-lookup"><span data-stu-id="510ee-120">The Work policies page</span></span>

<span data-ttu-id="510ee-121">İş ilkelerini ayarlamak için **Ambar Yönetimi \> Kurulum \> İş \> Çalışma ilkeleri**'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="510ee-121">To set up work policies, go to **Warehouse management \> Setup \> Work \> Work policies**.</span></span> <span data-ttu-id="510ee-122">Sonra, her hızlı sekmede, alanları aşağıdaki alt kısımlarda açıklandığı gibi ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="510ee-122">Then, on each FastTab, set the fields as described in the following subsections.</span></span>

### <a name="the-work-order-types-fasttab"></a><span data-ttu-id="510ee-123">İş emri türleri hızlı sekmesi</span><span class="sxs-lookup"><span data-stu-id="510ee-123">The Work order types FastTab</span></span>

<span data-ttu-id="510ee-124">**İş emri türleri** hızlı sekmesinde, tüm iş emri türlerini ve çalışma ilkesinin geçerli olduğu ilgili iş süreçlerini ekleyin.</span><span class="sxs-lookup"><span data-stu-id="510ee-124">On the **Work order types** FastTab, add all the work order types, and the related work processes, that the work policy applies to.</span></span> <span data-ttu-id="510ee-125">İş ilkeleri için aşağıdaki iş emri türleri ve ilgili iş süreçleri desteklenir.</span><span class="sxs-lookup"><span data-stu-id="510ee-125">The following work order types and related work processes are supported for work policies.</span></span>

| <span data-ttu-id="510ee-126">İş siparişi türü</span><span class="sxs-lookup"><span data-stu-id="510ee-126">Work order type</span></span> | <span data-ttu-id="510ee-127">İş süreci</span><span class="sxs-lookup"><span data-stu-id="510ee-127">Work process</span></span> |
|---|---|
| <span data-ttu-id="510ee-128">Hammadde çekme</span><span class="sxs-lookup"><span data-stu-id="510ee-128">Raw material picking</span></span>| <span data-ttu-id="510ee-129">İlgili tüm süreçler</span><span class="sxs-lookup"><span data-stu-id="510ee-129">All related processes</span></span> |
| <span data-ttu-id="510ee-130">Yerine konan ortak ürün ve yan ürün</span><span class="sxs-lookup"><span data-stu-id="510ee-130">Co-product and by-product put away</span></span> | <span data-ttu-id="510ee-131">İlgili tüm süreçler</span><span class="sxs-lookup"><span data-stu-id="510ee-131">All related processes</span></span> |
| <span data-ttu-id="510ee-132">Memul mal yerine koyma</span><span class="sxs-lookup"><span data-stu-id="510ee-132">Finished goods putaway</span></span> | <span data-ttu-id="510ee-133">İlgili tüm süreçler</span><span class="sxs-lookup"><span data-stu-id="510ee-133">All related processes</span></span> |
| <span data-ttu-id="510ee-134">Transfer alış irsaliyesi</span><span class="sxs-lookup"><span data-stu-id="510ee-134">Transfer receipt</span></span> | <span data-ttu-id="510ee-135">Plaka alma (ve yerine koyma)</span><span class="sxs-lookup"><span data-stu-id="510ee-135">License plate receiving (and putaway)</span></span> |
| <span data-ttu-id="510ee-136">Satın alma siparişleri</span><span class="sxs-lookup"><span data-stu-id="510ee-136">Purchase orders</span></span> | <ul><li><span data-ttu-id="510ee-137">Plaka alma (ve yerine koyma)</span><span class="sxs-lookup"><span data-stu-id="510ee-137">License plate receiving (and putaway)</span></span></li><li><span data-ttu-id="510ee-138">Yük kalemi teslim alma (ve yerine koyma)</span><span class="sxs-lookup"><span data-stu-id="510ee-138">Load item receiving (and putaway)</span></span></li><li><span data-ttu-id="510ee-139">Satın alma siparişi satırı teslim alma (ve yerine koyma)</span><span class="sxs-lookup"><span data-stu-id="510ee-139">Purchase order line receiving (and putaway)</span></span></li><li><span data-ttu-id="510ee-140">Satın alma siparişi kalemini teslim alma (ve yerine koyma)</span><span class="sxs-lookup"><span data-stu-id="510ee-140">Purchase order item receiving (and putaway)</span></span></li></ul> |

<span data-ttu-id="510ee-141">Bir iş ilkesini aynı iş emri türündeki birkaç iş sürecinde geçerli olacak şekilde ayarlamak için kılavuza her çalışma işlemine yönelik ayrı bir satır ekleyin.</span><span class="sxs-lookup"><span data-stu-id="510ee-141">To set up a work policy so that it applies to several work processes of the same work order type, add a separate line for each work process to the grid.</span></span>

<span data-ttu-id="510ee-142">Kılavuzdaki her satır için **İş oluşturma yöntemi** alanını aşağıdaki değerlerden birine ayarlayın:</span><span class="sxs-lookup"><span data-stu-id="510ee-142">For each line in the grid, set the **Work creation method** field to one of the following values:</span></span>

- <span data-ttu-id="510ee-143">**Hiçbir zaman**: İş ilkesi seçili iş emri türü için ambar işinin ve ilgili iş sürecinin oluşturulmasını önler.</span><span class="sxs-lookup"><span data-stu-id="510ee-143">**Never** – The work policy will prevent warehouse work from being created for the selected work order type and related work process.</span></span>
- <span data-ttu-id="510ee-144">**Çapraz sevk**: İş ilkesi, **Çapraz sevk ilkesi adı** alanında seçtiğiniz ilkeyi kullanarak çapraz sevk işi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="510ee-144">**Cross docking** – The work policy will create cross-docking work by using the policy that you select in the **Cross docking policy name** field.</span></span>

### <a name="the-inventory-locations-fasttab"></a><span data-ttu-id="510ee-145">Stok konumları hızlı sekmesi</span><span class="sxs-lookup"><span data-stu-id="510ee-145">The Inventory locations FastTab</span></span>

<span data-ttu-id="510ee-146">**Stok konumları** hızlı sekmesinde, bu iş ilkesinin uygulanacağı tüm konumları ekleyin.</span><span class="sxs-lookup"><span data-stu-id="510ee-146">On the **Inventory locations** FastTab, add all the locations where this work policy should be applied.</span></span> <span data-ttu-id="510ee-147">İş ilkesi ile ilişkilendirilmiş bir konum yoksa iş ilkesi herhangi bir sürece uygulanmaz.</span><span class="sxs-lookup"><span data-stu-id="510ee-147">If no location is associated with a work policy, the work policy won't be applied to any process.</span></span>

<span data-ttu-id="510ee-148">Birden fazla iş ilkesi için aynı konumu belirtemezsiniz.</span><span class="sxs-lookup"><span data-stu-id="510ee-148">You can't specify the same location for multiple work policies.</span></span>

<span data-ttu-id="510ee-149">**Plaka izlemeyi kullan** seçeneği kapalı olduğunda bir konum profiline atanmış ambar konumu kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="510ee-149">You can use a warehouse location that is assigned to a location profile where the **Use license plate tracking** option is turned off.</span></span> <span data-ttu-id="510ee-150">Bu durumda, çalışanlar eldeki stoku doğrudan kaydeder.</span><span class="sxs-lookup"><span data-stu-id="510ee-150">In this case, workers will directly register the on-hand inventory.</span></span>

### <a name="the-products-fasttab"></a><span data-ttu-id="510ee-151">Ürünler hızlı sekmesi</span><span class="sxs-lookup"><span data-stu-id="510ee-151">The Products FastTab</span></span>

<span data-ttu-id="510ee-152">**Ürünler** sekmesinde, ilkenin hangi ürünlere uygulanacağını denetlemek için **Ürün seçimi** alanını ayarlayın:</span><span class="sxs-lookup"><span data-stu-id="510ee-152">On the **Products** tab, set the **Product selection** field to control which products the policy should apply to:</span></span>

- <span data-ttu-id="510ee-153">**Tümü**: İlke tüm ürünler için geçerli olur.</span><span class="sxs-lookup"><span data-stu-id="510ee-153">**All** – The policy should apply to all products.</span></span>
- <span data-ttu-id="510ee-154">**Seçili**: İlke yalnızca kılavuzda listelenen ürünler için geçerli olur.</span><span class="sxs-lookup"><span data-stu-id="510ee-154">**Selected** – The policy should apply only to products that are listed in the grid.</span></span> <span data-ttu-id="510ee-155">Kılavuza ürün eklemek veya kılavuzdan ürün kaldırmak için **Ürünler** hızlı sekmesindeki araç çubuğunu kullanın.</span><span class="sxs-lookup"><span data-stu-id="510ee-155">Use the toolbar on the **Products** FastTab to add products to the grid or remove them from the grid.</span></span>

## <a name="default-and-custom-to-locations"></a><span data-ttu-id="510ee-156">Varsayılan ve özel "hedef" konumlar</span><span class="sxs-lookup"><span data-stu-id="510ee-156">Default and custom "to" locations</span></span>

> [!NOTE]
> <span data-ttu-id="510ee-157">Bu bölümde açıklanan işlevselliğin sisteminizde kullanılabilmesini sağlamak için [Özellik yönetimi](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)'ndeki gelen *Plaka alma geliştirmeleri* ve *Gelen iş için iş ilkesi geliştirmeleri*'ni açmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="510ee-157">To make the functionality that is described in this section available in your system, you must turn on the *License plate receiving enhancements* and *Work policy enhancements for inbound work* features in [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).</span></span>

<span data-ttu-id="510ee-158">Daha önce sistem, yalnızca her ambar için tanımlanan varsayılan konumda almayı destekler.</span><span class="sxs-lookup"><span data-stu-id="510ee-158">Previously, the system supported receiving only at the default location that is defined for each warehouse.</span></span> <span data-ttu-id="510ee-159">Ancak, aşağıdaki iş oluşturma süreçlerini kullanan mobil cihaz menü öğeleri artık **Varsayılan verileri kullan** seçeneğini sağlar.</span><span class="sxs-lookup"><span data-stu-id="510ee-159">However, mobile device menu items that use the following work creation processes now provide the **Use default data** option.</span></span> <span data-ttu-id="510ee-160">Bu seçenek, bir veya daha fazla menü öğesine özel bir "hedef" konum atamanıza olanak tanır.</span><span class="sxs-lookup"><span data-stu-id="510ee-160">This option lets you assign a custom "to" location to one or more menu items.</span></span> <span data-ttu-id="510ee-161">(Bu seçenek bazı menü öğesi türleri için zaten kullanılabilir.)</span><span class="sxs-lookup"><span data-stu-id="510ee-161">(This option was already available for some other types of menu items.)</span></span>

- <span data-ttu-id="510ee-162">Plaka alma (ve yerine koyma)</span><span class="sxs-lookup"><span data-stu-id="510ee-162">License plate receiving (and putaway)</span></span>
- <span data-ttu-id="510ee-163">Yük kalemi teslim alma (ve yerine koyma)</span><span class="sxs-lookup"><span data-stu-id="510ee-163">Load item receiving (and putaway)</span></span>
- <span data-ttu-id="510ee-164">Satın alma siparişi satırı teslim alma (ve yerine koyma)</span><span class="sxs-lookup"><span data-stu-id="510ee-164">Purchase order line receiving (and putaway)</span></span>
- <span data-ttu-id="510ee-165">Satın alma siparişi kalemini teslim alma (ve yerine koyma)</span><span class="sxs-lookup"><span data-stu-id="510ee-165">Purchase order item receiving (and putaway)</span></span>

<span data-ttu-id="510ee-166">Bir menü öğesinin **Hedef konum** ayarı, o menü öğesi kullanılarak işlenen tüm siparişler için ambarın varsayılan alma konumunu geçersiz kılar.</span><span class="sxs-lookup"><span data-stu-id="510ee-166">The **To location** setting for a menu item overrides the default receiving location for the warehouse, for all orders that are processed by using that menu item.</span></span>

<span data-ttu-id="510ee-167">Bir mobil cihaz menü öğesini özel bir konumda almayı destekleyecek şekilde ayarlamak için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="510ee-167">To set up a mobile device menu item to support receiving at a custom location, follow these steps.</span></span>

1. <span data-ttu-id="510ee-168">**Ambar yönetimi \> Kurulum \> Mobil cihaz \> Mobil cihaz menüsü öğeleri**'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="510ee-168">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu items**.</span></span>
1. <span data-ttu-id="510ee-169">Bu bölümün önceki kısımlarında listelenen iş oluşturma süreçlerinden birini kullanan bir menü öğesi seçin veya oluşturun.</span><span class="sxs-lookup"><span data-stu-id="510ee-169">Select or create a menu item that uses one of the work creation processes that are listed earlier in this section.</span></span>
1. <span data-ttu-id="510ee-170">**Genel** hızlı sekmesinde, **Varsayılan verileri kullan** seçeneğini **Evet** olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="510ee-170">On the **General** FastTab, set the **Use default data** option to **Yes**.</span></span>
1. <span data-ttu-id="510ee-171">Eylem Bölmesinde **Varsayılan veriler**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="510ee-171">On the Action Pane, select **Default data**.</span></span>
1. <span data-ttu-id="510ee-172">**Varsayılan veriler** sayfasında, aşağıdaki değerleri ayarlayın:</span><span class="sxs-lookup"><span data-stu-id="510ee-172">On the **Default data** page, set the following values:</span></span>

    - <span data-ttu-id="510ee-173">**Varsayılan veri alanı:** Bu alanı *Hedef konum* olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="510ee-173">**Default data field:** Set this field to *To location*.</span></span>
    - <span data-ttu-id="510ee-174">**Ambar:** Bu menü öğesiyle kullanılacak hedef ambarı seçin.</span><span class="sxs-lookup"><span data-stu-id="510ee-174">**Warehouse:** Select the destination warehouse to use with this menu item.</span></span>
    - <span data-ttu-id="510ee-175">**Konum:** Bu alan, seçili ambar için kullanılabilir olan tüm konum kimliklerini listeler.</span><span class="sxs-lookup"><span data-stu-id="510ee-175">**Location:** This field lists all the location IDs that are available for the selected warehouse.</span></span> <span data-ttu-id="510ee-176">Ancak, bu alanın ayarı aslında herhangi bir etkiye sahip değildir.</span><span class="sxs-lookup"><span data-stu-id="510ee-176">However, the setting of this field doesn't actually have any effect.</span></span> <span data-ttu-id="510ee-177">Bu nedenle boş bırakabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="510ee-177">Therefore, you can leave it blank.</span></span> <span data-ttu-id="510ee-178">Bununla birlikte, **Sabit kodlu değer** alanına girmeniz gereken kimliği onaylamak için listeyi kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="510ee-178">Nevertheless, you can use the list to confirm the ID that you must enter in the **Hardcoded value** field.</span></span>
    - <span data-ttu-id="510ee-179">**Sabit kodlu değer:** Bu menü öğesi için geçerli olan giriş konumunun konum kimliğini girin.</span><span class="sxs-lookup"><span data-stu-id="510ee-179">**Hardcoded value:** Enter the location ID for the receiving location that applies to this menu item.</span></span>

> [!TIP]
> <span data-ttu-id="510ee-180">Bir iş ilkesi, yalnızca tüm alma konumları ilgili iş ilkesi kurulumunda listeleniyorsa uygulanabilir.</span><span class="sxs-lookup"><span data-stu-id="510ee-180">A work policy can be applied only if all the receiving locations are listed in the relevant work policy setup.</span></span> <span data-ttu-id="510ee-181">Bu gereksinim, varsayılan ambar teslim alma konumu veya özel "hedef" konum olup olmadığına bakılmaksızın uygulanır.</span><span class="sxs-lookup"><span data-stu-id="510ee-181">This requirement applies regardless of whether you're using the default warehouse receiving location or a custom "to" location.</span></span>

## <a name="example-scenario-warehouse-receiving"></a><span data-ttu-id="510ee-182">Örnek senaryo: Ambar teslim alma</span><span class="sxs-lookup"><span data-stu-id="510ee-182">Example scenario: Warehouse receiving</span></span>

<span data-ttu-id="510ee-183">*Satınalma sipariş kalemi teslim alma (ve yerine koyma)* süreci tarafından alınan tüm ürünler, *FL-001* konumunda kayıtlı olmalıdır ve bunlar ambar *24*' te kullanılabilir olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="510ee-183">All products that are received by the *Purchase order item receiving (and putaway)* process must be registered in location *FL-001*, and they must be available in warehouse *24*.</span></span> <span data-ttu-id="510ee-184">Ancak, iş oluşturulmamalıdır.</span><span class="sxs-lookup"><span data-stu-id="510ee-184">However, work should not be created.</span></span> <span data-ttu-id="510ee-185">Başka bir süreç (diğer mobil cihaz menü öğelerini kullanan) tarafından teslim alınan ürünler varsayılan ambar teslim alma konumuna (*RECV*) kaydedilmelidir ve her zamanki gibi iş oluşturulması gerekir.</span><span class="sxs-lookup"><span data-stu-id="510ee-185">Products that are received by any other process (that is, by using other mobile device menu items) should be registered at the default warehouse receiving location (*RECV*), and work should be created as usual.</span></span> <span data-ttu-id="510ee-186">(Bu senaryo varsayılan teslim alma kurulumunu göstermez.)</span><span class="sxs-lookup"><span data-stu-id="510ee-186">(This scenario doesn't show the default receiving setup.)</span></span>

<span data-ttu-id="510ee-187">Bu senaryo için aşağıdaki öğeler gereklidir:</span><span class="sxs-lookup"><span data-stu-id="510ee-187">This scenario requires the following elements:</span></span>

- <span data-ttu-id="510ee-188">Tüm ürünler için *FL-001* konumuna *Satın alma sipariş kalemi teslim alma (ve yerine koyma)* süreci iş ilkesi</span><span class="sxs-lookup"><span data-stu-id="510ee-188">A work policy for the *Purchase order item receiving (and putaway)* process in location *FL-001*, for all products</span></span>
- <span data-ttu-id="510ee-189">Varsayılan verileri olan ve **Hedef konum** alanı *FL-001* olarak ayarlanmış bir mobil cihaz menü öğesi</span><span class="sxs-lookup"><span data-stu-id="510ee-189">A mobile device menu item that has default data, and that sets the **To location** field to *FL-001*</span></span>

### <a name="prerequisites"></a><span data-ttu-id="510ee-190">Önkoşullar</span><span class="sxs-lookup"><span data-stu-id="510ee-190">Prerequisites</span></span>

<span data-ttu-id="510ee-191">Bu senaryoda açıklanan işlevselliğin sisteminizde kullanılabilmesini sağlamak için [Özellik yönetimi](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)'ndeki gelen *Plaka alma geliştirmeleri* ve *Gelen iş için iş ilkesi geliştirmeleri*'ni açmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="510ee-191">To make the functionality that is described in this scenario available in your system, you must turn on the *License plate receiving enhancements* and *Work policy enhancements for inbound work* features in [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).</span></span>

<span data-ttu-id="510ee-192">Bu senaryo stamdart demo verilerini kullanır.</span><span class="sxs-lookup"><span data-stu-id="510ee-192">This scenario uses the standard demo data.</span></span> <span data-ttu-id="510ee-193">Bu nedenle, burada sunulan değerleri kullanarak bu senaryoyla çalışmak istiyorsanız demo verilerinin yüklenmiş olduğu bir sistemde çalışmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="510ee-193">Therefore, if you want to work through it by using the values that are provided here, you must work on a system where demo data is installed.</span></span> <span data-ttu-id="510ee-194">Ayrıca, **USMF** hukuk varlığını seçmelisiniz.</span><span class="sxs-lookup"><span data-stu-id="510ee-194">Additionally, you must select the **USMF** legal entity.</span></span>

### <a name="set-up-a-work-policy"></a><span data-ttu-id="510ee-195">İş ilkesi ayarlama</span><span class="sxs-lookup"><span data-stu-id="510ee-195">Set up a work policy</span></span>

1. <span data-ttu-id="510ee-196">**Ambar yönetimi \> Kurulum \> İş \> İş ilkeleri**'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="510ee-196">Go to **Warehouse management \> Setup \> Work \> Work policies**.</span></span>
1. <span data-ttu-id="510ee-197">**Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="510ee-197">Select **New**.</span></span>
1. <span data-ttu-id="510ee-198">**İş ilkesi adı** alanında, *Satın alma kalemi yerine koyma işi yok* girin.</span><span class="sxs-lookup"><span data-stu-id="510ee-198">In the **Work policy name** field, enter *No purchase item putaway work*.</span></span>
1. <span data-ttu-id="510ee-199">**Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="510ee-199">Select **Save**.</span></span>
1. <span data-ttu-id="510ee-200">**İş emri türleri** hızlı sekmesinde, kılavuza satır eklemek için **Ekle**'yi seçin ve sonra yeni satır için aşağıdaki değerleri ayarlayın:</span><span class="sxs-lookup"><span data-stu-id="510ee-200">On the **Work order types** FastTab, select **Add** to add a row to the grid, and then set the following values for the new row:</span></span>

    - <span data-ttu-id="510ee-201">**İş emri türü:** *Satın alma siparişleri*</span><span class="sxs-lookup"><span data-stu-id="510ee-201">**Work order type:** *Purchase orders*</span></span>
    - <span data-ttu-id="510ee-202">**İş süreci:** *Satın alma sipariş kalemi teslim alma (ve yerine koyma)*</span><span class="sxs-lookup"><span data-stu-id="510ee-202">**Work process:** *Purchase order item receiving (and putaway)*</span></span>
    - <span data-ttu-id="510ee-203">**İş oluşturma yöntemi:** *Hiçbir zaman*</span><span class="sxs-lookup"><span data-stu-id="510ee-203">**Work creation method:** *Never*</span></span>
    - <span data-ttu-id="510ee-204">**Çapraz sevk ilkesi adı:** Bu alanı boş bırakın.</span><span class="sxs-lookup"><span data-stu-id="510ee-204">**Cross docking policy name:** Leave this field blank.</span></span>

1. <span data-ttu-id="510ee-205">**Stok konumları** hızlı sekmesinde, kılavuza satır eklemek için **Ekle**'yi seçin ve sonra yeni satır için aşağıdaki değerleri ayarlayın:</span><span class="sxs-lookup"><span data-stu-id="510ee-205">On the **Inventory locations** FastTab, select **Add** to add a row to the grid, and then set the following values for the new row:</span></span>

    - <span data-ttu-id="510ee-206">**Ambar:** *24*</span><span class="sxs-lookup"><span data-stu-id="510ee-206">**Warehouse:** *24*</span></span>
    - <span data-ttu-id="510ee-207">**Konum:** *FL-001*</span><span class="sxs-lookup"><span data-stu-id="510ee-207">**Location:** *FL-001*</span></span>

1. <span data-ttu-id="510ee-208">**Ürünler** hızlı sekmesinde, **Ürün seçimi** alanını *Tümü* olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="510ee-208">On the **Products** FastTab, set the **Product selection** field to *All*.</span></span>
1. <span data-ttu-id="510ee-209">**Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="510ee-209">Select **Save**.</span></span>

### <a name="set-up-a-mobile-device-menu-item-to-change-the-receiving-location"></a><span data-ttu-id="510ee-210">Teslim alma konumunu değiştirmek için bir mobil cihaz menü öğesi ayarlama</span><span class="sxs-lookup"><span data-stu-id="510ee-210">Set up a mobile device menu item to change the receiving location</span></span>

1. <span data-ttu-id="510ee-211">**Ambar yönetimi \> Kurulum \> Mobil cihaz \> Mobil cihaz menüsü öğeleri**'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="510ee-211">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu items**.</span></span>
1. <span data-ttu-id="510ee-212">Sol bölmede, varolan **Satın alma teslimi** menü öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="510ee-212">In the left pane, select the existing **Purchase receive** menu item.</span></span>
1. <span data-ttu-id="510ee-213">**Genel** hızlı sekmesinde, **Varsayılan verileri kullan** seçeneğini *Evet* olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="510ee-213">On the **General** FastTab, set the **Use default data** option to *Yes*.</span></span>
1. <span data-ttu-id="510ee-214">**Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="510ee-214">Select **Save**.</span></span>
1. <span data-ttu-id="510ee-215">Eylem Bölmesinde **Varsayılan veriler**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="510ee-215">On the Action Pane, select **Default data**.</span></span>
1. <span data-ttu-id="510ee-216">**Varsayılan veriler** sayfasında, Eylem Bölmesinde kılavuza satır eklemek için **Yeni**'yi seçin ve sonra yeni satır için aşağıdaki değerleri ayarlayın:</span><span class="sxs-lookup"><span data-stu-id="510ee-216">On the **Default data** page, on the Action Pane, select **New** to add a row to the grid, and then set the following values for the new row:</span></span>

    - <span data-ttu-id="510ee-217">**Varsayılan veri alanı:** *Hedef konum*</span><span class="sxs-lookup"><span data-stu-id="510ee-217">**Default data field:** *To location*</span></span>
    - <span data-ttu-id="510ee-218">**Ambar:** *24*</span><span class="sxs-lookup"><span data-stu-id="510ee-218">**Warehouse:** *24*</span></span>
    - <span data-ttu-id="510ee-219">**Konum:** Bu alanı boş bırakın.</span><span class="sxs-lookup"><span data-stu-id="510ee-219">**Location:** Leave this field blank.</span></span>
    - <span data-ttu-id="510ee-220">**Sabit kodlu değer:** *FL-001*</span><span class="sxs-lookup"><span data-stu-id="510ee-220">**Hardcoded value:** *FL-001*</span></span>

1. <span data-ttu-id="510ee-221">**Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="510ee-221">Select **Save**.</span></span>

### <a name="receive-a-purchase-order-without-creating-work"></a><span data-ttu-id="510ee-222">İş oluşturmadan bir satın alma siparişi teslim alma</span><span class="sxs-lookup"><span data-stu-id="510ee-222">Receive a purchase order without creating work</span></span>

<span data-ttu-id="510ee-223">Bu bölümdeki örnekte, bir satın alma siparişi kaleminin ambar için ayarlanan varsayılan teslim alma konumundan farklı bir konumda iş oluşturulmadan nasıl teslim alınacağı gösterilmiştir.</span><span class="sxs-lookup"><span data-stu-id="510ee-223">The example in this section shows how to receive a purchase order item, but without creating work, at a location that differs from the default receiving location that is set up for the warehouse.</span></span> <span data-ttu-id="510ee-224">Bu örnekte, bu senaryoda daha önce oluşturduğunuz iş ilkesi ve mobil cihaz öğesi kullanılmaktadır.</span><span class="sxs-lookup"><span data-stu-id="510ee-224">This example uses the work policy and mobile device item that you created earlier in this scenario.</span></span>

#### <a name="create-a-purchase-order"></a><span data-ttu-id="510ee-225">Satınalma siparişi oluşturma</span><span class="sxs-lookup"><span data-stu-id="510ee-225">Create a purchase order</span></span>

1. <span data-ttu-id="510ee-226">**Tedarik ve kaynak atama \> Satınalma siparişleri \> Tüm satınalma siparişleri**'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="510ee-226">Go to **Procurement and sourcing \> Purchase orders \> All purchase orders**.</span></span>
1. <span data-ttu-id="510ee-227">**Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="510ee-227">Select **New**.</span></span>
1. <span data-ttu-id="510ee-228">**Satın alma siparişi oluştur** iletişim kutusunda, aşağıdaki değerleri ayarlayın:</span><span class="sxs-lookup"><span data-stu-id="510ee-228">In the **Create purchase order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="510ee-229">**Satıcı hesabı:** *US-101*</span><span class="sxs-lookup"><span data-stu-id="510ee-229">**Vendor account:** *US-101*</span></span>
    - <span data-ttu-id="510ee-230">**Tesis:** *2*</span><span class="sxs-lookup"><span data-stu-id="510ee-230">**Site:** *2*</span></span>
    - <span data-ttu-id="510ee-231">**Ambar:** *24*</span><span class="sxs-lookup"><span data-stu-id="510ee-231">**Warehouse:** *24*</span></span>

1. <span data-ttu-id="510ee-232">İletişim kutusunu kapatmak ve yeni satın alma siparişini açmak için **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="510ee-232">Select **OK** to close the dialog box and open the new purchase order.</span></span>
1. <span data-ttu-id="510ee-233">**Satın alma siparişi satırları** hızlı sekmesinde, boş satır için aşağıdaki değerleri ayarlayın:</span><span class="sxs-lookup"><span data-stu-id="510ee-233">On the **Purchase order lines** FastTab, set the following values for the empty row:</span></span>

    - <span data-ttu-id="510ee-234">**Madde numarası:** *A0001*</span><span class="sxs-lookup"><span data-stu-id="510ee-234">**Item number:** *A0001*</span></span>
    - <span data-ttu-id="510ee-235">**Miktar:** *1*</span><span class="sxs-lookup"><span data-stu-id="510ee-235">**Quantity:** *1*</span></span>

1. <span data-ttu-id="510ee-236">**Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="510ee-236">Select **Save**.</span></span>
1. <span data-ttu-id="510ee-237">Satın alma siparişi numarasını not edin.</span><span class="sxs-lookup"><span data-stu-id="510ee-237">Make a note of the purchase order number.</span></span>

#### <a name="receive-a-purchase-order"></a><span data-ttu-id="510ee-238">Satın alma siparişi teslim alma</span><span class="sxs-lookup"><span data-stu-id="510ee-238">Receive a purchase order</span></span>

1. <span data-ttu-id="510ee-239">Mobil cihazda, kullanıcı kimliği olarak *24* ve parola olarak *1* girerek ambar *24*'te oturum açın.</span><span class="sxs-lookup"><span data-stu-id="510ee-239">On the mobile device, sign in to warehouse *24* by using *24* as the user ID and *1* as the password.</span></span>
1. <span data-ttu-id="510ee-240">**Gelen**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="510ee-240">Select **Inbound**.</span></span>
1. <span data-ttu-id="510ee-241">**Satın alma teslim alma** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="510ee-241">Select **Purchase receive**.</span></span> <span data-ttu-id="510ee-242">**Konum** alanı *FL-001* olarak ayarlanmalıdır.</span><span class="sxs-lookup"><span data-stu-id="510ee-242">The **Location** field should be set to *FL-001*.</span></span>
1. <span data-ttu-id="510ee-243">Önceki yordamda oluşturduğunuz satın alma siparişinin satın alma siparişi numarasını girin.</span><span class="sxs-lookup"><span data-stu-id="510ee-243">Enter the purchase order number for the purchase order that you created in the previous procedure.</span></span>
1. <span data-ttu-id="510ee-244">**Kalem numarası** alanına *A0001* girin.</span><span class="sxs-lookup"><span data-stu-id="510ee-244">In the **Item number** field, enter *A0001*.</span></span>
1. <span data-ttu-id="510ee-245">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="510ee-245">Select **OK**.</span></span>
1. <span data-ttu-id="510ee-246">**Miktar** alanına *1* yazın.</span><span class="sxs-lookup"><span data-stu-id="510ee-246">In the **Quantity** field, enter *1*.</span></span>
1. <span data-ttu-id="510ee-247">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="510ee-247">Select **OK**.</span></span>

<span data-ttu-id="510ee-248">Satın alma siparişi artık teslim alındı, ancak ilişkilendirilmiş iş yok.</span><span class="sxs-lookup"><span data-stu-id="510ee-248">The purchase order is now received, but no work is associated with it.</span></span> <span data-ttu-id="510ee-249">Eldeki stok güncelleştirildi ve *FL-001* konumunda *A0001* kaleminden *1* adet bulunuyor.</span><span class="sxs-lookup"><span data-stu-id="510ee-249">The on-hand inventory has been updated, and a quantity of *1* of item *A0001* is now available at location *FL-001*.</span></span>

## <a name="example-scenario-manufacturing"></a><span data-ttu-id="510ee-250">Örnek senaryo: Üretim</span><span class="sxs-lookup"><span data-stu-id="510ee-250">Example scenario: Manufacturing</span></span>

<span data-ttu-id="510ee-251">Aşağıdaki örnekte, *PRD-001* ve *PRD-002* olmak üzere iki üretim emri bulunmaktadır.</span><span class="sxs-lookup"><span data-stu-id="510ee-251">In the following example, there are two production orders, *PRD-001* and *PRD-002*.</span></span> <span data-ttu-id="510ee-252">Üretim emri *PRD-001*, *SC1* ürününün *001* konumuna tamamlandı olarak bildirildiği *Derleme* adlı bir işleme sahiptir.</span><span class="sxs-lookup"><span data-stu-id="510ee-252">Production order *PRD-001* has an operation that is named *Assembly*, where product *SC1* is being reported as finished to location *001*.</span></span> <span data-ttu-id="510ee-253">Üretim emri *PRD-002*, *Boyama* adlı bir işleme sahiptir ve *001* konumundan *SC* 1 ürününü kullanır.</span><span class="sxs-lookup"><span data-stu-id="510ee-253">Production order *PRD-002* has an operation that is named *Painting* and consumes product *SC1* from location *001*.</span></span> <span data-ttu-id="510ee-254">Üretim emri *PRD-002* de *001* konumundan *RM* 1 hammaddesini kullanır.</span><span class="sxs-lookup"><span data-stu-id="510ee-254">Production order *PRD-002* also consumes raw material *RM1* from location *001*.</span></span> <span data-ttu-id="510ee-255">*RM1* hammaddesi, *BULK-001* ambar konumunda depolanır ve hammadde çekmeye yönelik ambar işi tarafından *001* konumuna çekilir.</span><span class="sxs-lookup"><span data-stu-id="510ee-255">Raw material *RM1* is stored in warehouse location *BULK-001* and will be picked to location *001* by warehouse work for raw material picking.</span></span> <span data-ttu-id="510ee-256">Malzeme çekme işi *PRD-002* üretimi serbest bırakıldığında oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="510ee-256">The picking work is generated when production *PRD-002* is released.</span></span>

<span data-ttu-id="510ee-257">[![Ambar iş ilkeleri](./media/warehouse-work-policies.png)](./media/warehouse-work-policies.png)</span><span class="sxs-lookup"><span data-stu-id="510ee-257">[![Warehouse work policies](./media/warehouse-work-policies.png)](./media/warehouse-work-policies.png)</span></span>

<span data-ttu-id="510ee-258">Bu senaryo için bir ambar işi ilkesi yapılandırmayı planlarken, aşağıdaki hususları göz önünde bulundurmalısınız:</span><span class="sxs-lookup"><span data-stu-id="510ee-258">When you're planning to configure a warehouse work policy for this scenario, you should consider the following points:</span></span>

- <span data-ttu-id="510ee-259">Yerine konan mamul mallar için ambar işi, *SC1* ürününü *PRD-001* üretim emrinden *001* konumuna tamamlandı olarak bildirdiğinizde gerekli değildir.</span><span class="sxs-lookup"><span data-stu-id="510ee-259">Warehouse work for putaway of finished goods isn't required when you report product *SC1* as finished from production order *PRD-001* to location *001*.</span></span> <span data-ttu-id="510ee-260">Bunun nedeni *PRD-002* üretim emrinin *Boyama* işleminin *SC* 1 ürününün aynı konumda kullanmasıdır.</span><span class="sxs-lookup"><span data-stu-id="510ee-260">The reason is that the *Painting* operation for production order *PRD-002* consumes product *SC1* at the same location.</span></span>
- <span data-ttu-id="510ee-261">Hammadde çekme için ambar işi *RM* 1 hammaddesini *BULK-001* ambar konumundan *001* konumuna taşımak için gereklidir.</span><span class="sxs-lookup"><span data-stu-id="510ee-261">Warehouse work for raw material picking is required to move raw material *RM1* from warehouse location *BULK-001* to location *001*.</span></span>

<span data-ttu-id="510ee-262">Bu noktalara göre, ayarlayabileceğiniz iş ilkesine bir örneği aşağıda bulabilirsiniz:</span><span class="sxs-lookup"><span data-stu-id="510ee-262">Here is an example of a work policy that you can set up, based on these considerations:</span></span>

- <span data-ttu-id="510ee-263">**İş ilkesi adı:** *Yerine koyma işi yok*</span><span class="sxs-lookup"><span data-stu-id="510ee-263">**Work policy name:** *No putaway work*</span></span>
- <span data-ttu-id="510ee-264">**İş emri türleri:** *Mamul mal yerine koyma* ve *Ortak ürün ve yan ürün yerine koyma*</span><span class="sxs-lookup"><span data-stu-id="510ee-264">**Work order types:** *Finished goods put away* and *Co-product and by-product put away*</span></span>
- <span data-ttu-id="510ee-265">**Stok konumları:** Ambar *51* ve konum *001*</span><span class="sxs-lookup"><span data-stu-id="510ee-265">**Inventory locations:** Warehouse *51* and location *001*</span></span>
- <span data-ttu-id="510ee-266">**Ürünler:** *SC1*</span><span class="sxs-lookup"><span data-stu-id="510ee-266">**Products:** *SC1*</span></span>

<span data-ttu-id="510ee-267">Aşağıdaki örnek senaryo bu senaryo için ambar iş ilkesini ayarlama konusunda adım adım yönergeler sağlar.</span><span class="sxs-lookup"><span data-stu-id="510ee-267">The following example scenario provides step-by-step instructions for setting up the warehouse work policy for this scenario.</span></span>

## <a name="example-scenario-report-as-finished-to-a-location-that-isnt-license-platecontrolled"></a><span data-ttu-id="510ee-268">Örnek senaryo: Plaka denetimli olmayan bir konuma tamamlandı olarak bildirme</span><span class="sxs-lookup"><span data-stu-id="510ee-268">Example scenario: Report as finished to a location that isn't license plate–controlled</span></span>

<span data-ttu-id="510ee-269">Bu senaryo, bir üretim emrinin plaka denetimli olmayan bir konuma tamamlandı olarak bildirildiği bir örneği göstermektedir.</span><span class="sxs-lookup"><span data-stu-id="510ee-269">This scenario shows an example where a production order is reported as finished to a location that isn't license plate–controlled.</span></span>

<span data-ttu-id="510ee-270">Bu senaryo stamdart demo verilerini kullanır.</span><span class="sxs-lookup"><span data-stu-id="510ee-270">This scenario uses the standard demo data.</span></span> <span data-ttu-id="510ee-271">Bu nedenle, burada sunulan değerleri kullanarak bu senaryoyla çalışmak istiyorsanız demo verilerinin yüklenmiş olduğu bir sistemde çalışmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="510ee-271">Therefore, if you want to work through it by using the values that are provided here, you must work on a system where demo data is installed.</span></span> <span data-ttu-id="510ee-272">Ayrıca, **USMF** hukuk varlığını seçmelisiniz.</span><span class="sxs-lookup"><span data-stu-id="510ee-272">Additionally, you must select the **USMF** legal entity.</span></span>

### <a name="set-up-a-warehouse-work-policy"></a><span data-ttu-id="510ee-273">Ambar iş ilkesi ayarlama</span><span class="sxs-lookup"><span data-stu-id="510ee-273">Set up a warehouse work policy</span></span>

<span data-ttu-id="510ee-274">Ambar işlemi her zaman ambar çalışmasını içermezler.</span><span class="sxs-lookup"><span data-stu-id="510ee-274">Warehouse processes don't always include warehouse work.</span></span> <span data-ttu-id="510ee-275">Bir çalışma ilkesi tanımlayarak, hammadde çekme ve tamamlanmış malların yerine koyması işlerinin oluşturulmasını, çeşitli bir ürün dizisi veya belirtilen konumlar için engelleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="510ee-275">By defining a work policy, you can prevent the creation of work for raw material picking and putaway of finished goods for a set of products at specific locations.</span></span>

1. <span data-ttu-id="510ee-276">**Ambar yönetimi \> Kurulum \> İş \> İş ilkeleri**'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="510ee-276">Go to **Warehouse management \> Setup \> Work \> Work policies**.</span></span>
1. <span data-ttu-id="510ee-277">**Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="510ee-277">Select **New**.</span></span>
1. <span data-ttu-id="510ee-278">**İş ilkesi adı** alanında, *Yerine koyma işi yok* girin.</span><span class="sxs-lookup"><span data-stu-id="510ee-278">In the **Work policy name** field, enter *No putaway work*.</span></span>
1. <span data-ttu-id="510ee-279">Eylem bölmesinde, **Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="510ee-279">On the Action Pane, select **Save**.</span></span>
1. <span data-ttu-id="510ee-280">**İş emri türleri** hızlı sekmesinde, kılavuza satır eklemek için **Ekle**'yi seçin ve sonra yeni satır için aşağıdaki değerleri ayarlayın:</span><span class="sxs-lookup"><span data-stu-id="510ee-280">On the **Work order types** FastTab, select **Add** to add a row to the grid, and then set the following values for the new row:</span></span>

    - <span data-ttu-id="510ee-281">**İş emri türü:** *Mamul malları yerine koyma*</span><span class="sxs-lookup"><span data-stu-id="510ee-281">**Work order type:** *Finished goods put away*</span></span>
    - <span data-ttu-id="510ee-282">**İş süreci:** *Tüm ilgili iş süreçleri*</span><span class="sxs-lookup"><span data-stu-id="510ee-282">**Work process:** *All related work processes*</span></span>
    - <span data-ttu-id="510ee-283">**İş oluşturma yöntemi:** *Hiçbir zaman*</span><span class="sxs-lookup"><span data-stu-id="510ee-283">**Work creation method:** *Never*</span></span>
    - <span data-ttu-id="510ee-284">**Çapraz sevk ilkesi adı:** Bu alanı boş bırakın.</span><span class="sxs-lookup"><span data-stu-id="510ee-284">**Cross docking policy name:** Leave this field blank.</span></span>

1. <span data-ttu-id="510ee-285">Kılavuza ikinci bir satır eklemek için **Ekle**'yi tekrar seçin ve sonra yeni satır için aşağıdaki değerleri ayarlayın:</span><span class="sxs-lookup"><span data-stu-id="510ee-285">Select **Add** again to add a second row to the grid, and then set the following values for the new row:</span></span>

    - <span data-ttu-id="510ee-286">**İş emri türü:** *Ortak ürün ve yan ürün yerine koyma*</span><span class="sxs-lookup"><span data-stu-id="510ee-286">**Work order type:** *Co-product and by-product put away*</span></span>
    - <span data-ttu-id="510ee-287">**İş süreci:** *Tüm ilgili iş süreçleri*</span><span class="sxs-lookup"><span data-stu-id="510ee-287">**Work process:** *All related work processes*</span></span>
    - <span data-ttu-id="510ee-288">**İş oluşturma yöntemi:** *Hiçbir zaman*</span><span class="sxs-lookup"><span data-stu-id="510ee-288">**Work creation method:** *Never*</span></span>
    - <span data-ttu-id="510ee-289">**Çapraz sevk ilkesi adı:** Bu alanı boş bırakın.</span><span class="sxs-lookup"><span data-stu-id="510ee-289">**Cross docking policy name:** Leave this field blank.</span></span>

1. <span data-ttu-id="510ee-290">**Stok konumları** hızlı sekmesinde, kılavuza satır eklemek için **Ekle**'yi seçin ve sonra yeni satır için aşağıdaki değerleri ayarlayın:</span><span class="sxs-lookup"><span data-stu-id="510ee-290">On the **Inventory locations** FastTab, select **Add** to add a row to the grid, and then set the following values for the new row:</span></span>

    - <span data-ttu-id="510ee-291">**Ambar:** *51*</span><span class="sxs-lookup"><span data-stu-id="510ee-291">**Warehouse:** *51*</span></span>
    - <span data-ttu-id="510ee-292">**Konum:** *001*</span><span class="sxs-lookup"><span data-stu-id="510ee-292">**Location:** *001*</span></span>

1. <span data-ttu-id="510ee-293">**Ürünler** hızlı sekmesinde, **Ürün seçimi** alanını *Seçili* olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="510ee-293">On the **Products** FastTab, set the **Product selection** field to *Selected*.</span></span>
1. <span data-ttu-id="510ee-294">**Ürünler** hızlı sekmesinde, kılavuza satır eklemek için **Ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="510ee-294">On the **Products** FastTab, select **Add** to add a row to the grid.</span></span>
1. <span data-ttu-id="510ee-295">Yeni satırda, **Kalem numarası** alanını *L0101* olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="510ee-295">In the new row, set the **Item number** field to *L0101*.</span></span>
1. <span data-ttu-id="510ee-296">Eylem bölmesinde, **Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="510ee-296">On the Action Pane, select **Save**.</span></span>

### <a name="set-up-an-output-location"></a><span data-ttu-id="510ee-297">Bir çıkış konumu ayarlama</span><span class="sxs-lookup"><span data-stu-id="510ee-297">Set up an output location</span></span>

1. <span data-ttu-id="510ee-298">**Kuruluş yönetimi \> Kaynaklar \> Kaynak grupları**'na gidin.</span><span class="sxs-lookup"><span data-stu-id="510ee-298">Go to **Organization administration \> Resources \> Resource groups**.</span></span>
1. <span data-ttu-id="510ee-299">Sol bölmeden **5102** kaynak grubunu seçin.</span><span class="sxs-lookup"><span data-stu-id="510ee-299">In the left pane, select resource group **5102**.</span></span>
1. <span data-ttu-id="510ee-300">**Genel** hızlı sekmesinde, aşağıdaki değerleri ayarlayın:</span><span class="sxs-lookup"><span data-stu-id="510ee-300">On the **General** FastTab, set the following values:</span></span>

    - <span data-ttu-id="510ee-301">**Çıkış ambarı:** *51*</span><span class="sxs-lookup"><span data-stu-id="510ee-301">**Output warehouse:** *51*</span></span>
    - <span data-ttu-id="510ee-302">**Çıkış konumu:** *001*</span><span class="sxs-lookup"><span data-stu-id="510ee-302">**Output location:** *001*</span></span>

1. <span data-ttu-id="510ee-303">Eylem bölmesinde, **Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="510ee-303">On the Action Pane, select **Save**.</span></span>

> [!NOTE]
> <span data-ttu-id="510ee-304">*001* konumu, plaka denetimli bir konum değildir.</span><span class="sxs-lookup"><span data-stu-id="510ee-304">Location *001* isn't a license plate–controlled location.</span></span> <span data-ttu-id="510ee-305">Konum için geçerli bir çalışma ilkesi bulunuyorsa sadece, plaka denetimli olmayan bir çıkış konumu ayarlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="510ee-305">You can set up an output location that isn't license plate–controlled only if an applicable work policy exists for the location.</span></span>

### <a name="create-a-production-order-and-report-it-as-finished"></a><span data-ttu-id="510ee-306">Bir üretim emri oluşturun ve bunu tamamlandı olarak rapor edin</span><span class="sxs-lookup"><span data-stu-id="510ee-306">Create a production order and report it as finished</span></span>

1. <span data-ttu-id="510ee-307">**Üretim denetimi \> Üretim emirleri \> Tüm üretim emirleri**'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="510ee-307">Go to **Production control \> Production orders \> All production orders**.</span></span>
1. <span data-ttu-id="510ee-308">Eylem Bölmesinde **Yeni üretim emri**'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="510ee-308">On the Action Pane, select **New production order**.</span></span>
1. <span data-ttu-id="510ee-309">**Üretim emri oluştur** iletişim kutusunda, **Kalem numarası** alanını *L0101* olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="510ee-309">In the **Create production order** dialog box, set the **Item number** field to *L0101*.</span></span>
1. <span data-ttu-id="510ee-310">Satış siparişi oluşturmak ve iletişim kutusunu kapatmak için **Oluştur**'u seçin.</span><span class="sxs-lookup"><span data-stu-id="510ee-310">Select **Create** to create the order and close the dialog box.</span></span>

    <span data-ttu-id="510ee-311">**Tüm üretim emirleri** sayfasındaki kılavuza yeni bir üretim emri eklenir.</span><span class="sxs-lookup"><span data-stu-id="510ee-311">A new production order is added to the grid on the **All production orders** page.</span></span>

    <span data-ttu-id="510ee-312">Yeni üretim emrini seçili durumda tutun.</span><span class="sxs-lookup"><span data-stu-id="510ee-312">Keep the new production order selected.</span></span>

1. <span data-ttu-id="510ee-313">Eylem Bölmesinde, **Üretim emri** sekmesinde **İşlem** grubunda **Tahmin**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="510ee-313">On the Action Pane, on the **Production order** tab, in the **Process** group, select **Estimate**.</span></span>
1. <span data-ttu-id="510ee-314">**Tahmin** iletişim kutusunda tahmini okuyun ve iletişim kutusunu kapatmak için **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="510ee-314">In the **Estimate** dialog box, read the estimate, and then select **OK** to close the dialog box.</span></span>
1. <span data-ttu-id="510ee-315">Eylem Bölmesinde, **Üretim emri** sekmesinde **İşlem** grubunda **Başlat**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="510ee-315">On the Action Pane, on the **Production order** tab, in the **Process** group, select **Start**.</span></span>
1. <span data-ttu-id="510ee-316">**Başlat** iletişim kutusunda, **Genel** sekmesinde, **Otomatik BOM kullanımı** alanını *Hiçbir zaman* olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="510ee-316">In the **Start** dialog box, on the **General** tab, set the **Automatic BOM consumption** field to *Never*.</span></span>
1. <span data-ttu-id="510ee-317">Ayarınızı kaydedip iletişim kutusunu kapatmak için **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="510ee-317">Select **OK** to save your setting and close the dialog box.</span></span>
1. <span data-ttu-id="510ee-318">Eylem Bölmesinde, **Üretim emri** sekmesinde **İşlem** grubunda **Tamamlandı olarak bildir**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="510ee-318">On the Action Pane, on the **Production order** tab, in the **Process** group, select **Report as finished**.</span></span>
1. <span data-ttu-id="510ee-319">**Tamamlandı olarak bildir** iletişim kutusunda, **Genel** sekmesinde **Hatayı kabul et** seçeneğini *Evet* olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="510ee-319">In the **Report as finished** dialog box, on the **General** tab, set the **Accept error** option to *Yes*.</span></span>
1. <span data-ttu-id="510ee-320">Ayarınızı kaydedip iletişim kutusunu kapatmak için **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="510ee-320">Select **OK** to save your setting and close the dialog box.</span></span>
1. <span data-ttu-id="510ee-321">Eylem Bölmesinde **Ambar** sekmesindeki **Genel** grubunda **İş ayrıntıları**'nı seçin.</span><span class="sxs-lookup"><span data-stu-id="510ee-321">On the Action Pane, on the **Warehouse** tab, in the **General** group, select **Work details**.</span></span>

<span data-ttu-id="510ee-322">Üretim emri, tamamlandı olarak bildirildiğinde, yerine koyma için hiçbir iş üretilmez.</span><span class="sxs-lookup"><span data-stu-id="510ee-322">When the production order is reported as finished, no work is generated for putaway.</span></span> <span data-ttu-id="510ee-323">Bu davramış, Ürün *L0101*, konum *001*'e tamamlandı olarak bildirildiğinde işin oluşturulmasının engellenmesi için tanımlanan bir iş ilkesi bulunmasından kaynaklanır.</span><span class="sxs-lookup"><span data-stu-id="510ee-323">This behavior occurs because a work policy is defined that prevents work from being generated when product *L0101* is reported as finished to location *001*.</span></span>

## <a name="more-information"></a><span data-ttu-id="510ee-324">Daha fazla bilgi</span><span class="sxs-lookup"><span data-stu-id="510ee-324">More information</span></span>

<span data-ttu-id="510ee-325">Mobil cihaz menü öğeleri hakkında daha fazla bilgi için bkz. [Ambar işi için mobil cihazları ayarlama](configure-mobile-devices-warehouse.md).</span><span class="sxs-lookup"><span data-stu-id="510ee-325">For more information about mobile device menu items, see [Set up mobile devices for warehouse work](configure-mobile-devices-warehouse.md).</span></span>

<span data-ttu-id="510ee-326">Plaka alma ve iş ilkeleri ile ilgili ayrıntılı bilgi için bkz. [Ambar Yönetimi mobil uygulaması üzerinden plaka alma](warehousing-mobile-device-app-license-plate-receiving.md).</span><span class="sxs-lookup"><span data-stu-id="510ee-326">For more information about license plate receiving and work policies, see [License plate receiving via the Warehouse Management mobile app](warehousing-mobile-device-app-license-plate-receiving.md).</span></span>

<span data-ttu-id="510ee-327">Giriş yük yönetimi hakkında daha fazla bilgi için bkz. [Satınalma siparişleri için gelen yüklerin ambarda işlenmesi.](inbound-load-handling.md)</span><span class="sxs-lookup"><span data-stu-id="510ee-327">For more information about inbound load management, see [Warehouse handling of inbound loads for purchase orders](inbound-load-handling.md).</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]