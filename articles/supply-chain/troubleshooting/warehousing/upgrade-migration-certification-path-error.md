---
title: WMS'ye yükseltirken veya geçerken sertifika yolu hatası
description: WMS'ye yükseltirken veya geçerken uygulamada "Sertifika yolu için güven çıpası bulunamadı" hatası gösteriliyorsa bu sayfa, sorunu düzeltme hakkında bilgi sağlamaktadır.
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 2cff41455268c43bdd99e285b9675f0c69be7de7
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/07/2021
ms.locfileid: "7477822"
---
 # <a name="trust-anchor-for-certification-path-not-found-when-updating-and-migrating-to-wms"></a>WMS'ye yükseltirken ve geçerken sertifika yolu için güven çıpası bulunamadı

## <a name="symptoms"></a>Belirtiler

Gelişmiş ambar yönetimine (WMS) yükseltirken ve geçerken Warehouse Management uygulamasında aşağıdaki hata iletisini görebilirsiniz:

> java.security.cert.certPathValidatorException: Sertifika yolu için güven çıpası bulunamadı.

## <a name="cause"></a>Nedeni

Bu, otomatik olarak imzalanan sertifikalara şirket içi ortamlarda Android 8+ sistemlerde güvenilmediğinden gerçekleşir.

## <a name="resolution"></a>Çözüm

Harici (ortak) bir sertifika yetkilisi (CA) kullanın. Bu sorunla ilgili düzeltme, Warehouse Management uygulamasının 1.9.0.0 sürümünde kullanıma sunulmuştur. Bu sorun ve nasıl düzeltileceği hakkında daha fazla bilgi için bkz. [Uygulama bağlantısı ayarlanırken sertifika yolu için güven çıpası bulunamadı](certification-path-app-connection-error.md).
