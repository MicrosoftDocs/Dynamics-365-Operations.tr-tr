---
title: Satış siparişi satırında stok rezervasyonu kaldırılamıyor
description: Satış satırı karşılığında açık iş varsa ve satırda stok rezervasyonunu kaldırmaya çalışıyorsanız bir hata alırsınız. Rezervasyonu boşaltmak için işi tamamlayın veya silin.
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 1a042065dc4cd637aff58e55cf16179b7022f6ca
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/07/2021
ms.locfileid: "7477857"
---
# <a name="cant-unreserve-inventory-on-a-sales-order-line"></a>Satış siparişi satırında stok rezervasyonu kaldırılamıyor

## <a name="symptoms"></a>Belirtiler

Satış siparişi satırı karşılığında açık iş varsa ve bu satırda stok rezervasyonunu kaldırmaya çalışıyorsanız aşağıdaki hata iletisini alırsınız:

> Rezervasyonlara dayanan iş oluşturulmuş olduğundan rezervasyonlar kaldırılamıyor.

## <a name="resolution"></a>Çözüm

Maddeyi bir paketleme istasyonundan başka bir konuma (*Baydoor* gibi) getirmek için açık paketleme grubu işinin bulunup bulunmadığını araştırın. Stok ayırma işlemini fiziksel olarak neyin yaptığını belirlemek için **İş oluşturma geçmişi günlüğü** ve **İş ayrıntıları** sayfalarındaki kayıtları gözden geçirin ve daha sonra ayırmayı geri almak için işi tamamlayın veya silin.
