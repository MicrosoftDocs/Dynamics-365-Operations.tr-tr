---
title: "Microsoft Dynamics 365 for Talent sağlama"
description: "Bu konuda, Microsoft Dynamics 365 for Talent için yeni bir ortam sağlama işlemi adım adım anlatılmaktadır."
author: rschloma
manager: AnnBe
ms.date: 11/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Talent
ms.custom: 17271
ms.assetid: ba1ad49d-8232-400e-b11f-525423506a3f
ms.search.region: Global
ms.author: rschloma
ms.search.validFrom: 2017-11-20
ms.dyn365.ops.version: Talent July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: b4b54e97bdebc158adc3bc6d57a6661cd536f5fb
ms.contentlocale: tr-tr
ms.lasthandoff: 04/13/2018

---
# <a name="provision-microsoft-dynamics-365-for-talent"></a>Microsoft Dynamics 365 for Talent sağlama

[!INCLUDE [banner](includes/banner.md)]

Bu konuda, Microsoft Dynamics 365 for Talent için yeni bir üretim ortamı sağlama işlemi adım adım gösterecektir. Bu konuda, Talent'ı bir Bulut Çözümü Sağlayıcısı (CSP) veya kurumsal mimari (EA) sözleşmesi aracılığıyla aldığınız varsayılır. Zaten Talent hizmet planını içeren mevcut bir Microsoft Dynamics 365 lisansınız varsa ve bu konudaki adımları tamamlayamıyorsanız Destek birimine başvurun.

