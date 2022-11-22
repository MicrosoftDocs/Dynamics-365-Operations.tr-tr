---
title: Inventory Visibility'yi yapılandırma
description: Bu makalede, Stok Görünürlüğü'nün nasıl yapılandırılacağını açıklanmaktadır.
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
ms.openlocfilehash: 915382c14cc9ba89b9d543cfd668a94cecbc0a55
ms.sourcegitcommit: 4f987aad3ff65fe021057ac9d7d6922fb74f980e
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/14/2022
ms.locfileid: "9765718"
---
# <a name="configure-inventory-visibility"></a>Inventory Visibility'yi yapılandırma

[!include [banner](../includes/banner.md)]

Bu makalede, Power Apps'te Stok Görünürlüğü uygulamasını kullanarak Stok Görünürlüğü'nü yapılandırma açıklanmaktadır.

## <a name="introduction"></a><a name="introduction"></a>Giriş

Stok Görünürlüğü ile çalışmaya başlamadan önce, bu makalede açıklandığı gibi aşağıdaki yapılandırmayı tamamlamanız gerekir:

- [Veri kaynağı yapılandırma](#data-source-configuration)
- [Bölüm yapılandırma](#partition-configuration)
- [Ürün dizini hiyerarşisi yapılandırma](#index-configuration)
- [Rezervasyon yapılandırma (isteğe bağlı)](#reservation-configuration)
- [Varsayılan yapılandırma örneği](#default-configuration-sample)

## <a name="prerequisites"></a>Önkoşullar

Başlamadan önce, Stok Görünürlüğü Eklentisini [Stok Görünürlüğü'nü yükleme ve ayarlama](inventory-visibility-setup.md) bölümünde açıklandığı gibi yükleyin ve ayarlayın.

## <a name="the-configuration-page-of-the-inventory-visibility-app"></a><a name="configuration"></a>Stok Görünürlüğü uygulamasının Yapılandırma sayfası

Power Apps'te, [Stok Görünürlüğü uygulamasının](inventory-visibility-power-platform.md) **Yapılandırma** sayfası eldeki yapılandırmasını ve geçici rezervasyon yapılandırmasını ayarlamanıza yardımcı olur. Eklenti yüklendikten sonra varsayılan yapılandırma, Microsoft Dynamics 365 Supply Chain Management'tan (`fno` veri kaynağı) alınan değeri içerir. Varsayılan ayarları inceleyebilirsiniz. Ek olarak, iş gereksinimlerinize ve harici sisteminizin stok deftere nakil gereksinimlerine göre yapılandırmayı, stok değişikliklerinin birden çok sistem arasında deftere nakledilme, düzenlenme ve sorgulanma şeklini standartlaştırmak için değiştirebilirsiniz. Bu makalenin geri kalan bölümlerinde **Yapılandırma** sayfasının her bir bölümünün nasıl kullanılacağı açıklanmaktadır.

Yapılandırma tamamlandıktan sonra uygulamada **Yapılandırmayı Güncelleştir** seçeneğinin belirlendiğinden emin olun.

## <a name="enable-inventory-visibility-features-in-power-apps-feature-management"></a><a name="feature-switch"></a>Power Apps özellik yönetiminde Stok Görünürlüğü özelliklerini etkinleştirme

Stok Görünürlüğü Eklentisi, Power Apps kurulumunuza birkaç yeni özellik ekler. Varsayılan olarak, bu özellikler kapalıdır. Bunları kullanmak için **Yapılandırma** sayfasını açın ve ardından **Özellik Yönetimi** sekmesinde aşağıdaki özellikleri istediğiniz gibi açın.

| Özellik Yönetimi adı | Açıklama |
|---|---|
| *OnHandReservation* | Bu özellik, Stok Görünürlüğü'nü kullanarak rezervasyon oluşturmanızı, rezervasyonları tüketmenizi ve/veya belirtilen stok miktarlarının rezervasyonunu kaldırmanızı sağlar. Daha fazla bilgi için bkz. [Stok Görünürlüğü rezervasyonları](inventory-visibility-reservations.md). |
| *OnHandMostSpecificBackgroundService* | Bu özellik, tüm boyutlarla birlikte ürünler için bir stok özeti sağlar. Stok özeti verileri, Stok Görünürlüğü'nden periyodik olarak eşitlenir. Varsayılan eşitleme sıklığı 15 dakikada birdir ve en çok 5 dakikada bir olarak ayarlanabilir. Daha fazla bilgi için bkz. [Stok özeti](inventory-visibility-power-platform.md#inventory-summary). |
| *onHandIndexQueryPreloadBackgroundService* | Bu özellik, önceden seçilen boyutlarla eldeki listeleri birleştirmek için Stok Görünürlüğü eldeki sorgulara önceden yüklemeye olanak sağlar. Varsayılan eşitleme sıklığı her 15 dakikada bir yapılır. Daha fazla bilgi için bkz. [Kolaylaştırılmış eldeki stok sorgusunu önceden yükleme](inventory-visibility-power-platform.md#preload-streamlined-onhand-query). |
| *OnhandChangeSchedule* | Bu isteğe bağlı özellik, eldeki değişiklik zamanlamasını etkinleştirir ve karşılanabilir miktar (KM) özelliklerini sunar. Daha fazla bilgi için bkz. [Stok Görünürlüğü eldeki değişiklik zamanlaması ve karşılanabilir miktarı](inventory-visibility-available-to-promise.md). |
| *Tahsisat* | Bu isteğe bağlı özellik Stok Görünürlüğünün stok koruması (sınırlama) ve fazla satış yapma denetimi yeteneğine sahip olmasını sağlar. Daha fazla bilgi için bkz. [Stok Görünürlüğü stok tahsisatı](inventory-visibility-allocation.md). |
| *Stok Görünürlüğünde ambar maddelerini etkinleştir* | Bu isteğe bağlı özellik, Stok Görünürlüğü'nün ambar yönetim süreçleri (WMS) için etkinleştirilen öğeleri desteklemesini sağlar. Daha fazla bilgi için bkz. [WMS öğeleri için Stok Görünürlüğü desteği](inventory-visibility-whs-support.md). |

## <a name="find-the-service-endpoint"></a><a name="get-service-endpoint"></a>Hizmet uç noktasını bulma

Doğru Stok Görünürlüğü hizmeti uç noktasını bilmiyorsanız Power Apps'te **Yapılandırma** sayfasını açın ve ardından sağ üst köşedeki **Hizmet Ayrıntılarını Göster**'i seçin. Sayfa doğru hizmet uç noktasını gösterir. Uç noktasını Microsoft Dynamics Lifecycle Services'ta [Lifecycle Services ortamınıza göre uç noktayı bulma](inventory-visibility-api.md#endpoint-lcs) bölümünde açıklandığı şekilde de bulabilirsiniz.

> [!NOTE]
> Yanlış bir uç nokta kullanımı, Supply Chain Management Stok Görünürlüğü'n eeşitlendiğinde, başarısız bir Stok Görünürlüğü yüklemesine ve hatalara neden olabilir. Uç noktasının ne olduğundan emin değilseniz, sistem yöneticinize başvurun. Uç nokta URL'leri için aşağıdaki biçimi kullanın:
>
> `https://inventoryservice.<RegionShortName>-il<IsLandNumber>.gateway.prod.island.powerapps.com`

## <a name="data-source-configuration"></a><a name="data-source-configuration"></a>Veri kaynağı yapılandırma

Her veri kaynağı, verilerinizin geldiği bir sistemi temsil eder. Örnek veri kaynağı adları arasında `fno` (Supply Chain Management anlamına gelir) ve `pos` ("satış noktası" anlamına gelir) bulunmaktadır. Varsayılan olarak Supply Chain Management, Stok Görünürlüğü'nde varsayılan veri kaynağı (`fno`) olarak ayarlanır.

> [!NOTE]
> `fno` veri kaynağı, Supply Chain Management için rezerve edilmiştir. Stok Görünürlüğü eklentiniz bir Supply Chain Management ortamıyla tümleşikse veri kaynağındaki `fno` ile ilgili yapılandırmaları silmemenizi öneririz.

Veri kaynağı eklemek için şu adımları izleyin.

1. Power Apps ortamınızda oturum açın ve **Stok Görünürlüğü**'nü açın.
1. **Yapılandırma** sayfasını açın.
1. Veri kaynağı eklemek için **Veri Kaynağı** sekmesinde **Yeni Veri Kaynağı**'nı seçin (örneğin `ecommerce` veya anlamlı başka bir veri kaynağı kimliği).

> [!NOTE]
> Bir veri kaynağı eklediğinizde, Stok Görünürlüğü hizmetinin yapılandırmasını güncelleştirmeden önce veri kaynağı adınızı, fiziksel ölçüleri ve boyut eşlemelerini doğrulamaya dikkat edin. **Yapılandırmayı Güncelleştirme**'yi seçtikten sonra bu ayarları değiştiremezsiniz.

Veri kaynağı yapılandırması aşağıdaki bölümleri içerir:

- Boyutlar (boyut eşleme)
- Fiziksel ölçüler
- Hesaplanan ölçüler

### <a name="dimensions-dimension-mapping"></a><a name="data-source-configuration-dimension"></a>Boyutlar (boyut eşleme)

Boyut yapılandırmasının amacı, boyut birleşimlerine göre olayları ve sorguları deftere nakletmek için çoklu sistem tümleştirmesini standart hale getirmektir. Stok Görünürlüğü, veri kaynağınızın boyutlarından eşlenebilir temel boyutların listesini sağlar. Eşleme için otuz üç boyut kullanılabilir.

- Veri kaynaklarınızdan biri olarak Supply Chain Management kullanıyorsanız 13 boyut, Supply Chain Management standart boyutlarıyla varsayılan olarak zaten eşlenmiştir. Diğer 12 boyut da (`inventDimension1` ile `inventDimension12` arasında) Supply Chain Management'ta özel boyutlara eşlenir. Kalan sekiz boyut, (`ExtendedDimension1` ile `ExtendedDimension8` arasında) harici veri kaynaklarıyla eşleyebileceğiniz genişletilmiş boyutlardır.
- Supply Chain Management'ı veri kaynaklarınızdan biri olarak kullanmıyorsanız boyutları serbestçe eşleyebilirsiniz. Aşağıdaki tabloda, kullanılabilir boyutların tam listesi gösterilmektedir.

> [!NOTE]
> Supply Chain Management kullanıyorsanız ve Supply Chain Management ile Stok Görünürlüğü arasındaki varsayılan boyut eşlemelerini değiştirirseniz, değiştirilen boyut verileri eşitlemez. Bu nedenle, boyutunuz varsayılan boyut listesinde değilse ve harici bir veri kaynağı kullanıyorsanız eşlemeyi yapmak için `ExtendedDimension1` aracılığıyla `ExtendedDimension8` kullanmanızı öneririz.

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
| Uzantı | `ExtendedDimension1` - `ExtendedDimension8` |
| Sistem | `Empty` |

> [!NOTE]
> Önceki tabloda listelenen boyut türleri yalnızca referans amaçlıdır. Bunları Stok Görünürlüğü'nde tanımlamanız gerekmez.
>
> Stok (özel) boyutları, Supply Chain Management için rezerve edilmiş olabilir. Bu durumda, bunun yerine genişletilmiş boyutları kullanın.

Harici sistemler, RESTful API'leri aracılığıyla Stok Görünürlüğü'ne erişebilir. Tümleştirme için Stok Görünürlüğü, *harici veri kaynağını* ve *harici boyutlardan* *temel boyutlara* eşlemeyi yapılandırmanıza olanak tanır. Aşağıda, bir boyut eşleme tablosu örneği verilmiştir.

| Harici boyut | Temel boyut |
|---|---|
| `MyColorId` | `ColorId` |
| `MySizeId` | `SizeId` |
| `MyStyleId` | `StyleId` |
| `MyDimension1` | `ExtendedDimension1` |
| `MyDimension2` | `ExtendedDimension2` |

Boyut eşlemesi yapılandırarak harici boyutları doğrudan Stok Görünürlüğü'ne gönderebilirsiniz. Stok Görünürlüğü daha sonra otomatik olarak harici boyutları temel boyutlara dönüştürür.

Boyut eşlemeleri eklemek için şu adımları izleyin.

1. Power Apps ortamınızda oturum açın ve **Stok Görünürlüğü**'nü açın.
1. **Yapılandırma** sayfasını açın.
1. **Veri kaynağı** sekmesinde, boyut eşlemesini yapmak istediğiniz veri kaynağını seçin. Ardından, **Boyut Eşlemeleri** bölümünde, boyut eşlemeleri eklemek için **Ekle**'yi seçin.

    ![Boyut eşlemeleri ekleme](media/inventory-visibility-dimension-mapping.png "Boyut eşlemeleri ekleme")

1. **Boyut Adı** alanında, kaynak boyutunu belirtin.
1. **Temel Boyuta** alanında, Stok Görünürlüğü'nde eşleştirmek istediğiniz boyutu seçin.
1. **Kaydet**'i seçin.

Örneğin, adı `ecommerce` olan bir veri kaynağı oluşturdunuz ve bir ürün rengi boyutu içeriyor. Bu durumda, eşlemeyi yapmak için önce `ecommerce` veri kaynağındaki **Boyut Adı** alanına `ProductColor` ekleyin ve ardından **Hedef Temel Boyut** alanında `ColorId` öğesini seçin.

### <a name="physical-measures"></a><a name="data-source-configuration-physical-measures"></a>Fiziksel ölçüler

Veri kaynağı, Stok Görünürlüğü'ne bir stok değişikliğini naklettiğinde bu değişikliği *fiziksel ölçüler* kullanarak nakleder. Fiziksel ölçüler miktarı değiştirir ve stok durumunu yansıtır. Gereksinimlerinize göre kendi fiziksel ölçülerinizi tanımlayabilirsiniz. Sorgular fiziksel ölçülere göre olabilir.

Stok Görünürlüğü, Supply Chain Management'a (`fno` veri kaynağı) eşlenen varsayılan fiziksel ölçülerin bir listesini sağlar. Bu varsayılan fiziksel ölçüler, Supply Chain Management'taki **Eldekilerin listesi** sayfasındaki stok hareket durumlarından alınır (**Stok yönetimi \> Sorgular ve Raporlar \> Eldekilerin listesi**). Aşağıdaki tabloda, fiziksel ölçülerin bir örneği sağlanmaktadır.

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
| `Received` | Teslim Alındı |
| `Registered` | Kayıtlı |
| `ReservOrdered` | Siparişli rezerve miktar |
| `ReservPhysical` | Fiziksel rezerve miktar |

Veri kaynağınız, Supply Chain Management ise varsayılan fiziksel ölçüleri yeniden oluşturmanız gerekmez. Ancak, harici veri kaynakları için aşağıdaki adımları izleyerek yeni fiziksel ölçüler oluşturabilirsiniz.

1. Power Apps ortamınızda oturum açın ve **Stok Görünürlüğü**'nü açın.
1. **Yapılandırma** sayfasını açın.
1. **Veri kaynağı** sekmesinde, fiziksel ölçüleri eklemek için veri kaynağını seçin (örneğin, `ecommerce` veri kaynağı). Sonra, **Fiziksel Ölçüler** bölümünde **Ekle**'yi seçin ve ölçü adını belirtin (örneğin, bu veri kaynağında iade edilen miktarları Stok Görünürlüğü'ne kaydetmek istiyorsanız `Returned`). Değişikliklerinizi kaydedin.

### <a name="calculated-measures"></a>Hesaplanan ölçüler

Hem stok fiziksel ölçülerini hem de *özel hesaplanmış ölçüleri* sorgulamak için Stok Görünürlüğü'nü kullanabilirsiniz. Hesaplanan ölçüler, fiziksel ölçülerin birleşiminden oluşan özelleştirilmiş bir hesaplama formülü sağlar. Bu işlev, özelleştirilmiş ölçümü oluşturmak için eklenecek bir dizi fiziksel ölçü ve/veya çıkarılacak bir dizi fiziksel ölçü tanımlamanıza olanak tanır.

> [!IMPORTANT]
> Hesaplanan ölçü fiziksel ölçülerin birleşimidir. Formülü hesaplanan ölçüler değil, yalnızca yinelenenlere sahip fiziksel ölçüleri içerebilir.

Yapılandırma, toplam toplu çıkış miktarını elde etmek için ekleme veya çıkarma değiştiricilerini içeren hesaplanan ölçüm formülleri kümesi tanımlamanızı sağlar.

Özel hesaplanmış bir ölçü ayarlamak için şu adımları izleyin.

1. Power Apps ortamınızda oturum açın ve **Stok Görünürlüğü**'nü açın.
1. **Yapılandırma** sayfasını açın.
1. **Hesaplanan Ölçü** sekmesinde, hesaplanmış bir ölçü eklemek için **Yeni Hesaplanmış Ölçü**'yü seçin.
1. Yeni hesaplanan ölçü için aşağıdaki alanları ayarlayın:

    - **Yeni hesaplanan ölçü adı**: Hesaplanan ölçünün adını girin.
    - **Veri kaynağı**: Yeni hesaplanan ölçüyü ekleyeceğiniz veri kaynağını seçin. Sorgulama sistemi bir veri kaynağıdır.

1. Yeni hesaplanan ölçü için bir değiştirici eklemek üzere **Ekle**'yi seçin.
1. Yeni değiştirici için aşağıdaki alanları ayarlayın:

    - **Değiştirici**: Değiştirici türünü seçin (*Toplama* veya *Çıkarma*).
    - **Veri kaynağı**: Değiştirici değerini sağlayan ölçünün bulunması gereken veri kaynağını seçin.
    - **Ölçü**: Değiştirici için değer sağlayan ölçünün adını (seçilen veri kaynağından) seçin.

1. Hesaplanan ölçünüz için gerekli tüm değiştiricileri ekleyene ve formülü tamamlayana kadar 5 ile 6 adımları tekrarlayın.
1. **Kaydet**'i seçin.

Örneğin, bir moda şirketi üç veri kaynağıyla çalışmaktadır:

- `pos`- Mağaza kanalına karşılık gelir.
- `fno` - Supply Chain Management'a karşılık gelir.
- `ecommerce` – Web kanalınıza karşılık gelir.

Hesaplanmış ölçüler olmadan tesis 1, ambar 11 ve `ColorID` boyut değeri `Red` altında D0002 ürünü (Dolap) için sorgulama yaptığınızda, yapılandırılan her fiziksel ölçü altında stok miktarlarını gösteren aşağıdaki sorgu sonucunu alabilirsiniz. Ancak, veri kaynaklarınızın tamamında rezervasyon miktarları için kullanılabilir toplamı görmezsiniz.

```json
[
    {
        "productId": "D0002",
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
            "ecommerce": {
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
| `CrossChannel` | `MyCustomAvailableforReservation` | `fno` | `availphysical` | `Addition` |
| `CrossChannel` | `MyCustomAvailableforReservation` | `fno` | `orderedintotal` | `Addition` |
| `CrossChannel` | `MyCustomAvailableforReservation` | `fno` | `orderedreserved` | `Subtraction` |
| `CrossChannel` | `MyCustomAvailableforReservation` | `pos` | `inbound` | `Addition` |
| `CrossChannel` | `MyCustomAvailableforReservation` | `pos` | `outbound` | `Subtraction` |
| `CrossChannel` | `MyCustomAvailableforReservation` | `ecommerce` | `received` | `Addition` |
| `CrossChannel` | `MyCustomAvailableforReservation` | `ecommerce` | `scheduled` | `Addition` |
| `CrossChannel` | `MyCustomAvailableforReservation` | `ecommerce` | `issued` | `Subtraction` |
| `CrossChannel` | `MyCustomAvailableforReservation` | `ecommerce` | `reserved` | `Subtraction` |

Bu hesaplama formülü kullanıldığında, yeni sorgu sonucu özelleştirilmiş ölçümü içerir.

```json
[
    {
        "productId": "D0002",
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
            "ecommerce": {
                "received": 90.0,
                "scheduled": 30.0,
                "issued": 60.0,
                "reserved": 40.0
            },
            "CrossChannel": {
                "MyCustomAvailableforReservation": 220.0
            }
        }
    }
]
```

Özel ölçümlerdeki hesaplama ayarına göre `MyCustomAvailableforReservation` çıkışı 100 + 50 – 10 + 80 – 20 + 90 + 30 – 60 – 40 = 220'dir.

## <a name="partition-configuration"></a><a name="partition-configuration"></a>Bölüm yapılandırma

Şu anda bölüm yapılandırması, verilerin nasıl dağıtıldığını gösteren iki temel boyuttan (`SiteId` ve `LocationId`) oluşur. Aynı bölüm altındaki işlemler daha düşük maliyetle daha yüksek performans sağlayabilir. Aşağıdaki tabloda, Stok Görünürlüğü eklentisinin sağladığı varsayılan bölüm yapılandırması gösterilmiştir.

| Temel boyut | Hiyerarşi |
|---|---|
| `SiteId` | 1 |
| `LocationId` | 2 |

Çözüm varsayılan olarak bu bölüm yapılandırmasını içerir. Bu nedenle, *kendiniz tanımlamak zorunda değilsiniz*.

> [!IMPORTANT]
> Varsayılan bölüm yapılandırmasını özelleştirmeyin. Yapılandırmayı siler veya değiştirirseniz beklenmeyen bir hataya neden olabilirsiniz.

## <a name="product-index-hierarchy-configuration"></a><a name="index-configuration"></a>Ürün dizini hiyerarşisi yapılandırma

Çoğu zaman, eldeki stok sorgusu yalnızca en yüksek "toplam" düzeyinde olmaz. Bunun yerine, stok boyutlarına göre toplanan sonuçları da görmek isteyebilirsiniz.

Stok Görünürlüğü, sorgularınızın performansını artırmak için *dizinleri* ayarlamanıza izin vererek esneklik sağlar. Bu dizinler bir boyutu veya boyutların birleşimini temel alır. Bir dizin, aşağıdaki tabloda tanımlandığı gibi bir *küme numarası*, bir *boyut* ve bir *hiyerarşi*'den oluşur.

| Kuruluş adı | Tanım |
|---|---|
| Küme numarası | Aynı kümeye (dizin) ait boyutlar birlikte gruplanır ve bunlara aynı küme numarası atanır. |
| Boyut | Sorgu sonucunun toplandığı temel boyutlar. |
| Hiyerarşi | Hiyerarşi, filtre ve gruplandırma sorgusu parametrelerinde kullanıldığında, belirli boyut birleşimlerinin performansını artırmanıza olanak sağlar. Örneğin, bir boyut kümesini `(ColorId, SizeId, StyleId)` hiyerarşi sırasıyla ayarlarsanız sistem, dört boyut birleşimi ile ilgili sorguları daha hızlı işleyebilir. İlk birleşim boş, ikincisi `(ColorId)`, üçüncüsü `(ColorId, SizeId)` ve dördüncüsü `(ColorId, SizeId, StyleId)` birleşimidir. Diğer birleşimler hızlanmaz. Filtreler sıraya göre kısıtlanmaz, ancak performanslarını artırmak istiyorsanız bu boyutların içinde olması gerekir. Daha fazla bilgi için aşağıdaki örneğe bakın. |

Ürün hiyerarşi dizininizi ayarlamak için şu adımları izleyin.

1. Power Apps ortamınızda oturum açın ve **Stok Görünürlüğü**'nü açın.
1. **Yapılandırma** sayfasını açın.
1. **Ürün Hiyerarşi Dizini** sekmesinde, **Boyut Eşlemeleri** bölümünde, boyut eşlemeleri eklemek için **Ekle**'yi seçin.
1. Varsayılan olarak, dizinlerin bir listesi sağlanır. Var olan bir dizini değiştirmek için ilgili dizin bölümünde **Düzenle** veya **Ekle**'yi seçin. Yeni bir dizin kümesi oluşturmak için **Yeni dizin kümesi**'ni seçin. Her dizin kümesindeki her bir satır için **Boyut** alanında, temel boyutlar listesinden seçim yapın. Aşağıdaki alanlar için değerler otomatik olarak oluşturulur:

    - **Küme numarası**: Aynı kümeye (dizin) ait boyutlar birlikte gruplanır ve bunlara aynı küme numarası atanır.
    - **Hiyerarşi** – Hiyerarşi, filtre ve gruplandırma sorgusu parametrelerinde kullanıldığında, belirli boyut birleşimlerinin performansını artırır.

> [!TIP]
> Dizin hiyerarşinizi ayarlarken aklınızda tutmanız gereken birkaç ipucu:
>
> - Bölüm yapılandırmasında tanımlanan temel boyutlar, dizin yapılandırmalarında tanımlanmamalıdır. Dizin yapılandırmasındaki bir temel boyut tekrar tanımlanmışsa bu dizinle sorgu yapamazsınız.
> - Yalnızca tüm boyut kombinasyonları tarafından toplanan stoku sorgulamanız gerekiyorsa `Empty` temel boyutunu içeren tek bir dizin ayarlayın.

### <a name="example"></a>Örnek

Bu bölüm, hiyerarşinin nasıl çalıştığını gösteren bir örnek sağlar.

Aşağıdaki tabloda, bu örnek için kullanılabilir stokun bir listesi verilmiştir.

| Öğe | ColorId | SizeId | StyleId | Miktar |
|---|---|---|---|---|
| D0002 | Siyah | Küçük | Geniş | 1 |
| D0002 | Siyah | Küçük | Normal | 2 |
| D0002 | Siyah | Büyük | Geniş | 3 |
| D0002 | Siyah | Büyük | Normal | 4 |
| D0002 | Kırmızı | Küçük | Geniş | 5 |
| D0002 | Kırmızı | Küçük | Normal | 6 |
| D0002 | Kırmızı | Büyük | Normal | 7 |

Aşağıdaki tabloda, dizin hiyerarşisinin nasıl ayarlanacağı gösterilmektedir.

| Küme Numarası | Boyut | Hiyerarşi |
|---|---|---|
| 1 | `ColorId` | 1 |
| 1 | `SizeId` | 2 |
| 1 | `StyleId` | 3 |

Dizin, eldeki stoku aşağıdaki yollarla sorgulamanıza olanak tanır:

- `()`: Tümüne göre gruplandırılmıştır

    - D0002, 28

- `(ColorId)`: `ColorId`'ye göre gruplandırılmıştır

    - D0002, Siyah, 10
    - D0002, Kırmızı, 18

- `(ColorId, SizeId)`: `ColorId` ve `SizeId` birleşimine göre gruplandırılmıştır

    - D0002, Siyah, Small, 3
    - D0002, Siyah, Large, 7
    - D0002, Kırmızı, Small, 11
    - D0002, Kırmızı, Large, 7

- `(ColorId, SizeId, StyleId)`: `ColorId`, `SizeId` ve `StyleId` birleşimine göre gruplandırılmıştır

    - D0002, Siyah, Small, Geniş, 1
    - D0002, Siyah, Small, Normal, 2
    - D0002, Siyah, Large, Geniş, 3
    - D0002, Siyah, Large, Normal, 4
    - D0002, Kırmızı, Small, Geniş, 5
    - D0002, Kırmızı, Small, Normal, 6
    - D0002, Kırmızı, Large, Normal, 7

## <a name="reservation-configuration-optional"></a><a name="reservation-configuration"></a>Rezervasyon yapılandırma (isteğe bağlı)

Geçici rezervasyon özelliğini kullanmak istiyorsanız rezervasyon yapılandırması gereklidir. Yapılandırma iki temel bölümden oluşur:

- Geçici rezervasyon eşleme
- Geçici rezervasyon hiyerarşisi

### <a name="soft-reservation-mapping"></a>Geçici rezervasyon eşleme

Rezervasyon yaptığınızda, eldeki stokun şu anda rezervasyon için uygun olup olmadığını bilmek isteyebilirsiniz. Doğrulama, fiziksel ölçülerin bir birleşiminin bir hesaplama formülünü temsil eden hesaplanmış bir ölçüyle bağlantılıdır.

Fiziksel ölçüden hesaplanan ölçüye eşlemeyi ayarlayarak, Stok Görünürlüğü hizmetinin fiziksel ölçüye göre rezervasyon kullanılabilirliğini otomatik olarak doğrulamasını sağlarsınız.

Bu eşlemeyi ayarlamadan önce, fiziksel ölçüler, hesaplanmış ölçüler ve bunların veri kaynakları, Power Apps'te (bu makalede daha önce açıklandığı gibi) **Yapılandırma** sayfasının **Veri kaynağı** ve **Hesaplanan ölçü** sekmelerinde tanımlanmalıdır.

Geçici rezervasyon eşlemesini tanımlamak için şu adımları izleyin.

1. Geçici rezervasyon ölçüsü olarak hizmet eden fiziksel ölçüyü tanımlayın (örneğin, `SoftReservPhysical`).
1. **Yapılandırma** sayfasının **Hesaplanan ölçü** sekmesinde, fiziksel ölçüyle eşlemek istediğiniz AFR hesaplama formülünü içeren *rezerve edilebilir* (AFR) hesaplanmış ölçüyü tanımlayın. Örneğin, `AvailableToReserve`'i (rezerve edilebilir) önceden tanımlanmış `SoftReservPhysical` fiziksel ölçüsüyle eşlenecek şekilde ayarlayabilirsiniz. Bu şekilde, `SoftReservPhysical` stok durumuna sahip olan hangi miktarların rezerve edilebileceğini bulabilirsiniz. Aşağıdaki tabloda, AFR hesaplama formülü gösterilmektedir.

    | Hesaplama türü | Veri kaynağı | Fiziksel ölçü |
    |---|---|---|
    | Fark hesap eki | `fno` | `AvailPhysical` |
    | Fark hesap eki | `pos` | `Inbound` |
    | Çıkarma | `pos` | `Outbound` |
    | Çıkarma | `iv` | `SoftReservPhysical` |

    Hesaplanan ölçüyü, rezervasyon ölçüsünün temel aldığı fiziksel ölçüyü içerecek şekilde ayarlamanızı öneririz. Bu şekilde, hesaplanan ölçü miktarı rezervasyon ölçüsü miktarından etkilenir. Bu nedenle, bu örnekte `iv` veri kaynağının `AvailableToReserve` hesaplanan ölçüsü, bileşen olarak `iv` kaynağındaki `SoftReservPhysical` fiziksel ölçüsünü içermelidir.

1. **Yapılandırma** sayfasını açın.
1. **Geçici rezervasyon eşlemesi** sekmesinde, fiziksel ölçüden hesaplanan ölçüye eşlemeyi ayarlayın. Önceki örnek için `AvailableToReserve`'i önceden tanımlanmış `SoftReservPhysical` fiziksel ölçüsüyle eşleştirmek için aşağıdaki ayarları kullanabilirsiniz.

    | Fiziksel ölçü veri kaynağı | Fiziksel ölçü | Rezerve edilebilir veri kaynağı | Rezerve edilebilir hesaplanan ölçü |
    |---|---|---|---|
    | `iv` | `SoftReservPhysical` | `iv` | `AvailableToReserve` |

    > [!NOTE]
    > **Geçici Rezervasyon Eşleme** sekmesini düzenleyemiyorsanız **Özellik Yönetimi** sekmesinde *OnHandReservation* özelliğini açmanız gerekebilir.

Şimdi, `SoftReservPhysical` üzerinden rezervasyon yaptığınızda Stok Görünürlüğü, rezervasyon doğrulamasını yapmak için otomatik olarak `AvailableToReserve` ve ilgili hesaplama formülünü bulur.

Örneğin, Stok Görünürlüğü'nde aşağıdaki eldeki stoka sahipsiniz.

```json
{
    "productId": "D0002",
    "dimensions": {
        "SiteId": "1",
        "LocationId": "11",
        "ColorId": "Red"
    },
    "quantities": {
        "iv": {
            "SoftReservPhysical": 90
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

`AvailableToReserve` = `fno.availphysical` + `pos.inbound` – `pos.outbound` – `iv.SoftReservPhysical`  
= 70 + 50 – 20 – 90  
= 10

Bu nedenle, `iv.SoftReservPhysical` üzerinden rezervasyon yapmaya çalışırsanız ve miktar `AvailableToReserve` (10) değerinden küçük veya eşit geçici rezervasyon isteği başarılı olur.

> [!NOTE]
> Rezervasyon API'sini çağırdığınızda istek gövdesinde Boolean `ifCheckAvailForReserv` parametresini belirterek rezervasyon doğrulamasını denetleyebilirsiniz. `True` değeri doğrulamanın gerekli olduğu anlamına gelirken `False` değeri doğrulamanın gerekli olmadığı anlamına gelir (negatif `AvailableToReserve` miktarıyla sonuçlanacak olsa bile sistem yine de geçici rezervasyona izin verir). Varsayılan değer `True` değeridir.

### <a name="soft-reservation-hierarchy"></a>Geçici rezervasyon hiyerarşisi

Rezervasyon hiyerarşisi, rezervasyonlar yapıldığında belirtilmesi gereken boyutların sırasını açıklar. Ürün dizini hiyerarşisinin eldeki sorgular için çalıştığı şekilde çalışır.

Rezervasyon hiyerarşisi, ürün dizini hiyerarşisinden bağımsızdır. Bu bağımsızlık, kullanıcıların daha hassas rezervasyonlar yapmak için gereksinimleri belirtmek üzere boyutları bölebilecekleri kategori yönetimi uygulamalarına olanak tanır. Geçici rezervasyon hiyerarşiniz, bölüm yapılandırmasını oluşturduklarından bileşen olarak `SiteId` ve `LocationId` öğelerini içermelidir. Rezervasyon yaptığınızda ürün için bir bölüm belirtmeniz gerekir.

Aşağıda, bir geçici rezervasyon hiyerarşisi örneği verilmiştir.

| Temel boyut | Hiyerarşi |
|---|---|
| `SiteId` | 1 |
| `LocationId` | 2 |
| `ColorId` | 3 |
| `SizeId` | 4 |
| `StyleId` | 5 |

Bu örnekte, aşağıdaki boyut serilerinde rezervasyon yapabilirsiniz. Rezervasyon yaptığınızda ürün için bir bölüm belirtmeniz gerekir. Bu nedenle, kullanabileceğiniz temel hiyerarşi `(SiteId, LocationId)` öğesidir.

- `(SiteId, LocationId)`
- `(SiteId, LocationId, ColorId)`
- `(SiteId, LocationId, ColorId, SizeId)`
- `(SiteId, LocationId, ColorId, SizeId, StyleId)`

Geçerli bir boyut serisi, boyuta göre boyut rezervasyon hiyerarşisini kesinlikle izlemelidir. Örneğin, `(SiteId, LocationId, SizeId)` hiyerarşi sırası, `ColorId` eksik olduğundan geçerli değildir.

## <a name="available-to-promise-configuration-optional"></a>Karşılanabilir miktar yapılandırması (isteğe bağlı)

Gelecekteki eldeki değişiklikleri zamanlamanıza ve karşılanabilir (KM) miktarları hesaplamanıza olanak tanıyan Stok Görünürlüğü'nü ayarlayabilirsiniz. KM, mevcut bulunan ve sonraki dönemde müşteriye vaat edilebilecek bir maddenin miktarıdır. Bu hesaplamanın kullanımı, sipariş karşılama yeteneğinizi büyük ölçüde artırabilir. Bu özelliği kullanmak için **Özellik Yönetimi** sekmesinde etkinleştirmeniz ve ardından **KM Ayarı** sekmesinde ayarlamanız gerekir. Daha fazla bilgi için bkz. [Stok Görünürlüğü eldeki değişiklik zamanlamaları ve karşılanabilir miktarı](inventory-visibility-available-to-promise.md).

## <a name="complete-and-update-the-configuration"></a>Yapılandırmayı tamamlama ve güncelleştirme

Yapılandırmayı tamamladıktan sonra, Stok Görünürlüğü'nde tüm değişiklikleri uygulamalısınız. Değişiklikleri uygulamak için bu adımları izleyin.

1. Power Apps'te **'Yapılandırma** sayfasının sağ üst köşesinde **Yapılandırmayı Güncelleştir**'i seçin. 
1. Sistem oturum açma kimlik bilgileri ister. Aşağıdaki değerleri girin:

    - **İstemci Kimliği**: Stok Görünürlüğü için oluşturduğunuz Azure uygulaması kimliği.
    - **Kiracı kimliği**: Azure kiracısı kimliğiniz.
    - **İstemci Gizli Anahtarı**: Stok Görünürlüğü için oluşturduğunuz Azure uygulaması kimliği.

    Bu kimlik bilgileri ve bunların nasıl bulunacağı hakkında daha fazla bilgi için bkz. [Stok Görünürlüğü yükleme ve ayarlama](inventory-visibility-setup.md).

    > [!IMPORTANT]
    > Yapılandırmayı güncelleştirmeden önce veri kaynağı adınızı, fiziksel ölçülerinizi ve boyut eşlemelerinizi doğruladığınızdan emin olun. Yapılandırmayı güncelleştirdikten sonra bu ayarları değiştiremezsiniz.

1. Oturum açtıktan sonra **Yapılandırmayı Güncelleştir**'i seçin. Sistem ayarlarınızı uygular ve nelerin değiştiğini gösterir.

## <a name="default-configuration-sample"></a><a name="default-configuration-sample"></a>Varsayılan yapılandırma örneği

Stok Görünürlüğü, başlatma aşaması sırasında ayrıntıları burada verilen bir varsayılan yapılandırma ayarlar. Bu yapılandırmayı gerektiği şekilde değiştirebilirsiniz.

### <a name="data-source-configuration"></a>Veri kaynağı yapılandırma

#### <a name="configuration-of-the-iv-data-source"></a>iv veri kaynağını yapılandırma

Bu bölümde `iv` veri kaynağının nasıl yapılandırıldığı açıklanmaktadır.

##### <a name="physical-measures-configured-for-the-iv-data-source"></a>"iv" veri kaynağı için yapılandırılmış fiziksel ölçüler

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
| Ekleme | `fno` | `ReservPhysical` |
| Ekleme | `fno` | `ReservOrdered` |
| Ekleme | `iv` | `ReservPhysical` |
| Ekleme | `iv` | `ReservOrdered` |

#### <a name="configuration-of-the-fno-data-source"></a>"fno" veri kaynağını yapılandırma

Bu bölümde `fno` veri kaynağının nasıl yapılandırıldığı açıklanmaktadır.

##### <a name="dimension-mappings-for-the-fno-data-source"></a>"fno" veri kaynağı için boyut eşlemeleri

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

##### <a name="physical-measures-configured-for-the-fno-data-source"></a>"fno" veri kaynağı için yapılandırılmış fiziksel ölçüler

`fno` veri kaynağı için aşağıdaki fiziksel ölçüler yapılandırılmıştır:

- `Arrived`
- `PhysicalInvent`
- `ReservPhysical`
- `onorder`
- `notspecified`
- `availordered`
- `availphysical`
- `picked`
- `postedqty`
- `quotationreceipt`
- `received`
- `ordered`
- `ReservOrdered`

#### <a name="configuration-of-the-pos-data-source"></a>"pos" veri kaynağını yapılandırma

Bu bölümde `pos` veri kaynağının nasıl yapılandırıldığı açıklanmaktadır.

##### <a name="physical-measures-for-the-pos-data-source"></a>"pos" veri kaynağı için yapılandırılmış fiziksel ölçüler

`pos` veri kaynağı için aşağıdaki fiziksel ölçüler yapılandırılmıştır:

- `PosInbound`
- `PosOutbound`

##### <a name="availquantity-calculated-measure"></a>AvailQuantity hesaplanan ölçüsü

`AvailQuantity` hesaplanan ölçüsü, aşağıdaki tabloda gösterildiği gibi `pos` veri kaynağı için yapılandırılmıştır.

| Hesaplama türü | Veri kaynağı | Fiziksel ölçü |
|---|---|---|
| Ekleme | `fno` | `AvailPhysical` |
| Ekleme | `pos` | `PosInbound` |
| Çıkarma | `pos` | `PosOutbound` |

#### <a name="configuration-of-the-iom-data-source"></a>"iom" veri kaynağını yapılandırma

Aşağıdaki fiziksel ölçüler `iom` (akıllı sipariş yönetimi) veri kaynağı için yapılandırılmıştır:

- `OnOrder`
- `OnHand`

#### <a name="configuration-of-the-erp-data-source"></a>"erp" veri kaynağını yapılandırma

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

Aşağıdaki tabloda, varsayılan rezervasyon eşlemesi gösterilmektedir.

| Fiziksel ölçü veri kaynağı | Fiziksel ölçü | Rezerve edilebilir veri kaynağı | Rezerve edilebilir hesaplanan ölçü |
|---|---|---|---|
| `iv` | `SoftReservPhysical` | `iv` | `AvailableToReserve` |

#### <a name="reservation-hierarchy"></a>Rezervasyon hiyerarşisi

Aşağıdaki tabloda, varsayılan rezervasyon hiyerarşisi gösterilmektedir.

| Temel boyut | Hiyerarşi |
|---|---|
| `SiteId` | 1 |
| `LocationId` | 2 |
| `ColorId` | 3 |
| `SizeId` | 4 |

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
