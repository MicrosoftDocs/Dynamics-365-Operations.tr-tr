---
title: Inventory Visibility rezervasyonları
description: Bu makalede, Stok Görünürlüğü'nü kullanarak rezervasyon oluşturmak, rezervasyonları tüketmek ve/veya belirtilen stok miktarlarının rezervasyonunu kaldırmak için rezervasyon özelliğinin nasıl ayarlanacağı açıklanmaktadır.
author: yufeihuang
ms.date: 08/02/2021
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yufeihuang
ms.search.validFrom: 2021-08-02
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: 3b74907709ab97ddf4cc829dba324df213ca229f
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8895742"
---
# <a name="inventory-visibility-reservations"></a>Inventory Visibility rezervasyonları

[!include [banner](../includes/banner.md)]


Bu makalede, Stok Görünürlüğü'nü kullanarak rezervasyon oluşturmak, rezervasyonları tüketmek ve/veya belirtilen stok miktarlarının rezervasyonunu kaldırmak için rezervasyon özelliğinin nasıl ayarlanacağı açıklanmaktadır.

Rezervasyonlar, gelecekte kullanılacak stok miktarını belirtir. Rezervasyon oluşturduğunuzda sistem, rezervasyon tüketilene veya rezervasyonu kaldırılana kadar diğer siparişlerin rezerve edilmesini veya rezerve edilen malların tüketilmesini engeller. Rezervasyonlar, Stok Görünürlüğü hizmeti için API çağrılarını kullanarak oluşturulur, tüketilir ve iptal edilir.

Stok Görünürlüğü'nü kullanarak rezerve edilen miktarı otomatik olarak denkleştirmek için isteğe bağlı olarak Microsoft Dynamics 365 Supply Chain Management'ı (ve diğer üçüncü taraf sistemleri) ayarlayabilirsiniz. Denkleştirme miktarı, Stok Görünürlüğü'nün rezervasyon kayıtlarından silinir.

Rezervasyon özelliğini açtığınızda Supply Chain Management otomatik olarak Stok Görünürlüğü'nü kullanarak yapılan rezervasyonları denkleştirmeye hazır hale gelir.

## <a name="turn-on-and-set-up-the-reservation-feature"></a><a name="turn-on"></a>Rezervasyon özelliğini açma ve ayarlama

Rezervasyon özelliğini açmak için aşağıdaki adımları izleyin.

1. Power Apps'te oturum açın ve **Stok Görünürlüğü**'nü açın.
1. **Yapılandırma** sayfasını açın.
1. **Özellik Yönetimi** sekmesinde, *OnHandReservation* özelliğini açın.
1. Supply Chain Management'ta oturun açın.
1. **[Özellik yönetimi](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)** çalışma alanına gidin ve *Rezervasyon denkleştirme ile Stok Görünürlüğü tümleştirmesi* özelliğini (sürüm 10.0.22 veya sonraki bir sürümü gerektirir) etkinleştirin.
1. **Stok Yönetimi \> Kurulum \> Stok Görünürlüğü tümleştirme parametreleri**'ne gidin ve **Rezervasyon denkleştirme** sekmesini açarak aşağıdaki ayarları yapın:
    - **Rezervasyon denkleştirmeyi etkinleştir**: Bu işlevi etkinleştirmek için *Evet* olarak ayarlayın.
    - **Rezervasyon denkleştirme değiştirici**: Stok Görünürlüğü'nde yapılan rezervasyonları denkleştirecek stok hareketi durumunu seçin. Bu ayar, denkleştirme işlemlerini tetikleyen sipariş işleme aşamasını belirler. Aşama, siparişin stok hareketi durumuna göre izlenir. Aşağıdakilerden birini seçin:
        - *Siparişte*: *Harekette* durumu için sipariş oluşturulduğunda bir denkleştirme isteği gönderir. Denkleştirme miktarı, oluşturulan siparişin miktarıdır.
        - *Rezerve edilmiş*: *Rezerve edilmiş siparişli hareket* durumu için sipariş, rezerve edildiğinde, alındığında, sevk irsaliyesi deftere nakledildiğinde veya faturalandığında bir denkleştirme isteği gönderir. İstek, belirtilen işlem gerçekleştiğinde ilk adım için yalnızca bir kez tetiklenir. Denkleştirme miktarı, ilgili sipariş satırında stok hareketi durumunun *Siparişte* yerine *Siparişli rezerve miktar* (veya sonraki durum) olarak değiştirildiği miktardır.

## <a name="use-the-reservation-feature-in-inventory-visibility"></a>Stok Görünürlüğü'nde rezervasyon özelliğini kullanma

Rezervasyon API'sini çağırdığınızda sistem, belirtilen mal ve miktarların rezervasyonunu işaretler. Bir rezervasyon hiyerarşisi ve bu rezervasyon hiyerarşisiyle eşleşen deftere nakletme istekleri tanımlamanız gerekir. Rezervasyonlar daha sonra doğrudan rezervasyon API'sini çağırarak yapılabilir.

### <a name="configure-the-reservation-hierarchy"></a>Rezervasyon hiyerarşisini yapılandırma

Rezervasyon hiyerarşisi, rezervasyonlar yapıldığında belirtilmesi gereken boyutların sırasını açıklar. Bu, dizin hiyerarşisinin eldeki sorgular için çalıştığı şekilde çalışır.

Rezervasyon hiyerarşisi, dizin hiyerarşisinden farklı olabilir. Bu bağımsızlık, kullanıcıların daha hassas rezervasyonlar yapmak için gereksinimleri belirtmek üzere boyutları bölebilecekleri kategori yönetimi uygulamalarına olanak tanır.

