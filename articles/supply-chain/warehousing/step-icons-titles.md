---
title: Warehouse Management mobil uygulaması için adım simgeleri ve başlıklar atama
description: Bu konuda, Warehouse Management mobil uygulaması için yeni veya özelleştirilmiş görev akışları için adım simgelerinin ve başlıklarının nasıl atandığı açıklanmaktadır.
author: MarkusFogelberg
ms.date: 05/17/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mafoge
ms.search.validFrom: 2021-05-17
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: a74847b50512d2f712e5a9a5125e520afc732591
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/06/2021
ms.locfileid: "6344508"
---
# <a name="assign-step-icons-and-titles-for-the-warehouse-management-mobile-app"></a>Warehouse Management mobil uygulaması için adım simgeleri ve başlıklar atama

[!include [banner](../includes/banner.md)]

Bu konuda, Warehouse Management mobil uygulaması için yeni veya özelleştirilmiş görev akışları için adım simgelerinin ve adım başlıklarının nasıl atandığı açıklanmaktadır.

Aşağıdaki çizimlerde, adım simgelerinin ve başlıkların Warehouse Management mobil uygulamasında nasıl göründüğü gösterilmektedir.

![Warehouse Management mobil uygulamasında adım simgesi ve adım başlığı örneği.](media/step-icon-example.png "Warehouse Management mobil uygulamasında adım simgesi ve adım başlığı örneği")

## <a name="turn-on-this-feature-in-your-system"></a>Sisteminizde bu özelliği etkinleştirme

Bu özelliği kullanabilmeniz için sisteminizde etkinleştirmeniz gerekir. Yöneticiler özellik durumunu denetlemek ve etkinleştirmek için [Özellik yönetimi](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) ayarlarını kullanabilir. **Özellik yönetimi** çalışma alanındabu özellik aşağıdaki şekilde listelenir:

- **Modül:** *Ambar yönetimi*
- **Özellik adı:** *Yeni ambar uygulaması için kullanıcı ayarları, simgeler ve adım başlıkları*

## <a name="standard-step-ids-classes-and-icons"></a>Standart adım kimlikleri, sınıflar ve simgeler

Görev akışındaki her adım bir adım kimliğiyle tanımlanır ve her adım kimliğinin karşılık gelen bir adım sınıfı vardır. Adım simgesi ve başlığı her adım sınıfında belirtilir.

### <a name="step-ids-and-step-classes"></a><a name="step-ids-classes"></a>Adım kimlikleri ve adım sınıfları

Aşağıdaki tabloda, şu anda kullanılabilen her adım kimliği listelenmiştir ve bu, karşılık gelen adım sınıfıdır. Birincil giriş alanının denetim adı adım kimliği olarak kullanılır.

