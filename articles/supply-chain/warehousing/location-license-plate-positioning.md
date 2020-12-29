---
title: Yerleşim plakası konumlandırmasıı
description: Lisans levhası yerleşim konumlama, Çift-derin palet yerleşiminden oluşan yerleşim gibi, bir lisans kalıbının çok palet bir yerleşimde nerede konumlanıldığını görmenizi sağlar.
author: Mirzaab
manager: tfehr
ms.date: 07/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSLicensePlate, WHSLocationProfile, WHSLocDirTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-01
ms.dyn365.ops.version: Release 10.0.7
ms.openlocfilehash: 7b0ebfb965e5a8f1bfe1857a9642d998dac2faf3
ms.sourcegitcommit: 827d77c638555396b32d36af5d22d1b61dafb0e8
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4439620"
---
# <a name="location-license-plate-positioning"></a><span data-ttu-id="2b92e-103">Yerleşim plakası konumlandırmasıı</span><span class="sxs-lookup"><span data-stu-id="2b92e-103">Location license plate positioning</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="2b92e-104">Lisans levhası yerleşim konumlama, Çift-derin palet yerleşiminden oluşan yerleşim gibi, bir lisans kalıbının çok palet bir yerleşimde nerede konumlanıldığını görmenizi sağlar.</span><span class="sxs-lookup"><span data-stu-id="2b92e-104">License plate location positioning lets you see where a license plate is located in a multi-pallet location, such as a location that uses double-deep pallet racking.</span></span>

<span data-ttu-id="2b92e-105">Özellik bir depolama konumuna yerleştirilecek her lisans kalıbına bir sıra numarası ekler.</span><span class="sxs-lookup"><span data-stu-id="2b92e-105">The feature adds a sequence number to each license plate that is put into a storage location.</span></span> <span data-ttu-id="2b92e-106">Bu sıra numarası depolama konumundaki lisans levhalarını sipariş etmek için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="2b92e-106">This sequence number is used to order the license plates in the storage location.</span></span> <span data-ttu-id="2b92e-107">Bu nedenle, özellik, müşterilerin yer çekimi takılabilir bir sistemi kullandığı ve malzeme çekme amaçları doğrultusunda, hangi lisans kalıbının öne geldiği ile ilgili bilinmesi gereken senaryoları akıllıca destekler.</span><span class="sxs-lookup"><span data-stu-id="2b92e-107">Therefore, the feature intelligently supports scenarios where customers are using a gravity racking system and must know, for picking purposes, which license plate is front-facing.</span></span>

<span data-ttu-id="2b92e-108">Bu konu özelliğin nasıl ayarlanacağını ve kullanılacağını gösteren bir senaryo sunar.</span><span class="sxs-lookup"><span data-stu-id="2b92e-108">This topic presents a scenario that shows how to set up and use the feature.</span></span>

## <a name="turn-on-the-location-license-plate-positioning-feature"></a><span data-ttu-id="2b92e-109">Konum lisans plağı konumlandırma özelliğini aç</span><span class="sxs-lookup"><span data-stu-id="2b92e-109">Turn on the Location license plate positioning feature</span></span>

<span data-ttu-id="2b92e-110">Lisans plakası konumlanırmayı kullanabilmeniz için sisteminizde etkinleştirilmesi gerekir.</span><span class="sxs-lookup"><span data-stu-id="2b92e-110">Before you can use license plate location positioning, the feature must be turned on in your system.</span></span> <span data-ttu-id="2b92e-111">Yöneticiler özellik durumunu denetlemek ve gerekirse etkinleştirmek için [özellik yönetimi](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) çalışma alanını kullanabilir.</span><span class="sxs-lookup"><span data-stu-id="2b92e-111">Admins can use the [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) workspace to check the status of the feature and turn it on if it's required.</span></span> <span data-ttu-id="2b92e-112">Burada, özellik aşağıdaki şekilde listelenmiştir:</span><span class="sxs-lookup"><span data-stu-id="2b92e-112">There, the feature is listed in the following way:</span></span>

- <span data-ttu-id="2b92e-113">**Modül:** *Ambar yönetimi*</span><span class="sxs-lookup"><span data-stu-id="2b92e-113">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="2b92e-114">**Özellik adı**: *Konum lisans plağı konumlandırma*</span><span class="sxs-lookup"><span data-stu-id="2b92e-114">**Feature name:** *Location license plate positioning*</span></span>

## <a name="example-scenario"></a><span data-ttu-id="2b92e-115">Örnek senaryo</span><span class="sxs-lookup"><span data-stu-id="2b92e-115">Example scenario</span></span>

### <a name="make-sample-data-available"></a><span data-ttu-id="2b92e-116">Örnek verilerini kullanılabilir hale getirme</span><span class="sxs-lookup"><span data-stu-id="2b92e-116">Make sample data available</span></span>

<span data-ttu-id="2b92e-117">Burada önerilen değerleri kullanarak bu senaryoyla çalışmak için, örnek verilerinin yüklenmiş olduğu bir sistemde çalışmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="2b92e-117">To work through this scenario by using the values that are suggested here, you must work on a system where sample data is installed.</span></span> <span data-ttu-id="2b92e-118">Ek olarak, başlamadan önce **USMF** tüzel kişiliğini seçmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="2b92e-118">Additionally, you must select the **USMF** legal entity before you start.</span></span>

### <a name="set-up-the-feature-for-this-scenario"></a><span data-ttu-id="2b92e-119">Bu senaryo için özellik ayarla</span><span class="sxs-lookup"><span data-stu-id="2b92e-119">Set up the feature for this scenario</span></span>

<span data-ttu-id="2b92e-120">Bu konuda sunulan senaryoya ait *konum lisans levhası konumlandırma* özelliğini ayarlamak için aşağıdaki yordamları tamamlayın.</span><span class="sxs-lookup"><span data-stu-id="2b92e-120">Complete the following procedures to set up the *Location license plate positioning* feature for the scenario that is presented in this topic.</span></span>

#### <a name="location-profiles"></a><span data-ttu-id="2b92e-121">Konum profilleri</span><span class="sxs-lookup"><span data-stu-id="2b92e-121">Location profiles</span></span>

