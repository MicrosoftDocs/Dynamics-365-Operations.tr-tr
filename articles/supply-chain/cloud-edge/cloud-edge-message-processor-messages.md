---
title: İleti işlemci iletileri
description: Bu konu, ölçek birimi iş yükleri için İleti işlemcisi iletileri özelliği hakkında bilgi sağlar.
author: perlynne
ms.date: 04/22/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SysMessageProcessorMessage, BusinessEventsWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: SCM
ms.author: perlynne
ms.search.validFrom: 2021-04-21
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 03d8cad743ac2b2b1e7b2832b8272ca3dbf5a163
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/11/2021
ms.locfileid: "6021067"
---
# <a name="message-processor-messages"></a><span data-ttu-id="a8d87-103">İleti işlemci iletileri</span><span class="sxs-lookup"><span data-stu-id="a8d87-103">Message processor messages</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="a8d87-104">İleti işlemcisi iletileri, [üretim iş yükleri](cloud-edge-workload-manufacturing.md) ve [ambar yönetimi iş yükleri](cloud-edge-workload-warehousing.md) için bulut ve kenar ölçek birimleri çalıştırıldığında kullanılır.</span><span class="sxs-lookup"><span data-stu-id="a8d87-104">Message processor messages are used when running cloud and edge scale units for [manufacturing workloads](cloud-edge-workload-manufacturing.md) and [warehouse management workloads](cloud-edge-workload-warehousing.md).</span></span>

<span data-ttu-id="a8d87-105">Merkez ve ölçek birim dağıtım ortamları arasındaki senkronizeliği korumak için büyük miktarlarda veri alışverişi yapılır ancak bu veri alışverişlerinin yalnızca birkaçı *ileti işlemcisi* tarafından işlenir.</span><span class="sxs-lookup"><span data-stu-id="a8d87-105">A large amount of data is exchanged between the hub and scale unit deployment environments to keep them in sync, but only a few of these data exchanges will be processed by the *message processor*.</span></span> <span data-ttu-id="a8d87-106">İleti işlemcisi tarafından işlem gören iletileri, **Sistem yönetimi > İleti işlemcisi > İleti işlemcisi iletileri**'ne giderek görüntüleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="a8d87-106">You can view the messages processed by the message processor by going to **System administration > Message processor > Message processor messages**.</span></span>

## <a name="message-grid-columns-and-filters"></a><span data-ttu-id="a8d87-107">İleti ızgarası sütunları ve filtreleri</span><span class="sxs-lookup"><span data-stu-id="a8d87-107">Message grid columns and filters</span></span>

<span data-ttu-id="a8d87-108">Aradığınız bir iletiyi bulmak için **İleti işlemci iletileri** sayfasının en üstünde yer alan alanları kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="a8d87-108">You can use the fields at the top of the **Message processor messages** page to help find any particular messages you are looking for.</span></span> <span data-ttu-id="a8d87-109">Bu filtrelerin çoğu ileti ızgarasındaki sütun başlıklarıyla eşleşir.</span><span class="sxs-lookup"><span data-stu-id="a8d87-109">Most of these filters match the column headings in the message grid.</span></span> <span data-ttu-id="a8d87-110">Aşağıdaki filtreler ve sütun başlıkları mevcuttur:</span><span class="sxs-lookup"><span data-stu-id="a8d87-110">The following filters and column headings are available:</span></span>

- <span data-ttu-id="a8d87-111">**İleti türü** – İletinin türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="a8d87-111">**Message type** – Specifies the type of message.</span></span>
- <span data-ttu-id="a8d87-112">**İleti kuyruğu** - İletinin işleme alınacağı sıranın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="a8d87-112">**Message queue** – Specifies the name of the queue in which the message is to be processed.</span></span> <span data-ttu-id="a8d87-113">Aşağıdaki kuyruklar sağlanır:</span><span class="sxs-lookup"><span data-stu-id="a8d87-113">The following queues are provided:</span></span>
  - <span data-ttu-id="a8d87-114">*Ölçek biriminden hub'a*</span><span class="sxs-lookup"><span data-stu-id="a8d87-114">*Scale unit to hub*</span></span>
  - <span data-ttu-id="a8d87-115">*Hub'dan ambara yürütme ölçek birimi*</span><span class="sxs-lookup"><span data-stu-id="a8d87-115">*Hub to warehouse execution scale unit*</span></span>
  - <span data-ttu-id="a8d87-116">*Hub'dan üretime yürütme ölçek birimi*</span><span class="sxs-lookup"><span data-stu-id="a8d87-116">*Hub to manufacturing execution scale unit*</span></span>
