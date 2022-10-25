---
title: Sınırlı kapasite planlaması ve zamanlama
description: Sınırlı kapasite planlaması ve zamanlama, farklı kaynaklarla ilgili sınırlamalar dikkate alınarak belirli bir dönemde ne kadar iş üretilebileceğini anlamanıza yardımcı olur.
author: t-benebo
ms.date: 09/19/2022
ms.topic: article
ms.search.form: ReqParameters, ReqPlanSched, WrkCtrTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2022-09-19
ms.dyn365.ops.version: 10.0.29
ms.openlocfilehash: 3d116b5f7f456630415378e6cc069907e339068b
ms.sourcegitcommit: 3e04f7e4bc0c29c936dc177d5fa11761a58e9a02
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/18/2022
ms.locfileid: "9689706"
---
# <a name="finite-capacity-planning-and-scheduling"></a>Sınırlı kapasite planlaması ve zamanlama

[!include [banner](../../includes/banner.md)]
[!INCLUDE [preview-banner](../../includes/preview-banner.md)]
<!--KFM: Preview until 10.0.31 GA -->

Sınırlı kapasite, farklı kaynaklarla ilgili sınırlamalar dikkate alınarak belirli bir dönemde ne kadar iş üretilebileceğini anlamanıza yardımcı olan bir yaklaşımdır. Sınırlı kapasite çizelgelemenin amacı, işin tesis genelinde eşit ve verimli bir hızda ilerlemesini sağlamaktır.

Sınırlı kapasite planlaması ve zamanlama, sınırsız yükleme yaklaşımının oluşturduğu üretim süreçleri için daha gerçekçi bir zaman çizelgesi oluşturur. Kaynaklarda yeterli kapasite yoksa teslim tarihi gönderilir ve iş, yeterli kapasite olduğunda çizelgelenir.

## <a name="planning-optimization-support-for-finite-capacity-planning"></a>Sınırsız kapasite planlaması için Planlama Optimizasyonu desteği

Sınırlı kapasite planlaması ve programlama, Planlama Optimizasyonu'nu veya yerleşik planlama altyapısını kullanmanızdan bağımsız olarak neredeyse aynı şekilde çalışır. Ancak Planlama Optimizasyonu **Darboğaz özellikli zaman** dilimi parametresini kullanmaz. Planlama Optimizasyonu kullandığınızda, darboğaz özellikli kaynaklar her zaman darboğaz özellikli olmayan kaynaklarla aynı zaman dilimi kullanılarak planlanır (sınırlı kapasite zaman dilimi ile belirtildiği gibi).

## <a name="set-up-finite-capacity-functionality"></a>Sonlu kapasite işlevselliği ayarlama

Sınırlı kapasite işlevlerini kullanmak için genel olarak kapasite planlamasını etkinleştirmeniz ve hem kullanmak istediğiniz master plan için hem de uygulandığı her kaynak için sonlu kapasite planlamasını etkinleştirmeniz gerekir. Sınırlı kapasitenin etkin olduğu planlar ve kaynaklar için planlı üretim emirlerinin planlanmasında zaten rezerve edilmiş olan kapasite dikkate alınacaktır. Planlı üretim emirleri, gereksinim tarihinden itibaren geriye doğru planlanır. Optimum programı karşılamak için kapasite mevcut değilse sistem bileşen öğelerini daha erken bir tarihte talep etmeye çalışır. Gereksinimler değişirken kapasiteniz de değişebiliyorsa (örneğin vardiyalı çalışma sırasında) hesaplanan işlem süreleri doğru olmayacağından, sınırlı kapasite işlevini kullanmamanız gerekir. Yalnızca sınırlı kapasitenin etkin olduğu kaynaklar için ayrılmış olan kapasiteyi dikkate alır. Bir kaynak için sınırlı kapasiteyi etkinleştirerek, sınırlı kapasite zaman dilimini değiştirebilirsiniz.

### <a name="activate-master-planning-parameters"></a>Master planlama parametrelerini etkinleştirme

Sınırlı kapasite işlevlerini kullanmak için **Master planlama parametreleri** sayfasında kapasite planlamasını etkinleştirmeniz gerekir.

1. **Master planlama \> Kurulum \> Master planlama parametreleri**'ne gidin.
1. **Planlı siparişler** sekmesinde **Kapasite planlaması** bölümünde **Üretim** seçeneğini *Evet* olarak ayarlayın.

### <a name="activate-a-master-plan"></a>Master planı etkinleştirme

