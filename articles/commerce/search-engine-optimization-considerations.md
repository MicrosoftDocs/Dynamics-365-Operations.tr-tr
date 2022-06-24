---
title: Siteniz için arama motoru optimizasyonuyla (SEO) ilgili konular
description: Bu makale, gelişmede sizin sitenizin üretime yönelik arama motoru iyileştirme (SEO) konularını kapsamaktadır.
author: psimolin
ms.date: 05/25/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgri
ms.search.region: Global
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.openlocfilehash: 6747df3c56fb05248210f78ebf2176a56ce78329
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8896913"
---
# <a name="search-engine-optimization-seo-considerations-for-your-site"></a>Siteniz için arama motoru optimizasyonuyla (SEO) ilgili konular


[!include [banner](includes/banner.md)]

Bu makale, gelişmede sizin sitenizin üretime yönelik arama motoru iyileştirme (SEO) konularını kapsamaktadır.

## <a name="a-site-that-is-under-development"></a>Geliştirilme aşamasında olan bir site

Arama motorlarının geliştirilmekte olan bir siteyi dizine eklemediğinden emin olmak için tüm site sayfalarında **noindex** ve **nofollow** meta etiketleri olmalıdır. Aşağıdaki meta etiketi girişini içeren [MetaTags modülünü](metatags-module.md) temel alan bir parça oluşturmanız ve parçanın sitenizde kullanılan tüm şablonların HTML \<head\> bölümüne eklendiğinden emin olmanız önerilir.

```html
<meta name="robots" content="noindex,nofollow" /> 
```

## <a name="soft-launch-of-a-site"></a>Siteyi yazılımla başlatma

"Yazılımla başlatma" sırasında, tam başlatma gerçekleşmeden önce sınırlı bir izleyici veya Pazar için bir Web sitesi kullanılabilir hale getirilir. Web sitenizin geçici olarak kullanıma sunulması durumunda, **noindex** meta etiketlerini kaldırmamayı düşünebilirsiniz. Bu şekilde, yazılım başlatmanın erişmek istediğiniz sınırlı hedef kitle ile sınırlı kalmasını sağlamaya yardımcı olursunuz.

## <a name="a-site-that-is-in-production"></a>Üretimdeki bir site

Bir site üretimde olduğunda, tüm site sayfalarının doğru etiketlendiğinden emin olmalısınız. Microsoft Dynamics 365 Commerce, sayfa için girilen bilgileri bu sayfadaki tüm SEO bilgilerini işlemek için kullanır. Aşağıdaki modüller bu işlevi sağlar: kategori sayfası Özeti, liste sayfası Özeti ve ürün sayfası Özeti.

Arama motoru dizinini oluşturma işlemini en iyi duruma getirmek için, işleme çerçevesi hem Dynamics 365 Commerce'de hem de modüle özel bilgiler için yapılandırılan SEO özelliklerinden bilgileri kullanır. Üretimdeki bir site için robots.txt dosyasının tüm sitenizde dizin oluşturmaya olanak verdiğinden ve yayımlanmış site haritası belgenize bağlantılar içerdiğinden emin olmalısınız. **Site ayarları \> Site eşlemelerinin etkin** olduğu site haritası oluşturma işlevini etkinleştirmeniz gerekir.

### <a name="page-seo-settings-for-internal-preview-limited-audiences-and-all-audiences"></a>Dahili önizleme, sınırlı hedef kitleler ve tüm izleyiciler için sayfa SEO ayarları

Dynamics 365 Commerce, görsel sayfa oluşturucuda "gördüğünüz şey aldığınız şeydir" (WYSIWYG) kimlik doğrulamalı önizleme desteği sağladığından, yazarlar bilgilerin site ziyaretçileri tarafından görülebileceğini düşünmenize gerek kalmadan sayfa içeriğini hazırlayabilir. Bir sayfanın yayımlanması ancak gösterilme sayısının sınırlı olması gerekiyorsa, sayfanın bir **noindex** meta etiketine sahip olmalısı gerekir. Böylece, arama motorları sayfayı dizine eklemez. Daha sonra, sayfa tüm izleyiciler için hazır olduğunda, arama motoru dizininin verimliliğini en üst düzeye çıkarmak için tüm temel SEO meta verileri bulunmalıdır. Ek olarak, **nolimit** meta etiketi kaldırılmalıdır.

## <a name="additional-resources"></a>Ek kaynaklar

[e-Ticaret kullanıcıları ve rolleri yönetme](manage-ecommerce-users-roles.md)

[Telemetriyi desteklemek için site sayfalarına komut dosyası kodu ekleme](add-telemetry.md)

[İçerik Güvenliği İlkesini (CSP) yönetme](manage-csp.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