- <span data-ttu-id="a8d87-117">**İleti durumu** – İletinin durumunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="a8d87-117">**Message state** – Specifies the state of the message.</span></span> <span data-ttu-id="a8d87-118">Aşağıdaki durumlar mevcuttur:</span><span class="sxs-lookup"><span data-stu-id="a8d87-118">The following states exists:</span></span>
  - <span data-ttu-id="a8d87-119">*Sıraya alındı* – İleti, ileti işlemcisi tarafından işlenmeye hazır.</span><span class="sxs-lookup"><span data-stu-id="a8d87-119">*Queued* – The message is ready to be processed by the message processor.</span></span>
  - <span data-ttu-id="a8d87-120">*İşlendi* – İleti, ileti işlemcisi tarafından başarıyla işlendi.</span><span class="sxs-lookup"><span data-stu-id="a8d87-120">*Processed* – The message was successfully processed by the message processor.</span></span>
  - <span data-ttu-id="a8d87-121">*İptal edildi* - İleti işlendi ancak işlem başarısız oldu.</span><span class="sxs-lookup"><span data-stu-id="a8d87-121">*Canceled* – The message was processed, but processing failed.</span></span>
- <span data-ttu-id="a8d87-122">**İleti içeriği** – Filtre, ileti içeriğinde tam metin araması yapar.</span><span class="sxs-lookup"><span data-stu-id="a8d87-122">**Message content** – This filter does a full-text search of message content.</span></span> <span data-ttu-id="a8d87-123">(İleti içeriği kılavuzda görüntülenmez.) Filtre, birçok özel simgeyi ("-" gibi) boşluk olarak işler ve tüm boşluk karakterlerini Boole VEYA işleçleri olarak değerlendirir.</span><span class="sxs-lookup"><span data-stu-id="a8d87-123">(Message content is not shown in the grid.) The filter treats most special symbols (such as "-") as spaces, and treats all space characters as Boolean OR operators.</span></span> <span data-ttu-id="a8d87-124">T=Örneğin bunun anlamı, "USMF-123456" değerine eşit belirli bir `journalid` arıyorsanız sistem, "usmf" veya "123456" içeren tüm iletileri bulur (bu liste muhtemelen uzun bir liste olacaktır).</span><span class="sxs-lookup"><span data-stu-id="a8d87-124">T=For example, this means if you search for a specific `journalid` value equal "USMF-123456", the system will find all messages that contain "USMF" or "123456", which is likely to be a long list.</span></span> <span data-ttu-id="a8d87-125">Bu nedenle, daha belirgin sonuçlar almak için yalnızca "123456" girilmesi daha iyi olacaktır.</span><span class="sxs-lookup"><span data-stu-id="a8d87-125">Therefore, it would be better to enter just "123456" alone because that will return more specific results.</span></span>

## <a name="example-message-type-request-inventory-adjustment-financial-update"></a><span data-ttu-id="a8d87-126">Örnek ileti türü: Stok ayarlaması mali güncelleştirmesi iste</span><span class="sxs-lookup"><span data-stu-id="a8d87-126">Example message type: Request inventory adjustment financial update</span></span>

<span data-ttu-id="a8d87-127">Örneğin, bir çalışan bir ölçek birimi ambar yönetimi iş yükünde [stok ayarlaması kaydetmek](cloud-edge-warehouse-inventory-adjustment.md) için ambar uygulamasını kullandığında, merkez üzerinde bir sayım günlüğü oluşturmak ve nakletmek için *Stok ayarlaması mali güncelleştirmesi iste* adlı **İleti türü** kullanılır.</span><span class="sxs-lookup"><span data-stu-id="a8d87-127">For example, the **Message type** *Request inventory adjustment financial update* is used to create and post a counting journal on the hub when a worker uses the warehouse app to [register an inventory adjustment](cloud-edge-warehouse-inventory-adjustment.md) on a scale unit warehouse management workload.</span></span> <span data-ttu-id="a8d87-128">Bu özel işlem bir ölçek biriminden geldiği için, **İleti sırası** alanı, *Birimi merkeze ölçekle* değerini gösterir.</span><span class="sxs-lookup"><span data-stu-id="a8d87-128">Because this specific process originates from a scale unit, the **Message queue** field will show the value *Scale unit to hub*.</span></span>

