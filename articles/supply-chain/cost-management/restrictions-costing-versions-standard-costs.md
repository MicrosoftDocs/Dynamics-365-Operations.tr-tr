---
title: Standart maliyetler için maliyetlendirme sürümlerindeki kısıtlamalar
description: Bu konu standart maliyetler için maliyetlendirme sürümüne uygulanan kısıtlamaları açıklar.
author: AndersGirke
manager: AnnBe
ms.date: 01/17/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CostingVersion
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.industry: Manufacturing
ms.author: aevengir
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 484471c6bbda1d7396dfcfa34c33f50d247dad98
ms.sourcegitcommit: 57bc7e17682e2edb5e1766496b7a22f4621819dd
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/18/2019
ms.locfileid: "2812684"
---
#  <a name="restrictions-on-costing-versions-for-standard-costs"></a>Standart maliyetler için maliyetlendirme sürümlerindeki kısıtlamalar

[!include [banner](../includes/banner.md)]

Bu konu standart maliyetler için maliyetlendirme sürümüne uygulanan kısıtlamaları açıklar. 

Aşağıdaki kısıtlamalar, standart maliyetlendirme ilkelerine bağlı kalınmasını sağlamaya yardımcı olur:

-  Bir maddenin maliyetine giderler dahil edilmelidir. Üretilen bir maddenin giderleri ürün reçetesi ve rota bilgilerinde itfa edilmiş sabit maliyetleri temsil eder. Bu nedenle, giderler birim maliyete dahil edilmelidir. Satınalınan bir maddenin giderleri de maddenin birim maliyetine dahil edilir.

-  Üretilen maddelerin standart maliyetlerinin hesaplaması standart maliyetlere ilişkin bir maliyetlendirme sürümündeki maliyet kayıtlarını temel almalıdır. Alternatif maliyet verisi kaynakları yalnızca planlanan maliyetlere (örneğin satınalınan maddeler için satınalma fiyatı ticaret anlaşmaları) ait bir maliyetlendirme sürümüyle birlikte kullanılabilir. Alternatif maliyet verisi kaynakları ürün reçetesi hesaplama grubu tarafından tanımlanır.

-  Ürün reçetesi hesaplamaları tek düzeyli bir açılım moduyla yapılmalıdır.

Standart maliyetlerin madde maliyet verileri standart veya planlanan maliyetler içeren başka bir maliyet versiyonuna kopyalanabilir. Ancak planlanan maliyetlerin madde maliyet verileri standart maliyetler içeren başka bir maliyet versiyonuna kopyalanamaz çünkü bu bölümde daha önce listelenen kısıtlamalar planlanan maliyetler için geçerli olmayacaktır.

<a name="related-topics"></a>İlgili konular
--------

[Maliyetlendirme sürümlerine genel bakış](costing-versions.md)

[İmalat dışı bir ortamda standart maliyetleri güncelleştirme](update-standard-costs-non-manufacturing-environment.md)

[Üretilmiş maddeler için standart maliyetleri sürdürmeye hazırlanma](update-standard-costs-manufacturing-environment.md)

