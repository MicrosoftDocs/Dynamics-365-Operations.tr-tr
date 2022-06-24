---
title: Gecikme toleransı (negatif günler)
description: Bu makale, gecikme toleransı hesaplaması ve bunun Planlamayı En İyi Duruma Getirme'de planlı sipariş oluşturmayı nasıl etkilediği hakkında bilgi sağlar.
author: t-benebo
ms.date: 07/30/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2021-07-30
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: 4bd6042f9dd33ba15773b251911e965cb870c5aa
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8865135"
---
# <a name="delay-tolerance-negative-days"></a>Gecikme toleransı (negatif günler)

[!include [banner](../../includes/banner.md)]

Gecikme toleransı işlevi, Planlamayı En İyi Duruma Getirme özelliğinin karşılama grupları için ayarlanan **Negatif günler** değerini dikkate almasını sağlar. Master planlama sırasında uygulanan gecikme toleransı süresini uzatmak için kullanılır. Bu şekilde, mevcut tedarik talebi kısa bir gecikmeyle karşılayabilecekse yeni tedarik emirleri oluşturmaktan kaçınabilirsiniz. İşlev'n amacı, belirli bir talep için yeni bir tedarik emri oluşturmanın mantıklı olup olmadığını belirlemektir.

## <a name="turn-on-the-feature-in-your-system"></a>Sisteminizdeki özelliği etkinleştirme

Gecikme toleransı işlevini sisteminizde kullanılabilir yapmak için, [Özellik yönetimi](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)'ne gidin ve *Planlamayı En İyi Duruma Getirme için negatif günler* özelliğini etkinleştirin.

## <a name="delay-tolerance-in-planning-optimization"></a>Planlamayı En İyi Duruma Getirmede gecikme toleransı

Gecikme toleransı, mevcut tedarik zaten planlandığında yeni stok yenileme istemeden önce beklemeye istekli olduğunuz sağlama süresi ötesindeki gün sayısını temsil eder. Gecikme toleransı, iş günleri değil takvim günleri kullanılarak tanımlanır.

Master planlama sırasında, sistem gecikme toleransını hesapladığında, **Negatif günler** ayarını dikkate alır. **Negatif günler** değerini, **Karşılama grupları** sayfasında veya **Madde karşılama** sayfasında ayarlayabilirsiniz.

Sistem gecikme toleransı hesaplamasını *en erken stok yenileme tarihine* bağlar; bu da bugünün tarihi + sağlama süresine eşittir. Gecikme toleransı, *maks()* öğesinin iki değerden daha büyük olanı bulduğu aşağıdaki formül kullanılarak hesaplanır:

*maks(En erken stok yenileme tarihi, Talep son tarihi)* – *Talep son tarihi* + *Negatif günler*

Bu formül, ürün sağlama süresi boyunca yeterli tedarik olduğunda master planlamanın yeni tedarik emirleri oluşturmamasını sağlar.

> [!NOTE]
> Planlamayı En İyi Duruma Getirme'de gecikme toleransı hesaplaması her zaman yerleşik master planlamadan alınan dinamik negatif gün hesaplamasını kullanır. **Master planlama parametreleri** sayfasindaki **Dinamik negatif günleri kullan** ayarının bu davranış üzerinde hiçbir etkisi yoktur.

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
