---
title: Inventory Visibility genel API'leri
description: Bu makalede, Stok Görünürlüğü tarafından sağlanan genel API'ler açıklanmaktadır.
author: yufeihuang
ms.date: 11/04/2022
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yufeihuang
ms.search.validFrom: 2021-08-02
ms.dyn365.ops.version: 10.0.22
ms.openlocfilehash: 8b0b8ca261237fbb2190f2a94cc11b816ae05af5
ms.sourcegitcommit: 49f8973f0e121eac563876d50bfff00c55344360
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/14/2022
ms.locfileid: "9762847"
---
# <a name="inventory-visibility-public-apis"></a>Inventory Visibility genel API'leri

[!include [banner](../includes/banner.md)]

Bu makalede, Stok Görünürlüğü tarafından sağlanan genel API'ler açıklanmaktadır.

Stok Görünürlüğü Eklentisi'nin genel REST API'si, birkaç özel tümleştirme uç noktası sunar. Dört ana etkileşim türünü destekler:

- Harici bir sistemden eldeki stok değişiklikleri eklentiye deftere nakletmek
- Harici bir sistemden eklentide eldeki stok miktarlarını ayarlama veya geçersiz kılma
- Harici bir sistemden eklentiye rezervasyon olayları nakletme
- Harici bir sistemden eldeki geçerli miktarları sorgulamak

Aşağıdaki tabloda, şu anda kullanılabilen API'ler listelenmektedir:

| Yol | Yöntem | Tanım |
|---|---|---|
| /api/environment/{environmentId}/onhand | Naklet | [Eldeki değişiklik olayı oluşturma](#create-one-onhand-change-event)|
| /api/environment/{environmentId}/onhand/bulk | Naklet | [Birden fazla değişiklik olayı oluşturma](#create-multiple-onhand-change-events) |
| /api/environment/{environmentId}/setonhand/{inventorySystem}/bulk | Naklet | [Eldeki miktarları ayarlama/geçersiz kılma](#set-onhand-quantities) |
| /api/environment/{environmentId}/onhand/reserve | Deftere naklet | [Bir geçici rezervasyon olayı oluşturma](#create-one-reservation-event) |
| /api/environment/{environmentId}/onhand/reserve/bulk | Deftere naklet | [Birden çok geçici rezervasyon olayı oluşturma](#create-multiple-reservation-events) |
| /api/environment/{environmentId}/onhand/unreserve | Deftere naklet | [Bir geçici rezervasyon olayını tersine çevirme](#reverse-one-reservation-event) |
| /api/environment/{environmentId}/onhand/unreserve/bulk | Deftere naklet | [Birden çok geçici rezervasyon olayını tersine çevirme](#reverse-multiple-reservation-events) |
| /api/environment/{environmentId}/onhand/changeschedule | Deftere naklet | [Bir zamanlanan eldeki değişiklik oluşturma](inventory-visibility-available-to-promise.md) |
| /api/environment/{environmentId}/onhand/changeschedule/bulk | Deftere naklet | [Tarihlerle birden çok eldeki stok değişikliği oluşturma](inventory-visibility-available-to-promise.md) |
| /api/environment/{environmentId}/onhand/indexquery | Deftere naklet | [Post yöntemini kullanarak sorgulama](#query-with-post-method) (önerilir) |
| /api/environment/{environmentId}/onhand | Al | [Get yöntemini kullanarak sorgulama](#query-with-get-method) |
| /api/environment/{environmentId}/onhand/exactquery | Deftere naklet | [Post yöntemini kullanarak tam sorgulama](#exact-query-with-post-method) |
| /api/environment/{environmentId}/allocation<wbr>/allocate | Deftere naklet | [Bir tahsisat olayı oluşturma](inventory-visibility-allocation.md#using-allocation-api) |
| /api/environment/{environmentId}/allocation<wbr>/unallocate | Deftere naklet | [Bir tahsisattan kaldırma olayı oluşturma](inventory-visibility-allocation.md#using-allocation-api) |
| /api/environment/{environmentId}/allocation<wbr>/reallocate | Deftere naklet | [Bir yeniden tahsis etme olayı oluşturma](inventory-visibility-allocation.md#using-allocation-api) |
| /api/environment/{environmentId}/allocation<wbr>/consume | Deftere naklet | [Bir tüketme olayı oluşturma](inventory-visibility-allocation.md#using-allocation-api) |
| /api/environment/{environmentId}/allocation<wbr>/query | Deftere naklet | [Tahsisat sorgusu sonucu](inventory-visibility-allocation.md#using-allocation-api) |

> [!NOTE]
> Yolun {environmentId} bölümü, Microsoft Dynamics Lifecycle Services'teki ortam kimliğidir.
> 
> Toplu API, her istek için en fazla 512 kayıt döndürebilir.

Microsoft, hazır bir *Postman* istek koleksiyonu sağlamıştır. Şu paylaşılan bağlantıyı kullanarak bu koleksiyonu *Postman* yazılımınıza içeri aktarabilirsiniz: <https://www.getpostman.com/collections/95a57891aff1c5f2a7c2>.

## <a name="find-the-endpoint-according-to-your-lifecycle-services-environment"></a><a name = "endpoint-lcs"></a>Lifecycle Services ortamınıza göre uç noktayı bulma

Stok Görünürlüğü mikro hizmeti, birden çok coğrafya ve bölgede Microsoft Azure Service Fabric'te dağıtılır. Şu anda isteğinizi ilgili coğrafya ve bölgeye otomatik olarak yönlendirebilecek merkezi bir uç nokta bulunmamaktadır. Bu nedenle, aşağıdaki modeli kullanarak bilgi parçalarını bir URL'de oluşturmanız gerekir:

`https://inventoryservice.<RegionShortName>-il<IsLandNumber>.gateway.prod.island.powerapps.com`

Bölge kısa adı, Lifecycle Services ortamında bulunabilir. Aşağıdaki tabloda, şu anda kullanılabilen bölgeler listelenmektedir.

| Azure bölgesi        | Bölge kısa adı |
| ------------------- | ----------------- |
| Doğu Avustralya      | eau               |
| Güneydoğu Avustralya | seau              |
| Orta Kanada      | cca               |
| Doğu Kanada         | eca               |
| Kuzey Avrupa        | neu               |
| Batı Avrupa         | weu               |
| Doğu ABD             | eus               |
| Batı ABD             | wus               |
| Güney BK            | suk               |
| Batı BK             | wuk               |
| Doğu Japonya          | ejp               |
| Batı Japonya          | wjp               |
| Orta Hindistan       | cin               |
| Güney Hindistan         | sin               |
| Kuzey İsviçre   | nch               |
| Batı İsviçre    | wch               |
| Güney Fransa        | sfr               |
| Doğu Asya           | eas               |
| Güneydoğu Asya     | seas              |
| Kuzey BAE           | nae               |
| Doğu Norveç         | eno               |
| Batı Norveç         | wno               |
| Güney Afrika - Batı   | wza               |
| Güney Afrika - Kuzey  | nza               |

Ada numarası, Lifecycle Services ortamınızın Service Fabric'te dağıtıldığı yerdir. Şu anda bu bilgileri kullanıcı tarafından almanın yolu yoktur.

Microsoft, Power Apps'te bir kullanıcı arabirimi (UI) oluşturmuştur, böylece mikro hizmetin tam uç noktasını alabilirsiniz. Daha fazla bilgi için bkz. [Hizmet uç noktasını bulma](inventory-visibility-configuration.md#get-service-endpoint).

## <a name="authentication"></a><a name="inventory-visibility-authentication"></a>Kimlik Doğrulama

Platform güvenlik belirteci, Stok Görünürlüğü genel API'sini çağırmak için kullanılır. Bu nedenle, Azure AD uygulamanızı kullanarak bir *Azure Active Directory (Azure AD) belirteci* oluşturmanız gerekir. Daha sonra güvenlik hizmetinden *erişim belirtecini* almak için Azure AD belirteci kullanmanız gerekir.

Microsoft, kullanıma hazır bir *Postman* belirteç koleksiyonu sağlar. Şu paylaşılan bağlantıyı kullanarak bu koleksiyonu *Postman* yazılımınıza içeri aktarabilirsiniz: <https://www.getpostman.com/collections/496645018f96b3f0455e>.

Güvenlik hizmeti belirteci almak için aşağıdaki adımları izleyin.

1. Azure portalda oturum açın ve bu portalı kullanarak Dynamics 365 Supply Chain Management uygulamanız için `clientId` ve `clientSecret` değerlerini bulun.
1. Aşağıdaki özelliklere sahip bir HTTP isteği göndererek Azure AD belirteci (`aadToken`) getirin:

    - **URL:** `https://login.microsoftonline.com/${aadTenantId}/oauth2/v2.0/token`
    - **Yöntem:** `GET`
    - **Gövde içeriği (form verileri):**

        | Anahtar           | Değer                                            |
        | ------------- | -------------------------------------------------|
        | client_id     | ${aadAppId}                                      |
        | client_secret | ${aadAppSecret}                                  |
        | grant_type    | client_credentials                               |
        | kapsam         | 0cdb527f-a8d1-4bf8-9436-b352c68682b2/.default    |

    Yanıtta bir Azure AD belirteci (`aadToken`) almanız gerekir. Bu etiket, aşağıdaki örneğe benzeyecektir.

    ```json
    {
        "token_type": "Bearer",
        "expires_in": "3599",
        "ext_expires_in": "3599",
        "access_token": "eyJ0eX...8WQ"
    }
    ```

1. Aşağıdaki örneğe benzer bir JavaScript Nesne Gösterimi (JSON) isteği düzenleyin.

    ```json
    {
        "grant_type": "client_credentials",
        "client_assertion_type": "aad_app",
        "client_assertion": "{Your_AADToken}",
        "scope": "https://inventoryservice.operations365.dynamics.com/.default",
        "context": "{$LCS_environment_id}",
        "context_type": "finops-env"
    }
    ```

    Aaşağıdaki noktaları unutmayın:

    - `client_assertion` değeri, önceki adımda aldığınız Azure AD belirteci (`aadToken`) olmalıdır.
    - `context` değeri, eklentiyi dağıtmak istediğiniz Lifecycle Services ortam kimliği olmalıdır.
    - Diğer tüm değerleri örnekte gösterildiği gibi ayarlayın.

1. Aşağıdaki özelliklere sahip bir HTTP isteği göndererek erişim belirteci (`access_token`) getirin:

    - **URL:** `https://securityservice.operations365.dynamics.com/token`
    - **Yöntem:** `POST`
    - **HTTP üst bilgisi:** API sürümünü ekleyin. (Anahtar `Api-Version` ve değer `1.0`.)
    - **Gövde içeriği:** Önceki adımda oluşturduğunuz JSON isteğini ekleyin.

    Yanıtta bir erişim belirteci (`access_token`) almanız gerekir. Stok Görünürlüğü API'sini çağırmak için taşıyıcı belirteç olarak bu belirteci kullanmanız gerekir. Aşağıda bir örnek verilmiştir.

    ```json
    {
        "access_token": "{Returned_Token}",
        "token_type": "bearer",
        "expires_in": 3600
    }
    ```

> [!IMPORTANT]
> Stok Görünürlüğü genel API'lerini çağırmak için *Postman* istek koleksiyonunu kullandığınızda her istek için bir taşıyıcı belirteci eklemelisiniz. Taşıyıcı belirtecinizi bulmak için istek URL'sinin altındaki **Yetkilendirme** sekmesini seçin, **Taşıyıcı Belirteci** türünü seçin ve son adımda getirilen erişim belirtecini kopyalayın. Bu makalenin sonraki bölümlerinde son adımda getirilen belirteci temsil etmek için `$access_token` kullanılacaktır.

## <a name="create-on-hand-change-events"></a><a name="create-onhand-change-event"></a>Eldeki değişiklik olayları oluşturma

Eldeki değişiklik olayları oluşturmak için iki API vardır:

- Bir kayıt oluşturun: `/api/environment/{environmentId}/onhand`
- Birden çok kayıt oluşturun: `/api/environment/{environmentId}/onhand/bulk`

Aşağıdaki tabloda, JSON gövdesindeki her bir alanın anlamı özetlenmektedir.

| Alan kodu | Açıklama |
|---|---|
| `id` | Belirli bir değişiklik olayı için benzersiz bir kimlik. Bir hizmet hatası nedeniyle yeniden gönderim meydana gelirse bu kimlik, aynı olayın sistemde iki kez sayılmamasını sağlamak için kullanılır. |
| `organizationId` | Olayla bağlantılı kuruluşun tanımlayıcısı. Bu değer, Supply Chain Management'ta bir kuruluş veya veri alanı kimliğiyle eşlenir. |
| `productId` | Ürünün tanımlayıcısı. |
| `quantities` | Eldeki miktarın değiştirilmesi gereken miktar. Örneğin, bir rafa 10 yeni kitap eklenirse bu değer `quantities:{ shelf:{ received: 10 }}` olur. Üç kitap raftan kaldırılırsa veya satılırsa bu değer `quantities:{ shelf:{ sold: 3 }}` olur. |
| `dimensionDataSource` | Deftere nakil değişikliği olayı ve sorgusunda kullanılan boyutların veri kaynağı. Veri kaynağını belirtirseniz belirtilen veri kaynağındaki özel boyutları kullanabilirsiniz. Stok Görünürlüğü, özel boyutları genel varsayılan boyutlarla eşleştirmek için boyut yapılandırmasını kullanır. `dimensionDataSource` değeri belirtilmezse sorgularınızda yalnızca [temel boyutları](inventory-visibility-configuration.md#data-source-configuration-dimension) kullanabilirsiniz. |
| `dimensions` | Dinamik bir anahtar-değer çifti. Değerler, Supply Chain Management'ta bazı boyutlarla eşleştirilir. Ancak olayın Supply Chain Management'tan veya harici bir sistemden geldiğini belirtmek için özel boyutlar da (örneğin, *Kaynak*) ekleyebilirsiniz. |

> [!NOTE]
> `siteId` ve `locationId` parametreleri [bölüm yapılandırmasını](inventory-visibility-configuration.md#partition-configuration) oluşturur. Bu nedenle, eldeki değişiklik olayları oluşturduğunuzda, eldeki miktarları ayarladığınızda veya geçersiz kıldığınızda ya da rezervasyon olayları oluşturduğunuzda bunları boyutlarda belirtmeniz gerekir.

Aşağıdaki alt bölümlerde bu API'lerin nasıl kullanıldığını gösteren örnekler verilmektedir.

### <a name="create-one-on-hand-change-event"></a><a name="create-one-onhand-change-event"></a>Eldeki değişiklik olayı oluşturma

Bu API, tek bir eldeki değişiklik olayı oluşturur.

```txt
Path:
    /api/environment/{environmentId}/onhand
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
        dimensionDataSource: string, # Optional
        dimensions: {
            [key:string]: string,
        },
        quantities: {
            [dataSourceName:string]: {
                [key:string]: number,
            },
        },
    }
```

Aşağıdaki örnekte, örnek gövde içeriği gösterilmektedir. Bu örnekte, şirket mağaza içi hareketleri ve stok değişikliklerini işleyen bir satış noktası (POS) sistemine sahiptir. Müşteri, kırmızı bir tişörtü mağazanıza iade etti. Değişikliği yansıtmak için *Tişört* ürünü için tek bir değişiklik olayını deftere nakledersiniz. Bu olay, *Tişört* ürünü miktarını 1 artırır.

```json
{
    "id": "Test201",
    "organizationId": "usmf",
    "productId": "T-shirt",
    "dimensionDataSource": "pos",
    "dimensions": {
        "siteId": "1",
        "locationId": "11",
        "posMachineId": "0001",
        "colorId": "red"
    },
    "quantities": {
        "pos": {
            "inbound": 1
        }
    }
}
```

Aşağıdaki örnekte, `dimensionDataSource` olmadan örnek gövde içeriği gösterilmektedir. Bu durumda,`dimensions` [temel boyutlar](inventory-visibility-configuration.md#data-source-configuration-dimension) olur. `dimensionDataSource` ayarlanırsa `dimensions` veri kaynağı boyutları veya temel boyutlar olabilir.

```json
{
    "id": "Test202",
    "organizationId": "usmf",
    "productId": "T-shirt",
    "dimensions": {
        "siteId": "1",
        "locationId": "11",
        "colorId": "red"
    },
    "quantities": {
        "pos": {
            "inbound": 1
        }
    }
}
```

### <a name="create-multiple-change-events"></a><a name="create-multiple-onhand-change-events"></a>Birden fazla değişiklik olayı oluşturma

Bu API, [tek olay API](#create-one-onhand-change-event)'sinin yaptığı gibi değiştirme olayları oluşturabilir. Tek fark, bu API'nin aynı anda birden çok kayıt oluşturabilmesidir. Bu nedenle `Path` ve `Body` değerleri farklıdır. Bu API için `Body` bir dizi kayıt sağlar. Maksimum kayıt sayısı 512'dir. Bu nedenle, eldeki stok değişikliği toplu API'si tek seferde 512 adede kadar değişiklik olayını destekleyebilir. 

Örneğin, bir perakende mağazası POS makinesi aşağıdaki iki hareketi işlemiştir:

- Bir kırmızı tişört için bir iade siparişi
- Üç siyah tişört için bir satış hareketi

Bu durumda, her iki stok güncelleştirmesini tek bir API çağrısına dahil edebilirsiniz.

```txt
Path:
    /api/environment/{environmentId}/onhand/bulk
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
            dimensionDataSource: string, # Optional
            dimensions: {
                [key:string]: string,
            },
            quantities: {
                [dataSourceName:string]: {
                    [key:string]: number,
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
        "id": "Test203",
        "organizationId": "usmf",
        "productId": "T-shirt",
        "dimensionDataSource": "pos",
        "dimensions": {
            "SiteId": "Site1",
            "LocationId": "11",
            "posMachineId&quot;: &quot;0001"
            "colorId&quot;: &quot;red"
        },
        "quantities": {
            "pos": { "inbound": 1 }
        }
    },
    {
        "id": "Test204",
        "organizationId": "usmf",
        "productId": "T-shirt",
        "dimensions": {
            "siteId": "1",
            "locationId": "11",
            "colorId&quot;: &quot;black"
        },
        "quantities": {
            "pos": { "outbound": 3 }
        }
    }
]
```

## <a name="setoverride-on-hand-quantities"></a><a name="set-onhand-quantities"></a>Eldeki miktarları ayarlama/geçersiz kılma

*Eldekini ayarlama* API'si, belirtilen ürün için geçerli verileri geçersiz kılar. Bu işlev genellikle stok sayımı güncelleştirmeleri yapmak için kullanılır. Örneğin, günlük stok sayımı sırasında bir mağaza kırmızı tişört için eldeki geçerli stoğun 100 adet olduğunu görebilir. Bu nedenle POS gelen miktarı önceki miktarın ne olduğundan bağımsız olarak 100'e güncelleştirilmelidir. Bu API'yi mevcut değeri geçersiz kılmak için kullanabilirsiniz.

```txt
Path:
    /api/environment/{environmentId}/setonhand/{inventorySystem}/bulk
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
            dimensionDataSource: string, # Optional
            dimensions: {
                [key:string]: string,
            },
            quantities: {
                [dataSourceName:string]: {
                    [key:string]: number,
                },
            },
            modifiedDateTimeUTC: datetime,
        },
        ...
    ]
```

Aşağıdaki örnekte, örnek gövde içeriği gösterilmektedir. Bu API'nin davranışı, bu makalede daha önce [Eldeki değişiklik olayları oluşturma](#create-onhand-change-event) bölümünde açıklanan API'lerin davranışından farklıdır. Bu örnekte, *Tişört* ürünü miktarı 1 olarak ayarlanır.

```json
[
    {
        "id": "Test204",
        "organizationId": "usmf",
        "productId": "T-shirt",
        "dimensionDataSource": "pos",
        "dimensions": {
            "SiteId": "1",
            "LocationId": "11",
            "posMachineId": "0001"
            "colorId": "red"
        },
        "quantities": {
            "pos": {
                "inbound": 100
            }
        }
    }
]
```

## <a name="create-reservation-events"></a>Rezervasyon olayları oluşturma

*Rezerve Etme* API'sini kullanmak için rezervasyon özelliğini açmanız ve rezervasyon yapılandırmasını tamamlamanız gerekir. Daha fazla bilgi için (veri akışı ve örnek senaryo dahil) bkz. [Rezervasyon yapılandırması (isteğe bağlı)](inventory-visibility-configuration.md#reservation-configuration).

### <a name="create-one-reservation-event"></a><a name="create-one-reservation-event"></a>Rezervasyon olayı oluşturma

Rezervasyon, farklı veri kaynağı ayarları için yapılabilir. Bu tür bir rezervasyonu yapılandırmak için öncelikle `dimensionDataSource` parametresinde veri kaynağını belirtin. Ardından `dimensions` parametresinde, hedef veri kaynağındaki boyut ayarlarına göre boyutları belirtin.

Rezervasyon API'sini çağırdığınızda istek gövdesinde Boolean `ifCheckAvailForReserv` parametresini belirterek rezervasyon doğrulamasını denetleyebilirsiniz. `True` değeri, doğrulamanın gerekli olduğu anlamına ve `False` değeri, doğrulamanın gerekli olmadığı anlamına gelir. Varsayılan değer `True` değeridir.

Rezervasyonu tersine çevirmek veya belirtilen stok miktarlarının rezervasyonunu kaldırmak istiyorsanız miktarı negatif bir değere ayarlayın ve doğrulamayı atlamak için `ifCheckAvailForReserv` parametresini `False` olarak ayarlayın. Ayrıca, aynı işlemi gerçekleştirmek için adanmış bir rezervasyonu kaldırma API'si de vardır. Fark yalnızca iki API'nin çağrılma biçimindedir. *Rezervasyonu kaldırma* API'si ile `reservationId` öğesini kullanarak belirli bir rezervasyon olayını tersine çevirmek daha kolaydır. Daha fazla bilgi için [Bir rezervasyon olayının rezervasyonunu kaldırma](#reverse-reservation-events) bölümüne bakın.

```txt
Path:
    /api/environment/{environmentId}/onhand/reserve
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
        dimensionDataSource: string,
        dimensions: {
            [key:string]: string,
        },
        quantityDataSource: string, # optional
        quantities: {
            [dataSourceName:string]: {
                [key:string]: number,
            },
        },
        modifier: string,
        quantity: number,
        ifCheckAvailForReserv: boolean,
    }
```

Aşağıdaki örnekte, örnek gövde içeriği gösterilmektedir.

```json
{
    "id": "reserve-0",
    "organizationId": "SCM_IV",
    "productId": "iv_postman_product",
    "quantity": 1,
    "quantityDataSource": "iv",
    "modifier": "softReservOrdered",
    "ifCheckAvailForReserv": true,
    "dimensions": {
        "siteId": "iv_postman_site",
        "locationId": "iv_postman_location",
        "colorId": "red",
        "sizeId&quot;: &quot;small"
    }
}
```

Aşağıdaki örnekte başarılı bir yanıt gösterilmektedir.

```json
{
    "reservationId": "RESERVATION_ID",
    "id": "ohre~id-822-232959-524",
    "processingStatus": "success",
    "message": "",
    "statusCode": 200
}
``` 

### <a name="create-multiple-reservation-events"></a><a name="create-multiple-reservation-events"></a>Birden fazla rezervasyon olayı oluşturma

Bu API, [tek olay API'sinin](#create-reservation-events) toplu bir sürümüdür.

```txt
Path:
    /api/environment/{environmentId}/onhand/reserve/bulk
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
            quantities: {
                [dataSourceName:string]: {
                    [key:string]: number,
                },
            },
            modifier: string,
            quantity: number,
            ifCheckAvailForReserv: boolean,
        },
        ...
    ]
```

## <a name="reverse-reservation-events"></a>Rezervasyon olaylarını tersine çevirme

*Rezervasyonu kaldırma* API'si, [*Rezervasyon*](#create-reservation-events) olayları için ters işlem görevi görür. Bu, `reservationId` ile belirtilen bir rezervasyon olayını tersine çevirmek veya rezervasyon miktarını azaltmak için bir yol sağlar.

### <a name="reverse-one-reservation-event"></a><a name="reverse-one-reservation-event"></a>Bir rezervasyon olayını tersine çevirme

Bir rezervasyon oluşturulduğunda, yanıt gövdesine bir `reservationId` dahil edilir. Rezervasyonu iptal etmek için aynı `reservationId` öğesini sağlamalısınız ve rezervasyon API çağrısı için kullanılan aynı `organizationId` ve `dimensions` öğelerini dahil etmelisiniz. Son olarak, önceki rezervasyondan serbest bırakılacak maddelerin sayısını temsil eden bir `OffsetQty` değeri belirtin. Rezervasyon, belirtilen `OffsetQty` değerine göre tamamen veya kısmen tersine çevrilebilir. Örneğin, bir maddenin *100* birimi rezerve edilmişse, başlangıçtaki rezerve edilen miktarın *10*'unun rezervasyonunu kaldırmak için `OffsetQty: 10` belirtebilirsiniz.

```txt
Path:
    /api/environment/{environmentId}/onhand/unreserve
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
        reservationId: string,
        dimensions: {
            [key:string]: string,
        },
        OffsetQty: number
    }
```

Aşağıdaki kodda, örnek bir gövde içeriği gösterilmektedir.

```json
{
    "id": "unreserve-0",
    "organizationId": "SCM_IV",
    "reservationId": "RESERVATION_ID",
    "dimensions": {
        "siteid":"iv_postman_site",
        "locationid":"iv_postman_location",
        "ColorId": "red",
        "SizeId&quot;: &quot;small"
    },
    "OffsetQty": 1
}
```

Aşağıdaki kodda başarılı bir yanıt gövdesi örneği gösterilmektedir.

```json
{
    "reservationId": "RESERVATION_ID",
    "totalInvalidOffsetQtyByReservId": 0,
    "id": "ohoe~id-823-11744-883",
    "processingStatus": "success",
    "message": "",
    "statusCode": 200
}
```

> [!NOTE]
> Yanıt gövdesinde, `OffsetQty` değeri rezervasyon miktarından küçük veya bu değere eşit olduğunda `processingStatus` "*success*" durumunda ve `totalInvalidOffsetQtyByReservId` *0* olur.
>
> `OffsetQty` değeri rezerve edilen miktardan büyükse, `processingStatus` "*partialSuccess*" durumunda olur ve `totalInvalidOffsetQtyByReservId`, `OffsetQty` ile rezerve edilen miktar arasındaki farka eşit olur.
>
>Örneğin, rezervasyonun miktarı *10* ve `OffsetQty` değeri *12* ise `totalInvalidOffsetQtyByReservId` *2* olur.

### <a name="reverse-multiple-reservation-events"></a><a name="reverse-multiple-reservation-events"></a>Birden fazla rezervasyon olayını tersine çevirme

Bu API, [tek olay API'sinin](#reverse-one-reservation-event) toplu bir sürümüdür.

```txt
Path:
    /api/environment/{environmentId}/onhand/unreserve/bulk
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
            reservationId: string,
            dimensions: {
                [key:string]: string,
            },
            OffsetQty: number
        }
        ...
    ]
```

## <a name="query-on-hand"></a>Eldekini sorgulama

Ürünlerinize ait mevcut eldeki stok verilerini getirmek için *Eldekini sorgulama* API'sını kullanın. Bu API'yi, e-ticaret web sitenizde ürün stok düzeylerini gözden geçirmek istediğinizde veya bölgeler arasında ya da yakındaki mağazalarda ve ambarlarda ürün kullanılabilirliğini denetlemek istediğinizde, stoğu bilmeniz gerektiğinde kullanabilirsiniz. API şu anda `productID` değerine göre en çok 5000 ayrı öğeye kadar sorgulamayı desteklemektedir. Her sorguda birden çok `siteID` ve `locationID` değeri de belirtilebilir. Maksimum sınır aşağıdaki denklemle tanımlanır:

*NumOf(SiteID) \* NumOf(LocationID) <= 100*.

### <a name="query-by-using-the-post-method"></a><a name="query-with-post-method"></a>Post yöntemini kullanarak sorgulama

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

Bu isteğin gövde kısmında, `dimensionDataSource` isteğe bağlı bir parametre olmaya devam eder. Ayarlanmamışsa `filters` *temel boyutlar* olarak kabul edilir. `filters` için `organizationId`, `productId`, `siteId` ve `locationId` olmak üzere dört gerekli alan vardır.

- `organizationId` yalnızca bir değer içermelidir ancak yine de bir dizidir.
- `productId` bir veya daha fazla değer içerebilir. Bu boş bir diziyse tüm ürünler döndürülür.
- `siteId` ve `locationId`, Stok Görünürlüğü'nde bölümleme için kullanılır. *Eldekini sorgulama* isteğinde birden fazla `siteId` ve `locationId` değeri belirtebilirsiniz. Geçerli sürümde hem `siteId` hem de `locationId` değerlerini belirtmelisiniz.

Dizin oluşturma yapılandırmanızı takip etmek için `groupByValues` parametresini kullanmanızı öneririz. Daha fazla bilgi için bkz. [Ürün dizini hiyerarşi yapılandırması](./inventory-visibility-configuration.md#index-configuration).

`returnNegative` parametresi, sonuçların negatif girişler içerip içermediğini denetler.

> [!NOTE]
> Eldeki değişiklik zamanlamasını ve karşılanabilir (KM) miktar özelliklerini etkinleştirdiyseniz sorgunuz, sorgu sonuçlarının KM bilgilerini içerip içermediğini denetleyen `QueryATP` Boole parametresini de içerebilir. Daha fazla bilgi ve örnekler için bkz. [Stok Görünürlüğü eldeki değişiklik zamanlamaları ve karşılanabilir miktarı](inventory-visibility-available-to-promise.md).

Aşağıdaki örnekte, örnek gövde içeriği gösterilmektedir. Eldeki stoğu birden fazla yerleşimden (ambar) sorgulayabileceğinizi gösterilir.

```json
{
    "dimensionDataSource": "pos",
    "filters": {
        "organizationId": ["usmf"],
        "productId": ["T-shirt"],
        "siteId": ["1"],
        "locationId": ["11","12","13"],
        "colorId": ["red"]
    },
    "groupByValues": ["colorId", "sizeId"],
    "returnNegative": true
}
```

Aşağıdaki örnekte, belirli bir tesis ve yerleşimdeki tüm ürünlerin nasıl sorgulanacağı gösterilmektedir.

```json
{
    "filters": {
        "organizationId": ["usmf"],
        "productId": [],
        "siteId": ["1"],
        "locationId": ["11"],
    },
    "groupByValues": ["colorId", "sizeId"],
    "returnNegative": true
}
```

### <a name="query-by-using-the-get-method"></a><a name="query-with-get-method"></a>Get yöntemini kullanarak sorgulama

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

Aşağıda, örnek bir alma URL'si bulunmaktadır. Bu alma isteği, daha önce sağlanan deftere nakletme örneği ile tam olarak aynıdır.

```txt
/api/environment/{environmentId}/onhand?organizationId=SCM_IV&productId=iv_postman_product&siteId=iv_postman_site&locationId=iv_postman_location&colorId=red&groupBy=colorId,sizeId&returnNegative=true
```

## <a name="on-hand-exact-query"></a><a name="exact-query-with-post-method"></a>Eldeki stok tam sorgusu

Eldeki stok tam sorguları normal eldeki stok sorgularına benzer ancak tesis ve yerleşim arasında bir eşleme hiyerarşisi belirtmenize olanak tanır. Örneğin, aşağıdaki iki tesise sahipsiniz:

- Tesis 1, A yerleşimi ile eşlenen
- Tesis 2, B yerleşimi ile eşlenen

Normal eldeki stok sorgusu için `"siteId": ["1","2"]` ve `"locationId": ["A","B"]` belirtirseniz, Stok Görünürlüğü aşağıdaki tesisler ve yerleşimler için sonucu otomatik olarak sorgular.

- Tesis 1, A yerleşimi
- Tesis 1, B yerleşimi
- Tesis 2, A yerleşimi
- Tesis 2, B yerleşimi

Gördüğünüz gibi, normal eldeki stok sorgusu A yerleşiminin yalnızca tesis 1'de var olduğunu ve B yerleşiminin yalnızca tesis 2'de var olduğunu tanımaz. Bu nedenle, gereksiz sorgular yapar. Bu hiyerarşik eşlemeye uyum sağlamak için, eldeki stok tam sorgusu kullanabilir ve sorgu gövdesinde yerleşim eşlemelerini belirtebilirsiniz. Bu durumda, yalnızca tesis 1, A yerleşimi ve tesis 2 B yerleşimi ile ilgili sonuçları sorgular ve sonuç alırsınız.

### <a name="exact-query-by-using-the-post-method"></a><a name="exact-query-with-post-method"></a>Post yöntemini kullanarak tam sorgulama

```txt
Path:
    /api/environment/{environmentId}/onhand/exactquery
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
            dimensions: string[],
            values: string[][],
        },
        groupByValues: string[],
        returnNegative: boolean,
    }
```

Bu isteğin gövde kısmında, `dimensionDataSource` isteğe bağlı bir parametredir. Ayarlanmamışsa `filters` içindeki `dimensions` *temel boyutlar* olarak kabul edilir. `filters` için `organizationId`, `productId`, `dimensions` ve `values` olmak üzere dört gerekli alan vardır.

- `organizationId` yalnızca bir değer içermelidir ancak yine de bir dizidir.
- `productId` bir veya daha fazla değer içerebilir. Bu boş bir diziyse tüm ürünler döndürülür.
- `dimensions` dizisi, `siteId` ve `locationId` gereklidir ancak herhangi bir sırada diğer öğelerle birlikte görüntülenebilir.
- `values`, `dimensions` öğesine karşılık gelen bir veya daha fazla farklı değer grubu içerebilir.

`filters` içindeki `dimensions` otomatik olarak `groupByValues` öğesine eklenir.

`returnNegative` parametresi, sonuçların negatif girişler içerip içermediğini denetler.

Aşağıdaki örnekte, örnek gövde içeriği gösterilmektedir.

```json
{
    "dimensionDataSource": "pos",
    "filters": {
        "organizationId": ["SCM_IV"],
        "productId": ["iv_postman_product"],
        "dimensions": ["siteId", "locationId", "colorId"],
        "values" : [
            ["iv_postman_site", "iv_postman_location", "red"],
            ["iv_postman_site", "iv_postman_location", "blue"],
        ]
    },
    "groupByValues": ["colorId", "sizeId"],
    "returnNegative": true
}
```

Aşağıdaki örnekte, birden çok tesis ve konumdaki tüm ürünlerin nasıl sorgulanacağı gösterilmektedir.

```json
{
    "filters": {
        "organizationId": ["SCM_IV"],
        "productId": [],
        "dimensions": ["siteId", "locationId"],
        "values" : [
            ["iv_postman_site_1", "iv_postman_location_1"],
            ["iv_postman_site_2", "iv_postman_location_2"],
        ]
    },
    "groupByValues": ["colorId", "sizeId"],
    "returnNegative": true
}
```

## <a name="available-to-promise"></a>Karşılanabilir miktar

Gelecekteki eldeki değişiklikleri zamanlamanıza ve KM miktarlarını hesaplamanıza olanak tanıyan Stok Görünürlüğü'nü ayarlayabilirsiniz. KM, mevcut bulunan ve sonraki dönemde müşteriye vaat edilebilecek bir maddenin miktarıdır. KM hesaplamasının kullanımı, sipariş karşılama yeteneğinizi büyük ölçüde artırabilir. Bu özelliği etkinleştirme ve özellik etkinleştirildikten sonra API aracılığıyla Stok Görünürlüğü ile etkileşim kurma hakkında bilgi için bkz. [Stok Görünürlüğü eldeki değişiklik zamanlamaları ve karşılanabilir miktarı](inventory-visibility-available-to-promise.md#api-urls).

## <a name="allocation"></a>Tahsisat

Tahsisat ile ilgili API'ler [Stok Görünürlüğü tahsisatında](inventory-visibility-allocation.md#using-allocation-api) yer alır.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
