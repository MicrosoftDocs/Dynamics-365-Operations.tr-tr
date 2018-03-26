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
ms.sourcegitcommit: 72d4ff5e1311005d3bf43a13e28208cd9b3d1457
ms.openlocfilehash: e4459e8be4bfab8e0789744eacd533286b6c05e0
ms.contentlocale: tr-tr
ms.lasthandoff: 03/08/2018

---
# <a name="provision-microsoft-dynamics-365-for-talent"></a>Microsoft Dynamics 365 for Talent sağlama

[!include[banner](includes/banner.md)]

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
2. Talent, PowerApps tümleştirmesi ve genişletilebilirliği sağlamak amacıyla daima bir Microsoft PowerApps ortamında sağlanır. Bir PowerApps ortamınız yoksa devam etmeden önce bu konuda yer alan "Yeni bir PowerApps ortamı oluşturma (gerekirse)" bölümündeki adımları izleyin.

    > [!NOTE]
    > Varolan ortamları görüntülemek veya yeni ortamlar oluşturmak için, Talent'ı sağlayan kiracı yöneticisine PowerApps P2 lisansı atanması gerekir. Kuruluşunuzun PowerApps P2 lisansı yoksa, bir CSP'den veya [PowerApps fiyatlandırma sayfasından](https://powerapps.microsoft.com/en-us/pricing/) bir lisans satın alabilirsiniz.

3. **Ekle**'yi ve ardından Talent sağlayacağınız ortamı seçin.
4. Koşulları kabul etmek için **Evet**'i seçin ve dağıtıma başlayın.

    Yeni ortamınız, soldaki gezinti bölmesinde bulunan ortam listesinde görüntülenir. Bununla birlikte, dağıtım durumunu **Dağıtıldı** olarak güncelleştirilene kadar ortamı kullanmaya başlayamazsınız. Tipik olarak bu işlem birkaç dakika sürebilir. Sağlama işlemi başarısız olursa Desteğe başvurmanız gerekir.

6. Yeni ortamı kullanmak için **Talent'ta oturum aç**'ı seçin.

> [!NOTE]
> Son gereksinimleri henüz yerine getirmediyseniz, projede Talent'ın bir test kurulumunu dağıtabilirsiniz. Ardından imzalayana kadar bu kurulumu kullanarak çözümünüzü test edebilirsiniz. Yeni ortamınızı test için kullanıyorsanız, bir üretim ortamı oluşturmak için bu yordamı yinelemeniz gerekir.

> [!NOTE]
> LCS aracılığıyla sağlanan Talent ortamları, İnsan Kaynakları (İK) görevleri için yapılandırılmış veya Talent'e özgü olan gösteri verilerini içermez. Demo verileri içeren bir ortama ihtiyaç duyarsanız 60 günlük ücretsiz [Talent deneme ortamına](https://dynamics.microsoft.com/en-us/talent/overview/) kaydolmanızı öneririz. Deneme ortamı, talep eden kullanıcıya ait olmakla birlikte, diğer kullanıcılar Ana İK için sistem yönetimi deneyimi aracılığıyla davet edilebilir. Deneme ortamları, programı güvenli bir şekilde keşfetmek için kullanılabilen hayali veriler içerir. Üretim ortamı olarak kullanılmaları amaçlanmamıştır. Deneme ortamının 60 gün sonra geçersiz olduğunda ortamdaki tüm verilerin silineceğini ve kurtarılamayacağını unutmayın. Mevcut ortam geçersiz olduktan sonra yeni bir deneme ortamına kaydolabilirsiniz.

## <a name="create-a-new-powerapps-environment-if-required"></a>Yeni bir PowerApps ortamı oluşturma (gerekirse)
Talent ve PowerApps ortamları arasındaki tümleştirme, PowerApps araçlarını kullanarak Talent verilerinin kullanımını tümleştirmenizi ve genişletmenizi sağlar. PowerApps ortamlarının amacını anlamak, Talent'i genişletmek için ihtiyacınız olan uygulamaları oluşturmanıza yardımcı olur. PowerApps ortamları hakkında ortamın kapsamı, ortama erişim ile ortam oluşturma ve seçme de dahil olmak üzere bilgi edinmek için bkz. [PowerApps ortamları duyurusu](https://powerapps.microsoft.com/en-us/blog/powerapps-environments/). Her kiracıya Varsayılan PowerApps ortamı otomatik olarak sağlanmasına karşın bu ortam, Talent dağıtımınız için kullanılacak en iyi ortam olmayabilir. Veri tümleştirme ve test stratejileri bu adımda değerlendirilmelidir. Daha sonra bazı kararların değiştirilmesi kolay olmayacağından, dağıtımınızı etkileyebilecek çeşitli etkileri değerlendirmenizi öneririz. 

Her kiracıya Varsayılan PowerApps ortamı otomatik olarak sağlanmasına rağmen bu ortam, Talent dağıtımınız için kullanılacak en iyi ortam olmayabilir. Bu adım sırasında veri tümleştirme ve test stratejileri dikkate alınmalıdır. Bu nedenle, PowerApps ortamını daha sonra değiştirmek kolay olmayacağından, dağıtımınızla ilgili çeşitli etkileri değerlendirmenizi öneririz.

1. LCS'de **Ortamları yönet**'i seçin. Mevcut ortamları görebileceğiniz ve yeni ortamlar oluşturabileceğiniz [PowerApps Yönetici merkezine](https://preview.admin.powerapps.com/environments) yönlendirilirsiniz.
2. **Yeni Ortam**'ı seçin.
3. Ortam için benzersiz bir ad girin ve dağıtmak için konum seçin.

    > [!NOTE]
    > Talent tüm bölgelerde kullanılamaz. Bu nedenle, ortamınız için konum seçmeden önce kullanılabilirliği kontrol ettiğinizden emin olun.

4. Bir veritabanı oluşturmak isteyip istemediğiniz sorulduğunda, Talent verilerinizi barındıracak olan bir Common Data Service (CDS) veritabanı oluşturmak için **Veritabanı oluştur**'u seçin. Bir veritabanı oluşturarak, PowerApps uygulamalarını Talent ile tümleştirebilirsiniz.
5. Veritabanı için kullanacağınız erişim düzeyi sorulur. **Erişimi kısıtla** seçeneğini belirlemenizi öneririz. Çünkü bu seçenek Talent kullanıcılarının PowerApps uygulamasını kullanarak hassas verilere doğrudan erişimini engeller.
6. Oluşturulan CDS veritabanı üretim ortamınıza, diğer bilgilerin yanında etkin olmayan personel ve hayali adresler ekleyen demo veriler içerir. Demo verileri kaldırmak için, CDS veritabanını oluşturmayı tamamladıktan sonra aşağıdaki adımları uygulayın:

    > [!IMPORTANT]
    > Daha önce bir CDS veritabanı oluşturup şirketinizin üretim verilerini bu veritabanına girdiyseniz bu adımlar seçilen veritabanındaki şirketinizin üretim verileri de dahil olmak üzere **tüm** verileri siler.

    1. [PowerApps](https://preview.web.powerapps.com/home) uygulamasında oturum açın.
    2. Sağ üstteki açılır listede 2. adımda oluşturduğunuz ortamı seçin.
    3. Soldaki gezinme bölmesinde **Common Data Service**'i genişletin ve ardından **Varlıklar**'ı seçin.
    4. Sayfanın sağ tarafında, elips (**…**) düğmeyi seçin ve ardından **Tüm verileri temizle**'yi seçin.
    5. Verileri kaldırmak istediğinizi onaylamak için **Verileri sil**'i seçin. Bu eylem varsayılan olarak CDS'ye dahil edilen tüm demo verileri kaldırır. Ayrıca, seçilen veritabanına girilmiş olan diğer tüm bilgileri de kaldırır.

Artık yeni ortamınızı kullanabilirsiniz.

## <a name="grant-access-to-the-environment"></a>Ortama erişim izni verme
Varsayılan olarak, ortamı oluşturan genel yöneticinin ortama erişimi vardır. Ancak ek uygulama kullanıcılarına erişim izninin açıkça verilmesi gerekir. Erişim izni vermek için Ana İK ortamında [kullanıcılar ekleyin](../dev-itpro/sysadmin/tasks/create-new-users.md) ve [kullanıcılara uygun roller atayın](../dev-itpro/sysadmin/tasks/assign-users-security-roles.md). Attract ve Onboard uygulamalarına erişebilmeleri için bu kullanıcıları PowerApps ortamına da eklemeniz gerekir. Yordam burada özetlenmiştir. Adımları tamamlamak için yardım gereksiniminiz varsa [PowerApps yönetim merkezine giriş](https://powerapps.microsoft.com/en-us/blog/introducing-admin-center-for-powerapps/) başlıklı blog gönderisine bakın.

Bu yordam, Talent ortamını dağıtan genel yönetici tarafından tamamlanır.

1. [PowerApps Yönetim merkezi](https://preview.admin.powerapps.com/environments)'ni açın.
2. İlgili ortamları seçin.
3. **Güvenlik** sekmesinde gereken kullanıcıları **Ortam Oluşturucu** rolüne ekleyin.

Kullanıcıların PowerApps ortamına el ile eklendiği bu son adımın geçici olduğunu unutmayın. Sonuçta, kullanıcılar Ana İK'ya eklendiğinde otomatik olarak tamamlanacaktır.

