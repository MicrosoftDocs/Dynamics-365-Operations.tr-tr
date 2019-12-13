---
title: Uyarı modülü
description: Bu konu uyarı modüllerini kapsamaktadır ve Microsoft Dynamics 365 Commerce'un site sayfalarına nasıl ekleneceğini açıklamaktadır.
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
ms.openlocfilehash: 82138dd7f0934f732215f67a3726638eb87075d4
ms.sourcegitcommit: 3a4e137ef3a96ba0a58c5352f4a3b57467ace9ae
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/11/2019
ms.locfileid: "2785364"
---
# <a name="alert-module"></a>Uyarı modülü

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

Bu konu uyarı modüllerini kapsamaktadır ve Microsoft Dynamics 365 Commerce'un site sayfalarına nasıl ekleneceğini açıklamaktadır.

## <a name="overview"></a>Genel Bakış

Bir sayfada satır içi bilgilendirici iletiler göstermek için bir uyarı modülü kullanılır. Uyarı modülleri bir metin iletisini ve bir bağlantıyı destekler. Bir e-ticaret sitesinin tüm sayfalarında görünen site çapında yükseltmeleri göstermek için kullanılabilirler. 

Uyarı modülleri, içerik yönetimi sistemindeki (CMS) veriler tarafından yönlendiriliyor ve herhangi bir sayfaya konabilir.

## <a name="examples-of-alert-modules-in-e-commerce"></a>E-ticarette uyarı modülleri örnekleri

Site üstbilgisinde site çapında yükseltmeler veya iletiler olduğu için uyarı modülleri kullanılabilir. Burada bazı örnekler verilmiştir:

"Yıllık satış, 10 gün içinde biter"

"Okul satışı ile büyük bir tasarruf yapın. Şimdi alışveriş yap."

## <a name="alert-module-properties"></a>Uyarı modülü özellikleri

| Özellik adı  | Değer                              | Tanım |
|----------------|------------------------------------|-------------|
| Metin           | Metin                               | Uyarı modülünde görünen metin iletisi. |
| Metin hizalama | **Sağ**, **Sol** veya **Orta** | Metnin uyarı modülünde nasıl hizalandığını tanımlayan bir değer. |
| Uyarıyı kapat  | **Doğru** veya **yanlış**              | Değer **doğru** olarak ayarlanırsa, müşteri uyarıyı yok edebilir. |
| Bağla           | URL                                | İsteğe bağlı bağlantı için URL. |

## <a name="add-an-alert-module-to-a-page"></a>Sayfaya uyarı modülü ekleme 

Bir sayfaya uyarı modülü eklemek ve gerekli özellikleri ayarlamak için aşağıdaki adımları izleyin.

1. **Uyarı şablonu** adlı bir sayfa şablonu oluşturun.
1. Varsayılan sayfanın **ana** yuvasına bir uyarı modülü ekleyin.
1. Şablonu giriş yapın ve yayımlayın. 
1. **Uyarı sayfası** adlı bir sayfa oluşturmak için yeni oluşturduğunuz uyarı şablonunu kullanın. 
1. Yeni sayfanın **ana** yuvasına bir uyarı modülü ekleyin.
1. Uyarı modülünün ayarlarında uyarı metnini girin. Uyarı modülünü daha fazla özelleştirmek istiyorsanız diğer özellikleri düzenleyebilirsiniz.
1. Sayfayı kaydet ve önizleyin. Sayfanın üst kısmında, eklediğiniz metni içeren bir uyarı görmelisiniz.
1. Sayfayı giriş yapın ve yayımlayın. 

## <a name="additional-resources"></a>Ek kaynaklar

[Başlangıç paketine genel bakış](starter-kit-overview.md)

[Döngü modülü](add-carousel.md)

[İçerik zengin blok modülü](add-content-rich-block.md)

[İçerik yerleştirme modülü](add-content-placement-modules.md)

[Özellik modülü](add-feature-module.md)

[Hero modülü](add-hero-module.md)

[Video oynatıcı modülü](add-video-player.md)
