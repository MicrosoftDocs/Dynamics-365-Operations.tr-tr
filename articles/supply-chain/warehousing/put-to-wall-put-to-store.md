---
title: Duvara yerleştirme - mağazaya yerleştirme
description: Bu konu, Duvara yerleştirme - Mağazaya yerleştirme işlevi hakkında bilgi sağlar. Bu işlev, bir ürünü, yapılandırılabilir ölçütlere göre bir ön paketleme hazırlık alanıyla birleştirmeniz gereken senaryoları işlemenize olanak tanır. Tek bir hedef plakaya malzeme çekme ve küme malzeme çekmeye göre daha fazla yerine koyma konumu kullanma olanağı sağladığından, malzeme çekme süresinin azalmasına yardımcı olur.
author: Mirzaab
ms.date: 07/16/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSLocationType, WHSLocationProfile, WHSLocation, WHSPackProfile, WHSWaveStepCode, WHSOutboundSortTemplate, WHSPostMethod, WHSWaveTemplateTable, WHSLocDirTable, WHSWorkClass, WHSWorkTemplateTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-16
ms.dyn365.ops.version: Release 10.0.9
ms.openlocfilehash: cf34a61d0b3f784b5a424473588d05bf8703635c
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/01/2021
ms.locfileid: "5823299"
---
# <a name="put-to-wall---put-to-store"></a><span data-ttu-id="2bc62-105">Duvara yerleştirme - mağazaya yerleştirme</span><span class="sxs-lookup"><span data-stu-id="2bc62-105">Put to wall - put to store</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="2bc62-106">*Duvara yerleştirme - mağazaya yerleştirme* işlevi, bir ürünü, yapılandırılabilir ölçütlere göre bir ön paketleme hazırlık alanıyla birleştirmeniz gereken senaryoları işlemenize olanak tanır.</span><span class="sxs-lookup"><span data-stu-id="2bc62-106">The *Put to wall - put to store* functionality lets you handle scenarios where you must consolidate a product to a prepack staging area, based on configurable criteria.</span></span> <span data-ttu-id="2bc62-107">Bu işlev tek bir hedef plakaya malzeme çekme işlemi yapılmasına izin verdiğinden ve küme malzeme çekmeye göre daha fazla yerleştirme konumu kullanılmasına olanak sağladığından, mağazalara sevkiyat yapan veya küçük miktarlı maddeleri işleyen şirketler, azalan malzeme çekme süresinden faydalanacaktır.</span><span class="sxs-lookup"><span data-stu-id="2bc62-107">Because this functionality allows for picking to a single target license plate and can use more put positions than cluster picking, companies that ship to stores or handle small items will benefit from decreased picking time.</span></span>

<span data-ttu-id="2bc62-108">Bu işlev için iş akışı, çekilen ürünü çeşitli türlerde konteynerlerde dağıtılmak üzere bir tasnif yerleşimine yönlendirir.</span><span class="sxs-lookup"><span data-stu-id="2bc62-108">The workflow for this functionality directs picked product to a sorting location for distribution into various types of containers.</span></span> <span data-ttu-id="2bc62-109">Genellikle, her tasnif yerleşimi birden fazla tasnif konumu içerir.</span><span class="sxs-lookup"><span data-stu-id="2bc62-109">Generally, each sorting location includes multiple sort positions.</span></span> <span data-ttu-id="2bc62-110">Her tasnif konumu iş süreci tarafından ayarlanan ölçütlere göre atanır.</span><span class="sxs-lookup"><span data-stu-id="2bc62-110">Each sort position is assigned according to the criteria that are set by the business process.</span></span> <span data-ttu-id="2bc62-111">Tipik ölçüt son varış yeri, sevkiyat veya yüktür.</span><span class="sxs-lookup"><span data-stu-id="2bc62-111">Typical criteria are the final destination, shipment, or load.</span></span> <span data-ttu-id="2bc62-112">Ürün alındıktan sonra sipariş, hedef, sevkiyat veya yük ile ilişkilendirilmiş miktara dayalı olarak her bir tasnif konumuna dağıtılır.</span><span class="sxs-lookup"><span data-stu-id="2bc62-112">After a product arrives, it's distributed to each sort position, based on the quantity that is associated with the order, destination, shipment, or load.</span></span> <span data-ttu-id="2bc62-113">Konteyner dolduğunda veya tamamlandığında, iş sürecine bağlı olarak daha fazla işlem yapmak amacıyla bir hazırlama yerleşimine veya sevkiyat yerleşimine taşınır.</span><span class="sxs-lookup"><span data-stu-id="2bc62-113">When a container is full or complete, it's moved to a staging location or a shipping location for further handling, depending on the business process.</span></span>

<span data-ttu-id="2bc62-114">Bu ambarlama işlevi, ışık yönlendirmeli ayrıştırma ve zorla açma gibi diğer adlarla da bilinir.</span><span class="sxs-lookup"><span data-stu-id="2bc62-114">This warehousing functionality is also referred to by other names, such as put-to-light and break opens.</span></span>

## <a name="turn-on-the-outbound-sorting-feature"></a><span data-ttu-id="2bc62-115">Giden tasnif özelliğini açma</span><span class="sxs-lookup"><span data-stu-id="2bc62-115">Turn on the Outbound sorting feature</span></span>

<span data-ttu-id="2bc62-116">*Duvara yerleştirme - mağazaya yerleştirme* işlevini kullanabilmeniz için *Çıkış tasnifi* özelliğinin sisteminizde açık olması gerekir.</span><span class="sxs-lookup"><span data-stu-id="2bc62-116">Before you can use the *Put to wall - put to store* functionality, the *Outbound sorting* feature must be turned on in your system.</span></span> <span data-ttu-id="2bc62-117">Yöneticiler özellik durumunu denetlemek ve gerekirse etkinleştirmek için [özellik yönetimi](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) çalışma alanını kullanabilir.</span><span class="sxs-lookup"><span data-stu-id="2bc62-117">Admins can use the [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) workspace to check the status of the feature and turn it on if it's required.</span></span> <span data-ttu-id="2bc62-118">Burada, özellik aşağıdaki şekilde listelenmiştir:</span><span class="sxs-lookup"><span data-stu-id="2bc62-118">There, the feature is listed in the following way:</span></span>

- <span data-ttu-id="2bc62-119">**Modül:** *Ambar yönetimi*</span><span class="sxs-lookup"><span data-stu-id="2bc62-119">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="2bc62-120">**Özellik adı:** *Giden tasnif*</span><span class="sxs-lookup"><span data-stu-id="2bc62-120">**Feature name:** *Outbound sorting*</span></span>

<span data-ttu-id="2bc62-121">*Çıkış tasnifi* özelliği, açıksa *Kuruluş genelinde dalga adımı kodu* özelliğiyle birlikte kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="2bc62-121">The *Outbound sorting* feature can be used in conjunction with the *Organization wide wave step code* feature if it's turned on.</span></span> <span data-ttu-id="2bc62-122">Dalga adım kodlarında ayarlanmış önceden tanımlı kodlar kullanacaksanız da bu özelliği etkinleştirmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="2bc62-122">You must also turn on this feature if you will use predefined codes that are set up in wave step codes.</span></span> <span data-ttu-id="2bc62-123">**Özellik yönetimi** çalışma alanındabu özellik aşağıdaki şekilde listelenir:</span><span class="sxs-lookup"><span data-stu-id="2bc62-123">In the **Feature management** workspace, this feature is listed in the following way:</span></span>

- <span data-ttu-id="2bc62-124">**Modül:** *Ambar yönetimi*</span><span class="sxs-lookup"><span data-stu-id="2bc62-124">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="2bc62-125">**Özellik adı:** *Kuruluş genelindeki dalga adım kodu:*</span><span class="sxs-lookup"><span data-stu-id="2bc62-125">**Feature name:** *Organization wide wave step code*</span></span>

## <a name="setup"></a><span data-ttu-id="2bc62-126">Ayar</span><span class="sxs-lookup"><span data-stu-id="2bc62-126">Setup</span></span>

<span data-ttu-id="2bc62-127">Bu demo için, standart Contoso verileri ve ambar *62* kullanılır.</span><span class="sxs-lookup"><span data-stu-id="2bc62-127">For this demo, standard Contoso data and warehouse *62* are used.</span></span> <span data-ttu-id="2bc62-128">Daha sonra belirtilen bazı eklemeler de kullanılmıştır.</span><span class="sxs-lookup"><span data-stu-id="2bc62-128">Some additions that are noted later are also used.</span></span>

### <a name="location-type"></a><span data-ttu-id="2bc62-129">Yerleşim türü</span><span class="sxs-lookup"><span data-stu-id="2bc62-129">Location type</span></span>

1. <span data-ttu-id="2bc62-130">**Ambar yönetimi \> Kurulum \> Ambar \> Yerleşim türleri** öğesine gidin.</span><span class="sxs-lookup"><span data-stu-id="2bc62-130">Go to **Warehouse management \> Setup \> Warehouse \> Location types**.</span></span>
1. <span data-ttu-id="2bc62-131">Eylem bölmesinde, tasnif için yerleşim türü oluşturmak üzere **Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="2bc62-131">On the Action Pane, select **New** to create a location type for sorting.</span></span>
1. <span data-ttu-id="2bc62-132">Aşağıdaki değerleri ayarlayın:</span><span class="sxs-lookup"><span data-stu-id="2bc62-132">Set the following values:</span></span>

    - <span data-ttu-id="2bc62-133">**Yerleşim türü:** *TASNİF*</span><span class="sxs-lookup"><span data-stu-id="2bc62-133">**Location type:** *SORT*</span></span>
    - <span data-ttu-id="2bc62-134">**Açıklama:** *Tasnif*</span><span class="sxs-lookup"><span data-stu-id="2bc62-134">**Description:** *Sort*</span></span>

1. <span data-ttu-id="2bc62-135">**Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="2bc62-135">Select **Save**.</span></span>

### <a name="warehouse-management-parameters"></a><span data-ttu-id="2bc62-136">Ambar yönetim parametreleri</span><span class="sxs-lookup"><span data-stu-id="2bc62-136">Warehouse management parameters</span></span>

1. <span data-ttu-id="2bc62-137">**Ambar yönetimi \> Kurulum \> Ambar yönetim parametreleri**'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="2bc62-137">Go to **Warehouse management \> Setup \> Warehouse management parameters**.</span></span>
1. <span data-ttu-id="2bc62-138">**Genel** sekmesinde **Yerleşim türleri** hızlı sekmesinde **Tasnif yerleşimi türü** alanına *TASNİF* girin.</span><span class="sxs-lookup"><span data-stu-id="2bc62-138">On the **General** tab, on the **Location types** FastTab, in the **Sorting location type** field, enter *SORT*.</span></span>
1. <span data-ttu-id="2bc62-139">**Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="2bc62-139">Select **Save**.</span></span>

### <a name="location-profile"></a><span data-ttu-id="2bc62-140">Yerleşim profili</span><span class="sxs-lookup"><span data-stu-id="2bc62-140">Location profile</span></span>

1. <span data-ttu-id="2bc62-141">**Ambar yönetimi \> Kurulum \> Ambar \> Konum profilleri**'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="2bc62-141">Go to **Warehouse management \> Setup \> Warehouse \> Location profiles**.</span></span>
1. <span data-ttu-id="2bc62-142">Eylem bölmesinde, tasnif yerleşimi için yerleşim profili oluşturmak üzere **Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="2bc62-142">On the Action Pane, select **New** to create a location profile for the sorting location.</span></span>
1. <span data-ttu-id="2bc62-143">Üst bilgide aşağıdaki değerleri ayarlayın:</span><span class="sxs-lookup"><span data-stu-id="2bc62-143">In the header, set the following values:</span></span>

    - <span data-ttu-id="2bc62-144">**Yerleşim profili kimliği:** *Tasnif*</span><span class="sxs-lookup"><span data-stu-id="2bc62-144">**Location profile ID:** *Sort*</span></span>
    - <span data-ttu-id="2bc62-145">**Ad:** *Tasnif*</span><span class="sxs-lookup"><span data-stu-id="2bc62-145">**Name:** *Sort*</span></span>

