---
title: Seyahat oluşturma varlıkları
description: Bu makalede, seyahat oluşturmak için gerekli veri varlıklarını gruplandıran seyahat oluşturma veri varlıkları hakkında bilgi sağlanır.
author: yufeihuang
ms.date: 05/27/2022
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yufeihuang
ms.search.validFrom: 2022-05-27
ms.dyn365.ops.version: 10.0.28
ms.openlocfilehash: 6234dfa61a5859e2ecaca75594c69c49ba326629
ms.sourcegitcommit: 5b34b41ae74269ba639e2876bc5862ef468da1cc
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/15/2022
ms.locfileid: "9167686"
---
# <a name="voyage-creation-entities"></a>Seyahat oluşturma varlıkları

[!include [banner](../includes/banner.md)]

Seyahat oluşturma veri varlıkları, seyahat oluşturmak için gerekli veri varlıklarını gruplandırır. Siz veya nakliye aracınız, mevcut satınalma siparişi veya transfer emri satırlarına başvuran seyahat, sevkiyat konteyneri, folyo ve seyahat satırı kayıtları oluşturmak için bu veri varlıklarını kullanabilirsiniz.

## <a name="voyages-itmtableentity"></a>Seyahatler (ITMTableEntity)

Seyahat, gelen malların yolculuğunu temsil eder ve Son teslim alma maliyetindeki en üst düzey maliyet alanıdır. Gemi, çıkış limanı ve hedef limanı ile ilgili üst bilgi düzeyinde bilgiler içerir. Bu işlev, `ITMTableEntity` varlığı tarafından desteklenir. Aşağıdaki tabloda, bu varlığı oluşturan alanlar ve eşlemeler listelenmektedir.

| Adı | Eşleme | Veri türü | Anahtar | Zorunlu |
|---|---|---|---|---|
| Teslimat şekli | ITMTable.DlvModeId | Nvarchar(10) | No. | No. |
| Aracı tarafından önerilir | ITMTable.ITMBrokerAdvised | Datetime | No. | No. |
| Müşteri randevusu | ITMTable.ITMCustomerAppointment | Datetime | No. | No. |
| Ambara teslim edildi | ITMTable.ITMDelAtWarehouse | Datetime | No. | No. |
| Teslimat talimatları | ITMTable.ITMDeliveryInstructions | Datetime | No. | No. |
| Yola çıkış tarihi | ITMTable.ITMDepartureDate | Datetime | No. | No. |
| Piyasaya sürülen mallar | ITMTable.ITMGoodsReleased | Datetime | No. | No. |
| Yerel taşıma tarihi | ITMTable.ITMLocalTransportDate | Datetime | No. | No. |
| Yerel taşıma saati | ITMTable.ITMLocalTransportTime | Int | No. | No. |
| Gönderilen orijinal konşimento | ITMTable.ITMOriginalBOLSebt | Datetime | No. | No. |
| Alınan orijinal belgeler | ITMTable.ITMOriginalDocsReceived | Datetime | No. | No. |
| Satın alma siparişi durumu | ITMTable.ITMPurchStatus | Int | No. | No. |
| Doğrulama tarihi | ITMTable.ITMVerificationDate | Datetime | No. | No. |
| Gümrük girişi tanımlayıcı | ITMTable.ShipCustomsEntryId | Nvarchar(20) | No. | No. |
| Sevk tarihi | ITMTable.ShipDate | Datetime | No. | No. |
| Açıklama | ITMTable.ShipDescription | Nvarchar(60) | No. | No. |
| Belgeler alındı | ITMTable.ShipDocReceived | Int | No. | No. |
| Tahmini teslim tarihi | ITMTable.ShipEstDlvDate | Datetime | No. | No. |
| Sevkiyat limanındaki ETA | ITMTable.ShipEstPortDate | Datetime | No. | No. |
| Çıkış limanı | ITMTable.ShipFromPort | Nvarchar(20) | No. | No. |
| Ara irsaliye/Konşimento | ITMTable.ShipHAWB | Nvarchar(20) | No. | No. |
| Seyahat | ITMTable.ShipId | Nvarchar(20) | **Evet** | **Evet** |
| Defter tutma referansı | ITMTable.ShipIdExternal | Nvarchar(20) | No. | No. |
| Yolculuk şablonu | ITMTable.ShipJourneyId | Nvarchar(20) | No. | No. |
| Yerel aracı | ITMTable.ShipLocalForwarder | Nvarchar(20) | No. | No. |
| Ana hava yolu irsaliyesi/Konşimento | ITMTable.ShipMAWB | Nvarchar(20) | No. | No. |
| Ölçüm | ITMTable.ShipMeasurement | Numeric(32, 6) | No. | No. |
| Ölçüm birimi | ITMTable.ShipMeasurementUnit | Int | No. | No. |
| Palet sayısı | ITMTable.ShipNoOfPallets | Int | No. | No. |
| Bekleyen seyahat | ITMTable.ShipPending | Int | No. | No. |
| Açıklamalar | ITMTable.ShipRemarks | Nvarchar(MAX) | No. | No. |
| Kiralık | ITMTable.ShipRental | Int | No. | No. |
| Seyahat durumu | ITMTable.ShipStatusId | Nvarchar(20) | No. | No. |
| Sayı cinsinden çetele | ITMTable.ShipTallyInNumber | Nvarchar(20) | No. | No. |
| Varış limanı | ITMTable.ShipToPort | Nvarchar(20) | No. | No. |
| Değerleme tarihi | ITMTable.ShipValuationDate | Datetime | No. | No. |
| Sevkiyat şirketi | ITMTable.ShipVendAccount | Nvarchar(20) | No. | No. |
| Tekne | ITMTable.ShipVesselId | Nvarchar(20) | No. | **Evet** |
| Seyahat harici kimliği | ITMTable.ShipVoyage | Nvarchar(20) | No. | No. |

