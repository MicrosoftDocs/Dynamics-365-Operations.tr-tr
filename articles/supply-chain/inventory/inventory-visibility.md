---
title: Stok Görünürlüğü Eklentisi
description: Bu konu, Dynamics 365 Supply Chain Management için Stok Görünürlüğü Eklentisinin nasıl yüklendiğini ve yapılandırıldığını açıklar.
author: sherry-zheng
ms.date: 10/26/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2020-10-26
ms.dyn365.ops.version: Release 10.0.15
ms.openlocfilehash: 8faae53f66c069c53609dee72fa30ca18a22c9eb8a86b4669c745c00976af34d
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/05/2021
ms.locfileid: "6742716"
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

Daha fazla bilgi için bkz. [Lifecycle Services kaynakları](../../fin-ops-core/dev-itpro/lifecycle-services/lcs.md).

### <a name="inventory-visibility-add-in-prerequisites"></a>Stok Görünürlüğü Eklentisi ön koşulları

Stok Görünürlüğü Eklentisi'ni yüklemeden önce aşağıdakileri yapmanız gerekir:

- En az bir ortam dağıtılan bir LCS uygulama projesi edinin.
- [Eklentilere genel bakış](../../fin-ops-core/dev-itpro/power-platform/add-ins-overview.md)'ta sağlanan eklentileri ayarlama ön koşullarının tamamlandığından emin olun. Stok Görünürlüğü, çift yazma bağlantısı gerektirmez.
- Aşağıdaki üç gerekli dosyayı almak için [inventvisibilitysupp@microsoft.com](mailto:inventvisibilitysupp@microsoft.com) adresinden Stok Görünürlüğü Ekibi'ne başvurun:
  - `Inventory Visibility Dataverse Solution.zip`
  - `Inventory Visibility Configuration Trigger.zip`
  - `Inventory Visibility Integration.zip` (Supply Chain Management'ın çalıştırdığınız bu sürümü 10.0.18 sürümünden daha eskiyse)
- Buna ek olarak, aşağıdaki Package Deployer paketlerini almak için [inventvisibilitysupp@microsoft.com](mailto:inventvisibilitysupp@microsoft.com) adresinden Stok Görünürlüğü Ekibi'ne başvurun: Bu paketler, resmi bir Package Deployer aracı tarafından kullanılabilir.
  - `InventoryServiceBase.PackageDeployer.zip`
  - `InventoryServiceApplication.PackageDeployer.zip`(Bu paket, `InventoryServiceBase` paketindeki tüm değişiklikleri ve ek kullanıcı arabirimi uygulama bileşenlerini içerir)
- Bir uygulamayı kaydettirmek ve Azure aboneliğiniz altında AAD'ye istemci gizli anahtarı eklemek için [Hızlı Başlangıç: Bir uygulamayı Microsoft kimlik platformuna kaydetme](/azure/active-directory/develop/quickstart-register-app) bölümünde verilen yönergeleri izleyin.
  - [Uygulama kaydetme](/azure/active-directory/develop/quickstart-register-app)
  - [İstemci gizli anahtarı](/azure/active-directory/develop/quickstart-register-app#add-a-certificate)
  - **Uygulama(İstemci) Kimliği**, **İstemci Gizli Anahtarı** ve **Kiracı Kimliği** aşağıdaki adımlarda kullanılacaktır.

> [!NOTE]
> Şu anda desteklenen ülkeler/bölgeler arasında Kanada, ABD ve Avrupa Birliği (AB) bulunmaktadır.

Bu ön koşullarla ilgili herhangi bir sorunuz varsa lütfen Stok Görünürlüğü ürün takımıyla iletişime geçin.

### <a name="set-up-dataverse"></a><a name="setup-microsoft-dataverse"></a>Ayarlama Dataverse

Dataverse'ü Stok Görünürlüğüyle kullanılacak şekilde ayarlamak için, önce önkoşulları hazırlamanız ve sonra Dataverse'ü Package Deployer aracını kullanarak mı yoksa çözümleri el ile içe aktararak mı ayarlayacağınıza karar vermeniz gerekir. Ardından Stok Görünürlüğü Eklentisini yükleyin. Aşağıdaki alt kısımlar, bu görevlerin nasıl tamamlanacağını açıklar.

#### <a name="prepare-dataverse-prerequisites"></a>Dataverse önkoşullarını hazırlama

Dataverse'ü kurmaya başlamadan önce, aşağıdakileri gerçekleştirerek kiracınıza bir hizmet ilkesi ekleyin:

1. Azure AD PowerShell Modülü v2'yi [ Graph için Azure Active Directory PowerShell'i Yüklema](/powershell/azure/active-directory/install-adv2) bölümünde açıklandığı gibi yükleyin.

1. Aşağıdaki PowerShell komutunu çalıştırın:

    ```powershell
    Connect-AzureAD # (open a sign in window and sign in as a tenant user)
    
    New-AzureADServicePrincipal -AppId "3022308a-b9bd-4a18-b8ac-2ddedb2075e1" -DisplayName "d365-scm-inventoryservice"
    ```

#### <a name="set-up-dataverse-using-the-package-deployer-tool"></a>Package Deployer aracını kullanarak Dataverse'ü kurma

Önkoşulları yerine getirdikten sonra, Dataverse'ü Package Deployer aracını kullanarak ayarlamayı tercih ediyorsanız aşağıdaki prosedürü kullanın. Bunun yerine, çözümlerin el ile nasıl içe aktarılacağı hakkında ayrıntılı bilgi için sonraki bölüme bakın (iki yöntemi birden uygulamayın).

1. Geliştirici araçlarını, [NuGet'ten araçları indirme](/dynamics365/customerengagement/on-premises/developer/download-tools-nuget) bölümünde açıklandığı şekilde yükleyin.

1. İş gereksinimlerinize göre, `InventoryServiceBase` veya `InventoryServiceApplication` paketini seçin.

1. Çözümleri içe aktarın:
    1. `InventoryServiceBase` paketi için:
        - `InventoryServiceBase.PackageDeployer.zip` zip dosyasını açın
        - `InventoryServiceBase` klasörünü, `[Content_Types].xml` dosyasını, `Microsoft.Dynamics.InventoryServiceBase.PackageExtension.dll` dosyasını, `Microsoft.Dynamics.InventoryServiceBase.PackageExtension.dll.config` dosyasını ve `Microsoft.Dynamics.InventoryServiceBase.PackageExtension.dll.config` dosyasını bulun. 
        - Bu klasör ve dosyaların her birini, geliştirici araçlarını yüklediğinizde oluşturulan `.\Tools\PackageDeployment` dizinine kopyalayın.
    1. `InventoryServiceApplication` paketi için:
        - `InventoryServiceApplication.PackageDeployer.zip` zip dosyasını açın
        - `InventoryServiceApplication` klasörünü, `[Content_Types].xml` dosyasını, `Microsoft.Dynamics.InventoryServiceApplication.PackageExtension.dll` dosyasını, `Microsoft.Dynamics.InventoryServiceApplication.PackageExtension.dll.config` dosyasını ve `Microsoft.Dynamics.InventoryServiceApplication.PackageExtension.dll.config` dosyasını bulun.
        - Bu klasör ve dosyaların her birini, geliştirici araçlarını yüklediğinizde oluşturulan `.\Tools\PackageDeployment` dizinine kopyalayın.
    1. `.\Tools\PackageDeployment\PackageDeployer.exe`'yi yürütün. Çözümleri içe aktarmak için ekranınızdaki talimatları izleyin.

1. Uygulama kullanıcısına güvenlik rolleri atayın.
    1. Dataverse ortamınızın URL'sini açın.
    1. **Gelişmiş Ayarlar \> Sistem \> Güvenlik \> Kullanıcılar**'a gidin ve **# InventoryVisibility** adlı kullanıcıyı bulun.
    1. **Rol Ata**'yı ve sonra **Sistem Yöneticisi**'ni seçin. **Common Data Service Kullanıcısı** adlı bir rol varsa bunu da seçin.

#### <a name="set-up-dataverse-manually-by-importing-solutions"></a>Çözümleri içe aktararak Dataverse'ü elle kurma

Önkoşulları yerine getirdikten sonra, Dataverse'ü çözümleri elle içe aktararak ayarlamayı tercih ediyorsanız aşağıdaki prosedürü kullanın. Bunun yerine Package Deployer aracının kullanımıyla ilgili ayrıntılar için önceki bölüme bakın (iki yöntemi birden uygulamayın).

1. Dataverse'te Stok Görünürlüğü için bir uygulama kullanıcısı oluşturun:

    1. Dataverse ortamınızın URL'sini açın.
    1. **Gelişmiş Ayar \> Sistem \> Güvenlik \> Kullanıcılar**'a gidin ve bir uygulama kullanıcısı oluşturun. Sayfa görünümünü **Uygulama Kullanıcıları** olarak değiştirmek için görünüm menüsünü kullanın.
    1. **Yeni**'yi seçin. Uygulama kimliğini *3022308a-b9bd-4a18-b8ac-2ddedb2075e1* olarak ayarlayın. (Değişikliklerinizi kaydettiğinizde nesne kimliği otomatik olarak yüklenir.) Adı özelleştirebilirsiniz. Örneğin *Stok Görünürlüğü* olarak ayarlayabilirsiniz. Tamamladıktan sonra **Kaydet**'i seçin.
    1. **Rol Ata**'yı ve sonra **Sistem Yöneticisi**'ni seçin. **Common Data Service Kullanıcısı** adlı bir rol varsa onu da seçin.

    Daha fazla bilgi için bkz. [Uygulama kullanıcısı oluşturma](/power-platform/admin/create-users-assign-online-security-roles#create-an-application-user).

1. Dataverse varsayılan diliniz **İngilizce** değilse:

    1. **Gelişmiş Ayar \> Yönetim \>Diller**'e gidin,
    1. **İngilizce (LanguageCode=1033)** dilini ve **Uygula**'yı seçin.

1. Dataverse yapılandırmasıyla ilgili varlıkları ve Power Apps'i içeren `Inventory Visibility Dataverse Solution.zip` dosyasını içeri aktarın:

    1. **Çözümler** sayfasına gidin.
    1. **İçe aktar**'ı seçin.

1. Yapılandırma yükseltme tetikleyici akışını içeri aktarın:

    1. Microsoft Flow sayfasına gidin.
    1. *Dataverse (eski)* olarak adlandırılan bağlantının mevcut olduğundan emin olun. (Yoksa oluşturun.)
    1. `Inventory Visibility Configuration Trigger.zip` dosyasını içeri aktarın. İçeri aktarıldıktan sonra tetikleyici **Akışlarım** altında görünecektir.
    1. Ortam bilgilerine bağlı olarak aşağıdaki dört değişkeni başlatın:

        - Azure Kiracısı Kimliği
        - Azure Uygulaması İstemci Kimliği
        - Azure Uygulaması Gizli Anahtarı
        - Stok Görünürlüğü Uç Noktası

            Bu değişken hakkında daha fazla bilgi için bu konuda ele alınacak olan [Stok Görünürlüğü tümleştirmesini ayarlama](#setup-inventory-visibility-integration) bölümüne bakın.

        ![Yapılandırma tetikleyicisi.](media/configuration-trigger.png "Yapılandırma tetikleyicisi")

    1. **Aç**'ı seçin.

### <a name="install-the-add-in"></a><a name="install-add-in"></a>Eklentiyi yükleme

Stok Görünürlüğü Eklentisi'ni yüklemek için aşağıdakileri yapın:

1. [Lifecycle Services (LCS)](https://lcs.dynamics.com/Logon/Index) portalında oturum açın.
1. Ana sayfada, ortamınızın dağıtıldığı projeyi seçin.
1. Proje sayfasında, eklentiyi yüklemek istediğiniz ortamı seçin.
1. Ortam sayfasında, **Power Platform tümleştirmesi** bölümünde Dataverse ortamı adını bulabileceğiniz **Ortam eklentileri** bölümünü görene kadar aşağı kaydırın.
1. **Ortam eklentileri** bölümünde, **Yeni bir eklenti yükleyin**'i seçin.

    ![LCS'deki ortam sayfası.](media/inventory-visibility-environment.png "LCS'deki ortam sayfası")

1. **Yeni eklenti yükleyin** bağlantısını seçin. Kullanılabilir eklentilerin bir listesi görüntülenir.
1. Listeden **Stok Görünürlüğü**'nü seçin.
1. Ortamınızın aşağıdaki alanlarının değerlerini girin:

    - **AAD uygulaması (istemci) kimliği**
    - **AAD kiracı kimliği**

    ![Eklenti kurulum sayfası.](media/inventory-visibility-setup.png "Eklenti kurulum sayfası")

1. **Şartlar ve koşullar** onay kutusunu seçerek şartlar ve koşulları kabul edin.
1. **Yükle**'yi seçin. Eklentinin durumu **Yükleniyor** olarak görünür. İşlem bittiğinde, durumun **Yüklendi** olarak değiştiğini görmek için sayfayı yenileyin.

### <a name="uninstall-the-add-in"></a><a name="uninstall-add-in"></a>Eklentiyi kaldırma

Eklentiyi kaldırmak için **Kaldır**'ı seçin. LCS'yi yenilediğinizde Stok Görünürlüğü Eklentisi kaldırılır. Kaldırma işlemi eklenti kaydını kaldırır ve hizmette depolanan tüm iş verilerini temizlemek için bir iş başlatır.

## <a name="consume-on-hand-inventory-data-from-supply-chain-management"></a>Supply Chain Management'tak eldeki stok verilerini kullanma

### <a name="deploy-the-inventory-visibility-integration-package"></a><a name="deploy-inventory-visibility-package"></a>Stok Görünürlüğü tümleştirme paketini dağıtma

Supply Chain Management sürüm 10.0.17 veya önceki bir sürümünü çalıştırıyorsanız paket dosyasını almak için [inventvisibilitysupp@microsoft.com](mailto:inventvisibilitysupp@microsoft.com) adresinden Stok Görünürlüğü yerleşik destek ekibine başvurun. Ardından LCS'de paketi dağıtın.

> [!NOTE]
> Dağıtım sırasında bir sürüm uyuşmazlığı hatası oluşursa X++ projesini geliştirme ortamınıza el ile içeri aktarmanız gerekir. Daha sonra, dağıtılabilir paketi geliştirme ortamınızda oluşturun ve üretim ortamınızda dağıtın.
> 
> Kod, Supply Chain Management sürüm 10.0.18'e dahildir. Bu sürümü veya sonraki bir sürümünü çalıştırıyorsanız dağıtım gerekli değildir.

Supply Chain Management ortamınızda aşağıdaki özelliklerin açık olduğundan emin olun. (Varsayılan olarak bunlar açıktır.)

| Özellik açıklaması | Kod sürümü | Sınıfı değiştirme |
|---|---|---|
| InventSum tablosunda stok boyutlarını kullanmayı etkinleştirme veya devre dışı bırakma | 10.0.11 | InventUseDimOfInventSumToggle |
| InventSumDelta tablosunda stok boyutlarını kullanmayı etkinleştirme veya devre dışı bırakma | 10.0.12 | InventUseDimOfInventSumDeltaToggle |

### <a name="set-up-inventory-visibility-integration"></a><a name="setup-inventory-visibility-integration"></a>Stok Görünürlüğü tümleştirmesini kurma

1. Supply Chain Management'ta **[Özellik yönetimi](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)** çalışma alanını açın ve **Stok Görünürlüğü Tümleştirmesi** özelliğini açın.
1. **Stok Yönetimi \> Kurulum \> Stok Görünürlüğü Tümleştirme parametreleri**'ne gidin ve Stok Görünürlüğü'nü çalıştırdığınız ortamın URL'sini girin.

    LCS ortamınızın Azure bölgesini bulun ve URL'yi girin. URL aşağıdaki biçimde olur:

    `https://inventoryservice.<RegionShortName>-il301.gateway.prod.island.powerapps.com`

    Örneğin, Avrupa'daysanız ortamınızda aşağıdaki URL'lerden biri bulunur:

    - `https://inventoryservice.neu-il301.gateway.prod.island.powerapps.com`
    - `https://inventoryservice.weu-il301.gateway.prod.island.powerapps.com`

    Şu anda aşağıdaki bölgeler kullanılabilirdir.

    | Azure bölgesi | Bölge kısa adı |
    |---|---|
    | Doğu Avustralya | eau |
    | Güneydoğu Avustralya | seau |
    | Orta Kanada | cca |
    | Doğu Kanada | eca |
    | Kuzey Avrupa | neu |
    | Batı Avrupa | weu |
    | Doğu ABD | eus |
    | Batı ABD | wus |

1. **Stok Yönetimi \> Periyodik \> Stok Görünürlüğü Tümleştirmesi**'ne gidin ve işi etkinleştirin. Supply Chain Management'taki tüm stok değişikliği olayları artık Stok Görünürlüğü'ne nakledilecektir.

## <a name="the-inventory-visibility-add-in-public-api"></a><a name="inventory-visibility-public-api"></a>Stok Görünürlüğü Eklentisi genel API'si

Stok Görünürlüğü Eklentisi'nin genel REST API'si, birkaç özel tümleştirme uç noktası sunar. Üç ana etkileşim türünü destekler:

- Harici bir sistemden eldeki stok değişiklikleri eklentiye deftere nakletmek
- Harici bir sistemden eldeki geçerli miktarları sorgulamak
- Supply Chain Management eldeki stoku ile otomatik eşitlemek

Otomatik eşitleme genel API kapsamında değildir. Bunun yerine, Stok Görünürlüğü Eklentisi'nin etkinleştirildiği ortamlar için arka planda işlenir.

### <a name="authentication"></a><a name="inventory-visibility-authentication"></a>Kimlik Doğrulama

Platform güvenlik belirteci, Stok Görünürlüğü Eklentisi'ni çağırmak için kullanılır. Bu nedenle, Azure AD uygulamanızı kullanarak bir *Azure Active Directory (Azure AD) belirteci* oluşturmanız gerekir. Daha sonra güvenlik hizmetinden *erişim belirtecini* almak için Azure AD belirteci kullanmanız gerekir.

Aşağıdakileri gerçekleştirerek güvenlik hizmeti belirteci alın:

1. Azure portalda oturum açın ve Supply Chain Management uygulamanız için `clientId` ve `clientSecret` bilgilerini bulmak için portalı kullanın.
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

### <a name="sample-request"></a><a name="inventory-visibility-sample-request"></a>Örnek İstek

İncelemeniz için örnek bir http isteği verilmiştir. Bu isteği göndermek için herhangi bir aracı veya kodlama dilini kullanabilirsiniz (örneğin ``Postman``).

```json
# Url
# replace {RegionShortName} and {EnvironmentId} with your value
https://inventoryservice.{RegionShortName}-il301.gateway.prod.island.powerapps.com/api/environment/{EnvironmentId}/onhand

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
    "quantities": {
        "pos": {
            "inbound": 5
        }  
    },
    "dimensions": {
        "SizeId": "Small",
        "ColorId": "Red",
        "SiteId": "1",
        "LocationId": "11"
    }
}
```

### <a name="configure-the-inventory-visibility-api"></a><a name="inventory-visibility-configuration"></a>Stok Görünürlüğü API'sını yapılandırma

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
        "ProductId": ["MyProduct1", "MyProduct2"],
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

`filters` alanı için şu anda yalnızca `ProductId` birden çok değeri desteklemektedir. `ProductId` boş bir diziyse, tüm ürünler sorgulanır.

#### <a name="custom-measurement"></a>Özel ölçüm

Varsayılan ölçüm miktarları Supply Chain Management'a bağlıdır. Ancak varsayılan ölçümlerin birleşiminden oluşan bir miktara sahip olmak isteyebilirsiniz. Bunu yapmak için eldeki sorguların çıktısına eklenecek özel miktarlar yapılandırmanız olabilir.

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


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
