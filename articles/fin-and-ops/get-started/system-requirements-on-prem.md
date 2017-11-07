---
title: "Şirket içi dağıtımlar için sistem gereksinimleri"
description: "Bu konuda Microsoft Dynamics 365 for Finance and Operations ve şirket içi dağıtımlar için Enterprise Edition geçerli sürümü için sistem gereksinimleri belirtilmektedir."
author: kfend
manager: AnnBe
ms.date: 08/02/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 55651
ms.assetid: 
ms.search.region: Global
ms.author: kfend
ms.search.validFrom: 2016-08-30
ms.dyn365.ops.version: Platform update 8
ms.translationtype: HT
ms.sourcegitcommit: 25a6f326c57e84d6a7c356ac5407be7ed3095f83
ms.openlocfilehash: 5edc6f0b2240e9dd2d3b72a13f35e96f016aa013
ms.contentlocale: tr-tr
ms.lasthandoff: 10/04/2017

---

# <a name="system-requirements-for-on-premises-deployments"></a>Şirket içi dağıtımlar için sistem gereksinimleri

[!include[banner](../includes/banner.md)]

Bu konuda Microsoft Dynamics 365 for Finance and Operations ve şirket içi dağıtımlar için Enterprise Edition geçerli sürümü için sistem gereksinimleri belirtilmektedir. Finance and Operations'u yüklemeden önce bu adım uygun olduğunda, çalışmakta olduğunuz sistemin minimum ağ, donanım ve yazılım gereksinimlerini karşıladığını doğrulayın.

## <a name="network-requirements"></a>Ağ gereksinimleri
Microsoft Dynamics 365 for Finance and Operations, Enterprise edition (şirket içi) Internet Protocol Version 4 (IPv4) veya Internet Protocol Version 6 (IPv6) kullanan ağlarda çalışabilir. Sisteminizi planlarken ağ ortamını dikkate alın ve aşağıdaki yönergeleri kullanın.

### <a name="network-response-time"></a>Ağ yanıt süresi
Aşağıdaki tablo, web tarayıcısı ve Application Object Server (AOS) ve şirket içindeki bir veritabanı ve AOS arasındaki minimum bağlantı gereksinimini listeler.

| Değer     | Web tarayıcısından AOS'e                      | Veritabanına AOS |
|-----------|-----------------------------------------|------------------------------------------------------------------------------------------|
| Bant genişliği | Kullanıcı başına saniyede 50 kilobayt (KBps) | 100 MB / saniye (MBps) |
| Gecikme süresi   | 250-300 milisaniyeden (ms) az     | 1 ms'den az (yerel ağ [LAN] yalnızca). AOS ve veritabanının birlikte bulundurulması gerekir. |

- Finance and Operations (şirket içi) 250-300 milisaniye (ms) veya daha az gecikmeye sahip ağlar için tasarlanmıştır. Bu gecikme, bir tarayıcı istemcisinden Finance and Operations'ı barındıran veri merkezine iletim süresidir.
- Finance and Operations (şirket içi) için bant genişliği gereksinimleri senaryoya bağlıdır. Tipik senaryolar tarayıcı ve Finance and Operations sunucusu arasında saniyede 50 KBps fazla bant genişliği gerektirir. Ancak, kapsamlı özelleştirme içeren çalışma alanları veya senaryolar gibi yüksek yük gereksinimleri olan senaryolar için daha yüksek bant genişliği öneririz. Bant genişliğinin belirli miktarı kullanıma bağlıdır.

AOS ve Microsoft SQL Server veritabanının farklı veri merkezlerinde olduğu dağıtımlar desteklenmez. AOS ve SQL Server veritabanının birlikte bulundurulması gerekir. 

Genel olarak Finance and Operations tarayıcıdan sunucuya gidiş gelişleri azaltmak üzere optimize edilmiştir. Bir tarayıcı istemcisinden veri merkezine gidiş dönüş sayısı her bir kullanıcı etkileşimi için sıfırdır veya birdir ve yükü sıkıştırılmıştır.

> [!WARNING]
> Kullanıcı sayısıyla minimum bant genişliği gereksinimlerini çarpıp bir müşteri konumundan bant genişliği gereksinimlerini hesaplama. Belirli bir konumun eşzamanlı kullanımını hesaplamak çok zordur. Özel durumunuzun performansı için en iyi gösterge için Finance and Operations üretim ortamına karşılık gerçek hayat simülasyonunu kullanmanızı tavsiye ederiz. 

