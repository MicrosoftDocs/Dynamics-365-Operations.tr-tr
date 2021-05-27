---
title: Negatif günler içinde bir satınalma varken planlı satınalma siparişi oluşturuluyor
description: Karşılama kodu Min/maks ise, satınalma işlemi negatif günler içinde olduğunda Planlama Optimizasyonu planlı bir satınalma siparişi oluşturur.
author: ChristianRytt
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: ReqTransPo,MpsIntegrationParameters
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: ilebedev
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 826496c2de956ff949dd79ab8aa643053719bf75
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026989"
---
# <a name="planned-purchase-order-is-created-when-a-purchase-exists-within-negative-days"></a>Negatif günler içinde bir satınalma varken planlı satınalma siparişi oluşturuluyor

KB numarası: 4614298

## <a name="symptoms"></a>Belirtiler

Karşılama kodu *Min/maks* ise, satınalma işlemi negatif günler içinde olduğunda Planlama Optimizasyonu planlı bir satınalma siparişi oluşturur.

## <a name="resolution"></a>Çözünürlük

Planlama Optimizasyonu, negatif günleri desteklemiyor. Ancak, her zaman planlı siparişlerin geçerli tarihe göre sağlama süresi içinde zamanlanmamasını sağlar. Örneğin, satınalma sağlama süresi 10 gün ve bir satınalma siparişinin bugünden itibaren sekiz gün sonra gelmesi bekleniyor. Bu durumda, satınalma siparişi bugünden beş gün sonra yapılacak bir talep için tedarik olarak kullanılır.

Bu nedenle, sağlama sürelerini senaryoların tümünü (veya neredeyse tümünü) kapsayacak şekilde ayarlamanızı öneririz.
