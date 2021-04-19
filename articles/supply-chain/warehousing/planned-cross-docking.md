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
ms.openlocfilehash: 49807c90c145eee55fae2d515fd19925eb2d944c
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/01/2021
ms.locfileid: "5810426"
---
# <a name="planned-cross-docking"></a><span data-ttu-id="b60e6-104">Planlanmış çapraz sevk</span><span class="sxs-lookup"><span data-stu-id="b60e6-104">Planned cross-docking</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b60e6-105">Bu konuda, ileri düzeyde planlı çapraz sevk açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="b60e6-105">This topic describes advanced planned cross-docking.</span></span> <span data-ttu-id="b60e6-106">Çapraz sevk, bir sipariş için gereken stok miktarının kabulden veya oluşturma aşamasından doğru çıkış noktasına veya hazırlama alanına kadar yönlendirildiği bir ambar sürecidir.</span><span class="sxs-lookup"><span data-stu-id="b60e6-106">Cross-docking is a warehouse process where the inventory quantity that is required for an order is directed straight from receipt or creation to the correct outbound dock or staging area.</span></span> <span data-ttu-id="b60e6-107">Gelen kaynaktan kalan tüm stok, normal yerine koyma işlemiyle doğru depolama yerleşimine yönlendirilir.</span><span class="sxs-lookup"><span data-stu-id="b60e6-107">All remaining inventory from the inbound source is directed to the correct storage location through the regular put-away process.</span></span>

<span data-ttu-id="b60e6-108">Çapraz sevk, çalışanların zaten bir giden sipariş için işaretlenmiş olan stokun gelen yerine koyma ve giden çekme işlemini atlamasını sağlar.</span><span class="sxs-lookup"><span data-stu-id="b60e6-108">Cross-docking lets workers skip inbound put-away and outbound picking of inventory that is already marked for an outbound order.</span></span> <span data-ttu-id="b60e6-109">Bu sayede stok işlem sayısı olabildiğince azaltılır.</span><span class="sxs-lookup"><span data-stu-id="b60e6-109">Therefore, the number of times that inventory is touched is minimized, where possible.</span></span> <span data-ttu-id="b60e6-110">Ek olarak, sistemle daha az etkileşim olduğu için, ambardaki zaman ve alan tasarrufları artar.</span><span class="sxs-lookup"><span data-stu-id="b60e6-110">Additionally, because there is less interaction with the system, time and space savings on the warehouse shop floor are increased.</span></span>

<span data-ttu-id="b60e6-111">Çapraz sevkin çalıştırılabilmesi için, kullanıcının tedarik kaynağının ve çapraz sevke ilişkin diğer gereksinimler dizisinin belirtildiği yeni bir çapraz sevk şablonu yapılandırması gerekir.</span><span class="sxs-lookup"><span data-stu-id="b60e6-111">Before cross-docking can be run, the user must configure a new cross-docking template, where the supply source and other sets of requirements for cross-docking are specified.</span></span> <span data-ttu-id="b60e6-112">Giden sipariş oluşturulurken, satır, aynı maddeyi içeren bir gelen siparişe göre işaretlenmelidir.</span><span class="sxs-lookup"><span data-stu-id="b60e6-112">As the outbound order is created, the line must be marked against an inbound order that contains the same item.</span></span>

<span data-ttu-id="b60e6-113">Her gelen sipariş alındığında, çapraz sevk kurulumu çapraz sevk gereksinimini otomatik olarak belirler ve yerleşim yönergesinin kurulumuna göre, gereken miktar için hareket işini oluşturur.</span><span class="sxs-lookup"><span data-stu-id="b60e6-113">At the time of inbound order receiving, the cross-docking setup automatically identifies the need for cross-docking and creates the movement work for the required quantity, based on the setup of the location directive.</span></span>

> [!NOTE]
> <span data-ttu-id="b60e6-114">Bu becerinin ayarı Ambar yönetimi parametrelerinde açık olsa bile, çapraz sevk işi iptal edildiği zaman stok hareketlerinin **kaydı silinmez**.</span><span class="sxs-lookup"><span data-stu-id="b60e6-114">Inventory transactions are **not** unregistered when crossing-dock work is canceled, even if the setting for this capability is turned on in Warehouse management parameters.</span></span>

## <a name="turn-on-the-planned-cross-docking-features"></a><span data-ttu-id="b60e6-115">Planlanmış merkezden dağıtım özelliklerini açma</span><span class="sxs-lookup"><span data-stu-id="b60e6-115">Turn on the planned cross docking features</span></span>

<span data-ttu-id="b60e6-116">Sisteminiz bu konuda açıklanan özellikleri zaten içermiyorsa [Özellik yönetimi](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)'ne gidin ve aşağıdaki özellikleri aşağıdaki sırayla açın:</span><span class="sxs-lookup"><span data-stu-id="b60e6-116">If your system doesn't already include the features described in this topic, go to [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) and turn on the following features in the following order:</span></span>

1. <span data-ttu-id="b60e6-117">*Planlanmış çapraz sevk*</span><span class="sxs-lookup"><span data-stu-id="b60e6-117">*Planned cross docking*</span></span>
2. <span data-ttu-id="b60e6-118">*Yerleşim yönergeleri olan çapraz sevk şablonları*</span><span class="sxs-lookup"><span data-stu-id="b60e6-118">*Cross docking templates with location directives*</span></span>

## <a name="setup"></a><span data-ttu-id="b60e6-119">Ayar</span><span class="sxs-lookup"><span data-stu-id="b60e6-119">Setup</span></span>

### <a name="regenerate-load-posting-methods"></a><span data-ttu-id="b60e6-120">Yükleme deftere nakil yöntemlerini yeniden oluşturma</span><span class="sxs-lookup"><span data-stu-id="b60e6-120">Regenerate load posting methods</span></span>

<span data-ttu-id="b60e6-121">Planlanmış çapraz sevk, bir yükleme deftere nakil yöntemi olarak uygulanır.</span><span class="sxs-lookup"><span data-stu-id="b60e6-121">Planned cross-docking is implemented as a load posting method.</span></span> <span data-ttu-id="b60e6-122">Özelliği açtıktan sonra, yöntemleri yeniden oluşturmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="b60e6-122">After you turn on the feature, you must regenerate the methods.</span></span>

