---
title: İçerik zengin blok modülü
description: Bu konu içerik zengin blok modüllerini kapsamaktadır ve Microsoft Dynamics 365 Commerce'un site sayfalarına nasıl ekleneceğini açıklamaktadır.
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
ms.openlocfilehash: 27dabb425b3c9a3015ffc54ff3c0e50b7ee11749
ms.sourcegitcommit: 3a4e137ef3a96ba0a58c5352f4a3b57467ace9ae
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/11/2019
ms.locfileid: "2785433"
---
# <a name="content-rich-block-module"></a>İçerik zengin blok modülü

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

Bu konu içerik zengin blok modüllerini kapsamaktadır ve Microsoft Dynamics 365 Commerce'un site sayfalarına nasıl ekleneceğini açıklamaktadır.

## <a name="overview"></a>Genel Bakış

İçerik zengin blok modülü, bir veya daha fazla içerik zengin blok öğenin içine koyulacağı özel bir konteynerdir. İçerik zengin blok modülleri, bir sayfadaki metin içeriği için kullanılır. Bu içerik bilgilendirici veya promosyon olabilir.

İçerik zengin blok modülleri, içerik yönetimi sistemindeki (CMS) veriler tarafından yönlendiriliyor ve herhangi bir sayfaya konabilir. Bunlar sayfa bağlamına veya diğer modüllere bağımlı olmayan bağımsız modüllerdir.

## <a name="examples-of-content-rich-block-modules-in-e-commerce"></a>E-ticarette içerik zengin blok modülleri örnekleri

İçerik zengin blok modüller aşağıdaki yollarla kullanılabilir:

* Ürün ayrıntıları sayfasında ürün özelliklerini sergileme.
* Her sayfada yalnızca bilgi amacıyladır. Örneğin, bağlılık programlarının yararlarını açıklayabilir, Sevkiyat ve iade ilkelerini açıklayabilir, sık sorulan soruların yanıtlanması veya "Hakkımızda" içeriği sağlayabilirler.
* Ürün ayrıntıları sayfasına özel iletiler eklemek için. (örneğin, "$50 üzerinden olan siparişler için ücretsiz sevkiyat").
* Ürün Ayrıntıları sayfaları, sepet sayfaları, kullanıma alma sayfaları ve diğer sayfalar hakkında feragatler ve ilgili kişi ayrıntıları için (örneğin, "Sevkiyat ve iadeler depolama ilkelerine tabidir").

## <a name="content-rich-block-module-properties"></a>İçerik zengin blok modülü özellikleri

| Özellik adı     | Değer                                 | Özellik |
|-------------------|---------------------------------------|----------|
| Sütun sayısı | **1** ile **4** arasında bir sayı     | İçerik zengin bloğundaki sütunların sayısı. En çok dört sütun olabilir. |
| Genişlik             | **Kapsayıcıya sığdır** veya **Ekrana doldur** | Değer **konteynere doldur** şekilde ayarlandıysa, konteyner içindeki öğeler konteyner genişliğiyle sınırlandırılır. Değer, **ekranı doldur**'a ayarlanmışsa, öğeler konteyner genişliğiyle sınırlandırılmaz ancak tam ekran moduna geçebilir. İstenen düzene ulaşmak için değeri değiştirebilirsiniz. |

## <a name="content-rich-block-item-module-properties"></a>İçerik zengin blok öğesi modülü özellikleri

| Özellik adı | Değer          | Tanım |
|---------------|----------------|-------------|
| Paragraf     | Paragraf metni | Her içerik zengin blok öğesine eşlik eden metin. Kalın, altı çizili, italik metin gibi bazı temel zengin metin özellikleri desteklenir. |

## <a name="add-a-content-rich-block-module-to-a-page"></a>Sayfaya içerik zengin blok modülü ekleme

Bir yeni sayfaya içerik zengin blok modülü eklemek ve gerekli özellikleri ayarlamak için aşağıdaki adımları izleyin.

1. **İçerik şablonu** adlı bir sayfa şablonu oluşturun.
1. Varsayılan sayfanın **ana** yuvasına bir içerik zengin blok modülü ekleyin.
1. Şablonu giriş yapın ve yayımlayın.
1. **İçerik sayfası** adlı bir sayfa oluşturmak için yeni oluşturduğunuz içerik şablonunu kullanın.
1. Yeni sayfanın **ana** yuvasına bir içerik zengin blok modülü ekleyin.
1. İçerik zengin blok modülünün özelliklerinde, sütun sayısını **2** olarak ayarlayın.
1. İçerik zengin blok modülünde **modül ekle**'yi seçin ve içerik zengin blok bir öğe ekleyin (örneğin, **item1**).
1. Yeni içerik zengin blok öğesinde paragraf metni ekleyin.
1. İçerik zengin blok modülünde **modül ekle**'yi seçin ve içerik zengin blok bir öğe ekleyin (örneğin, **item2**).
1. Yeni içerik zengin blok öğesinde paragraf metni ekleyin.
1. Sayfayı kaydedin ve değişiklikleri önizleyin. İki sütunlu görünümde iki zengin metin bloğu görmelisiniz.
1. Sayfayı giriş yapın ve yayımlayın.

> [!NOTE]
> Üçüncü içerikli bir zengin blok öğesi eklerseniz, bu öğe daha önce eklediğiniz iki öğenin altına yığılır. Konteynerdeki sütunların ve öğelerin sayısını değiştirerek metin içeriği için farklı düzenler elde edebilirsiniz.

## <a name="additional-resources"></a>Ek kaynaklar

[Başlangıç paketine genel bakış](starter-kit-overview.md)

[Uyarı modülü](add-alert.md)

[Döngü modülü](add-carousel.md)

[İçerik yerleştirme modülü](add-content-placement-modules.md)

[Özellik modülü](add-feature-module.md)

[Hero modülü](add-hero-module.md)

[Video oynatıcı modülü](add-video-player.md)

