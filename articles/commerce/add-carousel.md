---
title: Döngü modülü
description: Bu konu döngü kutusu modüllerini kapsamaktadır ve Microsoft Dynamics 365 Commerce'un site sayfalarına nasıl ekleneceğini açıklamaktadır.
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
ms.openlocfilehash: c2c5adc8ab2e0330f7b07e5153fd8332ab0203e5
ms.sourcegitcommit: 3a4e137ef3a96ba0a58c5352f4a3b57467ace9ae
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/11/2019
ms.locfileid: "2785249"
---
# <a name="carousel-module"></a>Döngü modülü

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

Bu konu döngü kutusu modüllerini kapsamaktadır ve Microsoft Dynamics 365 Commerce'un site sayfalarına nasıl ekleneceğini açıklamaktadır.

## <a name="overview"></a>Genel Bakış

Bir döngü modülü, müşterilerin gözatmasına olanak veren bir döngüde birden fazla promosyon öğesi yerleştirmek için kullanılır. Diğer modülleri barındıran özel konteyner modüldür. Örneğin, bir perakende birden fazla yeni ürün veya promosyonları sergileyebilecek bir giriş sayfasında döngü modülü kullanabilir.

Bir döngü modülü içinde Hero ve özellik modüllerini ekleyebilirsiniz. Bu şekilde, döngü modülünün özellikleri bu modüllerin nasıl işleneceğini tanımlar.

## <a name="examples-of-carousel-modules-in-e-commerce"></a>E-ticarette döngü modülleri örnekleri

- İçinde birden fazla promosyon modülü bulunan bir döngü, giriş sayfasında kullanılabilir.
- İçinde birden fazla promosyon modülü bulunan bir döngü, ürün ayrıntıları sayfasında kullanılabilir.
- Bir döngü, birden fazla promosyon veya ürünü yükseltmek için herhangi bir pazarlama sayfasında kullanılabilir.

## <a name="carousel-module-properties"></a>Döngü modülü özellikleri

| Özellik adı             | Değer                                | Tanım |
|---------------------------|--------------------------------------|-------------|
| Otomatik yürüt                  | **Doğru** veya **yanlış**                | Değer **doğru** olarak ayarlanırsa, döngü içindeki öğeler arasındaki geçiş otomatik olarak gerçekleşir. Değer **yanlış** olarak ayarlanırsa, müşteri bir maddeden bir sonraki öğeye geçmek için klavyeyi veya fareyi kullanmadıkça hiçbir geçiş gerçekleşmez. |
| Slayt geçiş aralığı | Saniye cinsinden bir değer                   | Öğeler arasındaki geçişler için Aralık. |
| Geçiş animasyonu      | **Kaydır** veya **Soldur**                | Geçiş efekti. |
| Genişlik                     | **Kapsayıcıya sığdır** veya **Ekrana doldur** | Değer **konteynere sığdır** şekilde ayarlandıysa, döngü içindeki öğeler döngünün genişliğiyle sınırlandırılır. Değer, **ekranı doldur**'a ayarlanmışsa, öğeler döngü genişliğiyle sınırlandırılmaz ancak tam ekran moduna geçebilir. İstenen düzene ulaşmak için değeri değiştirebilirsiniz. |

## <a name="add-a-carousel-module-to-a-page"></a>Sayfaya döngü modülü ekleme

Bir yeni sayfaya döngü modülü eklemek ve gerekli özellikleri ayarlamak için aşağıdaki adımları izleyin.

1. **Döngü şablonu** adlı bir sayfa şablonu oluşturun.
1. Varsayılan sayfanın **ana** yuvasına bir döngü modülü ekleyin.
1. Döngü modülüne bir Hero modülü ekleyin.
1. Döngü modülüne bir özellik modülü ekleyin.
1. Şablonu giriş yapın ve yayımlayın. 
1. **Döngü sayfası** adlı bir sayfa oluşturmak için yeni oluşturduğunuz döngü şablonunu kullanın.
1. Yeni sayfanın **ana** yuvasına bir döngü modülü ekleyin.
1. Döngü modülünün **genişlik** özelliğini **ekranı doldur** ayarlayın. 
1. **Geçiş animasyon** özelliğini **slayda**ayarlayın.
1. Döngü modülüne bir Hero modülü ekleyin.
1. Hero modülünde bir resim ve bir başlık ekleyin ve sonra da Save'i (**Kaydet**) seçin.
1. Döngü modülüne bir özellik modülü ekleyin.
1. Özellik modülünde bir resim, başlık ve bir metin paragrafı ekleyin.
1. Sayfayı kaydet ve önizleyin. Sayfa, içinde iki modül bulunan bir döngüyü göstermelidir (Hero modülü ve bir özellik modülü). İstenen etkiyi elde etmek için döngü, Hero ve özellik modüllerinin ek özelliklerini değiştirebilirsiniz.
1. Sayfayı giriş yapın ve yayımlayın.

## <a name="additional-resources"></a>Ek kaynaklar

[Başlangıç paketine genel bakış](starter-kit-overview.md)

[Uyarı modülü](add-alert.md)

[İçerik zengin blok modülü](add-content-rich-block.md)

[İçerik yerleştirme modülü](add-content-placement-modules.md)

[Özellik modülü](add-feature-module.md)

[Hero modülü](add-hero-module.md)

[Video oynatıcı modülü](add-video-player.md)
