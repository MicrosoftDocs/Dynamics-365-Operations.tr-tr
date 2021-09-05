---
title: GS1 barkodları ve QR kodları
description: Bu konuda, etiketlerin bir ambarda taranabilmesi için GS1 barkodlarının ve QR kodlarının nasıl ayarlanacağı açıklanmaktadır.
author: Mirzaab
ms.date: 08/02/2021
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2021-08-02
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: ef28fcaf308225a78bcbac42f591e6b24b21b1b1
ms.sourcegitcommit: 2b04b5a5c883d216072bb91123f9c7709a41f69a
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/16/2021
ms.locfileid: "7384549"
---
# <a name="gs1-bar-codes-and-qr-codes"></a>GS1 barkodları ve QR kodları

[!include [banner](../includes/banner.md)]
[!INCLUDE [preview-banner](../includes/preview-banner.md)]

Ambar çalışanlarının genellikle bir madde, palet veya konteynerin hareketlerini kaydetmek için mobil cihaz tarayıcısı kullanırken birkaç görevi tamamlaması gerekir. Bu görevler, mobil cihazda barkodları taramayı ve bilgileri el ile girmeyi içerebilir. Barkodlarda, Microsoft Dynamics 365 Supply Chain Management ile tanımlayıp yönettiğiniz şirkete özel bir biçim kullanılır.

Sevkiyat etiketleri için GS1 barkodu ve QR kodu biçimleri, şirketler arasında veri alışverişine yönelik genel bir standart sağlamak üzere geliştirilmiştir. GS1 biçimleri yalnızca verileri kodlamaz, aynı zamanda verilerin anlamını tanımlamak için önceden tanımlanmış bir *uygulama tanımlayıcıları* listesi kullanmanıza olanak tanır. GS1 standardı, veri biçimini ve kodlamak için kullanılabilecek çeşitli veri türlerini tanımlar. Eski barkodların aksine GS1 barkodlarında birden fazla veri öğesi bulunabilir. Bu nedenle, tek bir barkod taraması toplu iş ve son kullanma tarihi gibi çeşitli ürün bilgisi türlerini yakalayabilir.

Supply Chain Management'taki GS1 desteği, paletlerin ve konteynerlerin GS1 biçiminde kodları kullanarak etiketlendiği ambarlarda tarama işlemini önemli ölçüde kolaylaştırır. Ambar çalışanları, GS1 barkodunun tek bir taraması üzerinden gerekli tüm bilgileri ayıklayabilir. GS1 barkodları, birden çok tarama yapma ve/veya el ile bilgi girme ihtiyacını ortadan kaldırarak görevlerle ilişkili zamanın azaltılmasına yardımcı olur. Aynı zamanda, doğruluğu artırmaya da yardım eder.

Lojistik yöneticilerinin, gerekli uygulama tanımlayıcıları listesini ayarlaması ve tanımlayıcıların her birini uygun mobil cihaz menü öğeleriyle ilişkilendirmesi gerekir. Ardından uygulama tanımlayıcıları, taşıma ve paketleme amacıyla genel bir ayar olarak ambarlar genelinde kullanılabilir. Böylece tüm gönderim etiketleri, birleşik bir form alır.

Aksi belirtilmedikçe, bu konuda barkodlara ve QR kodlarına atıfta bulunmak için *barkod* terimi kullanılmaktadır.

## <a name="turn-on-the-gs1-feature"></a>GS1 özelliğini açma

Bu özelliği kullanabilmeniz için sisteminizde etkinleştirmeniz gerekir. Yöneticiler özellik durumunu denetlemek ve etkinleştirmek için [özellik yönetimi](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) ayarlarını kullanabilir. **Özellik yönetimi** çalışma alanındabu özellik aşağıdaki şekilde listelenir:

- **Modül:** *Ambar yönetimi*
- **Özellik adı:** *GS1 barkodlarını tarama*

## <a name="set-up-global-gs1-options"></a>Genel GS1 seçeneklerini ayarlama

**Ambar yönetimi parametreleri** sayfasında, genel GS1 seçeneklerini oluşturan birkaç ayar sağlanır.

Genel GS1 seçeneklerini ayarlamak için şu adımları izleyin.

1. **Ambar yönetimi \> Kurulum \> Ambar yönetim parametreleri**'ne gidin.
1. **Barkodlar** hızlı sekmesinde, aşağıdaki alanları ayarlayın:

    - **FNC1 Karakteri**: Barkod ayrıştırıldığında ön ek olarak yorumlanması gereken karakterleri belirtin.
    - **Datamatrix karakteri**: Datamatrix ayrıştırıldığında ön ek olarak yorumlanması gereken karakterleri belirtin.
    - **QR kodu karakteri**: QR kodu ayrıştırıldığında ön ek olarak yorumlanması gereken karakterleri belirtin.
    - **Grup ayırıcı**: Barkodun veya QR kodunun ayrı parçalarını tanımlayan karakteri belirtin.
    - **Tanımlayıcının maksimum uzunluğu**: Uygulama tanımlayıcısı için izin verilen maksimum karakter sayısını belirtin.

