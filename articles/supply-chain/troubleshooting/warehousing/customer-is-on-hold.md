---
title: Müşteri beklemede olduğundan sevkiyat onaylanamıyor
description: Müşteri beklemede olduğundan sevkiyat onaylanamıyor.
author: GalynaFedorova
ms.date: 07/30/2021
ms.topic: troubleshooting
ms.search.form: WHSLoadTable_WHSShipConfirm,WHSLoadPlanningListPage_WHSShipConfirm,WHSLoadPlanningWorkbench_WHSShipConfirm,WHSTransportLoad_WHSShipConfirm,WHSShipPlanningListPage_WHSShipConfirm,WHSShipmentDetails_WHSShipConfirm,WHSWorkTable_WHSShipConfirm,WHSWorkTableListPage_WHSShipConfirm,Dialog_WHSOutboundShipConfirmController_WHSOutboundShipConfirm
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: v-gfedorova
ms.search.validFrom: 2021-07-30
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: 82b28e7cfd8c88e453cdd09398f5a92f605eab15a17d33defa0b9729a53c05b6
ms.sourcegitcommit: fa5ff2a0822aac16b518a2aea0d3389f79793390
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/07/2021
ms.locfileid: "7012221"
---
# <a name="you-cant-confirm-a-shipment-because-the-customer-is-on-hold"></a>Müşteri beklemede olduğundan sevkiyat onaylanamıyor

Hata kodu: WAX:CustomerOnHoldShipmentCannotBeConfirmed

## <a name="symptoms"></a>Belirtiler

Bir sevkiyatı onaylamaya çalıştığınızda, sistem aşağıdaki hata iletisini gösterir:

> Müşteri %2 için beklemede olduğundan %1 sevkiyatı onaylanamıyor.

Bu nedenle, yükleme için sevkiyat işlemini onaylayamazsınız.

## <a name="cause"></a>Nedeni

Yük veya sevkiyatın müşteri hesabı beklemede. Bu nedenle, müşterinin durumu sevkiyat onayını engellemektedir.

## <a name="resolution"></a>Çözüm

Müşteri hesabının engelini kaldırmak için aşağıdaki yordamı kullanın.

1. **Alacak hesapları \> Müşteriler \> Tüm müşteriler**'e gidin.
1. Sevkiyatın onaylanamadığı müşteri hesabını açın.
1. **Alacak ve tahsilatlar** hızlı sekmesinde, **Faturalama ve beklemedeki teslimat** alanını *Hayır* olarak ayarlayın.
1. Yükün tüm engellenen müşterileri için bu yordamı tekrarlayın.
