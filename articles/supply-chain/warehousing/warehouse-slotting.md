---
title: Ambar yerleştirme
description: Bu konuda ambar yerleştirme hakkında bilgiler verilmektedir. Ambar yerleştirme, talebi Sipariş edilen, Rezerve veya Serbest bırakılmış durumundaki siparişlerden madde ve ölçü birimine göre konsolide etmenize olanak sağlar. Bu, ambar yöneticilerinin, siparişleri ambara serbest bırakmadan ve malzeme çekme işi oluşturmadan önce malzeme çekme yerleşimlerini daha iyi planlamalarına yardımcı olur.
author: mirzaab
manager: tfehr
ms.date: 07/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSInventFixedLocation, WHSSlotDemandLocated, WHSSlotDemand, WHSSlotUOMTier, WHSSlotTemplate, WHSLocDirHint, WHSLocDirTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-01
ms.dyn365.ops.version: Release 10.0.9
ms.openlocfilehash: ed9e6eae2ecc8de8d5eeef4699678e93dd74f193
ms.sourcegitcommit: a36a4f9915ae3eb36bf8220111cf1486387713d9
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4017426"
---
# <a name="warehouse-slotting"></a><span data-ttu-id="82349-105">Ambar yerleştirme</span><span class="sxs-lookup"><span data-stu-id="82349-105">Warehouse slotting</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="82349-106">Ambar yerleştirme, talebi *Sipariş edilen* , *Rezerve* veya *Serbest bırakılmış* durumundaki siparişlerden madde ve ölçü birimine göre konsolide etmenize olanak sağlar.</span><span class="sxs-lookup"><span data-stu-id="82349-106">Warehouse slotting lets you consolidate demand by item and unit of measure from orders that have a status of *Ordered* , *Reserved* , or *Released*.</span></span> <span data-ttu-id="82349-107">Oluşturulan talep; miktar, birim, fiziksel boyutlar, sabit yerleşimler vb. temelinde malzeme çekme için kullanılacak yerleşimlere uygulanabilir.</span><span class="sxs-lookup"><span data-stu-id="82349-107">Generated demand can then be applied to locations that will be used for picking, based on quantity, unit, physical dimensions, fixed locations, and more.</span></span> <span data-ttu-id="82349-108">Yerleştirme planı belirlendikten sonra, her yerleşime uygun stok miktarını getirmek için stok yenileme işi oluşturulabilir.</span><span class="sxs-lookup"><span data-stu-id="82349-108">After the slotting plan has been established, replenishment work can be created to bring the appropriate amount of inventory to each location.</span></span>

<span data-ttu-id="82349-109">Bu işlevsellik, ambar yöneticilerinin, siparişleri ambara serbest bırakmadan ve malzeme çekme işi oluşturmadan önce malzeme çekme yerleşimlerini daha iyi planlamalarına yardımcı olur.</span><span class="sxs-lookup"><span data-stu-id="82349-109">This functionality helps warehouse managers intelligently plan picking locations before they release orders to the warehouse and create picking work.</span></span>

## <a name="turn-on-the-warehouse-slotting-feature"></a><span data-ttu-id="82349-110">Ambar yerleştirme özelliğini açma</span><span class="sxs-lookup"><span data-stu-id="82349-110">Turn on the warehouse slotting feature</span></span>

<span data-ttu-id="82349-111">Bu özelliği kullanabilmeniz için sisteminizde etkinleştirmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="82349-111">Before you can use this feature, it must be turned on in your system.</span></span> <span data-ttu-id="82349-112">Yöneticiler özellik durumunu denetlemek ve gerekirse etkinleştirmek için [özellik yönetimi](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) ayarlarını kullanabilir.</span><span class="sxs-lookup"><span data-stu-id="82349-112">Admins can use the [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) settings to check the status of the feature and turn it on if it's required.</span></span> <span data-ttu-id="82349-113">**Özellik yönetimi** çalışma alanındabu özellik aşağıdaki şekilde listelenir:</span><span class="sxs-lookup"><span data-stu-id="82349-113">In the **Feature management** workspace, the feature is listed in the following way:</span></span>

- <span data-ttu-id="82349-114">**Modül:** *Ambar yönetimi*</span><span class="sxs-lookup"><span data-stu-id="82349-114">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="82349-115">**Özellik adı:** *Ambar yerleştirme özelliği*</span><span class="sxs-lookup"><span data-stu-id="82349-115">**Feature name:** *Warehouse slotting feature*</span></span>

## <a name="set-up-warehouse-slotting"></a><span data-ttu-id="82349-116">Ambar yerleştirmeyi ayarlama</span><span class="sxs-lookup"><span data-stu-id="82349-116">Set up warehouse slotting</span></span>

<span data-ttu-id="82349-117">Ambar yerleştirmeyi kullanmak için, sisteminizde aşağıdaki öğeleri ayarlamanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="82349-117">To use warehouse slotting, you must set up the following elements in your system.</span></span>

### <a name="create-unit-of-measure-tiers-for-slotting"></a><a name="unit-tiers"></a><span data-ttu-id="82349-118">Yerleştirme için ölçü birimi katmanları oluşturma</span><span class="sxs-lookup"><span data-stu-id="82349-118">Create unit-of-measure tiers for slotting</span></span>

<span data-ttu-id="82349-119">Ölçü birimi katmanları, yerleştirme amacıyla birden fazla ölçü biriminin birlikte gruplandırılmasını sağlar.</span><span class="sxs-lookup"><span data-stu-id="82349-119">Unit-of-measure tiers enable multiple units of measure to be grouped together for the purposes of slotting.</span></span> <span data-ttu-id="82349-120">Örneğin aynı kutu çekme alanından birden fazla kutu boyutu çekiliyorsa, tüm boyutlar için bir katman oluşturulabilir.</span><span class="sxs-lookup"><span data-stu-id="82349-120">For example, if multiple sizes of boxes are all picked from the same box picking area, one tier can be created for all the sizes.</span></span> <span data-ttu-id="82349-121">**Katmanın parçası olması gereken her ölçü birimi için bir satır oluşturulmalıdır.**</span><span class="sxs-lookup"><span data-stu-id="82349-121">**A line must be created for each unit of measure that should be part of the tier.**</span></span>

1. <span data-ttu-id="82349-122">**Ambar yönetimi \> Kurulum \> Stok yenileme \> Yerleştirme ölçü birimi katmanları** 'na gidin.</span><span class="sxs-lookup"><span data-stu-id="82349-122">Go to **Warehouse management \> Setup \> Replenishment \> Slotting unit of measure tiers**.</span></span>
1. <span data-ttu-id="82349-123">**Yeni** 'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="82349-123">Select **New**.</span></span>
1. <span data-ttu-id="82349-124">Üst bilgide aşağıdaki değerleri ayarlayın:</span><span class="sxs-lookup"><span data-stu-id="82349-124">In the header, set the following values:</span></span>

    - <span data-ttu-id="82349-125">**Ölçü birimi katmanı:** *HerKutuPl*</span><span class="sxs-lookup"><span data-stu-id="82349-125">**Unit of measure tier:** *EaBoxPl*</span></span>
    - <span data-ttu-id="82349-126">**Açıklama:** *Her kutu paleti*</span><span class="sxs-lookup"><span data-stu-id="82349-126">**Description:** *Each box pallet*</span></span>

