---
title: Malzeme çekme listesi kaydı sırasında konum seçildiğinde hata oluşur
description: Malzeme çekme listesi kaydı sırasında konum seçildiğinde hata oluşur.
author: perlynne
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: WMSPickingRegistration
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: b7fc579821f9a80d94aea949fcc0301b9d8f6935
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026967"
---
# <a name="an-error-occurs-when-the-location-is-selected-during-picking-list-registration"></a>Malzeme çekme listesi kaydı sırasında konum seçildiğinde hata oluşur

KB numarası: 4613106

## <a name="symptoms"></a>Belirtiler

Bu sorun, sisteminiz satış siparişlerini otomatik olarak rezerve etmek üzere yapılandırıldığında oluşur. Malzeme çekme listesi kayıt satırının konumunu seçmeyi denerseniz, ambar yönetimi (WMS) rezervasyon işlemlerini kullandığınızda aşağıdaki hata iletisini alırsınız:

> Miktar, yeni boyutlarla güncelleştirilemiyor

Belirtilen bir konumda yeterli eldeki stok olmadığı için bu sorun oluşabilir.

## <a name="resolution"></a>Çözünürlük

Sistem, beklendiği şekilde davranıyordur.

Ambar düzeyinde rezervasyon işlemini kullandığınız senaryolarda, eldeki stok tüm stok boyutları için rezerve edilemez ve belirtilen bir konumda eldeki stokta yeterli değilse, malzeme çekme satırından el ile rezervasyon işlemini kullanmanızı öneririz. Daha sonra, mevcut eldeki miktarların tümü için konum gibi alt rezervasyonları dağıtmak amacıyla *Lot rezerve et* işlevini kullanabilirsiniz.
