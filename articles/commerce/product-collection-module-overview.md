---
title: Ürün topluluğu modülleri
description: Bu makale Microsoft Dynamics 365 Commerce'ta ürün koleksiyonu modülleriyle ilgili genel bir bakış sağlar.
author: v-chgri
ms.date: 05/18/2022
ms.topic: overview
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: asharchw
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.assetid: ''
ms.openlocfilehash: 2ad50011e2f4c037a75c8c4b195c728bb58c3b47
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/12/2022
ms.locfileid: "9269875"
---
# <a name="product-collection-modules"></a>Ürün topluluğu modülleri

[!include [banner](includes/banner.md)]

Bu makale Microsoft Dynamics 365 Commerce'ta ürün koleksiyonu modülleriyle ilgili genel bir bakış sağlar.

Ürün bulma, perakendecilerin müşterileri e-ticaret Web sitesinde kullanmak için kullandıkları birincil araçtır. Ürün koleksiyonu modülleri, perakende olarak hızlı bir şekilde yazmak için kullanılabilen sezgisel bir görsel arabirim sağlayarak, perakendecilere çekici alışveriş deneyimleri oluşturur.

Ürün koleksiyonu modülleri, Web sitesindeki fiziksel ürünleri ve hizmetleri temsil eder. Ürün koleksiyonu modülü genellikle müşterilerin bir ürün veya hizmet satın alabileceği Ayrıntılar sayfasıyla bağlantılıdır veya bu konuda bilgi edinebilirsiniz. 

Ürün koleksiyonları için kaynaklar şu dört tür listeler olabilir:

- Bir ürün veya ürün listesi ile ilgili ürünler olarak Dynamics 365 Commerce'de el ile tanımlanan ürünlerin düzenleme listeleri
- Yeni, en iyi satış veya trend ürünlerinin listesi gibi Algoritmik listeler
- Makine öğrenmeyi esas alan öneri listeleri
- Bir müşteri için kişiselleştirilmiş sonuçları destekleyen kişiselleştirme listeleri. Kişiselleştirilmiş sonuçları görmek için müşteriler e-ticaret sitesinde oturum açmış olmalıdır. Ziyaretçi kullanıcılar kişiselleştirilmiş sonuçları göremez. Müşteriler [hesap yönetimi sayfasından](account-management.md) kişiselleştirmeye geri çevirme yapabilir.

Aşağıdaki resimde bir e-ticaret sitesinde kullanılan farklı ürün koleksiyonları türleri gösterilmektedir.

![Bir e-ticaret sitesinde farklı türde ürün koleksiyonları örneği.](./media/ProductCollectionsAcrossTheSiteUseProductPlacement.png)

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

## <a name="supported-modules"></a>Desteklenen modüller 

Ürün koleksiyonu modülü, kullanıcıların ürün bilgilerini görüntülemesine ve bir ürün koleksiyonu sayfasından alışveriş sepetine ürün eklemesine olanak veren [hızlı görüntüleme modülünü](quick-view-module.md) destekler.

## <a name="add-a-product-collection-module-to-a-category-page"></a>Kategori sayfasına ürün koleksiyonu modülü ekleme

Kategori sayfasına ürün koleksiyonu modülü eklemek için bu adımları izleyin.

1. **Sayfalar**'a gidin ve yeni sayfa oluşturmak için **Yeni**'yi seçin.
1. **Yeni sayfa oluştur** iletişim kutusundaki **Sayfa adı** altında, uygun bir sayfa adı girin ve ardından **İleri**'yi seçin.
1. **Şablon seç** bölümünde, varsayılan kategori sayfanız tarafından kullanılan şablonu seçin ve ardından **İleri**'yi seçin.
1. **Bir düzen seçin** bölümünde, bir sayfa düzeni seçin (ör. **Esnek düzen**) ve sonra **İleri**'yi seçin.
1. **İnceleyin ve bitirin** bölümünde, sayfa yapılandırmasını gözden geçirin. Sayfa bilgilerini düzenlemeniz gerekiyorsa, **Geri**'yi seçin. Sayfa bilgileri doğruysa, **Sayfa oluştur**'u seçin. 
1. **Alt alt bilgi** alanında, üç nokta (**...**) düğmesini seçin ve **Modül ekle**'yi seçin.
1. **Modül seç** iletişim kutusunda **Konteyner** modülünü seçin ve **Tamam**'ı seçin.
1. **Konteyner** alanında, üç nokta (**...**) düğmesini seçin ve **Modül ekle**'yi seçin.
1. **Modülleri seç** iletişim kutusunda, **Ürün koleksiyonu** modülünü seçin ve **Tamam**'ı seçin.  
1. Ürün koleksiyonu modülüyle ilgili Özellikler bölmesinde, **Ürün listesi ekle**'yi seçin.
1. **Ürün listesi yapılandırması seç** iletişim kutusunda liste türünü seçin, liste kaynağını seçin ve madde sayısını girin. Liste türü için kullanılabilen diğer seçenekleri yapılandırın. Liste türleri hakkında daha fazla bilgi için, aşağıdaki tabloya bakın. 
1. **Tamam**'ı seçin.
1. **Kaydet**'i seçin ve ardından sayfayı önizlemek için **Önizleme**'yi seçin.
1. Sayfayı iade etmek için **Düzenlemeyi bitir**'i seçin, ardından yayımlamak için **Yayımla**'yı seçin.