<span data-ttu-id="2b92e-122">Özelliğin, kullanılacağı her yerleşim için konum profilinde açık olması gerekir.</span><span class="sxs-lookup"><span data-stu-id="2b92e-122">The feature must be turned on in the location profile for every location where it will be used.</span></span>

1. <span data-ttu-id="2b92e-123">**Ambar yönetimi \> Kurulum \> Ambar \> Konum profilleri**'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="2b92e-123">Go to **Warehouse management \> Setup \> Warehouse \> Location profiles**.</span></span>
1. <span data-ttu-id="2b92e-124">Sol bölmedeki yerleşim profilleri listesinde, **toplu-06** seçeneğini belirleyin.</span><span class="sxs-lookup"><span data-stu-id="2b92e-124">In the list of location profiles in the left pane, select **BULK-06**.</span></span>
1. <span data-ttu-id="2b92e-125">**Genel** hızlı sekmesinde, özellik tarafından iki yeni seçenek eklenmiştir.</span><span class="sxs-lookup"><span data-stu-id="2b92e-125">On the **General** FastTab, two new options have been added by the feature.</span></span> <span data-ttu-id="2b92e-126">Aşağıdaki değerleri ayarlayın:</span><span class="sxs-lookup"><span data-stu-id="2b92e-126">Set the following values:</span></span>

    - <span data-ttu-id="2b92e-127">**Lisans plağı konumunu etkinleştir:** *Evet*</span><span class="sxs-lookup"><span data-stu-id="2b92e-127">**Enable license plate position:** *Yes*</span></span>

        <span data-ttu-id="2b92e-128">Bu seçenek *Evet* olarak ayarlandığında , bu konumdaki lisans levhaları için lisans levhası konumu korunur.</span><span class="sxs-lookup"><span data-stu-id="2b92e-128">When this option is set to *Yes*, the license plate position will be maintained for license plates in the location.</span></span>

    - <span data-ttu-id="2b92e-129">**Mobil aygıtı görüntüle LP konumu:** *Evet*</span><span class="sxs-lookup"><span data-stu-id="2b92e-129">**Display mobile device LP position:** *Yes*</span></span>

        <span data-ttu-id="2b92e-130">Bu seçenek *Evet* olarak ayarlandığında lisans levhası konumu ayarlama ve sayma sırasında mobil cihaz kullanıcıları tarafından gösterilir.</span><span class="sxs-lookup"><span data-stu-id="2b92e-130">When this option is set to *Yes*, the license plate position will be shown to mobile device users during adjustment and counting.</span></span> <span data-ttu-id="2b92e-131">Bu seçeneğin ayarını yalnızca özellik açık olduğunda değiştirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="2b92e-131">You can change the setting of this option only when the feature is turned on.</span></span>

1. <span data-ttu-id="2b92e-132">**Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="2b92e-132">Select **Save**.</span></span>

#### <a name="location-directives"></a><span data-ttu-id="2b92e-133">Konum yönergeleri</span><span class="sxs-lookup"><span data-stu-id="2b92e-133">Location directives</span></span>

1. <span data-ttu-id="2b92e-134">**Ambar Yönetimi \> Kurulum \> Konum yönergeleri** seçeneğine gidin.</span><span class="sxs-lookup"><span data-stu-id="2b92e-134">Go to **Warehouse management \> Setup \> Location directives**.</span></span>
1. <span data-ttu-id="2b92e-135">Sol bölmede, **iş emri türü** alanının *satış siparişleri* olarak ayarlandığından emin olun.</span><span class="sxs-lookup"><span data-stu-id="2b92e-135">In the left pane, make sure that the **Work order type** field is set to *Sales orders*.</span></span>
1. <span data-ttu-id="2b92e-136">Konum yönergeleri listesinde, **61 SO Alma siparişi** seçin.</span><span class="sxs-lookup"><span data-stu-id="2b92e-136">In the list of location directives, select **61 SO Pick order**.</span></span>
1. <span data-ttu-id="2b92e-137">Eylem Bölmesi'nde, **Düzenle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="2b92e-137">On the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="2b92e-138">**Satırlar** hızlı sekmesinde, **sıra numarası** değeri *2* olan satırı seçin.</span><span class="sxs-lookup"><span data-stu-id="2b92e-138">On the **Lines** FastTab, select the line that has a **Sequence number** value of *2*.</span></span>
1. <span data-ttu-id="2b92e-139">**Konum yönergesi eylemleri** hızlı sekmesinde, *daha az palet için çekme* **adı** değeri olan satırı seçin  (tek satır olmalıdır) ve **sıra numarası** değerini *2* olarak değiştirin.</span><span class="sxs-lookup"><span data-stu-id="2b92e-139">On the **Location Directive Actions** FastTab, select the line that has a **Name** value of *Pick for less than pallet* (it should be the only line), and change its **Sequence number** value to *2*.</span></span>
1. <span data-ttu-id="2b92e-140">Yeni bir konum yönergesi eylemine satır eklemek için kılavuzun üzerinde **yeni** 'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="2b92e-140">Select **New** above the grid to add a line for a new location directive action.</span></span>
1. <span data-ttu-id="2b92e-141">Yeni satırda aşağıdaki değerleri ayarlayın:</span><span class="sxs-lookup"><span data-stu-id="2b92e-141">On the new line, set the following values:</span></span>

    - <span data-ttu-id="2b92e-142">**Sıra numarası:** *1*</span><span class="sxs-lookup"><span data-stu-id="2b92e-142">**Sequence number:** *1*</span></span>
    - <span data-ttu-id="2b92e-143">**Ad:** *seçim pozisyonu 1*</span><span class="sxs-lookup"><span data-stu-id="2b92e-143">**Name:** *Pick position 1*</span></span>

