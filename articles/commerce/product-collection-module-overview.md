---
title: Ürün topluluğu modülleri
description: Bu konu Microsoft Dynamics 365 Commerce'ta ürün koleksiyonu modülleriyle ilgili genel bir bakış sağlar.
author: v-chgri
manager: annbe
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Operations, Retail, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: asharchw
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 44f78b55b8e67b7358be75aa63c40a0147507e26
ms.sourcegitcommit: 3a4e137ef3a96ba0a58c5352f4a3b57467ace9ae
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/11/2019
ms.locfileid: "2785479"
---
# <a name="product-collection-modules"></a>Ürün topluluğu modülleri  

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

Bu konu Microsoft Dynamics 365 Commerce'ta ürün koleksiyonu modülleriyle ilgili genel bir bakış sağlar.

## <a name="overview"></a>Genel Bakış

Ürün bulma, perakendecilerin müşterileri e-ticaret Web sitesinde kullanmak için kullandıkları birincil araçtır. Ürün koleksiyonu modülleri, perakende olarak hızlı bir şekilde yazmak için kullanılabilen sezgisel bir görsel arabirim sağlayarak, perakendecilere çekici alışveriş deneyimleri oluşturur.

Ürün koleksiyonu modülleri, Web sitesindeki fiziksel ürünleri ve hizmetleri temsil eder. Ürün koleksiyonu modülü genellikle müşterilerin bir ürün veya hizmet satın alabileceği Ayrıntılar sayfasıyla bağlantılıdır veya bu konuda bilgi edinebilirsiniz. 

Ürün koleksiyonları için kaynaklar şu üç tür listeler olabilir:

- Bir ürün veya ürün listesi ile ilgili ürünler olarak Dynamics 365 Retail'de el ile tanımlanan ürünlerin düzenleme listeleri
- Yeni, en iyi satış veya trend ürünlerinin listesi gibi Algoritmik listeler
- Makine öğrenmeyi esas alan öneri listeleri

Aşağıdaki resimde bir e-ticaret sitesinde kullanılan farklı ürün koleksiyonları türleri gösterilmektedir.

![Bir e-ticaret sitesinde farklı türde ürün koleksiyonları örneği](./media/ProductCollectionsAcrossTheSiteUseProductPlacement.png)

> [!NOTE]
> Benzer türdeki veya temadaki bir ürün grubunu göstermek için her zaman ürün koleksiyonu modüllerini kullanın.

## <a name="product-collection-modules-and-types"></a>Ürün topluluğu modülleri ve türleri

Aşağıdaki tabloda, Dynamics 365 Commerce'de çeşitli türlerdeki ürün koleksiyonu modülleri açıklanmıştır.

| Ürün topluluğu modülü  | Türü | Tanım |
|----------------------------|------|-------------|
| Kategorilere gözatma            | Düzenleme | Bu tür ürün toplama modülü, perakende kanalı için perakendecinin, belirli bir site kategorisinde sunulan ürünlerin gözatma akışını göstermesi için oluşturulan gezinti kategorisi hiyerarşisini kullanır. |
| Arama sonuçları             | Arama sorgusu | Bu tür bir ürün toplama modülü, müşterinin girdiği arama sorgusuyla en iyi şekilde eşleşen ürünlerin listesini gösterir. |
| İlgili ürünler           | Düzenleme | Bu tür bir ürün toplama modülü, yazarın seçtiği ilişki türü için, ticaret yöneticisinin Retail'de ilgili ürünler olarak konfigüre eden ürünlerin listesini gösterir. |
| Seçkin ürün listeleri      | Düzenleme | Bu tür ürün toplama modülü, tacirler ve editörler tarafından perakende olarak oluşturulan özel listeleri gösterir. |
| Yeni                        | Algoritmik | Bu tür ürün toplama modülü, kanallar ve kataloglarda sıralanan en yeni ürünlerin listesini gösterir. |
| En iyi satış               | Algoritmik | Bu tür bir ürün toplama modülü, en yüksek sayıda satış tarafından derecelendirilen ürünlerin listesini gösterir. |
| Popüler                   | Algoritmik | Bu tür bir ürün toplama modülü belirli bir döneme ait en yüksek performanslı ürünlerin listesini gösterir. |
| Sıklıkla birlikte satın alınan | Yapay Zeka/Makine öğrenme | Bu tür ürün toplama modülü, tüketici satın alma düzenlerini analiz etmek ve belirli bir ürünle birlikte satın alınan ilgili öğeleri önermek için makine öğrenmeyi kullanır. |
| Diğer sevilen ürünler           | Yapay Zeka/Makine öğrenme | Bu tür ürün toplama modülü, tüketici satın alma düzenlerini analiz etmek ve belirli bir ürünle ilgili öğeleri önermek için makine öğrenmeyi kullanır. |

