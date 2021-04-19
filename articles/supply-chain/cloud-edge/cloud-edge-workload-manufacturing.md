---
title: Bulut ve uç ölçek birimleri için üretim yürütme iş yükleri
description: Bu konuda, üretim yürütme iş yüklerinin bulut ve edge ölçek birimleri ile nasıl çalıştığı açıklanmaktadır.
author: cabeln
ms.date: 10/06/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: SCM
ms.author: cabeln
ms.search.validFrom: 2020-10-06
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: a8c263104e209a81e33ea0db9e5fecddff3bc95b
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/01/2021
ms.locfileid: "5809794"
---
# <a name="manufacturing-execution-workloads-for-cloud-and-edge-scale-units"></a><span data-ttu-id="9e2f2-103">Bulut ve uç ölçek birimleri için üretim yürütme iş yükleri</span><span class="sxs-lookup"><span data-stu-id="9e2f2-103">Manufacturing execution workloads for cloud and edge scale units</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

> [!WARNING]
> <span data-ttu-id="9e2f2-104">İş yükü ölçek birimleri kullanıldığında, genel önizlemedeki bazı iş işlevleri tam olarak desteklenmez.</span><span class="sxs-lookup"><span data-stu-id="9e2f2-104">Some business functionality isn't fully supported in the public preview when workload scale units are used.</span></span>

<span data-ttu-id="9e2f2-105">Üretim yürütmede, bulut ve edge ölçek birimleri, ölçek hub'a bağlı olmasalar bile aşağıdaki özellikleri sağlar:</span><span class="sxs-lookup"><span data-stu-id="9e2f2-105">In manufacturing execution, cloud and edge scale units deliver the following capabilities, even when edge units aren't connected to the hub:</span></span>

- <span data-ttu-id="9e2f2-106">Makine operatörleri ve üretim katı denetçileri operasyonel üretim planına erişebilirler.</span><span class="sxs-lookup"><span data-stu-id="9e2f2-106">Machine operators and shop floor supervisors can access the operational production plan.</span></span>
- <span data-ttu-id="9e2f2-107">Makine operatörleri, gizli ve süreç üretim işleri çalıştırarak planı güncel tutabilir.</span><span class="sxs-lookup"><span data-stu-id="9e2f2-107">Machine operators can keep the plan up to date by running discrete and process manufacturing jobs.</span></span>
- <span data-ttu-id="9e2f2-108">Üretim katı denetçisi, çalışma planını ayarlayabilir.</span><span class="sxs-lookup"><span data-stu-id="9e2f2-108">The shop floor supervisor can adjust the operational plan.</span></span>
- <span data-ttu-id="9e2f2-109">Çalışanlar, doğru çalışan maaşı hesaplamasını sağlamak için kenardan giriş ve çıkış zamanlarına erişebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="9e2f2-109">Workers can access time and attendance for clock-in and clock-out on the edge, to ensure correct worker pay calculation.</span></span>

<span data-ttu-id="9e2f2-110">Bu konuda, üretim yürütme iş yüklerinin bulut ve edge ölçek birimleri ile nasıl çalıştığı açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="9e2f2-110">This topic describes how manufacturing execution workloads work with cloud and edge scale units.</span></span>

## <a name="the-manufacturing-lifecycle"></a><span data-ttu-id="9e2f2-111">Üretim yaşam döngüsü</span><span class="sxs-lookup"><span data-stu-id="9e2f2-111">The manufacturing lifecycle</span></span>

<span data-ttu-id="9e2f2-112">Aşağıdaki çizimin gösterdiği gibi, üretim yaşam döngüsü üç aşamaya ayrılmıştır: *Planlama*, *Çalıştırma* ve *Sonuçlandırma*.</span><span class="sxs-lookup"><span data-stu-id="9e2f2-112">As the following illustration shows, the manufacturing lifecycle is divided into three phases: *Plan*, *Execute*, and *Finalize*.</span></span>

