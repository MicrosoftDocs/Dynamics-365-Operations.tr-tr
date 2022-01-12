---
title: Satış geçmişi temizleme işlemi performans iyileştirmeleri
description: Bu konu, satış geçmişi temizleme performans iyileştirmeleri özelliğini ve nasıl etkinleştirileceğini açıklar.
author: myvakalo
ms.date: 10/05/2021
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: myvakalo
ms.search.validFrom: 2021-09-29
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 610f0d4e0448dd21d10765400f25cd89e3c7a84b
ms.sourcegitcommit: 008779c530798f563fe216810d34b2d56f2c8d3c
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 12/14/2021
ms.locfileid: "7920285"
---
# <a name="sales-history-cleanup-performance-improvements"></a>Satış geçmişi temizleme işlemi performans iyileştirmeleri

[!include [banner](../includes/banner.md)]
[!INCLUDE [preview-banner](../includes/preview-banner.md)]
<!-- KFM: Preview until GA with 10.0.24 -->

**Satış güncelleme geçmişi temizleme** periyodik toplu iş, yüksek satış güncelleştirmeleri hacmine sahip ortamlarda seyrek çalıştırılırsa uzun sürebilir. Bu durumlarda, *Satış Geçmişi Temizleme performans iyileştirmeleri* özelliği çalışma süresinin azaltılmasına ve güvenilirliği artırmanıza yardımcı olur.

Özellik, varolan temizleme işini aşağıdaki yollarla geliştirir:

- Temizlemeyi toplu işlemlere böler (özelleştirmeler aracılığıyla toplu iş boyutunu değiştirebilirsiniz).
- En fazla 2 saat boyunca çalışacak (özelleştirmelerin süresini değiştirebilirsiniz).
- Mümkün olduğunda, kilitlemeyi en aza indirmek ve temizleme sırasında işlem tablolarını birleştirmekten kaçınmak için veritabanı yeteneklerinden yararlanılacaktır.

Özellik etkinleştirildikten sonra, **Satış güncelleştirme geçmişi temizliği** toplu işlemi (**Satış ve pazarlama \> dönemi görevleri \> Temizleme \> Satış güncelleme geçmiş temizleme**), daha önce olduğu gibi çalışacak, ancak daha iyi performans ve en fazla 2 saat boyunca çalışacaktır. Bu, belirli bir bekletme süresi çerçevesi için tüm verileri temizlemek amacıyla birkaç kez çalıştırılması gerekebilecek anlamına gelir.

## <a name="turn-on-the-sales-history-cleanup-performance-improvements-feature"></a>Satış geçmişi temizleme işlemi performans iyileştirmeleri özelliğini açma

Bu özelliği kullanabilmeniz için sisteminizde etkinleştirmeniz gerekir. Yöneticiler özellik durumunu denetlemek ve etkinleştirmek için [özellik yönetimi](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) ayarlarını kullanabilir. **Özellik yönetimi** çalışma alanındabu özellik aşağıdaki şekilde listelenir:

- **Model:** *Satış ve pazarlama*
- **Özellik adı:** *Satış geçmişi temizleme işlemi performans iyileştirmeleri*