> [!NOTE]
> Ön ekler, sisteme bir barkodun GS1 standardına göre şifrelendiğini söyler. Eş zamanlı olarak ve çeşitli amaçlar için en fazla üç ön ek (**FNC1 Karakteri**, **Datamatrix karakteri** ve **QR kodu karakteri**) kullanılabilir.

## <a name="gs1-application-identifiers"></a>GS1 uygulama tanımlayıcıları

GS1 biçimleri yalnızca verileri kodlamaz, aynı zamanda verilerin anlamını tanımlamak için önceden tanımlanmış bir uygulama tanımlayıcıları listesi kullanmanıza olanak tanır. Lojistik yöneticilerinin, gerekli uygulama tanımlayıcıları listesini ayarlaması ve tanımlayıcıların her birini uygun mobil cihaz menü öğeleriyle ilişkilendirmesi gerekir. Ardından tanımlayıcılar, taşıma ve paketleme amacıyla genel bir ayar olarak ambarlar genelinde kullanılabilir. Böylece tüm gönderim etiketleri, birleşik bir form alır.

Sistem, taranan bilgilerin ilgili parçasına uygulanması gereken kuralları oluşturmak için verileri, özellikle de önceden tanımlanmış uygulama tanımlayıcılarını kullanır.

Her uygulama tanımlayıcısı, taranan barkoddaki sonraki karakterlerin şifreli bilgiler bloğu olarak değerlendirilmesi gerektiğine dair sisteme işaret gönderir. Uygulama tanımlayıcılarının kurulumu, sistemin barkodu nasıl yorumlaması ve bunu sistemde değer olarak kaydetmesi gerektiğini tanımlar.

Lojistik yöneticileri, standart uluslararası uygulama tanımlayıcılarını kullanabilir ve/veya kendi tanımlayıcılarını oluşturabilir.

### <a name="load-the-standard-application-identifiers"></a>Standart uygulama tanımlayıcılarını yükleme

Hızlı bir şekilde başlamak için yaygın uluslararası uygulama tanımlayıcılarının listesini yükleyebilirsiniz. Daha sonra gerektiği gibi listeyi genişletebilir veya düzenleyebilirsiniz.

Standart uygulama tanımlayıcılarını yüklemek için şu adımları izleyin.

1. **Ambar yönetimi \> Kurulum \> GS1 \> GS1 uygulama tanımlayıcıları**'na gidin.
1. Eylem Bölmesinde **Varsayılan ayar oluştur**'u seçin.

> [!WARNING]
> **Varsayılan kurulum oluştur** komutu, geçerli olarak tanımlanan tüm uygulama tanımlayıcılarını siler ve yerine standart listeyi getirir. Ancak varsayılan kurulumu yükledikten sonra listeyi gerektiği gibi özelleştirebilirsiniz.

### <a name="set-up-custom-application-identifiers"></a>Özel uygulama tanımlayıcılarını ayarlama

Şirketinizin kullandığı bazı veya tüm uygulama tanımlayıcıları, standart kümeden farklıysa sıfırdan kendi kodlarınızı oluşturabilir veya standart kümeyi gerektiği şekilde özelleştirebilirsiniz.

Kendi GS1 uygulama tanımlayıcılarınızı ayarlamak ve özelleştirmek için şu adımları izleyin.

1. **Ambar yönetimi \> Kurulum \> GS1 \> GS1 uygulama tanımlayıcıları**'na gidin.
1. Şu adımlardan birini izleyin:

    - Yeni tanımlayıcı oluşturmak için: Eylem Bölmesi'nde **Yeni**'yi seçin.
    - Mevcut bir tanımlayıcıyı düzenlemek için: Tanımlayıcıyı seçin ve ardından Eylem Bölmesi'nde, **Düzenle** seçeneğini belirleyin.

