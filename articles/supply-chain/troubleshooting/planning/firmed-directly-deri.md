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
ms.openlocfilehash: d20f1c1d6e8fc83dd996b04bf0321a41f7b39290f306d1ac9f4fcd17514832e6
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/05/2021
ms.locfileid: "6721187"
---
# <a name="directly-derived-firmed-orders-are-processed-by-an-in-review-workflow"></a>Doğrudan türetilen kesinleştirilmiş siparişler inceleme iş akışı tarafından işlenir

KB numarası: 4612450

## <a name="symptoms"></a>Belirtiler

Doğrudan türetilen kesinleştirilmiş siparişler, durumu *İncelemede* olan bir iş akışı tarafından işlenir.

## <a name="resolution"></a>Çözünürlük

Değişiklik izleme etkinleştirildiğinde, kesinleştirilmiş türetilmiş siparişlere (alt yüklenici satınalma siparişleri) *İncelemede* durumu atanır. Bu nedenle, bir satınalma siparişi türetilmişse (bir alt yüklenici satınalma siparişi), bu yalnızca bir iş akışına gönderilir. Satınalma siparişi, kesinleştirilmemiş bir planlı satınalma siparişiyse satınalma siparişi hala *Taslak* durumunda olduğu sürece planlama altyapısının yeni planlı siparişler oluşturmamasını sağlamak için otomatik olarak onaylanır.
