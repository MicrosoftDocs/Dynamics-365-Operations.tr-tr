---
title: Yeni site sayfası ekleme
description: Bu makalede, Microsoft Dynamics 365 Commerce'e yeni bir site sayfası ekleme yöntemi açıklanmıştır.
author: josaw1
ms.date: 02/03/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.custom: ''
ms.assetid: ''
ms.openlocfilehash: f6714463c9d5dc844b03f78f0f6ff60c5f270da3
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/12/2022
ms.locfileid: "9270331"
---
# <a name="add-a-new-site-page"></a>Yeni site sayfası ekleme

[!include [banner](includes/banner.md)]

Bu makalede, Microsoft Dynamics 365 Commerce'e yeni bir site sayfası ekleme yöntemi açıklanmıştır.

Siteniz için şablonlar ve parçalar oluşturduktan sonraki adım bunları kullanan sayfalar oluşturmaya başlamak içindir. Başlamak için, bir şablon veya düzen, bir sayfa adı ve bir sayfa URL'si seçmelisiniz.

## <a name="template-or-layout"></a>Şablon veya düzen

Yeni sayfanız için bir şablon ya da Düzen kullanabilirsiniz. Daha fazla bilgi için bkz. [Şablonlar ve düzenlere genel bakış](templates-layouts-overview.md).

## <a name="specify-the-page-name"></a>Sayfa adını belirtme

Sayfa adı siteniz için eşsiz olmalı ve kolayca bulabilmeniz ve sayfanın amacı hakkında diğer kişileri de bilgilendirmeniz için açıklayıcı olmalıdır. Daha sonra, özellik bölmesinde sayfa adının yanında bulunan kalem sembolünü seçerek sayfanızı düzenleyip yeniden adlandırabilirsiniz.

## <a name="specify-the-page-url"></a>Sayfa URL'sini belirtme

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
1. **Sıvı kabı** seçin, üç nokta düğmesini seçin ve sonra **Modül ekle**'yi seçin.
1. **İçerik zengin bloğu** seçeneğini belirleyin ve **Tamam**'ı seçin.
1. **İçerik Zengin Blok** seçin, üç nokta düğmesini seçin ve sonra **Modül ekle**'yi seçin.
1. **İçerik zengin bloğu öğesi** seçeneğini belirleyin ve **Tamam**'ı seçin.
1. Sağdaki Özellikler bölmesinde, **paragraf**'ı seçin ve sonra alanına **test metnimi** girin.
1. **Kaydet** i seçin ve sonra **Düzenlemeyi bitir**'i seçin.
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

[Sayfa içeriği erişilebilirliğini doğrulama](verify-accessibility.md)

[URL parametrelerini temel alan dinamik e-ticaret sayfaları oluşturma](create-dynamic-pages.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
