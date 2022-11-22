---
title: Inventory Visibility stok tahsisatı
description: Bu makale, en karlı kanallarınızın veya müşterilerinizin siparişlerini karşılayabileceğinizden emin olmak için özel bir stok ayırmanıza olanak sağlayan stok tahsisatı özelliğinin nasıl ayarlanacağını ve kullanılacağını açıklar.
author: yufeihuang
ms.date: 11/04/2022
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yufeihuang
ms.search.validFrom: 2022-05-13
ms.dyn365.ops.version: 10.0.27
ms.openlocfilehash: 449ca0616405ba589b92fba1ef078a4350d1e3b1
ms.sourcegitcommit: 49f8973f0e121eac563876d50bfff00c55344360
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/14/2022
ms.locfileid: "9762685"
---
# <a name="inventory-visibility-inventory-allocation"></a>Inventory Visibility stok tahsisatı

[!include [banner](../includes/banner.md)]

## <a name="business-background-and-purpose"></a>İş arka planı ve amaç

Kuruluşların genellikle ellerindeki stoğu en önemli satış kanallarına, müşteri gruplarına, bölgelere ve promosyon etkinliklerşne önceden tahsis etmeleri ve önceden tahsis edilen stoğun başka şekilde kullanıma karşı korunduğundan ve yalnızca tahsisatla ilgili satış işlemleri aracılığıyla kullanılabilir olacağından emin olmaları gerekir. Stok Görünürlüğü'nde Stok tahsisatı satış operasyonel planlama sürecindeki bir bileşendir ve gerçek satış aktiviteleri gerçekleşmeden ve bir satış siparişi oluşturulmadan önce yapılır.

Örneğin, Contoso adlı bir şirket popüler bir bisiklet üretir. Ne yazık ki, yakın zamanda tedarik zincirinde meydana gelen bir kesinti bu bisikletin transitteki stoğunu etkilediğinden Contoso'nun eldeki stok miktarı sınırlıdır ve bunu en iyi şekilde kullanması gerekir. Contoso hem internet üzerinden hem de mağazada satış yapıyor. Şirketin, her satış kanalında bisikletin mevcut stoğunun belirli bir bölümünün kendilerine ayrılmasını talep eden birkaç önemli kurumsal iş ortağı (marketler ve büyük perakendeciler) bulunuyor. Bu nedenle, bisiklet şirketinin kanallar arasındaki stok dağılımını dengeleyebilmesi ve VIP iş ortaklarının beklentilerini yönetebilmesi gerekir. Her iki hedefe de ulaşmanın en iyi yolu, her bir kanal ve perakendecinin daha sonra tüketicilere satılmak üzere belirli miktarda tahsis edilen ürünleri alabilmesi için stok tahsisatının kullanılmasıdır.

Stok tahsisatının iki temel iş amacı vardır:

- **Stok koruma (sınırlama)**: Kuruluşlar, sınırlandırılan veya sınırlı stoğu öncelikli kanallara, bölgelere, VIP müşterilerine ve yan şirketlere önceden tahsis etmek ister. Stok Görünürlüğü tahsisat özelliği, tahsis edilen stoğu korumayı amaçlar. Böylece diğer tahsisatlar, rezervasyonlar veya diğer satış talepleri önceden tahsis edilen stoğu etkileyemez.
- **Fazla satış denetimi**: Stok Görünürlüğü tahsisat özelliği, önceden tahsis edilen miktarlara kısıtlama koymayı amaçlar. Böylece alıcı taraf (ör. kanal veya müşteri grubu), geçici rezervasyona dayalı gerçek satış hareketi gerçekleşirken aşırı miktarda tüketim yapmaz.

## <a name="allocation-definition-in-inventory-visibility-service"></a>Stok Görünürlük Hizmeti'ndeki tahsisat tanımı

### <a name="allocation-virtual-pool"></a>Tahsisat Sanal Havuzu

