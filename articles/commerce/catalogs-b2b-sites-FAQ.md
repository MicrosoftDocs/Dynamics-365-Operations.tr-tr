---
title: B2B için Commerce katalogları hakkında SSS
description: Bu makalede, Microsoft Dynamics 365 Commerce katalogları hakkında sık sorulan soruların yanıtları sağlanmaktadır.
author: ashishmsft
ms.date: 05/18/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: asharchw
ms.search.validFrom: 2022-02-28
ms.openlocfilehash: af69c3d27142a961049470dd1292ffbc3d8387a9
ms.sourcegitcommit: 6616b969afd6beb11a79d8e740560bf00016ea7f
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/17/2022
ms.locfileid: "9027380"
---
# <a name="commerce-catalogs-for-b2b-faq"></a>B2B için Commerce katalogları hakkında SSS

[!include [banner](includes/banner.md)]

Bu makalede, Microsoft Dynamics 365 Commerce [işletmeden işletmeye (B2B) katalogları](catalogs-b2b-sites.md) hakkında sık sorulan soruların yanıtları sağlanmaktadır.

## <a name="why-cant-i-configure-a-catalog-specific-navigation-hierarchy-or-see-an-option-to-associate-a-customer-hierarchy"></a>Kataloğa özel gezinti hiyerarşisini niçin konfigüre etmiyorum veya müşteri hiyerarşisini ilişkilendirme seçeneği göremiyor?

Commerce genel merkezinde **Özellik yönetimi** çalışma alanında **Perakende kanalları üzerinde çoklu katalog kullanımını etkinleştir** özelliğini etkinleştirdiğinizden emin olun. Ek olarak, ortamınızın Commerce sürüm 10.0.27 veya daha yeni sürümü kullanmasını sağlayın.

## <a name="can-i-view-the-catalog-specific-hierarchy-and-enrich-category-pages-in-commerce-site-builder"></a>Kataloğa özel hiyerarşiyi ve zenginleştirmeli kategori sayfalarını Commerce site oluşturucuda görebilir miyim?

Evet, site oluşturucuda **Ürünler** sayfasına erişimi olan Commerce site oluşturucu kullanıcıları bir katalog seçebilir ve kataloğa özel hiyerarşiyi görüntüleyebilir. **Ürünler** sayfasından, kullanıcılar katalogdaki belirli bir kategori için kategori sayfasını da zenginleştirebilirsiniz. Daha fazla bilgi için bkz. [Kategori giriş sayfasını zenginleştirme](enrich-category-page.md). Bir kataloğa özel zenginleştirme istiyorsanız, o katalog için farklı ve benzersiz bir gezinti hiyerarşinizin olmasını öneririz.

## <a name="can-a-b2b-shopper-purchase-from-multiple-catalogs-in-a-single-checkout"></a>Bir B2B alışverişçinin tek bir ödeme için çoklu kataloglardan satın alması mümkün mü?

Evet, tek bir ödeme için birden fazla kataloglardan satın almaya izin verilir. B2B alışverişçiler hangi maddelerin hangi kataloglardan eklendiğini belirlemek için sepet görünümündeki katalog göstergesini kullanabilir.

## <a name="if-a-b2b-shopper-purchases-the-same-item-from-different-catalogs-what-is-the-expected-behavior"></a>Bir B2B alışverişçisi farklı kataloglardan aynı maddeyi satın aldığında beklenen davranış nedir?

Belirli bir kullanıcının belirli bir anda birden fazla kataloga erişimi olsa da, bu katalogların içindeki ürünlerin birbirini dışlıyor olması da beklenmelidir. Başka bir deyişle, ideal olarak, belirli bir kullanıcı için aynı ürün birden fazla kataloğun parçası olmamalıdır.

Ancak, aynı ürünün birden çok katalogla ilgili olduğu bir durum ortaya çıkarsa, sistem o ürün için birden çok sepet satırı oluşturur. Her katalog için ayrı bir satır olacaktır. İki farklı katalogda bulunan aynı ürün, kullanıma alma sırasında birleştirilmeyecektir.

## <a name="when-a-b2b-shopper-is-shopping-is-there-any-validation-for-catalog-availability"></a>Bir B2B alışverişçinin alışveriş yaparken, katalog kullanılabilirliğine ilişkin herhangi bir doğrulama var mı?

