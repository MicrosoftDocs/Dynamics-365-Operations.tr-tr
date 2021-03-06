---
title: Human Resources'ı sağla
description: Bu konuda, Dynamics 365 Human Resources için yeni bir üretim ortam sağlama işlemi adım adım anlatılmaktadır.
author: andreabichsel
ms.date: 06/14/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SystemAdministrationWorkspaceForm
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 2632616834e405d31facdcf3853baaf96066e9aa
ms.sourcegitcommit: e6437d994c3be0c5bb4a9263af3aa8351020d83a
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/14/2021
ms.locfileid: "6248833"
---
# <a name="provision-human-resources"></a>Human Resources'ı sağla

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Bu konuda, Dynamics 365 Human Resources için yeni bir üretim ortam sağlama işlemi adım adım anlatılmaktadır. Bu konuda, İnsan Kaynaklarını bir Bulut Çözümü Sağlayıcısı (CSP) veya kurumsal mimari (EA) sözleşmesi aracılığıyla aldığınız varsayılır. Zaten insan kaynakları hizmet planını içeren mevcut bir Microsoft Dynamics 365 lisansınız varsa ve bu konudaki adımları tamamlayamıyorsanız Destek birimine başvurun.

Başlamak için, genel yöneticinin [Microsoft Dynamics Lifecycle Services](https://lcs.dynamics.com)'da oturum açması (LCS) ve yeni bir İnsan Kaynakları projesi oluşturması gerekir. İnsan Kaynaklarını sağlamanızı bir lisans sorunu engellemediği sürece, Destek biriminden veya Dynamics Hizmet Mühendisliği (DSE) temsilcilerinden yardım almanız gerekmez.

## <a name="provision-a-human-resources-trial-environment"></a>Human Resources deneme ortamı sağlama

İlk korumalı alanınızı veya üretim ortamınızı sağlamadan önce, Human Resources işlevselliğini doğrulamak için bir [Human Resources deneme ortamı](https://go.microsoft.com/fwlink/p/?LinkId=2115962) sağlamak isteyebilirsiniz. Deneme ortamları, programı güvenli bir şekilde keşfetmek için kullanılabilen hayali veriler içerir. Deneme ortamı, talep eden kullanıcıya ait olmakla birlikte, diğer kullanıcılar İnsan Kaynakları için sistem yönetimi deneyimi aracılığıyla davet edilebilir. 

Deneme ortamlarının üretim ortamı olarak kullanılmaları amaçlanmamıştır. 60 günlük deneme süresi ile sınırlıdır. Deneme süresi sona erdiğinde, ortam ve ortamdaki tüm verilerin silinir ve kurtarılamaz. Ortam bir korumalı alana veya üretim ortamına dönüştürülemez. Mevcut ortam geçersiz olduktan sonra yeni bir deneme ortamına kaydolabilirsiniz.

## <a name="plan-human-resources-environments"></a>Human Resources ortamlarını planlama

İlk Human Resources ortamınızı oluşturmadan önce, projeniz için ortam ihtiyaçlarını dikkatlice planlamalısınız. Human Resources'a temel abonelikte iki ortam bulunur: üretim ortamı ve korumalı alan ortamı. Projenizin karmaşıklığına bağlı olarak, proje etkinliklerini desteklemek için ek korumalı alan ortamları satın almanız gerekebilir. 

Ek ortamlar için dikkat edilmesi gereken noktalar şunlardır, ancak bunlarla sınırlı değildir:

- **Veri taşıma**: Korumalı alan ortamınızın proje boyunca test amacıyla kullanılmasına izin vermek için veri taşıma etkinlikleri için ek bir ortam düşünmeniz gerekebilir. Ek bir ortama sahip olduğunuzda, test ve yapılandırma etkinlikleri aynı anda farklı bir ortamda gerçekleşirken veri geçişleri etkinliklerinin devam etmesine olanak tanır.
- **Tümleştirme**: Tümleştirmeleri yapılandırmak ve test etmek için ek bir ortam düşünmeniz gerekebilir. Bu, Ceridian Dayforce LinkedIn Talent Hub tümleştirmeleri gibi yerel tümleştirmeleri veya bordro, başvuran izleme sistemleri veya yan hak sistemleri ve sağlayıcıları gibi özel tümleştirmeleri içerebilir.
- **Eğitim**: Çalışanlarınızı yeni sistemin kullanımı konusunda eğitmek için bir dizi eğitim verisiyle yapılandırılmış ayrı bir ortama ihtiyacınız olabilir. 
- **Çok aşamalı proje**: Projenin ilk yayınlanmasından sonra planlanan bir proje aşamasında yapılandırmayı, veri geçişini, testi veya diğer etkinlikleri desteklemek için ek bir ortama ihtiyacınız olabilir.

 > [!IMPORTANT]
 > GOLD yapılandırma ortamınız olarak projeniz boyunca üretim ortamınızı kullanmanızı öneririz. Korumalı alan ortamını üretim ortamına kopyalayamadığınızdan, bu önemlidir. Bu nedenle, yayına aldığınızda GOLD ortamınız üretim ortamınızdır ve bu ortamda kesin bitiş faaliyetlerinizi tamamlayacaksınız.</br></br>
 > Yayınlamadan önce sahte bir kesin bitiş gerçekleştirmek için korumalı alanınızı veya başka bir ortamı kullanmanızı öneririz. Bunu, GOLD yapılandırmanızın olduğu üretim ortamını korumalı alan ortamınıza yenileyerek yapabilirsiniz.</br></br>
 > Yayınlama işlemi sırasında son verileri üretim ortamına geçirmek için gereken veri paketlerinin her birini içeren ayrıntılı bir kesin bitiş denetim listesi tutmanızı öneririz.</br></br>
 > Ayrıca, TEST ortamınız olarak projeniz boyunca korumalı alan ortamınızı kullanmanızı öneririz. Ek ortamlara ihtiyacınız olursa kuruluşunuz bunları ek bir ücret karşılığında satın alabilir.</br></br>

## <a name="create-an-lcs-project"></a>LCS projesi oluşturma

İnsan Kaynakları ortamlarınızı yönetmek üzere LCS'yi kullanmak için öncelikle bir LCS projesi oluşturmanız gerekir.

1. İnsan Kaynaklarına abone olmak için kullandığınız hesabı kullanarak [LCS](https://lcs.dynamics.com/Logon/Index)'de oturum açın.

   > [!NOTE]
   > Sağlamanın başarılı olmasını sağlamak için, Human Resources ortamını sağlamak için kullandığınız hesap, Human Resources ortamıyla ilişkilendirilmiş Power Apps ortamındaki **Sistem Yöneticisi** veya **Sistem Özelleştirici** rolüne atanmalıdır. Power Platform'da kullanıcılara güvenlik rolleri atama hakkında daha fazla bilgi edinmek için bkz. [Kaynaklara kullanıcı güvenliği yapılandırma](/power-platform/admin/database-security).

2. Yeni bir proje oluşturmak için artı işaretini (**+**) seçin.

3. Ürün adı ve ürün sürümü olarak **Microsoft Dynamics 365 Human Resources**'ı seçin.

4. **Dynamics 365 Human Resources** metodolojisini seçin.

5. **Oluştur**'u seçin.

İnsan Kaynaklarını kullanmaya başlamayla ilgili bilgiler için yeni projede oluşturduğunuz **İnsan Kaynakları** metodolojisine bakın. Projeyi oluşturmayı tamamladıktan sonra, İnsan Kaynakları ortamınızı sağlamak için aşağıdaki yordamı tamamlayın.

## <a name="provision-a-human-resources-project"></a>İnsan kaynakları projesi hazırlığı

Bir LCS projesi oluşturduktan sonra, bir ortama İnsan Kaynakları sağlayabilirsiniz.

1. LCS projenizde **İnsan Kaynakları Uygulama Yöneticisi** kutucuğunu seçin.

2. Bu ortamın bir Korumalı Alan örneği mi yoksa Human Resources Üretim örneği mi olduğunu belirtin. Erken geri bildirim ve sınamaya izin vermek için korumalı alan örneklerinde önceki Önizleme özellikleri kullanılabilir olabilir.
   
    > [!NOTE]
    > Human Resources örneği türü ayarlandıktan sonra değiştirilemez. Devam etmeden önce doğru örnek türünün seçilmiş olduğundan emin olun.</br></br>
    > İnsan Kaynakları örnek türü, Power Apps Yönetim Merkezi'nde ayarladığınız Microsoft Power Apps ortamının örnek türünden ayrıdır.
    
3. Ortamınızın İnsan Kaynakları Test Sürümü deneyiminde kullanılan aynı tanıtım verileri kümesini içermesini istiyorsanız **Tanıtım Verilerini Ekle** seçeneğini seçin. Demo verileri uzun vadeli tanıtım veya eğitim ortamları için yararlıdır ve üretim ortamları için hiçbir zaman kullanılmamalıdır. İlk dağıtım sırasında bu seçeneği seçmeniz gerekir. Var olan bir dağıtımı sonra güncelleştiremezsiniz.

4. İnsan Kaynakları, Power Apps tümleştirmesi ve genişletilebilirliği sağlamak amacıyla daima bir Microsoft Power Apps ortamında sağlanır. Devam etmeden önce bu konudaki "Power Apps ortamı seçme" bölümünü okuyun. Power Apps ortamınız yoksa, LCS'de Ortamları yöneti seçin veya Power Apps Yönetim Merkezi'ne gidin. Ardından [Power Apps ortamı oluşturma](/powerapps/administrator/create-environment) adımlarını izleyin.

5. İnsan Kaynakları'nın tedarik edileceği ortamı seçin.

6. Koşulları kabul etmek için **Evet**'i seçin ve dağıtıma başlayın.

   Yeni ortamınız, soldaki gezinti bölmesinde bulunan ortam listesinde görüntülenir. Bununla birlikte, dağıtım durumunu **Dağıtıldı** olarak güncelleştirilene kadar ortamı kullanmaya başlayamazsınız. Tipik olarak bu işlem birkaç dakika sürebilir. Sağlama işlemi başarısız olursa Desteğe başvurmanız gerekir.

7. Yeni ortamı kullanmak için **Human Resources'ta oturum aç**'ı seçin.

    > [!NOTE]
    > Son gereksinimleri henüz yerine getirmediyseniz, projede İnsan Kaynakları'nın bir test kurulumunu dağıtabilirsiniz. Ardından imzalayana kadar bu kurulumu kullanarak çözümünüzü test edebilirsiniz. Yeni ortamınızı test için kullanıyorsanız, bir üretim ortamı oluşturmak için bu yordamı yinelemeniz gerekir.

## <a name="select-a-power-apps-environment"></a>Bir Power Apps ortamı seçin

Human Resources veri kullanımını, Power Apps araçlarını kullanarak tümleştirebilir ve genişletebilirsiniz. Power Apps ortamları hakkında ortamın kapsamı, ortama erişim ile ortam oluşturma ve seçme de dahil olmak üzere bilgi edinmek için bkz. [Power Apps ortamları duyurusu](https://powerapps.microsoft.com/blog/powerapps-environments/). 

İnsan Kaynakları'nı hangi Power Apps ortamına dağıtacağınızı belirlerken aşağıdaki yönergeleri kullanın: 

1. LCS'de **Ortamları yönet**'i seçin. Ayrıca, mevcut ortamları görebileceğiniz ve yeni ortamlar oluşturabileceğiniz Power Apps Yönetim merkezine doğrudan gidebilirsiniz.

2. Tek bir Power Apps ortamına tek bir İnsan Kaynakları ortamı eşlenir.

3. Power Apps ortamı ilgili Power Apps, Power Automate ve Dataverse uygulamalarının yanı sıra İnsan Kaynakları'nı içerir. Power Apps ortamı silinirse, içerdiği uygulamalar da silinir. Bir İnsan Kaynakları ortamı sağlanırken, bir **Denem** veya **Üretim** ortamı sağlayabilirsiniz. Ortamın nasıl kullanılacağına göre ortam türünü seçin. 

4. Veri tümleştirme ve test stratejileri göz önünde bulundurmalıdır: örneğin Korumalı alan, UAT veya Üretim. Human Resources ortamının eşlendiği Power Apps ortamını daha sonra değiştirmek kolay olmayacağından, dağıtımınızla ilgili çeşitli etkileri dikkatlice değerlendirin.

5. Human Resources için aşağıdaki Power Apps ortamlarını kullanamazsınız. Bunlar LCS içindeki seçim listesinden filtrelenmiştir:
 
    - **Varsayılan Power Apps ortamları** - Her kiracıya otomatik olarak varsayılan Power Apps ortamı sağlanmakla birlikte, bu ortamları Humans Resources ile kullanmanızı önermeyiz. Tüm kiracı kullanıcıları Power Apps ortamına erişebilir ve Power Apps veya Power Automate tümleştirmelerini test ederken veya keşfederken üretim verilerini istemeden bozabilir.
   
    - **Deneme ortamları** - Bu ortamlar bir sona erme tarihiyle oluşturulur. Kullanım süresi sona erdiğinde, ortamınız ve bunun içinde bulunan tüm Human Resources örnekleri otomatik olarak kaldırılır.
   
    - **Desteklenmeyen coğrafyalar** - Ortam, desteklenen bir coğrafyada olmalıdır. Daha fazla bilgi için bkz. [Desteklenen coğrafyalar](hr-admin-setup-provision.md#supported-geographies).

6. Kullanılacak doğru ortamı belirledikten sonra, sağlama işlemine devam edebilirsiniz. 

### <a name="supported-geographies"></a>Desteklenen coğrafyalar

Human Resources şu anda aşağıdaki coğrafyaları desteklemektedir:

- Amerika Birleşik Devletleri
- Avrupa
- Birleşik Krallık
- Avustralya
- Kanada
- Asya 

Bir Human Resources ortamı oluşturduğunuzda, Human Resources ortamıyla ilişkilendirilecek bir Power Apps ortamı seçersiniz. Daha sonra, Human Resources ortamı seçili Power Apps ortamı ile aynı Azure coğrafyasında sağlanır. Human Resources ortamıyla ilişkilendirilecek Power Apps ortamını oluştururken coğrafyayı seçerek Human Resources ortamı ve veritabanının fiziksel olarak nerede yer alacağınızı seçebilirsiniz.

Ortamın sağlanacağı Azure *coğrafyasını* seçebilirsiniz ancak Azure *bölgesini* tam olarak seçemezsiniz. Otomasyon, yük dengelemeyi ve performansı iyileştirmek için ortamın oluşturulduğu coğrafya içindeki bölgeyi belirler. Azure coğrafyaları ve bölgeleri hakkında bilgi edinmek için [Azure coğrafyaları](https://azure.microsoft.com/global-infrastructure/geographies) belgelerini inceleyebilirsiniz.

Human Resources ortamı verileri her zaman oluşturulduğu Azure coğrafyasında tutulur. Ancak, her zaman aynı Azure bölgesi içinde tutulmaz. Olağanüstü durum kurtarma amacıyla, veriler hem birincil Azure bölgesinde hem de coğrafya içinde ikincil bir yük devretme bölgesinde çoğaltılacaktır.

 > [!NOTE]
 > Human Resources ortamının başka bir Azure bölgesine geçirilmesi desteklenmez.

## <a name="grant-access-to-the-environment"></a>Ortama erişim izni verme

Varsayılan olarak, ortamı oluşturan genel yöneticinin ortama erişimi vardır. Ek uygulama kullanıcılarına erişim izninin açıkça verilmesi gerekir. Human Resources ortamında kullanıcılar eklemeniz ve kullanıcılara uygun roller atamanız gerekir. İnsan Kaynakları'nı dağıtan genel yönetici, başlatmayı tamamlamak ve diğer kiracı kullanıcılar için erişim sağlamak üzere Attract ve Onboard'ı da başlatmalıdır. Bu gerçekleştirilene kadar, diğer kullanıcılar Attract ve Onboard'a erişemez ve erişim ihlali hataları alır. Daha fazla bilgi için bkz. [Yeni kullanıcılar oluşturmak](/dynamics365/unified-operations/dev-itpro/sysadmin/tasks/create-new-users) ve [Kullanıcıları güvenlik rollerine atamak](/dynamics365/unified-operations/dev-itpro/sysadmin/tasks/assign-users-security-roles). 


[!INCLUDE[footer-include](../includes/footer-banner.md)]
