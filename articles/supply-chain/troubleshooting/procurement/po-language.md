---
title: Satınalma siparişleri tüzel kişiliğin dil ayarlarını yansıtmıyor
description: Satınalma siparişindeki ürün adı, satınalma siparişinin oluşturulduğu tüzel kişilik için ayarlanmış dil yerine sistem dilinde gösterilir
author: kamaybac
ms.date: 05/31/2021
ms.topic: troubleshooting
ms.search.form: PurchTable, PurchTablePart
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yanansong
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: 4deec493b5480dc570ac82876243bc31a2ae87aa
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/07/2021
ms.locfileid: "7477837"
---
# <a name="purchase-orders-dont-reflect-the-language-settings-of-the-legal-entity"></a>Satınalma siparişleri tüzel kişiliğin dil ayarlarını yansıtmıyor


## <a name="symptoms"></a>Belirtiler

Satın alma siparişindeki ürün adı, satınalma siparişinin oluşturulduğu yasal varlık için ayarlanmış dil yerine sistem dilinde gösterilir.

## <a name="reproduce-the-issue"></a>Sorunu yeniden oluşturma

Aşağıdaki yordamda, bu sorunu yeniden oluşturmanın bir yolu gösterilmektedir.

1. Sistem dilini *en-US* (ABD İngilizcesi) olarak ayarlayın.
1. Ürün adı çevirileri için *EN-US* ve *DE* (Almanca) dillerinin tutulduğu bir ürün bulunduğundan emin olun.
1. Geçerli bir varlığın dilini de *DE* olarak değiştirin.
1. *DE* dilinin ayarlandığı yasal varlıkta, ürünü içeren bir satınalma siparişi oluşturun.
1. Ürün adının ABD İngilizcesinde (sistem dili) gösterildiğine dikkat edin.

## <a name="resolution"></a>Çözüm

Bu davranış tasarımdan kaynaklanır. Satınalma siparişlerinde, ürün her zaman sistem dilinde gösterilir. Bir onay günlüğü oluşturulduğunda satınalma siparişi dili kullanılır.
