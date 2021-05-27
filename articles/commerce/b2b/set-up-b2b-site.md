---
title: B2B e-ticaret sitesi ayarlama
description: Bu konuda, Microsoft Dynamics 365 Commerce'te nasıl bir işletmeden işletmeye (B2B) e-ticaret sitesi kurulacağı açıklanmaktadır.
author: josaw1
ms.date: 04/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RetailOperations
audience: Application User, IT Pro
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: retail
ms.author: josaw
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 461e79f63569bbfe77f9075c562a5b1f3da28cc2
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/11/2021
ms.locfileid: "6018867"
---
# <a name="set-up-a-b2b-e-commerce-site"></a>B2B e-ticaret sitesi ayarlama

[!include [banner](../../includes/banner.md)]
[!include [banner](../../includes/preview-banner.md)]

İşletmeler arası (B2B) e-ticaret siteleri, B2B kullanıcısı için iş akışını iyileştiren bazı önemli özellikler sağlar. Bu konuda, Microsoft Dynamics 365 Commerce'te nasıl B2B e-ticaret sitesi kurulacağı açıklanmaktadır. B2B'ye özgü senaryoları etkinleştirmek için yapılandırılması gereken modüller ve site ayarları anlatılmaktadır.

## <a name="prerequisites"></a>Önkoşullar

- B2B e-ticaret sitesi kurmak için bu konuda açıklandığı gibi Commerce Headquarters'da belirli özellikleri etkinleştirmeniz ve yapılandırmanız gerekir.
- Ürün bulma, ürün ayrıntıları sayfaları, sepet ve ödeme gibi temel deneyimler, işletmeden tüketiciye (B2C) e-ticaret siteleri için kullanılan modüllerle desteklenir. Site yazarları, Dynamics 365 Commerce'ün desteklediği tüm modüllere aşina olmalıdır. Daha fazla bilgi için bkz. [Modül kitaplığına genel bakış](../starter-kit-overview.md).
- Bu konu, site yazarlarının e-ticaret sitelerine yönelik B2B özelliklerini etkinleştirebilmeleri için Commerce Site Builder, şablonlar, parçalar ve sayfalarla ilgili temel bilgileri bildiğini varsayar.

## <a name="site-level-settings"></a>Site düzeyi ayarlar

Site düzeyi ayarlara site oluşturucudan, **Site Ayarları \> Uzantılar**'dan erişebilirsiniz. B2B senaryoları için aşağıdaki iki site düzeyi ayar geçerlidir:

- **Müşteri hesabı ödemelerini etkinleştir**: Bu özellik, kullanıcıların müşteri hesaplarını kullanarak siparişler için ödeme yapmalarını sağlar. Kullanılabilir değerler **B2B müşterileri için etkin**, **B2C müşterileri için etkin**, **Tüm müşteriler için etkin** ve **Tüm müşteriler için devre dışı** şeklindedir. B2B siteniz müşteri hesaplarını destekliyorsa, **B2C müşterileri için etkin**'i seçmelisiniz.
- **Sipariş miktarı limitlerini etkinleştir**: Bu özellik, her ürün veya kategori için sipariş edilebilen madde sayısına yönelik limitler belirlemenizi sağlar. Kullanılabilir değerler **B2B müşterileri için etkin**, **B2C müşterileri için etkin**, **Tüm müşteriler için etkin** ve **Tüm müşteriler için devre dışı** şeklindedir.

> [!NOTE]
> Modül kitaplığının en son sürümüne geçiş yaptığınızda, daha önce açıklanan site ayarlarının ortamınızda kullanılabilir olduğundan emin olmak için ek adımları izlemeniz gerekir. Daha fazla bilgi için bkz. [app.settings.json dosyasını güncelleştirme](../e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file).

## <a name="create-business-partner-sign-up-pages"></a>İş ortağı kayıt sayfaları oluşturma

İş ortağı olmak için kullanıcıların önce bir iş ortağı isteği göndermesi gerekir. Kullanıcıların işlemi başlatabilmesi için B2B giriş sayfasında iş ortağı isteği sayfasına bir bağlantı sunulacaktır. Kullanıcılar bir iş ortağı isteği gönderdikten sonra, isteğin gönderildiğine dair onay alırlar. 

### <a name="create-a-business-partner-request-page"></a>İş ortağı isteği sayfası oluşturma

Bir iş ortağı isteği sayfasındaki **İş Ortağı Kaydı** modülü, kullanıcıların iş ortağı olma isteklerini başlatmak için kullanılır. Bu modül, kayıt işlemi için gereken kullanıcı bilgilerini toplamanızı sağlar. Ayrıca, **İşletme hesap adresi** modülü, kullanıcının adresini yakalamak için kullanılır.