1. <span data-ttu-id="b60e6-123">**Ambar yönetimi \> Kurulum \> Yükleme deftere nakil yöntemleri**'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="b60e6-123">Go to **Warehouse management \> Setup \> Load posting methods**.</span></span>
1. <span data-ttu-id="b60e6-124">Eylem bölmesinde, **Yöntemleri yeniden oluştur**'u seçin.</span><span class="sxs-lookup"><span data-stu-id="b60e6-124">On the Action Pane, select **Regenerate methods**.</span></span>

    <span data-ttu-id="b60e6-125">Yeniden oluşturma işlemi tamamlanınca **Yöntem adı** değeri *planCcrossDocking* olan bir yöntem göreceksiniz.</span><span class="sxs-lookup"><span data-stu-id="b60e6-125">When regeneration is completed, you should see a method that has a **Method name** value of *planCrossDocking*.</span></span>

1. <span data-ttu-id="b60e6-126">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="b60e6-126">Close the page.</span></span>

### <a name="create-a-cross-docking-template"></a><span data-ttu-id="b60e6-127">Bir çapraz sevk şablonu oluşturma</span><span class="sxs-lookup"><span data-stu-id="b60e6-127">Create a cross-docking template</span></span>

1. <span data-ttu-id="b60e6-128">**Ambar yönetimi \> Kurulum \> İş \> Çapraz sevk şablonları**'na gidin.</span><span class="sxs-lookup"><span data-stu-id="b60e6-128">Go to **Warehouse management \> Setup \> Work \> Cross docking templates**.</span></span>
1. <span data-ttu-id="b60e6-129">Eylem bölmesinde, bir şablon oluşturmak için **Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="b60e6-129">On the Action Pane, select **New** to create a template.</span></span>
1. <span data-ttu-id="b60e6-130">Üst bilgide aşağıdaki değerleri ayarlayın:</span><span class="sxs-lookup"><span data-stu-id="b60e6-130">In the header, set the following values:</span></span>

    - <span data-ttu-id="b60e6-131">**Sıra:** *1*</span><span class="sxs-lookup"><span data-stu-id="b60e6-131">**Sequence:** *1*</span></span>

        <span data-ttu-id="b60e6-132">Bu alan, şablonların değerlendirildiği sırayı tanımlar.</span><span class="sxs-lookup"><span data-stu-id="b60e6-132">This field defines the order that templates are evaluated in.</span></span>

    - <span data-ttu-id="b60e6-133">**Çapraz sevk şablonu kodu:** *51*</span><span class="sxs-lookup"><span data-stu-id="b60e6-133">**Cross docking template ID:** *51*</span></span>
    - <span data-ttu-id="b60e6-134">**Açıklama:** *Ambar 51*</span><span class="sxs-lookup"><span data-stu-id="b60e6-134">**Description:** *Warehouse 51*</span></span>
    - <span data-ttu-id="b60e6-135">**Talep serbest bırakma ilkesi:** *Tedarik girişinden önce*</span><span class="sxs-lookup"><span data-stu-id="b60e6-135">**Demand release policy:** *Before supply receipt*</span></span>
    - <span data-ttu-id="b60e6-136">**Ambar:** *51*</span><span class="sxs-lookup"><span data-stu-id="b60e6-136">**Warehouse:** *51*</span></span>