1. <span data-ttu-id="2bc62-146">**Genel** hızlı sekmesinde, aşağıdaki değerleri ayarlayın:</span><span class="sxs-lookup"><span data-stu-id="2bc62-146">On the **General** FastTab, set the following values:</span></span>

    - <span data-ttu-id="2bc62-147">**Yerleşim biçimi:** *PAKETLEME*</span><span class="sxs-lookup"><span data-stu-id="2bc62-147">**Location format:** *PACK*</span></span>
    - <span data-ttu-id="2bc62-148">**Yerleşim türü:** *TASNİF*</span><span class="sxs-lookup"><span data-stu-id="2bc62-148">**Location type:** *SORT*</span></span>
    - <span data-ttu-id="2bc62-149">**Plaka izleme kullan:** *Evet*</span><span class="sxs-lookup"><span data-stu-id="2bc62-149">**Use license plate tracking:** *Yes*</span></span>
    - <span data-ttu-id="2bc62-150">**Karışık maddelere izin ver:** *Evet*</span><span class="sxs-lookup"><span data-stu-id="2bc62-150">**Allow mixed items:** *Yes*</span></span>
    - <span data-ttu-id="2bc62-151">**Karışık stok durumlarına izin ver:** *Evet*</span><span class="sxs-lookup"><span data-stu-id="2bc62-151">**Allow mixed inventory statuses:** *Yes*</span></span>

1. <span data-ttu-id="2bc62-152">**Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="2bc62-152">Select **Save**.</span></span>

### <a name="locations"></a><span data-ttu-id="2bc62-153">Yerleşimler</span><span class="sxs-lookup"><span data-stu-id="2bc62-153">Locations</span></span>

1. <span data-ttu-id="2bc62-154">**Ambar yönetimi \> Kurulum \> Ambar \> Konumlar** öğesine gidin.</span><span class="sxs-lookup"><span data-stu-id="2bc62-154">Go to **Warehouse management \> Setup \> Warehouse \> Locations**.</span></span>
1. <span data-ttu-id="2bc62-155">**Yerleşim için denetleme basamakları oluştur** onay kutusunu temizleyin.</span><span class="sxs-lookup"><span data-stu-id="2bc62-155">Clear the **Generate check digits for location** check box.</span></span>
1. <span data-ttu-id="2bc62-156">Eylem bölmesinde **Yeni**'yi seçin ve ardından aşağıdaki değerleri ayarlayın:</span><span class="sxs-lookup"><span data-stu-id="2bc62-156">On the Action Pane, select **New**, and then set the following values:</span></span>

    - <span data-ttu-id="2bc62-157">**Ambar:** *62*</span><span class="sxs-lookup"><span data-stu-id="2bc62-157">**Warehouse:** *62*</span></span>
    - <span data-ttu-id="2bc62-158">**Yerleşim:** *Tasnif*</span><span class="sxs-lookup"><span data-stu-id="2bc62-158">**Location:** *Sort*</span></span>
    - <span data-ttu-id="2bc62-159">**Yerleşim profili kimliği:** *Tasnif*</span><span class="sxs-lookup"><span data-stu-id="2bc62-159">**Location profile ID:** *Sort*</span></span>

1. <span data-ttu-id="2bc62-160">**Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="2bc62-160">Select **Save**.</span></span>

### <a name="packing-profiles"></a><span data-ttu-id="2bc62-161">Paketleme profilleri</span><span class="sxs-lookup"><span data-stu-id="2bc62-161">Packing profiles</span></span>

1. <span data-ttu-id="2bc62-162">**Ambar yönetimi \> Kurulum \> Paketleme \> Paketleme profilleri**'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="2bc62-162">Go to **Warehouse management \> Setup \> Packing \> Packing profiles**.</span></span>
1. <span data-ttu-id="2bc62-163">Eylem bölmesinde **Yeni**'yi seçin ve ardından aşağıdaki değerleri ayarlayın:</span><span class="sxs-lookup"><span data-stu-id="2bc62-163">On the Action Pane, select **New**, and then set the following values:</span></span>

    - <span data-ttu-id="2bc62-164">**Paketleme profili kodu:** *Tasnif*</span><span class="sxs-lookup"><span data-stu-id="2bc62-164">**Packing profile ID:** *Sort*</span></span>
    - <span data-ttu-id="2bc62-165">**Açıklama:** *Tasnif*</span><span class="sxs-lookup"><span data-stu-id="2bc62-165">**Description:** *Sort*</span></span>
    - <span data-ttu-id="2bc62-166">**Konteyner paketleme ilkesi:** Bu alanı boş bırakın.</span><span class="sxs-lookup"><span data-stu-id="2bc62-166">**Container packing policy:** Leave this field blank.</span></span>
    - <span data-ttu-id="2bc62-167">**Konteyner kimliği modu:** *Otomatik*</span><span class="sxs-lookup"><span data-stu-id="2bc62-167">**Container ID mode:** *Auto*</span></span>
    - <span data-ttu-id="2bc62-168">**Konteyner türü:** *PALET 48x48*</span><span class="sxs-lookup"><span data-stu-id="2bc62-168">**Container type:** *PALLET 48X48*</span></span>
    - <span data-ttu-id="2bc62-169">**Konteyner kapatma sırasında konteyneri otomatik oluştur:** Bu alanı boş bırakın.</span><span class="sxs-lookup"><span data-stu-id="2bc62-169">**Autocreate container at container close:** Leave this field blank.</span></span>

1. <span data-ttu-id="2bc62-170">**Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="2bc62-170">Select **Save**.</span></span>

### <a name="wave-step-codes"></a><span data-ttu-id="2bc62-171">Dalga adım kodları</span><span class="sxs-lookup"><span data-stu-id="2bc62-171">Wave step codes</span></span>

<span data-ttu-id="2bc62-172">*Kuruluş genelinde dalga adımı kodu* özelliğini etkinleştirdiyseniz, aşağıdaki kodu ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="2bc62-172">If you turned on the *Organization wide wave step code* feature, set up the following code.</span></span>

1. <span data-ttu-id="2bc62-173">**Ambar yönetimi \> Kurulum \> Dalgalar \> Dalga adımı kodları**'na gidin.</span><span class="sxs-lookup"><span data-stu-id="2bc62-173">Go to **Warehouse management \> Setup \> Waves \> Wave step codes**.</span></span>
1. <span data-ttu-id="2bc62-174">Eylem bölmesinde **Yeni**'yi seçin ve ardından aşağıdaki değerleri ayarlayın:</span><span class="sxs-lookup"><span data-stu-id="2bc62-174">On the Action Pane, select **New**, and then set the following values:</span></span>

    - <span data-ttu-id="2bc62-175">**Dalga adımı kodu:** *Tasnif*</span><span class="sxs-lookup"><span data-stu-id="2bc62-175">**Wave step code:** *Sort*</span></span>
    - <span data-ttu-id="2bc62-176">**Dalga adımı açıklaması:** *Tasnif*</span><span class="sxs-lookup"><span data-stu-id="2bc62-176">**Wave step description:** *Sort*</span></span>
    - <span data-ttu-id="2bc62-177">**Dalga adımı türü:** *Tasnif şablonu*</span><span class="sxs-lookup"><span data-stu-id="2bc62-177">**Wave step type:** *Sort template*</span></span>

1. <span data-ttu-id="2bc62-178">**Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="2bc62-178">Select **Save**.</span></span>

### <a name="outbound-sorting-template"></a><span data-ttu-id="2bc62-179">Giden tasnif şablonu</span><span class="sxs-lookup"><span data-stu-id="2bc62-179">Outbound sorting template</span></span>

<span data-ttu-id="2bc62-180">Tasnif şablonu, tasnif konumlarının oluşturulup oluşturulmayacağını, hangi ölçütlerin kullanılacağını ve tasnif işleminin diğer özniteliklerini denetler.</span><span class="sxs-lookup"><span data-stu-id="2bc62-180">The sorting template controls whether sort positions are created, what criteria are used, and other attributes of the sorting process.</span></span>

1. <span data-ttu-id="2bc62-181">**Ambar Yönetimi \> Kurulum \> Paketleme \> Giden tasnif şablonu**'na gidin.</span><span class="sxs-lookup"><span data-stu-id="2bc62-181">Go to **Warehouse management \> Setup \> Packing \> Outbound sorting template**.</span></span>
1. <span data-ttu-id="2bc62-182">Eylem bölmesinde, bir tasnif şablonu oluşturmak için **Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="2bc62-182">On the Action Pane, select **New** to create a sorting template.</span></span>
1. <span data-ttu-id="2bc62-183">Yeni şablonun üst bilgisinde aşağıdaki değerleri ayarlayın:</span><span class="sxs-lookup"><span data-stu-id="2bc62-183">In the header of the new template, set the following values:</span></span>

    - <span data-ttu-id="2bc62-184">**Giden tasnif şablonu kodu:** *Dalga Tasnif*</span><span class="sxs-lookup"><span data-stu-id="2bc62-184">**Outbound sorting template ID:** *Wave Sort*</span></span>
    - <span data-ttu-id="2bc62-185">**Açıklama:** *Dalga tasnif*</span><span class="sxs-lookup"><span data-stu-id="2bc62-185">**Description:** *Wave sort*</span></span>
    - <span data-ttu-id="2bc62-186">**Tasnif şablonu türü:** *Dalga talebi*</span><span class="sxs-lookup"><span data-stu-id="2bc62-186">**Sort template type:** *Wave demand*</span></span>

        <span data-ttu-id="2bc62-187">Bu alan, tasnif şablonunun kullanıldığı işlemi tanımlar.</span><span class="sxs-lookup"><span data-stu-id="2bc62-187">This field defines the process that the sorting template is used for.</span></span> <span data-ttu-id="2bc62-188">Aşağıdaki değerler kullanılabilir:</span><span class="sxs-lookup"><span data-stu-id="2bc62-188">The following values are available:</span></span>

        - <span data-ttu-id="2bc62-189">**Dalga talebi**: Tasnif şablonu *Duvara yerleştir* işlemi için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="2bc62-189">**Wave demand** – The sorting template is used for the *Put to wall* process.</span></span> <span data-ttu-id="2bc62-190">Bu şablon türü, paketleme istasyonunu atlamak ve stoğu doğrudan dalga üzerinden işlemek için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="2bc62-190">This template type is used to bypass the pack station and process inventory directly out of the wave.</span></span> <span data-ttu-id="2bc62-191">Bu türü yalnızca **tasnif** dalga işlemi yöntemi dalga şablonuna dahil edilmişse kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="2bc62-191">You can use this type only if the **sorting** wave process method is included in the wave template.</span></span>
        - <span data-ttu-id="2bc62-192">**Konteyner**: Tasnif şablonu *Paketlemeden sonra palet oluşturma* işlemi için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="2bc62-192">**Container** – The sorting template is used for the *Pallet building after packing* process.</span></span> <span data-ttu-id="2bc62-193">Bu şablon türü paketleme istasyonunda kapatılmış olan ve paletler üzerinde tasnif edilmesi gereken konteynerleri işlemek için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="2bc62-193">This template type is used to process containers that are closed at the pack station and must be sorted onto pallets.</span></span>

    - <span data-ttu-id="2bc62-194">**Ambar:** *62*</span><span class="sxs-lookup"><span data-stu-id="2bc62-194">**Warehouse:** *62*</span></span>
    - <span data-ttu-id="2bc62-195">**Yerleşim:** *Tasnif*</span><span class="sxs-lookup"><span data-stu-id="2bc62-195">**Location:** *Sort*</span></span>

