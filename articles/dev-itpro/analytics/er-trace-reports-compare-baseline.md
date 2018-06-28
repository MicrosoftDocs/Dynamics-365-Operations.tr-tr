---
title: "Oluşturulan rapor sonuçlarını izleme ve temel değerlerle karşılaştırma"
description: "Bu konu, oluşturulan ER raporlarının sonuçlarını temel rapor değerleriyle nasıl karşılaştıracağınız hakkında bilgi vermektedir."
author: NickSelin
manager: AnnBe
ms.date: 05/25/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 220314
ms.assetid: 2685df16-5ec8-4fd7-9495-c0f653e82567
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2018-04-01
ms.dyn365.ops.version: Release 8.0
ms.translationtype: HT
ms.sourcegitcommit: 2fc887668171175d436b9eb281a35c1c9d089591
ms.openlocfilehash: 1a598d0bd053c60c3f8df6b05ecb7ff15addfaa3
ms.contentlocale: tr-tr
ms.lasthandoff: 05/25/2018

---

# <a name="trace-generated-report-results-and-compare-them-with-baseline-values"></a>Oluşturulan rapor sonuçlarını izleme ve temel değerlerle karşılaştırma

[!include[banner](../includes/banner.md)]

Giden elektronik belgeler oluşturan ER biçimlerinin sonuçlarını izleyebilirsiniz. İzleme oluşturma açıldığı zaman (ER kullanıcı parametresi **Hata ayıklama modunda çalıştır**), her ER raporu çalıştırıldığında ER biçimi yürütme günlüğünde yeni bir izleme kaydı oluşturulur. Oluşturulan her izlemede aşağıdaki ayrıntılar depolanır:

- Doğrulama kurallarıyla oluşturulan tüm uyarılar
- Doğrulama kurallarıyla oluşturulan tüm hatalar 
- İzleme kaydının ekleri olarak depolanan tüm oluşturulan dosyalar

Her ER biçimi için ayrı ayrı temel uygulama dosyaları depolayabilirsiniz. Dosyalar, çalıştırılan raporların beklenen sonuçlarını açıklıyorsa temel dosya olarak nitelendirilir. İzleme oluşturma açıkken çalıştırılmış bir ER biçimine ilişkin bir temel dosya varsa, izleme, daha önce sözü edilen ayrıntıların yanı sıra, oluşturulan elektronik belgeyi temel dosyayla karşılaştırma sonucunu depolar. Oluşturulan elektronik belgeyi ve temel dosyasını tek tıklamayla bir zip dosyasına alabilirsiniz. Bunun ardından, Windiff gibi harici bir araç kullanarak ayrıntılı bir karşılaştırma yapabilirsiniz.

Oluşturulan elektronik belgelerde beklenen içeriğin olup olmadığını analiz etmek için izlemeyi değerlendirebilirsiniz. Kod tabanı değiştiği zaman bu değerlendirmeyi bir kullanıcı kabul testi (UAT) ortamında yapabilirsiniz (örneğin uygulamanın yeni bir örneğine geçtiğiniz, düzeltme paketleri yüklediğiniz veya kod değişiklikleri dağıttığınız zaman). Bu sayede, değerlendirmenin, kullanılan ER raporlarının yürütülmesini etkilemediğinden emin olabilirsiniz. Birçok ER raporu için, değerlendirme müdahalesiz modda yapılabilir.

Bu özellik hakkında daha fazla bilgi için, **7.5.4.3 BT hizmetlerini/çözümlerini test etme (10679)** iş sürecinin birer parçası olan ve [Microsoft Download Center](https://go.microsoft.com/fwlink/?linkid=874684)'dan indirilebilen **ER - Raporlar oluşturma ve sonuçları karşılaştırma (Bölüm 1)** ve **ER - Raporlar oluşturma ve sonuçları karşılaştırma (Bölüm 2)** görev kılavuzlarını oynatın. Bu görev kılavuzları, oluşturulan elektronik belgeleri değerlendirmek üzere temel dosyaları kullanmak için ER çerçevesini yapılandırma işleminde size yol gösterir.