Bu adım kimliklerinin ve sınıflarının nasıl kullanıldığını gösteren bir örnek için, bu konunun sonraki bölümlerinde yer alan [Örnek: Özel akış bölümü için adım simgeleri ve başlıklar atama](#example) bölümünde `WHSMobileAppStepInfoBuilder.stepId()` yöntemin uygulanmasına bakın.

| Adım kodu | Adım Sınıfı |
|-|-|
| BatchDisposition | WHSMobileAppStepBatchDisposition |
| Taşıyıcı | WHSMobileAppStepCarrier |
| CatchWeight | WHSMobileAppStepCatchWeight |
| CatchWeightQtyOutboundWeight | WHSMobileAppStepCatchWeight |
| CatchWeightTag | WHSMobileAppStepCatchWeightTag |
| CatchWeightTagWeight | WHSMobileAppStepCatchWeightTagWeight |
| ChangeWarehouseSuccess | WHSMobileAppStepChangeWarehouseSuccess |
| CheckDigit | WHSMobileAppStepCheckDigit |
| ClusterId | WHSMobileAppStepClusterId |
| ClusterPickQtyVerification | WHSMobileAppStepQtyVerification |
| ClusterPosition | WHSMobileAppStepClusterPosition |
| ConfigId | WHSMobileAppStepConfigId |
| Onay | WHSMobileAppStepConfirmation |
| ConsolidateFromLicensePlateId | WHSMobileAppStepConsolidateFromLicensePlateId |
| ConsolidateLPConfirmation | WHSMobileAppStepConsolidateLPConfirmation |
| ConsolidateToLicensePlateId | WHSMobileAppStepConsolidateToLicensePlateId |
| ContainerType | WHSMobileAppStepContainerType |
| CountingReasonCode | WHSMobileAppStepCountingReasonCode |
| CycleCountingAddLPOrFinish | WHSMobileAppStepCycleCountingAddLPOrFinish |
| CycleCountQty1 | WHSMobileAppStepCycleCountQty |
| CycleCountQty2 | WHSMobileAppStepCycleCountQty |
| CycleCountQty3 | WHSMobileAppStepCycleCountQty |
| CycleCountQty4 | WHSMobileAppStepCycleCountQty |
| Elden Çıkarma | WHSMobileAppStepDisposition |
| DriverCheckInConfirmation | WHSMobileAppStepDriverCheckInConfirmation |
| DriverCheckInId | WHSMobileAppStepDriverCheckInId |
| DriverCheckOutConfirmation | WHSMobileAppStepDriverCheckOutConfirmation |
| DriverCheckOutId | WHSMobileAppStepDriverCheckOutId |
| ExpDate | WHSMobileAppStepExpDate |
| FromBatchDisposition | WHSMobileAppStepFromBatchDisposition |
| FromInventoryStatus | WHSMobileAppStepInventoryStatusFrom |
| FullQty | WHSMobileAppStepFullQty |
| InboundPut | WHSMobileAppStepInboundPut |
| InventBatchId | WHSMobileAppStepBatch |
| InventColorId | WHSMobileAppStepInventColorId |
| InventLocation | WHSMobileAppStepInventLocation |
| InventLocationId | WHSMobileAppStepWarehouse |
| InventSerialId | WHSMobileAppStepInventSerialId |
| InventSizeId | WHSMobileAppStepInventSizeId |
| InventStatusId | WHSMobileAppStepInventStatus |
| InventStyleId | WHSMobileAppStepInventStyleId |
| InventVersionId | WHSMobileAppStepInventVersionId |
| ItemId | WHSMobileAppStepItem |
| ITMContainerID | ITMMobileAppStepContainerId |
| ITMShipmentID | ITMMobileAppStepShipmentId |
| KanbanCardId | WHSMobileAppStepKanbanCard |
| KanbanCardToEmpty | WHSMobileAppStepKanbanCardToEmpty |
| KanbanOrCardId | WHSMobileAppStepKanbanCard |
| LicensePlateId | WHSMobileAppStepLicensePlate |
| LoadId | WHSMobileAppStepLoadId |
| LocationLicensePlatePosition | WHSMobileAppStepLocationLicensePlatePosition |
| LocOrLP | WHSMobileAppStepLocOrLP |
| LocOrLP_From | WHSMobileAppStepLocOrLPFrom |
| LocOrLP_To | WHSMobileAppStepLocOrLPTo |
| LocOrLPCheck | WHSMobileAppStepLocOrLPCheck |
| LocVerification | WHSMobileAppStepLocVerification |
| LPAdjustIn | WHSMobileAppStepLPAdjustIn |
| LPBreakChildLP | WHSMobileAppStepLPBreakChildLP |
| LPBreakParentLP | WHSMobileAppStepLPBreakParentLP |
| LPBuildChildLP | WHSMobileAppStepLPBuildChildLP |
| LPBuildParentLP | WHSMobileAppStepLPBuildParentLP |
| LPVerification | WHSMobileAppStepLPVerification |
| MergeContainerId | WHSMobileAppStepMergeContainerId |
| MixedLPLineNum | WHSMobileAppStepMixedLPLineNum |
| MobileDeviceQueueMessageCollectionIdentifierId | WHSMobileAppStepSelectOrder |
| MovementConfirmCancel | WHSMobileAppStepMovementConfirmCancel |
| NewCaptureWeight | WHSMobileAppStepCatchWeight |
| NewQty | WHSMobileAppStepNewQty |
| OutboundCatchWeightTag | WHSMobileAppStepCatchWeightTag |
| OutboundPut | WHSMobileAppStepOutboundPut |
| OutboundWeight | WHSMobileAppStepCatchWeight |
| OverridePutNewLocation | WHSMobileAppStepOverridePutNewLocation |
| PieceByPieceConfirmation | WHSMobileAppStepQtyVerification |
| POLineNum | WHSMobileAppStepPOLineNum |
| Satın Alma Siparişi Numarası | WHSMobileAppStepPONum |
| PositionFull | WHSMobileAppStepPositionFull |
| PositionFullQty | WHSMobileAppStepPositionFullQty |
| Kuvvet | WHSMobileAppStepPotency |
| PrinterName | WHSMobileAppStepPrinterName |
| ProdId | WHSMobileAppStepProdId |
| ProdLastPalletConfirmation | WHSMobileAppStepProdLastPalletConfirmation |
| ProductConfirmation | WHSMobileAppStepProductConfirmation |
| ProductionScrapConfirmation | WHSMobileAppStepProductionScrapConfirmation |
| Yerine Koy | WHSMobileAppStepPut |
| PutawayClusterId | WHSMobileAppStepPutawayClusterId |
| Miktar | WHSMobileAppStepQty |
| QtyAdjust | WHSMobileAppStepQtyAdjust |
| QtyShort | WHSMobileAppStepQtyShort |
| QtyToConsume | WHSMobileAppStepQtyToConsume |
| QtyToPick | WHSMobileAppStepQtyToPick |
| QtyToPut | WHSMobileAppStepQtyToPut |
| QtyToScrap | WHSMobileAppStepQtyToScrap |
| QtyVerification | WHSMobileAppStepQtyVerification |
| QtyWithScanningLimit | WHSMobileAppStepQtyAdjust |
| ReasonString | WHSMobileAppStepReasonString |
| RecvLocationId | WHSMobileAppStepRecvLocationId |
| RemoveContainerId | WHSMobileAppStepRemoveContainerId |
| ReprintLabelConfirmation | WHSMobileAppStepReprintLabelConfirmation |
| RMANum | WHSMobileAppStepRMANum |
| ShortPickReason | WHSMobileAppStepShortPickReason |
| SortConOrLP | WHSMobileAppStepSortConOrLP |
| SortLicensePlateId | WHSMobileAppStepSortLicensePlateId |
| SortPositionId | WHSMobileAppStepSortPositionId |
| SortVerification | WHSMobileAppStepSortVerification |
| StartLocationId | WHSMobileAppStepStartLocationId |
| StartProdOrderConfirmation | WHSMobileAppStepStartProdOrderConfirmation |
| TargetLicensePlateId | WHSMobileAppStepTargetLicensePlateId |
| TOLineNum | WHSMobileAppStepTOLineNum |
| ToLocation | WHSMobileAppStepToLocation |
| TONum | WHSMobileAppStepTONum |
| ToWarehouse | WHSMobileAppStepWarehouseTo |
| TransportLoadId | WHSMobileAppStepTransportLoadId |
| WaveLabelId | WHSMobileAppStepWaveLabelId |
| WaveLblQty | WHSMobileAppStepWaveLblQty |
| Ağırlık | WHSMobileAppStepWeight |
| WeightToConsume | WHSMobileAppStepWeightToConsume |
| WHSAdjustmentType | WHSMobileAppStepWHSAdjustmentType |
| WHSReceivingException | WHSMobileAppStepWHSReceivingException |
| WHSWorkException | WHSMobileAppStepWHSWorkException |
| WHSWorkLicensePlateId | WHSMobileAppStepWorkLicensePlateId |
| WMSLocationId | WHSMobileAppStepLocation |
| WorkId | WHSMobileAppStepWorkId |
| WorkIdToCancel | WHSMobileAppStepWorkIdToCancel |
| WorkLPIdPutawayCluster | WHSMobileAppStepWorkLPIdPutawayCluster |
| WorkPoolId | WHSMobileAppStepWorkPoolId |
| ZoneId | WHSMobileAppStepZoneId |

### <a name="available-step-icons"></a><a name="step-icons"></a>Kullanılabilir adım simgeleri

Sistem, özel adımlarınız için de kullanabileceğiniz standart adım simgeleri koleksiyonu içerir. Şu anda özel adım simgelerini yükleyemezsiniz. Bu nedenle, her zaman standart adım simgelerinden birini seçmelisiniz.

Aşağıdaki tabloda, şu anda kullanılabilen her standart adım simgesi ve adı gösterilmektedir.

<table>
<tbody>
<tr>
<td><img src="media/step-icons-about.png" alt="About step icon" title="Adım simgesi hakkında"><br>Hakkında</td>
<td><img src="media/step-icons-add-lp.png" alt="Add license plate or item step icon" title="Plaka veya öğe adımı simgesi ekleme"><br>AddLpOrItem</td>
<td><img src="media/step-icons-batch-disposition.png" alt="Batch disposition step icon" title="Toplu iş değerlendirme adım simgesi"><br>BatchDisposition</td>
<td><img src="media/step-icons-carrier.png" alt="Carrier step icon" title="Operatör adımı simgesi"><br>Taşıyıcı</td>
</tr>
<tr>
<td><img src="media/step-icons-cw-tag.png" alt="Catch weight tag step icon" title="Fiili ağırlık etiketi adım simgesi"><br>CatchWeightTag</td>
<td><img src="media/step-icons-cw-tag-weight.png" alt="Catch weight tag weight step icon" title="Fiili ağırlık etiketi ağırlık adım simgesi"><br>CatchWeightTagWeight</td>
<td><img src="media/step-icons-check-digit.png" alt="Check digit step icon" title="Basamak adımını denetle simgesi"><br>CheckDigit</td>
<td><img src="media/step-icons-check-in-out.png" alt="Check in or out ID step icon" title="Kimlik giriş veya çıkış adım simgesi"><br>CheckInOutId</td>
</tr>
<tr>
<td><img src="media/step-icons-child-lp.png" alt="Child license plate step icon" title="Alt lisans plakası adımı simgesi"><br>ChildLP</td>
<td><img src="media/step-icons-cluster-id.png" alt="Cluster ID step icon" title="Küme Kimliği adım simgesi"><br>ClusterId</td>
<td><img src="media/step-icons-cluster-position.png" alt="Cluster position step icon" title="Küme pozisyonu adım simgesi"><br>ClusterPosition</td>
<td><img src="media/step-icons-config-id.png" alt="Config ID step icon" title="Yapılandırma Kimliği adım simgesi"><br>ConfigId</td>
</tr>
<tr>
<td><img src="media/step-icons-configured-field.png" alt="Configured field step icon" title="Yapılandırılmış alan adımı simgesi"><br>ConfiguredField</td>
<td><img src="media/step-icons-con-lp.png" alt="Con or LP step icon" title="Con veya LP adım simgesi"><br>ConOrLP</td>
<td><img src="media/step-icons-consolidate-from-LP.png" alt="Consolidate from license plate ID step icon" title="Plaka kimliği adımı simgesinden konsolide"><br>ConsolidateFromLicensePlateID</td>
<td><img src="media/step-icons-consolidate-to-LP.png" alt="Consolidate to license plate ID step icon" title="Plaka kimliği adımı simgesine konsolide"><br>ConsolidateToLicensePlateID</td>
</tr>
<tr>
<td><img src="media/step-icons-container-type.png" alt="Container type step icon" title="Kapsayıcı türü adım simgesi"><br>ContainerType</td>
<td><img src="media/step-icons-counting.png" alt="Counting step icon" title="Adım sayma simgesi"><br>Sayım</td>
<td><img src="media/step-icons-counting-reason.png" alt="Counting reason code step icon" title="Neden kodu adımı simgesini sayma"><br>CountingReasonCode</td>
<td><img src="media/step-icons-country-origin.png" alt="Country of origin code step icon" title="Menşe ülke kodu adımı simgesi"><br>CountryOfOrigin</td>
</tr>
<tr>
<td><img src="media/step-icons-disposition.png" alt="Disposition step icon" title="Değerlendirme adım simgesi"><br>Değerlendirme</td>
<td><img src="media/step-icons-done.png" alt="Done step icon" title="Bitti adımı simgesi"><br>Bitti</td>
<td><img src="media/step-icons-driver-check-in-confirmation.png" alt="Driver check in confirmation step icon" title="Sürücü iade onay adımı simgesi"><br>DriverCheckInConfirmation</td>
<td><img src="media/step-icons-driver-check-in-id.png" alt="Driver check in ID step icon" title="Kimlik adımı simgesinde sürücü denetimi"><br>DriverCheckInId</td>
</tr>
<tr>
<td><img src="media/step-icons-driver-check-out-id.png" alt="Driver check out ID step icon" title="Kimlik çıkış adımı simgesinde sürücü denetimi"><br>DriverCheckOutId</td>
<td><img src="media/step-icons-exp-date.png" alt="Expiration date step icon" title="Son kullanma tarihi adımı simgesi"><br>ExpDate</td>
<td><img src="media/step-icons-field.png" alt="Field step icon" title="Alan adımı simgesi"><br>Alan</td>
<td><img src="media/step-icons-from-batch.png" alt="From batch disposition step icon" title="Toplu iş değerlendirmeden adım simgesi"><br>FromBatchDisposition</td>
</tr>
<tr>
<td><img src="media/step-icons-from-inventory-status.png" alt="From inventory status step icon" title="Stok durumundan adımı simgesinden"><br>FromInventoryStatus</td>
<td><img src="media/step-icons-id-attribute.png" alt="ID attribute step icon" title="Kimlik özniteliği adım simgesi"><br>IdAttribute</td>
<td><img src="media/step-icons-invent-batch-id.png" alt="Inventory batch ID step icon" title="Stok toplu iş kimliği adım simgesi"><br>InventBatchID</td>
<td><img src="media/step-icons-invent-color-id.png" alt="Inventory color ID step icon" title="Stok renkli kimliği adım simgesi"><br>InventColorID</td>
</tr>
<tr>
<td><img src="media/step-icons-invent-location.png" alt="Inventory location step icon" title="Stok konumu adım simgesi"><br>InventLocation</td>
<td><img src="media/step-icons-invent-serial-id.png" alt="Inventory serial ID step icon" title="Stok seri kimliği adım simgesi"><br>InventSerialID</td>
<td><img src="media/step-icons-invent-size-id.png" alt="Inventory size ID step icon" title="Stok boyut kimliği adım simgesi"><br>InventSizeID</td>
<td><img src="media/step-icons-invent-status-id.png" alt="Inventory status ID step icon" title="Stok durumu kimliği adım simgesi"><br>InventStatusID</td>
</tr>
<tr>
<td><img src="media/step-icons-invent-style-id.png" alt="Inventory style ID step icon" title="Stok stili kimliği adım simgesi"><br>InventStyleID</td>
<td><img src="media/step-icons-invent-version-id.png" alt="Inventory version ID step icon" title="Stok sürümü kimliği adım simgesi"><br>InventVersionID</td>
<td><img src="media/step-icons-item-id.png" alt="Item ID step icon" title="Madde Kimliği adım simgesi"><br>ItemID</td>
<td><img src="media/step-icons-itm-contianer-id.png" alt="ITM container ID step icon" title="ITM Kapsayıcı kimlik adım simgesi"><br>ITMContainerID</td>
</tr>
<tr>
<td><img src="media/step-icons-itm-shipment-id.png" alt="ITM shipment ID step icon" title="ITM sevkiyat kimliği adımı simgesi"><br>ITMShipmentID</td>
<td><img src="media/step-icons-kanban-card-id.png" alt="Kanban card ID step icon" title="Kanban kart kimliği adım simgesi"><br>KanbanCardID</td>
<td><img src="media/step-icons-kanban-or-card-id.png" alt="Kanban or card ID step icon" title="Kanban veya kart kimliği adım simgesi"><br>KanbanOrCardID</td>
<td><img src="media/step-icons-license-plate-id.png" alt="License plate ID step icon" title="Lisans plakası kimlik adım simgesi"><br>LicensePlateID</td>
</tr>
<tr>
<td><img src="media/step-icons-load-id.png" alt="Load ID step icon" title="Yük Kimliği adım simgesi"><br>LoadId</td>
<td><img src="media/step-icons-location-lp-pos.png" alt="Location license plate position step icon" title="Yerleşim plaka konum adım simgesi"><br>LocationLicensePlatePosition</td>
<td><img src="media/step-icons-location-or-lp.png" alt="Location or license plate step icon" title="Konum veya lisans plakası adımı simgesi"><br>LocOrLP</td>
<td><img src="media/step-icons-location-or-lp-check.png" alt="Location or license plate check step icon" title="Konum veya lisans plakası denetim adımı simgesi"><br>LocOrLPCheck</td>
</tr>
<tr>
<td><img src="media/step-icons-location-or-lp-from.png" alt="Location or license plate from step icon" title="Konum veya lisans plakasından adımı simgesi"><br>LocOrLPFrom</td>
<td><img src="media/step-icons-location-or-lp-to.png" alt="Location or license plate to step icon" title="Konum veya lisans plakasına adımı simgesi"><br>LocOrLPTo</td>
<td><img src="media/step-icons-long-process-complete.png" alt="Long process completed step icon" title="Uzun işlem tamamlandı adım simgesi"><br>LongProcessCompleted</td>
<td><img src="media/step-icons-lp-break-parent.png" alt="LP break parent LP step icon" title="LP kesme üst LP adım simgesi"><br>LPBreakParentLP</td>
</tr>
<tr>
<td><img src="media/step-icons-merge-container.png" alt="Merge container ID step icon" title="Birleştirme Kapsayıcı kimlik adım simgesi"><br>MergeContainerId</td>
<td><img src="media/step-icons-mixed-lp-line.png" alt="Mixed license plate line number step icon" title="Karışık lisans plakası satır numarası adım simgesi"><br>MixedLPLineNum</td>
<td><img src="media/step-icons-outbound-weight.png" alt="Outbound weight step icon" title="Giden ağırlık adımı simgesi"><br>OutboundWeight</td>
<td><img src="media/step-icons-owner.png" alt="Owner step icon" title="Sahip adımı simgesi"><br>Sahip</td>
</tr>
<tr>
<td><img src="media/step-icons-parent-lp.png" alt="Parent license plate step icon" title="Üst lisans plakası adımı simgesi"><br>ParentLP</td>
<td><img src="media/step-icons-please-confirm.png" alt="Please confirm step icon" title="Lütfen onaylayın adım simgesi"><br>PleaseConfirm</td>
<td><img src="media/step-icons-po-line-num.png" alt="Purchase order line number step icon" title="Satın alma sipariş satır numarası adım simgesi"><br>POLineNum</td>
<td><img src="media/step-icons-po-num.png" alt="Purchase order number step icon" title="Satın alma sipariş numarası adım simgesi"><br>Satın Alma Siparişi Numarası</td>
</tr>
<tr>
<td><img src="media/step-icons-position-full.png" alt="Position full step icon" title="Pozisyon tam adım simgesi"><br>PositionFull</td>
<td><img src="media/step-icons-potency.png" alt="Potency step icon" title="Kuvvet adım simgesi"><br>Kuvvet</td>
<td><img src="media/step-icons-printer-name.png" alt="Printer name step icon" title="Yazıcı adı adım simgesi"><br>PrinterName</td>
<td><img src="media/step-icons-prod-id.png" alt="Prod ID step icon" title="Ürün Kimliği adım simgesi"><br>ProdId</td>
</tr>
<tr>
<td><img src="media/step-icons-product-confirm.png" alt="Product confirmation step icon" title="Ürün onay adımı simgesi"><br>ProductConfirmation</td>
<td><img src="media/step-icons-put.png" alt="Put step icon" title="Yerine koy adım simgesi"><br>Yerine Koy</td>
<td><img src="media/step-icons-putaway-cluster-id.png" alt="Putaway cluster ID step icon" title="Yerine koyma küme Kimliği adım simgesi"><br>PutawayClusterId</td>
<td><img src="media/step-icons-qty.png" alt="Quantity step icon" title="Miktar adımı simgesi"><br>Miktar</td>
</tr>
<tr>
<td><img src="media/step-icons-qty-adjust-in.png" alt="Quantity adjust in step icon" title="Miktar ayarlama adım simgesi"><br>QtyAdjustIn</td>
<td><img src="media/step-icons-qty-short.png" alt="Quantity short step icon" title="Miktar kısa adımı simgesi"><br>QtyShort</td>
<td><img src="media/step-icons-qty-to-consume.png" alt="Quantity to consume step icon" title="Tüketilecek miktar adım simgesi"><br>QtyToConsume</td>
<td><img src="media/step-icons-qty-to-put.png" alt="Quantity to put step icon" title="Koyulacak miktar adım simgesi"><br>QtyToPut</td>
</tr>
<tr>
<td><img src="media/step-icons-qty-to-scrap.png" alt="Quantity to scrap step icon" title="Iskarta miktarı adım simgesi"><br>QtyToScrap</td>
<td><img src="media/step-icons-qty-confirmation.png" alt="Quantity confirmation step icon" title="Miktar onay adımı simgesi"><br>QuantityConfirmation</td>
<td><img src="media/step-icons-raf-end-job.png" alt="Report as finished end job step icon" title="Tamamlandı bildirimi bitiş işi adımı simgesi"><br>RAFEndJob</td>
<td><img src="media/step-icons-recv-loc-id.png" alt="Receive location ID step icon" title="Konum kimliği adımı simgesini al"><br>RecvLocationID</td>
</tr>
<tr>
<td><img src="media/step-icons-remove-container-id.png" alt="Remove container ID step icon" title="Kaldırma Kapsayıcı kimlik adım simgesi"><br>RemoveContainerID</td>
<td><img src="media/step-icons-rma-no.png" alt="RMA number step icon" title="RMA numarası adımı simgesi"><br>RMANum</td>
<td><img src="media/step-icons-select-order.png" alt="Select order step icon" title="Sipariş seç adımı simgesi"><br>SelectOrder</td>
<td><img src="media/step-icons-short-pick-reason.png" alt="Short pick reason step icon" title="Kısa çekme nedeni adım simgesi"><br>ShortPickReason</td>
</tr>
<tr>
<td><img src="media/step-icons-sort-position-id.png" alt="Sort position ID step icon" title="Konum kimliğini sınıflandır adım simgesi"><br>SortPositionId</td>
<td><img src="media/step-icons-target-lp-id.png" alt="Target license plate ID step icon" title="Hedef Lisans plakası kimlik adım simgesi"><br>TargetLicensePlateId</td>
<td><img src="media/step-icons-to-line-no.png" alt="To line number step icon" title="Satır numarası adım simgesine"><br>ToLineNum</td>
<td><img src="media/step-icons-to-location.png" alt="To location step icon" title="Konuma adım simgesi"><br>ToLocation</td>
</tr>
<tr>
<td><img src="media/step-icons-to-number.png" alt="To number step icon" title="Numaraya adımı simgesi"><br>ToNum</td>
<td><img src="media/step-icons-to-warehouse.png" alt="To warehouse step icon" title="Ambara adım simgesi"><br>ToWarehouse</td>
<td><img src="media/step-icons-tranport-load-id.png" alt="Transport load ID step icon" title="Taşıma yükü Kimliği adım simgesi"><br>TransportLoadId</td>
<td><img src="media/step-icons-vendor-batch-id.png" alt="Vendor batch ID step icon" title="Satıcı toplu iş kimliği adım simgesi"><br>VendBatchId</td>
</tr>
<tr>
<td><img src="media/step-icons-wave-label-id.png" alt="Wave label ID step icon" title="Dalga etiketi kimliği adım simgesi"><br>WaveLabelId</td>
<td><img src="media/step-icons-wave-label-qty.png" alt="Wave label quantity step icon" title="Dalga etiketi miktarı adım simgesi"><br>WaveLblQty</td>
<td><img src="media/step-icons-weight.png" alt="Weight step icon" title="Ağırlık adımı simgesi"><br>Ağırlık</td>
<td><img src="media/step-icons-weight-to-consume.png" alt="Weight to consume step icon" title="Tüketilecek ağırlık adım simgesi"><br>WeightToConsume</td>
</tr>
<tr>
<td><img src="media/step-icons-whs-adjustment-type.png" alt="WHS adjustment type step icon" title="WHS ayar türü adım simgesi"><br>WHSAdjustmentType</td>
<td><img src="media/step-icons-whs-receiving-exception.png" alt="WHS receiving exception step icon" title="WHS özel durum alma adım simgesi"><br>WHSReceivingException</td>
<td><img src="media/step-icons-wms-location-id.png" alt="WMS location ID step icon" title="WMS konum kimliği adım simgesi"><br>WMSLocationID</td>
<td><img src="media/step-icons-work-id.png" alt="Work ID step icon" title="İş Kimliği adım simgesi"><br>WorkId</td>
</tr>
<tr>
<td><img src="media/step-icons-work-id-to-cancel.png" alt="Work ID to cancel step icon" title="İptal edilecek iş kimliği Adım simgesi"><br>WorkIdToCancel</td>
<td><img src="media/step-icons-work-lp-id.png" alt="Work license plate ID step icon" title="İş Lisans plakası kimlik adım simgesi"><br>WorkLicensePlateId</td>
<td><img src="media/step-icons-work-lp-putaway-cluster.png" alt="Work license plate ID putaway cluster step icon" title="İş Lisans plakası kimlik koyma kümesi adım simgesi"><br>WorkLPIDPutawayCluster</td>
<td><img src="media/step-icons-work-pool-id.png" alt="Work pool ID step icon" title="İş havuzu Kimliği adım simgesi"><br>WorkPoolID</td>
</tr>
<tr>
<td><img src="media/step-icons-zone-pool-id.png" alt="Zone ID step icon" title="Bölge Kimliği adım simgesi"><br>ZoneID</td>
<td></td>
<td></td>
<td></td>
</tr>
</tbody>
</table>

## <a name="example-assign-step-icons-and-titles-for-a-custom-flow"></a><a name="example"></a>Örnek: Özel akış bölümü için adım simgeleri ve başlıklar atama

Bu örnek, özel bir görev akışı için adım simgelerinin ve başlıklarının nasıl ayarlanıp ayarlananın açıklanmaktadır. Senaryo, aşağıdaki blog gönderisinde daha ayrıntılı olarak sunulan ve araştırılan özel bir görev akışı örneği üzerine kuruludur: [Depolama Mobil Uygulamasını Özelleştirme](https://cloudblogs.microsoft.com/dynamics365/it/2017/07/06/customizing-the-warehousing-mobile-app). Görev akışı aşağıdaki şekilde çalışır:

1. Uygulama, çalışandan bir kapsayıcı kimliği sağlamasını isteyen bir sayfa gösterir (örneğin, bir barkodu tarayarak).
1. Kapsayıcı kimliği geçerliyse, uygulama çalışandan ağırlığı isteyen yeni bir sayfa açar. (Kapsayıcı kimliği geçerli değilse, çalışan ilk sayfaya döndürülür.)
1. Çalışan geçerli bir ağırlık girdiğinde, sistem ağırlığı depolar ve çalışanı ilk sayfaya döndürür.

Aşağıdaki şekilde bu görev akışı gösterilmiştir.

![Görev akışı diyagramı.](media/step-icons-example-task-flow.png "Görev akışı diyagramı")

### <a name="create-a-step-class-for-the-container-input-page"></a>Kapsayıcı giriş sayfası için adım sınıfı oluşturma

Kapsayıcı giriş sayfası, çalışanın bir kapsayıcı kimliği taramasına veya girmesine izin verir.

![Kapsayıcı giriş sayfası.](media/step-icons-example-container-input.png "Kapsayıcı giriş sayfası")

Kapsayıcı giriş sayfasında, giriş alanının denetim adı `ContainerId`. Bu denetim adı [adım kimlikleri listesinde](#step-ids-classes) olmadığından, temel alan varolan bir adımı bulamazsınız. Bu nedenle, adımı temsil eden bir adım sınıfı oluşturmanız gerekir. Aşağıda bir örnek verilmiştir.

```xpp
[WHSMobileAppStepId('ContainerId')]
final internal class WHSMobileAppStepContainerId extends WHSMobileAppStep
{
    private const WHSMobileAppStepIcon PopulationIcon = 'InventBatchID';
    private const WHSMobileAppStepTitle InputNotFilledTitle = "@WAX:WHSMobileAppStepContainerID_InputNotFilled"; //Scan a container
    protected void initValues()
    {
        defaultStepIcon = PopulationIcon;
        defaultStepTitle = InputNotFilledTitle;
    }
}
```

Adım simgesinin tanımlayıcısı `defaultStepIcon` sınıf üyesinde, adım başlığı ise `defaultStepTitle` sınıf üyesinde depolanır.

Adım simgesi atamak için, bu konunun önceki bölümlerindeki [Kullanılabilir adım simgeleri](#step-icons) bölümünde listelenen simge kimliklerinden birine `defaultStepIcon` ayarlayın.

### <a name="use-a-standard-or-custom-step-icon-and-title-for-the-weight-input"></a>Ağırlık girişi için standart veya özel adım simgesi ve başlığı kullanma

Ağırlık giriş sayfası, çalışanın bir ağırlık girmesini sağlar.

![Ağırlık giriş sayfası.](media/step-icons-example-weight-input.png "Ağırlık giriş sayfası")

Ağırlık giriş sayfasında, giriş alanının denetim adı `Weight`, bu da [adım kimlikleri listesindedir](#step-ids-classes). Bu nedenle, `WHSMobileAppStepWeight` sınıfta tanımlanan adım simgesi ve başlığı sizin için kabul edilebilirse, bu adım için hiçbir şeyi değiştirmeniz gerekmemektedir.

Ancak, bu adım için farklı bir simge veya başlık kullanmayı tercih ederseniz, `stepId()` yöntemi veya `stepInfo()` yöntemi oluşturucu sınıfında geçersiz kılabilirsiniz. Her görev akışının kendi adım bilgisi oluşturucusu vardır.

#### <a name="override-the-stepid-method"></a>stepId() yöntemini geçersiz kılma

Aşağıdaki örnek, `stepId()` yöntemi geçersiz kılarak bir oluşturucu sınıfını değiştirmenin bir yolunu gösterir.

```xpp
[WHSWorkExecuteMode(WHSWorkExecuteMode:: WeighContainer)]
public class WHSMobileAppStepInfoBuilderWeighContainer extends WHSMobileAppStepInfoBuilder
{
    protected WHSMobileAppStepId stepId()
    {
        WHSMobileAppStepId stepIdLocal = super();
        if (stepIdLocal == 'Weight')
        {
            return 'NewWeight';
        }
        return stepIdLocal;
    }
}
```

Daha sonra `NewWeight` adım için bir adım sınıfı oluşturursunuz. Kod, bu konuda daha önce gösterilen `ContainerId` örneğin koduna benzemelidir.

#### <a name="override-the-stepinfo-method"></a>stepInfo() yöntemini geçersiz kılma

Aşağıdaki örnek, `stepInfo()` yöntemi geçersiz kılarak bir oluşturucu sınıfını değiştirmenin bir yolunu gösterir.

```xpp
[WHSWorkExecuteMode(WHSWorkExecuteMode:: WeighContainer)]
public class WHSMobileAppStepInfoBuilderWeighContainer extends WHSMobileAppStepInfoBuilder
{
    protected WHSMobileAppStepInfo stepInfo()
    {
        if (stepId != 'Weight')
        {
            return super();
        }
        WHSMobileAppStepInfo stepInfo = WHSMobileAppStepInfo::construct();
        stepInfo.parmStepIcon('NewIcon');
        stepInfo.parmStepTitle('NewTitle');
        return stepInfo;
    }
}
```

Daha sonra bir `WHSMobileAppStepInfo` nesnesi oluşturursunuz ve simgeyi ve/veya başlığı doğrudan ayarlarsınız.

## <a name="additional-resources"></a>Ek kaynaklar

- [Ambar Yönetimi mobil uygulamasını yükleme ve bağlama](install-configure-warehouse-management-app.md)
- [Mobil cihaz kullanıcı ayarları](mobile-device-user-settings.md)
