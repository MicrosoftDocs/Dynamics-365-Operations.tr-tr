---
title: Ambar yerleştirme
description: Bu konuda ambar yerleştirme hakkında bilgiler verilmektedir. Ambar yerleştirme, talebi Sipariş edilen, Rezerve veya Serbest bırakılmış durumundaki siparişlerden madde ve ölçü birimine göre konsolide etmenize olanak sağlar. Bu, ambar yöneticilerinin, siparişleri ambara serbest bırakmadan ve malzeme çekme işi oluşturmadan önce malzeme çekme yerleşimlerini daha iyi planlamalarına yardımcı olur.
author: mirzaab
manager: tfehr
ms.date: 11/13/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSInventFixedLocation, WHSSlotDemandLocated, WHSSlotDemand, WHSSlotUOMTier, WHSSlotTemplate, WHSLocDirHint, WHSLocDirTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-01
ms.dyn365.ops.version: Release 10.0.9
ms.openlocfilehash: fb39daba393944471ee5d412b1eb61754843926f
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/15/2021
ms.locfileid: "4993765"
---
# <a name="warehouse-slotting"></a><span data-ttu-id="d6b0d-105">Ambar yerleştirme</span><span class="sxs-lookup"><span data-stu-id="d6b0d-105">Warehouse slotting</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d6b0d-106">Ambar yöneticilerinin, siparişleri ambara serbest bırakmadan ve malzeme çekme işi oluşturmadan önce malzeme çekme yerleşimlerini daha iyi planlamalarına yardımcı olan çok sayıda ambar yerleştirme özelliği mevcuttur.</span><span class="sxs-lookup"><span data-stu-id="d6b0d-106">Several warehouse slotting features are available to help warehouse managers intelligently plan picking locations before they release orders to the warehouse and create picking work.</span></span>

<span data-ttu-id="d6b0d-107">*Ambar yerleştirme* özelliği, talebi *Sipariş edildi*, *Rezerve edildi* veya *Serbest bırakıldı* durumundaki siparişlerden madde ve ölçü birimine göre konsolide etmenize olanak sağlar.</span><span class="sxs-lookup"><span data-stu-id="d6b0d-107">The *Warehouse slotting feature* lets you consolidate demand by item and unit of measure from orders that have a status of *Ordered*, *Reserved*, or *Released*.</span></span> <span data-ttu-id="d6b0d-108">Oluşturulan talep; miktar, birim, fiziksel boyutlar, sabit yerleşimler vb. temelinde malzeme çekme için kullanılacak yerleşimlere uygulanabilir.</span><span class="sxs-lookup"><span data-stu-id="d6b0d-108">Generated demand can then be applied to locations that will be used for picking, based on quantity, unit, physical dimensions, fixed locations, and more.</span></span> <span data-ttu-id="d6b0d-109">Yerleştirme planı belirlendikten sonra, her yerleşime uygun stok miktarını getirmek için stok yenileme işi oluşturulabilir.</span><span class="sxs-lookup"><span data-stu-id="d6b0d-109">After the slotting plan has been established, replenishment work can be created to bring the appropriate amount of inventory to each location.</span></span>

<span data-ttu-id="d6b0d-110">*Transfer emirleri için ambar yerleştirme* özelliği, ambar yöneticilerinin henüz ambara serbest bırakılmamış transfer emirlerinden gelen talepleri temel alarak malzeme çekme konumlarında stok yenilemelerine olanak tanır.</span><span class="sxs-lookup"><span data-stu-id="d6b0d-110">The *Warehouse slotting for transfer orders* feature lets warehouse managers replenish picking locations, based on demand from transfer orders that aren't yet released to the warehouse.</span></span> <span data-ttu-id="d6b0d-111">Malzeme çekme konumlarının, ambara serbest bırakıldıktan sonra transfer emirleri için gerekli olan tüm maddeleri içermesini sağlar.</span><span class="sxs-lookup"><span data-stu-id="d6b0d-111">It ensures that picking locations will include all the items that are required for the transfer orders after they are released to warehouse.</span></span> <span data-ttu-id="d6b0d-112">Bu özellik *Ambar yerleştirme* özelliğini de açmanızı gerektirir.</span><span class="sxs-lookup"><span data-stu-id="d6b0d-112">This feature requires that you also turn on the *Warehouse slotting feature* feature.</span></span>

<span data-ttu-id="d6b0d-113">*Ambar yerleştirme tahsisatı geliştirmeleri* özelliği, *Ambar yerleştirme özelliği* tarafından kullanılan şablon satırları için bir seçenek ekler.</span><span class="sxs-lookup"><span data-stu-id="d6b0d-113">The *Warehouse slotting allocation enhancements* feature adds an option for the template lines that are used by the *Warehouse slotting feature* feature.</span></span> <span data-ttu-id="d6b0d-114">Bu seçenek, sistemin bir hedef konumda var olan eldeki stoğu dikkate alabilmesini sağlar.</span><span class="sxs-lookup"><span data-stu-id="d6b0d-114">The option enables the system to consider existing on-hand inventory at a target location.</span></span> <span data-ttu-id="d6b0d-115">Bu nedenle, yerleştirme için daha az stok yenileme oluşturulabilir.</span><span class="sxs-lookup"><span data-stu-id="d6b0d-115">Therefore, fewer replenishments might be generated for slotting.</span></span> <span data-ttu-id="d6b0d-116">*Ambar yerleştirme ayırma geliştirmeleri* özelliği, *Ambar yerleştirme özelliğini* de açmanızı gerektirir.</span><span class="sxs-lookup"><span data-stu-id="d6b0d-116">The *Warehouse slotting allocation enhancements* feature requires that you also turn on the *Warehouse slotting feature* feature.</span></span> <span data-ttu-id="d6b0d-117">Bu, isteğe bağlı olarak *Transfer emirleri için ambar yerleştirme* ile birlikte kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="d6b0d-117">It can optionally be used together with the *Warehouse slotting for transfer orders* feature.</span></span>

## <a name="turn-on-the-warehouse-slotting-features"></a><span data-ttu-id="d6b0d-118">Ambar yerleştirme özelliklerini açma</span><span class="sxs-lookup"><span data-stu-id="d6b0d-118">Turn on the warehouse slotting features</span></span>

<span data-ttu-id="d6b0d-119">Özellikleri kullanabilmeniz için sisteminizde etkinleştirmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="d6b0d-119">Before you can use these features, they must be turned on in your system.</span></span> <span data-ttu-id="d6b0d-120">Yöneticiler bu özelliklerin durumunu denetlemek ve gerekirse etkinleştirmek için [özellik yönetimi](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) ayarlarını kullanabilir.</span><span class="sxs-lookup"><span data-stu-id="d6b0d-120">Admins can use the [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) settings to check the status of the features and turn them on if they are required.</span></span> <span data-ttu-id="d6b0d-121">Gerektiği şekilde aşağıdaki özellikleri açın:</span><span class="sxs-lookup"><span data-stu-id="d6b0d-121">Turn on the following features as required:</span></span>

- <span data-ttu-id="d6b0d-122">Ambar yerleştirme özelliği</span><span class="sxs-lookup"><span data-stu-id="d6b0d-122">Warehouse slotting feature</span></span>
- <span data-ttu-id="d6b0d-123">Transfer emirleri için ambar yerleştirme</span><span class="sxs-lookup"><span data-stu-id="d6b0d-123">Warehouse slotting for transfer orders</span></span>

    > [!IMPORTANT]
    > <span data-ttu-id="d6b0d-124">Bu özellikten önce *Ambar yerleştirme özelliği* açılmalıdır.</span><span class="sxs-lookup"><span data-stu-id="d6b0d-124">The *Warehouse slotting feature* feature must be turned on before this feature.</span></span>

- <span data-ttu-id="d6b0d-125">Ambar yerleştirme tahsisatı iyileştirmeleri</span><span class="sxs-lookup"><span data-stu-id="d6b0d-125">Warehouse slotting allocation enhancements</span></span>

    > [!IMPORTANT]
    > <span data-ttu-id="d6b0d-126">Bu özellikten önce *Ambar yerleştirme özelliği* açılmalıdır.</span><span class="sxs-lookup"><span data-stu-id="d6b0d-126">The *Warehouse slotting feature* feature must be turned on before this feature.</span></span>

## <a name="set-up-warehouse-slotting"></a><span data-ttu-id="d6b0d-127">Ambar yerleştirmeyi ayarlama</span><span class="sxs-lookup"><span data-stu-id="d6b0d-127">Set up warehouse slotting</span></span>

<span data-ttu-id="d6b0d-128">Ambar yerleştirmeyi kullanmak için, sisteminizde aşağıdaki öğeleri ayarlamanız gerekir:</span><span class="sxs-lookup"><span data-stu-id="d6b0d-128">To use warehouse slotting, you must set up the following elements in your system:</span></span>

