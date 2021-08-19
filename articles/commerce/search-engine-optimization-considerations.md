---
title: Siteniz için arama motoru optimizasyonu (SEO) konuları
description: Bu konu, gelişmede sizin sitenizin üretime yönelik arama motoru iyileştirme (SEO) konularını kapsamaktadır.
author: psimolin
ms.date: 10/01/2019
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
ms.openlocfilehash: df92aeae967bbf248b90dffc6bc2239a8d2959183acb9e9181bc344b9e3eff8d
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/05/2021
ms.locfileid: "6716869"
---
# <a name="search-engine-optimization-seo-considerations-for-your-site"></a>Siteniz için arama motoru optimizasyonu (SEO) konuları


[!include [banner](includes/banner.md)]

Bu konu, gelişmede sizin sitenizin üretime yönelik arama motoru iyileştirme (SEO) konularını kapsamaktadır.

## <a name="a-site-that-is-under-development"></a>Geliştirilme aşamasında olan bir site

Bir site gelitirme altýnda, tüm site sayfaları **NOINDEX** ve **NOFOLLOW** meta etiketlerine sahip olmalıdır, böylece arama motorları, sitenizin sayfalarını ve mağaza geliştirme sürümlerini kendi önbelleğinde dizinlerler. Bu konfigürasyonu yapmak için, site sayfası şablonuna varsayılan meta etiketler modülünü eklemeniz gerekir. Daha sonra, varsayılan meta etiketler özellikleri sayfa düzenleyicisinin SEO Özellikler bölümünde kullanılabilir olacak. Meta etiketleri yönetmek için bu özellikleri kullanabilirsiniz.

## <a name="soft-launch-of-a-site"></a>Siteyi yazılımla başlatma

"Yazılımla başlatma" sırasında, tam başlatma gerçekleşmeden önce sınırlı bir izleyici veya Pazar için bir Web sitesi kullanılabilir hale getirilir. Web sitenizin yazılımla başlatılması durumunda, **NOINDEX** meta etiketlerinin yerinde kalmasını düşünmelisiniz. Bu şekilde, yazılım başlatmanın erişmek istediğiniz sınırlı hedef kitle ile sınırlı kalmasını sağlamaya yardımcı olursunuz.

## <a name="a-site-that-is-in-production"></a>Üretimdeki bir site

Bir site üretimde olduğunda, tüm site sayfalarının doğru etiketlendiğinden emin olmalısınız. Microsoft Dynamics 365 Commerce, sayfa için girilen bilgileri bu sayfadaki tüm SEO bilgilerini işlemek için kullanır. Aşağıdaki modüller bu işlevi sağlar: kategori sayfası Özeti, liste sayfası Özeti ve ürün sayfası Özeti.

Arama motoru dizinini oluşturma işlemini en iyi duruma getirmek için, işleme çerçevesi hem Dynamics 365 Commerce'de hem de modüle özel bilgiler için yapılandırılan SEO özelliklerinden bilgileri kullanır. Üretimdeki bir site için robots.txt dosyasının tüm sitenizde dizin oluşturmaya olanak verdiğinden ve yayımlanmış site haritası belgenize bağlantılar içerdiğinden emin olmalısınız. **Site ayarları \> Site eşlemelerinin etkin** olduğu site haritası oluşturma işlevini etkinleştirmeniz gerekir.

### <a name="page-seo-settings-for-internal-preview-limited-audiences-and-all-audiences"></a>Dahili önizleme, sınırlı hedef kitleler ve tüm izleyiciler için sayfa SEO ayarları

Dynamics 365 Commerce, görsel sayfa oluşturucuda "gördüğünüz şey aldığınız şeydir" (WYSIWYG) kimlik doğrulamalı önizleme desteği sağladığından, yazarlar bilgilerin site ziyaretçileri tarafından görülebileceğini düşünmenize gerek kalmadan sayfa içeriğini hazırlayabilir. Bir sayfanın yayımlanması gerekiyorsa, ancak etkilenme sayısının sınırlı olması gerekiyorsa, bu bir **NOINDEX** meta etiketine sahip olmalıdır ve bu nedenle arama motorları tarafından dizin oluşturulmayacak. Daha sonra, sayfa tüm izleyiciler için hazır olduğunda, arama motoru dizininin verimliliğini en üst düzeye çıkarmak için tüm temel SEO meta verileri bulunmalıdır. Ek olarak, **NOLIMIT** meta etiketi kaldırılmalıdır.

## <a name="additional-resources"></a>Ek kaynaklar

[e-Ticaret kullanıcıları ve rolleri yönetme](manage-ecommerce-users-roles.md)

[Telemetriyi desteklemek için site sayfalarına komut dosyası kodu ekleme](add-telemetry.md)

[İçerik Güvenliği İlkesini (CSP) yönetme](manage-csp.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]