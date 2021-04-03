---
title: Önceki sürümlerdeki kaldırılmış veya kullanım dışı bırakılmış özellikler
description: Bu konuda, kaldırılmış olan veya Dynamics 365 for Finance and Operations'dan kaldırılması planlanan özellikler açıklanmaktadır.
author: sericks007
manager: AnnBe
ms.date: 02/16/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.custom: 21821
ms.assetid: 31019808-4cbf-47d7-b1ba-d791db4281ae
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: db276c693a729b919bc609bb4b94843bb11a8fe3
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/09/2021
ms.locfileid: "5559342"
---
# <a name="removed-or-deprecated-features-in-previous-releases"></a>Önceki sürümlerdeki kaldırılmış veya kullanım dışı bırakılmış özellikler

[!include [banner](../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

> [!IMPORTANT]
> Bu konu artık güncelleştirilmeyecektir. Finance and Operations uygulamalardan kaldırılmış veya kullanımı sonlandırılmış özelliklerin geçerli listesini görmek için, kullanmakta olduğunuz uygulamayla ilgili **"Kaldırılan veya Kullanımı sonlandırılan özellikler"** içeriğini arayın.

Bu konu, Dynamics 365 for Finance and Operations'dan ve bu ürünün önceki sürümlerinden kaldırılan veya kullanımı sonlandırılan özellikleri açıklar.

- *Kaldırılan* özellik artık üründe bulunmaz.
- *Kullanımına son verilen* özellik etkin geliştirmede değildir ve sonraki güncellemede kaldırılabilir.

Bu liste, kaldırılan veya kullanımına son verilen özellikleri kendi planlamanız için göz önünde bulundurmanız amacıyla hazırlanmıştır. 

Finance and Operations uygulamlarındai nesneler hakkında ayrıntılı bilgiye [Teknik referans](https://docs.microsoft.com/dynamics/s-e/global/axtechrefrep_61) raporları altından ulaşabilirsiniz. Finance and Operations uygulamalarının her sürümünde değiştirilen veya kaldırılan nesneler hakkında bilgi edinmek için bu raporların farklı sürümlerini karşılaştırabilirsiniz.

## <a name="finance-1007-with-platform-update-31"></a>Finance 10.0.7, Platform güncelleştirmesi 31 ile

### <a name="chinese-voucher-types-without-account-groups-selection"></a>Hesap grupları seçimi içermeyen Çince fiş türleri
|&nbsp;   | &nbsp; |
|------------|--------------------|
| **Kullanımı sonlandırma/kaldırma nedeni** | Hesap grupları seçimine sahip özellik olarak değiştirildi. |
| **Başka bir özellikle mi değiştirildi?**   | Evet |
| **Etkilenen ürün alanları**         | Uygulama |
| **Dağıtım seçeneği**              | Tümü |
| **Durum**                         | Kullanım dışı: 1 Aralık 2020 itibarıyla, Hesap grupları seçimi içermeyen Çince fiş türleri kurulumunu desteklememeyi planlıyoruz. 10.0.7'deki Yenilikler'de yeni özellik tasarımı hakkında daha fazla bilgi bulun |

## <a name="finance-and-operations-1006-with-platform-update-30"></a>Finance and Operations 10.0.6, Platform güncelleştirmesi 30 ile


### <a name="dimensionhashgethashstr-_message"></a>DimensionHash.getHash(str _message)

|&nbsp;   | &nbsp; |
|------------|--------------------|
| **Kullanımı sonlandırma/kaldırma nedeni** | Windows, [SHA1 Sertifikaları için Windows Uygulaması](https://social.technet.microsoft.com/wiki/contents/articles/32288.windows-enforcement-of-sha1-certificates.aspx)'nda belgelendiği gibi SHA1'i kullanımın dışı bırakıyor.  |
| **Başka bir özellikle mi değiştirildi?**   | Evet |
| **Etkilenen ürün alanları**         | Uygulama |
| **Dağıtım seçeneği**              | Tümü |
| **Durum**                         | Kullanım dışı: 1 Nisan 2020 tarihine kadar geliştiricilerin, **HasFunction** sınıfı içinde bulunan platform API'lerini kullanmaları gerekir. |

### <a name="hashcomputesha1hashstring-message"></a>Hash.ComputeSHA1Hash(dize iletisi)

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Kullanımı sonlandırma/kaldırma nedeni** | Windows, [SHA1 Sertifikaları için Windows Uygulaması](https://social.technet.microsoft.com/wiki/contents/articles/32288.windows-enforcement-of-sha1-certificates.aspx)'nda belgelendiği gibi SHA1'i kullanımın dışı bırakıyor.  |
| **Başka bir özellikle mi değiştirildi?**   | Evet |
| **Etkilenen ürün alanları**         | Platform |
| **Dağıtım seçeneği**              | Tümü |
| **Durum**                         | Kullanım dışı: 1 Nisan 2020 tarihine kadar geliştiricilerin, **HasFunction** sınıfı içinde bulunan platform API'lerini kullanmaları gerekir. |


### <a name="formdatetimecontrolsetutcstring"></a>FormDateTimeControl.setUtcString()

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Kullanımı sonlandırma/kaldırma nedeni** | Yerine daha iyi bir yöntem bulunduğundan **setUtcString()** yöntemini kullanımdan çekiyoruz. |
| **Başka bir özellikle mi değiştirildi?**   | Evet |
| **Etkilenen ürün alanları**         | Platform |
| **Dağıtım seçeneği**              | Tümü |
| **Durum**                         | Kullanımına son verildi: 1 Ekim 2020 itibarıyla **setUtcString()** yöntemini desteklememeyi planlıyoruz. Geliştiriciler bunun yerine **setUtcDateTime()** yöntemini kullanmalıdır. |

### <a name="blacklist-report-it--feature-reference-it-00001"></a>Bloke liste raporu (IT) – Özellik referansı IT-00001

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Kullanımı sonlandırma/kaldırma nedeni** | Yasal olarak gerekli değildir. |
| **Başka bir özellikle mi değiştirildi?**   | Hayır |
| **Etkilenen ürün alanları**         | İtalyanca yerelleştirme |
| **Dağıtım seçeneği**              | Tümü |
| **Durum**                         | Kullanımına son verildi: 1 Ekim 2020 itibarıyla **Bloke liste raporu (IT) – Özellik referansı IT-00001** özelliğini desteklememeyi planlıyoruz. |

### <a name="domestic-tax-report--feature-reference-it-00003"></a>Yurtiçi vergi raporu – Özellik referansı IT-00003

| &nbsp;  |&nbsp;  |
|------------|--------------------|
| **Kullanımı sonlandırma/kaldırma nedeni** | Yasal olarak gerekli değildir. |
| **Başka bir özellikle mi değiştirildi?**   | Hayır |
| **Etkilenen ürün alanları**         | İtalyanca yerelleştirme |
| **Dağıtım seçeneği**              | Tümü |
| **Durum**                         | Kullanımına son verildi: 1 Ekim 2020 itibarıyla **Yurtiçi vergi raporu (IT) – Özellik referansı IT-00003** özelliğini desteklememeyi planlıyoruz. |


## <a name="finance-and-operations-1005-with-platform-update-29"></a>Finance and Operations 10.0.5, Platform güncelleştirmesi 29 ile

### <a name="us-payroll-tax-updates"></a>ABD bordro vergisi güncelleştirmeleri

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Kullanımı sonlandırma/kaldırma nedeni** | Düşük kullanım ve artık stratejik entegrasyonlar aracılığıyla sunulan gelişmiş işlevsellik nedeniyle ABD Bordro işlevselliği için vergi güncellemelerini hizmetten çıkarıyoruz.  |
| **Başka bir özellikle mi değiştirildi?**   | Evet |
| **Etkilenen ürün alanları**         | Bordro |
| **Dağıtım seçeneği**              | Tümü |
| **Durum**                         | Kullanımdan kaldırıldı: 31 Temmuz 2024 itibarıyla artık ABD Bordro müşterilerine vergi güncelleştirmeleri sağlamayacağız. İşlevsellik ürün içinde kalacaktır, ancak geliştirmeler artık işlevselliği güncel tutamaz ve herhangi bir ürün kusuru duruma göre değerlendirilecektir. |

>[!NOTE]
> Bu, 1 Ekim 2021 orijinal kullanımdan kaldırma tarihinde yapılan değişikliği temsil eder. Daha fazla bilgi için bkz. [Microsoft Dynamics 365 for Finance and Operations'ta ABD Bordro özelliği vergi güncelleştirmeleri hizmetten çıkarılıyor](https://aka.ms/financepayrollfaq).


### <a name="data-management-staging-clean-up"></a>Veri yönetimi hazırlama temizleme
|&nbsp;   | &nbsp; |
|------------|--------------------|
| **Kullanımı sonlandırma/kaldırma nedeni** | Periyodik temizleme zamanlaması için gerekli olan çekirdek gereksinimlerini karşılamadı. |
| **Başka bir özellikle mi değiştirildi?**   | Evet, senaryoları bütünsel olarak karşılamak için İş geçmişi temizleme özelliği ekleniyor. |
| **Etkilenen ürün alanları**         | Veri yönetimi |
| **Dağıtım seçeneği**              | Tümü  |
| **Durum**                         | Kaldırıldı: İşlevin kaldırılması hedeflenen zaman aralığı Aralık 2020'dir. |

## <a name="finance-and-operations-1004-with-platform-update-28"></a>Finance and Operations 10.0.4, Platform güncelleştirmesi 28 ile

### <a name="france-fec-accounting-data-export-in-xml"></a>Fransa: XML'de FEC Muhasebe veri dışa aktarma

|  &nbsp; |&nbsp;  |
|------------|--------------------|
| **Kullanımı sonlandırma/kaldırma nedeni** | TXT biçimi tarafından yeri alındı **Fransa FEC denetim dosyası**, **Genel muhasebe** \> **Periyodik görevler** \> **Veri dışa aktarma** aracılığıyla kullanılabilir.
| **Başka bir özellikle mi değiştirildi?**   | Evet |
| **Etkilenen ürün alanları**         | Genel muhasebe |
| **Dağıtım seçeneği**              | Tümü |
| **Durum**                         | Kaldırıldı. İşlevin kaldırılması hedeflenen zaman aralığı Temmuz 2020'dir. |


### <a name="legacy-navigation-bar"></a>Eski gezinti çubuğu

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Kullanımı sonlandırma/kaldırma nedeni** | Diğer Dynamics ve Office ürünleriyle başlık hizalaması. Daha fazla ayrıntı için, [Office başlığı ile hizalanan güncelleştirilmiş gezinti çubuğu](https://docs.microsoft.com/business-applications-release-notes/April19/dynamics365-finance-operations/updatednavbar).
| **Başka bir özellikle mi değiştirildi?**   | 24 platform güncelleştirmesinde başlayarak, arama özelliklerinin bulunduğu yeniden tasarlanmış bir gezinti çubuğu sunulmuştur. |
| **Etkilenen ürün alanları**         | Web istemcisi |
| **Dağıtım seçeneği**              | Tümü |
| **Durum**                         | Kaldırıldı: Nisan 2020'den itibaren, eski gezinti çubuğu kullanılamayacaktır. Bu noktaya kadar, müşteriler **İstemci performans seçenekleri** sayfası aracılığıyla eski gezinti çubuğuna dönebilirler. |


## <a name="finance-and-operations-1002-with-platform-update-26"></a>Finance and Operations 10.0.2, Platform güncelleştirmesi 26 ile


### <a name="legacy-default-action-behavior"></a>Eski varsayılan eylem davranışı

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Kullanımı sonlandırma/kaldırma nedeni** | Kılavuzlar içindeki varsayılan eylemler için eski davranış, beklenmeyen bir sütunun kılavuz sütunları kişiselleştirmeyle yeniden düzenlenmesinden sonra varsayılan eylem bağlantısına sahip olmasına neden olur. Yeni yapışkan varsayılan eylem özelliği bunu düzeltir. Daha fazla bilgi için [kılavuzları Yapışkan varsayılan eylemi](https://docs.microsoft.com/business-applications-release-notes/October18/dynamics365-finance-operations/sticky-default-action). |
| **Başka bir özellikle mi değiştirildi?**   | Platform güncelleştirmesi 21 itibariyle "yapışkan varsayılan eylemler" için bir özellik kullanıma sunulmuştur. Bu özellik, **İstemci performans seçenekleri** sayfasında etkinleştirilebilir. |
| **Etkilenen ürün alanları**         | Web istemcisindeki kılavuzlar |
| **Dağıtım seçeneği**              | Tümü |
| **Durum**                         | Kullanımdan kalktı: Nisan 2020'den itibaren, yapışkan varsayılan eylemler varsayılan davranış olacaktır, eski davranışa dönme mekanizması sunulmayacaktır. |

### <a name="legacy-is-one-of-filtering-experience"></a>Eski, "biri" filtreleme deneyimini en iyi duruma getirir

|&nbsp;   | &nbsp; |
|------------|--------------------|
| **Kullanımı sonlandırma/kaldırma nedeni** | "Bunlardan biri" filtreleme deneyimi, Platform güncelleştirmesi 22'de yeniden tasarlandı ve bunun tek "bunlardan biri" filtreleme deneyimi olması planlandı. |
| **Başka bir özellikle mi değiştirildi?**   | Platform güncelleştirmesi 22 ile başlayarak, geliştirilmiş bir "bunlardan biri" filtreleme deneyimi **İstemci performans seçenekleri** sayfasında kullanılabilir hale gelmiştir. Daha fazla bilgi için bkz. [En iyi duruma getirilen filtreleme deneyiminden biri](https://docs.microsoft.com/business-applications-release-notes/October18/dynamics365-finance-operations/improved-isoneof-filtering). |
| **Etkilenen ürün alanları**         | Web istemcisi |
| **Dağıtım seçeneği**              | Tümü |
| **Durum**                         | Kullanımdan kalktı: Nisan 2020'den itibaren, iyileştirilmiş "bunlardan biri" deneyimi varsayılan davranış olacaktır, eski davranışa dönme mekanizması sunulmayacaktır. |

### <a name="parameter-to-enable-sales-orders-with-multiple-project-contract-funding-sources"></a>Satış siparişlerini birden fazla proje sözleşme finansman kaynağı ile etkinleştirme parametreleri
Proje tabanlı satış siparişlerini, proje sözleşmesi birden fazla finansman kaynağına sahip olduğunda, **Proje yönetimi parametreleri** ayarında, **Birden fazla finansman kaynağı projeler için satış siparişlerine izin ver** ile etkindir. Varsayılan olarak, bu parametre etkin değil. 

| &nbsp;  |&nbsp;  |
|------------|--------------------|
| **Kullanımı sonlandırma/kaldırma nedeni** | Bu işlev, parametre kaldırıldıktan sonra her zaman etkin olacaktır. |
| **Başka bir özellikle mi değiştirildi?**   | Hayır. Proje tabanlı satış siparişlerini birden fazla finansman kaynağı ile destekleme işlevi her zaman etkin olacaktır.   |
| **Etkilenen ürün alanları**         |**Birden fazla finansman kaynağı olan projeler için satış siparişlerine izin ver** parametresi kaldırılacaktır. Aşağıdaki yöntemler, parametre kaldırıldığında değiştirilir: **ctrlSalesOrderTable** yöntemi, **ProjStatusType** sınıfında, **doğrula** yöntemi **ProjId** alanında ve **çalıştır** yöntemi **SalescreateOrder** formunda. Aşağıdaki yöntemler parametre kaldırıldığında kullanımdan kaldırılır: **IsSalesOrderAllowedForMultipleFundingSources**, **ProjTable** tablo dosyası içinde; **IsAllowSalesOrdersForMultipleFundingSourcesParamEnabled** yöntemi, **ProjTable** tablo dosyası içinde; **AllowSalesOrdersForMultipleFundingSources** veri alanı, **ProjParameters** formunda ve **ProjParameterEntity** dosyaları, **IsAssociatedToMultipleFundingSourcesContract** özel yöntemi, **ProjTable** tablo dosyasında. |
| **Dağıtım seçeneği**              | Tümü  |
| **Durum**                         | Kullanımdan kaldırma Nisan 2020 sürüm dalgası için planlanmıştır. |

### <a name="legacy-workflow-reports-for-tracking-and-instance-status"></a>İzleme ve kurulum durumu için eski iş akışı raporları

|  &nbsp; | &nbsp; |
|------------|--------------------|
| **Kullanımı sonlandırma/kaldırma nedeni** | İzleme ve kurulum durumu için eski iş akışı raporları, gezintiden daha fazla referans gösterilmedikleri için kullanımdan kaldırılmıştır. Rapor adları WorkflowWorkflowInstanceByStatusReport ve WorkflowWorkflowTrackingReport'tur. |
| **Başka bir özellikle mi değiştirildi?**   | İş akışı geçmişi formu bunun yerine kullanılabilir. |
| **Etkilenen ürün alanları**         | Web istemcisi |
| **Dağıtım seçeneği**              | Tümü |
| **Durum**                         | Kaldırıldı: İşlevin kaldırılması hedeflenen zaman aralığı Nisan 2020'dir. |

## <a name="finance-and-operations-1001-with-platform-update-25"></a>Finance and Operations 10.0.1, Platform güncelleştirmesi 25 ile

### <a name="deprecated-apis-and-potential-breaking-changes"></a>Kaldırılan API'ler ve potansiyel bozucu değişiklikler


#### <a name="deriving-from-internal-classes-is-deprecated"></a>Dahili sınıftan türetme kalkmıştır

| &nbsp;  |&nbsp;  |
|------------|--------------------|
| **Kullanımı sonlandırma/kaldırma nedeni** | Platform güncelleştirmesi 25'ten önce, bu tablo bir iç sınıf/başka bir paket/modülünde tanımlanmış tablosu türetilen bir sınıf veya oluşturulabilir. Bu güvenli bir kodlama yöntemi değildir. Platform güncelleştirmesi 25 ile, derleyici bir uyarı görüntüler. |
| **Başka bir özellikle mi değiştirildi?**   | Derleyici uyarısı, Platform güncelleştirmesi 26'da değiştirilecektir. Bu değişiklik çalışma zamanında geriye yönelik uyumludur, bu da Platform güncelleştirmesi 25 veya üzerini kullanıyorsanız, bunun herhangi bir korumalı alanda veya üretim ortamında özel kodu değiştirmeye gerek olmadan kullanılabileceği anlamına gelir. Bu değişiklik yalnızca geliştirme ve derleme zamanını etkiler.|
| **Etkilenen ürün alanları**         | Visual Studio geliştirme araçları |
| **Dağıtım seçeneği**              | Tümü |
| **Durum**                         | Kaldırıldı: Uyarı, Platform güncelleştirmesi 26'da derleme hatası olarak değiştirilecektir. |

#### <a name="overriding-internal-methods-is-deprecated"></a>Dahili yöntemleri geçersiz kılma kalkmıştır

| &nbsp;  |&nbsp;  |
|------------|--------------------|
| **Kullanımı sonlandırma/kaldırma nedeni** | Platform güncelleştirmesi 25'ten öncesinde, başka bir paket/modülde tanımlanan türetilen bir sınıftaki dahili bir yöntemi geçersiz kılmak mümkündü. Bu güvenli bir kodlama yöntemi değildir. Platform güncelleştirmesi 25 ile, derleyici bir uyarı görüntüler. |
| **Başka bir özellikle mi değiştirildi?**   | Bu uyarı, Platform güncelleştirmesi 26'da bir derleme hatasıyla değiştirilecektir. Bu değişiklik çalışma zamanında geriye yönelik uyumludur, bu da Platform güncelleştirmesi 25 veya üzerini kullanıyorsanız, bunun herhangi bir korumalı alanda veya üretim ortamında özel kodu değiştirmeye gerek olmadan kullanılabileceği anlamına gelir. Bu değişiklik yalnızca geliştirme ve derleme zamanını etkiler. |
| **Etkilenen ürün alanları**         | Visual Studio geliştirme araçları |
| **Dağıtım seçeneği**              | Tümü |
| **Durum**                         | Kaldırıldı: Uyarı, Platform güncelleştirmesi 26'da derleme hatası olarak değiştirilecektir. |

## <a name="finance-and-operations-1000-with-platform-update-24"></a>Finance and Operations 10.0.0, Platform güncelleştirmesi 24 ile

### <a name="renaming-released-products"></a>Sunulan ürünleri yeniden adlandırma 
| &nbsp;  |&nbsp;  |
|------------|--------------------|
| **Kullanımı sonlandırma/kaldırma nedeni** | Serbest bırakılan bir ürünün birincil anahtarı yeniden adlandırmak için **Birincil anahtarı yeniden adlandır** işlevini kullandığınızda, yalnızca doğrudan yabancı anahtar başvuruları güncelleştirilir. Üretim emirlerinden dolayı, serbest bırakılan ürüne ilişkin diğer tüm başvurular eski madde kodunu korur. Sonuç olarak, sonuçta iş süreçlerini engelleyen tutarsız veriler olabilir. |
| **Başka bir özellikle mi değiştirildi?**   | Hayır. |
| **Etkilenen ürün alanları**         | Ürün bilgileri yönetimi |
| **Dağıtım seçeneği**              | Tümü  |
| **Durum**                         | Platform update 24 ile Finance and Operations 10.0.0 itibarıyla kaldırıldı.|


## <a name="finance-and-operations-813-with-platform-update-23"></a>Finance and Operations 8.1.3, Platform güncelleştirmesi 23 ile

### <a name="sql-server-reporting-services-reportviewer-control"></a>SQL Server Reporting Services ReportViewer Denetimi
Müşteriler katıştırılmış SQL Server Reporting Services (SSRS) ReportViewer denetimi tarafından sağlanan **Dışa aktar** eylemini, Finance and Operations uygulamaları tarafından üretilen belgeleri indirme için kullanabilirler. Raporun HTML tabanlı sunumu, belgenin sayfalandırılmamış önizlemesini kullanıcılara sunar.

| &nbsp;  |&nbsp;  |
|------------|--------------------|
| **Kullanımı sonlandırma/kaldırma nedeni** | HTML tabanlı önizleme deneyiminin sayfalandırılmamış doğası, Finance and Operations tarafından nihai olarak üretilen fiziksel belgelerin doğruluğunu **sunmaz**. PDF'i iş belgeleri için standart format olarak tümüyle benimseyerek, kullanıcılar, uygulama raporları oluştururken geliştirilmiş performansa sahip modern görüntüleme denetiminden faydalanabilmektedir. |
| **Başka bir özellikle mi değiştirildi?**   | Gelecekte, PDF belgeleri Finance and Operations tarafından oluşturulan raporlar için varsayılan biçim olacaktır.   |
| **Etkilenen ürün alanları**         | Bu değişiklik, raporların elektronik olarak dağıtıldığı veya doğrudan yazıcılara gönderildiği müşteri senaryolarını **etkilemez**.    |
| **Dağıtım seçeneği**              | Tümü  |
| **Durum**                         | Kullanımı sonlandırıldı: Bu özellik için kaldırma tarihi belirlenmedi. Katıştırılmış PDF görüntüleyici kullanarak uygulama raporlarını otomatik olarak önizleme özelliği, Mayıs 2019 platform güncelleştirmesi için planlanmaktadır. |

### <a name="client-kpi-controls"></a>İstemci KPI denetimleri
Katıştırılmış kilit performans göstergeleri (KPI'ları), bir geliştirici tarafından Visual Studio içinde modellenebilir ve son kullanıcı tarafından daha da özelleştirilebilir.

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Kullanımı sonlandırma/kaldırma nedeni** | KPI'ları tanımlamak için kullanılan yerel istemci denetimleri, düşük müşteri katılımına sahiptir ve geliştiricinin izlenebilir metrikler eklemesine bağlıdır. |
| **Başka bir özellikle mi değiştirildi?**   | PowerBI.com servisi, KPI'ları dış kaynak verilerine dayanarak tanımlama ve yönetme için üst düzey araçlar sağlar.  Gelen bir sürümde, uygulama çalışma alanlarında PowerBI.com barındırılan çözümleri katıştırmanız planlanmaktadır.   |
| **Etkilenen ürün alanları**         | Bu güncelleştirme, geliştiricilerin yeni KPI denetimlerini Visual Studio tasarımcısında dahil etmelerini engeller.    |
| **Dağıtım seçeneği**              | Tümü  |
| **Durum**                         | Kullanımı sonlandırıldı: Bu özellik için kaldırma tarihi belirlenmedi. |

### <a name="deprecated-apis-and-future-breaking-changes"></a>Kaldırılan API'ler ve gelecekteki bozucu değişiklikler

#### <a name="field-groups-containing-invalid-field-references"></a>Geçersiz alan referansı içeren alan denetimleri

| &nbsp;  |&nbsp;  |
|------------|--------------------|
| **Kullanımı sonlandırma/kaldırma nedeni** | Tablo metaveri tanımlarının geçersiz alan referansları içeren alan gruplarına sahip olması mümkündür. Dağıtıldığında, bu, Finansal Raporlama ve SQL Server Reporting Services (SSRS) içinde çalışma zamanı hatalarına neden olabilir. Bu sorun şu anda bir *hata* yerine *derleyici uyarısı* olarak kategorize edilmiştir, bu da dağıtılabilir paket oluşturma ve geliştirmenin bu sorun giderilmeden devam edebileceği anlamına gelir. Bu sorunu gidermek için:<br><br>1. Geçersiz alan başvurusunu tablo alanı grubunu tanımından kaldırın.<br><br>2. Yeniden derleyin.<br><br>3. Uyarılar veya hataların ele alındığından emin olun. |
| **Başka bir özellikle mi değiştirildi?**   | Bu uyarı, gelecekte bir derleme hatası ile değiştirilecektir. |
| **Etkilenen ürün alanları**         | Visual Studio geliştirme araçları |
| **Dağıtım seçeneği**              | Tümü |
| **Durum**                         | Kullanım dışı: Uyarı, Finance and Operations uygulamalarının 10.0.11 sürümü platform güncelleştirmeleri ile derleme zamanı hatasıdır. |

#### <a name="complete-list"></a>Tam liste
Kullanımdan kaldırılan API'lerin tam listesine erişmek için bkz. [Yöntemler ve meta veri öğelerinin kullanımdan kaldırılması](deprecation-deletion-apis.md).

## <a name="finance-and-operations-81-with-platform-update-20"></a>Finance and Operations 8.1, Platform güncelleştirmesi 20 ile

### <a name="batch-transfer-rules-for-subledger-journal-account-entries"></a>Muavin defteri günlüğü hesap girişleri için toplu transfer kuralları
Zaman uyumlu aktarım modunu genel muhasebe parametrelerinde kaldırılıyor.  Bu mod, halihazırda transfer için seçenek olarak mevcut olan Asenkron ve zamanlanan toplu iş ile değiştiriliyor. Ek bilgi için bkz [Genel muhasebe parametreleri – transfer toplu işi kuralları](https://community.dynamics.com/365/financeandoperations/b/financials/archive/2019/03/15/general-ledger-parameters-batch-transfer-rules) Web günlüğü.

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Kullanımı sonlandırma/kaldırma nedeni** | Sistem performansı üzerindeki etkisi nedeniyle zaman uyumlu seçeneği kaldırıyoruz. |
| **Başka bir özellikle mi değiştirildi?**   | Asenkron ve zamanlanan toplu iş seçenekleri, zaman uyumlu yerine kullanılacak seçeneklerdir.   |
| **Etkilenen ürün alanları**         | Genel muhasebe, Borç hesapları, Alacak Hesapları, satın alma, gider    |
| **Dağıtım seçeneği**              | Tümü  |
| **Durum**                         | Kullanımı sonlandırıldı: İşlevin kaldırılması hedeflenen zaman aralığı 10.0 sürümüdür.|

### <a name="electronic-reporting-for-russia"></a>Rusya için Elektronik raporlama
.txt ve .xml dosya biçimlerini bildirimler için yapılandırma özelliği. 

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Kullanımı sonlandırma/kaldırma nedeni** | Elektronik raporlama ile değiştirildi. |
| **Başka bir özellikle mi değiştirildi?**   | Evet. |
| **Etkilenen ürün alanları**         | Genel Muhasebe |
| **Dağıtım seçeneği**              | Tümü |
| **Durum**                         | Platform update 20 ile Finance and Operations 8.1 itibarıyla kaldırıldı. |

### <a name="financial-reports-generator-for-russia"></a>Rusya için finansal raporlar oluşturucusu
Muhasebe ve vergi raporları için veri toplamak ve XLS ve DOC rapor şablonlarına dışa veri aktarmak için bir araç. İşlevsel parçalar: XLS ve DOC rapor şablonlarına, sorgularına ve sabit gereksinimlerine veri dışa aktarma kaldırıldı. 

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Kullanımı sonlandırma/kaldırma nedeni** | Kaldırılan bölümler Elektronik Raporlama ile değiştiriliyor. |
| **Başka bir özellikle mi değiştirildi?**   | Evet. Finansal raporlar kullanıcı ayarı arabirimi, GL hesapları veya vergi kayıtları için veri toplama kuralları ayarlamak için kullanılmalıdır. Muhtelif veri türlerine, sabit gereksinimlere ve sorgu benzeri veri toplama kurallarına veri dışa aktarma, Elektronik raporlamada yapılandırılmalıdır. |
| **Etkilenen ürün alanları**         | Genel muhasebe. |
| **Dağıtım seçeneği**              | Tümü |
| **Durum**                         | Platform update 20 ile Finance and Operations 8.1 itibarıyla kaldırıldı. |

### <a name="integration-with-external-providers-for-sending-electronic-reporting-through-communication-channels-for-russia"></a>Rusya için iletişim kanalları üzerinden elektronik raporlama göndermek için dış sağlayıcılar ile tümleştirme
Dışa aktarma özelliğini klasörüne bildirimlerinin elektronik dosyalar daha ayrıntılı olarak elektronik raporlama durumuna geri alma resmi sağlayıcı göndermek için oluşturulur.

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Kullanımı sonlandırma/kaldırma nedeni** | Elektronik iletiler yapılandırılabilir özelliği ile değiştirildi. |
| **Başka bir özellikle mi değiştirildi?**   | Evet.  |
| **Etkilenen ürün alanları**         | Genel Muhasebe, Vergi |
| **Dağıtım seçeneği**              | Tümü |
| **Durum**                         | Platform update 20 ile Finance and Operations 8.1 itibarıyla kaldırıldı. |


### <a name="profit-tax-register-wizard"></a>Kar vergi kayıt sihirbazı
Yeni kar vergi kayıtları için şablonlar oluşturma özelliği. Bu özellik, yeni kayıtlar için X++ nesnelerini oluşturur, bunlar daha sonra şablonlar olarak uygun hesaplama mantığı eklenmiş biçimde oluşturulur.

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Kullanımı sonlandırma/kaldırma nedeni** | Finance and Operations genişletilebilirlik modeli ile uyumlu değil. |
| **Başka bir özellikle mi değiştirildi?**   | Hayır |
| **Etkilenen ürün alanları**         | Vergi |
| **Dağıtım seçeneği**              | Tümü |
| **Durum**                         | Platform update 20 ile Finance and Operations 8.1 itibarıyla kaldırıldı. |


## <a name="finance-and-operations-80-with-platform-update-15"></a>Finance and Operations 8.0, Platform güncelleştirmesi 15 ile
Bu sürümle hiçbir özellik kaldırılmamış veya kullanım dışı bırakılmamıştır. Platform Güncelleştirmesi 15 toplu güncelleştirmedir ve Platform Güncelleştirmesi 13, Platform Güncelleştirmesi 14 ve Platform Güncelleştirmesi 15'deki yeni veya değiştirilmiş özellikleri içerir.

## <a name="finance-and-operations-enterprise-edition-73-with-platform-update-12"></a>Finance and Operations, Enterprise Edition 7.3, Platform update 12 ile

### <a name="personalized-product-recommendations"></a>Kişiselleştirilmiş ürün önerileri 
15 Şubat 2018 tarihinden itibaren perakendeciler artık satış noktası cihazındaki (POS) kişiselleştirilmiş ürün önerilerini görüntüleyemeyecektir. Daha fazla bilgi için bkz. [Ürün önerilerine genel bakış](../../../commerce/product-recommendations.md).  

| &nbsp;  |&nbsp;  |
|------------|--------------------|
| **Kullanımı sonlandırma/kaldırma nedeni** | Bu özelliği daha iyi bir algoritma ve daha yeni perakende odaklı yeteneklerle yeniden tasarladığımızdan ürün öneri hizmetinin geçerli sürümünü kaldırıyoruz.  |
| **Başka bir özellik ile değiştirildi?**   | Hayır. Ancak, 2018 yılı bahar aylarından sonra yeni bir öneri hizmetinden yararlanmak için bu özelliği geri getirmeyi planlıyoruz.   |
| **Etkilenen ürün alanları**         | POS'ta kişiselleştirilmiş ürün önerileri.                                                    |
| **Dağıtım seçeneği**              | Tümü                                                                                      |
| **Durum**                         |15 Şubat 2018 itibarıyla kaldırıldı. Bu, Dynamics 365 for Operations 1611 veya sonrasını çalıştıran müşterileri etkiler.  |

### <a name="extension-of-the-list-of-electronic-reporting-er-functions"></a>Elektronik raporlama (ER) işlev listesi genişletmesi
ER ifade oluşturucuda kullanılmak üzere özel işlevler sağlama olasılığı (daha fazla bilgi için bkz. [Elektronik raporlama (ER) işlev listesini genişletme](../../dev-itpro/analytics/general-electronic-reporting-formulas-list-extension.md)) artık desteklenmemektedir. ER API'lerindeki değişiklikler nedeniyle, ER ifade oluşturucudan yerleşik işlevleri çağırmak için kullanılan API dahili hale gelmiştir ve artık genişletilemez.

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Kullanımı sonlandırma/kaldırma nedeni** | Kod kapama girişimi  |
| **Başka bir özellik ile değiştirildi?**   | Hiçbiri. Yeni bir yerleşik işlev gerektiğinde, yeni genişletme talebinin ER altyapısı ekibine bildirilmesi gerekir.<br><br>İstenen işlev ER ekibi tarafından geliştirilirken geçici bir çalışma olarak, talep edilen mantık özel uygulama sınıfı yöntemi olarak programlanabilir. Bu yönteme, eklenen ve özel uygulama sınıfına başvuruda bulunan **Application\Class** türündeki ER veri kaynağının bir özelliği olarak ER ifadesinden erişilebilir.  |
| **Etkilenen ürün alanları**         | Elektronik raporlama çerçevesi                                                      |
| **Dağıtım seçeneği**              | Tümü                                                                                      |
| **Durum**                         | Finance and Operations, Enterprise Edition 7.3 itibariyle kaldırıldı.    |

### <a name="inventory-by-item-group-and-inventory-by-inventory-dimension-aging-reports"></a>Madde grubuna göre stok ve stok boyutu yaşlandırmasına göre stok raporları

Bu iki rapor artık Finance and Operations'da desteklenmemektedir. Bunun yerine, **Stok yaşlandırma** raporu kullanıcı deneyimini geliştirmek için kullanılabilir.

| &nbsp;  | &nbsp; |
|--------------|-----------------------|
| **Kaldırılma nedeni**       | Tekrar eden işlevsellik  |
| **Başka bir özellik ile değiştirildi?** | Evet. İki rapor **Stok yaşlandırma** raporuyla değiştirilmiştir.     |
| **Etkilenen ürün alanları**       | Stok yönetimi, Maliyet yönetimi        |
| **Dağıtım seçeneği**        | Tümü|
| **Durum**                       | Kullanımı sonlandırıldı: Her iki raporun da menü öğeleri 7.3 sürümünde kaldırıldı. Ancak, raporların kodu üründe kaldı. Plan kodu sonraki bir sürümde kaldırmaktır. |

### <a name="power-bi-content-packs-available-on-appsource"></a>Power BI içerik paketleri AppSource'de kullanılabilir
[Microsoft AppSource](https://appsource.microsoft.com)'ta yayımlanmış olan **Maliyet yönetimi**, **Mali performans** ve **Retail Channel Performance** içerik paketleri, Microsoft Power BI'daki ürün güncelleştirmelerinin sonucu olarak kullanımdan kaldırıldı. PowerBI.com'da bu içerik paketlerini dağıtmak için kullanılan sistem yönetim formlarının kullanımı da Finance and Operations'ta sonlandırıldı.

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Kullanımı sonlandırma/kaldırma nedeni** | Microsoft Power BI'daki ürün güncelleştirmeleri. |
| **Başka bir özellikle mi değiştirildi?**   | [AppSource](https://appsource.microsoft.com) sitesinde bulunan **Yönetimi maliyet**, **Mali performans** ve **Retail Channel Performance** içerik paketleri, veritabanı düzeyinde çözüm tümleştirmelerine olanak tanıyan analiz uygulamalarıyla değiştirilmektedir. Analiz uygulamaları hakkında daha fazla bilgi için bkz. [Çalışma alanlarına katıştırılmış Power BI](../../dev-itpro/analytics/embed-power-bi-workspaces.md).    |
| **Etkilenen ürün alanları**         | Maliyet yönetimi, Finans ve Perakende                                                                                               |
| **Dağıtım seçeneği**              | Yalnızca bulut(PowerBI.com ile tümleştirme şirket içi dağıtımlarda desteklenmez.)                                                                                                            |
| **Durum**                         | Kullanımı sonlandırıldı: İşlevin kaldırılması hedeflenen zaman aralığı 2018 yılı 2. çeyreğidir.    |

### <a name="standard-ui-in-data-management-workspace"></a>Veri yönetimi çalışma alanında standart kullanıcı arabirimi

Veri yönetimindeki standart kullanıcı arabirimi, veri yönetimi çalışma alanını ziyaret ettiklerinde kullanıcılara sunulan varsayılan kullanıcı arabirimi olan eski kullanıcı arabirimidir.

| &nbsp;  | &nbsp; |
|------------------|-------------------------|
| **Kullanımı sonlandırma/kaldırma nedeni** | Yeni kullanıcı arabiriminde yeni kullanıcı deneyimleri sunmak için çalışıyoruz.             |
| **Başka bir özellik ile değiştirildi?**   | *Gelişmiş görünümler* adlı yeni kullanıcı arabirimi eski kullanıcı arabiriminin yerini aldı.            |
| **Etkilenen ürün alanları**         | Veri yönetimi çalışma alanı                                                     |
| **Dağıtım seçeneği**              | Tümü                                                                           |
| **Durum**                         | Kullanımı sonlandırıldı: İşlevin kaldırılması hedeflenen zaman aralığı 2018 yılı 2. çeyreğidir. |

### <a name="excise-sales-tax-service-tax-for-india"></a>Hindistan için Tüketim, Satış Vergisi, Hizmet Vergisi

Bu vergiler Hindistan GST içine eklendi.

|  &nbsp;                                           |      &nbsp;                                                                   |
|---------------------------------------------|-------------------------------------------------------------------------|
| **Kullanımı sonlandırma veya kaldırma nedeni**       | Bu vergiler Hindistan GST içine eklendi.                          |
| **Başka bir özellik ile değiştirildi?**            | Hindistan GST                                                              |
| **Etkilenen ürün alanları**                  | Vergi                                                                     |
| **Dağıtım seçeneği**                       | Tüm modüller                                                   |
| **Durum**                                  | Kullanımı sonlandırıldı: Bu özellik için kaldırma tarihi belirlenmedi. |    

### <a name="file-validation-utility-fvu-for-india"></a>Hindistan için Dosya Doğrulama Yardımcı Programı (FVU)

|              &nbsp;                               |      &nbsp;                                                                   |
|---------------------------------------------|-------------------------------------------------------------------------|
| **Kullanımı sonlandırma veya kaldırma nedeni**       | Müşteri kullanım eksikliği                                                  |
| **Başka bir özellik ile değiştirildi?**            | Hayır                                                                      |
| **Etkilenen ürün alanları**                  | Hindistan stopaj vergisi                                                  |
| **Dağıtım seçeneği**                       | Tüm modüller                                                                    |
| **Durum**                                  | Kullanımı sonlandırıldı: Bu özellik için kaldırma tarihi belirlenmedi.   |        

### <a name="tdstcs-certificate-for-india"></a>Hindistan için TDS/TCS sertifikası

Kullanıcılar bu formu resmi devlet portalından indirebilir.

|             &nbsp;                                |    &nbsp;                                                                     |
|---------------------------------------------|-------------------------------------------------------------------------|
| **Kullanımı sonlandırma veya kaldırma nedeni**       | Müşteri kullanım eksikliği                                                  |
| **Başka bir özellik ile değiştirildi?**            | Hayır                                                                      |
| **Etkilenen ürün alanları**                  | Hindistan stopaj vergisi                                                  |
| **Dağıtım seçeneği**                       | Tüm modüller                                                                   |
| **Durum**                                  | Kullanımı sonlandırıldı: Bu özellik için kaldırma tarihi belirlenmedi.     |    

### <a name="exportimport-exim-incentive-scheme-for-india"></a>Hindistan için ihracat/ithalat (EXIM) girişimi şeması


|              &nbsp;                               |        &nbsp;                                                                 |
|---------------------------------------------|-------------------------------------------------------------------------|
| **Kullanımı sonlandırma veya kaldırma nedeni**       | Müşteri kullanım eksikliği                                                  |
| **Başka bir özellik ile değiştirildi?**            | Hayır                                                                      |
| **Etkilenen ürün alanları**                  | İçe ve dışa aktar                                                       |
| **Dağıtım seçeneği**                       | Tüm modüller                                                                    |
| **Durum**                                  | Kullanımı sonlandırıldı: Bu özellik için kaldırma tarihi belirlenmedi.  |    


## <a name="dynamics-365-for-retail-72"></a>Dynamics 365 for Retail 7.2

### <a name="personalized-product-recommendations"></a>Kişiselleştirilmiş ürün önerileri 
15 Şubat 2018 tarihinden itibaren perakendeciler artık satış noktası cihazındaki (POS) kişiselleştirilmiş ürün önerilerini görüntüleyemeyecektir. Daha fazla bilgi için bkz. [Ürün önerilerine genel bakış](../../../commerce/product-recommendations.md).  

|  &nbsp; |  &nbsp;|
|------------|--------------------|
| **Kullanımı sonlandırma/kaldırma nedeni** | Bu özelliği daha iyi bir algoritma ve daha yeni perakende odaklı yeteneklerle yeniden tasarladığımızdan ürün öneri hizmetinin geçerli sürümünü kaldırıyoruz.  |
| **Başka bir özellik ile değiştirildi?**   | Hayır. Ancak, 2018 yılı bahar aylarından sonra yeni bir öneri hizmetinden yararlanmak için bu özelliği geri getirmeyi planlıyoruz.   |
| **Etkilenen ürün alanları**         | POS'ta kişiselleştirilmiş ürün önerileri.                                                    |
| **Dağıtım seçeneği**              | Tümü                                                                                      |
| **Durum**                         |15 Şubat 2018 itibarıyla kaldırıldı. Bu, Dynamics 365 for Retail 7.2 veya sonrasını çalıştıran müşterileri etkiler. |


## <a name="finance-and-operations-enterprise-edition-july-2017-with-platform-update-8"></a>Finance and Operations, Enterprise Edition Temmuz 2017, Platform update 8 ile

### <a name="currency-conversion-for-accounting-and-reporting-currencies"></a>Muhasebe ve raporlama para birimleri için para birimi dönüştürme

Muhasebe ve raporlama para birimleri için para birimi dönüştürme, avro çıktığı zaman kullanıma sunulmuştur.

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Kullanımı sonlandırma/kaldırma nedeni** | Tüzel kişilik kopyalama işlevselliğinin bir değişiklik olarak sınırlı kullanımı ve eklenmesi.      |
| **Başka bir özellikle mi değiştirildi?**   | Hayır, ancak Tüzel kişilik kopyalama ve Yapılandırmalar özellikleri, temel gereksinimlerini değiştiren bir şirkete taşımayı kolaylaştırmak için eklendi. |
| **Etkilenen ürün alanları**         | Mali yönetim     |
| **Durum**                         | Kullanımı sonlandırıldı: Bu özellik için kaldırma tarihi belirlenmedi.   |


### <a name="warehouse-mobile-devices-portal"></a>Ambar mobil cihazlar portalı

Ambar mobil cihazlar portalı (WMDP), yerinde kendi kedine dağıtım için amaçlanmış bir tek bileşendir. Bu bileşen artık Finance and Operations'da desteklenmiyor. Kullanıcı deneyimini iyileştiren bir yerel uygulama, WMDP'nin işlevinin yerini almıştır.

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Kullanımı sonlandırma/kaldırma nedeni** | Tekrar eden işlevsellik.       |
| **Başka bir özellikle mi değiştirildi?**   | Evet. Bu özellik Finance and Operations - Ambarlama ile değiştirilmiştir. Kurulum ve önkoşullar hakkında daha fazla bilgi için bkz. [Ambarlama uygulamasını yükleme ve yapılandırmaya genel bakış](../../../supply-chain/warehousing/install-configure-warehousing-app.md). |
| **Etkilenen ürün alanları**         | Ambar yönetimi, Taşıma yönetimi     |
| **Dağıtım seçeneği**              | Ambar mobil cihazlar portalı (WMDP), yerinde kendi kedine dağıtım için amaçlanmış bir tek bileşendir.               |
| **Durum**                         | Kaldırıldı: İşlevin kaldırılması hedeflenen zaman aralığı 2019 yılı 4. çeyreğidir.   |

### <a name="advanced-bank-reconciliation-matching-rule-for-manual-matching"></a>El ile eşleştirme için gelişmiş banka mutabakatı eşleştirme kuralı

Bir mutabakat kuralı, belgeler el ile mutabakat çalışma sayfasında eşleştirildiğinde bir banka belgesini seçmek ve işaretlemek için kullanılmıştır.

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Kullanımı sonlandırma/kaldırma nedeni** | Sınırlı kullanım.                                                                         |
| **Başka bir özellik ile değiştirildi?**   | Hayır. Sütun filtreleme yetenekleri, mutabakat için belgeleri bulmakta kullanılmalıdır. |
| **Etkilenen ürün alanları**         | Nakit ve banka yönetimi                                                               |
| **Dağıtım seçeneği**              | Tümü                                                                                    |
| **Durum**                         | Temmuz 2017 itibarıyla kaldırıldı.                                                               |

## <a name="dynamics-365-for-operations-1611-with-platform-update-3"></a>Dynamics 365 for Operations 1611, Platform güncelleştirmesi 3 ile

### <a name="aeb-payment-formats-for-spain"></a>İspanya için AEB ödeme biçimleri

Consejo Superior Bancario ödeme biçimleri, müşteri ödemeleri ve satıcı ödemeleri için havale dosyalarını bankaya göndermek amacıyla kullanılıyordu. Bu biçimlerin içeriği Asociación Española de Banca tarafından belirlenmiştir. Cuaderno 19, 32, 58, 34'ü kapsar.

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Kullanımı sonlandırma/kaldırma nedeni** | Ödeme biçimleri artık kullanılmamaktadır.                                  |
| **Başka bir özellik ile değiştirildi?**   | Evet, İspanya için ISO20022 Alacak transferi ve Otomatik ödeme biçimleri |
| **Etkilenen ürün alanları**         | Borç hesapları, Alacak hesapları                                    |
| **Durum**                         | Kullanımı sonlandırıldı: Bu özellik için kaldırma tarihi belirlenmedi.           |

### <a name="bank-payments-transfer-for-lithuania"></a>Litvanya için banka ödemeleri transferi

Litvanya için banka ödeme transferleri, Ödeme transferi (LT) dışa aktarma biçimi kullanarak oluşturuluyor ve yazdırılıyordu. Litvanya pazarı 2005'te birleştirilmiş elektronik bankacılık sistemi olan LİTAS'ı kullanmaya başladı.

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Kullanımı sonlandırma/kaldırma nedeni** | Ödeme biçimleri artık kullanılmamaktadır.                        |
| **Başka bir özellik ile değiştirildi?**   | Evet, Litvanya için ISO20022 Alacak transferi ödeme biçimi     |
| **Etkilenen ürün alanları**         | Borç hesapları                                               |
| **Durum**                         | Kullanımı sonlandırıldı: Bu özellik için kaldırma tarihi belirlenmedi. |

### <a name="bbs-direkte-remittering-payment-formats-for-norway"></a>Norveç için BBS Direkte Remittering ödeme biçimleri

BBS Direkte Remittering ödeme biçimleri, müşteri ödeme tahsilatını dışa aktarmayı (otomatik ödeme) ve geri dönen iletiyi içe aktarmayı içerir.

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Kullanımı sonlandırma/kaldırma nedeni** | Ödeme biçimleri artık kullanılmamaktadır.  |
| **Başka bir özellik ile değiştirildi?**   | Norveç için AvtaleGiro müşteri ödeme biçimi otomatik ödeme iletileri oluşturmak için kullanılabilir. Geri dönen iletiyi içe aktarma gelecek sürümlerde uygulanacaktır. |
| **Etkilenen ürün alanları**         | Borç hesapları, Alacak hesapları   |
| **Durum**                         | Kullanımı sonlandırıldı: Bu özellik için kaldırma tarihi belirlenmedi.                                                                                                 |

### <a name="chart-of-accounts-tool-for-spain"></a>İspanya için Hesap Planı aracı

Bu araç, İspanya'da bir hesap planında büyük değişiklikler yapılması gerektiğinde kullanılır. Kullanıcılar Microsoft Excel'de veya metin biçiminde yeni bir hesap planını ve ayrıca mali tabloları içe aktarabilir.

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Kullanımı sonlandırma/kaldırma nedeni** | Sınırlı kullanım                                                  |
| **Başka bir özellik ile değiştirildi?**   | Hayır                                                             |
| **Etkilenen ürün alanları**         | Genel muhasebe                                                 |
| **Durum**                         | Kullanımı sonlandırıldı: Bu özellik için kaldırma tarihi belirlenmedi. |

### <a name="dom80-payment-format-for-belgium"></a>Belçika için Dom80 ödeme biçimi

Ödeme tahsilatı (otomatik ödeme) için eski Belçika ödeme biçimi.

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Kullanımı sonlandırma/kaldırma nedeni** | Ödeme biçimi artık kullanılmamaktadır.                          |
| **Başka bir özellik ile değiştirildi?**   | Evet, Belçika için ISO 20022 Otomatik ödeme biçimi         |
| **Etkilenen ürün alanları**         | Alacak hesapları                                            |
| **Durum**                         | Kullanımı sonlandırıldı: Bu özellik için kaldırma tarihi belirlenmedi. |

### <a name="dtaezag-payment-formats-for-switzerland"></a>İsviçre için DTA/EZAG ödeme biçimleri

DTA/EZAG biçimleri, referans numarası ile ilişkili oldukları için ESR sistemine tümleştirilmiştir. Referans numarası zorunlu olmadığından bu biçimler her türlü satıcı ödemesini işlemek için kullanılabilir. Bu biçimler “Postfinance” dışında bir konumda banka hesabı bulunan şirketler tarafından kullanılır.

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Kullanımı sonlandırma/kaldırma nedeni** | Ödeme biçimleri artık kullanılmamaktadır.                        |
| **Başka bir özellik ile değiştirildi?**   | Evet, İsviçre için ISO20022 Alacak transferi ödeme biçimi   |
| **Etkilenen ürün alanları**         | Borç hesapları                                               |
| **Durum**                         | Kullanımı sonlandırıldı: Bu özellik için kaldırma tarihi belirlenmedi. |

### <a name="edifact-dirdeb-payment-format-for-austria"></a>Avusturya için EDIFACT DIRDEB ödeme biçimi

Ödeme tahsilatı (otomatik ödeme) için EDIFACT-DIRDEB ödeme biçimi.

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Kullanımı sonlandırma/kaldırma nedeni** | Ödeme biçimi artık kullanılmamaktadır.                          |
| **Başka bir özellik ile değiştirildi?**   | Evet, Avusturya için ISO 20022 Otomatik ödeme biçimi         |
| **Etkilenen ürün alanları**         | Alacak hesapları                                            |
| **Durum**                         | Kullanımı sonlandırıldı: Bu özellik için kaldırma tarihi belirlenmedi. |

### <a name="edivat-for-belgium"></a>Belçika için EDIVAT

EDIVAT güvenli posta yoluyla elektronik beyanname için geçersiz bir Belçika standardıdır. Dynamics AX 2012 geçmiş verilerine erişim sağlamak için salt okunur çözüm içerir.

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Kullanımı sonlandırma/kaldırma nedeni** | İşlev artık kullanılmamaktadır.                           |
| **Başka bir özellik ile değiştirildi?**   | Hayır                                                             |
| **Etkilenen ürün alanları**         | Genel muhasebe                                                 |
| **Durum**                         | Kullanımı sonlandırıldı: Bu özellik için kaldırma tarihi belirlenmedi. |

### <a name="egiro-edifact-cremul-payment-import-format-for-norway"></a>Norveç için eGiro EDIFACT CREMUL ödeme içe aktarma biçimi

eGiro müşteri ödemelerinin otomatik deftere nakil işleminde kullanılan uluslararası UN EDIFACT CREMUL (Birden Fazla Alacak Dekontu İletisi) standardını temel alır. Dynamics AX içinde eGiro bir müşterinin ödemesi içe aktarma biçimi olarak kullanılır.

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Kullanımı sonlandırma/kaldırma nedeni** | Ödeme biçimi artık kullanılmamaktadır.                                                     |
| **Başka bir özellikle mi değiştirildi?**   | Evet, ISO20022 CAMT.054 bildirimi içe aktarması. |
| **Etkilenen ürün alanları**         | Alacak hesapları                                                                       |
| **Durum**                         | Kullanımı sonlandırıldı: Bu özellik için kaldırma tarihi belirlenmedi.                            |

### <a name="external-inventory-for-poland"></a>Polonya için harici stok

Satınalma olmadan satış için bir satıcıdan alınan malların kanıtı. Dış stokta işlenen mallar standart stoğu etkilemez, satılabilir ve ardından otomatik olarak satın alınabilir. Bu işlem gerçek stok hareketleri oluşturur.

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Kullanımı sonlandırma/kaldırma nedeni** | Başka bir özellik ile değiştirildi                                    |
| **Başka bir özellik ile değiştirildi?**   | Evet, çekirdek Gelen konsinye işlevselliği                |
| **Etkilenen ürün alanları**         | Borç hesapları, Stok yönetimi                         |
| **Durum**                         | Kullanımı sonlandırıldı: Bu özellik için kaldırma tarihi belirlenmedi. |

### <a name="financial-reports-generator-for-eastern-europe"></a>Doğu Avrupa için mali rapor oluşturucusu

Muhasebe ve vergi raporları için veri toplamak ve XLS ve DOC rapor şablonlarına veri dışa aktarmak için bir araç kullanılır.

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Kullanımı sonlandırma/kaldırma nedeni** | Sınırlı kullanım                                                                            |
| **Başka bir özellik ile değiştirildi?**   | Hayır. Araç gelecekteki sürümlerde Elektronik raporlama yapılandırmaları ile değiştirilecektir. |
| **Etkilenen ürün alanları**         | Genel Muhasebe                                                                           |
| **Durum**                         | Kullanımı sonlandırıldı: Bu özellik için kaldırma tarihi belirlenmedi.                           |

### <a name="import-of-customer-payment-transactions-for-finland"></a>Finlandiya için müşteri ödeme hareketlerini içe aktarma

Finlandiya ödemelerinde müşteri ödeme hareketlerini banka tarafından sağlanan harici bir dosyadan içe aktarmak için bir içe aktarma biçimi seçebilirsiniz.

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Kullanımı sonlandırma/kaldırma nedeni** | Ödeme biçimi artık kullanılmamaktadır.                                                     |
| **Başka bir özellikle mi değiştirildi?**   | Evet, ISO20022 CAMT.054 bildirimi içe aktarması. |
| **Etkilenen ürün alanları**         | Alacak hesapları                                                                       |
| **Durum**                         | Kullanımı sonlandırıldı: Bu özellik için kaldırma tarihi belirlenmedi.                            |

### <a name="import-of-payment-transactions-into-a-general-ledger-journal-for-finland"></a>Finlandiya için ödeme hareketlerini genel muhasebe günlüğüne içe aktarma

Muhasebe hareketlerini genel muhasebeye içe aktarmak için Finlandiya'ya özgü bir biçim kullanılır.

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Kullanımı sonlandırma/kaldırma nedeni** | Ödeme biçimi artık kullanılmamaktadır.                                                     |
| **Başka bir özellikle mi değiştirildi?**   | Evet, ISO20022 CAMT.053 banka ekstresi gelişmiş banka mutabakatını kullanarak içe aktarma. |
| **Etkilenen ürün alanları**         | Alacak hesapları                                                                       |
| **Durum**                         | Kullanımı sonlandırıldı: Bu özellik için kaldırma tarihi belirlenmedi.                            |

### <a name="integration-with-isabel-synchronized-cis-for-belgium"></a>Belçika için Isabel ile tümleştirme eşitlendi (CIS)

Isabel, elektronik bankacılık için Avrupa'daki çerçevedir ve Belçika'da fiili bir standarttır.

|  &nbsp; | &nbsp; |
|------------|--------------------|
| **Kullanımı sonlandırma/kaldırma nedeni** | Isabel istemcisi ile tümleştirme kaldırıldı.   |
| **Başka bir özellik ile değiştirildi?**   | Hayır. Belçika için artık kullanılmayan ödeme biçimleri, ISO20022 Alacak transferi ödeme biçimi ile değiştirildi. |
| **Etkilenen ürün alanları**         | Borç hesapları     |
| **Durum**                         | Kullanımı sonlandırıldı: Bu özellik için kaldırma tarihi belirlenmedi.    |

### <a name="modifications-in-the-chart-of-accounts-and-accounting-rules-for-spain"></a>İspanya için hesap planı ve muhasebe kurallarındaki değişiklikler

Bu özellik, İspanya için hesap planında ve muhasebe kurallarındaki değişiklikler için kullanılır. Eski hesap planını yeni hesap planına dönüştürmeye yardımcı olmak için hesapları eşler ve farklı hesap numaralarına nakledilseler bile önceki mali yıl ile yeni mali yılı karşılaştırır.

|  &nbsp; |&nbsp;  |
|------------|--------------------|
| **Kullanımı sonlandırma/kaldırma nedeni** | Sınırlı kullanım                                                  |
| **Başka bir özellik ile değiştirildi?**   | Hayır                                                             |
| **Etkilenen ürün alanları**         | Genel muhasebe                                                 |
| **Durum**                         | Kullanımı sonlandırıldı: Bu özellik için kaldırma tarihi belirlenmedi. |

### <a name="pagamento-fornittori-vendor-payment-format"></a>Pagamento Fornittori satıcı ödemesi biçimi

Alacak transferleri için eski İtalyan ödeme biçimi.

| &nbsp;  |&nbsp;  |
|------------|--------------------|
| **Kullanımı sonlandırma/kaldırma nedeni** | Ödeme biçimi artık kullanılmamaktadır.                          |
| **Başka bir özellik ile değiştirildi?**   | Evet, İtalya için ISO20022 Alacak transferi ödeme biçimi         |
| **Etkilenen ürün alanları**         | Borç hesapları                                               |
| **Durum**                         | Kullanımı sonlandırıldı: Bu özellik için kaldırma tarihi belirlenmedi. |

### <a name="payment-export-formats-for-estonia"></a>Estonya için ödemeleri dışa aktarma biçimleri

Telehansa ve Teleservice biçimleri banka ödemesi dışa aktarımı için kullanılır.

| &nbsp;  |&nbsp;  |
|------------|--------------------|
| **Kullanımı sonlandırma/kaldırma nedeni** | Ödeme biçimleri artık kullanılmamaktadır.                        |
| **Başka bir özellik ile değiştirildi?**   | Evet, Estonya için ISO20022 Alacak transferi ödeme biçimi       |
| **Etkilenen ürün alanları**         | Borç hesapları                                               |
| **Durum**                         | Kullanımı sonlandırıldı: Bu özellik için kaldırma tarihi belirlenmedi. |

### <a name="payment-file-archive-for-norway"></a>Norveç için ödeme dosya arşivi

Ödeme dosyaları oluşturulduğunda dosya arşivi, dosyalar önceden yazılmış veya okunmuş olsalar bile oluşturulan tüm dosyaları otomatik olarak arşivler.

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Kullanımı sonlandırma/kaldırma nedeni** | Başka bir özellik ile değiştirildi                                        |
| **Başka bir özellik ile değiştirildi?**   | Evet, Arşivlenen elektronik raporlama işleri                            |
| **Etkilenen ürün alanları**         | Borç hesapları, Alacak hesapları, Organizasyon yönetimi |
| **Durum**                         | Kullanımı sonlandırıldı: Bu özellik için kaldırma tarihi belirlenmedi.     |

### <a name="payment-import-formats-for-estonia"></a>Estonya için ödemeleri içe aktarma biçimleri

Telehansa ve TeleTeenus biçimleri banka ödemesi içe aktarımı için kullanılır.

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Kullanımı sonlandırma/kaldırma nedeni** | Ödeme biçimleri artık kullanılmamaktadır.                                                    |
| **Başka bir özellikle mi değiştirildi?**   | Evet, ISO20022 CAMT.054 banka bildirimi içe aktarması. |
| **Etkilenen ürün alanları**         | Alacak hesapları                                                                        |
| **Durum**                         | Kullanımı sonlandırıldı: Bu özellik için kaldırma tarihi belirlenmedi.                             |

### <a name="payroll-information-in-human-resources"></a>İnsan Kaynakları'ndaki bordro bilgileri

İnsan Kaynakları bordro bilgileri

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Kullanımı sonlandırma/kaldırma nedeni** | Bu işlevin yerini temel Bordro ve İnsan Kaynakları sayfaları almıştır.  |
| **Başka bir özellik ile değiştirildi?**   | **Avantajlar**, **Kazançlar** ve daha önce ABD Bordro'da olan diğer ilgili sayfalar yeniden yapılandırıldı ve artık harici bordro işlemeyi desteklemeye yardımcı olacak temel İnsan Kaynakları yapılandırmasının bir parçasılar. Bu işleve **İnsan Kaynakları 1** \> **Bordro** konfigürasyon anahtarı kullanılarak erişilir. |
| **Etkilenen ürün alanları**         | İnsan kaynaklarını, Bordro   |
| **Durum**                         | Dynamics 365 for Operations sürüm 1611 itibarıyla kaldırıldı.    |

### <a name="performance-management-goal-workflow"></a>Performans yönetimi hedefi iş akışı

Performans yönetimi, hedef yönetimini ve performans gözden geçirmeleri ile tümleştirmeyi içerir.

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Kullanımı sonlandırma/kaldırma nedeni** | Performans yönetimi yeniden tasarlanmıştır ve hedef sayfalarının sayısı işlemi basitleştirecek şekilde azaltılmıştır.                 |
| **Başka bir özellik ile değiştirildi?**   | Hayır. Hedefler yöneticiler tarafından Yönetici Self Servis portalından görülebilir, değiştirilebilir ve görüntülenebilir. |
| **Etkilenen ürün alanları**         | İnsan sermayesi yönetimi       |
| **Durum**                         | Dynamics 365 for Operations sürüm 1611 itibarıyla kaldırıldı.    |

### <a name="postgirot-and-postgirot-utland-payment-formats-for-sweden"></a>İsveç için Postgirot ve Postgirot Utland ödeme biçimleri

İsveç için Postgirot ve Postgirot Utland ödeme biçimleri.

|&nbsp;   |&nbsp;  |
|------------|--------------------|
| **Kullanımı sonlandırma/kaldırma nedeni** | Ödeme biçimleri artık kullanılmamaktadır.                        |
| **Başka bir özellik ile değiştirildi?**   | Evet, İsveç için ISO20022 Alacak transferi ödeme biçimi        |
| **Etkilenen ürün alanları**         | Borç hesapları                                               |
| **Durum**                         | Kullanımı sonlandırıldı: Bu özellik için kaldırma tarihi belirlenmedi. |

### <a name="radio-frequency-identifier"></a>Radyo frekansı kimlik tanımlayıcı

Radyo Frekans Kimlik Belirleme (RFID), kimlik bilgilerini saklamak için elektronik etiket kullanan ve okuyucunun kimlik saptama verisini yakalaması için doğrudan yöneltmeye gerek duymayan bir veri toplama teknolojisidir.

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Kullanımı sonlandırma/kaldırma nedeni** | Düşük müşteri kullanımı ve sınırlı özellik kümesi.   |
| **Başka bir özellik ile değiştirildi?**   | Hayır                                              |
| **Etkilenen ürün alanları**         | Stok Yönetimi                            |
| **Durum**                         | Dynamics 365 for Operations 1611 itibarıyla kaldırıldı. |

### <a name="report-about-state-invoices-numbering-for-latvia"></a>Letonya için Fatura numarasının belirtilmesi hakkında rapor

Letonya mevzuatı satış faturalarının numaralandırılması hakkında belirli kurallar sağlar. İşlev, kullanıcı veya kullanıcı grubuna göre satış faturalarına belirli numaralar atamanızı sağlar. Ardından bir rapor veya bir XML dosyası oluşturabilirsiniz. Ayrıca, kullanılan fatura numaraları hakkında bir rapor yazdırabilirsiniz.

| &nbsp;  |&nbsp;  |
|------------|--------------------|
| **Kullanımı sonlandırma/kaldırma nedeni** | Artık fatura numarasının belirtilmesinin saklanması gerekmez. Kullanılan fatura numaraları hakkında rapor artık gerekli değildir. |
| **Başka bir özellik ile değiştirildi?**   | Hayır       |
| **Etkilenen ürün alanları**         | Alacak hesapları    |
| **Durum**                         | Kullanımı sonlandırıldı: Bu özellik için kaldırma tarihi belirlenmedi.  |

### <a name="set-up-the-names-of-the-manager-and-general-accountant-of-a-company-for-lithuania"></a>Litvanya için yönetici adları ve bir şirketin genel muhasebesini ayarlama

Yönetici adları ve şirketin genel muhasebesi şirket bilgilerinde belirtilebilir ve farklı yerel rapor çıktılarında kullanılabilir.

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Kullanımı sonlandırma/kaldırma nedeni** | Başka bir özellik ile değiştirildi                                     |
| **Başka bir özellik ile değiştirildi?**   | Evet, yetkililer kurulumu aynı amaç için kullanılabilir.   |
| **Etkilenen ürün alanları**         | Borç hesapları, Alacak hesapları, Nakit ve banka yönetimi |
| **Durum**                         | Kullanımı sonlandırıldı: Bu özellik için kaldırma tarihi belirlenmedi.  |

### <a name="shipping-carrier-interface"></a>Sevkiyat taşıyıcısı arabirimi

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Kullanımı sonlandırma/kaldırma nedeni** | Tekrar eden işlevsellik   |
| **Başka bir özellik ile değiştirildi?**   | Kısmen Taşıma yönetimiyle değiştirildi |
| **Etkilenen ürün alanları**         | Satış ve pazarlama, Stok Yönetimi  |
| **Durum**                         | Dynamics 365 for Operations sürüm 1611 itibarıyla kaldırıldı.  |

### <a name="telepay-payment-formats-for-norway"></a>Norveç için Telepay ödeme biçimleri

Telepay ödeme biçimleri, satıcı ödemesi dışa aktarımını (alacak transferi) ve müşteri ödeme tahsilatını (otomatik ödeme) içerir.

|&nbsp;   |&nbsp;  |
|------------|--------------------|
| **Kullanımı sonlandırma/kaldırma nedeni** | Ödeme biçimleri artık kullanılmamaktadır.                                                        |
| **Başka bir özellik ile değiştirildi?**   | Evet, ISO20022 kredi transfer ödeme biçimi ve Norveç için AvtaleGiro müşteri ödeme biçiminin yanı sıra pain.002 ve camt.054 banka bildirimi geri alma dosyalarını içe aktarma. |
| **Etkilenen ürün alanları**         | Borç hesapları, Alacak hesapları                                                          |
| **Durum**                         | Kullanımı sonlandırıldı: Bu özellik için kaldırma tarihi belirlenmedi.                                 |

### <a name="vendor-payment-export-formats-for-finland"></a>Finlandiya için satıcı ödeme dışa aktarma biçimleri

Finlandiya için ödemeleri dışa aktarmak üzere iki biçim kullanılabilir. Yurtiçi ödemeleri için kullanılan LM02 (FI) ve yurtdışı ödemeleri için kullanılan LUM2 (FI).

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Kullanımı sonlandırma/kaldırma nedeni** | Ödeme biçimleri artık kullanılmamaktadır.                        |
| **Başka bir özellik ile değiştirildi?**   | Evet, Finlandiya için ISO20022 Alacak transferi ödeme biçimi       |
| **Etkilenen ürün alanları**         | Borç hesapları                                               |
| **Durum**                         | Kullanımı sonlandırıldı: Bu özellik için kaldırma tarihi belirlenmedi. |

### <a name="warehouse-management-ii"></a>Ambar yönetimi II

|  &nbsp; |&nbsp;  |
|------------|--------------------|
| **Kullanımı sonlandırma/kaldırma nedeni** | **Stok yönetimi** modülündeki Ambar Yönetimi II çözümü (WMS II) Dynamics AX 2012 R3'de yayımlanmış olan **Ambar yönetimi** modülündeki işlevleri tekrarlar.                                                                         |
| **Başka bir özellikle mi değiştirildi?**   | AX 2012 R3, Dynamics AX 2012 R3 CU8 ve Dynamics AX 2012 R3 CU9'da yayınlanmış olan **Ambar yönetimi** modülü, Ambar yönetimi II özelliklerinin yerini almıştır. Yeni modül Ambar yönetimi II'dekinden daha gelişmiş özelliklere ve daha esnek ambar yönetim süreçlerine sahiptir. |
| **Etkilenen ürün alanları**         | Stok Yönetimi, satış ve pazarlama, tedarik ve kaynak atama   |
| **Durum**                         | Dynamics 365 for Operations sürüm 1611 itibarıyla kaldırıldı.    |

### <a name="worker-reminders-in-human-resources"></a>İnsan Kaynakları'ndaki çalışan anımsatıcıları

İnsan Kaynakları bordro bilgileri

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Kullanımı sonlandırma/kaldırma nedeni** | Düşük kullanım                                                           |
| **Başka bir özellik ile değiştirildi?**   | Hayır                                                                  |
| **Etkilenen ürün alanları**         | İnsan kaynakları                                                     |
| **Durum**                         | Dynamics 365 for Operations sürüm 1611 itibarıyla kaldırıldı |

### <a name="workflow-for-creating-goals"></a>Hedefleri oluşturmak için iş akışı

Personel hedeflerini oluşturmayı yöneten iş akışı, performans yönetim işleminin düzenlenmesine yardımcı olan birkaç iş akışından biridir.

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Kullanımı sonlandırma/kaldırma nedeni** | Performans yönetimi Finance and Operations içerisinde tümüyle baştan tasarlanmıştır.     |
| **Başka bir özellikle mi değiştirildi?**   | Yeniden tasarlanan Performans yönetimi özelliği hedef içeriği, ilerlemeyi izlemek için kullanılan ölçümler ve destekleyici belge eki üzerinde daha fazla kontrol sağlar. Hedefler şablon olarak saklanabilir ve daha sonra yeniden kullanılabilir. Bu özellik personeliniz için ek hedefleri daha hızlı bir şekilde ayarlamanıza yardımcı olabilir. |
| **Etkilenen ürün alanları**         | İnsan sermayesi yönetimi                 |
| **Durum**                         | Dynamics 365 for Operations sürüm 1611 itibarıyla kaldırıldı. |

## <a name="dynamics-ax-70"></a>Dynamics AX 7.0 


### <a name="ability-to-cancel-changes-to-a-vendor-invoice"></a>Satıcı faturasında yapılan değişiklikleri iptal yeteneği

| &nbsp;  |&nbsp;  |
|------------|--------------------|
| **Kullanımı sonlandırma/kaldırma nedeni** | Performans geliştirmesi        |
| **Başka bir özellik ile değiştirildi?**   | Hayır                             |
| **Etkilenen ürün alanları**         | Borç hesapları               |
| **Durum**                         | Dynamics AX 7.0 itibarıyla kaldırıldı. |

### <a name="aif-axd-and-axbc-integrations"></a>AIF, AxD ve AxBC entegrasyonlar

Uygulama Tümleştirme Çerçevesi (AIF) içerisinde veriler, hizmetler olarak gösterilen iş mantığı üzerinden dış sistemlerle değiştirilebilir. Dynamics AX, .NET Business Connector (AxBC) ve belgelere dayanan hizmetleri içerir. Bir belge, XML kullanılarak oluşturulur. XML, bir *ileti* oluşturmak için eklenen ve Dynamics AX içine veya dışına transfer edilebilen üstbilgi bilgilerini içerir. Belgelerin örnekleri satınalma siparişleri ve satış siparişlerini içerir. Ancak, bir müşteri gibi hemen hemen her varlık, bir belge tarafından temsil edilebilir. Belgelere dayanan hizmetler **Axd \<Document\>** sınıflarını kullanır.

|  &nbsp; | &nbsp; |
|------------|--------------------|
| **Kullanımı sonlandırma/kaldırma nedeni** | AIF ve AxDs mimarileri bir bulut hizmetine ölçeklenmiş değildirler. Toplu alma etrafında performans sorunları vardı.                                        |
| **Başka bir özellik ile değiştirildi?**   | Bu özelliğin yerini tekrar eden toplu içe aktarma/dışa aktarma işlemlerini destekleyen, Veri İçe Aktarma/Dışa Aktarma çerçevesi almıştır. AxBC için gerçek tabloları kullanmanızı öneririz. |
| **Etkilenen ürün alanları**         | AxDs, AxBCs ve AIF   |
| **Durum**                         | Dynamics AX 7.0 itibarıyla kaldırıldı.   |

### <a name="billing-code-rate-scripts"></a>Fatura kodu oran kodları

Faturalama kodları, faturalama kodları için faturalama oranlarını hesaplamakta kullanılır. Bu kodlar, C Sharp veya Visual Basic programlama dillerinde özel geliştirme gerektirmekte. Dynamics AX'in güncel sürümünde, **faturalama kodu oran komut dosyaları** desteklenmemektedir.

| &nbsp;  |&nbsp;  |
|------------|--------------------|
| **Kullanımı sonlandırma/kaldırma nedeni** | Özel C Sharp veya Visual Basic komut satırları için destek, Dynamics AX 7.0'a eklenmemişti. |
| **Başka bir özellikle mi değiştirildi?**   | Hayır                                                                                      |
| **Etkilenen ürün alanları**         | Kamu sektörü, Alacak hesapları                                    |
| **Durum**                         | Dynamics AX 7.0 itibarıyla kaldırıldı.                                                          |

### <a name="boms-without-bom-versions"></a>Ürün reçetesi sürümleri olmayan ürün reçeteleri

**BOM sürümleri** yapılandırma anahtarı devre dışı bırakıldığında, ürün reçetesi (BOM) sürümleri tüm formlarda gizleniyordu ve sistem serbest bırakılan ürünler ve ürün reçeteleri arasında bir 1:1 ilişkisini zorluyordu. **BOM sürümleri** yapılandırma anahtarı, Dynamics AX'in geçerli sürümünde devre dışı bırakılamaz.

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Kullanımı sonlandırma/kaldırma nedeni** | Ürün reçetesi sürümlerini denetlemek için konfigürasyon anahtarı kullanmak bir bulut ortamında ölçeklendirilemez. |
| **Başka bir özellik ile değiştirildi?**   | Hayır                                                                                      |
| **Etkilenen ürün alanları**         | Ürün bilgileri yönetimi, Stok Yönetimi                                    |
| **Durum**                         | Dynamics AX 7.0 itibarıyla kaldırıldı.                                                          |

### <a name="brazilian-bordero"></a>Brazilian Bordero

Brezilya şirketleri için belirli ödeme yöntemi

|  &nbsp; | &nbsp; |
|------------|--------------------|
| **Kullanımı sonlandırma/kaldırma nedeni** | Brazilian Bordero ödeme yöntemi için destek Brezilya yerelleştirmesinden kaldırılmıştır |
| **Başka bir özellik ile değiştirildi?**   | Hayır   |
| **Etkilenen ürün alanları**         | Borç hesapları   |
| **Durum**                         | Kullanımı sonlandırıldı: Bu özellik için kaldırma tarihi belirlenmedi. |

### <a name="brazilian-sintegra-statement"></a>Brazilian Sintegra ekstresi

ICMS vergisi için federal vergi ekstresi

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Kullanımı sonlandırma/kaldırma nedeni** | Bu ekstre bazı Brezilya eyaletlerinde artık kullanılmamaktadır. |
| **Başka bir özellik ile değiştirildi?**   | Hayır. Kullanıcılar Genel Elektronik raporlama aracını belirli durumlarda gerektiğinde ekstreyi yapılandırmak için kullanabilir. |
| **Etkilenen ürün alanları**         | Mali defterler    |
| **Durum**                         | Kullanımı sonlandırıldı: Bu özellik için kaldırma tarihi belirlenmedi.   |

### <a name="brazilian-scan-contingency-mode-for-nf-e"></a>NF-e için Brezilya SCAN yedeği modu

(SCAN) yedeği ortamı, Secretaria da Fazenda (SEFAZ) ortamı kullanılabilir olmadığında bir Nota Fiscal eletrônica (NF-e) durumunu oluşturmak, dışa aktarmak ve içe aktarmak için kullanılır.

|  &nbsp; | &nbsp; |
|------------|--------------------|
| **Kullanımı sonlandırma/kaldırma nedeni** | Bu yedek yöntem, Brezilya eyaletlerinin tamamında artık geçersizdir |
| **Başka bir özellik ile değiştirildi?**   | Hayır                                                                          |
| **Etkilenen ürün alanları**         | Alacak hesapları                                                         |
| **Durum**                         | Kullanımı sonlandırıldı: Bu özellik için kaldırma tarihi belirlenmedi.              |

### <a name="business-analyzer"></a>İş Çözümleyicisi

Bu mobil uygulama kullanıcıların anahtar iş ölçümlerini gözden geçirmelerini sağlar.

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Kullanımı sonlandırma/kaldırma nedeni** | Bu işlev başka bir özellik ile değiştirilmiştir.   |
| **Başka bir özellikle mi değiştirildi?**   | Microsoft Power BI için Finansal performans içeriği izleme paketi, daha önce Business Analyzer'da bulunan önemli mali ölçümleri içerecektir. |
| **Etkilenen ürün alanları**         | Genel muhasebe      |
| **Durum**                         | Kullanımı sonlandırıldı: İş Çözümleyicisi kullanımı sonlandırıldı.    |

### <a name="business-statistics"></a>İşletme istatistikleri

Kuruluşun performansını analiz etmenize yardımcı olabilecek iş istatistiği sorgularının kurulumu

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Kullanımı sonlandırma/kaldırma nedeni** | İş zekasına (BI) eski yaklaşım, düşük müşteri kullanımı ve sınırlı özellik kümesine |
| **Başka bir özellikle mi değiştirildi?**   | Dynamics AX'in geçerli sürümü için yeni BI çözümleri                                      |
| **Etkilenen ürün alanları**         | Tedarik ve kaynak hizmeti, Borç hesapları, Satış ve pazarlama, Alacak hesapları         |
| **Durum**                         | Dynamics AX 7.0 itibarıyla kaldırıldı.                                                               |

### <a name="change-document-date-function-in-invoice-approval-journal"></a>Fatura onay günlüğündeki belge tarihi değiştirme işlevi

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Kullanımı sonlandırma/kaldırma nedeni** | Düşük kullanım                                                               |
| **Başka bir özellik ile değiştirildi?**   | Evet. Deftere nakledilen satıcı hareketi üzerindeki belge tarihi değiştirilebilir. |
| **Etkilenen ürün alanları**         | Borç hesapları                                                        |
| **Durum**                         | Dynamics AX 7.0 itibarıyla kaldırıldı.                                          |

### <a name="clieop03-payment-format-for-the-netherlands"></a>Hollanda için ClieOp03 ödeme biçimi

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Kullanımı sonlandırma/kaldırma nedeni** | Biçim, artık tek Euro ödemeleri alan (SEPA) işlevi tarafından değiştirildiğinden, Hollanda'da artık geçerli değildir. |
| **Başka bir özellik ile değiştirildi?**   | SEPA ödemeleri dışa aktarımı  |
| **Etkilenen ürün alanları**         | Tüm modüller     |
| **Durum**                         | Kullanımı sonlandırıldı: Bu özellik için kaldırma tarihi belirlenmedi.   |

### <a name="compliance-center"></a>Uyumluluk Merkezi

Uyumluluk Merkezi, Sarbanes-Oxley Yasası ilgili uyumluluk girişimleriyle belgelerine gereksinimlerini yönetmek kullanılan bir Kurumsal Portal sitesiydi.

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Kullanımı sonlandırma/kaldırma nedeni** | Müşteri kullanım eksikliği. Microsoft SharePoint Uyumluluk Merkezi'nde sunulmuş olanlarla aynı özellikleri içerir. |
| **Başka bir özellik ile değiştirildi?**   | Hayır   |
| **Etkilenen ürün alanları**         | Uyumluluk ve dahili kontroller  |
| **Durum**                         | Dynamics AX 7.0 itibarıyla kaldırıldı.    |

### <a name="connector-for-microsoft-dynamics"></a>Microsoft Dynamics için Bağlayıcı

Bu araç, anahtar verileri Microsoft Dynamics CRM'den Dynamics ERP uygulamalarına tümleştirmek için kullanıldı.

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Kullanımı sonlandırma/kaldırma nedeni** | Bu işlev başka bir özellik ile değiştirilmiştir. |
| **Başka bir özellikle mi değiştirildi?**   | Dataverse                                      |
| **Etkilenen ürün alanları**         | Dynamics için Bağlayıcı                         |
| **Durum**                         | Dynamics AX 7.0 itibarıyla kaldırıldı.                           |

### <a name="container-unit-and-multi-dimension-on-hand"></a>Eldeki konteyner birimi ve çoklu boyut

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Kullanımı sonlandırma/kaldırma nedeni** | Tekrar eden işlevsellik |
| **Başka bir özellikle mi değiştirildi?**   | Evet. AX 2012'den itibaren bu işlevin yerini konsolide toplu iş siparişleri özellik kümesi almıştır. Bu özellik kümesi konsolide eldeki görünümünü içerir. |
| **Etkilenen ürün alanları**         | Ürün bilgileri yönetimi, Üretim kontrol, Stok Yönetimi, Satış ve pazarlama  |
| **Durum**                         | Dynamics AX 7.0 itibarıyla kaldırıldı. |

### <a name="cue-group-metadata"></a>İşaret Grup meta verileri

|  &nbsp; | &nbsp; |
|------------|--------------------|
| **Kullanımı sonlandırma/kaldırma nedeni** | İşaret grupları, bilgi alanında bir veya daha fazla ipucu görüntülemek için kullanılıyordu. Sınırlı kullanım vardı ve ayrıca performans kaygıları da mevcuttu çünkü bir üst formdaki değişiklik, her İşaret grubundaki her bir İşarette bir sorguya sebep oluyordu. |
| **Başka bir özellik ile değiştirildi?**   | Hayır      |
| **Etkilenen ürün alanları**         | Tüm modüller    |
| **Durum**                         | Dynamics AX 7.0 itibarıyla kaldırıldı.  |

### <a name="cue-metadata"></a>İşaret meta verileri

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Kullanımı sonlandırma/kaldırma nedeni** | İşaret meta veriler, sayma ve toplama bilgileri ile sınırlıydı.    |
| **Başka bir özellik ile değiştirildi?**   | Döşeme meta veri modelleme için daha fazla esneklik sağlamak amacıyla kullanılmaya başlandı. Örneğin, geçerli sayma, gezinti ve anahtar performans göstergeleri (APG) modelleyebilirsiniz. Sayım döşeme meta verileri, işaret meta verilerinin doğrudan yerini almıştır. |
| **Etkilenen ürün alanları**         | Tüm modüller           |
| **Durum**                         | Dynamics AX 7.0 itibarıyla kaldırıldı      |

### <a name="danish-check-format"></a>Danimarka çek biçimi

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Kullanımı sonlandırma/kaldırma nedeni** | Danimarka çek biçimi düzeni için destek kaldırılmıştır ve rapor DK yerelleştirmeden silinmiştir. |
| **Başka bir özellik ile değiştirildi?**   | Hayır    |
| **Etkilenen ürün alanları**         | Tüm modüller    |
| **Durum**                         | Kullanımı sonlandırıldı: Bu özellik için kaldırma tarihi belirlenmedi.  |

### <a name="data-partitions"></a>Veri bölümleri

Veri bölümleri, Dynamics AX veritabanındaki verinin mantıksal bir ayrımını sağlar.

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Kullanımı sonlandırma/kaldırma nedeni** | Veri bölümleri, veri yalıtımı sağlamak için Dynamics AX 2012 R2'de kullanılmaya başlanmıştır. Yaygın bir senaryoda, bir şirketin bağlı kuruluşları vardır ve her iki bağlı kuruluş da aynı BT departmanı tarafından yönetilseler bile bir bağlı kuruluşun verisinin diğer bağlı kuruluşa görünür olmaması gerekir. Ancak, yeni bölümler oluşturmak, bunları veri ile doldurmak ve bölüm verilerini yedeklemek için ekstra kodlar ve program boyunca genel yönetim giderleri gerekir. Hizmet olarak platform (PaaS) veritabanına (Microsoft Azure SQL veritabanı) erişimimizin olduğu bulutta, veritabanını bir yalıtım konteyneri olarak kullanmak program içinde yalıtmaya göre çok daha etkilidir. Veri bölümlemenin bağlı kuruluşlar, çoklu kiracılar veya yalnızca ölçek için gerekli olup olmadığına bakılmaksızın, senaryoların birden çok veritabanı veya birden çok Finance and Operations kurulumu ile daha iyi işlenebileceğine inanırız. |
| **Başka bir özellikle mi değiştirildi?**   | Veritabanı düzeyinde ayırma önemli bir sorunsa, veri bölümleri kullanan müşterilerin birden çok Finance and Operations kurulumu kullanması gerekir.    |
| **Etkilenen ürün alanları**         | Tüm modüller  |
| **Durum**                         | Dynamics AX 7.0 itibarıyla kaldırıldı.  |


### <a name="database-and-file-share-storage-for-attachments"></a>Ekler için veritabanı ve dosya paylaşım depolama

Dynamics AX 2012, eklerin veritabanında ve dosya paylaşımında depolanmasına izin vermekteydi. Bu seçeneklerin her ikisi de artık desteklenmiyor.

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Kullanımı sonlandırma/kaldırma nedeni** | Dosya paylaşım depolaması, bulutta barındırılan ortamlar yerel dosya paylaşımlarıyla iletişim kuramadığı için artık desteklenmiyor. Veritabanı depolama, Azure Blob depolama kullanıldığından kullanım dışı bırakıldı. Azure Blob depolama, veritabanında depolamaya eşdeğerdir çünkü belgeler yalnızca Finance and Operations istemci formları üzerinden erişilebilir. Bu, veritabanı performansını olumsuz etkilemeyen depolama sağlama faydasını sunar. Blob depolama, Belge Yönetimi için varsayılan mekanizmadır ve hemen çalışır. |
| **Başka bir özellik ile değiştirildi?**   | Veritabanı depolama, Azure Blob depolama kullanıldığından kullanım dışı bırakıldı.   |
| **Etkilenen ürün alanları**         | Tüm modüller  |
| **Durum**                         | Dynamics AX 7.0 itibarıyla kaldırıldı.   |

### <a name="delimitation"></a>Sınırlandırma

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Kullanımı sonlandırma/kaldırma nedeni** | İşlev için kullanım bulunamadı. |
| **Başka bir özellik ile değiştirildi?**   | Hayır                                     |
| **Etkilenen ürün alanları**         | Saat ve işe devam                    |
| **Durum**                         | Dynamics AX 7.0 itibarıyla kaldırıldı.         |

### <a name="desktop-client"></a>Masaüstü istemcisi

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Kullanımı sonlandırma/kaldırma nedeni** | Dynamics AX İstemci deneyimi, platformlar ve aygıtlar üzerinde kullanılabilirliğini artırmak için tasarlanmıştır.                      |
| **Başka bir özellik ile değiştirildi?**   | Yeni web istemci masaüstü formu meta verileri ve zengin web platformu sunmak için değiştirilmiş programlama modeline dayanır. |
| **Etkilenen ürün alanları**         | Tüm modüller  |
| **Durum**                         | Dynamics AX 7.0 itibarıyla kaldırıldı.   |

### <a name="direct-database-connection"></a>Doğrudan veritabanı bağlantısı

Dynamics AX 2012 R3 içerisinde, Retail Modern POS , Kanal Veritabanına, Kuruluş POS'a benzer şekilde doğrudan bağlanamadı. Bu, Retail Modern POS'un, Perakende Sunucusu üzerinden iletişim kurarken standart iletişim yöntemine ek olarak oluştu.

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Kullanımı sonlandırma/kaldırma nedeni** | Doğrudan veritabanı bağlantısı, daha düşük güvenlik protokolleri gerektirdi ve öncelikli olarak en yüksek seviye performansı elde etmek için kullanıldı. Finance and Operations içerisinde gerçekleşen performans ve güvenlik geliştirmeleri yüzünden, bu işlev artık çözdüğünden daha fazla soruna neden olmaktadır. |
| **Başka bir özellik ile değiştirildi?**   | Hayır. Artık yalnızca standart Perakende Sunucu iletişimi desteklenmektedir.  |
| **Etkilenen ürün alanları**         | Kanal Veritabanı/Retail Modern POS   |
| **Durum**                         | Dynamics AX 7.0 itibarıyla kaldırıldı.  |

### <a name="dutch-swift-mt940"></a>Felemenkçe SWIFT MT940

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Kullanımı sonlandırma/kaldırma nedeni** | Yerelleştirilmiş işlevsellik yerine artık genel işlevler kullanılır.                    |
| **Başka bir özellik ile değiştirildi?**   | Evet, bu işlevin yerini Gelişmiş banka mutabakatı işlevi aldı. |
| **Etkilenen ürün alanları**         | Tüm modüller                                                                              |
| **Durum**                         | Kullanımı sonlandırıldı: Bu özellik için kaldırma tarihi belirlenmedi.                           |

### <a name="ebilanz-xbrl-for-germany"></a>eBilanz (Almanya için XBRL)

Bu işlev Alman eBilanz taksonomisi için özel olarak tasarlanmış olan Genişletilebilir İş Raporlama Dili (XBRL) çıkışı sağlamaktaydı.

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Kullanımı sonlandırma/kaldırma nedeni** | Müşteri kullanım eksikliği  |
| **Başka bir özellik ile değiştirildi?**   | Bu özelliğin yerini bir başkası almadı ancak Almanya pazarı için zengin XBRL işlevselliği sağlayan birden çok özelleşmiş XBRL paketi sunulmuştur. |
| **Etkilenen ürün alanları**         | Management Reporter      |
| **Durum**                         | Kullanımı sonlandırıldı: Bu özellik için kaldırma tarihi belirlenmedi.  |

### <a name="enterprise-portal-client"></a>Kurumsal Portal istemcisi

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Kullanımı sonlandırma/kaldırma nedeni** | Bir tek istemci platformu sağlandı.  |
| **Başka bir özellik ile değiştirildi?**   | Yeni web istemci masaüstü formu meta verileri ve zengin web platformu sunmak için değiştirilmiş programlama modeline dayanır. |
| **Etkilenen ürün alanları**         | Tüm modüller  |
| **Durum**                         | Dynamics AX 7.0 itibarıyla kaldırıldı.   |

### <a name="environmental-sustainability"></a>Ortam sürdürülebilirliği

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Kullanımı sonlandırma/kaldırma nedeni** | Düşük müşteri kullanımı ve sınırlı özellik kümesi  |
| **Başka bir özellik ile değiştirildi?**   | Hayır              |
| **Etkilenen ürün alanları**         | Uyumluluk ve dahili kontroller, Borç hesapları  |
| **Durum**                         | Dynamics AX 7.0 itibarıyla kaldırıldı. |

### <a name="form-activex-and-managed-host-controls"></a>Form ActiveX ve yönetilen konak denetimleri

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Kullanımı sonlandırma/kaldırma nedeni** | ActiveX ve yönetilebilir konak denetimleri artık kullanılmayan masaüstü istemciyi temel alır. |
| **Başka bir özellik ile değiştirildi?**   | Genişletilebilir denetim çerçevesi HTML, CSS ve JavaScript'e dayanan yeni denetimleri oluşturmayı destekler ve Microsoft Visual Studio Tooling ortamındaki birinci sınıf bir denetimdir. |
| **Etkilenen ürün alanları**         | Tüm modüller     |
| **Durum**                         | Dynamics AX 7.0 itibarıyla kaldırıldı.       |

### <a name="generate-prenotes-by-using-a-batch"></a>Bir toplu işlem kullanarak açık provizyon oluşturmak

Açık provizyon oluşturma, bir toplu iş kullanarak yapılamaz ancak hala bir kullanıcı tarafından yapılabilir.

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Kullanımı sonlandırma/kaldırma nedeni** | Toplu iş kullanılarak oluşturulduğunda, ortaya çıkan açık provizyon dosyasını ısrar edip görüntülemek için form bulunmamaktadır. |
| **Başka bir özellik ile değiştirildi?**   | Açık provizyonlar hala oluşturulabilir ve kullanıcı dosyanın kaydedildiği yeri denetleyebilir.   |
| **Etkilenen ürün alanları**         | Borç hesapları, Alacak hesapları, Nakit ve banka yönetimi  |
| **Durum**                         | AX 7.0 itibarıyla kaldırıldı.    |

### <a name="german-dtaus-payment-export-and-account-statement-import-totals-and-transactions"></a>Almanca DTAUS ödeme dışa aktarma ve hesap ekstresi içeri alma (toplamları ve hareketler)

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Kullanımı sonlandırma/kaldırma nedeni** | Biçim, artık tek Euro ödemeleri alan (SEPA) işlevi tarafından değiştirildiğinden, Almanya'da artık geçerli değildir.                    |
| **Başka bir özellik ile değiştirildi?**   | Evet, bu özelliğin yerini SEPA ödeme dışa aktarma ve hesap ekstrelerini içeri aktarma için gelişmiş banka mutabakatı işlevi aldı. |
| **Etkilenen ürün alanları**         | Tüm modüller  |
| **Durum**                         | Kullanımı sonlandırıldı: Bu özellik için kaldırma tarihi belirlenmedi. |

### <a name="german-dtazv-payment-format-in-domestic-currency"></a>Yurtiçi para biriminde Alman DTAZV ödeme biçimi

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Kullanımı sonlandırma/kaldırma nedeni** | Biçim, artık tek Euro ödemeleri alan (SEPA) işlevi tarafından değiştirildiğinden, Almanya'da artık geçerli değildir. |
| **Başka bir özellikle mi değiştirildi?**   | SEPA ödemeleri dışa aktarımı    |
| **Etkilenen ürün alanları**         | Borç hesapları   |
| **Durum**                         | Kullanımı sonlandırıldı: Bu özellik için kaldırma tarihi belirlenmedi.    |

### <a name="german-mt940-import"></a>Almanca MT940 içe aktarımı

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Kullanımı sonlandırma/kaldırma nedeni** | Yerelleştirilmiş işlevsellik yerine artık genel işlevler kullanılır.                    |
| **Başka bir özellik ile değiştirildi?**   | Evet, bu işlevin yerini Gelişmiş banka mutabakatı işlevi aldı. |
| **Etkilenen ürün alanları**         | Tüm modüller                                                                              |
| **Durum**                         | Kullanımı sonlandırıldı: Bu özellik için kaldırma tarihi belirlenmedi.                           |

### <a name="german-xml-eu-sales-list"></a>Alman XML AB Satışlar listesi

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Kullanımı sonlandırma/kaldırma nedeni** | Almanca AB Satış Listesi raporlaması için XML biçimi artık desteklenmiyor. Alman Vergi Dairesi'ne AB Satış Listesi raporunu göndermek için yalnızca ELMA5 metin dosyası biçimi kullanılabilir. |
| **Başka bir özellik ile değiştirildi?**   | Hayır         |
| **Etkilenen ürün alanları**         | Vergi        |
| **Durum**                         | Kullanımı sonlandırıldı: Bu özellik için kaldırma tarihi belirlenmedi.   |

### <a name="gl-ssrs-reports"></a>GL SSRS raporları

Aşağıdaki menü öğelerini içeren raporlar kaldırıldı: **Özet mizan**, **ayrıntılı mizan**, **hesap planı**, **denetim izi**, **bakiyeler**, ve **bakiye listesi**.

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Kullanımı sonlandırma/kaldırma nedeni** | Mali Microsoft SQL Server Reporting Services (SSRS) raporlarının yeri, Management Reporter yetenekleri ve varsayılan raporlar tarafından alınmıştır. |
| **Başka bir özellik ile değiştirildi?**   | Management Reporter (Dynamics AX'ın geçerli sürümünde **finansal raporlama** etiketli)    |
| **Etkilenen ürün alanları**         | Genel muhasebe   |
| **Durum**                         | Dynamics AX 7.0 itibarıyla kaldırıldı.   |

### <a name="infopart-and-formpart-metadata"></a>InfoPart ve FormPart meta verileri

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Kullanımı sonlandırma/kaldırma nedeni** | InfoPart ve FormPart meta verileri, iki farklı istemci için bilgi kutularının oluşturulması sağlardı. |
| **Başka bir özellik ile değiştirildi?**   | Basitleştirilmiş form tanımı olan InfoPart meta verileri, forma yükseltme araç kullanımı tarafından dönüştürülür. Bir forma referans gösteren FormPart meta verileri, yükseltme araçları tarafından daha doğrudan bir referans ile değiştirildi. |
| **Etkilenen ürün alanları**         | Tüm modüller    |
| **Durum**                         | Dynamics AX 7.0 itibarıyla kaldırıldı.        |

### <a name="main-account-list-page"></a>Ana hesap liste sayfası

Tüzel kişilik ve ilgili bakiye bilgilerini hesapların listesi

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Kullanımı sonlandırma/kaldırma nedeni** | Bakiye bilgisi **Mizan** liste sayfasında hesap ve boyut olarak bulunabilir.  |
| **Başka bir özellik ile değiştirildi?**   | **Ana hesaplar**,**Ana hesap** sayfasında yer alan hesapların listesinin aynısını içerir. **Ana hesaplar**'daki ızgara görünümü daha da küçük ızgaraya benzer bir görünümü gösterir. |
| **Etkilenen ürün alanları**         | Genel muhasebe      |
| **Durum**                         | Dynamics AX 7.0 itibarıyla kaldırıldı.    |

### <a name="malaysia-and-singapore-bank-cash-flow-report"></a>Malezya ve Singapur banka nakit akışı raporu

Seçili banka hesapları için belirli bir tarih aralığındaki hareketlerin nakit giriş ve çıkış ayrıntılarını gösteren bir nakit akış raporu kullanıcı tarafından yazdırılabilir.

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Kullanımı sonlandırma/kaldırma nedeni** | Aynı bilgileri sorgulama banka hareketinden de elde edilebilir. |
| **Başka bir özellik ile değiştirildi?**   | Sorgulama banka hareketi                                            |
| **Etkilenen ürün alanları**         | Nakit ve banka yönetimi                                                |
| **Durum**                         | Kullanımı sonlandırıldı: Bu özellik için kaldırma tarihi belirlenmedi.          |

### <a name="mexican-cfd-electronic-invoice"></a>Meksika CFD elektronik fatura

Bu özellik, şirketin faturayı hükümetten ilgili izni isteyerek imzaladığı Comprobante Fiscal Digital (CFD) yöntemini kullanarak Meksika elektronik fatura oluşturmayı etkinleştirir. Bu özellik ayrıca bir dönemde çıkarılan tüm elektronik faturaları içeren aylık bir rapor sunar.

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Kullanımı sonlandırma/kaldırma nedeni** | Yöntemi artık geçerli değil. CFG yöntemini kullanarak elektronik faturaların oluşturulması vergi otoriteleri tarafından kaldırılıp yerine imzalamanın üçüncü taraf bir sağlayıcıya (PAC) devredildiği Comprobante Fiscal Digital a través de Internet (CFDI) metodu getirilmiştir. Aylık rapor kaldırıldı ve kullanıcıların geçmiş hareketler hakkında bilgi alması için sorgu seçeneği geliştirildi. |
| **Başka bir özellik ile değiştirildi?**   | Hayır    |
| **Etkilenen ürün alanları**         | Alacaklar hesabı, Proje   |
| **Durum**                         | Kullanımı sonlandırıldı: Bu özellik için kaldırma tarihi belirlenmedi. |

### <a name="mexico-realized-and-unrealized-vat"></a>Meksika gerçekleşmiş ve gerçekleşmemiş KDV

Dynamics AX 2012, gerçekleşmemiş katma değer vergisini (KDV) Meksika'ya özgü gerçekleşmemiş vergi işlevini kullanarak yönetiyordu.

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Kullanımı sonlandırma/kaldırma nedeni** | Tekrar eden işlevsellik  |
| **Başka bir özellik ile değiştirildi?**   | Evet, bu işlevin yerini Çekirdek tarafından sağlanan standart koşullu satış vergisi işlevleri aldı. |
| **Etkilenen ürün alanları**         | Vergi   |
| **Durum**                         | Kullanımı sonlandırıldı: Bu özellik için kaldırma tarihi belirlenmedi. |

### <a name="microsoft-outlook-integration"></a>Microsoft Outlook tümleştirmesi


| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Kullanımı sonlandırma/kaldırma nedeni** | Bu işlev Microsoft Exchange Server tümleştirmesi ile değiştirilmiştir. |
| **Başka bir özellikle mi değiştirildi?**   | Evet                                                                            |
| **Etkilenen ürün alanları**         | Sales and Marketing                                                            |
| **Durum**                         | Dynamics AX 7.0 itibarıyla kaldırıldı.                                                 |

### <a name="private-blocking-of-inventory-and-warehouse-management-journals"></a>Stok ve Ambar yönetim günlüklerinin özel durdurması

Stok ve Ambar günlükleri, günlüğün seçili kullanıcı için özel olarak işaretleme özelliğini artık desteklememektedir. Yalnızca kullanıcı grupları için özel olarak günlükleri engelleme ve düzenleme sırasında engelleme işlemi desteklenir.

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Kullanımı sonlandırma/kaldırma nedeni** | İşlev için kullanım bulunamadı. |
| **Başka bir özellik ile değiştirildi?**   | Hayır                                     |
| **Etkilenen ürün alanları**         | Stok Yönetimi                   |
| **Durum**                         | Dynamics AX 7.0 itibarıyla kaldırıldı.         |

### <a name="product-builder"></a>Ürün oluşturucu

Ürün Oluşturucu, bir satış siparişi, satınalma siparişi, üretim emri, satış teklifi, proje teklifi veya madde gereksinimi öğelerinden dinamik olarak ürün yapılandırmak için kullanılıyordu. Model oluşturma değişkenleri olan bir ürün modeline bağlı olarak, kullanıcı, müşteri gereksinimlerini karşılamak için bir ürün reçetesi ve rotası olan benzersiz bir ürün çeşidi sağlamak için değerler seçebiliyordu.

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Kullanımı sonlandırma/kaldırma nedeni** | Ürün Oluşturucu X ++ kodunu son kullanıcılara yansıtıyordu ve Dynamics AX'ın geçerli sürümünde desteklenmiyor. Büyük ve kesişen kod tabanlarında sürdürme çabalarının ikiye katlanmaması için kaldırıldı.  |
| **Başka bir özellik ile değiştirildi?**   | Evet. Kısıtlama tabanlı yapılandırma Dynamics AX 2012'de sunuldu ve Ürün oluşturucunun gelecekteki sürümlerde kullanımdan kaldırılacağı zaten açıklandı. Kısıtlama tabanlı yapılandırma teknolojisi yapılandırmayı etkinleştirmek ana ürünlerde seçilir. Daha fazla bilgi için bkz. [Ürün yapılandırmaya genel bakış](../../../supply-chain/pim/build-product-configuration-model.md). |
| **Etkilenen ürün alanları**         | Ürün bilgileri yönetimi, satış ve pazarlama  |
| **Durum**                         | Dynamics AX 7.0 itibarıyla kaldırıldı.      |

### <a name="production-floor-app"></a>Üretim Katı uygulaması
Bu uygulama, Windows 8.1 RT ve Windows 8.1 Pro çalıştıran tablet cihazlar için uygundur.

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Kullanımı sonlandırma/kaldırma nedeni** | Bir web tabanlı istemciye geçiş ile, yerel Dynamics AX 7.0 istemcisi aracılığıyla benzer işlevselliği sunmak mümkündür. İş Kartı Cihazı, dokunma ve tablet form faktörleri için bir üretim katı kullanıcı arabirimi sağlar. |
| **Başka bir özellikle mi değiştirildi?**   | Evet. İş Kartı Cihazı, Dynamics AX 7.0'ın yerel bir parçasıdır.                                                                           |
| **Etkilenen ürün alanları**         | Üretim denetimi                                                |
| **Durum**                         | Kaldırıldı: Bu özellik için Microsoft mağazasından bir kaldırma tarihi henüz belirlenmemiştir.                                                |


### <a name="rename-product-dimension"></a>Ürün boyutunu yeniden adlandır

Bu özellik, üç standart ürün boyutundan (boyut, renk veya stil) birinin adını işletme gereksinimlerinize daha iyi uygun bir adla değiştirmenize olanak sağlar. Yeniden adlandırma, ürün boyut adının kullanıldığı tüm etiketlere dahildir.

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Kullanımı sonlandırma/kaldırma nedeni** | Dynamics AX geçerli sürümününde, çalıştırma sırasında etiket değişikliklerini desteklemez. |
| **Başka bir özellikle mi değiştirildi?**   | Hayır                                                                            |
| **Etkilenen ürün alanları**         | Ürün bilgileri yönetimi                                                |
| **Durum**                         | Dynamics AX 7.0 itibarıyla kaldırıldı.                                                |

### <a name="retail-server-connectivity-using-http"></a>HTTP kullanarak Perakende Sunucu bağlantısı

Dynamics AX 2012 R3 içerisinde, Perakende Sunucu, HTTP iletişimi (güvenli olmayan) kullanarak işlev sağlayamıyordu. Bu, HTTPS kullanan standart iletişime ek olarak oluştu.

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Kullanımı sonlandırma/kaldırma nedeni** | Yeni güvenlik gereksinimleri nedeniyle, yalnızca TLS 1.2 (veya kullanılabilir olduğu takdirde üstü) artık desteklenmektedir. Self servis yükleyici, bilgisayarı bu iletişim için otomatik yapılandıracaktır. |
| **Başka bir özellik ile değiştirildi?**   | Hayır. Artık yalnızca standart HTTPS iletişimi desteklenmektedir. |
| **Etkilenen ürün alanları**         | Perakende Sunucusu  |
| **Durum**                         | Dynamics AX 7.0 itibarıyla kaldırıldı. |

### <a name="role-center-pages"></a>Rol Merkezi sayfaları

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Kullanımı sonlandırma/kaldırma nedeni** | Rol Merkezi sayfaları, kaldırılan Enterprise Portal platformu üzerine kurulmuştu ve Dynamics AX'ın geçerli sürümünde yeni web istemci platformu tarafından yenilendi. |
| **Başka bir özellikle mi değiştirildi?**   | Yeni çalışma alanı form düzeni kullanıcılara işlem merkezli tasarıma sahip, sık kullanılan işlemlere kolay erişim sağlayan bir işlem merkezli tasarımı sağlar.                       |
| **Etkilenen ürün alanları**         | Tüm modüller    |
| **Durum**                         | Dynamics AX 7.0 itibarıyla kaldırıldı   |

### <a name="sales-tax-jurisdictions"></a>Satış vergi daireleri

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Kullanımı sonlandırma/kaldırma nedeni** | Düşük müşteri kullanımı ve sınırlı özellik kümesi |
| **Başka bir özellik ile değiştirildi?**   | Hayır                                           |
| **Etkilenen ürün alanları**         | ABD satış vergisi                                 |
| **Durum**                         | Dynamics AX 7.0 itibarıyla kaldırıldı.               |

### <a name="sites-services"></a>Site Servisleri

Site Hizmetleri, BT desteği olmadan iş süreçlerinizi internete genişleten web siteleri kurmanıza olanak sağlar.

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Kullanımı sonlandırma/kaldırma nedeni** | Dynamics AX tarafından kullanılan Microsoft Azure altyapısı, alternatif olarak kullanılabilecek yeni özelliklere sahiptir (örneğin, Azure siteleri). |
| **Başka bir özellik ile değiştirildi?**   | Hayır   |
| **Etkilenen ürün alanları**         | İK işe alma, Servis talebi yönetimi, Teklif talebi, Satıcı kaydı, Fırsatlar ve kampanyalar için ortak çalışma alanları  |
| **Durum**                         | Dynamics AX 7.0 itibarıyla kaldırıldı.    |

### <a name="ssas-demand-forecasting-strategy"></a>SSASS talep tahmin stratejisi

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Kullanımı sonlandırma/kaldırma nedeni** | Özelliğin tasarımı yeni bulut mimarisinde desteklenemez. |
| **Başka bir özellik ile değiştirildi?**   | Azure Makine Öğrenimi talep tahmini stratejisi                           |
| **Etkilenen ürün alanları**         | Master planlama                                                              |
| **Durum**                         | Dynamics AX 7.0 itibarıyla kaldırıldı.                                               |

### <a name="vendor-invoice-pool-excluding-posting-details"></a>Deftere nakledilen ayrıntılar hariç satıcı faturası havuzu

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Kullanımı sonlandırma/kaldırma nedeni** | Düşük kullanım. Bu özelliğin yerini iş akışı işlevine sahip Fatura günlüğü almıştır. |
| **Başka bir özellik ile değiştirildi?**   | Fatura günlüğünün iş akışı özellikleri.     |
| **Etkilenen ürün alanları**         | Borç hesapları |
| **Durum**                         | Dynamics AX 7.0 itibarıyla kaldırıldı.    |


### <a name="virtual-company-accounts"></a>Sanal şirket hesapları

Sanal şirketler özelliği, Dynamics AX uygulamasında artık desteklenmiyor. Sanal şirketler özelliği, kullanıcılara bir dizi şirket tarafından paylaşılabilecek tablolar ayarlama olanağı sağlar. Özelliğin açıklaması için bkz. [Şirket hesapları ve Sanal şirket hesapları](https://msdn.microsoft.com/library/aa834382(v=ax.10).aspx). Bu özellik, tabloları, var olan "gerçek" şirketlerin grupları olan sanal şirketlere atanan koleksiyonlara gruplayarak çalışmaktadır. Sanal şirketteki tüm şirketlerin ilişkilendirilen tablo koleksiyonlarının tabloları içindeki verilere erişebileceği şekilde sorgular oluşturulur.

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Kullanımı sonlandırma/kaldırma nedeni** | - Tablolarda verilerin depolanmasından önce sanal şirketlerin ayarlanmış olması gerekir. Sanal şirketleri mevcut bir uygulamaya uyarlamak oldukça güçtür.<br><br>- Dynamics AX'in geçerli sürümünde çok fazla veri normalleştirmesi olduğundan, tablo koleksiyonlarına nelerin eklenmesi gerektiğini bilmek çok zor hale geldi. Örneğin, hangi tabloların paylaşılacağını bilmek zor. Bir sanal şirketteki tablolardan referans alınan tüm tabloların da ayrıca eklenmesi gerekir. Tablo normalleştirmesi nedeniyle, çok sayıda tabloya yayılan basit master verilerin bile sanal şirketin parçası haline gelmesi gerekiyor. Burada yapılan herhangi bir hata, işlevsel sorunlara neden olur.<br><br>- Bir tablo bir sanal şirketin parçası olduğunda, veri kaynağı hakkındaki bilgiyi kaybeder ve sadece sanal şirket kaydedilir.   |
| **Başka bir özellik ile değiştirildi?** | Tabloları tüm şirketlerden erişebilir hale getirmek için global tablolar kullanılabilir. Şu anda bir değişiklik yoktur. |   
| **Etkilenen ürün alanları**       | Tüm modüller |   
| **Durum**                       | Dynamics AX 7.0 itibarıyla kaldırıldı.   |   

### <a name="windows-8-tablet-app"></a>Windows 8 tablet uygulaması

Windows 8 tablet uygulaması, gider girişi ve onayı için işlevler sağlardı.

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Kullanımı sonlandırma/kaldırma nedeni** | Finance and Operations tabletler ile uyumludur. Tablet uygulaması artık gerekli değildir.    |
| **Başka bir özellik ile değiştirildi?**   | Hayır.          |
| **Etkilenen ürün alanları**         | Gider yönetimi   |
| **Durum**                         | Kaldırıldı: Bu işlev yalnızca Dynamics AX 2012 R3 için kullanılabilir. |

### <a name="workplanner"></a>İş planlayıcısı

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Kullanımı sonlandırma/kaldırma nedeni** | Düşük kullanım |
| **Başka bir özellik ile değiştirildi?**   | Hayır, ama **Profil grupları** sayfasından açılan **Profil ilişkisi** sayfası, kaldırılan **İş planlayıcısı** sayfası ile aynı iş senaryosunu destekler. |
| **Etkilenen ürün alanları**         | Saat ve işe devam     |
| **Durum**                         | Kod kaldırılmadı. Bununla birlikte, JmgWorkPlanner formunun geçişi yapılmadı.    |

### <a name="x-financial-statements"></a>X++ mali tablolar

| &nbsp;  | &nbsp; |
|-------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| <strong>Kullanımı sonlandırma/kaldırma nedeni</strong> |                         Bu işlev başka bir özellik ile değiştirilmiştir.                         |
|  <strong>Başka bir özellik ile değiştirildi?</strong>  | Management Reporter (Dynamics AX'ın geçerli sürümünde <strong>finansal raporlama</strong> etiketli) |
|     <strong>Etkilenen ürün alanları</strong>     |                                              Genel muhasebe                                              |
|             <strong>Durum</strong>             |                                      Dynamics AX 2012 itibarıyla kaldırıldı                                      |



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
