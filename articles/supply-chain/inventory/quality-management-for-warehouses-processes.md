---
title: Ambar işlemleri için kalite yönetimi
description: Bu konuda, ambar işlemleri özelliği için Kalite yönetimi hakkında bilgiler verilmektedir. Bu özellik kalite yönetimi yeteneklerini genişletir ve kullanıcıların gelişmiş ambar yönetimini kullanarak madde örnekleme kontrollerini ambar teslim alma işlemiyle tümleştirmelerini sağlar.
author: Henrikan
manager: tfehr
ms.date: 04/02/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2020-04-02
ms.dyn365.ops.version: Release 10.0.11
ms.openlocfilehash: c11821db796220cd61d776428fb6890480f27b8e
ms.sourcegitcommit: 6d6aa016c4971b0673d461b82fd80b060ae5f7a1
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/17/2020
ms.locfileid: "3269449"
---
# <a name="quality-management-for-warehouse-processes"></a>Ambar işlemleri için kalite yönetimi

_Ambar işlemleri için kalite yönetimi_ özelliği kalite yönetimi yeteneklerini genişletmenize ve gelişmiş ambar yönetimini kullanarak madde örnekleme kontrollerini ambar teslim alma işlemiyle tümleştirmenize olanak tanır. Ambar işi, yüzdeyi veya sabit miktarı ya da her *n*'înci plakayı temel alarak stoğu kalite kontrol konumuna taşımak için otomatik olarak oluşturulabilir. Bir kalite emri tamamlandıktan sonra, kalite sonuçlarına göre stoku sürecin bir sonraki konumuna taşımak için iş otomatik olarak oluşturulabilir.

_Ambar işlemleri için kalite yöntemleri_ özelliği, temel kalite yönetimi özelliğinin yeteneklerini uzatır. Kalite kontrol yerleşimine gönderilen stok için kalite emirleri oluşturma seçeneği sunar, ancak kalite emirleri her zaman gerekli değildir. Bu nedenle, ambar işine dayalı hafif bir kalite kontrol süreci sağlar.

## <a name="turn-on-the-quality-management-for-warehouse-processes-feature"></a>Ambar işlemleri için kalite yönetimi özelliğini açma

Bu özelliği kullanabilmeniz için sisteminizde etkinleştirmeniz gerekir. Yöneticiler özellik durumunu denetlemek ve etkinleştirmek için [özellik yönetimi](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) ayarlarını kullanabilir. **Özellik yönetimi** çalışma alanındabu özellik aşağıdaki şekilde listelenir:

- **Modül:** *Ambar yönetimi*
- **Özellik adı:** *Ambar işlemleri için kalite yönetimi*

## <a name="key-benefits"></a>Temel avantajlar

_Ambar işlemleri için kalite yönetimi_ özelliği, kalite kontrolü için gerekli olan stok miktarını kalite kontrol yerleşimine taşımak amacıyla, teslim alma sürecinin bir parçası olarak otomatik iş oluşturur. Teslim alınan miktar kalite kontrolü için gereken miktarı aşarsa (madde örnekleme kurulumuna göre), fazlalık miktar konum yönergesi kurulumunda tanımlanan bir gelen yerleşime taşınacaktır. Kalite emri doğrulandıktan sonra, kalite emrinin miktarını doğrulama sonucuna ve konum yönergesi kurulumuna göre yeni bir gelen veya iade konumuna taşımak için otomatik olarak iş oluşturulur. Yalnızca bir kalite kontrole veya bir kalite kontrolden taşınması gereken miktara sahip otomatik iş oluşturma, tümleşik bir işlem deneyimi sağlar.

> [!NOTE]
> _Ambar işlemleri için kalite yönetimi_ özelliği açık olduğunda, el ile işlemden yararlanmaya devam edebilirsiniz. El ile işlemde stok hareketi ve şablona göre hareket, bir kalite kontrol yerleşiminden alınan stoku yeni yerleşime taşımak amacıyla ambar çalışanı tetiklemesi sağlamak için kullanılır. Ayrıca, madde örnekleme kurulumunu dikkate almadan, stoğu kendi bütünlüğü içinde bir teslim alma yerleşiminden bir kalite kontrol yerleşimine taşıyan bir gelen yerleşim yönergesi de ayarlayabilirsiniz.

## <a name="quality-management-and-the-quality-management-for-warehouse-processes-feature"></a>Kalite yönetimi ve Ambar işlemleri için kalite yönetimi özelliği

_Ambar işlemleri için kalite yönetimi_ özelliği açık olduğunda, temel ambar yönetimi ve kalite yönetimi varlıklarının kurulumunu değiştirir. Aşağıdaki şekil, ambar işlemleri için kalite emirlerini etkinleştiren varlıkların genel görünümünü sağlar. Parantez içindeki metin, _Ambar yönetimi işlemleri için kalite yönetimi_ özelliği açılmadan önce kalite yönetimi uygulandığında önerilen eylemleri belirtir.

![Kalite yönetimi varlıkları](media/quality-management-entity-diagram.png "Kalite yönetimi varlıkları")

## <a name="enablers-the-quality-item-sampling-and-quality-order-work-order-types"></a>Etkinleştiriciler: Kalite madde örnekleme ve Kalite emri iş emri türleri

_Ambar işlemleri için kalite yönetimi_özelliği, iş oluşturma işlemini etkinleştiren iki iş emri türü sunar:

- **Kalite maddesi örnekleme** – Bu iş emri türü, kayıtlı stoğu kalite kontrolüne taşıyan bir iş oluşturmak için kullanılır.
- **Kalite emri** – Bu iş emri, yerleşim yönergesi kurulumunu temel alarak, stoğu kalite kontrolünden yeni bir yerleşime taşıyan bir iş oluşturmak için kullanılır.

### <a name="work-classes-location-directives-and-work-templates"></a>İş sınıfları, yerleşim yönergeleri ve iş şablonları

_Kalite maddesi örnekleme_ ve _Kalite emri_ iş emri türleri yerleşim yönergeleri, iş sınıfları ve iş şablonları tarafından kullanılır.

Stoğu kalite kontrolüne taşımak için ambar işi otomatik olarak oluşturulmadan önce, sisteminizi ayarlamak için aşağıdaki adımları izlemeniz gerekir.

1. _Kalite maddesi örnekleme_ ve _Kalite emri_ iş emri türleri için ayrı iş sınıfları oluşturun. Bu şekilde, uygun işin iki iş emri türüne dayalı olarak otomatik olarak oluşturulabilmesini ve bu işin Ambarlama mobil uygulaması (WMA) kullanılarak çalıştırılabilmesini sağlarsınız.
1. Her iş emri türü için iş şablonu ayarlama:

    - Kayıtlı stoğu otomatik olarak kalite kontrol konumuna taşımak için _Kalite maddesi örnekleme_ iş emri türünü kullanan bir iş şablonu ayarlayın.
    - Kalite kontrol tamamlandıktan sonra stoğu bir kalite kontrol yerleşiminden taşımak için _kalite emri_ iş emri türünü kullanan bir iş şablonu ayarlayın.

1. Her iş emri türü için, stoğun taşınması gereken doğru kalite kontrol yerleşimlerini uygulayan yerleşim yönergeleri ayarlayın. Kalite kontrol tamamlandıktan sonra, _Kalite emri_ iş emri türünün yerleşim yönergesi, stoğun kalite kontrol konumundan dışarı taşınabilmesi için yeni bir hedef yerleşim seçilmesini sağlar.
1. Teslim alınan stoğun kalite kontrol konumuna taşınmasını ve kalite kontrolünden geçen veya geçemeyen sotuğun kalite kontrol yerleşiminden yeni bir konuma taşınmasını desteklemek için ilgili mobil cihaz menü öğelerini ayarlayın.

