---
title: Sevk irsaliyesi oluşturma sırasında miktar fazla teslimat yüzdesini aşıyor
description: Sevk irsaliyesi oluşturduğunuzda, giden yük fazla teslimat yüzdesini aşan bir miktar içerir.
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
ms.openlocfilehash: bc74c5748950b1f0f001fd89acb2e023640065ee
ms.sourcegitcommit: 008779c530798f563fe216810d34b2d56f2c8d3c
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 12/14/2021
ms.locfileid: "7920062"
---
# <a name="quantity-exceeds-over-delivery-percentage-during-packing-slip-generation"></a>Sevk irsaliyesi oluşturma sırasında miktar fazla teslimat yüzdesini aşıyor

Hata kodu: SYS24920

## <a name="symptoms"></a>Belirtiler

Sevk irsaliyesi oluşturduğunuzda, giden yük fazla teslimat yüzdesini aşan bir miktar içerir.

Sevk irsaliyesi oluşturmaya çalıştığınızda, sistem aşağıdaki hata iletisini gösterir:

> Satırın fazla teslimat yüzdesi %1, ancak izin verilen fazla teslimat yüzdesi %2.

Bu nedenle, yükleme için sevk irsaliyesi oluşturamazsınız.

## <a name="cause"></a>Nedeni

Yük veya sevkiyart için çekilen miktar sipariş edilen miktardan çoktur ve fazla teslimat yüzdesi aralığında değildir.

## <a name="resolution"></a>Çözüm

Yükleme veya sevkiyat işlemi şu anda sevk irsaliyesi oluşturmanın başarısız olduğu bir durumdadır. Bu sorunu gidermek için aşağıdaki görevlerden birini tamamlayın:

- Yük satırı miktarını ayarlama
- Fazla teslimat yüzdesini ayarlayın.
- Tersine çevirin ve ayarlamalar yapın.

### <a name="adjust-the-load-line-quantity"></a>Yük satırı miktarını ayarlama

Yük satırı miktarını ayarlamak için aşağıdaki yordamı kullanın.

1. **Ambar yönetimi \> Yükler \> Tüm yükler**'e gidin.
1. Sevk irsaliyesinin oluşturulamadığı yükü seçin.
1. Eylem Bölmesinde, **Sevk ve teslim alma** sekmesinin **Tersine çevir** grubunda **Sevkiyat onayını tersine çevir**'i seçin.
1. **Yük satırları** sekmesinde, fazla teslimat yüzdesini aşan maddenin yük satırını seçin.
1. Çekilen miktarı ayarlamak için **Çekilen miktarı düş**'ü seçin.
1. **Satır ayrıntıları** sekmesinde, **Sipariş**'i seçin.
1. Sevk irsaliyesi oluşturma işleminin devam edebilmesi için **Miktar** alanını çekilen miktara (yani **İşle oluşturulan miktar** alanının değerine) ayarlayın.

### <a name="adjust-the-over-delivery-percentage"></a>Fazla teslimat yüzdesini ayarlama

Fazla teslimat yüzdesini ayarlamak için aşağıdaki yordamı kullanın.

1. **Alacak hesapları \> Siparişler \> Tüm siparişler**'e gidin.
1. Yük için sevk irsaliyesini deftere nakledemeyeceğiniz satış siparişini seçin.
1. **Satış siparişi satırları** sekmesinde, fazla teslimat yüzdesini aşan maddenin satış siparişi satırını seçin.
1. **Satır ayrıntıları** sekmesinde, **Teslimat**'ı seçin.
1. **Fazla teslimat** alanını, sevk irsaliyesi oluşturma işleminin devam edebilmesi için, yük miktarına karşı çekilen miktara uygun olması için daha yüksek bir yüzdeye ayarlayın.

### <a name="reverse-and-make-adjustments"></a>Tersine çevirme ve ayarlamalar yapma

Yük için deftere nakledilen her şeyi tersine çevirin (örneğin, sevk irsaliyesi, sevk irsaliyesi onayı ve iş), satış siparişi ayarlamaları yapın, siparişi ambara yeniden serbest bırakın ve sevkiyat yordamını tamamlayın.

Sevk irsaliyesini iptal etmek için aşağıdaki yordamı kullanın.

1. **Ambar yönetimi \> Yükler \> Tüm yükler**'e gidin.
1. Eylem Bölmesinde, **Sevk ve teslim alma** sekmesinin **Tersine çevir** grubunda **Sevk irsaliyelerini iptal et**'i seçin.

Sevkiyat onayını tersine çevirmek için aşağıdaki yordamı kullanın.

1. **Ambar yönetimi \> Yükler \> Tüm yükler**'e gidin.
1. Eylem Bölmesinde, **Sevk ve teslim alma** sekmesinin **Tersine çevir** grubunda **Sevkiyat onayını tersine çevir**'i seçin.

İşi tersine çevirmek için aşağıdaki yordamı kullanın.

1. **Ambar yönetimi \> Yükler \> Tüm yükler**'e gidin.
1. Eylem Bölmesinde, **Yükler** sekmesinin **İş** grubunda **İşi tersine çevir**'i seçin.
