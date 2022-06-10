---
title: Stok Görünürlüğü eldeki değişiklik zamanlamaları ve karşılanabilir miktarı
description: Bu konuda, gelecekteki eldeki değişikliklerin nasıl zamanlanacağı ve karşılanabilir miktarların (KM) nasıl hesaplanacağı açıklanmaktadır.
author: yufeihuang
ms.date: 05/11/2022
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yufeihuang
ms.search.validFrom: 2022-03-04
ms.dyn365.ops.version: 10.0.26
ms.openlocfilehash: 7456f87bede7bd0073223fa4762f96f919799e06
ms.sourcegitcommit: 38d97efafb66de298c3f504b83a5c9b822f5a62a
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/17/2022
ms.locfileid: "8763267"
---
# <a name="inventory-visibility-on-hand-change-schedules-and-available-to-promise"></a>Stok Görünürlüğü eldeki değişiklik zamanlamaları ve karşılanabilir miktarı

[!include [banner](../includes/banner.md)]

Bu konuda, gelecekteki eldeki değişiklikleri zamanlamak ve karşılanabilir miktarları (KM) hesaplamak için *Eldeki değişiklik zamanlaması* özelliğinin nasıl ayarlanacağı açıklanmaktadır. KM, mevcut bulunan ve sonraki dönemde müşteriye vaat edilebilecek bir maddenin miktarıdır. Bu hesaplamanın kullanımı, sipariş karşılama yeteneğinizi büyük ölçüde artırabilir.

Birçok üretici, perakendeci veya satıcı için şu anda eldeki stoğu bilmek yeterli değildir. Gelecekteki kullanılabilirliğe ilişkin tam görünürlüğe sahip olmaları da gerekir. Bu gelecekteki kullanılabilirlik için gelecekteki arz, gelecekteki talep ve KM dikkate alınmalıdır.

## <a name="enable-and-set-up-the-features"></a><a name="setup"></a>Özellikleri etkinleştirme ve ayarlama

KM'yi kullanabilmeniz için önce hesaplamak üzere bir veya daha fazla hesaplanan ölçü ayarlamanız gerekir. Ayrıca Microsoft Power Apps'te özelliği açmanız ve KM ayarlarını yapılandırmanız da gerekir.

### <a name="set-up-calculated-measures-for-atp-quantities"></a>KM için hesaplanan ölçüler ayarlama

*KM hesaplanan ölçüsü* genellikle mevcut kullanılabilir eldeki miktarı bulmak için kullanılan önceden tanımlanmış hesaplanan ölçüdür. *Arz miktarı*, *ekleme* niteleyici türüne sahip fiziksel ölçülerin miktarlarının toplamıdır. *Talep miktarı* ise *çıkarma* niteleyici türüne sahip fiziksel ölçülerin miktarlarının toplamıdır.

Birden çok KM miktarını hesaplamak için birden çok hesaplanan ölçü ekleyebilirsiniz. Ancak tüm KM hesaplanan ölçülerinde ayrı fiziksel ölçülerin toplam sayısı dokuzdan az olmalıdır.

> [!IMPORTANT]
> Hesaplanan ölçü fiziksel ölçülerin birleşimidir. Formülü hesaplanan ölçüler değil, yalnızca yinelenenlere sahip fiziksel ölçüleri içerebilir.

Örneğin, aşağıdaki hesaplanan ölçüyü ayarlayabilirsiniz:

**Eldeki kullanılabilir** = (*PhysicalInvent* + *OnHand* + *Kısıtlamasız* + *QualityInspection* + *Gelen*) – (*ReservPhysical* + *SoftReservePhysical* + *Giden*)

Toplam (*PhysicalInvent* + *OnHand* + *Kısıtlamasız* + *QualityInspection* + *Gelen*), arzı temsil eder ve toplam (*ReservPhysical* + *SoftReservePhysical* + *Giden*), talebi temsil eder. Böylece hesaplanan ölçü aşağıdaki şekilde anlaşılabilir:

