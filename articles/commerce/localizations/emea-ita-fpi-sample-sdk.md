---
title: İtalya için mali yazıcı tümleştirme örneğine ilişkin dağıtım kılavuzları (eski)
description: Bu konu, Microsoft Dynamics 365 Commerce Retail yazılım geliştirme setinden (SDK) İtalya için mali yazıcı tümleştirme örneğinin dağıtılmasına ilişkin yönergeler sağlar.
author: EvgenyPopovMBS
ms.date: 03/04/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: epopov
ms.search.validFrom: 2019-3-1
ms.openlocfilehash: 617e97272fb4bd7cea0958958ae99648bb847b56
ms.sourcegitcommit: 7faf82fa7ce269c0201abb8473af861ef7ce00bf
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/19/2022
ms.locfileid: "8614081"
---
# <a name="deployment-guidelines-for-the-fiscal-printer-integration-sample-for-italy-legacy"></a>İtalya için mali yazıcı tümleştirme örneğine ilişkin dağıtım kılavuzları (eski)

[!include[banner](../includes/banner.md)]

Bu konu, Microsoft Dynamics Lifecycle Services'taki (LCS) bir geliştirici sanal makinesinde (VM) Microsoft Dynamics 365 Commerce Retail yazılım geliştirme setinden (SDK) İtalya için mali yazıcı tümleştirme örneğinin dağıtılmasına ilişkin yönergeler sağlar. Bu mali tümleştirme örneği hakkında daha fazla bilgi için bkz. [İtalya için mali yazıcı tümleştirme örneği](emea-ita-fpi-sample.md). 

İtalya için mali tümleştirme örneği, Retail SDK'nin bir parçasıdır. SDK'yi yükleme ve kullanma hakkında daha fazla bilgi için bkz. [Retail yazılım geliştirme seti (SDK) mimarisi](../dev-itpro/retail-sdk/retail-sdk-overview.md). Bu örnek, Commerce Runtime ( CRT) ve Hardware station'a yönelik uzantılardan oluşur. Bu örneği çalıştırmak için CRT ve Hardware station projelerini değiştirip derlemeniz gerekir. Bu konuda açıklanan değişiklikleri yapmak için değiştirilmemiş bir Retail SDK kullanmanızı öneririz. Henüz değiştirilmiş bir dosya olmadığı durumlarda, Azure DevOps gibi bir kaynak denetimi sistemi kullanmanızı öneririz.

## <a name="development-environment"></a>Geliştirme ortamı

Örneği sınayabilmeniz ve genişletebilmeniz için bir geliştirme ortamı ayarlamak amacıyla bu adımları izleyin.

### <a name="commerce-runtime-extension-components"></a>Commerce Runtime uzantı bileşenleri

CRT uzantı bileşenleri, Retail SDK'ye dahil edilmiştir. Aşağıdaki yordamları tamamlamak için **RetailSdk\\SampleExtensions\\CommerceRuntime** bölümündeki **CommerceRuntimeSamples.sln** çözümünü açın.

1. **Runtime.Extensions.DocumentProvider.EpsonFP90IIISample** projesini bulun ve derleyin.
2. **Extensions.DocumentProvider.EpsonFP90IIISample\\bin\\Debug** klasöründe **Contoso.Commerce.Runtime.DocumentProvider.EpsonFP90IIISample.dll** derleme dosyasını bulun.
3. Derleme dosyasını CRT uzantılar klasörüne kopyalayın:

    - **Commerce Scale Unit:** Dosyayı Internet Information Services (IIS) Commerce Scale Unit site konumundaki **\\bin\\ext** klasörüne kopyalayın.
    - **Modern POS'taki yerel CRT:** Dosyayı yerel CRT istemci aracısı konumunda yer alan **\\ext** klasörüne kopyalayın.

4. CRT için uzantı yapılandırma dosyasını bulun:

    - **Commerce Scale Unit:** Dosya, **commerceruntime.ext.config** olarak adlandırılmıştır ve IIS Commerce Scale Unit site konumundaki **bin\\ext** klasöründe yer alır.
    - **Modern POS'taki yerel CRT:** Dosya, **CommerceRuntime.MPOSOffline.Ext.config** olarak adlandırılmıştır ve yerel CRT istemci aracısı konumunda yer alır.