Site oluşturucuda iş ortağı istek sayfasını ayarlamak ve yapılandırmak için şu adımları izleyin.

1. **Kayıt** adında bir şablon oluşturun. Bu şablon aşağıdaki modülleri içermelidir:

    - İş ortağı kaydı
    - İçerik haritası
    - Üst bilgi
    - Alt bilgi
    - İçerik bloğu
    - Metin bloğu
    - Ürün topluluğu

1. **İş Ortağı İsteği** adlı bir sayfa oluşturmak için **Kayıt** şablonunu kullanın.
1. **Üst bilgi** yuvasına, site üst bilgisiyle önceden yapılandırılmış üst bilgi parçasını ekleyin.
1. **Alt bilgi** yuvasına, site alt bilgisiyle önceden yapılandırılmış alt bilgi parçasını ekleyin.
1. **Ana** yuvasına bir **Kapsayıcı** modülü ekleyin. Modülün özellikler bölmesinde, **Genişlik** değerini **Dolgu Kapsayıcısı** olarak ayarlayın.
1. **Kapsayıcı** yuvasına bir **İçerik haritası** modülü ekleyin. Modül özellikleri bölmesinde, **Bağlantılar** altında, giriş sayfası bağlantısı yapılandırın ve bağlantı metni olarak **Giriş** girin.
1. **Kapsayıcı** yuvasında **İçerik haritası** modülünün altına bir **İş ortağı kaydı** modülü ekleyin. Modül özellikleri bölmesinde, **Başlık** altına **İş ortağı olun** girin.
1. **İş ortağı kaydı** yuvasında bir **İşletme hesabı adresi** modülü ekleyin.
1. **Kapsayıcı** yuvasında, **İş ortağı kaydı** modülünün altına bir **Metin bloğu** modülü ekleyin. Burada, kayıt işlemi için bazı hüküm ve koşullar tanımlayabilirsiniz.
1. **Kaydet**'i seçin ve ardından sayfayı önizlemek için **Önizleme**'yi seçin.
1. **Kaydet**'i seçin, sayfayı iade etmek için **Düzenlemeyi bitir**'i ve ardından yayımlamak için **Yayımla**'yı seçin.
1. Sayfanın URL'sini yayınlayın.

### <a name="create-a-business-partner-request-confirmation-page"></a>İş ortağı istek onayı sayfası oluşturma

Bir iş ortağı isteği gönderildikten sonra, gönderimi onaylamak için kullanıcıya bir onay sayfası gösterilmelidir. 

Site oluşturucuda istek onay sayfasını ayarlamak ve yapılandırmak için şu adımları izleyin.

1. **İş Ortağı İstek Onayı** adlı bir sayfa oluşturmak için az önce oluşturduğunuz **Kayıt** şablonunu kullanın.
1. **Üst bilgi** yuvasına, site üst bilgisiyle önceden yapılandırılmış üst bilgi parçasını ekleyin.
1. **Alt bilgi** yuvasına, site alt bilgisiyle önceden yapılandırılmış alt bilgi parçasını ekleyin.
1. **Ana** yuvasına bir **Kapsayıcı** modülü ekleyin. Modülün özellikler bölmesinde, **Genişlik** değerini **Dolgu Kapsayıcısı** olarak ayarlayın.
1. **Kapsayıcı** yuvasında bir **İçerik bloğu** modülü ekleyin. Modül özellikleri bölmesinde, **Başlık** altında, **İstek gönderildi** girin. **Zengin Metin** alanına **İsteğiniz gönderildi** girin. **Bağlantılar** altında, giriş sayfasına bir bağlantı yapılandırın ve bağlantı metni olarak **Alışverişe geri dön** girin.
1. Başka bir **Kapsayıcı** modülü ekleyin ve bir **Ürün Koleksiyonu** modülü ekleyin.
1. **Ürün Koleksiyonu** modülünü sayfada sergilemek istediğiniz öneri veya kategori listesiyle yapılandırın.
1. **Kaydet**'i seçin ve ardından sayfayı önizlemek için **Önizleme**'yi seçin.
1. **Kaydet**'i seçin, sayfayı iade etmek için **Düzenlemeyi bitir**'i ve ardından yayımlamak için **Yayımla**'yı seçin.
1. Sayfanın URL'sini yayınlayın.

Site oluşturucuda istek onay sayfasına bağlantı eklemek için şu adımları izleyin.