<span data-ttu-id="a8d87-129">Bu ileti türünde bir ölçek birimi iş yükü, bir ambar uygulama stok ayarlama işleminin parçası olarak iletiyi kaydeder.</span><span class="sxs-lookup"><span data-stu-id="a8d87-129">For this message type, a scale unit workload records the message as part of a warehouse app inventory adjustment operation.</span></span> <span data-ttu-id="a8d87-130">Ardından ileti verileri, [Commerce Data Exchange](../../commerce/commerce-architecture.md) mimarisi için kullanılan aynı işlemin bir parçası olarak merkeze aktarılır.</span><span class="sxs-lookup"><span data-stu-id="a8d87-130">The message data is then transferred to the hub as part of the same process used for the [Commerce data exchange architecture](../../commerce/commerce-architecture.md).</span></span> <span data-ttu-id="a8d87-131">İleti, **İleti durumunu** *Kuyruğa alındı* olarak gösterecek şekilde güncelleştirilecektir.</span><span class="sxs-lookup"><span data-stu-id="a8d87-131">The message will be updated to show **Message state** as *Queued*.</span></span> <span data-ttu-id="a8d87-132">İleti işlemcisi ardından iletiyi işlemeyi dener ve işlem başarılı olursa **İleti durumunu** *İşlendi* olarak, işlem başarısız olursa *İptal edildi* olarak güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="a8d87-132">The message processor then attempts to process the message and updates the **Message state** to *Processed* on success, or *Canceled* on failure.</span></span>

## <a name="view-the-message-log-message-content-and-details"></a><span data-ttu-id="a8d87-133">İleti günlüğünü, ileti içeriğini ve ayrıntıları görüntüleme</span><span class="sxs-lookup"><span data-stu-id="a8d87-133">View the message log, message content, and details</span></span>

<span data-ttu-id="a8d87-134">Bir iletiyle ilgili ayrıntılı bilgileri, iletiyi ızgarada seçip ardından her işleme olayının gösterildiği ileti ızgarası altında **Günlük** veya **İleti içeriği** sekmelerini açarak bulabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="a8d87-134">You can find detailed information about a message by selecting it in the grid and then opening the **Log** or **Message content** tabs under the message grid, where each processing event is shown.</span></span>

<span data-ttu-id="a8d87-135">**İleti içeriği**, **İleti türü**'ne bağlıdır ve bu nedenle farklı metin uzunluğuna sahip olur.</span><span class="sxs-lookup"><span data-stu-id="a8d87-135">The **Message content** depends on the **Message type** and will therefore have different text length.</span></span> <span data-ttu-id="a8d87-136">Tipik bir ileti içerik metni **{** ile başlar ve **}** ile biter, arasında `journalId` gibi bir alan adı bulunur ve bu alan ardının ardından bir **.** ve *USMF-123456* gibi bir değer gelir.</span><span class="sxs-lookup"><span data-stu-id="a8d87-136">A typical message content text will start with a **{** and end with a **}** and in between have field names such as `journalId` followed by a **:** and a value such as *USMF-123456*.</span></span>

<span data-ttu-id="a8d87-137">**Günlük** sekmesindeki araç çubuğunda aşağıdaki düğmeler bulunur:</span><span class="sxs-lookup"><span data-stu-id="a8d87-137">The toolbar on the **Log** tab includes the following buttons:</span></span>

- <span data-ttu-id="a8d87-138">**Günlük** – İşleme sonuçlarını görüntüler.</span><span class="sxs-lookup"><span data-stu-id="a8d87-138">**Log** – Displays the processing results.</span></span> <span data-ttu-id="a8d87-139">Bu, özellikle **İşlem sonucu** *Başarısız* olan iletilerde işlem hatasının nedenlerini anlamak için yararlıdır.</span><span class="sxs-lookup"><span data-stu-id="a8d87-139">This is especially helpful for understanding the reasons for a processing failure for messages having a **Processing result** of *Failed*.</span></span>
- <span data-ttu-id="a8d87-140">**Ürün demeti** – Birden fazla ileti işleme operasyonları, aynı toplu işlemin parçası olarak çalıştırılabilir.</span><span class="sxs-lookup"><span data-stu-id="a8d87-140">**Bundle** – Multiple message processing operations can run as part of the same batch process.</span></span> <span data-ttu-id="a8d87-141">Ayrıntılı verileri görüntülemek için bu düğmeyi seçin.</span><span class="sxs-lookup"><span data-stu-id="a8d87-141">Select this button to view this detailed data.</span></span> <span data-ttu-id="a8d87-142">Örneğin, sistemin belirli bir sırada belirli iletileri işlemesini gerektiren bağımlılıklar bulunup bulunmadığını görebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="a8d87-142">For example, you can see whether dependencies exist that require the system to process certain messages in a specific sequence.</span></span>