Power Apps'te geçici bir rezervasyon hiyerarşisi yapılandırmak için **Yapılandırma** sayfasını açın ve ardından **Geçici rezervasyon hiyerarşisi** sekmesinde boyutları ve hiyerarşi düzeylerini ekleyerek ve/veya düzenleyerek rezervasyon hiyerarşisini ayarlayın.

Geçici rezervasyon hiyerarşiniz, bölüm yapılandırmasını oluşturduklarından bileşen olarak `SiteId` ve `LocationId` öğelerini içermelidir.

Rezervasyonları yapılandırma hakkında daha fazla bilgi için bkz. [Rezervasyonları yapılandırma](inventory-visibility-configuration.md#reservation-configuration).

### <a name="call-the-reservation-api"></a>Rezervasyon API'sini çağırma

Rezervasyonlar, `/api/environment/{environment-ID}/onhand/reserve` gibi hizmetin URL'sine bir POST isteği göndererek Stok Görünürlüğü hizmetinde yapılır.

Rezervasyon için istek gövdesinde bir kuruluş kimliği, ürün kimliği, rezerve edilen miktarlar ve boyutlar bulunmalıdır. İstek, her rezervasyon kaydı için benzersiz bir rezervasyon kimliği oluşturur. Rezervasyon kaydı, ürün kimliğinin ve boyutların benzersiz birleşimini içerir.

Rezervasyon API'sini çağırdığınızda istek gövdesinde Boolean `ifCheckAvailForReserv` parametresini belirterek rezervasyon doğrulamasını denetleyebilirsiniz. `True` değeri, doğrulamanın gerekli olduğu anlamına ve `False` değeri, doğrulamanın gerekli olmadığı anlamına gelir. Varsayılan değer `True` değeridir.

Rezervasyonu iptal etmek veya belirtilen stok miktarlarının rezervasyonunu kaldırmak istiyorsanız miktarı negatif bir değere ayarlayın ve doğrulamayı atlamak için `ifCheckAvailForReserv` parametresini `False` olarak ayarlayın.

Aşağıda, referans olarak bir istek gövdesi örneği bulunmaktadır.

```json
# Url
# replace {RegionShortName} and {EnvironmentId} with your value
https://inventoryservice.{RegionShortName}-il301.gateway.prod.island.powerapps.com/api/environment/{EnvironmentId}/onhand/reserve

# Method
Post

# Header
# replace {access_token} with the one get from security service
Api-version: "1.0"
Content-Type: "application/json"
Authorization: "Bearer {access_token}"

# Body
{
    "id": "id-bike-0001",
    "organizationId": "usmf",
    "productId": "Bike",
    "dimensions": {
        "SiteId": "1",
        "LocationId": "11",
        "ColorId": "Red",
        "SizeId": "small"
    },
    "quantityDataSource": "iv",
    "modifier": "SoftReservOrdered",
    "quantity": 1,
    "ifCheckAvailForReserv": true
}
```

## <a name="offset-reservations-in-supply-chain-management"></a>Supply Chain Management'ta rezervasyonları denkleştirme

Belirli bir rezervasyon denkleştirme değiştiricisi içeren stok hareketi durumları için hareket güncelleştirmesi, aşağıdaki tüm koşullar karşılandığında ilgili rezervasyon kaydını denkleştirir:

- Stok hareketinde rezervasyon kimliği, Stok Görünürlüğü hizmetinde rezervasyon kaydının rezervasyon kimliği ile eşleşir.
- Stok hareketinin boyutları, Stok Görünürlüğü hizmetinde rezervasyon kaydının boyutlarıyla aynıdır.
- Stok hareketi durumundaki değişiklikler, stok hareketi durumu sipariş işleminin tamamlandığını veya atlandığını yansıttığında rezervasyonlar için denkleştirmeleri tetikler.

Denkleştirme miktarı, stok hareketlerinde belirtilen stok miktarını izler. Stok Görünürlüğü hizmetinde rezerve edilen miktar yoksa denkleştirme gerçekleşmez.

### <a name="set-up-the-reservation-offset-modifier"></a>Rezervasyon denkleştirme değiştiriciyi ayarlama

Daha önce yapmadıysanız rezervasyon değiştiriciyi [Rezervasyon özelliğini açma ve ayarlama](#turn-on) bölümünde açıklandığı gibi ayarlayın.

### <a name="set-up-reservation-ids"></a>Rezervasyon kimliklerini ayarlama

Rezervasyon kimliği, Stok Görünürlüğü'nde bir rezervasyon kaydını benzersiz şekilde işaretler. Supply Chain Management'ta kullanıcılar, ilgili rezervasyon kaydı için denkleştirmeyi işaretlemek üzere rezervasyonları sipariş satırlarına yerleştirir.

Supply Chain Management'ta rezervasyon kimliklerini ayarlamak için aşağıdaki adımları izleyin.

1. Bir satış siparişi açın (örneğin, **Tüm satış siparişleri** sayfasından).
1. **Satış siparişi satırları** hızlı sekmesinde bir sipariş satırı seçin.
1. **Satış siparişi satırları** hızlı sekmesinde, araç çubuğunda **Satırı güncelleştir \> Stok \> Stok Görünürlüğü tümleştirmesi**'ni seçin.
1. İlgili rezervasyon kimliklerini girin.

Stok durumu değişikliği, denkleştirme değiştiricisi kurulumuyla eşleşir.
