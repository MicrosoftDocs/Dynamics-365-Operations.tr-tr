---
title: Human Resources müşteri geçişi SSS
description: Bu makalede, Microsoft Dynamics 365 Human Resources ile finans ve operasyon uygulamalarının birleştirilmiş altyapısına geçiş hakkında sık sorulan sorular yanıtlanmaktadır.
author: twheeloc
ms.date: 07/06/2022
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: LeavePlanFormPart, LeaveAbsenceWorkspace
audience: Application User
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 8a6f883da07bd1d3a6b0379f1582dc8556e166ff
ms.sourcegitcommit: 9310c943ac76896663e5604209034da9f8d6139c
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/14/2022
ms.locfileid: "9151093"
---
# <a name="human-resources-customer-migration"></a>Human Resources müşteri geçişi

## <a name="how-should-dynamics-365-human-resources-customers-plan-to-move-to-the-finance-and-operations-infrastructure"></a>Dynamics 365 Human Resources müşterileri finans ve operasyonlar altyapısına geçişi nasıl planlıyor?

Microsoft Dynamics 365 Human Resources müşterilerinin iki kategorisi etkilenecek ve bunların en son finans ve operasyon altyapısında olduklarından emin olmak için değişiklik yapmak zorunda kalacak:

- Dynamics 365 Human Resources kullanan ve Dynamics 365'ten başka operasyon uygulamaları bulunmayan müşteriler
- Hem Dynamics 365 Human Resources hem de Dynamics 365 Finance, Dynamics 365 Supply Chain Management, Dynamics 365 Commerce veya Dynamics 365 Project Operations kullanan müşteriler

Ait oldukları kategori ne olursa olsun, müşterilerin finans ve operasyon altyapısında yeni oluşturulan bir ortama taşıması ve birleştirmenin başarıyla tamamlandığını doğrulaması gerekecektir.

İleride Dynamics 365 Human Resources uygulaması, diğer operasyon uygulamalarından ayrı olacak şekilde kendi finans ve operasyon ortamına sahip olacak. Bu şekilde, müşteriler mevcut verilerini birleştirmek zorunda kalmadan genişletilebilirlik seçeneklerinden yararlanabilecek. Microsoft, müşterilerin üretim ortamına geçmeden önce veri geçişini test etmek ve doğrulamak için kullanabileceği araçlar ve bir korumalı alan ortamı sağlayacak. Neredeyse otomatikleştirilmiş bir işlemi mümkün kılacak olan araçlar, Ağustos ve Kasım 2022 tarihleri arasında kullanılabilir olacak.

Finans ve operasyon altyapısında başka uygulamalar kullanan müşteriler, İnsan Kaynakları verilerini mevcut bir ortamla birleştirme seçeneğine sahip olacak. 

## <a name="when-will-customers-be-moved-to-the-finance-and-operations-infrastructure"></a>Müşteriler finans ve operasyon altyapısına ne zaman geçecek?

Her şirket için geçiş, şirketin geçerli yapılandırmasına ve finans ve operasyon altyapısına geçişe hazır olup olmadığına bağlıdır. Müşterilerin ileriye dönük en iyi yolu belirlemek için Microsoft iş ortaklarıyla birlikte çalışmalarını öneririz.

- Dynamics 365 Finance içindeki **İnsan Kaynakları** modülünü kullanan kuruluşlar, düzenli Tek Sürüm güncelleştirme işleminin parçası olarak Dynamics 365 Human Resources'tan yeni yetenekleri etkinleştirebilecek. Yeni özelliklerin Ocak 2022'den başlayarak genel kullanıma sunulması planlanmaktadır.
- Dynamics 365 Human Resources kullanan kuruluşların, altyapı birleştirmeyi tamamlamak için kullanabileceği araç erişimleri olacak. Microsoft, hizmette herhangi bir kesinti oluşmasını engellemeye yardımcı olmak için geçiş sırasında müşterilerle birlikte çalışacak. Geçiş aracının kullanılabilir olduğu zamandan başlayarak, müşterilerin geçişi yapması için 12 ile 18 ay arasında bir süre verilecek.
- Hem Dynamics 365 Human Resources hem de **İnsan Kaynakları** modülünü kullanan kuruluşlar, tek başına İnsan Kaynakları altyapısını finans ve operasyon altyapısına taşıyabilir. Başka bir seçenek de, ortamları tek bir ortama getirmek için birleştirme aracını kullanmaktır. İki ortamı birleştirmek için bir gereksinim veya zaman çerçevesi yok.

