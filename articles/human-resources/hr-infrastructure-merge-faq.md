---
title: Dynamics 365 Human Resources altyapı birleştirme hakkında SSS
description: Bu konu, Microsoft Dynamics 365 Human Resources ve Finans ve Operasyon uygulamaları için altyapı birleştirme hakkında sık sorulan soruları yanıtlar.
author: twheeloc
ms.date: 08/13/2021
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
ms.openlocfilehash: a905d752af2cf8397acb4927aa99edb4c23bfa6a
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/04/2022
ms.locfileid: "8688134"
---
# <a name="dynamics-365-human-resources-infrastructure-merge-faq"></a>Dynamics 365 Human Resources altyapı birleştirme hakkında SSS

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]



Bu konu, Microsoft Dynamics 365 Human Resources ve Finans ve Operasyon uygulamaları için altyapı birleştirme hakkında sık sorulan soruları yanıtlar.

## <a name="what-is-the-dynamics-365-human-resources-infrastructure-merge"></a>Dynamics 365 Human Resources altyapı birleştirme nedir?

Dynamics 365 Human Resources; Dynamics 365 Finance, Dynamics 365 Supply Chain Management, Dynamics 365 Commerce ve Dynamics 365 Project Operations gibi diğer Finans ve Operasyon uygulamalarından farklı bir altyapı kullanan tek başına bir uygulamadır. Altyapı birleştirme, Dynamics 365 Human Resources'ı diğer Finans ve Operasyon uygulamalarıyla aynı altyapıya getirecektir.

## <a name="value-and-benefits-of-the-infrastructure-merge"></a>Altyapı birleştirmenin değeri ve avantajları

### <a name="my-organization-uses-dynamics-365-human-resources-to-manage-its-hr-operations-what-benefits-will-we-see-from-these-changes"></a>Kuruluşum İK operasyonlarını yönetmek için Dynamics 365 Human Resources kullanır. Bu değişikliklerden ne gibi avantajlar elde edeceğiz?

- Bu değişiklikler, Dynamics 365'teki birden fazla Human Resources (HR) özellik kümesinin neden olduğu karışıklığı ortadan kaldırır.
- Hem Microsoft Power Platform genişletilebilirliği hem de iş mantığını ve özellik seçeneklerini genişletmenin bir yolunu sağlarlar.
- Uygulama Yaşam Döngüsü Yönetimi (ALM), Microsoft Dynamics Lifecycle Services (LCS), coğrafi kullanılabilirlik, genişletilebilirlik ve daha fazlası açısından Dynamics 365 Human Resources ile diğer Finans ve Operasyon uygulamaları arasında tutarlılık sağlar.
- Paylaşılan hizmetlerden ve araçlardan yararlanmanıza ve maliyetleri azaltmanıza yardımcı olurlar.

### <a name="my-organization-uses-the-human-resources-module-in-dynamics-365-finance-supply-chain-management-commerce-or-project-operations-what-benefits-will-we-see-from-these-changes"></a>Kuruluşum, Dynamics 365 Finance, Supply Chain Management, Commerce veya Project Operations'ta Human Resources modülünü kullanıyor. Bu değişikliklerden ne gibi avantajlar elde edeceğiz?

Dynamics 365 Human Resources'a eklenen özellikler ve yapılan yatırımlar artık Dynamics 365 Finance'teki İK modülünü kullanan müşteriler tarafından kullanılabilecek. Bu özelliklerden bazıları izin ve devamsızlık yönetimi, yan hak yönetimi ve görev yönetimidir.

### <a name="will-i-lose-any-features-or-capabilities-that-i-currently-use"></a>Şu anda kullandığım herhangi bir özelliği veya özelliği kaybedecek miyim?

