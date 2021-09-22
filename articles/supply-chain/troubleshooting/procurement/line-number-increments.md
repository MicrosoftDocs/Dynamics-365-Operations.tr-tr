---
title: İçeri aktarılan satınalma siparişlerinde yanlış satır numaraları gösteriliyor
description: Satınalma siparişleri veri yönetimi aracılığıyla içeri aktarıldığında satınalma siparişi satır numaraları sistem parametrelerinde tanımlanan artışı izlemiyor
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
ms.openlocfilehash: e1cf5cf1d04824213f495ac3ebf556796c96611a
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/07/2021
ms.locfileid: "7477803"
---
# <a name="imported-purchase-orders-show-incorrect-line-numbers"></a>İçeri aktarılan satınalma siparişlerinde yanlış satır numaraları gösteriliyor

## <a name="symptoms"></a>Belirtiler

Varsayılan olarak, *Satınalma siparişi satırları V2* veri varlığı aracılığıyla içe aktarılan satınalma siparişi satırları için otomatik olarak oluşturulan satır numaraları sistem parametrelerinde belirtilen sistem satır numarası artışını kullanmaz. El ile bir satınalma siparişi oluşturur ve kullanıcı arabirimiyle (UI) satır eklerseniz, satır numaraları doğru şekilde artırılır. Ancak veri yönetimi çerçevesi (DMF) kullanıyorsanız doğru şekilde arttırılmazlar.

Bu sorun; satırları DMF ile içe aktardığınızda, içe aktarılan varlıkta satır numaraları atanmış değilse, sistem bu dosyaları atamak için DMF yöntemini kullandığı için oluşur. Bu yöntem satır numaralarını her zaman bir sayı kadar arttırır.

## <a name="workaround"></a>Geçici çözüm

Satınalma siparişi satırlarını içe aktardığınızda, gerekli satır numaralarının veri varlığı satır numarası alanlarında zaten verildiğinden emin olun. Bu durumda, DMF satır numaralarının üzerine yazmaz.