1. Daha önce oluşturduğunuz **İş Ortağı İsteği** sayfasına gidin ve **Düzenle**'yi seçin. 
1. **İş ortağı kaydı** modülü yuvasını seçin. Özellikler bölmesinde, **Kayıt Onayı sayfası bağlantısı** altında, daha önce oluşturduğunuz iş ortağı istek sayfası bağlantısını yapılandırın. 
1. **Kaydet**'i seçin, sayfayı iade etmek için **Düzenlemeyi bitir**'i ve ardından yayımlamak için **Yayımla**'yı seçin.

### <a name="add-a-business-partner-request-link-to-the-home-page"></a>Giriş sayfasına iş ortağı isteği bağlantısı ekleme

İş ortağı isteği kayıt ve onay sayfaları oluşturulduktan sonra, kayıt sayfasını giriş sayfasındaki bir bağlantı aracılığıyla erişilebilir hale getirmeniz gerekir. Bu görevi, giriş sayfasındaki herhangi bir **İçerik bloğu** modülüne bağlantı ekleyerek tamamlayabilirsiniz.

Site oluşturucuda giriş sayfasına iş ortağı isteği bağlantısı eklemek için şu adımları izleyin.

1. Sitenizin giriş sayfasına gidin ve **Düzenle**'yi seçin.
1. Bir **İçerik bloğu** modül yuvası seçin. Modül özellikleri bölmesinde, **Bağlantılar** altında, daha önce oluşturduğunuz iş ortağı isteği sayfası bağlantısı yapılandırın ve **İş ortağı olmak için kaydolun** veya bağlantı metniyle benzer bir metin girin. Uygun bir resim ekleyin.
1. **Kaydet**'i seçin, sayfayı iade etmek için **Düzenlemeyi bitir**'i ve ardından yayımlamak için **Yayımla**'yı seçin.

## <a name="account-management-landing-page"></a>Hesap yönetimi giriş sayfası

Hesap yönetimi açılış sayfası, hem B2B hem de B2C e-ticaret siteleri için gerekli olan tüm hesap yönetimi bilgilerini içerir. Bu sayfayı yalnızca oturum açabilen kullanıcılar görüntüleyebilir.

Site oluşturucuda bir B2B hesap yönetimi açılış sayfası oluşturmak ve yapılandırmak için şu adımları izleyin.

1. **Hesap yönetimi** adında bir şablon oluşturun. Bu şablon aşağıdaki modülleri içermelidir:

    - Üst bilgi
    - Alt bilgi
    - İçerik haritası
    - Hesap karşılama kutucuğu
    - Hesap genel kutucuğu
    - Hesap Adresi kutucuğu
    - Hesap istek listesi kutucuğu
    - Hesap adres kutucuğu
    - Hesap bağlılık programı kutucuğu
    - Hesap müşteri bakiyesi kutucuğu
    - Hesap sipariş şablonları kutucuğu
    - Kuruluş kullanıcıları
    - İşletme organizasyonu listesi
    - Müşteri hesabı bakiyesi
    - Sipariş şablonu satırları
    - Sipariş şablonu listesi
    - Hesap faturası kutucuğu
    - Fatura listesi
    - Fatura ayrıntıları

