---
title: Miktar, eksik teslimat yüzdesini aştığından sevkiyatı onaylayamazsınız
description: Miktar, eksik teslimat yüzdesini aştığından sevkiyatı onaylayamazsınız
author: perlynne
ms.date: 04/21/2021
ms.topic: troubleshooting
ms.search.form: WHSLoadTable_WHSShipConfirm,WHSLoadPlanningListPage_WHSShipConfirm,WHSLoadPlanningWorkbench_WHSShipConfirm,WHSTransportLoad_WHSShipConfirm,WHSShipPlanningListPage_WHSShipConfirm,WHSShipmentDetails_WHSShipConfirm,WHSWorkTable_WHSShipConfirm,WHSWorkTableListPage_WHSShipConfirm,Dialog_WHSOutboundShipConfirmController_WHSOutboundShipConfirm,WHSContainerCloseDiag_WHSShipConfirm
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: lbc
ms.search.validFrom: 2021-04-21
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 625003731485329b93f5f9454ccece580c889613
ms.sourcegitcommit: c2c6d687a89bc1534c029109315c23e92865b63b
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/31/2021
ms.locfileid: "6123831"
---
# <a name="you-cant-confirm-a-shipment-because-the-quantity-exceeds-the-underdelivery-percentage"></a>Miktar, eksik teslimat yüzdesini aştığından sevkiyatı onaylayamazsınız

Hata kodu: WAX1686

## <a name="symptoms"></a>Belirtiler

Bir sevkiyatı onaylamaya çalıştığınızda, sistem aşağıdaki hata iletisini gösterir:

> %2 maddesinin miktarı eksik teslimat için tanımlanan yüzdeyi aştığından %1 yükü için sevkiyat onaylanamadı.

Bu nedenle, yükleme için sevkiyat işlemini onaylayamazsınız.

## <a name="cause"></a>Nedeni

Yük veya sevkiyat miktarı yalnızca kısmen çekildi. Mevcut miktar, izin verilen eksik teslimat yüzdesi dışında kalan bir yüzdeyle çekilen miktarın altında.

## <a name="resolution"></a>Çözünürlük

Bu sorunu gidermek için aşağıdaki görevlerden birini tamamlayın:

- Yük satırı miktarını ayarlayın.
- Eksik teslimat yüzdesini ayarlayın.

### <a name="set-the-load-line-quantity"></a>Yük satırı miktarını ayarlayın

Yük satırı miktarını ayarlamak için aşağıdaki adımları izleyin.

1. **Ambar yönetimi \> Yükler \> Tüm yükler**'e gidin.
1. Sevkiyatın onaylanamadığı ilgili yükü seçin.
1. **Yük satırları** hızlı sekmesinde, eksik teslimat yüzdesini aşan maddenin yük satırını seçin.
1. **Satır ayrıntıları** hızlı sekmesinde, **Sipariş**'i seçin.
1. **Miktar** alanında, sevkiyat onayının gerçekleşmesi için değeri çekilen miktara (yani **Oluşturulan çalışma miktarı** değerine) ayarlayın.

### <a name="set-the-underdelivery-percentage"></a>Eksik teslimat yüzdesini ayarlayın

eksik teslimat yüzdesini ayarlamak için aşağıdaki adımları izleyin.

1. **Ambar yönetimi \> Yükler \> Tüm yükler**'e gidin.
1. Sevkiyatın onaylanamadığı ilgili yükü seçin.
1. **Yük satırları** hızlı sekmesinde, eksik teslimat yüzdesini aşan maddenin yük satırını seçin.
1. **Satır ayrıntıları** hızlı sekmesinde, **Genel**'i seçin.
1. **eksik teslimat** alanında, sevkiyat onayının gerçekleşmesi için, değeri yük miktarına göre çekilen miktardan daha büyük bir yüzdeye ayarlayın.
