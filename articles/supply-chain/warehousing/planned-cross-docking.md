---
title: Planlanmış çapraz sevk
description: Bu konuda, bir sipariş için gereken stok miktarının kabulden veya oluşturma aşamasından doğru çıkış noktasına veya hazırlama alanına kadar yönlendirildiği, ileri düzeyde planlanmış çapraz sevk açıklanmaktadır. Gelen kaynaktan kalan tüm stok, normal yerine koyma işlemiyle doğru depolama yerleşimine yönlendirilir.
author: Mirzaab
manager: tfehr
ms.date: 07/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSCrossDockingTemplate, WHSLoadPostMethod, WHSWorkClass, WHSWorkTemplateTable, WHSLocDirTable, WHSPlannedCrossDocking
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-01
ms.dyn365.ops.version: Release 10.0.7
ms.openlocfilehash: cc217f21a5fa70feb9ef9161f3ef2e2b6a333f35
ms.sourcegitcommit: 827d77c638555396b32d36af5d22d1b61dafb0e8
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4439698"
---
# <a name="planned-cross-docking"></a><span data-ttu-id="63db5-104">Planlanmış çapraz sevk</span><span class="sxs-lookup"><span data-stu-id="63db5-104">Planned cross-docking</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="63db5-105">Bu konuda, ileri düzeyde planlı çapraz sevk açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="63db5-105">This topic describes advanced planned cross-docking.</span></span> <span data-ttu-id="63db5-106">Çapraz sevk, bir sipariş için gereken stok miktarının kabulden veya oluşturma aşamasından doğru çıkış noktasına veya hazırlama alanına kadar yönlendirildiği bir ambar sürecidir.</span><span class="sxs-lookup"><span data-stu-id="63db5-106">Cross-docking is a warehouse process where the inventory quantity that is required for an order is directed straight from receipt or creation to the correct outbound dock or staging area.</span></span> <span data-ttu-id="63db5-107">Gelen kaynaktan kalan tüm stok, normal yerine koyma işlemiyle doğru depolama yerleşimine yönlendirilir.</span><span class="sxs-lookup"><span data-stu-id="63db5-107">All remaining inventory from the inbound source is directed to the correct storage location through the regular put-away process.</span></span>

<span data-ttu-id="63db5-108">Çapraz sevk, çalışanların zaten bir giden sipariş için işaretlenmiş olan stokun gelen yerine koyma ve giden çekme işlemini atlamasını sağlar.</span><span class="sxs-lookup"><span data-stu-id="63db5-108">Cross-docking lets workers skip inbound put-away and outbound picking of inventory that is already marked for an outbound order.</span></span> <span data-ttu-id="63db5-109">Bu sayede stok işlem sayısı olabildiğince azaltılır.</span><span class="sxs-lookup"><span data-stu-id="63db5-109">Therefore, the number of times that inventory is touched is minimized, where possible.</span></span> <span data-ttu-id="63db5-110">Ek olarak, sistemle daha az etkileşim olduğu için, ambardaki zaman ve alan tasarrufları artar.</span><span class="sxs-lookup"><span data-stu-id="63db5-110">Additionally, because there is less interaction with the system, time and space savings on the warehouse shop floor are increased.</span></span>

<span data-ttu-id="63db5-111">Çapraz sevkin çalıştırılabilmesi için, kullanıcının tedarik kaynağının ve çapraz sevke ilişkin diğer gereksinimler dizisinin belirtildiği yeni bir çapraz sevk şablonu yapılandırması gerekir.</span><span class="sxs-lookup"><span data-stu-id="63db5-111">Before cross-docking can be run, the user must configure a new cross-docking template, where the supply source and other sets of requirements for cross-docking are specified.</span></span> <span data-ttu-id="63db5-112">Giden sipariş oluşturulurken, satır, aynı maddeyi içeren bir gelen siparişe göre işaretlenmelidir.</span><span class="sxs-lookup"><span data-stu-id="63db5-112">As the outbound order is created, the line must be marked against an inbound order that contains the same item.</span></span>

<span data-ttu-id="63db5-113">Her gelen sipariş alındığında, çapraz sevk kurulumu çapraz sevk gereksinimini otomatik olarak belirler ve yerleşim yönergesinin kurulumuna göre, gereken miktar için hareket işini oluşturur.</span><span class="sxs-lookup"><span data-stu-id="63db5-113">At the time of inbound order receiving, the cross-docking setup automatically identifies the need for cross-docking and creates the movement work for the required quantity, based on the setup of the location directive.</span></span>

> [!NOTE]
> <span data-ttu-id="63db5-114">Bu becerinin ayarı Ambar yönetimi parametrelerinde açık olsa bile, çapraz sevk işi iptal edildiği zaman stok hareketlerinin **kaydı silinmez**.</span><span class="sxs-lookup"><span data-stu-id="63db5-114">Inventory transactions are **not** unregistered when crossing-dock work is canceled, even if the setting for this capability is turned on in Warehouse management parameters.</span></span>

## <a name="turn-on-the-planned-cross-docking-feature"></a><span data-ttu-id="63db5-115">Planlanmış çapraz sevk özelliğini açın</span><span class="sxs-lookup"><span data-stu-id="63db5-115">Turn on the Planned cross docking feature</span></span>

<span data-ttu-id="63db5-116">İleri düzeyde planlanmış çapraz sevki kullanabilmeniz için özelliğin sisteminizde etkinleştirilmesi gerekir.</span><span class="sxs-lookup"><span data-stu-id="63db5-116">Before you can use advanced planned cross-docking, the feature must be turned on in your system.</span></span> <span data-ttu-id="63db5-117">Yöneticiler özellik durumunu denetlemek ve gerekirse etkinleştirmek için [özellik yönetimi](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) çalışma alanını kullanabilir.</span><span class="sxs-lookup"><span data-stu-id="63db5-117">Admins can use the [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) workspace to check the status of the feature and turn it on if it's required.</span></span> <span data-ttu-id="63db5-118">Burada, özellik aşağıdaki şekilde listelenmiştir:</span><span class="sxs-lookup"><span data-stu-id="63db5-118">There, the feature is listed in the following way:</span></span>

- <span data-ttu-id="63db5-119">**Modül:** *Ambar yönetimi*</span><span class="sxs-lookup"><span data-stu-id="63db5-119">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="63db5-120">**Özellik adı:** *Planlanmış çapraz sevk*</span><span class="sxs-lookup"><span data-stu-id="63db5-120">**Feature name:** *Planned cross docking*</span></span>

