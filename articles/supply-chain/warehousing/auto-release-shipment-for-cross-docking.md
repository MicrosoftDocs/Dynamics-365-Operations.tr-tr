---
title: çapraz sevk için sevkiyatı otomatik serbest bırakma
description: Bu konuda, talep miktarını sağlayan üretim emri tamamlandı olarak bildirildiğinde ambara otomatik olarak bir talep emri serbest bırakmanızı sağlayan çapraz sevk stratejisi açıklanır. Bu durumda, miktar doğrudan üretim çıkış konumundan giden konumuna taşınır.
author: omulvad
ms.date: 10/15/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSCrossDockingTemplate
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2019-10-1
ms.dyn365.ops.version: 10.0.6
ms.openlocfilehash: 1c831030659b38b52932e504f744d24d999958a5
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/01/2021
ms.locfileid: "5831446"
---
# <a name="auto-release-shipment-for-cross-docking"></a>çapraz sevk için sevkiyatı otomatik serbest bırakma

[!include [banner](../includes/banner.md)]

Bu konuda, talep miktarını sağlayan üretim emri tamamlandı olarak bildirildiğinde ambara otomatik olarak bir talep emri serbest bırakmanızı sağlayan çapraz sevk stratejisi açıklanır. Bu şekilde, talep emrinin karşılanması için gerekli olan miktar doğrudan üretim çıkış konumundan giden yerleşime taşınır.

Çapraz sevk, bir giden siparişi yerine getirmek için gereken miktarın gelen siparişin alındığı yerleşimden siparişin çıkış noktasına veya hazırlanma alanına yönlendirildiği ambar işleme akışıdır. (Gelen sipariş bir satınalma siparişi, transfer emri veya üretim emri olabilir.) Gelişmiş çapraz sevk özelliği tüm tedarik ve talep emirlerini desteklese ve çapraz sevk fırsatı tanımlanmadan önce giden talebin serbest bırakılmasını gerektirse de, Sevkiyatı otomatik serbest bırakma özelliğinin aşağıdaki özelliklere sahiptir:

- Yalnızca üretim emirlerini tedarik olarak ve yalnızca satış siparişlerini ve transfer emirlerini talep olarak destekler.
- Çapraz sevk işlemi, talep emri tedarik girişi kaydedilmeden önce ambarda serbest bırakılmamış olsa da başlatılabilir (yani, üretim tamamlandı olarak bildirilmeden önce).

Bu çapraz sevk işlevinin iki yararı vardır:

- Ambar operasyonları, bu miktarlar yalnızca giden siparişi karşılamak için tekrar çekilecekse, tamamlanmış malların miktarlarını normal ambar depolama alanına yerine koyma adımını atlayabilir. Bunun yerine, miktarlar bir kez, çıkış konumundan bir paketleme/sevkiyat yerleşimine taşınabilir. Bu şekilde, işlev stok işleme için harcanan zamanı en aza indirmeye ve sonuçta ambardaki zaman ve alan tasarruflarını en yüksek düzeye çıkarmaya yardımcı olur.
- İlişkili üretim emri için tamamlanan malların çıkışı tamamlandı olarak bildirilene kadar ambar operasyonları, satış siparişlerinin ve transfer emirlerinin ambara serbest bırakılmasını erteleyebilir. Bu avantaj özellikle, üretim sağlama sürelerinin stoğa göre üretim ortamlarındaki sağlama sürelerinden daha uzun olduğu, siparişe göre üretim ortamlarında ilgili olabilir.

## <a name="prerequisites"></a>Önkoşullar

| Önkoşul | Tanım |
|---|---|
| Öğe | Madde mutlaka ambar yönetimi süreçleri için etkinleştirilmelidir.<p>**Not:** Fiili ağırlığın etkin olduğu maddeler çapraz sevk işlemlerine eklenemez.</p> |
| Ambar | Ambar mutlaka ambar yönetimi süreçleri için etkinleştirilmelidir. |
| Çapraz sevk şablonları | Belirli bir ambar için **Tedarik girişinde** talep serbest bırakma ilkesini kullanan en az bir çapraz sevk şablonunun ayarlanması gerekir. |
| İş sınıfı | **Çapraz sevk** iş emri türü için bir çapraz sevk iş sınıfı kodu oluşturulmalıdır. |
| İş şablonları | **Çapraz sevk** iş emri türünün çalışma şablonları, çapraz sevk çekme ve yerine koyma işi oluşturmak için gereklidir. |
| Konum yönergeleri | Satış siparişi miktarlarının paketlendiği ve sevk edildiği konumlarda yerine koyma işi yönergesi sağlamak için **Çapraz sevk** iş emri türünün yerleşim yönergeleri gereklidir. |
| Talep emri ve üretim emri arasında işaretleme | Ambar sistemi, giden sipariş sevkiyatının otomatik olarak serbest bırakılmasını tetikleyebilir ve yalnızca satış siparişleri ve transfer emirleri bir üretim emrine karşı rezerve edilmiş ve işaretlenmiş olması durumunda tamamlandı olarak bildir eylemindeki çıkış yerleşiminden geçici stoklama oluşturabilir. |

