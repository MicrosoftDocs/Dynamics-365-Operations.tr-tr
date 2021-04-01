---
title: İşteki iş havuzunu değiştir
description: Bu konu, varolan işin iş havuzunu değiştirmek için iş öğelerinin İş havuzunu değiştir düğmesini nasıl kullanabileceğinizi açıklamaktadır.
author: mirzaab
manager: tfehr
ms.date: 07/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSWorkPool,WHSWorkTemplateTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: global
ms.author: mirzaab
ms.search.validFrom: 2020-07-16
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 61b988cf2501812e940f726e02d8fc1bcee2c035
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5233067"
---
# <a name="change-work-pool-on-work"></a><span data-ttu-id="e615e-103">İşteki iş havuzunu değiştir</span><span class="sxs-lookup"><span data-stu-id="e615e-103">Change work pool on work</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e615e-104">İş havuzlarını, işi gruplar halinde düzenlemek için kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="e615e-104">You can use work pools to organize work into groups.</span></span> <span data-ttu-id="e615e-105">Örneğin, belirli bir ambar konumundaki gerçekleşen işi sınıflandırmak için bir iş havuzu oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="e615e-105">For example, you can create a work pool to classify work that occurs in a specific warehouse location.</span></span>

<span data-ttu-id="e615e-106">*İşte iş havuzunu değiştir* özelliği iş öğeleri için Eylem Bölmesine bir **İş havuzunu değiştir** düğmesi ekler.</span><span class="sxs-lookup"><span data-stu-id="e615e-106">The *Change work pool on work* feature adds a **Change work pool** button to the Action Pane for work items.</span></span> <span data-ttu-id="e615e-107">Bu şekilde, ambar yöneticileri mevcut işin iş havuzunu kolayca değiştirebilir.</span><span class="sxs-lookup"><span data-stu-id="e615e-107">Therefore, warehouse managers can easily change the work pool of existing work.</span></span> <span data-ttu-id="e615e-108">Bu özellik, yöneticilerin ambar atölyesindeki değişikliklere hızla tepki vermesine olanak tanır ve değişen durumlara uyum yeteneği ve işi başka bir iş havuzuna aktarma gereksinimini geliştirmeye yardımcı olur.</span><span class="sxs-lookup"><span data-stu-id="e615e-108">This feature lets managers react quickly to changes on the warehouse shop floor, and it helps improve their ability to adapt to changing situations and the need to transfer work to another work pool.</span></span>

## <a name="turn-on-the-change-work-pool-on-work-feature"></a><span data-ttu-id="e615e-109">İşte iş havuzunu değiştir özelliğini açma</span><span class="sxs-lookup"><span data-stu-id="e615e-109">Turn on the Change work pool on work feature</span></span>

<span data-ttu-id="e615e-110">Bu özelliği ayarlamaya veya kullanmaya başlamadan önce, sisteminizde kullanılabilir olduğundan emin olmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="e615e-110">Before you begin to set up or use this feature, you must make sure that it's available in your system.</span></span> <span data-ttu-id="e615e-111">Yöneticiler özellik durumunu denetlemek ve gerekirse etkinleştirmek için [özellik yönetimi](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) ayarlarını kullanabilir.</span><span class="sxs-lookup"><span data-stu-id="e615e-111">Admins can use the [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) settings to check the status of the feature and turn it on if it's required.</span></span> <span data-ttu-id="e615e-112">**Özellik yönetimi** çalışma alanındabu özellik aşağıdaki şekilde listelenir:</span><span class="sxs-lookup"><span data-stu-id="e615e-112">In the **Feature management** workspace, the feature is listed in the following way:</span></span>

- <span data-ttu-id="e615e-113">**Modül:** *Ambar yönetimi*</span><span class="sxs-lookup"><span data-stu-id="e615e-113">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="e615e-114">**Değişiklik adı:** *İşte iş havuzunu değiştir*</span><span class="sxs-lookup"><span data-stu-id="e615e-114">**Feature name:** *Change work pool on work*</span></span>

## <a name="set-up-the-change-work-pool-on-work-feature"></a><span data-ttu-id="e615e-115">İşte iş havuzunu değiştir özelliğini ayarlama</span><span class="sxs-lookup"><span data-stu-id="e615e-115">Set up the Change work pool on work feature</span></span>

