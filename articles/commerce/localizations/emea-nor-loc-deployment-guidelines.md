---
title: Norveç için yazar kasalara ilişkin dağıtım kılavuzları (eski)
description: Bu makale, Norveç için Microsoft Dynamics 365 Commerce yerelleştirmesinin nasıl etkinleştirileceğini gösteren bir dağıtım kılavuzudur.
author: EvgenyPopovMBS
ms.date: 12/20/2021
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: epopov
ms.search.validFrom: 2018-2-28
ms.openlocfilehash: 7a6450215f152779428d3b0fd83bf09761e2ad98
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8894474"
---
# <a name="deployment-guidelines-for-cash-registers-for-norway-legacy"></a>Norveç için yazar kasalara ilişkin dağıtım kılavuzları (eski)

[!include [banner](../includes/banner.md)]

Bu makale, Norveç için Microsoft Dynamics 365 Commerce yerelleştirmesinin nasıl etkinleştirileceğini gösteren bir dağıtım kılavuzudur. Yerelleştirme, çeşitli Commerce bileşeni uzantılarından oluşur. Uzantılar örneğin; makbuzlara özel alanlar yazdırmanıza, Satış Noktasına (POS) ek denetim olayları, satış hareketleri ve ödeme hareketleri kaydetmenize, satış hareketlerini dijital olarak imzalamanıza ve X ve Z raporlarını yerel biçimlerde yazdırmanıza olanak sağlar. Norveç yerelleştirmesi hakkında daha fazla bilgi için bkz. [Norveç için yazar kasa işlevi](./emea-nor-cash-registers.md).

Bu örnek, Retail yazılım geliştirme setinin (SDK) bir parçasıdır. SDK hakkında bilgi için bkz. [Retail yazılım geliştirme seti (SDK) mimarisi](../dev-itpro/retail-sdk/retail-sdk-overview.md).

Bu örnek; Commerce Runtime ( CRT), Retail Server ve POS'a yönelik uzantılardan oluşur. Bu örneği çalıştırmak için CRT, Retail Server ve POS projelerini değiştirip derlemeniz gerekir. Bu makalede açıklanan değişiklikleri yapmak için değiştirilmemiş bir Retail SDK kullanmanızı öneririz. Henüz değiştirilmiş bir dosya olmadığı durumlarda, Microsoft Visual Studio Online (VSO) gibi bir kaynak denetimi sistemi kullanmanızı öneririz.