- <span data-ttu-id="d6b0d-129">Yerleştirme ölçü birimi katmanları</span><span class="sxs-lookup"><span data-stu-id="d6b0d-129">Slotting unit of measure tiers</span></span>
- <span data-ttu-id="d6b0d-130">Yönerge kodları</span><span class="sxs-lookup"><span data-stu-id="d6b0d-130">Directive codes</span></span>
- <span data-ttu-id="d6b0d-131">Yerleştirme şablonları</span><span class="sxs-lookup"><span data-stu-id="d6b0d-131">Slotting templates</span></span>
- <span data-ttu-id="d6b0d-132">Konum yönergeleri</span><span class="sxs-lookup"><span data-stu-id="d6b0d-132">Location directives</span></span>

### <a name="create-unit-of-measure-tiers-for-slotting"></a><a name="unit-tiers"></a><span data-ttu-id="d6b0d-133">Yerleştirme için ölçü birimi katmanları oluşturma</span><span class="sxs-lookup"><span data-stu-id="d6b0d-133">Create unit-of-measure tiers for slotting</span></span>

<span data-ttu-id="d6b0d-134">Ölçü birimi katmanları, yerleştirme amacıyla birden fazla ölçü biriminin birlikte gruplandırılmasını sağlar.</span><span class="sxs-lookup"><span data-stu-id="d6b0d-134">Unit-of-measure tiers enable multiple units of measure to be grouped together for the purposes of slotting.</span></span> <span data-ttu-id="d6b0d-135">Örneğin aynı kutu çekme alanından birden fazla kutu boyutu çekiliyorsa, tüm boyutlar için bir katman oluşturulabilir.</span><span class="sxs-lookup"><span data-stu-id="d6b0d-135">For example, if multiple sizes of boxes are all picked from the same box picking area, one tier can be created for all the sizes.</span></span> <span data-ttu-id="d6b0d-136">**Katmanın parçası olması gereken her ölçü birimi için bir satır oluşturulmalıdır.**</span><span class="sxs-lookup"><span data-stu-id="d6b0d-136">**A line must be created for each unit of measure that should be part of the tier.**</span></span>

1. <span data-ttu-id="d6b0d-137">**Ambar yönetimi \> Kurulum \> Stok yenileme \> Yerleştirme ölçü birimi katmanları**'na gidin.</span><span class="sxs-lookup"><span data-stu-id="d6b0d-137">Go to **Warehouse management \> Setup \> Replenishment \> Slotting unit of measure tiers**.</span></span>
1. <span data-ttu-id="d6b0d-138">**Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="d6b0d-138">Select **New**.</span></span>
1. <span data-ttu-id="d6b0d-139">Üst bilgide aşağıdaki değerleri ayarlayın:</span><span class="sxs-lookup"><span data-stu-id="d6b0d-139">In the header, set the following values:</span></span>

    - <span data-ttu-id="d6b0d-140">**Ölçü birimi katmanı:** *HerKutuPl*</span><span class="sxs-lookup"><span data-stu-id="d6b0d-140">**Unit of measure tier:** *EaBoxPl*</span></span>
    - <span data-ttu-id="d6b0d-141">**Açıklama:** *Her kutu paleti*</span><span class="sxs-lookup"><span data-stu-id="d6b0d-141">**Description:** *Each box pallet*</span></span>

1. <span data-ttu-id="d6b0d-142">**Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="d6b0d-142">Select **Save**.</span></span>
1. <span data-ttu-id="d6b0d-143">**Ölçü birimi** hızlı sekmesinde, kılavuza satır eklemek için **Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="d6b0d-143">On the **Units of measure** FastTab, select **New** to add a line to the grid.</span></span>
1. <span data-ttu-id="d6b0d-144">Yeni satırda aşağıdaki değerleri ayarlayın:</span><span class="sxs-lookup"><span data-stu-id="d6b0d-144">On the new line, set the following values:</span></span>

    - <span data-ttu-id="d6b0d-145">**Birim:** *Kutu*</span><span class="sxs-lookup"><span data-stu-id="d6b0d-145">**Unit:** *Box*</span></span>
    - <span data-ttu-id="d6b0d-146">**Açıklama:** Bu alanı boş bırakın.</span><span class="sxs-lookup"><span data-stu-id="d6b0d-146">**Description:** Leave this field blank.</span></span> <span data-ttu-id="d6b0d-147">Değişikliklerinizi kaydettiğiniz zaman otomatik olarak doldurulur.</span><span class="sxs-lookup"><span data-stu-id="d6b0d-147">It will be filled in automatically when you save your changes.</span></span>
    - <span data-ttu-id="d6b0d-148">**Birim sınıfı:** *Miktar*</span><span class="sxs-lookup"><span data-stu-id="d6b0d-148">**Unit class:** *Quantity*</span></span>

1. <span data-ttu-id="d6b0d-149">Kılavuza ikinci bir satır eklemek için **Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="d6b0d-149">Select **New** to add a second line to the grid.</span></span>
1. <span data-ttu-id="d6b0d-150">Yeni satırda aşağıdaki değerleri ayarlayın:</span><span class="sxs-lookup"><span data-stu-id="d6b0d-150">On the new line, set the following values:</span></span>

    - <span data-ttu-id="d6b0d-151">**Birim:** *ea*</span><span class="sxs-lookup"><span data-stu-id="d6b0d-151">**Unit:** *ea*</span></span>
    - <span data-ttu-id="d6b0d-152">**Açıklama:** Bu alanı boş bırakın.</span><span class="sxs-lookup"><span data-stu-id="d6b0d-152">**Description:** Leave this field blank.</span></span> <span data-ttu-id="d6b0d-153">Değişikliklerinizi kaydettiğiniz zaman otomatik olarak doldurulur.</span><span class="sxs-lookup"><span data-stu-id="d6b0d-153">It will be filled in automatically when you save your changes.</span></span>
    - <span data-ttu-id="d6b0d-154">**Birim sınıfı:** *Miktar*</span><span class="sxs-lookup"><span data-stu-id="d6b0d-154">**Unit class:** *Quantity*</span></span>

1. <span data-ttu-id="d6b0d-155">Kılavuza üçüncü bir satır eklemek için **Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="d6b0d-155">Select **New** to add a third line to the grid.</span></span>
1. <span data-ttu-id="d6b0d-156">Yeni satırda aşağıdaki değerleri ayarlayın:</span><span class="sxs-lookup"><span data-stu-id="d6b0d-156">On the new line, set the following values:</span></span>

    - <span data-ttu-id="d6b0d-157">**Birim:** *PL*</span><span class="sxs-lookup"><span data-stu-id="d6b0d-157">**Unit:** *PL*</span></span>
    - <span data-ttu-id="d6b0d-158">**Açıklama:** Bu alanı boş bırakın.</span><span class="sxs-lookup"><span data-stu-id="d6b0d-158">**Description:** Leave this field blank.</span></span> <span data-ttu-id="d6b0d-159">Değişikliklerinizi kaydettiğiniz zaman otomatik olarak doldurulur.</span><span class="sxs-lookup"><span data-stu-id="d6b0d-159">It will be filled in automatically when you save your changes.</span></span>
    - <span data-ttu-id="d6b0d-160">**Birim sınıfı:** *Miktar*</span><span class="sxs-lookup"><span data-stu-id="d6b0d-160">**Unit class:** *Quantity*</span></span>

1. <span data-ttu-id="d6b0d-161">Katmanı kaydetmek için **Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="d6b0d-161">Select **Save** to save the tier.</span></span>

### <a name="create-a-directive-code-for-slotting"></a><span data-ttu-id="d6b0d-162">Yerleştirme için yönerge kodu oluşturma</span><span class="sxs-lookup"><span data-stu-id="d6b0d-162">Create a directive code for slotting</span></span>

<span data-ttu-id="d6b0d-163">Bir şablonla ilişkilendirilmesi gereken yönerge kodunu seçmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="d6b0d-163">You must select the directive code that should be associated with a template.</span></span>

1. <span data-ttu-id="d6b0d-164">**Ambar yönetimi \> Kurulum \> Yönerge kodları**'na gidin.</span><span class="sxs-lookup"><span data-stu-id="d6b0d-164">Go to **Warehouse management \> Setup \> Directive codes**.</span></span>
1. <span data-ttu-id="d6b0d-165">Eylem Bölmesinde, **Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="d6b0d-165">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="d6b0d-166">**Yönerge kodu** alanına, *Yerleştirme* girin.</span><span class="sxs-lookup"><span data-stu-id="d6b0d-166">In the **Directive code** field, enter *Slotting*.</span></span>
1. <span data-ttu-id="d6b0d-167">**Yönerge açıklaması** alanına, *Yerleştirme* girin.</span><span class="sxs-lookup"><span data-stu-id="d6b0d-167">In the **Directive description** field, enter *Slotting*.</span></span>

### <a name="set-up-slotting-templates"></a><span data-ttu-id="d6b0d-168">Yerleştirme şablonlarını ayarlama</span><span class="sxs-lookup"><span data-stu-id="d6b0d-168">Set up slotting templates</span></span>

