---
title: B2B için Commerce katalogları hakkında SSS
description: Bu makalede, Microsoft Dynamics 365 Commerce katalogları hakkında sık sorulan sorular yanıtlanmıştır.
author: ashishmsft
ms.date: 07/15/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: asharchw
ms.search.validFrom: 2022-02-28
ms.openlocfilehash: 68c648c5caf2667f413b236dc437fc2c74c40d07
ms.sourcegitcommit: c271b2edc4bf777f7194b09139ccbd174a359c75
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/16/2022
ms.locfileid: "9168998"
---
# <a name="commerce-catalogs-for-b2b-faq"></a>B2B için Commerce katalogları hakkında SSS

[!include [banner](includes/banner.md)]

Bu makalede, Microsoft Dynamics 365 Commerce [işletmeden işletmeye (B2B) katalogları](catalogs-b2b-sites.md) hakkında sık sorulan sorular yanıtlanmıştır.

### <a name="why-cant-i-configure-a-catalog-specific-navigation-hierarchy-or-see-an-option-to-associate-a-customer-hierarchy"></a>Neden kataloğa özel gezinti hiyerarşisini konfigüre edemiyorum veya müşteri hiyerarşisini ilişkilendirme seçeneğini göremiyorum?

Commerce headquarters'ta **Özellik yönetimi** çalışma alanında **Perakende kanalları üzerinde çoklu katalog kullanımını etkinleştir** özelliğini etkinleştirdiğinizden ve ortamınızın Commerce 10.0.27 veya daha güncel bir sürüme sahip olduğundan emin olun. **Katalog türü** altında **B2B** seçtiğinizden emin olun.

### <a name="can-i-view-the-catalog-specific-hierarchy-and-enrich-category-pages-in-commerce-site-builder"></a>Commerce site oluşturucuda kataloğa özel hiyerarşiyi görebilir ve kategori sayfalarını zenginleştirebilir miyim?

Evet, site oluşturucuda **Ürünler** sayfasına erişimi olan Commerce site oluşturucu kullanıcıları, katalog seçebilir ve kataloğa özel hiyerarşiyi görüntüleyebilir. Kullanıcılar, **Ürünler** sayfasından katalogdaki belirli bir kategori için kategori sayfasını zenginleştirebilir. Daha fazla bilgi için bkz. [Kategori giriş sayfasını zenginleştirme](enrich-category-page.md). Belirli bir kataloğa özel zenginleştirme istiyorsanız, bu katalog için farklı ve benzersiz bir gezinti hiyerarşinizin olmasını öneririz.

### <a name="can-a-b2b-shopper-purchase-from-multiple-catalogs-in-a-single-checkout"></a>B2B müşterilerinin tek bir ödemede birden çok katalogdan satın alım yapması mümkün mü?

Evet, tek bir ödemede birden fazla katalogdan satın alınabilir. B2B müşterileri, hangi katalogdan hangi öğelerin eklendiğini belirlemek için sepet görünümündeki katalog göstergesini kullanabilir.

### <a name="if-a-b2b-shopper-purchases-the-same-item-from-different-catalogs-what-is-the-expected-behavior"></a>B2B müşterileri, farklı kataloglardan aynı öğeyi satın aldığında beklenen davranış ne olur?

Belirli bir kullanıcının belirli bir anda birden fazla kataloga erişimi olsa da, bu kataloglardaki ürünlerin birbirini dışlaması beklenir. Başka bir deyişle, aynı ürün, belirli bir kullanıcı için birden fazla katalogda olmamalıdır.

Ancak, aynı ürünün birden fazla katalogda olması durumunda sistem, o ürün için birden çok sepet satırı oluşturur. Her katalog için ayrı bir satır olacaktır. İki farklı katalogda bulunan aynı ürün, ödeme sırasında birleştirilmeyecektir.

### <a name="when-a-b2b-shopper-is-shopping-is-there-any-validation-for-catalog-availability"></a>B2B müşterileri alışveriş yaparken katalog kullanılabilirliğine ilişkin herhangi bir doğrulama var mıdır?

Evet. B2B müşterileri, yalnızca sepetteki tüm öğeler geçerli kataloglardan olduğunda ödeme sayfasına ilerleyebilir. Sepetteki öğelerin süresinin dolmuş veya geri çekilmiş olması durumunda bu öğeler sepetten kaldırılır ve kullanıcı bilgilendirilir.

### <a name="during-the-shopping-experience-are-search-and-product-discovery-including-related-and-recommended-product-collections-catalog-specific"></a>Alışveriş deneyimi sırasında arama ve ürün bulma (ilgili ve önerilen ürün koleksiyonları dahil) kataloğa özel mi?

