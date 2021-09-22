---
title: Teslimat notu düzeltmesi işlenemiyor
description: Teslimat notunu gönderilmesinin ardından düzeltmeye çalışırsanız bir hata alırsınız. Bu sayfada, WMS için etkinleştirilen maddelerdeki gönderilen sevk irsaliyelerinin nasıl düzeltileceği açıklanmaktadır.
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: bb0d827adff8abd8762bf2de844cad5574628e4b
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/07/2021
ms.locfileid: "7477874"
---
# <a name="delivery-note-correction-cant-be-processed"></a>Teslimat notu düzeltmesi işlenemiyor

## <a name="symptoms"></a>Belirtiler

Teslim notunu deftere naklettikten sonra iptal edemezsiniz çünkü **İptal** düğmesi kullanılamaz. Teslim notunu da düzeltemiyorsunuz. Bunu denerseniz aşağıdaki hata iletisini alırsınız:

> Teslimat notu düzeltmesi işlenemiyor. Teslimat notu, yalnızca ambar yönetimi işlemlerine tabi olan maddeleri içerir çünkü bunlar Teslimat Notu düzeltmesi tarafından desteklenmez.

## <a name="resolution"></a>Çözüm

Gelişmiş ambar yönetimi (WMS) için etkinleştirilen maddelere ait deftere nakledilen sevk irsaliyelerini düzeltmek için deftere nakletme işlemini doğrudan siparişten değil, yükten yapmanız gerekir.
