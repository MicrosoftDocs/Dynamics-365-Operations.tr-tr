---
title: İçerik blok modülü
description: Bu konu içerik blok modüllerini kapsamaktadır ve Microsoft Dynamics 365 Commerce'un site sayfalarına nasıl ekleneceğini açıklamaktadır.
author: anupamar-ms
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
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: a6359c915d053bb00c969b166325f675c0003ead
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/15/2021
ms.locfileid: "4980369"
---
# <a name="content-block-module"></a>İçerik blok modülü


[!include [banner](includes/banner.md)]

Bu konu içerik blok modüllerini kapsamaktadır ve Microsoft Dynamics 365 Commerce'un site sayfalarına nasıl ekleneceğini açıklamaktadır.

## <a name="overview"></a>Genel Bakış

Bir içerik bloku modülü, ürünleri veya promosyonları bir görüntü ve metin birleşimiyle pazarlamak için kullanılır. Örneğin, bir satıcı yeni bir ürünü yükseltmek ve müşterilerin dikkatini çekmek için bir e-ticaret sitesinin giriş sayfasına içerik bloku modülü ekleyebilir.

İçerik bloku modülü içerik yönetimi sistemindeki (CMS) veriler tarafından yönlendiriliyor. Bunlar sayfadaki diğer modüllere bağımlı olmayan bağımsız modüllerdir. Bir içerik bloku modülü, bir satıcıdan pazarlamak veya bir şeyi yükseltmek veya bir şeyin (örneğin, ürünler, Satışlar veya Özellikler) olmasını istediği herhangi bir site sayfasına yerleştirilebilir.

## <a name="examples-of-content-block-module-in-e-commerce"></a>E-ticarette içerik bloku modülü örnekleri

- Bir içerik bloku modülü, promosyonlar ve yeni ürünleri vurgulamak için e-ticaret sitesinin giriş sayfasında kullanılabilir.
- Bir içerik bloku modülü ürün bilgilerini sergilebilecek bir ürün ayrıntıları sayfasında kullanılabilir.
- Çoklu ürünleri veya promosyonları vurgulamak için bir döngü modülü birden fazla içerik bloku modül içinde yer alabilir.

## <a name="content-block-modules-and-themes"></a>İçerik bloğu modülleri ve temaları

İçerik bloğu modülleri, bir temaya dayalı olarak çeşitli düzen ve stilleri destekleyebilir. Örneğin, Fabrikam teması bir içerik bloğu modülünün üç düzen çeşitlemelerini destekler: Hero, özellik ve döşeme. Hero düzeni arka planda metin kaplaması olan bir resim gösterir. Özellik mizanpajı bir resmi ve bir metni yan yana gösterir. Kutucuk düzeni, kutucuk biçiminde birden çok içerik bloklarına izin verir.

Ek olarak, tema her düzen için farklı özellikler sergileyebilir. Bir tema geliştiricisi, içerik bloğu modülünü kullanarak daha fazla stil ile daha fazla düzen oluşturabilir.

Aşağıdaki resimde, Hero düzenine sahip bir içerik bloğu modülü örneği gösterilmektedir.

![Hero modülü örneği](./media/Hero.PNG)

Aşağıdaki resimde, özellik düzenine sahip bir içerik bloğu modülü örneği gösterilmektedir.

![Özellik modülleri örnekleri](./media/Feature.PNG)

## <a name="content-block-module-properties"></a>İçerik blok modülü özellikleri

| Özellik adı  | Değerler | Tanım |
|----------------|--------|-------------|
| Görüntü          | Resim dosyası | Bir görüntü, bir ürünü veya promosyonu sergilemede kullanılabilir. Görüntü Galerisine bir resim yüklenebilir veya varolan bir görüntü kullanılabilir. |
| Başlık        | Başlık metni ve başlık etiketi (**H1**, **H2**, **H3**, **H4**, **H5** veya **H6**) | Tüm Hero modülü bir başlığa sahip olabilir. Varsayılan olarak, başlık için **H2** başlık etiketi kullanılır. Ancak, bu etiket erişilebilirlik gereksinimlerini karşılayacak şekilde değiştirilebilir. |
| Paragraf      | Paragraf metni | Hero modülleri zengin metin biçimindeki paragraf metnini destekler. Kalın, altı çizili, italik metin ve köprüler gibi bazı temel zengin metin özellikleri desteklenir. Bu yeteneklerden bazıları, modüle uygulanan sayfa teması tarafından geçersiz kılınabilir. |
| Bağla           | Bağlantı metni, bağlantı URL'si, erişilebilir zengin internet uygulamaları (ARIA) etiketi ve **bağlantıyı yeni sekmede aç** | Hero modülü bir veya daha fazla "eyleme çağrı" bağlantıları destekler. Bir bağlantı eklenirse, bağlantı metni, bir URL ve bir ARIA etiketi gereklidir. ARIA etiketleri erişilebilirlik gereksinimlerini karşılayacak şekilde açıklayıcı olmalıdır. Bağlantılar yeni bir sekmede açılacak şekilde konfigüre edilebilir. |

