---
title: Human Resources'ı hazırlama
description: Bu makalede, Microsoft Dynamics 365 Human Resources için yeni bir üretim ortam sağlama işlemi adım adım anlatılmaktadır.
author: andreabichsel
manager: AnnBe
ms.date: 02/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 4f2fd2b7bf9f09a61d07e1bc35ad48fe2c5d7383
ms.sourcegitcommit: c69926b4285cb2ec2d9ce1ad72d1cb852024dd5e
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/18/2020
ms.locfileid: "3138371"
---
# <a name="provision-human-resources"></a>Human Resources'ı hazırlama

Bu makalede, Microsoft Dynamics 365 Human Resources için yeni bir üretim ortam sağlama işlemi adım adım anlatılmaktadır. Bu konuda, İnsan Kaynaklarını bir Bulut Çözümü Sağlayıcısı (CSP) veya kurumsal mimari (EA) sözleşmesi aracılığıyla aldığınız varsayılır. Zaten insan kaynakları hizmet planını içeren mevcut bir Microsoft Dynamics 365 lisansınız varsa ve bu konudaki adımları tamamlayamıyorsanız Destek birimine başvurun.

Başlamak için, genel yöneticinin [Microsoft Dynamics Lifecycle Services](https://lcs.dynamics.com)'da oturum açması (LCS) ve yeni bir İnsan Kaynakları projesi oluşturması gerekir. İnsan Kaynaklarını sağlamanızı bir lisans sorunu engellemediği sürece, Destek biriminden veya Dynamics Hizmet Mühendisliği (DSE) temsilcilerinden yardım almanız gerekmez.

## <a name="create-an-lcs-project"></a>LCS projesi oluşturma

İnsan Kaynakları ortamlarınızı yönetmek üzere LCS'yi kullanmak için öncelikle bir LCS projesi oluşturmanız gerekir.

1. İnsan Kaynaklarına abone olmak için kullandığınız hesabı kullanarak [LCS](https://lcs.dynamics.com/Logon/Index)'de oturum açın.

2. Yeni bir proje oluşturmak için artı işaretini (**+**) seçin.

3. Ürün adı ve ürün sürümü olarak **Microsoft Dynamics 365 Human Resources**'ı seçin.

4. **Dynamics 365 Human Resources** metodolojisini seçin.

5. **Oluştur**'u seçin.

İnsan Kaynaklarını kullanmaya başlamayla ilgili bilgiler için yeni projede oluşturduğunuz **İnsan Kaynakları** metodolojisine bakın. Projeyi oluşturmayı tamamladıktan sonra, İnsan Kaynakları ortamınızı sağlamak için aşağıdaki yordamı tamamlayın.

## <a name="provision-a-human-resources-project"></a>İnsan kaynakları projesi hazırlığı

Bir LCS projesi oluşturduktan sonra, bir ortama İnsan Kaynakları sağlayabilirsiniz.

1. LCS projenizde **İnsan Kaynakları Uygulama Yöneticisi** kutucuğunu seçin.

2. Bunun bir sanal alanda mı yoksa bir İnsan Kaynakları üretim örneği olup olmadığını belirtin. Erken geri bildirim ve sınamaya izin vermek için korumalı alan örneklerinde önceki Önizleme özellikleri kullanılabilir olabilir.
   
    > [!NOTE]
    > Human Resources örneği türü ayarlandıktan sonra değiştirilemez. Devam etmeden önce doğru örnek türünün seçilmiş olduğundan emin olun.</br></br>
    > İnsan Kaynakları örnek türü, Power Apps Yönetim Merkezi'nde ayarladığınız Microsoft Power Apps ortamının örnek türünden ayrıdır.
    
3. Ortamınızın İnsan Kaynakları Test Sürümü deneyiminde kullanılan aynı tanıtım verileri kümesini içermesini istiyorsanız **Tanıtım Verilerini Ekle** seçeneğini seçin. Bu uzun vadeli tanıtım veya eğitim ortamları için yararlıdır ve üretim ortamları için hiçbir zaman kullanılmamalıdır.  Not ilk dağıtım sırasında bu seçeneği seçmeniz gerekir. Var olan bir dağıtımı sonra güncelleştiremezsiniz.

4. İnsan Kaynakları, Power Apps tümleştirmesi ve genişletilebilirliği sağlamak amacıyla daima bir Microsoft Power Apps ortamında sağlanır. Devam etmeden önce bu konudaki "Power Apps ortamı seçme" bölümünü okuyun. Power Apps ortamınız yoksa, LCS'de Ortamları yöneti seçin veya Power Apps Yönetim Merkezi'ne gidin. Ardından [Power Apps ortamı oluşturma](https://docs.microsoft.com/powerapps/administrator/create-environment) adımlarını izleyin.

5. İnsan Kaynakları'nın tedarik edileceği ortamı seçin.

6. Koşulları kabul etmek için **Evet**'i seçin ve dağıtıma başlayın.

   Yeni ortamınız, soldaki gezinti bölmesinde bulunan ortam listesinde görüntülenir. Bununla birlikte, dağıtım durumunu **Dağıtıldı** olarak güncelleştirilene kadar ortamı kullanmaya başlayamazsınız. Tipik olarak bu işlem birkaç dakika sürebilir. Sağlama işlemi başarısız olursa Desteğe başvurmanız gerekir.

7. Yeni ortamı kullanmak için **İnsan Kaynakları'nda oturum aç**'ı seçin.

    > [!NOTE]
    > Son gereksinimleri henüz yerine getirmediyseniz, projede İnsan Kaynakları'nın bir test kurulumunu dağıtabilirsiniz. Ardından imzalayana kadar bu kurulumu kullanarak çözümünüzü test edebilirsiniz. Yeni ortamınızı test için kullanıyorsanız, bir üretim ortamı oluşturmak için bu yordamı yinelemeniz gerekir.

    > Ücretsiz olarak 60 günlük [Human Resources deneme ortamı](https://dynamics.microsoft.com/talent/overview/) kullanabilirsiniz. Deneme ortamı, talep eden kullanıcıya ait olmakla birlikte, diğer kullanıcılar İnsan Kaynakları için sistem yönetimi deneyimi aracılığıyla davet edilebilir. Deneme ortamları, programı güvenli bir şekilde keşfetmek için kullanılabilen hayali veriler içerir. Üretim ortamı olarak kullanılmaları amaçlanmamıştır. Deneme ortamının 60 gün sonra geçersiz olduğunda ortamdaki tüm verilerin silineceğini ve kurtarılamayacağını unutmayın. Mevcut ortam geçersiz olduktan sonra yeni bir deneme ortamına kaydolabilirsiniz.

## <a name="select-a-power-apps-environment"></a>Bir Power Apps ortamı seçin

İnsan Kaynakları ve Power Apps ortamları arasındaki tümleştirme, Power Apps araçlarını kullanarak İnsan Kaynakları verilerinin kullanımını tümleştirmenizi ve genişletmenizi sağlar. Power Apps ortamlarının amacını anlamak yalnızca İnsan Kaynakları'ı genişletecek uygulamalar oluşturmanıza değil, İnsan Kaynakları'ı sağlarken doğru ortamı seçmenize de yardımcı olur. Power Apps ortamları hakkında ortamın kapsamı, ortama erişim ile ortam oluşturma ve seçme de dahil olmak üzere bilgi edinmek için bkz. [Power Apps ortamları duyurusu](https://powerapps.microsoft.com/blog/powerapps-environments/). 

İnsan Kaynakları'nı hangi Power Apps ortamına dağıtacağınızı belirlerken aşağıdaki yönergeleri kullanın: 

1. LCS'de **Ortamları yönet** öğesini seçin veya doğrudan mevcut ortamları görebileceğiniz ve yeni ortamlar oluşturabileceğiniz Power Apps Yönetim merkezine gidin.

2. Tek bir Power Apps ortamına tek bir İnsan Kaynakları ortamı eşlenir.

3. Power Apps ortamı ilgili Power Apps, Power Automate ve Common Data Service uygulamalarının yanı sıra İnsan Kaynakları'nı içerir. Power Apps ortamı silinirse, içerdiği uygulamalar da silinir. Bir İnsan Kaynakları ortamı sağlanırken, bir **Denem** veya **Üretim** ortamı sağlayabilirsiniz. Ortamın nasıl kullanılacağına göre ortam türünü seçin. 

4. Veri tümleştirme ve test stratejileri göz önünde bulundurmalıdır: örneğin Korumalı alan, UAT veya Üretim. İnsan Kaynakları ortamının eşlendiği Power Apps ortamını daha sonra değiştirmek kolay olmayacağından, dağıtımınızla ilgili çeşitli etkileri değerlendirmenizi öneririz.

5. Aşağıdaki Power Apps ortamları İnsan Kaynakları için kullanılamaz ve LCS'deki seçim listesinden filtrelenecektir:
 
    - **Varsayılan Power Apps ortamları**: Her kiracıya otomatik olarak varsayılan bir Power Apps ortamı sağlansa da tüm kiracı kullanıcıların Power Apps ortamına erişimi olduğundan ve kiracılar Power Apps veya Power Automate tümleştirmelerini test ederken ve keşfederken yanlışlıkla üretim verilerine zarar verebileceklerinden, bu alanların İnsan Kaynakları ile kullanılmasını önermiyoruz.
   
    - **Deneme ortamları** - Bu ortamlar, bir bitiş tarihiyle oluşturulmuştur ve bu süreden sonra süreleri dolar, bu da ortamlarınızın ve içlerinde bulunan tüm İnsan Kaynakları kurulumlarının otomatik olarak kaldırılmasına neden olur.
   
    - **Desteklenmeyen bölgeler** - İnsan Kaynakları şu anda yalnızca şu bölgelerde desteklenmektedir: Amerika Birleşik Devletleri, Avrupa, Birleşik Krallık veya Avustralya, Kanada ve Asya.

    > [!NOTE]
    > Human Resources ortamı, Power Apps ortamın sağlandığı aynı bölgede sağlandı. Human Resources ortamın başka bir bölgeye geçirilmesi desteklenmez.

6. Kullanılacak doğru ortamı belirledikten sonra, sağlama işlemine devam edebilirsiniz. 
 
## <a name="grant-access-to-the-environment"></a>Ortama erişim izni verme

Varsayılan olarak, ortamı oluşturan genel yöneticinin ortama erişimi vardır. Ancak ek uygulama kullanıcılarına erişim izninin açıkça verilmesi gerekir. Erişim izni vermek için İnsan Kaynakları ortamında kullanıcılar ekleyin ve kullanıcılara uygun roller atamanız gerekir. İnsan Kaynakları'nı dağıtan genel yönetici, başlatmayı tamamlamak ve diğer kiracı kullanıcılar için erişim sağlamak üzere Attract ve Onboard'ı da başlatmalıdır.  Bu gerçekleştirilene kadar, diğer kullanıcılar Attract ve Onboard'a erişemez ve erişim ihlali hataları alır. Daha fazla bilgi için bkz. [Yeni kullanıcılar oluşturmak](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/sysadmin/tasks/create-new-users) ve [Kullanıcıları güvenlik rollerine atamak](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/sysadmin/tasks/assign-users-security-roles). 
