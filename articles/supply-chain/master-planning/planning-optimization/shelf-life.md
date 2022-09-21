---
title: Sınırlı raf ömrü olan ürünler için master planlama
description: Bu makalede, çabuk bozulabilen ürünlerin raf ömrünü dikkate alan planlama özelliklerinin nasıl ayarlanacağı ve kullanılacağı açıklanır.
author: t-benebo
ms.date: 08/10/2022
ms.topic: article
ms.search.form: ReqPlanSched, CustTable, EcoResProductDetailsExtended, InventModelGroup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2020-08-10
ms.dyn365.ops.version: 10.0.28
ms.openlocfilehash: 68a1ba2bfe90aaf0462917c405d483fa12bf8126
ms.sourcegitcommit: 3d7ae22401b376d2899840b561575e8d5c55658c
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/08/2022
ms.locfileid: "9428240"
---
# <a name="master-planning-for-products-with-limited-shelf-life"></a>Sınırlı raf ömrü olan ürünler için master planlama

[!include [banner](../../includes/banner.md)]

Raf ömrü, bir ürünün artık kullanılamaz veya satılamaz duruma gelene kadar saklanabileceği süredir. Raf ömrü sınırlı olan ürünler için büyük olasılıkla, maddelerin tüketimi ve satışını kalan raf ömrüne göre önceliklendiren ilk süresi dolan ilk çıkar (FEFO) ambar stratejisi kullanmanız gerekir. Bu ambar stratejisi kısa bir depolama süresine sahip olan gıda, ilaç ve diğer mallar için geçerlidir. FEFO'ya göre, ambardaki maddeler süpermarket rafındaki mallar gibi depolanır: uzun raf ömrü olan ürünler rafların gerisine depolanır ve daha kısa raf ömrü kalan ürünler daha önce sevk edilir.

## <a name="using-shelf-life-in-master-planning"></a>Master planlamada raf ömrü kullanma

Bu bölümde, master planlamanın raf ömrü olan maddeler için nasıl tedarik önerdiği açıklanmaktadır.

Master plan çalıştırdığınızda, talepinizi karşılayacak ve gecikmeleri en aza indirecek önerilen planlı siparişler (tedarik) oluşturur. Planınız sınırlı raf ömrü olan maddeleri içeriyorsa, planlama hesaplamaları daha karmaşık hale gelir çünkü plan gecikmeleri en aza indirmenin yanında geçerlilik süresi dolmadan önce mevcut tedariği kullanmalıdır. Plan, süresi dolmadan önce son kullanma tarihi en yakın olan tedariği kullanımmayı denemelidir. Bu nedenle, master planlama şu sırayla aşağıdaki hedeflere ulaşmayı dener:

1. Gecikmelerin toplamını en aza indirmek.
1. FEFO tedariği toplamını en üst düzeye çıkarmak.
1. Stok yenilemesini en aza indirmek.

Bazı durumlarda, ilk iki hedef arasında bir çakışma olabilir ve bir seçim yapılması gerekir: bir sevkiyatı geciktirmek mi yoksa son kullanma tarihi daha erken olan mallar yerine son kullanma tarihi daha geç olan malları kullanmak mı? Master planlama sırasında bu çakışmayı gidermek için sistem son kullanım süresi yaklaşan kaynağı kullanmak yerine gecikmeleri en aza indirmeye öncelik verir. Genel olarak, döneme göre gecikmeler ve karşılama söz konusu olduğunda bu tür bir çakışmalar oluşur. Bu nedenle, bir maddenin raf ömründen daha kısa olan bir karşılama dönemi kullanmanızı öneririz. Diğer karşılama türlerinde (gereksinim gibi) bu çakışma türüyle karşılaşma olasılığınız düşüktür.

## <a name="set-up-shelf-life"></a>Raf ömrü ayarlama

### <a name="configure-each-master-plan-to-consider-shelf-life"></a>Her master planı raf ömrünü dikkate alacak şekilde yapılandırma

Varsayılan olarak, master planlar raf ömrünü dikkate almaz. Gereken her master plan için raf ömrü hesaplamalarını etkinleştirmek üzere aşağıdaki yordamı kullanın.

