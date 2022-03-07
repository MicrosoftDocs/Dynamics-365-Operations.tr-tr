---
title: URL parametrelerini temel alan dinamik e-ticaret sayfaları oluşturma
description: Bu konuda, URL parametrelerine göre dinamik içerik sunabilen bir Microsoft Dynamics 365 Commerce e-ticaret sayfasının nasıl ayarlanacağı açıklanmaktadır.
author: StuHarg
manager: AnnBe
ms.date: 01/28/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ROBOTS: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.author: stuharg
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: e72b738133b396848848d167cace80fe23694334
ms.sourcegitcommit: 872600103d2a444d78963867e5e0cdc62e68c3ec
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/01/2021
ms.locfileid: "5098653"
---
# <a name="create-dynamic-e-commerce-pages-based-on-url-parameters"></a>URL parametrelerini temel alan dinamik e-ticaret sayfaları oluşturma

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

Bu konuda, URL parametrelerine göre dinamik içerik sunabilen bir Microsoft Dynamics 365 Commerce e-ticaret sayfasının nasıl ayarlanacağı açıklanmaktadır.

Bir e-ticaret sayfası, URL yolundaki bir segmente göre farklı içerikler sunmak üzere yapılandırılabilir. Bu nedenle, sayfa dinamik sayfa olarak bilinir. Segment, sayfa içeriğini almak için parametre olarak kullanılır. Örneğin, **blog\_görüntüleyicisi** adlı bir sayfa oluşturulur ve `https://fabrikam.com/blog` URL'si ile ilişkilendirilir. Bu sayfa daha sonra URL yolundaki son segmente göre farklı içerik göstermek için kullanılabilir. Örneğin, `https://fabrikam.com/blog/article-1` URL'sindeki son segment **makale-1**'dir.

Dinamik sayfayı geçersiz kılan ayrı özel sayfalar da URL yolundaki segmentlerle ilişkilendirilebilir. Örneğin, **blog\_özeti** adlı bir sayfa oluşturulur ve `https://fabrikam.com/blog/about-this-blog` URL'si ile ilişkilendirilir. Bu URL istendiğinde, **blog\_görüntüleyici** sayfası yerine **/bu-blog-hakkinda** parametresiyle ilişkili **blog\_özeti** sayfası döndürülür.

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

Yol yapılandırıldıktan sonra, parametreli URL yoluna yapılan tüm istekler bu URL ile ilişkilendirilmiş sayfayı döndürür. Herhangi bir istekte ek bir segment varsa, ilişkili sayfa döndürülür ve sayfa içeriği segment parametresi olarak kullanılarak alınır. Örneğin, `https://fabrikam.com/blog/article-1`, **blog\_özeti** sayfasını döndürür ve sayfa içeriği **/makale-1** parametresi kullanılarak getirilir.

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