1. <span data-ttu-id="2b92e-144">Yeni satır seçiliyken, kılavuzun üzerinde **Düzenle sorgu** seçin.</span><span class="sxs-lookup"><span data-stu-id="2b92e-144">While the new line is still selected, select **Edit query** above the grid.</span></span>
1. <span data-ttu-id="2b92e-145">Sorgu düzenleyicisinde, **birleşimler** sekmesini seçin.</span><span class="sxs-lookup"><span data-stu-id="2b92e-145">In the query editor, select the **Joins** tab.</span></span>
1. <span data-ttu-id="2b92e-146">**Stok boyutları** tablosuna birleşimi göstermek için **yerleşimler** tablosunu genişletin.</span><span class="sxs-lookup"><span data-stu-id="2b92e-146">Expand the **Locations** table join to show the join to the **Inventory dimensions** table.</span></span>
1. <span data-ttu-id="2b92e-147">**Mevcut envanter** tablosuna birleşimi göstermek için **envanter boyutları** tablosunu genişletin.</span><span class="sxs-lookup"><span data-stu-id="2b92e-147">Expand the **Inventory dimensions** table join to show the join to the **On-hand inventory** table.</span></span>
1. <span data-ttu-id="2b92e-148">**Stok boyutlarını** seçin ve sonra **tablo katılımı Ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="2b92e-148">Select **Inventory dimensions**, and then select **Add table join**.</span></span>
1. <span data-ttu-id="2b92e-149">Görünen tablolar listesinde, **ilişki** sütununda, **Lisans levhasını (lisans levhası)** seçin.</span><span class="sxs-lookup"><span data-stu-id="2b92e-149">In the list of tables that appears, in the **Relation** column, select **License plate (License plate)**.</span></span> <span data-ttu-id="2b92e-150">Daha sonra **Stok boyutları** tablo katılmasınına **lisans levhası** eklemek için **Seç**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="2b92e-150">Then select **Select** to add **License plate** to the **Inventory dimensions** table join.</span></span>
1. <span data-ttu-id="2b92e-151">**Lisans levhası** seçiliyken, **Tablo bağlaması ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="2b92e-151">While **License plate** is still selected, select **Add table join**.</span></span>
1. <span data-ttu-id="2b92e-152">Görünen tablolar listesinde, **ilişki** sütununda, **Konum lisans levhası konumlandırma (lisans levhası)** seçin.</span><span class="sxs-lookup"><span data-stu-id="2b92e-152">In the list of tables that appears, in the **Relation** column, select **Location license plate positioning (License plate)**.</span></span> <span data-ttu-id="2b92e-153">Daha sonra **Stok boyutları** tablo katılmasınına **Konum lisans levhası konumlandırma** eklemek için **Seç**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="2b92e-153">Then select **Select** to add **Location license plate positioning** to the **Inventory dimensions** table join.</span></span>

    <span data-ttu-id="2b92e-154">![Tablo birleştirmeleri](media/LpTableJoin.png "Tablo birleştirmeleri")</span><span class="sxs-lookup"><span data-stu-id="2b92e-154">![Table joins](media/LpTableJoin.png "Table joins")</span></span>

1. <span data-ttu-id="2b92e-155">Güncelleştirilen birleştirilmiş tabloları onaylamak ve sorgu düzenleyicisini kapatmak için **Tamam** 'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="2b92e-155">Select **OK** to confirm the updated joined tables and close the query editor.</span></span>
1. <span data-ttu-id="2b92e-156">**Yerleşim yönergesi eylemleri** hızlı sekmesinde sorgu düzenleyiciyi açmak için **Sorguyu düzenle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="2b92e-156">On the **Location Directive Actions** FastTab, select **Edit query** again to reopen to the query editor.</span></span>
1. <span data-ttu-id="2b92e-157">**Aralık** sekmesinde, kılavuza satır eklemek için **Ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="2b92e-157">On the **Range** tab, select **Add** to add a line to the grid.</span></span>
1. <span data-ttu-id="2b92e-158">Yeni satırda aşağıdaki değerleri ayarlayın:</span><span class="sxs-lookup"><span data-stu-id="2b92e-158">On the new line, set the following values:</span></span>

    - <span data-ttu-id="2b92e-159">**Tablo**: *Konum lisans plağı konumlandırma*</span><span class="sxs-lookup"><span data-stu-id="2b92e-159">**Table:** *Location license plate positioning*</span></span>
    - <span data-ttu-id="2b92e-160">**Türetilmiş tablo**: *Konum lisans plağı konumlandırma*</span><span class="sxs-lookup"><span data-stu-id="2b92e-160">**Derived table:** *Location license plate positioning*</span></span>
    - <span data-ttu-id="2b92e-161">**Alan:** *LP Konumu*</span><span class="sxs-lookup"><span data-stu-id="2b92e-161">**Field:** *LP Position*</span></span>
    - <span data-ttu-id="2b92e-162">**Ölçüt:** *1*</span><span class="sxs-lookup"><span data-stu-id="2b92e-162">**Criteria:** *1*</span></span>

    <span data-ttu-id="2b92e-163">![Yeni Aralık](media/LpPositionCriteria.png "Yeni Aralık")</span><span class="sxs-lookup"><span data-stu-id="2b92e-163">![New range](media/LpPositionCriteria.png "New range")</span></span>

1. <span data-ttu-id="2b92e-164">Değişikliklerinizi onaylayıp sorgu düzenleyicisi kapatmak için **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="2b92e-164">Select **OK** to confirm your changes and close the query editor.</span></span>

### <a name="set-up-sample-data-for-this-scenario"></a><span data-ttu-id="2b92e-165">Bu senaryo için örnek verilerini ayarla</span><span class="sxs-lookup"><span data-stu-id="2b92e-165">Set up sample data for this scenario</span></span>

<span data-ttu-id="2b92e-166">Bu senaryo için, kullanıcının, iş yapması amacıyla ambar *61* için ayarlanmış bir çalışanı kullanarak ambar mobil uygulamada oturum açması gerekir.</span><span class="sxs-lookup"><span data-stu-id="2b92e-166">For this scenario, the user must sign in to the warehousing mobile app by using a worker who is set up for warehouse *61* to perform work.</span></span> <span data-ttu-id="2b92e-167">Ayrıca, kullanıcının hareketleri tamamlaması de gerekir.</span><span class="sxs-lookup"><span data-stu-id="2b92e-167">The user must also complete transactions.</span></span>

<span data-ttu-id="2b92e-168">*Konum lisans levhası konumlandırma* özelliği bir konumdaki lisans levhası konumları için yeni bir tanımlayıcı eklemesine göre, önce senaryoyu destekleyecek bazı verileri oluşturmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="2b92e-168">Because the *Location license plate positioning* feature adds a new identifier for license plate positions in a location, you must first create some data to support the scenario.</span></span>