### <a name="number-sequences-for-voyages"></a>Seyahatler için numara serileri

Seyahatler için paylaşılan numara serisi, seyahat kodlarının tahsisatını denetler.

Veri varlığına **Seyahat Kimliği** (`ShipId`) değeri olarak geçirilen değer, güncelleştirme için mevcut bir kaydı tanımlamak amacıyla kullanılır. Söz konusu kayıt yoksa davranış, atanan numara serisinin el ile girişe izin verecek şekilde yapılandırılıp yapılandırılmamasına bağlıdır:

- El ile giriş etkinse, aktarılan değeri kullanan yeni bir kayıt oluşturulur.
- El ile giriş etkin değilse, aktarılan değer yerine, atanan numara serisindeki bir sonraki numara kullanılır.

İçeri aktarma oturumu sırasında, seyahat kimliği olarak içeri aktarılan yer tutucu değeri korunur. Bu davranış, yer tutucuya başvuran sevkiyat konteyneri ve seyahat satırlarının seyahate eklenmesini ve numara serisinden atanan değeri yansıtacak şekilde güncelleştirilmesini sağlar.

### <a name="automatic-cost-transactions"></a>Otomatik maliyet hareketleri

Otomatik maliyetler, Microsoft Dynamics 365 Supply Chain Management'taki **Otomatik maliyetler** sayfasından seyahate eklenebilir (**Son teslim alma maliyeti \> Maliyetlendirme kurulumu \> Otomatik maliyetler**). Otomatik maliyet kayıtları, Son teslim alma maliyetinin desteklediği her maliyet alanı için maliyet hareketi veri varlıkları kullanılarak da oluşturulabilir.

Seyahat satırı oluşturulduğunda, Supply Chain Management'ta yapılandırılan otomatik maliyetler seyahatte uygulanır. Üst bilgi kaydı satır bilgileriyle ilişkilendirilene kadar kayıtta hiçbir maliyet görünür olmayacaktır.

## <a name="shipping-containers-itmcontainersentity"></a>Sevkiyat konteynerleri (ITMContainersEntity)

