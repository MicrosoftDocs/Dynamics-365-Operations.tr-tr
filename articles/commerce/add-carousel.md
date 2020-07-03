---
title: Döngü modülü
description: Bu konu döngü kutusu modüllerini kapsamaktadır ve Microsoft Dynamics 365 Commerce'un site sayfalarına nasıl ekleneceğini açıklamaktadır.
author: anupamar-ms
manager: annbe
ms.date: 05/28/2020
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
ms.openlocfilehash: 35aaf35419a8c5b83b2a3e1136a02200bf347c6b
ms.sourcegitcommit: b52477b7d0d52102a7ca2fb95f4ebfa30ecd9f54
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/29/2020
ms.locfileid: "3411308"
---
# <a name="carousel-module"></a>Döngü modülü

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

Bu konu döngü kutusu modüllerini kapsamaktadır ve Microsoft Dynamics 365 Commerce'un site sayfalarına nasıl ekleneceğini açıklamaktadır.

## <a name="overview"></a>Genel Bakış

Bir döngü modülü, müşterilerin gözatmasına olanak veren bir döner döngüde birden fazla promosyon öğesini (zengin görseller dahil) yerleştirmek için kullanılır. Örneğin, bir perakende birden fazla yeni ürün veya promosyonları sergileyebilecek bir giriş sayfasında döngü modülü kullanabilir.

Bir içerik bloku modülünü bir döngü modülüne ekleyebilirsiniz. Bu şekilde, döngü modülünün özellikleri bu modüllerin nasıl işleneceğini tanımlar.

## <a name="examples-of-carousel-modules-in-e-commerce"></a>E-ticarette döngü modülleri örnekleri

- İçinde birden fazla promosyon modülü bulunan bir döngü, giriş sayfasında kullanılabilir.
- İçinde birden fazla promosyon modülü bulunan bir döngü, ürün ayrıntıları sayfasında kullanılabilir.
- Bir döngü, birden fazla promosyon veya ürünü yükseltmek için herhangi bir pazarlama sayfasında kullanılabilir.

Aşağıdaki resimde giriş sayfasında kullanılan bir döngü modülü örneği gösterilmektedir. Bu döngü modülü birden çok içerik bloğu öğesi içeriyor.

![Döngü modülü örneği](./media/Hero.PNG)

## <a name="carousel-module-properties"></a>Döngü modülü özellikleri

| Özellik adı             | Değer                 | Tanım |
|---------------------------|-----------------------|-------------|
| Otomatik yürüt                  | **Doğru** veya **yanlış** | Değer **doğru** olarak ayarlanırsa, döngü içindeki öğeler arasındaki geçiş otomatik olarak gerçekleşir. Değer **yanlış** olarak ayarlanırsa, müşteri bir maddeden bir sonraki öğeye geçmek için klavyeyi veya fareyi kullanmadıkça hiçbir geçiş gerçekleşmez. |
| Slayt geçiş aralığı | Saniye cinsinden bir değer    | Öğeler arasındaki geçişler için Aralık. |
| Geçiş türü           | **Kaydır** veya **Soldur** | Öğeler arasındaki geçiş efekti. |
| Döngü yüzgecini gizle     | **Doğru** veya **yanlış** | Değer **Doğru** olarak ayarlanmışsa, döngü değiştirici ve sekans göstergesi saklanır. |
| Döngü kapatmaya izin ver    | **Doğru** veya **yanlış** | Değer **Doğru** olarak ayarlandıysa, kullanıcılar döngüyü kapatabilir. |

## <a name="add-a-carousel-module-to-a-page"></a>Sayfaya döngü modülü ekleme

Bir yeni sayfaya döngü modülü eklemek ve gerekli özellikleri ayarlamak için aşağıdaki adımları izleyin.

1. Bir yeni şablonu oluşturmak için **Şablonlar**'a gidin ve **Yeni**'yi seçin.
1. **Yeni Şablon** iletişim kutusunda **Şablon adı** altında, **Döngü şablonu**'nu girin ve **Tamam**'ı seçin.
1. **Gövde** yuvasında bir **Varsayılan sayfa** modülü ekleyin.
1. Şablonu iade etmek için **Düzenlemeyi bitir**'i seçin, ardından yayımlamak için **Yayımla**'yı seçin.  
1. **Döngü sayfası** adlı bir sayfa oluşturmak için yeni oluşturduğunuz döngü şablonunu kullanın.
1. Yeni sayfanın **ana** yuvasına bir konteyner modülü ekleyin. 
1. Sağdaki panoda, **Genişlik** değerini **Ekranı doldur**'a ayarlayın.
1. **Sayfa Anahattı** altında, bir döngü modlünü konteyner modülüne ekleyin.
1. Döngü modülüne bir içerik bloku modülü ekle. **Başlık**, **bağlantı**, **yerleşim** ve diğer özellikleri sağlayarak içerik bloğu modülünün özelliklerini ayarlayın.
1. Başka bir içerik bloğu modülü ekleyin ve konfigüre edin.
1. Döngü Modülü için gerekli olan ek özellikleri ayarlayın.
1. **Kaydet**'i seçin ve ardından sayfayı önizlemek için **Önizleme**'yi seçin. Sayfa, içinde iki modül bulunan bir döngüyü göstermelidir (Hero modülü ve bir özellik modülü). İstenen etkiyi elde etmek için döngü, Hero ve özellik modüllerinin ek özelliklerini değiştirebilirsiniz.
1. Sayfayı iade etmek için **Düzenlemeyi bitir**'i seçin, ardından yayımlamak için **Yayımla**'yı seçin.

## <a name="additional-resources"></a>Ek kaynaklar

[Başlangıç paketine genel bakış](starter-kit-overview.md)

[Promosyon başlığı modülü](add-alert.md)

[Metin bloku modülü](add-content-rich-block.md)

[İçerik blok modülü](add-hero-module.md)

[Video oynatıcı modülü](add-video-player.md)
