---
title: Arama sonuçları modülü
description: Bu makale arama sonuçları modüllerini kapsamaktadır ve Microsoft Dynamics 365 Commerce'ün site sayfalarına nasıl ekleneceğini açıklamaktadır.
author: anupamar-ms
ms.date: 08/31/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.8
ms.search.industry: ''
ms.search.form: ''
ms.openlocfilehash: eeb7cd0769fcb866a3d7dcc03e8e87daf24b2c5d
ms.sourcegitcommit: 1d5cebea3e05b6d758cd01225ae7f566e05698d2
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/02/2022
ms.locfileid: "9405306"
---
# <a name="search-results-module"></a>Arama sonuçları modülü

[!include [banner](includes/banner.md)]

Bu makale arama sonuçları modüllerini kapsamaktadır ve Microsoft Dynamics 365 Commerce'ün site sayfalarına nasıl ekleneceğini açıklamaktadır.

rama sonuçları modülü, ürün arama sonuçlarını ve ürünler için geçerli iyileştiricilerin bir listesini döndürür. Dynamics 365 Commerce sitelerindeki arama sonuçları modülleri, aşağıdaki senaryoların sayfalarını işlemek için kullanılabilir:

- Kullanıcı araması tarafından başlatılan arama sonuçları
- "Benzer ürün görünümleri" gibi belirli bir ürün kümesini gösteren arama sonuçları
- Belirli bir kategoriye ait olan ürün listeleri.

Kategori ve arama sonuçları sayfaları hakkında daha fazla bilgi için bkz. [Varsayılan kategori açılış sayfası ve arama sonuçları sayfasına genel bakış](category-search-page-overview.md).

Aşağıdaki resimde Fabrikam sitesindeki bir kategori için arama sonuçları sayfası örneği gösterilmektedir.

![Fabrikam sitesindeki arama sonuçları sayfası örneği.](./media/SimpleCategoryLandingDressCategory.png)

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
| İyileştirici panelini güncelleştir | **Doğru** veya **yanlış** | Bu özellik **doğru** olarak ayarlanırsa, iyileştiriciler seçildiğinde iyileştirici paneli güncelleştirilir. Bu modda, bazı çok seçimli iyileştiriciler, iyileştirici paneli güncelleştirildiğinde tek seçimli iyileştiriciler gibi davranır. |

> [!IMPORTANT]
> Commerce 10.0.16 sürümünde ve sonrasında, **Bağlı kuruluş fiyatlarını göster** yapılandırması, sayfada bağlı kuruluş fiyatlarını göstermek için kullanılabilir.
>
> Commerce sürüm 10.0.20 sürümünde ve daha sonra, iyileştirici seçiminde iyileştiriciyi güncelleştirmek için kullanılabilen **İyileştirici panelini güncelleştir** yapılandırmasını güncelleştirmek için kullanılabilir.

## <a name="supported-modules"></a>Desteklenen modüller

Arama sonuçları modülü, kullanıcıların ürün bilgilerini görüntülemesine ve bir arama sonuçları sayfasından alışveriş sepetine ürün eklemesine olanak veren [hızlı görüntüleme modülünü](quick-view-module.md) destekler.

## <a name="add-a-search-results-module-to-a-category-page"></a>Kategori sayfasına arama sonuçları modülü ekleme

Site oluşturucuda bir kategoriye arama sonuçları modülünü eklemek için aşağıdaki adımları izleyin.

1. Bir yeni şablonu oluşturmak için **Şablonlar**'a gidin ve **Yeni**'yi seçin.
1. **Yeni şablon** iletişim kutusuna **Arama sonuçları** adını girin ve **Tamam**'ı seçin.
1. **Gövde** alanında, üç nokta (...) düğmesini seçin ve **Modül ekle**'yi seçin.
1. **Modülleri seç** iletişim kutusunda **Varsayılan Sayfa** modülünü seçin ve **Tamam**'ı seçin.
1. **Varsayılan sayfa** modülündeki **Ana** alanında, üç nokta düğmesini (...) ve ardından **Modül ekle**'yi seçin.
1. **Modül seç** iletişim kutusunda **Konteyner** modülünü seçin ve **Tamam**'ı seçin.
1. **Konteyner** alanında, üç nokta (...) düğmesini seçin ve **Modül ekle**'yi seçin.
1. **Modülleri seç** iletişim kutusunda **İçerik haritası** modülünü seçin ve **Tamam**'ı seçin.
1. **İçerik haritası** özellikleri bölmesinde, **Min Gerçekleşme** için **1** değerini girin.
1. **Konteyner** alanında, üç nokta (...) düğmesini seçin ve **Modül ekle**'yi seçin.
1. **Modülleri seç** iletişim kutusunda, **Arama sonuçları** modülünü seçin ve **Tamam**'ı seçin.
1. **Arama sonuçları** özellikleri bölmesinde, **Min Gerçekleşme** için **1** değerini girin ve arama sonuçları modülü için gerekli diğer özellikleri ayarlayın. Şablonda bu özellikleri ayarlayarak, belirli bir kategori sayfasındaki özelleştirmelerin bu ayarları otomatik olarak içermesini sağlayabilirsiniz.
1. **Düzenlemeyi bitir**'i seçin, ardından şablonu yayımlamak için **Yayımla**'yı seçin.
1. **Sayfalar**'a gidin ve yeni sayfa oluşturmak için **Yeni**'yi seçin.
1. **Yeni sayfa oluştur** iletişim kutusunda **Sayfa adı** altında, **Kategori sayfası**'nı girin ve **Tamam**'ı seçin.
1. **Şablon seç** bölümünde, oluşturduğunuz **Arama sonuçları** şablonunu seçin ve sonra **İleri**'yi seçin.
1. **Bir düzen seçin** bölümünde, bir sayfa düzeni seçin (ör. **Esnek düzen**) ve sonra **İleri**'yi seçin.
1. **İnceleyin ve bitirin** bölümünde, sayfa yapılandırmasını gözden geçirin. Sayfa bilgilerini düzenlemeniz gerekiyorsa, **Geri**'yi seçin. Sayfa bilgileri doğruysa, **Sayfa oluştur**'u seçin.
1. Sayfayı iade etmek için **Düzenlemeyi bitir**'i seçin, ardından yayımlamak için **Yayımla**'yı seçin.

## <a name="inventory-aware-search-results-module"></a>Stoğa duyarlı arama sonuçları modülü

Arama sonuçları modülü, envanter verilerini içerecek ve aşağıdaki deneyimleri sağlayacak şekilde yapılandırılabilir:

- Stok düzeyi etiketlerini ürünlerle birlikte görüntüleme.
- Stok dışı ürünleri ürün listesinden gizleyin.
- Ürün listesinin sonunda stok dışı ürünleri gösterme.
- Stok tabanlı ürün filtrelemeyi destekleme.

Bu deneyimleri etkinleştirmek için, öncelikle Commerce headquarters'ta **Stoğa duyarlı olacak şekilde geliştirilmiş e-Ticaret ürün keşfi** özelliğini ve ardından bazı önkoşul ayarlarını etkinleştirmeniz gerekir. Daha fazla bilgi için bkz. [Stoğa duyarlı ürün listelemesi](inventory-aware-product-listing.md).

## <a name="additional-resources"></a>Ek kaynaklar

[Varsayılan kategori açılış sayfası ve arama sonuçları sayfasına genel bakış](category-search-page-overview.md)

[Modül kitaplığına genel bakış](starter-kit-overview.md)

[Hızlı görünüm modülü](quick-view-module.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