5. CRT değişikliğini uzantı yapılandırma dosyasına kaydedin.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.DocumentProvider.EpsonFP90IIISample" />
    ```

6. Commerce Scale Unit'i yeniden başlatın:

    - **Commerce Scale Unit:** IIS Yöneticisi'nden Commerce Scale Unit sitesini yeniden başlatın.
    - **İstemci aracısı:** Görev Yöneticisi'nde **dllhost.exe** işlemini sonlandırın ve ardından Modern POS'u yeniden başlatın.

### <a name="hardware-station-extension-components"></a>Hardware Station uzantı bileşenleri

Hardware station uzantı bileşenleri, Retail SDK'ye dahil edilmiştir. Aşağıdaki yordamları tamamlamak için **RetailSdk\\SampleExtensions\\HardwareStation** bölümündeki **HardwareStationSamples.sln** çözümünü açın.

1. **HardwareStation.Extensions.EpsonFP90IIIFiscalDeviceSample** projesini bulun ve derleyin.
2. **Extensions.EpsonFP90IIIFiscalDeviceSample\\bin\\Debug** klasöründe **Contoso.Commerce.HardwareStation.EpsonFP90IIIFiscalDeviceSample.dll** derleme dosyasını bulun.
3. Derleme dosyasını dağıtılan bir Hardware station makinesine kopyalayın:

    - **Uzak Hardware station:** Dosyayı IIS Hardware station site konumundaki **bin** klasörüne kopyalayın.
    - **Yerel Hardware station:** Dosyayı Modern POS istemci aracısı konumuna kopyalayın.

4. Hardware station'ın uzantıları için yapılandırma dosyasını bulun. Dosya, **HardwareStation.Extension.config** olarak adlandırılmıştır:

    - **Uzak Hardware station:** Dosya, IIS Hardware station site konumunda yer alır.
    - **Yerel Hardware station:** Dosya, Modern POS istemci aracısı konumunda bulunur.

5. Yapılandırma dosyasının **composition** bölümüne aşağıdaki bölümü ekleyin.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.HardwareStation.EpsonFP90IIIFiscalDeviceSample" />
    ```

6. Hardware station hizmetini yeniden başlatın:

    - **Uzak Hardware station:** IIS Yöneticisi'nden Hardware station sitesini yeniden başlatın.
    - **Yerel Hardware station:** Görev Yöneticisi'nde **dllhost.exe** işlemini sonlandırın ve ardından Modern POS'u yeniden başlatın.

## <a name="production-environment"></a>Üretim ortamı

Commerce bileşenleri içeren dağıtılabilir paketler oluşturmak ve bu paketleri üretim ortamında uygulamak için aşağıdaki adımları izleyin.

