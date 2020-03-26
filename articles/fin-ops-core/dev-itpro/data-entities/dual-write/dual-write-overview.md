---
title: Çift yazmaya genel bakış
description: Bu konu, Çift yazılabilir bir genel bakış içermektedir. Çift yazım, Microsoft Dynamics 365 modele dayalı uygulamalar ve Finance and Operations uygulamalar arasında yakın zamanda gerçek zamanlı etkileşim sağlayan bir altyapıdır.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 02/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: c4a643d4981364cea5b549118c201ac8a9798e02
ms.sourcegitcommit: 141e0239b6310ab4a6a775bc0997120c31634f79
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/10/2020
ms.locfileid: "3113886"
---
# <a name="dual-write-overview"></a>Çift yazmaya genel bakış

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

## <a name="what-is-dual-write"></a>Çift yazma nedşr?

Çift yazım, Microsoft Dynamics 365 ve Finance and Operations uygulamalardaki modele dayalı uygulamalar arasında yakın zamanda gerçek zamanlı etkileşim sağlayan bir altyapıdır. Müşteriler, ürünler, kişiler ve işlemlerle ilgili veriler, uygulama sınırlarının ötesinde akar, bir kuruluştaki tüm bölümler korunur.

Çift-yazma, Finance and Operations uygulamalar ve Common Data Service arasında sıkı şekilde bağlanmış, çift yönlü tümleştirme sağlar. Finance and Operations uygulamalardaki tüm veri değişiklikleri Common Data Service'e yazmaya neden olur ve Common Data Service'deki tüm veri değişiklikleri Finance and Operations uygulamalara yazmaya neden olur. Bu otomatik veri akışı, uygulamalar arasında tümleşik bir kullanıcı deneyimi sağlar.

![Uygulamalar arasında veri ilişkisi](media/dual-write-overview.jpg)

Çift yazıış iki yönden sahiptir : *altyapı* yönü ve *uygulama* en yönü.

### <a name="infrastructure"></a>Altyapı

Çift-yazılır altyapı genişletilebilir ve güvenilirdir ve aşağıdaki önemli özellikleri içerir:

+ Uygulamalar arasında eşzamanlı ve çift yönlü veri akışı
+ Çevrimiçi ve çevrimdışı/zaman uyumsuz modlar sistemi destekleyecek şekilde yürütme, duraklatma ve yakalama modlarıyla birlikte eşitleme.
+ Uygulamalar arasında ilk verileri eşitleme yeteneği
+ Veri yöneticileri için etkinliğin birleştirilmiş görünümü ve hata günlükleri
+ Özel uyarıları ve eşikleri konfigüre etme ve bildirimlere abone olma yeteneği
+ Filtreleme ve dönüşümler için sezgisel kullanıcı arabirimi (UI)
+ Varlık bağımlılıklarını ve ilişkilerini ayarlama ve görüntüleme yeteneği
+ Standart ve özel varlıklar ve haritalar için genişletilebilirlik
+ Güvenilir uygulama yaşam döngüsü yönetimi
+ Yeni müşteriler için kutulu kurulum deneyimi

### <a name="application"></a>Uygulama

Çift-yazıma, Dynamics 365'te bulunan model kullanımlı uygulamalardaki Finance and Operations uygulama ve kavramlar arasında bir eşleme oluşturur. Bu tümleştirme aşağıdaki senaryoları destekler:

+ Tümleşik müşteri aslı
+ Müşteri bağlılık programı kartlarına ve ödül noktalarına erişim
+ Birleşik ürün uzmanlaşma deneyimi
+ Organizasyon hiyerarşisi farkındalığı
+ Tümleşik satıcı aslı
+ Finans ve vergi referans verilerine erişim
+ İsteğe bağlı fiyat altyapısı deneyimi
+ Tümleşik aday müşteri-nakit deneyimi
+ Alan aracıları aracılığıyla hem şirket içi kıymetler hem de müşteri varlıklarını kullanabilme olanağı
+ Entegre temin-ödeme deneyimi
+ Müşteri verileri ve belgeleri ile ilgili tümleşik etkinlikler ve notlar
+ Eldeki stok kullanılabilirliğini ve ayrıntılarını arama yeteneği
+ Proje-nakit deneyimi
+ Parti kavramıyla birden çok adres ve rolü işleyebilme yeteneği
+ Kullanıcılar için tek kaynak yönetimi
+ Perakendecilik ve pazarlama için tümleşik kanallar
+ Promosyonlar ve indirimler ile görünürlük
+ Servis isteği işlevleri
+ Kolaylaştırılmış servis işlemleri

