---
title: Maliyet güncelleştirmelerini yönetme
description: Standart maliyet verilerindeki güncelleştirmeler iki farklı yaklaşımla yönetilebilir - tek sürümlü yaklaşım ve iki sürümlü yaklaşım.
author: AndersGirke
ms.date: 01/15/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CostingVersion, InventItemPrice, InventParameters
audience: Application User
ms.reviewer: kamaybac
ms.custom: 69992
ms.assetid: 468de7af-c7b5-4345-bd5a-ba3aa5a900cc
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: mguada
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: 3485f0722b8b99d7dc2d6dab470fdcc465b1da3d
ms.sourcegitcommit: 1e5a46271bf7fae2f958d2b1b666a8d2583e04a8
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/25/2021
ms.locfileid: "7678678"
---
# <a name="manage-standard-cost-updates"></a>Maliyet güncelleştirmelerini yönetme

[!include [banner](../includes/banner.md)]

Standart maliyet verilerindeki güncelleştirmeler iki farklı yaklaşımla yönetilebilir - tek sürümlü yaklaşım ve iki sürümlü yaklaşım.

Tek sürümlü yaklaşım, tüm maliyet kayıtlarını içeren tek bir maliyetlendirme sürümünü kullanır. Bu kayıtlar orijinal maliyetleri ve tüm maliyet güncelleştirmelerini içerir.

İki sürümlü yaklaşım, orijinal maliyetlerin kayıtlarını içeren bir sürümü ve tüm maliyet güncelleştirmelerini içeren ikinci bir sürümü kullanır. İki versiyonlu yaklaşımın birincil avantajı, maliyet güncelleştirmelerinin, orijinal maliyetlendirme versiyonunu etkilemeden ayrı bir maliyetlendirme versiyonunda net bir şekilde açıklanması ve izlenmesidir. İki sürümlü yaklaşım, her artımlı güncelleştirmenin artımlı maliyet kayıtlarını içeren ayrı bir maliyetlendirme sürümünün bulunduğu birden fazla artımlı güncelleştirmeyi belirlemek için kullanılabilir.

## <a name="example"></a>Örnek

Aşağıdaki örnekte, bir üretim ortamında standart maliyetleri güncelleştirmek için bir sürümlü ve sürümlü yaklaşımların nasıl kullanılabileceği gösterilmiştir. Örneğin, yeni maddeleri veya hata düzeltmelerini gösteren güncelleştirmeler. Tek maliyetlendirme sürümünün geçerli yıl için standart maliyetleri temsil ettiğini varsayalım. Bu sürüm için tanımlayıcı 2020-STD'dir. Sürüm 2020-STD tüm maddeler için geçerli etkin maliyetleri içerir. Ek olarak, 2020 yılının başında bilinen rota ile ilgili maliyet kategorileri ve gider hesaplama formüllerini içerir. 2020-STD, özgün maliyet sürümüdür.