Sevkiyat konteyneri, malların içinde bulunduğu fiziksel bir konteyneri temsil eder. Bu fiziksel konteyner, gemi yükü için yük konteyneri veya uçak yükü için tekli palet olabilir. Sevkiyat konteyneri; sevkiyat konteyneri kimliği, mühür numarası ve sevkiyat konteyneri türü ile ilgili üst bilgi düzeyinde bilgiler içerir. (Sevkiyat konteyneri türü boyut bilgileri sağlar.) Bu işlev, `ITMContainersEntity` varlığı tarafından desteklenir. Aşağıdaki tabloda, bu varlığı oluşturan alanlar ve eşlemeler listelenmektedir.

| Adı | Eşleme | Veri türü | Anahtar | Zorunlu |
|---|---|---|---|---|
| Yola çıkış tarihi | ITMContainers.ITMDepartureDate | Datetime | No. | No. |
| Yerel taşıma tarihi | ITMContainers.ITMLocalTransportDate | Datetime | No. | No. |
| Yerel taşıma saati | ITMContainers.ITMLocalTransportTime | Int | No. | No. |
| Orijinal seyahat | ITMContainers.OrigShipId | Nvarchar(20) | No. | No. |
| Gerçek ağırlık | ITMContainers.ShipActualWeight | Numeric(32, 6) | No. | No. |
| Aracı tarafından önerilir | ITMContainers.ShipBrokerAdvised | Datetime | No. | No. |
| Sevkiyat konteyneri | ITMContainers.ShipContainerId | Nvarchar(20) | **Evet** | **Evet** |
| Sevkiyat konteyneri türü | ITMContainers.ShipContainerTypeId | Nvarchar(20) | No. | No. |
| Birim türü | ITMContainers.ShipContainerUnitTypeId | Nvarchar(10) | No. | No. |
| Kiralamaya dönüştürüldü | ITMContainers.ShipConvertedToRental | Int | No. | No. |
| Müşteri randevusu | ITMContainers.ShipCustomerAppointment | Datetime | No. | No. |
| Sevk tarihi | ITMContainers.ShipDate | Datetime | No. | No. |
| Ambara teslim edildi | ITMContainers.ShipDelAtWarehouse | Datetime | No. | No. |
| Teslimat talimatları | ITMContainers.ShipDeliveryInstructions | Datetime | No. | No. |
| Muayene belgesinin geçerli olduğu tarih | ITMContainers.ShipECAppliedDate | Datetime | No. | No. |
| Muayene belgesinin sona erme tarihi | ITMContainers.ShipECExpiryDate | Datetime | No. | No. |
| Muayene belgesi numarası | ITMContainers.ShipECNum | Nvarchar(20) | No. | No. |
| Muayene belgesinin alınma tarihi | ITMContainers.ShipECReceivedDate | Datetime | No. | No. |
| Tahmini teslim tarihi | ITMContainers.ShipEstDlvDate | Datetime | No. | No. |
| Sevkiyat limanındaki ETA | ITMContainers.ShipEstPortDate | Datetime | No. | No. |
| Beklenen yükleme tarihi | ITMContainers.ShipExpectedLoadingDate | Datetime | No. | No. |
| Çıkış limanı | ITMContainers.ShipFromPort | Nvarchar(20) | No. | No. |
| Malların açıklaması | ITMContainers.ShipGoodsDesc | Nvarchar(60) | No. | No. |
| Piyasaya sürülen mallar | ITMContainers.ShipGoodsReleased | Datetime | No. | No. |
| GPS takip birimi | ITMContainers.ShipGPSUnit | Nvarchar(30) | No. | No. |
| Ara irsaliye/Konşimento | ITMContainers.ShipHAWB | Nvarchar(20) | No. | No. |
| Seyahat | ITMContainers.ShipId | Nvarchar(20) | **Evet** | **Evet** |
| Yolculuk şablonu | ITMContainers.ShipJourneyId | Nvarchar(20) | No. | No. |
| Yerel aracı | ITMContainers.ShipLocalForwarder | Nvarchar(20) | No. | No. |
| Ölçüm | ITMContainers.ShipMeasurement | Numeric(32, 6) | No. | No. |
| Ölçüm birimi | ITMContainers.ShipMeasurementUnit | Int | No. | No. |
| Karton sayısı | ITMContainers.ShipNoOfCartons | Numeric(32, 6) | No. | No. |
| Gönderilen orijinal konşimento | ITMContainers.ShipOriginalBOLSebt | Datetime | No. | No. |
| Alınan orijinal belgeler | ITMContainers.ShipOriginalDocsReceived | Datetime | No. | No. |
| Mühür numaramız | ITMContainers.ShipOurSealNum | Nvarchar(20) | No. | No. |
| Kullanılan | ITMContainers.ShipPendingUsed | Int | No. | No. |
| Satın alma siparişi durumu | ITMContainers.ShipPurchStatus | Int | No. | No. |
| Soğutma türü | ITMContainers.ShipRefrigerationTypeId | Nvarchar(10) | No. | No. |
| Açıklamalar | ITMContainers.ShipRemarks | Nvarchar(MAX) | No. | No. |
| Kiralık | ITMContainers.ShipRental | Int | No. | No. |
| İade edilebilir | ITMContainers.ShipReturnable | Int | No. | No. |
| Seyahat durumu | ITMContainers.ShipStatusId | Nvarchar(20) | No. | No. |
| Sevkiyat şirketi mühür numarası | ITMContainers.ShipTheirSealNum | Nvarchar(20) | No. | No. |
| Varış limanı | ITMContainers.ShipToPort | Nvarchar(20) | No. | No. |
| Doğrulama tarihi | ITMContainers.ShipVerificationDate | Datetime | No. | No. |
| Tekne | ITMContainers.ShipVesselId | Nvarchar(20) | No. | **Evet** |

