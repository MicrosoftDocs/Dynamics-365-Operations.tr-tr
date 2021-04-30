---
title: Planlanmış çapraz sevk
description: Bu konuda, bir sipariş için gereken stok miktarının kabulden veya oluşturma aşamasından doğru çıkış noktasına veya hazırlama alanına kadar yönlendirildiği, ileri düzeyde planlanmış çapraz sevk açıklanmaktadır. Gelen kaynaktan kalan tüm stok, normal yerine koyma işlemiyle doğru depolama yerleşimine yönlendirilir.
author: Mirzaab
ms.date: 07/01/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSCrossDockingTemplate, WHSLoadPostMethod, WHSWorkClass, WHSWorkTemplateTable, WHSLocDirTable, WHSPlannedCrossDocking
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-01
ms.dyn365.ops.version: Release 10.0.7
ms.openlocfilehash: 11e044e04e05c68af676bf97e6085e9975da5c1d
ms.sourcegitcommit: bef7bd2aac00d7eb837fd275d383b7a5c3f1c1ee
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/19/2021
ms.locfileid: "5911260"
---
# <a name="planned-cross-docking"></a><span data-ttu-id="d79ba-104">Planlanmış çapraz sevk</span><span class="sxs-lookup"><span data-stu-id="d79ba-104">Planned cross-docking</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d79ba-105">Bu konuda, ileri düzeyde planlı çapraz sevk açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="d79ba-105">This topic describes advanced planned cross-docking.</span></span> <span data-ttu-id="d79ba-106">Çapraz sevk, bir sipariş için gereken stok miktarının kabulden veya oluşturma aşamasından doğru çıkış noktasına veya hazırlama alanına kadar yönlendirildiği bir ambar sürecidir.</span><span class="sxs-lookup"><span data-stu-id="d79ba-106">Cross-docking is a warehouse process where the inventory quantity that is required for an order is directed straight from receipt or creation to the correct outbound dock or staging area.</span></span> <span data-ttu-id="d79ba-107">Gelen kaynaktan kalan tüm stok, normal yerine koyma işlemiyle doğru depolama yerleşimine yönlendirilir.</span><span class="sxs-lookup"><span data-stu-id="d79ba-107">All remaining inventory from the inbound source is directed to the correct storage location through the regular put-away process.</span></span>

<span data-ttu-id="d79ba-108">Çapraz sevk, çalışanların zaten bir giden sipariş için işaretlenmiş olan stokun gelen yerine koyma ve giden çekme işlemini atlamasını sağlar.</span><span class="sxs-lookup"><span data-stu-id="d79ba-108">Cross-docking lets workers skip inbound put-away and outbound picking of inventory that is already marked for an outbound order.</span></span> <span data-ttu-id="d79ba-109">Bu sayede stok işlem sayısı olabildiğince azaltılır.</span><span class="sxs-lookup"><span data-stu-id="d79ba-109">Therefore, the number of times that inventory is touched is minimized, where possible.</span></span> <span data-ttu-id="d79ba-110">Ek olarak, sistemle daha az etkileşim olduğu için, ambardaki zaman ve alan tasarrufları artar.</span><span class="sxs-lookup"><span data-stu-id="d79ba-110">Additionally, because there is less interaction with the system, time and space savings on the warehouse shop floor are increased.</span></span>

<span data-ttu-id="d79ba-111">Çapraz sevkin çalıştırılabilmesi için, tedarik kaynağının ve çapraz sevke ilişkin diğer gereksinimler dizisinin belirtildiği yeni bir çapraz sevk şablonu yapılandırmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="d79ba-111">Before you can run cross-docking, you must configure a new cross-docking template, where the supply source and other sets of requirements for cross-docking are specified.</span></span> <span data-ttu-id="d79ba-112">Giden sipariş oluşturulurken, satır, aynı maddeyi içeren bir gelen siparişe göre işaretlenmelidir.</span><span class="sxs-lookup"><span data-stu-id="d79ba-112">As the outbound order is created, the line must be marked against an inbound order that contains the same item.</span></span> <span data-ttu-id="d79ba-113">Çapraz sevk şablonunda, stok yenileme ve satınalma siparişlerini ayarlama şeklinize benzer şekilde yönerge kodu alanını seçebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="d79ba-113">You can select the directive code field on the cross-docking template, similar to the way you set up replenishment and purchase orders.</span></span>

<span data-ttu-id="d79ba-114">Her gelen sipariş alındığında, çapraz sevk kurulumu çapraz sevk gereksinimini otomatik olarak belirler ve yerleşim yönergesinin kurulumuna göre, gereken miktar için hareket işini oluşturur.</span><span class="sxs-lookup"><span data-stu-id="d79ba-114">At the time of inbound order receiving, the cross-docking setup automatically identifies the need for cross-docking and creates the movement work for the required quantity, based on the setup of the location directive.</span></span>

> [!NOTE]
> <span data-ttu-id="d79ba-115">Bu becerinin ayarı Ambar yönetimi parametrelerinde açık olsa bile, çapraz sevk işi iptal edildiği zaman stok hareketlerinin *kaydı silinmez*.</span><span class="sxs-lookup"><span data-stu-id="d79ba-115">Inventory transactions are *not* unregistered when crossing-dock work is canceled, even if the setting for this capability is turned on in Warehouse management parameters.</span></span>

## <a name="turn-on-the-planned-cross-docking-features"></a><span data-ttu-id="d79ba-116">Planlanmış merkezden dağıtım özelliklerini açma</span><span class="sxs-lookup"><span data-stu-id="d79ba-116">Turn on the planned cross docking features</span></span>

<span data-ttu-id="d79ba-117">Sisteminiz bu konuda açıklanan özellikleri zaten içermiyorsa [Özellik yönetimi](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)'ne gidin ve aşağıdaki özellikleri aşağıdaki sırayla açın:</span><span class="sxs-lookup"><span data-stu-id="d79ba-117">If your system doesn't already include the features described in this topic, go to [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) and turn on the following features in the following order:</span></span>

1. <span data-ttu-id="d79ba-118">*Planlanmış çapraz sevk*</span><span class="sxs-lookup"><span data-stu-id="d79ba-118">*Planned cross docking*</span></span>
1. <span data-ttu-id="d79ba-119">*Yerleşim yönergeleri olan çapraz sevk şablonları*</span><span class="sxs-lookup"><span data-stu-id="d79ba-119">*Cross docking templates with location directives*</span></span>
    > [!NOTE]
    > <span data-ttu-id="d79ba-120">Bu özellik, çapraz sevk şablonunda, stok yenileme şablonlarını ayarlama şeklinize benzer şekilde **Yönerge kodu** alanının belirtilmesini sağlar.</span><span class="sxs-lookup"><span data-stu-id="d79ba-120">This feature enables the **Directive code** field to be specified on the cross-docking template, similar to the way you set up replenishment templates.</span></span> <span data-ttu-id="d79ba-121">Bu özelliği etkinleştirmek, son *Yerine koyma* satırı için çapraz sevk iş şablonu satırlarına bir yönerge kodu eklemenizi engeller.</span><span class="sxs-lookup"><span data-stu-id="d79ba-121">Enabling this feature prevents you from adding a directive code on the cross-docking work template lines for the final *Put* line.</span></span> <span data-ttu-id="d79ba-122">Bu, iş şablonlarını dikkate almadan önce son yerine koyma konumunun iş oluşturma sırasında belirlenebilmesini sağlar.</span><span class="sxs-lookup"><span data-stu-id="d79ba-122">This ensures that the final put location can be determined during work creation before considering work templates.</span></span>