1. <span data-ttu-id="b60e6-137">**Planlama** hızlı sekmesindeki kurulum, şablonun nasıl çalıştığını denetler.</span><span class="sxs-lookup"><span data-stu-id="b60e6-137">The setup on the **Planning** FastTab controls how the template works.</span></span> <span data-ttu-id="b60e6-138">Aşağıdaki değerleri ayarlayın:</span><span class="sxs-lookup"><span data-stu-id="b60e6-138">Set the following values:</span></span>

    - <span data-ttu-id="b60e6-139">**Talep gereksinimleri:** *Yok*</span><span class="sxs-lookup"><span data-stu-id="b60e6-139">**Demand requirements:** *None*</span></span>

        <span data-ttu-id="b60e6-140">Bu alan talep stoku gereksinimlerini tanımlar.</span><span class="sxs-lookup"><span data-stu-id="b60e6-140">This field defines the requirements of the demand inventory.</span></span> <span data-ttu-id="b60e6-141">Talebin serbest bırakmadan önce tedarikle bağlantılı olması gerekiyorsa *İşaretleme*'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="b60e6-141">If the demand must be linked to the supply before release, select *Marking*.</span></span> <span data-ttu-id="b60e6-142">Talebin serbest bırakmadan önce tedarike göre sipariş rezervasyonunun yapılması gerekiyorsa *Sipariş rezervasyonu*'nu seçin.</span><span class="sxs-lookup"><span data-stu-id="b60e6-142">If the demand must be order-reserved against the supply before release, select *Order reservation*.</span></span>

    - <span data-ttu-id="b60e6-143">**Bulma türü:** *Sevkiyat yerleşimleri*</span><span class="sxs-lookup"><span data-stu-id="b60e6-143">**Locating type:** *Shipment locations*</span></span>

        <span data-ttu-id="b60e6-144">Bu alan, çapraz sevk işinin sevk irsaliyesindeki hazırlama/yükleme yerleşimlerini kullanıp kullanmayacağını veya kendi hazırlama/yükleme yerleşimlerini bulmak için yerleşim yönergeleri kullanıp kullanmayacağını tanımlar.</span><span class="sxs-lookup"><span data-stu-id="b60e6-144">This field defines whether the cross-docking work should use the staging/load locations from the shipment, or whether it should use location directives to find its own staging/load locations.</span></span>

    - <span data-ttu-id="b60e6-145">**İş şablonu:** Bu alanı boş bırakın.</span><span class="sxs-lookup"><span data-stu-id="b60e6-145">**Work template:** Leave this field blank.</span></span>

        <span data-ttu-id="b60e6-146">Bu alan, çapraz sevk işi oluşturulduğunda kullanılması gereken iş şablonunu tanımlar.</span><span class="sxs-lookup"><span data-stu-id="b60e6-146">This field defines the work template that should be used when cross-docking work is created.</span></span>

    - <span data-ttu-id="b60e6-147">**Tedarik girişinde yeniden doğrula:** *Hayır*</span><span class="sxs-lookup"><span data-stu-id="b60e6-147">**Revalidate on supply receipt:** *No*</span></span>

        <span data-ttu-id="b60e6-148">Bu seçenek, tedarik girişi sırasında tedarikin yeniden doğrulanıp doğrulanmayacağını tanımlar.</span><span class="sxs-lookup"><span data-stu-id="b60e6-148">This option defines whether the supply should be revalidated during receipt.</span></span> <span data-ttu-id="b60e6-149">Bu seçenek *Evet* olarak ayarlanırsa , maksimum zaman aralığı ve sona erme gün sayısı aralığı da işaretlenir.</span><span class="sxs-lookup"><span data-stu-id="b60e6-149">If this option is set to *Yes*, both the maximum time window and the expiration days range are checked.</span></span>

    - <span data-ttu-id="b60e6-150">**Yönerge kodu** Bu alanı boş bırakın</span><span class="sxs-lookup"><span data-stu-id="b60e6-150">**Directive code** Leave this field blank</span></span>

        <span data-ttu-id="b60e6-151">Bu seçenek, sistemin geçici stoku taşımak için en iyi konumu belirlemeye yardımcı olmak üzere konum yönergelerini kullanmasını sağlar.</span><span class="sxs-lookup"><span data-stu-id="b60e6-151">This option enables the system to use location directives to help determine the best location to move cross-docking inventory to.</span></span> <span data-ttu-id="b60e6-152">İlgili her merkezden dağıtım şablonuna bir yönerge kodu atayarak ayarlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="b60e6-152">You can set it up by assigning a directive code to each relevant cross-docking template.</span></span> <span data-ttu-id="b60e6-153">Her yönerge kodu benzersiz bir konum yönergesi tanımlar.</span><span class="sxs-lookup"><span data-stu-id="b60e6-153">Each directive code identifies a unique location directive.</span></span>

    - <span data-ttu-id="b60e6-154">**Zaman aralığını doğrula:** *Evet*</span><span class="sxs-lookup"><span data-stu-id="b60e6-154">**Validate time window:** *Yes*</span></span>

        <span data-ttu-id="b60e6-155">Bu seçenek, bir tedarik kaynağı seçildiğinde maksimum zaman aralığının değerlendirilip değerlendirilmeyeceğini tanımlar.</span><span class="sxs-lookup"><span data-stu-id="b60e6-155">This option defines whether the maximum time window should be evaluated when a supply source is selected.</span></span> <span data-ttu-id="b60e6-156">Bu seçenek *Evet* olarak ayarlanırsa, maksimum ve minimum zaman aralıklarıyla ilgili alanlar kullanılabilir duruma gelir.</span><span class="sxs-lookup"><span data-stu-id="b60e6-156">If this option is set to *Yes*, the fields that are related to the maximum and minimum time windows become available.</span></span>

    - <span data-ttu-id="b60e6-157">**Maksimum zaman aralığı:** *5*</span><span class="sxs-lookup"><span data-stu-id="b60e6-157">**Maximum time window:** *5*</span></span>

        <span data-ttu-id="b60e6-158">Bu alan, tedarik varışı ve talep çıkışı arasında izin verilen maksimum süreyi tanımlar.</span><span class="sxs-lookup"><span data-stu-id="b60e6-158">This field defines the maximum period that is allowed between supply arrival and demand departure.</span></span>

    - <span data-ttu-id="b60e6-159">**Maksimum zaman aralığı birimi:** *Gün sayısı*</span><span class="sxs-lookup"><span data-stu-id="b60e6-159">**Maximum time window unit:** *Days*</span></span>
    - <span data-ttu-id="b60e6-160">**Minimum zaman aralığı:** *0*</span><span class="sxs-lookup"><span data-stu-id="b60e6-160">**Minimum time window:** *0*</span></span>

        <span data-ttu-id="b60e6-161">Bu alan, tedarik varışı ve talep çıkışı arasında izin verilen minimum süreyi tanımlar.</span><span class="sxs-lookup"><span data-stu-id="b60e6-161">This field defines the minimum period that is allowed between supply arrival and demand departure.</span></span>

    - <span data-ttu-id="b60e6-162">**Minimum zaman aralığı birimi:** *Gün sayısı*</span><span class="sxs-lookup"><span data-stu-id="b60e6-162">**Minimum time window unit:** *Days*</span></span>
    - <span data-ttu-id="b60e6-163">**Sona erme gün sayısı aralığı:** *0*</span><span class="sxs-lookup"><span data-stu-id="b60e6-163">**Expiration days range:** *0*</span></span>

        <span data-ttu-id="b60e6-164">*İlk sona eren ilk çıkar (FEFO) ölçütleri:* Bu alan, ambardaki mevcut ilk sona eren toplu işlemin bitiş tarihi ve alınmakta olan toplu işlem arasındaki maksimum gün sayısını tanımlar.</span><span class="sxs-lookup"><span data-stu-id="b60e6-164">*First expiry first out (FEFO) criteria:* This field defines the maximum number of days between the expiration date of the first-expiring batch that is currently in the warehouse and the batch that is being received.</span></span>

1. <span data-ttu-id="b60e6-165">**Tedarik kaynakları** hızlı sekmesinde, bu şablon için geçerli olan tedarik tiplerini belirtirsiniz.</span><span class="sxs-lookup"><span data-stu-id="b60e6-165">On the **Supply sources** FastTab, you specify the types of supply that are valid for this template.</span></span> <span data-ttu-id="b60e6-166">**Yeni**'yi seçin ve aşağıdaki değerleri ayarlayın:</span><span class="sxs-lookup"><span data-stu-id="b60e6-166">Select **New**, and then set the following values:</span></span>

    - <span data-ttu-id="b60e6-167">**Sıra numarası:** *1*</span><span class="sxs-lookup"><span data-stu-id="b60e6-167">**Sequence number:** *1*</span></span>
    - <span data-ttu-id="b60e6-168">**Tedarik kaynağı:** *Satınalma siparişi*</span><span class="sxs-lookup"><span data-stu-id="b60e6-168">**Supply source:** *Purchase order*</span></span>

### <a name="create-a-work-class"></a><span data-ttu-id="b60e6-169">İş sınıfı oluşturma</span><span class="sxs-lookup"><span data-stu-id="b60e6-169">Create a work class</span></span>

1. <span data-ttu-id="b60e6-170">**Ambar yönetimi \> Kurulum \> İş \> İş sınıfları** seçeneğine gidin.</span><span class="sxs-lookup"><span data-stu-id="b60e6-170">Go to **Warehouse management \> Setup \> Work \> Work classes**.</span></span>
1. <span data-ttu-id="b60e6-171">Eylem bölmesinde, bir iş sınıfı oluşturmak için **Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="b60e6-171">On the Action Pane, select **New** to create a work class.</span></span>
1. <span data-ttu-id="b60e6-172">Aşağıdaki değerleri ayarlayın:</span><span class="sxs-lookup"><span data-stu-id="b60e6-172">Set the following values:</span></span>

    - <span data-ttu-id="b60e6-173">**İş sınıfı kodu:** *CrossDock*</span><span class="sxs-lookup"><span data-stu-id="b60e6-173">**Work class ID:** *CrossDock*</span></span>
    - <span data-ttu-id="b60e6-174">**Açıklama:** *Çapraz Sevk*</span><span class="sxs-lookup"><span data-stu-id="b60e6-174">**Description:** *Cross Dock*</span></span>
    - <span data-ttu-id="b60e6-175">**İş emri türü:** *Çapraz sevk*</span><span class="sxs-lookup"><span data-stu-id="b60e6-175">**Work order type:** *Cross docking*</span></span>

