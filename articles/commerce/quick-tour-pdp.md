---
title: Ürün ayrıntıları sayfalarına genel bakış
description: Bu makale, Microsoft Dynamics 365 Commerce'ta ürün ayrıntıları sayfalarına (PDP'ler) genel bakış sağlar.
author: anupamar-ms
ms.date: 01/23/2020
ms.topic: overview
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.search.industry: ''
ms.search.form: ''
ms.openlocfilehash: 4856e6e208834d7dcc16d19ad4afb63c329a5868
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/12/2022
ms.locfileid: "9278513"
---
# <a name="product-details-pages-overview"></a>Ürün ayrıntıları sayfalarına genel bakış

[!include [banner](includes/banner.md)]

Bu makale, Microsoft Dynamics 365 Commerce'ta ürün ayrıntıları sayfalarına (PDP'ler) genel bakış sağlar.

PDP bir ürünle ilgili ayrıntılı bilgi sağlar ve müşteriler boyut, stil ve renk gibi ürün seçeneklerini seçsin. Bir PDP, bir müşterinin satın alma kararı vermek için gerek duyduğu tüm ürün bilgilerini sergilemelidir.

Aşağıdaki şekilde bir PDP örneği gösterilmiştir.

![Ürün ayrıntıları sayfası örneği.](./media/pdp.PNG)

## <a name="header-and-footer-modules"></a>Üst bilgi ve alt bilgi modülleri

PDP üst bölümünde, perakendecinin müşterilerin göz atmasını istediği tüm ürün kategorilerini ve diğer sayfaları gösteren bir başlık yer vardır. Sayfanın alt bölümünde, bir müşterilerin ilgilenebileceği çeşitli makalelerin hızlı bağlantılarını içeren bir altbilgi yer almaktadır.

## <a name="buy-box-module"></a>Satın alma kutusu modülü

Bir PDP üzerindeki en önemli modül, sayfanın ana bölümünde ilk öğe olarak görünen satın alma kutusu modülüdür. Satınalma kutusu modülü, ürün adı, ürün açıklaması, ürün fiyatı, ürün görüntüleri ve ürün derecelendirmeleri gibi önemli ürün bilgilerini gösterir.

Satın alma kutusu modülü müşterinin ürün seçeneklerini (örneğin, boyut, stil ve renk) seçmesini ve ürünü sepete eklemenizi sağlar. Ayrıca, müşterinin ürünü çevrimiçi olarak satın alıp bir mağaza içinde çekmesini sağlar. Çevrimiçi satın al ve kayıt depo modülünde, müşterinin belirttiği başka bir konumda yakındaki mağazaların veya mağazaların bulunması için Bing Haritalar uygulama programlama arabirimleriyle (API) tümleştirme kullanılır.

Satın alma kutusu modülü bir ürün kimliği gerektirir. Bu kod sayfa bağlamından türetilir. Bir satın alma kutusu modülü, sayfa içeriğinin ürün kimliği içerdiği bir sayfaya eklenirse, bilgileri doğru işlemez.

## <a name="product-specifications-module"></a>Ürün özellikleri modülü

Ürün belirtimleri modülü, ürünle ilgili ek ayrıntıları sergileyebilecek şekilde kullanılabilir. Bu Ayrıntılar Commerce'deki ürün özniteliklerinden alınmıştır. Ürün belirtimleri modülü, **görünür** özelliğinin **doğru** olarak ayarlandığı her özniteliği gösterir. Ürün özniteliklerini almak için ürün kodu gerekir.

## <a name="recommendations-module"></a>Ürün modülü

Öneriler modülü, PDP'de önemli modüldür. Müşteriler ürünlere göz atarken, doğru ürünü bulabilmeleri ve satın almak için daha fazla ürün seçeneği sunulmalıdır. Öneriler, müşterilerin ilgili içeriği kolayca bulmasına ve alışveriş yapmaya devam etmesine yardımcı olur.

Farklı öneri listesi türleri mevcuttur:

- **Bunları da sevdiler** listesi makine öğrenmeyi temel alır. Öneri sağlamak için diğer müşterilerin hareket geçmişini kullanır. Bu liste öneriler Servisi tarafından oluşturuldu ve "Bunu satın alan müşteriler de satın alınır..." gibi listelere benzer. Bu listeyi oluşturmak için bir ürün kimliği gereklidir.
- Commerce'de satılan bir ürün için **ilgili** bir liste konfigüre edilebilir. Örneğin, kahverengi bir deri yolculuğu el çantası için, deri temelli veya seyahat amacıyla tasarlanan diğer el çantaları ilgili liste için konfigüre edilebilir. Tıpkı **aksesuarlar** ve **Bunun gibi daha fazla** gibi diğer ilgili liste türleri de Commerce olarak konfigüre edilebilir. Bu listeyi oluşturmak için bir ürün kimliği gereklidir. Bu nedenle, sayfa içeriğinin bir ürün kimliği içerdiği bir giriş sayfasına eklenirse, liste boş olacaktır.
- Algoritmik oluşturulan öneri listeleri (örneğin, **Trend**, **en iyi satış** ve **yeni**), PDP'lerde kullanılabilir. Bu listeler PDP üzerindeki ürünle doğrudan ilişkili olmasa da, müşterileri ilgilendirebilecek ürünler bulmasına yardımcı olmanın başka bir yoludur. Bu tür listeler bir ürün kimliği gerektirmez. Bunlar, site genelinde alışveriş desenleri temel alınarak oluşturulan genel listelerdir.
- Düzenleme listeleri manue eklenen listelerdir. Örneğin, bir perakende, sergilemek istediği ürünlerin listesini el ile seçmeye karar verebilir.

## <a name="ratings-and-reviews-modules"></a>Derecelendirmelere ve inceleme modülleri

İncelemeleri göstermek ve eklemek için üç modül kullanılabilir:

- **İncelemeler** - Bu modülü, diğer müşteriler tarafından sağlanan derecelendirmeleri ve incelemeleri gösterir. Müşteriler İncelemeleri sıralayabilir ve süzebilir. Bu modül aynı zamanda müşterileri gözden geçirsin veya bunları beğenmediğiniz gibi sorunları rapor edin.
- **Derecelendirme yazma** – bu modül, müşterilerinin bir ürünle ilgili incelemeleri yazalım.
- **Derecelendirme histogramı** – bu modül, bir ürünle ilgili derecelendirme eğilimini gösteren bir histogram içerir.

Daha fazla bilgi için bkz: [Derecelendirme ve incelemeler genel bakışı](ratings-reviews-overview.md).

## <a name="marketing-modules"></a>Pazarlama modülleri

Belirli bir ürünle ilgili pazarlama içeriği benzersiz ise, tüm pazarlama modülleri PDP'ye eklenebilir. Bir PDC'ye, sayfaya "zenginleştirme" uygulayarak pazarlama modülleri ekleyebilirsiniz. Daha fazla ayrıntı için, bkz. [ürün sayfası zenginleştirme](enrich-product-page.md).

## <a name="additional-resources"></a>Ek kaynaklar

[Giriş sayfasına genel bakış](quick-tour-home-page.md)

[Sepet ve ödeme sayfalarına genel bakış](quick-tour-cart-checkout.md)

[Hesap yönetimi sayfalarına genel bakış](quick-tour-account-management.md)

[Ürün ayrıntıları sayfasını zenginleştirme](enrich-product-page.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