## <a name="example-cross-docking-flow"></a>Örnek çapraz sevk akışı

Tipik bir çapraz sevk akışı aşağıdaki ana adımlardan oluşur.

1. Bir satış siparişi alan kişi siparişe göre üretim ürünü için satış siparişi oluşturur. Normalde, istenen miktar eldeki miktar değildir ve öncelikle üretilmesi gerekir.
2. Satış siparişini alan kişi doğrudan satış siparişi satırından bir üretim emri oluşturur. Bu şekilde, satış siparişini alan kişi satış siparişi miktarını, üretim emri miktarına göre ayırır ve işaretler. 

    Alternatif olarak, bir üretim planlayıcısı, planlı siparişler kesinleştirildiğinde, bu işaretlemenin güncelleştirilmesi gerektiğini belirtir.

3. Üretim emri aşağıdaki adımlardan geçer:

    1. Üretim planlayıcısı, üretim emrini tahmin eder ve serbest bırakır. (Tahmin ham malzeme rezervasyonunu içerir ve serbest bırakma bir ambara serbest bırakmayı içerir.)
    2. Ambar çalışanı, üretim çekme işine uygun şekilde, depolama yerleşiminden üretim giriş yerleşimine ham madde çekme işlemini başlatır ve tamamlar.
    3. Bir atölye operatörü, üretim emrini başlatır.
    4. Son operasyonda, bir makine operatörü üretim emrini tamamlandı olarak bildirmek için mobil cihazı kullanır.

4. Sistem, iki bağlantılı siparişin çapraz sevk olayını tanımlamak için kurulumu kullanır ve sonra bu görevleri tamamlar:

    1. Sevkiyat oluşturmak için ilişkili satış siparişini bir ambara otomatik olarak serbest bırakmak.
    2. Çıkış yerleşiminden bitmiş malları çekme ve bunları satış siparişine atanan çapraz sevk yerleşimi yönergelerinin çıkış yerleşime taşıma yönergelerine sahip çapraz sevk işini otomatik olarak oluşturmak.
    3. Üretim emri tamamlandı olarak bildirildikten hemen sonra çapraz sevk işini tamamlamak için bir makine operatörünü bilgilendirmek.

5. Çapraz sevk işi tamamlandıktan ve miktarlar araç üzerine yüklendikten sonra, bir giden ambar planlayıcısı satış sevk irsaliyesini onaylar.

## <a name="example-scenario"></a>Örnek senaryo

Bu senaryo için, demo verilerinin yüklenmiş olması ve **USMF** demo veri şirketini kullanmanız gerekir.

### <a name="set-up-cross-docking-that-uses-the-auto-release-shipment-feature"></a>Sevkiyatı otomatik serbest bırakma özelliğini kullanan çapraz sevk kurulumu

#### <a name="cross-docking-template"></a>Çapraz sevk şablonu

1. **Ambar yönetimi** \> **Kurulum** \> **İş** \> **Çapraz sevk şablonları**'na gidin.
2. **Yeni**'yi seçin.
3. **Sıra numarası** alanına **1** girin.
4. **Çapraz sevk şablonu kodu** alanına, **XDock\_RAF** gibi bir ad girin.
5. **Talep serbest bırakma ilkesi** alanında, **Tedarik girişinde**'yi seçin.
6. **Ambar** alanına, çapraz sevk işlemini ayarlamak istediğiniz ambarın numarasını girin. Bu örnek için, **51**'i seçin.

    > [!NOTE]
    > Şablon için talep serbest bırakma ilkesi olarak **Tedarik girişinde**'yi seçersiniz, sayfadaki diğer tüm alanlar kullanılamaz duruma gelir. Benzer şekilde, herhangi bir tedarik kaynağı tanımlayamazsınız. Bu davranış, sevkiyatı otomatik serbest bırak özelliğini kullanan çapraz sevk tedarik kaynakları olarak yalnızca üretim emirlerini desteklediğinden ve satış siparişleri ile üretim emirleri arasında bir işaretleme olmasını gerektirdiğinden ortaya çıkar. Talep serbest bırakma ilkesi olarak **Tedarik girişinden önce**'yi seçerseniz, **Planlama** ve **Tedarik kaynakları** sekmelerindeki alanlar kullanılabilir ve düzenlenebilir.