### <a name="lan-environments"></a>LAN ortamları
LAN ortamlarında Microsoft Windows Server içindeki Microsoft Uzak Masaüstü, Finance and Operations'a bağlanmak için gerekli değildir. Ancak, sunucu dağıtımlarını oluşturan sanal makineler (VM) üzerindeki servis operasyonları için Uzak Masaüstü gerekli olabilir.

### <a name="wan-environments"></a>WAN ortamları
Geniş alan ağı (WAN) ortamlarında Windows Server içindeki Uzak Masaüstü, Finance and Operations'a bağlanmak için gerekli değildir.

### <a name="internet-connectivity-requirements"></a>Internet bağlantısı gereksinimleri
Finance and Operations (şirket içi) kullanıcı çalışma istasyonlarında internet bağlantısı gerektirmez. Ancak, bazı özellikler internet bağlantısı yoksa kullanılamaz.

|                    |   |
|--------------------|---|
| **Tarayıcı istemcisi** | İnternet bağlantısı olmayan bir intranet senaryosu, şirket içi dağıtım seçeneği için bir tasarım noktasıdır. Bulut hizmetleri gerektiren bazı özellikler kullanılamaz, örneğin Microsoft Dynamics Lifecycle Services (LCS) içindeki Yardım ve Görev kılavuzu kütüphaneleri gibi. |
| **Sunucu**         | AOS veya Microsoft Azure Service Fabric katmanının LCS ile iletişim kurabilmesi mümkün olmalıdır. Şirket içi tarayıcı tabanlı istemci internet erişimine ihtiyaç duymaz. |
| **Telemetri**      | Bağlantıda uzun kesintiler varsa telemetri veri kaybı olabilir. LCS'ye bağlantıda kesintiler şirket içi uygulama işlevlerini etkilemez. |
| **LCS**            | LCS'ye bağlantı dağıtım, kod dağıtımı ve servis operasyonları için gereklidir. |

## <a name="telemetry-data-transfer-to-the-cloud"></a>Buluta telemetri veri aktarımı
Çoğu telemetri verisi yerel olarak depolanır ve Microsoft Windows içerisinde Olay Görüntüleyicisi kullanılarak erişilebilir. Telemetri olaylarının küçük bir alt kümesi bulut için tanılama amacıyla Microsoft telemetri iletişim hattına aktarılır. Müşteri verileri ve kullanıcı tanımlanabilir verileri, Microsoft'a gönderilen telemetrinin verisinin parçası değildir. VM adları Microsoft'a ortam yönetimine ve tanılamaya LCS portalından yardımcı olmak üzere gönderilir.

## <a name="domain-requirements"></a>Etki alanı gereksinimleri
Finance and Operations (şirket içi) yüklediğinizde aşağıdaki etki alanı gereksinimleri göz önünde bulundurun:

- Finance and Operations (şirket içi) bileşenlerini barındıran VM'ler bir Active Directory etki alanına ait olmalıdır. Active Directory Domain Services (AD DS) yerel modda yapılanıdırılmış olmalıdır.
- Finance and Operations (şirket içi) bileşenlerini çalıştıran VM'lerin birbirlerine erişimleri olmalıdır. Bu erişim AD DS içerisinde yapılandırılır. 
- Etki alanı denetleyicisi 2012 R2 veya daha büyük etki alanı işlev düzeyine sahip Microsoft Windows Server 2012 R2 veya üzeri olmalıdır.

## <a name="hardware-requirements"></a>Donanım gereksinimleri
Bu bölüm Finance and Operations (şirket içi) çalıştırmak için gerekli olan donanımı açıklar.

Gerçek donanım gereksinimleri, sistem yapılandırmasına, veri bileşimi ve kullanmaya karar verdiğiniz uygulamalar ve özelliklere göre farklılık gösterir. Finance and Operations (şirket içi) için uygun donanım seçimini etkileyebilecek bazı faktörler aşağıda belirtilmiştir:

- Saat başına hareket sayısı
- Eşzamanlı kullanıcıların sayısı