1. Yeni veya seçili tanımlayıcı için aşağıdaki alanları ayarlayın:

    - **Uygulama tanımlayıcısı**: Uygulama tanımlayıcısı için tanımlama kodunu girin. Genellikle bu kod iki basamaklı bir tamsayıdır ancak daha uzun olabilir. Ondalık değerler için son basamak, ondalık basamak sayısını belirtir. Daha fazla bilgi için daha sonra bu listede **Ondalık** onay kutusu açıklamasına bakın.
    - **Açıklama**: Tanımlayıcının kısa açıklamasını girin.
    - **Sabit uzunluk**: Bu uygulama tanımlayıcını kullanarak taranan değerlerde sabit karakter sayısı varsa bu onay kutusunu işaretleyin. Değerlerin uzunluğu değişkense bu onay kutusunu temizleyin. Bu durumda, **Ambar yönetimi parametreleri** sayfasında belirttiğiniz grup ayırıcı karakterini kullanarak değerin bitişini belirtmeniz gerekir.
    - **Uzunluk**: Bu uygulama tanımlayıcısını kullanarak taranan değerlerde görünebilen maksimum karakter sayısını girin. **Sabit uzunluk** onay kutusu işaretliyse tam olarak bu karakter sayısı beklenir.
    - **Tür**: Bu uygulama tanımlayıcısını kullanarak taranan değerin türünü seçin (*Sayısal*, *Alfasayısal* veya *Tarih*). Tarihler için beklenen biçim YYAAGG'dir (boşluk veya tire olmadan).
    - **Ondalık**: Değer kasıtlı bir ondalık virgülü içeriyorsa bu onay kutusunu seçin. Bu kutu seçilirse sistem, ondalık basamak sayısını belirlemek için uygulama tanımlayıcısının son basamağını kullanır. Örneğin, uygulama tanımlayıcısı *3205* ise değerin en sağdaki beş basamağı, ondalık virgülünden sonra gelecek şekilde yorumlanır.

> [!NOTE]
> Uygulama tanımlayıcısı tarafından izlenen değerin sabit uzunluğu varsa veya değer maksimum uzunluktaysa (yani uzunluk, uygulama tanımlayıcısı için ayarlanan **Uzunluk** değerine eşitse) **Ambar yönetimi parametreleri** sayfasında belirtilen grup ayırıcı isteğe bağlıdır.

## <a name="establish-the-generic-gs1-setup"></a>Genel GS1 kurulumunu oluşturma

Genel GS1 kurulumu, ortak bir eşlemeler topluluğu oluşturur. Bu eşlemeler, mobil uygulamadaki her bir ilgili giriş alanını taranan barkodlardaki değerlerin bu alanda nasıl yorumlanıp depolanması gerektiğini kontrol eden uygulama tanımlayıcısı ile eşleştirir. Varsayılan olarak, bu ayarlar tüm mobil cihaz menü öğelerinin tüm taramaları için geçerlidir. Ancak bunlar, belirli bir menü öğesine atanan bir GS1 ilkesine göre bir veya daha fazla belirli alan için geçersiz kılınabilir.

Genel GS1 kurulumu, tek seferde yalnızca bir değerin taranmasına olanak tanır. Bu nedenle, tek bir taramadan birden fazla alan değeri yüklemek isterseniz ilgili menü öğeleri için bir GS1 ilkesi ayarlamanız gerekir.

GS1 ilkeleri hakkında daha fazla bilgi için sonraki bölüme bakın.

### <a name="load-the-standard-generic-gs1-setup"></a>Standart genel GS1 kurulumunu yükleme

**GS1 genel kurulumu** sayfası, mobil cihaz alanları ile varsayılan kurulum tarafından oluşturulan standart uygulama tanımlayıcıları arasında standart bir eşleme kümesi yüklemenize olanak tanır.

Genel GS1 kurulumunu oluşturmak için **Ambar yönetimi \> Kurulum \> GS1 \> GS1 genel kurulumu**'na gidin. Ardından genellikle mobil cihaz menü öğeleri tarafından kullanılan her alana otomatik olarak uygun bir uygulama tanımlayıcısı atamak için **Varsayılan kurulum oluştur**'u seçin.

> [!WARNING]
> Herhangi bir genel GS1 kurulumu zaten varsa **Varsayılan kurulum oluştur** komutu bunu tamamen siler ve standart kurulumu yükler.

### <a name="customize-the-standard-generic-gs1-setup"></a>Standart genel GS1 kurulumunu özelleştirme

Genel GS1 kurulumunu özelleştirmek için şu adımları izleyin.

1. **Ambar yönetimi \> Kurulum \> GS1 \> GS1 genel kurulumu**'na gidin.
1. Şu adımlardan birini izleyin:

    - Yeni bir eşleme oluşturmak için: Eylem Bölmesi'nde **Yeni**'yi seçin.
    - Mevcut bir eşlemeyi düzenlemek için: Eşlemeyi seçin ve ardından Eylem Bölmesi'nde, **Düzenle** seçeneğini belirleyin.