Dynamics 365 Human Resources ile Finans ve Operasyon uygulamalarındaki İK modülü arasında işlevsel eşlik olacaktır. Dynamics 365 Human Resources, benzer özelliklere sahip olacaktır. Daha fazla bilgi için bkz. [Özellik yönetimine genel bakış](../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

### <a name="will-the-experience-change-for-my-users"></a>Kullanıcılarım için deneyim değişecek mi?

Yeni İK özellikleri Özellik yönetimi üzerinden yönetilecektir. Müşteriler özellikleri almak isteyip istemediklerine karar verecektir. Bazı durumlarda özellikler değiştirilebilir. Bu durumlarda, belgeler sağlanacaktır.

### <a name="how-does-this-change-affect-me-if-i-am-an-existing-customer-and-i-use-both-the-hr-module-on-the-finance-and-operations-infrastructure-and-dynamics-365-human-resources-through-custom-integrations"></a>Mevcut bir müşteriysem ve hem Finance and Operations altyapısındaki İK modülünü hem de özel entegrasyonlar aracılığıyla Dynamics 365 Human Resources'ı kullanıyorsam bu değişiklik beni nasıl etkiler?

Dynamics 365 Human Resources ile Dynamics 365 Finance'teki İK modülü arasındaki özel tümleştirmelere artık gerek yoktur. Tüm İK verileri diğer Finans ve Operasyon uygulamalarında olduğu gibi aynı veritabanında yer alacaktır.

## <a name="migration-from-dynamics-365-human-resources-to-finance-and-operations-apps"></a>Dynamics 365 Human Resources'dan Finans ve Operasyon uygulamalarına geçiş

### <a name="my-organization-uses-dynamics-365-human-resources-to-manage-hr-operations-what-do-we-have-to-plan-for-to-migrate-to-the-new-experience"></a>Kuruluşum İK operasyonlarını yönetmek için Dynamics 365 Human Resources kullanıyor. Yeni deneyime geçiş için ne planlamamız gerekiyor?

Kuruluşunuz Dynamics 365 Human Resources'ı kullanıyor ancak diğer Finans ve Operasyon uygulamalarını kullanmıyorsa Human Resources ortamınız yeni altyapıya geçirilir. Bu geçiş işleminin çoğu otomatikleştirilecektir. Veritabanınızı geçirmek ve yeni altyapıyla eşitlemek için işlemler uygulanacaktır.

Ayrıca, üretim ortamınızı geçirmeden önce geçiş işlemini test edebilmeniz ve verilerinizi ve deneyiminizi doğrulayabilmeniz için araçlar uygulanacaktır.

Kuruluşunuz hem Dynamics 365 Human Resources hem de diğer Finans ve Operasyon uygulamalarını kullanıyorsa verilerinizin yeni ortama doğru şekilde geçirildiğinden emin olmak için doğrulama için daha fazla zaman planlamanız gerekir. Yeni altyapıya geçiş, Human Resources ortamınızdaki verileri Finance and Operations ortamınızla birleştirir. Çakışan verilerde çakışmanın nasıl çözülmesi gerektiğini belirlemek için kullanıcı girişi gerekir. Kullanıcılar ve yöneticiler, çakışmaların olduğu veri eşlemelerini yönetmek ve üretim ortamlarının geçişinden önce korumalı alan ortamlarında geçişi test etmek zorunda kalacaktır.

### <a name="my-organization-uses-the-human-resources-module-in-dynamics-365-finance-supply-chain-management-commerce-or-project-operations-what-do-we-have-to-plan-for-to-migrate-to-the-new-experience"></a>Kuruluşum, Dynamics 365 Finance, Supply Chain Management, Commerce veya Project Operations'ta Human Resources modülünü kullanıyor. Yeni deneyime geçiş için ne planlamamız gerekiyor?

Finans ve Operasyon uygulamalarındaki İK modülünü kullanan kuruluşlar için Dynamics 365 Human Resources'daki yeni özellik işlevselliği standart One Version güncelleme işlemi aracılığıyla ortamınıza uygulanır. Her güncelleştirmede kullanılabilir hale gelirken ortamınızdaki yeni işlevselliği görmeyi bekleyebilirsiniz. Yeni özellikleri açmak için Özellik yönetimini kullanabilirsiniz ancak bu özellikleri doğrulamayı planlamanız gerekir. Ortamınızdaki diğer güncelleştirmeleri doğrulamak için uyguladığınız işlemleri izleyin. Güncelleştirmelerin Finans ve Operasyon uygulamalarına nasıl uygulandığı hakkında daha fazla bilgi için bkz. [One Version'a genel bakış](../fin-ops-core/dev-itpro/lifecycle-services/oneversion-overview.md).

### <a name="when-will-my-organization-be-migrated"></a>Kuruluşum için geçiş ne zaman yapılacak?

Her kuruluş için geçiş, geçerli yapılandırmasına ve yeni altyapıya geçişe hazır olup olmadığına bağlıdır. Bu tarihler değişebilir.