## <a name="setup"></a><span data-ttu-id="d79ba-123">Ayar</span><span class="sxs-lookup"><span data-stu-id="d79ba-123">Setup</span></span>

### <a name="regenerate-load-posting-methods"></a><span data-ttu-id="d79ba-124">Yükleme deftere nakil yöntemlerini yeniden oluşturma</span><span class="sxs-lookup"><span data-stu-id="d79ba-124">Regenerate load posting methods</span></span>

<span data-ttu-id="d79ba-125">Planlanmış çapraz sevk, bir yükleme deftere nakil yöntemi olarak uygulanır.</span><span class="sxs-lookup"><span data-stu-id="d79ba-125">Planned cross-docking is implemented as a load posting method.</span></span> <span data-ttu-id="d79ba-126">Özelliği açtıktan sonra, yöntemleri yeniden oluşturmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="d79ba-126">After you turn on the feature, you must regenerate the methods.</span></span>

1. <span data-ttu-id="d79ba-127">**Ambar yönetimi \> Kurulum \> Yükleme deftere nakil yöntemleri**'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="d79ba-127">Go to **Warehouse management \> Setup \> Load posting methods**.</span></span>
1. <span data-ttu-id="d79ba-128">Eylem bölmesinde, **Yöntemleri yeniden oluştur**'u seçin.</span><span class="sxs-lookup"><span data-stu-id="d79ba-128">On the Action Pane, select **Regenerate methods**.</span></span>

    <span data-ttu-id="d79ba-129">Yeniden oluşturma işlemi tamamlanınca **Yöntem adı** değeri *planCcrossDocking* olan bir yöntem göreceksiniz.</span><span class="sxs-lookup"><span data-stu-id="d79ba-129">When regeneration is completed, you should see a method that has a **Method name** value of *planCrossDocking*.</span></span>

1. <span data-ttu-id="d79ba-130">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="d79ba-130">Close the page.</span></span>

### <a name="create-a-cross-docking-template"></a><span data-ttu-id="d79ba-131">Bir çapraz sevk şablonu oluşturma</span><span class="sxs-lookup"><span data-stu-id="d79ba-131">Create a cross-docking template</span></span>

1. <span data-ttu-id="d79ba-132">**Ambar yönetimi \> Kurulum \> İş \> Çapraz sevk şablonları**'na gidin.</span><span class="sxs-lookup"><span data-stu-id="d79ba-132">Go to **Warehouse management \> Setup \> Work \> Cross docking templates**.</span></span>
1. <span data-ttu-id="d79ba-133">Eylem bölmesinde, bir şablon oluşturmak için **Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="d79ba-133">On the Action Pane, select **New** to create a template.</span></span>
1. <span data-ttu-id="d79ba-134">Üst bilgide aşağıdaki değerleri ayarlayın:</span><span class="sxs-lookup"><span data-stu-id="d79ba-134">In the header, set the following values:</span></span>

    - <span data-ttu-id="d79ba-135">**Sıra:** *1*</span><span class="sxs-lookup"><span data-stu-id="d79ba-135">**Sequence:** *1*</span></span>

        <span data-ttu-id="d79ba-136">Bu alan, şablonların değerlendirildiği sırayı tanımlar.</span><span class="sxs-lookup"><span data-stu-id="d79ba-136">This field defines the order that templates are evaluated in.</span></span>

    - <span data-ttu-id="d79ba-137">**Çapraz sevk şablonu kodu:** *51*</span><span class="sxs-lookup"><span data-stu-id="d79ba-137">**Cross docking template ID:** *51*</span></span>
    - <span data-ttu-id="d79ba-138">**Açıklama:** *Ambar 51*</span><span class="sxs-lookup"><span data-stu-id="d79ba-138">**Description:** *Warehouse 51*</span></span>
    - <span data-ttu-id="d79ba-139">**Talep serbest bırakma ilkesi:** *Tedarik girişinden önce*</span><span class="sxs-lookup"><span data-stu-id="d79ba-139">**Demand release policy:** *Before supply receipt*</span></span>
    - <span data-ttu-id="d79ba-140">**Ambar:** *51*</span><span class="sxs-lookup"><span data-stu-id="d79ba-140">**Warehouse:** *51*</span></span>

