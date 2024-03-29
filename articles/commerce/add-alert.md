---
title: Promosyon başlık modülü
description: Bu makale promosyon başlığı modüllerini kapsamaktadır ve Microsoft Dynamics 365 Commerce'un site sayfalarına nasıl ekleneceğini açıklamaktadır.
author: anupamar-ms
ms.date: 05/18/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.custom: ''
ms.assetid: ''
ms.search.industry: ''
ms.openlocfilehash: fbde146923d1448e382cbf2458880f7e300f605c
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/12/2022
ms.locfileid: "9279748"
---
# <a name="promo-banner-module"></a>Promosyon başlık modülü

[!include [banner](includes/banner.md)]

Bu makale promosyon başlığı modüllerini kapsamaktadır ve Microsoft Dynamics 365 Commerce'un site sayfalarına nasıl ekleneceğini açıklamaktadır.

Promosyon başlığı modülleri, bir sayfadaki satır içi bilgilendirme iletilerini göstermekte kullanılır. Bir e-ticaret sitesinin tüm sayfalarında görünen site çapında yükseltmeleri göstermek için kullanılabilirler. 

Promosyon başlığı modülleri bir metin iletisini ve bir bağlantıyı destekler. Bir promosyon başlık modülüne birden fazla ileti eklenirse, müşterilerin tüm iletiler arasında dolaşmasına olanak veren bir döner başlığı olur. 

Promosyon başlığı, içerik yönetimi sistemindeki (CMS) veriler tarafından yönlendiriliyor ve herhangi bir sayfaya konabilir.

## <a name="usage-examples-of-promo-banners-in-e-commerce"></a>E-ticaret'teki promosyon başlık sayfaları için kullanım örnekleri

Promosyon başlık sayfaları site başlığında, aşağıdaki örneklerde olduğu gibi, site çapında yükseltmeleri veya iletileri göstermek amacıyla kullanılabilir.

"Yıllık satış, 10 gün içinde biter"

"Okul satışı ile büyük bir tasarruf yapın. Şimdi alışveriş yap."

"Şükran günü İNDİRİM alışverişi yap!" 

Aşağıdaki resimde, bir promosyon başlığı örneği gösterilmektedir.

![Promosyon başlık modülü örneği.](./media/ecommerce-Promobanner.PNG)

## <a name="promo-banner-module-properties"></a>Promosyon başlığı modülü özellikleri

| Özellik adı             | Değer                              | Tanım |
|---------------------------|------------------------------------|-------------|
| Başlık iletileri           | Metin ve bağlantılar                     | Metin ve bağlantılar dizisi. |
| Otomatik yürüt                  | **Doğru** veya **yanlış**              | Birden fazla ileti yapılandırılmışsa, iletilerin otomatik olarak açılıp eklenmesini belirten bir değer. |
| Slayt geçiş aralığı | Milisaniyelerin sayısı (MS)      | İletiler arasında geçiş yapmak için kullanılan aralık. |
| Kapatmaya izin ver             | **Doğru** veya **yanlış**              | Değer **doğru** olarak ayarlanırsa, müşteriler uyarıyı yok edebilir. |
| Carusel kolu göster     | **Doğru** veya **yanlış**              | Döner değiştiricilerin gösterilip gösterilmeyeceğini belirten ve müşterilerin birden çok Başlık öğelerini el ile dolaşabilmesi için bir değer. |
| Metin hizalama            | **Sağ**, **Sol** veya **Orta** | Promosyon başlık modülünde metin hizalaması. |
| Bağla                      | Bir URL                              | İsteğe bağlı bağlantı için URL. |
|Metin hizalama             | **Sağ**, **Sol** veya **Orta** | Bu özellik, Adventure Works temalarında bir tema uzantısı olarak mevcuttur. Kullanıcının, promosyon başlığında metin hizalaması ayarlamasını sağlar. |

> [!IMPORTANT]
> Adventure Works teması Dynamics 365 Commerce Sürüm 10.0.20 itibarıyla kullanılabilir.

## <a name="add-a-promo-banner-module-to-a-page"></a>Bir sayfaya bir promosyon başlığı ekle 

Bir sayfaya bir promosyon başlığı modülü eklemek ve gerekli özellikleri ayarlamak için şu adımları izleyin.

1. Bir yeni şablonu oluşturmak için **Şablonlar**'a gidin ve **Yeni**'yi seçin.
1. **Yeni şablon** iletişim kutusundaki **Şablon Adı** bölümünde, **Promosyon başlığı şablonu**'nu girin ve **Tamam**'ı seçin.
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

[Modül kitaplığına genel bakış](starter-kit-overview.md)

[Döngü modülü](add-carousel.md)

[Metin bloğu modülü](add-content-rich-block.md)

[İçerik bloğu modülü](add-hero-module.md)

[Video oynatıcı modülü](add-video-player.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
