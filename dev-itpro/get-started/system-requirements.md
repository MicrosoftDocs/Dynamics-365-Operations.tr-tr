---
title: Sistem gereksinimleri
description: "Bu konuda Microsoft Dynamics 365 for Operations&quot;ın geçerli sürümü için sistem gereksinimleri belirtilmektedir."
author: sericks007
manager: AnnBe
ms.date: 2017-04-04
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User, Developer, IT Pro
ms.search.scope: Core
ms.custom: 55651
ms.assetid: e564d51d-42d3-47c5-b388-93b8219c692a
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2016-08-30
ms.dyn365.ops.version: Platform update 2
translationtype: Human Translation
ms.sourcegitcommit: c8c96dc9705688308dd4a5c720700ddc17657d75
ms.openlocfilehash: 9220c093d3f6d6700127c93651db4083be300311
ms.lasthandoff: 03/31/2017


---

# <a name="system-requirements"></a>Sistem gereksinimleri

Bu konuda Microsoft Dynamics 365 for Operations'ın geçerli sürümü için sistem gereksinimleri belirtilmektedir.

<a name="supported-web-browsers"></a>Desteklenen web tarayıcıları
----------------------

Microsoft Dynamics 365 for Operations web uygulamasını belirtilen işletim sistemleri üzerinde çalışan aşağıdaki web tarayıcılarından birinde çalıştırabilirsiniz:

-   Windows 10 üzerinde Microsoft Edge (son genel olarak yayımlanmış sürüm)
-   Windows 10, Windows 8.1 veya Windows 7 üzerinde Internet Explorer 11
-   Windows 10, Windows 8.1, Windows 8, Windows 7 veya Google Nexus 10 tablet üzerinde Google Chrome (son genel olarak yayımlanan sürümü)
-   Mac OS X 10.10 (Yosemite), 10.11 (El Capitan) ve 10.12 (Sierra) veya Apple iPad üzerinde Apple Safari (son genel olarak yayınlanmış sürüm)

Her web tarayıcısı için en son sürümü bulmak için, yazılım üreticisinin web sitesine gidin. **Notlar:**

-   Görev Kaydedici'den oluşturulmuş görüntüleri yakalamak ve bunları Microsoft Word belgelerine eklemek için bir Chrome eklentisinin yüklü olması gerekir. <!---For instructions about how to install the extension, see [Screenshot Extension setup](/dynamics365/operations/dev-itpro/user-interface/task-recorder).-->
-   İş Akışı Düzenleyicisi bir ClickOnce uygulaması olarak başlatılır. ClickOnce uygulamalarını yalnızca Microsoft Edge ve Internet Explorer (Microsoft Windows'un desteklenen bir sürümünde) destekler. İş Akışı Düzenleyicisi ClickOnce uygulaması için 64-bit uyumlu bir işletim sistemi gereklidir.
-   Finansal raporlama için Rapor Tasarımcısı bir ClickOnce uygulaması olarak başlatılır. 64-bit uyumlu bir işletim sistemi gerektirir. Chrome kullanıyorsanız, rapor tasarımcısı istemcisini indirebilmek için ClickOnce eklentisini yüklemeniz gerekir. Chrome'u gizli modda kullanıyorsanız, ClickOnce uzantısının da gizli mod için etkinleştirildiğinden emin olun.

### <a name="supported-web-browsers-for-retail-cloud-pos"></a>Perakende Bulut POS'u için desteklenen web tarayıcıları

Dynamics 365 for Operations için Retail Cloud POS, belirtilen işletim sistemleri üzerinde çalışan aşağıdaki web tarayıcılarının herhangi birinde çalıştırılabilir:

-   Windows 10 üzerinde Microsoft Edge (son genel olarak yayımlanmış sürüm)
-   Windows 10, Windows 8.1 veya Windows 7 üzerinde Internet Explorer 11
-   Windows 10, Windows 8.1 veya Windows 7 üzerinde Chrome (son genel olarak yayımlanmış sürüm)

## <a name="network-requirements"></a>Ağ gereksinimleri
-   Dynamics 365 for Operations 150 milisaniyeden (ms) daha az gecikmeli ağlar için tasarlanmıştır. Bu gecikme, bir tarayıcı istemcisinden Dynamics 365 for Operations'ı barındıran Microsoft Azure veri merkezine iletim süresidir. Ağ gecikmesini <http://www.azurespeed.com>'da sınamanızı öneririz.
-   Dynamics 365 for Operations için bant genişliği gereksinimleri senaryoya bağlıdır. En tipik senaryolar 50 kilobayt/saniye (KBps) üzerinde bir bant genişliği gerektirir. Ancak, kapsamlı özelleştirme içeren çalışma alanları veya senaryolar gibi yüksek yük gereksinimleri olan senaryolar için daha yüksek bant genişliği önerilir.

Genel olarak, Dynamics 365 for Operations Internet için optimize edilmiştir. Bir tarayıcı istemcisinden Azure veri merkezine gidiş dönüş sayısı oldukça küçüktür ve tüm yükü sıkıştırılmıştır. **Uyarı:** Kullanıcı sayısıyla minimum bant genişliği gereksinimlerini çarpıp bir müşteri konumundan bant genişliği gereksinimlerini hesaplamayın. Belirli bir konumun eşzamanlı kullanımını hesaplamak çok zordur. Bant genişliği gereksinimleri konusunda kaygıları olan müşteriler Dynamics 365 for Operations'ın bir önizleme sürümünü kullanabilir.

## <a name="net-framework-requirements"></a>.NET Framework gereksinimleri
Dynamics 365 for Operations, belge yönlendirme aracısı gibi ClickOnce uygulamaları için .NET Framework sürüm 4.6.2 gerektirir. Yükleme yönergeleri için bkz. [.NET Framework'ü yükleme](https://msdn.microsoft.com/en-us/library/5a4x27ek(v=vs.110).aspx).

## <a name="supported-microsoft-office-applications"></a>Desteklenen Microsoft Office uygulamaları
-   Microsoft Excel ve Word eklentilerini çalıştırmak için Windows veya Mac için Microsoft Office 2016'yı yüklemiş olmanız gerekir. Sürüm gereksinimleri hakkında daha fazla bilgi için bkz. [Office tümleştirme sorunlarını giderme](/dynamics365/operations/dev-itpro/office-integration/office-integration-troubleshooting).
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

## <a name="requirements-for-development-on-local-vms"></a>Yerel VM'ler üzerinde geliştirme için gereksinimler
Yerel sanal makinelerde (VM) geliştirme için gereksinimler hakkında bilgi için bkz. [yerinde çalışan VM](/dynamics365/operations/dev-itpro/dev-tools/access-instances#vm-that-is-running-in-premises).

<a name="see-also"></a>Ayrıca bkz.
--------

[Dynamics 365 for Operations'ın değerlendirme kopyasını edinin](/dynamics365/operations/dev-itpro/dev-tools/get-evaluation-copy)