Aşağıdaki tabloda, **Ürün listesi konfigürasyonu seç** iletişim kutusunda seçim için kullanılabilen liste türleri gösterilmiştir.

| Türü                       | Tanım | Kullanım | Sayfa bağlamı | Belirli bağlam | Kişiselleştirme |
|----------------------------|-------------|-------|--------------|------------------|-----------------|
| Kategoriye göre ürünler       | Belirli bir kategoriye ait olan ürünlerin listesi. Bu kategori sayfa bağlamından veya yazarın sağladığı içerikten belirlenir. | Belirli bir ürün kategorisini yükseltmek için herhangi bir sayfada bu tür bir liste (örneğin, bir giriş sayfası, kategori sayfası, pazarlama sayfası veya ürün ayrıntıları sayfası \[PDP\]) kullanılabilir. | Sayfa içeriğindeki kategori (örneğin, kategori sayfası) | Yazar, liste bağlamı olarak belirli bir kategori sağlayabilir. | Uygulanamaz |
| İlgili ürünler           | İlişki türü için Commerce olarak ilgili ürünler olarak ticari bir yöneticinin konfigüre eden ürünlerin listesi. | Bu tür liste öncelikle PDP'ler üzerinde kullanılır, ancak bir ana ürün sağlandığında herhangi bir sayfada kullanılabilir. | Sayfadaki ürün, ilişki türü (zorunlu) | Ürün, seçicide seçilebilir ve ilişki türü kullanılır. | Uygulanamaz |
| Oluşturuldu                    | Commerce olarak tacirler ve düzenleyicilerin oluşturulduğu özel liste. | Zenginleştirme kategorisi sayfası, giriş sayfası, kullanıma alma ve sepet sayfaları ve ürün sayfaları | Uygulanamaz | Uygulanamaz | Uygulanamaz |
| Algoritmik                | <ul><li>**Yeni** – kanallara ve kataloglara önceden sıralanmış en yeni ürünlerin listesi.</li><li>**En çok satan** – en yüksek sayıda satış ile derecelendirilen ürünlerin listesi.</li><li>**Trend** – belirli bir döneme ait en yüksek performanslı ürünlerin listesi.</li></ul> | Giriş sayfası, zenginleştirme kategorisi sayfası, kullanıma alma ve sepet sayfaları | Sayfa içeriğindeki kategori (örneğin, kategori sayfası) | Site yazarı tarafından belirlenen kategori | Destekleniyor |
| Sıklıkla birlikte satın alınan | Bir liste, tüketici satın alma düzenlerini analiz etmek ve belirli bir ürünle birlikte satın alınan ilgili öğeleri önermek için makine öğrenmeyi kullanır. | Bu tip listeler yalnızca sepet sayfası için geçerlidir. | Alışveriş sepeti | Uygulanamaz | Destekleniyor |
| Diğer sevilen ürünler           | Bir liste, tüketici satın alma düzenlerini analiz etmek ve belirli bir ürünle ilgili öğeleri önermek için makine öğrenmeyi kullanır. | Bu tip listeler, PDP'ler üzerinde diğer müşterilerin satın aldığı ürünleri göstermek için kullanılır. | Sayfadan ürün bağlamı | Site yazarı tarafından sağlanan ürün | Destekleniyor |
| Size özel çekmeler              | Müşteri tercihlerini belirlemek için makine öğrenmeyi kullanan liste. | Bu tür listeler herhangi bir sayfada kullanılabilir. | Geçerli değil| Geçerli değil | Destekleniyor | 

## <a name="additional-resources"></a>Ek kaynaklar

[Modül kitaplığına genel bakış](starter-kit-overview.md)

[Döngü modülü](add-carousel.md)

[İçerik zengin blok modülü](add-content-rich-block.md)

[Kapsayıcı modülü](add-container-module.md)

[Satın alma kutusu modülü](add-buy-box.md)

[Ürün önerilerine genel bakış](product-recommendations.md)

[Hızlı görüntüleme modülü](quick-view-module.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