Evet. Kullanıcı belirli bir kataloğu seçtiğinde, alışveriş sürecinin tamamı kataloğa özgü olur. Bu sürece, arama önerileri, arama sonuçları, kategori sonuçları, iyileştiriciler, fiyatlandırma, öznitelikler ve önerilen ürünler (yeni, en iyi satış, trend, bir arada satın alınan ve ilgili ürünler gibi) gibi ürün bulma deneyimleri dahildir.

### <a name="can-a-b2b-shopper-purchase-from-the-default-assortment-catalogid0"></a>B2B müşterileri, varsayılan ürün çeşitlerinden satın alabilir mi (catalogID=0)?

Hayır, B2B müşterilerinin varsayılan ürün çeşitlerinden satın almasına izin verilmez. Bu ürün çeşitleri, yalnızca anonim göz atma amaçlıdır. B2B müşterilerinin katalog atamaları yoksa (yönetiminden gelen bekleyen güncelleştirmeler), seçebilecekleri bir katalog göremezler ve hiçbir kategori hiyerarşisi görünür olmaz.

### <a name="can-marketing-content-be-curated-for-a-product-that-is-specific-to-a-catalog"></a>Kataloğa özel bir ürün için pazarlama içeriği oluşturulabilir mi?

Ürün zenginleştirme, şu an için yalnızca site ve kanal düzeylerinde desteklenir. Başka bir deyişle, bir ürün zenginleştirilir ve birden çok katalogda paylaşılırsa bu ürünün zenginleştirilmiş ürün ayrıntı sayfası (PDP), sitenin tüm kataloglarında aynı şekilde işlenir. 

### <a name="is-catalog-support-available-for-both-b2b-and-business-to-consumer-b2c-online-channels"></a>Katalog desteği hem B2B hem de işletmeler arası (B2C) çevrimiçi kanallar için kullanılabilir mi?

Commerce katalogları, şu an için yalnızca B2B çevrimiçi kanallarıyla çalışacak şekilde tasarlanmıştır.

### <a name="a-new-customer-was-added-to-the-customer-hierarchy-or-a-new-hierarchy-was-associated-with-the-catalog-but-the-catalog-is-not-available-to-the-user-why"></a>Müşteri hiyerarşisine yeni bir müşteri eklenmiş veya katalogla yeni bir hiyerarşi ilişkilendirilmiştir ancak katalog, kullanıcı için kullanılabilir değildir. Neden?

Yeni müşteriyi mevcut müşteri hiyerarşisiyle ilişkilendirdikten ve yeni bir müşteri hiyerarşisi oluşturduktan sonra **1010** işlerini çalıştırdığınızdan emin olun. Müşteri hiyerarşisi ile ilişkilendirilmiş kataloglar, yalnızca **1010** işleri başarıyla tamamlandıktan sonra görünür. Kataloğun da yeni olması halinde **1010** işlerine ek olarak **1150** (katalog) işini de çalıştırdığınızdan emin olun. Her yeni katalogda olduğu gibi verinin kanal ve arama dizininde eşitlenmesi için bekleyin. İş durumunun "Uygulandı" olması, verilerin kanal veri tabanı ile eşitlenmiş olduğu, ancak arama dizini ile eşitlenmesi için zaman gerektiği anlamına gelir. 

### <a name="can-we-set-up-catalog-specific-upsellcross-sell-items"></a>Kataloğa özel dikey satış/çapraz satış öğeleri ayarlayabilir miyiz?

Şimdilik yalnızca ilgili ürünler işlevi desteklenmektedir. Ancak, arama merkezleri için dikey ve çapraz satış öğe konfigürasyonları mevcuttur.

Aşağıdaki özellikler yalnızca çağrı merkezleri için desteklenir:

- Katalog kaynak kodları
- Maliyetleri ve yanıt oranlarını izlemek için kaynak kimliklerini kullanma
- Kataloğa özel sipariş ve öğe komut dosyaları
- Katalog sayfası analizi
- Katalog istekleri
- Ödeme planları
- Kaynak kodlarına dayalı serbest ürünler

### <a name="can-we-use-catalog-source-codes-for-b2b-orders-through-the-e-commerce-portal"></a>E-ticaret portalı aracılığıyla B2B siparişleri için katalog kaynak kodlarını kullanabilir miyiz?

Hayır. Katalog kaynak kodları yalnızca arama merkezi kanalları için desteklenir.

## <a name="additional-resources"></a>Ek kaynaklar

[B2B siteleri için ticari Katalog oluştur](catalogs-b2b-sites.md)

[Katalog seçicisi modülü](catalog-picker.md)

[B2B özelleştirmeleri için Commerce kataloglarının genişletilebilirlik etkisi](catalogs-b2b-sites-dev.md)
