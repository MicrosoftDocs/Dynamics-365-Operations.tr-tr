---
title: Inventory Visibility rezervasyonları
description: Bu makalede, Stok Görünürlüğü'nü kullanarak rezervasyon oluşturmak, rezervasyonları tüketmek ve/veya belirtilen stok miktarlarının rezervasyonunu kaldırmak için rezervasyon özelliğinin nasıl ayarlanacağı açıklanmaktadır.
author: yufeihuang
ms.date: 11/04/2022
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yufeihuang
ms.search.validFrom: 2021-08-02
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: 0ae0589f8bac7ebf9b43cf0f3bc02680d324b29b
ms.sourcegitcommit: 49f8973f0e121eac563876d50bfff00c55344360
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/14/2022
ms.locfileid: "9762754"
---
# <a name="inventory-visibility-reservations"></a>Inventory Visibility rezervasyonları

[!include [banner](../includes/banner.md)]

Bu makalede, geçici rezervasyonlar için tipik bir kullanım örneği anlatılmakta ve Stok Görünürlüğünde bunların nasıl ayarlanacağı açıklanmaktadır. Geçici rezervasyonların nasıl oluşturulacağı, fiziksel tüketim sırasında nasıl denkleştirileceği ve belirtilen stok miktarlarının nasıl ayarlanacağı veya rezervasyonun nasıl kaldırılacağı hakkında bilgiler içerir.

## <a name="sample-use-case-for-soft-reservation"></a>Geçici rezervasyon için örnek kullanım örneği

Geçici rezervasyonlar kuruluşların, özellikle sipariş karşılama süreci sırasında kullanılabilir stok için tek doğru kaynak elde etmesine yardımcı olur. Bu işlevsellik, aşağıdaki koşulların bulunduğu kuruluşlar için yararlıdır:

- Kuruluşun, doğrudan giden siparişleri alan en az iki farklı sistemi vardır.
- Kuruluş çok sıkıdır ve ürün stoğu için çift ayırmayı önlemek istemektedir; bu durum, birden fazla sistemin en son stok parçasını kapasite üzerinde rezerve edebildiği durumlarda gerçekleşir. Bu durum, tüm sipariş sistemleri stok görünürlüğü için tek bir doğru kaynak sunan Stok Görünürlüğüne anlık geçici ayırma API çağrıları yapabildiğinde önlenir.

[<img src="media/inventory-visibility-soft-reservation.png" alt="Inventory Visibility soft reservation." title="Stok Görünürlüğü geçici ayırma" width="720" />](media/inventory-visibility-soft-reservation.png)

Önceki şekil, geçici rezervasyonun nasıl çalıştığını gösterir ve aşağıdaki işlemleri vurgular:

- Başlangıç stok düzeyiniz Microsoft Dynamics 365 Supply Chain Management'ın Stok Görünürlüğünde eşitlenir.
- Geçici rezervasyonlar her sipariş kanalından veya sisteminden Stok Görünürlüğüne gönderilir. Stok Görünürlüğü, stok kullanılabilirliğini doğrular ve geçici rezervasyon yapmaya çalışır. Geçici rezervasyon başarılı olursa Stok Görünürlüğü, geçici rezerve edilen miktara ekler, rezervasyon için kullanılabilir miktardan (AFR) çıkarır ve bir geçici rezervasyon kimliğiyle yanıt verir.
- Şu anda fiziksel stok miktarınız aynı kalır.
- Daha sonra, kalıcı rezervasyonlar yapmak, ambara serbest bırakmak veya nihai stok miktarını güncelleştirmek için, tek veya toplu geçici rezerve edilöiş siparişleri (sipariş satırları) Supply Chain Management'a eşitleyebilirsiniz.
- Supply Chain Management'ta fiziksel stok güncelleştirildiğinde sistemi, [geçici rezervasyonları denkleştirmek](#offset-scm) üzere ayarlayabilirsiniz.

Geçici rezervasyonlar genellikle Stok Görünürlüğü hizmeti için API çağrılarını kullanarak oluşturulur, tüketilir ve iptal edilir.

