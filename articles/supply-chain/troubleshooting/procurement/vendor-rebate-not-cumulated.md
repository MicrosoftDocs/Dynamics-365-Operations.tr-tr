---
title: Satıcı indirimi, faturalara dayalı olarak kümülatif değil
description: Satıcı indirimi, faturalara dayalı olarak kümülatif değil
author: kamaybac
ms.date: 05/31/2021
ms.topic: troubleshooting
ms.search.form: PurchTable, PurchTablePart, PurchRFQTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yanansong
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: 9d4596a7351969bf181982a24ea1dcc6f5732831
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/07/2021
ms.locfileid: "7477891"
---
# <a name="a-vendor-rebate-isnt-cumulated-based-on-invoices"></a>Satıcı indirimi, faturalara dayalı olarak kümülatif değil

## <a name="symptoms"></a>Belirtiler

Deftere nakledilen faturaların farklı vade tarihleri varsa, bu faturalar bunlardan oluşturulan satıcı indirimlerine yansıtılmazlar.

## <a name="resolution"></a>Çözüm

Satıcı indirimi hesaplanırken vade tarihi dikkate alınmaz. Sistemi, gerçek satıcı indirimi açısından faturadaki vade sonu ve ilgili ilişki daha belirgin olacak şekilde özelleştirmeyi düşünebilirsiniz.
