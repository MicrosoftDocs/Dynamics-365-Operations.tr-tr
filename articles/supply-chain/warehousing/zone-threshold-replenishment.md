---
title: Bölge eşiği stok yenilemesi
description: Bölge tabanlı stok yenileme, minimum/maksimum (min/maks) stok yenileme stratejisi kullanır ancak yalnızca tekil yerleşimler yerine tüm ambar bölgelerini değerlendirir. Bu nedenle, ambar yöneticileri bir malzeme çekme bölgesinde ek stok gerektiğini daha çabuk öğrenebilir.
author: Mirzaab
manager: tfehr
ms.date: 07/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSReplenishmentTemplates, WHSLocDirHint, WHSLocDirTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-01
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: e13b5fd895fca7f8fe77809348d63ed8867dea9e
ms.sourcegitcommit: a36a4f9915ae3eb36bf8220111cf1486387713d9
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4017343"
---
# <a name="zone-threshold-replenishment"></a><span data-ttu-id="b60df-104">Bölge eşiği stok yenilemesi</span><span class="sxs-lookup"><span data-stu-id="b60df-104">Zone threshold replenishment</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b60df-105">Bölge tabanlı stok yenileme, minimum/maksimum (min/maks) [stok yenileme](replenishment.md) stratejisi kullanır ancak yalnızca tekil yerleşimler yerine tüm ambar bölgelerini değerlendirir.</span><span class="sxs-lookup"><span data-stu-id="b60df-105">Zone-based replenishment uses a minimum/maximum (min/max) [replenishment](replenishment.md) strategy, but it evaluates whole warehouse zones instead of just individual locations.</span></span> <span data-ttu-id="b60df-106">Bu nedenle, ambar yöneticileri bir malzeme çekme bölgesinde ek stok gerektiğini daha çabuk öğrenebilir.</span><span class="sxs-lookup"><span data-stu-id="b60df-106">Therefore, warehouse managers can more quickly learn when additional inventory is required in a picking zone.</span></span>

<span data-ttu-id="b60df-107">Bu özelliğin kurulumu, yerleşim tabanlı stok yenileme kurulumuna benzer.</span><span class="sxs-lookup"><span data-stu-id="b60df-107">The setup for this feature resembles the setup for location-based replenishment.</span></span> <span data-ttu-id="b60df-108">Ancak, minimum/maksimum stok yenileme için bir şablon ayarlarken, eşiğin yerleşim başına mı yoksa bölge başına mı değerlendirileceğini de belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="b60df-108">However, when you set up a template for min/max replenishment, you can also specify whether the threshold should be evaluated per location or per zone.</span></span> <span data-ttu-id="b60df-109">Bölgelere dayalı değerlendirme ayarlarsanız, bölge seçim sorgusuna belirli bölgeler eklemeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="b60df-109">If you set up evaluation that is based on zones, you must add specific zones to the zone selection query.</span></span>

<span data-ttu-id="b60df-110">Yerleşim tabanlı minimum/maksimum stok yenileme gibi, bölgeye dayalı minimum/maksimum stok yenileme, seçili maddeler için stok yenileme işi oluşturulmasını tetikleyen bir minimum stok eşiğinin kurulumunu temel alır.</span><span class="sxs-lookup"><span data-stu-id="b60df-110">Like location-based min/max replenishment, zone-based min/max replenishment is based the setup of a minimum inventory threshold that triggers the creation of replenishment work for selected items.</span></span> <span data-ttu-id="b60df-111">Bu stok yenileme işi, stoku bölge için belirtilen maksimum eşiğe kadar artırır.</span><span class="sxs-lookup"><span data-stu-id="b60df-111">This replenishment work will increase inventory up to the specified maximum threshold for the zone.</span></span>

> [!NOTE]
> <span data-ttu-id="b60df-112">Geçerli sürümde, ürün çeşitleri için bölge stok yenileme işlemleri desteklenmiyor.</span><span class="sxs-lookup"><span data-stu-id="b60df-112">Zone replenishment processes for product variants aren't supported in the current release.</span></span>


<span data-ttu-id="b60df-113">Yerleşim tabanlı minimum/maksimum stok yenileme işleminden farklı olarak, bölgeye dayalı minimum/maksimum stok yenileme, sabit yerleşimlerin yerleşimlerde belirli bir maddenin depolanıp depolanmayacağını değerlendirmesini zorunlu kılmaz.</span><span class="sxs-lookup"><span data-stu-id="b60df-113">Unlike location-based min/max replenishment, zone-based min/max replenishment doesn't require fixed locations to evaluate whether locations should store a specific item.</span></span> <span data-ttu-id="b60df-114">Bu nedenle, bölge tabanlı stok yenileme, ambarda her madde veya madde çeşidi için sabit yerleşimleriniz olmasa da, minimum/maksimum stok yenilemeyi kullanmanıza olanak sağlar.</span><span class="sxs-lookup"><span data-stu-id="b60df-114">Therefore, zone-based replenishment lets you use min/max replenishment even if you don't have fixed locations for each item or item variant in the warehouse.</span></span> <span data-ttu-id="b60df-115">Bölgedeki bir miktar, belirtilen minimum eşiğin altına düştüğünde stok yenileme işi oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="b60df-115">When a quantity in the zone falls below the specified minimum threshold, replenishment work is created.</span></span> <span data-ttu-id="b60df-116">Yerleşim yönergeleri, stokun hangi konuma yerleştirilmesi gerektiğini belirler.</span><span class="sxs-lookup"><span data-stu-id="b60df-116">Location directives will determine which specific location the inventory should be put into.</span></span>

## <a name="turn-on-the-zone-threshold-replenishment-feature"></a><span data-ttu-id="b60df-117">Bölge eşiği stok yenilemesi özelliğini açın</span><span class="sxs-lookup"><span data-stu-id="b60df-117">Turn on the Zone threshold replenishment feature</span></span>

<span data-ttu-id="b60df-118">*Bölge eşiği stok yenilemesi* özelliğini kullanabilmeniz için, özelliğin sisteminizde etkinleştirilmesi gerekir.</span><span class="sxs-lookup"><span data-stu-id="b60df-118">Before you can use the *Zone threshold replenishment* feature, it must be turned on in your system.</span></span> <span data-ttu-id="b60df-119">Yöneticiler özellik durumunu denetlemek ve gerekirse etkinleştirmek için [özellik yönetimi](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) ayarlarını kullanabilir.</span><span class="sxs-lookup"><span data-stu-id="b60df-119">Admins can use the [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) settings to check the status of the feature and turn it on if it's required.</span></span> <span data-ttu-id="b60df-120">**Özellik yönetimi** çalışma alanındabu özellik aşağıdaki şekilde listelenir:</span><span class="sxs-lookup"><span data-stu-id="b60df-120">In the **Feature management** workspace, the feature is listed in the following way:</span></span>

- <span data-ttu-id="b60df-121">**Modül:** *Ambar yönetimi*</span><span class="sxs-lookup"><span data-stu-id="b60df-121">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="b60df-122">**Özellik adı:** *Bölge eşiği stok yenilemesi*</span><span class="sxs-lookup"><span data-stu-id="b60df-122">**Feature name:** *Zone threshold replenishment*</span></span>

## <a name="set-up-zone-based-replenishment"></a><a name="setup"></a><span data-ttu-id="b60df-123">Bölge tabanlı stok yenilemeyi ayarlama</span><span class="sxs-lookup"><span data-stu-id="b60df-123">Set up zone-based replenishment</span></span>

<span data-ttu-id="b60df-124">Bölgeye dayalı stok yenilemeyi ayarlamak için sistemin çeşitli kısımlarını yapılandırmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="b60df-124">To set up zone-based replenishment, you must configure several parts of the system.</span></span> <span data-ttu-id="b60df-125">Bu bölümde çeşitli ayarlar tanıtılmakta ve bu konunun sonundaki senaryo üzerinden çalışmak istiyorsanız girebileceğiniz tanıtım veri değerleri sağlamaktadır.</span><span class="sxs-lookup"><span data-stu-id="b60df-125">This section introduces the various settings and provides demo data values that you can enter if you want to work through the scenario at the end of this topic.</span></span>

### <a name="set-up-directive-codes"></a><span data-ttu-id="b60df-126">Yönerge kodlarını ayarlama</span><span class="sxs-lookup"><span data-stu-id="b60df-126">Set up directive codes</span></span>

