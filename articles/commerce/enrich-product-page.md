---
title: Ürün sayfasını zenginleştirme
description: Bu konuda, Microsoft Dynamics 365 Commerce'te ürün sayfası zenginleştirme yöntemi açıklanmıştır .
author: psimolin
manager: annbe
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: d9c0f329d21cdda5c36a39a8c602d5925b720f52
ms.sourcegitcommit: ef3a1d7527311d00b69a1072ae5eb021ce68034c
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/09/2020
ms.locfileid: "2945755"
---
# <a name="enrich-a-product-page"></a>Ürün sayfasını zenginleştirme

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

Bu konuda, Microsoft Dynamics 365 Commerce'te ürün sayfası zenginleştirme yöntemi açıklanmıştır .

## <a name="overview"></a>Genel Bakış

Varsayılan olarak, siteniz ürün verilerini göstermek için genel bir sayfa kullanır. Bu sayfa, ürünle ilgili temel bilgileri ve bunu satmak için gerekli olan denetimleri içerir. Ancak, perakende sunucusundan belirli bir ürünle ilgili ek resim veya metinle gelen bilgileri ekleyebilirsiniz. Bu işleme, ürün sayfasını zenginleştirme adı verilir.

Birçok durumda, ürünleriniz için özel ek içerik kullanmak isteyeceksiniz. Geliştirme aracında **perakende**'e gittiğinizde, bu siteye atanan kanaldan bir ürün listesi göreceksiniz. Bu listede, **zenginleştirilmiş** sütun, bir ürünle ilgili ürün sayfasının zenginleştirilmiş olduğunu gösterir. Sütunda bir onay işareti görünürse, ürün için zenginleştirilmiş bir ürün sayfası bulunur. Onay işareti görüntülenmezse, ürün için varsayılan ürün sayfası ve içerik kullanılır. Listeden ürün adını seçerek, bir kategori için hem zenginleştirilmiş hem de zenginleştirilmemiş ürün sayfalarını önizleyebilirsiniz.

## <a name="enrich-a-product-page"></a>Ürün sayfasını zenginleştirme

Ürün sayfasını zenginleştirmek için aşağıdaki adımları izleyin.

1. **Siteler** altında, **Fabrikam**'ı seçin (veya sitenizin adını).
1. Soldaki gezinti bölmesinde **Ürünler** seçin.
1. Zenginleştirilmiş ürün sayfasına sahip olmayan herhangi bir ürünü seçin.
1. Eylem Bölmesinde, **Ürün sayfasını zenginleştir**'i seçin.
1. **PDP şablonu**'nu seçin ve sonra **Tamam**'i seçin.
1. Soldaki sayfa anahat ağacında **ana** yuvayı genişletin.
1. **Ana** yuvası için üç nokta (**...**) düğmesini seçin ve **Modül ekle**'yi seçin.
1. **Konteyner 2**'i seçin ve sonra **Tamam**'i seçin.
1. **konteyner 2** seçin, üç nokta düğmesini seçin ve sonra **Modül ekle**'yi seçin.
1. **Özellik**'i seçin ve sonra **Tamam**'i seçin.
1. Sağdaki Özellikler bölmesinde, **zengin metin** alanına ürünün güncelleştirilmiş açıklamasını girin.
1. **Başlık** alanına başlık metnini girin ve **Tamam**'ı seçin.
1. **Kaydet**i seçin ve sonra **Giriş**'i seçin.
1. **Yorumlar** alanında **Zenginleştirilmiş ürün** seçeneğini girin ve **Tamam**'ı seçin.
1. Zenginleştirilmiş ürün sayfasını önizlemek için **Önizleme** 'yi seçin . Bitirdiğinizde, geliştirme aracına dönmek için Önizleme sekmesini kapatın.
1. **Yayımla**'yı seçin.

## <a name="additional-resources"></a>Ek kaynaklar

[Var olan site sayfasını değiştirme](modify-existing-page.md)

[Yeni site sayfası ekleme](add-new-page.md)

[Sayfa düzeni seçme](select-page-layouts.md)

[SEO meta verilerini yönetme](manage-seo-metadata.md)

[Sayfa kaydetme, önizleme ve yayımlama](save-preview-publish-page.md)

[Kategori açılış sayfasını zenginleştirme](enrich-category-page.md)

[Sayfa içeriği erişilebilirliğini doğrula](verify-accessibility.md)
