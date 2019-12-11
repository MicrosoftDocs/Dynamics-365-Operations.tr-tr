---
title: Ürün ayrıntıları sayfalarına genel bakış
description: Bu konu, Microsoft Dynamics 365 Commerce'ta ürün ayrıntıları sayfalarına (PDP'ler) genel bakış sağlar.
author: anupamar-ms
manager: annbe
ms.date: 10/31/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 3b02d50adbfcda27d590bcb87fd9669d67d4a01c
ms.sourcegitcommit: 295d940a345879b3dfc5991e387b91c7257019ea
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/01/2019
ms.locfileid: "2697877"
---
# <a name="overview-of-product-details-pages"></a>Ürün ayrıntıları sayfalarına genel bakış

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

Bu konu, Microsoft Dynamics 365 Commerce'ta ürün ayrıntıları sayfalarına (PDP'ler) genel bakış sağlar.

## <a name="overview"></a>Genel Bakış

PDP bir ürünle ilgili ayrıntılı bilgi sağlar ve müşteriler boyut, stil ve renk gibi ürün seçeneklerini seçsin. Bir PDP, bir müşterinin satın alma kararı vermek için gerek duyduğu tüm ürün bilgilerini sergilemelidir.

Aşağıdaki şekilde bir PDP örneği gösterilmiştir.

![Ürün ayrıntıları sayfası örneği](./media/pdp.PNG)

## <a name="header-and-footer-modules"></a>Üst bilgi ve alt bilgi modülleri

PDP üst bölümünde, perakendecinin müşterilerin göz atmasını istediği tüm ürün kategorilerini ve diğer sayfaları gösteren bir başlık yer vardır. Sayfanın alt bölümünde, bir müşterilerin ilgilenebileceği çeşitli konularda hızlı bağlantılar içeren bir altbilgi yer almaktadır.

## <a name="buy-box-module"></a>Satınalma kutusu modülü

Bir PDP üzerindeki en önemli modül satın alma kutusu modülüdür. Bu nedenle, sayfanın ana bölümündeki ilk öğe olur. Satın alma kutusu modülü bir konteyner modülüdür ve ürünle ilgili en önemli bilgileri içeren birkaç modülü barındırır. Bu bilgiler ürün adını, ürün görüntülerini, açıklamayı, fiyatı ve ürün derecelendirmelerini içerir.

Satın alma kutusu modülü müşterinin ürün seçeneklerini (örneğin, boyut, stil ve renk) seçmesini ve ürünü sepete eklemenizi sağlar. Ayrıca, müşterinin ürünü çevrimiçi olarak satın alıp bir mağaza içinde çekmesini sağlar. Çevrimiçi satın al ve kayıt depo modülünde, müşterinin belirttiği başka bir konumda yakındaki mağazaların veya mağazaların bulunması için Bing Haritalar uygulama programlama arabirimleriyle (API) tümleştirme kullanılır.

Satın alma kutusu modülü bir ürün kimliği gerektirir. Bu kod sayfa bağlamından türetilir. Bir satın alma kutusu modülü, sayfa içeriğinin ürün kimliği içerdiği bir sayfaya eklenirse, bilgileri doğru işlemez.

## <a name="product-specifications-module"></a>Ürün özellikleri modülü

Ürün belirtimleri modülü, ürünle ilgili ek ayrıntıları sergileyebilecek şekilde kullanılabilir. Bu Ayrıntılar Dynamics 365 Retail'deki ürün özniteliklerinden alınmıştır. Ürün belirtimleri modülü, **görünür** özelliğinin **doğru** olarak ayarlandığı her özniteliği gösterir. Ürün özniteliklerini almak için ürün kodu gerekir.

## <a name="recommendations-module"></a>Ürün modülü

Öneriler modülü, PDP'de önemli modüldür. Müşteriler ürünlere göz atarken, doğru ürünü bulabilmeleri ve satın almak için daha fazla ürün seçeneği sunulmalıdır. Öneriler, müşterilerin ilgili içeriği kolayca bulmasına ve alışveriş yapmaya devam etmesine yardımcı olur.

Farklı öneri listesi türleri mevcuttur:

- **Bunları da sevdiler** listesi makine öğrenmeyi temel alır. Öneri sağlamak için diğer müşterilerin hareket geçmişini kullanır. Bu liste öneriler Servisi tarafından oluşturuldu ve "Bunu satın alan müşteriler de satın alınır..." gibi listelere benzer. Bu listeyi oluşturmak için bir ürün kimliği gereklidir.
- Perakende satılan bir ürün için **ilgili** bir liste konfigüre edilebilir. Örneğin, kahverengi bir deri yolculuğu el çantası için, deri temelli veya seyahat amacıyla tasarlanan diğer el çantaları ilgili liste için konfigüre edilebilir. Tıpkı **aksesuarlar** ve **Bunun gibi daha fazla** gibi diğer ilgili liste türleri de perakende olarak konfigüre edilebilir. Bu listeyi oluşturmak için bir ürün kimliği gereklidir. Bu nedenle, sayfa içeriğinin bir ürün kimliği içerdiği bir giriş sayfasına eklenirse, liste boş olacaktır.
- Algoritmik oluşturulan öneri listeleri (örneğin, **Trend**, **en iyi satış** ve **yeni**), PDP'lerde kullanılabilir. Bu listeler PDP üzerindeki ürünle doğrudan ilişkili olmasa da, müşterileri ilgilendirebilecek ürünler bulmasına yardımcı olmanın başka bir yoludur. Bu tür listeler bir ürün kimliği gerektirmez. Bunlar, site genelinde alışveriş desenleri temel alınarak oluşturulan genel listelerdir.
- Düzenleme listeleri manue eklenen listelerdir. Örneğin, bir perakende, sergilemek istediği ürünlerin listesini el ile seçmeye karar verebilir.

## <a name="ratings-and-reviews-module"></a>Derecelendirmelere ve inceleme modülleri

Derecelendirmeler ve İncelemeler modülü, diğer müşteriler tarafından sağlanan derecelendirmeleri ve incelemeleri gösterir. Ayrıca, bir müşterinin ürünün incelemesini kendi başına yazması da sağlar. Ek olarak, ürünle ilgili derecelendirme eğilimini gösteren bir histogram da içerir. Daha fazla bilgi için bkz: [Derecelendirme ve incelemeler genel bakışı](ratings-reviews-overview.md).

## <a name="marketing-modules"></a>Pazarlama modülleri

Belirli bir ürünle ilgili pazarlama içeriği benzersiz ise, tüm pazarlama modülleri PDP'ye eklenebilir. Bir PDC'ye, sayfaya "zenginleştirme" uygulayarak pazarlama modülleri ekleyebilirsiniz. 

## <a name="additional-resources"></a>Ek kaynaklar

[Giriş sayfasına genel bakış](quick-tour-home-page.md)

[Varsayılan kategori açılış sayfası ve arama sonuçları sayfasına genel bakış](category-search-page-overview.md)

[Sepet ve ödeme sayfalarına genel bakış](quick-tour-cart-checkout.md)

[Hesap yönetimi sayfalarına genel bakış](quick-tour-account-management.md)