<span data-ttu-id="b60df-127">[Yönerge kodları ](control-warehouse-location-directives.md), bir iş şablonunda kullanılan yerleşim şablonunu tanımlarken daha kesin bilgiler belirtmenizi sağlar.</span><span class="sxs-lookup"><span data-stu-id="b60df-127">[Directive codes](control-warehouse-location-directives.md) let you be more specific when you define the location template that is used in a work template.</span></span> <span data-ttu-id="b60df-128">Her kod, her bir şablon türünü yapılandırırken başvurabileceğiniz ortak bir değer oluşturur.</span><span class="sxs-lookup"><span data-stu-id="b60df-128">Each code establishes a common value that you can refer to when you configure each type of template.</span></span>

#### <a name="view-and-edit-directive-codes"></a><span data-ttu-id="b60df-129">Yönerge kodlarını görüntüleme ve düzenleme</span><span class="sxs-lookup"><span data-stu-id="b60df-129">View and edit directive codes</span></span>

<span data-ttu-id="b60df-130">Yönerge kodlarınızı görüntülemek veya düzenlemek için, **Ambar yönetimi \> Kurulum \> Yönerge kodları** 'na gidin.</span><span class="sxs-lookup"><span data-stu-id="b60df-130">To view or edit your directive codes, go to **Warehouse management \> Setup \> Directive codes**.</span></span>

#### <a name="prepare-demo-data-directive-codes"></a><span data-ttu-id="b60df-131">Tanıtım verileri yönerge kodlarını hazırlama</span><span class="sxs-lookup"><span data-stu-id="b60df-131">Prepare demo data directive codes</span></span>

<span data-ttu-id="b60df-132">Bu örnek, bir yönerge kodunun nasıl hazırlanacağını göstermektedir.</span><span class="sxs-lookup"><span data-stu-id="b60df-132">This example shows how to prepare a directive code.</span></span> <span data-ttu-id="b60df-133">Bu konunun sonundaki senaryo üzerinden çalışmayı planlıyorsanız, burada sağlanan tanıtım veri değerlerini kullanın.</span><span class="sxs-lookup"><span data-stu-id="b60df-133">If you're planning to work through the scenario at the end of this topic, use the demo data values that are provided here.</span></span> <span data-ttu-id="b60df-134">Aksi durumda, kendi değerlerinizi kullanın.</span><span class="sxs-lookup"><span data-stu-id="b60df-134">Otherwise, use your own values.</span></span>

1. <span data-ttu-id="b60df-135">Tanıtım verileriyle çalışmak için **USMF** tüzel kişiliğini seçin.</span><span class="sxs-lookup"><span data-stu-id="b60df-135">Select the **USMF** legal entity to work with the demo data.</span></span>
1. <span data-ttu-id="b60df-136">**Ambar yönetimi \> Kurulum \> Yönerge kodları** 'na gidin.</span><span class="sxs-lookup"><span data-stu-id="b60df-136">Go to **Warehouse management \> Setup \> Directive codes**.</span></span>
1. <span data-ttu-id="b60df-137">Eylem bölmesinde, kılavuzuna satır eklemek için **Yeni** 'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="b60df-137">On the Action Pane, select **New** to add a row to the grid.</span></span>
1. <span data-ttu-id="b60df-138">Yeni satırda aşağıdaki değerleri ayarlayın:</span><span class="sxs-lookup"><span data-stu-id="b60df-138">In the new row, set the following values:</span></span>

    - <span data-ttu-id="b60df-139">**Yönerge kodu:** _Bölge stok yenileme_</span><span class="sxs-lookup"><span data-stu-id="b60df-139">**Directive code:** _Zone replen_</span></span>
    - <span data-ttu-id="b60df-140">**Yönerge açıklaması:** _Bölge stok yenileme_</span><span class="sxs-lookup"><span data-stu-id="b60df-140">**Directive description:** _Zone replenishment_</span></span>

1. <span data-ttu-id="b60df-141">Yeni kodu kaydetmek için **Kaydet** 'i seçin.</span><span class="sxs-lookup"><span data-stu-id="b60df-141">Select **Save** to save the new code.</span></span>

### <a name="set-up-replenishment-templates"></a><span data-ttu-id="b60df-142">Stok yenileme şablonlarını ayarla</span><span class="sxs-lookup"><span data-stu-id="b60df-142">Set up replenishment templates</span></span>

<span data-ttu-id="b60df-143">[Min/maks stok yenileme şablonları](tasks/set-up-min-max-replenishment-process.md) malzeme çekme yerleşimlerinde en uygun düzeyleri korumak için kullanılan birincil mekanizmadır.</span><span class="sxs-lookup"><span data-stu-id="b60df-143">[Min/max replenishment templates](tasks/set-up-min-max-replenishment-process.md) are the primary mechanism for maintaining optimal levels in picking locations.</span></span> <span data-ttu-id="b60df-144">Bu şablonlarda, ambarda stok yenilemek için kullanılacak kuralları ayarlamanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="b60df-144">In these templates, you must set up the rules that will be used to replenish inventory in the warehouse.</span></span> <span data-ttu-id="b60df-145">Şablonların kullanılabileceği stok yenileme, bölgeye dayalı stok yenilemeyi içerir.</span><span class="sxs-lookup"><span data-stu-id="b60df-145">The replenishment that the templates can be used for includes zone-based replenishment.</span></span>

#### <a name="view-and-edit-replenishment-templates"></a><span data-ttu-id="b60df-146">Stok yenileme şablonlarını görüntüleme ve düzenleme</span><span class="sxs-lookup"><span data-stu-id="b60df-146">View and edit replenishment templates</span></span>

<span data-ttu-id="b60df-147">Stok yenileme şablonu, bir yerleşimde stokun ne zaman ve nasıl yenileneceğini denetleyen kural kümesidir.</span><span class="sxs-lookup"><span data-stu-id="b60df-147">A replenishment template is a set of rules that control when and how a location is replenished.</span></span> <span data-ttu-id="b60df-148">Stok yenilemenin ne zaman ve nasıl yapılacağını denetlemek için bir şablon seçersiniz.</span><span class="sxs-lookup"><span data-stu-id="b60df-148">You select a template to control when and how replenishment is done.</span></span> <span data-ttu-id="b60df-149">Stok yenileme şablonlarınızı görüntülemek veya düzenlemek için **Ambar yönetimi \> Kurulum \> Stok yenileme \> Stok yenileme şablonları** 'na gidin.</span><span class="sxs-lookup"><span data-stu-id="b60df-149">To view or edit your replenishment templates, go to **Warehouse management \> Setup \> Replenishment \> Replenishment templates**.</span></span>

#### <a name="prepare-a-demo-data-replenishment-template"></a><span data-ttu-id="b60df-150">Tanıtım verileri stok yenileme şablonu hazırlama</span><span class="sxs-lookup"><span data-stu-id="b60df-150">Prepare a demo data replenishment template</span></span>

<span data-ttu-id="b60df-151">Bu örnek, bir stok yenileme şablonunun nasıl hazırlanacağını göstermektedir.</span><span class="sxs-lookup"><span data-stu-id="b60df-151">This example shows how to prepare a replenishment template.</span></span> <span data-ttu-id="b60df-152">Bu konunun sonundaki senaryo üzerinden çalışmayı planlıyorsanız, burada sağlanan tanıtım veri değerlerini kullanın.</span><span class="sxs-lookup"><span data-stu-id="b60df-152">If you're planning to work through the scenario at the end of this topic, use the demo data values that are provided here.</span></span> <span data-ttu-id="b60df-153">Aksi durumda, kendi değerlerinizi kullanın.</span><span class="sxs-lookup"><span data-stu-id="b60df-153">Otherwise, use your own values.</span></span>

1. <span data-ttu-id="b60df-154">Tanıtım verileriyle çalışmak için **USMF** tüzel kişiliğini seçin.</span><span class="sxs-lookup"><span data-stu-id="b60df-154">Select the **USMF** legal entity to work with the demo data.</span></span>
1. <span data-ttu-id="b60df-155">**Ambar yönetimi \> Kurulum \> Stok yenileme \> Stok yenileme şablonları** 'na gidin.</span><span class="sxs-lookup"><span data-stu-id="b60df-155">Go to **Warehouse management \> Setup \> Replenishment \> Replenishment templates**.</span></span>
1. <span data-ttu-id="b60df-156">Sayfayı düzenleme moduna sokmak için **Düzenle** 'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="b60df-156">Select **Edit** to put the page into edit mode.</span></span>
1. <span data-ttu-id="b60df-157">Eylem bölmesinde, **Genel bakış** kılavuzuna satır eklemek için **Yeni** 'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="b60df-157">On the Action Pane, select **New** to add a row to the **Overview** grid.</span></span>
1. <span data-ttu-id="b60df-158">Yeni satırda aşağıdaki değerleri ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="b60df-158">In the new row, set the following values.</span></span> <span data-ttu-id="b60df-159">Tüm diğer alanlar için varsayılan değerleri kabul edin.</span><span class="sxs-lookup"><span data-stu-id="b60df-159">Accept the default values for all other fields.</span></span>

    - <span data-ttu-id="b60df-160">**Stok yenileme şablonu:** _Bölge min/maks stok yenileme_</span><span class="sxs-lookup"><span data-stu-id="b60df-160">**Replenish template:** _Zone min/max replen_</span></span>
    - <span data-ttu-id="b60df-161">**Açıklama:** _Bölge min/maks stok yenileme_</span><span class="sxs-lookup"><span data-stu-id="b60df-161">**Description:** _Zone min/max replenishment_</span></span>
    - <span data-ttu-id="b60df-162">**Stok yenileme türü:** _Minimum veya maksimum_</span><span class="sxs-lookup"><span data-stu-id="b60df-162">**Replenishment type:** _Minimum or maximum_</span></span>

