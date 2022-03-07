---
title: Iframe modülü
description: Bu konu iframe modülünü kapsamaktadır ve Microsoft Dynamics 365 Commerce'ün site sayfalarına nasıl ekleneceğini açıklamaktadır.
author: anupamar-ms
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2020-02-10
ms.dyn365.ops.version: Release 10.0.13
ms.openlocfilehash: 55526b34eb057abb9a8c33cbfea1807601da6577
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/06/2021
ms.locfileid: "6348226"
---
# <a name="iframe-module"></a>Iframe modülü

[!include [banner](includes/banner.md)]

Bu konu iframe modülünü kapsamaktadır ve Microsoft Dynamics 365 Commerce'ün site sayfalarına nasıl ekleneceğini açıklamaktadır.

iframe modülü, bir sitedeki harici içeriği barındıran bir iframe (satır içi çerçeve) sağlar. Örneğin, herhangi bir site sayfasında bir YouTube videosu veya PDF dosyası görüntüleyiciyi barındırmak için kullanılabilir. 

Iframe modülü için hedef URL gereklidir. Sonra, hedef sayfanın içeriğini bir HTML **iframe** öğesinin içinde barındırır. Harici URL'lerin sitenin içerik güvenlik ilkesi (CSP) yönergeleri gereğince izin verilenler listesinde olmaları gerekir. Iframe içeriği için URL'lere **frame-ancestor** yönergesi kullanılarak izin verilmesi gerekir. Daha fazla bilgi için bkz. [İçerik Güvenlik İlkesini (CSP) yönetme](manage-csp.md).

> [!NOTE]
> iframe modülü Dynamics 365 Commerce 10.0.13 sürümünde bulunur.

Aşağıdaki resimde, site sayfalarındaki harici videoları gösteren iframe modülleri örnekleri gösterilmektedir.

![Harici videoları gösteren iframe modülleri örneği.](./media/ecommerce-iframe.PNG)

## <a name="iframe-module-properties"></a>iframe modülü özellikleri

| Özellik adı             | Değer                 | Tanım |
|---------------------------|-----------------------|-------------|
| Başlık | Metin | Modülün başlığı. |
| Hedef URL | URL | Modülde barındırılan URL. |
| Yükseklik | Sayı veya yüzde | Modülün piksel cinsinden veya yüzde olarak yüksekliği. Örneğin, **100** değeri piksel sayısı olarak değerlendirilir ve **%100** değeri yüzde olarak kabul edilir. |
| Aria etiketi | Metin | Erişilebilirlik amacıyla, bir Erişilebilir Zengin İnternet Uygulamaları (ARIA) etiketi tanımlanabilir. |

## <a name="add-an-iframe-module-to-a-page"></a>Sayfaya iframe modülü ekleme

Bir sayfaya harici bir video göstermek üzere bir iframe modülü eklemek için aşağıdaki adımları izleyin.

1. Bir yeni şablonu oluşturmak için **Şablonlar**'a gidin ve **Yeni**'yi seçin.
1. **Yeni Şablon** iletişim kutusunda **Şablon adı** altında, **Pazarlama şablonu**'nu girin ve **Tamam**'ı seçin.
1. **Kaydet**'i seçin, şablonu iade etmek için **Düzenlemeyi bitir**'i ve ardından yayımlamak için **Yayımla**'yı seçin.
1. **Sayfalar**'a gidin ve yeni sayfa oluşturmak için **Yeni**'yi seçin.
1. **Şablon seçin** iletişim kutusunda **Pazarlama şablonu** şablonunu seçin. **Sayfa adı** altında **Pazarlama sayfası** girin ve **Tamam**'ı seçin.
1. Yeni sayfada **ana** yuvayı seçin, üç nokta düğmesini (**...**) ve sonra **Modül ekle**'yi seçin.
1. **Modül Ekle** iletişim kutusunda **Konteyner** modülünü seçin ve **Tamam**'ı seçin.
1. Modülün özellikler bölmesinde, **Genişlik** değerini **Dolgu Kapsayıcısı** olarak ayarlayın.
1. **Konteyner** yuvası için üç nokta (**...**) düğmesini seçin ve **Modül Ekle**'yi seçin.
1. **Modül Ekle** iletişim kutusunda **iframe** modülünü seçin ve **Tamam**'ı seçin.
1. Modülün özellikler bölmesinde, **Hedef URL** değerini bir videonun harici URL'si olarak ayarlayın.
1. İhtiyacınıza göre, **Başlık** ve **Yükseklik** gibi diğer özellikleri ayarlayın.
1. **Kaydet**'i seçin, sayfayı iade etmek için **Düzenlemeyi bitir**'i ve ardından yayımlamak için **Yayımla**'yı seçin.
1. Sitenizdeki pazarlama sayfasına gidin. Videonun iframe modülünde işlendiğini görürsünüz.
 
## <a name="additional-resources"></a>Ek kaynaklar

[Modül kitaplığına genel bakış](starter-kit-overview.md)

[İçerik Güvenliği İlkesini (CSP) yönetme](manage-csp.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]