1. **Master planlama \> kurulum \> planlar \> Master planlar** bölümüne gidin.
1. Liste bölmesindeki master planlardan birini seçin veya yeni bir tane oluşturun.
1. **Genel** hızlı sekmesinde, **Raf ömrü tarihlerini kullan** seçeneğini *Evet* olarak ayarlayın.

### <a name="configure-tracking-dimension-groups-to-track-the-batch-dimension"></a>İzleme boyutunu izlemek için izleme boyutu gruplarını yapılandırma

Bir maddenin raf ömrü ancak bu madde toplu iş boyutunda izleniyorsa izlenebilir. Başka bir deyişle, toplu iş başvurusu ve gerekli tarihler, giriş veya üretim sırasında ve maddenin her stok hareketiyle kaydedilmelidir. Bu seçeneği yönetmek için, gerekli izlemeyi yapmak üzere bir veya daha fazla izleme boyutu grubu ayarlayın ve sonra gerekli maddeleri gerektiği gibi bu gruplara atayın.

Toplu iş boyutunu izlemek üzere bir izleme boyutu grubu ayarlamak için aşağıdaki yordamı kullanın.

1. **Ürün bilgileri yönetimi \> Kurulum \> Boyut ve varyant grupları \> Boyut gruplarını izleme**'ye gidin.
1. Şu adımlardan birini izleyin:

    - Eylem bölmesinde **Yeni**'yi seçerek yeni bir izleme boyutu grubu oluşturun. Bir ad ve açıklama girin ve Eylem Bölmesinde **Kaydet**'i seçin.
    - Liste bölmesinde, toplu iş boyutunu izlemek üzere ayarlamak istediğiniz mevcut izleme boyutu grubunu seçin.

1. **İzleme boyutu** hızlı sekmesinde **Toplu iş numarası** satırında **Etkin** ve **Fiziksel stok** sütunlarındaki onay kutularını seçin.

### <a name="set-up-shelf-life-for-a-product"></a>Ürün için raf ömrü ayarlama

Ürünle ilgili raf ömrünü ayarlamak için aşağıdaki yordamı kullanın.

1. Sırasıyla **Ürün bilgi yönetimi \> Ürünler \> Serbest bırakılmış ürünler**'e gidin.
1. Ayarlamak istediğiniz ürünü oluşturun veya açın.
1. Raf ömrü ayarlarını kullanmak için **Genel** hızlı sekmesinde **İzleme boyutu grubu** alanını toplu iş boyutunu izlemek üzere ayarlanan izleme boyutu grubuna ayarlayın. Bu alanı yalnızca bir ürünü ilk kez oluştururken ayarlayabilirsiniz. Mevcut ürünler için değeri değiştiremezsiniz.
1. **Stoğu yönet** hızlı sekmesinde aşağıdaki alanları ayarlayın:

    - **Gün cinsinden raf önerisi dönemi**: Tüketim veya yeniden satılmaya uygun olmasını sağlamak üzere bu ürünün toplu işinin denetleneceği süreyi (gün olarak) belirtin. Bu alanın değeri, *raf önerisi tarihini* belirlemek üzere toplu işin *üretim tarihine* eklenir. Bir toplu iş önerilen raf tarihine yaklaştığında sistemi kalite emirleri üretecek şekilde yapılandırabilirsiniz.
    - **Gün olarak raf ömrü dönemi**: Bu ürünün bir partisinin süresi dolmadan önce geçecek gün sayısını belirtin. Bu değer, *sona kullanma tarihini* belirlemek üzere *üretim tarihine* eklenir. Toplu iş bu tarihten sonra kullanılamaz olarak kabul edilir.
    - **Gün olarak tavsiye edilen kullanım dönemi**: Bu ürün partisinin hala satılabilir olarak kabul edildiği ancak artık başlagıçtaki özelliklerinden bazılarını korumdağı dönemi (gün olarak ) belirtin. Bu değer, *son kullanma tarihini* belirlemek üzere *üretim tarihine* eklenir. Önerilen son kullanma tarihi geçen stoğu belirlemek için raporlar çalıştırabilirsiniz. 

