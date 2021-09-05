---
title: Stok Görünürlüğü rezervasyonları
description: Bu konuda, Stok Görünürlüğü'nü kullanarak rezervasyon oluşturmak, rezervasyonları tüketmek ve/veya belirtilen stok miktarlarının rezervasyonunu kaldırmak için rezervasyon özelliğinin nasıl ayarlanacağı açıklanmaktadır.
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
ms.openlocfilehash: 6c87018cbfbe22fbbc441a1a23aee0ac44af9ddc
ms.sourcegitcommit: b9c2798aa994e1526d1c50726f807e6335885e1a
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/13/2021
ms.locfileid: "7345161"
---
# <a name="inventory-visibility-reservations"></a>Stok Görünürlüğü rezervasyonları

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]
[!INCLUDE [cc-data-platform-banner](../../includes/cc-data-platform-banner.md)]

Bu konuda, Stok Görünürlüğü'nü kullanarak rezervasyon oluşturmak, rezervasyonları tüketmek ve/veya belirtilen stok miktarlarının rezervasyonunu kaldırmak için rezervasyon özelliğinin nasıl ayarlanacağı açıklanmaktadır.

Rezervasyonlar, gelecekte kullanılacak stok miktarını belirtir. Rezervasyon oluşturduğunuzda sistem, rezervasyon tüketilene veya rezervasyonu kaldırılana kadar diğer siparişlerin rezerve edilmesini veya rezerve edilen malların tüketilmesini engeller. Rezervasyonlar, Stok Görünürlüğü hizmeti için API çağrılarını kullanarak oluşturulur, tüketilir ve iptal edilir.

Stok Görünürlüğü'nü kullanarak rezerve edilen miktarı otomatik olarak denkleştirmek için isteğe bağlı olarak Microsoft Dynamics 365 Supply Chain Management'ı (ve diğer üçüncü taraf sistemleri) ayarlayabilirsiniz. Denkleştirme miktarı, Stok Görünürlüğü'nün rezervasyon kayıtlarından silinir.

Rezervasyon özelliğini açtığınızda Supply Chain Management otomatik olarak Stok Görünürlüğü'nü kullanarak yapılan rezervasyonları denkleştirmeye hazır hale gelir.

> [!NOTE]
> Denkleştirme işlevi için Supply Chain Management sürüm 10.0.22 veya üzeri gerekir. Stok Görünürlüğü rezervasyonlarını kullanmak isterseniz Supply Chain Management'ı sürüm 10.0.22 veya üzerine yükseltene kadar beklemenizi öneririz.

## <a name="turn-on-the-reservation-feature"></a>Rezervasyon özelliğini açma

Rezervasyon özelliğini açmak için şu adımları izleyin.

1. Power Apps'te, **Stok Görünürlüğü**'nü açın.
1. **Yapılandırma** sayfasını açın.
1. **Özellik Yönetimi** sekmesinde, *OnHandReservation* özelliğini açın.
1. Supply Chain Management'ta oturun açın.
1. **Stok Yönetimi \> Kurulum \> Stok Görünürlüğü tümleştirme parametreleri**'ne gidin.
1. **Rezervasyon denkleştirme** altında, **Rezervasyon denkleştirmeyi etkinleştir** seçeneğini *Evet* olarak ayarlayın.

## <a name="use-the-reservation-feature-in-inventory-visibility"></a>Stok Görünürlüğü'nde rezervasyon özelliğini kullanma

Rezervasyon API'sini çağırdığınızda sistem, belirtilen mal ve miktarların rezervasyonunu işaretler. Bir rezervasyon hiyerarşisi ve bu rezervasyon hiyerarşisiyle eşleşen deftere nakletme istekleri tanımlamanız gerekir. Rezervasyonlar daha sonra doğrudan rezervasyon API'sini çağırarak yapılabilir.

### <a name="configure-the-reservation-hierarchy"></a>Rezervasyon hiyerarşisini yapılandırma