## <a name="setup"></a><span data-ttu-id="63db5-121">Ayar</span><span class="sxs-lookup"><span data-stu-id="63db5-121">Setup</span></span>

### <a name="regenerate-load-posting-methods"></a><span data-ttu-id="63db5-122">Yükleme deftere nakil yöntemlerini yeniden oluşturma</span><span class="sxs-lookup"><span data-stu-id="63db5-122">Regenerate load posting methods</span></span>

<span data-ttu-id="63db5-123">Planlanmış çapraz sevk, bir yükleme deftere nakil yöntemi olarak uygulanır.</span><span class="sxs-lookup"><span data-stu-id="63db5-123">Planned cross-docking is implemented as a load posting method.</span></span> <span data-ttu-id="63db5-124">Özelliği açtıktan sonra, yöntemleri yeniden oluşturmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="63db5-124">After you turn on the feature, you must regenerate the methods.</span></span>

1. <span data-ttu-id="63db5-125">**Ambar yönetimi \> Kurulum \> Yükleme deftere nakil yöntemleri**'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="63db5-125">Go to **Warehouse management \> Setup \> Load posting methods**.</span></span>
1. <span data-ttu-id="63db5-126">Eylem bölmesinde, **Yöntemleri yeniden oluştur**'u seçin.</span><span class="sxs-lookup"><span data-stu-id="63db5-126">On the Action Pane, select **Regenerate methods**.</span></span>

    <span data-ttu-id="63db5-127">Yeniden oluşturma işlemi tamamlanınca **Yöntem adı** değeri *planCcrossDocking* olan bir yöntem göreceksiniz.</span><span class="sxs-lookup"><span data-stu-id="63db5-127">When regeneration is completed, you should see a method that has a **Method name** value of *planCrossDocking*.</span></span>

1. <span data-ttu-id="63db5-128">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="63db5-128">Close the page.</span></span>

### <a name="create-a-cross-docking-template"></a><span data-ttu-id="63db5-129">Bir çapraz sevk şablonu oluşturma</span><span class="sxs-lookup"><span data-stu-id="63db5-129">Create a cross-docking template</span></span>

1. <span data-ttu-id="63db5-130">**Ambar yönetimi \> Kurulum \> İş \> Çapraz sevk şablonları**'na gidin.</span><span class="sxs-lookup"><span data-stu-id="63db5-130">Go to **Warehouse management \> Setup \> Work \> Cross docking templates**.</span></span>
1. <span data-ttu-id="63db5-131">Eylem bölmesinde, bir şablon oluşturmak için **Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="63db5-131">On the Action Pane, select **New** to create a template.</span></span>
1. <span data-ttu-id="63db5-132">Üst bilgide aşağıdaki değerleri ayarlayın:</span><span class="sxs-lookup"><span data-stu-id="63db5-132">In the header, set the following values:</span></span>

    - <span data-ttu-id="63db5-133">**Sıra:** *1*</span><span class="sxs-lookup"><span data-stu-id="63db5-133">**Sequence:** *1*</span></span>

        <span data-ttu-id="63db5-134">Bu alan, şablonların değerlendirildiği sırayı tanımlar.</span><span class="sxs-lookup"><span data-stu-id="63db5-134">This field defines the order that templates are evaluated in.</span></span>

    - <span data-ttu-id="63db5-135">**Çapraz sevk şablonu kodu:** *51*</span><span class="sxs-lookup"><span data-stu-id="63db5-135">**Cross docking template ID:** *51*</span></span>
    - <span data-ttu-id="63db5-136">**Açıklama:** *Ambar 51*</span><span class="sxs-lookup"><span data-stu-id="63db5-136">**Description:** *Warehouse 51*</span></span>
    - <span data-ttu-id="63db5-137">**Talep serbest bırakma ilkesi:** *Tedarik girişinden önce*</span><span class="sxs-lookup"><span data-stu-id="63db5-137">**Demand release policy:** *Before supply receipt*</span></span>
    - <span data-ttu-id="63db5-138">**Ambar:** *51*</span><span class="sxs-lookup"><span data-stu-id="63db5-138">**Warehouse:** *51*</span></span>