<span data-ttu-id="d6b0d-169">Her yerleştirme şablonu, stokun belirli bir ambar için yerleşimlere nasıl atandığını denetler.</span><span class="sxs-lookup"><span data-stu-id="d6b0d-169">Each slotting template controls how inventory is assigned to locations for a specific warehouse.</span></span> <span data-ttu-id="d6b0d-170">Her şablon her bir yerleştirme belirtimi için bir satır içermelidir.</span><span class="sxs-lookup"><span data-stu-id="d6b0d-170">Each template must include a line for each slotting specification.</span></span> <span data-ttu-id="d6b0d-171">Yerleştirme şablonlarını ayarlamak için bu bölümdeki yordamları kullanın.</span><span class="sxs-lookup"><span data-stu-id="d6b0d-171">Use the procedures in this section to set up slotting templates.</span></span>

1. <span data-ttu-id="d6b0d-172">**Ambar yönetimi \> Kurulum \> Stok yenileme \> Yerleştirme şablonları**'na gidin.</span><span class="sxs-lookup"><span data-stu-id="d6b0d-172">Go to **Warehouse management \> Setup \> Replenishment \> Slotting templates**.</span></span>
1. <span data-ttu-id="d6b0d-173">Şablon oluşturmak için **Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="d6b0d-173">Select **New** to create a template.</span></span>

<span data-ttu-id="d6b0d-174">Ardından, aşağıdaki alt bölümlerde anlatıldığı gibi, şablon üst bilgisini, yerleştirme belirtimlerini ve yerleşim yönergelerini ayarlamanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="d6b0d-174">Next, you must set up the template header, slotting specifications, and location directives, as explained in the following subsections.</span></span> <span data-ttu-id="d6b0d-175">Transfer emirlerinin yerleştirilmesine yönelik kurulum, satış siparişlerinin yerleştirilmesine yönelik kuruluma benzerdir ancak **Talep türü** alanı *Satış siparişi* yerine *Transfer emirleri* olarak ayarlanır.</span><span class="sxs-lookup"><span data-stu-id="d6b0d-175">The setup for slotting for transfer orders resembles the setup for slotting for sales orders, but the **Demand type** field is set *Transfer orders* instead of *Sales order*.</span></span>

#### <a name="set-up-the-header-for-a-sales-order-slotting-template"></a><span data-ttu-id="d6b0d-176">Satış siparişi yerleştirme şablonu için başlığı ayarlama</span><span class="sxs-lookup"><span data-stu-id="d6b0d-176">Set up the header for a sales order slotting template</span></span>

1. <span data-ttu-id="d6b0d-177">Şablonun üst bilgisinde aşağıdaki değerleri ayarlayın:</span><span class="sxs-lookup"><span data-stu-id="d6b0d-177">In the header for the template, set the following values:</span></span>

    - <span data-ttu-id="d6b0d-178">**Yerleştirme şablonu:** _61_</span><span class="sxs-lookup"><span data-stu-id="d6b0d-178">**Slotting template:** _61_</span></span>
    - <span data-ttu-id="d6b0d-179">**Açıklama:** _61_</span><span class="sxs-lookup"><span data-stu-id="d6b0d-179">**Description:** _61_</span></span>
    - <span data-ttu-id="d6b0d-180">**Talep türü:** *Satış siparişi*</span><span class="sxs-lookup"><span data-stu-id="d6b0d-180">**Demand type:** *Sales order*</span></span>

        > [!NOTE]
        > <span data-ttu-id="d6b0d-181">Şu anda, *Satış siparişleri* ve *Transfer emirleri*, desteklenen tek talep türleridir.</span><span class="sxs-lookup"><span data-stu-id="d6b0d-181">Currently, *Sales orders* and *Transfer orders* are the only demand types that are supported.</span></span> <span data-ttu-id="d6b0d-182">*Transfer emirlerini* yalnızca *Transfer emirleri için ambar yerleştirme* özelliği açık olduğunda seçebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="d6b0d-182">You can select *Transfer orders* only if the *Warehouse Slotting for transfer orders* feature is turned on.</span></span>

    - <span data-ttu-id="d6b0d-183">**Talep stratejisi:** _Sipariş edilen_</span><span class="sxs-lookup"><span data-stu-id="d6b0d-183">**Demand strategy:** _Ordered_</span></span>

        <span data-ttu-id="d6b0d-184">Bu alanda aşağıdaki değerler kullanılabilir:</span><span class="sxs-lookup"><span data-stu-id="d6b0d-184">The following values are available in this field:</span></span>

        - <span data-ttu-id="d6b0d-185">**Sipariş edilen** – Satış siparişindeki tam sipariş edilen miktar talep olarak kabul edilecektir.</span><span class="sxs-lookup"><span data-stu-id="d6b0d-185">**Ordered** – The full ordered quantity on the sales order should be considered demand.</span></span>
        - <span data-ttu-id="d6b0d-186">**Rezerve** – Yalnızca rezerve edilen (fiziksel ve sipariş edilen) satış siparişi satırı miktarları talep olarak kabul edilecektir.</span><span class="sxs-lookup"><span data-stu-id="d6b0d-186">**Reserved** – Only the sales order line quantities that are reserved (physical and ordered) should be considered demand.</span></span>
        - <span data-ttu-id="d6b0d-187">**Serbest bırakıldı**: Serbest bırakılan miktar talep olarak kabul edilmelidir.</span><span class="sxs-lookup"><span data-stu-id="d6b0d-187">**Released** – The released quantity should be considered demand.</span></span>

    - <span data-ttu-id="d6b0d-188">**Ambar:** _61_</span><span class="sxs-lookup"><span data-stu-id="d6b0d-188">**Warehouse:** _61_</span></span>
    - <span data-ttu-id="d6b0d-189">**Dalga talebinin rezerve edilmemiş miktarları kullanmasına izin ver:** _Evet_</span><span class="sxs-lookup"><span data-stu-id="d6b0d-189">**Allow wave demand to use unreserved quantities:** _Yes_</span></span>

<span data-ttu-id="d6b0d-190">Değerlendirilen talebin kapsamını daraltmak için bir sorgu da belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="d6b0d-190">You can also specify a query to narrow the scope of the demand that is evaluated.</span></span>

#### <a name="set-up-slotting-specifications-for-each-template"></a><span data-ttu-id="d6b0d-191">Her şablon için yerleştirme belirtimlerini ayarlama</span><span class="sxs-lookup"><span data-stu-id="d6b0d-191">Set up slotting specifications for each template</span></span>

<span data-ttu-id="d6b0d-192">Oluşturduğunuz her satış siparişi şablonu için, her yerleştirme belirtimi için bir satır eklemek üzere aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="d6b0d-192">For each sales order template that you create, follow these steps to add a line for each slotting specification.</span></span>

