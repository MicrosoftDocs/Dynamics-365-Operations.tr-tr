---
title: 0,00 kullanılabildiğinden stok rezervasyonları yapılamıyor
description: Stokta yalnızca 0,00 kullanılabildiğinden sistemin rezervasyon yapamadığını belirten bir hata alırsınız. Bu sorun büyük olasılıkla açık olan bir iş nedeniyle oluşur.
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 75d72f7ee1bdecca5a087b75b1de9907b9d244ab
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/07/2021
ms.locfileid: "7477879"
---
# <a name="system-cant-make-reservations-because-000-are-available-in-the-inventory"></a>Sistem, stokta 0,00 kullanılabildiğinden rezervasyon yapamıyor

## <a name="symptoms"></a>Belirtiler

Bu sorun, belirtilen boyutlara sahip yeterli stok hareketi bulunmadığından, sistem bir stok miktarını güncelleştiremediği takdirde oluşabilir. Aşağıdaki hata iletisini alırsınız:

> Fiziksel eldeki miktar Tesis=%1, Ambar=%2, Stok durumu = Mevcut, Parti numarası=%3, Sahip=%4: Stokta yalnızca 0,00 mevcut olduğundan %5 ayrılamaz.

## <a name="resolution"></a>Çözüm

Bu sorun büyük olasılıkla açık olan bir iş nedeniyle oluşur. İşi tamamlayın ya da iş oluşturma işlemi olmadan alın. Hiçbir stok hareketinin fiziksel olarak miktar ayırmadığından emin olun. Örneğin, bu hareketler açık kalite emirleri, stok bloke kayıtları veya çıkış emirleri olabilir.
