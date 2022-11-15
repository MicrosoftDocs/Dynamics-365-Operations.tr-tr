---
title: Gecikme toleransı (negatif günler)
description: Bu makale, gecikme toleransı hesaplaması ve bunun Planlamayı En İyi Duruma Getirme'de planlı sipariş oluşturmayı nasıl etkilediği hakkında bilgi sağlar.
author: t-benebo
ms.date: 08/09/2022
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2021-07-30
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: 78ba4236705f1a200d9fe796eb80d0241b0fa537
ms.sourcegitcommit: 491ab9ae2b6ed991b4eb0317e396fef542d3a21b
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/03/2022
ms.locfileid: "9740481"
---
# <a name="delay-tolerance-negative-days"></a>Gecikme toleransı (negatif günler)
<!-- KFM: Split topic into PO and classic -->

[!include [banner](../../includes/banner.md)]

Gecikme toleransı işlevi, Planlamayı En İyi Duruma Getirme özelliğinin karşılama grupları, madde karşılaması ve/veya master planları için **Negatif günler** değerini dikkate almasını sağlar. Master planlama sırasında uygulanan gecikme toleransı süresini uzatmak için kullanılır. Bu şekilde, mevcut tedarik talebi kısa bir gecikmeyle karşılayabilecekse yeni tedarik emirleri oluşturmaktan kaçınabilirsiniz. İşlev'n amacı, belirli bir talep için yeni bir tedarik emri oluşturmanın mantıklı olup olmadığını belirlemektir.

## <a name="turn-delay-tolerance-features-on-or-off"></a>Gecikme toleransı özelliklerini açma veya kapama

Gecikme toleransı işlevini sisteminizde kullanılabilir yapmak için, [Özellik yönetimine](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) gidin ve aşağıdaki özellikleri etkinleştirin:

- *Planlamayı En İyi Duruma Getirme için negatif günler* – Bu özellik, kapsam grupları ve madde karşılaması için negatif gün ayarlarını etkinleştirir. Supply Chain Management sürüm 10.0.29 itibarıyla, özellik zorunludur ve kapatılamaz.
- *Siparişe göre üretim tedarik otomasyonu* – Bu özellik master planlar için negatif gün ayarlarını etkinleştirir. (Daha fazla bilgi için bkz. [Siparişe göre üretim tedarik otomasyonu](../make-to-order-supply-automation.md).)

## <a name="delay-tolerance-in-planning-optimization"></a>Planlamayı En İyi Duruma Getirmede gecikme toleransı

Gecikme toleransı, mevcut tedarik zaten planlandığında yeni stok yenileme istemeden önce beklemeye istekli olduğunuz sağlama süresi ötesindeki gün sayısını temsil eder. Gecikme toleransı, iş günleri değil takvim günleri kullanılarak tanımlanır.

Master planlama sırasında, sistem gecikme toleransını hesapladığında, **Negatif günler** ayarını dikkate alır. **Negatif günler** değerini, **Karşılama grupları** sayfasında veya **Madde karşılama** sayfasında veya **Master planlar** sayfasında ayarlayabilirsiniz. Negatif günler birden fazla düzeye atanırsa, hangi ayarın kullanılacağının kararını vermek için sistem aşağıdaki hiyerarşiyi uygular:

- **Master planlar** sayfasında negatif günler etkinse, bu ayar plan çalıştığı zaman diğer tüm negatif günlerin ayarlarını geçersiz kılar.
- **Madde karşılama** sayfasında negatif günler yapılandırılmışsa bu ayar karşılama grubu ayarını geçersiz kılar.
- **Karşılama grupları** sayfasında yapılandırılan negatif günler yalnızca, ilgili madde veya plan için negatif günler yapılandırılmamış ise geçerlidir.

Sistem gecikme toleransı hesaplamasını *en erken stok yenileme tarihine* bağlar; bu da bugünün tarihi + sağlama süresine eşittir. Gecikme toleransı, *maks()* öğesinin iki değerden daha büyük olanı bulduğu aşağıdaki formül kullanılarak hesaplanır:

*maks(En erken stok yenileme tarihi, Talep son tarihi)* – *Talep son tarihi* + *Negatif günler*

Bu formül, ürün sağlama süresi boyunca yeterli tedarik olduğunda master planlamanın yeni tedarik emirleri oluşturmamasını sağlar.

> [!NOTE]
> Planlama Optimizasyonu'nda gecikme toleransı hesaplaması her zaman kullanımdan kaldırılan master planlama altyapısından alınan dinamik negatif gün hesaplamasını kullanır. **Master planlama parametreleri** sayfasindaki **Dinamik negatif günleri kullan** ayarının bu davranış üzerinde hiçbir etkisi yoktur.

Mevcut tedarik, hesaplanan gecikme toleransından daha az veya buna eşit bir talep gecikmesi anlamına gelirse Planlamayı En İyi Duruma Getirme, mevcut tedariki taleple birlikte sabitler. Bazı durumlarda, aşırı tedarikle sonuçlanmaktansa talebi geciktirmek daha iyidir.

Aşağıdaki alt bölümler, gecikme toleransının Planlamayı En İyi Duruma Getirmedeki planlı siparişlerin oluşturulmasını nasıl etkilediğini gösteren örnekler sağlar.

### <a name="example-1"></a>Örnek 1

Bir ürün aşağıdaki yapılandırmaya sahiptir:

- **Sağlama süresi:** *10*
- **Negatif günler:** *2*

Ürün için aşağıdaki tedarik ve talep mevcuttur:

- **Bugün için talep:** 10 adet için satış siparişi
- **12 günde tedarik:** 10 adet için satınalma siparişi

Mevcut tedarik, talebi 12 gün içinde karşılayabilir ve bu süre gecikme toleransına eşittir. Bu nedenle, master planlama çalıştığında, planlı sipariş oluşturulmaz.

### <a name="example-2"></a>Örnek 2

Bir ürün aşağıdaki yapılandırmaya sahiptir:

- **Sağlama süresi:** *10*
- **Negatif günler:** *0*

Ürün için aşağıdaki tedarik ve talep mevcuttur:

- **Bugün için talep:** 10 adet için satış siparişi
- **12 günde tedarik:** 10 adet için satınalma siparişi

Mevcut tedairk talebi ancak 12 gün sonra karşılayabilir. Ancak, gecikme toleransı 10 gündür. Bu nedenle, master planlama çalıştığında, 10 adet için planlı bir sipariş oluşturulur.

### <a name="example-3"></a>Örnek 3

Bir ürün aşağıdaki yapılandırmaya sahiptir:

- **Sağlama süresi:** *10*
- **Negatif günler:** *2*

Ürün için aşağıdaki tedarik ve talep mevcuttur:

- **11 gün içinde talep:** 10 adet için satış siparişi
- **14 günde tedarik:** 10 adet için satınalma siparişi

Mevcut tedairk talebi ancak üç gün sonra karşılayabilir. Ancak, gecikme toleransı iki gündür. (Bu durumda, gecikme toleransı yalnızca iki negatif günü içerir. Talep tarihi, ürün sağlama süresinden sonra olduğu için dahil edilmez.) Bu nedenle, master planlama çalıştığında, 10 miktarı için planlı bir sipariş oluşturulur.
