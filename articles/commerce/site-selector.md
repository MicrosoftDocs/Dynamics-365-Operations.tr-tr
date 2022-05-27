---
title: Site seçicisi modülü
description: Bu konu site seçicisi modüllerini kapsamaktadır ve Microsoft Dynamics 365 Commerce'in site sayfalarına nasıl ekleneceğini açıklamaktadır.
author: anupamar-ms
ms.date: 05/04/2022
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
ms.openlocfilehash: a1954f6b2fea35d5138218e6a2a23ab1fd04c8fc
ms.sourcegitcommit: 04e6c1c9400e1b582180cf3e0e4767434e736c26
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/05/2022
ms.locfileid: "8710316"
---
# <a name="site-picker-module"></a>Site seçicisi modülü

[!include [banner](includes/banner.md)]

Bu konu site seçicisi modüllerini kapsamaktadır ve Microsoft Dynamics 365 Commerce'in site sayfalarına nasıl ekleneceğini açıklamaktadır.

Bir işletme, pazarlar, bölgeler ve konumlarda farklı sitelere sahip olduğunda, site kullanıcıları siteler arasında geçiş yapmak ve tercih edilen alışveriş sitesini seçmek için kolay bir yola gereksinim duyar. Bu senaryoya uyum sağlamak için, site seçicisi modülü kullanıcıların birden çok siteye göz atmasına olanak tanır. E-ticaret siteniz için [coğrafi konum algılama ve yeniden yönlendirme](geo-detection-redirection.md) uygulandığında bir site seçici de önerilir, böylece müşteriler [ülke/bölge seçici](country-region-picker-module.md) modülünü kullanarak belirttikleri site tercihini geçersiz kılmanın bir yoluna sahip olur. 

Site seçicisi modülü site kullanıcılarının göz atabileceği siteler listesi (pazarlar, bölgeler veya konumlar) ile konfigüre edilmelidir. Aşağıdaki çizimde site sayfası üstbilgisinde tanıtılan bir site seçicisi modülü örneği gösterilmektedir.

![Site sayfası üst bilgisindeki bir site seçicisi modülü örneği.](./media/ecommerce-sitepicker.PNG)

## <a name="site-picker-module-properties"></a>Site seçicisi modülü özellikleri

| Özellik adı | Değer                 | Açıklama |
|---------------|-----------------------|-------------|
| Başlık       | Metin                  | Modülün başlığı. |
| Site seçenekleri  | Ad, resim, URL      | Bu özellik, bir ad, sitenin giriş sayfası bağlantısı ve modüldeki her site için gösterilecek isteğe bağlı bir resim belirtir. Resim bir bayrak veya bir pazar, bölge veya konumun herhangi bir temsili olabilir. |

## <a name="add-a-site-picker-module-to-a-page"></a>Bir sayfaya site seçicisi modülü ekleme

Site seçicisi modülü, **Site seçicisi** yuvasının altındaki [üst bilgi modülüne](author-header-module.md) eklenebilir. Site seçicisi modülü eklendikten sonra, modül üst bilgisini ve site seçeneklerini tanımlayabilirsiniz. Genel olarak, bir üst bilgi modülü bir sitenin e-ticaret sayfalarında paylaşılabilecek bir üst bilgi parçasında bulunur. 

Üst bilgi modülüne site seçici modülü eklemek için aşağıdaki adımları izleyin.

1. Üst bilgi parçasının üst bilgi modülünü içeren **Site seçici** yuvasında üç noktayı (**...**) seçin ve sonra **Modül Ekle**'yi seçin.
1. **Modül seç** iletişim kutusunda bir **Site seçici** modülü ekleyin ve **Tamam**'ı seçin.
1. **Site seçici** özellikleri bölmesinde, **Site seçenekleri listesi ekle**'yi seçin. Düzenlenebilir **Site seçenekleri listesi** seçeneği görüntülenir.
1. **Site seçenekleri listesi**'ni seçin. **Site seçenekleri listesi** iletişim kutusu görüntülenir.
1. **Site adı** altında, site seçici açılır listesinde gösterilecek site adı metnini girin.
1. **Site yeniden yönlendirme URL'si** altında **Bağlantı ekle**'yi seçin. **Bağlantı ekle** açılır bölmesi görünür.
1. **Bağlantı ekle** açılır bölmesinde **Özel sayfa**'yı seçin ve sonra **İleri**'yi seçin.
1. Site URL'si listesinden, kanalı siteye eklerken oluşturduğunuz yolun bulunduğu URL'yi (örneğin, `www.adventure-works.com/fr-ca`) seçin ve **Uygula**'yı seçin.
1. **Tamam**'ı seçin.
1. **Kaydet** i seçin ve sonra **Düzenlemeyi bitir**'i seçin.
1. Sayfayı yayımlamak için **Yayımla**'yı seçin.

Aşağıdaki örnekte, site seçicisi modülü **HeaderContainer adlı**  adlı üstbilgi parçasında bulunan bir üstbilgi modülünün **Site seçicisi** yuvasına eklenmiştir.

![Üst bilgi parçasındakş bir site seçicisi modülü örneği.](./media/ecommerce-sitepicker-2.png)

## <a name="additional-resources"></a>Ek kaynaklar

[Modül kitaplığına genel bakış](starter-kit-overview.md)

[Üst bilgi modülü](author-header-module.md)

[İçerik haritası modülü](add-breadcrumb.md)

[Gezinti menüsü modülü](nav-menu-module.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
