---
title: Kategori açılış sayfasını zenginleştirme
description: Bu konu, Dynamics 365 Commerce'deki kategori sayfalarının zenginini kapsamaktadır.
author: v-chgri
ms.date: 04/14/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: asharchw
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 5bb28c3b5fbb1133d32219b9c47dd1477ae2ac982ee035321dafd77c53dc910b
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/05/2021
ms.locfileid: "6771019"
---
# <a name="enrich-a-category-landing-page"></a>Kategori açılış sayfasını zenginleştirme

[!include [banner](includes/banner.md)]

Bu konu, Dynamics 365 Commerce'deki kategori sayfalarının zenginini kapsamaktadır.

Commerce, kategori verileri gösterildiğinde kullanılan varsayılan bir kategori iniş sayfası sağlar. Varsayılan bir kategori sayfası, iyileştiriciler, kategori oluşturma, sıralama seçenekleri, seçim Özeti ve sayfalandırma denetimleri gibi gerekli öğeleri içerir. 

Ancak, varsayılan kategori sayfasını kullanmak yerine, daha fazla içeriğe ve daha belirli öğelere sahip bir "zenginleştirilmiş" Kategori iniş sayfası kullanmak isteyebilirsiniz. Tipik bir zenginleştirme kategori sayfasına özel pazarlama içeriği eklenmesini gerektirebilir. Bu içerik, çapraz satış amaçları, düzenleme listeleri, resimler, videolar ve diğer metinler için çapraz kategori ürün yerleştirmesi içerebilir. Varsayılan kategori sayfasını değiştirebilir veya belirli bir kategori için farklı bir kategori sayfası tanımlayabilirsiniz.

![Zenginleştirilmiş kategori açılış sayfası.](./media/CategoryLandingPages.png)

Commerce site oluşturucuda **Ürünler** sayfası, siteye atanan kanaldaki kategorilerin listesini içerir. Bir kategori sayfası için **zenginleştirilmiş** durum seçildiyse, bu kategori sayfası zenginleştirgeçer. Aksi durumda, kategori için varsayılan kategori sayfası ve içerik kullanılır. Kategori adını seçerek, bir kategori için hem zenginleştirilmiş hem de zenginleştirilmemiş kategori sayfalarını önizleyebilirsiniz.

Bir kategori sayfasını zenginleştirmek için, aşağıdakileri yapın.

1. **Ürünler** sayfasında, kategori sayfasını zenginleştirmek istediğiniz kategorinin adını seçin. Seçili Kategori için varsayılan kategori sayfası düzenleyicisinde açılır.
2. **Kategori sayfasını zenginleştir**'i seçin.
3. Zenginleştirilmiş kategori sayfası için bir şablon seçin. Yalnızca küçük değişiklikler yapıyorsanız, varsayılan kategori sayfasını seçebilirsiniz. Alternatif olarak, belirli bir kategori sayfası şablonu da seçebilirsiniz. Şablonu seçtiğinizde, sayfa Düzenleyicisi açılır ve seçili şablon seçili kategori için yeni bir kategori sayfası oluşturmak için kullanılır. Sayfa kullanımınıza alındı ve şimdi değişikliklerinizi yapabilirsiniz.

> [!NOTE]
> Kategori belirtim verileri kullanan modüller seçtiğiniz kategorideki verileri kullanır. Seçtiğiniz şablonun ayarları yapabileceğiniz değişiklikleri belirler.

## <a name="additional-resources"></a>Ek kaynaklar

[Var olan site sayfasını değiştirme](modify-existing-page.md)

[Yeni site sayfası ekleme](add-new-page.md)

[Sayfa düzeni seçme](select-page-layouts.md)

[SEO meta verilerini yönetme](manage-seo-metadata.md)

[Sayfa kaydetme, önizleme ve yayımlama](save-preview-publish-page.md)

[Ürün sayfasını zenginleştirme](enrich-product-page.md)

[Sayfa içeriği erişilebilirliğini doğrulama](verify-accessibility.md)

[URL parametrelerini temel alan dinamik e-ticaret sayfaları oluşturma](create-dynamic-pages.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