> [!NOTE]
> Commerce 10.0.8 ve üzeri sürümlerde Retail Server, Commerce Scale Unit olarak bilinir. Bu makale uygulamanın önceki birden çok sürümü için geçerli olduğundan, makale genelinde *Retail Server* kullanılmıştır.
>
> Bu makaledeki yordamlarda yer alan bazı adımlar, kullandığınız Commerce sürümüne bağlı olarak farklılık gösterir. Daha fazla bilgi için bkz. [Dynamics 365 Retail'deki yenilikler veya değişiklikler](../get-started/whats-new.md).

### <a name="using-certificate-profiles-in-commerce-channels"></a>Commerce kanallarında sertifika profillerini kullanma

Commerce 10.0.15 ve sonraki sürümlerde, Key Vault veya Commerce Headquarters kullanılabilir olmadığında çevrimdışı duruma yük devretmeyi destekleyen, [Perakende mağazalarına yönelik kullanıcı tanımlı sertifika profillerini](./certificate-profiles-for-retail-stores.md) kullanabilirsiniz. Özellik, [Perakende kanalları için gizli dizileri yönetme](../dev-itpro/manage-secrets.md) özelliğini genişletir.

CRT uzantısında bu işlevi uygulamak için aşağıdaki adımları izleyin.

1. Yeni bir CRT uzantı projesi (C# sınıf kitaplığı proje türü) oluşturun. Retail yazılım geliştirme setindeki (SDK) örnek şablonları kullanın (RetailSDK\SampleExtensions\CommerceRuntime).

2. CertificateSignatureServiceRequest için özel işleyiciyi SequentialSignatureRegister projesine ekleyin.

3. Bir gizli dizi çağrısını okumak için, profileId parametresiyle bir oluşturucu kullanarak `GetUserDefinedSecretCertificateServiceRequest` komutunu verin. Bu, Sertifika profillerindeki ayarlarla çalışma işlevini başlatır. Ayarlara bağlı olarak sertifika, Azure Key Vault'tan veya yerel makine depolama alanından alınır.

    ```csharp
    GetUserDefinedSecretCertificateServiceRequest getUserDefinedSecretCertificateServiceRequest = new GetUserDefinedSecretCertificateServiceRequest(profileId: "ProfileId", secretName: null, thumbprint: null, expirationInterval: null);
    GetUserDefinedSecretCertificateServiceResponse getUserDefinedSecretCertificateServiceResponse = request.RequestContext.Execute<GetUserDefinedSecretCertificateServiceResponse>(getUserDefinedSecretCertificateServiceRequest);

    X509Certificate2 Certificate = getUserDefinedSecretCertificateServiceResponse.Certificate;
    ```

4. Sertifika alındığında veri imzalaması işlemiyle devam edin.

5. CRT uzantı projesini derleyin.

6. Çıktı sınıfı kitaplığını kopyalayın ve el ile test işlemi için ...\RetailServer\webroot\bin\Ext dizinine yapıştırın.

7. CommerceRuntime.Ext.config dosyasında, uzantı bileşimi bölümünü özel kitaplık bilgileriyle güncelleştirin.

## <a name="development-environment"></a>Geliştirme ortamı

Örneği sınayabilmeniz ve genişletebilmeniz için bir geliştirme ortamı ayarlamak amacıyla bu yordamları tamamlayın.

### <a name="the-crt-extension-components"></a>CRT uzantısı bileşenleri

CRT uzantısı bileşenleri, CRT örneklerine dahil edilmiştir. Aşağıdaki yordamları tamamlamak için **RetailSdk\\SampleExtensions\\CommerceRuntime** bölümündeki CRT çözümü **CommerceRuntimeSamples.sln**'yi açın.

#### <a name="receiptsnorway-component"></a>ReceiptsNorway bileşeni

1. **Runtime.Extensions.ReceiptsNorway** projesini bulun ve derleyin.
2. **Extensions.ReceiptsNorway\\bin\\Debug** klasöründe **Contoso.Commerce.Runtime.ReceiptsNorway.dll** derleme dosyasını bulun.
3. Derleme dosyasını CRT uzantılar klasörüne kopyalayın:

    - **Retail Server:** Derlemeyi Microsoft Internet Information Services (IIS) Retail Server site konumundaki **\\bin\\ext** klasörüne kopyalayın.
    - **Modern POS'taki yerel CRT:** Derlemeyi yerel CRT istemci aracısı konumunda yer alan **\\ext** klasörüne kopyalayın.

4. CRT için uzantı yapılandırma dosyasını bulun:

    - **Retail Server:** Dosya, **commerceruntime.ext.config** olarak adlandırılmıştır ve IIS Retail Server site konumundaki **bin\\ext** klasöründe yer alır.
    - **Modern POS'taki yerel CRT:** Dosya, **CommerceRuntime.MPOSOffline.Ext.config** olarak adlandırılmıştır ve yerel CRT istemci aracısı konumunda yer alır.

5. CRT değişikliğini uzantı yapılandırma dosyasına kaydedin.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.ReceiptsNorway" />
    ```

    > [!WARNING]
    > commerceruntime.config ve CommerceRuntime.MPOSOffline.config dosyalarını **düzenlemeyin**. Bu dosyalarda özelleştirmeler yapılması amaçlanmamıştır.

#### <a name="salespaymenttransext-component"></a>SalesPaymentTransExt bileşeni

1. **Runtime.Extensions.SalesPaymentTransExt** projesini bulun ve derleyin.
2. **Extensions.SalesPaymentTransExt\\bin\\Debug** klasöründe **Contoso.Commerce.Runtime.SalesPaymentTransExt.dll** derleme dosyasını bulun.
3. Derleme dosyasını CRT uzantılar klasörüne kopyalayın:

    - **Retail Server:** Derlemeyi IIS Retail Server site konumundaki **\\bin\\ext** klasörüne kopyalayın.
    - **Modern POS'taki yerel CRT:** Derlemeyi yerel CRT istemci aracısı konumunda yer alan **\\ext** klasörüne kopyalayın.

4. CRT için uzantı yapılandırma dosyasını bulun:

    - **Retail Server:** Dosya, **commerceruntime.ext.config** olarak adlandırılmıştır ve IIS Retail Server site konumundaki **bin\\ext** klasöründe yer alır.
    - **Modern POS'taki yerel CRT:** Dosya, **CommerceRuntime.MPOSOffline.Ext.config** olarak adlandırılmıştır ve yerel CRT istemci aracısı konumunda yer alır.

5. CRT değişikliğini uzantı yapılandırma dosyasına kaydedin.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.SalesPaymentTransExt" />
    ```

    > [!WARNING]
    > commerceruntime.config ve CommerceRuntime.MPOSOffline.config dosyalarını **düzenlemeyin**. Bu dosyalarda özelleştirmeler yapılması amaçlanmamıştır.

#### <a name="xzreportsnorway-component"></a>XZReportsNorway bileşeni

1. **Runtime.Extensions.XZReportsNorway** projesini bulun ve derleyin.
2. **Extensions.XZReportsNorway\\bin\\Debug** klasöründe **Contoso.Commerce.Runtime.XZReportsNorway.dll** derleme dosyasını bulun.
3. Derleme dosyasını CRT uzantılar klasörüne kopyalayın:

    - **Retail Server:** Derlemeyi IIS Retail Server site konumundaki **\\bin\\ext** klasörüne kopyalayın.
    - **Modern POS'taki yerel CRT:** Derlemeyi yerel CRT istemci aracısı konumunda yer alan **\\ext** klasörüne kopyalayın.

4. CRT için uzantı yapılandırma dosyasını bulun:

    - **Retail Server:** Dosya, **commerceruntime.ext.config** olarak adlandırılmıştır ve IIS Retail Server site konumundaki **bin\\ext** klasöründe yer alır.
    - **Modern POS'taki yerel CRT:** Dosya, **CommerceRuntime.MPOSOffline.Ext.config** olarak adlandırılmıştır ve yerel CRT istemci aracısı konumunda yer alır.

5. CRT değişikliğini uzantı yapılandırma dosyasına kaydedin.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.XZReportsNorway" />
    ```

    > [!WARNING]
    > commerceruntime.config ve CommerceRuntime.MPOSOffline.config dosyalarını **düzenlemeyin**. Bu dosyalarda özelleştirmeler yapılması amaçlanmamıştır.

# <a name="application-update-4"></a>[Uygulama güncelleştirmesi 4](#tab/app-update-4)

#### <a name="registerauditevent-sample-component"></a>RegisterAuditEvent örnek bileşeni

1. **Runtime.Extensions.RegisterAuditEventSample** projesini bulun ve derleyin.
2. **Extensions.RegisterAuditEventSample\\bin\\Debug** klasöründe **Contoso.Commerce.Runtime.RegisterAuditEventSample.dll** derleme dosyasını bulun.
3. Derleme dosyasını CRT uzantılar klasörüne kopyalayın:

    - **Retail Server:** Derlemeyi IIS Retail Server site konumundaki **\\bin\\ext** klasörüne kopyalayın.
    - **Modern POS'taki yerel CRT:** Derlemeyi yerel CRT istemci aracısı konumunda yer alan **\\ext** klasörüne kopyalayın.

4. CRT için uzantı yapılandırma dosyasını bulun:

    - **Retail Server:** Dosya, **commerceruntime.ext.config** olarak adlandırılmıştır ve IIS Retail Server site konumundaki **bin\\ext** klasöründe yer alır.
    - **Modern POS'taki yerel CRT:** Dosya, **CommerceRuntime.MPOSOffline.Ext.config** olarak adlandırılmıştır ve yerel CRT istemci aracısı konumunda yer alır.

5. CRT değişikliğini uzantı yapılandırma dosyasına kaydedin.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.RegisterAuditEventSample" />
    ```

    > [!WARNING]
    > commerceruntime.config ve CommerceRuntime.MPOSOffline.config dosyalarını **düzenlemeyin**. Bu dosyalarda özelleştirmeler yapılması amaçlanmamıştır.

#### <a name="salestransactionsignature-sample-component"></a>SalesTransactionSignature örnek bileşeni

1. **Runtime.Extensions.SalesTransactionSignatureSample** projesini bulun.
2. Satış hareketlerini imzalamak için kullanılması gereken sertifikanın parmak izini, mağaza konumunu ve mağaza adını belirterek **App.config** dosyasını değiştirin.
3. Projeyi derleyin.
4. **Extensions.SalesTransactionSignatureSample\\bin\\Debug** klasöründe aşağıdaki dosyaları bulun:

    - **Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll** derleme dosyası
    - **Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll.config** yapılandırma dosyası

5. Dosyaları CRT uzantıları klasörüne kopyalayın:

    - **Retail Server:** Derlemeyi IIS Retail Server site konumundaki **\\bin\\ext** klasörüne kopyalayın.
    - **Modern POS'taki yerel CRT:** Derlemeyi yerel CRT istemci aracısı konumunda yer alan **\\ext** klasörüne kopyalayın.

6. CRT için uzantı yapılandırma dosyasını bulun:

    - **Retail Server:** Dosya, **commerceruntime.ext.config** olarak adlandırılmıştır ve IIS Retail Server site konumundaki **bin\\ext** klasöründe yer alır.
    - **Modern POS'taki yerel CRT:** Dosya, **CommerceRuntime.MPOSOffline.Ext.config** olarak adlandırılmıştır ve yerel CRT istemci aracısı konumunda yer alır.

7. CRT değişikliğini uzantı yapılandırma dosyasına kaydedin.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.SalesTransactionSignatureSample" />
    ```

    > [!WARNING]
    > commerceruntime.config ve CommerceRuntime.MPOSOffline.config dosyalarını **düzenlemeyin**. Bu dosyalarda özelleştirmeler yapılması amaçlanmamıştır.

# <a name="application-update-5-and-later"></a>[Uygulama güncelleştirmesi 5 ve sonrası](#tab/app-update-5-and-later)

#### <a name="registerauditevent-sample-component"></a>RegisterAuditEvent örnek bileşeni

1. **Runtime.Extensions.RegisterAuditEventSample** projesini bulun ve derleyin.
2. **Extensions.RegisterAuditEventSample\\bin\\Debug** klasöründe **Contoso.Commerce.Runtime.RegisterAuditEventSample.dll** derleme dosyasını bulun.
3. Derleme dosyasını CRT uzantılar klasörüne kopyalayın:

    - **Retail Server:** Derlemeyi IIS Retail Server site konumundaki **\\bin\\ext** klasörüne kopyalayın.
    - **Modern POS'taki yerel CRT:** Derlemeyi yerel CRT istemci aracısı konumunda yer alan **\\ext** klasörüne kopyalayın.

4. CRT için uzantı yapılandırma dosyasını bulun:

    - **Retail Server:** Dosya, **commerceruntime.ext.config** olarak adlandırılmıştır ve IIS Retail Server site konumundaki **bin\\ext** klasöründe yer alır.
    - **Modern POS'taki yerel CRT:** Dosya, **CommerceRuntime.MPOSOffline.Ext.config** olarak adlandırılmıştır ve yerel CRT istemci aracısı konumunda yer alır.

5. CRT değişikliğini uzantı yapılandırma dosyasına kaydedin.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.RegisterAuditEventSample" />
    ```

    > [!WARNING]
    > commerceruntime.config ve CommerceRuntime.MPOSOffline.config dosyalarını **düzenlemeyin**. Bu dosyalarda özelleştirmeler yapılması amaçlanmamıştır.

#### <a name="salestransactionsignature-sample-component"></a>SalesTransactionSignature örnek bileşeni

1. **Runtime.Extensions.SalesTransactionSignatureSample** projesini bulun.
2. Satış hareketlerini imzalamak için kullanılması gereken sertifikanın parmak izini, mağaza konumunu ve mağaza adını belirterek **App.config** dosyasını değiştirin.
3. Projeyi derleyin.
4. **Extensions.SalesTransactionSignatureSample\\bin\\Debug** klasöründe aşağıdaki dosyaları bulun:

    - **Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll** derleme dosyası
    - **Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll.config** yapılandırma dosyası

5. Dosyaları CRT uzantıları klasörüne kopyalayın:

    - **Retail Server:** Derlemeyi IIS Retail Server site konumundaki **\\bin\\ext** klasörüne kopyalayın.
    - **Modern POS'taki yerel CRT:** Derlemeyi yerel CRT istemci aracısı konumunda yer alan **\\ext** klasörüne kopyalayın.

6. CRT için uzantı yapılandırma dosyasını bulun:

    - **Retail Server:** Dosya, **commerceruntime.ext.config** olarak adlandırılmıştır ve IIS Retail Server site konumundaki **bin\\ext** klasöründe yer alır.
    - **Modern POS'taki yerel CRT:** Dosya, **CommerceRuntime.MPOSOffline.Ext.config** olarak adlandırılmıştır ve yerel CRT istemci aracısı konumunda yer alır.

7. CRT değişikliğini uzantı yapılandırma dosyasına kaydedin.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.SalesTransactionSignatureSample" />
    ```

    > [!WARNING]
    > commerceruntime.config ve CommerceRuntime.MPOSOffline.config dosyalarını **düzenlemeyin**. Bu dosyalarda özelleştirmeler yapılması amaçlanmamıştır.

#### <a name="salestransactionsignaturesamplemessages-component"></a>SalesTransactionSignatureSample.Messages bileşeni

1. **Runtime.Extensions.SalesTransactionSignatureSample.Messages** projesini bulun.
2. **Extensions.SalesTransactionSignatureSample.Messages\\bin\\Debug** klasöründe **Contoso.Commerce.Runtime.SalesTransactionSignatureSample.Messages.dll** derleme dosyasını bulun.
3. Derleme dosyasını CRT uzantılar klasörüne kopyalayın:

    - **Retail Server:** Derlemeyi IIS Retail Server site konumundaki **\\bin\\ext** klasörüne kopyalayın.
    - **Modern POS'taki yerel CRT:** Derlemeyi yerel CRT istemci aracısı konumunda yer alan **\\ext** klasörüne kopyalayın.

4. CRT için uzantı yapılandırma dosyasını bulun:

    - **Retail Server:** Dosya, **commerceruntime.ext.config** olarak adlandırılmıştır ve IIS Retail Server site konumundaki **bin\\ext** klasöründe yer alır.
    - **Modern POS'taki yerel CRT:** Dosya, **CommerceRuntime.MPOSOffline.Ext.config** olarak adlandırılmıştır ve yerel CRT istemci aracısı konumunda yer alır.

5. CRT değişikliğini uzantı yapılandırma dosyasına kaydedin.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.SalesTransactionSignatureSample.Messages" />
    ```

    > [!WARNING]
    > commerceruntime.config ve CommerceRuntime.MPOSOffline.config dosyalarını **düzenlemeyin**. Bu dosyalarda özelleştirmeler yapılması amaçlanmamıştır.

# <a name="retail-731"></a>[Retail 7.3.1](#tab/retail-7-3-1)

#### <a name="registerauditevent-sample-component"></a>RegisterAuditEvent örnek bileşeni

1. **Runtime.Extensions.RegisterAuditEventSample** projesini bulun ve derleyin.
2. **Extensions.RegisterAuditEventSample\\bin\\Debug** klasöründe **Contoso.Commerce.Runtime.RegisterAuditEventSample.dll** derleme dosyasını bulun.
3. Derleme dosyasını CRT uzantılar klasörüne kopyalayın:

    - **Retail Server:** Derlemeyi IIS Retail Server site konumundaki **\\bin\\ext** klasörüne kopyalayın.
    - **Modern POS'taki yerel CRT:** Derlemeyi yerel CRT istemci aracısı konumunda yer alan **\\ext** klasörüne kopyalayın.

4. CRT için uzantı yapılandırma dosyasını bulun:

    - **Retail Server:** Dosya, **commerceruntime.ext.config** olarak adlandırılmıştır ve IIS Retail Server site konumundaki **bin\\ext** klasöründe yer alır.
    - **Modern POS'taki yerel CRT:** Dosya, **CommerceRuntime.MPOSOffline.Ext.config** olarak adlandırılmıştır ve yerel CRT istemci aracısı konumunda yer alır.

5. CRT değişikliğini uzantı yapılandırma dosyasına kaydedin.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.RegisterAuditEventSample" />
    ```

    > [!WARNING]
    > commerceruntime.config ve CommerceRuntime.MPOSOffline.config dosyalarını **düzenlemeyin**. Bu dosyalarda özelleştirmeler yapılması amaçlanmamıştır.

#### <a name="salestransactionsignature-sample-component"></a>SalesTransactionSignature örnek bileşeni

1. **Runtime.Extensions.SalesTransactionSignatureSample** projesini bulun.
2. Satış hareketlerini imzalamak için kullanılması gereken sertifikanın parmak izini, mağaza konumunu ve mağaza adını belirterek **App.config** dosyasını değiştirin.
3. Projeyi derleyin.
4. **Extensions.SalesTransactionSignatureSample\\bin\\Debug** klasöründe aşağıdaki dosyaları bulun:

    - **Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll** derleme dosyası
    - **Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll.config** yapılandırma dosyası

5. Dosyaları CRT uzantıları klasörüne kopyalayın:

    - **Retail Server:** Derlemeyi IIS Retail Server site konumundaki **\\bin\\ext** klasörüne kopyalayın.
    - **Modern POS'taki yerel CRT:** Derlemeyi yerel CRT istemci aracısı konumunda yer alan **\\ext** klasörüne kopyalayın.

6. CRT için uzantı yapılandırma dosyasını bulun:

    - **Retail Server:** Dosya, **commerceruntime.ext.config** olarak adlandırılmıştır ve IIS Retail Server site konumundaki **bin\\ext** klasöründe yer alır.
    - **Modern POS'taki yerel CRT:** Dosya, **CommerceRuntime.MPOSOffline.Ext.config** olarak adlandırılmıştır ve yerel CRT istemci aracısı konumunda yer alır.

7. CRT değişikliğini uzantı yapılandırma dosyasına kaydedin.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.SalesTransactionSignatureSample" />
    ```

    > [!WARNING]
    > commerceruntime.config ve CommerceRuntime.MPOSOffline.config dosyalarını **düzenlemeyin**. Bu dosyalarda özelleştirmeler yapılması amaçlanmamıştır.

#### <a name="sequentialsignatureregistercontracts-component"></a>SequentialSignatureRegister.Contracts bileşeni

1. **Runtime.Extensions.SequentialSignatureRegister.Contracts** projesini bulun.
2. **Extensions.SequentialSignatureRegister.Contracts\\bin\\Debug** klasöründe **Contoso.Commerce.Runtime.SequentialSignatureRegister.Contracts.dll** derleme dosyasını bulun.
3. Derleme dosyasını CRT uzantılar klasörüne kopyalayın:

    - **Retail Server:** Derlemeyi IIS Retail Server site konumundaki **\\bin\\ext** klasörüne kopyalayın.
    - **Modern POS'taki yerel CRT:** Derlemeyi yerel CRT istemci aracısı konumunda yer alan **\\ext** klasörüne kopyalayın.

# <a name="retail-732-and-later"></a>[Retail 7.3.2 ve sonrası](#tab/retail-7-3-2)

#### <a name="registerauditevent-sample-component"></a>RegisterAuditEvent örnek bileşeni

1. **Runtime.Extensions.RegisterAuditEventSample** projesini bulun ve derleyin.
2. **Extensions.RegisterAuditEventSample\\bin\\Debug** klasöründe **Contoso.Commerce.Runtime.RegisterAuditEventSample.dll** derleme dosyasını bulun.
3. Derleme dosyasını CRT uzantılar klasörüne kopyalayın:

    - **Retail Server:** Derlemeyi IIS Retail Server site konumundaki **\\bin\\ext** klasörüne kopyalayın.
    - **Modern POS'taki yerel CRT:** Derlemeyi yerel CRT istemci aracısı konumunda yer alan **\\ext** klasörüne kopyalayın.

4. CRT için uzantı yapılandırma dosyasını bulun:

    - **Retail Server:** Dosya, **commerceruntime.ext.config** olarak adlandırılmıştır ve IIS Retail Server site konumundaki **bin\\ext** klasöründe yer alır.
    - **Modern POS'taki yerel CRT:** Dosya, **CommerceRuntime.MPOSOffline.Ext.config** olarak adlandırılmıştır ve yerel CRT istemci aracısı konumunda yer alır.

5. CRT değişikliğini uzantı yapılandırma dosyasına kaydedin.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.RegisterAuditEventSample" />
    ```

    > [!WARNING]
    > commerceruntime.config ve CommerceRuntime.MPOSOffline.config dosyalarını **düzenlemeyin**. Bu dosyalarda özelleştirmeler yapılması amaçlanmamıştır.

#### <a name="sequentialsignatureregister-component"></a>SequentialSignatureRegister bileşeni

1. **Runtime.Extensions.SequentialSignatureRegister** projesini bulun.
2. Satış hareketlerini imzalamak için kullanılması gereken sertifikanın parmak izini, mağaza konumunu ve mağaza adını belirterek **App.config** dosyasını değiştirin.
3. Projeyi derleyin.
4. **Extensions.SequentialSignatureRegister\\bin\\Debug** klasöründe aşağıdaki dosyaları bulun:

    - **Contoso.Commerce.Runtime.SequentialSignatureRegister.dll** derleme dosyası
    - **Contoso.Commerce.Runtime.SequentialSignatureRegister.dll.config** yapılandırma dosyası

5. Dosyaları CRT uzantıları klasörüne kopyalayın:

    - **Retail Server:** Derlemeyi IIS Retail Server site konumundaki **\\bin\\ext** klasörüne kopyalayın.
    - **Modern POS'taki yerel CRT:** Derlemeyi yerel CRT istemci aracısı konumunda yer alan **\\ext** klasörüne kopyalayın.

6. CRT için uzantı yapılandırma dosyasını bulun:

    - **Retail Server:** Dosya, **commerceruntime.ext.config** olarak adlandırılmıştır ve IIS Retail Server site konumundaki **bin\\ext** klasöründe yer alır.
    - **Modern POS'taki yerel CRT:** Dosya, **CommerceRuntime.MPOSOffline.Ext.config** olarak adlandırılmıştır ve yerel CRT istemci aracısı konumunda yer alır.

7. CRT değişikliğini uzantı yapılandırma dosyasına kaydedin.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.SequentialSignatureRegister" />
    ```

    > [!WARNING]
    > commerceruntime.config ve CommerceRuntime.MPOSOffline.config dosyalarını **düzenlemeyin**. Bu dosyalarda özelleştirmeler yapılması amaçlanmamıştır.

#### <a name="salestransactionsignaturenorway-component"></a>SalesTransactionSignatureNorway bileşeni

1. **Runtime.Extensions.SalesTransactionSignatureNorway** projesini bulun.
2. **Extensions.SalesTransactionSignatureNorway\\bin\\Debug** klasöründe **Contoso.Commerce.Runtime.SalesTransactionSignatureNorway.dll** derleme dosyasını bulun.
3. Derleme dosyasını CRT uzantılar klasörüne kopyalayın:

    - **Retail Server:** Derlemeyi IIS Retail Server site konumundaki **\\bin\\ext** klasörüne kopyalayın.
    - **Modern POS'taki yerel CRT:** Derlemeyi yerel CRT istemci aracısı konumunda yer alan **\\ext** klasörüne kopyalayın.

4. CRT için uzantı yapılandırma dosyasını bulun:

    - **Retail Server:** Dosya, **commerceruntime.ext.config** olarak adlandırılmıştır ve IIS Retail Server site konumundaki **bin\\ext** klasöründe yer alır.
    - **Modern POS'taki yerel CRT:** Dosya, **CommerceRuntime.MPOSOffline.Ext.config** olarak adlandırılmıştır ve yerel CRT istemci aracısı konumunda yer alır.

5. CRT değişikliğini uzantı yapılandırma dosyasına kaydedin.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.SalesTransactionSignatureNorway" />
    ```

    > [!WARNING]
    > commerceruntime.config ve CommerceRuntime.MPOSOffline.config dosyalarını **düzenlemeyin**. Bu dosyalarda özelleştirmeler yapılması amaçlanmamıştır.

#### <a name="sequentialsignatureregistercontracts-component"></a>SequentialSignatureRegister.Contracts bileşeni

1. **Runtime.Extensions.SequentialSignatureRegister.Contracts** projesini bulun.
2. **Extensions.SequentialSignatureRegister.Contracts\\bin\\Debug** klasöründe **Contoso.Commerce.Runtime.SequentialSignatureRegister.Contracts.dll** derleme dosyasını bulun.
3. Derleme dosyasını CRT uzantılar klasörüne kopyalayın:

    - **Retail Server:** Derlemeyi IIS Retail Server site konumundaki **\\bin\\ext** klasörüne kopyalayın.
    - **Modern POS'taki yerel CRT:** Derlemeyi yerel CRT istemci aracısı konumunda yer alan **\\ext** klasörüne kopyalayın.

#### <a name="salespaymenttransextnorway-component"></a>SalesPaymentTransExtNorway bileşeni

1. **Runtime.Extensions.SalesPaymentTransExtNorway** projesini bulun ve derleyin.
2. **Extensions.SalesPaymentTransExtNorway\\bin\\Debug** klasöründe **Contoso.Commerce.Runtime.SalesPaymentTransExtNorway.dll** derleme dosyasını bulun.
3. Derleme dosyasını CRT uzantılar klasörüne kopyalayın:

    - **Retail Server:** Derlemeyi IIS Retail Server site konumundaki **\\bin\\ext** klasörüne kopyalayın.
    - **Modern POS'taki yerel CRT:** Derlemeyi yerel CRT istemci aracısı konumunda yer alan **\\ext** klasörüne kopyalayın.

4. CRT için uzantı yapılandırma dosyasını bulun:

    - **Retail Server:** Dosya, **commerceruntime.ext.config** olarak adlandırılmıştır ve IIS Retail Server site konumundaki **bin\\ext** klasöründe yer alır.
    - **Modern POS'taki yerel CRT:** Dosya, **CommerceRuntime.MPOSOffline.Ext.config** olarak adlandırılmıştır ve yerel CRT istemci aracısı konumunda yer alır.

5. CRT değişikliğini uzantı yapılandırma dosyasına kaydedin.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.SalesPaymentTransExtNorway" />
    ```

    > [!WARNING]
    > commerceruntime.config ve CommerceRuntime.MPOSOffline.config dosyalarını **düzenlemeyin**. Bu dosyalarda özelleştirmeler yapılması amaçlanmamıştır.

# <a name="retail-735-and-later"></a>[Retail 7.3.5 ve sonrası](#tab/retail-7-3-5)

#### <a name="registerauditeventnorway-component"></a>RegisterAuditEventNorway bileşeni

1. CRT için uzantı yapılandırma dosyasını bulun:

    - **Retail Server:** Dosya, **commerceruntime.ext.config** olarak adlandırılmıştır ve IIS Retail Server site konumundaki **bin\\ext** klasöründe yer alır.
    - **Modern POS'taki yerel CRT:** Dosya, **CommerceRuntime.MPOSOffline.Ext.config** olarak adlandırılmıştır ve yerel CRT istemci aracısı konumunda yer alır.

2. CRT değişikliğini uzantı yapılandırma dosyasına kaydedin.

    ``` xml
    <add source="assembly" value="Microsoft.Dynamics.Commerce.Runtime.RegisterAuditEventNorway" />
    ```

    > [!WARNING]
    > commerceruntime.config ve CommerceRuntime.MPOSOffline.config dosyalarını **düzenlemeyin**. Bu dosyalarda özelleştirmeler yapılması amaçlanmamıştır.

#### <a name="sequentialsignatureregister-component"></a>SequentialSignatureRegister bileşeni

1. **Runtime.Extensions.SequentialSignatureRegister** projesini bulun.
2. Satış hareketlerini imzalamak için kullanılması gereken sertifikanın parmak izini, mağaza konumunu ve mağaza adını belirterek **App.config** dosyasını değiştirin.
3. Projeyi derleyin.
4. **Extensions.SequentialSignatureRegister\\bin\\Debug** klasöründe aşağıdaki dosyaları bulun:

    - **Contoso.Commerce.Runtime.SequentialSignatureRegister.dll** derleme dosyası
    - **Contoso.Commerce.Runtime.SequentialSignatureRegister.dll.config** yapılandırma dosyası

5. Dosyaları CRT uzantıları klasörüne kopyalayın:

    - **Retail Server:** Derlemeyi IIS Retail Server site konumundaki **\\bin\\ext** klasörüne kopyalayın.
    - **Modern POS'taki yerel CRT:** Derlemeyi yerel CRT istemci aracısı konumunda yer alan **\\ext** klasörüne kopyalayın.

6. CRT için uzantı yapılandırma dosyasını bulun:

    - **Retail Server:** Dosya, **commerceruntime.ext.config** olarak adlandırılmıştır ve IIS Retail Server site konumundaki **bin\\ext** klasöründe yer alır.
    - **Modern POS'taki yerel CRT:** Dosya, **CommerceRuntime.MPOSOffline.Ext.config** olarak adlandırılmıştır ve yerel CRT istemci aracısı konumunda yer alır.

7. CRT değişikliğini uzantı yapılandırma dosyasına kaydedin.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.SequentialSignatureRegister" />
    ```

    > [!WARNING]
    > commerceruntime.config ve CommerceRuntime.MPOSOffline.config dosyalarını **düzenlemeyin**. Bu dosyalarda özelleştirmeler yapılması amaçlanmamıştır.

#### <a name="salestransactionsignaturenorway-component"></a>SalesTransactionSignatureNorway bileşeni

1. **Runtime.Extensions.SalesTransactionSignatureNorway** projesini bulun.
2. **Extensions.SalesTransactionSignatureNorway\\bin\\Debug** klasöründe **Contoso.Commerce.Runtime.SalesTransactionSignatureNorway.dll** derleme dosyasını bulun.
3. Derleme dosyasını CRT uzantılar klasörüne kopyalayın:

    - **Retail Server:** Derlemeyi IIS Retail Server site konumundaki **\\bin\\ext** klasörüne kopyalayın.
    - **Modern POS'taki yerel CRT:** Derlemeyi yerel CRT istemci aracısı konumunda yer alan **\\ext** klasörüne kopyalayın.

4. CRT için uzantı yapılandırma dosyasını bulun:

    - **Retail Server:** Dosya, **commerceruntime.ext.config** olarak adlandırılmıştır ve IIS Retail Server site konumundaki **bin\\ext** klasöründe yer alır.
    - **Modern POS'taki yerel CRT:** Dosya, **CommerceRuntime.MPOSOffline.Ext.config** olarak adlandırılmıştır ve yerel CRT istemci aracısı konumunda yer alır.

5. CRT değişikliğini uzantı yapılandırma dosyasına kaydedin.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.SalesTransactionSignatureNorway" />
    ```

    > [!WARNING]
    > commerceruntime.config ve CommerceRuntime.MPOSOffline.config dosyalarını **düzenlemeyin**. Bu dosyalarda özelleştirmeler yapılması amaçlanmamıştır.

#### <a name="sequentialsignatureregistercontracts-component"></a>SequentialSignatureRegister.Contracts bileşeni

1. **Runtime.Extensions.SequentialSignatureRegister.Contracts** projesini bulun.
2. **Extensions.SequentialSignatureRegister.Contracts\\bin\\Debug** klasöründe **Contoso.Commerce.Runtime.SequentialSignatureRegister.Contracts.dll** derleme dosyasını bulun.
3. Derleme dosyasını CRT uzantılar klasörüne kopyalayın:

    - **Retail Server:** Derlemeyi IIS Retail Server site konumundaki **\\bin\\ext** klasörüne kopyalayın.
    - **Modern POS'taki yerel CRT:** Derlemeyi yerel CRT istemci aracısı konumunda yer alan **\\ext** klasörüne kopyalayın.

#### <a name="salespaymenttransextnorway-component"></a>SalesPaymentTransExtNorway bileşeni

1. **Runtime.Extensions.SalesPaymentTransExtNorway** projesini bulun ve derleyin.
2. **Extensions.SalesPaymentTransExtNorway\\bin\\Debug** klasöründe **Contoso.Commerce.Runtime.SalesPaymentTransExtNorway.dll** derleme dosyasını bulun.
3. Derleme dosyasını CRT uzantılar klasörüne kopyalayın:

    - **Retail Server:** Derlemeyi IIS Retail Server site konumundaki **\\bin\\ext** klasörüne kopyalayın.
    - **Modern POS'taki yerel CRT:** Derlemeyi yerel CRT istemci aracısı konumunda yer alan **\\ext** klasörüne kopyalayın.

4. CRT için uzantı yapılandırma dosyasını bulun:

    - **Retail Server:** Dosya, **commerceruntime.ext.config** olarak adlandırılmıştır ve IIS Retail Server site konumundaki **bin\\ext** klasöründe yer alır.
    - **Modern POS'taki yerel CRT:** Dosya, **CommerceRuntime.MPOSOffline.Ext.config** olarak adlandırılmıştır ve yerel CRT istemci aracısı konumunda yer alır.

5. CRT değişikliğini uzantı yapılandırma dosyasına kaydedin.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.SalesPaymentTransExtNorway" />
    ```

    > [!WARNING]
    > commerceruntime.config ve CommerceRuntime.MPOSOffline.config dosyalarını **düzenlemeyin**. Bu dosyalarda özelleştirmeler yapılması amaçlanmamıştır.

# <a name="retail-811-and-later"></a>[Retail 8.1.1 ve sonrası](#tab/retail-8-1-1)

#### <a name="registerauditeventnorway-component"></a>RegisterAuditEventNorway bileşeni

1. CRT için uzantı yapılandırma dosyasını bulun:

    - **Retail Server:** Dosya, **commerceruntime.ext.config** olarak adlandırılmıştır ve IIS Retail Server site konumundaki **bin\\ext** klasöründe yer alır.
    - **Modern POS'taki yerel CRT:** Dosya, **CommerceRuntime.MPOSOffline.Ext.config** olarak adlandırılmıştır ve yerel CRT istemci aracısı konumunda yer alır.

2. CRT değişikliğini uzantı yapılandırma dosyasına kaydedin.

    ``` xml
    <add source="assembly" value="Microsoft.Dynamics.Commerce.Runtime.RegisterAuditEventNorway" />
    ```

    > [!WARNING]
    > commerceruntime.config ve CommerceRuntime.MPOSOffline.config dosyalarını **düzenlemeyin**. Bu dosyalarda özelleştirmeler yapılması amaçlanmamıştır.

#### <a name="sequentialsignatureregister-component"></a>SequentialSignatureRegister bileşeni

1. **Runtime.Extensions.SequentialSignatureRegister** projesini bulun.
2. Satış hareketlerini imzalamak için kullanılması gereken sertifikanın parmak izini, mağaza konumunu ve mağaza adını belirterek **App.config** dosyasını değiştirin.
3. Projeyi derleyin.
4. **Extensions.SequentialSignatureRegister\\bin\\Debug** klasöründe aşağıdaki dosyaları bulun:

    - **Contoso.Commerce.Runtime.SequentialSignatureRegister.dll** derleme dosyası
    - **Contoso.Commerce.Runtime.SequentialSignatureRegister.dll.config** yapılandırma dosyası

5. Dosyaları CRT uzantıları klasörüne kopyalayın:

    - **Retail Server:** Derlemeyi IIS Retail Server site konumundaki **\\bin\\ext** klasörüne kopyalayın.
    - **Modern POS'taki yerel CRT:** Derlemeyi yerel CRT istemci aracısı konumunda yer alan **\\ext** klasörüne kopyalayın.

6. CRT için uzantı yapılandırma dosyasını bulun:

    - **Retail Server:** Dosya, **commerceruntime.ext.config** olarak adlandırılmıştır ve IIS Retail Server site konumundaki **bin\\ext** klasöründe yer alır.
    - **Modern POS'taki yerel CRT:** Dosya, **CommerceRuntime.MPOSOffline.Ext.config** olarak adlandırılmıştır ve yerel CRT istemci aracısı konumunda yer alır.

7. CRT değişikliğini uzantı yapılandırma dosyasına kaydedin.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.SequentialSignatureRegister" />
    ```

    > [!WARNING]
    > commerceruntime.config ve CommerceRuntime.MPOSOffline.config dosyalarını **düzenlemeyin**. Bu dosyalarda özelleştirmeler yapılması amaçlanmamıştır.

#### <a name="salestransactionsignaturenorway-component"></a>SalesTransactionSignatureNorway bileşeni

1. **Runtime.Extensions.SalesTransactionSignatureNorway** projesini bulun.
2. **Extensions.SalesTransactionSignatureNorway\\bin\\Debug** klasöründe **Contoso.Commerce.Runtime.SalesTransactionSignatureNorway.dll** derleme dosyasını bulun.
3. Derleme dosyasını CRT uzantılar klasörüne kopyalayın:

    - **Retail Server:** Derlemeyi IIS Retail Server site konumundaki **\\bin\\ext** klasörüne kopyalayın.
    - **Modern POS'taki yerel CRT:** Derlemeyi yerel CRT istemci aracısı konumunda yer alan **\\ext** klasörüne kopyalayın.

4. CRT için uzantı yapılandırma dosyasını bulun:

    - **Retail Server:** Dosya, **commerceruntime.ext.config** olarak adlandırılmıştır ve IIS Retail Server site konumundaki **bin\\ext** klasöründe yer alır.
    - **Modern POS'taki yerel CRT:** Dosya, **CommerceRuntime.MPOSOffline.Ext.config** olarak adlandırılmıştır ve yerel CRT istemci aracısı konumunda yer alır.

5. CRT değişikliğini uzantı yapılandırma dosyasına kaydedin.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.SalesTransactionSignatureNorway" />
    ```

    > [!WARNING]
    > commerceruntime.config ve CommerceRuntime.MPOSOffline.config dosyalarını **düzenlemeyin**. Bu dosyalarda özelleştirmeler yapılması amaçlanmamıştır.

#### <a name="sequentialsignatureregistercontracts-component"></a>SequentialSignatureRegister.Contracts bileşeni

1. **Runtime.Extensions.SequentialSignatureRegister.Contracts** projesini bulun.
2. **Extensions.SequentialSignatureRegister.Contracts\\bin\\Debug** klasöründe **Contoso.Commerce.Runtime.SequentialSignatureRegister.Contracts.dll** derleme dosyasını bulun.
3. Derleme dosyasını CRT uzantılar klasörüne kopyalayın:

    - **Retail Server:** Derlemeyi IIS Retail Server site konumundaki **\\bin\\ext** klasörüne kopyalayın.
    - **Modern POS'taki yerel CRT:** Derlemeyi yerel CRT istemci aracısı konumunda yer alan **\\ext** klasörüne kopyalayın.

#### <a name="salespaymenttransextnorway-component"></a>SalesPaymentTransExtNorway bileşeni

1. **Runtime.Extensions.SalesPaymentTransExtNorway** projesini bulun ve derleyin.
2. **Extensions.SalesPaymentTransExtNorway\\bin\\Debug** klasöründe **Contoso.Commerce.Runtime.SalesPaymentTransExtNorway.dll** derleme dosyasını bulun.
3. Derleme dosyasını CRT uzantılar klasörüne kopyalayın:

    - **Retail Server:** Derlemeyi IIS Retail Server site konumundaki **\\bin\\ext** klasörüne kopyalayın.
    - **Modern POS'taki yerel CRT:** Derlemeyi yerel CRT istemci aracısı konumunda yer alan **\\ext** klasörüne kopyalayın.

4. CRT için uzantı yapılandırma dosyasını bulun:

    - **Retail Server:** Dosya, **commerceruntime.ext.config** olarak adlandırılmıştır ve IIS Retail Server site konumundaki **bin\\ext** klasöründe yer alır.
    - **Modern POS'taki yerel CRT:** Dosya, **CommerceRuntime.MPOSOffline.Ext.config** olarak adlandırılmıştır ve yerel CRT istemci aracısı konumunda yer alır.

5. CRT değişikliğini uzantı yapılandırma dosyasına kaydedin.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.SalesPaymentTransExtNorway" />
    ```

    > [!WARNING]
    > commerceruntime.config ve CommerceRuntime.MPOSOffline.config dosyalarını **düzenlemeyin**. Bu dosyalarda özelleştirmeler yapılması amaçlanmamıştır.

---

### <a name="the-retail-server-extension-components"></a>Retail Server uzantısı bileşenleri

#### <a name="salestransactionsignature-retail-server-sample-component"></a>SalesTransactionSignature Retail Server örnek bileşeni

1. **RetailSDK\\SampleExtensions\\RetailServer\\RetailServer.Extensions.SalesTransactionSignatureSample** klasöründe **RetailServer.Extensions.SalesTransactionSignatureSample** projesini bulun ve derleyin.
2. **RetailServer\\Extensions.SalesTransactionSignatureSample\\bin\\Debug** klasöründe **Contoso.RetailServer.SalesTransactionSignatureSample.dll** derleme dosyasını bulun.
3. Derleme dosyasını Retail Server uzantılar klasörüne kopyalayın.

    # <a name="application-update-4"></a>[Uygulama güncelleştirmesi 4](#tab/app-update-4)

    Klasör, IIS Retail Server site konumunda yer alan **\\bin** klasörüdür.

    # <a name="application-update-5-and-later"></a>[Uygulama güncelleştirmesi 5 ve sonrası](#tab/app-update-5-and-later)

    Klasör, IIS Retail Server site konumunda yer alan **\\bin** klasörüdür.

    # <a name="retail-731"></a>[Retail 7.3.1](#tab/retail-7-3-1)

    Klasör, IIS Retail Server site konumunda yer alan **\\bin\\ext** klasörüdür.

    # <a name="retail-732-and-later"></a>[Retail 7.3.2 ve sonrası](#tab/retail-7-3-2)

    Klasör, IIS Retail Server site konumunda yer alan **\\bin\\ext** klasörüdür.

    # <a name="retail-735-and-later"></a>[Retail 7.3.5 ve sonrası](#tab/retail-7-3-5)

    Klasör, IIS Retail Server site konumunda yer alan **\\bin\\ext** klasörüdür.

    # <a name="retail-811-and-later"></a>[Retail 8.1.1 ve sonrası](#tab/retail-8-1-1)

    Klasör, IIS Retail Server site konumunda yer alan **\\bin\\ext** klasörüdür.

    ---

4. Retail Server yapılandırma dosyasını bulun. Dosya **web.config** olarak adlandırılmıştır ve IIS Retail Server site konumundaki kök klasörde yer alır.
5. Retail Server uzantılarını yapılandırma dosyasının **extensionComposition** bölümüne kaydedin.

    ``` xml
    <add source="assembly" value="Contoso.RetailServer.SalesTransactionSignatureSample" />
    ```

6. Retail Server uzantılarının bağımlılıklarını kaydedin.

    # <a name="application-update-4"></a>[Uygulama güncelleştirmesi 4](#tab/app-update-4/)

    1. **CommerceRuntime\\Extensions.SalesTransactionSignatureSample\\bin\\Debug** klasöründe aşağıdaki dosyaları bulun:

        - **Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll** derleme dosyası
        - **Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll.config** yapılandırma dosyası

    2. Dosyaları IIS Retail Server site konumundaki **\\bin** klasörüne kopyalayın.
    3. CRT değişikliğini CRT'ye ait uzantı yapılandırma dosyasına kaydedin. Bu dosya, **commerceruntime.ext.config** olarak adlandırılmıştır ve IIS Retail Server site konumundaki **bin** klasöründe yer alır.

        ``` xml
        <add source="assembly" value="Contoso.Commerce.Runtime.SalesTransactionSignatureSample" />
        ```

    # <a name="application-update-5-and-later"></a>[Uygulama güncelleştirmesi 5 ve sonrası](#tab/app-update-5-and-later/)

    1. **CommerceRuntime\\Extensions.SalesTransactionSignatureSample.Messages\\bin\\Debug** klasöründe **Contoso.Commerce.Runtime.SalesTransactionSignatureSample.Messages.dll** derleme dosyasını bulun.
    2. Dosyayı IIS Retail Server site konumundaki **\\bin** klasörüne kopyalayın.
    3. CRT değişikliğini CRT'ye ait uzantı yapılandırma dosyasına kaydedin. Bu dosya, **commerceruntime.ext.config** olarak adlandırılmıştır ve IIS Retail Server site konumundaki **bin** klasöründe yer alır.

        ``` xml
        <add source="assembly" value="Contoso.Commerce.Runtime.SalesTransactionSignatureSample.Messages" />
        ```

    # <a name="retail-731"></a>[Retail 7.3.1](#tab/retail-7-3-1)

    > [!NOTE]
    > Herhangi bir eyleme gerek yoktur.

    # <a name="retail-732-and-later"></a>[Retail 7.3.2 ve sonrası](#tab/retail-7-3-2)

    > [!NOTE]
    > Herhangi bir eyleme gerek yoktur.

    # <a name="retail-735-and-later"></a>[Retail 7.3.5 ve sonrası](#tab/retail-7-3-5)

    > [!NOTE]
    > Herhangi bir eyleme gerek yoktur.

    # <a name="retail-811-and-later"></a>[Retail 8.1.1 ve sonrası](#tab/retail-8-1-1)

    > [!NOTE]
    > Herhangi bir eyleme gerek yoktur.

    ---

### <a name="the-modern-pos-extension-components"></a>Modern POS uzantı bileşenleri

#### <a name="implement-the-proxy-code-for-offline-mode"></a>Çevrimdışı mod için ara sunucu kodunu uygulama

Bu bölüm, Retail Server denetleyicisine eşdeğerdir ancak istemci bağlı değilken kullanılan yerel CRT'yi genişletir.

1. Ara sunucu oluşturma işlemi için yeni Retail Server derlemesinin kullanılması amacıyla, **customization.settings** dosyasında **@(RetailServerLibraryPathForProxyGeneration)** bölümünü değiştirin.
2. **StoreOperationsManager** sınıfında aşağıdaki arabirim yöntemlerini uygulayın. İlk yineleme için aşağıdaki kodu ekleyin:

    # <a name="application-update-4"></a>[Uygulama güncelleştirmesi 4](#tab/app-update-4)

    ``` csharp
    public Task<bool> SalesTransactionSignatureServiceIsReady()
    {
        throw new NotImplementedException();
    }
    public Task<FiscalTransaction> GetLastFiscalTransaction(string storeNumber, string terminalId)
    {
        throw new NotImplementedException();
    }
    ```

    # <a name="application-update-5-and-later"></a>[Uygulama güncelleştirmesi 5 ve sonrası](#tab/app-update-5-and-later)

    ``` csharp
    public Task<bool> SalesTransactionSignatureServiceIsReady(string correlationId)
    {
        throw new NotImplementedException();
    }
    public Task<FiscalTransaction> GetLastFiscalTransaction(string storeNumber, string terminalId)
    {
        throw new NotImplementedException();
    }
    ```

    # <a name="retail-731"></a>[Retail 7.3.1](#tab/retail-7-3-1)

    > [!NOTE]
    > Bu adım, bu sürüm için geçerli değildir.

    # <a name="retail-732-and-later"></a>[Retail 7.3.2 ve sonrası](#tab/retail-7-3-2)

    > [!NOTE]
    > Bu adım, bu sürüm için geçerli değildir.

    # <a name="retail-735-and-later"></a>[Retail 7.3.5 ve sonrası](#tab/retail-7-3-5)

    > [!NOTE]
    > Bu adım, bu sürüm için geçerli değildir.

    # <a name="retail-811-and-later"></a>[Retail 8.1.1 ve sonrası](#tab/retail-8-1-1)

    > [!NOTE]
    > Bu adım, bu sürüm için geçerli değildir.

    ---

3. Ara sunucu kodunu yeniden üretmek için **msbuild /t:Rebuild** komutunu kullanarak komut satırından **Proxies** klasörünü derleyin.
4. **Proxies.RetailProxy** proje bağımlılıklarını çözümleyin:

    # <a name="application-update-4"></a>[Uygulama güncelleştirmesi 4](#tab/app-update-4)

    **RetailSDK\\Proxies\\RetailProxy\\Proxies.RetailProxy.csproj** öğesini açın, çözüme **RetailSDK\\SampleExtensions\\CommerceRuntime\\Extensions.SalesTransactionSignatureSample\\CommerceRuntime.Extensions.SalesTransactionSignatureSample** projesini ekleyin ve **SalesTransactionSignatureSample** öğesine atıfta bulunmak için **RetailProxy** projesine bir proje başvurusu ekleyin.

    # <a name="application-update-5-and-later"></a>[Uygulama güncelleştirmesi 5 ve sonrası](#tab/app-update-5-and-later)

    **RetailSDK\\Proxies\\RetailProxy\\Proxies.RetailProxy.csproj** öğesini açın, çözüme **RetailSDK\\SampleExtensions\\CommerceRuntime\\Extensions.SalesTransactionSignatureSample.Messages\\CommerceRuntime.Extensions.SalesTransactionSignatureSample.Messages** projesini ekleyin ve **SalesTransactionSignatureSample.Messages** öğesine atıfta bulunmak için **RetailProxy** projesine bir proje başvurusu ekleyin.

    # <a name="retail-731"></a>[Retail 7.3.1](#tab/retail-7-3-1)

    > [!NOTE]
    > Bu adım, bu sürüm için geçerli değildir.

    # <a name="retail-732-and-later"></a>[Retail 7.3.2 ve sonrası](#tab/retail-7-3-2)

    > [!NOTE]
    > Bu adım, bu sürüm için geçerli değildir.

    # <a name="retail-735-and-later"></a>[Retail 7.3.5 ve sonrası](#tab/retail-7-3-5)

    > [!NOTE]
    > Bu adım, bu sürüm için geçerli değildir.

    # <a name="retail-811-and-later"></a>[Retail 8.1.1 ve sonrası](#tab/retail-8-1-1)

    > [!NOTE]
    > Bu adım, bu sürüm için geçerli değildir.

    ---

5. **StoreOperationsManager** sınıfındaki arabirim yöntemlerini düzeltin:

    # <a name="application-update-4"></a>[Uygulama güncelleştirmesi 4](#tab/app-update-4)

    ``` csharp
    public Task<bool> SalesTransactionSignatureServiceIsReady()
    {
        return Task.Run(() => CommerceRuntimeManager.Runtime.Execute<SalesTransactionSignatureServiceIsReadyResponse>(new SalesTransactionSignatureServiceIsReadyRequest(), null).IsReady);
    }
    public Task<FiscalTransaction> GetLastFiscalTransaction(string storeNumber, string terminalId)
    {
        return Task.Run(() => CommerceRuntimeManager.Runtime.Execute<GetLastFiscalTransactionResponse>(new GetLastFiscalTransactionRequest(), null).FiscalTransaction);
    }
    ```

    # <a name="application-update-5-and-later"></a>[Uygulama güncelleştirmesi 5 ve sonrası](#tab/app-update-5-and-later)

    ``` csharp
    public Task<bool> SalesTransactionSignatureServiceIsReady(string correlationId)
    {
        return Task.Run(() => CommerceRuntimeManager.Runtime.Execute<SalesTransactionSignatureServiceIsReadyResponse>(new SalesTransactionSignatureServiceIsReadyRequest(), null).IsReady);
    }
    public Task<FiscalTransaction> GetLastFiscalTransaction(string storeNumber, string terminalId)
    {
        return Task.Run(() => CommerceRuntimeManager.Runtime.Execute<GetLastFiscalTransactionResponse>(new GetLastFiscalTransactionRequest(), null).FiscalTransaction);
    }
    ```

    # <a name="retail-731"></a>[Retail 7.3.1](#tab/retail-7-3-1)

    > [!NOTE]
    > Bu adım, bu sürüm için geçerli değildir.

    # <a name="retail-732-and-later"></a>[Retail 7.3.2 ve sonrası](#tab/retail-7-3-2)

    > [!NOTE]
    > Bu adım, bu sürüm için geçerli değildir.

    # <a name="retail-735-and-later"></a>[Retail 7.3.5 ve sonrası](#tab/retail-7-3-5)

    > [!NOTE]
    > Bu adım, bu sürüm için geçerli değildir.

    # <a name="retail-811-and-later"></a>[Retail 8.1.1 ve sonrası](#tab/retail-8-1-1)

    > [!NOTE]
    > Bu adım, bu sürüm için geçerli değildir.

    ---

6. İstemci aracısının yeni RetailProxy derlemesini yüklemesini sağlamak için **dllhost.exe.config** dosyasını güncelleştirin.

    ``` xml
    <add key="RetailProxyAssemblyName" value="Contoso.Commerce.RetailProxy" />
    <add key="AdaptorCallerFullTypeName" value="Contoso.Commerce.RetailProxy.Adapters.AdaptorCaller" />
    ```

#### <a name="retail-proxy-extension-component-retail-731-and-later"></a>Retail ara sunucu uzantısı bileşeni (Retail 7.3.1 ve sonrası)

Aşağıdaki yordamı yalnızca Retail 7.3.1 ve sonraki sürümlerini kullanıyorsanız tamamlayın.

1. **RetailSDK\\SampleExtensions\\RetailProxy\\RetailProxy.Extensions.SalesTransactionSignatureSample** klasöründe **RetailServer.Extensions.SalesTransactionSignatureSample** projesini bulun ve derleyin.
2. **RetailProxy\\RetailProxy.Extensions.SalesTransactionSignatureSample\\bin\\Debug** klasöründe **Contoso.Commerce.RetailProxy.SalesTransactionSignatureSample** derleme dosyasını bulun.
3. Derleme dosyalarını yerel CRT istemci aracısı konumundaki **\\ext** klasörüne kopyalayın.
4. Retail ara sunucusu değişikliğini uzantı yapılandırma dosyasına kaydedin. Dosya, **RetailProxy.MPOSOffline.ext.config** olarak adlandırılmıştır ve yerel CRT istemci aracısı konumunda yer alır.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.RetailProxy.SalesTransactionSignatureSample" />
    ```

#### <a name="modern-pos-extension-components"></a>Modern POS uzantı bileşenleri

1. **RetailSdk\\POS\\ModernPOS.sln** kısmından çözümü açın ve çözümün hatasız şekilde derlenebildiğinden emin olun. Ayrıca, **Çalıştır** komutunu kullanarak Microsoft Visual Studio'dan Modern POS'u çalıştırabildiğinizden emin olun.

    > [!NOTE]
    > Modern POS özelleştirilmemelidir. Kullanıcı Hesabı Denetimi'ni (UAC) etkinleştirmeniz ve Modern POS'un önceden yüklenmiş olan örneklerini gerektiği gibi kaldırmanız gerekir.

2. Aşağıdaki mevcut kaynak kodu klasörlerini **Pos.Extensions** projesine dahil edin.

    # <a name="application-update-4"></a>[Uygulama güncelleştirmesi 4](#tab/app-update-4)

    - AuditEventExtensionSample
    - SalesTransactionSignatureSample

    # <a name="application-update-5-and-later"></a>[Uygulama güncelleştirmesi 5 ve sonrası](#tab/app-update-5-and-later)

    - AuditEventExtensionSample
    - SalesTransactionSignatureSample

    # <a name="retail-731"></a>[Retail 7.3.1](#tab/retail-7-3-1)

    - AuditEventExtensionSample
    - SalesTransactionSignatureSample

    # <a name="retail-732-and-later"></a>[Retail 7.3.2 ve sonrası](#tab/retail-7-3-2)

    - AuditEventExtensionSample
    - SalesTransactionSignatureSample
    - SalesTransactionSignatureNorway
    - SequentialSignature

    # <a name="retail-735-and-later"></a>[Retail 7.3.5 ve sonrası](#tab/retail-7-3-5)

    - SalesTransactionSignatureSample
    - SalesTransactionSignatureNorway
    - SequentialSignature

    # <a name="retail-811-and-later"></a>[Retail 8.1.1 ve sonrası](#tab/retail-8-1-1)

    - SalesTransactionSignatureSample
    - SalesTransactionSignatureNorway
    - SequentialSignature

    ---

3. Aşağıdaki klasörleri hariç tutma listesinden kaldırarak, **tsconfig.json** içinde derlenecek uzantıları etkinleştirin.

    # <a name="application-update-4"></a>[Uygulama güncelleştirmesi 4](#tab/app-update-4)

    - AuditEventExtensionSample
    - SalesTransactionSignatureSample

    # <a name="application-update-5-and-later"></a>[Uygulama güncelleştirmesi 5 ve sonrası](#tab/app-update-5-and-later)

    - AuditEventExtensionSample
    - SalesTransactionSignatureSample

    # <a name="retail-731"></a>[Retail 7.3.1](#tab/retail-7-3-1)

    - AuditEventExtensionSample
    - SalesTransactionSignatureSample

    # <a name="retail-732-and-later"></a>[Retail 7.3.2 ve sonrası](#tab/retail-7-3-2)

    - AuditEventExtensionSample
    - SalesTransactionSignatureSample
    - SalesTransactionSignatureNorway
    - SequentialSignature

    # <a name="retail-735-and-later"></a>[Retail 7.3.5 ve sonrası](#tab/retail-7-3-5)

    - SalesTransactionSignatureSample
    - SalesTransactionSignatureNorway
    - SequentialSignature

    # <a name="retail-811-and-later"></a>[Retail 8.1.1 ve sonrası](#tab/retail-8-1-1)

    - SalesTransactionSignatureSample
    - SalesTransactionSignatureNorway
    - SequentialSignature

    ---

4. Aşağıdaki satırları uygun yere ekleyerek, **extensions.json** dosyasında yüklenecek uzantıları etkinleştirin.

    # <a name="application-update-4"></a>[Uygulama güncelleştirmesi 4](#tab/app-update-4)

    ``` json
    {
        "baseUrl": "AuditEventExtensionSample"
    },
    {
        "baseUrl": "SalesTransactionSignatureSample"
    }
    ```

    # <a name="application-update-5-and-later"></a>[Uygulama güncelleştirmesi 5 ve sonrası](#tab/app-update-5-and-later)

    ``` json
    {
        "baseUrl": "AuditEventExtensionSample"
    },
    {
        "baseUrl": "SalesTransactionSignatureSample"
    }
    ```

    # <a name="retail-731"></a>[Retail 7.3.1](#tab/retail-7-3-1)

    ``` json
    {
        "baseUrl": "AuditEventExtensionSample"
    },
    {
        "baseUrl": "SalesTransactionSignatureSample"
    }
    ```

    # <a name="retail-732-and-later"></a>[Retail 7.3.2 ve sonrası](#tab/retail-7-3-2)

    ``` json
    {
        "baseUrl": "AuditEventExtensionSample"
    },
    {
        "baseUrl": "SalesTransactionSignatureSample"
    },
    {
        "baseUrl": "SalesTransactionSignatureNorway"
    },
    {
        "baseUrl": "SequentialSignature"
    }
    ```

    # <a name="retail-735-and-later"></a>[Retail 7.3.5 ve sonrası](#tab/retail-7-3-5)

    ``` json
    {
        "baseUrl": "Microsoft/AuditEvent.NO"
    },
    {
        "baseUrl": "SalesTransactionSignatureSample"
    },
    {
        "baseUrl": "SalesTransactionSignatureNorway"
    },
    {
        "baseUrl": "SequentialSignature"
    }
    ```

    # <a name="retail-811-and-later"></a>[Retail 8.1.1 ve sonrası](#tab/retail-8-1-1)

    ``` json
    {
        "baseUrl": "Microsoft/AuditEvent.NO"
    },
    {
        "baseUrl": "SalesTransactionSignatureSample"
    },
    {
        "baseUrl": "SalesTransactionSignatureNorway"
    },
    {
        "baseUrl": "SequentialSignature"
    }
    ```

    ---

    > [!NOTE]
    > Kaynak kodu klasörlerinin nasıl dahil edileceğini ve yüklenecek uzantıların nasıl etkinleştirileceğini gösteren örneklerle birlikte daha fazla bilgi için **Pos.Extensions** projesindeki readme.md dosyasındaki talimatlara bakın.

5. Çözümü yeniden oluşturun.
6. Hata ayıklayıcıda Modern POS'u çalıştırın ve işlevi sınayın.

### <a name="cloud-pos-extension-components"></a>Bulut POS uzantı bileşenleri

1. **RetailSdk\\POS\\CloudPOS.sln** kısmından çözümü açın ve çözümün hatasız şekilde derlenebildiğinden emin olun.
2. Aşağıdaki mevcut kaynak kodu klasörlerini **Pos.Extensions** projesine dahil edin.

    # <a name="application-update-4"></a>[Uygulama güncelleştirmesi 4](#tab/app-update-4)

    - AuditEventExtensionSample
    - SalesTransactionSignatureSample

    # <a name="application-update-5-and-later"></a>[Uygulama güncelleştirmesi 5 ve sonrası](#tab/app-update-5-and-later)

    - AuditEventExtensionSample
    - SalesTransactionSignatureSample

    # <a name="retail-731"></a>[Retail 7.3.1](#tab/retail-7-3-1)

    - AuditEventExtensionSample
    - SalesTransactionSignatureSample

    # <a name="retail-732-and-later"></a>[Retail 7.3.2 ve sonrası](#tab/retail-7-3-2)

    - AuditEventExtensionSample
    - SalesTransactionSignatureSample
    - SalesTransactionSignatureNorway
    - SequentialSignature

    # <a name="retail-735-and-later"></a>[Retail 7.3.5 ve sonrası](#tab/retail-7-3-5)

    - SalesTransactionSignatureSample
    - SalesTransactionSignatureNorway
    - SequentialSignature

    # <a name="retail-811-and-later"></a>[Retail 8.1.1 ve sonrası](#tab/retail-8-1-1)

    - SalesTransactionSignatureSample
    - SalesTransactionSignatureNorway
    - SequentialSignature

    ---

3. Aşağıdaki klasörleri hariç tutma listesinden kaldırarak, **tsconfig.json** içinde derlenecek uzantıları etkinleştirin.

    # <a name="application-update-4"></a>[Uygulama güncelleştirmesi 4](#tab/app-update-4)

    - AuditEventExtensionSample
    - SalesTransactionSignatureSample

    # <a name="application-update-5-and-later"></a>[Uygulama güncelleştirmesi 5 ve sonrası](#tab/app-update-5-and-later)

    - AuditEventExtensionSample
    - SalesTransactionSignatureSample

    # <a name="retail-731"></a>[Retail 7.3.1](#tab/retail-7-3-1)

    - AuditEventExtensionSample
    - SalesTransactionSignatureSample

    # <a name="retail-732-and-later"></a>[Retail 7.3.2 ve sonrası](#tab/retail-7-3-2)

    - AuditEventExtensionSample
    - SalesTransactionSignatureSample
    - SalesTransactionSignatureNorway
    - SequentialSignature

    # <a name="retail-735-and-later"></a>[Retail 7.3.5 ve sonrası](#tab/retail-7-3-5)

    - SalesTransactionSignatureSample
    - SalesTransactionSignatureNorway
    - SequentialSignature

    # <a name="retail-811-and-later"></a>[Retail 8.1.1 ve sonrası](#tab/retail-8-1-1)

    - SalesTransactionSignatureSample
    - SalesTransactionSignatureNorway
    - SequentialSignature

    ---

4. Aşağıdaki satırları uygun yere ekleyerek, **extensions.json** dosyasında yüklenecek uzantıları etkinleştirin.

    # <a name="application-update-4"></a>[Uygulama güncelleştirmesi 4](#tab/app-update-4)

    ``` json
    {
        "baseUrl": "AuditEventExtensionSample"
    },
    {
        "baseUrl": "SalesTransactionSignatureSample"
    }
    ```

    # <a name="application-update-5-and-later"></a>[Uygulama güncelleştirmesi 5 ve sonrası](#tab/app-update-5-and-later)

    ``` json
    {
        "baseUrl": "AuditEventExtensionSample"
    },
    {
        "baseUrl": "SalesTransactionSignatureSample"
    }
    ```

    # <a name="retail-731"></a>[Retail 7.3.1](#tab/retail-7-3-1)

    ``` json
    {
        "baseUrl": "AuditEventExtensionSample"
    },
    {
        "baseUrl": "SalesTransactionSignatureSample"
    }
    ```

    # <a name="retail-732-and-later"></a>[Retail 7.3.2 ve sonrası](#tab/retail-7-3-2)

    ``` json
    {
        "baseUrl": "AuditEventExtensionSample"
    },
    {
        "baseUrl": "SalesTransactionSignatureSample"
    },
    {
        "baseUrl": "SalesTransactionSignatureNorway"
    },
    {
        "baseUrl": "SequentialSignature"
    }
    ```

    # <a name="retail-735-and-later"></a>[Retail 7.3.5 ve sonrası](#tab/retail-7-3-5)

    ``` json
    {
        "baseUrl": "Microsoft/AuditEvent.NO"
    },
    {
        "baseUrl": "SalesTransactionSignatureSample"
    },
    {
        "baseUrl": "SalesTransactionSignatureNorway"
    },
    {
        "baseUrl": "SequentialSignature"
    }
    ```

    # <a name="retail-811-and-later"></a>[Retail 8.1.1 ve sonrası](#tab/retail-8-1-1)

    ``` json
    {
        "baseUrl": "Microsoft/AuditEvent.NO"
    },
    {
        "baseUrl": "SalesTransactionSignatureSample"
    },
    {
        "baseUrl": "SalesTransactionSignatureNorway"
    },
    {
        "baseUrl": "SequentialSignature"
    }
    ```

    ---

    > [!NOTE]
    > Kaynak kodu klasörlerinin nasıl dahil edileceğini ve yüklenecek uzantıların nasıl etkinleştirileceğini gösteren örneklerle birlikte daha fazla bilgi için **Pos.Extensions** projesindeki readme.md dosyasındaki talimatlara bakın.

5. Çözümü yeniden oluşturun.
6. **Çalıştır** komutunu kullanarak ve Retail SDK el kitabındaki adımları izleyerek çözümü çalıştırın.
7. İşlevi sınayın.

### <a name="set-up-required-parameters-in-headquarters"></a>Headquarters'da gerekli parametreleri ayarlama

Daha fazla bilgi için bkz. [Norway için yazar kasa işlevi](./emea-nor-cash-registers.md).

## <a name="production-environment"></a>Üretim ortamı

Commerce bileşenleri içeren dağıtılabilir paketler oluşturmak ve bu paketleri üretim ortamında uygulamak için aşağıdaki adımları izleyin.

1. Bu makalenin daha önceki [Bulut POS uzantı bileşenleri](#cloud-pos-extension-components) veya [Modern POS uzantı bileşenleri](#modern-pos-extension-components) bölümünde yer alan adımları tamamlayın.
2. **RetailSdk\\Assets** klasöründeki paket yapılandırma dosyalarında aşağıdaki değişiklikleri yapın:

    1. **commerceruntime.ext.config** ve **CommerceRuntime.MPOSOffline.Ext.config** yapılandırma dosyalarında, **composition** bölümüne aşağıdaki satırları ekleyin:

        # <a name="application-update-4"></a>[Uygulama güncelleştirmesi 4](#tab/app-update-4)

        ``` xml
        <add source="assembly" value="Contoso.Commerce.Runtime.ReceiptsNorway" />
        <add source="assembly" value="Contoso.Commerce.Runtime.RegisterAuditEventSample" />
        <add source="assembly" value="Contoso.Commerce.Runtime.SalesPaymentTransExt" />
        <add source="assembly" value="Contoso.Commerce.Runtime.SalesTransactionSignatureSample" />
        <add source="assembly" value="Contoso.Commerce.Runtime.XZReportsNorway" />
        ```

        # <a name="application-update-5-and-later"></a>[Uygulama güncelleştirmesi 5 ve sonrası](#tab/app-update-5-and-later)

        ``` xml
        <add source="assembly" value="Contoso.Commerce.Runtime.ReceiptsNorway" />
        <add source="assembly" value="Contoso.Commerce.Runtime.RegisterAuditEventSample" />
        <add source="assembly" value="Contoso.Commerce.Runtime.SalesPaymentTransExt" />
        <add source="assembly" value="Contoso.Commerce.Runtime.SalesTransactionSignatureSample" />
        <add source="assembly" value="Contoso.Commerce.Runtime.SalesTransactionSignatureSample.Messages" />
        <add source="assembly" value="Contoso.Commerce.Runtime.XZReportsNorway" />
        ```

        # <a name="retail-731"></a>[Retail 7.3.1](#tab/retail-7-3-1)

        ``` xml
        <add source="assembly" value="Contoso.Commerce.Runtime.ReceiptsNorway" />
        <add source="assembly" value="Contoso.Commerce.Runtime.RegisterAuditEventSample" />
        <add source="assembly" value="Contoso.Commerce.Runtime.SalesPaymentTransExt" />
        <add source="assembly" value="Contoso.Commerce.Runtime.SalesTransactionSignatureSample" />
        <add source="assembly" value="Contoso.Commerce.Runtime.XZReportsNorway" />
        ```

        # <a name="retail-732-and-later"></a>[Retail 7.3.2 ve sonrası](#tab/retail-7-3-2)

        ``` xml
        <add source="assembly" value="Contoso.Commerce.Runtime.ReceiptsNorway" />
        <add source="assembly" value="Contoso.Commerce.Runtime.RegisterAuditEventSample" />
        <add source="assembly" value="Contoso.Commerce.Runtime.SalesPaymentTransExt" />
        <add source="assembly" value="Contoso.Commerce.Runtime.SalesPaymentTransExtNorway" />
        <add source="assembly" value="Contoso.Commerce.Runtime.SequentialSignatureRegister" />
        <add source="assembly" value="Contoso.Commerce.Runtime.SalesTransactionSignatureNorway" />
        <add source="assembly" value="Contoso.Commerce.Runtime.XZReportsNorway" />
        ```

        # <a name="retail-735-and-later"></a>[Retail 7.3.5 ve sonrası](#tab/retail-7-3-5)

        ``` xml
        <add source="assembly" value="Microsoft.Dynamics.Commerce.Runtime.RegisterAuditEventNorway" />
        <add source="assembly" value="Contoso.Commerce.Runtime.ReceiptsNorway" />
        <add source="assembly" value="Contoso.Commerce.Runtime.RegisterAuditEventSample" />
        <add source="assembly" value="Contoso.Commerce.Runtime.SalesPaymentTransExt" />
        <add source="assembly" value="Contoso.Commerce.Runtime.SalesPaymentTransExtNorway" />
        <add source="assembly" value="Contoso.Commerce.Runtime.SequentialSignatureRegister" />
        <add source="assembly" value="Contoso.Commerce.Runtime.SalesTransactionSignatureNorway" />
        <add source="assembly" value="Contoso.Commerce.Runtime.XZReportsNorway" />
        ```

        # <a name="retail-811-and-later"></a>[Retail 8.1.1 ve sonrası](#tab/retail-8-1-1)

        ``` xml
        <add source="assembly" value="Microsoft.Dynamics.Commerce.Runtime.RegisterAuditEventNorway" />
        <add source="assembly" value="Contoso.Commerce.Runtime.ReceiptsNorway" />
        <add source="assembly" value="Contoso.Commerce.Runtime.SalesPaymentTransExt" />
        <add source="assembly" value="Contoso.Commerce.Runtime.SalesPaymentTransExtNorway" />
        <add source="assembly" value="Contoso.Commerce.Runtime.SequentialSignatureRegister" />
        <add source="assembly" value="Contoso.Commerce.Runtime.SalesTransactionSignatureNorway" />
        <add source="assembly" value="Contoso.Commerce.Runtime.XZReportsNorway" />
        ```

        ---

    2. Commerce ara sunucu özelleştirmesini etkinleştirin:

        # <a name="application-update-4"></a>[Uygulama güncelleştirmesi 4](#tab/app-update-4)

        **dllhost.exe.config** yapılandırma dosyasında, **configuration** bölümünün **appSettings** alt bölümüne aşağıdaki satırları ekleyin.

        ``` xml
        <add key="RetailProxyAssemblyName" value="Contoso.Commerce.RetailProxy"/>
        <add key="AdaptorCallerFullTypeName" value ="Contoso.Commerce.RetailProxy.Adapters.AdaptorCaller"/>
        ```

        # <a name="application-update-5-and-later"></a>[Uygulama güncelleştirmesi 5 ve sonrası](#tab/app-update-5-and-later)

        **dllhost.exe.config** yapılandırma dosyasında, **configuration** bölümünün **appSettings** alt bölümüne aşağıdaki satırları ekleyin.

        ``` xml
        <add key="RetailProxyAssemblyName" value="Contoso.Commerce.RetailProxy"/>
        <add key="AdaptorCallerFullTypeName" value ="Contoso.Commerce.RetailProxy.Adapters.AdaptorCaller"/>
        ```

        # <a name="retail-731"></a>[Retail 7.3.1](#tab/retail-7-3-1)

        **RetailProxy.MPOSOffline.ext.config** yapılandırma dosyasında, **composition** bölümüne aşağıdaki satırları ekleyin:

        ``` xml
        <add source="assembly" value="Contoso.Commerce.RetailProxy.SalesTransactionSignatureSample" />
        ```

        # <a name="retail-732-and-later"></a>[Retail 7.3.2 ve sonrası](#tab/retail-7-3-2)

        **RetailProxy.MPOSOffline.ext.config** yapılandırma dosyasında, **composition** bölümüne aşağıdaki satırları ekleyin:

        ``` xml
        <add source="assembly" value="Contoso.Commerce.RetailProxy.SalesTransactionSignatureSample" />
        ```

        # <a name="retail-735-and-later"></a>[Retail 7.3.5 ve sonrası](#tab/retail-7-3-5)

        **RetailProxy.MPOSOffline.ext.config** yapılandırma dosyasında, **composition** bölümüne aşağıdaki satırları ekleyin:

        ``` xml
        <add source="assembly" value="Contoso.Commerce.RetailProxy.SalesTransactionSignatureSample" />
        ```

        # <a name="retail-811-and-later"></a>[Retail 8.1.1 ve sonrası](#tab/retail-8-1-1)

        **RetailProxy.MPOSOffline.ext.config** yapılandırma dosyasında, **composition** bölümüne aşağıdaki satırları ekleyin:

        ``` xml
        <add source="assembly" value="Contoso.Commerce.RetailProxy.SalesTransactionSignatureSample" />
        ```

        ---

3. **Customization.settings** paket özelleştirme yapılandırma dosyasında aşağıdaki değişiklikleri yapın:

    1. Retail ara sunucu özelleştirmesini etkinleştirin.

        # <a name="application-update-4"></a>[Uygulama güncelleştirmesi 4](#tab/app-update-4)

        **&lt;ItemGroup Condition="'@(RetailServerLibraryPathForProxyGeneration)' == ''"&gt;** bölümüne aşağıdaki satırları ekleyin.

        ``` xml
        <RetailServerLibraryPathForProxyGeneration Include="$(SdkReferencesPath)\Contoso.RetailServer.SalesTransactionSignatureSample.dll"/>
        ```

        # <a name="application-update-5-and-later"></a>[Uygulama güncelleştirmesi 5 ve sonrası](#tab/app-update-5-and-later)

        **&lt;ItemGroup Condition="'@(RetailServerLibraryPathForProxyGeneration)' == ''"&gt;** bölümüne aşağıdaki satırları ekleyin.

        ``` xml
        <RetailServerLibraryPathForProxyGeneration Include="$(SdkReferencesPath)\Contoso.RetailServer.SalesTransactionSignatureSample.dll"/>
        ```

        # <a name="retail-731"></a>[Retail 7.3.1](#tab/retail-7-3-1)

        Dağıtılabilir paketleri Retail ara sunucu uzantısına dahil etmek için **ItemGroup** bölümüne aşağıdaki satırları ekleyin:

        ``` xml
        <ISV_RetailProxy_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.RetailProxy.SalesTransactionSignatureSample.dll" />
        ```

        # <a name="retail-732-and-later"></a>[Retail 7.3.2 ve sonrası](#tab/retail-7-3-2)

        Dağıtılabilir paketleri Retail ara sunucu uzantısına dahil etmek için **ItemGroup** bölümüne aşağıdaki satırları ekleyin:

        ``` xml
        <ISV_RetailProxy_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.RetailProxy.SalesTransactionSignatureSample.dll" />
        ```

        # <a name="retail-735-and-later"></a>[Retail 7.3.5 ve sonrası](#tab/retail-7-3-5)

        Dağıtılabilir paketleri Retail ara sunucu uzantısına dahil etmek için **ItemGroup** bölümüne aşağıdaki satırları ekleyin:

        ``` xml
        <ISV_RetailProxy_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.RetailProxy.SalesTransactionSignatureSample.dll" />
        ```

        # <a name="retail-811-and-later"></a>[Retail 8.1.1 ve sonrası](#tab/retail-8-1-1)

        Dağıtılabilir paketleri Retail ara sunucu uzantısına dahil etmek için **ItemGroup** bölümüne aşağıdaki satırları ekleyin:

        ``` xml
        <ISV_RetailProxy_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.RetailProxy.SalesTransactionSignatureSample.dll" />
        ```

        ---

    2. Dağıtılabilir paketleri CRT uzantılarına dahil etmek için **ItemGroup** bölümüne aşağıdaki satırları ekleyin:

        # <a name="application-update-4"></a>[Uygulama güncelleştirmesi 4](#tab/app-update-4)

        ``` xml
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.ReceiptsNorway.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.RegisterAuditEventSample.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesPaymentTransExt.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll.config" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.XZReportsNorway.dll" />
        ```

        # <a name="application-update-5-and-later"></a>[Uygulama güncelleştirmesi 5 ve sonrası](#tab/app-update-5-and-later)

        ``` xml
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.ReceiptsNorway.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.RegisterAuditEventSample.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesPaymentTransExt.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll.config" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesTransactionSignatureSample.Messages.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.XZReportsNorway.dll" />
        ```

        # <a name="retail-731"></a>[Retail 7.3.1](#tab/retail-7-3-1)

        ``` xml
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.ReceiptsNorway.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.RegisterAuditEventSample.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesPaymentTransExt.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll.config" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SequentialSignatureRegister.Contracts.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.XZReportsNorway.dll" />
        ```

        # <a name="retail-732-and-later"></a>[Retail 7.3.2 ve sonrası](#tab/retail-7-3-2)

        ``` xml
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.ReceiptsNorway.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.RegisterAuditEventSample.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesPaymentTransExt.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesPaymentTransExtNorway.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SequentialSignatureRegister.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesTransactionSignatureNorway.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SequentialSignatureRegister.dll.config" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SequentialSignatureRegister.Contracts.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.XZReportsNorway.dll" />
        ```

        # <a name="retail-735-and-later"></a>[Retail 7.3.5 ve sonrası](#tab/retail-7-3-5)

        ``` xml
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.ReceiptsNorway.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesPaymentTransExt.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesPaymentTransExtNorway.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SequentialSignatureRegister.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesTransactionSignatureNorway.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SequentialSignatureRegister.dll.config" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SequentialSignatureRegister.Contracts.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.XZReportsNorway.dll" />
        ```

        # <a name="retail-811-and-later"></a>[Retail 8.1.1 ve sonrası](#tab/retail-8-1-1)

        ``` xml
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.ReceiptsNorway.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesPaymentTransExt.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesPaymentTransExtNorway.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SequentialSignatureRegister.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesTransactionSignatureNorway.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SequentialSignatureRegister.dll.config" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SequentialSignatureRegister.Contracts.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.XZReportsNorway.dll" />
        ```

        ---

    3. Dağıtılabilir paketleri Retail Server uzantısına dahil etmek için **ItemGroup** bölümüne aşağıdaki satırları ekleyin:

        # <a name="application-update-4"></a>[Uygulama güncelleştirmesi 4](#tab/app-update-4)

        ``` xml
        <ISV_RetailServer_CustomizableFile Include="$(SdkReferencesPath)\Contoso.RetailServer.SalesTransactionSignatureSample.dll" />
        <ISV_RetailServer_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll" />
        <ISV_RetailServer_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll.config" />
        ```

        # <a name="application-update-5-and-later"></a>[Uygulama güncelleştirmesi 5 ve sonrası](#tab/app-update-5-and-later)

        ``` xml
        <ISV_RetailServer_CustomizableFile Include="$(SdkReferencesPath)\Contoso.RetailServer.SalesTransactionSignatureSample.dll" />
        <ISV_RetailServer_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesTransactionSignatureSample.Messages.dll" />
        ```

        # <a name="retail-731"></a>[Retail 7.3.1](#tab/retail-7-3-1)

        ``` xml
        <ISV_RetailServer_CustomizableFile Include="$(SdkReferencesPath)\Contoso.RetailServer.SalesTransactionSignatureSample.dll" />
        ```

        # <a name="retail-732-and-later"></a>[Retail 7.3.2 ve sonrası](#tab/retail-7-3-2)

        ``` xml
        <ISV_RetailServer_CustomizableFile Include="$(SdkReferencesPath)\Contoso.RetailServer.SalesTransactionSignatureSample.dll" />
        ```

        # <a name="retail-735-and-later"></a>[Retail 7.3.5 ve sonrası](#tab/retail-7-3-5)

        ``` xml
        <ISV_RetailServer_CustomizableFile Include="$(SdkReferencesPath)\Contoso.RetailServer.SalesTransactionSignatureSample.dll" />
        ```

        # <a name="retail-811-and-later"></a>[Retail 8.1.1 ve sonrası](#tab/retail-8-1-1)

        ``` xml
        <ISV_RetailServer_CustomizableFile Include="$(SdkReferencesPath)\Contoso.RetailServer.SalesTransactionSignatureSample.dll" />
        ```

        ---

4. Norveç'e yönelik kaynak dosyalarını dağıtılabilir paketlere dahil etmek için aşağıdaki dosyaları değiştirin:
    - Packages\_SharedPackagingProjectComponents\Sdk.ModernPos.Shared.csproj
    - Packages\RetailServer\Sdk.RetailServerSetup.proj
  
  - **Sdk.ModernPos.Shared.csproj** dosyası için 
    - **ItemGroup** bölümüne satır ekleyin
    
        ``` xml
        <<File_name> Include="$(SdkReferencesPath)\nb-NO\*" />
        ```
    > [!Note]
    > <File_name> yerine kaynak dosyası için bir ad belirtin. Aynı durum, aşağıda verilen diğer örnekler için de geçerlidir.
 
    - **Target Name="CopyPackageFiles"** bölümüne satır ekleyin
       ``` xml
        <Copy SourceFiles="@(<File_name>)" DestinationFolder="$(OutputPath)content.folder\CustomizedFiles\ClientBroker\ext\nb-NO" SkipUnchangedFiles="true" />
        ```
  
  - **Sdk.RetailServerSetup.proj** dosyası için 
    - **ItemGroup** bölümüne satır ekleyin
        ``` xml
        <<File_name> Include="$(SdkReferencesPath)\nb-NO\*" />
        ```    
    - **Target Name="CopyPackageFiles"** bölümüne satır ekleyin
         ``` xml
        <Copy SourceFiles="@(<File_name>)" DestinationFolder="$(OutputPath)content.folder\RetailServer\Code\bin\ext\nb-NO" SkipUnchangedFiles="true" />
        ```    

5. Satış hareketlerini imzalamak için kullanılması gereken sertifikanın parmak izini, mağaza konumunu ve mağaza adını belirterek sertifikanın yapılandırma dosyasını değiştirin. Ardından yapılandırma dosyasını **References** klasörüne kopyalayın.

    # <a name="application-update-4"></a>[Uygulama güncelleştirmesi 4](#tab/app-update-4)

    Dosya, **Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll.config** olarak adlandırılmıştır ve **CommerceRuntime\\Extensions.SalesTransactionSignatureSample\\bin\\Debug** klasöründe yer alır.

    # <a name="application-update-5-and-later"></a>[Uygulama güncelleştirmesi 5 ve sonrası](#tab/app-update-5-and-later)

    Dosya, **Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll.config** olarak adlandırılmıştır ve **CommerceRuntime\\Extensions.SalesTransactionSignatureSample\\bin\\Debug** klasöründe yer alır.

    # <a name="retail-731"></a>[Retail 7.3.1](#tab/retail-7-3-1)

    Dosya, **Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll.config** olarak adlandırılmıştır ve **CommerceRuntime\\Extensions.SalesTransactionSignatureSample\\bin\\Debug** klasöründe yer alır.

    # <a name="retail-732-and-later"></a>[Retail 7.3.2 ve sonrası](#tab/retail-7-3-2)

    Dosya, **Contoso.Commerce.Runtime.SequentialSignatureRegister.dll.config** olarak adlandırılmıştır ve **Extensions.SequentialSignatureRegister\\bin\\Debug** klasöründe yer alır.

    # <a name="retail-735-and-later"></a>[Retail 7.3.5 ve sonrası](#tab/retail-7-3-5)

    Dosya, **Contoso.Commerce.Runtime.SequentialSignatureRegister.dll.config** olarak adlandırılmıştır ve **Extensions.SequentialSignatureRegister\\bin\\Debug** klasöründe yer alır.

    # <a name="retail-811-and-later"></a>[Retail 8.1.1 ve sonrası](#tab/retail-8-1-1)

    Dosya, **Contoso.Commerce.Runtime.SequentialSignatureRegister.dll.config** olarak adlandırılmıştır ve **Extensions.SequentialSignatureRegister\\bin\\Debug** klasöründe yer alır.

    ---

6. Retail Server yapılandırma dosyasını güncelleştirin. **RetailSDK\\Packages\\RetailServer\\Code\\web.config** dosyasında, **extensionComposition** bölümüne aşağıdaki satırları ekleyin.

    ``` xml
    <add source="assembly" value="Contoso.RetailServer.SalesTransactionSignatureSample" />
    ```

7. Dağıtılabilir paketler oluşturmak üzere tüm Retail SDK için **msbuild**'i çalıştırın.
8. Paketleri Microsoft Dynamics Lifecycle Services (LCS) aracılığıyla veya el ile uygulayın. Daha fazla bilgi için bkz. [Dağıtılabilir paketler oluşturma](../dev-itpro/retail-sdk/retail-sdk-packaging.md).

### <a name="enable-the-digital-signature-in-offline-mode-for-modern-pos"></a>Modern POS için çevrimdışı modda dijital imzayı etkinleştirme

Modern POS'un çevrimdışı modunda dijital imzayı etkinleştirmek için, yeni bir cihazda Modern POS'u etkinleştirdikten sonra aşağıdaki adımları izlemeniz gerekir.

1. POS'de oturum açın
2. **Veritabanı bağlantı durumu** sayfasında, çevrimdışı veritabanının tamamen eşitlendiğinden emin olun. **Bekleyen indirmeler** alanının değeri **0** (zero) olduğunda veritabanı tamamen eşitlenmiş demektir.
3. POS oturumunu kapatın.
4. Çevrimdışı veritabanının tamamen eşitlenmesi için bir süre bekleyin.
5. POS'de oturum açın
6. **Veritabanı bağlantı durumu** sayfasında, çevrimdışı veritabanının tamamen eşitlendiğinden emin olun. **Çevrimdışı veritabanında bekleyen hareketler** alanının değeri **0** (zero) olduğunda veritabanı tamamen eşitlenmiş demektir.
7. Modern POS'u yeniden başlatın.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
