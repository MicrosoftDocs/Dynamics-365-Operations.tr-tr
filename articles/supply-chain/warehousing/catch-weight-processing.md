---
title: Ambar yönetimi ile Fiili ağırlık ürün işlemi
description: Bu konuda ambar içinde işin nasıl ve nerede gerçekleştirileceğini belirlemek için iş şablonları ve konum yönergelerinin nasıl kullanılacağı açıklanmaktadır.
author: perlynne
manager: AnnBe
ms.date: 01/10/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSCatchWeightTag, WHSCatchWeightItemHandlingPolicy
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2019-1-31
ms.dyn365.ops.version: 8.1.3
ms.openlocfilehash: 8bc3e3e7bea15127062edfcd362476de97bff07d
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/01/2020
ms.locfileid: "3004123"
---
# <a name="catch-weight-product-processing-with-warehouse-management"></a>Ambar yönetimi ile Fiili ağırlık ürün işlemi

[!include [banner](../includes/banner.md)]


## <a name="feature-exposure"></a>Özellik tanıtımı

Fiili ağırlık ürünlerini kullanmak için Ambar yönetimini kullanmak için işlevi açmak için bir lisans yapılandırma anahtarını kullanmalısınız. (**Sistem yönetimi \> Kurulum \> Lisans yapılandırma** seçeneğine gidin. **Yapılandırma anahtarları** sekmesinde, **Ticari \> Ambar ve Nakliye yönetimi** üzerinde, **Ambar için Fiili ağırlık** seçeneği için onay kutusunu seçin.

> [!NOTE]
> **Hem Ambar ve Taşıma yönetimi** lisans yapılandırması anahtarı hem de **İşlem dağıtımı \> Fiili ağırlık** lisans yapılandırma anahtarlarının da açık olması gerekir. Fiili ağırlığa ilişkin yapılandırma anahtarlarını ayarlamak için, **Özellik yönetimi** çalışma alanını kullanarak özelliği de etkinleştirmelisiniz. Etkinleştirilmesi gereken ana özellik, **Ambar yönetimi ile Fiili ağırlık ürün işlemi**'dir. Etkinleştirmek isteyebileceğiniz başka bir ilişkili ancak isteğe bağlı bir özellik, **Fiili ağırlık ürünleri için stok durumu değişiklikleri**'dir . Bu özellik, fiili ağırlık için etkinleştirilen ürünlerin stok durumundaki değişikliklere yönelik destek ekler.

Lisans yapılandırma anahtarı açıldıktan sonra serbest bırakılan bir ürün oluşturduğunuzda **Fiili ağırlık** seçebilirsiniz. Serbest bırakılan ürünü **Ambar yönetim işlemi** parametresinin seçili olduğu bir depolama boyut grubu ile ilişkilendirebilirsiniz.

Ürünü Ambar yönetimi içinde kullanabilmeden önce fiili ağırlık için bazı temel ürüne özel ayarlar yapmanız gerekir:

- Fiili ağırlık birim (kutu) ve stok birimi (kilogram\[kg\]) arasındaki nominal ağırlık dönüşümünü ürün dönüşüm tanımının bir parçası olarak tanımlayın.
- Minimum ve maksimum ağırlık toleranslarını fiili ağırlık birim ayarlamasının bir parçası olarak tanımlayın.
- Fiili ağırlık biriminin en düşük stok tutma birimi (SKU) olarak tanımlandığı bir birim sıra grubu ayarlayın.
- Fiili ağırlık öge işleme ilkesi ayarlayın.

Daha fazla bilgi için bkz. [Fiili ağırlık ögeleri ayarlamak ve bakımı](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/setting-up-and-maintaining-catch-weight-items)'na bakın.

## <a name="transaction-adjustments"></a>Hareket ayarlamaları

Stokun ambara girdiğindeki ağırlığı, stokun ambardan çıktığındaki ağırlıktan farklı olabileceği için fiili ağırlık ürün işlemenin stoku ayarlaması gerekir.

> [!NOTE]
> Mobil cihaz faaliyeti, yalnızca maddenin fiili ağırlık kalem işleme ilkesinin Giden ağırlık farkı yöntemi **Ağırlık farkına izin ver** olduğu zaman hareket düzeltmelerini tetikler.

**Örnek 1**

**Tamamlandı olarak raporla** üretim işlemi sırasında, sekiz kutu fiili ağırlık ürün içeren bir plakanın giriş ağırlığının 80,1 kg olarak yakalandı olarak raporlanmıştır. Plaka tamamlanmış ürünler bölgesine depolandığında, depolama süresi boyunca ağırlığın bir miktarı havaya karışır.

Daha sonra, satış siparişi çekme işleminin bir parçası olarak, aynı plakanın ağırlığı 79,8 kg olarak yakalanır. Bu nedenle, sistemde fiziksel boyut kümesinin bir parçası olarak bir ağırlık farkına sahip olursunuz.

Bu durumda, sistem farkı eksik 0,3 kg için bir hareket naklederek farkı otomatik olarak ayarlar.

**Örnek 2**

Tanımında, bir ürün minimum ağırlık olan 8 kg'ı ve maksimum ağırlık olan 12 kg'ı **Kutu** fiili ağırlık birimi için tolere etmek üzere ayarlanır.

Üründen iki kutuya sahipsiniz ve 16 kg kayıtlı ağırlığa sahiptirler. Bir ambar çalışanı kutulardan birini çeker ve tartarsa, ağırlık 9 kg olarak yakalanır, kalan kutu 7 kg ağırlığındadır. Ancak, 7 kg ağırlık minimum ağırlığın olduğu için sistem eldeki stokun ağırlığını artırmak için 1 kg miktarında bir otomatik ayarlama yapar.

Bu ayarların deftere nakledileceği hesaplar ayarlamak için **Maliyet yönetimi \> Genel muhasebe tümleştirme ilkeleri ayarı \> Deftere nakil**'e gidin. Daha sonra **Stok** sekmesinde, aşağıdaki hesapları tanımlayın:

- Fiili ağırlık zarar hesabı
- Fiili ağırlık kar hesabı

## <a name="catch-weight-item-handling-policy"></a>Fiili ağırlık maddesi işleme ilkesi

Fiili ağırlık öge işleme ilkesi, ögeler için iki ana ambar yönetim akışını tanımlar: ögenin ağırlığının yakalanması ve nasıl yakalandığı.

Ağırlığın satış ve transfer sipariş işleme için ne zaman yakalanacağını tanımlayabilirsiniz. Ağırlık, aşağıdaki işlemler sırasında yakalanabilir:

- **Malzeme çekme** - Ağırlık sipariş işinin ilk çekme iş satırında yakalanır.
- **Paketleme** - Ağırlık, el ile paketleme sırasında yakalanır. (Ögeleri bir paketleme istasyonuna göndermelisiniz.)

Gerçek ağırlık paketleme istasyonunda konteyner paketleme işlemleri sırasında yakalanırsa, ambar çalışanlarının ağırlığı malzeme çekme işi sırasında yakalamaları gerekmez. Bunun yerine, fiziksel stokun ortalama ağırlığı, paketleme alanına giden çekilen stokun ağırlığı olarak kullanır. Bu kavram, etiketlerle izlenen fiili ağırlık kalemleri için de geçerlidir. Etiket izlemeli kalemler için bu parametreler etiketin ne zaman yakalandığını belirler. Etiket, mobil cihaz kullanılarak veya el ile paketleme yapılırken malzeme çekme sırasında yakalanabilir.

> [!NOTE]
> **Ambalaj** seçeneği stokun ortalama çekilen ağırlıkla güncelleştirilmesini sağladığından, bu, eldeki stok ağırlığı ile fiili ağırlık etiket ağırlığı arasındaki bir fiili ağırlık kar/zarar ayarlamasına ve/veya farkına neden olabilecek bir uyuşmazlığı tetikleyebilir.

Sayım ve ayarlama düzeltmeleri gibi dahili ambar yönetimi işlemleri için, ağırlığın yakalanması gerekip gerekmediğini tanımlayabilirsiniz. Yakalanmamışsa nominal ağırlık kullanılır. Diğer seçenekler, her fiili ağırlık birimi ve her sayım miktarı için ağırlık yakalamanızı sağlar.

Ayrıca ağırlığın nasıl yakalanacağını da tanımlayabilirsiniz. İki ana akıştan birinde, fiili ağırlık etiketleri izlenir ve ağırlığı yakalamak için kullanılır. Diğer akışta, fiili ağırlık etiketleri izlenmez.

- **Evet** - Öge fiili ağırlık etiketlerini kullanır. Her bir etiket numarası bir fiili ağırlık birimi (kutusu) temsil eder ve ağrılık ve diğer bilgiler etiket ile ilişkilendirilir. Giden işlemler için etiket ile ilişkilendirilen ağırlık kullanılır.
- **Hayır** – Öge fiili ağırlık etiketlerini kullanmıyor. Giren ve çıkan tartım işlemleri her bir işlem sırasında yakalanan gerçek ağırlıklara dayanmaktadır.

Fiili ağırlık etiketlerini izleme işlemi depolama süresince ağırlıkları değişmeyecek ögeler için kullanılabilir. Ağırlık yalnızca giriş ambar işlemleri sırasında yakalanacaktır. Çıkan işlemler sırasında, fiili ağırlık etiketleri yalnızca taratılır ve etiketlerle ilişkilendirilmiş ağırlıklar çıkış hareket işlemleri için kullanılır.

Fiili ağırlık etiketlerinin işlenmesiyle ilgili başka bir önemli parametre ise **Fiili ağırlık etiketi boyut izleme yöntemi**'dir. Etiketler kısmen veya tamamen izlenebilir. Bir etiket kısmen izleniyorsa, ürün boyutlarını, izleme boyutlarını ve stok durumunu izler. Bir etiket tamamen izleniyorsa, ürün boyutlarını, izleme boyutlarını ve **tüm** depolama boyutlarını izler.

Ek olarak, bir kalem etiket izlemeliyse bir **Giden etiketi yakalama yöntemi** parametresi vardır. Bu parametreyi, mobil cihazdan giden hareketlerdeki etiketin sizden her zaman isteneceği şekilde ayarlayabilirsiniz. Alternatif olarak, parametreleri etiketlerin yalnızca gerekli olduklarında sizden isteneceği şekilde ayarlayabilirsiniz. Örneğin, belirli bir plaka üzerinde stokta beş fiili ağırlık etiketi var ve plakadan beş etiketin tümünü çekmek istediğinizi belirttiniz. Bu durumda, **Giden etiketi yakalama yöntemi** parametresi **Etiketi yalnızca gerekliyse iste** olarak ayarlandıysa, beş etiket otomatik olarak çekilir. Her bir etiketi taramanız gerekmez. Parametre **Etiketi her zaman iste** olarak ayarlandıysa, beş etiketin tümü çekilse bile her etiketi taramanız gerekir.

> [!NOTE]
> Kural olarak, etiketler yalnızca mobil cihaz menü öğelerinden yakalanıp güncelleştirilir. Yine de, etiketlerin başka bir yerde (örneğin el ile ambalaj istasyonundan) yakalandığı birkaç senaryo vardır. Ancak, genel olarak, etiketler kullanılıyorsa, mobil cihaz menü öğeleri tüm ambar faaliyeti için kullanılmalıdır.

### <a name="how-to-capture-catch-weight"></a>Fiili ağırlığı yakalamak

**Bir fiili ağırlık etiketi izleme kullanılıyorsa**, bir etiketin her zaman alınan her bir fiili ağırlık birimi için oluşturulması ve her bir etiketin her zaman bir ağırlık ile ilişkilendirilmesi gerekir.

Örneğin **Kutu** fiili ağırlık birimidir ve sekiz kutudan oluşan bir palet alırsınız. Bu durumda, sekiz benzersiz fiili ağırlık etiketinin oluşturulması ve bir ağırlığın her bir etiket ile ilişkilendirilmesi gerekir. Giriş fili ağırlık etiketine bağlı olarak, tüm sekiz kutunun ağırlığı yakalana bilir ve ortalama ağırlık her bir kutuya dağıtılabilir veya benzersiz bir ağırlık her bir kutu için yakalanır.

**Fiili ağırlık etiketi izleme kullanılmıyorsa**, ağırlık her bir boyut kümesi için yakalanabilir (örneğin her bir plaka ve izleme boyutu için). Alternatif olarak, ağırlık birleştirilmiş düzeye dayanarak toplanabilir, örneğin beş plaka gibi (palet).

Giden ağırlığı yakalama yöntemleri için, **Fiili ağırlık birimi başına** seçeneği her bir fiili ağırlık yakalama birimi için (örneğin kutu başına) tartma uygulanacağını belirtmenize olanak sağlar. **Malzeme çekme birimi başına** seçeneği, ağırlığın çekilecek miktara göre (örneğin üç kutu) yakalanması gerektiğini belirtmenize olanak sağlar. Üretim hattı çekme ve dahili hareket işlemleri için ortalama ağırlığın **Yakalanmadı** seçeneği kullanılırsa kullanılacağını unutmayın.

Fiili ağırlık kalem işleme ilkesinde birden fazla ağırlık yakalama yöntemi tanımlanır. Her ağırlık yakalama yöntemi parametresi çeşitli hareketler tarafından kullanılır. Aşağıdaki tablo, hangi parametrelerin hangi hareketlerle kullanıldığını özetlemektedir.

| Yöntem                                     | Hareket                                |
|--------------------------------------------|--------------------------------------------|
| Giden ağırlık yakalama yöntemi           | Satış için malzeme çekme, Aktarım için malzeme çekme            |
| Üretim malzeme çekme ağırlığı yakalama yöntemi | Üretim için malzeme çekme, Üretim tüketimi |
| Hareket ağırlık yakalama yöntemi           | Hareket                                   |
| Ağırlık düzeltmesi yakalandığında       | Düzeltmeler, Sayım                      |
| Sayım ağırlığı yakalama yöntemi           | Sayım                                   |
| Ambar transfer ağırlığı yakalama yöntemi | Ambar transferi                         |

Fiili ağırlık kar/zarar ayarlamalarıyla sonuçlanan ağırlık yakalamadan ambar yönetimi çekme işlemlerini önlemek için, Giden ağırlık farkı yöntemini kullanabilirsiniz. Giden ağırlık farkı yöntemi şu mobil cihaz işlemleri sırasında geçerlidir: satış için malzeme çekme, aktarım için malzeme çekme, üretim için malzeme çekme, hareketler, sayım ve ambar transferleri. Ambar depolama sırasında fiili ağırlık kaleminin ağırlığı dalgalanmazsa ve fiili ağırlık kar/zarar düzeltmeleri gerekmiyorsa, **Ağırlık farkını kısıtla** seçeneğini kullanabilirsiniz. Ağırlık dalgalanabiliyorsa ve ağırlık dalgalanması kaydedildiğinde fiili ağırlık kar/zarar düzeltmeleri yapmak gerekiyorsa, **Ağırlık farkına izin ver** seçeneğini kullanabilirsiniz.

## <a name="unsupported-scenarios"></a>Desteklenmeyen senaryolar

Her iş akışı ambar yönetimi ile fiili ağırlık ürün işlemeyi desteklemez. Aşağıdaki kısıtlamalar şu anda geçerlidir. Etiketlenip etiketlenmedikleri dikkate alınmadan, tüm fiili ağırlık maddelerine uygulanır.

### <a name="configuring-catch-weight-products-for-warehouse-management-processes"></a>Ambar yönetimi işlemleri için fiili ağırlık ürünlerini yapılandırmak.

- Yalnızca formül işlem fiili ağırlık ürünleri için desteklenir (ürün reçetesi değil).
- Fiili ağırlık ürünleri, Sahip boyutu kullanarak bir izleme boyut grubu ile ilişkilendirilemez.
- Fiili ağırlık ürünleri hizmetler olarak kullanılamaz.
- Fiili ağırlık ürünleri, yalnızca öğe model grubunun parası olarak "stoklu ürün" olarak kullanılabilir.
- Fiili ağırlık ürünleri, "Satış işleminde etkin" izleme özelliği ile birlikte kullanılamaz.
- Fiili ağırlık ürünleri, seri numaraları yakalama özelliği ile birlikte kullanılamaz. Bu nedenle, ürünler "boş"tan bir seri numarasına bir çekme/paketleme işleminin parçası olarak aktarılamaz.
- Fiili ağırlık ürünleri, tüketimden önce serileri kaydetme özelliğiyle birlikte kullanılamaz.
- Çeşit özelliği etkin fiili ağırlık ürünleri, çeşit birim ölçümlerini dönüştürme özelliğiyle birlikte kullanılamaz.
- Fiili ağırlık ürünleri ticari bir "ürün seti" olarak işaretlenemez.
- Fiili ağırlık ürünleri yalnızca fiili ağırlık işleme birimlerine sahip bir birim sıra grubu, ile fiili ağırlık biriminin en düşük sıralamada olmasıyla kullanılabilir.
- Fiili ağırlık ürünleri için stok birimi yalnızca dönüşüm 1'den büyük bir nominal miktar oluşturduğunda fiili ağırlık birimine dönüştürülebilir.
- Fiili ağırlık ürünler için barkod kurulumu değişken ağırlık ayarını desteklemiyor.

### <a name="order-processing"></a>Sipariş işleme

- Ön sevkiyat bildirimi (ASN/sevk yapıları), ağırlık bilgisini desteklemiyor.
- Sipariş miktarı fiili ağırlık birimine dayanarak korunmalıdır.

### <a name="inbound-warehouse-processing"></a>Giriş ambar işleme

- Plakaları almak, ağırlıkların kayıt sırasında atanmasını gerektirir çünkü ağırlık bilgisi ön sevkiyat bildiriminin parası olarak desteklenmez. Fiili ağırlık etiket işlemleri kullanıldığında, fiili ağırlık birimi başına etiket numarası ile atanması gerekir.
- Gelen kalite denetimi işi, fiili ağırlık ürünleri için desteklenmez. Yapılandırıldıysa, kalite denetimi işi atlanır.

### <a name="inventory-and-warehouse-operations"></a>Stok ve ambar operasyonları

- Karantina emirlerinin el ile oluşturulması fiili ağırlık ürünleri için desteklenmiyor.
- Açık iş ile ilgili stokun el ile taşınması işlemi, fiili ağırlık ürünleri için desteklenmez.
- Ambar stokunu başlatmak için plaka yükleme fiili ağırlık ürünleri için desteklenmiyor.
- Toplu iş dengelemesi işlemleri fiili ağırlık ürünleri için desteklenmiyor.
- Negatif fiziksel stokun işlenmesi fiili ağırlık ürünleri için desteklenmiyor.
- Stok işaretleme fiili ağırlık ürünleri için kullanılamıyor.

### <a name="outbound-warehouse-processing"></a>Giden ambar işleme

- Küme çekme için işlev fiili ağırlık ürünleri için desteklenmiyor.
- Çekme ve paketleme amber işleme fiili ağırlık ürünleri için desteklenmiyor.
- Fiili ağırlık ürünleri için bir iş şablonunda tanımlanan bir iş otomatik olarak yürütülebilir.
- Fiili ağırlık ürünleri için, sistem, konteynerler kapatıldıktan sonra sevk edilmiş konteyner çekme işinin oluşturulduğu durumlarda el ile işleme istasyon işlemini desteklemez.
- Adet başına tarama işlevi, fiili ağırlık ürünleri için desteklenmiyor.

### <a name="production-processing"></a>Üretim işleme

- Fiili ağırlık ürünleri için yalnızca formül ürünleri çiin toplu iş siparişleri desteklenir.
- Kanban işlevi fiili ağırlık ürünleri için desteklenmiyor.
- Fiili ağırlık ürünleri için seri numaralar tüketimden önce kaydedilemez.
- Üründen plakalara uygulanan ters işlem işlevi, fiili ağırlık ürünleri için desteklenmez.
- Fiili ağırlık ürünleri için, tamamlandı olarak raporlama, seri numarasıyla kaydedilemez.

### <a name="transportation-management-processing"></a>Taşıma yönetimi işleme

- Yükleme binası workbench işleme fiili ağırlık ürünleri için desteklenmiyor.
- Taşıma talebi satırları fiili ağırlık ürünleri için desteklenmiyor.

### <a name="other-restrictions-and-behaviors-for-catch-weight-product-processing-with-warehouse-management"></a>Ambar yönetimi ile fiili ağırlık ürün işleme için diğer kısıtlamalar ve davranışlar

- Kullanıcının izleme boyutlarını belirlemesi istenmediği malzeme çekme işlemleri sırasında, ağırlık ataması ortalama ağırlığa dayalı olarak yapılır. Bu davranış, örneğin bir izleme boyutu kombinasyonu aynı konumda kullanıldığında ve bir kullanıcı çekmeyi işledikten sonra konumda yalnızca bir izleme boyutu değeri kalırsa ortaya çıkar.
- Stok bir ambar yönetimi işleminde yapılandırılmış bir fiili ağırlık ürünü için rezerve edilirse, rezervasyon tanımlanan minimum ağırlığa dayanarak gerçekleştirilir, bu miktar eldeki son işlem miktarı olsa bile. Bu davranış, ambar yönetimi işlemleri için yapılandırılmamış ögelerin davranışından farklıdır. Bu kısıtlamanın bir istisnası vardır. Üretim için çekme işlemi için, seri numarası denetimli bir fiili ağırlık ürününün son işleme miktarı çekilirken gerçek ağırlık kullanılır.
- Ağırlığı kapasite hesaplamalarının parçası olarak kullanan işlemlerde (dalga eşikleri, iş maksimum molalar, konteyner maksimumları, konum yük kapasiteleri ve benzeri), stokun gerçek ağırlığını kullanmayın. Bunun yerine, işlemler ürün için tanımlanmış fiziksel işleme ağırlığına dayanır.
- Genel olarak, Ticaret işlevi, fiili ağırlık ürünleri için desteklenmez.
- Fiili ağırlık ürünleri için, stok durumu, **Ambar durumu değişikliği**'nden güncelleştirilemez.

### <a name="catch-weight-tags"></a>Fiili ağırlık etiketleri

Bir fiili ağırlık etiketi bir ambar uygulaması işlemi kullanılarak, formda el ile veya bir veri varlığı işlemiyle oluşturulabilir. Bir fiili ağırlık etiketi bir gelen kaynak belgesi satırıyla (örneğin bir satınalma siparişi satırı vb.) ilişkilendirilirse, etiket kaydedilir. Satır giden işlem için kullanılıyorsa, etiket sevk edilmiş olarak güncelleştirilir.

Fiili ağırlık ürünleri için geçerli olan kısıtlamalara ek olarak, etiketli fiili ağırlık ürünleri için geçerli olan başka kısıtlamalar da vardır.

- Stoktaki tüm el ile yapılan güncelleştirmeler (yani bir mobil cihazla yapılmayan güncelleştirmeler), ilişkili fiili ağırlık etiketlerine karşılık gelen el ile güncelleştirmeler içermelidir çünkü bu güncelleştirmeler otomatik olarak yapılmaz. Örneğin, el ile yapılan düzeltme günlükleri stoku güncelleştirecek ama ilişkili fiili ağırlık etiketlerini güncelleştirmeyecektir.
- Stok yenileme işi hareketlerini yansıtmak için, fiili ağırlık etiketlerini el ile güncelleştirmeniz gerekir. Bunun nedeni, sistemin stok yenileme işini işlerken ağırlıkları yakalayamaması ve bu nedenle ortalama ağırlığı kaydetmesidir.
- Karma plaka alma işlemi, etiketli fiili ağırlık kalemleri için şu anda desteklenmemektedir.
- Satış iade emri alma işlemi, fiili ağırlık etiketlerini kaydedebilir. Ancak bu işlem, iade edildi etiketinin, başlangıçta bir satış siparişi için sevk edilen etiketle aynı olduğunu doğrulamaz.
- **Malzeme tüketimini kaydet** faaliyet kodunu taşıyan mobil cihaz menüsü öğesi, fiili ağırlık etiketlerinin kaydedilmesini şu anda desteklememektedir.
- Etiketli fiili ağırlık kalemleri için sayım işlemleri desteklenmekle birlikte, bu işlemler sınırlıdır. Örneğin, etiketli fiili ağırlık kalemlerinin sayımı için mobil cihaz seçeneklerini kullanabilirsiniz ve ortalama ağırlık kullanılır. Ancak, fiili ağırlık etiketleri sayım işlemiyle otomatik olarak güncelleştirilmez. Sayım işlemi tamamlandıktan sonra, fiili ağırlık etiketlerinin stoku yansıtması için el ile güncelleştirilmesi gerekir. Başlangıçta bir konumda bulunmayan kalemlerin sayımı o konuma dahil ediliyorsa, nominal ağırlık kullanılır.
- Plaka birleştirme, etiketli fiili ağırlık kalemlerini şu anda desteklemiyor.
- İşi geri al işlevi, etiket numarasıyla izlenen fiili ağırlık maddeleri için desteklenmez.

> [!NOTE]
> Fiili ağırlık etiketleriyle ilgili önceki bilgiler, yalnızca, fiili ağırlık ürününde, tamamen izlenen bir fiili ağırlık etiketi boyut izleme yöntemi olduğu zaman (yani, fiili ağırlık kalemi işleme ilkesindeki **Fiili ağırlık etiket boyutu izleme yöntemi** parametresinin ayarı **Ürün boyutları, izleme boyutları ve tüm depolama boyutları** olduğu zaman) geçerlidir. Fiili ağırlık kalemi yalnızca kısmi etiket izlemeli olduğu zaman (yani, fiili ağırlık kalemi işleme ilkesindeki **Fiili ağırlık etiketi boyut izleme yöntemi** parametresinin ayarı **Ürün boyutları, izleme boyutları ve Stok Durumu** olduğu zaman) ek sınırlamalar uygulanır. Bu durumda, etiket ile stok arasında görünürlük kaybolduğu için bazı ek senaryolar desteklenmez.