> [!NOTE]
> Stok Görünürlüğü'nü kullanarak rezerve edilen miktarı otomatik olarak denkleştirmek için isteğe bağlı olarak Supply Chain Management'ı (ve diğer üçüncü taraf sistemleri) ayarlayabilirsiniz. Denkleştirme miktarı, Stok Görünürlüğü'nün rezervasyon kayıtlarından silinir.
>
> Varsayılan olarak, geçici rezervasyon özelliğini etkinleştirdiğinizde denkleştirme işlevi otomatik olarak açılır.

## <a name="turn-on-and-set-up-the-reservation-feature"></a><a name="turn-on"></a>Rezervasyon özelliğini açma ve ayarlama

Rezervasyon özelliğini açmak için aşağıdaki adımları izleyin.

1. Power Apps'te oturum açın ve **Stok Görünürlüğü**'nü açın.
1. **Yapılandırma** sayfasını açın.
1. **Özellik Yönetimi** sekmesinde, *OnHandReservation* özelliğini açın.
1. Supply Chain Management ortamınızda oturum açın.
1. **[Özellik yönetimi](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)** çalışma alanına gidin ve *Rezervasyon denkleştirme ile Stok Görünürlüğü tümleştirmesi* özelliğini (sürüm 10.0.22 veya sonraki bir sürümü gerektirir) etkinleştirin.
1. **Stok Yönetimi \> Kurulum \> Stok Görünürlüğü tümleştirme parametreleri**'ne gidin ve **Rezervasyon denkleştirme** sekmesini açarak aşağıdaki ayarları yapın:

    - **Rezervasyon denkleştirmeyi etkinleştir**: Bu işlevi etkinleştirmek için *Evet* olarak ayarlayın.
    - **Rezervasyon denkleştirme değiştirici**: Stok Görünürlüğü'nde yapılan rezervasyonları denkleştirecek stok hareketi durumunu seçin. Bu ayar, denkleştirme işlemlerini tetikleyen sipariş işleme aşamasını belirler. Aşama, siparişin stok hareketi durumuna göre izlenir. Aşağıdaki değerlerden birini seçin:

        - *Siparişte*: *Siparişte* durumundaki siparişler oluşturulduklarında bir denkleştirme isteği gönderir. Denkleştirme miktarı, oluşturulan siparişin (satır) miktarıdır.
        - *Rezerve et*: *Rezerve et* durumundaki siparişler, siparişle rezerve edildiğinde veya fiziksel olarak rezerve edildiğinde bir denkleştirme isteği gönderir. *Rezerve et* durumunda denkleştirme yaptığınızda sipariş, rezerve edildi alında durumuna en yakın olan herhangi bir stok durumunda (örneğin al, sevk irsaliyesi gönderildi veya faturalandı) bir denkleştirme isteği gönderir. Bu davranış, Supply Chain Management'taki rezervasyonu atlayıp başka bir stok durumuna (örneğin, ambardan serbest bıraktan çek ve paketleye atladığınızda) bile oluşur. İstek yalnızca bir kez tetiklenir. Çekme sırasında tetiklenirse, sevk irsaliyesi deftere nakledildiğinde denkleştirme yinelenmez. Denkleştirme miktarı, denkleştirme tetiklendiğindeki stok işlemi durumu miktarıyla aynı olur (başka bir deyişle *Siparişle rezerve*/*Fiziksel Rezerve* veya ilgili satırdaki daha sonraki bir durum).

1. Stok Görünürlüğü uygulamasında yeniden oturum açın, **Yapılandırma** sayfasına gidin ve **Geçici Rezervasyon** sekmesinde varsayılan geçici rezervasyon hiyerarşisini gözden geçirin. Hiyerarşiye yeni boyutları gerektiği şekilde ekleyin.
1. **Geçici Rezervasyon Eşlemesi Ayarla** bölümünde, varsayılan ayarları görüntüleyin. Varsayılan olarak, geçici rezerve edilen stok miktarları `iv` veri kaynağının `softreservephysical` fiziksel ölçüsüne göre kaydedilir. *Rezerve edilebilir* hesaplanan ölçümü `availabletoreserve` ile eşlenir. `availabletoreserve` hesaplanan ölçümünü güncelleştirmek istiyorsanız, **Yapılandırma** sayfasına gidin ve ardından **Hesaplanmış Ölçüm** sekmesinde hesaplanmış ölçümü genişletip değiştirin.

