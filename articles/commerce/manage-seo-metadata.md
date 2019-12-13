---
title: SEO meta verilerini yönetme
description: Bu konuda, Microsoft Dynamics 365 Commerce'ta arama motoru optimizasyonu (SEO) meta verilerinin nasıl yönetileceği açıklanmaktadır.
author: psimolin
manager: annbe
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: b69d9d2769023967e2b94fef1b8fcf6b5b3357c5
ms.sourcegitcommit: 295d940a345879b3dfc5991e387b91c7257019ea
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/01/2019
ms.locfileid: "2698361"
---
# <a name="manage-seo-metadata"></a>SEO meta verilerini yönetme

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

Bu konuda, Microsoft Dynamics 365 Commerce'ta arama motoru optimizasyonu (SEO) meta verilerinin nasıl yönetileceği açıklanmaktadır.

## <a name="overview"></a>Genel Bakış

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
1. Eylem Bölmesinde, **Çıkış yap** öğesini seçin.
1. Sağdaki özellikler bölmesinde, **Varsayılan meta verileri** genişletin.
1. Yeni bir metaetiketi eklemek için, **Ekle**'yi seçin ve alana etiketi girin.

    Varolan bir meta etiketi kaldırmak için, sağ tarafta bulunan çöp tenekesi sembolünü seçin.

1. **Kaydet**i seçin ve sonra **Giriş**'i seçin.
1. **Yorumlar** alanında **Güncellenen meta etiketler** seçeneğini girin ve **Tamam**'ı seçin.
1. Sayfanızın önizlemesini görüntülemek için **Önizleme**'yi seçin. Bitirdiğinizde, geliştirme aracına dönmek için Önizleme sekmesini kapatın.
1. **Yayımla**'yı seçin.

## <a name="additional-resources"></a>Ek kaynaklar

[Var olan site sayfasını değiştirme](modify-existing-page.md)

[Yeni site sayfası ekleme](add-new-page.md)

[Sayfa düzeni seçme](select-page-layouts.md)

[Sayfa kaydetme, önizleme ve yayımlama](save-preview-publish-page.md)

[Ürün sayfasını zenginleştirme](enrich-product-page.md)

[Kategori açılış sayfasını zenginleştirme](enrich-category-page.md)

