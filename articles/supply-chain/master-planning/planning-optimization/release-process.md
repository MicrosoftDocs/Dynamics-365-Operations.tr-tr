---
title: Planlama Optimizasyonu yayımlama işlemi ve sürüm geçmişi
description: Bu konuda, Planlama Optimizasyonu için yayımlama işlemi ve sürüm geçmişi hakkında bilgi verilmektedir.
author: ChristianRytt
ms.date: 09/21/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2021-07-28
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: f9674bb68d7f577a6efdef3416d1731d743d0555
ms.sourcegitcommit: 7893ffb081c36838f110fadf29a183f9bdb72dd3
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/02/2022
ms.locfileid: "8087178"
---
# <a name="planning-optimization-release-process-and-release-history"></a>Planlama Optimizasyonu yayımlama işlemi ve sürüm geçmişi

[!include [banner](../../includes/banner.md)]

Microsoft, Planlama Optimizasyonu'nu aylık olarak güncelleştirir. Ancak iş gereksinimlerine bağlı olarak zamanlanmış sürümler arasında zaman zaman ek güncelleştirmeler yayımlarız.

Her sürüm, Planlama Optimizasyonu'nun kullanılabildiği bölgelere özel olarak yayımlanır. İşlem genellikle üç gün sürer.

Planlama Optimizasyonu güncelleştirilirken master planlama, normalden biraz daha yavaş çalışabilir.

Planlama Optimizasyonu'nu kullanan ortamlar en son sürümü otomatik olarak alır. Kullanıcı eylemi gerekmez: Hizmet otomatik olarak güncelleştirilir. Bununla birlikte, hataya neden olmayan değişiklik işlevi kesinlikle ortamlara otomatik olarak yayımlanmaz. Varsayılan olarak, hataya neden olduğu düşünülen tüm değişiklikler kapalıdır ve [özellik yönetimi](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) kullanılarak açık bir şekilde belirtilerek açılması gerekir. Bu nedenle, siz bunları etkinleştirmeyi seçene kadar bu değişiklikler ortamlarda görünmez.

Planlama Optimizasyonu, ortamınızda güncelleştirildiğinde herhangi bir bildirim gösterilmediğinden değişikliklerin ne zaman yayımlandığını ve hangi işlevleri getirdiğini belirlemek üzere aşağıdaki tablodaki sürüm notlarını inceleyebilirsiniz. Bu tablo, Planlama Optimizasyonu için yayımlanan değişiklikleri, bu değişikliklerin özellik yönetiminden bir özellikle ilişkili olup olmadığını ve sürüm tarihini gösterir.

| Değişiklikler | Özellik yönetimi ayrıntıları | Yayın tarihleri |
|---|---|---|
| <p>Üretim emirleri için planlama önceliği desteği eklendi. | Planlama İyileştirmesi için *Öncelik temelli MRP desteği* özelliği kapsamında 10.0.25 sürümünde kullanıma sunuldu. | 12-18 Kasım 2021 |
| <p>Genel performans, kalite ve kararlılık iyileştirmeleri. | Özellik yönetimi gerekmez. | 12-18 Kasım 2021 |
| <p>İşlem süresi hesaplaması formülleri, çakışmayla üretim rotası ve gereksinim hareketlerinde üretim operasyon numarası için destek eklendi.</p><p>Zaman aşımı ile ilgili üretim planlama çizelgeleme için geliştirilmiş hata iletileri, kapasite bulunamadı ve döngüsel rota.</p><p>Planlı siparişlerde ve kesinleştirilmiş siparişlerde giriş tarihleri ve çıkış tarihleri hesaplanırken iyileştirilmiş tutarlılık.</p><p>Genel performans, kalite ve kararlılık iyileştirmeleri. | Özellik adı: *Planlama Optimizasyonu için sonsuz kapasite zamanlaması* | 22-27 Ekim, 2021 |
| <p>İşlem süresi hesaplamasında ıskarta yüzdesini dikkate alarak destek eklendi.</p><p>Planlama sırasında operasyon numarası ve malzeme kullanımı desteği eklendi. | Özellik adı: *Planlama Optimizasyonu için sonsuz kapasite zamanlaması* | 5-7 Ekim, 2021 |
| <p>Üretim rotası iş tipleri için destek eklendi: **Önceden kuyruğa al**, **Sonradan kuyruğa al** ve **Taşıma süresi**.</p><p>Genel performans, kalite ve kararlılık iyileştirmeleri. | Özellik adı: *Planlama Optimizasyonu için sonsuz kapasite zamanlaması* | 25-30 Eylül 2021 |
| <p>**Planlama yöntemi** *İşlemleri planlama* olarak ayarlanan master planlar için destek eklendi.</p><p>**Rota grupları** sayfasında, *Kurulum* veya *İşlem* için **Rota/iş türü** bulunan satırlarda **Etkinleştirme**, **Çalışma zamanı** ve **Kapasite** onay kutularının ayarlarını dikkate alın. </p><p>Genel performans, kalite ve kararlılık iyileştirmeleri. | <p>İşlemleri planlama, 10.0.20 sürümünden itibaren özellik yönetiminde kullanılabilir.</p><p>Özellik adı: *Planlama Optimizasyonu için sonsuz kapasite zamanlaması*</p>  | 9 - 17 Eylül 2021 |
| Genel performans, kalite ve kararlılık iyileştirmeleri. | Özellik yönetimi gerekmez. | 25 - 30 Ağustos 2021 |
| <p>**Sağlama süresi** alanı planlı siparişlere eklendi.</p><p>Genel performans, kalite ve kararlılık iyileştirmeleri.</p> | Özellik yönetimi gerekmez. | 12 - 17 Ağustos 2021 |
| <p>Sonsuz kapasite planlaması için kaynak türü gereksinimleri eklendi.</p><p>Sonsuz kapasite planlaması için kaynak verimliliği ve takvim verimliliği iyileştirildi.</p><p>Daha fazla bilgi için bkz. [Sonsuz kapasiteyle zamanlama](infinite-capacity-planning.md). | <p>10.0.20 sürümünden itibaren özellik yönetiminde kullanılabilir.</p><p>Özellik adı: *Planlama Optimizasyonu için sonsuz kapasite zamanlaması*</p> | 6 - 12 Temmuz 2021 |
| Genel kalite iyileştirmeleri. | Özellik yönetimi gerekmez. | 6 - 12 Temmuz 2021 |

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