1. <span data-ttu-id="63db5-139">**Planlama** hızlı sekmesindeki kurulum, şablonun nasıl çalıştığını denetler.</span><span class="sxs-lookup"><span data-stu-id="63db5-139">The setup on the **Planning** FastTab controls how the template works.</span></span> <span data-ttu-id="63db5-140">Aşağıdaki değerleri ayarlayın:</span><span class="sxs-lookup"><span data-stu-id="63db5-140">Set the following values:</span></span>

    - <span data-ttu-id="63db5-141">**Talep gereksinimleri:** *Yok*</span><span class="sxs-lookup"><span data-stu-id="63db5-141">**Demand requirements:** *None*</span></span>

        <span data-ttu-id="63db5-142">Bu alan talep stoku gereksinimlerini tanımlar.</span><span class="sxs-lookup"><span data-stu-id="63db5-142">This field defines the requirements of the demand inventory.</span></span> <span data-ttu-id="63db5-143">Talebin serbest bırakmadan önce tedarikle bağlantılı olması gerekiyorsa *İşaretleme*'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="63db5-143">If the demand must be linked to the supply before release, select *Marking*.</span></span> <span data-ttu-id="63db5-144">Talebin serbest bırakmadan önce tedarike göre sipariş rezervasyonunun yapılması gerekiyorsa *Sipariş rezervasyonu*'nu seçin.</span><span class="sxs-lookup"><span data-stu-id="63db5-144">If the demand must be order-reserved against the supply before release, select *Order reservation*.</span></span>

    - <span data-ttu-id="63db5-145">**Bulma türü:** *Sevkiyat yerleşimleri*</span><span class="sxs-lookup"><span data-stu-id="63db5-145">**Locating type:** *Shipment locations*</span></span>

        <span data-ttu-id="63db5-146">Bu alan, çapraz sevk işinin sevk irsaliyesindeki hazırlama/yükleme yerleşimlerini kullanıp kullanmayacağını veya kendi hazırlama/yükleme yerleşimlerini bulmak için yerleşim yönergeleri kullanıp kullanmayacağını tanımlar.</span><span class="sxs-lookup"><span data-stu-id="63db5-146">This field defines whether the cross-docking work should use the staging/load locations from the shipment, or whether it should use location directives to find its own staging/load locations.</span></span>

    - <span data-ttu-id="63db5-147">**İş şablonu:** Bu alanı boş bırakın.</span><span class="sxs-lookup"><span data-stu-id="63db5-147">**Work template:** Leave this field blank.</span></span>

        <span data-ttu-id="63db5-148">Bu alan, çapraz sevk işi oluşturulduğunda kullanılması gereken iş şablonunu tanımlar.</span><span class="sxs-lookup"><span data-stu-id="63db5-148">This field defines the work template that should be used when cross-docking work is created.</span></span>

    - <span data-ttu-id="63db5-149">**Tedarik girişinde yeniden doğrula:** *Hayır*</span><span class="sxs-lookup"><span data-stu-id="63db5-149">**Revalidate on supply receipt:** *No*</span></span>

        <span data-ttu-id="63db5-150">Bu seçenek, tedarik girişi sırasında tedarikin yeniden doğrulanıp doğrulanmayacağını tanımlar.</span><span class="sxs-lookup"><span data-stu-id="63db5-150">This option defines whether the supply should be revalidated during receipt.</span></span> <span data-ttu-id="63db5-151">Bu seçenek *Evet* olarak ayarlanırsa , maksimum zaman aralığı ve sona erme gün sayısı aralığı da işaretlenir.</span><span class="sxs-lookup"><span data-stu-id="63db5-151">If this option is set to *Yes*, both the maximum time window and the expiration days range are checked.</span></span>

    - <span data-ttu-id="63db5-152">**Zaman aralığını doğrula:** *Evet*</span><span class="sxs-lookup"><span data-stu-id="63db5-152">**Validate time window:** *Yes*</span></span>

        <span data-ttu-id="63db5-153">Bu seçenek, bir tedarik kaynağı seçildiğinde maksimum zaman aralığının değerlendirilip değerlendirilmeyeceğini tanımlar.</span><span class="sxs-lookup"><span data-stu-id="63db5-153">This option defines whether the maximum time window should be evaluated when a supply source is selected.</span></span> <span data-ttu-id="63db5-154">Bu seçenek *Evet* olarak ayarlanırsa, maksimum ve minimum zaman aralıklarıyla ilgili alanlar kullanılabilir duruma gelir.</span><span class="sxs-lookup"><span data-stu-id="63db5-154">If this option is set to *Yes*, the fields that are related to the maximum and minimum time windows become available.</span></span>

    - <span data-ttu-id="63db5-155">**Maksimum zaman aralığı:** *5*</span><span class="sxs-lookup"><span data-stu-id="63db5-155">**Maximum time window:** *5*</span></span>

        <span data-ttu-id="63db5-156">Bu alan, tedarik varışı ve talep çıkışı arasında izin verilen maksimum süreyi tanımlar.</span><span class="sxs-lookup"><span data-stu-id="63db5-156">This field defines the maximum period that is allowed between supply arrival and demand departure.</span></span>

    - <span data-ttu-id="63db5-157">**Maksimum zaman aralığı birimi:** *Gün sayısı*</span><span class="sxs-lookup"><span data-stu-id="63db5-157">**Maximum time window unit:** *Days*</span></span>
    - <span data-ttu-id="63db5-158">**Minimum zaman aralığı:** *0*</span><span class="sxs-lookup"><span data-stu-id="63db5-158">**Minimum time window:** *0*</span></span>

        <span data-ttu-id="63db5-159">Bu alan, tedarik varışı ve talep çıkışı arasında izin verilen minimum süreyi tanımlar.</span><span class="sxs-lookup"><span data-stu-id="63db5-159">This field defines the minimum period that is allowed between supply arrival and demand departure.</span></span>

    - <span data-ttu-id="63db5-160">**Minimum zaman aralığı birimi:** *Gün sayısı*</span><span class="sxs-lookup"><span data-stu-id="63db5-160">**Minimum time window unit:** *Days*</span></span>
    - <span data-ttu-id="63db5-161">**Sona erme gün sayısı aralığı:** *0*</span><span class="sxs-lookup"><span data-stu-id="63db5-161">**Expiration days range:** *0*</span></span>

        <span data-ttu-id="63db5-162">*İlk sona eren ilk çıkar (FEFO) ölçütleri:* Bu alan, ambardaki mevcut ilk sona eren toplu işlemin bitiş tarihi ve alınmakta olan toplu işlem arasındaki maksimum gün sayısını tanımlar.</span><span class="sxs-lookup"><span data-stu-id="63db5-162">*First expiry first out (FEFO) criteria:* This field defines the maximum number of days between the expiration date of the first-expiring batch that is currently in the warehouse and the batch that is being received.</span></span>

1. <span data-ttu-id="63db5-163">**Tedarik kaynakları** hızlı sekmesinde, bu şablon için geçerli olan tedarik tiplerini belirtirsiniz.</span><span class="sxs-lookup"><span data-stu-id="63db5-163">On the **Supply sources** FastTab, you specify the types of supply that are valid for this template.</span></span> <span data-ttu-id="63db5-164">**Yeni**'yi seçin ve aşağıdaki değerleri ayarlayın:</span><span class="sxs-lookup"><span data-stu-id="63db5-164">Select **New**, and then set the following values:</span></span>

    - <span data-ttu-id="63db5-165">**Sıra numarası:** *1*</span><span class="sxs-lookup"><span data-stu-id="63db5-165">**Sequence number:** *1*</span></span>
    - <span data-ttu-id="63db5-166">**Tedarik kaynağı:** *Satınalma siparişi*</span><span class="sxs-lookup"><span data-stu-id="63db5-166">**Supply source:** *Purchase order*</span></span>

### <a name="create-a-work-class"></a><span data-ttu-id="63db5-167">İş sınıfı oluşturma</span><span class="sxs-lookup"><span data-stu-id="63db5-167">Create a work class</span></span>

1. <span data-ttu-id="63db5-168">**Ambar yönetimi \> Kurulum \> İş \> İş sınıfları** seçeneğine gidin.</span><span class="sxs-lookup"><span data-stu-id="63db5-168">Go to **Warehouse management \> Setup \> Work \> Work classes**.</span></span>
1. <span data-ttu-id="63db5-169">Eylem bölmesinde, bir iş sınıfı oluşturmak için **Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="63db5-169">On the Action Pane, select **New** to create a work class.</span></span>
1. <span data-ttu-id="63db5-170">Aşağıdaki değerleri ayarlayın:</span><span class="sxs-lookup"><span data-stu-id="63db5-170">Set the following values:</span></span>

    - <span data-ttu-id="63db5-171">**İş sınıfı kodu:** *CrossDock*</span><span class="sxs-lookup"><span data-stu-id="63db5-171">**Work class ID:** *CrossDock*</span></span>
    - <span data-ttu-id="63db5-172">**Açıklama:** *Çapraz Sevk*</span><span class="sxs-lookup"><span data-stu-id="63db5-172">**Description:** *Cross Dock*</span></span>
    - <span data-ttu-id="63db5-173">**İş emri türü:** *Çapraz sevk*</span><span class="sxs-lookup"><span data-stu-id="63db5-173">**Work order type:** *Cross docking*</span></span>

