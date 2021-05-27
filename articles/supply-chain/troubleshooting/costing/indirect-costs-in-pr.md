---
title: İşlenen dolaylı maliyetler raporu, silinen üretim emirlerini içerir
description: İşlenen dolaylı maliyetler raporu, kısmen işlenmiş ve daha sonra silinen üretim emirleri hakkında bilgi sunar.
author: niwang
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: ProdIndirectCostInProgress
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 707fa9bb30129c3656e10c6756dee770a7712e65
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026984"
---
# <a name="the-indirect-costs-in-process-report-includes-deleted-production-orders"></a>İşlenen dolaylı maliyetler raporu, silinen üretim emirlerini içerir

KB numarası: 4612748

## <a name="symptoms"></a>Belirtiler

**İşlenen dolaylı maliyetler** raporu, kısmen işlenmiş ve daha sonra silinen üretim emirleri hakkında bilgi sunar.

## <a name="resolution"></a>Çözünürlük

Bir üretim emrini tersine çevirdiğinizde, aynı zamanda o üretim emrinin tüm hareketlerini de tersine çevirirsiniz. Üretim emrini sildiğinizde, alt genel muhasebe tabloları ve genel muhasebe ile ilişkili tüm hareketler korunur. Raporlar, alt genel muhasebe tablolarındaki hareketleri gösterir. Belirli üretim emri için net değerin 0,00 olması gerekir.