1. <span data-ttu-id="2bc62-196">**Genel** hızlı sekmesinde, aşağıdaki değerleri ayarlayın:</span><span class="sxs-lookup"><span data-stu-id="2bc62-196">On the **General** FastTab, set the following values:</span></span>

    - <span data-ttu-id="2bc62-197">**Tasnif doğrulaması:** *Konum tarama*</span><span class="sxs-lookup"><span data-stu-id="2bc62-197">**Sort verification:** *Position scan*</span></span>

        <span data-ttu-id="2bc62-198">Bu alan, tasnif sırasında gerekli olan doğrulamayı tanımlar.</span><span class="sxs-lookup"><span data-stu-id="2bc62-198">This field defines the verification that is required during sorting.</span></span> <span data-ttu-id="2bc62-199">Aşağıdaki değerler kullanılabilir:</span><span class="sxs-lookup"><span data-stu-id="2bc62-199">The following values are available:</span></span>

        - <span data-ttu-id="2bc62-200">Hiçbiri</span><span class="sxs-lookup"><span data-stu-id="2bc62-200">None</span></span>
        - <span data-ttu-id="2bc62-201">Plaka taraması</span><span class="sxs-lookup"><span data-stu-id="2bc62-201">License plate scan</span></span>
        - <span data-ttu-id="2bc62-202">Konum taraması</span><span class="sxs-lookup"><span data-stu-id="2bc62-202">Position scan</span></span>

    - <span data-ttu-id="2bc62-203">**Pozisyon kapanışında iş oluştur:** *Evet*</span><span class="sxs-lookup"><span data-stu-id="2bc62-203">**Create work on position close:** *Yes*</span></span>

        <span data-ttu-id="2bc62-204">Bu seçenek *Evet* olarak ayarlandığında, konum kapatıldığı zaman stoğu nihai sevkiyat yerleşimine taşımak için iş oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="2bc62-204">If this option is set to *Yes*, when the position is closed, work will be created to move inventory to the final shipping location.</span></span> <span data-ttu-id="2bc62-205">*Hayır* olarak ayarlanırsa, konum kapatıldığında stok anında sipariş için çekilir.</span><span class="sxs-lookup"><span data-stu-id="2bc62-205">If it's set to *No*, inventory will immediately be picked to the order when the position is closed.</span></span>

    - <span data-ttu-id="2bc62-206">**Konum atama:** *El ile*</span><span class="sxs-lookup"><span data-stu-id="2bc62-206">**Position assignment:** *Manual*</span></span>

        <span data-ttu-id="2bc62-207">Bu alan konum atama türünü tanımlar.</span><span class="sxs-lookup"><span data-stu-id="2bc62-207">This field defines the type of position assignment.</span></span> <span data-ttu-id="2bc62-208">Aşağıdaki değerler kullanılabilir:</span><span class="sxs-lookup"><span data-stu-id="2bc62-208">The following values are available:</span></span>

        - <span data-ttu-id="2bc62-209">**El ile**: Kullanıcının her zaman stoğun hangi konumda sıralanacağını belirtmesi gerekir.</span><span class="sxs-lookup"><span data-stu-id="2bc62-209">**Manual** – The user must always indicate which position the inventory should be sorted to.</span></span>
        - <span data-ttu-id="2bc62-210">**Otomaik**: Sistem tasnif şablonu dökümlerini temel alarak mümkün olduğunda stoğu otomatik olarak bir konuma yönlendirir.</span><span class="sxs-lookup"><span data-stu-id="2bc62-210">**Automatic** – The system will automatically guide the inventory to a position whenever it can, based on the sort template breaks.</span></span>

    - <span data-ttu-id="2bc62-211">**Tasnif konumu ata ölçütü:** *Yalnızca boş konum kullan*</span><span class="sxs-lookup"><span data-stu-id="2bc62-211">**Assign sort position criteria:** *Only use empty position*</span></span>

        <span data-ttu-id="2bc62-212">Bu alan, tasnif konumlarında zaten mevcut olan stoğun talep için konum atanırken dikkate alınıp alınmayacağını kontrol eder.</span><span class="sxs-lookup"><span data-stu-id="2bc62-212">This field controls whether inventory that is already present on sort positions is taken into account when a position is assigned for the demand.</span></span> <span data-ttu-id="2bc62-213">Aşağıdaki değerler kullanılabilir:</span><span class="sxs-lookup"><span data-stu-id="2bc62-213">The following values are available:</span></span>

        - <span data-ttu-id="2bc62-214">**Yalnızca boş konum kullan**: Önceden ilişkilendirilmiş stoğu olan konumlar dikkate alınacaktır</span><span class="sxs-lookup"><span data-stu-id="2bc62-214">**Only use empty position** – Positions that already have inventory associated with them will be taken into account</span></span>
        - <span data-ttu-id="2bc62-215">**Konumun boş olduğunu varsay**: Konumda zaten olan tüm stoklar atama sırasında yok sayılır.</span><span class="sxs-lookup"><span data-stu-id="2bc62-215">**Assume position empty** – Any inventory that is already on the position will be disregarded during assignment.</span></span> <span data-ttu-id="2bc62-216">Kullanılabilir tüm konumlar kullanılır.</span><span class="sxs-lookup"><span data-stu-id="2bc62-216">All available positions will be used.</span></span>

    - <span data-ttu-id="2bc62-217">**Dalga adımı kodu:** *Tasnif*</span><span class="sxs-lookup"><span data-stu-id="2bc62-217">**Wave step code:** *Sort*</span></span>

        <span data-ttu-id="2bc62-218">*Kuruluş genelinde dalga adımı kodu* özelliği açıksa, *Tasnif* dalga adımı kodu dalga adım kodlarında da ayarlanmalıdır.</span><span class="sxs-lookup"><span data-stu-id="2bc62-218">If the *Organization wide wave step code* feature is turned on, the *Sort* wave step code must also be set up in wave step codes.</span></span>

    - <span data-ttu-id="2bc62-219">**Tasnif konumunu otomatik kapat:** *Evet*</span><span class="sxs-lookup"><span data-stu-id="2bc62-219">**Auto close sort position:** *Yes*</span></span>

        <span data-ttu-id="2bc62-220">Bu seçenek *Evet* olarak ayarlandığında, konuma gelen tüm iş tamamlandığında, tasnif konumu otomatik olarak kapatılır.</span><span class="sxs-lookup"><span data-stu-id="2bc62-220">If this option is set to *Yes*, the sort position will automatically be closed when all work that comes to the position has been completed.</span></span>

    - <span data-ttu-id="2bc62-221">**Tasnif konumlarının sayısı:** *3*</span><span class="sxs-lookup"><span data-stu-id="2bc62-221">**Number of sort positions:** *3*</span></span>

        <span data-ttu-id="2bc62-222">Bu alan, sistemin oluşturulacağı maksimum tasnif konumu sayısını tanımlar.</span><span class="sxs-lookup"><span data-stu-id="2bc62-222">This field defines the maximum number of sort positions that the system will create.</span></span>

    - <span data-ttu-id="2bc62-223">**Tasnif konumu öneki:** *SP-*</span><span class="sxs-lookup"><span data-stu-id="2bc62-223">**Sort position prefix:** *SP-*</span></span>

        <span data-ttu-id="2bc62-224">Bu alan, sistemin konum numarasından önce atadığı öneki tanımlar.</span><span class="sxs-lookup"><span data-stu-id="2bc62-224">This field defines the prefix that the system assigns before the position number.</span></span>

    - <span data-ttu-id="2bc62-225">**Tasnif konumunu otomatik paketle** *Evet*</span><span class="sxs-lookup"><span data-stu-id="2bc62-225">**Auto pack sort position:** *Yes*</span></span>

        <span data-ttu-id="2bc62-226">Bu seçenek *Evet* olarak ayarlandığında, konum kapatıldığında tasnif konumunda bulunan stok bir konteyner içinde paketlenir.</span><span class="sxs-lookup"><span data-stu-id="2bc62-226">If this option is set to *Yes*, the inventory on the sort position will be packed into a container when the position is closed.</span></span>

    - <span data-ttu-id="2bc62-227">**Paketleme profili kodu:** *Tasnif*</span><span class="sxs-lookup"><span data-stu-id="2bc62-227">**Packing profile ID:** *Sort*</span></span>

        <span data-ttu-id="2bc62-228">Bu alana, tasnif konumu bir konteynere paketlenceği zaman kullanılacak paketleme profilini tanımlar.</span><span class="sxs-lookup"><span data-stu-id="2bc62-228">This field defines the packing profile that will be used when the sort position is packed into a container.</span></span>

1. <span data-ttu-id="2bc62-229">Eylem bölmesinde, bu tasnif şablonu için kullanılan ölçütleri belirtmek üzere **Sorguyu düzenle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="2bc62-229">On the Action Pane, select **Edit query** to specify the criteria that are used for this sorting template.</span></span>
1. <span data-ttu-id="2bc62-230">Sorgu iletişim kutusunda, **Tasnif** sekmesinde bir satır eklemek için **Yeni**'yi seçin ve sonra aşağıdaki değerleri ayarlayın:</span><span class="sxs-lookup"><span data-stu-id="2bc62-230">In the query dialog box, on the **Sorting** tab, select **New** to add a line, and then set the following values:</span></span>

    - <span data-ttu-id="2bc62-231">**Tablo:** *ayrıntıları yükle*</span><span class="sxs-lookup"><span data-stu-id="2bc62-231">**Table:** *Load details*</span></span>
    - <span data-ttu-id="2bc62-232">**Türetilmiş tablo:** *ayrıntıları yükle*</span><span class="sxs-lookup"><span data-stu-id="2bc62-232">**Derived table:** *Load details*</span></span>
    - <span data-ttu-id="2bc62-233">**Alan:** *Sevkiyat kodu*</span><span class="sxs-lookup"><span data-stu-id="2bc62-233">**Field:** *Shipment ID*</span></span>
    - <span data-ttu-id="2bc62-234">**Arama yönü:** *Artan*</span><span class="sxs-lookup"><span data-stu-id="2bc62-234">**Search direction:** *Ascending*</span></span>

1. <span data-ttu-id="2bc62-235">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="2bc62-235">Select **OK**.</span></span>
1. <span data-ttu-id="2bc62-236">Aşağıdaki iletiyi alabilirsiniz: "Gruplama sıfırlanacak, devam edilsin mi?"</span><span class="sxs-lookup"><span data-stu-id="2bc62-236">You might receive the following message: "Grouping will be reset, continue?"</span></span> <span data-ttu-id="2bc62-237">**Evet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="2bc62-237">Select **Yes**.</span></span>

    <span data-ttu-id="2bc62-238">Eylem Bölmesindeki **Giden tasnif şablonu dökümleri** düğmesi kullanılabilir duruma gelir.</span><span class="sxs-lookup"><span data-stu-id="2bc62-238">The **Outbound sorting template breaks** button on the Action Pane becomes available.</span></span>

1. <span data-ttu-id="2bc62-239">Eylem Bölmesinde, **Giden tasnif şablonu dökümleri**'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="2bc62-239">On the Action Pane, select **Outbound sorting template breaks**.</span></span>
1. <span data-ttu-id="2bc62-240">Sevkiyat koduna göre gruplandırmak için **Alana göre gruplandır** onay kutusunu seçin.</span><span class="sxs-lookup"><span data-stu-id="2bc62-240">Select the **Group by field** check box to group by shipment ID.</span></span>

    <span data-ttu-id="2bc62-241">Bu ayar, her sevkiyat için dalga içindeki bir konteyner olan bir tasnif konumu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="2bc62-241">This setting will create one sort position per shipment that is a container in the wave.</span></span>

1. <span data-ttu-id="2bc62-242">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="2bc62-242">Select **OK**.</span></span>

### <a name="wave-process-methods"></a><span data-ttu-id="2bc62-243">Dalga işleme yöntemleri</span><span class="sxs-lookup"><span data-stu-id="2bc62-243">Wave process methods</span></span>

1. <span data-ttu-id="2bc62-244">**Ambar yönetimi \> Kurulum \> Dalgalar \> Dalga işleme yöntemleri**'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="2bc62-244">Go to **Warehouse management \> Setup \> Waves \> Wave process methods**.</span></span>
1. <span data-ttu-id="2bc62-245">Eylem bölmesinde, **Yöntemleri yeniden oluştur**'u seçin.</span><span class="sxs-lookup"><span data-stu-id="2bc62-245">On the Action Pane, select **Regenerate methods**.</span></span>

    <span data-ttu-id="2bc62-246">**Tasnif** yöntemi kullanılabilir yöntemler listesine eklenir ve bunun için *Sevkiyat* dalga şablonu türü seçilir.</span><span class="sxs-lookup"><span data-stu-id="2bc62-246">The **sorting** method is added to the list of available methods, and the *Shipping* wave template type is selected for it.</span></span>

### <a name="wave-templates"></a><span data-ttu-id="2bc62-247">Dalga şablonları</span><span class="sxs-lookup"><span data-stu-id="2bc62-247">Wave templates</span></span>

<span data-ttu-id="2bc62-248">Dalga talep tasnifi için kullanılan dalga şablonunu düzenleyin.</span><span class="sxs-lookup"><span data-stu-id="2bc62-248">Edit the wave template that is used for wave demand sorting.</span></span>