<span data-ttu-id="e615e-116">Bu özelliği kullanmak için ayarlanmış iş havuzlarınız olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="e615e-116">To use this feature, you must have some work pools set up.</span></span> <span data-ttu-id="e615e-117">Ayrıca iş şablonlarınızı otomatik olarak bir havuz atayacak şekilde ayarlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="e615e-117">You might also set up your work templates so that they automatically assign a pool.</span></span> <span data-ttu-id="e615e-118">Bu konunun ilerleyen kısımlarında sağlanan örnek senaryo aracılığıyla çalışmak istiyorsanız, sisteminizi bu bölümde anlatıldığı şekilde ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="e615e-118">If you want to work through the example scenario that is provided later in this topic, set up your system as described in this section.</span></span>

### <a name="set-up-work-pools"></a><span data-ttu-id="e615e-119">İş havuzlarını ayarlama</span><span class="sxs-lookup"><span data-stu-id="e615e-119">Set up work pools</span></span>

<span data-ttu-id="e615e-120">İş havuzları, iş öğelerini türlerine göre düzenlemenizi sağlar.</span><span class="sxs-lookup"><span data-stu-id="e615e-120">Work pools let you organize work items by type.</span></span> <span data-ttu-id="e615e-121">*İşte iş havuzunu değiştir* özelliğini kullanmak için en az iki iş havuzunuz olması gerekir.</span><span class="sxs-lookup"><span data-stu-id="e615e-121">To work with the *Change work pool on work* feature, you must have at least two work pools available.</span></span> <span data-ttu-id="e615e-122">İş havuzlarını görüntülemek ve eklemek için şu adımları izleyin:</span><span class="sxs-lookup"><span data-stu-id="e615e-122">To view and add work pools, follow these steps.</span></span>

1. <span data-ttu-id="e615e-123">**Ambar yönetimi \> Kurulum \> İş \> İş öğeleri** seçeneğine gidin.</span><span class="sxs-lookup"><span data-stu-id="e615e-123">Go to **Warehouse management \> Setup \> Work \> Work pools**.</span></span>
1. <span data-ttu-id="e615e-124">**USMF** şirketinden demo verilerle çalışıyorsanız ve bu konunun ilerleyen kısımlarında örnek senaryo üzerinden çalışacaksanız, aşağıdaki ayarlara sahip iki iş havuzu ekleyin:</span><span class="sxs-lookup"><span data-stu-id="e615e-124">If you're working with demo data from the **USMF** company and will work through the example scenario later in this topic, add two work pools that have the following settings:</span></span>

    - <span data-ttu-id="e615e-125">İş havuzu 1:</span><span class="sxs-lookup"><span data-stu-id="e615e-125">Work pool 1:</span></span>

        - <span data-ttu-id="e615e-126">**İş havuzu kimliği:** *Webshop*</span><span class="sxs-lookup"><span data-stu-id="e615e-126">**Work pool ID:** *Webshop*</span></span>
        - <span data-ttu-id="e615e-127">**Açıklama:** *Web Mağazası*</span><span class="sxs-lookup"><span data-stu-id="e615e-127">**Description:** *Web Shop*</span></span>

    - <span data-ttu-id="e615e-128">İş havuzu 2:</span><span class="sxs-lookup"><span data-stu-id="e615e-128">Work pool 2:</span></span>

        - <span data-ttu-id="e615e-129">**İş havuzu kimliği:** *CallCenter*</span><span class="sxs-lookup"><span data-stu-id="e615e-129">**Work pool ID:** *CallCenter*</span></span>
        - <span data-ttu-id="e615e-130">**Açıklama:** *Çağrı Merkezi*</span><span class="sxs-lookup"><span data-stu-id="e615e-130">**Description:** *Call Center*</span></span>

1. <span data-ttu-id="e615e-131">Eylem bölmesinde, **Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="e615e-131">On the Action Pane, select **Save**.</span></span>

### <a name="set-up-work-templates"></a><span data-ttu-id="e615e-132">İş şablonlarını ayarla</span><span class="sxs-lookup"><span data-stu-id="e615e-132">Set up work templates</span></span>

