---
title: Sistemin yönlendirdiği iş sıralaması
description: Bu konu, sistemin yönlendirdiği iş sıralaması hakkında bilgi sağlar. Bu işlevsellik, sistemin yürütülmek üzere kullanıcılara sunduğu iş emirlerini sıralamanızı ve filtrelemenizi sağlar. Ambar malzeme çekme sürecini yönetmek için ek ölçütlerin gerekli olduğu senaryolarda yardımcı olur.
author: Mirzaab
manager: tfehr
ms.date: 07/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSRFSystemDirectedWorkSequenceQuery, WHSLocDirTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-03
ms.dyn365.ops.version: Release 10.0.7
ms.openlocfilehash: 86d396b069a354b8fa7e15793372a8293273d238
ms.sourcegitcommit: 827d77c638555396b32d36af5d22d1b61dafb0e8
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4439687"
---
# <a name="system-directed-work-sequencing"></a><span data-ttu-id="65262-105">Sistemin yönlendirdiği iş sıralaması</span><span class="sxs-lookup"><span data-stu-id="65262-105">System-directed work sequencing</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="65262-106">Sistemin yönlendirdiği iş sıralaması, sistemin yürütülmek üzere kullanıcılara sunduğu iş emirlerini sıralamanızı ve filtrelemenizi sağlar.</span><span class="sxs-lookup"><span data-stu-id="65262-106">System-directed work sequencing lets you sort and filter the work orders that the system presents to users for execution.</span></span> <span data-ttu-id="65262-107">Ambar malzeme çekme sürecini yönetmek için ek ölçütlerin (sevkiyat zamanı, malzeme çekme alanı, yerleşim profili veya çeşitli ölçütlerin birleşimi gibi) gerekli olduğu senaryolarda yardımcı olur.</span><span class="sxs-lookup"><span data-stu-id="65262-107">It's helpful in scenarios where additional criteria (such as the time of shipping, the picking zone, the location profile, or a combination of various criteria) are required to drive the warehouse picking process.</span></span>

<span data-ttu-id="65262-108">Bu işlevsellik, kullanıcıların oluşturulan tüm iş emirlerini değerlendirecek bir veya daha fazla sorgu ve bir sıra ayarlayabileceği, sistemin yönlendirdiği bir sorgu sırası ekleyerek, geçerli sistemin yönlendirdiği malzeme çekme işlevini genişletir.</span><span class="sxs-lookup"><span data-stu-id="65262-108">This functionality extends the current system-directed picking functionality by adding a system-directed query order, where users can set up a sequence and one or more queries that will evaluate all work orders that are created.</span></span> <span data-ttu-id="65262-109">Yalnızca mobil cihaz menü öğesinin kurulumunda belirtilen ölçütlere uyan iş emirleri yakalanıp sunulur.</span><span class="sxs-lookup"><span data-stu-id="65262-109">Only work orders that meet the criteria that are specified in the setup of the mobile device menu item will be captured and presented.</span></span>

<span data-ttu-id="65262-110">Bu nedenle, bu işlevsellik, belirtilen ölçütlere uyan iş emirlerini tanımladığı şekilde ambar çekme işlemlerinin daha iyi duruma getirilmesini sağlar, bunları doğru mobil cihaz menü öğesine atar ve sonra belirli bir beceri kümesi, malzeme çekme ekipmanı veya başka bir gereksinime göre bir çalışana sunar.</span><span class="sxs-lookup"><span data-stu-id="65262-110">Therefore, this functionality allows for further optimization of warehouse picking processes as it identifies work orders that match the specified criteria, assigns them to the correct mobile device menu item, and then presents them to a worker, based on a specific skill set, picking equipment, or other requirement.</span></span>

> [!NOTE]
> <span data-ttu-id="65262-111">Farklı ölçütler gerekiyorsa, birden çok mobil cihaz menü öğesi kullanılmalıdır.</span><span class="sxs-lookup"><span data-stu-id="65262-111">If different criteria are needed, multiple mobile device menu items must be used.</span></span>

## <a name="turn-on-the-organization-wide-system-directed-work-sequencing-feature"></a><span data-ttu-id="65262-112">Kuruluş çapında sistemin yönlendirdiği iş sıralaması özelliği</span><span class="sxs-lookup"><span data-stu-id="65262-112">Turn on the Organization-wide system directed work sequencing feature</span></span>

<span data-ttu-id="65262-113">Sistemin yönlendirdiği iş sıralamasını kullanabilmeniz için özelliğin sisteminizde etkinleştirilmesi gerekir.</span><span class="sxs-lookup"><span data-stu-id="65262-113">Before you can use system-directed work sequencing, the feature must be turned on in your system.</span></span> <span data-ttu-id="65262-114">Yöneticiler özellik durumunu denetlemek ve gerekirse etkinleştirmek için [özellik yönetimi](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) çalışma alanını kullanabilir.</span><span class="sxs-lookup"><span data-stu-id="65262-114">Admins can use the [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) workspace to check the status of the feature and turn it on if it's required.</span></span> <span data-ttu-id="65262-115">Burada, özellik aşağıdaki şekilde listelenmiştir:</span><span class="sxs-lookup"><span data-stu-id="65262-115">There, the feature is listed in the following way:</span></span>

- <span data-ttu-id="65262-116">**Modül:** *Ambar yönetimi*</span><span class="sxs-lookup"><span data-stu-id="65262-116">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="65262-117">**Özellik adı:** *Kuruluş çapında sistemin yönlendirdiği iş sıralaması*</span><span class="sxs-lookup"><span data-stu-id="65262-117">**Feature name:** *Organization-wide system directed work sequencing*</span></span>

## <a name="setup"></a><span data-ttu-id="65262-118">Ayar</span><span class="sxs-lookup"><span data-stu-id="65262-118">Setup</span></span>

### <a name="make-demo-data-available"></a><span data-ttu-id="65262-119">Tanıtım verilerini kullanılabilir hale getirme</span><span class="sxs-lookup"><span data-stu-id="65262-119">Make demo data available</span></span>