## <a name="message-processor-batch-job"></a><span data-ttu-id="a8d87-143">İleti işlemcisi toplu işlemi</span><span class="sxs-lookup"><span data-stu-id="a8d87-143">Message processor batch job</span></span>

<span data-ttu-id="a8d87-144">Bir bulut ve kenar dağıtımı çalıştırılırken, işlem için yeni bir ileti oluşturulurken *İleti işlemcisi* toplu işi otomatik olarak gönderilir, bu nedenle bu işi manuel olarak zamanlamanız gerekmez.</span><span class="sxs-lookup"><span data-stu-id="a8d87-144">When running a cloud and edge deployment, the *Message processor* batch job will automatically be evoked when a new message is created for processing, so you should not need to schedule this job manually.</span></span>

<span data-ttu-id="a8d87-145">Gerekirse, **Sistem yönetimi > İleti işlemcisi > İleti işlemcisi**'ne giderek toplu işe erişebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="a8d87-145">If necessary, you can access the batch job by going to **System administration > Message  processor > Message processor**.</span></span>

## <a name="manually-process-or-cancel-a-message"></a><span data-ttu-id="a8d87-146">İletiyi manuel olarak işleme veya iptal etme</span><span class="sxs-lookup"><span data-stu-id="a8d87-146">Manually process or cancel a message</span></span>

<span data-ttu-id="a8d87-147">Gerekirse, mevcut durumuna bağlı olarak bir iletiyi manuel olarak işleyebilir veya iptal edebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="a8d87-147">If needed, you can manually process or cancel a message, depending on its current state.</span></span> <span data-ttu-id="a8d87-148">Bunu yapmak için, ızgarada iletiyi seçin ve sonra Eylem Bölmesi'nde **İşle** veya **İptal Et**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="a8d87-148">To do so, select the message in the grid and then select **Process** or **Cancel** on the Action Pane</span></span>

## <a name="set-up-business-events-to-deliver-alerts-for-failed-processing-results"></a><span data-ttu-id="a8d87-149">Başarısız işleme sonuçları için uyarı vermek üzere iş olayları ayarlama</span><span class="sxs-lookup"><span data-stu-id="a8d87-149">Set up business events to deliver alerts for failed processing results</span></span>

<span data-ttu-id="a8d87-150">Başarısız iletileri sorgulamak için **İleti durumu** değeri *İptal Edildi* filtresini uygulamaya ek olarak başarısız işleme sonuçlarıyla ilgili bildirim almak için merkezde [İş olayları](../../fin-ops-core/dev-itpro/business-events/home-page.md) ayarlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="a8d87-150">In addition to filtering on the **Message state** value *Canceled* to inquire for failed messages, you can set up [Business events](../../fin-ops-core/dev-itpro/business-events/home-page.md) on the hub to alert you to failed processing results.</span></span> <span data-ttu-id="a8d87-151">Bunu yapmak için, **İş olayları kataloğu** sayfasında (**Sistem yönetimi > Kurulum > İş olayları > İş olayları kataloğu**) *İleti işlemcisi işlenen ileti* adlı iş olayını etkinleştirin.</span><span class="sxs-lookup"><span data-stu-id="a8d87-151">To do so, activate the business event named *Message processor message processed*  on the **Business events catalog** page (**System administration > Setup > Business events > Business events catalog**).</span></span>

<span data-ttu-id="a8d87-152">Etkinleştirme işleminin bir parçası olarak, olayın bir tüzel kişilik için mi tüm tüzel kişilikler için mi olduğunu belirlemeniz ve önce tanımlanması gereken bir **Uç nokta adı** sağlamanız istenir.</span><span class="sxs-lookup"><span data-stu-id="a8d87-152">As part of the activation process, you will be guided to specify whether the event is specific to one or all legal entities and provide an **Endpoint name**, which must be defined first.</span></span>