### <a name="create-a-work-template"></a><span data-ttu-id="b60e6-176">İş şablonu oluşturma</span><span class="sxs-lookup"><span data-stu-id="b60e6-176">Create a work template</span></span>

1. <span data-ttu-id="b60e6-177">**Ambar yönetimi \> Kurulum \> İş \> İş şablonları**'na gidin.</span><span class="sxs-lookup"><span data-stu-id="b60e6-177">Go to **Warehouse management \> Setup \> Work \> Work templates**.</span></span>
1. <span data-ttu-id="b60e6-178">**İş emri türü** alanını *Çapraz sevk* olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="b60e6-178">Set the **Work order type** field to *Cross docking*.</span></span>
1. <span data-ttu-id="b60e6-179">Eylem bölmesinde, **Genel bakış** sekmesine satır eklemek için **Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="b60e6-179">On the Action Pane, select **New** to add a line to the **Overview** tab.</span></span>
1. <span data-ttu-id="b60e6-180">Yeni satırda aşağıdaki değerleri ayarlayın:</span><span class="sxs-lookup"><span data-stu-id="b60e6-180">On the new line, set the following values:</span></span>

    - <span data-ttu-id="b60e6-181">**Sıra numarası:** *1*</span><span class="sxs-lookup"><span data-stu-id="b60e6-181">**Sequence number:** *1*</span></span>
    - <span data-ttu-id="b60e6-182">**İş şablonu:** *51 Çapraz Sevk*</span><span class="sxs-lookup"><span data-stu-id="b60e6-182">**Work template:** *51 Cross Dock*</span></span>
    - <span data-ttu-id="b60e6-183">**İş şablonu açıklaması:** *51 Çapraz Sevk*</span><span class="sxs-lookup"><span data-stu-id="b60e6-183">**Work template description:** *51 Cross Dock*</span></span>

1. <span data-ttu-id="b60e6-184">**İş Şablonu Ayrıntıları** hızlı sekmesini kullanılabilir hale getirmek için **Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="b60e6-184">Select **Save** to make the **Work Template Details** FastTab available.</span></span>
1. <span data-ttu-id="b60e6-185">**İş Şablonu Ayrıntıları** hızlı sekmesinde, kılavuza satır için **Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="b60e6-185">On the **Work Template Details** FastTab, select **New** to add a line to the grid.</span></span>
1. <span data-ttu-id="b60e6-186">Yeni satırda aşağıdaki değerleri ayarlayın:</span><span class="sxs-lookup"><span data-stu-id="b60e6-186">On the new line, set the following values:</span></span>

    - <span data-ttu-id="b60e6-187">**İş türü:** *Çekme*</span><span class="sxs-lookup"><span data-stu-id="b60e6-187">**Work type:** *Pick*</span></span>
    - <span data-ttu-id="b60e6-188">**İş sınıfı kodu:** *CrossDock*</span><span class="sxs-lookup"><span data-stu-id="b60e6-188">**Work class ID:** *CrossDock*</span></span>

1. <span data-ttu-id="b60e6-189">**Yeni**'yi seçerek bir satır daha ekleyin ve üzerinde aşağıdaki değerleri ayarlayın:</span><span class="sxs-lookup"><span data-stu-id="b60e6-189">Select **New** to add another line, and set the following values on it:</span></span>

    - <span data-ttu-id="b60e6-190">**İş türü:** *Yerine koyma*</span><span class="sxs-lookup"><span data-stu-id="b60e6-190">**Work type:** *Put*</span></span>
    - <span data-ttu-id="b60e6-191">**İş sınıfı kodu:** *CrossDock*</span><span class="sxs-lookup"><span data-stu-id="b60e6-191">**Work class ID:** *CrossDock*</span></span>

1. <span data-ttu-id="b60e6-192">**Kaydet**'i seçin ve *51 Çapraz Sevk* şablonu için **Geçerli** onay kutusunun işaretlendiğini onaylayın.</span><span class="sxs-lookup"><span data-stu-id="b60e6-192">Select **Save**, and confirm that the **Valid** check box is selected for the *51 Cross Dock* template.</span></span>

> [!NOTE]
> <span data-ttu-id="b60e6-193">*Çekme* ve *Koyma* iş türleri için iş sınıfı kodları aynı olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="b60e6-193">The work class IDs for the *Pick* and *Put* work types must be the same.</span></span>

### <a name="create-location-directives"></a><span data-ttu-id="b60e6-194">Yerleşim yönergeleri oluşturma</span><span class="sxs-lookup"><span data-stu-id="b60e6-194">Create location directives</span></span>

1. <span data-ttu-id="b60e6-195">**Ambar Yönetimi \> Kurulum \> Konum yönergeleri** seçeneğine gidin.</span><span class="sxs-lookup"><span data-stu-id="b60e6-195">Go to **Warehouse management \> Setup \> Location directives**.</span></span>
1. <span data-ttu-id="b60e6-196">Sol bölmede, **İş emri türü** alanını *Çapraz sevk* olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="b60e6-196">In the left pane, set the **Work order type** field to *Cross docking*.</span></span>
1. <span data-ttu-id="b60e6-197">Eylem bölmesinde **Yeni**'yi seçin ve aşağıdaki değerleri ayarlayın:</span><span class="sxs-lookup"><span data-stu-id="b60e6-197">On the Action Pane, select **New**, and set the following values:</span></span>

    - <span data-ttu-id="b60e6-198">**Sıra numarası:** *1*</span><span class="sxs-lookup"><span data-stu-id="b60e6-198">**Sequence number:** *1*</span></span>
    - <span data-ttu-id="b60e6-199">**Ad:** *51 Çapraz Sevk Koyma*</span><span class="sxs-lookup"><span data-stu-id="b60e6-199">**Name:** *51 Cross Dock Put*</span></span>
    - <span data-ttu-id="b60e6-200">**İş türü:** *Yerine koyma*</span><span class="sxs-lookup"><span data-stu-id="b60e6-200">**Work type:** *Put*</span></span>
    - <span data-ttu-id="b60e6-201">**Tesis:** *5*</span><span class="sxs-lookup"><span data-stu-id="b60e6-201">**Site:** *5*</span></span>
    - <span data-ttu-id="b60e6-202">**Ambar:** *51*</span><span class="sxs-lookup"><span data-stu-id="b60e6-202">**Warehouse:** *51*</span></span>

