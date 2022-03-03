---
title: Satış güncelleştirme geçmişi temizleme işi başarısız oluyor veya performans sorunları var
description: Büyük miktarda satış güncelleştirme verisi varsa, satış geçmişi temizleme toplu işi başarısız olabilir veya çok uzun sürebilir.
author: myvakalo
ms.date: 10/05/2021
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: myvakalo
ms.search.validFrom: 2021-09-29
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 371a8c7178cd7c5091d6dd9a91d0ee03b943a269
ms.sourcegitcommit: fcb8a3419e3597fe855cae9eb21333698518c2c7
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/09/2022
ms.locfileid: "8103200"
---
# <a name="sales-update-history-cleanup-job-fails-or-has-performance-issues"></a>Satış güncelleştirme geçmişi temizleme işi başarısız oluyor veya performans sorunları var

## <a name="symptoms"></a>Belirtiler

**Satış güncelleştirme geçmişi temizleme** işi başarısız oluyor veya performans sorunları var.  

## <a name="cause"></a>Nedeni

Sisteminizde çok sayıda satış güncelleştirmesi olduğunda bu durum ortaya çıkabilir ve bu büyük miktarda satış güncelleştirme verisine neden olabilir. Temizleme işi bu verilerin tümünü tek bir harekette temizlemeyi dener. Sonuç olarak, işin çalıştırılması uzun sürebilir, hatta başarısız olabilir.

## <a name="resolution"></a>Çözüm

Supply Chain Management sürüm 10.0.19 ve üstü için **satış güncelleştirme geçmişi temizleme** toplu işleminin yeni bir sürümü mevcut. Bu özellik, varsayılan olarak açık değildir. Nasıl çalıştığı ve özellik yönetiminde nasıl etkinleştirileceği ile ilgili ayrıntılar için bkz. [Satış geçmişi temizleme işlemi performans iyileştirmeleri](../../sales-marketing/sales-update-history-cleanup-performance-improvements.md).