<span data-ttu-id="e615e-133">Her iş şablonunuz için, istediğiniz şekilde varsayılan bir iş havuzu ayarlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="e615e-133">For each of your work templates, you can set a default work pool, as you require.</span></span> <span data-ttu-id="e615e-134">Her ilgili şablon için **İş havuzu kimliği** sütununa bir iş havuzu atarsınız.</span><span class="sxs-lookup"><span data-stu-id="e615e-134">For each relevant template, you assign a work pool in the **Work pool ID** column.</span></span> <span data-ttu-id="e615e-135">Bu durumda, belirli bir şablon kullanılarak oluşturulan tüm iş öğeleri atanan iş havuzunu otomatik olarak devralır.</span><span class="sxs-lookup"><span data-stu-id="e615e-135">In this case, all work items that are generated by using a given template automatically inherit the assigned work pool.</span></span> <span data-ttu-id="e615e-136">**USMF** şirketinden demo verilerle çalışıyorsanız ve bu konunun ilerleyen kısımlarında örnek senaryo üzerinden çalışacaksanız aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="e615e-136">If you're working with the demo data from the **USMF** company and will work through the example scenario later in this topic, follow these steps.</span></span>

1. <span data-ttu-id="e615e-137">**Ambar yönetimi \> Kurulum \> İş \> İş şablonları**'na gidin.</span><span class="sxs-lookup"><span data-stu-id="e615e-137">Go to **Warehouse management \> Setup \> Work \> Work templates**.</span></span>
1. <span data-ttu-id="e615e-138">Eylem Bölmesinde, sayfayı düzenleme moduna geçirmek için **Düzenle** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="e615e-138">On the Action Pane, select **Edit** to put the page into editing mode.</span></span>
1. <span data-ttu-id="e615e-139">Aşağıdaki değerleri ayarlayarak şablonu düzenleyin:</span><span class="sxs-lookup"><span data-stu-id="e615e-139">Edit the template by setting the following values:</span></span>

    - <span data-ttu-id="e615e-140">**İş şablonu:** *62 Paketleme için çek*</span><span class="sxs-lookup"><span data-stu-id="e615e-140">**Work template:** *62 Pick to pack*</span></span>
    - <span data-ttu-id="e615e-141">**İş havuzu kimliği:** *Webshop*</span><span class="sxs-lookup"><span data-stu-id="e615e-141">**Work pool ID:** *Webshop*</span></span>

1. <span data-ttu-id="e615e-142">**Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="e615e-142">Select **Save**.</span></span>

## <a name="example-scenario"></a><span data-ttu-id="e615e-143">Örnek senaryo</span><span class="sxs-lookup"><span data-stu-id="e615e-143">Example scenario</span></span>

<span data-ttu-id="e615e-144">Bu senaryo, çalışma havuzunu değiştirerek varolan bir iş öğesinin işlem akışının nasıl değiştirileceğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="e615e-144">This scenario shows how to change the stream of processing for an existing work item by changing its work pool.</span></span> <span data-ttu-id="e615e-145">**USMF** şirketinden demo veriler ve bu konunun önceki bölümlerinde önerilen ayarlar kullanılır.</span><span class="sxs-lookup"><span data-stu-id="e615e-145">It uses demo data from the **USMF** company and the settings that were suggested earlier in this topic.</span></span>

### <a name="create-a-sales-order-and-release-it-to-the-warehouse"></a><span data-ttu-id="e615e-146">Satış siparişi oluşturma ve ambara serbest bırakma</span><span class="sxs-lookup"><span data-stu-id="e615e-146">Create a sales order and release it to the warehouse</span></span>