1. **Hesabım** adlı bir sayfa oluşturmak için **Hesap yönetimi** şablonunu kullanın.
1. **Üst bilgi** yuvasına, site üst bilgisiyle önceden yapılandırılmış üst bilgi parçasını ekleyin.
1. **Alt bilgi** yuvasına, site alt bilgisiyle önceden yapılandırılmış alt bilgi parçasını ekleyin.
1. **Ana** yuvasına bir **Kapsayıcı** modülü ekleyin. Modülün özellikler bölmesinde, **Genişlik** değerini **Dolgu Kapsayıcısı** olarak ayarlayın. 
1. **Kapsayıcı** yuvasına bir **İçerik haritası** modülü ekleyin. Modül özellikleri bölmesinde, **Bağlantılar** altında, giriş sayfası bağlantısı yapılandırın ve bağlantı metni olarak **Giriş** girin.
1. **Kapsayıcı** yuvasında bir **Hoş geldiniz kutucuğu** modülü ekleyin. Modül özellikleri bölmesinde, **Başlık** altında, **Hoş Geldiniz** girin.
1. **Ana** yuvaya başka bir **Kapsayıcı** modülü (**Kapsayıcı 2**) ekleyin. Modülün özellikler bölmesinde, **Genişlik** değerini **Dolgu Kapsayıcısı** olarak ayarlayın. **Gösterilen Alt Öğeler** değerini **İki** olarak ayarlayın. 
1. **Kapsayıcı 2** yuvasına bir **Hesap genel kutucuğu** modülü ekleyin. Modül özellikleri bölmesinde, **Başlık** altında **Profilim** girin. **Bağlantılar** altında, **Profilim** sayfası bağlantısı yapılandırın. 
1. **Kapsayıcı 2** yuvasına başka bir **Hesap genel kutucuğu** modülü ekleyin. Modül özellikleri bölmesinde, **Başlık** altında **Sipariş geçmişi** girin. **Bağlantılar** altında, sipariş geçmişi sayfası bağlantısı yapılandırın.
1. **Ana** yuvaya başka bir **Kapsayıcı** modülü (**Kapsayıcı 3**) ekleyin. Modülün özellikler bölmesinde, **Genişlik** değerini **Dolgu Kapsayıcısı** olarak ayarlayın. **Gösterilen Alt Öğeler** değerini **İki** olarak ayarlayın. 
1. **Kapsayıcı 3** yuvasına bir **Hesap adresi kutucuğu** modülü ekleyin. Modül özellikleri bölmesinde, **Başlık** altında **Adresim** girin. **Bağlantılar** altında, **Adresim** sayfasına bir bağlantı yapılandırın. 
1. **Kapsayıcı 3** yuvasına bir **Hesap istek listesi kutucuğu** modülü ekleyin. Modül özellikleri bölmesinde, **Başlık** altında **İstek Listem** girin. **Bağlantılar** altında, **İstek Listem** sayfasına bir bağlantı yapılandırın.
1. **Ana** yuvaya başka bir **Kapsayıcı** modülü (**Kapsayıcı 4**) ekleyin. Modülün özellikler bölmesinde, **Genişlik** değerini **Dolgu Kapsayıcısı** olarak ayarlayın. **Gösterilen Alt Öğeler** değerini **İki** olarak ayarlayın. 
1. **Kapsayıcı 4** yuvasına bir **Kuruluş kullanıcıları** modülü ekleyin. Modül özellikleri bölmesinde, **Başlık** altında **Kuruluş Kullanıcıları** girin. 
1. **Kapsayıcı 4** yuvasına bir **Hesap müşteri bakiyesi kutucuğu** modülü ekleyin. Modül özellikleri bölmesinde, **Başlık** altında, **Hesap kredisi** girin. 
1. **Ana** yuvaya başka bir **Kapsayıcı** modülü (**Kapsayıcı 5**) ekleyin. Modülün özellikler bölmesinde, **Genişlik** değerini **Dolgu Kapsayıcısı** olarak ayarlayın. **Gösterilen Alt Öğeler** değerini **İki** olarak ayarlayın. 
1. **Kapsayıcı 5** modülüne bir **Hesap siparişi şablonları kutucuğu** modülü ekleyin. Modül özellikleri bölmesinde, **Başlık** altında **Sipariş Şablonları** girin. 
1. **Kaydet**'i seçin, sayfayı iade etmek için **Düzenlemeyi bitir**'i ve ardından yayımlamak için **Yayımla**'yı seçin.

> [!NOTE] 
> 13 ile 18 arasındaki adımlarda eklediğiniz bazı bölümler, oturum açmış bir B2B hesabı gerektirdiğinden, site oluşturucudaki "gördüğünüz şey elde edeceğiniz sonucu gösterir" (WYSIWIG) tuvalinde görünmez.

## <a name="create-and-configure-customer-balance-pages-and-modules"></a>Müşteri bakiyesi sayfaları ve modülleri oluşturma ve yapılandırma 

Müşteri hesapları, siparişleri ödemek için kullanılabilir. Müşteri hesabındaki kullanılabilir bakiye, kullanıcının hesap yönetimi sayfasından görüntülenebilir.

### <a name="create-a-customer-balance-page"></a>Müşteri bakiyesi sayfası oluşturma 

Oturum açmış B2B kullanıcılarının müşteri bakiyelerini görüntüleyebilmeleri için önce bir müşteri bakiyesi sayfası oluşturmanız gerekir. 

Site oluşturucuda müşteri bakiyesi sayfası oluşturmak için aşağıdaki adımları izleyin.