<span data-ttu-id="9e2f2-113">[![Tek bir ortam kullanıldığında üretim yürütme aşamaları](media/mes-phases.png "Tek bir ortam kullanıldığında üretim yürütme aşamaları")](media/mes-phases-large.png)</span><span class="sxs-lookup"><span data-stu-id="9e2f2-113">[![Manufacturing execution phases when a single environment is used](media/mes-phases.png "Manufacturing execution phases when a single environment is used")](media/mes-phases-large.png)</span></span>

<span data-ttu-id="9e2f2-114">_Planlama_ aşaması; ürün tanımı, planlama, sipariş oluşturma ve zamanlama ile serbest bırakma bilgilerini içerir.</span><span class="sxs-lookup"><span data-stu-id="9e2f2-114">The _Plan_ phase includes product definition, planning, order creation and scheduling, and release.</span></span> <span data-ttu-id="9e2f2-115">Serbest bırakma adımı; _Planlama_ aşamasından _Yürütme_ aşamasına geçişin nasıl yapılacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="9e2f2-115">The release step indicates the transition from the _Plan_ phase to the _Execute_ phase.</span></span> <span data-ttu-id="9e2f2-116">Bir üretim emri serbest bırakıldığında, üretim emri işleri üretim katında görünür ve yürütülmeye hazırdır.</span><span class="sxs-lookup"><span data-stu-id="9e2f2-116">When a production order is released, the production order jobs will be visible on the production floor and ready for execution.</span></span>

<span data-ttu-id="9e2f2-117">Bir üretim işi tamamlandı olarak işaretlendiğinde, _Yürütme_ aşamasından _Sonlandırma_ aşamasına kadar hareket eder.</span><span class="sxs-lookup"><span data-stu-id="9e2f2-117">When a production job is marked as completed, it moves from the _Execute_ phase to the _Finalize_ phase.</span></span> <span data-ttu-id="9e2f2-118">_Sonlandırma_ aşamasında, *Yürütme* aşamasındaki kayıtlar hesaplandıkları, onaylandıkları ve transfer edildikleri bir onay iş akışından geçer.</span><span class="sxs-lookup"><span data-stu-id="9e2f2-118">In the _Finalize_ phase, the registrations from the *Execute* phase go through an approval workflow, where they are calculated, approved, and transferred.</span></span> <span data-ttu-id="9e2f2-119">Bu noktada, üretim emri tamamlanır.</span><span class="sxs-lookup"><span data-stu-id="9e2f2-119">At that point, the production order is completed.</span></span> <span data-ttu-id="9e2f2-120">Bu nedenle, çalışanların ödemeleri için temel üretilir.</span><span class="sxs-lookup"><span data-stu-id="9e2f2-120">Therefore, the basis for the workers' pay is generated.</span></span>

## <a name="splitting-the-execute-phase-into-a-separate-workload"></a><span data-ttu-id="9e2f2-121">Yürütme aşamasını ayrı bir iş yüküne bölme</span><span class="sxs-lookup"><span data-stu-id="9e2f2-121">Splitting the Execute phase into a separate workload</span></span>

<span data-ttu-id="9e2f2-122">Aşağıdaki çizimin gösterdiği gibi, ölçek birimleri kullanıldığında, _Yürütme_ aşaması ayrı bir iş yükü olarak bölünür.</span><span class="sxs-lookup"><span data-stu-id="9e2f2-122">As the following illustration shows, when scale units are used, the _Execute_ phase is split out as a separate workload.</span></span>

<span data-ttu-id="9e2f2-123">[![Ölçek birimleri kullanıldığında üretim yürütme aşamaları](media/mes-phases-workloads.png "Ölçek birimleri kullanıldığında üretim yürütme aşamaları")](media/mes-phases-workloads-large.png)</span><span class="sxs-lookup"><span data-stu-id="9e2f2-123">[![Manufacturing execution phases when scale units are used](media/mes-phases-workloads.png "Manufacturing execution phases when scale units are used")](media/mes-phases-workloads-large.png)</span></span>

