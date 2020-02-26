---
title: Ürün topluluğu modülleri
description: Bu konu Microsoft Dynamics 365 Commerce'ta ürün koleksiyonu modülleriyle ilgili genel bir bakış sağlar.
author: v-chgri
manager: annbe
ms.date: 01/07/2020
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
ms.openlocfilehash: 069fa1cb6acad4b8d6618cebb754cbc0892ca9cf
ms.sourcegitcommit: 829329220475ed8cff5a5db92a59dd90c22b04fa
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/05/2020
ms.locfileid: "3025960"
---
# <a name="product-collection-modules"></a>Ürün topluluğu modülleri


[!include [banner](includes/banner.md)]

Bu konu Microsoft Dynamics 365 Commerce'ta ürün koleksiyonu modülleriyle ilgili genel bir bakış sağlar.

## <a name="overview"></a>Genel Bakış

Ürün bulma, perakendecilerin müşterileri e-ticaret Web sitesinde kullanmak için kullandıkları birincil araçtır. Ürün koleksiyonu modülleri, perakende olarak hızlı bir şekilde yazmak için kullanılabilen sezgisel bir görsel arabirim sağlayarak, perakendecilere çekici alışveriş deneyimleri oluşturur.

Ürün koleksiyonu modülleri, Web sitesindeki fiziksel ürünleri ve hizmetleri temsil eder. Ürün koleksiyonu modülü genellikle müşterilerin bir ürün veya hizmet satın alabileceği Ayrıntılar sayfasıyla bağlantılıdır veya bu konuda bilgi edinebilirsiniz. 

Ürün koleksiyonları için kaynaklar şu dört tür listeler olabilir:

- Bir ürün veya ürün listesi ile ilgili ürünler olarak Dynamics 365 Commerce'de el ile tanımlanan ürünlerin düzenleme listeleri
- Yeni, en iyi satış veya trend ürünlerinin listesi gibi Algoritmik listeler
- Makine öğrenmeyi esas alan öneri listeleri
- Bir müşteri için kişiselleştirilmiş sonuçları destekleyen kişiselleştirme listeleri. Kişiselleştirilmiş sonuçları görmek için müşteriler e-ticaret sitesinde oturum açmış olmalıdır. Ziyaretçi kullanıcılar kişiselleştirilmiş sonuçları göremez. Müşteriler [hesap yönetimi sayfasından](account-management.md) kişiselleştirmeye geri çevirme yapabilir.

Aşağıdaki resimde bir e-ticaret sitesinde kullanılan farklı ürün koleksiyonları türleri gösterilmektedir.

![Bir e-ticaret sitesinde farklı türde ürün koleksiyonları örneği](./media/ProductCollectionsAcrossTheSiteUseProductPlacement.png)

> [!NOTE]
> Benzer türdeki bir ürün grubunu göstermek için her zaman ürün koleksiyonu modüllerini kullanın.

## <a name="product-collection-modules-and-types"></a>Ürün topluluğu modülleri ve türleri

Aşağıdaki tabloda, Dynamics 365 Commerce'de çeşitli türlerdeki ürün koleksiyonu modülleri açıklanmıştır.

| Ürün topluluğu modülü  | Türü | Tanım |
|----------------------------|------|-------------|
| Kategori                   | Kategori | Bu modül, bir kategorideki ürünlerin listesini gösterir ve bu satıcı kanalı için oluşturulan gezinti kategorisi hiyerarşisinde tanımlanır. |
| İlgili ürünler           | Düzenleme | Bu modülü, yazarın seçtiği ilişki türü için, ticaret yöneticisinin Commerce'de ilgili ürünler olarak konfigüre eden ürünlerin listesini gösterir. |
| Arama sonuçları             | Arama sorgusu | Bu tür bir ürün toplama modülü, müşterinin girdiği arama sorgusuyla en iyi şekilde eşleşen ürünlerin listesini gösterir. |
| Seçkin ürün listeleri      | Düzenleme | Bu modül, Commerce olarak tacirler ve düzenleyicilerin oluşturulduğu özel liste. |
| Yeni                        | Algoritmik | Bu modül, kanallara ve kataloglara önceden sıralanmış en yeni ürünlerin listesi. Site yazarı bu seçeneği seçerse, bu liste, oturum açmış bir kullanıcının kişiselleştirilmiş sonuçlarını gösterebilir. |
| En iyi satış               | Algoritmik | Bu modül, en yüksek sayıda satış ile derecelendirilen ürünlerin listesi. Site yazarı bu seçeneği seçerse, bu liste, oturum açmış bir kullanıcının kişiselleştirilmiş sonuçlarını gösterebilir. |
| Popüler                   | Algoritmik | Bu modül, belirli bir döneme ait en yüksek performanslı ürünlerin listesi. Site yazarı bu seçeneği seçerse, bu liste, oturum açmış bir kullanıcının kişiselleştirilmiş sonuçlarını gösterebilir. |
| Sıklıkla birlikte satın alınan | Yapay Zeka/Makine öğrenme | Bu modül, tüketici satın alma düzenlerini analiz etmek ve belirli bir ürünle birlikte satın alınan ilgili öğeleri önermek için makine öğrenmeyi kullanır. Site yazarı bu seçeneği seçerse, bu liste, oturum açmış bir kullanıcının kişiselleştirilmiş sonuçlarını gösterebilir. |
| Diğer sevilen ürünler           | Yapay Zeka/Makine öğrenme | Bu modül, tüketici satın alma düzenlerini analiz etmek ve belirli bir ürünle ilgili öğeleri önermek için makine öğrenmeyi kullanır. Site yazarı bu seçeneği seçerse, bu liste, oturum açmış bir kullanıcının kişiselleştirilmiş sonuçlarını gösterebilir. |
| Size özel çekmeler              | Yapay Zeka/Makine öğrenme | Bu modül, oturum açan kullanıcının satın alma düzenlerini analiz etmek ve bu satınalma desenlerine dayalı kişiselleştirilmiş öneriler sağlamak için makine öğrenmeyi kullanır. Konuk Kullanıcı için bu liste daraltılacak. |

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