1. <span data-ttu-id="82349-127">**Kaydet** 'i seçin.</span><span class="sxs-lookup"><span data-stu-id="82349-127">Select **Save**.</span></span>
1. <span data-ttu-id="82349-128">**Ölçü birimi** hızlı sekmesinde, kılavuza satır eklemek için **Yeni** 'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="82349-128">On the **Units of measure** FastTab, select **New** to add a line to the grid.</span></span>
1. <span data-ttu-id="82349-129">Yeni satırda aşağıdaki değerleri ayarlayın:</span><span class="sxs-lookup"><span data-stu-id="82349-129">On the new line, set the following values:</span></span>

    - <span data-ttu-id="82349-130">**Birim:** *Kutu*</span><span class="sxs-lookup"><span data-stu-id="82349-130">**Unit:** *Box*</span></span>
    - <span data-ttu-id="82349-131">**Açıklama:** Bu alanı boş bırakın.</span><span class="sxs-lookup"><span data-stu-id="82349-131">**Description:** Leave this field blank.</span></span> <span data-ttu-id="82349-132">Değişikliklerinizi kaydettiğiniz zaman otomatik olarak doldurulur.</span><span class="sxs-lookup"><span data-stu-id="82349-132">It will be filled in automatically when you save your changes.</span></span>
    - <span data-ttu-id="82349-133">**Birim sınıfı:** *Miktar*</span><span class="sxs-lookup"><span data-stu-id="82349-133">**Unit class:** *Quantity*</span></span>

1. <span data-ttu-id="82349-134">Kılavuza ikinci bir satır eklemek için **Yeni** 'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="82349-134">Select **New** to add a second line to the grid.</span></span>
1. <span data-ttu-id="82349-135">Yeni satırda aşağıdaki değerleri ayarlayın:</span><span class="sxs-lookup"><span data-stu-id="82349-135">On the new line, set the following values:</span></span>

    - <span data-ttu-id="82349-136">**Birim:** *ea*</span><span class="sxs-lookup"><span data-stu-id="82349-136">**Unit:** *ea*</span></span>
    - <span data-ttu-id="82349-137">**Açıklama:** Bu alanı boş bırakın.</span><span class="sxs-lookup"><span data-stu-id="82349-137">**Description:** Leave this field blank.</span></span> <span data-ttu-id="82349-138">Değişikliklerinizi kaydettiğiniz zaman otomatik olarak doldurulur.</span><span class="sxs-lookup"><span data-stu-id="82349-138">It will be filled in automatically when you save your changes.</span></span>
    - <span data-ttu-id="82349-139">**Birim sınıfı:** *Miktar*</span><span class="sxs-lookup"><span data-stu-id="82349-139">**Unit class:** *Quantity*</span></span>

1. <span data-ttu-id="82349-140">Kılavuza üçüncü bir satır eklemek için **Yeni** 'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="82349-140">Select **New** to add a third line to the grid.</span></span>
1. <span data-ttu-id="82349-141">Yeni satırda aşağıdaki değerleri ayarlayın:</span><span class="sxs-lookup"><span data-stu-id="82349-141">On the new line, set the following values:</span></span>

    - <span data-ttu-id="82349-142">**Birim:** *PL*</span><span class="sxs-lookup"><span data-stu-id="82349-142">**Unit:** *PL*</span></span>
    - <span data-ttu-id="82349-143">**Açıklama:** Bu alanı boş bırakın.</span><span class="sxs-lookup"><span data-stu-id="82349-143">**Description:** Leave this field blank.</span></span> <span data-ttu-id="82349-144">Değişikliklerinizi kaydettiğiniz zaman otomatik olarak doldurulur.</span><span class="sxs-lookup"><span data-stu-id="82349-144">It will be filled in automatically when you save your changes.</span></span>
    - <span data-ttu-id="82349-145">**Birim sınıfı:** *Miktar*</span><span class="sxs-lookup"><span data-stu-id="82349-145">**Unit class:** *Quantity*</span></span>

1. <span data-ttu-id="82349-146">Katmanı kaydetmek için **Kaydet** 'i seçin.</span><span class="sxs-lookup"><span data-stu-id="82349-146">Select **Save** to save the tier.</span></span>

### <a name="create-a-directive-code-for-slotting"></a><span data-ttu-id="82349-147">Yerleştirme için yönerge kodu oluşturma</span><span class="sxs-lookup"><span data-stu-id="82349-147">Create a directive code for slotting</span></span>

<span data-ttu-id="82349-148">Bir şablonla ilişkilendirilmesi gereken yönerge kodunu seçmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="82349-148">You must select the directive code that should be associated with a template.</span></span>

1. <span data-ttu-id="82349-149">**Ambar yönetimi \> Kurulum \> Yönerge kodları** 'na gidin.</span><span class="sxs-lookup"><span data-stu-id="82349-149">Go to **Warehouse management \> Setup \> Directive codes**.</span></span>
1. <span data-ttu-id="82349-150">Eylem Bölmesinde, **Yeni** 'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="82349-150">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="82349-151">**Yönerge kodu** alanına, *Yerleştirme* girin.</span><span class="sxs-lookup"><span data-stu-id="82349-151">In the **Directive code** field, enter *Slotting*.</span></span>
1. <span data-ttu-id="82349-152">**Yönerge açıklaması** alanına, *Yerleştirme* girin.</span><span class="sxs-lookup"><span data-stu-id="82349-152">In the **Directive description** field, enter *Slotting*.</span></span>

### <a name="set-up-slotting-templates"></a><span data-ttu-id="82349-153">Yerleştirme şablonlarını ayarlama</span><span class="sxs-lookup"><span data-stu-id="82349-153">Set up slotting templates</span></span>

<span data-ttu-id="82349-154">Her yerleştirme şablonu, stokun belirli bir ambar için yerleşimlere nasıl atandığını denetler.</span><span class="sxs-lookup"><span data-stu-id="82349-154">Each slotting template controls how inventory is assigned to locations for a specific warehouse.</span></span> <span data-ttu-id="82349-155">Her şablon her bir yerleştirme belirtimi için bir satır içermelidir.</span><span class="sxs-lookup"><span data-stu-id="82349-155">Each template must include a line for each slotting specification.</span></span> <span data-ttu-id="82349-156">Yerleştirme şablonlarını ayarlamak için bu bölümdeki yordamları kullanın.</span><span class="sxs-lookup"><span data-stu-id="82349-156">Use the procedures in this section to set up slotting templates.</span></span>

1. <span data-ttu-id="82349-157">**Ambar yönetimi \> Kurulum \> Stok yenileme \> Yerleştirme şablonları** 'na gidin.</span><span class="sxs-lookup"><span data-stu-id="82349-157">Go to **Warehouse management \> Setup \> Replenishment \> Slotting templates**.</span></span>
1. <span data-ttu-id="82349-158">Şablon oluşturmak için **Yeni** 'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="82349-158">Select **New** to create a template.</span></span>

<span data-ttu-id="82349-159">Ardından, aşağıdaki alt bölümlerde anlatıldığı gibi, şablon üst bilgisini, yerleştirme belirtimlerini ve yerleşim yönergelerini ayarlamanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="82349-159">Next, you must set up the template header, slotting specifications, and location directives, as explained in the following subsections.</span></span>

