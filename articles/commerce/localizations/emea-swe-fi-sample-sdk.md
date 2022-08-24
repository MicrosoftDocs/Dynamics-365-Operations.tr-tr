---
ms.openlocfilehash: a20971ac9a44c409363bbce6cd8b8343f16d800f
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/12/2022
ms.locfileid: "9274218"
---
# <a name="deployment-guidelines-for-the-control-unit-integration-sample-for-sweden-legacy"></a>İsveç için kontrol birimi tümleştirme örneğine ilişkin dağıtım kılavuzları (eski)
---

title: İsveç için kontrol birimi tümleştirme örneğine ilişkin dağıtım kılavuzları (eski) [!include [banner](../includes/banner.md)]
description: Bu makale, Retail SDK'den İsveç için kontrol birimi tümleştirme örneğinin dağıtılmasına ilişkin yönergeler sağlar

author: EvgenyPopovMBS Bu makale, Microsoft Dynamics Lifecycle Services'taki (LCS) bir geliştirici sanal makinesinde (VM) Retail yazılım geliştirme setinden (SDK) İsveç için kontrol birimi tümleştirme örneğinin dağıtılmasına ilişkin yönergeler sağlar. Bu mali tümleştirme örneği hakkında daha fazla bilgi için bkz. [İsveç için kontrol birimi tümleştirme örneği](emea-swe-fi-sample.md). ms.date: 20.12.2021

ms.topic: article İsveç için mali tümleştirme örneği, Retail SDK'nin bir parçasıdır. SDK'yi yükleme ve kullanma hakkında daha fazla bilgi için bkz. [Retail yazılım geliştirme seti (SDK) mimarisi](../dev-itpro/retail-sdk/retail-sdk-overview.md). Bu örnek, Commerce Runtime ( CRT) ve satış noktasına (POS) yönelik uzantılardan oluşur. Bu örneği çalıştırmak için CRT, Hardware station ve POS projelerini değiştirip derlemeniz gerekir. Bu makalede açıklanan değişiklikleri yapmak için değiştirilmemiş bir Retail SDK kullanmanızı öneririz. Henüz değiştirilmiş bir dosya olmadığı durumlarda, Azure DevOps gibi bir kaynak denetimi sistemi kullanmanızı öneririz.
hedef kitle: Uygulama Kullanıcısı, Geliştirici, BT Uzmanı

ms.reviewer: v-chgriffin
## <a name="development-environment"></a>Geliştirme ortamı
ms.search.region: Global

ms.author: josaw Örneği sınayabilmeniz ve genişletebilmeniz için bir geliştirme ortamı ayarlamak amacıyla bu adımları izleyin.
ms.search.validFrom: 2019-03-01

### <a name="enable-crt-extensions"></a>CRT uzantılarını etkinleştirme
---


CRT uzantısı bileşenleri, CRT örneklerine dahil edilmiştir. Aşağıdaki yordamları tamamlamak için **RetailSdk\\SampleExtensions\\CommerceRuntime** bölümündeki **CommerceRuntimeSamples.sln** çözümünü açın.
2. **HardwareStation.Extension.config** yapılandırma dosyasındaki **composition** bölümüne aşağıdaki satırı ekleyerek güncel örnek Hardware station uzantısını etkinleştirin.


#### <a name="documentprovidercleancashsample-component"></a>DocumentProvider.CleanCashSample bileşeni
    ``` xml

    <add source="assembly" value="Contoso.Commerce.HardwareStation.CleanCashSample" />
1. **Runtime.Extensions.DocumentProvider.CleanCashSample** projesini bulun ve derleyin.
    ```
2. In the **Runtime.Extensions.DocumentProvider.CleanCashSample\\bin\\Debug** folder, find the **Contoso.Commerce.Runtime.DocumentProvider.CleanCashSample.dll** assembly file.