1. <span data-ttu-id="d79ba-141">**Planlama** hızlı sekmesindeki kurulum, şablonun nasıl çalıştığını denetler.</span><span class="sxs-lookup"><span data-stu-id="d79ba-141">The setup on the **Planning** FastTab controls how the template works.</span></span> <span data-ttu-id="d79ba-142">Aşağıdaki değerleri ayarlayın:</span><span class="sxs-lookup"><span data-stu-id="d79ba-142">Set the following values:</span></span>

    - <span data-ttu-id="d79ba-143">**Talep gereksinimleri:** *Yok*</span><span class="sxs-lookup"><span data-stu-id="d79ba-143">**Demand requirements:** *None*</span></span>

        <span data-ttu-id="d79ba-144">Bu alan talep stoku gereksinimlerini tanımlar.</span><span class="sxs-lookup"><span data-stu-id="d79ba-144">This field defines the requirements of the demand inventory.</span></span> <span data-ttu-id="d79ba-145">Talebin serbest bırakmadan önce tedarikle bağlantılı olması gerekiyorsa *İşaretleme*'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="d79ba-145">If the demand must be linked to the supply before release, select *Marking*.</span></span> <span data-ttu-id="d79ba-146">Talebin serbest bırakmadan önce tedarike göre sipariş rezervasyonunun yapılması gerekiyorsa *Sipariş rezervasyonu*'nu seçin.</span><span class="sxs-lookup"><span data-stu-id="d79ba-146">If the demand must be order-reserved against the supply before release, select *Order reservation*.</span></span>

    - <span data-ttu-id="d79ba-147">**Bulma türü:** *Sevkiyat yerleşimleri*</span><span class="sxs-lookup"><span data-stu-id="d79ba-147">**Locating type:** *Shipment locations*</span></span>

        <span data-ttu-id="d79ba-148">Bu alan, çapraz sevk işinin sevk irsaliyesindeki hazırlama/yükleme yerleşimlerini kullanıp kullanmayacağını veya kendi hazırlama/yükleme yerleşimlerini bulmak için yerleşim yönergeleri kullanıp kullanmayacağını tanımlar.</span><span class="sxs-lookup"><span data-stu-id="d79ba-148">This field defines whether the cross-docking work should use the staging/load locations from the shipment, or whether it should use location directives to find its own staging/load locations.</span></span>

    - <span data-ttu-id="d79ba-149">**İş şablonu:** Bu alanı boş bırakın.</span><span class="sxs-lookup"><span data-stu-id="d79ba-149">**Work template:** Leave this field blank.</span></span>

        <span data-ttu-id="d79ba-150">Bu alan, çapraz sevk işi oluşturulduğunda kullanılması gereken iş şablonunu tanımlar.</span><span class="sxs-lookup"><span data-stu-id="d79ba-150">This field defines the work template that should be used when cross-docking work is created.</span></span>

    - <span data-ttu-id="d79ba-151">**Tedarik girişinde yeniden doğrula:** *Hayır*</span><span class="sxs-lookup"><span data-stu-id="d79ba-151">**Revalidate on supply receipt:** *No*</span></span>

        <span data-ttu-id="d79ba-152">Bu seçenek, tedarik girişi sırasında tedarikin yeniden doğrulanıp doğrulanmayacağını tanımlar.</span><span class="sxs-lookup"><span data-stu-id="d79ba-152">This option defines whether the supply should be revalidated during receipt.</span></span> <span data-ttu-id="d79ba-153">Bu seçenek *Evet* olarak ayarlanırsa , maksimum zaman aralığı ve sona erme gün sayısı aralığı da işaretlenir.</span><span class="sxs-lookup"><span data-stu-id="d79ba-153">If this option is set to *Yes*, both the maximum time window and the expiration days range are checked.</span></span>

    - <span data-ttu-id="d79ba-154">**Yönerge kodu:** Bu alanı boş bırakın</span><span class="sxs-lookup"><span data-stu-id="d79ba-154">**Directive code:** Leave this field blank</span></span>

        <span data-ttu-id="d79ba-155">Bu seçenek, *Konum yönergelerine sahip çapraz sevk şablonları* özelliği tarafından etkinleştirilir.</span><span class="sxs-lookup"><span data-stu-id="d79ba-155">This option is enabled by the *Cross docking templates with location directives* feature.</span></span> <span data-ttu-id="d79ba-156">Sistem, geçici stoku taşımak için en iyi konumu belirlemeye yardımcı olmak üzere konum yönergelerini kullanır.</span><span class="sxs-lookup"><span data-stu-id="d79ba-156">The system uses location directives to help determine the best location to move cross-docking inventory to.</span></span> <span data-ttu-id="d79ba-157">İlgili her merkezden dağıtım şablonuna bir yönerge kodu atayarak ayarlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="d79ba-157">You can set it up by assigning a directive code to each relevant cross-docking template.</span></span> <span data-ttu-id="d79ba-158">Yönerge kodu ayarlanırsa, iş oluşturulduğunda sistem yerleşim yönergelerini yönerge koduna göre arar.</span><span class="sxs-lookup"><span data-stu-id="d79ba-158">If a directive code is set, the system will search location directives by directive code when work is generated.</span></span> <span data-ttu-id="d79ba-159">Bu şekilde, belirli bir çapraz sevk şablonu için kullanılan konum yönergelerini sınırlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="d79ba-159">In this way, you can limit location directives that are used for a particular cross-docking template.</span></span>

    - <span data-ttu-id="d79ba-160">**Zaman aralığını doğrula:** *Evet*</span><span class="sxs-lookup"><span data-stu-id="d79ba-160">**Validate time window:** *Yes*</span></span>

        <span data-ttu-id="d79ba-161">Bu seçenek, bir tedarik kaynağı seçildiğinde maksimum zaman aralığının değerlendirilip değerlendirilmeyeceğini tanımlar.</span><span class="sxs-lookup"><span data-stu-id="d79ba-161">This option defines whether the maximum time window should be evaluated when a supply source is selected.</span></span> <span data-ttu-id="d79ba-162">Bu seçenek *Evet* olarak ayarlanırsa, maksimum ve minimum zaman aralıklarıyla ilgili alanlar kullanılabilir duruma gelir.</span><span class="sxs-lookup"><span data-stu-id="d79ba-162">If this option is set to *Yes*, the fields that are related to the maximum and minimum time windows become available.</span></span>

    - <span data-ttu-id="d79ba-163">**Maksimum zaman aralığı:** *5*</span><span class="sxs-lookup"><span data-stu-id="d79ba-163">**Maximum time window:** *5*</span></span>

        <span data-ttu-id="d79ba-164">Bu alan, tedarik varışı ve talep çıkışı arasında izin verilen maksimum süreyi tanımlar.</span><span class="sxs-lookup"><span data-stu-id="d79ba-164">This field defines the maximum period that is allowed between supply arrival and demand departure.</span></span>

    - <span data-ttu-id="d79ba-165">**Maksimum zaman aralığı birimi:** *Gün sayısı*</span><span class="sxs-lookup"><span data-stu-id="d79ba-165">**Maximum time window unit:** *Days*</span></span>
    - <span data-ttu-id="d79ba-166">**Minimum zaman aralığı:** *0*</span><span class="sxs-lookup"><span data-stu-id="d79ba-166">**Minimum time window:** *0*</span></span>

        <span data-ttu-id="d79ba-167">Bu alan, tedarik varışı ve talep çıkışı arasında izin verilen minimum süreyi tanımlar.</span><span class="sxs-lookup"><span data-stu-id="d79ba-167">This field defines the minimum period that is allowed between supply arrival and demand departure.</span></span>

    - <span data-ttu-id="d79ba-168">**Minimum zaman aralığı birimi:** *Gün sayısı*</span><span class="sxs-lookup"><span data-stu-id="d79ba-168">**Minimum time window unit:** *Days*</span></span>
    - <span data-ttu-id="d79ba-169">**Sona erme gün sayısı aralığı:** *0*</span><span class="sxs-lookup"><span data-stu-id="d79ba-169">**Expiration days range:** *0*</span></span>

        <span data-ttu-id="d79ba-170">*İlk sona eren ilk çıkar (FEFO) ölçütleri:* Bu alan, ambardaki mevcut ilk sona eren toplu işlemin bitiş tarihi ve alınmakta olan toplu işlem arasındaki maksimum gün sayısını tanımlar.</span><span class="sxs-lookup"><span data-stu-id="d79ba-170">*First expiry first out (FEFO) criteria:* This field defines the maximum number of days between the expiration date of the first-expiring batch that is currently in the warehouse and the batch that is being received.</span></span>

1. <span data-ttu-id="d79ba-171">**Tedarik kaynakları** hızlı sekmesinde, bu şablon için geçerli olan tedarik tiplerini belirtirsiniz.</span><span class="sxs-lookup"><span data-stu-id="d79ba-171">On the **Supply sources** FastTab, you specify the types of supply that are valid for this template.</span></span> <span data-ttu-id="d79ba-172">**Yeni**'yi seçin ve aşağıdaki değerleri ayarlayın:</span><span class="sxs-lookup"><span data-stu-id="d79ba-172">Select **New**, and then set the following values:</span></span>

    - <span data-ttu-id="d79ba-173">**Sıra numarası:** *1*</span><span class="sxs-lookup"><span data-stu-id="d79ba-173">**Sequence number:** *1*</span></span>
    - <span data-ttu-id="d79ba-174">**Tedarik kaynağı:** *Satınalma siparişi*</span><span class="sxs-lookup"><span data-stu-id="d79ba-174">**Supply source:** *Purchase order*</span></span>

