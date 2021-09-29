---
title: Yerleşik master planlama ile Planlama Optimizasyonu arasındaki farklar
description: Bu konuda, Planlama Optimizasyonu'nun henüz desteklemediği ve Planlama Optimizasyonu uygunluk analizi sayfasında listelenmeyen özellikler listelenmektedir.
author: crytt
ms.date: 07/30/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2021-07-30
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: 63f3bc6cb7563ee6ff719272a0795efffcb40bc8
ms.sourcegitcommit: ecd4c148287892dcd45656f273401315adb2805e
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/18/2021
ms.locfileid: "7500209"
---
# <a name="differences-between-built-in-master-planning-and-planning-optimization"></a>Yerleşik master planlama ile Planlama Optimizasyonu arasındaki farklar

[!include [banner](../../includes/banner.md)]

Planlama Optimizasyonu sonuçları, yerleşik master planlama motorundan alınan sonuçlardan farklı olabilir. Farklılıkların nedeni beklemedeki özellikler olabilir. Bu konuda, Planlama Optimizasyonu'nun henüz desteklemediği ve **[Planlama Optimizasyonu uygunluk analizi](planning-optimization-fit-analysis.md)** sayfası'nda listelenmeyen özellikler listelenmektedir].

| Özellik | Planlama Optimizasyonu'nun geçerli davranışı |
|---|---|
| Fiili ağırlık ürünleri | Fiili ağırlık ürünleri normal ürünler olarak kabul edilir.|
| Genişletilebilir boyutlar | **Depolama boyutu grupları** veya **İzleme boyutu grupları** sayfasında **Boyuta göre kapsam planı** onay kutusu seçili olsa bile planlı siparişlerde genişletilebilir boyutlar boştur. |
| Filtrelenmiş üretim çalışmaları | Ayrıntılar için bkz. [Üretim planlaması: Filtreler](production-planning.md#filters). |
| Tahmin planlama | Tahmin planlama desteklenmez. Master planlamaya bir tahmin modeli atandığında master planlamayı kullanmanızı öneririz. |
| Planlanan siparişler için numara serileri | Planlanan siparişler için numara serileri desteklenmez. Hizmet tarafında planlı sipariş numaraları oluşturulur. |
| Plan kopyalama, plan silme ve plan sürümünü temizleme | <p>Gezinti bölmesinde **Master planlama \> Master planlama \> Planları yönet** altındaki aşağıdaki öğeler devre dışı bırakılmıştır:</p><ul><li>Plan kopyala</li><li>Planı sil</li><li>Sürüm temizleme planla</li></ul> |
| Sipariş iadeleri | İade emirleri dikkate alınmaz. |
| Zamanlama ile ilgili özellikler | Ayrıntılı bilgi için bkz. [Sonsuz kapasiteyle zamanlama](infinite-capacity-planning.md#limitations). |
| Emniyet stoğu karşılama | Planlama Optimizasyonu'nda, **Madde karşılama** sayfasındaki **Minimum karşılama** alanı için her zaman *Bugünün tarihi + tedarik süresi* seçeneği kullanılır. Bu, emniyet stoku için tedarik süresi dahil edilmezse düşük eldeki stok için oluşturulan planlı siparişler sağlama süresi nedeniyle her zaman gecikeceğinden istenmeyen planlı siparişleri ve diğer sorunları önlemeye yardımcı olur. |
| Emniyet stoku ilişkilendirme ve net gereksinimler | *Emniyet stoku* gereksinim türü dahil edilmez ve **Net gereksinimler** sayfasında görüntülenmez. Emniyet stoku, talebi temsil etmez ve kendisiyle ilişkilendirilmiş gereksinim tarihi yoktur. Bunun yerine, her zaman stokta bulunması gereken miktar ile ilgili kısıtlama ayarlar. Ancak master planlama sırasında planlı siparişleri hesaplarken **Minimum** alan değeri yine de dikkate alınır. Bu değerin dikkate alındığını görmek için **Net gereksinimler** sayfasında **Kümülatif miktar** sütununu incelemenizi öneririz. |
| Taşıma takvimleri | **Teslimat şekilleri** sayfasındaki **Taşıma takvimi** sütunundaki değer yok sayılır. |

## <a name="additional-resources"></a>Ek kaynaklar

- [Planlama Optimizasyonu uygunluk analizi](planning-optimization-fit-analysis.md)
- [Planlama Optimizasyonu tarafından kullanılmayan parametreler](not-used-parameters.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
