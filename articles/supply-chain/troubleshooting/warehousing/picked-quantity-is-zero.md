---
title: Miktar sıfır olduğundan sevkiyatı onaylayamazsınız
description: Miktar sıfır olduğundan sevkiyatı onaylayamazsınız
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
ms.openlocfilehash: b2f9f8deaca30e318d0393fb1d7911eebf63060ccca83dc6f1de9b04b9e30e11
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/05/2021
ms.locfileid: "6712898"
---
# <a name="you-cant-confirm-a-shipment-because-there-is-zero-quantity"></a>Miktar sıfır olduğundan sevkiyatı onaylayamazsınız

Hata kodu: LoadLineWarningUpdatedToZero

## <a name="symptoms"></a>Belirtiler

Bir sevkiyatı onaylamaya çalıştığınızda, sistem aşağıdaki hata iletisini gösterir:

> Bu madde için hiçbir miktarın sevk edilmesine izin vermeyen eksik teslimat ayarlarından dolayı, %1 maddesi ve %2 sevkiyatı için yük satırı sıfır miktara sahip olacak şekilde güncelleştirildi.

Bu nedenle, yükleme için sevkiyat işlemini onaylayamazsınız.

## <a name="cause"></a>Nedeni

Sistem, teslim alınan miktarın; teslim alınan miktar, yükleme satırı miktarı ve eksik teslimat yüzdesine göre beklenen sınırlar içinde olup olmadığını değerlendirir. Sistem, yükleme satırındaki teslim alınan miktarın 0 (sıfır) olduğunu belirlerse, sevkiyatı onaylayamazsınız. Örneğin, iş iptal edilirse ve yükleme satırındaki eksik teslimat yüzdesi yüzde 100 ise bu sorun oluşabilir.

## <a name="resolution"></a>Çözünürlük

Eksik teslimat yüzdesinin ve miktarların, teslim alınan işle uyumlu olduğundan emin olmak için yükleme satırlarını denetleyin.

1. **Ambar yönetimi \> Yükler \> Tüm yükler**'e gidin.
1. Sevkiyatın onaylanamadığı ilgili yükü seçin.
1. **Yük satırları** hızlı sekmesinde, eksik teslimat yüzdesini aşan maddenin yük satırını seçin.
1. **Eksik teslimat** alanının veya **Miktar** alanının değerini gerektiği gibi ayarlayın.

> [!TIP]
> Sorun hala düzelmezse mevcut miktar, yükleme veya sevkiyat ile uyumlu hale gelene kadar ilgili satış siparişleri veya transfer emirleri için daha fazla teslim alma işi tamamlamanız gerekebilir.