## <a name="add-a-product-collection-module-to-a-category-page"></a>Kategori sayfasına ürün koleksiyonu modülü ekleme

Kategori sayfasına ürün koleksiyonu modülü eklemek için bu adımları izleyin.

1. Dynamics 365 Commerce içinde sitenize gidin ve varsayılan kategori sayfanız olarak aynı şablonu kullanan bir sayfa oluşturun.
1. Sayfa anahattında **Alt bilgi** yuvayı seçin, üç nokta düğmesini (**...**) ve sonra **Modül ekle**'yi seçin.
1. **Modül Ekle** iletişim kutusunda **konteyner**i seçin ve **Tamam**'ı seçin.
1. Konteyner modülünde, üç nokta düğmesini seçin ve sonra **Modül ekle**'yi seçin.
1. **Modül Ekle** iletişim kutusunda **Ürün koleksiyonu**'nu seçin ve **Tamam**'ı seçin.
1. Ayarları, ürün koleksiyonu için uygun bir veri kaynağı ve girişler seçerek konfigüre edin.
1. Ürün koleksiyonu modülüyle ilgili Özellikler bölmesinde, **Ürün listesi ekle**'yi seçin.
1. **Ürün listesi konfigürasyonu seç** iletişim kutusunda liste türünü seçin, öğe sayısını girin ve liste türü için kullanılabilen diğer seçenekleri belirleyin. Liste türleri hakkında daha fazla bilgi için, aşağıdaki tabloya bakın. 
1. **Tamam**'ı seçin.
1. Sayfayı kaydet ve yayımlayın.

Aşağıdaki tabloda, **Ürün listesi konfigürasyonu seç** iletişim kutusunda seçim için kullanılabilen liste türleri gösterilmiştir.
   
| Türü                       | Tanım | Genel uygulama | Sayfa bağlamından türetilebilecek bağlam | Yazarın sayfa bağlamını geçersiz kılabileceği bağlam |
|----------------------------|-------------|------------------|-------------------------------------|-----------------------------------------------|
| Kategoriye göre ürünler       | Belirli bir kategoriye ait olan ürünlerin listesi. Bu kategori sayfa bağlamından veya yazarın sağladığı içerikten belirlenir. | Zenginleştirme kategorisi sayfası, giriş sayfası, kullanıma alma ve sepet sayfaları ve ürün sayfaları | Kategori | Yazarın belirlediği kategori |
| İlgili ürünler           | İlişki türü için perakende olarak ilgili ürünler olarak ticari bir yöneticinin konfigüre eden ürünlerin listesi. | Ürün sayfaları, kullanıma alma ve sepet sayfaları, istek listesi sayfası ve müşteri hesabı sayfası | Ürün, ilişki türü (Zorunlu)  | Ürün, ilişki türleri |
| Oluşturuldu                    | Perakende olarak tacirler ve düzenleyicilerin oluşturulduğu özel liste. | Zenginleştirme kategorisi sayfası, giriş sayfası, kullanıma alma ve sepet sayfaları ve ürün sayfaları | Uygulanamaz | Liste seçici |
| Algoritmik                | <ul><li>**Yeni** – kanallara ve kataloglara önceden sıralanmış en yeni ürünlerin listesi.</li><li>**En çok satan** – en yüksek sayıda satış ile derecelendirilen ürünlerin listesi.</li><li>**Trend** – belirli bir döneme ait en yüksek performanslı ürünlerin listesi.</li></ul> | Giriş sayfası, zenginleştirme kategorisi sayfası, kullanıma alma ve sepet sayfaları | Kategori | Yazarın belirlediği kategori |
| Sıklıkla birlikte satın alınan | Bir liste, tüketici satın alma düzenlerini analiz etmek ve belirli bir ürünle birlikte satın alınan ilgili öğeleri önermek için makine öğrenmeyi kullanır. | Ürün sayfaları ve kullanıma alma ve sepet sayfaları | Ürün, sepet | Sepeti Dahil Et |
| Diğer sevilen ürünler           | Bir liste, tüketici satın alma düzenlerini analiz etmek ve belirli bir ürünle ilgili öğeleri önermek için makine öğrenmeyi kullanır. | Ürün sayfaları ve kullanıma alma ve sepet sayfaları | Ürün, sepet | Uygulanamaz |

## <a name="additional-resources"></a>Ek kaynaklar

[Başlangıç paketine genel bakış](starter-kit-overview.md)

[Döngü modülü](add-carousel.md)

[İçerik zengin blok modülü](add-content-rich-block.md)

[İçerik yerleşimi modülü](add-content-placement-modules.md)

[Konteyner modülü](add-container-module.md)

[Satınalma kutusu modülü](add-buy-box.md)

