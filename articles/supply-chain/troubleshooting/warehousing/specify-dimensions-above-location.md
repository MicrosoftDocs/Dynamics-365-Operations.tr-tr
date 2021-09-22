---
title: Toplu iş üstü hiyerarşisi olan kısmi miktar için yük serbest bırakılamıyor
description: Toplu iş üstü rezervasyon hiyerarşisi olan bir maddeyi kullanırken yük satırlarının, tahsis edilecek stok için siparişte konum üzerindeki boyutları belirtmesi gerekir.
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: eb7e71cc271903cb689c33777b72862246f2dd42
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/07/2021
ms.locfileid: "7477823"
---
# <a name="cant-release-a-load-for-partial-quantity-with-batch-above-reservation-hierarchy"></a>Toplu iş üstü rezervasyon hiyerarşisi olan kısmi miktar için yük serbest bırakılamıyor

## <a name="symptoms"></a>Belirtiler

*Toplu iş üstü* rezervasyon hiyerarşisine sahip bir madde kullandığınızda Kısmi bir miktar için Yük serbest bırakmaya çalışıyorsanız **Yük planlama çalışma ekranı** sayfasındaki **Ambara serbest bırak** komutu çalışmaz. Aşağıdaki hata iletisini alırsınız:

> Dalgaya atanması için yük satırlarının konum üzerindeki boyutları belirtmesi gerekir. Bu boyutları atamak için yük satırını rezerve edin ve yeniden oluşturun.

Ancak, *toplu iş altı* ayırma hiyerarşisine sahip bir madde kullandığınızda **Yük planlama çalışma ekranı sayfasından** kısmi bir miktar için bir yükü serbest bırakabilirsiniz.

## <a name="cause"></a>Nedeni

Boyut, Ayırma hiyerarşisindeki **Konum** boyutunun üzerinde olduğunda ambara serbest bırakma işlemi öncesinde belirtilmelidir. Yalnızca konum üstü boyutta yer yoksa, stok başarıyla tahsis edilebilir.

## <a name="resolution"></a>Çözüm

Yük satırını rezerve edip yeniden oluşturarak **Konum** üzerindeki tüm boyutların atandığından emin olun.