### <a name="create-a-work-template"></a><span data-ttu-id="63db5-174">İş şablonu oluşturma</span><span class="sxs-lookup"><span data-stu-id="63db5-174">Create a work template</span></span>

1. <span data-ttu-id="63db5-175">**Ambar yönetimi \> Kurulum \> İş \> İş şablonları**'na gidin.</span><span class="sxs-lookup"><span data-stu-id="63db5-175">Go to **Warehouse management \> Setup \> Work \> Work templates**.</span></span>
1. <span data-ttu-id="63db5-176">**İş emri türü** alanını *Çapraz sevk* olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="63db5-176">Set the **Work order type** field to *Cross docking*.</span></span>
1. <span data-ttu-id="63db5-177">Eylem bölmesinde, **Genel bakış** sekmesine satır eklemek için **Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="63db5-177">On the Action Pane, select **New** to add a line to the **Overview** tab.</span></span>
1. <span data-ttu-id="63db5-178">Yeni satırda aşağıdaki değerleri ayarlayın:</span><span class="sxs-lookup"><span data-stu-id="63db5-178">On the new line, set the following values:</span></span>

    - <span data-ttu-id="63db5-179">**Sıra numarası:** *1*</span><span class="sxs-lookup"><span data-stu-id="63db5-179">**Sequence number:** *1*</span></span>
    - <span data-ttu-id="63db5-180">**İş şablonu:** *51 Çapraz Sevk*</span><span class="sxs-lookup"><span data-stu-id="63db5-180">**Work template:** *51 Cross Dock*</span></span>
    - <span data-ttu-id="63db5-181">**İş şablonu açıklaması:** *51 Çapraz Sevk*</span><span class="sxs-lookup"><span data-stu-id="63db5-181">**Work template description:** *51 Cross Dock*</span></span>

1. <span data-ttu-id="63db5-182">**İş Şablonu Ayrıntıları** hızlı sekmesini kullanılabilir hale getirmek için **Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="63db5-182">Select **Save** to make the **Work Template Details** FastTab available.</span></span>
1. <span data-ttu-id="63db5-183">**İş Şablonu Ayrıntıları** hızlı sekmesinde, kılavuza satır için **Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="63db5-183">On the **Work Template Details** FastTab, select **New** to add a line to the grid.</span></span>
1. <span data-ttu-id="63db5-184">Yeni satırda aşağıdaki değerleri ayarlayın:</span><span class="sxs-lookup"><span data-stu-id="63db5-184">On the new line, set the following values:</span></span>

    - <span data-ttu-id="63db5-185">**İş türü:** *Çekme*</span><span class="sxs-lookup"><span data-stu-id="63db5-185">**Work type:** *Pick*</span></span>
    - <span data-ttu-id="63db5-186">**İş sınıfı kodu:** *CrossDock*</span><span class="sxs-lookup"><span data-stu-id="63db5-186">**Work class ID:** *CrossDock*</span></span>

1. <span data-ttu-id="63db5-187">**Yeni**'yi seçerek bir satır daha ekleyin ve üzerinde aşağıdaki değerleri ayarlayın:</span><span class="sxs-lookup"><span data-stu-id="63db5-187">Select **New** to add another line, and set the following values on it:</span></span>

    - <span data-ttu-id="63db5-188">**İş türü:** *Yerine koyma*</span><span class="sxs-lookup"><span data-stu-id="63db5-188">**Work type:** *Put*</span></span>
    - <span data-ttu-id="63db5-189">**İş sınıfı kodu:** *CrossDock*</span><span class="sxs-lookup"><span data-stu-id="63db5-189">**Work class ID:** *CrossDock*</span></span>

1. <span data-ttu-id="63db5-190">**Kaydet**'i seçin ve *51 Çapraz Sevk* şablonu için **Geçerli** onay kutusunun işaretlendiğini onaylayın.</span><span class="sxs-lookup"><span data-stu-id="63db5-190">Select **Save**, and confirm that the **Valid** check box is selected for the *51 Cross Dock* template.</span></span>

> [!NOTE]
> <span data-ttu-id="63db5-191">*Çekme* ve *Koyma* iş türleri için iş sınıfı kodları aynı olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="63db5-191">The work class IDs for the *Pick* and *Put* work types must be the same.</span></span>

### <a name="create-location-directives"></a><span data-ttu-id="63db5-192">Yerleşim yönergeleri oluşturma</span><span class="sxs-lookup"><span data-stu-id="63db5-192">Create location directives</span></span>

1. <span data-ttu-id="63db5-193">**Ambar Yönetimi \> Kurulum \> Konum yönergeleri** seçeneğine gidin.</span><span class="sxs-lookup"><span data-stu-id="63db5-193">Go to **Warehouse management \> Setup \> Location directives**.</span></span>
1. <span data-ttu-id="63db5-194">Sol bölmede, **İş emri türü** alanını *Çapraz sevk* olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="63db5-194">In the left pane, set the **Work order type** field to *Cross docking*.</span></span>
1. <span data-ttu-id="63db5-195">Eylem bölmesinde **Yeni**'yi seçin ve aşağıdaki değerleri ayarlayın:</span><span class="sxs-lookup"><span data-stu-id="63db5-195">On the Action Pane, select **New**, and set the following values:</span></span>

    - <span data-ttu-id="63db5-196">**Sıra numarası:** *1*</span><span class="sxs-lookup"><span data-stu-id="63db5-196">**Sequence number:** *1*</span></span>
    - <span data-ttu-id="63db5-197">**Ad:** *51 Çapraz Sevk Koyma*</span><span class="sxs-lookup"><span data-stu-id="63db5-197">**Name:** *51 Cross Dock Put*</span></span>
    - <span data-ttu-id="63db5-198">**İş türü:** *Yerine koyma*</span><span class="sxs-lookup"><span data-stu-id="63db5-198">**Work type:** *Put*</span></span>
    - <span data-ttu-id="63db5-199">**Tesis:** *5*</span><span class="sxs-lookup"><span data-stu-id="63db5-199">**Site:** *5*</span></span>
    - <span data-ttu-id="63db5-200">**Ambar:** *51*</span><span class="sxs-lookup"><span data-stu-id="63db5-200">**Warehouse:** *51*</span></span>

