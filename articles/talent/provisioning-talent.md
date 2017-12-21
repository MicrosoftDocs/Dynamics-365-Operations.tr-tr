---
title: "Microsoft Dynamics 365 for Talent sağlama"
description: "Bu konuda, Microsoft Dynamics 365 for Talent için yeni bir ortam sağlama işlemi adım adım anlatılmaktadır."
author: rschloma
manager: AnnBe
ms.date: 11/20/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: Talent
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
ms.sourcegitcommit: 6ffb97b53f522cfe8ccd8e89df854cbc557e4f1f
ms.openlocfilehash: fadc373b2c1c06987f22d4d9c20a9ab07b0c85d5
ms.contentlocale: tr-tr
ms.lasthandoff: 11/20/2017

---
# <a name="provision-microsoft-dynamics-365-for-talent"></a>Microsoft Dynamics 365 for Talent sağlama
Bu konuda, Microsoft Dynamics 365 for Talent için yeni bir ortam sağlama işlemi adım adım anlatılmaktadır. Bu konuda, Talent'ı bir Bulut Çözümü Sağlayıcısı (CSP) veya kurumsal mimari (EA) sözleşmesi aracılığıyla aldığınız varsayılır. Zaten Talent hizmet planını içeren mevcut bir Microsoft Dynamics 365 lisansınız varsa ve bu konudaki adımları tamamlayamıyorsanız Destek birimine başvurun.

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

    Yeni ortamınız, soldaki gezinti bölmesinde bulunan ortam listesinde görüntülenir. Bununla birlikte, dağıtım durumunu **Dağıtıldı** olarak güncelleştirilene kadar ortamı kullanmaya başlayamazsınız. Tipik olarak bu işlem birkaç dakika sürebilir. Sağlama başarısız olursa, Desteğe başvurmanız gerekir.

6. Yeni ortamı kullanmak için **Talent'ta oturum aç**'ı seçin.

> [!NOTE]
> Son gereksinimleri henüz yerine getirmediyseniz, projede Talent'ın bir test kurulumunu dağıtabilirsiniz. Ardından imzalayana kadar bu kurulumu kullanarak çözümünüzü test edebilirsiniz. Yeni ortamınızı test için kullanıyorsanız, bir üretim ortamı oluşturmak için bu yordamı yinelemeniz gerekir.

## <a name="create-a-new-powerapps-environment-if-required"></a>Yeni bir PowerApps ortamı oluşturma (gerekirse)
1. LCS'de **Ortamları Yönet**'i seçin. Mevcut ortamları görebileceğiniz ve yeni ortamlar oluşturabileceğiniz [PowerApps Yönetici Merkezi](https://preview.admin.powerapps.com/environments)'ne yönlendirilirsiniz.
2. (**+**) **Yeni ortam** düğmesini seçin.
3. Ortam için benzersiz bir ad girin ve dağıtmak için konum seçin.

    > [!NOTE]
    > Talent tüm bölgelerde kullanılamaz. Bu nedenle, ortamınız için konum seçmeden önce kullanılabilirliği kontrol ettiğinizden emin olun.

4. Bir veritabanı oluşturmak isteyip istemediğiniz sorulduğunda, Talent verilerinizi barındıracak olan bir Common Data Service (CDS) veritabanı oluşturmak için **Veritabanı oluştur**'u seçin. Bir veritabanı oluşturarak, PowerApps uygulamalarını Talent ile tümleştirebilirsiniz.
5. Veritabanı için kullanmak istediğiniz erişim düzeyi sorulur. **Erişimi kısıtla** seçeneğini belirlemenizi öneririz. Çünkü bu seçenek Talent kullanıcılarının PowerApps uygulamasını kullanarak hassas verilere doğrudan erişimini engeller.
6. Oluşturulan CDS veri tabanı demo veriler içerir. Demo veriler yararlıdır. Demo veri şirketini test için veya görev kayıtları ya da görev kılavuzları oluşturmak üzere kullanabilirsiniz. Ancak, demo veriler, üretim ortamınıza, diğer bilgilerin yanında etkin olmayan personel ve sahte adresler ekler. Demo verileri kaldırmak için, CDS veritabanını oluşturmayı tamamladıktan sonra aşağıdaki adımları uygulayın:

    > [!IMPORTANT]
    > Daha önce bir CDS veritabanı oluşturup şirketinizin üretim verilerini bu veritabanına girdiyseniz, bu adımların seçilen veritabanındaki şirketinizin üretim verileri de dahil olmak üzere **tüm** adımları sileceğini unutmayın.

    1. [PowerApps](https://preview.web.powerapps.com/home)'te oturum açın ve adım 2'de oluşturduğunuz ortama gidin.
    2. **Varlıklar**'ı seçin. Sayfanın sağ tarafında, elips (**…**) düğmeyi seçin ve ardından **Tüm verileri temizle**'yi seçin.
    3. Verileri kaldırmak istediğinizi onaylamak için **Verileri sil**'i seçin. Bu eylem varsayılan olarak CDS'ye dahil edilen tüm demo verileri kaldırır. Ayrıca, seçilen veritabanına girilmiş olan diğer tüm bilgileri de kaldırır.

Artık yeni ortamınızı kullanabilirsiniz.