#### <a name="spot-count-the-first-location"></a><span data-ttu-id="2b92e-169">Nokta-ilk konumu say</span><span class="sxs-lookup"><span data-stu-id="2b92e-169">Spot-count the first location</span></span>

1. <span data-ttu-id="2b92e-170">Ambar mobil uygulamasında ambar *61*'deki bir kullanıcı olarak oturum açın.</span><span class="sxs-lookup"><span data-stu-id="2b92e-170">Open the warehousing mobile app, and sign in to warehouse *61*.</span></span>
1. <span data-ttu-id="2b92e-171">**Stok \> nokta sayma** gidin.</span><span class="sxs-lookup"><span data-stu-id="2b92e-171">Go to **Inventory \> Spot Counting**.</span></span>
1. <span data-ttu-id="2b92e-172">**Nokta sayım** sayfasında, **Konum** alanını *01A01R1S1B* olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="2b92e-172">On the **Spot Counting** page, set the **Location** field to *01A01R1S1B*.</span></span>
1. <span data-ttu-id="2b92e-173">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="2b92e-173">Select **OK**.</span></span>

    <span data-ttu-id="2b92e-174">Sayfa, girdiğiniz konumu gösterir.</span><span class="sxs-lookup"><span data-stu-id="2b92e-174">The page shows the location that you entered.</span></span> <span data-ttu-id="2b92e-175">Ayrıca şu iletiyi gösterir: "yerleşim tamamlandı, yeni LP veya öğe Ekle?"</span><span class="sxs-lookup"><span data-stu-id="2b92e-175">It also shows the following message: "Location complete, add new LP or Item?"</span></span>

1. <span data-ttu-id="2b92e-176">Yerleşime sayı eklemek için **Yenile** seçin.</span><span class="sxs-lookup"><span data-stu-id="2b92e-176">Select **Refresh** to add a count in the location.</span></span>
1. <span data-ttu-id="2b92e-177">**Döngü sayımında: Yeni LP veya madde Ekle** sayfası, **madde** alanını seçin ve *A0001* değerini girin.</span><span class="sxs-lookup"><span data-stu-id="2b92e-177">On the **Cycle Count: Add New LP or Item** page, select the **Item** field, and then enter the value *A0001*.</span></span>
1. <span data-ttu-id="2b92e-178">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="2b92e-178">Select **OK**.</span></span>
1. <span data-ttu-id="2b92e-179">**Döngü sayımı: Yeni LP veya madde** sayfası ekle, **LP** alanını seçin ve *LP1001* değerini (veya istediğiniz diğer tüm lisans plakası numarasını) girin.</span><span class="sxs-lookup"><span data-stu-id="2b92e-179">On the **Cycle Count: Add New LP or Item** page, select the **LP** field, and then enter the value *LP1001* (or any other license plate number of your choice).</span></span>

    <span data-ttu-id="2b92e-180">**Döngü sayısı: Yeni LP veya madde ekle** sayfası **Lisans plağı 1. konumu** gösterir.</span><span class="sxs-lookup"><span data-stu-id="2b92e-180">The **Cycle Count: Add New LP or Item** page shows **License Plate Position 1**.</span></span>

1. <span data-ttu-id="2b92e-181">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="2b92e-181">Select **OK**.</span></span>

    <span data-ttu-id="2b92e-182">Şimdi, lisans kalıbına sayılan madde miktarını belirtmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="2b92e-182">You must now specify the quantity of the item that is counted on the license plate.</span></span>

1. <span data-ttu-id="2b92e-183">**Miktar** alanı *10* olarak ayarlanmıştır.</span><span class="sxs-lookup"><span data-stu-id="2b92e-183">Set the **Qty** field to *10*.</span></span>
1. <span data-ttu-id="2b92e-184">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="2b92e-184">Select **OK**.</span></span>

    <span data-ttu-id="2b92e-185">Sayfa, girdiğiniz konumu gösterir.</span><span class="sxs-lookup"><span data-stu-id="2b92e-185">The page shows the location that you entered.</span></span> <span data-ttu-id="2b92e-186">Ayrıca şu iletiyi gösterir: "yerleşim tamamlandı, yeni LP veya öğe Ekle?"</span><span class="sxs-lookup"><span data-stu-id="2b92e-186">It also shows the following message: "Location complete, add new LP or Item?"</span></span>

1. <span data-ttu-id="2b92e-187">Yerleşime başka sayı eklemek için **Yenile** seçin.</span><span class="sxs-lookup"><span data-stu-id="2b92e-187">Select **Refresh** to add another count in the location.</span></span>
1. <span data-ttu-id="2b92e-188">**Döngü sayımında: Yeni LP veya madde Ekle** sayfası, **madde** alanını seçin ve *A0002* değerini girin.</span><span class="sxs-lookup"><span data-stu-id="2b92e-188">On the **Cycle Count: Add New LP or Item** page, select the **Item** field, and then enter the value *A0002*.</span></span>
1. <span data-ttu-id="2b92e-189">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="2b92e-189">Select **OK**.</span></span>
1. <span data-ttu-id="2b92e-190">**Döngü sayımı: yenı LP veya madde ekle** sayfası, **LP** alanını seçin ve sonra *LP1002* değerini (veya daha önce belirttiğiniz lisans plakasından farklı olarak istediğiniz diğer herhangi bir lisans plakası numarası) girin.</span><span class="sxs-lookup"><span data-stu-id="2b92e-190">On the **Cycle Count: Add New LP or Item** page, select the **LP** field, and then enter the value *LP1002* (or any other license plate number of your choice, provided that it differs from the license plate number that you specified earlier).</span></span>
1. <span data-ttu-id="2b92e-191">**LP Konumu** alanını *2* olarak ayarlayarak, lisans levhası konumunu değiştirin.</span><span class="sxs-lookup"><span data-stu-id="2b92e-191">Change the license plate position by setting the **LP Position** field to *2*.</span></span>
1. <span data-ttu-id="2b92e-192">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="2b92e-192">Select **OK**.</span></span>
1. <span data-ttu-id="2b92e-193">**Miktar** alanını *10* olarak ayarlayarak, lisans plakası üzerinde sayılan maddenin miktarını belirtin.</span><span class="sxs-lookup"><span data-stu-id="2b92e-193">Specify the quantity of the item that is counted on the license plate by setting the **Qty** field to *10*.</span></span>
1. <span data-ttu-id="2b92e-194">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="2b92e-194">Select **OK**.</span></span>

    <span data-ttu-id="2b92e-195">Sayfa, girdiğiniz konumu gösterir.</span><span class="sxs-lookup"><span data-stu-id="2b92e-195">The page shows the location that you entered.</span></span> <span data-ttu-id="2b92e-196">Ayrıca şu iletiyi gösterir: "yerleşim tamamlandı, yeni LP veya öğe Ekle?"</span><span class="sxs-lookup"><span data-stu-id="2b92e-196">It also shows the following message: "Location complete, add new LP or Item?"</span></span>

