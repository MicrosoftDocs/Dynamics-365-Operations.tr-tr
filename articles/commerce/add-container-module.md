---
title: Konteyner modülü
description: Bu konu konteyner modüllerini kapsamaktadır ve Microsoft Dynamics 365 Commerce'un site sayfalarına nasıl ekleneceğini açıklamaktadır.
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
ms.openlocfilehash: 22a09b61fbe3bd1cca96011d3fb81a12ef1bc844
ms.sourcegitcommit: 295d940a345879b3dfc5991e387b91c7257019ea
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/01/2019
ms.locfileid: "2697072"
---
# <a name="container-module"></a>Konteyner modülü

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

Bu konu konteyner modüllerini kapsamaktadır ve Microsoft Dynamics 365 Commerce'un site sayfalarına nasıl ekleneceğini açıklamaktadır.

## <a name="overview"></a>Genel Bakış

Konteyner modülü, diğer modülleri barındıran bir modüldür. Bu, Dynamics 365 Commerce'de kullanılan en genel konteynerdir. Bir konteyner modülünün birincil amacı, kendisi için ayarlanan özellikler boyunca, içinde olan modüllerin düzenini tanımlamak amacıyla kullanılır. Örneğin, bu modüller iki sütunlu, üç sütunlu, dört sütunlu veya altı sütunlu düzende yan yana görüntülenebilir. Ayrıca, konteyner genişliği ile sınırlanabilirler veya ekranı doldurabilirler. Bir başlık, her konteyner modüle da eklenebilir.

Üç standart konteyner Modül türü vardır: konteyner, 2-yuvası olan konteyner ve 3-yuvası olan konteyner. Her türlü modül türünün modülleri bu konteynerlerin içine yerleştirilebilir. Ayrıca döngü, içerik zengin bloğu, içerik yerleşimi, sepet, ödeme, satın alma kutusu, başlık ve altbilgi gibi özel tür konteyner modülleri vardır. Bu konteynerlerin belirli amaçları vardır ve yalnızca belirli desteklenen modül türleri bunların içine yerleştirilebilir.

Modüllerin konteyner genişliğiyle sınırlanabilmesi için bunları bir konteyner içinde yerleştirmenizi öneririz.

## <a name="examples-of-container-modules-in-e-commerce"></a>E-ticarette konteyner modülleri örnekleri

- Site yazarı, yan yana üç modül görüntülendiği üç sütunlu bir düzen istiyor. Bu nedenle, site yazarı konteyner için 3-yuva türü bulunan bir konteyner modülü kullanır.
- Site yazarı, yan yana altı modül görüntülendiği altı sütunlu bir düzen istiyor. Bu nedenle, site yazarı, içinde altı sütun bulunan bir içerme türü konteyner kullanır.
- Site yazarı bir sayfaya modül koymak istiyor ancak ekranı doldurmasını istemiyorum. Bu nedenle, site yazarı modülü bir konteyner modüle ekler ve kapsayıcının **Genişlik** özelliğini **konteyner sığdır** şekilde ayarlar.

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
| Orta Görünüm bağlantı noktası konfigürasyonu  | **%25/%75**, **%75/%25**, **%50/%50**, **%67/%33**, **%33/%67** veya **%100** | Bu özellik, tabletler gibi orta Görünüm bağlantı noktaları için Düzen tanımlar. |
| Büyük Görünüm bağlantı noktası konfigürasyonu   | **%25/%75**, **%75/%25**, **%50/%50**, **%67/%33**, **%33/%67** veya **%100** | Bu özellik, bilgisayarlar gibi büyük Görünüm bağlantı noktaları için Düzen tanımlar. |

## <a name="container-with-3-slots"></a>3 alanlı kapsayıcı

3-yuvalı modül türü olan konteyner, üç sütunlu bir düzen için en iyi duruma getirilmiştir.

Farklı görünüm bağlantı noktalarının düzenini en iyi duruma getirmek için ek özellikler kullanılabilir. Her bir görünüm bağlantı noktası için, her bir sütunun genişliği tanımlanabilir. Aşağıdaki sütun genişliği ayarları kullanılabilir:

- **%33/%33/%33** – Üç modül da eşit sütun genişliğine sahiptir.
- **50%/25%/%25** - ilk modülde yüzde 50 sütun genişliği vardır ve geri kalan iki modülün sütun genişliği yüzde 25 ' tir. **%25/%50/%25** ve **%25/%25/%50** seçenekler de kullanılabilir.
- **16%/16%/%67** - ilk iki modülde yüzde 16 sütun genişliği vardır ve üçüncü modülün sütun genişliği yüzde 67 ' tir. **%16/%67/%16** ve **%67/%16/%16** seçenekler de kullanılabilir.

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

1. **Konteyner şablonu** adlı bir sayfa şablonu oluşturun.
1. Varsayılan sayfanın **ana** yuvasına bir konteyner modülü ekleyin.
1. Koteyner modülüne bir özellik modülü ekleyin.
1. Şablonu giriş yapın ve yayımlayın.
1. **Konteyner sayfası** adlı bir sayfa oluşturmak için yeni oluşturduğunuz konteyner şablonunu kullanın.
1. Yeni sayfanın **ana** yuvasına bir konteyner modülü ekleyin.
1. Konteyner modülüyle ilgili Özellik bölmesinde, **sütun sayısı** özelliğini **1**'e ve **Genişlik** özelliğini  **kapsayıcıya uyacak** şekilde ayarlayın.
1. Koteyner modülüne bir özellik modülü ekleyin.
1. Özellik modülünün Özellik bölmesinde bir başlık konfigüre edin.
1. Sayfayı kaydet ve önizleyin. Konteyner modülünün genişliğine uyan tek bir özellik modülü görmelisiniz.
1. Konteyner modülüyle ilgili özellik bölmesinde, **sütun sayısı** özelliğinin değerini **3** olarak değiştirin.
1. Koteyner modülüne iki veya daha fazla özellik modülü ekleyin.
1. Sayfayı kaydet ve önizleyin. Yan yana görünen üç özellik modülü şimdi görmelisiniz.
1. İstediğiniz düzeni elde ettikten sonra, sayfayı iade edin ve yayımlayın.

## <a name="additional-resources"></a>Ek kaynaklar

[Başlangıç paketine genel bakış](starter-kit-overview.md)

[Döngü modülü](add-carousel.md)

[İçerik zengin blok modülü](add-content-rich-block.md)

[İçerik yerleştirme modülü](add-content-placement-modules.md)

[Satın alma kutusu modülü](add-buy-box.md)

[Sepet modülü](add-cart-module.md)

[Ödeme modülü](add-checkout-module.md)

[Üst bilgi modülü](author-header-module.md)

[Alt bilgi modülü](author-footer-module.md)