### <a name="voyage-id-validation"></a>Seyahat kimliği doğrulaması

Sevkiyat konteyneri kodu bir numara serisiyle kontrol edilmez. Yalnızca kullanıldığı seyahat bağlamında benzersizdir.

Sevkiyat konteyneri varlığı (`ITMContainersEntity`), seyahat varlığından (`ITMTableEntity`) bağımsız olarak kullanılıyorsa **Seyahat Kimliği** (`ShipId`) değeri seyahat tablosundaki mevcut bir değerle eşleşmelidir. Aksi durumda içeri aktarma başarısız olur.

Sevkiyat konteyneri varlığı (`ITMContainersEntity`) ve seyahat varlığı (`ITMTableEntity`) aynı içeri aktarma oturumunun parçası olarak kullanılıyorsa, seyahat varlığı sevkiyat konteynerinden önce oluşturulmalıdır. Aksi takdirde, **Seyahat Kimliği** (`ShipId`) değeri başarıyla doğrulanamaz. **Seyahat kimliği** (`ShipId`) değeri için yer tutucu değeri kullanılıyorsa ilişkilendirme, yalnızca aynı yer tutucunun sevkiyat konteyneri varlığında **Seyahat Kimliği** (`ShipId`) olarak kullanılması durumunda oluşturulabilir.

### <a name="other-field-validations"></a>Diğer alan doğrulamaları

Aşağıdaki tabloda, Son teslim alma maliyeti kurulum tablolarıyla karşılaştırılarak doğrulanan sevkiyat konteyneri tablosundaki (`ITMContainers`) alanlar gösterilmiştir. Ayrıca, bir nakliye aracısının mevcut değerleri okumak ve ortamınızda geçerli değerler alınmasını sağlamak için kullanabileceği Son teslim alma maliyeti veri varlıklarını da gösterir.

| ITMContainers tablosundaki alan | Son teslim alma maliyeti veri varlığı |
|---|---|
| Sevkiyat konteyneri türü | ITMShippingContainerTypeEntity |
| Malların açıklaması | ITMGoodsDescriptionEntity |
| Soğutma türü | ITMShippingContainerRefrigerationTypeEntity |