1. <span data-ttu-id="2bc62-249">**Ambar yönetimi \> Kurulum \> Dalgalar \> Dalga şablonları**'na gidin.</span><span class="sxs-lookup"><span data-stu-id="2bc62-249">Go to **Warehouse management \> Setup \> Waves \> Wave templates**.</span></span>
1. <span data-ttu-id="2bc62-250">**Dalga şablonu türü** alanında *Sevkiyat*'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="2bc62-250">In the **Wave template type** field, select *Shipping*.</span></span>
1. <span data-ttu-id="2bc62-251">Varolan **62 Sevkiyat varsayılanı** şablonunu seçin.</span><span class="sxs-lookup"><span data-stu-id="2bc62-251">Select the existing **62 Shipping default** template.</span></span>
1. <span data-ttu-id="2bc62-252">Eylem Bölmesi'nde, **Düzenle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="2bc62-252">On the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="2bc62-253">**Genel** hızlı sekmesinde, aşağıdaki değişiklikleri yapın:</span><span class="sxs-lookup"><span data-stu-id="2bc62-253">On the **General** FastTab, make the following changes:</span></span>

    - <span data-ttu-id="2bc62-254">**Dalgayı ambara serbest bırakma sırasında işle** seçeneğini *Hayır* olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="2bc62-254">Set the **Process wave at release to warehouse** option to *No*.</span></span>
    - <span data-ttu-id="2bc62-255">**Açık dalgalara ata** seçeneğini *Evet* olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="2bc62-255">Set the **Assign to open waves** option to *Yes*.</span></span>

1. <span data-ttu-id="2bc62-256">**Yöntemler** hızlı sekmesinde, **tasnif** yöntemini ayarlayın:</span><span class="sxs-lookup"><span data-stu-id="2bc62-256">On the **Methods** FastTab, set up the **sorting** method:</span></span>

    1. <span data-ttu-id="2bc62-257">**Kalan Yöntemler** kılavuzunda, **tasnif**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="2bc62-257">In the **Remaining Methods** grid, select **sorting**.</span></span>
    2. <span data-ttu-id="2bc62-258">**Tasnif** yöntemini **Seçili Yöntemler** kılavuzuna taşımak için sağ oku seçin.</span><span class="sxs-lookup"><span data-stu-id="2bc62-258">Select the right arrow button to move **sorting** to the **Selected Methods** grid.</span></span>
    3. <span data-ttu-id="2bc62-259">**Seçili Yöntemler** kılavuzunda, **tasnif**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="2bc62-259">In the **Selected Methods** grid, select **sorting**.</span></span>
    4. <span data-ttu-id="2bc62-260">**Dalga adımı kodu** alanını *Tasnif* olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="2bc62-260">Set the **Wave step code** field to *Sort*.</span></span>

1. <span data-ttu-id="2bc62-261">**Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="2bc62-261">Select **Save**.</span></span>

### <a name="mobile-device-menu-items"></a><span data-ttu-id="2bc62-262">Mobil cihaz menü öğeleri</span><span class="sxs-lookup"><span data-stu-id="2bc62-262">Mobile device menu items</span></span>

1. <span data-ttu-id="2bc62-263">**Ambar yönetimi \> Kurulum \> Mobil cihaz \> Mobil cihaz menüsü öğeleri**'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="2bc62-263">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu items**.</span></span>
1. <span data-ttu-id="2bc62-264">Eylem Bölmesinde, **Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="2bc62-264">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="2bc62-265">Üst bilgide aşağıdaki değerleri ayarlayın:</span><span class="sxs-lookup"><span data-stu-id="2bc62-265">In the header, set the following values:</span></span>

    - <span data-ttu-id="2bc62-266">**Menü öğesi adı:** *Tasnif*</span><span class="sxs-lookup"><span data-stu-id="2bc62-266">**Menu item name:** *Sort*</span></span>
    - <span data-ttu-id="2bc62-267">**Başlık:** *Tasnif*</span><span class="sxs-lookup"><span data-stu-id="2bc62-267">**Title:** *Sort*</span></span>
    - <span data-ttu-id="2bc62-268">**Mod:** *Dolaylı*</span><span class="sxs-lookup"><span data-stu-id="2bc62-268">**Mode:** *Indirect*</span></span>
    - <span data-ttu-id="2bc62-269">**Varolan çalışmayı kullan:** *Hayır*</span><span class="sxs-lookup"><span data-stu-id="2bc62-269">**Use existing work:** *No*</span></span>

1. <span data-ttu-id="2bc62-270">**Genel** hızlı sekmesinde, aşağıdaki değerleri ayarlayın:</span><span class="sxs-lookup"><span data-stu-id="2bc62-270">On the **General** FastTab, set the following values:</span></span>

    - <span data-ttu-id="2bc62-271">**Faaliyet kodu:** *Giden tasnif*</span><span class="sxs-lookup"><span data-stu-id="2bc62-271">**Activity code:** *Outbound sorting*</span></span>
    - <span data-ttu-id="2bc62-272">**İşlem kılavuzunu kullan:** *Evet* (varsayılan değer)</span><span class="sxs-lookup"><span data-stu-id="2bc62-272">**Use process guide:** *Yes* (default value)</span></span>
    - <span data-ttu-id="2bc62-273">**Giden tasnif şablonu kodu:** *Dalga Tasnif*</span><span class="sxs-lookup"><span data-stu-id="2bc62-273">**Outbound sorting template ID:** *Wave Sort*</span></span>

1. <span data-ttu-id="2bc62-274">**Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="2bc62-274">Select **Save**.</span></span>

### <a name="mobile-device-menu"></a><span data-ttu-id="2bc62-275">Mobil cihaz menüsü</span><span class="sxs-lookup"><span data-stu-id="2bc62-275">Mobile device menu</span></span>

1. <span data-ttu-id="2bc62-276">**Ambar yönetimi \> Kurulum \> Mobil cihaz \> Mobil cihaz menüsü**'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="2bc62-276">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu**.</span></span>
1. <span data-ttu-id="2bc62-277">Menüler listesinde **Giden**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="2bc62-277">In the list of menus, select **Outbound**.</span></span>
1. <span data-ttu-id="2bc62-278">Eylem Bölmesi'nde, **Düzenle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="2bc62-278">On the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="2bc62-279">**Kullanılabilir Menüler ve Menü Öğeleri** kılavuzunda, yeni oluşturduğunuz **Tasnif** menü öğesini bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="2bc62-279">In the **Available Menus And Menu Items** grid, find and select the **Sort** menu item that you just created.</span></span>
1. <span data-ttu-id="2bc62-280">**Tasnif** i **Menü Yapısı** kılavuzuna taşımak için sağ ok düğmesini seçin.</span><span class="sxs-lookup"><span data-stu-id="2bc62-280">Select the right arrow button to move **Sort** to the **Menu Structure** grid.</span></span> <span data-ttu-id="2bc62-281">Böylece, yeni menü öğesini **Giden** menüsüne eklersiniz.</span><span class="sxs-lookup"><span data-stu-id="2bc62-281">In this way, you add the menu item to the **Outbound** menu.</span></span>
1. <span data-ttu-id="2bc62-282">**Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="2bc62-282">Select **Save**.</span></span>

### <a name="location-directives"></a><span data-ttu-id="2bc62-283">Konum yönergeleri</span><span class="sxs-lookup"><span data-stu-id="2bc62-283">Location directives</span></span>

<span data-ttu-id="2bc62-284">Tasnif tamamlandıktan sonra oluşturulan işe kılavuz olacak yerleşim yönergeleri oluşturmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="2bc62-284">You must create location directives to guide the work that is created after the sorting is completed.</span></span>

1. <span data-ttu-id="2bc62-285">**Ambar Yönetimi \> Kurulum \> Konum yönergeleri** seçeneğine gidin.</span><span class="sxs-lookup"><span data-stu-id="2bc62-285">Go to **Warehouse management \> Setup \> Location directives**.</span></span>
1. <span data-ttu-id="2bc62-286">**İş emri türü** alanında *Tasnif edilen stoğu çekme*'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="2bc62-286">In the **Work order type** field, select *Sorted inventory picking*.</span></span>
1. <span data-ttu-id="2bc62-287">Eylem Bölmesinde, **Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="2bc62-287">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="2bc62-288">Üst bilgide aşağıdaki değerleri ayarlayın:</span><span class="sxs-lookup"><span data-stu-id="2bc62-288">In the header, set the following values:</span></span>

    - <span data-ttu-id="2bc62-289">**Sıra:** *1*</span><span class="sxs-lookup"><span data-stu-id="2bc62-289">**Sequence:** *1*</span></span>
    - <span data-ttu-id="2bc62-290">**Ad:** *Baydoor'a yerleştir*</span><span class="sxs-lookup"><span data-stu-id="2bc62-290">**Name:** *Put to Baydoor*</span></span>

1. <span data-ttu-id="2bc62-291">**Yerleşim yönergeleri** hızlı sekmesinde aşağıdaki değerleri ayarlayın:</span><span class="sxs-lookup"><span data-stu-id="2bc62-291">On the **Location directives** FastTab, set the following values:</span></span>

    - <span data-ttu-id="2bc62-292">**İş türü:** *Yerine koyma*</span><span class="sxs-lookup"><span data-stu-id="2bc62-292">**Work type:** *Put*</span></span>
    - <span data-ttu-id="2bc62-293">**Tesis:** *6*</span><span class="sxs-lookup"><span data-stu-id="2bc62-293">**Site:** *6*</span></span>
    - <span data-ttu-id="2bc62-294">**Ambar:** *62*</span><span class="sxs-lookup"><span data-stu-id="2bc62-294">**Warehouse:** *62*</span></span>
    - <span data-ttu-id="2bc62-295">**Yönerge kodu:** Boş bırakın.</span><span class="sxs-lookup"><span data-stu-id="2bc62-295">**Directive code:** Leave this field blank.</span></span>
    - <span data-ttu-id="2bc62-296">**Birden çok SKU:** *Hayır*</span><span class="sxs-lookup"><span data-stu-id="2bc62-296">**Multiple SKU:** *No*</span></span>

1. <span data-ttu-id="2bc62-297">**Satırlar** hızlı sekmesini kullanılabilir hale getirmek için **Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="2bc62-297">Select **Save** to make the **Lines** FastTab available.</span></span>
1. <span data-ttu-id="2bc62-298">**Satırlar** hızlı sekmesinde, **Yeni**'yi seçin ve sonra aşağıdaki değerleri ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="2bc62-298">On the **Lines** FastTab, select **New**, and then set the following values.</span></span> <span data-ttu-id="2bc62-299">Tüm diğer alanlar için varsayılan değerleri kabul edin.</span><span class="sxs-lookup"><span data-stu-id="2bc62-299">Accept the default values for all the other fields.</span></span>

    - <span data-ttu-id="2bc62-300">**Sıra numarası:** *1*</span><span class="sxs-lookup"><span data-stu-id="2bc62-300">**Sequence number:** *1*</span></span>
    - <span data-ttu-id="2bc62-301">**Başlangıç miktarı:** *0*</span><span class="sxs-lookup"><span data-stu-id="2bc62-301">**From quantity:** *0*</span></span>
    - <span data-ttu-id="2bc62-302">**Son miktar:** *1000000*</span><span class="sxs-lookup"><span data-stu-id="2bc62-302">**To quantity:** *1000000*</span></span>

1. <span data-ttu-id="2bc62-303">**Yerleşim Yönergesi Eylemleri** hızlı sekmesini kullanılabilir hale getirmek için **Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="2bc62-303">Select **Save** to make the **Location Directive Actions** FastTab available.</span></span>
1. <span data-ttu-id="2bc62-304">**Yerleşim Yönergesi Eylemleri** hızlı sekmesinde, **Yeni**'yi seçin ve sonra aşağıdaki değerleri ayarlayın:</span><span class="sxs-lookup"><span data-stu-id="2bc62-304">On the **Location Directive Actions** FastTab, select **New**, and then set the following values.</span></span> <span data-ttu-id="2bc62-305">Tüm diğer alanlar için varsayılan değerleri kabul edin.</span><span class="sxs-lookup"><span data-stu-id="2bc62-305">Accept the default values for all the other fields.</span></span>

    - <span data-ttu-id="2bc62-306">**Sıra numarası:** *1*</span><span class="sxs-lookup"><span data-stu-id="2bc62-306">**Sequence number:** *1*</span></span>
    - <span data-ttu-id="2bc62-307">**Ad:** *Baydoor*</span><span class="sxs-lookup"><span data-stu-id="2bc62-307">**Name:** *Baydoor*</span></span>