### <a name="create-a-work-class"></a><span data-ttu-id="d79ba-175">İş sınıfı oluşturma</span><span class="sxs-lookup"><span data-stu-id="d79ba-175">Create a work class</span></span>

1. <span data-ttu-id="d79ba-176">**Ambar yönetimi \> Kurulum \> İş \> İş sınıfları** seçeneğine gidin.</span><span class="sxs-lookup"><span data-stu-id="d79ba-176">Go to **Warehouse management \> Setup \> Work \> Work classes**.</span></span>
1. <span data-ttu-id="d79ba-177">Eylem bölmesinde, bir iş sınıfı oluşturmak için **Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="d79ba-177">On the Action Pane, select **New** to create a work class.</span></span>
1. <span data-ttu-id="d79ba-178">Aşağıdaki değerleri ayarlayın:</span><span class="sxs-lookup"><span data-stu-id="d79ba-178">Set the following values:</span></span>

    - <span data-ttu-id="d79ba-179">**İş sınıfı kodu:** *CrossDock*</span><span class="sxs-lookup"><span data-stu-id="d79ba-179">**Work class ID:** *CrossDock*</span></span>
    - <span data-ttu-id="d79ba-180">**Açıklama:** *Çapraz Sevk*</span><span class="sxs-lookup"><span data-stu-id="d79ba-180">**Description:** *Cross Dock*</span></span>
    - <span data-ttu-id="d79ba-181">**İş emri türü:** *Çapraz sevk*</span><span class="sxs-lookup"><span data-stu-id="d79ba-181">**Work order type:** *Cross docking*</span></span>

### <a name="create-a-work-template"></a><span data-ttu-id="d79ba-182">İş şablonu oluşturma</span><span class="sxs-lookup"><span data-stu-id="d79ba-182">Create a work template</span></span>

1. <span data-ttu-id="d79ba-183">**Ambar yönetimi \> Kurulum \> İş \> İş şablonları**'na gidin.</span><span class="sxs-lookup"><span data-stu-id="d79ba-183">Go to **Warehouse management \> Setup \> Work \> Work templates**.</span></span>
1. <span data-ttu-id="d79ba-184">**İş emri türü** alanını *Çapraz sevk* olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="d79ba-184">Set the **Work order type** field to *Cross docking*.</span></span>
1. <span data-ttu-id="d79ba-185">Eylem bölmesinde, **Genel bakış** sekmesine satır eklemek için **Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="d79ba-185">On the Action Pane, select **New** to add a line to the **Overview** tab.</span></span>
1. <span data-ttu-id="d79ba-186">Yeni satırda aşağıdaki değerleri ayarlayın:</span><span class="sxs-lookup"><span data-stu-id="d79ba-186">On the new line, set the following values:</span></span>

    - <span data-ttu-id="d79ba-187">**Sıra numarası:** *1*</span><span class="sxs-lookup"><span data-stu-id="d79ba-187">**Sequence number:** *1*</span></span>
    - <span data-ttu-id="d79ba-188">**İş şablonu:** *51 Çapraz Sevk*</span><span class="sxs-lookup"><span data-stu-id="d79ba-188">**Work template:** *51 Cross Dock*</span></span>
    - <span data-ttu-id="d79ba-189">**İş şablonu açıklaması:** *51 Çapraz Sevk*</span><span class="sxs-lookup"><span data-stu-id="d79ba-189">**Work template description:** *51 Cross Dock*</span></span>

1. <span data-ttu-id="d79ba-190">**İş Şablonu Ayrıntıları** hızlı sekmesini kullanılabilir hale getirmek için **Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="d79ba-190">Select **Save** to make the **Work Template Details** FastTab available.</span></span>
1. <span data-ttu-id="d79ba-191">**İş Şablonu Ayrıntıları** hızlı sekmesinde, kılavuza satır için **Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="d79ba-191">On the **Work Template Details** FastTab, select **New** to add a line to the grid.</span></span>
1. <span data-ttu-id="d79ba-192">Yeni satırda aşağıdaki değerleri ayarlayın:</span><span class="sxs-lookup"><span data-stu-id="d79ba-192">On the new line, set the following values:</span></span>

    - <span data-ttu-id="d79ba-193">**İş türü:** *Çekme*</span><span class="sxs-lookup"><span data-stu-id="d79ba-193">**Work type:** *Pick*</span></span>
    - <span data-ttu-id="d79ba-194">**İş sınıfı kodu:** *CrossDock*</span><span class="sxs-lookup"><span data-stu-id="d79ba-194">**Work class ID:** *CrossDock*</span></span>

1. <span data-ttu-id="d79ba-195">**Yeni**'yi seçerek bir satır daha ekleyin ve üzerinde aşağıdaki değerleri ayarlayın:</span><span class="sxs-lookup"><span data-stu-id="d79ba-195">Select **New** to add another line, and set the following values on it:</span></span>

    - <span data-ttu-id="d79ba-196">**İş türü:** *Yerine koyma*</span><span class="sxs-lookup"><span data-stu-id="d79ba-196">**Work type:** *Put*</span></span>
    - <span data-ttu-id="d79ba-197">**İş sınıfı kodu:** *CrossDock*</span><span class="sxs-lookup"><span data-stu-id="d79ba-197">**Work class ID:** *CrossDock*</span></span>

1. <span data-ttu-id="d79ba-198">**Kaydet**'i seçin ve *51 Çapraz Sevk* şablonu için **Geçerli** onay kutusunun işaretlendiğini onaylayın.</span><span class="sxs-lookup"><span data-stu-id="d79ba-198">Select **Save**, and confirm that the **Valid** check box is selected for the *51 Cross Dock* template.</span></span>

> [!NOTE]
> <span data-ttu-id="d79ba-199">*Çekme* ve *Koyma* iş türleri için iş sınıfı kodları aynı olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="d79ba-199">The work class IDs for the *Pick* and *Put* work types must be the same.</span></span>

### <a name="create-location-directives"></a><span data-ttu-id="d79ba-200">Yerleşim yönergeleri oluşturma</span><span class="sxs-lookup"><span data-stu-id="d79ba-200">Create location directives</span></span>