### <a name="set-a-sellable-days-rule-for-each-customer"></a>Her müşteri için bir satış yapılabilir gün kuralı ayarlama

*Satış yapılabilir gün* işlevi, kısa süre içinde tarihi dolacak bir partideki ürünlerin müşterilere gönderilmemesini sağlar. Üstelik, ürünler müşteriye gönderildiğinde, teslimat sonrasında yeterli sayıda satış yapılabilir gün kaldığından emin olur.

Satış yapılabilir gün sayısı işlevini kullanmak için, her bir müşterinin her ürünü (veya ürün grubu) için geçerli olan satış yapılabilir gün sayısı tanımlamanız gerekir. Bunun için bir veri varlığı olmadığından bu işlemi el ile tamamlamanız gerekir.

Her müşterinin her ürünü için satış yapılabilir gün sayısını ayarlamak üzere aşağıdaki yordamı kullanın.

1. **Satış ve pazarlama \> Müşteriler \> Tüm müşteriler** öğesine gidin.
1. Ayarlamak istediğiniz müşteriyi bulun ve seçin.
1. Eylem Bölmesi'nde, **Sat** sekmesindeki **Ayar** gurubunda **Sat \>Satış yapılabilir gün sayısı**'nı seçin.
1. **Müşteri için satış yapılabilir gün sayısı** sayfasındaki ızgarda her ürün veya ürün grubu için mevcut satış yapılabilir gün sayısı kuralları listelenir. Gerektiğinde ızgaraya satır eklemek veya satırları düzenlemek için Eylem Bölmesindeki düğmeleri kullanın. Mevcut satırları bulmanıza yardımcı olmak için bir **Filtre** sağlanır.
1. Her satır için aşağıdaki alanları ayarlayın:

    - **Madde kodu**: Etkilenecek maddelerin kapsamını belirtmek için aşağıdaki değerlerden birini seçin:

        - *Tablo*: Satır belirli bir madde için geçerlidir.
        - *Grup*: Satır bir madde grubu için geçerlidir.
        - *Tümü*: Satır tüm maddeler için geçerlidir.

    - **Madde ilişkisi**: **Madde kodu** alanını *Tablo* olarak ayarlarsanız belirli bir maddeyi seçin. **Madde kodu** alanını *Grup* olarak ayarladıysanız bir madde  grubu seçin. **Madde kodu** alanını *Tümü* olarak ayarlarsanız bu alan kullanılmaz.
    - **Satış yapılabilir gün sayısı**: Müşterinin parti tarihi sona ermeden eşleşen ürünleri satması gereken minimum gün sayısını girin. Satış siparişindeki ilgili ürünler için satış yapılabilir gün sayısı değeri istenen giriş tarihini (veya tanımlanmışsa onaylanan giriş tarihini) temel alır.
    - *(Diğer ürün boyutları)*: Bir satırın kapsamını daha fazla sınırlamak için gerektiğinde diğer boyut değerlerini (**Boyut** ve **Renk** gibi) belirtin. Izgarada gösterilecek boyutları kontrol etmek için Eylem Bölmesinde **Boyutları görüntüle**'yi seçin.

### <a name="set-up-all-relevant-products-so-that-they-are-fefo-date-controlled"></a>İlgili ürünlerin tümünü FEFO tarihi denetimli olacak şekilde ayarlama

Satış yapılabilir gün sayısının çalışabilmesi için ilgili her maddenin **FEFO tarihi denetimli** onay kutusunun seçildiği bir madde model grubuna ait olması gerekir.

Satış yapılabilir gün sayısı işlevini destekleyecek şekilde bir madde modeli grubu ayarlamak için aşağıdaki yordamı kullanın.

1. **Stok yönetimi \> Kurulum \> Stok \> Madde modeli grupları** öğesine gidin.
1. Liste bölmesinden mevcut bir grubu seçin veya Eylem Bölmesi'nde **Yeni**'yi seçerek yeni bir grup oluşturun.
1. **Stok ilkeleri** hızlı sekmesinde, **FEFO tarihi denetimli** onay kutusunu seçin.
1. Grup için diğer alanları gereken şekilde ayarlayın.

