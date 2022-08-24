---
title: Metin bloku modülü
description: Bu makale metin bloku modüllerini kapsamaktadır ve Microsoft Dynamics 365 Commerce'un site sayfalarına nasıl ekleneceğini açıklamaktadır.
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
ms.dyn365.ops.version: Release 10.0.5
ms.search.industry: ''
ms.search.form: ''
ms.openlocfilehash: 9e422c203d719b2e46620ce50b9d029e7ebd8d4c
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/12/2022
ms.locfileid: "9270495"
---
# <a name="text-block-module"></a>Metin bloku modülü

[!include [banner](includes/banner.md)]

Bu makale metin bloku modüllerini kapsamaktadır ve Microsoft Dynamics 365 Commerce'un site sayfalarına nasıl ekleneceğini açıklamaktadır.

Bir metin bloğu modülü, metin içeriği eklemek için kullanılan bir modüldür. Bu içerik bilgilendirici veya promosyon olabilir.

Metin bloku modülleri, içerik yönetimi sistemindeki (CMS) veriler tarafından yönlendiriliyor ve herhangi bir sayfaya konabilir. Bunlar sayfa bağlamına veya diğer modüllere bağımlı olmayan bağımsız modüllerdir.

## <a name="examples-of-text-block-modules-in-e-commerce"></a>E-ticarette metin bloku örnekleri

Metin bloku modüller aşağıdaki yollarla kullanılabilir:

* Ürün ayrıntıları sayfasında ürün özelliklerini sergileme.
* Her sayfada yalnızca bilgi amacıyladır. Örneğin, bağlılık programlarının yararlarını açıklayabilir, Sevkiyat ve iade ilkelerini açıklayabilir, sık sorulan soruların yanıtlanması veya "Hakkımızda" içeriği sağlayabilirler.
* Ürün ayrıntıları sayfasına özel iletiler eklemek için. (örneğin, "$50 üzerinden olan siparişler için ücretsiz sevkiyat").
* Ürün Ayrıntıları sayfaları, sepet sayfaları, kullanıma alma sayfaları ve diğer sayfalar hakkında feragatler ve ilgili kişi ayrıntıları için (örneğin, "Sevkiyat ve iadeler depolama ilkelerine tabidir").

Aşağıdaki resimde giriş sayfasında kullanılan bir metin bloku modülü örneği gösterilmektedir.

![Metin bloğu modülü örneği.](./media/ecommerce-textblock.PNG)

## <a name="text-block-module-properties"></a>Metin bloku modülü özellikleri

| Özellik adı     | Değer                                            | Tanım |
|-------------------|--------------------------------------------------|-------------|
| Zengin metin         | Zengin metin                                        | Paragraf metni. Kalın, altı çizili, italik metin gibi bazı temel zengin metin özellikleri desteklenir. |
| Özel sınıfı adı | Geçişli stil sayfaları (CSS) sınıf adı        | Bu modülü biçimlendirmek için bir CSS geliştiricinin sağladığı özel sınıfın adı. Sınıf adı Tema paketinde tanımlanmalıdır. |
| Yazı türü boyutu         | **Küçük**, **orta**, **büyük** veya **Ekstra büyük** | İçeriğin yazı tipi boyutu. |

## <a name="add-a-text-block-module-to-a-page"></a>Bir sayfaya metin bloku modülü ekleme

Bir yeni sayfaya metin bloku modülü eklemek ve gerekli özellikleri ayarlamak için aşağıdaki adımları izleyin.

1. Bir yeni şablonu oluşturmak için **Şablonlar**'a gidin ve **Yeni**'yi seçin.
1. **Yeni şablon** iletişim kutusundaki **Şablon adı** bölümünde, **İçerik şablonu**'nu girin.
1. **Gövde** alanında, üç nokta (**...**) düğmesini seçin ve **Modül ekle**'yi seçin.
1. **Modülleri seç** iletişim kutusunda **Varsayılan sayfa** modülünü seçin ve **Tamam**'ı seçin.
1. **Kaydet**'i seçin, şablonu iade etmek için **Düzenlemeyi bitir**'i ve ardından yayımlamak için **Yayımla**'yı seçin.
1. **Sayfalar**'a gidin ve yeni sayfa oluşturmak için **Yeni**'yi seçin.
1. **Yeni sayfa oluştur** iletişim kutusundaki **Sayfa adı** bölümünde, **İçerik sayfası**'nı girin ve **Tamam**'ı seçin.
1. **Şablon seç** bölümünde, **İçerik şablonu**'nu seçin ve ardından **İleri**'yi seçin.
1. **Bir düzen seçin** bölümünde, bir sayfa düzeni seçin (ör. **Esnek düzen**) ve sonra **İleri**'yi seçin.
1. **İnceleyin ve bitirin** bölümünde, sayfa yapılandırmasını gözden geçirin. Sayfa bilgilerini düzenlemeniz gerekiyorsa, **Geri**'yi seçin. Sayfa bilgileri doğruysa, **Sayfa oluştur**'u seçin. 
1. Yeni sayfanın **Ana** alanında, üç nokta düğmesini (**...**) ve sonra **Modül ekle**'yi seçin.
1. **Modül seç** iletişim kutusunda **Konteyner** modülünü seçin ve **Tamam**'ı seçin.
1. Konteyner modülü için özellik panosunda **Genişlik** özelliğini **Konteyneri doldur**'a ayarlayın.
1. **Konteyner** alanında, üç nokta (**...**) düğmesini seçin ve **Modül ekle**'yi seçin.
1. **Modülleri seç** iletişim kutusunda **Metin bloğu** modülünü seçin ve **Tamam**'ı seçin. 
1. Metin bloku modülünün özellik panosunda, **Zengin metin** alanına bir metin ekleyin.
1. **Kaydet**'i seçin ve ardından sayfayı önizlemek için **Önizleme**'yi seçin.
1. Sayfayı iade etmek için **Düzenlemeyi bitir**'i seçin, ardından yayımlamak için **Yayımla**'yı seçin.

## <a name="additional-resources"></a>Ek kaynaklar

[Modül kitaplığına genel bakış](starter-kit-overview.md)

[Promosyon başlığı modülü](add-alert.md)

[Döngü modülü](add-carousel.md)

[İçerik bloğu modülü](add-hero-module.md)

[Video oynatıcı modülü](add-video-player.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]
