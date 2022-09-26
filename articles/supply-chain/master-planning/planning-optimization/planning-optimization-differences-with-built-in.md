---
title: Yerleşik master planlama ile Planlama Optimizasyonu arasındaki farklar
description: Bu makalede, Planlama Optimizasyonu'nun henüz desteklemediği ve Planlama Optimizasyonu uygunluk analizi sayfasında listelenmeyen özellikler listelenmektedir.
author: t-benebo
ms.date: 07/30/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2021-07-30
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: dd9493e85a90c00b2dd50abb6530661c0fbb77dc
ms.sourcegitcommit: d2046cad5de570e6302a4390b41881a7ecb12e26
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/15/2022
ms.locfileid: "9520856"
---
# <a name="differences-between-built-in-master-planning-and-planning-optimization"></a>Yerleşik master planlama ile Planlama Optimizasyonu arasındaki farklar

[!include [banner](../../includes/banner.md)]

Planlama Optimizasyonu sonuçları, yerleşik master planlama motorundan alınan sonuçlardan farklı olabilir. Farklılıkların nedeni beklemedeki özellikler olabilir. Bu makalede, Planlama Optimizasyonu'nun henüz desteklemediği ve **[Planlama Optimizasyonu uygunluk analizi](planning-optimization-fit-analysis.md)** sayfası'nda listelenmeyen özellikler listelenmektedir].

| Özellik | Planlama Optimizasyonu'nun geçerli davranışı |
|---|---|
| Fiili ağırlık ürünleri | Fiili ağırlık ürünleri normal ürünler olarak kabul edilir.|
| Genişletilebilir boyutlar | Genişletilebilir boyutlar Planlama İyileştirmesi tarafından desteklenmiyor. Planlama İyileştirmesi kullanırken, **Depolama boyutu grupları** veya **İzleme boyutu grupları** sayfasında **Boyuta göre kapsam planı** onay kutusu seçili olsa bile planlı siparişlerde genişletilebilir boyutlar boştur. |
| Filtrelenmiş üretim çalışmaları | Ayrıntılar için bkz. [Üretim planlaması: Filtreler](production-planning.md#filters). |
| Tahmin planlama | Tahmin planlama desteklenmez. Master planlamaya bir tahmin modeli atandığında master planlamayı kullanmanızı öneririz. |
| Planlanan siparişler için numara serileri | Planlanan siparişler için numara serileri desteklenmez. Hizmet tarafında planlı sipariş numaraları oluşturulur. Planlı sipariş numarası normalde 10 basamakla gösterilir, ancak sıra, planlanan siparişler sayımında planlama çalıştırma sayısı ve diğer 10 basamak için tahsis edilen 20 karakter üzerine oluşturulmuştur. |
| Plan kopyalama, plan silme ve plan sürümünü temizleme | <p>Gezinti bölmesinde **Master planlama \> Master planlama \> Planları yönet** altındaki aşağıdaki öğeler devre dışı bırakılmıştır:</p><ul><li>Plan kopyala</li><li>Planı sil</li><li>Sürüm temizleme planla</li></ul> |
| Sipariş iadeleri | İade emirleri dikkate alınmaz. |
| Zamanlama ile ilgili özellikler | Ayrıntılı bilgi için bkz. [Sonsuz kapasiteyle zamanlama](infinite-capacity-planning.md#limitations). |
| Emniyet stoğu karşılama | Planlama Optimizasyonu'nda, **Madde karşılama** sayfasındaki **Minimum karşılama** alanı için her zaman *Bugünün tarihi + tedarik süresi* seçeneği kullanılır. Bu, emniyet stoku için tedarik süresi dahil edilmezse düşük eldeki stok için oluşturulan planlı siparişler sağlama süresi nedeniyle her zaman gecikeceğinden istenmeyen planlı siparişleri ve diğer sorunları önlemeye yardımcı olur. |
| Emniyet stoku ilişkilendirme ve net gereksinimler | *Emniyet stoku* gereksinim türü dahil edilmez ve **Net gereksinimler** sayfasında görüntülenmez. Emniyet stoku, talebi temsil etmez ve kendisiyle ilişkilendirilmiş gereksinim tarihi yoktur. Bunun yerine, her zaman stokta bulunması gereken miktar ile ilgili kısıtlama ayarlar. Ancak master planlama sırasında planlı siparişleri hesaplarken **Minimum** alan değeri yine de dikkate alınır. Bu değerin dikkate alındığını görmek için **Net gereksinimler** sayfasında **Kümülatif miktar** sütununu incelemenizi öneririz. |
| Taşıma takvimleri | **Teslimat şekilleri** sayfasındaki **Taşıma takvimi** sütunundaki değer yok sayılır. |
| Değeri olmayan minimum/maksimum karşılama kodu| Yerleşik planlama altyapısıyla, minimum veya maksimum değerlerin ayarlandığı bir minimum/maksimum karşılama kodu kullandığınızda, planlama altyapısı karşılama kodunu gereksinim olarak işler ve her gereksinim için bir sipariş oluşturur. Planlama Optimizasyonu ile sistem, o güne ait tam tutarın kapsayacağı bir günde bir sipariş oluşturacaktır.  |
| Net gereksinimler ve el ile oluşturulan planlı siparişler | Yerleşik planlama altyapısıyla, bir madde için el ile oluşturulmuş tedarik emirleri bu maddeyle ilgili net gereksinimler arasında otomatik olarak görüntülenir. Örneğin, bir satış siparişinden bir satınalma siparişi oluştururken, satınalma siparişi, **Net gereksinimler** sayfasında, önceki bir eylemi gerektirmeden görünür. Bunun nedeni, yerleşik planlama motorunun `inventLogTTS` tablosunda stok hareketlerini günlüklerine kaydettiği ve dinamik planlar için **Net gereksinimler** sayfasındaki değişiklikleri gösterdiği bir yer değildir. Ancak, Planlama Optimizasyonu sayesinde manuel oluşturulan siparişler, Planlama Optimizasyonu çalıştırılana kadar (maddeyi içeren bir plan ile) veya maddeyle ilgili master planlamayı çalıştıracak olan **Net gereksinimler** sayfasının eylem bölmesinde **Güncelleştir \> Master planlama**'yı seçene kadar maddenin net gereksinimleri içinde görüntülenmez. **Net gereksinimler** sayfası ile nasıl çalışılacağı hakkında daha fazla bilgi için bkz. [Planlama Optimizasyonu ile ilgili net gereksinimler ve ilişkilendirme bilgileri](net-requirements.md). |
| Kaynak ataması | Sonsuz kapasiteyle çalışırken, yerleşik ana planlama altyapısı tüm planlanan siparişleri belirli bir kaynak grubuna aynı kaynağa atar. Planlama İyileştirmesi bunu, kaynakları rasgele seçerek artırmak için farklı üretim emirlerinin farklı kaynaklar kullanmasına olanak sağlar. Tüm planlı siparişler için aynı kaynağı kullanmak istiyorsanız, bu kaynağı rotada belirtmeniz gerekir. |

## <a name="additional-resources"></a>Ek kaynaklar

- [Planlama Optimizasyonu uygunluk analizi](planning-optimization-fit-analysis.md)
- [Planlama Optimizasyonu tarafından kullanılmayan parametreler](not-used-parameters.md)
- [Planlama Optimizasyonu tarafından kullanılan tarih ve saat parametreleri](date-time-used.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