1. <span data-ttu-id="e615e-147">Ambar *62*'de *A0001* ve *A0002* öğeleri için yeterli eldeki stok olduğunu doğrulayın.</span><span class="sxs-lookup"><span data-stu-id="e615e-147">Confirm that there is enough on-hand inventory for items *A0001* and *A0002* in warehouse *62*.</span></span> <span data-ttu-id="e615e-148">**Stok yönetimi \> Sorgular ve raporlar \>Eldeki stok listesi**'ne gidin ve filtreleri aşağıda gösterildiği gibi düzenleyin:</span><span class="sxs-lookup"><span data-stu-id="e615e-148">Go to **Inventory management \> Inquiries and reports \> On-hand list**, and edit the filters as shown here:</span></span>

    - <span data-ttu-id="e615e-149">**Ambar** değeri *62* ile başlar.</span><span class="sxs-lookup"><span data-stu-id="e615e-149">The **Warehouse** value begins with *62*.</span></span>
    - <span data-ttu-id="e615e-150">**Madde numarası** değeri *A001* veya *A002*'dir.</span><span class="sxs-lookup"><span data-stu-id="e615e-150">The **Item number** value is either *A001* or *A002*.</span></span>

    <span data-ttu-id="e615e-151">Demo verilerinde miktar olarak her birinden 10 birim bulunmalıdır.</span><span class="sxs-lookup"><span data-stu-id="e615e-151">Demo data should have a quantity of 10 each.</span></span>

    <span data-ttu-id="e615e-152">Daha sonra, bir satış siparişi oluşturmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="e615e-152">Next, you must create a sales order.</span></span>

1. <span data-ttu-id="e615e-153">**Satış ve pazarlama \> Satış siparişleri \> Tüm satış siparişleri**'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="e615e-153">Go to **Sales and marketing \> Sales orders \> All sales orders**.</span></span>
1. <span data-ttu-id="e615e-154">Eylem Bölmesinde, **Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="e615e-154">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="e615e-155">**Satış siparişi oluştur** iletişim kutusunda, aşağıdaki değerleri ayarlayın:</span><span class="sxs-lookup"><span data-stu-id="e615e-155">In the **Create sales order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="e615e-156">**Müşteri hesabı:** *US-007*</span><span class="sxs-lookup"><span data-stu-id="e615e-156">**Customer account:** *US-007*</span></span>
    - <span data-ttu-id="e615e-157">**Ambar:** *62*</span><span class="sxs-lookup"><span data-stu-id="e615e-157">**Warehouse:** *62*</span></span>

1. <span data-ttu-id="e615e-158">Satış siparişi oluşturmak ve iletişim kutusunu kapatmak için **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="e615e-158">Select **OK** to create the sales order and close the dialog box.</span></span>
1. <span data-ttu-id="e615e-159">Yeni satış siparişi açılır.</span><span class="sxs-lookup"><span data-stu-id="e615e-159">The new sales order is opened.</span></span> <span data-ttu-id="e615e-160">**Satış siparişi satırları** hızlı sekmesi 'ndeki kılavuza yeni, boş bir satır dahil etmelidir.</span><span class="sxs-lookup"><span data-stu-id="e615e-160">It should include a new, empty line in the grid on the **Sales order lines** FastTab.</span></span> <span data-ttu-id="e615e-161">Bu satır için aşağıdaki değerleri ayarlayın:</span><span class="sxs-lookup"><span data-stu-id="e615e-161">On this line, set the following values:</span></span>

    - <span data-ttu-id="e615e-162">**Madde numarası:** *A0001*</span><span class="sxs-lookup"><span data-stu-id="e615e-162">**Item number:** *A0001*</span></span>
    - <span data-ttu-id="e615e-163">**Miktar:** *2*</span><span class="sxs-lookup"><span data-stu-id="e615e-163">**Quantity:** *2*</span></span>

1. <span data-ttu-id="e615e-164">Kılavuzun üzerindeki **stok** menüsünde **rezervasyon**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="e615e-164">On the **Inventory** menu above the grid, select **Reservation**.</span></span>
1. <span data-ttu-id="e615e-165">**Rezervasyon** sayfasında, Eylem Bölmesi'nde stok rezerve etmek için **Lotu rezerve et**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="e615e-165">On the **Reservation** page, on the Action Pane, select **Reserve lot** to reserve the inventory.</span></span>
1. <span data-ttu-id="e615e-166">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="e615e-166">Close the page.</span></span>
1. <span data-ttu-id="e615e-167">**Satış siparişi satırları** hızlı sekmesinde, satış siparişinize başka bir satır eklemek için **Satır ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="e615e-167">On the **Sales order lines** FastTab, select **Add line** to add another line to your sales order.</span></span> <span data-ttu-id="e615e-168">Bu satır için aşağıdaki değerleri ayarlayın:</span><span class="sxs-lookup"><span data-stu-id="e615e-168">On this line, set the following values:</span></span>

    - <span data-ttu-id="e615e-169">**Madde numarası:** *A0002*</span><span class="sxs-lookup"><span data-stu-id="e615e-169">**Item number:** *A0002*</span></span>
    - <span data-ttu-id="e615e-170">**Miktar:** *2*</span><span class="sxs-lookup"><span data-stu-id="e615e-170">**Quantity:** *2*</span></span>

