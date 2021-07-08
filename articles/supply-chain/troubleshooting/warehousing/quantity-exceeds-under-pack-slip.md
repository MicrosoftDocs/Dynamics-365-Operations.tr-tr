---
title: Sevk irsaliyesi oluşturma sırasında miktar eksik teslimat yüzdesini aşıyor
description: Sevk irsaliyesi oluşturduğunuzda, giden yük eksik teslimat yüzdesini aşan bir miktar içerir.
author: GalynaFedorova
ms.date: 5/31/2021
ms.topic: troubleshooting
ms.search.form: WHSLoadTable_WHSSalesPackingSlipPost,WHSLoadPlanningListPage_WHSSalesPackingSlipPost,WHSLoadPlanningWorkbench_WHSSalesPackingSlipPost
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: v-gfedorova
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: ecdd377d12faf40f64736e93671dcf42ff132403
ms.sourcegitcommit: e6437d994c3be0c5bb4a9263af3aa8351020d83a
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/14/2021
ms.locfileid: "6249182"
---
# <a name="quantity-exceeds-under-delivery-percentage-during-packing-slip-generation"></a>Sevk irsaliyesi oluşturma sırasında miktar eksik teslimat yüzdesini aşıyor

Hata kodu: SYS24921

## <a name="symptoms"></a>Belirtiler

Sevk irsaliyesi oluşturduğunuzda, giden yük eksik teslimat yüzdesini aşan bir miktar içerir.

Sevk irsaliyesi oluşturmaya çalıştığınızda, sistem aşağıdaki hata iletisini gösterir:

> Satırın eksik teslimat yüzdesi %1, ancak izin verilen eksik teslimat yüzdesi %2.

Bu nedenle, yükleme için sevk irsaliyesi oluşturamazsınız.

## <a name="cause"></a>Nedeni

Yük veya sevkiyart için çekilen miktar sipariş edilen miktardan azdır ve eksik teslimat yüzdesi aralığında değildir.

## <a name="resolution"></a>Çözüm

Yükleme veya sevkiyat işlemi şu anda sevk irsaliyesi oluşturmanın başarısız olduğu bir durumdadır. Bu sorunu gidermek için aşağıdaki görevlerden birini tamamlayın:

- Eksik teslimat yüzdesini ayarlayın.
- Tersine çevirin ve ayarlamalar yapın.

### <a name="adjust-the-under-delivery-percentage"></a>Eksik teslimat yüzdesini ayarlama

Eksik teslimat yüzdesini ayarlamak için aşağıdaki yordamı kullanın.

1. **Alacak hesapları \> Siparişler \> Tüm siparişler**'e gidin.
1. Yük için sevk irsaliyesini deftere nakledemeyeceğiniz satış siparişini seçin.
1.  **Satış siparişi satırları** sekmesinde, eksik teslimat yüzdesini aşan satış siparişi satırını seçin.
1.  **Satır ayrıntıları** sekmesinde, **Teslimatı**'ı seçin.
1. **Eksik teslimat** alanını, sevk irsaliyesi oluşturma işleminin devam edebilmesi için, yük miktarına karşı çekilen miktara uygun olması için daha yüksek bir yüzdeye ayarlayın.

### <a name="reverse-and-make-adjustments"></a>Tersine çevirme ve ayarlamalar yapma

Yük için deftere nakledilen her şeyi tersine çevirin (örneğin, sevk irsaliyesi, sevk irsaliyesi onayı ve iş), satış siparişi ayarlamaları yapın, siparişi ambara yeniden serbest bırakın ve sevkiyat yordamını tamamlayın.

Sevk irsaliyesini iptal etmek için aşağıdaki yordamı kullanın.

1. **Ambar yönetimi \> Yükler \> Tüm yükler**'e gidin.
1. Eylem Bölmesi'nde,  **Sevk ve teslim alma** sekmesinin  **Tersine çevir** grubunda  **Sevk irsaliyelerini iptal et**'i seçin.

Sevkiyat onayını tersine çevirmek için aşağıdaki yordamı kullanın.

1. **Ambar yönetimi \> Yükler \> Tüm yükler**'e gidin.
1. Eylem Bölmesi'nde,  **Sevk ve teslim alma** sekmesinin  **Tersine çevir** grubunda  **Sevkiyat onayını tersine çevir**'i seçin.

İşi tersine çevirmek için aşağıdaki yordamı kullanın.

1. **Ambar yönetimi \> Yükler \> Tüm yükler**'e gidin.
1. Eylem Bölmesinde  **Yükler** sekmesindeki  **İş** grubunda  **İşi tersine çevir**'i seçin.
