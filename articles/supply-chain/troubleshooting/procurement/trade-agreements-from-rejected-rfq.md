---
title: Ticari sözleşmeler, reddedilen RFQ'lardan oluşturulabiliyor
description: Ticari sözleşmeler, reddedilen RFQ'lardan oluşturulabilir. RFQ satırı kabul edilmediyse sistem, ticari sözleşme günlüklerinin oluşturulmasını engellemiyor
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
ms.openlocfilehash: de3011c6660b1cdccf94def32864316525adcde6
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/07/2021
ms.locfileid: "7477881"
---
# <a name="trade-agreements-can-be-created-from-rejected-rfqs"></a>Ticari sözleşmeler, reddedilen RFQ'lardan oluşturulabiliyor

## <a name="symptoms"></a>Belirtiler

Ticari sözleşmeler, reddedilen RFQ'lardan oluşturulabilir. Bu nedenle, RFQ satırı kabul edilmediyse, sistem ticari sözleşme günlüklerinin oluşturulmasını engellemez.

## <a name="resolution"></a>Çözüm

Bu, beklenen davranıştır. Kabul edilip edilmediğine bakılmaksızın, bir teklif talebi (RFQ) için herhangi bir yanıt için ticari sözleşmeler oluşturabilirsiniz. Daha fazla bilgi için bkz. [Teklif talebine (RFQ) genel bakış](/dynamics365/supply-chain/procurement/request-quotations.md).