Kullanmak istediğiniz her master plan için sınırlı kapasite planlamasını ve çizelgelemeyi etkinleştirmeniz gerekir.

1. **Master planlama \> Kurulum \> Planlar \> Master planlar** bölümüne gidin.
1. Liste bölmesinde, sınırlı kapasite planlaması ve çizelgeleme kullanacak şekilde ayarlamak istediğiniz bir master plan seçin.
1. **Genel** hızlı sekmesinde **Planlı üretim emirleri** bölümünde **Sınırlı kapasite** seçeneğini *Evet* olarak ayarlayın.
1. Ayarlamak istediğiniz her ek master plan için 2 ve 3 numaralı adımları yineleyin.

### <a name="activate-resources"></a>Kaynakları etkinleştirme

Kullanmak istediğiniz her kaynak için sınırlı kapasite planlamasını ve çizelgelemeyi etkinleştirmeniz gerekir.

1. **Üretim denetimi \> Kurulum \> Kaynaklar \> Kaynaklar**'a gidin.
1. Liste bölmesinde, sınırlı kapasite planlaması ve çizelgeleme kullanacak şekilde ayarlamak istediğiniz bir kaynak seçin.
1. **İşlem** hızlı sekmesinde, **Kapasite düğmesi** bölümünde **Sınırlı kapasite** seçeneğini *Evet* olarak ayarlayın.
1. Ayarlamak istediğiniz her ek kaynak için 2 ve 3 numaralı adımları yineleyin.

## <a name="examples"></a>Örnekler

Bu bölüm, sınırlı ve sınırsız kapasite planlaması ve zamanlama ile nasıl çalışacağınıza ilişkin aşağıdaki örnekleri sağlamaktadır:

- Örnek 1 – Sonsuz kapasite planlaması
- Örnek 2 – Bir günlük zaman dilimiyle sınırlı kapasite planlaması
- Örnek 3 – İki günlük zaman dilimiyle sınırlı kapasite planlaması

### <a name="preconditions"></a>Ön koşullar

Üç örnek de bu bölümde açıklanan ön koşullar varsaymaktadır.

*Product1* ürünü, aşağıdaki işlemleri içeren bir rotaya sahiptir.

| İşlem no. | Operasyon adı | Kaynak        | Çalıştırma | İşlem miktarı | İleri |
|---------------|----------------|-----------------|----------|--------------|------|
| 10            | Kaynak        | Kaynak hattı    | 1        | 2            | 20   |
| 20            | Montaj     | Montaj hattı | 1        | 4            |      |

Şirketinizdeki çalışanlar sekiz saat boyunca tek vardiyada çalışıyor (8:00 – 16:00).

*24 adet* *Product1* için planlı üretim emri mevcut. Teslim tarihi *Bugün + 3 gün*'dür.

Planlama sonucunda, sistem, kaynakları aşağıdaki şekilde yükler:

- **Kaynak hattı:** Bu kaynak *Bugün, saat 8:00*'den *Bugün + 1, saat 12:00*'ye kadar yüklenir.
- **Montaj hattı:** Bu kaynak *Bugün + 1, saat 12:00*'den *Bugün + 2, saat 10:00*'a kadar yüklenir.

Aşağıdaki şekil, elde edilen Gantt grafiğini gösterir (daha büyük bir görünüm için seçin).

[![Ön koşulları gösteren Gantt grafiği.](media/finite-examples-conditions-small.png "Ön koşulları gösteren Gantt grafiği")](media/finite-examples-conditions.png)

### <a name="example-1--infinite-capacity-planning"></a>Örnek 1 – Sonsuz kapasite planlaması

Bu örnek, sınırlı kapasite planlaması yerine sınırsız kapasite planlaması kullandığınızda planlama sonuçlarını gösterir.

Master planda, plan için sınırlı kapasite planlamasını devre dışı bırakan aşağıdaki ilgili ayar vardır:

- **Sınırlı kapasite:** *Hayır*

Sınırlı kapasite planlamasını devre dışı bırakmak için her iki kaynak için de **Sınırlı kapasite** seçeneği *Hayır* olarak ayarlanır:

- Kaynak hattı
- Montaj hattı

Şimdi *8 adet* *Product1* için yeni bir satış emri ekliyor ve planı çalıştırıyorsunuz. Sonuç olarak sistem, kaynak hattını *Bugün, saat 8:00*'den *Bugün, saat 12:00*'ye kadar yükler. Kaynak hattındaki işlemler tamamlandıktan sonra, sistem, montaj hattını *Bugün, saat 12:00*'den *Bugün, saat 14:00*'e kadar yükler.