Güncel bilgiler için, [Yayın planlarını](/dynamics365/release-plans/) düzenli olarak denetleyin.

## <a name="will-customers-still-need-custom-integrations-between-dynamics-365-human-resources-and-the-human-resources-module"></a>Müşteriler Dynamics 365 Human Resources ve İnsan Kaynakları modülü arasında özel tümleştirmelere hala gereksinim duyar mı?

- Hem Dynamics 365 Human Resources hem de günümüzde tümleşik olan diğer finans ve operasyon altyapısı ortamlarına sahip müşteriler, birleştirme sonrasında iki ortamı tümleştirmeye devam etmesi gerekecek.
- Dynamics 365 Human Resources ortamını, mevcut finans ve operasyon uygulaması ortamından ayrı tutmayı tercih eden müşteriler, verileri her iki ortamda da kullanılabilir hale getirmek için ortamları tümleştirmeye devam etmek zorunda kalacak.
- Müşteriler, verileri iki ortam arasında kopyalamak için Veri Tümleştiricisi kullanmaya devam edebilir. Geçiş işleminden sonra verileri tek bir ortamda birleştiren müşteriler, tüm veriler tek bir veritabanında olacağından artık verileri tümleştirmek zorunda kalmayacak.

## <a name="will-customer-isv-solutions-automatically-be-migrated"></a>Müşteri ISV çözümleri otomatik olarak geçirilecek mi?

Her bağımsız yazılım satıcısı (ISV) çözümü için geçiş deneyimi, çözümün tümleştirme yöntemine bağlı olarak değişir. Microsoft, finans ve operasyon altyapısına sorunsuz bir geçiş sağlamaya yardımcı olmak için ISV'lerle yakından çalışacak. Birçok ISV çözümü, Microsoft Power Platform özellikleri kullanılarak Dataverse üzerine kurulmuştur. Bu çözümler, Dynamics 365 Human Resources ortamı ile Dataverse ortamı arasında Dataverse entegrasyonuna bağlıdır. Dataverse tümleştirme, altyapı birleştirmenin bir parçası olarak kullanım dışıdır. Finans ve operasyon altyapısında, Dataverse tümleştirmenin işlevselliğini değiştirmek için yeni çift yazma eşlemeler planlanmaktadır.

## <a name="how-will-the-data-integrator-that-moves-data-between-dynamics-365-human-resources-and-other-dynamics-365-apps-be-affected"></a>Verileri Dynamics 365 Human Resources ve diğer Dynamics 365 uygulamaları arasında taşıyan Veri Tümleştiricisi nasıl etkilenecek?

Müşteriler finans ve operasyon altyapısına geçtikten sonra, verileri iki ortam arasında bütünleştirmeye devam etmek zorunda olacak. Müşteriler bu veri geçiş görevlerini gerçekleştirmek için Veri Tümleştiricisi kullanmaya devam edebilir. Dynamics 365 Human Resources ortamını, mevcut finans ve operasyon uygulamaları ortamından ayrı tutmayı planlayan müşteriler, verileri iki ortam arasında tümleştirmeye devam etmek zorunda kalacak. İki ortamı tek bir ortamda birleştiren müşteriler için, iki ortam arasında bütünleşme artık gerekli olmayacak.

## <a name="how-will-data-be-moved-between-dynamics-365-human-resources-on-the-finance-and-operations-infrastructure-and-dataverse-after-the-migration"></a>Veriler, finans ve operasyon altyapısında Dynamics 365 Human Resources ile geçişten sonra Dataverse arasında nasıl taşınacak?

