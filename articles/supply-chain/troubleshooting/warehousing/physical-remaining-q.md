---
title: Birimde kalan fiziksel miktar sıfır olmamalıdır
description: Bir sevk irsaliyesi oluşturduğunuzda, buna sağlanan verilerde sıfır olmayan stok miktarı ancak sıfır satış miktarı vardır.
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
ms.openlocfilehash: bfd381160bcfd1e6e5489e16cc22178b8a5142ee
ms.sourcegitcommit: e6437d994c3be0c5bb4a9263af3aa8351020d83a
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/14/2021
ms.locfileid: "6248808"
---
# <a name="physical-remaining-quantity-in-the-unit-must-not-be-zero"></a>Birimde kalan fiziksel miktar sıfır olmamalıdır

Hata kodu: SYS19591

## <a name="symptoms"></a>Belirtiler

Bir sevk irsaliyesi oluşturduğunuzda, buna sağlanan verilerde sıfır olmayan stok miktarı ancak sıfır satış miktarı vardır.

Sevk irasliyesi oluşturmaya çalıştığınızda, sistem aşağıdaki hata iletisini gösterir:

> %1 birimi cinsinden kalan fiziksel miktar sıfırdan farklı olmalıdır.

Bu nedenle, yükleme için sevk irsaliyesi oluşturamazsınız.

## <a name="cause"></a>Nedeni

Sistem, stok birimindeki fiziksel kalan miktarı ve sevkiyat birimindeki fiziksel kalan miktarı değerlendirir. Sistem sevkiyat biriminde kalan fiziksel miktarın 0 (sıfır) olduğunu, ancak stok birimindeki fiziksel kalan miktarın 0 olmadığını tespit ederse, sevk irsaliyesini oluşturamazsınız. Örneğin, maddenin satış birimi ve stok birimi farklıysa ve birimler arasındaki dönüştürme doğru değilse bu sorun oluşabilir.

## <a name="resolution"></a>Çözüm

Yükleme veya sevkiyat işlemi şu anda sevk irsaliyesi oluşturmanın başarısız olduğu bir durumdadır. Bu sorunu gidermek için aşağıdaki görevlerden birini tamamlayın:

- Yük satırlarınızı gözden geçirin ve tüm ilgili işlerin son sevkiyat konumunda tamamlandığından ve miktarların aynı olduğundan emin olun.
- Yük satırlarını gözden geçirin ve miktarın yuvarlama sorunları olmadan net bir şekilde dönüştürülebilmesini sağlamak için ayarlamalar yapın.
- Yük satırlarınızı gözden geçirin ve birim ve miktarın birimin ondalık duyarlığıyla uyumlu hale getirilmesini sağlamak için ayarlamalar yapın.
- Stok ölçü biriminin satış ölçü biriminden küçük olduğundan emin olun.

### <a name="review-your-load-lines-and-make-sure-that-all-the-related-work-has-been-completed-at-the-final-shipping-location-and-that-the-quantities-match"></a>Yük satırlarınızı gözden geçirin ve tüm ilgili işlerin son sevkiyat konumunda tamamlandığından ve miktarların aynı olduğundan emin olun

Yük satırlarınızı gözden geçirmek için aşağıdaki yordamı kullanın ve tüm ilgili işlerin son sevkiyat konumunda tamamlandığından ve miktarların aynı olduğundan emin olun.

1. **Ambar yönetimi \> Yükler \> Tüm yükler**'e gidin.
1. Sevkiyatın onaylanamadığı ilgili yükü seçin.
1. **Yük satırları** hızlı sekmesinde, yük satırını seçin.
1. **Oluşturulan iş miktarı** alanının değerini not alın.
1. Eylem Bölmesinde **Yüklemeler** sekmesindeki **İlgili bilgiler** grubunda **Çalışma**'yı seçin.
1. İşin son sevkiyat konumunda tamamlandığını ve teslim alınan iş miktarının yükleme satırındaki oluşturulan iş miktarıyla eşleştiğini doğrulayın.
1. Tüm ölçütlerin karşılandığından emin olmak için bu prosedürü tüm yükleme satırları için yineleyin.

### <a name="review-your-load-lines-and-make-adjustments-to-ensure-that-the-quantity-can-be-cleanly-converted-without-rounding-issues"></a>Yük satırlarını gözden geçirin ve miktarın yuvarlama sorunları olmadan net bir şekilde dönüştürülebilmesini sağlamak için ayarlamalar yapın

Yük satırlarını gözden geçirmek için aşağıdaki yordamı kullanın ve miktarın yuvarlama sorunları olmadan net bir şekilde dönüştürülebilmesini sağlamak için ayarlamalar yapın

1. **Ambar yönetimi \> Yükler \> Tüm yükler**'e gidin.
1. Sevk irsaliyesinin oluşturulamadığı yükü seçin.
1. Eylem Bölmesi'nde,  **Sevk ve teslim alma** sekmesinin  **Tersine çevir** grubunda  **Sevkiyat onayını tersine çevir**'i seçin.
1.  **Yük satırları** sekmesinde, fazla teslimatı aşan maddenin yük satırını seçin.
1. Çekilen miktarı ayarlamak için **Çekilen miktarı düş**'ü seçin.
1.  **Satır ayrıntıları** sekmesinde, **Sipariş**'i seçin.
1. Sevk irsaliyesi oluşturma işleminin devam edebilmesi için **Miktar** alanını çekilen miktara (yani **İşle oluşturulan miktar** alanının değerine) ayarlayın.

### <a name="review-your-load-lines-and-make-adjustments-to-ensure-that-the-unit-and-quantity-are-aligned-with-the-decimal-precision-of-the-unit"></a>Yük satırlarınızı gözden geçirin ve birim ve miktarın birimin ondalık duyarlığıyla uyumlu hale getirilmesini sağlamak için ayarlamalar yapın

Yük satırlarınızı gözden geçirmek için aşağıdaki yordamı kullanın ve birim ve miktarın birimin ondalık duyarlığıyla uyumlu hale getirilmesini sağlamak için ayarlamalar yapın.

1. **Ambar yönetimi \> Yükler \> Tüm yükler**'e gidin.
1. Sevk irsaliyesinin oluşturulamadığı yükü seçin.
1. **Yük satırları** hızlı sekmesinde, soruna neden olan maddenin yük satırını seçin. **Miktar** ve **Birim** alanlarının değerini not alın.
1. **Kuruluş yönetimi \> Birimler \> Birimler**'e gidin.
1. Sevk irsaliyesinin oluşturulamadığı birimi seçin.
1. **Ondalık duyarlık** alanının değerini gerektiği gibi ayarlayın.

### <a name="make-sure-that-the-inventory-unit-of-measure-is-smaller-than-the-sales-unit-of-measure"></a>Stok ölçüm biriminin satış ölçüm biriminden küçük olduğundan emin olun

Stok ölçü biriminin satış ölçü biriminden küçük olduğundan emin olun. Madde için ölçü birimini gerektiği gibi yeniden yapılandırmayı düşünün.