Evet. Bir B2B alışverişçisi, yalnızca sepetteki tüm maddeler geçerli kataloglardan olduğunda kullanıma devam edecek şekilde izin verilir. Eğer herhangi bir alışveriş sepetinin süresi dolmuş veya geri çekilen kataloglarından biri varsa, bunlar kaldırılır ve Kullanıcı uyarılacaktır.

## <a name="during-the-shopping-experience-are-search-and-product-discovery-including-related-and-recommended-product-collections-catalog-specific"></a>Alışveriş deneyimi sırasında arama ve ürün bulma (ilgili ve önerilen ürün koleksiyonları dahil) kataloğa özel mi?

Evet. Kullanıcı belirli bir kataloğu seçtiğinde, tüm alışverişin kataloğu kataloğa özgüdür. Bu, arama önerileri, arama sonuçları, kategori sonuçları, iyileştiriciler, fiyatlandırma, öznitelikler ve önerilen ürünler (yeni, en iyi satış, trend, bir arada satın alınan ve ilgili ürünler gibi) gibi ürün bulma deneyimleri içerir.

## <a name="can-a-b2b-shopper-purchase-from-the-default-assortment-catalogid0"></a>Bir B2B alışverişçisi varsayılan sınıflamadan satın alabilir mi (catalogID=0)?

Hayır, bir B2B alışverişçinin varsayılan sınıflamadan satın alma yapmasına izin verilmez. Bu sınıflamanın yalnızca anonim gözatma amaçlı olduğu düşünülmüştür. Bir B2B alışverişçinin katalog atamaları eksikse (yönetiminden gelen bekleyen güncelleştirmeler), aralarından seçim yapabilen herhangi bir kataloğu göremez ve hiçbir kategori hiyerarşisi görünür olmayacaktır.

## <a name="can-marketing-content-be-curated-for-a-product-that-is-specific-to-a-catalog"></a>Kataloğa özel bir ürün için pazarlama içeriği eklenebilir mi?

Günümüzde, ürün zenginleştirme yalnızca site ve kanal düzeylerinde desteklenir. Başka bir deyişle, bir ürün zenginleştirilmez, birden çok katalog arasında paylaşılır ve ilgili ürün ayrıntılar sayfası (PDP) belirli bir sitenin tüm kataloglarında aynı şekilde işlenir.

## <a name="is-catalog-support-available-for-both-b2b-and-business-to-consumer-b2c-online-channels"></a>Katalog desteği hem B2B hem de işletmeler arası (B2C) çevrimiçi kanallar için kullanılabilir mi?

Geçerli olarak, Commerce katalogları yalnızca B2B kanallarıyla çalışacak şekilde tasarlanmıştır.

## <a name="can-we-set-up-catalog-specific-upsellcross-sell-items"></a>Kataloğa özel dikey satış/çapraz satış maddeleri ayarlayabilir miyiz?

Şimdilik yalnızca ilgili ürünler işlevi desteklenmektedir. Ancak, arama merkezleri için büyük satış ve çapraz satış madde konfigürasyonları mevcuttur.

Aşağıdaki özellikler yalnızca çağrı merkezleri için desteklenir:

- Katalog kaynak kodları
- Maliyetleri ve yanıt oranlarını izlemek için kaynak kimliklerini kullanma
- Kataloğa özel sipariş ve madde komut dosyaları
- Katalog sayfası analizi
- Katalog istekleri
- Ödeme planları
- Kaynak kodlarına dayalı serbest ürünler

## <a name="can-we-use-catalog-source-codes-for-b2b-orders-through-the-e-commerce-portal"></a>E-ticaret portalı aracılığıyla B2B siparişleri için katalog kaynak kodlarını kullanabilir misiniz?

Hayır. Katalog kaynak kodları yalnızca arama merkezi kanalları için desteklenir.

## <a name="additional-resources"></a>Ek kaynaklar

[B2B siteleri için ticari Katalog oluştur](catalogs-b2b-sites.md)

[B2B özelleştirmeleri için Commerce kataloglarının genişletilebilirlik etkisi](catalogs-b2b-sites-dev.md)
