---
title: Hero modülü
description: Bu konu hero modüllerini kapsamaktadır ve Microsoft Dynamics 365 Commerce'un site sayfalarına nasıl ekleneceğini açıklamaktadır.
author: anupamar-ms
manager: annbe
ms.date: 10/31/2019
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
ms.openlocfilehash: c43704992e9759e7207f1b1c9bc958449daa6d1d
ms.sourcegitcommit: 3a4e137ef3a96ba0a58c5352f4a3b57467ace9ae
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/11/2019
ms.locfileid: "2785410"
---
# <a name="hero-module"></a>Hero modülü

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

Bu konu hero modüllerini kapsamaktadır ve Microsoft Dynamics 365 Commerce'un site sayfalarına nasıl ekleneceğini açıklamaktadır.

## <a name="overview"></a>Genel Bakış

Hero modülü, ürünleri veya promosyonları bir görüntü ve metin birleşimiyle pazarlamak için kullanılır. Örneğin, bir satıcı yeni bir ürünü yükseltmek ve müşterilerin dikkatini çekmek için bir e-ticaret sitesinin giriş sayfasına Hero modülü ekleyebilir.

Hero modülü içerik yönetimi sistemindeki (CMS) veriler tarafından yönlendiriliyor. Bunlar sayfadaki diğer modüllere bağımlı olmayan bağımsız modüllerdir. Bir Hero modülü, bir satıcıdan pazarlamak veya bir şeyi yükseltmek veya bir şeyin (örneğin, ürünler, Satışlar veya Özellikler) olmasını istediği herhangi bir site sayfasına yerleştirilebilir.

## <a name="examples-of-hero-module-in-e-commerce"></a>E-ticarette Hero modülleri örnekleri

- Bir Hero modülü, promosyonlar ve yeni ürünleri vurgulamak için e-ticaret sitesinin giriş sayfasında kullanılabilir.
- Hero modülü ürün bilgilerini sergilebilecek bir ürün ayrıntıları sayfasında kullanılabilir.
- Çoklu ürünleri veya promosyonları vurgulamak için bir döngü modülü birden fazla Hero modül içinde yer alabilir.

## <a name="hero-module-properties"></a>Hero modülü özellikleri

| Özellik adı  | Değerler | Tanım |
|----------------|--------|-------------|
| Görüntü          | Resim dosyası | Bir görüntü, bir ürünü veya promosyonu sergilemede kullanılabilir. Görüntü Galerisine bir resim yüklenebilir veya varolan bir görüntü kullanılabilir. |
| Başlık        | Başlık metni ve başlık etiketi (**H1**, **H2**, **H3**, **H4**, **H5** veya **H6**) | Tüm Hero modülü bir başlığa sahip olabilir. Varsayılan olarak, başlık için **H2** başlık etiketi kullanılır. Ancak, bu etiket erişilebilirlik gereksinimlerini karşılayacak şekilde değiştirilebilir. |
| Paragraf      | Paragraf metni | Hero modülleri zengin metin biçimindeki paragraf metnini destekler. Kalın, altı çizili, italik metin ve köprüler gibi bazı temel zengin metin özellikleri desteklenir. Bu yeteneklerden bazıları, modüle uygulanan sayfa teması tarafından geçersiz kılınabilir. |
| Bağla           | Bağlantı metni, bağlantı URL'si, erişilebilir zengin internet uygulamaları (ARIA) etiketi ve **bağlantıyı yeni sekmede aç** | Hero modülü bir veya daha fazla "eyleme çağrı" bağlantıları destekler. Bir bağlantı eklenirse, bağlantı metni, bir URL ve bir ARIA etiketi gereklidir. ARIA etiketleri erişilebilirlik gereksinimlerini karşılayacak şekilde açıklayıcı olmalıdır. Bağlantılar yeni bir sekmede açılacak şekilde konfigüre edilebilir. |
| Metin yerleştirme | **Üst sola**, **üst sağa**, **üst orta**, **alt sola**, **alt sağa**, **alt orta**, **orta sola**, **Merkez sağa** veya **Merkez Merkezi** | Bu özellik resmin metne göre konumunu tanımlar. Örneğin, **Sağ** seçilirse görüntü metnin sağında görüntülenir. |
| Metin teması     | **Açık** veya **Koyu** | Arka plan resmine dayalı olarak metin için bir renk düzeni tanımlanabilir. Örneğin, görüntüde koyu renkli bir arka plan varsa, metin görünür hale getirmek ve erişilebilirlik amacıyla renk karşıtlığı oranlarını karşılamak için açık bir tema uygulanabilir. |
| Gradyan       | **Doğru** veya **yanlış** | Bir gradyan, erişilebilirlik amacıyla renk karşıtlığı oranlarını karşılamak üzere görüntüye uygulanabilir. |

## <a name="add-a-hero-module-to-a-new-page"></a>Yeni sayfaya Hero modülü ekleme

Bir yeni sayfaya Hero modülü eklemek ve gerekli özellikleri ayarlamak için aşağıdaki adımları izleyin.

1. **Şablonlara** gidin ve **Hero şablonu** adlı bir sayfa şablonu oluşturun.
1. Varsayılan sayfanın **ana** yuvasına bir Hero modülü ekleyin.
1. Şablonu giriş yapın ve yayımlayın.
1. **Hero sayfası** adlı bir sayfa oluşturmak için yeni oluşturduğunuz hero şablonunu kullanın.
1. Varsayılan sayfada **ana** yuvayı seçin, üç nokta düğmesini (**...**) ve sonra **Modül ekle**'yi seçin.
1. **Modül Ekle** iletişim kutusunda **modüller'i seçin**, Hero modülünü seçin ve **Tamam**'ı seçin.
1. Soldaki anahat ağacında, Hero modülünü seçin.
1. Sağdaki özellikler bölmesinde, **Resim Ekle**'yi seçin. Sonra da varolan bir görüntüyü seçin veya yeni bir görüntü yükleyin.
1. **Başlık** öğesini seçin.
1. **Başlık** iletişim kutusunda başlık metnini ekleyin, başlık düzeyini seçin ve **Tamam**'ı seçin.
1. **Zengin metin**altında, istediğiniz metni ekleyin.
1. **Eylem bağlantısı ekle**'yi seçin.
1. **Eylem bağlantısı** iletişim kutusunda bağlantı metni, bağlantı URL 'si ve bağlantı için bir Aria etiketi ekleyin ve **Tamam**'ı seçin.
1. Sayfayı kaydedin ve değişikliklerinizi önizleyin.
1. Sayfayı giriş yapın ve yayımlayın.

## <a name="additional-resources"></a>Ek kaynaklar

[Başlangıç paketine genel bakış](starter-kit-overview.md)

[Uyarı modülü](add-alert.md)

[Döngü modülü](add-carousel.md)

[İçerik zengin blok modülü](add-content-rich-block.md)

[İçerik yerleştirme modülü](add-content-placement-modules.md)

[Özellik modülü](add-feature-module.md)

[Video oynatıcı modülü](add-video-player.md)