1. <span data-ttu-id="d79ba-201">**Ambar Yönetimi \> Kurulum \> Konum yönergeleri** seçeneğine gidin.</span><span class="sxs-lookup"><span data-stu-id="d79ba-201">Go to **Warehouse management \> Setup \> Location directives**.</span></span>
1. <span data-ttu-id="d79ba-202">Sol bölmede, **İş emri türü** alanını *Çapraz sevk* olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="d79ba-202">In the left pane, set the **Work order type** field to *Cross docking*.</span></span>
1. <span data-ttu-id="d79ba-203">Eylem bölmesinde **Yeni**'yi seçin ve aşağıdaki değerleri ayarlayın:</span><span class="sxs-lookup"><span data-stu-id="d79ba-203">On the Action Pane, select **New**, and set the following values:</span></span>

    - <span data-ttu-id="d79ba-204">**Sıra numarası:** *1*</span><span class="sxs-lookup"><span data-stu-id="d79ba-204">**Sequence number:** *1*</span></span>
    - <span data-ttu-id="d79ba-205">**Ad:** *51 Çapraz Sevk Koyma*</span><span class="sxs-lookup"><span data-stu-id="d79ba-205">**Name:** *51 Cross Dock Put*</span></span>
    - <span data-ttu-id="d79ba-206">**İş türü:** *Yerine koyma*</span><span class="sxs-lookup"><span data-stu-id="d79ba-206">**Work type:** *Put*</span></span>
    - <span data-ttu-id="d79ba-207">**Tesis:** *5*</span><span class="sxs-lookup"><span data-stu-id="d79ba-207">**Site:** *5*</span></span>
    - <span data-ttu-id="d79ba-208">**Ambar:** *51*</span><span class="sxs-lookup"><span data-stu-id="d79ba-208">**Warehouse:** *51*</span></span>

1. <span data-ttu-id="d79ba-209">**Satırlar** hızlı sekmesini kullanılabilir hale getirmek için **Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="d79ba-209">Select **Save** to make the **Lines** FastTab available.</span></span>
1. <span data-ttu-id="d79ba-210">**Satırlar** hızlı sekmesinde, kılavuza satır eklemek için **Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="d79ba-210">On the **Lines** FastTab, select **New** to add a line to the grid.</span></span>
1. <span data-ttu-id="d79ba-211">Yeni satırda aşağıdaki değerleri ayarlayın:</span><span class="sxs-lookup"><span data-stu-id="d79ba-211">On the new line, set the following values:</span></span>

    - <span data-ttu-id="d79ba-212">**Başlangıç miktarı:** *1*</span><span class="sxs-lookup"><span data-stu-id="d79ba-212">**From quantity:** *1*</span></span>
    - <span data-ttu-id="d79ba-213">**Son miktar:** *1000000*</span><span class="sxs-lookup"><span data-stu-id="d79ba-213">**To quantity:** *1,000,000*</span></span>

1. <span data-ttu-id="d79ba-214">**Yerleşim Yönergesi Eylemleri** hızlı sekmesini kullanılabilir hale getirmek için **Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="d79ba-214">Select **Save** to make the **Location Directive Actions** FastTab available.</span></span>
1. <span data-ttu-id="d79ba-215">**Konum Yönerge Eylemleri** hızlı sekmesinde, kılavuza satır eklemek için **Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="d79ba-215">On the **Location Directive Actions** FastTab, select **New** to add a line to the grid.</span></span>
1. <span data-ttu-id="d79ba-216">Yeni satırda aşağıdaki değerleri ayarlayın:</span><span class="sxs-lookup"><span data-stu-id="d79ba-216">On the new line, set the following values:</span></span>

    - <span data-ttu-id="d79ba-217">**Ad:** *Baydoor*</span><span class="sxs-lookup"><span data-stu-id="d79ba-217">**Name:** *Baydoor*</span></span>
    - <span data-ttu-id="d79ba-218">**Sabit yerleşim kullanımı:** *Sabit ve sabit olmayan yerleşimler*</span><span class="sxs-lookup"><span data-stu-id="d79ba-218">**Fixed location usage:** *Fixed and non-fixed locations*</span></span>

1. <span data-ttu-id="d79ba-219">**Yerleşim Yönergesi Eylemleri** araç çubuğunda **Sorguyu düzenle** düğmesini kullanılabilir hale getirmek için **Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="d79ba-219">Select **Save** to make the **Edit query** button on the **Location Directive Actions** toolbar available.</span></span>
1. <span data-ttu-id="d79ba-220">Sorgu düzenleyicisini açmak için **Sorguyu düzenle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="d79ba-220">Select **Edit query** to open the query editor.</span></span>
1. <span data-ttu-id="d79ba-221">**Aralık** sekmesinde, aşağıdaki iki satırın yapılandırıldığından emin olun:</span><span class="sxs-lookup"><span data-stu-id="d79ba-221">On the **Range** tab, make sure that the following two lines are configured:</span></span>

    - <span data-ttu-id="d79ba-222">Satır 1:</span><span class="sxs-lookup"><span data-stu-id="d79ba-222">Line 1:</span></span>

        - <span data-ttu-id="d79ba-223">**Tablo:** *Yerleşimler*</span><span class="sxs-lookup"><span data-stu-id="d79ba-223">**Table:** *Locations*</span></span>
        - <span data-ttu-id="d79ba-224">**Türetilmiş Tablo:** *Yerleşimler*</span><span class="sxs-lookup"><span data-stu-id="d79ba-224">**Derived Table:** *Locations*</span></span>
        - <span data-ttu-id="d79ba-225">**Alan:** *Ambar*</span><span class="sxs-lookup"><span data-stu-id="d79ba-225">**Field:** *Warehouse*</span></span>
        - <span data-ttu-id="d79ba-226">**Ölçüt:** *51*</span><span class="sxs-lookup"><span data-stu-id="d79ba-226">**Criteria:** *51*</span></span>

    - <span data-ttu-id="d79ba-227">Satır 2:</span><span class="sxs-lookup"><span data-stu-id="d79ba-227">Line 2:</span></span>

        - <span data-ttu-id="d79ba-228">**Tablo:** *Yerleşimler*</span><span class="sxs-lookup"><span data-stu-id="d79ba-228">**Table:** *Locations*</span></span>
        - <span data-ttu-id="d79ba-229">**Türetilmiş Tablo:** *Yerleşimler*</span><span class="sxs-lookup"><span data-stu-id="d79ba-229">**Derived Table:** *Locations*</span></span>
        - <span data-ttu-id="d79ba-230">**Alan:** *Yerleşim*</span><span class="sxs-lookup"><span data-stu-id="d79ba-230">**Field:** *Location*</span></span>
        - <span data-ttu-id="d79ba-231">**Ölçüt:** *Baydoor*</span><span class="sxs-lookup"><span data-stu-id="d79ba-231">**Criteria:** *Baydoor*</span></span>

1. <span data-ttu-id="d79ba-232">Sorgu düzenleyicisini kapatmak için **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="d79ba-232">Select **OK** to close the query editor.</span></span>

### <a name="create-a-mobile-device-menu-item"></a><span data-ttu-id="d79ba-233">Mobil cihaz menü öğesi oluşturma</span><span class="sxs-lookup"><span data-stu-id="d79ba-233">Create a mobile device menu item</span></span>

