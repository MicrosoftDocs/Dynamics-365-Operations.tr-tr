---
title: Ambar uygulaması olayları
description: Bu konu, toplu işin bir parçası olarak ambar uygulaması olay iletilerini işlemek için kullanılan ambar uygulaması olayını işlemeyi açıklamaktadır.
author: perlynne
manager: tfehr
ms.date: 09/02/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSMobileDeviceQueueEvent
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-10-09
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 0bafcbd5306860cb80d6e813aabf83853a9011c1
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5248655"
---
# <a name="warehouse-app-event-processing"></a><span data-ttu-id="68361-103">Ambar uygulaması olayı işleme</span><span class="sxs-lookup"><span data-stu-id="68361-103">Warehouse app event processing</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="68361-104">Supply Chain Management'ta çalışan toplu işler, sinyal verilen olaylara gerektiğinde tepki vermek üzere ambar uygulaması tarafından yayınlanan olayları işlemek için bir kuyruktaki verileri kullanabilir.</span><span class="sxs-lookup"><span data-stu-id="68361-104">Batch jobs running in Supply Chain Management can use data from a queue for processing events issued by the warehouse app to react as needed to the signaled events.</span></span> <span data-ttu-id="68361-105">Bu özellik, uygulamayı kullanan çalışanların yaptığı belirli eylem türlerine yanıt olarak kuyruğa ilgili olayları ekler.</span><span class="sxs-lookup"><span data-stu-id="68361-105">This feature add relevant events to the queue in response to certain types of actions taken by workers using the app.</span></span> <span data-ttu-id="68361-106">Örneğin, **Ambar uygulamasından transfer emirleri oluşturma ve işleme** özelliği kullanıldığında sistem **Ambar uygulaması olaylarını işle** toplu işini çalıştırırken transfer emri başlıkları ve satırları arkauçta oluşturulur ve güncelleştirilir.</span><span class="sxs-lookup"><span data-stu-id="68361-106">An example is when using the **Create and process transfer orders from the warehouse app** feature, the transfer order header and lines get created and updated in the back end when the system is running the **Process warehouse app events** batch job.</span></span>

## <a name="enable-the-process-warehouse-app-events-feature"></a><span data-ttu-id="68361-107">Ambarı uygulaması olaylarını işle özelliğini etkinleştirme</span><span class="sxs-lookup"><span data-stu-id="68361-107">Enable the Process warehouse app events feature</span></span>

<span data-ttu-id="68361-108">Bu özelliği kullanabilmeniz için sisteminizde etkinleştirmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="68361-108">Before you can use this feature, it must be enabled on your system.</span></span> <span data-ttu-id="68361-109">Yöneticiler özellik durumunu denetlemek ve gerekirse etkinleştirmek için [özellik yönetimi](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) sayfasını kullanabilir.</span><span class="sxs-lookup"><span data-stu-id="68361-109">Administrators can use the [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) page to check the feature status and enable it if needed.</span></span> <span data-ttu-id="68361-110">Ambarı uygulaması olaylarını işle özelliği şu şekilde listelenir:</span><span class="sxs-lookup"><span data-stu-id="68361-110">The Process warehouse app events feature is listed as:</span></span>

- <span data-ttu-id="68361-111">**Modül** - Ambar yönetimi</span><span class="sxs-lookup"><span data-stu-id="68361-111">**Module** - Warehouse management</span></span>
- <span data-ttu-id="68361-112">**Özellik adı** - Ambarı uygulaması olaylarını işle</span><span class="sxs-lookup"><span data-stu-id="68361-112">**Feature name** - Process warehouse app events</span></span>

## <a name="set-up-a-batch-job-to-process-warehouse-app-events"></a><span data-ttu-id="68361-113">Ambar uygulaması olaylarını işlemek için bir toplu iş ayarlayın</span><span class="sxs-lookup"><span data-stu-id="68361-113">Set up a batch job to process warehouse app events</span></span>

### <a name="process-warehouse-app-events"></a><span data-ttu-id="68361-114">Ambar uygulaması olaylarını işle</span><span class="sxs-lookup"><span data-stu-id="68361-114">Process warehouse app events</span></span>

<span data-ttu-id="68361-115">Transfer emri oluşturma ve satır güncelleştirmeleri için ambar uygulaması olaylarını işlemek üzere bir planlı toplu iş ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="68361-115">Set up a scheduled batch job to process the warehouse app events for the transfer order creation and line updates.</span></span>

