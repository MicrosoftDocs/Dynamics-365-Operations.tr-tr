---
title: Planlama Optimizasyonu yayımlama işlemi ve sürüm geçmişi
description: Bu konuda, Planlama Optimizasyonu için yayımlama işlemi ve sürüm geçmişi hakkında bilgi verilmektedir.
author: crytt
ms.date: 8/17/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2021-07-28
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: fcd18341629afcf3092a457ae711e27b0bbfeb2a
ms.sourcegitcommit: 03f53980a4bc67b73ac2be76a3b3e7331d0db705
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/18/2021
ms.locfileid: "7394429"
---
# <a name="planning-optimization-release-process-and-release-history"></a>Planlama Optimizasyonu yayımlama işlemi ve sürüm geçmişi

[!include [banner](../../includes/banner.md)]

Microsoft, Planlama Optimizasyonu'nu aylık olarak güncelleştirir. Ancak iş gereksinimlerine bağlı olarak zamanlanmış sürümler arasında zaman zaman ek güncelleştirmeler yayımlarız.

Her sürüm, Planlama Optimizasyonu'nun kullanılabildiği bölgelere özel olarak yayımlanır. İşlem genellikle üç gün sürer.

Planlama Optimizasyonu güncelleştirilirken master planlama, normalden biraz daha yavaş çalışabilir.

Planlama Optimizasyonu'nu kullanan ortamlar en son sürümü otomatik olarak alır. Kullanıcı eylemi gerekmez: Hizmet otomatik olarak güncelleştirilir. Bununla birlikte, hataya neden olmayan değişiklik işlevi kesinlikle ortamlara otomatik olarak yayımlanmaz. Varsayılan olarak, hataya neden olduğu düşünülen tüm değişiklikler kapalıdır ve [özellik yönetimi](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) kullanılarak açık bir şekilde belirtilerek açılması gerekir. Bu nedenle, siz bunları etkinleştirmeyi seçene kadar bu değişiklikler ortamlarda görünmez.

Planlama Optimizasyonu, ortamınızda güncelleştirildiğinde herhangi bir bildirim gösterilmediğinden değişikliklerin ne zaman yayımlandığını ve hangi işlevleri getirdiğini belirlemek üzere aşağıdaki tablodaki sürüm notlarını inceleyebilirsiniz. Bu tablo, Planlama Optimizasyonu için yayımlanan değişiklikleri, bu değişikliklerin özellik yönetiminden bir özellikle ilişkili olup olmadığını ve sürüm tarihini gösterir.

| Değişiklikler | Özellik yönetimi ayrıntıları | Nakledilebilecek tarih |
|---|---|---|
| <p>**Sağlama süresi** alanı planlı siparişlere eklendi.</p><p>Genel performans, kalite ve kararlılık iyileştirmeleri.</p> | Özellik yönetimi gerekmez. | 16 Ağustos 2021 |
| <p>Sonsuz kapasite planlaması için kaynak türü gereksinimleri eklendi.</p><p>Sonsuz kapasite planlaması için kaynak verimliliği ve takvim verimliliği iyileştirildi.</p><p>Daha fazla bilgi için bkz. [Sonsuz kapasiteyle zamanlama](infinite-capacity-planning.md). | <p>10.0.20 sürümünden itibaren özellik yönetiminde kullanılabilir.</p><p>Özellik adı: *Planlama Optimizasyonu için sonsuz kapasite zamanlaması*</p> | 6 Temmuz 2021 |
| Genel kalite iyileştirmeleri. | Özellik yönetimi gerekmez. | 6 Temmuz 2021 |

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
