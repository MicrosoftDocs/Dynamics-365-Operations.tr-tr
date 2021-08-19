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
ms.openlocfilehash: 6b4361682246397732e8326b98b1b86ff878664e54c8c352296b0d7eaff6bbbd
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/05/2021
ms.locfileid: "6719563"
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