Başlamak için, genel yöneticinin [Microsoft Dynamics Lifecycle Services](http://lcs.dynamics.com)'da oturum açması (LCS) ve yeni bir Talent projesi oluşturması gerekir. Talent'ı sağlamanızı bir lisans sorunu engellemediği sürece, Destek biriminden veya Dynamics Hizmet Mühendisliği (DSE) temsilcilerinden yardım almanız gerekmez.

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
2. Talent, PowerApps tümleştirmesi ve genişletilebilirliği sağlamak amacıyla daima bir Microsoft PowerApps ortamında sağlanır. Devam etmeden önce bu konudaki "PowerApps ortamı seçme" bölümünü okuyun. 
3. Bir PowerApps ortamınız yoksa devam etmeden önce bu konuda yer alan "Yeni bir PowerApps ortamı oluşturma (gerekirse)" bölümündeki adımları izleyin.

    > [!NOTE]
    > Varolan ortamları görüntülemek veya yeni ortamlar oluşturmak için, Talent'ı sağlayan kiracı yöneticisine PowerApps P2 lisansı atanması gerekir. Kuruluşunuzun PowerApps P2 lisansı yoksa, bir CSP'den veya [PowerApps fiyatlandırma sayfasından](https://powerapps.microsoft.com/en-us/pricing/) bir lisans satın alabilirsiniz.

4. **Ekle**'yi ve ardından Talent sağlayacağınız ortamı seçin.
5. Koşulları kabul etmek için **Evet**'i seçin ve dağıtıma başlayın.

    Yeni ortamınız, soldaki gezinti bölmesinde bulunan ortam listesinde görüntülenir. Bununla birlikte, dağıtım durumunu **Dağıtıldı** olarak güncelleştirilene kadar ortamı kullanmaya başlayamazsınız. Tipik olarak bu işlem birkaç dakika sürebilir. Sağlama işlemi başarısız olursa Desteğe başvurmanız gerekir.

6. Yeni ortamı kullanmak için **Talent'ta oturum aç**'ı seçin.

> [!NOTE]
> Son gereksinimleri henüz yerine getirmediyseniz, projede Talent'ın bir test kurulumunu dağıtabilirsiniz. Ardından imzalayana kadar bu kurulumu kullanarak çözümünüzü test edebilirsiniz. Yeni ortamınızı test için kullanıyorsanız, bir üretim ortamı oluşturmak için bu yordamı yinelemeniz gerekir.

> [!NOTE]
> LCS aracılığıyla sağlanan Talent ortamları, İnsan Kaynakları (İK) görevleri için yapılandırılmış veya Talent'e özgü olan gösteri verilerini içermez. Demo verileri içeren bir ortama ihtiyaç duyarsanız 60 günlük ücretsiz [Talent deneme ortamına](https://dynamics.microsoft.com/en-us/talent/overview/) kaydolmanızı öneririz. Deneme ortamı, talep eden kullanıcıya ait olmakla birlikte, diğer kullanıcılar Ana İK için sistem yönetimi deneyimi aracılığıyla davet edilebilir. Deneme ortamları, programı güvenli bir şekilde keşfetmek için kullanılabilen hayali veriler içerir. Üretim ortamı olarak kullanılmaları amaçlanmamıştır. Deneme ortamının 60 gün sonra geçersiz olduğunda ortamdaki tüm verilerin silineceğini ve kurtarılamayacağını unutmayın. Mevcut ortam geçersiz olduktan sonra yeni bir deneme ortamına kaydolabilirsiniz.

## <a name="select-a-powerapps-environment"></a>PowerApps ortamı seçme

Talent ve PowerApps ortamları arasındaki tümleştirme, PowerApps araçlarını kullanarak Talent verilerinin kullanımını tümleştirmenizi ve genişletmenizi sağlar. PowerApps ortamlarının amacını anlamak yalnızca Talent'ı genişletecek uygulamalar oluşturmanıza değil aynı zamanda Talent'ı sağlarken doğru ortamı seçmenize de yardımcı olur. PowerApps ortamları hakkında ortamın kapsamı, ortama erişim ile ortam oluşturma ve seçme de dahil olmak üzere bilgi edinmek için bkz. [PowerApps ortamları duyurusu](https://powerapps.microsoft.com/en-us/blog/powerapps-environments/). 

Talent'ı hangi PowerApps ortamına dağıtacağınızı belirlerken aşağıdaki yönergeleri kullanın: 
1. LCS'de Ortamları yönet öğesini seçin veya doğrudan mevcut ortamları görebileceğiniz ve yeni ortamlar oluşturabileceğiniz PowerApps Yönetim merkezine gidin.
2. Tek bir PowerApps ortamına tek bir Talent ortamı eşlenir.
3. PowerApps ortamı ilgili PowerApps, Flow ve CDS uygulamalarının yanı sıra Talent uygulamasını "içerir". PowerApps ortamı silinirse, içerdiği uygulamalar da silinir.
4. Veri tümleştirme ve test stratejileri göz önünde bulundurmalıdır: örneğin Korumalı alan, UAT, Üretim. Bu nedenle, Talent ortamının eşlendiği PowerApps ortamını daha sonra değiştirmek kolay olmayacağından, dağıtımınızla ilgili çeşitli etkileri değerlendirmenizi öneririz.
5. Aşağıdaki PowerApps ortamları Talent için kullanılamaz ve LCS'deki seçim listesinden filtrelenecektir:
 
    **CD 2.0 Ortamları** CDS 2.0 21 Mart 2018'de genel kullanıma sunulacaktır ancak Talent henüz CDS 2.0'ı desteklememektedir. PowerApps Yönetim merkezinden CDS 2.0 veritabanları oluşturabilir ve görüntüleyebilirsiniz ancak bunları Talent'ta kullanamazsınız. CDS 2.0 Ortamlarını Talent dağıtımlarında kullanma seçeneği ileri bir tarihte kullanılabilir olacaktır.
   
   > [!Note]
   > Yönetim portalında CDS 1.0 ve 2.0 ortamlarını birbirinden ayırmak için bir ortam seçin ve **Ayrıntılar**'a bakın. CD 2.0 ortamlarının tümü "Bu ayarları Dynamics 365 Yönetim Merkezinde yönetebilirsiniz" referansıyla bir örnek sürüme yönlendirir ve Veritabanı sekmesi bulunmaz. 
 
   **Varsayılan Power Apps ortamları** Her kiracıya otomatik olarak varsayılan bir PowerApps ortamı sağlanmasına karşın tüm kiracı kullanıcıların PowerApps ortamına erişimi olduğundan ve kiracılar PowerApps veya Flow tümleştirmelerini test ederken ve keşfederken yanlışlıkla üretim verilerine zarar verebileceklerinden, bu alanların Talent ile kullanılmasını önermiyoruz.
   
   <strong>Deneme Sürüşü ortamları</strong> ‘TestDrive – alias@domain’ gibi bir ada sahip ortamlar 60 günlük kullanım için oluşturulur ve süre dolduğunda sonlandırılarak ortamınızın otomatik olarak kaldırılmasına neden olur.
   
   **Desteklenmeyen bölgeler** Talent şu anda yalnızca şu bölgelerde desteklenmektedir: Amerika Birleşik Devletleri, Avrupa veya Avustralya.
  
6. Kullanılacak doğru ortamı belirledikten sonra gerçekleştirmeniz gereken belirli bir eylem yoktur. Sağlama işlemine devam edin. 
 
## <a name="create-a-new-powerapps-environment-if-required"></a>Yeni bir PowerApps ortamı oluşturma (gerekirse)

PowerApps 2 lisansına sahip kiracı yönetici bağlamında Talent için yeni bir PowerApps ortamı oluşturmak için PowerShell komut dosyası çalıştırın. Komut dosyası otomatik olarak aşağıdaki adımları gerçekleştirir:


 + PowerApps ortamı oluşturma
 + CDS 1.0 veritabanı oluşturma
 + CDS 1.0 veritabanındaki tüm örnek verileri temizleme


Komut dosyasını çalıştırmak için aşağıdaki yönergeleri izleyin:

1. Şu konumdan ProvisionCDSEnvironment.zip dosyasını indirin: [ProvisionCDSEnvironment komut dosyaları](https://go.microsoft.com/fwlink/?linkid=870436)  

2. ProvisionCDSEnviroinment.zip dosyasının tüm içeriğini başka bir klasöre çıkarın.

3. Yönetici olarak Windows PowerShell veya Windows PowerShell ISE programını çalıştırın.

   Komut dosyasının çalışabilmesi için yürütme ilkesini ayarlama hakkında daha fazla bilgi için [Yürütme İlkesi Ayarlama](https://docs.microsoft.com/en-us/powershell/module/microsoft.powershell.security/set-executionpolicy?view=powershell-6) konusuna bakın.
  
4. PowerShell içinde, dosyayı çıkardığınız klasöre gidin ve değerleri aşağıda belirtildiği şekilde değiştirerek komutu çalıştırın:
 
   ```.\ProvisionCDSEnvironment -EnvironmentName MyNewEnvironment -Location YourLocation```

    
   **MyNewEnvironment** ortam adınız ile değiştirilmelidir. Bu ad LCS'de görüntülenir ve kullanıcılar kullanılacak Talent ortamını seçerken gösterilir. 

   **YourLocation** Talent için desteklenen bölgelerden biriyle değiştirilir: amerika birleşik devletleri, avrupa, avustralya. 

   **-Verbose** isteğe bağlıdır ve sorunla karşılaşırsanız destek birimine gönderilmek üzere ayrıntılı bilgiler sağlar.

5. Sağlama işlemine devam edin.
 


## <a name="grant-access-to-the-environment"></a>Ortama erişim izni verme
Varsayılan olarak, ortamı oluşturan genel yöneticinin ortama erişimi vardır. Ancak ek uygulama kullanıcılarına erişim izninin açıkça verilmesi gerekir. Erişim izni vermek için Ana İK ortamında [kullanıcılar ekleyin](../dev-itpro/sysadmin/tasks/create-new-users.md) ve [kullanıcılara uygun roller atayın](../dev-itpro/sysadmin/tasks/assign-users-security-roles.md). Attract ve Onboard uygulamalarına erişebilmeleri için bu kullanıcıları PowerApps ortamına da eklemeniz gerekir. Yordam burada özetlenmiştir. Adımları tamamlamak için yardım gereksiniminiz varsa [PowerApps yönetim merkezine giriş](https://powerapps.microsoft.com/en-us/blog/introducing-admin-center-for-powerapps/) başlıklı blog gönderisine bakın.

Bu yordam, Talent ortamını dağıtan genel yönetici tarafından tamamlanır.

1. [PowerApps Yönetim merkezi](https://preview.admin.powerapps.com/environments)'ni açın.
2. İlgili ortamları seçin.
3. **Güvenlik** sekmesinde gereken kullanıcıları **Ortam Oluşturucu** rolüne ekleyin.

    Kullanıcıların PowerApps ortamına el ile eklendiği bu son adımın geçici olduğunu unutmayın. Sonuçta, kullanıcılar Ana İK'ya eklendiğinde otomatik olarak tamamlanacaktır.

