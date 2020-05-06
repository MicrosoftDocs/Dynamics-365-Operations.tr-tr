---
title: Promosyon başlık modülü
description: Bu konu promosyon başlığı modüllerini kapsamaktadır ve Microsoft Dynamics 365 Commerce'un site sayfalarına nasıl ekleneceğini açıklamaktadır.
author: anupamar-ms
manager: annbe
ms.date: 04/14/2020
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
ms.openlocfilehash: 12cabbf0b8d9f337f15a8cd6cb1f2a85100b75f7
ms.sourcegitcommit: 7a1d01122790b904e2d96a7ea9f1d003392358a6
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/17/2020
ms.locfileid: "3269786"
---
# <a name="promo-banner-module"></a>Promosyon başlık modülü


[!include [banner](includes/banner.md)]

Bu konu promosyon başlığı modüllerini kapsamaktadır ve Microsoft Dynamics 365 Commerce'un site sayfalarına nasıl ekleneceğini açıklamaktadır.

## <a name="overview"></a>Genel Bakış

Promosyon başlığı modülleri, bir sayfadaki satır içi bilgilendirme iletilerini göstermekte kullanılır. Bir e-ticaret sitesinin tüm sayfalarında görünen site çapında yükseltmeleri göstermek için kullanılabilirler. 

Promosyon başlığı modülleri bir metin iletisini ve bir bağlantıyı destekler. Bir promosyon başlık modülüne birden fazla ileti eklenirse, müşterilerin tüm iletiler arasında dolaşmasına olanak veren bir döner başlığı olur. 

Promosyon başlığı, içerik yönetimi sistemindeki (CMS) veriler tarafından yönlendiriliyor ve herhangi bir sayfaya konabilir.

## <a name="usage-examples-of-promo-banners-in-e-commerce"></a>E-ticaret'daki promosyon başlık sayfaları için kullanım örnekleri

Promosyon başlık sayfaları site başlığında, aşağıdaki örneklerde olduğu gibi, site çapında yükseltmeleri veya iletileri göstermek amacıyla kullanılabilir.

"Yıllık satış, 10 gün içinde biter"

"Okul satışı ile büyük bir tasarruf yapın. Şimdi alışveriş yap."

## <a name="promo-banner-module-properties"></a>Promosyon başlığı modülü özellikleri

| Özellik adı             | Value                              | Tanım |
|---------------------------|------------------------------------|-------------|
| Başlık iletileri           | Metin ve bağlantılar                     | Metin ve bağlantılar dizisi. |
| Otomatik yürüt                  | **Doğru** veya **yanlış**              | Birden fazla ileti yapılandırılmışsa, iletilerin otomatik olarak açılıp eklenmesini belirten bir değer. |
| Slayt geçiş aralığı | Milisaniyelerin sayısı (MS)      | İletiler arasında geçiş yapmak için kullanılan aralık. |
| Kapatmaya izin ver             | **Doğru** veya **yanlış**              | Değer **doğru** olarak ayarlanırsa, müşteriler uyarıyı yok edebilir. |
| Carusel kolu göster     | **Doğru** veya **yanlış**              | Döner değiştiricilerin gösterilip gösterilmeyeceğini belirten ve müşterilerin birden çok Başlık öğelerini el ile dolaşabilmesi için bir değer. |
| Metin hizalama            | **Sağ**, **Sol** veya **Orta** | Promosyon başlık modülünde metin hizalaması. |
| Bağla                      | Bir URL                              | İsteğe bağlı bağlantı için URL. |

## <a name="add-a-promo-banner-module-to-a-page"></a>Bir sayfaya bir promosyon başlığı ekle 

Bir sayfaya bir promosyon başlığı modülü eklemek ve gerekli özellikleri ayarlamak için şu adımları izleyin.

1. Yeni sayfa şablonu oluşturmak için **Yeni**'yi seçin.
1. **Yeni Şablon** iletişim kutusunda **Şablon adı** altında, **Promosyon başlığı şablonu**'nu girin ve **Tamam**'ı seçin.
1. **Sayfa Anahattı** altında, bir **Varsayılan sayfa** modülünü **Gövde** yuvasına ekleyin. 
1. Şablonu iade etmek için **Düzenlemeyi bitir**'i seçin, ardından yayımlamak için **Yayımla**'yı seçin. 
1. **Promosyon başlığı sayfası** adlı bir sayfa oluşturmak için yeni oluşturduğunuz uyarı şablonunu kullanın. 
1. Yeni sayfanın **ana** yuvasına bir konteyner modülü ekleyin. 
1. Sağdaki panoda, **Genişlik** değerini **Konteyneri doldur**'a ayarlayın.
1. **Sayfa Anahattı** altında, bir promosyon başlığı modlünü konteyner modülüne ekleyin.
1. Başlık modülünün ayarlarında bir veya daha fazla başlık ekleyin. Her iletinin bir bağlantı ile birlikte bir metni olabilir. Modülü daha fazla özelleştirmek için diğer özellikleri düzenleyebilirsiniz.
1. **Kaydet**'i seçin ve ardından sayfayı önizlemek için **Önizleme**'yi seçin. Sayfanın üst kısmında, eklediğiniz metni içeren bir uyarı görmelisiniz.
1. Sayfayı iade etmek için **Düzenlemeyi bitir**'i seçin, ardından yayımlamak için **Yayımla**'yı seçin. 

> [!NOTE]
> Bir promosyon başlığı genellikle sayfa üstbilgisi yuvasında veya alt başlık yuvasında kullanılır.


## <a name="additional-resources"></a>Ek kaynaklar

[Başlangıç paketine genel bakış](starter-kit-overview.md)

[Döngü modülü](add-carousel.md)

[Metin bloku modülü](add-content-rich-block.md)

[İçerik blok modülü](add-hero-module.md)

[Video oynatıcı modülü](add-video-player.md)