1. <span data-ttu-id="b60df-163">**Kaydet** 'i seçin.</span><span class="sxs-lookup"><span data-stu-id="b60df-163">Select **Save**.</span></span>
1. <span data-ttu-id="b60df-164">**Genel bakış** kılavuzunda yeni satır seçiliyken , yeni oluşturduğunuz *Bölge min/maks stok yenileme* stok yenileme şablonuyla ilişkili bir satır eklemek için **Stok Yenileme Şablonu Ayrıntıları** kılavuzunun yukarısındaki **Yeni** 'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="b60df-164">While the new row is still selected in the **Overview** grid, select **New** above the **Replenishment Template Details** grid to add a row that is associated with the *Zone Min/Max replen* replenishment template that you just created.</span></span>
1. <span data-ttu-id="b60df-165">Yeni satırda aşağıdaki değerleri ayarlayın:</span><span class="sxs-lookup"><span data-stu-id="b60df-165">In the new row, set the following values:</span></span>

    - <span data-ttu-id="b60df-166">**Sıra numarası:** _1_ girin.</span><span class="sxs-lookup"><span data-stu-id="b60df-166">**Sequence number:** Enter _1_.</span></span>
    - <span data-ttu-id="b60df-167">**Açıklama:** _Malzeme çekme bölge stok yenileme_ girin.</span><span class="sxs-lookup"><span data-stu-id="b60df-167">**Description:** Enter _Pick zone replenishment_.</span></span>
    - <span data-ttu-id="b60df-168">**Stok yenileme birimi:** _beher_ 'i seçin.</span><span class="sxs-lookup"><span data-stu-id="b60df-168">**Replenishment unit:** Select _ea_.</span></span>
    - <span data-ttu-id="b60df-169">**İstek türü:** Bu alanı boş bırakın.</span><span class="sxs-lookup"><span data-stu-id="b60df-169">**Request type:** Leave this field blank.</span></span>
    - <span data-ttu-id="b60df-170">**Yönerge kodu:** Bu alan, stok yenileme şablonunu bir yerleşim yönergesiyle bağlantılandırır.</span><span class="sxs-lookup"><span data-stu-id="b60df-170">**Directive code:** This field links the replenishment template with a location directive.</span></span> <span data-ttu-id="b60df-171">Daha önce oluşturduğunuz tanıtım verileri yönerge kodunu seçin ( _Bölge stok yenileme_ ).</span><span class="sxs-lookup"><span data-stu-id="b60df-171">Select the demo data directive code that you created earlier ( _Zone replen_ ).</span></span>
    - <span data-ttu-id="b60df-172">**İş şablonu:** Bu alanı boş bırakın.</span><span class="sxs-lookup"><span data-stu-id="b60df-172">**Work template:** Leave this field blank.</span></span>
    - <span data-ttu-id="b60df-173">**Minimum miktar:** Bu alan, stok yenilemenin tetikleneceği miktarı ayarlar.</span><span class="sxs-lookup"><span data-stu-id="b60df-173">**Minimum quantity:** This field sets the quantity that replenishment will be triggered at.</span></span> <span data-ttu-id="b60df-174">_50_ girin.</span><span class="sxs-lookup"><span data-stu-id="b60df-174">Enter _50_.</span></span>
    - <span data-ttu-id="b60df-175">**Maksimum miktar:** Bu alan, bir maddenin bir bölgede bulunabilecek maksimum miktarını ayarlar.</span><span class="sxs-lookup"><span data-stu-id="b60df-175">**Maximum quantity:** This field sets the maximum quantity of an item that can be present in a zone.</span></span> <span data-ttu-id="b60df-176">Oluşturulan stok yenileme işi stoku bu miktara artıracaktır.</span><span class="sxs-lookup"><span data-stu-id="b60df-176">Generated replenishment work will increase inventory to this quantity.</span></span> <span data-ttu-id="b60df-177">_150_ girin.</span><span class="sxs-lookup"><span data-stu-id="b60df-177">Enter _150_.</span></span>
    - <span data-ttu-id="b60df-178">**Birim:** Bu alan, minimum ve maksimum değerlerin birimini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="b60df-178">**Unit:** This field sets the unit for the minimum and maximum values.</span></span> <span data-ttu-id="b60df-179">_Beher_ 'i seçin.</span><span class="sxs-lookup"><span data-stu-id="b60df-179">Select _ea_.</span></span>
    - <span data-ttu-id="b60df-180">**Talep artışı:** _Yuvarla_ 'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="b60df-180">**Demand increment:** Select _Round up_.</span></span>
    - <span data-ttu-id="b60df-181">**Boş sabit yerleşimleri yenile:** Bu onay kutusunu işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="b60df-181">**Replenish empty fixed locations:** Select this check box.</span></span>
    - <span data-ttu-id="b60df-182">**Yalnızca sabit yerleşimeri yenile:** Bu onay kutusunu işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="b60df-182">**Replenish only fixed locations:** Clear this check box.</span></span>
    - <span data-ttu-id="b60df-183">**Ürün sorgu modu:** _Ürün sorgusu_ 'nu seçin.</span><span class="sxs-lookup"><span data-stu-id="b60df-183">**Product query mode:** Select _Product query_.</span></span>
    - <span data-ttu-id="b60df-184">**Stok yenileme eşik kapsamı:** Bu alan, şablonun bölgeye göre mi yoksa belirli bir yerleşime göre mi değerlendirileceğini tanımlar.</span><span class="sxs-lookup"><span data-stu-id="b60df-184">**Replenishment threshold scope:** This field defines whether the template should evaluate by zone or by specific location.</span></span> <span data-ttu-id="b60df-185">_Bölge_ 'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="b60df-185">Select _Zone_.</span></span>
    - <span data-ttu-id="b60df-186">**Ambar:** _61_ 'i seçin.</span><span class="sxs-lookup"><span data-stu-id="b60df-186">**Warehouse:** Select _61_.</span></span>

1. <span data-ttu-id="b60df-187">**Stok Yenileme Şablonu Ayrıntıları** kılavuzunun yukarısındaki **Ürünleri seç** 'i seçin.</span><span class="sxs-lookup"><span data-stu-id="b60df-187">Select **Select products** above the **Replenishment Template Details** grid.</span></span>
1. <span data-ttu-id="b60df-188">**Ürün sorgusu** iletişim kutusundaki **Aralık** sekmesinde **Ekle** 'yi seçerek kılavuza bir satır ekleyin:</span><span class="sxs-lookup"><span data-stu-id="b60df-188">In the **Product query** dialog box, on the **Range** tab, select **Add** to add a row to the grid.</span></span>
1. <span data-ttu-id="b60df-189">Yeni satırda aşağıdaki değerleri ayarlayın:</span><span class="sxs-lookup"><span data-stu-id="b60df-189">In the new row, set the following values:</span></span>

    - <span data-ttu-id="b60df-190">**Tablo:** _Maddeler_</span><span class="sxs-lookup"><span data-stu-id="b60df-190">**Table:** _Items_</span></span>
    - <span data-ttu-id="b60df-191">**Türetilmiş tablo:** _Maddeler_</span><span class="sxs-lookup"><span data-stu-id="b60df-191">**Derived table:** _Items_</span></span>
    - <span data-ttu-id="b60df-192">**Alan:** _Madde numarası_</span><span class="sxs-lookup"><span data-stu-id="b60df-192">**Field:** _Item number_</span></span>
    - <span data-ttu-id="b60df-193">**Ölçüt:** _A0001_</span><span class="sxs-lookup"><span data-stu-id="b60df-193">**Criteria:** _A0001_</span></span>

