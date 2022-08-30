---
title: Almanya için mali tümleştirme örneğine ilişkin dağıtım kılavuzları (eski)
description: Bu makale, Microsoft Dynamics 365 Commerce Retail yazılım geliştirme setinden (SDK) Almanya için mali tümleştirme örneğinin dağıtılmasına ilişkin yönergeler sağlar.
author: EvgenyPopovMBS
ms.date: 08/17/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2019-03-01
ms.openlocfilehash: 7315b6bb145ccdc5631a558af88de55660ebf877
ms.sourcegitcommit: 0feb5d0b06e04f99903069ff2801577be86b8555
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/18/2022
ms.locfileid: "9313868"
---
# <a name="deployment-guidelines-for-the-fiscal-registration-service-integration-sample-for-germany-legacy"></a>Almanya için mali tümleştirme örneğine ilişkin dağıtım kılavuzları (eski)

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]

> [!IMPORTANT]
> Bu makaledeki yönergeleri yalnızca Microsoft Dynamics 365 Commerce 10.0.28 veya önceki bir sürümü kullanıyorsanız uygulamalısınız. Commerce 10.0.29 sürümü itibarıyla Almanya için mali kayıt hizmeti tümleştirme örneği, Commerce yazılım geliştirme setinde (SDK) bulunur. Daha fazla bilgi için bkz. [Kanal bileşenlerini yapılandırma](./emea-deu-fi-sample.md#configure-channel-components).

Bu makale, Microsoft Dynamics Lifecycle Services'taki (LCS) bir geliştirici sanal makinesinde (VM) Dynamics 365 Commerce Retail SDK'dan Almanya için mali kayıt hizmeti tümleştirme örneğinin dağıtılmasına ilişkin yönergeler sağlar. Bu mali tümleştirme örneği hakkında daha fazla bilgi için bkz. [Almanya için mali kayıt hizmeti tümleştirme örneği](emea-deu-fi-sample.md). 

Almanya için mali tümleştirme örneği, Retail SDK'nin bir parçasıdır. SDK'yi yükleme ve kullanma hakkında daha fazla bilgi için bkz. [Retail yazılım geliştirme seti (SDK) mimarisi](../dev-itpro/retail-sdk/retail-sdk-overview.md). Bu örnek, Commerce Runtime ( CRT) ve Hardware station'a yönelik uzantılardan oluşur. Bu örneği çalıştırmak için CRT ve Hardware station projelerini değiştirip derlemeniz gerekir. Bu makalede açıklanan değişiklikleri yapmak için değiştirilmemiş bir Retail SDK kullanmanızı öneririz. Henüz değiştirilmiş bir dosya olmadığı durumlarda, Azure DevOps gibi bir kaynak denetimi sistemi kullanmanızı öneririz.

## <a name="development-environment"></a>Geliştirme ortamı

Örneği sınayabilmeniz ve genişletebilmeniz için bir geliştirme ortamı ayarlamak amacıyla bu adımları izleyin.

### <a name="enable-commerce-runtime-extensions"></a>Commerce Runtime uzantılarını etkinleştirme

CRT uzantısı bileşenleri, CRT örneklerine dahil edilmiştir. Aşağıdaki yordamları tamamlamak için **RetailSdk\\SampleExtensions\\CommerceRuntime** bölümündeki **CommerceRuntimeSamples.sln** çözümünü açın.

#### <a name="documentproviderefrsample-component"></a>DocumentProvider.EFRSample bileşeni

1. **Runtime.Extensions.DocumentProvider.EFRSample** projesini bulun ve derleyin.
2. **Runtime.Extensions.DocumentProvider.EFRSample\\bin\\Debug** klasöründe **Contoso.Commerce.Runtime.DocumentProvider.EFRSample.dll** derleme dosyasını bulun.
3. Derleme dosyasını CRT uzantılar klasörüne kopyalayın:

    - **Commerce Scale Unit:** Dosyayı Internet Information Services (IIS) Commerce Scale Unit site konumundaki **\\bin\\ext** klasörüne kopyalayın.
    - **Modern POS'taki yerel CRT:** Dosyayı yerel CRT istemci aracısı konumunda yer alan **\\ext** klasörüne kopyalayın.

4. CRT için uzantı yapılandırma dosyasını bulun:

    - **Commerce Scale Unit:** Dosya, **commerceruntime.ext.config** olarak adlandırılmıştır ve IIS Commerce Scale Unit site konumundaki **bin\\ext** klasöründe yer alır.
    - **Modern POS'taki yerel CRT:** Dosya, **CommerceRuntime.MPOSOffline.Ext.config** olarak adlandırılmıştır ve yerel CRT istemci aracısı konumunda yer alır.

5. CRT değişikliğini uzantı yapılandırma dosyasına kaydedin.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.DocumentProvider.EFRSample" />
    ```

#### <a name="documentproviderdatamodelefr-component"></a>DocumentProvider.DataModelEFR bileşeni

1. **Runtime.Extensions.DocumentProvider.DataModelEFR** projesini bulun ve derleyin.
2. **Runtime.Extensions.DocumentProvider.DataModelEFR\\bin\\Debug** klasöründe **Contoso.Commerce.Runtime.DocumentProvider.DataModelEFR.dll** derleme dosyasını bulun.
3. Derleme dosyasını CRT uzantılar klasörüne kopyalayın:

    - **Commerce Scale Unit:** Dosyayı IIS Commerce Scale Unit site konumundaki **\\bin\\ext** klasörüne kopyalayın.
    - **Modern POS'taki yerel CRT:** Dosyayı yerel CRT istemci aracısı konumunda yer alan **\\ext** klasörüne kopyalayın.

4. CRT için uzantı yapılandırma dosyasını bulun:

    - **Commerce Scale Unit:** Dosya, **commerceruntime.ext.config** olarak adlandırılmıştır ve IIS Commerce Scale Unit site konumundaki **bin\\ext** klasöründe yer alır.
    - **Modern POS'taki yerel CRT:** Dosya, **CommerceRuntime.MPOSOffline.Ext.config** olarak adlandırılmıştır ve yerel CRT istemci aracısı konumunda yer alır.

5. CRT değişikliğini uzantı yapılandırma dosyasına kaydedin.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.DocumentProvider.DataModelEFR" />
    ```

#### <a name="extension-configuration-file"></a>Uzantı yapılandırma dosyası

1. CRT için uzantı yapılandırma dosyasını bulun:

    - **Commerce Scale Unit:** Dosya, **commerceruntime.ext.config** olarak adlandırılmıştır ve IIS Commerce Scale Unit site konumundaki **bin\\ext** klasöründe yer alır.
    - **Modern POS'taki yerel CRT:** Dosya, **CommerceRuntime.MPOSOffline.Ext.config** olarak adlandırılmıştır ve yerel CRT istemci aracısı konumunda yer alır.

2. CRT değişikliğini uzantı yapılandırma dosyasına kaydedin.

    ``` xml
    <add source="assembly" value="Microsoft.Dynamics.Commerce.Runtime.ReceiptsGermany" />
    ```

### <a name="enable-fiscal-connector-extensions"></a>Mali bağlayıcı uzantılarını etkinleştirme

Mali bağlayıcı uzantılarını [Donanım istasyonuna](fiscal-integration-for-retail-channel.md#fiscal-registration-is-done-via-a-device-connected-to-the-hardware-station) veya [POS kaydına](fiscal-integration-for-retail-channel.md#fiscal-registration-is-done-via-a-device-or-service-in-the-local-network) etkinleştirebilirsiniz.

#### <a name="enable-hardware-station-extensions"></a>Hardware Station uzantılarını etkinleştirme

Hardware station uzantı bileşenleri, Hardware station örneklerine dahil edilmiştir. Aşağıdaki yordamları tamamlamak için **RetailSdk\\SampleExtensions\\HardwareStation** bölümündeki **HardwareStationSamples.sln** çözümünü açın.

##### <a name="efrsample-component"></a>EFRSample bileşeni

1. **HardwareStation.Extension.EFRSample** projesini bulun ve derleyin.
2. **Extension.EFRSample\\bin\\Debug** klasöründe aşağıdaki derleme dosyalarını bulun:

    - Contoso.Commerce.HardwareStation.EFRSample.dll
    - Contoso.Commerce.Runtime.DocumentProvider.DataModelEFR.dll

3. Derleme dosyalarını Hardware station uzantılar klasörüne kopyalayın:

    - **Paylaşılan hardware station:** Dosyaları IIS Hardware station site konumundaki **bin** klasörüne kopyalayın.
    - **Modern POS'taki ayrılmış hardware station:** Dosyaları Modern POS istemci aracısı konumuna kopyalayın.

4. Hardware station'ın uzantıları için uzantı yapılandırma dosyasını bulun. Dosya, **HardwareStation.Extension.config** olarak adlandırılmıştır.

    - **Paylaşılan hardware station:** Dosya, IIS Hardware station site konumunda yer alır.
    - **Modern POS'taki ayrılmış hardware station:** Dosya, Modern POS istemci aracısı konumunda yer alır.

5. Yapılandırma dosyasının **composition** bölümüne aşağıdaki satırı ekleyin.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.HardwareStation.EFRSample.dll" />
    ```

#### <a name="enable-pos-extensions"></a>POS uzantılarını etkinleştirme

POS uzantı örneği,, [Dynamics 365 Commerce Çözümleri](https://github.com/microsoft/Dynamics365Commerce.Solutions/) deposunun **src\\FiscalIntegration\\PosFiscalConnectorSample** klasöründe bulunur.

POS uzantı örneğini eski SDK'de kullanmak için aşağıdaki adımları izleyin.

1. **POS.Extension** klasörünü eski SDK'nın POS **Uzantıları** klasörüne kopyalayın (örneğin `C:\RetailSDK\src\POS\Extensions`).
1. **POS.Extension** klasörünün kopyasını, **PosFiscalConnector** olarak yeniden adlandırın.
1. Aşağıdaki klasörleri ve dosyaları, **PosFiscalConnector** klasöründen kaldırın:

    - bin
    - DataService
    - devDependencies
    - Kitaplıklarım
    - obj
    - Contoso.PosFiscalConnectorSample.Pos.csproj
    - RetailServerEdmxModel.g.xml
    - tsconfig.json

1. **CloudPos.sln** veya **ModernPos.sln** çözümünü açın.
1. **Pos.Extensions** projesinde, **PosFiscalConnector** klasörünü dahil edin.
1. **extensions.json** dosyasını açın ve **PosFiscalConnector** uzantısını ekleyin.
1. SDK'yı oluşturun.

### <a name="production-environment"></a>Üretim ortamı

Önceki yordamda, mali kayıt hizmeti tümleştirme örneğinin bileşenleri olan uzantıları etkinleştirdiniz. Buna ek olarak, Commerce bileşenleri içeren dağıtılabilir paketler oluşturmak ve bu paketleri üretim ortamında uygulamak için aşağıdaki adımları izlemeniz gerekir.

1. **RetailSdk\\Assets** klasöründeki paket yapılandırma dosyalarında aşağıdaki değişiklikleri yapın:

    - **commerceruntime.ext.config** ve **CommerceRuntime.MPOSOffline.Ext.config** yapılandırma dosyalarında, **composition** bölümüne aşağıdaki satırları ekleyin.

        ``` xml
        <add source="assembly" value="Microsoft.Dynamics.Commerce.Runtime.ReceiptsGermany" />
        <add source="assembly" value="Contoso.Commerce.Runtime.DocumentProvider.EFRSample" />
        <add source="assembly" value="Contoso.Commerce.Runtime.DocumentProvider.DataModelEFR" />
        ```

    - **HardwareStation.Extension.config** yapılandırma dosyasında, **composition** bölümüne aşağıdaki satırları ekleyin.

        ``` xml
        <add source="assembly" value="Contoso.Commerce.HardwareStation.EFRSample" />
        <add source="assembly" value="Contoso.Commerce.Runtime.DocumentProvider.DataModelEFR" />
        ```

2. **BuildTools** klasöründeki **Customization.settings** paket özelleştirme yapılandırma dosyasında aşağıdaki değişiklikleri yapın:

    - CRT uzantılarını dağıtılabilir paketlere dahil etmek için aşağıdaki satırları ekleyin.

        ``` xml
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.DocumentProvider.EFRSample.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.DocumentProvider.DataModelEFR.dll" />
        ```

    - Hardware station uzantılarını dağıtılabilir paketlere dahil etmek için aşağıdaki satırları ekleyin.

        ``` xml
        <ISV_HardwareStation_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.HardwareStation.EFRSample.dll" />
        <ISV_HardwareStation_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.DocumentProvider.DataModelEFR.dll" />
        ```

3. Visual Studio için MSBuild Komut İstemi yardımcı programını başlatın ve dağıtılabilir paketler oluşturmak üzere Retail SDK klasöründeki **msbuild** öğesini çalıştırın.
4. Paketleri LCS aracılığıyla veya el ile uygulayın. Daha fazla bilgi için bkz. [Dağıtılabilir paketler oluşturma](../dev-itpro/retail-sdk/retail-sdk-packaging.md).
5. [Almanya için Commerce'ı ayarlama](emea-deu-fi-sample.md#set-up-commerce-for-germany) konusunda açıklanan gerekli tüm kurulum görevlerini tamamlayın.

## <a name="design-of-extensions"></a>Uzantıların tasarımı

Almanya için mali kayıt hizmeti tümleştirme örneği, [mali tümleştirme işlevine](fiscal-integration-for-retail-channel.md) dayanır. Mali tümleştirme çözümünün tasarımı hakkında daha fazla bilgi için bkz. [Mali tümleştirme örneği tasarımına genel bakış](fiscal-integration-for-retail-channel.md#fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices-and-services).

### <a name="commerce-runtime-extension-design"></a>Commerce Runtime uzantı tasarımı

Bir mali belge sağlayıcısı olan uzantının amacı, hizmete özel belgeler oluşturmak ve mali kayıt hizmetinden gelen yanıtları işlemektir.

CRT uzantısı **Runtime.Extensions.DocumentProvider.EFRSample** öğesidir. Mali tümleştirme çözümünün tasarımı hakkında daha fazla bilgi için bkz. [Commerce kanalları için mali tümleştirme genel bakışı](fiscal-integration-for-retail-channel.md#fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices-and-services).

#### <a name="request-handler"></a>İstek işleyicisi

Belge sağlayıcısı olan **DocumentProviderEFRFiscalDEU** için bir istek işleyicisi mevcuttur. Bu işleyici, mali kayıt hizmeti için mali belgeler oluşturmak üzere kullanılır. **INamedRequestHandler** arabiriminden devralınır. **HandlerName** yöntemi, işleyicinin adını döndürmekten sorumludur. İşleyicinin adı, Commerce Headquarters'da belirtilen bağlayıcı belge sağlayıcı adıyla eşleşmelidir.

Bağlayıcı aşağıdaki istekleri destekler:

- **GetFiscalDocumentDocumentProviderRequest** – Bu istek, hangi belgelerin oluşturulması gerektiği bilgisini içerir. Mali kayıt hizmetine kaydedilmesi gereken, hizmete özgü bir belgeyi döndürür.
- **GetFiscalTransactionExtendedDataDocumentProviderRequest** – Bu istek, yanıtı genişletilmiş verilerle birlikte döndürür.

#### <a name="configuration"></a>Yapılandırma

**DocumentProviderFiscalEFRSampleGermany** yapılandırma dosyası, uzantı projesinin **Configuration** klasöründe bulunur. Bu dosyanın amacı, belge sağlayıcısı ayarlarının Commerce Headquarters'dan yapılandırılmasını etkinleştirmektir. Dosya biçimi, mali tümleştirme yapılandırmasıyla ilgili gereksinimlere uygundur.

Aşağıdaki ayarlar eklenmiştir:

- **KDV oranlarının eşlemesi** – Satış vergisi kodları için ayarlanan vergi yüzdesi değerlerinin, mali hizmete gönderilen isteklerdeki **TaxG** (vergi grubu) özniteliğinin değerleriyle eşlenmesi.
- **Hediye kartları ve havaleler için vergi grubu** – Hediye kartları veya havalelerle ilgili işlemler temel alınarak mali hizmete gönderilen isteklerdeki **TaxG** özniteliğinin değeri.
- **Ödeme türü eşlemesi** – Ödeme yöntemlerinin, mali hizmete gönderilen isteklerdeki **PayG** (ödeme grubu) özniteliğinin değerleriyle eşlenmesi.
- **KDV muafiyeti için vergi grubu** – Vergi yükümlülüklerinden muaf tutulan işlemler temel alınarak mali hizmete gönderilen isteklerdeki **TaxG** özniteliğinin değeri.
- **Müşteri verilerini dahil et** – Bu parametre açıksa mali hizmete gönderilen istekler, müşterinin bir harekete eklendiği durumlarda ad ve adres gibi müşteri bilgilerini içerecektir.

### <a name="hardware-station-extension-design"></a>Hardware station uzantı tasarımı

Bir mali bağlayıcı olan uzantının amacı, mali kayıt hizmeti ile iletişim kurmaktır.

Hardware station uzantısı, **HardwareStation.Extension.EFRSample** öğesidir. CRT uzantısının oluşturduğu belgeleri mali kayıt hizmetine göndermek için HTTP protokolünü kullanır. Ayrıca, mali kayıt hizmetinden alınan yanıtları da işler.

#### <a name="request-handler"></a>İstek işleyicisi

**EFRHandler** istek işleyicisi, mali kayıt hizmetine giden isteklerin işlenmesi için giriş noktasıdır. Bu işleyici **INamedRequestHandler** arabiriminden devralınır. **HandlerName** yöntemi, işleyicinin adını döndürmekten sorumludur. İşleyicinin adı, Commerce Headquarters'da belirtilen mali bağlayıcı adıyla eşleşmelidir.

Bağlayıcı aşağıdaki istekleri destekler:

- **SubmitDocumentFiscalDeviceRequest** – Bu istek, belgeleri mali kayıt hizmetine gönderir ve hizmetten bir yanıt döndürür.
- **IsReadyFiscalDeviceRequest** – Bu istek, mali kayıt hizmetinin sistem durumu denetimi için kullanılır.
- **InitializeFiscalDeviceRequest** – Bu istek, mali kayıt hizmetini başlatmak için kullanılır.

#### <a name="configuration"></a>Yapılandırma

Yapılandırma dosyası, uzantı projesinin **Configuration** klasöründe bulunur. Dosyanın amacı, mali bağlayıcı ayarlarının Commerce Headquarters'dan yapılandırılmasını etkinleştirmektir. Dosya biçimi, mali tümleştirme yapılandırmasıyla ilgili gereksinimlere uygundur.

Aşağıdaki ayarlar eklenmiştir:

- **Uç nokta adresi** – Mali kayıt hizmetinin URL'si.
- **Zaman aşımı** – Sürücünün mali kayıt hizmetinden yanıt gelmesini bekleyeceği, milisaniye (ms) cinsinden süre.
- **Mali kayıt bildirimlerini göster** – Bu parametre açıksa mali hizmetten gelen bildirimler POS'ta kullanıcı iletileri olarak gösterilir.

### <a name="pos-fiscal-connector-extension-design"></a>POS mali bağlayıcı uzantısı tasarımı

Bir POS mali bağlayıcı uzantısının amacı, POS'den mali kayıt hizmeti ile iletişim kurmaktır. İletişim için HTTPS protokolünü kullanır.

#### <a name="fiscal-connector-factory"></a>Mali bağlayıcı fabrikası

Mali bağlayıcı fabrikası, bağlayıcı adını mali bağlayıcı uygulamasıyla eşleştirir ve **Pos.Extension\\Connectors\\FiscalConnectorFactory.ts** dosyasında bulunur. Bağlayıcı adı, Commerce Headquarters'da belirtilen mali bağlayıcı adıyla eşleşmelidir.

#### <a name="efr-fiscal-connector"></a>EFR mali bağlayıcı

EFR mali bağlayıcısı, **Pos.Extension\\Connectors\\Efr\\EfrFiscalConnector.ts** dosyasında bulunur. Aşağıdaki istekleri destekleyen **IFiscalConnector** arabirimini uygular:

- **FiscalRegisterSubmitDocumentClientRequest** – Bu istek, belgeleri mali kayıt hizmetine gönderir ve hizmetten bir yanıt döndürür.
- **FiscalRegisterIsReadyClientRequest** – Bu istek, mali kayıt hizmetinin sistem durumu denetimi için kullanılır.
- **FiscalRegisterInitializeClientRequest** – Bu istek, mali kayıt hizmetini başlatmak için kullanılır.

#### <a name="configuration"></a>Yapılandırma

Yapılandırma dosyası, [Dynamics 365 Commerce Çözümleri](https://github.com/microsoft/Dynamics365Commerce.Solutions/) deposunun **src\\FiscalIntegration\\Efr\\Configurations\\Connectors** klasöründe bulunur. Dosyanın amacı, mali bağlayıcı ayarlarının Commerce Headquarters'dan yapılandırılmasını etkinleştirmektir. Dosya biçimi, mali tümleştirme yapılandırmasıyla ilgili gereksinimlere uygundur. Aşağıdaki ayarlar eklenmiştir:

- **Uç nokta adresi** – Mali kayıt hizmetinin URL'si.
- **Zaman aşımı** – Bağlayıcının mali kayıt hizmetinden yanıt gelmesini bekleyeceği, milisaniye cinsinden süre.
