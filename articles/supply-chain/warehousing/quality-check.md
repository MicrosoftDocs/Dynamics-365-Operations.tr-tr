---
title: Kalite denetimi
description: Bu konuda, Kalite denetimi özelliğiyle ilgili bilgiler verilir. Bu özellik, ambar çalışanlarının kalemleri giriş noktası alanına alırken kalite açısından hızlı bir şekilde denetlemesine olanak tanır.
author: mirzaab
manager: tfehr
ms.date: 07/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSQualityCheckTemplate, WHSWorkClass, WHSWorkTemplateTable, WHSLocDirTable, WHSQualityCheckResult
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-16
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 585ca933726cb932290f8abf8504aeb13848a0e5
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/15/2021
ms.locfileid: "4996266"
---
# <a name="quality-check"></a><span data-ttu-id="99697-104">Kalite denetimi</span><span class="sxs-lookup"><span data-stu-id="99697-104">Quality check</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="99697-105">*Kalite denetimi* özelliği, ambar çalışanlarının kalemleri giriş noktası alanına alırken kalite açısından hızlı bir şekilde denetlemesine olanak tanır.</span><span class="sxs-lookup"><span data-stu-id="99697-105">The *Quality check* feature lets warehouse workers do quick spot checks for quality while they receive items to the inbound dock area.</span></span> <span data-ttu-id="99697-106">Bu rastgele denetimler, çalışanlar ambalajı veya bir öğenin kolayca tanınabilen bölümlerini denetlediğinde yararlıdır.</span><span class="sxs-lookup"><span data-stu-id="99697-106">These spot checks are beneficial when workers inspect packaging or other easily recognizable parts of an item.</span></span> <span data-ttu-id="99697-107">Özellik, çalışanların stoku yerine koyma konumuna yerleştirmeden önce hatalı veya hasarlı olup olmadığını görmesini sağlamak amacıyla hızlı bir şekilde kontrol etmesini sağlar.</span><span class="sxs-lookup"><span data-stu-id="99697-107">The feature guides workers to take a quick look to see whether anything is obviously faulty or damaged before they stock the inventory in its putaway location.</span></span>

<span data-ttu-id="99697-108">Bu özellik standart kalite denetimi işleminin bir alternatifidir.</span><span class="sxs-lookup"><span data-stu-id="99697-108">This feature is an alternative to the standard quality check process.</span></span> <span data-ttu-id="99697-109">Daha fazla esneklik ve daha hızlı işlem sunar.</span><span class="sxs-lookup"><span data-stu-id="99697-109">It offers more flexibility and faster processing.</span></span>

<span data-ttu-id="99697-110">Bu özelliği kullandığınızda, varış ve kalite denetimi aşağıdaki şekilde gerçekleştirilir:</span><span class="sxs-lookup"><span data-stu-id="99697-110">When you use this feature, the arrival and quality check occur in the following way:</span></span>

1. <span data-ttu-id="99697-111">Bir sevkiyat geldiğinde, bir ambar çalışanı varış kaydını yapar.</span><span class="sxs-lookup"><span data-stu-id="99697-111">When a shipment arrives, a warehouse worker registers the arrival.</span></span> <span data-ttu-id="99697-112">Çalışan aynı zamanda, konumu kaydetmek için plakayı tarar.</span><span class="sxs-lookup"><span data-stu-id="99697-112">The worker also scans a license plate to register the location.</span></span>
1. <span data-ttu-id="99697-113">Çalışan hızlı bir kalite denetimi yapar ve bu plaka için sonuçları (başarılı veya başarısız) kaydeder.</span><span class="sxs-lookup"><span data-stu-id="99697-113">The worker does a quick quality check and records the result (pass or fail) for that license plate.</span></span>
1. <span data-ttu-id="99697-114">Aşağıdaki eylemlerden biri gerçekleşir:</span><span class="sxs-lookup"><span data-stu-id="99697-114">One of the following actions occurs:</span></span>

    - <span data-ttu-id="99697-115">Plaka kalite denetiminden geçerse kabul edilir ve her zamanki gibi bir teslim alma konumuna yönlendirilir.</span><span class="sxs-lookup"><span data-stu-id="99697-115">If the quality check is passed, the license plate is accepted and guided to a receiving location, as usual.</span></span>
    - <span data-ttu-id="99697-116">Kalite denetimi başarısız olursa, plaka reddedilir ve bu plaka için varolan yerine koyma işi, daha fazla inceleme için alternatif bir konuma yönlendirilir.</span><span class="sxs-lookup"><span data-stu-id="99697-116">If the quality check is failed, the license plate is rejected, and existing putaway work for it is redirected to an alternate location for further inspection.</span></span> <span data-ttu-id="99697-117">Yeni bir kalite emri oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="99697-117">A new quality order is created.</span></span> <span data-ttu-id="99697-118">Başarısız olan kalite denetiminden oluşturulan kalite emrini görüntülemek için **Stok Yönetimi \> Periyodik görevler \> Kalite yönetimi \> Kalite emirleri**'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="99697-118">To view the quality order that is created from the failed quality check, go to **Inventory management \> Periodic tasks \> Quality management \> Quality orders**.</span></span>

<span data-ttu-id="99697-119">Bu işlem, taranan tüm plakaların hemen kalite denetimi konumuna yönlendirilmesi için de ayarlanabilir.</span><span class="sxs-lookup"><span data-stu-id="99697-119">This process can also be set up so that all scanned license plates are immediately diverted to the quality check location.</span></span>

## <a name="turn-on-the-quality-check-feature"></a><span data-ttu-id="99697-120">Kalite denetimi özelliğini açma</span><span class="sxs-lookup"><span data-stu-id="99697-120">Turn on the Quality check feature</span></span>

<span data-ttu-id="99697-121">*Kalite denetimi* özelliğini kullanabilmeniz için sisteminizde etkinleştirmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="99697-121">Before you can use the *Quality check* feature, it must be turned on in your system.</span></span> <span data-ttu-id="99697-122">Yöneticiler özellik durumunu denetlemek ve gerekirse etkinleştirmek için [özellik yönetimi](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) ayarlarını kullanabilir.</span><span class="sxs-lookup"><span data-stu-id="99697-122">Admins can use the [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) settings to check the status of the feature and turn it on if it's required.</span></span> <span data-ttu-id="99697-123">**Özellik yönetimi** çalışma alanındabu özellik aşağıdaki şekilde listelenir:</span><span class="sxs-lookup"><span data-stu-id="99697-123">In the **Feature management** workspace, the feature is listed in the following way:</span></span>

- <span data-ttu-id="99697-124">**Modül:** *Ambar yönetimi*</span><span class="sxs-lookup"><span data-stu-id="99697-124">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="99697-125">**Özellik adı:** *Kalite denetimi*</span><span class="sxs-lookup"><span data-stu-id="99697-125">**Feature name:** *Quality check*</span></span>

## <a name="set-up-the-feature-for-the-example-scenario"></a><span data-ttu-id="99697-126">Örnek senaryo için özelliği ayarlama</span><span class="sxs-lookup"><span data-stu-id="99697-126">Set up the feature for the example scenario</span></span>

<span data-ttu-id="99697-127">Bu bölümde, *Kalite denetimi* özelliğinin nasıl ayarlanacağı ve bu konunun ilerleyen kısımlarında sağlanan örnek senaryo için örnek verilerin nasıl hazırlanacağı gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="99697-127">This section provides guidelines and an example that shows how to set up the *Quality check* feature and prepare sample data for the example scenario that is provided later in this topic.</span></span>

### <a name="make-sample-data-available"></a><span data-ttu-id="99697-128">Örnek verilerini kullanılabilir hale getirme</span><span class="sxs-lookup"><span data-stu-id="99697-128">Make sample data available</span></span>