1. <span data-ttu-id="b60df-194">Sorgunuzu kaydetmek için **Tamam** 'ı seçin ve iletişim kutusunu kapatın.</span><span class="sxs-lookup"><span data-stu-id="b60df-194">Select **OK** to save your query and close the dialog box.</span></span>
1. <span data-ttu-id="b60df-195">**Stok Yenileme Şablonu Ayrıntıları** kılavuzunun yukarısındaki **Stok yenilenecek bölgeleri seç** 'i seçin.</span><span class="sxs-lookup"><span data-stu-id="b60df-195">Select **Select zones to replenish** above the **Replenishment Template Details** grid.</span></span>
1. <span data-ttu-id="b60df-196">**Bölge sorgusu** iletişim kutusundaki **Aralık** sekmesinde kılavuza bir satır ekleyin.</span><span class="sxs-lookup"><span data-stu-id="b60df-196">In the **Zone query** dialog box, on the **Range** tab, add a row to the grid.</span></span>
1. <span data-ttu-id="b60df-197">Yeni satırda aşağıdaki değerleri ayarlayın:</span><span class="sxs-lookup"><span data-stu-id="b60df-197">In the new row, set the following values:</span></span>

    - <span data-ttu-id="b60df-198">**Tablo:** _Ambar bölgesi_</span><span class="sxs-lookup"><span data-stu-id="b60df-198">**Table:** _Warehouse zone_</span></span>
    - <span data-ttu-id="b60df-199">**Türetilmiş tablo:** _Ambar bölgesi_</span><span class="sxs-lookup"><span data-stu-id="b60df-199">**Derived table:** _Warehouse zone_</span></span>
    - <span data-ttu-id="b60df-200">**Alan:** _Bölge Kodu_</span><span class="sxs-lookup"><span data-stu-id="b60df-200">**Field:** _Zone ID_</span></span>
    - <span data-ttu-id="b60df-201">**Ölçütler:** _KAT_</span><span class="sxs-lookup"><span data-stu-id="b60df-201">**Criteria:** _FLOOR_</span></span>

1. <span data-ttu-id="b60df-202">Sorgunuzu kaydetmek için **Tamam** 'ı seçin ve iletişim kutusunu kapatın.</span><span class="sxs-lookup"><span data-stu-id="b60df-202">Select **OK** to save your query and close the dialog box.</span></span>

### <a name="set-up-location-directives"></a><span data-ttu-id="b60df-203">Yerleşim yönergelerini kur</span><span class="sxs-lookup"><span data-stu-id="b60df-203">Set up location directives</span></span>

<span data-ttu-id="b60df-204">Yerleşim temelli min/maks stok yenileme işleminden farklı olarak, sistem giden iş için yalnızca çekme yerleşimi yerine tüm bölgeyi değerlendirdiğinden, bölge temelli min/maks stok yenileme için hem malzeme çekme yerleşim yönergelerini hem de koyma yerleşim yönergelerini ayarlamanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="b60df-204">Unlike location-based min/max replenishment, zone-based min/max replenishment requires that you set up both pick location directives and put location directives, because the system evaluates the whole zone instead of just the pick location for outbound work.</span></span>

#### <a name="view-and-edit-location-directives"></a><span data-ttu-id="b60df-205">Yerleşim yönergelerini görüntüleme ve düzenleme</span><span class="sxs-lookup"><span data-stu-id="b60df-205">View and edit location directives</span></span>

<span data-ttu-id="b60df-206">Yerleşim yönergelerinizi görüntülemek veya düzenlemek için **Ambar yönetimi \> Kurulum \> Yerleşim yönergeleri** 'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="b60df-206">To view or edit your location directives, go to **Warehouse management \> Setup \> Location directives**.</span></span>

<span data-ttu-id="b60df-207">Gerekli çekme yerleşimi yönergelerini ve koyma yerleşim yönergelerini oluşturmada ayarların nasıl kullanılacağını gösteren örnekler için sonraki bölüme bakın.</span><span class="sxs-lookup"><span data-stu-id="b60df-207">For examples that show how to use the settings to create the required pick location directives and put location directives, see the next section.</span></span>

#### <a name="prepare-demo-data-location-directives"></a><span data-ttu-id="b60df-208">Tanıtım verileri yerleşim yönergelerini hazırlama</span><span class="sxs-lookup"><span data-stu-id="b60df-208">Prepare demo data location directives</span></span>

<span data-ttu-id="b60df-209">Tanıtım verilerini bu konunun sonundaki senaryoda kullanılabilecek şekilde hazırlamak için iki yerleşim yönergesi oluşturmanız gerekir: biri çekme ve diğeri koyma için.</span><span class="sxs-lookup"><span data-stu-id="b60df-209">To prepare demo data so that it can be used in the scenario at the end of this topic, you must create two location directives: one for pick and one for put.</span></span>

##### <a name="create-a-replenishment-pick-directive"></a><span data-ttu-id="b60df-210">Bir stok yenileme çekme yönergesi oluşturma</span><span class="sxs-lookup"><span data-stu-id="b60df-210">Create a replenishment pick directive</span></span>

1. <span data-ttu-id="b60df-211">Tanıtım verileriyle çalışmak için **USMF** tüzel kişiliğini seçin.</span><span class="sxs-lookup"><span data-stu-id="b60df-211">Select the **USMF** legal entity to work with the demo data.</span></span>
1. <span data-ttu-id="b60df-212">**Ambar Yönetimi \> Kurulum \> Konum yönergeleri** seçeneğine gidin.</span><span class="sxs-lookup"><span data-stu-id="b60df-212">Go to **Warehouse management \> Setup \> Location directives**.</span></span>
1. <span data-ttu-id="b60df-213">Sol bölmede, **İş emri türü** alanını _Stok yenileme_ olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="b60df-213">In the left pane, set the **Work order type** field to _Replenishment_.</span></span>
1. <span data-ttu-id="b60df-214">Eylem bölmesinde **Yeni** 'yi seçerek yeni bir yönerge oluşturun.</span><span class="sxs-lookup"><span data-stu-id="b60df-214">On the Action Pane, select **New** to create a new directive.</span></span>
1. <span data-ttu-id="b60df-215">Aşağıdaki değerleri ayarlayın:</span><span class="sxs-lookup"><span data-stu-id="b60df-215">Set the following values:</span></span>

    - <span data-ttu-id="b60df-216">**Sıra numarası:** Varsayılan değeri kabul edin.</span><span class="sxs-lookup"><span data-stu-id="b60df-216">**Sequence number:** Accept the default value.</span></span>
    - <span data-ttu-id="b60df-217">**Ad:** _Bölge çekme_ girin.</span><span class="sxs-lookup"><span data-stu-id="b60df-217">**Name:** Enter _Zone pick_.</span></span>
    - <span data-ttu-id="b60df-218">**İş türü:** _Çekme_ 'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="b60df-218">**Work type:** Select _Pick_.</span></span>
    - <span data-ttu-id="b60df-219">**Tesis:** _6_ 'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="b60df-219">**Site:** Select _6_.</span></span>
    - <span data-ttu-id="b60df-220">**Ambar:** _61_ 'i seçin.</span><span class="sxs-lookup"><span data-stu-id="b60df-220">**Warehouse:** Select _61_.</span></span>
    - <span data-ttu-id="b60df-221">**Yönerge kodu:** Boş bırakın.</span><span class="sxs-lookup"><span data-stu-id="b60df-221">**Directive code:** Leave this field blank.</span></span>
    - <span data-ttu-id="b60df-222">**Çoklu SKU:** Bu seçeneği _Hayır_ olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="b60df-222">**Multi SKU:** Set this option to _No_.</span></span>

1. <span data-ttu-id="b60df-223">Şimdiye kadar yapılandırdığınız ayarları taşıyan bir yönerge oluşturmak için **Kaydet** 'i seçin.</span><span class="sxs-lookup"><span data-stu-id="b60df-223">Select **Save** to create a directive that has the settings that you've configured so far.</span></span>
1. <span data-ttu-id="b60df-224">**Satırlar** hızlı sekmesinde, kılavuza satır eklemek için **Yeni** 'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="b60df-224">On the **Lines** FastTab, select **New** to add a line to the grid.</span></span>
1. <span data-ttu-id="b60df-225">Yeni satırda aşağıdaki değerleri ayarlayın:</span><span class="sxs-lookup"><span data-stu-id="b60df-225">On the new line, set the following values:</span></span>

    - <span data-ttu-id="b60df-226">**Sıra numarası:** _1_ girin.</span><span class="sxs-lookup"><span data-stu-id="b60df-226">**Sequence number:** Enter _1_.</span></span>
    - <span data-ttu-id="b60df-227">**Başlangıç miktarı:** _0_ girin.</span><span class="sxs-lookup"><span data-stu-id="b60df-227">**From quantity:** Enter _0_.</span></span>
    - <span data-ttu-id="b60df-228">**Son miktar:** _10000000_ girin.</span><span class="sxs-lookup"><span data-stu-id="b60df-228">**To quantity:** Enter _10000000_.</span></span>
    - <span data-ttu-id="b60df-229">**Birim:** Bu alanı boş bırakın.</span><span class="sxs-lookup"><span data-stu-id="b60df-229">**Unit:** Leave this field blank.</span></span>
    - <span data-ttu-id="b60df-230">**Miktarı bul:** _Yok_ 'u seçin.</span><span class="sxs-lookup"><span data-stu-id="b60df-230">**Locate quantity:** Select _None_.</span></span>
    - <span data-ttu-id="b60df-231">**Birime göre kısıtla:** Bu onay kutusunun işaretini kaldırın.</span><span class="sxs-lookup"><span data-stu-id="b60df-231">**Restrict by unit:** Clear this check box.</span></span>
    - <span data-ttu-id="b60df-232">**Birime yuvarla:** Bu onay kutusunun işaretini kaldırın.</span><span class="sxs-lookup"><span data-stu-id="b60df-232">**Round up to unit:** Clear this check box.</span></span>
    - <span data-ttu-id="b60df-233">**Ambalaj miktarını bul:** Bu onay kutusunun işaretini kaldırın.</span><span class="sxs-lookup"><span data-stu-id="b60df-233">**Locate packing quantity:** Clear this check box.</span></span>
    - <span data-ttu-id="b60df-234">**Bölmeye izin ver:** Bu onay kutusunu işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="b60df-234">**Allow split:** Select this check box.</span></span>

