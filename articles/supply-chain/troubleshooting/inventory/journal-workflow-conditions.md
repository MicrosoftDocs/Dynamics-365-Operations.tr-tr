---
title: Stok günlüğü iş akışı koşulları, satır düzeyinde değil günlük düzeyinde uygulanıyor
description: Stok günlüğü iş akışı koşulları, satır düzeyinde değil yalnızca günlük düzeyinde uygulanıyor.
author: sherry-zheng
ms.date: 05/31/2021
ms.topic: troubleshooting
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.16
ms.openlocfilehash: 46bdde7f09c639fbefd46162431762b056d521ae
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/07/2021
ms.locfileid: "7477847"
---
# <a name="inventory-journal-workflow-conditions-apply-at-the-journal-level-not-line-level"></a>Stok günlüğü iş akışı koşulları, satır düzeyinde değil günlük düzeyinde uygulanıyor

## <a name="symptoms"></a>Belirtiler

Bu sorunla, maliyet tutarında stok günlüğü iş akışı koşulu ayarlamaya çalışmanız gibi durumlarda karşılaşabilirsiniz. 1. adımın yalnızca maliyet tutarı 100'den az olduğunda çalışması için bir koşul ayarlarsınız. Ardından 2. adımın yalnızca maliyet tutarı 100'e eşit veya daha fazla olduğunda çalışması için başka bir koşul daha ayarlarsınız. Ardından, iş akışı çalıştırıldığında iş akışı geçmişinde yalnızca tek satır gösterilir ve gönderilen değere bakılmaksızın, her zaman ilk koşul *true* olarak değerlendirilir.

## <a name="workaround"></a>Geçici çözüm

Geçerli sürümde, stok günlüğü iş akışı koşulları, satır düzeyinde değil, yalnızca günlük düzeyinde uyglanır. Bu davranış tasarımdan kaynaklanır. Koşul ölçütlerinizi yalnızca günlük düzeyi özniteliklerinde ayarlamanızı öneririz.
