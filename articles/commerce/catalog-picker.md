---
title: Katalog seçicisi modülü
description: Bu makalede katalog seçici modülleri ele alınır ve bunların Microsoft Dynamics 365 Commerce işletmeler arası (B2B) e-ticaret sitelerine nasıl ekleneceği açıklanır.
author: ashishmsft
ms.date: 07/11/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: asharchw
ms.search.validFrom: 2022-04-21
ms.openlocfilehash: 642319eea7e40415fd32898f6ec07bfc86f3b1b1
ms.sourcegitcommit: d1491362421bf2fcf72a81dc2dc2d13d3b98122b
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/11/2022
ms.locfileid: "9136953"
---
# <a name="catalog-picker-module"></a>Katalog seçicisi modülü

[!include [banner](includes/banner.md)]

Bu makalede katalog seçici modülleri ele alınır ve bunların Microsoft Dynamics 365 Commerce işletmeler arası (B2B) e-ticaret sitelerine nasıl ekleneceği açıklanır.

Katalog seçici modülü, B2B site kullanıcılarının kullanabildiği tüm ürün kataloglarını listelemek için kullanılan özel bir kapsayıcıdır. Birden çok katalog şu anda yalnızca B2B siteleri için desteklenir.

Aşağıdaki şekilde bir katalog seçici modülü örneği gösterilmiştir.

![Üç ürün katalogunu listeleyen bir katalog seçici modülü örneği.](./media/Catalog-picker-sample.png)

## <a name="add-a-catalog-picker-module-to-your-site"></a>Sitenize katalog seçici modülü ekleme

Commerce site oluşturucuda sitenize bir katalog seçici modülü eklemek için aşağıdaki adımları izleyin.

### <a name="create-a-catalog-picker-page"></a>Katalog seçici sayfası oluşturma

Öncelikle bir katalog seçici sayfası oluşturun.

1. **Sayfalar**'a gidin ve yeni sayfa oluşturmak için **Yeni**'yi seçin.
1. **Yeni sayfa oluştur** iletişim kutusundaki **Sayfa adı** bölümünde, **Katalog seçici**'yi girin.
1. **Sayfa URL**'si altında sayfa için bir URL girin ve ardından **İleri**'yi seçin.

    ![Yeni bir sayfa oluştur iletişim kutusu.](./media/Create-catalog-picker-page.png)

1. **Şablon seç** bölümünde, **Genel içerik** öğesini seçin ve ardından **İleri**'yi seçin.
1. **Düzen seç** bölümünde, **Esnek düzen**'i seçin ve ardından **İleri**'yi seçin.
1. **İnceleyin ve bitirin** bölümünde, sayfa yapılandırmasını gözden geçirin. Sayfa bilgilerini düzenlemeniz gerekiyorsa **Geri**'yi seçin. Sayfa bilgileri doğruysa, **Sayfa oluştur**'u seçin.
1. **Katalog seçici** altında, **Ana yuvayı** seçin, üç nokta düğmesini (**...**) ve ardından **Modül ekle**'yi seçin.

    ![Katalog seçici altına Ana yuvaya modül ekleme.](./media/Author-web-page-catalog-picker-1.png)

1. **Modül seç** iletişim kutusunda **Konteyner** modülünü seçin ve **Tamam**'ı seçin.
1. **Konteyner** alanını seçin, üç nokta (**...**) düğmesini seçin ve **Modül ekle**'yi seçin.
1. **Modülleri seç** iletişim kutusunda **Katalog seçici** modülünü seçin ve **Tamam**'ı seçin.
1. **Katalog seçici** özellikleri bölmesinde, **Başlık** altında, **Kataloglar** öğesini seçin ve ardından katalog seçici sayfası için bir başlık girin.
1. **Başlık düzeyi** altında başlık düzeyi seçin ve ardından **Tamam** öğesini seçin.
1. **Zengin metin**, altında katalog seçici sayfasının üst kısmında görünecek metni girin.
1. **Kaydet**'i seçin, sayfayı iade etmek için **Düzenlemeyi bitir**'i ve ardından yayımlamak için **Yayımla**'yı seçin.