1. <span data-ttu-id="b60df-235">Yeni satırı kaydetmek için **Kaydet** 'i seçin.</span><span class="sxs-lookup"><span data-stu-id="b60df-235">Select **Save** to save the new line.</span></span>
1. <span data-ttu-id="b60df-236">Yeni satırınız **Satırlar** kılavuzunda hala seçiliyken, kılavuza satır eklemek için **Yerleşim Yönergesi Eylemleri** hızlı sekmesinde **Yeni** 'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="b60df-236">While your new line is still selected in the **Lines** grid, select **New** on the **Location Directive Actions** FastTab to add a row to the grid.</span></span>
1. <span data-ttu-id="b60df-237">Yeni satırda aşağıdaki değerleri ayarlayın:</span><span class="sxs-lookup"><span data-stu-id="b60df-237">In the new row, set the following values:</span></span>

    - <span data-ttu-id="b60df-238">**Sıra numarası:** _1_ girin.</span><span class="sxs-lookup"><span data-stu-id="b60df-238">**Sequence number:** Enter _1_.</span></span>
    - <span data-ttu-id="b60df-239">**Ad:** _Toplu işten çek_ girin.</span><span class="sxs-lookup"><span data-stu-id="b60df-239">**Name:** Enter _Pick from bulk_.</span></span>
    - <span data-ttu-id="b60df-240">**Sabit yerleşim kullanımı:** _Sabit ve sabit olmayan yerleşimler_ 'i seçin.</span><span class="sxs-lookup"><span data-stu-id="b60df-240">**Fixed location usage:** Select _Fixed and non-fixed locations_.</span></span>
    - <span data-ttu-id="b60df-241">**Negatif stoka izin ver:** Bu onay kutusunun işaretini kaldırın.</span><span class="sxs-lookup"><span data-stu-id="b60df-241">**Allow negative inventory:** Clear this check box.</span></span>
    - <span data-ttu-id="b60df-242">**Toplu iş etkin:** Bu onay kutusunun işaretini kaldırın.</span><span class="sxs-lookup"><span data-stu-id="b60df-242">**Batch enabled:** Clear this check box.</span></span>
    - <span data-ttu-id="b60df-243">**Strateji:** _Yok_ 'u seçin.</span><span class="sxs-lookup"><span data-stu-id="b60df-243">**Strategy:** Select _None_.</span></span>

1. <span data-ttu-id="b60df-244">Yeni eylemi kaydetmek için **Kaydet** 'i seçin.</span><span class="sxs-lookup"><span data-stu-id="b60df-244">Select **Save** to save the new action.</span></span>
1. <span data-ttu-id="b60df-245">Yeni eyleminiz hala seçiliyken, **Yerleşim Yönergesi Eylemleri** kılavuzunun yukarısındaki **Sorgu düzenle** 'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="b60df-245">While your new action still selected, select **Edit query** above the **Location Directive Actions** grid.</span></span>
1. <span data-ttu-id="b60df-246">Stok yenileme kaynak yerleşimlerini seçebileceğiniz bir sorgu iletişim kutusu görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="b60df-246">A query dialog box appears, where you can select the locations to replenish from.</span></span> <span data-ttu-id="b60df-247">**Aralık** sekmesinde, kılavuza satır eklemek için **Ekle** 'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="b60df-247">On the **Range** tab, select **Add** to add a row to the grid.</span></span>
1. <span data-ttu-id="b60df-248">Yeni satırda aşağıdaki değerleri ayarlayın:</span><span class="sxs-lookup"><span data-stu-id="b60df-248">In the new row, set the following values:</span></span>

    - <span data-ttu-id="b60df-249">**Tablo:** _Yerleşimler_</span><span class="sxs-lookup"><span data-stu-id="b60df-249">**Table:** _Locations_</span></span>
    - <span data-ttu-id="b60df-250">**Türetilmiş tablo:** _Yerleşimler_</span><span class="sxs-lookup"><span data-stu-id="b60df-250">**Derived table:** _Locations_</span></span>
    - <span data-ttu-id="b60df-251">**Alan:** _Bölge Kodu_</span><span class="sxs-lookup"><span data-stu-id="b60df-251">**Field:** _Zone ID_</span></span>
    - <span data-ttu-id="b60df-252">**Ölçüt:** _BULK_</span><span class="sxs-lookup"><span data-stu-id="b60df-252">**Criteria:** _BULK_</span></span>

1. <span data-ttu-id="b60df-253">Sorgunuzu kaydetmek için **Tamam** 'ı seçin ve iletişim kutusunu kapatın.</span><span class="sxs-lookup"><span data-stu-id="b60df-253">Select **OK** to save your query and close the dialog box.</span></span>
1. <span data-ttu-id="b60df-254">Yerleşim yönergenizi kaydetmek için **Kaydet** 'i seçin.</span><span class="sxs-lookup"><span data-stu-id="b60df-254">Select **Save** to save your location directive.</span></span>

##### <a name="create-a-replenishment-put-directive"></a><span data-ttu-id="b60df-255">Bir stok yenileme koyma yönergesi oluşturma</span><span class="sxs-lookup"><span data-stu-id="b60df-255">Create a replenishment put directive</span></span>

1. <span data-ttu-id="b60df-256">**Yerleşim yönergeleri** sayfasındaki sol bölmede, **İş emri türü** alanının hala _Stok yenileme_ olarak ayarlandığından emin olun.</span><span class="sxs-lookup"><span data-stu-id="b60df-256">On the **Location directives** page, in the left pane, make sure that the **Work order type** field is still set to _Replenishment_.</span></span>
1. <span data-ttu-id="b60df-257">Eylem bölmesinde **Yeni** 'yi seçerek yeni bir yönerge daha oluşturun.</span><span class="sxs-lookup"><span data-stu-id="b60df-257">On the Action Pane, select **New** to create another new directive.</span></span>
1. <span data-ttu-id="b60df-258">Aşağıdaki değerleri ayarlayın:</span><span class="sxs-lookup"><span data-stu-id="b60df-258">Set the following values:</span></span>

    - <span data-ttu-id="b60df-259">**Sıra numarası:** Varsayılan değeri kabul edin.</span><span class="sxs-lookup"><span data-stu-id="b60df-259">**Sequence number:** Accept the default value.</span></span>
    - <span data-ttu-id="b60df-260">**Ad:** _Bölge koyma_ girin.</span><span class="sxs-lookup"><span data-stu-id="b60df-260">**Name:** Enter _Zone put_.</span></span>
    - <span data-ttu-id="b60df-261">**İş emri türü:** _Koyma_ 'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="b60df-261">**Work order type:** Select _Put_.</span></span>
    - <span data-ttu-id="b60df-262">**Tesis:** _6_ 'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="b60df-262">**Site:** Select _6_.</span></span>
    - <span data-ttu-id="b60df-263">**Ambar:** _61_ 'i seçin.</span><span class="sxs-lookup"><span data-stu-id="b60df-263">**Warehouse:** Select _61_.</span></span>
    - <span data-ttu-id="b60df-264">**Yönerge kodu:** Bu konum yönergesini, daha önce oluşturduğunuz kodu kullanarak daha önce oluşturduğunuz stok yenileme şablonuyla bağlantılandırmak için _Bölge stok yenileme_ 'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="b60df-264">**Directive code:** Select _Zone replen_ to link this location directive with the replenishment template that you created earlier by using the code that you created earlier.</span></span>
    - <span data-ttu-id="b60df-265">**Çoklu SKU:** Bu seçeneği _Hayır_ olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="b60df-265">**Multi SKU:** Set this option to _No_.</span></span>