1. <span data-ttu-id="2bc62-308">**Yerleşim Yönergesi Eylemleri** hızlı sekmesinde **Sorguyu düzenle** düğmesini kullanılabilir hale getirmek için **Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="2bc62-308">Select **Save** to make the **Edit query** button on the **Location Directive Actions** FastTab available.</span></span>
1. <span data-ttu-id="2bc62-309">**Yerleşim Yönergesi Eylemleri** hızlı sekmesinde **Sorguyu düzenle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="2bc62-309">On the **Location Directive Actions** FastTab, select **Edit query**.</span></span>
1. <span data-ttu-id="2bc62-310">Sorgu iletişim kutusunda, **Aralık** sekmesinde, **Alan** alanının *Yerleşim* olarak ayarlandığı satırı bulun.</span><span class="sxs-lookup"><span data-stu-id="2bc62-310">In the query dialog box, on the **Range** tab, find the row where the **Field** field is set to *Location*.</span></span> <span data-ttu-id="2bc62-311">Bu satır için **Ölçüt** alanını *Baydoor* olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="2bc62-311">Set the **Criteria** field for this row to *Baydoor*.</span></span>
1. <span data-ttu-id="2bc62-312">Düzenlemeyi onaylamak için **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="2bc62-312">Select **OK** to confirm the edit.</span></span>

### <a name="work-classes"></a><span data-ttu-id="2bc62-313">İş sınıfları</span><span class="sxs-lookup"><span data-stu-id="2bc62-313">Work classes</span></span>

1. <span data-ttu-id="2bc62-314">**Ambar yönetimi \> Kurulum \> İş \> İş sınıfları** seçeneğine gidin.</span><span class="sxs-lookup"><span data-stu-id="2bc62-314">Go to **Warehouse management \> Setup \> Work \> Work classes**.</span></span>
1. <span data-ttu-id="2bc62-315">Eylem Bölmesinde, **Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="2bc62-315">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="2bc62-316">Üst bilgide aşağıdaki değerleri ayarlayın:</span><span class="sxs-lookup"><span data-stu-id="2bc62-316">In the header, set the following values:</span></span>

    - <span data-ttu-id="2bc62-317">**İş sınıfı kodu:** *Tasnif*</span><span class="sxs-lookup"><span data-stu-id="2bc62-317">**Work class ID:** *Sorting*</span></span>
    - <span data-ttu-id="2bc62-318">**Açıklama:** *Tasnif*</span><span class="sxs-lookup"><span data-stu-id="2bc62-318">**Description:** *Sorting*</span></span>
    - <span data-ttu-id="2bc62-319">**İş emri türü:** *Tasnif edilmiş stok çekme*</span><span class="sxs-lookup"><span data-stu-id="2bc62-319">**Work order type:** *Sorted inventory picking*</span></span>

1. <span data-ttu-id="2bc62-320">**Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="2bc62-320">Select **Save**.</span></span>

### <a name="work-templates"></a><span data-ttu-id="2bc62-321">İş şablonları</span><span class="sxs-lookup"><span data-stu-id="2bc62-321">Work templates</span></span>

1. <span data-ttu-id="2bc62-322">**Ambar yönetimi \> İş \> İş şablonları**'na gidin.</span><span class="sxs-lookup"><span data-stu-id="2bc62-322">Go to **Warehouse management \> Work \> Work templates**.</span></span>
1. <span data-ttu-id="2bc62-323">**İş siparişi türü** alanında *Satış siparişi*'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="2bc62-323">In the **Work order type** field, select *Sales orders*.</span></span>
1. <span data-ttu-id="2bc62-324">Kılavuzda **62 Paketleme için çek** iş şablonunu seçin.</span><span class="sxs-lookup"><span data-stu-id="2bc62-324">In the grid, select the **62 Pick to pack** work template.</span></span>
1. <span data-ttu-id="2bc62-325">Eylem Bölmesinde **İş başlığı sonları**'nı seçin.</span><span class="sxs-lookup"><span data-stu-id="2bc62-325">On the Action Pane, select **Work header breaks**.</span></span>
1. <span data-ttu-id="2bc62-326">Eylem Bölmesi'nde, **Düzenle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="2bc62-326">On the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="2bc62-327">**Alan adı** alanının *Sevkiyat Kodu* olarak ayarlandığı satırsa **Bu alan göre sınıflandır** onay kutusunu temizleyin.</span><span class="sxs-lookup"><span data-stu-id="2bc62-327">On the line where the **Field name** field is set to *Shipment ID*, clear the **Group by this field** check box.</span></span>
1. <span data-ttu-id="2bc62-328">**Kaydet**'i seçin ve sonra **İş başlığı sonları** iletişim kutusunu kapatın.</span><span class="sxs-lookup"><span data-stu-id="2bc62-328">Select **Save**, and then close the **Work header breaks** dialog box.</span></span>
1. <span data-ttu-id="2bc62-329">**İş emri türü** alanında *Tasnif edilen stoğu çekme*'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="2bc62-329">In the **Work order type** field, select *Sorted inventory picking*.</span></span>
1. <span data-ttu-id="2bc62-330">Yeni şablon oluşturmak için **Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="2bc62-330">Select **New** to create a work template.</span></span>
1. <span data-ttu-id="2bc62-331">**Genel bakış** bölümünde aşağıdaki değerleri ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="2bc62-331">In the **Overview** section, set the following values.</span></span> <span data-ttu-id="2bc62-332">Tüm diğer alanlar için varsayılan değerleri kabul edin.</span><span class="sxs-lookup"><span data-stu-id="2bc62-332">Accept the default values for all the other fields.</span></span>

    - <span data-ttu-id="2bc62-333">**İş şablonu:** *Tasnif edilmiş çekme*</span><span class="sxs-lookup"><span data-stu-id="2bc62-333">**Work template:** *Sorted picking*</span></span>
    - <span data-ttu-id="2bc62-334">**İş şablonu açıklaması:** *Tasnif edilmiş çekme*</span><span class="sxs-lookup"><span data-stu-id="2bc62-334">**Work template description:** *Sorted picking*</span></span>

1. <span data-ttu-id="2bc62-335">**İş Şablonu Ayrıntıları** bölümünü kullanılabilir hale getirmek için **Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="2bc62-335">Select **Save** to make the **Work Template Details** section available.</span></span>
1. <span data-ttu-id="2bc62-336">**İş Şablonu Ayrıntıları** bölümünde, iki satır oluşturacaksınız.</span><span class="sxs-lookup"><span data-stu-id="2bc62-336">In the **Work Template Details** section, you will create two lines.</span></span> <span data-ttu-id="2bc62-337">**Yeni**'yi seçin ve satır 1 için aşağıdaki değerleri ayarlayın:</span><span class="sxs-lookup"><span data-stu-id="2bc62-337">Select **New**, and then set the following values for line 1:</span></span>

    - <span data-ttu-id="2bc62-338">**İş türü:** *Çekme*</span><span class="sxs-lookup"><span data-stu-id="2bc62-338">**Work type:** *Pick*</span></span>
    - <span data-ttu-id="2bc62-339">**Zorunlu:** Seçili (= *Evet*)</span><span class="sxs-lookup"><span data-stu-id="2bc62-339">**Mandatory:** Selected (= *Yes*)</span></span>
    - <span data-ttu-id="2bc62-340">**İş sınıfı kodu:** *Tasnif*</span><span class="sxs-lookup"><span data-stu-id="2bc62-340">**Work class ID:** *Sorting*</span></span>

1. <span data-ttu-id="2bc62-341">**Yeni**'yi tekrar seçin ve satır 2 için aşağıdaki değerleri ayarlayın:</span><span class="sxs-lookup"><span data-stu-id="2bc62-341">Select **New** again, and then set the following values for line 2:</span></span>

    - <span data-ttu-id="2bc62-342">**İş türü:** *Yerine koyma*</span><span class="sxs-lookup"><span data-stu-id="2bc62-342">**Work type:** *Put*</span></span>
    - <span data-ttu-id="2bc62-343">**Zorunlu:** Seçili (= *Evet*)</span><span class="sxs-lookup"><span data-stu-id="2bc62-343">**Mandatory:** Selected (= *Yes*)</span></span>
    - <span data-ttu-id="2bc62-344">**İş sınıfı kodu:** *Tasnif*</span><span class="sxs-lookup"><span data-stu-id="2bc62-344">**Work class ID:** *Sorting*</span></span>

1. <span data-ttu-id="2bc62-345">**Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="2bc62-345">Select **Save**.</span></span>

## <a name="example-scenario"></a><span data-ttu-id="2bc62-346">Örnek senaryo</span><span class="sxs-lookup"><span data-stu-id="2bc62-346">Example scenario</span></span>

<span data-ttu-id="2bc62-347">Bu senaryo, ambarın yerleşimlerde küçük maddeleri depoladığı ve bu maddelerin sevk edilmeden önce kutular içinde paketlenmesinin gerekli olduğu ve paketleme istasyonu işlevinin gerçekten uygun olmadığı bir durumun benzetimini yapar.</span><span class="sxs-lookup"><span data-stu-id="2bc62-347">This scenario simulates a situation where the warehouse stores small items in locations and must pack them into boxes before they are shipped, and where packing station functionality isn't really suitable.</span></span> <span data-ttu-id="2bc62-348">Çalışanlar, çekme hızını artırmak için birden fazla müşteri ve farklı adres için aynı anda siparişleri çeker.</span><span class="sxs-lookup"><span data-stu-id="2bc62-348">Workers pick orders for multiple customers and different addresses at the same time to increase the picking speed.</span></span> <span data-ttu-id="2bc62-349">Çekme işlemi tamamlandıktan sonra çalışanlar, çekilen maddelerin gereken ölçütlere göre doğru kutuya tasnif edilebileceği tasnif yerleşimine gelir.</span><span class="sxs-lookup"><span data-stu-id="2bc62-349">After picking has been completed, the workers arrive at the sorting location, where the picked items can be sorted to the correct box, based on required criteria.</span></span> <span data-ttu-id="2bc62-350">Bu örnekte, sevkiyat kodu doğru kutuyu belirlemekte kullanılır, çünkü her sevkiyat farklı bir adrese sahiptir.</span><span class="sxs-lookup"><span data-stu-id="2bc62-350">In this example, the shipment ID will be used to determine the correct box, because each shipment has a different address.</span></span> <span data-ttu-id="2bc62-351">Yükteki tüm maddeler paketlendikten ve sevkiyat bazında tasnif edildikten sonra, kutular hazırlama alanına taşınacak ve bir kamyona yüklenecektir.</span><span class="sxs-lookup"><span data-stu-id="2bc62-351">After all items from the load are packed and sorted by shipment, the boxes will be moved to the staging area and eventually loaded onto a truck.</span></span>

<span data-ttu-id="2bc62-352">Senaryoya başlamadan önce, tüm standart ambar işlevlerinin ambarınız için doğru ayarlandığından emin olun.</span><span class="sxs-lookup"><span data-stu-id="2bc62-352">Before you start the scenario, make sure that all standard warehouse functionality is set up correctly for your warehouse.</span></span> <span data-ttu-id="2bc62-353">Bu amaç için standart Contoso ambar *62* kullanılır.</span><span class="sxs-lookup"><span data-stu-id="2bc62-353">Standard Contoso warehouse *62* is used for this purpose.</span></span> <span data-ttu-id="2bc62-354">Kurulumundaki açıklamasının yanı sıra standart yapılandırmalar da değiştirilmemiştir.</span><span class="sxs-lookup"><span data-stu-id="2bc62-354">Standard configurations haven't been changed, besides what is described in the setup.</span></span>

### <a name="create-demand"></a><span data-ttu-id="2bc62-355">Talep oluşturma</span><span class="sxs-lookup"><span data-stu-id="2bc62-355">Create demand</span></span>

<span data-ttu-id="2bc62-356">İşlevin gösterilebilmesi için öncelikle bir talep oluşturmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="2bc62-356">Before the functionality can be demonstrated, you must create some demand.</span></span> <span data-ttu-id="2bc62-357">Bu senaryo için, farklı teslimat adresleri benzetimi yapmak için üç farklı müşteriye ait üç satış siparişi oluşturacaksınız.</span><span class="sxs-lookup"><span data-stu-id="2bc62-357">For this scenario, you will create three sales orders for three different customers to simulate different delivery addresses.</span></span> <span data-ttu-id="2bc62-358">Bu şekilde, üç ayrı sevkiyat oluşturacaksınız.</span><span class="sxs-lookup"><span data-stu-id="2bc62-358">In this way, you will create three separate shipments.</span></span>

