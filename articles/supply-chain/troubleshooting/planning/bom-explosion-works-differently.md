---
title: Ürün reçetesi açılımı kesinleştirilmiş ve tahmini üretim emirleri için farklı şekilde davranıyor
description: Ürün reçetesi açılımı, kesinleştirilen üretim emirleri için ve el ile oluşturulmuş iş için tahmini üretim emirlerinde farklı şekilde davranıyor
author: ChristianRytt
ms.date: 05/31/2021
ms.topic: troubleshooting
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: 94d4b00ea30396923a61b2748cf1aaeedc0af8af
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/07/2021
ms.locfileid: "7477845"
---
# <a name="bom-explosion-behaves-differently-for-firmed-and-estimated-production-orders"></a>Ürün reçetesi açılımı kesinleştirilmiş ve tahmini üretim emirleri için farklı şekilde davranıyor

## <a name="symptoms"></a>Belirtiler

Bir üretim emri kesinleştirildiğinde, ürün reçetesini açtığınızda maddeler açılmaz. Ancak, bir iş emrini el ile oluşturduğunuzda ve üretim emrini tahmin ettiğinizde, maddeler açılır.

### <a name="resolution"></a>Çözüm

Üretim emri kesinleştirildiğinde gerçekleşen açılım, planlı siparişi işaret eder ancak bu durumda planlı sipariş kesinleştirilmiş olduğu görünmüyor. Ancak üretim emri tahmin edildiyse açılım, planlanmış sipariş bulunmayan serbest bırakılmış üretim emrinden tetiklenir.
