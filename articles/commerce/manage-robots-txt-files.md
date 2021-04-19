---
title: robots.txt dosyalarını yönetme
description: Bu konuda, Microsoft Dynamics 365 Commerce'te robots.txt dosyalarının nasıl yönetileceği açıklanmaktadır.
author: BrianShook
ms.date: 07/02/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: retail
ms.author: brshoo
ms.search.validFrom: 2019-12-18
ms.dyn365.ops.version: ''
ms.openlocfilehash: b9b832d6714447f8957095c8c87d48527087f12d
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/31/2021
ms.locfileid: "5794247"
---
# <a name="manage-robotstxt-files"></a>robots.txt dosyalarını yönetme

[!include [banner](includes/banner.md)]

Bu konuda, Microsoft Dynamics 365 Commerce'te robots.txt dosyalarının nasıl yönetileceği açıklanmaktadır.

Robotlar özel durum standardı veya robots.txt, Web sitelerinin ağ robotları ile iletişim kurmak için kullandığı standarttır. Web robotları bir Web sitesinin herhangi bir alanını ziyaret etmemesini söyler. Robotlar, Web sitelerinin dizinini oluşturmada genellikle arama motorları tarafından kullanılır.

Robotları bir sunucudan dışlamak için, sunucuda bir dosya oluşturursunuz. Bu dosyada, robotlar ile ilgili bir erişim ilkesi belirtirsiniz. Dosya, **/robots.txt** yerel URL'sinde http aracılığıyla erişilebilir olmalıdır. Robots.txt dosyası, arama alt yapılarının sitenizdeki içeriği dizine almanıza yardımcı olur.

Dynamics 365 Commerce etki alanınız için robots.txt dosyasını karşıya yüklemenize olanak tanır. Commerce ortamınızdaki her etki alanı için bir robots.txt dosyası karşıya yükleyebilir ve bu etki alanıyla ilişkilendirebilirsiniz.