1. <span data-ttu-id="2b92e-197">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="2b92e-197">Select **OK**.</span></span>

<span data-ttu-id="2b92e-198">İş artık tamamlanmıştır.</span><span class="sxs-lookup"><span data-stu-id="2b92e-198">Work is now completed.</span></span>

#### <a name="spot-count-the-second-location"></a><span data-ttu-id="2b92e-199">Nokta ikinci konumu say</span><span class="sxs-lookup"><span data-stu-id="2b92e-199">Spot-count the second location</span></span>

1. <span data-ttu-id="2b92e-200">**Nokta sayım** sayfasında, **Konum** alanını *01A01R1S2B* olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="2b92e-200">On the **Spot Counting** page, set the **Location** field to *01A01R1S2B*.</span></span>
1. <span data-ttu-id="2b92e-201">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="2b92e-201">Select **OK**.</span></span>

    <span data-ttu-id="2b92e-202">Sayfa, girdiğiniz konumu gösterir.</span><span class="sxs-lookup"><span data-stu-id="2b92e-202">The page shows the location that you entered.</span></span> <span data-ttu-id="2b92e-203">Ayrıca şu iletiyi gösterir: "yerleşim tamamlandı, yeni LP veya öğe Ekle?"</span><span class="sxs-lookup"><span data-stu-id="2b92e-203">It also shows the following message: "Location complete, add new LP or Item?"</span></span>

1. <span data-ttu-id="2b92e-204">Yerleşime sayı eklemek için **Yenile** seçin.</span><span class="sxs-lookup"><span data-stu-id="2b92e-204">Select **Refresh** to add a count in the location.</span></span>
1. <span data-ttu-id="2b92e-205">**Döngü sayımında: Yeni LP veya madde Ekle** sayfası, **madde** alanını seçin ve *A0002* değerini girin.</span><span class="sxs-lookup"><span data-stu-id="2b92e-205">On the **Cycle Count: Add New LP or Item** page, select the **Item** field, and then enter the value *A0002*.</span></span>
1. <span data-ttu-id="2b92e-206">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="2b92e-206">Select **OK**.</span></span>
1. <span data-ttu-id="2b92e-207">**Döngü sayımı: yenı LP veya madde ekle** sayfası, **LP** alanını seçin ve sonra *LP1003* değerini (veya daha önce belirttiğiniz lisans plakasından farklı olarak istediğiniz diğer herhangi bir lisans plakası numarası) girin.</span><span class="sxs-lookup"><span data-stu-id="2b92e-207">On the **Cycle Count: Add New LP or Item** page, select the **LP** field, and then enter the value *LP1003* (or any other license plate number of your choice, provided that it differs from the both the license plate numbers that you specified in the previous procedure).</span></span>

    <span data-ttu-id="2b92e-208">**Döngü sayısı: Yeni LP veya madde ekle** sayfası **Lisans plağı 1. konumu** gösterir.</span><span class="sxs-lookup"><span data-stu-id="2b92e-208">The **Cycle Count: Add New LP or Item** page shows **License Plate Position 1**.</span></span>

1. <span data-ttu-id="2b92e-209">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="2b92e-209">Select **OK**.</span></span>
1. <span data-ttu-id="2b92e-210">**Miktar** alanını *10* olarak ayarlayarak, lisans plakası üzerinde sayılan maddenin miktarını belirtin.</span><span class="sxs-lookup"><span data-stu-id="2b92e-210">Specify the quantity of the item that is counted on the license plate by setting the **Qty** field to *10*.</span></span>
1. <span data-ttu-id="2b92e-211">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="2b92e-211">Select **OK**.</span></span>

    <span data-ttu-id="2b92e-212">Sayfa, girdiğiniz konumu gösterir.</span><span class="sxs-lookup"><span data-stu-id="2b92e-212">The page shows the location that you entered.</span></span> <span data-ttu-id="2b92e-213">Ayrıca şu iletiyi gösterir: "yerleşim tamamlandı, yeni LP veya öğe Ekle?"</span><span class="sxs-lookup"><span data-stu-id="2b92e-213">It also shows the following message: "Location complete, add new LP or Item?"</span></span>

1. <span data-ttu-id="2b92e-214">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="2b92e-214">Select **OK**.</span></span>

<span data-ttu-id="2b92e-215">İş artık tamamlanmıştır.</span><span class="sxs-lookup"><span data-stu-id="2b92e-215">Work is now completed.</span></span>

#### <a name="work-details"></a><span data-ttu-id="2b92e-216">İş ayrıntıları</span><span class="sxs-lookup"><span data-stu-id="2b92e-216">Work details</span></span>

> [!NOTE]
> <span data-ttu-id="2b92e-217">Mobil uygulamadaki nokta sayıları Microsoft Dynamics 365 içinde iş döngüsü sayımı işi oluştur.</span><span class="sxs-lookup"><span data-stu-id="2b92e-217">Spot counts from the mobile app create cycle counting work in Microsoft Dynamics 365.</span></span> <span data-ttu-id="2b92e-218">İş, sayımlar stoka nakledilmeden önce kabul edilmesini gerektirir.</span><span class="sxs-lookup"><span data-stu-id="2b92e-218">The work requires that the counts be accepted before they are posted to inventory.</span></span>