1. **Müşteri Bakiyesi** adlı bir sayfa oluşturmak için az önce oluşturduğunuz **Hesap yönetimi** şablonunu kullanın.
1. **Üst bilgi** yuvasına, site üst bilgisiyle önceden yapılandırılmış üst bilgi parçasını ekleyin.
1. **Alt bilgi** yuvasına, site alt bilgisiyle önceden yapılandırılmış alt bilgi parçasını ekleyin.
1. **Ana** yuvaya başka bir **Kapsayıcı** modülü (**Kapsayıcı 3**) ekleyin. Modülün özellikler bölmesinde, **Genişlik** değerini **Dolgu Kapsayıcısı** olarak ayarlayın. **Gösterilen Alt Öğeler** değerini **İki** olarak ayarlayın.
1. **Kapsayıcı** yuvasına bir **İçerik haritası** modülü ekleyin. Modül özellikleri bölmesinde, **Bağlantılar** altında, hesap yönetimi açılış sayfasına bir bağlantı yapılandırın ve bağlantı metni olarak **Hesabım** girin.
1. **Kapsayıcı** yuvasında bir **Müşteri Hesap Bakiyesi** modülü ekleyin. Modül özellikleri bölmesinde, **Başlık** altında **Hesap Bakiyesi** girin.
1. **Kaydet**'i seçin, sayfayı iade etmek için **Düzenlemeyi bitir**'i ve ardından yayımlamak için **Yayımla**'yı seçin.
1. Sayfanın URL'sini yayınlayın.
1. Daha önce oluşturduğunuz hesap yönetimi açılış sayfasına (**Hesabım**) gidin.
1. **Hesap müşteri bakiyesi kutucuğu** modülünün özellikler bölmesinde, müşteri bakiyesi sayfasına bir bağlantı ekleyin. 
1. Sayfayı kaydedip yayınlayın.

Müşteri bakiyesi sayfası oluşturuldu ve kullanıcılar bu sayfaya hesap yönetimi açılış sayfasından erişebilir.

### <a name="configure-a-checkout-page-so-that-the-customer-balance-can-be-used-as-a-form-of-payment"></a>Müşteri bakiyesinin bir ödeme şekli olarak kullanılabilmesi için ödeme sayfası yapılandırma

Müşteri bakiyesinin bir ödeme şekli olarak kullanılmasını sağlamak için **Müşteri Hesabı Ödeme** modülü gereklidir. Bu modül ödeme sayfasına bir ödeme şekli olarak eklenmelidir. Ödeme sayfasının nasıl yapılandırılacağı ve tüm ödeme ayrıntıları da dahil olmak üzere ödeme için gerekli modüller hakkında bilgi için, bkz. [Ödeme modülü](../add-checkout-module.md).

Bir ödeme sayfası yapılandırdıktan sonra, **Müşteri Hesabı Ödeme** modülünü ödeme bölümüne eklemeniz ve ardından sayfayı kaydedip yayınlamanız gerekir. B2B kullanıcılar daha sonra e-ticaret sitesinde oturum açabilecek ve mevcut müşteri bakiyelerini ödeme sırasında siparişlere uygulayabilecekler.

Ayrıca, **Site Oluşturucu \> Uzantılar**'da, **Müşteri hesabı ödemelerini etkinleştir** özelliğinin **B2B müşterileri için etkin** olarak ayarlı olduğundan emin olmalısınız.

## <a name="create-order-template-pages"></a>Sipariş şablonu oluşturma sayfası

B2B e-ticaret sitesi için iki sipariş şablonu sayfası ayarlanabilir: sipariş şablonları liste sayfası ve sipariş şablonu satırları sayfası.

Sipariş şablonları listesi sayfasında, kullanılabilen tüm sipariş şablonlarının listesi gösterilir. **Sipariş şablonları listesi** modülü kullanılarak ayarlanır. Sipariş şablonları liste sayfası, şablon oluşturmanıza veya silmenize ve şablondaki öğeleri sepete eklemenize olanak tanır.

Sipariş şablonu satırları sayfası, sipariş şablonları listesi sayfasında seçilen sipariş şablonunun ayrıntılarını gösterir. **Sipariş şablonları satırları** modülü kullanılarak ayarlanır. Kullanıcı sipariş şablonları listesi sayfasında bir şablonun adını seçtiğinde, sipariş şablonu satırları sayfası görüntülenir ve şablonun ayrıntıları gösterilir. Kullanıcı daha sonra şablondaki öğeleri görüntüleyebilir ve düzenleyebilir.

### <a name="create-an-order-templates-list-page"></a>Sipariş şablonları listesi sayfası oluşturma

Site oluşturucuda bir sipariş şablonları liste sayfası oluşturmak için aşağıdaki adımları izleyin.