1. <span data-ttu-id="d79ba-234">**Ambar yönetimi \> Kurulum \> Mobil cihaz \> Mobil cihaz menüsü öğeleri**'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="d79ba-234">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu items**.</span></span>
1. <span data-ttu-id="d79ba-235">Sol bölmedeki menü öğeleri listesinde, **Satınalma yerine koyma**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="d79ba-235">In the list of menu items in the left pane, select **Purchase Put-away**.</span></span>
1. <span data-ttu-id="d79ba-236">**Düzenle** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="d79ba-236">Select **Edit**.</span></span>
1. <span data-ttu-id="d79ba-237">**İş sınıfları** hızlı sekmesinde, kılavuza satır eklemek için **Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="d79ba-237">On the **Work classes** FastTab, select **New** to add a line to the grid.</span></span>
1. <span data-ttu-id="d79ba-238">Yeni satırda aşağıdaki değerleri ayarlayın:</span><span class="sxs-lookup"><span data-stu-id="d79ba-238">On the new line, set the following values:</span></span>

    - <span data-ttu-id="d79ba-239">**İş sınıfı kodu:** *CrossDock*</span><span class="sxs-lookup"><span data-stu-id="d79ba-239">**Work class ID:** *CrossDock*</span></span>
    - <span data-ttu-id="d79ba-240">**İş emri türü:** *Çapraz sevk*</span><span class="sxs-lookup"><span data-stu-id="d79ba-240">**Work order type:** *Cross docking*</span></span>

1. <span data-ttu-id="d79ba-241">**Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="d79ba-241">Select **Save**.</span></span>

## <a name="scenario"></a><span data-ttu-id="d79ba-242">Senaryo</span><span class="sxs-lookup"><span data-stu-id="d79ba-242">Scenario</span></span>

### <a name="create-a-purchase-order"></a><span data-ttu-id="d79ba-243">Satınalma siparişi oluşturma</span><span class="sxs-lookup"><span data-stu-id="d79ba-243">Create a purchase order</span></span>

<span data-ttu-id="d79ba-244">Tedarik kaynağı olarak bir satınalma siparişi oluşturmak için bu adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="d79ba-244">Follow these steps to create a purchase order as a source of supply.</span></span>

1. <span data-ttu-id="d79ba-245">**Tedarik ve kaynak atama \> Satınalma siparişleri \> Tüm satınalma siparişleri**'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="d79ba-245">Go to **Procurement and sourcing \> Purchase orders \> All purchase orders**.</span></span>
1. <span data-ttu-id="d79ba-246">Eylem Bölmesinde, **Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="d79ba-246">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="d79ba-247">**Satın alma siparişi oluştur** iletişim kutusunda, aşağıdaki değerleri ayarlayın:</span><span class="sxs-lookup"><span data-stu-id="d79ba-247">In the **Create purchase order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="d79ba-248">**Satıcı hesabı:** *104*</span><span class="sxs-lookup"><span data-stu-id="d79ba-248">**Vendor account:** *104*</span></span>
    - <span data-ttu-id="d79ba-249">**Ambar:** *51*</span><span class="sxs-lookup"><span data-stu-id="d79ba-249">**Warehouse:** *51*</span></span>

1. <span data-ttu-id="d79ba-250">**Tamam**'ı seçin ve sipariş numarasını not alın.</span><span class="sxs-lookup"><span data-stu-id="d79ba-250">Select **OK**, and make a note of the order number.</span></span>
1. <span data-ttu-id="d79ba-251">**Satınalma siparişi satırları** hızlı sekmesine yeni bir satır eklenir.</span><span class="sxs-lookup"><span data-stu-id="d79ba-251">A new line is added to the **Purchase order lines** FastTab.</span></span> <span data-ttu-id="d79ba-252">Bu satır için aşağıdaki değerleri ayarlayın:</span><span class="sxs-lookup"><span data-stu-id="d79ba-252">On this line, set the following values:</span></span>

    - <span data-ttu-id="d79ba-253">**Madde numarası:** *A0001*</span><span class="sxs-lookup"><span data-stu-id="d79ba-253">**Item number:** *A0001*</span></span>
    - <span data-ttu-id="d79ba-254">**Miktar:** *5*</span><span class="sxs-lookup"><span data-stu-id="d79ba-254">**Quantity:** *5*</span></span>

### <a name="create-a-sales-order"></a><span data-ttu-id="d79ba-255">Satış siparişi oluştur</span><span class="sxs-lookup"><span data-stu-id="d79ba-255">Create a sales order</span></span>

<span data-ttu-id="d79ba-256">Talep kaynağı olarak bir satış siparişi oluşturmak için bu adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="d79ba-256">Follow these steps to create a sales order as a source of demand.</span></span>

1. <span data-ttu-id="d79ba-257">**Satış ve pazarlama \> Satış siparişleri \> Tüm satış siparişleri**'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="d79ba-257">Go to **Sales and marketing \> Sales orders \> All sales orders**.</span></span>
1. <span data-ttu-id="d79ba-258">Eylem Bölmesinde, **Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="d79ba-258">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="d79ba-259">**Satış siparişi oluştur** iletişim kutusunda, aşağıdaki değerleri ayarlayın:</span><span class="sxs-lookup"><span data-stu-id="d79ba-259">In the **Create sales order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="d79ba-260">**Müşteri hesabı:** *US-002*</span><span class="sxs-lookup"><span data-stu-id="d79ba-260">**Customer account:** *US-002*</span></span>
    - <span data-ttu-id="d79ba-261">**Ambar:** *51*</span><span class="sxs-lookup"><span data-stu-id="d79ba-261">**Warehouse:** *51*</span></span>

1. <span data-ttu-id="d79ba-262">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="d79ba-262">Select **OK**.</span></span>
1. <span data-ttu-id="d79ba-263">**Satış siparişi satırları** hızlı sekmesine yeni bir satır eklenir.</span><span class="sxs-lookup"><span data-stu-id="d79ba-263">A new line is added to the **Sales order lines** FastTab.</span></span> <span data-ttu-id="d79ba-264">Bu satır için aşağıdaki değerleri ayarlayın:</span><span class="sxs-lookup"><span data-stu-id="d79ba-264">On this line, set the following values:</span></span>

    - <span data-ttu-id="d79ba-265">**Madde numarası:** *A0001*</span><span class="sxs-lookup"><span data-stu-id="d79ba-265">**Item number:** *A0001*</span></span>
    - <span data-ttu-id="d79ba-266">**Miktar:** *3*</span><span class="sxs-lookup"><span data-stu-id="d79ba-266">**Quantity:** *3*</span></span>

### <a name="create-planned-cross-docking"></a><span data-ttu-id="d79ba-267">Planlanmış çapraz sevk oluşturma</span><span class="sxs-lookup"><span data-stu-id="d79ba-267">Create planned cross-docking</span></span>

<span data-ttu-id="d79ba-268">Planlanmış çapraz sevki satış siparişinden oluşturmak için bu adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="d79ba-268">Follow these steps to create the planned cross-docking from the sales order.</span></span>

