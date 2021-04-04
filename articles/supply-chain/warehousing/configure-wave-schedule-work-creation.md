---
title: Dalga sırasında iş oluşturmayı zamanlama
description: Bu konu, İş oluşturmayı zamanlama dalga işleme yönteminin nasıl ayarlanacağını ve kullanılacağını açıklamaktadır.
author: perlynne
manager: mirzaab
ms.date: 01/14/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSPostMethod, WHSWavePostMethodTaskConfig, WHSWaveTemplateTable, WHSParameters, WHSWaveTableListPage, WHSWorkTableListPage, WHSWorkTable, BatchJobEnhanced, WHSPlannedWorkOrder
audience: Application User
ms.reviewer: ''
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2021-01-14
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: 36a450f78695f617056875f8d236fe46bc66aaaf
ms.sourcegitcommit: 2b4809e60974e72df9476ffd62706b1bfc8da4a7
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/04/2021
ms.locfileid: "5501234"
---
# <a name="schedule-work-creation-during-wave"></a><span data-ttu-id="05cc6-103">Dalga sırasında iş oluşturmayı zamanlama</span><span class="sxs-lookup"><span data-stu-id="05cc6-103">Schedule work creation during wave</span></span>

[!include [banner](../../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="05cc6-104">Sistemin paralel işlemeyi kullanarak iş oluşturmasıyla dalga işleme aktarım hızını artırmak için dalga işlemenin parçası olarak *İş oluşturmayı zamanla* özelliğini kullanın.</span><span class="sxs-lookup"><span data-stu-id="05cc6-104">Use the *Schedule work creation* feature as part of your waving process to help increase wave processing throughput by having the system create work using parallel processing.</span></span>

<span data-ttu-id="05cc6-105">İşlev etkinleştirildiğinde, planlanan çalışma otomatik olarak oluşturulur ve sistem daha sonra bunu asılı işi oluşturmak için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="05cc6-105">When the functionality is enabled, planned work will automatically get created, which the system will eventually process to create actual work.</span></span> <span data-ttu-id="05cc6-106">Dalga yükü satırlarının sayısı önceden belirlenmiş bir eşiğe ulaşırsa sistem paralel, zaman uyumsuz işlem uygulayarak asıl işi daha hızlı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="05cc6-106">If the number of wave load lines reaches a predetermined threshold, the system will create actual work more quickly by applying parallel, asynchronous processing.</span></span>

## <a name="enable-the-schedule-work-creation-feature"></a><span data-ttu-id="05cc6-107">İş oluşturmayı zamanla özelliğini etkinleştirme</span><span class="sxs-lookup"><span data-stu-id="05cc6-107">Enable the Schedule work creation feature</span></span>

### <a name="enable-the-feature-in-feature-management"></a><span data-ttu-id="05cc6-108">Özelliği özellik yönetiminde etkinleştirme</span><span class="sxs-lookup"><span data-stu-id="05cc6-108">Enable the feature in feature management</span></span>

<span data-ttu-id="05cc6-109">*İş oluşturmayı zamanla* özelliğini kullanabilmeniz için sisteminizde etkinleştirmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="05cc6-109">Before you can use the *Schedule work creation* feature, it must be turned on in your system.</span></span> <span data-ttu-id="05cc6-110">Yöneticiler özellik durumunu denetlemek ve gerekirse etkinleştirmek için [özellik yönetimi](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) çalışma alanını kullanabilir.</span><span class="sxs-lookup"><span data-stu-id="05cc6-110">Admins can use the [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) workspace to check the status of the feature and turn it on if it's required.</span></span> <span data-ttu-id="05cc6-111">Burada, özellik aşağıdaki şekilde listelenmiştir:</span><span class="sxs-lookup"><span data-stu-id="05cc6-111">There, the feature is listed in the following way:</span></span>

- <span data-ttu-id="05cc6-112">**Modül:** *Ambar yönetimi*</span><span class="sxs-lookup"><span data-stu-id="05cc6-112">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="05cc6-113">**Özellik adı:** *İş oluşturmayı zamanla*</span><span class="sxs-lookup"><span data-stu-id="05cc6-113">**Feature name:** *Schedule work creation*</span></span>

> [!NOTE]
> <span data-ttu-id="05cc6-114">*İşi oluşturmayı zamanla* özelliğini etkinleştirebilmeniz için *Kuruluş çapında işi engelleme* özelliğinin etkin olması gerekir.</span><span class="sxs-lookup"><span data-stu-id="05cc6-114">The *Organization-wide work blocking* feature must be enabled before you can enable *Schedule work creation*.</span></span>

### <a name="manually-enable-batch-processing-of-waves"></a><span data-ttu-id="05cc6-115">Dalgaların toplu işlenmesini etkinleştirme</span><span class="sxs-lookup"><span data-stu-id="05cc6-115">Manually enable batch processing of waves</span></span>

<span data-ttu-id="05cc6-116">Ambar işi oluştururken paralel zaman uyumsuz yöntemden yararlanmak için dalga işleminizin toplu iş olarak çalışıyor olması gerekir.</span><span class="sxs-lookup"><span data-stu-id="05cc6-116">To take advantage of a parallel asynchronous method to create warehouse work, your wave process must be running in batch.</span></span> <span data-ttu-id="05cc6-117">Bunu ayarlamak için:</span><span class="sxs-lookup"><span data-stu-id="05cc6-117">To set this up:</span></span>

1. <span data-ttu-id="05cc6-118"> *\*Ambar yönetimi \> Kurulum \> Ambar yönetimi parametreleri*\*'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="05cc6-118">Go to **Warehouse management \> Setup \> Warehouse management parameters**.</span></span>

1. <span data-ttu-id="05cc6-119">**Genel** sekmesinde, **Dalgaları toplu iş halinde işle** seçeneğini *Evet* olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="05cc6-119">On the **General** tab, set **Process waves in batch** to *Yes*.</span></span> <span data-ttu-id="05cc6-120">İsteğe bağlı olarak, toplu iş kuyruğu işlemenin diğer işlemlerle aynı anda çalışmasını önlemek için özel bir **Dalga işleme toplu iş grubu** da seçebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="05cc6-120">Optionally, you can also select a dedicated **Wave processing batch group** to prevent your batch queue processing from running at the same time as other processes.</span></span>

1. <span data-ttu-id="05cc6-121">Sistem, aynı anda birden fazla dalga işlerken geçerli olan **Kilit süresini bekle (ms)** özelliğini de ayarlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="05cc6-121">Set the **Wait for lock (ms) time**, which applies when the system is processing several waves at the same time.</span></span> <span data-ttu-id="05cc6-122">Daha uzun dalga işlemleri için *60000* değerini öneririz.</span><span class="sxs-lookup"><span data-stu-id="05cc6-122">For most larger waving processes, we recommend a value of *60000*.</span></span>

### <a name="manually-enable-the-new-wave-step-method-for-existing-wave-templates"></a><span data-ttu-id="05cc6-123">Mevcut dalga şablonları için yeni dalga adımı yöntemini el ile etkinleştirme</span><span class="sxs-lookup"><span data-stu-id="05cc6-123">Manually enable the new wave step method for existing wave templates</span></span>

<span data-ttu-id="05cc6-124">Yeni dalga adımı yöntemini oluşturarak ve bu yöntemi paralel zaman uyumsuz görev işleme için etkinleştirerek başlayın.</span><span class="sxs-lookup"><span data-stu-id="05cc6-124">Start by creating the new wave step method and enabling it for parallel asynchronous task processing.</span></span>

1. <span data-ttu-id="05cc6-125"> *\*Ambar yönetimi \>Kurulum \> Dalgalar \> Dalga işleme yöntemleri*\*'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="05cc6-125">Go to **Warehouse management \> Setup \> Waves \> Wave process methods**.</span></span>

1. <span data-ttu-id="05cc6-126"> *\*Yöntemi yeniden oluştur*\*'u seçin; \*WHSScheduleWorkCreationWaveStepMethod* yönteminin sevkiyat dalga şablonlarınızda kullanabileceğiniz dalga işleme yöntemleri listesine eklendiğini görürsünüz.</span><span class="sxs-lookup"><span data-stu-id="05cc6-126">Select  **Regenerate method** and note that *WHSScheduleWorkCreationWaveStepMethod* has been added to the list of wave process methods you can use in your shipping wave templates.</span></span>

1. <span data-ttu-id="05cc6-127">*WHSScheduleWorkCreationWaveStepMethod* **Yöntem adı**'na sahip kaydı seçin ve **Görev yapılandırması**'nı seçin.</span><span class="sxs-lookup"><span data-stu-id="05cc6-127">Select the record with the **Method name** *WHSScheduleWorkCreationWaveStepMethod* and select **Task configuration**.</span></span>

1. <span data-ttu-id="05cc6-128">Izgaraya yeni satır eklemek için Eylem Bölmesinde **Yeni**'yi seçin ve aşağıdaki ayarları kullanın:</span><span class="sxs-lookup"><span data-stu-id="05cc6-128">To add a new row to the grid, select **New** on the Action Pane and use the following settings:</span></span>

    - <span data-ttu-id="05cc6-129">**Ambar**: İş oluşturma işlemesini zamanlamak için kullanacağınız ambarı seçin.</span><span class="sxs-lookup"><span data-stu-id="05cc6-129">**Warehouse** - Select the warehouse you will use to schedule work creation processing.</span></span>

    - <span data-ttu-id="05cc6-130">**Maksimum toplu görev sayısı**: Maksimum toplu görev sayısını belirtin.</span><span class="sxs-lookup"><span data-stu-id="05cc6-130">**Maximum number of batch tasks** - Specify a maximum number of batch tasks.</span></span> <span data-ttu-id="05cc6-131">Çoğu durumda bu değer 8-16 aralığında olmalıdır, ancak senaryolarınıza göre en iyi ayarı denemeniz önerilir.</span><span class="sxs-lookup"><span data-stu-id="05cc6-131">In most cases, this value should be in the range from 8-16, however we recommend that you experiment with the optimal setting based on your scenarios.</span></span>

    - <span data-ttu-id="05cc6-132">**Dalga işleme toplu iş grubu**: Toplu iş kuyruğu işlemenizi iyileştirmek için özel bir dalga işleme toplu iş grubu seçin.</span><span class="sxs-lookup"><span data-stu-id="05cc6-132">**Wave processing batch group** - Select a dedicated wave processing batch group to optimize your batch queue processing.</span></span>

<span data-ttu-id="05cc6-133">Şimdi, *İş oluşturmayı zamanla* dalga işleme yöntemini kullanmak için mevcut bir dalga şablonunu güncelleştirmeye hazırsınız (veya yeni bir tane oluşturabilirsiniz).</span><span class="sxs-lookup"><span data-stu-id="05cc6-133">Now you are ready to update an existing wave template (or create a new one) to use the *Schedule work creation* wave processing method.</span></span>

1. <span data-ttu-id="05cc6-134"> *\*Ambar yönetimi \> Kurulum \> Dalgalar \> Dalga şablonları*\*'na gidin.</span><span class="sxs-lookup"><span data-stu-id="05cc6-134">Go to **Warehouse management \> Setup \> Waves \> Wave templates**.</span></span>

1. <span data-ttu-id="05cc6-135">Eylem Bölmesinde, **Düzenle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="05cc6-135">Select **Edit** on the Action Pane.</span></span>

1. <span data-ttu-id="05cc6-136">Liste bölmesinde, güncelleştirmek istediğiniz dalga şablonunu seçin (tanıtım verilerini kullanarak test ediyorsanız, *24 Sevkiyat varsayılan*'ı kullanabilirsiniz).</span><span class="sxs-lookup"><span data-stu-id="05cc6-136">In the list pane, select the wave template you would like to update (if you are testing using demo data, then you could use *24 Shipping default*).</span></span>

1. <span data-ttu-id="05cc6-137">**Yöntemler** hızlı sekmesini genişletin ve **Kalan yöntemler** ızgarasında *İş oluşturmayı zamanla* **Adı**'na sahip satırı seçin.</span><span class="sxs-lookup"><span data-stu-id="05cc6-137">Expand the **Methods** FastTab and select the row with the **Name** *Schedule work creation* in the **Remaining methods** grid.</span></span>

1. <span data-ttu-id="05cc6-138">Seçili satırı ilgili sütuna taşımak için **Seçili yöntemler** sütununu işaret eden oku seçin.</span><span class="sxs-lookup"><span data-stu-id="05cc6-138">Select the arrow pointing to the **Selected methods** column to move the selected row to that column.</span></span> <span data-ttu-id="05cc6-139">(Bir seferde yalnızca *WHSScheduleWorkCreationWaveStepMethod* veya *createWork* yöntemini kullanan seçili bir yönteminiz olabilir. Bu nedenle, *createWork* **Yöntem adı**'na sahip mevcut satır otomatik olarak **Kalan yöntemler** ızgarasına taşınır.)</span><span class="sxs-lookup"><span data-stu-id="05cc6-139">(You can only have one selected method at a time that uses either *WHSScheduleWorkCreationWaveStepMethod* or *createWork*, so the existing row with **Method name** *createWork* is automatically moved to the **Remaining methods** grid.)</span></span>

## <a name="set-wave-task-processing-threshold-data"></a><span data-ttu-id="05cc6-140">Dalga görevi işleme eşik verilerini ayarla</span><span class="sxs-lookup"><span data-stu-id="05cc6-140">Set wave task processing threshold data</span></span>

<span data-ttu-id="05cc6-141">Dalga işlemi ilk kez görev tabanlı işleme kullanarak çalıştırıldığında sistem, varsayılan dalga görevi işleme eşik değeri oluşturur.</span><span class="sxs-lookup"><span data-stu-id="05cc6-141">The system will create default wave task processing threshold data the first time a wave process runs using any task-based processing.</span></span> <span data-ttu-id="05cc6-142">Bu veri, dalga işleminin zaman uyumsuz olarak çalıştırıldığı ve görev tabanlı olduğu durumları kontrol etmek için kullanılır. Bu da işi paralel olarak işlemesini ve oluşturmasını sağlar.</span><span class="sxs-lookup"><span data-stu-id="05cc6-142">The data is used to control when wave processing will run asynchronously and be task-based, which enables it to process and create work in parallel.</span></span>

<span data-ttu-id="05cc6-143">Varsayılan veriler, ilk başta minimum yük satırı sayısı olarak 15 eşik değerini kullanacaktır (MINIMUMWAVELOADLINES).</span><span class="sxs-lookup"><span data-stu-id="05cc6-143">The default data will initially use a threshold value of 15 for the minimum number of load lines (MINIMUMWAVELOADLINES).</span></span> <span data-ttu-id="05cc6-144">Bu, sistemin 15 yük satırından fazlasını içeren bir dalgayı işlediğinde zaman uyumsuz görev işlemeyi kullanacağı anlamına gelir.</span><span class="sxs-lookup"><span data-stu-id="05cc6-144">This means that when the system processes a wave with more than 15 loads lines, it will use asynchronous task processing.</span></span> <span data-ttu-id="05cc6-145">Test ortamlarınızda **WHSWaveTaskProcessingThresholdParameters** tablosundaki bu veriyi el ile ekleyebilirsiniz/güncelleştirebilirsiniz ancak bu ayarı üretim ortamında değiştirmeniz gerekirse güncelleştirmeyi istemek için Microsoft Desteği ile iletişim kurmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="05cc6-145">You can manually insert/update this data in the **WHSWaveTaskProcessingThresholdParameters** table in your test environments, but if you need to change this setting in a production environment, you must contact Microsoft Support to request the update.</span></span>

## <a name="work-with-the-feature"></a><span data-ttu-id="05cc6-146">Özellik ile çalışma</span><span class="sxs-lookup"><span data-stu-id="05cc6-146">Work with the feature</span></span>

<span data-ttu-id="05cc6-147">*İş oluşturmayı zamanla* işlevi etkinleştirildiğinde dalga işleme, planlı iş oluşturacaktır. Bu da daha sonra yeni iş oluşturma işlemi tarafından kullanılacaktır.</span><span class="sxs-lookup"><span data-stu-id="05cc6-147">When the *Schedule work creation* functionality is enabled, wave processing will create planned work, which will eventually be used by the new work creation process.</span></span> <span data-ttu-id="05cc6-148">İş oluşturma sırasında iş, *Kuruluş genelinde iş engelleme* özelliği kullanılarak engellenir.</span><span class="sxs-lookup"><span data-stu-id="05cc6-148">During work creation, the work will be blocked using the *Organization-wide work blocking* feature.</span></span>

<span data-ttu-id="05cc6-149">Aşağıdaki akış çizelgesi, dalga işleme sırasında planlanan işin nasıl oluşturulduğunu gösterir.</span><span class="sxs-lookup"><span data-stu-id="05cc6-149">The following flowchart shows how planned work is created during wave processing.</span></span>

![İş oluşturmayı planla](media/schedule-work-creation-process.png)

### <a name="planned-work"></a><span data-ttu-id="05cc6-151">Planlı iş</span><span class="sxs-lookup"><span data-stu-id="05cc6-151">Planned work</span></span>

<span data-ttu-id="05cc6-152">**Planlı iş ayrıntıları** sayfası (**Ambar yönetimi \> İş \> Planlı iş ayrıntıları**), dalga işleme sırasında oluşturulan planlı iş hakkında bilgiler gösterir.</span><span class="sxs-lookup"><span data-stu-id="05cc6-152">The **Planned work details** page (**Warehouse management \> Work \> Planned work details**) shows information about the planned work, which is initially created during wave processing.</span></span> <span data-ttu-id="05cc6-153">Aşağıdaki **İşleme durumu** değerleri mevcuttur:</span><span class="sxs-lookup"><span data-stu-id="05cc6-153">The following **Process status** values are available:</span></span>

- <span data-ttu-id="05cc6-154">**Sıraya Alındı**: Planlanan iş, iş oluşturmak için kullanılmak üzere bekliyor.</span><span class="sxs-lookup"><span data-stu-id="05cc6-154">**Queued** - The planned work is waiting to be used to create work.</span></span>
- <span data-ttu-id="05cc6-155">**Tamamlandı**: Planlanan iş, iş oluşturmak için kullanıldı.</span><span class="sxs-lookup"><span data-stu-id="05cc6-155">**Completed** - The planned work has been used to create work.</span></span>
- <span data-ttu-id="05cc6-156">**Başarısız**: Dalga işleme başarısız oldu.</span><span class="sxs-lookup"><span data-stu-id="05cc6-156">**Failed** – The wave processing has failed.</span></span> <span data-ttu-id="05cc6-157">Planlı işin, ilgili gerçek iş olup olmadığına bakılmaksızın **Başarısız** durumunda olabileceğini unutmayın.</span><span class="sxs-lookup"><span data-stu-id="05cc6-157">Note that the planned work can be in a **Failed** state with or without related actual work.</span></span> <span data-ttu-id="05cc6-158">Asıl iş oluşturma işlemi başarısız olduğunda asıl iş, *İptal edildi* durumunda kalır.</span><span class="sxs-lookup"><span data-stu-id="05cc6-158">When the actual work creation process fails, the actual work remains in status *Cancelled*.</span></span>

### <a name="batch-job-for-the-work-creation-process"></a><span data-ttu-id="05cc6-159">İş oluşturma işlemi için toplu iş</span><span class="sxs-lookup"><span data-stu-id="05cc6-159">Batch job for the work creation process</span></span>

<span data-ttu-id="05cc6-160">Dalgaları işlemeye yönelik toplu işleri görüntülemek için **Tüm dalgalar** sayfasındaki Eylem Bölmesinde **Toplu işler**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="05cc6-160">To view the batch jobs for processing waves, select **Batch jobs** on the Action Pane on the **All waves** page.</span></span>

<span data-ttu-id="05cc6-161">Buradan, toplu iş kodlarının her biri için tüm toplu görev ayrıntılarını görüntüleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="05cc6-161">From here, you can view all the batch task details for each of the batch job IDs.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]