1. <span data-ttu-id="b60e6-203">**Satırlar** hızlı sekmesini kullanılabilir hale getirmek için **Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="b60e6-203">Select **Save** to make the **Lines** FastTab available.</span></span>
1. <span data-ttu-id="b60e6-204">**Satırlar** hızlı sekmesinde, kılavuza satır eklemek için **Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="b60e6-204">On the **Lines** FastTab, select **New** to add a line to the grid.</span></span>
1. <span data-ttu-id="b60e6-205">Yeni satırda aşağıdaki değerleri ayarlayın:</span><span class="sxs-lookup"><span data-stu-id="b60e6-205">On the new line, set the following values:</span></span>

    - <span data-ttu-id="b60e6-206">**Başlangıç miktarı:** *1*</span><span class="sxs-lookup"><span data-stu-id="b60e6-206">**From quantity:** *1*</span></span>
    - <span data-ttu-id="b60e6-207">**Son miktar:** *1000000*</span><span class="sxs-lookup"><span data-stu-id="b60e6-207">**To quantity:** *1,000,000*</span></span>

1. <span data-ttu-id="b60e6-208">**Yerleşim Yönergesi Eylemleri** hızlı sekmesini kullanılabilir hale getirmek için **Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="b60e6-208">Select **Save** to make the **Location Directive Actions** FastTab available.</span></span>
1. <span data-ttu-id="b60e6-209">**Konum Yönerge Eylemleri** hızlı sekmesinde, kılavuza satır eklemek için **Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="b60e6-209">On the **Location Directive Actions** FastTab, select **New** to add a line to the grid.</span></span>
1. <span data-ttu-id="b60e6-210">Yeni satırda aşağıdaki değerleri ayarlayın:</span><span class="sxs-lookup"><span data-stu-id="b60e6-210">On the new line, set the following values:</span></span>

    - <span data-ttu-id="b60e6-211">**Ad:** *Baydoor*</span><span class="sxs-lookup"><span data-stu-id="b60e6-211">**Name:** *Baydoor*</span></span>
    - <span data-ttu-id="b60e6-212">**Sabit yerleşim kullanımı:** *Sabit ve sabit olmayan yerleşimler*</span><span class="sxs-lookup"><span data-stu-id="b60e6-212">**Fixed location usage:** *Fixed and non-fixed locations*</span></span>

1. <span data-ttu-id="b60e6-213">**Yerleşim Yönergesi Eylemleri** araç çubuğunda **Sorguyu düzenle** düğmesini kullanılabilir hale getirmek için **Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="b60e6-213">Select **Save** to make the **Edit query** button on the **Location Directive Actions** toolbar available.</span></span>
1. <span data-ttu-id="b60e6-214">Sorgu düzenleyicisini açmak için **Sorguyu düzenle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="b60e6-214">Select **Edit query** to open the query editor.</span></span>
1. <span data-ttu-id="b60e6-215">**Aralık** sekmesinde, aşağıdaki iki satırın yapılandırıldığından emin olun:</span><span class="sxs-lookup"><span data-stu-id="b60e6-215">On the **Range** tab, make sure that the following two lines are configured:</span></span>

    - <span data-ttu-id="b60e6-216">Satır 1:</span><span class="sxs-lookup"><span data-stu-id="b60e6-216">Line 1:</span></span>

        - <span data-ttu-id="b60e6-217">**Tablo:** *Yerleşimler*</span><span class="sxs-lookup"><span data-stu-id="b60e6-217">**Table:** *Locations*</span></span>
        - <span data-ttu-id="b60e6-218">**Türetilmiş Tablo:** *Yerleşimler*</span><span class="sxs-lookup"><span data-stu-id="b60e6-218">**Derived Table:** *Locations*</span></span>
        - <span data-ttu-id="b60e6-219">**Alan:** *Ambar*</span><span class="sxs-lookup"><span data-stu-id="b60e6-219">**Field:** *Warehouse*</span></span>
        - <span data-ttu-id="b60e6-220">**Ölçüt:** *51*</span><span class="sxs-lookup"><span data-stu-id="b60e6-220">**Criteria:** *51*</span></span>

    - <span data-ttu-id="b60e6-221">Satır 2:</span><span class="sxs-lookup"><span data-stu-id="b60e6-221">Line 2:</span></span>

        - <span data-ttu-id="b60e6-222">**Tablo:** *Yerleşimler*</span><span class="sxs-lookup"><span data-stu-id="b60e6-222">**Table:** *Locations*</span></span>
        - <span data-ttu-id="b60e6-223">**Türetilmiş Tablo:** *Yerleşimler*</span><span class="sxs-lookup"><span data-stu-id="b60e6-223">**Derived Table:** *Locations*</span></span>
        - <span data-ttu-id="b60e6-224">**Alan:** *Yerleşim*</span><span class="sxs-lookup"><span data-stu-id="b60e6-224">**Field:** *Location*</span></span>
        - <span data-ttu-id="b60e6-225">**Ölçüt:** *Baydoor*</span><span class="sxs-lookup"><span data-stu-id="b60e6-225">**Criteria:** *Baydoor*</span></span>

1. <span data-ttu-id="b60e6-226">Sorgu düzenleyicisini kapatmak için **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="b60e6-226">Select **OK** to close the query editor.</span></span>

### <a name="create-a-mobile-device-menu-item"></a><span data-ttu-id="b60e6-227">Mobil cihaz menü öğesi oluşturma</span><span class="sxs-lookup"><span data-stu-id="b60e6-227">Create a mobile device menu item</span></span>

1. <span data-ttu-id="b60e6-228">**Ambar yönetimi \> Kurulum \> Mobil cihaz \> Mobil cihaz menüsü öğeleri**'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="b60e6-228">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu items**.</span></span>
1. <span data-ttu-id="b60e6-229">Sol bölmedeki menü öğeleri listesinde, **Satınalma yerine koyma**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="b60e6-229">In the list of menu items in the left pane, select **Purchase Put-away**.</span></span>
1. <span data-ttu-id="b60e6-230">**Düzenle** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="b60e6-230">Select **Edit**.</span></span>
1. <span data-ttu-id="b60e6-231">**İş sınıfları** hızlı sekmesinde, kılavuza satır eklemek için **Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="b60e6-231">On the **Work classes** FastTab, select **New** to add a line to the grid.</span></span>
1. <span data-ttu-id="b60e6-232">Yeni satırda aşağıdaki değerleri ayarlayın:</span><span class="sxs-lookup"><span data-stu-id="b60e6-232">On the new line, set the following values:</span></span>

    - <span data-ttu-id="b60e6-233">**İş sınıfı kodu:** *CrossDock*</span><span class="sxs-lookup"><span data-stu-id="b60e6-233">**Work class ID:** *CrossDock*</span></span>
    - <span data-ttu-id="b60e6-234">**İş emri türü:** *Çapraz sevk*</span><span class="sxs-lookup"><span data-stu-id="b60e6-234">**Work order type:** *Cross docking*</span></span>

