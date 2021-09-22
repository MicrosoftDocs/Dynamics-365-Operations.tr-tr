---
title: Otomatik rezervasyon istemi kullanılabilir stokla birlikte görüntülenir
description: Ambar işlemlerinin etkinleştirilmediği bir ambarda bir madde kullandığınızda otomatik rezervasyon istemi görüntülenir. Konumun üzerindeki tüm boyutları belirtin.
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: a15502ce8c5bc61d37cedd746985176408a2f362
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/07/2021
ms.locfileid: "7477885"
---
# <a name="auto-reservation-prompt-for-batch-number-is-shown-even-with-available-inventory"></a>Toplu iş numarası için otomatik rezervasyon istemi de kullanılabilir stokla birlikte görüntülenir

## <a name="symptoms"></a>Belirtiler

Ambar işlemlerini etkinleştirilmemiş bir ambarda *toplu iş üstü* rezervasyon hiyerarşisine sahip bir madde kullandığınızda ve otomatik rezervasyon etkinleştirildiğinde, malzeme çekme için yalnızca bir toplu iş olsa bile bir toplu iş numarası için otomatik rezervasyon istemi görüntülenir.

Ancak, ambar işlemlerinin etkinleştirildiği bir ambarda aynı maddeyi kullandığınızda, otomatik rezervasyon istemi gösterilmez.

## <a name="resolution"></a>Çözüm

Rezervasyon hiyerarşisi *toplu iş üstü* veya *seri üstü* olarak tanımlanmışsa, referansta bulunulan boyut (**toplu iş numarası** veya **seri numarası**) her zaman talep siparişlerinde belirtilmelidir. Tek bir toplu iş veya seri numarası varsa, ambar işlemleri bu bilgileri tamamlayabilirler. Ancak Ambar, ambar işlemleri için etkinleştirilmediğinden, kullanıcının her zaman **konumun** üzerindeki tüm boyutları belirtmesi gerekir.
