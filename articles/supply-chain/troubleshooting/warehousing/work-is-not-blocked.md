---
title: Çalışma durdurulmadı
description: Çalışma durdurulmamış
author: perlynne
ms.date: 04/15/2021
ms.topic: troubleshooting
ms.search.form: WHSWorkTable_WHSWorkUnblocking
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-05-15
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: d64ab282972e46e8857581b59e5705dd15667328
ms.sourcegitcommit: 5f5afb46431e1abd8fb6e92e0189914b598dc7fd
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2021
ms.locfileid: "5924216"
---
# <a name="work-isnt-blocked"></a>Çalışma durdurulmamış

Hata kodu: WHSUnblockNotBlockedWorkErrorMessage

## <a name="symptoms"></a>Belirtiler

Sistem, aşağıdaki hata iletisini gösterir:

> %1 koduna sahip çalışma durdurulmadı.

## <a name="cause"></a>Nedeni

Dalgadaki, **Dalga durduruldu** seçeneği *Hayır* olarak ayarlı. İşin durdurulması, iş durdurulmuş olmadığından kaldırılamıyor.

## <a name="resolution"></a>Çözünürlük

 Yalnızca **Dalga durduruldu** seçeneğinin *Evet* olarak ayarlandığı işlerin durdurulması kaldırılabilir.
