---
title: Fiziksel güncelleştirme miktarının ondalık yuvarlaması hatalı
description: Sevk irsaliyesi oluşturduğunuzda giden yük, birimde tanımlanan ondalık hassasiyetle eşleşmeyen bir miktar içeriyor.
author: GalynaFedorova
ms.date: 5/31/2021
ms.topic: troubleshooting
ms.search.form: WHSLoadPlanningListPage_WHSSalesPackingSlipPost, WHSLoadTable_WHSSalesPackingSlipPost
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: v-gfedorova
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: a9e0475aab452daa9e1a6f012e17a59e611010da
ms.sourcegitcommit: 008779c530798f563fe216810d34b2d56f2c8d3c
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 12/14/2021
ms.locfileid: "7920485"
---
# <a name="decimal-rounding-of-the-physical-updating-quantity-is-incorrect"></a>Fiziksel güncelleştirme miktarının ondalık yuvarlaması hatalı

Hata kodu: SYS19589

## <a name="symptoms"></a>Belirtiler

Sevk irsaliyesi oluşturduğunuzda giden yük, birimde tanımlanan ondalık hassasiyetle eşleşmeyen bir miktar içeriyor.

Sevk irsaliyesi oluşturmaya çalıştığınızda, sistem aşağıdaki hata iletisini gösterir:

> %1 birimi cinsinden fiziksel güncelleştirme miktarıyla ilgili ondalık yuvarlama işlemi yanlış.

Bu nedenle, yükleme için sevk irsaliyesi oluşturamazsınız.

## <a name="cause"></a>Nedeni

Sistem, sevkiyat miktarını ondalık yuvarlamasının sevkiyat birimi için tanımlanan ondalık hassasiyetle uygun olup olmadığını değerlendirir. Sistem sevkiyat miktarını belirtilen ondalık basamak sayısına yuvarladığında, yuvarlanan sevkiyat miktarının gerçek sevkiyat miktarıyla eşleşmediğini tespit ederse, sevk irsaliyesini oluşturamazsınız. Örneğin, satış miktarı 1,75 kilogram (kg) ise, ancak ondalık duyarlık *1* olarak ayarlanmışsa, bu sorun oluşabilir.

## <a name="resolution"></a>Çözüm

Yükleme veya sevkiyat işlemi şu anda sevk irsaliyesi oluşturmanın başarısız olduğu bir durumdadır. Bu sorunu gidermek için aşağıdaki görevlerden birini tamamlayın:

- Yük satırlarını gözden geçirin ve miktarın ondalık sayılar veya yuvarlama sorunları olmadan net bir şekilde dönüştürülebilmesini sağlamak için ayarlamalar yapın.
- Yük satırlarınızı gözden geçirin ve birim ve miktarın birimin ondalık duyarlığıyla uyumlu hale getirilmesini sağlamak için ayarlamalar yapın.

### <a name="review-your-load-lines-and-make-adjustments-to-ensure-that-the-quantity-can-be-cleanly-converted-without-decimal-numbers-and-any-other-rounding-issues"></a>Yük satırlarını gözden geçirin ve miktarın ondalık sayılar veya yuvarlama sorunları olmadan net bir şekilde dönüştürülebilmesini sağlamak için ayarlamalar yapın

Yük satırlarını gözden geçirmek için aşağıdaki yordamı kullanın ve miktarın ondalık sayılar veya yuvarlama sorunları olmadan net bir şekilde dönüştürülebilmesini sağlamak için ayarlamalar yapın.

1. **Ambar yönetimi \> Yükler \> Tüm yükler**'e gidin.
1. Sevk irsaliyesinin oluşturulamadığı yükü seçin.
1. Eylem Bölmesinde, **Sevk ve teslim alma** sekmesinin **Tersine çevir** grubunda **Sevkiyat onayını tersine çevir**'i seçin.
1. **Yük satırları** sekmesinde, soruna neden olan maddenin yük satırını seçin.
1. Çekilen miktarı ayarlamak için **Çekilen miktarı düş**'ü seçin.
1. **Satır ayrıntıları** sekmesinde, **Sipariş**'i seçin.
1. Sevk irsaliyesi oluşturma işleminin devam edebilmesi için **Miktar** alanını çekilen miktara (yani **İşle oluşturulan miktar** alanının değerine) ayarlayın.

### <a name="review-your-load-lines-and-make-adjustments-to-ensure-that-the-unit-and-quantity-are-aligned-with-the-decimal-precision-of-the-unit"></a>Yük satırlarınızı gözden geçirin ve birim ve miktarın birimin ondalık duyarlığıyla uyumlu hale getirilmesini sağlamak için ayarlamalar yapın

Yük satırlarınızı gözden geçirmek için aşağıdaki yordamı kullanın ve birim ve miktarın birimin ondalık duyarlığıyla uyumlu hale getirilmesini sağlamak için ayarlamalar yapın.

1. **Ambar yönetimi \> Yükler \> Tüm yükler**'e gidin.
1. Sevk irsaliyesinin oluşturulamadığı yükü seçin.
1. **Yük satırları** hızlı sekmesinde, soruna neden olan maddenin yük satırını seçin. **Miktar** ve **Birim** alanlarının değerini not alın.
1. **Kuruluş yönetimi \> Birimler \> Birimler**'e gidin.
1. Sevk irsaliyesinin oluşturulamadığı birimi seçin.
1. **Ondalık duyarlık** alanının değerini gerektiği gibi ayarlayın.
