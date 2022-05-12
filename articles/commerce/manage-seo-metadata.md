---
title: SEO meta verilerini yönetme
description: Bu konuda, Microsoft Dynamics 365 Commerce'ta arama motoru optimizasyonu (SEO) meta verilerinin nasıl yönetileceği açıklanmaktadır.
author: psimolin
ms.date: 04/21/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 3d6f56968e9adfe90142955cba8e6c7ecc50fc92
ms.sourcegitcommit: d715e44b92b84b1703f5915d15d403ccf17c6606
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/27/2022
ms.locfileid: "8644771"
---
# <a name="manage-seo-metadata"></a>SEO meta verilerini yönetme

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

Bu konuda, Microsoft Dynamics 365 Commerce'ta arama motoru optimizasyonu (SEO) meta verilerinin nasıl yönetileceği açıklanmaktadır.

Bir sitenin SEO meta verileri, site haritaları ve sayfa meta verileri kullanılarak yönetilebilir.
    
## <a name="site-maps"></a>Site haritaları

Site haritası, Web sitenizdeki sayfaların, XML biçimindeki, makine tarafından okunabilen bir listesidir. Arama motorları tarafından, sitenizde daha iyi arama sonuçları sağlayabilmeleri için tüketilmesi amaçlanmıştır. Site eşlemeleri arama motorları tarafından el ile gerçekleştirilebilir veya robots. txt dosyasında yayımlanabilir.

Dynamics 365 Commerce Site eşlemelerinin otomatik olarak oluşturulmasını destekler. Sayfalar yayımlanana ve yayımdan kaldırılmış olduğunda, site eşleştirmeleri otomatik olarak güncelleştirilir.

### <a name="turn-on-site-map-generation"></a>Site Haritası oluşturmayı aç

1. Geliştirme aracında oturum açın.
1. **Siteler** altında, **Fabrikam**'ı seçin (veya sitenizin adını).
1. Soldaki gezinti bölmesinde **Site Yönetimi** seçin.
1. **Site haritaları etkin** seçeneğinin açık olduğundan emin olun.

## <a name="page-metadata"></a>Sayfa meta verileri

Dynamics 365 Commerce Her bir sayfa için SEO meta verilerini yönetmenizi sağlar. Bu bilgileri bir sayfa kapsayıcısının **SEO Özellikler** bölümünde görüntüleyebilir ve değiştirebilirsiniz. Şu anda aşağıdaki SEO meta veri özellikleri desteklenmektedir:

- Ünvan
- Tanım
- SEO Anahtar sözcükler
- Aria etiketleri
- noindex
- nofollow
- noarchive
- nocache
- noOpenDirectoryProject
- nosnippet
- noImageIndex
- unavailableAfter

### <a name="modify-page-metadata"></a>Sayfa meta verilerini Değiştir

Sayfa meta verilerini değiştirmek için aşağıdaki adımları izleyin.
1. **Siteler** altında, **Fabrikam**'ı seçin (veya sitenizin adını).
1. Soldaki gezinti bölmesinde **Sayfalar** seçin.
1. Sayfa düzenleyicisinde açmak için giriş sayfasını seçin.
1. Komut çubuğunda, **Düzenle** öğesini seçin.
1. Soldaki sayfa ana hat denetiminin üst kısmındaki sayfa düzenleyicisinde, **Ana hat modu seçeneğini** (dişli sembolü) seçin ve **Gelişmiş ana hat görünümünü** seçin.
1. Ana hat görünümünde, **HTML başlık** yuvasının içeriğini göstermek için ağaç kontrollerini genişletin.
1. **HTML başlık** yuvasında, istenen SEO modülünü (örneğin, **Sayfa özeti**, **Ürün sayfa özeti**, **Kategori sayfa özeti** veya **Meta etiketler**) seçin.
1. Sağdaki özellikler bölmesinde, seçili SEO modülü (örneğin, **Başlık**, **Açıklama** veya **Paylaşım görüntüsü**) için istenen SEO verilerini düzenleyin.
1. **Kaydet** i seçin ve sonra **Düzenlemeyi bitir**'i seçin.
1. **Yorumlar** alanında **Güncellenen SEO verileri** seçeneğini girin ve **Tamam**'ı seçin.
1. Sayfanızın önizlemesini görüntülemek için **Önizleme**'yi seçin. Bitirdiğinizde, geliştirme aracına dönmek için Önizleme sekmesini kapatın.
1. **Yayımla**'yı seçin.

> [!TIP]
> Yazarlar, **Temel ana hat görünümü** ile **Gelişmiş ana hat görünümü** arasında geçiş yapmak için sayfa düzenleyicisindeki sol ana hat denetiminin üst kısmındaki **Ana hat modu** seçeneğini (dişli sembolü) kullanabilirler. **Temel ana hat görünümü** varsayılan ayardır ve ana hatta filtre uygular ve yalnızca sayfanın **Gövde** HTML yuvasındaki modülleri gösterir. **Gelişmiş ana hat görünümü** **HTML başlık**, **Gövde başlangıcı** ve **Gövde bitiş** yuvaları dahil olmak üzere tüm sayfa modülünü gösterir. Yazarların belirli SEO veya kod modülü ayarlarını bir sayfaya düzenlemesi gerektiğinde bu görünüm yararlıdır.

## <a name="additional-resources"></a>Ek kaynaklar

[Var olan site sayfasını değiştirme](modify-existing-page.md)

[Yeni site sayfası ekleme](add-new-page.md)

[Sayfa düzeni seçme](select-page-layouts.md)

[Sayfa kaydetme, önizleme ve yayımlama](save-preview-publish-page.md)

[Ürün sayfasını zenginleştirme](enrich-product-page.md)

[Kategori açılış sayfasını zenginleştirme](enrich-category-page.md)

[Sayfa içeriği erişilebilirliğini doğrulama](verify-accessibility.md)

[URL parametrelerini temel alan dinamik e-ticaret sayfaları oluşturma](create-dynamic-pages.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
