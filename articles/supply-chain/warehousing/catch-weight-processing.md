---
title: Ambar yönetimi ile Fiili ağırlık ürün işlemi
description: Bu konuda ambar içinde işin nasıl ve nerede gerçekleştirileceğini belirlemek için iş şablonları ve konum yönergelerinin nasıl kullanılacağı açıklanmaktadır.
author: perlynne
manager: AnnBe
ms.date: 03/18/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSCatchWeightTag, WHSCatchWeightItemHandlingPolicy
ROBOTS: NOINDEX, NOFOLLOW
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2019-1-31
ms.dyn365.ops.version: 8.1.3
ms.openlocfilehash: 6e295456838ca0195a472518b5979dfdc7819f74
ms.sourcegitcommit: 19859d8566a8c7840066b2c10c6b08b67f1b83f4
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/04/2019
ms.locfileid: "1617985"
---
# <a name="catch-weight-product-processing-with-warehouse-management"></a>Ambar yönetimi ile Fiili ağırlık ürün işlemi

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/pivate-preview-banner.md)]


## <a name="feature-exposure"></a>Özellik tanıtımı

Fiili ağırlık ürünlerini kullanmak için Ambar yönetimini kullanmak için işlevi açmak için bir lisans yapılandırma anahtarını kullanmalısınız. (**Sistem yönetimi \> Kurulum \> Lisans yapılandırma** seçeneğine gidin. **Yapılandırma anahtarları** sekmesinde, **Ticari \> Ambar ve Nakliye yönetimi** üzerinde, **Ambar için Fiili ağırlık** seçeneği için onay kutusunu seçin.

> [!NOTE]
> **Hem Ambar ve Taşıma yönetimi** lisans yapılandırması anahtarı hem de **İşlem dağıtımı \> Fiili ağırlık** lisans yapılandırma anahtarlarının da açık olması gerekir.

Lisans yapılandırma anahtarı açıldıktan sonra serbest bırakılan bir ürün oluşturduğunuzda **Fiili ağırlık** seçebilirsiniz. Serbest bırakılan ürünü **Ambar yönetim işlemi** parametresinin seçili olduğu bir depolama boyut grubu ile ilişkilendirebilirsiniz.

Ürünü Ambar yönetimi içinde kullanabilmeden önce fiili ağırlık için bazı temel ürüne özel ayarlar yapmanız gerekir:

- Fiili ağırlık birim (kutu) ve stok birimi (kilogram\[kg\]) arasındaki nominal ağırlık dönüşümünü ürün dönüşüm tanımının bir parçası olarak tanımlayın.
- Minimum ve maksimum ağırlık toleranslarını fiili ağırlık birim ayarlamasının bir parçası olarak tanımlayın.
- Fiili ağırlık biriminin en düşük stok tutma birimi (SKU) olarak tanımlandığı bir birim sıra grubu ayarlayın.
- Fiili ağırlık öge işleme ilkesi ayarlayın.

Daha fazla bilgi için bkz. [Fiili ağırlık ögeleri ayarlamak ve bakımı](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/setting-up-and-maintaining-catch-weight-items)'na bakın.

## <a name="transaction-adjustments"></a>Hareket ayarlamaları

Stokun ambara girdiğindeki ağırlığı, stokun ambardan çıktığındaki ağırlıktan farklı olabileceği için fiili ağırlık ürün işlemenin stoku ayarlaması gerekir.

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

Gerçek ağırlık paketleme istasyonunda konteyner paketleme işlemleri sırasında yakalanırsa, ambar çalışanlarının ağırlığı malzeme çekme işi sırasında yakalamaları gerekmez. Bunun yerine, fiziksel stokun ortalama ağırlığı, paketleme alanına giden çekilen stokun ağırlığı olarak kullanır.

Sayım ve ayarlama düzeltmeleri gibi dahili ambar yönetimi işlemleri için ağırlığın yakalanmış olup olmaması gerektiğini tanımlamak mümkündür. Yakalanmamışsa nominal ağırlık kullanılır.

Ayrıca ağırlığın nasıl yakalanacağını da tanımlayabilirsiniz. İki ana akıştan birinde, fiili ağırlık etiketleri izlenir ve ağırlığı yakalamak için kullanılır. Diğer akışta, fiili ağırlık etiketleri izlenmez.

- **Evet** - Öge fiili ağırlık etiketlerini kullanır. Her bir etiket numarası bir fiili ağırlık birimi (kutusu) temsil eder ve ağrılık ve diğer bilgiler etiket ile ilişkilendirilir. Giden işlemler için etiket ile ilişkilendirilen ağırlık kullanılır.
- **Hayır** – Öge fiili ağırlık etiketlerini kullanmıyor. Giren ve çıkan tartım işlemleri her bir işlem sırasında yakalanan gerçek ağırlıklara dayanmaktadır.

Fiili ağırlık etiketlerini izleme işlemi depolama süresince ağırlıkları değişmeyecek ögeler için kullanılabilir. Ağırlık yalnızca giriş ambar işlemleri sırasında yakalanacaktır. Çıkan işlemler sırasında, fiili ağırlık etiketleri yalnızca taratılır ve etiketlerle ilişkilendirilmiş ağırlıklar çıkış hareket işlemleri için kullanılır.

### <a name="how-to-capture-catch-weight"></a>Fiili ağırlığı yakalamak

Bir fiili ağırlık etiket izleme kullanılırsa, bir etiketin her zaman alınan her bir fiili ağırlık birimi için oluşturulması gerekir ve her bir etiketin her zaman bir ağırlık ile ilişkilendirilesi gerekir.

Örneğin **Kutu** fiili ağırlık birimidir ve sekiz kutudan oluşan bir palet alırsınız. Bu durumda, sekiz benzersiz fiili ağırlık etiketinin oluşturulması ve bir ağırlığın her bir etiket ile ilişkilendirilmesi gerekir. Giriş fili ağırlık etiketine bağlı olarak, tüm sekiz kutunun ağırlığı yakalana bilir ve ortalama ağırlık her bir kutuya dağıtılabilir veya benzersiz bir ağırlık her bir kutu için yakalanır.

Fiili ağırlık etiketi kullanılmadığında, ağırlık her bir birim kümesi için yakalanabilir (örn. her bir plaka ve izleme boyutu için). Alternatif olarak, ağırlık birleştirilmiş düzeye dayanarak toplanabilir, örneğin beş plaka gibi (palet).

Çıkış ağılığı yakalamak için yöntemler için tartımın her bir fiili ağırlık birimi için mi yapılacağını (yani kutu başın) yoksa ağırlığın çekilecek miktara dayanarak mı yapılacağını (örn. üç kutu) tanımlayabilirsiniz. Üretim hattı çekme ve dahili hareket işlemleri için ortalama ağırlığın **Yakalanmadı** seçeneği kullanılırsa kullanılacağını unutmayın.

Fiili ağırlık kar/zarar ayarlamalarıyla sonuçlanan ağırlık yakalamadan ambar yönetimi çekme işlemlerini kısıtlamak için, Giden ağırlık farkı yöntemi kullanılabilir.

## <a name="supported-scenarios"></a>Desteklenen senaryolar

Her iş akışı ambar yönetimi ile fiili ağırlık ürün işlemeyi desteklemez. Aşağıdaki kısıtlamalar şu anda geçerlidir.
 
### <a name="configuring-catch-weight-products-for-warehouse-management-processes"></a>Ambar yönetimi işlemleri için fiili ağırlık ürünlerini yapılandırmak.

- Fiili ağırlık ürünleri için depolama boyut grubu öğeler için değiştirilemez (böylece ambar yönetimi işlemleri bunları kullanabilir).
- Yalnızca formül işlem fiili ağırlık ürünleri için desteklenir (ürün reçetesi değil).
- Fiili ağırlık ürünleri, Sahip boyutu kullanarak bir izleme boyut grubu ile ilişkilendirilemez.
- Fiili ağırlık ürünleri hizmetler olarak kullanılamaz.
- Fiili ağırlık ürünleri, yalnızca öğe model grubunun parası olarak "stoklu ürün" olarak kullanılabilir.
- Fiili ağırlık ürünleri, "Satış işleminde etkin" izleme özelliği ile birlikte kullanılamaz.
- Fiili ağırlık ürünleri, seri numaraları yakalama özelliği ile birlikte kullanılamaz. Bu nedenle, ürünler "boş"tan bir seri numarasına bir çekme/paketleme işleminin parçası olarak aktarılamaz.
- Fiili ağırlık ürünleri, tüketimden önce serileri kaydetme özelliğiyle birlikte kullanılamaz.
- Çeşit özelliği etkin fiili ağırlık ürünleri, çeşit birim ölçümlerini dönüştürme özelliğiyle birlikte kullanılamaz.
- Fiili ağırlık ürünleri perakende "ürün paketi" olarak işaretlenemez.
- Fiili ağırlık ürünleri yalnızca fiili ağırlık işleme birimlerine sahip bir birim sıra grubu, ile fiili ağırlık biriminin en düşük sıralamada olmasıyla kullanılabilir.
- Fiili ağırlık ürünleri için stok birimi yalnızca dönüşüm 1'den büyük bir nominal miktar oluşturduğunda fiili ağırlık birimine dönüştürülebilir.
- Fiili ağırlık ürünler için barkod kurulumu değişken ağırlık ayarını desteklemiyor.
 
### <a name="order-processing"></a>Sipariş işleme

- Ön sevkiyat bildirimi (ASN/sevk yapıları), ağırlık bilgisini desteklemiyor.
- Sipariş miktarı fiili ağırlık birimine dayanarak korunmalıdır.
 
### <a name="inbound-warehouse-processing"></a>Giriş ambar işleme

- Plakaları almak, ağırlıkların kayıt sırasında atanmasını gerektirir çünkü ağırlık bilgisi ön sevkiyat bildiriminin parası olarak desteklenmez. Fiili ağırlık etiket işlemleri kullanıldığında, fiili ağırlık birimi başına etiket numarası ile atanması gerekir.
 
### <a name="inventory-and-warehouse-operations"></a>Stok ve ambar operasyonları

- Karantina emirlerinin el ile oluşturulması fiili ağırlık ürünleri için desteklenmiyor.
- İş ile ilgili olan stokun el ile taşıması fiili ağırlık ürünleri için desteklenmiyor.
- Plakaların birleştirilmesi fiili ağırlık ürünleri için desteklenmiyor.
- Ambar stokunu başlatmak için plaka yükleme fiili ağırlık ürünleri için desteklenmiyor.
- Toplu iş dengelemesi işlemleri fiili ağırlık ürünleri için desteklenmiyor.
- Negatif fiziksel stokun işlenmesi fiili ağırlık ürünleri için desteklenmiyor.
- Stok işaretleme fiili ağırlık ürünleri için kullanılamıyor.
 
### <a name="outbound-warehouse-processing"></a>Giden ambar işleme

- Küme çekme için işlev fiili ağırlık ürünleri için desteklenmiyor.
- Çekme ve paketleme amber işleme fiili ağırlık ürünleri için desteklenmiyor.
- Fiili ağırlık ürünleri için bir iş şablonunda tanımlanan bir iş otomatik olarak yürütülebilir.
- İş ters işlem için işlev fiili ağırlık ürünleri için desteklenmiyor.
- Fiili ağırlık ürünleri için el ile işleme istasyon işleme, işin konteynerler kapatıldıktan sonra oluşturulduğu durumlarda desteklenmiyor.
- Adet başına tarama işlevi, fiili ağırlık ürünleri için desteklenmiyor.
 
### <a name="production-processing"></a>Üretim işleme

- Fiili ağırlık ürünleri için yalnızca formül ürünleri çiin toplu iş siparişleri desteklenir.
- Kanban işlevi fiili ağırlık ürünleri için desteklenmiyor.
- Fiili ağırlık ürünleri için seri numaralar tüketimden önce kaydedilemez.
- Plaka ters işlem için işlev fiili ağırlık ürünleri için desteklenmiyor.
- Fiili ağırlık ürünleri için tamamlandı olarak raporlamak bir seri numarası olarak kaydedilemez.

### <a name="transportation-management-processing"></a>Taşıma yönetimi işleme

- Yükleme binası workbench işleme fiili ağırlık ürünleri için desteklenmiyor.
- Taşıma talebi satırları fiili ağırlık ürünleri için desteklenmiyor.
 
### <a name="other-restrictions-and-behaviors-for-catch-weight-product-processing-with-warehouse-management"></a>Ambar yönetimi ile fiili ağırlık ürün işleme için diğer kısıtlamalar ve davranışlar

- Kullanıcının izleme boyutlarını belirlemesi istenmediği malzeme çekme işlemleri sırasında, ağırlık ataması ortalama ağırlığa dayalı olarak yapılır. Bu davranış, örneğin bir izleme boyutu kombinasyonu aynı konumda kullanıldığında ve bir kullanıcı çekmeyi işledikten sonra konumda yalnızca bir izleme boyutu değeri kalırsa ortaya çıkar.
- Stok bir ambar yönetimi işleminde yapılandırılmış bir fiili ağırlık ürünü için rezerve edilirse, rezervasyon tanımlanan minimum ağırlığa dayanarak gerçekleştirilir, bu miktar eldeki son işlem miktarı olsa bile. Bu davranış, ambar yönetimi işlemleri için yapılandırılmamış ögelerin davranışından farklıdır.
- Ağırlığı kapasite hesaplamalarının parçası olarak kullanan işlemlerde (dalga eşikleri, iş maksimum molalar, konteyner maksimumları, konum yük kapasiteleri ve benzeri), stokun gerçek ağırlığını kullanmayın. Bunun yerine, işlemler ürün için tanımlanmış fiziksel işleme ağırlığına dayanır.
- Genel olarak, Perakende işlevi fiili ağırlık ürünleri için desteklenmez.
 
### <a name="catch-weight-tags"></a>Fiili ağırlık etiketleri

Şu anda, fiili ağırlık etiketleri için işlevsellik yalnızca aşağıdaki senaryoların bir parçası olarak desteklenir:

- İşlem satın alma siparişi uygulaması alındığında.
- Ambar uygulaması aracılığıyla yük alım işlendiğinde.
- Satınalma siparişi yükü ile ilgili plaka alındığında, yük ataması alınma işlemi sırasında talep edilir. Bunun aksine, transfer emri alımı için transfer emri için sevkiyat verisindeki ağırlık kullanılır.
- Ambar olmayan yönetim işlemi ambarından gelen transfer emri ögesi ve satır alma için.
- Satış iade emri alımının işlenmesi fiili ağırlık etiketlerini kaydedebilir, ancak işleme etiketler belirli bir satış siparişi satırı için sevk edilen etiketlerle aynıysa doğrulanmaz.
- Ambar uygulaması kullanılarak bir stok durumu değişikliği işlendiğinde.
- Bir ambar transferi ambar uygulaması kullanılarak gerçekleştirildiğinde.
- Ambar uygulaması aracılığıyla giriş ve çıkış ayarlaması işlendiğinde.
- Çekme işi satış ve transfer emirleri için işlendiğinde. (Fiili ağırlık etiketleri üretim bileşeni çekme için kaydedilemez.)
- Çekilen miktarlar yük satırlarından çıkartıldığında, konteynerlerin kullanılmasından bağımsız olarak.
- Ürünler bir paketleme istasyonunda konteynerlere paketlendiğinde.
- Konteynerler yeniden açıldığında.
- Formül ürünleri ambar uygulaması kullanarak tamamlandı olarak raporlanırsa.
- Taşıma yükleri ambar uygulaması kullanılarak işlendiğinde.

Bir fiili ağırlık etiketi, bir ambar uygulaması işlemi kullanılarak veya form içinde el ile oluşturularak veya bir veri varlığı işlemi kullanılarak oluşturulabilir. Bir fiili ağırlık etiketi, bir gelen kaynak belgesi satırıyla ilişkilendirilirse, örneğin bir satınalma siparişi satırı gibi, etiket kaydedilir. Satır, giden işlem için kullanılıyorsa. Etiket, güncelleştirilir ve sevk edilir.
