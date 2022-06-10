---
title: Konteyner modülü
description: Bu konu konteyner modüllerini kapsamaktadır ve Microsoft Dynamics 365 Commerce'un site sayfalarına nasıl ekleneceğini açıklamaktadır.
author: anupamar-ms
ms.date: 05/18/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: aa4bf7523acee06e91f0ebb983dd8777dec4bac5
ms.sourcegitcommit: ccb39767bd3430c24f4653c26560bba2cd66553c
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/19/2022
ms.locfileid: "8780726"
---
# <a name="container-module"></a>Konteyner modülü

[!include [banner](includes/banner.md)]

Bu konu konteyner modüllerini kapsamaktadır ve Microsoft Dynamics 365 Commerce'un site sayfalarına nasıl ekleneceğini açıklamaktadır.

Konteyner modülü, diğer modülleri barındıran bir modüldür. Bir konteyner modülünün birincil amacı, kendisi için ayarlanan özellikler boyunca, içinde olan modüllerin düzenini tanımlamak amacıyla kullanılır. Örneğin, bu modüller iki sütunlu, üç sütunlu, dört sütunlu veya altı sütunlu düzende yan yana görüntülenebilir. Ayrıca, konteyner genişliği ile sınırlanabilirler veya ekranı doldurabilirler. Bir başlık, her konteyner modüle da eklenebilir.

Üç konteyner modülü desteklenir: konteyner, 2 yuvalı konteyner ve 3 yuvalı konteyner. Her türlü modül türünün bu konteynerlerin içine yerleştirilebilir. 

> [!NOTE] 
> Her zaman modüllerin konteyner genişliğiyle sınırlanabilmesi için bunları bir konteyner modülünün içinde yerleştirmenizi öneririz.

## <a name="examples-of-container-modules-in-e-commerce"></a>E-ticarette konteyner modülleri örnekleri

- Site yazarı, yan yana üç modül görüntülendiği üç sütunlu bir düzen istiyor. Bu nedenle, site yazarı konteyner için 3-yuva türü bulunan bir konteyner modülü kullanır.
- Site yazarı, yan yana altı modül görüntülendiği altı sütunlu bir düzen istiyor. Bu nedenle, site yazarı, içinde altı sütun bulunan bir içerme türü konteyner kullanır.
- Site yazarı bir sayfaya modül koymak istiyor ancak ekranı doldurmasını istemiyorum. Bu nedenle, site yazarı modülü bir konteyner modüle ekler ve kapsayıcının **Genişlik** özelliğini **konteyner sığdır** şekilde ayarlar.

Aşağıdaki resimde, ticaret sitesi oluşturucuda döngü modülü içeren bir kapsayıcı modülü örneği gösterilmektedir. Bu örnekte, konteyner modülünün **genişlik** özelliği **Ekranı doldur** ayarlanır.

![Konteyner modülü örneği.](./media/ecommerce-container.PNG)

## <a name="container-module-properties"></a>Konteyner modülü özellikler

| Özellik adı     | Değerler | Tanım |
|-------------------|--------|-------------|
| Başlık           | Başlık metni ve başlık etiketi (**H1**, **H2**, **H3**, **H4**, **H5** veya **H6**) | Konteyner için isteğe bağlı bir başlık sağlanabilir. Varsayılan olarak, başlık için **H2** başlık etiketi kullanılır. Ancak, bu etiket erişilebilirlik gereksinimlerini karşılayacak şekilde değiştirilebilir. |
| Genişlik             | **Kapsayıcıya sığdır** veya **Ekrana doldur** | Değer **konteynere sığdır** (varsayılan değer) şekilde ayarlandıysa, konteyner içindeki öğeler konteyner genişliğiyle sınırlandırılır. Değer, **ekranı doldur**'a ayarlanmışsa, modüller konteyner genişliğiyle sınırlandırılmaz ancak ekranı doldurabilir. |
| Sütun sayısı | **1**, **2**, **3**, **4**, **6** veya **12** | Bu özellik konteynerdeki sütun sayısını tanımlar. Bir konteynerin en çok 12 sütunu olabilir. |

## <a name="container-with-2-slots"></a>2 alanlı kapsayıcı

2-yuva türü olan konteyner, iki sütunlu bir düzen için en iyi duruma getirilmiştir. Bu konteyner türünde, içinde modüllerin yan yana görünümüne izin veren iki yuva vardır.

Farklı görünüm bağlantı noktaları (mobil cihazlar, tabletler, bilgisayarlar, vb.) için düzeni en iyi duruma getirmek amacıyla ek özellikler kullanılabilir. Her bir görünüm bağlantı noktası için, her bir sütunun genişliği tanımlanabilir. Aşağıdaki sütun genişliği ayarları kullanılabilir:

- **%75/%25** - ilk modülde yüzde 75 sütun genişliği vardır ve ikinci modülün sütun genişliği yüzde 25'tir. **%25/%75** seçeneği de kullanılabilir.
- **%50/%50** – her iki modül da eşit sütun genişliğine sahiptir.
- **%67/%33** - ilk modülde yüzde 67 sütun genişliği vardır ve ikinci modülün sütun genişliği yüzde 33'tir. **%33/%67** seçeneği de kullanılabilir.
- **%100** – her iki modül da tam sütun genişliğine sahiptir. Bu nedenle, modüller tek bir sütunda dikey olarak yığılır. Bu tek sütunlu düzen konteyner amacına (2-yuva türü) sahip olmakla birlikte, bazı Görünüm bağlantı noktaları (örneğin, mobil aygıtlar gibi ek küçük Görünüm bağlantı noktaları) için tercih edilebilir.

### <a name="container-with-2-slots-properties"></a>2-yuva özelliklerine sahip konteyner

| Özellik adı                   | Değerler | Tanım |
|---------------------------------|--------|-------------|
| Başlık                         | Başlık metni ve başlık etiketi | Konteyner için isteğe bağlı sağlanabilir. |
| X-küçük Görünüm bağlantı noktası konfigürasyonu | **%25/%75**, **%75/%25**, **%50/%50**, **%67/%33**, **%33/%67** veya **%100** | Bu özellik, ek küçük Görünüm bağlantı noktaları için Düzen tanımlar. |
| Küçük Görünüm bağlantı noktası konfigürasyonu   | **%25/%75**, **%75/%25**, **%50/%50**, **%67/%33**, **%33/%67** veya **%100** | Bu özellik, mobil cihazlar gibi küçük Görünüm bağlantı noktaları için Düzen tanımlar. |
| Orta Görünüm bağlantı noktası konfigürasyonu  | **25%/75%**, **75%/25%**, **50%/50%**, **67%/33%**, **33%/67%** veya **100%** | Bu özellik, tabletler gibi orta Görünüm bağlantı noktaları için Düzen tanımlar. |
| Büyük Görünüm bağlantı noktası konfigürasyonu   | **25%/75%**, **75%/25%**, **50%/50%**, **67%/33%**, **33%/67%** veya **100%** | Bu özellik, bilgisayarlar gibi büyük Görünüm bağlantı noktaları için Düzen tanımlar. |

## <a name="container-with-3-slots"></a>3 alanlı kapsayıcı

3-yuvalı modül türü olan konteyner, üç sütunlu bir düzen için en iyi duruma getirilmiştir.

Farklı görünüm bağlantı noktalarının düzenini en iyi duruma getirmek için ek özellikler kullanılabilir. Her bir görünüm bağlantı noktası için, her bir sütunun genişliği tanımlanabilir. Aşağıdaki sütun genişliği ayarları kullanılabilir:

- **33%/33%/33%** - Üç modül da eşit sütun genişliğine sahiptir.
- **50%/25%/25%** – ilk modülde yüzde 50 sütun genişliği vardır ve geri kalan iki modülün sütun genişliği yüzde 25'tir. **25%/50%/25%** ve **25%/25%/50%** seçenekler de kullanılabilir.
- **16%/16%/67%** – İlk iki modülde yüzde 16 sütun genişliği vardır ve üçüncü modülün sütun genişliği yüzde 67'dir. **16%/67%/16%** ve **67%/16%/16%** seçenekler de kullanılabilir.

### <a name="container-with-3-slots-properties"></a>3-yuva özelliklerine sahip konteyner

| Özellik adı                   | Değerler | Tanım |
|---------------------------------|--------|-------------|
| Başlık                         | Başlık metni ve başlık etiketi | Konteynere isteğe bağlı bir başlık eklenebilir. |
| X-küçük Görünüm bağlantı noktası konfigürasyonu | **33%/33%/33%**, **50%/25%/25%**, **25%/50%/25%**, **25%/25%/50%**, **16%/16%/67%**, **16%/67%/16%** veya **67%/16%/16%** | Bu özellik, ek küçük Görünüm bağlantı noktaları için Düzen tanımlar. |
| Küçük Görünüm bağlantı noktası konfigürasyonu   | **33%/33%/33%**, **50%/25%/25%**, **25%/50%/25%**, **25%/25%/50%**, **16%/16%/67%**, **16%/67%/16%** veya **67%/16%/16%** | Bu özellik, mobil cihazlar gibi küçük Görünüm bağlantı noktaları için Düzen tanımlar. |
| Orta Görünüm bağlantı noktası konfigürasyonu  | **33%/33%/33%**, **50%/25%/25%**, **25%/50%/25%**, **25%/25%/50%**, **16%/16%/67%**, **16%/67%/16%** veya **67%/16%/16%** | Bu özellik, tabletler gibi orta Görünüm bağlantı noktaları için Düzen tanımlar. |
| Büyük Görünüm bağlantı noktası konfigürasyonu   | **33%/33%/33%**, **50%/25%/25%**, **25%/50%/25%**, **25%/25%/50%**, **16%/16%/67%**, **16%/67%/16%** veya **67%/16%/16%** | Bu özellik, bilgisayarlar gibi büyük Görünüm bağlantı noktaları için Düzen tanımlar. |