Robots.txt dosyası hakkında daha fazla bilgi için [Web robots sayfalarını](https://www.robotstxt.org/) ziyaret edin.

## <a name="upload-a-robotstxt-file"></a>Robots.txt dosyasını karşıya yükleme

Robots.txt dosyanızı [robots dışlama standardına](https://www.robotstxt.org/orig.html) göre oluşturup düzenledikten sonra, Commerce geliştirme araçlarını kullanacağınız bilgisayarda dosyaya erişilebildiğinden emin olun. Dosya **robots.txt** olarak adlandırılmalıdır. En iyi sonuçlar için, bu, standart olarak belirtilen biçimde olmalıdır. Her bir Commerce müşterisi, robots.txt dosyasının içeriğini doğrulamadan ve korumadan sorumludur. Robots.txt dosyasını karşıya yüklemek için, Commerce'te sistem yöneticisi olarak oturum açmanız gerekir.

Bir robots.txt dosyasını ticari olarak karşıya yüklemek için aşağıdaki adımları izleyin.

1. Commerce'te sistem yöneticisi olarak oturum açın.
2. Sol gezinti bölmesinde, genişletmek için **Kiracı Ayarlarını** seçin (dişli simgesinin yanında).
3. **Kiracı ayarları** altında **robots.txt** dosyasını seçin. Ortamınız ile ilişkilendirilmiş tüm etki alanlarının listesi pencerenin ana bölümünde görüntülenir.
4. Ortamınızdaki bir etki alanı için robots.txt dosyası yüklemek için **Yönet**'i seçin.
5. Sağdaki menüde, robots.txt dosyasıyla ilişkilendirilmiş etki alanının yanında bulunan **Yükle** düğmesini (yukarı yönlü ok) seçin. Bir dosya tarayıcısı iletişim kutusu görüntülenir.
6. İletişim kutusunda, ilişkili etki alanı için karşıya yüklemek istediğiniz robots.txt dosyasını bulup seçin ve sonra yüklemeyi tamamlamak için **Aç**'ı seçin.

> [!NOTE] 
> Karşıya yükleme sırasında, Commerce dosyanın bir metin dosyası olduğunu doğrular, ancak dosyanın içeriğini doğrulamaz.

## <a name="download-a-robotstxt-file"></a>Robots.txt dosyasını indirme

Bir robots.txt dosyasını ticari olarak indirmek için aşağıdaki adımları izleyin.

1. Commerce'te sistem yöneticisi olarak oturum açın.
2. Sol gezinti bölmesinde, genişletmek için **Kiracı Ayarlarını** seçin (dişli simgesinin yanında).
3. **Kiracı ayarları** altında **robots.txt** dosyasını seçin. Ortamınız ile ilişkilendirilmiş tüm etki alanlarının listesi pencerenin ana bölümünde görüntülenir.
4. Ortamınızdaki bir etki alanı için robots.txt dosyası indirmek için **Yönet**'i seçin.
5. Sağdaki menüde, robots.txt dosyasıyla ilişkilendirilmiş etki alanının yanında bulunan **İndir** düğmesini (aşağı yönlü ok) seçin. Bir dosya tarayıcısı iletişim kutusu görüntülenir.
6. İletişim kutusunda, yerel sürücünüzde istediğiniz konuma gidin, bir dosya adı doğrulayın veya girin ve karşıdan yüklemeyi tamamlamak için **Kaydet**'i seçin.

> [!NOTE]
> Bu yordam, daha önce Commerce geliştirme araçlarıyla karşıya yüklenen robots.txt dosyalarını karşıdan yüklemek için kullanılabilir.

## <a name="delete-a-robotstxt-file"></a>Robots.txt dosyasını silme

Bir robots.txt dosyasını ticari olarak silmek için aşağıdaki adımları izleyin.

1. Commerce'te sistem yöneticisi olarak oturum açın.
2. Sol gezinti bölmesinde, genişletmek için **Kiracı Ayarlarını** seçin (dişli simgesinin yanında).
3. **Kiracı ayarları** altında **robots.txt** dosyasını seçin. Ortamınız ile ilişkilendirilmiş tüm etki alanlarının listesi pencerenin ana bölümünde görüntülenir.
4. Ortamınızdaki bir etki alanı için robots.txt dosyası silmek için **Yönet**'i seçin.
5. Sağdaki menüde, robots.txt dosyasıyla ilişkilendirilmiş etki alanının yanında bulunan **Sil** düğmesini (çöp kutusu simgesi) seçin. Bir dosya tarayıcı penceresi görünür.
6. Dosya tarayıcı penceresinde, ilişkili etki alanı için silmek istediğiniz robots.txt dosyasını bulup seçin ve sonra **Aç**'ı seçin. Bir uyarı iletisi kutusu görüntülenir.
7. Robots.txt dosyasının silinmesini onaylamak için, ileti kutusunda, **Sil**'i seçin.

> [!NOTE] 
> Bu yordam, daha önce Commerce geliştirme araçlarıyla karşıya yüklenen robots.txt dosyalarını silmek için kullanılabilir.

## <a name="additional-resources"></a>Ek kaynaklar

[Etki alanı adınızı yapılandırma](configure-your-domain-name.md)

[Yeni bir e-ticaret kiracısını dağıtma](deploy-ecommerce-site.md)

[E-ticaret sitesi oluşturma](create-ecommerce-site.md)

[Dynamics 365 Commerce sitesini çevrimiçi bir kanalla ilişkilendirme](associate-site-online-store.md)

[URL yeniden yönlendirmelerini toplu olarak yükleme](upload-bulk-redirects.md)

[Commerce'ta B2C kiracısı ayarlama](set-up-B2C-tenant.md)

[Kullanıcı oturum açma işlemleri için özel sayfalar ayarlama](custom-pages-user-logins.md)

[Commerce ortamında birden fazla B2C kiracısı yapılandırma](configure-multi-B2C-tenants.md)

[İçerik teslim ağı (CDN) için destek ekleme](add-cdn-support.md)

[Konum tabanlı mağaza algılamayı etkinleştirme](enable-store-detection.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