1. <span data-ttu-id="b60df-266">Şimdiye kadar yapılandırdığınız ayarları taşıyan bir yönerge oluşturmak için **Kaydet** 'i seçin.</span><span class="sxs-lookup"><span data-stu-id="b60df-266">Select **Save** to create a directive that has the settings that you've configured so far.</span></span>
1. <span data-ttu-id="b60df-267">**Satırlar** hızlı sekmesinde, kılavuza satır eklemek için **Yeni** 'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="b60df-267">On the **Lines** FastTab, select **New** to add a line to the grid.</span></span>
1. <span data-ttu-id="b60df-268">Yeni satırda aşağıdaki değerleri ayarlayın:</span><span class="sxs-lookup"><span data-stu-id="b60df-268">On the new line, set the following values:</span></span>

    - <span data-ttu-id="b60df-269">**Sıra numarası:** _1_ girin.</span><span class="sxs-lookup"><span data-stu-id="b60df-269">**Sequence number:** Enter _1_.</span></span>
    - <span data-ttu-id="b60df-270">**Başlangıç miktarı:** _0_ girin.</span><span class="sxs-lookup"><span data-stu-id="b60df-270">**From quantity:** Enter _0_.</span></span>
    - <span data-ttu-id="b60df-271">**Son miktar:** _10000000_ girin.</span><span class="sxs-lookup"><span data-stu-id="b60df-271">**To quantity:** Enter _10000000_.</span></span>
    - <span data-ttu-id="b60df-272">**Birim:** Bu alanı boş bırakın.</span><span class="sxs-lookup"><span data-stu-id="b60df-272">**Unit:** Leave this field blank.</span></span>
    - <span data-ttu-id="b60df-273">**Miktarı bul:** _Yok_ 'u seçin.</span><span class="sxs-lookup"><span data-stu-id="b60df-273">**Locate quantity:** Select _None_.</span></span>
    - <span data-ttu-id="b60df-274">**Birime göre kısıtla:** Bu onay kutusunun işaretini kaldırın.</span><span class="sxs-lookup"><span data-stu-id="b60df-274">**Restrict by unit:** Clear this check box.</span></span>
    - <span data-ttu-id="b60df-275">**Birime yuvarla:** Bu onay kutusunun işaretini kaldırın.</span><span class="sxs-lookup"><span data-stu-id="b60df-275">**Round up to unit:** Clear this check box.</span></span>
    - <span data-ttu-id="b60df-276">**Ambalaj miktarını bul:** Bu onay kutusunun işaretini kaldırın.</span><span class="sxs-lookup"><span data-stu-id="b60df-276">**Locate packing quantity:** Clear this check box.</span></span>
    - <span data-ttu-id="b60df-277">**Bölmeye izin ver:** Bu onay kutusunu işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="b60df-277">**Allow split:** Select this check box.</span></span>

1. <span data-ttu-id="b60df-278">Yeni satırı kaydetmek için **Kaydet** 'i seçin.</span><span class="sxs-lookup"><span data-stu-id="b60df-278">Select **Save** to save the new line.</span></span>
1. <span data-ttu-id="b60df-279">Yeni satırınız **Satırlar** kılavuzunda hala seçiliyken, kılavuza satır eklemek için **Yerleşim Yönergesi Eylemleri** hızlı sekmesinde **Yeni** 'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="b60df-279">While your new line is still selected in the **Lines** grid, select **New** on the **Location Directive Actions** FastTab to add a row to the grid.</span></span>
1. <span data-ttu-id="b60df-280">Yeni satırda aşağıdaki değerleri ayarlayın:</span><span class="sxs-lookup"><span data-stu-id="b60df-280">In the new row, set the following values:</span></span>

    - <span data-ttu-id="b60df-281">**Sıra numarası:** _1_ girin.</span><span class="sxs-lookup"><span data-stu-id="b60df-281">**Sequence number:** Enter _1_.</span></span>
    - <span data-ttu-id="b60df-282">**Ad:** _Bölge koyma_ girin.</span><span class="sxs-lookup"><span data-stu-id="b60df-282">**Name:** Enter _Zone put_.</span></span>
    - <span data-ttu-id="b60df-283">**Sabit yerleşim kullanımı:** _Sabit ve sabit olmayan yerleşimler_ 'i seçin.</span><span class="sxs-lookup"><span data-stu-id="b60df-283">**Fixed location usage:** Select _Fixed and non-fixed locations_.</span></span>
    - <span data-ttu-id="b60df-284">**Negatif stoka izin ver:** Bu onay kutusunun işaretini kaldırın.</span><span class="sxs-lookup"><span data-stu-id="b60df-284">**Allow negative inventory:** Clear this check box.</span></span>
    - <span data-ttu-id="b60df-285">**Toplu iş etkin:** Bu onay kutusunun işaretini kaldırın.</span><span class="sxs-lookup"><span data-stu-id="b60df-285">**Batch enabled:** Clear this check box.</span></span>
    - <span data-ttu-id="b60df-286">**Strateji:** _Konsolide et_ 'i seçin.</span><span class="sxs-lookup"><span data-stu-id="b60df-286">**Strategy:** Select _Consolidate_.</span></span>

1. <span data-ttu-id="b60df-287">Yeni eylemi kaydetmek için **Kaydet** 'i seçin.</span><span class="sxs-lookup"><span data-stu-id="b60df-287">Select **Save** to save the new action.</span></span>
1. <span data-ttu-id="b60df-288">Yeni eyleminiz hala seçiliyken, **Yerleşim Yönergesi Eylemleri** kılavuzunun yukarısındaki **Sorgu düzenle** 'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="b60df-288">While your new action is still selected, select **Edit query** above the **Location Directive Actions** grid.</span></span>
1. <span data-ttu-id="b60df-289">Stok yenilenecek bölgeyi seçebileceğiniz bir sorgu iletişim kutusu görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="b60df-289">A query dialog box appears, where you can select the zone to replenish to.</span></span> <span data-ttu-id="b60df-290">Bu bölge, stok yenileme şablonunda belirtilen bölgeyle aynı olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="b60df-290">This zone should be the same zone that is specified in the replenishment template.</span></span> <span data-ttu-id="b60df-291">**Aralık** sekmesinde, kılavuza satır eklemek için **Ekle** 'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="b60df-291">On the **Range** tab, select **Add** to add a row to the grid.</span></span>
1. <span data-ttu-id="b60df-292">Yeni satırda aşağıdaki değerleri ayarlayın:</span><span class="sxs-lookup"><span data-stu-id="b60df-292">In the new row, set the following values:</span></span>

    - <span data-ttu-id="b60df-293">**Tablo:** _Yerleşimler_</span><span class="sxs-lookup"><span data-stu-id="b60df-293">**Table:** _Locations_</span></span>
    - <span data-ttu-id="b60df-294">**Türetilmiş tablo:** _Yerleşimler_</span><span class="sxs-lookup"><span data-stu-id="b60df-294">**Derived table:** _Locations_</span></span>
    - <span data-ttu-id="b60df-295">**Alan:** _Bölge Kodu_</span><span class="sxs-lookup"><span data-stu-id="b60df-295">**Field:** _Zone ID_</span></span>
    - <span data-ttu-id="b60df-296">**Ölçütler:** _KAT_</span><span class="sxs-lookup"><span data-stu-id="b60df-296">**Criteria:** _FLOOR_</span></span>

1. <span data-ttu-id="b60df-297">Sorgunuzu kaydetmek için **Tamam** 'ı seçin ve iletişim kutusunu kapatın.</span><span class="sxs-lookup"><span data-stu-id="b60df-297">Select **OK** to save your query and close the dialog box.</span></span>
1. <span data-ttu-id="b60df-298">Yerleşim yönergenizi kaydetmek için **Kaydet** 'i seçin.</span><span class="sxs-lookup"><span data-stu-id="b60df-298">Select **Save** to save your location directive.</span></span>

## <a name="scenario"></a><span data-ttu-id="b60df-299">Senaryo</span><span class="sxs-lookup"><span data-stu-id="b60df-299">Scenario</span></span>

<span data-ttu-id="b60df-300">Bu bölümde, özellikle nasıl çalışılacağını gösteren örnek bir senaryo verilmektedir.</span><span class="sxs-lookup"><span data-stu-id="b60df-300">This section provides a sample scenario that shows how to work with the feature.</span></span>

### <a name="prepare-the-sample-data-that-is-required-for-the-sample-scenario"></a><span data-ttu-id="b60df-301">Örnek senaryo için gereken örnek verileri hazırlama</span><span class="sxs-lookup"><span data-stu-id="b60df-301">Prepare the sample data that is required for the sample scenario</span></span>

