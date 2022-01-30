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
ms.openlocfilehash: 3c8ad7b0bd46c49fc989be091f44630a6a3eebc1
ms.sourcegitcommit: 3754d916799595eb611ceabe45a52c6280a98992
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/15/2022
ms.locfileid: "7985923"
---
# <a name="sales-history-cleanup-performance-improvements"></a>Satış geçmişi temizleme işlemi performans iyileştirmeleri

[!include [banner](../includes/banner.md)]

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