<span data-ttu-id="2bc62-359">Satış siparişlerini ve sevkiyatları oluşturabilmeniz için, çekme yerleşimlerinde siparişlerdeki tüm maddeler için yeterli stok bulunduğundan emin olun.</span><span class="sxs-lookup"><span data-stu-id="2bc62-359">Before you create sales orders and shipments, make sure that the pick locations have enough inventory for all the items on the orders.</span></span> <span data-ttu-id="2bc62-360">Satış siparişi çekme için kullanılan çekme yerleşimlerini onaylamak için yerleşim yönergesi ayarlarını gözden geçirin.</span><span class="sxs-lookup"><span data-stu-id="2bc62-360">Review the location directive settings to confirm the picking locations that are used for sales order picking.</span></span> <span data-ttu-id="2bc62-361">Stoku ayarlamanız gerekiyorsa, el ile hareketler oluşturabilir, stok yenilemeyi veya başka bir akışı kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="2bc62-361">If you must adjust the inventory, you can create manual movements, use replenishment, or use any other flow.</span></span> <span data-ttu-id="2bc62-362">Ardından stoğu rezerve edin.</span><span class="sxs-lookup"><span data-stu-id="2bc62-362">Then reserve the inventory.</span></span>

1. <span data-ttu-id="2bc62-363">**Satış ve pazarlama \> Satış siparişleri \> Tüm satış siparişleri**'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="2bc62-363">Go to **Sales and marketing \> Sales orders \> All sales orders**.</span></span>
1. <span data-ttu-id="2bc62-364">Sipariş 1 için satış siparişi oluşturmak üzere **Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="2bc62-364">Select **New** to create a sales order for order 1.</span></span>
1. <span data-ttu-id="2bc62-365">**Satış siparişi oluştur** iletişim kutusunda, aşağıdaki değerleri ayarlayın:</span><span class="sxs-lookup"><span data-stu-id="2bc62-365">In the **Create sales order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="2bc62-366">**Müşteri:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="2bc62-366">**Customer:** *US-001*</span></span>
    - <span data-ttu-id="2bc62-367">**Ambar:** *62*</span><span class="sxs-lookup"><span data-stu-id="2bc62-367">**Warehouse:** *62*</span></span>

1. <span data-ttu-id="2bc62-368">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="2bc62-368">Select **OK**.</span></span>
1. <span data-ttu-id="2bc62-369">**Satış siparişi satırları** hızlı sekmesine yeni bir satır eklenir.</span><span class="sxs-lookup"><span data-stu-id="2bc62-369">A new line is added to the **Sales order lines** FastTab.</span></span> <span data-ttu-id="2bc62-370">Aşağıdaki değerleri ayarlayın:</span><span class="sxs-lookup"><span data-stu-id="2bc62-370">Set the following values:</span></span>

    - <span data-ttu-id="2bc62-371">**Madde numarası:** *A0001*</span><span class="sxs-lookup"><span data-stu-id="2bc62-371">**Item number:** *A0001*</span></span>
    - <span data-ttu-id="2bc62-372">**Miktar:** *5*</span><span class="sxs-lookup"><span data-stu-id="2bc62-372">**Quantity:** *5*</span></span>

1. <span data-ttu-id="2bc62-373">**Satır ekle**'yi seçerek ikinci bir satır ekleyin ve aşağıdaki değerleri ayarlayın:</span><span class="sxs-lookup"><span data-stu-id="2bc62-373">Select **Add line** to add a second line, and set the following values:</span></span>

    - <span data-ttu-id="2bc62-374">**Madde numarası:** *A0002*</span><span class="sxs-lookup"><span data-stu-id="2bc62-374">**Item number:** *A0002*</span></span>
    - <span data-ttu-id="2bc62-375">**Miktar:** *10*</span><span class="sxs-lookup"><span data-stu-id="2bc62-375">**Quantity:** *10*</span></span>

1. <span data-ttu-id="2bc62-376">Stok rezerve etmek için, siparişteki her satış satırı için aşağıdaki adımları yineleyin:</span><span class="sxs-lookup"><span data-stu-id="2bc62-376">Repeat the following steps for each sales line on the order to reserve inventory for it:</span></span>

    1. <span data-ttu-id="2bc62-377">**Satış siparişi satırları** hızlı sekmesinde **Stok** menüsünde **Rezervasyon**'u seçin.</span><span class="sxs-lookup"><span data-stu-id="2bc62-377">On the **Sales order lines** FastTab, on the **Inventory** menu, select **Reservation**.</span></span>
    1. <span data-ttu-id="2bc62-378">**Rezervasyon** sayfasında, **Lotu rezerve et**'i seçin ve ardından sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="2bc62-378">On the **Reservation** page, select **Reserve lot**, and then close the page.</span></span>
    1. <span data-ttu-id="2bc62-379">**Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="2bc62-379">Select **Save**.</span></span>

1. <span data-ttu-id="2bc62-380">Sipariş 2 için satış siparişi oluşturmak üzere **Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="2bc62-380">Select **New** to create a sales order for order 2.</span></span>
1. <span data-ttu-id="2bc62-381">**Satış siparişi oluştur** iletişim kutusunda, aşağıdaki değerleri ayarlayın:</span><span class="sxs-lookup"><span data-stu-id="2bc62-381">In the **Create sales order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="2bc62-382">**Müşteri:** *US-004*</span><span class="sxs-lookup"><span data-stu-id="2bc62-382">**Customer:** *US-004*</span></span>
    - <span data-ttu-id="2bc62-383">**Ambar:** *62*</span><span class="sxs-lookup"><span data-stu-id="2bc62-383">**Warehouse:** *62*</span></span>

1. <span data-ttu-id="2bc62-384">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="2bc62-384">Select **OK**.</span></span>
1. <span data-ttu-id="2bc62-385">**Satış siparişi satırları** hızlı sekmesine yeni bir satır eklenir.</span><span class="sxs-lookup"><span data-stu-id="2bc62-385">A new line is added to the **Sales order lines** FastTab.</span></span> <span data-ttu-id="2bc62-386">Aşağıdaki değerleri ayarlayın:</span><span class="sxs-lookup"><span data-stu-id="2bc62-386">Set the following values:</span></span>

    - <span data-ttu-id="2bc62-387">**Madde numarası:** *A0001*</span><span class="sxs-lookup"><span data-stu-id="2bc62-387">**Item number:** *A0001*</span></span>
    - <span data-ttu-id="2bc62-388">**Miktar:** *7*</span><span class="sxs-lookup"><span data-stu-id="2bc62-388">**Quantity:** *7*</span></span>

1. <span data-ttu-id="2bc62-389">**Satır ekle**'yi seçerek ikinci bir satır ekleyin ve aşağıdaki değerleri ayarlayın:</span><span class="sxs-lookup"><span data-stu-id="2bc62-389">Select **Add line** to add a second line, and set the following values:</span></span>

    - <span data-ttu-id="2bc62-390">**Madde numarası:** *A0002*</span><span class="sxs-lookup"><span data-stu-id="2bc62-390">**Item number:** *A0002*</span></span>
    - <span data-ttu-id="2bc62-391">**Miktar:** *3*</span><span class="sxs-lookup"><span data-stu-id="2bc62-391">**Quantity:** *3*</span></span>

1. <span data-ttu-id="2bc62-392">Stok rezerve etmek için, siparişteki her satış satırı için aşağıdaki adımları yineleyin:</span><span class="sxs-lookup"><span data-stu-id="2bc62-392">Repeat the following steps for each sales line on the order to reserve inventory for it:</span></span>

    1. <span data-ttu-id="2bc62-393">**Satış siparişi satırları** hızlı sekmesinde **Stok** menüsünde **Rezervasyon**'u seçin.</span><span class="sxs-lookup"><span data-stu-id="2bc62-393">On the **Sales order lines** FastTab, on the **Inventory** menu, select **Reservation**.</span></span>
    1. <span data-ttu-id="2bc62-394">**Rezervasyon** sayfasında, **Lotu rezerve et**'i seçin ve ardından sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="2bc62-394">On the **Reservation** page, select **Reserve lot**, and then close the page.</span></span>
    1. <span data-ttu-id="2bc62-395">**Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="2bc62-395">Select **Save**.</span></span>

1. <span data-ttu-id="2bc62-396">Sipariş 3 için satış siparişi oluşturmak üzere **Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="2bc62-396">Select **New** to create a sales order for order 3.</span></span>
1. <span data-ttu-id="2bc62-397">**Satış siparişi oluştur** iletişim kutusunda, aşağıdaki değerleri ayarlayın:</span><span class="sxs-lookup"><span data-stu-id="2bc62-397">In the **Create sales order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="2bc62-398">**Müşteri:** *US-007*</span><span class="sxs-lookup"><span data-stu-id="2bc62-398">**Customer:** *US-007*</span></span>
    - <span data-ttu-id="2bc62-399">**Ambar:** *62*</span><span class="sxs-lookup"><span data-stu-id="2bc62-399">**Warehouse:** *62*</span></span>

1. <span data-ttu-id="2bc62-400">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="2bc62-400">Select **OK**.</span></span>
1. <span data-ttu-id="2bc62-401">**Satış siparişi satırları** hızlı sekmesine yeni bir satır eklenir.</span><span class="sxs-lookup"><span data-stu-id="2bc62-401">A new line is added to the **Sales order lines** FastTab.</span></span> <span data-ttu-id="2bc62-402">Aşağıdaki değerleri ayarlayın:</span><span class="sxs-lookup"><span data-stu-id="2bc62-402">Set the following values:</span></span>

    - <span data-ttu-id="2bc62-403">**Madde numarası:** *A0001*</span><span class="sxs-lookup"><span data-stu-id="2bc62-403">**Item number:** *A0001*</span></span>
    - <span data-ttu-id="2bc62-404">**Miktar:** *8*</span><span class="sxs-lookup"><span data-stu-id="2bc62-404">**Quantity:** *8*</span></span>

1. <span data-ttu-id="2bc62-405">Satış satırı için stok rezerve etmek üzere aşağıdaki adımları izleyin:</span><span class="sxs-lookup"><span data-stu-id="2bc62-405">Follow these steps to reserve inventory for the sales line:</span></span>

    1. <span data-ttu-id="2bc62-406">**Satış siparişi satırları** hızlı sekmesinde **Stok** menüsünde **Rezervasyon**'u seçin.</span><span class="sxs-lookup"><span data-stu-id="2bc62-406">On the **Sales order lines** FastTab, on the **Inventory** menu, select **Reservation**.</span></span>
    1. <span data-ttu-id="2bc62-407">**Rezervasyon** sayfasında, **Lotu rezerve et**'i seçin ve ardından sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="2bc62-407">On the **Reservation** page, select **Reserve lot**, and then close the page.</span></span>
    1. <span data-ttu-id="2bc62-408">**Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="2bc62-408">Select **Save**.</span></span>

<span data-ttu-id="2bc62-409">Her satış siparişini ambara serbest bırakmak için aşağıdaki yordamı tamamlayın.</span><span class="sxs-lookup"><span data-stu-id="2bc62-409">Complete the following procedure to release each sales order to the warehouse.</span></span> <span data-ttu-id="2bc62-410">Üç farklı sevkiyat oluşturulacaktır.</span><span class="sxs-lookup"><span data-stu-id="2bc62-410">Three different shipments will be created.</span></span> <span data-ttu-id="2bc62-411">Daha sonra, üç sevkiyatı da tek bir yeni dalgaya ekleyeceksiniz.</span><span class="sxs-lookup"><span data-stu-id="2bc62-411">You will then add all three shipments to one new wave.</span></span>

1. <span data-ttu-id="2bc62-412">**Satış ve pazarlama \> Satış siparişleri \> Tüm satış siparişleri**'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="2bc62-412">Go to **Sales and marketing \> Sales orders \> All sales orders**.</span></span>
1. <span data-ttu-id="2bc62-413">Kılavuzda, oluşturduğunuz ilk satış siparişini seçin.</span><span class="sxs-lookup"><span data-stu-id="2bc62-413">In the grid, select the first sales order that you created.</span></span>
1. <span data-ttu-id="2bc62-414">Eylem bölmesinde, **Ambar** sekmesinde **Ambara serbest bırak**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="2bc62-414">On the Action Pane, on the **Warehouse** tab, select **Release to warehouse**.</span></span>

    <span data-ttu-id="2bc62-415">Ouşturulan dalga kimliğini ve sevkiyat kimliğini gösteren bir bilgi iletisi alırsınız.</span><span class="sxs-lookup"><span data-stu-id="2bc62-415">You receive an informational message that shows the wave ID and shipment ID that were created.</span></span>

