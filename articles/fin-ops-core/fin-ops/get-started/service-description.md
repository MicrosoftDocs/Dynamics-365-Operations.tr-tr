---
title: Finans ve operasyon uygulamaları için hizmet açıklaması
description: Bu makalede, finans ve operasyon uygulamaları için hizmet açıklaması sağlanmaktadır.
author: tomhig
ms.date: 04/27/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: whigginb
ms.search.validFrom: 2021-09-03
ms.openlocfilehash: 9e5160cc3961703475ffb8dc4a4daf2ae872aaba
ms.sourcegitcommit: 873d66c03a51ecb7082e269f30f5f980ccd9307f
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/06/2022
ms.locfileid: "9124958"
---
# <a name="service-description-for-finance-and-operations-apps"></a>Finans ve operasyon uygulamaları için hizmet açıklaması

[!include[banner](../includes/banner.md)]

Finans ve operasyon uygulamaları, [Microsoft Azure](https://azure.microsoft.com/overview/what-is-azure/) uygulaması üzerinde ve bu uygulama için oluşturulmuş kurumsal kaynak planlama (ERP) hizmet olarak yazılım (SaaS) teklifleridir. Finans ve operasyon hizmeti, kuruluşlara benzersiz gereksinimlerini destekleyen ve altyapıyı yönetmelerine gerek kalmadan sürekli değişen iş ortamlarına uyum sağlamalarına yardımcı olan ERP işlevleri sunar. Finans ve operasyon uygulamaları aşağıdaki çözüm alanlarından birini veya daha fazlasını içerebilir:

- [Dynamics 365 Finance](/dynamics365/finance/)
- [Dynamics 365 Human Resources](/dynamics365/human-resources/)
- [Dynamics 365 Supply Chain Management](/dynamics365/supply-chain/)
- [Dynamics 365 Commerce](/dynamics365/commerce/)
- [Dynamics 365 Project Operations](/dynamics365/project-operations/)

Bu uygulamalar, [iş zekası](/power-bi/fundamentals/power-bi-service-overview), [altyapı](https://azure.microsoft.com/global-infrastructure/), [hesaplama](/azure/service-fabric/service-fabric-overview) ve [veritabanı hizmetleri](https://devblogs.microsoft.com/azure-sql/running-1m-databases-on-azure-sql-for-a-large-saas-provider-microsoft-dynamics-365-and-power-platform/) ile birlikte kuruluşların sektöre özel ve operasyonel iş süreçlerini yürütmesini sağlar. Uygulama ortakları tarafından desteklenen müşteriler, benzersiz iş süreçlerine en uygun iş uygulaması mantığı yapılandırmasını belirler. İşlevler ve iş süreçleri, aşağıdaki çözümlerden biri veya bunların birleşimi aracılığıyla artırılabilir veya genişletilebilir:

- Yerleşik [kişiselleştirme deneyimi](personalize-user-experience.md)
- [Microsoft Power Platform](../../dev-itpro/power-platform/overview.md) araçları
- [Visual Studio](https://visualstudio.microsoft.com) tabanlı [finans ve operasyon yazılım geliştirme seti (SDK)](../../dev-itpro/dev-tools/developer-home-page.md) ve [Azure DevOps derleme otomasyonu](../../dev-itpro/dev-tools/developer-home-page.md#build-automation-using-azure)
- [AppSource](https://appsource.microsoft.com/partners) içindeki bağımsız yazılım satıcısı (ISV) çözümleri

Müşteriler, gereksinimlere göre çözüm yaklaşımlarını seçerler. [Microsoft Dynamics Lifecycle Services (LCS)](../../dev-itpro/lifecycle-services/lcs.md) içinde sağlanan araçları ve en iyi uygulamaları kullanarak çözümlerini tanımlamak, geliştirmek ve test etmek için uygulama iş ortaklarıyla birlikte çalışırlar. Dört ortak senaryo vardır:

- Standart finans ve operasyon uygulamaları "kullanıma hazır" konfigürasyonu (uzantı yok)
- Bir veya daha fazla ISV çözümü içeren finans ve operasyon uygulamaları konfigürasyonu
- Bir veya daha fazla müşteriye özel uzantı içeren finans ve operasyon uygulamaları konfigürasyonu
- Müşteriye özel uzantıların ve bir veya daha fazla ISV çözümünün birleşimini içeren finans ve operasyon uygulamaları yapılandırması

Kuruluşlar, basit ve şeffaf bir abonelik modeli aracılığıyla kullanıcıları ve iş süreçlerini kolayca ekleyerek işlerinin büyüme süreçlerini eşleştirebilir. Daha fazla bilgi için bkz. [Dynamics 365 Lisans Kılavuzu](https://www.microsoft.com/licensing/docs/view/Microsoft-Dynamics-365).

## <a name="operating-model"></a>İşletim modeli

Finans ve operasyon uygulamaları uygulamalarının işletim modeli, hizmetin yaşam döngüsü boyunca müşteri, uygulama iş ortağı ve Microsoft'un belirli rol ve sorumluluklarını tanımlar. Daha fazla bilgi için bkz. [Bulut işlemleri ve servis](../../dev-itpro/lifecycle-services/cloud-operations-servicing.md).

### <a name="customer-activities"></a>Müşteri faaliyetler

Müşteriler, çözümlerini uygulamak için[Dynamics 365 Uygulama Kılavuzu](https://community.dynamics.com/365/dynamics-365-fasttrack/p/dynamics365implementationguide), [Success by Design](/dynamics365/fasttrack/success-by-design-overview) çerçevesini takip ederek ve [Lifecycle Services](../../dev-itpro/lifecycle-services/lcs.md) içinde sağlanan araçları ve en iyi uygulama şablonlarını kullanarak iş ortakları ve [Microsoft FastTrack](/dynamics365/fasttrack/) ile çalışır. Ortak etkinlikler şunları içerir:

- Kullanıcı kimliği ve güvenlik yönetimi
- İş süreçlerini tanımlama, geliştirme ve çalıştırma
- Uzantıları tanımlama, geliştirme, test etme ve çalıştırma
- Üretim dışı dağıtımları izleme ve yönetme
- Uygulama güncelleştirmelerini yönetme ve uzantıları doğrulama
- ISV çözümlerini ve 3. taraf tümleştirmelerini yönetme

### <a name="microsoft-responsibilities"></a>Microsoft'un sorumlulukları

Microsoft, Microsoft SaaS aboneliğinde müşteri korumalı alanı ve üretim ortamlarını dağıtarak, etkin bir şekilde izleyerek ve bunlara hizmet sağlayarak finans ve operasyon hizmetini yönetir. Bu yönetim, hizmeti çalıştırmak için gerekli sistem altyapısının tahsis edilmesini ve hizmet durumu hakkında müşterilerle proaktif olarak iletişim kurulmasını içerir. Sorumluluklar şunları içerir:

**Altyapı yönetimi**
- Güvenlik ve yalıtım
- İşletim sistemleri ve sanallaştırma
- Sunucular, depolama ve ağ oluşturma
- Veri merkezi gücü, ağ oluşturma, soğutma

**Uygulama platformu yönetimi**
- 7/24 uygulama izleme ve bildirimler
- Tanılama, platform güncelleştirmeleri, yamalar, hizmet güncelleştirmeleri
- Uygulama yönlendirme, yük dengeleme, site çoğaltma
- Ortam sağlama ve yönetme
- Veritabanı yönetimi, yüksek kullanılabilirlik (HA)/olağanüstü durum kurtarma (DR), ölçek, işlemler
- Dağıtım hesaplama, ölçeği artırma, ölçeği azaltma

## <a name="system-configuration"></a>Sistem yapılandırması

Finans ve operasyon uygulamaları, hareket hacmine ve kullanıcı yüküne göre ölçeklendirilir. Her müşteri uygulaması, aşağıdaki öğelerden oluşan benzersiz bir çözüm üretir:

- **Veri bileşimi**: Davranışı, kuruluşun düzenini, ana verilerin yapısını (mali boyutlar ve stok boyutları gibi) ve işlem izleme ayrıntı düzeyini kontrol eden benzersiz bir parametreler kümesidir.
- **Uzantı ve yapılandırma**: Kod uzantılarını, ISV çözümlerini ve iş akışları, tümleştirmeler ve rapor yapılandırmalarından oluşan benzersiz yapılandırmaları kullanan uzantı mekanizmalarıdır.
- **Kullanım modelleri**: Birleşik veri akışı için yukarı akış ve aşağı akış sistemleriyle tümleştirme ve müşterilerin iş süreçlerinde kullandıkları bilgi görünümlerine göre ayırt etme olanağı sunan çevrimiçi ve toplu kullanımın benzersiz birleşimidir.

Microsoft, hareket hacimlerini ve kullanıcı eşzamanlılığını işlemek için boyutlandırılmış müşteri üretim ortamlarını yapılandırır. Microsoft aşağıdaki görevlerden sorumludur:

- [LCS Abonelik tahmin aracı](../../dev-itpro/lifecycle-services/subscription-estimator.md) içindeki müşterinin profil bilgilerine göre üretim ortamlarının kaynaklarını doğru şekilde tahsis etme
- Üretim ortamlarının hizmet kullanılabilirliğini sürekli olarak izleme ve tanılama
- Finans ve operasyon uygulamalarıyla sistem performansı sorunlarını analiz etme ve giderme

Uygulamanın yüksek performans için yapılandırıldığından emin olmak için müşterilerin şu görevleri tamamlaması gerekir:

- [LCS Abonelik tahmin aracı](../../dev-itpro/lifecycle-services/subscription-estimator.md) içinde finans ve operasyon uygulamalarının uygulanmasıyla ilgili doğru kullanım bilgileri sağlama.
- Performans ve ölçeklendirme için uzantılar oluşturup test etme.
- Performans için veri yapılandırmalarını uygun şekilde test etme.
- Servise almadan önce [performans testleri](https://community.dynamics.com/365/b/techtalks/posts/performance-testing-approach-april-30-2018) yaparak ölçeklenebilirlik sağlama.

## <a name="onboarding-and-implementation"></a>Ekleme ve uygulama

Aşağıdaki tabloda, genel ekleme ve uygulama olayları gösterilmektedir.

| İstek | Beklenen Microsoft eylemi | Beklenen müşteri/uygulama iş ortağı eylemi |
|---|---|---|
| Başlangıç teklifini satın alma | Teklifin satın alınmasından sonra müşteri tarafından tetiklenen olay temel alınarak bir LCS projesi oluşturulur. | Kurumsal Anlaşma (EA) veya Bulut Çözümü Sağlayıcısı (CSP) aşamasına geçin [ticari işlem](before-you-buy.md). İş ortağı, varsa müşteri için bir kiracı oluşturur. |
| Eklenti satın alma | Müşteriye uygulama sırasında seçilen eklenti için erişim sağlayın. | Geçerli değil |
| Uygulama planlaması ve analizi | LCS'de [İş süreci modelleyici (BPM)](../../dev-itpro/lifecycle-services/bpm-overview.md) ve [Azure DevOps ile birlikte çalışılabilirlik](../../dev-itpro/lifecycle-services/synchronize-bpm-vsts.md) gibi ilgili araçları sağlayın. | Proje planlaması yapın, Azure DevOps'u ayarlayın, sistem eklemeyi tamamlayın ve yönetici hesapları ayarlayın. |

Daha fazla bilgi için bkz. [Uygulama projesi ekleme](../imp-lifecycle/onboard.md).

## <a name="globalization"></a>Globalleştirme

Finans ve operasyon uygulamaları, dünya çapında çeşitli Azure bölgelerinde sunulur. Finans ve operasyon uygulamaları, farklı ülkeleri/bölgeleri ve ana dilleri desteklemek üzere işlevler sunar. Daha fazla bilgi için bkz. [Yerelleştirme ve düzenleme özellikleri](../../dev-itpro/lcs-solutions/country-region.md#localization-and-regulatory-features).

### <a name="countryregion-specific-considerations"></a>Ülkeye/bölgeye özel konular

- Fransa'da yerel veri yerleşimi gerektiren kuruluşlarla iş yapan, düzenlemeye tabi sektörler veya ticari kuruluşlardaki müşterilerin [Fransa'da finans ve operasyon uygulamaları](../../dev-itpro/deployment/france-local-deployment.md) uygulamasını incelemesi gerekir.
- Çin'de faaliyet gösteren müşterilerin [Azure Çin Playbook](/azure/china/) ve [Çin'de 21Vianet tarafından işletilen finans ve operasyon uygulamaları](../../dev-itpro/deployment/china-local-deployment.md) uygulamasını incelemesi gerekir.
- Rusya'da faaliyet gösteren müşterilerin [Rusça kişisel veri yerelleştirme yasasını](/business-applications-release-notes/october18/dynamics365-finance-operations/russian-regulations-on-prem#when-will-the-cloud-deployment-option-of-dynamics-365-for-finance-and-operations-be-generally-available-for-russia) incelemesi gerekir.

### <a name="general-data-protection-regulation-gdpr"></a>Genel Veri Koruma Yönetmeliği (GDPR)

Finans ve operasyon uygulamaları için, Microsoft bir işlemci işlevi görür. Finans ve operasyon uygulamaları, veri işleyici olarak müşterilerin veri denetleyicisi olarak GDPR yükümlülüklerine uymasına yardımcı olan süreçler ve özellikler sağlar. Daha fazla bilgi için bkz. [GDPR'ye Genel Bakış](../../dev-itpro/gdpr/gdpr-guide.md).

## <a name="environment-and-data-management"></a>Çevre ve veri yönetimi

Bu bölümde, hizmette gerçekleşen bazı genel ortam ve veri yönetimi olayları açıklanmaktadır.

### <a name="environment-and-data-management-events-for-production-instances"></a>Üretim örnekleri için ortam ve veri yönetimi olayları

LCS, ortam ve veri yönetimi görevlerini gerçekleştirmek için kullanılan [self servis araçlar](../../dev-itpro/deployment/infrastructure-stack.md) ve [veritabanı taşıma işlemleri](../../dev-itpro/database/dbmovement-operations.md) sağlar. Burada bazı örnekler verilmiştir:

**Olay:** [Üretim kurulumu isteme](../imp-lifecycle/go-live-faq.md#when-can-i-configure-and-request-my-production-environment)

- [Servise alınmaya hazırlık durumu incelemesini](../imp-lifecycle/prepare-go-live.md) tamamlayın ve [Microsoft FastTrack](/dynamics365/fasttrack/) takımına gönderin.
- Bir üretim kurulumu istemeden önce [LCS Abonelik tahmin aracı](../../dev-itpro/lifecycle-services/subscription-estimator.md)'nı tamamlayın.
- [LCS metodolojisinde](../../dev-itpro/lifecycle-services/create-methodology.md) belirtilen tüm uygulama görevlerini tamamlayın.

**Olay:** [Korumalı alan veritabanını bir üretim kurulumuna kopyalama](../../dev-itpro/database/dbmovement-scenario-goldenconfig.md)

- Sahte servise alma veya gerçek servise alma kesin bitiş işlemi gerçekleştirilir.

**Olay:** [Bakım modu](../../dev-itpro/sysadmin/maintenance-mode.md)

1. LCS'de bakım modunu açın.
2. Gerekli bakımı tamamlayın.
3. LCS'de bakım modunu kapatın.

### <a name="environment-and-data-management-events-for-non-production-instances"></a>Üretim dışı kurulumlar için ortam ve veri yönetimi olayları

LCS, ortam ve veri yönetimi görevlerini gerçekleştirmek için kullanılan [self servis sağlama](../../dev-itpro/deployment/infrastructure-stack.md) ve [veritabanı taşıma işlemleri](../../dev-itpro/database/dbmovement-operations.md) sağlar. Burada bazı örnekler verilmiştir:

**Olay:** [Yeni bir korumalı alan kurulumunu dağıtma](../../dev-itpro/deployment/deployenvironment-newinfrastructure.md)

- Tüm gerekli kurulumların [planlandığından](../imp-lifecycle/environment-planning.md) ve geçerli eklenti tekliflerinin satın alındığından emin olun.
- LCS'de dağıtım işlemini çalıştırın.
- LCS denetim listelerinde belirtilen tüm görevleri tamamlayın.
    
>[!NOTE]
>Geliştirme korumalı alan ortamı, [müşterinin Azure aboneliğine dağıtılan](../../dev-itpro/dev-tools/access-instances.md) ve müşteri tarafından yönetilen bir sanal makinedir (VM).

**Olay:** [Altın yapılandırma veritabanını korumalı alandan üretime kopyalama](../../dev-itpro/database/dbmovement-scenario-goldenconfig.md)

- Sahte servise alma veya gerçek servise alma kesin bitiş işlemi gerçekleştirilir.

**Olay:** [Belirli bir noktadaki üretim yedeklemesini üretim dışı bir kuruluma geri yükleme](../../dev-itpro/database/database-pitr-prod-sandbox.md)

- LCS'de [Veritabanını yenile](../../dev-itpro/database/database-refresh.md) seçeneğini çalıştırın.
- Kopyalama sonrası: Komut dosyaları aracılığıyla hassas verileri silin veya karartın, ortama özel uygulama yapılandırmalarını (tümleştirme uç noktaları gibi) ayarlayın ve kullanıcıları etkinleştirin veya ekleyin. Bu değişikliklerin bir [veri paketi](../../dev-itpro/data-entities/data-entities-data-packages.md#import-a-data-package) uygulayarak yapıldığını unutmayın.

**Olay:** [Üretim dışı kurulum veritabanını belirli bir noktaya geri yükleme](../../dev-itpro/database/database-point-in-time-restore.md)

- İşlemin geri alınamayacağını unutmayın.
- LCS 'de belirli bir noktaya geri yükleme işlemini çalıştırın.

**Olay:** Sorun giderme ve [hata ayıklama](../../dev-itpro/database/dbmovement-scenario-debugdiag.md) için Katman 2 korumalı alan veritabanını bir geliştirme korumalı alanına kopyalama

- Veritabanı dışarı aktarma işlemini, Katman 2 korumalı alan ortamındaki LCS'de çalıştırın.
- Geliştirme ortamındaki veritabanını içeri aktarın ve güncelleştirin.

## <a name="data-backup-and-retention"></a>Veri yedeklemesi ve elde tutma

SaaS aboneliğindeki finans ve operasyon ortamları için veritabanları otomatik yedeklemelerle korunur. Üretim ortamlarında, Microsoft geri alma yapmadığı sürece otomatik yedeklemeler 28 gün boyunca saklanır. Korumalı alan (Katman 2+) ortamlarında yedi gün boyunca saklanırlar. Planlı bakım güncelleştirmeleri sırasında bir hata oluşursa üretim ortamının geri alma işlemi yapılabilir.

Otomatik yedeklemeler hakkında daha fazla bilgi için bkz. [Otomatik yedeklemeler - Azure SQL Veritabanı ve SQL Tarafından Yönetilen Kurulum](/azure/azure-sql/database/automated-backups-overview?tabs=single-database).

## <a name="service-activity-responsibilities"></a>Hizmet faaliyeti sorumlulukları

Aşağıdaki tabloda, hizmetle ilgili bazı genel senaryolar ve faaliyetler açıklanmaktadır. Ayrıca faaliyetlerden Microsoft'un, müşterinin ya da hem Microsoft'un hem de müşterinin sorumlu olup olmadığını gösterir.

| Faaliyet | Microsoft'un sorumlulukları | Müşterinin sorumlulukları |
|---|---|---|
| **İlk kiracıları sağlama** | | |
| Abonelik tahmin aracını kullanarak LCS'de tahmini yükü boyutlandırın ve belirli ortamların sağlanmasını isteyin. | | X |
| Tüm üretim kurulumlarını ve üretim dışı kurulumları sağlayın. | X | |
| Dağıtılmış üretim kurulumlarını ve üretim dışı kurulumları doğrulayın. | | X |
| **Hizmet güncelleştirmeleri** | |
| Hizmet güncelleştirmelerini belirlenen üretim dışı ve üretim kurulumlarına uygulayın. | X | |
| LCS'den korumalı alan kurulumlarına hizmet güncelleştirmelerini el ile uygulayın. Güncelleştirmeyi tanımlayın, geliştirin, sınayın ve kod güncelleştirme paketini LCS'ye geri sağlayın. | | X |
| Üretim kurulumuna uygulanacak uzantı güncelleştirmelerini isteyin ve zamanlayın. | | X |
| Güncelleştirmeler uygulanmadan önce üretim kurulumu için bir kod ve veri yedeği oluşturun. | X | |
| Herhangi bir hata durumunda üretim kurulumunu koda ve veri yedeklemesine geri alın. | X | |
| **Veri yönetimi (yedekleme, geri yükleme ve güncelleştirme)** | | |
| Veritabanını yedekleyin. | X | |
| Yüksek kullanılabilirliği ve olağanüstü durum kurtarma planını belirleyin. | X | |
| Üretim kurulumu veritabanının performansını izleyin. | X | |
| Performans için üretim kurulumu veritabanını ayarlayın. | X | |
| Üretim kurulumu veritabanını, üretim dışı bir kurulum için belirli bir noktaya yenileyin. | | X |
| **Altyapıyı güncelleştirme** | | |
| Düzenli altyapı güncelleştirmeleri zamanlayın. | X | |
| **Ölçeği artırma ve azaltma (kullanıcılar, depolama ve kurulumlar)** | | |
| Ek kullanıcılar ve üretim dışı eklentiler satın alın. | | X |
| LCS Abonelik tahmin aracında kullanım değişikliklerini güncelleştirin. | | X |
| Hizmet kullanımını etkileyen önemli performans sorunlarını bildirin. | | X |
| Geçerli hizmet için gereken kaynakları proaktif olarak yönetin. | X | |
| Olayları araştırın ve sorunları giderin. | X | |
| **Güvenlik (kullanıcı erişimi)** | | |
| Kullanıcıya hizmet erişimi sağlayın. | | X |
| LCS aracılığıyla dağıtılan kurulumların yönetimi ve işletimi için LCS projesine erişim sağlayın. | | X |
| **Üretim kurulumlarını izleme** | | |
| Üretim kurulumlarını 7/24 izleyin. | X | |
| Üretim kurulumunu içeren olaylar hakkında müşteriyi proaktif olarak bilgilendirin. | X | |
| **Üretim dışı kurulumları yönetme ve izleme** | | |
| LCS kullanarak üretim dışı kurulumları yönetin. | | X |
| Üretim dışı kurulumları izleyin. | | X |

## <a name="service-update-strategy"></a>Hizmet güncelleştirme stratejisi

[Yazılım yaşam döngüsü ilkesi](../../dev-itpro/migration-upgrade/versions-update-policy.md) gereğince finans ve operasyon uygulamaları için sürekli hizmet sağlanan ve desteklenen ürünleri kapsayan Microsoft [Modern Yaşam Döngüsü İlkesi](../../dev-itpro/migration-upgrade/versions-update-policy.md#modern-lifecycle-policy) izlenir. 

Microsoft, her yıl aşağıdaki aylarda finans ve operasyon uygulamalarına yönelik sekiz hizmet güncelleştirmesi yayınlar:

- Ocak
- Şubat
- Nisan
- Mayıs
- Temmuz
- Ağustos
- Ekim
- Kasım

>[!NOTE]
>Nisan ve Ekim, ana özellik sürüm dalgalarıdır. Müşteriler, bireysel bir hizmet güncelleştirmesini art arda gelen üç güncelleştirme döngüsüne kadar duraklatabilir.

Daha fazla bilgi edinmek için aşağıdaki konuları inceleyin:

- [One Version hizmet güncelleştirmelerine genel bakış](../../dev-itpro/lifecycle-services/oneversion-overview.md)
- [LCS aracılığıyla hizmet güncelleştirmelerini yapılandırma](../../dev-itpro/lifecycle-services/configure-service-updates.md)
- [LCS aracılığıyla hizmet güncelleştirmelerini duraklatma](../../dev-itpro/lifecycle-services/pause-service-updates.md)
- [LCS aracılığıyla hizmet güncelleştirmeleri hakkında bilgilendirilme](../../dev-itpro/lifecycle-services/notifications-service-updates.md)
- [Hizmet güncelleştirmelerini doğrulamaya yönelik gerileme testi araçları](../../dev-itpro/perf-test/rsat/rsat-overview.md)
- [Dynamics 365 yol haritası ve sürüm dalgaları](https://dynamics.microsoft.com/roadmap/overview/)

## <a name="security-and-administrative-access"></a>Güvenlik ve yönetici erişimi

Finans ve operasyon uygulamaları üretim ortamına yönetici erişimi sıkı bir şekilde denetlenir ve günlüğe kaydedilir. Müşteri verileri [Microsoft Online Services Koşulları](https://www.microsoft.com/licensing/terms/productoffering)'na uygun şekilde işlenir. 

### <a name="customer-administrative-access"></a>Müşteri yönetici erişimi

Müşterinin kiracı yöneticisi, aşağıdaki tabloda açıklandığı gibi üretim kurulumlarına veya üretim dışı kurulumlara erişebilir:

| Ortam türü | Amaç | Müşteri erişimi düzeyi |
|---|---|---|
| **Üretim dışı**<br>Katman 1 korumalı alanı | Müşterilerin geliştirme, tanıtım veya eğitim amacıyla dağıttığı üretim dışı ortamdır. | Katman 1 korumalı alanı (bulutta barındırılan ortam olarak da adlandırılır), LCS'den müşterinin Azure aboneliğine dağıtılan, müşteri tarafından yönetilen bir sanal makinedir. Müşterinin Azure aboneliğindeki bir sanal makine olduğundan müşteri Uzak Masaüstü aracılığıyla ortama tam yönetici erişimi sağlayabilir. |
| **Üretim dışı**<br>Katman 2 (veya üzeri) korumalı alanı | Müşterilerin kullanıcı kabul testi, tümleştirme testi, eğitim, hazırlama veya diğer üretim öncesi senaryolar için dağıttığı üretim dışı ortamdır. | Katman 2 ve üzeri korumalı alanlar finans ve operasyon uygulamaları SaaS aboneliğine dağıtılır. Üretim dışı ortamla ilişkilendirilmiş Azure SQL veritabanlarına erişim, [tam zamanında erişim](../../dev-itpro/database/database-just-in-time-jit-access.md) aracılığıyla sağlanır. Uzak Masaüstü erişimi kullanılamaz. |
| **Üretim** | Proje [ilk servise almaya hazır olduğunda](../imp-lifecycle/environment-planning.md#production-system-readiness) üretim ortamı dağıtılır. | Üretim ortamları SaaS aboneliğine dağıtılır. Tüm erişim tarayıcı, hizmet uç noktaları veya LCS aracılığıyla gerçekleştirilir. |

### <a name="microsoft-administrative-access"></a>Microsoft yönetici erişimi

Aşağıdaki tabloda, farklı Microsoft yöneticileri için farklı erişim düzeyleri gösterilmektedir:

| Yönetici | Müşteri verileri |
|---|---|
| İşlem yanıtları takımı<br>(Yalnızca kilit personel ile sınırlıdır) | Erişim izni destek bileti aracılığıyla verilir. Erişim denetlenir ve destek faaliyetinin süresi ile sınırlıdır. |
| Microsoft Müşteri Destek Hizmetleri (CSS) | Doğrudan erişim yoktur. Müşteri, hata ayıklama sorunları için destek personeliyle birlikte çalışmak üzere ekran paylaşımını kullanabilir. |
| Mühendislik | Doğrudan erişim yoktur. İşlem yanıt takımı, hata ayıklama sorunları için mühendislik bölümüyle çalışmak üzere ekran paylaşımını kullanabilir. |
| Microsoft'taki diğer takımlar | Erişim yoktur. |

## <a name="monitoring"></a>İzleme

Microsoft, müşterilerin üretim kurulumlarını izlemek ve tanılamak için kapsamlı bir araç takımına yatırım yapmıştır. Microsoft, müşterilerin üretim ortamlarını haftada 7 gün, günde 24 saat izler. Daha fazla bilgi için bkz. [Üretim desteği ve izleme](../imp-lifecycle/production-support-monitoring.md).

| Microsoft'un sorumlulukları | Müşterinin sorumlulukları |
|---|---|
| <ul><li>Hizmetin kullanılabilirliğini izleyin.</li><li>Uygulama Nesne Sunucusu (AOS), Toplu İş, Veri İçeri Dışarı Aktarma Çerçevesi (DIXF), Commerce ve Management Reporter gibi kritik bileşenleri sistem durumu ölçümleri ve izleyiciler aracılığıyla sürekli olarak izleyin ve uyarıda bulunun.</li><li>Altyapı hizmetlerinin (Azure Active Directory \[Azure AD\] ve Azure SQL gibi) neden olduğu performans düşüşünü izleyin.</li><li>Microsoft, tek bir işlemin veya toplu işin sapmalara neden olduğunu belirlerse müşteriyle iletişim kurulduktan sonra ilgili işlem veya iş sonlandırılır.</li></ul> | <ul><li>İşlev ve performans sorunlarına neden olabilecek uygulama yapılandırmalarında ve uzantılarında yapılan değişiklikleri izleyin.</li><li>Uygulama hataları, izleme araçları kullanılarak tanılanmalıdır. Kullanıcı tarafından bildirilen performans sapmalarını tanılamak için bu araçları kullanın.</li><li>Sistemde tahmini en yüksek kullanımın üzerinde beklenen bir yük varsa Microsoft'u bilgilendirin.</li><li>Geçerli hizmet üretim kurulumunda kullanılamıyorsa müşteri, [üretim kesintisini](../../dev-itpro/lifecycle-services/report-production-outage.md) bildirmek için LCS'yi kullanabilir.</li></ul> |

Müşteriler, destek isteklerini LCS aracılığıyla çevrimiçi olarak göndererek Microsoft'un etkin ve verimli şekilde hızlı ve ayrıntılı teknik uzmanlık sunmasını sağlar. Telefon seçeneği kullanılabilse de yalnızca çevrimiçi seçenek yoksa kullanılmalıdır. Daha fazla bilgi için bkz. [Telefon desteği seçenekleri](/power-platform/admin/support-overview?toc=%2Fdynamics365%2Ffin-ops-core%2Fdev-itpro%2Ftoc.json&bc=%2Fdynamics365%2Fbreadcrumb%2Ftoc.json#is-there-a-phone-number-i-can-call-to-contact-support).

## <a name="incident-management"></a>Olay yönetimi

Microsoft, olaylara önem düzeylerine göre yanıt verir ve bunları düzeltir. Microsoft'un olay önem düzeyleri, olayın ilk değerlendirmesi sırasında ve etki ve kapsam hakkında daha fazla bilgi kullanılabilir oldukça değiştirilebilir. Olay hafifletilse de olayın önem düzeyi değişmeden kalır.

Önem düzeyleri hakkında daha fazla bilgi için bkz. [bu önem düzeyi tablosu](/power-platform/admin/support-overview#what-is-initial-response-time-and-how-quickly-can-i-expect-to-hear-back-from-someone-after-submitting-my-support-request).

## <a name="business-continuity-through-high-availability-and-disaster-recovery"></a>Yüksek kullanılabilirlik ve olağanüstü durum kurtarma aracılığıyla iş sürekliliği 

Microsoft, Azure bölgesi genelinde kesinti olması durumunda finans ve operasyon uygulamalarının üretim kurulumları için iş sürekliliği ve olağanüstü durum kurtarma sunar. Hizmet Kurtarma Süresi Hedefi (RTO) ve Kurtarma Noktası Hedefi (RPO) dahil daha fazla bilgi için bkz. [İş sürekliliği ve olağanüstü durum kurtarma](../../dev-itpro/sysadmin/business-continuity-disaster-recovery.md).

- **Yüksek kullanılabilirlik**: HA işlevi, bir Azure veri merkezindeki tek bir düğüm hatasının neden olduğu kesinti süresini önlemenin yollarını sağlar. Her hizmetin bulut mimarisi, tek bir noktadaki hata olaylarını önlemek üzere hesaplama katmanı için Azure kullanılabilirlik kümelerini kullanır. Veritabanları için HA [Azure SQL HA özellikleri](/azure/azure-sql/database/high-availability-sla) aracılığıyla sağlanır.
- **Olağanüstü durum kurtarma**: [Azure olağanüstü durum kurtarma özellikleri](/azure/best-practices-availability-paired-regions), her hizmeti Azure veri merkezinin tamamını geniş ölçüde etkileyen kesintilere karşı korur. Bu özelliklerden birkaçı şunlardır:

    - Birincil veritabanı (iş veritabanı) için Azure SQL etkin coğrafi çoğaltma.
    - Diğer Azure bölgelerinde Azure Blob Depolama'nın (belge eklerini içeren) coğrafi olarak yedekli kopyaları.
    - Azure SQL ve Azure Blob Depolama çoğaltmaları için ikincil bölge.

Müşterinin üretim kurulumunu kurtarmak için olağanüstü durum kurtarma kullanılıyorsa Microsoft ve müşteri [olay yönetimi](service-description.md#incident-management) sorumluluklarını yerine getirir.

Microsoft'un Olağanüstü Durum Kurtarma planları ve yordamları, Sistem ve Kuruluş Denetimleri (SOC) denetimleri aracılığıyla düzenli olarak incelenir. Bu uyumluluk denetimleri, Dynamics 365 finans ve operasyon uygulamaları dahil olmak üzere Microsoft DR'sinin teknik ve yordam sürecini doğrular. [SOC uyumluluğu](/compliance/regulatory/offering-soc-2) denetim raporları ve tüm diğer Uyumluluk Raporları [Microsoft Güven Merkezi Uyumluluk Teklifleri](/compliance/regulatory/offering-home) bölümünde bulunabilir.

## <a name="finance-and-operations-support-offerings"></a>Finans ve operasyon uygulamaları desteği teklifleri

Finans ve operasyon hizmetlerinin sunulduğu pazarlarda teknik destek kullanılabilir. LCS veya finans ve operasyon uygulamalarında [destek deneyimleri](../../dev-itpro/lifecycle-services/lcs-support.md) sağlanır. Burada bazı örnekler verilmiştir:

- LCS'de [konu arama](../../dev-itpro/lifecycle-services/issue-search-lcs.md)
- Finans ve operasyon uygulamaları içinde [tümleşik teknik destek](../../dev-itpro/lifecycle-services/support-experience.md)
- LCS'de [buluttan sağlanan destek](../../dev-itpro/lifecycle-services/cloud-powered-support-lcs.md)

Microsoft, finans ve operasyon uygulamaları müşterilerine üç destek planı sunar: Premier, Profesyonel Doğrudan ve aboneliğe dahil olan destek. Destek düzeyi plana göre değişiklik gösterir. Aşağıdaki tabloda, üç planın karşılaştırması gösterilmektedir.

| Destek özelliği | Premier | Uzman Doğrudan Desteği | Abonelik |
|---|---|---|---|
| Sınırsız onarım olayı gönderme | Evet | Evet | Evet |
| LCS aracılığıyla 7/24 erişim | Evet | Evet | Evet |
| Olay yanıt süresi | Bir saatten az | Bir saatten az | Sonraki iş günü |
| Danışmanlık saatleri | Havuzlar sözleşmeye göre alınır. | Hayır | Hayır |
| Ayrılmış destek hesabı yöneticisi | Evet | Hayır | Hayır |
| Ayrılmış destek mühendisi | Ayrı bir sözleşmeyle bağlı olma | Hayır | Hayır |

Daha fazla bilgi için bkz. [Destek'e genel bakış](/power-platform/admin/support-overview).

### <a name="process-to-engage-support"></a>Destekle iletişim kurma süreci

Finans ve operasyon uygulamalarını içeren olaylar olması durumunda müşteriler, LCS aracılığıyla Microsoft'a destek biletleri gönderir. CSS, olayları müşterinin destek planına ve CSS tarafından belirlenen olayın önem derecesine göre ele alır.

### <a name="service-level-agreement"></a>servis düzeyi sözleşmesi

Microsoft, hizmetin aylık yüzde 99,9 kullanılabilirlik oranını taahhüt eder. Microsoft, servis düzeyi sözleşmesinde (SLA) açıklandığı gibi geçerli hizmetin hizmet düzeyine ulaşamaz ve bunu sürdüremezse müşteri, bu hizmet için aylık hizmet ücretlerinin bir kısmını almaya hak kazanabilir. Hizmet alacağını başlatma hakkında bilgi için [SLA](https://www.microsoft.com/licensing/docs/view/Service-Level-Agreements-SLA-for-Online-Services)'nın "Talepler" bölümüne bakın.

## <a name="important-resources"></a>Önemli kaynaklar

- **[Güven Merkezi](https://www.microsoft.com/trust-center)**: Finans ve operasyon uygulamaları verilerinizin nerede depolandığı hakkında bilgiler ile gizlilik, uyumluluk ve güvenlik yordamları hakkında ek bilgiler alın.
- **[Lisans koşulları ve belgeler](https://www.microsoftvolumelicensing.com/)**: Microsoft toplu lisans programları aracılığıyla lisanslanan ürün ve hizmetlerin kullanımıyla ilgili lisans hükümlerine, koşullarına ve ek bilgilere hızla erişin.
- **[Lisans koşulları](https://www.microsoft.com/licensing/product-licensing/)**: Bu sayfadaki kaynaklar, Microsoft ticari lisans programları aracılığıyla satın aldığınız yazılım ve çevrimiçi hizmet ürünleriyle ilgili hüküm ve koşulları tanımlar.
- **[Microsoft Yaşam Döngüsü İlkesi](/lifecycle/)**: Bu sayfa, bir ürünün ömrü boyunca desteğin kullanılabilirliği için tutarlı ve tahmin edilebilir yönergeler sağlar.
- **[Lisans kılavuzu](https://www.microsoft.com/licensing/docs/view/Microsoft-Dynamics-365)**: Dynamics 365'i lisanslama hakkında daha fazla bilgi edinmek için bu kılavuzu kullanın.
- **[Müşteri desteği](https://dynamics.microsoft.com/support/)**: Dynamics 365 uygulamalarınız için sektör lideri destek alın.
- **[Dynamics Lifecycle Services](https://lcs.dynamics.com/)**: Uygulama yaşam döngünüzü yönetin ve tahmin edilebilir, tekrarlanabilir, yüksek kaliteli uygulamalara geçiş yapın.
- **[Dynamics 365 Uygulama Kılavuzu](https://aka.ms/D365ImplementationGuideFlip)** - Dynamics 365 Uygulama Kılavuzu, zamanla sınanan Success by Design ilkelerini belgelemektedir ve Dynamics 365 çözümlerini geliştirmek, oluşturmak, test etmek ve dağıtmak için tavsiyeler sunar.

## <a name="definitions"></a>Tanımlar

### <a name="azure-region"></a>[Azure bölgesi](/azure/availability-zones/az-overview#regions)

Bir veya daha fazla Azure veri merkezinin bulunduğu coğrafi bölgedir. Örnek olarak ABD ve Avrupa verilebilir.

### <a name="business-process-modeler-bpm"></a>[İş süreci modelleyici (BPM)](../../dev-itpro/lifecycle-services/bpm-overview.md)

LCS'de, finans ve operasyon uygulamalarında desteklenen Amerikan Üretkenlik ve Kalite Merkezi'nin (APQC) iş süreci tanımlarını kullanarak belirli bir uygulama için sığdırma-boşluk analizinin tamamlanmasına yardımcı olan bir araçtır.

### <a name="cloud-solution-provider"></a>Bulut çözümü sağlayıcısı

Microsoft Bulut Çözümü Sağlayıcısı (CSP) programının bir parçası olan ve müşterilere katma değerli bulut hizmetleri, destek, tek fatura ve büyük ölçekte müşteri yönetimi sağlayan bir iş ortağıdır.

### <a name="customer"></a>Müşteri

Finans ve operasyon uygulamalarını kullanan ve Office 365'te bir kiracı tarafından temsil edilen tüzel kişiliktir.

### <a name="development-environment"></a>Geliştirme ortamı

Uzantıları geliştirmek için kullanılan, üretim dışı bir korumalı alan ortamıdır. Müşteriler bu ortamı LCS'den kendi Azure aboneliklerine dağıtır. Bu ortam, tanıtım, eğitim veya diğer test görevleri için de kullanılabilir. [Katman 1 korumalı alanı](../imp-lifecycle/environment-planning.md#tier-1-vs-tier-2-and-higher) olarak da bilinir.

### <a name="downtime"></a>Kesinti süresi

Microsoft'un otomatik sistem durumu izleme ve sistem günlüklerinden belirlediği gibi, süresi dolmamış platformdaki veya hizmet altyapısındaki bir hata nedeniyle kullanıcıların oturum açamadığı ya da etkin kiracılarına erişemediği herhangi bir dönemdir. Kesinti süresi, zamanlanmış kesinti süresini, hizmet eklenti özelliklerinin kullanılamamasını, hizmette yaptığınız değişiklikler nedeniyle hizmete erişilememesini veya ölçek birimi kapasitesinin aşıldığı dönemleri içermez.

### <a name="implementation-partner"></a>Uygulama iş ortağı

Müşterinin finans ve operasyon uygulamaları çözümlerini özelleştirmek, yapılandırmak, uygulamak ve yönetmek için seçtiği iş ortağıdır.

### <a name="incident"></a>Olay

Müşterilerin finans ve operasyon hizmetini kullanırken karşılaştıkları ve LCS aracılığıyla bilet gönderdikleri sorundur.

### <a name="microsoft-customer-support-services-css"></a>Microsoft Müşteri Destek Hizmetleri (CSS)

Finans ve operasyon uygulamaları için kaliteli hizmet sağlamaya ayrılmış Microsoft global destek ekibidir.

### <a name="microsoft-dynamics-lifecycle-services-lcs"></a>Microsoft Dynamics Lifecycle Services (LCS)

Finans ve operasyon uygulamalarının deneme sürümünden uygulamaya, üretim sonrası yönetim ve desteğe kadar yaşam döngüsü yönetimi için yönetim portalıdır. Daha fazla bilgi için bkz. [Lifecycle Services Kaynakları](../../dev-itpro/lifecycle-services/lcs.md).

### <a name="non-production-instance"></a>Üretim dışı kurulum

Müşterinin uzantıları doğrulamak ve diğer geliştirme görevlerini gerçekleştirmek için kullandığı aşağıdaki hizmet kurulumlarından herhangi biridir:

- **Korumalı Alan Katmanı 1**: Geliştirici kurulumu (müşteri tarafından barındırılan)
- **Korumalı Alan Katmanı 2**: Standard Kabul Testi kurulumu
- **Korumalı Alan Katmanları 3 - 5**: Eklenti korumalı alanları

Katman 2 - 5 hakkında daha fazla bilgi için bkz. [Doğru Katman 2 veya üzeri ortamı seçme](../imp-lifecycle/environment-planning.md#selecting-the-correct-tier-2-or-higher-environment).

### <a name="production-instance"></a>Üretim kurulumu

Müşterinin "canlı" günlük hareketlerini ve iş süreçlerini yönetmek için kullandığı bir finans ve operasyon ortamıdır.

### <a name="sandbox-environment"></a>Korumalı alan ortamı

Müşterinin tanıtım, eğitim, kullanıcı kabul testi, uzantıların doğrulanması ve diğer test görevleri için kullandığı bir üretim dışı ortamdır.

### <a name="service"></a>Servis

Finans ve operasyon uygulamalarına dahil olan temel hizmetlerden herhangi biridir.

### <a name="service-level-agreement-sla-for-microsoft-online-services"></a>Microsoft çevrimiçi hizmetleri için servis düzeyi sözleşmesi (SLA)

SLA, Microsoft çevrimiçi hizmetleri için geçerlidir. Daha fazla bilgi için bkz. [servis düzeyi sözleşmeleri](https://www.microsoft.com/licensing/docs/view/Service-Level-Agreements-SLA-for-Online-Services).

### <a name="service-update"></a>Hizmet güncelleştirmesi

Microsoft, hizmet güncelleştirmeleri aracılığıyla finans ve operasyon ortamlarına tutarlı bir şekilde hizmet sağlar. Müşteriler, iş gereksinimlerine göre kendi hizmet güncelleştirme takvimlerini belirler. Daha fazla bilgi için bkz. [Bir Sürüm hizmeti güncelleştirmeleri](../../dev-itpro/lifecycle-services/oneversion-overview.md).

### <a name="success-by-design"></a>[Success by Design](/dynamics365/fasttrack/success-by-design-overview)

Bir Dynamics 365 çözümü için en uygun mimariyi, güvenlik, performans ve Kullanıcı deneyimini sağlamak amacıyla, kritik aşamalardaki bir uygulamayı sistematik olarak yönlendiren bir çerçeve.

### <a name="user"></a>Kullanıcı

Finans ve operasyon ortamlarını kullanan ve bir müşterinin kiracısıyla ilişkilendirilmiş tek bir kişi.