1. <span data-ttu-id="2b92e-219">Dynamics 365 Supply Chain Management'da oturum açın</span><span class="sxs-lookup"><span data-stu-id="2b92e-219">Sign in to Dynamics 365 Supply Chain Management.</span></span>
1. <span data-ttu-id="2b92e-220">**Ambar yönetimi \> İş \> İş ayrıntıları**'na gidin.</span><span class="sxs-lookup"><span data-stu-id="2b92e-220">Go to **Warehouse management \> Work \> Work details**.</span></span>
1. <span data-ttu-id="2b92e-221">**Özet** sekmesinde, aşağıdaki değerlere sahip satırları arayın:</span><span class="sxs-lookup"><span data-stu-id="2b92e-221">On the **Overview** tab, look for the lines that have the following values:</span></span>

    - <span data-ttu-id="2b92e-222">**İş emri türü:** *döngü sayımı*</span><span class="sxs-lookup"><span data-stu-id="2b92e-222">**Work order type:** *Cycle counting*</span></span>
    - <span data-ttu-id="2b92e-223">**Ambar:** *61*</span><span class="sxs-lookup"><span data-stu-id="2b92e-223">**Warehouse:** *61*</span></span>
    - <span data-ttu-id="2b92e-224">**İş durumu:** *Gözden geçirme bekleniyor*</span><span class="sxs-lookup"><span data-stu-id="2b92e-224">**Work status:** *Pending review*</span></span>

    <span data-ttu-id="2b92e-225">Bu satırlar için iki iş kodu oluşturulmuş olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="2b92e-225">Two work IDs should have been created for these lines.</span></span> <span data-ttu-id="2b92e-226">Bu iş kimliklerinin her ikisi için olan sayımlar kabul edilmesi gerekir.</span><span class="sxs-lookup"><span data-stu-id="2b92e-226">The counts for both these work IDs must be accepted.</span></span>

1. <span data-ttu-id="2b92e-227">Kılavuzda, *döngü sayımı* iş emri türü için ilk Iş kodunu seçin.</span><span class="sxs-lookup"><span data-stu-id="2b92e-227">In the grid, select the first work ID for the *Cycle counting* work order type.</span></span>
1. <span data-ttu-id="2b92e-228">Eylem Bölmesinde **İş** sekmesindeki **İş** grubunda **döngü sayımı**'nı seçin.</span><span class="sxs-lookup"><span data-stu-id="2b92e-228">On the Action Pane, on **Work** tab, in the **Work** group, select **Cycle counting**.</span></span>

    <span data-ttu-id="2b92e-229">Her biri her madde ve lisans levhası için olmak üzere iki satır gösterilir.</span><span class="sxs-lookup"><span data-stu-id="2b92e-229">Two lines are shown, one for each item and license plate.</span></span> <span data-ttu-id="2b92e-230">**Sayılan miktar**, **yerleşim**, **Lisans levhası** ve **madde** alanlarındaki değerler, mobil cihazda oluşturduğunuz sayım girişleriyle eşleşmelidir.</span><span class="sxs-lookup"><span data-stu-id="2b92e-230">The values in the **Counted quantity**, **Location**, **License plate**, and **Item** fields should match the count entries that you created on the mobile device.</span></span> <span data-ttu-id="2b92e-231">Bu alanlardan herhangi biri görünmüyorsa, kılavuza eklemek Için eylem bölmesindeki **boyutları görüntüle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="2b92e-231">If any of these fields aren't visible, select **Display dimensions** on the Action Pane to add them to the grid.</span></span>

1. <span data-ttu-id="2b92e-232">Her iki satırı da seçin.</span><span class="sxs-lookup"><span data-stu-id="2b92e-232">Select both lines.</span></span>
1. <span data-ttu-id="2b92e-233">Eylem Bölmesinde, **Sayımı kabul et**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="2b92e-233">On the Action Pane, select **Accept count**.</span></span>
1. <span data-ttu-id="2b92e-234">"Deftere nakil günlüğü" iletisi alıyorsunuz.</span><span class="sxs-lookup"><span data-stu-id="2b92e-234">You receive a "Posting - Journal" message.</span></span> <span data-ttu-id="2b92e-235">Deftere nakledilen günlük numarasını görüntülemek için **ileti ayrıntılarını** seçin.</span><span class="sxs-lookup"><span data-stu-id="2b92e-235">Select **Message details** to view the posted journal number.</span></span>
1. <span data-ttu-id="2b92e-236">İleti ayrıntılarını kapatın.</span><span class="sxs-lookup"><span data-stu-id="2b92e-236">Close the message details.</span></span>
1. <span data-ttu-id="2b92e-237">**İş** sayfasını yenileyin.</span><span class="sxs-lookup"><span data-stu-id="2b92e-237">Refresh the **Work** page.</span></span>

    <span data-ttu-id="2b92e-238">İlk iş kodu kapatıldı ve artık gösterilmemektedir.</span><span class="sxs-lookup"><span data-stu-id="2b92e-238">The first work ID has been closed and is no longer shown.</span></span>

    > [!TIP]
    > <span data-ttu-id="2b92e-239">Kapatılan çalışmayı görüntülemek için kılavuzun üzerindeki **kapalı göster** onay kutusunu seçin.</span><span class="sxs-lookup"><span data-stu-id="2b92e-239">To view closed work, select the **Show closed** check box above the grid.</span></span>

    <span data-ttu-id="2b92e-240">Şimdi, *01A01R1S2B* konumundaki lisans levhası için işi kabul etmiş olursunuz.</span><span class="sxs-lookup"><span data-stu-id="2b92e-240">You will now accept the work for the license plate in the *01A01R1S2B* location.</span></span>

1. <span data-ttu-id="2b92e-241">**Genel bakış** sekmesinde *döngü sayımı* iş emri türü için ikinci iş kodunu seçin.</span><span class="sxs-lookup"><span data-stu-id="2b92e-241">On the **Overview** tab, select the second work ID for the *Cycle counting* work order type.</span></span>
1. <span data-ttu-id="2b92e-242">Eylem Bölmesinde **İş** sekmesindeki **İş** grubunda **döngü sayımı**'nı seçin.</span><span class="sxs-lookup"><span data-stu-id="2b92e-242">On the Action Pane, on **Work** tab, in the **Work** group, select **Cycle counting**.</span></span>

    <span data-ttu-id="2b92e-243">Madde ve lisans levhası için bir satır gösterilir.</span><span class="sxs-lookup"><span data-stu-id="2b92e-243">One line is shown, for the item and license plate.</span></span> <span data-ttu-id="2b92e-244">**Sayılan miktar**, **yerleşim**, **Lisans levhası** ve **madde** alanlarındaki değerler, mobil cihazda oluşturduğunuz sayım girişleriyle eşleşmelidir.</span><span class="sxs-lookup"><span data-stu-id="2b92e-244">The values in the **Counted quantity**, **Location**, **License plate**, and **Item** fields should match the count entries that you created on the mobile device.</span></span>