1. <span data-ttu-id="2bc62-416">Satış siparişi 2 ve 3'ü ambara serbest bırakmak için önceki adımları yenileyin.</span><span class="sxs-lookup"><span data-stu-id="2bc62-416">Repeat the previous steps to release sales orders 2 and 3 to the warehouse.</span></span> <span data-ttu-id="2bc62-417">Aldığınız bilgi iletisinin, satış siparişi 1'i serbest bıraktığınızda oluşturulan dalgaya bir sevkiayt eklendiğini belirttiğine dikkat edin.</span><span class="sxs-lookup"><span data-stu-id="2bc62-417">Notice that the informational message that you receive indicates that a shipment has been added to the wave that was created when you released sales order 1.</span></span>
1. <span data-ttu-id="2bc62-418">**Ambar yönetimi \> Giden dalgalar \> Sevkiyat dalgaları \> Tüm dalgalar**'a gidin.</span><span class="sxs-lookup"><span data-stu-id="2bc62-418">Go to **Warehouse management \> Outbound waves \> Shipment waves \> All waves**.</span></span>
1. <span data-ttu-id="2bc62-419">**Dalgalar** sayfasını açmak için satış siparişlerinin serbest bırakma işleminden oluşturulan dalga kodunu seçin.</span><span class="sxs-lookup"><span data-stu-id="2bc62-419">Select the wave ID that was created from the release of the sales orders to open the **Waves** page.</span></span> <span data-ttu-id="2bc62-420">Bu sayfa, dalga ayrıntılarını gösterir.</span><span class="sxs-lookup"><span data-stu-id="2bc62-420">This page shows the wave details.</span></span> <span data-ttu-id="2bc62-421">**Dalga satırları** hızlı sekmesi oluşturulan sevkiyatları gösterir.</span><span class="sxs-lookup"><span data-stu-id="2bc62-421">The **Wave lines** FastTab shows the shipments that were created.</span></span>

    <span data-ttu-id="2bc62-422">Malzeme çekme yerleşimlerinden alınan maddeleri sıralama yerleşimine getirmek için şimdi iş oluşturmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="2bc62-422">You must now create work to bring items from the picking locations to the sorting location.</span></span>

1. <span data-ttu-id="2bc62-423">Eylem Bölmesinde, **İşlem**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="2bc62-423">On the Action Pane, select **Process**.</span></span>

    <span data-ttu-id="2bc62-424">Dalga işleme sırasında tasnif yöntemi, stoğu tasnif konumlarına atamak için tasnif şablonunu kullanır.</span><span class="sxs-lookup"><span data-stu-id="2bc62-424">During wave processing, the sorting method will use the sorting template to assign the inventory to sort positions.</span></span> <span data-ttu-id="2bc62-425">Dalga işleme tamamlandığında, işin oluşturulduğunu ve dalganın deftere nakledildiğini gösteren bilgi iletisi alırsınız.</span><span class="sxs-lookup"><span data-stu-id="2bc62-425">When wave processing is completed, you receive an informational message that states that the wave has been posted and work has been created.</span></span>

1. <span data-ttu-id="2bc62-426">Eylem Bölmesinde, **Dalga** sekmesinde, **İlgili bilgi** grubunda, oluşturulan işi görüntülemek için **İş**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="2bc62-426">On the Action Pane, on the **Wave** tab, in the **Related information** group, select **Work** to view the work that was created.</span></span> <span data-ttu-id="2bc62-427">İş kodunu not edin.</span><span class="sxs-lookup"><span data-stu-id="2bc62-427">Make a note of the work ID.</span></span>
1. <span data-ttu-id="2bc62-428">**Ambar yönetimi \> Paketleme ve konteyner kullanımı \> Giden tasnif konumu atamaları**'na gidin.</span><span class="sxs-lookup"><span data-stu-id="2bc62-428">Go to **Warehouse management \> Packing and containerization \> Outbound sorting position assignments**.</span></span>
1. <span data-ttu-id="2bc62-429">Sol sütunda, her sevkiyat için oluşturulan giden tasnif konumunu görüntüleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="2bc62-429">In the left column, you can view the outbound sorting position that was created for each shipment.</span></span>
1. <span data-ttu-id="2bc62-430">**Tasnif konumu ölçütleri** hızlı sekmesinde, o konumun sevkiyat kodunu görüntüleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="2bc62-430">On the **Sort position criteria** FastTab, you can view the shipment ID for that position.</span></span>

<span data-ttu-id="2bc62-431">Stoğu malzeme çekme yerleşimlerinden tasnif yerleşimine getirmek için bir iş oluşturulmuştur.</span><span class="sxs-lookup"><span data-stu-id="2bc62-431">One work ID has been created to bring inventory from the picking locations to the sorting location.</span></span> <span data-ttu-id="2bc62-432">İşi tamamlamak için, dalga işleme sırasında oluşturulan iş koduna ihtiyacınız olacaktır.</span><span class="sxs-lookup"><span data-stu-id="2bc62-432">To complete the work, you will need the work ID that was created during wave processing.</span></span>

### <a name="sales-order-picking-to-the-sorting-location"></a><span data-ttu-id="2bc62-433">Tasnif yerleşimine satış siparişi çekme</span><span class="sxs-lookup"><span data-stu-id="2bc62-433">Sales order picking to the sorting location</span></span>

1. <span data-ttu-id="2bc62-434">Mobil cihazınızdan Ambar *62*'de çalışan olarak oturum açın.</span><span class="sxs-lookup"><span data-stu-id="2bc62-434">Sign in to the mobile app as a worker in warehouse *62*.</span></span>
1. <span data-ttu-id="2bc62-435">Ana menüde **Giden**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="2bc62-435">On the main menu, select **Outbound**.</span></span>
1. <span data-ttu-id="2bc62-436">**Giden** menüsünden **Satış Çekme**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="2bc62-436">On the **Outbound** menu, select **Sales Picking**.</span></span>
1. <span data-ttu-id="2bc62-437">**Kod** alanını seçin ve sonra dalga işlemeden gelen iş kodunu girin.</span><span class="sxs-lookup"><span data-stu-id="2bc62-437">Select the **ID** field, and then enter the work ID from the wave processing.</span></span>
1. <span data-ttu-id="2bc62-438">Girişinizi onaylayın.</span><span class="sxs-lookup"><span data-stu-id="2bc62-438">Confirm your entry.</span></span>

    <span data-ttu-id="2bc62-439">Sonra, bir hedef plaka (LP) girmeniz istenir.</span><span class="sxs-lookup"><span data-stu-id="2bc62-439">Next, you're prompted to enter a target license plate (LP).</span></span> <span data-ttu-id="2bc62-440">Satış siparişi 1' deki satır 1'in çekilip hedef plakaya eklenmesi gereken öğe olduğunu unutmayın.</span><span class="sxs-lookup"><span data-stu-id="2bc62-440">Notice that line 1 from sales order 1 is what must be picked and added to the target license plate.</span></span> <span data-ttu-id="2bc62-441">Madde numarası, miktar, madde açıklaması ve çekme yerleşimi gösterilir.</span><span class="sxs-lookup"><span data-stu-id="2bc62-441">The item number, quantity, item description, and pick location are shown.</span></span>

1. <span data-ttu-id="2bc62-442">**Hedef LP** alanında plaka numarasını girin.</span><span class="sxs-lookup"><span data-stu-id="2bc62-442">In the **Target LP** field, enter a license plate number.</span></span>

    <span data-ttu-id="2bc62-443">İşlenen bir dalgadan oluşturulan tüm satırları aynı hedef plakaya çekeceksiniz.</span><span class="sxs-lookup"><span data-stu-id="2bc62-443">You will pick all lines that were created from the processed wave onto the same target license plate.</span></span>

1. <span data-ttu-id="2bc62-444">Girişinizi onaylayın.</span><span class="sxs-lookup"><span data-stu-id="2bc62-444">Confirm your entry.</span></span>

    <span data-ttu-id="2bc62-445">Mobil uygulama şimdi, sizi çekme yerleşimine ve çekilmesi gereken maddeye ve miktara yönlendireen bir dizi **Çekme** sayfası sunar.</span><span class="sxs-lookup"><span data-stu-id="2bc62-445">The mobile app now presents a series of **Pick** pages that point you to the picking location, and to the item and quantity that must be picked.</span></span> <span data-ttu-id="2bc62-446">Çekilen madde plakaya eklendikten sonra çekme işini onaylarsınız.</span><span class="sxs-lookup"><span data-stu-id="2bc62-446">After the picked item is added to the license plate, you will confirm the pick work.</span></span> <span data-ttu-id="2bc62-447">Son sayfa, çekilen maddeleri tasnif konumuna yerleştirecek iş olacaktır.</span><span class="sxs-lookup"><span data-stu-id="2bc62-447">The last page will be the work to put the picked items into the sorting location.</span></span>

1. <span data-ttu-id="2bc62-448">İlk çekme işini onaylayın.</span><span class="sxs-lookup"><span data-stu-id="2bc62-448">Confirm the first pick work.</span></span>
1. <span data-ttu-id="2bc62-449">Sonraki çekme işi görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="2bc62-449">The next pick work is shown.</span></span> <span data-ttu-id="2bc62-450">Çekme işlemini onaylayın.</span><span class="sxs-lookup"><span data-stu-id="2bc62-450">Confirm the pick.</span></span>
1. <span data-ttu-id="2bc62-451">Kalan çekme işini onaylamak için devam edin.</span><span class="sxs-lookup"><span data-stu-id="2bc62-451">Continue to confirm the remaining pick work.</span></span>
1. <span data-ttu-id="2bc62-452">Son adım, yerine koyma işini tamamlamaktır.</span><span class="sxs-lookup"><span data-stu-id="2bc62-452">The last step is to complete the put work.</span></span> <span data-ttu-id="2bc62-453">Tasnif yerleşiminde yerine koymayı onaylayın.</span><span class="sxs-lookup"><span data-stu-id="2bc62-453">Confirm the put-away to the sorting location.</span></span>

    <span data-ttu-id="2bc62-454">Bir "İş tamamlandı" iletisi alırsınız.</span><span class="sxs-lookup"><span data-stu-id="2bc62-454">You receive a "Work completed" message.</span></span>

1. <span data-ttu-id="2bc62-455">Mobil uygulamada **Satış Çekme**'den çıkın.</span><span class="sxs-lookup"><span data-stu-id="2bc62-455">Exit **Sales Picking** on the mobile app.</span></span>

### <a name="sortingput-to-wall"></a><span data-ttu-id="2bc62-456">Tasnif/duvara yerleştirme</span><span class="sxs-lookup"><span data-stu-id="2bc62-456">Sorting/put-to-wall</span></span>

<span data-ttu-id="2bc62-457">Tüm stoklar tasnif yerleşimine konulduğu için, doğru tasnif konumuna tasnif edilmesi gerekir.</span><span class="sxs-lookup"><span data-stu-id="2bc62-457">Now that all inventory has been put to the sorting location, it must be sorted to the correct sort position.</span></span>

