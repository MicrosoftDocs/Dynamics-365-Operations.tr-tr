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
ms.openlocfilehash: 563ac90dc8c037066b8ccd6d8986e089a66245af
ms.sourcegitcommit: 42bd701179e664947b6eafcd1804c83a5e64abcb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2021
ms.locfileid: "7641488"
---
# <a name="saleshistorycleanupperformanceimprovements"></a>Satış geçmişi temizleme işlemi performans iyileştirmeleri

[!include [banner](../includes/banner.md)]
[!INCLUDE [preview-banner](../includes/preview-banner.md)]

**Satış güncelleme geçmişi temizleme** periyodik toplu iş, yüksek satış güncelleştirmeleri hacmine sahip ortamlarda seyrek çalıştırılırsa uzun sürebilir. Bu durumlarda, *Satış Geçmişi Temizleme performans iyileştirmeleri* özelliği çalışma süresinin azaltılmasına ve güvenilirliği artırmanıza yardımcı olur.

Özellik, varolan temizleme işini aşağıdaki yollarla geliştirir:

- Temizlemeyi toplu işlemlere böler (özelleştirmeler aracılığıyla toplu iş boyutunu değiştirebilirsiniz).
- En fazla 2 saat boyunca çalışacak (özelleştirmelerin süresini değiştirebilirsiniz).
- Mümkün olduğunda, kilitlemeyi en aza indirmek ve temizleme sırasında işlem tablolarını birleştirmekten kaçınmak için veritabanı yeteneklerinden yararlanılacaktır.

Özellik etkinleştirildikten sonra, **Satış güncelleştirme geçmişi temizliği** toplu işlemi (**Satış ve pazarlama \> dönemi görevleri \> Temizleme \> Satış güncelleme geçmiş temizleme**), daha önce olduğu gibi çalışacak, ancak daha iyi performans ve en fazla 2 saat boyunca çalışacaktır. Bu, belirli bir bekletme süresi çerçevesi için tüm verileri temizlemek amacıyla birkaç kez çalıştırılması gerekebilecek anlamına gelir.

## <a name="turn-on-the-saleshistorycleanupperformanceimprovements-feature"></a>Satış geçmişi temizleme işlemi performans iyileştirmeleri özelliğini aç

Bu özelliği kullanabilmeniz için sisteminizde etkinleştirmeniz gerekir. Yöneticiler özellik durumunu denetlemek ve etkinleştirmek için [özellik yönetimi](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) ayarlarını kullanabilir. **Özellik yönetimi** çalışma alanındabu özellik aşağıdaki şekilde listelenir:

- **Model:** *Satış ve pazarlama*
- **Özellik adı:** *Satış geçmişi temizleme işlemi performans iyileştirmeleri*