Stok Görünürlüğü'ndeki tahsisat özelliği stok miktarını fiziksel olarak kenara ayırmasa da ilk *tahsisata uygun* sanal havuz miktarını belirlemek için uygun fiziksel stok miktarına başvurur. Stok Görünürlüğündeki stok tahsisatı geçici bir tahsisattır. Gerçek satış hareketlerinin gerçekleşmesinden önce olur ve satış siparişlerini temel almaz. Örneğin, herhangi bir son müşteri satın almak için satış kanalını veya perakende satış mağazasını ziyaret etmeden önce, en önemli satış kanallarınıza veya büyük perakende şirketlerine stok tahsis edebilirsiniz.

### <a name="difference-between-inventory-allocation-and-soft-reservation"></a>Stok tahsisatı ve geçici rezervasyon arasındaki fark

[Geçici rezervasyonlar](inventory-visibility-reservations.md) genellikle gerçek satış hareketlerine (satış siparişi satırları) bağlıdır. Hem tahsisat hem de geçici rezervasyon bağımsız olarak kullanılabilir ancak bunları birlikte kullanmak istiyorsanız geçici rezervasyon tahsisat sonrasında yapılmalıdır. Tahsisata karşılık neredeyse gerçek zamanlı tüketim elde etmek için önce stok tahsisatı yapmanızı ve ardından tahsis edilen miktarlara göre geçici rezervasyon yapmanızı öneririz. Daha fazla bilgi için bkz. [Geçici rezervasyon olarak tüketme](#consume-to-soft-reserved).

Stok tahsisatı özelliği satış planlayıcıları veya başlıca hesapların yöneticilerinin, önemli stoğu yönetmelerine ve tahsisat grupları (ör. kanallar, bölgeler ve müşteri grupları) arasında önceden tahsis etmesine olanak tanır. Ayrıca, stok yenileme veya yeniden tahsisat işlemlerinin zamanında yapılabilmesini sağlamak için tahsis edilen miktarlarla ilgili tüketimin gerçek zamanlı olarak izlenmesi, düzeltilmesi ve analiz edilmesi işlemlerini de destekler. Tahsisat, tüketim ve tahsisat bakiyesine dair gerçek zamanlı görünürlük özelliği, hızlı satış veya promosyon etkinliklerinde özellikle büyük önem taşır.

## <a name="terminology"></a>Terminoloji

Stok tahsisatıyla ilgili konularda aşağıdaki terimler ve kavramlar faydalıdır:

- **Tahsisat grubu**: Tahsisatın sahibi olan grup (ör. satış kanalı, müşteri grubu veya sipariş türü).
- **Tahsisat grubu değeri**: Her tahsisat grubunun değeri. Örneğin, *web* veya *mağaza*, satış kanalı tahsisat grubunun değeri olabilir; *VIP* veya *normal* ise müşteri tahsisat grubunun değeri olabilir.
- **Tahsisat hiyerarşisi**: Tahsisat gruplarını hiyerarşik bir şekilde birleştirme yöntemi. Örneğin, *kanal* öğesini hiyerarşi düzeyi 1, *bölge* öğesini düzey 2 ve *müşteri grubu* öğesini düzey 3 olarak tanımlayabilirsiniz. Stok tahsisatı sırasında, tahsisat grubunun değerini belirttiğinizde tahsisat hiyerarşisi sırasını izlemeniz gerekir. Örneğin, *Web* kanalına, *Londra* bölgesine ve *VIP* müşteri grubuna 200 kırmızı bisiklet tahsis edebilirsiniz.
- **Tahsisata uygun**: Daha fazla tahsisata uygun olan miktarı gösteren *sanal ortak havuz*. Kendi formülünüzü kullanarak serbestçe tanımlayabileceğiniz hesaplanmış bir ölçümdür. Aynı zamanda geçici rezervasyon özelliğini de kullanıyorsanız, tahsisata uygun ve rezervasyona uygun miktar değerlerini hesaplamak için aynı formülü kullanmanız önerilir.
- **Tahsis edilen**: Tahsisat grupları tarafından tüketilebilen tahsis edilmiş kotayı gösteren fiziksel ölçü. Tüketilen miktarın eklendiği sırada kesinti yapılır.
- **Tüketilen**: Başlangıçta tahsis edilen miktara karşı tüketilen miktarların gösterildiği fiziksel ölçü. Bu fiziksel ölçüye numaralar eklendikçe, Tahsis edilen fiziksel ölçü otomatik olarak düşürülür.

Aşağıdaki şekilde, kuruluşlar için stok tahsisatının iş akışı gösterilmektedir.

![Stok Görünürlüğü kuruluşlar için tahsisat iş akışı.](media/inventory-visibility-allocation-flow.png "Stok Görünürlüğü kuruluşlar için tahsisat iş akışı.")

Aşağıdaki şekil tahsisat hiyerarşisini ve tahsisat gruplarını gösterir. Burada gösterilen *sanal ortak havuz* tahsis edilebilir miktardır.

[<img src="media/inventory-visibility-allocation-hierarchy.png" alt="Inventory Visibility allocation hierarchy." title="Stok Görünürlüğü tahsisat hiyerarşisi" width="720" />](media/inventory-visibility-allocation-hierarchy.png)

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

Tahsisat özelliğini yapılandırma işleminin üç adımı vardır:

- **Yapılandırma \> Özellik Yönetimi ve Ayarlar \> Tahsisat**'a giderek Stok Görünürlüğü uygulamaında özelliği etkinleştirin.
- [Veri kaynağını](inventory-visibility-configuration.md#data-source-configuration) ve [ölçülerini](inventory-visibility-configuration.md#data-source-configuration-physical-measures) ayarlayın.
- Tahsisat grubu adını ve hiyerarşisini ayarlayın.

### <a name="predefined-data-source"></a>Önceden tanımlanmış veri kaynağı

Tahsisat özelliğini etkinleştirip yapılandırma güncelleştirmesi API'sini çağırırsanız, Stok Görünürlüğü önceden tanımlanmış bir veri kaynağı ve birkaç başlangıç ölçüsü oluşturur.

Veri kaynağı `@iv` olarak adlandırılır. Varsayılan fiziksel ölçümler kümesi içerir. Bunları Stok Görünürlüğü uygulamasında **Yapılandırma \> Veri Kaynağı**'na giderek görebilirsiniz. **Veri kaynağı - @IV** görmeniz gerekir. İlk fiziksel ölçüm listesini görüntülemek için `@iv` veri kaynağını genişletin:

- `@iv`

    - `@allocated`
    - `@cumulative_allocated`
    - `@consumed`
    - `@cumulative_consumed`

`@iv.@available_to_allocate` olarak adlandırılan ilk hesaplanmış ölçümü görmek için **Hesaplanan Ölçümler** sekmesini seçin:

- `@iv`

    - `@iv.@available_to_allocate` = `??` – `??` – `@iv.@allocated`

### <a name="add-other-physical-measures-to-the-available-to-allocate-calculated-measure"></a>Tahsisata uygun hesaplanan ölçüsüne diğer fiziksel ölçüleri ekleme

Tahsisatı kullanmak için, tahsis edilebilir hesaplanan ölçüm formülü düzgün ayarlamanız gerekir (`@iv.@available_to_allocate`). Örneğin, `fno` veri kaynağına ve `onordered` ölçüsüne; `pos` veri kaynağına ve `inbound` ölçüsüne sahip olduğunuzu ve `fno.onordered` ve `pos.inbound` toplamı için eldeki stokta tahsisat yapmak istediğinizi varsayalım. Bu durumda `@iv.@available_to_allocate`, formülünde `pos.inbound` ve `fno.onordered` öğelerini içermelidir. Aşağıda bir örnek verilmiştir:

`@iv.@available_to_allocate` = `fno.onordered` + `pos.inbound` – `@iv.@allocated`

> [!NOTE]
> Veri kaynağı `@iv`, önceden tanımlanmış bir veri kaynağıdır ve `@` önekiyle `@iv` içinde tanımlanan fiziksel ölçümlerdir. Bu ölçümler tahsisat özelliği için önceden tanımlanmış bir yapılandırmadır; bu nedenle onları değiştirmeyin veya silmeyin. Aksi durumda, tahsisat özelliğini kullanırken beklenmedik hatalarla karşılaşabilirsiniz.
>
> Önceden tanımlanmış hesaplanan `@iv.@available_to_allocate` ölçümüne yeni fiziksel ölçümler ekleyebilirsiniz ancak adını değiştirmemeniz gerekir.

### <a name="manage-allocation-groups"></a>Tahsisat gruplarını yönetme

En fazla sekiz tahsisat grubu adı ayarlanabilir. Grupların bir hiyerarşisi vardır. Tahsisat gruplarını görüntülemek ve güncelleştirmek için şu adımları izleyin.

1. Power Apps ortamınızda oturum açın ve **Stok Görünürlüğü**'nü açın.
1. **Yapılandırma** sayfasını açın ve **Tahsisat** sekmesinde **Yapılandırmayı Düzenle**'yi seçin. Varsayılan olarak dört katmanlı bir tahsisat hiyerarşisi vardır: `Channel` (üst katman), `customerGroup` (ikinci katman), `Region` (üçüncü katman) ve `OrderType` (dördüncü katman).
1. Varolan bir tahsisat grubunu, yanındaki **X** simgesini seçerek kaldırabilirsiniz. Ayrıca, her yeni grubun adını alana doğrudan girerek de hiyerarşiye yeni tahsisat grupları ekleyebilirsiniz.

    > [!IMPORTANT]
    > Tahsisat hiyerarşisi eşlemesini silerken veya değiştirirken dikkatli olun. Açıklama için bkz. [Tahsisat kullanma ipuçları](#allocation-tips).

1. Tahsisat grubunu ve hiyerarşi ayarlarını yapılandırmayı tamamladığınızda değişikliklerinizi kaydedin ve sonra sağ üst köşede **Yapılandırmayı Güncelleştir**'i seçin. Yapılandırılan tahisat gruplarının değerleri, kullanıcı arabirimi veya API POST (/api<wbr>/environment<wbr>/\{environmentId\}<wbr>/allocation<wbr>/allocate) kullanarak bir tahsisat oluşturduğunuzda güncelleştirilir. Her iki yaklaşım hakkındaki ayrıntılar da bu makalenin sonraki bölümünde sağlanmaktadır.

Dört grup adı kullanır ve bunları \[`channel`, `customerGroup`, `region`, `orderType`\] ayarlarsanız yapılandırma güncelleştirme API'sini çağırdığınızda, bu adlar tahsisat ile ilgili istekler için geçerli olur.

### <a name="tips-for-using-allocation"></a><a name="allocation-tips"></a>Tahsisat kullanmayla ilgili ipuçları

- Tahsisat işlevi, her ürün için [ürün dizini hiyerarşisi yapılandırmasında](inventory-visibility-configuration.md#index-configuration) ayarladığınız ürün dizini hiyerarşisine göre aynı *boyut düzeyinde* kullanılmalıdır. Örneğin, dizin hiyerarşinizin şöyle olduğunu varsayalım: \[`Site`, `Location`, `Color`, `Size`\]. Boyut düzeyinde \[`Site`, `Location`, `Color`\] bir ürün için bir miktar tahsis ederseniz daha sonra bu ürünü tahsis etmek istediğinizde, aynı düzeyde \[`Site`, `Location`, `Color`\] tahsisat yapmanız gerekir. \[`Site`, `Location`, `Color`, `Size`\] or \[`Site`, `Location`\] düzeyini kullanırsanız veriler tutarsız olacaktır.
- **Tahsisat gruplarını ve hiyerarşiyi değiştirme:** Sistemde tahsisat verileri zaten varsa mevcut tahsisat gruplarının silinmesi veya tahsisat grubu hiyerarşisindeki bir değişiklik tahsisat grupları arasındaki mevcut eşlemeyi bozacaktır. Bu nedenle, yeni yapılandırmanızı güncelleştirmeden önce, eski verilerin tümünü el ile temizlediğinizden emin olun. Ancak, en düşük hiyerarşiye yeni tahsisat gruplarının eklenmesi mevcut eşlemeleri etkilemediği için, verileri temizlemeniz gerekmez.
- Tahsisat ancak ürünün pozitif `available_to_allocate` miktarı varsa başarılı olur.
- Ürünleri yüksek bir *tahsisat düzeyi* grubundan bir alt gruba tahsis etmek için `Reallocate` API'sini kullanın. Örneğin, \[`channel`, `customerGroup`, `region`, `orderType`\] şeklinde bir tahsisat grubu hiyerarşiniz var ve tahsisat grubundan\[Online, VIP\] alt tahsisat grubuna \[Online, VIP, EU\], bir ürünü tahsis etmek istiyorsanız miktarı taşımak için `Reallocate` API'sini kullanın `Allocate` API'sini kullanırsanız sanal ortak havuzdaki miktar tahsis edilir.
- Genel ürün kullanılabilirliğini (ortak havuz) görüntülemek için *tahsis edilebilir* olan stok miktarını talep etmek üzere [eldeki stoğu sorgula](inventory-visibility-api.md#query-on-hand) API'sini kullanın. Daha sonra bu bilgileri temel alan tahsisat kararları verebilirsiniz.

## <a name="use-the-allocation-api"></a><a name="using-allocation-api"></a>Tahsisat API'sini kullanma

Şu anda beş tahsisat API'si açıktır:

- **POST /api<wbr>/environment<wbr>/\{environmentId\}<wbr>/allocation<wbr>/allocate** – Bu API, ilk tahsisatı oluşturmak için kullanılır.
- **POST /api<wbr>/environment<wbr>/\{environmentId\}<wbr>/allocation<wbr>/unallocate** – Bu API, tahsis edilen miktarları geri almak veya kaldırmak için kullanılır.
- **POST /api<wbr>/environment<wbr>/\{environmentId\}<wbr>/allocation<wbr>/reallocate** – Bu API, tahsis edilen miktarı mevcut bir tahsisattan başka tahsisat gruplarına taşımak için kullanılır.
- **POST /api<wbr>/environment<wbr>/\{environmentId\}<wbr>/allocation<wbr>/consume** – Bu API, tahsis edilen miktarı eksiltmek (kullanmak) için kullanılır.
- **POST /api<wbr>/environment<wbr>/\{environmentId\}<wbr>/allocation<wbr>/query** – Bu API, mevcut tahsisat kayıtlarını tahsisat grupları ile hiyerarşiye göre denetlemek için kullanılır.

### <a name="allocate"></a>Tahsis Et

Belirli boyutlara sahip bir ürünü tahsis etmek için `Allocate` API'sini çağırın. Bu istek gövdesinin şemasını aşağıda görebilirsiniz.

```json
{
    "id": "string",
    "productId": "string",
    "dimensionDataSource": "string",
    "groups": {
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
    "id": "test101",
    "productId": "Bike",
    "groups": {
        "channel": "Web",
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

### <a name="unallocate"></a>Tahsisatı kaldırma

`Allocate` işlemini tersine çevirmek için `Unallocate` API'sini kullanın. `Allocate` işleminde negatif miktara izin verilmez. `Unallocate` gövdesi, `Allocate` gövdesi ile aynıdır.

### <a name="reallocate"></a>Yeniden tahsis etme

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
    "groups": {
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
    "id": "test102",
    "productId": "Bike",
    "sourceGroups": {
        "channel": "Web",
        "customerGroup": "VIP",
        "region": "US"
    },
    "groups": {
        "channel": "Web",
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

### <a name="consume"></a>Tüketim

Tahsisata karşılık tüketim miktarını deftere nakletmek için `Consume` API'sini kullanın. Örneğin, tahsis edilen miktarı bazı gerçek ölçülere taşımak için bu API'yi kullanabilirsiniz. Bu istek gövdesinin şemasını aşağıda görebilirsiniz.

```json
{
    "id": "string",
    "productId": "string",
    "dimensionDataSource": "string",
    "groups": {
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
    "id": "test103",
    "organizationId": "usmf",
    "productId": "Bike",
    "dimensions": {
        "siteId": "1",
        "locationId": "11",
        "colorId": "red"
    },
    "groups": {
        "channel": "Web",
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

### <a name="consume-as-a-soft-reservation"></a><a name="consume-to-soft-reserved"></a>Geçici rezervasyon olarak tüketme

`Consume` API'si, tahsis edilen miktarı geçici rezervasyon olarak da tüketebilir. Bu durumda, `Consume` işlemi tahsis edilen miktarı azaltacak ve söz konusu miktar için geçici rezervasyon yapacaktır. Bu yaklaşımı kullanmak için, Stok Görünürlüğünün [geçici rezervasyon](inventory-visibility-reservations.md) özelliğini de kullanıyor olmanız gerekir.

Örneğin, geçici rezervasyon fiziksel ölçüsünü `iv.softreserved` olarak ayarladığınızı varsayalım. Rezervasyona uygun hesaplanan ölçüsü için aşağıdaki formül kullanılır:

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
    "groups": {
        "channel": "Web",
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

### <a name="query"></a>Sorgu

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
        "channel": "Web",
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
        "channel": "Web",
        "customerGroup": "VIP",
        "region": "US"
    },
}
```

## <a name="use-the-allocation-user-interface"></a>Tahsisat kullanıcı arabirimini kullanma

Stok Görünürlüğü uygulamasını açıp **Operasyonel Görünürlük \> Tahsisat** alanına giderek tahsisatları kullanıcı arabirimi aracılığıyla el ile yönetebilirsiniz. Burada, aşağıdaki alt bölümlerde anlatılan eylemlerden herhangi birini gerçekleştirebilirsiniz.

### <a name="create-an-allocation"></a>Tahsisat oluşturma

Stok Görünürlüğü uygulamasının **Tahsisat** sayfasından bir tahsisat oluşturmak için bu adımları izleyin.

1. **Tahsis et**'i seçin.
1. Temel alanları, boyutları ve hedef tahsisat grupları değerlerini ayarlayın. (**Boyutlar** bölümünde veri kaynağı toplayı seçtiğinizde boyutları belirmek için önce açılan listeyi kullanın (örneğin, `siteId`). Ardından, görüntülenen alanlara boyut değerlerini girin.)
1. **Gönder**'i seçin.

### <a name="consume-an-allocation"></a>Tahsisat tüketme

Bir tahsisatı tüketmek için **Tüket**'i seçin. Doğru tahsisat grubu ve hiyerarşi içinde tükettiğinizden emin olmak için, tahsisatı oluştururken girdiğiniz aynı kuruluş ve boyut ayrıntıları kümesini girin.

### <a name="reallocate-an-allocation"></a>Tahsisat yeniden tahsis etme

Mevcut tahsis edilmiş miktarı bir tahsisat grubu kümesinden diğerine taşımak için **Yeniden tahsis et**'i seçin.

### <a name="query-existing-allocations"></a>Mevcut tahsisatları sorgulama

**Sorgula**'yı seçin ve mevcut tahsisatların sorgu sonuçlarını elde etmek için ürün, kuruluş, boyut ve tahsisat grubu değerlerini girin.