1. <span data-ttu-id="b60e6-235">**Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="b60e6-235">Select **Save**.</span></span>

## <a name="scenario"></a><span data-ttu-id="b60e6-236">Senaryo</span><span class="sxs-lookup"><span data-stu-id="b60e6-236">Scenario</span></span>

### <a name="create-a-purchase-order"></a><span data-ttu-id="b60e6-237">Satınalma siparişi oluşturma</span><span class="sxs-lookup"><span data-stu-id="b60e6-237">Create a purchase order</span></span>

<span data-ttu-id="b60e6-238">Tedarik kaynağı olarak bir satınalma siparişi oluşturmak için bu adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="b60e6-238">Follow these steps to create a purchase order as a source of supply.</span></span>

1. <span data-ttu-id="b60e6-239">**Tedarik ve kaynak atama \> Satınalma siparişleri \> Tüm satınalma siparişleri**'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="b60e6-239">Go to **Procurement and sourcing \> Purchase orders \> All purchase orders**.</span></span>
1. <span data-ttu-id="b60e6-240">Eylem Bölmesinde, **Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="b60e6-240">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="b60e6-241">**Satın alma siparişi oluştur** iletişim kutusunda, aşağıdaki değerleri ayarlayın:</span><span class="sxs-lookup"><span data-stu-id="b60e6-241">In the **Create purchase order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="b60e6-242">**Satıcı hesabı:** *104*</span><span class="sxs-lookup"><span data-stu-id="b60e6-242">**Vendor account:** *104*</span></span>
    - <span data-ttu-id="b60e6-243">**Ambar:** *51*</span><span class="sxs-lookup"><span data-stu-id="b60e6-243">**Warehouse:** *51*</span></span>

1. <span data-ttu-id="b60e6-244">**Tamam**'ı seçin ve sipariş numarasını not alın.</span><span class="sxs-lookup"><span data-stu-id="b60e6-244">Select **OK**, and make a note of the order number.</span></span>
1. <span data-ttu-id="b60e6-245">**Satınalma siparişi satırları** hızlı sekmesine yeni bir satır eklenir.</span><span class="sxs-lookup"><span data-stu-id="b60e6-245">A new line is added to the **Purchase order lines** FastTab.</span></span> <span data-ttu-id="b60e6-246">Bu satır için aşağıdaki değerleri ayarlayın:</span><span class="sxs-lookup"><span data-stu-id="b60e6-246">On this line, set the following values:</span></span>

    - <span data-ttu-id="b60e6-247">**Madde numarası:** *A0001*</span><span class="sxs-lookup"><span data-stu-id="b60e6-247">**Item number:** *A0001*</span></span>
    - <span data-ttu-id="b60e6-248">**Miktar:** *5*</span><span class="sxs-lookup"><span data-stu-id="b60e6-248">**Quantity:** *5*</span></span>

### <a name="create-a-sales-order"></a><span data-ttu-id="b60e6-249">Satış siparişi oluştur</span><span class="sxs-lookup"><span data-stu-id="b60e6-249">Create a sales order</span></span>

<span data-ttu-id="b60e6-250">Talep kaynağı olarak bir satış siparişi oluşturmak için bu adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="b60e6-250">Follow these steps to create a sales order as a source of demand.</span></span>

1. <span data-ttu-id="b60e6-251">**Satış ve pazarlama \> Satış siparişleri \> Tüm satış siparişleri**'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="b60e6-251">Go to **Sales and marketing \> Sales orders \> All sales orders**.</span></span>
1. <span data-ttu-id="b60e6-252">Eylem Bölmesinde, **Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="b60e6-252">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="b60e6-253">**Satış siparişi oluştur** iletişim kutusunda, aşağıdaki değerleri ayarlayın:</span><span class="sxs-lookup"><span data-stu-id="b60e6-253">In the **Create sales order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="b60e6-254">**Müşteri hesabı:** *US-002*</span><span class="sxs-lookup"><span data-stu-id="b60e6-254">**Customer account:** *US-002*</span></span>
    - <span data-ttu-id="b60e6-255">**Ambar:** *51*</span><span class="sxs-lookup"><span data-stu-id="b60e6-255">**Warehouse:** *51*</span></span>

1. <span data-ttu-id="b60e6-256">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="b60e6-256">Select **OK**.</span></span>
1. <span data-ttu-id="b60e6-257">**Satış siparişi satırları** hızlı sekmesine yeni bir satır eklenir.</span><span class="sxs-lookup"><span data-stu-id="b60e6-257">A new line is added to the **Sales order lines** FastTab.</span></span> <span data-ttu-id="b60e6-258">Bu satır için aşağıdaki değerleri ayarlayın:</span><span class="sxs-lookup"><span data-stu-id="b60e6-258">On this line, set the following values:</span></span>

    - <span data-ttu-id="b60e6-259">**Madde numarası:** *A0001*</span><span class="sxs-lookup"><span data-stu-id="b60e6-259">**Item number:** *A0001*</span></span>
    - <span data-ttu-id="b60e6-260">**Miktar:** *3*</span><span class="sxs-lookup"><span data-stu-id="b60e6-260">**Quantity:** *3*</span></span>

### <a name="create-planned-cross-docking"></a><span data-ttu-id="b60e6-261">Planlanmış çapraz sevk oluşturma</span><span class="sxs-lookup"><span data-stu-id="b60e6-261">Create planned cross-docking</span></span>

<span data-ttu-id="b60e6-262">Planlanmış çapraz sevki satış siparişinden oluşturmak için bu adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="b60e6-262">Follow these steps to create the planned cross-docking from the sales order.</span></span>

