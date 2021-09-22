---
title: Stok kapanışı sırasında geriye dönük maliyet hesaplaması hatası
description: Önceki sürümlerde, stok kapanışı sırasında geriye dönük maliyet hesaplaması hatası almış olabilirsiniz. Bu sorun giderilmiştir.
author: SmithaNataraj
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: ae92b7121998d6b1ba2f08ea5736c55637867fbf
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/07/2021
ms.locfileid: "7477833"
---
# <a name="backflush-costing-calculation-error-during-inventory-closing"></a>Stok kapanışı sırasında geriye dönük maliyet hesaplaması hatası

## <a name="symptoms"></a>Belirtiler

10.0.13 öncesi sürümlerde, stok kapatma sırasında aşağıdaki hatalı uyarı iletisini alırsınız:

> Bir stok kapanışını bir %1 tarihiyle yürütmek üzeresiniz. Bir %1 tarihi eşleştirme dönemi sonuyla hiçbir geriye dönük maliyet hesaplama yürütmesi kaydedilmedi. Bir %1 tarihi eşleştirme dönemi sonuyla bir geriye dönük maliyet hesaplaması yürütmeyi unutmayın. Stok değerlemesi, satılan malların maliyeti ve farklar, bu işlem yürütülünceye kadar Yardımcı Kayıt Defteri veya Genel Kayıt Defteri'nde doğru olmayabilir.

## <a name="resolution"></a>Çözüm

Bu sorun 10.0.13 ve sonraki sürümlerde giderilmiştir. Daha fazla bilgi için bkz. [KB 4582468](https://fix.lcs.dynamics.com/Issue/Details?kb=4582468&bugId=468844&dbType=3&qc=fcd64080446a27382cfde3e4c3bdcfb714279185932259cd11ceb0d500617296).
