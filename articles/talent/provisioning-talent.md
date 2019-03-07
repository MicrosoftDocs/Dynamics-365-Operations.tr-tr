---
title: Talent sağlama
description: Bu konuda, Dynamics 365 for Talent için yeni bir ortam sağlama işlemi adım adım anlatılmaktadır.
author: rschloma
manager: AnnBe
ms.date: 09/27/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent
ms.custom: 17271
ms.assetid: ba1ad49d-8232-400e-b11f-525423506a3f
ms.search.region: Global
ms.author: rschloma
ms.search.validFrom: 2017-11-20
ms.dyn365.ops.version: Talent July 2017 update
ms.openlocfilehash: 6fb41a8c1ff4ce95bab5b169256955f244e66071
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2019
ms.locfileid: "306628"
---
# <a name="provision-talent"></a>Talent sağlama

[!include [banner](includes/banner.md)]

Bu konuda, Dynamics 365 for Talent için yeni bir üretim ortam sağlama işlemi adım adım anlatılmaktadır. Bu konuda, Talent'ı bir Bulut Çözümü Sağlayıcısı (CSP) veya kurumsal mimari (EA) sözleşmesi aracılığıyla aldığınız varsayılır. Zaten Talent hizmet planını içeren mevcut bir Microsoft Dynamics 365 lisansınız varsa ve bu konudaki adımları tamamlayamıyorsanız Destek birimine başvurun.