Bu kurulumun nasıl tamamlandığını gösteren adım adım bir örnek için bu konunun sonundaki [örnek senaryoya](#example-scenario) bakın.

## <a name="enable-a-warehouse-for-quality-management"></a>Ambarı kalite yönetimi için etkinleştirme

Belirli bir ambar için _Ambar işlemleri için kalite yönetimi özelliği_ uygulanmadan önce, özelliği bu ambar için kullanılabilir hale getirmek üzere aşağıdaki adımları izlemeniz gerekir.

1. **Ambar yönetimi \> Kurulum \> Ambar  \> Ambarlar**'a gidin.
1. Kalite yönetimi için etkinleştirilecek ambarı seçin.
1. **Ambar** hızlı sekmesinde **Ambar işlemleri için kalite emrini etkinleştir** seçeneğini _Evet_ olarak ayarlayın. (Bu seçenek yalnızca ambar yönetimi işlemlerini kullanan ambarlar için _Evet_ olarak ayarlanabilir.)

**Ambar işlemleri için kalite emrini etkinleştir** seçeneği _Evet_olarak ayarlandığında, kalite ilişkisi kurulumu _Ambar işlemleri için kalite yönetimi_ özelliğinin seçili ambar için geçerli olup olmadığını kontrol eder. Seçeneğin ayarını istediğiniz zaman _Hayır_ olarak değiştirebilirsiniz. Bu durumda, kalite ilişkisi kurulumuna bakılmaksızın özellik artık ambar için geçerli olmayacaktır.

## <a name="quality-control"></a>Kalite kontrol

_Ambar işlemleri için kalite yönetimi_ özelliği, kalite ilişkileri ve madde örnekleme için çeşitli temel ayarları denetler.

### <a name="quality-associations"></a>Kalite ilişkileri

Her [kalite ilişkisi kaydı](enable-quality-management.md) aynı zamanda oluşturulan kalite emirleri için geçerli olacak testler kümesini, kabul edilebilir kalite düzeyini (AQL) ve örnek alma planını da tanımlamaktadır. Bir kalite ilişkisi kaydı ayarlamak için bu adımları izleyin.

1. **Stok yönetimi \> Kurulum \> Kalite kontrol \> Kalite ilişkileri**'ne gidin.
1. Üzerinde çalıştığınız madde veya grup için veya tüm maddeler için kalite ilişkisi girişi oluşturun veya seçin.
1. **Koşullar** hızlı sekmesinde, **Uygulanabilir ambar türü** alanını aşağıdaki değerlerden biriyle ayarlayın:

    - **Yalnızca ambar işlemleri için kalite yönetimi** – _Ambar işlemleri için kalite yönetimi_ özelliğini etkinleştirin. Bu değeri, yalnızca referans türü *Satınalma* veya *Üretim* ise seçebilirsiniz.
    - **Tümü** - _Ambar işlemleri için kalite yönetimi_ özelliğini devre dışı bırakın. *Satınalma* ve *Üretim* dışındaki tüm referans türleri için bu değeri seçin.

> [!NOTE]
> _Ambar işlemleri için kalite yönetimi_ özelliği, yalnızca kaynak belge satırındaki madde gelişmiş ambar yönetimi işlemlerini kullanıyorsa ve **Ambar işlemleri için kalite emrini etkinleştir** seçeneği kaynak belge satırındaki ambar için _Evet_ olarak ayarlanmışsa etkinleşir.

Her madde kayıtlı (veya tamamlandı olarak bildirildi) olduğundan, sistem hangi kalite ilişkilerinin uygulanacağını saptar.

_Ambar işlemleri için kalite yönetimi_ özelliği açık olduğunda, ilgili ambar türü, kalite ilişkisi arama hiyerarşisinin dördüncü arama grubuna mantıksal olarak eklenir. Aşağıdaki tablo arama hiyerarşisinin mantıksal gösterimini sağlar.

| Arama grubu | Tanım |
|---|---|
| Grup 1 | Her kalite ilişkisi için **Referans türü**, **Olay türü** ve **Yürütme eşleştirme** değerlerini öğeye göre denetleyin. Kaynak belge satırıyla ilgili bir eşleşme varsa, grup 2'ye geçin. |
| Grup 2 | Her kalite ilişkisi için, **Madde kodu** değerini (_Tablo_, _Grup_ veya _Tümü_) maddeye göre denetleyin. _Tablo_, _Grup_ seçeneğine göre daha özel ve _Grup_ _Tümü_ seçeneğinden daha özeldir. _Tablo_ (belirli bir madde) için bir eşleşme varsa , grup 3'e geçin. _Tablo_ için bir eşleşme yoksa, _Grup_ için bir eşleşme arayın. _Grup_ için eşleşme yoksa, _Tümü_ geçerli olur. Eşleşme varsa, grup 3'e geçin. |
| Grup 3 | Her kalite ilişkisi için, **Hesap kodu** ve **Kaynak kodu** değerlerini maddeye göre denetleyin. Uygulanan mantık, **Madde kodu** değeri için geçerli olan mantığa benzer. |
| Grup 4 | Her kalite ilişkisi için, **İlgili ambar türü** değerini (_Yalnızca ambar işlemleri için kalite yönetimi_ veya _Tümü_) maddeye göre denetleyin. **Ambar işlemleri için kalite emrini etkinleştir** seçeneği kaynak belgedeki ambar için _Evet_ olarak ayarlanmışsa ve kaynak belge satırındaki madde _Ambar yönetim işlemlerini kullan_ olarak ayarlanmışsa, her ikisinin de mevcut olması durumunda,  _Yalnızca ambar işlemleri için kalite yönetimi_ için bir eşleşmenin olduğu ilişkiler ve _Tümü_ için eşleşmelerin olduğu ilişkiler paralel olarak geçerli olacaktır. **Ambar işlemleri için kalite yönetimini etkinleştir** özelliği kaynak belgedeki ambar için _Hayır_ olarak ayarlanırsa seçeneği ve kaynak belge satırındaki madde  _Ambar yönetimi işlemlerini kullan_ olarak ayarlanırsa, yalnızca kalite yönetimi geçerli olur. |

Örneğin, **Ambar işlemleri için kalite emrini etkinleştir** seçeneğinin _Evet_ olarak ayarlandığı bir ambar tanımladınız ve *Satınalma* referans türü için tanımlanmış iki kalite ilişkilendirmeniz var: biri tüm maddeler için, diğeri ise *Kayıt* olay türü için. İki kalite ilişkisi arasındaki tek fark **Geçerli ambar türü** değeridir: bir kalite ilişkisi için _Tümü_ diğeri için _Yalnızca ambar işlemleri için kalite yönetimi_ olarak ayarlanır. Bu durumda, her iki kalite ilişkisi de eşit derecede özeldir ve her ikisi de uygulanabilir.

Kalite ilişkileri için **Test grubu** alanının değeri de bir faktördür. Bu alan uygulanması gereken test yordamını tanımlar. **Test grubu** değeri her iki ilişki için aynıysa, **Geçerli ambar türü** diğerinin _Yalnızca ambar işlemleri için kalite yönetimi_ olduğu kalite ilişkisi için yalnızca bir kalite emri oluşturulur. **Test grubu** değeri her iki ilişki için aynı değilse, iki kalite emri oluşturulur. İlk kalite emri, **Geçerli ambar türü** değerinin _Yalnızca ambar işlemleri için kalite yönetimi_ olduğu kalite ilişkisi için ayarlanır. İkinci kalite emri, **Geçerli ambar türü** değerinin _Tümü_ olduğu kalite ilişkisi için ayarlanır.

> [!NOTE]
> _Yalnızca ambar işlemleri için kalite yönetimi_ değeri, grup 1 ve 2 için kalite ilişkileri ölçütü aynı olduğunda ve test grubu aynı olduğunda _Tümü_'ne göre daha özel kabul edilir. Test grupları farklı olduğunda yalnızca iki kalite emri oluşturulur.

#### <a name="reference-types"></a>Referans türleri

**Referans türü** değeri _Satınalma_ ve **Geçerli ambar türü** değeri _Yalnızca ambar işlemleri için kalite yönetimi_ olduğunda, **İşlem** hızlı sekmesindeki **Olay türü** alanının  _Kayıt_ olarak ayarlanması gerekir. _Ambar işlemleri için kalite yönetimi_ özelliğini kullanırken, _Satınalma_ referans türü için yalnızca _Kayıt_ olay türü desteklenir.

#### <a name="quality-processing-policy"></a>Kalite işleme ilkesi

_Ambar işlemleri için kalite yönetimi_ özelliği, işin yalnızca madde örneklemesine dayalı olarak oluşturulmasına izin verir. Bu nedenle, hafif bir işlem yapılmasına olanak tanır. İşin oluşturulduğu stok, kalite ilişkisiyle ilişkilendirilmiş madde örneklemesine bağlıdır. Hafif işlem kullanıldığında, bir çalışan kalite kontrol konumunda miktarı yerine koyduktan sonra kalite emri gerekiyorsa kalite departmanı el ile bir kalite emri oluşturabilir.

**Kalite emri işlemi** hızlı sekmesindeki **Kalite işleme ilkesi** alanı, bir maddeyi kalite kontrol konumuna taşımak için iş oluşturulurken bir kalite emrinin oluşturulup oluşturulmayacağını denetler. Bu alan, _Kalite emri oluştur_ veya _Yalnızca iş oluştur_ olarak ayarlanabilir. Varsayılan değer _Kalite emri oluştur_'dur.

> [!NOTE]
> Kalite emirlerini el ile veya otomatik olarak oluşturmuş olmanıza bakılmaksızın, kalite emri doğrulanmış olarak işaretlendiğinde sistem, maddeleri kalite kontrol konumundan dışarı taşımak için otomatik olarak iş oluşturur.

Kalite emri işinin oluşturulması kalite ilişkisi kurulumuyla ilgili değildir. **İş emri türü** değeri *Kalite emri* olan bir iş şablonu varsa ve bu iş şablonu için sorgu ölçütleri karşılanırsa, kalite emri doğrulaması kalite emri işi oluşturma işlemini tetikler.

#### <a name="referenced-item-sampling"></a>Başvurulan madde örnekleme

Her kalite ilişkisinin bir madde örneklemesine başvurması gerekir. Madde örnekleme, kalite kontrol için gönderilecek miktarı tanımlar. **Geçerli ambar türü** değerinin _Yalnızca ambar işlemleri için kalite yönetimi_ olduğu kalite ilişkilerine uygulanacak şekilde ayarlanır. Madde örneklemesi için **Örnekleme kapsamı** değeri _Yük_ veya _Sevkiyat_ ise veya **Miktar belirtimi** değeri _Tam plaka_ ise, madde örneklemesine yalnızca **Geçerli ambar türü** değerinin _Yalnızca ambar işlemleri için kalite yönetimi_ olduğu kalite ilişkileri tarafından başvurulabilir.

_Yalnızca ambar işlemleri için kalite yönetimi_ ambar türünü kullanan bir madde örnekleme tanımlarsanız, _Ambar işlemleri için kalite yönetimi_ özelliğini kullanmayan bir kalite ilişkisinden başvurmaya çalıştığınızda hata alırsınız.

> [!NOTE]
> Tam durdurma kullanan madde örnekleme, **Geçerli ambar türü** alanının _Yalnızca ambar işlemleri için kalite yönetimi_ olarak ayarlandığı kalite ilişkileri için desteklenmez.

### <a name="item-sampling"></a>Madde örnekleme

Madde örnekleme, kalite kontrolü için maddelerin ne sıklıkta gönderildiğini denetler. _Ambar  işlemleri için kalite yönetimi_ özelliği _Madde örnekleme kapsamı_ kavramını sunar. Sistem, kalite emirlerinin ve/veya kalite maddesi örnekleme işinin ve kalite emri işinin oluşturulup oluşturulmayacağını ve nasıl oluşturulacağını değerlendirirken, madde örnekleme kapsamını kullanır.

Madde örneklemesi ayarlamak için **Stok yönetimi \> Kurulum \> Kalite kontrol \> Madde örnekleme**'ye gidin ve **Örnekleme kapsamı** alanını aşağıdaki değerlerden birine ayarlayın:

- **Sipariş** - Kalite emirlerinin ve/veya kalite maddesi örnekleme işinin ve kalite emri işinin oluşturulup oluşturulmayacağını ve nasıl oluşturulacağını değerlendirmede kaynak belge satırı temel alınır. Bu değer varsayılan değerdir ve seçildiğinde, _Ambar işlemleri için kalite yönetimi_ özelliği açık olmadığında nasıl çalışıyorsa aynı şekilde çalışır.
- **Yük** – Yükler, bir kalite emrinin ve/veya işinin oluşturulup oluşturulmayacağını ve nasıl oluşturulacağını değerlendirmede temel olarak kullanılır. Bu değer yalnızca _Ambar işlemleri için kalite yönetimi_ özelliği açık olduğunda kullanılabilir.
- **Sevkiyat** – Sevkiyatlar, bir kalite emrinin ve/veya işinin oluşturulup oluşturulmayacağını ve nasıl oluşturulacağını değerlendirmede temel olarak kullanılır. Bu değer yalnızca _Ambar işlemleri için kalite yönetimi_ özelliği açık olduğunda kullanılabilir.

> [!NOTE]
> **Örnekleme kapsamı** alanı *Yük* veya *Sevkiyat* olarak ayarlandığında, varsa yük varlığı ve sevkiyat varlıkları kullanılır. Kullanılabilir değillerse, sipariş varlığı kullanılır.

_Ambar işlemleri için kalite yönetimi_ özelliği ayrıca, *Miktar belirtimi* alanı için **Tam plaka** değerini sağlar. Bu değer, plakaları temel alarak kalite emri işi ve kalite madde örneklemesi işi oluşturulmasını destekler. Bu değeri seçtiğinizde, aşağıdaki değişiklikler gerçekleşir:

- **Sayımı maddeye göre böl** seçeneği ve **İşlem** hızlı sekmesindeki **n'inci plaka başına** alanı kullanılabilir hale gelir.
- **Örnekleme miktarı** hızlı sekmesindeki **Değer** alanı kullanılamaz duruma gelir.
- **Güncelleştirilen miktar başına**, **Konum** ve **Plaka** seçeneklerinin tümü *Evet* olarak ayarlanır ve ayarlar değiştirilemez.

**Sayımı maddeye göre böl** seçeneği, plaka sayısının madde başına mı yoksa örnekleme kapsamındaki tüm maddeler üzerinden mi değerlendirileceğini denetler. Ürün çeşitleri aynı madde gibi kabul edilir. Bu seçenek ayrıca her bir madde için plaka sayısının sıfırlanıp sıfırlanmayacağını da denetler.

**n'inci plaka başına** alanının değeri, kalite emirlerinin kayıtlı madde sayısıyla ilişkili olarak kaç kez oluşturulduğunu kontrol eder. Örneğin, *3* değeri ilk maddeden başlayarak, her üçüncü maddeyi kalite kontrole gönderir. Değer 0'dan (sıfır) fazla olmalıdır.

Çalışanlar WMA kullanarak maddeleri teslim alırken, sistem her gelen madde için kalite ilişkisinin ayarlanıp ayarlanmayacağını doğrular. Kalite ilişkisi ayarlanmışsa sistem kalite emirlerini, kalite maddesi örnekleme işini ve satınalma siparişi işinin nasıl oluşturulacağının belirlenmesi için o kalite ilişkisi için yapılandırılan madde örnekleme kaydını kullanır.

> [!NOTE]
> Web istemcisinde giriş kaydı yapıldığında (küçük kayıt sayfası veya satınalma siparişi satırları için madde varış günlüğü kullanılarak), kurulum ne olursa olsun kalite maddesi örnekleme işi veya satınalma siparişi işi oluşturulmaz. Bunun yerine, bir kalite ilişkisiyle eşleşen maddeler için, yalnızca kalite emirlerinin oluşturulmasını denetlemek amacıyla referansta bulunulan madde örneklemesi kullanılır.

## <a name="examples-of-automatic-generation-of-quality-orders"></a>Kalite emirlerinin otomatik oluşturulmasına ilişkin örnekler

Aşağıdaki örnekler, **Geçerli ambar türü** alanı _Yalnızca ambar işlemleri için kalite yönetimi_ olarak ayarlandığında, kalite ilişkisi kurulumunun ve ilişkili madde örneklemenin kalite emirlerinin oluşturulmasını nasıl etkilediğini gösterir.

**Miktar belirtimi** değeri _Tam plaka_ olduğunda, **n'inci plaka başına** alanı, hangi plaka kalite madde örnekleme işinin oluşturulduğunu kontrol eder. İlk plaka her zaman kalite kontrolüne gider ve bu alanın değeri, bu plakanın ardından gelen her *n*'inci plakanın da kalite kontrole gitmesi gerektiğini belirtir.

Aşağıdaki örneklerin **Referans türü** değeri _Satınalma_'dır ve **Olay türü** değeri *Kayıt*'tır.

| Örnekleme kapsamı | Miktar belirtimi | Güncelleştirilen miktar başına | Depolama boyutu başına | Maddeye göre mola sayısı | n. plaka başına | Sonuç |
|---|---|---|---|---|---|---|
| Sipariş | Tam plaka | Evet _(kilitli/düzenlenemez)_ | <p>Konum: Evet</p><p>Plaka: Evet _(kilitli/düzenlenemez)_</p> | No | 3 | <p>**Sipariş satırı miktarı: 100 EA**</p><ol><li>20 EA, LP1 için WMA'daki kayıt girişi<p>20 EA için kalite madde örneklemesi işi</p><p>20 EA için kalite emri 1</p></li><li>20 EA, LP2 için WMA'daki kayıt girişi<p>20 EA (yerine koyma) için satınalma siparişi işi</p></li><li>20 EA, LP3 için WMA'daki kayıt girişi<p>20 EA (yerine koyma) için satınalma siparişi işi</p></li><li>20 EA, LP4 için WMA'daki kayıt girişi<p>20 EA için kalite madde örneklemesi işi</p></li><li>20 EA, LP5 için WMA'daki kayıt girişi<p>20 EA (yerine koyma) için satınalma siparişi işi</p></li></ol> |
| Sipariş | Sabit miktar = 1 | Evet | <p>Konum: Evet</p><p>Plaka: Evet</p> | No | Geçerli değil | <p>**Sipariş satırı miktarı: 100**</p><ol><li>20 EA, LP1 için WMA'daki kayıt girişi<p>1 EA için kalite madde örneklemesi işi</p><p>1 EA için kalite emri 1</p><p>19 EA (yerine koyma) için satınalma siparişi işi</p></li><li>20 EA, LP2 için WMA'daki kayıt girişi<p>1 EA için kalite Madde örneklemesi işi</p><p>1 EA için kalite emri 1</p><p>19 (yerine koyma) için satınalma siparişi işi</p></li><li>20 EA, LP3 için WMA'daki kayıt girişi<p>1 EA için kalite madde örneklemesi işi</p><p>1 EA için kalite emri 1</p><p>19 EA (yerine koyma) için satınalma siparişi işi</p></li><li>20 EA, LP4 için WMA'daki kayıt girişi<p>1 EA için kalite madde örneklemesi işi</p><p>1 EA için kalite emri 1</p><p>19 EA (yerine koyma) için satınalma siparişi işi</p></li><li>20 EA, LP5 için WMA'daki kayıt girişi<p>1 EA için kalite madde örneklemesi işi</p><p>1 EA için kalite emri 1</p><p>19 EA (yerine koyma) için satınalma siparişi işi</p></li></ol> |
| Sipariş | Yüzde = 10 | No | <p>Konum: Hayır</p><p>Plaka: Hayır</p> | No | Geçerli değil | <p>**Sipariş satırı miktarı: 100 EA**</p><ol><li>50 EA, LP1 için WMA'daki kayıt girişi<p>10 EA için kalite madde örneklemesi işi</p><p>10 EA için kalite emri 1</p><p>40 EA (yerine koyma) için satınalma siparişi işi</p></li><li>50 EA, LP2 için WMA'daki kayıt girişi<p>50 EA (yerine koyma) için satınalma siparişi işi</p></li></ol> |
| Yükle | Yüzde = 5 | Evet _(kilitli/düzenlenemez)_ | <p>Konum: Hayır</p><p>Plaka: Hayır</p> | No | Geçerli değil | <p>**Sipariş satırı miktarı: 500 EA**</p><p>**İki yük: ilk yük 200 EA, ikinci yük 300 EA**</p><ol><li>100 EA için ilk yük için WMA'da kayıt girişi<p>5 EA için kalite madde örneklemesi işi</p><p>5 EA için kalite emri 1</p><p>95 EA (yerine koyma) için satınalma siparişi işi</p></li><li>100 EA için ilk yük için WMA'da kayıt girişi<p>5 EA için kalite madde örneklemesi işi</p><p>5 EA için kalite emri 1</p><p>95 EA (yerine koyma) için satınalma siparişi işi</p></li><li>300 EA için ikinci yük için WMA'da kayıt girişi<p>15 EA için kalite madde örneklemesi işi</p><p>15 EA için kalite emri 1</p><p>285 EA (yerine koyma) için satınalma siparişi işi</p></li></ol> |
| Sipariş | Yüzde = 10 | No | <p>Konum: Evet</p><p>Plaka: Evet</p> | No | Geçerli değil | <p>**Sipariş satırı miktarı: 100**</p><ol><li>50 EA, LP1 için WMA'daki kayıt girişi<p>5 EA için kalite madde örneklemesi işi</p><p>5 EA için kalite emri 1</p><p>45 EA (yerine koyma) için satınalma siparişi işi</p></li><li>50 EA, LP2 için WMA'daki kayıt girişi<p>5 EA için kalite madde örneklemesi işi</p><p>5 EA için kalite emri 1</p><p>45 (yerine koyma) için satınalma siparişi işi</p></li></ol> |
| Yükle | Tam plaka | Evet _(kilitli/düzenlenemez)_ | <p>Konum: Evet</p><p>Plaka: Evet _(kilitli/düzenlenemez)_</p> | No | 3 | <p>**İki madde:**</p><ul><li>**A maddesi için sipariş satırı miktarı: 120 EA (4 palet)**</li><li>**B maddesi için sipariş satırı miktarı: 90 EA (3 palet)**</li></ul><p>**Bir yük, her sipariş satırıyla iyi yük satırı**</p><ol><li>30 EA, LP1, madde A için WMA'daki kayıt girişi<p>30 EA için kalite madde örneklemesi işi</p><p>30 EA için kalite emri 1</p></li><li>30 EA, LP2, madde A için WMA'daki kayıt girişi<p>30 EA (yerine koyma) için satınalma siparişi işi</p></li><li>30 EA, LP3, madde A için WMA'daki kayıt girişi<p>30 EA (yerine koyma) için satınalma siparişi işi</p></li><li>30 EA, LP4, madde A için WMA'daki kayıt girişi<p>30 EA için kalite madde örneklemesi işi</p><p>30 EA için kalite emri 1</p></li><li>30 EA, LP5, madde B için WMA'daki kayıt girişi<p>30 EA (yerine koyma) için satınalma siparişi işi</p></li><li>30 EA, LP6, madde B için WMA'daki kayıt girişi<p>30 EA (yerine koyma) için satınalma siparişi işi</p></li><li>30 EA, LP7, madde A için WMA'daki kayıt girişi<p>30 EA için kalite madde örneklemesi işi</p><p>30 EA için kalite emri 1</p></li></ol> |
| Yükle | Tam plaka | Evet _(kilitli/düzenlenemez)_ | <p>Konum: Evet</p><p>Plaka: Evet _(kilitli/düzenlenemez)_</p> | Evet | 3 | <p>**İki madde:**</p><ul><li>**A maddesi için sipariş satırı miktarı: 120 EA (4 palet)**</li><li>**B maddesi için sipariş satırı miktarı: 90 EA (3 palet)**</li></ul><p>**Bir yük, her sipariş satırıyla iyi yük satırı**</p><ol><li>30 EA, LP1, madde A için WMA'daki kayıt girişi<p>30 EA için kalite madde örneklemesi işi</p><p>30 EA için kalite emri 1</p></li><li>30 EA, LP2, madde A için WMA'daki kayıt girişi<p>30 EA (yerine koyma) için satınalma siparişi işi</p></li><li>30 EA, LP3, madde A için WMA'daki kayıt girişi<p>30 EA (yerine koyma) için satınalma siparişi işi</p></li><li>30 EA, LP4, madde A için WMA'daki kayıt girişi<p>30 EA için kalite madde örneklemesi işi</p><p>30 EA için kalite emri 1</p></li><li>30 EA, LP5, madde B için WMA'daki kayıt girişi<p>30 EA için kalite madde örneklemesi işi</p><p>30 EA için kalite emri 1</p></li><li>30 EA, LP6, madde B için WMA'daki kayıt girişi<p>30 EA (yerine koyma) için satınalma siparişi işi</p></li><li>30 EA, LP7, madde A için WMA'daki kayıt girişi<p>30 EA (yerine koyma) için satınalma siparişi işi</p></li></ol> |
| Yükle | Yüzde = 10 | Evet _(kilitli/düzenlenemez)_ | <p>Konum: Hayır</p><p>Plaka: Hayır</p> | No | Geçerli değil | <p>**Sipariş satırı miktarı: 100 EA**</p><p>**Hiçbir yük oluşturulmadı. Sipariş kapsamı uygulandı.**</p><ol><li>50 EA, LP1 için WMA'daki kayıt girişi<p>5 EA için kalite madde örneklemesi işi</p><p>5 EA için kalite emri 1</p><p>45 EA (yerine koyma) için satınalma siparişi işi</p></li><li>50 EA, LP2 için WMA'daki kayıt girişi<p>5 EA için kalite madde örneklemesi işi</p><p>5 EA için kalite emri 1</p><p>45 EA (yerine koyma) için satınalma siparişi işi</p></li></ol> |

Bir çalışan önceki tabloda gösterilen kalite emirlerinden birini doğrularsa sistem, stoğu kalite kontrol yerleşiminden _Kalite emri_ iş emri türü için yerleşim yönergesinde tanımlanan yerleşime taşımak üzere otomatik olarak kalite emri işi oluşturur. Bu amaç için, iade veya depolama yerleşimi gibi herhangi bir konumu, kalite emrinin test sonucuna bağlı olarak ayarlayabilirsiniz. Bu kurulumun bir örneği için bu konunun sonundaki [örnek senaryoya](#example-scenario) bakın.

Stoğun kalite kontrol yerleşiminden taşınmasına ilişkin kalite emri işinin **İş durumu** *Kapalı* veya *Sürüyor* olmadığı sürece önceden doğrulanmış bir kalite emrini yeniden açabilirsiniz.

## <a name="process-insights-when-multiple-quality-associations-coexist"></a>Birden çok kalite ilişkisi birlikte bulunduğunda öngörüleri işleme

Aynı kaynak belge satırına birden fazla kalite ilişkilendirmesi tanımlanabilir ve uygulanabilir ve bu kalite ilişkilendirmelerinin bazıları için **Geçerli ambar türü** alanı _Yalnızca ambar işlemleri için kalite yönetimi_ olarak, bazıları için ise _Tümü_ olarak ayarlanabilir.

Aşağıdaki örnekte **Referans türü** değeri _Satınalma_'dır.

1. İlk kalite ilişkisi aşağıdaki şekilde ayarlanmıştır:

    - **Geçerli ambar türü:** *Yalnızca ambar işlemleri için kalite yönetimi*
    - **Madde kodu:** *A0001*
    - **Hesap kodu:** *Tümü*
    - **Test grubu:** *Kutu*
    - **Madde örnekleme:** *5 adet*

1. İkinci kalite ilişkisi aşağıdaki şekilde ayarlanmıştır:

    - **Geçerli ambar türü:** *Tümü*
    - **Madde kodu:** *Tümü*
    - **Hesap kodu:** *Tümü*
    - **Test grubu:** *Kutu*
    - **Madde örnekleme:** *1 adet*

1. Üçüncü kalite ilişkisi aşağıdaki şekilde ayarlanmıştır:

    - **Geçerli ambar türü:** *Yalnızca ambar işlemleri için kalite yönetimi*
    - **Madde kodu:** *Tümü*
    - **Hesap kodu:** *104*
    - **Test grubu:** *Empedans*
    - **Madde örnekleme:** *Her ikinci plaka* (Bu ayar, alınan ilk, üçüncü, beşinci vb. plakaların kalite emri oluşturacağı anlamına gelir.)

1. Dördüncü kalite ilişkisi aşağıdaki şekilde ayarlanmıştır:

    - **Geçerli ambar türü:** *Tümü*
    - **Madde kodu:** *Tümü*
    - **Hesap kodu:** *Tümü*
    - **Test grubu:** *Empedans*
    - **Madde örnekleme:** *5 adet*

1. Beşinci kalite ilişkisi aşağıdaki şekilde ayarlanmıştır:

    - **Geçerli ambar türü:** *Tümü*
    - **Madde kodu:** *Tümü*
    - **Hesap kodu:** *Tümü*
    - **Test grubu:** *Koni*
    - **Madde örnekleme:** *%10*

Satıcı 104 için A0001 maddesinden 10 adetlik miktar için bir satınalma siparişi oluşturulur. Daha sonra, miktarı 10 olan bir satınalma siparişi satırı WMA kullanılarak bir plakaya alındı olarak kaydedilir. Sonuç aşağıdaki gibidir:

- *Kutu* test grubu için ilk kalite ilişkisinden bir kalite emri vardır. Miktar 5'dir. İlk kalite ilişkisinin ölçütleri, *Kutu* test grubuna göre daha özel olduğundan, ikinci kalite ilişkisinden herhangi bir kalite emri yoktur.
- *Empedans* test grubu için üçüncü kalite ilişkisinden bir kalite emri vardır. Miktar 10'dir. İlk kalite ilişkisinin ölçütleri, *Empedans* test grubuna göre daha özel olduğundan, dördüncü kalite ilişkisinden herhangi bir kalite emri yoktur.
- *Koni* test grubu için beşinci kalite ilişkisinden bir kalite emri vardır. Miktar 1'dir.

Üç kalite ilişkisinin her biri için tek bir kalite emri oluşturmayla bağlantılı olarak, kalite maddesi örnekleme işi de oluşturulur. Kaydedilen miktar yalnızca 10'dur. Ancak, madde örnekleme kurulumu nedeniyle, *Yalnızca ambar işlemleri için kalite yönetimi* geçerli ambar türü için oluşturulan kalite emri miktarlarının toplamı 16'dır ve bu miktar fiziksel olarak kaydedilen 10 miktarını aşar. Bu nedenle, kalite kontrol konumuna taşınmak etmek üzere yalnızca 10 fiziksel olarak kullanılabilen miktar olduğundan tam kalite emri miktarları (16) için iş oluşturulmayacaktır. Kalite maddesi örnekleme işi oluşturmak için kullanılan öncelik, kalite emri oluşturma sırasını izler:

- **İlk kalite emri (miktar = 5):** Kalite maddesi örnekleme işi 5 adet için oluşturulur. Daha sonra kalite maddesi örnekleme işi oluşturulması için 5 (10 – 5) adet kalır.
- **İkinci kalite emri (miktar = 10):** Kalite maddesi örnekleme işi 5 adet için oluşturulur. Daha sonra kalite maddesi örnekleme işi oluşturulması için 0 (sıfır) adet kalır.
- **Üçünü kalite emri (miktar = 1):** Kalite maddesi örnekleme işi oluşturulmaz.

Kalite emirleri oluşturma sürecinin bir parçası olarak, 10 miktarlık stok durdurma işlemi oluşturulur. Bu stok durdurmaya her üç kalite emriyle ilgili olarak başvuruda bulunulur. Kalite emri miktarlarının toplamı 16'dır.

Kalite emirleri doğrulandığında, sistem doğrulanan her kalite emri için kalite emri işi oluşturmaya çalışır. Kalite emri miktarlarının toplamı, gerçekten durdurulan ve iş oluşturma için kullanılabilir olan miktarı aştığından, burada gösterildiği gibi tam kalite emri miktarları için kalite emri işi oluşturulamaz. (Bu örnek, önceki örneğin devamıdır.)

1. **Oluşturulan ikinci kalite emrini doğrulayın (miktar = 10). 4 miktarı için kalite emri işi oluşturulur.**

    Kalite emri işinin oluşturulması stok durdurma miktarındaki bir değişiklikle tetiklenir. Kalite emri miktarlarının toplamı 16 olduğundan, 10 miktarının doğrulanması kalan kalite emri miktarının 6'ya eşit olarak doğrulanmasına neden olur. Stok durdurma miktarı 10'dan 6'ya düşürülür. Azaltılan miktar olan 4, kalite emri işi oluşturma için tahsis edilir.

2. **Oluşturulan birinci kalite emrini doğrulayın (miktar = 5). 5 miktarı için kalite emri işi oluşturulur.**

    Kalite emri işinin oluşturulması stok durdurma miktarındaki bir değişiklikle tetiklenir. Kalite emri miktarlarının toplamı 6 olduğundan, 5 miktarının doğrulanması kalan kalite emri miktarının 1'e eşit olarak doğrulanmasına neden olur. Stok durdurma miktarı 6'dan 1'e düşürülür. Azaltılan miktar olan 5, kalite emri işi oluşturma için tahsis edilir.

3. **Oluşturulan üçüncü kalite emrini doğrulayın (miktar = 1). 1 miktarı için kalite emri işi oluşturulur.**

    Kalite emri işinin oluşturulması stok durdurma miktarındaki bir değişiklikle tetiklenir. Kalite emri miktarlarının toplamı 1 olduğundan, 1 miktarının doğrulanması kalan kalite emri miktarının 0'a (sıfır) eşit olarak doğrulanmasına neden olur. Stok durdurma kaldırılır (yani stok durdurma miktarı 1'den 0'a düşürülür). Azaltılan miktar olan 1, kalite emri işi oluşturma için tahsis edilir.

> [!NOTE]
> Kalite emri işinin oluşturulması, bir veya daha fazla kalite emrine karşı referans gösterilen stok durdurma miktarına bağlıdır. Kalite emri miktarlarının toplamı referansta bulunulan stok durdurma miktarını aşarsa, kalite emirlerinin doğrulandığı sipariş kalite emri işi oluşturma işlemini belirler.

## <a name="canceling-quality-item-sampling-work"></a>Kalite maddesi örneklemesi işini iptal etme

Kalite maddesi örnekleme için oluşturulan işi iptal edebilirsiniz. Bu iş iptal edildiğinde ne olacağını denetlemek için aşağıdaki adımları izleyin.

1. **Ambar yönetimi \> Kurulum \> Ambar yönetim parametreleri**'ne gidin.
1. **Genel** sekmesinde, **İş** hızlı sekmesinde, **İşi iptal ederken girişin kaydını kaldır** seçeneğini aşağıdaki değerlerden birine ayarlayın:

    - **Evet** – Kalite maddesi örnekleme işi iptal edildiğinde, ilişkili kalite emri silinir ve stok kaydı kaldırılır.
    - **Hayır** – Kalite maddesi örnekleme işi iptal edildiğinde, ilişkili kalite emri silinmez ve stok kaydı kaldırılmaz.

## <a name="cross-docking"></a>Çapraz sevk

Madde örnekleme işi oluşturan bir kalite ilişkisi kurulumunuz olabilir. Ancak, kalite maddesi örnekleme işi oluşturan kalite ilişkisiyle paralel olarak çapraz sevk mevcut olduğunda, yalnızca çapraz sevki karşılamak için yeterli miktar varsa, yalnızca madde örnekleme işi oluşturulur. **Ambar işlemleri için kalite emrini etkinleştir** seçeneği teslim alan ambar için _Evet_ olarak ayarlanmış ve **Geçerli ambar türü** alanı _Yalnızca ambar işlemleri için kalite yönetimi_ olarak ayarlanmışsa, kalite maddesi örnekleme işinin oluşturulması çapraz sevk işinin oluşturulmasına göre önceliğe sahiptir. Miktar çapraz sevk gereksinimini aşarsa, sistem yine yalnızca madde örnekleme işi oluşturur.

## <a name="destructive-testing"></a>Bozucu test

Bozucu test gerçekleştiren bir test grubu tanımlayabilirsiniz. Bozucu test durumunda, test sonucu ne olursa olsun test edilen madde miktarı testin bir parçası olarak yok edilir. _Ambar işlemleri için Kalite Yönetimi_ özelliğinin bozucu testi destekleme şekli, özellik açık olmadığında kalite yönetiminin destekleme şekline benzer. Kalite emrinin doğrulanabilbilmesi için, kalite kontrolcünün imha edilen miktar için çekme yerleşimini belirtmesi gerekir. Eylem bölmesinde **Stok \> Malzeme çekme**'yi seçerek malzeme çekmeyi kalite emri sayfasından kaydedebilirsiniz. Kalite emri miktarı için çekmenin kaydedilmesi tamamlandıktan sonra, doğrulama işlemi tamamlanabilir.

## <a name="example-scenario"></a>Örnek senaryo

### <a name="prepare-the-scenario"></a>Senaryoyu hazırlama

Bu senaryo aracılığıyla çalışabilmek için, sisteminizi aşağıdaki şekilde hazırlamanız gerekir:

- Demo verisinin sistemde yüklü olduğundan emin olun ve **USMF** tüzel kişiliğini seçin.
- [Özellik yönetiminde](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) _Ambar işlemleri için kalite yönetimi_ özelliğini açın.
- Aşağıdaki adımları izleyerek _Ambar işlemleri için kalite yönetimi_ özelliğini kullanmak üzere Ambar 51'i yapılandırın:

    1. **Ambar yönetimi \> Kurulum \> Ambar  \> Ambarlar**'a gidin.
    1. Ambar 51'ü seçin.
    1. **Ambar** hızlı sekmesinde **Ambar işlemleri için kalite emrini etkinleştir** seçeneğini *Evet* olarak ayarlayın.

### <a name="quality-in-setup--move-to-the-quality-control-location"></a>Kalite giriş kurulumu - Kalite kontrol yerleşimine taşı

Şimdi, sisteminizin ambar 51 için _Ambar işlemleri için Kalite Yönetimi_ özelliğini desteklemesine olanak tanıyacak temel kurulumu ayarlamanız gerekir. (Demo verileri, *QMS* adlı bir kalite yönetimi yerleşimini tanımlar. Bu senaryoda bu konuma birkaç kez başvurulur.) Bu bölümün alt bölümünde anlatıldığı gibi aşağıdaki öğeleri hazırlayın:

- İş sınıfı
- İş şablonu
- Konum yönergesi
- Madde örnekleme
- Kalite ilişkisi
- Mobil cihaz menü öğeleri

#### <a name="work-class-for-quality-in"></a>Kalite girişi için iş sınıfı

1. **Ambar yönetimi \> Kurulum \> İş \> İş sınıfları** seçeneğine gidin.
1. Bir iş sınıfı oluşturun ve aşağıdaki değerleri ayarlayın:

    - **İş sınıfı kodu:** _QualityIn_
    - **Açıklama:** _Kalite maddesi örnekleme_
    - **İş emri türü:** _Kalite maddesi örnekleme_

#### <a name="work-template"></a>İş şablonu

1. **Ambar yönetimi \> Kurulum \> İş \> İş şablonları**'na gidin.
1. **İş emri türü** alanını _Kalite maddesi örnekleme_ olarak ayarlayın.
1. Bir iş şablonu oluşturun ve aşağıdaki değerleri ayarlayın:

    - **İş şablonu:** _51 Kalite_
    - **İş şablonu açıklaması:** _51 Kalite_

1. İş şablonuna bir satır ekleyin ve aşağıdaki değerleri ayarlayın:

    - **İş türü:** _Çekme_
    - **İş sınıfı kodu:** _QualityIn_

1. İş şablonuna ikinci bir satır ekleyin ve aşağıdaki değerleri ayarlayın:

    - **İş türü:** _Yerine koyma_
    - **İş sınıfı kodu:** _QualityIn_

#### <a name="location-directive"></a>Konum yönergesi

1. **Ambar Yönetimi \> Kurulum \> Konum yönergeleri** seçeneğine gidin.
1. **İş emri türü** alanını _Kalite maddesi örnekleme_ olarak ayarlayın.
1. Konum yönergesi oluşturun ve aşağıdaki değerleri ayarlayın:

    - **Ad:** _51 kalite_
    - **İş türü:** _Yerine koyma_
    - **Tesis:** 5
    - **Ambar:** _51_

1. Konum yönergesi için bir satır ekleyin ve aşağıdaki değerleri ayarlayın:

    - **Başlangıç miktarı:** _1_
    - **Son miktar:** _1000000_

1. Konum yönergesi eylemi oluşturun ve aşağıdaki değeri ayarlayın:

    - **Ad:** _Kalite_

1. Yeni konum yönergesi eylemi için **Sorguyu düzenle**'yi seçin ve aşağıdaki değerlere sahip bir **Aralık** kaydı belirtin:

    - **Tablo:** *Yerleşimler*
    - **Alan:** _Yerleşim profili kodu_
    - **Ölçüt:** *QMS*

1. Sorguyu kaydetmek için **Tamam**'ı seçin ve yeni konum yönergesini kaydedin.

Ardından, ambar 51 için varolan satınalma siparişi konum yönergelerinin sırasını değiştirmeniz gerekir. Demo verileri, **İş emri türü** değeri _Satınalma_ olan iki konum yönergesi içerir: biri _51 QMS_ olarak ve diğeri _51 PO Direct_ olarak adlandırılmıştır. *Ambar işlemleri için kalite yönetimi* özelliğinin ambar 51'e uygulanmasını sağlamak için _51 QMS_ yerleşim yönergesinin uygulanmadığından emin olmanız gerekir. Ancak, bu konum yönergesini silmek yerine (ileride kullanmak isteyebileceğiniz için), yalnızca sırayı değiştirebilirsiniz.

1. **Ambar Yönetimi \> Kurulum \> Konum yönergeleri** seçeneğine gidin.
1. **İş emri türü** alanını _Satınalma siparişi_ olarak ayarlayın.
1. Sıra listesinde, _51 PO Direct_ konum yönergesi için sıra numarası 5'i seçin.
1. Seçili sırayı, 4. sıra numarasına taşıyın.
1. _51 QMS_ konum yönergesi sıra numarasının şimdi en az 5 olduğunu doğrulayın.

#### <a name="item-sampling"></a>Madde örnekleme

_Ambar işlemleri için kalite yönetimi_ özelliği bazı yeni madde örnekleme yetenekleri ekler. **Örnekleme kapsamı** değeri artık _Sipariş_, _Sevkiyat_ veya _Yük_olabilir ve **Örnekleme miktarı** değeri artık _Tam plaka_ olabilir.

1. **Stok yönetimi \> Kurulum \> Kalite kontrol \> Madde örnekleme**'ye gidin.
1. Bir madde örnekleme kaydı oluşturun ve aşağıdaki değerleri ayarlayın:

    - **Madde örnekleme:**_3'üncü LP_
    - **Açıklama:** _Her üçüncü plaka_
    - **Örnekleme Kapsamı:** _Sipariş_

1. **Örnekleme miktarı** hızlı sekmesinde **Miktar belirtimi** alanını _Tam plaka_ olarak ayarlayın.
1. **İşlem** hızlı sekmesinde, **n'inci plaka başına** alanını _3_ olarak ayarlayın.
1. **Depolama boyutu başına** bölümünde **Ambar** ve **Stok durumu**'nu etkinleştirin.

#### <a name="quality-associations"></a>Kalite ilişkileri

Yeni madde örneklemesini kullanacak kalite ilişkisi oluşturun.

1. **Stok yönetimi \> Kurulum \> Kalite kontrol \> Kalite ilişkileri**'ne gidin.
1. Bir kalite ilişkisi kaydı oluşturun ve aşağıdaki değerleri ayarlayın:

    - **Referans türü:** _Satınalma_
    - **Madde kodu:** _Tablo_
    - **Madde:** _M9201_
    - **Tesis:** _5_

1. **İşlem** hızlı sekmesinde, **Olay türü** alanını *Kayıt* olarak ayarlayın.
1. **Koşullar** hızlı sekmesinde, **Geçerli ambar türü** alanını *Yalnızca ambar işlemleri için kalite yönetimi* olarak ayarlayın.
1. **Kalite emri işlemi** hızlı sekmesinde, **Kalite işleme ilkesi** alanını _Kalite emri oluştur_ olarak ayarlayın.
1. **Belirtimler** hızlı sekmesinde **Test Grubu** alanını sağ tıklatın ve sonra **Test grupları** sayfasını açmak için **Ayrıntıları görüntüle**'yi seçin.
1. **Test grupları** sayfasında, üst kılavuzun **Genel bakış** sekmesinde bir test grubu oluşturun ve aşağıdaki değerleri ayarlayın:

    - **Test Grubu:** _QMS_
    - **Açıklama:** _QMS testi_
    - **Kabul edilebilir miktar:** _100_
    - **Madde Örnekleme:** _3'üncü LP_ (Seçin)

1. Alt kılavuzun **Genel bakış** sekmesinde bir test için bir kayıt ekleyin ve aşağıdaki değerleri ayarlayın:

    - **Sıra:** *1*
    - **Test:** *Kasa ölçme*

1. Alt kılavuzun **Test** sekmesinde, aşağıdaki değerleri ayarlayın:

    - **Test değişkenleri:** *Başarılı/Başarısız*
    - **Varsayılan sonuç:** *Başarılı*

1. Yeni test grubunu kaydedin ve **Test grupları** sayfasını kapatın.
1. **Kalite ilişkileri** sayfasında tekrar **Test grubu** alanında **QMS**'yi seçin.
1. Kaydı kaydedin.

#### <a name="mobile-device-menu-items-for-quality-in"></a>Kalite girişi için mobil cihaz menüsü öğeleri

Malları kalite kontrol yerleşimine taşımak üzere kurulum işlemini tamamlamak için, mobil cihaz menü öğesinden kalite maddesi örnekleme işinin kullanılabilir olmasını sağlamalısınız.

1. **Ambar yönetimi \> Kurulum \> Mobil cihaz \> Mobil cihaz menüsü öğeleri**'ne gidin.
1. **Satınalma Yerine koyma** mobil cihaz menü öğesini seçin.
1. **İş sınıfları** hızlı sekmesinde, *QualityIn* iş sınıfı kimliğini ekleyin.

#### <a name="summary-your-setup-to-move-goods-to-quality-control"></a>Özet: Malları kalite kontrole taşımak için yaptığınız ayarlar

Şimdi, bir kalite emri oluşturulmasını tetiklemek üzere *Ambar işlemleri için kalite yönetimi* özelliğini kullanan bir kalite ilişkisi tanımladınız. Ambar 51 için iş ve konum verilerini, madde M9201 için satınalma kaydı yapıldığında belirli bir işin oluşturulmasını sağlamak üzere ayarladınız. Bu kurulum, kayıtlı her üçüncü plakanın kalite yerleşimine (_QMS_) taşınmasını ve plaka miktarı için bir kalite emrinin oluşturulmasını sağlar. Bunun dışındaki herşey, kalite kontrol yerleşimi yerine yerine koyma işlemi için taşınacaktır.

### <a name="process-quality-management-work"></a>Kalite yönetimi işini işleme

1. **Tedarik ve kaynak atama \> Satınalma siparişleri \> Tüm satınalma siparişleri**'ne gidin.
1. Satınalma siparişi oluşturun ve aşağıdaki değerleri ayarlayın:

    - **Satıcı hesabı belirtin:** *104*
    - **Ambar:** *51*

1. Satınalma siparişi satırı ekleyin ve aşağıdaki değerleri ayarlayın:

    - **Madde:** *M9201*
    - **Miktar:** *20*
    - **Ölçü Birimi:** *ea*
    - **Ambar:** *51*

1. Daha sonra kullanabilmek için satınalma siparişi numarasını not edin.
1. WMA çalıştıran bir mobil cihaza veya emülatöre gidin ve kullanıcı kimliği olarak *51* ve parola olarak *1* kullanarak ambar 51'de oturum açın.
1. **Gelen \> Satınalma Teslim alma**'ya gidin ve aşağıdaki değerleri girin:

    - **PONum:** Yeni oluşturduğunuz satınalma siparişi numarasını girin
    - **Miktar:** *5*
    - **Birim:** *ea*

1. Satıra göre teslim almaya devam edin; bir kerede *5 ea*, satır tamamen teslim alınana kadar. (Toplam dört plaka oluşturulur.)
1. WMA oturumunu kapatın.
1. Web istemcisine geri dönün, **Tedarik ve kaynak atama \> Satınalma siparişleri \> Tüm satınalma siparişleri**'ne gidin.
1. Satınalma siparişinizi bulun ve açın.
1. **Satınalma siparişi satırları** bölümünde, *M9201* madde numarasıyla ilgili satırı seçin ve **Satınalma siparişi satırları \> İş ayrıntıları**'nı seçin.
1. Oluşturulan ikinci ve üçüncü iş başlıklarının olağan yerine koyma işi olduğuna, birinci ve dördüncü çalışma başlıklarının ise kalite madde örnekleme işi olduğuna dikkat edin. Bu sonuç, her üçüncü plakanın örneği oluşturulacak şekilde yapılandırılan madde örnekleme kurulumu ile tutarlıdır.

#### <a name="move-to-the-quality-control-location"></a>Kalite kontrol konumuna taşıma

Şimdi plakaları belirlenen konumlara taşıyacaksınız. Birinci ve dördüncü plakalar kalite kontrol konumuna gider, buna karşılık ikinci ve üçüncü plakalar doğrudan depolama alanına gider.

1. WMA çalıştıran bir mobil cihaza veya emülatöre gidin ve kullanıcı kimliği olarak *51* ve parola olarak *1* kullanarak ambar 51'de oturum açın.
1. **Gelen \> Satınalma yerine koyma**'ya gidin ve tüm işinizi kapatıncaya kadar önceki yordamdaki her plakayı yerine koyun.

#### <a name="summary-process-quality-management-work"></a>Özet: Kalite yönetimi işini işleme

Şimdi, birinci ve dördüncü plaka için kalite maddesi örnekleme işini plakaları kalite kontrol konumuna taşıyarak çalıştırırsınız. Ayrıca, ikinci ve üçüncü plakaları da yerine koydunuz. Sonraki adım, kalite emri testi ve kontrolü yapmaktır.

### <a name="quality-out-setup-move-from-the-quality-control-location-to-storage-or-return"></a>Kalite çıkış kurulumu: Kalite kontrol konumundan depolama veya iadeye taşıma

Çalışanlar kalite emri sonuçlarını rapor ettiğinde, sistem otomatik olarak iş oluşturur.

Şimdi, ambar işlemleri için kalite yönetimini etkinleştirmek üzere iş sınıfı, iş şablonu ve konum yönergesinin gerekli temel kurulumuna devam edin; böylece kalite emri miktarını kalite kontrol yerleşiminden belirlenen ambar yerleşimine taşımak için gereken iş oluşturulabilir.

#### <a name="work-class-for-quality-out"></a>Kalite çıkışı için iş sınıfı

1. **Ambar yönetimi \> Kurulum \> İş \> İş sınıfları** seçeneğine gidin.
1. Bir iş sınıfı oluşturun ve aşağıdaki değerleri ayarlayın:

    - **İş sınıfı kodu:** *QualityOut*
    - **Açıklama:** *Kalite Çıkış*
    - **İş emri türü:** *Kalite Emri*

#### <a name="work-templates"></a>İş şablonları

1. **Ambar yönetimi \> Kurulum \> İş \> İş şablonları**'na gidin.
1. **İş emri türü** değerini *Kalite emri* olarak değiştirin.
1. Bir iş şablonu oluşturun ve aşağıdaki değerleri ayarlayın:

    - **İş şablonu:** *51 kalite çıkış*
    - **İş şablonu açıklaması:** *51 kalite çıkış*

1. Satır ekleyin ve aşağıdaki değerleri ayarlayın:

    - **İş türü:** *Çekme*
    - **İş sınıfı kodu:** **QualityOut**

1. İkinci bir satır ekleyin ve aşağıdaki değerleri ayarlayın:

    - **İş türü:** *Yerine koyma*
    - **İş sınıfı kodu:** *QualityOut*

#### <a name="location-directives"></a>Konum yönergeleri

1. **Ambar Yönetimi \> Kurulum \> Konum yönergeleri** seçeneğine gidin.
1. **İş emri türü** değerini *Kalite emri* olarak değiştirin.
1. Konum yönergesi oluşturun ve aşağıdaki değerleri ayarlayın:

    - **Ad:** *51 Başarılı*
    - **İş türü:** *Yerine koyma*
    - **Tesis:** *5*
    - **Ambar:** *51*

1. Eylem Bölmesinde, Sorgu düzenleyici iletişim kutusunu açmak için **Sorguyu düzenle**'yi seçin.
1. **Aralık** sekmesinde, aşağıdaki değerleri ayarlayın:

    - **Tablo:** *Kalite emirleri*
    - **Alan:** *Durum*
    - **Ölçüt:** *Başarılı*

1. Sorguyu kaydetmek için **Tamam**'ı seçin ve iletişim kutusunu kapatın.
1. **Satırlar** hızlı sekmesinde bir satır ekleyin ve aşağıdaki değerleri ayarlayın:

    - **Başlangıç miktarı:** *1*
    - **Son miktar:** *1000000*

1. **Konum yönergesi eylemleri** hızlı sekmesinde bir satır ekleyin ve aşağıdaki değeri ayarlayın:

    - **Ad:** *Başarılı*

1. **Yerleşim yönergesi eylemleri** hızlı sekmesinde sorgu düzenleyici iletişim kutusunu açmak için **Sorguyu düzenle**'yi seçin.
1. **Aralık** sekmesinde, aşağıdaki değerleri ayarlayın:

    - **Tablo:** *Yerleşimler*
    - **Alan:** *Bölge Kodu*
    - **Ölçüt:** *Toplu*

1. Sorguyu kaydetmek için **Tamam**'ı seçin ve iletişim kutusunu kapatın.
1. Eylem Bölmesinde, yeni yerleşim yönergesini kaydetmek için **Kaydet**'i seçin.
1. İkinci bir konum yönergesi oluşturun ve aşağıdaki değerleri ayarlayın:

    - **Ad:** *51 Başarısız*
    - **İş türü:** *Yerine koyma*
    - **Tesis:** *5*
    - **Ambar:** *51*

1. Eylem Bölmesinde, Sorgu düzenleyici iletişim kutusunu açmak için **Sorguyu düzenle**'yi seçin.
1. **Aralık** sekmesinde, aşağıdaki değerleri ayarlayın:

    - **Tablo:** *Kalite emirleri*
    - **Alan:** *Durum*
    - **Ölçüt:** *Başarısız*

1. Sorguyu kaydetmek için **Tamam**'ı seçin ve iletişim kutusunu kapatın.
1. **Satırlar** hızlı sekmesinde bir satır ekleyin ve aşağıdaki değerleri ayarlayın:

    - **Başlangıç miktarı:** *1*
    - **Son miktar:** *1000000*

1. **Konum yönergesi eylemleri** hızlı sekmesinde bir satır ekleyin ve aşağıdaki değeri ayarlayın:

    - **Ad:** *Başarısız*

1. **Yerleşim yönergesi eylemleri** hızlı sekmesinde sorgu düzenleyici iletişim kutusunu açmak için **Sorguyu düzenle**'yi seçin.
1. **Aralık** sekmesinde, aşağıdaki değerleri ayarlayın:

    - **Tablo:** *Yerleşimler*
    - **Alan:** *Bölge Kodu*
    - **Ölçüt:** *İade*

1. Sorguyu kaydetmek için **Tamam**'ı seçin ve iletişim kutusunu kapatın.
1. Eylem Bölmesinde, yeni yerleşim yönergesini kaydetmek için **Kaydet**'i seçin.

#### <a name="mobile-device-menu-items-for-quality-out"></a>Kalite çıkışı için mobil cihaz menüsü öğeleri

1. **Ambar yönetimi \> Kurulum \> Mobil cihaz \> Mobil cihaz menüsü öğeleri**'ne gidin.
1. **QMS yerine koyma** mobil cihaz menü öğesini seçin.
1. **İş sınıfları** hızlı sekmesinde, *QualityPut* iş sınıfı kimliğini ekleyin.

Ambar çalışanları şimdi, **QMS yerine koyma** menü öğesini kullanarak kalite emri işini çekebilir. Kalite kontrolden geçemeyen mallar bir iade konumuna konulabilir ve kontrolü geçen mallar toplu-001 konumuna konulabilir.

#### <a name="summary-your-setup-to-move-goods-from-quality-control"></a>Özet: Malları kalite kontrolden taşımak için yaptığınız ayarlar

Ambar 51 için iş ve konum verilerini, kalite emirleri tamamlandığında işin otomatik olarak oluşturulmasını sağlamak üzere ayarladınız. Bu kurulum, her kalite denetimli plakanın bir toplu yerleşime veya iade yerleşimine taşınmasını sağlar.

### <a name="process-quality-management-work"></a>Kalite yönetimi işini işleme

1. **Stok yönetimi \> Periyodik görevler \> Kalite yönetimi \> Kalite emirleri**'ne gidin.
1. Kaydedilen miktarlar için birinci kalite emrini seçin.
1. **Doğrula**'yı seçin. Testin durumu *Başarısız* olarak güncelleştirilir.
1. **Ambar yönetimi \> Tüm işler**'e gidin.
1. Yeni oluşturduğunuz işi açın ve **İş emri türü** değerinin *Kalite emri* olduğuna dikkat edin. İş, yerine koyma konumunun *İade* olduğu ve durumun *Başarısız* olduğu bir satır içerir. (Kalite emrinin durumu *Başarılı* olduysa, yerine koyma yerleşimi bunun yerine *Toplu* olur.)
1. **Stok yönetimi \> Periyodik görevler \> Kalite yönetimi \> Kalite emirleri**'ne geri dönün.
1. Kaydedilen maddeler için ikinci kalite emrini seçin.
1. Alt kılavuzun üstündeki **Sonuçlar**'ı seçin. **Sonuç miktarı** değerini *5* olarak güncelleştirin ve **Test sonucu** değerinin onay işareti olarak değiştiğini doğrulayın.
1. **Doğrula**'yı seçip sayfayı kapatın.
1. **Kalite emirleri** sayfasına dönün, **Doğrula**'yı seçin ve doğrulama işlemi yapın. Durum *Başarılı* olarak güncelleştirilir.

    > [!NOTE]
    > Doğrulama olayı, miktarın kalite kontrol konumundanyeni bir yerleşime taşınmasını sağlamak üzere kalite emri işi oluşturulmasını tetikler.

1. **Ambar yönetimi \> Tüm işler**'e gidin.
1. Yeni oluşturulan işi seçin ve ikinci bir kalite emri işi başlığı oluşturulduğuna ve yerine koyma konumunun *TOPLU-001* olduğuna dikkat edin.
1. WMA çalıştıran bir mobil cihaza veya emülatöre gidin ve kullanıcı kimliği olarak *51* ve parola olarak *1* kullanarak ambar 51'de oturum açın.
1. **Kalite \>QMS'den Yerine Koyma**'ya gidin ve tüm işin kapatılması için her iki iş parçasının ilişkili olduğu iki plakanın her birini işleyin.

> [!NOTE]
> Etkinlik kodunun *Açık iş listesini görüntüle* olduğu bir mobil cihaz menü öğesine bir kalite çıkış girişi eklemeyi düşünün. Örnek olarak, demo verilerdeki **İş listesi** adlı mobil cihaz menü öğesine bakın. Öncelikle *Kalite emri* iş sınıfını kullanıcı tarafından yönlendirilen bir menü öğesine ekleyin; çünkü işin iş listesinde görünmesi için bu iş sınıfı gereklidir. Sonra *Kalite emri* iş sınıfını **İş listesi** menü öğesine ekleyin. Bu durumda, iş listesine erişimi olan kullanıcılar otomatik olarak kalite emri doğrulaması tarafından oluşturulan işi çekebilir ve işleyebilir.
