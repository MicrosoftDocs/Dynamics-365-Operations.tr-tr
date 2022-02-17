---
title: Çek Cumhuriyeti için mali kayıt hizmeti tümleştirme örneğine ilişkin dağıtım kılavuzları (eski)
description: Bu konu, Microsoft Dynamics 365 Commerce Retail yazılım geliştirme setinden (SDK) Çek Cumhuriyeti için mali tümleştirme örneğinin dağıtılmasına ilişkin yönergeler sağlar.
author: EvgenyPopovMBS
ms.date: 12/20/2021
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: epopov
ms.search.validFrom: 2019-3-1
ms.openlocfilehash: adafde2123afdc793a6ef4edf8fa16b857c55bf8
ms.sourcegitcommit: 5cefe7d2a71c6f220190afc3293e33e2b9119685
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/01/2022
ms.locfileid: "8076948"
---
# <a name="deployment-guidelines-for-the-fiscal-registration-service-integration-sample-for-the-czech-republic-legacy"></a>Çek Cumhuriyeti için mali kayıt hizmeti tümleştirme örneğine ilişkin dağıtım kılavuzları (eski)

[!include [banner](../includes/banner.md)]

Bu konu, Microsoft Dynamics Lifecycle Services'taki (LCS) bir geliştirici sanal makinesinde (VM) Microsoft Dynamics 365 Commerce Retail yazılım geliştirme setinden (SDK) Çek Cumhuriyeti için mali kayıt hizmeti tümleştirme örneğinin dağıtılmasına ilişkin yönergeler sağlar. Bu mali tümleştirme örneği hakkında daha fazla bilgi için bkz. [Çek Cumhuriyeti için mali kayıt hizmeti tümleştirme örneği](emea-cze-fi-sample.md). 

