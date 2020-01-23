---
title: Kategori açılış sayfasını zenginleştirme
description: Bu konu, Dynamics 365 Commerce'deki kategori sayfalarının zenginini kapsamaktadır.
author: v-chgri
manager: annbe
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Operations, Retail, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: asharchw
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 4ab152dff0925f9c816419083577b5272ac813be
ms.sourcegitcommit: ef3a1d7527311d00b69a1072ae5eb021ce68034c
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/09/2020
ms.locfileid: "2945801"
---
# <a name="enrich-a-category-landing-page"></a>Kategori açılış sayfasını zenginleştirme

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

Bu konu, Dynamics 365 Commerce'deki kategori sayfalarının zenginini kapsamaktadır.

## <a name="overview"></a>Genel Bakış

Commerce, kategori verileri gösterildiğinde kullanılan varsayılan bir kategori iniş sayfası sağlar. Varsayılan bir kategori sayfası, iyileştiriciler, kategori oluşturma, sıralama seçenekleri, seçim Özeti ve sayfalandırma denetimleri gibi gerekli öğeleri içerir. 

Ancak, varsayılan kategori sayfasını kullanmak yerine, daha fazla içeriğe ve daha belirli öğelere sahip bir "zenginleştirilmiş" Kategori iniş sayfası kullanmak isteyebilirsiniz. Tipik bir zenginleştirme kategori sayfasına özel pazarlama içeriği eklenmesini gerektirebilir. Bu içerik, çapraz satış amaçları, düzenleme listeleri, resimler, videolar ve diğer metinler için çapraz kategori ürün yerleştirmesi içerebilir. Varsayılan kategori sayfasını değiştirebilir veya belirli bir kategori için farklı bir kategori sayfası tanımlayabilirsiniz.

![Zenginleştirilmiş kategori açılış sayfası](./media/CategoryLandingPages.png)

Geliştirme aracında, **ürün** sayfası, siteye atanan kanaldan bir kategori listesi içerir. Bir kategori sayfası için **zenginleştirilmiş** durum seçildiyse, bu kategori sayfası zenginleştirgeçer. Aksi durumda, kategori için varsayılan kategori sayfası ve içerik kullanılır. Kategori adını seçerek, bir kategori için hem zenginleştirilmiş hem de zenginleştirilmemiş kategori sayfalarını önizleyebilirsiniz.

Bir kategori sayfasını zenginleştirmek için, aşağıdakileri yapın.

1. **Ürünler** sayfasında, kategori sayfasını zenginleştirmek istediğiniz kategorinin adını seçin. Seçili Kategori için varsayılan kategori sayfası düzenleyicisinde açılır.
2. **Kategori sayfasını zenginleştir**'i seçin.
3. Zenginleştirilmiş kategori sayfası için bir şablon seçin. Yalnızca küçük değişiklikler yapıyorsanız, varsayılan kategori sayfasını seçebilirsiniz. Alternatif olarak, belirli bir kategori sayfası şablonu da seçebilirsiniz. Şablonu seçtiğinizde, sayfa Düzenleyicisi açılır ve seçili şablon seçili kategori için yeni bir kategori sayfası oluşturmak için kullanılır. Sayfa kullanımınıza alındı ve şimdi değişikliklerinizi yapabilirsiniz.

> [!NOTE]
> Kategori belirtim verileri kullanan modüller seçtiğiniz kategorideki verileri kullanır.
>
> Seçtiğiniz şablonun ayarları yapabileceğiniz değişiklikleri belirler.

## <a name="additional-resources"></a>Ek kaynaklar

[Var olan site sayfasını değiştirme](modify-existing-page.md)

[Yeni site sayfası ekleme](add-new-page.md)

[Sayfa düzeni seçme](select-page-layouts.md)

[SEO meta verilerini yönetme](manage-seo-metadata.md)

[Sayfa kaydetme, önizleme ve yayımlama](save-preview-publish-page.md)

[Ürün sayfasını zenginleştirme](enrich-product-page.md)

[Sayfa içeriği erişilebilirliğini doğrula](verify-accessibility.md)
