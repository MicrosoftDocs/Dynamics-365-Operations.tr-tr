---
title: Yeni site sayfası ekleme
description: Bu konuda, Microsoft Dynamics 365 Commerce'e yeni bir site sayfası ekleme yöntemi açıklanmıştır .
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
ms.openlocfilehash: 1993e58108ad73aad4adf382bb03ec2e62231add
ms.sourcegitcommit: ef3a1d7527311d00b69a1072ae5eb021ce68034c
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/09/2020
ms.locfileid: "2945617"
---
# <a name="add-a-new-site-page"></a>Yeni site sayfası ekleme

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

Bu konuda, Microsoft Dynamics 365 Commerce'e yeni bir site sayfası ekleme yöntemi açıklanmıştır .

## <a name="overview"></a>Genel Bakış

Siteniz için şablonlar ve parçalar oluşturduktan sonraki adım bunları kullanan sayfalar oluşturmaya başlamak içindir. Başlamak için, bir şablon veya düzen, bir sayfa adı ve bir sayfa URL'si seçmelisiniz.

## <a name="template-or-layout"></a>Şablon veya düzen

Yeni sayfanız için bir şablon ya da Düzen kullanabilirsiniz. Daha fazla bilgi için bkz. [Şablonlar ve düzenlere genel bakış](templates-layouts-overview.md).

## <a name="page-name"></a>Sayfa adı

Sayfa adı sayfanız için benzersiz olmalıdır. Açıklayıcı olmalıdır, böylece kolayca bulabilmeniz için ve sayfanın ne için amaçlandığı hakkında diğer kişileri de bulabilirsiniz. Sayfa adını daha sonra değiştirilemediğinden, dikkatlice seçin.

## <a name="page-url"></a>Sayfa URL'si

Yeni sayfanız için bir URL girme seçeneğiniz olabilir. Sayfa oluşturduğunuzda, tam bir URL oluşturmak için kullanılacak bir dize girebilirsiniz. Bu dize göreli bir URL veya URL bilgi olarak bilinir. URL bilgisinin temel alınarak tam bir URL oluşturulur ve yeni sayfa buna atanır. Sayfayı yayımlamadan önce URL başlık bilgisinin değiştirilmesini sağlayabilirsiniz. Daha fazla bilgi için bkz. [Sayfa URL'si oluşturma](create-page-URL.md).

> [!NOTE]
> Dynamics 365 Commerce URL'leri ve içeriği ayrıştırır. Başka bir deyişle, bir URL ile ilişkili olmayan bir sayfa oluşturulabilir ve bir sayfayla ilişkili olmayan bir URL oluşturulabilir. Bu nedenle, bir URL için içerik takası yapılabilir; kesinti süresi gerekmez ve yeniden yönlendirmeler daha kolay yönetilebilir.

## <a name="add-a-new-page"></a>Yeni sayfa ekleme

Sitenize yeni site sayfası eklemek için şu adımları izleyin.

1. **Siteler** altında, **Fabrikam**'ı seçin (veya sitenizin adını).
1. **Yeni Sayfa**'yı seçin.
1. **Yeni Sayfa** iletişim kutusunda , bir şablon ürün reçetesi seçin ve **Tamam**'ı tıklatın.
1. **Sayfa Adı** alanına bir sayfa adı girin (örneğin, **Yeni Sayfam**).
1. **URL** alanına URL'yi tamamlamak için bir dize (URL bilgi) girin (örneğin, **mynewpage**).
1. **Tamam**'ı seçin. Sayfa düzenleyici görüntülenir. Seçtiğiniz şablona göre bir üstbilgi ve altbilgi sayfaya otomatik olarak eklendiğine dikkat edin.
1. Sayfa anahattında **ana** yuvayı seçin, üç nokta düğmesini (**...**) ve sonra **Modül ekle**'yi seçin.
1. **Konteyner**'i seçin ve sonra **Tamam**'i seçin.
1. **Sıvı kabı**seçin, üç nokta düğmesini seçin ve sonra **Modül ekle**'yi seçin.
1. **İçerik zengin bloğu**seçeneğini belirleyin ve **Tamam**'ı seçin.
1. **İçerik Zengin Blok** seçin, üç nokta düğmesini seçin ve sonra **Modül ekle**'yi seçin.
1. **İçerik zengin bloğu öğesi**seçeneğini belirleyin ve **Tamam**'ı seçin.
1. Sağdaki Özellikler bölmesinde, **paragraf**'ı seçin ve sonra alanına **test metnimi** girin.
1. **Kaydet**i seçin ve sonra **Giriş**'i seçin.
1. **Yorumlar** alanında **yeni sayfa eklendi** seçeneğini girin ve **Tamam**'ı seçin.
1. Sayfanızın önizlemesini görüntülemek için **Önizleme**'yi seçin. Bitirdiğinizde, geliştirme aracına dönmek için Önizleme sekmesini kapatın.
1. **Yayımla**'yı seçin.
1. Gezinti yolunda (Breadcrumbs), **Fabrikam**'ı (veya sitenizin adını) seçin.
1. Soldaki gezinti bölmesinde **URL'leri** seçin.
1. Listede (**mynewpage**) öğesini bulun ve seçin.
1. **Yayımla**'yı seçin.

## <a name="additional-resources"></a>Ek kaynaklar

[Var olan site sayfasını değiştirme](modify-existing-page.md)

[Sayfa düzeni seçme](select-page-layouts.md)

[SEO meta verilerini yönetme](manage-seo-metadata.md)

[Sayfa kaydetme, önizleme ve yayımlama](save-preview-publish-page.md)

[Ürün sayfasını zenginleştirme](enrich-product-page.md)

[Kategori açılış sayfasını zenginleştirme](enrich-category-page.md)

[Sayfa içeriği erişilebilirliğini doğrula](verify-accessibility.md)