Dynamics 365 Human Resources ile Dataverse arasındaki mevcut Dataverse entegrasyonu, finans ve operasyon altyapısının bir parçası olarak kullanımdan kaldırılır. Finans ve operasyon varlıklarını Dataverse tablolarıyla eşleştirmek için çift yazma haritaları sunma planları vardır. Müşterilerin, uygulamaları için hangi çift yazma eşleşmelerine ihtiyaç duyduklarına karar vermeleri gerekir. İş mantığını çalıştırmak için verilerin Dataverse içinde çoğaltılmasına yönelik belirli bir iş gerekmedikçe, tümleştirme ve ISV çözümleri için sanal tabloların kullanılmasını öneriyoruz.

## <a name="how-does-the-migration-affect-dataverse-extensions-for-dynamics-365-human-resources"></a>Geçiş, Dynamics 365 Human Resources için Dataverse uzantılarını nasıl etkiler?

Müşterilerin, üretim ortamını geçirmeden önce bir korumalı alan ortamına geçirilmesi gerekecek. Müşteriler korumalı alan ortamını geçirirken, yeni finans ve operasyon geçirilmiş ortamına bağlanmak için Dataverse ortamının bir kopyasını oluşturmak zorunda kalırlar. Müşterinin, mevcut üretim ortamıyla eşleşmesi için hem verileri hem de ortam için çözümleri kopyalamasını öneriyoruz.

Müşteriler, üretim Dynamics 365 Human Resources ortamlarına geçiş yapmaya hazır olduklarında, Microsoft, veritabanını ve Azure Blob depolama alanını otomatik olarak geçirir. Geçirilen veritabanı ve depolama alanı, finans ve operasyon altyapısındaki yeni ortamı, aynı üretim Dataverse ortamına yönlendirir. Verileri Dataverse'e kopyalamaya devam etmeden önce müşterilerin; Dataverse üzerinde kurulu tümleştirmeler, uzantılar ve ISV çözümleri için gerekli olan tüm ikili yazma eşlemelerini etkinleştirmeleri gerekir.

## <a name="will-microsoft-power-platform-components-that-were-built-for-dynamics-365-human-resources-automatically-work-after-the-infrastructure-migration-is-completed"></a>Altyapı geçişi tamamlandıktan sonra Dynamics 365 Human Resources için oluşturulmuş Microsoft Power Platform bileşenleri altyapıya geçiş tamamlandıktan sonra otomatik olarak çalışacak mı?

Power Apps içinde oluşturulan uygulamalar, Power Automate içinde oluşturulan akışlar ve diğer Microsoft Power Platform özelleştirmeleri Dataverse uzantıları gibidir. Müşteri üretim ortamlarının taşınması sırasında, tüm uzantılar dahil olmak üzere Dataverse ortamları üzerinde herhangi bir etki yoktur. Uygulamalar, akışlar ve diğer Power Microsoft Platformu özelleştirmeleri ek yapılandırma gerektirmeden çalışmaya devam etmelidir.

## <a name="what-will-happen-to-dataverse-virtual-table-entities-for-dynamics-365-human-resources-during-the-migration"></a>Geçiş sırasında Dynamics 365 Human Resources için Dataverse sanal tablo varlıklarına ne olacak?

Müşteriler, Dynamics 365 Human Resources ortamını finans ve operasyon altyapısına geçirdiğinde, ortam şu anda Dynamics 365 Human Resources'a bağlı olan Dataverse ortamına bağlı kalacaktır. Ortamda oluşturulmuş Dataverse sanal tabloları herhangi bir ek yapılandırma gerektirmeden çalışmaya devam edebilir. Sanal tabloların, müşterinin mevcut finans ve operasyon ortamına bağlı olan Dataverse ortamında yeniden oluşturulması gerekebilir.

## <a name="how-will-an-integration-that-uses-the-applicant-tracking-system-ats-api-payroll-api-dataverse-virtual-tables-for-dynamics-365-human-resources-or-other-entities-in-the-dataverse-web-api-work-after-the-infrastructure-merge-is-completed"></a>Altyapı birleştirme işlemi tamamlandıktan sonra, Başvuran İzleme Sistemi (ATS) API'sini, Bordro API'sini, Dynamics 365 Human Resources için Dataverse sanal tabloları veya Dataverse Web API'sindeki diğer varlıkları kullanan bir tümleştirme nasıl çalışacak?