## <a name="top-reasons-to-use-dual-write"></a>Çift-yazma kullanmanın başlıca nedenleri

Çift-yazılır, Microsoft Dynamics 365 uygulama arasında veri tümleştirmesi sağlar. Bu güçlü çerçeve, ortamları birbirine bağlar ve farklı iş uygulamalarının birlikte çalışmasını sağlar. Çift-yazmayı kullanmanız gereken başlıca nedenler şunlardır:

+ Çift-yazılır, Dynamics 365'deki modele dayalı uygulamalar ve Finance and Operations uygulamaları arasında sıkı şekilde bağlanmış, yakın zamanda ve çift yönlü bütünleştirme sağlar. Bu bütünleşme, Microsoft Dynamics 365 tüm iş çözümleri için tek durduran mağaza yapar. Müşteri İlişkileri Yönetimi (CRM) için Microsoft dışı çözümler kullanan ancak Dynamics 365 Finance ve Dynamics 365 Supply Chain Management kullanan müşteriler çift yaz desteği için Dynamics 365'e doğru hareket ettirillerdir.
+ Müşteriler, ürünler, operasyonlar, projeler ve bunların Internet bilgileri (IoT), otomatik olarak çift-yazılabilir olarak Common Data Service'e akar. Bu bağlantı, Microsoft Power Platform uzantıları ile ilgilenen işletmeler için çok yararlıdır.
+ Çift-yazılır altyapı, No-Code/Low-Code ilkesini izler. Standart tablo-tablo eşlemelerini genişletmek ve özel eşlemeler eklemek için minimal mühendislik çaba gereklidir.
+ Çift yazım, hem çevrimiçi modu, hem de çevrimdışı modu destekler. Microsoft, çevrimiçi ve çevrimdışı modlar için destek sunan tek şirkettir.

## <a name="what-does-dual-write-mean-for-users-and-architects-of-crm-products"></a>CRM ürünlerinin kullanıcıları ve mimarları için çift-yazılır ortalama nedir?

Çift-yazılır Finance and Operations uygulamaları ve Common Data Service arasında veri akışını otomatikleştirir. Gelecek sürümlerde, Dynamics 365 model temelli uygulamalardaki kavramlar (örneğin, müşteri, ilgili kişi, teklif, ve sipariş), orta ölçekli ve büyük ölçekli pazar müşterilerine göre ölçeklenir.

İlk sürümde, otomasyonun çoğu çift-yazılır çözümler tarafından işlenir. Gelecek sürümlerde, bu çözümler bir Common Data Service parçası olacak. Yaklaşan değişikliklerini anlayarak, kendi Common Data Service çalışmalarınızı uzun vadeye kaydedebilirsiniz. Önemli değişikliklerden bazıları şunlardır:

+ Common Data Service şirket ve parti gibi yeni kavramlar olacaktır. Bu kavramlar Dynamics 365 Sales, Dynamics 365 Marketing, Dynamics 365 Customer Service ve Dynamics 365 Field Service gibi Common Data Service'e yerleşik tüm uygulamaları etkiler.
+ Aktiviteler ve notlar, C1S (sistemin kullanıcılarını) ve C2s (sistemin müşterileri) desteklenmesi için birleştirilmiş ve genişletilmiştir.
+ Common Data Service'teki yaklaşan değişikliklerden bazıları şunlardır:

    - Ondalık veri türü, para veri türünün yerini alacaktır.
    - Tarih etkililiği, aynı yerde geçmiş, şimdiki ve gelecekteki verileri destekleyecaktır.
    - Para birimi ve Döviz Kurları için daha fazla destek ve **Döviz Kuru** uygulama programlama arabirimi (API) gözden geçirilmesi gerekir.
    - Birim dönüştürmeleri destekedilecek.

Yaklaşan değişiklikler hakkında daha fazla bilgi için, [Common Data Service'deki veriler: aşama 1 ve 2](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/finance-operations-crossapp-capabilities/data-common-data-service-phase-1)'ye bakın.
