---
title: Inventory Visibility genel API'leri
description: Bu makalede, Stok Görünürlüğü tarafından sağlanan genel API'ler açıklanmaktadır.
author: yufeihuang
ms.date: 12/09/2021
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yufeihuang
ms.search.validFrom: 2021-08-02
ms.dyn365.ops.version: 10.0.22
ms.openlocfilehash: 25f6539616d4567249e1d1eb4297090176526fde
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8902038"
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
| /api/environment/{environmentId}/onhand | Naklet | [Eldeki değişiklik olayı oluşturma](#create-one-onhand-change-event) |
| /api/environment/{environmentId}/onhand/bulk | Naklet | [Birden fazla değişiklik olayı oluşturma](#create-multiple-onhand-change-events) |
| /api/environment/{environmentId}/setonhand/{inventorySystem}/bulk | Naklet | [Eldeki miktarları ayarlama/geçersiz kılma](#set-onhand-quantities) |
| /api/environment/{environmentId}/onhand/reserve | Naklet | [Bir rezervasyon olayı oluşturma](#create-one-reservation-event) |
| /api/environment/{environmentId}/onhand/reserve/bulk | Naklet | [Birden fazla rezervasyon olayı oluşturma](#create-multiple-reservation-events) |
| /api/environment/{environmentId}/onhand/changeschedule | Deftere naklet | [Bir zamanlanan eldeki değişiklik oluşturma](inventory-visibility-available-to-promise.md) |
| /api/environment/{environmentId}/onhand/changeschedule/bulk | Deftere naklet | [Birden fazla zamanlanan eldeki değişiklik oluşturma](inventory-visibility-available-to-promise.md) |
| /api/environment/{environmentId}/onhand/indexquery | Deftere naklet | [Post yöntemini kullanarak sorgulama](#query-with-post-method) |
| /api/environment/{environmentId}/onhand | Al | [Get yöntemini kullanarak sorgulama](#query-with-get-method) |
| /api/environment/{environmentId}/allocation/allocate | Deftere naklet | [Bir tahsisat olayı oluşturma](inventory-visibility-allocation.md#using-allocation-api) |
| /api/environment/{environmentId}/allocation/unallocate | Deftere naklet | [Bir tahsisattan kaldırma olayı oluşturma](inventory-visibility-allocation.md#using-allocation-api) |
| /api/environment/{environmentId}/allocation/reallocate | Deftere naklet | [Bir yeniden tahsis etme olayı oluşturma](inventory-visibility-allocation.md#using-allocation-api) |
| /api/environment/{environmentId}/allocation/consume | Deftere naklet | [Bir tüketme olayı oluşturma](inventory-visibility-allocation.md#using-allocation-api) |
| /api/environment/{environmentId}/allocation/query | Deftere naklet | [Tahsisat sorgusu sonucu](inventory-visibility-allocation.md#using-allocation-api) |

> [!NOTE]
> Yolun {environmentId} bölümü, Microsoft Dynamics Lifecycle Services'teki (LCS) ortam kimliğidir.
> 
> Toplu API, her istek için en fazla 512 kayıt döndürebilir.

Microsoft, hazır bir *Postman* istek koleksiyonu sağlamıştır. Şu paylaşılan bağlantıyı kullanarak bu koleksiyonu *Postman* yazılımınıza içeri aktarabilirsiniz: <https://www.getpostman.com/collections/ad8a1322f953f88d9a55>.

## <a name="find-the-endpoint-according-to-your-lifecycle-services-environment"></a>Lifecycle Services ortamınıza göre uç noktayı bulma

Stok Görünürlüğü mikro hizmeti, birden çok coğrafya ve bölgede Microsoft Azure Service Fabric'te dağıtılır. Şu anda isteğinizi ilgili coğrafya ve bölgeye otomatik olarak yönlendirebilecek merkezi bir uç nokta bulunmamaktadır. Bu nedenle, aşağıdaki modeli kullanarak bilgi parçalarını bir URL'de oluşturmanız gerekir:

`https://inventoryservice.<RegionShortName>-il<IsLandNumber>.gateway.prod.island.powerapps.com`

Bölge kısa adı, Microsoft Dynamics Lifecycle Services (LCS) ortamında bulunabilir. Aşağıdaki tabloda, şu anda kullanılabilen bölgeler listelenmektedir.

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
| Güney Brezilya        | sbr               |
| Güney Orta ABD    | scus              |

Ada numarası, LCS ortamınızın Service Fabric'te dağıtıldığı yerdir. Şu anda bu bilgileri kullanıcı tarafında almanın yolu yoktur.

Microsoft, Power Apps'te bir kullanıcı arabirimi (UI) oluşturmuştur, böylece mikro hizmetin tam uç noktasını alabilirsiniz. Daha fazla bilgi için bkz. [Hizmet uç noktasını bulma](inventory-visibility-configuration.md#get-service-endpoint).

## <a name="authentication"></a><a name="inventory-visibility-authentication"></a>Kimlik Doğrulama

Platform güvenlik belirteci, Stok Görünürlüğü genel API'sini çağırmak için kullanılır. Bu nedenle, Azure AD uygulamanızı kullanarak bir _Azure Active Directory (Azure AD) belirteci_ oluşturmanız gerekir. Daha sonra güvenlik hizmetinden _erişim belirtecini_ almak için Azure AD belirteci kullanmanız gerekir.

Microsoft, kullanıma hazır bir *Postman* belirteç koleksiyonu sağlar. Şu paylaşılan bağlantıyı kullanarak bu koleksiyonu *Postman* yazılımınıza içeri aktarabilirsiniz: <https://www.getpostman.com/collections/496645018f96b3f0455e>.

Güvenlik hizmeti belirteci almak için aşağıdaki adımları izleyin.

1. Azure portalda oturum açın ve bu portalı kullanarak Dynamics 365 Supply Chain Management uygulamanız için `clientId` ve `clientSecret` değerlerini bulun.
1. Aşağıdaki özelliklere sahip bir HTTP isteği göndererek Azure AD belirteci (`aadToken`) getirin:

   - **URL:** `https://login.microsoftonline.com/${aadTenantId}/oauth2/token`
   - **Yöntem:** `GET`
   - **Gövde içeriği (form verileri):**

     | Anahtar           | Değer                                |
     | ------------- | ------------------------------------ |
     | client_id     | ${aadAppId}                          |
     | client_secret | ${aadAppSecret}                      |
     | grant_type    | client_credentials                   |
     | resource      | 0cdb527f-a8d1-4bf8-9436-b352c68682b2 |

   Yanıtta bir Azure AD belirteci (`aadToken`) almanız gerekir. Bu etiket, aşağıdaki örneğe benzeyecektir.

   ```json
   {
       "token_type": "Bearer",
       "expires_in": "3599",
       "ext_expires_in": "3599",
       "expires_on": "1610466645",
       "not_before": "1610462745",
       "resource": "0cdb527f-a8d1-4bf8-9436-b352c68682b2",
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
       "context": "5dbf6cc8-255e-4de2-8a25-2101cd5649b4",
       "context_type": "finops-env"
   }
   ```

   Aaşağıdaki noktaları unutmayın:

   - `client_assertion` değeri, önceki adımda aldığınız Azure AD belirteci (`aadToken`) olmalıdır.
   - `context`değeri, eklentiyi dağıtmak istediğiniz LCS ortamı kimliği olmalıdır.
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

| Alan kodu | Tanım |
|---|---|
| `id` | Belirli bir değişiklik olayı için benzersiz bir kimlik. Bu kimlik, deftere nakil sırasında hizmetle iletişim başarısız olursa aynı olayın yeniden gönderilmesi durumunda sistemde iki kez sayılmamasını sağlamak için kullanılır. |
| `organizationId` | Olayla bağlantılı kuruluşun tanımlayıcısı. Bu değer, Supply Chain Management'ta bir kuruluş veya veri alanı kimliğiyle eşlenir. |
| `productId` | Ürünün tanımlayıcısı. |
| `quantities` | Eldeki miktarın değiştirilmesi gereken miktar. Örneğin, bir rafa 10 yeni kitap eklenirse bu değer `quantities:{ shelf:{ received: 10 }}` olur. Üç kitap raftan kaldırılırsa veya satılırsa bu değer `quantities:{ shelf:{ sold: 3 }}` olur. |
| `dimensionDataSource` | Deftere nakil değişikliği olayı ve sorgusunda kullanılan boyutların veri kaynağı. Veri kaynağını belirtirseniz belirtilen veri kaynağındaki özel boyutları kullanabilirsiniz. Stok Görünürlüğü, özel boyutları genel varsayılan boyutlarla eşleştirmek için boyut yapılandırmasını kullanır. `dimensionDataSource` değeri belirtilmezse sorgularınızda yalnızca [temel boyutları](inventory-visibility-configuration.md#data-source-configuration-dimension) kullanabilirsiniz. |
| `dimensions` | Dinamik bir anahtar-değer çifti. Değerler, Supply Chain Management'ta bazı boyutlarla eşleştirilir. Ancak olayın Supply Chain Management'tan veya harici bir sistemden geldiğini belirtmek için özel boyutlar da (örneğin, _Kaynak_) ekleyebilirsiniz. |

> [!NOTE]
> `SiteId` ve `LocationId` parametreleri [bölüm yapılandırmasını](inventory-visibility-configuration.md#partition-configuration) oluşturur. Bu nedenle, eldeki değişiklik olayları oluşturduğunuzda, eldeki miktarları ayarladığınızda veya geçersiz kıldığınızda ya da rezervasyon olayları oluşturduğunuzda bunları boyutlarda belirtmeniz gerekir.

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

Aşağıdaki örnekte, örnek gövde içeriği gösterilmektedir. Bu örnekte, *Tişört* ürünü için bir değişiklik olayı deftere nakledersiniz. Bu olay, satış noktası (POS) sisteminden alınır ve müşteri, mağazaya kırmızı bir Tişört döndürmüştür. Bu olay, *Tişört* ürünü miktarını 1 artırır.

```json
{
    "id": "123456",
    "organizationId": "usmf",
    "productId": "T-shirt",
    "dimensionDataSource": "pos",
    "dimensions": {
        "SiteId": "1",
        "LocationId": "11",
        "PosMachineId": "0001",
        "ColorId": "Red"
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
    "id": "123456",
    "organizationId": "usmf",
    "productId": "T-shirt",
    "dimensions": {
        "SiteId": "1",
        "LocationId": "11",
        "ColorId": "Red"
    },
    "quantities": {
        "pos": {
            "inbound": 1
        }
    }
}
```

### <a name="create-multiple-change-events"></a><a name="create-multiple-onhand-change-events"></a>Birden fazla değişiklik olayı oluşturma

Bu API aynı anda birden çok kayıt oluşturabilir. Bu API ile [tek olay API'si](#create-one-onhand-change-event) arasındaki tek fark, `Path` ve `Body` değerleridir. Bu API için `Body` bir dizi kayıt sağlar. En fazla kayıt sayısı 512'dir. Yani, eldeki toplu API değişimi, bir seferde 512 değişiklik olayına kadar destek alabilir.

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
        "id": "123456",
        "organizationId": "usmf",
        "productId": "T-shirt",
        "dimensionDataSource": "pos",
        "dimensions": {
            "PosSiteId": "1",
            "PosLocationId": "11",
            "PosMachineId&quot;: &quot;0001"
        },
        "quantities": {
            "pos": { "inbound": 1 }
        }
    },
    {
        "id": "654321",
        "organizationId": "usmf",
        "productId": "Pants",
        "dimensions": {
            "SiteId": "1",
            "LocationId": "11",
            "ColorId&quot;: &quot;black"
        },
        "quantities": {
            "pos": { "outbound": 3 }
        }
    }
]
```

## <a name="setoverride-on-hand-quantities"></a><a name="set-onhand-quantities"></a>Eldeki miktarları ayarlama/geçersiz kılma

_Eldekini ayarlama_ API'si, belirtilen ürün için geçerli verileri geçersiz kılar.

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
        "id": "123456",
        "organizationId": "usmf",
        "productId": "T-shirt",
        "dimensionDataSource": "pos",
        "dimensions": {
             "PosSiteId": "1",
            "PosLocationId": "11",
            "PosMachineId": "0001"
        },
        "quantities": {
            "pos": {
                "inbound": 1
            }
        }
    }
]
```

## <a name="create-reservation-events"></a>Rezervasyon olayları oluşturma

*Rezerve Etme* API'sini kullanmak için rezervasyon özelliğini açmanız ve rezervasyon yapılandırmasını tamamlamanız gerekir. Daha fazla bilgi için bkz. [Rezervasyon yapılandırması (isteğe bağlı)](inventory-visibility-configuration.md#reservation-configuration).

### <a name="create-one-reservation-event"></a><a name="create-one-reservation-event"></a>Rezervasyon olayı oluşturma

Rezervasyon, farklı veri kaynağı ayarları için yapılabilir. Bu tür bir rezervasyonu yapılandırmak için öncelikle `dimensionDataSource` parametresinde veri kaynağını belirtin. Ardından `dimensions` parametresinde, hedef veri kaynağındaki boyut ayarlarına göre boyutları belirtin.

Rezervasyon API'sini çağırdığınızda istek gövdesinde Boolean `ifCheckAvailForReserv` parametresini belirterek rezervasyon doğrulamasını denetleyebilirsiniz. `True` değeri, doğrulamanın gerekli olduğu anlamına ve `False` değeri, doğrulamanın gerekli olmadığı anlamına gelir. Varsayılan değer `True` değeridir.

Rezervasyonu iptal etmek veya belirtilen stok miktarlarının rezervasyonunu kaldırmak istiyorsanız miktarı negatif bir değere ayarlayın ve doğrulamayı atlamak için `ifCheckAvailForReserv` parametresini `False` olarak ayarlayın.

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
    "organizationId": "usmf",
    "productId": "T-shirt",
    "quantity": 1,
    "quantityDataSource": "iv",
    "modifier": "softreservordered",
    "ifCheckAvailForReserv": true,
    "dimensions": {
        "SiteId": "1",
        "LocationId": "11",
        "ColorId": "Red",
        "SizeId&quot;: &quot;Small"
    }
}
```

### <a name="create-multiple-reservation-events"></a><a name="create-multiple-reservation-events"></a>Birden fazla rezervasyon olayı oluşturma

Bu API, [tek olay API'sinin](#create-one-reservation-event) toplu bir sürümüdür.

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

## <a name="query-on-hand"></a>Eldekini sorgulama

Ürünlerinize ait mevcut eldeki stok verilerini getirmek için _Eldekini sorgulama_ API'sını kullanın. API şu anda `ProductID` değerine göre en çok 100 ayrı öğeye kadar sorgulamayı desteklemektedir. Her sorguda birden çok `SiteID` ve `LocationID` değeri de belirtilebilir. Maksimum sınır `NumOf(SiteID) * NumOf(LocationID) <= 100` olarak tanımlanmıştır.

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

`groupByValues` parametresi, dizin oluşturma yapılandırmanızı takip etmelidir. Daha fazla bilgi için bkz. [Ürün dizini hiyerarşi yapılandırması](./inventory-visibility-configuration.md#index-configuration).

`returnNegative` parametresi, sonuçların negatif girişler içerip içermediğini denetler.

> [!NOTE]
> Eldeki değişiklik zamanlamasını ve karşılanabilir (KM) miktar özelliklerini etkinleştirdiyseniz sorgunuz, sorgu sonuçlarının KM bilgilerini içerip içermediğini denetleyen `QueryATP` Boole parametresini de içerebilir. Daha fazla bilgi ve örnekler için bkz. [Stok Görünürlüğü eldeki değişiklik zamanlamaları ve karşılanabilir miktarı](inventory-visibility-available-to-promise.md).

Aşağıdaki örnekte, örnek gövde içeriği gösterilmektedir.

```json
{
    "dimensionDataSource": "pos",
    "filters": {
        "organizationId": ["usmf"],
        "productId": ["T-shirt"],
        "siteId": ["1"],
        "LocationId": ["11"],
        "ColorId": ["Red"]
    },
    "groupByValues": ["ColorId", "SizeId"],
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
        "LocationId": ["11"],
    },
    "groupByValues": ["ColorId", "SizeId"],
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
/api/environment/{environmentId}/onhand?organizationId=usmf&productId=T-shirt&SiteId=1&LocationId=11&ColorId=Red&groupBy=ColorId,SizeId&returnNegative=true
```

## <a name="available-to-promise"></a>Karşılanabilir miktar

Gelecekteki eldeki değişiklikleri zamanlamanıza ve KM miktarlarını hesaplamanıza olanak tanıyan Stok Görünürlüğü'nü ayarlayabilirsiniz. KM, mevcut bulunan ve sonraki dönemde müşteriye vaat edilebilecek bir maddenin miktarıdır. KM hesaplamasının kullanımı, sipariş karşılama yeteneğinizi büyük ölçüde artırabilir. Bu özelliği etkinleştirme ve özellik etkinleştirildikten sonra API aracılığıyla Stok Görünürlüğü ile etkileşim kurma hakkında bilgi için bkz. [Stok Görünürlüğü eldeki değişiklik zamanlamaları ve karşılanabilir miktarı](inventory-visibility-available-to-promise.md#api-urls).

## <a name="allocation"></a>Tahsisat

Tahsisat ile ilgili API'ler [Stok Görünürlüğü tahsisatında](inventory-visibility-allocation.md#using-allocation-api) yer alır.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