1. <span data-ttu-id="d79ba-269">Az önce oluşturduğunuz satış siparişinin **Satış siparişi ayrıntıları** sayfasında, eylem bölmesindeki **Ambar** sekmesinde, **Eylemler** grubunda **Ambara serbest bırak**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="d79ba-269">In the **Sales order details** page for the sales order that you just created, on the Action Pane, on the **Warehouse** tab, in the **Actions** group, select **Release to warehouse**.</span></span>

    <span data-ttu-id="d79ba-270">Ambara serbest bırakma eylemi, satış siparişi satırı için bir sevkiyat ve yükleme satırı oluşturur ve stok tahsis etmeye çalışır.</span><span class="sxs-lookup"><span data-stu-id="d79ba-270">The release to warehouse action creates a shipment and load line for the sales order line, and tries to allocate inventory.</span></span>
    
    <span data-ttu-id="d79ba-271">Bir bilgi iletisi alırsınız.</span><span class="sxs-lookup"><span data-stu-id="d79ba-271">You receive an informational message.</span></span> <span data-ttu-id="d79ba-272">Ayrıca şu uyarı iletisini alırsınız: "Dalga XXXX için iş oluşturulmadı.</span><span class="sxs-lookup"><span data-stu-id="d79ba-272">You also receive the following warning message: "No work was created for wave XXXX.</span></span> <span data-ttu-id="d79ba-273">Ayrıntılar için iş oluşturma geçmişi günlüğüne bakın."</span><span class="sxs-lookup"><span data-stu-id="d79ba-273">See the work creation history log for details."</span></span> <span data-ttu-id="d79ba-274">Ambarda stok bulunmadığı için bu davranış olağandır.</span><span class="sxs-lookup"><span data-stu-id="d79ba-274">This behavior is expected, because there is no inventory in the warehouse.</span></span>

1. <span data-ttu-id="d79ba-275">**Satış siparişi satırları** hızlı sekmesinde **Ambar** menüsünde **Sevkiyat ayrıntıları**'nı seçin.</span><span class="sxs-lookup"><span data-stu-id="d79ba-275">On the **Sales order lines** FastTab, on the **Warehouse** menu, select **Shipment details**.</span></span>

    <span data-ttu-id="d79ba-276">**Sevkiyat ayrıntıları** sayfası görüntülenir ve satış siparişi için oluşturulan sevkiyatı gösterir.</span><span class="sxs-lookup"><span data-stu-id="d79ba-276">The **Shipment details** page appears and shows the shipment that was created for the sales order.</span></span>

1. <span data-ttu-id="d79ba-277">**Yük satırları** hızlı sekmesinde, **Planlanmış çapraz sevk miktarı** alanının *3* olarak ayarlandığına dikkat edin.</span><span class="sxs-lookup"><span data-stu-id="d79ba-277">On the **Load lines** FastTab, notice that the **Planned cross docking quantity** field is set to *3*.</span></span> <span data-ttu-id="d79ba-278">Ambarda stok mevcut olmadığı halde çapraz sevk şablonunda tanımlanan zaman aralığında geçerli tedarik kaynağı geleceği için, çapraz sevk miktarı oluşturulmuştur.</span><span class="sxs-lookup"><span data-stu-id="d79ba-278">Because no inventory was available in the warehouse, but a valid supply source will arrive within the time window that is defined in the cross-docking template, the cross-docking quantity was created.</span></span>
1. <span data-ttu-id="d79ba-279">**Yük satırları** hızlı sekmesinde, oluşturulan çapraz sevkin ayrıntılarını görüntülemek için **Planlanmış çapraz sevk**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="d79ba-279">On the **Load lines** FastTab, select **Planned cross docking** to view the details of the cross-docking that was created.</span></span>

## <a name="process-the-cross-docking"></a><span data-ttu-id="d79ba-280">Çapraz sevki işleme</span><span class="sxs-lookup"><span data-stu-id="d79ba-280">Process the cross-docking</span></span>

### <a name="purchase-order-receiving-on-the-warehousing-mobile-app"></a><span data-ttu-id="d79ba-281">Ambarlama mobil uygulamasında satınalma siparişini teslim alma</span><span class="sxs-lookup"><span data-stu-id="d79ba-281">Purchase order receiving on the warehousing mobile app</span></span>

<span data-ttu-id="d79ba-282">Sistem, satınalma siparişindeki 5 miktarını teslim alma yerleşimine alır ve iki iş parçası oluşturur.</span><span class="sxs-lookup"><span data-stu-id="d79ba-282">The system will receive the quantity of 5 from the purchase order into the receiving location and create two pieces of work.</span></span>

<span data-ttu-id="d79ba-283">Oluşturulan ilk iş kodunun **İş emri türü** değeri *Çapraz sevk*'tir ve satış siparişine bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="d79ba-283">The first work ID that is created has a **Work order type** value of *Cross docking* and is linked to the sales order.</span></span> <span data-ttu-id="d79ba-284">Miktar değeri 3'tür ve hemen sevk edilebilmesi için son sevkiyat yerleşimine yönlendirilir.</span><span class="sxs-lookup"><span data-stu-id="d79ba-284">It has a quantity of 3 and is directed to the final shipping location so that it can be shipped out immediately.</span></span>

<span data-ttu-id="d79ba-285">Oluşturulan ikinci iş kodunun **İş emri türü** değeri *Satınalma siparişleri*'dir ve satınalma siparişine bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="d79ba-285">The second work ID that is created has a **Work order type** value of *Purchase orders* and is linked to the purchase order.</span></span> <span data-ttu-id="d79ba-286">Kalan miktarı 2 olan bu parça çapraz sevk edilmemiştir ve depoda yerine koymaya yönlendirilir.</span><span class="sxs-lookup"><span data-stu-id="d79ba-286">It has the remaining quantity of 2 that wasn't cross-docked and is directed to put-away to storage.</span></span>

1. <span data-ttu-id="d79ba-287">Mobil cihazda *51* kodlu ambarda bir kullanıcı olarak oturum açın.</span><span class="sxs-lookup"><span data-stu-id="d79ba-287">Sign in to the mobile device as a user in warehouse *51*.</span></span>
1. <span data-ttu-id="d79ba-288">**Gelen \> Satınalma Teslim Alma**'ya gidin.</span><span class="sxs-lookup"><span data-stu-id="d79ba-288">Go to **Inbound \> Purchase Receive**.</span></span>
1. <span data-ttu-id="d79ba-289">**PONum** alanına satınalma sipariş numaranızı girin.</span><span class="sxs-lookup"><span data-stu-id="d79ba-289">In the **PONum** field, enter your purchase order number.</span></span>
1. <span data-ttu-id="d79ba-290">**Miktar** alanına *5* girin.</span><span class="sxs-lookup"><span data-stu-id="d79ba-290">In the **Qty** field, enter *5*.</span></span>
1. <span data-ttu-id="d79ba-291">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="d79ba-291">Select **OK**.</span></span>
1. <span data-ttu-id="d79ba-292">Sonraki sayfada, **Madde** alanını *A0001* olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="d79ba-292">On the next page, set the **Item** field to *A0001*.</span></span>
1. <span data-ttu-id="d79ba-293">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="d79ba-293">Select **OK**.</span></span>
1. <span data-ttu-id="d79ba-294">Sonraki sayfada, **Tamam**'ı seçerek **PONum**, **Madde** ve **Miktar** değerlerini onaylayın.</span><span class="sxs-lookup"><span data-stu-id="d79ba-294">On the next page, confirm the **PONum**, **Item**, and **Qty** values by selecting **OK**.</span></span>

    <span data-ttu-id="d79ba-295">Bir "İş Tamamlandı" iletisi alırsınız.</span><span class="sxs-lookup"><span data-stu-id="d79ba-295">You receive a "Work Completed" message.</span></span>