1. <span data-ttu-id="63db5-201">**Satırlar** hızlı sekmesini kullanılabilir hale getirmek için **Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="63db5-201">Select **Save** to make the **Lines** FastTab available.</span></span>
1. <span data-ttu-id="63db5-202">**Satırlar** hızlı sekmesinde, kılavuza satır eklemek için **Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="63db5-202">On the **Lines** FastTab, select **New** to add a line to the grid.</span></span>
1. <span data-ttu-id="63db5-203">Yeni satırda aşağıdaki değerleri ayarlayın:</span><span class="sxs-lookup"><span data-stu-id="63db5-203">On the new line, set the following values:</span></span>

    - <span data-ttu-id="63db5-204">**Başlangıç miktarı:** *1*</span><span class="sxs-lookup"><span data-stu-id="63db5-204">**From quantity:** *1*</span></span>
    - <span data-ttu-id="63db5-205">**Son miktar:** *1000000*</span><span class="sxs-lookup"><span data-stu-id="63db5-205">**To quantity:** *1,000,000*</span></span>

1. <span data-ttu-id="63db5-206">**Yerleşim Yönergesi Eylemleri** hızlı sekmesini kullanılabilir hale getirmek için **Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="63db5-206">Select **Save** to make the **Location Directive Actions** FastTab available.</span></span>
1. <span data-ttu-id="63db5-207">**Konum Yönerge Eylemleri** hızlı sekmesinde, kılavuza satır eklemek için **Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="63db5-207">On the **Location Directive Actions** FastTab, select **New** to add a line to the grid.</span></span>
1. <span data-ttu-id="63db5-208">Yeni satırda aşağıdaki değerleri ayarlayın:</span><span class="sxs-lookup"><span data-stu-id="63db5-208">On the new line, set the following values:</span></span>

    - <span data-ttu-id="63db5-209">**Ad:** *Baydoor*</span><span class="sxs-lookup"><span data-stu-id="63db5-209">**Name:** *Baydoor*</span></span>
    - <span data-ttu-id="63db5-210">**Sabit yerleşim kullanımı:** *Sabit ve sabit olmayan yerleşimler*</span><span class="sxs-lookup"><span data-stu-id="63db5-210">**Fixed location usage:** *Fixed and non-fixed locations*</span></span>

1. <span data-ttu-id="63db5-211">**Yerleşim Yönergesi Eylemleri** araç çubuğunda **Sorguyu düzenle** düğmesini kullanılabilir hale getirmek için **Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="63db5-211">Select **Save** to make the **Edit query** button on the **Location Directive Actions** toolbar available.</span></span>
1. <span data-ttu-id="63db5-212">Sorgu düzenleyicisini açmak için **Sorguyu düzenle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="63db5-212">Select **Edit query** to open the query editor.</span></span>
1. <span data-ttu-id="63db5-213">**Aralık** sekmesinde, aşağıdaki iki satırın yapılandırıldığından emin olun:</span><span class="sxs-lookup"><span data-stu-id="63db5-213">On the **Range** tab, make sure that the following two lines are configured:</span></span>

    - <span data-ttu-id="63db5-214">Satır 1:</span><span class="sxs-lookup"><span data-stu-id="63db5-214">Line 1:</span></span>

        - <span data-ttu-id="63db5-215">**Tablo:** *Yerleşimler*</span><span class="sxs-lookup"><span data-stu-id="63db5-215">**Table:** *Locations*</span></span>
        - <span data-ttu-id="63db5-216">**Türetilmiş Tablo:** *Yerleşimler*</span><span class="sxs-lookup"><span data-stu-id="63db5-216">**Derived Table:** *Locations*</span></span>
        - <span data-ttu-id="63db5-217">**Alan:** *Ambar*</span><span class="sxs-lookup"><span data-stu-id="63db5-217">**Field:** *Warehouse*</span></span>
        - <span data-ttu-id="63db5-218">**Ölçüt:** *51*</span><span class="sxs-lookup"><span data-stu-id="63db5-218">**Criteria:** *51*</span></span>

    - <span data-ttu-id="63db5-219">Satır 2:</span><span class="sxs-lookup"><span data-stu-id="63db5-219">Line 2:</span></span>

        - <span data-ttu-id="63db5-220">**Tablo:** *Yerleşimler*</span><span class="sxs-lookup"><span data-stu-id="63db5-220">**Table:** *Locations*</span></span>
        - <span data-ttu-id="63db5-221">**Türetilmiş Tablo:** *Yerleşimler*</span><span class="sxs-lookup"><span data-stu-id="63db5-221">**Derived Table:** *Locations*</span></span>
        - <span data-ttu-id="63db5-222">**Alan:** *Yerleşim*</span><span class="sxs-lookup"><span data-stu-id="63db5-222">**Field:** *Location*</span></span>
        - <span data-ttu-id="63db5-223">**Ölçüt:** *Baydoor*</span><span class="sxs-lookup"><span data-stu-id="63db5-223">**Criteria:** *Baydoor*</span></span>

1. <span data-ttu-id="63db5-224">Sorgu düzenleyicisini kapatmak için **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="63db5-224">Select **OK** to close the query editor.</span></span>

### <a name="create-a-mobile-device-menu-item"></a><span data-ttu-id="63db5-225">Mobil cihaz menü öğesi oluşturma</span><span class="sxs-lookup"><span data-stu-id="63db5-225">Create a mobile device menu item</span></span>

1. <span data-ttu-id="63db5-226">**Ambar yönetimi \> Kurulum \> Mobil cihaz \> Mobil cihaz menüsü öğeleri**'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="63db5-226">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu items**.</span></span>
1. <span data-ttu-id="63db5-227">Sol bölmedeki menü öğeleri listesinde, **Satınalma yerine koyma**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="63db5-227">In the list of menu items in the left pane, select **Purchase Put-away**.</span></span>
1. <span data-ttu-id="63db5-228">**Düzenle** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="63db5-228">Select **Edit**.</span></span>
1. <span data-ttu-id="63db5-229">**İş sınıfları** hızlı sekmesinde, kılavuza satır eklemek için **Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="63db5-229">On the **Work classes** FastTab, select **New** to add a line to the grid.</span></span>
1. <span data-ttu-id="63db5-230">Yeni satırda aşağıdaki değerleri ayarlayın:</span><span class="sxs-lookup"><span data-stu-id="63db5-230">On the new line, set the following values:</span></span>

    - <span data-ttu-id="63db5-231">**İş sınıfı kodu:** *CrossDock*</span><span class="sxs-lookup"><span data-stu-id="63db5-231">**Work class ID:** *CrossDock*</span></span>
    - <span data-ttu-id="63db5-232">**İş emri türü:** *Çapraz sevk*</span><span class="sxs-lookup"><span data-stu-id="63db5-232">**Work order type:** *Cross docking*</span></span>

