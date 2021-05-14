---
title: Miktar, fazla teslimat yüzdesini aştığından sevkiyatı onaylayamazsınız
description: Miktar, fazla teslimat yüzdesini aştığından sevkiyatı onaylayamazsınız
author: perlynne
ms.date: 04/21/2021
ms.topic: troubleshooting
ms.search.form: WHSLoadTable_WHSShipConfirm,WHSLoadPlanningListPage_WHSShipConfirm,WHSLoadPlanningWorkbench_WHSShipConfirm,WHSTransportLoad_WHSShipConfirm,WHSShipPlanningListPage_WHSShipConfirm,WHSShipmentDetails_WHSShipConfirm,WHSWorkTable_WHSShipConfirm,WHSWorkTableListPage_WHSShipConfirm,Dialog_WHSOutboundShipConfirmController_WHSOutboundShipConfirm
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: lbc
ms.search.validFrom: 2021-04-21
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: c9b5ba8dedb927ee049d7e53e9a666902f563f49
ms.sourcegitcommit: cd9016e9787169cb800889d335b9c5919ddbe4af
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2021
ms.locfileid: "5938570"
---
# <a name="you-cant-confirm-a-shipment-because-the-quantity-exceeds-the-overdelivery-percentage"></a>Miktar, fazla teslimat yüzdesini aştığından sevkiyatı onaylayamazsınız

Hata kodu: WAX1687

## <a name="symptoms"></a>Belirtiler

Bir sevkiyatı onaylamaya çalıştığınızda, sistem aşağıdaki hata iletisini gösterir:

> %2 maddesinin miktarı fazla teslimat için tanımlanan yüzdeyi aştığından %1 yükü için sevkiyat onaylanamadı.

Bu nedenle, yükleme için sevkiyat işlemini onaylayamazsınız.

## <a name="cause"></a>Nedeni

Yük veya sevkiyat miktarı yalnızca kısmen çekildi. Mevcut miktar, izin verilen fazla teslimat yüzdesi dışında kalan bir yüzdeyle çekilen miktarı aşıyor.

## <a name="resolution"></a>Çözünürlük

Bu sorunu gidermek için aşağıdaki görevlerden birini tamamlayın:

- Yük satırı miktarını ayarlayın.
- Fazla teslimat yüzdesini ayarlayın.

### <a name="set-the-load-line-quantity"></a>Yük satırı miktarını ayarlayın

Yük satırı miktarını ayarlamak için aşağıdaki adımları izleyin.

1. **Ambar yönetimi \> Yükler \> Tüm yükler**'e gidin.
1. Sevkiyatın onaylanamadığı ilgili yükü seçin.
1. **Yük satırları** hızlı sekmesinde, fazla teslimat yüzdesini aşan maddenin yük satırını seçin.
1. **Satır ayrıntıları** hızlı sekmesinde, **Sipariş**'i seçin.
1. **Miktar** alanında, sevkiyat onayının gerçekleşmesi için değeri çekilen miktara (yani **Oluşturulan çalışma miktarı** değerine) ayarlayın.

### <a name="set-the-overdelivery-percentage"></a>Fazla teslimat yüzdesini ayarlayın

eksik teslimat yüzdesini ayarlamak için aşağıdaki adımları izleyin.

1. **Ambar yönetimi \> Yükler \> Tüm yükler**'e gidin.
1. Sevkiyatın onaylanamadığı ilgili yükü seçin.
1. **Yük satırları** hızlı sekmesinde, fazla teslimat yüzdesini aşan maddenin yük satırını seçin.
1. **Satır ayrıntıları** hızlı sekmesinde, **Genel**'i seçin.
1. **Fazla teslimat** alanında, sevkiyat onayının gerçekleşmesi için, değeri yük miktarına göre çekilen miktardan daha büyük bir yüzdeye ayarlayın.