Müşteriler, Dynamics 365 Human Resources ortamını finans ve operasyon altyapısına geçirdiğinde, ortam şu anda Dynamics 365 Human Resources'a bağlı olan Dataverse ortamına bağlı kalacaktır. Dataverse Web API'sine karşı geliştirilen tüm tümleştirmeler, geçiş işlemi tamamlandıktan sonra çalışmaya devam eder.

## <a name="our-organization-has-configured-custom-security-in-dynamics-365-human-resources-will-it-still-be-applied-after-the-infrastructure-migration-is-completed"></a>Kuruluşumuz Dynamics 365 Human Resources'ta özel güvenlik yapılandırdı. Altyapı geçişi tamamlandıktan sonra uygulanmaya devam edecek mi?

Evet, özel güvenlik yapılandırmaları veri geçişine dahil edilecektir.

## <a name="will-workflows-in-dynamics-365-human-resources-automatically-be-migrated"></a>İş akışları Dynamics 365 Human Resources'a otomatik olarak geçirilecek mi?

Evet, iş akışı yapılandırmaları, iş akışı geçmişi ve geçerli işlem içi iş akışları, birleştirilmiş altyapıya geçirilecektir.

## <a name="will-saved-views-in-dynamics-365-human-resources-automatically-be-migrated"></a>Kaydedilen görünümler Dynamics 365 Human Resources'a otomatik olarak geçirilecek mi?

Evet, kaydedilmiş görünümler birleştirilmiş altyapıya geçirilecek.

## <a name="will-features-that-are-enabled-in-dynamics-365-human-resources-automatically-be-available-after-the-infrastructure-merge"></a>Dynamics 365 Human Resources'da otomatik olarak etkinleştirilen özellikler altyapı birleşiminden sonra otomatik olarak kullanılabilir olacak mı?

- **İnsan Kaynakları** modülünü kullanan müşteriler için yalnızca Dynamics 365 Human Resources içinde bulunan özellikler, Özellik yönetimi üzerinden yönetilir. Bu özellikler genellikle varsayılan olarak etkinleştirilmez. Varsayılan olarak etkinleştirilmesi gereken tüm özellikler belgelenir.
- Dynamics 365 Human Resources kullanan müşteriler için özellikler, altyapıda yer alır. Kullanılamayan tüm özellikler belgelenir. Mevcut Dynamics 365 Human Resources ortamda etkinleştirilen her Özellik yönetim anahtarı, birleştirilmiş altyapıda etkinleştirilecek. Daha fazla bilgi için bkz. [Özellik yönetimine genel bakış](/fin-ops/get-started/feature-management-overview.md).

## <a name="what-happens-to-byod-databases-during-the-migration"></a>Geçiş sırasında KVG veritabanlarına ne olur?

Kendi veritabanınızı getirin (KVG) için içeri aktarma ve dışarı aktarma yapılandırmaları finans ve operasyon altyapısına geçirilecektir.

## <a name="is-there-an-impact-on-the-azure-region-when-the-customer-environment-is-migrated"></a>Müşteri ortamı geçirildiğinde Azure bölgesi üzerinde bir etkisi olacak mı?

Dynamics 365 Human Resources ortamı, geçiş işlemi için aynı Azure bölgesinde kalır. Bir ortamın farklı bir Azure bölgesine taşıma gereksinimi varsa müşterilerin, geçiş tamamlandıktan sonra yeni bir bölgeye geçiş yapmak için standart adımları izlemesi gerekecek.

## <a name="what-happens-to-azure-data-lakes-during-the-migration"></a>Geçiş sırasında Azure veri göllerine ne olur?

Şu anda finans ve operasyon uygulamalarında Azure Data Lake için yapılandırılan tüm dışarı aktarmalar, geçişten sonra aynı yapılandırmayı koruyacaktır.

