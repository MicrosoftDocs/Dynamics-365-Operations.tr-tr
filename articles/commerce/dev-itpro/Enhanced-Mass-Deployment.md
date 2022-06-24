---
title: Mühürlü Commerce self servis bileşenlerinin toplu dağıtımı
description: Bu makale, dağıtımların sessizce yüklenmesi ve dağıtımlara hizmet sunulması için self servis bileşen yükleyicileri altyapısının nasıl kullanıldığını açıklamaktadır.
author: jashanno
ms.date: 05/11/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: jashanno
ms.search.validFrom: 2021-04-30
ms.openlocfilehash: a679d78db3ad5bd9cccbd4ab6a7026bd07890f55
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8898591"
---
# <a name="mass-deployment-of-sealed-commerce-self-service-components"></a>Mühürlü Commerce self servis bileşenlerinin toplu dağıtımı

[!include [banner](../includes/banner.md)]

Bu makale, mühürlü altyapı, 10.0.18 sürümünden başlayarak her ay yayınlanan bileşen yükleyicileri ve Microsoft Dynamics Lifecycle Services'taki (LCS) paylaşılan varlık kitaplığında kullanılabilir hale getirilen bileşen yükleyicileri için geçerlidir. Bu yeni yükleyicilerin ilk birkaç sürümünün **(Önizleme)** olarak tanımlandığını unutmayın. Ancak bu tanımlamanın tek amacı, Microsoft yeni yükleyicileri kullanmak için ek işlevsel gereksinimler olup olmadığını belirlerken bu yükleyicilerin ayırt edilmesini sağlamaktır. Bu, yükleyicilerin üretim için geçerli olmadığı anlamına gelmez. Microsoft, bu yeni yükleyicilerin yayınlanmasıyla ilgili olarak, Ekim 2023'te veya bu tarih civarında eski yükleyicileri kullanımdan kaldırmayı planlamaktadır. 

Bu makale, komut satırı bağımsız değişkenleriyle sessiz yükleme ve hizmet sunma güncelleştirmeleri gerçekleştirmek için yeni yükleyicilerin nasıl kullanılacağını açıklamaktadır. Bu bağımsız değişkenler, birçok farklı yolla toplu dağıtım yapmanızı sağlar.

> [!NOTE]
> Yeni self servis, mühürlü yükleyiciler Headquarters'dan edinilemeyecek ve yalnızca LCS aracılığıyla indirilebilir

## <a name="delimiters-for-mass-deployment"></a>Toplu dağıtım sınırlayıcıları

Aşağıdaki tablo, komut satırı yürütmesinde kullanılabilecek sınırlayıcıları gösterir.