Çek Cumhuriyeti için mali tümleştirme örneği, Retail SDK'nin bir parçasıdır. SDK'yi yükleme ve kullanma hakkında daha fazla bilgi için bkz. [Retail yazılım geliştirme seti (SDK) mimarisi](../dev-itpro/retail-sdk/retail-sdk-overview.md). Bu örnek, Commerce Runtime ( CRT) ve Hardware station'a yönelik uzantılardan oluşur. Bu örneği çalıştırmak için CRT ve Hardware station projelerini değiştirip derlemeniz gerekir. Bu konuda açıklanan değişiklikleri yapmak için değiştirilmemiş bir Retail SDK kullanmanızı öneririz. Henüz değiştirilmiş bir dosya olmadığı durumlarda, Azure DevOps gibi bir kaynak denetimi sistemi kullanmanızı öneririz.

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
    <add source="assembly" value="Microsoft.Dynamics.Commerce.Runtime.ReceiptsCzechia" />
    ```

### <a name="enable-hardware-station-extensions"></a>Hardware Station uzantılarını etkinleştirme

Hardware station uzantı bileşenleri, Hardware station örneklerine dahil edilmiştir. Aşağıdaki yordamları tamamlamak için **RetailSdk\\SampleExtensions\\HardwareStation** bölümündeki **HardwareStationSamples.sln** çözümünü açın.

#### <a name="efrsample-component"></a>EFRSample bileşeni

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

### <a name="production-environment"></a>Üretim ortamı

Önceki yordam, mali kayıt hizmeti tümleştirme örneğinin bileşenleri olan uzantıları etkinleştirir. Buna ek olarak, Commerce bileşenleri içeren dağıtılabilir paketler oluşturmak ve bu paketleri üretim ortamında uygulamak için aşağıdaki adımları izlemeniz gerekir.

1. **RetailSdk\\Assets** klasöründeki paket yapılandırma dosyalarında aşağıdaki değişiklikleri yapın.

    - **commerceruntime.ext.config** ve **CommerceRuntime.MPOSOffline.Ext.config** yapılandırma dosyalarında, **composition** bölümüne aşağıdaki satırları ekleyin.

        ``` xml
        <add source="assembly" value="Contoso.Commerce.Runtime.DocumentProvider.EFRSample" />
        <add source="assembly" value="Contoso.Commerce.Runtime.DocumentProvider.DataModelEFR" />
        <add source="assembly" value="Microsoft.Dynamics.Commerce.Runtime.ReceiptsCzechia" />
        ```

    - **HardwareStation.Extension.config** yapılandırma dosyasında, **composition** bölümüne aşağıdaki satırı ekleyin.

        ``` xml
        <add source="assembly" value="Contoso.Commerce.HardwareStation.EFRSample" />
        ```

2. **BuildTools** klasöründeki **Customization.settings** paket özelleştirme yapılandırma dosyasında aşağıdaki değişiklikleri yapın.

    - CRT uzantılarını dağıtılabilir paketlere dahil etmek için aşağıdaki satırları ekleyin.

        ``` xml
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.DocumentProvider.EFRSample.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.DocumentProvider.DataModelEFR.dll" />
        <ISV_HardwareStation_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.DocumentProvider.DataModelEFR.dll" />
        ```

    - Hardware station uzantısını dağıtılabilir paketlere dahil etmek için aşağıdaki satırı ekleyin.

        ``` xml
        <ISV_HardwareStation_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.HardwareStation.EFRSample" />
        ```

3. Visual Studio için MSBuild Komut İstemi yardımcı programını başlatın ve dağıtılabilir paketler oluşturmak üzere Retail SDK klasöründeki **msbuild** öğesini çalıştırın.
4. Paketleri LCS aracılığıyla veya el ile uygulayın. Daha fazla bilgi için bkz. [Dağıtılabilir paketler oluşturma](../dev-itpro/retail-sdk/retail-sdk-packaging.md).
5. [Çek Cumhuriyeti için Commerce'ı ayarlama](emea-cze-fi-sample.md#set-up-commerce-for-the-czech-republic) konusunda açıklanan gerekli tüm kurulum görevlerini tamamlayın.

## <a name="design-of-extensions"></a>Uzantıların tasarımı

Çek Cumhuriyeti için mali kayıt hizmeti tümleştirme örneği, [mali tümleştirme işlevine](fiscal-integration-for-retail-channel.md) dayanır. Mali tümleştirme çözümünün tasarımı hakkında daha fazla bilgi için bkz. [Mali tümleştirme örneği tasarımına genel bakış](fiscal-integration-for-retail-channel.md#fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices-and-services).

### <a name="commerce-runtime-extension-design"></a>Commerce Runtime uzantı tasarımı

Bir mali belge sağlayıcısı olan uzantının amacı, hizmete özel belgeler oluşturmak ve mali kayıt hizmetinden gelen yanıtları işlemektir.

CRT uzantısı **Runtime.Extensions.DocumentProvider.EFRSample** öğesidir.

#### <a name="request-handler"></a>İstek işleyicisi

Belge sağlayıcısı için tek bir **DocumentProviderEFRFiscalCZE** istek işleyicisi vardır. Mali kayıt hizmeti için mali belgeler oluşturmak üzere kullanılır.

Bu işleyici **INamedRequestHandler** arabiriminden devralınır. **HandlerName** yöntemi, işleyicinin adını döndürmekten sorumludur. İşleyicinin adı, Commerce Headquarters'da belirtilen bağlayıcı belge sağlayıcı adıyla eşleşmelidir.

Bağlayıcı aşağıdaki istekleri destekler:

- **GetFiscalDocumentDocumentProviderRequest** – Bu istek, hangi belgelerin oluşturulması gerektiği bilgisini içerir. Mali kayıt hizmetine kaydedilmesi gereken, hizmete özgü bir belgeyi döndürür.
- **GetSupportedRegistrableEventsDocumentProviderRequest** – Bu istek, abone olunacak olay listesini döndürür. Şu anda şu olaylar desteklenmektedir: satış, müşteri hesabı havaleleri ve müşteri siparişi havaleleri.
- **GetFiscalRegisterResponseToSaveDocumentProviderRequest** – Bu istek, mali kayıt hizmetinden gelen yanıtı döndürür. Bu yanıt, kaydedilmeye hazır olması için dize oluşturacak şekilde seri hale getirilir.

#### <a name="configuration"></a>Yapılandırma

**DocumentProviderFiscalEFRSampleCzech** yapılandırma dosyası, uzantı projesinin **Configuration** klasöründe bulunur. Bu dosyanın amacı, belge sağlayıcısı ayarlarının Commerce Headquarters'dan yapılandırılmasını etkinleştirmektir. Dosya biçimi, mali tümleştirme yapılandırmasıyla ilgili gereksinimlere uygundur. Aşağıdaki ayarlar eklenmiştir:

- KDV oranları eşlemesi
- Varsayılan KDV grubu
- Havale KDV grubu

### <a name="hardware-station-extension-design"></a>Hardware station uzantı tasarımı

Bir mali bağlayıcı olan uzantının amacı, mali kayıt hizmeti ile iletişim kurmaktır.

Hardware station uzantısı, **HardwareStation.Extension.EFRSample** öğesidir. Hardware station uzantısı, CRT uzantısının oluşturduğu belgeleri mali kayıt hizmetine göndermek için HTTP protokolünü kullanır. Ayrıca, mali kayıt hizmetinden alınan yanıtları da işler.

#### <a name="request-handler"></a>İstek işleyicisi

**EFRHandler** istek işleyicisi, mali kayıt hizmetine giden isteklerin işlenmesi için giriş noktasıdır.

İşleyici **INamedRequestHandler** arabiriminden devralınır. **HandlerName** yöntemi, işleyicinin adını döndürmekten sorumludur. İşleyicinin adı, Commerce Headquarters'da belirtilen mali bağlayıcı adıyla eşleşmelidir.

Bağlayıcı aşağıdaki istekleri destekler:

- **SubmitDocumentFiscalDeviceRequest** – Bu istek, belgeleri mali kayıt hizmetine gönderir ve hizmetten bir yanıt döndürür.
- **IsReadyFiscalDeviceRequest** – Bu istek, mali kayıt hizmetinin sistem durumu denetimi için kullanılır.
- **InitializeFiscalDeviceRequest** – Bu istek, mali kayıt hizmetini başlatmak için kullanılır.

#### <a name="configuration"></a>Yapılandırma

Yapılandırma dosyası, uzantı projesinin **Configuration** klasöründe bulunur. Dosyanın amacı, mali bağlayıcı ayarlarının Commerce Headquarters'dan yapılandırılmasını etkinleştirmektir. Dosya biçimi, mali tümleştirme yapılandırmasıyla ilgili gereksinimlere uygundur. Aşağıdaki ayarlar eklenmiştir:

- **Uç nokta adresi** – Mali kayıt hizmetinin URL'si.
- **Zaman aşımı** – Sürücünün mali kayıt hizmetinden yanıt gelmesini bekleyeceği süre (milisaniye cinsinden).
