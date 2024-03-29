---
title: Kaldırılan veya kullanım dışı bırakılan platform özellikleri
description: Bu makale, finans ve operasyon uygulamalarının platform güncellemelerinde kaldırılmış veya kaldırılması planlanan özellikleri açıklar.
author: sericks007
ms.date: 08/09/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2020-02-29
ms.dyn365.ops.version: Platform update 33
ms.openlocfilehash: 6283e07b87dc169d3cbaa71a371839ab9b2d6150
ms.sourcegitcommit: ee13b854cbd52a3aa33e2449a296aed775862594
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/21/2022
ms.locfileid: "9799049"
---
# <a name="removed-or-deprecated-platform-features"></a>Kaldırılan veya kullanım dışı bırakılan platform özellikleri

[!include [banner](../includes/banner.md)]

Bu makale, finans ve operasyon uygulamalarının platform güncellemelerinde kaldırılmış veya kaldırılması planlanan özellikleri açıklar.

- *Kaldırılan* özellik artık üründe bulunmaz.
- *Kullanımına son verilen* özellik etkin geliştirmede değildir ve sonraki güncellemede kaldırılabilir.

Bu liste, kaldırılan veya kullanımına son verilen özellikleri kendi planlamanız için göz önünde bulundurmanız amacıyla hazırlanmıştır. 

Finans ve operasyon uygulamalarındaki nesneler hakkında ayrıntılı bilgiye [Teknik referans raporları](/dynamics/s-e/global/axtechrefrep_61) altından ulaşabilirsiniz. Finans ve operasyon uygulamalarının her sürümünde değiştirilen veya kaldırılan nesneler hakkında bilgi edinmek için bu raporların farklı sürümlerini karşılaştırabilirsiniz.

## <a name="feature-deprecation-effective-august-2022"></a>Ağustos 2022'den itibaren geçerli olmak üzere özellik kullanımdan kaldırma bildirimi

### <a name="lifecycle-services-lcs-features-deprecated-in-august-2022"></a>Lifecycle Services (LCS) özellikleri Ağustos 2022'de kullanım dışı bırakıldı

[Tek bir Dynamics One platformu](/dynamics365-release-plan/2022wave2/finance-operations/finance-operations-crossapp-capabilities/one-dynamics-one-platform) çalışma çabası kapsamında, aşağıdaki LCS özellikleri kullanım dışı bırakılmıştır.

| Özellik adı | AX 2012 ile kullanıldı mı? | Finans ve operasyon uygulamaları ile kullanıldı mı? | Başka bir özellik ile değiştirildi? |
|--------------|--------------------|----------------------------------------|------------------------------|
| Duyurular | Evet | Evet | Evet: Başlık sayfaları bildirimlere yönelik ayrı proje ve ortam sayfalarında mevcuttur. |
| Yapılandırma yöneticisi | Evet | No. | No. |
| Kilitlenme bilgi dökümü analizi | Evet | No. | No. |
| Geri bildirim ve hatalar | Evet | Evet | No. |
| Aboneliklerim | Evet | Evet | No. |
| Office 365 | Evet | Evet | Evet: Azure Active Directory veya Microsoft yönetici portalı. |
| Etki analizi | No. | Evet | No. |
| Toplam ekonomik etki tahmin aracı | No. | Evet | No. |
| Servis talepleri | No. | Evet | Evet: [Self servis dağıtımlar](../deployment/infrastructure-stack.md) |
| SharePoint tümleştirmesi | Evet | Evet | No. |
| Yapılandırma ve veri yöneticisi | No. | Evet | No. |
| İşlem verileri paketleri | No. | Evet | Evet: [Veri İçe/Dışa Aktarma Çerçevesi (DIXF)](/dynamics365/fin-ops-core/dev-itpro/data-entities/data-import-export-job) |
| Ortamı yükseltme | No. | Evet | Evet: [One Version](../lifecycle-services/oneversion-overview.md) hizmet güncelleştirmeleri mevcuttur. |
| Altyapı tahmin aracı | Evet | No. | No. |
| Lisans boyutlandırma | Evet | No. | No. |
| Kullanım profili oluşturma aracı | Evet | No. | No. |
| Özelleştirme analizi | Evet | No. | No. |
| Sistem tanılama | Evet | Evet | No. |
| İş süreci modelleyici Visio yönetimi | Evet | Evet | No. |
| AX 2012 bulut ortamı yönetimi | Evet | No. | No. |
| RDFE Azure bağlayıcıları | Evet | Evet | No. |
| AX 2012 sürümleri | Evet | No. | No. |
| LCS depolama alanında depolanan iş öğeleri | Evet | Evet | No. |
| Düzeltme istekleri | Evet | Evet | No. |


### <a name="transport-layer-security-tls-rsa-cipher-suites"></a>Aktarım Katmanı Güvenliği (TLS) RSA şifre paketleri

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Kullanımı sonlandırma/kaldırma nedeni** | Geçerli güvenlik protokollerimize uymak için aşağıdaki şifre paketleri listesini kaldırıyoruz.<br><br>TLS_RSA_WITH_AES_256_GCM_SHA384<br>TLS_RSA_WITH_AES_128_GCM_SHA256<br>TLS_RSA_WITH_AES_256_CBC_SHA256<br>TLS_RSA_WITH_AES_128_CBC_SHA256<br>TLS_RSA_WITH_AES_256_CBC_SHA<br>TLS_RSA_WITH_AES_256_CBC_SHA  |
| **Başka bir özellikle mi değiştirildi?**   | Ocak 2023 tarihinden başlayarak, müşteriler yalnızca [standart şifre paketlerimizi](/power-platform/admin/server-cipher-tls-requirements) kullanabilecektir. Bu değişiklik, sunucularımızla iletişim kuran istemcilerinizi ve sunucularınızı etkiler. Örneğin, standart şifre paketlerimize uymayan üçüncü taraf tümleştirmelerinizi etkileyebilir. |
| **Etkilenen ürün alanları**         | Finans ve Operasyon uygulamaları |
| **Dağıtım seçeneği**              | Bulut dağıtımları |
| **Çalıştırma Durumu**                         | Kaldırıldı. Müşteriler Ocak 2023 tarihinden önce sunucularını yükseltmelidir. TLS Şifre Paketi sırasını yapılandırma hakkında daha fazla bilgi için bkz. [Aktarım Katmanı Güvenliğini (TLS) yönetme](/windows-server/security/tls/manage-tls).  |