<span data-ttu-id="9e2f2-124">Model şimdi tek örnekli bir yüklemeden hub ve ölçek birimlerine dayalı bir modele geçer.</span><span class="sxs-lookup"><span data-stu-id="9e2f2-124">The model now goes from a single-instance installation to a model that is based on the hub and scale units.</span></span> <span data-ttu-id="9e2f2-125">_Planlama_ ve _Sonlandırma_ aşamaları, hub'da arka ofis işlemleri olarak çalışır ve üretim yürütme iş yükü ölçek birimleri üzerinde çalışır.</span><span class="sxs-lookup"><span data-stu-id="9e2f2-125">The _Plan_ and _Finalize_ phases run as back-office operations on the hub, and the manufacturing execution workload runs on the scale units.</span></span> <span data-ttu-id="9e2f2-126">Veriler, hub ve ölçek birimleri arasında zaman uyumsuz olarak aktarılır.</span><span class="sxs-lookup"><span data-stu-id="9e2f2-126">Data is transferred asynchronously between the hub and scale units.</span></span>

<span data-ttu-id="9e2f2-127">Bir üretim emri hub üzerinde serbest bırakıldığında, üretim işlerini işlemek için gereken tüm veriler ölçek birimine aktarılır.</span><span class="sxs-lookup"><span data-stu-id="9e2f2-127">When a production order is released on the hub, all data that is required to process production jobs is transferred to the scale unit.</span></span> <span data-ttu-id="9e2f2-128">Bu veriler üretim emirlerini, üretim rotalarını, ürün reçetelerini ve ürünleri içerir.</span><span class="sxs-lookup"><span data-stu-id="9e2f2-128">This data includes production orders, production routes, bills of materials, and products.</span></span> <span data-ttu-id="9e2f2-129">Bir üretim emriyle (dolaylı faaliyetler, devamsızlık kodları ve üretim parametreleri gibi) ilgili olmayan veriler de hub'dan ölçek birimine transfer edilir.</span><span class="sxs-lookup"><span data-stu-id="9e2f2-129">Data that isn't related to a production order (such as indirect activities, absence codes, and production parameters) is also transferred from the hub to the scale unit.</span></span> <span data-ttu-id="9e2f2-130">Kural olarak, hub'dan kaynaklanan ve ölçek birimine aktarılan veriler yalnızca hub'da oluşturulabilir veya güncelleştirilebilir.</span><span class="sxs-lookup"><span data-stu-id="9e2f2-130">As a rule, data that originates from the hub and that is transferred to the scale unit can be created or updated only on the hub.</span></span> <span data-ttu-id="9e2f2-131">Örneğin, ölçek biriminde yeni bir devamsızlık kodu veya dolaylı faaliyet oluşturulamaz,&mdash;bunlar yalnızca kayıt için kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="9e2f2-131">For example, a new absence code or indirect activity can't be created on the scale unit&mdash;they can be used only for registration.</span></span> <span data-ttu-id="9e2f2-132">Yürütme sırasında ölçek biriminde yapılan kayıtlar, zaman ve katılımcı onayı, stok ve mali güncelleştirmelerin işlendiği hub'a aktarılır.</span><span class="sxs-lookup"><span data-stu-id="9e2f2-132">The registrations that are made on the scale unit during execution are then transferred to the hub, where time and attendance approval, inventory, and financial updates are processed.</span></span>

## <a name="manufacturing-execution-tasks-that-can-be-run-on-workloads"></a><span data-ttu-id="9e2f2-133">İş yükleri üzerinde çalıştırılabilecek üretim yürütme görevleri</span><span class="sxs-lookup"><span data-stu-id="9e2f2-133">Manufacturing execution tasks that can be run on workloads</span></span>

