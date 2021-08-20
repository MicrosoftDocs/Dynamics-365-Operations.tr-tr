---
title: Tamamlanmamış veya eksik çalışmalar nedeniyle sevkiyatı onaylayamıyorsunuz
description: Tamamlanmamış veya eksik çalışmalar nedeniyle sevkiyatı onaylayamıyorsunuz
author: perlynne
ms.date: 04/21/2021
ms.topic: troubleshooting
ms.search.form: WHSLoadTable_WHSShipConfirm,WHSLoadPlanningListPage_WHSShipConfirm,WHSLoadPlanningWorkbench_WHSShipConfirm,WHSTransportLoad_WHSShipConfirm,WHSShipPlanningListPage_WHSShipConfirm,WHSShipmentDetails_WHSShipConfirm,WHSWorkTable_WHSShipConfirm,WHSWorkTableListPage_WHSShipConfirm,Dialog_WHSOutboundShipConfirmController_WHSOutboundShipConfirm, WHSContainerCloseDiag_WHSShipConfirm
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: lbc
ms.search.validFrom: 2021-04-21
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 59def4427f9fff32fd3839bb9f9b5d5cccdc7720f92a84f1af3adad596d8b352
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/05/2021
ms.locfileid: "6730070"
---
# <a name="you-cant-confirm-a-shipment-because-of-incomplete-or-missing-work"></a>Tamamlanmamış veya eksik çalışmalar nedeniyle sevkiyatı onaylayamıyorsunuz

Hata kodu: WAX515

## <a name="symptoms"></a>Belirtiler

Bir sevkiyatı onaylamaya çalıştığınızda, sistem aşağıdaki hata iletisini gösterir:

> %1 yükü için sevkiyat onaylanamıyor çünkü yük için tüm işler tamamlanmış olmalıdır.

Bu nedenle, yükleme için sevkiyat işlemini onaylayamazsınız.

## <a name="cause"></a>Nedeni

Yükleme veya sevkiyat işlemi şu anda sevkiyat onayının başarısız olduğu bir durumdadır. Sevkiyatı onaylamadan önce, yükleme için en az bir miktar çalışmanın mevcut olması ve bu çalışmanın *Kapalı* veya *İptal edilmiş* durumunda olması gerekir.

## <a name="resolution"></a>Çözünürlük

Yükleme veya sevkiyat ile ilgili satış siparişlerini veya transfer emirlerini kontrol edin ve ilgili tüm çalışmanın tamamlandığından veya iptal edildiğinden emin olun.

Birkaç sayfada birden sevkiyatlar ve yüklemelerde çalışabilirsiniz. Aşağıdaki alt bölümler birkaç örnek sağlar.

### <a name="all-loads-page"></a>Tüm yüklemeler sayfası

1. **Ambar yönetimi \> Yükler \> Tüm yükler**'e gidin.
1. Sevkiyatın onaylanamadığı ilgili yükü seçin.
1. Eylem Bölmesinde **Yüklemeler** sekmesindeki **İlgili bilgiler** grubunda **Çalışma**'yı seçin.
1. Her çalışma kodunun durumunu denetleyin. *Kapalı* veya *İptal edildi* durumundaki çalışma kodlarını takip edin.
1. Her çalışma kodu *Kapalı* veya *İptal edildi* durumunda olduğunda, sevkiyatı onaylamak için yeniden deneyin.

### <a name="all-shipments-page"></a>Tüm sevkiyatlar sayfası

1. **Ambar yönetimi \> Sevkiyatlar \> Tüm sevkiyatlar**'a gidin.
1. Onaylanamayan sevkiyatı seçin.
1. Eylem Bölmesinde **Sevkiyatlar** sekmesindeki **Çalışma** grubunda **İş ayrıntıları**'nı seçin.
1. Her çalışma kodunun durumunu denetleyin. *Kapalı* veya *İptal edildi* durumundaki çalışma kodlarını takip edin.
1. Her çalışma kodu *Kapalı* veya *İptal edildi* durumunda olduğunda, sevkiyatı onaylamak için yeniden deneyin.

### <a name="all-work-page"></a>Tüm çalışmalar sayfası

1. **Ambar yönetimi \> İş \> Tüm çalışmalar**'a gidin.
1. Sevkiyatın onaylanamadığı sipariş numarası ile ilgili çalışmayı seçin.
1. Eylem Bölmesinde **Sevkiyat** sekmesindeki **Sevkiyat** grubunda **Sevkiyatı onayla**'yı seçin.
1. Her çalışma kodunun durumunu denetleyin. *Kapalı* veya *İptal edildi* durumundaki çalışma kodlarını takip edin.
1. Her çalışma kodu *Kapalı* veya *İptal edildi* durumunda olduğunda, sevkiyatı onaylamak için yeniden deneyin.