## <a name="feature-deprecation-effective-june-2022"></a>Haziran 2022'den itibaren geçerli olmak üzere özellik kullanımdan kaldırma bildirimi

### <a name="finance-and-operations-dynamics-365-mobile-application-and-mobile-platform"></a>Finans ve operasyon (Dynamics 365) mobil uygulaması ve mobil platformu 

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Kullanımı sonlandırma/kaldırma nedeni** | Tek bir mobil platformda (Power Apps) birleştirme için finans ve operasyon (Dynamics 365) mobil uygulaması ve platformunu kullanım dışı bırakıyoruz. |
| **Başka bir özellikle mi değiştirildi?**   | Evet, finans ve operasyon uygulaması verilerini temel alan mobil deneyimler Power Platform tümleştirmesiyle oluşturulabilir. Daha ayrıntılı bilgi için [blog gönderisini](https://cloudblogs.microsoft.com/dynamics365/it/2022/06/03/finance-and-operations-dynamics-365-mobile-app-to-be-deprecated/) ve [Mobil deneyimler oluşturma](../power-platform/build-mobile-experiences.md) başlıklı makaleye bakın. |
| **Etkilenen ürün alanları**         | Finans ve Operasyon uygulamaları |
| **Dağıtım seçeneği**              | Tümü |
| **Çalıştırma Durumu**                         | Kaldırıldı. Destek tarihi sonu, Ekim 2024 olarak hedeflenmektedir. |


## <a name="platform-updates-for-version-10029-of-finance-and-operations-apps"></a>Finans ve operasyon uygulamalarının 10.0.29 sürümü için platform güncelleştirmeleri

### <a name="panorama-tab-style"></a>Panorama sekme stili

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Kullanımı sonlandırma/kaldırma nedeni** | Yatay olarak kayan sayfalar, bilinen kullanılabilirlik ve erişilebilirlik sorunları olan güncelliğini yitirmiş düzen desenlerine uyum sağlar.  |
| **Başka bir özellikle mi değiştirildi?**   | Hayır ancak diğer sekme stilleri hala kullanılabilir durumdadır. |
| **Etkilenen ürün alanları**         | Web istemcisi |
| **Dağıtım seçeneği**              | Tümü |
| **Çalıştırma Durumu**                         | Kaldırıldı. |


## <a name="feature-deprecation-effective-april-2022"></a>Nisan 2022'den itibaren geçerli olmak üzere özellik kullanımdan kaldırma bildirimi

### <a name="xml-url-resolution-in-data-management"></a>Veri yönetiminde XML URL'si çözümlemesi 

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Kullanımı sonlandırma/kaldırma nedeni** | Olası bir güvenlik açığı olarak tanımlandığından XML URL çözümlemesi desteğini kaldırıyoruz. Bu, XML dosyalarıyla ilişkili dış kaynakların artık giderilemeyeceği anlamına gelir.  |
| **Başka bir özellikle mi değiştirildi?**   | Hayır. |
| **Etkilenen ürün alanları**         | Finans ve Operasyon uygulamaları |
| **Dağıtım seçeneği**              | Tümü |
| **Çalıştırma Durumu**                         | Kaldırıldı. |

## <a name="feature-deprecation-effective-march-14-2022"></a>14 Mart 2022'den itibaren geçerli olmak üzere özellik kullanımdan kaldırma bildirimi

### <a name="xslt-scripting-in-data-management"></a>Veri yönetiminde XSLT komut dosyası

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Kullanımı sonlandırma/kaldırma nedeni** | Finans ve operasyon uygulamalarındaki güvenlik ve veri korumasının geliştirilmesi için veri yönetimindeki XSLT komut dosyası desteği kullanım dışıdır.  |
| **Başka bir özellikle mi değiştirildi?**   | Hayır. Müşteriler ve ISV'ler, XSLT kodu yerine X++ diline dayalı olarak çözümlerinin yeniden uygulanması gerektiğini düşünmelidir. |
| **Etkilenen ürün alanları**         | Finans ve Operasyon uygulamaları |
| **Dağıtım seçeneği**              | Tümü |
| **Çalıştırma Durumu**                         | Kaldırıldı <br><br>**Özel durum:** XLST komut dosyası kullanmakta olan müşteriler. Sürüm 10.0.30 veya daha yenisine güncelleştirene kadar kullanmaya devam edebilir. Önceki sürümlerde, özel durum 31 Ocak 2023 tarihinden sonra sona erer. Bu özel duruma sahip müşteriler Microsoft 365 Yönetim Merkezinde bulunan İleti merkezinde bir bildirim almıştır. |

## <a name="feature-removal-effective-october-2021"></a>Özellik kaldırma geçerlilik tarihi: 2021 Ekim

### <a name="microsoft-azure-sql-reports-in-lifecycle-services-lcs"></a>Lifecycle Services'de (LCS) Microsoft Azure SQL raporları

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Kullanımı sonlandırma/kaldırma nedeni** | Tüm etkinlikler ve izleme; dahili olarak, platform tarafından ve otomasyon üzerinden gerçekleştirilir. Bu işlem için el ile müdahale gerekmez.|
| **Başka bir özellikle mi değiştirildi?**   | Evet, artık bu yetenekleri geçersiz kılan otomatik bir sistem var. |
| **Etkilenen ürün alanları**         | SQL raporları: Geçerli DTU, Geçerli DTU Ayrıntıları, Kilit Ayrıntılarını Al, Geçerli Plan Kılavuzunun Listesi, Sorgu Kimliklerinin Listesini Al, Belirli bir Plan Kimliği için SQL sorgu planını al, Sorgu planlarını ve yürütme durumunu al, Azaltma yapılandırmasını al, Bekleme istatistiklerini al, En pahalı sorguları listele |
| **Dağıtım seçeneği**              | Bulut dağıtımı: Microsoft tarafından yönetilen üretim ortamlarını ve Katman 2 ile Katman 5 arasındaki korumalı alan ortamlarını etkiler. |
| **Durum**                         | Kaldırıldı |

### <a name="azure-sql-actions-in-lcs"></a>LCS'de Azure SQL eylemleri

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Kullanımı sonlandırma/kaldırma nedeni** | LCS'de bazı SQL eylemlerini kullanımdan kaldırıyoruz. Tüm etkinlikler ve izleme; dahili olarak, platform tarafından ve otomasyon üzerinden gerçekleştirilir. Bu işlem için el ile müdahale gerekmez. |
| **Başka bir özellikle mi değiştirildi?**   | Evet, artık bu yetenekleri geçersiz kılan otomatik bir sistem var. |
| **Etkilenen ürün alanları**         | SQL eylemleri: Plan Kodu zorlamak için bir plan kılavuzu oluştur, Tablo ipuçları eklemek için bir plan kılavuzu oluştur, Plan Kılavuzunu kaldır, Sayfa kilitlerini ve kilit ilerletmeyi Devre Dışı Bırak/Etkinleştir, Tablodaki istatistikleri güncelleştir, Dizini yeniden oluştur, Dizin oluştur |
| **Dağıtım seçeneği**              | Bulut dağıtımı: Microsoft tarafından yönetilen üretim ortamlarını ve Katman 2 ile Katman 5 arasındaki korumalı alan ortamlarını etkiler. |
| **Durum**                         | Kaldırıldı |


## <a name="feature-deprecation-effective-october-2021"></a>Ekim 2021'den itibaren geçerli olmak üzere özellik kullanımdan kaldırma bildirimi

### <a name="show-related-document-attachments-feature"></a>"İlgili belge eklerini göster" özelliği

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Kullanımı sonlandırma/kaldırma nedeni** | Özellik, beklenmeyen sonuçlar döndürdü. |
| **Başka bir özellikle mi değiştirildi?**   | Hayır. Bu işlevlerle ilgili daha fazla plan, standart serbest bırakma bilgi işlem sürecimiz aracılığıyla size gönderilecek. |
| **Etkilenen ürün alanları**         | Web istemcisi - Belge eki deneyimi |
| **Dağıtım seçeneği**              | Tümü |
| **Çalıştırma Durumu**                         | Kaldırıldı  |

## <a name="platform-updates-for-version-10023-of-finance-and-operations-apps"></a>Finans ve operasyon uygulamalarının 10.0.23 sürümü için platform güncelleştirmeleri

### <a name="ondbsynchronize-event"></a>OnDBSynchronize olayı

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Kullanımı sonlandırma/kaldırma nedeni** | Bu olayı yürütecek bir denetim yok. |
| **Başka bir özellikle mi değiştirildi?**   | Evet, **OnDBSynchronize** olayıyla abone olunan mevcut yöntemleri SysSetup genişletilmiş sınıfına taşıyın. |
| **Etkilenen ürün alanları**         | Veritabanı eşitleme |
| **Dağıtım seçeneği**              | Tümü |
| **Durum**                         | Kaldırıldı. Planlanan kaldırma tarihi: Ekim 2022. |


### <a name="systemnotificationsmanageraddnotification-api"></a>SystemNotificationsManager.AddNotification API

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Kullanımı sonlandırma/kaldırma nedeni** | Microsoft, bildirim eklerken ek parametreler gerektirir. |
| **Başka bir özellikle mi değiştirildi?**   | Evet, **SystemNotificationsManager.AddSystemNotification()** API. Bu API, üretilen bildirimler için ExpirationDateTime ve RuleID'yi açık olarak ayarlamış olmanızı gerektiriyor. |
| **Etkilenen ürün alanları**         | Web istemcisi |
| **Dağıtım seçeneği**              | Tümü |
| **Durum**                         | Kaldırıldı. Planlanan kaldırma tarihi: Nisan 2023. |

## <a name="platform-updates-for-version-10021-of-finance-and-operations-apps"></a>Finans ve operasyon uygulamalarının 10.0.21 sürümü için platform güncelleştirmeleri

### <a name="skype-for-business-online-support"></a>Skype for Business Çevrimiçi desteği

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Kullanımı sonlandırma/kaldırma nedeni** | Skype for Business Çevrimiçi kullanım dışı bırakılmıştır. Daha fazla bilgi için bkz. [Skype for Business Çevrimiçi hizmeti kullanım dışı bırakıldı](https://techcommunity.microsoft.com/t5/microsoft-teams-blog/the-skype-for-business-online-service-has-retired/ba-p/2596601). |
| **Başka bir özellikle mi değiştirildi?**   | Şu anda değil ancak gelecekte Teams uygulamasından varlık eklemeyi düşünebiliriz.|
| **Etkilenen ürün alanları**         | Web istemcisi |
| **Dağıtım seçeneği**              | Tümü |
| **Durum**                         | Kaldırıldı. **Skype etkinleştirildi** ayarı, 10.0.21 sürümünden itibaren kapatılmıştır. Nisan 2022'de bu ayarın kaldırılması hedefleniyor ancak, Skype ekibi hizmeti kapattıktan sonra özellik çalışmayı durduracaktır. |
 
## <a name="feature-deprecation-effective-august-2021"></a>Ağustos 2021'den itibaren geçerli olmak üzere özellik kullanımdan kaldırma bildirimi

### <a name="microsoft-azure-sql-reports-in-lifecycle-services-lcs"></a>Lifecycle Services'de (LCS) Microsoft Azure SQL raporları

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Kullanımı sonlandırma/kaldırma nedeni** | Tüm etkinlikler ve izleme; dahili olarak, platform tarafından ve otomasyon üzerinden gerçekleştirilir. Bu işlem için el ile müdahale gerekmez.|
| **Başka bir özellikle mi değiştirildi?**   | Evet, artık bu yetenekleri geçersiz kılan otomatik bir sistem var. |
| **Etkilenen ürün alanları**         | SQL raporları: Geçerli DTU, Geçerli DTU Ayrıntıları, Kilit Ayrıntılarını Al, Geçerli Plan Kılavuzunun Listesi, Sorgu Kimliklerinin Listesini Al, Belirli bir Plan Kimliği için SQL sorgu planını al, Sorgu planlarını ve yürütme durumunu al, Azaltma yapılandırmasını al, Bekleme istatistiklerini al, En pahalı sorguları listele |
| **Dağıtım seçeneği**              | Bulut dağıtımı: Microsoft tarafından yönetilen üretim ortamlarını ve Katman 2 ile Katman 5 arasındaki korumalı alan ortamlarını etkiler. |
| **Durum**                         | Kullanım dışı: Ekim 2021'de planlanan kaldırma tarihi. |

### <a name="azure-sql-actions-in-lcs"></a>LCS'de Azure SQL eylemleri

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Kullanımı sonlandırma/kaldırma nedeni** | LCS'de bazı SQL eylemlerini kullanımdan kaldırıyoruz. Tüm etkinlikler ve izleme; dahili olarak, platform tarafından ve otomasyon üzerinden gerçekleştirilir. Bu işlem için el ile müdahale gerekmez. |
| **Başka bir özellikle mi değiştirildi?**   | Evet, artık bu yetenekleri geçersiz kılan otomatik bir sistem var. |
| **Etkilenen ürün alanları**         | SQL eylemleri: Plan Kodu zorlamak için bir plan kılavuzu oluştur, Tablo ipuçları eklemek için bir plan kılavuzu oluştur, Plan Kılavuzunu kaldır, Sayfa kilitlerini ve kilit ilerletmeyi Devre Dışı Bırak/Etkinleştir, Tablodaki istatistikleri güncelleştir, Dizini yeniden oluştur, Dizin oluştur |
| **Dağıtım seçeneği**              | Bulut dağıtımı: Microsoft tarafından yönetilen üretim ortamlarını ve Katman 2 ile Katman 5 arasındaki korumalı alan ortamlarını etkiler. |
| **Durum**                         | Kullanım dışı: Ekim 2021'de planlanan kaldırma tarihi. |

## <a name="feature-deprecation-effective-may-2021"></a>Mayıs 2021'den itibaren geçerli olmak üzere özellik kullanımdan kaldırma bildirimi

### <a name="globalization-portal-in-lifecycle-services-lcs"></a>Lifecycle Services (LCS) içinde genelleştirme portalı

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Kullanımı sonlandırma/kaldırma nedeni** | Bu özellik diğer LCS tabanlı hizmetler tarafından yerine geçirildikçe LCS'deki Genelleştirme portalını kullanımdan kaldırdık. |
| **Başka bir özellikle mi değiştirildi?**   | Evet, bu özelliğin yerini LCS [Sorunu arama](../lifecycle-services/issue-search-lcs.md) ve [Dynamics düzenleyici uyarı gönderme hizmeti](../lcs-solutions/submit-localization-alerts.md). |
| **Etkilenen ürün alanları**         | LCS'de genelleştirme portalı|
| **Dağıtım seçeneği**              | Bulut dağıtımı |
| **Durum**                         | Kullanım dışı: Mayıs 2022'de planlanan kaldırma tarihi. |


## <a name="feature-removed-effective-january-28-2021"></a>Özellik 28 Ocak 2021'de kaldırıldı

### <a name="batch-job-to-handle-sql-index-defragmentation"></a>SQL dizin birleştirmeyi işlemek için toplu iş

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Kullanımı sonlandırma/kaldırma nedeni** | Müşterilerin dizin yönetimini işletmek, izlemek ve sürdürmekle ilgili ek yükünü azaltmak için bu özellik kaldırıldı. |
| **Başka bir özellikle mi değiştirildi?**   | İleride, dizin bakımı Microsoft hizmetleri tarafından gerçekleştirilecektir. Bu, kullanıcı iş yüklerini etkilemeden sürekli olarak gerçekleşecektir. |
| **Etkilenen ürün alanları**         | Finans ve Operasyon uygulamaları|
| **Dağıtım seçeneği**              | Bulut dağıtımı: Microsoft tarafından yönetilen üretim ortamlarını ve Katman 2 ile Katman 5 arasındaki korumalı alan ortamlarını etkiler. |
| **Durum**                         | Bu özellik kaldırılmıştır. |


## <a name="platform-updates-for-version-10017-of-finance-and-operations-apps"></a>Finans ve operasyon uygulamalarının 10.0.17 sürümü için platform güncelleştirmeleri


### <a name="visual-studio-2015"></a>Visual Studio2015

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Kullanımı sonlandırma/kaldırma nedeni** | Visual Studio'Nin en son sürümlerini desteklemek için Visual Studio için X++ uzantılarında bazı değişiklikler yapılmalıdır . Bu değişiklikler Visual Studio 2015 ile uyumsuz . |
| **Başka bir özellikle mi değiştirildi?**   | Visual Studio 2017, Dağıtılmış ve gerekli sürüm olarak Visual Studio 2015 yerine çalışacak. |
| **Etkilenen ürün alanları**         | Visual Studio geliştirme araçları |
| **Dağıtım seçeneği**              | Tümü |
| **Durum**                         | Kullanım dışı: Güncelleştirme sonrasında, önceki X++ Visual Studio 2015'ten kaldırılacaktır ve güncelleştirilen araçlar Visual Studio 2015'e yüklenmeyecektir. Barındırılan yapılar üzerinde hiçbir etkisi yoktur. Derleme sanal makineleri için derleme işlem hattı (derleme tanımı), bağımlılığı MSBuild 14.0 (Visual Studio 2015) sürümünden MSBuild 15.0 (Visual Studio 2017) sürümüne değiştirmek için [Azure Pipelines'ta eski bir işlem hattını güncelleştirme](../dev-tools/pipeline-msbuild-update.md) konusunda açıklanan şekilde el ile güncelleştirilmelidir. |

### <a name="user-avatar"></a>Kullanıcı avatarı 

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Kullanımı sonlandırma/kaldırma nedeni** | Gezinti çubuğunun sağ tarafında görüntülenen kullanıcı avatarı, kullanım dışı bırakılan bir Dynamics 365 üst bilgi denetiminden bir API kullanılarak alındı. |
| **Başka bir özellikle mi değiştirildi?**   | Bunun yerine, kullanıcılar kendi baş harflerini gezinme çubuğunda bir daire içinde görür. Bu, geliştirme makinelerinde şu anda kullanılmakta olan görseldir. |
| **Etkilenen ürün alanları**         | Web istemcisi |
| **Dağıtım seçeneği**              | Tümü |
| **Durum**                         | Sürüm 10.0.17 itibarıyla kaldırıldı |

### <a name="enterprise-portal-ep-deprecation"></a>Enterprise Portal (EP) kullanımdan kaldırma  

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Kullanımı sonlandırma/kaldırma nedeni** | EP, finans ve operasyon uygulamalarında hiçbir zaman desteklenmediğinden, Dynamics AX 2012 Enterprise Portal (EP) ile ilişkili meta veri yapıtları, kullanımdan kaldırıldı. |
| **Başka bir özellikle mi değiştirildi?**   | No. |
| **Etkilenen ürün alanları**         | Web istemcisi |
| **Dağıtım seçeneği**              | Tümü |
| **Durum**                         | Kullanım dışı: EP kodunun tamamının, Ekim 2021 sürümünde kaldırılması planlanıyor. |

## <a name="deprecation-effective-december-2020"></a>Kullanımdan kaldırma Kasım 2020'den itibaren geçerli olacaktır

### <a name="internet-explorer-11-support-for-dynamics-365-is-deprecated"></a>Dynamics 365 için Internet Explorer 11 desteği kullanım dışı bırakılmıştır

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Kullanımı sonlandırma/kaldırma nedeni** | Aralık 2020 itibarıyla geçerli olmak üzere tüm Dynamics 365 ve Dynamics Lifecycle Services (LCS) ürünleri için Microsoft Internet Explorer 11 desteği kullanım dışı, bırakılacaktır ve Internet Explorer 11, Ağustos 2021'den sonra desteklenmeyecektir.<br><br>Bu, Internet Explorer 11 arabirimi aracılığıyla kullanılmak üzere tasarlanmış olan Dynamics 365 ve LCS ürünlerini kullanan müşterileri etkileyecektir. Ağustos 2021'den sonra, Internet Explorer 11, bu tür Dynamics 365 ürünleri ve LCS için desteklenmeyecektir. |
| **Başka bir özellikle mi değiştirildi?**   | Müşterilerin Microsoft Edge'e geçiş yapması önerilir.|
| **Etkilenen ürün alanları**         | Tüm Dynamics 365 ürünleri ve LCS |
| **Dağıtım seçeneği**              | Tümü|
| **Çalıştırma Durumu**                         | Kullanım dışı: Internet Explorer 11 Ağustos 2021'den sonra desteklenmeyecektir.|

## <a name="platform-updates-for-version-10015-of-finance-and-operations-apps"></a>Finans ve operasyon uygulamalarının 10.0.15 sürümü için platform güncelleştirmeleri

### <a name="visual-studio-add-in-to-apply-metadata-hotfixes"></a>Meta veri düzeltmelerini uygulamak için Visual Studio eklentisi

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Kullanımı sonlandırma/kaldırma nedeni** | Meti veri düzeltmeleri artık Temmuz 2018'de 8.1 sürümüyle sunulan [One Version](../../fin-ops/get-started/one-version.md) hizmet güncelleştirmeleriyle desteklenmemektedir. |
| **Başka bir özellikle mi değiştirildi?**   | Desteklenen sürümler için bağımsız meta veri düzeltmeleri yoktur. Bunun yerine toplu kalite güncelleştirmeleri uygulanır. |
| **Etkilenen ürün alanları**         | Visual Studio eklentileri |
| **Dağıtım seçeneği**              | Geliştirme sanal makineleri |
| **Durum**                         | Sürüm 10.0.15 ile eklenti artık Visual Studio araçlarına dahil değildir. |


## <a name="platform-updates-for-version-10014-of-finance-and-operations-apps"></a>Finans ve operasyon uygulamalarının 10.0.14 sürümü için platform güncelleştirmeleri

### <a name="online-users-page"></a>Çevrimiçi kullanıcılar sayfası 

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Kullanımı sonlandırma/kaldırma nedeni** | Bu, önceki istemci/sunucu mimarisi için oluşturulmuş eski bir sayfadır. Bu sayfadaki bilgiler her zaman doğru değildir ve karıştırıcı ve yanıltıcı olabilir. |
| **Başka bir özellikle mi değiştirildi?**   | Gelecekteki bir güncelleştirmede yeni bir sayfa sağlayacağız.|
| **Etkilenen ürün alanları**         | Sistem Yönetimi |
| **Dağıtım seçeneği**              | Tümü |
| **Durum**                         | 2021 Ekim'de bu form kaldırılacaktır.   |


## <a name="platform-updates-for-version-10013-of-finance-and-operations-apps"></a>Finans ve operasyon uygulamalarının 10.0.13 sürümü için platform güncelleştirmeleri


### <a name="custom-code-defined-in-ssrs-report-properties"></a>SSRS rapor özelliklerinde tanımlanan özel kod 

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Kullanımı sonlandırma/kaldırma nedeni** | Genel olarak, özel kod sınırlı avantaj sunarken destek için önemli miktarda kaynak kullanımı ve işlem gerektirir. Özel kod, öncelikle özel bir kod derlemesinden genel yöntemleri çağırmak için rapor yazarları tarafından kullanılır. Ancak, bulutta barındırılan hizmet SSRS raporları için özel derlemelere yönelik başvuruları desteklemez. |
| **Başka bir özellikle mi değiştirildi?**   | Rapor yazarları, herhangi bir metin kutusu ifadesinden Matematik, Dönüştürme ve Biçim işlemleri için genel .NET API'larına başvuruda bulunmaya devam etmeyi seçebilirler. Daha fazla bilgi için bkz. [Rapora Kod Ekleme (SSRS)](/sql/reporting-services/report-design/add-code-to-a-report-ssrs).  |
| **Etkilenen ürün alanları**         | Özel kod içeren RDL'de tanımlanan uygulama raporu tasarımlarının alt kümesi. |
| **Dağıtım seçeneği**              | Tümü |
| **Durum**                         | Sürüm 10.0.13 ile, derleyici bir SSRS rapor tanımında özel kodun algılandığı durumlar için uyarı vermeyi başlayacaktır. Sorunu gidermek için rapor tasarımı tanımını açın ve tüm özel kod yapılarını kaldırın. Bu uyarı gelecekteki bir güncelleştirmede bulunan bir derleyici hatasıyla değiştirilecektir.   |

### <a name="upgrade-of-three-jquery-component-libraries"></a>Üç jQuery bileşen kitaplığını yükseltme 

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Kullanımı sonlandırma/kaldırma nedeni** | Üç jQuery bileşen kitaplığı güvenlik düzeltmeleri ve para birimini koruma açısından güncelleştirilmektedir.   
| **Başka bir özellikle mi değiştirildi?**   | Aşağıdaki kitaplıklar etkilenmiştir: jQuery (3.5.0 sürümünden 2.1.4 sürümüne kadar), jQuery UI (1.12.1 sürümünden 1.11.4 sürümüne kadar), jQuery Qtıp (2.2.1 sürümünden 3.0.3 sürümüne kadar). Geçiş kılavuzu, jQuery tarafından çevrimiçi olarak sağlanmıştır.  |
| **Etkilenen ürün alanları**         | Genişletilebilir denetimler, özellikle özel JavaScript kod kullanımı kullanım dışı bırakıldı veya API'lar kaldırıldı |
| **Dağıtım seçeneği**              | Tümü |
| **Durum**                         | Sürüm 10.0.13/Platform güncelleştirmesi 37 ile, müşteriler isteğe bağlı olarak "üç jQuery bileşen kitaplığını yükselt" özelliğini etkinleştirerek en son kitaplıklara geçiş yapabilir. Etkilenen API'ların taşınması için zaman vermek amacıyla, yeni kitaplıklara geçiş Nisan 2021 sürümü ile zorunlu olacaktır.   |

### <a name="existing-grid-controlforcelegacygrid-api"></a>Varolan kılavuz denetimi/forceLegacyGrid() API

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Kullanımı sonlandırma/kaldırma nedeni** | Varolan kılavuz denetimi yeni kılavuz denetimiyle değiştiriliyor. |
| **Başka bir özellikle mi değiştirildi?**   | [Yeni kılavuz denetimi](../..//fin-ops/get-started/grid-capabilities.md) |
| **Etkilenen ürün alanları**         | Web istemcisi |
| **Dağıtım seçeneği**              | Tümü |
| **Durum**                         | Sürüm 10.0.13'te, yeni kılavuz denetimi genellikle kullanılabilirdir ve müşteriler isteğe bağlı olarak bu özelliği açabilir. Yeni kılavuz denetimi, Ekim 2021 sürümüyle varsayılan olarak kullanılabilecektir ve şu anda Nisan 2022'de zorunlu olması hedeflenmektedir. Yeni kılavuz denetimi zorunlu hale geldiğinde **forceLegacyGrid()** API kabul edilmeyecek. |

### <a name="personalization-without-saved-views"></a>Kaydedilmiş görünümler olmadan kişiselleştirme 

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Kullanımı sonlandırma/kaldırma nedeni** | Kişiselleştirme alt sistemi, çok daha iyi performansa sahip olması ve ek özellikler sunması için kaydedilmiş görünümler özelliğiyle yenilendi. |
| **Başka bir özellikle mi değiştirildi?**   | Kayıtlı görünümler |
| **Etkilenen ürün alanları**         | Web istemcisi |
| **Dağıtım seçeneği**              | Tümü |
| **Durum**                         | Sürüm 10.0.13/Platform güncelleştirmesi 37'de, kaydedilmiş görünümler özelliği genellikle kullanılabilirdir ve müşteriler isteğe bağlı olarak bu özelliği açabilir. Kaydedilmiş görünüm özelliği Ekim 2021 sürümünde zorunlu olacaktır. |


## <a name="platform-updates-for-version-10012-of-finance-and-operations-apps"></a>Finans ve operasyon uygulamalarının 10.0.12 sürümü için platform güncelleştirmeleri

### <a name="grid-or-group-control-form-extensions-containing-invalid-field-references"></a>Geçersiz alan başvurularını içeren kılavuz veya Grup denetimi formu uzantıları

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Kullanımı sonlandırma/kaldırma nedeni** | Kılavuz veya grup denetimlerindeki veri grubu özelliği, bir alan grubunun tüm alanlarını otomatik olarak göstermek için kullanılır. Uzantıya göre eklenen bir kılavuz veya Grup denetimi, alan grubunda artık tanımlanmamış alanlar içerebilir veya alan grubunda tanımlanmış alanlar eksik olabilir. Bu durum çalışma zamanında tutarsız davranışlara neden olabilir. Finans ve operasyon uygulamalarının 10.0.12 sürümü için platform güncelleştirmeleri bu sorunu bir derleyici *uyarı* olarak sınıflandırır. Bu sorunu gidermek için, form uzantısını açın ve kaydedin.
| **Başka bir özellikle mi değiştirildi?**   | Bu derleyici uyarısı gelecekteki bir güncelleştirmede bulunan bir derleyici hatasıyla değiştirilecektir. |
| **Etkilenen ürün alanları**         | Visual Studio geliştirme araçları |
| **Dağıtım seçeneği**              | Tümü |
| **Durum**                         | Derleyici uyarısı, finans ve operasyon uygulamalarının 10.0.12 sürümü platform güncelleştirmelerinde bir derleyici hatasıdır. |

## <a name="platform-updates-for-version-10011-of-finance-and-operations-apps"></a>Finans ve operasyon uygulamalarının 10.0.11 sürümü için platform güncelleştirmeleri

### <a name="explicit-safe-lists-for-self-service-environments"></a>Self servis ortamları için açık güvenli listeler

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Kullanımı sonlandırma/kaldırma nedeni** | IP'yi güvenli listelere taşıma işlemi değiştirildi. Self servis artık IP güvenli listelerini desteklemiyor. |
| **Başka bir özellikle mi değiştirildi?**   | Daha fazla bilgi için bkz. [Azure Active Directory Koşullu Erişimi yapılandırma](/appcenter/general/configuring-aad-conditional-access).|
| **Etkilenen ürün alanları**         | Güvenlik |
| **Dağıtım seçeneği**              | Bulut |
| **Durum**                         | Kullanım dışı: Bu özellik self servis dağıtımları için tam olarak kullanım dışıdır. |

### <a name="visual-studio-2015"></a>Visual Studio2015

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Kullanımı sonlandırma/kaldırma nedeni** | Visual Studio'Nin en son sürümlerini desteklemek için Visual Studio için X++ uzantılarında bazı değişiklikler yapılmalıdır . Bu değişiklikler Visual Studio 2015 ile uyumsuz . |
| **Başka bir özellikle mi değiştirildi?**   | Visual Studio 2017, Dağıtılmış ve gerekli sürüm olarak Visual Studio 2015 yerine çalışacak. |
| **Etkilenen ürün alanları**         | Visual Studio geliştirme araçları |
| **Dağıtım seçeneği**              | Tümü |
| **Durum**                         | Sürüm 10.0.13 (Platform update 37) veya sonraki sürümler üzerinde dağıtılan sanal makineler Visual Studio 2017 içerir. Sürüm 10.0.16 (Platform update 40), Visual Studio 2015 desteği sunan son sürümdür. Yalnızca Visual Studio 2015 bulunan sanal makineler, sürüm 10.0.17'ye (Platform update 41) güncelleştirilemeyecektir. |

### <a name="field-groups-containing-invalid-field-references"></a>Geçersiz alan referansı içeren alan denetimleri

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Kullanımı sonlandırma/kaldırma nedeni** | Tablo meta veri tanımlarındaki alan grupları, geçersiz alan referansları içerebilir. Bu alan grupları dağıtılırsa, Financial Reporting ve  Microsoft SQL Server Reporting Services (SSRS) içinde çalışma zamanı hatalarına neden olabilir. Platform güncelleştirmesi 23, bu meta veri veri sorununun giderilmesi için bir derleyici *uyarısı* getirdi. Finans ve operasyon uygulamalarının 10.0.11 sürümü için platform güncelleştirmeleri bu sorunu bir derleyici *hata* olarak sınıflandırır.<p>Bu sorunu düzeltmek için aşağıdaki adımları izleyin.</p><ol><li>Geçersiz alan referansını tablo alanı grubu tanımından kaldırın.</li><li>Yeniden derleyin.</li><li>Hataların giderildiğinden emin olun.</li></ol> |
| **Başka bir özellikle mi değiştirildi?**   | Bu derleyici hatası, derleyici uyarısının kalıcı olarak yerini alır.  |
| **Etkilenen ürün alanları**         | Visual Studio geliştirme araçları |
| **Dağıtım seçeneği**              | Tümü |
| **Durum**                         | Kullanım dışı: Derleme uyarısı, finans ve operasyon uygulamalarının 10.0.11 sürümü platform güncelleştirmeleri ile derleme hatasıdır. |

### <a name="isv-licenses-created-by-using-the-sha1-hashing-algorithm"></a>SHA1 karma algoritması kullanılarak oluşturulan ISV lisansları

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Kullanımı sonlandırma/kaldırma nedeni** | Bağımsız yazılım satıcısı (ISV) lisansları oluşturma işlemi değişti. Daha fazla bilgi için bkz. [Bağımsız yazılım satıcısı (ISV) lisansı](../dev-tools/isv-licensing.md#appendix-create-self-signed-certificates-for-test-purposes). |
| **Başka bir özellikle mi değiştirildi?**   | Evet. Lisans oluşturmak için Windows PowerShell'i kullanın. |
| **Etkilenen ürün alanları**         | Visual Studio geliştirme araçları |
| **Dağıtım seçeneği**              | Tümü |
| **Durum**                         | Kullanım dışı: SHA1 karma algoritması kullanılarak oluşturulan ISV lisansları. Bu algoritma MakeCert yardımcı programı kullanılarak oluşturulan sertifikalara bağımlıydı ve bu yardımcı program kullanım dışı bırakıldı.<br><br>Kullanım dışı: Güvenlik veya karma amaçlar için SHA1 kullanımı. SHA1 işlevi, 2021'in ilk dönemlerinde sonlandırılacaktır. Bu nedenle, artık kullanılmamalıdır.<br><br>Kaldırıldı: Aktarım Katmanı Güvenliği (TLS) 1.0 ve TLS 1.1 gelen veya giden istekleri için destek. |

## <a name="platform-update-32"></a>Platform update 32

### <a name="workflow-request-change-dialog-box-no-longer-includes-user-selection-drop-down-list"></a>İş akışı isteği değişikliği iletişim kutusu artık kullanıcı seçimi açılan listesini içermiyor

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Kullanımı sonlandırma/kaldırma nedeni** | Değişiklik isteği istenmeyen bir kullanıcıya gönderilebileceğinden bu bir güvenlik sorunudur. Bu aynı zamanda bir kullanılabilirlik sorunudur ve kullanıcıyı iş akışının kaynağını belirlemeye ve bunları el ile seçmelerine olanak sağlar.  |
| **Başka bir özellikle mi değiştirildi?**   | Hayır |
| **Etkilenen ürün alanları**         | İş akışı |
| **Dağıtım seçeneği**              | Tümü |
| **Durum**                         | Kullanıcı seçimi açılan listesi, platform güncelleştirmesi 32 ' deki istek değişimi iletişim kutusundan kaldırıldı. İstek değişikliği istekleri oluşturana otomatik olarak istendiği gibi gönderilecek. Bu işlevsellik hakkında daha fazla bilgi için bkz. [İş akışı onay sürecindeki eylemler](../../fin-ops/organization-administration/workflow-actions.md?toc=%2fdynamics365%2fcommerce%2ftoc.json#request-change). |

### <a name="embedded-drill-through-links-are-no-longer-supported-in-paginated-documents-rendered-by-the-cloud-hosted-service"></a>Katıştırılmış ayrıntılandırma bağlantıları bulut tarafından barındırılan hizmet tarafından işlenen sayfalandırılmış belgelerde artık desteklenmiyor 

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Kullanımı sonlandırma/kaldırma nedeni** | Hizmet tarafından işlenen belgelere katıştırılmış olan gezinti URL'leri hassas iş verileri içerebilir. Müşteri verilerini daha iyi korumak amacıyla bir güvenlik önlemi olarak belgelerdeki katıştırılmış ayrıntılandırma bağlantıları için desteği kaldırıyoruz. Kullanıcılar ayrıca, bu değişikliğin sonucunda etkileşimli olarak belge oluştururken gelişmiş performanstan da yararlanacaktır.  |
| **Başka bir özellikle mi değiştirildi?**   | Hayır |
| **Etkilenen ürün alanları**         | Raporlama |
| **Dağıtım seçeneği**              | Tümü |
| **Durum**                         | Bu özellik, hizmetten etkin olarak kaldırılmaktadır.<br><br>Modern istemci, uygulamada gezinme konusunda yardımcı olacak otomatik oluşturulmuş bağlantılar içeren görünümler üretmek için birçok seçenek sunar. Hizmet tarafından işlenen sayfalandırılmış belgeler e-postayla gönderilen, arşivlenen ve alıcılar için yazdırılan harici iletişimler için önerilir. Belgeleri doğrudan tarayıcıda önizleme deneyimini geliştirdik (yerel yazıcılara doğrudan erişim sunar). Daha fazla bilgi için bkz. [Katıştırılmış görüntüleyiciyle PDF belgelerini önizleme](../analytics/preview-pdf-documents.md). |

## <a name="previous-announcements-about-removed-or-deprecated-features"></a>Kaldırılmış veya kullanım dışı bırakılmış özellikler hakkındaki önceki duyurular
Önceki sürümlerde kaldırılmış veya kaldırılmış özellikler hakkında daha fazla bilgi edinmek için, [önceki sürümlerdeki kaldırılmış veya kaldırılmış özelliklere](../migration-upgrade/deprecated-features.md) bakın.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