>[!NOTE]
> <span data-ttu-id="a8d87-153">**Bir İş Olayı gerçekleştiğinde** alanı *Microsoft Power Automate* olarak ayarlandığında (örneğin *HTTPS* yerine), **Uç nokta adı** otomatik olarak *Microsoft Power Automate* kurulumuna bağlı olarak Supply Chain Management'ta oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="a8d87-153">If **When a Business Event occurs** is set to *Microsoft Power Automate* (rather than *HTTPS*, for example), the **Endpoint name** will automatically be created in Supply Chain Management based on the *Microsoft Power Automate* setup.</span></span>

### <a name="microsoft-power-automate-example"></a><span data-ttu-id="a8d87-154">Microsoft Power Automate örneği</span><span class="sxs-lookup"><span data-stu-id="a8d87-154">Microsoft Power Automate example</span></span>

<span data-ttu-id="a8d87-155">Bu örnekte, **Bir İş Olayı gerçekleştiğinde**'yi *Microsoft Power Automate* ile kullanmak, merkez dağıtımında başarısız olan belirli bir iletinin **İleti işlemci iletileri** sayfasını açmak için bilgi günlüğü iletileri ve köprüler içeren e-postalar gönderir.</span><span class="sxs-lookup"><span data-stu-id="a8d87-155">In this example, use **When a Business Event occurs** with *Microsoft Power Automate* sends emails containing InfoLog messages and hyperlinks to open the **Message processor messages** page for a specific failed message on the hub deployment.</span></span> <span data-ttu-id="a8d87-156">Gerekirse, farklı kanallar kullanarak bildirimleri paralel olarak göndermek ve olay verilerini esas alarak alıcıları denetlemek için ek mantık ekleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="a8d87-156">If needed, you can add extra logic to send the notifications in parallel using different channels and control the recipients based on the event data.</span></span>