> [!NOTE]
> Çift yazma eşleştirmelerinin, İnsan Kaynakları ortamından Dataverse'e verileri yazmaya devam etmek için etkinleştirilmesi gerekir.

İnsan Kaynakları verilerini veri gölüne aktarmak isteyen müşteriler, finans ve operasyon altyapısına geçiş tamamlandıktan sonra bu özelliği etkinleştirebilir. Daha fazla bilgi için bkz. [Veri gölleri - Azure Architecture Center](/azure/architecture/data-guide/scenarios/data-lake).

Müşteriler birden fazla finans ve operasyon ortamını aynı veri gölüne bağlayabilir. Ancak her ortam farklı bir klasörü ve bir kapsayıcıyı işaret eder. Ortamları daha sonra birleştirmeyi planlayan müşteriler, yaklaşımını dikkatle planlıyor olmalıdır.
 
## <a name="what-migration-will-be-required-if-a-customer-is-currently-using-the-human-resources-module"></a>Müşteri şu anda İnsan Kaynakları modülünü kullanıyorsa hangi geçiş yapılması gerekir?

**İnsan Kaynakları** modülünü kullanan müşteriler, Dynamics 365 Human Resources'taki yeni özellik işlevini standart Tek Sürüm güncelleme işlemi aracılığıyla kendi ortamına uygular. Her güncelleştirmede kullanılabilir hale gelirken müşteriler, ortamlarında yeni işlevselliği görmeyi bekleyebilir. Müşteriler, özelliklerini etkinleştirmek için Özellik yönetimini kullanabilir. Müşteriler, bu yeni özellikleri halihazırda sahip oldukları ve ortamlarındaki diğer güncellemeleri doğrulamak için kullandıkları süreçleri kullanarak doğrulamayı planlamalıdır.

## <a name="what-will-happen-to-custom-integrations-to-external-systems"></a>Harici sistemlere özel entegrasyonlara ne olacak?

Müşterilerin tümleştirmeleri finans ve operasyon ortamına taşımaları gerekecek. Bu ortamın uç noktası farklı olduğundan, müşteriler yeni ortama işaret eden tümleştirmeleri güncelleştirmek veya değiştirmek zorunda kalabilir. Bu görev öncelikle manuel bir işlem olacak ve gereken değişiklikler tümleştirmenin mimarisine bağlı olarak değişecektir. Müşteriler, tümleştirmeleri taşımak için en iyi yaklaşımı belirlemek üzere Microsoft iş ortaklarıyla birlikte çalışmalıdır.

## <a name="what-will-happen-to-microsoft-power-platform-dataverse-extensions-if-customers-merge-a-dynamics-365-human-resources-environment-with-an-existing-finance-and-operations-environment"></a>Müşteriler bir Dynamics 365 Human Resources ortamını mevcut bir finans ve operasyon ortamıyla birleştirirse Microsoft Power Platform (Dataverse) uzantılarına ne olur?

Müşteriler, geçişten sonra Dynamics 365 Human Resources ortamı ile mevcut finans ve operasyon ortamını tek bir Dataverse örneğinde birleştirmeye karar verirse Dataverse ortamları, birleştirme işleminin bir parçası olarak birleştirilmelidir. Bu görev, Power Apps kullanılarak oluşturulan tüm uygulamalar ve diğer tüm özelleştirmelerin yeni ortamda yeniden dağıtılmasını gerektirir.

## <a name="what-will-happen-to-documents-during-the-migration"></a>Geçiş sırasında belgelere ne olacak?

Müşteriler Dynamics 365 Human Resources ortamını finans ve operasyon altyapısına geçirdiğinde, belgeler mevcut belge depolama alanında kalacak ve finans ile operasyon altyapısındaki yeni ortamla otomatik olarak eşleştirecek.

Gelecek sürümde yeni veri varlıkları sağlanacaktır. Değişiklik yapıldıktan sonra Dynamics 365 Human Resources ortamını mevcut bir finans ve operasyon ortamıyla birleştirmeyi tercih eden müşteriler, daha sonra belgeleri dışa aktarabilir ve bunları mevcut bir ortama taşıyabilir.

