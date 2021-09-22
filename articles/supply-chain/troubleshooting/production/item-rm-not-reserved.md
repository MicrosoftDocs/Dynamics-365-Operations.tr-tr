---
title: Üretim emri serbest bırakıldığında RM maddesi rezerve edilemiyor
description: 'Üretim emrini serbest bırakırken şu hatayı alabilirsiniz: "RM maddesi tam olarak rezerve edilemiyor." Tam miktarın kullanılabilir olduğundan emin olun veya maddeleri el ile rezerve edin.'
author: SmithaNataraj
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 528895252d661bb012f49190c15853989833064d
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/07/2021
ms.locfileid: "7477875"
---
# <a name="item-rm-cant-be-fully-reserved-when-a-production-order-is-released"></a>Üretim emri serbest bırakıldığında RM maddesi tam olarak rezerve edilemiyor

## <a name="symptoms"></a>Belirtiler

Üretim emri ambara serbest bırakıldığında tüm ürün reçetesi satır öğeleri fiziksel olarak kullanılamıyorsa ve **Ambara serbest bırakma** ilkesi *Tam ayırma gerekli* olarak ayarlanmışsa aşağıdaki hata iletisini alırsınız:

> RM maddesi tam olarak ayrılmadı. Tam miktarın kullanılabilir olduğundan emin olun veya ürün reçetesi satırındaki Ayırma alanı El İle veya Başlatıldı olarak ayarlanmışsa maddeleri el ile ayırın. Bazı malzemeler rezerve edilemediğinden sipariş ambara serbest bırakılamadı.

## <a name="resolution"></a>Çözüm

Bu davranış tasarım gereğidir ve beklendiği gibi çalışmaktadır. Bu sorunu gidermek için hata iletisinde sağlanan yönergeyi izleyin: "Tam miktarın kullanılabilir olduğundan emin olun veya ürün reçetesi satırındaki Ayırma alanı El İle veya Başlatıldı olarak ayarlanmışsa maddeleri el ile ayırın."