<span data-ttu-id="9e2f2-134">Aşağıdaki üretim yürütme görevleri, şu anda iş yükleri üzerinde ölçek birimleri kullanıldığında çalışabilir:</span><span class="sxs-lookup"><span data-stu-id="9e2f2-134">The following manufacturing execution tasks can currently be run on workloads when scale units are used:</span></span>

- <span data-ttu-id="9e2f2-135">Giriş, oturum açma, çıkış ve devamsızlık</span><span class="sxs-lookup"><span data-stu-id="9e2f2-135">Clock-in, log-in, clock-out, and absence</span></span>
- <span data-ttu-id="9e2f2-136">İşi başlat</span><span class="sxs-lookup"><span data-stu-id="9e2f2-136">Start job</span></span>
- <span data-ttu-id="9e2f2-137">Paket işleri</span><span class="sxs-lookup"><span data-stu-id="9e2f2-137">Bundle jobs</span></span>
- <span data-ttu-id="9e2f2-138">Rapor ilerlemesi</span><span class="sxs-lookup"><span data-stu-id="9e2f2-138">Report progress</span></span>
- <span data-ttu-id="9e2f2-139">Iskarta bildir</span><span class="sxs-lookup"><span data-stu-id="9e2f2-139">Report scrap</span></span>
- <span data-ttu-id="9e2f2-140">Dolaylı faaliyet</span><span class="sxs-lookup"><span data-stu-id="9e2f2-140">Indirect activity</span></span>
- <span data-ttu-id="9e2f2-141">Mola</span><span class="sxs-lookup"><span data-stu-id="9e2f2-141">Break</span></span>

## <a name="working-with-manufacturing-execution-workloads-on-the-hub"></a><span data-ttu-id="9e2f2-142">Hub'da üretim yürütme iş yükleri ile çalışma</span><span class="sxs-lookup"><span data-stu-id="9e2f2-142">Working with manufacturing execution workloads on the hub</span></span>

<span data-ttu-id="9e2f2-143">Genellikle, üretim yürütme iş yüklerini çalıştırmak için gereken süreçler, gerektiğinde hub'ı ve tüm ölçek birimlerini eşit tutmak için otomatik olarak çalışır.</span><span class="sxs-lookup"><span data-stu-id="9e2f2-143">Usually, the processes that are required to run manufacturing execution workloads run automatically to keep the hub and all the scale units in sync, as needed.</span></span> <span data-ttu-id="9e2f2-144">Ancak sorununuz varsa, iş yüklerinden alınan ham kayıtların işlenmesini el ile tetikleyebilir ve/veya kayıt işleme günlüğünü kontrol edebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="9e2f2-144">However, if you're having trouble, you can manually trigger the processing of raw registrations that are received from workloads and/or check the registration processing log.</span></span>

### <a name="manually-process-raw-registrations"></a><span data-ttu-id="9e2f2-145">Ham kayıtları el ile işleme</span><span class="sxs-lookup"><span data-stu-id="9e2f2-145">Manually process raw registrations</span></span>

<span data-ttu-id="9e2f2-146">İş yüklerinden alınan tüm kayıtları işlemek için Supply Chain Management'ta bir toplu işlem otomatik olarak çalışır.</span><span class="sxs-lookup"><span data-stu-id="9e2f2-146">A batch job in Supply Chain Management runs automatically to process all the registrations that have been received from the workloads.</span></span> <span data-ttu-id="9e2f2-147">İş yükü üzerinde tamamlanmış bir proje için bir kayıt işlenirken, bu iş gerekli üretim günlüklerini ve günlük defteri girişlerini oluşturur.</span><span class="sxs-lookup"><span data-stu-id="9e2f2-147">This job creates the required production journals and logbook entries when a registration is processed for a completed job on the workload.</span></span>

