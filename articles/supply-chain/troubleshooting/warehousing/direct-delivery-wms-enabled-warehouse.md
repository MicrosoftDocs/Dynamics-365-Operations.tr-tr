---
title: WMS özellikli ambar için doğrudan teslimat işlenemiyor
description: Ambarda WMS etkinse doğrudan teslimatı desteklemez. Doğrudan teslimi kullanmak için WMS harici bir madde ve ambar seçmelisiniz.
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 090e17091e9fb92c2065679bb9b04637214e2eea
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/07/2021
ms.locfileid: "7477900"
---
# <a name="direct-delivery-not-able-to-process-for-wms-enabled-warehouse"></a>WMS özellikli ambar için doğrudan teslimat işlenemiyor

## <a name="symptoms"></a>Belirtiler

Ambar yönetimi (WMS) için etkinleştirilen bir ambardan doğrudan teslim edilmek üzere bir satış satırına bir madde eklenirse satış satırı güncelleştirildiğinde aşağıdaki hata iletisini alırsınız:

> Ambar yönetimi etkinleştirilmiş olduğundan doğrudan teslimat %1 ambarı için işlenemiyor. Lütfen ambar yönetimi için etkinleştirilmemiş olan başka bir ambar belirtin.

## <a name="resolution"></a>Çözüm

Microsoft bu sorunu değerlendirmiş ve bir özellik sınırlaması olduğunu tespit etmiştir. Şu anda WMS doğrudan teslimi desteklemiyor. Bu nedenle, doğrudan teslimi kullanmak için WMS harici bir madde ve ambar seçmelisiniz.
