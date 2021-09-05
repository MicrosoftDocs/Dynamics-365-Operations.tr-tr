---
title: Stok Görünürlüğü yapılandırma
description: Bu konuda, Stok Görünürlüğü'nün nasıl yapılandırılacağını açıklanmaktadır.
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
ms.openlocfilehash: 92e42b22d424ab80303d771f760cfcf0599b9f4c
ms.sourcegitcommit: b9c2798aa994e1526d1c50726f807e6335885e1a
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/13/2021
ms.locfileid: "7345045"
---
# <a name="inventory-visibility-configuration"></a>Stok Görünürlüğü yapılandırma

[!include [banner](../includes/banner.md)]
[!INCLUDE [cc-data-platform-banner](../../includes/cc-data-platform-banner.md)]

Bu konuda, Stok Görünürlüğü'nün nasıl yapılandırılacağını açıklanmaktadır.

## <a name="introduction"></a><a name="introduction"></a>Giriş

Stok Görünürlüğü ile çalışmaya başlamadan önce, bu konuda açıklandığı gibi aşağıdaki yapılandırmayı tamamlamanız gerekir:

- [Veri kaynağı yapılandırma](#data-source-configuration)
- [Bölüm yapılandırma](#partition-configuration)
- [Ürün dizini hiyerarşisi yapılandırma](#index-configuration)
- [Rezervasyon yapılandırma (isteğe bağlı)](#reservation-configuration)
- [Varsayılan yapılandırma örneği](#default-configuration-sample)

> [!NOTE]
> Stok Görünürlüğü yapılandırmalarını [Microsoft Power Apps](./inventory-visibility-power-platform.md#configuration)'te görüntüleyebilir ve düzenleyebilirsiniz. Yapılandırma tamamlandıktan sonra uygulamada **Yapılandırmayı Güncelleştir**'i seçin.

## <a name="data-source-configuration"></a><a name="data-source-configuration"></a>Veri kaynağı yapılandırma

Veri kaynağı, verilerinizin geldiği sistemi temsil eder. Örnekler arasında `fno` ("Dynamics 365 Finance and Operations uygulamaları" anlamına gelir) ve `pos` ("satış noktası" anlamına gelir) bulunmaktadır.

Veri kaynağı yapılandırması aşağıdaki bölümleri içerir:

- Boyut (boyut eşleme)
- Fiziksel ölçü
- Hesaplanan ölçü

> [!NOTE]
> `fno` veri kaynağı, Dynamics 365 Supply Chain Management için rezerve edilmiştir.

### <a name="dimension-dimension-mapping"></a><a name="data-source-configuration-dimension"></a>Boyut (boyut eşleme)

Boyut yapılandırmasının amacı, boyut birleşimlerine göre olayları ve sorguları deftere nakletmek için çoklu sistem tümleştirmesini standart hale getirmektir.

Stok Görünürlüğü aşağıdaki genel temel boyutları destekler.

| Boyut türü | Temel boyut |
|---|---|
| Ürün | `ColorId` |
| Ürün | `SizeId` |
| Ürün | `StyleId` |
| Ürün | `ConfigId` |
| İzleme | `BatchId` |
| İzleme | `SerialId` |
| Yer | `LocationId` |
| Yer | `SiteId` |
| Stok durumu | `StatusId` |
| Ambara özel | `WMSLocationId` |
| Ambara özel | `WMSPalletId` |
| Ambara özel | `LicensePlateId` |
| Diğerleri | `VersionId` |
| Stok (özel) | `InventDimension1` - `InventDimension12` |
| Dahili | `ExtendedDimension1` - `ExtendedDimension8` |

> [!NOTE]
> Önceki tabloda listelenen boyut türleri yalnızca referans amaçlıdır. Bunları Stok Görünürlüğü'nde tanımlamanız gerekmez.
>
> Stok (özel) boyutları, Supply Chain Management için rezerve edilmiş olabilir. Bu durumda, bunun yerine genişletilmiş boyutları kullanabilirsiniz.

Harici sistemler, RESTful API'leri aracılığıyla Stok Görünürlüğü'ne erişebilir. Tümleştirme için Stok Görünürlüğü, _harici veri kaynağını_ ve _harici boyutlardan_ _temel boyutlara_ eşlemeyi yapılandırmanıza olanak tanır. Aşağıda, bir boyut eşleme tablosu örneği verilmiştir.

| Harici boyut | Temel boyut |
|---|---|
| `MyColorId` | `ColorId` |
| `MySizeId` | `SizeId` |
| `MyStyleId` | `StyleId` |
| `MyDimension1` | `ExtendedDimension1` |
| `MyDimension2` | `ExtendedDimension2` |

Boyut eşlemesi yapılandırarak harici boyutları doğrudan Stok Görünürlüğü'ne gönderebilirsiniz. Stok Görünürlüğü daha sonra otomatik olarak harici boyutları temel boyutlara dönüştürür.

### <a name="physical-measures"></a>Fiziksel ölçüler

Fiziksel ölçüler miktarı değiştirir ve stok durumunu yansıtır. Gereksinimlerinize göre kendi fiziksel ölçülerinizi tanımlayabilirsiniz.

Stok Görünürlüğü, Supply Chain Management'a (`fno` veri kaynağı) bağlı varsayılan fiziksel ölçülerin bir listesini sağlar. Aşağıdaki tabloda, fiziksel ölçülerin bir örneği sağlanmaktadır.

| Fiziksel ölçü adı | Tanım |
|---|---|
| `NotSpecified` | Belirtilmemiş |
| `Arrived` | Gelen |
| `AvailOrdered` | Kullanılabilir sipariş edilen miktar |
| `AvailPhysical` | Kullanılabilir fiziksel miktar |
| `Deducted` | Düşülen |
| `OnOrder` | OnOrder |
| `Ordered` | Sipariş edilen |
| `PhysicalInvent` | Fiziksel stok |
| `Picked` | Çekildi |
| `PostedQty` | Deftere nakledilen miktar |
| `QuotationIssue` | Teklif çıkışı |
| `QuotationReceipt` | Teklif girişi |
| `Received` | Teslim alındı |
| `Registered` | Kayıtlı |
| `ReservOrdered` | Siparişli rezerve miktar |
| `ReservPhysical` | Fiziksel rezerve miktar |

### <a name="calculated-measures"></a><a name="data-source-configuration-calculated-measure"></a>Hesaplanan ölçüler

Hesaplanan ölçüler, fiziksel ölçülerin birleşiminden oluşan özelleştirilmiş bir hesaplama formülü sağlar. Bu işlev, özelleştirilmiş ölçümü oluşturmak için eklenecek bir dizi fiziksel ölçü ve/veya çıkarılacak bir dizi fiziksel ölçü tanımlamanıza olanak tanır.

Örneğin, aşağıdaki sorgu sonucuna sahipsiniz.

```json
[
    {
        "productId": "T-shirt",
        "dimensions": {
            "SiteId": "1",
            "LocationId": "11",
            "ColorId": "Red"
        },
        "quantities": {
            "pos": {
                "inbound": 80.0,
                "outbound": 20.0
            },
            "fno": {
                "availphysical": 100.0,
                "orderedintotal": 50.0,
                "orderedreserved": 10.0
            },
            "externalchannel": {
                "received": 90.0,
                "scheduled": 30.0,
                "issued": 60.0,
                "reserved": 40.0
            }
        }
    }
]
```

Ardından, aşağıdaki tabloda gösterildiği gibi `MyCustomAvailableforReservation` olarak adlandırılan bir hesaplanmış ölçü yapılandırırsınız. Hesaplanan bu ölçü tüketim sistemi tarafından tüketilir.

| Tüketim sistemi | Hesaplanan ölçü | Veri kaynağı | Fiziksel ölçü | Hesaplama türü |
|---|---|---|---|---|
| `CustomChannel` | `MyCustomAvailableforReservation` | `fno` | `availphysical` | `Addition` |
| `CustomChannel` | `MyCustomAvailableforReservation` | `fno` | `orderedintotal` | `Addition` |
| `CustomChannel` | `MyCustomAvailableforReservation` | `fno` | `orderedreserved` | `Subtraction` |
| `CustomChannel` | `MyCustomAvailableforReservation` | `pos` | `inbound` | `Addition` |
| `CustomChannel` | `MyCustomAvailableforReservation` | `pos` | `outbound` | `Subtraction` |
| `CustomChannel` | `MyCustomAvailableforReservation` | `externalchannel` | `received` | `Addition` |
| `CustomChannel` | `MyCustomAvailableforReservation` | `externalchannel` | `scheduled` | `Addition` |
| `CustomChannel` | `MyCustomAvailableforReservation` | `externalchannel` | `issued` | `Subtraction` |
| `CustomChannel` | `MyCustomAvailableforReservation` | `externalchannel` | `reserved` | `Subtraction` |

Bu hesaplama formülü kullanıldığında, yeni sorgu sonucu özelleştirilmiş ölçümü içerir.

```json
[
    {
        "productId": "T-shirt",
        "dimensions": {
            "SiteId": "1",
            "LocationId": "11",
            "ColorId": "Red"
        },
        "quantities": {
            "pos": {
                "inbound": 80.0,
                "outbound": 20.0
            },
            "fno": {
                "availphysical": 100.0,
                "orderedintotal": 50.0,
                "orderedreserved": 10.0
            },
            "externalchannel": {
                "received": 90.0,
                "scheduled": 30.0,
                "issued": 60.0,
                "reserved": 40.0
            },
            "CustomChannel": {
                "MyCustomAvailableforReservation": 220.0
            }
        }
    }
]
```

Özel ölçümlerdeki hesaplama ayarına göre `MyCustomAvailableforReservation` çıkışı 100 + 50 + 80 + 90 + 30 – 10 – 20 – 60 – 40 = 220'dir.

## <a name="partition-configuration"></a><a name="partition-configuration"></a>Bölüm yapılandırma

Bölüm yapılandırma, temel boyutların bir birleşiminden oluşur. Veri dağıtım modelini tanımlar. Aynı bölümdeki veri işlemleri yüksek performansı destekler ve çok fazla maliyeti yoktur. Bu nedenle, iyi bölüm modelleri önemli kazançlara katkıda bulunabilir.

Stok Görünürlüğü aşağıdaki varsayılan bölüm yapılandırmasını sağlar.

| Temel boyut | Hiyerarşi |
|---|---|
| `SiteId` | 1 |
| `LocationId` | 2 |

> [!NOTE]
> Varsayılan bölüm yapılandırması yalnızca referans içindir. Bunu Stok Görünürlüğü'nde tanımlamanız gerekmez. Şu anda bölüm yapılandırma yükseltmesi desteklenmemektedir.

## <a name="product-index-hierarchy-configuration"></a><a name="index-configuration"></a>Ürün dizini hiyerarşisi yapılandırma

Çoğu zaman, eldeki stok sorgusu yalnızca en yüksek "toplam" düzeyinde olmaz. Bunun yerine, stok boyutlarına göre toplanan sonuçları da görmek isteyebilirsiniz.

Stok Görünürlüğü, _dizinleri_ ayarlamanıza izin vererek esneklik sağlar. Bu dizinler bir boyutu veya boyutların birleşimini temel alır. Bir dizin, aşağıdaki tabloda tanımlandığı gibi bir *küme numarası*, bir *boyut* ve bir *hiyerarşi*'den oluşur.

| Kuruluş adı | Tanım |
|---|---|
| Küme numarası | Aynı kümeye (dizin) ait boyutlar birlikte gruplanır ve bunlara aynı küme numarası atanır. |
| Boyut | Sorgu sonucunun toplandığı temel boyutlar. |
| Hiyerarşi | Hiyerarşi sorgulanabilen desteklenen boyut birleşimlerini tanımlamak için kullanılır. Örneğin, hiyerarşi sırası `(ColorId, SizeId, StyleId)` olan bir boyut kümesi ayarlarsınız. Bu durumda sistem, dört boyutlu birleşimlerde sorguları destekler. İlk birleşim boş, ikincisi `(ColorId)`, üçüncüsü `(ColorId, SizeId)` ve dördüncüsü `(ColorId, SizeId, StyleId)` birleşimidir. Diğer birleşimler desteklenmez. Daha fazla bilgi için aşağıdaki örneğe bakın. |

### <a name="example"></a>Örnek

Bu bölüm, hiyerarşinin nasıl çalıştığını gösteren bir örnek sağlar.

Stokunuzda aşağıdaki maddeler var.

| Ürün | ColorId | SizeId | StyleId | Miktar |
|---|---|---|---|---|
| Tişört | Siyah | Küçük | Geniş | 1 |
| Tişört | Siyah | Küçük | Normal | 2 |
| Tişört | Siyah | Büyük | Geniş | 3 |
| Tişört | Siyah | Büyük | Normal | 4 |
| Tişört | Kırmızı | Küçük | Geniş | 5 |
| Tişört | Kırmızı | Küçük | Normal | 6 |
| Tişört | Kırmızı | Büyük | Normal | 7 |

Dizin aşağıdaki gibidir.

| Küme Numarası | Boyut | Hiyerarşi |
|---|---|---|
| 1 | `ColorId` | 1 |
| 1 | `SizeId` | 2 |
| 1 | `StyleId` | 3 |

Dizin, eldeki stoku aşağıdaki yollarla sorgulamanıza olanak tanır:

- `()`: Tümüne göre gruplandırılmıştır

    - Tişört, 28

- `(ColorId)`: `ColorId`'ye göre gruplandırılmıştır

    - Tişört, Siyah, 10
    - Tişört, Kırmızı, 18

- `(ColorId, SizeId)`: `ColorId` ve `SizeId` birleşimine göre gruplandırılmıştır

    - Tişört, Siyah, Küçük, 3
    - Tişört, Siyah, Büyük, 7
    - Tişört, Kırmızı, Küçük, 11
    - Tişört, Kırmızı, Büyük, 7

- `(ColorId, SizeId, StyleId)`: `ColorId`, `SizeId` ve `StyleId` birleşimine göre gruplandırılmıştır

    - Tişört, Siyah, Küçük, Geniş, 1
    - Tişört, Siyah, Küçük, Normal, 2
    - Tişört, Siyah, Büyük, Geniş, 3
    - Tişört, Siyah, Büyük, Normal, 4
    - Tişört, Kırmızı, Küçük, Geniş, 5
    - Tişört, Kırmızı, Küçük, Normal, 6
    - Tişört, Kırmızı, Büyük, Normal, 7

> [!NOTE]
> Bölüm yapılandırmasında tanımlanan temel boyutlar, dizin yapılandırmalarında tanımlanmamalıdır.

## <a name="reservation-configuration-optional"></a><a name="reservation-configuration"></a>Rezervasyon yapılandırma (isteğe bağlı)

[!INCLUDE [preview-banner-section](../../includes/preview-banner-section.md)]

Geçici rezervasyon özelliğini kullanmak istiyorsanız rezervasyon yapılandırması gereklidir. Yapılandırma iki temel bölümden oluşur:

- Geçici rezervasyon eşleme
- Geçici rezervasyon hiyerarşisi

### <a name="soft-reservation-mapping"></a>Geçici rezervasyon eşleme

Rezervasyon yaptığınızda, eldeki stokun şu anda rezervasyon için uygun olup olmadığını bilmek isteyebilirsiniz. Doğrulama, fiziksel ölçülerin bir birleşiminin bir hesaplama formülünü temsil eden hesaplanmış bir ölçüyle bağlantılıdır.

Örneğin, bir rezervasyon ölçüsü, `iv` (Stok Görünürlüğü) veri kaynağından alınan `SoftReservOrdered` fiziksel ölçüsünü temel alır. Bu durumda, burada gösterildiği gibi `iv` veri kaynağının `AvailableToReserve` hesaplanmış ölçüsünü ayarlayabilirsiniz.

| Hesaplama türü | Veri kaynağı | Fiziksel ölçü |
|---|---|---|
| Fark hesap eki | `fno` | `AvailPhysical` |
| Fark hesap eki | `pos` | `Inbound` |
| Çıkarma | `pos` | `Outbound` |
| Çıkarma | `iv` | `SoftReservOrdered` |

Ardından, `SoftReservOrdered` rezervasyon ölçüsünden `AvailableToReserve` hesaplanmış ölçüsüne bir eşleme sağlamak için bir geçici rezervasyon eşlemesi ayarlayın.

| Fiziksel ölçü veri kaynağı | Fiziksel ölçü | Rezerve edilebilir veri kaynağı | Rezerve edilebilir hesaplanan ölçü |
|---|---|---|---|
| `iv` | `SoftReservOrdered` | `iv` | `AvailableToReserve` |

Şimdi, `SoftReservOrdered` üzerinden rezervasyon yaptığınızda Stok Görünürlüğü, rezervasyon doğrulamasını yapmak için otomatik olarak `AvailableToReserve` ve ilgili hesaplama formülünü bulur.

Örneğin, Stok Görünürlüğü'nde aşağıdaki eldeki stoka sahipsiniz.

```json
{
    "productId": "T-shirt",
    "dimensions": {
        "SiteId": "1",
        "LocationId": "11",
        "ColorId": "Red"
    },
    "quantities": {
        "iv": {
            "SoftReservOrdered": 90
        },
        "fno": {
            "availphysical": 70.0,
        },
        "pos": {
            "inbound": 50.0,
            "outbound": 20.0
        }
    }
}
```

Bu durumda, aşağıdaki hesaplama geçerlidir:

`AvailableToReserve` = `fno.availphysical` + `pos.inbound` – `pos.outbound` – `iv.SoftReservOrdered`  
= 70 + 50 – 20 – 90  
= 10

Bu nedenle, `iv.SoftReservOrdered` üzerinden rezervasyon yapmaya çalışırsanız ve miktar `AvailableToReserve` (10) değerinden küçük veya eşit ise rezervasyonu yapabilirsiniz.

### <a name="soft-reservation-hierarchy"></a>Geçici rezervasyon hiyerarşisi

Rezervasyon hiyerarşisi, rezervasyonlar yapıldığında belirtilmesi gereken boyutların sırasını açıklar. Ürün dizini hiyerarşisinin eldeki sorgular için çalıştığı şekilde çalışır.

Rezervasyon hiyerarşisi, ürün dizini hiyerarşisinden bağımsızdır. Bu bağımsızlık, kullanıcıların daha hassas rezervasyonlar yapmak için gereksinimleri belirtmek üzere boyutları bölebilecekleri kategori yönetimi uygulamalarına olanak tanır.

Aşağıda, bir geçici rezervasyon hiyerarşisi örneği verilmiştir.

| Temel boyut | Hiyerarşi |
|---|---|
| `SiteId` | 1 |
| `LocationId` | 2 |
| `ColorId` | 3 |
| `SizeId` | 4 |
| `StyleId` | 5 |

Bu örnekte, aşağıdaki boyut serilerinde rezervasyon yapabilirsiniz:

- `()`: Hiçbir boyut belirtilmedi.
- `(SiteId)`
- `(SiteId, LocationId)`
- `(SiteId, LocationId, ColorId)`
- `(SiteId, LocationId, ColorId, SizeId)`
- `(SiteId, LocationId, ColorId, SizeId, StyleId)`

Geçerli bir boyut serisi, boyuta göre boyut rezervasyon hiyerarşisini kesinlikle izlemelidir. Örneğin, `(SiteId, LocationId, SizeId)` hiyerarşi sırası, `ColorId` eksik olduğundan geçerli değildir.

## <a name="default-configuration-sample"></a><a name="default-configuration-sample"></a>Varsayılan yapılandırma örneği

Stok Görünürlüğü, başlatma aşaması sırasında bir varsayılan yapılandırma ayarlar. Yapılandırmayı gerektiği şekilde değiştirebilirsiniz.

### <a name="data-source-configuration"></a>Veri kaynağı yapılandırma

#### <a name="configuration-of-the-iv-data-source"></a>iv veri kaynağını yapılandırma

Bu bölümde `iv` veri kaynağının nasıl yapılandırıldığı açıklanmaktadır.

##### <a name="physical-measures-configured-for-the-iv-data-source"></a>iv veri kaynağı için yapılandırılmış fiziksel ölçüler

`iv` veri kaynağı için aşağıdaki fiziksel ölçüler yapılandırılmıştır:

- `Ordered`
- `SoftReservPhysical`
- `SoftReservOrdered`
- `ReservOrdered`
- `ReservPhysical`

##### <a name="orderedtotal-calculated-measure"></a>OrderedTotal hesaplanan ölçüsü

`OrderedTotal` hesaplanan ölçüsü, aşağıdaki tabloda gösterildiği gibi `iv` veri kaynağı için yapılandırılmıştır.

| Hesaplama türü | Veri kaynağı | Fiziksel ölçü |
|---|---|---|
| Fark hesap eki | `fno` | `Ordered` |
| Fark hesap eki | `fno` | `Arrived` |
| Fark hesap eki | `iv` | `Ordered` |

##### <a name="onhand-calculated-measure"></a>OnHand hesaplanan ölçüsü

`OnHand` hesaplanan ölçüsü, aşağıdaki tabloda gösterildiği gibi `iv` veri kaynağı için yapılandırılmıştır.

| Hesaplama türü | Veri kaynağı | Fiziksel ölçü |
|---|---|---|
| Fark hesap eki | `fno` | `PhysicalInvent` |
| Fark hesap eki | `iom` | `OnHand` |
| Fark hesap eki | `erp` | `Unrestricted` |
| Fark hesap eki | `erp` | `QualityInspection` |
| Fark hesap eki | `pos` | `PosInbound` |
| Çıkarma | `pos` | `PosOutbound` |

##### <a name="reservedtotal-calculated-measure"></a>ReservedTotal hesaplanan ölçüsü

`ReservedTotal` hesaplanan ölçüsü, aşağıdaki tabloda gösterildiği gibi `iv` veri kaynağı için yapılandırılmıştır.

| Hesaplama türü | Veri kaynağı | Fiziksel ölçü |
|---|---|---|
| Fark hesap eki | `fno` | `ReservPhysical` |
| Fark hesap eki | `fno` | `ReservOrdered` |
| Fark hesap eki | `iv` | `SoftReservPhysical` |
| Fark hesap eki | `iv` | `SoftReservOrdered` |
| Fark hesap eki | `iv` | `ReservPhysical` |
| Fark hesap eki | `iv` | `ReservOrdered` |

##### <a name="softreserved-calculated-measure"></a>SoftReserved hesaplanan ölçüsü

`SoftReserved` hesaplanan ölçüsü, aşağıdaki tabloda gösterildiği gibi `iv` veri kaynağı için yapılandırılmıştır.

| Hesaplama türü | Veri kaynağı | Fiziksel ölçü |
|---|---|---|
| Fark hesap eki | `iv` | `SoftReservPhysical` |
| Fark hesap eki | `iv` | `SoftReservOrdered` |

##### <a name="hardreserved-calculated-measure"></a>HardReserved hesaplanan ölçüsü

`HardReserved` hesaplanan ölçüsü, aşağıdaki tabloda gösterildiği gibi `iv` veri kaynağı için yapılandırılmıştır.

| Hesaplama türü | Veri kaynağı | Fiziksel ölçü |
|---|---|---|
| Fark hesap eki | `fno` | `ReservPhysical` |
| Fark hesap eki | `fno` | `ReservOrdered` |
| Fark hesap eki | `iv` | `ReservPhysical` |
| Fark hesap eki | `iv` | `ReservOrdered` |

##### <a name="openorder-calculated-measure"></a>OpenOrder hesaplanan ölçüsü

`OpenOrder` hesaplanan ölçüsü, aşağıdaki tabloda gösterildiği gibi `iv` veri kaynağı için yapılandırılmıştır.

| Hesaplama türü | Veri kaynağı | Fiziksel ölçü |
|---|---|---|
| Fark hesap eki | `fno` | `OnOrder` |
| Fark hesap eki | `iom` | `OnOrder` |

##### <a name="onhandavailable-calculated-measure"></a>OnHandAvailable hesaplanan ölçüsü

`OnHandAvailable` hesaplanan ölçüsü, aşağıdaki tabloda gösterildiği gibi `iv` veri kaynağı için yapılandırılmıştır.

| Hesaplama türü | Veri kaynağı | Fiziksel ölçü |
|---|---|---|
| Fark hesap eki | `fno` | `PhysicalInvent` |
| Fark hesap eki | `iom` | `OnHand` |
| Fark hesap eki | `erp` | `Unrestricted` |
| Fark hesap eki | `erp` | `QualityInspection` |
| Fark hesap eki | `pos` | `PosInbound` |
| Çıkarma | `fno` | `ReservPhysical` |
| Çıkarma | `iv` | `SoftReservPhysical` |
| Çıkarma | `pos` | `PosOutbound` |

##### <a name="availabletoreserve-calculated-measure"></a>AvailableToReserve hesaplanan ölçüsü

`AvailableToReserve` hesaplanan ölçüsü, aşağıdaki tabloda gösterildiği gibi `iv` veri kaynağı için yapılandırılmıştır.

| Hesaplama türü | Veri kaynağı | Fiziksel ölçü |
|---|---|---|
| Fark hesap eki | `fno` | `PhysicalInvent` |
| Fark hesap eki | `iom` | `OnHand` |
| Fark hesap eki | `erp` | `Unrestricted` |
| Fark hesap eki | `erp` | `QualityInspection` |
| Fark hesap eki | `pos` | `PosInbound` |
| Fark hesap eki | `fno` | `Ordered` |
| Fark hesap eki | `fno` | `Arrived` |
| Fark hesap eki | `iv` | `Ordered` |
| Çıkarma | `fno` | `ReservPhysical` |
| Çıkarma | `fno` | `ReservOrdered` |
| Çıkarma | `iv` | `SoftReservPhysical` |
| Çıkarma | `iv` | `SoftReservOrdered` |
| Çıkarma | `iv` | `ReservPhysical` |
| Çıkarma | `iv` | `ReservOrdered` |
| Çıkarma | `pos` | `PosOutbound` |

##### <a name="inventorysupply-calculated-measure"></a>InventorySupply hesaplanan ölçüsü

`InventorySupply` hesaplanan ölçüsü, aşağıdaki tabloda gösterildiği gibi `iv` veri kaynağı için yapılandırılmıştır.

| Hesaplama türü | Veri kaynağı | Fiziksel ölçü |
|---|---|---|
| Fark hesap eki | `fno` | `Ordered` |
| Fark hesap eki | `fno` | `Arrived` |
| Fark hesap eki | `iv` | `Ordered` |
| Fark hesap eki | `fno` | `PhysicalInvent` |
| Fark hesap eki | `iom` | `OnHand` |
| Fark hesap eki | `erp` | `Unrestricted` |
| Fark hesap eki | `erp` | `QualityInspection` |
| Fark hesap eki | `pos` | `PosInbound` |
| Çıkarma | `pos` | `PosOutbound` |

##### <a name="inventorydemand-calculated-measure"></a>InventoryDemand hesaplanan ölçüsü

`InventoryDemand` hesaplanan ölçüsü, aşağıdaki tabloda gösterildiği gibi `iv` veri kaynağı için yapılandırılmıştır.

| Hesaplama türü | Veri kaynağı | Fiziksel ölçü |
|---|---|---|
| Fark hesap eki | `fno` | `OnOrder` |
| Fark hesap eki | `iom` | `OnOrder` |
| Fark hesap eki | `iv` | `SoftReservPhysical` |
| Fark hesap eki | `iv` | `SoftReservOrdered` |
| Fark hesap eki | `fno` | `ReservPhysical` |
| Fark hesap eki | `fno` | `ReservOrdered` |
| Fark hesap eki | `iv` | `ReservPhysical` |
| Fark hesap eki | `iv` | `ReservOrdered` |

#### <a name="configuration-of-the-fno-data-source"></a>fno veri kaynağını yapılandırma

Bu bölümde `fno` veri kaynağının nasıl yapılandırıldığı açıklanmaktadır.

##### <a name="dimension-mappings-for-the-fno-data-source"></a>fno veri kaynağı için boyut eşlemeleri

Aşağıdaki tabloda listelenen boyut eşlemeleri, `fno` veri kaynağı için yapılandırılmıştır.

| Harici boyut | Temel boyut |
|---|---|
| `InventBatchId` | `BatchId` |
| `InventColorId` | `ColorId` |
| `InventLocationId` | `LocationId` |
| `InventSerialId` | `SerialId` |
| `InventSiteId` | `SiteId` |
| `InventSizeId` | `SizeId` |
| `InventStatusId` | `StatusId` |
| `InventStyleId` | `StyleId` |
| `LicensePlateId` | `LicensePlateId` |
| `WMSLocationId` | `WMSLocationId` |
| `WMSPalletId` | `WMSPalletId` |
| `ConfigId` | `ConfigId` |
| `InventVersionId` | `VersionId` |
| `InventDimension1` | `CustomDimension1` |
| `InventDimension2` | `CustomDimension2` |
| `InventDimension3` | `CustomDimension3` |
| `InventDimension4` | `CustomDimension4` |
| `InventDimension5` | `CustomDimension5` |
| `InventDimension6` | `CustomDimension6` |
| `InventDimension7` | `CustomDimension7` |
| `InventDimension8` | `CustomDimension8` |
| `InventDimension9` | `CustomDimension9` |
| `InventDimension10` | `CustomDimension10` |
| `InventDimension11` | `CustomDimension11` |
| `InventDimension12` | `CustomDimension12` |

##### <a name="physical-measures-configured-for-the-fno-data-source"></a>fno veri kaynağı için yapılandırılmış fiziksel ölçüler

`fno` veri kaynağı için aşağıdaki fiziksel ölçüler yapılandırılmıştır:

- `Ordered`
- `Arrived`
- `AvailPhysical`
- `PhysicalInvent`
- `ReservPhysical`
- `ReservOrdered`
- `OnOrder`

#### <a name="configuration-of-the-pos-data-source"></a>pos veri kaynağını yapılandırma

Bu bölümde `pos` veri kaynağının nasıl yapılandırıldığı açıklanmaktadır.

##### <a name="physical-measures-for-the-pos-data-source"></a>pos veri kaynağı için yapılandırılmış fiziksel ölçüler

`pos` veri kaynağı için aşağıdaki fiziksel ölçüler yapılandırılmıştır:

- `PosInbound`
- `PosOutbound`

##### <a name="availquantity-calculated-measure"></a>AvailQuantity hesaplanan ölçüsü

`AvailQuantity` hesaplanan ölçüsü, aşağıdaki tabloda gösterildiği gibi `pos` veri kaynağı için yapılandırılmıştır.

| Hesaplama türü | Veri kaynağı | Fiziksel ölçü |
|---|---|---|
| Fark hesap eki | `fno` | `AvailPhysical` |
| Fark hesap eki | `pos` | `PosInbound` |
| Çıkarma | `pos` | `PosOutbound` |

#### <a name="configuration-of-the-iom-data-source"></a>iom veri kaynağını yapılandırma

Aşağıdaki fiziksel ölçüler `iom` (akıllı sipariş yönetimi) veri kaynağı için yapılandırılmıştır:

- `OnOrder`
- `OnHand`

#### <a name="configuration-of-the-erp-data-source"></a>erp veri kaynağını yapılandırma

Aşağıdaki fiziksel ölçüler `erp` (kurumsal kaynak planlama) veri kaynağı için yapılandırılmıştır:

- `Unrestricted`
- `QualityInspection`

### <a name="partition-configuration"></a>Bölüm yapılandırma

Aşağıdaki tabloda, varsayılan bölüm yapılandırması gösterilmektedir.

| Temel boyut | Hiyerarşi |
|---|---|
| `SiteId` | 1 |
| `LocationId` | 2 |

### <a name="index-configuration"></a>Dizin yapılandırma

Aşağıdaki tabloda, varsayılan dizin yapılandırması gösterilmektedir.

| Küme Numarası | Boyut | Hiyerarşi |
|---|---|---|
| 1 | `ColorId` | 1 |
| 1 | `SizeId` | 2 |
| 1 | `StyleId` | 3 |

### <a name="reservation-configuration"></a>Rezervasyon yapılandırma

Bu bölümde, varsayılan rezervasyon yapılandırması açıklanmaktadır.

#### <a name="reservation-mapping"></a>Rezervasyon eşlemesi

[!INCLUDE [preview-banner-section](../../includes/preview-banner-section.md)]

Aşağıdaki tabloda, varsayılan rezervasyon eşlemesi gösterilmektedir.

| Fiziksel ölçü veri kaynağı | Fiziksel ölçü | Rezerve edilebilir veri kaynağı | Rezerve edilebilir hesaplanan ölçü |
|---|---|---|---|
| `iv` | `SoftReservOrdered` | `iv` | `AvailableToReserve` |

#### <a name="reservation-hierarchy"></a>Rezervasyon hiyerarşisi

Aşağıdaki tabloda, varsayılan rezervasyon hiyerarşisi gösterilmektedir.

| Temel boyut | Hiyerarşi |
|---|---|
| `SiteId` | 1 |
| `LocationId` | 2 |
| `ColorId` | 3 |
| `SizeId` | 4 |
| `StyleId` | 5 |
| `BatchId` | 6 |
| `SerialId` | 7 |
| `StatusId` | 8 |
| `LicensePlateId` | 9 |
| `WMSLocationId` | 10 |
| `WMSPalletId` | 11 |
| `ConfigId` | 12 |
| `VersionId` | 13 |
| `CustomDimension1` | 14 |
| `CustomDimension2` | 15 |
| `CustomDimension3` | 16 |
| `CustomDimension4` | 17 |
| `CustomDimension5` | 18 |
| `CustomDimension6` | 19 |
| `CustomDimension7` | 20 |
| `CustomDimension8` | 21 |
| `CustomDimension9` | 22 |
| `CustomDimension10` | 23 |
| `CustomDimension11` | 24 |
| `CustomDimension12` | 25 |
| `ExtendedDimension1` | 26 |
| `ExtendedDimension2` | 27 |
| `ExtendedDimension3` | 28 |
| `ExtendedDimension4` | 29 |
| `ExtendedDimension5` | 30 |
| `ExtendedDimension6` | 31 |
| `ExtendedDimension7` | 32 |
| `ExtendedDimension8` | 33 |

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