<span data-ttu-id="b60df-302">Senaryo üzerinden çalışmaya başlamadan önce, örnek verileri etkinleştirmeniz ve özelliği bu bölümde ve bu konunun önceki bölümlerinde açıklandığı şekilde ayarlamanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="b60df-302">Before you start to work through the scenario, you must activate sample data and set up the feature as described in this section and in the previous sections of this topic.</span></span>

#### <a name="use-the-usmf-legal-entity"></a><span data-ttu-id="b60df-303">Tüzel kişilik olarak USMF'yi kullanın</span><span class="sxs-lookup"><span data-stu-id="b60df-303">Use the USMF legal entity</span></span>

<span data-ttu-id="b60df-304">Burada belirtilen örnek kayıtları ve değerleri kullanarak senaryo üzerinden çalışmak için, standart [tanıtım verilerinin](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) yüklenmiş olduğu bir sistemde olmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="b60df-304">To work through the scenario by using the sample records and values that are specified here, you must be on a system where the standard [demo data](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) is installed.</span></span> <span data-ttu-id="b60df-305">Ek olarak, başlamadan önce **USMF** tüzel kişiliğini seçmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="b60df-305">Additionally, you must select the **USMF** legal entity before you begin.</span></span>

#### <a name="prepare-additional-sample-data"></a><span data-ttu-id="b60df-306">Ek örnek veriler hazırlama</span><span class="sxs-lookup"><span data-stu-id="b60df-306">Prepare additional sample data</span></span>

