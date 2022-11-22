---
title: Finans ve operasyon altyapısına Dynamics 365 Human Resources müşteri geçişi
description: Bu makalede, finans ve operasyon altyapısına Microsoft Dynamics 365 Human Resources müşteri geçişi yapma açıklanmaktadır.
author: twheeloc
ms.date: 10/25/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-10-13
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 4df9a68ea0128378224bf77bd66423fd2e13fa55
ms.sourcegitcommit: e5b290bac7e8f468167caa1a5607aac6eac9aaea
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/11/2022
ms.locfileid: "9760375"
---
# <a name="dynamics-365-human-resources-customer-migration"></a>Dynamics 365 Human Resources müşteri geçişi

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]
[!include [preview banner](../includes/preview-banner.md)]

Müşteri geçişi, müşteri veritabanının finans ve operasyonlar alt yapısına "lift-and-shift ile taşımak geçişi" (hareket) sağlar. Otomatik geçiş aracı kullanılır. Sonuç, müşterinin Human Resources veritabanını kullanan yeni bir finans ve operasyonlar ortamıdır.

## <a name="prerequisites"></a>Ön Koşullar

### <a name="user-access-and-permissions"></a>Kullanıcı erişim ve izinleri

- Microsoft Dynamics Lifecycle Services kullanıcısının **Kuruluş Yöneticisi** rolü olmalıdır.
- Kullanıcı, [Azure DevOps projeleri oluşturabilmeli](/azure/devops/organizations/projects/create-project) veya varolan Azure DevOps projesini kullanabilmelidir.
- Kullanıcının, [Azure DevOps kişisel erişim güvenlik belirteci](/azure/devops/organizations/accounts/use-personal-access-tokens-to-authenticate) oluşturmak için erişimi olmalıdır veya kullanılabilecek bir belirteç olmalıdır.

### <a name="dataverse-environment-backup-sandbox"></a>Dataverse ortam yedeği (Korumalı alan)

 - İsteğe bağlı ancak önerilen: Human Resources üretim ortamının bir kopyasını kullanarak varolan Human Resources korumalı alan ortamını yenileme.
 - Power Platform yönetici merkezini kullanarak yeni bir Dataverse ortamı oluşturma.
 - Bağımsız Human Resources uygulaması ile bağlantılı varolan Dataverse ortamını, önceki adımda oluşturduğunuz ortama kopyalayın.