1. Bu konunun daha önceki [Geliştirme ortamı](#development-environment) bölümünde açıklanan adımları tamamlayın.
2. **RetailSdk\\Assets** klasöründeki paket yapılandırma dosyalarında aşağıdaki değişiklikleri yapın:

    1. **commerceruntime.ext.config** ve **CommerceRuntime.MPOSOffline.Ext.config** yapılandırma dosyalarında, **composition** bölümüne aşağıdaki satırı ekleyin.

        ``` xml
        <add source="assembly" value="Contoso.Commerce.Runtime.DocumentProvider.EpsonFP90IIISample" />
        ```

    1. **HardwareStation.Extension.config** yapılandırma dosyasında, **composition** bölümüne aşağıdaki satırı ekleyin.

        ``` xml
        <add source="assembly" value="Contoso.Commerce.HardwareStation.EpsonFP90IIIFiscalDeviceSample" />
        ```

3. **BuildTools** klasöründeki **Customization.settings** paket özelleştirme yapılandırma dosyasında aşağıdaki değişiklikleri yapın:

    1. CRT uzantısını dağıtılabilir paketlere dahil etmek için aşağıdaki satırı ekleyin.

        ``` xml
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.DocumentProvider.EpsonFP90IIISample.dll"/>
        ```

    1. Hardware station uzantısını dağıtılabilir paketlere dahil etmek için aşağıdaki satırı ekleyin.

        ``` xml
        <ISV_HardwareStation_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.HardwareStation.EpsonFP90IIIFiscalDeviceSample.dll"/>
        ```

4. İtalya için kaynak dosyaları dağıtılabilir paketlere dahil etmek için **Packages\_SharedPackagingProjectComponents** klasörü altındaki **Sdk.ModernPos.Shared.csproj** dosyasında aşağıdaki değişiklikleri yapın:

    1. İstenen çeviriler için kaynak dosyalarını gösteren düğümler içeren bir **ItemGroup** bölümü ekleyin. Doğru ad alanları ve örnek adlar belirttiğinizden emin olun. Aşağıdaki örnek, **it** ve **it-CH** yerel ayarları için kaynak düğümleri ekler.

        ```xml
        <ItemGroup>
            <ResourcesIt Include="$(SdkReferencesPath)\it\Contoso.Commerce.Runtime.DocumentProvider.EpsonFP90IIISample.resources.dll"/>
            <ResourcesItCh Include="$(SdkReferencesPath)\it-CH\Contoso.Commerce.Runtime.DocumentProvider.EpsonFP90IIISample.resources.dll"/>
        </ItemGroup>
        ```

    1. **Target Name="CopyPackageFiles"** bölümünde, her yerel ayar için aşağıdaki örnekte gösterildiği gibi bir satır ekleyin.

        ```xml
        <Copy SourceFiles="@(ResourcesIt)" DestinationFolder="$(OutputPath)content.folder\CustomizedFiles\ClientBroker\ext\it" SkipUnchangedFiles="true" />
        <Copy SourceFiles="@(ResourcesItCh)" DestinationFolder="$(OutputPath)content.folder\CustomizedFiles\ClientBroker\ext\it-CH" SkipUnchangedFiles="true" />
        ```

5. İtalya için kaynak dosyaları dağıtılabilir paketlere dahil etmek için **Packages\_SharedPackagingProjectComponents** klasörü altındaki **Sdk.RetailServerSetup.proj** dosyasında aşağıdaki değişiklikleri yapın:

    1. İstenen çeviriler için kaynak dosyalarını gösteren düğümler içeren bir **ItemGroup** bölümü ekleyin. Doğru ad alanları ve örnek adlar belirttiğinizden emin olun. Aşağıdaki örnek, **it** ve **it-CH** yerel ayarları için kaynak düğümleri ekler.

        ```xml
        <ItemGroup>
            <ResourcesIt Include="$(SdkReferencesPath)\it\Contoso.Commerce.Runtime.DocumentProvider.EpsonFP90IIISample.resources.dll"/>
            <ResourcesItCh Include="$(SdkReferencesPath)\it-CH\Contoso.Commerce.Runtime.DocumentProvider.EpsonFP90IIISample.resources.dll"/>
        </ItemGroup>
        ```

    1. **Target Name="CopyPackageFiles"** bölümünde, her yerel ayar için aşağıdaki örnekte gösterildiği gibi bir satır ekleyin.

        ``` xml
        <Copy SourceFiles="@(ResourcesIt)" DestinationFolder="$(OutputPath)content.folder\RetailServer\Code\bin\ext\it" SkipUnchangedFiles="true" />
        <Copy SourceFiles="@(ResourcesItCh)" DestinationFolder="$(OutputPath)content.folder\RetailServer\Code\bin\ext\it-CH" SkipUnchangedFiles="true" />
        ```

6. Visual Studio için MSBuild Komut İstemi yardımcı programını başlatın ve ardından dağıtılabilir paketler oluşturmak üzere Retail SDK klasöründeki **msbuild** öğesini çalıştırın.
7. Paketleri LCS aracılığıyla veya el ile uygulayın. Daha fazla bilgi için bkz. [Dağıtılabilir paketler oluşturma](../dev-itpro/retail-sdk/retail-sdk-packaging.md).

## <a name="design-of-extensions"></a>Uzantıların tasarımı

### <a name="commerce-runtime-extension-design"></a>Commerce Runtime uzantı tasarımı

Bir mali belge sağlayıcısı olan uzantının amacı, yazıcıya özgü belgeler oluşturmak ve mali yazıcıdan gelen yanıtları işlemektir.

CRT uzantısı **Runtime.Extensions.DocumentProvider.EpsonFP90IIISample** öğesidir.

Mali tümleştirme çözümünün tasarımı hakkında daha fazla bilgi için bkz. [Mali cihazlar ve hizmetler için mali kayıt işlemi ve mali tümleştirme örnekleri](fiscal-integration-for-retail-channel.md#fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices-and-services).

#### <a name="request-handler"></a>İstek işleyicisi

**DocumentProviderEpsonFP90III** istek işleyicisi, mali yazıcıdan belge oluşturma isteğinin giriş noktasıdır.

İşleyici **INamedRequestHandler** arabiriminden devralınır. **HandlerName** yöntemi, işleyicinin adını döndürmekten sorumludur. İşleyicinin adı, Commerce Headquarters'da belirtilen bağlayıcı belge sağlayıcı adıyla eşleşmelidir.

Bağlayıcı aşağıdaki istekleri destekler:

- **GetFiscalDocumentDocumentProviderRequest** – Bu istek, hangi belgelerin oluşturulması gerektiği bilgisini içerir. Mali yazıcıya kaydedilmesi gereken, yazıcıya özgü bir belgeyi döndürür.
- **GetSupportedRegistrableEventsDocumentProviderRequest** – Bu istek, abone olunacak olay listesini döndürür. Şu anda şu olaylar desteklenmektedir: satış, X raporu yazdırma ve Z raporu yazdırma.

#### <a name="configuration"></a>Yapılandırma

Yapılandırma dosyası, uzantı projesinin **Configuration** klasöründe bulunur. Dosyanın amacı, belge sağlayıcısı ayarlarının Commerce Headquarters'dan yapılandırılmasını etkinleştirmektir. Dosya biçimi, mali tümleştirme yapılandırmasıyla ilgili gereksinimlere uygundur. Aşağıdaki ayarlar eklenmiştir:

- KDV kodları eşlemesi
- KDV oranları eşlemesi
- Ödeme türü eşlemesi
- Makbuz numarası için barkod türü
- Havale ödeme türü

### <a name="hardware-station-extension-design"></a>Hardware station uzantı tasarımı

Bir mali bağlayıcı olan uzantının amacı, mali yazıcı ile iletişim kurmaktır.

Hardware station uzantısı, **HardwareStation.Extension.EpsonFP90IIIFiscalDeviceSample** öğesidir. Bu uzantı, CRT uzantısının oluşturduğu belgeleri mali yazıcıya göndermek için HTTP protokolünü kullanır. Ayrıca, mali yazıcıdan alınan yanıtları da işler.

#### <a name="request-handler"></a>İstek işleyicisi

**EpsonFP90IIISample** istek işleyicisi, mali çevre birimi cihazına giden isteklerin işlenmesi için giriş noktasıdır.

İşleyici **INamedRequestHandler** arabiriminden devralınır. **HandlerName** yöntemi, işleyicinin adını döndürmekten sorumludur. İşleyicinin adı, Commerce Headquarters'da belirtilen mali bağlayıcı adıyla eşleşmelidir.

Bağlayıcı aşağıdaki istekleri destekler:

- **SubmitDocumentFiscalDeviceRequest** – Bu istek, belgeleri yazıcılara gönderir ve mali yazıcıdan yanıt döndürür.
- **IsReadyFiscalDeviceRequest** – Bu istek, cihazın sistem durumu denetimi için kullanılır.
- **InitializeFiscalDeviceRequest** – Bu istek, yazıcıyı başlatmak için kullanılır.

#### <a name="configuration"></a>Yapılandırma

Yapılandırma dosyası, uzantı projesinin **Configuration** klasöründe bulunur. Dosyanın amacı, bağlayıcı ayarlarının Commerce Headquarters'dan yapılandırılmasını etkinleştirmektir. Dosya biçimi, mali tümleştirme yapılandırmasıyla ilgili gereksinimlere uygundur. Aşağıdaki ayarlar eklenmiştir:

- **Uç noktası adresi** – Yazıcının URL'si.
- **Tarih ve saat eşitleme** – Yazıcının tarih ve saatinin bağlı Hardware station ile eşitlenip eşitlenmeyeceğini belirten bir değer.