1. <span data-ttu-id="2b92e-245">Satırı seçin.</span><span class="sxs-lookup"><span data-stu-id="2b92e-245">Select the line.</span></span>
1. <span data-ttu-id="2b92e-246">Eylem Bölmesinde, **Sayımı kabul et**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="2b92e-246">On the Action Pane, select **Accept count**.</span></span>
1. <span data-ttu-id="2b92e-247">"Deftere nakil günlüğü" iletisi alıyorsunuz.</span><span class="sxs-lookup"><span data-stu-id="2b92e-247">You receive a "Posting - Journal" message.</span></span> <span data-ttu-id="2b92e-248">Deftere nakledilen günlük numarasını görüntülemek için **ileti ayrıntılarını** seçin.</span><span class="sxs-lookup"><span data-stu-id="2b92e-248">Select **Message details** to view the posted journal number.</span></span>
1. <span data-ttu-id="2b92e-249">İleti ayrıntılarını kapatın.</span><span class="sxs-lookup"><span data-stu-id="2b92e-249">Close the message details.</span></span>
1. <span data-ttu-id="2b92e-250">**İş** sayfasını yenileyin.</span><span class="sxs-lookup"><span data-stu-id="2b92e-250">Refresh the **Work** page.</span></span>

    <span data-ttu-id="2b92e-251">İkinci iş kodu kapatıldı ve artık gösterilmemektedir.</span><span class="sxs-lookup"><span data-stu-id="2b92e-251">The second work ID has been closed and is no longer shown.</span></span>

    > [!TIP]
    > <span data-ttu-id="2b92e-252">Kapatılan çalışmayı görüntülemek için kılavuzun üzerindeki **kapalı göster** onay kutusunu seçin.</span><span class="sxs-lookup"><span data-stu-id="2b92e-252">To view closed work, select the **Show closed** check box above the grid.</span></span>

#### <a name="on-hand-by-location"></a><span data-ttu-id="2b92e-253">Konuma göre eldeki</span><span class="sxs-lookup"><span data-stu-id="2b92e-253">On-hand by location</span></span>

1. <span data-ttu-id="2b92e-254">**Ambar yönetimi \> Sorgular ve raporlar \> Yerleşime göre eldeki**'ye gidin.</span><span class="sxs-lookup"><span data-stu-id="2b92e-254">Go to **Warehouse management \> Inquiries and reports \> On-hand by location**.</span></span>
1. <span data-ttu-id="2b92e-255">Aşağıdaki değerleri ayarlayın:</span><span class="sxs-lookup"><span data-stu-id="2b92e-255">Set the following values:</span></span>

    - <span data-ttu-id="2b92e-256">**Tesis:** *6*</span><span class="sxs-lookup"><span data-stu-id="2b92e-256">**Site:** *6*</span></span>
    - <span data-ttu-id="2b92e-257">**Ambar:** *61*</span><span class="sxs-lookup"><span data-stu-id="2b92e-257">**Warehouse:** *61*</span></span>
    - <span data-ttu-id="2b92e-258">**Konumlar arasında Yenile:** *Evet*</span><span class="sxs-lookup"><span data-stu-id="2b92e-258">**Refresh across locations:** *Yes*</span></span>

1. <span data-ttu-id="2b92e-259">*01A01R1S1B* konumunun iki lisans tabakadığına sahip olduğuna dikkat edin:</span><span class="sxs-lookup"><span data-stu-id="2b92e-259">Notice that location *01A01R1S1B* has two license plates:</span></span>

    - <span data-ttu-id="2b92e-260">**A0001**, **LP Konumu** alanının *1* olarak ayarlandığı yerdir</span><span class="sxs-lookup"><span data-stu-id="2b92e-260">**A0001**, where the **LP Position** field is set to *1*</span></span>
    - <span data-ttu-id="2b92e-261">**A0002**, **LP Konumu** alanının *2* olarak ayarlandığı yerdir</span><span class="sxs-lookup"><span data-stu-id="2b92e-261">**A0002**, where the **LP Position** field is set to *2*</span></span>

1. <span data-ttu-id="2b92e-262">*01A01R1S2B* konumunun bir lisans tabakadığına sahip olduğuna dikkat edin:</span><span class="sxs-lookup"><span data-stu-id="2b92e-262">Notice that location *01A01R1S2B* has one license plate:</span></span>

    - <span data-ttu-id="2b92e-263">**A0002**, **LP Konumu** alanının *1* olarak ayarlandığı yerdir</span><span class="sxs-lookup"><span data-stu-id="2b92e-263">**A0002**, where the **LP Position** field is set to *1*</span></span>

### <a name="sales-order-scenario"></a><span data-ttu-id="2b92e-264">Satış siparişi senaryosu</span><span class="sxs-lookup"><span data-stu-id="2b92e-264">Sales order scenario</span></span>

<span data-ttu-id="2b92e-265">*Yerleşim lisansı plak konumlama* özelliği ayarlanmış ve stok hazırlanmıştır, böylece ambar çalışanını Palet kodunun pozisyon *1* ' deki stok yerleşiminden çekme maddesi *A0002* yönlendirecek şekilde bir satış siparişi oluşturmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="2b92e-265">Now that the *Location license plate positioning* feature has been set up, and the inventory has been staged, you must create a sales order to generate picking work that will direct the warehouse worker to pick item *A0002* from the inventory location where the pallet ID is in position *1*.</span></span>

