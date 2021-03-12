---
title: Derecelendirmelere ve inceleme modülleri
description: Bu konu, Microsoft Dynamics 365 Commerce'un ürün ayrıntıları sayfalarında kullanılan derecelendirmeleri ve İnceleme modüllerini kapsamaktadır.
author: gvrmohanreddy
manager: annbe
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2020-10-31
ms.dyn365.ops.version: Release 10.0.6
ms.openlocfilehash: b17e986c2e30134c334cd547a85a1dd682172a0e
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/15/2021
ms.locfileid: "4979815"
---
# <a name="ratings-and-reviews-modules"></a>Derecelendirmelere ve inceleme modülleri

[!include [banner](includes/banner.md)]

Bu konu, Microsoft Dynamics 365 Commerce'un ürün ayrıntıları sayfalarında (PDP'ler) kullanılan derecelendirmeleri ve İnceleme modüllerini kapsamaktadır.

## <a name="overview"></a>Genel Bakış

E-ticaret web sitelerindeki derecelendirmeler ve incelemeler, müşterilere bir satın alma kararı vermeden önce ürünler hakkında bilgi edinmesine yardımcı olur ve ürünlerle ilgili müşteri geribildirimi toplama mekanizmasıdır. 

Derecelendirmeler, ürün listesi sayfalarında, kategori listesi sayfalarında, arama sonuçları sayfalarında ve diğer site sayfalarında gösterilir. 

Derecelendirme çubuk grafikleri ve ürün değerlendirmeleri, PDP'ler gösterilir. **Gözden geçirme yazma** düğmesi müşterilerin bir ürün için derecelendirme ve İnceleme göndermelerini sağlar. Bu PDP özellikleri derecelendirmelere göre denetlenir ve modülleri gözden geçirebilir.

## <a name="ratings-and-reviews-modules-on-pdps"></a>PDP'lerde derecelendirmelere ve inceleme modülleri 

Üç modül, PDP'ler üzerinde derecelendirme ve İnceleme özetini gösterir:
- Gözden geçirme yazma modülü
- Ürün değerlendirmeleri liste modülü
- Derecelendirme çubuk grafik modülü
 
Aşağıdaki şekil, bir PDP'de derecelendirmelerin ve gözden geçirme modüllerinin nasıl göründüğünü gösterir.

![PDP'de derecelendirmelere ve inceleme modülleri](media/rnr-eCommerce-pdp-reviews-modules_design.png)

> [!TIP] 
> PDP şablonlarını ve düzenlerini en iyi duruma getirme hakkında bilgi için (böylece e-ticaret sitenizde birden çok PDC arasındaki derecelendirme ve değerlendirme modülleriyle ilgili yapılandırmaları paylaşabilirsiniz) [şablonlar ve mizanpajlara genel bakış](templates-layouts-overview.md) konularına bakın.

Aşağıdaki şekil, **Modül Ekle** iletişim kutusunun Dynamics 365 Commerce'te derecelendirmeyi ve İnceleme modüllerini nasıl sunduğunu gösterir.
![Modül Ekle iletişim kutusu](media/rnr-eCommerce-pdp-adding-rnr-modules.png)

### <a name="write-review-module"></a>Gözden geçirme yazma modülü

İnceleme yazma modülü, kullanıcıların bir ürünü oturum açmalarını, derecelendirmesine ve bir ürün incelemesi yazmalarına olanak tanıyan bir **inceleme yaz** düğmesi içerir. Bu modül ayrıca kullanıcıların daha önceden gönderdikleri bir derecelendirme veya gözden geçirmelerini sağlar. Bu modül, bir PDP üzerinde genellikle derecelendirme çubuk grafiği ve ürün incelemeleri liste modüllerinin üzerinde görünür.
Aşağıdaki şekil, bir müşteri **gözden geçirme yaz** 'ı seçtiğinde beliren bir **gözden geçirme yazma** iletişim kutusunu göstermektedir. Müşteri bu iletişim kutusunu, bir derecelendirme ve İnceleme göndermek için kullanabilir.
![İnceleme yaz iletişim kutusu](media/rnr-eCommerce-write-review-module.png) Aşağıdaki tablo, geliştirme aracında konfigüre etmek için gereken yazma İnceleme modülünü gösterir.
| Özellik adı | Değer        | Özellik açıklaması                 |
|---------------|--------------|--------------------------------------|
| Dosya Adı          | İnceleme yaz | İnceleme yazma modülünün adı. |

### <a name="ratings-histogram-module"></a>Derecelendirme çubuk grafik modülü

Derecelendirmeler çubuk grafik modülü bir derecelendirme çubuk grafik gösterir. Bu modül tipik olarak, bir PDP üzerindeki İnceleme yazma modülü ile ürün değerlendirmeleri listesi modülü arasında görüntülenir.
Derecelendirme çubuk grafiği modülü için konfigürasyon gerekmez. Modülü PDP şablonuna eklemeniz yeterlidir. Aşağıdaki çizimler, PDP'lerde görüntülenmek üzere derecelendirmeler ve incelemeler modülleri yapılandırıldığında bir PDP şablonunun Dynamics 365 Commerce içinde nasıl göründüğünü gösterir.
![PDP'lerde görüntülenmek üzere derecelendirme ve İncelemeler yapılandırıldığında PDP şablonu](media/rnr-eCommerce-pdp-reviews-modules.png)

### <a name="product-reviews-list-module"></a>Ürün değerlendirmeleri liste modülü

Ürün gözden geçirme listesi modülü sıralama, filtre ve sayfalandırma seçenekleriyle birlikte ürün incelemelerinin listesini gösterir. Bu modül, genel olarak bir PDP üzerindeki derecelendirme çubuk grafik modülünden sonra görüntülenir.
Aşağıdaki tablo, geliştirme aracında konfigüre etmek için gereken ürün değerlendirmeleri listesi modülü özelliklerini gösterir.

| Özellik adı              | Değer | Özellik açıklaması |
|----------------------------|-------| ---------------------|
| her sayfada gösterilen incelemeler | 10    | PDP'de bir seferde gösterilmesi gereken gözden geçirme sayısı. Kullanıcıların gözden geçirme sayfalarında hareket edebilmesi için **sonraki** ve **önceki** düğmeler eklenmiştir. |

#### <a name="ratings-histogram--summary-view"></a>Derecelendirme çubuk grafiği – Özet görünümü

Ürün değerlendirmeleri listesi modülü, bir derecelendirme çubuk grafiği modülü ekleyebileceğiniz bir yuva içerir. Aşağıdaki şekil, Dynamics 365 Commerce'teki Ürün İncelemeleri listesi modülünde bir derecelendirme çubuk grafiği modülünü nasıl ekleyekullanabileceğinizi gösterir .

![Ürün eleştiriler listesi modülünde derecelendirme çubuk grafiği modülü ekleme](media/rnr-eCommerce-pdp-rating-histogram-summary.png)

## <a name="additional-resources"></a>Ek kaynaklar

[Modül kitaplığına genel bakış](starter-kit-overview.md)

[Kapsayıcı modülü](add-container-module.md)

[Alışveriş sepeti modülü](add-cart-module.md)

[Ödeme yapma modülü](add-checkout-module.md)

[Sipariş onayı modülü](order-confirmation-module.md)

[Üst bilgi modülü](author-header-module.md)

[Alt bilgi modülü](author-footer-module.md)