<span data-ttu-id="65262-120">Bu konu altında sunulan değerleri kullanarak bu senaryoyla çalışmak için, standart tanıtım verilerinin yüklenmiş olduğu bir sistemde çalışmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="65262-120">To work through the scenario by using the values that are presented in this topic, you must work on a system where the standard demo data is installed.</span></span> <span data-ttu-id="65262-121">Ayrıca, **USMF** hukuk varlığını seçmelisiniz.</span><span class="sxs-lookup"><span data-stu-id="65262-121">Additionally, you must select the **USMF** legal entity.</span></span> <span data-ttu-id="65262-122">Senaryo, tanıtım verilerinden ambar *51*'i kullanır.</span><span class="sxs-lookup"><span data-stu-id="65262-122">The scenario uses warehouse *51* from the demo data.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="65262-123">Siparişleri ambara serbest bırakmadan önce, çekme yerleşimlerinin siparişlerdeki tüm maddeler için yeterli stok içerdiğinden emin olun.</span><span class="sxs-lookup"><span data-stu-id="65262-123">Before you release the orders to the warehouse, make sure that the pick locations have enough inventory for all the items on the orders.</span></span>
>
> <span data-ttu-id="65262-124">Varsayılan USMF verileri bu senaryoyu desteklemelidir.</span><span class="sxs-lookup"><span data-stu-id="65262-124">Default USMF data should support this scenario.</span></span> <span data-ttu-id="65262-125">Tanıtım verilerini kullanmıyorsanız satış siparişi çekmek üzere hangi malzeme çekme konumlarının kullanıldığını öğrenmek için **Yerleşim yönergesi** ayarını inceleyin.</span><span class="sxs-lookup"><span data-stu-id="65262-125">If you aren't using demo data, review the **Location directive** setting to learn which picking locations are used for sales order picking.</span></span> <span data-ttu-id="65262-126">Stoku ayarlamanız gerekiyorsa, el ile hareketler oluşturabilir, stok yenilemeyi veya başka bir akışı kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="65262-126">If you must adjust the inventory, you can create manual movements, use replenishment, or use any other flow.</span></span>

### <a name="set-up-a-mobile-device-menu-item"></a><span data-ttu-id="65262-127">Mobil cihaz menü öğesi ayarlama</span><span class="sxs-lookup"><span data-stu-id="65262-127">Set up a mobile device menu item</span></span>

1. <span data-ttu-id="65262-128">**Ambar yönetimi \> Kurulum \> Mobil cihaz \> Mobil cihaz menüsü öğeleri**'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="65262-128">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu items**.</span></span>
1. <span data-ttu-id="65262-129">Mobil cihaz menü öğeleri listesinde **Satış Malzeme Çekme – Sistem**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="65262-129">In the list of mobile device menu items, select **Sales Picking – System**.</span></span> <span data-ttu-id="65262-130">Gerekli menü öğesi zaten mevcut olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="65262-130">The required menu item should already exist.</span></span> 
1. <span data-ttu-id="65262-131">Şu ayarları onaylayın:</span><span class="sxs-lookup"><span data-stu-id="65262-131">Confirm the following settings:</span></span>

    - <span data-ttu-id="65262-132">**Genel** hızlı sekmesinde **Yöneten** alanı *Sistem yönlendirmesinde* olarak ayarlanmalıdır.</span><span class="sxs-lookup"><span data-stu-id="65262-132">On the **General** FastTab, the **Directed by** field should be set to *System directed*.</span></span>
    - <span data-ttu-id="65262-133">**İş sınıfları** hızlı sekmesi aşağıdaki ayarları göstermelidir.</span><span class="sxs-lookup"><span data-stu-id="65262-133">The **Work classes** FastTab should show the following settings.</span></span>

        | <span data-ttu-id="65262-134">İş sınıfı kodu</span><span class="sxs-lookup"><span data-stu-id="65262-134">Work class ID</span></span> | <span data-ttu-id="65262-135">İş siparişi türü</span><span class="sxs-lookup"><span data-stu-id="65262-135">Work order type</span></span> |
        |---|---|
        | <span data-ttu-id="65262-136">Satışlar</span><span class="sxs-lookup"><span data-stu-id="65262-136">Sales</span></span> | <span data-ttu-id="65262-137">Satış siparişleri</span><span class="sxs-lookup"><span data-stu-id="65262-137">Sales orders</span></span> |
        | <span data-ttu-id="65262-138">Satış Siparişi Çekme</span><span class="sxs-lookup"><span data-stu-id="65262-138">SO Pick</span></span> | <span data-ttu-id="65262-139">Satış siparişleri</span><span class="sxs-lookup"><span data-stu-id="65262-139">Sales orders</span></span> |

1. <span data-ttu-id="65262-140">Eylem bölmesinde **Sistemin yönlendirdiği iş sıralaması sorguları**'nı seçin.</span><span class="sxs-lookup"><span data-stu-id="65262-140">On the Action Pane, select **System directed work sequence queries**.</span></span>
1. <span data-ttu-id="65262-141">**Düzenle** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="65262-141">Select **Edit**.</span></span>
1. <span data-ttu-id="65262-142">Mevcut satırı silin ve sonra **Evet**'i seçerek eylemi onaylayın.</span><span class="sxs-lookup"><span data-stu-id="65262-142">Delete the existing line, and then confirm the action by selecting **Yes**.</span></span>
1. <span data-ttu-id="65262-143">Eylem bölmesinde, bir satır oluşturmak için **Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="65262-143">On the Action Pane, select **New** to create a line.</span></span>
1. <span data-ttu-id="65262-144">Yeni satırda aşağıdaki değerleri ayarlayın:</span><span class="sxs-lookup"><span data-stu-id="65262-144">On the new line, set the following values:</span></span>

    - <span data-ttu-id="65262-145">**Sıra numarası:** *1*</span><span class="sxs-lookup"><span data-stu-id="65262-145">**Sequence number:** *1*</span></span>
    - <span data-ttu-id="65262-146">**Açıklama alanı:** *20'den az iş miktarı ve Azalan*</span><span class="sxs-lookup"><span data-stu-id="65262-146">**Description field:** *Work quantity less than 20 and Descending*</span></span>

1. <span data-ttu-id="65262-147">**Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="65262-147">Select **Save**.</span></span>
1. <span data-ttu-id="65262-148">Eylem bölmesinde **Sorgu düzenle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="65262-148">On the Action Pane, select **Edit Query**.</span></span>
1. <span data-ttu-id="65262-149">**Birleşimler** sekmesinde, **İş satırları** tablosunu göstermek için birleştirme hiyerarşisini genişletin.</span><span class="sxs-lookup"><span data-stu-id="65262-149">On the **Joins** tab, expand the join hierarchy to show the **Work lines** table.</span></span>
1. <span data-ttu-id="65262-150">**İş satırları** tablo birleşimini seçin.</span><span class="sxs-lookup"><span data-stu-id="65262-150">Select the **Work lines** table join.</span></span>
1. <span data-ttu-id="65262-151">**Tablo birleşimi ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="65262-151">Select **Add table join**.</span></span>
1. <span data-ttu-id="65262-152">Görüntülenen listede, aşağıdaki ayarlara sahip satırı bulun ve seçin:</span><span class="sxs-lookup"><span data-stu-id="65262-152">In the list that appears, find and select the row that has the following settings:</span></span>

    - <span data-ttu-id="65262-153">**Birleştirme modu:** *n:1*</span><span class="sxs-lookup"><span data-stu-id="65262-153">**Join mode:** *n:1*</span></span>
    - <span data-ttu-id="65262-154">**İlişki:** *Yerleşimler (Yerleşim)*</span><span class="sxs-lookup"><span data-stu-id="65262-154">**Relation:** *Locations (Location)*</span></span>

