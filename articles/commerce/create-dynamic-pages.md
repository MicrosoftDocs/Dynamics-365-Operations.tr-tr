---
title: URL parametrelerini temel alan dinamik e-ticaret sayfaları oluşturma
description: Bu konuda, URL parametrelerine göre dinamik içerik sunabilen bir Microsoft Dynamics 365 Commerce e-ticaret sayfasının nasıl ayarlanacağı açıklanmaktadır.
author: StuHarg
ms.date: 05/27/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: global
ms.author: stuharg
ms.search.validFrom: 2019-09-30
ms.openlocfilehash: 3443dad9ead40b59da994c56e22fe2599f4bac82
ms.sourcegitcommit: 336a0ad772fb55d52b4dcf2fafaa853632373820
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/28/2022
ms.locfileid: "8811043"
---
# <a name="create-dynamic-e-commerce-pages-based-on-url-parameters"></a>URL parametrelerini temel alan dinamik e-ticaret sayfaları oluşturma

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

Bu konuda, URL parametrelerine göre dinamik içerik sunabilen bir Microsoft Dynamics 365 Commerce e-ticaret sayfasının nasıl ayarlanacağı açıklanmaktadır.

Bir e-ticaret sayfası, URL yolundaki bir segmente göre farklı içerikler sunmak üzere yapılandırılabilir. Bu nedenle, sayfa dinamik sayfa olarak bilinir. Segment, sayfa içeriğini almak için parametre olarak kullanılır. Örneğin, site oluşturucusunda oluşturulan **blog\_viewer** adlı bir sayfa `https://fabrikam.com/blog` URL'si ile eşleştirilir. Bu sayfa daha sonra URL yolundaki son segmente göre farklı içerik göstermek için kullanılabilir. Örneğin, `https://fabrikam.com/blog/article-1` URL'sindeki son segment **makale-1**'dir.

Ayrıca site oluşturucusu sayfasıyla parametreli hale getirilen bir URL segmentini geçersiz kılabilirsiniz. Örneğin, site oluşturucusunda oluşturulan **blog\_summary** adlı bir sayfa `https://fabrikam.com/blog/about-this-blog` URL'si ile eşleştirilir. `https://fabrikam.com/blog` URL'si sonunda `/about-this-blog` segmentiyle istendiğinde, `/about-this-blog` segmenti `https://fabrikam.com/blog` sayfasıyla kullanılacak bir parametre biçiminde yorumlanmaz. Bunun yerine **blog\_summary** sayfası döndürülür. 

Dinamik sayfaya geçirilecek parametreler için ad seçerken, dinamik sayfa adı URL'deki şekliyle (yukarıdaki örnekte `/blog`) parametre adı veya parametre adının alt dizesi olarak kullanılamaz. 

> [!NOTE]
> Dinamik sayfa içeriğini barındırma, alma ve gösterme işlevi özel bir modül kullanılarak uygulanır. Daha fazla bilgi için, bkz. [Çevrimiçi kanal genişletilebilirliği](e-commerce-extensibility/overview.md).

## <a name="set-up-a-dynamic-e-commerce-page"></a>Dinamik e-ticaret sayfası ayarlama

Dinamik bir e-ticaret sayfası ayarlamak için dinamik sayfayı oluşturmanız, temel URL'yi oluşturmanız ve dinamik sayfaya giden yolu yapılandırmanız gerekir.

### <a name="create-the-page-that-will-serve-dynamic-content"></a>Dinamik içeriğe hizmet edecek sayfayı oluşturma

Dinamik içerik sunacak bir sayfa oluşturmak için [Yeni site sayfası ekleme](add-new-page.md) bölümündeki adımları izleyin. Oluşturduğunuz sayfa, dış veri kaynağından içerik almak için URL yolundaki son segmenti kullanan bir modülün uygulanmasını gerektirir. Özel modül geliştirme hakkında daha fazla bilgi için bkz. [Çevrimiçi kanal genişletilebilirliği](e-commerce-extensibility/overview.md).