### <a name="add-a-link-on-your-account-page"></a>Hesap sayfanıza bağlantı ekleyin

Sonra, **Hesabım** sayfasındaki katalog seçici sayfanıza bir referans ekleyin.

1. **Sayfalar** bölümüne gidin, sitenizin **Hesabım** sayfasını bulup seçin ve **Düzenle**'yi seçin.
1. Sayfanın **Ana** yuvası altında, **Hesap jenerik kutucuğu** yuvasını seçin. 
1. **Hesap genel kutucuğu** özellikleri bölmesinde, **Bağlantılar** altında, **Eylem bağlantısını ekle**'yi seçin ve ardından **Eylem bağlantısı**'nı seçin.
1. **Eylem bağlantısı** iletişim kutusunda, **Bağlantı metni** altında, katalog seçici sayfasına bağlantı için bağlantı metni girin.
1. **Bağlantı hedefi** altında, **Bağlantı ekle**'yi seçin.
1. **Bağlantı ekle** iletişim kutusunda **Özel sayfa**'yı seçin ve sonra **İleri**'yi seçin.
1. **Ad** altında, katalog seçici sayfanızı seçin, **Uygula**'yı seçin ve ardından **Tamam** öğesini seçin.
1. **Kaydet**'i seçin, sayfayı iade etmek için **Düzenlemeyi bitir**'i ve ardından yayımlamak için **Yayımla**'yı seçin.

Aşağıdaki şekilde katalog sayfasına referans içeren bir hesap sayfası örneği gösterilmektedir.

![Katalogda bağlantı içeren hesaplar sayfası.](./media/my-accounts.png)

### <a name="add-a-link-from-the-header"></a>Başlıktan bir bağlantı ekleme

Son olarak sitenizin üst bilgisinden kataloglarınıza bir bağlantı ekleyin.

1. **Parçalar** bölümüne gidin, sitenizin üst bilgi parçasını bulup seçin ve **Düzenle**'yi seçin.
1. **Üstbilgi** yuvasını seçin. 
1. **Üst bilgi** özellikleri bölmesinde, **Hesap bağlantılarım** altında, **Eylem bağlantısını ekle**'yi seçin ve ardından **Eylem bağlantısı**'nı seçin.
1. **Eylem bağlantısı** iletişim kutusunda, **Bağlantı metni** altında, katalog seçici sayfasına bağlantı için bağlantı metni girin.
1. **Bağlantı hedefi** altında, **Bağlantı ekle**'yi seçin.
1. **Bağlantı ekle** iletişim kutusunda **Özel sayfa**'yı seçin ve sonra **İleri**'yi seçin.
1. **Ad** altında, katalog seçici sayfanızı seçin, **Uygula**'yı seçin ve ardından **Tamam** öğesini seçin.
1. **Kaydet**'i seçin, başlık parçasını iade etmek için **Düzenlemeyi bitir**'i ve ardından yayımlamak için **Yayımla**'yı seçin.

Aşağıdaki şekilde B2B kataloğuna bağlantı içeren bir e-ticaret web sitesi üst bilgisi örneği gösterilmektedir.

![Kataloğa açılır bir bağlantı içeren e-ticaret web sitesi üst bilgisi.](./media/catalog-in-header.png)


## <a name="additional-resources"></a>Ek kaynaklar 

[B2B siteleri için ticari Katalog oluştur](catalogs-b2b-sites.md)

[B2B özelleştirmeleri için Commerce kataloglarının genişletilebilirlik etkisi](catalogs-b2b-sites-dev.md)

[B2B için Commerce katalog hakkında SSS](catalogs-b2b-sites-FAQ.md)

[Hesap yönetimi sayfaları ve modülleri](account-management.md)

[Üst bilgi modülü](author-header-module.md)