## <a name="minimum-infrastructure-requirements"></a>Altyapı minimum gereksinimleri
Finance and Operations (şirket içi) AOS, Toplu iş, Veri yönetimi, Yönetim raporlayıcısı ve Ortam düzenleyici hizmetleri için Service Fabric kullanır. 

SQL Server üretim kullanımı için en az iki düğüme sahip yüksek kullanılabilirlik HADRON kurulumuna sahip olmalıdır.

Aşağıdaki şekil, Service Fabric kümeniz için önerilen minimum düğümlerin sayısını gösterir.

[![Service Fabric kümesi için önerilen düğüm sayısı](./media/system-reqs-on-premises-01.png)](./media/system-reqs-on-premises-01.png) 

## <a name="processor-and-ram-requirements"></a>İşlemci ve RAM gereksinimleri
Aşağıdaki tablolar, bu dağıtım seçeneğinin her bir rolünü çalıştırmak için gerekli işlemcilerin sayısını ve rastgele erişim belleğini (RAM) miktarını belirtir. Bir Service Fabric tek başına kümesi minimum gereksinim önerileri için daha fazla bilgi için bkz [Service Fabric tek başına küme dağıtımınızı planlama ve hazırlama](/azure/service-fabric/service-fabric-cluster-standalone-deployment-preparation).

> [!NOTE]
> Aynı bilgisayarda diğer Microsoft yazılımları yüklüyse, sistem bu yazılım için de donanım gereksinimleriyle uyumlu olmalıdır. Diğer sunucu uygulamaları AOS ile aynı bilgisayarda yüklüyse, bu sunucu uygulamalarını 1 gigabayt (GB) RAM ile sınırlamanızı öneririz.

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

**Üretim ve korumalı alan dağıtımları için minimum boyutlandırma tahminleri\***

| Topoloji                                        | Rol                          | Örneklerin sayısı |
|-------------------------------------------------|-------------------------------|---------------------|
| Üretim                                      | AOS (Veri yönetimi, Toplu iş)  | 3                   |
|                                                 | Yönetim Raporlayıcısı           | 2                   |
|                                                 | SQL Server Reporting Services | 1                   |
|                                                 | Düzenleyici\*\*              | 3                   |
| Korumalı alan                                         | AOS, Veri yönetimi, Toplu iş   | 2                   |
|                                                 | Yönetim Raporlayıcısı           | 1                   |
|                                                 | SQL Server Reporting Services | 1                   |
|                                                 | Düzenleyici                  | 3                   |
| *Üretim ve korumalı alan topolojileri özeti* |                               | *16*                |

\* Bu tablodaki sayılar önizleme müşterilerimiz tarafından doğrulanır ve bu müşterilerden gelen geribildirimler doğrultusunda değiştirilebilir.

\*\* Orchestrator birincil düğüm türü olarak atanmıştır ve Service Fabric hizmetlerini de çalıştırmak üzere kullanılır.

**Arka uç SQL Server and AD DS için ilk tahminler**

<table>
<thead>
<tr>
<th></th>
<th>Rol</th>
<th>VM'ler/örnekler</th>
<th>Çekirdekler</th>
<th>Toplam çekirdekler</th>
<th>Örnek başına bellek (GB)</th>
<th>Toplam bellek (GB)</th>
</tr>
</thead>
<tbody>
<tr>
<td rowspan="3"><strong>Paylaşılan alt yapı</strong></td>
<td>SQL Server*</td>
<td>2</td>
<td>8</td>
<td>16</td>
<td>32</td>
<td>64</td>
</tr>
<tr>
<td>Dosya sunucusu/Depolama alanı ağı/Yüksek oranda kullanılabilir depolama</td>
<td colspan="5"><p>Arka uç depolama, bir çalışma zamanı depolama alan ağı (SAN) üzerindeki katı hal sürücülerine (SSD) dayalı olmalıdır.</p>
<p>Saniyedeki boyut ve giriş/çıkış işlemleri (IOPS) işlem hacmi, iş yükünün boyutuna dayanır.</p></td>
</tr>
<tr>
<td>Active Directory</td>
<td>3</td>
<td>4</td>
<td>12</td>
<td>16</td>
<td>48</td>
</tr>
<tr>
<td><em>Paylaşılan alt yapı özeti</em></td>
<td></td>
<td><em>5</em></td>
<td></td>
<td><em>28</em></td>
<td></td>
<td><em>112</em></td>
</tr>
</tbody>
</table>

