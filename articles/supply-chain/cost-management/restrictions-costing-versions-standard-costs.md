---
title: "Standart maliyetler için maliyetlendirme sürümlerindeki kısıtlamalar"
description: "Bu konu standart maliyetler için maliyetlendirme sürümüne uygulanan kısıtlamaları açıklar."
author: AndersGirke
manager: AnnBe
ms.date: 01/17/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CostingVersion
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.industry: Manufacturing
ms.author: aevengir
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: e14d5d11e987d2dbc841f86c39fc7e94864144d3
ms.openlocfilehash: 658575492597eed91509561f4710f07e271c53c8
ms.contentlocale: tr-tr
ms.lasthandoff: 01/17/2018

---


#  <a name="restrictions-on-costing-versions-for-standard-costs"></a>Standart maliyetler için maliyetlendirme sürümlerindeki kısıtlamalar

[!include[banner](../includes/banner.md)]

Bu konu standart maliyetler için maliyetlendirme sürümüne uygulanan kısıtlamaları açıklar. 

Aşağıdaki kısıtlamalar, standart maliyetlendirme ilkelerine bağlı kalınmasını sağlamaya yardımcı olur:

-  Bir maddenin maliyetine giderler dahil edilmelidir. Üretilen bir maddenin giderleri ürün reçetesi ve rota bilgilerinde itfa edilmiş sabit maliyetleri temsil eder. Bu nedenle, giderler birim maliyete dahil edilmelidir. Satınalınan bir maddenin giderleri de maddenin birim maliyetine dahil edilir.

-  Üretilen maddelerin standart maliyetlerinin hesaplaması standart maliyetlere ilişkin bir maliyetlendirme sürümündeki maliyet kayıtlarını temel almalıdır. Alternatif maliyet verisi kaynakları yalnızca planlanan maliyetlere (örneğin satınalınan maddeler için satınalma fiyatı ticaret anlaşmaları) ait bir maliyetlendirme sürümüyle birlikte kullanılabilir. Alternatif maliyet verisi kaynakları ürün reçetesi hesaplama grubu tarafından tanımlanır.

-  Ürün reçetesi hesaplamaları tek düzeyli bir açılım moduyla yapılmalıdır.

Standart maliyetlerin madde maliyet verileri standart veya planlanan maliyetler içeren başka bir maliyet versiyonuna kopyalanabilir. Ancak planlanan maliyetlerin madde maliyet verileri standart maliyetler içeren başka bir maliyet versiyonuna kopyalanamaz çünkü bu bölümde daha önce listelenen kısıtlamalar planlanan maliyetler için geçerli olmayacaktır.

<a name="related-topics"></a>İlgili konular
--------

[Maliyetlendirme versiyonları](costing-versions.md)

[Standart maliyetleri imalat dışı bir ortamda güncelleme](update-standard-costs-non-manufacturing-environment.md)

[Üretilmiş maddeler için standart maliyetleri sürdürmeye hazırlanma](update-standard-costs-manufacturing-environment.md)