## <a name="folios-itmfolioentity"></a>Folyolar (ITMFolioEntity)

Folyo, gümrük beyanı için sevkiyat konteynerindeki maddelerin gruplandırılmasını temsil eder. Folyo, gümrük müşaviri ve malların açıklaması ile ilgili üst bilgi düzeyindeki bilgileri içerir. Bu işlev, `ITMFolioEntity` varlığı tarafından desteklenir. Aşağıdaki tabloda, bu varlığı oluşturan alanlar ve eşlemeler listelenmektedir.

| Adı | Eşleme | Veri türü | Anahtar | Zorunlu |
|---|---|---|---|---|
| Aracı tarafından önerilir | ITMFolioTable.ShipBrokerAdvised | Datetime | No. | No. |
| Kargo kontrol numarası | ITMFolioTable.ShipCargoControlNumber | Nvarchar(20) | No. | No. |
| Müşteri randevusu | ITMFolioTable.ShipCustomerAppointment | Datetime | No. | No. |
| Gümrük müşaviri | ITMFolioTable.ShipCustomsBroker | Nvarchar(20) | No. | No. |
| Gümrük Kimliği | ITMFolioTable.ShipCustomsId | Nvarchar(60) | No. | No. |
| Şirket | ITMFolioTable.ShipDataArea | Nvarchar(4) | No. | **Evet** |
| Ambara teslim edildi | ITMFolioTable.ShipDelAtWarehouse | Datetime | No. | No. |
| Teslimat talimatları | ITMFolioTable.ShipDeliveryInstructions | Datetime | No. | No. |
| Belgeler alındı | ITMFolioTable.ShipDocReceived | Int | No. | No. |
| Tahmini teslim tarihi | ITMFolioTable.ShipEstDlvDate | Datetime | No. | No. |
| Sevkiyat limanındaki ETA | ITMFolioTable.ShipEstPortDate | Datetime | No. | No. |
| İhracatçı | ITMFolioTable.ShipExporterId | Nvarchar(20) | No. | No. |
| Adı | ITMFolioTable.ShipExporterName | Nvarchar(60) | No. | No. |
| Folyo tarihi | ITMFolioTable.ShipFolioDate | Datetime | No. | No. |
| Folyo | ITMFolioTable.ShipFolioId | Nvarchar(20) | **Evet** | **Evet** |
| Çıkış limanı | ITMFolioTable.ShipFromPort | Nvarchar(20) | No. | No. |
| Malların açıklaması | ITMFolioTable.ShipGoodsDesc | Nvarchar(60) | No. | No. |
| Piyasaya sürülen mallar | ITMFolioTable.ShipGoodsReleased | Datetime | No. | No. |
| Ara irsaliye/Konşimento | ITMFolioTable.ShipHAWB | Nvarchar(20) | No. | No. |
| Seyahat | ITMFolioTable.ShipId | Nvarchar(20) | No. | **Evet** |
| Ölçüm | ITMFolioTable.ShipMeasurement | Numeric(32, 6) | No. | No. |
| Ölçüm birimi | ITMFolioTable.ShipMeasurementUnit | Int | No. | No. |
| Karton sayısı | ITMFolioTable.ShipNoOfCartons | Numeric(32, 6) | No. | No. |
| Gönderilen orijinal konşimento | ITMFolioTable.ShipOriginalBOLSebt | Datetime | No. | No. |
| Alınan orijinal belgeler | ITMFolioTable.ShipOriginalDocsReceived | Datetime | No. | No. |
| Satın alma siparişi durumu | ITMFolioTable.ShipPurchStatus | Int | No. | No. |
| Açıklamalar | ITMFolioTable.ShipRemarks | Nvarchar(MAX) | No. | No. |
| Seyahat durumu | ITMFolioTable.ShipStatusId | Nvarchar(20) | No. | No. |
| Tarife kodu | ITMFolioTable.ShipTariffCode | Nvarchar(10) | No. | No. |
| Varış limanı | ITMFolioTable.ShipToPort | Nvarchar(20) | No. | No. |
| Değerleme tarihi | ITMFolioTable.ShipValuationDate | Datetime | No. | No. |
| Doğrulama tarihi | ITMFolioTable.ShipVerificationDate | Datetime | No. | No. |
| Satıcı hesabı | ITMFolioTable.VendAccount | Nvarchar(20) | No. | No. |