\*SQL Server boyutları iş yüklerine yüksek oranda bağlıdır. Daha fazla bilgi için bkz. [Şirket içi ortamlar donanım boyutlandırma](hardware-sizing-on-premises-environments.md).

## <a name="storage"></a>Depolama

- **AOS** – Finance and Operations (şirket içi) yapılandırılmamış veriyi depolamak için bir Server Message Block (SMB) 3.0 paylaşımını kullanır. Daha fazla bilgi için bkz [Windows Server 2016 içinde Storage Spaces Direct](/windows-server/storage/storage-spaces/storage-spaces-direct-overview).
- **SQL** – Aşağıdaki seçenekler uygundur:

    - Yüksek oranda kullanılabilir bir SSD kurulumu
    - Çevrimiçi hareket işleme (OLTP) iş çıkarma yeteneği için optimize edilmiş bir SAN
    - Yüksek performans doğrudan bağlantılı depolama (DAS) 

- **SQL Server ve veri yönetimi IOPS** – Hem veri yönetimi hem de SQL Server için depolamanı en az saniyede 2.000 IOPS'a sahip olması gerekir. Üretim IOPS birçok etmene bağlıdır. Daha fazla bilgi için bkz. [Şirket içi ortamlar donanım boyutlandırma](hardware-sizing-on-premises-environments.md).
- **VM IOPS** – Her bir VM, en az 100 IOPS'a sahip olmalıdır.

## <a name="virtual-host-requirements"></a>Sanal ana makine gereksinimleri
Finance and Operations (şirket içi) ortamı için sanal ana bilgisayarlar ayarlamak istiyorsanız aşağıdaki kılavuzlara bkz.: [Service Fabric kümenizi planlama ve hazırlama](/azure/service-fabric/service-fabric-cluster-standalone-deployment-preparation) ve [Bir service fabric kümesini açıklama](/azure/service-fabric/service-fabric-cluster-resource-manager-cluster-description). Her sanal ana bilgisayar boyutlandırılacak altyapı için yeterli çekirdeğe sahip olmalıdır. SQL Server'ın fiziksel donanım üzerinde bulunduğu çoklu gelişmiş yapılandırmalar mümkündür ancak geri kalan her şey sanallaştırılmıştır. SQL Server sanallaştırılmış ise, disk alt sisteminde hızlı bir SAN veya eşdeğer olmalıdır. Her durumda, sanal ana bilgisayarın temel kurulumunun yüksek oranda kullanılabilir ve yedekli olduğundan emin olun. Sanallaştırılma kullanılan her durumda VM anlık görüntüleri alınmamalıdır.

## <a name="software-requirements-for-all-server-computers"></a>Tüm sunucu bilgisayarları için yazılım gereksinimleri
Aşağıdaki yazılım Finance and Operations (şirket içi) bileşenlerin yüklenebilmesi için bilgisayarda mevcut olmalıdır.

- The Microsoft .NET Framework sürüm 4.5.1 veya daha sonrası
- Service Fabric

Daha fazla bilgi için bkz. [Service Fabric kümenizi hazırlayın ve planlayın](/azure/service-fabric/service-fabric-cluster-standalone-deployment-preparation).

## <a name="supported-server-operating-systems"></a>Desteklenen sunucu işletim sistemleri
Aşağıdaki tablo Finance and Operations bileşenleri için desteklenen sunucu işletim sistemlerini listeler.

| İşletim sistemi                                     | Notlar |
|------------------------------------------------------|-------|
| Microsoft Windows Server 2016 Veri Merkezi veya Standart | Bu gereksinimler AOS'yi barındıran veritabanı ve Service Fabri kümesi içindir. |

## <a name="software-requirements-for-database-servers"></a>Veritabanı sunucuları için yazılım gereksinimleri

- SQL Server 2016'nın yalnızca 64-bit sürümleri desteklenir.
- Bir üretim ortamında, kullandığınız SQL Server sürümü için en son toplu güncelleştirmeyi (CU) yüklemenizi öneririz.
- Finance and Operations (şirket içi) büyük küçük harfe duyarlı olmayan, aksana duyarlı olan, kana duyarlı olan ve genişliğe duyarlı olmayan Unicode harmanlamalarını destekler. Harmanlama AOS örneklerini çalıştıran bilgisayarların Windows yerel alfabeleri ile aynı olmalıdır. Yeni bir yükleme ayarlıyorsanız, SQL Server harmanlaması yerine Windows harmanlamasını seçmenizi öneririz. Bir SQL Sunucu veritabanı için bir harmanlam seçmek hakkında daha fazla bilgi için bkz. [SQL Server belgeleri](/sql/sql-server/sql-server-technical-documentation).

