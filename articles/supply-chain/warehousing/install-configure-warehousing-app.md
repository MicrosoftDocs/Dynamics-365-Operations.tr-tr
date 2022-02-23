---
title: Ambar uygulamasını yükleme ve bağlama
description: Bu konuda, ambar uygulamasının mobil cihazlarınızın her birine nasıl yükleneceği ve Microsoft Dynamics 365 Supply Chain Management ortamınıza bağlanacak şekilde nasıl yapılandırılacağı açıklanmaktadır. Her cihazı el ile yapılandırabilir veya bir dosya ya da bir QR kodunu tarayarak bağlantı ayarlarını içe aktarabilirsiniz.
author: MarkusFogelberg
manager: tfehr
ms.date: 05/25/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysAADClientTable, WHSMobileAppField, WHSMobileAppFieldPriority, WHSRFMenu, WHSRFMenuItem, WHSWorker
audience: Application User, IT Pro
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 267694
ms.assetid: d95d43b2-13ff-4189-a71a-3a1fb57d55ed
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: mafoge
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 88bce09a6d3bf154592955a6fb2dada6247f1993
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "4439514"
---
# <a name="install-and-connect-the-warehouse-app"></a>Ambar uygulamasını yükleme ve bağlama

[!include [banner](../includes/banner.md)]

> [!NOTE]
> Bu konu bulut dağıtımları için ambarlamanın nasıl yapılandırılacağını açıklar. Ambarlamanın şirket içi dağıtımlar için nasıl yapılandırılacağı hakkında bilgi arıyorsanız bkz. [Şirket için dağıtımlar için ambarlama](../../dev-itpro/deployment/warehousing-for-on-premise-deployments.md).

Ambar uygulaması Google Play Store ve Microsoft Store'dan edinilebilir. Bağımsız bir bileşen olarak sağlanır. Bu nedenle, her cihaza indirmeli ve sonra Microsoft Dynamics 365 Supply Chain Management ortamınıza bağlanacak şekilde yapılandırmalısınız.

Bu konuda, ambar uygulamasının mobil cihazlarınızın her birine nasıl yükleneceği ve Supply Chain Management ortamınıza bağlanacak şekilde nasıl yapılandırılacağı açıklanmaktadır. Her cihazı el ile yapılandırabilir veya bir dosya ya da bir QR kodunu tarayarak bağlantı ayarlarını içe aktarabilirsiniz.

## <a name="system-requirements"></a>Sistem gereksinimleri

Ambar uygulaması hem Windows hem de Android işletim sistemleri için kullanılabilir. Uygulamanın en son sürümünü kullanmak için mobil cihazlarınızda aşağıdaki işletim sistemlerinden birine sahip olmanız gerekir:

- Windows 10 (Evrensel Windows Platformu \[UWP \]) Fall Creators Update 1709 (derleme 10.0.16299) veya üstü
- Android 4.4 veya üstü