> [!NOTE]
> Veritabanı eklediğinizde, **Dynamics 365 uygulamalarını etkinleştir** seçeneğinin **Evet** olarak ayarlandığından emin olun. Ayrıntılı bilgi için bkz. [Power Platform ortamı hazırlama](hr-cust-migration.md#prepare-a-power-platform-environment)

### <a name="dataverse-capacity"></a>Dataverse kapasitesi

1. [Dataverse depolamasının](/power-platform/admin/finance-operations-storage-capacity) ortam kopyası için yeterli kullanılabilir kapasiteye sahip olduğunu doğrulamak için Power Platform yönetim merkezindeki **Özet** sayfasını kullanın.
2. Yeterli kapasite yoksa, genel tüketimi azaltmak için [depolama alanı boşaltma kılavuzunu](/power-platform/admin/free-storage-space) kullanın. Müşteriler ayrıca [ek depolama kapasitesi de ekleyebilir](/power-platform/admin/add-storage).

## <a name="customer-migration-process"></a>Müşteri geçişi işlemi

### <a name="create-a-lifecycle-services-project-for-human-resources-migration"></a>Human Resources geçişi için bir Lifecycle Services projesi oluşturun

İlk adım, Lifecycle Services'te yeni bir finans ve operasyon uygulama projesi oluşturmaktır. Müşterinin varolan Human Resources Lifecycle Services projesi olacaktır. Mevcut Human Resources ortamları, yeni finans ve operasyonlar Uygulama projesine geçirilir.

Bir yeni proje oluşturmak için şu adımları izleyin.

1. Lifecycle Services'te genel yönetici veya atanan hizmet hesabı kullanıcısı olarak oturum açın.
2. Lifecycle Services giriş sayfasında, **Oluştur/yeni (+)** seçeneğini belirleyin.
3. Ürün olarak finans ve operasyonlar uygulamalarını seçin.
4. **Proje amacı** alanında **Uygulama**'yı seçin.
5. Proje adı ve açıklama girin.
6. **Proje özel türü** alanında, **Microsoft Dynamics 365 Human Resources geçişi**'ni seçin.
7. Hüküm ve koşulları kabul etmek için onay kutusunu seçin.
8. **Oluştur**'u seçin.

Yeni bir Lifecycle Services projesi oluşturduktan sonra, yapılandırmak için aşağıdaki adımları izleyin.

1. Proje ekleme işlemini tamamlamak için **proje eklemeyi** seçin. Daha fazla bilgi için bkz. [Proje ekleme](../fin-ops-core/dev-itpro/lifecycle-services/project-onboarding.md).

    - Geçerli ortamlarınızla aynı bölgeyi seçin. Bu seçim geçişi etkilemeyecek.
    - Eski sistemlerde, **Diğer**'i seçin.

2. Proje ayarlarını tamamlayın. Bu adımın bir parçası olarak, gerekli olmaları halinde SharePoint çevrimiçi kitaplığı, Azure DevOps'u ve Azure bağlantılarını konfigüre etmelisiniz. Daha fazla bilgi için bkz. [Lifecycle Services (LCS) kullanıcı kılavuzu](../dev-itpro/lifecycle-services/lcs-user-guide.md).

> [!NOTE]
> Müşteriler varolan bir Azure DevOps projesini ve ilişkili kişisel erişim güvenlik belirtecini kullanabilir. Varolan bir proje kullanılırsa, projeyle ilişkili yapılandırmalar otomatik olarak kullanılabilir ve doğruluk açısından gözden geçirilebilir.

### <a name="migrate-a-human-resources-sandbox-environment"></a>Human Resources korumalı alan ortamını geçirme

#### <a name="prepare-to-migrate-the-sandbox-environment"></a>Korumalı alan ortamını geçirmeye hazırlık

Yeni bir Lifecycle Services projesi oluşturulduktan ve proje ekleme işlemi tamamlandıktan sonra, ilk ortamınızı geçirmeye hazırsınız demektir. Bu işleme başlamadan önce, tek başına alt yapı üzerinde üretim ortamınızdan geçirmek istediğiniz korumalı alan ortamını yenilemenizi öneririz.

#### <a name="prepare-a-power-platform-environment"></a>Power Platform ortamını hazırlama

> [!NOTE]
> Bu adım yalnızca korumalı alan ortam geçişi için geçerlidir. Üretim ortamını geçirirken, üretim ortamına iliştirilmiş varolan Power Platform yönetim merkezi ortamı ileri taşınır. Veritabanı eklediğinizde, **Dynamics 365 uygulamalarını etkinleştir** düğmesinin **Evet** olarak ayarlandığından emin olun. 

- Power Platform Yönetim Merkezinde, korumalı alan geçişi için kullanmak için [veritabanı ile bir ortam oluşturun](/power-platform/admin/create-environment#create-an-environment-with-a-database) veya varolan bir ortamı seçin.
- Eşleme için kullanılacak Power Platform ortamını yenilemek için [ortam kopyalayın](/power-platform/admin/copy-environment).

#### <a name="migrate-the-sandbox-environment"></a>Korumalı alan ortamını geçirme

1. Lifecycle Services'te genel yönetici veya atanan hizmet hesabı kullanıcısı olarak oturum açın.

    > [!NOTE]
    > Adlı kullanıcı hesabı kullanmanızı öneririz. Oturum açan kullanıcının, bağımsız Human Resources Lifecycle Services projesinde güvenlik rolü **Proje sahibi** veya **Ortam yöneticisi** olmalıdır.

2. Yeni oluşturulan Human Resources geçiş projesini açın.
3. Taşıma yöntemi ve proje ekleme için uygun aşamaları gözden geçirin ve tamamlayın.
4. Proje panosunda, **Varsayılan: Standart kabul testi** bölmesinde **HR'yi geçir**'i seçin.
5. **Geçirilecek ortamı seç** bölmesine, uygun Lifecycle Services projesini ve kaynak Human Resources ortamını (bağımsız kaynak Human Resource uygulamasından) seçin.
6. **Yeni Power Platform ortamına eşleştir**'i etkinleştirin ve uygun Power Platform ortamını seçin. Sonra **İleri**'yi seçin.
7. Ayrıntıları ve müşteri oturum açmasını onaylamak için **Dağıtım ayarları (finans ve operasyonlar - korumalı alan)** sihirbazını tamamlayın ve **Dağıt**'ı seçin.

Ortam durumu ilerlemeyi gösterir. Durum, **Yükleme** durumundan **Dağıtılıyor**'a ve **Dağıtıldı**'ya değişir.

> [!NOTE]
> Üretim bölmesi, canlı proje hazırlık listesi tamamlanana kadar kullanılamaz. Daha fazla bilgi için bkz. [Kullanıma alma için hazırlık](../fin-ops-core/fin-ops/imp-lifecycle/prepare-go-live.md).

#### <a name="considerations-and-assumptions"></a>Dikkat edilecek hususlar ve varsayımlar

Kiracıda bulunan ve aşağıdaki özelliklere sahip bir Lifecycle Services projesinde bir Human Resources korumalı alan ortamı bulunmaktadır:

- Human Resources korumalı alan ortamı, varolan bir birleştirilmiş ortamla bağlantılı değil. Belirli bir Human Resources ortamı için bir seferde yalnızca bir geçiş devam ediyor olabilir.
- Bir seferde izin verilen korumalı alan ortamları sayısı Human Resources lisanslarına bağlıdır. Kiracı için yeterli lisans satın alındıysa, projenin **Ortam** bölmesinde ek korumalı alan ortamları listelenecektir.
- Aynı türdeki ortamlarda geçişler yapılmalıdır. Başka bir deyişle, yalnızca korumalı alan ile korumalı alan veya üretimden üretim arası geçişler yapılabilir.

    > [!NOTE]
    > Üretim veya sanal alan durumu saptanmışsa, yalnızca Human Resources ortam türleri dikkate alınır. Ortamlar yanlış kategorize edilir (diğer bir deyişle, bir üretim ortamı bir koruma alanı ortamı olarak işaretlenmişse veya bir korumalı alan ortamı üretim ortamı olarak işaretlenmişse), Desteğe başvurun.

- Geçiş işlemi başarılı olmazsa, bir hata iletisi görüntülenir ve bir **Sil** düğmesi kullanılabilir hale gelir. Başarısız geçişi silmek için bu düğmeyi kullanın. Daha sonra ortamı yeniden geçirebilirsiniz.

#### <a name="validate-the-sandbox-migration"></a>Korumalı alan geçişini doğrula

Korumalı geçiş işlemi başarılı bir şekilde tamamlandıktan sonra, tüm iş süreçlerinde doğrulama ve oturumu kapatma için ayrıntılı bir test planı oluşturun.

Sınamaya başlamadan önce aşağıdaki ayrıntıları doğrulayın:

- Oluşturulan URL'de geçirilen ortama erişilebildiğini doğrulayın.
- Kullanıcıların geçirilen korumalı alana erişebileceğini doğrulayın.
- Geçirilmiş korumalı alan ortamıyla ilişkilendirilmiş olan Dataverse ortamına erişilebildiğini doğrulayın.
- En güncel verilerin kullanılabilir olduğunu onaylamak için farklı verileri denetleyin.
- Doğrulama için kritik iş süreçlerini tamamlayın.
- Güvenlik ilkelerinizin uygulanabilir olduğunu onaylayın.
- Toplu işlerin beklendiği gibi tetiklendiklerini doğrulayın.

Geçirilen sanal alana Uzak Masaüstü erişiminiz olmayacak. Katman 2+ korumalı alan ortamlarınız için aşağıdaki eylemleri gerçekleştirmek üzere kendi kendine hizmet özelliklerini ve araçlarını kullanabilirsiniz:

- [Azure SQL veritabanına](../fin-ops-core/dev-itpro/deployment/deploymentfaq.md#access-the-azure-sql-database) erişin.
- [Günlük dosyalarına](../fin-ops-core/dev-itpro/deployment/deploymentfaq.md#access-log-files) erişin.
- [Perfmon araçlarını](../fin-ops-core/dev-itpro/deployment/deploymentfaq.md#use-perfmon-tools) kullanın.
- [Bakım modunu](../fin-ops-core/dev-itpro/deployment/deploymentfaq.md#access-self-service-logs) açın/kapatın.
- [Hizmetleri](../fin-ops-core/dev-itpro/deployment/deploymentfaq.md#restart-services) yeniden başlat.
- [Regression Suite Automation Tool'u](../fin-ops-core/dev-itpro/deployment/deploymentfaq.md#configure-the-regression-suite-automation-tool) yapılandırın.

Daha fazla bilgi için bkz. [Self hizmet dağıtım ile ilgili SSS](../fin-ops-core/dev-itpro/deployment/deploymentfaq.md).

### <a name="migrate-a-human-resources-production-environment"></a>Human Resources üretim ortamını geçirme

Bir korumalı alan ortamını taşımayı ve doğrulamayı bitirdikten sonra, üretim ortamını geçirmek için aşağıdaki adımları izleyin.

#### <a name="prerequisites"></a>Ön Koşullar

- Abonelik tahmin aracının tamamlanmış olması gerekir.
- Kullanıma sunma [hazırlık değerlendirmesi](../fin-ops-core/fin-ops/imp-lifecycle/prepare-go-live.md) tamamlanmalıdır.

#### <a name="migrate-the-production-environment"></a>Üretim ortamını geçirme

1. Lifecycle Services'te genel yönetici veya atanan hizmet hesabı kullanıcısı olarak oturum açın.

    > [!NOTE]
    > Adlı kullanıcı hesabı kullanmanızı öneririz. Oturum açan kullanıcının, Lifecycle Services projesinde güvenlik rolü **Proje sahibi** veya **Ortam yöneticisi** olmalıdır.

2. Yeni Human resources geçiş projesini açın.
3. Taşıma yöntemi ve proje ekleme için uygun aşamaları gözden geçirin ve tamamlayın.
4. Proje panosunda, **Üretim** bölmesinde **HR'yi geçir**'i seçin.
5. **Geçirilecek ortamı seç** bölmesine, uygun Lifecycle Services projesini ve kaynak Human Resources ortamını (bağımsız kaynak Human Resource uygulamasından) seçin. Sonra **İleri**'yi seçin.
6. Ayrıntıları ve müşteri oturum açmasını onaylamak için **Dağıtım ayarları (finans ve operasyonlar - korumalı alan)** sihirbazını tamamlayın ve **Dağıt**'ı seçin.

Ortam durumu dağıtım ilerlemesini gösterir. Durum, **Yükleme** durumundan **Dağıtılıyor**'a ve **Dağıtıldı**'ya değişir.

#### <a name="post-migration-considerations"></a>Tümleştirme sonrasıyla ilgili değerlendirmeler

- Ortamlarınızda son [kalite güncellemesini](/fin-ops-core/fin-ops/get-started/quality-updates) uygulama.
- [Sanal tabloları](hr-admin-integration-common-data-service-virtual-entities.md) kullanıyorsanız, son noktaları yeniden konfigüre edin.
- Çift-yazma tümleştirmesini yeniden yapılandırın. Hangi varlıkların etkinleştirilmesi gerektiğini değerlendirin.
- Tümleştirme amacıyla çift yazıyı değiştirmek için sanal tabloları kullanmayı düşünün.

#### <a name="dual-write-integration"></a>Çift yazma tümleştirmesi

##### <a name="set-up-microsoft-power-platform-dual-write-integration"></a>Microsoft Power Platform çift-yazma tümleştirmesini kurun

1. Power Platform yönetim merkezine gidin ve sol gezinti bölmesinde **Ortamlar**'ı seçin.
2. Daha önce kopyalanmış/yenilenen ortamı seçin ve durumun **Hazır** olduğunu onaylayın.
3. Lifecycle Services'a gidin ve geçiş projesinin durumunun **Dağıtıldığını** doğrulayın.
4. Geçirilen ortam altında ek ayrıntıları görüntülemek ve [çift-yazma uygulaması kurmak](../fin-ops-core/dev-itpro/data-entities/dual-write/lcs-setup.md#set-up-dual-write-for-new-or-existing-dataverse-environments) için **Tüm ayrıntılar**'ı seçin.
5. **Çift yazma uygulama yapılandırması** bölmesinde, veritabanları arasında veri eşlemeyi ve eşitlemeyi kabul etmek için onay kutusunu seçin ve **Yapılandır**'ı seçin.
6. Bir ileti kutusu başarılı bir ikili yazma yapılandırması bildirdiğinde, **Tamam**'ı seçin.
7. Konfigürasyonda ayrıntıların ilerlemesini izleyebilirsiniz.
8. Konfigürasyon tamamlandığında, kullanılabilir veri varlıklarını eşitlemek için **Power Platform ortamına bağlantı**'yı seçin.
9. Durum, ortamların başarıyla bağlandığını gösteriyorsa, uygun veri varlıklarını incelemek ve seçmek için Power Platform Yönetim Merkezine gidin.
10. Sol bölmede, **Dynamics 365 uygulamaları \> Kaynaklar**'ı seçin.
11. Çift-yazma Human Resources uygulamasının durumunun **Etkin** olduğunu doğrulayın.
12. İkili yazma Human Resources uygulamasını seçin ve sonra **Yükle**'yi seçin.
13. **Çift yazma Dynamics 365 Human Resources uygulaması yükle** bölmesinde, paketin yükleneceği uygun ortamı seçin.
14. Servis koşullarını kabul etmek için onay kutusunu seçin ve sonra **Yükle**'yi seçin.
15. Dynamics 365 uygulama ortamında, yükleme devam ederken durum **Yükleniyor** olur. Yükleme tamamlandığında durum, **Yüklendi** olarak güncellenir.

##### <a name="review-and-apply-a-dual-write-solution"></a>İkili yazma çözümünü gözden geçirme ve uygulama

1. Yeni finans ve operasyonlar ortamında, **Veri yönetimi \> Çift-yazma**'ya gidin.
2. **Çözümü Uygula**'yı seçin.
3. Bölmede, **Dynamics yüklü çözümler**, **Çift yaz uygulamaları çekirdek varlık haritaları** ve **Dynamics 365 Human Resources haritalar**'ı seçin. Ardından **Uygula**'yı seçin. Bir ileti, çözümün uygulanmakta olduğunu onaylar. Çözüm başarılı bir şekilde uygulandıktan sonra, kullanılabilir tüm tablo eşlemeleri gösterilir.
4. Çift yaz kullanarak tümleştirmeyi seçmek ve çalıştırmak için kullanılabilir tablo eşlemelerini gözden geçirin.
5. Tablo eşlemeleri için ikili yazma tümleştirmesini ilk kez çalıştırdığınızda, **İlk eşitleme** onay kutusunu seçin. Kaynak Human Resources ortamından varolan bir tümleştirme varsa, tablo eşlemeleriyle ilgili tümleştirmeyi çalıştırdığınızda **İlk eşitleme** onay kutusunu seçmeniz gerekmez.

#### <a name="recommended-practices"></a>Önerilen yöntemler

Bu bölümde, tek başına altyapıdan finans ve operasyonlar alt yapısına geçiş yapma önerileri özetlenmektedir.

- Human Resources ortam geçişiniz ile ilgili yardım almak için Microsoft Dynamics ortağınızla çalışmanızı öneririz.
- Korumalı alan ortamında tam kullanıcı kabul testi (UAT) yapmak için uygun zamanı planlayın.
- Bütünleşmeleri geçirilen ortama geçirmek için ayrıntılı adımları planlayın ve belgeleyin.
- Geçiş işlemi için kesin bitiş işleminin ana hattını oluşturmak üzere ayrıntılı bir denetim listesi oluşturun.
- Geçişi yaparken işletmeniz için uygun bir kesinti süresi planlayın.
- Taşıma işleminin üstesinden gelme konusunda yardım almak için, FastTrack nitelikli müşterilerimizin FastTrack çözümü mimarisiyle çalışmasını öneririz.
- İlk geçişi yapmadan önce korumalı alan ortamınızı tek başına çalışan altyapısında yenilemenizi öneririz. Bu yenileme işlemi, geçiş işlemi planladığınız korumalı alan ortamına bağlı olan Dataverse ortamınızı içermelidir.
- Lifecycle Services projenizi dağıtırken, geçirirken ve oluşturduğunuzda bir hizmet hesabı kullanmanızı öneririz.
- En son genel kullanılabilirlik (GA) sürümü üzerinde UAT doğrulaması için korumalı alan ortamını yükseltmeyi planlayın. Daha fazla bilgi için bkz. [dikkate alınması gereken hususlar](hr-infrastructure-merge.md#considerations).