1. <span data-ttu-id="63db5-233">**Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="63db5-233">Select **Save**.</span></span>

## <a name="scenario"></a><span data-ttu-id="63db5-234">Senaryo</span><span class="sxs-lookup"><span data-stu-id="63db5-234">Scenario</span></span>

### <a name="create-a-purchase-order"></a><span data-ttu-id="63db5-235">Satınalma siparişi oluşturma</span><span class="sxs-lookup"><span data-stu-id="63db5-235">Create a purchase order</span></span>

<span data-ttu-id="63db5-236">Tedarik kaynağı olarak bir satınalma siparişi oluşturmak için bu adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="63db5-236">Follow these steps to create a purchase order as a source of supply.</span></span>

1. <span data-ttu-id="63db5-237">**Tedarik ve kaynak atama \> Satınalma siparişleri \> Tüm satınalma siparişleri**'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="63db5-237">Go to **Procurement and sourcing \> Purchase orders \> All purchase orders**.</span></span>
1. <span data-ttu-id="63db5-238">Eylem Bölmesinde, **Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="63db5-238">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="63db5-239">**Satın alma siparişi oluştur** iletişim kutusunda, aşağıdaki değerleri ayarlayın:</span><span class="sxs-lookup"><span data-stu-id="63db5-239">In the **Create purchase order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="63db5-240">**Satıcı hesabı:** *104*</span><span class="sxs-lookup"><span data-stu-id="63db5-240">**Vendor account:** *104*</span></span>
    - <span data-ttu-id="63db5-241">**Ambar:** *51*</span><span class="sxs-lookup"><span data-stu-id="63db5-241">**Warehouse:** *51*</span></span>

1. <span data-ttu-id="63db5-242">**Tamam**'ı seçin ve sipariş numarasını not alın.</span><span class="sxs-lookup"><span data-stu-id="63db5-242">Select **OK**, and make a note of the order number.</span></span>
1. <span data-ttu-id="63db5-243">**Satınalma siparişi satırları** hızlı sekmesine yeni bir satır eklenir.</span><span class="sxs-lookup"><span data-stu-id="63db5-243">A new line is added to the **Purchase order lines** FastTab.</span></span> <span data-ttu-id="63db5-244">Bu satır için aşağıdaki değerleri ayarlayın:</span><span class="sxs-lookup"><span data-stu-id="63db5-244">On this line, set the following values:</span></span>

    - <span data-ttu-id="63db5-245">**Madde numarası:** *A0001*</span><span class="sxs-lookup"><span data-stu-id="63db5-245">**Item number:** *A0001*</span></span>
    - <span data-ttu-id="63db5-246">**Miktar:** *5*</span><span class="sxs-lookup"><span data-stu-id="63db5-246">**Quantity:** *5*</span></span>

### <a name="create-a-sales-order"></a><span data-ttu-id="63db5-247">Satış siparişi oluştur</span><span class="sxs-lookup"><span data-stu-id="63db5-247">Create a sales order</span></span>

<span data-ttu-id="63db5-248">Talep kaynağı olarak bir satış siparişi oluşturmak için bu adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="63db5-248">Follow these steps to create a sales order as a source of demand.</span></span>

1. <span data-ttu-id="63db5-249">**Satış ve pazarlama \> Satış siparişleri \> Tüm satış siparişleri**'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="63db5-249">Go to **Sales and marketing \> Sales orders \> All sales orders**.</span></span>
1. <span data-ttu-id="63db5-250">Eylem Bölmesinde, **Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="63db5-250">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="63db5-251">**Satış siparişi oluştur** iletişim kutusunda, aşağıdaki değerleri ayarlayın:</span><span class="sxs-lookup"><span data-stu-id="63db5-251">In the **Create sales order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="63db5-252">**Müşteri hesabı:** *US-002*</span><span class="sxs-lookup"><span data-stu-id="63db5-252">**Customer account:** *US-002*</span></span>
    - <span data-ttu-id="63db5-253">**Ambar:** *51*</span><span class="sxs-lookup"><span data-stu-id="63db5-253">**Warehouse:** *51*</span></span>

1. <span data-ttu-id="63db5-254">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="63db5-254">Select **OK**.</span></span>
1. <span data-ttu-id="63db5-255">**Satış siparişi satırları** hızlı sekmesine yeni bir satır eklenir.</span><span class="sxs-lookup"><span data-stu-id="63db5-255">A new line is added to the **Sales order lines** FastTab.</span></span> <span data-ttu-id="63db5-256">Bu satır için aşağıdaki değerleri ayarlayın:</span><span class="sxs-lookup"><span data-stu-id="63db5-256">On this line, set the following values:</span></span>

    - <span data-ttu-id="63db5-257">**Madde numarası:** *A0001*</span><span class="sxs-lookup"><span data-stu-id="63db5-257">**Item number:** *A0001*</span></span>
    - <span data-ttu-id="63db5-258">**Miktar:** *3*</span><span class="sxs-lookup"><span data-stu-id="63db5-258">**Quantity:** *3*</span></span>

### <a name="create-planned-cross-docking"></a><span data-ttu-id="63db5-259">Planlanmış çapraz sevk oluşturma</span><span class="sxs-lookup"><span data-stu-id="63db5-259">Create planned cross-docking</span></span>

<span data-ttu-id="63db5-260">Planlanmış çapraz sevki satış siparişinden oluşturmak için bu adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="63db5-260">Follow these steps to create the planned cross-docking from the sales order.</span></span>