| Ayırıcı                 | Açıklama |
|---------------------------|-------------|
| --AadTokenIssuerPrefix | Microsoft Azure Active Directory (Azure AD) belirteci veren için önek. |
| --AsyncClientAadClientId | Headquarters ile iletişim sırasında Async Client'ın kullanması gereken Azure AD istemci kimliği. |
| --AsyncClientAppInsightsInstrumentationKey | Async Client AppInsights izleme anahtarı. |
| --AsyncClientCertFullPath | Headquarters iletişimlerinde Azure AD ile kimlik doğrulaması yapmak üzere kullanılması gereken Async Client kimlik sertifikası konumunun arama ölçümü olarak parmak izini kullanan tam biçimlendirilmiş URN yolu. Örneğin, `store://My/LocalMachine?FindByThumbprint=<MyThumbprint>` doğru biçimlendirilmiş bir URN'dir. **\<MyThumbprint\>** değeri, kullanılacak sertifika parmak izi ile değiştirilir. **-AsyncClientCertThumbprint** parametresi ile birlikte bu parametreyi kullanmayın. |
| --AsyncClientCertThumbprint | Headquarters iletişimlerinde Azure AD ile kimlik doğrulaması yapmak üzere kullanılması gereken Async Client kimlik sertifikasının parmak izi. Bu parmak izi, kullanılacak doğru sertifikayı bulmak için **LocalMachine/My store** konumunda ve adında arama yapmak amacıyla kullanılacaktır. **-AsyncClientCertFullPath** parametresi ile birlikte bu parametreyi kullanmayın. |
| --ClientAppInsightsInstrumentationKey | İstemci AppInsights izleme anahtarı. |
| --CloudPosAppInsightsInstrumentationKey | Cloud POS AppInsights izleme anahtarı. |
| --Config | Yükleme sırasında kullanılması gereken yapılandırma dosyası. **Contoso.CommerceScaleUnit.xml**, bir dosya adı örneğidir. |
| --CposAadClientId | Cloud POS'un cihaz etkinleştirme sırasında kullanması gereken Azure AD istemci kimliği. Bu parametre, şirket içi dağıtımlar için gerekli değildir. |
| --Device | Headquarters'da **Cihazlar** sayfasında gösterilen cihaz kimliği. |
| --EnvironmentId | Ortam kimliği. |
| --HardwareStationAppInsightsInstrumentationKey | Hardware Station AppInsights izleme anahtarı. |
| --Install | Bu yükleyicinin sağladığı bileşenin yüklenip yüklenmeyeceğini belirten bir parametre. Bu parametre zorunlu değildir. |
| --InstallOffline | Modern POS için bu parametre, çevrimdışı veritabanının da yüklenip yapılandırılacağını belirtir. **-SQLServerName** parametresini de kullanın. Aksi durumda yükleyici, önkoşullara uyan varsayılan bir örneği bulmaya çalışır. |
| --Port | Retail Server sanal dizini ile ilişkilendirilmesi ve tarafından kullanılması gereken bağlantı noktası. Bağlantı noktası ayarlanmamışsa 443 numaralı varsayılan bağlantı noktası kullanılır. |
| --Register | Headquarters'da **Kayıtlar** sayfasında gösterilen kayıt kimliği. |
| --RetailServerAadClientId | Headquarters ile iletişim sırasında Retail Server'ın kullanması gereken Azure AD istemci kimliği. |
| --RetailServerAadResourceId | Cihaz etkinleştirme sırasında kullanılması gereken Retail Server Azure AD uygulaması kaynak kodu. Bu parametre, şirket içi dağıtımlar için gerekli değildir. |
| --RetailServerCertFullPath | Headquarters ile iletişimlerde Azure AD ile kimlik doğrulaması için kullanılması gereken Retail Server kimlik sertifikasının arama ölçümü olarak parmak izini kullanan tam biçimlendirilmiş URN yolu. Örneğin, `store://My/LocalMachine?FindByThumbprint=<MyThumbprint>` doğru biçimlendirilmiş bir URN olup **\<MyThumbprint\>** değeri, kullanılması gereken sertifika parmak izi ile değiştirilir. **-RetailServerCertThumbprint** parametresi ile birlikte bu parametreyi kullanmayın. |
| --RetailServerCertThumbprint | Headquarters ile iletişimler için Azure AD ile kimlik doğrulaması yapmak üzere kullanılması gereken Retail Server kimlik sertifikasının parmak izi. Bu parmak izi, kullanılacak doğru sertifikayı bulmak için **LocalMachine/My store** mağaza konumunda ve adında arama yapmak amacıyla kullanılacaktır. **-RetailServerCertFullPath** parametresi ile birlikte bu parametreyi kullanmayın. |
| --RetailServerURL | Yükleyicinin kullanması gereken Retail Server URL'si. (Bu URL, Commerce Scale Unit \[CSU\] URL'si olarak da bilinir.) Modern POS için bu değer, cihaz etkinleştirme sırasında kullanılır. |
| --SkipAadCredentialsCheck| Azure AD kimlik bilgileri önkoşul denetimlerinin atlanıp atlanmayacağını belirten anahtar. Varsayılan değer **yanlış** değeridir. |
| --SkipCertCheck | Sertifika önkoşul denetimlerinin atlanıp atlanmayacağını belirten anahtar. Varsayılan değer **yanlış** değeridir. |
| --SkipIisCheck | Internet Information Services (IIS) önkoşul denetimlerinin atlanıp atlanmayacağını belirten anahtar. Varsayılan değer **yanlış** değeridir. |
| --SkipNetFrameworkCheck | .NET Framework önkoşul denetimlerinin atlanıp atlanmayacağını belirten anahtar. Varsayılan değer **yanlış** değeridir. |
| --SkipScaleUnitHealthcheck | Yüklü bileşenlerdeki sistem durumu denetiminin atlanması gerekip gerekmediğini belirten bir anahtar. Varsayılan değer **yanlış** değeridir. |
| --SkipSChannelCheck | Güvenli kanal önkoşul denetimlerinin atlanıp atlanmayacağını belirten anahtar. Varsayılan değer **yanlış** değeridir. |
| --SkipSqlFullTextCheck | Tam metin araması gerektiren SQL Server önkoşul doğrulamasının atlanıp atlanmayacağını belirten bir anahtar. Varsayılan değer **yanlış** değeridir. |
| --SkipSqlServerCheck | SQL Server önkoşul denetimlerinin atlanıp atlanmayacağını belirten anahtar. Varsayılan değer **yanlış** değeridir. |
| --SqlServerName | SQL Server adı. Ad belirtilmezse yükleyici, varsayılan örneği bulmaya çalışır. |
| --SslcertFullPath | Ölçek birimine HTTP trafiğini şifrelemek için kullanılması gereken sertifika konumunun arama ölçümü olarak izi kullanan tam biçimlendirilmiş URN yolu. Örneğin, `store:\/\/My\/LocalMachine\?FindByThumbprint\=\<MyThumbprint\>` doğru biçimlendirilmiş bir URN olup **\<MyThumbprint\>** değeri, kullanılması gereken sertifika parmak izi ile değiştirilir. **-SslCertThumbprint** parametresi ile birlikte bu parametreyi kullanmayın. |
| --SslCertThumbprint | HTTP trafiğini ölçek birimine şifrelemek için kullanılması gereken sertifikanın parmak izi. Bu parmak izi, kullanılacak doğru sertifikayı bulmak için **LocalMachine/My store** konumunda ve adında arama yapmak amacıyla kullanılacaktır. **-SslCertFullPath** parametresi ile birlikte bu parametreyi kullanmayın. |
| --StoreSystemAosUrl | Headquarters (AOS) URL'si. |
| --StoreSystemChannelDatabaseId | Kanal veritabanı kodu (ad). |
| --TenantId | Azure AD kiracı kodu. |
| --TransactionServiceAzureAuthority | Transaction Service Azure AD yetkilisi. |
| --TransactionServiceAzureResource | Transaction Service Azure AD kaynağı. |
| --TrustSqlServerCertificate | SQL Server'a bağlantı kurulurken sunucu sertifikasının güvenilir olup olmayacağını belirten anahtar. Güvenlik risklerini önlemenize yardımcı olmak için, üretim dağıtımlarında hiçbir zaman **doğru** değeri sağlanmamalıdır. Varsayılan değer **yanlış** değeridir. |
| --Verbosity | Yükleme sırasında istenen günlük düzeyi. Genellikle, bu değer kullanılmamalıdır. |
| --WindowsPhoneAppInsightsInstrumentationKey | Hardware Station AppInsights izleme anahtarı. |

