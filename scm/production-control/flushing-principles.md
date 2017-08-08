---
title: "Otomatik tüketim kuralları"
description: "Bu konu ham madde tüketiminde kullanılan dört otomatik tüketim prensibini açıklar."
author: BibiSp
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, Operations, UnifiedOperations
ms.custom: 221264
ms.assetid: dde49743-1541-4353-a030-63ca3069cd7d
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2016-11-30T00:00:00.000Z
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: 08c38aada355583c5a6872f75b57db95d9b81786
ms.openlocfilehash: 9eb39893bbb7fdcb11d6c1d0b73dc0278ff1f814
ms.contentlocale: tr-tr
ms.lasthandoff: 07/27/2017

---

# <a name="controlling-raw-material-consumption-by-using-flushing-principles"></a>Temizlik ilkeleri kullanarak ham madde tüketimini kontrol etme

[!include[banner](../includes/banner.md)]

Otomatik tüketim ilkeleri, üretim işlemlerinde kullanılan ham maddeler için farklı tüketim stratejilerini yansıtır. Tüketim, malzemeyi eldeki stoktan azaltan ve tüketilen maddelerin değerini üretim emirleri ve toplu iş siparişleri için **Süren iş**'e (WIP) ayarlayan işlemdir. Hammaddeler genellikle, maddeyi tüketen işlem için yapılandırılan konumda tüketilir. Bu konum üretim giriş konumu olarak bilinir.

Malzeme tüketiminden önce, malzemeler giriş konumuna taşınır. Aşağıdaki çizimde işlem gösterilmiştir.

[![scenario4a](./media/scenario4a.png)](./media/scenario4a.png)

1. Malzeme ambarı
2. Hammadde çekme
3. Üretim giriş yeri
4. Hammadde tüketimi
5. Üretim işlemi

Malzeme tüketimi aşağıdaki dört otomatik tüketim ilkeleri kullanılarak denetlenir:

- El ile
- Başlat
- Son
- Yerleşimde kullanılabilir

Otomatik tüketim ilkeleri varsayılan değerler hiyerarşisi içerisinde yapılandırılır. Hiyerarşi, otomatik tüketim ilkesinin **Başlat** değerine sahip olduğu serbest bırakılan üründe başlar. Ürün reçetesi (BOM) veya formül satırı üzerinde, üründen gelen otomatik tüketim ilkesi geçersiz kılınabilir. BOM satırları veya toplu iş siparişi formül satırlarındaki varsayılan otomatik tüketim ilkesi, üründen veya BOM veya formüller üzerindeki geçersiz kılınan değerden alınır.

## <a name="description-of-the-flushing-principles"></a>Otomatik tüketim ilkelerinin açıklaması

### <a name="manual"></a>El ile
El ile otomatik tüketim ilkesi, malzeme tüketiminin el ile yapılan bir işlem olduğunu gösterir. Bu ilke, örneğin zamanı izlemek istiyorsanız ve tüketilen toplu iş miktarlarını ve seri numaralarının izleme amacıyla takip edilmesi gerekiyorsa uygundur. El ile tüketim, bir üretim malzeme çekme listesi günlüğünde kayıtlıdır. Gelişmiş ambar işlemleri için etkinleştirilmiş maddeler için, bir el ile akış uygulanabilir.

### <a name="start"></a>Başlat
Otomatik tüketme başla ilkesi, malzemenin üretim emri başladığında otomatik olarak tüketileceğini belirtir. Tüketilen malzeme tutarı, başlatılan miktar ile orantılıdır. Otomatik tüketime başla ilkesi, üretim yürütme sistemiyle birlikte kullanıldığında, bir operasyon veya işlem işi başladığında malzemeleri otomatik tüketmek için de kullanılabilir. Bu ilke, örneğin tüketim farkı düşükse, malzemeler düşük değerli malzemelerse, izleme gereksinimleri yoksa veya operasyonlarda kısa çalışma zamanı varsa uygundur. 

### <a name="finish"></a>Son
Otomatik tüketimi tamamla ilkesi, malzemenin üretim emri tamamlandı olarak raporlandığında veya malzemeleri tüketmek üzere ayarlanmış bir operasyon tamamlandı olarak kaydedildiğinde otomatik olarak tüketileceğini belirtir. Tüketilen malzeme tutarı, tamamlandı olarak raporlanan miktar ile orantılıdır. Otomatik tüketimi tamamla ilkesi, üretim yürütme sistemiyle birlikte kullanıldığında, bir operasyon veya işlem işi tamamlandığında malzemeleri otomatik tüketmek için de kullanılabilir. Bu ilke, Başlat ilkesi ile aynı durumlarda geçerlidir. Ancak, Tamamla ilkesi, malzemenin operasyon tamamlanmadan önce WIP olarak ayarlanmaması gereken daha uzun çalışma süresine sahip operasyonlar içindir. 

### <a name="available-at-location"></a>Yerleşimde kullanılabilir
Konum otomatik tüketimde kullanılabilir ilkesi, malzeme üretim için çekildi olarak kaydedildiğinde malzemenin otomatik olarak tüketileceğini belirtir. Malzeme, hammadde çekme işi tamamlandığında veya malzeme üretim giriş konumunda kullanılabilir olduğunda ve malzeme hattı ambara serbest bırakıldığında konumdan çekildi olarak kaydedilir. İşlem içinde oluşturulan malzeme çekme listesi, toplu iş içerisinde deftere nakledilir. Bu örnek, örneğin bir üretim emrine karşılık birden fazla malzeme çekme etkinliği varsa uygundur. Bu durumda malzeme çekme listesini el ile güncelleştirmeniz gerekmez ve WIP bakiyesinin geçerli görünümünü elde edebilirsiniz.

