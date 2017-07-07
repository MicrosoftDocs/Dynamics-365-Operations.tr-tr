---
title: "Dynamics AX 2012&quot;yi Microsoft Dynamics 365 for Finance and Operations, Enterprise sürümüne yükseltme"
description: "Bu konuda, şu anda Microsoft Dynamics AX 2012 çalıştıran müşterilerin verilerini ve kodlarını Microsoft Dynamics 365 for Finance and Operations, Enterprise sürümüne taşımak için kullanabilecekleri işlem açıklanmaktadır."
author: tariqbell
manager: AnnBe
ms.date: 06/16/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Developer, IT Pro
ms.reviewer: margoc
ms.search.scope: Operations Platform
ms.search.region: Global
ms.author: tabell
ms.search.validFrom: 2017-06-16
ms.dyn365.ops.version: Platform update 8
ms.translationtype: Human Translation
ms.sourcegitcommit: 6816e3820ab77c71bbf9bde4a068375448331671
ms.openlocfilehash: 13507fcf9c0d626709aeb4e00a8632411204c20f
ms.contentlocale: tr-tr
ms.lasthandoff: 06/15/2017

---

# <a name="upgrade-microsoft-dynamics-ax-2012-to-microsoft-dynamics-365-for-finance-and-operations-enterprise-edition"></a>Microsoft Dynamics AX 2012'yi Microsoft Dynamics 365 for Finance and Operations, Enterprise sürümüne yükseltme

[!include[banner](../includes/banner.md)]

Microsoft Dynamics 365 for Finance and Operations, Enterprise sürümü, platform güncelleştirmesi 8'de şu anda Microsoft Dynamics AX 2012 kullanan müşterilerin verilerini ve kodlarını Finance and Operations'a taşımak için kullanabilecekleri bir yükseltme yolu sunulmaktadır. Yükseltme işlemi aşağıdaki öğeler üzerinde oluşturulur:

- Varolan özel uygulama kodunu AX 2012'den taşımaya yardımcı olan araçlar.
- Veritabanınızı iletmek için kullanabileceğiniz veri yükseltme işlemi. Böylece, tüm hareket geçmişinizi yükseltebilirsiniz.

## <a name="overview"></a>Özet

Tüm yükseltme işlemi üç ilişkili aşama halinde görselleştirilebilir: Analiz, Yürütme ve Doğrulama.

Aşağıdaki şemada uçtan uça yükseltme işlemi ve her aşama için dikkate alınması gereken faaliyetler gösterilmektedir. 

![Yükseltme işlemi](./media/upgrade-process.png)

## <a name="analyze"></a>Analiz yap

Analiz aşamasındaki faaliyetler yükseltmek için gereken çabayı tahmin etmenize yardımcı olur. Ayrıca, proje planı hazırlamanıza yardımcı olur. Bu faaliyetleri Finance and Operations'ı satın almadan önce gerçekleştirebilirsiniz. Bunlar, gerekli olacak çaba ve kaynaklar hakkında bir veri noktası sağlayarak bilgiye dayalı satın alma kararı vermenize yardımcı olur.

### <a name="sign-up-for-a-public-preview-in-lcs"></a>LCS'de genel önizleme için kaydolma

Finance and Operations'ı satın almadan Analiz faaliyetlerini gerçekleştirmek için genel önizlemeye kaydolabilirsiniz. Genel önizleme kendi Finance and Operations ortamlarınızı dağıtma olanağı sunar. Ayrıca, Microsoft Dynamics Lifecycle Services'daki (LCS), AX 2012 ortamınızı ve mevcut özel kodunuzu değerlendirmek için kullanılan araçlara da erişmenizi sağlar.

AX 2012 için mevcut bir LCS projeniz olsa da Finance and Operations'ı değerlendirmek üzere yeni bir proje için kaydolmanız gerekir.

Müşteriler için genel önizlemeyi nasıl edineceğinize ilişkin bilgi için bkz. https://mbs.microsoft.com/customersource/global/AX/news-events/news/Microsoft_Dynamics_AX_Public_Preview.

İş ortakları için genel önizlemeyi nasıl edineceğinize ilişkin bilgi için bkz. https://mbs.microsoft.com/partnersource/global/news-events/news/Microsoft_Dynamics_AX_Public_Preview.