### <a name="number-sequences-for-folios"></a>Folyolar için numara serileri

Folyolar için numara serisi, folyo kimliklerinin tahsisatını denetler.

Veri varlığına **Folyo Kimliği** (`FolioId`) değeri olarak geçirilen değer, güncelleştirme için mevcut bir kaydı tanımlamak amacıyla kullanılır. Söz konusu kayıt yoksa davranış, atanan numara serisinin el ile girişe izin verecek şekilde yapılandırılıp yapılandırılmamasına bağlıdır:

- El ile giriş etkinse, aktarılan değeri kullanan yeni bir kayıt oluşturulur.
- El ile giriş etkin değilse, aktarılan değer yerine, atanan numara serisindeki bir sonraki numara kullanılır.

İçeri aktarma oturumu sırasında, folyo kimliği olarak içeri aktarılan yer tutucu değeri korunur. Bu davranış, yer tutucuya başvuran seyahat satırlarının doğru şekilde ilişkilendirilmesini ve numara serisinden atanan değeri yansıtacak şekilde güncelleştirilmesini sağlar.

### <a name="field-validations"></a>Alan doğrulamaları

Folyo tablosundaki (`ITMFolioTable`) **Malların açıklaması** alanı, aynı ada sahip Son teslim alma maliyeti kurulum tablosuyla karşılaştırılarak doğrulanır. Bir nakliye aracısı, mevcut değerleri okumak ve ortamınızda geçerli değerler alınmasını sağlamak için `ITMGoodsDescriptionEntity` Son teslim alma maliyeti veri varlığını kullanabilir.

## <a name="voyage-lines-for-purchase-orders-itmpurchaselineentity"></a>Satınalma siparişleri için seyahat satırları (ITMPurchaseLineEntity)

Seyahat satırı, seyahate dahil olan tek bir satınalma siparişi satırını temsil eder. Bu ilişki, **Satınalma siparişi numarası** ve **Satınalma satır numarası** alanları aracılığıyla oluşturulur. Seyahat satırı; seyahat, sevkiyat konteyneri ve folyo için oluşturulan tüm önceki kayıtlara başvurur. Bu işlev, `ITMPurchaseLineEntity` varlığı tarafından desteklenir. Aşağıdaki tabloda, bu varlığı oluşturan alanlar ve eşlemeler listelenmektedir.

| Adı | Eşleme | Veri türü | Anahtar | Zorunlu |
|---|---|---|---|---|
| Para birimi | ITMLine.CurrencyCode | Nvarchar(3) | No. | No. |
| Net tutar | ITMLine.LineAmountMST | Numeric(32, 6) | No. | No. |
| Satınalma satır numarası | ITMLine.RefRecId | Numeric(32, 6) | **Evet** | No. |
| Sevkiyat konteyneri | ITMLine.ShipContainerId | Int | No. | No. |
| Şirket | ITMLine.ShipDataArea | Nvarchar(20) | **Evet** | No. |
| Beyan edilen miktar | ITMLine.ShipDeclaredQty | Nvarchar(4) | No. | No. |
| Folyo | ITMLine.ShipFolioId | Numeric(32, 6) | No. | No. |
| Seyahat | ITMLine.ShipId | Nvarchar(20) | **Evet** | No. |
| Madde numarası | ITMLine.ShipItemId | Nvarchar(20) | No. | No. |
| Ölçüm | ITMLine.ShipMeasurement | Nvarchar(20) | No. | No. |
| Ölçüm birimi | ITMLine.ShipMeasurementUnit | Numeric(32, 6) | No. | No. |
| Karton sayısı | ITMLine.ShipNoOfCartons | Int | No. | No. |
| Konum | ITMLine.ShipPosition | Numeric(32, 6) | No. | No. |
| Miktar | ITMLine.ShipQty | Int | No. | No. |
| Satın alma siparişi numarası | ITMLine.TransRefId | Numeric(32, 6) | **Evet** | No. |
| Birim | ITMLine.UnitId | Int | No. | No. |
| Hacim | ITMLine.Volume | Nvarchar(10) | No. | No. |
| Ağırlık | ITMLine.Weight | Numeric(32, 6) | No. | No. |

