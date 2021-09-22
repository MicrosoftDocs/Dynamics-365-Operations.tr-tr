---
title: Tamamlandı bildirimi güncelleştirmesi eksik miktar hatasıyla başarısız oluyor
description: Süre veya malzeme miktarı yerine hata miktarını bildirirken bir üretim emrini sonlandırmayı denerseniz tamamlandı bildirimi güncelleştirmesi başarısız olur.
author: SmithaNataraj
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 7785549c47063727f2749749940c1a96a351e70f
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/07/2021
ms.locfileid: "7477819"
---
# <a name="report-as-finished-update-fails-with-a-missing-quantity-error"></a>Tamamlandı bildirimi güncelleştirmesi bir eksik miktar hatasıyla başarısız oluyor

## <a name="symptoms"></a>Belirtiler

Süre veya malzeme miktarını bildirirken değil hata miktarını bildirirken bir üretim emrini tamamlandı olarak bildirmeyi deniyorsunuz. Üretim emrini sonlandırmayı denediğinizde tamamlandı bildirimi güncelleştirmesi başarısız olur ve aşağıdaki hata iletisini alırsınız:

> Eksik tamamlandı bildirimi miktarı.

## <a name="resolution"></a>Çözüm

Üretim emrindeki hata miktarını bildirirseniz mal miktarını da bildirmeniz gerekir.
