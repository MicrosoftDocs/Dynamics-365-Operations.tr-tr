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
ms.openlocfilehash: f1fccd10d8867252f32b37c77f9a3bad54157bdd
ms.sourcegitcommit: cd9016e9787169cb800889d335b9c5919ddbe4af
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2021
ms.locfileid: "5938569"
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