## <a name="voyage-lines-for-transfer-orders-itmtransferlineentity"></a>Transfer emirleri için seyahat satırları (ITMTransferLineEntity)

Seyahat satırı, seyahate dahil olan tek bir transfer emri satırını temsil eder. Bu ilişki, **Transfer emri numarası** ve **Transfer satır numarası** alanları aracılığıyla oluşturulur. Seyahat satırı; seyahat, sevkiyat konteyneri ve folyo için oluşturulan tüm önceki kayıtlara başvurur. Bu işlev, `ITMTransferLineEntity` varlığı tarafından desteklenir. Aşağıdaki tabloda, bu varlığı oluşturan alanlar ve eşlemeler listelenmektedir.

| Adı | Eşleme | Veri türü | Anahtar | Zorunlu |
|---|---|---|---|---|
| Para birimi | ITMLine.CurrencyCode | Nvarchar(3) | No. | No. |
| Net tutar | ITMLine.LineAmountMST | Numeric(32, 6) | No. | No. |
| Sevkiyat konteyneri | ITMLine.ShipContainerId | Int | No. | No. |
| Şirket | ITMLine.ShipDataArea | Nvarchar(20) | **Evet** | No. |
| Beyan edilen miktar | ITMLine.ShipDeclaredQty | Nvarchar(4) | No. | No. |
| Folyo | ITMLine.ShipFolioId | Numeric(32, 6) | No. | No. |
| Seyahat | ITMLine.ShipId | Nvarchar(20) | **Evet** | No. |
| Madde numarası | ITMLine.ShipItemId | Nvarchar(20) | No. | No. |
| Ölçüm | ITMLine.ShipMeasurement | Nvarchar(20) | No. | No. |
| Ölçüm birimi | ITMLine.ShipMeasurementUnit | Numeric(32, 6) | No. | No. |
| Karton sayısı | ITMLine.ShipNoOfCartons | Int | No. | No. |
| Konum | ITMLine.ShipPosition | Numeric(32, 6) | No. | No. |
| Miktar | ITMLine.ShipQty | Int | No. | No. |
| Transfer satır numarası | ITMLine.TransferLineNumber | Numeric(32, 6) | **Evet** | No. |
| Transfer emri numarası | ITMLine.TransRefId | Numeric(32, 6) | **Evet** | No. |
| Birim | ITMLine.UnitId | Int | No. | No. |
| Hacim | ITMLine.Volume | Nvarchar(10) | No. | No. |
| Ağırlık | ITMLine.Weight | Numeric(32, 6) | No. | No. |

### <a name="reference-table"></a>Referans tablosu

Seyahat satırları açık bir gelen sipariş satırıyla kurulan ilişki üzerinden oluşturulur. Bu satır bir satınalma siparişinde bulunabilir veya bir transfer emrindeki teslim alma hareketi olabilir. Seyahat satırı tablosundaki (`ITMLine`) `RefTableId` alanı, tablo numarasına başvurarak satırın hangi sipariş türü ile ilişkili olduğunu belirtir. Verilerin oluşturulduğu tabloda belirli tablo numaralarına başvuruda bulunuluyorsa, varlıklar bu değerlere göre bölünür.

Referans tablosu (`RefTableId`) ve hareket türü (`TransType`) değerleri, Son teslim alma maliyeti satınalma satırı varlığı veya Son teslim alma maliyeti transfer satırı varlığı seçiminde örtüktür.

### <a name="validation"></a>Doğrulama