1. <span data-ttu-id="68361-116">**Ambar yönetimi \> Periyodik görevler \> Ambar uygulaması olaylarını işle**'ye gidin.</span><span class="sxs-lookup"><span data-stu-id="68361-116">Go to **Warehouse management \> Periodic tasks \> Process warehouse app events**.</span></span>
1. <span data-ttu-id="68361-117">Ambar uygulaması olaylarını işle iletişim kutusu açılır.</span><span class="sxs-lookup"><span data-stu-id="68361-117">The Process warehouse app events dialog box opens.</span></span> <span data-ttu-id="68361-118">**Arka planda çalıştır** hızlı sekmesini genişletin ve **Toplu işleme** öğesini **Evet** olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="68361-118">Expand the **Run in background** FastTab and set **Batch processing** to **Yes**.</span></span>
1. <span data-ttu-id="68361-119">**Arka planda çalıştır** sekmesinde **Tekrar**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="68361-119">On the **Run in the background** FastTab, select **Recurrence**.</span></span>
1. <span data-ttu-id="68361-120">**Yinelemeyi tanımlayın** iletişim kutusu açılır.</span><span class="sxs-lookup"><span data-stu-id="68361-120">The **Define recurrence** dialog box opens.</span></span> <span data-ttu-id="68361-121">İşletmeniz için gereken çalışma zamanlamasını ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="68361-121">Set the run schedule as needed for your business.</span></span>
1. <span data-ttu-id="68361-122">**Ambar uygulaması olaylarını işle** iletişim kutusuna dönmek için **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="68361-122">Select **OK** to return to the **Process warehouse app events** dialog box.</span></span>
1. <span data-ttu-id="68361-123">Toplu işi toplu iş kuyruğuna eklemek için **Ambar uygulaması olaylarını işle** iletişim kutusunda **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="68361-123">Select **OK** in the **Process warehouse app events** dialog box to add the batch job to the batch queue.</span></span>

## <a name="query-warehouse-app-events"></a><span data-ttu-id="68361-124">Ambar uygulaması olaylarını sorgulama</span><span class="sxs-lookup"><span data-stu-id="68361-124">Query warehouse app events</span></span>

<span data-ttu-id="68361-125">Ambar uygulaması tarafından oluşturulan olay kuyruğunu ve olay iletilerini **Ambar yönetimi \> Sorgular ve raporlar \> Mobil cihaz günlükleri \> Ambar uygulaması olayları**'na giderek görüntüleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="68361-125">You can view the event queue and events messages generated by the warehouse app by going to **Warehouse management \> Inquiries and reports \> Mobile device logs \> Warehouse app events**.</span></span>

## <a name="the-standard-event-queue-process"></a><span data-ttu-id="68361-126">Standart olay kuyruğu işlemi</span><span class="sxs-lookup"><span data-stu-id="68361-126">The standard event queue process</span></span>

<span data-ttu-id="68361-127">Ambar uygulaması olayları kuyruğu genellikle aşağıdaki açıklanan akışla kullanılır:</span><span class="sxs-lookup"><span data-stu-id="68361-127">The warehouse apps events queue will typically be used with the following described flow:</span></span>

1. <span data-ttu-id="68361-128">Bir olay, bir olay iletisi ile kuyruğa eklenir.</span><span class="sxs-lookup"><span data-stu-id="68361-128">An event gets added to the queue  with an event message.</span></span> <span data-ttu-id="68361-129">Yeni iletin başlangıçta **Beklemede** Olay durumuna sahiptir; bu, **Ambar uygulaması olaylarını işle** toplu işinin bu iletiyi çekmeyeceği ve işlemeyeceği anlamına gelir.</span><span class="sxs-lookup"><span data-stu-id="68361-129">The new message initially has an Event state of **Waiting**, which means that the **Process warehouse app events** batch job will not pick up and process this message.</span></span>
1. <span data-ttu-id="68361-130">İleti durumu **Kuyruğa alındı** olarak güncelleştirildiğinde, **Ambar uygulaması olaylarını işle** toplu işi olayı alır ve işler.</span><span class="sxs-lookup"><span data-stu-id="68361-130">As soon as the message state is updated to **Queued**, the **Process warehouse app** events batch job will pick up and process the event.</span></span>
1. <span data-ttu-id="68361-131">Toplu iş istenen işlemin gerçekleştirilmiş olup olmamasına bağlı olarak, olay durumlarını **Tamamlandı** veya **Başarısız oldu** olarak güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="68361-131">The batch job updates the event states to either **Completed** or **Failed**, depending on whether the requested process was possible.</span></span>
1. <span data-ttu-id="68361-132">İlgili tüm olay iletileri **Tamamlandığına** olay kuyruktan silinir.</span><span class="sxs-lookup"><span data-stu-id="68361-132">When all the related event messages are **Completed**, the event is deleted from the queue.</span></span>

 <span data-ttu-id="68361-133">Ayrıntılı bir örnek için bkz. [Ambar uygulamasından transfer emri oluşturma işlemi](create-transfer-order-from-warehouse-app.md).</span><span class="sxs-lookup"><span data-stu-id="68361-133">For a detailed example, see [Create transfer order from warehouse app process](create-transfer-order-from-warehouse-app.md).</span></span>

