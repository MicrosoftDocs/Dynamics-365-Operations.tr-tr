---
title: İçerik yerleştirme modülü
description: Bu konu içerik yerleştirme ve içerik yerleştirme öğesi modüllerini kapsamaktadır ve Microsoft Dynamics 365 Commerce'un site sayfalarına nasıl ekleneceğini açıklamaktadır.
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
ms.openlocfilehash: 1b64e930628c969334ff6e643ba23b77445e6e4c
ms.sourcegitcommit: 3a4e137ef3a96ba0a58c5352f4a3b57467ace9ae
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/11/2019
ms.locfileid: "2785312"
---
# <a name="content-placement-module"></a>İçerik yerleştirme modülü

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

Bu konu içerik yerleştirme ve içerik yerleştirme öğesi modüllerini kapsamaktadır ve Microsoft Dynamics 365 Commerce'un site sayfalarına nasıl ekleneceğini açıklamaktadır.

## <a name="overview"></a>Genel Bakış

İçerik yerleşim modülü, diğer modüllerin belirli bir düzene koyulacağı özel bir kapsayıcıdır. İçerik yerleşim modülleri aşağıdaki modül türlerini alt modüller olarak destekler: içerik yerleşim öğesi, hesap karşılama öğesi, hesap sipariş maddesi, hesap istek listesi öğesi ve hesap profili öğesi.

İçerik yerleşim modülleri, destekledikleri alt modülden veri türetin. Bu nedenle, içerik yerleşim modülleri, eklenen modüllere bağlı olarak çeşitli şekillerde kullanılabilir.

İçerik yerleşim öğesi modülleri, promosyonları, ilkeleri ve ürün özelliklerini sergilemek için hem görüntüleri hem de metni kullanır. Örneğin, bir içerik yerleşim öğesi modülü, bir giriş sayfasında mağaza ilkelerini veya kargo bilgilerini göstermek için kullanılabilir. İçerik yerleştirme öğesi modülleri, içerik yönetimi sistemindeki (CMS) veriler tarafından yönlendiriliyor ve herhangi bir sayfaya konabilir. Ancak, bunlar yalnızca bir içerik yerleşim modülü içinde kullanılabilirler.

## <a name="examples-of-content-placement-modules-in-e-commerce"></a>E-ticarette içerik yerleştirme modülleri örnekleri

* İçerik yerleştirme öğesi modülleri içeren içerik yerleşim modülleri, ürün özelliklerini, yükseltmeleri, mağaza ilkelerini, sevkiyat bilgilerini ve diğer bilgileri hem görüntü hem de metinden sergilebilecek bir giriş sayfasında veya pazarlama sayfalarında kullanılabilir.
* İçerik yerleştirme öğesi modülleri içeren içerik yerleşim modülleri, ürün özelliklerini sergilebilecek ürün ayrıntıları sayfalarında kullanılabilir.
* Hesap karşılama öğesi veya hesap sipariş öğesi modülleri içeren içerik yerleşim modülleri Hesap Yönetimi sayfalarında kullanılabilir.

## <a name="content-placement-module-properties"></a>İçerik yerleştirme modülü özellikleri

| Özellik adı | Değer | Tanım |
|---------------|-------|-------------|
| Genişlik         | **Kapsayıcıya sığdır** veya **Ekrana doldur** | Değer **konteynere sığdır** şekilde ayarlandıysa, içerik yerleştirme modülü içindeki öğeler içerik yerleştirme modülü genişliğiyle sınırlandırılır. Değer, **ekranı doldur**'a ayarlanmışsa, öğeler içerik yerleştirme modülü genişliğiyle sınırlandırılmaz ancak tam ekran moduna geçebilir. |

## <a name="content-placement-item-module-properties"></a>İçerik yerleştirme öğesi modülü özellikleri