#### <a name="work-classes"></a>İş sınıfları

1. **Ambar Yönetimi** \> **Kurulum** \> **İş** \> **İş sınıfları** seçeneğine gidin.
2. **Yeni**'yi seçin.
3. **İş sınıfı kodu** alanında, **CrossDock** gibi bir ad girin.
4. **İş emri türü** alanında **Çapraz sevk**'i seçin.

Çapraz sevki yapılan mamul malların konabileceği yerleşim türlerini sınırlandırmak için, bir veya daha fazla geçerli yerleşim türü belirtebilirsiniz.

#### <a name="work-templates"></a>İş şablonları

1. **Ambar yönetimi** \> **Kurulum** \> **İş** \> **İş şablonları**'na gidin.
2. **İş emri türü** alanında **Çapraz sevk**'i seçin.
3. **Yeni**'yi seçin.
4. **Sıra numarası** alanına **1** girin.
5. **İş şablonu** alanında, **CrossDock\_51** gibi bir ad girin.
6. **Kaydet**'i seçin.
7. **İş Şablonu Ayrıntıları** bölümünde **Yeni**'yi seçin.
8. Yeni satır için **İş türü** alanında, **Çekme**'yi seçin. **İş sınıfı kodu** alanında **CrossDock**'u seçin.
9. **Yeni**'yi seçin.
10. Yeni satır için **İş türü** alanında, **Koyma**'yı seçin. **İş sınıfı kodu** alanında **CrossDock**'u seçin.

#### <a name="location-directives"></a>Konum yönergeleri

Mamul mallar için standart bir yerine koyma süreci, çekilen üretim miktarlarının taşınmasını normal bir depolama alanına yönlendirecek bir **Koyma** yerleşimi yönergesi gerektirir. Benzer şekilde, işe ilgili satış siparişinin sevkiyatını oluşturan atanmış bir çıkış yerleşimine tamamlanan miktarın yerleştirilmesi işini bildirmek için bir çapraz sevk **Koyma** yerleşimi yönergesi ayarlamanız gerekir.

Çapraz sevk için, biten mallara ilişkin normal yerine koyma işlemi olarak, çıkış yerleşimi verildiğinden çekme işi eylemi için bir yerleşim yönergesi oluşturmanız gerekmez. Ek olarak, bu çıktı konumunun kaynakla ilişkili kayıtlardan birinde varsayılan çıkış konumu olarak (kaynak, kaynak grubu ilişkisi veya kaynak grubu) veya bir ambar için varsayılan üretim mamul mal yerleşimi olarak ayarlanması beklenir.

1. **Ambar Yönetimi** \> **Kurulum** \> **Konum yönergeleri** seçeneğine gidin.
2. **İş emri türü** alanında **Çapraz sevk**'i seçin.
3. **Yeni**'yi seçin.
4. **Sıra numarası** alanına **1** girin.
5. **Ad** alanına, **Baydoor** gibi bir ad girin.
6. **İş türü** alanında, **Yerine koyma**'yı seçin.
7. **Site** alanında, **5**'i seçin.
8. **Ambar** alanında **51**'i seçin.
9. **Satırlar** hızlı sekmesinde **Yeni**'yi seçin.
10. **Son miktar** alanına aralık için maksimum miktarı girin (**1000000** gibi).
11. **Kaydet**'i seçin.
12. **Konum Yönergeleri Eylemleri** hızlı sekmesinde, **Yeni**'yi seçin.
13. **Ad** alanına, **Baydoor** gibi bir ad girin.
14. **Kaydet**'i seçin.
15. Koyma konumlarını bir veya daha fazla belirli konumla sınırlamak için standart sorgu olanağını kullanabilirsiniz. **Sorguyu düzenle**'yi ve **Yerleşimler** tablosundaki **Ambar** alanı için ölçüt olarak **51**' i seçin.

### <a name="cross-dock-finished-goods-to-the-outbound-location"></a>Mamul malları çıkış yerleşimine çapraz sevk etme

Mamul malların miktarını ilişkili satış siparişinin giden yerleşimine çapraz sevk etmek için aşağıdaki adımları izleyin.

