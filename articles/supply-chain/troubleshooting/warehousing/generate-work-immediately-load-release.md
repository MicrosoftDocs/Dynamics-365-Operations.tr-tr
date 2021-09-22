---
title: Yük serbest bırakıldığında malzeme çekme işini hemen oluşturma
description: İşin yük serbest bırakıldığında hemen oluşturulması gerekiyorsa dalga şablonunu buna göre yapılandırmalısınız. Bu sayfada size adım adım yol gösterilmektedir.
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: fdeb0b27f4d2c1a2cc9f8e0c4ba537cdce604bd2
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/07/2021
ms.locfileid: "7477866"
---
# <a name="picking-work-isnt-generated-immediately-when-outbound-load-is-released"></a>Giden yük serbest bırakıldığında malzeme çekme işi hemen oluşturulmaz

## <a name="symptoms"></a>Belirtiler

Satış siparişi veya transfer emrini kullanarak giden yük oluşturur ve yükü ambarda serbest bırakırsınız. Ancak henüz bir malzeme çekme işinin oluşturulmadığına dikkat edin.

## <a name="resolution"></a>Çözüm

İşin yük serbest bırakıldığında hemen oluşturulması gerekiyorsa dalga şablonunu buna göre yapılandırmalısınız. Dalga şablonunda, aşağıdaki seçenekleri *Evet* olarak ayarlayın:

- Dalga oluşturmayı otomatik hale getir
- Dalgayı ambara serbest bırakma sırasında işle
- Dalga serbest bırakma işlemini otomatikleştir