<span data-ttu-id="b60df-307">**USMF** tüzel kişiliğini seçtikten sonra, bu konunun önceki [Bölge tabanlı stok yenileme](#setup) bölümünde açıklandığı gibi gerekli ek örnek verileri ekleyin.</span><span class="sxs-lookup"><span data-stu-id="b60df-307">After you've selected the **USMF** legal entity, add the additional sample data that is required, as described in the [Set up zone-based replenishment](#setup) section earlier in this topic.</span></span>

#### <a name="check-your-on-hand-inventory"></a><span data-ttu-id="b60df-308">Eldeki stokunuzu denetleme</span><span class="sxs-lookup"><span data-stu-id="b60df-308">Check your on-hand inventory</span></span>

<span data-ttu-id="b60df-309">Sisteminizde örnek senaryoyu destekleyecek yeterli sayıda stok bulunduğundan emin olmak için bu adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="b60df-309">Follow these steps to make sure that your system includes enough inventory to support the sample scenario.</span></span>

1. <span data-ttu-id="b60df-310">Stok yenileme şablonunda belirtilen çekme bölgesindeki ( *KAT* ) iki farklı konumda *A0001* kodlu madde için eldeki stok bulunduğundan emin olun.</span><span class="sxs-lookup"><span data-stu-id="b60df-310">Make sure that there is on-hand inventory for item *A0001* at two different locations in the pick zone ( *FLOOR* ) that is specified in the replenishment template.</span></span> <span data-ttu-id="b60df-311">Ancak, toplam stok, stok yenileme şablonunda belirtilen gerekli minimum miktardan ( *50* ) az olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="b60df-311">However, the total inventory should be less than the required minimum quantity ( *50* ) that is specified on the replenishment template.</span></span> <span data-ttu-id="b60df-312">Böylece, tek bir yerleşim yerine, tüm bölge için hesaplamanın nasıl gerçekleşeceğinin benzetimini yapabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="b60df-312">In this way, you can simulate how the calculation occurs for the whole zone instead of just for a single location.</span></span> <span data-ttu-id="b60df-313">**Stoku gerektiği gibi ayarlamak için ambar işlemlerini kullanın.**</span><span class="sxs-lookup"><span data-stu-id="b60df-313">**Use any of the warehouse processes to adjust inventory as required.**</span></span>
1. <span data-ttu-id="b60df-314">Stok yenileme işinin maddeleri *TOPLU* kodlu bölgeden çekeceği bölge çekme konumu yönergesinde belirtilen bir toplu yerleşimde madde *A0001* için yeterli stok bulunduğundan emin olun.</span><span class="sxs-lookup"><span data-stu-id="b60df-314">Make sure that there is enough inventory for item *A0001* at a bulk location that is specified in the zone pick location directive where the replenishment work should pick the items from zone ID *BULK*.</span></span> <span data-ttu-id="b60df-315">Toplam stok, stok yenileme şablonunda belirtilen gerekli maksimum miktardan ( *150* ) fazla olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="b60df-315">The total inventory must be more than the required maximum quantity ( *150* ) that is specified in the replenishment template.</span></span>
1. <span data-ttu-id="b60df-316">İsteğe bağlı olmakla birlikte önerilir: Stok ayarlama günlüğü oluşturmak için şu adımları izleyin:</span><span class="sxs-lookup"><span data-stu-id="b60df-316">Optional but recommended: Follow these steps to create an inventory adjustment journal:</span></span>

    1. <span data-ttu-id="b60df-317">**Stok yönetimi \> Günlük girişleri \> Maddeler \> Stok ayarlama** 'ya gidin.</span><span class="sxs-lookup"><span data-stu-id="b60df-317">Go to **Inventory management \> Journal entries \> Items \> Inventory adjustment**.</span></span>
    1. <span data-ttu-id="b60df-318">**Yeni** 'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="b60df-318">Select **New**.</span></span>
    1. <span data-ttu-id="b60df-319">**Stok günlüğü oluştur** iletişim kutusundaki **Ambar** alanında *61* 'i seçin.</span><span class="sxs-lookup"><span data-stu-id="b60df-319">In the **Create inventory journal** dialog box, in the **Warehouse** field, select *61*.</span></span>
    1. <span data-ttu-id="b60df-320">**Tamam** 'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="b60df-320">Select **OK**.</span></span>
    1. <span data-ttu-id="b60df-321">**Günlük satırları** hızlı sekmesinde **Yeni** düğmesini kullanarak kılavuza üç satır ekleyin ve aşağıdaki değerleri ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="b60df-321">On the **Journal lines** FastTab, use the **New** button to add three lines to the grid, and set the following values.</span></span> <span data-ttu-id="b60df-322">Her satırı ayarlamayı bitirdikten sonra **Kaydet** 'i seçin.</span><span class="sxs-lookup"><span data-stu-id="b60df-322">After you've finished setting up each line, select **Save**.</span></span>

        - <span data-ttu-id="b60df-323">**Satır 1:**</span><span class="sxs-lookup"><span data-stu-id="b60df-323">**Line 1:**</span></span>

            - <span data-ttu-id="b60df-324">**Madde numarası:** *A0001*</span><span class="sxs-lookup"><span data-stu-id="b60df-324">**Item number:** *A0001*</span></span>
            - <span data-ttu-id="b60df-325">**Tesis:** *6*</span><span class="sxs-lookup"><span data-stu-id="b60df-325">**Site:** *6*</span></span>
            - <span data-ttu-id="b60df-326">**Ambar:** *61*</span><span class="sxs-lookup"><span data-stu-id="b60df-326">**Warehouse:** *61*</span></span>
            - <span data-ttu-id="b60df-327">**Yerleşim:** *02A01R1S1B*</span><span class="sxs-lookup"><span data-stu-id="b60df-327">**Location:** *02A01R1S1B*</span></span>
            - <span data-ttu-id="b60df-328">**Plaka:** Listeden varolan bir plakayı seçin veya yeni bir plaka oluşturun.</span><span class="sxs-lookup"><span data-stu-id="b60df-328">**License plate:** Select an existing license plate in the list, or create a new license plate.</span></span>
            - <span data-ttu-id="b60df-329">**Miktar:** *1000*</span><span class="sxs-lookup"><span data-stu-id="b60df-329">**Quantity:** *1000*</span></span>

        - <span data-ttu-id="b60df-330">**Satır 2:**</span><span class="sxs-lookup"><span data-stu-id="b60df-330">**Line 2:**</span></span>

            - <span data-ttu-id="b60df-331">**Madde numarası:** *A0001*</span><span class="sxs-lookup"><span data-stu-id="b60df-331">**Item number:** *A0001*</span></span>
            - <span data-ttu-id="b60df-332">**Tesis:** *6*</span><span class="sxs-lookup"><span data-stu-id="b60df-332">**Site:** *6*</span></span>
            - <span data-ttu-id="b60df-333">**Ambar:** *61*</span><span class="sxs-lookup"><span data-stu-id="b60df-333">**Warehouse:** *61*</span></span>
            - <span data-ttu-id="b60df-334">**Yerleşim:** *07A01R2S1B*</span><span class="sxs-lookup"><span data-stu-id="b60df-334">**Location:** *07A01R2S1B*</span></span>
            - <span data-ttu-id="b60df-335">**Plaka:** Listeden varolan bir plakayı seçin veya yeni bir plaka oluşturun.</span><span class="sxs-lookup"><span data-stu-id="b60df-335">**License plate:** Select an existing license plate in the list, or create a new license plate.</span></span>
            - <span data-ttu-id="b60df-336">**Miktar:** *15*</span><span class="sxs-lookup"><span data-stu-id="b60df-336">**Quantity:** *15*</span></span>

        - <span data-ttu-id="b60df-337">**Satır 3:**</span><span class="sxs-lookup"><span data-stu-id="b60df-337">**Line 3:**</span></span>

            - <span data-ttu-id="b60df-338">**Madde numarası:** *A0001*</span><span class="sxs-lookup"><span data-stu-id="b60df-338">**Item number:** *A0001*</span></span>
            - <span data-ttu-id="b60df-339">**Tesis:** *6*</span><span class="sxs-lookup"><span data-stu-id="b60df-339">**Site:** *6*</span></span>
            - <span data-ttu-id="b60df-340">**Ambar:** *61*</span><span class="sxs-lookup"><span data-stu-id="b60df-340">**Warehouse:** *61*</span></span>
            - <span data-ttu-id="b60df-341">**Yerleşim:** *07A01R1S1B*</span><span class="sxs-lookup"><span data-stu-id="b60df-341">**Location:** *07A01R1S1B*</span></span>
            - <span data-ttu-id="b60df-342">**Plaka:** Listeden varolan bir plakayı seçin veya yeni bir plaka oluşturun.</span><span class="sxs-lookup"><span data-stu-id="b60df-342">**License plate:** Select an existing license plate in the list, or create a new license plate.</span></span>
            - <span data-ttu-id="b60df-343">**Miktar:** *10*</span><span class="sxs-lookup"><span data-stu-id="b60df-343">**Quantity:** *10*</span></span>

    1. <span data-ttu-id="b60df-344">Eylem bölmesinde **Doğrula** 'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="b60df-344">On the Action Pane, select **Validate**.</span></span> <span data-ttu-id="b60df-345">Bir sonraki adıma geçmeden önce bulunan tüm hataları çözün.</span><span class="sxs-lookup"><span data-stu-id="b60df-345">Address any errors that are found before you move on to the next step.</span></span>
    1. <span data-ttu-id="b60df-346">Eylem bölmesinde, stoku ambara nakletmek için **Deftere naklet** 'i seçin.</span><span class="sxs-lookup"><span data-stu-id="b60df-346">On the Action Pane, select **Post** to post the inventory to the warehouse.</span></span>

### <a name="sample-scenario-run-zone-based-minmax-replenishment"></a><span data-ttu-id="b60df-347">Örnek senaryo: Bölge tabanlı min/maks stok yenilemeyi çalıştırma</span><span class="sxs-lookup"><span data-stu-id="b60df-347">Sample scenario: Run zone-based min/max replenishment</span></span>

<span data-ttu-id="b60df-348">Tüm önkoşul örnek verileri oluşturulduktan sonra, bu adımları izleyerek stok yenilemeyi tetikleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="b60df-348">After all the prerequisite sample data is in place, you can trigger replenishment by following these steps.</span></span>

1. <span data-ttu-id="b60df-349">**Ambar yönetimi \> Stok yenileme \> Stok yenilemeleri** 'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="b60df-349">Go to **Warehouse management \> Replenishment \> Replenishments**.</span></span>
1. <span data-ttu-id="b60df-350">**Stok yenileme** iletişim kutusundaki **Eklenecek kayıtlar** hızlı sekmesinde **Filtre** 'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="b60df-350">In the **Replenishment** dialog box, on the **Records to include** FastTab, select **Filter**.</span></span>
1. <span data-ttu-id="b60df-351">**Sorgulama** iletişim kutusundaki **Aralık** sekmesinde, varsayılan tablo satırını aşağıdaki şekilde düzenleyin:</span><span class="sxs-lookup"><span data-stu-id="b60df-351">In the **Inquiry** dialog box, on the **Range** tab, edit the default table row in the following way:</span></span>

    - <span data-ttu-id="b60df-352">**Tablo:** _Stok yenileme şablonları_ 'nı seçin.</span><span class="sxs-lookup"><span data-stu-id="b60df-352">**Table:** Select _Replenishment templates_.</span></span>
    - <span data-ttu-id="b60df-353">**Türetilmiş tablo:** _Stok yenileme şablonları_ 'nı seçin.</span><span class="sxs-lookup"><span data-stu-id="b60df-353">**Derived table:** Select _Replenishment templates_.</span></span>
    - <span data-ttu-id="b60df-354">**Alan:** _Stok yenileme şablonu_ 'nu seçin.</span><span class="sxs-lookup"><span data-stu-id="b60df-354">**Field:** Select _Replenishment template_.</span></span>
    - <span data-ttu-id="b60df-355">**Ölçütler:** _Bölge min/maks stok yenileme_ 'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="b60df-355">**Criteria:** Select _Zone min/max replen_.</span></span> <span data-ttu-id="b60df-356">Bu stok yenileme şablonu, bu senaryo için tanıtım verilerini hazırlarken oluşturduğunuz stok yenileme şablonudur.</span><span class="sxs-lookup"><span data-stu-id="b60df-356">This replenishment template is the replenishment template that you created while you were preparing the demo data for this scenario.</span></span>

1. <span data-ttu-id="b60df-357">Sorguyu kaydetmek için **Tamam** 'ı seçin ve **Stok yenileme** iletişim kutusuna dönün.</span><span class="sxs-lookup"><span data-stu-id="b60df-357">Select **OK** to save the query and go back to the **Replenishment** dialog box.</span></span>
1. <span data-ttu-id="b60df-358">Stok yenileme şablonunu çalıştırmak için **Tamam** 'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="b60df-358">Select **OK** to run the replenishment template.</span></span>

<span data-ttu-id="b60df-359">*TOPLU İŞ* bölgesinden stok çekmek ve bunu *KAT* bölgesinde stok yenilemek için artık stok yenileme işi oluşturulmuştur.</span><span class="sxs-lookup"><span data-stu-id="b60df-359">Replenishment work is now created to pick inventory from the *BULK* zone and replenish it to the *FLOOR* zone.</span></span>

## <a name="notes-and-tips"></a><span data-ttu-id="b60df-360">Notlar ve ipuçları</span><span class="sxs-lookup"><span data-stu-id="b60df-360">Notes and tips</span></span>

<span data-ttu-id="b60df-361">Özellikle çalışma hakkında birkaç not ve ipucu:</span><span class="sxs-lookup"><span data-stu-id="b60df-361">Here are a few notes and tips for working with the feature:</span></span>

- <span data-ttu-id="b60df-362">İstenen bölgeye giden stok yenileme işi ayarlamak için, stok yenileme şablonu satırlarını ve yerleşim yönergelerini aşağıdaki yollardan biriyle bağlantılandırabilirsiniz:</span><span class="sxs-lookup"><span data-stu-id="b60df-362">To set up replenishment work that goes to the desired zone, you can link the replenishment template lines and location directives in either of the following ways:</span></span>

    - <span data-ttu-id="b60df-363">Yerleşim yönergesi başlık sorgusunu düzenleyin ve seçili stok yenileme şablonu satırlarına filtre uygulayın.</span><span class="sxs-lookup"><span data-stu-id="b60df-363">Edit the location directive header query, and filter the selected replenishment template lines.</span></span>
    - <span data-ttu-id="b60df-364">Stok yenileme şablonu satırında bir yönerge kodu kullanın ve bu kodu, koyma yerleşimi yönergesiyle eşleştirin.</span><span class="sxs-lookup"><span data-stu-id="b60df-364">Use a directive code on the replenishment template line, and match it to the put location directive.</span></span>

- <span data-ttu-id="b60df-365">Dinamik yerleşimleri kullanıyorsanız ve yerleşim yönergesi eylemi **Konsolide etme** stratejisini kullanacak şekilde ayarlandıysa, stok yenileme işi ya ilk uygun yerleşim için veya zaten stok içeren bir yerleşim için oluşturulacaktır.</span><span class="sxs-lookup"><span data-stu-id="b60df-365">If you're using dynamic locations, replenishment work will be created either for the first available location or for a location that already contains inventory, if the location directive action is set up to use the **Consolidate** strategy.</span></span>
- <span data-ttu-id="b60df-366">Bölgeler yerine sabit yerleşimler kullanıyorsanız [standart min/maks stok yenilemeyi](tasks/set-up-min-max-replenishment-process.md) kullanmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="b60df-366">If you're using fixed locations instead of zones, you should use [standard min/max replenishment](tasks/set-up-min-max-replenishment-process.md).</span></span>
