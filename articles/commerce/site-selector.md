---
title: Site seçicisi modülü
description: Bu konu site seçicisi modüllerini kapsamaktadır ve Microsoft Dynamics 365 Commerce'in site sayfalarına nasıl ekleneceğini açıklamaktadır.
author: anupamar-ms
ms.date: 02/11/2022
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
ms.openlocfilehash: 381163fdd6180a76def2e1bfb733f597b611c517
ms.sourcegitcommit: 3105642fca2392edef574b60b4748a82cda0a386
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/12/2022
ms.locfileid: "8109718"
---
# <a name="site-picker-module"></a>Site seçicisi modülü

[!include [banner](includes/banner.md)]

Bu konu site seçicisi modüllerini kapsamaktadır ve Microsoft Dynamics 365 Commerce'in site sayfalarına nasıl ekleneceğini açıklamaktadır.

Bir işletme, pazarlar, bölgeler ve konumlarda farklı sitelere sahip olduğunda, site kullanıcıları siteler arasında geçiş yapmak ve tercih edilen alışveriş sitesini seçmek için kolay bir yola gereksinim duyar. Bu senaryoya uyum sağlamak için, site seçicisi modülü kullanıcıların birden çok siteye göz atmasına olanak tanır.

Site seçicisi modülü site kullanıcılarının göz atabileceği siteler listesi (pazarlar, bölgeler veya konumlar) ile konfigüre edilmelidir.

> [!NOTE]
> Site seçicisi modülü Dynamics 365 Commerce 10.0.14 sürümünde bulunur.

Aşağıdaki çizimde site sayfası üstbilgisinde tanıtılan bir site seçicisi modülü örneği gösterilmektedir.

![Site sayfası üst bilgisindeki bir site seçicisi modülü örneği.](./media/ecommerce-sitepicker.PNG)

## <a name="site-picker-module-properties"></a>Site seçicisi modülü özellikleri

| Özellik adı | Değer                 | Açıklama |
|---------------|-----------------------|-------------|
| Başlık       | Metin                  | Modülün başlığı. |
| Site seçenekleri  | Ad, resim, URL      | Bu özellik, bir ad, sitenin giriş sayfası bağlantısı ve modüldeki her site için gösterilecek isteğe bağlı bir resim belirtir. Resim bir bayrak veya bir pazar, bölge veya konumun herhangi bir temsili olabilir. |

## <a name="add-a-site-picker-module-to-a-page"></a>Bir sayfaya site seçicisi modülü ekleme

Site seçicisi modülü, **Site seçicisi** yuvasının altındaki [üst bilgi modülüne](author-header-module.md) eklenebilir. Site seçicisi modülü eklendikten sonra, modül üst bilgisini ve site seçeneklerini tanımlayabilirsiniz. Genel olarak, bir üst bilgi modülü bir sitenin e-ticaret sayfalarında paylaşılabilecek bir üst bilgi parçasında bulunur. Aşağıdaki örnekte, site seçicisi modülü **HeaderContainer adlı**  adlı üstbilgi parçasında bulunan bir üstbilgi modülünün **Site seçicisi** yuvasına eklenmiştir.

![Üst bilgi parçasındakş bir site seçicisi modülü örneği.](./media/ecommerce-sitepicker-2.png)

## <a name="additional-resources"></a>Ek kaynaklar

[Modül kitaplığına genel bakış](starter-kit-overview.md)

[Üst bilgi modülü](author-header-module.md)

[İçerik haritası modülü](add-breadcrumb.md)

[Gezinti menüsü modülü](nav-menu-module.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