1. **Sipariş şablonları** adlı bir sayfa oluşturmak için az önce oluşturduğunuz **Hesap yönetimi** şablonunu kullanın.
1. **Üst bilgi** yuvasına, site üst bilgisiyle önceden yapılandırılmış üst bilgi parçasını ekleyin.
1. **Alt bilgi** yuvasına, site alt bilgisiyle önceden yapılandırılmış alt bilgi parçasını ekleyin.
1. **Ana** yuvasına bir **Kapsayıcı** modülü ekleyin. Modülün özellikler bölmesinde, **Genişlik** değerini **Dolgu Kapsayıcısı** olarak ayarlayın.
1. **Kapsayıcı** yuvasına bir **İçerik haritası** modülü ekleyin. Modül özellikleri bölmesinde, **Bağlantılar** altında, hesap yönetimi açılış sayfasına bir bağlantı yapılandırın ve bağlantı metni olarak **Hesabım** girin.
1. **Kapsayıcı** yuvasına **Sipariş şablonları listesi** modülü ekleyin.
1. **Kaydet**'i seçin, sayfayı iade etmek için **Düzenlemeyi bitir**'i ve ardından yayımlamak için **Yayımla**'yı seçin.
1. Sayfanın URL'sini yayınlayın.
1. Daha önce oluşturduğunuz hesap yönetimi açılış sayfasına (**Hesabım**) gidin.
1. **Hesap sipariş şablonları kutucuğu** modülünün özellikler bölmesinde, **Bağlantılar** altında, yeni oluşturduğunuz sipariş şablonları listesi sayfasına bir bağlantı yapılandırın.
1. Sayfayı kaydedip yayınlayın.

Sipariş şablonları listesi sayfası oluşturuldu ve kullanıcılar bu sayfaya hesap yönetimi açılış sayfasından erişebilir.

### <a name="create-an-order-template-lines-page"></a>Sipariş şablonu satırları sayfası oluşturma

Site oluşturucuda bir sipariş şablon satırları sayfası oluşturmak için aşağıdaki adımları izleyin.

1. **Sipariş şablon satırları** adlı bir sayfa oluşturmak için az önce oluşturduğunuz **Hesap yönetimi** şablonunu kullanın.
1. **Üst bilgi** yuvasına, site üst bilgisiyle önceden yapılandırılmış üst bilgi parçasını ekleyin.
1. **Alt bilgi** yuvasına, site alt bilgisiyle önceden yapılandırılmış alt bilgi parçasını ekleyin.
1. **Ana** yuvasına bir **Kapsayıcı** modülü ekleyin. Modülün özellikler bölmesinde, **Genişlik** değerini **Dolgu Kapsayıcısı** olarak ayarlayın.
1. **Kapsayıcı** yuvasına bir **İçerik haritası** modülü ekleyin. Modül özellikleri bölmesinde, **Bağlantılar** altında, hesap yönetimi açılış sayfasına bir bağlantı yapılandırın ve bağlantı metni olarak **Hesabım** girin.
1. **Kapsayıcı** yuvasına **Sipariş şablon satırları** modülü ekleyin.
1. **Kaydet**'i seçin, sayfayı iade etmek için **Düzenlemeyi bitir**'i ve ardından yayımlamak için **Yayımla**'yı seçin.
1. Sayfanın URL'sini yayınlayın.

## <a name="onboard-business-partner-users"></a>İş ortağı kullanıcılarını ekleme

Kuruluş kullanıcıları sayfası, bir iş ortağı kuruluşunun yöneticisinin bu kuruluştan B2B e-ticaret sitesine ek kullanıcılar eklemesine olanak tanır. **İşletme organizasyonu listesi** modülü kullanılarak ayarlanır. Yönetici, kuruluş kullanıcıları sayfasından kullanıcı ekleyebilir veya kaldırabilir, hesap bakiyelerini tanımlayabilir ve kullanıcı için ekstre isteyebilir.

Site oluşturucuda kuruluş kullanıcıları sayfası oluşturmak için aşağıdaki adımları izleyin.