### <a name="create-the-base-url-for-the-dynamic-page"></a>Dinamik sayfa için temel URL oluşturma

Commerce Site Builder'da dinamik sayfa için temel oluşturmak üzere aşağıdaki adımları izleyin.

1. **URL'ler** bölümüne gidin ve **Yeni \> Yeni URL**'yi seçin.
1. **Yeni URL oluştur** iletişim kutusunda **Dahili sayfalar**'ı seçin. **URL yolu** altında, dinamik sayfa için kök olarak kullanılacak yolu girin (bu örnekte, **/blog**). Sonra **İleri**'yi seçin.
1. **Sayfa seçin** iletişim kutusunda dinamik sayfa olarak kullanılması için oluşturduğunuz sayfayı ve sonra **Kaydet**'i seçin.
1. **Yayımla**'yı seçin.

### <a name="configure-the-route-to-the-dynamic-page"></a>Dinamik sayfa yolunu yapılandırma

Commerce Site Builder'da dinamik sayfa yolunu yapılandırmak için aşağıdaki adımları izleyin.

1. **Site Ayarları \> Uzantılar**'a gidin.
1. **Parametreli URL yolları** altında, **Ekle**'yi seçin ve URL'yi oluştururken girdiğiniz URL yolunu girin (bu örnekte, **/blog**).
1. **Kaydet ve yayınla** yı seçin.

Yol yapılandırıldıktan sonra, parametreli URL yoluna yapılan tüm istekler bu URL ile ilişkilendirilmiş sayfayı döndürür. Herhangi bir istekte ek bir segment varsa, ilişkili sayfa döndürülür ve sayfa içeriği segment parametresi olarak kullanılarak alınır. Örneğin, `https://fabrikam.com/blog/article-1` **/article-1** parametresini kullanarak aldığı içeriği gösteren `https://fabrikam.com/blog` sayfasını döndürür.

## <a name="override-a-parameterized-url-with-a-custom-page"></a>Parametreli URL'yi özel bir sayfayla geçersiz kılma

Commerce Site Builder'da özel bir sayfayla parametreli URL'yi geçersiz kılmak için aşağıdaki adımları izleyin.

1. **URL'ler** bölümüne gidin ve **Yeni \> Yeni URL**'yi seçin.
1. **Yeni URL oluştur** iletişim kutusunda **Dahili sayfalar**'ı seçin. **URL yolu** altında, geçersiz kılınacak segmenti içeren yolu girin (bu örnekte, **/blog/bu-blog-hakkinda**) girin. Sonra **İleri**'yi seçin.
1. **Bir sayfa seçin** iletişim kutusunda özel sayfayı seçin ve sonra **Kaydet**'i seçin.
1. **Yayımla**'yı seçin.
1. Özel sayfa henüz yayılanmadıysa, **Sayfalar**'a gidin, özel sayfayı seçin ve sonra **Yayınla**'yı seçin.

Özel sayfa yayınlandıktan sonra, üzerinde parametreli içerik bulunan dinamik sayfa yerine hizmet sunulur.

## <a name="additional-resources"></a>Ek kaynaklar

[Var olan site sayfasını değiştirme](modify-existing-page.md)

[Yeni site sayfası ekleme](add-new-page.md)

[Sayfa düzeni seçme](select-page-layouts.md)

[SEO meta verilerini yönetme](manage-seo-metadata.md)

[Sayfa kaydetme, önizleme ve yayımlama](save-preview-publish-page.md)

[Ürün sayfasını zenginleştirme](enrich-product-page.md)

[Kategori açılış sayfasını zenginleştirme](enrich-category-page.md)

[Sayfa içeriği erişilebilirliğini doğrulama](verify-accessibility.md)

[Çevrimiçi kanal genişletilebilirliği](e-commerce-extensibility/overview.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
