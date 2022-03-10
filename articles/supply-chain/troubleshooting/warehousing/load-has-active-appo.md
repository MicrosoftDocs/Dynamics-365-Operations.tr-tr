---
title: Takvimdeki bir sorun nedeniyle sevkiyatı onaylayamıyorsunuz
description: Takvimdeki bir sorun nedeniyle sevkiyatı onaylayamıyorsunuz
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
ms.openlocfilehash: 8aae45beeef1934760d620874897f46a1cf901995e2b83e148a1d56898d9c717
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/05/2021
ms.locfileid: "6735956"
---
# <a name="you-cant-confirm-a-shipment-because-of-an-issue-with-the-calendar"></a>Takvimdeki bir sorun nedeniyle sevkiyatı onaylayamıyorsunuz

Hata kodu: TRX2716

## <a name="symptoms"></a>Belirtiler

Bir sevkiyatı onaylamaya çalıştığınızda, sistem aşağıdaki hata iletisini gösterir:

> Takvim türü %1 randevu %2 için giriş ve çıkış yapılmasını gerektiriyor.

Bu nedenle, yükleme için sevkiyat işlemini onaylayamazsınız.

## <a name="cause"></a>Nedeni

Yükleme için etkin randevular mevcut. Örneğin, sürücü girişi gerektiren bir kural vardır. Bu nedenle, yükleme işlemi şu anda sevkiyat onayının başarısız olduğu bir durumdadır.

## <a name="resolution"></a>Çözünürlük

Yükleme ile bağlantılı etkin randevularla ilgili tüm sorunları araştırmanız ve düzeltmeniz gerekir.

1. **Ambar yönetimi \> Yükler \> Tüm yükler**'e gidin.
1. Sevkiyatın onaylanamadığı ilgili yükü seçin.
1. Eylem Bölmesinde **Taşıma** sekmesinde **Randevular** grubunda **Randevu zamanlama** öğesini seçin.
1. Şu adımlardan birini izleyin:

    - Randevu için sürücünün giriş/çıkış işlemlerinin tamamlandığından emin olun.
    - Randevuyu tamamlayın veya iptal edin.
    - İlgili randevu kuralı için **Sürücü girişi gerekli** seçeneğini devre dışı bırakın.
