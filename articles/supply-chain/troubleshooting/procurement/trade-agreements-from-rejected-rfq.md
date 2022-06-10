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
ms.openlocfilehash: 92731f0f56e6eba05043403c121939accbe26c05
ms.sourcegitcommit: 220101d2511a3164572226294ef090a43a1e6cdd
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/23/2022
ms.locfileid: "8789254"
---
# <a name="trade-agreements-can-be-created-from-rejected-rfqs"></a>Ticari sözleşmeler, reddedilen RFQ'lardan oluşturulabiliyor

## <a name="symptoms"></a>Belirtiler

Ticari sözleşmeler, reddedilen RFQ'lardan oluşturulabilir. Bu nedenle, RFQ satırı kabul edilmediyse, sistem ticari sözleşme günlüklerinin oluşturulmasını engellemez.

## <a name="resolution"></a>Çözüm

Bu, beklenen davranıştır. Kabul edilip edilmediğine bakılmaksızın, bir teklif talebi (RFQ) için herhangi bir yanıt için ticari sözleşmeler oluşturabilirsiniz. Daha fazla bilgi için bkz. [Teklif talebine (RFQ) genel bakış](/dynamics365/supply-chain/procurement/request-quotations).