1. <span data-ttu-id="65262-155">**Seç** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="65262-155">Select **Select**.</span></span>

    <span data-ttu-id="65262-156">Yerleşimler tablo birleşimine eklenir.</span><span class="sxs-lookup"><span data-stu-id="65262-156">Locations are added to the table join.</span></span>

1. <span data-ttu-id="65262-157">**Sıralama** sekmesinde, satır eklemek için **Ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="65262-157">On the **Sorting** tab, select **Add** to add a line.</span></span>
1. <span data-ttu-id="65262-158">Yeni satırda aşağıdaki değerleri ayarlayın:</span><span class="sxs-lookup"><span data-stu-id="65262-158">On the new line, set the following values:</span></span>

    - <span data-ttu-id="65262-159">**Tablo:** *İş satırları*</span><span class="sxs-lookup"><span data-stu-id="65262-159">**Table:** *Work lines*</span></span>
    - <span data-ttu-id="65262-160">**Türetilen tablo:** *İş satırları*</span><span class="sxs-lookup"><span data-stu-id="65262-160">**Derived table:** *Work lines*</span></span>
    - <span data-ttu-id="65262-161">**Alan:** *İş miktarı* (Görünen ileti kutusunda, bu alana göre sıralama eklemek için **Evet**'i seçin.)</span><span class="sxs-lookup"><span data-stu-id="65262-161">**Field:** *Work quantity* (In the message box that appears, select **Yes** to add sorting to this field.)</span></span>
    - <span data-ttu-id="65262-162">**Arama yönü:** *Azalan*</span><span class="sxs-lookup"><span data-stu-id="65262-162">**Search direction:** *Descending*</span></span>

1. <span data-ttu-id="65262-163">**Aralık** sekmesini seçin.</span><span class="sxs-lookup"><span data-stu-id="65262-163">Select the **Range** tab.</span></span>

    <span data-ttu-id="65262-164">Sıralamaya yalnızca belirli iş ölçütlerinin dahil edilmesi gerekiyorsa bunları **Aralık** sekmesinde belirtebilirsiniz. Bu örnekte, yalnızca miktarın 20 beher'den (en düşük ölçü birimi) az olduğu işleri dahil etmek istiyorsunuz.</span><span class="sxs-lookup"><span data-stu-id="65262-164">If only specific work criteria should be included in the sequencing, you can specify them on the **Range** tab. In this example, you want to include only work where the quantity is less than 20 ea (the lowest unit of measure).</span></span>

    <span data-ttu-id="65262-165">Bazı satırların zaten dahil edildiğini unutmayın.</span><span class="sxs-lookup"><span data-stu-id="65262-165">Notice that some lines are already included.</span></span> <span data-ttu-id="65262-166">Bu satırların kaldırılmaması gerekir.</span><span class="sxs-lookup"><span data-stu-id="65262-166">Those lines should not be removed.</span></span>

1. <span data-ttu-id="65262-167">Bir satır eklemek için **Ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="65262-167">Select **Add** to add a line.</span></span>
1. <span data-ttu-id="65262-168">Yeni satırda aşağıdaki değerleri ayarlayın:</span><span class="sxs-lookup"><span data-stu-id="65262-168">On the new line, set the following values:</span></span>

    - <span data-ttu-id="65262-169">**Tablo:** *İş satırları*</span><span class="sxs-lookup"><span data-stu-id="65262-169">**Table:** *Work lines*</span></span>
    - <span data-ttu-id="65262-170">**Türetilen tablo:** *İş satırları*</span><span class="sxs-lookup"><span data-stu-id="65262-170">**Derived table:** *Work lines*</span></span>
    - <span data-ttu-id="65262-171">**Alan:** *Stok iş miktarı*</span><span class="sxs-lookup"><span data-stu-id="65262-171">**Field:** *Inventory work quantity*</span></span>
    - <span data-ttu-id="65262-172">**Ölçüt:** *\<20* (20'den az)</span><span class="sxs-lookup"><span data-stu-id="65262-172">**Criteria:** *\<20* (less than 20)</span></span>

1. <span data-ttu-id="65262-173">Bir satır daha eklemek için **Ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="65262-173">Select **Add** to add another line.</span></span>
1. <span data-ttu-id="65262-174">Yeni satırda aşağıdaki değerleri ayarlayın:</span><span class="sxs-lookup"><span data-stu-id="65262-174">On the new line, set the following values:</span></span>

    - <span data-ttu-id="65262-175">**Tablo:** *İş satırları*</span><span class="sxs-lookup"><span data-stu-id="65262-175">**Table:** *Work lines*</span></span>
    - <span data-ttu-id="65262-176">**Türetilen tablo:** *İş satırları*</span><span class="sxs-lookup"><span data-stu-id="65262-176">**Derived table:** *Work lines*</span></span>
    - <span data-ttu-id="65262-177">**Alan:** *İş türü*</span><span class="sxs-lookup"><span data-stu-id="65262-177">**Field:** *Work type*</span></span>
    - <span data-ttu-id="65262-178">**Ölçüt:** *Malzeme çekme*</span><span class="sxs-lookup"><span data-stu-id="65262-178">**Criteria:** *Pick*</span></span>

1. <span data-ttu-id="65262-179">Bir satır daha eklemek için **Ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="65262-179">Select **Add** to add another line.</span></span>
1. <span data-ttu-id="65262-180">Yeni satırda aşağıdaki değerleri ayarlayın:</span><span class="sxs-lookup"><span data-stu-id="65262-180">On the new line, set the following values:</span></span>

    - <span data-ttu-id="65262-181">**Tablo:** *Yerleşimler*</span><span class="sxs-lookup"><span data-stu-id="65262-181">**Table:** *Locations*</span></span>
    - <span data-ttu-id="65262-182">**Türetilmiş tablo:** *Yerleşimler*</span><span class="sxs-lookup"><span data-stu-id="65262-182">**Derived table:** *Locations*</span></span>
    - <span data-ttu-id="65262-183">**Alan:** *Yerleşim profili kodu*</span><span class="sxs-lookup"><span data-stu-id="65262-183">**Field:** *Location profile ID*</span></span>
    - <span data-ttu-id="65262-184">**Ölçüt:** *!STAGE*</span><span class="sxs-lookup"><span data-stu-id="65262-184">**Criteria:** *!STAGE*</span></span>

        > [!IMPORTANT]
        > <span data-ttu-id="65262-185">*STAGE*'in önüne ünlem işareti (*!*) eklemeyi unutmayın.</span><span class="sxs-lookup"><span data-stu-id="65262-185">Be sure to include the exclamation point (*!*) in front of *STAGE*.</span></span>

1. <span data-ttu-id="65262-186">Sorguyu kaydedip kapatmak için **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="65262-186">Select **OK** to save and close the query.</span></span>
1. <span data-ttu-id="65262-187">**Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="65262-187">Select **Save**.</span></span>
1. <span data-ttu-id="65262-188">**Mobil cihaz menü öğeleri** sayfasına dönmek için sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="65262-188">Close the page to return to the **Mobile device menu items** page.</span></span>

> [!NOTE]
> <span data-ttu-id="65262-189">Bu kurulum, mobil cihaz menü öğesine uygun iş akışı için kullanılacak ölçütleri tanımlar.</span><span class="sxs-lookup"><span data-stu-id="65262-189">This setup defines the criteria that will be used to feed eligible work to the mobile device menu item.</span></span> <span data-ttu-id="65262-190">Sorguya başka ölçüt satırları eklerseniz, sistem ilk olarak en düşük sıra numaralı sorgu satırını kullanır.</span><span class="sxs-lookup"><span data-stu-id="65262-190">If you add more criteria lines to the query, the system will use the query line that has lowest sequence number first.</span></span> <span data-ttu-id="65262-191">Başka bir deyişle, kullanıcıya önce sıra numarası 1 için uygun olan tüm işler ve ardından 2 numaralı sıra için tüm işler sunulur.</span><span class="sxs-lookup"><span data-stu-id="65262-191">In other words, all eligible work for sequence number 1 will be presented to the user first, and then all work for sequence number 2.</span></span> <span data-ttu-id="65262-192">Bu nedenle, belirli bir aralık ve sıralamanın birlikte kullanılması gerekiyorsa, bunlar aynı sistemin yönlendirdiği iş sırası sorgusunda belirtilmelidir.</span><span class="sxs-lookup"><span data-stu-id="65262-192">Therefore, if a specific range and sorting must be used together, they should be specified in the same system-directed work sequence query.</span></span>
>
> <span data-ttu-id="65262-193">Bu kurulum, miktarın 20 beher'den az olduğu en az bir satır bulunan tüm işleri yakalar.</span><span class="sxs-lookup"><span data-stu-id="65262-193">This setup will capture any work that has at least one line where the quantity is less than 20 ea.</span></span> <span data-ttu-id="65262-194">Bu nedenle, işin, miktarı tam 20 beher veya 20 beherden fazla bir satırı varsa, bu, miktarın 20 beher'den az olduğu en az bir satırı olması koşuluyla geçerli olacaktır.</span><span class="sxs-lookup"><span data-stu-id="65262-194">Therefore, if the work has a line where the quantity is exactly 20 ea or more than 20 ea, it will be valid, provided that it also has at least one line where the quantity is less than 20 ea.</span></span>

### <a name="location-directives"></a><span data-ttu-id="65262-195">Konum yönergeleri</span><span class="sxs-lookup"><span data-stu-id="65262-195">Location directives</span></span>

<span data-ttu-id="65262-196">Varsayılan Contoso verilerini kullanıyorsanız, yerleşim yönergesi eyleminin sorgusu için değişiklik yapılması gerekmez.</span><span class="sxs-lookup"><span data-stu-id="65262-196">If you're using default Contoso data, the query for the location directive action won't require changes.</span></span> <span data-ttu-id="65262-197">Ancak, özelliği Contoso dışı bir ortama uyguladığınızda yerleşim yönergelerinin satış siparişlerindeki maddeleri yakalayacağından emin olmak için yeni bir yerleşim yönergesi oluşturun.</span><span class="sxs-lookup"><span data-stu-id="65262-197">However, to make sure that the location directives will capture the items on the sales orders when you apply the feature in a non-Contoso environment, create a new location directive.</span></span> <span data-ttu-id="65262-198">Tanıtım ortamındaki ayarları doğrulamak için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="65262-198">To verify the settings in the demo environment, follow these steps.</span></span>

1. <span data-ttu-id="65262-199">**Ambar Yönetimi** \> **Kurulum** \> **Konum yönergeleri** seçeneğine gidin.</span><span class="sxs-lookup"><span data-stu-id="65262-199">Go to **Warehouse management** \> **Setup** \> **Location directives**.</span></span>
1. <span data-ttu-id="65262-200">**İş siparişi türü** alanında *Satış siparişi*'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="65262-200">In the **Work order type** field, select *Sales orders*.</span></span>
1. <span data-ttu-id="65262-201">*51 malzeme çekme* adlı yerleşim yönergesini seçin.</span><span class="sxs-lookup"><span data-stu-id="65262-201">Select the location directive that is named *51 Pick*.</span></span>
1. <span data-ttu-id="65262-202">**Yerleşim Yönergesi Eylemleri** hızlı sekmesinde, **Çek** eyleminin satırını seçin.</span><span class="sxs-lookup"><span data-stu-id="65262-202">On the **Location Directive Actions** FastTab, select the line for the **Pick** action.</span></span>
1. <span data-ttu-id="65262-203">Kılavuzun yukarısında **Sorguyu düzenle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="65262-203">Select **Edit query** above the grid.</span></span>
1. <span data-ttu-id="65262-204">**Aralık** sorgusunu inceleyin.</span><span class="sxs-lookup"><span data-stu-id="65262-204">Review the **Range** query.</span></span>

    1. <span data-ttu-id="65262-205">**Alan** alanının *Yerleşim* olarak ayarlandığı satırı bulun.</span><span class="sxs-lookup"><span data-stu-id="65262-205">Find the line where the **Field** field is set to *Location*.</span></span>
    2. <span data-ttu-id="65262-206">**Ölçüt** alanının boş olduğundan emin olun (yani sınırlama yoktur).</span><span class="sxs-lookup"><span data-stu-id="65262-206">Make sure that the **Criteria** field is blank (that is, there are no restrictions).</span></span>

## <a name="scenario"></a><span data-ttu-id="65262-207">Senaryo</span><span class="sxs-lookup"><span data-stu-id="65262-207">Scenario</span></span>

### <a name="create-sales-order-picking-work"></a><span data-ttu-id="65262-208">Satış siparişi malzeme çekme işi oluşturma</span><span class="sxs-lookup"><span data-stu-id="65262-208">Create sales order picking work</span></span>

<span data-ttu-id="65262-209">Sistemin yönlendirdiği malzeme çekme işlemi çalıştırılmadan önce bazı giden işler oluşturulmalıdır.</span><span class="sxs-lookup"><span data-stu-id="65262-209">Before system-directed picking is run, some outbound work should be created.</span></span> <span data-ttu-id="65262-210">Bu senaryo için, belirtilen sistemin yönlendirdiği iş sırası sorgularını temel alan dört satış siparişi oluşturacaksınız.</span><span class="sxs-lookup"><span data-stu-id="65262-210">For this scenario, you will create four sales orders that are based on the specified system-directed work sequence queries.</span></span>

<span data-ttu-id="65262-211">Her satış siparişi için stok miktarlarını rezerve edeceksiniz.</span><span class="sxs-lookup"><span data-stu-id="65262-211">You will reserve inventory quantities for each sales order.</span></span> <span data-ttu-id="65262-212">Bu nedenle, stok rezervasyonu veya stok rezervasyonunun bir kısmı iptal edilmedikçe, rezerve edilen stok diğer siparişler için ambardan çekilemez.</span><span class="sxs-lookup"><span data-stu-id="65262-212">Therefore, reserved inventory can't be withdrawn from the warehouse for other orders unless the inventory reservation, or part of the inventory reservation, is canceled.</span></span>

<span data-ttu-id="65262-213">Bunun ardından, giden işi oluşturmak için her bir satış siparişini ambara serbest bırakacaksınız.</span><span class="sxs-lookup"><span data-stu-id="65262-213">You will then release each sales order to the warehouse to create the outbound work.</span></span>

#### <a name="sales-order-1"></a><span data-ttu-id="65262-214">Satış siparişi 1</span><span class="sxs-lookup"><span data-stu-id="65262-214">Sales order 1</span></span>

1. <span data-ttu-id="65262-215">**Satış ve pazarlama \> Satış siparişleri \> Tüm satış siparişleri**'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="65262-215">Go to **Sales and marketing \> Sales orders \> All sales orders**.</span></span>
1. <span data-ttu-id="65262-216">Eylem bölmesinde, satış siparişi 1'i oluşturmak için **Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="65262-216">On the Action Pane, select **New** to create sales order 1.</span></span>
1. <span data-ttu-id="65262-217">**Satış siparişi oluştur** iletişim kutusunda, aşağıdaki değerleri ayarlayın:</span><span class="sxs-lookup"><span data-stu-id="65262-217">In the **Create sales order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="65262-218">**Müşteri** bölümünde, **Müşteri hesabı** alanını *ABD-004* olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="65262-218">In the **Customer** section, set the **Customer account** field to *US-004*.</span></span>
    - <span data-ttu-id="65262-219">**Genel** bölümünde, **Ambar** alanını *51* yapın.</span><span class="sxs-lookup"><span data-stu-id="65262-219">In the **General** section, set the **Warehouse** field to *51*.</span></span>

1. <span data-ttu-id="65262-220">İletişim kutusunu kapatmak için **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="65262-220">Select **OK** to close the dialog box.</span></span> <span data-ttu-id="65262-221">Satış siparişi numarasını not edin.</span><span class="sxs-lookup"><span data-stu-id="65262-221">Make a note of the sales order number.</span></span>
1. <span data-ttu-id="65262-222">Yeni satış siparişine bir satır ekleyin ve aşağıdaki değerleri ayarlayın:</span><span class="sxs-lookup"><span data-stu-id="65262-222">Add a line to the new sales order, and set the following values:</span></span>

    - <span data-ttu-id="65262-223">**Madde numarası:** *M9200*</span><span class="sxs-lookup"><span data-stu-id="65262-223">**Item number:** *M9200*</span></span>
    - <span data-ttu-id="65262-224">**Miktar:** *20*</span><span class="sxs-lookup"><span data-stu-id="65262-224">**Quantity:** *20*</span></span>

1. <span data-ttu-id="65262-225">Kılavuzun üzerindeki **stok** menüsünde **rezervasyon**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="65262-225">On the **Inventory** menu above the grid, select **Reservation**.</span></span>
1. <span data-ttu-id="65262-226">**Rezervasyon** sayfasında stoku rezerve etmek için **Lotu rezerve et**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="65262-226">On the **Reservation** page, select **Reserve lot** to reserve the inventory.</span></span>
1. <span data-ttu-id="65262-227">**Rezervasyon** sayfasını kapatın.</span><span class="sxs-lookup"><span data-stu-id="65262-227">Close the **Reservation** page.</span></span>
1. <span data-ttu-id="65262-228">Eylem bölmesindeki **Ambar** sekmesinde **Ambara serbest bırak**'ı seçerek ambar için iş oluşturun.</span><span class="sxs-lookup"><span data-stu-id="65262-228">On the Action Pane, on the **Warehouse** tab, select **Release to warehouse** to create work for the warehouse.</span></span>

    <span data-ttu-id="65262-229">Satış siparişi için oluşturulan dalga kimliğini ve sevkiyat kimliklerini gösteren bilgi iletileri alırsınız.</span><span class="sxs-lookup"><span data-stu-id="65262-229">You receive informational messages that show the wave ID and shipment IDs that were created for the sales order.</span></span>

#### <a name="sales-order-2"></a><span data-ttu-id="65262-230">Satış siparişi 2</span><span class="sxs-lookup"><span data-stu-id="65262-230">Sales order 2</span></span>

1. <span data-ttu-id="65262-231">Eylem bölmesinde, satış siparişi 2'yi oluşturmak için **Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="65262-231">On the Action Pane, select **New** to create sales order 2.</span></span>
1. <span data-ttu-id="65262-232">**Satış siparişi oluştur** iletişim kutusunda, aşağıdaki değerleri ayarlayın:</span><span class="sxs-lookup"><span data-stu-id="65262-232">In the **Create sales order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="65262-233">**Müşteri hesabı:** *US-007*</span><span class="sxs-lookup"><span data-stu-id="65262-233">**Customer account:** *US-007*</span></span>
    - <span data-ttu-id="65262-234">**Ambar:** *51*</span><span class="sxs-lookup"><span data-stu-id="65262-234">**Warehouse:** *51*</span></span>

1. <span data-ttu-id="65262-235">İletişim kutusunu kapatmak için **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="65262-235">Select **OK** to close the dialog box.</span></span> <span data-ttu-id="65262-236">Satış siparişi numarasını not edin.</span><span class="sxs-lookup"><span data-stu-id="65262-236">Make a note of the sales order number.</span></span>
1. <span data-ttu-id="65262-237">Yeni satış siparişine bir satır ekleyin ve aşağıdaki değerleri ayarlayın:</span><span class="sxs-lookup"><span data-stu-id="65262-237">Add a line to the new sales order, and set the following values:</span></span>

    - <span data-ttu-id="65262-238">**Madde numarası:** *M9200*</span><span class="sxs-lookup"><span data-stu-id="65262-238">**Item number:** *M9200*</span></span>
    - <span data-ttu-id="65262-239">**Miktar:** *5*</span><span class="sxs-lookup"><span data-stu-id="65262-239">**Quantity:** *5*</span></span>

1. <span data-ttu-id="65262-240">**Satır ekle**'yi seçerek ikinci bir satır ekleyin ve aşağıdaki değerleri ayarlayın:</span><span class="sxs-lookup"><span data-stu-id="65262-240">Select **Add line** to add a second line, and set the following values:</span></span>

    - <span data-ttu-id="65262-241">**Madde numarası:** *M9201*</span><span class="sxs-lookup"><span data-stu-id="65262-241">**Item number:** *M9201*</span></span>
    - <span data-ttu-id="65262-242">**Miktar:** *1*</span><span class="sxs-lookup"><span data-stu-id="65262-242">**Quantity:** *1*</span></span>

1. <span data-ttu-id="65262-243">Her iki satır için stok rezerve edin.</span><span class="sxs-lookup"><span data-stu-id="65262-243">Reserve inventory for both lines.</span></span>
1. <span data-ttu-id="65262-244">Siparişi ambara serbest bırakın.</span><span class="sxs-lookup"><span data-stu-id="65262-244">Release the order to the warehouse.</span></span>

#### <a name="sales-order-3"></a><span data-ttu-id="65262-245">Satış siparişi 3</span><span class="sxs-lookup"><span data-stu-id="65262-245">Sales order 3</span></span>

1. <span data-ttu-id="65262-246">Eylem bölmesinde, satış siparişi 3'ü oluşturmak için **Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="65262-246">On the Action Pane, select **New** to create sales order 3.</span></span>
1. <span data-ttu-id="65262-247">**Satış siparişi oluştur** iletişim kutusunda, aşağıdaki değerleri ayarlayın:</span><span class="sxs-lookup"><span data-stu-id="65262-247">In the **Create sales order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="65262-248">**Müşteri hesabı:** *US-009*</span><span class="sxs-lookup"><span data-stu-id="65262-248">**Customer account:** *US-009*</span></span>
    - <span data-ttu-id="65262-249">**Ambar:** *51*</span><span class="sxs-lookup"><span data-stu-id="65262-249">**Warehouse:** *51*</span></span>

1. <span data-ttu-id="65262-250">İletişim kutusunu kapatmak için **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="65262-250">Select **OK** to close the dialog box.</span></span> <span data-ttu-id="65262-251">Satış siparişi numarasını not edin.</span><span class="sxs-lookup"><span data-stu-id="65262-251">Make a note of the sales order number.</span></span>
1. <span data-ttu-id="65262-252">Yeni satış siparişine bir satır ekleyin ve aşağıdaki değerleri ayarlayın:</span><span class="sxs-lookup"><span data-stu-id="65262-252">Add a line to the new sales order, and set the following values:</span></span>

    - <span data-ttu-id="65262-253">**Madde numarası:** *M9200*</span><span class="sxs-lookup"><span data-stu-id="65262-253">**Item number:** *M9200*</span></span>
    - <span data-ttu-id="65262-254">**Miktar:** *7*</span><span class="sxs-lookup"><span data-stu-id="65262-254">**Quantity:** *7*</span></span>

1. <span data-ttu-id="65262-255">**Satır ekle**'yi seçerek ikinci bir satır ekleyin ve aşağıdaki değerleri ayarlayın:</span><span class="sxs-lookup"><span data-stu-id="65262-255">Select **Add line** to add a second line, and set the following values:</span></span>

    - <span data-ttu-id="65262-256">**Madde numarası:** *M9202*</span><span class="sxs-lookup"><span data-stu-id="65262-256">**Item number:** *M9202*</span></span>
    - <span data-ttu-id="65262-257">**Miktar:** *8*</span><span class="sxs-lookup"><span data-stu-id="65262-257">**Quantity:** *8*</span></span>

1. <span data-ttu-id="65262-258">Her iki satır için stok rezerve edin.</span><span class="sxs-lookup"><span data-stu-id="65262-258">Reserve inventory for both lines.</span></span>
1. <span data-ttu-id="65262-259">Siparişi ambara serbest bırakın.</span><span class="sxs-lookup"><span data-stu-id="65262-259">Release the order to the warehouse.</span></span>

#### <a name="sales-order-4"></a><span data-ttu-id="65262-260">Satış siparişi 4</span><span class="sxs-lookup"><span data-stu-id="65262-260">Sales order 4</span></span>

1. <span data-ttu-id="65262-261">Eylem bölmesinde, satış siparişi 4'ü oluşturmak için **Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="65262-261">On the Action Pane, select **New** to create sales order 4.</span></span>
1. <span data-ttu-id="65262-262">**Satış siparişi oluştur** iletişim kutusunda, aşağıdaki değerleri ayarlayın:</span><span class="sxs-lookup"><span data-stu-id="65262-262">In the **Create sales order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="65262-263">**Müşteri hesabı:** *US-010*</span><span class="sxs-lookup"><span data-stu-id="65262-263">**Customer account:** *US-010*</span></span>
    - <span data-ttu-id="65262-264">**Ambar:** *51*</span><span class="sxs-lookup"><span data-stu-id="65262-264">**Warehouse:** *51*</span></span>

1. <span data-ttu-id="65262-265">İletişim kutusunu kapatmak için **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="65262-265">Select **OK** to close the dialog box.</span></span> <span data-ttu-id="65262-266">Satış siparişi numarasını not edin.</span><span class="sxs-lookup"><span data-stu-id="65262-266">Make a note of the sales order number.</span></span>
1. <span data-ttu-id="65262-267">Yeni satış siparişine bir satır ekleyin ve aşağıdaki değerleri ayarlayın:</span><span class="sxs-lookup"><span data-stu-id="65262-267">Add a line to the new sales order, and set the following values:</span></span>

    - <span data-ttu-id="65262-268">**Madde numarası:** *M9200*</span><span class="sxs-lookup"><span data-stu-id="65262-268">**Item number:** *M9200*</span></span>
    - <span data-ttu-id="65262-269">**Miktar:** *25*</span><span class="sxs-lookup"><span data-stu-id="65262-269">**Quantity:** *25*</span></span>

1. <span data-ttu-id="65262-270">**Satır ekle**'yi seçerek ikinci bir satır ekleyin ve aşağıdaki değerleri ayarlayın:</span><span class="sxs-lookup"><span data-stu-id="65262-270">Select **Add line** to add a second line, and set the following values:</span></span>

    - <span data-ttu-id="65262-271">**Madde numarası:** *M9202*</span><span class="sxs-lookup"><span data-stu-id="65262-271">**Item number:** *M9202*</span></span>
    - <span data-ttu-id="65262-272">**Miktar:** *10*</span><span class="sxs-lookup"><span data-stu-id="65262-272">**Quantity:** *10*</span></span>

1. <span data-ttu-id="65262-273">Her iki satır için stok rezerve edin.</span><span class="sxs-lookup"><span data-stu-id="65262-273">Reserve inventory for both lines.</span></span>
1. <span data-ttu-id="65262-274">Siparişi ambara serbest bırakın.</span><span class="sxs-lookup"><span data-stu-id="65262-274">Release the order to the warehouse.</span></span>

### <a name="get-work-ids-for-the-work-that-was-created"></a><span data-ttu-id="65262-275">Oluşturulan iş için iş kodlarını alma</span><span class="sxs-lookup"><span data-stu-id="65262-275">Get work IDs for the work that was created</span></span>

1. <span data-ttu-id="65262-276">**Ambar yönetimi \> İş \> İş ayrıntıları**'na gidin.</span><span class="sxs-lookup"><span data-stu-id="65262-276">Go to **Warehouse management \> Work \> Work details**.</span></span>
1. <span data-ttu-id="65262-277">Yalnızca ambar *51*'in gösterilmesi için **Ambar** alanına filtre uygulayın.</span><span class="sxs-lookup"><span data-stu-id="65262-277">Filter on the **Warehouse** field so that only work for warehouse *51* is shown.</span></span>
1. <span data-ttu-id="65262-278">Dört iş kodu oluşturulması gerekir.</span><span class="sxs-lookup"><span data-stu-id="65262-278">Four work IDs should have been created.</span></span> <span data-ttu-id="65262-279">Her satış siparişinin iş kodunu not edin.</span><span class="sxs-lookup"><span data-stu-id="65262-279">Make a note of the work ID for each sales order.</span></span>

    | <span data-ttu-id="65262-280">Satış siparişi kodu</span><span class="sxs-lookup"><span data-stu-id="65262-280">Sales order ID</span></span> | <span data-ttu-id="65262-281">İş Kodu</span><span class="sxs-lookup"><span data-stu-id="65262-281">Work ID</span></span> | <span data-ttu-id="65262-282">İş miktarı</span><span class="sxs-lookup"><span data-stu-id="65262-282">Work quantity</span></span> |
    |---|---|---|
    | <span data-ttu-id="65262-283">Satış Siparişi 1</span><span class="sxs-lookup"><span data-stu-id="65262-283">Sales Order 1</span></span> | <span data-ttu-id="65262-284">İş Kodu 1</span><span class="sxs-lookup"><span data-stu-id="65262-284">Work ID 1</span></span> | <span data-ttu-id="65262-285">20 beher</span><span class="sxs-lookup"><span data-stu-id="65262-285">20 ea</span></span> |
    | <span data-ttu-id="65262-286">Satış Siparişi 2</span><span class="sxs-lookup"><span data-stu-id="65262-286">Sales Order 2</span></span> | <span data-ttu-id="65262-287">İş Kodu 2</span><span class="sxs-lookup"><span data-stu-id="65262-287">Work ID 2</span></span> | <span data-ttu-id="65262-288">6 beher (her iki satırın toplamı)</span><span class="sxs-lookup"><span data-stu-id="65262-288">6 ea (sum of both lines)</span></span> |
    | <span data-ttu-id="65262-289">Satış Siparişi 3</span><span class="sxs-lookup"><span data-stu-id="65262-289">Sales Order 3</span></span> | <span data-ttu-id="65262-290">İş Kodu 3</span><span class="sxs-lookup"><span data-stu-id="65262-290">Work ID 3</span></span> | <span data-ttu-id="65262-291">15 beher (her iki satırın toplamı)</span><span class="sxs-lookup"><span data-stu-id="65262-291">15 ea (sum of both lines)</span></span> |
    | <span data-ttu-id="65262-292">Satış Siparişi 4</span><span class="sxs-lookup"><span data-stu-id="65262-292">Sales Order 4</span></span> | <span data-ttu-id="65262-293">İş Kodu 4</span><span class="sxs-lookup"><span data-stu-id="65262-293">Work ID 4</span></span> | <span data-ttu-id="65262-294">35 beher (her iki satırın toplamı)</span><span class="sxs-lookup"><span data-stu-id="65262-294">35 ea (sum of both lines)</span></span> |

<span data-ttu-id="65262-295">Akışı mobil cihazda çalıştırmadan önce, yalnızca yeni oluşturduğunuz işin ambar *51* için *Açık* durumda ve iş emri türünün *Satış siparişi* olduğundan emin olun.</span><span class="sxs-lookup"><span data-stu-id="65262-295">Before you run the flow on the mobile device, make sure that only the work that you just created is in *Open* status for warehouse *51* and the *Sales order* work order type.</span></span> <span data-ttu-id="65262-296">Aksi takdirde, sistem-doğrudan malzeme çekme işlemi tüm uygun işleri içereceği için, testin sonuçları farklılık gösterebilir.</span><span class="sxs-lookup"><span data-stu-id="65262-296">Otherwise, the results of the test might vary, because the system-direct picking will include all eligible work.</span></span>

1. <span data-ttu-id="65262-297">**Ambar yönetimi \> İş \> Giden \> Açık satış işi**'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="65262-297">Go to **Warehouse management \> Work \> Outbound \> Open sales work**.</span></span>
1. <span data-ttu-id="65262-298">**Açık satış işi** kılavuzunda, yalnızca ambar *51* için işin gösterilmesi için **Ambar** alanına filtre uygulayın.</span><span class="sxs-lookup"><span data-stu-id="65262-298">In the **Open sales work** grid, filter on the **Warehouse** field so that only work for warehouse *51* is shown.</span></span>
1. <span data-ttu-id="65262-299">Yalnızca daha önce oluşturduğunuz dört iş kodunun gösterildiğini onaylayın.</span><span class="sxs-lookup"><span data-stu-id="65262-299">Confirm that only the four work IDs that you created earlier are shown.</span></span>
1. <span data-ttu-id="65262-300">**İş** sayfasını kapatın.</span><span class="sxs-lookup"><span data-stu-id="65262-300">Close the **Work** page.</span></span>

### <a name="mobile-device-flow-execution"></a><span data-ttu-id="65262-301">Mobil cihaz akışını yürütme</span><span class="sxs-lookup"><span data-stu-id="65262-301">Mobile device flow execution</span></span>

<span data-ttu-id="65262-302">Kuruluma bağlı olarak, sistem, en yüksek iş satırı miktarından en düşük miktara sıralanan kullanıcı işini akışa alır.</span><span class="sxs-lookup"><span data-stu-id="65262-302">Based on the setup, the system will feed the user work that is sorted from the highest work line quantity to the lowest.</span></span> <span data-ttu-id="65262-303">Her satırdaki miktar 20 beher'den az olacaktır.</span><span class="sxs-lookup"><span data-stu-id="65262-303">The quantity on every line will be less than 20 ea.</span></span>

<span data-ttu-id="65262-304">Bu kurulumun, miktarın 20 beher'den az olduğu en az bir satır bulunan tüm işleri yakalayacağını unutmayın.</span><span class="sxs-lookup"><span data-stu-id="65262-304">Remember that this setup will capture any work that has at least one line where the quantity is less than 20 ea.</span></span> <span data-ttu-id="65262-305">Bu nedenle, işte miktarı tam 20 beher veya 20 beher'den fazla başka bir satır varsa, o da geçerli olur.</span><span class="sxs-lookup"><span data-stu-id="65262-305">Therefore, if the work has another line where the quantity is exactly 20 ea or more than 20 ea, it will also be valid.</span></span>

#### <a name="mobile-app"></a><span data-ttu-id="65262-306">Mobil uygulama</span><span class="sxs-lookup"><span data-stu-id="65262-306">Mobile app</span></span>

1. <span data-ttu-id="65262-307">Ambar uygulamasında ambar *51*'deki bir kullanıcı olarak oturum açın.</span><span class="sxs-lookup"><span data-stu-id="65262-307">Sign in to the warehousing app as a user in warehouse *51*.</span></span>
1. <span data-ttu-id="65262-308">**Giden \> Satış Malzeme Çekme - Sistem**'e gidin.</span><span class="sxs-lookup"><span data-stu-id="65262-308">Go to **Outbound \> Sales Picking - System**.</span></span>

    <span data-ttu-id="65262-309">İş kodu *4* için malzeme çekme adımı sunulur.</span><span class="sxs-lookup"><span data-stu-id="65262-309">The pick step for work ID *4* is presented.</span></span> <span data-ttu-id="65262-310">Sistemin yönlendirdiği sorgu siparişinin kurulumunda işin azalan iş satırı miktarına göre sıralanacağını belirttiğiniz için ilk olarak bu iş kodu sunulur.</span><span class="sxs-lookup"><span data-stu-id="65262-310">This work ID is presented first because of the setup of the system-directed query order, where you specified that work should be sequenced based on descending work line quantity.</span></span>

1. <span data-ttu-id="65262-311">Gerekli çekme işlemini tamamlayın ve iş kodunu kapanışa sokun.</span><span class="sxs-lookup"><span data-stu-id="65262-311">Complete the required pick and put to close the work ID.</span></span>

    <span data-ttu-id="65262-312">Bunun ardından iş kodu *3* sunulur.</span><span class="sxs-lookup"><span data-stu-id="65262-312">Next, work ID *3* is presented.</span></span> <span data-ttu-id="65262-313">İş satırlarından biri, iş satırı miktarına göre sırada sonraki öğe olarak yer alır.</span><span class="sxs-lookup"><span data-stu-id="65262-313">One of its work lines is next in the sequence, based on the work line quantity.</span></span>

1. <span data-ttu-id="65262-314">Çekme işlemini tamamlayın ve iş kodunu kapanışa sokun.</span><span class="sxs-lookup"><span data-stu-id="65262-314">Complete the pick and put to close the work ID.</span></span>

    <span data-ttu-id="65262-315">Bunun ardından iş kodu *2* sunulur.</span><span class="sxs-lookup"><span data-stu-id="65262-315">Next, work ID *2* is presented.</span></span> <span data-ttu-id="65262-316">Bu çalışmanın çekme satırı sırada sonraki öğedir.</span><span class="sxs-lookup"><span data-stu-id="65262-316">This work's pick line is next in the sequence.</span></span>

1. <span data-ttu-id="65262-317">Çekme işlemini tamamlayın ve iş kodunu kapanışa sokun.</span><span class="sxs-lookup"><span data-stu-id="65262-317">Complete the pick and put to close the work ID.</span></span>

    <span data-ttu-id="65262-318">Size artık başka iş sunulmaz.</span><span class="sxs-lookup"><span data-stu-id="65262-318">No further work should be presented to you.</span></span> <span data-ttu-id="65262-319">İş kodu *1* bu mobil cihaz menü öğesi için uygun değildir çünkü sorgu iş başlıklarının yalnızca iş satırlarındaki miktar 20 beher'den az olduğu zaman değerlendirileceğini belirtmektedir.</span><span class="sxs-lookup"><span data-stu-id="65262-319">Work ID *1* isn't eligible for this mobile device menu item, because the query specifies that work headers are considered only if the quantity on the work lines is less than 20 ea.</span></span>

## <a name="tips"></a><span data-ttu-id="65262-320">İpuçları</span><span class="sxs-lookup"><span data-stu-id="65262-320">Tips</span></span>

<span data-ttu-id="65262-321">Sistemin yönlendirdiği iş sırası sorguları *dahildir*.</span><span class="sxs-lookup"><span data-stu-id="65262-321">The system-directed work sequence queries are *inclusive*.</span></span> <span data-ttu-id="65262-322">Bu olguyu bazı kurulumlar için hatırlamanız önemlidir.</span><span class="sxs-lookup"><span data-stu-id="65262-322">It's important that you remember this fact for some setups.</span></span> <span data-ttu-id="65262-323">Örneğin, belirli bir menü öğesinin yalnızca iş biriminin *beher* olduğu işleri işlemesini istiyor ve sorgunun **Aralık** sekmesinde bu kısıtlamayı belirtiyorsunuz.</span><span class="sxs-lookup"><span data-stu-id="65262-323">For example, you want a specific menu item to process only work where the work unit is *ea*, and you specify that restriction on the **Range** tab of the query.</span></span> <span data-ttu-id="65262-324">Bu durumda, en az bir iş satırının iş birimi *beher* olarak ayarlandığı tüm işler çalışana sunulur.</span><span class="sxs-lookup"><span data-stu-id="65262-324">In this case, all work where at least one work line has the work unit set to *ea* will be fed to the worker.</span></span> <span data-ttu-id="65262-325">Bu nedenle, bu iş, iş birimi *beher*'den farklı (*kutu* veya *palet* vb.) iş satırları olan işler de içerebilir.</span><span class="sxs-lookup"><span data-stu-id="65262-325">Therefore, this work might also include work where work lines have a work unit other than *ea* (such as *box* or *pallet*).</span></span> <span data-ttu-id="65262-326">Sorgu yalnızca iş birimi *beher* olan iş satırı bulunmayan işleri hariç tutacaktır.</span><span class="sxs-lookup"><span data-stu-id="65262-326">The query will exclude only work where no work line has the work unit set to *ea*.</span></span>

<span data-ttu-id="65262-327">Bu nedenle, bu senaryodaki örnekte iş kodu *4* de sorgu tarafından yakalanmıştır.</span><span class="sxs-lookup"><span data-stu-id="65262-327">Therefore, in the example from this scenario, work ID *4* was also captured by the query.</span></span> <span data-ttu-id="65262-328">Oluşturulduğu zaman iki satır eklenmiştir: biri 25 beher, diğeri 10 beher için.</span><span class="sxs-lookup"><span data-stu-id="65262-328">When it was created, two lines were added: one for 25 ea and another for 10 ea.</span></span> <span data-ttu-id="65262-329">En az bir iş satırı 20 beher'den az miktarda olduğu için, iş yine de kullanıcıya sunulmuştur.</span><span class="sxs-lookup"><span data-stu-id="65262-329">The work was still presented to the user, because at least one work line has a quantity of less than 20 ea.</span></span>

<span data-ttu-id="65262-330">Senaryoya bağlı olarak, molaları kullanarak bu davranışı önleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="65262-330">Depending on the scenario, you can prevent this behavior by using work breaks.</span></span>
