---
title: Erteleme deftere nakil yöntemleri
description: Bu makalede, abonelik faturalamasında gelir ve gider ertelemeleri için erteleme deftere nakil yöntemleri arasındaki farklar açıklanır.
author: JodiChristiansen
ms.date: 6/10/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 539093
ms.search.region: Global
ms.author: jchrist
ms.search.validFrom: 2021-11-05
ms.dyn365.ops.version: 10.0.24
ms.openlocfilehash: c66ed1c38251140dd798c39797873ceb5f7121a4
ms.sourcegitcommit: cfe8fbc202c3eb05d894076fdf99e46704f17365
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/15/2022
ms.locfileid: "9019107"
---
# <a name="deferral-posting-methods"></a>Erteleme deftere nakil yöntemleri

Bu makalede, abonelik faturalamasında gelir ve gider ertelemeleri için erteleme deftere nakil yöntemleri arasındaki farklar açıklanır.

**Gelir ve gider erteleme parametreleri** sayfasındaki erteleme deftere nakil yöntemi seçenekleri **Bilanço** ve **Kar ve zarar**'dır. Bu makaledeki örnekte, iki yöntem arasındaki farklar ve bir yöntemi ya da diğerini kullanmanın nedenleri açıklanacaktır.

**Bilanço** yöntemi yalnızca iki hesap kullanır. Bu nedenle, daha az kurulum söz konusudur. **Kar ve zarar** yönteminde, hareket türüne bağlı olarak gelir, iskontolar ve maliyetler için iki ek hesap (**İlk kabul** ve **Kabul mahsup**) yer alır. Bu hesaplar **Erteleme varsayılanları** sayfasında (**Abonelik faturalaması \> Gelir ve gider ertelemeleri \> Kurulum**) ayarlanır. Örnekte ertelenen gelire odaklanıldığı halde, aynı kavram ertelenmiş iskontolara ve ertelenmiş maliyetlere de uygulanabilir.

## <a name="example"></a>Örnek

Satış faturası 1, toplam 3.000 $'a ve ertelenen gelire sahiptir. Aşağıdaki tablolar, bu satış faturası deftere nakledilirken yapılan dağıtımları gösterir.

**Bilanço yöntemi**

| Türü | Hesap | Borç | Kredi|
|---|---|---|---|
| Borç | Alacak hesapları | 3,000.00 | |
| Kredi | Ertelenmiş gelir | | 3,000.00 |

**Kar ve zarar yöntemi**

| Türü | Hesap | Borç | Kredi |
|---|---|---|---|
| Borç | Alacak hesapları | 3,000.00 | |
| Borç | Gelir kabulü mahsup | 3,000.00 | |
| Kredi | Ertelenmiş gelir | | 3,000.00 |
| Kredi | İlk gelir kabulü | | 3,000.00 |

Satış faturası 2, toplam 2.000 $'a sahiptir ve ertelenen gelir yoktur.

| Türü | Hesap | Tutar |
|---|---|---|
| Borç | Alacak hesapları | 3,000.00 |
| Kredi | Gelir | 3,000.00 |

**Satış faturası 1 ve 2 birleştirildiğinde bilanço yöntemi toplamları**

| Hesap | Borç | Kredi |
|---|---|---|
| Alacak hesapları | 5,000.00 | |
| Gelir | | 2,000.00 |
| Ertelenmiş gelir | | 3,000.00 |

**Bilanço** yöntemi kullanıldığında, bir döneme ait brüt geliri görmek kolay değildir. Gelirin bir kısmı **Ertelenen gelir** hesabına nakledilir. Gelir her dönemde kabul edildiğinden, **Ertelenen gelir** hesabında birden çok borç ve alacak olduğunu unutmayın. Belirli bir döneme ait brüt gelir, gelir kabulünün ayrıntıları ile karıştırılır.

**Satış faturası 1 ve 2 birleştirildiğinde kar ve zarar yöntemi toplamları**

| Hesap | Borç | Kredi |
|---|---|---|
| Alacak hesapları | 5,000.00 | |
| Gelir | | 5,000.00 |
| Gelir mahsup | 3,000.00 | |
| Ertelenmiş gelir | | 3,000.00 |

Tüm gelir, kar ve zarar **Gelir** hesabına gider. Ertelenen gelir, kar ve zarar ekstresinden bilanço tablosuna taşınacaktır. Her şey **Gelir** hesabına nakledildiğinden, brüt geliri kolayca görebilirsiniz. Ancak, bu brüt gelirlerin bir kısmı ertelenir. Bu nedenle, **Ertelenen gelir** hesabına taşınır ve daha sonra kabul edilir.

**Kar ve zarar** yönteminde, **Gelir** hesabına ve **Gelir mahsup** hesabına bakarak, 5.000 $ brüt gelir ve 2.000 $ net gelir (ertelenen net tutar) görebilirsiniz. **Kar ve zarar** yöntemi raporlamayı kolaylaştırsa da bu yöntemde daha fazla hesap ayarlanması gerekir.
