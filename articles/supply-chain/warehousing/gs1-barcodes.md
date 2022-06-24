---
title: GS1 barkodları
description: Bu makalede, etiketlerin bir ambarda taranabilmesi için GS1 barkodlarının ve QR kodlarının nasıl ayarlanacağı açıklanmaktadır.
author: Mirzaab
ms.date: 03/21/2022
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2021-08-02
ms.dyn365.ops.version: 10.0.25
ms.openlocfilehash: 67c54f344ff7091f4a25198fdafa745c6c84d5d0
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8907159"
---
# <a name="gs1-bar-codes"></a>GS1 barkodları

[!include [banner](../includes/banner.md)]

Ambar çalışanlarının genellikle bir madde, palet veya konteynerin hareketlerini kaydetmek için mobil cihaz tarayıcısı kullanırken birkaç görevi tamamlaması gerekir. Bu görevler, mobil cihazda barkodları taramayı ve bilgileri el ile girmeyi içerebilir. Barkodlarda, Microsoft Dynamics 365 Supply Chain Management ile tanımlayıp yönettiğiniz şirkete özel bir biçim kullanılır.

Sevkiyat etiketleri için GS1 barkodları, şirketler arasında veri alışverişine yönelik genel bir standart sağlamak üzere geliştirilmiştir. Bunlar hem GS1-128 gibi doğrusal (1D) sembolojilerde (barkod biçimleri) hem de GS1 DataMatrix ve GS1 QR kodları gibi 2D sembolojilerde kullanılabilir. GS1 barkodları yalnızca verileri kodlamaz, aynı zamanda bu verilerin anlamını tanımlamak için önceden tanımlanmış bir *uygulama tanımlayıcıları* listesi kullanmanıza olanak tanır. GS1 standardı, veri biçimini ve kodlamak için kullanılabilecek çeşitli veri türlerini tanımlar. Eski barkod standartlarının aksine GS1 barkodlarında birden fazla veri öğesi bulunabilir. Bu nedenle, tek bir barkod taraması toplu iş ve son kullanma tarihi gibi çeşitli ürün bilgisi türlerini yakalayabilir.

Supply Chain Management'taki GS1 desteği, paletlerin ve konteynerlerin GS1 biçiminde barkodlar kullanılarak etiketlendiği ambarlarda tarama işlemini önemli ölçüde kolaylaştırır. Ambar çalışanları, GS1 barkodunun tek bir taraması üzerinden gerekli tüm bilgileri ayıklayabilir. GS1 barkodları, birden çok tarama yapma ve/veya el ile bilgi girme ihtiyacını ortadan kaldırarak görevlerle ilişkili zamanın azaltılmasına yardımcı olur. Aynı zamanda, doğruluğu artırmaya da yardım eder.

Lojistik yöneticilerinin, gerekli uygulama tanımlayıcıları listesini ayarlaması ve tanımlayıcıların her birini uygun mobil cihaz menü öğeleriyle ilişkilendirmesi gerekir. Ardından uygulama tanımlayıcıları, taşıma ve paketleme amacıyla genel bir ayar olarak ambarlar genelinde kullanılabilir. Böylece tüm gönderim etiketleri, birleşik bir form alır.

Aksi belirtilmedikçe, bu makalede doğrusal (1D) barkodlara ve 2D barkodlara atıfta bulunmak için *barkod* terimi kullanılmaktadır.

## <a name="the-gs1-bar-code-format"></a>GS1 barkod biçimi