Başlamak için, genel yöneticinin [Microsoft Dynamics Lifecycle Services](https://lcs.dynamics.com)'da oturum açması (LCS) ve yeni bir Talent projesi oluşturması gerekir. Talent'ı sağlamanızı bir lisans sorunu engellemediği sürece, Destek biriminden veya Dynamics Hizmet Mühendisliği (DSE) temsilcilerinden yardım almanız gerekmez.

## <a name="create-an-lcs-project"></a>LCS projesi oluşturma
Talent ortamlarınızı yönetmek üzere LCS'yi kullanmak için öncelikle bir LCS projesi oluşturmanız gerekir.

1. Talent'a abone olmak için kullandığınız hesabı kullanarak [LCS](https://lcs.dynamics.com/Logon/Index)'de oturum açın.
2. Yeni bir proje oluşturmak için artı işaretini (**+**) seçin.
3. Ürün adı ve ürün sürümü olarak **Microsoft Dynamics 365 for Talent**'ı seçin.
4. **Dynamics 365 for Talent** metodolojisini seçin.
5. **Oluştur**'u seçin.

Talent'ı kullanmaya başlamayla ilgili bilgiler için yeni projede oluşturduğunuz **Talent** metodolojisine bakın. Projeyi oluşturmayı tamamladıktan sonra, Talent ortamınızı sağlamak için aşağıdaki yordamı tamamlayın.

## <a name="provision-a-talent-project"></a>Talent projesi sağlama
Bir LCS projesi oluşturduktan sonra, bir ortama Talent sağlayabilirsiniz.

1. LCS projenizde **Talent Uygulama Yöneticisi** kutucuğunu seçin.
2. Talent, PowerApps tümleştirmesi ve genişletilebilirliği sağlamak amacıyla daima bir Microsoft PowerApps ortamında sağlanır. Devam etmeden önce bu konudaki "PowerApps ortamı seçme" bölümünü okuyun. PowerApps ortamınız yoksa, LCS'de Ortamları yöneti seçin veya PowerApps Yönetim Merkezi'ne gidin. Ardından [PowerApps ortamı oluşturma](https://docs.microsoft.com/en-us/powerapps/administrator/create-environment) adımlarını izleyin.

    > [!NOTE]
    > Varolan ortamları görüntülemek veya yeni ortamlar oluşturmak için, Talent'ı sağlayan kiracı yöneticisine PowerApps P2 lisansı atanması gerekir. Kuruluşunuzun PowerApps P2 lisansı yoksa, bir CSP'den veya [PowerApps fiyatlandırma sayfasından](https://powerapps.microsoft.com/en-us/pricing/) bir lisans satın alabilirsiniz.

4. **Ekle**'yi ve ardından Talent sağlayacağınız ortamı seçin.
5. Ortamınızın Talent Test Sürümü deneyiminde kullanılan aynı Tanıtım verileri kümesini içermesini istiyorsanız "Tanıtım Verilerini Ekle" seçeneğini seçin.  Bu uzun vadeli tanıtım veya eğitim ortamları için yararlıdır ve üretim ortamları için hiçbir zaman kullanılmamalıdır.  Bu seçeneği ilk dağıtımda seçmeniz gerektiğini ve mevcut bir dağıtımda sonradan güncelleştiremeyeceğinizi unutmayın.
6. Koşulları kabul etmek için **Evet**'i seçin ve dağıtıma başlayın.

    Yeni ortamınız, soldaki gezinti bölmesinde bulunan ortam listesinde görüntülenir. Bununla birlikte, dağıtım durumunu **Dağıtıldı** olarak güncelleştirilene kadar ortamı kullanmaya başlayamazsınız. Tipik olarak bu işlem birkaç dakika sürebilir. Sağlama işlemi başarısız olursa Desteğe başvurmanız gerekir.

7. Yeni ortamı kullanmak için **Talent'ta oturum aç**'ı seçin.

> [!NOTE]
> Son gereksinimleri henüz yerine getirmediyseniz, projede Talent'ın bir test kurulumunu dağıtabilirsiniz. Ardından imzalayana kadar bu kurulumu kullanarak çözümünüzü test edebilirsiniz. Yeni ortamınızı test için kullanıyorsanız, bir üretim ortamı oluşturmak için bu yordamı yinelemeniz gerekir.

> [!NOTE]
> Talent aboneliğinin bir parçası olarak yalnızca iki LCS ortamına izin verildiğinden, ücretsiz 60 günlük [Talent deneme ortamından](https://dynamics.microsoft.com/en-us/talent/overview/) yaralanmayı düşünebilirsiniz. Deneme ortamı, talep eden kullanıcıya ait olmakla birlikte, diğer kullanıcılar Ana İK için sistem yönetimi deneyimi aracılığıyla davet edilebilir. Deneme ortamları, programı güvenli bir şekilde keşfetmek için kullanılabilen hayali veriler içerir. Üretim ortamı olarak kullanılmaları amaçlanmamıştır. Deneme ortamının 60 gün sonra geçersiz olduğunda ortamdaki tüm verilerin silineceğini ve kurtarılamayacağını unutmayın. Mevcut ortam geçersiz olduktan sonra yeni bir deneme ortamına kaydolabilirsiniz.

## <a name="select-a-powerapps-environment"></a>PowerApps ortamı seçme

Talent ve PowerApps ortamları arasındaki tümleştirme, PowerApps araçlarını kullanarak Talent verilerinin kullanımını tümleştirmenizi ve genişletmenizi sağlar. PowerApps ortamlarının amacını anlamak yalnızca Talent'ı genişletecek uygulamalar oluşturmanıza değil aynı zamanda Talent'ı sağlarken doğru ortamı seçmenize de yardımcı olur. PowerApps ortamları hakkında ortamın kapsamı, ortama erişim ile ortam oluşturma ve seçme de dahil olmak üzere bilgi edinmek için bkz. [PowerApps ortamları duyurusu](https://powerapps.microsoft.com/en-us/blog/powerapps-environments/). 

Talent'ı hangi PowerApps ortamına dağıtacağınızı belirlerken aşağıdaki yönergeleri kullanın: 
1. LCS'de Ortamları yönet öğesini seçin veya doğrudan mevcut ortamları görebileceğiniz ve yeni ortamlar oluşturabileceğiniz PowerApps Yönetim merkezine gidin.
2. Tek bir PowerApps ortamına tek bir Talent ortamı eşlenir.
3. PowerApps ortamı ilgili PowerApps, Flow ve CDS uygulamalarının yanı sıra Talent uygulamasını "içerir". PowerApps ortamı silinirse, içerdiği uygulamalar da silinir. Bir Yetenek ortamı sağlama sırasında "Deneme" veya "Ürün" sağlanabilir. Ortamın nasıl kullanılacağına göre ortam türünü seçin. 
4. Veri tümleştirme ve test stratejileri göz önünde bulundurmalıdır: örneğin Korumalı alan, UAT, Üretim. Bu nedenle, Talent ortamının eşlendiği PowerApps ortamını daha sonra değiştirmek kolay olmayacağından, dağıtımınızla ilgili çeşitli etkileri değerlendirmenizi öneririz.
5. Aşağıdaki PowerApps ortamları Talent için kullanılamaz ve LCS'deki seçim listesinden filtrelenecektir:
 
   **Varsayılan Power Apps ortamları** Her kiracıya otomatik olarak varsayılan bir PowerApps ortamı sağlanmasına karşın tüm kiracı kullanıcıların PowerApps ortamına erişimi olduğundan ve kiracılar PowerApps veya Flow tümleştirmelerini test ederken ve keşfederken yanlışlıkla üretim verilerine zarar verebileceklerinden, bu alanların Talent ile kullanılmasını önermiyoruz.
   
   <strong>Deneme Sürüşü ortamları</strong> ‘TestDrive – alias@domain’ gibi bir ada sahip ortamlar 60 günlük kullanım için oluşturulur ve süre dolduğunda sonlandırılarak ortamınızın otomatik olarak kaldırılmasına neden olur.
   
   **Desteklenmeyen bölgeler** Talent şu anda yalnızca şu bölgelerde desteklenmektedir: Amerika Birleşik Devletleri, Avrupa veya Avustralya.
  
6. Kullanılacak doğru ortamı belirledikten sonra gerçekleştirmeniz gereken belirli bir eylem yoktur. Sağlama işlemine devam edin. 
 
## <a name="grant-access-to-the-environment"></a>Ortama erişim izni verme
Varsayılan olarak, ortamı oluşturan genel yöneticinin ortama erişimi vardır. Ancak ek uygulama kullanıcılarına erişim izninin açıkça verilmesi gerekir. Erişim izni vermek için Ana İK ortamında [kullanıcılar ekleyin](https://docs.microsoft.com/en-us/dynamics365/unified-operations/dev-itpro/sysadmin/tasks/create-new-users) ve [kullanıcılara uygun roller atayın](https://docs.microsoft.com/en-us/dynamics365/unified-operations/dev-itpro/sysadmin/tasks/assign-users-security-roles). Talent'ı dağıtan genel yönetici, başlatmayı tamamlamak ve diğer kiracı kullanıcılar için erişim sağlamak üzere Attract ve Onboard uygulamalarını da başlatmalıdır.  Bu gerçekleştirilene kadar, diğer kullanıcılar Attract ve Onboard uygulamalarına erişemez ve erişim ihlali hataları alır.

