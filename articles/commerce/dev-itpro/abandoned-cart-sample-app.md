---
title: Bırakılmış alışveriş sepetlerini algılama ve müşterilere bildirimler gönderme
description: Bu konu, Microsoft Dynamics 365 Commerce terk edilen sepetleri algılamak ve müşterilere anımsatıcı e-posta bildirimleri göndermek için bırakılan sepet bağlayıcısı örnek uygulamasını nasıl özelleştireceğinizi açıklar.
author: bicyclingfool
ms.date: 02/25/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: stuharg
ms.search.validFrom: 2017-06-20
ms.openlocfilehash: 1db4e988653aa55db2b18fb201edeafc4d16a1bc
ms.sourcegitcommit: ab690bc897699ff8a4c489e749251fe0367050ca
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/26/2022
ms.locfileid: "8489042"
---
# <a name="detect-abandoned-carts-and-send-notifications-to-customers"></a>Bırakılmış alışveriş sepetlerini algılama ve müşterilere bildirimler gönderme

[!include [banner](../includes/banner.md)]

Bu konu, Microsoft Dynamics 365 Commerce terk edilen sepetleri algılamak ve müşterilere anımsatıcı e-posta bildirimleri göndermek için bırakılan sepet bağlayıcısı örnek uygulamasını nasıl özelleştireceğinizi açıklar.

Terk edilen sepet bildirimleri aracılığıyla geliri kurtarma ve müşterileri tutma becerisi, Dynamics 365 Commerce'in desteklediği önemli bir özelliktir. Commerce terk edilmiş sepet bağlayıcısı örnek uygulamasını özelleştiren perakendeciler, perakendeci tarafından belirlenen bir zaman içinde değiştirilmemiş olan Perakende Sunucusundaki alışveriş sepetlerine erişebilir. Bu sepetler daha sonra alınabilir, ürün ve müşteri verileriyle geliştirilebilir ve e-posta bildirimleri oluşturup bunları müşterilere gönderecek üçüncü taraf e-posta pazarlama sağlayıcılarına iletilebilir.

Müşterilerin aldığı terk edilen sepet e-posta bildiriminde aşağıdaki bilgiler yer alabilir:

- Müşterinin adı.
- Müşterinin soyadı.
- Müşteri e-posta adresi.
- Müşteriyi, alışveriş sepetine döndüren bir URL.
- Hareketin para birimi.
- Müşterinin sepetindeki ürünlerin listesi. Her ürün için aşağıdaki bilgiler yer alır:

    - Ürünün görünen adı
    - Ürün kimliği (bir URL'yi ürün açıklaması sayfasına birleştirmek için kullanılır)
    - Farklı görünüm penceresi boyutlarına uyacak şekilde otomatik olarak yeniden boyutlandırılan ürün görüntüsü
    - Ürün resmi için alternatif metin
    - Ürünün birim fiyatı

## <a name="abandoned-cart-connector-sample"></a>Terk edilmiş sepet bağlayıcısı örneği

Microsoft'un perakende yazılım geliştirme seti (SDK) aracılığıyla sağladığı bağlayıcı modeli, terk edilen sepet bilgilerinin alınmasını ve üçüncü taraf e-posta pazarlama sağlayıcısına gönderilmesini sağlar. Bu bağlayıcı, Perakende Sunucusu ile iletişimi yönetir, güvenlik için Azure Key Vault kullanır, belirli bir zaman penceresi için sepet alımı gerçekleştirir ve sipariş ve ürün verilerini alır. Ayrıca üçüncü taraf e-posta pazarlama sağlayıcısıyla tümleştirme için örnek bir uygulama da sağlar. Bağlayıcı, kullanıma hazır olarak [Emarsys](https://emarsys.com) ile iletişim kuracak şekilde tasarlanmıştır. Ancak, Constant Contact, Mailchip ve SendGrid gibi farklı çözümlerle de kolaylıkla tümleştirilebilir.

Aşağıdaki şekil, terk edilen sepet bağlayıcısı örnek uygulamasının bileşenlerini gösterir.

![Terk edilen sepet bağlayıcısı örnek uygulaması bileşenleri](media/AbandonedCartConnector.png)

> [!IMPORTANT]
> Bazı bölgeler, müşterilerin alışveriş sepetlerine bir e-posta pazarlama sağlayıcısına aktarılmasını veya verilerinin kaldırılmasına talep etmesini gerektirebilir. Ancak, Microsoft bu seçenekleri müşteriler için sağlamaz. Bu nedenle, bunları zorunlu kılan bölgelerde iş yapmayı planlıyorsanız, müşterilerin tercihlerini izlemek ve bunlara dayalı olarak, müşteri verilerinin e-posta platformunuza geçirilmesini önlemek için gerekli altyapıyı ve özelleştirmeleri sağlamanız gerekir. Müşterinin isteğindeki, e-posta pazarlama sağlayıcınızdan müşteri verilerini temizleme işlemini de tanımlamanız gerekir.

## <a name="obtain-the-code-sample"></a>Kod örneğini elde etme

Terk edilen sepet bağlayıcısı örnek uygulaması, 10.0.16 sürümüyle birlikte Perakende SDK içinde bulunur. Kod, **\\RetailSDK\\Code\\SampleExtensions\\RetailServer\\Extensions.AbandonedCartSample** altında bulunabilir. Retail SDK ve elde etme hakkında daha fazla bilgi için bkz. [Retail yazılım geliştirme seti (SDK)](retail-sdk/retail-sdk-overview.md).

> [!NOTE]
> Örnek kod ilk olarak sürüm 10.0.16 yapılarında kullanılabilir ancak perakende sunucusunun sürüm 10.0.13 ve sonraki sürümleri ile uyumludur.

## <a name="prerequisites-and-dependencies"></a>Önkoşullar ve bağımlılıklar

Terk edilen sepet bağlayıcısı örnek kodunu dağıtmadan ve konfigüre etmeden önce aşağıdaki önkoşulların karşılanması gerekir.

### <a name="access-to-commerce-resources"></a>Commerce kaynaklarına erişim

Terk edilen sepet bağlayıcı uygulamasını konfigüre etmek ve dağıtmak için aşağıdaki Commerce kaynaklarına erişiminizin olması gerekir:

- Ortamınız için Commerce genel merkeze yönetici erişimi
- Ortamınız için yaşam Microsoft Dynamics Lifecycle Services (LCS) projesine erişim

### <a name="azure-cosmos-db"></a>Azure Cosmos DB

Terk edilen sepet bağlayıcı uygulaması daha önce alınmış olan sepetlerin kimliklerini ve zaman damgalarını izlemek için Azure Cosmos DB kullanır. Bu verileri kalıcı hale getirmek için Azure Cosmos DB kullanabilirsiniz veya kod örneğini başka bir veri saklama seçeneği ile tümleştirebilecek şekilde özelleştirebilirsiniz. Azure Cosmos DB hakkında daha fazla bilgi için bkz [Azure Cosmos DB'ye hoş geldiniz](/azure/cosmos-db/introduction).

Azure Cosmos DB kullanıyorsanız örneği çalıştırmadan önce aşağıdaki önkoşulların yerine getirilmesi gerekir:

- Etkin bir Azure Cosmos DB hesabınız olmalıdır. Hesabınız yoksa bkz. [Veritabanı hesabı oluşturma](/azure/cosmos-db/create-sql-api-dotnet#create-a-database-account).
- Azure portaldaki Azure Cosmos DB hesabınızın **Anahtarlar** penceresinden **URI** ve **BİRİNCİL ANAHTAR** (veya **İKİNCİL ANAHTAR**) değerlerini almanız gerekir. Azure Cosmos DB hesabınızla ilgili bitiş noktası ve anahtar bilgilerinin nasıl alınacağı hakkında daha fazla bilgi için, bkz. [Erişim anahtarları ve parolaları görüntüleme, kopyalama ve yeniden oluşturma](/azure/cosmos-db/manage-account#keys).

### <a name="azure-key-vault"></a>Azure Key Vault

Terk edilen sepet bağlayıcısı uygulaması, güvenli erişim gerektiren farklı bileşenlerin adlarını ve gizli parolalarını saklamak için Anahtar Kasası kullanır.

Anahtar kasası ayarlamak için aşağıdaki adımları izleyin.

1. [Portalı kullanarak Azure Stack Hub'da Anahtar Kasasını yönetme](/azure-stack/user/azure-stack-key-vault-manage-portal?view=azs-2002&preserve-view=true) bölümündeki talimatları izleyin.
2. Aşağıdaki bilgiler için gizli diziler oluşturun:

    - Emarsys uygulama programlama arabirimi (API) kullanıcı adı ve API parolası
    - Terk edilen sepet uygulama kimliği ve gizli dizisi

Terk edilen sepet bağlayıcısı örnek kodu, Anahtar Kasasına erişmek için Azure varsayılan kimlik bilgilerini kullanır. Anahtar Kasasına erişim planladığınız kimlik için **Liste** ve **Okuma** izinleri sağlamanız gerekir.

Azure varsayılan kimlik bilgileri hakkında daha fazla bilgi için bkz: [DefaultAzureCredential Sınıfı](/dotnet/api/azure.identity.defaultazurecredential?view=azure-dotnet&preserve-view=true).

## <a name="create-an-abandoned-cart-connector-sample-app-application-id-for-the-azure-ad-tenant"></a>Azure AD kiracısı için terk edilen bir sepet bağlayıcısı örneği uygulama kimliği oluşturma

Azure Active Directory (AD) kiracısı için terk edilen bir sepet bağlayıcısı örneği uygulama kimliği oluşturmanız gerekir. Uygulama kimliği oluşturma hakkında bilgi için bkz. [Kaynaklara erişebilen bir Azure AD uygulaması ve hizmet sorumlusu oluşturmak için portalı kullanma](/azure/active-directory/develop/howto-create-service-principal-portal).

## <a name="add-the-abandoned-cart-connector-sample-app-application-id-to-the-allow-list-for-the-retail-server-api"></a>Perakende sunucu API'si için izin verilenler listesine bırakılan sepet bağlayıcısı örnek uygulaması uygulama kimliğini ekleyin

Ardından, perakende sunucu API'si için izin verilenler listesine bırakılan sepet bağlayıcısı örnek uygulaması uygulama kimliğini eklemeniz gerekir. Azure'de izin verilenler listesine uygulama kimliği ekleme hakkında daha fazla bilgi için bkz. [Perakende Sunucusunda Hizmetten Hizmete kimlik doğrulama desteği](https://community.dynamics.com/ax/b/axforretail/posts/support-for-service-to-service-authentication-in-retail-server).

## <a name="configure-the-abandoned-cart-connector-sample-app"></a>Terk edilen sepet bağlayıcısı örnek uygulamasını yapılandırma

Terk edilen sepet bağlayıcısı örnek uygulamasını konfigüre etmek için **AbandonedCartDetectionSample** dizininin kökünde bulunan **appSettings.json** yapılandırma dosyasını değiştirin. Aşağıdaki tablolarda konfigürasyon dosyası özellikleri açıklanmaktadır.

### <a name="keyvaultoptions"></a>KeyVaultOptions

| Özellik    | Açıklama |
| ----------- | ----------- |
| KeyVaultURI | Azure portalında kullandığınız anahtar kasanın Etki Alanı Adı Sistemi (DNS) adı. |

### <a name="retailserverclientoptions"></a>RetailServerClientOptions

| Özellik                                      | Açıklama |
| --------------------------------------------- | ----------- |
| TenantId                                      | Azure kiracınızın Azure AD kiracı kimliği. |
| RetailServerAudienceId                        | Perakende Sunucusu hedef kitle kodu. Varsayılan değeri bırakabilirsiniz. |
| AppIdKeyVaultSecretName                       | Terk edilen sepet bağlayıcısı örnek uygulaması uygulama kimliği için oluşturduğunuz gizli dizinin adı. |
| AppSecretKeyVaultSecretName                   | Terk edilen sepet bağlayıcısı örnek uygulaması uygulama kimliğinin uygulama gizli dizisini saklayan gizli dizinin adı. |
| RetailServerUrl                               | Perakende Sunucusu örneğinizin URL'si. Bu değeri LCS'de bulabilirsiniz. |
| OperatingUnitNumber                           | Faaliyet birim numarası (OUN). Bu değeri Commerce genel merkezinde bulabilirsiniz. |
| IncludeAbandonedCartsModifiedSinceLastMinutes | Geri almak istediğiniz terk edilen sepetlerin zaman penceresinin başlangıcı. Değer, geçerli zamandan önceki dakika sayısı olarak ifade edilir. Örneğin, 120 dakika öncelik zaman içinde değiştirilmiş tüm sepetleri almak için bu özelliği ve **ExcludeAbandonedCartsModifiedSinceLastMinutes** özelliği tarafından belirlenen süre sonunu **120** olarak ayarlayın. |
| ExcludeAbandonedCartsModifiedSinceLastMinutes | Geri almak istediğiniz terk edilen sepetlerin zaman penceresinin sonu. Değer, geçerli zamandan önceki dakika sayısı olarak ifade edilir. Örneğin **IncludeAbandonedCartsModifiedSinceLastMinutes** özelliği **120** olarak ayarlanmışsa son 120 dakika ve 30 dakika arasında değiştirilmiş tüm sepetleri almak için bu özelliği **30** olarak ayarlayın. Uygulamada bu özellik, bir sepetin terk edilmeden önce beklemek istediğiniz süreyi tanımlar. |
| ReturnToCartUrl                               | E-ticaret sitenizdeki sepetin URL'si, **app.config** dosyasında kullanılan biçimde. |

### <a name="azurecosmosoptions"></a>AzureCosmosOptions

Terk edilen sepeti alma işi durumu, sepet kimlikleri ve değiştirilen zaman damgaları Azure Cosmos DB'de saklanır. Varsayılan olarak yapılandırma dosyası noktasındaki ayarlar, Azure Cosmos DB'nin yerel öykünücü örneğine işaret eder. Bağlayıcıyı üretime dağıttığınızda, bu ayarları Azure aboneliğinizdeki Azure Cosmos DB örneğine işaret edecek şekilde güncelleştirmeniz gerekir. Yerel veya korumalı alanda test için [Azure Cosmos DB Emulator'ü](/azure/cosmos-db/local-emulator) kullanabilirsiniz.

| Özellik    | Açıklama |
| ----------- | ----------- |
| EndPointUri | Azure veya öykünücü tarafından sağlanan uç nokta URI. |
| PrimaryKey  | Azure veya öykünücü tarafından sağlanan birincil anahtar. |
| DatabaseId  | Veritabanı kimliği. Varsayılan değeri bırakabilir veya kendi değerinizi girebilirsiniz. |
| ContainerId | Konteyner kodu. Varsayılan değeri bırakabilir veya kendi değerinizi girebilirsiniz. |

### <a name="emarsysclientoptions"></a>EmarsysClientOptions

> [!NOTE]
> Emarsys dışında bir e-posta pazarlama sağlayıcısıyla tümleştirme sağlıyorsanız bu sağlayıcı ile iletişim kurmak için **IEmailProvider** arabirimini uygun şekilde genişletmeniz gerekir.

| Özellik                      | Açıklama |
| ----------------------------- | ----------- |
| ApiUrl                        | `https://api.emarsys.net/api/v2/event/{0}/trigger` |
| ExternalEventId               | Emarsys'te oluşturulan dış olay kaydının kimliği. Terk edilmiş sepet e-posta bildirimleri göndermek üzere oluşturduğunuz kampanyada, **Tetikleme ayarları** altında değeri bulabilirsiniz. |
| ApiUserNameKeyVaultSecretName | Emarsys API kullanıcı adının saklandığı anahtarın adı. |
| ApiSecretKeyVaultSecretName   | Emarsys API gizli dizisinin saklandığı anahtarın adı. |
| EmarsysContactKeyId           | Emarsys ilgili kişi veritabanındaki e-posta sütununun kodu. Varsayılan değer **3**'dür ve değiştirilmesi gerekmez. |

### <a name="mediaoptions"></a>MediaOptions

Commerce'te e-ticaret özellikleri kullanıyorsanız ürün görüntüleri almak için Commerce dijital valrık yönetimini kullanabilirsiniz. Dijital varlık yönetiminde resim boyutlandırıcı hakkında daha fazla bilgi edinmek için bkz. [ImageSettings görünüm penceresi yapılandırması](../e-commerce-extensibility/image-component.md#imagesettings-viewport-configuration).

| Özellik                             | Açıklama |
| ------------------------------------ | ----------- |
| ImageServerUrl                       | Sitenizin dijital varlık yöneticisinin kök URL'si. Değeri, Commerce genel merkezindeki **Retail ve Commerce \> Kanal kurulumu \> Kanal profilleri** altında **Medya Sunucu Temel URL** bölümünde bulabilirsiniz. |
| ImageViewPorts                       | Bağımsız görünüm penceresi yapılandırmaları için kapsayıcı düğüm. |
| ImageViewPorts/viewport              | Görünüm penceresi açıklaması. Piksel cinsinden görünüm penceresinde genişlik aralıklarını belirlemek için bu özelliği kullanın. Bu özelliğin nasıl kullanıldığını gösteren bir örnek görmek için **appSettings.json** yapılandırma dosyasını inceleyin. |
| ImageViewPorts/imageWidth            | Piksel cinsinden görünüm penceresinin görüntü genişliği. |
| imageViewPorts/imageHeight           | Piksel cinsinden görünüm penceresinin görüntü yüksekliği. |
| imageViewPorts/useForDefaultImageTag | Görünüm penceresi tarafından belirlenen görüntü boyutlarının, web tarayıcı veya e-posta istemcisi için `<picture>` HTML etiketi desteklenmiyorsa kullanılıp kullanmaması gerektiğini gösteren bir **doğru**/**yanlış** değeri. |

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