1. <span data-ttu-id="b60e6-263">Az önce oluşturduğunuz satış siparişinin **Satış siparişi ayrıntıları** sayfasında, eylem bölmesindeki **Ambar** sekmesinde, **Eylemler** grubunda **Ambara serbest bırak**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="b60e6-263">In the **Sales order details** page for the sales order that you just created, on the Action Pane, on the **Warehouse** tab, in the **Actions** group, select **Release to warehouse**.</span></span>

    <span data-ttu-id="b60e6-264">Ambara serbest bırakma eylemi, satış siparişi satırı için bir sevkiyat ve yükleme satırı oluşturur ve stok tahsis etmeye çalışır.</span><span class="sxs-lookup"><span data-stu-id="b60e6-264">The release to warehouse action creates a shipment and load line for the sales order line, and tries to allocate inventory.</span></span>
    
    <span data-ttu-id="b60e6-265">Bir bilgi iletisi alırsınız.</span><span class="sxs-lookup"><span data-stu-id="b60e6-265">You receive an informational message.</span></span> <span data-ttu-id="b60e6-266">Ayrıca şu uyarı iletisini alırsınız: "Dalga XXXX için iş oluşturulmadı.</span><span class="sxs-lookup"><span data-stu-id="b60e6-266">You also receive the following warning message: "No work was created for wave XXXX.</span></span> <span data-ttu-id="b60e6-267">Ayrıntılar için iş oluşturma geçmişi günlüğüne bakın."</span><span class="sxs-lookup"><span data-stu-id="b60e6-267">See the work creation history log for details."</span></span> <span data-ttu-id="b60e6-268">Ambarda stok bulunmadığı için bu davranış olağandır.</span><span class="sxs-lookup"><span data-stu-id="b60e6-268">This behavior is expected, because there is no inventory in the warehouse.</span></span>

1. <span data-ttu-id="b60e6-269">**Satış siparişi satırları** hızlı sekmesinde **Ambar** menüsünde **Sevkiyat ayrıntıları**'nı seçin.</span><span class="sxs-lookup"><span data-stu-id="b60e6-269">On the **Sales order lines** FastTab, on the **Warehouse** menu, select **Shipment details**.</span></span>

    <span data-ttu-id="b60e6-270">**Sevkiyat ayrıntıları** sayfası görüntülenir ve satış siparişi için oluşturulan sevkiyatı gösterir.</span><span class="sxs-lookup"><span data-stu-id="b60e6-270">The **Shipment details** page appears and shows the shipment that was created for the sales order.</span></span>

1. <span data-ttu-id="b60e6-271">**Yük satırları** hızlı sekmesinde, **Planlanmış çapraz sevk miktarı** alanının *3* olarak ayarlandığına dikkat edin.</span><span class="sxs-lookup"><span data-stu-id="b60e6-271">On the **Load lines** FastTab, notice that the **Planned cross docking quantity** field is set to *3*.</span></span> <span data-ttu-id="b60e6-272">Ambarda stok mevcut olmadığı halde çapraz sevk şablonunda tanımlanan zaman aralığında geçerli tedarik kaynağı geleceği için, çapraz sevk miktarı oluşturulmuştur.</span><span class="sxs-lookup"><span data-stu-id="b60e6-272">Because no inventory was available in the warehouse, but a valid supply source will arrive within the time window that is defined in the cross-docking template, the cross-docking quantity was created.</span></span>
1. <span data-ttu-id="b60e6-273">**Yük satırları** hızlı sekmesinde, oluşturulan çapraz sevkin ayrıntılarını görüntülemek için **Planlanmış çapraz sevk**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="b60e6-273">On the **Load lines** FastTab, select **Planned cross docking** to view the details of the cross-docking that was created.</span></span>

## <a name="process-the-cross-docking"></a><span data-ttu-id="b60e6-274">Çapraz sevki işleme</span><span class="sxs-lookup"><span data-stu-id="b60e6-274">Process the cross-docking</span></span>

### <a name="purchase-order-receiving-on-the-warehousing-mobile-app"></a><span data-ttu-id="b60e6-275">Ambarlama mobil uygulamasında satınalma siparişini teslim alma</span><span class="sxs-lookup"><span data-stu-id="b60e6-275">Purchase order receiving on the warehousing mobile app</span></span>

<span data-ttu-id="b60e6-276">Sistem, satınalma siparişindeki 5 miktarını teslim alma yerleşimine alır ve iki iş parçası oluşturur.</span><span class="sxs-lookup"><span data-stu-id="b60e6-276">The system will receive the quantity of 5 from the purchase order into the receiving location and create two pieces of work.</span></span>

<span data-ttu-id="b60e6-277">Oluşturulan ilk iş kodunun **İş emri türü** değeri *Çapraz sevk*'tir ve satış siparişine bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="b60e6-277">The first work ID that is created has a **Work order type** value of *Cross docking* and is linked to the sales order.</span></span> <span data-ttu-id="b60e6-278">Miktar değeri 3'tür ve hemen sevk edilebilmesi için son sevkiyat yerleşimine yönlendirilir.</span><span class="sxs-lookup"><span data-stu-id="b60e6-278">It has a quantity of 3 and is directed to the final shipping location so that it can be shipped out immediately.</span></span>

<span data-ttu-id="b60e6-279">Oluşturulan ikinci iş kodunun **İş emri türü** değeri *Satınalma siparişleri*'dir ve satınalma siparişine bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="b60e6-279">The second work ID that is created has a **Work order type** value of *Purchase orders* and is linked to the purchase order.</span></span> <span data-ttu-id="b60e6-280">Kalan miktarı 2 olan bu parça çapraz sevk edilmemiştir ve depoda yerine koymaya yönlendirilir.</span><span class="sxs-lookup"><span data-stu-id="b60e6-280">It has the remaining quantity of 2 that wasn't cross-docked and is directed to put-away to storage.</span></span>

1. <span data-ttu-id="b60e6-281">Mobil cihazda *51* kodlu ambarda bir kullanıcı olarak oturum açın.</span><span class="sxs-lookup"><span data-stu-id="b60e6-281">Sign in to the mobile device as a user in warehouse *51*.</span></span>
1. <span data-ttu-id="b60e6-282">**Gelen \> Satınalma Teslim Alma**'ya gidin.</span><span class="sxs-lookup"><span data-stu-id="b60e6-282">Go to **Inbound \> Purchase Receive**.</span></span>
1. <span data-ttu-id="b60e6-283">**PONum** alanına satınalma sipariş numaranızı girin.</span><span class="sxs-lookup"><span data-stu-id="b60e6-283">In the **PONum** field, enter your purchase order number.</span></span>
1. <span data-ttu-id="b60e6-284">**Miktar** alanına *5* girin.</span><span class="sxs-lookup"><span data-stu-id="b60e6-284">In the **Qty** field, enter *5*.</span></span>
1. <span data-ttu-id="b60e6-285">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="b60e6-285">Select **OK**.</span></span>
1. <span data-ttu-id="b60e6-286">Sonraki sayfada, **Madde** alanını *A0001* olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="b60e6-286">On the next page, set the **Item** field to *A0001*.</span></span>
1. <span data-ttu-id="b60e6-287">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="b60e6-287">Select **OK**.</span></span>
1. <span data-ttu-id="b60e6-288">Sonraki sayfada, **Tamam**'ı seçerek **PONum**, **Madde** ve **Miktar** değerlerini onaylayın.</span><span class="sxs-lookup"><span data-stu-id="b60e6-288">On the next page, confirm the **PONum**, **Item**, and **Qty** values by selecting **OK**.</span></span>

    <span data-ttu-id="b60e6-289">Bir "İş Tamamlandı" iletisi alırsınız.</span><span class="sxs-lookup"><span data-stu-id="b60e6-289">You receive a "Work Completed" message.</span></span>