Rezervasyon hiyerarşisi, rezervasyonlar yapıldığında belirtilmesi gereken boyutların sırasını açıklar. Bu, dizin hiyerarşisinin eldeki sorgular için çalıştığı şekilde çalışır.

Rezervasyon hiyerarşisi, dizin hiyerarşisinden farklı olabilir. Bu bağımsızlık, kullanıcıların daha hassas rezervasyonlar yapmak için gereksinimleri belirtmek üzere boyutları bölebilecekleri kategori yönetimi uygulamalarına olanak tanır.

Power Apps'te geçici bir rezervasyon hiyerarşisi yapılandırmak için **Yapılandırma** sayfasını açın ve ardından, **Geçici rezervasyon eşlemesi** sekmesinde boyutları ve hiyerarşi düzeylerini ekleyerek ve/veya düzenleyerek rezervasyon hiyerarşisini ayarlayın.

### <a name="call-the-reservation-api"></a>Rezervasyon API'sini çağırma

Rezervasyonlar, `/api/environment/{environment-ID}/onhand/reserve` gibi hizmetin URL'sine bir POST isteği göndererek Stok Görünürlüğü hizmetinde yapılır.

Rezervasyon için istek gövdesinde bir kuruluş kimliği, ürün kimliği, rezerve edilen miktarlar ve boyutlar bulunmalıdır. İstek, her rezervasyon kaydı için benzersiz bir rezervasyon kimliği oluşturur. Rezervasyon kaydı, ürün kimliğinin ve boyutların benzersiz birleşimini içerir.

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

> [!NOTE]
> Denkleştirme işlevi, sürüm 10.0.22 itibarıyla kullanılabilir

### <a name="set-up-the-reserve-offset-modifier"></a>Rezerve denkleştirme değiştiricisini ayarlama

Rezerve denkleştirme değiştiricisi, denkleştirmeleri tetikleyen sipariş işleme aşamasını belirler. Aşama, siparişin stok hareketi durumuna göre izlenir. Rezervasyon denkleştirme değiştiricisini ayarlamak için şu adımları izleyin.

1. **Stok Yönetimi \> Kurulum \> Stok Görünürlüğü tümleştirme parametreleri \> Rezervasyon denkleştirme**'ye gidin.
1. **Rezervasyon denkleştirme değiştiricisi** alanını, aşağıdaki değerlerden biri olarak ayarlayın:

    - *Siparişte*: *Harekette* durumu için sipariş oluşturulduğunda bir denkleştirme isteği gönderir.
    - *Rezerve edilmiş*: *Rezerve edilmiş siparişli hareket* durumu için sipariş, rezerve edildiğinde, alındığında, sevk irsaliyesi deftere nakledildiğinde veya faturalandığında bir denkleştirme isteği gönderir. İstek, belirtilen işlem gerçekleştiğinde ilk adım için yalnızca bir kez tetiklenir.

### <a name="set-up-reservation-ids"></a>Rezervasyon kimliklerini ayarlama

Rezervasyon kimliği, Stok Görünürlüğü'nde bir rezervasyon kaydını benzersiz şekilde işaretler. Supply Chain Management'ta kullanıcılar, ilgili rezervasyon kaydı için denkleştirmeyi işaretlemek üzere rezervasyonları sipariş satırlarına yerleştirir.

Supply Chain Management'ta rezervasyon kimliklerini ayarlamak için şu adımları izleyin.

1. Bir satış siparişi açın (örneğin, **Tüm satış siparişleri** sayfasından).
1. **Satış siparişi satırları** hızlı sekmesinde bir sipariş satırı seçin.
1. **Satış siparişi satırları** hızlı sekmesinde, araç çubuğunda **Satırı güncelleştir \> Stok \> Stok Görünürlüğü tümleştirmesi**'ni seçin.
1. İlgili rezervasyon kimliklerini girin.

Stok durumu değişikliği, denkleştirme değiştiricisi kurulumuyla eşleşir.
