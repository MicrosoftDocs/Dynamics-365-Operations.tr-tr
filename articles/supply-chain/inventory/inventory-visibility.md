---
title: Stok Görünürlüğü Eklentisi
description: Bu konu, Dynamics 365 Supply Chain Management için Stok Görünürlüğü Eklentisinin nasıl yüklendiğini ve yapılandırıldığını açıklar.
author: sherry-zheng
manager: tfehr
ms.date: 10/26/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2020-10-26
ms.dyn365.ops.version: Release 10.0.15
ms.openlocfilehash: 4e6f7e0a3978bbf7e520f8cbcfd27c4cfe507777
ms.sourcegitcommit: ea2d652867b9b83ce6e5e8d6a97d2f9460a84c52
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/03/2021
ms.locfileid: "5114682"
---
# <a name="inventory-visibility-add-in"></a>Stok Görünürlüğü Eklentisi

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]
[!INCLUDE [cc-data-platform-banner](../../includes/cc-data-platform-banner.md)]

Stok Görünürlüğü Eklentisi, gerçek zamanlı olarak elden stok takibi sağlayan ve böylece stok görünürlüğünün genel görünümünü sunan bağımsız ve yüksek ölçeklenebilir bir mikro hizmettir.

Eldeki stokla ilgili tüm bilgiler, düşük düzeyli SQL tümleştirmesi aracılığıyla neredeyse gerçek zamanlı olarak hizmete dışarı aktarılır. Harici sistemler, verilen boyut kümeleri üzerindeki bilgileri sorgulamak için restful API'lar aracılığıyla hizmete erişir ve böylece eldeki mevcut pozisyonların bir listesini alır.

Stok Görünürlüğü, Microsoft Dataverse üzerine kurulmuş bir mikro hizmettir; diğer bir ifadeyle, iş gereksinimlerinizi karşılamak için özelleştirilmiş işlevsellik sağlamak için Power Apps oluşturup Power BI uygulayarak genişletebilirsiniz. Envanter sorguları yapmak için dizini yükseltmeniz de mümkündür.

Stok Görünürlüğü, birden çok üçüncü taraf sistemle tümleştirmeye olanak tanıyan yapılandırma seçenekleri sağlar. Standartlaştırılmış stok boyutunu, özelleştirilmiş genişletilebilirliği ve standartlaştırılmış, yapılandırılabilir hesaplanmış miktarları destekler.

Bu konu, Dynamics 365 Supply Chain Management için Stok Görünürlüğü Eklentisi'nin nasıl yüklenilip yapılandırılacağını ve uygulama programlama arabiriminin (API) nasıl kullanılacağını açıklar.

## <a name="install-the-inventory-visibility-add-in"></a>Stok Görünürlüğü Eklentisini Yükleme

Stok Görünürlüğü Eklentisi'ni, Microsoft Dynamics Lifecycle Services'ı (LCS) kullanarak yüklemeniz gerekir. LCS, Dynamics 365 Finance and Operations uygulamalarınızın uygulama yaşam döngüsünü yönetmenize yardımcı olan bir ortam ve düzenli olarak güncelleştirilen bir dizi hizmet sağlayan bir işbirliği portalıdır.

Daha fazla bilgi için bkz. [Lifecycle Services kaynakları](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/lifecycle-services/lcs).

### <a name="prerequisites"></a>Önkoşullar

Stok Görünürlüğü Eklentisi'ni yüklemeden önce aşağıdakileri yapmanız gerekir:

- En az bir ortam dağıtılan bir LCS uygulama projesi edinin.
- LCS'de sunduklarınız için beta anahtarlarını oluşturun.
- LCS'de kullanıcınız için sunduğunuz beta anahtarlarını etkinleştirin.
- Microsoft Stok Görünürlüğü ürün takımına başvurun ve Stok Görünürlüğü Eklentisi'ni dağıtmak istediğiniz ortamın kimliği sağlayın.

