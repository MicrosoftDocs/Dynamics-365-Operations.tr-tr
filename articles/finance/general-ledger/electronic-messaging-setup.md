---
title: Elektronik iletileri ayarlama
description: Bu konu, Elektronik iletiler (EM) işlevinin nasıl ayarlanacağı hakkında bilgi sağlar.
author: liza-golub
ms.date: 07/07/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: ''
ms.search.region: Global
ms.author: elgolu
ms.search.validFrom: 2021-06-23
ms.dyn365.ops.version: 8.0999999999999996
ms.openlocfilehash: 2b62efabfae26a6cc004604e687a49bce992d78a30f0d441aa74fa5cde70e063
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/05/2021
ms.locfileid: "6752187"
---
# <a name="set-up-electronic-messages"></a>Elektronik iletileri ayarlama

[!include [banner](../includes/banner.md)]

**Elektronik iletiler** (EM) işlevi, farklı belge türleri için farklı elektronik raporlama işlemlerini yönetmenize yardımcı olur. [Ülkeye özgü raporlama özelliklerini](electronic-messaging.md#country-specific-regulatory-features-supported-by-the-em-functionality) destekleyen bazı karmaşık senaryolarda EM işlevi, birden fazla ileti durumuna, ileti öğesi durumuna, eyleme, ek alanlara ve yürütülebilir sınıflara sahip olacak şekilde kurulur. Bu senaryolarda, veri varlıkları paketleri içe aktarmak için kullanılabilir. Bu veri paketlerini kullanıyorsanız, bunları bir tüzel kişiliğe, Veri yönetimi aracını kullanarak aktarın. Veri yönetimi aracını kullanmak hakkında daha fazla bilgi için bkz. [Veri yönetimi](../../fin-ops-core/dev-itpro/data-entities/data-entities-data-packages.md)

Bir varlık paketini içe aktarmazsanız, EM işlevini el ile ayarlayabilirsiniz. Bu durumda, aşağıdaki öğeleri ayarlamanız gerekir:

- [Numara serileri](#sequences)
- [İleti maddesi türleri](#types)
- [İleti maddesi durumları](#item)
- [İleti durumları](#statuses)
- [Ek alanlar](#additional)
- [Yürütülebilir sınıf ayrıntıları](#executable)
- [Kayıtları doldur eylemleri](#populate)
- [Web uygulamaları](#applications)
- [Web hizmeti ayarları](#settings)
- [İleti işleme eylemleri](#actions)
- [Elektronik ileti işleme](#processing)

Aşağıdaki bölümler bu öğelerin her biri hakkında daha fazla bilgi sağlar.

## <a name="number-sequences"></a><a id="sequences"></a>Numara serileri

Hem mesajlar hem de mesaj öğeleri için numara serileri ayarlayın. Numara sıraları, iletileri ve ileti öğelerini otomatik olarak numaralandırmak için kullanılır. Sayılar, iletiler ve ileti öğeleri için sistemde benzersiz kimlik tanımlayıcıları olarak atanacaktır ve kullanılacaktır. Elektronik iletiler için numara serilerini **Genel muhasebe** \> **Genel muhasebe kurulumu** \> **Genel muhasebe parametreleri**'ne giderek ayarlayabilirsiniz.

## <a name="message-item-types"></a><a id="types"></a>İleti maddesi türleri

İleti öğesi türü, elektronik iletilerde kullanılacak kayıt türlerini tanımlar. İleti öğesi türlerini **Vergi** \> **Kurulum** \> **Elektronik iletiler** \> **İleti öğesi türleri**'ne giderek ayarlayabilirsiniz.

## <a name="message-item-statuses"></a><a id="item"></a>İleti maddesi durumları

İleti öğesi durumları, ayarlamakta olduğunu işlemede ileti öğelerine uygulanacak durumları belirler. İleti öğesi durumlarını **Vergi** \> **Kurulum** \> **Elektronik iletiler** \> **İleti öğesi durumları**'na giderek ayarlayabilirsiniz.

Bir ileti öğesi durumunun **Silmeye izin ver** parametresi, bu durumdaki öğeyi **Elektronik iletiler** formu veya **Elektronik ileti öğeleri** sayfasında silmenize izin verilip verilmeyeceğini belirler.

## <a name="message-statuses"></a><a id="statuses"></a>İleti durumları

Mesaj işlemede kullanılabilir olacak mesaj durumlarını ayarlamak. İleti durumlarını **Vergi** \> **Kurulum** \> **Elektronik iletiler** \> **İleti durumları**'na giderek ayarlayabilirsiniz.

Aşağıdaki tablo **İleti durumları** sayfasındaki alanları açıklar.

| Alan adı          | Tanım |
|---------------------|-------------|
| İleti durumu      | İleti durumu için benzersiz bir ad girin. İleti durumları, herhangi bir anda elektronik iletinin durumunu karakterize etmekte kullanılır. Girdiğiniz ad **Elektronik iletiler** sayfasında ve elektronik iletilerle ilişkili bir kayıtta gösterilir. |
| Tanım         | İleti durumunun bir açıklamasını girin |
| Yanıt türü       | İleti durumu için yanıt türünü seçin. Bir işlemedeki bazı eylemler birden fazla yanıt türü üretebilir. Örnek olarak, yürütme sonucuna bağlı olarak **Web hizmeti** eylemi türü **Başarıyla tamamlandı** veya **Teknik hata** türünde yanıtlar üretebilir. Bu durumda, her iki yanıt türü için de ileti durumunu tanımlayın. Eylem türleri ve bunlarla ilişkili yanıtlar hakkında daha fazla bilgi için bu konunun ilerleyen bölümlerindeki [İleti işleme eylem türleri](#action-types) konusuna bakın. |
| İleti maddesi durumu | Bazı durumlarda, bir elektronik iletinin durumu, ilgili iletilerin durumunu etkilemesi gerekir. İleti durumuyla ilişkilendirmek için bu alanda bir ileti öğe durumu seçin. |
| Silmeye izin ver        | Kullanıcıların bu duruma sahip iletileri **Elektronik iletiler** sayfasında silebilmelerine olanak sağlamak için bu iletişim kutusunu işaretleyin. |

## <a name="additional-fields"></a><a id="additional"></a>Ek alanlar

EM işlevi, Microsoft Dynamics 365 Finance içindeki işlem tablolarından kayıtları ileti öğeleri olarak toplamanıza olanak sağlar. Bu şekilde, kayıtları raporlama için hazırlayabilir ve daha sonra raporlayabilirsiniz. Ancak, hareket tabloları bazen kayıtları raporlama gereksinimlerini karşılayan şekilde doldurmak için yeterli bilgiye sahip değildir. Bir kayıt için raporlanması gereken tüm bilgileri, ek alanlar ayarlayarak doldurabilirsiniz. Ek alanlar, hem iletiler hem de ileti öğeleri ile ilişkilendirilebilir. Ek alanları **Vergi** \> **Kurulum** \> **Elektronik iletiler** \> **Ek alanlar**'a giderek ayarlayabilirsiniz.

Aşağıdaki tablo **Ek alanlar** sayfasındaki genel alanları açıklar.

| Alan       | Tanım |
|-------------|-------------|
| Alan adı  | İşlem ile ilgili olan elektronik iletiler veya ileti öğeleri için ek alanın adını girin. Bu ad, işlemde çalışırken kullanıcı arabiriminde (UI) gösterilir. Ad, işlemle ilişkili Elektronik raporlama (ER) için de kullanılabilir. |
| Tanım | Ek alanın açıklamasını girin. |
| Kullanıcı düzenleme   | Kullanıcılar ek alanın değerini kullanıcı arabiriminden değiştirebileceklerse bu seçeneği **Evet** olarak ayarlayın. |
| Sayaç     | Ek alan elektronik iletide bir numara serisi içerecekse bu seçeneği **Evet** olarak ayarlayın. Ek alan değeri, **Elektronik raporlamayı dışa aktarma** türü eylem çalıştırıldığında otomatik olarak doldurulur. |
| Gizli      | **Elektronik iletiler** sayfasındaki veya **Elektronik ileti öğeleri** sayfasındaki Kullanıcı arabiriminde ek alanın gizlenmesi gerekiyorsa bu seçeneği **Evet** olarak ayarlayın. |

**Değerler** hızlı sekmesinde, bir ek alanın sahip olabileceği değerleri önceden tanımlayabilirsiniz. Ardından bu değerler, kullanıcıların seçmesi için sunulabilir. Bu nedenle, işlem sırasında el ile doldurulması gerekmez. Aşağıdaki tablo bu alanları açıklar.

| Alan                | Tanım |
|----------------------|-------------|
| Alan değeri          | Raporlama sırasında bir mesaj veya mesaj öğesi için kullanılmak üzere bir alan değeri girin. |
| Tanım          | Alan değerinin açıklamasını girin. |
| Hesap türü         | Bazı alan değerleri sınırlı hesap türlerine sınırlı olabilir. Aşağıdaki değerlerden birini seçin: **Tümü**, **Müşteri** veya **Satıcı**. |
| Hesap kodu         | **Müşteri** veya **Satıcı** seçeneklerini **Hesap türü** alanında seçerseniz, alan değerinin kullanımını belirli bir grup veya tabloya daha da fazla sınırlandırabilirsiniz. |
| Hesap/Grup numarası | **Müşteri** veya **Satıcı** seçeneğini **Hesap türü** alanında seçtiyseniz ve, bir grup veya tabloyu **Hesap kodu** alanında girdiyseniz, bu alana belirli bir grup veya karşıt öğe girebilirsiniz. |
| Yürürlüğe giriş            | Değerin dikkate alınması gereken başlangıç tarihini belirtin. |
| Bitiş           | Değerin dikkate alınması gereken bitiş tarihini belirtin. |

Varsayılan olarak, **Hesap/Grup numarası**, **Hesap kodu**, **Efektif** ve **Sona erme** alanları tarafından tanımlanan kriter kombinasyonları, ek alanlar için değerlerin seçimini etkilemez. Bununla birlikte, bu birleşimleri yürütülebilir bir sınıf içinde ek alanlar için değerleri hesaplar belirli mantığını gerçekleştirmek için kullanılabilir.

## <a name="executable-class-settings"></a><a id="executable"></a>Yürütülebilir sınıf ayrıntıları

Bir yürütülebilir sınıf, bir X++ yöntemidir veya elektronik mesajlaşma işleme içindeki sınıf, işlem için değerlendirmeler gerekiyorsa bir eyleme ilişkili çağrılabilir.

**Vergi** \> **Kurulum** \> **Elektronik iletiler** \> **Yürütülebilir sınıf ayarları**'na giderek, işlem sırasında çağrılması gereken bir yürütülebilir sınıfı el ile ayarlayabilirsiniz. **Yürütülebilir sınıf ayarları** sayfasında bir satır oluşturun ve aşağıdaki alanları ayarlayın.

| Alan                 | Tanım |
|-----------------------|-------------|
| Yürütülebilir sınıf      | Bu sınıfın ilişkili olarak çağrılacağı bir mesaj işleme eyleminin kurulumunda kullanılacak bir adı girin. |
| Tanım           | Yürütülebilir sınıf için bir açıklama girin. |
| Yürütülebilir sınıf adı | Bir X++ yürütülebilir sınıfı seçin. |
| Yürütme düzeyi       | Bu alan otomatik olarak ayarlanır, çünkü değer seçilen yürütülebilir sınıf için önceden belirlenmiştir. Bu alan, ilişkili değerlendirmenin yürütüleceği düzeyi sınırlar. |
| Sınıf açıklaması     | Bu alan otomatik olarak ayarlanır, çünkü değer seçilen yürütülebilir sınıf için önceden belirlenmiştir. |
| Eylem türü           | Bu alan, **\[EM\] Yürütülebilir sınıf eylem türü** özelliği **Özellik yönetimi** çalışma alanında açık olduğunda kullanılabilir. Yürütülebilir sınıfa ait eylem türünü belirtmek için bu alanı kullanın. Bu alan, **Elektronik iletiler** sayfasında elektronik ileti için kullanılabilen sonraki eylemler üzerinde daha kesin bir denetim sağlar . |

Bazı yürütülebilir sınıflar, yürütülebilir sınıf ilk defa çalıştırılmadan önce tanımlanması gereken zorunlu parametrelere sahip olabilir. Bu parametreleri tanımlamak için Eylem Bölmesinde **Parametreler** öğesini seçin. Görüntülenen iletişim kutusunda alanları ayarlayın ve **Tamam**'ı seçin. **Tamam**'ı seçmeniz önemlidir. Aksi taktirde, parametreler veritabanına kaydedilmez ve yürütülebilir sınıf doğru şekilde çağırılmaz.

## <a name="populate-records-actions"></a><a id="populate"></a>Kayıtları doldur eylemleri

Doldurulmuş kayıt eylemlerini, İleti öğeleri tablosuna kayıtlar ekleyecek eylemler oluşturmak için kullanırsınız, böylece bir elektronik iletiye eklenebilirler. Örneğin, elektronik mesajınız müşteri faturalarını raporlayacaksa, Müşteri faturası günlüğü tablosunda **Veri kaynağı** alanında bağlantılı olan Kayıtları doldur eylemini ayarlamanız gerekir.

**Vergi** \> **Kurulum** \> **Elektronik iletiler** \> **Kayıt eylemlerini doldur**'a giderek kayıtları doldurma eylemini ayarlayabilirsiniz. Tabloya kayıtlar ekleyecek her bir eylem için yeni bir kayıt oluşturun ve aşağıdaki alanları ayarlayın.

| Alan       | Tanım |
|-------------|-------------|
| Dosya Adı        | İşleminizdeki kayıtları dolduran eylem için bir ad girin. |
| Tanım | Kayıtları doldur eylemi için bir açıklama girin. |

**Veri kaynakları kurulumu** hızlı sekmesinde, işlem için kullanılacak her bir veri kaynağı için bir satır ekleyin ve aşağıdaki alanları ayarlayın.

| Alan                  | Tanım |
|------------------------|-------------|
| Dosya Adı                   | Veri kaynağı için bir ad girin. |
| İleti maddesi türü      | Veri kaynağı için kayıtlar oluşturulduğunda kullanılacak ileti öğesi türünü seçin. |
| Hesap türü           | Veri kaynağından kayıtlarla ilişkilendirilecek hesap türünü seçin. |
| Ana tablo adı      | Veri kaynağı olması gereken tabloyu seçin. |
| Belge numarası alanı  | Seçili ana tablodan belge numarasının alınacağı alanı seçin. Bu alanın değeri, ileti öğesinin **Belge numarası** alanının değeri olarak kullanılır. |
| Belge tarihi alanı    | Seçili ana tablodan belge tarihinin alınacağı alanı seçin. Bu alanın değeri, ileti öğesinin **İleti öğesi tarihi** alanının değeri olarak kullanılır. |
| Belge hesabı alanı | Seçili ana tablodan belge hesabının alınacağı alanı seçin. Bu alanın değeri, ileti öğesinin **Hesap numarası** alanının değeri olarak kullanılır. |
| Şirket                | Bu alan, **Özellik yönetimi** çalışma alanında **Kayıtları doldur eylemleri için şirketler arası sorgular** özelliği açıldığında kullanılabilir. Kayıtları doldur eylemlerine yönelik şirketler arası veri kaynakları ayarlamak için bu özelliği kullanın. Veriler birden fazla şirketten getirilebilir. |
| Kullanıcı sorgusu             | <p>Izgaranın üst kısmında **Sorguyu düzenle**'yi seçerek bir sorgu ayarlarsanız ve verilerin doldurulduğu seçili ana tabloya uygulanması gereken ölçütleri belirtirseniz, bu onay kutusu otomatik olarak seçilir. Aksi taktirde tüm kayıtlar seçilen anan tablo kaynağından doldurulur.</p><p>**Özellik yönetimi** çalışma alanında **Kayıtları doldur eylemleri için şirketler arası sorgular** özelliği açık olduğunda ve kayıtların birden fazla şirketten toplanması gerektiğinde, raporlamaya eklenmesi gereken her ek tüzel kişilik için bir satır ekleyin. Her yeni satır için **Sorguyu düzenle**'yi seçin ve satırdaki **Şirket** alanında belirtilen tüzel kişiliğe özel ilgili bir ölçüt belirtin. Bitirdiğinizde, **Veri kaynakları kurulumu** ızgarasında raporlamaya eklenmesi gereken tüm tüzel kişilikler için satırlar yer alır.</p> |

## <a name="web-applications"></a><a id="applications"></a>Web uygulamaları

Bir web uygulamasını Open Authorization (OAuth) 2.0'yi destekleyecek şekilde ayarlamak için web uygulaması ayarlarını kullanın. OAuth, kullanıcıların uygulamaya kendileri adına "güvenli temsili erişim" sağlamalarını ve bunu kimlik bilgilerine erişmeden yapmalarını sağlayan açık bir standarttır. Bir erişim kodu ve erişim belirteci alarak bir kimlik doğrulama işleminden geçebilirsiniz. **Vergi** \> **Kurulum** \> **Elektronik iletiler**\> **Web uygulamaları**'na giderek web uygulaması ayarlarını ayarlayabilirsiniz.

Aşağıdaki tablo **Web uygulamaları** sayfasındaki alanları açıklar.

| Alan                        | Tanım |
|------------------------------|-------------|
| Uygulama adı             | Web uygulaması için bir ad girin. |
| Tanım                  | Web uygulamasının açıklamasını girin. |
| Temel URL                     | Web uygulaması taban internet adresini girin. |
| Yetkilendirme URL'si yolu       | Yetkilendirme için URL oluşturmada kullanılan yolu belirtin. |
| Belirteç URL'si yolu               | Belirteç için URL oluşturmada kullanılan yolu belirtin. |
| Yeniden yönlendirme URL'si                 | Bir yönlendirme URL'si girin. |
| İstemci kodu                    | Web uygulamasının istemci kimlik kodunu girin. |
| İstemci gizli anahtarı                | Web uygulamasının istemci sırrını girin. |
| Sunucu belirteci                 | Web uygulamasının sunucu belirtecini girin. |
| Yetkilendirme biçimi eşlemesi | Yetkilendirme talebini oluşturmakta kullanılacak ER biçimini seçin. |
| Belirteç model eşlemesini içe aktar   | Erişim belirtecini depolamakta kullanılacak bir ER içe aktarma modeli eşleştirmesi seçin. |
| Verilen kapsam                | Uygulamanın taleplerinin karşılanma kapsamı. Bu alan otomatik olarak güncelleştirilir. |
| Erişim belirtecinin sona ermesine kalan süre:  | Erişim belirtecinin süresinin dolmasına kalan zaman. Bu alan otomatik olarak güncelleştirilir. | 
| Kabul Et                       | Web talebinin **Kabul** özelliğini belirtin. Örneğin, **application/vnd.hmrc.1.0+json** girin. |
| İçerik türü                 | İçerik türünü belirtin. Örneğin, **uygulama/json** girin. |

Ek olarak, aşağıdaki düğmeler **Web uygulamaları** sayfasının Eylem Panosunda, yetkilendirme sürecini desteklemek için kullanılabilir:

- **Yetkilendirme kodunu alın** - Web uygulamasının yetkilendirmesini başlatmak. Bu işlev, yetkilendirme isteği oluşturmak için **Yetkilendirme biçimi eşlemesi** alanında belirtilen ER biçimini kullanır.
- **Erişim belirteci edin** - Erişim belirteci edinme işlemini başlat.
- **Erişim belirtecini yenile** - bir erişim belirtecini yenilemek. Bu işlev, alınan erişim belirteciyle ilgili bilgileri içe aktarmak için **İçe aktarma belirteci model eşlemesi** alanında belirtilen ER biçimini kullanır.

Bir erişim belirteci, veri tabanı olan şifrelenmiş biçimde sistemde depolanan bir web uygulaması için istekleri bir web hizmeti için kullanılabilir. Güvenlik amacıyla, erişim belirtecine erişimin yalnızca bu talepleri yanıtlamasına izni olan güvenlik rollerine sınırlanması gerekir. Güvenlik grubu dışındaki bir kullanıcı bir talebi adreslemeye çalışırsa, seçilen web uygulaması aracılığıyla birlikte çalışmalarına izin verilmediğine dair bir uyarı görür. Erişim belirtecine erişimi olan güvenlik rollerini ayarlamak için **Web uygulamaları** sayfasındaki **Güvenlik rolleri** Hızlı Sekmesini kullanın. Güvenlik rolleri bir web uygulaması için tanımlanmadığında, yalnızca bir sistem yöneticisi yalnızca bu web uygulaması aracılığını kullanarak birlikte çalışabilecektir.

Seçili Web uygulamasıyla her eylem için, **Eylem günlüğü** Hızlı sekmesi kullanıcıyla ilgili bilgileri ve tarih ile saati kaydeder.

Bazı web hizmetleri isteklere farklı üst bilgiler eklenmesini gerektirebilir. Sistem yöneticisi **Tamamlayıcı üst bilgiler** hızlı sekmesinde ek üst bilgiler ve bunların değerlerini ayarlayabilir ve bunları istek oluşturma sırasında kullanabilir.

## <a name="web-service-settings"></a><a id="settings"></a>Web hizmeti ayarları

Bir web hizmetine doğrudan veri aktarımı ayarlamak için web hizmeti ayarlarını kullanın. **Vergi** \> **Kurulum** \> **Elektronik iletiler** \> **Web hizmeti ayarları**'na giderek web hizmeti ayarlarını ayarlayabilirsiniz.

Aşağıdaki tablo **Web hizmeti ayarları** sayfasındaki alanları açıklar.

| Alan                          | Tanım |
|--------------------------------|-------------|
| Web hizmeti                    | Web hizmeti için bir ad girin. |
| Tanım                    | Web hizmetinin açıklamasını girin. |
| Internet adresi               | <p>Web hizmetinin internet adresini girin. Bir web uygulaması web servisi için belirtilmişse ve web servisinin internet adresi, bu web uygulaması için tanımlanmış internet adresiyle aynı olmalıysa **Temel URL'yi kopyala**'yı seçin. Web uygulamasının temel URL'si bu alana kopyalanır.</p><p>**Uyarı:** Burada yapılandırdığınız üçüncü taraf hizmetler veya diğer hizmetler sertifika gerektirmez ve Microsoft gizlilik standartlarını karşılamayabilir. Hizmetin sağladığı uyumluluk düzeyi hakkında daha fazla bilgi edinmek için, her bir hizmetin gizlilik belgelerini gözden geçirmeniz ve her hizmet sağlayıcısıyla birlikte çalışmanız gerekir. Bu hizmetlerin güvenlik, gizlilik ve yasal standartlarınızı karşıladığından emin olmak sizin sorumluluğunuzdadır. Hizmetleri kullanma riski size aittir. Microsoft hiçbir açık garanti veya koşul vermez. Yalnızca, HTTPS gibi güvenli ve yetkilendirilmiş bağlantılar sağlayan Hizmetleri kullanmanızı öneririz.</p> |
| Sertifika                    | Önceden ayarlanmış bir Azure Key Vault sertifikasını seçin. |
| Web uygulaması                | Önceden ayarlanmış bir web uygulaması seçin. |
| Yanıt türü – XML        | Yanıt türü XML ise bu seçeneği **Evet** olarak ayarlayın. |
| İstek yöntemi                 | Talep yöntemini belirtin. HTTP, belirli bir kaynak için gerçekleştirilmesini gereken talep yöntemlerinin kümesini belirtir. Talep yöntemi **GET** **POST** veya başka bir HTTP yöntemi olabilir. |
| İstek başlıkları                | Talep başlıklarını belirtin. İstek üst bilgisi, HTTP isteğinde kullanılabilen bir HTTP üst bilgisidir. İletinin içeriğiyle ilişkili değildir. |
| Kabul Et                         | Web talebinin kabul özelliğini belirtin. |
| Kodlamayı kabul et                | Kodlamayı kabul et değerini belirtin. Kodlamayı kabul et talep HTTP başlığı, istemcinin anlayabileceği içerik kodlamasını tanıtır. Bu içerik kodlama genellikle bir sıkıştırma algoritmasıdır. |
| İçerik türü                   | İçerik türünü belirtin. İçerik türü varlık HTTP başlığı, kaynağın medya türünü belirtir. |
| Başarılı yanıt kodu       | Talebin başarılı olduğunu belirten HTTP durum kodunu belirtin. |
| İstek başlıkları biçim eşlemesi | Web talep başlıklarını oluşturmakta kullanılan ER biçimini seçin. |

## <a name="message-processing-actions"></a><a id="actions"></a>İleti işleme eylemleri

İşlemleriniz için eylemler oluşturmak için mesaj işleme eylemlerini kullanır ve parametrelerini ayarlarsınız. **Vergi** \> **Kurulum** \> **Elektronik iletiler** \> **İleti işleme eylemleri**'ne giderek ileti işleme eylemlerini ayarlayabilirsiniz.

Aşağıdaki tablo, **Mesaj işleme eylemleri** sayfasındaki alanları açıklar.

### <a name="general-fasttab"></a>Genel FastTab

| Alan                                     | Tanım |
|-------------------------------------------|-------------|
| Eylem türü                               | Eylem türünü seçin. Kullanılabilir seçenekler hakkında bilgi için bu konunun ilerleyen kısmında yer alan [Mesaj işleme eylem türleri](#action-types) bölümüne bakın. |
| Biçim eşleme                            | Eylem için çağrılması gereken ER biçimini seçin. Bu alan yalnızca **Elektronik raporlama dışa aktarma**, **Elektronik raporlama içe aktarma** ve **Elektronik raporlama dışa aktarma mesajı** türleri için kullanılabilirdir. |
| URL yolu için biçim eşlemesi               | Eylem için çağrılması gereken ER biçimini seçin. Bu biçim, seçilen web sunucusu için belirtilen temel internet adresine eklenecek URL adresinin yolunu oluşturmak için kullanılır. Bu alan yalnızca **Web servisi** türünün eylemleri için kullanılabilirdir. |
| İleti maddesi türü                         | Eylemin değerlendirileceği kayıt türlerini seçin. Bu alan **Mesaj öğesi yürütme seviyesi**, **Elektronik raporlama dışa aktarma** ve **Elektronik raporlama içe aktarma** türleri, **Web servisi** ve diğer türler için kullanılabilirdir. Bu alanı boş bırakırsanız, mesaj işleme için tanımlanan tüm mesaj öğesi türleri değerlendirilir. |
| Yürütülebilir sınıf                          | Mevcut bir yürütülebilir sınıf ayarı seçin. Bu alan, yalnızca **Mesaj öğesi yürütme düzeyi** ve **Mesaj öğesi yürütme düzeyi** yürleri için kullanılabilirdir. |
| Kayıtları doldur eylemi                   | Mevcut bir kayıt doldurma eylemini seçin. Bu alan yalnızca **Kayıtları doldur** türünün eylemleri için kullanılabilirdir. |
| Web hizmeti                               | Mevcut bir Web hizmeti seçin. Bu alan yalnızca **Web servisi** türünün eylemleri için kullanılabilirdir. |
| Dosya adı                                 | Eylemin sonucu olacak dosyanın adını belirtin. Bu dosya, web sunucusunun yanıtı veya oluşturulan rapor olabilir. Bu alan yalnızca **Web servisi** ve **Elektronik raporlama dışa aktarma iletisi** türlerinde eylemler için kullanılabilir. |
| Dosyaları kaynak belgelere ekle          | Oluşturulan dosyaları EM öğeleri için başvurulan ana tablodaki kayıtlara iliştirmek üzere bu onay kutusunu seçin. Bu alan yalnızca **Web hizmeti** ve **Elektronik raporlamayı dışa aktar** türlerindeki eylemler için kullanılabilir. |
| Dosyaları çıktı arşivinden maddelere ekleyin | Ayrı XML dosyalarını çıkış arşiv dosyasından ayıklamak ve bunları ilgili elektronik ileti öğelerine eklemek için bu onay kutusunu seçin. Bu alan yalnızca **Elektronik raporlamayı dışa aktar** türünde eylemler için kullanılabilir. |
| Dışa aktarma başına ileti maddeleri sayısı        | Tek bir dosyaya eklenmesi gereken ileti öğesi sayısı sınırını (ileti) belirtin. Bu alan yalnızca **Elektronik raporlamayı dışa aktar** türünde eylemler için kullanılabilir. |
| ER kaynağı kullan                             | İçe aktarma işlemi için ER kaynak parametrelerini kullanmak üzere bu onay kutusunu seçin. Aksi durumda, elektronik iletideki ek kullanılır. Bu alan yalnızca **Elektronik raporlamayı içe aktar** türünde eylemler için kullanılabilir. |
| İletişim kutusunu göster                               | Bir iletişim kutusunun rapor oluşturulmadan önce kullanıcıya gösterilmesi gerekiyorsa bu seçeneği **Evet** olarak işaretleyin. Bu alan yalnızca **Elektronik raporlama dışa aktarma iletisi** türünde eylemler için kullanılabilir. |

#### <a name="message-processing-action-types"></a><a id="action-types"></a>Mesaj işleme eylem türleri

Aşağıdaki seçenekler **Eylem türü** alanında kullanılabilir:

- **Mesaj oluştur** - Bu eylem türünü kullanıcıların **Elektronik mesaj** sayfasında el ile mesajlar oluşturmasına izin vermek için kullanın. Bir başlangıç durumu, bu tür bir eylem için ayarlanamaz.
- **Kayıtları doldur** – Bu eylem türünün önceden ayarlanmış olması gerekir. İşlemeye dahil edilecek eylemi etkinleştirmek için kayıt doldurma eylemiyle ilişkilendirin. Bu eylem türünün mesaj işlemede ilk eylem için kullanıldığı (elektronik ileti önden oluşturulmadıysa) veya ileti öğelerini daha önceden oluşturulmuş bir iletiye ekleyen bir eylem olarak (**İleti oluştur** türünde bir eylem) kullanıldığı varsayılır. Bu nedenle, bu türdeki eylemler için bir sonuç durumu yalnızca ileti öğeleri için ayarlanabilir. Bir başlangıç durumu yalnızca iletiler için ayarlanabilir.
- **Mesaj yürütme düzeyi** - Bu eylem türünü, mesaj düzeyinde değerlendirilecek bir yürütülebilir sınıf ayarlamak için kullanın.
- **Mesaj öğesi yürütme düzeyi** - Bu eylem türünü, mesaj öğesi düzeyinde değerlendirilecek bir yürütülebilir sınıf ayarlamak için kullanın.
- **Elektronik rapor dışa aktarma** - Bu eylem türünü, ileti öğesi düzeyinde dışa aktarılan bir ER yapılandırmasına dayanan bir rapor oluşturacak eylemler için kullanın.
- **Elektronik rapor dışa aktarma mesajı** - Bu eylem türünü, ileti öğesi düzeyinde dışa aktarılan bir ER yapılandırmasına dayanan bir rapor oluşturacak eylemler için kullanın (örneğin, bir ileti, herhangi bir ileti öğesine sahip olmadığında).
- **Elektronik rapor içe aktarma** - Bu eylem türünü, içe aktarılan bir ER yapılandırmasına dayanan bir rapor oluşturacak eylemler için kullanın.
- **Mesaj düzeyi kullanıcı işleme** -Bu eylem türünü, kullanıcı tarafından el ile bazı eylemler varsayılan eylemler için kullanın, mesaj düzeyinde. Örneğin, kullanıcı, mesajların durumunu güncelleştirebilir.
- **Kullanıcı işleme** -Bu eylem türünü, kullanıcı tarafından el ile bazı eylemler varsayılan eylemler için kullanın, mesaj öğesi düzeyinde. Örneğin, kullanıcı, mesajlar öğelerinin durumunu güncelleştirebilir.
- **Web hizmeti** - Bu eylem türünü, oluşturulan bir raporu bir web hizmetine aktarmak için kullanın. Bu eylem türü, İtalyan Satın alma ve Satış Faturası İletişimi raporlaması için kullanılmaz. Bu eylem türü için **Mesaj işleme eylemleri** sayfası bir **Muhtelif ayrıntılar** hızlı sekmesi içerir ve burada bir onay metni belirtebilirsiniz. Bu onay metni, seçilen web hizmetine istekler aktarılmadan önce kullanıcıya gösterilir.
- **Talep doğrulama** - Bu eylem türü, sunucudan bir doğrulama talep etmek için kullanın.

### <a name="initial-statuses-fasttab"></a>Başlangıç durumları FastTab

> [!NOTE]
> **İlk durumlar** FastTab'i, **Mesaj oluştur** başlangıç eylem türüne sahip eylemler için kullanılamaz.

| Alan               | Tanım |
|---------------------|-------------|
| İleti maddesi durumu | Seçilen mesaj işleme eyleminin değerlendirileceği mesaj öğesi durumunu seçin. |
| Tanım         | Seçilen mesaj öğesi durumunun açıklaması. |

### <a name="result-statuses-fasttab"></a>Sonuç durumları FastTab'i

| Alan               | Tanım |
|---------------------|-------------|
| İleti durumu      | Seçilen mesaj işleme eyleminin değerlendirileceği mesaj durumlarını seçin. Bu alan, yalnızca mesaj düzeyinde değerlendirilecek mesaj işleme eylemleri için kullanılabilir. Örneğin, **Elektronik raporlama dışa aktarma** ve **Elektronik raporlama içe aktarma** türleri eylemler için kullanılabilir ancak **Kullanıcı işleme** ve **İleti öğesi yürütme seviyesi** türleri için kullanılabilir değildir. |
| Tanım         | Seçilen mesaj durumunun açıklaması. |
| Yanıt türü       | Seçilen mesaj durumunun yanıt türü. |
| İleti maddesi durumu | Seçili mesaj işleme eylemi değerlendirildikten sonra kullanılabilir olacak sonuçlanan durumları seçin. Bu alan, yalnızca mesaj öğesi düzeyinde değerlendirilecek mesaj işleme eylemleri için kullanılabilir. Örneğin,, **Kullanıcı işleme** ve **Mesaj öğesi yürütme düzeyi** türlerinin eylemleri için kullanılabilir. Mesaj düzeyinde değerlendirilecek işleme eylemleri için bu alan, seçilen mesaj durumunda ayarlanan mesaj düzeyi durumunu gösterir. |

Aşağıdaki tablo, farklı eylem türleri ve yanıt türleri için ayarlanması gereken sonuç durumlarını gösteriri.

| Elektronik ileti eylem türü/Yanıt türü | Başarıyla yürütüldü | İş hatası | Teknik hata | Kullanıcı tanımlı | İptal et |
|----------------------------------------------|-----------------------|----------------|-----------------|--------------|--------|
| İleti oluştur                               | X                     |                |                 |              |        |
| Elektronik raporlama dışa aktarma                  | X                     |                |                 |              |        |
| Elektronik raporlama içe aktarma                  |                       |                |                 |              |        |
| Web hizmeti                                  | X                     |                | X               |              |        |
| Kullanıcı işleme                              |                       |                |                 |              |        |
| İleti yürütme düzeyi                      |                       |                |                 |              |        |
| Kayıtları doldur                             |                       |                |                 |              |        |
| İleti maddesi yürütme düzeyi                 |                       |                |                 |              |        |
| İstek doğrulaması                         | X                     | X              | X               |              |        |
| Elektronik raporlama dışa aktarma iletisi          | X                     |                |                 |              |        |
| İleti düzeyinde kullanıcı işleme                |                       |                |                 |              |        |

## <a name="electronic-message-processing"></a><a id="processing"></a>Elektronik ileti işleme

Elektronik ileti işleme, EM işlevinin temel bir kavramıdır. Elektronik mesaj için değerlendirilecek eylemleri toplar. Eylemler, bir başlangıç durumu ve bir sonuç durumu ile ilişkilendirilebilir. Alternatif olarak, **Kullanıcı işleme** türünün eylemleri bağımsız olarak başlatılabilir. Elektronik iletilerin işlenmesini ayarlamak için **Vergi** \> **Kurulum** \> **Elektronik iletiler** \> **Elektronik ileti işleme** seçeneğine gidin.

**Eylem** FastTab'i, işlemeye önceden belirlenmiş eylemler eklemenize olanak sağlar. Bir eylemin ayrı olarak mı çalıştırılacağı yoksa işleme ile mi başlatılacağını belirtebilirsiniz. İşlenme sırasındaki bir eylemin yalnızca bir kullanıcı tarafından başlatılabileceğini belirtmek için **Ayrıca çalıştır** alanına bu eylem için **Evet** olarak ayarlayın. Bir eylem, durumu eylem için başlangıç durumu olarak tanımlanan iletiler ve ileti öğeleri için başlatılacaksa, **Ayrıca çalıştır** alanını **Hayır** olarak ayarlayın. **Kullanıcı eylemi** türündeki eylemlerin her zaman ayrı çalıştırılması gerekir.

Bazen, ilk eylem ayrı çalışmak üzere ayarlanmış olsa bile, çeşitli eylemlerin tek bir sırada toplanması gerekir. Örneğin, bir kullanıcının rapor oluşturmayı başlatması gerekir. Ancak, rapor oluşturulduktan hemen sonra, bir web hizmetine gönderilir ve web hizmetinden yanıtın sisteme yansıtılması gerekir. Bu durumda, her zaman birlikte çalışması gereken eylemler için ayrılmaz bir sıralama oluşturabilirsiniz. **Eylem** hızlı sekmesinde, **Ayrılmaz sıralar**'ı kılavuzun üstünde seçin ve bir sıra oluşturun. Daha sonra, tek bir sırada birlikte çalışması gereken tüm eylemler için **Ayrılmaz sıra** alanında bir sıra seçin. Bu örnekte, **Ayrı çalıştır** alanı, sıradaki ilk eylem için **Evet** ancak diğer tüm eylem için **Hayır** olarak ayarlanabilir.

**Elektronik raporlama dışa aktarma** eylemleri ve **Elektronik raporlama dışa aktarma iletisi** türleri, giriş parametreleri içeren bir ER biçimi çalıştırır. Elektronik ileti işlemenin bu türlerden birindeki eylemler içermesi durumunda, rapor oluşturulmadan önce giriş parametrelerinin değerlerini belirtmeniz gerekir. Bu şekilde sistem, raporu oluşturmak için bir toplu iş rejimi kullanabilir. Seçili eylem türü için parametreleri ayarlamak üzere ızgaranın üzerindeki **Parametreler** öğesini seçebilirsiniz (**Elektronik raporlamayı dışa aktar** veya **Elektronik raporlamayı dışa aktar iletisi**). Toplu iş rejiminde belirtilen parametrelerle çalıştırılması gereken eylem için **Parametreleri kullan** onay kutusunu seçin.

**İleti öğesi ek alanları** hızlı sekmesini kullanarak ileti öğeleriyle ilişkili önceden belirlenmiş ek alanlar ekleyebilirsiniz. Alanın ilişkili olduğu her türde mesaj öğesi için ek alanlar eklemeniz gerekir. İşleme sırasında ek alana atanacak bir varsayılan değer belirtebilirsiniz.

**İleti ek alanları** hızlı sekmesini kullanarak iletilere önceden belirlenmiş ilişkili ek alanlar ekleyebilirsiniz. İşleme sırasında ek alana atanacak bir varsayılan değer belirtebilirsiniz.

Belirli işlemler için sistemde önceden tanımlanmış güvenlik rollerini ayarlamak için **Güvenlik rolleri** hızlı sekmesini kullanın. Belirli bir role sahip kullanıcılar yalnızca bu role tanımlanan işlemleri görür.

Toplu iş rejiminde işi işlemeyi ayarlamak için **Toplu iş** hızlı sekmesini kullanın. İşlemeyi başlatmak için eylem bölmesinde **İşlemeyi çalıştır**'ı seçtiğinizde, doğrudan **Elektronik iletiler** veya **Elektronik ileti öğeleri** sayfasında işleme için bir toplu iş rejimi ayarlamanızı öneririz.