- Şu anda uygulamalarda Finans ve Operasyon uygulamalarındaki İK modülünü kullanan kuruluşlar, normal One Version güncelleştirme işlemi kapsamında Dynamics 365 Human Resources için İK işlevini alacaktır. Yeni özelliklerin Ocak 2022'den itibaren genel kullanıma sunulması planlanmaktadır.
- Yalnızca Dynamics 365 Human Resources kullanan kuruluşlar, test etmeye başlayabilmeleri ve 2022'nin ortasından itibaren geçişi başlatabilmeleri için geçiş aracına erişebilir. Yeni altyapıya geçişin tamamlanması gereken tarih henüz belirlenmedi. Ancak, geçiş aracının kullanılabilir olduğu tarihten en az bir yıl sonra olacaktır.
- Hem Dynamics 365 Human Resources ve diğer Finans ve Operasyon uygulamalarını kullanan kuruluşlar, test etmeye başlayabilmeleri ve 2022'nin sonlarından itibaren geçişi başlatabilmeleri için geçiş aracına erişebilir. Yeni altyapıya geçişin tamamlanması gereken tarih henüz belirlenmedi. Ancak, geçiş aracının kullanılabilir olduğu tarihten en az bir yıl sonra olacaktır.

Dynamics 365 Human Resources için yeni özellikler hakkında daha fazla bilgi için bkz. [Human Resources'daki yenilikler veya değişiklikler](./hr-admin-whats-new.md).

### <a name="my-organization-has-not-yet-gone-live-on-dynamics-365-human-resources-should-we-go-live-with-the-human-resources-module-in-the-finance-and-operations-apps-or-with-the-dynamics-365-human-resources-app-on-the-legacy-infrastructure"></a>Kuruluşum henüz Dynamics 365 Human Resources'ı servise almadı. Finans ve Operasyon uygulamalarındaki Human Resources modülüyle mi yoksa eski altyapıdaki Dynamics 365 Human Resources uygulamasıyla mı servise almalıyız?

Dikkate alınması gereken önemli noktalar, hangi İK işlevlerinin gerekli olduğu ve bu işlevlerin yeni altyapıda ne zaman kullanıma sunulacağıdır. Kuruluş personel yönetimi için temel işlevlere gereksinim duyuyorsa bu işlevler şu anda yeni altyapıdaki Finans ve Operasyon uygulamalarının İK modülünde kullanıma sunulmaktadır. Finans ve Operasyon uygulamalarının İK modülü ile Dynamics 365 Human Resources uygulaması arasındaki özellik eşliğinin, Mart 2022'de genel kullanıma sunulması planlanan 10.0.25 sürümünde olması beklenmektedir. Teams uygulaması ve Dataverse varlık tümleştirmeleri gibi tümleştirme özellikleri sonraki sürümlerde kullanıma sunulacaktır.

Kuruluşun İK işlevleri gereksinimi kuruluşun servise alma işlemini gerçekleştireceği zaman aralığında yeni altyapıda kullanılabilir olduğunda Finans ve Operasyon uygulamalarındaki Human Resources modülünde servise alma işlemi daha kolay hale gelebilir. Bu, Dynamics 365 Human Resources uygulamasına standart bir uygulama yükseltme işlemi olacağından ve müşteri zaten yeni altyapıda olacağından geçiş daha kolay olacaktır. Kuruluş, eski altyapı üzerinde Dynamics 365 Human Resources uygulamasında servise alma işlemine karar verirse yeni altyapıya taşınmak için bir ortam geçişi gerekir. Bu durum, yeni altyapıda servise alma işlemi yapılarak önlenebilir.

### <a name="i-am-using-new-capabilities-that-are-available-only-in-dynamics-365-human-resources-such-as-leave-and-absence-and-benefits-management-will-these-capabilities-now-be-available-in-the-human-resources-module-on-the-finance-and-operations-infrastructure-too"></a>Yalnızca Dynamics 365 Human Resources'ta kullanılabilen yeni özellikleri **(İzin ve devamsızlık** ve **Yan hak yönetimi** gibi) kullanıyorum. Bu özellikler Finance and Operations altyapısındaki İnsan Kaynakları modülünde de mevcut olacak mı?

Evet, Dynamics 365 Human Resources'taki tüm modüller Finans ve Operasyon uygulamalarında olduğu gibi çalışacak ve yüzde 100 özellik eşliği olacaktır. Şu anda İK'daki bu özellikleri kullanan müşteriler için genel geçiş stratejisinin bir parçası olarak, müşteri verileri Finance and Operations altyapısı üzerinde çalışmaya devam edecek şekilde geçirilecektir.

### <a name="i-use-the-new-dynamics-365-human-resources-benefits-management-capabilities-ive-built-custom-integrations-with-the-hr-module-on-the-finance-and-operations-infrastructure-so-that-i-can-take-advantage-of-the-payroll-capabilities-by-using-benefits-data-will-these-custom-integrations-be-required-going-forward"></a>Yeni Dynamics 365 Human Resources yan hak yönetimi özelliklerini kullanıyorum. Yan hak verilerini kullanarak bordro özelliklerinden yararlanabilmek için Finance and Operations altyapısı üzerinde İK modülüyle özel tümleştirmeler oluşturdum. Bu özel tümleştirmeler ileride gerekli olacak mı?

Altyapı birleştirmenin bir parçası olarak, İK verileri diğer Finans ve Operasyon uygulamalarıyla aynı veritabanına aktarılır. Finans ve Operasyon uygulamalarındaki modüller arasında tümleştirme artık gerekli olmayacaktır.

### <a name="my-organization-uses-one-or-more-isv-solutions-with-dynamics-365-human-resources-will-our-isv-solutions-be-migrated-automatically"></a>Kuruluşum Dynamics 365 Human Resources ile bir veya daha fazla ISV çözümü kullanıyor. ISV çözümlerimiz otomatik olarak geçirilecek mi?

Her bağımsız yazılım satıcısı (ISV) çözümü için geçiş deneyimi, çözümün tümleştirme yöntemine bağlı olarak değişir. Microsoft, yeni altyapıya sorunsuz bir geçiş sağlamak için ISV'lerle yakından çalışacaktır.

### <a name="my-organization-uses-linkedin-talent-hub-integration-with-dynamics-365-human-resources-will-this-integration-continue-to-work-after-the-infrastructure-change-is-completed"></a>Kuruluşum Dynamics 365 Human Resources ile LinkedIn Talent Hub tümleştirmesini kullanıyor. Altyapı değişikliği tamamlandıktan sonra da bu tümleştirme çalışmaya devam edecek mi?

Hayır, LinkedIn Talent Hub tümleştirmesi yeni altyapıya geçişten sonra da çalışmaya devam etmez. LinkedIn Talent Hub tümleştirmesi hizmeti, eski Dynamics 365 Human Resources altyapısıyla kullanımdan kaldırılacaktır.

### <a name="my-organization-uses-the-human-resources-app-for-teams-will-the-app-continue-to-work-after-the-infrastructure-change-is-completed"></a>Kuruluşum Teams için Human Resources uygulamasını kullanıyor. Altyapı değişikliği tamamlandıktan sonra uygulama çalışmaya devam edecek mi?

Evet, Teams için Human Resources uygulaması yeni altyapıya geçişten sonra çalışmaya devam edecektir.

### <a name="my-organization-has-configured-custom-security-in-dynamics-365-human-resources-will-our-custom-security-still-be-applied-after-the-infrastructure-change-is-completed"></a>Kuruluşum Dynamics 365 Human Resources'ta özel güvenlik yapılandırdı. Altyapı değişikliği tamamlandıktan sonra özel güvenliğimiz uygulanmaya devam edecek mi?

Evet, özel güvenlik yapılandırmaları yeni altyapıya veri geçişine dahil edilecektir.

### <a name="we-are-using-data-integrator-to-move-data-between-dynamics-365-human-resources-and-finance-and-operations-apps-how-will-the-data-that-is-currently-being-integrated-be-affected"></a>Dynamics 365 Human Resources ile Finans ve Operasyon uygulamaları arasında verileri taşımak için Veri entegratörü kullanıyoruz. Şu anda tümleşik olan veriler nasıl etkilenecek?

Şu anda Dynamics 365 Human Resources'ta bulunan İK verileri Dataverse ile eşitlenir. Daha sonra Finans ve Operasyon uygulamalarıyla tek yönlü eşitleme için Veri Entegratörü kullanılabilir. Yeni altyapıya geçişten sonra İK verileri Finans ve Operasyon uygulamalarında yerel olacaktır. Finans ve Operasyon uygulamaları ile Human Resources arasında verileri eşitlemek için artık veri entegratörü gerekli olmayacaktır.

Human Resources için geçerli Dataverse yerel veri tabloları, yeni altyapıdaki ortamda bulunan verileri eşitlemeye devam edecektir. Varlıklar çift yazmayı desteklemek için dönüştürülecektir. Diğer Dynamics 365 uygulamaları için veri entegratörü aracılığıyla bu tablolara karşı yapılandırılan diğer veri tümleştirmeleri, şu anda yapılandırıldıkları gibi çalışmaya devam edecektir.

### <a name="we-are-using-dual-write-to-move-hr-data-between-dataverse-and-other-finance-and-operations-apps-how-will-the-data-that-is-currently-being-integrated-be-affected-by-the-migration-to-the-new-infrastructure"></a>Dataverse ile diğer Finans ve Operasyon uygulamaları arasında İK verilerini taşımak için çift yazmayı kullanıyoruz. Şu anda tümleştirilen veriler yeni altyapıya geçişte nasıl etkilenecek?

İK verileri, yeni altyapıda ortamdaki Finans ve Operasyon uygulamalarına özgü olacaktır. İK verilerini yeni ortam ile Dataverse ortamı arasında taşımak için çift yazma kullanılacaktır.

### <a name="we-have-built-custom-integrations-from-dynamics-365-human-resources-to-one-or-more-external-systems-will-we-have-to-develop-new-integrations-after-the-infrastructure-change-is-completed"></a>Dynamics 365 Human Resources'tan bir veya daha fazla harici sisteme özel tümleştirmeler oluşturduk. Altyapı değişikliği tamamlandıktan sonra yeni tümleştirme geliştirmek zorunda kalacak mıyız?

Tümleştirme uç noktasına bağlıdır. Finans ve Operasyon uygulamalarında kullanılabilen tümleştirme teknolojileri ve en iyi tümleştirme teknolojisinin nasıl seçileceği hakkında daha fazla bilgi için bkz. [Tümleştirmeye genel bakış](../fin-ops-core/dev-itpro/data-entities/integration-overview.md).

### <a name="we-have-extended-dataverse-for-dynamics-365-human-resources-will-these-extensions-be-migrated-automatically"></a>Dynamics 365 Human Resources için Dataverse'ü genişlettik. Bu uzantılar otomatik olarak geçirilecek mi?

Yeni altyapıda ortamda birleştirilecek Dynamics 365 Human Resources ve Finance and Operations ortamları aynı Dataverse ortamına bağlıysa iki uygulama geçiş sonrasında da aynı Dataverse ortamına bağlı olmaya devam eder. Hiçbir Dataverse uzantısı için geçiş gerekmez.

Ancak, Dynamics 365 Human Resources ve Finance and Operations ortamları şu anda ayrı Dataverse ortamlarına bağlıysa iki Dataverse ortamının yeni altyapıda tek bir ortama bağlı olması için birleştirilmesi gerekir. Bu Dataverse geçişi için Human Resources çözümlerinde standart olan Dataverse tabloları yeni Dataverse ortamına bağlanabilir ve yeniden eşitlenebilir. Dataverse ortamındaki uzantılar otomatik olarak geçirilmez ve yeni ortamda yeniden dağıtılması gerekir. Dataverse uzantılarınızı yönetmek için yönetilen çözümler kullanmanızı öneririz. Daha fazla bilgi için bkz. [Çözümlere giriş](/powerapps/developer/data-platform/introduction-solutions).

### <a name="we-have-configured-microsoft-power-automate-flows-andor-microsoft-power-apps-to-work-with-dynamics-365-human-resources-will-these-microsoft-power-platform-components-be-migrated-and-work-automatically-after-the-infrastructure-change-is-completed"></a>Dynamics 365 Human Resources ile çalışacak Microsoft Power Automate akışları ve/veya Microsoft Power Apps yapılandırdık. Altyapı değişikliği tamamlandıktan sonra bu Microsoft Power Platform bileşenleri geçirilecek ve otomatik olarak çalışacak mı?

Power Apps, Power Automate akışları ve diğer Microsoft Power Platform özelleştirmeleri, Dataverse uzantılarına benzerdir. Yeni altyapıya geçişten sonra otomatik olarak çalışıp çalışmadıkları, Human Resources uygulamasının ve Finans ve Operasyon uygulamalarının geçiş öncesinde aynı Power Apps ortamına bağlı olup olmadığına bağlıdır.

Uygulamalar şu anda aynı Power Apps ortamına bağlıysa yeni altyapıya geçişten sonra bu Power Apps ortamına bağlı olmaya devam eder. Bu durumda, Power Apps, Power Automate akışları ve diğer Microsoft Power Platform özelleştirmeleri herhangi bir ek yapılandırma olmadan çalışmaya devam eder. Dataverse'teki uygulama uzantılarınızı yönetmek için yönetilen çözümler kullanmanızı öneririz. Daha fazla bilgi için bkz. [Çözümlere giriş](/powerapps/developer/data-platform/introduction-solutions).

Ancak, Human Resources uygulaması ve Finans ve Operasyon uygulamaları ayrı Power Apps ortamlarına bağlıysa geçişin bir parçası olarak birleştirilmeleri gerekir. Bu görev, tüm Power Apps ve diğer özelleştirmelerin yeni ortamda yeniden dağıtılmasını gerektirir.

### <a name="we-have-enabled-dataverse-virtual-tables-for-dynamics-365-human-resources-what-will-happen-to-these-tables-during-the-migration"></a>Dynamics 365 Human Resources için Dataverse sanal tabloları etkinleştirdik. Geçiş sırasında bu tablolara ne olacak?

Geçişten sonra, yeni altyapıdaki ortam şu anda Dynamics 365 Human Resources'a bağlı olan Dataverse ortamına bağlı kalırsa bu ortamda oluşturulan Dataverse sanal tabloları herhangi bir ek yapılandırma olmadan çalışmaya devam eder.

Ancak, yeni altyapıdaki ortam geçişten sonra farklı bir Dataverse ortamına bağlı olursa sanal tabloların yeni Dataverse ortamında yeniden oluşturulması gerekir.

### <a name="we-have-developed-an-integration-by-using-the-applicant-tracking-system-ats-api-payroll-api-dataverse-virtual-tables-for-dynamics-365-human-resources-or-other-entities-in-the-dataverse-web-api-will-these-integrations-continue-to-work-after-the-infrastructure-change-is-completed"></a>Başvuru İzleme Sistemi (ATS) API'sini, Bordro API'sini, Dynamics 365 Human Resources için Dataverse sanal tablolarını veya Dataverse Web API'sindeki diğer varlıkları kullanarak bir tümleştirme geliştirdik. Altyapı değişikliği tamamlandıktan sonra bu tümleştirmeler çalışmaya devam edecek mi?

Geçiştan sonra, yeni altyapıdaki ortam şu anda bağlı olduğu şu anda Dynamics 365 Human Resources'a bağlı Dataverse ortamına bağlı kalırsa Dataverse Web API'sine karşı geliştirilen tümleştirmeler geçiş tamamlandıktan sonra çalışmaya devam eder.

Ancak, yeni altyapıdaki ortam geçişten sonra farklı bir Dataverse ortamına bağlı olursa Dataverse Web API'sine karşı geliştirilen tümleştirmelerin yeni Dataverse ortamına bağlanacak şekilde yeniden yapılandırılması gerekir.

### <a name="is-there-an-impact-on-the-azure-region-when-my-environment-is-migrated"></a>Ortamım geçirildiğinde Azure bölgesi üzerinde bir etkisi olacak mı?

Human Resources ortamınızın geçiş sırasında genellikle aynı Azure bölgesinde kalması beklenir. Yalnızca Human Resources ortamı farklı bir bölgedeki bir Finance and Operations ortamıyla birleştirilirse özel durum oluşur. Bu durumda, Human Resources ortamı, Finance and Operations ortamının Azure bölgesine geçirilir.

### <a name="my-organization-depends-on-workflows-in-dynamics-365-human-resources-for-one-or-more-business-processes-will-the-workflows-be-migrated-automatically"></a>Kuruluşum, bir veya daha fazla iş süreci için Dynamics 365 Human Resources iş akışlarını kullanıyor. İş akışları otomatik olarak geçirilecek mi?

Evet, iş akışı yapılandırmaları, iş akışı geçmişi ve geçerli işlem içi iş akışları geçirilecektir.

### <a name="what-training-and-resources-will-be-available-to-help-with-the-migration-process"></a>Geçiş sürecine yardımcı olmak için hangi eğitim ve kaynaklar mevcut olacak?

Geçiş işleminin her adımını ayrıntılı olarak açıklamak için tüm belgeler sağlanacaktır. Video ve atölye gibi ek eğitim kaynakları da ihtiyaca bağlı olarak sunulabilir.

### <a name="my-organization-has-created-saved-views-in-dynamics-365-human-resources-to-improve-the-usability-of-the-interface-will-the-saved-views-be-migrated-automatically"></a>Kuruluşum, arabirimin kullanılabilirliğini artırmak için Dynamics 365 Human Resources'ta Kaydedilmiş görünümler oluşturdu. Kaydedilen görünümler otomatik olarak geçirilecek mi?

Evet, Kaydedilmiş görünümler yeni altyapıya geçirilecek.

### <a name="we-are-using-ceridian-with-dynamics-365-human-resources-will-the-ceridian-integration-be-available-after-the-infrastructure-change-is-completed"></a>Dynamics 365 Human Resources ile Ceridian kullanıyoruz. Altyapı değişikliği tamamlandıktan sonra Ceridian tümleştirmesi kullanıma sunulacak mı? 

Ceridian ile tümleştirme Bordro API'si tabanlı tümleştirmeye geçirilecektir. Şu anda Dynamics 365 Human Resources'da bulunan dosya tabanlı tümleştirme Finance and Operations altyapısına geçirilmeyecek. Daha fazla bilgi için bkz. [Bordro API'sine giriş](./hr-admin-integration-payroll-api-introduction.md).

### <a name="how-will-the-migration-affect-the-service-update-process"></a>Geçiş, hizmet güncelleştirme işlemini nasıl etkileyecek?

Geçişten sonra müşteriler ALM ve hizmet güncellemeleri açısından çok daha fazla esnekliğe sahip olacak. Hizmet güncelleştirmeleri artık Human Resources ortamlarına otomatik olarak uygulanmayacak. Bunun yerine, hizmet One Version hizmet güncelleştirme işlemlerini ve işlevselliğini izleyecek. Bu nedenle, güncellemeler için yapılandırma seçenekleri LCS üzerinden sunulacak. Daha fazla bilgi için bkz. [One Version'a genel bakış](../fin-ops-core/dev-itpro/lifecycle-services/oneversion-overview.md).

### <a name="how-will-the-migration-affect-my-lcs-project-for-dynamics-365-human-resources"></a>Geçiş Dynamics 365 Human Resources için LCS projemi nasıl etkileyecek?

Yeni altyapıya geçiş, Dynamics 365 Human Resources ortamlarınızın yönetimini LCS'de bir Finance and Operations uygulama projesine taşıyacaktır. Geçiş Dynamics 365 Human Resources'ı mevcut bir Finance and Operations ortamıyla birleştirirse Human Resources LCS projeniz Finance and Operations uygulamanızın LCS uygulama projesiyle birleştirilecektir. Şu anda yalnızca Dynamics 365 Human Resources kullanıyorsanız yeni bir LCS uygulama projesi oluşturulur ve mevcut Human Resources LCS projeniz yeni projeye geçirilir.

Yeni proje, Finans ve Operasyon uygulamalarının kullandığı proje türüyle aynı olacak. Ortam yönetimi için aynı özelliklere ve işlevlere sahip olacaktır. Daha fazla bilgi için bkz. [Lifecycle Services kaynakları](../fin-ops-core/dev-itpro/lifecycle-services/lcs.md).

### <a name="we-have-linked-our-task-recordings-to-the-business-process-modeler-in-human-resources-how-will-the-business-process-modeler-be-migrated-and-merged-into-lcs"></a>Görev kayıtlarımızı Human Resources'ndaki İş Süreci Modelleyicisi'ne bağladık. İş Süreci Modelleyicisi nasıl geçirilecek ve LCS ile nasıl birleştirilecek?

LCS projesi için iş süreci kitaplıkları, Human Resources için yeni LCS projesine geçirilecektir.

### <a name="my-organization-currently-uses-only-dynamics-365-human-resources-what-resources-are-available-so-that-we-can-learn-more-about-the-development-capabilities-after-the-infrastructure-change-is-completed"></a>Kuruluşum şu anda yalnızca Dynamics 365 Human Resources kullanıyor. Altyapı değişikliği tamamlandıktan sonra geliştirme özellikleri hakkında daha fazla bilgi edinebilmemiz için hangi kaynaklar sunulacak?

Hem Microsoft Power Platform genişletilebilirlik seçenekleri hem de Finance and Operations genişletilebilirlik seçenekleri mevcut olacak ve geliştirme için kullanılabilecek. Daha fazla bilgi için bkz. [Giriş sayfasını geliştirme ve özelleştirme](../fin-ops-core/dev-itpro/dev-tools/developer-home-page.md).

### <a name="we-have-enabled-features-in-dynamics-365-human-resources-will-these-features-be-enabled-automatically-during-the-migration"></a>Dynamics 365 Human Resources'ta özellikleri etkinleştirdik. Bu özellikler geçiş sırasında otomatik olarak etkinleştirilecek mi?

Bir özelliğin yeni altyapıda otomatik olarak etkinleştirilip etkinleştirilmediği her özellik için ayrı ayrı belirlenir. Bu bilgiler özellik belgelerine eklenecektir.

### <a name="what-happens-to-my-byod-database-during-the-migration"></a>Geçiş sırasında KVG veritabanıma ne olur?

Kendi veritabanınızı getirin (KVG) için içeri aktarma ve dışarı aktarma yapılandırmaları yeni altyapıya geçirilecektir.

### <a name="what-happens-to-my-azure-data-lake-during-the-migration"></a>Geçiş sırasında Azure Data Lake'e ne olur?

Şu anda Finans ve Operasyon uygulamalarında Azure Data Lake Storage için yapılandırılan tüm dışarı aktarmalar, geçişten sonra aynı yapılandırmayı koruyacaktır.

### <a name="we-are-currently-using-dynamics-ax-2012-will-the-upgrade-tools-that-are-currently-available-be-used-to-upgrade-the-hr-module-in-ax-2012-to-dynamics-365-human-resources"></a>Şu anda Dynamics AX 2012 kullanıyoruz. Şu anda mevcut olan yükseltme araçları, AX 2012'deki İK modülünü Dynamics 365 Human Resources'a yükseltmek için kullanılacak mi?

Evet. Dynamics 365 Human Resources, Finans ve Operasyon uygulamaları için birleştirilmiş kod tabanına ve altyapıya dahil edilecektir. Dynamics AX 2012'den Dynamics 365 Human Resources'a yükseltme, Finans ve Operasyon uygulamalarının en son sürümüne yükseltmek için kullanılan yükseltme yolunu ve aracını kullanır.

### <a name="we-use-document-handling-with-dynamics-365-human-resources-what-will-happen-to-the-documents-during-the-migration"></a>Dynamics 365 Human Resources ile Belge yönetimini kullanıyoruz. Geçiş sırasında belgelere ne olacak?

Belgeler var olan belge depolama alanında kalacaktır. Yeni altyapıda ortama yeniden eşlenecekler.

### <a name="what-happens-to-the-batch-jobs-that-we-have-configured-in-dynamics-365-human-resources-after-the-migration"></a>Geçişten sonra Dynamics 365 Human Resources'ta yapılandırdığımız toplu işlere ne olacak?

Uygulanabilir toplu işlemler otomatik olarak yeni altyapıya geçirilecektir.

## <a name="licensing-impact"></a>Lisanslama etkisi

Bu belgeler, kullanım haklarını kapsayan yasal belgelerin hiçbirinin yerini almaz veya bunları değiştirmez.

### <a name="my-organization-uses-dynamics-365-human-resources-to-manage-its-hr-operations-does-our-licensing-or-cost-change"></a>Kuruluşum İK operasyonlarını yönetmek için Dynamics 365 Human Resources kullanır. Lisanslamamız veya maliyetimiz değişecek mi?

Dynamics 365 Human Resources lisansı satın alan müşteriler etkilenmeyecektir. Bu müşteriler için lisans geçişi yoktur. Human Resources için özel olan ek korumalı alan stok tutma birimi (SKU) artık geçerli olmayacaktır. Bunun yerine, müşteriler biraz daha düşük bir maliyetle bir Finans ve Operasyon uygulamaları Katman 2 korumalı alanı satın almayı seçebilir. Human Resources korumalı alanı satın alan mevcut müşteriler, ek ücret ödemeden bir Finans ve Operasyon uygulamaları Katman 2 korumalı alanına geçirilir.

### <a name="my-organization-uses-the-human-resources-module-in-dynamics-365-finance-supply-chain-management-commerce-or-project-operations-does-my-licensing-or-cost-change"></a>Kuruluşum, Dynamics 365 Finance, Supply Chain Management, Commerce veya Project Operations'ta Human Resources modülünü kullanıyor. Lisanslamam veya maliyetim değişecek mi?

Dynamics 365 uygulamalarının mevcut kullanıcıları ile bağımsız Dynamics 365 Finance, Supply Chain Management, Commerce ve Project Operations kullanıcıları, Şubat 2025'e kadar veya geçerli lisans sözleşmesinin süresi dolana kadar (hangisi daha önce olursa) bu lisanslar kapsamında Human Resources'a erişebilir. Daha iyi maliyet tasarrufu elde etmenize yardımcı olacaksa Human Resources lisanslarına daha erken geçmeyi seçebilirsiniz. Şubat 2025'ten itibaren, mevcut tüm CSP ve EA müşterilerinin, Finans ve Operasyon uygulamalarına getirilen yeni özelliklerden yararlanmak için İK modülden çıkmaları ve Human Resources lisansı satın almaları gerekecektir.

### <a name="my-organization-is-live-with-dynamics-365-finance-supply-chain-management-commerce-or-project-operations-will-we-be-required-to-purchase-an-additional-environment-to-support-the-infrastructure-merge"></a>Kuruluşum Dynamics 365 Finance, Supply Chain Management, Commerce veya Project Operations kullanıyor. Altyapı birleştirmeyi desteklemek için ek bir ortam satın almamız gerekecek mi?

Altyapı değişikliğini desteklemek için ek ortamlar gerekmez.