1. <span data-ttu-id="d79ba-296">Çıkmak için **İptal**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="d79ba-296">Select **Cancel** to exit.</span></span>

### <a name="put-away-to-cross-docking-and-bulk"></a><span data-ttu-id="d79ba-297">Çapraz sevk ve toplu işlem için yerine koyma</span><span class="sxs-lookup"><span data-stu-id="d79ba-297">Put-away to cross-docking and bulk</span></span>

<span data-ttu-id="d79ba-298">Şu anda her iki iş kodunun da hedef plakası aynıdır.</span><span class="sxs-lookup"><span data-stu-id="d79ba-298">Currently, both work IDs have the same target license plate.</span></span> <span data-ttu-id="d79ba-299">Sonraki adımları tamamlamak için iş kodunu ve hedef plaka kodunu almanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="d79ba-299">To complete the next steps, you must get the work ID and the target license plate ID.</span></span> <span data-ttu-id="d79ba-300">Bu bilgileri satınalma siparişi satırı ve satış siparişi satırı ile ilgili iş ayrıntılardan edinebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="d79ba-300">You can get this information from the work details for the purchase order line and the sales order line.</span></span> <span data-ttu-id="d79ba-301">Alternatif olarak, **Ambar yönetimi \> İş \> İş ayrıntıları**'na gidip **Ambar** değerinin *51* olduğu işi filtreleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="d79ba-301">Alternately, you can go to **Warehouse management \> Work \> Work details** and filter for work where the **Warehouse** value is *51*.</span></span>

1. <span data-ttu-id="d79ba-302">Mobil cihazda **Gelen \> Satın alma yerine koyma**'ya gidin ve işin hedef plakasını girin.</span><span class="sxs-lookup"><span data-stu-id="d79ba-302">On the mobile device, go to **Inbound \> Purchase put-away**, and enter the target license plate from the work.</span></span>
1. <span data-ttu-id="d79ba-303">**Kod** alanına, iş ayrıntılarından alınan hedef plaka kodunu girin.</span><span class="sxs-lookup"><span data-stu-id="d79ba-303">In the **ID** field, enter the target license plate ID from the work details.</span></span>

    <span data-ttu-id="d79ba-304">Çapraz sevk çekme sayfası, malzeme çekme yerleşimini (*RECV*), hedef plakayı ( *plaka*), maddeyi (*A0001*) ve miktarı ( *3*) gösterir.</span><span class="sxs-lookup"><span data-stu-id="d79ba-304">The cross-docking pick page shows the picking location (*RECV*), target license plate (*license plate*), item (*A0001*), and quantity (*3*).</span></span>

1. <span data-ttu-id="d79ba-305">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="d79ba-305">Select **OK**.</span></span>
1. <span data-ttu-id="d79ba-306">**Hedef Plaka** alanına, sevkiyat yerleşimine yerleştirilmesi (çapraz sevk edilmesi) gereken plaka kodu için bir hedef plaka girin.</span><span class="sxs-lookup"><span data-stu-id="d79ba-306">In the **Target LP** field, enter a target license plate for the license plate ID that should be put (cross-docked) to the shipping location.</span></span> <span data-ttu-id="d79ba-307">İstediğiniz herhangi bir plaka kodunu seçebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="d79ba-307">You can select any license plate ID of your choice.</span></span>
1. <span data-ttu-id="d79ba-308">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="d79ba-308">Select **OK**.</span></span>
1. <span data-ttu-id="d79ba-309">Sonraki sayfada, **Kod** alanına, hedef plaka kodunu girin.</span><span class="sxs-lookup"><span data-stu-id="d79ba-309">On the next page, in the **ID** field, enter the target license plate ID.</span></span>
1. <span data-ttu-id="d79ba-310">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="d79ba-310">Select **OK**.</span></span>
1. <span data-ttu-id="d79ba-311">Kalan 2 miktarını çekmek için işi onaylayın ve **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="d79ba-311">Confirm the work for picking the remaining quantity of 2, and then select **OK**.</span></span>
1. <span data-ttu-id="d79ba-312">Sonraki sayfada, malzeme çekme işlemini bitirmek ve yerine koyma işlemine başlamak için **Bitti**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="d79ba-312">On the next page, select **Done** to end the picking process and begin the put-away process.</span></span>

    <span data-ttu-id="d79ba-313">Mobil uygulama, size, maddenin yerleştirileceği yerleşimi ve plakayı verir.</span><span class="sxs-lookup"><span data-stu-id="d79ba-313">The mobile app presents you with the location and license plate to put the item to.</span></span>

1. <span data-ttu-id="d79ba-314">**Tamam**'ı seçerek toplu depolama **Koyma** işlemini onaylayın.</span><span class="sxs-lookup"><span data-stu-id="d79ba-314">Confirm the bulk storage **Put** by selecting **OK**.</span></span>
1. <span data-ttu-id="d79ba-315">Sonraki sayfada, **Tamam**'ı seçerek çapraz sevk **Koyma** işlemini onaylayın.</span><span class="sxs-lookup"><span data-stu-id="d79ba-315">On the next page, confirm the cross-docking **Put** by selecting **OK**.</span></span>

    <span data-ttu-id="d79ba-316">Bir "İş Tamamlandı" iletisi alırsınız.</span><span class="sxs-lookup"><span data-stu-id="d79ba-316">You receive a "Work Completed" message.</span></span>

1. <span data-ttu-id="d79ba-317">Çıkmak için **İptal**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="d79ba-317">Select **Cancel** to exit.</span></span>

<span data-ttu-id="d79ba-318">Aşağıdaki şekil, tamamlanmış çapraz sevk işinin Microsoft Dynamics 365 Supply Chain Management'ta nasıl görünebileceğini gösteriyor.</span><span class="sxs-lookup"><span data-stu-id="d79ba-318">The following illustration shows how the completed cross-docking work might appear in Microsoft Dynamics 365 Supply Chain Management.</span></span>

<span data-ttu-id="d79ba-319">![Tamamlanmış çapraz sevk işi](media/PlannedCrossDockingWork.png "Tamamlanmış çapraz sevk işi")</span><span class="sxs-lookup"><span data-stu-id="d79ba-319">![Cross-docking work completed](media/PlannedCrossDockingWork.png "Cross-docking work completed")</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]