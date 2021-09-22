---
title: Devam eden işler, son işte kısmi miktar bildirildiğinde sona eriyor
description: Üretim emrinin son işindeki kısmi miktarı raporlamak üzere iş kartı cihazı kullanılırsa Devam ediyor durumundaki önceki tüm işler sonlandırılır.
author: SmithaNataraj
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 11511d4ac7524facdd0d647e9bc38fe09c282be1
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/07/2021
ms.locfileid: "7477890"
---
# <a name="previous-in-progress-jobs-are-ended-when-reporting-partial-quantity-on-last-job"></a>Son işte kısmi miktar raporlanırken devam eden önceki işler sona eriyor

## <a name="symptoms"></a>Belirtiler

Üretim emrinin son işindeki kısmi miktarı raporlamak için iş kartı cihazı kullanılıyorsa o siparişteki Devam Ediyor durumundaki tüm önceki işler otomatik olarak sonlandırılır.

## <a name="resolution"></a>Çözüm

Bu davranış tasarımdan kaynaklanır. **Üretim emri varsayılanları** sayfasında, **Tamamlandı olarak bildir** sekmesinde, **Rotaya bitiş işareti yerleştir** adlı bir seçenek vardır. Bu seçenek *Evet* olarak ayarlanırsa bir çalışan son işlemi bildirmek üzere iş kartı cihazını veya iş kartı terminalini kullandığında rota kartı günlüğü deftere nakledilir. Bu günlük tüm işlemleri tamamlandı olarak işaretler ve tüm üretim işlerini sonlandırır. **Rotaya bitiş işareti yerleştir** seçeneği *Evet* olarak ayarlandığında sistem, çalışanın son işlemi bildirdiğinde seçtiği iş durumunu dikkate almaz. Sistem aynı zamanda çalışanın tam mı yoksa kısmi bir miktar mı bildirdiğini de dikkate almaz.
