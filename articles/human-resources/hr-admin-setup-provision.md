---
title: Human Resources'ı sağla
description: Bu makalede, Microsoft Dynamics 365 Human Resources için yeni bir üretim ortamı hazırlama işlemi açıklanmaktadır.
author: twheeloc
ms.date: 01/07/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SystemAdministrationWorkspaceForm
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 6fc44b52e2f7662fc6be609562cec903a8755d1b
ms.sourcegitcommit: 1401d66b6b64c590ca1f8f339d622e922920cf15
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/20/2022
ms.locfileid: "9178518"
---
# <a name="provision-human-resources"></a>Human Resources'ı sağla

_**Uygulandığı Öğe** tek başına çalışan altyapıda İnsan Kaynakları_ 

> [!NOTE]
> Haziran 2022'den başlayarak İnsan Kaynakları ortamları yalnızca finans ve operasyon uygulama altyapısı üzerinden dağıtılabilir. Daha fazla bilgi için bkz. [Finans ve operasyon altyapısında İnsan Kaynakları sağlama](hr-admin-setup-provision-fo.md).

Bu makalede, Microsoft Dynamics 365 Human Resources için yeni bir üretim ortamı hazırlama işlemi açıklanmaktadır. 

## <a name="prerequisites"></a>Önkoşullar

Yeni bir üretim ortamını hazırlamaya başlayabilmeniz için aşağıdaki önkoşulların yerine getirilmiş olması gerekir:

- Human Resources'ı bir Bulut Çözümü Sağlayıcısı (CSP) veya kurumsal mimari (EA) sözleşmesi aracılığıyla satın almış olmalısınız. Zaten insan kaynakları hizmet planını içeren mevcut bir Microsoft Dynamics 365 lisansınız varsa ve bu konudaki adımları tamamlayamıyorsanız Destek birimine başvurun.

