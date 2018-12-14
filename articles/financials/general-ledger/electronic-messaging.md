---
title: "Elektronik mesajlaşma"
description: "Bu konu Microsoft Dynamics 365 for Finance and Operations içinde elektronik mesajlaşmaya genel bakış ve kurulum bilgisi sağlar."
author: ShylaThompson
manager: AnnBe
ms.date: 11/16/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2018-10-28
ms.dyn365.ops.version: 8.1
ms.translationtype: HT
ms.sourcegitcommit: 232398a6c4193d0074881e26fff361deb9784bf2
ms.openlocfilehash: 082ad886f40a52457900523f44158da3ed939458
ms.contentlocale: tr-tr
ms.lasthandoff: 12/04/2018

---

# <a name="electronic-messaging"></a>Elektronik mesajlaşma

[!include [banner](../includes/banner.md)]

Bu konu Microsoft Dynamics 365 for Finance and Operations içinde elektronik mesajlaşmaya genel bakış ve kurulum bilgisi sağlar.

Yakın zamanda çeşitli ülkelerin ve bölgelerin hükümetleri ve mevzuatları, bu ülkelerde ve bölgelerde kayıtlı olan şirketler için raporlama gereksinimleri belirlemiştir. Gereksinimlerin amacı, bu şirketlerden verilerin elektronik biçimde, doğrudan tutuldukları, işlendikleri ve hesaplandıkları sistemlerden alınabilmesidir.

Finance and Operations içindeki elektronik mesajlaşma işlevi, Finance and Operations ile hükümetler ve yasama otoritelerinin resmi bilgiyi raporlama, gönderme ve alma sistemleri arasında birlikte çalışabilirliği desteklemektedir.

