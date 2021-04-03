---
title: Site seçicisi modülü
description: Bu konu site seçici modüllerini kapsamaktadır ve Microsoft Dynamics 365 Commerce'in site sayfalarına nasıl ekleneceğini açıklamaktadır.
author: anupamar-ms
manager: annbe
ms.date: 10/20/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
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
ms.openlocfilehash: e24590d4a8f172809704aab0d761f6db0fb0e11b
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5234353"
---
# <a name="site-selector-module"></a>Site seçicisi modülü

[!include [banner](includes/banner.md)]

Bu konu site seçici modüllerini kapsamaktadır ve Microsoft Dynamics 365 Commerce'in site sayfalarına nasıl ekleneceğini açıklamaktadır.

Bir işletme, pazarlar, bölgeler ve konumlarda farklı sitelere sahip olduğunda, site kullanıcıları siteler arasında geçiş yapmak ve tercih edilen alışveriş sitesini seçmek için kolay bir yola gereksinim duyar. Bu senaryoya uyum sağlamak için, site seçici modülü kullanıcıların birden çok siteye göz atmasına olanak tanır.

Site seçici modülü site kullanıcılarının göz atabileceği siteler listesi (pazarlar, bölgeler veya konumlar) ile konfigüre edilmelidir.

> [!NOTE]
> Site seçici modülü Dynamics 365 Commerce 10.0.14 sürümünde bulunur.

Aşağıdaki çizimde site sayfası üstbilgisinde tanıtılan bir site seçici modülü örneği gösterilmektedir.

![Site sayfası üst bilgisindeki bir site seçici modülü örneği](./media/ecommerce-sitepicker.PNG)

## <a name="site-selector-module-properties"></a>Site seçicisi modülü özellikleri

| Özellik adı | Değer                 | Tanım |
|---------------|-----------------------|-------------|
| Başlık       | Metin                  | Modülün başlığı. |
| Site seçenekleri  | Ad, resim, URL      | Bu özellik, bir ad, sitenin giriş sayfası bağlantısı ve modüldeki her site için gösterilecek isteğe bağlı bir resim belirtir. Resim bir bayrak veya bir pazar, bölge veya konumun herhangi bir temsili olabilir. |

## <a name="add-a-site-selector-module-to-a-page"></a>Bir sayfaya site seçici modülü ekleme

Site seçici modülü, site seçici yuvasının altındaki [üst bilgi modülüne](author-header-module.md) eklenebilir. Eklendikten sonra, modül üst bilgisini ve site seçeneklerini tanımlayabilirsiniz.

## <a name="additional-resources"></a>Ek kaynaklar

[Modül kitaplığına genel bakış](starter-kit-overview.md)

[Üst bilgi modülü](author-header-module.md)

[İçerik haritası modülü](add-breadcrumb.md)

[Gezinti menüsü modülü](nav-menu-module.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]