---
title: Üçüncü taraf üretim yürütme sistemleriyle tümleştirme
description: Bu makale, Microsoft Dynamics 365 Supply Chain Management'ın üçüncü taraf bir üretim yürütme sistemi (MES) ile nasıl tümleştirileceğini açıklamaktadır.
author: johanhoffmann
ms.date: 08/09/2022
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2021-10-01
ms.dyn365.ops.version: 10.0.23
ms.openlocfilehash: 8629ef2581a114609d14999a3c1fc48b49c988e0
ms.sourcegitcommit: 203c8bc263f4ab238cc7534d4dd902fd996d2b0f
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/23/2022
ms.locfileid: "9336230"
---
# <a name="integrate-with-third-party-manufacturing-execution-systems"></a>Üçüncü taraf üretim yürütme sistemleriyle tümleştirme

[!include [banner](../includes/banner.md)]

Microsoft Dynamics 365 Supply Chain Management kullanan bazı üretim kuruluşları , makineler, ekipmanlar ve çalışanlara ilişkin üretim faaliyetlerini denetlemek için Dynamics 365 yerel işlevlerini kullanır. Ancak, başka üretim kuruluşları, özellikle de ileri düzeyde üretim gereklilikleri olan, bunun yerine üçüncü tarafa ait bir üretim yürütme sistemi (MES) kullanır. Kuruluşlar, örneğin dikey sektörlere özellikle uyarlanmış olduğundan, üçüncü tarafa ait bir MES çözümü seçebilirler.

Tümleşik çözümde, veri alışverişi tamamen otomatiktir ve gerçek zamanlı olarak gerçekleşir. Bu nedenle, veriler her iki sistemde de tutulur ve el ile veri girişi gerekmez. Örneğin, malzeme tüketimi MES'te kaydedildiğinde, tümleştirme aynı tüketimin Dynamics 365'te de kayıtlı olmasını sağlar. Bu nedenle, güncel stok kayıtları planlama ve satış gibi diğer önemli işlemler tarafından kullanılabilir.

Çözüm, Supply Chain Management kullanıcılarının üçüncü taraf MES'lerle tümleştirme sağlaması için daha hızlı, kolay ve ucuz bir araç oluşturur. Aşağıdaki özellikleri sunar:

- [Anahtar üretim yürütme işlemlerini](#processes-available-for-mes-integration) destekleyen iş olayları ve arabirimler
- Olay işleme geçmişini izleyebileceğiniz ve başarısız olan işlemlerin sorunlarını giderebileceğiniz merkezi bir pano

Aşağıdaki şekil, tümleşik bir çözümde alınan iş olayları, işlemler ve iletilerin tipik bir koleksiyonunu göstermektedir.

![Tipik bir tümleştirme senaryosu.](media/3p-mes-scenario.png "Tipik bir tümleştirme senaryosu.")

## <a name="turn-on-the-mes-integration-feature"></a>MES tümleştirme özelliğini açma

Aşağıdaki prosedürde açıklandığı şekilde, bu özelliği kullanabilmeden önce yöneticinizin bunu sisteminizde açması gerekir.

1. **Sistem yönetimi \> Kurulum \> Lisans yapılandırma** seçeneğine gidin.
1. **Zaman ve katılım** lisans anahtarının etkin olduğundan emin olun (onay işareti gösterir). Üretim yürütme sisteminin işlevlerini ve verilerini kontrol ettiğinden, bu lisans anahtarı gereklidir. Bu etkin değilse, aşağıdaki adımları uygulayın:
    1. Sisteminizi [Bakım modu](../../fin-ops-core/dev-itpro/sysadmin/maintenance-mode.md) bölümünde anlatıldığı şekilde bakım moduna alın.
    1. **Lisans yapılandırması** sayfasında, **zaman ve katılım** onay kutusunu seçin.
    1. [Bakım modu](../../fin-ops-core/dev-itpro/sysadmin/maintenance-mode.md) bölümünde anlatıldığı şekilde bakım modunu kapatın
1. **Sistem yönetimi \> Çalışma alanları \> Özellik yönetimi**'ne gidin.
1. *Üretim yürütme sistemi tümleştirmesi* özelliğini açmak için [Özellik yönetimi](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) çalışma alanını kullanın. (Supply Chain Management sürüm 10.0.29 itibariyle, bu özellik varsayılan olarak açıktır.)

## <a name="processes-available-for-mes-integration"></a>MES entegrasyonu için kullanılabilen işler

Tümleştirme için aşağıdaki işlemlerin herhangi birini veya tümünü etkinleştirebilirsiniz.

| İşlem adı | Tanım |
|---|---|
| Üretim emirlerini ve üretim emri durumu değişikliği iş olaylarını serbest bırakma | Bu işlem, MES'nin dinleyebileceği ve üretilmesi gereken üretim emirleriyle ilgili bilgi edinebileceği bir iş olayı sağlar. Üretim emriyle ilgili referans verilerinin, Açık Veri Protokolü (OData) veya veri varlıkları aracılığıyla Supply Chain Management'tan MES'e paylaşılabilecek olması beklenir. |
| Üretim emrini başlat | Bu süreç, MES kullanılarak başlatılan üretim emirleri hakkındaki bilgileri Supply Chain Management'a sağlar. Her iki sistemde tüm üretim faaliyetlerinin güncel görünümü olmasını sağlar. |
| Üretilen veya ıskartaya çıkan miktarı raporla | Bu süreç, MES kullanılarak üretim emrinde bildirilen mal ve hata miktarları bilgilerini Supply Chain Management'a sağlar. Atölye amirlerinin, üretim planı ilerlemesinin güncel görünümüne sahip olmasını sağlar. |
| Hammadde tüketimini bildir | Bu işlem, tüketilen malzeme miktarları hakkında bilgileri MES'ten alarak Supply Chain Management'a sağlar. Güncel stok kayıtları planlama ve satış gibi diğer önemli işlemler tarafından kullanılabilir. |
| Operasyon için tüketilen rapor zamanı | Bu işlem, belirli bir operasyon için kullanılan saat hakkında bilgileri Supply Chain Management'a sağlar. |
| Üretim emrini bitir | Bu işlem Supply Chain Management'a, MES'in bir üretim emrini sona erdiği *Son* durumuna kadar güncelleştirdiğini bildirir. Bu durum, üretim emrinde başka miktarların üretilemeyeceğini gösterir. |

## <a name="monitor-incoming-messages"></a>Gelen iletileri izle

Sisteme gelen iletileri izlemek için, **Üretim yürütme sistemi tümleştirme** sayfasını açın. Burada sorunları görüntüleyebilir, işleyebilir ve sorunları giderebilirsiniz.

Belirli bir üretim emrine yönelik tüm iletiler alındıkları sırayla işlenir. Ancak toplu işler paralel olarak işlendiğinden farklı üretim emirlerine yönelik iletiler alınan sırayla işlenmeyebilir. İşlem başarısız olursa toplu iş, *Başarısız* durumuna ayarlamadan önce her iletiyi üç kez işlemeyi dener.

## <a name="call-the-api"></a>API'yi çağır

MES Tümleştirme API'sini çağırmak için aşağıdaki bitiş noktası URL'sine bir `POST` isteği gönderin:

`/api/services/SysMessageServices/SysMessageService/SendMessage`

Gönderdiğiniz isteğin gövdesi, aşağıdaki örneğe benzemelidir. `_companyId`, `_messageType` ve `_messageContent` değerlerini gerektiği gibi değiştirin. API'nin desteklediği çeşitli ileti türleri ve içeriklerinin nasıl tasarlandıkları hakkında bilgi için sonraki bölüme bakın.

```json
{
    "_companyId": "USMF",
    "_messageQueue": "JmgMES3P",
    "_messageType": "ProdProductionOrderReportFinished",
    "_messageContent":
    "{\"ProductionOrderNumber\": \"P000123\", \"ReportFinishedLines\": [{\"ItemNumber\": \"A0001\", \"ReportedGoodQuantity\": 10, \"ReportAsFinishedDate\": \"2021-01-01\"}]}"
}
```

## <a name="api-message-types-and-content"></a>API ileti türleri ve içeriği

Bu bölümde, MES Tümleştirme API aracılığıyla alışverişi yapılabilecek her ileti türü açıklanmıştır.

### <a name="start-production-order-message"></a>Bir üretim emri iletisi başlatın

*Üretim emri başlangıcı* iletisi için `_messageType` değeri: `ProdProductionOrderStart`. Aşağıdaki tabloda bu iletinin desteklediği alanlar gösterilmektedir.

| Alan adı | Çalıştırma Durumu | Tür |
|---|---|---|
| `ProductionOrderNumber` | Zorunlu | Dize |
| `StartedQuantity` | İsteğe bağlı | Gerçek |
| `StartedDate` | İsteğe bağlı | Tarih |
| `AutomaticBOMConsumptionRule` | İsteğe bağlı | Enum (FlushingPrincip \| Her zaman \| Asla) |

### <a name="report-as-finished-message"></a>Tamamlandı olarak bildirme iletisi

*Tamamlandı bildirimi* iletisi için, `_messageType` değeri: `ProdProductionOrderReportFinished`. Aşağıdaki tabloda bu iletinin desteklediği alanlar gösterilmektedir.

| Alan adı | Çalıştırma Durumu | Tür |
|---|---|---|
| `ProductionOrderNumber` | Zorunlu | Dize |
| `ReportFinishedLines` | Zorunlu | Her biri bir sonraki tabloda açıklanan yükü içeren bir satır listesi (en az bir) |

Aşağıdaki tabloda, `ProdProductionOrderReportFinished` iletisinin `ReportFinishedLines` bölümündeki her bir satırın desteklediği alanlar gösterilmektedir.

| Alan adı | Çalıştırma Durumu | Tür |
|---|---|---|
| `LineNumber` | İsteğe bağlı | Gerçek |
| `ItemNumber` | İsteğe bağlı | Dize|
| `ProductionType` | İsteğe bağlı | Enum (MainItem \| Formül \| Ürün Reçetesi \| Co_Product \| By_Product \| Hiçbiri), genişletilebilir |
| `ReportedErrorQuantity` | İsteğe bağlı | Gerçek|
| `ReportedGoodQuantity` | İsteğe bağlı | Gerçek|
| `ReportedErrorCatchWeightQuantity` | İsteğe bağlı | Gerçek |
| `ReportedGoodCatchWeightQuantity` | İsteğe bağlı | Gerçek |
| `AcceptError` | İsteğe bağlı | Numaralandırma (Evet \| Hayır) |
| `ErrorCause` | İsteğe bağlı | Enum (Hiçbiri \| Malzeme \| Makine \| OperatingStaff), genişletilebilir |
| `ExecutedDateTime` | İsteğe bağlı | Tarih/Saat |
| `ReportAsFinishedDate` | İsteğe bağlı | Tarih |
| `AutomaticBOMConsumptionRule` | İsteğe bağlı | Enum (FlushingPrincip \| Her zaman \| Asla) |
| `AutomaticRouteConsumptionRule` | İsteğe bağlı |Enum (RouteDependent \| Her zaman \| Asla) |
| `RespectFlushingPrincipleDuringOverproduction` | İsteğe bağlı | Numaralandırma (Evet \| Hayır) |
| `ProductionJournalNameId` | İsteğe bağlı | Dize |
| `PickingListProductionJournalNameId` | İsteğe bağlı | Dize|
| `RouteCardProductionJournalNameId` | İsteğe bağlı | Dize |
| `FromOperationNumber` | İsteğe bağlı | Tamsayı|
| `ToOperationNumber` | İsteğe bağlı | Tamsayı|
| `InventoryLotId` | İsteğe bağlı | Dize |
| `BaseValue` | İsteğe bağlı | Dize |
| `EndJob` | İsteğe bağlı | Numaralandırma (Evet \| Hayır) |
| `EndPickingList` | İsteğe bağlı | Numaralandırma (Evet \| Hayır) |
| `EndRouteCard` | İsteğe bağlı | Numaralandırma (Evet \| Hayır) |
| `PostNow` | İsteğe bağlı | Numaralandırma (Evet \| Hayır) |
| `AutoUpdate` | İsteğe bağlı | Numaralandırma (Evet \| Hayır) |
| `ProductColorId` | İsteğe bağlı | Dize|
| `ProductConfigurationId` | İsteğe bağlı | Dize |
| `ProductSizeId` | İsteğe bağlı | Dize |
| `ProductStyleId` | İsteğe bağlı | Dize |
| `ProductVersionId` | İsteğe bağlı | Dize |
| `ItemBatchNumber` | İsteğe bağlı | Dize |
| `ProductSerialNumber` | İsteğe bağlı | Dize |
| `LicensePlateNumber` | İsteğe bağlı | Dize |
| `InventoryStatusId` | İsteğe bağlı | Dize |
| `ProductionWarehouseId` | İsteğe bağlı | Dize |
| `ProductionSiteId` | İsteğe bağlı | Dize |
| `ProductionWarehouseLocationId` | İsteğe bağlı | Dize |
| `InventoryDimension1` - `InventoryDimension12` | İsteğe bağlı | Dize |

12 genişletilebilir boyut ( `InventoryDimension1` - `InventoryDimension12`) özelleştirme gerektirir ve her zaman kullanılmaz. Bunlar hakkında daha fazla bilgi için bkz. [Genişletme aracılığıyla yeni stok boyutları ekleme](../../fin-ops-core/dev-itpro/extensibility/inventory-dimensions.md).

### <a name="material-consumption-picking-list-message"></a>Malzeme tüketimi (malzeme çekme listesi) iletisi

*Malzeme tüketimi (malzeme çekme listesi)* iletisinde, `_messageType`değeri: `ProdProductionOrderPickingList`. Aşağıdaki tabloda bu iletinin desteklediği alanlar gösterilmektedir.

| Alan adı | Çalıştırma Durumu | Tür |
|---|---|---|
| `ProductionOrderNumber` | Zorunlu | Dize |
| `JournalNameId` | İsteğe bağlı | Dize |
| `PickingListLines` | Zorunlu | Her biri bir sonraki tabloda açıklanan yükü içeren bir satır listesi (en az bir) |

Aşağıdaki tabloda, `ProdProductionOrderPickingList` iletisinin `PickingListLines` bölümündeki her bir satırın desteklediği alanlar gösterilmektedir.

| Alan adı | Çalıştırma Durumu | Tür |
|---|---|---|
| `ItemNumber` | Zorunlu | Dize |
| `ConsumptionBOMQuantity` | İsteğe bağlı | Gerçek |
| `ProposalBOMQuantity` | İsteğe bağlı | Gerçek |
| `ScrapBOMQuantity` | İsteğe bağlı | Gerçek |
| `BOMUnitSymbol` | İsteğe bağlı | Dize |
| `ConsumptionInventoryQuantity` | İsteğe bağlı | Gerçek |
| `ProposalInventoryQuantity` | İsteğe bağlı | Gerçek |
| `ConsumptionCatchWeightQuantity` | İsteğe bağlı | Gerçek |
| `ProposalCatchWeightQuantity` | İsteğe bağlı | Gerçek |
| `ConsumptionDate` | İsteğe bağlı | Tarih |
| `OperationNumber` | İsteğe bağlı | Tamsayı |
| `LineNumber` | İsteğe bağlı | Gerçek |
| `PositionNumber` | İsteğe bağlı | Dize |
| `IsConsumptionEnded` | İsteğe bağlı | Numaralandırma (Evet \| Hayır) |
| `ErrorCause` | İsteğe bağlı | Enum (Hiçbiri \| Malzeme \| Makine \| OperatingStaff), genişletilebilir |
| `InventoryLotId` | İsteğe bağlı | Dize |

### <a name="time-used-for-operation-route-card-message"></a>Operasyon (rota kartı) için kullanılan zaman iletisi

*Operasyon (rota kartı) için kullanılan zaman* iletisinde, `_messageType` değeri: `ProdProductionOrderRouteCard`. Aşağıdaki tabloda bu iletinin desteklediği alanlar gösterilmektedir.

| Alan adı | Çalıştırma Durumu | Tür |
|---|---|---|
| `ProductionOrderNumber` | Zorunlu | Dize |
| `JournalNameId` | İsteğe bağlı | Dize |
| `RouteCardLines` | Zorunlu | Her biri bir sonraki tabloda açıklanan yükü içeren bir satır listesi (en az bir) |

Aşağıdaki tabloda, `ProdProductionOrderRouteCard` iletisinin `RouteCardLines` bölümündeki her bir satırın desteklediği alanlar gösterilmektedir.

| Alan adı | Çalıştırma Durumu | Tür |
|---|---|---|
| `OperationNumber` | Zorunlu | Tamsayı |
| `OperationPriority` | İsteğe bağlı | Enum (Birincil \| İkincil1 \| İkincil2 \| ... \| İkincil20) |
| `OperationId` | İsteğe bağlı | Dize |
| `OperationsResourceId` | İsteğe bağlı | Dize |
| `Worker` | İsteğe bağlı | Dize |
| `HoursRouteCostCategoryId` | İsteğe bağlı | Dize |
| `QuantityRouteCostCategoryId` | İsteğe bağlı | Dize |
| `HourlyRate` | İsteğe bağlı | Gerçek |
| `Hours` | İsteğe bağlı | Gerçek |
| `GoodQuantity` | İsteğe bağlı | Gerçek |
| `ErrorQuantity` | İsteğe bağlı | Gerçek |
| `CatchWeightGoodQuantity` | İsteğe bağlı | Gerçek |
| `CatchWeightErrorQuantity` | İsteğe bağlı | Gerçek |
| `QuantityPrice` | İsteğe bağlı | Gerçek |
| `ProcessingPercentage` | İsteğe bağlı | Gerçek |
| `ConsumptionDate` | İsteğe bağlı | Tarih |
| `TaskType` | İsteğe bağlı | Enum (QueueBefore \| Kurulum \| Süreç \| Çakışma \| Taşıma \| QueueAfter \| Yük) |
| `ErrorCause` | İsteğe bağlı | Enum (Hiçbiri \| Malzeme \| Makine \| OperatingStaff), genişletilebilir |
| `OperationCompleted` | İsteğe bağlı | Numaralandırma (Evet \| Hayır) |
| `BOMConsumption` | İsteğe bağlı | Numaralandırma (Evet \| Hayır) |
| `ReportAsFinished` | İsteğe bağlı | Numaralandırma (Evet \| Hayır) |

### <a name="end-production-order-message"></a>Bir üretim emri iletisi bitirin

*Üretim emri bitişi* iletisi için `_messageType` değeri: `ProdProductionOrderEnd`. Aşağıdaki tabloda bu iletinin desteklediği alanlar gösterilmektedir.

| Alan adı | Çalıştırma Durumu | Tür |
|---|---|---|
| `ProductionOrderNumber` | Zorunlu | Dize |
| `ExecutedDateTime` | İsteğe bağlı | Tarih/Saat |
| `EndedDate` | İsteğe bağlı | Tarih |
| `UseTimeAndAttendanceCost` | İsteğe bağlı | Numaralandırma (Evet \| Hayır) |
| `AutoReportAsFinished` | İsteğe bağlı | Numaralandırma (Evet \| Hayır) |
| `AutoUpdate` | İsteğe bağlı | Numaralandırma (Evet \| Hayır) |

## <a name="other-production-information"></a>Diğer üretim bilgileri

İletiler atölyede gerçekleşen eylemleri veya olayları destekler. Bunlar bu makalede açıklanan MES tümleştirme çerçevesi kullanılarak işlenir. Tasarım, MES ile paylaşılacak diğer başvuru bilgilerinin (ürünle ilgili bilgiler veya ürün reçetesi ya da belirli bir üretim emrinde kullanılan rota (belirli kurulum ve yapılandırma süreleriyle birlikte) gibi) dosya aktarımı veya OData aracılığıyla [veri varlıkları](../../fin-ops-core/dev-itpro/data-entities/data-entities-data-packages.md#data-entities) kullanılarak sistemden alınacağını varsayar.

## <a name="receive-feedback-about-the-state-of-a-message"></a>İletinin durumu hakkında geribildirim alma

MES, Supply Chain Management'a bir ileti gönderdikten sonra, Supply Chain Management'ın iletinin durumuyla ilgili geribildirim döndürmesine uygun olabilir. Bu davranışın ilgili olabileceği durumlara yönelik birkaç örnek aşağıda gösterilmiştir:

- MES tümleştirmesini sürekli gözlemekten sorumlu kimse yoktur.
- MES tümleştirmesini izlemekten sorumlu olan kişi, bir ileti başarısız olduğunda e-posta yoluyla bildirilmesini istiyordur ki eyleme geçmesi gerektiğini bilsin.
- MES, BT departmanına veya atölye operatörüne eyleme geçmeleri gerektiğini bildiren bir hata iletisi göstermelidir.
- Bir hata iletisi aldıktan sonra (örneğin bir üretim emri başlatılamadığında) MES, sipariş zamanlamasını yeniden hesaplamalıdır.

Bu gibi durumlarda, Supply Chain Management'ta standart uyarı özelliğinden yararlanabilirsiniz. Standart uyarıların nasıl çalıştığı hakkında bilgi için, aşağıdaki kaynaklara bakın:

- Yardım makalesi: [Uyarılara genel bakış](../../fin-ops-core/fin-ops/get-started/alerts-overview.md)
- Video: [Finans ve operasyon uygulamalarında uyarı kuralı seçenekleri](https://www.youtube.com/watch?v=cpzimwOjicM&ab_channel=MicrosoftDynamics365)

Örneğin, bir iletinin durumu hakkında geribildirim sağlamak için aşağıdaki uyarıları ayarlayabilirsiniz:

- İleti *Başarısız* olduğunda kullanılan bir iş olayı ("Harici gönder") oluşturun.
- BT yöneticisine veya atölye yöneticisine bir bildirim ve e-posta gönderin.