- Genel yönetici, [Microsoft Dynamics Lifecycle Services](https://lcs.dynamics.com) (LCS) hizmetinde oturum açmış ve yeni bir Human Resources projesi oluşturmuş olmalıdır. 

## <a name="provision-a-human-resources-trial-environment"></a>Human Resources deneme ortamı sağlama

>[!NOTE]
> Nisan 2022'den itibaren, tek başına çalışan uygulamada Human Resources deneme ortamları kullanılamaz. Finans ve operasyon uygulamalarındaki İnsan Kaynakları özelliklerini değerlendirmeyle ilgilenen potansiyel müşteriler bunu, demo verileriyle birlikte ücretsiz 30 günlük deneme sürümünü kullanarak yapabilir. Dynamics 365 Finance, tek başına çalışan uygulamanın birleştirilmesi yoluyla Finance altyapısına getirilen İnsan Kaynakları özelliklerini içerecektir. Daha fazla bilgi için bkz. [İK tekliflerinin birleştirilmesi müşteriler için özellikleri bir araya getirir](https://cloudblogs.microsoft.com/dynamics365/it/2021/09/15/merging-of-hr-offerings-brings-capabilities-together-for-customers). Dynamics 365 Finance denemeleri hakkında daha fazla bilgi için [bu adım adım kılavuza](../fin-ops-core/fin-ops/get-started/before-you-buy.md) bakın. 


İlk korumalı alanınızı veya üretim ortamınızı sağlamadan önce, Human Resources işlevselliğini doğrulamak için bir [Human Resources deneme ortamı](https://go.microsoft.com/fwlink/p/?LinkId=2115962) sağlamak isteyebilirsiniz. Deneme ortamları, programı güvenli bir şekilde keşfetmek için kullanılabilen hayali veriler içerir. Deneme ortamı, talep eden kullanıcıya ait olmakla birlikte, diğer kullanıcılar İnsan Kaynakları için sistem yönetimi deneyimi aracılığıyla davet edilebilir. 

Deneme ortamları, bir İnsan Kaynakları ortamına erişimi olmayan kişiler için insan kaynakları işlevini değerlendirmeye yardımcı olur. Deneme ortamı sağlıyorsanız ve kimliği doğrulanmış kullanıcının mevcut bir veya daha fazla İnsan Kaynakları ortamına erişimi zaten varsa Kullanıcı mevcut ortama ya da ortam listesine yeniden yönlendirilir.

Deneme ortamlarının üretim ortamı olarak kullanılmaları amaçlanmamıştır. 30 günlük deneme süresi ile sınırlıdır. Deneme süresi sona erdiğinde, ortam ve ortamdaki tüm verileri silinir ve kurtarılamaz. Ortam bir korumalı alana veya üretim ortamına dönüştürülemez. Mevcut ortam geçersiz olduktan sonra yeni bir deneme ortamına kaydolabilirsiniz.

Human Resources deneme ortamı oluştururken kiracıda ayrıca bir Power Apps deneme ortamı oluşturulur ve Human Resources ortamına bağlanır. "TestDrive" adlı Power Apps ortamı, Human Resources ortamı ile aynı deneme süresine sahiptir.

> [!NOTE]
> Kimliği doğrulanmış kullanıcının Power Apps deneme ortamları oluşturma izni yoksa Human Resources deneme ortamı hazırlanamaz. Kullanıcı, Power Platform yönetim merkezinde deneme ortamları oluşturabilen kullanıcı grubuna dahil edilmelidir. Daha fazla bilgi için bkz. [Power Platform yönetim merkezinde kimlerin ortam oluşturup yönetebileceğini denetleme](/power-platform/admin/control-environment-creation).

## <a name="plan-human-resources-environments"></a>Human Resources ortamlarını planlama

İlk Human Resources ortamınızı oluşturmadan önce, projeniz için ortam ihtiyaçlarını dikkatlice planlamalısınız. Human Resources'a temel abonelikte iki ortam bulunur: üretim ortamı ve korumalı alan ortamı. Projenizin karmaşıklığına bağlı olarak, proje etkinliklerini desteklemek için ek korumalı alan ortamlarının satın alınması gerekebilir. 

Ek ortamlar için dikkat edilmesi gereken hususlar:

- **Veri taşıma**: Korumalı alan ortamınızın proje boyunca test amacıyla kullanılmasına izin vermek için veri taşıma etkinlikleri. Ek bir ortama sahip olduğunuzda, test ve yapılandırma etkinlikleri aynı anda farklı bir ortamda gerçekleşirken veri geçişleri etkinliklerinin devam etmesine olanak tanır.
- **Tümleştirme**: Ceridian Dayforce veya özel tümleştirmeler gibi yerel tümleştirmeler içerebilen tümleştirmeleri yapılandırın ve test edin.
- **Eğitim**: Personelinizi yeni sistemin kullanımı konusunda eğitmek için bir dizi eğitim verisiyle yapılandırılmış ayrı bir ortama ihtiyacınız olabilir. 
- **Çok aşamalı proje**: Projenin ilk yayınlanmasından sonra planlanan bir proje aşamasında yapılandırmayı, veri geçişini, testi veya diğer etkinlikleri destekleyin.

 > [!IMPORTANT]
 > Ortamınızı değerlendirirken aşağıda belirtilenleri uygulamanızı öneririz:
 > - Projeniz boyunca üretim ortamınızı GOLD yapılandırma ortamınız olarak kullanın. Korumalı alan ortamını üretim ortamına kopyalayamadığınızdan, bu önemlidir. Bu nedenle, yayına aldığınızda GOLD ortamınız üretim ortamınızdır ve bu ortamda kesin bitiş faaliyetlerinizi tamamlayacaksınız.</br></br>
 > - Servise alma işleminizi gerçekleştirmeden önce sahte bir kesin bitiş gerçekleştirmek için korumalı alanınızı veya başka bir ortamı kullanın. Bunu, GOLD yapılandırmanızın olduğu üretim ortamını korumalı alan ortamınıza yenileyerek yapabilirsiniz.</br></br>
 > - Servise alma kesin bitiş işlemi sırasında son verileri üretim ortamına geçirmek için gereken veri paketlerinin her birini içeren ayrıntılı bir kesin bitiş denetim listesi tutun.</br></br>
 > - Projeniz boyunca korumalı alan ortamınızı TEST ortamınız olarak kullanın. Ek ortamlara ihtiyacınız olursa kuruluşunuz bunları ek bir ücret karşılığında satın alabilir.</br></br>

## <a name="create-an-lcs-project"></a>LCS projesi oluşturma

İnsan Kaynakları ortamlarınızı yönetmek üzere LCS'yi kullanmak için öncelikle bir LCS projesi oluşturmanız gerekir.

1. İnsan Kaynaklarına abone olmak için kullandığınız hesabı kullanarak [LCS](https://lcs.dynamics.com/Logon/Index)'de oturum açın.

   > [!NOTE]
   > Sağlamanın başarılı olmasını sağlamak için, Human Resources ortamını sağlamak için kullandığınız hesap, Human Resources ortamıyla ilişkilendirilmiş Power Apps ortamındaki **Sistem Yöneticisi** veya **Sistem Özelleştirici** rolüne atanmalıdır. Power Platform'da kullanıcılara güvenlik rolleri atama hakkında daha fazla bilgi için bkz. [Kaynaklara kullanıcı güvenliği yapılandırma](/power-platform/admin/database-security).

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
    
3. Ortamınızın, Human Resources Deneme ortamında kullanılan tanıtım verileri kümesini içermesini istiyorsanız **Tanıtım Verilerini Ekle** seçeneğini belirleyin. Demo verileri uzun vadeli tanıtım veya eğitim ortamları için yararlıdır ve üretim ortamları için hiçbir zaman kullanılmamalıdır. İlk dağıtım sırasında bu seçeneği seçmeniz gerekir. Var olan bir dağıtımı sonra güncelleştiremezsiniz.

4. İnsan Kaynakları, Power Apps tümleştirmesi ve genişletilebilirliği sağlamak amacıyla daima bir Microsoft Power Apps ortamında sağlanır. Devam etmeden önce bu konudaki "Power Apps ortamı seçme" bölümünü okuyun. Power Apps ortamınız yoksa, LCS'de Ortamları yöneti seçin veya Power Apps Yönetim Merkezi'ne gidin. Ardından [Power Apps ortamı oluşturma](/powerapps/administrator/create-environment) adımlarını izleyin.

5. İnsan Kaynakları'nın tedarik edileceği ortamı seçin.

6. Koşulları kabul etmek için **Evet**'i seçin ve dağıtıma başlayın.

   Yeni ortamınız, soldaki gezinti bölmesinde bulunan ortam listesinde görüntülenir. Bununla birlikte, dağıtım durumunu **Dağıtıldı** olana kadar ortamı kullanmaya başlayamazsınız. Tipik olarak bu işlem birkaç dakika sürebilir. Sağlama işlemi başarısız olursa Desteğe başvurun.

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

5. Aşağıdaki Power Apps ortamları Human Resources için kullanılamaz. Bunlar LCS içindeki seçim listesinden filtrelenmiştir:
 
    - **Varsayılan Power Apps ortamları** - Her kiracıya otomatik olarak varsayılan Power Apps ortamı sağlanmakla birlikte, bu ortamları Humans Resources ile kullanmanızı önermeyiz. Tüm kiracı kullanıcıları Power Apps ortamına erişebilir ve Power Apps veya Power Automate tümleştirmelerini test ederken veya keşfederken üretim verilerini istemeden bozabilir.
   
    - **Deneme ortamları** - Bu ortamlar bir sona erme tarihiyle oluşturulur. Kullanım süresi sona erdiğinde, ortamınız ve bunun içinde bulunan tüm Human Resources örnekleri otomatik olarak kaldırılır.
   
    - **Desteklenmeyen coğrafyalar** - Ortam, desteklenen bir coğrafyada olmalıdır. Daha fazla bilgi için bkz. [Desteklenen coğrafyalar](hr-admin-setup-provision.md#supported-geographies).

6. Ortam için **Dynamics 365 uygulamalarını etkinleştir** seçeneği belirlenirse İnsan Kaynakları verilerini Power Apps ortamı ile tümleştirmek üzere yalnızca çift yazma özellikleri kullanılabilir. Daha fazla bilgi için bkz. [Çift yazma giriş sayfası](../fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-home-page.md).

    > [!NOTE]
    > Power Apps ortamı oluşturulduğunda **Dynamics 365 uygulamalarını etkinleştir** seçeneği belirlenmelidir. Sağlama sırasında bu seçenek belirlenmezse verileri Dynamics 365 Human Resources ile Power Apps ortamı arasında tümleştirmek veya ortamda Dynamics 365 Sales ve Field Service gibi Dynamics 365 uygulamalarını yüklemek için Çift yazmayı kullanamazsınız. Bu seçenek geri alınamaz. 
    > -  Human Resources, Human Resources dağıtıldıktan sonra bağlı Dataverse örneğinin değiştirilmesini desteklemez. </br></br>
    > Daha fazla bilgi için Power Platform belge sitesinde [Yeni bir ortam oluştururken dikkate alınması gereken bazı önemli noktalar](/power-platform/admin/create-environment#some-important-considerations-when-creating-a-new-environment) bölümüne bakın.  

7. Kullanılacak doğru ortamı belirledikten sonra, sağlama işlemine devam edebilirsiniz. 

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

Varsayılan olarak, ortamı oluşturan genel yöneticinin ortama erişimi vardır. Ek uygulama kullanıcılarına erişim izninin açıkça verilmesi gerekir. Human Resources ortamında kullanıcılar eklemeniz ve kullanıcılara uygun roller atamanız gerekir. Daha fazla bilgi için bkz. [Yeni kullanıcılar oluşturmak](/dynamics365/unified-operations/dev-itpro/sysadmin/tasks/create-new-users) ve [Kullanıcıları güvenlik rollerine atamak](/dynamics365/unified-operations/dev-itpro/sysadmin/tasks/assign-users-security-roles). 


[!INCLUDE[footer-include](../includes/footer-banner.md)]