> [!NOTE]
> Windows'un en son sürümünü çalıştıramayan eski Windows aygıtlarını desteklemeniz gerekiyorsa yine de ambar uygulamasının 1.6.3.0 sürümünü Microsoft Store'dan indirebilirsiniz. Bu sürüm, Windows 10 (UWP) Kasım Güncelleştirmesi 1511 (derleme 10.0.10586) veya üstünde kullanılabilir. Ancak; ambar uygulamasının bu sürümünün, bağlantı ayarlarının toplu dağıtımını desteklemediğini unutmayın. Bu nedenle, uygulamanın bu sürümünü çalıştıran her cihazda [bağlantıyı el ile yapılandırmanız](#config-manually) gerekir.

## <a name="get-the-warehouse-app"></a>Ambar uygulamasını edinme

Uygulamayı indirmek için aşağıdaki bağlantılardan birini kullanın:

- **Windows (UWP):** [Microsoft Store'da Dynamics 365 for Finance and Operations - Warehousing](https://www.microsoft.com/store/apps/9p1bffd5tstm)
- **Android:** [Google Play Store'da Warehousing - Dynamics 365](https://play.google.com/store/apps/details?id=com.Microsoft.Dynamics365forOperationsWarehousing)

Daha küçük dağıtımlar için, uygulamayı her bir cihazdaki ilgili mağazadan yüklemek ve ardından kullandığınız ortamlara olan bağlantıyı el ile yapılandırmak isteyebilirsiniz. Ancak, ambar uygulamasının 1.7.0.0 ve üstü sürümlerinde uygulama dağıtımını ve/veya yapılandırmasını da otomatikleştirebilirsiniz. Birçok cihazı yönetiyorsanız ve [Microsoft Intune](https://docs.microsoft.com/mem/intune/fundamentals/what-is-intune) gibi bir mobil cihaz yönetimi ve mobil uygulama yönetimi çözümü kullanıyorsanız bu yaklaşımı uygun bulabilirsiniz. Uygulama eklemek için Intune'u kullanma hakkında bilgi için bkz. [Microsoft Intune'a uygulama ekleme](https://docs.microsoft.com/mem/intune/apps/apps-add).

## <a name="create-a-web-service-application-in-azure-active-directory"></a><a name="create-service"></a>Azure Active Directory içinde bir web hizmeti uygulaması oluşturma

Ambar uygulamasının belirli bir Supply Chain Management sunucusuyla etkileşime girmesini sağlamak için Azure Active Directory (Azure AD) uygulamasında Supply Chain Management kiracısı için bir web hizmeti uygulaması kaydetmeniz gerekir. Aşağıdaki yordamda, bu görevi tamamlamanın bir yolu gösterilmektedir. Ayrıntılı bilgi ve alternatifler için yordamdan sonraki bağlantılara bakın.

1. Web tarayıcısında [https://portal.azure.com](https://portal.azure.com/) adresine gidin.
1. Azure aboneliğine erişimi olan kullanıcının adını ve parolasını girin.
1. Azure portalında, sol gezinti bölmesinde, **Azure Active Directory** uygulamasını seçin.

    ![Azure Active Directory](media/app-connect-azure-aad.png "Azure Active Directory")

1. Supply Chain Management tarafından kullanılan Azure AD örneğiyle çalıştığınızdan emin olun.
1. **Yönet** listesinde **Uygulama kayıtları**'nı seçin.

    ![Uygulama kayıtları](media/app-connect-azure-register.png "Uygulama kayıtları")

1. **Uygulamayı kaydet** sihirbazını açmak için araç çubuğunda **Yeni kayıt**'ı seçin.
1. Uygulama için bir ad girin, **Yalnızca bu kuruluş dizinindeki hesaplar** seçeneğini belirleyin ve ardından **Kayıt**'ı seçin.

    ![Uygulama kaydetme sihirbazı](media/app-connect-azure-register-wizard.png "Uygulama kaydetme sihirbazı")

1. Yeni uygulama kaydınız açıldı. Daha sonra gereksinim duyacağınız **Uygulama (istemci) Kodu** değerini not edin. Bu kod, bu konuda daha sonra *istemci kimliği* olarak ifade edilecektir.

    ![Uygulama (istemci) kodu](media/app-connect-azure-app-id.png "Uygulama (istemci) kodu")

1. **Yönet** listesinde **Sertifika ve parolalar**'ı seçin. Ardından, uygulamayı kimlik doğrulama için nasıl yapılandırmak istediğinize bağlı olarak aşağıdaki düğmelerden birini seçin. (Daha fazla bilgi için bu konunun ilerisindeki [Sertifika veya istemci parolası kullanarak kimlik doğrulaması](#authenticate) bölümüne bakın.)

    - **Karşıya yükleme sertifikası**: Bir sertifikayı parola olarak kullanmak için karşıya yükleyin. Daha güvenli ve tamamen otomatikleştirilebilir olduğu için bu yaklaşımı öneriyoruz. Ambar uygulamasını Windows cihazlarında çalıştırıyorsanız sertifikayı yükledikten sonra gösterilen **Parmak İzi** değerini not edin. Sertifikayı Windows cihazlarında yapılandırırken bu değere ihtiyacınız olacaktır.
    - **Yeni istemci parolası**: **Parolalar** bölümüne bir anahtar açıklama ve süre girerek bir anahtar oluşturun ve **Ekle**'yi seçin. Anahtarın bir kopyasını oluşturun ve güvenli bir şekilde saklayın.

    ![Sertifika ve parolalar](media/app-connect-azure-authentication.png "Sertifika ve parolalar")

Azure AD uygulamasında web hizmeti uygulamalarını ayarlama hakkında daha fazla bilgi için aşağıdaki kaynaklara bakın:

- Azure AD uygulamasında web hizmeti uygulamalarını ayarlamak için Windows PowerShell'in nasıl kullanılacağını gösteren yönergeler için bkz. [Nasıl yapılır: Sertifikalı bir hizmet sorumlusu oluşturmak için Azure PowerShell'i kullanma](https://docs.microsoft.com/azure/active-directory/develop/howto-authenticate-service-principal-powershell).
- Azure AD uygulamasında el ile bir web hizmeti uygulaması oluşturma hakkında ayrıntılı bilgi için aşağıdaki konulara bakın:

    - [Hızlı Başlangıç: Microsoft kimlik platformu ile bir uygulamayı kaydetme](https://docs.microsoft.com/azure/active-directory/develop/quickstart-register-app)
    - [Nasıl yapılır: Kaynaklara erişebilen bir Azure AD uygulaması ve hizmet sorumlusu oluşturmak için portalı kullanma](https://docs.microsoft.com/azure/active-directory/develop/howto-create-service-principal-portal)

## <a name="create-and-configure-a-user-account-in-supply-chain-management"></a>Supply Chain Management içinde bir kullanıcı hesabı oluşturma ve yapılandırma

Supply Chain Management'ın Azure AD uygulamanızı kullanmasını sağlamak için aşağıdaki adımları izleyin.

1. Ambar uygulaması için kullanıcı kimlik bilgilerine karşılık gelen bir kullanıcı oluşturun:

    1. Supply Chain Management uygulamasında **Sistem yönetimi \> Kullanıcıları \> Kullanıcıları**'na gidin.
    1. Kullanıcı oluşturun.
    1. Ambarlama mobil cihaz kullanıcısını atayın.

    ![Ambarlama mobil cihaz kullanıcısını atama](media/app-connect-app-users.png "Ambarlama mobil cihaz kullanıcısını atama")

1. Azure AD uygulamanızı, ambar uygulaması kullanıcısı ile ilişkilendirin:

    1. **Sistem yönetimi \> Kurulum \> Azure Active Directory uygulamaları**'na gidin.
    1. Satır oluşturun.
    1. Önceki bölümde not ettiğiniz istemci kimliğini girin, kimliğe bir ad verin ve az önce oluşturduğunuz kullanıcıyı seçin. Tüm cihazlarınızı etiketlemenizi öneririz. Sonrasında, cihazınız kaybolursa Supply Chain Management erişimini bu sayfadan kolayca kaldırabilirsiniz.

    ![Azure Active Directory uygulamaları](media/app-connect-aad-apps.png "Azure Active Directory uygulamaları")

## <a name="authenticate-by-using-a-certificate-or-client-secret"></a><a name="authenticate"></a>Sertifika veya istemci parolası kullanarak kimlik doğrulama

Azure AD ile kimlik doğrulaması, bir mobil cihazı Supply Chain Management uygulamasında bağlamak için güvenli bir yol sağlar. İstemci parolası veya sertifika kullanarak kimlik doğrulaması yapabilirsiniz. Bağlantı ayarlarını içe aktaracaksanız istemci parolası yerine bir sertifika kullanmanızı öneririz. İstemci parolasının her zaman güvenli bir şekilde saklanması gerektiğinden, bu konuda daha sonra açıklandığı gibi istemci parolasını bir bağlantı ayarları dosyasından veya bir QR kodundan içe aktaramazsınız.

Sertifikalar, bir belirteç istendiğinde uygulamanın kimliğini kanıtlamak için parola olarak kullanılabilir. Sertifikanın genel kısmı Azure portalındaki uygulama kaydına yüklenirken tam sertifikanın ambar uygulamasının yüklü olduğu her cihaza dağıtılması gerekir. Kuruluşunuz sertifikayı, rotasyonu vb. konularda yönetmekle sorumludur. Kendinden imzalı sertifikalar kullanabilirsiniz ancak her zaman dışa aktarılamayan sertifikalar kullanmalısınız.

Sertifikayı, ambar uygulamasını çalıştırdığınız her cihazda yerel olarak kullanılabilir hale getirmelisiniz. Intune kullanıyorsanız, Intune denetimli cihazlara yönelik sertifikaları yönetme hakkında bilgi için bkz. [Microsoft Intune'da kimlik doğrulama için sertifika kullanma](https://docs.microsoft.com/mem/intune/protect/certificates-configure).

## <a name="configure-the-application-by-importing-connection-settings"></a>Bağlantı ayarlarını içe aktararak uygulamayı yapılandırma

Uygulamanın birçok mobil cihazda bakımını ve dağıtımını kolaylaştırmak için bağlantı ayarlarını her bir cihaza el ile girmek yerine içe aktarabilirsiniz. Bu bölümde, ayarların nasıl oluşturulacağı ve içe aktarılacağı açıklanmaktadır.

### <a name="create-a-connection-settings-file-or-qr-code"></a>Bağlantı ayarları dosyası veya QR kodu oluşturma

Bağlantı ayarlarını bir dosyadan veya bir QR kodundan alabilirsiniz. Her iki yaklaşım için de önce JavaScript Nesne Gösterimi (JSON) biçimini ve söz dizimini kullanan bir ayar dosyası oluşturmanız gerekir. Dosya, eklenmesi gereken her bir bağlantıyı içeren bir bağlantı listesi içermelidir. Aşağıdaki tabloda bağlantı ayarları dosyasında belirtmeniz gereken parametreler özetlenmektedir.

| Parametre | Tanım |
| --- | --- |
| ConnectionName | Bağlantı ayarlarının adını belirtin. En fazla 20 karakter kullanılabilir. Bu değer, bir bağlantı ayarının benzersiz tanımlayıcısı olduğu için listede benzersiz olduğundan emin olun. Cihazda aynı ada sahip bir bağlantı zaten varsa içe aktarılan dosyadaki ayarlar tarafından geçersiz kılınır. |
| ActiveDirectoryClientAppId | [Azure Active Directory uygulamasında bir web hizmeti uygulaması oluşturma](#create-service) bölümünde Azure AD uygulamasını ayarlarken not ettiğiniz istemci kimliğini belirtin. |
| ActiveDirectoryResource | Supply Chain Management uygulamasının kök URL'sini belirtin. |
| ActiveDirectoryTenant | Supply Chain Management sunucusuyla kullandığınız Azure AD kiracısını belirtin. Bu değer `https://login.windows.net/<your-Azure-AD-tenant-ID>` formuna sahiptir. İşte bir örnek: `https://login.windows.net/contosooperations.onmicrosoft.com`. |
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

Genellikle, bağlantı ayarları dosyalarını yönettiğiniz her cihazda dağıtmak için bir cihaz yönetim aracı veya komut dosyası kullanırsınız. Bağlantı ayarları dosyasını her bir cihaza kaydettiğinizde varsayılan adı ve konumu kullanırsanız ambar uygulaması, uygulama yüklendikten sonraki ilk çalıştırmada bile dosyayı otomatik olarak içe aktarır. Dosya için özel bir ad veya konum kullanırsanız uygulama kullanıcısının değerleri, ilk çalıştırma sırasında belirtmesi gerekir. Ancak, uygulama daha sonra belirtilen adı ve konumu kullanmaya devam eder.

Uygulama her başlatıldığında, herhangi bir değişiklik olup olmadığını belirlemek için bağlantı ayarlarını önceki konumlarından yeniden içe aktarır. Uygulama yalnızca bağlantı ayarları dosyasındaki bağlantılarla aynı ada sahip bağlantıları güncelleştirecektir. Diğer adları kullanan, kullanıcı tarafından oluşturulan bağlantılar güncellenmez.

Bağlantı ayarları dosyasını kullanarak bir bağlantıyı kaldıramazsınız.

Daha önce de belirtildiği gibi varsayılan dosya adı *connections.json* şeklindedir. Varsayılan dosya konumu, bir Windows cihazı mı yoksa Android cihazı mı kullandığınıza bağlıdır:

- **Windows:** `C:\Users\<User>\AppData\Local\Packages\Microsoft.Dynamics365forOperations-Warehousing_8wekyb3d8bbwe\LocalState`
- **Android:** `Android\data\com.Microsoft.Dynamics365forOperationsWarehousing\files`

Genellikle yollar, uygulamanın ilk çalıştırılmasından sonra otomatik olarak oluşturulur. Ancak, kurulumdan önce bağlantı ayarları dosyasını cihaza aktarmanız gerekiyorsa bunları el ile olarak oluşturabilirsiniz.

> [!NOTE]
> Uygulama kaldırılırsa varsayılan yol ve içeriği kaldırılır.

### <a name="import-the-connection-settings"></a>Bağlantı ayarlarını içe aktarma

Bağlantı ayarlarını bir dosyadan veya bir QR kodundan içe aktarmak için aşağıdaki adımları izleyin.

1. Mobil cihazınızda ambar uygulamasını açın.
1. **Bağlantı ayarları**'na gidin.
1. **Tanıtım modunda kullan** seçeneğinde _Hayır_'ı işaretleyin.

    ![Tanıtım modunda kullan seçeneği](media/app-connect-app-demo-mode.png "Tanıtım modunda kullan seçeneği")

1. Ayarları nasıl içe aktarmak istediğinize bağlı olarak **Dosya seç** veya **QR kodunu tara**'yı seçin:

    - Bağlantı ayarlarını bir dosyadan içe aktarıyorsanız ve varsayılan ad ve varsayılan konum kaydedilirken kullanılmışsa uygulama, dosyayı zaten bulmuş olabilir. Aksi durumda **Dosya seç**'i seçin, yerel cihazınızdaki dosyaya göz atın ve dosyayı seçin. Özel bir konum seçerseniz uygulama konumu kaydeder ve bir sonraki sefer otomatik olarak kullanır.
    - QR kodunu tarayarak bağlantı ayarlarını içe aktarıyorsanız **QR kodunu tara**'yı seçin. Uygulama, cihazın kamerasını kullanmak için sizden izin ister. İzin verdikten sonra kamera başlatılır, böylece tarama için kullanılabilir. Cihazın kamerasının kalitesine ve QR kodunun karmaşıklığına bağlı olarak doğru bir tarama elde etmekte zorlanabilirsiniz. Bu durumda, her QR kodu için yalnızca bir bağlantı oluşturarak QR kodunun karmaşıklığını azaltmaya çalışın. (Şu anda, QR kodunu taramak için yalnızca cihazın kamerasını kullanabilirsiniz.)

    ![Bağlantı ayarlarını içe aktarma](media/app-connect-app-select-file.png "Bağlantı ayarlarını içe aktarma")

1. Bağlantı ayarları başarıyla yüklendiğinde sayfanın sol üst köşesindeki **Geri** (sol ok) düğmesini seçin.

    ![Bağlantı ayarları yüklendi](media/app-connect-app-settings-loaded.png "Bağlantı ayarları yüklendi")

1. Android cihazı kullanıyorsanız ve kimlik doğrulama için bir sertifika kullanıyorsanız cihaz sizden sertifikayı seçmenizi ister.

    ![Android cihazında sertifika komutu seçme](media/app-connect-app-choose-cert.png "Android cihazında sertifika komutu seçme")

1. Uygulama, Supply Chain Management sunucunuza bağlanır ve oturum açma sayfasını gösterir.

    ![Oturum açma sayfası](media/app-connect-sign-in.png "Oturum açma sayfası")

## <a name="manually-configure-the-application"></a><a name="config-manually"></a>Uygulamayı el ile yapılandırma

Azure AD uygulaması aracılığıyla Supply Chain Management sunucusuna erişebilmek için cihaz üzerindeki uygulamayı el ile yapılandırabilirsiniz.

1. Mobil cihazınızda ambar uygulamasını açın.
1. **Bağlantı ayarları**'na gidin.
1. **Tanıtım modunda kullan** seçeneğinde _Hayır_'ı işaretleyin.

    ![Tanıtım modu kapalı](media/app-connect-app-select-file.png "Tanıtım modu kapalı")

1. Bağlantı ayrıntılarını el ile girmek üzere gereken ayarları genişletmek için **Bağlantı seç** alanına dokunun.

    ![El ile bağlantı alanları](media/app-connect-manual-connect.png "El ile bağlantı alanları")

1. Aşağıdaki bilgileri girin:

    - **İstemci parolası kullanma**: Supply Chain Management ile kimlik doğrulaması yapmak üzere bir istemci parolası kullanmak için bu seçeneği _Evet_ olarak ayarlayın. Kimlik doğrulaması için sertifika kullanacaksanız _Hayır_ olarak ayarlayın. (Daha fazla bilgi için bkz [Azure Active Directory içinde bir web hizmeti uygulaması oluşturma](#create-service).)
    - **Bağlantı adı**: Yeni bağlantı için bir ad girin. Bu ad, bağlantı ayarlarını bir sonraki açışınızda **Bağlantı seç** alanında görünür. Girdiğiniz ad benzersiz olmalıdır: (Başka bir deyişle, orada başka bir bağlantı adı depolanmışsa cihazınızda depolanan diğer tüm bağlantı adlarından farklı olmalıdır.).
    - **Active Directory istemci kimliği**: [Azure Active Directory uygulamasında bir web hizmeti uygulaması oluşturma](#create-service) bölümünde Azure AD uygulamasını ayarlarken not ettiğiniz istemci kimliğini girin.
    - **Active Directory istemci parolası**: Bu alan yalnızca **İstemci parolasını kullan** seçeneği _Evet_ olarak ayarlandığında kullanılabilir. [Azure Active Directory uygulamasında bir web hizmeti uygulaması oluşturma](#create-service) bölümünde Azure AD uygulamasını ayarlarken not ettiğiniz istemci parolasını girin.
    - **Active Directory sertifika parmak izi**: Bu alan Windows cihazları için yalnızca **İstemci parolasını kullan** seçeneği _Hayır_ olarak ayarlandığında kullanılabilir. [Azure Active Directory uygulamasında bir web hizmeti uygulaması oluşturma](#create-service) bölümünde Azure AD uygulamasını ayarlarken not ettiğiniz sertifika parmak izini girin.
    - **Active Directory kaynağı**: Supply Chain Management uygulamasının kök URL'sini belirtin.

        > [!NOTE]
        > Bu değeri eğik çizgi (/) ile bitirmeyin.

    - **Active Directory kiracısı**: Supply Chain Management sunucusuyla kullandığınız Azure AD kiracısını girin. Bu değer `https://login.windows.net/<your-Azure-AD-tenant-ID>` formuna sahiptir. İşte bir örnek: `https://login.windows.net/contosooperations.onmicrosoft.com`.

        > [!NOTE]
        > Bu değeri eğik çizgi (/) ile bitirmeyin.

    - **Şirket**: Uygulamanın bağlanmasını istediğiniz Supply Chain Management uygulamasına tüzel varlığı girin.

1. Sayfanın sağ üst köşesindeki **Kaydet** düğmesini seçin.
1. Android cihazı kullanıyorsanız ve kimlik doğrulama için bir sertifika kullanıyorsanız cihaz sizden sertifikayı seçmenizi ister.
1. Uygulama, Supply Chain Management sunucunuza bağlanır ve oturum açma sayfasını gösterir.

## <a name="remove-access-for-a-device"></a>Cihazın erişimini kaldır

Kayıp veya güvenliği aşılmış bir cihaz durumunda bu cihaz için Supply Chain Management erişimini kaldırmanız gerekir. Aşağıdaki adımlar, erişimi kaldırmak için önerilen adımları açıklar.

1. **Sistem yönetimi \> Kurulum \> Azure Active Directory uygulamaları**'na gidin.
1. Erişimini kaldırmak istediğiniz cihaza karşılık gelen satırı silin. Kaldırılan cihaz için kullanılan istemci kimliğini not edin, çünkü daha sonra ihtiyacınız olacaktır.

    Yalnızca bir istemci kimliği kaydettiyseniz ve birden fazla cihaz aynı müşteri kimliğini kullanıyorsa bu cihazlara yeni bağlantı ayarları göndermeniz gerekir. Aksi takdirde erişimlerini kaybederler.

1. Azure portalında [https://portal.azure.com](https://portal.azure.com/) adresinden oturum açın.
1. Sol gezinme bölmesinde **Active Directory**'yi seçin ve doğru dizinde olduğunuzdan emin olun.
1. **Yönet** listesinde, **Uygulama kayıtları**'nı ve ardından yapılandırılacak uygulamayı seçin. **Ayarlar** sayfası görüntülenir ve yapılandırma bilgilerini gösterir.
1. Uygulamanın istemci kimliğinin 2. adımda not ettiğiniz istemci kimliğiyle eşleştiğinden emin olun.
1. Araç çubuğunda **Sil**'i seçin.
1. Görüntülenen onay iletisinde **Evet**'i seçin.
