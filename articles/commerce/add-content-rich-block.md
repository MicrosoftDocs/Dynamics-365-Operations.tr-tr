---
title: Metin bloku modülü
description: Bu konu metin bloku modüllerini kapsamaktadır ve Microsoft Dynamics 365 Commerce'un site sayfalarına nasıl ekleneceğini açıklamaktadır.
author: anupamar-ms
manager: annbe
ms.date: 01/23/2020
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
ms.openlocfilehash: fc5b2fa35633b1ce7f7ffefacec318e14fa8db3f
ms.sourcegitcommit: 829329220475ed8cff5a5db92a59dd90c22b04fa
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/05/2020
ms.locfileid: "3025609"
---
# <a name="text-block-module"></a>Metin bloku modülü


[!include [banner](includes/banner.md)]

Bu konu metin bloku modüllerini kapsamaktadır ve Microsoft Dynamics 365 Commerce'un site sayfalarına nasıl ekleneceğini açıklamaktadır.

## <a name="overview"></a>Genel Bakış

Bir metin bloğu modülü, metin içeriği eklemek için kullanılan bir modüldür. Bu içerik bilgilendirici veya promosyon olabilir.

Metin bloku modülleri, içerik yönetimi sistemindeki (CMS) veriler tarafından yönlendiriliyor ve herhangi bir sayfaya konabilir. Bunlar sayfa bağlamına veya diğer modüllere bağımlı olmayan bağımsız modüllerdir.

## <a name="examples-of-text-block-modules-in-e-commerce"></a>E-ticarette metin bloku örnekleri

Metin bloku modüller aşağıdaki yollarla kullanılabilir:

* Ürün ayrıntıları sayfasında ürün özelliklerini sergileme.
* Her sayfada yalnızca bilgi amacıyladır. Örneğin, bağlılık programlarının yararlarını açıklayabilir, Sevkiyat ve iade ilkelerini açıklayabilir, sık sorulan soruların yanıtlanması veya "Hakkımızda" içeriği sağlayabilirler.
* Ürün ayrıntıları sayfasına özel iletiler eklemek için. (örneğin, "$50 üzerinden olan siparişler için ücretsiz sevkiyat").
* Ürün Ayrıntıları sayfaları, sepet sayfaları, kullanıma alma sayfaları ve diğer sayfalar hakkında feragatler ve ilgili kişi ayrıntıları için (örneğin, "Sevkiyat ve iadeler depolama ilkelerine tabidir").

## <a name="text-block-module-properties"></a>Metin bloku modülü özellikleri

| Özellik adı     | Value                                            | Tanım |
|-------------------|--------------------------------------------------|-------------|
| Zengin metin         | Zengin metin                                        | Paragraf metni. Kalın, altı çizili, italik metin gibi bazı temel zengin metin özellikleri desteklenir. |
| Özel sınıfı adı | Geçişli stil sayfaları (CSS) sınıf adı        | Bu modülü biçimlendirmek için bir CSS geliştiricinin sağladığı özel sınıfın adı. Sınıf adı Tema paketinde tanımlanmalıdır. |
| Yazı türü boyutu         | **Küçük**, **orta**, **büyük** veya **Ekstra büyük** | İçeriğin yazı tipi boyutu. |

## <a name="add-a-text-block-module-to-a-page"></a>Bir sayfaya metin bloku modülü ekleme

Bir yeni sayfaya metin bloku modülü eklemek ve gerekli özellikleri ayarlamak için aşağıdaki adımları izleyin.

1. **İçerik şablonu** adlı bir sayfa şablonu oluşturun. 
1. **Gövde** yuvasında bir **Varsayılan sayfa** modülü ekleyin.
1. Şablon düzenlemeyi tamamlayın ve sonra yayımlayın.
1. **İçerik sayfası** adlı bir sayfa oluşturmak için yeni oluşturduğunuz içerik şablonunu kullanın.
1. Yeni sayfanın **ana** yuvasına bir konteyner modülü ekleyin.
1. Konteyner modülü için özellik panosunda **Genişlik** özelliğini **Konteyneri doldur**'a ayarlayın.
1. Kapsayıcı modülüne bir metin bloku modülü ekleyin. 
1. Metin bloku modülünün özellik panosunda, **Zengin metin** alanına bir metin ekleyin.
1. Sayfayı düzenlemeyi tamamlayın ve sonra yayımlayın.

## <a name="additional-resources"></a>Ek kaynaklar

[Başlangıç paketine genel bakış](starter-kit-overview.md)

[Promosyon başlık modülü](add-alert.md)

[Döngü modülü](add-carousel.md)

[İçerik blok modülü](add-hero-module.md)

[Video oynatıcı modülü](add-video-player.md)