1. <span data-ttu-id="2b92e-266">**Satış ve pazarlama \> Satış siparişleri \> Tüm satış siparişleri**'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="2b92e-266">Go to **Sales and marketing \> Sales orders \> All sales orders**.</span></span>
1. <span data-ttu-id="2b92e-267">Eylem Bölmesinde, **Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="2b92e-267">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="2b92e-268">**Satış siparişi oluştur** iletişim kutusunda, aşağıdaki değerleri ayarlayın:</span><span class="sxs-lookup"><span data-stu-id="2b92e-268">In the **Create sales order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="2b92e-269">**Müşteri hesabı:** *US-004*</span><span class="sxs-lookup"><span data-stu-id="2b92e-269">**Customer account:** *US-004*</span></span>
    - <span data-ttu-id="2b92e-270">**Ambar:** *61*</span><span class="sxs-lookup"><span data-stu-id="2b92e-270">**Warehouse:** *61*</span></span>

1. <span data-ttu-id="2b92e-271">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="2b92e-271">Select **OK**.</span></span>
1. <span data-ttu-id="2b92e-272">**Satış siparişi satırları** hızlı sekmesine yeni bir satır eklenir.</span><span class="sxs-lookup"><span data-stu-id="2b92e-272">A new line is added to the grid on the **Sales order lines** FastTab.</span></span> <span data-ttu-id="2b92e-273">Bu yeni satırda aşağıdaki değerleri ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="2b92e-273">On this new line, set the following values:</span></span>

    - <span data-ttu-id="2b92e-274">**Madde numarası:** *A0002*</span><span class="sxs-lookup"><span data-stu-id="2b92e-274">**Item number:** *A0002*</span></span>
    - <span data-ttu-id="2b92e-275">**Miktar:** *1*</span><span class="sxs-lookup"><span data-stu-id="2b92e-275">**Quantity:** *1*</span></span>

1. <span data-ttu-id="2b92e-276">Kılavuzun üzerindeki **stok** menüsünde **rezervasyon**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="2b92e-276">On the **Inventory** menu above the grid, select **Reservation**.</span></span>
1. <span data-ttu-id="2b92e-277">**Rezervasyon** sayfasında, Eylem Bölmesi'nde sipariş satırı için envanter rezerve etmek için **Lotu rezerve et**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="2b92e-277">On the **Reservation** page, on the Action Pane, select **Reserve lot** to reserve inventory for the order line.</span></span>
1. <span data-ttu-id="2b92e-278">**Rezervasyon** sayfasını kapatın.</span><span class="sxs-lookup"><span data-stu-id="2b92e-278">Close the **Reservation** page.</span></span>
1. <span data-ttu-id="2b92e-279">Eylem Bölmesinde, **Ambar** sekmesindeki **Eylemler** grubunda, **Ambara serbest bırak**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="2b92e-279">On the Action Pane, on the **Warehouse** tab, in the **Actions** group, select **Release to warehouse**.</span></span>

    <span data-ttu-id="2b92e-280">Satış siparişi için oluşturulan dalga kimliğini ve sevkiyat kimliklerini gösteren bilgi iletileri alırsınız.</span><span class="sxs-lookup"><span data-stu-id="2b92e-280">You receive an informational message that indicates the wave ID and shipment ID that were created for the order.</span></span>

1. <span data-ttu-id="2b92e-281">**Satış siparişi satırları** hızlı sekmesinde kılavuz üzerinde **Ambar** menüsünde **İş ayrıntıları**'nı seçin.</span><span class="sxs-lookup"><span data-stu-id="2b92e-281">On the **Sales order lines** FastTab, on the **Warehouse** menu above the grid, select **Work details**.</span></span>
1. <span data-ttu-id="2b92e-282">**İş** sayfası görüntülenir ve satış satırı için oluşturulan işi gösterir.</span><span class="sxs-lookup"><span data-stu-id="2b92e-282">The **Work** page appears and shows the work that was created for the sales line.</span></span> <span data-ttu-id="2b92e-283">Gösterilen iş kimliğini not edin.</span><span class="sxs-lookup"><span data-stu-id="2b92e-283">Make a note of the work ID that is shown.</span></span>

### <a name="sales-picking-scenario"></a><span data-ttu-id="2b92e-284">Satış malzeme çekme senaryosu</span><span class="sxs-lookup"><span data-stu-id="2b92e-284">Sales picking scenario</span></span>

1. <span data-ttu-id="2b92e-285">Mobil uygulamasında ambar *61*'deki bir kullanıcı olarak oturum açın.</span><span class="sxs-lookup"><span data-stu-id="2b92e-285">Open the mobile app, and sign in to warehouse *61*.</span></span>
1. <span data-ttu-id="2b92e-286">**Giden \> Satış Çekme**'yi gidin.</span><span class="sxs-lookup"><span data-stu-id="2b92e-286">Go to **Outbound \> Sales picking**.</span></span>
1. <span data-ttu-id="2b92e-287">**Iş kodu Tara/lisans levhası kimlik** sayfasında **kimlik** alanını seçin ve satış satırındaki iş kodunu girin.</span><span class="sxs-lookup"><span data-stu-id="2b92e-287">On the **Scan a work ID / license plate ID** page, select the **ID** field, and then enter the work ID from the sales line.</span></span>
1. <span data-ttu-id="2b92e-288">Malzeme çekme çalışmasının *A0002* *01A01R1S2B* konumundan maddeyi çekmesini yönlendirdiğine dikkat edin.</span><span class="sxs-lookup"><span data-stu-id="2b92e-288">Notice that the picking work directs you to pick item *A0002* from location *01A01R1S2B*.</span></span> <span data-ttu-id="2b92e-289">Bu yönergeyi, madde *A0002* Bu konumdaki *1* konumunda bulunan bir lisans kalıbının açık olması nedeniyle alırsınız.</span><span class="sxs-lookup"><span data-stu-id="2b92e-289">You receive this instruction because item *A0002* is on a license plate that is in position *1* in that location.</span></span>

    <span data-ttu-id="2b92e-290">![Pozisyon 1 konumu](media/LocationLicensePlatePositioning.png "Pozisyon 1 konumu")</span><span class="sxs-lookup"><span data-stu-id="2b92e-290">![Position 1 location](media/LocationLicensePlatePositioning.png "Position 1 location")</span></span>

1. <span data-ttu-id="2b92e-291">Konum için oluşturduğunuz lisans plakası kodunu girin ve satış siparişini seçmek için istemleri izleyin.</span><span class="sxs-lookup"><span data-stu-id="2b92e-291">Enter the license plate ID that you created for the location, and then follow the prompts to pick the sales order.</span></span>
