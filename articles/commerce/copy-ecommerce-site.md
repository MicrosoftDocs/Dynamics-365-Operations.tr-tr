---
title: E-ticaret sitesini kopyalama
description: Bu konuda, varolan bir e-ticaret sitesinin Microsoft Dynamics 365 Commerce site oluşturucuda e-ticaret ortamları içinde veya arasında nasıl kopyalanacağı açıklanmaktadır.
author: psimolin
ms.date: 03/03/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: psimolin
ms.search.validFrom: 2017-06-20
ms.openlocfilehash: 284a33099fecc5a8e8d5d5d31612abab51735773
ms.sourcegitcommit: 2e554371f5005ef26f8131ac27eb171f0bb57b4e
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/04/2022
ms.locfileid: "8386988"
---
# <a name="copy-an-e-commerce-site"></a>E-ticaret sitesini kopyalama

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]

Bu konuda, varolan bir e-ticaret sitesinin Microsoft Dynamics 365 Commerce site oluşturucuda e-ticaret ortamları içinde veya arasında nasıl kopyalanacağı açıklanmaktadır.

Dynamics 365 Commerce, Commerce site oluşturucuda siteleri kendi başına işlem olarak kopyalamayı veya klonlamalarını destekler. Siteler, tek bir e-ticaret ortamında veya iki e-ticaret ortamı arasında kopyalanabilir. Site kopyalama işlemini başlatan kullanıcının hem kaynak hem de hedef e-ticaret ortamlarında kiracı yöneticisi olması gerekir.

Site kopyalama işlemi, kaynak sitenin tüm e-ticaret içeriğini kopyalar. Bu içerik; sayfalar, parçalar, şablonlar, URL'ler ve varlıkları içerir. Yeni bir sitenin kullanılabilmesi için önce ilk çalıştırma deneyimi (FRE) işlemi aracılığıyla başlatılması gerekir. Kanallar, site oluşturucuda **Site Ayarları \> Kanallar** bölümünde eşlenebilir ve yönetilebilir.

Site kopyalama işleminin süresi esas olarak kaynak sitedeki varlık sayısına bağlıdır. Çok büyük siteler için, bunun yerine ortam kopyalama işlemini kullanmanızı öneririz. (Bu işlem, veri taşınabilirlik işlemi olarak da bilinir).

> [!NOTE]
> - Kaynak site, site kopyalama işlemi süresince salt okunur olacak.
> - Yalnızca belgelerin yayınlanmış sürümleri üzerine kopyalanır. Yayımlanmış sürüm yoksa, yalnızca en son sürümler üzerine kopyalanır.
> - İçerik için sürüm geçmişi hedef sitede kullanılamayacak.

## <a name="copy-a-site-within-an-e-commerce-environment"></a>Bir siteyi e-ticaret ortamı içinde kopyalama

Bir siteyi e-ticaret ortamı içinde kopyalamak için, aşağıdaki adımları izleyin.

1. Kopyalama işlemini gerçekleştirmek istediğiniz ortam için site oluşturucuda oturum açın.
1. Sağ üst köşedeki **Site değiştirici**'yi seçip ardından **Siteleri yönet**'i seçerek site listesini açın.
1. Kopyalamak veya klonlamak istediğiniz siteyi bulun ve site adının yanındaki onay kutusunu işaretleyerek bunu seçin.
1. Eylem Bölmesi'nde, **Siteyi kopyala**'yı seçin.
1. **Siteyi kopyala** iletişim kutusunda, **Yeni site** alanına yeni site için bir ad girin. Yeni site adı, e-ticaret ortamında benzersiz olmalıdır. **Kaynak kiracı** ve **Kaynak site** alanları otomatik olarak geçerli kiracı ve seçili site bilgilerine ayarlanır.
1. **Kopya oluştur**'u seçin.

