---
title: Planlama altyapısı performansını iyileştirme
description: Bu konu, planlama altyapısı ve performansın nasıl geliştirileceği hakkında bilgi sağlar.
author: ChristianRytt
ms.date: 09/03/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: 19311
ms.assetid: 5ffb1486-2e08-4cdc-bd34-b47ae795ef0f
ms.search.region: Global
ms.search.industry: ''
ms.author: crytt
ms.search.validFrom: 2020-09-03
ms.dyn365.ops.version: ''
ms.openlocfilehash: 2495339f25469af705cff841f090c5df95b4d996
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/29/2021
ms.locfileid: "7578452"
---
# <a name="improve-scheduling-engine-performance"></a>Planlama altyapısı performansını iyileştirme

[!include [banner](../includes/banner.md)]

Kaynak planlama altyapısı, planlanan ve serbest bırakılmış üretim emirleri için rota planlarken kullanılır. Altyapı, ilk olarak Dynamics AX 2012'nin bir parçası olarak yayımlanmıştır ve yayımlanmasından bu yana çeşitli geliştirmeler yapılmıştır.

[İş atölyesi planlama sorunu](https://en.wikipedia.org/wiki/Job_shop_scheduling) çözüm süresinin karar değişkenlerinin sayısıyla katlanarak büyümesine neden olan çok karmaşık bir birleşimsel sorundur. Genellikle müşteriler, üretim rotalarını ve ilgili verileri, en modern donanımda bile, makul saatlerde çözülemeyen bir planlama sorununa neden olacak şekilde ayarlar. Bu konu, planlama altyapısını ve belirli bir kurulumun performans üzerindeki etkisini anlamanıza yardımcı olacaktır.

Planlamanın performansını geliştirmek söz konusu olduğunda, genel yönergeler altyapının çözmesi gereken sorunun karmaşıklığını azaltmayı önerir. Performansı etkileyebilen ana faktörlerin bazıları şunlardır:

- Birçok operasyon olan rotalar
- Paralel operasyonlar bulunan rotalar
- Kaynak miktarının birden yüksek olduğu operasyonlar
- Birçok uygulanabilir kaynağa sahip operasyonlar
- Sabit bağlantılar kullanımı
- Sınırlı kapasite kullanımı
- Kullanılan farklı takvimlerin sayısı
- Takvimde gün başına çalışma zamanı aralıklarının sayısı
- Rotanın toplam süresi
- Birden çok zamanlama altyapısını paralel çalıştırma

## <a name="overview-of-basic-scheduling-flow"></a>Temel planlama akışına genel bakış

Belirli bir kurulumun performansı nasıl etkileyebileceğini anlamak için, sürecin hem altyapıda hem de bunu çevreleyen X++ kodunda nasıl aktığını anlamak önemlidir.

Bir siparişin planlama için temel süreç üç ana adımdan oluşur:

- **Verileri yükleme** – Burada, X++ veri modelleri işler ve sınırlamalar biçiminde altyapının dahili veri modeline dönüştürülür.
- **Planlama** – Bu, belirli model ve sınırlamaları işleyen ve sonuç oluşturan zamanlama için ana kaynaktır. Bu süreç sırasında, altyapı çalışma zamanı bilgilerini ve mevcut kapasite rezervasyonlarını gerektiğinde X++'dan isteyecektir.
- **Veri kaydetme** – İş kapasitesi rezervasyon yuvaları formundaki altyapı sonucu, kapasite rezervasyonlarını kaydetmek ve işlerin/operasyonun/siparişin başlangıç ve bitiş saatlerini güncelleştirmek için X++ kodu tarafından işlenir.

## <a name="load-data-into-the-engine"></a>Altyapıya veri yükleme

Planlama altyapısının, farklı veri kaynaklarını işleyebilen bir genel altyapı olarak oluşturulması nedeniyle, Supply Chain Management veritabanından daha soyut bir veri modeli vardır. Rota, ikincil operasyonlar ve çalışma zamanı kavramlarının, altyapının sunduğu genel iş ve sınırlama modeline "çevrilmesi" gerekir. Modeli oluşturma mantığının, önemli miktarda iş mantığı vardır ve kaynak verilere göre farklılık gösterir. Sorumlu X++ sınıfı `WrkCtrScheduler`'dır ve planlanan üretim emirleri, serbest bırakılan üretim emirleri ve proje tahminleri için türetilmiş sınıflara sahiptir.

Örnek olarak, aşağıdaki tablo ve görüntüde gösterilen ve görece basit görünen bir yolu düşünün.

| Operasyon Hayır. | Öncelik | Hazırlık süresi | Çalıştırma | Sonrasındaki kuyruk süresi | Kaynak miktarı | İleri |
| --- | --- | --- | --- | --- | --- | --- |
| 10 | Birincil | 1.00 | 2.00 | | 1 | 20 |
| 10 | İkincil&nbsp;1 | | | | 1 | 20 |
| 20 | Birincil | | 3.00 | 1.00 | 3 | 0 |

![Örnek rota diyagramı.](media/scheduling-engine-route.png "Örnek rota diyagramı")

Bunu altyapıya gönderirken, aşağıdaki şekilde gösterildiği gibi sekiz işe bölünür (büyütmek istediğiniz görüntüyü seçin).

[![Altyapı işlerini planlama](media/scheduling-engine-jobs.png "Planlama altyapısı işleri.")](media/scheduling-engine-jobs-large.png)

İki iş arasındaki standart bağlantı `FinishStart` olur; bir işin bitiş saatinin başka bir işin başlangıç saatinden önce olması gerektiğini belirtir. Kurulumun daha sonra işlemi gerçekleştirecek aynı kaynak tarafından gerçekleştirilmesi gerektiğinden, aralarında `OnSameResource` sınırlamaları bulunur. 10 için birincil ve ikincil operasyon arasındaki işler `StartStart` ve `FinishFinish` bağlantıları bulunur; bu, işlerin aynı anda başlaması ve bitmesi gerektiği anlamına gelir ve birincil ve ikincil için aynı kaynağı engelleyecek `NotOnSameResource` sınırlamaları vardır.

Kaynak miktarının 3 olarak ayarlandığı 20 operasyonu için, işleme işi tüm işlerin tam olarak aynı anda çalışması gereken üç ayrı işe bölünmüştür.
Bu durumda, rota grubu saatlerden sonra kuyruk için kapasiteyi rezerve etmemek üzere ayarlanmıştır, bu nedenle sonrasında kuyruk için tek bir iş vardır.

Planlama altyapısı yalnızca iş kavramlarını anlar ve operasyon kavramı yoktur. Bu, operasyon planlaması yapılırken veritabanında kalıcı olmayacak olmasına rağmen operasyonların projelere bölüneceği anlamına gelir.

Her iş için, proje kapasitesi gereksiniminin (gerekli olan saniye sayısı) ne olduğunu da tanımlayacağız. Kaynak gereksinimlerinin nasıl tanımlandığına bağlı olarak, her iş için, işin çalıştırabileceği tüm olası kaynakların listesini ve bu belirli bir kaynak için kapasite gereksinimini gönderebiliriz. Model oluşturulurken uygulanabilir kaynaklar listesi gönderilse bile altyapının kaynak atamasının tüm iş süresi için geçerli olmasını sağlamaya devam etmesi gerekecektir.

## <a name="scheduling-engine-internals"></a>Planlama altyapısı iç yapıları

### <a name="scheduling-engine-interface"></a>Planlama altyapısı arabirimi

Altyapının dahili olarak nasıl çalıştığı hakkında bir fikir almak için, dışarıdan sağladığı işleve bakmak en iyi yoldur. X++ içinde, ana arabirim şudur: `WrkCtrSchedulerEngineInterface`. Aşağıdaki alt bölümlerde açıklanan yöntemlere sahiptir.

#### <a name="general-engine"></a>Genel altyapı

| **Yöntem** | **Amaç** |
| --- | --- |
| `run` | Tüm yüklü işleri zamanlar ve hata kodunu döndürür. |
| `getJobSchedulingSequenceResult` | Belirli bir iş tarafından tanımlanan sıraya göre planlama sonucunu ve ilk hata işini alır. |
| `validateJobCapacityReservations` | Altyapı tarafından depolanan tüm işlerin kapasite rezervasyonlarını doğrular. |
| `setReservationsTimeStamp` | Altyapının önbelleğindeki planlanmış işler için tüm yeni kapasite rezervasyonlarında ayarlanan alt yapıya bir zaman damgası gönderir. |
| `addPropertyToGroupAggregation` | Kapasite toplandığında kullanılan özellikler kümesine özellik öneki ekler. |
| `addResource` | Planlama altyapısı kaynak havuzuna kaynak ekler. |
| `addResourceGroup` | Planlama altyapısı kaynak grubu havuzuna kaynak grubu ekler. |
| `addResourceGroupMembership` | Kaynak grubuna üye olarak kaynak ekler. |
| `addOptimizationGoal` | Planlamayı en iyi duruma getirme hedefi ekler (süre veya öncelik). |

#### <a name="individual-jobs"></a>Bireysel işler

| **Yöntem** | **Amaç** |
| --- | --- |
| `addJobInfo` | Altyapıyı planlanması gereken bir iş hakkında bilgilendiren iş bilgileri kaydı ekler. |
| `addConstraintJobEndsAt` | Bir işin belirtilen tarih ve saatte bitmesi gereken bir sınırlama ekler. |
| `addConstraintJobStartsAt` | Bir işin belirtilen tarih ve saatte başlaması gereken bir sınırlama ekler. |
| `addConstraintMaxJobDays` | Bir işin, belirtilen maksimum gün sayısına yayılabileceği kısıtlamayı tanımlar. |
| `addConstraintResourceRequirement` | İşin belirli bir kaynakta planlanmasını gerektiren kısıtlamayı ekler. |
| `addJobBindPriority` | Bir (iş, sınırlama düzeyi) çifti için iş bağlama önceliği ekler. Yüksek öncelik değeri, iş değişkenlerinin daha önce bağlanacağı anlamına gelir. İş, aynı sıradaki düşük öncelik değerine sahip işlerden önce işlenecektir. |
| `addJobCapacity` | İşin çalıştığı kaynaktan bağımsız olarak bir iş (gerekli iş çalışma zamanı gibi) için kapasite yükü bilgilerini ekler. |
| `addJobResourceCapacity` | Bir kaynağı, bir işi gerçekleştirmek için kullanılabilecek kaynaklar kümesine ekler ve o kaynakta çalışırken gereken kapasiteyi belirtir. |
| `addJobGoal` | Belirli bir sınırlama düzeyi için (en erken bitiş saati veya en geç başlangıç saati) iş hedefi bilgileri ekler. |
| `addJobResourcePriority` | Bir kaynak üzerinde bir iş zamanlandığında kullanılacak önceliği ekler. |
| `addJobResourceRuntime` | İşin planlandığı kaynağa bağlı iş süresini belirtir. |
| `addJobRuntime` | İşin planlanacağı kaynaktan bağımsız iş süresini belirtir. |
| `scheduleJobOnResourceGroup` | İşi, kaynak grubu düzeyinde planlama için işaretler. |
| `setJobResourcePreemptionAllowed` | Bir kaynaktaki bir iş için önalım izni verilip verilmediğini ayarlar (altyapının, işi bitişik olmayan kapasite yuvalarında planlamasına izin veriliyorsa). |
| `setRequiredNumberOfResources` | Bir işi planlamak için gereken kaynak sayısını ayarlar (yalnızca operasyonlar planlama için). |

#### <a name="constraints-between-jobs"></a>İşler arasındaki sınırlamalar

| **Yöntem** | **Amaç** |
| --- | --- |
| `addJobLink` | İki iş arasına bir bağlantı (bitiş\>başlangıç gibi) ekler. |
| `addConstraintEndsDelayed` | Bir işin, başka işler bitmeden önce artı bazı gecikme süresiyle sona eremeyeceği kısıtlamasını tanımlar. |
| `addConstraintJobListWorkingTimeIntersect` | İşler için ayrılan kapasite yuvalarının, işler tarafından kullanılan iki kaynak için kesişen çalışma saatlerinde olması gerektiğini belirten bir sınırlama ekler. |
| `addConstraintJobOverlap` | İlk kaynak hala işlemeyi bitirmemişken ikinci kaynağın işlemeye başlayabilmesi için maddenin belirtilen miktarı iki kaynak arasında taşınabildiğinde işlerin nasıl sıralanacağını tanımlayan bir kısıtlama ekleyin. |
| `addConstraintNotOnSameResource` | Aynı kaynak üzerinde iki işin planlanmaması için bir sınırlama ekler. |
| `addConstraintOnSameResource` | İki işin aynı kaynağı kullanması gerektiği konusunda bir kısıtlama ekler. |
| `addJobSameReservations` | Bir işin, birincil işle aynı zaman aralıkları için kapasite rezervasyonları olmasını gerektiren bir sınırlama ekler. |
| `setPrimaryParallelJob` | Bir paralel işler kümesindeki hangi işin birincil iş olduğu hakkında bilgiler ekler. |

### <a name="solver"></a>Çözücü

Altyapının kendisi aslında özel buluşsal yöntemler eklenmiş özelleştirilmiş bir sınırlama çözücü altyapısıdır. Çözücü iki ana öğeye dayanır: değişkenler ve sınırlamalar.

#### <a name="variable"></a>Değişken

Değişken, olası değerlerin etki alanını gösterir. Zamanlama altyapısında iki tür değişken vardır:

- **Tarih Saat değişkeni** - Tüm tarih ve zamanların bir etki alanı vardır ve etki alanı değişken zamanı için alt ve üst sınırı birbirlerine yaklaştırarak kısıtlanabilir.
- **Kaynak değişkeni** - İlgili kaynakların bir etki alanını vardır ve etki alanı listeden kaynakları kaldırarak kısıtlanabilir.

#### <a name="constraint"></a>Sınırlama

Sınırlama, etki alanlarını sınırlayarak değişkenler üzerinde etki eder ancak değişkenlere de bağlıdır ve değişkenler değiştiğinde etkinleşir. "Kısıtlama yayılması" işlemi, bir kısıtlamanın ana işlevini gerçekleştirmesi ve başarılı olursa ana mantığa bildirimde bulunmasıdır.

Bir değişken, daha sonra kısıtlanamıyorsa sınırlı olarak kabul edilir; bu durumda, Tarih Saat değişkeni üst ve alt sınırı aynı olur ve Kaynak değişkeninin tek bir uygulanabilir kaynağı bulunur. Tüm değişkenler sınırlandığında bir çözüm bulunur.

### <a name="constraint-levels"></a>Sınırlama düzeyleri

Planlama, malzeme gereksinimleri planlamasını (MRP) karşılama aşamasının bir parçası olarak yürütüldüğünde, siparişler gereksinim tarihinden geriye doğru planlanacaktır. Ancak, bugün veya sonraki bir tarihte başlayan ve gereksinim tarihinden önce sona eren bir plan bulmak mümkün değilse, planlama yönü bugünden ileriye doğru değişecektir.

Bu ana iş kuralı, düzeylerdeki sınırlamalar düzenlenerek gerçekleştirilir. En yüksek düzeydeki sınırlamaları kullanırken çözüm bulunamazsa, o düzeydeki kısıtlamalar tümüyle bırakılır ve alt düzey denenir. Uygulamada, bu geriye dönük planlama için modelin maksimum sona erme süresi kısıtlaması (gereksinim tarihi) nedeniyle en geç başlangıç tarihli iş hedefleriyle düzey 1 ve en erken bitiş tarihi ve bugün itibarıyla minimum başlama zamanı kısıtlaması olan iş hedefleriyle düzey 0 içereceği anlamına gelir.

### <a name="algorithm"></a>Algoritma

Altyapı algoritmasının başlıca adımları şunlardır:

1. Ayrı olarak çözülebilecek sıraları (iş zincirleri) bulun.
1. En yüksek kısıtlama düzeyi için sıraya yönelik bir başlangıç çözümü bulmaya çalışın.
    1. Sıradaki işleri, iş hedefini ve öncelikleri temel alarak sıralayın; böylece bir başlangıç işi bulunabilir.
    1. İşleri aşağıdaki sırada döngüye alın:
        1. Yayılması ve yayılım çalıştırması gereken tüm kısıtlamaları bulun.
        1. İşle ilgili tüm değişkenler sınırlanmışsa, o iş için çözüm bulunmuştur.
        1. Değişkenlerden biri, kısıtlamaları ihlal etmeden sınırlandırılamadıysa, değişken bağlamasın geri alın, etki alanında farklı bir değer deneyin (kaynak değişkeni için) ve kısıtlama yaymayı yeniden çalıştırın.
1. Çözüm bulunamazsa, geçerli kısıtlama düzeyindeki tüm kısıtlamalar kaldırılır, kısıtlama düzeyi düşürülür (alt düzeyler varsa) ve çözüm araması yeni sınırlama kümesiyle yeniden denenir.
1. Uygulanabilir bir çözüm bulunursa, en iyi duruma getirme zaman aşımına ulaşılana veya tüm kaynak kombinasyonları tükenene kadar daha iyi bir çözüm bulmaya çalışacak en iyi duruma getirme aşaması başlatılır.

Kısıtlama çözücü, planlama algoritmasının özelliklerini bilmez. İşlemin "sihirli" tarafı çeşitli kısıtlamaların tanımında ve birleşimindedir.

### <a name="determining-working-times"></a>Çalışma zamanlarını belirleme

Altyapıdaki (dahili) kısıtlamaların büyük bir bölümü bir kaynağın çalışma süresini ve kapasitesini denetler. Esas olarak görev, bir kaynak için çalışma zamanı aralıklarını belirli bir noktadan belirli bir yöne geçirmek ve iş için gerekli olan kapasitenin (saat) uygun olacağı yeterince uzun bir zaman aralığı bulmaktır.

Bunu yapmak için, altyapının bir kaynağın çalışma saatlerini bilmesi gerekir. Ana model verilerinin tersine çalışma süreleri *yavaş yüklenir*, diğer deyişle altyapıya gerektiğinde yüklenir. Bu yaklaşımın nedeni, genellikle Supply Chain Management'ta çok uzun süreli bir takvim çalışma sürelerinin olması ve genellikle birçok takvimin bulunması ve buna bağlı olarak verilerin önceden yükleme için oldukça fazla olmasıdır.

Takvim bilgileri, altyapı tarafından X++ sınıfı yöntemi `WrkCtrSchedulingInteropDataProvider.getWorkingTimes` çağrılarak öbekler halinde istenir. İstek, belirli bir zaman aralığındaki belirli bir takvim kodu için yapılır. Supply Chain Management'daki sunucu önbelleğinin durumuna bağlı olarak, bu isteklerin her biri uzun süren (saf bilgi işlem zamanına göre) birkaç veritabanı çağrısıyla sonlanabilir. Ayrıca, takvimde gün başına birçok çalışma zamanı aralığı içeren çok ayrıntılı çalışma zamanı tanımları varsa bu, yükleme süresine eklenir.

Çalışma zamanı verileri zamanlama altyapısına yüklendiğinde, belirli bir takvim için dahili önbelleğinde korunur (başka işler veya kaynaklar aynı takvimi kullanıyorsa, sonraki aramalar bellekten hızlı bir şekilde gerçekleştirilebilir.) Performans zayıflığının yaygın bir nedeni, her bir kaynak için ayrı bir takvim kodu kullanılmasıdır; çünkü bu takvimlerin içeriği aynı olsa bile, her bir takvim için bir verilerin istenmesi gerekir.

### <a name="finite-capacity"></a>Sınırlı kapasite

Sınırlı kapasite kullanılırken, takvimdeki çalışma zamanı aralıkları varolan kapasite rezervasyonlarına göre bölünür ve azaltılır. Bu rezervasyonlar aynı zamanda takvimlerle aynı `WrkCtrSchedulingInteropDataProvider` sınıfı üzerinden getirilir ancak bunun yerine `getCapacityReservations` yöntemi kullanılır. Master planlama sırasında planlama yapılırken, belirli bir ana planın rezervasyonları dikkate alınır ve **Master planlama parametreleri** sayfasında etkinse, kesinleştirilmiş üretim emirlerinden alınan rezervasyonlar da dahil edilir. Benzer şekilde, bir üretim emri zamanlarken, diğer yol kadar yaygın kullanılmasa da mevcut planlı siparişlerden rezervasyonlar dahil etme seçeneği de vardır.

Sınırlı kapasitenin kullanılması, birkaç nedenden dolayı zamanlamanın daha uzun sürmesine neden olur:

- Kapasite bilgilerinin veritabanından getirilmesi yavaş bir işlemdir ve kapasite bilgilerinin sunucu tarafında önbelleğe alınması genellikle, çalışma süreleri kadar iyi değildir, çünkü bunlar takvimler gibi kaynaklar arasında paylaşılmaz.
- Bölmeler nedeniyle geçiş yapılacak çalışma zamanı aralıklarının sayısı artar ve çözüm bulunmadan önce daha uzun süreli aralıkların araştırılması gerekir.
- Zamanlama tamamlandıktan sonra, çakışan rezervasyonlar için bir denetim gerçekleştirilmelidir (ayrıntılar için "Zmanlama altyapılarını paralel çalıştırma" bölümüne bakın).

### <a name="examining-the-resource-combinations"></a>Kaynak birleşimlerini inceleme

İş sırası yalnızca standart `FinishStart` bağlantıları içeriyorsa, yani herhangi bir dal içermeyen basit bir zincir şeklinde oluşuyorsa, ilk iş için en iyi çözümü bulup bir sonraki iş için en iyi çözümü bulmaya geçerek en uygun sonuç (tek bir sipariş için, siparişler arasında değil) elde edilebilir. Bir iş için en iyi çözüm, kısıtlamalara uygun olarak iş hedefine en yakın iş başlangıç ve bitiş tarihini elde edebilecek kaynağı bulmak anlamına gelir (ileriye doğru planlamada, işin bitiş tarihini mümkün olan en erken tarihe almak anlamına gelir).

Paralel işler olduğunda, çözüm bulmak farklı kaynak birleşimlerini incelemeyi gerektirebilir. Olası kaynak birleşimlerinin sayısı, bağlı olan paralel işler için uygun kaynak sayısı ürünüdür. Özellikle de gereksinim tarihinden geriye doğru sipariş zamanlarken, sonuç verebilecek daha yüksek verimliliğe sahip kaynakların tüm kombinasyonlarını veya farklı bir takvimi denetlemesi gerektiğinden mantığın bugünün tarihinden öncesine uyan paralel işler yapacak soruna bir çözüm olmadığını belirlemesi biraz uzun sürebilir. Bu, zaman aşımı sınırı ayarlanmazsa, yönü ileriye doğru değiştirmeden önce uzun bir süre çalışacağı anlamına gelir.

Bu kombinasyon mantığı, daha fazla uygun kaynak eklemenin altyapının daha yavaş çalışmasına neden olabileceği anlamına gelir. Paralel işlemler olduğunda ve sonsuz kapasiteyle zamanlama yaparken performans sorunları oluşursa, bu sorun yönlendirme tasarımcısının hangi kaynağın kullanılması gerektiğini belirlemesi ve sonra kaynağı doğrudan işleme atamasıyla kısmen düzeltilebilir (çünkü çoğu durumda altyapı her zaman aynı kaynağı çekecek ve nihai sonuç aynı olacaktır).

### <a name="hard-links"></a>Sabit bağlantılar

İki iş arasında bağlantı türünü sabit olarak ayarlamak, bir işin bitişi ile bir sonraki bir projenin başlangıcı arasında zaman aralığı olmamasını sağlar. Bu, örneğin metalin bir iş için ısıtıldığı ve sonraki işte işlendiği ve bunların işler arasında metalin soğumasının istenmediği senaryolarda yararlıdır.

Standart sembolik bağlantılar ve ileriye doğru planlamayla, rota dal içermeyen basit bir zincir oluşturuyorsa, kendi kısıtlamalarını karşılayan ilk iş için bir çözüm bulup bitiş zamanını önceki işten sonraki işe yayan zincirde ilerleyerek bir çözüm bulunabilir. Geçerli iş herhangi bir kapasite bulamazsa, potansiyel olarak işler arasında boşluk oluşturan önceki işler için herhangi bir sonuç doğrumadan söz konu işin başlangıç tarihi ileriye taşınabilir. Ancak, sabit bağlantılarla (özellikle sınırlı kapasiteyle bağlantılı olarak) aynı senaryo için, zincirdeki bir işin daha sonra kapasite bulamaması durumu, planlanmış önceki tüm işlerin tek tek "sürüklenmesi" ve birçok kez yeniden zamanlanması anlamına gelecektir. Özellikle birden çok kaynak için yüksek yük içeren senaryolarda, sabit bağlantılar işlerin birbirini etkileyeceği bir zincir reaksiyona neden olabilir ve ve sonucun uygun zamanlamaya uygun hale gelebilmesi için bir dizi tekrarın gerçekleştirilmesi gerekebilir.

## <a name="running-scheduling-engines-in-parallel"></a>Zamanlama altyapılarını paralel çalıştırma

Yardımcıları kullanıldığı master planlama çalıştırmasının bir parçası olarak planlama yapılırken, Master planlama yardımcısı iş parçacıklarının her biri üretim emri planlama görevlerini de alabilir. Bu, birden çok planlama altyapısının aynı anda çalışabileceği anlamına gelir. Genel olarak çoklu iş parçacığı kullanımı çok önemli bir performans avantajı olmakla birlikte, zamanlama söz konusu olduğunda bazı işlevsel olumsuz yanları da vardır.

MRP'de, belirli bir ürün reçetesi (BOM) düzeyi için tüm üretim emirleri gereksinim tarihi sırasına göre zamanlanır, bu da en erken gereksinim tarihine sahip siparişlerin önce zamanlanabilmesi ve böylece kullanılabilir kaynak kapasitesini elde etmek için en yüksek şansa sahip olması anlamına gelir. Ancak, birden çok alt yapısının zamanlanmamış siparişler listesinden çekme işlemi yapması durumunda, biri diğerinden daha hızlı tamamlanbileceğinden, sıra artık kesin değildir.

Ayrıca, sınırlı kapasite kullanılarak planlama yapıldığında ve birden çok altyapı örneği potansiyel olarak aynı anda aynı kaynakları kullanan siparişleri zamanlamaya çalışırken, bir yarış durumu oluşabilir. Bu tür yarış durumlarının sayısı ana planlar geçmişi sayfasındaki **Zamanlama çakışmaları** alanına kaydedilir. Çakışma çözümü mantığı aşağıdaki gibidir:

- Bir sipariş (kilitli-serbest) zamanlayın ve kapasite rezervasyonlarını alın.
- Kilidi alın.
- Zaman aralığı içindeki zamanlanan kaynaklar için yeni kapasite rezervasyonlarının mevcut olup olmadığını denetleyin.
  - Yoksa, kapasiteyi yazın ve kilidi serbest bırakın.
  - Varsa, kilidi bırakın ve siparişi baştan başlayarak yeniden zamanlayın.

Böylece, birden çok altyapı örneğiyle planlama yapılırken, sonuç tam olarak belirleyici değildir çünkü iş parçacıklarının her birinin zamanlamasına bağlıdır.

## <a name="operation-scheduling-performance"></a>Operasyon planlama performansı

Operasyon planlamaları aynı zamanda kabaca kapasite planlaması olarak da bilinse de, altyapı açısından bakıldığında, olasılığın belirlenmesi için daha fazla veri gerekli olduğundan, sınırlı kapasite kullanılıyorsa çözümü daha zor bir problem olabilir.

Kaynak grubunun kapasitesi, kaç kaynağın kaynak grubunun üyesi olduğuna bağlıdır. Bir kaynak grubunun kendisinin kapasitesi yoktur&mdash;yalnızca kaynaklar gruba üye olduğunda kapasiteye sahip olur. Kaynak grubu üyeliği zaman içinde değişebileceğinden, kapasite her gün için değerlendirilmelidir.

Operasyon planlamasında, kaynak grubunun takvimi her operasyonun başlangıç ve bitiş saatlerini belirlemek için kullanılır. Bu, kaynak grubu takviminin bir tek günde bir kaynak grubunda bir operasyon için operasyonların kaç kez zamanlanabileceğine sınır koyacağı anlamına gelir. Belirli kaynaklara ilişkin takvimin tersine, kaynak grubu için takvimin verimlilik verileri gerçek kapasiteyi değil yalnızca açılış saatlerini belirttiği için dikkate alınmaz.

Örneğin, belirli bir tarihteki bir kaynak grubu için çalışma zamanı 8:00-16:00 arasında ise, bir operasyon kaynak grubuna o gündeki toplam kullanılabilir kapasite miktarına bakılmaksızın 8 saate sığabilecek daha azla yük koyabilir. Ancak, kullanılabilir kapasite yükü daha fazla sınırlayabilir.

Belirli bir gündeki kaynak grubuna dahil edilen tüm kaynaklardaki iş planlamadan alınan yük, aynı gün içindeki kaynak grubunun kullanılabilir kapasitesi hesaplanırken dikkate alınır. Her tarih için hesaplama şu şekilde yapılır:

*Kullanılabilir kaynak grubu kapasitesi = Gruptaki kaynakların takvimlerine göre kapasitesi &ndash; Gruptaki kaynaklar üzerinde planlanan iş yükü &ndash; gruptaki kaynaklar üzerinde planlanan operasyon yükü &ndash; kaynak grubu üzerinde planlanan operasyon yükü*

Rota operasyonunun **Kaynak gereksinimleri** sekmesinde, kaynak gereksinimleri belirli bir kaynak kullanılarak (bu durumda operasyon söz konusu kaynak kullanılarak planlanır), bir kaynak grubu, bir kaynak türü veya bir ya da daha fazla yetenek, beceri, kurs veya sertifika ile ilgili olarak belirtilebilir. Bu seçeneklerin tümünün kullanılması, rota tasarımında büyük bir esneklik sağlar, ayrıca kapasite "özellik" başına (yetenek, beceri, vb. için altyapıda kullanılan soyut ad) dikkate alınacağından planlamayı karmaşıklaştırır.

Bir yetenek için kaynak grubu kapasitesi, kaynak grubunda söz konusu yeteneğe sahip tüm kaynakların kapasitesinin toplamıdır. Gruptaki bir kaynak bir özelliğe sahip ise, kapasitenin hangi düzeyde olması gerektiğine bakılmaksızın dikkate alınır.

Operasyon planlamasında, bir kaynak grubuna ilişkin belirli bir yetenek için kullanılabilen kapasite, söz konusu yeteneğe gereksinim duyan bir operasyonla yüklendiğinde azaltılır. Operasyon birden fazla yetenek gerektiriyorsa, gerekli tüm yetenekler için kapasite azaltılır.

Her tarih için gerekli hesaplama şu şekilde yapılır:

*Bir yetenek için kullanılabilir kapasite = Yetenek için kapasite &ndash; Kaynak grubu dahil edilen belirli bir yeteneğe sahip kaynaklar üzerinde planlanan iş yükü &ndash; Kaynak grubuna dahil edilen belirli bir yeteneğe sahip kaynaklar üzerinde planlanan operasyon yükü &ndash; Belirli bir yeteneği gerektiren kaynak grubunun kendisi üzerinde planlanan operasyon yükü*

Bu, belirli bir kaynakta yük varsa, yükün yetenek için kaynak grubundaki kullanılabilir kapasite hesaplamasında dikkate alınacağı anlamına gelir çünkü belirli bir kaynaktaki yük kaynağın kaynak grubu kapasitesine katkısını (belirli kaynaktaki yükün bu belirli yetenek için olup olmadığına bakılmaksızın) azaltır. Kaynak grubu düzeyinde yük varsa, yalnızca yükün belirli bir yeteneği gerektiren bir operasyonla ilgili olması durumunda, kaynak grubunun yetenek başına kullanılabilir kapasitesini hesaplamada dikkate alınır.

Yukarıdaki mantık her "özellik" türü için aynı olduğundan karmaşıktır bu nedenle sınırlı kapasiteli operasyon zamanlamasını kullanmak için önemli miktarda veri yüklenmesi gerekir.

## <a name="viewing-scheduling-engine-input-and-output"></a>Planlama alt yapısı giriş ve çıkışını görüntüleme

Planlama sürecinin giriş ve çıkışıyla ilgili özel ayrıntılar almak için, **Kuruluş Yönetimi \> Kurulum \> Planlama \> Planlama izleme kokpiti**'ni kullanarak günlük kaydını etkinleştirin.

Bu sayfada, önce Eylem bölmesinde **Günlük kaydını etkinleştir**'i seçin. Ardından, üretim emri için planlamayı çalıştırın. Tamamlandığında, **Planlama izleme kokpiti** sayfasına geri dönün ve Eylem bölmesinde **Günlük kaydını devre dışı bırak**'ı seçin. Sayfayı yenileyin; ızgarada yeni bir satır görüntülenir. Yeni satırı ve ardından Eylem Bölmesinde **İndir**'i seçin. Bu size, aşağıdaki dosyaları içeren .zip ile sıkıştırılmış bir klasör verecektir:

- **Log.txt** - Bu, altyapının geçtiği adımları açıklayan günlük dosyasıdır. Çok ayrıntılı ve bunaltıcı olabilir, ancak performans sorunlarını çözmede izlenecek yolun bir parçası olarak kullanıldığında, ilk bakılacak olan ilk ve son satır arasındaki farktır çünkü bu değer planlayıcının harcadığı toplam süreyi belirtir.
- **XmlModel.xml** - X++ içinde oluşturulan ve altyapının üzerinde işlem yaptığı modeli içerir. Dosyada kullanılan `JobId` işleri içeren kaynak tablodan alınan `RecId` ile ilişkilidir (`ReqRouteJob` veya `ProdRouteJob`). Bu dosyada aranacak tipik şey, `ConstraintJobStartsAt` ve `ConstraintJobEndsAt` içindeki tarihlerin beklendiği gibi olup olmadığı, `JobGoal` özelliğin doğru şekilde ayarlandığı ve işlerin `JobLink` kısıtlamaları üzerinden birbirleriyle ilişkili olduğudur.
- **XmlSlots.xml** - Bu, alt yapının istediği tüm çalışma zamanlarını ve kapasite rezervasyonlarını içerir. Takvim çalışma zamanları ve rezervasyonlar altyapı tarafından yalnızca, işleri (ve fazladan bir arabelleği) yerleştirmeye çalıştığı dönemler için istenecektir, bu nedenle dosya gelecekteki zamanları içeriyorsa bu, kurulumla ilgili bir sorun göstergesi olabilir. `ResourceProperty` düğümleri, her kaynak için hangi kaynak grubu ve yeteneklerin hangi dönemlerle ilişkili olduğunu gösterir.
- **Result.xml** - Planlama çalıştırma işleminin sonucu içerir.

İzleme işlevinin önemli performans yükü ekleyebileceğini, bu nedenle yalnızca belirli siparişlerin planlanmasında denetimli bir şekilde kullanılması gerektiğini unutmayın. Bir master planlama sırasında açık olduğunda, boyut sınırına hızlı bir şekilde ulaşıp durur.

## <a name="troubleshooting-performance"></a>Performans sorununu giderme

Önceki bölümlerin tümünden anlaşılabileceği gibi, planlama altyapısının kurulum ve kullanımı söz konusu olduğunda, performans sorunlarına yol açabilecek bazı ayarlar da vardır. Bu tür sorunları gidermek için aşağıdaki onay listesi kullanılabilir. Tüm noktalara bakmak önemlidir, çünkü genellikle sorunlara bir çok etkenin birleşimi yol açar.

### <a name="performing-scheduling-as-part-of-mrp-when-it-is-not-needed"></a>Gerekli olmadığında MRP'nin parçası olarak planlama gerçekleştirme

Rotalar, maliyet ve raporlama gibi üretim denetleme amaçlarıyla kullanılsa da, MRP sırasında bunları dikkate almak gerekli olmayabilir. Bazı durumlarda, madde için standart üretim sağlama süresine sahip olmak, planlama için yeterli olacaktır. Rota planlamasını kapatmak için, kapasite zaman aralığını sıfıra ayarlayın. Planlamanın gerçekleştirilmesi gerekiyorsa, kapasite zaman aralığı dikkatli şekilde ayarlanmalıdır çünkü rotaların tüm MRP karşılama zaman diliminin tam kapsamı için dikkate alınması gerekli olmayabilir.

Sipariş MRP sırasında planlanmazsa, bunun yerine planlanan sipariş kesinleştirildiğinde planlanması gerekir. Bu da, kesinleştirme sürecinin daha uzun sürmesi anlamına gelir ve böylece önerilen planlı siparişlerin kaçının kesinleştirileceğine bağlı olarak MRP sırasındaki performans kazancının kesinleştirmede kaybedilmesine neden olur.

### <a name="route-with-unnecessary-operations"></a>Gereksiz operasyonlar içeren rota

Rotayı tasarlarken, üretimin gittiği tüm adımlarla gerçek dünyanın tam olarak modellenmesi gerekir. Bazı durumlarda yararlı olmakla birlikte, işin ve kapasite rezervasyonlarının eklenmesi ve güncelleştirilmesi için altyapının (hem işler hem de sınırlamalar açısından) daha fazla çalışması ve daha fazla SQL deyimi yürütülmesini gerektiren bir model olduğundan performans için iyi değildir. Ayrıca, işleri devam etmek zorunda olan, otomatik nakiller için de etkileri olan ilerlemeyi raporlamak zorunda olan bir aşağı akış etkisi vardır. Veriler herhangi bir işlem için kullanılmıyorsa, gereksiz yük oluşturur.

Yalnızca planlama (genellikle darboğaz kaynakları olacaktır) ve/veya maliyetlendirme amacıyla için kesinlikle gerekli olan operasyonları oluşturmanız önerilir. Alternatif olarak, birçok küçük farklı işlemi, sürecin daha büyük bir bölümünü temsil eden daha büyük operasyonda gruplamanız gerekebilir.

### <a name="many-applicable-resources-for-an-operation"></a>Bir operasyon için çok fazla uygulanabilir kaynak

Bir operasyon için uygulanabilir kaynak sayısı, operasyon ilişkisinde ayarlanan kaynak gereksinimleri ile belirlenir. Gereksinim belirli bir (birey) kaynak için olabilir veya kaynağın bir kaynak grubu veya yeteneğe ait üyeliğini temel alabilir.

Sınırlı kapasite kullanılarak planlama yapılmadıysa ve ilgili tüm kaynaklar aynı takvime ve verimliliğe sahipse, iş planlama altyapısı her zaman bir operasyon için aynı kaynağı çekecektir ancak bunu yapmadan önce diğerlerinden "daha iyi" bir kaynak olup olmadığını belirlemek için tüm uygun kaynakları denetleyecektir. Bu durumda, planlama yükü, rota tasarımı sırasında operasyona her zaman belirli bir kaynağı atayarak büyük ölçüde azaltılabilir.

### <a name="route-with-parallel-operations"></a>Paralel operasyonlar bulunan rota

Paralel operasyonlar (birincil/ikincil), belirli bir görevi gerçekleştirmek için bir makine ve operatörün gerekli olduğu durumlar için senaryo modelleme açısından güçlü bir araçtır, ayrıca birçok performans sorununa da kaynak olur. Belirli bir kaynağa ilişkin gereksinim hem birincil hem de ikincil operasyona atanırsa, bu genellikle sorun değildir. Ancak, operasyonların her biri için birçok olası kaynak varsa, planlamaya önemli hesaplama karmaşıklığı eklenir.

Paralel operasyonları kullanmaya alternatif olarak, çiftler "sanal" kaynaklar olarak modellenebilir (daha sonra operasyon için her zaman birlikte geçen bir takımı temsil edecektir) veya bir dar boğazı temsil etmiyorsa operasyonlardan biri modellenmeyebilir.

### <a name="route-with-quantity-of-resources-higher-than-1"></a>Kaynak miktarı 1'den yüksek olan rotalar

Operasyon için 1'den yüksek olan kaynak miktarını ayarlamak gerekiyorsa, altyapıya birden fazla paralel gönderildiği için birincil/ikincil operasyonları kullanmayla aynı sonuç elde edilir. Ancak, bu durumda belirli kaynak atamalarını kullanma seçeneği yoktur, çünkü birden yüksek bir miktar, operasyon için birden fazla kaynağın uygun olmasını gerektirir.

### <a name="excessive-use-of-finite-capacity"></a>Sınırlı kapasitenin aşırı kullanımı

Sınırlı kapasitenin kullanılması, altyapının bir veritabanındaki kapasite bilgilerini yüklemesini gerektirir ve özellikle kaynakların maksimum kapasitesine yakın olarak ayrıldığı ortamlarda, bir çözümü bulmak daha zor olacağından aşırı bilgi işleme yükü olabilir. Sonuç olarak, bir kaynağın sınırlı kapasite kullanmasının gerçekten gerekli olup olmadığının veya kapasitesi üzerinde rezerve edilip edilemeyeceğinin dikkatle değerlendirilmesi önemlidir. Sınırlı kapasite kaynakları arasında kapasiteleri üzerine rezerve edilmemeleri açısından önemli bir fark olabileceğinden, "Darboğaz kaynakları için kapasite zaman aralığı" içinde yer alan planda ayrı bir değerle birlikte kullanmanızı öneririz. Darboğaz kavramı kullanmak, genel sınırlı kapasite zaman diliminin düşürülebilmesini sağlayabilir.

### <a name="setting-hard-links"></a>Sabit bağlantılar ayarlama

Rotanın standart bağlantı türü *esnek* bağlantıdır yani bir operasyonun bitiş zamanı ile diğerinin başlangıcı arasında zaman aralığı olmasına izin verilir. Buna izin verilmesi, malzeme veya kapasite operasyonlardan biri için çok uzun süre kullanılabilir olmadığında, üretimin bir süre boşta kalmasına ve ilerlemede olası iş artışlarına yol açabilir. Bitiş ve başlangıçın tamamen uyumlu olması gerektiğinden, bu durum sabit bağlantılarla gerçekleşmeyecektir. Ancak, sabit bağlantılar ayarlamak, operasyonlardaki iki kaynak için çalışma süresi ve kapasite kesişmelerinin hesaplanması gerektiğinden, zamanlama sorununu daha zor hale getirir. Ayrıca, dahil edilen paralel operasyonlar varsa, bu önemli bir bilgi işleme süresi ekler. İki operasyonun kaynaklarının hiç çakışmayan farklı takvimleri varsa, sorunun çözülemez duruma gelir.

Sabit bağlantıları yalnızca kesin olarak gerekli olduğunda kullanmanızı ve rotanın her operasyonu için gerekli olup olduğunu dikkatlice değerlendirmenizi öneririz.

Sabit bağlantıları uygulamadan devam eden işi azaltmak için, siparişi ikinci geçişte ters yönde olacak şekilde ikinci kez planlanabilir. İlk planlama teslimat tarihinden geriye doğru yapıldıysa, ikincisi planlama başlangıç tarihinden ileriye doğru yapılmalıdır. Bu, işlerin mümkün olduğunca sıkıştırılmasına ve ilerleyen işin minimuma indirilmesine yol açar.

### <a name="separate-calendar-for-each-resource"></a>Her kaynak için ayrı takvim

Zamanlama alt yapısının ana veri kaynaklarından biri, veritabanından yüklenmesi pahalı olabilecek takvim bilgileridir. Takvimler şablon temel alınarak oluşturulduğundan, her bir kaynak için bir takvim oluşturmak, sonra da kaynakta kesinti ve diğer sorunlar olduğunda bu takvimdeki bilgileri ayarlamak amacıyla kullanılabilir. Ancak bunu yaparsanız, her kaynak için yeni veri istemesi gerekeceğinden altyapının takvim verilerini önbelleğe alma yeteneği ciddi şekilde sınırlanır ve performans sorunları açısından büyük bir kaynağı oluşturabilir. Bunun yerine, takvimleri kaynaklar arasında olabildiğince yeniden kullanmanızı ve bir dönem için farklı bir takvim kodu atayarak kesinti süresini denetlemenizi öneririz.

### <a name="high-number-of-working-time-slots-per-calendar-day"></a>Takvim günü başına yüksek çalışma zamanı aralığı sayısı

Altyapı, zaman dilimlerini kapasite için tek tek inceleyerek çalıştığı için, takvim günü başına zaman dilimi sayısını en aza indirmek yararlıdır. Bu işlem, örneğin, sonuçta elde edilen planlamanın çalışanların her saat 5 dakikalık bir molası olduğunu yansıtmasının önemli olup olmadığı göz önünde bulundurularak yapılabilir.

### <a name="large-or-none-scheduling-timeouts"></a>Büyük (veya hiç) planlama zaman aşımları

Zamanlama altyapısı performansı, **Planlama parametreleri** sayfasında bulunan parametreler kullanılarak en iyi duruma getirilebilir. **Planlama zaman aşımı etkin** ve **Planlamayı en iyi duruma getirme zaman aşımı etkin** ayarları her zaman **Evet** olarak ayarlanmalıdır. **Hayır** olarak ayarlanırsa, çok fazla seçenek içeren gerçekleştirilemeyecek bir rota oluşturulduğunda planlama potansiyel olarak sonsuz çalışabilir. 

**Sıra başına maksimum planlama zamanı** değeri tek bir sıra için (çoğu zaman bir sıra tek bir siparişe karşılık gelir) çözüm bulmak üzere en fazla kaç saniye harcanacağını denetler. Burada kullanılacak değer rotanın karmaşıklığına ve sınırlı kapasite gibi ayarlara bağlıdır; maksimum 30 saniyelik bir süre iyi bir başlangıç noktasıdır.

**İyileştirme denemeleri zaman aşımı** değeri, özgün olarak bulunana oranla daha iyi bir çözüm bulmak için en çok kaç saniye kullanılabileceğini denetler. Bu yalnızca, farklı kombinasyonların test edilmesini gerekitren paralel operasyonları kullanan yolları etkiler.

> [!NOTE]
> Zaman aşımları için ayarlanan değerler hem serbest bırakılmış üretim emirlerinin, hem de MRP'nin bir parçası olarak planlanan siparişlerin planlanması için uygulanır. Sonuç olarak, çok yüksek değerlerin ayarlanması, planlanan birçok üretim emri bulunan bir plan için çalışırken, MRP çalışma süresine önemli ölçüde ekleme yapabilir.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]