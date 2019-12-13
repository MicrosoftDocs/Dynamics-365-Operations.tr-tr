---
title: Başlangıç paketine genel bakış
description: Bu konu Microsoft Dynamics 365 Commerce başlangıç kiti hakkında bilgi sağlar.
author: anupamar-ms
manager: annbe
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: 73af7fc8845fe08bc4aa014abe4d8c6dcf7ccb7d
ms.sourcegitcommit: 3a4e137ef3a96ba0a58c5352f4a3b57467ace9ae
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/11/2019
ms.locfileid: "2785272"
---
# <a name="starter-kit-overview"></a>Başlangıç paketine genel bakış

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

Bu konu Microsoft Dynamics 365 Commerce başlangıç kiti hakkında bilgi sağlar.

## <a name="overview"></a>Genel Bakış

Dynamics 365 Commerce başlangıç kiti, bir e-ticaret Web sitesi oluşturmak için kullanılabilen modüller topluluğudur. Modüllerin hem Kullanıcı arabirimi (UI) yönleri, hem de işlevsel davranış yönleri vardır.

Görünüm ve hissini değiştirmek için, Temalar, başlangıç setlerindeki modüllere uygulanabilir. Temalar geçişli stil sayfaları (CSS) kullanır. "Fabrikam" adlı hayali bir e-ticaret sitesi için Tema, başlangıç kitinin bir parçası olarak sağlanmıştır ve bir referans olarak kullanılabilir.

## <a name="starter-kit-modules"></a>Başlangıç kiti modülleri

Aşağıdaki modül türleri, başlangıç kitinde sağlanmıştır:

- **Konteyner modülü** – Bir konteyner modülü, diğer modüller için ana bilgisayar görevi gören basit bir modüldür. İçinde olan modüllerin yerleşimini denetler.
- **Pazarlama modülleri** – Pazarlama modüllerinde hero, özellik, içerik yerleşimi, içerik zengin blok, video oynatıcı ve döngü modüller bulunur. İçeriğin gösterimi için tüm bu modüller kullanılabilir. İçerik yönetimi sistemindeki (CMS) veriler tarafından yönlendiriliyor ve herhangi bir sayfaya konabilir.
- **Üstbilgi ve altbilgi modülleri** – Üstbilgi ve altbilgi modülleri, tüm site sayfalarının üstbilgi ve altbilgisinde görüntülenir. Bu modüller, özellikler üzerinden gerektikçe yapılandırılabilir.
- **Arama modülleri** – Başlıktaki arama modülü kullanılarak ürünler keşfedilebilir. Arama sonuçları arama sonuçları sayfasında görünür. Ürünler, kanal gezinti hiyerarşisinde desteklenen her kategori için adanmış sayfalar olan Kategori sayfalarında da bulunabilir. Ek olarak, iyileştirici modülleri arama sonuçları ve kategori sayfalarındaki sonuçlara ek filtre uygulamak için kullanılabilir.
- **Ürün ayrıntıları sayfası modülleri** – Ürün ayrıntıları sayfaları ürün bilgilerini göstermek için birkaç modül kullanır. Satın alma kutusu modülü müşterilerin ürünleri görüntülemesine ve bunları alışveriş sepetine eklemesine olanak tanır. Teknik özellikler modülü gibi diğer modüller ürün ayrıntılarını gösterir. Derecelendirmeler ve incelemeler modülü incelemeleri görüntülemek ve sağlamak için kullanılabilir.
- **Mağaza modülünde çevrimiçi mağazadan satın alın** – depo modülünde çevrimiçi mağazadan satın alma , Bing Haritalar ile tümleşiktir. Satın aldıkları ürünlerin nereden çekilebileceği, yakındaki mağazaların bulunması için kullanılabilir.
- **Satın alma modülleri** – Satın alma modülleri, alışveriş sepetine madde eklemek için kullanılabilen sepet modülünü içerir. Kullanıma alma modülü sevkiyat adresini, teslimat seçeneklerini ve hediye kartını, bağlılık programı ve kredi kartı bilgilerini yakalar ve böylece bir sipariş işlenebilir. Bir sipariş yerleştirildikten sonra, onay ayrıntılarını göstermek için sipariş teyidi modülü kullanılabilir.
- **Hesap yönetimi modülleri** – oturum açma modülü müşterilerinin varolan bir hesapla oturum açmasına izin verir ve kaydolma modülü de yeni bir hesap oluşturur. Bir hesap oluşturulduktan sonra, sipariş geçmişi modülü en son siparişleri görüntülemek için kullanılabilir ve sipariş ayrıntıları modülü sipariş ayrıntılarını görüntülemek için kullanılabilir.
- **Öneriler modülü** – Öneriler, ürün yerleştirme modülü kullanılarak gösterilir. Bu modül herhangi bir sayfada gezinebilecek algoritmik ve düzenleme listelerini destekler.

## <a name="additional-resources"></a>Ek kaynaklar

[Konteyner modülü](add-container-module.md)

[Satınalma kutusu modülü](add-buy-box.md)

[Sepet modülü](add-cart-module.md)

[Ödeme modülü](add-checkout-module.md)

[Sipariş onayı modülü](order-confirmation-module.md)

[Üst bilgi modülü](author-header-module.md)

[Alt bilgi modülü](author-footer-module.md)
