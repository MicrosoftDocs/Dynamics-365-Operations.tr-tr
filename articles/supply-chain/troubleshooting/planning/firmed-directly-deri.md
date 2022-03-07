---
title: Doğrudan türetilen kesinleştirilmiş siparişler inceleme iş akışı tarafından işlenir
description: Doğrudan türetilen kesinleştirilmiş siparişler, durumu İncelemede olan bir iş akışı tarafından işlenir.
author: ChristianRytt
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: ReqTransPo
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: ilebedev
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: d54985707d82df2b947a7cb615fc25f90aa31702
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026991"
---
# <a name="directly-derived-firmed-orders-are-processed-by-an-in-review-workflow"></a>Doğrudan türetilen kesinleştirilmiş siparişler inceleme iş akışı tarafından işlenir

KB numarası: 4612450

## <a name="symptoms"></a>Belirtiler

Doğrudan türetilen kesinleştirilmiş siparişler, durumu *İncelemede* olan bir iş akışı tarafından işlenir.

## <a name="resolution"></a>Çözünürlük

Değişiklik izleme etkinleştirildiğinde, kesinleştirilmiş türetilmiş siparişlere (alt yüklenici satınalma siparişleri) *İncelemede* durumu atanır. Bu nedenle, bir satınalma siparişi türetilmişse (bir alt yüklenici satınalma siparişi), bu yalnızca bir iş akışına gönderilir. Satınalma siparişi, kesinleştirilmemiş bir planlı satınalma siparişiyse satınalma siparişi hala *Taslak* durumunda olduğu sürece planlama altyapısının yeni planlı siparişler oluşturmamasını sağlamak için otomatik olarak onaylanır.