#### <a name="set-up-a-slotting-template-header"></a><span data-ttu-id="82349-160">Yerleştirme şablon üst bilgisini ayarlama</span><span class="sxs-lookup"><span data-stu-id="82349-160">Set up a slotting template header</span></span>

1. <span data-ttu-id="82349-161">Şablonun üst bilgisinde aşağıdaki değerleri ayarlayın:</span><span class="sxs-lookup"><span data-stu-id="82349-161">In the header for the template, set the following values:</span></span>

    - <span data-ttu-id="82349-162">**Yerleştirme şablonu:** _61_</span><span class="sxs-lookup"><span data-stu-id="82349-162">**Slotting template:** _61_</span></span>
    - <span data-ttu-id="82349-163">**Açıklama:** _61_</span><span class="sxs-lookup"><span data-stu-id="82349-163">**Description:** _61_</span></span>
    - <span data-ttu-id="82349-164">**Talep türü:** *Satış siparişi*</span><span class="sxs-lookup"><span data-stu-id="82349-164">**Demand type:** *Sales order*</span></span>

        <span data-ttu-id="82349-165">Şu anda, *Satış siparişi* desteklenen tek talep türüdür.</span><span class="sxs-lookup"><span data-stu-id="82349-165">Currently, *Sales order* is the only demand type that is supported.</span></span>

    - <span data-ttu-id="82349-166">**Talep stratejisi:** _Sipariş edilen_</span><span class="sxs-lookup"><span data-stu-id="82349-166">**Demand strategy:** _Ordered_</span></span>

        <span data-ttu-id="82349-167">Bu alanda aşağıdaki değerler kullanılabilir:</span><span class="sxs-lookup"><span data-stu-id="82349-167">The following values are available in this field:</span></span>

        - <span data-ttu-id="82349-168">**Sipariş edilen** – Satış siparişindeki tam sipariş edilen miktar talep olarak kabul edilecektir.</span><span class="sxs-lookup"><span data-stu-id="82349-168">**Ordered** – The full ordered quantity on the sales order should be considered demand.</span></span>
        - <span data-ttu-id="82349-169">**Rezerve** – Yalnızca rezerve edilen (fiziksel ve sipariş edilen) satış siparişi satırı miktarları talep olarak kabul edilecektir.</span><span class="sxs-lookup"><span data-stu-id="82349-169">**Reserved** – Only the sales order line quantities that are reserved (physical and ordered) should be considered demand.</span></span>

    - <span data-ttu-id="82349-170">**Ambar:** _61_</span><span class="sxs-lookup"><span data-stu-id="82349-170">**Warehouse:** _61_</span></span>
    - <span data-ttu-id="82349-171">**Dalga talebinin rezerve edilmemiş miktarları kullanmasına izin ver:** _Evet_</span><span class="sxs-lookup"><span data-stu-id="82349-171">**Allow wave demand to use unreserved quantities:** _Yes_</span></span>

<span data-ttu-id="82349-172">Değerlendirilen talebin kapsamını daraltmak için bir sorgu da belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="82349-172">You can also specify a query to narrow the scope of the demand that is evaluated.</span></span>

#### <a name="set-up-slotting-specifications-for-each-template"></a><span data-ttu-id="82349-173">Her şablon için yerleştirme belirtimlerini ayarlama</span><span class="sxs-lookup"><span data-stu-id="82349-173">Set up slotting specifications for each template</span></span>

<span data-ttu-id="82349-174">Oluşturduğunuz her şablon için, her yerleştirme belirtimi için bir satır eklemek üzere aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="82349-174">For each template that you create, follow these steps to add a line for each slotting specification.</span></span>