1. <span data-ttu-id="e615e-171">Kılavuzun üzerindeki **stok** menüsünde **rezervasyon**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="e615e-171">On the **Inventory** menu above the grid, select **Reservation**.</span></span>
1. <span data-ttu-id="e615e-172">**Rezervasyon** sayfasında, Eylem Bölmesi'nde stok rezerve etmek için **Lotu rezerve et**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="e615e-172">On the **Reservation** page, on the Action Pane, select **Reserve lot** to reserve the inventory.</span></span>
1. <span data-ttu-id="e615e-173">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="e615e-173">Close the page.</span></span>
1. <span data-ttu-id="e615e-174">Eylem bölmesinde, **Ambar** sekmesinde **Ambara serbest bırak**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="e615e-174">On the Action Pane, on the **Warehouse** tab, select **Release to warehouse**.</span></span>
1. <span data-ttu-id="e615e-175">Serbest bırakma işleminden oluşturulan dalga kimliğini ve sevkiyat kimliklerini gösteren bilgi iletileri alırsınız.</span><span class="sxs-lookup"><span data-stu-id="e615e-175">You receive informational messages that show the wave ID and shipment ID that were created from the release.</span></span> <span data-ttu-id="e615e-176">Dalga kodunu not edin.</span><span class="sxs-lookup"><span data-stu-id="e615e-176">Make a note of the wave ID.</span></span>

### <a name="review-the-outbound-wave"></a><span data-ttu-id="e615e-177">Giden dalgayı gözden geçirme</span><span class="sxs-lookup"><span data-stu-id="e615e-177">Review the outbound wave</span></span>

1. <span data-ttu-id="e615e-178">**Ambar yönetimi \> Giden dalgalar \> Sevkiyat dalgaları \> Tüm dalgalar**'a gidin.</span><span class="sxs-lookup"><span data-stu-id="e615e-178">Go to **Warehouse management \> Outbound waves \> Shipment waves \> All waves**.</span></span>
1. <span data-ttu-id="e615e-179">Kılavuzda, satış siparişinin serbest bırakma işleminden oluşturulan dalga kodunu arayın.</span><span class="sxs-lookup"><span data-stu-id="e615e-179">In the grid, search for the wave ID that was created from the release of the sales order.</span></span>
1. <span data-ttu-id="e615e-180">Ayrıntıları görüntülemek için dalga kodunu seçin.</span><span class="sxs-lookup"><span data-stu-id="e615e-180">Select the wave ID to view the details.</span></span>
1. <span data-ttu-id="e615e-181">**Dalga satırları** hızlı sekmesinde, satış siparişi için bir sevkiyat kodu gösterildiğinden emin olun.</span><span class="sxs-lookup"><span data-stu-id="e615e-181">On the **Wave lines** FastTab, make sure that a shipment ID is shown for the sales order.</span></span>

    > [!TIP]
    > <span data-ttu-id="e615e-182">**Ambara serbest bırakıldığında dalgayı işle** seçeneğinin sevkiyat dalga şablonu için *Hayır* olarak ayarlanmış olması durumunda , işi oluşturmak için Eylem Bölmesindeki **Dalga** sekmesinden **İşlem**'i seçerek işlemi el ile oluşturmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="e615e-182">If the **Process wave at release to warehouse** option is set to *No* in the setup for the shipping wave template, you must manually process the wave by selecting **Process** from the **Wave** tab on the Action Pane to create work.</span></span>

1. <span data-ttu-id="e615e-183">Dalganın işlenmiş olduğundan emin olun.</span><span class="sxs-lookup"><span data-stu-id="e615e-183">Make sure that the wave has been processed.</span></span> <span data-ttu-id="e615e-184">Bu işlem gerekli işi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="e615e-184">This processing creates the required work.</span></span>

