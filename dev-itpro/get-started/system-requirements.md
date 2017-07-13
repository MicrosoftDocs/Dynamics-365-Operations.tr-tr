---
title: Sistem gereksinimleri
description: "Bu konuda Microsoft Dynamics 365 Finance and Operations, Enterprise Edition&quot;ın geçerli sürümü için sistem gereksinimleri belirtilmektedir."
author: sericks007
manager: AnnBe
ms.date: 06/16/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, Developer, IT Pro
ms.search.scope: Core
ms.custom: 55651
ms.assetid: e564d51d-42d3-47c5-b388-93b8219c692a
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2016-08-30
ms.dyn365.ops.version: Platform update 2
ms.translationtype: Human Translation
ms.sourcegitcommit: 869151f2486b7a481e4694cfb6992d0ee2cfc008
ms.openlocfilehash: 724ee7ec29f8a9c4e8cc0b244193cd6c83c37f03
ms.contentlocale: tr-tr
ms.lasthandoff: 06/13/2017


---

# <a name="system-requirements"></a>Sistem gereksinimleri

[!include[banner](../includes/banner.md)]


Bu konuda Microsoft Dynamics 365 Finance and Operations, Enterprise Edition'ın geçerli sürümü için sistem gereksinimleri belirtilmektedir.

<a name="supported-web-browsers"></a>Desteklenen web tarayıcıları
----------------------

Web uygulamasını belirtilen işletim sistemleri üzerinde çalışan aşağıdaki web tarayıcılarından birinde çalıştırabilirsiniz:

-   Windows 10 üzerinde Microsoft Edge (son genel olarak yayımlanmış sürüm)
-   Windows 10, Windows 8.1 veya Windows 7 üzerinde Internet Explorer 11
-   Windows 10, Windows 8.1, Windows 8, Windows 7 veya Google Nexus 10 tablet üzerinde Google Chrome (son genel olarak yayımlanan sürümü)
-   Mac OS X 10.10 (Yosemite), 10.11 (El Capitan) ve 10.12 (Sierra) veya Apple iPad üzerinde Apple Safari (son genel olarak yayınlanmış sürüm)

Her web tarayıcısı için en son sürümü bulmak için, yazılım üreticisinin web sitesine gidin. 

**Notlar:**

-   Görev Kaydedici'den ekran görüntülerinin alınmasına ve bunların oluşturulan Microsoft Word belgelerine eklenmesine izin vermek için bir önceden yayınlanmış Chrome eklentisinin yüklü olması gerekir. <!---For instructions about how to install the extension, see [Screenshot Extension setup](/dynamics365/unified-operations/dev-itpro/user-interface/task-recorder).-->
-   İş Akışı Düzenleyicisi bir ClickOnce uygulaması olarak başlatılır. ClickOnce uygulamalarını yalnızca Microsoft Edge ve Internet Explorer (Microsoft Windows'un desteklenen bir sürümünde) destekler. İş Akışı Düzenleyicisi ClickOnce uygulaması için 64-bit uyumlu bir işletim sistemi gereklidir.
-   Finansal raporlama için Rapor Tasarımcısı bir ClickOnce uygulaması olarak başlatılır. 64-bit uyumlu bir işletim sistemi gerektirir. Chrome kullanıyorsanız, rapor tasarımcısı istemcisini indirebilmek için ClickOnce eklentisini yüklemeniz gerekir. Chrome'u gizli modda kullanıyorsanız, ClickOnce uzantısının da gizli mod için etkinleştirildiğinden emin olun.
-   PDF dosyalarının önizlemesini yapmak için (en son sürüm genel kullanıma açık) Windows 10 üzerinde, Microsoft Edge veya (en son sürüm genel kullanıma açık) Windows 10, Windows 8.1, Windows 8, Windows 7 veya Google Nexus 10 tablet üzerinde Google Chrome gibi tarayıcıları kullanmanızı öneririz.


### <a name="supported-web-browsers-for-retail-cloud-pos"></a>Perakende Bulut POS'u için desteklenen web tarayıcıları

Retail Cloud POS belirtilen işletim sistemleri üzerinde çalışan aşağıdaki web tarayıcılarından birinde çalıştırılabilir:

-   Windows 10 üzerinde Microsoft Edge (son genel olarak yayımlanmış sürüm)
-   Windows 10, Windows 8.1 veya Windows 7 üzerinde Internet Explorer 11
-   Windows 10, Windows 8.1 veya Windows 7 üzerinde Chrome (son genel olarak yayımlanmış sürüm)

## <a name="network-requirements"></a>Ağ gereksinimleri
-   Dynamics 365 for Finance and Operations, Enterprise Edition 250-300 milisaniye (ms) veya daha az gecikmeli ağlar için tasarlanmıştır. Bu gecikme, bir tarayıcı istemcisinden Finance and Operations'ı barındıran Microsoft Azure veri merkezine iletim süresidir. Ağ gecikmesini <http://www.azurespeed.com>'da sınamanızı öneririz.
-   Bant genişliği gereksinimlerini senaryoya bağlıdır. En tipik senaryolar 50 kilobayt/saniye (KBps) üzerinde bir bant genişliği gerektirir. Ancak, kapsamlı özelleştirme içeren çalışma alanları veya senaryolar gibi yüksek yük gereksinimleri olan senaryolar için daha yüksek bant genişliği önerilir.

Genel olarak, Finance and Operations Internet için optimize edilmiştir. Bir tarayıcı istemcisinden Azure veri merkezine gidiş dönüş sayısı küçüktür ve tüm yükü sıkıştırılmıştır. 

**Uyarı:** Kullanıcı sayısıyla minimum bant genişliği gereksinimlerini çarpıp bir müşteri konumundan bant genişliği gereksinimlerini hesaplamayın. Belirli bir konumun eşzamanlı kullanımını hesaplamak zordur. Bant genişliği gereksinimleri konusunda kaygıları olan müşteriler Finance and Operations'ın bir önizleme sürümünü kullanabilir.

## <a name="net-framework-requirements"></a>.NET Framework gereksinimleri
Belge yönlendirme aracısı gibi ClickOnce uygulamaları için .NET Framework sürüm 4.6.2 gereklidir. Yükleme yönergeleri için bkz. [.NET Framework'ü yükleme](https://msdn.microsoft.com/en-us/library/5a4x27ek(v=vs.110).aspx).

## <a name="supported-microsoft-office-applications"></a>Desteklenen Microsoft Office uygulamaları
-   Microsoft Excel ve Word eklentilerini çalıştırmak için Windows veya Mac için Microsoft Office 2016'yı yüklemiş olmanız gerekir. Sürüm gereksinimleri hakkında daha fazla bilgi için bkz. [Office tümleştirme sorunlarını giderme](/dynamics365/unified-operations/dev-itpro/office-integration/office-integration-troubleshooting).
-   Excel'e Aktar veya Word'e Aktar işleviyle oluşturulan belgeleri görüntülemek için Microsoft Office 2007 veya sonraki bir sürümü yüklemiş olmanız gerekir.

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
    -   Windows 7 Professional, Enterprise ve Ultimate sürümleri **Not:** Windows 7 ancak Internet Explorer 11 sisteme el ile yüklendiği zaman desteklenir.
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

<a name="see-also"></a>Ayrıca bkz.
--------

[Dynamics 365 for Finance and Operations, Enterprise Edition'ın değerlendirme kopyasını edinin](/dynamics365/unified-operations/dev-itpro/dev-tools/get-evaluation-copy)