## <a name="handle-event-errors"></a><span data-ttu-id="68361-134">Olay hatalarını işleme</span><span class="sxs-lookup"><span data-stu-id="68361-134">Handle event errors</span></span>

<span data-ttu-id="68361-135">Ambar olayı işlemenin bir parçası olarak, istenen ileti etkinliği işlemleri toplu işten alamayabilir.</span><span class="sxs-lookup"><span data-stu-id="68361-135">As part of the warehouse event processing, the requested message activity may not receive processes from the batch job.</span></span> <span data-ttu-id="68361-136">Bu durumda, olay iletisi **Başarısız oldu** şekilde değişecektir.</span><span class="sxs-lookup"><span data-stu-id="68361-136">In this case, the event message will change to **Failed**.</span></span> <span data-ttu-id="68361-137">Nedenini öğrnemke ve sorunları düzeltmek için gerekli adımları atmak için **Toplu iş günlüğü** bilgilerini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="68361-137">You can use the **Batch log** information to learn why and take needed action to correct any problems.</span></span>

<span data-ttu-id="68361-138">Ayrıntılı bir örnek için bkz. [Ambar uygulamasından transfer emri oluşturma](create-transfer-order-from-warehouse-app.md).</span><span class="sxs-lookup"><span data-stu-id="68361-138">For a detailed example, see [Create transfer order from warehouse app](create-transfer-order-from-warehouse-app.md).</span></span>

<span data-ttu-id="68361-139">Başarısız olan bir ambar uygulaması olay iletisini sıfırlamak için:</span><span class="sxs-lookup"><span data-stu-id="68361-139">To reset a failed warehouse app event message:</span></span>

1. <span data-ttu-id="68361-140">**Ambar yönetimi \> Sorgulamalar ve raporlar \> Mobil cihaz günlükleri \> Ambar uygulaması olayları**'na gidin.</span><span class="sxs-lookup"><span data-stu-id="68361-140">Go to **Warehouse management \> Inquiries and reports \> Mobile device logs \> Warehouse app events**.</span></span>
1. <span data-ttu-id="68361-141">**Ambar uygulaması olay iletileri** hızlı sekmesinde, **Olay durumu** sütununda **Başarısız oldu** olarak gösterilen ilgili olayı seçin.</span><span class="sxs-lookup"><span data-stu-id="68361-141">On the **Warehouse app event messages** FastTab, find and select a relevant event that is showing **Failed** in the **Event state** column.</span></span>
1. <span data-ttu-id="68361-142">**Ambar uygulaması olay iletileri** araç çubuğundan **Sıfırla** seçeneğini belirleyin.</span><span class="sxs-lookup"><span data-stu-id="68361-142">Select **Reset** from the **Warehouse app event messages** toolbar.</span></span>
1. <span data-ttu-id="68361-143">İlgili tüm iletiler sıfırlanana kadar çalışmaya devam edin.</span><span class="sxs-lookup"><span data-stu-id="68361-143">Continue working until all relevant messages are reset.</span></span>

<span data-ttu-id="68361-144">Ayrıca, **Ambar uygulaması olay iletileri** araç çubuğundaki **Sil** seçeneğini kullanarak **Başarısız oldu** olay iletisini kaldırabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="68361-144">You can also remove a **Failed** event message by using the **Delete** option on the **Warehouse app event messages** toolbar.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]