---
title: Sistem yöneticileri, yetkilendirilmedikleri için sipariş tutma bilgilerini temizleyemiyor
description: Sistem yöneticileri, yetkilendirilmedikleri için sipariş tutma bilgilerini temizleyemiyor.
author: SmithaNataraj
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: SalesTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 0d0fbcc111d77ae1a362984033216f5973e2bc74f2ee95947b662ef60a13d83e
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/05/2021
ms.locfileid: "6750918"
---
# <a name="system-administrators-cant-clear-order-holds-because-they-arent-authorized"></a>Sistem yöneticileri, yetkilendirilmedikleri için sipariş tutma bilgilerini temizleyemiyor

KB numarası: 4614642

## <a name="symptoms"></a>Belirtiler

Sistem yöneticileri sipariş tutma kodunda atanan belirli bir role sahip olmadıkça satış siparişi tutmalarını temizleyemez.

## <a name="resolution"></a>Çözünürlük

Satış siparişi tutmalarını temizleme gibi bazı işlemlere erişim, iş ilkesinin kurulumu tarafından belirlenir. Sistem yöneticilerinin bu tür işlemleri gerçekleştirmesine genelde izin verilmez. 

Daha çok, belirli bir görevi gerçekleştirmek için erişim iş ilkelerine göre yönetilir ve bu görevi gerçekleştirmek için yalnızca bir kuruluştaki belirli kişiler onaylanır. Örnek olarak, iş akışı onayları ve iş akışı yapılandırmasının sonucu olan belirli görevler sonucu olan iş akışı onayları gösterilebilir.

Sipariş tutmalarla ilişkilendirilmiş bir iş akışı olmasa da, ilke benzerdir. İlgili bir rol, kuruluştaki sipariş tutmaları temizleme yetkisine sahip belirli kişi gruplarını belirtir. Bu yetki, tanımlanmış işletme ilkesini ihlal ettiğinden tüm yöneticilere verilmemelidir.