<span data-ttu-id="9e2f2-148">İş genellikle otomatik olarak çalışmasına rağmen, hub'da oturum açıp **Üretim denetimi \> Periyodik görevler \> Arka ofis iş yükü yönetimi \> Ham kayıtları işleme**'ye giderek istediğiniz zaman el ile çalıştırabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="9e2f2-148">Although the job usually runs automatically, you can run it manually at any time by signing in to the hub and going to **Production control \> Periodic tasks \> Backoffice workload management \> Process raw registrations**.</span></span>

### <a name="check-the-raw-registration-processing-log"></a><span data-ttu-id="9e2f2-149">Ham kayıt işlem günlüğünü denetleme</span><span class="sxs-lookup"><span data-stu-id="9e2f2-149">Check the raw registration processing log</span></span>

<span data-ttu-id="9e2f2-150">Kayıt işleme günlüğünü gözden geçirmek için hub'da oturum açın ve **Üretim denetimi \> Periyodik görevler \> Arka ofis iş yükü yönetimi \> Ham kayıt işleme günlüğü**'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="9e2f2-150">To review the registration processing log, sign in to the hub, and go to **Production control \> Periodic tasks \> Backoffice workload management \> Raw registration processing log**.</span></span> <span data-ttu-id="9e2f2-151">**Ham kayıt işleme günlüğü** sayfası, işlenen ham kayıtların bir listesini ve her kaydın durumunu gösterir.</span><span class="sxs-lookup"><span data-stu-id="9e2f2-151">The **Raw registration processing log** page shows a list of processed raw registrations and the status of each registration.</span></span>

<span data-ttu-id="9e2f2-152">![Ham kayıt işlem günlüğü sayfası](media/mes-processing-log.png "Ham kayıt işlem günlüğü sayfası")</span><span class="sxs-lookup"><span data-stu-id="9e2f2-152">![Raw registration processing log page](media/mes-processing-log.png "Raw registration processing log page")</span></span>

<span data-ttu-id="9e2f2-153">Listede herhangi bir kayıt seçip Eylem bölmesinden aşağıdaki düğmelerden birini seçerek çalışabilirsiniz:</span><span class="sxs-lookup"><span data-stu-id="9e2f2-153">You can work on any registration in the list by selecting it and then selecting one of the following buttons on the Action Pane:</span></span>

- <span data-ttu-id="9e2f2-154">**İşle**: Seçilen kaydı el ile işleyin.</span><span class="sxs-lookup"><span data-stu-id="9e2f2-154">**Process** – Manually process the selected registration.</span></span> <span data-ttu-id="9e2f2-155">Bu eylem, _Ham kayıtları işle_ işi çalıştırılmamışsa veya başarısız olduğunda yararlı olabilir.</span><span class="sxs-lookup"><span data-stu-id="9e2f2-155">This action can be useful if the _Process raw registrations_ job hasn't run, or if it failed.</span></span>
- <span data-ttu-id="9e2f2-156">**İptal et**: Seçili kaydı iptal edin.</span><span class="sxs-lookup"><span data-stu-id="9e2f2-156">**Cancel** – Cancel the selected registration.</span></span>

## <a name="working-with-manufacturing-execution-workloads-on-a-scale-unit"></a><span data-ttu-id="9e2f2-157">Bir ölçek biriminde üretim yürütme iş yükleri ile çalışma</span><span class="sxs-lookup"><span data-stu-id="9e2f2-157">Working with manufacturing execution workloads on a scale unit</span></span>

<span data-ttu-id="9e2f2-158">Genellikle, üretim yürütme iş yüklerini çalıştırmak için gereken süreçler, gerektiğinde hub'ı ve tüm ölçek birimlerini eşit tutmak için otomatik olarak çalışır.</span><span class="sxs-lookup"><span data-stu-id="9e2f2-158">Usually, the processes that are required to run manufacturing execution workloads run automatically to keep the hub and all the scale units in sync, as needed.</span></span> <span data-ttu-id="9e2f2-159">Ancak sorun yaşıyorsanız bir ölçek biriminde işlenmiş olan siparişlerin geçmişini denetleyebilir veya _Üretim hub'ından ölçek birimi ileti işleyici_ işini el ile çalıştırabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="9e2f2-159">However, if you're having trouble, you can check the history of orders that have been processed on a scale unit or manually run the _Manufacturing hub to scale unit message processor_ job.</span></span>