Bir ürünün ait olduğu madde modeli grubunu görüntülemek veya ayarlamak için aşağıdaki yordamı kullanın.

1. Sırasıyla **Ürün bilgi yönetimi \> Ürünler \> Serbest bırakılmış ürünler**'e gidin.
1. Denetlemek veya düzenlemek istediğiniz ürünü açın.
1. **Genel** hızlı sekmesinde, **Madde modeli grubu** alanını **FEFO tarihi denetimli** onay kutusunun işaretli olduğu bir grup olarak ayarlayın.

## <a name="example-1-simple-fefo-10-day-period-zero-days-of-lead-time"></a>Örnek 1: Basit FEFO, 10 günlük dönem, sıfır günlük sağlama süresi

Bu örnekte, sistemin aşağıdaki hedeflerine ulaşmak amacıyla tedarik emirleri ile talep arasındaki ilişkilendirmenin yapıldığı temel bir raf ömrü örneği gösterilmektedir:

- Gecikmelerin toplamını en aza indirmek.
- FEFO tedariği toplamını en üst düzeye çıkarmak.
- Stok yenilemesini en aza indirmek.

Sistemde aşağıdaki madde ve master plan ayarları bulunur:

- **Karşılama kodu (stok yenileme stratejisi):** Dönem 
- **Karşılama dönemi:** 10 gün (raf ömrüne eşit)
- **Raf ömrü:** 10 gün
- **Satış yapılabilir gün sayısı:** 0
- **Sağlama süresi:** 0 gün
- **Negatif günler:** 0 gün
- **Planlı sipariş türü (maddenin varsayılan sipariş ayarları):** Satınalma siparişi

Bu madde için sistemde aşağıdaki satış siparişleri bulunur:

- **SO1:** Miktar (miktar) = 2, istenen teslimat tarihi = bugün + 1 gün
- **SO2:** Miktar = 1, istenen teslimat tarihi = bugün + 4 gün
- **SO3:** Miktar = 1, istenen teslimat tarihi = bugün + 5 gün

Tüm bu satış siparişleri madde için talep oluşturur.

Madde için aşağıdaki tedarik bulunur:

- **Eldeki stok:** Miktar = 1, son kullanma tarihi = bugün + 5 gün
- **Satınalma siparişi 1 (PO1):** Giriş tarihi = bugün + 2 gün, miktar = 1, son kullanma tarihi = bugün + 4 gün

Sistem bu talebi karşılayabilecek bir tedarik listesi oluşturur ve listeyi son kullanma tarihine (FEFO kullanarak) göre sıralar.

Master planlama, tedarik ile talep arasında gerekli ilişkilendirmeyi oluşturur. Ayrıca, tedarik listesine dayalı olarak gerekli talebi oluşturur (FEFO kullanılarak) ve kullanılabilirlik tarihini dikkate alır.

- SO1 eldeki miktarla yerine karşılanabilir ancak PO tarafından karşılanamaz çünkü PO1 için kullanılabilirlik tarihi SO1'in gerektirdiğinden bir gün daha geçtir. Bu nedenle, SO1 bir mal birimi için talep oluşturur.
- SO2, PO1 tarafından karşılanabilir çünkü PO1 istenen tarihte gelecektir ve son kullanma tarihi hala geçerli olacaktır. Bu nedenle SO2 gereksinimi tamamen PO1 tarafından karşılanır.
- Kaynaklar kullanılabilir olmadığı için SO3 karşılanmaz. Bu nedenle, SO3 bir mal birimi için talep oluşturur.

Kalan tüm gereksinimleri karşılamak için sistemin aşağıdaki planlı satınalma siparişini oluşturması gerekir:

- **PPO1:** Giriş tarihi = bugün, miktar = 2, son kullanma tarihi = bugün + 10 gün

Aşağıdaki tablo sonucu özetlemektedir.