- **Maliyet verileri güncelleştirmeleri için tek sürümlü yaklaşım** - Tek sürümlü yaklaşımda, orijinal 2020-STD maliyetlendirme sürümü tüm maliyet kayıtlarını içerir. Maliyet güncelleştirmeleri 2020-STD içerisinde kaydedilir ve Beklemede durumuna ayarlanır. Bekleyen maliyetler yeni satın alınan maddeler için el ile girilmiş olabilir veya düzeltmeleri yansıtmak için üretilmiş bir madde için hesaplanmış olabilir. Tek versiyonlu yaklaşım kullanıldığında ürün reçetesi hesaplamaları, tüm etkin maliyetler maliyetlendirme versiyonunda yer aldığından geri dönüş veri kaynağı gerektirmez. Beklemede olan maliyetler etkin duruma geldiğinde, 2020-STD orijinal maliyetlendirme sürümü yeniden tüm geçerli etkin maliyetleri kapsar.
- **Maliyet verileri güncelleştirmeleri için iki sürümlü yaklaşım** − İki sürümlü yaklaşım, yalnızca maliyet güncelleştirmelerini içeren ek bir maliyetlendirme sürümü gerektirir. Bu sürüm için tanımlayıcı 2020-STD-CHANGES'dir. Maliyet güncelleştirmeleri 2020-STD-CHANGES içerisinde kaydedilir ve Beklemede durumuna ayarlanır. İki sürümlü yaklaşımda, üretilen maddeler için bekleyen maliyetlerin ürün reçetesi hesaplamaları bir geri dönüş veri kaynağı gerektirir. Bunun nedeni, ek maliyetlendirme sürümü olan 2020-STD-CHANGES'ın yalnızva bir maliyet verisi alt grubu içermesidir. Her ikisi de 2020-STD-CHANGES içinde yer almayan maliyet verilerinin kaynağını tanımladığından, geri dönüş etkin maliyetler veya maliyetlendirme versiyonu 2020-STD olarak ifade edilir. Bekleyen maliyetler etkinleştirildikten sonra, maliyetlendirme versiyonu 2020-STD-CHANGES güncelleştirmeleri yansıtan geçerli etkin maliyetleri içerirken, orijinal maliyetlendirme versiyonu 2020-STD bu durumdan etkilenmez. İki versiyonlu yaklaşım kullanıldığında, orijinal maliyetlendirme sürümü için durdurma ilkelerinin güncelleştirmeleri önleyecek şekilde ayarlanması gerekir. Belirtilen başlangıç tarihi ve güncelleştirmelere izin vermek için durdurma ilkelerinin seçimli kullanımı dışında, ek maliyetlendirme sürümü için aynı ilkeler ayarlanmalıdır. Belirtilen başlangıç tarihi, planlanan etkinleştirme tarihini yansıtmak için her toplu değişiklikle güncelleştirilmelidir.

Bu örnekte 2020 yılı boyunca güncelleştirmeleri yönetmek için bir ek maliyetlendirme versiyonu kullanılmıştır. Her toplu güncelleştirme için ayrı bir versiyon gibi birden fazla ek maliyetlendirme versiyonu da kullanılabilirdi. Birden fazla maliyetlendirme kullanıldığında, etkin maliyetler birden fazla maliyetlendirme sürümüne dağıtılacağından geri dönüşün etkin maliyetler şeklinde ifade edilmesi gerekir.

## <a name="financial-dimensions-for-the-standard-cost-revaluation"></a>Standart maliyet yeniden değerlemesi için mali boyutlar

Yeni bir standart fiyat etkinleştirildiğinde, genellikle eldeki stok değeri standart maliyet yeniden değerlemesi hareketleriyle yeniden değerlenir. Genellikle maddenin mali boyutları daha sonra hareketlerde deftere nakledilir. Ancak mali boyutların deftere nakledilip nakledilmeyeceğini ve nasıl nakledileceğini denetlemek istiyorsanız *Stok standart maliyeti yeniden değerlemesi için mali boyutları varsayılana ayarlama seçenekleri* adlı özelliği açmak için [özellik yönetimini](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) kullanın. Bu özelliği etkinleştirdikten sonra **Maliyet yönetimi > Stok muhasebesi ilkeleri kurulumu > Parametreler**'e gidin ve yeni **Mali boyut kaynağı** açılır listesini aşağıdaki değerlerden birine ayarlayın.

- **Hiçbiri**: Hiçbir mali boyut, yeniden değerleme işlemi hareketlerine nakledilmez. Hesap yapınız zorunlu bir mali boyut içeriyorsa yeniden değerleme süreci çalışmaya devam eder ancak mali boyutları olmayan muhasebe girişleri oluşturur. Bu durumda, kullanıcılar önce bir uyarı iletisi alır; böylece gerekirse yeniden değerlemeyi iptal edebilirler.
- **Tablo**: Maddenin mali boyutları, yeniden değerleme işlemi hareketlerinde deftere nakledilir. Bu, varsayılan ayardır ve *Stok standart maliyeti yeniden değerlemesi için mali boyutları varsayılana ayarlama seçenekleri* özelliğini açmadan gerçekleşen özgün sistem davranışıyla uyumludur.
- **Nakletme** – Yeniden değerleme yapılan hareketin mali boyutları, yeniden değerleme işlemi hareketlerine nakledilir. Varsayılan olarak, hem stok hesabı hem de yeniden değerleme hesabı için özgün hareketin stok hesabındaki mali boyutlar kullanılır.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]