<span data-ttu-id="99697-129">Burada belirtilen örnek kayıtları ve değerleri kullanarak [örnek senaryo](#example-scenario) üzerinden çalışmak için standart [demo verilerinin](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) yüklenmiş olduğu bir sistemde olmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="99697-129">To work through the [example scenario](#example-scenario) by using the sample records and values that are specified here, you must be on a system where the standard [demo data](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) is installed.</span></span> <span data-ttu-id="99697-130">Ek olarak, başlamadan önce **USMF** tüzel kişiliğini seçmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="99697-130">Additionally, you must select the **USMF** legal entity before you begin.</span></span>

### <a name="quality-check-template"></a><a name="quality-template"></a><span data-ttu-id="99697-131">Kalite denetimi şablonu</span><span class="sxs-lookup"><span data-stu-id="99697-131">Quality check template</span></span>

<span data-ttu-id="99697-132">Kalite denetimi şablonu, teslim alma sırasında kalite için hızlı rastgele denetim kurallarını tanımlar.</span><span class="sxs-lookup"><span data-stu-id="99697-132">The quality check template defines the rules for doing quick spot checks for quality at the time of receiving.</span></span>

1. <span data-ttu-id="99697-133">**Ambar yönetimi \> Kurulum \> İş \> Kalite denetimi şablonu**'na gidin.</span><span class="sxs-lookup"><span data-stu-id="99697-133">Go to **Warehouse management \> Setup \> Work \> Quality check template**.</span></span>
1. <span data-ttu-id="99697-134">Kılavuza şablon eklemek için **Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="99697-134">Select **New** to add a template to the grid.</span></span>
1. <span data-ttu-id="99697-135">Yeni şabonu tanımlamak için aşağıdaki değerleri ayarlayın:</span><span class="sxs-lookup"><span data-stu-id="99697-135">Set the following values to define the new template:</span></span>

    - <span data-ttu-id="99697-136">**Kalite denetim şablonu adı:** *Giriş noktası denetimi*</span><span class="sxs-lookup"><span data-stu-id="99697-136">**Quality check template name:** *Dock check*</span></span>

        <span data-ttu-id="99697-137">Bu şablon için geçerli olan ilkeleri tanımlayan bir ad girin.</span><span class="sxs-lookup"><span data-stu-id="99697-137">Enter a name that identifies the policies applied for this template.</span></span>

    - <span data-ttu-id="99697-138">**Kabul ilkesi:** *Kullanıcıya sor*</span><span class="sxs-lookup"><span data-stu-id="99697-138">**Acceptance policy:** *Prompt user*</span></span>

        <span data-ttu-id="99697-139">Kullanıcılara, işi işlerken stok kalitesini kabul etmeleri veya reddetmeleri için istemde bulunulup bulunulmayacağını ya da kalitenin otomatik reddedilip edilmeyeceğini belirtin.</span><span class="sxs-lookup"><span data-stu-id="99697-139">Specify whether users should be prompted to accept or reject the quality of the inventory while they process the work, or whether the quality should automatically be rejected.</span></span> <span data-ttu-id="99697-140">Kullanılabilir seçenekler *Otomatik olarak reddet* ve *Kullanıcıya sor* şeklindedir.</span><span class="sxs-lookup"><span data-stu-id="99697-140">The available options are *Auto reject* and *Prompt user*.</span></span>

    - <span data-ttu-id="99697-141">**Kalite işleme ilkesi:** *Kalite emri oluştur*</span><span class="sxs-lookup"><span data-stu-id="99697-141">**Quality processing policy:** *Create quality order*</span></span>

        <span data-ttu-id="99697-142">Stok kalitesini reddederken kullanılacak ilkeyi seçin.</span><span class="sxs-lookup"><span data-stu-id="99697-142">Select the policy that should be used when the quality of the inventory is rejected.</span></span> <span data-ttu-id="99697-143">Aşağıdaki seçenekler bulunur:</span><span class="sxs-lookup"><span data-stu-id="99697-143">The following options are available:</span></span>

        - <span data-ttu-id="99697-144">*Yalnızca iş oluştur* – Yalnızca stok hareketlerini kolaylaştırmak için iş oluşturun.</span><span class="sxs-lookup"><span data-stu-id="99697-144">*Create work only* – Just create work to facilitate inventory movement.</span></span>
        - <span data-ttu-id="99697-145">*Kalite emri oluştur* – Kalite testlerini kolaylaştırmak için bir kalite emri oluşturun.</span><span class="sxs-lookup"><span data-stu-id="99697-145">*Create quality order* – Create a quality order to facilitate quality tests.</span></span>

    - <span data-ttu-id="99697-146">**Test grubu:** *Kutu*</span><span class="sxs-lookup"><span data-stu-id="99697-146">**Test group:** *Enclosure*</span></span>

        <span data-ttu-id="99697-147">Oluşturulan kalite emrinde kullanılacak test grubunu belirtin.</span><span class="sxs-lookup"><span data-stu-id="99697-147">Specify the test group that should be used in the quality order that is created.</span></span> <span data-ttu-id="99697-148">Test grupları **Stok yönetimi** modülünde ayarlanır.</span><span class="sxs-lookup"><span data-stu-id="99697-148">Test groups are set up in the **Inventory management** module.</span></span>

        <span data-ttu-id="99697-149">Test grubu için **Bozma metni** seçeneğini kapalı bırakın.</span><span class="sxs-lookup"><span data-stu-id="99697-149">Leave the **Destructive text** option turned off for the test group.</span></span> <span data-ttu-id="99697-150">Bu seçenek, test grubu içindeki testler kapsamında örneklerin imha edilip edilmeyeceğini tanımlar.</span><span class="sxs-lookup"><span data-stu-id="99697-150">This option defines whether the sample will be destroyed as part of the tests in the test group.</span></span> <span data-ttu-id="99697-151">Bozucu bir test kullanılırsa bir kalem için kalite emri oluşturulduğunda sistem bir stok hareketi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="99697-151">If a destructive test is used, the system generates an inventory transaction when a quality order is created for an item.</span></span> <span data-ttu-id="99697-152">Yeni stok hareketi test miktar için stok azaltması öngörür.</span><span class="sxs-lookup"><span data-stu-id="99697-152">The new inventory transaction predicts the inventory reduction for the test quantity.</span></span> <span data-ttu-id="99697-153">Kalite emri doğrulama adımı yoluyla tamamlandığında stok azaltma işlemi gerçekleşir.</span><span class="sxs-lookup"><span data-stu-id="99697-153">The inventory reduction occurs when the quality order is completed through the validation step.</span></span> <span data-ttu-id="99697-154">Stok hareketi kalite emri olarak tanımlanır.</span><span class="sxs-lookup"><span data-stu-id="99697-154">The inventory transaction is identified as a quality order.</span></span>

### <a name="work-class--quality-check"></a><a name="work-class"></a><span data-ttu-id="99697-155">İş sınıfı – Kalite denetimi</span><span class="sxs-lookup"><span data-stu-id="99697-155">Work class – Quality check</span></span>

<span data-ttu-id="99697-156">İş sınıfları, ambar çalışanları tarafından bir mobil cihazda işlenebilecek iş emri satırlarının türünü yönetmek ve/veya sınırlamak için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="99697-156">Work classes are used to direct and/or limit the type of work order lines that warehouse workers can process on a mobile device.</span></span>

1. <span data-ttu-id="99697-157">**Ambar yönetimi \> Kurulum \> İş \> İş sınıfları** seçeneğine gidin.</span><span class="sxs-lookup"><span data-stu-id="99697-157">Go to **Warehouse management \> Setup \> Work \> Work classes**.</span></span>
1. <span data-ttu-id="99697-158">Yeni iş sınıfı oluşturmak için **Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="99697-158">Select **New** to create a work class.</span></span>
1. <span data-ttu-id="99697-159">Üst bilgide aşağıdaki değerleri ayarlayın:</span><span class="sxs-lookup"><span data-stu-id="99697-159">In the header, set the following values:</span></span>

    - <span data-ttu-id="99697-160">**İş sınıfı kodu:** *QC Check*</span><span class="sxs-lookup"><span data-stu-id="99697-160">**Work class ID:** *QC Check*</span></span>

        <span data-ttu-id="99697-161">İş sınıfını tanımlayan bir ad girin.</span><span class="sxs-lookup"><span data-stu-id="99697-161">Enter a name that identifies the work class.</span></span>

    - <span data-ttu-id="99697-162">**Açıklama:** *QC Check*</span><span class="sxs-lookup"><span data-stu-id="99697-162">**Description:** *QC Check*</span></span>

        <span data-ttu-id="99697-163">İş sınıfının ne için kullanıldığını gösteren kısa bir açıklama girin.</span><span class="sxs-lookup"><span data-stu-id="99697-163">Enter a short description that indicates what the work class is used for.</span></span>

    - <span data-ttu-id="99697-164">**İş emri türü:** *Kalite denetiminde kalite*</span><span class="sxs-lookup"><span data-stu-id="99697-164">**Work order type:** *Quality in quality check*</span></span>

        <span data-ttu-id="99697-165">İş sınıfı tarafından oluşturulan iş emri türünü seçin.</span><span class="sxs-lookup"><span data-stu-id="99697-165">Select the type of work order that is created by the work class.</span></span> <span data-ttu-id="99697-166">Kalite denetimi işi ayarladığınızda, her zaman *Kalite denetiminde kalite*'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="99697-166">When you set up quality control work, always select *Quality in quality check*.</span></span>

1. <span data-ttu-id="99697-167">**Geçerli yerine koyma konumu türleri** hızlı sekmesinde, **Konum türü** alanını boş bırakın.</span><span class="sxs-lookup"><span data-stu-id="99697-167">On the **Valid put location types** FastTab, leave the **Location type** field blank.</span></span>

    <span data-ttu-id="99697-168">Bir konum türü seçerseniz kalemler çekildikten sonra koyulacakları konumları sınırlamış olursunuz.</span><span class="sxs-lookup"><span data-stu-id="99697-168">If you select a location type, you limit the locations where items can be put after they are picked.</span></span> <span data-ttu-id="99697-169">Bu alan, konum yönergesi konumu çözümlemeye çalışırken ya da bir ambar çalışanı el ile mobil cihaz menü öğesi konumunu belirtirken kullanılır.</span><span class="sxs-lookup"><span data-stu-id="99697-169">This field is used when a location directive tries to resolve the location, or when a warehouse worker manually specifies the location for the mobile device menu item.</span></span>

<span data-ttu-id="99697-170">İş sınıfları ve bunların nasıl oluşturulacağı hakkında daha fazla bilgi için bkz. [İş sınıfı oluşturma](tasks/create-work-class.md).</span><span class="sxs-lookup"><span data-stu-id="99697-170">For more information about work classes and how to create them, see [Create a work class](tasks/create-work-class.md).</span></span>

### <a name="work-template"></a><span data-ttu-id="99697-171">İş şablonu</span><span class="sxs-lookup"><span data-stu-id="99697-171">Work template</span></span>

<span data-ttu-id="99697-172">İş şablonları, ambarda gerçekleştirilmesi gereken iş operasyonlarını tanımlamanıza olanak sağlar.</span><span class="sxs-lookup"><span data-stu-id="99697-172">Work templates let you define the work operations that must be performed in the warehouse.</span></span> <span data-ttu-id="99697-173">Genellikle, ambar iş operasyonları bir eylemler çiftinden oluşur: Bir ambar çalışanı eldeki stoku bir konumdan çeker ve çekilen stoku başka bir konuma indirir.</span><span class="sxs-lookup"><span data-stu-id="99697-173">Typically, warehouse work operations consist of a pair of actions: a warehouse worker picks on-hand inventory up in one location and then puts the picked inventory down in another location.</span></span> <span data-ttu-id="99697-174">Kalite denetimi için iş şablonu, kalite denetimleri yapmaya yönelik iş işlemlerini tanımlar.</span><span class="sxs-lookup"><span data-stu-id="99697-174">A work template for quality control defines the work operations for doing quality checks.</span></span>

#### <a name="purchase-orders"></a><span data-ttu-id="99697-175">Satın alma siparişleri</span><span class="sxs-lookup"><span data-stu-id="99697-175">Purchase orders</span></span>

1. <span data-ttu-id="99697-176">**Ambar yönetimi \> Kurulum \> İş \> İş şablonları**'na gidin.</span><span class="sxs-lookup"><span data-stu-id="99697-176">Go to **Warehouse management \> Setup \> Work \> Work templates**.</span></span>
1. <span data-ttu-id="99697-177">Başlıkta, **İş emri türü** alanını *Satın alma siparişi* olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="99697-177">In the header, set the **Work order type** field to *Purchase orders*.</span></span>
1. <span data-ttu-id="99697-178">Eylem Bölmesi'nde, **Düzenle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="99697-178">On the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="99697-179">Kalite denetimi adımı içerecek bir iş şablonu seçin.</span><span class="sxs-lookup"><span data-stu-id="99697-179">Select a work template that should include a quality check step.</span></span> <span data-ttu-id="99697-180">**Genel bakış** bölümünde, **İş şablonu** alanında, *51 SAS Girişi* öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="99697-180">In the **Overview** section, in the **Work template** field, select *51 PO Receipt*.</span></span>
1. <span data-ttu-id="99697-181">**İş şablonu ayrıntıları** bölümünde, kılavuzun mevcut iki satırı olduğuna dikkat edin: *Malzeme çekme* için bir ve *Yerine koyma* için bir adet.</span><span class="sxs-lookup"><span data-stu-id="99697-181">In the **Work template details** section, notice that the grid has two existing lines: one for *Pick* and one for *Put*.</span></span>
1. <span data-ttu-id="99697-182">**İş şablonu ayrıntıları** bölümünde, kılavuza kalite denetimi satırı eklemek için **Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="99697-182">In the **Work template details** section, select **New** to add a row for quality control to the grid.</span></span> <span data-ttu-id="99697-183">Yeni satır için **Satır numarası** alanının *3* olarak ayarlandığına dikkat edin.</span><span class="sxs-lookup"><span data-stu-id="99697-183">Notice that the **Line number** field for the new line is set to *3*.</span></span>
1. <span data-ttu-id="99697-184">Yeni satırda aşağıdaki değerleri ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="99697-184">On the new line, set the following values.</span></span> <span data-ttu-id="99697-185">Kalan alanlar için varsayılan değerleri kabul edin.</span><span class="sxs-lookup"><span data-stu-id="99697-185">Accept the default values for the remaining fields.</span></span>

    - <span data-ttu-id="99697-186">**İş türü:** *Kalite denetimi*</span><span class="sxs-lookup"><span data-stu-id="99697-186">**Work type:** *Quality check*</span></span>
    - <span data-ttu-id="99697-187">**İş sınıfı kodu:** *Purchase*</span><span class="sxs-lookup"><span data-stu-id="99697-187">**Work class ID:** *Purchase*</span></span>
    - <span data-ttu-id="99697-188">**Kalite denetim şablonu adı:** *Giriş noktası denetimi*</span><span class="sxs-lookup"><span data-stu-id="99697-188">**Quality check template name:** *Dock check*</span></span>

        <span data-ttu-id="99697-189">İş sınıfı için benzersiz kimlik seçin.</span><span class="sxs-lookup"><span data-stu-id="99697-189">Select the unique ID for the work class.</span></span> <span data-ttu-id="99697-190">Mobil cihazdaki menü öğelerini ve bu menü öğelerinin işleyebildiği iş türlerini konfigüre etmek için bu değeri kullanın.</span><span class="sxs-lookup"><span data-stu-id="99697-190">You use this value to configure the menu items on the mobile device and the types of work that those menu items can process.</span></span>

1. <span data-ttu-id="99697-191">Eylem Bölmesinde, şimdiye kadarki çalışmanızı kaydetmek için **Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="99697-191">On the Action Pane, select **Save** to save your work so far.</span></span>

    <span data-ttu-id="99697-192">"Geçersiz - Kalite denetiminin malzeme çekme işleminden hemen sonra gelmesi gerekir" şeklinde bir bilgi iletisi alırsınız.</span><span class="sxs-lookup"><span data-stu-id="99697-192">You receive an informational message that states, "Invalid - Quality check must come directly after a pick."</span></span> <span data-ttu-id="99697-193">Bu nedenle, az önce eklediğiniz satırın **Satır numarası** değerini değiştirmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="99697-193">Therefore, you must change the **Line number** value for the line that you just added.</span></span>

1. <span data-ttu-id="99697-194">Yeni satırın **Satır numarası** değerini değiştirmek için şu adımları izleyin:</span><span class="sxs-lookup"><span data-stu-id="99697-194">Follow these steps to change the **Line number** value for the new line:</span></span>

    1. <span data-ttu-id="99697-195">**İş şablonu ayrıntıları** bölümünde, **İş türü** alanının *Kalite denetimi* olarak ayarlandığı satırı seçin.</span><span class="sxs-lookup"><span data-stu-id="99697-195">In the **Work template details** section, select the line where the **Work type** field is set to *Quality check*.</span></span>
    2. <span data-ttu-id="99697-196">*Kalite denetimi* satırını *Malzeme çekme* satırından sonra olacak şekilde taşımak için **Yukarı taşı** veya **Aşağı taşı** düğmesini seçin.</span><span class="sxs-lookup"><span data-stu-id="99697-196">Select the **Move up** or **Move down** button to move the *Quality check* line so that it's after the *Pick* line.</span></span>

1. <span data-ttu-id="99697-197">Eylem bölmesinde, **Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="99697-197">On the Action Pane, select **Save**.</span></span>

#### <a name="quality-in-quality-check"></a><span data-ttu-id="99697-198">Kalite denetiminde kalite</span><span class="sxs-lookup"><span data-stu-id="99697-198">Quality in quality check</span></span>

<span data-ttu-id="99697-199">Daha sonra, kalite denetimi için bir iş şablonu oluşturun.</span><span class="sxs-lookup"><span data-stu-id="99697-199">Next, create a work template for the quality check.</span></span>

1. <span data-ttu-id="99697-200">**İş şablonları** sayfasının başlığında, **İş emri türü** alanının değerini *Kalite denetiminde kalite* olarak değiştirin.</span><span class="sxs-lookup"><span data-stu-id="99697-200">In the header of the **Work templates** page, change the value of the **Work order type** field to *Quality in quality check*.</span></span>
1. <span data-ttu-id="99697-201">Eylem Bölmesinde, **Genel bakış** bölümünde kılavuzuna satır eklemek için **Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="99697-201">On the Action Pane, select **New** to add a row to the grid in the **Overview** section.</span></span>
1. <span data-ttu-id="99697-202">Yeni satırda aşağıdaki değerleri ayarlayın:</span><span class="sxs-lookup"><span data-stu-id="99697-202">In the new row, set the following values:</span></span>

    - <span data-ttu-id="99697-203">**İş şablonu:** *51 Kalite Denetimi*</span><span class="sxs-lookup"><span data-stu-id="99697-203">**Work template:** *51 Quality Check*</span></span>

        <span data-ttu-id="99697-204">Şablon için bir ad girin.</span><span class="sxs-lookup"><span data-stu-id="99697-204">Enter a name for the template.</span></span>

    - <span data-ttu-id="99697-205">**İş şablonu açıklaması:** *51 Kalite Denetimi*</span><span class="sxs-lookup"><span data-stu-id="99697-205">**Work template description:** *51 Quality Check*</span></span>

1. <span data-ttu-id="99697-206">Eylem Bölmesinde, **İş şablonu ayrıntıları** bölümünü kullanılabilir hale getirmek için **Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="99697-206">On the Action Pane, select **Save** to make the **Work template details** section available.</span></span>
1. <span data-ttu-id="99697-207">Yeni şablon **Genel bakış** bölümünde hala seçiliyken, kılavuza bir satır eklemek için **İş şablonu ayrıntıları** bölümünde **Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="99697-207">While the new template is still selected in the **Overview** section, select **New** in the **Work template details** section to add a row to the grid there.</span></span>
1. <span data-ttu-id="99697-208">Yeni satırda aşağıdaki değerleri ayarlayın:</span><span class="sxs-lookup"><span data-stu-id="99697-208">In the new row, set the following values:</span></span>

    - <span data-ttu-id="99697-209">**İş türü:** *Çekme*</span><span class="sxs-lookup"><span data-stu-id="99697-209">**Work type:** *Pick*</span></span>
    - <span data-ttu-id="99697-210">**İş sınıfı kodu:** *QC Check*</span><span class="sxs-lookup"><span data-stu-id="99697-210">**Work class ID:** *QC Check*</span></span>

        <span data-ttu-id="99697-211">Kalite denetimi işi için daha önce oluşturduğunuz [iş sınıfının](#work-class) adını seçin.</span><span class="sxs-lookup"><span data-stu-id="99697-211">Select the name of the [work class](#work-class) that you created earlier for quality control work.</span></span>

1. <span data-ttu-id="99697-212">**İş şablonu ayrıntıları** bölümünde, başka bir satır eklemek için **Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="99697-212">In the **Work template details** section, select **New** again to add another row.</span></span>
1. <span data-ttu-id="99697-213">Yeni satırda aşağıdaki değerleri ayarlayın:</span><span class="sxs-lookup"><span data-stu-id="99697-213">In the new row, set the following values:</span></span>

    - <span data-ttu-id="99697-214">**İş türü:** *Yerine koyma*</span><span class="sxs-lookup"><span data-stu-id="99697-214">**Work type:** *Put*</span></span>
    - <span data-ttu-id="99697-215">**İş sınıfı kodu:** *QC Check*</span><span class="sxs-lookup"><span data-stu-id="99697-215">**Work class ID:** *QC Check*</span></span>

        <span data-ttu-id="99697-216">Kalite denetimi işi için daha önce oluşturduğunuz [iş sınıfının](#work-class) adını seçin.</span><span class="sxs-lookup"><span data-stu-id="99697-216">Select the name of the [work class](#work-class) that you created earlier for quality control work.</span></span>

1. <span data-ttu-id="99697-217">Eylem bölmesinde, **Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="99697-217">On the Action Pane, select **Save**.</span></span>

<span data-ttu-id="99697-218">İş şablonları hakkında daha fazla bilgi için bkz. [İş şablonları ve konum yönergelerini kullanarak ambar işini denetleme](control-warehouse-location-directives.md)</span><span class="sxs-lookup"><span data-stu-id="99697-218">For more information about work templates, see [Control warehouse work by using work templates and location directives](control-warehouse-location-directives.md)</span></span>

### <a name="location-directive--quality-failures"></a><span data-ttu-id="99697-219">Konum yönergesi – Kalite başarısızlıkları</span><span class="sxs-lookup"><span data-stu-id="99697-219">Location directive – Quality failures</span></span>

<span data-ttu-id="99697-220">Konum yönergeleri stok hareketi için çekme ve indirme konumlarını belirlemeye yardımcı olan kurallardır.</span><span class="sxs-lookup"><span data-stu-id="99697-220">Location directives are rules that help identify pick and put locations for inventory movement.</span></span> <span data-ttu-id="99697-221">Örneğin, bir satış siparişi hareketinde, kalemlerin nereden çekileceğini ve nereye indirileceğini bir konum yönergesi belirler.</span><span class="sxs-lookup"><span data-stu-id="99697-221">For example, in a sales order transaction, a location directive determines where the items will be picked and where the picked items will be put.</span></span> <span data-ttu-id="99697-222">Başarısız kalite denetimlerinin nasıl işleneceğini tanımlamak için bir konum yönergesi kuralı yapılandırmalısınız.</span><span class="sxs-lookup"><span data-stu-id="99697-222">You must configure a location directive rule to define how failed quality checks will be handled.</span></span>

1. <span data-ttu-id="99697-223">**Ambar Yönetimi \> Kurulum \> Konum yönergeleri** seçeneğine gidin.</span><span class="sxs-lookup"><span data-stu-id="99697-223">Go to **Warehouse management \> Setup \> Location directives**.</span></span>
1. <span data-ttu-id="99697-224">Sol bölmede, **İş emri türü** alanını, ilgili türdeki konum yönergeleriyle çalışacak şekilde *Satın alma siparişleri* olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="99697-224">In the left pane, set the **Work order type** field to *Purchase orders* to work with location directives of that type.</span></span>
1. <span data-ttu-id="99697-225">Eylem Bölmesinde, kalite denetimleri için konum yönergesi oluşturmak üzere **Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="99697-225">On the Action Pane, select **New** to create a location directive for quality checks.</span></span>
1. <span data-ttu-id="99697-226">Üst bilgide aşağıdaki değerleri ayarlayın:</span><span class="sxs-lookup"><span data-stu-id="99697-226">In the header, set the following values:</span></span>

    - <span data-ttu-id="99697-227">**Sıra numarası:** Varsayılan değeri kabul edin.</span><span class="sxs-lookup"><span data-stu-id="99697-227">**Sequence number:** Accept the default value.</span></span>
    - <span data-ttu-id="99697-228">**Ad:** *51 Kalite*</span><span class="sxs-lookup"><span data-stu-id="99697-228">**Name:** *51 To Quality*</span></span>

1. <span data-ttu-id="99697-229">**Yerleşim yönergeleri** hızlı sekmesinde aşağıdaki değerleri ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="99697-229">On the **Location directives** FastTab, set the following values.</span></span> <span data-ttu-id="99697-230">Kalan alanlar için varsayılan değerleri kabul edin.</span><span class="sxs-lookup"><span data-stu-id="99697-230">Accept the default values for the remaining fields.</span></span>

    - <span data-ttu-id="99697-231">**İş türü:** *Yerine koyma*</span><span class="sxs-lookup"><span data-stu-id="99697-231">**Work type:** *Put*</span></span>
    - <span data-ttu-id="99697-232">**Tesis:** *5*</span><span class="sxs-lookup"><span data-stu-id="99697-232">**Site:** *5*</span></span>
    - <span data-ttu-id="99697-233">**Ambar:** *51*</span><span class="sxs-lookup"><span data-stu-id="99697-233">**Warehouse:** *51*</span></span>

1. <span data-ttu-id="99697-234">Eylem Bölmesinde, **Kaydet**'i seçerek yönergenizi kaydedin ve **Satırlar** hızlı sekmesini kullanılabilir hale getirin.</span><span class="sxs-lookup"><span data-stu-id="99697-234">On the Action Pane select **Save** to save your directive and make the **Lines** FastTab available.</span></span>
1. <span data-ttu-id="99697-235">**Satırlar** hızlı sekmesinde, kılavuza satır eklemek için **Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="99697-235">On the **Lines** FastTab, select **New** to add a line to the grid.</span></span>
1. <span data-ttu-id="99697-236">Yeni satırda aşağıdaki değerleri ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="99697-236">On the new line, set the following values.</span></span> <span data-ttu-id="99697-237">Kalan alanlar için varsayılan değerleri kabul edin.</span><span class="sxs-lookup"><span data-stu-id="99697-237">Accept the default values for the remaining fields.</span></span>

    - <span data-ttu-id="99697-238">**Başlangıç miktarı:** *1*</span><span class="sxs-lookup"><span data-stu-id="99697-238">**From quantity:** *1*</span></span>
    - <span data-ttu-id="99697-239">**Son miktar:** *1000000*</span><span class="sxs-lookup"><span data-stu-id="99697-239">**To quantity:** *1000000*</span></span>

1. <span data-ttu-id="99697-240">Eylem Bölmesinde, **Kaydet**'i seçerek yeni satırı kaydedin ve **Konum yönergesi eylemleri** hızlı sekmesini kullanılabilir hale getirin.</span><span class="sxs-lookup"><span data-stu-id="99697-240">On the Action Pane, select **Save** to save the new line and make the **Location directive actions** FastTab available.</span></span>
1. <span data-ttu-id="99697-241">Yeni satır **Satırlar** hızlı sekmesinde seçili durumdayken, kılavuza bir satır eklemek için **Konum yönergesi eylemleri** hızlı sekmesinde **Yeni**'yi seçin; böylece satır için bir eylem ayarlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="99697-241">While the new line is still selected on the **Lines** FastTab, select **New** on the **Location directive actions** FastTab to add a row to the grid there, so that you can set up an action for the line.</span></span>
1. <span data-ttu-id="99697-242">Yeni satırda, **Ad** alanını *Kalite* olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="99697-242">In the new row, set the **Name** field to *Quality*.</span></span> <span data-ttu-id="99697-243">Kalan alanlar için varsayılan değerleri kabul edin.</span><span class="sxs-lookup"><span data-stu-id="99697-243">Accept the default values for the remaining fields.</span></span>
1. <span data-ttu-id="99697-244">**Konum yönergesi eylemleri** hızlı sekmesinde **Sorguyu düzenle** düğmesini kullanılabilir hale getirmek için Eylem Bölmesindeki **Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="99697-244">On the Action Pane, select **Save** to make the **Edit query** button on the **Location directive actions** FastTab available.</span></span>
1. <span data-ttu-id="99697-245">Yeni eklediğiniz satır **Konum yönergesi eylemleri** hızlı sekmesinde seçiliyken, eylem sorgusunu düzenleyebileceğiniz bir iletişim kutusu açmak için **Sorguyu düzenle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="99697-245">While the line that you just added is still selected on the **Location directive actions** FastTab, select **Edit query** to open a dialog box where you can edit the query for the action.</span></span>
1. <span data-ttu-id="99697-246">**Aralık** sekmesinde, sorguya satır eklemek için **Ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="99697-246">On the **Range** tab, select **Add** to add a row to the query.</span></span>
1. <span data-ttu-id="99697-247">Yeni satırda aşağıdaki değerleri ayarlayın:</span><span class="sxs-lookup"><span data-stu-id="99697-247">In the new row, set the following values:</span></span>

    - <span data-ttu-id="99697-248">**Tablo:** *Yerleşimler*</span><span class="sxs-lookup"><span data-stu-id="99697-248">**Table:** *Locations*</span></span>
    - <span data-ttu-id="99697-249">**Türetilmiş tablo:** *Yerleşimler*</span><span class="sxs-lookup"><span data-stu-id="99697-249">**Derived table:** *Locations*</span></span>
    - <span data-ttu-id="99697-250">**Alan:** *Yerleşim*</span><span class="sxs-lookup"><span data-stu-id="99697-250">**Field:** *Location*</span></span>
    - <span data-ttu-id="99697-251">**Ölçüt:** *QMS*</span><span class="sxs-lookup"><span data-stu-id="99697-251">**Criteria:** *QMS*</span></span>

    <span data-ttu-id="99697-252">*QMS* konumu, kalite için bir ambar konumudur.</span><span class="sxs-lookup"><span data-stu-id="99697-252">The *QMS* location is a warehouse location for quality.</span></span>

1. <span data-ttu-id="99697-253">İletişim kutusunu kapatmak için **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="99697-253">Select **OK** to close the dialog box.</span></span>
1. <span data-ttu-id="99697-254">Ambar *51* için satın alma siparişi konum yönergelerinin sırasını değiştirmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="99697-254">You must now change the sequence of purchase order location directives for warehouse *51*.</span></span> <span data-ttu-id="99697-255">Kalite konumu yönergesine yeni *51 Kalite* konumu kaydedin, sayfayı yenileyin ve listeden konum yönergesini seçin.</span><span class="sxs-lookup"><span data-stu-id="99697-255">Save the new *51 To Quality* location directive, refresh the page, and select the location directive in the list.</span></span> <span data-ttu-id="99697-256">Sonra, ambar *51* için konum yönergesini aşağıdaki sıraya koymak için Eylem Bölmesindeki **Yukarı taşı** ve **Aşağı taşı** düğmelerini kullanın.</span><span class="sxs-lookup"><span data-stu-id="99697-256">Then use the **Move up** and **Move down** buttons on the Action Pane to put the location directive for warehouse *51* in the following order.</span></span> <span data-ttu-id="99697-257">(**Yukarı taşı** veya **Aşağı taşı** düğmelerini seçmeden önce listeden bir konum yönergesi seçmelisiniz.)</span><span class="sxs-lookup"><span data-stu-id="99697-257">(Before you select **Move up** or **Move down**, you must select a location directive in the list.)</span></span>

    1. <span data-ttu-id="99697-258">51 Kalite</span><span class="sxs-lookup"><span data-stu-id="99697-258">51 To Quality</span></span>
    2. <span data-ttu-id="99697-259">51 SAS Doğrudan</span><span class="sxs-lookup"><span data-stu-id="99697-259">51 PO Direct</span></span>
    3. <span data-ttu-id="99697-260">51 QMS</span><span class="sxs-lookup"><span data-stu-id="99697-260">51 QMS</span></span>

### <a name="mobile-device-menu-items"></a><span data-ttu-id="99697-261">Mobil cihaz menü öğeleri</span><span class="sxs-lookup"><span data-stu-id="99697-261">Mobile device menu items</span></span>

<span data-ttu-id="99697-262">Mobil cihazların **Kalite Denetimi** işlevini gerçekleştirebilmesi için bir menü öğesini yapılandırın.</span><span class="sxs-lookup"><span data-stu-id="99697-262">Configure a menu item so that mobile devices can perform the **Quality Check** function.</span></span>

#### <a name="purchase-putaway"></a><span data-ttu-id="99697-263">Satın alma yerine koyma</span><span class="sxs-lookup"><span data-stu-id="99697-263">Purchase putaway</span></span>

1. <span data-ttu-id="99697-264">**Ambar yönetimi \> Kurulum \> Mobil cihaz \> Mobil cihaz menüsü öğeleri**'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="99697-264">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu items**.</span></span>
1. <span data-ttu-id="99697-265">Listeden, **Satın alma yerine koyma** menü öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="99697-265">In the list, select the **Purchase put-away** menu item.</span></span>
1. <span data-ttu-id="99697-266">Eylem Bölmesi'nde, **Düzenle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="99697-266">On the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="99697-267">**İş sınıfları** bölümünde, kılavuza satır eklemek için **Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="99697-267">In the **Work classes** section, select **New** to add a row to the grid.</span></span>
1. <span data-ttu-id="99697-268">Yeni satırda aşağıdaki değerleri ayarlayın:</span><span class="sxs-lookup"><span data-stu-id="99697-268">In the new row, set the following values:</span></span>

    - <span data-ttu-id="99697-269">**İş sınıfı kodu:** *QC Check*</span><span class="sxs-lookup"><span data-stu-id="99697-269">**Work class ID:** *QC Check*</span></span>

        <span data-ttu-id="99697-270">Kalite denetimi işi için daha önce oluşturduğunuz [iş sınıfının](#work-class) adını girin.</span><span class="sxs-lookup"><span data-stu-id="99697-270">Enter the name of the [work class](#work-class) that you created earlier for quality control work.</span></span>

    - <span data-ttu-id="99697-271">**İş emri türü:** *Kalite denetiminde kalite*</span><span class="sxs-lookup"><span data-stu-id="99697-271">**Work order type:** *Quality in quality check*</span></span>

1. <span data-ttu-id="99697-272">Eylem bölmesinde, **Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="99697-272">On the Action Pane, select **Save**.</span></span>

#### <a name="purchase-order-line-receiving"></a><span data-ttu-id="99697-273">Satınalma siparişi satırı teslim alma</span><span class="sxs-lookup"><span data-stu-id="99697-273">Purchase order line receiving</span></span>

1. <span data-ttu-id="99697-274">**Ambar yönetimi \> Kurulum \> Mobil cihaz \> Mobil cihaz menüsü öğeleri**'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="99697-274">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu items**.</span></span>
1. <span data-ttu-id="99697-275">Eylem Bölmesinde, **Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="99697-275">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="99697-276">Üst bilgide aşağıdaki değerleri ayarlayın:</span><span class="sxs-lookup"><span data-stu-id="99697-276">In the header, set the following values:</span></span>

    - <span data-ttu-id="99697-277">**Menü madde adı:** *Satınalma siparişi satın alma*</span><span class="sxs-lookup"><span data-stu-id="99697-277">**Menu item name:** *PO line receiving*</span></span>
    - <span data-ttu-id="99697-278">**Başlık:** *Satınalma siparişi satın alma*</span><span class="sxs-lookup"><span data-stu-id="99697-278">**Title:** *PO line receiving*</span></span>
    - <span data-ttu-id="99697-279">**Mod:** *İş*</span><span class="sxs-lookup"><span data-stu-id="99697-279">**Mode:** *Work*</span></span>
    - <span data-ttu-id="99697-280">**Varolan çalışmayı kullan:** *Hayır*</span><span class="sxs-lookup"><span data-stu-id="99697-280">**Use existing work:** *No*</span></span>

1. <span data-ttu-id="99697-281">**Genel** hızlı sekmesinde, aşağıdaki değerleri ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="99697-281">On the **General** FastTab, set the following values.</span></span> <span data-ttu-id="99697-282">Kalan alanlar için varsayılan değerleri kabul edin.</span><span class="sxs-lookup"><span data-stu-id="99697-282">Accept the default values for the remaining fields.</span></span>

    - <span data-ttu-id="99697-283">**İş oluşturma işlemi:** *Satın alma siparişi satırı teslim alma ve yerine koyma*</span><span class="sxs-lookup"><span data-stu-id="99697-283">**Work creation process:** *Purchase order line receiving and put away*</span></span>
    - <span data-ttu-id="99697-284">**Plaka oluştur:** *Evet*</span><span class="sxs-lookup"><span data-stu-id="99697-284">**Generate license plate:** *Yes*</span></span>
    - <span data-ttu-id="99697-285">**İş şablonu:** *51 SAS Girişi*</span><span class="sxs-lookup"><span data-stu-id="99697-285">**Work template:** *51 PO Receipt*</span></span>

1. <span data-ttu-id="99697-286">Eylem bölmesinde, **Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="99697-286">On the Action Pane, select **Save**.</span></span>

#### <a name="add-the-menu-item-to-a-mobile-device-menu"></a><span data-ttu-id="99697-287">Mobil cihaz menüsüne menü öğesi ekleme</span><span class="sxs-lookup"><span data-stu-id="99697-287">Add the menu item to a mobile device menu</span></span>

1. <span data-ttu-id="99697-288">**Ambar yönetimi \> Kurulum \> Mobil cihaz \> Mobil cihaz menüsü**'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="99697-288">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu**.</span></span>
1. <span data-ttu-id="99697-289">Sol bölmede, **Gelen** menüsünü seçin.</span><span class="sxs-lookup"><span data-stu-id="99697-289">In the left pane, select the **Inbound** menu.</span></span>
1. <span data-ttu-id="99697-290">Eylem Bölmesi'nde, **Düzenle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="99697-290">On the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="99697-291">**Mevcut menüler ve menü öğeleri** sütununda, yeni **SAS satırı alma** menüsü öğesini bulup seçin.</span><span class="sxs-lookup"><span data-stu-id="99697-291">In the **Available menus and menu items** column, select the new **PO line receiving** menu item.</span></span>
1. <span data-ttu-id="99697-292">**SAS satırı alma**'yı **Menü yapısı** sütununa taşımak için sağ ok düğmesini seçin.</span><span class="sxs-lookup"><span data-stu-id="99697-292">Select the right arrow button to move **PO line receiving** to the **Menu structure** column.</span></span>
1. <span data-ttu-id="99697-293">**Menü yapısı** sütununda, **SAS satırı alma**'yı seçin ve ardından menü öğesini mobil cihaz menüsünde istediğiniz konuma taşımak için yukarı ok veya aşağı ok düğmesini seçin.</span><span class="sxs-lookup"><span data-stu-id="99697-293">In the **Menu structure** column, select **PO line receiving**, and then select the up arrow or down arrow button to move the menu item to the desired position on the mobile device menu.</span></span>
1. <span data-ttu-id="99697-294">Eylem bölmesinde, **Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="99697-294">On the Action Pane, select **Save**.</span></span>

## <a name="example-scenario"></a><a name="example-scenario"></a><span data-ttu-id="99697-295">Örnek senaryo</span><span class="sxs-lookup"><span data-stu-id="99697-295">Example scenario</span></span>

<span data-ttu-id="99697-296">Daha önce açıklanan örnek verilerin tümünü kullanılabilir hale getirip ayarladıktan sonra, bu senaryoda, *Kalite denetimi* özelliğini deneyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="99697-296">After you've made all the previously described sample data available and set it up, you can work through this scenario to try out the *Quality check* feature.</span></span> <span data-ttu-id="99697-297">Bu senaryoda gösterilen değerler, standart demo verileriyle çalıştığınızı, **USMF** tüzel kişiliğini seçmiş olduğunuzu ve bu konunun önceki bölümlerinde açıklanan örnek kayıtları hazırladığınızı varsayar.</span><span class="sxs-lookup"><span data-stu-id="99697-297">The values that are shown in this scenario assume that you're working with the standard demo data, that you selected the **USMF** legal entity, and that you prepared the sample records that are described earlier in this topic.</span></span> <span data-ttu-id="99697-298">Bu senaryo aynı zamanda özelliğin bir üretim ayarında nasıl kullanılabileceğini gösteren bir örnek işlevi de görür.</span><span class="sxs-lookup"><span data-stu-id="99697-298">This scenario also serves as an example that shows how the feature can be used in a production setting.</span></span>

### <a name="create-a-purchase-order"></a><span data-ttu-id="99697-299">Satınalma siparişi oluşturma</span><span class="sxs-lookup"><span data-stu-id="99697-299">Create a purchase order</span></span>

1. <span data-ttu-id="99697-300">**Tedarik ve kaynak atama \> Satınalma siparişleri \> Tüm satınalma siparişleri**'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="99697-300">Go to **Procurement and sourcing \> Purchase orders \> All purchase orders**.</span></span>
1. <span data-ttu-id="99697-301">Eylem Bölmesinde, **Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="99697-301">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="99697-302">**Satın alma siparişi oluştur** iletişim kutusunda, aşağıdaki değerleri ayarlayın:</span><span class="sxs-lookup"><span data-stu-id="99697-302">In the **Create purchase order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="99697-303">**Satıcı hesabı:** *104*</span><span class="sxs-lookup"><span data-stu-id="99697-303">**Vendor account:** *104*</span></span>
    - <span data-ttu-id="99697-304">**Ambar:** *51*</span><span class="sxs-lookup"><span data-stu-id="99697-304">**Warehouse:** *51*</span></span>

1. <span data-ttu-id="99697-305">İletişim kutusunu kapatmak ve yeni satın alma siparişini açmak için **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="99697-305">Select **OK** to close the dialog box and open the new purchase order.</span></span>
1. <span data-ttu-id="99697-306">**Satın alma siparişi satırları** hızlı sekmesine, kılavuzda yeni, boş bir satır bulunur.</span><span class="sxs-lookup"><span data-stu-id="99697-306">On the **Purchase order lines** FastTab, the grid contains a new, blank line.</span></span> <span data-ttu-id="99697-307">Bu satır için aşağıdaki değerleri ayarlayın:</span><span class="sxs-lookup"><span data-stu-id="99697-307">On this line, set the following values:</span></span>

    - <span data-ttu-id="99697-308">**Madde numarası:** *M9203*</span><span class="sxs-lookup"><span data-stu-id="99697-308">**Item number:** *M9203*</span></span>
    - <span data-ttu-id="99697-309">**Miktar:** *3*</span><span class="sxs-lookup"><span data-stu-id="99697-309">**Quantity:** *3*</span></span>
    - <span data-ttu-id="99697-310">**Birim:** *PL*</span><span class="sxs-lookup"><span data-stu-id="99697-310">**Unit:** *PL*</span></span>

1. <span data-ttu-id="99697-311">Eylem bölmesinde, **Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="99697-311">On the Action Pane, select **Save**.</span></span>

### <a name="process-quality-check-receiving"></a><span data-ttu-id="99697-312">İşlem kalite denetimi alma</span><span class="sxs-lookup"><span data-stu-id="99697-312">Process quality check receiving</span></span>

<span data-ttu-id="99697-313">Satın alma siparişi oluşturulduktan sonra, **SAS satırı teslim alma** menü öğesi ve *Kalite denetimi* özelliğinin işlevleri kullanılarak teslim edilebilir.</span><span class="sxs-lookup"><span data-stu-id="99697-313">After the purchase order has been created, it can be received by using the **PO line receiving** menu item and the functionality of the *Quality check* feature.</span></span>

#### <a name="receive-pallet-1"></a><span data-ttu-id="99697-314">Palet 1'i alma</span><span class="sxs-lookup"><span data-stu-id="99697-314">Receive pallet 1</span></span>

1. <span data-ttu-id="99697-315">Ambar uygulamasında ambar *51*'deki bir kullanıcı olarak oturum açın.</span><span class="sxs-lookup"><span data-stu-id="99697-315">Sign in to the warehouse app as a user for warehouse *51*.</span></span> <span data-ttu-id="99697-316">(Kullanıcı kimliği olarak *51*, parola olarak *1* girin.)</span><span class="sxs-lookup"><span data-stu-id="99697-316">(Enter *51* as the user ID and *1* as the password.)</span></span>
1. <span data-ttu-id="99697-317">**Gelen \> SAS satırı teslim alma** bölümüne gidin.</span><span class="sxs-lookup"><span data-stu-id="99697-317">Go to **Inbound \> PO line receiving**.</span></span>
1. <span data-ttu-id="99697-318">**PONUM** alanına satın alma siparişi numaranızı girin.</span><span class="sxs-lookup"><span data-stu-id="99697-318">In the **PONUM** field, enter the purchase order number.</span></span>
1. <span data-ttu-id="99697-319">Satın alma siparişi numarasını doğrulayın.</span><span class="sxs-lookup"><span data-stu-id="99697-319">Confirm the purchase order number.</span></span>
1. <span data-ttu-id="99697-320">**LINENUM** alanına, alınmakta olan satın alma siparişinin numarasını girin.</span><span class="sxs-lookup"><span data-stu-id="99697-320">In the **LINENUM** field, enter the number of the purchase order line that is being received.</span></span> <span data-ttu-id="99697-321">Bu senaryoda siparişin yalnızca bir satırı bulunduğundan, her teslim alma alma adımı için **LINENUM** alanına *1* girin.</span><span class="sxs-lookup"><span data-stu-id="99697-321">Because the order has only one line in this scenario, you will enter *1* in the **LINENUM** field for each receiving step.</span></span>
1. <span data-ttu-id="99697-322">Satır numarasını onaylayın.</span><span class="sxs-lookup"><span data-stu-id="99697-322">Confirm the line number.</span></span>
1. <span data-ttu-id="99697-323">**Miktar** alanına teslim alınacak miktarı girin.</span><span class="sxs-lookup"><span data-stu-id="99697-323">In the **QTY** field, enter the quantity to receive.</span></span> <span data-ttu-id="99697-324">Bu senaryoda satın alma siparişi üç palet (*PL*) için olduğundan ve üç teslim alma adımı olduğundan her teslim alma adımı için **Miktar** alanına *1* girin.</span><span class="sxs-lookup"><span data-stu-id="99697-324">Because the purchase order is for three pallets (*PL*) in this scenario, and there are three receiving steps, you will enter *1* in the **QTY** field for each receiving step.</span></span>
1. <span data-ttu-id="99697-325">Onaylanan miktar.</span><span class="sxs-lookup"><span data-stu-id="99697-325">Confirm the quantity.</span></span>

    <span data-ttu-id="99697-326">Açılan **Kalite denetimi** sayfasında hiç giriş alanı yok.</span><span class="sxs-lookup"><span data-stu-id="99697-326">The **Quality check** page that appears has no entry fields.</span></span> <span data-ttu-id="99697-327">Yalnızca en altta bulunan onay (onay işareti) düğmesi ve en üstteki Menü düğmesi (**≡**) var.</span><span class="sxs-lookup"><span data-stu-id="99697-327">It has only the confirmation (check mark) button at the bottom and the Menu button (**≡**) at the top.</span></span> <span data-ttu-id="99697-328">(Menü düğmesine bazen hamburger veya hamburger düğmesi denir.) Kalite denetimi işlemini hızlandırmak için palet kalite denetimini geçtiğinde kullanıcının yalnızca **Kalite denetimi** sayfasını onaylaması yeterlidir.</span><span class="sxs-lookup"><span data-stu-id="99697-328">(The Menu button is sometimes referred to as the hamburger or the hamburger button.) To expedite the quality check process, when the pallet passes the quality check, the user just confirms the **Quality check** page.</span></span>

    <span data-ttu-id="99697-329">![Kalite denetimi sayfası](media/quality-check.png "Kalite denetimi sayfası")</span><span class="sxs-lookup"><span data-stu-id="99697-329">![Quality check page](media/quality-check.png "Quality check page")</span></span>

1. <span data-ttu-id="99697-330">Palet1'i kalite denetimini geçirmek için satır 1'den onay düğmesini seçin.</span><span class="sxs-lookup"><span data-stu-id="99697-330">Select the confirmation button to pass the quality check for pallet 1 from line 1.</span></span>

    <span data-ttu-id="99697-331">Açılan **Satın alma siparişleri: Yerine koyma** sayfası, yerine koyma işinin ayrıntılarını gösterir:</span><span class="sxs-lookup"><span data-stu-id="99697-331">The **Purchase orders: Put** page that appears shows details of the put work:</span></span>

    - <span data-ttu-id="99697-332">**KONUM:** Sistem tarafından belirlenen konum</span><span class="sxs-lookup"><span data-stu-id="99697-332">**LOC:** The system determined location</span></span>

        <span data-ttu-id="99697-333">Bu konum, satın alma siparişi teslim alma için belirlenmiş yerine koyma konumudur.</span><span class="sxs-lookup"><span data-stu-id="99697-333">This location is the designated putaway location for purchase order receiving.</span></span>

    - <span data-ttu-id="99697-334">**LP:** Sistem tarafından oluşturulan plaka kimliği</span><span class="sxs-lookup"><span data-stu-id="99697-334">**LP:** The system-generated License plate ID</span></span>
    - <span data-ttu-id="99697-335">**Madde:** *M9203*</span><span class="sxs-lookup"><span data-stu-id="99697-335">**Item:** *M9203*</span></span>
    - <span data-ttu-id="99697-336">**Miktar:** *1 PL: 100 beher*</span><span class="sxs-lookup"><span data-stu-id="99697-336">**Qty:** *1 PL: 100 ea*</span></span>

    <span data-ttu-id="99697-337">Kalem açıklaması da gösterilir.</span><span class="sxs-lookup"><span data-stu-id="99697-337">The item description is also shown.</span></span>

1. <span data-ttu-id="99697-338">Yerine koyma işini onaylayın.</span><span class="sxs-lookup"><span data-stu-id="99697-338">Confirm the putaway work.</span></span>

    <span data-ttu-id="99697-339">Satın alma siparişi satırı teslim alma **Görev** sayfasında, "İş Tamamlanadı" iletisi alırsınız.</span><span class="sxs-lookup"><span data-stu-id="99697-339">On the **Task** page for purchase order line receiving, you receive a "Work Completed" message.</span></span> <span data-ttu-id="99697-340">Bir sonraki paleti almaya başlamak için **LINENUM** alanı kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="99697-340">The **LINENUM** field is available so that you can start to receive the next pallet.</span></span>

#### <a name="receive-pallet-2"></a><span data-ttu-id="99697-341">Palet 2'yi alma</span><span class="sxs-lookup"><span data-stu-id="99697-341">Receive pallet 2</span></span>

<span data-ttu-id="99697-342">Bu senaryo için palet 2 reddedilecektir.</span><span class="sxs-lookup"><span data-stu-id="99697-342">For this scenario, pallet 2 will be rejected.</span></span>

1. <span data-ttu-id="99697-343">**LINENUM** alanına *1* girip satır numarasını onaylayın.</span><span class="sxs-lookup"><span data-stu-id="99697-343">In the **LINENUM** field, enter *1*, and confirm the line number.</span></span>
1. <span data-ttu-id="99697-344">**Miktar** alanı artık kullanılabilirdir.</span><span class="sxs-lookup"><span data-stu-id="99697-344">The **QTY** field is now available.</span></span> <span data-ttu-id="99697-345">*1* girin ve miktarı onaylayın.</span><span class="sxs-lookup"><span data-stu-id="99697-345">Enter *1*, and confirm the quantity.</span></span>

    <span data-ttu-id="99697-346">**Kalite denetimi** sayfası görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="99697-346">The **Quality check** page appears.</span></span> <span data-ttu-id="99697-347">Bu giriş için palet, kalite açısından reddedilecek ve *QMS* kalite konumuna yerleştirilecek.</span><span class="sxs-lookup"><span data-stu-id="99697-347">For this receipt, the pallet will be rejected for quality, and it will be put into the *QMS* quality location.</span></span>

1. <span data-ttu-id="99697-348">Sayfanın üst kısmındaki Menü düğmesini (**≡**) seçin ve ardından menüden **Reddet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="99697-348">Select the Menu button (**≡**) at the top of the page, and then, on the menu, select **Reject**.</span></span>
1. <span data-ttu-id="99697-349">Görüntülenen **Görev** sayfasında, paletin daha fazla inceleme için gönderileceği *Yerine koyma* konumu konumu olarak **QMS** girin.</span><span class="sxs-lookup"><span data-stu-id="99697-349">On the **Task** page that appears, enter **QMS** as the *Put* location to send the pallet to for further inspection.</span></span>

    <span data-ttu-id="99697-350">Açılan **Kalite denetiminde kalite: Yerine koyma** sayfası, yerine koyma işinin ayrıntılarını gösterir:</span><span class="sxs-lookup"><span data-stu-id="99697-350">The **Quality in quality check: Put** page that appears shows details of the put work:</span></span>

    - <span data-ttu-id="99697-351">**KONUM:** *QMS*</span><span class="sxs-lookup"><span data-stu-id="99697-351">**LOC:** *QMS*</span></span>

        <span data-ttu-id="99697-352">Bu konum, reddedilen kalite teslim alma için belirlenmiş yerine koyma konumudur.</span><span class="sxs-lookup"><span data-stu-id="99697-352">This location is the designated putaway location for rejected quality receiving.</span></span>

    - <span data-ttu-id="99697-353">**LP:** Sistem tarafından oluşturulan plaka kimliği</span><span class="sxs-lookup"><span data-stu-id="99697-353">**LP:** The system-generated License plate ID</span></span>
    - <span data-ttu-id="99697-354">**Madde:** *M9203*</span><span class="sxs-lookup"><span data-stu-id="99697-354">**Item:** *M9203*</span></span>
    - <span data-ttu-id="99697-355">**Miktar:** *1 PL: 100 beher*</span><span class="sxs-lookup"><span data-stu-id="99697-355">**Qty:** *1 PL: 100 ea*</span></span>

    <span data-ttu-id="99697-356">Kalem açıklaması da gösterilir.</span><span class="sxs-lookup"><span data-stu-id="99697-356">The item description is also shown.</span></span>

1. <span data-ttu-id="99697-357">Yerine koyma işini onaylayın.</span><span class="sxs-lookup"><span data-stu-id="99697-357">Confirm the putaway work.</span></span>

    <span data-ttu-id="99697-358">Satın alma siparişi satırı teslim alma **Görev** sayfasında, "İş Tamamlanadı" iletisi alırsınız.</span><span class="sxs-lookup"><span data-stu-id="99697-358">On the **Task** page for purchase order line receiving, you receive a "Work Completed" message.</span></span> <span data-ttu-id="99697-359">Bir sonraki paleti almaya başlamak için **LINENUM** alanı kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="99697-359">The **LINENUM** field is available so that you can start to receive the next pallet.</span></span>

<span data-ttu-id="99697-360">Kalite denetimini tamamladınız ve reddedilmiş palet için bir kalite emri oluşturdunuz.</span><span class="sxs-lookup"><span data-stu-id="99697-360">You've now completed the quality check and created a quality order for the rejected pallet.</span></span> <span data-ttu-id="99697-361">Oluşturulan emri görüntülemek için **Stok Yönetimi \> Periyodik görevler \> Kalite yönetimi \> Kalite emirleri**'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="99697-361">To view the order that was created, go to **Inventory management \> Periodic tasks \> Quality management \> Quality orders**.</span></span>

<span data-ttu-id="99697-362">Kalite emri testleri artık işlenebilir.</span><span class="sxs-lookup"><span data-stu-id="99697-362">Quality order testing can now be processed.</span></span> <span data-ttu-id="99697-363">Kalite testi bu konuda ele alınmamaktadır.</span><span class="sxs-lookup"><span data-stu-id="99697-363">Quality testing isn't covered in this topic.</span></span>

<span data-ttu-id="99697-364">Kalite yönetimi hakkında daha fazla bilgi için bkz. [Kalite yönetimine genel bakış](../inventory/enable-quality-management.md)</span><span class="sxs-lookup"><span data-stu-id="99697-364">For more information about quality management, see [Quality management overview](../inventory/enable-quality-management.md)</span></span>

#### <a name="receive-pallet-3"></a><span data-ttu-id="99697-365">Palet 3'ü alma</span><span class="sxs-lookup"><span data-stu-id="99697-365">Receive pallet 3</span></span>

<span data-ttu-id="99697-366">Bu senaryo için palet 3 kabul edilecektir.</span><span class="sxs-lookup"><span data-stu-id="99697-366">For this scenario, pallet 3 will be accepted.</span></span>

1. <span data-ttu-id="99697-367">**LINENUM** alanına *1* girip satır numarasını onaylayın.</span><span class="sxs-lookup"><span data-stu-id="99697-367">In the **LINENUM** field, enter *1*, and confirm the line number.</span></span>
1. <span data-ttu-id="99697-368">**Miktar** alanı artık kullanılabilirdir.</span><span class="sxs-lookup"><span data-stu-id="99697-368">The **QTY** field is now available.</span></span> <span data-ttu-id="99697-369">*1* girin ve miktarı onaylayın.</span><span class="sxs-lookup"><span data-stu-id="99697-369">Enter *1*, and confirm the quantity.</span></span>

    <span data-ttu-id="99697-370">**Kalite denetimi** sayfası görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="99697-370">The **Quality check** page appears.</span></span> <span data-ttu-id="99697-371">Bu giriş için palet, kalite açısından kabul edilecek ve toplu yerine koyma konumuna yerleştirilecek.</span><span class="sxs-lookup"><span data-stu-id="99697-371">For this receipt, the pallet will be accepted for quality, and it will be put into a bulk putaway location.</span></span>

1. <span data-ttu-id="99697-372">Kalite denetiminden geçirmek için onay düğmesini seçin.</span><span class="sxs-lookup"><span data-stu-id="99697-372">Select the confirmation button to pass the quality check.</span></span>

    <span data-ttu-id="99697-373">Açılan **Satın alma siparişleri: Yerine koyma** sayfası, yerine koyma işinin ayrıntılarını gösterir:</span><span class="sxs-lookup"><span data-stu-id="99697-373">The **Purchase orders: Put** page that appears shows details of the put work:</span></span>

    - <span data-ttu-id="99697-374">**KONUM:** Sistem tarafından belirlenen konum</span><span class="sxs-lookup"><span data-stu-id="99697-374">**LOC:** The system determined location</span></span>

        <span data-ttu-id="99697-375">Bu konum, satın alma siparişi teslim alma için belirlenmiş yerine koyma konumudur.</span><span class="sxs-lookup"><span data-stu-id="99697-375">This location is the designated putaway location for purchase order receiving.</span></span>

    - <span data-ttu-id="99697-376">**LP:** Sistem tarafından oluşturulan plaka kimliği</span><span class="sxs-lookup"><span data-stu-id="99697-376">**LP:** The system-generated License plate ID</span></span>
    - <span data-ttu-id="99697-377">**Madde:** *M9203*</span><span class="sxs-lookup"><span data-stu-id="99697-377">**Item:** *M9203*</span></span>
    - <span data-ttu-id="99697-378">**Miktar:** *1 PL: 100 beher*</span><span class="sxs-lookup"><span data-stu-id="99697-378">**Qty:** *1 PL: 100 ea*</span></span>

    <span data-ttu-id="99697-379">Kalem açıklaması da gösterilir.</span><span class="sxs-lookup"><span data-stu-id="99697-379">The item description is also shown.</span></span>

1. <span data-ttu-id="99697-380">Yerine koyma işini onaylayın.</span><span class="sxs-lookup"><span data-stu-id="99697-380">Confirm the putaway work.</span></span>

    <span data-ttu-id="99697-381">Satın alma siparişi satırı teslim alma **Görev** sayfasında, "İş Tamamlanadı" iletisi alırsınız.</span><span class="sxs-lookup"><span data-stu-id="99697-381">On the **Task** page for purchase order line receiving, you receive a "Work Completed" message.</span></span> <span data-ttu-id="99697-382">Bir sonraki paleti almaya başlamak için **LINENUM** alanı kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="99697-382">The **LINENUM** field is available so that you can start to receive the next pallet.</span></span>

1. <span data-ttu-id="99697-383">Sayfanın üst kısmındaki Menü düğmesini (**≡**) seçin ve ardından menüden **İptal**'i seçerek menüye dönün.</span><span class="sxs-lookup"><span data-stu-id="99697-383">Select the Menu button (**≡**) at the top of the page, and then, on the menu, select **Cancel** to return to the menu.</span></span>

<span data-ttu-id="99697-384">Artık mobil uygulamayı kapatabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="99697-384">You can now close the mobile app.</span></span>
