---
title: "Maliyet güncelleştirmelerini yönetme"
description: "Standart maliyet verilerindeki güncelleştirmeler iki farklı yaklaşımla yönetilebilir -  tek sürümlü yaklaşım ve iki sürümlü yaklaşım."
author: YuyuScheller
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CostingVersion
audience: Application User
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 69992
ms.assetid: 468de7af-c7b5-4345-bd5a-ba3aa5a900cc
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: mguada
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: d1d498b1a843415e106c90330dd661b78bc2865e
ms.contentlocale: tr-tr
ms.lasthandoff: 05/25/2017


---

# <a name="manage-standard-cost-updates"></a>Maliyet güncelleştirmelerini yönetme

[!include[banner](../includes/banner.md)]


Standart maliyet verilerindeki güncelleştirmeler iki farklı yaklaşımla yönetilebilir -  tek sürümlü yaklaşım ve iki sürümlü yaklaşım. 

Tek sürümlü yaklaşım, tüm maliyet kayıtlarını içeren tek bir maliyetlendirme sürümünü kullanır. Bu kayıtlar orijinal maliyetleri ve tüm maliyet güncelleştirmelerini içerir.
İki sürümlü yaklaşım, orijinal maliyetlerin kayıtlarını içeren bir sürümü ve tüm maliyet güncelleştirmelerini içeren ikinci bir sürümü kullanır. İki versiyonlu yaklaşımın birincil avantajı, maliyet güncelleştirmelerinin, orijinal maliyetlendirme versiyonunu etkilemeden ayrı bir maliyetlendirme versiyonunda net bir şekilde açıklanması ve izlenmesidir. İki sürümlü yaklaşım, her artımlı güncelleştirmenin artımlı maliyet kayıtlarını içeren ayrı bir maliyetlendirme sürümünün bulunduğu birden fazla artımlı güncelleştirmeyi belirlemek için kullanılabilir. **Örnek** Aşağıdaki örnekte, bir üretim ortamında standart maliyetleri güncelleştirmek için bir sürümlü ve sürümlü yaklaşımların nasıl kullanılabileceği gösterilmiştir. Örneğin, yeni maddeleri veya hata düzeltmelerini gösteren güncelleştirmeler. Tek maliyetlendirme sürümünün geçerli yıl için standart maliyetleri temsil ettiğini varsayalım. Bu sürüm için tanımlayıcı 2016-STD'dir. Sürüm 2016-STD tüm maddeler için geçerli etkin maliyetleri içerir. Ek olarak, 2016 yılının başında bilinen rota ile ilgili maliyet kategorileri ve gider hesaplama formüllerini içerir. 2016-STD, özgün maliyet sürümüdür.
-   **Maliyet verileri güncelleştirmeleri için tek sürümlü yaklaşım** - Tek sürümlü yaklaşımda, orijinal 2016-STD maliyetlendirme sürümü tüm maliyet kayıtlarını içerir. Maliyet güncelleştirmeleri 2016-STD içerisinde kaydedilir ve "Beklemede" durumuna ayarlanır Bekleyen maliyetler yeni satın alınan maddeler için el ile girilebilir veya düzeltmeleri yansıtacak şekilde üretilen bir maddeden hesaplanabilir. Tek sürümlü yaklaşım kullanıldığında, tüm etkin maliyetler maliyetlendirme sürümü tarafından kapsandığından, ürün reçetesi hesaplamaları için geri dönüş veri kaynağı gerekmez. Beklemede olan maliyetler etkin duruma geldiğinde, 2016-STD orijinal maliyetlendirme sürümü yeniden tüm geçerli etkin maliyetleri kapsar.
-   **Maliyet verileri güncelleştirmeleri için iki sürümlü yaklaşım** − İki sürümlü yaklaşım, yalnızca maliyet güncelleştirmelerini içeren ek bir maliyetlendirme sürümü gerektirir. Bu sürüm için tanımlayıcı 2016-STD-CHANGES'dir. Maliyet güncelleştirmeleri 2016-STD-CHANGES'a kaydedilir ve "Beklemede" durumuna ayarlanır. İki sürümlü yaklaşımla, üretilen maddeler için bekleyen maliyetlere ilişkin ürün reçetesi hesaplamaları bir geri dönüş veri kaynağı gerektirir. Bunun nedeni, ek maliyetlendirme sürümü olan 2016-STD-CHANGES'ın yalnızva bir maliyet verisi alt grubu içermesidir. Her ikisi de 2016-STD-CHANGES içinde yer almayan maliyet verilerinin kaynağını tanımladığından, geri dönüş etkin maliyetler veya maliyetlendirme versiyonu 2016-STD olarak ifade edilir. Bekleyen maliyetler etkin hale geldikten sonra, orijinal maliyetlendirme sürümü 2016-STD olduğu gibi kalırken maliyetlendirme sürümü 2016-STD-CHANGES güncellemeleri yansıtan geçerli etkin maliyetleri içerecektir. İki sürüm yaklaşımı kullanıldığında, orijinal maliyetlendirme sürümü için engelleme ilkeleri güncellemeleri engelleyecek şekilde ayarlanmalıdır. Belirtilen başlangıç tarihi ve güncelleştirmelere izin vermek için durdurma ilkelerinin seçimli kullanımı dışında, ek maliyetlendirme sürümü için aynı ilkeler ayarlanmalıdır. Belirtilen başlangıç tarihi, planlanan etkinleştirme tarihini yansıtmak için her toplu değişiklikle güncelleştirilmelidir.

Bu örnekte 2016 yılı boyunca güncelleştirmeleri yönetmek için bir ek maliyetlendirme versiyonu kullanılmıştır. Her toplu güncelleştirme için ayrı bir versiyon gibi birden fazla ek maliyetlendirme versiyonu da kullanılabilirdi. Birden fazla maliyetlendirme kullanıldığında, etkin maliyetler birden fazla maliyetlendirme sürümüne dağıtılacağından geri dönüşün etkin maliyetler şeklinde ifade edilmesi gerekir.