## <a name="add-a-container-module-to-a-page"></a>Sayfaya konteyner modülü ekleme

Bir yeni sayfaya konteyner oynatma modülü eklemek ve gerekli özellikleri ayarlamak için aşağıdaki adımları izleyin.

1. Bir yeni şablonu oluşturmak için **Şablonlar**'a gidin ve **Yeni**'yi seçin.
1. **Yeni şablon** iletişim kutusunda **Şablon adı** altında, **Konteyner şablonu**'nu girin ve **Tamam**'ı seçin.
1. **Gövde** alanında, üç nokta (**...**) düğmesini seçin ve **Modül ekle**'yi seçin.
1. **Modülleri seç** iletişim kutusunda **Varsayılan Sayfa** modülünü seçin ve **Tamam**'ı seçin.
1. **Kaydet**'i seçin, şablonu iade etmek için **Düzenlemeyi bitir**'i ve ardından yayımlamak için **Yayımla**'yı seçin. 
1. **Sayfalar**'a gidin ve yeni sayfa oluşturmak için **Yeni**'yi seçin.
1. **Yeni sayfa oluştur** iletişim kutusunda **Sayfa adı** altında, **Konteyner sayfası**'nı girin ve **Tamam**'ı seçin.
1. **Şablon seç** bölümünde, oluşturduğunuz **Konteyner şablonunu** seçin ve sonra **İleri**'yi seçin.
1. **Bir düzen seçin** bölümünde, bir sayfa düzeni seçin (ör. **Esnek düzen**) ve sonra **İleri**'yi seçin.
1. **İnceleyin ve bitirin** bölümünde, sayfa yapılandırmasını gözden geçirin. Sayfa bilgilerini düzenlemeniz gerekiyorsa, **Geri**'yi seçin. Sayfa bilgileri doğruysa, **Sayfa oluştur**'u seçin. 
1. Yeni sayfanın **Ana** alanında, üç nokta düğmesini (**...**) ve sonra **Modül ekle**'yi seçin.
1. **Modül seç** iletişim kutusunda **Konteyner** modülünü seçin ve **Tamam**'ı seçin.
1. Konteyner modülüyle ilgili Özellik bölmesinde, **sütun sayısı** özelliğini **1**'e ve **Genişlik** özelliğini **Kapsayıcıyı doldur** şekilde ayarlayın.
1. **Konteyner** alanında, üç nokta (**...**) düğmesini seçin ve **Modül ekle**'yi seçin.
1. **Modülleri seç** iletişim kutusunda **İçerik bloğu** modülünü seçin ve **Tamam**'ı seçin.
1. İçerik bloğu modülü özellik bölmesinde başlığı, görüntüyü ve düzeni yapılandırın.
1. **Kaydet**'i seçin ve ardından sayfayı önizlemek için **Önizleme**'yi seçin. Konteyner modülünün genişliğine uyan tek bir özellik modülü görmelisiniz.
1. Konteyner modülüyle ilgili özellik bölmesinde, **sütun sayısı** özelliğinin değerini **3** olarak değiştirin.
1. Konteyner modülüne iki tane daha içerik bloğu modülü ekleyin ve konfigüre edin.
1. **Kaydet**'i seçin ve ardından sayfayı önizlemek için **Önizleme**'yi seçin. Yan yana görünen üç içerik bloku modülü şimdi görmelisiniz.
1. İstediğiniz düzeni elde ettikten sonra, sayfayı iade etmek için **düzenlemeyi bitir** 'i seçin ve yayınlamak için **Yayınla** 'yı seçin.

## <a name="additional-resources"></a>Ek kaynaklar

[Modül kitaplığına genel bakış](starter-kit-overview.md)

[Akordeon modülü](add-accordion.md)

[Sekme modülü](add-tab.md)

[Döngü modülü](add-carousel.md)

[Metin bloğu modülü](add-content-rich-block.md)

[Satınalma kutusu modülü](add-buy-box.md)

[Sepet modülü](add-cart-module.md)

[Ödeme modülü](add-checkout-module.md)

[Üst bilgi modülü](author-header-module.md)

[Alt bilgi modülü](author-footer-module.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