3. Copy the assembly file to the CRT extensions folder:
3. Make the following changes in the **Customization.settings** package customization configuration file under the **BuildTools** folder:


    - **Commerce Scale Unit:** Copy the file to the **\\bin\\ext** folder under the Internet Information Services (IIS) Commerce Scale Unit site location.
    - Remove the following line to exclude the earlier Hardware station extension from deployable packages.
    - **Local CRT on Modern POS:** Copy the file to the **\\ext** folder under the local CRT client broker location.


        ``` xml
4. Find the extension configuration file for CRT:
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.HardwareStation.Extension.FiscalRegisterSample.dll" />

        ```
    - **Commerce Scale Unit:** The file is named **commerceruntime.ext.config**, and it's in the **bin\\ext** folder under the IIS Commerce Scale Unit site location.

    - **Local CRT on Modern POS:** The file is named **CommerceRuntime.MPOSOffline.Ext.config**, and it's under the local CRT client broker location.
    - Add the following lines to include the current sample Hardware station extension in deployable packages.


5. Register the CRT change in the extension configuration file.
        ``` xml

        <ISV_HardwareStation_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.HardwareStation.CleanCashSample.dll" />
    ``` xml
        <ISV_HardwareStation_CustomizableFile Include="$(SdkReferencesPath)\Interop.CleanCash_1_1.dll" />
    <add source="assembly" value="Contoso.Commerce.Runtime.DocumentProvider.CleanCashSample" />
        ```
    ```


#### <a name="update-modern-pos"></a>Modern POS'u güncelleştirme
#### <a name="extension-configuration-file"></a>Uzantı yapılandırma dosyası


1. **RetailSdk\\POS** bölümündeki **CloudPOS.sln** çözümünü açın.
1. CRT için uzantı yapılandırma dosyasını bulun:
2. Önceki POS uzantısını devre dışı bırakın:


    - **Commerce Scale Unit:** Dosya, **commerceruntime.ext.config** olarak adlandırılmıştır ve IIS Commerce Scale Unit site konumundaki **bin\\ext** klasöründe yer alır.
    - **tsconfig.json** dosyasında, **FiscalRegisterSample** klasörünü hariç tutma listesine ekleyin.
    - **Modern POS'taki yerel CRT:** Dosya, **CommerceRuntime.MPOSOffline.Ext.config** olarak adlandırılmıştır ve yerel CRT istemci aracısı konumunda yer alır.
    - **RetailSDK\\POS\\Extensions** klasöründeki **extensions.json** dosyasından aşağıdaki satırları kaldırın.


2. CRT değişikliğini uzantı yapılandırma dosyasına kaydedin.
        ``` json

        {
    ``` xml
            "baseUrl": "FiscalRegisterSample"
    <add source="assembly" value="Microsoft.Dynamics.Commerce.Runtime.ReceiptsSweden" />
        }
    ```
        ```


### <a name="enable-hardware-station-extensions"></a>Hardware Station uzantılarını etkinleştirme
3. **RetailSDK\\POS\\Extensions** klasöründeki **extensions.json** dosyasına aşağıdaki satırları ekleyerek güncel örnek POS uzantısını etkinleştirin.


Hardware station uzantı bileşenleri, Hardware station örneklerine dahil edilmiştir. Aşağıdaki yordamları tamamlamak için **RetailSdk\\SampleExtensions\\HardwareStation** bölümündeki **HardwareStationSamples.sln** çözümünü açın.
    ``` json

    {
#### <a name="cleancash-component"></a>CleanCash bileşeni
        "extensionPackages": [

            {
1. **HardwareStation.Extension.CleanCashSample** projesini bulun ve derleyin.
                "baseUrl": "Microsoft/AuditEvent.SE"
2. **Extension.CleanCashSample\\bin\\Debug** klasöründe **Contoso.Commerce.HardwareStation.CleanCashSample.dll** ve **Interop.CleanCash\_1\_1.dll** derleme dosyalarını bulun.
            }
3. Derleme dosyalarını Hardware station uzantılar klasörüne kopyalayın:      ]

    }
    - **Paylaşılan hardware station:** Dosyaları IIS Hardware station site konumundaki **bin** klasörüne kopyalayın.
    ```
    - **Dedicated hardware station on Modern POS:** Copy the files to the Modern POS client broker location.