Aşağıdaki şekil, elde edilen Gantt grafiğini gösterir (daha büyük bir görünüm için seçin).

[![Sınırsız kapasite planlaması örneği gösteren Gantt grafiği.](media/finite-examples-example1-small.png "Sınırsız kapasite planlaması örneği gösteren Gantt grafiği")](media/finite-examples-example1.png)

### <a name="example-2--finite-capacity-planning-with-a-time-fence-of-one-day"></a>Örnek 2 – Bir günlük zaman dilimiyle sınırlı kapasite planlaması

Bu örnek, sınırlı kapasite planlaması ve bir günlük zaman dilimi kullandığınızda planlama sonuçlarını gösterir.

Master planda, plan için sınırlı kapasite planlamasını etkinleştiren ve bir zaman dilimi ayarlayan aşağıdaki ilgili ayarlar vardır:

- **Sınırlı kapasite:** *Evet*
- **Sınırlı kapasite zaman dilimi:** *1*

Sınırlı kapasite planlamasını devre dışı bırakmak için her iki kaynak için de **Sınırlı kapasite** seçeneği *Evet* olarak ayarlanır:

- Kaynak hattı
- Montaj hattı

Şimdi *8 adet* *Product1* için yeni bir satış emri ekliyor ve planı çalıştırıyorsunuz. Sonuç olarak sistem, kaynak hattını *Bugün +1, saat 8:00*'den *Bugün + 1, saat 12:00*'ye kadar yükler. Kaynak hattındaki işlemler tamamlandıktan sonra, sistem, montaj hattını *Bugün +1, saat 12:00*'den *Bugün +1, saat 14:00*'e kadar yükler. Sistem sınırlı kapasiteyi yalnızca bir gün için kabul eder.

Aşağıdaki şekil, elde edilen Gantt grafiğini gösterir (daha büyük bir görünüm için seçin).

[![Bir günlük zaman dilimiyle sınırlı kapasite planlamasını gösteren Gantt grafiği.](media/finite-examples-example2-small.png "Bir günlük zaman dilimiyle sınırlı kapasite planlamasını gösteren Gantt grafiği")](media/finite-examples-example2.png)

### <a name="example-3--finite-capacity-planning-with-a-time-fence-of-two-days"></a>Örnek 3 – İki günlük zaman dilimiyle sınırlı kapasite planlaması

Bu örnek, sınırlı kapasite planlaması ve iki günlük zaman dilimi kullandığınızda planlama sonuçlarını gösterir.

Master planda, plan için sınırlı kapasite planlamasını etkinleştiren ve bir zaman dilimi ayarlayan aşağıdaki ilgili ayarlar vardır:

- **Sınırlı kapasite:** *Evet*
- **Sınırlı kapasite zaman dilimi:** *2*

Sınırlı kapasite planlamasını devre dışı bırakmak için her iki kaynak için de **Sınırlı kapasite** seçeneği *Evet* olarak ayarlanır:

- Kaynak hattı
- Montaj hattı

Şimdi *8 adet* *Product1* için yeni bir satış emri ekliyor ve planı çalıştırıyorsunuz. Sonuç olarak sistem, kaynak hattını *Bugün +1, saat 12:00*'den *Bugün + 1, saat 16:00*'ye kadar yükler. Kaynak hattındaki işlemler tamamlandıktan sonra, sistem, montaj hattını *Bugün + 2, saat 8:00*'den *Bugün + 2, saat 10:00*'e kadar yükler. Sistem sınırlı kapasiteyi yalnızca iki gün için kabul eder.

Aşağıdaki şekil, elde edilen Gantt grafiğini gösterir (daha büyük bir görünüm için seçin).

[![İki günlük zaman dilimiyle sınırlı kapasite planlamasını gösteren Gantt grafiği.](media/finite-examples-example3-small.png "İki günlük zaman dilimiyle sınırlı kapasite planlamasını gösteren Gantt grafiği")](media/finite-examples-example3.png)

> [!IMPORTANT]
> Sınırlı kapasite zaman dilimini daima iş ihtiyaçlarınıza uyacak şekilde ayarlamalısınız. Bu makalede sağlanan örneklerde yalnızca işlevler gösterilmektedir. Gerçekte, sınırlı kapasite planlaması kullanan çoğu üretici için bir günlük zaman dilimi muhtemelen çok düşüktür.
