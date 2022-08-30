---
title: Polonya için mali yazıcı tümleştirme örneğine ilişkin dağıtım kılavuzları (eski)
description: Bu makale, Microsoft Dynamics 365 Commerce Retail yazılım geliştirme setinden (SDK) Polonya için mali yazıcı tümleştirme örneğinin dağıtılmasına ilişkin yönergeler sağlar.
author: EvgenyPopovMBS
ms.date: 08/18/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2019-03-01
ms.openlocfilehash: 178301e6d8e5f87376ed893e4bf5f966260cad62
ms.sourcegitcommit: 203c8bc263f4ab238cc7534d4dd902fd996d2b0f
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/23/2022
ms.locfileid: "9336763"
---
# <a name="deployment-guidelines-for-the-fiscal-printer-integration-sample-for-poland-legacy"></a>Polonya için mali yazıcı tümleştirme örneğine ilişkin dağıtım kılavuzları (eski)

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]

> [!IMPORTANT]
> Bu makaledeki yönergeleri yalnızca Microsoft Dynamics 365 Commerce 10.0.28 veya önceki bir sürümü kullanıyorsanız uygulamalısınız. Commerce 10.0.29 sürümü itibarıyla Polonya için mali yazıcı hizmeti tümleştirme örneği, Commerce yazılım geliştirme setinde (SDK) bulunur. Daha fazla bilgi için bkz. [Kanal bileşenlerini yapılandırma](./emea-pol-fpi-sample.md#configure-channel-components).

Bu makale, Microsoft Dynamics Lifecycle Services'taki (LCS) bir geliştirici sanal makinesinde (VM) Dynamics 365 Commerce Retail SDK'dan Polonya için mali yazıcı tümleştirme örneğinin dağıtılmasına ilişkin yönergeler sağlar. Bu mali tümleştirme örneği hakkında daha fazla bilgi için bkz. [Polonya için mali yazıcı tümleştirme örneği](emea-pol-fpi-sample.md). 

Polonya için mali tümleştirme örneği, Retail SDK'nin bir parçasıdır. SDK'yi yükleme ve kullanma hakkında daha fazla bilgi için bkz. [Retail yazılım geliştirme seti (SDK) mimarisi](../dev-itpro/retail-sdk/retail-sdk-overview.md). Bu örnek, Commerce Runtime ( CRT) ve Hardware station'a yönelik uzantılardan oluşur. Bu örneği çalıştırmak için CRT ve Hardware station projelerini değiştirip derlemeniz gerekir. Bu makalede açıklanan değişiklikleri yapmak için değiştirilmemiş bir Retail SDK kullanmanızı öneririz. Henüz değiştirilmiş bir dosya olmadığı durumlarda, Azure DevOps gibi bir kaynak denetimi sistemi kullanmanızı öneririz.

## <a name="development-environment"></a>Geliştirme ortamı

Örneği sınayabilmeniz ve genişletebilmeniz için bir geliştirme ortamı ayarlamak amacıyla bu adımları izleyin.

### <a name="commerce-runtime-extension-components"></a>Commerce Runtime uzantı bileşenleri

CRT uzantı bileşenleri, Retail SDK'ye dahil edilmiştir. Aşağıdaki yordamları tamamlamak için **RetailSdk\\SampleExtensions\\CommerceRuntime** bölümündeki **CommerceRuntimeSamples.sln** çözümünü açın.

1. **Runtime.Extensions.DocumentProvider.PosnetSample** projesini bulun ve derleyin.
2. **Extensions.DocumentProvider.PosnetSample\\bin\\Debug** klasöründe **Contoso.Commerce.Runtime.Extensions.DocumentProvider.PosnetSample.dll** derleme dosyasını bulun.
3. Derleme dosyasını CRT uzantı klasörüne kopyalayın:

    - **Commerce Scale Unit:** Dosyayı Internet Information Services (IIS) Commerce Scale Unit site konumundaki **\\bin\\ext** klasörüne kopyalayın.
    - **Modern POS'taki yerel CRT:** Dosyayı yerel CRT istemci aracısı konumunda yer alan **\\ext** klasörüne kopyalayın.

4. CRT için uzantı yapılandırma dosyasını bulun:

    - **Commerce Scale Unit:** Dosya, **commerceruntime.ext.config** olarak adlandırılmıştır ve IIS Commerce Scale Unit site konumundaki **bin\\ext** klasöründe yer alır.
    - **Modern POS'taki yerel CRT:** Dosya, **CommerceRuntime.MPOSOffline.Ext.config** olarak adlandırılmıştır ve yerel CRT istemci aracısı konumunda yer alır.

5. CRT değişikliğini uzantı yapılandırma dosyasına kaydedin.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.Extensions.DocumentProvider.PosnetSample" />
    ```

6. Commerce hizmetini yeniden başlatın:

    - **Commerce Scale Unit:** IIS Yöneticisi'nden Commerce hizmeti sitesini yeniden başlatın.
    - **İstemci aracısı:** Görev Yöneticisi'nde **dllhost.exe** işlemini sonlandırın ve ardından Modern POS'u yeniden başlatın.

### <a name="hardware-station-extension-components"></a>Hardware Station uzantı bileşenleri

Hardware station uzantı bileşenleri, Retail SDK'ye dahil edilmiştir. Aşağıdaki yordamları tamamlamak için **RetailSdk\\SampleExtensions\\HardwareStation** bölümündeki **HardwareStationSamples.sln** çözümünü açın.

1. **HardwareStation.Extension.PosnetThermalFVFiscalPrinterSample** projesini bulun ve derleyin.
2. **Extension.Posnet.ThermalFVFiscalPrinterSample\\bin\\Debug** klasöründe **Contoso.Commerce.HardwareStation.PosnetThermalFVFiscalPrinterSample.dll** derleme dosyasını bulun.
3. Derleme dosyasını dağıtılan bir Hardware station makinesine kopyalayın:

    - **Uzak Hardware station:** Dosyayı IIS Hardware station site konumundaki **bin** klasörüne kopyalayın. Yazıcı sürücüsü kitaplıklarını (**libposcmbth.dll**, **libcmbth\_serial.dll**, and **cmbth\_pl.lng**) kopyalayın.

4. Hardware station'ın uzantıları için yapılandırma dosyasını bulun. Dosya, **HardwareStation.Extension.config** olarak adlandırılmıştır:

    - **Uzak Hardware station:** Dosya, IIS Hardware station site konumunda yer alır.

5. Yapılandırma dosyasının **composition** bölümüne aşağıdaki satırı ekleyin.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.HardwareStation.PosnetThermalFVFiscalPrinterSample" />
    ```

6. Hardware station hizmetini yeniden başlatın:

    - **Uzak Hardware station:** IIS Yöneticisi'nden Hardware station sitesini yeniden başlatın.

## <a name="production-environment"></a>Üretim ortamı

Önceki yordamda, mali kayıt hizmeti tümleştirme örneğinin bileşenleri olan uzantıları etkinleştirdiniz. Buna ek olarak, Commerce bileşenleri içeren dağıtılabilir paketler oluşturmak ve bu paketleri üretim ortamında uygulamak için aşağıdaki adımları izlemeniz gerekir.

1. **RetailSdk\\Assets** klasöründeki paket yapılandırma dosyalarında aşağıdaki değişiklikleri yapın:

    - **commerceruntime.ext.config** ve **CommerceRuntime.MPOSOffline.Ext.config** yapılandırma dosyalarında, **composition** bölümüne aşağıdaki satırı ekleyin.

        ``` xml
        <add source="assembly" value="Contoso.Commerce.Runtime.Extensions.DocumentProvider.PosnetSample" />
        ```

    - **HardwareStation.Extension.config** yapılandırma dosyasında, **composition** bölümüne aşağıdaki satırı ekleyin.

        ``` xml
        <add source="assembly" value="Contoso.Commerce.HardwareStation.PosnetThermalFVFiscalPrinterSample" />
        ```

1. **BuildTools** klasöründeki **Customization.settings** paket özelleştirme yapılandırma dosyasında aşağıdaki değişiklikleri yapın:

    - CRT uzantısını dağıtılabilir paketlere dahil etmek için aşağıdaki satırı ekleyin.

        ``` xml
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.Extensions.DocumentProvider.PosnetSample.dll"/>
        ```

    - Hardware station uzantısını dağıtılabilir paketlere dahil etmek için aşağıdaki satırı ekleyin.

        ``` xml
        <ISV_HardwareStation_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.HardwareStation.PosnetThermalFVFiscalPrinterSample.dll"/>
        ```

1. Visual Studio için MSBuild Komut İstemi yardımcı programını başlatın ve dağıtılabilir paketler oluşturmak üzere Retail SDK klasöründeki **msbuild** öğesini çalıştırın.
1. Paketleri LCS aracılığıyla veya el ile uygulayın. Daha fazla bilgi için bkz. [Dağıtılabilir paketler oluşturma](../dev-itpro/retail-sdk/retail-sdk-packaging.md).

## <a name="design-of-extensions"></a>Uzantıların tasarımı

Polonya için mali yazıcı tümleştirme örneği, [mali tümleştirme işlevine](fiscal-integration-for-retail-channel.md) dayanır. Mali tümleştirme çözümünün tasarımı hakkında daha fazla bilgi için bkz. [Mali tümleştirme örneği tasarımına genel bakış](fiscal-integration-for-retail-channel.md#fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices-and-services).

### <a name="commerce-runtime-extension-design"></a>Commerce Runtime uzantı tasarımı

Bir mali belge sağlayıcısı olan uzantının amacı, yazıcıya özgü belgeler oluşturmak ve mali yazıcıdan gelen yanıtları işlemektir.

CRT uzantısı **Runtime.Extensions.DocumentProvider.PosnetSample** öğesidir. Bu uzantı, JavaScript Nesne Gösterimi (JSON) biçiminde olmak üzere, POSNET Specification 19-3678 tarafından tanımlanan yazıcıya özgü bir komut grubu oluşturur.

Mali tümleştirme çözümünün tasarımı hakkında daha fazla bilgi için bkz. [Mali cihazlar ve hizmetler için mali kayıt işlemi ve mali tümleştirme örnekleri](fiscal-integration-for-retail-channel.md#fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices-and-services).

#### <a name="request-handler"></a>İstek işleyicisi

**DocumentProviderPosnetProtocol** istek işleyicisi, mali yazıcıdan belge oluşturma isteğinin giriş noktasıdır.

İşleyici **INamedRequestHandler** arabiriminden devralınır. **HandlerName** yöntemi, işleyicinin adını döndürmekten sorumludur. İşleyicinin adı, Commerce Headquarters'da belirtilen bağlayıcı belge sağlayıcı adıyla eşleşmelidir.

Bağlayıcı aşağıdaki istekleri destekler:

- **GetFiscalDocumentDocumentProviderRequest** – Bu istek, hangi belgelerin oluşturulması gerektiği bilgisini içerir. Mali yazıcıya kaydedilmesi gereken, yazıcıya özgü bir belgeyi döndürür.
- **GetSupportedRegistrableEventsDocumentProviderRequest** – Bu istek, abone olunacak olay listesini döndürür. Şu anda şu olaylar desteklenmektedir: satış, X raporu yazdırma ve Z raporu yazdırma.

#### <a name="configuration"></a>Yapılandırma

Yapılandırma dosyası, uzantı projesinin **Configuration** klasöründe bulunur. Dosyanın amacı, belge sağlayıcısı ayarlarının Commerce Headquarters'dan yapılandırılmasını etkinleştirmektir. Dosya biçimi, mali tümleştirme yapılandırmasıyla ilgili gereksinimlere uygundur. Aşağıdaki ayarlar eklenmiştir:

- KDV oranları eşlemesi
- Ödeme türü eşlemesi
- Havale ödeme türü

### <a name="hardware-station-extension-design"></a>Hardware station uzantı tasarımı

Bir mali bağlayıcı olan uzantının amacı, mali yazıcı ile iletişim kurmaktır.

Hardware station uzantısı, **HardwareStation.Extension.PosnetThermalFVFiscalPrinterSample** öğesidir. Bu uzantı, CRT uzantısının ürettiği komutları mali yazıcıya göndermek için POSNET sürücüsünün işlevlerini çağırır. Ayrıca cihaz hatalarını işler.

#### <a name="request-handler"></a>İstek işleyicisi

**FiscalPrinterHandler** istek işleyicisi, mali çevre birimi cihazına giden isteklerin işlenmesi için giriş noktasıdır.

İşleyici **INamedRequestHandler** arabiriminden devralınır. **HandlerName** yöntemi, işleyicinin adını döndürmekten sorumludur. İşleyicinin adı, Commerce Headquarters'da belirtilen mali bağlayıcı adıyla eşleşmelidir.

Bağlayıcı aşağıdaki istekleri destekler:

- **SubmitDocumentFiscalDeviceRequest** – Bu istek, belgeleri yazıcılara gönderir ve mali yazıcıdan yanıt döndürür.
- **IsReadyFiscalDeviceRequest** – Bu istek, cihazın sistem durumu denetimi için kullanılır.
- **InitializeFiscalDeviceRequest** – Bu istek, yazıcıyı başlatmak için kullanılır.

#### <a name="configuration"></a>Yapılandırma

Yapılandırma dosyası, uzantı projesinin **Configuration** klasöründe bulunur. Dosyanın amacı, bağlayıcı ayarlarının Commerce Headquarters'dan yapılandırılmasını etkinleştirmektir. Dosya biçimi, mali tümleştirme yapılandırmasıyla ilgili gereksinimlere uygundur. Aşağıdaki ayarlar eklenmiştir:

- **Bağlantı dizesi** – Cihaz bağlantısının ayrıntılarını sürücü tarafından desteklenen bir biçimde açıklayan bir dize. Daha fazla bilgi için POSNET sürücü belgelerine bakın.
- **Tarih ve saat eşitleme** – Yazıcının tarih ve saatinin bağlı Hardware station ile eşitlenip eşitlenmeyeceğini belirten bir değer.
- **Cihaz zaman aşımı** – Sürücünün cihazdan yanıt gelmesini bekleyeceği süre (milisaniye cinsinden). Daha fazla bilgi için POSNET sürücü belgelerine bakın.