1. <span data-ttu-id="a8d87-157">[Power Automate](https://preview.flow.microsoft.com) bölümünde, ardından **JSON'u ayrıştır** ve **Bir e-posta gönder** adımları gelen **Bir İş Olayı gerçekleştiğinde - Fin ve Ops Uygulaması (Dynamics 365)** akış tetikleyicisi için yeni bir otomatik bulut akışı oluşturun.</span><span class="sxs-lookup"><span data-stu-id="a8d87-157">In [Power Automate](https://preview.flow.microsoft.com), create a new automated cloud flow for the flow trigger **When a Business Event occurs - Fin & Ops App (Dynamics 365)** followed by the **Parse JSON** and **Send an email** steps, as shown in the following illustration.</span></span>

    :::image type="content" source="./media/cloud-edge-power-automate-example1.png" alt-text="Power Automate otomatik bulut akışı":::

1. <span data-ttu-id="a8d87-159">**Bir İş Olayı gerçekleştiğinde** adımında, **Kategori**'nin ardından gelen merkez **Örnek**'ini ve ardından **İş olayı** *İleti işlemcisi ileti işlendi*'yi arayabilir veya girebilirsiniz (aşağıdaki resimde gösterildiği üzere).</span><span class="sxs-lookup"><span data-stu-id="a8d87-159">In the **When a Business Event occurs** step, you can look up or enter the hub **Instance** following the **Category** and then the **Business event** *Message processor message processed*, as shown in the following illustration.</span></span>

    :::image type="content" source="./media/cloud-edge-power-automate-example2.png" alt-text="Power Automate Bir İş Olayı gerçekleştiğinde adımı":::

1. <span data-ttu-id="a8d87-161">**JSON'u ayrıştır** adımı için genişletilmiş alanları tanımlayan bir **Şema** girin.</span><span class="sxs-lookup"><span data-stu-id="a8d87-161">For the **Parse JSON** step, enter a **Schema** that defines the extended fields.</span></span> <span data-ttu-id="a8d87-162">Supply Chain Management içindeki **İş olayları kataloğu** sayfasında yer alan *Şemayı indir* seçeneğini kullanabilir veya örnek şema metnini yapıştırarak başlatabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="a8d87-162">You can use the *Download schema* option on the **Business events catalog** page in Supply Chain Management or start by pasting in the example schema text.</span></span> <span data-ttu-id="a8d87-163">Bu örnek metin, aşağıdaki resimde yer alan örnekle ilişkilidir.</span><span class="sxs-lookup"><span data-stu-id="a8d87-163">This example text is provided after the following illustration.</span></span>

    :::image type="content" source="./media/cloud-edge-power-automate-example3.png" alt-text="Power Automate JSON'u ayrıştır adımı":::

    ```json
    {
        "properties": {
            "BusinessEventId": {
                "type": "string"
            },
            "ControlNumber": {
                "type": "integer"
            },
            "EventId": {
                "type": "string"
            },
            "EventTime": {
                "type": "string"
            },
            "MajorVersion": {
                "type": "integer"
            },
            "MessageContent": {
                "type": "string"
            },
            "MessageDestinationCompanyId": {
                "type": "string"
            },
            "MessageDestinationOperationalSiteId": {
                "type": "string"
            },
            "MessageDestinationWarehouseId": {
                "type": "string"
            },
            "MessageDestinationWorkloadName": {
                "type": "string"
            },
            "MessageInfolog": {
                "type": "string"
            },
            "MessageProcessingResult": {
                "type": "string"
            },
            "MessageProcessingResultLabel": {
                "type": "string"
            },
            "MessageProcessorMessagePageUrl": {
                "type": "string"
            },
            "MessageQueue": {
                "type": "string"
            },
            "MessageQueueLabel": {
                "type": "string"
            },
            "MessageSourceCompanyId": {
                "type": "string"
            },
            "MessageSourceOperationalSiteId": {
                "type": "string"
            },
            "MessageSourceWarehouseId": {
                "type": "string"
            },
            "MessageSourceWorkloadName": {
                "type": "string"
            },
            "MessageState": {
                "type": "string"
            },
            "MessageStateLabel": {
                "type": "string"
            },
            "MessageType": {
                "type": "string"
            },
            "MessageTypeLabel": {
                "type": "string"
            },
            "MinorVersion": {
                "type": "integer"
            }
        },
        "type": "object"
    }
    ```

1. <span data-ttu-id="a8d87-165">**E-posta gönder** adımında, alanları tek tek seçebilir veya e-posta gövdesini **Gövde** alanına yapıştırarak başlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="a8d87-165">In the **Send an email** step, you can select the individual fields or start by pasting the email body example into the **Body** field.</span></span> <span data-ttu-id="a8d87-166">Bu örnek, aşağıdaki resimde yer alan örnekle ilişkilidir.</span><span class="sxs-lookup"><span data-stu-id="a8d87-166">This example is provided after the following illustration.</span></span>

    :::image type="content" source="./media/cloud-edge-power-automate-example4.png" alt-text="Power Automate e-posta gönder adımı":::

    ```plaintext
    Message queue: @{body('Parse_JSON')?['MessageQueue']}
    Message queue label: @{body('Parse_JSON')?['MessageQueueLabel']}
    Message type: @{body('Parse_JSON')?['MessageQueueType']}
    Message type label: @{body('Parse_JSON')?['MessageQueueTypeLabel']}
    Message content: @{body('Parse_JSON')?['MessageContent']}
    Message state: @{body('Parse_JSON')?['MessageState']}
    Message state label: @{body('Parse_JSON')?['MessageStateLabel']}
    Message processing result: @{body('Parse_JSON')?['MessageProcessingResult']}
    Message processing result label: @{body('Parse_JSON')?['MessageProcessingResultLabel']}
    Message infolog: @{body('Parse_JSON')?['MessageInfolog']}
    Message source company ID: @{body('Parse_JSON')?['MessageSourceCompanyId']}
    Message source workload name: @{body('Parse_JSON')?['MessageSourceWorkloadName']}
    Message source site ID: @{body('Parse_JSON')?['MessageSourceOperationalSiteId']}
    Message source warehouse ID: @{body('Parse_JSON')?['MessageSourceWarehouseId']}
    Message destination company ID: @{body('Parse_JSON')?['MessageDestinationCompanyId']}
    Message destination workload name: @{body('Parse_JSON')?['MessageDestinationWorkloadName']}
    Message destination site ID: @{body('Parse_JSON')?['MessageDestinationOperationalSiteId']}
    Message destination warehouse ID: @{body('Parse_JSON')?['MessageDestinationWarehouseId']}
    Message processor message page URL: @{body('Parse_JSON')?['MessageProcessorMessagePageUrl']}
    ```

1. <span data-ttu-id="a8d87-168">İş olayını kaydettiğinizde, otomatik olarak etkinleştirilir ve Supply Chain Management'ın bir parçası olarak kullanılmaya hazır hale gelir.</span><span class="sxs-lookup"><span data-stu-id="a8d87-168">When you save the business event, it will automatically be activated and ready to use as part of Supply Chain Management.</span></span>