1. <span data-ttu-id="d6b0d-193">**Yerleştirme şablonu ayrıntıları** hızlı sekmesinde, şablon satırı oluşturmak için **Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="d6b0d-193">On the **Slotting template details** FastTab, select **New** to create a template line.</span></span>
1. <span data-ttu-id="d6b0d-194">Yeni satırda aşağıdaki değerleri ayarlayın:</span><span class="sxs-lookup"><span data-stu-id="d6b0d-194">On the new line, set the following values:</span></span>

    - <span data-ttu-id="d6b0d-195">**Sıra:** _1_</span><span class="sxs-lookup"><span data-stu-id="d6b0d-195">**Sequence:** _1_</span></span>
    - <span data-ttu-id="d6b0d-196">**Açıklama:** _Sabit yerleşim_</span><span class="sxs-lookup"><span data-stu-id="d6b0d-196">**Description:** _Fixed location_</span></span>
    - <span data-ttu-id="d6b0d-197">**Minimum miktar:** _1_</span><span class="sxs-lookup"><span data-stu-id="d6b0d-197">**Minimum quantity:** _1_</span></span>

        <span data-ttu-id="d6b0d-198">Bu alan, satır için gereken minimum talep miktarını tanımlar.</span><span class="sxs-lookup"><span data-stu-id="d6b0d-198">This field defines the minimum quantity of demand that is required for the line.</span></span>

    - <span data-ttu-id="d6b0d-199">**Maksimum miktar:** _1000000_</span><span class="sxs-lookup"><span data-stu-id="d6b0d-199">**Maximum quantity:** _1000000_</span></span>

        <span data-ttu-id="d6b0d-200">Bu alan, satır için geçerli olan maksimum talep miktarını tanımlar.</span><span class="sxs-lookup"><span data-stu-id="d6b0d-200">This field defines the maximum quantity of demand that is valid for the line.</span></span>

    - <span data-ttu-id="d6b0d-201">**Birim:** Bu alanı boş bırakın.</span><span class="sxs-lookup"><span data-stu-id="d6b0d-201">**Unit:** Leave this field blank.</span></span>

        <span data-ttu-id="d6b0d-202">Bu alan, minimum ve maksimum miktarların başvuruda bulunduğu ölçü birimini tanımlar.</span><span class="sxs-lookup"><span data-stu-id="d6b0d-202">This field defines the unit of measure that the minimum and maximum quantities refer to.</span></span>

    - <span data-ttu-id="d6b0d-203">**Ölçü Birimi Katmanı:** _HerKutuPl_</span><span class="sxs-lookup"><span data-stu-id="d6b0d-203">**Unit of Measure Tier:** _EaBoxPl_</span></span>

        <span data-ttu-id="d6b0d-204">Bu alan, satır için geçerli olan talebin ölçü birimlerini tanımlar.</span><span class="sxs-lookup"><span data-stu-id="d6b0d-204">This field defines the units of measure of demand that are valid for the line.</span></span> <span data-ttu-id="d6b0d-205">(Daha fazla bilgi için bu konuda daha önce işlenen [Yerleştirme için ölçü birimi katmanlarını ayarlama](#unit-tiers) bölümüne bakın.)</span><span class="sxs-lookup"><span data-stu-id="d6b0d-205">(For more information, see the [Set up unit-of-measure tiers for slotting](#unit-tiers) section earlier in this topic.)</span></span>

    - <span data-ttu-id="d6b0d-206">**Yerleştirme atama ölçütü:** _Miktarı dikkate al_</span><span class="sxs-lookup"><span data-stu-id="d6b0d-206">**Assign slot criteria:** _Consider qty_</span></span>

        <span data-ttu-id="d6b0d-207">Bu alanda aşağıdaki değerler kullanılabilir:</span><span class="sxs-lookup"><span data-stu-id="d6b0d-207">The following values are available in this field:</span></span>

        - <span data-ttu-id="d6b0d-208">**Boş kabul et** – Bu sistem, malzeme çekme alanındaki tüm yerleşimlerin boş olduğunu varsayacak ve bu yerleşimlerde stok denetimi yapmayacaktır.</span><span class="sxs-lookup"><span data-stu-id="d6b0d-208">**Assume empty** – This system should assume that all locations in the picking area are empty and should not check those locations for inventory.</span></span>
        - <span data-ttu-id="d6b0d-209">**Miktarı dikkate al** – Sistem, malzeme çekme alanındaki tüm yerleşimlerde stok denetimi yapacak ve boş olmayan yerleşimleri atlayacaktır.</span><span class="sxs-lookup"><span data-stu-id="d6b0d-209">**Consider qty** – The system should check the locations in the picking area for inventory and should skip any locations that aren't empty.</span></span>
        - <span data-ttu-id="d6b0d-210">**Eldeki stok miktarını dikkate al**: Sistem, herhangi bir hedef konumun talep satırındaki madde için rezerve edilmemiş miktarlar içerip içermediğini denetlemelidir.</span><span class="sxs-lookup"><span data-stu-id="d6b0d-210">**Consider on-hand** – The system should check whether any target location contains unreserved quantities for the item on the demand line.</span></span> <span data-ttu-id="d6b0d-211">Miktar, talep satırındaki en az bir birimi karşılayabilecek büyüklükte ise oluşturulan yerleştirme planı kaydı, kullanılabilir tutar kadar azaltılır.</span><span class="sxs-lookup"><span data-stu-id="d6b0d-211">If the quantity is large enough to satisfy at least one unit of the demand line, the generated slotting plan record is reduced by the available amount.</span></span> <span data-ttu-id="d6b0d-212">Örneğin, talep 10 servis talebi ise ve elde bir servis talebi varsa bulunan talep, dokuz servis talebi olacaktır.</span><span class="sxs-lookup"><span data-stu-id="d6b0d-212">For example, if the demand is 10 cases, and one case is on hand, the located demand will be nine cases.</span></span> <span data-ttu-id="d6b0d-213">Talep 10 servis talebi ise ve her bir servis talebi eldeyse, bulunan talep, 10 servis talebi olacaktır.</span><span class="sxs-lookup"><span data-stu-id="d6b0d-213">If the demand is 10 cases, and one each is on hand, the located demand will be 10 cases.</span></span> <span data-ttu-id="d6b0d-214">Bu değer yalnızca *Ambar yerleştirme tahsisatı geliştirmeleri* özelliği açık olduğunda kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="d6b0d-214">This value is available only when the *Warehouse slotting allocation enhancements* feature is turned on.</span></span>

    - <span data-ttu-id="d6b0d-215">**Yönerge kodu:** _Yerleştirme_</span><span class="sxs-lookup"><span data-stu-id="d6b0d-215">**Directive code:** _Slotting_</span></span>

        <span data-ttu-id="d6b0d-216">Bu alan, stok yenileme işinin malzeme çekme yerleşimini bulmak için kullanılan yerleşim yönergesini tanımlar.</span><span class="sxs-lookup"><span data-stu-id="d6b0d-216">This field defines the location directive that is used to find the picking location of the replenishment work.</span></span>

    - <span data-ttu-id="d6b0d-217">**Taşma konumu:** Bu alanı boş bırakın.</span><span class="sxs-lookup"><span data-stu-id="d6b0d-217">**Overflow location:** Leave this field blank.</span></span>

        <span data-ttu-id="d6b0d-218">Bu alan, satırın işlendiği sırada miktar için bir yerleşim bulunamazsa, stokun koyulacağı yerleşimi tanımlar.</span><span class="sxs-lookup"><span data-stu-id="d6b0d-218">This field defines the location that inventory that is put to if a location can't be found for the quantity when the line is processed.</span></span>

    - <span data-ttu-id="d6b0d-219">**Araya izin ver:** _Evet_</span><span class="sxs-lookup"><span data-stu-id="d6b0d-219">**Allow let up:** _Yes_</span></span>

        <span data-ttu-id="d6b0d-220">Bu seçenek *Evet* olarak ayarlandığında, herhangi bir talep yerleştirilemezse, stok bulunan ama yerleştirme yapılmayan yerleşimlerden dışarıya stok çekmek için hareket işi oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="d6b0d-220">When this option is set to *Yes*, if any demand can't be slotted, movement work will be created to take inventory out of locations where there is inventory, but where nothing was slotted.</span></span> <span data-ttu-id="d6b0d-221">Bunun üzerine şablon yeniden çalıştırılır.</span><span class="sxs-lookup"><span data-stu-id="d6b0d-221">The template is then run again.</span></span> <span data-ttu-id="d6b0d-222">Bu kez, yerleşimlerdeki stoku yok sayar.</span><span class="sxs-lookup"><span data-stu-id="d6b0d-222">This time, it ignores the inventory in the locations.</span></span> <span data-ttu-id="d6b0d-223">Bu işlevsellik en iyi şekilde, **Yerleştirme atama ölçütü** alanı _Miktarı dikkate al_ olarak ayarlandığı zaman çalışır.</span><span class="sxs-lookup"><span data-stu-id="d6b0d-223">This functionality works best when the **Assign slot criteria** field is set to _Consider qty_.</span></span>

    - <span data-ttu-id="d6b0d-224">**Sabit yerleşim kullanımı:** _Ürün için yalnızca sabit yerleşimler_</span><span class="sxs-lookup"><span data-stu-id="d6b0d-224">**Fixed location usage:** _Only fixed locations for the product_</span></span>

        <span data-ttu-id="d6b0d-225">Bu alanda aşağıdaki değerler kullanılabilir:</span><span class="sxs-lookup"><span data-stu-id="d6b0d-225">The following values are available in this field:</span></span>

        - <span data-ttu-id="d6b0d-226">**Sabit ve sabit olmayan yerleşimler** – Sistem sabit yerleşimleri kullanmayla sınırlı kalmaz.</span><span class="sxs-lookup"><span data-stu-id="d6b0d-226">**Fixed and non-fixed locations** – The system should not be limited to using only fixed locations.</span></span>
        - <span data-ttu-id="d6b0d-227">**Ürün için yalnızca sabit yerleşimler** – Sistem ürün için yalnızca sabit yerleşimler olan yerleşimlere yerleştirme yapar.</span><span class="sxs-lookup"><span data-stu-id="d6b0d-227">**Only fixed locations for the product** – The system should slot only to locations that are fixed locations for the product.</span></span>
        - <span data-ttu-id="d6b0d-228">**Ürün çeşidi için yalnızca sabit yerleşimler** – Sistem ürün çeşidi için yalnızca sabit yerleşimler olan yerleşimlere yerleştirme yapar.</span><span class="sxs-lookup"><span data-stu-id="d6b0d-228">**Only fixed locations for the product variant** – The system should slot only to locations that are fixed locations for the product variant.</span></span>

> [!NOTE]
> <span data-ttu-id="d6b0d-229">Yerleştirme şablonunda, **Yerleştirme ölçütü ata** alanının *Eldeki miktarı dikkate al* olarak ayarlandığı en az bir satır varsa, bu şablondaki hiçbir satırda ara işlerine artık izin verilmez.</span><span class="sxs-lookup"><span data-stu-id="d6b0d-229">If the slotting template contains at least one line where the **Assign slot criteria** field is set to *Consider on-hand*, let-ups are no longer allowed for any line in the template.</span></span>

1. <span data-ttu-id="d6b0d-230">**Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="d6b0d-230">Select **Save**.</span></span>
1. <span data-ttu-id="d6b0d-231">İkinci bir şablon satırı oluşturmak için **Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="d6b0d-231">Select **New** to create a second template line.</span></span>
1. <span data-ttu-id="d6b0d-232">Yeni satırda aşağıdaki değerleri ayarlayın:</span><span class="sxs-lookup"><span data-stu-id="d6b0d-232">On the new line, set the following values:</span></span>

    - <span data-ttu-id="d6b0d-233">**Sıra:** _2_</span><span class="sxs-lookup"><span data-stu-id="d6b0d-233">**Sequence:** _2_</span></span>
    - <span data-ttu-id="d6b0d-234">**Açıklama:** _Diğer_</span><span class="sxs-lookup"><span data-stu-id="d6b0d-234">**Description:** _Other_</span></span>
    - <span data-ttu-id="d6b0d-235">**Minimum Miktar:** _1_</span><span class="sxs-lookup"><span data-stu-id="d6b0d-235">**Minimum Qty:** _1_</span></span>
    - <span data-ttu-id="d6b0d-236">**Maksimum Miktar:** _1000000_</span><span class="sxs-lookup"><span data-stu-id="d6b0d-236">**Maximum Qty:** _1000000_</span></span>
    - <span data-ttu-id="d6b0d-237">**Birim:** Bu alanı boş bırakın.</span><span class="sxs-lookup"><span data-stu-id="d6b0d-237">**Unit:** Leave this field blank.</span></span>
    - <span data-ttu-id="d6b0d-238">**Ölçü birimi katmanı:** _HerKutuPl_</span><span class="sxs-lookup"><span data-stu-id="d6b0d-238">**Unit of measure tier:** _EaBoxPl_</span></span>
    - <span data-ttu-id="d6b0d-239">**Yerleştirme atama ölçütü:** _Miktarı dikkate al_</span><span class="sxs-lookup"><span data-stu-id="d6b0d-239">**Assign slot criteria:** _Consider qty_</span></span>
    - <span data-ttu-id="d6b0d-240">**Yönerge kodu:** _Yerleştirme_</span><span class="sxs-lookup"><span data-stu-id="d6b0d-240">**Directive code:** _Slotting_</span></span>
    - <span data-ttu-id="d6b0d-241">**Taşma konumu:** Bu alanı boş bırakın.</span><span class="sxs-lookup"><span data-stu-id="d6b0d-241">**Overflow location:** Leave this field blank.</span></span>
    - <span data-ttu-id="d6b0d-242">**Araya izin ver:** _Evet_</span><span class="sxs-lookup"><span data-stu-id="d6b0d-242">**Allow let up:** _Yes_</span></span>
    - <span data-ttu-id="d6b0d-243">**Sabit yerleşimleri kullan:** _Sabit ve sabit olmayan yerleşimler_</span><span class="sxs-lookup"><span data-stu-id="d6b0d-243">**Use fixed locations:** _Fixed and non-fixed locations_</span></span>

    <span data-ttu-id="d6b0d-244">İkinci satır için sorguda, o satırla ilgili talebin yerleştirilebileceği yerleşimleri belirlemek için kullanılan ölçütleri belirtirsiniz.</span><span class="sxs-lookup"><span data-stu-id="d6b0d-244">In the query for the second line, you will now specify the criteria that are used to determine what locations the demand for that line can be slotted to.</span></span>

1. <span data-ttu-id="d6b0d-245">**Sıra** alanının *2* olarak ayarlandığı satırı seçin.</span><span class="sxs-lookup"><span data-stu-id="d6b0d-245">Select the line where the **Sequence** field is set to *2*.</span></span>
1. <span data-ttu-id="d6b0d-246">**Sorguyu düzenle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="d6b0d-246">Select **Edit query**.</span></span>
1. <span data-ttu-id="d6b0d-247">**Aralık** sekmesinde, kılavuza satır eklemek için **Ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="d6b0d-247">On the **Range** tab, select **Add** to add a line to the grid.</span></span>
1. <span data-ttu-id="d6b0d-248">Yeni satırda aşağıdaki değerleri ayarlayın:</span><span class="sxs-lookup"><span data-stu-id="d6b0d-248">On the new line, set the following values:</span></span>

    - <span data-ttu-id="d6b0d-249">**Tablo:** *Yerleşimler*</span><span class="sxs-lookup"><span data-stu-id="d6b0d-249">**Table:** *Locations*</span></span>
    - <span data-ttu-id="d6b0d-250">**Türetilmiş tablo:** *Yerleşimler*</span><span class="sxs-lookup"><span data-stu-id="d6b0d-250">**Derived table:** *Locations*</span></span>
    - <span data-ttu-id="d6b0d-251">**Alan:** *Yerleşim profili kodu*</span><span class="sxs-lookup"><span data-stu-id="d6b0d-251">**Field:** *Location profile ID*</span></span>
    - <span data-ttu-id="d6b0d-252">**Ölçüt:** *Malzeme Çekme-06* (Listeyi genişletmek için alandaki çift artı işaretini \[**++**\] ve ardından *Malzeme Çekme-06* - *Malzeme Çekme Tesisi 6*'yı seçin.)</span><span class="sxs-lookup"><span data-stu-id="d6b0d-252">**Criteria:** *Pick-06* (Select the double plus sign \[**++**\] in the field to expand the list, and then select *Pick-06* - *Picking Site 6*.)</span></span>

1. <span data-ttu-id="d6b0d-253">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="d6b0d-253">Select **OK**.</span></span>

#### <a name="set-up-location-directives"></a><span data-ttu-id="d6b0d-254">Yerleşim yönergelerini kur</span><span class="sxs-lookup"><span data-stu-id="d6b0d-254">Set up location directives</span></span>

<span data-ttu-id="d6b0d-255">Yerleştirme çekme işlemlerini destekleyecek en az bir yerleştirme yönergesi ayarlanmalıdır.</span><span class="sxs-lookup"><span data-stu-id="d6b0d-255">At least one location directive must be set up to support slotting picks.</span></span> <span data-ttu-id="d6b0d-256">Yerleştirme çekme işlemleri için yeni bir *stok yenileme yerleşimi yönergesi* ayarlamak için bu bölümdeki yordamları kullanın.</span><span class="sxs-lookup"><span data-stu-id="d6b0d-256">Use the procedures in this section to set up a new *replenishment location directive* for slotting picks.</span></span>

1. <span data-ttu-id="d6b0d-257">**Ambar Yönetimi \> Kurulum \> Konum yönergeleri** seçeneğine gidin.</span><span class="sxs-lookup"><span data-stu-id="d6b0d-257">Go to **Warehouse management \> Setup \> Location directives**.</span></span>
1. <span data-ttu-id="d6b0d-258">Sol bölmedeki **İş emri türü** alanında *Stok yenileme*'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="d6b0d-258">In the left pane, in the **Work order type** field, select *Replenishment*.</span></span>
1. <span data-ttu-id="d6b0d-259">Eylem Bölmesinde, **Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="d6b0d-259">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="d6b0d-260">Yeni yerleşim yönergesinin üst bilgisindeki **Ad** alanına *61 Yerleştirme çekme işlemi* girin.</span><span class="sxs-lookup"><span data-stu-id="d6b0d-260">In the header for the new location directive, in the **Name** field, enter *61 Slotting pick*.</span></span>
1. <span data-ttu-id="d6b0d-261">**Sıra numarası** alanındaki varsayılan değeri kabul edin.</span><span class="sxs-lookup"><span data-stu-id="d6b0d-261">In the **Sequence number** field, accept the default value.</span></span>

##### <a name="configure-the-location-directives-fasttab"></a><span data-ttu-id="d6b0d-262">Yerleşim yönergeleri hızlı sekmesini yapılandırma</span><span class="sxs-lookup"><span data-stu-id="d6b0d-262">Configure the Location directives FastTab</span></span>

1. <span data-ttu-id="d6b0d-263">**Yerleşim yönergeleri** hızlı sekmesinde aşağıdaki değerleri ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="d6b0d-263">On the **Location directives** FastTab, set the following values.</span></span> <span data-ttu-id="d6b0d-264">Tüm diğer alanlar için varsayılan değerleri kabul edin.</span><span class="sxs-lookup"><span data-stu-id="d6b0d-264">Accept the default values for all other fields.</span></span>

    - <span data-ttu-id="d6b0d-265">**İş türü:** _Çekme_</span><span class="sxs-lookup"><span data-stu-id="d6b0d-265">**Work type:** _Pick_</span></span>
    - <span data-ttu-id="d6b0d-266">**Tesis:** _6_</span><span class="sxs-lookup"><span data-stu-id="d6b0d-266">**Site:** _6_</span></span>
    - <span data-ttu-id="d6b0d-267">**Ambar:** _61_</span><span class="sxs-lookup"><span data-stu-id="d6b0d-267">**Warehouse:** _61_</span></span>
    - <span data-ttu-id="d6b0d-268">**Yönerge kodu:** _Yerleştirme_</span><span class="sxs-lookup"><span data-stu-id="d6b0d-268">**Directive code:** _Slotting_</span></span>

1. <span data-ttu-id="d6b0d-269">**Satırlar** hızlı sekmesini kullanılabilir hale getirmek için **Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="d6b0d-269">Select **Save** to make the **Lines** FastTab available.</span></span>

##### <a name="configure-the-lines-fasttab"></a><span data-ttu-id="d6b0d-270">Satırlar hızlı sekmesini yapılandırma</span><span class="sxs-lookup"><span data-stu-id="d6b0d-270">Configure the Lines FastTab</span></span>

1. <span data-ttu-id="d6b0d-271">**Satırlar** hızlı sekmesinde yeni bir satır oluşturmak için **Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="d6b0d-271">On the **Lines** FastTab, select **New** to create a line.</span></span>
1. <span data-ttu-id="d6b0d-272">Yeni satırda aşağıdaki değerleri ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="d6b0d-272">On the new line, set the following values.</span></span>

    - <span data-ttu-id="d6b0d-273">**Başlangıç miktarı:** _0_</span><span class="sxs-lookup"><span data-stu-id="d6b0d-273">**From quantity:** _0_</span></span>
    - <span data-ttu-id="d6b0d-274">**Son miktar:** _1000000_</span><span class="sxs-lookup"><span data-stu-id="d6b0d-274">**To quantity:** _1000000_</span></span>

1. <span data-ttu-id="d6b0d-275">Kalan alanlar için varsayılan değerleri kabul edin.</span><span class="sxs-lookup"><span data-stu-id="d6b0d-275">Accept the default values for the remaining fields.</span></span>
1. <span data-ttu-id="d6b0d-276">**Yerleşim Yönergesi Eylemleri** hızlı sekmesini kullanılabilir hale getirmek için **Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="d6b0d-276">Select **Save** to make the **Location Directive Actions** FastTab available.</span></span>

##### <a name="configure-the-location-directive-actions-fasttab"></a><span data-ttu-id="d6b0d-277">Yerleşim Yönergesi Eylemleri hızlı sekmesini yapılandırma</span><span class="sxs-lookup"><span data-stu-id="d6b0d-277">Configure the Location Directive Actions FastTab</span></span>

1. <span data-ttu-id="d6b0d-278">**Yerleşim Yönergesi Eylemleri** hızlı sekmesinde yeni bir satır oluşturmak için **Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="d6b0d-278">On the **Location Directive Actions** FastTab, select **New** to create a line.</span></span>
1. <span data-ttu-id="d6b0d-279">Yeni satırda aşağıdaki değerleri ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="d6b0d-279">On the new line, set the following values.</span></span> <span data-ttu-id="d6b0d-280">Tüm diğer alanlar için varsayılan değerleri kabul edin.</span><span class="sxs-lookup"><span data-stu-id="d6b0d-280">Accept the default values for all other fields.</span></span>

    - <span data-ttu-id="d6b0d-281">**Sıra numarası:** Varsayılan değeri kabul edin.</span><span class="sxs-lookup"><span data-stu-id="d6b0d-281">**Sequence number:** Accept the default value.</span></span>
    - <span data-ttu-id="d6b0d-282">**Ad:** _Toplu_</span><span class="sxs-lookup"><span data-stu-id="d6b0d-282">**Name:** _Bulk_</span></span>
    - <span data-ttu-id="d6b0d-283">**Strateji:** _Yok_</span><span class="sxs-lookup"><span data-stu-id="d6b0d-283">**Strategy:** _None_</span></span>

1. <span data-ttu-id="d6b0d-284">Kalan alanlar için varsayılan değerleri kabul edin.</span><span class="sxs-lookup"><span data-stu-id="d6b0d-284">Accept the default values for the remaining fields.</span></span>
1. <span data-ttu-id="d6b0d-285">**Sorguyu düzenle** düğmesini kullanılabilir hale getirmek için **Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="d6b0d-285">Select **Save** to make the **Edit query** button available.</span></span>

##### <a name="edit-the-query"></a><span data-ttu-id="d6b0d-286">Sorguyu düzenleme</span><span class="sxs-lookup"><span data-stu-id="d6b0d-286">Edit the query</span></span>

1. <span data-ttu-id="d6b0d-287">**Yerleşim Yönergesi Eylemleri** hızlı sekmesinde **Sorguyu düzenle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="d6b0d-287">On the **Location Directive Actions** FastTab, select **Edit query**.</span></span>
1. <span data-ttu-id="d6b0d-288">**Aralık** sekmesinde, kılavuza satır eklemek için **Ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="d6b0d-288">On the **Range** tab, select **Add** to add a line to the grid.</span></span>
1. <span data-ttu-id="d6b0d-289">Yeni satırda aşağıdaki değerleri ayarlayın:</span><span class="sxs-lookup"><span data-stu-id="d6b0d-289">On the new line, set the following values:</span></span>

    - <span data-ttu-id="d6b0d-290">**Tablo:** *Yerleşimler*</span><span class="sxs-lookup"><span data-stu-id="d6b0d-290">**Table:** *Locations*</span></span>
    - <span data-ttu-id="d6b0d-291">**Türetilmiş tablo:** *Yerleşimler*</span><span class="sxs-lookup"><span data-stu-id="d6b0d-291">**Derived table:** *Locations*</span></span>
    - <span data-ttu-id="d6b0d-292">**Alan:** *Bölge Kodu*</span><span class="sxs-lookup"><span data-stu-id="d6b0d-292">**Field:** *Zone ID*</span></span>
    - <span data-ttu-id="d6b0d-293">**Ölçüt:** *Toplu* (Listeyi genişletmek için alandaki çift artı işaretini \[**++**\] ve ardından *Toplu*'yu seçin.)</span><span class="sxs-lookup"><span data-stu-id="d6b0d-293">**Criteria:** *Bulk* (Select the double plus sign \[**++**\] in the field to expand the list, and then select *Bulk*.)</span></span>

1. <span data-ttu-id="d6b0d-294">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="d6b0d-294">Select **OK**.</span></span>

## <a name="scenario"></a><span data-ttu-id="d6b0d-295">Senaryo</span><span class="sxs-lookup"><span data-stu-id="d6b0d-295">Scenario</span></span>

### <a name="set-up-the-scenario"></a><span data-ttu-id="d6b0d-296">Senaryoyu ayarlama</span><span class="sxs-lookup"><span data-stu-id="d6b0d-296">Set up the scenario</span></span>

<span data-ttu-id="d6b0d-297">Bu senaryo için, yerleşik örnek verileri kullanın ve bu bölümde açıklanan kayıtları oluşturun.</span><span class="sxs-lookup"><span data-stu-id="d6b0d-297">For this scenario, use the built-in sample data, and create the records that are described in this section.</span></span>

#### <a name="use-the-usmf-sample-data"></a><span data-ttu-id="d6b0d-298">USMF örnek verilerini kullanın</span><span class="sxs-lookup"><span data-stu-id="d6b0d-298">Use the USMF sample data</span></span>

<span data-ttu-id="d6b0d-299">Burada belirtilen örnek kayıtları ve değerleri kullanarak bu senaryo üzerinden çalışmak için, standart [tanıtım verilerinin](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) yüklenmiş olduğu bir sistemde olmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="d6b0d-299">To work through this scenario by using the sample records and values that are specified here, you must be on a system where the standard [demo data](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) is installed.</span></span> <span data-ttu-id="d6b0d-300">Ek olarak, başlamadan önce **USMF** tüzel kişiliğini seçmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="d6b0d-300">Additionally, you must select the **USMF** legal entity before you begin.</span></span>

#### <a name="create-demand"></a><span data-ttu-id="d6b0d-301">Talep oluşturma</span><span class="sxs-lookup"><span data-stu-id="d6b0d-301">Create demand</span></span>

<span data-ttu-id="d6b0d-302">Yerleştirme uygulayacağınız talebi oluşturmak için bu adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="d6b0d-302">Follow these steps to create the demand that you will apply slotting to.</span></span>

1. <span data-ttu-id="d6b0d-303">**Satış ve pazarlama \> Satış siparişleri \> Tüm satış siparişleri**'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="d6b0d-303">Go to **Sales and marketing \> Sales orders \> All sales order**.</span></span>
1. <span data-ttu-id="d6b0d-304">Satış siparişi oluşturmak için **Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="d6b0d-304">Select **New** to create a sales order.</span></span>
1. <span data-ttu-id="d6b0d-305">**Satış siparişi oluştur** iletişim kutusundaki **Müşteri hesabı** alanında _ABD-007_'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="d6b0d-305">In the **Create sales order** dialog box, in the **Customer account** field, select _US-007_.</span></span>
1. <span data-ttu-id="d6b0d-306">**Ambar** alanında _61_'i seçin.</span><span class="sxs-lookup"><span data-stu-id="d6b0d-306">In the **Warehouse** field, select _61_.</span></span>
1. <span data-ttu-id="d6b0d-307">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="d6b0d-307">Select **OK**.</span></span>
1. <span data-ttu-id="d6b0d-308">Yeni satış siparişi açılır.</span><span class="sxs-lookup"><span data-stu-id="d6b0d-308">The new sales order is opened.</span></span> <span data-ttu-id="d6b0d-309">**Satış siparişi satırları** hızlı sekmesinde boş bir satır bulunur.</span><span class="sxs-lookup"><span data-stu-id="d6b0d-309">It includes an empty line on the **Sales order lines** FastTab.</span></span> <span data-ttu-id="d6b0d-310">Bu satır için aşağıdaki değerleri ayarlayın:</span><span class="sxs-lookup"><span data-stu-id="d6b0d-310">On this line, set the following values:</span></span>

    - <span data-ttu-id="d6b0d-311">**Madde:** _L0101_</span><span class="sxs-lookup"><span data-stu-id="d6b0d-311">**Item:** _L0101_</span></span>
    - <span data-ttu-id="d6b0d-312">**Miktar:** _20_</span><span class="sxs-lookup"><span data-stu-id="d6b0d-312">**Quantity:** _20_</span></span>

1. <span data-ttu-id="d6b0d-313">**Satır ekle**'yi seçerek yeni bir satır ekleyin ve aşağıdaki değerleri ayarlayın:</span><span class="sxs-lookup"><span data-stu-id="d6b0d-313">Select **Add line** to add a new line, and set the following values:</span></span>

    - <span data-ttu-id="d6b0d-314">**Madde:** _T0100_</span><span class="sxs-lookup"><span data-stu-id="d6b0d-314">**Item:** _T0100_</span></span>
    - <span data-ttu-id="d6b0d-315">**Miktar:** _8_</span><span class="sxs-lookup"><span data-stu-id="d6b0d-315">**Quantity:** _8_</span></span>

1. <span data-ttu-id="d6b0d-316">**Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="d6b0d-316">Select **Save**.</span></span>
1. <span data-ttu-id="d6b0d-317">İkinci bir satış siparişi oluşturmak için **Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="d6b0d-317">Select **New** to create a second sales order.</span></span>
1. <span data-ttu-id="d6b0d-318">**Satış siparişi oluştur** iletişim kutusundaki **Müşteri hesabı** alanında _ABD-008_'i seçin.</span><span class="sxs-lookup"><span data-stu-id="d6b0d-318">In the **Create sales order** dialog box, in the **Customer account** field, select _US-008_.</span></span>
1. <span data-ttu-id="d6b0d-319">**Ambar** alanında _61_'i seçin.</span><span class="sxs-lookup"><span data-stu-id="d6b0d-319">In the **Warehouse** field, select _61_.</span></span>
1. <span data-ttu-id="d6b0d-320">Yeni satış siparişi açılır.</span><span class="sxs-lookup"><span data-stu-id="d6b0d-320">The new sales order is opened.</span></span> <span data-ttu-id="d6b0d-321">**Satış siparişi satırları** hızlı sekmesinde boş bir satır bulunur.</span><span class="sxs-lookup"><span data-stu-id="d6b0d-321">It includes an empty line on the **Sales order lines** FastTab.</span></span> <span data-ttu-id="d6b0d-322">Bu satır için aşağıdaki değerleri ayarlayın:</span><span class="sxs-lookup"><span data-stu-id="d6b0d-322">On this line, set the following values:</span></span>

    - <span data-ttu-id="d6b0d-323">**Madde:** _T0100_</span><span class="sxs-lookup"><span data-stu-id="d6b0d-323">**Item:** _T0100_</span></span>
    - <span data-ttu-id="d6b0d-324">**Miktar:** _1_</span><span class="sxs-lookup"><span data-stu-id="d6b0d-324">**Quantity:** _1_</span></span>

1. <span data-ttu-id="d6b0d-325">**Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="d6b0d-325">Select **Save**.</span></span>

### <a name="walk-through-a-typical-slotting-scenario"></a><span data-ttu-id="d6b0d-326">Tipik bir yerleştirme senaryosu üzerinden ilerleme</span><span class="sxs-lookup"><span data-stu-id="d6b0d-326">Walk through a typical slotting scenario</span></span>

<span data-ttu-id="d6b0d-327">Önceki bölümde açıklandığı gibi, tüm önkoşul öğeleri belirlendikten sonra, bu bölümdeki her alıştırmada çalışarak bu özelliği denemeye hazırsınız demektir.</span><span class="sxs-lookup"><span data-stu-id="d6b0d-327">After all the prerequisite elements are in place, as described in the previous section, you're ready to try out the feature by working through each exercise in this section.</span></span>

#### <a name="generate-demand"></a><span data-ttu-id="d6b0d-328">Talep oluştur</span><span class="sxs-lookup"><span data-stu-id="d6b0d-328">Generate demand</span></span>

1. <span data-ttu-id="d6b0d-329">**Ambar yönetimi \> Kurulum \> Stok yenileme \> Yerleştirme şablonları**'na gidin ve daha önce oluşturduğunuz yerleştirme şablonunu seçin.</span><span class="sxs-lookup"><span data-stu-id="d6b0d-329">Go to **Warehouse management \> Setup \> Replenishment \> Slotting templates**, and select the slotting template that you created earlier.</span></span>
1. <span data-ttu-id="d6b0d-330">Eylem bölmesinde, **Talep oluştur**'u seçin.</span><span class="sxs-lookup"><span data-stu-id="d6b0d-330">On the Action Pane, select **Generate demand**.</span></span> <span data-ttu-id="d6b0d-331">Bu komut sistemdeki tüm talepleri değerlendirir ve yerleştirme şablon sorgusunu eşleştirir.</span><span class="sxs-lookup"><span data-stu-id="d6b0d-331">This command evaluates all demand that is in the system, and that matches the slotting template query.</span></span> <span data-ttu-id="d6b0d-332">Böylece tüm siparişlerdeki toplam talep, miktar/ölçü birimi başına tek bir satırda birleştirilir.</span><span class="sxs-lookup"><span data-stu-id="d6b0d-332">The total demand across all orders is then consolidated onto one line per quantity/unit of measure.</span></span> <span data-ttu-id="d6b0d-333">İşlem tamamlanınca bir bilgi iletisi görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="d6b0d-333">An informational message appears when the process is completed.</span></span>

#### <a name="slotting-demand"></a><span data-ttu-id="d6b0d-334">Yerleştirme talebi</span><span class="sxs-lookup"><span data-stu-id="d6b0d-334">Slotting demand</span></span>

<span data-ttu-id="d6b0d-335">*Yerleştirme talebi*, yerleştirme şablonunun kurulumuna bağlı olarak, talep oluşturma sonuçlarını gösterir.</span><span class="sxs-lookup"><span data-stu-id="d6b0d-335">The *slotting demand* shows the results of demand generation, based on the setup of the slotting template.</span></span>

- <span data-ttu-id="d6b0d-336">Eylem bölmesinde, **Talep oluştur** komutundan elde edilen sonuçları görmek için **Yerleştirme talebi**'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="d6b0d-336">On the Action Pane, select **Slotting demand** to view the results from the **Generate demand** command.</span></span> <span data-ttu-id="d6b0d-337">Yerleştirme talebindeki satırlar düzenlenebilir.</span><span class="sxs-lookup"><span data-stu-id="d6b0d-337">The lines in the slotting demand can be edited.</span></span> <span data-ttu-id="d6b0d-338">Bir satırı silebilir, yeni bir satır ekleyebilir veya satır ayrıntılarını düzenleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="d6b0d-338">You can delete a line, add a new line, or edit the line details.</span></span>

> [!NOTE]
> <span data-ttu-id="d6b0d-339">Talebi el ile düzenleyebilir veya veri yönetimini kullanarak harici bir sistemden içe aktarabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="d6b0d-339">You can edit demand manually, or you can import it from an external system by using data management.</span></span> <span data-ttu-id="d6b0d-340">Yerleştirme talebindeki her şey sonraki adımda nereden geldiği dikkate alınmaksızın kullanılır.</span><span class="sxs-lookup"><span data-stu-id="d6b0d-340">Whatever is in the slotting demand will be used in the next step, regardless of where it came from.</span></span>

#### <a name="locate-demand"></a><span data-ttu-id="d6b0d-341">Talebi bul</span><span class="sxs-lookup"><span data-stu-id="d6b0d-341">Locate demand</span></span>

<span data-ttu-id="d6b0d-342">Talep oluşturulduktan sonra, *yerleştirme planı* oluşturmak için **Talep bul** komutunu kullanmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="d6b0d-342">After demand has been generated, you must use the **Locate demand** command to generate the *slotting plan*.</span></span>

- <span data-ttu-id="d6b0d-343">Eylem bölmesinde, **Talep bul**'u seçin.</span><span class="sxs-lookup"><span data-stu-id="d6b0d-343">On the Action Pane, select **Locate demand**.</span></span> <span data-ttu-id="d6b0d-344">Yerleştirme işlemi çalıştırılır.</span><span class="sxs-lookup"><span data-stu-id="d6b0d-344">The slotting process runs.</span></span> <span data-ttu-id="d6b0d-345">İşlem tamamlanınca bir bilgi iletisi görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="d6b0d-345">An informational message appears when the process is completed.</span></span>

#### <a name="slotting-plan"></a><span data-ttu-id="d6b0d-346">Yerleştirme planı</span><span class="sxs-lookup"><span data-stu-id="d6b0d-346">Slotting plan</span></span>

<span data-ttu-id="d6b0d-347">Yerleştirme planı, her madde/miktarın atandığı yerleşimi, taşma kullanılıp kullanılmadığını, ara işi oluşturulup oluşturulmadığını ve kullanılan şablon satırını gösterir.</span><span class="sxs-lookup"><span data-stu-id="d6b0d-347">The slotting plan shows the location that each item/quantity was assigned to, whether overflow was used, whether let-up work was created, and the template line that was used.</span></span> <span data-ttu-id="d6b0d-348">*Yerleştirilememiş talepler kırmızı renkle vurgulanır.*</span><span class="sxs-lookup"><span data-stu-id="d6b0d-348">*Any demand that could not be slotted is highlighted in red.*</span></span>

- <span data-ttu-id="d6b0d-349">Eylem bölmesinde, sonuçları görüntülemek için **Yerleştirme planı**'nı seçin.</span><span class="sxs-lookup"><span data-stu-id="d6b0d-349">On the Action Pane, select **Slotting plan** to view the results.</span></span>

> [!NOTE]
> - <span data-ttu-id="d6b0d-350">**Talep oluştur**, **Talebi bul** ve **Stok yenilemeyi çalıştır** işlemleri artık bir korumalı alanda çalıştırılır.</span><span class="sxs-lookup"><span data-stu-id="d6b0d-350">The **Generate demand**, **Locate demand**, and **Run replenishment** processes are now run in a sandbox.</span></span> <span data-ttu-id="d6b0d-351">(Bu işlemler, **Yerleştirme şablonları** sayfasındaki Eylem bölmesinde bulunabilir.)</span><span class="sxs-lookup"><span data-stu-id="d6b0d-351">(These processes are available from the Action Pane on the **Slotting templates** page.)</span></span>
> - <span data-ttu-id="d6b0d-352">**Talep oluştur**, **Talebi bul** ve **Stok yenilemeyi çalıştır** işlemlerinde, aynı anda çalıştırılmamalarını sağlayan bir kilit bulunur.</span><span class="sxs-lookup"><span data-stu-id="d6b0d-352">The **Generate demand**, **Locate demand**, and **Run replenishment** processes have a lock to ensure that they can't be triggered at the same time.</span></span> <span data-ttu-id="d6b0d-353">Aksi durumda, kullanılan veriler silinebilir.</span><span class="sxs-lookup"><span data-stu-id="d6b0d-353">Otherwise, the data that is used could be deleted.</span></span>
> - <span data-ttu-id="d6b0d-354">**Talep oluştur** ve **Talebi bul** işlemleri, çalıştırma işleminin kayıt oluşturmaması veya kayıtlarda bilgilerin eksi olması durumunda uyarı gösterebilir.</span><span class="sxs-lookup"><span data-stu-id="d6b0d-354">The **Generate demand** and **Locate demand** processes show a warning if the run didn't generate records, or if the records are missing information.</span></span>
> - <span data-ttu-id="d6b0d-355">**Yerleştirme planı**'nı seçtiğinizde, veri kaynağı düzenlenemediği için, Eylem bölmesinde **Yeni**, **Düzenle** veya **Sil** düğmeleri bulunmaz.</span><span class="sxs-lookup"><span data-stu-id="d6b0d-355">When you select **Slotting plan**, the page doesn't have **New**, **Edit**, or **Delete** buttons on the Action Pane, because the data source can't be edited.</span></span>
> - <span data-ttu-id="d6b0d-356">**Stok yenilemeyi çalıştır**'ı seçtiğinizde, sistem seçilen yerleştirme şablonunu ve işlemleri doğrular.</span><span class="sxs-lookup"><span data-stu-id="d6b0d-356">When you select **Run replenishment**, the system validates the selected slot template and processes.</span></span>

#### <a name="create-replenishment"></a><span data-ttu-id="d6b0d-357">Stok yenileme oluşturma</span><span class="sxs-lookup"><span data-stu-id="d6b0d-357">Create replenishment</span></span>

<span data-ttu-id="d6b0d-358">Yerleştirme planı oluşturulduktan sonra, plana göre, *stok yenileme işi* oluşturmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="d6b0d-358">After the slotting plan has been created, you must create *replenishment work*, based on the plan.</span></span>

- <span data-ttu-id="d6b0d-359">Eylem bölmesinde **Stok yenilemeyi çalıştır**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="d6b0d-359">On the Action Pane, select **Run replenishment**.</span></span> <span data-ttu-id="d6b0d-360">İşlem tamamlanınca bir bilgi iletisi görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="d6b0d-360">An informational message appears when the process is completed.</span></span> <span data-ttu-id="d6b0d-361">Bu ileti, iş yapı kodu için oluşturulan üst bilgilerin sayısını gösterir.</span><span class="sxs-lookup"><span data-stu-id="d6b0d-361">This message indicates the number of headers that were created for the work build ID.</span></span>

<span data-ttu-id="d6b0d-362">Kullanılacak yerleşim yönergeleri her bir şablon satırında belirtilen yönerge koduna göre tanımlanır.</span><span class="sxs-lookup"><span data-stu-id="d6b0d-362">Location directives that will be used are identified based on the directive code that is specified on each template line.</span></span>

## <a name="tips"></a><span data-ttu-id="d6b0d-363">İpuçları</span><span class="sxs-lookup"><span data-stu-id="d6b0d-363">Tips</span></span>

### <a name="set-up-automatic-slotting"></a><span data-ttu-id="d6b0d-364">Otomatik yerleştirme ayarlama</span><span class="sxs-lookup"><span data-stu-id="d6b0d-364">Set up automatic slotting</span></span>

<span data-ttu-id="d6b0d-365">Gerekli tüm öğeler belirlendikten sonra, aşağıdaki adımları izleyerek otomatik olarak çalışacak bir yerleştirme ayarlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="d6b0d-365">After all the required elements are in place, you can set up slotting to run automatically by following these steps.</span></span>

1. <span data-ttu-id="d6b0d-366">**Ambar yönetimi \> Stok yenileme \> Yerleştirmeyi çalıştır**'a gidin.</span><span class="sxs-lookup"><span data-stu-id="d6b0d-366">Go to **Warehouse management \> Replenishment \> Run slotting**.</span></span>
1. <span data-ttu-id="d6b0d-367">Çalıştırılacak yerleştirme adımlarını belirtin.</span><span class="sxs-lookup"><span data-stu-id="d6b0d-367">Specify the slotting steps to run.</span></span> <span data-ttu-id="d6b0d-368">Aşağıdaki yerleştirme adımlarından birini veya birkaçını seçin:</span><span class="sxs-lookup"><span data-stu-id="d6b0d-368">Select one or more of the following slotting steps:</span></span>

    - <span data-ttu-id="d6b0d-369">Talep oluştur</span><span class="sxs-lookup"><span data-stu-id="d6b0d-369">Generate demand</span></span>
    - <span data-ttu-id="d6b0d-370">Talebi bul</span><span class="sxs-lookup"><span data-stu-id="d6b0d-370">Locate demand</span></span>
    - <span data-ttu-id="d6b0d-371">Stok yenileme işi oluştur</span><span class="sxs-lookup"><span data-stu-id="d6b0d-371">Create replenishment work</span></span>

    > [!NOTE]
    > <span data-ttu-id="d6b0d-372">Yerleştirme adımları aşamalıdır.</span><span class="sxs-lookup"><span data-stu-id="d6b0d-372">The slotting steps are progressive.</span></span> <span data-ttu-id="d6b0d-373">*Talebi bul*'u seçmek istiyorsanız, önce *Talep oluştur*'u seçmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="d6b0d-373">If you want to select *Locate demand*, you must first select *Generate demand*.</span></span>

1. <span data-ttu-id="d6b0d-374">Kullanılacak yerleştirme şablonunu belirtin.</span><span class="sxs-lookup"><span data-stu-id="d6b0d-374">Specify the slotting template to use.</span></span>
1. <span data-ttu-id="d6b0d-375">İsterseniz otomatik çalışma tekrar sayısını belirleyin.</span><span class="sxs-lookup"><span data-stu-id="d6b0d-375">Set the recurrence to run automatically, if you want.</span></span>

<span data-ttu-id="d6b0d-376">Senaryodaki alıştırmalarda otomatik yerleştirme **ayarlamayın**.</span><span class="sxs-lookup"><span data-stu-id="d6b0d-376">For the exercises in the scenario, do **not** set up automatic slotting.</span></span>