## <a name="general-overview"></a>Genel bakış

Self servis yükleyicileri için yeni çerçeve çeşitli özelliklere ve gelişmelere sahiptir. Yeni çerçeve şu anda yalnızca Modern POS, hardware station ve CSU (şirket içinde barındırılan) için yükleyicileri oluşturur. Mühürlenmiş yükleyicilerin, aşağıdaki örnekte kullanılanlara benzer şekilde görünen temel komut satırı kullanımını anlamanız önemlidir. 
 
```Console
<Component Installer Name>.exe install --<Parameter Name> "<Parameter Information>"
```

Yükleyici **install** (veya yüklemeyi kaldırmak için **uninstall**) parametresini ve o yüklemeye özel parametreleri gerektirir. **Parameter Name**, kayıt, CSU URL'si veya sertifika bilgileri gibi gerekli parametreleri içermelidir. **Parameter Information**, parametrelerle ilgili ek bilgiler içermelidir.

Mühürlenmiş çerçeve, aşağıdaki değişiklikleri sağlamak için oluşturuldu:
- **Mühürlü** – Yeni yükleyici çerçevesi, Microsoft tarafından dağıtılan temel bileşen yükleyicilerini genişletilebilirlik tabanlı özelleştirmelerinden tümüyle ayırır. Özelleştirmeler daha sonra yüklenecektir, ancak daha sonra güncelleştirmelere ilişkin bağlantısı kesilecektir (böylece güncelleştirmelere yalnızca Microsoft temel bileşeni için, yalnızca özelleştirmeler için veya her ikisi için de izin verilir).
- **Grafik kullanıcı arabirimi yok** – Artık bir kullanıcı arabirimi (UI) yoktur. Bunun yerine, her bileşen yükleyicisi için tümüyle komut satırı kullanan yürütülebilir dosya vardır. Bu değişiklik, yeni yükleyici çerçevesini toplu dağıtımla kullanmak üzere odaklamak için kullanılan anahtar değişikliklerden veya özelliklerden biridir.
- **Daha derin günlük kaydı** – Geliştirilmiş yükleyici günlükleri, yüklemenin tamamlanmasını veya başarısızlığını, gerçekleştirilen adımları ve oluşturulan tüm uyarıları veya hataları daha iyi doğrulamaya olanak sağlar.
- **Temizlik** – Yeni çerçevede bileşen yükleyicileri, daha yeni bileşenleri yüklemeden önce bileşen klasörünün tüm içeriğini temizleyerek, yükleme dizinlerinin temizlenmesini korumak için daha çok çalışır. Bu temizleme, soruna neden olabilecek ve yüklemenin başarılı olmasını engelleyebilecek kalan dosyalar olmamasını sağlar.

