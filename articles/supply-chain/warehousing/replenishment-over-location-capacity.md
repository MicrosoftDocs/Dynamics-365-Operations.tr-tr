---
title: Yerleşim kapasitesine göre stok yenileme
description: Bu konu, Konum kapasitesine göre stok yenileme özelliği hakkında bilgi sağlar. Bu özellik, gün için gerekli olacak tüm stok yenileme işini etkinleştirir ve malzeme çekme konumunun stok dışında veya kapasitenin üzerine geçmediğinden emin olmak amacıyla bu stok yenileme çalışmasının kullanılabilirliğini yönetir.
author: mirzaab
manager: tfehr
ms.date: 07/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSReplenishmentTemplates, WHSLocationLimit
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-16
ms.dyn365.ops.version: Release 10.0.7
ms.openlocfilehash: 8e9ae16fea892d1d6b6a6b5d06137576623e7f5b
ms.sourcegitcommit: 827d77c638555396b32d36af5d22d1b61dafb0e8
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4439688"
---
# <a name="replenishment-over-location-capacity"></a><span data-ttu-id="4b9e9-104">Yerleşim kapasitesine göre stok yenileme</span><span class="sxs-lookup"><span data-stu-id="4b9e9-104">Replenishment over location capacity</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="4b9e9-105">Bazı yüksek hacimli veya alan kısıtlamalı ambarlar, malzeme çekme konumuna sığmayacak bir gün içindeki kalem miktarını sevk etmelidir.</span><span class="sxs-lookup"><span data-stu-id="4b9e9-105">Some high-volume or space-constrained warehouses must ship more quantity of an item in a day than will fit in the picking location.</span></span> <span data-ttu-id="4b9e9-106">*Konum kapasitesine göre stok yenileme* özelliği, gün için gerekli olacak tüm stok yenileme işini etkinleştirir ve malzeme çekme konumunun stok dışında veya kapasitenin üzerine geçmediğinden emin olmak amacıyla bu stok yenileme çalışmasının kullanılabilirliğini yönetir.</span><span class="sxs-lookup"><span data-stu-id="4b9e9-106">The *Replenishment over location capacity* feature enables all replenishment work that will be required for the day to be created and manages availability of that replenishment work to ensure that the picking location neither runs out of inventory nor goes above capacity.</span></span>

<span data-ttu-id="4b9e9-107">Özellik, bir konuma sığacak olandan daha fazla stok yenileme işinin oluşturulmasını sağlar ve konum dolduğunda, stok yenileme işinin tamamlanmasını engeller.</span><span class="sxs-lookup"><span data-stu-id="4b9e9-107">The feature enables more replenishment work to be created than will fit in a location, and it blocks replenishment work from being completed when the location is full.</span></span> <span data-ttu-id="4b9e9-108">Malzeme çekme konumundaki stok yapılandırılabilir bir eşiğin altına düşerse daha fazla stok yenileme işi kullanılabilir duruma getirilir.</span><span class="sxs-lookup"><span data-stu-id="4b9e9-108">As inventory in the picking location drops below a configurable threshold, more replenishment work is made available.</span></span>

## <a name="turn-on-the-replenishment-over-location-capacity-feature"></a><span data-ttu-id="4b9e9-109">Konum kapasitesine göre stok yenileme özelliğini açma</span><span class="sxs-lookup"><span data-stu-id="4b9e9-109">Turn on the Replenishment over location capacity feature</span></span>

<span data-ttu-id="4b9e9-110">Bu özelliği kullanılabilir hale getirmek için [özellik yönetiminde](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) aşağıdaki özellikleri etkinleştirin (bu sırayla):</span><span class="sxs-lookup"><span data-stu-id="4b9e9-110">To make this feature available, turn on the following features in [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) (in this order):</span></span>

1. <span data-ttu-id="4b9e9-111">Kuruluş çapında işi engelleme</span><span class="sxs-lookup"><span data-stu-id="4b9e9-111">Organization-wide work blocking</span></span>
1. <span data-ttu-id="4b9e9-112">Yerleşim kapasitesine göre stok yenileme</span><span class="sxs-lookup"><span data-stu-id="4b9e9-112">Replenishment over location capacity</span></span>

## <a name="set-up-the-feature-for-the-example-scenario"></a><span data-ttu-id="4b9e9-113">Örnek senaryo için özelliği ayarlama</span><span class="sxs-lookup"><span data-stu-id="4b9e9-113">Set up the feature for the example scenario</span></span>

<span data-ttu-id="4b9e9-114">Bu bölümde, bu özelliğin nasıl ayarlanacağı ve bu konunun ilerleyen kısımlarında sağlanan örnek senaryo için örnek verilerin nasıl hazırlanacağı gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="4b9e9-114">This section provides guidelines and an example that shows how to set up this feature and prepare sample data for the example scenario that is provided later in this topic.</span></span>

### <a name="enable-sample-data"></a><span data-ttu-id="4b9e9-115">Örnek verileri etkinleştirme</span><span class="sxs-lookup"><span data-stu-id="4b9e9-115">Enable sample data</span></span>