Aşağıdaki tablo Finance and Operations veritabanları için desteklenen SQL Server sürümlerini listeler. Daha fazla bilgi için, [SQL Server](https://www.microsoft.com/en-us/sql-server/sql-server-2016) minimum donanım gereksinimlerine göz atın.

| Gereksinim                                                      | Notlar |
|------------------------------------------------------------------|-------|
| Microsoft SQL Server 2016 Standard Edition veya Enterprise Edition | SQL Server 2016 donanım gereksinimleri için bkz. [SQL Server 2016 yüklemek için Donanım ve Yazılım Gereksinimleri](/sql/sql-server/install/hardware-and-software-requirements-for-installing-sql-server). |

## <a name="software-requirements-for-application-object-server-aos"></a>Uygulama Nesne Sunucusu (AOS) için yazılım gereksinimleri 
- SQL Server Integation Services (SSIS)

## <a name="software-requirements-for-reporting-server-bi"></a>Raporlama Sunucusu için yazılım gereksinimleri (BI)
- SQL Server Reporting Services (SSRS)

## <a name="software-requirements-for-client-computers"></a>İstemci bilgisayarları için yazılım gereksinimleri
Finance and Operations web uygulaması HTML 5.0 uyumlu web tarayıcısına sahip herhangi bir cihazda çalışabilir. Microsoft'un onaylamış olduğu belirli cihaz/tarayıcı kombinasyonlarından bazıları şunlardır:

- Windows 10 üzerinde Microsoft Edge (son genel olarak yayımlanmış sürüm)
- Windows 10, Windows 8.1 veya Windows 7 üzerinde Internet Explorer 11
- Windows 10, Windows 8.1, Windows 8, Windows 7 veya Google Nexus 10 tablet üzerinde Google Chrome (son genel olarak yayımlanan sürümü)
- Mac OS X 10.10 (Yosemite), 10.11 (El Capitan) ve 10.12 (Sierra) veya Apple iPad üzerinde Apple Safari (son genel olarak yayınlanmış sürüm)

## <a name="software-requirements-for-active-directory-federation-services"></a>Active Directory Federasyon Hizmetleri için yazılım gereksinimleri 
Windows Server 2016 üzerinde Active Directory Federation Services (AD FS) gereklidir.

Etki alanı denetleyicisi 2012 R2 veya daha büyük etki alanı işlev düzeyine sahip Windows Server 2012 R2 veya üzeri olmalıdır. Etki alanı işlev düzeyleri hakkında daha fazla bilgi için aşağıdaki sayfalara bakınız:

- [Active Directory İşlevsellik düzeyleri nedir](https://technet.microsoft.com/en-us/library/cc787290(v=ws.10).aspx)
- [Active Directory Etki alanı hizmetleri işlev düzeyini anlamak](https://technet.microsoft.com/en-us/library/understanding-active-directory-functional-levels(v=ws.10).aspx)

## <a name="supported-microsoft-office-applications"></a>Desteklenen Microsoft Office uygulamaları
Aşağıdaki Microsoft Office uygulamaları Finance and Operations şirket içi dağıtımlarında bulutta desteklenir.

-   Microsoft Excel ve Microsoft Word eklentilerini çalıştırmak için Windows veya Mac için Microsoft Office 2016'yı yüklemiş olmanız gerekir. Sürüm gereksinimleri hakkında daha fazla bilgi için bkz. [Office tümleştirme sorunlarını giderme](../../dev-itpro/office-integration/office-integration-troubleshooting.md).
-   Excel'e Aktar veya Word'e Aktar işleviyle oluşturulan belgeleri görüntülemek için Microsoft Office 2007 veya sonraki bir sürümü yüklemiş olmanız gerekir.
 
## <a name="hardware-and-software-requirements-for-retail-components"></a>Perakende bileşenleri için donanım ve yazılım gereksinimleri
Şu anda, Finance and Operations (şirket içi) Perakende bileşenlerini içermez.

