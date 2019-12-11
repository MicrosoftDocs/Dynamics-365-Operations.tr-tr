---
title: Özellik modülü
description: Bu konu özellik modüllerini kapsamaktadır ve Microsoft Dynamics 365 Commerce'un site sayfalarına nasıl ekleneceğini açıklamaktadır.
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
ms.openlocfilehash: 76b59681d0bda11446f6db8b2685d1a0656f8f55
ms.sourcegitcommit: 3a4e137ef3a96ba0a58c5352f4a3b57467ace9ae
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/11/2019
ms.locfileid: "2785318"
---
# <a name="feature-module"></a>Özellik modülü 

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

Bu konu özellik modüllerini kapsamaktadır ve Microsoft Dynamics 365 Commerce'un site sayfalarına nasıl ekleneceğini açıklamaktadır.

## <a name="overview"></a>Genel Bakış

Özellik modülü, ürünleri veya promosyonları bir görüntü ve metin birleşimiyle pazarlamak için kullanılır. Örneğin, bir satıcı ürün ayrıntıları sayfasına, ürünün özelliklerini vurgulamak için özellik modülü ekleyebilir.

Özellik modülü içerik yönetimi sistemindeki (CMS) veriler tarafından yönlendiriliyor. Bunlar sayfadaki diğer modüllere bağımlı olmayan bağımsız modüllerdir. Bir özellik modülü, bir satıcıdan pazarlamak veya bir şeyi yükseltmek veya bir şeyin (örneğin, ürünler, Satışlar veya Özellikler) olmasını istediği herhangi bir site sayfasına yerleştirilebilir.

## <a name="examples-of-feature-modules-in-e-commerce"></a>E-ticarette özellik modülleri örnekleri

Bir özellik modülü aşağıdaki sayfalarda kullanılabilir:

- Ürün özelliklerini göstermek için ürün ayrıntıları sayfası
- Ürünleri yükseltmek için giriş sayfası
- Bir ürün kategorisini vurgulamak için kategori sayfası

## <a name="feature-module-properties"></a>Özellik modülü özellikleri

| Özellik adı     | Değerler | Tanım |
|-------------------|--------|-------------|
| Görüntü             | Resim dosyası | Bir görüntü, bir ürünü veya promosyonu pazarlamada kullanılabilir. Görüntü Galerisine bir resim yüklenebilir veya varolan bir görüntü kullanılabilir. |
| Başlık           | Başlık metni ve başlık etiketi (**H1**, **H2**, **H3**, **H4**, **H5** veya **H6**) | Tüm özellik modülü bir başlığa sahip olabilir. Varsayılan olarak, başlık için **H2** başlık etiketi kullanılır. Ancak, bu etiket erişilebilirlik gereksinimlerini karşılayacak şekilde değiştirilebilir. |
| Paragraf         | Paragraf metni | Özellik modülleri zengin metin biçimindeki paragraf metnini destekler. Kalın, altı çizili, italik metin ve köprüler gibi bazı temel zengin metin özellikleri desteklenir. Bu yeteneklerden bazıları, modüle uygulanan sayfa teması tarafından geçersiz kılınabilir. |
| Bağla              | Bağlantı metni, bağlantı URL'si, erişilebilir zengin internet uygulamaları (ARIA) etiketi ve **bağlantıyı yeni sekmede aç** | Özellik modülü bir veya daha fazla "eyleme çağrı" bağlantıları destekler. Bir bağlantı eklenirse, bağlantı metni, bir URL ve bir ARIA etiketi gereklidir. ARIA etiketleri erişilebilirlik gereksinimlerini karşılayacak şekilde açıklayıcı olmalıdır. Bağlantılar yeni bir sekmede açılacak şekilde konfigüre edilebilir. |
| Görüntü yerleştirme   | **Sağ**, **Sol**, **Üst** veya **Alt** | Bu özellik resmin metne göre konumunu tanımlar. Örneğin, **Sağ** seçilirse görüntü metnin sağında görüntülenir. |
| Görüntü sütunu boyutu | **1** ile **12** arasında bir değer | Bu özellik resmin metne göre boyutunu tanımlar. Boyut, sayfada bir dizi sütun olarak ifade edilir. Sayfada 12 sütun vardır. Varsayılan olarak resmin ve metnin boyutu aynı (her biri altı sütun) olacaktır. Ancak, boyut gerektiği gibi ayarlanabilir. |

## <a name="add-a-feature-module-to-a-new-page"></a>Yeni sayfaya özellik modülü ekleme 

Bir yeni sayfaya özellik modülü eklemek ve gerekli özellikleri ayarlamak için aşağıdaki adımları izleyin.

1. **Şablonlara** gidin ve **özellik şablonu** adlı bir sayfa şablonu oluşturun.
1. Varsayılan sayfanın **ana** yuvasına bir özellik modülü ekleyin.
1. Şablonu giriş yapın ve yayımlayın.
1. **Özellik sayfası** adlı bir sayfa oluşturmak için yeni oluşturduğunuz özellik şablonunu kullanın.
1. Varsayılan sayfada **ana** yuvayı seçin, üç nokta düğmesini (**...**) ve sonra **Modül ekle**'yi seçin.
1. **Modül Ekle** iletişim kutusunda **modüller'i seçin**, özellik modülünü seçin ve **Tamam**'ı seçin.
1. Soldaki anahat ağacında, özellik modülünü seçin.
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

[İçerik yerleşimi modülü](add-content-placement-modules.md)

[Hero modülü](add-hero-module.md)

[Video oynatıcı modülü](add-video-player.md)