<span data-ttu-id="4b9e9-116">Burada belirtilen örnek kayıtları ve değerleri kullanarak [örnek senaryo](#example-scenario) üzerinden çalışmak için standart [demo verilerinin](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) yüklenmiş olduğu bir sistemde olmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="4b9e9-116">To work through the [example scenario](#example-scenario) by using the sample records and values that are specified here, you must be on a system where the standard [demo data](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) is installed.</span></span> <span data-ttu-id="4b9e9-117">Ek olarak, başlamadan önce **USMF** tüzel kişiliğini seçmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="4b9e9-117">Additionally, you must select the **USMF** legal entity before you begin.</span></span>

### <a name="location-profile"></a><span data-ttu-id="4b9e9-118">Yerleşim profili</span><span class="sxs-lookup"><span data-stu-id="4b9e9-118">Location profile</span></span>

<span data-ttu-id="4b9e9-119">Konum profilinde kapasiteye göre stok yenileme işlevini etkinleştirin.</span><span class="sxs-lookup"><span data-stu-id="4b9e9-119">Enable the replenish over capacity functionality on the location profile.</span></span>

1. <span data-ttu-id="4b9e9-120">**Ambar yönetimi \> Kurulum \> Ambar \> Konum profilleri**'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="4b9e9-120">Go to **Warehouse management \> Setup \> Warehouse \> Locations profiles**.</span></span>
1. <span data-ttu-id="4b9e9-121">Sol bölmede **PICK-06** seçin.</span><span class="sxs-lookup"><span data-stu-id="4b9e9-121">In the left pane, select **PICK-06**.</span></span>
1. <span data-ttu-id="4b9e9-122">Eylem Bölmesi'nde, **Düzenle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="4b9e9-122">On the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="4b9e9-123">**Stok yenileme** hızlı sekmesinde, aşağıdaki değerleri ayarlayın:</span><span class="sxs-lookup"><span data-stu-id="4b9e9-123">On the **Replenishment** FastTab, set the following values:</span></span>

    - <span data-ttu-id="4b9e9-124">**Konum Kapasitesini Aş:** *Evet*</span><span class="sxs-lookup"><span data-stu-id="4b9e9-124">**Exceed Location Capacity:** *Yes*</span></span>

        <span data-ttu-id="4b9e9-125">Etkin olduğunda, yerleşimin maksimum kapasitesinin stok yenileme işi tarafından aşılmasına izin verilir.</span><span class="sxs-lookup"><span data-stu-id="4b9e9-125">When enabled, the maximum capacity of the location will be allowed to be exceeded by replenishment work.</span></span> <span data-ttu-id="4b9e9-126">Ayrıca, **Stok yenileme** hızlı sekmesindeki diğer alanları da etkinleştirir.</span><span class="sxs-lookup"><span data-stu-id="4b9e9-126">This also enables other fields on the **Replenishment** FastTab.</span></span>

    - <span data-ttu-id="4b9e9-127">**İş kullanılabilirlik eşiği türü:** *Miktar*</span><span class="sxs-lookup"><span data-stu-id="4b9e9-127">**Work availability threshold type:** *Quantity*</span></span>

        <span data-ttu-id="4b9e9-128">Bu alan, ne kadar işin serbest bırakılacağını belirlemek için kullanılan yöntemi tanımlar.</span><span class="sxs-lookup"><span data-stu-id="4b9e9-128">This field defines the method that is used to determine when more work should be released.</span></span> <span data-ttu-id="4b9e9-129">Miktar ya da yüzdeye göre serbest bırakabilirsiniz:</span><span class="sxs-lookup"><span data-stu-id="4b9e9-129">You can release by either quantity or a percentage:</span></span>

        - <span data-ttu-id="4b9e9-130">*Yüzde* - Stok sınırları veya hacimlere göre kapasite yüzdesi kullanmak için bu seçeneği işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="4b9e9-130">*Percent* – Select this option to use percentage capacity that is based on stocking limits or volumetrics.</span></span> <span data-ttu-id="4b9e9-131">Bu seçeneğin belirlenmesi **Taşma yüzdesi** alanını etkinleştirir ve ilgili iki miktar alanı olan **Taşma miktarı** ve **Taşma birimi**'ni devre dışı bırakır.</span><span class="sxs-lookup"><span data-stu-id="4b9e9-131">Selecting this option enables the **Overflow percentage** field, and disables the two quantity related fields,  **Overflow quantity** and **Overflow unit**.</span></span>

            <span data-ttu-id="4b9e9-132">Malzeme çekme konumları hacim kullanıyorsa bu seçeneği kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="4b9e9-132">You can use this option if the picking locations use volumetrics.</span></span>

            <span data-ttu-id="4b9e9-133">Bu seçenek işaretliyse **Taşma yüzdesi** alanını daha fazla stok yenileme işinin kullanılabilir hale gelmesini sağlayacak yüzdeye ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="4b9e9-133">If this option is selected, set the **Overflow percentage** field to the percentage at which more replenishment work will be made available.</span></span>

        - <span data-ttu-id="4b9e9-134">*Miktar* - Belirli bir miktar değeri kullanmak için bu seçeneği belirleyin.</span><span class="sxs-lookup"><span data-stu-id="4b9e9-134">*Quantity* – Select this option to use a specific quantity value.</span></span> <span data-ttu-id="4b9e9-135">Bu seçeneğin belirlenmesi **Taşma yüzdesi** alanını devre dışı bırakır ve **Taşma miktarı** ile **Taşma birimi** alanlarını etkinleştirir.</span><span class="sxs-lookup"><span data-stu-id="4b9e9-135">Selecting this option disables the **Overflow percentage** field and enables **Overflow quantity** and **Overflow unit** fields.</span></span>

            <span data-ttu-id="4b9e9-136">Stok yenilenen konumlarda hacim kullanmıyorsanız veya konuma daha fazla stok getirilmesini istediğiniz tutarlı miktarlar olduğunda bu seçeneği kullanın.</span><span class="sxs-lookup"><span data-stu-id="4b9e9-136">Use this option when you aren't using volumetrics for the locations that are being replenished, or when you have consistent quantities at which you want more inventory to be brought to the location.</span></span>

           <span data-ttu-id="4b9e9-137">Bu seçenek işaretliyse **Taşma miktarı** ve **Taşma birimi** alanlarını daha fazla stok yenileme işinin kullanılabilir hale gelmesini sağlayacak miktara ve birime ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="4b9e9-137">If this option is selected, set the **Overflow quantity** and **Overflow unit** fields to the quantity and unit at which more replenishment work will be made available.</span></span>

    - <span data-ttu-id="4b9e9-138">**Taşma miktarı:** *0,65*</span><span class="sxs-lookup"><span data-stu-id="4b9e9-138">**Overflow quantity:** *0.65*</span></span>

        <span data-ttu-id="4b9e9-139">Bu alan, konumun taştığı miktarı tanımlar.</span><span class="sxs-lookup"><span data-stu-id="4b9e9-139">This field defines the quantity at which the location overflows.</span></span>

        <span data-ttu-id="4b9e9-140">İş, konumdaki eldeki stok miktarı ve iş miktarı toplamı bu değerin altında olduğunda kullanılabilir olur.</span><span class="sxs-lookup"><span data-stu-id="4b9e9-140">Work will be available whenever the sum of the on-hand quantity in the location and the work quantity is below this value.</span></span> <span data-ttu-id="4b9e9-141">Bu değerin üzerindeki tüm stok yenileme işleri engellenir ve engellemenin el ile kaldırılması gerekir.</span><span class="sxs-lookup"><span data-stu-id="4b9e9-141">Any replenishment work above this value will be blocked and must be manually unblocked.</span></span>

        <span data-ttu-id="4b9e9-142">Konum stok sınırlamaları, iş miktarı hesaplanırken dikkate alınır.</span><span class="sxs-lookup"><span data-stu-id="4b9e9-142">Location stocking limits are considered when the work quantity is calculated.</span></span>

    - <span data-ttu-id="4b9e9-143">**Taşma birimi:** *PL*</span><span class="sxs-lookup"><span data-stu-id="4b9e9-143">**Overflow unit:** *PL*</span></span>

        <span data-ttu-id="4b9e9-144">Bu alan taşma miktarıyla ilişkilendirilmiş birimi tanımlar.</span><span class="sxs-lookup"><span data-stu-id="4b9e9-144">This field defines the unit that is associated with the overflow quantity.</span></span>

        <span data-ttu-id="4b9e9-145">Bu durumda, konum 0,65 palet (PL) olarak ayarlandığında, daha fazla stok yenileme işi kullanılabilir duruma gelir.</span><span class="sxs-lookup"><span data-stu-id="4b9e9-145">In this case, more replenishment work will be made available when the location gets down to 0.65 pallet (PL).</span></span>

    - <span data-ttu-id="4b9e9-146">**Taşma yüzdesi**</span><span class="sxs-lookup"><span data-stu-id="4b9e9-146">**Overflow percentage**</span></span>

        <span data-ttu-id="4b9e9-147">Bu alan, konumun taştığı yüzdeyi tanımlar.</span><span class="sxs-lookup"><span data-stu-id="4b9e9-147">This field defines the percentage at which the location overflows.</span></span>

        <span data-ttu-id="4b9e9-148">İş, konumdaki eldeki stok miktarı ve iş miktarı toplamı bu yüzdenin altında olduğunda kullanılabilir olur.</span><span class="sxs-lookup"><span data-stu-id="4b9e9-148">Work will be available whenever the sum of the on-hand quantity in the location and the work quantity is below this percentage.</span></span> <span data-ttu-id="4b9e9-149">Bu değerin üzerindeki tüm stok yenileme işi miktarı yüzdesi engellenir ve engellemenin el ile kaldırılması gerekir.</span><span class="sxs-lookup"><span data-stu-id="4b9e9-149">Any replenishment work quantity percentage above this value will be blocked and must be manually unblocked.</span></span>

        <span data-ttu-id="4b9e9-150">Konum stok sınırlamaları, iş miktarı yüzdesi hesaplanırken dikkate alınır.</span><span class="sxs-lookup"><span data-stu-id="4b9e9-150">Location stocking limits are considered when the work quantity percentage is calculated.</span></span> <span data-ttu-id="4b9e9-151">Konum stok sınırlarının tanımlanmaması durumunda, konum profili için birim kısıtlamaları tanımlandıysa iş miktarı yüzdesi birime göre hesaplanır.</span><span class="sxs-lookup"><span data-stu-id="4b9e9-151">If no location stocking limits are defined, the work quantity percentage is calculated by volume if volume constraints are defined for the location profile.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="4b9e9-152">**USMF** tüzel kişiliği ve daha önce etkinleştirilen *Konum plakası konumlandırması* özelliği için demo verileri kullanıyorsanız, örnek senaryoda mobil adımları tamamlamak için **BULK-06** konum profilinin **Plaka konumlandırmayı etkinleştir** ayarını kapatmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="4b9e9-152">If you're using the demo data for the **USMF** legal entity and previously turned on the *Location license plate positioning* feature, you must turn off the **Enable license plate positioning** setting for the **BULK-06** location profile to complete the mobile steps in the example scenario.</span></span>

### <a name="wave-step-code"></a><span data-ttu-id="4b9e9-153">Dalga adım kodu</span><span class="sxs-lookup"><span data-stu-id="4b9e9-153">Wave step code</span></span>

> [!NOTE]
> <span data-ttu-id="4b9e9-154">Burada açıklandığı gibi bir dalga adımı kodu ayarlamak için öncelikle *Kuruluş genelinde dalga adımı kodu* adlı özelliği açmak üzere [özellik yönetimini](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) kullanmanız gerekebilir.</span><span class="sxs-lookup"><span data-stu-id="4b9e9-154">To set up a wave step code as described here, you might first have to use [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) to turn on the feature that is named *Organization wide wave step code*.</span></span>

1. <span data-ttu-id="4b9e9-155">**Ambar Yönetimi \> Kurulum \> Dalgalar \> Dalga adımı kodları**'na gidin.</span><span class="sxs-lookup"><span data-stu-id="4b9e9-155">Go to **Warehouse Management \> Setup \> Waves \> Wave step codes**.</span></span>
1. <span data-ttu-id="4b9e9-156">**Yeni**'yi seçin ve ardından aşağıdaki değerleri ayarlayın:</span><span class="sxs-lookup"><span data-stu-id="4b9e9-156">Select **New**, and set the following values:</span></span>

    - <span data-ttu-id="4b9e9-157">**Dalga adımı kodu:** *Stok yenileme*</span><span class="sxs-lookup"><span data-stu-id="4b9e9-157">**Wave step code:** *Replen*</span></span>
    - <span data-ttu-id="4b9e9-158">**Dalga adımı açıklaması:** *Stok yenileme*</span><span class="sxs-lookup"><span data-stu-id="4b9e9-158">**Wave step description:** *Replenishment*</span></span>
    - <span data-ttu-id="4b9e9-159">**Dalga adımı türü:** *Stok yenileme*</span><span class="sxs-lookup"><span data-stu-id="4b9e9-159">**Wave step type:** *Replenishment*</span></span>

1. <span data-ttu-id="4b9e9-160">**Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="4b9e9-160">Select **Save**.</span></span>

### <a name="replenishment-template"></a><span data-ttu-id="4b9e9-161">Stok yenileme şablonu</span><span class="sxs-lookup"><span data-stu-id="4b9e9-161">Replenishment template</span></span>

<span data-ttu-id="4b9e9-162">Stok yenileme şablonları, bir konumda stokun ne zaman ve nasıl yenileneceğini denetleyen kural kümesidir.</span><span class="sxs-lookup"><span data-stu-id="4b9e9-162">Replenishment templates are a set of rules that control when and how a location is replenished.</span></span>

1. <span data-ttu-id="4b9e9-163">**Ambar yönetimi \> Kurulum \> Stok yenileme \> Stok yenileme şablonları**'na gidin.</span><span class="sxs-lookup"><span data-stu-id="4b9e9-163">Go to **Warehouse management \> Setup \> Replenishment \> Replenishment templates**.</span></span>
1. <span data-ttu-id="4b9e9-164">Eylem Bölmesi'nde, **Düzenle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="4b9e9-164">On the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="4b9e9-165">**Genel Bakış** bölümünde, **Stok yenileme şablonu** alanının *Talep stok yenilemesi* olarak ayarlandığı satırı seçin.</span><span class="sxs-lookup"><span data-stu-id="4b9e9-165">In the **Overview** section, select the line where the **Replenish template** field is set to *Demand replenish*.</span></span>
1. <span data-ttu-id="4b9e9-166">Aşağıdaki değerleri ayarlayın:</span><span class="sxs-lookup"><span data-stu-id="4b9e9-166">Set the following values:</span></span>

    - <span data-ttu-id="4b9e9-167">**Dalga adımı kodu:** *Stok yenileme*</span><span class="sxs-lookup"><span data-stu-id="4b9e9-167">**Wave step code:** *Replen*</span></span>
    - <span data-ttu-id="4b9e9-168">**Dalga talebinin rezerve edilmemiş miktarları kullanmasına izin ver:** *Evet*</span><span class="sxs-lookup"><span data-stu-id="4b9e9-168">**Allow wave demand to use unreserved quantities:** *Yes*</span></span>

1. <span data-ttu-id="4b9e9-169">**Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="4b9e9-169">Select **Save**.</span></span>

### <a name="wave-template"></a><span data-ttu-id="4b9e9-170">Dalga şablonu</span><span class="sxs-lookup"><span data-stu-id="4b9e9-170">Wave template</span></span>

1. <span data-ttu-id="4b9e9-171">**Ambar yönetimi \> Kurulum \> Dalgalar \> Dalga şablonları**'na gidin.</span><span class="sxs-lookup"><span data-stu-id="4b9e9-171">Go to **Warehouse management \> Setup \> Waves \> Wave templates**.</span></span>
1. <span data-ttu-id="4b9e9-172">Sol bölmede, **Dalga şablonu türü** alanını *Sevkiyat* olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="4b9e9-172">In the left pane, set the **Wave template type** field to *Shipping*.</span></span>
1. <span data-ttu-id="4b9e9-173">Listeden **61 Sevkiyat** şablonunu seçin.</span><span class="sxs-lookup"><span data-stu-id="4b9e9-173">Select template **61 Shipping** in the list.</span></span>
1. <span data-ttu-id="4b9e9-174">Eylem Bölmesi'nde, **Düzenle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="4b9e9-174">On the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="4b9e9-175">**Genel** hızlı sekmesinde **Stok yenileme işi serbest bırakmayı otomatik hale getir** seçeneğini *Evet* olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="4b9e9-175">On the **General** FastTab, set the **Automate replenishment work release** option to *Yes*.</span></span>

    <span data-ttu-id="4b9e9-176">Talep tabanlı stok yenileme işi oluşturmak ve bunu otomatik olarak serbest bırakmak için bu seçeneği *Evet* olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="4b9e9-176">Set this option to *Yes* to create demand-based replenishment work and release it automatically.</span></span> <span data-ttu-id="4b9e9-177">Stok yenileme dalga yöntemini dalga şablonuna eklemeniz **Dalga talebi** türünde stok yenileme şablonu oluşturmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="4b9e9-177">You must add the replenishment wave method to the wave template and create a replenishment template of the **Wave demand** type.</span></span> <span data-ttu-id="4b9e9-178">**Stok yenileme şablonları** sayfasında bir stok yenileme şablonu ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="4b9e9-178">Set up a replenishment template on the **Replenishment templates** page.</span></span> <span data-ttu-id="4b9e9-179">Stok yenileme şablonu ayarlamak için bu stok yenileme yöntemini dalga şablonuna eklemeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="4b9e9-179">To set up a replenishment template, you must add the replenish method to the wave template.</span></span>

1. <span data-ttu-id="4b9e9-180">**Yöntemler** hızlı sekmesinde, **Seçili yöntemler** sütununda, aşağıdaki satırı bulun:</span><span class="sxs-lookup"><span data-stu-id="4b9e9-180">On the **Methods** FastTab, in the **Selected methods** column, find the following line:</span></span>

    - <span data-ttu-id="4b9e9-181">**Yöntem adı:** *stok yenileme*</span><span class="sxs-lookup"><span data-stu-id="4b9e9-181">**Method name:** *replenish*</span></span>
    - <span data-ttu-id="4b9e9-182">**Ad:** *Stok yenileme*</span><span class="sxs-lookup"><span data-stu-id="4b9e9-182">**Name:** *Replenishment*</span></span>

1. <span data-ttu-id="4b9e9-183">Bu satır için **Dalga adımı kodu** alanını *Stok yenileme* olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="4b9e9-183">Set the **Wave step code** field for this line to *Replen*.</span></span>
1. <span data-ttu-id="4b9e9-184">**Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="4b9e9-184">Select **Save**.</span></span>

## <a name="example-scenario"></a><span data-ttu-id="4b9e9-185">Örnek senaryo</span><span class="sxs-lookup"><span data-stu-id="4b9e9-185">Example scenario</span></span>

<span data-ttu-id="4b9e9-186">Daha önce açıklanan örnek verilerin tümünü kullanılabilir hale getirip ayarladıktan sonra, bu senaryoda, *Konum kapasitesine göre stok yenileme* özelliğini deneyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="4b9e9-186">After you've made all the previously described sample data available and set it up, you can work through this scenario to try out the *Replenishment over location capacity* feature.</span></span> <span data-ttu-id="4b9e9-187">Bu senaryoda gösterilen değerler, standart demo verileriyle çalıştığınızı, **USMF** tüzel kişiliğini seçmiş olduğunuzu ve bu konunun önceki bölümlerinde açıklanan örnek kayıtları hazırladığınızı varsayar.</span><span class="sxs-lookup"><span data-stu-id="4b9e9-187">The values that are shown in this scenario assume that you're working with the standard demo data, that you selected the **USMF** legal entity, and that you prepared the sample records that are described earlier in this topic.</span></span> <span data-ttu-id="4b9e9-188">Bu senaryo aynı zamanda özelliğin bir üretim ayarında nasıl kullanılabileceğini gösteren bir örnek işlevi de görür.</span><span class="sxs-lookup"><span data-stu-id="4b9e9-188">This scenario also serves as an example that shows how the feature can be used in a production setting.</span></span>

### <a name="create-replenishment-work"></a><span data-ttu-id="4b9e9-189">Stok yenileme işi oluştur</span><span class="sxs-lookup"><span data-stu-id="4b9e9-189">Create replenishment work</span></span>

#### <a name="create-sales-order-1"></a><span data-ttu-id="4b9e9-190">Satış siparişi oluşturma 1</span><span class="sxs-lookup"><span data-stu-id="4b9e9-190">Create sales order 1</span></span>

1. <span data-ttu-id="4b9e9-191">**Satış ve pazarlama \> Satış siparişleri \> Tüm satış siparişleri**'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="4b9e9-191">Go to **Sales and marketing \> Sales orders \> All sales orders**.</span></span>
1. <span data-ttu-id="4b9e9-192">Eylem Bölmesinde, yeni satış siparişi oluşturma iletişim kutusunu açmak için **Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="4b9e9-192">On the Action Pane, select **New** to open a dialog box for creating a new sales order.</span></span>
1. <span data-ttu-id="4b9e9-193">İletişim kutusunda aşağıdaki değerleri ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="4b9e9-193">In the dialog box, set the following values:</span></span>

    - <span data-ttu-id="4b9e9-194">**Müşteri hesabı:** *US-007*</span><span class="sxs-lookup"><span data-stu-id="4b9e9-194">**Customer account:** *US-007*</span></span>
    - <span data-ttu-id="4b9e9-195">**Ambar:** *61*</span><span class="sxs-lookup"><span data-stu-id="4b9e9-195">**Warehouse:** *61*</span></span>

1. <span data-ttu-id="4b9e9-196">Satış siparişi oluşturmak ve iletişim kutusunu kapatmak için **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="4b9e9-196">Select **OK** to create the sales order and close the dialog box.</span></span>
1. <span data-ttu-id="4b9e9-197">Yeni satış siparişi açılır.</span><span class="sxs-lookup"><span data-stu-id="4b9e9-197">The new sales order is opened.</span></span> <span data-ttu-id="4b9e9-198">**Satış siparişi satırları** hızlı sekmesinde yeni, boş bir satır bulunur.</span><span class="sxs-lookup"><span data-stu-id="4b9e9-198">It includes a new, empty line on the **Sales order lines** FastTab.</span></span> <span data-ttu-id="4b9e9-199">Bu satır için aşağıdaki değerleri ayarlayın:</span><span class="sxs-lookup"><span data-stu-id="4b9e9-199">On this line, set the following values:</span></span>

    - <span data-ttu-id="4b9e9-200">**Madde numarası:** *T0100*</span><span class="sxs-lookup"><span data-stu-id="4b9e9-200">**Item number:** *T0100*</span></span>
    - <span data-ttu-id="4b9e9-201">**Miktar:** *40*</span><span class="sxs-lookup"><span data-stu-id="4b9e9-201">**Quantity:** *40*</span></span>

1. <span data-ttu-id="4b9e9-202">**Satış siparişi satırları** hızlı sekmesinde **Stok \> Rezervasyon**'u seçin.</span><span class="sxs-lookup"><span data-stu-id="4b9e9-202">On the **Sales order lines** FastTab, select **Inventory \> Reservation**.</span></span>
1. <span data-ttu-id="4b9e9-203">**Rezervasyon** sayfasında, **Lot rezerve et** 'i seçin.</span><span class="sxs-lookup"><span data-stu-id="4b9e9-203">On the **Reservation** page, select **Reserve lot**.</span></span>
1. <span data-ttu-id="4b9e9-204">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="4b9e9-204">Close the page.</span></span>
1. <span data-ttu-id="4b9e9-205">Eylem bölmesinde, **Ambar** sekmesinde **Ambara serbest bırak**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="4b9e9-205">On the Action Pane, on the **Warehouse** tab, select **Release to warehouse**.</span></span>

    <span data-ttu-id="4b9e9-206">Ouşturulan dalga kimliğini ve sevkiyat kimliğini gösteren bilgi iletileri alırsınız.</span><span class="sxs-lookup"><span data-stu-id="4b9e9-206">You receive informational messages that show the wave and shipment IDs that were created.</span></span> <span data-ttu-id="4b9e9-207">Ayrıca bir stok yenileme dalgası da oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="4b9e9-207">A replenishment wave is also created.</span></span>

    <span data-ttu-id="4b9e9-208">"İş kimliği XXXX, bitmemiş stok yenileme işi nedeniyle engellenemez" şeklinde bir uyarı iletisi alırsınız.</span><span class="sxs-lookup"><span data-stu-id="4b9e9-208">You also receive a warning message that states, "Work ID XXXX cannot be unblocked because it has unfinished replenishment work."</span></span>

#### <a name="create-sales-order-2"></a><span data-ttu-id="4b9e9-209">Satış siparişi oluşturma 2</span><span class="sxs-lookup"><span data-stu-id="4b9e9-209">Create sales order 2</span></span>

1. <span data-ttu-id="4b9e9-210">**Tüm satış siparişleri** sayfasında, Eylem Bölmesinde, yeni satış siparişi oluşturma iletişim kutusunu açmak için **Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="4b9e9-210">On the **All sales orders**, page, on the Action Pane, select **New** to open a dialog box for creating a new sales order.</span></span>
1. <span data-ttu-id="4b9e9-211">İletişim kutusunda aşağıdaki değeri ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="4b9e9-211">In the dialog box, set the following value:</span></span>

    - <span data-ttu-id="4b9e9-212">**Müşteri hesabı:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="4b9e9-212">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="4b9e9-213">**Ambar:** *61*</span><span class="sxs-lookup"><span data-stu-id="4b9e9-213">**Warehouse:** *61*</span></span>

1. <span data-ttu-id="4b9e9-214">Satış siparişi oluşturmak ve iletişim kutusunu kapatmak için **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="4b9e9-214">Select **OK** to create the sales order and close the dialog box.</span></span>
1. <span data-ttu-id="4b9e9-215">Yeni satış siparişi açılır.</span><span class="sxs-lookup"><span data-stu-id="4b9e9-215">The new sales order is opened.</span></span> <span data-ttu-id="4b9e9-216">**Satış siparişi satırları** hızlı sekmesinde yeni, boş bir satır bulunur.</span><span class="sxs-lookup"><span data-stu-id="4b9e9-216">It includes a new, empty line on the **Sales order lines** FastTab.</span></span> <span data-ttu-id="4b9e9-217">Bu satır için aşağıdaki değerleri ayarlayın:</span><span class="sxs-lookup"><span data-stu-id="4b9e9-217">On this line, set the following values:</span></span>

    - <span data-ttu-id="4b9e9-218">**Madde numarası:** *T0100*</span><span class="sxs-lookup"><span data-stu-id="4b9e9-218">**Item number:** *T0100*</span></span>
    - <span data-ttu-id="4b9e9-219">**Miktar:** *60*</span><span class="sxs-lookup"><span data-stu-id="4b9e9-219">**Quantity:** *60*</span></span>

1. <span data-ttu-id="4b9e9-220">**Satış siparişi satırları** hızlı sekmesinde **Stok \> Rezervasyon**'u seçin.</span><span class="sxs-lookup"><span data-stu-id="4b9e9-220">On the **Sales order lines** FastTab, select **Inventory \> Reservation**.</span></span>
1. <span data-ttu-id="4b9e9-221">**Rezervasyon** sayfasında, **Lot rezerve et** 'i seçin.</span><span class="sxs-lookup"><span data-stu-id="4b9e9-221">On the **Reservation** page, select **Reserve lot**.</span></span>
1. <span data-ttu-id="4b9e9-222">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="4b9e9-222">Close the page.</span></span>
1. <span data-ttu-id="4b9e9-223">Eylem bölmesinde, **Ambar** sekmesinde **Ambara serbest bırak**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="4b9e9-223">On the Action Pane, on the **Warehouse** tab, select **Release to warehouse**.</span></span>

    <span data-ttu-id="4b9e9-224">Ouşturulan dalga kimliğini ve sevkiyat kimliğini gösteren bilgi iletileri alırsınız.</span><span class="sxs-lookup"><span data-stu-id="4b9e9-224">You receive informational messages that show the wave and shipment IDs that were created.</span></span> <span data-ttu-id="4b9e9-225">Ayrıca bir stok yenileme dalgası da oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="4b9e9-225">A replenishment wave is also created.</span></span>

    <span data-ttu-id="4b9e9-226">"İş kimliği XXXX, bitmemiş stok yenileme işi nedeniyle engellenemez" şeklinde bir uyarı iletisi alırsınız.</span><span class="sxs-lookup"><span data-stu-id="4b9e9-226">You also receive a warning message that states, "Work ID XXXX cannot be unblocked because it has unfinished replenishment work."</span></span>

#### <a name="create-sales-order-3"></a><span data-ttu-id="4b9e9-227">Satış siparişi oluşturma 3</span><span class="sxs-lookup"><span data-stu-id="4b9e9-227">Create sales order 3</span></span>

1. <span data-ttu-id="4b9e9-228">**Tüm satış siparişleri** sayfasında, Eylem Bölmesinde, yeni satış siparişi oluşturma iletişim kutusunu açmak için **Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="4b9e9-228">On the **All sales orders** page, on the Action Pane, select **New** to open a dialog box for creating a new sales order.</span></span>
1. <span data-ttu-id="4b9e9-229">İletişim kutusunda aşağıdaki değerleri ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="4b9e9-229">In the dialog box, set the following values:</span></span>

    - <span data-ttu-id="4b9e9-230">**Müşteri hesabı:** *US-004*</span><span class="sxs-lookup"><span data-stu-id="4b9e9-230">**Customer account:** *US-004*</span></span>
    - <span data-ttu-id="4b9e9-231">**Ambar:** *61*</span><span class="sxs-lookup"><span data-stu-id="4b9e9-231">**Warehouse:** *61*</span></span>

1. <span data-ttu-id="4b9e9-232">Satış siparişi oluşturmak ve iletişim kutusunu kapatmak için **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="4b9e9-232">Select **OK** to create the sales order and close the dialog box.</span></span>
1. <span data-ttu-id="4b9e9-233">Yeni satış siparişi açılır.</span><span class="sxs-lookup"><span data-stu-id="4b9e9-233">The new sales order is opened.</span></span> <span data-ttu-id="4b9e9-234">**Satış siparişi satırları** hızlı sekmesinde yeni, boş bir satır bulunur.</span><span class="sxs-lookup"><span data-stu-id="4b9e9-234">It includes a new, empty line on the **Sales order lines** FastTab.</span></span> <span data-ttu-id="4b9e9-235">Bu satır için aşağıdaki değerleri ayarlayın:</span><span class="sxs-lookup"><span data-stu-id="4b9e9-235">On this line, set the following values:</span></span>

    - <span data-ttu-id="4b9e9-236">**Madde numarası:** *T0100*</span><span class="sxs-lookup"><span data-stu-id="4b9e9-236">**Item number:** *T0100*</span></span>
    - <span data-ttu-id="4b9e9-237">**Miktar:** *30*</span><span class="sxs-lookup"><span data-stu-id="4b9e9-237">**Quantity:** *30*</span></span>

1. <span data-ttu-id="4b9e9-238">**Satış siparişi satırları** hızlı sekmesinde **Stok \> Rezervasyon**'u seçin.</span><span class="sxs-lookup"><span data-stu-id="4b9e9-238">On the **Sales order lines** FastTab, select **Inventory \> Reservation**.</span></span>
1. <span data-ttu-id="4b9e9-239">**Rezervasyon** sayfasında, **Lot rezerve et** 'i seçin.</span><span class="sxs-lookup"><span data-stu-id="4b9e9-239">On the **Reservation** page, select **Reserve lot**.</span></span>
1. <span data-ttu-id="4b9e9-240">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="4b9e9-240">Close the page.</span></span>
1. <span data-ttu-id="4b9e9-241">Eylem bölmesinde, **Ambar** sekmesinde **Ambara serbest bırak**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="4b9e9-241">On the Action Pane, on the **Warehouse** tab, select **Release to warehouse**.</span></span>

    <span data-ttu-id="4b9e9-242">Ouşturulan dalga kimliğini ve sevkiyat kimliğini gösteren bilgi iletileri alırsınız.</span><span class="sxs-lookup"><span data-stu-id="4b9e9-242">You receive informational messages that show the wave and shipment IDs that were created.</span></span> <span data-ttu-id="4b9e9-243">Ayrıca bir stok yenileme dalgası da oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="4b9e9-243">A replenishment wave is also created.</span></span>

    <span data-ttu-id="4b9e9-244">"İş kimliği XXXX, bitmemiş stok yenileme işi nedeniyle engellenemez" şeklinde bir uyarı iletisi alırsınız.</span><span class="sxs-lookup"><span data-stu-id="4b9e9-244">You also receive a warning message that states, "Work ID XXXX cannot be unblocked because it has unfinished replenishment work."</span></span>

#### <a name="view-work-details"></a><span data-ttu-id="4b9e9-245">İş ayrıntılarını görüntüleme</span><span class="sxs-lookup"><span data-stu-id="4b9e9-245">View work details</span></span>

1. <span data-ttu-id="4b9e9-246">**Ambar yönetimi \> İş \> İş ayrıntıları**'na gidin.</span><span class="sxs-lookup"><span data-stu-id="4b9e9-246">Go to **Warehouse management \> Work \> Work details**.</span></span>
1. <span data-ttu-id="4b9e9-247">**Genel Bakış** bölümünde, ambar *61* için **Ambar** sütununa filtre uygulayın.</span><span class="sxs-lookup"><span data-stu-id="4b9e9-247">In the **Overview** section, filter the **Warehouse** column for warehouse *61*.</span></span>
1. <span data-ttu-id="4b9e9-248">Üç talepli satış siparişi için yedi iş kodu oluşturulduğunu görürsünüz.</span><span class="sxs-lookup"><span data-stu-id="4b9e9-248">You should see that seven work IDs were created for the three demand sales orders.</span></span>

    - <span data-ttu-id="4b9e9-249">Yedi iş kodunun üçünde, **İş emri türü** için *Stok yenileme* değerine ve dördü ise **İş emri türü** için *Satış siparişleri* değerine sahiptir.</span><span class="sxs-lookup"><span data-stu-id="4b9e9-249">Three of the seven work IDs have a **Work order type** value of *Replenishment*, and four have a **Work order type** value of *Sales orders*.</span></span>
    - <span data-ttu-id="4b9e9-250">**İş emri türü** için *Stok yenileme* değerine sahip olan üç iş kodu, **Satırlar** bölümünde aynı *Malzeme çekme* ve *Yerine koyma* konumlarına sahiptir:</span><span class="sxs-lookup"><span data-stu-id="4b9e9-250">All three work IDs that have a **Work order type** value of *Replenishment* have the same *Pick* and *Put* locations in the **Lines** section:</span></span>

        - <span data-ttu-id="4b9e9-251">**Malzeme çekme:** *02A01R5S1B*</span><span class="sxs-lookup"><span data-stu-id="4b9e9-251">**Pick:** *02A01R5S1B*</span></span>
        - <span data-ttu-id="4b9e9-252">**Yerine koyma:** *06A01R2S1B*</span><span class="sxs-lookup"><span data-stu-id="4b9e9-252">**Put:** *06A01R2S1B*</span></span>

    - <span data-ttu-id="4b9e9-253">Satış siparişi 1 için iki iş kodu oluşturuldu.</span><span class="sxs-lookup"><span data-stu-id="4b9e9-253">Two work IDs were created for sales order 1.</span></span>

1. <span data-ttu-id="4b9e9-254">Satış siparişinin iş kodlarını not edin.</span><span class="sxs-lookup"><span data-stu-id="4b9e9-254">Make a note of the work IDs for the sales orders.</span></span>

<span data-ttu-id="4b9e9-255">Eldeki miktarlarınıza bağlı olarak, oluşturulan iş miktarları biraz farklı olabilir.</span><span class="sxs-lookup"><span data-stu-id="4b9e9-255">Depending on your on-hand quantities, the work quantities that are created might vary slightly.</span></span> <span data-ttu-id="4b9e9-256">Ancak, oluşturulan iş başlıklarının tümü bu senaryo örneği ile eşleşmelidir.</span><span class="sxs-lookup"><span data-stu-id="4b9e9-256">However, overall, the work headers that are created should match this scenario example.</span></span>

#### <a name="on-hand-inventory-license-plate-id"></a><span data-ttu-id="4b9e9-257">Eldeki stok plakası kodu</span><span class="sxs-lookup"><span data-stu-id="4b9e9-257">On-hand inventory license plate ID</span></span>

<span data-ttu-id="4b9e9-258">Bu senaryonun devamında, malzeme çekme ve stok yenileme senaryolarını tamamlamak için plakalevhasını tanımlamanız gereken ambar uygulamasını (veya bir emülatör) kullanacaksınız.</span><span class="sxs-lookup"><span data-stu-id="4b9e9-258">Later in this scenario, you will use the warehouse app (or an emulator), where you must identify the license plate to complete the picking and replenishment scenarios.</span></span>

<span data-ttu-id="4b9e9-259">Daha sonra gereksinim duyacağınız plaka kodlarını bulmak için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="4b9e9-259">To find the license plate IDs that you will need later, follow these steps.</span></span>

1. <span data-ttu-id="4b9e9-260">**Stok yönetimi \> Sorgular ve raporlar \>> Eldeki stok** öğesine gidin.</span><span class="sxs-lookup"><span data-stu-id="4b9e9-260">Go to **Inventory management \> Inquiries and reports \> On-hand list**.</span></span>
1. <span data-ttu-id="4b9e9-261">Filtre bölmesini açmak için **Filtreleri göster** düğmesini seçin.</span><span class="sxs-lookup"><span data-stu-id="4b9e9-261">Select the **Show filters** button to open the filter pane.</span></span>
1. <span data-ttu-id="4b9e9-262">Senaryo için plakaları almak üzere aşağıdaki filtre ölçütlerini girin.</span><span class="sxs-lookup"><span data-stu-id="4b9e9-262">Enter the following filtering criteria to get the license plates for the scenario.</span></span> <span data-ttu-id="4b9e9-263">*Şununla başlar* filtresini kullanın.</span><span class="sxs-lookup"><span data-stu-id="4b9e9-263">Use the *begins with* filter.</span></span>

    - <span data-ttu-id="4b9e9-264">**Madde numarası:** *T0100*</span><span class="sxs-lookup"><span data-stu-id="4b9e9-264">**Item number:** *T0100*</span></span>
    - <span data-ttu-id="4b9e9-265">**Ambar:** *61*</span><span class="sxs-lookup"><span data-stu-id="4b9e9-265">**Warehouse:** *61*</span></span>

1. <span data-ttu-id="4b9e9-266">**Uygula**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="4b9e9-266">Select **Apply**.</span></span>
1. <span data-ttu-id="4b9e9-267">Eylem Bölmesinde **Boyutlar** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="4b9e9-267">On the Action Pane, select **Dimensions**.</span></span>
1. <span data-ttu-id="4b9e9-268">**Boyutlar görünümü** iletişim kutusunda **Depolama Boyutları** bölümünde, tüm değerleri seçin.</span><span class="sxs-lookup"><span data-stu-id="4b9e9-268">In the **Dimensions display** dialog box, in the **Storage Dimensions** section, select all the values.</span></span>
1. <span data-ttu-id="4b9e9-269">**Hareketler** bölümünde, **Kalem numarası** ve **Miktar \<\> 0**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="4b9e9-269">In the **Transactions** section, select **Item number** and **Quantity \<\> 0**.</span></span>
1. <span data-ttu-id="4b9e9-270">Bitirdiğinizde iletişim kutusunu kapatmak için **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="4b9e9-270">When you've finished, select **OK** to close the dialog box.</span></span>
1. <span data-ttu-id="4b9e9-271">**Eldeki stok** kılavuzu her bir konumdaki *T0100* kalemi için plaka numaralarını gösterir.</span><span class="sxs-lookup"><span data-stu-id="4b9e9-271">The **On-hand** grid shows the license plate numbers for item *T0100* in each location.</span></span> <span data-ttu-id="4b9e9-272">Daha sonra bu bilgilere gereksinim duyacağınız için her konumdaki plakayı not edin.</span><span class="sxs-lookup"><span data-stu-id="4b9e9-272">Make a note of the license plate that is in each location, because you will need this information later.</span></span>
1. <span data-ttu-id="4b9e9-273">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="4b9e9-273">Close the page.</span></span>

### <a name="process-steps"></a><span data-ttu-id="4b9e9-274">İşlem adımları</span><span class="sxs-lookup"><span data-stu-id="4b9e9-274">Process steps</span></span>

<span data-ttu-id="4b9e9-275">İlk iki iş kodu için ambar konumu stok yenileme işlemi gerçekleştirin.</span><span class="sxs-lookup"><span data-stu-id="4b9e9-275">You will perform the warehouse location replenishment for the first two work IDs.</span></span> <span data-ttu-id="4b9e9-276">Üçüncü stok yenileme işi üzerindeki çalışma, malzeme çekme konumundaki stok düzeyi eşiğin altında oluncaya kadar engellenir.</span><span class="sxs-lookup"><span data-stu-id="4b9e9-276">Work on the third replenishment work will be blocked until the inventory level in the picking location falls below the threshold.</span></span>

#### <a name="replenishment"></a><span data-ttu-id="4b9e9-277">Stok yenileme</span><span class="sxs-lookup"><span data-stu-id="4b9e9-277">Replenishment</span></span>

1. <span data-ttu-id="4b9e9-278">Ambar uygulamasında ambar *61*'deki bir kullanıcı olarak oturum açın.</span><span class="sxs-lookup"><span data-stu-id="4b9e9-278">Sign in to the warehouse app as a user in warehouse *61*.</span></span> <span data-ttu-id="4b9e9-279">(Kullanıcı kimliği olarak *61*, parola olarak *1* girin.)</span><span class="sxs-lookup"><span data-stu-id="4b9e9-279">(Enter *61* as the user ID and *1* as the password.)</span></span>
1. <span data-ttu-id="4b9e9-280">**Stok \> Stok yenileme**'ye gidin.</span><span class="sxs-lookup"><span data-stu-id="4b9e9-280">Go to **Inventory \> Replenishment**.</span></span>

    <span data-ttu-id="4b9e9-281">İlk stok yenileme işlemini tamamlamanız istenir.</span><span class="sxs-lookup"><span data-stu-id="4b9e9-281">You're prompted to complete the first replenishment work.</span></span> <span data-ttu-id="4b9e9-282">Kalem numarası, miktar ve malzeme çekme konumu gösterilir.</span><span class="sxs-lookup"><span data-stu-id="4b9e9-282">The item number, quantity, and location to pick from are shown.</span></span>

1. <span data-ttu-id="4b9e9-283">**LP** alanına, gösterilen konumdaki kalemin plaka numarasını girin.</span><span class="sxs-lookup"><span data-stu-id="4b9e9-283">In the **LP** field, enter the license plate number for the item in the location that is shown.</span></span>
1. <span data-ttu-id="4b9e9-284">**Tamam** düğmesini (onay işareti sembolü) seçin.</span><span class="sxs-lookup"><span data-stu-id="4b9e9-284">Select the **OK** button (check mark symbol).</span></span>

    <span data-ttu-id="4b9e9-285">Sistem, çekilen kalemin yeni plakaso için bir hedef plaka numarası oluşturur.</span><span class="sxs-lookup"><span data-stu-id="4b9e9-285">The system generates a target license plate number for the new license plate for the picked item.</span></span>

1. <span data-ttu-id="4b9e9-286">Değeri onaylamak için **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="4b9e9-286">Select **OK** to confirm the value.</span></span>

    <span data-ttu-id="4b9e9-287">Kullanıcıya hedef plakayı stok yenileme konumuna koymasını bildiren yerine koyma işi gösterilir.</span><span class="sxs-lookup"><span data-stu-id="4b9e9-287">Put work is shown that instructs the user to put the target license plate into the replenishment location.</span></span> <span data-ttu-id="4b9e9-288">*Yerine koyma* konumu **06A01R2S1B** olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="4b9e9-288">The *Put* location should be **06A01R2S1B**.</span></span>

1. <span data-ttu-id="4b9e9-289">Yerine koyma ayrıntılarını onaylayın ve **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="4b9e9-289">Confirm the put details, and select **OK**.</span></span>

    <span data-ttu-id="4b9e9-290">"İş Tamamlandı" iletisi alırsınız ve sonraki stok yenileme malzeme çekme görevinin ayrıntıları gösterilir: kalem numarası, miktar ve malzeme çekilecek konum.</span><span class="sxs-lookup"><span data-stu-id="4b9e9-290">You receive a "Work Completed" message, and the details of the next replenishment pick task are shown: the item number, quantity, and location to pick from.</span></span> <span data-ttu-id="4b9e9-291">Malzeme çekme konumu ilk stok yenileme konumuyla aynı olacaktır.</span><span class="sxs-lookup"><span data-stu-id="4b9e9-291">The picking location will be the same as the first replenishment location.</span></span> <span data-ttu-id="4b9e9-292">Bu nedenle, plaka ilk stok yenileme işi görevi için kullanılan plakayla aynı koda sahip olacaktır.</span><span class="sxs-lookup"><span data-stu-id="4b9e9-292">Therefore, the license plate will have the same license plate ID that was used for the first replenishment work task.</span></span>

1. <span data-ttu-id="4b9e9-293">İkinci iş göreviyle ilgili stok yenileme işini tamamlamak için önceki adımları yineleyin.</span><span class="sxs-lookup"><span data-stu-id="4b9e9-293">Repeat the preceding steps to complete the replenishment work for the second work task.</span></span> <span data-ttu-id="4b9e9-294">Miktar ve hedef plaka, ilk iş göreviyle ilgili miktar ve hedef plakadan farklı olacaktır.</span><span class="sxs-lookup"><span data-stu-id="4b9e9-294">The quantity and target license plate will differ from the quantity and target license plate for the first work task.</span></span>

<span data-ttu-id="4b9e9-295">İkinci stok yenileme işi tamamlandıktan sonra, "İş Tamamlandı" iletisi alırsınız.</span><span class="sxs-lookup"><span data-stu-id="4b9e9-295">After the second replenishment work is completed, you receive a "Work Completed" message.</span></span> <span data-ttu-id="4b9e9-296">Mobil cihaz da bazı stok yenileme işleri kalsa bile, kullanılabilir iş olmadığını bildirir.</span><span class="sxs-lookup"><span data-stu-id="4b9e9-296">The mobile device also informs you that there is no work available, even though some replenishment work remains.</span></span> <span data-ttu-id="4b9e9-297">Bu davranış, stok yenileme işinin kullanılabilirlik durumunun *Bekletiliyor* olması nedeniyle oluşur ve bu nedenle **Engellendi** olarak işaretlenir.</span><span class="sxs-lookup"><span data-stu-id="4b9e9-297">This behavior occurs because the replenishment work has an availability status of *Held* and is therefore marked as **Blocked**.</span></span>

<span data-ttu-id="4b9e9-298">İşin atandığı malzeme çekme konumunun konum profilinin **Taşma miktarı** değeri *0,65 PL* olduğu için *Bekletiliyor* durumu tetiklenmiştir.</span><span class="sxs-lookup"><span data-stu-id="4b9e9-298">The *Held* status was triggered because the location profile for the picking location that the work is being assigned to has an **Overflow quantity** value of *0.65 PL*.</span></span> <span data-ttu-id="4b9e9-299">Önceki iki stok yenileme işi görevi, konumu *T0100* kalemi için neredeyse taşma sınırına kadar doldurmuştur.</span><span class="sxs-lookup"><span data-stu-id="4b9e9-299">The two previous replenishment work tasks filled the location almost to its overflow limit for item *T0100*.</span></span> <span data-ttu-id="4b9e9-300">(Kalemin birim dönüştürmesi *1 PL = 100 beher* şeklindedir.) Bu nedenle, kalan stok yenileme işi, konumun taşma sınırını aşmasına neden olur.</span><span class="sxs-lookup"><span data-stu-id="4b9e9-300">(The unit conversion for the item is *1 PL = 100 ea*.) Therefore, the remaining replenishment work would cause the location to exceed its overflow limit.</span></span>

<span data-ttu-id="4b9e9-301">Konumdan yeterince stok çekilene kadar mobil cihaz menü öğesindeki iş serbest bırakma eşiğinin altına getirmek için bu stok yenileme işi engellenmiş olarak kalır.</span><span class="sxs-lookup"><span data-stu-id="4b9e9-301">Until enough inventory is picked from the location to bring it below the work release threshold on the mobile device menu item, this replenishment work will remain blocked.</span></span>

#### <a name="sales-order-pick"></a><span data-ttu-id="4b9e9-302">Satış siparişi çekme</span><span class="sxs-lookup"><span data-stu-id="4b9e9-302">Sales order pick</span></span>

<span data-ttu-id="4b9e9-303">Kalan stok yenileme görevinin tamamlanabilmesi için önce, malzeme çekme konumunda stokun kalan stok yenileme işini engellemeyecek bir düzeyde olması gerekir.</span><span class="sxs-lookup"><span data-stu-id="4b9e9-303">Before the remaining replenishment work task can be completed, the picking location must be depleted of inventory to a level where the remaining replenishment work can be unblocked.</span></span> <span data-ttu-id="4b9e9-304">Başka bir deyişle,konumdaki eldeki stok miktarının ve stok yenileme miktarının toplamı, **Taşma miktarı** değerini aşamaz.</span><span class="sxs-lookup"><span data-stu-id="4b9e9-304">In other words, the sum of the quantity of on-hand inventory in the location and the replenishment quantity can't exceed the **Overflow quantity** value.</span></span> <span data-ttu-id="4b9e9-305">Bu toplam, taşma miktarından az olduğunda, kalan stok yenileme işinin engeli kaldırılır.</span><span class="sxs-lookup"><span data-stu-id="4b9e9-305">When this sum is less than the overflow quantity, the remaining replenishment work will be unblocked.</span></span>

1. <span data-ttu-id="4b9e9-306">Ambar uygulamasında ambar *61*'deki bir kullanıcı olarak oturum açın.</span><span class="sxs-lookup"><span data-stu-id="4b9e9-306">Sign in to the warehouse app as a user in warehouse *61*.</span></span> <span data-ttu-id="4b9e9-307">(Kullanıcı kimliği olarak *61*, parola olarak *1* girin.)</span><span class="sxs-lookup"><span data-stu-id="4b9e9-307">(Enter *61* as the user ID and *1* as the password.)</span></span>
1. <span data-ttu-id="4b9e9-308">**Giden \> Satış çekme**'ye gidin.</span><span class="sxs-lookup"><span data-stu-id="4b9e9-308">Go to **Outbound \> Sales Picking**.</span></span>
1. <span data-ttu-id="4b9e9-309">Satış siparişi 1'in ilk iş kodunu girin.</span><span class="sxs-lookup"><span data-stu-id="4b9e9-309">Enter the first work ID for sales order 1.</span></span>

    <span data-ttu-id="4b9e9-310">Daha önce **İş ayrıntıları** sayfasında not ettiğiniz satış siparişleri iş kodlarına bakın.</span><span class="sxs-lookup"><span data-stu-id="4b9e9-310">Refer to the work IDs for sales orders that you made a note of earlier, on the **Work details** page.</span></span> <span data-ttu-id="4b9e9-311">Buraya gireceğiniz iş kodu, iki ayrı konumdan 10 beher miktarında malzeme çekme işi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="4b9e9-311">The work ID that you enter here will generate pick work for a quantity of 10 ea from two separate locations.</span></span>

1. <span data-ttu-id="4b9e9-312">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="4b9e9-312">Select **OK**.</span></span>

    <span data-ttu-id="4b9e9-313">**Satış siparişleri: Malzeme çekme** görevi sayfası, ilk konum için kalem numarası, miktar ve malzeme çekilecek konumu gösterir.</span><span class="sxs-lookup"><span data-stu-id="4b9e9-313">The **Sales orders: Pick** task page shows the item number, quantity, and location to pick from for the first location.</span></span>

1. <span data-ttu-id="4b9e9-314">**LP** alanına, gösterilen konumdaki kalemin plaka numarasını girin.</span><span class="sxs-lookup"><span data-stu-id="4b9e9-314">In the **LP** field, enter the license plate number for the item in the location that is shown.</span></span>
1. <span data-ttu-id="4b9e9-315">**Tamam** düğmesini (onay işareti sembolü) seçin.</span><span class="sxs-lookup"><span data-stu-id="4b9e9-315">Select the **OK** button (check mark symbol).</span></span>

    <span data-ttu-id="4b9e9-316">**Satış siparişleri: Malzeme çekme** görevi sayfası, sonraki konum için kalem numarası, miktar ve malzeme çekilecek konumu gösterir.</span><span class="sxs-lookup"><span data-stu-id="4b9e9-316">The **Sales orders: Pick** task page shows the item number, quantity, and location to pick from for the next location.</span></span>

1. <span data-ttu-id="4b9e9-317">**LP** alanına, gösterilen konumdaki kalemin plaka numarasını girin.</span><span class="sxs-lookup"><span data-stu-id="4b9e9-317">In the **LP** field, enter the license plate number for the item in the location that is shown.</span></span>
1. <span data-ttu-id="4b9e9-318">**Tamam** düğmesini (onay işareti sembolü) seçin.</span><span class="sxs-lookup"><span data-stu-id="4b9e9-318">Select the **OK** button (check mark symbol).</span></span>

    <span data-ttu-id="4b9e9-319">**Satış siparişleri: Yerine koyma** sayfasında, tamamlanan her iki işi giden hazırlama konumuna yerine koymanız istenir.</span><span class="sxs-lookup"><span data-stu-id="4b9e9-319">The **Sales orders: Put** page instructs you to put away both the completed picking works to the outbound staging location.</span></span>

1. <span data-ttu-id="4b9e9-320">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="4b9e9-320">Select **OK**.</span></span>

    <span data-ttu-id="4b9e9-321">Bir "İş Tamamlandı" iletisi alırsınız.</span><span class="sxs-lookup"><span data-stu-id="4b9e9-321">You receive a "Work Completed" message.</span></span>

1. <span data-ttu-id="4b9e9-322">Satış siparişi 1'in ikinci iş kodunu girin.</span><span class="sxs-lookup"><span data-stu-id="4b9e9-322">Enter the second work ID for sales order 1.</span></span>

    <span data-ttu-id="4b9e9-323">Bu iş kodu için yalnızca bir malzeme çekme görevi vardır.</span><span class="sxs-lookup"><span data-stu-id="4b9e9-323">There is only one pick task for this work ID.</span></span>

1. <span data-ttu-id="4b9e9-324">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="4b9e9-324">Select **OK**.</span></span>

    <span data-ttu-id="4b9e9-325">**Satış siparişleri: Malzeme çekme** görevi sayfası, kalem numarası, miktar ve malzeme çekilecek konumu gösterir.</span><span class="sxs-lookup"><span data-stu-id="4b9e9-325">The **Sales orders: Pick** task page shows the item number, quantity, and location to pick from.</span></span>

1. <span data-ttu-id="4b9e9-326">**LP** alanına, gösterilen konumdaki kalemin plaka numarasını girin.</span><span class="sxs-lookup"><span data-stu-id="4b9e9-326">In the **LP** field, enter the license plate number for the item in the location that is shown.</span></span>

    <span data-ttu-id="4b9e9-327">Belirttiğiniz plaka, stok yenileme işi görevlerinden alınan sistem tarafından oluşturulan plakalardan biridir.</span><span class="sxs-lookup"><span data-stu-id="4b9e9-327">The license plate that you specify will be one of the system-generated license plates from the replenishment work tasks.</span></span> <span data-ttu-id="4b9e9-328">Doğru plaka kodunu aldığınızdan emin olmak için kalem, konum ve miktar açısından **Eldeki stok listesi** sayfasındaki stoku kontrol edin.</span><span class="sxs-lookup"><span data-stu-id="4b9e9-328">To make sure that you capture the correct license plate ID, check the inventory on the **On-hand list** page for the item, location, and quantity.</span></span>

1. <span data-ttu-id="4b9e9-329">**Tamam** düğmesini (onay işareti sembolü) seçin.</span><span class="sxs-lookup"><span data-stu-id="4b9e9-329">Select the **OK** button (check mark symbol).</span></span>
1. <span data-ttu-id="4b9e9-330">Giden hazırlama konumunda yerine koyma görevi yönergelerini onaylayın.</span><span class="sxs-lookup"><span data-stu-id="4b9e9-330">Confirm the instructions for the put task to the outbound staging location.</span></span>
1. <span data-ttu-id="4b9e9-331">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="4b9e9-331">Select **OK**.</span></span>

    <span data-ttu-id="4b9e9-332">Bir "İş Tamamlandı" iletisi alırsınız.</span><span class="sxs-lookup"><span data-stu-id="4b9e9-332">You receive a "Work Completed" message.</span></span>

<span data-ttu-id="4b9e9-333">Bağlantılı olduğu stok yenileme görevi tamamlanmadığı için satış siparişi 2, malzeme çekmeye karşı engellenmiştir.</span><span class="sxs-lookup"><span data-stu-id="4b9e9-333">Sales order 2 is blocked from picking because the replenishment task that it's linked to isn't completed.</span></span> <span data-ttu-id="4b9e9-334">Şu anda malzeme çekme konumunda hala 30 beher miktarı bulunmaktadır ve satış siparişi 2 için stok yenileme miktarı 60 beherdir.</span><span class="sxs-lookup"><span data-stu-id="4b9e9-334">Currently, there is still a quantity of 30 ea in the picking location, and the replenishment quantity for sales order 2 is 60 ea.</span></span> <span data-ttu-id="4b9e9-335">Eldeki stok ve stok yenileme stoku toplamı (90 beher), 0,65 PL (veya 65 beher) olan taşma miktarını aşıyor.</span><span class="sxs-lookup"><span data-stu-id="4b9e9-335">The sum of the on-hand inventory and the replenishment inventory (90 ea) exceeds the overflow quantity of 0.65 PL (or 65 ea).</span></span> <span data-ttu-id="4b9e9-336">Stok yenileme işinin tamamlanabilmesi için önce satış siparişi 3'ün çekilmesi gerekir.</span><span class="sxs-lookup"><span data-stu-id="4b9e9-336">Before the replenishment work can be completed, sales order 3 must be picked.</span></span>

1. <span data-ttu-id="4b9e9-337">Satış siparişi 3'ün iş kodunu girin.</span><span class="sxs-lookup"><span data-stu-id="4b9e9-337">Enter the work ID for sales order 3.</span></span>

    <span data-ttu-id="4b9e9-338">Bu iş kodu için yalnızca bir malzeme çekme görevi vardır.</span><span class="sxs-lookup"><span data-stu-id="4b9e9-338">There is only one pick task for this work ID.</span></span>

1. <span data-ttu-id="4b9e9-339">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="4b9e9-339">Select **OK**.</span></span>

    <span data-ttu-id="4b9e9-340">**Satış siparişleri: Malzeme çekme** görevi sayfası, kalem numarası, miktar ve malzeme çekilecek konumu gösterir.</span><span class="sxs-lookup"><span data-stu-id="4b9e9-340">The **Sales orders: Pick** task page shows the item number, quantity, and location to pick from.</span></span>

1. <span data-ttu-id="4b9e9-341">**LP** alanına, gösterilen konumdaki kalemin plaka numarasını girin.</span><span class="sxs-lookup"><span data-stu-id="4b9e9-341">In the **LP** field, enter the license plate number for the item in the location that is shown.</span></span>

    <span data-ttu-id="4b9e9-342">Belirttiğiniz plaka, stok yenileme işi görevlerinden alınan sistem tarafından oluşturulan plakalardan biridir.</span><span class="sxs-lookup"><span data-stu-id="4b9e9-342">The license plate that you specify will be one of the system-generated license plates from the replenishment work tasks.</span></span> <span data-ttu-id="4b9e9-343">Doğru plaka kodunu aldığınızdan emin olmak için kalem, konum ve miktar açısından **Eldeki stok listesi** sayfasındaki stoku kontrol edin.</span><span class="sxs-lookup"><span data-stu-id="4b9e9-343">To make sure that you capture the correct license plate ID, check the inventory on the **On-hand list** page for the item, location, and quantity.</span></span>

1. <span data-ttu-id="4b9e9-344">**Tamam** düğmesini (onay işareti sembolü) seçin.</span><span class="sxs-lookup"><span data-stu-id="4b9e9-344">Select the **OK** button (check mark symbol).</span></span>
1. <span data-ttu-id="4b9e9-345">Giden hazırlama konumunda yerine koyma görevi yönergelerini onaylayın.</span><span class="sxs-lookup"><span data-stu-id="4b9e9-345">Confirm the instructions for the put task to the outbound staging location.</span></span>
1. <span data-ttu-id="4b9e9-346">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="4b9e9-346">Select **OK**.</span></span>

    <span data-ttu-id="4b9e9-347">Bir "İş Tamamlandı" iletisi alırsınız.</span><span class="sxs-lookup"><span data-stu-id="4b9e9-347">You receive a "Work Completed" message.</span></span>

<span data-ttu-id="4b9e9-348">Malzeme çekme konumundaki eldeki stok miktarı ve stok yenileme miktarının toplamı eşiğin altında olduğunda, kalan stok yenileme işini işleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="4b9e9-348">As soon as the sum of the on-hand quantity in the picking location and the replenishment quantity is below the threshold, you will be able to process the remaining replenishment work.</span></span>

<span data-ttu-id="4b9e9-349">**İş ayrıntıları** sayfasına geri dönün ve konumda stok yenilemeyi kabul edecek kadar yeterli alan olmadığından nihai stok yenileme kısmının (satış siparişi 2 için) stok yenileme işi kullanılabilirliğinin *Açık* olduğuna dikkat edin.</span><span class="sxs-lookup"><span data-stu-id="4b9e9-349">Return to the **Work details** page, and notice that the replenishment work availability for the final piece of replenishment (for sales order 2) is *Open*, because there is now enough space in the location to accept the replenishment.</span></span>

<span data-ttu-id="4b9e9-350">Şimdi mobil cihaz üzerinden bu stok yenileme işini işleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="4b9e9-350">You can now process this replenishment work via the mobile device.</span></span>

1. <span data-ttu-id="4b9e9-351">**Stok \> Stok yenileme**'ye gidin.</span><span class="sxs-lookup"><span data-stu-id="4b9e9-351">Go to **Inventory \> Replenishment**.</span></span>

    <span data-ttu-id="4b9e9-352">Kalan stok yenileme işlemini tamamlamanız istenir.</span><span class="sxs-lookup"><span data-stu-id="4b9e9-352">You're prompted to complete the remaining replenishment work.</span></span> <span data-ttu-id="4b9e9-353">Kalem numarası, miktar ve malzeme çekme konumu gösterilir.</span><span class="sxs-lookup"><span data-stu-id="4b9e9-353">The item number, quantity, and location to pick from are shown.</span></span>

1. <span data-ttu-id="4b9e9-354">**LP** alanına, gösterilen konumdaki kalemin plaka numarasını girin.</span><span class="sxs-lookup"><span data-stu-id="4b9e9-354">In the **LP** field, enter the license plate number for the item in the location that is shown.</span></span>
1. <span data-ttu-id="4b9e9-355">**Tamam** düğmesini (onay işareti sembolü) seçin.</span><span class="sxs-lookup"><span data-stu-id="4b9e9-355">Select the **OK** button (check mark symbol).</span></span>

    <span data-ttu-id="4b9e9-356">Sistem, çekilen kalemin yeni plakaso için bir hedef plaka numarası oluşturur.</span><span class="sxs-lookup"><span data-stu-id="4b9e9-356">The system generates a target license plate number for the new license plate for the picked item.</span></span>

1. <span data-ttu-id="4b9e9-357">Değeri onaylamak için **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="4b9e9-357">Select **OK** to confirm the value.</span></span>

    <span data-ttu-id="4b9e9-358">Kullanıcıya hedef plakayı stok yenileme konumuna koymasını bildiren yerine koyma işi gösterilir.</span><span class="sxs-lookup"><span data-stu-id="4b9e9-358">Put work is shown that instructs the user to put the target license plate into the replenishment location.</span></span> <span data-ttu-id="4b9e9-359">*Yerine koyma* konumu **06A01R2S1B** olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="4b9e9-359">The *Put* location should be **06A01R2S1B**.</span></span>

1. <span data-ttu-id="4b9e9-360">Yerine koyma ayrıntılarını onaylayın ve **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="4b9e9-360">Confirm the put details, and select **OK**.</span></span>

    <span data-ttu-id="4b9e9-361">"İş Tamamlandı" ve "Kullanılabilir İş Yok" iletilerini alırsınız.</span><span class="sxs-lookup"><span data-stu-id="4b9e9-361">You receive "Work Completed" and "No Work Available" messages.</span></span>

<span data-ttu-id="4b9e9-362">Şimdi satış siparişi 2'yi çekebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="4b9e9-362">You can now pick sales order 2.</span></span> <span data-ttu-id="4b9e9-363">Satış siparişiyle bağlantılı stok yenileme işi tamamlandığında, engeli kaldırılmıştır.</span><span class="sxs-lookup"><span data-stu-id="4b9e9-363">It became unblocked when the replenishment work that is linked to the sales order was completed.</span></span>

1. <span data-ttu-id="4b9e9-364">Satış siparişi 2'nin iş kodunu girin.</span><span class="sxs-lookup"><span data-stu-id="4b9e9-364">Enter the work ID for sales order 2.</span></span>

    <span data-ttu-id="4b9e9-365">Bu iş kodu için yalnızca bir malzeme çekme görevi vardır.</span><span class="sxs-lookup"><span data-stu-id="4b9e9-365">There is only one pick task for this work ID.</span></span>

1. <span data-ttu-id="4b9e9-366">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="4b9e9-366">Select **OK**.</span></span>

    <span data-ttu-id="4b9e9-367">**Satış siparişleri: Malzeme çekme** görevi sayfası, kalem numarası, miktar ve malzeme çekilecek konumu gösterir.</span><span class="sxs-lookup"><span data-stu-id="4b9e9-367">The **Sales orders: Pick** task page shows the item number, quantity, and location to pick from.</span></span>

1. <span data-ttu-id="4b9e9-368">**LP** alanına, gösterilen konumdaki kalemin plaka numarasını girin.</span><span class="sxs-lookup"><span data-stu-id="4b9e9-368">In the **LP** field, enter the license plate number for the item in the location that is shown.</span></span>

    <span data-ttu-id="4b9e9-369">Belirttiğiniz plaka, stok yenileme işi görevinden alınan sistem tarafından oluşturulan bir plakadır.</span><span class="sxs-lookup"><span data-stu-id="4b9e9-369">The license plate that you specify will be the system-generated license plate from the replenishment work task.</span></span> <span data-ttu-id="4b9e9-370">Doğru plaka kodunu aldığınızdan emin olmak için kalem, konum ve miktar açısından **Eldeki stok listesi** sayfasındaki stoku kontrol edin.</span><span class="sxs-lookup"><span data-stu-id="4b9e9-370">To make sure that you capture the correct license plate ID, check the inventory on the **On-hand list** page for the item, location, and quantity.</span></span>

1. <span data-ttu-id="4b9e9-371">**Tamam** düğmesini (onay işareti sembolü) seçin.</span><span class="sxs-lookup"><span data-stu-id="4b9e9-371">Select the **OK** button (check mark symbol).</span></span>
1. <span data-ttu-id="4b9e9-372">Giden hazırlama konumunda yerine koyma görevi yönergelerini onaylayın.</span><span class="sxs-lookup"><span data-stu-id="4b9e9-372">Confirm the instructions for the put task to the outbound staging location.</span></span>
1. <span data-ttu-id="4b9e9-373">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="4b9e9-373">Select **OK**.</span></span>

    <span data-ttu-id="4b9e9-374">Bir "İş Tamamlandı" iletisi alırsınız.</span><span class="sxs-lookup"><span data-stu-id="4b9e9-374">You receive a "Work Completed" message.</span></span>

## <a name="notes-and-tips"></a><span data-ttu-id="4b9e9-375">Notlar ve ipuçları</span><span class="sxs-lookup"><span data-stu-id="4b9e9-375">Notes and tips</span></span>

- <span data-ttu-id="4b9e9-376">Bu işlev, tüm stok yenileme türleriyle çalışır: dalga talebi, minimum/maksimum, yükleme talebi ve eğri yerleştirme.</span><span class="sxs-lookup"><span data-stu-id="4b9e9-376">This functionality works with all types of replenishment: wave demand, min/max, load demand, and slotting.</span></span>
- <span data-ttu-id="4b9e9-377">Dilerseniz **İş ayrıntıları** sayfasından, her iş başlığı için stok yenileme işi kullanılabilirliğini el ile geçersiz kılabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="4b9e9-377">You can manually override the replenishment work availability for each work header from the **Work details** page if you want.</span></span>
- <span data-ttu-id="4b9e9-378">Sistem stok yenileme işi kullanılabilirliğini ayarladığında, herhangi bir iş tamamlanmadan önce o konumda olan tüm stoku dikkate alır</span><span class="sxs-lookup"><span data-stu-id="4b9e9-378">When the system sets the replenishment work availability, it considers any inventory that is already in the location before any work is completed</span></span>
- <span data-ttu-id="4b9e9-379">Satış siparişi işinin her parçası belirli bir stok yenileme işine bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="4b9e9-379">Each piece of sales order work is linked to a specific replenishment work.</span></span> <span data-ttu-id="4b9e9-380">Karşılık gelen satış işi kullanılabilirlik işlevi yoktur.</span><span class="sxs-lookup"><span data-stu-id="4b9e9-380">There is no corresponding sales work availability functionality.</span></span>
