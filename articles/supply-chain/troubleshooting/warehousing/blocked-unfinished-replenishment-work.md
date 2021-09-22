---
title: Bitmemiş stok yenileme işi nedeniyle malzeme çekme işi engellendi
description: Bağımlı stok yenileme işi nedeniyle malzeme çekme işi engellenebilir. Stok yenileme işini tamamlayın ve ardından malzeme çekme işini işleyin.
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 53b50d1e3e2d7bb64e78514affe80076ddcb9052
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/07/2021
ms.locfileid: "7477894"
---
# <a name="picking-work-cant-be-unblocked-because-of-unfinished-replenishment-work"></a>Bitmemiş stok yenileme işi nedeniyle malzeme çekme işi engellenemiyor

## <a name="symptoms"></a>Belirtiler

Dalga talep stok yenilemesini kullanırken bağımlı stok yenileme işi nedeniyle malzeme çekme işi engellenebilir. Kaynak sipariş talebini yerine getirmek için bir malzeme çekme konumunda stokun yenilenmesi gerekiyorsa sistem hem stok yenileme işini hem de malzeme çekme işini oluşturur. Ancak bu, stok yenileme işi tamamlanana kadar malzeme çekme işini engeller ve aşağıdaki hata iletisini alırsınız:

> Tamamlanmamış stok yenileme işi olduğundan %1 işinin engeli kaldırılamıyor.

## <a name="resolution"></a>Çözüm

Bu davranış kasıtlı yapılır çünkü stok yenileme işi tamamlanana kadar malzeme çekme konumunda stok yeterli olmaz. Stok yenileme işini tamamlayın ve ardından malzeme çekme işini işleyin.