## <a name="content-block-module-properties-exposed-by-the-fabrikam-theme"></a>Fabrikam teması tarafından gösterilen içerik bloğu modülü özellikleri 

| Özellik adı  | Değerler | Tanım |
|----------------|--------|-------------|
| Metin yerleştirme | **Sol**, **Sağ**, **Orta** | Bu özellik, resmin üzerinde metnin konumunu belirler. Yalnızca hero düzenine uygulanır. |
| Metin teması     | **Açık** veya **Koyu** | Arka plan resmine dayalı olarak metin için bir renk düzeni tanımlanabilir. Örneğin, görüntüde koyu renkli bir arka plan varsa, metin görünür hale getirmek ve erişilebilirlik amacıyla renk karşıtlığı oranlarını karşılamak için açık bir tema uygulanabilir. Yalnızca hero düzenine uygulanır.|
| Görüntü yerleştirme       | **Sol**,  **Sağ** | Bu özellik, resmin metnin solunda mı yoksa sağda mı olması gerektiğini belirtir. Yalnızca özellik düzenine uygulanır.  |

## <a name="add-a-content-block-module-to-a-new-page"></a>Yeni bir sayfaya içerik blok modülü ekleme

Bir yeni sayfaya Hero modülü eklemek ve gerekli özellikleri ayarlamak için aşağıdaki adımları izleyin.

1. **Şablonlara** gidin ve **İçerik bloğu şablonu** adlı bir sayfa şablonu oluşturun.
1. Varsayılan sayfanın **ana** yuvasına bir Hero modülü ekleyin.
1. **Kaydet**'i seçin, şablonu iade etmek için **Düzenlemeyi bitir**'i ve ardından yayımlamak için **Yayımla**'yı seçin.
1. **İçerik bloğu sayfası** adlı bir sayfa oluşturmak için yeni oluşturduğunuz hero şablonunu kullanın.
1. Varsayılan sayfada **ana** yuvayı seçin, üç nokta düğmesini (**...**) ve sonra **Modül ekle**'yi seçin.
1. **Modül Ekle** iletişim kutusunda **modüller'i seçin**, Hero modülünü seçin ve **Tamam**'ı seçin.
1. Soldaki anahat ağacında, içerik bloku modülünü seçin.
1. Sağdaki özellikler bölmesinde, **Resim Ekle**'yi seçin. Sonra da varolan bir görüntüyü seçin veya yeni bir görüntü yükleyin.
1. **Başlık** öğesini seçin.
1. **Başlık** iletişim kutusunda başlık metnini ekleyin, başlık düzeyini seçin ve **Tamam**'ı seçin.
1. **Zengin metin** altında, istediğiniz metni ekleyin.
1. **Bağlantı Ekle**'yi seç.
1. **Bağlantı** iletişim kutusunda bağlantı metni, bağlantı URL 'si ve bağlantı için bir Aria etiketi ekleyin ve **Tamam**'ı seçin.
1. **Hero** düzenini seçin.
1. **Kaydet**'i seçin ve ardından sayfayı önizlemek için **Önizleme**'yi seçin.
1. Şablonu iade etmek için **Düzenlemeyi bitir**'i seçin, ardından yayımlamak için **Yayımla**'yı seçin. 

## <a name="additional-resources"></a>Ek kaynaklar

[Modül kitaplığına genel bakış](starter-kit-overview.md)

[Promosyon başlığı modülü](add-alert.md)

[Döngü modülü](add-carousel.md)

[Metin bloğu modülü](add-content-rich-block.md)

[Video oynatıcı modülü](add-video-player.md)