1. Yeni veya seçili eşleme için aşağıdaki alanları ayarlayın:

    - **Alan**: Gelen değerin atanması gereken mobil uygulama giriş alanını seçin veya girin. Değer, çalışanların gördüğü görünen ad değildir. Bunun yerine bu, temel koddaki alana atanan anahtar addır. Varsayılan kurulum, faydalı olabilecek bir alan koleksiyonu sağlar ve her alan için sezgisel anahtar adları ve eşleşen programlanabilir işlevi içerir. Ancak uygulamanız için doğru seçimleri bulmak üzere geliştirme iş ortaklarınızla konuşmanız gerekebilir.
    - **Uygulama tanımlayıcısı**: **GS1 uygulama tanımlayıcıları** sayfasında tanımlandığı üzere uygun uygulama tanımlayıcısını seçin. Tanımlayıcı, barkodun nasıl yorumlanacağını ve adlandırılmış alan için değer olarak nasıl depolanacağını belirler. Uygulama tanımlayıcısını seçtikten sonra **Açıklama** alanında buna dair açıklama gösterilir.

## <a name="set-up-gs1-policies-that-you-can-assign-to-mobile-device-menu-items"></a>Mobil cihaz menü öğelerine atayabileceğiniz GS1 ilkelerini ayarlama

GS1 standardının amacı, çalışanların tek bir barkodu bir kez taradığında çeşitli değerleri yüklemesini sağlamaktır. Bu amaca ulaşmak için lojistik yöneticilerinin sisteme birden çok değerli barkodları nasıl yorumlayacağını belirten GS1 ilkelerini ayarlamanız gerekir. Daha sonra, çalışanlar belirli bir menü öğesini kullanırken bir barkodu taradığında bunun nasıl yorumlanacağını kontrol etmek için mobil cihaz menü öğelerine ilkeler atayabilirsiniz.

Menü öğesine GS1 ilkesi atanmadıysa sistem yalnızca tek bir değer yakalayabilir. Bu değer, genel GS1 kurulumu tarafından belirtildiği üzere çalışan taramayı yaptığında seçilen mobil uygulama girişine uygulanır. Menü öğesine GS1 ilkesi atanırsa sistem, ilk barkod değerini seçili alanla eşlemek için yine de genel GS1 kurulumunu kullanır. Ancak geçerli ilke tarafından belirtildiği üzere ek alan değerlerini yakalayabilir.

### <a name="load-the-standard-specific-gs1-policies"></a>Standart özel GS1 ilkelerini yükleme

Hızlı bir şekilde başlamak için bir dizi GS1 ilkesi yükleyebilirsiniz. Daha sonra gerektiği gibi ilkeleri genişletebilir veya düzenleyebilirsiniz.

Standart uygulama tanımlayıcılarını yüklemek için şu adımları izleyin.

1. **Ambar yönetimi \> Kurulum \> GS1 \> GS1 ilkesi**'ne gidin.
1. Eylem Bölmesinde **Varsayılan ayar oluştur**'u seçin.

> [!WARNING]
> **Varsayılan kurulum oluştur** komutu, geçerli olarak tanımlanan tüm ilkeleri siler ve yerine standart ilke kümesini getirir. Ancak varsayılan kurulum yüklendikten sonra ilkeleri gerektiği gibi özelleştirebilirsiniz.

### <a name="set-up-custom-specific-gs1-policies"></a>Özel belirli GS1 ilkelerini ayarlama

GS1 ilkelerinizi ayarlamak ve özelleştirmek için şu adımları izleyin.

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
1. **Öğe** alanını seçin ve şu barkodu tarayın: *\]C10100000012345678\~3030\~10b1\~17220215*.

Bu örnek için oluşturulan ayarlar nedeniyle sistem, taranan barkodu aşağıdaki şekilde ayrıştırır.

| Alan anahtarı | Başvuru kodu | Değer | Dekont |
|---|---|---|---|
| ItemId | 01 | 00000012345678 | Çalışan **Öğe** alanını taradığından barkoddaki ilk değer bu alanla eşlenir. Eşleme, GS1 genel kurulumundan alınır. |
| Miktar | 30 | 30 | Tek bir taramada birden fazla alan değeri yakalandığından bu eşleme ve tüm kalan eşlemeler, **Satınalma alınıyor** menü öğesine atanan GS1 ilkesinden alınır. Bu değer, alınan miktardır. |
| InventBatchId | 10 | b1 | Bu değer, toplu iş kimliğidir. |
| ExpDate | 17 | 220215 | Tarih biçimi, YYAAGG'dir. Bu nedenle, bitiş tarihi 15 Şubat 2022'dir. |

Daha sonra makbuz kaydedilir ve tek bir taramadan sonra ilgili veritabanı değerleri girilir.
