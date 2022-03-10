---
title: Master plan için parametreler yok
description: Planlı siparişi kesinleştirmeye çalıştığınızda, master plan için hiçbir parametre belirtilmediğini belirten bir hata iletisi alırsınız.
author: ankubik
ms.date: 06/10/2021
ms.topic: troubleshooting
ms.search.form: ReqTransPo
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: ankubik
ms.search.validFrom: 2021-06-10
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: d039b79684f87e7791fb9dae7cbdc6ced220bc092d9a0ab624616c1c345986da
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/05/2021
ms.locfileid: "6756787"
---
# <a name="parameters-for-the-master-plan-dont-exist"></a>Master plan için parametreler yok

Hata kodu: SYS25368

## <a name="symptoms"></a>Belirtiler

Planlı siparişi kesinleştirmeye çalıştığınızda aşağıdaki hata iletisini alırsınız:

> %1 master planına ait parametreler yok.

## <a name="cause"></a>Nedeni

Yapılandırma sorunları nedeniyle, sistem belirtilen planın ayarlarını bulamıyor.

## <a name="resolution"></a>Çözüm

- **Master planlama \> Kurulum \> Planlar \> Master planlar**'a gidin ve belirtilen ada sahip bir plan olduğundan emin olun.
