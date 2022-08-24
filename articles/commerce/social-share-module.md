---
title: Sosyal içerik paylaşım modülü
description: Bu makale sosyal içerik paylaşım modüllerini kapsamaktadır ve Microsoft Dynamics 365 Commerce'ün site sayfalarına nasıl ekleneceğini açıklamaktadır.
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
ms.dyn365.ops.version: Release 10.0.14
ms.custom: ''
ms.assetid: ''
ms.search.industry: ''
ms.openlocfilehash: 88bc5469e3072b625836cc942efbd2206f6dd6ba
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/12/2022
ms.locfileid: "9284697"
---
# <a name="social-share-module"></a>Sosyal içerik paylaşım modülü

[!include [banner](includes/banner.md)]

Bu makale sosyal içerik paylaşım modüllerini kapsamaktadır ve Microsoft Dynamics 365 Commerce'ün site sayfalarına nasıl ekleneceğini açıklamaktadır.

Sosyal içerik paylaşımı modülleri, kullanıcıların e-ticaret sitesi sayfası URL'lerini Facebook, Twitter, Pinterest ve LinkedIn gibi sosyal medya üzerinde paylaşmasına olanak tanır. Site sayfası URL'Leri e-posta yoluyla da paylaşılabilir. Sosyal içerik paylaşımı modülleri, kullanıcıların ürün bilgilerini paylaşmasına yardımcı olmak için ürün ayrıntıları sayfalarında (PDP'ler) kullanılır.

Her sosyal içerik paylaşım modülü sosyal içerik paylaşımı öğe modülleri için bir kapsayıcıdır. Her sosyal içerik paylaşımı öğe modülü belirli bir sosyal medya sitesini işaret etmek üzere yapılandırılabilir. Facebook, Twitter, Pinterest, LinkedIn ve e-posta ile tümleştirme, hazırda desteklenmektedir. Bir site kullanıcısı bir sosyal medya sembolünü seçtiğinde, ilgili sosyal medya sitesi için bir HTML iframe başlatılır. iframe içinde kullanıcı oturum açarak, görüntüledikleri sayfa içeriğini paylaşabilir.

Her sosyal medya platformu tanımlama bilgilerini izleyebilir, bu nedenle bu modül site kullanıcılarının tanımlama bilgisi onayı bildirim iletisini kabul etmesini gerektirir. Tanımlama bilgisi izni verilmediğinde, modül sayfada gizlenir. Daha fazla bilgi için bkz. [Tanımlama bilgisi uyumluluğu](cookie-compliance.md).

Aşağıdaki çizimde, ürün ayrıntıları sayfasında kullanılan sosyal içerik paylaşım modülüne bir örnek gösterilmektedir.

![Sosyal içerik paylaşım modülü örneği.](./media/ecommerce-socialshare.png)

## <a name="social-share-module-properties"></a>Sosyal içerik paylaşım modülü özellikleri

| Özellik adı             | Değer                 | Tanım |
|---------------------------|-----------------------|-------------|
| Açıklama yazısı                  | Metin | Bu özellik modül için bir açıklamalı alt yazı belirtir. |
| Hizalama | **Yatay** veya **Dikey**  | Bu özellik, sosyal medya öğelerinin yerleşim yönünü tanımlar. |

## <a name="social-share-item-module-properties"></a>Sosyal içerik paylaşım öğesi modülü özellikleri
| Özellik adı             | Değer                 | Tanım |
|---------------------------|-----------------------|-------------|
| Sosyal medya              | **Facebook**, **Twitter**, **Pinterest**, **LinkedIn**, **Posta** | Sosyal medya platformlarının listesinin bulunduğu bir açılan menü. |
| Simge |Görüntü    | Bu, ilgili sosyal medyada gösterilecek resim olacaktır. En iyi uygulama olarak, her bir platformda kullanılacak resim için sosyal medya platformunun SDK'sine başvurun. |

## <a name="add-a-social-share-module-to-a-buy-box-module"></a>Satın al kutusu modülüne bir sosyal içerik paylaşım modülü ekleme

Satın al kutusu modülüne bir sosyal içerik paylaşım modülü eklemek için aşağıdaki adımları izleyin.

1. Fabrikam sitesinde, **Sayfalar**'ı seçin ve sonra ürün ayrıntıları sayfasını açmak için **DefaultPDP** sayfasını seçin. 
1. **Buybox (gerekli)** alanında, üç nokta (**...**) düğmesini seçin ve **Modül ekle**'yi seçin.
1. **Modülleri seç** iletişim kutusunda **Sosyal Paylaşım** modülünü seçin ve **Tamam**'ı seçin.
1. **Sosyal Paylaşım** alanında, üç nokta (**...**) düğmesini seçin ve **Modül ekle**'yi seçin.
1. **Modülleri seç** iletişim kutusunda **SocialShare** modülünü seçin ve **Tamam**'ı seçin.
1. **Socialshare** modülünün özellikler bölmesinde, **Yönlendirme** altında **Yatay**'ı seçin. Gerektiğinde bir açıklamalı alt yazı ekleyin.
1. **SocialShare** alanında, üç nokta (**...**) düğmesini seçin ve **Modül ekle**'yi seçin.
1. **Modülleri seç** iletişim kutusunda **SocialShareItem** modülünü seçin ve **Tamam**'ı seçin.
1. **SocialShareItem** modülünün özellikler bölmesinde, **Sosyal Medya** altında **Facebook** öğesini seçin.
1. **SocialShareItem** modülünün özellikler bölmesinde, **Simge** altında **+Resim ekleyin** öğesini seçin.
1. **Ortam Seçicisi** iletişim kutusunda Facebook logo resmini seçin ve **Tamam**'ı seçin. Herhangi bir Facebook logo resmi yoksa karşıya yüklemek için **Yeni ortam öğesini karşıya yükle**'yi seçin.
1. Gerektiğinde ek **SocialShareItem** modülleri ekleyin ve yapılandırın.
1. **Kaydet**'i seçin ve ardından sayfayı önizlemek için **Önizleme**'yi seçin. Sayfada sosyal içerik paylaşım modülü gösterilir.
1. Sayfayı iade etmek için **Düzenlemeyi bitir**'i seçin, ardından yayımlamak için **Yayımla**'yı seçin.

## <a name="additional-resources"></a>Ek kaynaklar

[Modül kitaplığına genel bakış](starter-kit-overview.md)

[Satın alma kutusu modülü](add-buy-box.md)

[Tanımlama bilgisi uyumluluğu](cookie-compliance.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
