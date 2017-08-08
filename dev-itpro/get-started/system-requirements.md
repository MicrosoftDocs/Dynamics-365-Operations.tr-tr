---
title: Sistem gereksinimleri
description: "Bu konuda Microsoft Dynamics 365 Finance and Operations, bulut ve şirket içi dağıtımlar için Enterprise Edition geçerli sürümü için sistem gereksinimleri belirtilmektedir."
author: sericks007
manager: AnnBe
ms.date: 07/14/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, Developer, IT Pro
ms.reviewer: robinr
ms.search.scope: Core
ms.custom: 55651
ms.assetid: e564d51d-42d3-47c5-b388-93b8219c692a
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2016-08-30T00:00:00.000Z
ms.dyn365.ops.version: Platform update 2
ms.translationtype: HT
ms.sourcegitcommit: 08c38aada355583c5a6872f75b57db95d9b81786
ms.openlocfilehash: 871ba89973f6af341c536f67db056bebb54600b3
ms.contentlocale: tr-tr
ms.lasthandoff: 07/25/2017

---

# <a name="system-requirements"></a>Sistem gereksinimleri

[!include[banner](../includes/banner.md)]


Bu konuda Microsoft Dynamics 365 Finance and Operations, bulut ve şirket içi dağıtımlar için Enterprise Edition, geçerli sürümü için sistem gereksinimleri belirtilmektedir. Finance and Operations'u yüklemeden önce uygun olduğunda, çalışmakta olduğunuz sistemin minimum ağ, donanım ve yazılım gereksinimlerini karşıladığını doğrulayın.


## <a name="supported-microsoft-office-applications"></a>Desteklenen Microsoft Office uygulamaları
Aşağıdaki Office uygulamaları Finance and Operations şirket içi dağıtımlarında bulutta desteklenir.
-   Microsoft Excel ve Word eklentilerini çalıştırmak için Windows veya Mac için Microsoft Office 2016'yı yüklemiş olmanız gerekir. Sürüm gereksinimleri hakkında daha fazla bilgi için bkz. [Office tümleştirme sorunlarını giderme](/dynamics365/unified-operations/dev-itpro/office-integration/office-integration-troubleshooting).
-   Excel'e Aktar veya Word'e Aktar işleviyle oluşturulan belgeleri görüntülemek için Microsoft Office 2007 veya sonraki bir sürümü yüklemiş olmanız gerekir.

# <a name="system-requirements-specific-to-cloud-deployments"></a>Bulut dağıtımlarına özel sistem gereksinimleri
## <a name="network-requirements"></a>Ağ gereksinimleri
-   Finance and Operations 250-300 milisaniye (ms) veya daha az gecikmeye sahip ağlar için tasarlanmıştır. Bu gecikme, bir tarayıcı istemcisinden Finance and Operations'ı barındıran Microsoft Azure veri merkezine iletim süresidir. Ağ gecikmesini <http://www.azurespeed.com>'da sınamanızı öneririz.
-   Finance and Operations için bant genişliği gereksinimleri senaryoya bağlıdır. En tipik senaryolar 50 kilobayt/saniye (KBps) üzerinde bir bant genişliği gerektirir. Ancak, kapsamlı özelleştirme içeren çalışma alanları veya senaryolar gibi yüksek yük gereksinimleri olan senaryolar için daha yüksek bant genişliği önerilir.

Genel olarak, Finance and Operations Internet için optimize edilmiştir. Bir tarayıcı istemcisinden Azure veri merkezine gidiş dönüş sayısı oldukça küçüktür ve tüm yükü sıkıştırılmıştır. 

> [!WARNING]
> Kullanıcı sayısıyla minimum bant genişliği gereksinimlerini çarpıp bir müşteri konumundan bant genişliği gereksinimlerini hesaplamayın. Belirli bir konumun eşzamanlı kullanımını hesaplamak çok zordur. Bant genişliği gereksinimleri konusunda kaygıları olan müşteriler Finance and Operations'ın bir önizleme sürümünü kullanabilir.