| Talep | İlişkilendirme |
|---|---|
| **SO1:** Teslimat tarihi = bugün + 1 gün, miktar = 2 | <p>**Eldeki:** Miktar = 1, son kullanma tarihi = bugün + 5 gün</p><p>**PPO1:** Giriş tarihi = bugün, miktar = 1, son kullanma tarihi = bugün + 10 gün</p> |
| **SO2:** Teslimat tarihi = bugün + 4 gün, miktar = 1 | **PO1:** Giriş tarihi = bugün + 2gün, 1 miktar, son kullanma tarihi = bugün + 4 gün |
| **SO3:** Teslimat tarihi = bugün + 5 gün, miktar = 1 | **PPO1:** Giriş tarihi = bugün, miktar = 2, son kullanma tarihi = bugün + 10 gün |

Aşağıdaki çizim, bu örnekte zaman çizelgesinin nasıl göründüğünü göstermektedir.

![Örnek 1: Basit FEFO, 10 günlük dönem, sıfır günlük sağlama süresi.](media/fefo-example-1.png "Örnek 1: Basit FEFO, 10 günlük dönem, sıfır günlük sağlama süresi")

## <a name="example-2-simple-fefo-requirement-three-days-of-lead-time"></a>Örnek 2: Basit FEFO, gereksinim, üç günlük sağlama süresi

Bu örnek, sistemin gecikmeleri en aza indirme girişiminin nasıl fazla sipariş oluşmasına neden olabileceğini göstermektedir.

Sistemde aşağıdaki madde ve master plan ayarları bulunur:

- **Karşılama kodu (stok yenileme stratejisi):** Gereksinim
- **Raf ömrü:** 10 gün
- **Satış yapılabilir gün sayısı:** 0
- **Sağlama süresi:** Aşağıdaki satıcı ticari sözleşmeleri tarafından kurulur:

    - **Ticari sözleşme 1:** Miktar = 1 ise, sağlama süresi = 4
    - **Ticari sözleşme 2:** Miktar = 2 ise, sağlama süresi = 3

- **Negatif günler:** 0 gün
- **Planlı sipariş türü (maddenin varsayılan sipariş ayarları):** Satınalma siparişi

Sistemde aşağıdaki satış siparişi vardır:

- **SO1:** Miktar = 2, istenen teslimat tarihi = bugün + 3 gün

Bu talep, mevcut tedarik emri ve onaylanmış bir satınalma siparişinin kapsamına alınmıştır:

- **Eldeki stok:** Kullanılabilir = bugün, miktar = 1, son kullanma tarihi = bugün + 2 gün
- **PO1:** Giriş tarihi = bugün + 3 gün, miktar = 1, son kullanma tarihi = bugün + 4 gün

Stok bitiş tarihi sevkiyat tarihinden önce olduğundan SO1 eldeki stok tarafından karşılanamıyor. PO1, yalnızca 1 miktarına sahip SO1 gereksinimini karşılayabilir. Bu nedenle, SO1 bir mal birimi için talep oluşturur. Bu gereksinimi karşılamak için sistem bir planlı satınalma siparişi (PPO1) oluşturur.

Sistemde iki ticari sözleşme vardır (biri için miktar = 1, sağlama süresi = 4 gün, diğer için miktar = 2, sağlama süresi = 3 gün). Bu nedenle, sistem ikinci ticari sözleşmeyi karşılayan planlı bir satınalma siparişi (PPO1) oluşturarak gecikmeleri en aza indirmeye çalışır. Sonuç fazla teslimattır (miktar = 2, sona kullanma tarihi = bugün + 10 gün).

Aşağıdaki tablo sonucu özetlemektedir.

| Talep | İlişkilendirme |
|---|---|
| **SO1:** Teslimat tarihi = bugün + 3 gün, miktar = 2 | <p>**PO1:** Giriş tarihi = bugün + 3 gün, miktar = 1, son kullanma tarihi = bugün + 4 gün</p><p>**PPO1:** Giriş tarihi = bugün + 3 gün, miktar = 1, son kullanma tarihi = bugün + 10 gün</p> |

Aşağıdaki çizim, bu örnekte zaman çizelgesinin nasıl göründüğünü göstermektedir.

![Örnek 2: Basit FEFO, gereksinim, üç günlük sağlama süresi.](media/fefo-example-2.png "Örnek 2: Basit FEFO, gereksinim, üç günlük sağlama süresi")