#### Update Cloud POS
4. Find the extension configuration file for the Hardware station's extensions. The file is named **HardwareStation.Extension.config**.


1. Open the **ModernPOS.sln** solution under **RetailSdk\\POS**.
    - **Shared hardware station:** The file is under the IIS Hardware station site location.
2. Disable the earlier POS extension:
    - **Dedicated hardware station on Modern POS:** The file is under the Modern POS client broker location.


    - In the **tsconfig.json** file, add the **FiscalRegisterSample** folder to the exclude list.
5. Add the following line to the **composition** section of the configuration file.
    - Remove the following lines from the **extensions.json** file under the **RetailSDK\\POS\\Extensions** folder.


    ``` xml
        ``` json
    <add source="assembly" value="Contoso.Commerce.HardwareStation.CleanCashSample" />
        {
    ```
            "baseUrl": "FiscalRegisterSample"

        }
### <a name="enable-modern-pos-extension-components"></a>Modern POS uzantı bileşenlerini etkinleştirme
        ```


1. **RetailSdk\\POS** kısmından **ModernPOS.sln** çözümünü açın ve çözümün hatasız şekilde derlenebildiğinden emin olun. Ayrıca, **Çalıştır** komutunu kullanarak Visual Studio'dan Modern POS'u çalıştırabildiğinizden emin olun.
3. **RetailSDK\\POS\\Extensions** klasöründeki **extensions.json** dosyasına aşağıdaki satırları ekleyerek güncel örnek POS uzantısını etkinleştirin.


    > [!NOTE]
    ``` json
    > Modern POS must not be customized. You must enable User Account Control (UAC), and you must uninstall previously installed instances of Modern POS as required.
    {

        "extensionPackages": [
2. Enable the extensions that must be loaded by adding the following lines in the **extensions.json** file.
            {

                "baseUrl": "Microsoft/AuditEvent.SE"
    ``` json
            }
    {
        ]
        "extensionPackages": [
    }
            {
    ```
                "baseUrl": "Microsoft/AuditEvent.SE"

            }
#### <a name="create-deployable-packages"></a>Dağıtılabilir paketler oluşturma
        ]

    }
Dağıtılabilir paketler oluşturmak üzere tüm Retail SDK için **msbuild**'i çalıştırın. Paketleri LCS aracılığıyla veya el ile uygulayın. Daha fazla bilgi için bkz. [Retail SDK paketlemesi](../dev-itpro/retail-sdk/retail-sdk-packaging.md).
    ```

    > [!NOTE]
    > For more information, and for samples that show how to include source code folders and enable extensions to be loaded, see the instructions in the readme.md file in the **Pos.Extensions** project.

3. Çözümü yeniden oluşturun.
4. Hata ayıklayıcıda Modern POS'u çalıştırın ve işlevi sınayın.

### <a name="enable-cloud-pos-extension-components"></a>Bulut POS uzantı bileşenlerini etkinleştirme

1. **RetailSdk\\POS** kısmından **CloudPOS.sln** çözümünü açın ve çözümün hatasız şekilde derlenebildiğinden emin olun.
2. Yüklenmesi gereken uzantıları etkinleştirmek için **extensions.json** dosyasına aşağıdaki satırları ekleyin.

    ``` json
    {
        "extensionPackages": [
            {
                "baseUrl": "Microsoft/AuditEvent.SE"
            }
        ]
    }
    ```

    > [!NOTE]
    > Kaynak kodu klasörlerinin nasıl dahil edileceğini ve yüklenecek uzantıların nasıl etkinleştirileceğini gösteren örneklerle birlikte daha fazla bilgi için **Pos.Extensions** projesindeki readme.md dosyasındaki talimatlara bakın.

3. Çözümü yeniden oluşturun.
4. **Çalıştır** komutunu kullanarak ve Retail SDK el kitabındaki adımları izleyerek çözümü çalıştırın.

## <a name="production-environment"></a>Üretim ortamı

Önceki yordam, kontrol birimi tümleştirme örneğinin bileşenleri olan uzantıları etkinleştirir. Buna ek olarak, Commerce bileşenleri içeren dağıtılabilir paketler oluşturmak ve bu paketleri üretim ortamında uygulamak için aşağıdaki adımları izlemeniz gerekir.

1. **RetailSdk\\Assets** klasöründeki paket yapılandırma dosyalarında aşağıdaki değişiklikleri yapın:

    - **commerceruntime.ext.config** ve **CommerceRuntime.MPOSOffline.Ext.config** yapılandırma dosyalarında, **composition** bölümüne aşağıdaki satırları ekleyin.

        ``` xml
        <add source="assembly" value="Contoso.Commerce.Runtime.DocumentProvider.CleanCashSample" />
        <add source="assembly" value="Microsoft.Dynamics.Commerce.Runtime.ReceiptsSweden" />
        ```

    - **HardwareStation.Extension.config** yapılandırma dosyasında, **composition** bölümüne aşağıdaki satırı ekleyin.

        ``` xml
        <add source="assembly" value="Contoso.Commerce.HardwareStation.CleanCashSample" />
        ```

2. **BuildTools** klasöründeki **Customization.settings** paket özelleştirme yapılandırma dosyasında aşağıdaki değişiklikleri yapın:

    - CRT uzantılarını dağıtılabilir paketlere dahil etmek için aşağıdaki satırı ekleyin.

        ``` xml
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.DocumentProvider.CleanCashSample.dll" />
        ```

    - Hardware station uzantısını dağıtılabilir paketlere dahil etmek için aşağıdaki satırları ekleyin.

        ``` xml
        <ISV_HardwareStation_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.HardwareStation.CleanCashSample.dll" />
        <ISV_HardwareStation_CustomizableFile Include="$(SdkReferencesPath)\Interop.CleanCash_1_1.dll" />
        ```

3. **RetailSDK\\POS\\Extensions** klasöründeki **extensions.json** dosyasına aşağıdaki satırları ekleyerek POS uzantısını etkinleştirin.

    ``` json
    {
        "extensionPackages": [
            {
            "baseUrl": "Microsoft/AuditEvent.SE"
            }
        ]
    }
    ```

4. Visual Studio için MSBuild Komut İstemi yardımcı programını başlatın ve dağıtılabilir paketler oluşturmak üzere Retail SDK klasöründeki **msbuild** öğesini çalıştırın.
5. Paketleri LCS aracılığıyla veya el ile uygulayın. Daha fazla bilgi için bkz. [Dağıtılabilir paketler oluşturma](../dev-itpro/retail-sdk/retail-sdk-packaging.md).
6. [Kontrol birimleriyle tümleştirmeyi ayarlama](emea-swe-fi-sample.md#setting-up-the-integration-with-control-units) konusunda açıklanan gerekli tüm kurulum görevlerini tamamlayın.

## <a name="design-of-the-extensions"></a>Uzantıların tasarımı

### <a name="crt-extension-design"></a>CRT uzantısı tasarımı

Bir mali belge sağlayıcısı olan uzantının amacı, hizmete özel belgeler oluşturmak ve kontrol biriminden gelen yanıtları işlemektir.

CRT uzantısı **Runtime.Extensions.DocumentProvider.CleanCashSample** öğesidir.

Mali tümleştirme çözümünün tasarımı hakkında daha fazla bilgi için bkz. [Mali cihazlar ve hizmetler için mali kayıt işlemi ve mali tümleştirme örnekleri](fiscal-integration-for-retail-channel.md#fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices-and-services).

#### <a name="request-handler"></a>İstek işleyicisi

Belge sağlayıcısı için tek bir **DocumentProviderCleanCash** istek işleyicisi vardır. Bu işleyici, kontrol birimi için mali belgeler oluşturmak üzere kullanılır.

Bu işleyici **INamedRequestHandler** arabiriminden devralınır. **HandlerName** yöntemi, işleyicinin adını döndürmekten sorumludur. İşleyicinin adı, Commerce Headquarters'da belirtilen bağlayıcı belge sağlayıcı adıyla eşleşmelidir.

Bağlayıcı aşağıdaki istekleri destekler:

- **GetFiscalDocumentDocumentProviderRequest** – Bu istek, hangi belgelerin oluşturulması gerektiği bilgisini içerir. Kontrol birimine kaydedilmesi gereken, hizmete özgü bir belgeyi döndürür.
- **GetSupportedRegistrableEventsDocumentProviderRequest** – Bu istek, abone olunacak olay listesini döndürür. Şu anda satış olayları ve denetim olayları desteklenmektedir.

#### <a name="configuration"></a>Yapılandırma

**DocumentProviderFiscalCleanCashSample** yapılandırma dosyası, uzantı projesinin **Configuration** klasöründe bulunur. Bu dosyanın amacı, belge sağlayıcısı ayarlarının Commerce Headquarters'dan yapılandırılmasını etkinleştirmektir. Dosya biçimi, mali tümleştirme yapılandırmasıyla ilgili gereksinimlere uygundur. Aşağıdaki ayarlar eklenmiştir:

- KDV kodları eşlemesi

### <a name="hardware-station-extension-design"></a>Hardware station uzantı tasarımı

Bir mali bağlayıcı olan uzantının amacı, kontrol birimi ile iletişim kurmaktır.

Hardware station uzantısı, **HardwareStation.Extension.CleanCashSample** öğesidir. CRT uzantısının oluşturduğu belgeleri kontrol birimine göndermek için HTTP protokolünü kullanır. Ayrıca, kontrol biriminden alınan yanıtları da işler.

#### <a name="request-handler"></a>İstek işleyicisi

**CleanCashHandler** istek işleyicisi, kontrol birimine giden isteklerin işlenmesi için giriş noktasıdır.

İşleyici **INamedRequestHandler** arabiriminden devralınır. **HandlerName** yöntemi, işleyicinin adını döndürmekten sorumludur. İşleyicinin adı, Commerce Headquarters'da belirtilen mali bağlayıcı adıyla eşleşmelidir.

Bağlayıcı aşağıdaki istekleri destekler:

- **SubmitDocumentFiscalDeviceRequest** – Bu istek, belgeleri kontrol birimine gönderir ve hizmetten bir yanıt döndürür.
- **IsReadyFiscalDeviceRequest** – Bu istek, kontrol biriminin sistem durumu denetimi için kullanılır.
- **InitializeFiscalDeviceRequest** – Bu istek, kontrol birimini başlatmak için kullanılır.

#### <a name="configuration"></a>Yapılandırma

Yapılandırma dosyası, uzantı projesinin **Configuration** klasöründe bulunur. Dosyanın amacı, mali bağlayıcı ayarlarının Commerce Headquarters'dan yapılandırılmasını etkinleştirmektir. Dosya biçimi, mali tümleştirme yapılandırmasıyla ilgili gereksinimlere uygundur. Aşağıdaki ayarlar eklenmiştir:

- **Bağlantı dizesi** – Kontrol birimi bağlantı ayarları.
- **Zaman aşımı** – Sürücünün kontrol biriminden yanıt gelmesini bekleyeceği süre (milisaniye cinsinden).

## <a name="migrating-from-the-earlier-integration-sample"></a>Önceki tümleştirme örneğinden geçiş yapma

Önceki [İsveç için kontrol birimleriyle POS tümleştirmesi örneğini](retail-sdk-control-unit-sample.md) kullanıyorsanız bu örnekten güncel tümleştirme örneğine geçmeniz gerekebilir. İsveç özelliklerindeki değişiklikleri ve güncelleştirmeleri zamanında almak için, oluşturduğunuz uzantıları yükseltmeniz, bu uzantılarda küçük kod ve yapılandırma ayarlamaları yapmanız ve çözümlerinizi yeniden oluşturmanız gerekebilir. Oluşturduğunuz uzantı mantığında önemli değişikliklere gerek yoktur. Önceki tümleştirme örneği ve özelleştirmeleriniz, sizin tarafınızdan herhangi bir değişiklik yapılmaması durumunda çalışmaya devam edecektir. Böylece, ortamınız için planlama yapabilir, hazırlanabilir ve alım yapabilirsiniz.

### <a name="migration-process"></a>Geçiş işlemi

Önceki tümleştirme örneğinden güncel kontrol birimi tümleştirme örneğine geçiş, aşamalı güncelleştirme kavramına dayanarak yapılmalıdır. Başka bir deyişle, POS ve Hardware station bileşenlerini güncelleştirmeye başlamadan önce tüm Commerce Headquarters ve Commerce Scale Unit bileşenleri güncelleştirilmiş olmalıdır.

Bir olayın veya hareketin iki kez imzalanması (yani, hem önceki uzantı hem de güncel uzantı tarafından imzalanması) veya eksik yapılandırma nedeniyle bir olay veya hareketin imzalanamaması durumunu önlemeye yardımcı olması için, önceki örneği kullanan tüm POS ve Hardware station cihazlarını kapatmanız ve bunları eş zamanlı olarak güncelleştirmeniz önerilir. Bu eş zamanlı güncelleştirme örneğin, mağazanın işlev profili ve Hardware station'ın donanım profili güncelleştirilerek her bir mağaza özelinde yapılabilir.

Geçiş işlemi aşağıdaki adımlardan oluşmalıdır.

1. Commerce Headquarters bileşenlerini güncelleştirin.
1. Commerce Scale Unit bileşenlerini güncelleştirin ve güncel örneğin uzantılarını etkinleştirin.
1. Tüm çevrimdışı hareketlerin, çevrimdışı olarak etkinleştirilmiş MPOS cihazlarından eşitlendiğinden emin olun.
1. Önceki örneğin bileşenlerini kullanan tüm cihazları kapatın.
1. [Kontrol birimleriyle tümleştirmeyi ayarlama](emea-swe-fi-sample.md#setting-up-the-integration-with-control-units) konusunda açıklanan gerekli tüm kurulum görevlerini tamamlayın.
1. POS ve Hardware station bileşenlerini güncelleştirin, önceki örneğin parçası olan uzantıları devre dışı bırakın ve güncel örneğin uzantılarını etkinleştirin.

    > [!NOTE]
    > Ortam türüne bağlı olarak, bu makalenin [Geliştirme ortamında geçiş](#migration-in-a-development-environment) veya [Üretim ortamında geçiş](#migration-in-a-production-environment) bölümünde geçiş işlemi hakkında daha fazla teknik ayrıntı bulabilirsiniz.

### <a name="migration-in-a-development-environment"></a>Geliştirme ortamında geçiş

#### <a name="update-crt"></a>CRT öğesini güncelleştir

1. **Runtime.Extensions.DocumentProvider.CleanCashSample** projesini bulun ve derleyin.
2. **Runtime.Extensions.DocumentProvider.CleanCashSample\\bin\\Debug** klasöründe **Contoso.Commerce.Runtime.DocumentProvider.CleanCashSample.dll** derleme dosyasını bulun.
3. Derleme dosyasını CRT uzantılar klasörüne kopyalayın:

    - **Commerce Scale Unit:** Dosyayı IIS Commerce Scale Unit site konumundaki **\\bin\\ext** klasörüne kopyalayın.
    - **Modern POS'taki yerel CRT:** Dosyayı yerel CRT istemci aracısı konumunda yer alan **\\ext** klasörüne kopyalayın.

4. CRT için uzantı yapılandırma dosyasını bulun:

    - **Commerce Scale Unit:** Dosya, **CommerceRuntime.ext.config** olarak adlandırılmıştır ve IIS Commerce Scale Unit site konumundaki **bin\\ext** klasöründe yer alır.
    - **Modern POS'taki yerel CRT:** Dosya, **CommerceRuntime.MPOSOffline.Ext.config** olarak adlandırılmıştır ve yerel CRT istemci aracısı konumundaki **bin\\ext** klasöründe yer alır.

    > [!WARNING]
    > CommerceRuntime.config ve CommerceRuntime.MPOSOffline.config dosyalarını **düzenlemeyin**. Bu dosyalarda özelleştirmeler yapılması amaçlanmamıştır.

5. Uzantı yapılandırma dosyasından önceki CRT uzantısını bulun ve kaldırın.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.FiscalRegisterReceiptSample" />
    ```

    > [!WARNING]
    > Bu CRT örneğiyle çalışan tüm POS cihazlarını güncelleştirene kadar bu adımı tamamlamayın.

6. Aşağıdaki satırları ekleyerek, güncel örnek CRT uzantılarını uzantı yapılandırma dosyasına kaydedin.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.DocumentProvider.CleanCashSample" />
    <add source="assembly" value="Microsoft.Dynamics.Commerce.Runtime.ReceiptsSweden" />
    ```

#### <a name="update-hardware-station"></a>Hardware station'ı güncelleştirme

1. **HardwareStation.Extension.CleanCashSample** projesini bulun ve derleyin.
2. **Extension.CleanCashSample\\bin\\Debug** klasöründe **Contoso.Commerce.HardwareStation.CleanCashSample.dll** ve **Interop.CleanCash\_1\_1.dll** derleme dosyalarını bulun.
3. Derleme dosyalarını Hardware station uzantılar klasörüne kopyalayın:

    - **Paylaşılan hardware station:** Dosyaları IIS Hardware station site konumundaki **bin** klasörüne kopyalayın.
    - **Modern POS'taki ayrılmış hardware station:** Dosyaları Modern POS istemci aracısı konumuna kopyalayın.

4. **HardwareStation.Extension.config** uzantı yapılandırma dosyasını bulun:

    - **Uzak Hardware station:** Dosya, IIS Hardware station site konumunda yer alır.
    - **Modern POS'taki yerel Hardware station:** Dosya, Modern POS istemci aracısı konumunda yer alır.

    > [!WARNING]
    > CommerceRuntime.config ve CommerceRuntime.MPOSOffline.config dosyalarını **düzenlemeyin**. Bu dosyalarda özelleştirmeler yapılması amaçlanmamıştır.

5. Uzantı yapılandırma dosyasından önceki Hardware station uzantısını bulun ve kaldırın.

    # <a name="retail-73-and-earlier"></a>[Retail 7.3 ve öncesi](#tab/retail-7-3)

    ``` xml
    <add source="assembly" value="Contoso.Commerce.HardwareStation.Extension.FiscalRegisterSample" />
    ```

    # <a name="retail-731-and-later"></a>[Retail 7.3.1 ve sonrası](#tab/retail-7-3-1)

    ``` xml
    <add source="assembly" value="Contoso.Commerce.HardwareStation.Extension.FiscalRegisterSample" />
    ```

    # <a name="retail-100-and-later"></a>[Retail 10.0 ve sonrası](#tab/retail-10-0)

    ``` xml
    <add source="assembly" value="Contoso.Commerce.HardwareStation.FiscalRegisterSample" />
    ```
    ---

6. Uzantı yapılandırma dosyasının **composition** bölümüne aşağıdaki satırı ekleyin.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.HardwareStation.CleanCashSample" />
    ```

#### <a name="update-modern-pos"></a>Modern POS'u güncelleştirme

1. **RetailSdk\\POS** bölümündeki **CloudPOS.sln** çözümünü açın.
2. **extensions.json** dosyasından aşağıdaki satırları kaldırarak önceki POS uzantısını devre dışı bırakın.

    ``` json
    {
        "baseUrl": "FiscalRegisterSample"
    }
    ```

2. Güncel örnek POS uzantısını etkinleştirmek için **extensions.json** dosyasına aşağıdaki satırları ekleyin.

    ``` json
    {
        "extensionPackages": [
            {
                "baseUrl": "Microsoft/AuditEvent.SE"
            }
        ]
    }
    ```

#### <a name="update-cloud-pos"></a>Bulut POS'u güncelleştirme

1. **RetailSdk\\POS** bölümündeki **ModernPOS.sln** çözümünü açın.
2. **extensions.json** dosyasından aşağıdaki satırları kaldırarak önceki POS uzantısını devre dışı bırakın.

    ``` json
    {
        "baseUrl": "FiscalRegisterSample"
    }
    ```

2. Güncel örnek POS uzantısını etkinleştirmek için **extensions.json** dosyasına aşağıdaki satırları ekleyin.

    ``` json
    {
        "extensionPackages": [
            {
                "baseUrl": "Microsoft/AuditEvent.SE"
            }
        ]
    }
    ```

### <a name="migration-in-a-production-environment"></a>Üretim ortamında geçiş

#### <a name="update-crt"></a>CRT öğesini güncelleştir

1. Önceki CRT uzantısını **RetailSdk\\Assets** klasöründeki **CommerceRuntime.ext.config** ve **CommerceRuntime.MPOSOffline.Ext.config** yapılandırma dosyalarından kaldırın.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.FiscalRegisterReceiptSample" />
    ```

    > [!WARNING]
    > Bu CRT örneğiyle çalışan tüm POS cihazlarını güncelleştirene kadar bu adımı tamamlamayın.

2. **RetailSdk\\Assets** klasöründeki **CommerceRuntime.ext.config** ve **CommerceRuntime.MPOSOffline.Ext.config** yapılandırma dosyalarında aşağıdaki değişiklikleri yaparak güncel örnek CRT uzantılarını etkinleştirin.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.DocumentProvider.CleanCashSample" />
    <add source="assembly" value="Microsoft.Dynamics.Commerce.Runtime.ReceiptsSweden" />
    ```

3. **BuildTools** klasöründeki **Customization.settings** paket özelleştirme yapılandırma dosyasında, güncel örnek CRT uzantısını dağıtılabilir paketlere dahil etmek için aşağıdaki satırı ekleyin.

    ``` xml
    <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.DocumentProvider.CleanCashSample.dll" />
    ```

#### <a name="update-hardware-station"></a>Hardware station'ı güncelleştirme

1. **HardwareStation.Extension.config** yapılandırma dosyasında değişiklik yaparak önceki Hardware station uzantısını kaldırın.

    # <a name="retail-73-and-earlier"></a>[Retail 7.3 ve öncesi](#tab/retail-7-3)

    **HardwareStation.Shared.config** ve **HardwareStation.Dedicated.config** yapılandırma dosyalarından aşağıdaki bölümü kaldırın.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.HardwareStation.Extension.FiscalRegisterSample" />
    ```

    # <a name="retail-731-and-later"></a>[Retail 7.3.1 ve sonrası](#tab/retail-7-3-1)

    **HardwareStation.Extension.config** yapılandırma dosyasından aşağıdaki bölümü kaldırın.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.HardwareStation.Extension.FiscalRegisterSample" />
    ```

    # <a name="retail-100-and-later"></a>[Retail 10.0 ve sonrası](#tab/retail-10-0)

    **HardwareStation.Extension.config** yapılandırma dosyasından aşağıdaki bölümü kaldırın.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.HardwareStation.FiscalRegisterSample" />
    ```
    ---