Elektronik mesaj işlevselliği, **Elektronik Raporlama** (ER) modülüne tümleşiktir. Bu nedenle, elektronik mesajlar için ER biçimlerini ayarlayabilirsiniz. Daha fazla bilgi için bkz: [Elektronik raporlamaya (ER) genel bakış](https://docs.microsoft.com/en-us/dynamics365/unified-operations/dev-itpro/analytics/general-electronic-reporting).

Elektronik mesajlaşma aşağıdaki varlıklara bağlıdır:

- **Elektronik mesaj** – Dahili olarak raporlanması ve/veya aktarılması gereken bir rapor veya bildirim. Buna bir örnek, bir vergi dairesine gönderilen bir rapordur.
- **Elektronik mesaj öğeleri** - Raporlanan mesaja dahil edilmesi gereken kayıtlar.
- **Elektronik mesaj işleme** - Veri toplama, rapor oluşturma ve Microsoft Azure Blob depolama içerisinde veri depolama, raporları sistem dışına aktarma, sistem dışından yanıtlar alma ve alınan bilgiye dayalı olarak veritabanını güncelleştirmek için çalıştırılması gereken, bağlı veya bağlı olmayan bir eylem zinciri.

Aşağıdaki şekil, elektronik mesajlaşma için veri akışını gösterir.

![Elektronik mesaj veri akışı](media/electronic-messaging-data-flow.png)

Elektronik mesajlar işlevi, aşağıdaki senaryoları destekler:

- Çeşitli türlerin ER biçimlerinin dışa aktarılmasıyla ilişkili mesajları ve raporları el ile oluşturma: Microsoft Excel, XML, JavaScript Object Notation (JSON), PDF, metin ve Microsoft Word.
- Bir otorite tarafından ilişkilendirilmiş bir içe aktarma ER biçimi aracılığıyla talep edilen veya elde edilen bilgiye dayalı mesajları otomatik olarak oluşturmak ve işleme.
- Bir veri kaynağından (Finance and Operations tablosu) bilgileri mesaj öğeleri olarak toplama ve işleme.
- Ek bilgiler depolama, tanımlanmış çeşitli yürütülebilir sınıfları mesajlar veya mesaj öğelerine ilişkin değerlendirme.
- Mesaj öğelerinde toplanan bilgiyi bir araya getirme, bu bilgiyi mesaj ile bölme ve ER raporlama biçimlerinde ilişkilendirilmiş raporlar oluşturma.
- Azure Anahtar Kasasında depolanan bilgiyi kullanarak oluşturulan raporları bir web hizmetine aktarmak.
- Bir web hizmetinden bir yanıt al, yanıtı yorumla ve Finance and Operations içindeki veriyi uygun biçimde güncelleştir.
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
- [Web hizmeti ayarları](#web-service-settings)
- [İleti işleme eylemleri](#message-processing-actions)
- [Elektronik ileti işleme](#electronic-message-processing)

Aşağıdaki bölümler bu öğelerin her biri hakkında daha fazla bilgi sağlar.

### <a name="number-sequences"></a>Numara serileri

Hem mesajlar hem de mesaj öğeleri için numara serileri ayarlayın. Numara serileri, mesajları ve mesaj öğelerini otomatik olarak numaralandırmak için kullanılır ve atanan numaralar, sistem içerisinde mesajlar ve mesaj öğeleri için benzersiz tanımlayıcılar olarak kullanılır. Elektronik mesajlaşmalar için numara serilerini **Genel muhasebe parametreleri** sayfasında ayarlayabilirsiniz (**Genel muhasebe** \> **Genel muhasebe kurulumu** \> **Genel muhasebe parametreleri**).

### <a name="message-item-types-and-statuses"></a>Mesaj öğesi türleri ve durumları

Mesaj öğesi türü, elektronik mesajlarda kullanılacak kayıt türlerini tanımlar. Mesaj öğesi türlerini **Mesaj öğesi türleri** sayfasında ayarlayabilirsiniz (**Vergi** \> **Kurulum** \> **Elektronik mesajlar** \> **Mesaj öğesi türleri**).

Mesaj öğesi durumları, ayarlamakta olduğunu işlemede mesaj öğelerine uygulanacak durumları belirler. Mesaj öğesi türlerini **Mesaj öğesi durumları** sayfasında ayarlayabilirsiniz (**Vergi** \> **Kurulum** \> **Elektronik mesajlar** \> **Mesaj öğesi durumları**).

### <a name="message-statuses"></a>İleti durumları

Mesaj işlemede kullanılabilir olacak mesaj durumlarını ayarlamak. Mesaj durumlarını **Mesaj durumları** sayfasında ayarlayabilirsiniz (**Vergi** \> **Kurulum** \> **Elektronik mesajlar** \> **Mesaj durumları**).

### <a name="additional-fields"></a>Ek alanlar

Elektronik mesajlaşma işlevselliği, kayıtları bir işlem tablosundan doldurmanıza olanak sağlar. Bu şekilde, kayıtları raporlama için hazırlayabilir ve daha sonra raporlayabilirsiniz. Bazı durumlarda, rapor gereksinimlerine uygun biçimde bir kaydı raporlamak için işlem tablosunda yeterli bilgi olmayabilir. Bir kayıt için raporlanması gereken tüm bilgileri, ek alanlar ayarlayarak doldurabilirsiniz. Ek alanlar, hem mesajlar hem de mesaj öğeleri ile ilişkilendirilebilir. Ek alanları **Ek alanlar** sayfasında (**Vergi** \> **Kurum** \> **Elektronik mesajlar** \> **Ek alanlar**) ayarlayabilirsiniz.

Aşağıdaki tablo **Ek alanlar** sayfasındaki alanları açıklar.

| Alan                | Tanım |
|----------------------|-------------|
| Alan adı           | İşlem ile ilgili olan mesaj öğeleri için ek öznitelikler için adı girin. Bu ad, işlemde çalışırken kullanıcı arabiriminde gösterilir. İşlemle ilişkili ER yapılandırmaları için de kullanılabilir. |
| Tanım          | İşlem ile ilgili olan mesaj öğeleri için ek öznitelikler için bir açıklama girin. |
| Alan değeri          | Raporlama sırasında bir mesaj ile ilişkili kullanılmak üzere bir alan değeri girin. |
| Alan açıklaması    | Raporlama sırasında bir mesaj ile ilişkili kullanılmak üzere bir alan değerinin açıklamasını girin. |
| Hesap türü         | Bazı ek alanların değerleri sınırlı hesap türlerine sınırlı olabilir. Aşağıdaki değerlerden birini seçin: **Tümü**, **Müşteri** veya **Satıcı**. |
| Hesap kodu         | **Müşteri** veya **Satıcı** seçeneklerini **Hesap türü** alanında seçerseniz, alan değerlerinin kullanımını belirli bir grup veya tabloya daha da fazla sınırlandırabilirsiniz. |
| Hesap/Grup numarası | **Müşteri** veya **Satıcı** seçeneğini **Hesap türü** alanında seçtiyseniz ve, bir grup veya tabloyu **Hesap kodu** alanında girdiyseniz, bu alana belirli bir grup veya karşıt öğe girebilirsiniz. |
| Yürürlüğe giriş            | Değerin dikkate alınması gereken başlangıç tarihini belirtin. |
| Bitiş           | Değerin dikkate alınması gereken bitiş tarihini belirtin. |

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

### <a name="populate-records-actions"></a>Kayıtları doldur eylemleri

Doldurulmuş kayıt eylemlerini, Mesaj öğeleri tablosuna kayıtlar ekleyecek eylemler oluşturmak için kullanırsınız, böylece bir elektronik mesaja eklenebilirler. Örneğin, elektronik mesajınız müşteri faturalarını raporlayacaksa, **Müşteri faturası günlüğü** tablosunda (**Veri kaynağı** alanında) bağlantılı olan **Kayıtları doldur** eylemini ayarlamanız gerekir. **Kayıtları doldur eylemi** sayfasında (**Vergi** \> **Kurulum** \> **Elektronik mesajlar** \> **Kayıt eylemlerini doldur**) kayıtları doldurma eylemini ayarlayabilirsiniz. Tabloya kayıtlar ekleyecek her bir eylem için yeni bir kayıt oluşturun ve aşağıdaki alanları ayarlayın.

| Alan       | Tanım                                                               |
|-------------|---------------------------------------------------------------------------|
| Dosya Adı        | İşleminizdeki kayıtları dolduran eylem için bir ad girin.       |
| Tanım | İşleminizdeki kayıtları dolduran eylem için bir açıklama girin. |

**Veri kaynakları kurulumu** hızlı sekmesinde, işlem için kullanılacak her bir veri kaynağı için bir satır ekleyin ve aşağıdaki alanları ayarlayın.

| Alan                  | Tanım |
|------------------------|-------------|
| Dosya Adı                   | Veri kaynağı için bir ad girin. |
| İleti maddesi türü      | Veri kaynağı için kayıtlar oluşturulduğunda kullanılacak mesaj öğesi türünü seçin. |
| Hesap türü           | Veri kaynağından kayıtlarla ilişkilendirilecek hesap türünü seçin. |
| Ana tablo adı      | Finance and Operations içerisinde bir veri kaynağı olacak tabloyu seçin. |
| Belge numarası alanı  | Seçili tablodan belge numarasının alınacağı alanı seçin. |
| Belge tarihi alanı    | Seçili tablodan belge tarihinin alınacağı alanı seçin. |
| Belge hesabı alanı | Seçili tablodan belge hesabının alınacağı alanı seçin. |
| Kullanıcı sorgusu             | Bu onay kutusu seçiliyse, kılavuzun üstündeki **Sorguyu düzenle**'yi seçerek bir sorgu ayarlayabilirsiniz. Aksi taktirde, tüm kayıtlar veri kaynağından doldurulur. |

### <a name="web-service-settings"></a>Web hizmeti ayarları

Bir web hizmetine doğrudan veri aktarımı ayarlamak için web hizmeti ayarlarını kullanırsınız. **Web hizmeti ayarları** sayfasında web hizmeti ayarlarını ayarlayabilirsiniz (**Vergi** \> **Kurulum** \> **Elektronik mesajlar** \> **Web hizmeti ayarları**).

Aşağıdaki tablo **Web hizmeti ayarları** sayfasındaki alanları açıklar.

| Alan                   | Tanım |
|-------------------------|-------------|
| Web hizmeti             | Web hizmeti için bir ad girin. |
| Tanım             | Web hizmetinin açıklamasını girin. |
| Internet adresi        | Web hizmetinin internet adresini girin. |
| Sertifika             | Önceden ayarlanmış bir Key Vault sertifikasını seçin. |
| Yanıt türü – XML | Yanıt türü XML ise bu seçeneği **Evet** olarak ayarlayın. |
| İstek yöntemi          | Talep yöntemini belirtin. HTTP, belirli bir kaynak için gerçekleştirilmesini gereken talep yöntemlerinin kümesini belirtir. Yöntem **GET** **POST** veya başka bir HTTP yöntemi olabilir. |
| İstek başlıkları         | Talep başlıklarını belirtin. Bir talep başlığı, bir HTTP talebinde kullanılabilen bir HTTP başlığıdır ve mesajın içeriğiyle ilişkili değildir. |
| Kodlamayı kabul et         | Kodlamayı kabul et'i belirtin. Kodlamayı kabul et talep HTTP başlığı, istemcinin anlayabileceği içerik kodlamasını tanıtır. Bu içerik kodlama genellikle bir sıkıştırma algoritmasıdır. |
| İçerik türü            | İçerik türünü belirtin. İçerik türü varlık başlığı, kaynağın medya türünü belirtir. |

### <a name="message-processing-actions"></a>İleti işleme eylemleri

İşlemleriniz için eylemler oluşturmak için mesaj işleme eylemlerini kullanır ve parametrelerini ayarlarsınız. İşleme eylemlerini **Mesaj işleme eylemleri** sayfasında ayarlayabilirsiniz (**Vergi** \> **Kurulum** \> **Elektronik mesajlar** \> **Mesaj işleme eylemleri**).

Aşağıdaki tablo, **Mesaj işleme eylemleri** sayfasındaki alanları açıklar.

#### <a name="general-fasttab"></a>Genel FastTab

| Alan                   | Tanım |
|-------------------------|-------------|
| Eylem türü             | Eylem türünü seçin. Kullanılabilir seçenekler hakkında bilgi için [Mesaj işleme eylem türleri](#message-processing-action-types) bölümüne bakın. |
| Biçim eşleme          | Eylem için çağrılması gereken ER biçimini seçin. Bu alan yalnızca **Elektronik raporlama dışa aktarma**, **Elektronik raporlama içe aktarma** ve **Elektronik raporlama dışa aktarma mesajı** türleri için kullanılabilirdir. |
| İleti maddesi türü       | Eylemin değerlendirileceği kayıt türlerini seçin. Bu alan **Mesaj öğesi yürütme seviyesi**, **Elektronik raporlama dışa aktarma** ve **Elektronik raporlama içe aktarma** türleri ve bazı diğer türler için kullanılabilirdir. Bu alanı boş bırakırsanız, mesaj işleme için tanımlanan tüm mesaj öğesi türleri değerlendirilir. |
| Yürütülebilir sınıf        | Daha önceden oluşturulmuş yürütülebilir sınıf ayarlarını seçin. Bu alan, yalnızca **Mesaj öğesi yürütme düzeyi** ve **Mesaj öğesi yürütme düzeyi** yürleri için kullanılabilirdir. |
| Kayıtları doldur eylemi | Daha önceden ayarlanmış bir kayıtları doldur eylemini seçin. Bu alan yalnızca **Kayıtları doldur** türünün eylemleri için kullanılabilirdir. |

##### <a name="message-processing-action-types"></a>Mesaj işleme eylem türleri

Aşağıdaki seçenekler **Eylem türü** alanında kullanılabilir:

- **Kayıtları doldur** - Bir **Kayıtları doldur** eyleminin önceden ayarlanmış olması gerekir. İşlemeye dahil edilmesi için **Kayıtları doldur** türünün eylemleri ile ilişkilendirin. Bu eylem türünün, mesaj işlemedeki ilk eylem için kullanılacağı varsayılır. Bu nedenle, yalnızca sonuç durumları bu tür bir eylem için ayarlanabilir. Bir başlangıç durumu ayarlanamaz.
- **Mesaj oluştur** - Bu türü kullanıcıların **Elektronik mesaj** sayfasında el ile mesajlar oluşturmasına izn vermek için kullanın. Bir başlangıç durumu, bu tür bir eylem için ayarlanamaz.
- **Mesaj yürütme düzeyi** - Bu türü, mesaj düzeyinde değerlendirilecek bir yürütülebilir sınıf ayarlamak için kullanın.
- **Mesaj öğesi yürütme düzeyi** - Bu türü, mesaj öğesi düzeyinde değerlendirilecek bir yürütülebilir sınıf ayarlamak için kullanın.
- **Elektronik rapor dışa aktarma** - Bu türü, mesaj öğesi düzeyinde dışa aktarılan bir ER yapılandırmasına dayanan bir rapor oluşturacak eylemler için kullanın.
- **Elektronik rapor dışa aktarma mesajı** - Bu türü, mesaj öğesi düzeyinde dışa aktarılan bir ER yapılandırmasına dayanan bir rapor oluşturacak eylemler için kullanın (örneğin, bir mesaj, herhangi bir mesaj öğesine sahip olmadığında).
- **Elektronik rapor içe aktarma** - Bu türü, içe aktarılan bir ER yapılandırmasına dayanan bir rapor oluşturacak eylemler için kullanın.
- **Mesaj düzeyi kullanıcı işleme** -Bu türü, kullanıcı tarafından el ile bazı eylemler varsayılan eylemler için kullanın. Örneğin, kullanıcı, mesajların durumunu güncelleştirebilir.
- **Kullanıcı işleme** -Bu türü, kullanıcı tarafından el ile bazı eylem varsayılan eylemler için kullanın. Örneğin, kullanıcı, mesajlar öğelerinin durumunu güncelleştirebilir.
- **Web hizmeti** - Bu türü, oluşturulan bir raporu bir web hizmetine aktarmak için kullanın. Bu eylem türü, İtalyan Satın alma ve Satış Faturası İletişimi raporlaması için kullanılmaz.
- **Talep doğrulama** - Bu türü, sunucudan bir doğrulama talep etmek için kullanın.

#### <a name="initial-statuses-fasttab"></a>Başlangıç durumları FastTab

> [!NOTE]
> **İlk durumlar** FastTab'i, **Kayıtları doldur** veya **Mesaj oluştur** başlangıç türüne sahip eylemler için kullanılamaz.

| Alan               | Tanım                                                                                         |
|---------------------|-----------------------------------------------------------------------------------------------------|
| İleti maddesi durumu | Seçilen mesaj işleme eyleminin değerlendirileceği mesaj öğesi durumunu seçin. |
| Tanım         | Seçilen mesaj öğesi durumunun açıklaması.                                                  |

#### <a name="result-statuses-fasttab"></a>Sonuç durumları FastTab'i

| Alan               | Tanım |
|---------------------|-------------|
| İleti durumu      | Seçilen mesaj işleme eyleminin değerlendirileceği mesaj durumlarını seçin. Bu alan, yalnızca mesaj düzeyinde değerlendirilecek mesaj işleme eylemleri için kullanılabilir. Örneğini, **Elektronik raporlama dışa aktarma** ve **Elektronik raporlama içe aktarma** türlerinin eylemleri için kullanılabilir. **Kullanıcı işleme** ve **Mesaj öğesi çalıştırma düzeyi** türlerinin eylemleri için kullanılamaz. |
| Tanım         | Seçilen mesaj durumunun açıklaması. |
| Yanıt türü       | Seçilen mesaj durumunun yanıt türü. |
| İleti maddesi durumu | Seçili mesaj işleme eylemi değerlendirildikten sonra kullanılabilir olacak sonuçlanan durumları seçin. Bu alan, yalnızca mesaj öğesi düzeyinde değerlendirilecek mesaj işleme eylemleri için kullanılabilir. Örneğin,, **Kullanıcı işleme** ve **Mesaj öğesi yürütme düzeyi** türlerinin eylemleri için kullanılabilir. Mesaj düzeyinde değerlendirilecek işleme eylemleri için bu alan, seçilen mesaj durumunda ayarlanan mesaj düzeyi durumunu gösterir. |

### <a name="electronic-message-processing"></a>Elektronik ileti işleme

Elektronik mesaj işleme, Elektronik mesaj işlevinin temel bir kavramıdır. Elektronik mesaj için değerlendirilecek eylemleri toplar. Eylemler, bir başlangıç durumu ve bir sonuç durumu ile ilişkilendirilebilir. Alternatif olarak, **Kullanıcı işleme** türünün eylemleri bağımsız olarak başlatılabilir. **Elektronik mesaj işleme** sayfasında (**Vergi** \> **Kurulum** \> **Elektronik mesajlar** \> **Elektronik mesaj işleme**), işleme için desteklenecek ek alanlar da seçebilirsiniz.

**Eylem** FastTab'i, işlemeye önceden belirlenmiş eylemler eklemenize olanak sağlar. Bir eylemin ayrı olarak mı çalıştırılacağı yoksa işleme ile mi başlatılacağını belirtebilirsiniz. (Kullanıcı eylemlerinin ayrı çalıştırılması gerekir.)

**Mesaj öğesi ek alanları** FastTab'i, mesaj öğeleriyle ilişkili önceden belirlenmiş ek alanlar eklemenize olanak sağlar. Alanın ilişkili olduğu her türde mesaj öğesi için ek alanlar eklemeniz gerekir.

**Mesaj ek alanları** FastTab'i, mesajlara ilişkili önceden belirlenmiş ek alanlar eklemenize olanak sağlar.

**Güvenlik rolleri** FastTab'i, belirli işlemler için sistemde önceden belirlenmiş güvenlik rolleri ayarlamanıza olanak sağlar. Belirli bir role sahip kullanıcılar yalnızca bu role tanımlanan işlemleri görür.

**Toplu iş** FastTab'i, bir toplu iş rejiminde işlemeyi ayarlamanıza olanak sağlar.

## <a name="work-with-electronic-messages-functionality"></a>Elektronik mesajlar işlevselliği ile çalışmak

Mesaj düzeyinde çalışıyorsanız, **Elektronik mesajlar** sayfası (**Vergi** \> **Sorgular ve raporlar** \> **Elektronik mesajlar** \> **Elektronik mesajlar**) daha yararlıdır. Veri toplama (mesaj öğesi) düzeyinde çalışıyorsanız **Elektronik mesaj öğeleri** sayfası (**Vergi** \> **Sorgular ve raporlar** \> **Elektronik mesajlar** \> **Elektronik mesaj öğeleri**) daha yararlıdır.

### <a name="electronic-messages"></a>Elektronik iletiler

**Elektronik mesajlar** sayfası, rolünüze dayalı olarak kullanabileceğiniz işlemleri sunar. Güvenlik rolleri bu işlemenin kurulumundaki işlemler ile ilişkilendirilmiştir. Kullanabileceğiniz her işleme için sayfa size bunlarla ilişkili elektronik mesajlar ve bilgiler gösterir.

**Mesajlar** FastTab'i, seçilen işleme için elektronik mesajlar gösterir. Seçilen mesajın ve önceden tanımlanmış işlemenin durumuna bağlı olarak, kılavuzun üstündeki düğmeleri seçerek bazı eylemleri gerçekleştirebilirsiniz:

- **Yeni** - Bu düğme, **Mesaj oluştur** türünün eylemleri ile ilişkilendirilmiştir.
- **Sil** - Bu düğme, **Silmeye izin ver** onay kutusu seçili mesajın geçerli durumu için seçiliyse kullanılabilir olur.
- **Rapor oluştur** - Bu düğme, **Elektronik raporlama dışa aktarma mesajı**nın eylemleri ile ilişkilendirilmiştir.
- **Rapor gönder** - Bu düğme, **Web hizmeti** türünün eylemleri ile ilişkilendirilmiştir.
- **Güncelleştirme durumu** - Bu düğme, **Mesaj düzeyi kullanıcı işleme** türünün eylemleri ile ilişkilendirilmiştir.
- **Mesaj öğeleri** - **Elektronik mesaj öğeleri** sayfasını açın.

**Eylem günlüğü** FastTab'i, seçilen mesaj için yürütülmüş olan tüm eylemler hakkında bilgileri gösterir.

**Mesaj ek alanları** FastTab'i işleme kurulumunda mesajlar için tanımlanmış tüm ek alanları gösterir. Ayrıca bu ek alanların değerlerini de gösterir.

**Mesaj öğeleri** FastTab'i, seçilen mesaj ile ilişkili tüm mesaj öğelerini gösterir.

Seçili iletinin tüm eklerini gözden geçirebilirsiniz. Bu ekler, halihazırda oluşturulmuş ve alınmış olan raporlardır. Eklerini görüntülemek istediğiniz mesajı seçin ve sonra Eylem Panosunda **Ek** düğmesine basın.

![Ek düğmesi](media/attachment-icon.png)

**Ekler** sayfası, mesaj ile ilişkili tüm ekleri gösterir. Bir dosyayı görüntülemek için soldaki listeden seçin ve sonra Eylem Panosunda **Aç** öğesini seçin.

![Aç düğmesi](media/open-button.png)

Bir mesaj için daha önce yürütülmüş belirli bir eylem ile ilişkili bir eki gözden geçirmek için **Elektronik mesajlar** sayfasında mesajı seçin ve sonra **Eylem günlüğü** FastTab'inde eylemi seçin. Daha sonra **Ek** düğmesini Eylem Panosunda seçin.

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
<td>Bir müşteri veya satıcının hesap numarası (veya başka bir alan değeri, <strong>Kayıtları doldur</strong> eyleminde tanımlanmış olan alana dayanarak). Bu alan bir fatura Mesaj öğeleri tablosuna bir fatura eklendiğinde otomatik olarak doldurulabilir.</td>
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

**Durumu güncelleştir** öğesini Eylem Panosu üzerinde seçerek bir veya birden fazla mesaj öğesinin durmunu güncelleştirin. **Durumu güncelleştir** iletişim kutusunda, güncelleştirilerek mesaj öğelerini seçmek için **Dahil edilecek kayıtlar** FastTab'i kullanın. Seçim kriterini doğru tanımladığınızdan emin olun çünkü mesaj öğesi durumları bu kriterler, seçilen eylemin başlangıç durumu ve ayarladığınız **Yeni durum** değeri doğrultusunda güncelleştirilecektir. Bir durum güncelleştirmesi tamamlandıktan sonra, hangi öğelerin güncelleştirildiğini belirlemek güç olacaktır. Bu nedenle, durum güncelleştirmelerini geri almak zor olacaktır.

#### <a name="electronic-messages"></a>Elektronik iletiler

Seçilen mesaj öğesi ile ilişkili bir elektronik mesajı görüntülemek için Eylem Panosunda **Elektronik mesaj** öğesini seçin.

Mesaj öğesine karşılık gelen tüm dosyaları gözden geçirebilirsiniz. Mesaj öğesinin **Mesaj** alanını seçin veya Eylem Panosunda **Elektronik mesaj** öğesini seçin. **Elektronik mesaj** sayfasında, raporu görüntülenecek mesajı seçin ve sonra Eylem Panosunda **Ek** düğmesini seçin.

![Ek düğmesi](media/attachment-icon.png)

**Ekler** sayfası, mesaj ile ilişkili tüm ekleri gösterir. Bir dosyayı görüntülemek için soldaki listeden seçin ve sonra Eylem Panosunda **Aç** öğesini seçin.

![Aç düğmesi](media/open-button.png)

#### <a name="original-document"></a>Özgün belge

Seçilen mesaj öğesi için orijinal belgeyi açmak için Eylem Panosunda **Orijinal belge** öğesini seçin.

## <a name="example"></a>Örnek

ER biçiminizi oluşturduktan, veri kaynaklarına eşleştirdikten ve tamamladıktan sonra, bunu **Elektronik raporlama** çalışma alanını kullanarak çalıştırabilirsiniz. Yerel olarak kaydedebileceğiniz bir rapor oluşturulur.

Raporlama işleminin aşağıdaki yönlerini kontrol etmek için, elektronik mesajlaşma işlemesini ayarlamanız gerekir:

- Raporu kimin oluşturduğuna dair günlük bilgisi.
- Rapor oluşturulduğunda günlük tut.
- Önceki dönemler için oluşturulmuş raporları kaydet.

Bu bölüm, bir raporlama işlemi oluşturmak için Elektronik mesajlar işlevselliğini nasıl ayarlayabileceğinize dair bir örnek gösterir.

### <a name="set-up-and-run-processing-to-call-a-simple-er-exporting-format-to-generate-an-excel-report"></a>Basit bir ER dışa aktarma biçimini, bir Excel raporu oluşturmak için ayarlayın ve çağırın.

Bu bölüm, Excel için bir dışa aktarma ER biçimine dayanan bir rapor oluşturmak için elektronik mesajlaşmayı nasıl kurabileceğinize dair bir örnek gösterir. Bu örneği takip etmek için, ER Excel dışa aktarma biçiminin halihazırda oluşturulmuş, veri kaynaklarına eşleştirilmiş ve tamamlanmış olması gerekir. Bir numara serisinin elektronik iletiler için zaten ayarlanmış olması gerekir.

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
    - **Sonuç durumları** FastTab'inde, **Mesaj durumu** alanında, **Hazırlanmış**'ı veya (ve) **Yeni**'yi seçin. **Yanıt türü** alanında, **Başarıyla yürütüldü** girin.

#### <a name="electronic-message-processing"></a>Elektronik ileti işleme

Bu örnekte, tüm eylemler ayrı yürütülebilecek şekilde ayarlanmış olmalıdır. Her eylemin kullanıcı tarafından başlatılacağı varsayılır.

1. **Vergi \> Kurulum \> Elektronik mesajlaşma \> Elektronik mesaj işleme**'ye gidin.
2. İşlemeni için bir kayıt girin, tüm önceden tanımlanmış eylemleri ekleyin ve bir ek alan ekleyin.
3. İsteğe bağlı: **Güvenlik rolleri** FastTab'inde, belirli raporlamalara erişimi kısıtlamak için güvenlik rollerini tanımlayın.
4. **Vergi \> Sorgular ve raporlar \> Elektronik mesajlar \> Elektronik mesajlar**'a gidin.
5. Bir mesaj oluşturmak için **Yeni**'yi seçin. Bu noktada, tarihler ve bir açıklama ekleyebilirsiniz. Ayrıca, ihtiyaç duyarsanız ek alanların değerlerini de güncelleştirebilirsiniz.

    ![Bir elektronik mesaj oluşturmak](media/create-electronic-message.png)

**Eylem günlüğü** FastTab'i üzerindeki kılavuz, mesaj üzerinde gerçekleştirilmiş olan tüm eylemlerin bir kaydı ile otomatik olarak doldurulur.

Şimdi mesaj durumunu silebilir veya güncelleştirebilirsiniz. Mesaj durumunu güncelleştirmek için **Durumu güncelleştir**'i seçin ve sonra **Yeni durum** alanında, **Hazırlanmış**'ı seçin. Daha sonra **Tamam**'ı seçin.

![Mesaj durumunu güncelleştirmek](media/update-status.png)

Mesaj durumu **Hazırlanmış** olarak güncelleştirilir ve şimdi raporu **Rapor oluştur**'u seçerek oluşturabilirsiniz. Rapor oluşturulur ve mesaj durumu ve eylem günlüğü güncelleştirilir. Oluşturulan raporu görmek için Eylem Panosu üzerinde **Ek** düğmesini seçin.

