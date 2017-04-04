---
title: Sistem gereksinimleri
description: "Bu konu Microsoft Dynamics 365 işlemleri için geçerli sürümünün sistem gereksinimleri listelenir."
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

Bu konu Microsoft Dynamics 365 işlemleri için geçerli sürümünün sistem gereksinimleri listelenir.

<a name="supported-web-browsers"></a>Desteklenen web tarayıcıları
----------------------

Microsoft Dynamics 365 işlemleri web uygulaması için belirtilen işletim sistemleri üzerinde çalışan aşağıdaki web tarayıcılardan birinde çalıştırabilirsiniz:

-   Microsoft Edge (son sürüm bulunabilen) üzerinde Windows 10
-   Windows 10, Windows 8.1 veya Windows 7 üzerinde Internet Explorer 11
-   Google Chrome (son sürüm bulunabilen) Windows 10, Windows 8.1, Windows 8, Windows 7 veya Google Nexus 10 Tablet
-   Apple Safari (son sürüm bulunabilen) Mac OS X (Yosemite) 10.10, 10.11 (El Capitan) veya 10,12 (Sierra) veya Apple iPad üzerinde

Her web tarayıcısı için en son sürümü bulmak için, yazılım üreticisinin web sitesine gidin. **Notlar:**

-   Görev kaydediciden oluşturulur ve bunları Microsoft Word belgelerine dahil görüntüleri yakalamak için yüklü bir Chrome uzantısı olmalıdır. <!---For instructions about how to install the extension, see [Screenshot Extension setup](/dynamics365/operations/dev-itpro/user-interface/task-recorder).-->
-   Bir ClickOnce uygulaması olarak iş akışı Düzenleyicisi başlatılır. Yalnızca Microsoft Edge ve Internet Explorer (Microsoft Windows'un desteklenen bir sürümü), ClickOnce uygulamalarını destekler. İş akışı Düzenleyicisi ClickOnce uygulaması 64-bit uyumlu bir işletim sistemi gerektirir.
-   Finansal raporlama için Rapor Tasarımcısı bir ClickOnce uygulaması başlatıldı. 64-bit uyumlu bir işletim sistemi gerektirir. Krom kullanıyorsanız, Rapor Tasarımcısı istemci yüklemek için ClickOnce uzantısı yüklemeniz gerekir. Krom ile incognito mod kullanıyorsanız, ClickOnce uzantısı için incognito modu etkin olduğundan emin olun.

### <a name="supported-web-browsers-for-retail-cloud-pos"></a>Perakende Bulut POS'u için desteklenen web tarayıcıları

Perakende bulut POS işlemleri için Dynamics 365 için belirtilen işletim sistemleri üzerinde çalışan aşağıdaki web tarayıcılardan birinde çalıştırabilirsiniz:

-   Microsoft Edge (son sürüm bulunabilen) üzerinde Windows 10
-   Windows 10, Windows 8.1 veya Windows 7 üzerinde Internet Explorer 11
-   Krom (son sürüm bulunabilen) Windows 10, Windows 8.1 veya Windows 7

## <a name="network-requirements"></a>Ağ gereksinimleri
-   Dynamics 365 işlemleri için 150'den daha az milisaniye (ms) gecikme süresi ile ağlar için tasarlanmıştır. Bu bir tarayıcı istemci işlemleri için Dynamics 365 barındıran Microsoft Azure veri merkezine gecikme olur. Ağ gecikmesi sırasında sınamanızı öneririz <http://www.azurespeed.com>.
-   Dynamics 365 işlemleri için bant genişliği gereksinimleri, senaryoya bağlıdır. En tipik senaryolar birden fazla 50 KB / saniye (KBps) olan bir bant genişliği gerektirir. Ancak, çalışma veya kapsamlı özelleştirme ilgili senaryolar gibi yüksek yük gereksinimlerin senaryoları için daha fazla bant genişliği önerilir.

Genel olarak, Dynamics 365 işlemleri için Internet için optimize edilmiştir. Azure veri merkezine gidiş gelişlerini bir tarayıcı istemci sayısı oldukça küçüktür ve tüm yükü sıkıştırılmış. **Uyarı:** göre en düşük bant genişliği gereksinimlerini kullanıcı sayısını çarparak istemci konumdan bant genişliği gereksinimlerini hesaplamak yoktur. Verilen bir konuma eşzamanlı kullanımını hesaplamak çok zordur. Bant genişliği gereksinimleri hakkında endişe olan müşteriler için operasyonlar için Dynamics 365 önizleme sürümünü kullanın.

## <a name="net-framework-requirements"></a>.NET framework gereksinimleri
Dynamics 365 işlemleri için .NET Framework sürüm 4.6.2 için tüm tıklatın gerektirir-kez belge yönlendirme aracı gibi uygulamalar. Yükleme yönergeleri için bkz: [.NET Framework yükleme](https://msdn.microsoft.com/en-us/library/5a4x27ek(v=vs.110).aspx).

## <a name="supported-microsoft-office-applications"></a>Desteklenen Microsoft Office uygulamaları
-   Yüklü Mac veya Microsoft Excel ve Word eklentileri çalıştırmak için Windows için Microsoft Office 2016 olmalıdır. Sürüm gereksinimleri hakkında daha fazla bilgi için bkz: [Office tümleştirme sorunlarını giderme](/dynamics365/operations/dev-itpro/office-integration/office-integration-troubleshooting).
-   Excel'e veya Word işlevine verme tarafından oluşturulan belgeleri görüntülemek için Microsoft Office 2007 olmalıdır veya sonraki bir sürümü yüklü.

## <a name="retail-modern-pos-requirements"></a>Perakende Modern POS gereksinimleri
### <a name="supported-operating-systems"></a>Desteklenen işletim sistemleri

-   Modern POS perakende 32 bitlik bir uygulama olmakla birlikte, hem x86 hem de x64 mimarileri üzerinde çalışır.
-   Modern POS perakende yalnızca Windows 10 Pro, kurumsal ve kurumsal uzun vadeli hizmet dalı (LTSB) sürümlerinde desteklenir.

### <a name="minimum-system-requirements"></a>Minimum sistem gereksinimleri

-   Desteklenen en düşük çözünürlüğü 1280 × 1024 ' dir.
-   Modern perakende POS üzerinde çalıştığı bilgisayarın aşağıdaki gereksinimleri karşılaması gerekir:
    -   Bu, en azından inden az 2 gigahertz at (GHz) çalışan bir çift çekirdekli işlemci olmalıdır.
    -   Bu, en azından, 3 gigabayta (GB) RAM olması gerekir.
    -   Internet erişimi olması gerekir.

## <a name="retail-hardware-station-requirements"></a>Perakende istasyonu için gerekli donanım
### <a name="supported-operating-systems"></a>Desteklenen işletim sistemleri

-   Perakende donanım istasyonu 32 bitlik bir uygulama olmakla birlikte, hem x86 hem de x64 mimarileri üzerinde çalışır.
-   Perakende donanım istasyon aşağıdaki işletim sistemlerinde desteklenir:
    -   Windows 7 Professional, Enterprise ve Ultimate sürümlerinde **Not:** Windows 7, yalnızca Internet Explorer 11 sistem üzerinde el ile yüklüyse desteklenir.
    -   Katıştırılmış Windows 8.1 güncelleştirmesini 1 Professional ve Enterprise sürümleri
    -   Windows 10 Pro, kurumsal ve kurumsal LTSB sürümleri

### <a name="minimum-system-requirements"></a>Minimum sistem gereksinimleri

Bilgisayara yükleyip aşağıdaki öğeleri kullanarak tüm sistem gereksinimleri karşılaması gerekir:

-   Internet Information Services (IIS)
-   Üçüncü taraf donanım

## <a name="retail-store-scale-unit-requirements"></a>Perakende Mağaza ölçek birimi gereksinimleri
### <a name="supported-operating-systems"></a>Desteklenen işletim sistemleri

-   Perakende Mağaza ölçek birimini 32 bitlik bir uygulama olmakla birlikte, hem x86 hem de x64 mimarileri üzerinde çalışır.
-   Perakende Mağaza ölçek birimi aşağıdaki işletim sistemlerinde desteklenir:
    -   Windows 7 Professional, Enterprise ve Ultimate sürümlerinde
    -   Katıştırılmış Windows 8.1 güncelleştirmesini 1 Professional ve Enterprise sürümleri
    -   Windows 10 Pro, kurumsal ve kurumsal LTSB sürümleri

### <a name="minimum-system-requirements"></a>Minimum sistem gereksinimleri

-   4 GB RAM
-   1,6 GHz çekirdek başına en yüksek CPU hızı (iki çekirdeği olan minimum.)
-   En az 10 GB boş alan (kanal veritabanı büyük miktarda boş alan gerekebilir.)

### <a name="recommended-system-requirements"></a>Önerilen sistem gereksinimleri

-   6 GB RAM
-   2.4 GHz i7 (veya eşdeğeri) en yüksek CPU hızı çekirdek (dört çekirdek önerilir.)
-   En az 10 GB boş alan (kanal veritabanı büyük miktarda boş alan gerekebilir.)

## <a name="requirements-for-development-on-local-vms"></a>Yerel VMs üzerinde geliştirme gereksinimleri
Yerel sanal makinelerde (VMs) geliştirme gereksinimleri hakkında bilgi için bkz: [VM yerinde çalışan](/dynamics365/operations/dev-itpro/dev-tools/access-instances#vm-that-is-running-in-premises).

<a name="see-also"></a>Ayrıca bkz.
--------

[Dynamics 365 değerlendirme kopyasının işlemleri için Al](/dynamics365/operations/dev-itpro/dev-tools/get-evaluation-copy)


