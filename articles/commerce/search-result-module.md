---
title: Arama sonuçları modülü
description: Bu konu arama sonuçları modüllerini kapsamaktadır ve Microsoft Dynamics 365 Commerce'ün site sayfalarına nasıl ekleneceğini açıklamaktadır.
author: anupamar-ms
manager: annbe
ms.date: 01/28/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 5d852fe1a81b1e42484bc49ae136ef8613a2d3a5
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5254781"
---
# <a name="search-results-module"></a>Arama sonuçları modülü

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

Bu konu arama sonuçları modüllerini kapsamaktadır ve Microsoft Dynamics 365 Commerce'ün site sayfalarına nasıl ekleneceğini açıklamaktadır.

rama sonuçları modülü, ürün arama sonuçlarını ve ürünler için geçerli iyileştiricilerin bir listesini döndürür. Dynamics 365 Commerce sitelerindeki arama sonuçları modülleri, aşağıdaki senaryoların sayfalarını işlemek için kullanılabilir:

- Kullanıcı araması tarafından başlatılan arama sonuçları
- "Benzer ürün görünümleri" gibi belirli bir ürün kümesini gösteren arama sonuçları
- Belirli bir kategoriye ait olan ürün listeleri.

Kategori ve arama sonuçları sayfaları hakkında daha fazla bilgi için bkz. [Varsayılan kategori açılış sayfası ve arama sonuçları sayfasına genel bakış](category-search-page-overview.md).

Aşağıdaki resimde Fabrikam sitesindeki bir kategori için arama sonuçları sayfası örneği gösterilmektedir.

![Fabrikam sitesindeki arama sonuçları sayfası örneği](./media/SimpleCategoryLandingDressCategory.png)

## <a name="search-results-module-properties"></a>Arama sonuçları modülü özellikleri

Aşağıdaki tabloda, arama sonucu modüllerinin özellikleri, değerleri ve açıklamaları ile birlikte listelenmiştir.

| Özellik | Değerler | Tanım |
|----------|--------|-------------|
| Sayfa başına öğe sayısı | Tamsayı | Her sayfada gösterilen maddelerin sayısı. |
| PDP üzerinde yeniden izin ver | **Doğru** veya **yanlış** | Bu özellik **Doğru** olarak ayarlanırsa, kullanıcı arama sonuçları sayfasında bir ürün seçtiğinde, açılan ürün ayrıntıları sayfasındaki (PDP) içerik haritası gezintisi "Sonuçlara geri dön" bağlantısını gösterir. |
| İyileştiricileri genişlet | **Tümü**, **1**, **2**, **3** veya **4** | Bir sayfa yüklendiğinde genişletilmesi gereken en iyi iyileştiricilerin sayısı. Örneğin, bu özellik **3** olarak ayarlanırsa, sayfadaki ilk üç iyileştirici genişletilir. |
| Kategori hiyerarşisi görüntüsünü gizle | **Doğru** veya **yanlış** | Bu özellik **Doğru** olarak ayarlanırsa, sayfadaki kategori hiyerarşisi ekranı gizlenir. Kategori hiyerarşisini göstermek için [içerik haritası modülünü](add-breadcrumb.md) kullanıyorsanız bu özellik **Doğru** olarak ayarlanmalıdır.|
| Ürün özniteliklerini arama sonuçlarına dahil et | **Doğru** veya **yanlış** | Bu özellik **Doğru** olarak ayarlanırsa, arama sonuçlarındaki ürünler için öznitelikler döndürülür. Bu öznitelikler bir Ticaret sitesinde gösterilebilse de, bir uzantı gereklidir.|
| İlişki fiyatlarını göster | **Doğru** veya **yanlış** | Bu özellik **Doğru** olarak ayarlanırsa, oturum açmış bir kullanıcı sayfaya göz attığında, ürünlerin bağlı kuruluş fiyatları arama sonuçlarında gösterilir. |

> [!IMPORTANT]
> Dynamics 365 Commerce 10.0.16 sürümünde ve sonrasında, **Bağlı kuruluş fiyatlarını göster** yapılandırması, sayfada bağlı kuruluş fiyatlarını göstermek için kullanılabilir.

## <a name="supported-modules"></a>Desteklenen modüller

Arama sonuçları modülü, kullanıcıların ürün bilgilerini görüntülemesine ve bir arama sonuçları sayfasından alışveriş sepetine ürün eklemesine olanak veren [hızlı görüntüleme modülünü](quick-view-module.md) destekler.

## <a name="add-a-search-results-module-to-a-category-page"></a>Kategori sayfasına arama sonuçları modülü ekleme

Kategori sayfasına arama sonuçları modülü eklemek için bu adımları izleyin.

1. Bir yeni şablonu oluşturmak için **Şablonlar**'a gidin ve **Yeni**'yi seçin.
1. **Yeni şablon** iletişim kutusuna **Arama sonuçları** adını girin ve **Tamam**'ı seçin.
1. **Gövde** bölmesi için üç nokta (...) düğmesini seçin ve **Modül Ekle**'yi seçin.
1. **Modül Ekle** iletişim kutusunda **Varsayılan sayfa** modülünü seçin ve **Tamam**'ı seçin.
1. **Varsayılan sayfa** modülünde **Ana** bölmeyi seçin, üç nokta düğmesini (...) ve sonra **Modül ekle**'yi seçin.
1. **Modül Ekle** iletişim kutusunda **Konteyner** modülünü seçin ve **Tamam**'ı seçin.
1. **Konteyner** yuvası için üç nokta (...) düğmesini seçin ve **Modül Ekle**'yi seçin.
1. **Modül Ekle** iletişim kutusunda **İçerik haritası** modülünü seçin ve **Tamam**'ı seçin.
1. **İçerik haritası** özellikleri bölmesinde, **Min Gerçekleşme** için **1** değerini girin.
1. **Konteyner** yuvası için üç nokta (...) düğmesini seçin ve **Modül Ekle**'yi seçin.
1. **Modül Ekle** iletişim kutusunda, **Arama sonuçları** modülünü seçin ve **Tamam**'ı seçin.
1. **Arama sonuçları** özellikleri bölmesinde, **Min Gerçekleşme** için **1** değerini girin ve arama sonuçları modülü için gerekli diğer özellikleri ayarlayın. Şablonda bu özellikleri ayarlayarak, belirli bir kategori sayfasındaki özelleştirmelerin bu ayarları otomatik olarak içermesini sağlayabilirsiniz.
1. **Düzenlemeyi bitir**'i seçin, ardından şablonu yayımlamak için **Yayımla**'yı seçin.
1. **Sayfalar**'a gidin ve yeni sayfa oluşturmak için **Yeni**'yi seçin.
1. **Şablon seçin** iletişim kutusunda, oluşturduğunuz **Arama sonuçları** şablonunu seçin, **Sayfa adı** için **Kategori sayfası** girin ve sonra **Tamam**'ı seçin. Tüm değerler şablonda ayarlandığı için sayfa yayınlanmaya hazırdır.
1. Sayfayı iade etmek için **Düzenlemeyi bitir**'i seçin, ardından yayımlamak için **Yayımla**'yı seçin.

## <a name="additional-resources"></a>Ek kaynaklar

[Varsayılan kategori açılış sayfası ve arama sonuçları sayfasına genel bakış](category-search-page-overview.md)

[Modül kitaplığına genel bakış](starter-kit-overview.md)

[Hızlı görünüm modülü](quick-view-module.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]