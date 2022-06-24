---
title: Inventory Visibility stok tahsisatı
description: Bu makale, en karlı kanallarınızın veya müşterilerinizin siparişlerini karşılayabileceğinizden emin olmak için özel bir stok ayırmanıza olanak sağlayan stok tahsisatı özelliğinin nasıl ayarlanacağını ve kullanılacağını açıklar.
author: yufeihuang
ms.date: 05/27/2022
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yufeihuang
ms.search.validFrom: 2022-05-13
ms.dyn365.ops.version: 10.0.27
ms.openlocfilehash: ccc3a8c4b3d0649397b1d1f9139f7feebf39b02f
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8852519"
---
# <a name="inventory-visibility-inventory-allocation"></a>Stok Görünürlüğü stok tahsisatı

[!include [banner](../includes/banner.md)]

## <a name="business-background-and-purpose"></a>İş arka planı ve amaç

Birçok durumda üreticiler, perakendeciler ve tedarik zincirindeki diğer iş sahipleri; önemli satış kanalları, konumlar veya müşteriler için ya da belirli satış olayları için önceden stok tahsis etmelidir. Stok tahsisatı satış operasyonel planlama sürecindeki tipik bir uygulamadır ve gerçek satış aktiviteleri gerçekleşmeden ve bir satış siparişi oluşturulmadan önce yapılır.

Örneğin, bir bisiklet şirketinin çok popüler bir bisiklet için sınırlı miktarda stoğu olduğunu düşünelim. Bu şirket hem internet üzerinden hem de mağazada satış yapıyor. Şirketin, her satış kanalında bisikletin mevcut stoğunun belirli bir bölümünün kendilerine ayrılmasını talep eden birkaç önemli kurumsal iş ortağı (marketler ve büyük perakendeciler) bulunuyor. Bu nedenle, bisiklet şirketinin kanallar arasındaki stok dağılımını dengeleyebilmesi ve VIP iş ortaklarının beklentilerini yönetebilmesi gerekir. Her iki hedefe de ulaşmanın en iyi yolu, her bir kanal ve perakendecinin daha sonra tüketicilere satılmak üzere belirli miktarda tahsis edilen ürünleri alabilmesi için stok tahsisatının kullanılmasıdır.

Stok tahsisatının iki temel iş amacı vardır:

- **Stok koruma (koruma altına alma)**: Kuruluşlar, sınırlandırılan veya sınırlı stoğu öncelikli kanallara, bölgelere, VIP müşterilerine ve yan şirketlere önceden tahsis etmek ister. Stok Görünürlüğü tahsisat özelliği, tahsis edilen stoğu korumayı amaçlar. Böylece diğer tahsisatlar, rezervasyonlar veya diğer satış talepleri önceden tahsis edilen stoğu etkileyemez.
- **Fazla satış denetimi**: Stok Görünürlüğü tahsisat özelliği, önceden tahsis edilen miktarlara kısıtlama koymayı amaçlar. Böylece alıcı taraf (ör. kanal veya müşteri grubu), geçici rezervasyona dayalı gerçek satış hareketi gerçekleşirken aşırı miktarda tüketim yapmaz.

## <a name="allocation-definition-in-inventory-visibility-service"></a>Stok Görünürlük Hizmeti'ndeki tahsisat tanımı

Stok Görünürlük hizmetindeki tahsisat özelliği stok miktarını fiziksel olarak kenara ayırmasa da ilk *tahsisata uygun* sanal havuz miktarını belirlemek için uygun fiziksel stok miktarına başvurur. Stok Görünürlüğündeki stok tahsisatı geçici bir tahsisattır. Gerçek satış hareketlerinin gerçekleşmesinden önce olur ve satış siparişlerini temel almaz. Örneğin, herhangi bir son müşteri satın almak için satış kanalını veya perakende satış mağazasını ziyaret etmeden önce, en önemli satış kanallarınıza veya büyük perakende şirketlerine stok tahsis edebilirsiniz.