Üç bileşen yeni çerçeveye taşınmadı: Sanal Çevre Birimi Benzeticisi, Async Server Connector Service (Dynamics AX 2012 R3 desteği için kullanılır) ve Real-time Service Replacement (Dynamics AX 2012 R3 desteği için kullanılır).

> [!NOTE]
> Yükleyiciler yerel olarak depolanır ve tutulur.  Disk alanını boşa harcamamak için, tutulan yükleyicileri zaman içinde yönetmek veya silmek önemlidir. Ana bileşenlerin mevcut yükleyicisini ve en son sürümlerin uzantı yükleyicilerini olağanüstü durumlardan korunma amaçlarıyla saklamanız önerilir.

## <a name="migration"></a>Geçiş

Eski self-servis çerçeve bileşeni yükleyicilerinden yeni çerçeve bileşeni yükleyicilerine geçiş eski bileşenlerin kaldırılmasını gerektirir.

- **Modern POS** – Yeni yükleyici çerçevesi uygulamanın yeni bir uygulama imza kodu almasına neden oldu. Bu nedenle, yeni çerçeve Modern POS bileşeni yüklenmeden önce eski bileşenlerin tam olarak kaldırılması gerekir. Tam kaldırma gereksiniminden dolayı, cihaz etkinleştirme işlemi yeniden gerekecektir. (Bu cihaz yeniden etkinleştirme işlemi bir kerelik bir gereksinim olduğundan, kaldırma işlemi tekrar gerçekleşmeyebilir.)
- **Hardware station** – Bir IIS web sitesi olarak yeni yükleyici çerçevesi, temel klasör yapısının düzeltilmesini gerektirir. Bu nedenle, yeni çerçeve hardware station bileşeni yüklenmeden önce eski bileşenlerin tam olarak kaldırılması gerekir.
- **Commerce Scale Unit (CSU, şirket içinde barındırılan)** – Bir dizi IIS web sitesi olarak yeni yükleyici çerçevesi, temel klasör yapısının düzeltilmesini gerektirir.  Bu nedenle, yeni çerçeve CSU (şirket içinde barındırılan) bileşeni yüklenmeden önce eski bileşenlerin tam olarak kaldırılması gerekir.

## <a name="modern-pos"></a>Modern POS

### <a name="before-you-begin"></a>Başlamadan önce

Eski, self-servis Modern POS bileşenini kaldırmanız kritik önem taşır. Daha fazla bilgi için bu makalenin önceki kısımlarında yer alan geçiş adımlarına bakın.

### <a name="examples-of-silent-deployment"></a>Sessiz dağıtım örnekleri

Bu bölüm, Modern POS'u yüklemek için kullanılan komutların örneklerini gösterir.

#### <a name="silently-install-modern-pos"></a>Modern POS'u sessizce yükleme

Aşağıdaki komut, Modern POS'u sessizce yükler (veya güncelleştirir). Şu anda yüklü olan bileşenlerin sessiz bakımı için kullanılan standart bir komut yapısına sahiptir. Yapı, **&lt;InstallerName&gt;.exe**'nin temel değerlerini kullanır.

Aşağıdaki temel komut, yükleme isteğinde bulunulduğunda kullanılabilir seçenekleri gösterir. Bu komutun, yükleyiciyi ilk kez sınarken veya kullanırken kullanılması önemle tavsiye edilir.

```Console
CommerceModernPOS.exe --help install
```

> [!NOTE]
> Modern POS için bir yapılandırma dosyası gerekli değildir. Cihaz etkinleştirme sırasında kullanılan çeşitli değerler için yükleyici artık bu bölümde gösterilen parametrelere (bu makalede daha önce gösterilmiştir) sahiptir.