| Türü                       | Tanım | Kullanım | Sayfa bağlamı | Belirli bağlam | Kişiselleştirme |
|----------------------------|-------------|-------|--------------|------------------|-----------------|
| Kategoriye göre ürünler       | Belirli bir kategoriye ait olan ürünlerin listesi. Bu kategori sayfa bağlamından veya yazarın sağladığı içerikten belirlenir. | Belirli bir ürün kategorisini yükseltmek için herhangi bir sayfada bu tür bir liste (örneğin, bir giriş sayfası, kategori sayfası, pazarlama sayfası veya ürün ayrıntıları sayfası \[PDP\]) kullanılabilir. | Sayfa içeriğindeki kategori (örneğin, kategori sayfası) | Yazar, liste bağlamı olarak belirli bir kategori sağlayabilir. | Uygulanamaz |
| İlgili ürünler           | İlişki türü için Commerce olarak ilgili ürünler olarak ticari bir yöneticinin konfigüre eden ürünlerin listesi. | Bu tür liste öncelikle PDP'ler üzerinde kullanılır, ancak bir ana ürün sağlandığında herhangi bir sayfada kullanılabilir. | Sayfadaki ürün, ilişki türü (zorunlu) | Ürün, seçicide seçilebilir ve ilişki türü kullanılır. | Uygulanamaz |
| Oluşturuldu                    | Commerce olarak tacirler ve düzenleyicilerin oluşturulduğu özel liste. | Zenginleştirme kategorisi sayfası, giriş sayfası, kullanıma alma ve sepet sayfaları ve ürün sayfaları | Uygulanamaz | Uygulanamaz | Uygulanamaz |
| Algoritmik                | <ul><li>**Yeni** – kanallara ve kataloglara önceden sıralanmış en yeni ürünlerin listesi.</li><li>**En çok satan** – en yüksek sayıda satış ile derecelendirilen ürünlerin listesi.</li><li>**Trend** – belirli bir döneme ait en yüksek performanslı ürünlerin listesi.</li></ul> | Giriş sayfası, zenginleştirme kategorisi sayfası, kullanıma alma ve sepet sayfaları | Sayfa içeriğindeki kategori (örneğin, kategori sayfası) | Site yazarı tarafından belirlenen kategori | Destekleniyor |
| Sıklıkla birlikte satın alınan | Bir liste, tüketici satın alma düzenlerini analiz etmek ve belirli bir ürünle birlikte satın alınan ilgili öğeleri önermek için makine öğrenmeyi kullanır. | Bu tip listeler yalnızca sepet sayfası için geçerlidir. | Alışveriş sepeti | Uygulanamaz | Destekleniyor |
| Diğer sevilen ürünler           | Bir liste, tüketici satın alma düzenlerini analiz etmek ve belirli bir ürünle ilgili öğeleri önermek için makine öğrenmeyi kullanır. | Bu tip listeler, PDP'ler üzerinde diğer müşterilerin satın aldığı ürünleri göstermek için kullanılır. | Sayfadan ürün bağlamı | Site yazarı tarafından sağlanan ürün | Destekleniyor |
| Size özel çekmeler              | Müşteri tercihlerini belirlemek için makine öğrenmeyi kullanan liste. | Bu tür listeler herhangi bir sayfada kullanılabilir. | Uygulanamaz| Uygulanamaz | Destekleniyor | 

## <a name="additional-resources"></a>Ek kaynaklar

[Başlangıç paketine genel bakış](starter-kit-overview.md)

[Döngü modülü](add-carousel.md)

[İçerik zengin blok modülü](add-content-rich-block.md)

[Konteyner modülü](add-container-module.md)

[Satınalma kutusu modülü](add-buy-box.md)

[Ürün önerilerine genel bakış](product-recommendations.md)