1. <span data-ttu-id="63db5-261">Az önce oluşturduğunuz satış siparişinin **Satış siparişi ayrıntıları** sayfasında, eylem bölmesindeki **Ambar** sekmesinde, **Eylemler** grubunda **Ambara serbest bırak**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="63db5-261">In the **Sales order details** page for the sales order that you just created, on the Action Pane, on the **Warehouse** tab, in the **Actions** group, select **Release to warehouse**.</span></span>

    <span data-ttu-id="63db5-262">Ambara serbest bırakma eylemi, satış siparişi satırı için bir sevkiyat ve yükleme satırı oluşturur ve stok tahsis etmeye çalışır.</span><span class="sxs-lookup"><span data-stu-id="63db5-262">The release to warehouse action creates a shipment and load line for the sales order line, and tries to allocate inventory.</span></span>
    
    <span data-ttu-id="63db5-263">Bir bilgi iletisi alırsınız.</span><span class="sxs-lookup"><span data-stu-id="63db5-263">You receive an informational message.</span></span> <span data-ttu-id="63db5-264">Ayrıca şu uyarı iletisini alırsınız: "Dalga XXXX için iş oluşturulmadı.</span><span class="sxs-lookup"><span data-stu-id="63db5-264">You also receive the following warning message: "No work was created for wave XXXX.</span></span> <span data-ttu-id="63db5-265">Ayrıntılar için iş oluşturma geçmişi günlüğüne bakın."</span><span class="sxs-lookup"><span data-stu-id="63db5-265">See the work creation history log for details."</span></span> <span data-ttu-id="63db5-266">Ambarda stok bulunmadığı için bu davranış olağandır.</span><span class="sxs-lookup"><span data-stu-id="63db5-266">This behavior is expected, because there is no inventory in the warehouse.</span></span>

1. <span data-ttu-id="63db5-267">**Satış siparişi satırları** hızlı sekmesinde **Ambar** menüsünde **Sevkiyat ayrıntıları**'nı seçin.</span><span class="sxs-lookup"><span data-stu-id="63db5-267">On the **Sales order lines** FastTab, on the **Warehouse** menu, select **Shipment details**.</span></span>

    <span data-ttu-id="63db5-268">**Sevkiyat ayrıntıları** sayfası görüntülenir ve satış siparişi için oluşturulan sevkiyatı gösterir.</span><span class="sxs-lookup"><span data-stu-id="63db5-268">The **Shipment details** page appears and shows the shipment that was created for the sales order.</span></span>

1. <span data-ttu-id="63db5-269">**Yük satırları** hızlı sekmesinde, **Planlanmış çapraz sevk miktarı** alanının *3* olarak ayarlandığına dikkat edin.</span><span class="sxs-lookup"><span data-stu-id="63db5-269">On the **Load lines** FastTab, notice that the **Planned cross docking quantity** field is set to *3*.</span></span> <span data-ttu-id="63db5-270">Ambarda stok mevcut olmadığı halde çapraz sevk şablonunda tanımlanan zaman aralığında geçerli tedarik kaynağı geleceği için, çapraz sevk miktarı oluşturulmuştur.</span><span class="sxs-lookup"><span data-stu-id="63db5-270">Because no inventory was available in the warehouse, but a valid supply source will arrive within the time window that is defined in the cross-docking template, the cross-docking quantity was created.</span></span>
1. <span data-ttu-id="63db5-271">**Yük satırları** hızlı sekmesinde, oluşturulan çapraz sevkin ayrıntılarını görüntülemek için **Planlanmış çapraz sevk**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="63db5-271">On the **Load lines** FastTab, select **Planned cross docking** to view the details of the cross-docking that was created.</span></span>

## <a name="process-the-cross-docking"></a><span data-ttu-id="63db5-272">Çapraz sevki işleme</span><span class="sxs-lookup"><span data-stu-id="63db5-272">Process the cross-docking</span></span>

### <a name="purchase-order-receiving-on-the-warehousing-mobile-app"></a><span data-ttu-id="63db5-273">Ambarlama mobil uygulamasında satınalma siparişini teslim alma</span><span class="sxs-lookup"><span data-stu-id="63db5-273">Purchase order receiving on the warehousing mobile app</span></span>

<span data-ttu-id="63db5-274">Sistem, satınalma siparişindeki 5 miktarını teslim alma yerleşimine alır ve iki iş parçası oluşturur.</span><span class="sxs-lookup"><span data-stu-id="63db5-274">The system will receive the quantity of 5 from the purchase order into the receiving location and create two pieces of work.</span></span>

<span data-ttu-id="63db5-275">Oluşturulan ilk iş kodunun **İş emri türü** değeri *Çapraz sevk*'tir ve satış siparişine bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="63db5-275">The first work ID that is created has a **Work order type** value of *Cross docking* and is linked to the sales order.</span></span> <span data-ttu-id="63db5-276">Miktar değeri 3'tür ve hemen sevk edilebilmesi için son sevkiyat yerleşimine yönlendirilir.</span><span class="sxs-lookup"><span data-stu-id="63db5-276">It has a quantity of 3 and is directed to the final shipping location so that it can be shipped out immediately.</span></span>

<span data-ttu-id="63db5-277">Oluşturulan ikinci iş kodunun **İş emri türü** değeri *Satınalma siparişleri*'dir ve satınalma siparişine bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="63db5-277">The second work ID that is created has a **Work order type** value of *Purchase orders* and is linked to the purchase order.</span></span> <span data-ttu-id="63db5-278">Kalan miktarı 2 olan bu parça çapraz sevk edilmemiştir ve depoda yerine koymaya yönlendirilir.</span><span class="sxs-lookup"><span data-stu-id="63db5-278">It has the remaining quantity of 2 that wasn't cross-docked and is directed to put-away to storage.</span></span>

1. <span data-ttu-id="63db5-279">Mobil cihazda *51* kodlu ambarda bir kullanıcı olarak oturum açın.</span><span class="sxs-lookup"><span data-stu-id="63db5-279">Sign in to the mobile device as a user in warehouse *51*.</span></span>
1. <span data-ttu-id="63db5-280">**Gelen \> Satınalma Teslim Alma**'ya gidin.</span><span class="sxs-lookup"><span data-stu-id="63db5-280">Go to **Inbound \> Purchase Receive**.</span></span>
1. <span data-ttu-id="63db5-281">**PONum** alanına satınalma sipariş numaranızı girin.</span><span class="sxs-lookup"><span data-stu-id="63db5-281">In the **PONum** field, enter your purchase order number.</span></span>
1. <span data-ttu-id="63db5-282">**Miktar** alanına *5* girin.</span><span class="sxs-lookup"><span data-stu-id="63db5-282">In the **Qty** field, enter *5*.</span></span>
1. <span data-ttu-id="63db5-283">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="63db5-283">Select **OK**.</span></span>
1. <span data-ttu-id="63db5-284">Sonraki sayfada, **Madde** alanını *A0001* olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="63db5-284">On the next page, set the **Item** field to *A0001*.</span></span>
1. <span data-ttu-id="63db5-285">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="63db5-285">Select **OK**.</span></span>
1. <span data-ttu-id="63db5-286">Sonraki sayfada, **Tamam**'ı seçerek **PONum**, **Madde** ve **Miktar** değerlerini onaylayın.</span><span class="sxs-lookup"><span data-stu-id="63db5-286">On the next page, confirm the **PONum**, **Item**, and **Qty** values by selecting **OK**.</span></span>

    <span data-ttu-id="63db5-287">Bir "İş Tamamlandı" iletisi alırsınız.</span><span class="sxs-lookup"><span data-stu-id="63db5-287">You receive a "Work Completed" message.</span></span>