Aşağıdaki komut, Modern POS uygulaması yüklendikten sonra cihaz etkinleştirme sırasında kullanılması gereken tüm parametreleri belirtir. Bu örnekte, Dynamics 365 Commerce demo verilerinde yaygın olarak kullanılan bir değer olan **Houston-3** kaydı kullanılır.

```Console
CommerceModernPOS.exe install --Register "Houston-3" --Device "Houston-3" --RetailServerURL "https://MyDynamics365CommerceURL.dynamics.com/Commerce"
```

Aşağıdaki komut, çevrimdışı veritabanını yüklemek ve yapılandırmak için kullanılması gereken parametreleri belirtir. SQL Server, kullanılması gereken yapılandırma dosyası ile birlikte belirtilir.

```Console
CommerceModernPOS.exe install --InstallOffline --SQLServerName "SQLExpress" --Config "ModernPOS.Houston-3.xml"
```

İstediğiniz yükleme sonuçlarını elde etmek için bu kavramları birlikte kullanabilir ve eşleştirebilirsiniz.

## <a name="hardware-station"></a>Donanım istasyonu

### <a name="before-you-begin"></a>Başlamadan önce

Eski, self-servis hardware station bileşenini kaldırmanız kritik önem taşır. Daha fazla bilgi için bu makalenin önceki kısımlarında yer alan geçiş adımlarına bakın. Artık bir Satıcı Hesap Bilgileri Aracı yok. Bunun yerine, satıcı hesap bilgileri, bir POS terminali hardware station ile eşlendiğinde yüklenir. Bu yükleyiciyi ilk kez sınarken aşağıdaki komutu çalıştırmanız önemle tavsiye edilir:

```Console
CommerceHardwareStation.exe --help install
```

### <a name="examples-of-silent-deployment"></a>Sessiz dağıtım örnekleri

Bu bölüm, hardware station'ı yüklemek için kullanılan komutların örneklerini gösterir.

#### <a name="silently-install-hardware-station"></a>Hardware station'ı sessizce yükleme

Aşağıdaki komut, hardware station'ı sessizce yükler (veya güncelleştirir). Şu anda yüklü olan bileşenlerin bakımı için kullanılan standart bir komut yapısına sahiptir. Yapı, **&lt;InstallerName&gt;.exe**'nin temel değerlerini kullanır.

Aşağıdaki temel komut, yürütülebilir dosya yükleyicisini çalıştırır.

```Console
HardwareStation.exe install --Port 443 --StoreSystemAOSURL "https://MyDynamics365CommerceURL.dynamics.com/" --StoreSystemChannelDatabaseID "Houston" --SSLCertThumbprint "MySSLCertificateThumbprintOftenHasNumbers"
```

> [!NOTE]
> Hardware station için bir yapılandırma dosyası gerekli değildir. Gerekli çeşitli değerler için yükleyici artık bu bölümde gösterilen parametrelere (bu makalede daha önce gösterilmiştir) sahiptir.

Aşağıdaki komut, standart yükleme sırasında önkoşul denetimlerini atlamak için gerekli tüm parametreleri belirtir. 

> [!NOTE]
> Denetimleri atlamak, önceden tam test etmeden veya geliştirme durumlarında önerilmez.

```Console
HardwareStation.exe install --SkipFirewallUpdate --SkipOPOSCheck --SkipVersionCheck --SkipURLCheck --Config "HardwareStation.Houston.xml"
```

Her zaman olduğu gibi, istediğiniz yükleme sonuçlarını elde etmek için bu kavramları birlikte kullanmak ve eşleştirmek yaygın bir durumdur.

## <a name="commerce-scale-unit-self-hosted"></a>Commerce Scale Unit (şirket içinde barındırılan)

Bu yükleyiciyi ilk kez sınarken aşağıdaki komutu çalıştırmanız önemle tavsiye edilir:

```Console
CommerceStoreScaleUnitSetup.exe --help install
```

### <a name="before-you-begin"></a>Başlamadan önce

Eski, self-servis CSU (şirket içinde barındırılan) bileşenini kaldırmanız kritik önem taşır. Daha fazla bilgi için bu makalenin önceki kısımlarında yer alan geçiş adımlarına bakın.

### <a name="examples-of-silent-deployment"></a>Sessiz dağıtım örnekleri

Bu bölüm, CSU'yu (şirket içinde barındırılan) yüklemek için kullanılan komutların örneklerini gösterir.

