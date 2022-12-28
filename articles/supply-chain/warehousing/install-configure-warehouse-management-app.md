---
title: Warehouse Management mobil uygulamasını yükleme ve bağlama
description: Bu konuda, Ambar Yönetimi mobil uygulamasının mobil cihazlarınızın her birine nasıl yükleneceği ve Microsoft Dynamics 365 Supply Chain Management ortamınıza bağlanacak şekilde nasıl yapılandırılacağı açıklanmaktadır.
author: Mirzaab
ms.date: 02/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SysAADClientTable, WHSMobileAppField, WHSMobileAppFieldPriority, WHSRFMenu, WHSRFMenuItem, WHSWorker
audience: Application User, IT Pro
ms.reviewer: kamaybac
ms.custom: 267694
ms.assetid: d95d43b2-13ff-4189-a71a-3a1fb57d55ed
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: mirzaab
ms.search.validFrom: 2021-02-28
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: 1333881f80c735794784831d4042bfe7d070b796
ms.sourcegitcommit: bdee5e642d417a13abdb778c14ec5f2dbbf8dee7
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 12/09/2022
ms.locfileid: "9838485"
---
# <a name="install-and-connect-the-warehouse-management-mobile-app"></a>Warehouse Management mobil uygulamasını yükleme ve bağlama

[!include [banner](../includes/banner.md)]

Bu konuda, Ambar Yönetimi uygulamasının mobil cihazlarınızın her birine nasıl indirilip yükleneceği ve uygulamanın Supply Chain Management ortamınıza bağlanacak şekilde nasıl yapılandırılacağı açıklanmaktadır. Her cihazı el ile yapılandırabilir veya bir dosya ya da bir QR kodunu tarayarak bağlantı ayarlarını içe aktarabilirsiniz.

## <a name="system-requirements"></a>Sistem gereksinimleri

Ambar Yönetimi mobil uygulaması hem Windows hem de Google Android işletim sistemleri için kullanılabilir. Uygulamayı kullanmak için mobil cihazlarınızda aşağıdaki işletim sistemlerinden biri yüklü olmalıdır:

- Windows 10 (Evrensel Windows Platformu \[UWP\]) Ekim 2018 güncelleştirmesi 1809 (derleme 10.0.17763) veya sonraki bir sürüm
- Android 4.4 veya üstü

## <a name="turn-warehouse-management-mobile-app-features-on-or-off-in-supply-chain-management"></a>Supply Chain Management'ta Warehouse Management mobile app özelliklerini açma veya kapatma

Warehouse Management mobile app kullanmak için, *Yeni ambar uygulaması için kullanıcı ayarları, simgeler ve adım başlıkları* özelliğinin sisteminizde açık olması gerekir. Supply Chain Management 10.0.25 itibarıyla, bu özellik zorunludur ve kapatılamaz. 10.0.25 sürümünden daha eski bir sürümü çalıştırıyorsanız, yöneticiler [Özellik yönetimi](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) çalışma alanında *Yeni ambar uygulaması için kullanıcı ayarları, simgeler ve adım başlıkları* özelliğini aratarak bu işlevi açabilir veya kapatabilir.

## <a name="get-the-warehouse-management-mobile-app"></a>Ambar Yönetimi mobil uygulamasını edinme

Daha küçük dağıtımlar için uygulamayı her bir cihazdaki ilgili mağazadan yüklemek ve ardından kullandığınız ortamlara olan bağlantıyı el ile yapılandırmak isteyebilirsiniz.

Daha büyük dağıtımlar için uygulama dağıtımını ve/veya yapılandırmayı otomatikleştirebilirsiniz ve bu seçenek birçok cihazı yönetiyorsanız daha rahat olabilir. Örneğin, [Microsoft Intune](/mem/intune/fundamentals/what-is-intune) gibi bir mobil cihaz yönetimi ve mobil uygulama yönetimi çözümü kullanabilirsiniz. Uygulama eklemek için Intune'u kullanma hakkında bilgi için bkz. [Microsoft Intune'a uygulama ekleme](/mem/intune/apps/apps-add).

### <a name="install-the-app-from-an-app-store"></a>Uygulamayı bir uygulama mağazasından yükleme

