---
title: Elektronik mesajlaşma
description: Bu konu, Microsoft Dynamics 365 Finance içinde elektronik mesajlaşma için kurulum bilgisi ve genel bakış sağlar.
author: ShylaThompson
manager: AnnBe
ms.date: 11/16/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2018-10-28
ms.dyn365.ops.version: 8.0999999999999996
ms.openlocfilehash: b5887efc32c71759e4cb3c31e1b18c4c8b64f173
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/10/2020
ms.locfileid: "3977203"
---
# <a name="electronic-messaging"></a>Elektronik mesajlaşma

[!include [banner](../includes/banner.md)]

Bu konu, elektronik mesajlaşma için kurulum bilgisi ve genel bakış sağlar.

Yakın zamanda çeşitli ülkelerin ve bölgelerin hükümetleri ve mevzuatları, bu ülkelerde ve bölgelerde kayıtlı olan şirketler için raporlama gereksinimleri belirlemiştir. Gereksinimlerin amacı, bu şirketlerden verilerin elektronik biçimde, doğrudan tutuldukları, işlendikleri ve hesaplandıkları sistemlerden alınabilmesidir.

Finance içindeki elektronik mesajlaşma işlevi, Finance ile hükümetler ve yasama otoritelerinin resmi bilgiyi raporlama, gönderme ve alma sistemleri arasında birlikte çalışabilirliği desteklemektedir.

Elektronik mesaj işlevselliği, **Elektronik Raporlama** (ER) modülüne tümleşiktir. Bu nedenle, elektronik mesajlar için ER biçimlerini ayarlayabilirsiniz. Daha fazla bilgi için bkz: [Elektronik raporlamaya (ER) genel bakış](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/analytics/general-electronic-reporting).

Elektronik mesajlaşma aşağıdaki varlıklara bağlıdır:

- **Elektronik mesaj** – Dahili olarak raporlanması ve/veya aktarılması gereken bir rapor veya bildirim. Buna bir örnek, bir vergi dairesine gönderilen bir rapordur.
- **Elektronik mesaj öğeleri** - Raporlanan mesaja dahil edilmesi gereken kayıtlar.
- **Elektronik mesaj işleme** - Veri toplama, rapor oluşturma ve Microsoft Azure Blob depolama içerisinde veri depolama, raporları sistem dışına aktarma, sistem dışından yanıtlar alma ve alınan bilgiye dayalı olarak veritabanını güncelleştirmek için çalıştırılması gereken bir eylem zinciri. Zincirdeki eylemler bağlı olabilir veya olmayabilir.

Aşağıdaki şekil, elektronik mesajlaşma için veri akışını gösterir.

![Elektronik mesaj veri akışı](media/electronic-messaging-data-flow.png)

Elektronik mesajlar işlevi, aşağıdaki senaryoları destekler:

- Çeşitli türlerin ER biçimlerinin dışa aktarılmasıyla ilişkili mesajları ve raporları el ile oluşturma: Microsoft Excel, XML, JavaScript Object Notation (JSON), PDF, metin ve Microsoft Word.
- Bir otorite tarafından ilişkilendirilmiş bir içe aktarma ER biçimi aracılığıyla talep edilen veya alınan bilgiye dayalı mesajları otomatik olarak oluşturmak ve işleme.
- Bir veri kaynağından bilgileri mesaj öğeleri olarak toplama ve işleme. Veri kaynağı bir Finance tablosudur.
- Ek bilgiler depolama, tanımlanmış çeşitli yürütülebilir sınıfları mesajlar veya mesaj öğelerine ilişkin değerlendirme.
- Mesaj öğelerinde toplanan bilgiyi bir araya getirme, bu bilgiyi mesaj ile bölme ve ER raporlama biçimlerinde ilişkilendirilmiş raporlar oluşturma.
- Azure Anahtar Kasasında depolanan bilgiyi kullanarak oluşturulan raporları bir web hizmetine aktarmak.
- Bir web hizmetinden bir yanıt al, yanıtı yorumla ve Finance içindeki veriyi uygun biçimde güncelleştir.
- Oluşturulan tüm raporları depola ve gözden geçir.
- Bir mesaj veya mesaj öğesi için çalıştırılmış olan eylemlere ilişkin tüm kayıt bilgisini depola ve gözden geçir.
- Çeşitli mesaj durumları ve mesaj öğesi durumları ile işlemeyi kontrol et.

## <a name="set-up-electronic-messaging"></a>Elektronik mesajlaşmayı kurma

Elektronik mesajlaşma, farklı elektronik raporlama işlemlerini farklı belge türleri için korumanıza yardımcı olur. Bazı karmaşık senaryolarda elektronik mesajlaşma, birden fazla mesaj durumuna, mesaj öğesi durumuna, eyleme, ek alanlara ve yürütülebilir sınıflara sahip olmak üzere kurulur. Bu senaryolarda, veri varlıkları paketleri içe aktarmak için kullanılabilir. Bu veri paketlerini kullanıyorsanız, bunları bir tüzel kişiliğe, Veri yönetimi aracını kullanarak içe aktarmalısınız. Veri yönetimi aracını kullanmak hakkında daha fazla bilgi için bkz. [Veri yönetimi](../../dev-itpro/data-entities/data-entities-data-packages.md)

Bir varlık paketini içe aktarmazsanız, Elektronik mesajlaşma işlevselliğini el ile ayarlayabilirsiniz. Bu durumda, aşağıdaki öğeleri ayarlamanız gerekir:

- [Numara serileri](#number-sequences)
- [Mesaj öğesi türleri ve durumları](#message-item-types-and-statuses)
- [İleti durumları](#message-statuses)
- [Ek alanlar](#additional-fields)
- [Yürütülebilir sınıf ayrıntıları](#executable-class-settings)
- [Kayıtları doldur eylemleri](#populate-records-actions)
- [Web uygulamaları](#web-applications)
- [Web hizmeti ayarları](#web-service-settings)
- [İleti işleme eylemleri](#message-processing-actions)
- [Elektronik ileti işleme](#electronic-message-processing)

Aşağıdaki bölümler bu öğelerin her biri hakkında daha fazla bilgi sağlar.

### <a name="number-sequences"></a>Numara serileri

Hem mesajlar hem de mesaj öğeleri için numara serileri ayarlayın. Numara serileri iletileri ve ileti öğelerini otomatik olarak numaralandırmak için kullanılır. Sayılar, iletiler ve ileti öğeleri için sistemde benzersiz kimlik tanımlayıcıları olarak atanacaktır ve kullanılacaktır. Elektronik mesajlaşmalar için numara serilerini **Genel muhasebe parametreleri** sayfasında ayarlayabilirsiniz (**Genel muhasebe** \> **Genel muhasebe kurulumu** \> **Genel muhasebe parametreleri**).

### <a name="message-item-types-and-statuses"></a>Mesaj öğesi türleri ve durumları

Mesaj öğesi türü, elektronik mesajlarda kullanılacak kayıt türlerini tanımlar. Mesaj öğesi türlerini **Mesaj öğesi türleri** sayfasında ayarlayabilirsiniz (**Vergi** \> **Kurulum** \> **Elektronik mesajlar** \> **Mesaj öğesi türleri**).

Mesaj öğesi durumları, ayarlamakta olduğunu işlemede mesaj öğelerine uygulanacak durumları belirler. Mesaj öğesi türlerini **Mesaj öğesi durumları** sayfasında ayarlayabilirsiniz (**Vergi** \> **Kurulum** \> **Elektronik mesajlar** \> **Mesaj öğesi durumları**).

Bir ileti öğe durumunun **Silmeye izin ver** parametresi, kullanıcının bu durumdaki öğeyi **Elektronik iletiler** formu veya **Elektronik ileti öğeleri** sayfasında silmesine izin veril verilmeyeceğini belirler.

### <a name="message-statuses"></a>İleti durumları

Mesaj işlemede kullanılabilir olacak mesaj durumlarını ayarlamak. Mesaj durumlarını **Mesaj durumları** sayfasında ayarlayabilirsiniz (**Vergi** \> **Kurulum** \> **Elektronik mesajlar** \> **Mesaj durumları**).

Aşağıdaki tablo **İleti durumları** sayfasındaki alanları açıklar.

| Alan adı          | Tanım |
|---------------------|-------------|
| İleti durumu      | İleti durumu için benzersiz bir ad girin. İleti durumları, herhangi bir anda elektronik iletinin durumunu karakterize etmekte kullanılır. Girdiğiniz ad **Elektronik iletiler** sayfasında ve elektronik iletilerle ilişkili bir kayıtta gösterilir. |
| Tanım         | İleti durumunun bir açıklamasını girin |
| Yanıt türü       | İleti durumu için yanıt türünü seçin. Bir işlemedeki bazı eylemler birden fazla yanıt türü üretebilir. Örnek olarak, **Web servisi** türü eylem **Başarıyla tamamlandı** veya **Teknik hata** türü üretbilir, çalıştırılmasının sonucuna bağlı olarak. Bu durumda, her iki yanıt türü için de ileti durumları tanımlamanız gerekir. Eylem türleri ve bunlarla ilişkili yanıtlar hakkında daha fazla bilgi için bkz. [İleti işleme eylem türleri](#message-processing-action-types). |
| İleti maddesi durumu | Bazı durumlarda, bir elektronik iletinin durumu, ilgili iletilerin durumunu etkilemesi gerekir. İleti durumuyla ilişkilendirmek için bu alanda bir ileti öğe durumu seçin. |
| Silmeye izin ver        | Kullanıcıların bu duruma sahip iletileri **Elektronik iletiler** sayfasında silebilmelerine olanak sağlamak için bu iletişim kutusunu işaretleyin. |

### <a name="additional-fields"></a>Ek alanlar

Elektronik mesajlaşma işlevselliği, kayıtları bir işlem tablosundan doldurmanıza olanak sağlar. Bu şekilde, kayıtları raporlama için hazırlayabilir ve daha sonra raporlayabilirsiniz. Ancak, hareket tabloları bazen kayıtları raporlama gereksinimlerini karşılayan şekilde doldurmak için yeterli bilgiye sahip değildir. Bir kayıt için raporlanması gereken tüm bilgileri, ek alanlar ayarlayarak doldurabilirsiniz. Ek alanlar, hem mesajlar hem de mesaj öğeleri ile ilişkilendirilebilir. Ek alanları **Ek alanlar** sayfasında (**Vergi** \> **Kurum** \> **Elektronik mesajlar** \> **Ek alanlar**) ayarlayabilirsiniz.

Aşağıdaki tablo **Ek alanlar** sayfasındaki genel alanları açıklar.

| Alan       | Tanım |
|-------------|-------------|
| Alan adı  | İşlem ile ilgili olan mesaj öğeleri için ek öznitelikler için adı girin. Bu ad, işlemde çalışırken kullanıcı arabiriminde (UI) gösterilir. İşlemle ilişkili ER yapılandırmaları için de kullanılabilir. |
| Tanım | Ek alanın açıklamasını girin. |
| Kullanıcı düzenleme   | Kullanıcılar ek alanın değerini kullanıcı arabiriminden değiştirebileceklerse bu seçeneği **Evet** olarak ayarlayın. |
| Sayaç     | Ek alan elektronik iletide bir numara serisi içerecekse bu seçeneği **Evet** olarak ayarlayın. Ek alan değerninin çalıştırma sırasında eylem **Dışa aktarma elektronik Raporlama** tipi otomatik olarak doldurulur. |
| Gizli      | Ek alan kullanıcı arabiriminde gizlenecekse bu alanı **Evet** olarak ayarlayın. |

Her bir ek alan, işleme için farklı değerlere sahip olabilir. Bu değerleri, **Değerler** hızlı sekmesinde tanımlayabilirsiniz. Aşağıdaki tablo bu alanları açıklar.

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

### <a name="executable-class-settings"></a>Yürütülebilir sınıf ayrıntıları

Bir yürütülebilir sınıf, bir X++ yöntemidir veya elektronik mesajlaşma işleme içindeki sınıf, işlem için değerlendirmeler gerekiyorsa bir eyleme ilişkili çağrılabilir.

Yürütülebilir sınıfı **Yürütülebilir sınıf ayarları** (**Vergi** \> **Kurulum** \> **Elektronik mesajlar** \> **Elektronik sınıf ayarları**) sayfasında el ile ayarlayabilirsiniz. Bir satır oluşturun ve aşağıdaki alanları ayarlayın.

| Alan                 | Tanım |
|-----------------------|-------------|
| Yürütülebilir sınıf      | Bu sınıfın ilişkili olarak çağrılacağı bir mesaj işleme eyleminin kurulumunda kullanılacak bir adı girin. |
| Tanım           | Yürütülebilir sınıf için bir açıklama girin. |
| Yürütülebilir sınıf adı | Bir X++ yürütülebilir sınıfı seçin. |
| Yürütme düzeyi       | Bu alan otomatik olarak ayarlanır, çünkü değer seçilen yürütülebilir sınıf için önceden belirlenmiş olmalıdır. Bu alan, ilişkili değerlendirmenin yürütüleceği düzeyi sınırlar. |
| Sınıf açıklaması     | Bu alan otomatik olarak ayarlanır, çünkü değer seçilen yürütülebilir sınıf için önceden belirlenmiş olmalıdır. |

Bazı yürütülebilir sınıflar, yürütülebilir sınıf ilk defa çalıştırılmadan önce tanımlanması gereken zorunlu parametrelere sahip olabilir. Bu parametreler tanımlamak için **parametreler** eylem bölmesini seçin, alanları görünür kılın ve ardından seçin iletişim kutusunda ayarlanan **Tamam**. **Tamam**'ı seçmeniz önemlidir. Aksi taktirde, parametreler veritabanına kaydedilmez ve yürütülebilir sınıf doğru şekilde çağırılmaz.

### <a name="populate-records-actions"></a>Kayıtları doldur eylemleri

Doldurulmuş kayıt eylemlerini, Mesaj öğeleri tablosuna kayıtlar ekleyecek eylemler oluşturmak için kullanırsınız, böylece bir elektronik mesaja eklenebilirler. Örneğin, elektronik mesajınız müşteri faturalarını raporlayacaksa, Müşteri faturası günlüğü tablosunda **Veri kaynağı** alanında bağlantılı olan Kayıtları doldur eylemini ayarlamanız gerekir. **Kayıtları doldur eylemi** sayfasında (**Vergi** \> **Kurulum** \> **Elektronik mesajlar** \> **Kayıt eylemlerini doldur**) kayıtları doldurma eylemini ayarlayabilirsiniz. Tabloya kayıtlar ekleyecek her bir eylem için yeni bir kayıt oluşturun ve aşağıdaki alanları ayarlayın.

| Alan       | Tanım |
|-------------|-------------|
| Dosya Adı        | İşleminizdeki kayıtları dolduran eylem için bir ad girin. |
| Tanım | Kayıtları doldur eylemi için bir açıklama girin. |

**Veri kaynakları kurulumu** hızlı sekmesinde, işlem için kullanılacak her bir veri kaynağı için bir satır ekleyin ve aşağıdaki alanları ayarlayın.

| Alan                  | Tanım |
|------------------------|-------------|
| Dosya Adı                   | Veri kaynağı için bir ad girin. |
| İleti maddesi türü      | Veri kaynağı için kayıtlar oluşturulduğunda kullanılacak mesaj öğesi türünü seçin. |
| Hesap türü           | Veri kaynağından kayıtlarla ilişkilendirilecek hesap türünü seçin. |
| Ana tablo adı      | Veri kaynağı olması gereken tabloyu seçin. |
| Belge numarası alanı  | Seçili tablodan belge numarasının alınacağı alanı seçin. |
| Belge tarihi alanı    | Seçili tablodan belge tarihinin alınacağı alanı seçin. |
| Belge hesabı alanı | Seçili tablodan belge hesabının alınacağı alanı seçin. |
| Kullanıcı sorgusu             | Bu onay kutusu seçiliyse, kılavuzun üstündeki **Sorguyu düzenle**'yi seçerek bir sorgu ayarlayabilirsiniz. Aksi taktirde tüm kayıtlar seçilen veri kaynağında doldurulur. |

### <a name="web-applications"></a>Web uygulamaları

Web uygulaması ayarlarını kullanarak, Open Authorization (OAuth) 2.0 desteklemesi için bir web uygulaması ayarlayabilirsiniz. OAuth, kullanıcıların uygulamaya kendileri adına "güvenli temsili erişim" sağlamalarını ve bunu kimlik bilgilerine erişmeden yapmalarını sağlayan açık bir standarttır. Bir erişim kodu ve erişim belirteci alarak bir kimlik doğrulama işleminden geçebilirsiniz. **Web uygulamaları** sayfasında web uygulaması ayarlarını ayarlayabilirsiniz (**Vergi** \> **Kurulum** \> **Elektronik mesajlar** \> **Web uygulamaları**).

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
| Erişim belirtecinin sona ermesine kalan süre:  | Erişim belirtecinin süresinin dolmasına kalan zaman. | 
| Kabul et                       | Web talebinin **Kabul** özelliğini belirtin. Örneğin, **application/vnd.hmrc.1.0+json** girin. |
| İçerik türü                 | İçerik türünü belirtin. Örneğin, **uygulama/json** girin. |

Ek olarak, aşağıdaki düğmeler **Web uygulamaları** sayfasının Eylem Panosunda, yetkilendirme sürecini desteklemek için kullanılabilir:

- **Yetkilendirme kodunu alın** - Web uygulamasının yetkilendirmesini başlatmak.
- **Erişim belirteci edin** - Erişim belirteci edinme işlemini başlat.
- **Erişim belirtecini yenile** - bir erişim belirtecini yenilemek.

Bir erişim belirteci, veri tabanı olan şifrelenmiş biçimde sistemde depolanan bir web uygulaması için istekleri bir web hizmeti için kullanılabilir. Güvenlik amacıyla, erişim belirtecine erişimin yalnızca bu talepleri yanıtlamasına izni olan güvenlik rollerine sınırlanması gerekir. Güvenlik grubu dışındaki kullanıcılar bir talebi adreslemeye çalışırsa, seçilen web uygulaması aracılığıyla birlikte çalışmalarına izin verilmediğine dair bir uyarı görürler. Erişim belirtecine erişimi olan güvenlik rollerini ayarlamak **Güvenlik rolleri** Hızlı Sekmesini **Web uygulamaları** sayfasında kullanın. Güvenlik rolleri bir web uygulaması için tanımlanmadığında, yalnızca bir sistem yöneticisi yalnızca bu web uygulaması aracılığıyla birlikte çalışabilecektir.

### <a name="web-service-settings"></a>Web hizmeti ayarları

Bir web hizmetine doğrudan veri aktarımı ayarlamak için web hizmeti ayarlarını kullanırsınız. **Web hizmeti ayarları** sayfasında web hizmeti ayarlarını ayarlayabilirsiniz (**Vergi** \> **Kurulum** \> **Elektronik mesajlar** \> **Web hizmeti ayarları**).

Aşağıdaki tablo **Web hizmeti ayarları** sayfasındaki alanları açıklar.

| Alan                          | Tanım |
|--------------------------------|-------------|
| Web hizmeti                    | Web hizmeti için bir ad girin. |
| Tanım                    | Web hizmetinin açıklamasını girin. |
| Internet adresi               | Web hizmetinin internet adresini girin. Bir web uygulaması web servisi için belirtilmişse ve web servisinin internet adresi, bu web uygulaması için tanımlanmış internet adresiyle aynı olmalıysa, web uygulamasının taban URL'sini bu alana kopyalamak için **Taban URL'yi kopyala**'yı seçin. |
| Sertifika                    | Önceden ayarlanmış bir Key Vault sertifikasını seçin. |
| Web uygulaması                | Önceden ayarlanmış bir Key Vault sertifikasını seçin. |
| Yanıt türü – XML        | Yanıt türü XML ise bu seçeneği **Evet** olarak ayarlayın. |
| İstek yöntemi                 | Talep yöntemini belirtin. HTTP, belirli bir kaynak için gerçekleştirilmesini gereken talep yöntemlerinin kümesini belirtir. Talep yöntemi **GET** **POST** veya başka bir HTTP yöntemi olabilir. |
| İstek başlıkları                | Talep başlıklarını belirtin. Bir talep başlığı, bir HTTP talebinde kullanılabilen bir HTTP başlığıdır ve mesajın içeriğiyle ilişkili değildir. |
| Kabul et                         | Web talebinin **Kabul** özelliğini belirtin. |
| Kodlamayı kabul et                | **Kodlamayı kabul et** değerini belirt. Kodlamayı kabul et talep HTTP başlığı, istemcinin anlayabileceği içerik kodlamasını tanıtır. Bu içerik kodlama genellikle bir sıkıştırma algoritmasıdır. |
| İçerik türü                   | İçerik türünü belirtin. İçerik türü varlık HTTP başlığı, kaynağın medya türünü belirtir. |
| Başarılı yanıt kodu       | Talebin başarılı olduğunu belirten HTTP durum kodunu belirtin. |
| İstek başlıkları biçim eşlemesi | Web talep başlıklarını oluşturmakta kullanılan ER biçimini seçin. |

### <a name="message-processing-actions"></a>İleti işleme eylemleri

İşlemleriniz için eylemler oluşturmak için mesaj işleme eylemlerini kullanır ve parametrelerini ayarlarsınız. İşleme eylemlerini **Mesaj işleme eylemleri** sayfasında ayarlayabilirsiniz (**Vergi** \> **Kurulum** \> **Elektronik mesajlar** \> **Mesaj işleme eylemleri**).

Aşağıdaki tablo, **Mesaj işleme eylemleri** sayfasındaki alanları açıklar.

#### <a name="general-fasttab"></a>Genel FastTab

| Alan                       | Tanım |
|-----------------------------|-------------|
| Eylem türü                 | Eylem türünü seçin. Kullanılabilir seçenekler hakkında bilgi için [Mesaj işleme eylem türleri](#message-processing-action-types) bölümüne bakın. |
| Biçim eşleme              | Eylem için çağrılması gereken ER biçimini seçin. Bu alan yalnızca **Elektronik raporlama dışa aktarma**, **Elektronik raporlama içe aktarma** ve **Elektronik raporlama dışa aktarma mesajı** türleri için kullanılabilirdir. |
| URL yolu için biçim eşlemesi | Eylem için çağrılması gereken ER biçimini seçin. Bu alan yalnızca **Web servisi** türünün eylemleri için kullanılabilirdir. Seçilen web sunucusu için belirtilen taban internet adresine eklenecek URL adresinin yolunu oluşturmakta kullanılır. |
| İleti maddesi türü           | Eylemin değerlendirileceği kayıt türlerini seçin. Bu alan **Mesaj öğesi yürütme seviyesi**, **Elektronik raporlama dışa aktarma** ve **Elektronik raporlama içe aktarma** türleri, **Web servisi** ve bazı diğer türler için kullanılabilirdir. Bu alanı boş bırakırsanız, mesaj işleme için tanımlanan tüm mesaj öğesi türleri değerlendirilir. |
| Yürütülebilir sınıf            | Daha önceden oluşturulmuş yürütülebilir sınıf ayarlarını seçin. Bu alan, yalnızca **Mesaj öğesi yürütme düzeyi** ve **Mesaj öğesi yürütme düzeyi** yürleri için kullanılabilirdir. |
| Kayıtları doldur eylemi     | Daha önceden ayarlanmış bir kayıtları doldur eylemini seçin. Bu alan yalnızca **Kayıtları doldur** türünün eylemleri için kullanılabilirdir. |
| Web hizmeti                 | Daha önceden ayarlanmış bir web servisi seçin. Bu alan yalnızca **Web servisi** türünün eylemleri için kullanılabilirdir. |
| Dosya adı                   | Eylemin sonucu olacak dosyanın adını belirtin. Bu dosya, web sunucusunun yanıtı veya oluşturulan rapor olabilir. Bu alan yalnızca **Web servisi** ve **Elektronik raporlama dışa aktarma iletisi** türlerinde eylemler için kullanılabilir. |
| İletişim kutusunu göster                 | Bir iletişim kutusunun rapor oluşturmadan önce kullanıcıya gösterilmesi gerekiyorsa bu seçeneği **Evet** olarak işaretleyin. Bu alan yalnızca **Elektronik raporlama dışa aktarma iletisi** türünde eylemler için kullanılabilir. |

##### <a name="message-processing-action-types"></a>Mesaj işleme eylem türleri

Aşağıdaki seçenekler **Eylem türü** alanında kullanılabilir:

- **Mesaj oluştur** - Bu eylem türünü kullanıcıların **Elektronik mesaj** sayfasında el ile mesajlar oluşturmasına izin vermek için kullanın. Bir başlangıç durumu, bu tür bir eylem için ayarlanamaz.
- **Kayıtları doldur** - Bir **Kayıtları doldur** türünde bir eylemin önceden ayarlanmış olması gerekir. Bu eylem türünü bir kayıtları doldur eylem türüyle ilişkilendirerek bu eylemin işlenmeye dahil edilmesini sağlayın. Bu eylem türünün ya mesaj işlemede ilk eylem için kullanıldığı (elektronik ileti önden oluşturulmadıysa) veya ileti öğelerini daha önceden oluşturulmuş bir iletiye ekleyen bir eylem olarak (**İleti oluştur** türünde bir eylem). Bu nedenle, bu türdeki eylemler için bir sonuç durumu yalnızca ileti öğeleri için ayarlanabilir. Bir başlangıç durumu yalnızca iletiler için ayarlanabilir.
- **Mesaj yürütme düzeyi** - Bu eylem türünü, mesaj düzeyinde değerlendirilecek bir yürütülebilir sınıf ayarlamak için kullanın.
- **Mesaj öğesi yürütme düzeyi** - Bu eylem türünü, mesaj öğesi düzeyinde değerlendirilecek bir yürütülebilir sınıf ayarlamak için kullanın.
- **Elektronik rapor dışa aktarma** - Bu eylem türünü, mesaj öğesi düzeyinde dışa aktarılan bir ER yapılandırmasına dayanan bir rapor oluşturacak eylemler için kullanın.
- **Elektronik rapor dışa aktarma mesajı** - Bu eylem türünü, mesaj öğesi düzeyinde dışa aktarılan bir ER yapılandırmasına dayanan bir rapor oluşturacak eylemler için kullanın (örneğin, bir mesaj, herhangi bir mesaj öğesine sahip olmadığında).
- **Elektronik rapor içe aktarma** - Bu eylem türünü, içe aktarılan bir ER yapılandırmasına dayanan bir rapor oluşturacak eylemler için kullanın.
- **Mesaj düzeyi kullanıcı işleme** -Bu eylem türünü, kullanıcı tarafından el ile bazı eylemler varsayılan eylemler için kullanın, mesaj düzeyinde. Örneğin, kullanıcı, mesajların durumunu güncelleştirebilir.
- **Kullanıcı işleme** -Bu eylem türünü, kullanıcı tarafından el ile bazı eylemler varsayılan eylemler için kullanın, mesaj öğesi düzeyinde. Örneğin, kullanıcı, mesajlar öğelerinin durumunu güncelleştirebilir.
- **Web hizmeti** - Bu eylem türünü, oluşturulan bir raporu bir web hizmetine aktarmak için kullanın. Bu eylem türü, İtalyan Satın alma ve Satış Faturası İletişimi raporlaması için kullanılmaz. **Web servisi** türü eylemler için **Mesaj işleme eylemleri** sayfası bir **Muhtelif ayrıntılar** hızlı sekmesi içerir ve burada bir onay metni belirtebilirsiniz. Bu onay metni, seçilen web servisine talep aktarılmadan önce kullanıcıya gösterilecektir.
- **Talep doğrulama** - Bu eylem türü, sunucudan bir doğrulama talep etmek için kullanın.

#### <a name="initial-statuses-fasttab"></a>Başlangıç durumları FastTab

> [!NOTE]
> **İlk durumlar** FastTab'i, **Mesaj oluştur** başlangıç eylem türüne sahip eylemler için kullanılamaz.

| Alan               | Tanım |
|---------------------|-------------|
| İleti maddesi durumu | Seçilen mesaj işleme eyleminin değerlendirileceği mesaj öğesi durumunu seçin. |
| Tanım         | Seçilen mesaj öğesi durumunun açıklaması. |

#### <a name="result-statuses-fasttab"></a>Sonuç durumları FastTab'i

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

### <a name="electronic-message-processing"></a>Elektronik ileti işleme

Elektronik mesaj işleme, Elektronik mesaj işlevinin temel bir kavramıdır. Elektronik mesaj için değerlendirilecek eylemleri toplar. Eylemler, bir başlangıç durumu ve bir sonuç durumu ile ilişkilendirilebilir. Alternatif olarak, **Kullanıcı işleme** türünün eylemleri bağımsız olarak başlatılabilir. **Elektronik mesaj işleme** sayfasında (**Vergi** \> **Kurulum** \> **Elektronik mesajlar** \> **Elektronik mesaj işleme**), ileti düzeyinde veya ileti öğeleri düzeyinde işleme için desteklenecek ek alanlar da seçebilirsiniz.

**Eylem** FastTab'i, işlemeye önceden belirlenmiş eylemler eklemenize olanak sağlar. Bir eylemin ayrı olarak mı çalıştırılacağı yoksa işleme ile mi başlatılacağını belirtebilirsiniz. İşlenme sırasındaki bir eylemin yalnızca bir kullanıcı tarafından başlatılabileceğini belirtmek için **Ayrıca çalıştır** alanına bu eylem için **Evet** olarak ayarlayın. Bir eylem, durumu eylem için başlangıç durumu olarak tanımlanan iletiler ve ileti öğeleri için başlatılacaksa, **Ayrıca çalıştır** alanını **Hayır** olarak ayarlayın. **Kullanıcı eylemi** türündeki eylemlerin her zaman ayrı çalıştırılması gerekir.

Bazen, çeşitli eylemlerin tek bir sekansa toplanması gerekir, ilk eylem ayrı çalışmak üzere ayarlanmış olsa bile. Örneğin, bir kullanıcı rapor oluşturmayı başlatması gerekir ancak rapor oluşturulduktan hemen sonra, bir web hizmetine gönderilir ve web hizmetinden yanıtın sisteme yansıtılması gerekir. Bu durumda, her zaman birlikte çalışması gerek eylemler için ayrılmaz bir sıralama oluşturabilirsiniz. **Eylem** hızlı sekmesinde, **Ayrılmaz sıralar**'ı kılavuzun üstünde seçin ve bir sıra oluşturun. Daha sonra, birlikte çalışması gereken tüm eylemler için **Ayrılmaz sıra** alanında bir sıra seçin. Bu durumda **Ayrı çalıştır** alanı, sıradaki ilk eylem için **Evet** ancak diğer tüm eylem için **Hayır** olarak ayarlanabilir.

**Mesaj öğesi ek alanları** FastTab'i, mesaj öğeleriyle ilişkili önceden belirlenmiş ek alanlar eklemenize olanak sağlar. Alanın ilişkili olduğu her türde mesaj öğesi için ek alanlar eklemeniz gerekir.

**Mesaj ek alanları** FastTab'i, mesajlara ilişkili önceden belirlenmiş ek alanlar eklemenize olanak sağlar.

**Güvenlik rolleri** FastTab'i, belirli işlemler için sistemde önceden belirlenmiş güvenlik rolleri ayarlamanıza olanak sağlar. Belirli bir role sahip kullanıcılar yalnızca bu role tanımlanan işlemleri görür.

**Toplu iş** FastTab'i, bir toplu iş rejiminde işlemeyi ayarlamanıza olanak sağlar.

## <a name="work-with-the-electronic-messages-functionality"></a>Elektronik mesajlar işlevselliği ile çalışmak

Mesaj düzeyinde çalışıyorsanız, **Elektronik mesajlar** sayfası (**Vergi** \> **Sorgular ve raporlar** \> **Elektronik mesajlar** \> **Elektronik mesajlar**) daha yararlıdır. Veri toplama (mesaj öğesi) düzeyinde çalışıyorsanız **Elektronik mesaj öğeleri** sayfası (**Vergi** \> **Sorgular ve raporlar** \> **Elektronik mesajlar** \> **Elektronik mesaj öğeleri**) daha yararlıdır.

### <a name="electronic-messages"></a>Elektronik iletiler

**Elektronik mesajlar** sayfası, rolünüze dayalı olarak kullanabileceğiniz işlemleri sunar. Güvenlik rolleri bu işlemenin kurulumundaki işlemler ile ilişkilendirilmiştir. Kullanabileceğiniz her işleme için sayfa size bunlarla ilişkili elektronik mesajlar ve bilgiler gösterir.

**Mesajlar** FastTab'i, seçilen işleme için elektronik mesajlar gösterir. Seçilen mesajın ve önceden tanımlanmış işlemenin durumuna bağlı olarak, kılavuzun üstündeki düğmeleri kullanarak bazı eylemleri gerçekleştirebilirsiniz:

- **Yeni** - Bu düğme, **Mesaj oluştur** türünün eylemleri ile ilişkilendirilmiştir.
- **Sil** - Bu düğme, **Silmeye izin ver** onay kutusu seçili mesajın geçerli durumu için seçiliyse kullanılabilir olur.
- **Veri topla** - Bu düğme, **Kayıtları doldur** türü eylemleriyle ilişkilendirilmiştir.
- **Rapor oluştur** - Bu düğme, **Elektronik raporlama dışa aktarma mesajı**nın eylemleri ile ilişkilendirilmiştir.
- **Rapor gönder** - Bu düğme, **Web hizmeti** türünün eylemleri ile ilişkilendirilmiştir.
- **Yanıt içe aktar** - Bu düğme, **Elektronik raporlama içe aktarma** türünün eylemleriyle ilişkilendirilmiştir.
- **Güncelleştirme durumu** - Bu düğme, **Mesaj düzeyi kullanıcı işleme** türünün eylemleri ile ilişkilendirilmiştir.
- **Mesaj öğeleri** - **Elektronik mesaj öğeleri** sayfasını açın.

**Eylem günlüğü** FastTab'i, seçilen mesaj için yürütülmüş olan tüm eylemler hakkında bilgileri gösterir. Bir eylem bir hataya sebep olursa, hata hakkındaki bilgi kılavuzdaki ilgili satıra eklenir. Hata hakkındaki bilgiyi görüntülemek için kılavuzdaki satırı seçin ve sonra **Ek** düğmesini seçin (ataş simgesi), sayfanın sağ üst köşesidne bulunur.

**Mesaj ek alanları** FastTab'i işleme kurulumunda mesajlar için tanımlanmış tüm ek alanları gösterir. Ayrıca bu ek alanların değerlerini de gösterir.

**Mesaj öğeleri** FastTab'i, seçilen mesaj ile ilişkili tüm mesaj öğelerini gösterir. Seçilen mesajın öğesinin durumuna bağlı olarak, kılavuzun üstündeki düğmeleri kullanarak bazı eylemleri gerçekleştirebilirsiniz:

- **Sil** - Bu düğme, **Silmeye izin ver** onay kutusu seçili mesaj öğesinin geçerli durumu için seçiliyse kullanılabilir olur.
- **Güncelleştirme durumu** - Bu düğme, **Kullanıcı işleme** türünün eylemleri ile ilişkilendirilmiştir.
- **Orijinal belge** - Seçilen mesaj öğesi için orijinal belgeyi gösteren bir sayfa açın.

Bir ileti için halihazırda oluşturulan ve alınan tüm raporlar bu iletiye eklenmiştir. Hata hakkındaki ekleri görüntülemek için iletiyi seçin ve sonra **Ek** düğmesini seçin (ataş simgesi), sayfanın sağ üst köşesidne bulunur.

![Ek düğmesi](media/attachment-icon.png)

**Ekler** sayfası, seçilen mesaj ile ilişkili tüm ekleri gösterir. Bir dosyayı görüntülemek için soldaki listeden seçin ve sonra Eylem Panosunda **Aç** öğesini seçin.

![Aç düğmesi](media/open-button.png)

Bir mesaj için önceden çalıştırılmış belirli bir eylemle ilişkili ekleri de gözden geçirebilirsiniz. **Elektronik iletiler** sayfasında, **İletiler** Hızlı Sekmesinde mesajı seçin **Eylem günlüğü** hızlı sekmesindeki eylemi seçin ve sayfanın sağ üst köşesindeki **Ek** düğmesini seçin.

Tüm işlemi veya belirli bir eylemi Eylem Panosunda **İşlemeyi yürüt** seçeneğini işaretleyerek de çalıştırabilirsiniz.

### <a name="electronic-message-items"></a>Elektronik ileti maddeleri

**Elektronik mesaj öğeleri** sayfası, tüm mesaj öğelerini ve her bir mesaj öğesi için çalıştırılmış eylemleri sunar. Ayrıca, mesaj öğeleri için tanımlanmış ek alanları ve bu ek alanların değerlerini de gösterir.

Aşağıdaki tablo, **Mesaj öğeleri** sekmesindeki alnları açıklar.

<table>
<thead>
<tr>
<th>Alan</th>
<th>Tanım</th>
</tr>
</thead>
<tbody>
<tr>
<td>İşleniyor</td>
<td>Mesaj öğesini oluşturmak için kullanılmış olan işlemin adı.</td>
</tr>
<tr>
<td>İleti maddesi</td>
<td>Mesaj öğesinin kimlik kodu. Bu kimlik kodu otomatik olarak, <strong>Genel muhasebe parametreleri</strong> sayfasında tanımlanmış olan <strong>Mesaj öğesi</strong> numara serisine göre atanır.</td>
</tr>
<tr>
<td>İleti maddesi tarihi</td>
<td>Mesaj öğesinin oluşturulduğu tarih.</td>
</tr>
<tr>
<td>İleti maddesi türü</td>
<td>Mesaj öğesinin türü. Çeşitli mesaj öğesi türleri aynı işlem için ayarlanabilir (örneğin, <strong>Gelen faturalar</strong> ve <strong>Giden faturalar</strong>). Bu alan bir fatura Mesaj öğeleri tablosuna bir fatura eklendiğinde otomatik olarak doldurulabilir.</td>
</tr>
<tr>
<td>İleti maddesi durumu</td>
<td>Mesaj öğesinin gerçek durumu. Kullanılabilir durumlar, mesaj öğesinin türüne göre farklılık gösterir. Burada bazı örnekler verilmiştir:
<ul>
<li><strong>Doldurulan</strong> - Bir kayıt Mesaj öğeleri tablosuna eklendi.</li>
<li><strong>Değerlendirilen</strong> - Ek öznitelikler mesaj öğesi için hesaplandı.</li>
<li><strong>Bildirilen</strong> - Mesaj öğesi rapora başarıyla eklendi.</li>
<li><strong>Hariç bırakılan</strong> - Bu durum bazı mesajları dışa aktarılmadan önce bir raporun dışında bırakmanız gerekirse faydalı olabilir.</li>
</ul>
</td>
</tr>
<tr>
<td>İletim tarihi</td>
<td>Oluşturulan bir raporu otomatik olarak sistem dışına aktaran bir işleme için mesaj öğesinin aktarıldığı tarih.</td>
</tr>
<tr>
<td>Belge numarası</td>
<td>Bu alan otomatik olarak, kayıtları doldur eyleminin kurulumuna dayalı olarak oluşturulur. Bu alan bir fatura Mesaj öğeleri tablosuna bir fatura eklendiğinde otomatik olarak doldurulabilir.</td>
</tr>
<tr>
<td>Hesap numarası</td>
<td>Bir müşteri veya satıcının hesap numarası (veya başka bir alan değeri, Kayıtları doldur eyleminde tanımlanmış olan alana dayanarak). Bu alan bir fatura Mesaj öğeleri tablosuna bir fatura eklendiğinde otomatik olarak doldurulabilir.</td>
</tr>
<tr>
<td>İleti</td>
<td>Mesajın numarası. Bu numara otomatik olarak, <strong>Genel muhasebe parametreleri</strong> sayfasında tanımlanmış olan <strong>Mesaj</strong> numara serisine göre atanır.</td>
</tr>
<tr>
<td>İleti durumu</td>
<td>Elektronik mesajın gerçek durumu.</td>
</tr>
<tr>
<td>Sonraki eylem</td>
<td>Mesaj öğesinin geçerli durumu için başlatılabilecek sonraki eylemler.</td>
</tr>
</tbody>
</table>

**Ek alanlar** sekmesi, seçilen mesaj öğesi için ek alanları ve bunların değerlerini gösterir.

#### <a name="run-processing"></a>İşlemeyi başlat

Eylem Panosu üzerinde **İşlemeyi yürüt** öğesini seçerek mesaj öğeleri için işlemeyi çalıştırın. Belirli bir eylemi yürütmek için **İşlemeyi çalıştır** iletişim kutusunda, **Eylemi seç** seçeneğini **Evet** olarak ayarlayın ve sonra bir eylem seçin. Tüm işlemeyi çalıştırmak için **Eylem seç** seçeneğini **Hayır** olarak ayarlayın.

#### <a name="generate-report"></a>Rapor oluştur

Bir rapor oluşturmak için **Rapor oluştur** öğesini Eylem Panosunda seçin. Bu düğme, **Elektronik raporlama dışa aktarma** türünün eylemleri ile ilişkilendirilmiştir.

#### <a name="update-status"></a>Güncelleştirme durumu

**Durumu güncelleştir** öğesini Eylem Panosu üzerinde seçerek bir veya birden fazla mesaj öğesinin durmunu güncelleştirin. **Durumu güncelleştir** iletişim kutusunda, güncelleştirilerek mesaj öğelerini seçmek için **Dahil edilecek kayıtlar** FastTab'i kullanın. Seçim kriterini doğru tanımladığınızdan emin olun çünkü mesaj öğesi durumları bu kriterler, seçilen eylemin başlangıç durumu ve belirttiğiniz **Yeni durum** değeri doğrultusunda güncelleştirilecektir. Bir durum güncelleştirmesi tamamlandıktan sonra, hangi öğelerin güncelleştirildiğini belirlemek güç olacaktır. Bu nedenle, durum güncelleştirmesini geri almak zor olacaktır.

#### <a name="electronic-messages"></a>Elektronik iletiler

Seçilen mesaj öğesi ile ilişkili bir elektronik mesajı görüntülemek için Eylem Panosunda **Elektronik mesajlar** öğesini seçin.

Belirli bir ileti öğesine ilişkin özel tüm dosyaları da gözden geçirebilirsiniz. Mesaj öğesinin **Mesaj** alanını seçin veya Eylem Panosunda **Elektronik mesajlar** öğesini seçin. Daha sonra, **Elektronik mesaj** sayfasında, dosyalarının gözden geçileceği iletiyi seçin ve **Ek** düğmesini (ataş simgesi), sayfanın sağ üst köşesinden seçin.

![Ek düğmesi](media/attachment-icon.png)

**Ekler** sayfası, mesaj ile ilişkili tüm ekleri gösterir. Bir dosyayı görüntülemek için soldaki listeden seçin ve sonra Eylem Panosunda **Aç** öğesini seçin.

![Aç düğmesi](media/open-button.png)

#### <a name="original-document"></a>Özgün belge

Seçilen mesaj öğesi için orijinal belgeyi açmak için Eylem Panosunda **Orijinal belge** öğesini seçin.

## <a name="example-set-up-and-run-processing-to-call-a-simple-er-exporting-format-to-generate-an-excel-report"></a>Örnek: Basit bir ER dışa aktarma biçimini, bir Excel raporu oluşturmak için ayarlayın ve çağırın.

ER biçiminizi oluşturduktan, veri kaynaklarına eşleştirdikten ve tamamladıktan sonra, bunu **Elektronik raporlama** çalışma alanını kullanarak çalıştırabilirsiniz. Bir rapor oluşturulur ve yerel olarak kaydedebilirsiniz.

Raporlama işleminin aşağıdaki yönlerini kontrol etmek için, elektronik mesajlaşma işlemesini ayarlamanız gerekir:

- Raporu kimin oluşturduğuna dair günlük bilgisi.
- Raporun ne zaman oluşturulduğunda dair günlük bilgisi.
- Önceki dönemler için oluşturulmuş raporları kaydet.

Bu bölüm, Excel için bir dışa aktarma ER biçimine dayanan bir rapor oluşturmak için elektronik mesajlaşmayı nasıl kurabileceğinize dair bir örnek gösterir. Bu örneği takip etmek istiyorsanız, ER Excel dışa aktarma biçiminin halihazırda oluşturulmuş, veri kaynaklarına eşleştirilmiş ve tamamlanmış olması gerekir. Ek olarak, bir numara serisinin elektronik iletiler için zaten ayarlanmış olması gerekir.

İşleme kurduğunuzda, ilk önce ayarlanacak işleme eylemlerini ve durumlarını tanımlamanız yararlıdır. Aşağıdaki çizim, bu örnekte işlemenin nasıl göründüğünü göstermektedir.

![İşleme düzeni](media/processing-scheme.png)

#### <a name="create-message-statuses"></a>Mesaj durumları oluşturmak

1. **Vergi \> Kurulum \> Elektronik mesajlaşma \> Mesaj durumları**'na gidin.
2. Aşağıdaki mesaj durumlarını oluşturun:

    - Yeni
    - Hazırlandı
    - Oluşturuldu

    ![İleti durumları](media/message-statuses.png)

3. **Yeni** durum satırında, **Silmeye izin ver** onay kutusunu seçerek kullanıcıların bu duruma sahip mesajları silmesine izin verin.

#### <a name="create-additional-fields"></a>Ek alanlar oluştur

1. **Vergi \> Kurulum \> Elektronik mesajlaşma \> Ek alanlar**'a gidin.
2. Başka bir alanı ve değerlerini ekleyin. Aşağıda bir örnek verilmiştir.

    ![Ek alanlar](media/additional-fields.png)

3. **Kullanıcı düzenlemesi** seçeneğini **Evet** olarak ayarlayarak kullanıcıların alanı düzenlemesine izin verin.

#### <a name="create-message-processing-actions"></a>Mesaj işleme eylemleri oluşturun

Bu örnek için, aşağıdaki eylemleri oluşturacaksınız:

- **İleti oluştur**
- **Hazırlanmışa Güncelleştir**
- **Rapor oluştur**
- **Başlangıç durumuna güncelleştir** (isteğe bağlı)

1. **Vergi \> Kurulum \> Elektronik mesajlaşma \> Mesaj işleme eylemleri**'ne gidin.
2. **Mesaj oluştur** olarak adlandırılmış bir eylem oluşturun. **Genel** FastTab'i üzerinde, **Eylem türü** alanında **Mesaj oluştur**'u seçin.
3. **Hazırlanmışa Güncelleştir** olarak adlandırılmış olan bir eylem oluşturun ve aşağıdaki alanları ayarlayın:

    - **Genel** FastTab'i üzerinde, **Eylem türü** alanında **Mesaj düzeyi kullanıcı işleme**'yi seçin.
    - **Başlangıç durumlar** FastTab'inde, **Mesaj durumu** alanında, **Yeni**'yi seçin.
    - **Sonuç durumları** FastTab'inde, **Mesaj durumu** alanında, **Hazırlanmış**'ı seçin. **Yanıt türü** alanında, **Başarıyla yürütüldü** girin.

4. **Rapor oluştur** olarak adlandırılmış olan bir eylem oluşturun ve aşağıdaki alanları ayarlayın:

    - **Genel** FastTab'i üzerinde, **Eylem türü** alanında **Elektronik raporlama dışa aktarma**'yı seçin. **Biçim eşleştirme** alanında, ER biçimi dışa aktarmayı seçin. Seçenekler **Excel**, **XML**, **JSON**, **Metin** ve **Diğer**'dir.
    - **Başlangıç durumları** FastTab'inde, **Mesaj durumu** alanında, **Hazırlanmış**'ı seçin.
    - **Sonuç durumları** FastTab'inde, **Mesaj durumu** alanında, **Oluşturuldu**'yu seçin. **Yanıt türü** alanında, **Başarıyla yürütüldü** girin.

    ![Rapor eylemi oluştur](media/generate-report-action.png)

5. İsteğe bağlı: Kullanıcıların bir raporu birden fazla kez yeniden oluşturmasına izin vermek için **Başlangıç durumuna güncelleştir** eylemi oluşturun ve aşağıdaki alanları ayarların:

    - **Genel** FastTab'i üzerinde, **Eylem türü** alanında **Mesaj düzeyi kullanıcı işleme**'yi seçin.
    - **Başlangıç durumları** FastTab'inde, **Mesaj durumu** alanında, **Oluşturuldu**'yu seçin.
    - **Sonuç durumlar** hızlı sekmesinde, iki ileti durumunun her biri için ayrı bir satır ekleyin (**Hazırlandı** ve **Yeni**). Her iki satır için, **Yanıt türü** alanını **Başarıyla yürütüldü** olarak ayarlayın.

#### <a name="electronic-message-processing"></a>Elektronik ileti işleme

Bu örnekte, tüm eylemler ayrı yürütülebilecek şekilde ayarlanmış olmalıdır. Varsayım, her kullanıcının her eylemi başlatacağıdır.

1. **Vergi \> Kurulum \> Elektronik mesajlaşma \> Elektronik mesaj işleme**'ye gidin.
2. İşlemeni için bir kayıt girin, tüm önceden tanımlanmış eylemleri ekleyin ve bir ek alan ekleyin.
3. İsteğe bağlı: **Güvenlik rolleri** FastTab'inde, belirli raporlamalara erişimi kısıtlamak için güvenlik rollerini tanımlayın.
4. **Vergi \> Sorgular ve raporlar \> Elektronik mesajlar \> Elektronik mesajlar**'a gidin.
5. Bir mesaj oluşturmak için **Yeni**'yi seçin. Bu noktada, tarihler ve bir açıklama ekleyebilirsiniz. Ayrıca, ihtiyaç duyarsanız ek alanların değerlerini de güncelleştirebilirsiniz.

    ![Bir elektronik mesaj oluşturmak](media/create-electronic-message.png)

**Eylem günlüğü** FastTab'i üzerindeki kılavuz, mesaj üzerinde gerçekleştirilmiş olan tüm eylemlerin bir kaydı ile otomatik olarak doldurulur.

Şimdi mesaj durumunu silebilir veya güncelleştirebilirsiniz. Mesaj durumunu güncelleştirmek için **Durumu güncelleştir**'i seçin. **Yeni durum** alanında, **Hazırlanmış**'ı seçin ve sonra **Tamam**'ı seçin.

![Mesaj durumunu güncelleştirmek](media/update-status.png)

Mesaj durumu **Hazırlanmış** olarak güncelleştirilir ve şimdi raporu **Rapor oluştur**'u seçerek oluşturabilirsiniz. Rapor oluşturulur ve mesaj durumu ve eylem günlüğü güncelleştirilir. Oluşturulan raporu görüntülemek için **Ek** düğmesini seçin, sayfanın sağ üst köşesinde bulunan (ataş simgesi).