Bu genel önizlemenin [30 günlük denemeden](https://aka.ms/D365OperationTrials) farklı olduğunu unutmayın. Otuz günlük deneme, uygulamayı keşfetmek ve değerlendirmek için kullanabileceğiniz dağıtılmış bir Finance and Operations kurulumu sağlar. Ancak, Analiz faaliyetleri tam LCS deneyimi ve araçları gerektirir.

### <a name="select-the-upgrade-methodology"></a>Yükseltme meotodolojisini seçme
Yeni LCS projenizde, proje metodolojisini **Dynamics AX 2012'yi Dynamics 365 for Operations'a Yükselt** olarak ayarlayın. Bu metodoloji yükseltme yapan AX 2012 müşterileri için özel olarak yapılmıştır. Üç aşamayı ayrıntılı biçimde açıklar ve işlemle ilgili tüm destekleyici belgelere bağlantı sağlar.

![Yüksetlem metodolojisi(./media/methodology.png)
 
### <a name="run-the-upgrade-analyzer"></a>Yükseltme analiz aracını çalıştırma
Yükseltme analizi aracı AX 2012 ortamınızda çalışır ve yükseltme işleminin daha sorunsuz ve saha uygun maliyetli olmasına yardımcı olmak amacıyla AX 2012 ortamını hazırlamak için yapmanız gereken görevleri tanımlar.

- **Veri temizleme** – Bu işlem işlevselliğin kaybolmasına neden olmadan kaldırabileceğiniz verileri belirlemenize yardımcı olur. Bu araç bir temizleme işlemi çalıştırarak azaltabileceğiniz çeşitli veri türlerini tanımlar. Her veri türü için, temizlemenin etkisi hakkında bir açıklama verilmiştir. Daha sonra, temizleme işlemini çalıştırıp çalıştırmayacağınıza karar verirsiniz. Finance and Operations aboneliğinizin maliyet bölümü veritabanı boyutuna bağlıdır. Bu nedenle, boyutunu azaltarak, bu bileşenin abonelik maliyetini azaltabilir ve yükseltme işlemi için gerekli süreyi kısaltmaya yardımcı olabilirsiniz. Daha küçük bir veritabanı daha hızlı yükseltme yapılmasına yardımcı olur.
- **SQL yapılandırması** – Bu işlem SQL yapılandırmasını gözden geçirir ve optimizasyon önerilerinde bulunur. SQL'in en iyi şekilde çalıştığından emin olmanızı sağlayan bu işlem, yükseltme işleminin servise alınması için gereken sürenin kısaltılmasına yardımcı olur.
- **Kaldırılan özellikler** – Bu işlem, şu anda kullanmakta olduğunuz, ancak Finance and Operations'da kullanılabilir olmayan özellikleri tanımlar. Bu nedenle, işlem işlev eksikliklerini erken keşfetmenize yardımcı olur. Ayrıca, alternatifler için öneriler de sağlar.

Buna ek olarak, bu adımın bir parçası olarak, AX 2012 ortamında KBXXXXXXX yüklemeniz gerekir. Bu düzeltme yükseltme öncesi denetim listesi sağlar. AX 2012 ortamında, bu denetim listesini yükseltme yordamı için gerekli olacak verileri girmek için kullanabilirsiniz. Örneğin, bir yükseltme öncesi denetim listesi görevinde, geçerli her AX 2012 kullanıcısı için Microsoft Azure Active Directory (Azure AD) oturum açma bilgileri sağlarsınız, böylece her kullanıcı Finance and Operations'da oturum açabilir.

Bu adımın çıkışı AX 2012 sistem yöneticileriniz için yükseltme proje planındaki iş akışı olur.

Daha fazla bilgi için bkz. [Analiz: Geçiş işini planlamak için yükseltme analiz aracını kullanın](upgrade-analyzer-tool.md).

### <a name="run-the-code-upgrade-estimation-tools"></a>Kod yükseltme tahmini araçlarını çalıştırma
Bu adım AX 2012'den kodunuzu alır, yeni biçime dönüştürür ve bir geliştiricinin daha sonra çözmesi gereken çakışmalar hakkında geri bildirim sağlar. Bu adım, kod yükseltmenizin maliyet tahmini için temel oluşturur.

Bu adımı tamamlamak için, kodunuzu AX 2012'den model deposu olarak dışa aktarmanız ve aracı yükseltmek için bunu LCS'ye yüklemeniz gerekir. Kod yükseltme aracı kodunuzun yükseltilmiş sürümünü ve çözümlenmesi gereken çakışmalarla ilgili bir rapor oluşturur. Geliştiriciniz, hem yükseltilen kodu hem de raporu inceleyerek kod tabanınızı yükseltmek için gerekli olacak çabayı belirleyebilir.

Bu adımın çıkışı Microsoft Dynamics AX geliştiricileriniz için yükseltme proje planındaki iş akışını temsil eder.

Daha fazla bilgi için bkz. [Analiz: Kod yükseltme için gereken çabayı tahmin etme](analyze-code-upgrade.md).

### <a name="deploy-a-demo-environment"></a>Tanıtım ortamını dağıtma
Tanıtım ortamları, tanıtım amaçlı veriler (sizin verilerinizi değil) ve standart kod (özelleştirme olmadan) içeren varsayılan ortamlardır. Yeni özellikleri değerlendirmek için bir tanıtım ortamı dağıtmanızı ve AX 2012 içinde kullanılan ancak Finance and Operations'da değişmiş olabilecek standart işlemler için temel boşluk analizi gerçekleştirmenizi öneririz. Bu tanıtım ortamlarını Azure'da dağıtabilir veya kendi donanımınızda çalışan bir sanal makine (VM) olarak indirebilirsiniz. Azure içinde dağıtım yaparsanız, hala bir genel önizleme projesi kullanıyor olduğunuzdan ve henüz Finance and Operations aboneliği satın almadığınızdan Azure aboneliğinizi vermeniz gerekir.

Bu adımın çıkışı işlevsel kullanıcılarınız veya kurumsal kullanıcılarınız için yükseltme proje planındaki iş akışını temsil eder.

Daha fazla bilgi için bkz. [Analiz: Korumalı alan ortamı dağıtma](analysis-sandbox.md)

### <a name="create-a-project-plan"></a>Proje planı oluşturma
Yükseltme metodololjisinde proje planı için bir şablon verilir. Bu adımda, Analiz aşamasındaki önceki adımların sonucu yükseltme projesi için proje planını doldurmak üzere kullanılır. Proje planı ayrıca tüm test ayrıntılarını da içerir: veri yükseltme testi, kesin bitiş testi, işlev testi geçiş tekrarları ve bu görevler için çeşitli kaynak atamalarına ilişkin ayrıntılar.

Bu aşamada, proje planı Finance and Operations'a yükseltme yapmak için gerekli olan süreyi ve maliyeti anlamanıza yardımcı olabilecek bir veri noktası sunar.

## <a name="execute"></a>Yürüt
Yürütme aşaması sırasında, Analiz aşamasında planladığınız görevleri uygularsınız. Yürütme aşamasına geçmek için, Finance and Operations'ı satın almanız ve yükseltme işleminde çalışabilecek kaynaklara sahip olmanız gerekir.

### <a name="switch-to-the-lcs-implementation-project"></a>LCS uygulama projesine geçme
Analiz aşamasında kullandığınız genel önizleme projesi amacına uygun şekilde hizmet verdi. Artık bunu atabilirsiniz. Kalan adımlar için, yalnızca Analiz aşamasının son adımında oluşturduğunuz proje planına ihtiyacınız olacaktır.

Finance and Operations aboneliği satın aldığınızda, yeni bir LCS projesi için kaydolma hakkında ayrıntılı bilgi alırsınız. Bu proje bir uygulama projesi olarak bilinir ve bu aboneliğe sahip olduğunuz sürece, aboneliğiniz için yeni kalıcı LCS projesi olacaktır. Bu proje, Microsoft tarafından yönetilen genel önizleme projesinden farklıdır. Bu nedenle, bu proje şu özelliklere sahiptir:

- Projedeki tüm ortamlar Azure'da barındırılır.
- Projeyle ilişkili Azure aboneliği Microsoft tarafından yönetilir. Bu nedenle, Azure maliyetleri için ayrı bir faturalama yapılmaz. Maliyetler Finance and Operations aboneliğiniz kapsamındadır.
- Projedeki üretim ortamı Microsoft tarafından sürdürülür. Bu nedenle kod dağıtımları, yükseltme ve altyapı bakımı sizin personeliniz tarafından değil doğrudan Microsoft tarafından çalıştırılır. 

### <a name="perform-the-ax-2012-preparation-tasks"></a>AX 2012 hazırlık görevlerini gerçekleştirme
Yükseltme analiz aracının keşfettiği ve yükseltme proje planında belgelenen görevleri tamamlayın. Bu görevler veritabanı yöneticisi (DBA) ve Microsoft Dynamics AX Sistem Yöneticisi tarafından tamamlanmalıdır.

[AX 2012'den Dynamics 365 for Operations'a veri yükseltme - AX 2012'de yükseltme öncesi denetim listesi](prepare-data-upgrade.md)

### <a name="perform-code-upgrade"></a>Kod yükseltmesini gerçekleştirme
Analiz aşamasının kod yükseltme tahmini adımında planlanan görevleri tamamlayın. Bu görevleri geliştiricilerinizin çalıştırması gerekir.

Bu noktadan itibaren, AX 2012 kod değişiklikleri dondurulmuş olmalıdır. AX 2012 içinde yalnızca acil kod değişikliklerine izin verilmelidir. Bir değişiklik yapılırsa, bu el ile yeni kod tabanına eklenmelidir.

### <a name="develop-new-code"></a>Yeni kod geliştirme
Analiz aşamasının "bir tanıtım ortamı dağıtın" aşamasında gerçekleştirilen uygun boşluk analizindeki görevleri tamamlayın. Bu görevler büyük olasılıkla yapılandırmayı tanımlayan işlev görevleri ile alınacak yeni özelliklerle ilgili özelleştirmelere ilişkin geliştirme testlerinin bir bileşimi olacaktır.

### <a name="data-upgrade-development-environment"></a>Veri yükseltme (geliştirme ortamı)
Kod yükseltme görevleri tamamlandıktan sonra, AX 2012 veritabanınızı ilk olarak Finance and Operations'a yükseltebilirsiniz. Bu ilk yükseltme geliştirme ortamında gerçekleşir, böylece bu aşamada bulunan sorunları daha kolay giderebilir veya ayıklayabilirsiniz. Geliştirme ortamında, bir sorun için anında hata ayıklama işlemi yapılabilir, kod ayarlanabilir ve yükseltme dakikalar içinde yeniden çalıştırılabilir. Daha geniş korumalı alan ortamları bu cevikliği sunmaz ve hata ayıklama ve sorunları giderme, kodu güncelleştirme, güncelleştirilen kodun dağıtma ve yükseltmeyi yeniden çalıştırma için en az birkaç saat gerekir.

Aşağıdaki çizimde işlem gösterilmiştir. AX 2012 veritabanı yedeklemeniz, Azure'a yüklemeniz, Finance and Operations ortamına geri yüklemeniz ve veri yükseltmeyi çalıştırmanız yeterli.

![Geliştirme ortamında veri yükseltme](./media/data-upgrade-dev.png)
 
Veri yükseltme belirli türdeki bir dağıtılabilir paketle yapılır. Aynı mekanizma yeni Finance and Operations kodunu bir ortamdan başka bir ortama dağıtmak için kullanılır.

Bu işlem sırasında veritabanındaki verileri dönüştürmek için kullanılan temel çerçeve büyük ölçüde AX 2012'deki **ReleaseUpdatexxx** sınıflarını çalıştıran X ++ toplu işleri temel alan yükseltme çerçevesiyle aynıdır.

Ayrıntılı bilgi için bkz [Geliştirme ortamına AX 2012'den Dynamics 365 for Operations'a veri yükseltme](data-upgrade-2012.md).

### <a name="data-upgrade-sandbox-environments"></a>Veri yükseltme (korumalı alan ortamları)
Geliştirme ortamında bir veri yükseltme işlemi tamamlandığında, aynı işlem korumalı alan ortamında da çalıştırılabilir. Korumalı alan ortamı iş kullanıcılarının ve işlevsel ekip üyelerinin iş süreçlerini yükseltilen AX 2012 verilerini ve kodunu kullanarak test edebilecekleri ortamdır.

Aşağıdaki şekilde korumalı alan ortamında veri yükseltmesi çalıştırma işlemi gösterilmektedir. Burada fark geleneksel SQL yedekleme yerine bacpac aracı kullanılmasıdır. Bu araç Microsoft SQL Server ile Azure SQL Veritabanı arasında dönüştürme için gereklidir. Standart bir SQL aracıdır ve Finance and Operations'a özel değildir.

![Korumalı alan ortamında veri yükseltme](./media/data-upgrade-sandbox.png)

Ayrıntılı bilgi için bkz [Korumalı alan ortamına AX 2012'den Dynamics 365 for Operations'a veri yükseltme](upgrade-data-sandbox.md).
 
## <a name="validate"></a>Doğrula
Doğrulama aşamasına girdiğinizde, yükseltilen özel kod ve yükseltilmiş verilerinizi içeren kullanılabilir ortamlar olacaktır. Bu aşama yükseltilen ortamın istediğiniz şekilde çalıştığını test etme ve doğrulama sürecini açıklar. Ayrıca servise alma için hazırlık işlemini açıklar.

### <a name="perform-cutover-testing-and-create-a-cutover-plan"></a>Kesin bitiş testini gerçekleştirir ve kesin bitiş planı oluşturur
_Kesin bitiş_ terimi burada yeni sistemi kullanıma almak için gerekli son işlemi ifade eder. Bu işlem AX 2012 kapatıldıktan sonra ve Finance and Operations açılmadan önce gerçekleşen görevlerden oluşur. 

Testin amacı kesin bitiş işlemiyle ilgili uygulama yapmaktır. Bu şekilde, servise alma için gerçek kesin bitiş işlemine katılan herkesin sorunsuz bir deneyim yaşamasını garanti edersiniz.

İki ana iş akışı vardır:

- **Teknik iş akışı** – Bu iş akışı veri yükseltmeyi çalıştırma işlemidir. İşletmeniz izin verilen kesinti süresi miktarı üzerinde bir sınır uygular. Bu kesinti sırasında, ne AX 2012 ne de Finance and Operations kullanılabilir olmaz. Teknik iş akışının, işletmenin kesinti süresi sınırını karşılamak amacıyla veri yükseltme yordamına performans ayarı yapması gerekebilir. 
- **İşlevsel iş akışı** – Veri yükseltme işleminden sonra, Finance and Operations ortamında çeşitli yapılandırma görevleri gerçekleştirilmesi gerekir. Bu görevlerin tümü belgelenmeli ve sayısal ölçümleri yapılmalıdır, görevlerin iş kesinti süresi sınırı içindeki teknik görevlere uygun olması gerektiğinden görevlere bir kaynak atanması gerekir.

Ayrıntılı bilgi için bkz. 
- [Doğrulama: Kesin bitiş testi](upgrade-cutover-testing.md)
- [Doğrulama: Uygulama doğrulama işlemi](app-validation-process.md)

### <a name="functional-test-pass"></a>İşlev testi geçişi
Tüm iş süreçleri için bir tam işlevsel test geçişi tamamlayın. Bu test geçişi Finance and Operations'a dahil olan tüm iş süreçleri için kapsamlı bir yeniden test olacaktır. Bu iş süreçleri AX 2012'den taşınan eski işlemleri hem de Finance and Operations'da ilk defa alınan yeni özellikleri içeren yeni işlemleri içerir. 

Kod kalitesine bağlı olarak, sorunu düzeltme ve yeniden test işlevsel test geçişinin birkaç kez tekrarlanmasını gerektirebilir. Bir sorun düzeltildiğinde, yukarı alış ve aşağı akış sürecinin değişiklikten etkilenmemesini sağlamaya yardımcı olması için tüm işlemlerin yeniden test edildiğinden emin olun.

Ayrıntılı bilgi için bkz. [Doğrulama: İşlevsel test](upgrade-functional-validation.md).

### <a name="pre-go-live-checklist"></a>Servise alma öncesi denetim listesi
Servise alma öncesi denetim listesi, servise alma işleminden önceki son kesin bitiş sırasında hata olasılığını azaltmaya yardımcı olan ve önerilen bir yordamdır. Servise almadan bir hafta önce, AX 2012'de yapılandırma değişikliklerini durdurun (\<modül\>\Kurulum altından). Bu yapılandırma değişikliği kısıtlaması yalnızca yordam kısıtlamasıdır. Microsoft Dynamics AX sistem yöneticileri bu noktada bu tür değişikliklerin bekletilmesi gerektiğine katılmaktadır.

Finance and Operations kod tabanındaki kod değişikliklerini de dondurmanız önerilir. Değerlendirilmedikçe ve servise alma işlemini engellemeyecekleri belirlenmedikçe değişiklik yapılmasına izin verilmemelidir.  

Yapılandırma kısıtlaması ve kod dondurma gerçekleştirildikten sonra, veri yükseltmenin kesin bitiş öncesinde son bir kez çalıştırılması gerekir. Bu şekilde, her şeyin beklendiği gibi çalışmaya devam ettiğinden emin olabilirsiniz. 

Ayrıntılar için bkz. [Doğrulama: Servise alma için hazırlanma](upgrade-go-live-prep.md)



### <a name="supported-upgrade-paths"></a>Desteklenen yükseltme yolları
Haziran 2017 itibariyle, Microsoft Dynamics 365 Finance and Operations, Enterprise Edition, 0617 sürümüne yükseltme Microsoft Dynamics AX 2012 R3 tarafından desteklenir. Tüm toplu AX 2012 R3 güncelleştirmeleri (CU'lar) desteklenir.

Microsoft Dynamics AX 2012 R2 ve Microsoft Dynamics AX 2012 RTM şu anda desteklenmemektedir. 2017 desteği daha sonra eklenecektir.

Yalnızca Finance and Operations'ın bulutta dağıtılan sürümüne yükseltme desteklenir. Şirket içi sürümüne yükseltme desteklenmez. Şirket içi sürümü için yükseltme desteği 2017 içinde daha sonra 2017 eklenecektir.

