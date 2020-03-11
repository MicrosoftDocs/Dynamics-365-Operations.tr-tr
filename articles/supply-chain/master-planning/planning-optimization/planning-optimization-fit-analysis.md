---
title: Planlamayı En İyi Duruma Getirme uygunluk analizi
description: Bu konuda, geçerli ayar ve verilerinizi Planlamayı En İyi Duruma Getirme işlevinin özelliklerine göre nasıl doğrulayacağınız açıklanmaktadır.
author: ChristianRytt
manager: AnnBe
ms.date: 10/30/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: AX 10.0.5
ms.openlocfilehash: 25f3b39d0e6e88eb3f042ab93773e9724528ab0f
ms.sourcegitcommit: a688c864fc609e35072ad8fd2c01d71f6a5ee7b9
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/20/2020
ms.locfileid: "3076190"
---
# <a name="planning-optimization-fit-analysis"></a>Planlamayı En İyi Duruma Getirme uygunluk analizi

[!include [banner](../../includes/preview-banner.md)]
[!include [banner](../../includes/banner.md)]

Geçerli ayar ve verilerinizin Planlamayı En İyi Duruma Getirme işleviyle nasıl uyumlu olduğunu görmek için **Master planlama** \> **Ayar** \> **Planlamayı En İyi Duruma Getirme uygunluk analizi** bölümüne gidin ve ardından **Analizi çalıştır**'ı seçin. Analizde tutarsızlıklar bulunursa bunlar aynı sayfada listelenir. (Analizin çalıştırılması birkaç dakika sürebilir.)

> [!NOTE]
> Tutarsızlıklar varsa yine de Planlamayı En İyi Duruma Getirmeye özelliğini kullanabilirsiniz. Uygunluk analizinin sonuçları yalnızca planlama servisinin geçerli ayarınızı dikkate almadığı yerleri gösterir. Başka bir deyişle, bazı işlemlerin yok sayılabileceği veya desteklenmeyebileceği yerleri gösterir.

## <a name="analysis-results-example-1"></a>Analiz sonuçları: Örnek 1

- **Özellik:** Üretim
- **Sorun:** Ürün reçetesi düzeyi sıfırdan büyük olan maddeler: 56
- **Açıklama:** Uygunluk analizi üretim için ürün reçetesi (BOM) ayarı olan 56 madde buldu. Planlamayı En İyi Duruma Getirme özelliğinin geçerli sürümü üretimi desteklemediğinden Planlamayı En İyi Duruma Getirme, planlı üretim emirleri yerine planlı satın alma emirleri oluşturur. Ayrıca etkilenen maddelerin listelendiği bir uyarı da gösterir.

### <a name="analysis-results-example-2"></a>Analiz sonuçları: Örnek 2

- **Özellik:** Eylemler
- **Sorun:** Eylem hesaplaması etkinleştirilen karşılama grupları: 6
- **Açıklama:** Uygunluk analizi, eylem hesaplamasının açık olduğu altı karşılama grubu buldu. Planlamayı En İyi Duruma Getirme özelliğinin geçerli sürümü eylemleri desteklemediğinden eylemler master planlama sırasında oluşturulur.

## <a name="related-resources"></a>İlgili kaynaklar

[Planlamayı En İyi Duruma Getirmeye genel bakış](planning-optimization-overview.md)

[Planlamayı En İyi Duruma Getirmeye başlayın](get-started.md)

[Plan geçmişini ve planlama günlüklerini görüntüleme](plan-history-logs.md)

[Plana filtre uygulama](plan-filters.md)

[Planlama işini iptal etme](cancel-planning-job.md)