| Özellik adı | Değer | Tanım |
|---------------|-------|-------------|
| Başlık       | Başlık metni ve başlık etiketleri (**H1**, **H2**, **H3**, **H4**, **H5** veya **H6**) | Her içerik yerleşim öğesi modülünün bir başlığı olabilir. **Başlık** özelliği Başlık etiketlerini destekler. Varsayılan olarak **H2** başlık etiketi kullanılır, ancak başlık etiketi erişilebilirlik gereksinimlerini karşılamak için değiştirilebilir. |
| Paragraf     | Paragraf metni | İçerik yerleşim öğesi modülleri zengin metin biçimindeki paragraf metnini destekler. Kalın, altı çizili, italik metin ve köprüler gibi bazı temel zengin metin özellikleri desteklenir. Bu yeteneklerden bazıları, modüle uygulanan sayfa teması tarafından geçersiz kılınabilir. |
| Görüntü         | Resim dosyası | Bir resim metinle ilişkilendirilebilir. |
| Bağla          | URL'ye bağlantı ve bağlantı metni | Kullanıcıları belirli bir sayfaya yeniden yönlendirmek için metne bir bağlantı eklenebilir. |
| Kutucuk boyutu     | **1** ile **12** arasında bir sayı | Her içerik yerleşim öğesi için bu özellik, öğenin içerik yerleşim modülüne doldurması gereken yuva sayısını tanımlar. İçerik yerleşim modülünün en büyük boyutu 12 yuvadır. İçerik yerleştirme modülündeki ilk *n* öğe için toplam döşeme boyutu 12 yuvayı geçerse, öğeler bir sonraki satıra kaydırılır. |

## <a name="add-a-content-placement-module-that-contains-a-content-placement-item-module-to-a-page"></a>Sayfaya içerik yerleşim öğesi modülü içeren bir içerik yerleşim modülü ekler

Yeni bir sayfaya içerik yerleşim öğesi modülü içeren bir içerik yerleşim modülü eklemek ve gerekli özellikleri ayarlamak için aşağıdaki adımları izleyin.

1. **İçerik yerleşim şablonu** adlı bir şablonu oluşturun.
1. Varsayılan sayfanın **ana** yuvasına bir içerik yerleşim modülü ekleyin.
1. İçerik yerleşim öğesi modülünü bir içerik yerleşim modülüne ekleyin.
1. Şablonu giriş yapın ve yayımlayın.
1. **İçerik yerleştirme sayfası** adlı bir sayfa oluşturmak için yeni oluşturduğunuz içerik yerleştirme şablonunu kullanın.
1. Yeni sayfanın **ana** yuvasına bir içerik yerleşim modülü ekleyin.
1. İçerik yerleşim öğesi modülünü bir içerik yerleşim modülüne ekleyin.
1. İçerik yerleşim öğesi modülünün Özellik bölmesinde bir resim seçin, başlık ekleyin, paragraf ekleyin, bağlantı ekleyin, bağlantı URL'sini ayarlayın ve döşeme boyutunu **6** olarak ayarlayın.
1. Aynı döşeme boyutuna sahip başka bir içerik yerleşim öğesi modülü eklemek için 7. ve 8. adımlarını yineleyin.
1. Sayfayı kaydet ve önizleyin. Yan yana görünen iki içerik yerleşimi öğesi görmelisiniz. Her bir içerik yerleşim öğesi modülünün **döşeme boyutu** özelliğini ayarlayabilir veya istenen mizanpajı elde etmek için daha fazla modül ekleyebilirsiniz.
1. Sayfayı giriş yapın ve yayımlayın.

## <a name="additional-resources"></a>Ek kaynaklar

[Başlangıç paketine genel bakış](starter-kit-overview.md)

[Uyarı modülü](add-alert.md)

[Döngü modülü](add-carousel.md)

[İçerik zengin blok modülü](add-content-rich-block.md)

[Özellik modülü](add-feature-module.md)

[Hero modülü](add-hero-module.md)

[Video oynatıcı modülü](add-video-player.md)
