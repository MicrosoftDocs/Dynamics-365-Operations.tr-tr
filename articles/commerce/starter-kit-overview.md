---
title: Modül kitaplığına genel bakış
description: Bu konu Microsoft Dynamics 365 Commerce modül kitaplığı hakkında bilgi sağlar.
author: anupamar-ms
manager: annbe
ms.date: 09/15/2020
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
ms.openlocfilehash: dfc52dd8e14bb2e9f2f9c026ee0e058aee4cedcb
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "4416498"
---
# <a name="module-library-overview"></a>Modül kitaplığına genel bakış

[!include [banner](includes/banner.md)]

Bu konu Microsoft Dynamics 365 Commerce modül kitaplığı hakkında bilgi sağlar.

## <a name="overview"></a>Genel bakış

Dynamics 365 Commerce modül kitaplığı, bir e-ticaret Web sitesi oluşturmak için kullanılabilen modüller topluluğudur. Modüllerin hem Kullanıcı arabirimi (UI) yönleri, hem de işlevsel davranış yönleri vardır.

Görünüm ve deneyimi değiştirmek için, Temalar, modül kitaplığındaki modüllere uygulanabilir. Temalar geçişli stil sayfaları (CSS) kullanır. "Fabrikam" adlı hayali bir e-ticaret sitesi için Tema, modül kitaplığının bir parçası olarak sağlanmıştır ve bir referans olarak kullanılabilir.

## <a name="module-library-modules"></a>Modül kitaplığı modülleri

Aşağıdaki modül türleri, modül kitaplığında sağlanmıştır:

- **Konteyner modülü** – Bir konteyner modülü, diğer modüller için ana bilgisayar görevi gören basit bir modüldür. İçinde olan modüllerin yerleşimini denetler.
- **Pazarlama modülleri** – Pazarlama modüllerinde engel, metin engeli, video oynatıcı ve döngü modüller bulunur. İçeriğin gösterimi için tüm bu modüller kullanılabilir. İçerik yönetimi sistemindeki (CMS) veriler tarafından yönlendiriliyor ve herhangi bir sayfaya konabilir.
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