1. **Kuruluş Kullanıcıları** adlı bir sayfa oluşturmak için az önce oluşturduğunuz **Hesap yönetimi** şablonunu kullanın.
1. **Üst bilgi** yuvasına, site üst bilgisiyle önceden yapılandırılmış üst bilgi parçasını ekleyin.
1. **Alt bilgi** yuvasına, site alt bilgisiyle önceden yapılandırılmış alt bilgi parçasını ekleyin.
1. **Ana** yuvasına bir **Kapsayıcı** modülü ekleyin. Modülün özellikler bölmesinde, **Genişlik** değerini **Dolgu Kapsayıcısı** olarak ayarlayın.
1. **Kapsayıcı** yuvasına bir **İçerik haritası** modülü ekleyin. Modül özellikleri bölmesinde, **Bağlantılar** altında, hesap yönetimi açılış sayfasına bir bağlantı yapılandırın ve bağlantı metni olarak **Hesabım** girin.
1. **Kapsayıcı** yuvasına **İşletme organizasyonu listesi** modülü ekleyin. Modül özellikleri bölmesinde, **Başlık** altında **Kuruluş Kullanıcıları** girin.
1. **İşletme organizasyonu listesi** modülü özellikleri bölmesinde, **Tablo Sıralama** ve **Tablo sayfalandırma** özelliklerini etkinleştirin. Sayfalandırma sayısını **5** olarak ayarlayın.
1. **Kaydet**'i seçin, sayfayı iade etmek için **Düzenlemeyi bitir**'i ve ardından yayımlamak için **Yayımla**'yı seçin.
1. Sayfanın URL'sini yayınlayın.
1. Daha önce oluşturduğunuz hesap yönetimi açılış sayfasına (**Hesabım**) gidin.
1. **Kuruluş kullanıcıları kutucuğu** modülünün özellikler bölmesinde, **Bağlantılar** altında, yeni oluşturduğunuz kuruluş kullanıcıları sayfasına bir bağlantı yapılandırın. 
1. **Kaydet**'i seçin, sayfayı iade etmek için **Düzenlemeyi bitir**'i ve ardından yayımlamak için **Yayımla**'yı seçin.

## <a name="create-invoice-pages"></a>Fatura sayfaları oluşturma

Fatura listesi sayfasında, kullanılabilir tüm faturaların listesi gösterilir. **Fatura Listesi** modülü kullanılarak ayarlanır. Fatura listesi sayfasından kullanıcılar faturalarını ödeyebilir veya talep edebilir. 

Fatura ayrıntıları sayfasında, fatura listesi sayfasında seçilen faturanın ayrıntıları gösterilir. **Fatura ayrıntıları** modülü kullanılarak ayarlanır. Kullanıcı fatura listesi sayfasında bir fatura kimliği seçtiğinde, fatura ayrıntıları sayfası görüntülenir ve faturanın ayrıntıları gösterilir.

### <a name="create-an-invoices-list-page"></a>Fatura listesi sayfası oluşturma

Site oluşturucuda fatura listesi sayfası oluşturmak için aşağıdaki adımları izleyin.

1. **Fatura Listesi** adlı bir sayfa oluşturmak için az önce oluşturduğunuz **Hesap yönetimi** şablonunu kullanın.
1. **Üst bilgi** yuvasına, site üst bilgisiyle önceden yapılandırılmış üst bilgi parçasını ekleyin.
1. **Alt bilgi** yuvasına, site alt bilgisiyle önceden yapılandırılmış alt bilgi parçasını ekleyin.
1. **Ana** yuvasına bir **Kapsayıcı** modülü ekleyin. Modülün özellikler bölmesinde, **Genişlik** değerini **Dolgu Kapsayıcısı** olarak ayarlayın.
1. **Kapsayıcı** yuvasına bir **İçerik haritası** modülü ekleyin. Modül özellikleri bölmesinde, **Bağlantılar** altında, hesap yönetimi açılış sayfasına bir bağlantı yapılandırın ve bağlantı metni olarak **Hesabım** girin.
1. **Kapsayıcı** yuvasına bir **Fatura Listesi** modülü ekleyin. Modül özellikleri bölmesinde, **Başlık** altında **Faturalar** girin.
1. **Kaydet**'i seçin, sayfayı iade etmek için **Düzenlemeyi bitir**'i ve ardından yayımlamak için **Yayımla**'yı seçin.
1. Sayfanın URL'sini yayınlayın.
1. Daha önce oluşturduğunuz hesap yönetimi açılış sayfasına (**Hesabım**) gidin.
1. **Hesap faturaları kutucuğu** modülünün özellikler bölmesinde, **Bağlantılar** altında, yeni oluşturduğunuz fatura listesi sayfasına bir bağlantı yapılandırın. 
1. **Kaydet**'i seçin, sayfayı iade etmek için **Düzenlemeyi bitir**'i ve ardından yayımlamak için **Yayımla**'yı seçin.

### <a name="create-an-invoice-details-page"></a>Fatura ayrıntıları sayfası oluşturma

Site oluşturucuda fatura ayrıntıları sayfası oluşturmak için aşağıdaki adımları izleyin.