### <a name="view-work-details-and-change-the-work-pool"></a><span data-ttu-id="e615e-185">İş ayrıntılarını görüntüleme ve iş havuzunu değiştirme</span><span class="sxs-lookup"><span data-stu-id="e615e-185">View work details and change the work pool</span></span>

<span data-ttu-id="e615e-186">Oluşturulan işi görüntülemek ve iş havuzunu yönetmek için **İş ayrıntıları** sayfasını kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="e615e-186">You can use the **Work details** page to view the work that was created and to manage the work pool.</span></span>

1. <span data-ttu-id="e615e-187">**Ambar yönetimi \> İş \> İş ayrıntıları**'na gidin.</span><span class="sxs-lookup"><span data-stu-id="e615e-187">Go to **Warehouse management \> Work \> Work details**.</span></span>
1. <span data-ttu-id="e615e-188">Yeni oluşturulan işe ilişkin satırı seçin.</span><span class="sxs-lookup"><span data-stu-id="e615e-188">Select the row for the work that was just created.</span></span> <span data-ttu-id="e615e-189">**Sipariş numarası** sütunu satış siparişi numarasını gösterir.</span><span class="sxs-lookup"><span data-stu-id="e615e-189">The **Order number** column will show the sales order number.</span></span>

    <span data-ttu-id="e615e-190">**İş havuzu kimliği** alanı, iş şablonunda ayarlanmış olan iş havuzu kimliğine ayarlanır.</span><span class="sxs-lookup"><span data-stu-id="e615e-190">The **Work pool ID** field will be set to the work pool ID that was set up in the work template.</span></span>

    > [!TIP]
    > <span data-ttu-id="e615e-191">**İş havuzu kimliği** alanını göremiyorsanız, sütunu kılavuza ekleyin ve sonra sayfayı yenileyin.</span><span class="sxs-lookup"><span data-stu-id="e615e-191">If you don't see the **Work pool ID** field, add the column to the grid, and then refresh the page.</span></span>

1. <span data-ttu-id="e615e-192">İş koduyla ilişkilendirilmiş çalışma havuzunu değiştirmek için, Eylem Bölmesindeki **İş** sekmesinde **İş havuzu kodunu değiştir**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="e615e-192">To change the work pool that is associated with the work ID, on the Action Pane, on the **Work** tab, select **Change Work pool ID**.</span></span>
1. <span data-ttu-id="e615e-193">**İş havuzunu değiştir** iletişim kutusunda, **Parametreler** hızlı sekmesindeki **İş havuzu kimliği** alanında *CallCenter*'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="e615e-193">In the **Change work pool** dialog box, on the **Parameters** FastTab, in the **Work pool ID** field, select *CallCenter*.</span></span>
1. <span data-ttu-id="e615e-194">Değişiklerinizi uygulamak için **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="e615e-194">Select **OK** to apply your change.</span></span>
1. <span data-ttu-id="e615e-195">**İş havuzu kimliği** alanı değerinin şimdi *CallCenter* olarak değiştirilmiş olduğuna dikkat edin.</span><span class="sxs-lookup"><span data-stu-id="e615e-195">Notice that the value of the **Work pool ID** field has now been changed to *CallCenter*.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="e615e-196">**İş havuzunu değiştir** iletişim kutusu göründüğünde, **İş havuzu kimliği** alanı varsayılan olarak boş olabilir.</span><span class="sxs-lookup"><span data-stu-id="e615e-196">When the **Change work pool** dialog box appears, the **Work pool ID** field might be blank by default.</span></span> <span data-ttu-id="e615e-197">Değişiklikleri uygulamak için **Tamam**'ı seçtiğinizde alan boşsa, iş havuzunu tamamen işten kaldırırsınız.</span><span class="sxs-lookup"><span data-stu-id="e615e-197">If the field is blank when you select **OK** to apply changes, you will remove the work pool completely from the work.</span></span>
>
> <span data-ttu-id="e615e-198">İş havuzlarını değiştirmeye ek olarak, bu yordamı iş havuzu olmayan bir iş öğesine iş havuzu eklemek veya iş havuzu olan bir iş öğesinden iş havuzunu kaldırmak için de kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="e615e-198">In addition to switching work pools, you can use this procedure to add a work pool to any work item that doesn't have one, or to remove a work pool from any work item that does have one.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]