Uygulamayı tek bir cihaza yüklemenin en kolay yolu, her zaman en son genel sürümü sağlayan bir uygulama mağazasından yüklemektir. Microsoft Intune, uygulama mağazalarındaki uygulamaları da getirebilir. Uygulamayı uygulama mağazasından yüklemek için aşağıdaki bağlantılardan birini kullanın:

- **Windows (UWP):** [Microsoft Store'da Ambar Yönetimi](https://www.microsoft.com/store/apps/9pd35cdqcmg3)

- **Android:** [Google Play Store'da Ambar Yönetimi](https://play.google.com/store/apps/details?id=com.Microsoft.WarehouseManagement)

### <a name="download-the-app-from-microsoft-app-center"></a>Uygulamayı Microsoft App Center'dan indirme

Bir uygulama mağazasından yüklemeye alternatif olarak uygulamayı Microsoft App Center'dan da indirebilirsiniz. App Center, dışarıdan yükleyebileceğiniz yüklenebilir paketler sağlar. Geçerli sürüme ek olarak, App Center önceki sürümleri indirmenize de olanak tanır ve deneyebileceğiniz yaklaşan özelliklerle önizleme sürümleri sağlayabilir. Ambar Yönetimi mobil uygulamasının geçerli, önceki veya önizleme sürümlerini Microsoft App Center'dan indirmek için aşağıdaki bağlantılardan birini kullanın:

- **Windows (UWP):** [Ambar Yönetimi (Windows)](https://aka.ms/wma-windows-official-release)  
    İndirilen paketi bir Windows cihaza yükleme ve ardından gerekli sertifikaları ayarlama hakkında yönergeler için bkz. [App Center'dan Bir Derleme İndirme](/appcenter/distribution/installation).

- **Android:** [Ambar Yönetimi (Android)](https://aka.ms/wma-android-official-release)  
    Önizleme sürümünü indirirseniz yüklemek için birkaç ek adım gerekir. Ayrıntılar için bkz. [Android Uygulamalarını Test Etme](/appcenter/distribution/testers/testing-android).

App Center'dan indirilen bir derlemeyi yükleme hakkında bilgi için bkz. [Derleme yükleme](/appcenter/distribution/installation).

## <a name="create-a-web-service-application-in-azure-active-directory"></a><a name="create-service"></a>Azure Active Directory içinde bir web hizmeti uygulaması oluşturma

Ambar Yönetimi mobil uygulamasının belirli bir Supply Chain Management sunucusuyla etkileşime girmesini sağlamak için Azure Active Directory (Azure AD) uygulamasında Supply Chain Management kiracısı için bir web hizmeti uygulaması kaydetmeniz gerekir. Aşağıdaki yordamda, bu görevi tamamlamanın bir yolu gösterilmektedir. Ayrıntılı bilgi ve alternatifler için yordamdan sonraki bağlantılara bakın.

1. Web tarayıcısında [https://portal.azure.com](https://portal.azure.com/) adresine gidin.
1. Azure aboneliğine erişimi olan kullanıcının adını ve parolasını girin.
1. Azure portalında, sol gezinti bölmesinde, **Azure Active Directory** uygulamasını seçin.

    ![Azure Active Directory.](media/app-connect-azure-aad.png "Azure Active Directory")

1. Supply Chain Management tarafından kullanılan Azure AD örneğiyle çalıştığınızdan emin olun.
1. **Yönet** listesinde **Uygulama kayıtları**'nı seçin.

    ![Uygulama kayıtları.](media/app-connect-azure-register.png "Uygulama kayıtları")

1. **Uygulamayı kaydet** sihirbazını açmak için araç çubuğunda **Yeni kayıt**'ı seçin.
1. Uygulama için bir ad girin, **Yalnızca bu kuruluş dizinindeki hesaplar** seçeneğini belirleyin ve ardından **Kayıt**'ı seçin.

    ![Uygulama kaydetme sihirbazı.](media/app-connect-azure-register-wizard.png "Uygulama kaydetme sihirbazı")

1. Yeni uygulama kaydınız açıldı. Daha sonra gereksinim duyacağınız **Uygulama (istemci) Kodu** değerini not edin. Bu kod, bu makalede daha sonra *istemci kimliği* olarak ifade edilecektir.

    ![Uygulama (istemci) kodu.](media/app-connect-azure-app-id.png "Uygulama (istemci) kodu")

1. **Yönet** listesinde **Sertifika ve parolalar**'ı seçin. Ardından, uygulamayı kimlik doğrulama için nasıl yapılandırmak istediğinize bağlı olarak aşağıdaki düğmelerden birini seçin. (Daha fazla bilgi için bu makalenin ilerisindeki [Sertifika veya istemci parolası kullanarak kimlik doğrulaması](#authenticate) bölümüne bakın.)

    - **Karşıya yükleme sertifikası**: Bir sertifikayı parola olarak kullanmak için karşıya yükleyin. Daha güvenli ve tamamen otomatikleştirilebilir olduğu için bu yaklaşımı öneriyoruz. Ambar Yönetimi mobil uygulamasını Windows cihazlarında çalıştırıyorsanız sertifikayı yükledikten sonra gösterilen **Parmak İzi** değerini not edin. Sertifikayı Windows cihazlarında yapılandırırken bu değere ihtiyacınız olacaktır.
    - **Yeni istemci parolası**: **Parolalar** bölümüne bir anahtar açıklama ve süre girerek bir anahtar oluşturun ve **Ekle**'yi seçin. Anahtarın bir kopyasını oluşturun ve güvenli bir şekilde saklayın.

    ![Sertifika ve parolalar.](media/app-connect-azure-authentication.png "Sertifika ve parolalar")

Azure AD uygulamasında web hizmeti uygulamalarını ayarlama hakkında daha fazla bilgi için aşağıdaki kaynaklara bakın:

- Azure AD uygulamasında web hizmeti uygulamalarını ayarlamak için Windows PowerShell'in nasıl kullanılacağını gösteren yönergeler için bkz. [Nasıl yapılır: Sertifikalı bir hizmet sorumlusu oluşturmak için Azure PowerShell'i kullanma](/azure/active-directory/develop/howto-authenticate-service-principal-powershell).
- Azure AD uygulamasında el ile bir web hizmeti uygulaması oluşturma hakkında ayrıntılı bilgi için aşağıdaki makalelere bakın:

    - [Hızlı Başlangıç: Microsoft kimlik platformu ile bir uygulamayı kaydetme](/azure/active-directory/develop/quickstart-register-app)
    - [Nasıl yapılır: Kaynaklara erişebilen bir Azure AD uygulaması ve hizmet sorumlusu oluşturmak için portalı kullanma](/azure/active-directory/develop/howto-create-service-principal-portal)

## <a name="create-and-configure-a-user-account-in-supply-chain-management"></a><a name="user-azure-ad"></a>Supply Chain Management içinde bir kullanıcı hesabı oluşturma ve yapılandırma

Supply Chain Management'ın Azure AD uygulamanızı kullanmasını sağlamak için aşağıdaki adımları izleyin.

1. Ambar Yönetimi mobil uygulaması için kullanıcı kimlik bilgilerine karşılık gelen bir kullanıcı oluşturun:

    1. Supply Chain Management uygulamasında **Sistem yönetimi \> Kullanıcıları \> Kullanıcıları**'na gidin.
    1. Kullanıcı oluşturun.
    1. *Ambarlama mobil cihaz kullanıcısı* rolünü kullanıcıya atayın.

    ![Ambarlama mobil cihaz kullanıcısını atayın.](media/app-connect-app-users.png "Ambarlama mobil cihaz kullanıcısını atama")

1. Azure AD uygulamanızı, Ambar Yönetimi mobil uygulaması kullanıcısı ile ilişkilendirin:

    1. **Sistem yönetimi \> Kurulum \> Azure Active Directory uygulamaları**'na gidin.
    1. Eylem Bölmesinde, bir satır oluşturmak için **Yeni**'yi seçin.
    1. **İstemci kimliği** alanında, önceki bölümde not ettiğiniz istemci kimliğini girin.
    1. **Ad** alanına, bir ad girin.
    1. **Kullanıcı kimliği** alanında, yeni oluşturduğunuz kullanıcı kimliğini seçin.

    ![Azure Active Directory uygulamaları.](media/app-connect-aad-apps.png "Azure Active Directory uygulamaları")

> [!TIP]
> Bu ayarları kullanmanın bir yolu, fiziksel aygıtlarınızın her biri için Azure'da bir istemci kimliği oluşturmak ve sonra her bir istemci kodunu **Azure Active Directory uygulamalar** sayfasına eklemektir. Sonrasında, cihaz kaybolursa cihazın Supply Chain Management erişimini bu sayfadan istemci kimliğini kaldırarak kolayca kaldırabilirsiniz. (Bu yaklaşım, bu konunun ilerisinde anlatıldığı gibi, her aygıta kaydedilen bağlantı kimlik bilgileri de bir istemci kimliği belirtmesine karşı çalışır.)
>
> Ek olarak, her istemci kimliği için varsayılan dil, sayı biçimi ve saat dilimi ayarları, burada eşlenen **Kullanıcı kimliği** değeri için ayarlanmış tercihlerde oluşturulur. Bu nedenle, istemci kimliğine göre her aygıt veya aygıt koleksiyonunda varsayılan ayar oluşturmak için bu tercihleri kullanabilirsiniz. Ancak, bir çalışanın cihazda oturum açmak için kullandığı *ambar uygulama kullanıcı hesabı* için de tanımlanmışsa, bu varsayılan ayarlar geçersiz kılınır. (Daha fazla bilgi için [Mobil aygıt kullanıcı hesapları](mobile-device-work-users.md) bölümüne bakın.)

## <a name="authenticate-by-using-a-certificate-or-client-secret"></a><a name="authenticate"></a>Sertifika veya istemci parolası kullanarak kimlik doğrulama

Azure AD ile kimlik doğrulaması, bir mobil cihazı Supply Chain Management uygulamasında bağlamak için güvenli bir yol sağlar. İstemci parolası veya sertifika kullanarak kimlik doğrulaması yapabilirsiniz. Bağlantı ayarlarını içe aktaracaksanız istemci parolası yerine bir sertifika kullanmanızı öneririz. İstemci parolasının her zaman güvenli bir şekilde saklanması gerektiğinden, bu makalede daha sonra açıklandığı gibi istemci parolasını bir bağlantı ayarları dosyasından veya bir QR kodundan içe aktaramazsınız.

Sertifikalar, bir belirteç istendiğinde uygulamanın kimliğini kanıtlamak için parola olarak kullanılabilir. Sertifikanın genel kısmı Azure portalındaki uygulama kaydına yüklenirken tam sertifikanın Ambar Yönetimi mobil uygulamasının yüklü olduğu her cihaza dağıtılması gerekir. Kuruluşunuz sertifikayı, rotasyonu vb. konularda yönetmekle sorumludur. Kendinden imzalı sertifikalar kullanabilirsiniz ancak her zaman dışa aktarılamayan sertifikalar kullanmalısınız.

Sertifikayı, Ambar Yönetimi mobil uygulamasını çalıştırdığınız her cihazda yerel olarak kullanılabilir hale getirmelisiniz. Intune kullanıyorsanız, Intune denetimli cihazlara yönelik sertifikaları yönetme hakkında bilgi için bkz. [Microsoft Intune'da kimlik doğrulama için sertifika kullanma](/mem/intune/protect/certificates-configure).

## <a name="configure-the-warehouse-management-mobile-app-for-cloud-and-edge-scale-units"></a>Bulut ve uç ölçek birimleri için Warehouse Management mobil uygulamasını yapılandırma

Warehouse Management mobil uygulamasını bir bulut veya uç ölçek birimi ile karşılaştırarak çalıştırmayı planlıyorsanız fazladan birkaç adım gereklidir. Talimatlar için bkz. [Bulut ve uç ölçek birimleri için Warehouse Management mobil uygulamasını yapılandırma](../cloud-edge/cloud-edge-workload-setup-warehouse-app.md).

## <a name="configure-the-application-by-importing-connection-settings"></a>Bağlantı ayarlarını içe aktararak uygulamayı yapılandırma

Uygulamanın birçok mobil cihazda bakımını ve dağıtımını kolaylaştırmak için bağlantı ayarlarını her bir cihaza el ile girmek yerine içe aktarabilirsiniz. Bu bölümde, ayarların nasıl oluşturulacağı ve içe aktarılacağı açıklanmaktadır.

### <a name="create-a-connection-settings-file-or-qr-code"></a>Bağlantı ayarları dosyası veya QR kodu oluşturma

Bağlantı ayarlarını bir dosyadan veya bir QR kodundan alabilirsiniz. Her iki yaklaşım için de önce JavaScript Nesne Gösterimi (JSON) biçimini ve söz dizimini kullanan bir ayar dosyası oluşturmanız gerekir. Dosya, eklenmesi gereken her bir bağlantıyı içeren bir bağlantı listesi içermelidir. Aşağıdaki tabloda bağlantı ayarları dosyasında belirtmeniz gereken parametreler özetlenmektedir.

| Parametre | Tanım |
|---|---|
| ConnectionName | Bağlantı ayarlarının adını belirtin. En fazla 20 karakter kullanılabilir. Bu değer, bir bağlantı ayarının benzersiz tanımlayıcısı olduğu için listede benzersiz olduğundan emin olun. Cihazda aynı ada sahip bir bağlantı zaten varsa içe aktarılan dosyadaki ayarlar tarafından geçersiz kılınır. |
| ActiveDirectoryClientAppId | [Azure Active Directory uygulamasında bir web hizmeti uygulaması oluşturma](#create-service) bölümünde Azure AD uygulamasını ayarlarken not ettiğiniz istemci kimliğini belirtin. |
| ActiveDirectoryResource | Supply Chain Management uygulamasının kök URL'sini belirtin. |
| ActiveDirectoryTenant | Supply Chain Management sunucusuyla kullandığınız Azure AD etki alanı adını belirtin. Bu değer `https://login.windows.net/<your-Azure-AD-domain-name>` formuna sahiptir. İşte bir örnek: `https://login.windows.net/contosooperations.onmicrosoft.com`. Azure AD etki alanı adınızı bulma hakkında daha fazla bilgi için bkz. [Kullanıcının önemli kimliklerini bulma](/partner-center/find-ids-and-domain-names). |
| Şirket | Uygulamanın bağlanmasını istediğiniz tüzel varlığı Supply Chain Management uygulamasında belirtin. |
| ConnectionType | (İsteğe bağlı) Bağlantı ayarının bir ortama bağlanmak için sertifika veya istemci parolası kullanıp kullanmayacağını belirtin. Geçerli değerler *"certificate"* ve *"clientsecret"* değerleridir. Varsayılan değer *"certificate"* değeridir.<p>**Not:** İstemci parolaları içe aktarılamaz.</p> |
| IsEditable | (İsteğe bağlı) Uygulama kullanıcısının bağlantı ayarını düzenleyip düzenleyemeyeceğini belirtin. Geçerli değerler *"true"* ve *"false"* değerleridir. Varsayılan değer *"true"* değeridir. |
| IsDefault | (İsteğe bağlı) Bağlantının varsayılan bağlantı olup olmadığını belirtin. Varsayılan bağlantı olarak ayarlanan bir bağlantı, uygulama açıldığında otomatik olarak önceden seçilir. Yalnızca tek bir bağlantı varsayılan bağlantı olarak ayarlanabilir. Geçerli değerler *"true"* ve *"false"* değerleridir. Varsayılan değer *"false"* değeridir. |
| CertificateThumbprint | (İsteğe bağlı) Windows cihazlarında bağlantı için sertifika parmak izini belirleyebilirsiniz. Android cihazlarında, uygulama kullanıcısının bir bağlantı ilk kez kullanıldığında sertifikayı seçmesi gerekir. |

Aşağıdaki örnek, iki bağlantı içeren geçerli bir bağlantı ayarları dosyasını gösterir. Gördüğünüz gibi bağlantı listesi (dosyada *"ConnectionList"* olarak adlandırılır), her bağlantıyı bir nesne olarak depolayan bir diziye sahip bir nesnedir. Her nesne parantez içine alınmalı ({}) ve virgülle ayrılmalıdır ve dizi, parantez içine alınmalıdır (\[\]).

```json
{
    "ConnectionList": [
        {
            "ActiveDirectoryClientAppId":"aaaaaaaa-bbbb-ccccc-dddd-eeeeeeeeeeee",
            "ConnectionName": "Connection1",
            "ActiveDirectoryResource": "https://yourenvironment.cloudax.dynamics.com",
            "ActiveDirectoryTenant": "https://login.windows.net/contosooperations.onmicrosoft.com",
            "Company": "USMF",
            "IsEditable": false,
            "IsDefaultConnection": true,
            "CertificateThumbprint": "aaaabbbbcccccdddddeeeeefffffggggghhhhiiiii",
            "ConnectionType": "certificate"
        },
        {
            "ActiveDirectoryClientAppId":"aaaaaaaa-bbbb-ccccc-dddd-eeeeeeeeeeee",
            "ConnectionName": "Connection2",
            "ActiveDirectoryResource": "https://yourenvironment2.cloudax.dynamics.com",
            "ActiveDirectoryTenant": "https://login.windows.net/contosooperations.onmicrosoft.com",
            "Company": "USMF",
            "IsEditable": true,
            "IsDefaultConnection": false,
            "ConnectionType": "clientsecret"
        }
    ]
}
```

Bilgileri bir JSON dosyası olarak kaydedebilir veya aynı içeriğe sahip bir QR kodu oluşturabilirsiniz. Bilgileri bir dosya olarak kaydederseniz, özellikle her mobil cihazda varsayılan konumda saklayacaksanız, *connections.json* varsayılan adını kullanarak kaydetmenizi öneririz.

### <a name="save-the-connection-settings-file-on-each-device"></a>Bağlantı ayarları dosyasını her cihaza kaydetme

Genellikle, bağlantı ayarları dosyalarını yönettiğiniz her cihazda dağıtmak için bir cihaz yönetim aracı veya komut dosyası kullanırsınız. Bağlantı ayarları dosyasını her bir cihaza kaydettiğinizde varsayılan adı ve konumu kullanırsanız Ambar Yönetimi mobil uygulaması, uygulama yüklendikten sonraki ilk çalıştırmada bile dosyayı otomatik olarak içe aktarır. Dosya için özel bir ad veya konum kullanırsanız uygulama kullanıcısının değerleri, ilk çalıştırma sırasında belirtmesi gerekir. Ancak, uygulama daha sonra belirtilen adı ve konumu kullanmaya devam eder.

Uygulama her başlatıldığında, herhangi bir değişiklik olup olmadığını belirlemek için bağlantı ayarlarını önceki konumlarından yeniden içe aktarır. Uygulama yalnızca bağlantı ayarları dosyasındaki bağlantılarla aynı ada sahip bağlantıları güncelleştirecektir. Diğer adları kullanan, kullanıcı tarafından oluşturulan bağlantılar güncellenmez.

Bağlantı ayarları dosyasını kullanarak bir bağlantıyı kaldıramazsınız.

Daha önce de belirtildiği gibi varsayılan dosya adı *connections.json* şeklindedir. Varsayılan dosya konumu, bir Windows cihazı mı yoksa Android cihazı mı kullandığınıza bağlıdır:

- **Windows:** `C:\Users\<User>\AppData\Local\Packages\Microsoft.WarehouseManagement_8wekyb3d8bbwe\LocalState`
- **Android:** `Android\data\com.Microsoft.WarehouseManagement\files`

Genellikle yollar, uygulamanın ilk çalıştırılmasından sonra otomatik olarak oluşturulur. Ancak, kurulumdan önce bağlantı ayarları dosyasını cihaza aktarmanız gerekiyorsa bunları el ile olarak oluşturabilirsiniz.

> [!NOTE]
> Uygulama kaldırılırsa varsayılan yol ve içeriği kaldırılır.

### <a name="import-the-connection-settings"></a>Bağlantı ayarlarını içe aktarma

Bağlantı ayarlarını bir dosyadan veya bir QR kodundan içe aktarmak için aşağıdaki adımları izleyin.

1. Mobil cihazınızda Ambar Yönetimi mobil uygulamasını başlatın. Uygulamayı ilk kez başlattığınızda, bir hoş geldiniz iletisi görüntülenir. **Bir bağlantı seç**'i seçin.

    ![Karşılama iletisi.](media/app-configure-welcome-screen.png "Hoş geldiniz iletisi")

1. Bağlantı ayarlarını bir dosyadan içeri aktarıyorsanız ve dosya kaydedilirken varsayılan ad ve konunm kullanılmışsa uygulama, dosyayı zaten bulmuş olabilir. Bu durumda 4. adıma geçin. Aksi durumda, **Bağlantıyı ayarla**'yı sçein ve ardından 3. adıma geçin.

    ![Bağlantı kurma.](media/app-configure-set-up-connection.png "Bağlantı kur")

1. **Bağlantı kurulumu** iletişim kutusunda, ayarları nasıl içeri aktarmak istediğinize bağlı olarak **Dosyadan ekle** veya **QR kodundan ekle** seçeneklerinden birini belirleyin.

    - Bağlantı ayarlarını bir dosyadan içeri aktarıyorsanız **Dosyadan ekle**'yi seçin, yerel cihazınızda dosyaya göz atın ve dosyayı seçin. Özel bir konum seçerseniz uygulama konumu kaydeder ve bir sonraki sefer otomatik olarak kullanır.
    - QR kodunu tarayarak bağlantı ayarlarını içerş aktarıyorsanız **QR kodundan ekle**'yi seçin. Uygulama, cihazın kamerasını kullanmak için sizden izin ister. İzin verdikten sonra kamera başlatılır, böylece tarama için kullanılabilir. Cihazın kamerasının kalitesine ve QR kodunun karmaşıklığına bağlı olarak doğru bir tarama elde etmekte zorlanabilirsiniz. Bu durumda, her QR kodu için yalnızca bir bağlantı oluşturarak QR kodunun karmaşıklığını azaltmaya çalışın. (Şu anda, QR kodunu taramak için yalnızca cihazın kamerasını kullanabilirsiniz.)

    ![Bağlantı kurulumu menüsü.](media/app-configure-connection-setup-flyout.png "Bağlantı kurulum menüsü")

1. Bağlantı ayarları başarıyla yüklendiğinde, seçilen bağlantı gösterilir.

    ![Bağlantı ayarları yüklendi.](media/app-configure-select-connection.png "Bağlantı ayarları yüklendi")

1. Android cihazı kullanıyorsanız ve kimlik doğrulama için bir sertifika kullanıyorsanız cihaz sizden sertifikayı seçmenizi ister.

    ![Android cihazda sertifika komutunu seçme.](media/app-configure-select-certificate.png "Android cihazda sertifika komutunu seçme")

1. Uygulama, Supply Chain Management sunucunuza bağlanır ve oturum açma sayfasını gösterir.

    ![Oturum açma sayfası.](media/app-configure-sign-in-page.png "Oturum açma sayfası")

## <a name="manually-configure-the-application"></a><a name="config-manually"></a>Uygulamayı el ile yapılandırma

Dosyanız veya QR kodunuz yoksa, Azure AD uygulaması aracılığıyla Supply Chain Management sunucusuna bağlanması için cihaz üzerindeki uygulamayı el ile yapılandırabilirsiniz.

1. Mobil cihazınızda Ambar Yönetimi mobil uygulamasını başlatın.
1. Uygulama **Tanıtım modunda** başlatılırsa **Bağlantı ayarları**'nı seçin. Uygulama başlatıldığında **Oturum aç** sayfası gösterilirse **Bağlantıyı değiştir**'i seçin.
1. **Bağlantıyı ayarla**'yı seçin.

    ![Bağlantı kurma.](media/app-configure-set-up-connection.png "Bağlantı kur")

1. **El ile giriş**'i seçin.

    ![Bağlantı kurulumu menüsü.](media/app-configure-connection-setup-flyout.png "Bağlantı kurulum menüsü")

    **Yeni Bağlantı** sayfası gösterilir ve bağlantı ayarlarını manuel olarak girmek için gerekli ayarlar görüntülenir.

    ![El ile bağlantı alanları.](media/app-configure-input-manually.png "El ile bağlantı alanları")

1. Aşağıdaki bilgileri girin:

    - **İstemci parolası kullanma**: Supply Chain Management ile kimlik doğrulaması yapmak üzere bir istemci parolası kullanmak için bu seçeneği _Evet_ olarak ayarlayın. Kimlik doğrulaması için sertifika kullanacaksanız _Hayır_ olarak ayarlayın. (Daha fazla bilgi için bu konunun önceki kısımlarında yer alan [Azure Active Directory'de web hizmeti uygulaması oluşturma](#create-service) bölümüne bakın.)
    - **Bağlantı adı**: Yeni bağlantı için bir ad girin. Bu ad, bağlantı ayarlarını bir sonraki açışınızda **Bağlantı seç** alanında görünür. Girdiğiniz ad benzersiz olmalıdır: (Başka bir deyişle, orada başka bir bağlantı adı depolanmışsa cihazınızda depolanan diğer tüm bağlantı adlarından farklı olmalıdır.)
    - **Active Directory istemci kimliği**: [Azure Active Directory uygulamasında bir web hizmeti uygulaması oluşturma](#create-service) bölümünde Azure AD uygulamasını ayarlarken not ettiğiniz istemci kimliğini girin.
    - **Active Directory istemci parolası**: Bu alan yalnızca **İstemci parolasını kullan** seçeneği _Evet_ olarak ayarlandığında kullanılabilir. [Azure Active Directory uygulamasında bir web hizmeti uygulaması oluşturma](#create-service) bölümünde Azure AD uygulamasını ayarlarken not ettiğiniz istemci parolasını girin.
    - **Active Directory sertifika parmak izi**: Bu alan yalnızca Windows cihazlarında ve yalnızca **Gizli anahtarı kullan** seçeneği _Hayır_ olarak ayarlandığında kullanılabilir. [Azure Active Directory uygulamasında bir web hizmeti uygulaması oluşturma](#create-service) bölümünde Azure AD uygulamasını ayarlarken not ettiğiniz sertifika parmak izini girin.
    - **Active Directory kaynağı**: Supply Chain Management uygulamasının kök URL'sini belirtin.

        > [!IMPORTANT]
        > Bu değeri eğik çizgi (/) ile bitirmeyin.
        > HTTPS (SSL) sertifikasının geçerli olduğundan emin olun.

    - **Active Directory kiracısı**: Supply Chain Management sunucusuyla kullandığınız Azure AD etki alanı adını girin. Bu değer `https://login.windows.net/<your-Azure-AD-domain-name>` formuna sahiptir. İşte bir örnek: `https://login.windows.net/contosooperations.onmicrosoft.com`. Azure AD etki alanı adınızı bulma hakkında daha fazla bilgi için bkz. [Kullanıcının önemli kimliklerini bulma](/partner-center/find-ids-and-domain-names).

        > [!IMPORTANT]
        > Bu değeri eğik çizgi (/) ile bitirmeyin.

    - **Şirket**: Uygulamanın bağlanmasını istediğiniz Supply Chain Management uygulamasına tüzel kişiliği (şirketi) girin.

1. Sayfanın sağ üst köşesindeki **Kaydet** düğmesini seçin.
1. Android cihazı kullanıyorsanız ve kimlik doğrulama için bir sertifika kullanıyorsanız cihaz sizden sertifikayı seçmenizi ister.
1. Uygulama, Supply Chain Management sunucunuza bağlanır ve oturum açma sayfasını gösterir.

## <a name="remove-access-for-a-device"></a>Cihazın erişimini kaldır

Cihazın kaybolması veya güvenliğinin aşılması durumunda, cihazın Supply Chain Management erişimini kaldırmanız gerekir. Aşağıdaki adımlar, erişimi kaldırmak için önerilen adımları açıklar.

1. **Sistem yönetimi \> Kurulum \> Azure Active Directory uygulamaları**'na gidin.
1. Erişimini kaldırmak istediğiniz cihaza karşılık gelen satırı silin. Cihaz için kullanılan istemci kimliğini not edin. Buna daha sonra ihtiyacınız olacaktır.

    Yalnızca bir istemci kimliği kaydettiyseniz ve birden fazla cihaz aynı müşteri kimliğini kullanıyorsa bu cihazlara yeni bağlantı ayarları göndermeniz gerekir. Aksi takdirde erişimlerini kaybederler.

1. Azure portalında [https://portal.azure.com](https://portal.azure.com/) adresinden oturum açın.
1. Sol gezinme bölmesinde **Active Directory**'yi seçin ve doğru dizinde olduğunuzdan emin olun.
1. **Yönet** listesinde, **Uygulama kayıtları**'nı ve ardından yapılandırılacak uygulamayı seçin. **Ayarlar** sayfası görüntülenir ve yapılandırma bilgilerini gösterir.
1. Uygulamanın istemci kimliğinin 2. adımda not ettiğiniz istemci kimliğiyle eşleştiğinden emin olun.
1. Araç çubuğunda **Sil**'i seçin.
1. Görüntülenen onay iletisinde **Evet**'i seçin.

## <a name="additional-resources"></a>Ek kaynaklar

- [Mobil cihaz kullanıcı ayarları](mobile-device-user-settings.md)
- [Warehouse Management mobil uygulaması için adım simgeleri ve başlıklar atama](step-icons-titles.md)
- [Bulut ve uç ölçek birimleri için Warehouse Management mobil uygulamasını yapılandırma](../cloud-edge/cloud-edge-workload-setup-warehouse-app.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