GS1 Genel Şartnamesi, GS1 barkodları için hangi sembolojilerin kullanılabileceğini ve barkoddaki verilerin nasıl kodlanacağını belirtir. Bu bölüm makaleye kısa bir giriş yapar. Ayrıntılı bilgi için GS1 tarafından yayımlanan [GS1 Genel Şartnamesi](https://www.gs1.org/docs/barcodes/GS1_General_Specifications.pdf) belgesine bakın. GS1 şartname belgesi düzenli olarak güncelleştirilir ve sağladığı bilgiler GS1 Genel Şartnamesi sürüm 22.0 ile günceldir.

GS1 barkodları şu sembolojileri kullanır:

- **Doğrusal veya 1D barkodlar** – GS1-128 ve GS1 DataBar
- **2D barkodlar** – GS1 DataMatrix, GS1 QR Kodu ve GS1 Dotcode

Normal Code-128 doğrusal barkodu, GS1 DataMatrix ve GS1 QR Kodu'nun özel bir durumu olan GS1-128'de GS1'den özel olarak bahsedilmektedir. GS1 sürümü ile GS1 olmayan sürüm arasındaki fark, barkod verilerinde ilk karakter olarak özel bir karakterin (FNC1) bulunmasıdır. Bir FNC1 karakterinin varlığı, barkoddaki verilerin GS1 şartnamesine göre yorumlanması gerektiğini belirtir.

Barkoddaki veriler, her biri alanın başlangıcında bir uygulama tanımlayıcısıyla tanımlanan birden çok veri öğesinden oluşur. Genellikle veriler, barkod altında kullanıcı tarafından okunabilen bir biçimde ve parantez içinde uygulama tanımlayıcısı gösterilerek sunulur. İşte bir örnek: `(01) 09521101530001 (17) 210119 (10) AB-123`. Bu barkod üç öğe içerir:

- **Uygulama tanımlayıcısı 01** – Maddenin GS1 global ticaret madde numarası (GTIN).
- **Uygulama tanımlayıcısı 17** – Sona erme tarihi.
- **Uygulama tanımlayıcısı 10** – Toplu iş numarası.

Verilerin her öğe için, önceden tanımlanmış bir uzunluğu veya değişken uzunluğu olabilir. Önceden tanımlanmış uzunlukları bulunan bir sabit uygulama tanımlayıcıları listesi vardır. Tüm diğer uygulama tanımlayıcıları, değişken uzunluktadır ve GS1 uygulama tanımlayıcı listesi verilerin maksimum uzunluğunu ve biçimini belirtir. Örneğin, uygulama tanımlayıcısı 01, önceden tanımlanmış 16 karakterlik uzunluğa (uygulama tanımlayıcısının kendisi için iki, GTIN için 14) ve uygulama tanımlayıcısı 17, önceden tanımlanmış sekiz karakterlik uzunluğa (uygulama tanımlayıcısının kendisi için iki ve tarih için altı) sahiptir. Ancak uygulama tanımlayıcısı 10, uygulama tanımlayıcısının kendisi için iki sayıya ve 20 adede kadar alfasayısal karaktere sahiptir.

Öğeler bir araya getirildiğinde bir öğe, değişken uzunluklu bir öğeyi izliyorsa ayırıcı bir karakter kullanılmalıdır. Bu ayırıcı, özel FNC1 karakteri veya grup ayırıcı karakteri (ASCII kodu 29 ve onaltılık kodu 1D olan yazdırılamayan bir karakter) olabilir. Ayırıcı son öğeden sonra kullanılmamalıdır. Ayırıcı, önceden tanımlanmış uzunluğa sahip öğelerden sonra da kullanılmamalıdır ancak varlığı kritik bir hata değildir.

01, 17 ve 10 numaralı uygulama tanımlayıcılar içeren önceki barkod örneğindeki barkod verilerinde, Code-128, QR Kodu veya DataMatrix sembolündeki veriler `<FNC1>`**`01`**`09521101530001`**`17`**`210119`**`10`**`AB-123` olur (uygulama tanımlayıcıları kalın olarak gösterilir). En iyi uygulama olarak, değişken uzunlukta olan herhangi bir öğenin, ek bir grup ayırıcı karakter gereksinimini ortadan kaldırmak için en sona yerleştirilmesi gerekir. Ancak barkod, ayırıcının zorunlu olduğu durumlarda farklı bir öğe sırası da içerebilir. İşte bir örnek: `<FNC1>`**`01`**`09521101530001`**`10`**`AB-123<GS>`**`17`**`210119`.

### <a name="dates-and-decimal-numbers"></a>Tarihler ve ondalık sayılar

Tarihler her zaman *YYAAGG* biçiminde gösterilir; burada yüzyıl GS1 şartnamesine göre belirlenir. Yalnızca 49 yıl öncesi ile 50 yıl sonrası (şu anki yıla göre) arasındaki tarihler gösterilebilir.

Bazı veri öğeleri ondalık sayılar içerir. Örneğin, uygulama tanımlayıcıları 3100, 3101, ... 3105, net ağırlığı kilogram olarak gösterir. Bu uygulama tanımlayıcılarının önceden tanımlanmış 10 karakterlik uzunluğa sahip olması nedeniyle, miktar için altı numara kullanılabilir. Ondalık noktasının konumu, uygulama tanımlayıcısının son numarası ile belirtilir. Bu nedenle, bu uygulama tanımlayıcısı ailesi de *310n* olarak gösterilebilir. GS1 standardı, her zaman ondalık noktasının solunda en az bir sayı olması gerektiğini belirttiğinden, maksimum beş ondalık basamağa izin verilir.

Aşağıda, *123456* sayısının farklı uygulama tanımlayıcıları (kalın olarak gösterilir) tarafından nasıl yorumlanacağı ile ilgili örnekler gösterilmektedir:

- **`3100`**`123456` &rarr; 123456 (tamsayı)
- **`3101`**`123456` &rarr; 12345,6 (bir ondalık basamak)
- **`3102`**`123456` &rarr; 1234,56 (iki ondalık basamak)
- **`3103`**`123456` &rarr; 123,456 (üç ondalık basamak)
- **`3104`**`123456` &rarr; 12,3456 (dört ondalık basamak)
- **`3105`**`123456` &rarr; 1,23456 (beş ondalık basamak)

## <a name="scanning-gs1-bar-codes-in-supply-chain-management"></a>Supply Chain Management'ta GS1 barkodlarının taranması

GS1 barkodların taranması için ambar çalışanları, mobil aygıta yerleşik veya bağlanmış bir tarayıcı kullanır. Tarayıcı daha sonra taranan barkodu Warehouse Management mobil uygulamasına bir dizi klavye olayı olarak iletir. Bu işlem modu, *klavye emülasyonu* veya *emülasyon* olarak da bilinir. Mobil uygulama, alınan metni Supply Chain Management'a olduğu gibi gönderir. Sistem giriş verilerini aldığında önce, verilerin gerçekten bir GS1 barkodu olduğunu belirten yapılandırılmış öneklerden biriyle başlayıp başlamadığını belirler ([Global GS1 seçeneklerini ayarlama](#set-gs1-options) bölümüne bakın). Taranan veriler bu öneklerden biriyle başlamazsa sistem, verileri ayrıştırmak ve bağımsız veri öğelerini kendi uygulama tanımlayıcılarına göre ayıklamak için bir GS1 ayrıştırıcısı kullanır. Veriler ayrıştırıldıktan sonra, geçerli giriş alanı veya birden çok alan taranmış verilerle doldurulacaktır.

### <a name="configuration-of-bar-code-scanner-hardware-and-software"></a>Barkod tarayıcı donanımı ve yazılımı yapılandırması

Supply Chain Management'ın GS1 barkodlarını doğru şekilde tanıması ve bunların kodunu çözmesi amacıyla, donanım tarayıcısı veya destekleyici yazılımlar aşağıdaki eylemleri gerçekleştirecek şekilde yapılandırılmalıdır:

- Sistemin bir GS1 barkodunu tanıyabilmesi için taranan barkodlara önek ekleyin.
- Yazdırılamayan ASCII grup ayırıcı karakterini (ASCII kodu 29 veya onaltılı kodu 1D), tilde (~) gibi yazdırılabilir bir karaktere dönüştürün.

Taranan barkoda herhangi bir önek ekleyebilmenize karşın, bir seçenek de, bir *AIM tanımlayıcısı* olarak da bilinen bir ISO/IEC 15424 semboloji tanımlayıcısı eklemektir. Bu üç karakterlik tanımlayıcı `]` ile başlar, ardından kullanılan sembolojiyi tanımlayan bir karakter ve daha sonra da başka bir değiştirici olarak kullanılan bir sayı içerir. Örneğin AIM tanımlayıcısı `]C1`, Code 128 barkodunu (`C` karakteri nedeniyle) belirtir ve değiştirici `1`, verinin ilk konumunda bir FNC1 karakteri olduğunu belirtir. Diğer taraftan `]C0`, verilerin ilk karakteri olarak diğer herhangi bir karaktere sahip olan Code 128 barkodudur.

Aşağıdaki beş semboloji tanımlayıcısı, uygulama tanımlayıcısı öğelerine sahip GS1 barkodlarına karşılık gelir:

- `]C1` – İlk konumunda FNC1 karakteri olan (`1`) Code 128 (`C`), GS1-128 olarak da bilinir.
- `]e0` – GS1 DataBar.
- `]d2` – İlk konumunda ECC 200 ve FNC1 (`2`) olan DataMatrix (`d`), GS1 DataMatrix olarak da bilinir.
- `]Q3` – İlk konumunda FNC1 olan (`3`) QR Kodu (`Q`) Model 2 sembolü, GS1 QR Kodu olarak da bilinir.
- `]J1` – GS1 DotCode.

Bu tanımlayıcıları kullanırsanız, GS1 olmayan barkodlar ile uyumluluk için, tarayıcıların veya tarama yazılımının GS1 tanımlayıcılarına karşılık gelmeyen tanımlayıcıları kaldırmak üzere yapılandırılması gerekir. Örneğin, "normal" bir Code 39 barkodunu tarıyorsanız `]A0` öneki eklenir. Sistem bu öneki GS1 öneklerinden biri olarak anlamayacağından, bunu bir veri olarak yorumlar ve beklenmedik sonuçlara neden olur.

> [!NOTE]
> Kolaylık sağlamak için, Warehouse Management mobil uygulamasının sürüm 2.0.17.0 ve sonrasında, önceki listede bulunmayan tüm AIM önekleri kaldırılmıştır. Bu davranış, tarayıcıyı AIM önekini eklemek ancak istenmeyen önekleri kaldırmamak üzere yapılandırdığınız durumları destekler.

### <a name="single-and-multiple-field-scanning"></a>Tek ve çoklu alan taraması

Veriler barkoddan ayrıştırıldıktan sonra, mobil aygıt akış denetimlerine eklenecektir. Sırayla işlenecek iki yöntem vardır:

- **Tek alan taraması** – Bu yöntem yalnızca barkodun tarandığı alanı doldurur. Örneğin imleç **Madde** alanındayken `<FNC1>`**`01`**`09521101530001`**`17`**`210119`**`10`**`AB-123` barkodunu tararsanız barkoddaki `09521101530001` numaralı GTIN bu alana girilir. Örneğin imleç **Toplu İş Kimliği** alanındayken aynı barkodu tararsanız barkoddaki `AB-123` toplu iş numarası girilir. Bu mod tüm akışlarda tüm alanlar için çalışır ve yalnızca GS1 genel kurulumunun yapılandırılmış olmasını gerektirir. Mobil cihaz akışına aynı anda yalnızca bir barkod parçası girilebileceğinden, bir barkod birden çok öğe içeriyorsa birden çok kez taranmalıdır. Bu davranış, [Genel GS1 kurulumunu oluşturma](#generic-gs1-setup) bölümünde açıklandığı gibi GS1 genel kurulumu tarafından denetlenir.
- **Çoklu alan taraması** – Bir barkod tarandığında, mobil cihazın akış durumuna ek veriler göndererek birden çok alanı doldurur. Örneğin ilke, uygulama tanımlayıcısı 01'i `ItemId` denetimine ve uygulama tanımlayıcısı 10'u `InventBatchId` alanına göndermek üzere yapılandırılmıştır. Bu durumda, `<FNC1>`**`01`**`09521101530001`**`17`**`210119`**`10`**`AB-123` barkodunu tararsanız her iki değişkenin verileri aynı anda iletilecektir. Bu nedenle sistem, akışta madde ve/veya toplu iş numarası için sizi uyarmaz. Bu davranış, [Mobil cihaz menü öğelerine GS1 ilkelerini ayarlama](#policies-for-menus) bölümünde açıklandığı gibi, menü öğelerine bağlı GS1 ilkeleri tarafından denetlenir.

> [!WARNING]
> Varsayılan GS1 ilkeleri, beklenmeyen davranışlar olmaksızın çalışacak şekilde sınanmıştır. Ancak, menü öğelerine bağlanan GS1 ilkelerinin özelleştirilmesi beklenmeyen davranışlara neden olabilir, çünkü akış, bazı verilerin belirli bir zamanda kullanılabilir olmasını beklemeyebilir.

## <a name="turn-on-the-gs1-feature"></a>GS1 özelliğini açma

Bu özelliği kullanabilmeniz için sisteminizde etkinleştirmeniz gerekir. Yöneticiler özellik durumunu denetlemek ve etkinleştirmek için [özellik yönetimi](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) ayarlarını kullanabilir. **Özellik yönetimi** çalışma alanındabu özellik aşağıdaki şekilde listelenir:

- **Modül:** *Ambar yönetimi*
- **Özellik adı:** *GS1 barkodlarını tara*

### <a name="turn-on-the-enhanced-parser-for-gs1-barcodes-feature"></a>GS1 barkodları için geliştirilmiş ayrıştırıcı özelliğini açma

GS1 barkodları kullanıyorsanız *GS1 barkodları için geliştirilmiş ayrıştırıcı* özelliğin de etkinleştirmeniz önerilir. Bu özellik GS1 barkod ayrıştırıcısının gelişmiş bir uygulamasını sağlar. Aşağıdaki geliştirmeleri ekler:

- Sembol verilerinin ayrıştırılması için GS1 Genel Şartname algoritmasını izler ve semboldeki verilerin şartnameye göre geçerli olduğunu doğrular.
- **Tanımlayıcının maksimum uzunluğu** değeri ayarlamanızı gerektirmez ve yapılandırılan uygulama tanımlayıcıları arasından en uzun önek eşleşmesini kullanır.
- Herhangi bir sayıyla eşleştirmek için, *n* harfini kullanarak ondalık uygulama tanımlayıcılarını daha kolay yapılandırmanıza olanak sağlar. Örneğin, ayrı uygulama tanımlayıcıları (*3101*, *3102*, *3103* vb.) yerine yalnızca tek bir uygulama tanımlayıcı (*310n*) yapılandırabilirsiniz.
- Hatalı kodlanmış verilerin alan verileri olarak yorumlanmasına neden olan bir sorunu giderir.
- Başka bağlamlarda yeniden kullanılabilen ayrı bir sınıf olarak gelir ve akış alanları doldurulmadan önce taranan verileri değiştirmek için bir genişletilebilirlik noktası kullanılmasına olanak sağlar.

## <a name="set-up-global-gs1-options"></a><a name="set-gs1-options"></a>Genel GS1 seçeneklerini ayarlama

**Ambar yönetimi parametreleri** sayfasında, genel GS1 seçeneklerini oluşturan birkaç ayar sağlanır.

Genel GS1 seçeneklerini ayarlamak için aşağıdaki adımları izleyin.

1. **Ambar yönetimi \> Kurulum \> Ambar yönetim parametreleri**'ne gidin.
1. **Barkodlar** hızlı sekmesinde, aşağıdaki alanları ayarlayın:

    - **FNC1 karakteri**, **Datamatrix karakteri** ve **QR kodu karakteri** – Her bir GS1 barkodu için önek olarak yorumlanması gereken karakterleri belirtin.
    - **Grup ayırıcısı** – ASCII grup ayırıcı karakterinin yerini alan karakteri belirtin.
    - **Tanımlayıcının maksimum uzunluğu**: Uygulama tanımlayıcısı için izin verilen maksimum karakter sayısını belirtin. Sisteminizde *Geliştirilmiş GS1 Ayrıştırıcı* özelliği açıksa bu alan gerekli değildir.

> [!NOTE]
> Ön ekler, sisteme bir barkodun GS1 standardına göre kodlandığını söyler. Eş zamanlı olarak ve çeşitli amaçlar için en fazla üç ön ek (**FNC1 Karakteri**, **Datamatrix karakteri** ve **QR kodu karakteri**) kullanılabilir.

## <a name="gs1-application-identifiers"></a>GS1 uygulama tanımlayıcıları

GS1 biçimleri yalnızca verileri kodlamaz, aynı zamanda verilerin anlamını tanımlamak için önceden tanımlanmış bir uygulama tanımlayıcıları listesi kullanmanıza olanak tanır. Lojistik yöneticilerinin, gerekli uygulama tanımlayıcıları listesini ayarlaması ve tanımlayıcıların her birini uygun mobil cihaz menü öğeleriyle ilişkilendirmesi gerekir. Ardından tanımlayıcılar, taşıma ve paketleme amacıyla genel bir ayar olarak ambarlar genelinde kullanılabilir. Böylece tüm gönderim etiketleri, birleşik bir form alır.

Sistem, taranan bilgilerin ilgili parçasına uygulanması gereken kuralları oluşturmak için verileri, özellikle de önceden tanımlanmış uygulama tanımlayıcılarını kullanır.

Her uygulama tanımlayıcısı, taranan barkoddaki sonraki karakterlerin şifreli bilgiler bloğu olarak değerlendirilmesi gerektiğine dair sisteme işaret gönderir. Uygulama tanımlayıcılarının kurulumu, sistemin barkodu nasıl yorumlaması ve bunu sistemde değer olarak kaydetmesi gerektiğini tanımlar.

Lojistik yöneticileri, standart uluslararası uygulama tanımlayıcılarını kullanabilir ve/veya kendi tanımlayıcılarını oluşturabilir.

### <a name="load-the-standard-application-identifiers"></a>Standart uygulama tanımlayıcılarını yükleme

Hızlı bir şekilde başlamak için yaygın uluslararası uygulama tanımlayıcılarının listesini yükleyebilirsiniz. Daha sonra gerektiği gibi listeyi genişletebilir veya düzenleyebilirsiniz.

Standart uygulama tanımlayıcılarını yüklemek için aşağıdaki adımları izleyin.

1. **Ambar yönetimi \> Kurulum \> GS1 \> GS1 uygulama tanımlayıcıları**'na gidin.
1. Eylem Bölmesinde **Varsayılan ayar oluştur**'u seçin.

> [!WARNING]
> **Varsayılan kurulum oluştur** komutu, geçerli olarak tanımlanan tüm uygulama tanımlayıcılarını siler ve yerine standart listeyi getirir. Ancak varsayılan kurulumu yükledikten sonra listeyi gerektiği gibi özelleştirebilirsiniz.

### <a name="set-up-custom-application-identifiers"></a>Özel uygulama tanımlayıcılarını ayarlama

Şirketinizin kullandığı bazı veya tüm uygulama tanımlayıcıları, standart kümeden farklıysa sıfırdan kendi kodlarınızı oluşturabilir veya standart kümeyi gerektiği şekilde özelleştirebilirsiniz.

Kendi GS1 uygulama tanımlayıcılarınızı ayarlamak ve özelleştirmek için aşağıdaki adımları izleyin.

1. **Ambar yönetimi \> Kurulum \> GS1 \> GS1 uygulama tanımlayıcıları**'na gidin.
1. Şu adımlardan birini izleyin:

    - Yeni tanımlayıcı oluşturmak için: Eylem Bölmesi'nde **Yeni**'yi seçin.
    - Mevcut bir tanımlayıcıyı düzenlemek için: Tanımlayıcıyı seçin ve ardından Eylem Bölmesi'nde, **Düzenle** seçeneğini belirleyin.

1. Yeni veya seçili tanımlayıcı için aşağıdaki alanları ayarlayın:

    - **Uygulama tanımlayıcısı**: Uygulama tanımlayıcısı için tanımlama kodunu girin. Genellikle bu kod iki basamaklı bir tamsayıdır ancak daha uzun olabilir. Ondalık değerler için son basamak, ondalık basamak sayısını belirtir. Daha fazla bilgi için daha sonra bu listede **Ondalık** onay kutusu açıklamasına bakın. *GS1 barkodları için geliştirilmiş ayrıştırıcı* özelliği etkinse, uygulama tanımlayıcısındaki son karakter olarak *n* harfini kullanarak, tüm ondalık basamak çeşitleri için tek bir uygulama tanımlayıcısı oluşturabilirsiniz. Örneğin, her bir ondalık basamak numarası için ayrı bir uygulama tanımlayıcı (*3101*, *3102*, *3103* vb.) yerine yalnızca tek bir uygulama tanımlayıcı (*310n*) yapılandırabilirsiniz.
    - **Açıklama**: Tanımlayıcının kısa açıklamasını girin.
    - **Sabit uzunluk**: Bu uygulama tanımlayıcını kullanarak taranan değerlerde sabit karakter sayısı varsa bu onay kutusunu işaretleyin. Değerlerin uzunluğu değişkense bu onay kutusunu temizleyin. Bu durumda, **Ambar yönetimi parametreleri** sayfasında belirttiğiniz grup ayırıcı karakterini kullanarak değerin bitişini belirtmeniz gerekir.
    - **Uzunluk**: Bu uygulama tanımlayıcısını kullanarak taranan değerlerde görünebilen maksimum karakter sayısını girin. **Sabit uzunluk** onay kutusu işaretliyse tam olarak bu karakter sayısı beklenir.
    - **Tür**: Bu uygulama tanımlayıcısını kullanarak taranan değerin türünü seçin (*Sayısal*, *Alfasayısal* veya *Tarih*). Tarihlerin ve sayıların barkod verilerinde nasıl gösterileceği hakkında daha fazla bilgi için [Tarihler ve ondalık sayılar](#dates-and-decimal-numbers) bölümüne bakın.
    - **Ondalık**: Değer kasıtlı bir ondalık virgülü içeriyorsa bu onay kutusunu seçin. Bu kutu seçilirse sistem, ondalık basamak sayısını belirlemek için uygulama tanımlayıcısının son basamağını kullanır. Tarihlerin ve sayıların barkod verilerinde nasıl gösterileceği hakkında daha fazla bilgi için [Tarihler ve ondalık sayılar](#dates-and-decimal-numbers) bölümüne bakın.

> [!WARNING]
> Sistem, herhangi bir uygulama tanımlayıcısı için **Sabit uzunluk** onay kutusunu ayarlamanıza izin verse de, bu onay kutusu yalnızca GS1 Genel Şartnamesine uygun bir önceden tanımlanmış uzunluğu olan uygulama tanımlayıcılarının alt kümesi için kullanılmalıdır. Gelişmiş GS1 ayrıştırıcı önceden tanımlanmış uzunlukları olan tüm uygulama tanımlayıcılarının listesini zaten içerir.

> [!NOTE]
> **Ambar yönetimi parametreleri** sayfasında belirtilen **Grup ayırıcı** değeri, uygulama tanımlayıcısından sonra gelen değerin sabit bir uzunluğu varsa isteğe bağlıdır.

## <a name="establish-the-generic-gs1-setup"></a><a name="generic-gs1-setup"></a>Genel GS1 kurulumunu oluşturma

Genel GS1 kurulumu, ortak bir eşlemeler topluluğu oluşturur. Bu eşlemeler, mobil uygulamadaki her bir ilgili giriş alanını taranan barkodlardaki değerlerin bu alanda nasıl yorumlanıp depolanması gerektiğini kontrol eden uygulama tanımlayıcısı ile eşleştirir. Varsayılan olarak, bu ayarlar tüm mobil cihaz menü öğelerinin tüm taramaları için geçerlidir. Ancak bunlar, belirli bir menü öğesine atanan bir GS1 ilkesine göre bir veya daha fazla belirli alan için geçersiz kılınabilir.

Genel GS1 kurulumu, tek seferde yalnızca bir değerin taranmasına olanak tanır. Bu nedenle, tek bir taramadan birden fazla alan değeri yüklemek isterseniz ilgili menü öğeleri için bir GS1 ilkesi ayarlamanız gerekir.

GS1 ilkeleri hakkında daha fazla bilgi için sonraki bölüme bakın.

### <a name="load-the-standard-generic-gs1-setup"></a>Standart genel GS1 kurulumunu yükleme

**GS1 genel kurulumu** sayfası, mobil cihaz alanları ile varsayılan kurulum tarafından oluşturulan standart uygulama tanımlayıcıları arasında standart bir eşleme kümesi yüklemenize olanak tanır.

Genel GS1 kurulumunu oluşturmak için **Ambar yönetimi \> Kurulum \> GS1 \> GS1 genel kurulumu**'na gidin. Ardından genellikle mobil cihaz menü öğeleri tarafından kullanılan her alana otomatik olarak uygun bir uygulama tanımlayıcısı atamak için **Varsayılan kurulum oluştur**'u seçin.

> [!WARNING]
> Herhangi bir genel GS1 kurulumu zaten varsa **Varsayılan kurulum oluştur** komutu bunu tamamen siler ve standart kurulumu yükler.

### <a name="customize-the-standard-generic-gs1-setup"></a>Standart genel GS1 kurulumunu özelleştirme

Genel GS1 kurulumunu özelleştirmek için aşağıdaki adımları izleyin.

1. **Ambar yönetimi \> Kurulum \> GS1 \> GS1 genel kurulumu**'na gidin.
1. Şu adımlardan birini izleyin:

    - Yeni bir eşleme oluşturmak için: Eylem Bölmesi'nde **Yeni**'yi seçin.
    - Mevcut bir eşlemeyi düzenlemek için: Eşlemeyi seçin ve ardından Eylem Bölmesi'nde, **Düzenle** seçeneğini belirleyin.

1. Yeni veya seçili eşleme için aşağıdaki alanları ayarlayın:

    - **Alan**: Gelen değerin atanması gereken mobil uygulama giriş alanını seçin veya girin. Değer, çalışanların gördüğü görünen ad değildir. Bunun yerine bu, temel koddaki alana atanan anahtar addır. Varsayılan kurulum, faydalı olabilecek bir alan koleksiyonu sağlar ve her alan için sezgisel anahtar adları ve eşleşen programlanabilir işlevi içerir. Ancak uygulamanız için doğru seçimleri bulmak üzere geliştirme iş ortaklarınızla konuşmanız gerekebilir.
    - **Uygulama tanımlayıcısı**: **GS1 uygulama tanımlayıcıları** sayfasında tanımlandığı üzere uygun uygulama tanımlayıcısını seçin. Tanımlayıcı, barkodun nasıl yorumlanacağını ve adlandırılmış alan için değer olarak nasıl depolanacağını belirler. Uygulama tanımlayıcısını seçtikten sonra **Açıklama** alanında buna dair açıklama gösterilir.

## <a name="set-up-gs1-policies-to-be-to-mobile-device-menu-items"></a><a name="policies-for-menus"></a>Mobil cihaz menü öğelerine atanacak GS1 ilkelerini ayarlama

GS1 standardının amacı, çalışanların tek bir barkodu bir kez taradığında çeşitli değerleri yüklemesini sağlamaktır. Bu amaca ulaşmak için lojistik yöneticilerinin sisteme birden çok değerli barkodları nasıl yorumlayacağını belirten GS1 ilkelerini ayarlamanız gerekir. Daha sonra, çalışanlar belirli bir menü öğesini kullanırken bir barkodu taradığında bunun nasıl yorumlanacağını kontrol etmek için mobil cihaz menü öğelerine ilkeler atayabilirsiniz.

Menü öğesine GS1 ilkesi atanmadıysa sistem yalnızca tek bir değer yakalayabilir. Bu değer, genel GS1 kurulumu tarafından belirtildiği üzere çalışan taramayı yaptığında seçilen mobil uygulama girişine uygulanır. Menü öğesine GS1 ilkesi atanırsa sistem, ilk barkod değerini seçili alanla eşlemek için yine de genel GS1 kurulumunu kullanır. Ancak geçerli ilke tarafından belirtildiği üzere ek alan değerlerini yakalayabilir.

### <a name="load-the-standard-specific-gs1-policies"></a>Standart özel GS1 ilkelerini yükleme

Hızlı bir şekilde başlamak için bir dizi GS1 ilkesi yükleyebilirsiniz. Daha sonra gerektiği gibi ilkeleri genişletebilir veya düzenleyebilirsiniz.

Standart uygulama tanımlayıcılarını yüklemek için aşağıdaki adımları izleyin.

1. **Ambar yönetimi \> Kurulum \> GS1 \> GS1 ilkesi**'ne gidin.
1. Eylem Bölmesinde **Varsayılan ayar oluştur**'u seçin.

> [!WARNING]
> **Varsayılan kurulum oluştur** komutu, geçerli olarak tanımlanan tüm ilkeleri siler ve yerine standart ilke kümesini getirir. Ancak varsayılan kurulum yüklendikten sonra ilkeleri gerektiği gibi özelleştirebilirsiniz.

### <a name="set-up-custom-specific-gs1-policies"></a>Özel belirli GS1 ilkelerini ayarlama

> [!WARNING]
> Bazı GS1 ilkeleri, kullandığınız her mobil akışta çalışmayabilir. Özel GS1 ilkelerini yapılandırdığınızda, akışın farklı noktalarında taranan farklı bilgi parçalarını kullanarak mobil cihaz akışını sınamanız gerekir; bu şekilde akışın beklediğiniz gibi davranıp davranmadığını belirleyebilirsiniz.

GS1 ilkelerinizi ayarlamak ve özelleştirmek için aşağıdaki adımları izleyin.

1. **Ambar yönetimi \> Kurulum \> GS1 \> GS1 ilkesi**'ne gidin.
1. Şu adımlardan birini izleyin:

    - Yeni bir ilke oluşturmak için: Eylem Bölmesi'nde **Yeni**'yi seçin.
    - Mevcut bir ilkeyi düzenlemek için: Liste bölmesinde ilkeyi seçin.

1. Yeni veya seçili ilkenin üst bilgisinde aşağıdaki alanları ayarlayın:

    - **İlke adı**: İlke için bir ad girin.
    - **Açıklama**: İlkenin kısa açıklamasını girin.

1. Üst bilginin altındaki hızlı sekmede, geçerli ilke için gerektiği üzere alan adlarını uygulama tanımlayıcılarıyla eşleyin. Gerektiği gibi sıra eklemek veya kaldırmak için araç çubuğundaki düğmeleri kullanın. Her satır için aşağıdaki alanları ayarlayın:

    - **Alan**: Gelen değerin atanması gereken mobil uygulama giriş alanını seçin veya girin. Değer, çalışanların gördüğü görünen ad değildir. Bunun yerine bu, temel koddaki alana atanan anahtar addır. Varsayılan kurulum, faydalı olabilecek bir alan koleksiyonu sağlar ve her alan için sezgisel anahtar adları ve eşleşen programlanabilir işlevi içerir. Ancak uygulamanız için doğru seçimleri bulmak üzere geliştirme iş ortaklarınızla konuşmanız gerekebilir.
    - **Uygulama tanımlayıcısı**: **GS1 uygulama tanımlayıcıları** sayfasında tanımlandığı üzere uygun uygulama tanımlayıcısını seçin. Tanımlayıcı, barkodun nasıl yorumlanacağını ve adlandırılmış alan için değer olarak nasıl depolanacağını belirler. Uygulama tanımlayıcısını seçtikten sonra **Açıklama** alanında buna dair açıklama gösterilir.
    - **Sıralama**: Her birden çok değerli barkod, her biri bir değer tarafından izlenen bir dizi uygulama tanımlayıcısı içerir. Uygulanabilir GS1 ilkesi, her veritabanı alanıyla hangi uygulama tanımlayıcısının eşlendiğini tanımlar. Ancak bir barkod aynı uygulama tanımlayıcısını birden çok kez kullanıyorsa sistem, uygulama tanımlayıcılarını alanlarla eşlemek için bunların kodda görüntülenme sırasını kullanır. Uygulama tanımlayıcısını bir veya daha fazla diğer satırla paylaşan satırlar için eşleşen satırların işlendiği sırayı oluşturmak üzere bu alanı kullanın. En düşük sıralama değerine sahip satır önce işlenir.

> [!NOTE]
> Birden fazla aynı uygulama tanımlayıcısı içeren barkodlar için alanların sırasını oluşturmak üzere **Sıralama** alanını kullanmanız *gerekir*.

## <a name="assign-gs1-policies-to-mobile-device-menu-items"></a>Mobil cihaz menü öğelerine GS1 ilkeleri atama

Varsayılan olarak tüm taşınabilir cihaz menüsü öğeleri, çalışanların genel GS1 kurulumuna göre tek bir değeri tarayabileceği giriş alanları sağlar. Çalışanların mobil cihaz menü öğeleri için tek bir taramada birden fazla alan değerini tarayabilmesini isterseniz aşağıdaki adımları izleyerek bir GS1 ilkesi atamanız gerekir.

1. **Ambar yönetimi \> Kurulum \> Mobil cihaz \> Mobil cihaz menüsü öğeleri**'ne gidin.
1. Bir menü öğesi oluşturun veya açın.
1. **Genel** hızlı sekmesinde, **GS1 ilkesi** alanını menü öğesine uygulanan ilke olarak ayarlayın.

## <a name="gs1-setup-example"></a>GS1 kurulum örneği

Bu örnek, GS1 seçeneklerinin aşağıdaki şekilde ayarlandığı bir sistem için geçerlidir:

- **Ambar yönetimi parametreleri** sayfasında, aşağıdaki genel ayarlar oluşturulur:

    - **FNC1 karakteri:** *\]C1*
    - **Grup ayırıcı:** *\~*

- **GS1 uygulama tanımlayıcıları** sayfasında, aşağıdaki uygulama tanımlayıcıları bu örnekle ilgilidir.

    | Uygulama tanımlayıcısı | Tanım | Sabit uzunluk | Uzunluk | Türü | Ondalık |
    |---|---|---|---|---|---|
    | 01 | GTIN | Seçili | 14 | Sayısal | Temizlenmiş |
    | 10 | Parti numarası | Temizlenmiş | 20 | Alfasayısal | Temizlenmiş |
    | 17 | Bitiş tarihi | Seçili | 6 | Date | Temizlenmiş |
    | 30 | Miktar alınıyor | Temizlenmiş | 8 | Sayısal | Temizlenmiş |

- **GS1 genel kurulumu** sayfasında, genel GS1 ilkesi için aşağıdaki ayarlar bu örnekle ilgilidir.

    | Alan | Uygulama tanımlayıcısı | Tanım |
    |---|---|---|
    | ItemId | 01 | GTIN |

- **GS1 ilkesi** sayfasında, **İlke adı** alanının *Satınalma alınıyor* olarak ayarlandığı ilke bulunur. Bu ilke, aşağıdaki satırları içerir.

    | Alan | Uygulama tanımlayıcısı | Tanım | Sıralama |
    |---|---|---|---|
    | ExpDate | 17 | Bitiş tarihi | 0 |
    | InventBatchId | 10 | Parti numarası | 0 |
    | Miktar | 30 | Miktar alınıyor | 0 |

- **Mobil cihaz menü öğeleri** sayfasında, *Satınalma alınıyor* adlı bir menü öğesi bulunur. Bunun **GS1 ilkesi** alanı *Satınalma alınıyor* olarak ayarlanır.

Satınalma siparişi için mallar ambara ulaştıktan sonra çalışan şu adımları izler.

1. Mobil cihazda, **Satınalma alınıyor** menü öğesini seçin.
1. Satınalma siparişi numarasını girin.
1. **Öğe** alanını seçin ve şu barkodu tarayın: `]C10100000012345678~3030~10b1~17220215`.

Bu örnek için oluşturulan ayarlar nedeniyle sistem, taranan barkodu aşağıdaki şekilde ayrıştırır.

| Alan anahtarı | Başvuru kodu | Değer | Dekont |
|---|---|---|---|
| ItemId | 01 | 00000012345678 | Çalışan **Öğe** alanını taradığından barkoddaki ilk değer bu alanla eşlenir. Eşleme, GS1 genel kurulumundan alınır. |
| Miktar | 30 | 30 | Tek bir taramada birden fazla alan değeri yakalandığından bu eşleme ve tüm kalan eşlemeler, **Satınalma alınıyor** menü öğesine atanan GS1 ilkesinden alınır. Bu değer, alınan miktardır. |
| InventBatchId | 10 | b1 | Bu değer, toplu iş kimliğidir. |
| ExpDate | 17 | 220215 | Tarih biçimi, YYAAGG'dir. Bu nedenle, bitiş tarihi 15 Şubat 2022'dir. |

Daha sonra makbuz kaydedilir ve tek bir taramadan sonra ilgili veritabanı değerleri girilir.