Seyahat satırı, doğrudan seyahat kaydına, sevkiyat konteyneri kaydına ve folyo kaydına başvuruda bulunur. Satınalma satırı varlığı (`ITMPurchaseLinesEntity`) veya transfer satırı varlığı (`ITMPurchaseLinesEntity`), bu başvuru kayıtlarını oluşturmak için kullanılan varlıklardan bağımsız olarak kullanıldıysa **Seyahat Kimliği** (`ShipId`), **Sevkiyat konteyneri** (`ShipContainerId`) ve **Folyo** (`ShipFolioId`) değerleri ilgili tablolardaki mevcut bir kayıtla eşleşmelidir. Aksi durumda içeri aktarma başarısız olur.

İki satır varlığından herhangi biri aynı içeri aktarma oturumunun parçası olarak kullanılırsa, bu diğer varlıklar seyahat satırından önce oluşturulmalıdır. Aksi takdirde, değerler başarıyla doğrulanamaz. Seyahat veya folyo numarası için yer tutucu değeri kullanılıyorsa ilişkilendirme, yalnızca aynı yer tutucunun seyahat satırı varlığında seyahat veya folyo numarası olarak kullanılması durumunda oluşturulabilir.

Satınalma siparişi veya transfer emri satırı mevcut bir seyahat satırına zaten atanmışsa, yeni seyahat satırı oluşturulmaz. Sipariş satırının yeni bir seyahate atanabilmesi için önce geçerli yolculuğundan kaldırılması gerekir.

### <a name="order-line-identification"></a>Sipariş satırı tanımlayıcısı

Seyahat satırları; başvuru **Kayıt Kimliği** (`RefRecId`), **Stok boyutu kimliği** (`InventDimId`) ve **Stok hareketi kimliği** (`InventTransId`) değerlerine doğrudan başvurur. Veri varlığı kullanıldığında artık bu değerlerin eklenmesi gerekmez. Bunun yerine, artık sipariş satırı numarası eklenmelidir. Sipariş satırı numarası ve sipariş numarası, birlikte kullanıldığında bu başvuru değerlerinden her birinin tanımlanmasını sağlar.

### <a name="voyage-line-quantity"></a>Seyahat satırı miktarı

Seyahat satırı doğrudan bir sipariş satırıyla ilişkilendirildiğinden, varlık kullanılarak girilen **Miktar** (`ShipQty`) değeri, değerlerin eşleşmesini gerektirir. Doğrulama, satınalma siparişi satırındaki veya transfer satırındaki miktarla karşılaştırılarak yapılır. Doğrulama başarısız olursa kayıt işlenmez.

### <a name="calculated-fields"></a>Hesaplanan alanlar

**Ağırlık** ve **Hacim** hesaplanan alanları, veri varlığı aracılığıyla alınan değerleri kabul eder. Hiçbir değer sağlanmazsa sistem değerleri varsa bu alanları güncelleştirmek için sistem değerleri kullanılır. Son teslim alma maliyeti için değerler aşağıdaki şekilde hesaplanır:

- *Ağırlık* = *Miktar* × *Maddenin brüt ağırlığı*
- *Hacim* = *Miktar* × (*Maddenin brüt derinliği* × *Maddenin brüt yüksekliği* × *Maddenin brüt genişliği*)

## <a name="sequencing"></a>Sıralama

Tablolar arasındaki bağımlılıklar nedeniyle, önce seyahat kaydı oluşturulmalıdır. Seyahat satırı yalnızca seyahat, sevkiyat konteyneri ve folyolar oluşturulduktan sonra oluşturulabilir.

Sistem, doğrulama uyarıları olmadan seyahat oluşturabilmek için varlıkları aşağıdaki sıraya göre işlemelidir:

1. Seyahatler (`ITMTableEntity`)
1. Sevkiyat konteynerleri (`ITMContainersEntity`)
1. Folyolar (`ITMFolioTableEntity`)
1. Seyahat satırları (`ITMPurchaseLinesEntity` veya `ITMTransferLinesEntity`)
