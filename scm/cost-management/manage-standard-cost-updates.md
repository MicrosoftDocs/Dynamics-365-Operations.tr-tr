---
title: "Standart Maliyet güncelleştirmeleri yönetme"
description: "Standart maliyet verileri güncelleştirmeler iki farklı yaklaşım - sürüm bir yaklaşım ve iki sürüm yaklaşım kullanılarak yönetilebilir."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: CostingVersion
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 69992
ms.assetid: 468de7af-c7b5-4345-bd5a-ba3aa5a900cc
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: mguada
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9ccbe5815ebb54e00265e130be9c82491aebabce
ms.openlocfilehash: 7e0f0817ff37c82ed98a51f10bcdde7e785a19a3
ms.lasthandoff: 03/31/2017


---

# <a name="manage-standard-cost-updates"></a>Standart Maliyet güncelleştirmeleri yönetme

Standart maliyet verileri güncelleştirmeler iki farklı yaklaşım - sürüm bir yaklaşım ve iki sürüm yaklaşım kullanılarak yönetilebilir. 

Tek sürümlü yaklaşım, tüm maliyet kayıtlarını içeren tek bir maliyetlendirme sürümünü kullanır. Bu kayıtlar orijinal maliyetleri ve tüm maliyet güncelleştirmelerini içerir.
İki sürümlü yaklaşım, orijinal maliyetlerin kayıtlarını içeren bir sürümü ve tüm maliyet güncelleştirmelerini içeren ikinci bir sürümü kullanır. İki versiyonlu yaklaşımın birincil avantajı, maliyet güncelleştirmelerinin, orijinal maliyetlendirme versiyonunu etkilemeden ayrı bir maliyetlendirme versiyonunda net bir şekilde açıklanması ve izlenmesidir. İki sürümlü yaklaşım, her artımlı güncelleştirmenin artımlı maliyet kayıtlarını içeren ayrı bir maliyetlendirme sürümünün bulunduğu birden fazla artımlı güncelleştirmeyi belirlemek için kullanılabilir. **Örnek** Aşağıdaki örnekte, bir üretim ortamında standart maliyetleri güncelleştirmek için bir sürümlü ve sürümlü yaklaşımların nasıl kullanılabileceği gösterilmiştir. Örneğin, yeni maddeleri veya hata düzeltmelerini gösteren güncelleştirmeler. Tek maliyetlendirme sürümünün geçerli yıl için standart maliyetleri temsil ettiğini varsayalım. Bu sürüm için tanımlayıcı 2016-STD'dir. Sürüm 2016-STD tüm maddeler için geçerli etkin maliyetleri içerir. Ayrıca, tüm yönlendirme ile ilgili maliyet kategorileri ve 2016 yılı başlangıcında bilinir genel gider hesaplama formülleri içerir. Özgün maliyet sürümü 2016-STD.
-   **Maliyet verileri güncelleştirmeleri için tek sürümlü yaklaşım** - Tek sürümlü yaklaşımda, orijinal 2016-STD maliyetlendirme sürümü tüm maliyet kayıtlarını içerir. Maliyet güncelleştirmeleri 2016-STD kaydedilir ve "Beklemede" durumuna ayarla Bekleyen maliyetleri yeni satın alınan maddeler için el ile girilebilir veya düzeltmeleri yansıtacak şekilde mamul bir madde için hesaplanabilecek. Sürüm bir yaklaşım kullanıldığında, tüm etkin maliyetleri maliyet sürümüne içerdiğinden ürün reçetesi hesaplamaları temel veri kaynağı gerektirmez. Beklemede olan maliyetler etkin duruma geldiğinde, 2016-STD orijinal maliyetlendirme sürümü yeniden tüm geçerli etkin maliyetleri kapsar.
-   **Maliyet verileri güncelleştirmeleri için iki sürümlü yaklaşım** − İki sürümlü yaklaşım, yalnızca maliyet güncelleştirmelerini içeren ek bir maliyetlendirme sürümü gerektirir. Bu sürüm için tanımlayıcı 2016-STD-CHANGES'dir. Maliyet güncelleştirmeleri 2016-STD-CHANGES'a kaydedilir ve "Beklemede" durumuna ayarlanır. İki sürümlü yaklaşımla, üretilen maddeler için bekleyen maliyetlere ilişkin ürün reçetesi hesaplamaları bir geri dönüş veri kaynağı gerektirir. Bunun nedeni, ek maliyetlendirme sürümü olan 2016-STD-CHANGES'ın yalnızva bir maliyet verisi alt grubu içermesidir. Her ikisi de 2016-STD-CHANGES içinde yer almayan maliyet verilerinin kaynağını tanımladığından, geri dönüş etkin maliyetler veya maliyetlendirme versiyonu 2016-STD olarak ifade edilir. Bekleyen maliyetler etkin hale geldikten sonra, orijinal maliyetlendirme sürümü 2016-STD olduğu gibi kalırken maliyetlendirme sürümü 2016-STD-CHANGES güncellemeleri yansıtan geçerli etkin maliyetleri içerecektir. İki sürüm yaklaşımı kullanıldığında, orijinal maliyetlendirme sürümü için engelleme ilkeleri güncellemeleri engelleyecek şekilde ayarlanmalıdır. Belirtilen başlangıç tarihi ve güncelleştirmelere izin vermek için durdurma ilkelerinin seçimli kullanımı dışında, ek maliyetlendirme sürümü için aynı ilkeler ayarlanmalıdır. Belirtilen başlangıç tarihi, planlanan etkinleştirme tarihini yansıtmak için her toplu değişiklikle güncelleştirilmelidir.

Bu örnek, bir ek maliyet sürümü 2016 yılı boyunca güncelleştirmeleri yönetmek için kullanılır. Her toplu güncelleştirmeleri için ayrı bir sürüm gibi birden fazla ek maliyet sürümü kullanılabilir. Birden fazla maliyetlendirme kullanıldığında, etkin maliyetler birden fazla maliyetlendirme sürümüne dağıtılacağından geri dönüşün etkin maliyetler şeklinde ifade edilmesi gerekir.