Daha fazla bilgi için bkz. [Stok Görünürlüğü'nü yapılandırma](inventory-visibility-configuration.md).

> [!NOTE]
> Rezervasyon hiyerarşisi, rezervasyonlar yapıldığında belirtilmesi gereken boyutların sırasını açıklar. Bu işlem, dizin hiyerarşisinin eldeki miktar sorguları için çalıştığı şekilde çalışır ancak bağımsız olarak kullanılır ve kullanıcıların daha hassas rezervasyonlar oluşturmak için boyut ayrıntılarını belirtebilmesini sağlar.
>
> Geçici rezervasyon hiyerarşiniz, Stok Görünürlüğünün bölüm yapılandırmasını oluşturduklarından bileşen olarak `SiteId` ve `LocationId` öğelerini içermelidir.

Rezervasyonları yapılandırma hakkında daha fazla bilgi için bkz. [Rezervasyonları yapılandırma](inventory-visibility-configuration.md#reservation-configuration).

## <a name="use-the-reservation-feature-in-inventory-visibility"></a>Stok Görünürlüğü'nde rezervasyon özelliğini kullanma

Rezervasyon API'sini çağırdığınızda sistem, belirtilen mal ve miktarların rezervasyonunu işaretler.

Aşağıda örnek bir senaryo ve örnek bir API sorgusu gövdesi bulunmaktadır. Contoso şirketi, e-ticaret web sitesinden D0002 (Dolap) ürünü satar. Bir müşteri web sitesini kullanarak küçük bir kırmızı dolap için sipariş oluşturur. Contoso, aşağıdaki boyutları kullanarak bu siparişi karşılamaya karar verir:

- Kuruluş Kimliği= usmf
- Tesis = 1
- Ambar = 11
- Ürün = D0002
- Renk = kırmızı
- Boyut = küçük

Contoso, zaten kendi e-ticaret sisteminden Stok Görünürlüğüne API bağlantısı ayarlamıştır. Sipariş alındığında sistem, Stok Görünürlüğünde geçici bir rezervasyon oluşturmak amacıyla anlık olarak bir API çağrısı tetikler.

### <a name="create-soft-reservations-using-the-reservation-api"></a>Rezervsayon API'sini kullanarak geçici rezervasyonlar oluşturma

Rezervasyonlar, `/api/environment/{environmentId}/onhand/reserve` gibi hizmetin URL'sine bir POST isteği göndererek Stok Görünürlüğü hizmetinde yapılır.

Rezervasyon için istek gövdesinde bir kuruluş kimliği, ürün kimliği, rezerve edilen miktarlar ve boyutlar bulunmalıdır.

Rezervasyon API'sini çağırdığınızda istek gövdesinde Boolean `ifCheckAvailForReserv` parametresini belirterek rezervasyon doğrulamasını denetleyebilirsiniz. `True` değeri, doğrulamanın gerekli olduğu anlamına ve `False` değeri, doğrulamanın gerekli olmadığı anlamına gelir. Varsayılan değer `True` değeridir.

Rezervasyonu iptal etmek veya belirtilen stok miktarlarının rezervasyonunu kaldırmak istiyorsanız miktarı negatif bir değere ayarlayın ve doğrulamayı atlamak için `ifCheckAvailForReserv` parametresini `False` olarak ayarlayın.

Aşağıda, önceki bağlamdaki satış siparişine başvuruda bulnan bir istek gövdesi örneği yer almaktadır.

```json
# Url

#Replace {endpoint} with your system endpoint.
    {endpoint}/api/environment/{environmentId}/onhand/reserve

# Method
Post

# Header
# replace {access_token} with the one get from security service
Api-version: "1.0"
Content-Type: "application/json"
Authorization: "Bearer {access_token}"

# Body
{
    "id": "Testrequest-0005",
    "organizationId": "usmf",
    "productId": "D0002",
    "dimensions": {
        "SiteId": "1",
        "LocationId": "11",
        "ColorId": "red",
        "SizeId": "small"
    },
    "quantityDataSource": "iv",
    "modifier": "softreservphysical",
    "quantity": 1,
    "ifCheckAvailForReserv": true
}
```

Başarılı bir geçici rezervasyon isteği, her bir rezervasyon kaydı için bir *geçici rezervasyon kimliği* döndürür. Geçici rezervasyon kimliği tek bir geçici rezervasyon kaydı için benzersiz bir tanımlayıcı değildir ancak geçici rezervasyon isteğiyle ilişkili olan ürün kimliği ve boyut değerleri kombinasyonudur. Başarıyla rezerve edilen siparişleri Supply Chain Management'a veya başka bir ERP sistemine eşitlediğinizde, sipariş satırındaki geçici rezervasyon kimliğini kaydedebilirsiniz.

### <a name="offset-soft-reservations-in-supply-chain-management"></a><a name="offset-scm"></a>Supply Chain Management'ta geçici rezervasyonları denkleştirme

Geçici rezere edilen miktarı, bir siparişteki miktarı Supply Chain Management veya başka bir ERP sisteminden fiziksel olarak düşürdükten sonra denkleştirebilirsiniz. Stok Görünürlüğü, Supply Chain Management ile kullanıma hazır geçici rezervasyon denkeltirme tümleştirmesi sunar.

Geçici rezervasyonu denkleştirmek için şu adımları izleyin.

1. Supply Chain Management'ta oturun açın.
1. **Satış ve pazarlama \> Satış Siparişleri \> Tüm Satış Siparişleri**'ne gidin.
1. Eylem Bölmesinde, **Yeni**'yi seçin.
1. Harici satış siparişini yeniden oluşturun ve tam olarak aynı ürün kimliği, kuruluş, tesis, ambar ve boyut değerlerini kullanan bir satış satırı ekleyin.
1. **Satış siparişi satırları** hızlı sekmesinde yeni girdiğiniz satış satırını seçin ve ardından araççubuğunda **Stok \> Rezervasyon Kimliği**'ni seçin.
1. Şu adımlardan birini izleyin:

    - Geçici rezervasyon yanıtınızdaki geçici rezervasyon kimliğini kopyalayın ve **Rezervasyon Kimliği** alanına yapıştırın.
    - **Rezervasyon Kimliği** alanını boş bırakın ancak **Stok hizmeti otomatik denkleştirme** onay kutusunu seçin. Sistem, seçilen satıra girilen madde kimliği ve boyut değerlerini temel alarak hangi ürün ve ürün boyutlarının denkleştirileceğini otomatik olarak belirleyecektir.

1. **Tamam**'ı seçin.
1. Aynı satış satırı hala seçili durumdayken **Satış sipariş satırları** hızlı sekmesinin araç çubuğunda **Stok \> Rezervasyon**'u seçerek sipariş edilen miktarı fiziksel olarak rezerve edin.
1. **Rezervasyon denkleştirme değiştiricisi** alanını daha önce *Rezerve edildi* olarak ayarladıysanız denkleştirme, sipariş satırı durumu *Fiziksel rezerve* veya *Siparişle rezerve* olduğunda tetiklenir. Toplu iş, Supply Chain Management'tan Stok Görünürlüğüne denkleştirme isteklerini eşitlemek için bir dakika çalışır.

> [!NOTE]
> Belirli bir rezervasyon denkleştirme değiştiricisi içeren hareket durumları için hareket güncelleştirmesi, aşağıdaki tüm koşullar karşılandığında ilgili rezervasyon kaydını denkleştirir:
>
> - Stok hareketinde rezervasyon kimliği, Stok Görünürlüğü'nde rezervasyon kaydının rezervasyon kimliği ile eşleşir.
> - Stok hareketinin boyutları, Stok Görünürlüğü'nde rezervasyon kaydının boyutlarıyla eşleşir.
> - Stok hareketi durumundaki değişiklikler, stok hareketi durumu sipariş işleminin tamamlandığını veya atlandığını yansıttığında rezervasyonlar için denkleştirmeleri tetikler.

Denkleştirme miktarları, ilgili stok hareketlerinde belirtilen stok miktarlarını izler. Stok Görünürlüğü'nde rezerve edilen miktar yoksa denkleştirme gerçekleşmez.

### <a name="cancel-or-revert-a-soft-reservation"></a>Geçici rezervasyonu iptal etme veya geri alma

Orijinal sipariş satırı iptal edilir veya silinirse ve ilgili geçici rezervasyonu geri almanız gerekiyorsa API isteği gövdenizdeki ile tam olarak aynı bilgilere sahip negatif bir miktar gönderin.
