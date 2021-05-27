---
title: Üretim emirleri bir toplu iş aracılığıyla sıfırlanırsa, geç seçim dikkate alınmaz
description: Bir üretim emrinin durumunu sıfırlamak için tekrarlayan bir toplu iş kullandığınızda, geç seçimler dikkate alınmaz.
author: johanhoffmann
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: ProdTableListPage
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: e53198f427f4060421a4f0078277682c43db1320
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026977"
---
# <a name="late-selection-isnt-respected-when-production-orders-are-reset-via-a-batch-job"></a>Üretim emirleri bir toplu iş aracılığıyla sıfırlanırsa, geç seçim dikkate alınmaz

KB numarası: 4614634

## <a name="symptoms"></a>Belirtiler

Bir üretim emrinin durumunu sıfırlamak için tekrarlayan bir toplu iş kullandığınızda, geç seçimler dikkate alınmaz.

## <a name="resolution"></a>Çözünürlük

Mevcut tasarım, *Durumu sıfırla* işlemi için geç seçimlerinin kullanımını desteklemiyor.