Bilgiler doğrulandıktan sonra, yeni bir site kopyalama işinin oluşturulduğunu belirtir. İşin ilerleme durumunu, [**Kiracı işleri** sayfasının sağ bölmesinde](#monitor-the-site-copy-operation) takip edebilirsiniz. Kopyalama işlemi başarılı bir şekilde tamamlandığında yeni site, site listesi görünümündeki siteler listesinde görünür.

Aşağıdaki çizimde, site oluşturucuda **Site kopyalama** iletişim kutusu örneği gösterilmektedir.

![Site oluşturucudaki Site kopyalama iletişim kutusu.](media/site-copy_1.png)

## <a name="copy-a-site-between-two-e-commerce-environments"></a>İki e-ticaret ortamı arasında site kopyalama

İki e-ticaret ortamı arasında bir site kopyalamak için aşağıdaki adımları izleyin.

1. Hedef e-ticaret ortamı için site oluşturucuda oturum açın.
1. Eylem Bölmesi'nde, **Siteyi kopyala**'yı seçin.
1. **Siteyi kopyala** iletişim kutusunda, **Yeni site** alanına yeni site için bir ad girin. Yeni site adı, e-ticaret ortamında benzersiz olmalıdır.
1. **Kaynak kiracı** alanında, kaynak kiracının adını seçin.
1. **Kaynak site** alanında, kaynak siteyi seçin.
1. **Kopya oluştur**'u seçin.

> [!NOTE]
> Hem kaynak hem de hedef e-ticaret ortamları için kiracı yöneticisi izinleri gereklidir.

Bilgiler doğrulandıktan sonra, yeni bir site kopyalama işinin oluşturulduğunu belirtir. İşin ilerleme durumunu, [**Kiracı işleri** sayfasının sağ bölmesinde](#monitor-the-site-copy-operation) takip edebilirsiniz. Kopyalama işlemi başarılı bir şekilde tamamlandığında yeni site, site listesi görünümündeki siteler listesinde görünür.

## <a name="monitor-the-site-copy-operation"></a>Site kopya işlemini izleme

Site kopyalama işleminin ilerlemesini izlemek için aşağıdaki adımları izleyin.

1. Hedef e-ticaret ortamı için site oluşturucuda oturum açın.
1. Soldaki bölmede **Kiracı işleri**'ni seçin.
1. **Kiracı işleri** sayfasında, listeden site kopyalama işini bulun ve seçin. Sağda bir bölme görünür ve seçili işin durumunu ve ayrıntılarını gösterir.

Durumu **Devam ediyor** olan bir işi iptal edebilirsiniz. Listedeki işi seçin ve ardından Eylem Bölmesinde **İptal et**'i seçin.

Durumu **Başarısız** veya **Hatalarla tamamlandı** olan bir işi yeniden deneyebilirsiniz. Listedeki işi seçin ve ardından Eylem Bölmesinde **Yeniden dene**'yi seçin.

> [!NOTE]
> Bir site kopyalama işi tamamlandıktan sonra video varlıklarının işlenmesi devam edebilir.

Aşağıdaki şekilde, site oluşturucudaki **Kiracı işleri**'nin sağ bölmesinin örneği gösterilmektedir.

![Site oluşturucudaki Kiracı işleri sayfasının sağ bölmesindeki iş ayrıntıları.](media/site-copy_2.png)

## <a name="initialize-a-new-site-by-using-the-fre-process"></a>FRE işlemini kullanarak yeni bir site başlatma

Yeni sitenin kullanılabilmesi için önce FRE işlemi aracılığıyla başlatılması gerekir.

FRE işlemini kullanarak yeni bir siteyi başlatmak için, aşağıdaki adımları izleyin.

1. Yeni site için site oluşturucuda oturum açın.
1. Sağ üst köşedeki **Site değiştirici**'yi seçip ardından **Siteleri yönet**'i seçerek site listesini açın.
1. Başlatmak istediğiniz yeni siteyi bulup seçin.
1. **Sitenizi ayarlayın** iletişim kutusundaki **Etki alanı seçin** alanından bir etki alanı seçin. Başlatma sırasında e-ticaret ortamıyla ilişkilendirilmiş tüm etki alanları seçim için kullanılabilir.
1. **Varsayılan kanal seçin** alanında, ilişkilendirilmiş çevrimiçi mağaza kanalını seçin. Seçilen kanal sınıflamalar ve Commerce genel merkezinde depolanan diğer bilgileri sağlar.
1. **Varsayılan dili seçin** alanında, varsayılan yazma dilini seçin. Seçili çevrimiçi mağaza kanalı için yapılandırılmış tüm diller seçim için kullanılabilir.
1. **Yol** alanında değer, ana etki alanından ve girebileceğiniz isteğe bağlı bir URL yolundan oluşur. Kanal etki alanı kökünden sunulacaksa, veya daha sonra bu bilgileri site oluşturucuda kanal yapılandırması görünümüne girmek istiyorsanız URL yolunu boş bırakabilirsiniz. Site yolu, e-ticaret ortamında benzersiz olmalıdır.
1. **Tamam**'ı seçin. Site, sağladığınız bilgilerle başlatılır ve site yönetimi görünümüne yeniden gönderilir.

Aşağıdaki çizimde, site oluşturucuda **Sitenizi ayarlama** iletişim kutusu örneği gösterilmektedir.

![Site oluşturucudaki sitenizi oluşturma iletişim kutusu.](media/site-copy_3.png)

## <a name="additional-resources"></a>Ek kaynaklar

[Etki alanı adınızı yapılandırma](configure-your-domain-name.md)

[Yeni bir e-ticaret kiracısını dağıtma](deploy-ecommerce-site.md)

[Dynamics 365 Commerce sitesini çevrimiçi bir kanalla ilişkilendirme](associate-site-online-store.md)

[robots.txt dosyalarını yönetme](manage-robots-txt-files.md)

[URL yeniden yönlendirmelerini toplu olarak yükleme](upload-bulk-redirects.md)

[Commerce'ta B2C kiracısı ayarlama](set-up-b2c-tenant.md)

[Kullanıcı oturum açma işlemleri için özel sayfalar ayarlama](custom-pages-user-logins.md)

[Commerce ortamında birden fazla B2C kiracısı yapılandırma](configure-multi-b2c-tenants.md)

[İçerik teslim ağı (CDN) için destek ekleme](add-cdn-support.md)

[Konum tabanlı mağaza algılamayı etkinleştirme](enable-store-detection.md)