## <a name="example-3-simple-fefo-requirement-three-days-of-lead-time-five-sellable-days"></a>Örnek 3: Basit FEFO, gereksinim, üç günlük sağlama süresi, beş satış yapılabilir gün

Bu örnek, bir madde için satış yapılabilir günler eklendiğinde raf ömrünün nasıl çalışacağını gösterir.

Sistemde aşağıdaki madde ve master plan ayarları bulunur:

- **Karşılama kodu (stok yenileme stratejisi):** Gereksinim
- **Raf ömrü:** 10 gün
- **Satış yapılabilir gün sayısı:** 5
- **Sağlama süresi:** 5 gün
- **Negatif günler:** 0 gün
- **Planlı sipariş türü (maddenin varsayılan sipariş ayarları):** Satınalma siparişi

Sistemde aşağıdaki satış siparişi vardır:

- **SO1:** Miktar = 2, istenen teslimat tarihi = bugün + 2 gün
- **SO2:** Miktar = 1, istenen teslimat tarihi = bugün + 3 gün
- **SO3:** Miktar = 1, istenen teslimat tarihi = bugün + 5 gün

Bu talep, mevcut tedarik ve onaylanmış bir satınalma siparişi tarafından karşılanabilir:

- **Eldeki stok:** Kullanılabilir = bugün, miktar = 1, son kullanma tarihi = Bugün + 6 gün
- **PO1:** Giriş tarihi = bugün + 2 gün, miktar = 3, son kullanma tarihi = bugün + 10 gün

Sistem, tedarik (FEFO) listesi ve kullanılabilirlik tarihlerine göre bir ilişkilendirme aday listesi oluşturur. Bu nedenle SO1 eldeki stok tarafından karşılanamaz çünkü stok müşterinin gerektirdiği (istenen giriş tarihi + 5 gün) satış yapılabilir gün sayısından önce sona erer. PO1, iki birimli SO1 gereksinimi ve bir birimli SO2 gereksinimini karşılayabilir. Bu nedenle, yalnızca SO3'de hala bir birim mal için karşılanmamış talep vardır. Bu gereksinimi karşılamak için sistem aşağıdaki planlı satınalma siparişini oluşturur:

- **PP01:** Giriş tarihi = bugün + 5 gün, miktar = 1, son kullanma tarihi = bugün + 10 gün

Aşağıdaki tablo sonucu özetlemektedir.

| Talep | İlişkilendirme |
|---|---|
| **SO1:** Teslimat tarihi = bugün + 2 gün, miktar = 2 | **PO1:** Giriş tarihi = bugün + 2 gün, miktar = 2, son kullanma tarihi = bugün + 10 gün |
| **SO2:** Teslimat tarihi = bugün + 3 gün, miktar = 1 | **PO1:** Giriş tarihi = bugün + 2 gün, miktar = 1, son kullanma tarihi = bugün + 10 gün |
| **SO3:** Teslimat tarihi = bugün + 5 gün, miktar = 1 | **PPO1:** Giriş tarihi = bugün + 5 gün, miktar = 1, son kullanma tarihi = bugün + 10 gün |

Aşağıdaki çizim, bu örnekte zaman çizelgesinin nasıl göründüğünü göstermektedir.

![Örnek 3: Basit FEFO, gereksinim, üç günlük sağlama süresi, beş satış yapılabilir gün.](media/fefo-example-3.png "Örnek 3: Basit FEFO, gereksinim, üç günlük sağlama süresi, beş satış yapılabilir gün")

## <a name="example-4-simple-fefo-period-lead-time-depends-on-the-quantity"></a>Örnek 4: Basit FEFO, dönem, sağlama süresi miktara bağlıdır

Bu örnek, sistemin gecikmeleri en aza indirme girişiminin nasıl fazla sipariş oluşmasına neden olabileceğini göstermektedir.

Sistemde aşağıdaki madde ve master plan ayarları bulunur:

- **Karşılama kodu (stok yenileme stratejisi):** Dönem
- **Karşılama dönemi:** 10 gün (raf ömrüne eşit)
- **Raf ömrü:** 10 gün
- **Satış yapılabilir gün sayısı:** 0
- **Sağlama süresi:** Aşağıdaki satıcı ticari sözleşmeleri tarafından kurulur:

    - **Ticari sözleşme 1:** Miktar = 1 ise, sağlama süresi = 5
    - **Ticari sözleşme 2:** Miktar = 2 ise, sağlama süresi = 0

- **Negatif günler:** 0 gün
- **Planlı sipariş türü (maddenin varsayılan sipariş ayarları):** Satınalma siparişi

Sistemde aşağıdaki satış siparişi vardır:

- **SO1:** Miktar = 1, istenen teslimat tarihi = bugün
- **SO2:** Miktar = 1, istenen teslimat tarihi = bugün + 6 gün

Bu talep, aşağıdaki teyit edilen satınalma siparişlerinden mevcut tedarik tarafından kısmen karşılanabilir:

- **PO1:** Giriş tarihi = bugün + 1 gün, miktar = 1, son kullanma tarihi = bugün + 2 gün
- **PO2:** Giriş tarihi = bugün + 3 gün, miktar = 1, son kullanma tarihi = bugün + 7 gün

Sistemde iki ticari sözleşme vardır (biri için miktar = 1, sağlama süresi = 5 gün, diğer için miktar = 2, sağlama süresi = 0 gün). Bu nedenle, sistem ikinci ticari sözleşmeyi karşılayan aşağıdaki planlı bir satınalma siparişini oluşturarak gecikmeyi en aza indirmeye çalışır:

- **PP01:** Giriş tarihi = bugün, miktar = 2, son kullanma tarihi = bugün + 10 gün

SO1, PO1'deki bir birim tarafından karşılanır. SO2 PPO2 tarafından karşılanır çünkü PO2'nin süresi PPO1'den önce dolacaktır.

Aşağıdaki tablo sonucu özetlemektedir.

| Talep | İlişkilendirme |
|---|---|
| **SO1:** Teslimat tarihi = bugün, miktar = 1 | **PPO1:** Giriş tarihi = bugün, miktar = 1, son kullanma tarihi = bugün + 10 gün |
| **SO2:** Teslimat tarihi = bugün + 6 gün, miktar = 1 | **PO2:** Giriş tarihi = bugün + 3 gün, miktar = 1, son kullanma tarihi = bugün + 7 gün |

> [!NOTE]
> PO1 kullanılmaz çünkü S01 için çok geç gelecektir ve S02 teslim edilmeden önce süresi dolacaktır. PPO1, ticari sözleşme 2'e göre sağlama süresinin 0 (sıfır) olmasını sağlamak üzere bir birim fazla sipariş edilmiştir.

Aşağıdaki çizim, bu örnekte zaman çizelgesinin nasıl göründüğünü göstermektedir.

![Örnek 4: Basit FEFO, dönem, sağlama süresi miktara bağlıdır.](media/fefo-example-4.png "Örnek 4: Basit FEFO, dönem, sağlama süresi miktara bağlıdır")

## <a name="example-5-simple-fefo-requirement-10-negative-days"></a>Örnek 5: Basit FEFO, gereksinim, 10 negatif gün

Bu örnek, bir madde için çok sayıda negatif gün eklendiğinde raf ömrünün nasıl çalışacağını gösterir. Negatif günler, negatif stoğu olan bir maddenin sipariş stok yenilemesinden önce beklemek isteyeceğiniz gün sayısıdır. Negatif gün sayısı aşılmadıkça sistem tedarik oluşturmaz.

Sistemde aşağıdaki madde ve master plan ayarları bulunur:

- **Karşılama kodu (stok yenileme stratejisi):** Gereksinim
- **Sağlama süresi:** 0 gün
- **Negatif günler:** 10 gün
- **Planlı sipariş türü (maddenin varsayılan sipariş ayarları):** Satınalma siparişi

Sistemde aşağıdaki satış siparişi vardır:

- **SO1:** Miktar = 1, istenen teslimat tarihi = bugün

Bu talep, aşağıdaki teyit edilen siparişten mevcut tedarik tarafından karşılanabilir:

- **PO1:** Giriş tarihi = bugün + 3 gün, miktar = 1, son kullanma tarihi = bugün + 5 gün

Sistem 10 negatif güne izin verecek şekilde yapılandırıldığından SO1 talebini PO kullanarak karşılar. (SO1, PO gelene kadar negatif stok oluşturacağından sonuç üç günlük bir gecikme olacak olsa bile). Sağlama süresi 0 (sıfır) ve planlı satınalma siparişi oluşturma işlemi gecikmeleri düşürecek olsa bile planlı satın alma siparişi oluşturulmaz.

Aşağıdaki tablo sonucu özetlemektedir.

| Talep | İlişkilendirme |
|---|---|
| **SO1:** Teslimat tarihi = bugün, miktar = 1 | **PO1:** Giriş tarihi = bugün + 3 gün, miktar = 1, son kullanma tarihi = bugün + 5 gün |

Aşağıdaki çizim, bu örnekte zaman çizelgesinin nasıl göründüğünü göstermektedir.

![Örnek 5: Basit FEFO, gereksinim, 10 negatif gün.](media/fefo-example-5.png "Örnek 5: Basit FEFO, gereksinim, 10 negatif gün")

## <a name="example-6-simple-fefo-requirement-five-negative-days"></a>Örnek 6: Basit FEFO, gereksinim, beş negatif gün

Bu örnek, bir madde için eklenen negatif gün sayısı raf ömrü döneminden az olduğunda raf ömrünün nasıl çalıştığını gösterir.

Sistemde aşağıdaki madde ve master plan ayarları bulunur:

- **Karşılama kodu (stok yenileme stratejisi):** Gereksinim
- **Satış yapılabilir gün sayısı:** 0
- **Sağlama süresi:** 0 gün
- **Negatif günler:** 5 gün
- **Planlı sipariş türü (maddenin varsayılan sipariş ayarları):** Satınalma siparişi

Sistemde aşağıdaki satış siparişi vardır:

- **SO1:** Miktar = 2, istenen teslimat tarihi = bugün

Bu talep, aşağıdaki teyit edilen siparişlerden mevcut tedarik tarafından karşılanabilir:

- **PO1:** Giriş tarihi = bugün, miktar = 1, son kullanma tarihi = bugün + 1 gün
- **PO2:** Giriş tarihi = bugün + 2 gün, miktar = 1, son kullanma tarihi = bugün + 3 gün

Ancak, sistemin sevk edilen maddelerin sevkiyat sırasında süresinin dolamayacağı kısıtlamasına uyması gerekir. Bu nedenle, PO2 ve PO1'in ikisi birlikte SO!1 için kullanılamaz çünkü PO1'in süresi PO2 gelmeden önce sona erer. Sistem, SO1 için talebi karşılamayı tamamlamak üzere aşağıdaki planlı satınalma siparişini oluşturur:

- **PPO1:** Giriş tarihi = bugün, miktar = 1, son kullanma tarihi = bugün + 10 gün

Sistem, beş negatif günden faydalanabilir ve SO1'i karşılamak için PO2 ve PPO1'i kullanır. Ancak bu yaklaşım, PO2 gelene kadar teslimatın gecikmesine neden olur ve aynı sırada PO1'in süresi dolacaktır. Bu nedenle, sistem SO1'i PPO1 ve PO1 kullanarak karşılar.

Aşağıdaki tablo sonucu özetlemektedir.

| Talep | İlişkilendirme |
|---|---|
| **SO1:** Teslimat tarihi = bugün, miktar = 2 | <p>**PO1:** Giriş tarihi = bugün, miktar = 1, son kullanma tarihi = bugün + 1 gün</p><p>**PPO1:** Giriş tarihi = bugün, miktar = 1, son kullanma tarihi = bugün + 10 gün</p> |

Aşağıdaki çizim, bu örnekte zaman çizelgesinin nasıl göründüğünü göstermektedir.

![Örnek 6: Basit FEFO, gereksinim, beş negatif gün.](media/fefo-example-6.png "Örnek 6: Basit FEFO, gereksinim, beş negatif gün")