**Eldeki kullanılabilir** = *Arz* - *Talep*

**Eldeki fiziksel miktar** KM miktarını hesaplamak için başka bir hesaplanan ölçü ekleyebilirsiniz.

**Eldeki fiziksel miktar** = (*PhysicalInvent* + *OnHand* + *Unrestricted* + *QualityInspection* + *Inbound*) – (*Outbound*)

Bu iki KM hesaplanan ölçüsü genelinde sekiz farklı fiziksel ölçü vardır: *PhysicalInvent*, *OnHand*, *Unrestricted*, *QualityInspection*, *Inbound*, *ReservPhysical*, *SoftReservePhysical* ve *Outbound*.

Hesaplanan ölçüler hakkında daha fazla bilgi için bkz. [Hesaplanan ölçüler](inventory-visibility-configuration.md#calculated-measures).

### <a name="turn-on-the-on-hand-change-schedule-feature-and-configure-atp-settings"></a>Eldeki değişiklik zamanlaması özelliğini açma ve KM ayarlarını yapılandırma

Power Apps'te *Eldeki değişiklik zamanlaması* özelliğini açmak ve KM ayarlarını yapılandırmak için bu adımları izleyin.

1. Power Apps'te oturum açın ve Stok Görünürlüğü'nü açın.
1. **Yapılandırma** sayfasını açın.
1. **Özellik Yönetimi** sekmesinde, *OnhandChangeSchedule* özelliğini açın.
1. **KM Ayarı** sekmesini seçin.
1. Stok Görünürlüğü'nü sorguladığınızda buraya eklediğiniz her KM hesaplanan ölçüsünü içeren bir sonuç sağlanır. KM için yeni bir hesaplanan ölçü eklemek üzere **Ekle**'yi seçin.
1. Aşağıdaki alanları ayarlayın:

    - **Veri Kaynağı**: Hesaplanan ölçü ile ilişkili olan veri kaynağını seçin.
    - **Hesaplanan Ölçü**: Seçilen veri kaynağıyla ilişkili olan ve mevcut kullanılabilir eldeki miktarı bulmak için kullanmak istediğiniz hesaplanan ölçüyü seçin.
    - **Zamanlama Dönemi**: Seçilen hesaplanan ölçü kullanıldığında kullanıcıların zamanlanan eldeki değişiklikleri görüntüleyip gönderebileceği gün sayısını girin. Stok bilgilerini sorgulayan kullanıcılar, geçerli tarihten itibaren bu dönemde her gün için eldeki miktarı, zamanlanan eldeki değişiklikleri ve KM'yi elde eder. 1 ile 7 arasında bir tamsayı seçin.

    > [!IMPORTANT]
    > Zamanlama dönemi, geçerli tarihi içerir. Bu nedenle kullanıcılar, geçerli tarihten (değişikliğin gönderildiği gün) gelecekteki (zamanlama dönemi - 1) güne kadar herhangi bir zamanda gerçekleşecek eldeki değişiklikleri zamanlayabilir.

1. **Kaydet**'i seçin.
1. KM için gereken tüm hesaplanan ölçüleri ekleyene kadar 5 ila 7. adımları tekrarlayın.
1. Gerekli tüm ayarları yapılandırmayı tamamladığınızda **Yapılandırmayı Güncelleştir**'i seçin.

Daha fazla bilgi için bkz. [Yapılandırmayı tamamlama ve güncelleştirme](inventory-visibility-configuration.md).

## <a name="how-the-on-hand-change-schedule-and-atp-calculations-work"></a>Eldeki değişiklik zamanlaması ve KM hesaplamaları nasıl çalışır?

*Eldeki değişiklik zamanlaması*, zamanlanan eldeki değişikliklerin beklenen tarihlerini ve miktarlarını belirler. Tarihlerin **Zamanlama dönemi** ayarı tarafından tanımlanan dönem içinde olması şartıyla Stok Görünürlüğü için bir eldeki değişiklik zamanlaması gönderebilirsiniz ([Özellikleri etkinleştirme ve ayarlama](#setup) bölümüne bakın). Stok bilgilerini sorgulayan kullanıcılar, bu dönemde her gün için eldeki miktarı, zamanlanan eldeki değişiklikleri ve KM'yi elde eder.

Zamanlanan değişiklikler başlangıçta kaydedilmez ve bu nedenle sistemdeki gerçek eldeki miktarlarınızı etkilemez. Değişiklikleri kaydetmek için gerçek kullanılabilir eldeki miktarı güncelleştiren bir *eldeki değişiklik olayı* göndermeniz gerekir. Ardından, eşleşen negatif miktar için bir eldeki değişiklik zamanlaması göndererek zamanlanan değişikliği geri almanız gerekir.

Örneğin, 10 bisiklet siparişi verdiniz ve ertesi gün gelmesini bekliyorsunuz. Bu nedenle, gelen miktarı 10 ve tarihi ertesi gün olan bir eldeki değişiklik zamanlaması gönderirsiniz. Sipariş ertesi gün ulaştığında bisikletleri fiziksel eldeki stoğa eklersiniz. Ardından, gerçek eldeki miktarı güncelleştirmek için değişikliği sisteminize yüklemeniz gerekir. Değişikliği kaydetmek için gelen miktarı 10 olan bir eldeki değişiklik olayı gönderirsiniz. Ardından, gelen miktarı -10 olan bir eldeki değişiklik zamanlaması göndererek zamanlanan değişikliği geri alırsınız.

Eldeki miktar ve KM için Stok Görünürlüğü'nü sorguladığınızda zamanlama dönemindeki her gün için aşağıdaki bilgiler döndürülür:

- **Tarih**: Sonucun geçerli olduğu tarih. Saat dilimi Eşgüdümlü Evrensel Saat'tir (UTC).
- **Eldeki miktar**: Belirtilen tarih için gerçek eldeki miktar. Bu hesaplama, Stok Görünürlüğü için yapılandırılan KM hesaplanan ölçüsüne göre yapılır.
- **Zamanlanan arz**: Belirtilen tarih itibarıyla hemen tüketim veya sevkiyat için fiziksel olarak kullanılabilir hale gelmeyen tüm zamanlanan gelen miktarların toplamı.
- **Zamanlanan talep**: Belirtilen tarih itibarıyla tüketilmeyen veya sevk edilmeyen tüm zamanlanan giden miktarların toplamı.
- **KM**: Belirtilen tarihten zamanlama döneminin sonuna kadar kullanılabilen minimum tahmini eldeki miktar. Bu miktar, tüm zamanlanan miktar ayarlamalarını içerir. Bu günde teslim veya tüketim için geçerli tarihte vaat edilebilecek maksimum miktardır.

Örneğin, geçerli tarih 1 Şubat 2022 ve zamanlama dönemi 7 ise kullanıcılar 1 Şubat 2022'den 7 Şubat 2022'ye kadar gerçekleşmesi beklenen zamanlanan eldeki değişiklikleri gönderebilir. Bu durumda, örneğin 3 Şubat için KM, bu gün için eldeki miktar ve 3 Şubat'tan 7 Şubat'a kadar zamanlanan miktarlar temel alınarak hesaplanır.

## <a name="example"></a>Örnek

Aşağıdaki örnekte, bir dizi zamanlanan miktar değişikliğinin Stok Görünürlüğü'nde raporlanan eldeki miktarı ve KM'yi nasıl etkilediği gösterilmektedir. Ayrıca, zamanlanan değişikliğin nasıl kaydedileceği, kaydedilen zamanlama değişikliğinin sonuçları nasıl etkilediği ve zamanlanan değişiklik kaydetmezseniz neler olabileceği de gösterilmektedir.

Bu örnekte sonuçlarda bir *tahmini eldeki* değer gösterilmektedir. Bu değer, gösterim amacıyla tüm zamanlanan güncelleştirmeleri içerir ancak Stok Görünürlüğü'nü sorguladığınızda gerçekten raporlanmaz.

1. Aşağıdaki ayarlar, Power Apps'te **KM ayarı** sayfasında sisteminiz için yapılandırılır:

    - **KM hesaplanan ölçüsü**: *Eldeki* olarak adlandırılan bir hesaplanan ölçünüz vardır. Bu, *Eldeki = Arz - Talep* olarak hesaplanır. Burada bu ölçüyü seçersiniz.
    - **Zamanlama dönemi**: *7*'yi seçersiniz.

1. Aşağıdaki koşullar da geçerlidir:

    - Geçerli tarih 1 Şubat 2022'dir.
    - Geçerli eldeki miktar 20'dir.

1. Geçerli tarih (1 Şubat 2022) için zamanlanan talep miktarı olarak 3'ü Stok Görünürlüğü'ne gönderirsiniz. Böylece tahmini eldeki miktar 17 olur. Aşağıdaki tabloda sonuç gösterilmektedir.

    | Tarih | Eldeki | Zamanlanan arz | Zamanlanan talep | Tahmini eldeki | KM |
    | --- | --- | --- | --- | --- | --- |
    | 2022-02-01 | 20 | | 3 | 17 | 17 |
    | 2022-02-02 | 20 | | | 17 | 17 |
    | 2022-02-03 | 20 | | | 17 | 17 |
    | 2022-02-04 | 20 | | | 17 | 17 |
    | 2022-02-05 | 20 | | | 17 | 17 |
    | 2022-02-06 | 20 | | | 17 | 17 |
    | 2022-02-07 | 20 | | | 17 | 17 |

1. Geçerli tarihte (1 Şubat 2022), 3 Şubat 2022 için zamanlanan arz miktarı olarak 10'u gönderirsiniz. Aşağıdaki tabloda sonuç gösterilmektedir.

    | Tarih | Eldeki | Zamanlanan arz | Zamanlanan talep | Tahmini eldeki | KM |
    | --- | --- | --- | --- | --- | --- |
    | 2022-02-01 | 20 | | 3 | 17 | 17 |
    | 2022-02-02 | 20 | | | 17 | 17 |
    | 2022-02-03 | 20 | 10 | | 27 | 27 |
    | 2022-02-04 | 20 | | | 27 | 27 |
    | 2022-02-05 | 20 | | | 27 | 27 |
    | 2022-02-06 | 20 | | | 27 | 27 |
    | 2022-02-07 | 20 | | | 27 | 27 |

1. Geçerli tarihte (1 Şubat 2022), aşağıdaki zamanlanan miktar değişikliklerini gönderirsiniz:

    - 4 Şubat 2022 için talep miktarı olarak 15
    - 5 Şubat 2022 için arz miktarı olarak 1
    - 6 Şubat 2022 için arz miktarı olarak 3

    Aşağıdaki tabloda sonuç gösterilmektedir.

    | Tarih | Eldeki | Zamanlanan arz | Zamanlanan talep | Tahmini eldeki | KM |
    | --- | --- | --- | --- | --- | --- |
    | 2022-02-01 | 20 | | 3 | 17 | 12 |
    | 2022-02-02 | 20 | | | 17 | 12 |
    | 2022-02-03 | 20 | 10 | | 27 | 12 |
    | 2022-02-04 | 20 | | 15 | 12 | 12 |
    | 2022-02-05 | 20 | 1 | | 13 | 13 |
    | 2022-02-06 | 20 | 3 | | 16 | 16 |
    | 2022-02-07 | 20 | | | 16 | 16 |

1. Geçerli tarihte (1 Şubat 2022), zamanlanan talep miktarı olarak 3'ü sevk edersiniz: Bu nedenle, bu değişikliği gerçek eldeki miktarınızda yansıtılacak şekilde kaydetmeniz gerekir. Değişikliği kaydetmek için giden miktarı 3 olan bir eldeki değişiklik olayı gönderirsiniz. Ardından, giden miktarı -3 olan bir eldeki değişiklik zamanlaması göndererek zamanlanan değişikliği geri alırsınız. Aşağıdaki tabloda sonuç gösterilmektedir.

    | Tarih | Eldeki | Zamanlanan arz | Zamanlanan talep | Tahmini eldeki | KM |
    | --- | --- | --- | --- | --- | --- |
    | 2022-02-01 | 17 | | 0 | 17 | 12 |
    | 2022-02-02 | 17 | | | 17 | 12 |
    | 2022-02-03 | 17 | 10 | | 27 | 12 |
    | 2022-02-04 | 17 | | 15 | 12 | 12 |
    | 2022-02-05 | 17 | 1 | | 13 | 13 |
    | 2022-02-06 | 17 | 3 | | 16 | 16 |
    | 2022-02-07 | 17 | | | 16 | 16 |

1. Sonraki gün (2 Şubat 2022), zamanlama dönemi bir gün ileri kayar. Aşağıdaki tabloda sonuç gösterilmektedir.

    | Tarih | Eldeki | Zamanlanan arz | Zamanlanan talep | Tahmini eldeki | KM |
    | --- | --- | --- | --- | --- | --- |
    | 2022-02-02 | 17 | | | 17 | 12 |
    | 2022-02-03 | 17 | 10 | | 27 | 12 |
    | 2022-02-04 | 17 | | 15 | 12 | 12 |
    | 2022-02-05 | 17 | 1 | | 13 | 13 |
    | 2022-02-06 | 17 | 3 | | 16 | 16 |
    | 2022-02-07 | 17 | | | 16 | 16 |
    | 2022-02-08 | 17 | | | 16 | 16 |

1. Ancak iki gün sonra (4 Şubat 2022), 3 Şubat için zamanlanan arz miktarı olarak 10 hâlâ gelmemiştir. Aşağıdaki tabloda sonuç gösterilmektedir.

    | Tarih | Eldeki | Zamanlanan arz | Zamanlanan talep | Tahmini eldeki | KM |
    | --- | --- | --- | --- | --- | --- |
    | 2022-02-04 | 17 | | 15 | 2 | 2 |
    | 2022-02-05 | 17 | 1 | | 3 | 3 |
    | 2022-02-06 | 17 | 3 | | 6 | 6 |
    | 2022-02-07 | 17 | | | 6 | 6 |
    | 2022-02-08 | 17 | | | 6 | 6 |
    | 2022-02-09 | 17 | | | 6 | 6 |
    | 2022-02-10 | 17 | | | 6 | 6 |

    Gördüğünüz gibi, zamanlanan (ancak kaydedilmeyen) eldeki değişiklikler gerçek eldeki miktarı etkilemez.

## <a name="submit-change-schedules-change-events-and-atp-queries-through-the-api"></a><a name="api-urls"></a>API üzerinden değişiklik zamanlamaları, değişiklik olayları ve KM sorguları gönderme

Eldeki değişiklik zamanlamaları, değişiklik olayları ve sorgular göndermek için aşağıdaki uygulama programlama arabirimi (API) URL'lerini kullanabilirsiniz.

| Yol | Yöntem | Açıklama |
| --- | --- | --- |
| `/api/environment/{environmentId}/onhand/changeschedule` | `POST` | Bir zamanlanan eldeki değişiklik oluşturun. |
| `/api/environment/{environmentId}/onhand/changeschedule/bulk` | `POST` | Birden fazla zamanlanan eldeki değişiklik oluşturun. |
| `/api/environment/{environmentId}/onhand` | `POST` | Eldeki değişiklik olayı oluşturun. |
| `/api/environment/{environmentId}/onhand/bulk` | `POST` | Birden fazla değişiklik olayı oluşturun. |
| `/api/environment/{environmentId}/onhand/indexquery` | `POST` | `POST` yöntemini kullanarak sorgulayın. |
| `/api/environment/{environmentId}/onhand` | `GET` | `GET` yöntemini kullanarak sorgulayın. |

Daha fazla bilgi için bkz. [Stok Görünürlüğü genel API'leri](inventory-visibility-api.md).

### <a name="create-one-on-hand-change-schedule"></a>Eldeki stok değişikliği zamanlaması oluşturma

Eldeki stok değişikliği zamanlaması, ilgili Stok Görünürlüğü hizmeti URL'sine bir `POST` isteği göndererek oluşturulur ([API üzerinden değişiklik zamanlamaları, değişiklik olayları ve KM sorguları gönderme](#api-urls) bölümüne bakın). Ayrıca toplu istekler de gönderebilirsiniz.

Eldeki stok değişikliği zamanlaması, yalnızca zamanlanan tarihin geçerli tarih ile geçerli zamanlama döneminin sonu arasında olması koşuluyla oluşturulabilir. Tarih saat biçimi *yıl-ay-gün* (ör. **2022-02-01**) biçiminde olmalıdır. Saat biçimi yalnızca ilgili gün için doğru olmalıdır.

Bu API, tek bir eldeki stok değişikliği zamanlaması oluşturur.

```txt
Path:
    /api/environment/{environmentId}/onhand/changeschedule
Method:
    Post
Headers:
    Api-Version="1.0"
    Authorization="Bearer $access_token"
ContentType:
    application/json
Body:
    {
        id: string,
        organizationId: string,
        productId: string,
        dimensionDataSource: string, # optional
        dimensions: {
            [key:string]: string,
        },
        quantitiesByDate: {
            [datetime:datetime]: {
                [dataSourceName:string]: {
                    [key:string]: number,
                },
            },
        },
    }
```

Aşağıdaki örnekte, `dimensionDataSource` olmadan örnek gövde içeriği gösterilmektedir.

```json
{
    "id": "id-bike-0001",
    "organizationId": "usmf",
    "productId": "Bike",
    "dimensions": {
        "SiteId": "1",
        "LocationId": "11",
        "ColorId": "Red",
        "SizeId&quot;: &quot;Small"
    },
    "quantitiesByDate":
    {
        "2022-02-01": // today
        {
            "pos":{
                "inbound": 10
            }
        }
    }
}
```

### <a name="create-multiple-on-hand-change-schedules"></a>Birden fazla eldeki stok değişikliği zamanlaması oluşturma

Bu API aynı anda birden çok kayıt oluşturabilir. Bu API ile tek olay API'si arasındaki tek fark, `Path` ve `Body` değerleridir. Bu API için `Body` bir dizi kayıt sağlar. Maksimum kayıt sayısı 512'dir. Bu nedenle, eldeki stok değişikliği zamanlaması toplu API'si tek seferde 512 adede kadar zamanlanan değişikliği destekleyebilir.

```txt
Path:
    /api/environment/{environmentId}/onhand/changeschedule/bulk
Method:
    Post
Headers:
    Api-Version="1.0"
    Authorization="Bearer $access_token"
ContentType:
    application/json
Body:
    [
        {
            id: string,
            organizationId: string,
            productId: string,
            dimensionDataSource: string,
            dimensions: {
                [key:string]: string,
            },
            quantityDataSource: string, # optional
            quantitiesByDate: {
                [datetime:datetime]: {
                    [dataSourceName:string]: {
                        [key:string]: number,
                    },
                },
            },
        },
        ...
    ]
```

Aşağıdaki örnekte, örnek gövde içeriği gösterilmektedir.

```json
[
    {
        "id": "id-bike-0001",
        "organizationId": "usmf",
        "productId": "Bike",
        "dimensions": {
            "SiteId": "1",
            "LocationId": "11",
            "ColorId": "Red",
            "SizeId&quot;: &quot;Small"
        },
        "quantitiesByDate":
        {
            "2022-02-01": // today
            {
                "pos":{
                    "inbound": 10
                }
            }
        }
    },
    {
        "id": "id-car-0002",
        "organizationId": "usmf",
        "productId": "Car",
        "dimensions": {
            "SiteId": "1",
            "LocationId": "11",
            "ColorId": "Red",
            "SizeId&quot;: &quot;Small"
        },
        "quantitiesByDate":
        {
            "2022-02-05":
            {
                "pos":{
                    "outbound": 10
                }
            }
        }
    }
]
```

### <a name="create-on-hand-change-events"></a>Eldeki değişiklik olayları oluşturma

Eldeki değişiklik olayları, ilgili Stok Görünürlüğü hizmeti URL'sine bir `POST` isteği göndererek yapılır ([API üzerinden değişiklik zamanlamaları, değişiklik olayları ve KM sorguları gönderme](#api-urls) bölümüne bakın). Ayrıca toplu istekler de gönderebilirsiniz.

> [!NOTE]
> Eldeki değişiklik olayları, KM işlevine özgü değildir ancak standart Stok Görünürlüğü API'sinin parçasıdır. Olaylar KM ile çalışmanızla ilgili olduğundan bu örnek eklenmiştir. Eldeki değişiklik olayları, eldeki değişiklik rezervasyonlarına benzer ancak olay iletilerinin farklı bir API URL'sine gönderilmesi gerekir ve olaylarda, ileti gövdesinde `quantityByDate` yerine `quantities` kullanılır. Eldeki değişiklik olayları ve Stok Görünürlüğü API'sinin diğer özellikleri hakkında daha fazla bilgi için bkz. [Stok Görünürlüğü genel API'leri](inventory-visibility-api.md#create-one-onhand-change-event).

Aşağıdaki örnekte, tek bir eldeki değişiklik olayı içeren istek gövdesi gösterilmektedir.

```json
{
    "id": "id-bike-0001",
    "organizationId": "usmf",
    "productId": "Bike",
    "dimensions": {
        "SiteId": "1",
        "LocationId": "11",
        "SizeId": "Big",
        "ColorId": "Red"
    },
    "quantities": {
        "pos": {
            "inbound": 10.0
        }
    }
}
```

## <a name="query-the-scheduled-on-hand-changes-and-atp-results"></a>Zamanlanan eldeki değişiklikleri ve KM sonuçlarını sorgulama

Uygun API URL'sine bir `POST` isteği veya `GET` isteği göndererek zamanlanan eldeki değişiklikleri ve KM sonuçlarını sorgulayabilirsiniz ([API üzerinden değişiklik zamanlamaları, değişiklik olayları ve KM sorguları gönderme](#api-urls) bölümüne bakın).

Zamanlanan eldeki değişiklikleri ve KM sonuçlarını sorgulamak isterseniz isteğinizde `QueryATP` parametresini *true* olarak ayarlayın.

- İsteği `GET` yöntemini kullanarak gönderiyorsanız URL'de bu parametreyi ayarlayın.
- İsteği `POST` yöntemini kullanarak gönderiyorsanız istek gövdesinde bu parametreyi ayarlayın.

> [!NOTE]
> İstek gövdesinde `returnNegative` parametresinin *true* veya *false* olarak ayarlanmasına bakılmaksızın, zamanlanan eldeki değerler ve KM sonuçları için sorgulama yaptığınızda sonuç negatif değerler içerir. Yalnızca talep siparişleri zamanlanırsa veya arz miktarları talep miktarlarından azsa zamanlanan eldeki değişiklik miktarları negatif olacağından bu negatif değerler dahil edilir. Negatif değerler dahil edilmediyse sonuçlar kafa karıştırıcı olur. Bu seçenek ve diğer sorgu türlerinin nasıl çalıştığı hakkında daha fazla bilgi için bkz. [Stok Görünürlüğü genel API'leri](inventory-visibility-api.md#query-with-post-method).

```txt
Path:
    /api/environment/{environmentId}/onhand/indexquery
Method:
    Post
Headers:
    Api-Version="1.0"
    Authorization="Bearer $access_token"
ContentType:
    application/json
Body:
    {
        dimensionDataSource: string, # Optional
        filters: {
            organizationId: string[],
            productId: string[],
            siteId: string[],
            locationId: string[],
            [dimensionKey:string]: string[],
        },
        groupByValues: string[],
        returnNegative: boolean,
    }
```

Aşağıdaki örnekte, `POST` yöntemini kullanarak Stok Görünürlüğü'ne gönderilebilen istek gövdesinin nasıl oluşturulacağı gösterilmektedir.

```json
{
    "filters": {
        "organizationId": ["usmf"],
        "productId": ["Bike"],
        "siteId": ["1"],
        "LocationId": ["11"]
    },
    "groupByValues": ["ColorId", "SizeId"],
    "returnNegative": true,
    "QueryATP":true
}
```

### <a name="get-method-example"></a>GET yöntemi örneği

```txt
Path:
    /api/environment/{environmentId}/onhand
Method:
    Get
Headers:
    Api-Version="1.0"
    Authorization="Bearer $access_token"
ContentType:
    application/json
Query(Url Parameters):
    groupBy
    returnNegative
    [Filters]
```

Aşağıdaki örnekte, `GET` isteği olarak istek URL'sinin nasıl oluşturulacağı gösterilmektedir.

```txt
https://inventoryservice.{RegionShortName}-il301.gateway.prod.island.powerapps.com/api/environment/{EnvironmentId}/onhand?organizationId=usmf&productId=Bike&SiteId=1&LocationId=11&groupBy=ColorId,SizeId&returnNegative=true&QueryATP=true
```

Bu `GET` isteğinin sonucu, önceki örnekteki `POST` isteğinin sonucuyla tam olarak aynıdır.

### <a name="query-result-example"></a>Sorgu sonucu örneği

Önceki sorgu örneklerinin ikisinde de aşağıdaki yanıt oluşabilir. Bu örnekte, sistem aşağıdaki ayarlarla yapılandırılır:

- **KM hesaplanan ölçüsü:** *iv.onhand = pos.inbound – pos.outbound*
- **Zamanlama dönemi:** *7*

Burada yanıt gövdesi için bir örnek yer almaktadır.

```json
[
    {
        "quantitiesByDate": {
            "2022-02-02T00:00:00": {
                "pos": {
                    "outbound": 5,
                    "inbound": 0,
                },
                "iv": {
                    "onhand": -5,
                },
            },
            "2022-02-06T00:00:00": {
                "pos": {
                    "inbound": 7,
                    "outbound": 0,
                },
                "iv": {
                    "onhand": 7,
                },
            }
        },
        "atpQuantities": {
            "2022-02-01T00:00:00Z": {
                "iv": {
                    "onhand": 5.0
                }
            },
            "2022-02-02T00:00:00Z": {
                "iv": {
                    "onhand": 5.0
                }
            },
            "2022-02-03T00:00:00Z": {
                "iv": {
                    "onhand": 5.0
                }
            },
            "2022-02-04T00:00:00Z": {
                "iv": {
                    "onhand": 5.0
                }
            },
            "2022-02-05T00:00:00Z": {
                "iv": {
                    "onhand": 5.0
                }
            },
            "2022-02-06T00:00:00Z": {
                "iv": {
                    "onhand": 12.0
                }
            },
            "2022-02-07T00:00:00Z": {
                "iv": {
                    "onhand": 12.0
                }
            }
        },
        "productId": "Bike ",
        "dimensions": {
            "ColorId": "Red",
            "SizeId": "Big",
            "siteid": "1",
            "locationid": "11"
        },
        "quantities": {
            "pos": {
                "inbound": 10.0,
                "outbound": 0,
            },
            "iv": {
                "onhand": 10.0,
            }
        }
    }
]
```