### <a name="view-the-history-of-manufacturing-jobs-that-have-been-processed-on-a-scale-unit"></a><span data-ttu-id="9e2f2-160">Bir ölçek biriminde işlenmiş olan üretim işlerinin geçmişini görüntüleme</span><span class="sxs-lookup"><span data-stu-id="9e2f2-160">View the history of manufacturing jobs that have been processed on a scale unit</span></span>

<span data-ttu-id="9e2f2-161">Bir ölçek biriminde işlenmiş olan üretim işlerinin geçmişini gözden geçirmek için ölçek birimi makinesinde oturum açın ve **Üretim denetimi \> Periyodik görevler \> Arka ofis iş yükü yönetimi \> Üretim işleri işlem geçmişi**'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="9e2f2-161">To review the history of manufacturing jobs that have been processed on a scale unit, sign in to the scale unit machine, and go to **Production control \> Periodic tasks \> Backoffice workload management \> Manufacturing jobs processing history**.</span></span> <span data-ttu-id="9e2f2-162">**Üretim işleri işleme geçmişi** sayfası, ölçek birimindeki üretim emirlerinin işlem geçmişini gösterir.</span><span class="sxs-lookup"><span data-stu-id="9e2f2-162">The **Manufacturing jobs processing history** page shows the processing history of the production orders on the scale unit.</span></span> <span data-ttu-id="9e2f2-163">Listeden herhangi bir üretim emri seçip Eylem bölmesinden aşağıdaki düğmelerden birini seçerek çalışabilirsiniz:</span><span class="sxs-lookup"><span data-stu-id="9e2f2-163">You can work on any production order in the list by selecting it and then selecting one of the following buttons on the Action Pane:</span></span>

- <span data-ttu-id="9e2f2-164">**İşle**: Seçilen üretim emrini el ile işleyin.</span><span class="sxs-lookup"><span data-stu-id="9e2f2-164">**Process** – Manually process the selected production order.</span></span>
- <span data-ttu-id="9e2f2-165">**İptal et**: Seçilen üretim emrini iptal edin.</span><span class="sxs-lookup"><span data-stu-id="9e2f2-165">**Cancel** – Cancel the selected production order.</span></span>

### <a name="manufacturing-hub-to-scale-unit-message-processor-job"></a><span data-ttu-id="9e2f2-166">Üretim hub'ından ölçek birimine ileti işleyici işi</span><span class="sxs-lookup"><span data-stu-id="9e2f2-166">Manufacturing hub to scale unit message processor job</span></span>

<span data-ttu-id="9e2f2-167">_Üretim hub'ından ölçek birimine ileti işleyicisi_ işi, hub'dan ölçek birimine giden verileri işler.</span><span class="sxs-lookup"><span data-stu-id="9e2f2-167">The _Manufacturing hub to scale unit message processor_ job processes data from the hub to the scale unit.</span></span> <span data-ttu-id="9e2f2-168">Üretim yürütme iş yükü dağıtıldığında bu iş otomatik olarak başlatılır.</span><span class="sxs-lookup"><span data-stu-id="9e2f2-168">This job is automatically started when the manufacturing execution workload is deployed.</span></span> <span data-ttu-id="9e2f2-169">Bununla birlikte, **Üretim denetimi \> Periyodik görevler \> Arka ofis iş yükü yönetimi \> Üretim hub'ından ölçek birimine ileti işleyici**'ye giderek istediğiniz zaman el ile çalıştırabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="9e2f2-169">However, you can run it manually at any time by going to **Production control \> Periodic tasks \> Backoffice workload management \> Manufacturing hub to scale unit message processor**.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]