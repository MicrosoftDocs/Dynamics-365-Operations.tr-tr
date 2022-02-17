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
ms.openlocfilehash: 68db4c6561f2cc3fcfd64b49da59a4cc164685f2
ms.sourcegitcommit: 3a7f1fe72ac08e62dda1045e0fb97f7174b69a25
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/31/2022
ms.locfileid: "8069441"
---
# <a name="message-processor-messages"></a>İleti işlemci iletileri

[!include [banner](../includes/banner.md)]

İleti işlemcisi iletileri, [üretim iş yükleri](cloud-edge-workload-manufacturing.md) ve [ambar yönetimi iş yükleri](cloud-edge-workload-warehousing.md) için bulut ve kenar ölçek birimleri çalıştırıldığında kullanılır.

Merkez ve ölçek birimi dağıtım ortamları, eşitlenmiş olarak kalmak için büyük miktarda veri alıp verir. Alıp verilen verilerin bir kısmı, *ileti işleyicide* ek mantıkları tetikler. İleti işlemcisi tarafından işlenen iletileri, **Sistem yönetimi > İleti işlemcisi > İleti işlemcisi iletileri**'ne giderek görüntüleyebilirsiniz.

## <a name="message-grid-columns-and-filters"></a>İleti ızgarası sütunları ve filtreleri

Aradığınız bir iletiyi bulmak için **İleti işlemci iletileri** sayfasının en üstünde yer alan alanları kullanabilirsiniz. Bu filtrelerin çoğu ileti ızgarasındaki sütun başlıklarıyla eşleşir. Aşağıdaki filtreler ve sütun başlıkları mevcuttur:

- **İleti türü** – İletinin türünü belirtir.
- **İleti kuyruğu** - İletinin işleme alınacağı sıranın adını belirtir. Aşağıdaki kuyruklar sağlanır:
  - *Ölçek biriminden hub'a*
  - *Hub'dan ambara yürütme ölçek birimi*
  - *Hub'dan üretime yürütme ölçek birimi*
- **İleti durumu** – İletinin durumunu belirtir. Aşağıdaki durumlar mevcuttur:
  - *Sıraya alındı* – İleti, ileti işlemcisi tarafından işlenmeye hazır.
  - *İşlendi* – İleti, ileti işlemcisi tarafından başarıyla işlendi.
  - *İptal edildi* - İleti işlendi ancak işlem başarısız oldu.
- **İleti içeriği** – Filtre, ileti içeriğinde tam metin araması yapar. (İleti içeriği kılavuzda görüntülenmez.) Filtre, birçok özel simgeyi ("-" gibi) boşluk olarak işler ve tüm boşluk karakterlerini Boole VEYA işleçleri olarak değerlendirir. Örneğin bu, "USMF-123456" değerine eşit belirli bir `journalid` arıyorsanız sistemin, "usmf" veya "123456" içeren tüm iletileri bulacağı anlamına gelir (bu liste muhtemelen uzun bir liste olacaktır). Bu nedenle, daha belirgin sonuçlar almak için yalnızca "123456" girilmesi daha iyi olacaktır.

## <a name="example-message-type-request-inventory-adjustment-financial-update"></a>Örnek ileti türü: Stok ayarlaması mali güncelleştirmesi iste

Örneğin, bir çalışan bir ölçek birimi ambar yönetimi iş yükünde [stok ayarlaması kaydetmek](cloud-edge-warehouse-inventory-adjustment.md) için ambar uygulamasını kullandığında, merkez üzerinde bir sayım günlüğü oluşturmak ve nakletmek için *Stok ayarlaması mali güncelleştirmesi iste* adlı **İleti türü** kullanılır. Bu özel işlem bir ölçek biriminden geldiği için, **İleti sırası** alanı, *Birimi merkeze ölçekle* değerini gösterir.

Bu ileti türünde bir ölçek birimi iş yükü, bir ambar uygulama stok ayarlama işleminin parçası olarak iletiyi kaydeder. Ardından ileti verileri, [Commerce Data Exchange](../../commerce/commerce-architecture.md) mimarisi için kullanılan aynı işlemin bir parçası olarak merkeze aktarılır. İleti, **İleti durumunu** *Kuyruğa alındı* olarak gösterecek şekilde güncelleştirilecektir. İleti işlemcisi ardından iletiyi işlemeyi dener ve işlem başarılı olursa **İleti durumunu** *İşlendi* olarak, işlem başarısız olursa *İptal edildi* olarak güncelleştirir.

## <a name="view-the-message-log-message-content-and-details"></a>İleti günlüğünü, ileti içeriğini ve ayrıntıları görüntüleme

Bir iletiyle ilgili ayrıntılı bilgileri, iletiyi ızgarada seçip ardından her işleme olayının gösterildiği ileti ızgarası altında **Günlük** veya **İleti içeriği** sekmelerini açarak bulabilirsiniz.

**İleti içeriği**, **İleti türü**'ne bağlıdır ve bu nedenle farklı metin uzunluğuna sahip olur. Tipik bir ileti içerik metni **{** ile başlar ve **}** ile biter, arasında `journalId` gibi bir alan adı bulunur ve bu alan ardının ardından bir **.** ve *USMF-123456* gibi bir değer gelir.

**Günlük** sekmesindeki araç çubuğunda aşağıdaki düğmeler bulunur:

- **Günlük** – İşleme sonuçlarını görüntüler. Bu, özellikle **İşlem sonucu** *Başarısız* olan iletilerde işlem hatasının nedenlerini anlamak için yararlıdır.
- **Ürün demeti** – Birden fazla ileti işleme operasyonları, aynı toplu işlemin parçası olarak çalıştırılabilir. Ayrıntılı verileri görüntülemek için bu düğmeyi seçin. Örneğin, sistemin belirli bir sırada belirli iletileri işlemesini gerektiren bağımlılıklar bulunup bulunmadığını görebilirsiniz.

## <a name="message-processor-batch-job"></a>İleti işlemcisi toplu işlemi

Ölçek birimleriyle bir dağıtılmış karma topoloji çalıştırılırken işlem için yeni bir ileti oluşturulursa *İleti işlemcisi* toplu işi otomatik olarak gönderilir. Bu nedenle, bu işi el ile zamanlamanız gerekmez.

Gerekirse, **Sistem yönetimi > İleti işlemcisi > İleti işlemcisi**'ne giderek toplu işe erişebilirsiniz.

## <a name="manually-process-or-cancel-a-message"></a>İletiyi manuel olarak işleme veya iptal etme

Gerekirse, mevcut durumuna bağlı olarak bir iletiyi manuel olarak işleyebilir veya iptal edebilirsiniz. Bunu yapmak için, ızgarada iletiyi seçin ve sonra Eylem Bölmesi'nde **İşle** veya **İptal Et**'i seçin.

## <a name="set-up-business-events-to-deliver-alerts-for-failed-processing-results"></a>Başarısız işleme sonuçları için uyarı vermek üzere iş olayları ayarlama

Başarısız iletileri sorgulamak için **İleti durumu** değeri *İptal Edildi* filtresini uygulamaya ek olarak başarısız işleme sonuçlarıyla ilgili bildirim almak için merkezde [İş olayları](../../fin-ops-core/dev-itpro/business-events/home-page.md) ayarlayabilirsiniz. Bunu yapmak için, **İş olayları kataloğu** sayfasında (**Sistem yönetimi > Kurulum > İş olayları > İş olayları kataloğu**) *İleti işlemcisi işlenen ileti* adlı iş olayını etkinleştirin.

Etkinleştirme işleminin bir parçası olarak, olayın bir tüzel kişilik için mi tüm tüzel kişilikler için mi olduğunu belirlemeniz ve önce tanımlanması gereken bir **Uç nokta adı** sağlamanız istenir.

>[!NOTE]
> **Bir İş Olayı gerçekleştiğinde** alanı *Microsoft Power Automate* olarak ayarlandığında (örneğin *HTTPS* yerine), **Uç nokta adı** otomatik olarak *Microsoft Power Automate* kurulumuna bağlı olarak Supply Chain Management'ta oluşturulur.

### <a name="microsoft-power-automate-example"></a>Microsoft Power Automate örneği

Bu örnekte, **Bir İş Olayı gerçekleştiğinde**'yi *Microsoft Power Automate* ile kullanmak, merkez dağıtımında başarısız olan belirli bir iletinin **İleti işlemci iletileri** sayfasını açmak için bilgi günlüğü iletileri ve köprüler içeren e-postalar gönderir. Gerekirse, farklı kanallar kullanarak bildirimleri paralel olarak göndermek ve olay verilerini esas alarak alıcıları denetlemek için ek mantık ekleyebilirsiniz.

1. [Power Automate](https://preview.flow.microsoft.com) bölümünde, ardından **JSON'u ayrıştır** ve **Bir e-posta gönder** adımları gelen **Bir İş Olayı gerçekleştiğinde - Fin ve Ops Uygulaması (Dynamics 365)** akış tetikleyicisi için yeni bir otomatik bulut akışı oluşturun.

    :::image type="content" source="./media/cloud-edge-power-automate-example1.png" alt-text="Power Automate otomatik bulut akışı.":::

1. **Bir İş Olayı gerçekleştiğinde** adımında, **Kategori**'nin ardından gelen merkez **Örnek**'ini ve ardından **İş olayı** *İleti işlemcisi ileti işlendi*'yi arayabilir veya girebilirsiniz (aşağıdaki resimde gösterildiği üzere).

    :::image type="content" source="./media/cloud-edge-power-automate-example2.png" alt-text="Power Automate Bir İş Olayı gerçekleştiğinde adımı.":::

1. **JSON'u ayrıştır** adımı için genişletilmiş alanları tanımlayan bir **Şema** girin. Supply Chain Management içindeki **İş olayları kataloğu** sayfasında yer alan *Şemayı indir* seçeneğini kullanabilir veya örnek şema metnini yapıştırarak başlatabilirsiniz. Bu örnek metin, aşağıdaki resimde yer alan örnekle ilişkilidir.

    :::image type="content" source="./media/cloud-edge-power-automate-example3.png" alt-text="Power Automate JSON'u ayrıştır adımı.":::

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

1. **E-posta gönder** adımında, alanları tek tek seçebilir veya e-posta gövdesini **Gövde** alanına yapıştırarak başlayabilirsiniz. Bu örnek, aşağıdaki resimde yer alan örnekle ilişkilidir.

    :::image type="content" source="./media/cloud-edge-power-automate-example4.png" alt-text="Power Automate e-posta gönder adımı.":::

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

1. İş olayını kaydettiğinizde, otomatik olarak etkinleştirilir ve Supply Chain Management'ın bir parçası olarak kullanılmaya hazır hale gelir.