#### <a name="silently-install-csu-self-hosted"></a>CSU'yu (şirket içinde barındırılan) sessiz olarak yükleme

Aşağıdaki komut, CSU'yu (şirket içinde barındırılan) sessizce yükler (veya güncelleştirir). Şu anda yüklü olan bileşenlerin sessiz bakımı için kullanılan standart bir komut yapısına sahiptir. Yapı, **&lt;InstallerName&gt;.exe**'nin temel değerlerini kullanır.

Diğer self servis yükleyicilerle karşılaştırıldığında, Commerce Scale Unit (CSU) daha karmaşıktır ve daha fazla miktarda ek bilgi gerektirir. Aşağıdaki komut, herhangi bir yapılandırma dosyası bulunmadığı sırada yürütülebilir dosya yükleyicisini çalıştırmak için gerekli olan minimum komuttur (parametrelerle).

```Console
CommerceScaleUnit.exe install --port 446 --SSLCertThumbprint "MySSLCertificateThumbprintOftenHasNumbers" --RetailServerCertFullPath "store://My/LocalMachine?FindByThumbprint=MyCertificateThumbprintUsedByRetailServer" --AsyncClientAADClientID "MyAAD-Client-IDFor-AsyncClient" --RetailServerAADClientID "MyAAD-Client-IDFor-RetailServer" --CPOSAADClientID "MyAAD-Client-IDFor-CloudPOS" --RetailServerAADResourceID "https://retailstorescaleunit.retailserver.com" --TrustSqlServerCertificate --Config "Contoso.StoreSystemSetup.xml"
```

> [!NOTE]
> CSU (şirket içinde barındırılan) için bir yapılandırma dosyası hala gereklidir.

Aşağıdaki komut, yürütülebilir dosya yükleyicisini bazı alternatif parametrelerle çalıştıran daha kapsamlı bir komuttur.

```Console
CommerceScaleUnit.exe install --Port 446 --SSLCertFullPath "store://My/LocalMachine?FindByThumbprint=MySSLCertificateThumbprintOftenHasNumbers" --AsyncClientCertFullPath "store://My/LocalMachine?FindByThumbprint=MySSLCertificateThumbprintOftenHasNumbers" --RetailServerCertFullPath "store://My/LocalMachine?FindByThumbprint=MyCertificateThumbprintUsedByRetailServer" --AsyncClientAADClientID "MyAAD-Client-IDFor-AsyncClient" --RetailServerAADClientID "MyAAD-Client-IDFor-RetailServer" --CPOSAADClientID "MyAAD-Client-IDFor-CloudPOS" --RetailServerAADResourceID "https://retailstorescaleunit.retailserver.com" --TrustSqlServerCertificate --Verbosity 0 --Config "Contoso.StoreSystemSetup.xml"
```

Aşağıdaki komut, standart yükleme sırasında önkoşul denetimlerini atlamak için gerekli parametreleri belirtir. 

> [!NOTE]
> Denetimleri atlamak, önceden tam test etmeden veya geliştirme durumlarında önerilmez.


```Console
CommerceScaleUnit.exe installer --skipscaleunithealthcheck --skipcertcheck --skipaadcredentialscheck --skipschannelcheck --skipiischeck --skipnetcorebundlecheck --skipsqlservercheck --skipnetframeworkcheck --skipversioncheck --skipurlcheck --Config "Contoso.StoreSystemSetup.xml" --SSLCertFullPath "store://My/LocalMachine?FindByThumbprint=MySSLCertificateThumbprintOftenHasNumbers" --AsyncClientCertFullPath "store://My/LocalMachine?FindByThumbprint=MySSLCertificateThumbprintOftenHasNumbers" --RetailServerCertFullPath "store://My/LocalMachine?FindByThumbprint=MyCertificateThumbprintUsedByRetailServer" --AsyncClientAADClientID "MyAAD-Client-IDFor-AsyncClient" --RetailServerAADClientID "MyAAD-Client-IDFor-RetailServer" --CPOSAADClientID "MyAAD-Client-IDFor-CloudPOS" --RetailServerAADResourceID "https://retailstorescaleunit.retailserver.com" --TrustSqlServerCertificate
```

İstediğiniz yükleme sonuçlarını elde etmek için bu kavramları birlikte kullanabilir ve eşleştirebilirsiniz.

<!--## Mass deployment examples using InTune

This section will be added in a future update.

## Mass deployment examples using System Center Configuration Manager (SCCM)

This section will be added in a future update.-->

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