Bu ön koşullarla ilgili herhangi bir sorunuz varsa lütfen Stok Görünürlüğü ürün takımıyla iletişime geçin.

### <a name="install-the-add-in"></a><a name="install-add-in"></a>Eklentiyi yükleme

Stok Görünürlüğü Eklentisi'ni yüklemek için aşağıdakileri yapın:

1. [Lifecycle Services (LCS)](https://lcs.dynamics.com/Logon/Index) portalında oturum açın.
1. Ana sayfada, ortamınızın dağıtıldığı projeyi seçin.
1. Proje sayfasında, eklentiyi yüklemek istediğiniz ortamı seçin.
1. Ortam sayfasında, **Ortam eklentileri** bölümünü görene kadar aşağı kaydırın. Bölüm görünmüyorsa, ön koşuldaki beta anahtarlarının tam olarak işlendiğinden emin olun.
1. **Ortam eklentileri** bölümünde, **Yeni bir eklenti yükleyin**'i seçin.
    ![LCS'deki ortam sayfası](media/inventory-visibility-environment.png "LCS'deki ortam sayfası")
1. **Yeni eklenti yükleyin** bağlantısını seçin. Kullanılabilir eklentilerin bir listesi görüntülenir.
1. Listeden **Stok hizmeti**'ni seçin. (Not: Bu çözüm artık **Dynamics 365 Supply Chain Management için Stok Görünürlüğü Eklentisi** olarak listelenmiş olabilir.)
1. Ortamınızın aşağıdaki alanlarının değerlerini girin:

    - **AAD uygulama kodu**
    - **AAD kiracı kimliği**

    ![Eklenti kurulum sayfası](media/inventory-visibility-setup.png "Eklenti kurulum sayfası")

1. **Şartlar ve koşullar** onay kutusunu seçerek şartlar ve koşulları kabul edin.
1. **Yükle**'yi seçin. Eklentinin durumu **Yükleniyor** olarak görünür. İşlem bittiğinde, durumun **Yüklendi** olarak değiştiğini görmek için sayfayı yenileyin.

### <a name="get-a-security-service-token"></a>Güvenlik hizmeti belirteci alma

Aşağıdakileri gerçekleştirerek güvenlik hizmeti belirteci alın:

1. Azure portalında oturum açın ve Supply Chain Management uygulamanız için `clientId` ve `clientSecret` öğelerini bulurken bunu kullanın.
1. Aşağıdaki özelliklere sahip bir HTTP isteği göndererek Azure Active Directory belirteci (`aadToken`) getirin:
    - **URL** - `https://login.microsoftonline.com/${aadTenantId}/oauth2/token`
    - **Yöntem** - `GET`
    - **Gövde içeriği (form verileri)**:

        | key | değer |
        | --- | --- |
        | client_id | ${aadAppId} |
        | client_secret | ${aadAppSecret} |
        | grant_type | client_credentials |
        | resource | 0cdb527f-a8d1-4bf8-9436-b352c68682b2 |
1. Yanıt olarak aşağıdaki örneğe benzeyen bir `aadToken` almanız gerekir.

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

1. Aşağıdakine benzer bir JSON isteğini formülleştirin:

    ```json
    {
        "grant_type": "client_credentials",
        "client_assertion_type":"aad_app",
        "client_assertion": "{Your_AADToken}",
        "scope":"https://inventoryservice.operations365.dynamics.com/.default",
        "context": "5dbf6cc8-255e-4de2-8a25-2101cd5649b4",
        "context_type": "finops-env"
    }
    ```

    Where:
    - `client_assertion` değeri, önceki adımda aldığınız `aadToken` olmalıdır.
    - `context`değeri, eklentiyi dağıtmak istediğiniz ortam kimliği olmalıdır.
    - Diğer tüm değerleri örnekte gösterilen şekilde ayarlayın.

1. Aşağıdaki özelliklere sahip bir HTTP isteği gönderin:
    - **URL** - `https://securityservice.operations365.dynamics.com/token`
    - **Yöntem** - `POST`
    - **HTTP üst bilgisi**: API sürümünü ekleyin (anahtar: `Api-Version` ve değer: `1.0` olmalıdır)
    - **Gövde içeriği:** Önceki adımda oluşturduğunuz JSON isteğini ekleyin.

1. Yanıt olarak bir `access_token` alırsınız. Stok Görünürlüğü API'sını çağırmak için taşıyıcı belirteç olarak ihtiyacınız olan budur. Aşağıda bir örnek verilmiştir.

    ```json
    {
        "access_token": "{Returned_Token}",
        "token_type": "bearer",
        "expires_in": 1200
    }
    ```

### <a name="uninstall-the-add-in"></a>Eklentiyi kaldırma

Eklentiyi kaldırmak için **Kaldır**'ı seçin. LCS'yi yenilediğinizde Stok Görünürlüğü Eklentisi kaldırılır. Kaldırma işlemi eklenti kaydını kaldırır ve hizmette depolanan tüm iş verilerini temizlemek için bir iş başlatır.

## <a name="inventory-visibility-add-in-public-api"></a>Stok Görünürlüğü Eklentisi genel API'sı

Stok Görünürlüğü Eklentisi'nin genel REST API'sı, birkaç özel tümleştirme uç noktası sunar. Üç ana etkileşim türünü destekler:

- Harici bir sistemden eldeki değişiklikleri eklentiye deftere nakletmek.
- Harici bir sistemden eldeki geçerli miktarları sorgulamak.
- Eldeki Supply Chain Management ile otomatik eşitleme.

Otomatik eşitleme, genel API'nın bir parçası değildir ancak Stok Görünürlüğü Eklentisi'ni etkinleştiren ortamlar için arka planda işlenir.

### <a name="authentication"></a>Kimlik Doğrulama

Platform güvenlik belirteci, Stok Görünürlüğü Eklentisi'ni çağırmak için kullanılır, bu nedenle Azure Active Directory uygulamanızı kullanarak bir Azure Active Directory belirteci oluşturmanız gerekir.

Güvenlik belirtecini alma hakkında daha fazla bilgi için bkz. [Stok Görünürlüğü Eklentisi'ni Yükleme](#install-add-in).

### <a name="configure-the-inventory-visibility-api"></a>Stok Görünürlüğü API'sını yapılandırma

Hizmeti kullanmadan önce, aşağıdaki alt bölümlerde açıklanan yapılandırmaları tamamlamanız gerekir. Yapılandırma, ortamınızın ayrıntılarına bağlı olarak değişebilir. Başlıca dört bölümden oluşur:

- [Bölümleme](#partitioning)
- [Boyut yapılandırmaları](#dimension-configurations)
- [Dizin oluşturma](#indexing)
- [Özel ölçüm](#custom-measurement)

#### <a name="partitioning"></a>Bölümleme

Bölümleme, Stok Görünürlüğü API'sının performansını önemli ölçüde etkileyebilir. Anlamlı veri sorgularına izin verirken küçük veri gruplandırmalarına olanak tanıyan bir düzen tanımlamak iyi bir fikirdir.

`organizationId` (Supply Chain Management'ta `dataAreaId`), her zaman bölümlemenin bir parçası olacaktır ve varsayılan olarak Stok Görünürlüğü, *Tesis + Konum* olarak boyutlara göre bölümlenecek şekilde ayarlanır. Bu, hizmetin her zaman filtrelerde tanımlanan bu boyutlarla sorgulanması gerektiği anlamına gelir.

> [!NOTE]
> *Tesis* ve *Konum*, Stok Görünürlüğü'nde iki genel varsayılan boyuttur. Supply Chain Management'ta, bu boyutlara *Tesis* (`InventSiteId`) ve *Ambar* (`InventLocationId`) adı verilir.

### <a name="dimension-configurations"></a>Boyut yapılandırmaları

Stok Görünürlüğü, birden çok kaynağın sistem tümleştirmesini etkinleştirmek için genel varsayılan boyutların bir listesini sağlar.

Aşağıdaki tabloda, Stok Görünürlüğü'nde varsayılan boyut adları olacak stok boyutları listelenmektedir.

| Boyut türü | Boyut adı |
|---|---|
| Ürün | `ColorId` |
| Ürün | `SizeId` |
| Ürün | `StyleId` |
| Ürün | `ConfigId` |
| İzleme | `BatchId` |
| İzleme | `SerialId` |
| Yer | `LocationId` |
| Yer | `SiteId` |
| Stok Durumu | `StatusId` |
| Ambara Özel | `WMSLocationId` |
| Ambara Özel | `WMSPalletId` |
| Ambara Özel | `LicensePlateId` |

> [!NOTE]
> Önceki tabloda listelenen boyut türü yalnızca referans içindir. Stok Görünürlüğü'nde boyut türünü tanımlamanız gerekmez.

Özel bir boyut varsa ve Stok Görünürlüğü tarafından tüketildiğinde varsayılan değere ayarlanması gerekiyorsa Stok Görünürlüğü'nde **Özel boyut** adını yapılandırabilirsiniz.

Harici sistemler, sorgulanacak belirli boyut kümeleri hakkında eldeki bilgilerin sorgulanmasını sağlayan RESTful API'lar aracılığıyla Stok Görünürlüğü'ne erişir. Tümleştirme için Stok Görünürlüğü, *dış kanal veri kaynağını* ve kaynak boyutunu Stok Görünürlüğü'ndeki *hedef boyutlara* yapılandırmanızı sağlar.

Hedef boyutlar aşağıdakilerden biri olmalıdır:

- Stok Görünürlüğü'ndeki varsayılan boyutlar
- Özel boyutlar

Boyut yapılandırmasının amacı, boyutlardaki sorgular ve boyutlarla deftere nakil olayı için çoklu sistem tümleştirmesini standartlaştırmaktır.

#### <a name="indexing"></a>Dizin oluşturma

Çoğu zaman, eldeki stok sorgusu yalnızca en yüksek "toplam" düzeyinde olmakla birlikte, sonuçları stok boyutlarına göre toplanmış olarak görmek isteyebilirsiniz.

Stok Görünürlüğü, boyuta veya boyutların karışımına göre dizinleri ayarlamanıza izin vererek esneklik sağlar.

> [!NOTE]
> Şu anda, yalnızca en fazla beş adet dizin yapılandırabilirsiniz. İş ihtiyaçlarınızı karşıladığından emin olmak için uygulamadan önce hangi boyutu veya boyut karışımını kullanacağınızı dikkatlice düşünmeniz gerekir. Örneğin, ürünleri aşağıdaki gibi sorgulamak istiyorsanız:

- Kümelenmiş ürün eldeki verilerini *Renk* ve *Boyut* boyutlarına göre sorgulayın.
- Bazı durumlarda, ürün üzerinde toplu olarak sorgu yapmak istersiniz.

Aşağıdaki gibi tanımlanan iki dizininiz olur:

- `["ColorId", "SizeId"]`
- `[]`

Boş köşeli ayraç, bölüm içindeki ürün kimliğine göre kümelenir.

Dizin oluşturma, sonuçlarınızı `groupBy` sorgu ayarına göre nasıl gruplanabileceğinizi tanımlar. Bu durumda, herhangi bir `groupBy` değeri tanımlamazsanız, toplamları `productid` değerine göre alırsınız. Aksi takdirde, `groupBy=ColorId&groupBy=SizeId` olarak `groupBy` tanımlarsanız sistemde farklı renk ve boyut kombinasyonlarına dayalı olarak döndürülen birden çok satır alırsınız.

Sorgu ölçütlerinizi istek gövdesine koyabilirsiniz.

Renk ve boyut kombinasyonuna sahip ürün üzerinde gerçekleştirilen bir sorgu örneği.

```json
{
    "filters": {
        "OrganizationId": ["usmf"],
        "ProductId": ["MyProduct"],
        "LocationId": ["21"],
        "SiteId": ["2"],
        "ColorId": ["Red"]
    },
    "groupByValues": [
        "SizeId",
        "ColorId"
    ],
    "returnNegative": true
}
```

#### <a name="custom-measurement"></a>Özel ölçüm

Varsayılan ölçüm miktarları Supply Chain Management'a bağlıdır, ancak varsayılan ölçümlerin bir karışımından oluşan bir miktara sahip olmak isteyebilirsiniz. Bunu yapmak için eldeki sorguların çıktısına eklenecek özel miktarlar yapılandırmanız olabilir.

İşlev, özel ölçümü oluşturmak için eklenecek bir dizi ölçü ve/veya çıkarılacak bir dizi ölçü belirlemenize olanak tanır.

Örneğin, aşağıdaki sorgu koşulunda, `MyCustomAvailableforReservation` özel ölçüm miktarını tüketim sistemi tarafından tüketilecek şekilde yapılandırabilirsiniz.

```json
[
    {
        "productId": "MyProduct",
        "dimensions": {
            "colorid": "Red"
        },
        "quantities": {
            "mypos": {
                "outbound": 20.0,
                "inbound": 80.0
            },
            "fno": {
                "availphysical": 100.0,
                "orderedintotal": 50.0,
                "orderedreserved": 10.0
            },
            "exterchannel": {
                "received": 90.0,
                "scheduled": 30.0,
                "issued": 60.0,
                "reserved": 40.0
            }
        }
    }
]

```



| Tüketim sistemi | Hesaplanan ölçümler | Veri kaynağı | Değiştirici | Değiştirici hesaplama türü |
|---|---|---|---|---|
| `CustomChannel` | `MyCustomAvailableforReservation` | `fno` | `availphysical` | Fark hesap eki |
| `CustomChannel` | `MyCustomAvailableforReservation` | `fno` | `orderedintotal` | Fark hesap eki |
| `CustomChannel` | `MyCustomAvailableforReservation` | `fno` | `orderedreserved` | Çıkarma |
| `CustomChannel` | `MyCustomAvailableforReservation` | `mypos` | `inbound` | Fark hesap eki |
| `CustomChannel` | `MyCustomAvailableforReservation` | `mypos` | `outbound` | Çıkarma |
| `CustomChannel` | `MyCustomAvailableforReservation` | `exterchannel` | `received` | Fark hesap eki |
| `CustomChannel` | `MyCustomAvailableforReservation` | `exterchannel` | `scheduled` | Fark hesap eki |
| `CustomChannel` | `MyCustomAvailableforReservation` | `exterchannel` | `issued` | Çıkarma |
| `CustomChannel` | `MyCustomAvailableforReservation` | `exterchannel` | `reserved` | Çıkarma |

Bununla, özel ölçüm miktarı üzerindeki sorgu, aşağıdaki çıktıyı döndürecektir.

```json
[
    {
        "productId": "MyProduct",
        "dimensions": {
            "colorid": "Red"
        },
        "quantities": {
            "mypos": {
                "outbound": 20.0,
                "inbound": 80.0
            },
            "fno": {
                "availphysical": 100.0,
                "orderedintotal": 50.0,
                "orderedreserved": 10.0
            },
            "exterchannel": {
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

`MyCustomAvailableforReservation` çıktısı, aşağıdaki gibi, özel ölçümlerdeki hesaplama ayarına dayanır:  
 *100 + 50 + 80 + 90 + 30 &ndash; 10 &ndash; 20 &ndash; 60 &ndash; 40 = 220*

### <a name="posting-on-hand-changes"></a>Eldeki değişiklikleri deftere nakletme

Etkinliğin yayınlanacağı URL, coğrafi bölgenize bağlıdır. Şu şekilde olacaktır:

`https://{serviceURL}/api/environment/{environmentId}/onhand`

Kimlik doğrulaması yapıldığında, bu URL, hizmete eldeki değişiklik olaylarını göndermek için HTTP `POST` yöntemiyle birlikte kullanılabilir.

Dynamics 365 hizmetleriyle HTTP istekleri üzerinden iletişim kurmak için özel bir üst bilgi kullanılır ve verilerin bağlı olduğu Supply Chain Management kurulumunun ortam kimliğini belirtir. Örneğin:

`x-ms-environment-id: 2db79622-f97a-4d64-9844-d12efed41796`

#### <a name="posting-on-hand-changes-query-example-1"></a>Eldeki değişikliklerle ilgili sorguyu deftere nakletme örneği 1

Bu örnekte Power Apps'te boyut yapılandırmasını ayarlayacağınız bir senaryo gösterilmektedir.

Power Apps'te boyut eşlemesini yapılandırmak için aşağıdaki sorguyu kullanın:

```json
{
    "PosSizeId": "SizeId",
    "PosColorId": "ColorId",
    "PosSiteId": "SiteId",
    "PosLocationId": "LocationId"
}
```

Artık sorgularınızda `dimensionDataSource` belirtebilir ve özel boyutları kullanabilirsiniz. Sistem, özel boyutları otomatik olarak temel boyutlara dönüştürür.

```json
{
    "id": "demo-test-00007",
    "organizationId": "usmf",
    "productId": "MyProduct",
    "quantities": {
        "pos": {
            "Outbound": 1
        }
    },
    "dimensionDataSource": "pos",
    "dimensions": {
        "PosSizeId": "Large",
        "PosColorId": "Red",
        "PosSiteId": "2",
        "PosLocationId": "21"
    }
}
```

#### <a name="posting-on-hand-changes-query-example-2"></a>Eldeki değişikliklerle ilgili sorguyu deftere nakletme örneği 2

Bu örnekte, Power Apps'te boyut yapılandırması için eşlemelerin ayarlandığı bir senaryo gösterilmektedir, bu nedenle deftere nakil de temel boyutları kullanmalıdır. `dimensionDataSource` alanı null, boş veya boşluk olduğunda tüm boyutlar temel boyutlar olmalıdır.

```json
{
    "id": "demo-test-00007",
    "organizationId": "usmf",
    "productId": "MyProduct",
    "quantities": {
        "pos": {
            "Outbound": 1
        }
    },
    "dimensions": {
        "SizeId": "Large",
        "ColorId": "Red",
        "SiteId": "2",
        "LocationId": "21"
    }
}
```

#### <a name="json-document-field-properties"></a>JSON belge alanı özellikleri

Daha önce sağlanan JSON sorgu örneklerindeki alanlar aşağıdaki tabloda listelenen özelliklere sahiptir.

| Alan kodu | Tanım |
|---|---|
| `id` | Belirli bir değişiklik olayı için benzersiz bir kimlik. Bu kimlik, deftere nakil sırasında hizmetle iletişim başarısız olursa olursa olayın yeniden gönderilmesinin aynı olayın sistemde iki kez sayılmasıyla sonuçlanmamasını sağlamak için kullanılır. |
| `organizationId` | Olayla bağlantılı kuruluşun tanımlayıcısı. Bu, Supply Chain Management kuruluşları veya veri alanı kimlikleriyle eşlenir. |
| `productId` | Söz konusu ürünün tanımlayıcısı. |
| `quantity` | Eldeki miktarın değiştirilmesi gereken miktar. Örneğin, bir rafa 10 yeni simit eklenseydi, bu değer 10 olur. Raftan 3 simit çıkarılırsa veya satılırsa bu değer -3 olur. |
| `dimensionDataSource` | Deftere nakil değişikliği olayı ve sorgusunda kullanılan boyutların veri kaynağı. Veri kaynağını belirtirseniz belirtilen veri kaynağındaki özel boyutları kullanabilirsiniz. Boyut yapılandırmasıyla, Stok Görünürlüğü özel boyutları genel varsayılan boyutlarla eşleştirebilir. `dimensionDataSource` belirtilmemişse sorgularınızda yalnızca genel varsayılan boyutları kullanabilirsiniz.   |
| `dimensions` | Anahtar/değer çiftlerinden oluşan dinamik bir set. Bunlar Supply Chain Management'taki bazı boyutlarla eşlenir ancak olay Supply Chain Management'tan veya harici bir sistemden geliyorsa gösterebilecek özel boyutlar *(Kaynak* gibi) da ekleyebilirsiniz. |

### <a name="querying-current-on-hand"></a>Mevcut eldeki miktarı sorgulama

Mevcut eldeki miktarı sorgulamak için uç noktası, benzer bir URL'ye sahip olacaktır:

`https://{serviceURL}/api/environment/{environmentId}/onhand/indexquery`

HTTP `POST` yöntemi ile sorgulanacaktır.

#### <a name="current-on-hand-query-example-1"></a>Geçerli eldeki miktar sorgusu örneği 1

Bu örnekte Power Apps'te boyut yapılandırmasını zaten tamamladığınız bir senaryo gösterilmektedir.

Power Apps'te boyut eşlemesini yapılandırmak için aşağıdaki sorguyu kullanın:

```json
{
    "PosSizeId": "SizeId",
    "PosColorId": "ColorId",
    "PosSiteId": "SiteId",
    "PosLocationId": "LocationId"
}
```

Artık sorgularınızda `dimensionDataSource` belirtebilir ve özel boyutları kullanabilirsiniz. Sistem, özel boyutları otomatik olarak temel boyutlara dönüştürür. `DimensionDataSource` değerini `filters` içinde belirtebilir ve özel boyutları hem `filters` hem de `groupByValues` ile gelirtebilirsiniz. Sistem, özel boyutları otomatik olarak temel boyutlara dönüştürür.

```json
{
    "filters": {
        "OrganizationId": ["usmf"],
        "ProductId": ["MyProduct"],
        "DimensionDataSource": ["Pos"],
        "PosLocationId": ["21"],
        "PosSiteId": ["2"],
        "PosColorId": ["Red"]
    },
    "groupByValues": [
        "PosSizeId",
        "PosColorId"
    ],
    "returnNegative": true
}
```

#### <a name="current-on-hand-query-example-2"></a>Geçerli eldeki miktar sorgusu örneği 2

Bu örnekte, Power Apps'te boyut yapılandırması için eşlemelerin ayarlandığı bir senaryo gösterilmektedir, bu nedenle deftere nakil de temel boyutları kullanmalıdır. `filters` altındaki `dimensionDataSource` alanı null, boş veya boşluk olduğunda tüm boyutlar temel boyutlar olmalıdır.

```json
{
    "filters": {
        "OrganizationId": ["usmf"],
        "ProductId": ["MyProduct"],
        "LocationId": ["21"],
        "SiteId": ["2"],
        "ColorId": ["Red"]
    },
    "groupByValues": [
        "SizeId",
        "ColorId"
    ],
    "returnNegative": true
}
```

#### <a name="example-return-result"></a>Örnek döndürme sonucu

Önceki örneklerde gösterilen sorgular böyle bir sonuç döndürebilir.

```json
[
    {
        "productId": "MyProduct",
        "dimensions": {
            "colorid": "Red"
        },
        "quantities": {
            "mypos": {
                "outbound": 20.0,
                "inbound": 80.0
            },
            "fno": {
                "availphysical": 100.0,
                "orderedintotal": 50.0,
                "orderedreserved": 10.0
            },
            "exterchannel": {
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

Miktar alanlarının ölçümler sözlüğü ve ilişkili değerleri şeklinde yapılandırıldığını unutmayın.