1. <span data-ttu-id="2bc62-458">Mobil uygulamada oturum açın.</span><span class="sxs-lookup"><span data-stu-id="2bc62-458">Sign in to the mobile app.</span></span>
1. <span data-ttu-id="2bc62-459">Ana menüde **Giden**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="2bc62-459">On the main menu, select **Outbound**.</span></span>
1. <span data-ttu-id="2bc62-460">**Giden** menüsünde, maddeleri tasnif etmeye başlamak için **Tasnif**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="2bc62-460">On the **Outbound** menu, select **Sort** to start to sort the items.</span></span>
1. <span data-ttu-id="2bc62-461">**LP/YER** alanına, çekilen satış siparişi işinin hedef plakasını girin.</span><span class="sxs-lookup"><span data-stu-id="2bc62-461">In the **LP/CON** field, enter the target license plate of the picked sales order work.</span></span>
1. <span data-ttu-id="2bc62-462">Girişinizi onaylayın.</span><span class="sxs-lookup"><span data-stu-id="2bc62-462">Confirm your entry.</span></span>
1. <span data-ttu-id="2bc62-463">Öncelikle tasnif edilecek madde numarasını girin.</span><span class="sxs-lookup"><span data-stu-id="2bc62-463">Enter the item number to sort first.</span></span>
1. <span data-ttu-id="2bc62-464">Sistem, gösterilmesi gereken ilk tasnif konumunu belirler.</span><span class="sxs-lookup"><span data-stu-id="2bc62-464">The system determines the first sort position that should be shown.</span></span> <span data-ttu-id="2bc62-465">Tasnif konumunu onaylayın.</span><span class="sxs-lookup"><span data-stu-id="2bc62-465">Confirm the sort position.</span></span>
1. <span data-ttu-id="2bc62-466">Tasnif konumuna bir plaka atamanız istenir.</span><span class="sxs-lookup"><span data-stu-id="2bc62-466">You're prompted to assign a license plate to the sort position.</span></span> <span data-ttu-id="2bc62-467">**LP** alanını seçin, plaka numarası girin ve sonra girişinizi onaylayın.</span><span class="sxs-lookup"><span data-stu-id="2bc62-467">Select the **LP** field, enter a license plate number, and then confirm your entry.</span></span>

    <span data-ttu-id="2bc62-468">Tasnif konumu sevkiyat koduyla ilişkili olduğundan, çekilen maddeleri giden sevk irsaliyesine ve satış siparişine özel olan bir plakaya tasnif edersiniz.</span><span class="sxs-lookup"><span data-stu-id="2bc62-468">Because the sort position is related to the shipment ID, you will sort the picked items into a license plate that is specific to the outbound shipment and sales order.</span></span>

    <span data-ttu-id="2bc62-469">Sonraki sayfada madde kodu, miktar, tasnif konumu kodu ve "kaynak" (malzeme çekme) ve "hedef" (tasnif) plaka kodları gösterilir.</span><span class="sxs-lookup"><span data-stu-id="2bc62-469">The next page shows the item ID, quantity, sort position ID, and the "from" (picking) and "to" (sorting) license plate IDs.</span></span> <span data-ttu-id="2bc62-470">Bu sayfadaki bilgiler, belirtilen madde ve miktarları malzeme çekme plakasından tasnif plakasına tasnif etmenizi belirtir.</span><span class="sxs-lookup"><span data-stu-id="2bc62-470">The information on this page instructs you to sort the specified item and quantities from the picking license plate into the sorting license plate.</span></span>

1. <span data-ttu-id="2bc62-471">Tasnif konumunu onaylayın.</span><span class="sxs-lookup"><span data-stu-id="2bc62-471">Confirm the sort position.</span></span>
1. <span data-ttu-id="2bc62-472">İlk tasnif konumundaki maddeleri tasnif edin.</span><span class="sxs-lookup"><span data-stu-id="2bc62-472">Sort the items in the first sort position.</span></span> <span data-ttu-id="2bc62-473">Bitirdiğinizde, sistem sizi sonraki tasnif konumuna yönlendirir.</span><span class="sxs-lookup"><span data-stu-id="2bc62-473">When you've finished, the system directs you to the next sort position.</span></span>
1. <span data-ttu-id="2bc62-474">Bu işlemi, iş emrindeki tüm çekilen satırlar için yineleyin.</span><span class="sxs-lookup"><span data-stu-id="2bc62-474">Repeat this process for all picked lines on the work order.</span></span> <span data-ttu-id="2bc62-475">Aynı madde numarasına sahip birden fazla çekme satırı olduğunda da bu işlemi kullanmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="2bc62-475">You should also use this process when there are multiple pick lines that have the same item number.</span></span>

    <span data-ttu-id="2bc62-476">Bu işlemi tüm maddeler için tekrarlamak amacıyla, sistem ölçütü bir sonraki taranan maddeden (iş satırı) değerlendirir ve hangi tasnif konumuna konulması gerektiğini belirler.</span><span class="sxs-lookup"><span data-stu-id="2bc62-476">As you repeat this process for all items, the system evaluates the criteria from the next scanned item (work line) and determines which sorting position it should be put to.</span></span> <span data-ttu-id="2bc62-477">Maddeyi doğru tasnif konumuna koymak için otomatik olarak yönlendirilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="2bc62-477">You're automatically directed to put the item to the correct sort position.</span></span> <span data-ttu-id="2bc62-478">Onay kurulumuna bağlı olarak, konum numarasını veya plaka kodunu girerek bu eylemi onaylamak üzere de yönlendirilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="2bc62-478">Depending on the confirmation setup, you're also directed to confirm this action by entering the position number or license plate ID.</span></span>

    > [!NOTE]
    > <span data-ttu-id="2bc62-479">Otomatik tasnif açıksa el ile geçersiz kılma kullanılamaz.</span><span class="sxs-lookup"><span data-stu-id="2bc62-479">If automatic sorting is turned on, manual override isn't available.</span></span>

1. <span data-ttu-id="2bc62-480">Bitirdiğinizde, Microsoft Dynamics 365 Supply Chain Management'ta konumların durumunu gözden geçirmek için **Giden tasnif konumu atamaları** sayfasını açın.</span><span class="sxs-lookup"><span data-stu-id="2bc62-480">When you've finished, in Microsoft Dynamics 365 Supply Chain Management, open the **Outbound sorting position assignments** page to review the status of the positions.</span></span>

    - <span data-ttu-id="2bc62-481">Konumlar otomatik olarak kapatılırsa, kapalı konumları göstermek için **Kapatılanı göster**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="2bc62-481">If positions are closed automatically, select **Show closed** to show the closed positions.</span></span>
    - <span data-ttu-id="2bc62-482">Tasnif konumu hareketlerinin gösterildiğine dikkat edin.</span><span class="sxs-lookup"><span data-stu-id="2bc62-482">Notice that sort position transactions are shown.</span></span> <span data-ttu-id="2bc62-483">Konumla işlenen madde ve miktar gösterilir.</span><span class="sxs-lookup"><span data-stu-id="2bc62-483">The item and quantity that were processed through the position are shown.</span></span>

    <span data-ttu-id="2bc62-484">Giden tasnif şablonunu ayarlarken, **Tasnif konumunu otomatik kapat** seçeneğini *Evet* olarak ayarlarsınız.</span><span class="sxs-lookup"><span data-stu-id="2bc62-484">When you set up the outbound sorting template, you set the **Auto close sort position** option to *Yes*.</span></span> <span data-ttu-id="2bc62-485">Bu nedenle, son beklenen stok koyulduktan sonra konum otomatik olarak kapatılır.</span><span class="sxs-lookup"><span data-stu-id="2bc62-485">Therefore, the position is automatically closed after the last expected inventory is put to it.</span></span> <span data-ttu-id="2bc62-486">Tasnif pozisyonları **Kapalı** durumundadır ve iş tasnif edilen stoğu *Bölme kapısı* yerleşimine taşımak üzere oluşturulmuştur.</span><span class="sxs-lookup"><span data-stu-id="2bc62-486">The sort positions are in **Closed** status, and work has been created to move the sorted inventory to *Baydoor* location.</span></span>

1. <span data-ttu-id="2bc62-487">Stoğu sevkiyat yerleşimine taşımak için tasnif edilmiş stok malzeme çekme işini tamamlayın.</span><span class="sxs-lookup"><span data-stu-id="2bc62-487">Complete the sorted inventory picking work to move the inventory to the shipping location.</span></span> <span data-ttu-id="2bc62-488">Stok hazır olduğunda, sevkiyat için onaylayın.</span><span class="sxs-lookup"><span data-stu-id="2bc62-488">When the inventory is ready, ship-confirm it.</span></span>

> [!NOTE]
> <span data-ttu-id="2bc62-489">Tasnif edilen stok çekme işinin doğru olarak işlenmesi için, taşıma ve yükleme işlemleri için **İş emri türü** alanının *Tasnif edilmiş stok çekme* olarak ayarlandığı iş sınıfı koduna sahip bir mobil cihaz menüsü kullanılmalıdır.</span><span class="sxs-lookup"><span data-stu-id="2bc62-489">For sorted inventory picking work to be processed correctly, a mobile device menu item that has a work class ID where the **Work order type** field is set to *Sorted inventory picking* should be used for the movement and loading process.</span></span>

### <a name="manually-close-a-position-optional"></a><span data-ttu-id="2bc62-490">Konumu el ile kapatma (isteğe bağlı)</span><span class="sxs-lookup"><span data-stu-id="2bc62-490">Manually close a position (optional)</span></span>

<span data-ttu-id="2bc62-491">Tasnif konumlarının el ile kapatılması gerekiyorsa, giden tasnif şablonu için **Tasnif konumunu otomatik kapat** seçeneği *Hayır* olarak ayarlanmalıdır ve stoğun bölme kapısı alanına taşınabilmesi için kapatma işlemi yapılmalıdır.</span><span class="sxs-lookup"><span data-stu-id="2bc62-491">If sort positions should be closed manually, the **Auto close sort position** option for the outbound sorting template must be set to *No*, and closing must be done before inventory can be moved to the bay door area.</span></span> <span data-ttu-id="2bc62-492">Konumlar çeşitli şekillerde kapatılabilir:</span><span class="sxs-lookup"><span data-stu-id="2bc62-492">Positions can be closed in various ways:</span></span>

- <span data-ttu-id="2bc62-493">Ambar Yönetimi mobil uygulaması aracılığıyla:</span><span class="sxs-lookup"><span data-stu-id="2bc62-493">Via the Warehouse Management mobile app:</span></span>

    - <span data-ttu-id="2bc62-494">Kullanıcı, zaten o konumdaki maddelerden birini tarayabilir ve konumu kapatmak için **Kapat**'ı seçebilir.</span><span class="sxs-lookup"><span data-stu-id="2bc62-494">The user can scan one of the items that are already on the position and then select **Close** to close the position.</span></span>
    - <span data-ttu-id="2bc62-495">Kullanıcı zaten tasnif edilmiş bir konteyneri tararsa, bir hata iletisi görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="2bc62-495">If the user scans a container that has already been sorted container, an error message is shown.</span></span> <span data-ttu-id="2bc62-496">Ancak, kullanıcı konumu kapatmaya devam edebilir.</span><span class="sxs-lookup"><span data-stu-id="2bc62-496">However, the user can still continue to close the position.</span></span>

- <span data-ttu-id="2bc62-497">Microsoft Dynamics 365 Supply Chain Management **Giden tasnif konum atamaları** sayfasından:</span><span class="sxs-lookup"><span data-stu-id="2bc62-497">From the Microsoft Dynamics 365 Supply Chain Management **Outbound sorting position assignments** page:</span></span>

    - <span data-ttu-id="2bc62-498">Kullanıcı giden tasnif konumu kaydını seçebilir ve sonra Eylem Bölmesinde **Konumu kapat**'ı seçebilir.</span><span class="sxs-lookup"><span data-stu-id="2bc62-498">The user can select the outbound sorting position record and then select **Close position** on the Action Pane.</span></span>

## <a name="tips"></a><span data-ttu-id="2bc62-499">İpuçları</span><span class="sxs-lookup"><span data-stu-id="2bc62-499">Tips</span></span>

- <span data-ttu-id="2bc62-500">Maddeler birine atandıktan sonra konumlar arasında taşınamaz.</span><span class="sxs-lookup"><span data-stu-id="2bc62-500">Items can't be moved between positions after they have been assigned to one.</span></span> <span data-ttu-id="2bc62-501">Sistem her bir maddeden kaç tanesinin belirtilen konuma gitmesi gerektiğini değerlendirir.</span><span class="sxs-lookup"><span data-stu-id="2bc62-501">The system evaluates how many of each item should go to a specific position.</span></span>
- <span data-ttu-id="2bc62-502">Tasnifler şablonu, konumlar kapatıldığında konteynerleri otomatik olarak oluşturmak üzere yapılandırılabilir.</span><span class="sxs-lookup"><span data-stu-id="2bc62-502">Sorts template can be configured to automatically create containers when positions are closed.</span></span> <span data-ttu-id="2bc62-503">Bu yaklaşım, belirtilen paketleme profilini temel alan standart konteyner kodu yapısı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="2bc62-503">This approach will create standard container ID structure that is based on the specified packing profile.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="2bc62-504">Hareket işi tasnif yerleşiminden oluşturulduktan sonra, işi iptal etmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="2bc62-504">After movement work has been created from the sorting location, you must not cancel the work.</span></span> <span data-ttu-id="2bc62-505">Aksi durumda, konum ve içerdiği konteynerler sistemden silinir ve daha fazla işlem için kullanılamaz.</span><span class="sxs-lookup"><span data-stu-id="2bc62-505">Otherwise, the position and the containers in it will be deleted from the system and unavailable for further processing.</span></span> <span data-ttu-id="2bc62-506">Stok da kaldırılır.</span><span class="sxs-lookup"><span data-stu-id="2bc62-506">The inventory will also be removed.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]