1. <span data-ttu-id="63db5-288">Çıkmak için **İptal**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="63db5-288">Select **Cancel** to exit.</span></span>

### <a name="put-away-to-cross-docking-and-bulk"></a><span data-ttu-id="63db5-289">Çapraz sevk ve toplu işlem için yerine koyma</span><span class="sxs-lookup"><span data-stu-id="63db5-289">Put-away to cross-docking and bulk</span></span>

<span data-ttu-id="63db5-290">Şu anda her iki iş kodunun da hedef plakası aynıdır.</span><span class="sxs-lookup"><span data-stu-id="63db5-290">Currently, both work IDs have the same target license plate.</span></span> <span data-ttu-id="63db5-291">Sonraki adımları tamamlamak için iş kodunu ve hedef plaka kodunu almanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="63db5-291">To complete the next steps, you must get the work ID and the target license plate ID.</span></span> <span data-ttu-id="63db5-292">Bu bilgileri satınalma siparişi satırı ve satış siparişi satırı ile ilgili iş ayrıntılardan edinebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="63db5-292">You can get this information from the work details for the purchase order line and the sales order line.</span></span> <span data-ttu-id="63db5-293">Alternatif olarak, **Ambar yönetimi \> İş \> İş ayrıntıları**'na gidip **Ambar** değerinin *51* olduğu işi filtreleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="63db5-293">Alternately, you can go to **Warehouse management \> Work \> Work details** and filter for work where the **Warehouse** value is *51*.</span></span>

1. <span data-ttu-id="63db5-294">Mobil cihazda **Gelen \> Satın alma yerine koyma**'ya gidin ve işin hedef plakasını girin.</span><span class="sxs-lookup"><span data-stu-id="63db5-294">On the mobile device, go to **Inbound \> Purchase put-away**, and enter the target license plate from the work.</span></span>
1. <span data-ttu-id="63db5-295">**Kod** alanına, iş ayrıntılarından alınan hedef plaka kodunu girin.</span><span class="sxs-lookup"><span data-stu-id="63db5-295">In the **ID** field, enter the target license plate ID from the work details.</span></span>

    <span data-ttu-id="63db5-296">Çapraz sevk çekme sayfası, malzeme çekme yerleşimini (*RECV*), hedef plakayı ( *plaka*), maddeyi (*A0001*) ve miktarı ( *3*) gösterir.</span><span class="sxs-lookup"><span data-stu-id="63db5-296">The cross-docking pick page shows the picking location (*RECV*), target license plate (*license plate*), item (*A0001*), and quantity (*3*).</span></span>

1. <span data-ttu-id="63db5-297">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="63db5-297">Select **OK**.</span></span>
1. <span data-ttu-id="63db5-298">**Hedef Plaka** alanına, sevkiyat yerleşimine yerleştirilmesi (çapraz sevk edilmesi) gereken plaka kodu için bir hedef plaka girin.</span><span class="sxs-lookup"><span data-stu-id="63db5-298">In the **Target LP** field, enter a target license plate for the license plate ID that should be put (cross-docked) to the shipping location.</span></span> <span data-ttu-id="63db5-299">İstediğiniz herhangi bir plaka kodunu seçebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="63db5-299">You can select any license plate ID of your choice.</span></span>
1. <span data-ttu-id="63db5-300">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="63db5-300">Select **OK**.</span></span>
1. <span data-ttu-id="63db5-301">Sonraki sayfada, **Kod** alanına, hedef plaka kodunu girin.</span><span class="sxs-lookup"><span data-stu-id="63db5-301">On the next page, in the **ID** field, enter the target license plate ID.</span></span>
1. <span data-ttu-id="63db5-302">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="63db5-302">Select **OK**.</span></span>
1. <span data-ttu-id="63db5-303">Kalan 2 miktarını çekmek için işi onaylayın ve **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="63db5-303">Confirm the work for picking the remaining quantity of 2, and then select **OK**.</span></span>
1. <span data-ttu-id="63db5-304">Sonraki sayfada, malzeme çekme işlemini bitirmek ve yerine koyma işlemine başlamak için **Bitti**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="63db5-304">On the next page, select **Done** to end the picking process and begin the put-away process.</span></span>

    <span data-ttu-id="63db5-305">Mobil uygulama, size, maddenin yerleştirileceği yerleşimi ve plakayı verir.</span><span class="sxs-lookup"><span data-stu-id="63db5-305">The mobile app presents you with the location and license plate to put the item to.</span></span>

1. <span data-ttu-id="63db5-306">**Tamam**'ı seçerek toplu depolama **Koyma** işlemini onaylayın.</span><span class="sxs-lookup"><span data-stu-id="63db5-306">Confirm the bulk storage **Put** by selecting **OK**.</span></span>
1. <span data-ttu-id="63db5-307">Sonraki sayfada, **Tamam**'ı seçerek çapraz sevk **Koyma** işlemini onaylayın.</span><span class="sxs-lookup"><span data-stu-id="63db5-307">On the next page, confirm the cross-docking **Put** by selecting **OK**.</span></span>

    <span data-ttu-id="63db5-308">Bir "İş Tamamlandı" iletisi alırsınız.</span><span class="sxs-lookup"><span data-stu-id="63db5-308">You receive a "Work Completed" message.</span></span>

1. <span data-ttu-id="63db5-309">Çıkmak için **İptal**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="63db5-309">Select **Cancel** to exit.</span></span>

<span data-ttu-id="63db5-310">Aşağıdaki şekil, tamamlanmış çapraz sevk işinin Microsoft Dynamics 365 Supply Chain Management'ta nasıl görünebileceğini gösteriyor.</span><span class="sxs-lookup"><span data-stu-id="63db5-310">The following illustration shows how the completed cross-docking work might appear in Microsoft Dynamics 365 Supply Chain Management.</span></span>

<span data-ttu-id="63db5-311">![Tamamlanmış çapraz sevk işi](media/PlannedCrossDockingWork.png "Tamamlanmış çapraz sevk işi")</span><span class="sxs-lookup"><span data-stu-id="63db5-311">![Cross-docking work completed](media/PlannedCrossDockingWork.png "Cross-docking work completed")</span></span>