1. **Satış ve pazarlama** \> **Satış siparişleri** \> **Tüm satış siparişleri**'ne gidin.
2. **Yeni**'yi seçin.
3. Satış siparişi başlığı için, müşteri hesabı **US-001**'İ ve sevkiyatı otomatik serbest bırakma özelliğini kullanan çapraz sevk için ayarlanmış bir ambar seçin.
4. Mamul ürün için bir satır ekleyin ve miktar olarak **10** girin.
5. **Satış siparişi satırları** bölümünde **Ürün ve tedarik** \> **Üretim emri**'ni seçin.
6. **Üretim emri oluştur** iletişim kutusunda, varsayılan değerleri gözden geçirin ve **Oluştur**'u seçin. Yeni bir üretim emri oluşturulur ve satış siparişine bağlanır (rezerve edilmiş ve işaretlenmiş).
7. İsteğe bağlı: **Miktar** alanının değerini, satış siparişini karşılamak için gereken değerden daha büyük olacak şekilde değiştirin. Üretim miktarı tamamlandı olarak bildirildiğinde, sistem işaretlenen miktar için çapraz sevk işi ve biten malların yerine konmasını işlemine yönelik normal yordama uygun olarak kalan miktar için yerine koyma işi oluşturur.

    Daha önce belirtildiği gibi, satış siparişi ile üretim emri arasında bir işaret olması gerekir. Aksi durumda, çapraz sevk çalışmaz. Bir işaretleme birden çok şekilde oluşturulabilir:

    - Sistem, aşağıdaki durumlarda işaretlemeyi otomatik olarak oluşturabilir:

        - Üretim emri doğrudan satış siparişi satırından el ile oluşturulur (bkz. adım 6).
        - Planlı üretim emirleri kesinleştirilir ve **İşaretlemeyi güncelleştir** alanı **Standart** olarak ayarlanır.

    - Kullanıcı, **İşaretleme** sayfasını talep emri satırından açarak işaretlemeyi el ile oluşturabilir.

    > [!NOTE]
    > Stok modeli olarak standart ve ağırlıklı ortalamayı kullanacak şekilde ayarlanmış maddeler için bir işaret el ile oluşturulamaz.

8. **Üretim emri** sayfasında, Eylem bölmesindeki **Üretim emri** sekmesinde, **İşlem** grubunda **Tahmini**'yi ve ardından **Tamam**'ı seçin. Sipariş tahmini yapılır ve hammadde miktarı üretim için rezerve edilir.
9. Eylem bölmesindeki **Üretim emri** sekmesinde, **İşlem** grubunda **Serbest bırak**'ı ve ardından **Tamam**'ı seçin. Ham madde için ambar çekme işi oluşturulur.
10. İşi açın ve gözden geçirin. Eylem Bölmesinde **Ambar** sekmesindeki **Genel** grubunda **İş ayrıntıları**'nı seçin. İş kodunu not edin.
11. Ambarda 51'de işi çalıştırmak için Ambar Yönetimi mobil uygulamasına oturum açın.
12. **Üretim** \> **Üretim çekme**'ye gidin.
13. Ham maddenin çekilmesini başlatmak ve tamamlamak için iş kodunu girin. 

    İş tamamlandı olarak bildirildikten sonra, hammade miktarı üretim giriş yerleşiminde (USMF demo verilerinde **005**) kullanılabilir ve üretim emrini yürütme işlemi başlayabilir.

14. **Üretim emri** sayfasında, Eylem bölmesindeki **Üretim emri** sekmesinde, **İşlem** grubunda **Başlat**'ı ve ardından **Tamam**'ı seçin.
15. Uygulamada **Üretim** \> **RAF ve yerine koy**'a gidin.
16. **Üretim kodu** alanına üretim emri numarasını ve diğer zorunlu ayrıntıları girin ve **Tamam**'ı seçin.

Aşağıdaki olayların gerçekleştiğine dikkat edin:

- Bağlantılı satış siparişi için ambara serbest bırakma tetiklenir.
- Serbest bırakmaya bağlı olarak, sevkiyat ve çapraz sevk işi oluşturulur. Bu iş, ambar operatörüne satış siparişi satırını karşılamak için gereken miktarları çekmesini ve bunları çapraz sevk yerleşimi yönergesinde belirtilen çıkış yerleşimine koymasını söyler.
- Üretim emri miktarı, satış siparişinin gerektirdiği miktardan büyükse, olağan yerine koyma çalışması oluşturulur. Bu iş ambar operatörüne çapraz sevk sonrasında kalan mamul mal miktarını çekmesini ve bunu yerleşim yönergesine göre normal depolama birimine taşımasını bildirir.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]