## <a name="net-framework-requirements"></a>.NET Framework gereksinimleri
Finance and Operations, belge yönlendirme aracısı gibi click-once uygulamaları için .NET Framework sürüm 4.6.2 gerektirir. Yükleme yönergeleri için bkz. [.NET Framework'ü yükleme](https://msdn.microsoft.com/en-us/library/5a4x27ek(v=vs.110).aspx).

## <a name="supported-web-browsers"></a>Desteklenen web tarayıcıları
Web uygulamasını belirtilen işletim sistemleri üzerinde çalışan aşağıdaki web tarayıcılarından birinde çalıştırabilirsiniz:


-   Windows 10 üzerinde Microsoft Edge (son genel olarak yayımlanmış sürüm)
-   Windows 10, Windows 8.1 veya Windows 7 üzerinde Internet Explorer 11
-   Windows 10, Windows 8.1, Windows 8, Windows 7 veya Google Nexus 10 tablet üzerinde Google Chrome (son genel olarak yayımlanan sürümü)
-   Mac OS X 10.10 (Yosemite), 10.11 (El Capitan) ve 10.12 (Sierra) veya Apple iPad üzerinde Apple Safari (son genel olarak yayınlanmış sürüm)

Her web tarayıcısı için en son sürümü bulmak için, yazılım üreticisinin web sitesine gidin. 

> [!NOTE]
> -   Görev Kaydedici'den ekran görüntülerinin alınmasına ve bunların oluşturulan Microsoft Word belgelerine eklenmesine izin vermek için bir önceden yayınlanmış Chrome eklentisinin yüklü olması gerekir. <!---For instructions about how to install the extension, see [Screenshot Extension setup](/dynamics365/unified-operations/dev-itpro/user-interface/task-recorder).-->
> -   İş Akışı Düzenleyicisi bir ClickOnce uygulaması olarak başlatılır. ClickOnce uygulamalarını yalnızca Microsoft Edge ve Internet Explorer (Microsoft Windows'un desteklenen bir sürümünde) destekler. İş Akışı Düzenleyicisi ClickOnce uygulaması için 64-bit uyumlu bir işletim sistemi gereklidir.
> -   Finansal raporlama için Rapor Tasarımcısı bir ClickOnce uygulaması olarak başlatılır. 64-bit uyumlu bir işletim sistemi gerektirir. Chrome kullanıyorsanız, rapor tasarımcısı istemcisini indirebilmek için ClickOnce eklentisini yüklemeniz gerekir. Chrome'u gizli modda kullanıyorsanız, ClickOnce uzantısının da gizli mod için etkinleştirildiğinden emin olun.
> -   PDF dosyalarının önizlemesini yapmak için (en son sürüm genel kullanıma açık) Windows 10 üzerinde, Microsoft Edge veya (en son sürüm genel kullanıma açık) Windows 10, Windows 8.1, Windows 8, Windows 7 veya Google Nexus 10 tablet üzerinde Google Chrome gibi tarayıcıları kullanmanızı öneririz.


### <a name="supported-web-browsers-for-retail-cloud-pos"></a>Perakende Bulut POS'u için desteklenen web tarayıcıları

Retail Cloud POS belirtilen işletim sistemleri üzerinde çalışan aşağıdaki web tarayıcılarından birinde çalıştırılabilir:

-   Windows 10 üzerinde Microsoft Edge (son genel olarak yayımlanmış sürüm)
-   Windows 10, Windows 8.1 veya Windows 7 üzerinde Internet Explorer 11
-   Windows 10, Windows 8.1 veya Windows 7 üzerinde Chrome (son genel olarak yayımlanmış sürüm)

## <a name="retail-modern-pos-requirements"></a>Retail Modern POS gereksinimleri
### <a name="supported-operating-systems"></a>Desteklenen işletim sistemleri

-   Retail Modern POS 32 bitlik bir uygulama olmakla birlikte, hem x86 hem de x64 mimarileri üzerinde çalışır.
-   Retail Modern POS yalnızca Windows 10 Pro, Enterprise ve Enterprise Long Term Servicing Branch (LTSB) sürümlerinde desteklenir.

### <a name="minimum-system-requirements"></a>Minimum sistem gereksinimleri

-   Desteklenen en düşük çözünürlük 1280 × 1024'tür.
-   Retail Modern POS'un çalıştığı bilgisayarın aşağıdaki gereksinimleri karşılaması gerekir:
    -   En az 2 gigahertz at (GHz) hızla çalışan bir çift çekirdekli işlemcisi olmalıdır.
    -   En az 3 gigabayt (GB) RAM'i olması gerekir.
    -   Internet erişiminin olması gerekir.

## <a name="retail-hardware-station-requirements"></a>Retail hardware station gereksinimleri
### <a name="supported-operating-systems"></a>Desteklenen işletim sistemleri

-   Retail hardware station 32 bitlik bir uygulama olmakla birlikte, hem x86 hem de x64 mimarileri üzerinde çalışır.
-   Retail hardware station aşağıdaki işletim sistemlerinde desteklenir:
    -   Windows 7 Professional, Enterprise ve Ultimate sürümleri 
    
    > [!NOTE]
    > Windows 7 yalnızca Internet Explorer 11 sistem üzerine el ile yüklendiyse desteklenir.

    -   Windows 8.1 Güncelleme 1 Professional, Enterprise ve Embedded sürümleri
    -   Windows 10 Pro, Enterprise ve Enterprise LTSB sürümleri

### <a name="minimum-system-requirements"></a>Minimum sistem gereksinimleri

Aşağıdaki öğelerin yüklenip kullanılabilmesi için bilgisayarın tüm sistem gereksinimlerini karşılaması gerekir:

-   Internet Information Services (IIS)
-   Üçüncü taraf donanım

## <a name="retail-store-scale-unit-requirements"></a>Perakende Mağaza Ölçeği Birimi gereksinimleri
### <a name="supported-operating-systems"></a>Desteklenen işletim sistemleri

-   Perakende Mağaza Ölçeği Birimi 32 bitlik bir uygulama olmakla birlikte, hem x86 hem de x64 mimarileri üzerinde çalışır.
-   Perakende Mağaza Ölçeği Birimi aşağıdaki işletim sistemlerinde desteklenir:
    -   Windows 7 Professional, Enterprise ve Ultimate sürümleri
    -   Windows 8.1 Güncelleme 1 Professional, Enterprise ve Embedded sürümleri
    -   Windows 10 Pro, Enterprise ve Enterprise LTSB sürümleri

### <a name="minimum-system-requirements"></a>Minimum sistem gereksinimleri

-   4 GB RAM
-   1.6 GHz çekirdek başına en yüksek CPU hızı (En az iki çekirdek.)
-   En az 10 GB boş alan (kanal veritabanı için büyük bir boş alan gerekebilir.)

### <a name="recommended-system-requirements"></a>Önerilen sistem gereksinimleri

-   6 GB RAM
-   2.4 GHz i7 (veya eşdeğeri) çekirdek başına en yüksek CPU hızı (Dört çekirdek önerilir.)
-   En az 10 GB boş alan (kanal veritabanı için büyük bir boş alan gerekebilir.)

## <a name="connector-requirements"></a>Bağlayıcı gereksinimleri
### <a name="supported-operating-systems"></a>Desteklenen işletim sistemleri

-   Connector for Microsoft Dynamics AX'te iki ayrı yükleyici olan **Async Server Connector service** ve **Real-time service for Dynamics AX 2012 R3** bulunur.
-   İki bileşen de 32 bitlik bir uygulama olmakla birlikte, hem x86 hem de x64 mimarileri üzerinde çalışır.
-   Her iki bileşen de aşağıdaki işletim sistemlerinde desteklenir:
    -   Windows 7 Professional, Enterprise ve Ultimate sürümleri
    -   Windows 8.1 Güncelleme 1 Professional, Enterprise ve Embedded sürümleri
    -   Windows 10 Pro, Enterprise ve Enterprise LTSB sürümleri
    -   Windows Server 2012 R2, Windows Server 2016

### <a name="minimum-system-requirements"></a>Minimum sistem gereksinimleri

-   2 GB RAM, 4 GB RAM önerilir
-   1.6 GHz çekirdek başına en yüksek CPU hızı (En az iki çekirdek.)
-   En az 10 GB boş alan (kanal veritabanı için büyük bir boş alan gerekebilir.)

## <a name="requirements-for-development-on-local-vms"></a>Yerel VM'ler üzerinde geliştirme için gereksinimler
Yerel sanal makinelerde (VM) geliştirme için gereksinimler hakkında bilgi için bkz. [yerinde çalışan VM](../dev-tools/access-instances.md).

# <a name="system-requirements-for-on-premises-deployments"></a>Şirket içi dağıtımlar için sistem gereksinimleri

## <a name="network-requirements"></a>Ağ gereksinimleri
Finance and Operations (şirket içi) Internet Protocol Version 4 (IPv4) veya Internet Protocol Version 6 (IPv6) kullanın ağlarda çalışabilir. Sisteminizi planlarken ağ ortamını dikkate alın ve aşağıdaki yönergeleri kullanın.

### <a name="network-response-time"></a>Ağ yanıt süresi
Aşağıdaki tablo, web tarayıcısı ve Application Object Server (AOS) ve şirket içindeki bir veritabanı ve AOS arasındaki minimum bağlantı gereksinimini listeler.

| Değer     | Web tarayıcısından AOS'e | Veritabanına AOS                                            |
|-----------|--------------------|------------------------------------------------------------|
| Bant genişliği | Kullanıcı başına 50 KBps   | 100 MBps                                                   |
| Gecikme süresi   | < 250-300 ms       | < 1 ms (yalnızca yerel ağ). AOS ve veritabanının birlikte bulunması gerekir. |

- Finance and Operations (şirket içi) 250-300 milisaniye (ms) veya daha az gecikmeye sahip ağlar için tasarlanmıştır. Bu gecikme, bir tarayıcı istemcisinden Finance and Operations'ı barındıran veri merkezine iletim süresidir.
- Finance and Operations (şirket içi) için bant genişliği gereksinimleri senaryoya bağlıdır. Tipik senaryolar tarayıcı ve Finance and Operations sunucusu arasında saniyede 50 kilobayttan (KBps) fazla bant genişliği gerektirir. Ancak, kapsamlı özelleştirme içeren çalışma alanları veya senaryolar gibi yüksek yük gereksinimleri olan senaryolar için daha yüksek bant genişliği önerilir ve kullanıma bağlıdır.
AOS ve SQL Server Veritabanının farklı veri merkezlerinde olduğu dağıtımlar desteklenmez. AOS ve SQL Server veritabanının birlikte bulunması gerekir. Genel olarak Finance and Operations tarayıcıdan sunucuya gidiş gelişleri azaltmak üzere optimize edilmiştir. Bir tarayıcı istemcisinden veri merkezine gidiş dönüş sayısı her bir kullanıcı etkileşimi için sıfırdır veya birdir ve yükü sıkıştırılmıştır.

> [!WARNING]
> Kullanıcı sayısıyla minimum bant genişliği gereksinimlerini çarpıp bir müşteri konumundan bant genişliği gereksinimlerini hesaplama. Belirli bir konumun eşzamanlı kullanımını hesaplamak çok zordur. Özel durumunuzun performansı için en iyi gösterge için Finance and Operations üretim ortamına karşılık gerçek hayat simülasyonunu kullanmanızı öneririz. 

### <a name="lan-environments"></a>LAN ortamları
Yerel ağ (LAN) ortamlarında Microsoft Windows Server içindeki Microsoft Uzak Masaüstü, Finance and Operations'a bağlanmak için gerekli değildir. Ancak, sunucu dağıtımlarını oluşturan VM'ler üzerindeki servis operasyonları için gerekli olabilir.

### <a name="wan-environments"></a>WAN ortamları
geniş alan ağı (WAN) ortamlarında Windows Server içindeki Uzak Masaüstü, Finance and Operations'a bağlanmak için gerekli değildir.

### <a name="internet-connectivity-requirements"></a>Internet bağlantısı gereksinimleri
Finance and Operations (şirket içi) son kullanıcı çalışma istasyonlarında İnternet bağlantısı gerektirmez. Ancak, bazı özellikler İnternet bağlantısı olmadan kullanılamaz.

| Tarayıcı istemcisi | İnternet bağlantısı olmayan bir intranet senaryosu, şirket içi dağıtım seçeneği için bir tasarım noktasıdır. Bulut hizmetleri gerektiren bazı özellikler kullanılamaz, örneğin LCS içindeki Yardım ve Görev kılavuzu kütüphaneleri gibi. |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Sunucu         | AOS veya Service Fabric katmanının LCS ile iletişim kurabilmesi mümkün olmalıdır. Şirket içi tarayıcı tabanlı istemci İnternet erişimine ihtiyaç duymaz.                                                                                |
| Telemetri      | Bağlantıda uzun kesintiler varsa telemetri veri kaybı olabilir. LCS'ye bağlantıda kesintiler şirket içi uygulama işlevlerini etkilemez.                                                |
| LCS            | LCS'ye bağlantı dağıtım, kod dağıtımı ve servis operasyonları için gereklidir.                                                                                                                                 |
## <a name="telemetry-data-transfer-to-the-cloud"></a>Buluta telemetri veri aktarımı
Çoğu telemetri yerel olarak depolanır ve Microsoft Windows içerisinde Olay Görüntüleyicisi kullanılarak erişilebilir. Telemetri olaylarının küçük bir alt kümesi bulut için tanılama amacıyla Microsoft telemetri iletişim hattına aktarılır. Müşteri verileri ve son kullanıcı tanımlanabilir verileri, Microsoft'a gönderilen telemetrinin parçası değildir. VM adları Microsoft'a ortam yönetimine ve tanılamaya LCS portalından yardımcı olmak üzere gönderilir.

## <a name="domain-requirements"></a>Etki alanı gereksinimleri
Finance and Operations (şirket içi) yüklediğinizde aşağıdaki etki alanı gereksinimleri göz önünde bulundurun:

- Finance and Operations (şirket içi) bileşenlerini barındıran sanal makineler bir Active Directory Etki Alanına ait olmalıdır. Active Directory Domain Services (AD DS) yerel modda yapılanıdırılmış olmalıdır.
- Finance and Operations (şirket içi) bileşenlerini çalıştıran Sanal Makineler, Active Directory Domain Services'ta birbirlerine erişime sahip olmalıdır. 
- Etki alanı denetleyicisinin Microsoft Windows Server 2016'da çalışması gerekir.

## <a name="hardware-requirements"></a>Donanım gereksinimleri
Bu bölüm Finance and Operations (şirket içi) çalıştırmak için gerekli donanımı açıklar.
Sistem yapılandırmasına, veri bileşimi ve kullanmaya karar verdiğiniz uygulamalar ve özelliklere göre gerçek donanım gereksinimleri farklılık gösterir. Finance and Operations (şirket içi) için uygun donanım seçimini etkileyebilecek bazı faktörler aşağıda belirtilmiştir:

- Saat başına hareket sayısı.
- Eşzamanlı kullanıcıların sayısı.

## <a name="minimum-infrastructure-requirements"></a>Altyapı minimum gereksinimleri
Finance and Operations (şirket içi) AOS, Toplu iş, Veri yönetimi, Yönetim raporlayıcısı ve Ortam düzenleyici hizmetleri için Microsoft Azure Service Fabric kullanır. Microsoft SQL Server Reporting Services (SSRS), Service Fabric kümesinde barındırılmaz.
SQL Server üretim kullanımı için en az iki düğüme sahip yüksek kullanılabilirlik HADRON kurulumunda ayarlanmış olmalıdır.
Aşağıdaki şekil, Service Fabric kümenizdeki önerilen minimum düğümlerin sayısını gösterir.

[![service fabric kümesi için önerilen düğüm sayısı](./media/system-reqs-on-premises-01.png)](./media/system-reqs-on-premises-01.png) 

## <a name="processor-and-ram-requirements"></a>İşlemci ve RAM gereksinimleri
Aşağıdaki tablo bu dağıtım seçeneğinin her bir rolünü çalıştırmak için gerekli işlemcilerin sayısını ve rastgele erişim belleğini (RAM) miktarını belirtir. Service Fabric tek başına kümesi minimum gereksinim önerileri için daha fazla bilgi için bkz [Service Fabric tek başına küme dağıtımınızı planlama ve hazırlama](/azure/service-fabric/service-fabric-cluster-standalone-deployment-preparation).

> [!NOTE]
> Aynı bilgisayarda diğer Microsoft yazılımları yüklüyse, sistem bu yazılım için de donanım gereksinimleriyle uyumlu olmalıdır. Aynı bilgisayardaki sunucu uygulamalarını AOS olarak 1 gigabayt (GB) RAM ile sınırlamanızı öneririz.

**Rol ve topoloji türüne göre boyutlandırma**

| Topoloji   | Rol (düğüm türü)              | Önerilen işlemci çekirdekleri | Önerilen bellek (GB) |
|------------|-------------------------------|-----------------------------|-------------------------|
| Üretim | AOS, Veri yönetimi, Toplu iş   | 8                           | 24                      |
|            | Yönetim Raporlayıcısı           | 4                           | 16                      |
|            | SQL Server Reporting Services | 4                           | 16                      |
|            | Düzenleyici                  | 4                           | 16                      |
| Korumalı alan    | AOS, Veri yönetimi, Toplu iş   | 4                           | 24                      |
|            | Yönetim Raporlayıcısı           | 4                           | 16                      |
|            | SQL Server Reporting Services | 4                           | 16                      |
|            | Düzenleyici                  | 4                           | 16                      |

**Üretim ve korumalı alan dağıtımları için minimum boyutlandırma tahminleri**\*

| Topoloji                                  | Rol                          | Örneklerin sayısı |
|-------------------------------------------|-------------------------------|---------------------|
| Üretim                                | AOS (Veri yönetimi, Toplu iş)  | 3                   |
|                                           | Yönetim Raporlayıcısı           | 2                   |
|                                           | SQL Server Reporting Services | 1                   |
|                                           | Düzenleyici\*\*                | 3                   |
| Korumalı alan                                   | AOS, Veri yönetimi, Toplu iş   | 2                   |
|                                           | Yönetim Raporlayıcısı           | 1                   |
|                                           | SQL Server Reporting Services | 1                   |
|                                           | Düzenleyici                  | 3                   |
| *Üretim ve Korumalı alan topolojileri özeti* |                               | 16                  |

\*Bu sayılar önizleme müşterilimiz tarafından doğrulanmaktadır ve bu bildirime dayalı olarak ihtiyaç duyulduğu şekilde değiştirilebilir.

\*\*Orchestrator birincil düğüm türü olarak atanmıştır ve Service Fabric hizmetlerini de çalıştırmak üzere kullanılır.

**İlk arka uç SQL Server AD tahminleri**

[![İlk arka uç SQL Server AD tahminleri](./media/system-reqs-on-premises-02.PNG)](./media/system-reqs-on-premises-02.PNG) 

\*SQL Server boyutları iş yüklerine yüksek oranda bağlıdır. Daha fazla bilgi için bkz. [Şirket içi ortamlar donanım boyutlandırma](#Hardware-sizing-for-on-premises-environments) bölümü.

## <a name="storage"></a>Depolama

- **AOS** - Finance and Operations (şirket içi) yapılandırılmamış veriyi depolamak için bir Server Message Block (SMB) 3.0 paylaşımını kullanacaktır. Daha fazla bilgi için bkz [Windows Server 2016 içinde Storage Spaces Direct](/windows-server/storage/storage-spaces/storage-spaces-direct-overview).
- **SQL** – Geçerli seçenekler:
    - Yüksek kullanılabilirliğe sahip bir katı hal sürücüsü (SSD) kurulumu.
    - OLTP çıkışları için optimize bir ağ alanı depolama (SAN).
    - Yüksek performans doğrudan bağlantılı depolama (DAS) 
- **SQL ve veri yönetimi IOPS** – Hem veri yönetimi hem de SQL Server için depolamanı en az saniyede 2.000 giriş/çıkış operasyonlarına (IOPS) sahip olması gerekir. Üretim IOPS birçok etmene bağlıdır. Daha fazla bilgi için bkz. "Şirket içi ortamlar donanım boyutlandırma" bölümü. 
- **Sanal makine IOPS** – Her bir sanal makine en az 100 yazma IOPS'ye sahip olmalıdır.

## <a name="virtual-host-requirements"></a>Sanal ana makine gereksinimleri
Finance and Operations (şirket içi) ortamı için sanal ana bilgisayarlar ayarlamak istiyorsanız aşağıdaki kılavuzlara başvurun: [Service Fabric kümenizi planlama ve hazırlama](/azure/service-fabric/service-fabric-cluster-standalone-deployment-preparation) ve [Bir service fabric kümesini açıklama](/azure/service-fabric/service-fabric-cluster-resource-manager-cluster-description). Her sanal ana bilgisayar boyutlandırılacak altyapı için yeterli çekirdeğe sahip olmalıdır. SQL Server'ın fiziksel donanım üzerinde bulunduğu çoklu gelişmiş yapılandırmalar mümkündür ancak geri kalan her şey sanallaştırılmıştır. SQL Server sanallaştırılmış ise, disk alt sisteminde hızlı bir SAN veya eşdeğer olmalıdır. Her durumda, sanal ana bilgisayarın temel kurulumunun yüksek oranda kullanılabilir ve yedekli olduğundan emin olun. Sanallaştırılma kullanılan her durumda VM anlık görüntüleri alınmamalıdır.

## <a name="software-requirements-for-all-server-computers"></a>Tüm sunucu bilgisayarları için yazılım gereksinimleri
Aşağıdaki yazılım Finance and Operations (şirket içi) bileşenlerin yüklenebilmesi için bilgisayarda mevcut olmalıdır.

- Microsoft .NET Framework 4.5.1 veya daha yüksek
- Service Fabric Daha fazla bilgi için bkz. [Service Fabric kümenizi hazırlayın ve planlayın](/azure/service-fabric/service-fabric-cluster-standalone-deployment-preparation).

## <a name="supported-server-operating-systems"></a>Desteklenen sunucu işletim sistemleri
Aşağıdaki tablo Finance and Operations bileşenleri için desteklenen sunucu işletim sistemlerini listeler.

| İşletim sistemi                                     | Notlar                                                                                  |
|------------------------------------------------------|----------------------------------------------------------------------------------------|
| Microsoft Windows Server 2016 Veri Merkezi veya Standart | Bu gereksinimler AOS'yi barındıran veritabanı ve Service Fabri kümesi içindir. |

## <a name="software-requirements-for-database-servers"></a>Veritabanı sunucuları için yazılım gereksinimleri

- SQL Server 2016'nın yalnızca 64-bit sürümleri desteklenir.
- Bir üretim ortamında, kullandığınız SQL Server sürümü için en son toplu güncelleştirmeyi (CU) yüklemenizi öneririz.
- Finance and Operations (şirket içi) büyük küçük harfe duyarlı olmayan, aksana duyarlı olan, kana duyarlı olan ve genişliğe duyarlı olmayan Unicode harmanlamalarını destekler. Harmanlama AOS örneklerini çalıştıran bilgisayarların Windows yerel alfabeleri ile aynı olmalıdır. Yeni bir yükleme ayarlıyorsanız, SQL Server harmanlaması yerine Windows harmanlamasını seçmenizi öneririz. Bir SQL Sunucu veritabanı için bir harmanlam seçmek hakkında daha fazla bilgi için bkz. [SQL Server belgeleri](/sql/sql-server/sql-server-technical-documentation).
Aşağıdaki tablo Finance and Operations veritabanları için desteklenen SQL Server sürümlerini listeler. Daha fazla bilgi için, [SQL Server](https://www.microsoft.com/en-us/sql-server/sql-server-2016) minimum donanım gereksinimlerine göz atın.

| Gereksinim                                                      | Notlar                                                                                                                     |
|------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------|
| Microsoft SQL Server 2016 Standard Edition veya Enterprise Edition | SQL Server 2016 donanım gereksinimleri için bkz. [SQL Server 2016 yüklemek için Donanım ve Yazılım Gereksinimleri](/sql/sql-server/install/hardware-and-software-requirements-for-installing-sql-server). |

## <a name="software-requirements-for-client-computers"></a>İstemci bilgisayarları için yazılım gereksinimleri
Finance and Operations web uygulaması HTML5.0 uyumlu web tarayıcısına sahip herhangi bir cihazda çalışabilir. Microsoft'un onaylamış olduğu belirli cihaz/tarayıcı kombinasyonlarına şunlar dahildir:

- Windows 10 üzerinde Microsoft Edge (son genel olarak yayımlanmış sürüm)
- Windows 10, Windows 8.1 veya Windows 7 üzerinde Internet Explorer 11
- Windows 10, Windows 8.1, Windows 8, Windows 7 veya Google Nexus 10 tablet üzerinde Google Chrome (son genel olarak yayımlanan sürümü)
- Mac OS X 10.10 (Yosemite), 10.11 (El Capitan) ve 10.12 (Sierra) veya Apple iPad üzerinde Apple Safari (son genel olarak yayınlanmış sürüm)

## <a name="software-requirements-for-active-directory-federation-services"></a>Active Directory Federasyon Hizmetleri için yazılım gereksinimleri 
Windows Server 2016 üzerinde Active Directory Federation Services (AD FS)

Etki alanı denetleyicisi 2012 R2 veya daha büyük etki alanı işlev düzeyine sahip Windows Server 2012 R2 veya üzeri olmalıdır

Etki alanı işlev düzeyleri hakkında daha fazla bilgi için bakınız: 
- [Active Directory İşlevsellik düzeyleri nedir](https://technet.microsoft.com/en-us/library/cc787290(v=ws.10).aspx)
- [Active Directory Etki alanı hizmetleri işlev düzeyini anlamak](https://technet.microsoft.com/en-us/library/understanding-active-directory-functional-levels(v=ws.10).aspx)
 
## <a name="hardware-and-software-requirements-for-retail-components"></a>Perakende bileşenleri için donanım ve yazılım gereksinimleri
Finance and Operations (şirket içi) şu anda Perakende bileşenlerini içermez.

<a name="see-also"></a>Ayrıca bkz.
--------

[Dynamics 365 for Finance and Operations, Enterprise Edition'ın değerlendirme kopyasını edinin](/dynamics365/unified-operations/dev-itpro/dev-tools/get-evaluation-copy)