1. **Fatura Ayrıntıları** adlı bir sayfa oluşturmak için az önce oluşturduğunuz **Hesap yönetimi** şablonunu kullanın.
1. **Üst bilgi** yuvasına, site üst bilgisiyle önceden yapılandırılmış üst bilgi parçasını ekleyin.
1. **Alt bilgi** yuvasına, site alt bilgisiyle önceden yapılandırılmış alt bilgi parçasını ekleyin.
1. **Ana** yuvasına bir **Kapsayıcı** modülü ekleyin. Modülün özellikler bölmesinde, **Genişlik** değerini **Dolgu Kapsayıcısı** olarak ayarlayın.
1. **Kapsayıcı** yuvasına bir **İçerik haritası** modülü ekleyin. Modül özellikleri bölmesinde, **Bağlantılar** altında, hesap yönetimi açılış sayfasına bir bağlantı yapılandırın ve bağlantı metni olarak **Hesabım** girin. Ardından, fatura listesi sayfasına bir bağlantı yapılandırın ve bağlantı metni olarak **Fatura Listeleri** girin.
1. **Kapsayıcı** yuvasına bir **Fatura ayrıntıları** modülü ekleyin.
1. **Kaydet**'i seçin, sayfayı iade etmek için **Düzenlemeyi bitir**'i ve ardından yayımlamak için **Yayımla**'yı seçin.
1. Sayfanın URL'sini yayınlayın.

## <a name="add-a-quick-add-module-to-the-cart-page"></a>Sepet sayfasına hızlı ekleme modülü ekleme

Hızlı ekleme modülü, madde kodları (stok saklama birimi \[SKU\] kodu olarak da bilinir) kullanılarak alışveriş sepetine hızlı bir şekilde birden fazla madde eklemenin bir yolunu sağlar. Hızlı ekleme modülü, sitenin sepet sayfasına eklenir.

Commerce site oluşturucuda bir sepet sayfasına hızlı ekleme modülü eklemek için aşağıdaki adımları izleyin.

1. **Şablonlar**'a gidin ve sitenizin sepet sayfası şablonunu seçin.
1. **Düzenle** öğesini seçin.
1. **Varsayılan sayfa** modülünde **ana** yuvayı seçin, üç nokta düğmesini (**...**) ve sonra **Modül ekle**'yi seçin.
1. **Modül Ekle** iletişim kutusunda **Konteyner** modülünü seçin ve **Tamam**'ı seçin.
1. **Konteyner** yuvası için üç nokta (**...**) düğmesini seçin ve **Modül Ekle**'yi seçin.
1. **Modül Ekle** iletişim kutusunda **Hızlı ekleme** modülünü seçin ve **Tamam**'ı seçin.
1. **Kaydet**'i seçin, şablonu iade etmek için **Düzenlemeyi bitir**'i ve ardından yayımlamak için **Yayımla**'yı seçin.
1. **Sayfalar**'a gidin ve sitenizin sepet sayfası şablonunu seçin.
1. **Varsayılan sayfa** modülünde **ana** yuvayı seçin, üç nokta düğmesini (**...**) ve sonra **Modül ekle**'yi seçin.
1. **Modül Ekle** iletişim kutusunda **Konteyner** modülünü seçin ve **Tamam**'ı seçin.
1. **Konteyner** modülü için özellikler panosunda **Genişlik** altında, **Konteyneri doldur**'u seçin.
1. **Konteyner** yuvası için üç nokta (**...**) düğmesini seçin ve **Modül Ekle**'yi seçin.
1. **Modül Ekle** iletişim kutusunda **Hızlı ekleme** modülünü seçin ve **Tamam**'ı seçin.
1. **Kaydet**'i seçin, sayfayı iade etmek için **Düzenlemeyi bitir**'i ve ardından yayımlamak için **Yayımla**'yı seçin.

> [!NOTE] 
> Hızlı ekleme modülü, Commerce 10.0.17 sürümü itibarıyla kullanılabilir. Commerce'ün eski sürümlerinden birini güncelleştiriyorsanız, appsettings.json dosyasını el ile güncelleştirmeniz gerekir. Talimatlar için bkz. [SDK ve modül kitaplığı güncelleştirmeleri](../e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file).

## <a name="additional-resources"></a>Ek kaynaklar

[Modül kitaplığına genel bakış](../starter-kit-overview.md)

[SDK ve modül kitaplığı güncelleştirmeleri](../e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file)

[Yazma sayfasına genel bakış](../authoring-home-overview.md)

[Şablonlar ve düzenlere genel bakış](../templates-layouts-overview.md)

[Parçalarla çalışma](../work-with-fragments.md)

[Yeni site sayfası ekleme](../add-new-page.md)

[Ödeme yapma modülü](../add-checkout-module.md)

[İçerik bloğu modülü](../add-hero-module.md)

[Ürün topluluğu modülü](../product-collection-module-overview.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