1. <span data-ttu-id="82349-175">**Yerleştirme şablonu ayrıntıları** hızlı sekmesinde, şablon satırı oluşturmak için **Yeni** 'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="82349-175">On the **Slotting template details** FastTab, select **New** to create a template line.</span></span>
1. <span data-ttu-id="82349-176">Yeni satırda aşağıdaki değerleri ayarlayın:</span><span class="sxs-lookup"><span data-stu-id="82349-176">On the new line, set the following values:</span></span>

    - <span data-ttu-id="82349-177">**Sıra:** _1_</span><span class="sxs-lookup"><span data-stu-id="82349-177">**Sequence:** _1_</span></span>
    - <span data-ttu-id="82349-178">**Açıklama:** _Sabit yerleşim_</span><span class="sxs-lookup"><span data-stu-id="82349-178">**Description:** _Fixed location_</span></span>
    - <span data-ttu-id="82349-179">**Minimum miktar:** _1_</span><span class="sxs-lookup"><span data-stu-id="82349-179">**Minimum quantity:** _1_</span></span>

        <span data-ttu-id="82349-180">Bu alan, satır için gereken minimum talep miktarını tanımlar.</span><span class="sxs-lookup"><span data-stu-id="82349-180">This field defines the minimum quantity of demand that is required for the line.</span></span>

    - <span data-ttu-id="82349-181">**Maksimum miktar:** _1000000_</span><span class="sxs-lookup"><span data-stu-id="82349-181">**Maximum quantity:** _1000000_</span></span>

        <span data-ttu-id="82349-182">Bu alan, satır için geçerli olan maksimum talep miktarını tanımlar.</span><span class="sxs-lookup"><span data-stu-id="82349-182">This field defines the maximum quantity of demand that is valid for the line.</span></span>

    - <span data-ttu-id="82349-183">**Birim:** Bu alanı boş bırakın.</span><span class="sxs-lookup"><span data-stu-id="82349-183">**Unit:** Leave this field blank.</span></span>

        <span data-ttu-id="82349-184">Bu alan, minimum ve maksimum miktarların başvuruda bulunduğu ölçü birimini tanımlar.</span><span class="sxs-lookup"><span data-stu-id="82349-184">This field defines the unit of measure that the minimum and maximum quantities refer to.</span></span>

    - <span data-ttu-id="82349-185">**Ölçü Birimi Katmanı:** _HerKutuPl_</span><span class="sxs-lookup"><span data-stu-id="82349-185">**Unit of Measure Tier:** _EaBoxPl_</span></span>

        <span data-ttu-id="82349-186">Bu alan, satır için geçerli olan talebin ölçü birimlerini tanımlar.</span><span class="sxs-lookup"><span data-stu-id="82349-186">This field defines the units of measure of demand that are valid for the line.</span></span> <span data-ttu-id="82349-187">(Daha fazla bilgi için bu konuda daha önce işlenen [Yerleştirme için ölçü birimi katmanlarını ayarlama](#unit-tiers) bölümüne bakın.)</span><span class="sxs-lookup"><span data-stu-id="82349-187">(For more information, see the [Set up unit-of-measure tiers for slotting](#unit-tiers) section earlier in this topic.)</span></span>

    - <span data-ttu-id="82349-188">**Yerleştirme atama ölçütü:** _Miktarı dikkate al_</span><span class="sxs-lookup"><span data-stu-id="82349-188">**Assign slot criteria:** _Consider qty_</span></span>

        <span data-ttu-id="82349-189">Bu alanda aşağıdaki değerler kullanılabilir:</span><span class="sxs-lookup"><span data-stu-id="82349-189">The following values are available in this field:</span></span>

        - <span data-ttu-id="82349-190">**Boş kabul et** – Bu sistem, malzeme çekme alanındaki tüm yerleşimlerin boş olduğunu varsayacak ve bu yerleşimlerde stok denetimi yapmayacaktır.</span><span class="sxs-lookup"><span data-stu-id="82349-190">**Assume empty** – This system should assume that all locations in the picking area are empty and should not check those locations for inventory.</span></span>
        - <span data-ttu-id="82349-191">**Miktarı dikkate al** – Sistem, malzeme çekme alanındaki tüm yerleşimlerde stok denetimi yapacak ve boş olmayan yerleşimleri atlayacaktır.</span><span class="sxs-lookup"><span data-stu-id="82349-191">**Consider qty** – The system should check the locations in the picking area for inventory and should skip any locations that aren't empty.</span></span>

    - <span data-ttu-id="82349-192">**Yönerge kodu:** _Yerleştirme_</span><span class="sxs-lookup"><span data-stu-id="82349-192">**Directive code:** _Slotting_</span></span>

        <span data-ttu-id="82349-193">Bu alan, stok yenileme işinin malzeme çekme yerleşimini bulmak için kullanılan yerleşim yönergesini tanımlar.</span><span class="sxs-lookup"><span data-stu-id="82349-193">This field defines the location directive that is used to find the picking location of the replenishment work.</span></span>

    - <span data-ttu-id="82349-194">**Taşma konumu:** Bu alanı boş bırakın.</span><span class="sxs-lookup"><span data-stu-id="82349-194">**Overflow location:** Leave this field blank.</span></span>

        <span data-ttu-id="82349-195">Bu alan, satırın işlendiği sırada miktar için bir yerleşim bulunamazsa, stokun koyulacağı yerleşimi tanımlar.</span><span class="sxs-lookup"><span data-stu-id="82349-195">This field defines the location that inventory that is put to if a location can't be found for the quantity when the line is processed.</span></span>

    - <span data-ttu-id="82349-196">**Araya izin ver:** _Evet_</span><span class="sxs-lookup"><span data-stu-id="82349-196">**Allow let up:** _Yes_</span></span>

        <span data-ttu-id="82349-197">Bu seçenek *Evet* olarak ayarlandığında, herhangi bir talep yerleştirilemezse, stok bulunan ama yerleştirme yapılmayan yerleşimlerden dışarıya stok çekmek için hareket işi oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="82349-197">When this option is set to *Yes* , if any demand can't be slotted, movement work will be created to take inventory out of locations where there is inventory, but where nothing was slotted.</span></span> <span data-ttu-id="82349-198">Bunun üzerine şablon yeniden çalıştırılır.</span><span class="sxs-lookup"><span data-stu-id="82349-198">The template is then run again.</span></span> <span data-ttu-id="82349-199">Bu kez, yerleşimlerdeki stoku yok sayar.</span><span class="sxs-lookup"><span data-stu-id="82349-199">This time, it ignores the inventory in the locations.</span></span> <span data-ttu-id="82349-200">Bu işlevsellik en iyi şekilde, **Yerleştirme atama ölçütü** alanı _Miktarı dikkate al_ olarak ayarlandığı zaman çalışır.</span><span class="sxs-lookup"><span data-stu-id="82349-200">This functionality works best when the **Assign slot criteria** field is set to _Consider qty_.</span></span>

    - <span data-ttu-id="82349-201">**Sabit yerleşim kullanımı:** _Ürün için yalnızca sabit yerleşimler_</span><span class="sxs-lookup"><span data-stu-id="82349-201">**Fixed location usage:** _Only fixed locations for the product_</span></span>

        <span data-ttu-id="82349-202">Bu alanda aşağıdaki değerler kullanılabilir:</span><span class="sxs-lookup"><span data-stu-id="82349-202">The following values are available in this field:</span></span>

        - <span data-ttu-id="82349-203">**Sabit ve sabit olmayan yerleşimler** – Sistem sabit yerleşimleri kullanmayla sınırlı kalmaz.</span><span class="sxs-lookup"><span data-stu-id="82349-203">**Fixed and non-fixed locations** – The system should not be limited to using only fixed locations.</span></span>
        - <span data-ttu-id="82349-204">**Ürün için yalnızca sabit yerleşimler** – Sistem ürün için yalnızca sabit yerleşimler olan yerleşimlere yerleştirme yapar.</span><span class="sxs-lookup"><span data-stu-id="82349-204">**Only fixed locations for the product** – The system should slot only to locations that are fixed locations for the product.</span></span>
        - <span data-ttu-id="82349-205">**Ürün çeşidi için yalnızca sabit yerleşimler** – Sistem ürün çeşidi için yalnızca sabit yerleşimler olan yerleşimlere yerleştirme yapar.</span><span class="sxs-lookup"><span data-stu-id="82349-205">**Only fixed locations for the product variant** – The system should slot only to locations that are fixed locations for the product variant.</span></span>

1. <span data-ttu-id="82349-206">**Kaydet** 'i seçin.</span><span class="sxs-lookup"><span data-stu-id="82349-206">Select **Save**.</span></span>
1. <span data-ttu-id="82349-207">İkinci bir şablon satırı oluşturmak için **Yeni** 'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="82349-207">Select **New** to create a second template line.</span></span>
1. <span data-ttu-id="82349-208">Yeni satırda aşağıdaki değerleri ayarlayın:</span><span class="sxs-lookup"><span data-stu-id="82349-208">On the new line, set the following values:</span></span>

    - <span data-ttu-id="82349-209">**Sıra:** _2_</span><span class="sxs-lookup"><span data-stu-id="82349-209">**Sequence:** _2_</span></span>
    - <span data-ttu-id="82349-210">**Açıklama:** _Diğer_</span><span class="sxs-lookup"><span data-stu-id="82349-210">**Description:** _Other_</span></span>
    - <span data-ttu-id="82349-211">**Minimum Miktar:** _1_</span><span class="sxs-lookup"><span data-stu-id="82349-211">**Minimum Qty:** _1_</span></span>
    - <span data-ttu-id="82349-212">**Maksimum Miktar:** _1000000_</span><span class="sxs-lookup"><span data-stu-id="82349-212">**Maximum Qty:** _1000000_</span></span>
    - <span data-ttu-id="82349-213">**Birim:** Bu alanı boş bırakın.</span><span class="sxs-lookup"><span data-stu-id="82349-213">**Unit:** Leave this field blank.</span></span>
    - <span data-ttu-id="82349-214">**Ölçü birimi katmanı:** _HerKutuPl_</span><span class="sxs-lookup"><span data-stu-id="82349-214">**Unit of measure tier:** _EaBoxPl_</span></span>
    - <span data-ttu-id="82349-215">**Yerleştirme atama ölçütü:** _Miktarı dikkate al_</span><span class="sxs-lookup"><span data-stu-id="82349-215">**Assign slot criteria:** _Consider qty_</span></span>
    - <span data-ttu-id="82349-216">**Yönerge kodu:** _Yerleştirme_</span><span class="sxs-lookup"><span data-stu-id="82349-216">**Directive code:** _Slotting_</span></span>
    - <span data-ttu-id="82349-217">**Taşma konumu:** Bu alanı boş bırakın.</span><span class="sxs-lookup"><span data-stu-id="82349-217">**Overflow location:** Leave this field blank.</span></span>
    - <span data-ttu-id="82349-218">**Araya izin ver:** _Evet_</span><span class="sxs-lookup"><span data-stu-id="82349-218">**Allow let up:** _Yes_</span></span>
    - <span data-ttu-id="82349-219">**Sabit yerleşimleri kullan:** _Sabit ve sabit olmayan yerleşimler_</span><span class="sxs-lookup"><span data-stu-id="82349-219">**Use fixed locations:** _Fixed and non-fixed locations_</span></span>

    <span data-ttu-id="82349-220">İkinci satır için sorguda, o satırla ilgili talebin yerleştirilebileceği yerleşimleri belirlemek için kullanılan ölçütleri belirtirsiniz.</span><span class="sxs-lookup"><span data-stu-id="82349-220">In the query for the second line, you will now specify the criteria that are used to determine what locations the demand for that line can be slotted to.</span></span>

1. <span data-ttu-id="82349-221">**Sıra** alanının *2* olarak ayarlandığı satırı seçin.</span><span class="sxs-lookup"><span data-stu-id="82349-221">Select the line where the **Sequence** field is set to *2*.</span></span>
1. <span data-ttu-id="82349-222">**Sorguyu düzenle** 'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="82349-222">Select **Edit query**.</span></span>
1. <span data-ttu-id="82349-223">**Aralık** sekmesinde, kılavuza satır eklemek için **Ekle** 'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="82349-223">On the **Range** tab, select **Add** to add a line to the grid.</span></span>
1. <span data-ttu-id="82349-224">Yeni satırda aşağıdaki değerleri ayarlayın:</span><span class="sxs-lookup"><span data-stu-id="82349-224">On the new line, set the following values:</span></span>

    - <span data-ttu-id="82349-225">**Tablo:** *Yerleşimler*</span><span class="sxs-lookup"><span data-stu-id="82349-225">**Table:** *Locations*</span></span>
    - <span data-ttu-id="82349-226">**Türetilmiş tablo:** *Yerleşimler*</span><span class="sxs-lookup"><span data-stu-id="82349-226">**Derived table:** *Locations*</span></span>
    - <span data-ttu-id="82349-227">**Alan:** *Yerleşim profili kodu*</span><span class="sxs-lookup"><span data-stu-id="82349-227">**Field:** *Location profile ID*</span></span>
    - <span data-ttu-id="82349-228">**Ölçüt:** *Malzeme Çekme-06* (Listeyi genişletmek için alandaki çift artı işaretini \[**++**\] ve ardından *Malzeme Çekme-06* - *Malzeme Çekme Tesisi 6* 'yı seçin.)</span><span class="sxs-lookup"><span data-stu-id="82349-228">**Criteria:** *Pick-06* (Select the double plus sign \[**++**\] in the field to expand the list, and then select *Pick-06* - *Picking Site 6*.)</span></span>

1. <span data-ttu-id="82349-229">**Tamam** 'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="82349-229">Select **OK**.</span></span>

#### <a name="set-up-location-directives"></a><span data-ttu-id="82349-230">Yerleşim yönergelerini kur</span><span class="sxs-lookup"><span data-stu-id="82349-230">Set up location directives</span></span>

<span data-ttu-id="82349-231">Yerleştirme çekme işlemlerini destekleyecek en az bir yerleştirme yönergesi ayarlanmalıdır.</span><span class="sxs-lookup"><span data-stu-id="82349-231">At least one location directive must be set up to support slotting picks.</span></span> <span data-ttu-id="82349-232">Yerleştirme çekme işlemleri için yeni bir *stok yenileme yerleşimi yönergesi* ayarlamak için bu bölümdeki yordamları kullanın.</span><span class="sxs-lookup"><span data-stu-id="82349-232">Use the procedures in this section to set up a new *replenishment location directive* for slotting picks.</span></span>

1. <span data-ttu-id="82349-233">**Ambar Yönetimi \> Kurulum \> Konum yönergeleri** seçeneğine gidin.</span><span class="sxs-lookup"><span data-stu-id="82349-233">Go to **Warehouse management \> Setup \> Location directives**.</span></span>
1. <span data-ttu-id="82349-234">Sol bölmedeki **İş emri türü** alanında *Stok yenileme* 'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="82349-234">In the left pane, in the **Work order type** field, select *Replenishment*.</span></span>
1. <span data-ttu-id="82349-235">Eylem Bölmesinde, **Yeni** 'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="82349-235">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="82349-236">Yeni yerleşim yönergesinin üst bilgisindeki **Ad** alanına *61 Yerleştirme çekme işlemi* girin.</span><span class="sxs-lookup"><span data-stu-id="82349-236">In the header for the new location directive, in the **Name** field, enter *61 Slotting pick*.</span></span>

##### <a name="configure-the-location-directives-fasttab"></a><span data-ttu-id="82349-237">Yerleşim yönergeleri hızlı sekmesini yapılandırma</span><span class="sxs-lookup"><span data-stu-id="82349-237">Configure the Location directives FastTab</span></span>

1. <span data-ttu-id="82349-238">**Yerleşim yönergeleri** hızlı sekmesinde aşağıdaki değerleri ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="82349-238">On the **Location directives** FastTab, set the following values.</span></span> <span data-ttu-id="82349-239">Tüm diğer alanlar için varsayılan değerleri kabul edin.</span><span class="sxs-lookup"><span data-stu-id="82349-239">Accept the default values for all other fields.</span></span>

    - <span data-ttu-id="82349-240">**İş türü:** _Çekme_</span><span class="sxs-lookup"><span data-stu-id="82349-240">**Work type:** _Pick_</span></span>
    - <span data-ttu-id="82349-241">**Tesis:** _6_</span><span class="sxs-lookup"><span data-stu-id="82349-241">**Site:** _6_</span></span>
    - <span data-ttu-id="82349-242">**Ambar:** _61_</span><span class="sxs-lookup"><span data-stu-id="82349-242">**Warehouse:** _61_</span></span>
    - <span data-ttu-id="82349-243">**Yönerge kodu:** _Yerleştirme_</span><span class="sxs-lookup"><span data-stu-id="82349-243">**Directive code:** _Slotting_</span></span>

1. <span data-ttu-id="82349-244">**Satırlar** hızlı sekmesini kullanılabilir hale getirmek için **Kaydet** 'i seçin.</span><span class="sxs-lookup"><span data-stu-id="82349-244">Select **Save** to make the **Lines** FastTab available.</span></span>

##### <a name="configure-the-lines-fasttab"></a><span data-ttu-id="82349-245">Satırlar hızlı sekmesini yapılandırma</span><span class="sxs-lookup"><span data-stu-id="82349-245">Configure the Lines FastTab</span></span>

1. <span data-ttu-id="82349-246">**Satırlar** hızlı sekmesinde yeni bir satır oluşturmak için **Yeni** 'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="82349-246">On the **Lines** FastTab, select **New** to create a line.</span></span>
1. <span data-ttu-id="82349-247">Yeni satırda aşağıdaki değerleri ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="82349-247">On the new line, set the following values.</span></span> <span data-ttu-id="82349-248">Tüm diğer alanlar için varsayılan değerleri kabul edin.</span><span class="sxs-lookup"><span data-stu-id="82349-248">Accept the default values for all other fields.</span></span>

    - <span data-ttu-id="82349-249">**Başlangıç miktarı:** _0_</span><span class="sxs-lookup"><span data-stu-id="82349-249">**From quantity:** _0_</span></span>
    - <span data-ttu-id="82349-250">**Son miktar:** _1000000_</span><span class="sxs-lookup"><span data-stu-id="82349-250">**To quantity:** _1000000_</span></span>

1. <span data-ttu-id="82349-251">**Yerleşim Yönergesi Eylemleri** hızlı sekmesini kullanılabilir hale getirmek için **Kaydet** 'i seçin.</span><span class="sxs-lookup"><span data-stu-id="82349-251">Select **Save** to make the **Location Directive Actions** FastTab available.</span></span>

##### <a name="configure-the-location-directive-actions-fasttab"></a><span data-ttu-id="82349-252">Yerleşim Yönergesi Eylemleri hızlı sekmesini yapılandırma</span><span class="sxs-lookup"><span data-stu-id="82349-252">Configure the Location Directive Actions FastTab</span></span>

1. <span data-ttu-id="82349-253">**Yerleşim Yönergesi Eylemleri** hızlı sekmesinde yeni bir satır oluşturmak için **Yeni** 'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="82349-253">On the **Location Directive Actions** FastTab, select **New** to create a line.</span></span>
1. <span data-ttu-id="82349-254">Yeni satırda aşağıdaki değerleri ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="82349-254">On the new line, set the following values.</span></span> <span data-ttu-id="82349-255">Tüm diğer alanlar için varsayılan değerleri kabul edin.</span><span class="sxs-lookup"><span data-stu-id="82349-255">Accept the default values for all other fields.</span></span>

    - <span data-ttu-id="82349-256">**Ad:** _Toplu_</span><span class="sxs-lookup"><span data-stu-id="82349-256">**Name:** _Bulk_</span></span>
    - <span data-ttu-id="82349-257">**Strateji:** _Yok_</span><span class="sxs-lookup"><span data-stu-id="82349-257">**Strategy:** _None_</span></span>

1. <span data-ttu-id="82349-258">**Sorguyu düzenle** düğmesini kullanılabilir hale getirmek için **Kaydet** 'i seçin.</span><span class="sxs-lookup"><span data-stu-id="82349-258">Select **Save** to make the **Edit query** button available.</span></span>

##### <a name="edit-the-query"></a><span data-ttu-id="82349-259">Sorguyu düzenleme</span><span class="sxs-lookup"><span data-stu-id="82349-259">Edit the query</span></span>

1. <span data-ttu-id="82349-260">**Yerleşim Yönergesi Eylemleri** hızlı sekmesinde **Sorguyu düzenle** 'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="82349-260">On the **Location Directive Actions** FastTab, select **Edit query**.</span></span>
1. <span data-ttu-id="82349-261">**Aralık** sekmesinde, kılavuza satır eklemek için **Ekle** 'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="82349-261">On the **Range** tab, select **Add** to add a line to the grid.</span></span>
1. <span data-ttu-id="82349-262">Yeni satırda aşağıdaki değerleri ayarlayın:</span><span class="sxs-lookup"><span data-stu-id="82349-262">On the new line, set the following values:</span></span>

    - <span data-ttu-id="82349-263">**Tablo:** *Yerleşimler*</span><span class="sxs-lookup"><span data-stu-id="82349-263">**Table:** *Locations*</span></span>
    - <span data-ttu-id="82349-264">**Türetilmiş tablo:** *Yerleşimler*</span><span class="sxs-lookup"><span data-stu-id="82349-264">**Derived table:** *Locations*</span></span>
    - <span data-ttu-id="82349-265">**Alan:** *Bölge Kodu*</span><span class="sxs-lookup"><span data-stu-id="82349-265">**Field:** *Zone ID*</span></span>
    - <span data-ttu-id="82349-266">**Ölçüt:** *Toplu* (Listeyi genişletmek için alandaki çift artı işaretini \[**++**\] ve ardından *Toplu* 'yu seçin.)</span><span class="sxs-lookup"><span data-stu-id="82349-266">**Criteria:** *Bulk* (Select the double plus sign \[**++**\] in the field to expand the list, and then select *Bulk*.)</span></span>

1. <span data-ttu-id="82349-267">**Tamam** 'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="82349-267">Select **OK**.</span></span>

## <a name="scenario"></a><span data-ttu-id="82349-268">Senaryo</span><span class="sxs-lookup"><span data-stu-id="82349-268">Scenario</span></span>

### <a name="set-up-the-scenario"></a><span data-ttu-id="82349-269">Senaryoyu ayarlama</span><span class="sxs-lookup"><span data-stu-id="82349-269">Set up the scenario</span></span>

<span data-ttu-id="82349-270">Bu senaryo için, yerleşik örnek verileri kullanın ve bu bölümde açıklanan kayıtları oluşturun.</span><span class="sxs-lookup"><span data-stu-id="82349-270">For this scenario, use the built-in sample data, and create the records that are described in this section.</span></span>

#### <a name="use-the-usmf-sample-data"></a><span data-ttu-id="82349-271">USMF örnek verilerini kullanın</span><span class="sxs-lookup"><span data-stu-id="82349-271">Use the USMF sample data</span></span>

<span data-ttu-id="82349-272">Burada belirtilen örnek kayıtları ve değerleri kullanarak bu senaryo üzerinden çalışmak için, standart [tanıtım verilerinin](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) yüklenmiş olduğu bir sistemde olmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="82349-272">To work through this scenario by using the sample records and values that are specified here, you must be on a system where the standard [demo data](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) is installed.</span></span> <span data-ttu-id="82349-273">Ek olarak, başlamadan önce **USMF** tüzel kişiliğini seçmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="82349-273">Additionally, you must select the **USMF** legal entity before you begin.</span></span>

#### <a name="create-demand"></a><span data-ttu-id="82349-274">Talep oluşturma</span><span class="sxs-lookup"><span data-stu-id="82349-274">Create demand</span></span>

<span data-ttu-id="82349-275">Yerleştirme uygulayacağınız talebi oluşturmak için bu adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="82349-275">Follow these steps to create the demand that you will apply slotting to.</span></span>

1. <span data-ttu-id="82349-276">**Satış ve pazarlama \> Satış siparişleri \> Tüm satış siparişleri** 'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="82349-276">Go to **Sales and marketing \> Sales orders \> All sales order**.</span></span>
1. <span data-ttu-id="82349-277">Satış siparişi oluşturmak için **Yeni** 'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="82349-277">Select **New** to create a sales order.</span></span>
1. <span data-ttu-id="82349-278">**Satış siparişi oluştur** iletişim kutusundaki **Müşteri hesabı** alanında _ABD-007_ 'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="82349-278">In the **Create sales order** dialog box, in the **Customer account** field, select _US-007_.</span></span>
1. <span data-ttu-id="82349-279">**Ambar** alanında _61_ 'i seçin.</span><span class="sxs-lookup"><span data-stu-id="82349-279">In the **Warehouse** field, select _61_.</span></span>
1. <span data-ttu-id="82349-280">**Tamam** 'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="82349-280">Select **OK**.</span></span>
1. <span data-ttu-id="82349-281">Yeni satış siparişi açılır.</span><span class="sxs-lookup"><span data-stu-id="82349-281">The new sales order is opened.</span></span> <span data-ttu-id="82349-282">**Satış siparişi satırları** hızlı sekmesinde boş bir satır bulunur.</span><span class="sxs-lookup"><span data-stu-id="82349-282">It includes an empty line on the **Sales order lines** FastTab.</span></span> <span data-ttu-id="82349-283">Bu satır için aşağıdaki değerleri ayarlayın:</span><span class="sxs-lookup"><span data-stu-id="82349-283">On this line, set the following values:</span></span>

    - <span data-ttu-id="82349-284">**Madde:** _L0101_</span><span class="sxs-lookup"><span data-stu-id="82349-284">**Item:** _L0101_</span></span>
    - <span data-ttu-id="82349-285">**Miktar:** _20_</span><span class="sxs-lookup"><span data-stu-id="82349-285">**Quantity:** _20_</span></span>

1. <span data-ttu-id="82349-286">**Satır ekle** 'yi seçerek yeni bir satır ekleyin ve aşağıdaki değerleri ayarlayın:</span><span class="sxs-lookup"><span data-stu-id="82349-286">Select **Add line** to add a new line, and set the following values:</span></span>

    - <span data-ttu-id="82349-287">**Madde:** _T0100_</span><span class="sxs-lookup"><span data-stu-id="82349-287">**Item:** _T0100_</span></span>
    - <span data-ttu-id="82349-288">**Miktar:** _8_</span><span class="sxs-lookup"><span data-stu-id="82349-288">**Quantity:** _8_</span></span>

1. <span data-ttu-id="82349-289">**Kaydet** 'i seçin.</span><span class="sxs-lookup"><span data-stu-id="82349-289">Select **Save**.</span></span>
1. <span data-ttu-id="82349-290">İkinci bir satış siparişi oluşturmak için **Yeni** 'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="82349-290">Select **New** to create a second sales order.</span></span>
1. <span data-ttu-id="82349-291">**Satış siparişi oluştur** iletişim kutusundaki **Müşteri hesabı** alanında _ABD-008_ 'i seçin.</span><span class="sxs-lookup"><span data-stu-id="82349-291">In the **Create sales order** dialog box, in the **Customer account** field, select _US-008_.</span></span>
1. <span data-ttu-id="82349-292">**Ambar** alanında _61_ 'i seçin.</span><span class="sxs-lookup"><span data-stu-id="82349-292">In the **Warehouse** field, select _61_.</span></span>
1. <span data-ttu-id="82349-293">Yeni satış siparişi açılır.</span><span class="sxs-lookup"><span data-stu-id="82349-293">The new sales order is opened.</span></span> <span data-ttu-id="82349-294">**Satış siparişi satırları** hızlı sekmesinde boş bir satır bulunur.</span><span class="sxs-lookup"><span data-stu-id="82349-294">It includes an empty line on the **Sales order lines** FastTab.</span></span> <span data-ttu-id="82349-295">Bu satır için aşağıdaki değerleri ayarlayın:</span><span class="sxs-lookup"><span data-stu-id="82349-295">On this line, set the following values:</span></span>

    - <span data-ttu-id="82349-296">**Madde:** _T0100_</span><span class="sxs-lookup"><span data-stu-id="82349-296">**Item:** _T0100_</span></span>
    - <span data-ttu-id="82349-297">**Miktar:** _1_</span><span class="sxs-lookup"><span data-stu-id="82349-297">**Quantity:** _1_</span></span>

1. <span data-ttu-id="82349-298">**Kaydet** 'i seçin.</span><span class="sxs-lookup"><span data-stu-id="82349-298">Select **Save**.</span></span>

### <a name="walk-through-a-typical-slotting-scenario"></a><span data-ttu-id="82349-299">Tipik bir yerleştirme senaryosu üzerinden ilerleme</span><span class="sxs-lookup"><span data-stu-id="82349-299">Walk through a typical slotting scenario</span></span>

<span data-ttu-id="82349-300">Önceki bölümde açıklandığı gibi, tüm önkoşul öğeleri belirlendikten sonra, bu bölümdeki her alıştırmada çalışarak bu özelliği denemeye hazırsınız demektir.</span><span class="sxs-lookup"><span data-stu-id="82349-300">After all the prerequisite elements are in place, as described in the previous section, you're ready to try out the feature by working through each exercise in this section.</span></span>

#### <a name="generate-demand"></a><span data-ttu-id="82349-301">Talep oluştur</span><span class="sxs-lookup"><span data-stu-id="82349-301">Generate demand</span></span>

1. <span data-ttu-id="82349-302">**Ambar yönetimi \> Kurulum \> Stok yenileme \> Yerleştirme şablonları** 'na gidin ve daha önce oluşturduğunuz yerleştirme şablonunu seçin.</span><span class="sxs-lookup"><span data-stu-id="82349-302">Go to **Warehouse management \> Setup \> Replenishment \> Slotting templates** , and select the slotting template that you created earlier.</span></span>
1. <span data-ttu-id="82349-303">Eylem bölmesinde, **Talep oluştur** 'u seçin.</span><span class="sxs-lookup"><span data-stu-id="82349-303">On the Action Pane, select **Generate demand**.</span></span> <span data-ttu-id="82349-304">Bu komut sistemdeki tüm talepleri değerlendirir ve yerleştirme şablon sorgusunu eşleştirir.</span><span class="sxs-lookup"><span data-stu-id="82349-304">This command evaluates all demand that is in the system, and that matches the slotting template query.</span></span> <span data-ttu-id="82349-305">Böylece tüm siparişlerdeki toplam talep, miktar/ölçü birimi başına tek bir satırda birleştirilir.</span><span class="sxs-lookup"><span data-stu-id="82349-305">The total demand across all orders is then consolidated onto one line per quantity/unit of measure.</span></span> <span data-ttu-id="82349-306">İşlem tamamlanınca bir bilgi iletisi görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="82349-306">An informational message appears when the process is completed.</span></span>

#### <a name="slotting-demand"></a><span data-ttu-id="82349-307">Yerleştirme talebi</span><span class="sxs-lookup"><span data-stu-id="82349-307">Slotting demand</span></span>

<span data-ttu-id="82349-308">*Yerleştirme talebi* , yerleştirme şablonunun kurulumuna bağlı olarak, talep oluşturma sonuçlarını gösterir.</span><span class="sxs-lookup"><span data-stu-id="82349-308">The *slotting demand* shows the results of demand generation, based on the setup of the slotting template.</span></span>

- <span data-ttu-id="82349-309">Eylem bölmesinde, **Talep oluştur** komutundan elde edilen sonuçları görmek için **Yerleştirme talebi** 'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="82349-309">On the Action Pane, select **Slotting demand** to view the results from the **Generate demand** command.</span></span> <span data-ttu-id="82349-310">Yerleştirme talebindeki satırlar düzenlenebilir.</span><span class="sxs-lookup"><span data-stu-id="82349-310">The lines in the slotting demand can be edited.</span></span> <span data-ttu-id="82349-311">Bir satırı silebilir, yeni bir satır ekleyebilir veya satır ayrıntılarını düzenleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="82349-311">You can delete a line, add a new line, or edit the line details.</span></span>

> [!NOTE]
> <span data-ttu-id="82349-312">Talebi el ile düzenleyebilir veya veri yönetimini kullanarak harici bir sistemden içe aktarabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="82349-312">You can edit demand manually, or you can import it from an external system by using data management.</span></span> <span data-ttu-id="82349-313">Yerleştirme talebindeki her şey sonraki adımda nereden geldiği dikkate alınmaksızın kullanılır.</span><span class="sxs-lookup"><span data-stu-id="82349-313">Whatever is in the slotting demand will be used in the next step, regardless of where it came from.</span></span>

#### <a name="locate-demand"></a><span data-ttu-id="82349-314">Talebi bul</span><span class="sxs-lookup"><span data-stu-id="82349-314">Locate demand</span></span>

<span data-ttu-id="82349-315">Talep oluşturulduktan sonra, *yerleştirme planı* oluşturmak için **Talep bul** komutunu kullanmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="82349-315">After demand has been generated, you must use the **Locate demand** command to generate the *slotting plan*.</span></span>

- <span data-ttu-id="82349-316">Eylem bölmesinde, **Talep bul** 'u seçin.</span><span class="sxs-lookup"><span data-stu-id="82349-316">On the Action Pane, select **Locate demand**.</span></span> <span data-ttu-id="82349-317">Yerleştirme işlemi çalıştırılır.</span><span class="sxs-lookup"><span data-stu-id="82349-317">The slotting process runs.</span></span> <span data-ttu-id="82349-318">İşlem tamamlanınca bir bilgi iletisi görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="82349-318">An informational message appears when the process is completed.</span></span>

#### <a name="slotting-plan"></a><span data-ttu-id="82349-319">Yerleştirme planı</span><span class="sxs-lookup"><span data-stu-id="82349-319">Slotting plan</span></span>

<span data-ttu-id="82349-320">Yerleştirme planı, her madde/miktarın atandığı yerleşimi, taşma kullanılıp kullanılmadığını, ara işi oluşturulup oluşturulmadığını ve kullanılan şablon satırını gösterir.</span><span class="sxs-lookup"><span data-stu-id="82349-320">The slotting plan shows the location that each item/quantity was assigned to, whether overflow was used, whether let-up work was created, and the template line that was used.</span></span> <span data-ttu-id="82349-321">**Yerleştirilememiş talepler kırmızı renkle vurgulanır.**</span><span class="sxs-lookup"><span data-stu-id="82349-321">**Any demand that could not be slotted is highlighted in red.**</span></span>

- <span data-ttu-id="82349-322">Eylem bölmesinde, sonuçları görüntülemek için **Yerleştirme planı** 'nı seçin.</span><span class="sxs-lookup"><span data-stu-id="82349-322">On the Action Pane, select **Slotting plan** to view the results.</span></span>

#### <a name="create-replenishment"></a><span data-ttu-id="82349-323">Stok yenileme oluşturma</span><span class="sxs-lookup"><span data-stu-id="82349-323">Create replenishment</span></span>

<span data-ttu-id="82349-324">Yerleştirme planı oluşturulduktan sonra, plana göre, *stok yenileme işi* oluşturmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="82349-324">After the slotting plan has been created, you must create *replenishment work* , based on the plan.</span></span>

- <span data-ttu-id="82349-325">Eylem bölmesinde **Stok yenilemeyi çalıştır** 'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="82349-325">On the Action Pane, select **Run replenishment**.</span></span> <span data-ttu-id="82349-326">İşlem tamamlanınca bir bilgi iletisi görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="82349-326">An informational message appears when the process is completed.</span></span> <span data-ttu-id="82349-327">Bu ileti, iş yapı kodu için oluşturulan üst bilgilerin sayısını gösterir.</span><span class="sxs-lookup"><span data-stu-id="82349-327">This message indicates the number of headers that were created for the work build ID.</span></span>

<span data-ttu-id="82349-328">Kullanılacak yerleşim yönergeleri her bir şablon satırında belirtilen yönerge koduna göre tanımlanır.</span><span class="sxs-lookup"><span data-stu-id="82349-328">Location directives that will be used are identified based on the directive code that is specified on each template line.</span></span>

## <a name="tips"></a><span data-ttu-id="82349-329">İpuçları</span><span class="sxs-lookup"><span data-stu-id="82349-329">Tips</span></span>

### <a name="set-up-automatic-slotting"></a><span data-ttu-id="82349-330">Otomatik yerleştirme ayarlama</span><span class="sxs-lookup"><span data-stu-id="82349-330">Set up automatic slotting</span></span>

<span data-ttu-id="82349-331">Gerekli tüm öğeler belirlendikten sonra, aşağıdaki adımları izleyerek otomatik olarak çalışacak bir yerleştirme ayarlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="82349-331">After all the required elements are in place, you can set up slotting to run automatically by following these steps.</span></span>

1. <span data-ttu-id="82349-332">**Ambar yönetimi \> Stok yenileme \> Yerleştirmeyi çalıştır** 'a gidin.</span><span class="sxs-lookup"><span data-stu-id="82349-332">Go to **Warehouse management \> Replenishment \> Run slotting**.</span></span>
1. <span data-ttu-id="82349-333">Çalıştırılacak yerleştirme adımlarını belirtin.</span><span class="sxs-lookup"><span data-stu-id="82349-333">Specify the slotting steps to run.</span></span> <span data-ttu-id="82349-334">Aşağıdaki yerleştirme adımlarından birini veya birkaçını seçin:</span><span class="sxs-lookup"><span data-stu-id="82349-334">Select one or more of the following slotting steps:</span></span>

    - <span data-ttu-id="82349-335">Talep oluştur</span><span class="sxs-lookup"><span data-stu-id="82349-335">Generate demand</span></span>
    - <span data-ttu-id="82349-336">Talebi bul</span><span class="sxs-lookup"><span data-stu-id="82349-336">Locate demand</span></span>
    - <span data-ttu-id="82349-337">Stok yenileme işi oluştur</span><span class="sxs-lookup"><span data-stu-id="82349-337">Create replenishment work</span></span>

    > [!NOTE]
    > <span data-ttu-id="82349-338">Yerleştirme adımları aşamalıdır.</span><span class="sxs-lookup"><span data-stu-id="82349-338">The slotting steps are progressive.</span></span> <span data-ttu-id="82349-339">*Talebi bul* 'u seçmek istiyorsanız, önce *Talep oluştur* 'u seçmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="82349-339">If you want to select *Locate demand* , you must first select *Generate demand*.</span></span>

1. <span data-ttu-id="82349-340">Kullanılacak yerleştirme şablonunu belirtin.</span><span class="sxs-lookup"><span data-stu-id="82349-340">Specify the slotting template to use.</span></span>
1. <span data-ttu-id="82349-341">İsterseniz otomatik çalışma tekrar sayısını belirleyin.</span><span class="sxs-lookup"><span data-stu-id="82349-341">Set the recurrence to run automatically, if you want.</span></span>

<span data-ttu-id="82349-342">Senaryodaki alıştırmalarda otomatik yerleştirme **ayarlamayın**.</span><span class="sxs-lookup"><span data-stu-id="82349-342">For the exercises in the scenario, do **not** set up automatic slotting.</span></span>