## <a name="after-the-migration-what-happens-to-the-batch-jobs-that-were-configured-in-dynamics-365-human-resources"></a>Geçişten sonra, Dynamics 365 Human Resources'ta yapılandırılan toplu işlere ne olacak?

Toplu işlerin, finans ve operasyon ortamında yeniden yapılandırılması gerekecek. Müşterilerin her bir toplu işi değerlendirmeleri ve finans ve operasyon ortamındaki toplu işlerin geçerli listesiyle karşılaştırmaları gerekecek. Müşteriler toplu iş çizelgesine, önceliklere veya toplu iş gruplarına yapılması gereken değişikliklerin yapılıp yapılmadığını belirlemek için iki toplu iş kümesini birleştirirken genel toplu iş planını da analiz etmelidir.

## <a name="how-will-the-migration-affect-the-lcs-project-for-dynamics-365-human-resources"></a>Geçiş Dynamics 365 Human Resources için LCS projesini nasıl etkileyecek?

Müşteriler yeni bir Microsoft Dynamics Yaşam Döngüsü Servisi (LCS) projesi oluşturmaları ve ürün olarak finans ve operasyon uygulamalarını, proje türü olarak da **Uygulama** seçeneğini belirlemeleri gerekecek. Ek olarak, bir LCS projesi oluşturulduğunda, alt proje türü için yeni bir alan kullanılabilir. Müşterilerin, mevcut İnsan Kaynakları LCS projesini finans ve operasyon altyapısına geçirmek üzere Dynamics 365 Human Resources taşıma seçeneğini belirlemeleri gerekecek.

Finans ve operasyon LCS projelerinin özellikleri İnsan Kaynakları LCS projelerinin özelliklerinden farklıdır.

Kullanmaya başlamak için yeni müşterilerin aşağıdaki görevleri tamamlaması gerekecek:

- Proje eklemeyi tamamlayın.
- Metodolojiyi tamamlayın.
- Abonelik tahmin aracını doldurun.
- Canlı yayın başlat hazırlık işlemini tamamlayın.

## <a name="how-will-the-business-process-modeler-be-migrated"></a>İş süreci modelleyici nasıl geçirilecek?

Müşteriler, İnsan Kaynakları LCS projesinden İş süreci modelleyici kitaplığını dışa aktarmak ve bunu finans ve operasyon LCS projesine içe aktarmak için gerekli olacak. Ek olarak, müşterilerin yeni LCS projesini işaret eden uygulamadaki Yardım ayarlarını güncelleştirmeleri gerekecek.

## <a name="how-will-the-service-update-process-be-affected-by-the-migration"></a>Hizmet güncelleme süreci geçişten nasıl etkilenecek?

Geçişten sonra müşteriler uygulama yaşam döngüsü yönetimi (ALM) ve hizmet güncelleştirmeleri açısından çok daha fazla esnekliğe sahip olacak. Hizmet güncelleştirmeleri artık İnsan Kaynakları ortamlarına otomatik olarak uygulanmayacak. Bunun yerine, hizmet Tek Sürüm hizmeti güncelleştirme işlemlerini ve işlevselliğini izleyecek ve LCS ile güncelleştirmeler için yapılandırma seçenekleri etkinleştirilecek.

## <a name="will-customers-be-eligible-for-fasttrack-assistance-with-the-infrastructure-merge"></a>Müşteriler altyapı birleştirme ile ilgili FastTrack yardımına uygun olacak mı?

Microsoft, birleştirme işlemine yardımcı olmak üzere, FastTrack aracılığıyla hangi araç ve kaynakların kullanılabileceğini tanımlamaya devam ediyor.

## <a name="licensing-impact"></a>Lisanslama etkisi

Lisanslamanın nasıl etkilendiği hakkında daha fazla bilgi için bkz. [Dynamics 365 Human Resources altyapı birleştirmesi SSS](hr-infrastructure-merge-faq.md#licensing-impact).
