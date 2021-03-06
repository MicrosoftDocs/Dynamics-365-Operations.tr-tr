---
title: Plana filtre uygulama
description: Bu konuda, Planlamayı En İyi Duruma Getirme işlevi kullanıldığında bir planda filtrelerin nasıl kullanılacağı açıklanmaktadır.
author: ChristianRytt
ms.date: 01/08/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: AX 10.0.5
ms.openlocfilehash: 7b605f9826d2116f6f52a4b880f4fb5bd24cfdd0
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/01/2021
ms.locfileid: "5813063"
---
# <a name="apply-filters-to-a-plan"></a>Plana filtre uygulama

[!include [banner](../../includes/banner.md)]

Planlamayı En İyi Duruma Getirme işlevi kullanıldığında plana bir filtre uygulayabilirsiniz. **Plan filtresi**, her zaman master planlama çalışması sırasında uygulanır. **Plan filtresi**, bir planı belirli bir madde grubuyla sınırlamak ve ortaya çıkan master planlamanın bir parçası olarak başka hiçbir maddenin dahil edilmediğinden emin olmak istediğinizde yararlıdır.

**Plan filtresi** uygulanırsa ve master planlama çalışması sırasında bir çalışma zamanı filtresi de uygulanırsa planlama çalışmasına yalnızca iki filtrenin kesişimi dahil edilir.

**Plan filtresi**, en iyi duruma getirme işlemi kullanılırken **ana planlardan** erişilebilir.

## <a name="example-scenario"></a>Örnek senaryo

A, B ve C maddelerini içeren bir plan filtresi ayarlanır. Ardından master planlama çalışmaları aynı plan için çalıştırılır ancak farklı çalışma zamanı filtreleri uygulanır:

- **D maddesini içeren çalışma zamanı filtresi:** Plan filtresi ile çalışma zamanı filtresi kesişmediğinden hiçbir madde planlanmaz.
- **A ve D maddelerini içeren çalışma zamanı filtresi:** D maddesi plan filtresinin parçası olmadığından yalnızca A maddesi planlama çalışmasına dahil edilir.
- **B maddesini içeren çalışma zamanı filtresi:** Yalnızca B maddesi planlama çalışmasına dahil edilir ve A maddesinin önceki planlama çıktısı tutulur.
- **Tüm maddeleri içeren çalışma zamanı filtresi (boş filtre):** A, B ve C maddeleri planlama çalışmasına dahil edilir ve A ve B maddelerinin önceki planlama çıktısı üzerine yazılır.

> [!NOTE]
> **Master planlama parametreleri** sayfasında **Geçerli dinamik master plan** olarak seçilen planda bir plan filtresi ayarlamaktan kaçınmanız gerekir. Aksi takdirde, dinamik master plan işlevleri filtrelenen maddelerle sınırlandırılır. Örneğin, net gereksinimler, plan filtresinin parçası olmayan bir madde için güncelleştirilirse hiçbir sonuç oluşturulmaz.

## <a name="related-resources"></a>İlgili kaynaklar

[Planlamayı En İyi Duruma Getirmeye genel bakış](planning-optimization-overview.md)

[Planlamayı En İyi Duruma Getirmeye başlayın](get-started.md)

[Planlamayı En İyi Duruma Getirme uygunluk analizi](planning-optimization-fit-analysis.md)

[Plan geçmişini ve planlama günlüklerini görüntüleme](plan-history-logs.md)

[Planlama işini iptal etme](cancel-planning-job.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]