1. <span data-ttu-id="b60e6-290">Çıkmak için **İptal**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="b60e6-290">Select **Cancel** to exit.</span></span>

### <a name="put-away-to-cross-docking-and-bulk"></a><span data-ttu-id="b60e6-291">Çapraz sevk ve toplu işlem için yerine koyma</span><span class="sxs-lookup"><span data-stu-id="b60e6-291">Put-away to cross-docking and bulk</span></span>

<span data-ttu-id="b60e6-292">Şu anda her iki iş kodunun da hedef plakası aynıdır.</span><span class="sxs-lookup"><span data-stu-id="b60e6-292">Currently, both work IDs have the same target license plate.</span></span> <span data-ttu-id="b60e6-293">Sonraki adımları tamamlamak için iş kodunu ve hedef plaka kodunu almanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="b60e6-293">To complete the next steps, you must get the work ID and the target license plate ID.</span></span> <span data-ttu-id="b60e6-294">Bu bilgileri satınalma siparişi satırı ve satış siparişi satırı ile ilgili iş ayrıntılardan edinebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="b60e6-294">You can get this information from the work details for the purchase order line and the sales order line.</span></span> <span data-ttu-id="b60e6-295">Alternatif olarak, **Ambar yönetimi \> İş \> İş ayrıntıları**'na gidip **Ambar** değerinin *51* olduğu işi filtreleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="b60e6-295">Alternately, you can go to **Warehouse management \> Work \> Work details** and filter for work where the **Warehouse** value is *51*.</span></span>

1. <span data-ttu-id="b60e6-296">Mobil cihazda **Gelen \> Satın alma yerine koyma**'ya gidin ve işin hedef plakasını girin.</span><span class="sxs-lookup"><span data-stu-id="b60e6-296">On the mobile device, go to **Inbound \> Purchase put-away**, and enter the target license plate from the work.</span></span>
1. <span data-ttu-id="b60e6-297">**Kod** alanına, iş ayrıntılarından alınan hedef plaka kodunu girin.</span><span class="sxs-lookup"><span data-stu-id="b60e6-297">In the **ID** field, enter the target license plate ID from the work details.</span></span>

    <span data-ttu-id="b60e6-298">Çapraz sevk çekme sayfası, malzeme çekme yerleşimini (*RECV*), hedef plakayı ( *plaka*), maddeyi (*A0001*) ve miktarı ( *3*) gösterir.</span><span class="sxs-lookup"><span data-stu-id="b60e6-298">The cross-docking pick page shows the picking location (*RECV*), target license plate (*license plate*), item (*A0001*), and quantity (*3*).</span></span>

1. <span data-ttu-id="b60e6-299">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="b60e6-299">Select **OK**.</span></span>
1. <span data-ttu-id="b60e6-300">**Hedef Plaka** alanına, sevkiyat yerleşimine yerleştirilmesi (çapraz sevk edilmesi) gereken plaka kodu için bir hedef plaka girin.</span><span class="sxs-lookup"><span data-stu-id="b60e6-300">In the **Target LP** field, enter a target license plate for the license plate ID that should be put (cross-docked) to the shipping location.</span></span> <span data-ttu-id="b60e6-301">İstediğiniz herhangi bir plaka kodunu seçebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="b60e6-301">You can select any license plate ID of your choice.</span></span>
1. <span data-ttu-id="b60e6-302">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="b60e6-302">Select **OK**.</span></span>
1. <span data-ttu-id="b60e6-303">Sonraki sayfada, **Kod** alanına, hedef plaka kodunu girin.</span><span class="sxs-lookup"><span data-stu-id="b60e6-303">On the next page, in the **ID** field, enter the target license plate ID.</span></span>
1. <span data-ttu-id="b60e6-304">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="b60e6-304">Select **OK**.</span></span>
1. <span data-ttu-id="b60e6-305">Kalan 2 miktarını çekmek için işi onaylayın ve **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="b60e6-305">Confirm the work for picking the remaining quantity of 2, and then select **OK**.</span></span>
1. <span data-ttu-id="b60e6-306">Sonraki sayfada, malzeme çekme işlemini bitirmek ve yerine koyma işlemine başlamak için **Bitti**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="b60e6-306">On the next page, select **Done** to end the picking process and begin the put-away process.</span></span>

    <span data-ttu-id="b60e6-307">Mobil uygulama, size, maddenin yerleştirileceği yerleşimi ve plakayı verir.</span><span class="sxs-lookup"><span data-stu-id="b60e6-307">The mobile app presents you with the location and license plate to put the item to.</span></span>

1. <span data-ttu-id="b60e6-308">**Tamam**'ı seçerek toplu depolama **Koyma** işlemini onaylayın.</span><span class="sxs-lookup"><span data-stu-id="b60e6-308">Confirm the bulk storage **Put** by selecting **OK**.</span></span>
1. <span data-ttu-id="b60e6-309">Sonraki sayfada, **Tamam**'ı seçerek çapraz sevk **Koyma** işlemini onaylayın.</span><span class="sxs-lookup"><span data-stu-id="b60e6-309">On the next page, confirm the cross-docking **Put** by selecting **OK**.</span></span>

    <span data-ttu-id="b60e6-310">Bir "İş Tamamlandı" iletisi alırsınız.</span><span class="sxs-lookup"><span data-stu-id="b60e6-310">You receive a "Work Completed" message.</span></span>

1. <span data-ttu-id="b60e6-311">Çıkmak için **İptal**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="b60e6-311">Select **Cancel** to exit.</span></span>

<span data-ttu-id="b60e6-312">Aşağıdaki şekil, tamamlanmış çapraz sevk işinin Microsoft Dynamics 365 Supply Chain Management'ta nasıl görünebileceğini gösteriyor.</span><span class="sxs-lookup"><span data-stu-id="b60e6-312">The following illustration shows how the completed cross-docking work might appear in Microsoft Dynamics 365 Supply Chain Management.</span></span>

<span data-ttu-id="b60e6-313">![Tamamlanmış çapraz sevk işi](media/PlannedCrossDockingWork.png "Tamamlanmış çapraz sevk işi")</span><span class="sxs-lookup"><span data-stu-id="b60e6-313">![Cross-docking work completed](media/PlannedCrossDockingWork.png "Cross-docking work completed")</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]