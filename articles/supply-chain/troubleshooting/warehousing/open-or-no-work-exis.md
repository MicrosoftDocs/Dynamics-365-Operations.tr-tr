---
title: Tamamlanmamış veya eksik çalışmalar nedeniyle sevkiyatı onaylayamıyorsunuz
description: Tamamlanmamış veya eksik çalışmalar nedeniyle sevkiyatı onaylayamıyorsunuz
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
ms.openlocfilehash: da6388d433d6021a99840ae9781c717db1b540a9
ms.sourcegitcommit: cd9016e9787169cb800889d335b9c5919ddbe4af
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2021
ms.locfileid: "5938568"
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