Stok tahsisatı ile [stok geçici rezervasyonu](inventory-visibility-reservations.md) arasındaki fark, geçici rezervasyonun genellikle gerçek satış hareketlerine (satış siparişi satırları) bağlı olmasıdır. Bu nedenle, tahsisat ve geçici rezervasyon özelliklerini birlikte kullanmak istiyorsanız, önce stok tahsisatı yapmanızı ve ardından tahsis edilen miktarlara göre geçici rezervasyon yapmanızı öneririz. Daha fazla bilgi için bkz. [Geçici rezervasyon olarak tüketme](#consume-to-soft-reserved).

Stok tahsisatı özelliği satış planlayıcıları veya başlıca hesapların yöneticilerinin, önemli stoğu yönetmelerine ve tahsisat grupları (ör. kanallar, bölgeler ve müşteri grupları) arasında önceden tahsis etmesine olanak tanır. Ayrıca, stok yenileme veya yeniden tahsisat işlemlerinin zamanında yapılabilmesi için tahsis edilen miktarlarla ilgili tüketimin gerçek zamanlı olarak izlenmesi, düzeltilmesi ve analiz edilmesi işlemlerini de destekler. Tahsisat, tüketim ve tahsisat bakiyesine dair gerçek zamanlı görünürlük özelliği, hızlı satış veya promosyon etkinliklerinde özellikle büyük önem taşır.

## <a name="terminology"></a>Terminoloji

Stok tahsisatıyla ilgili konularda aşağıdaki terimler ve kavramlar faydalıdır:

- **Tahsisat grubu**: Tahsisatın sahibi olan grup (ör. satış kanalı, müşteri grubu veya sipariş türü).
- **Tahsisat grubu değeri**: Her tahsisat grubunun değeri. Örneğin, *web* veya *mağaza*, satış kanalı tahsisat grubunun değeri olabilir; *VIP* veya *normal* ise müşteri tahsisat grubunun değeri olabilir.
- **Tahsisat hiyerarşisi**: Tahsisat gruplarını hiyerarşik bir şekilde birleştirme yöntemi. Örneğin, *kanal* öğesini hiyerarşi düzeyi 1, *bölge* öğesini düzey 2 ve *müşteri grubu* öğesini düzey 3 olarak tanımlayabilirsiniz. Stok tahsisatı sırasında, tahsisat grubunun değerini belirttiğinizde tahsisat hiyerarşisi sırasını izlemeniz gerekir. Örneğin, *Web* kanalına, *Londra* bölgesine ve *VIP* müşteri grubuna 200 kırmızı bisiklet tahsis edebilirsiniz.
- **Tahsisata uygun**: Daha fazla tahsisata uygun olan miktarı gösteren *sanal ortak havuz*. Kendi formülünüzü kullanarak serbestçe tanımlayabileceğiniz hesaplanmış bir ölçümdür. Aynı zamanda geçici rezervasyon özelliğini de kullanıyorsanız, tahsisata uygun ve rezervasyona uygun miktar değerlerini hesaplamak için aynı formülü kullanmanız önerilir.
- **Tahsis edilen**: Tahsisat grupları tarafından tüketilebilen tahsis edilmiş kotayı gösteren fiziksel ölçü.
- **Tüketilen**: Başlangıçta tahsis edilen miktara karşı tüketilen miktarların gösterildiği fiziksel ölçü. Bu fiziksel ölçüye numaralar eklendikçe, Tahsis edilen fiziksel ölçü otomatik olarak düşürülür.

Aşağıdaki şekilde, kuruluşlar için stok tahsisatının iş akışı gösterilmektedir.

![Stok Görünürlüğü kuruluşlar için tahsisat iş akışı.](media/inventory-visibility-allocation-flow.png "Stok Görünürlüğü kuruluşlar için tahsisat iş akışı.")

## <a name="set-up-inventory-allocation"></a>Stok tahsisatını ayarlama

Stok tahsisatı özelliği aşağıdaki bileşenlerden oluşur:

- Önceden tanımlanmış, tahsisat ile ilgili veri kaynağı, fiziksel ölçüler ve hesaplanan ölçüler.
- Maksimum sekiz düzeye sahip özelleştirilebilir tahsisat grupları.
- Tahsisat uygulama programlama arabirimleri (API) kümesi:

    - allocate
    - reallocate
    - unallocate
    - consume
    - query

Tahsisat özelliğini yapılandırma işleminin iki adımı vardır:

- [Veri kaynağını](inventory-visibility-configuration.md#data-source-configuration) ve [ölçülerini](inventory-visibility-configuration.md#data-source-configuration-physical-measures) ayarlayın.
- Tahsisat grubu adını ve hiyerarşisini ayarlayın.

### <a name="predefined-data-source"></a>Önceden tanımlanmış veri kaynağı

Tahsisat özelliğini etkinleştirip yapılandırma güncelleştirmesi API'sini çağırırsanız, Stok Görünürlüğü önceden tanımlanmış bir veri kaynağı ve birkaç başlangıç ölçüsü oluşturur.

Veri kaynağı `@iv` olarak adlandırılır.

Başlangıçtaki fiziksel ölçüler şunlardır:

- `@iv`

    - `@allocated`
    - `@cumulative_allocated`
    - `@consumed`
    - `@cumulative_consumed`

Başlangıçtaki hesaplanan ölçüler şunlardır:

- `@iv`

    - `@iv.@available_to_allocate` = `??` – `??` – `@iv.@allocated`

### <a name="add-other-physical-measures-to-the-available-to-allocate-calculated-measure"></a>Tahsisata uygun hesaplanan ölçüsüne diğer fiziksel ölçüleri ekleme

Tahsisatı kullanmak için, tahsisata uygun hesaplanan ölçüsünü ayarlamanız gerekir (`@iv.@available_to_allocate`). Örneğin, `fno` veri kaynağına ve `onordered` ölçüsüne; `pos` veri kaynağına ve `inbound` ölçüsüne sahip olduğunuzu ve `fno.onordered` ve `pos.inbound` toplamı için eldeki stokta tahsisat yapmak istediğinizi varsayalım. Bu durumda `@iv.@available_to_allocate`, formülünde `pos.inbound` ve `fno.onordered` öğelerini içermelidir. Aşağıda bir örnek verilmiştir:

`@iv.@available_to_allocate` = `fno.onordered` + `pos.inbound` – `@iv.@allocated`

### <a name="change-the-allocation-group-name"></a>Tahsisat grubu adını değiştirme

En fazla sekiz tahsisat grubu adı ayarlanabilir. Grupların bir hiyerarşisi vardır.

Grup adlarını **Stok Görünürlüğü Power App Yapılandırması** sayfasında ayarlarsınız. Bu sayfayı açmak için Microsoft Dataverse ortamınızda Stok Görünürlüğü uygulamasını açın ve **Yapılandırma \> Tahsisat**'ı seçin.

Örneğin, dört grup adı kullanır ve bunları \[`channel`, `customerGroup`, `region`, `orderType`\] ayarlarsanız yapılandırma güncelleştirme API'sini çağırdığınızda, bu adlar tahsisat ile ilgili istekler için geçerli olur.

### <a name="allocation-using-tips"></a>Tahsisatı kullanmayla ilgili ipuçları

- Tahsisat işlevi, her ürün için [ürün dizini hiyerarşisi yapılandırmasında](inventory-visibility-configuration.md#index-configuration) ayarladığınız ürün dizini hiyerarşisine göre aynı *boyut düzeyinde* kullanılmalıdır. Örneğin, dizin hiyerarşinizin şöyle olduğunu varsayalım: \[`Site`, `Location`, `Color`, `Size`\]. Boyut düzeyinde \[`Site`, `Location`, `Color`\] bir ürün için bir miktar tahsis ederseniz daha sonra bu ürünü tahsis etmek istediğinizde, aynı düzeyde \[`Site`, `Location`, `Color`\] tahsisat yapmanız gerekir. \[`Site`, `Location`, `Color`, `Size`\] or \[`Site`, `Location`\] düzeyini kullanırsanız veriler tutarsız olacaktır.
- Tahsisat grubu adının değiştirilmesi, hizmete kaydedilen verileri etkilemez.
- Tahsisat, ürünün eldeki stok miktara pozitif olduktan sonra gerçekleştirilmelidir.
- Ürünleri yüksek bir *tahsisat düzeyi* grubundan bir alt gruba tahsis etmek için `Reallocate` API'sini kullanın. Örneğin, \[`channel`, `customerGroup`, `region`, `orderType`\] şeklinde bir tahsisat grubu hiyerarşiniz var ve tahsisat grubundan\[Online, VIP\] alt tahsisat grubuna \[Online, VIP, EU\], bir ürünü tahsis etmek istiyorsanız miktarı taşımak için `Reallocate` API'sini kullanın `Allocate` API'sini kullanırsanız sanal ortak havuzdaki miktar tahsis edilir.

### <a name="using-the-allocation-api"></a><a name="using-allocation-api"></a>Tahsisat API'sini kullanma

Şu anda beş tahsisat API'si açıktır:

- POST /api/environment/{environmentId}/allocation/allocate
- POST /api/environment/{environmentId}/allocation/unallocate
- POST /api/environment/{environmentId}/allocation/reallocate
- POST /api/environment/{environmentId}/allocation/consume
- POST /api/environment/{environmentId}/allocation/query

#### <a name="allocate"></a>Tahsis Et

Belirli boyutlara sahip bir ürünü tahsis etmek için `Allocate` API'sini çağırın. Bu istek gövdesinin şemasını aşağıda görebilirsiniz.

```json
{
    "id": "string",
    "productId": "string",
    "dimensionDataSource": "string",
    "targetGroups": {
        "groupA": "string",
        "groupB": "string",
        "groupC": "string"
    },
    "quantity": 0,
    "organizationId": "string",
    "dimensions": {
        "dimension1": "string",
        "dimension2": "string",
        "dimension3": "string"
    }
}
```

Örneğin ürün *Bisiklet*, tesis *1*, yerleşim *11*, renk *kırmızı*, kanal *Çevrimiçi*, müşteri grubu *VIP* ve bölge *ABD* için miktarı 10 olan bir tahsisat yapmak istiyorsunuz. Bu tahsisatı yapmak için, aşağıdaki gövde içeriğine sahip bir çağrı yapabilirsiniz.

```json
{
    "id": "???",
    "productId": "Bike",
    "targetGroups": {
        "channel": "Online",
        "customerGroup": "VIP",
        "region": "US"
    },
    "quantity": 10,
    "organizationId": "usmf",
    "dimensions": {
        "siteId": "1",
        "locationId": "11",
        "colorId": "red"
    }
}
```

Miktar her zaman 0 (sıfır) değerinden büyük olmalıdır.

#### <a name="unallocate"></a>Tahsisatı kaldırma

`Allocate` işlemini tersine çevirmek için `Unallocate` API'sini kullanın. `Allocate` işleminde negatif miktara izin verilmez. `Unallocate` gövdesi, `Allocate` gövdesi ile aynıdır.

#### <a name="reallocate"></a>Yeniden tahsis etme

Tahsis edilen miktarın bir kısmını başka bir grup birleşimine taşımak için `Reallocate` API'sini kullanın. Bu istek gövdesinin şemasını aşağıda görebilirsiniz.

```json
{
    "id": "string",
    "productId": "string",
    "dimensionDataSource": "string",
    "sourceGroups": {
        "groupA": "string",
        "groupB": "string",
        "groupC": "string"
    },
    "targetGroups": {
        "groupD": "string",
        "groupE": "string",
        "groupF": "string"
    },
    "quantity": 0,
    "organizationId": "string",
    "dimensions": {
        "dimension1": "string",
        "dimension2": "string",
        "dimension3": "string"
    }
}
```

Örneğin, `Reallocate` API'sini çağırıp aşağıdaki gövde metnini girerek bir tahsisat grubundaki \[site=1, location=11, color=red\] from allocation group \[Online, VIP, US\] boyutlarına sahip iki bisikleti \[Online, VIP, EU\] tahsisat grubuna taşıyabilirsiniz.

```json
{
    "id": "???",
    "productId": "Bike",
    "sourceGroups": {
        "channel": "Online",
        "customerGroup": "VIP",
        "region": "US"
    },
    "targetGroups": {
        "channel": "Online",
        "customerGroup": "VIP",
        "region": "EU"
    },
    "quantity": 2,
    "organizationId": "usmf",
    "dimensions": {
        "siteId": "1",
        "locationId": "11",
        "colorId": "red"
    }
}
```

#### <a name="consume"></a>Tüketim

Tahsisata karşılık tüketim miktarını deftere nakletmek için `Consume` API'sini kullanın. Örneğin, tahsis edilen miktarı bazı gerçek ölçülere taşımak için bu API'yi kullanabilirsiniz. Bu istek gövdesinin şemasını aşağıda görebilirsiniz.

```json
{
    "id": "string",
    "productId": "string",
    "dimensionDataSource": "string",
    "targetGroups": {
        "groupA": "string",
        "groupB": "string",
        "groupC": "string"
    },
    "quantity": 0,
    "organizationId": "string",
    "dimensions": {
        "dimension1": "string",
        "dimension2": "string",
        "dimension3": "string"
    },
    "physicalMeasures": {
        "datasource1": {
            "measure": "string" // Addition or Subtraction
        }
    }
}
```

Örneğin, \[site=1, location=11, color=red\] for allocation group \[Online, VIP, US\] boyutuna sahip sekiz tahsis edilmiş bisiklet bulunur. Aşağıdaki tahsisata uygun formülü kullanılır:

`@iv.@available_to_allocate` = `fno.onordered` + `pos.inbound` – `@iv.@allocated`

Sekiz bisiklet, `pos.inbound` ölçüsünden atanır.

Şimdi, üç bisiklet satılır ve bunlar tahsisat havuzundan alınır. Bu hareketi kaydetmek için aşağıdaki istek gövdesine sahip bir çağrı yapabilirsiniz.

```json
{
    "id": "???",
    "organizationId": "usmf",
    "productId": "Bike",
    "dimensions": {
        "siteId": "1",
        "locationId": "11",
        "colorId": "red"
    },
    "targetGroups": {
        "channel": "Online",
        "customerGroup": "VIP",
        "region": "US"
    },
    "quantity": 3,
    "physicalMeasures": {
        "pos": {
            "inbound": "Subtraction"
        }
    }
}
```

Bu çağrıdan sonra, ürün için tahsis edilen miktar 3 adet azaltılır. Ek olarak, Stok Görünürlüğü `pos.inbound` = *-3* olan bir eldeki stok değişikliği olayı oluşturur. Alternatif olarak `pos.inbound` değerini olduğu gibi tutup yalnızca tahsis edilen miktarı tüketebilirsiniz. Ancak, bu durumda, tüketilen miktarları korumak için başka bir fiziksel ölçü oluşturmanız veya önceden tanımlanmış `@iv.@consumed` ölçüsünü kullanmanız gerekir.

Bu istekte, tüketme isteği gövdesinde kullandığınız fiziksel ölçünün hesaplanan ölçüde kullanılan niteleyici türüne göre zıt niteleyici türünü (Toplama veya Çıkarma) kullanmalısınız. Bu tüketim gövdesinde, `iv.inbound` `Addition` değil `Subtraction` değerine sahiptir.

Stok Görünürlüğünün `fno` veri kaynağındaki hiçbir veriyi değiştiremeyeceğini belirttiğimiz için `fno` veri kaynağı tüketim gövdesinde kullanılamaz. Veri akışı tek yönlüdür. Diğer bir ifadeyle, `fno` veri kaynağına ilişkin tüm miktar değişiklikleri Supply Chain Management ortamınızdan gelmelidir.

#### <a name="consume-as-a-soft-reservation"></a><a name="consume-to-soft-reserved"></a>Geçici rezervasyon olarak tüketme

`Consume` API'si, tahsis edilen miktarı geçici rezervasyon olarak da tüketebilir. Bu durumda, `Consume` işlemi tahsis edilen miktarı azaltacak ve söz konusu miktar için geçici rezervasyon yapacaktır. Bu yaklaşımı kullanmak için, Stok Görünürlüğünün [geçici rezervasyon](inventory-visibility-reservations.md) özelliğini de kullanıyor olmanız gerekir.

Örneğin, geçici rezervasyon niteleyicisini (ölçü) `iv.softreserved` olarak ayarladığınızı varsayalım. Rezervasyona uygun hesaplanan ölçüsü için aşağıdaki formül kullanılır:

`iv.available_to_reserve` = `fno.onordered` + `pos.inbound` – `iv.softreserved`

Bu ayarı tahsisat özelliğiyle kullanmak için aşağıdaki formülü üretmek üzere `@iv.@allocated` öğesini `iv.available_to_reserve` öğesine ekleyin:

`iv.available_to_reserve` = `fno.onordered` + `pos.inbound` – `iv.softreserved` – `@iv.@allocated`

Ardından `@iv.@available_to_allocate` öğesini aynı değere güncelleştirin.

Miktar olarak 3 adet tüketmek ve bu miktar için doğrudan rezervasyon yapmak istiyorsanız aşağıdaki istek gövdesine sahip bir çağrı yapabilirsiniz.

```json
{
    "id": "???",
    "organizationId": "usmf",
    "productId": "Bike",
    "dimensions": {
        "siteId": "1",
        "locationId": "11",
        "colorId": "red"
    },
    "targetGroups": {
        "channel": "Online",
        "customerGroup": "VIP",
        "region": "US"
    },
    "quantity": 3,
    "physicalMeasures": {
        "iv": {
            "softreserved": "Addition"
        }
    }
}
```

Bu istekte, `iv.softreserved` öğesinin `Subtraction` değil `Addition` değerine sahip olduğunu görürsünüz.

#### <a name="query"></a>Sorgu

Bazı ürünler için tahsisatlarla ilgili bilgileri almak üzere `Query` API'sini kullanın. Sonuçları daraltmak için boyut filtreleri ve tahsisat grubu filtreleri kullanabilirsiniz. Boyutlar tam olarak almak istediğiniz değerle eşleşmelidir: Örneğin, \[site=1, location=11\], \[site=1, location=11, color=red\] boyutuna kıyasla ilgisiz sonuçlar döndürecektir.

```json
{
    "productId": "string",
    "organizationId": "string",
    "dimensions": {
        "dimension1": "string",
        "dimension2": "string",
        "dimension3": "string"
    },
    "groups": {
        "additionalProp1": "string",
        "additionalProp2": "string",
        "additionalProp3": "string"
    },
}
```

Örneğin, \[site=1, location=11, color=red\] boyutlarını kullanın ve tüm tahsisat kayıtlarını almak için grup alanlarını boşaltın.

```json
{
    "organizationId": "usmf",
    "productId": "Bike",
    "dimensions": {
        "siteId": "1",
        "locationId": "11",
        "colorId": "red"
    },
    "groups": {
        "channel": "Online",
        "customerGroup": "VIP",
        "region": "US"
    },
}
```

Şu grup için tahsisat kayıtlarını almak üzere  \[site=1, location=11, color=red\] boyutları ile \[channel=Online, customerGroup=VIP, region=US\] gruplarını kullanın.

```json
{
    "organizationId": "usmf",
    "productId": "Bike",
    "dimensions": {
        "siteId": "1",
        "locationId": "11",
        "colorId": "red"
    },
    "groups": {
        "channel": "Online",
        "customerGroup": "VIP",
        "region": "US"
    },
}
```
