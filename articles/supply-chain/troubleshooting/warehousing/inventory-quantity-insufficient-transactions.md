---
title: Yetersiz hareketler nedeniyle stok miktarı güncelleştirilemiyor
description: Belirtilen boyutlara sahip %2 maddesi için yeterli stok hareketi bulunmadığından -1% stok miktarı güncelleştirilemiyor.
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 88130a969039dd741c8ea4fbaabe81acf0e6fb6a
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/07/2021
ms.locfileid: "7477799"
---
# <a name="system-cant-update-inventory-quantity-because-of-insufficient-transactions"></a>Sistem yetersiz hareketler nedeniyle stok miktarını güncelleştiremiyor

## <a name="symptoms"></a>Belirtiler

Bu sorun, belirtilen boyutlara sahip yeterli stok hareketi bulunmadığından, sistem bir stok miktarını güncelleştiremediği takdirde oluşabilir. Aşağıdaki hata iletisini alırsınız:

> %12 Lot Kimliği ve %11 başvuru kodu için boyutları Boyut=%3, Renk=%4, Ekler=%5, Tesis=%6, Ambar=%7, Konum=%8, Stok durumu=Mevcut, Plaka=%9, Parti numarası=%10 olan %2 maddesi için yeterli stok hareketi olmadığından %1 stok miktarı güncelleştirilemedi.

## <a name="resolution"></a>Çözüm

Hiçbir stok hareketinin fiziksel olarak miktar ayırmadığından emin olun. Örneğin, bu hareketler açık kalite emirleri, stok bloke kayıtları veya çıkış emirleri olabilir.
