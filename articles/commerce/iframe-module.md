---
title: iFrame modülü
description: Bu makale iframe modülünü kapsamaktadır ve Microsoft Dynamics 365 Commerce'ün site sayfalarına nasıl ekleneceğini açıklamaktadır.
author: anupamar-ms
ms.date: 05/18/2022
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
ms.openlocfilehash: e9f1804cde1010c585d53d63bc0a487bc5407552
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8858949"
---
# <a name="iframe-module"></a>iFrame modülü

[!include [banner](includes/banner.md)]

Bu makale iframe modülünü kapsamaktadır ve Microsoft Dynamics 365 Commerce'ün site sayfalarına nasıl ekleneceğini açıklamaktadır.

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
1. **Yeni şablon** iletişim kutusunda **Şablon adı** altında, **Pazarlama şablonu**'nu girin ve **Tamam**'ı seçin.
1. **Kaydet**'i seçin, şablonu iade etmek için **Düzenlemeyi bitir**'i ve ardından yayımlamak için **Yayımla**'yı seçin.
1. **Sayfalar**'a gidin ve yeni sayfa oluşturmak için **Yeni**'yi seçin.
1. **Yeni sayfa oluştur** iletişim kutusunda **Sayfa adı** altında, **Pazarlama sayfası**'nı girin ve **Tamam**'ı seçin.
1. **Şablon seç** bölümünde, oluşturduğunuz **Pazarlama şablonunu** seçin ve sonra **İleri**'yi seçin.
1. **Bir düzen seçin** bölümünde, bir sayfa düzeni seçin (ör. **Esnek düzen**) ve sonra **İleri**'yi seçin.
1. **İnceleyin ve bitirin** bölümünde, sayfa yapılandırmasını gözden geçirin. Sayfa bilgilerini düzenlemeniz gerekiyorsa, **Geri**'yi seçin. Sayfa bilgileri doğruysa, **Sayfa oluştur**'u seçin. 
1. Yeni sayfanın **Ana** alanında, üç nokta düğmesini (**...**) ve sonra **Modül ekle**'yi seçin.
1. **Modül seç** iletişim kutusunda **Konteyner** modülünü seçin ve **Tamam**'ı seçin.
1. Modülün özellikler bölmesinde, **Genişlik** değerini **Dolgu Kapsayıcısı** olarak ayarlayın.
1. **Konteyner** alanında, üç nokta (**...**) düğmesini seçin ve **Modül ekle**'yi seçin.
1. **Modülleri seç** iletişim kutusunda **iframe** modülünü seçin ve **Tamam**'ı seçin.
1. Modülün özellikler bölmesinde, **Hedef URL** değerini bir videonun harici URL'si olarak ayarlayın.
1. İhtiyacınıza göre, **Başlık** ve **Yükseklik** gibi diğer özellikleri ayarlayın.
1. **Kaydet**'i seçin, sayfayı iade etmek için **Düzenlemeyi bitir**'i ve ardından yayımlamak için **Yayımla**'yı seçin.
1. Sitenizdeki pazarlama sayfasına gidin. Videonun iframe modülünde işlendiğini görürsünüz.

> [!NOTE]
> iFrame modülü harici içerik barındırdığı için, site yazarları bir iFrame modülü içinde barındırılan içeriğin ilgili pazardaki içerik sınırlama ilkelerini ihlal etmemesini sağlamalıdır. iFrame modülünü kullanan bir sayfada içerik ihlali varsa site yazarı, site oluşturucuda sayfayı açıp, iFrame modülü yuvasında **Modülü kaldır**'ı seçerek ve sonra sayfayı kaydedip yeniden yayımlayarak iFrame modülünü kaldırabilir.

## <a name="additional-resources"></a>Ek kaynaklar

[Modül kitaplığına genel bakış](starter-kit-overview.md)

[İçerik Güvenliği İlkesini (CSP) yönetme](manage-csp.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
