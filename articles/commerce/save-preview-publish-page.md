---
title: Sayfa kaydetme, önizleme ve yayımlama
description: Bu konuda, Microsoft Dynamics 365 Commerce'te sayfa kaydetme, önizleme ve yayınlama yöntemi açıklanmıştır.
author: psimolin
manager: annbe
ms.date: 04/14/2020
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
ms.openlocfilehash: db4866b22060b764fdde3e4a44e99e969133c0a0
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "4416518"
---
# <a name="save-preview-and-publish-a-page"></a>Sayfa kaydetme, önizleme ve yayımlama

[!include [banner](includes/banner.md)]

Bu konuda, Microsoft Dynamics 365 Commerce'te sayfa kaydetme, önizleme ve yayınlama yöntemi açıklanmıştır.

## <a name="save-a-page"></a>Sayfa kaydetme

Sayfayı kaydetmek için, belgenizi kullanıma almış ve sayfa düzenleyicisinde açmanız gerekir. Bir sayfayı kullanıma almak için komut çubuğunda **Düzenle**'yi seçin. Bir sayfayı düzenlemeyi bitirdikten sonra, değişikliklerinizin saklanmasını sağlamak sayfayı hemen kaydetmelisiniz.

Bir sayfayı kaydettiğinizde, değişiklikler yalnızca size görünebilir. Kaydetme işlemi öncelikle, sayfa henüz iade edilmeye hazır olmadığı sürece değişiklikleri depolamaya yöneliktir. Sayfayı değiştirmeyi bitirdiğinizde, gözden geçirin ve böylece değişiklikler başkaları tarafından görülebilir hale gelir. Bu noktada, sayfa değiştirilmesi gereken diğer kullanıcılar tarafından da kullanıma açılabilir.

## <a name="preview-a-page"></a>Sayfayı önizleme

Geliştirme aracı, iki tür önizleme özelliği sunar: Sayfa düzenleyicisinde "gördüğünüz şey aldığınız şeydir" (WYSIWYG) Önizleme bölmesi olan görsel sayfa oluşturucu ve ayrı bir önizleme penceresi.

Sayfa düzenleyicisini kullanırken, Orta bölmede "aldığınız şey görüntülenir" (WYSIWYG) önizlemesi görüntülenir. Bu önizleme, sayfayı her kaydedişinizde otomatik olarak güncelleştirilir. Bunu, komut çubuğunda **Yenile** seçerek el ile de güncelleştirebilirsiniz. Önizleme, sayfayı sitenin kullanıcıları göreceği gibi işler, ancak yazma yardımcıları bunun üzerinde işlenir.

Sayfayı değiştirmeyi bitirdiğinizde, hangi müşterilerin görebileceğini görmek için önizlemek isteyebilirsiniz. Bir sayfayı önizlemek için, komut çubuğunda **önizleme**'yi seçin. Önizleme, ayrı bir tarayıcı penceresinde görüntülenir. Önizleme penceresindeki sayfa, sitenin kullanıcısı tarafından göreceğiniz şekilde oluşturulur. Yanıt veren modüllerin tüm görünüm bağlantı noktalarında doğru şekilde işlendiğine emin olmak için pencereyi yeniden boyutlandırabilirsiniz.

> [!NOTE]
> Yayımlanmamış içeriğin önizlemesi için kimlik doğrulama ve doğru izinler gereklidir. Bu nedenle, önizlemenin URL'sini başka biriyle paylaşıyorsanız bu kişinin içeriğe erişmek için doğru izinlere sahip olması gerekir.

## <a name="publish-a-page"></a>Sayfayı yayımla

Sayfanız hazır olduğunda, bir sonraki adım bunu yayınlamaktır, böylece harici kullanıcılar içeriği görüntüleyebilir. Bir sayfayı yayımlayabilmeniz için, komut çubuğunda **Düzenlemeyi bitir**'i seçerek sayfayı iade etmeniz gerekir.

Sayfaları sayfa denetçisinde veya sayfa düzenleyicisinden yayımlayabilir veya yayımdan kaldırabilirsiniz. Sayfa denetçisi, sayfaların listesini gösterir ve toplu işlemlere izin verir. Sayfa düzenleyicisi, yalnızca içinde açık olan tek bir sayfayı yayınlamak veya yayımdan kaldırmak için kullanılabilir.

Sayfa denetçisinde bir veya daha fazla sayfa yayınlamak için sayfaları seçin, bunların iade edilmiş olduklarından emin olun ve sonra komut çubuğunda **Yayınla**'yı seçin. Sayfalar yayımlanır ve geliştirme aracında bu işlemle ilgili bir bildirim alırsınız.

Sayfa düzenleyicisinden tek bir sayfa yayımlamak için, yordam benzerdir. Sayfa düzenleyicisinde açık olduğu sürece, iade edilmiş olduğundan emin olun ve sonra komut çubuğunda **yayınla**'yı seçin. Sayfa yayımlanır ve bu işlemle ilgili bir bildirim alırsınız.

Bir sayfayı yayımladığınızda, yalnızca sayfa içeriği yayımlanır. Siz ve diğer kullanıcılar sayfaya gidip URL ile ilişkilendirildikten sonra görebilir. URL'nin ayrı olarak yayımlanması gerekir.

> [!IMPORTANT]
> Bir sayfayı yayımlayabilmeniz için, sayfanın referans aldığı tüm resimler veya parçalar önceden yayımlanmış olmalıdır.

## <a name="save-preview-and-publish-a-home-page"></a>Giriş sayfa kaydetme, önizleme ve yayımlama

Bir giriş sayfasını kaydetmek, önizlemek ve yayınlamak için aşağıdaki adımları izleyin.

1. **Siteler** altında, **Fabrikam**'ı seçin (veya sitenizin adını).
1. Soldaki gezinti bölmesinde **Sayfalar** seçin.
1. Sayfa düzenleyicisinde açmak için giriş sayfasını bulun ve seçin.
1. **Düzenle** öğesini seçin.
1. Sayfayı gerektiği gibi değiştirin.
1. **Kaydet** i seçin ve sonra **Düzenlemeyi bitir**'i seçin.
1. **Yorumlar** alanına yaptığınız değişikliklerle ilgili bir not girin ve **Tamam**'ı seçin.
1. Sayfanızın önizlemesini görüntülemek için **Önizleme**'yi seçin. Bitirdiğinizde, geliştirme aracına dönmek için Önizleme sekmesini kapatın.
1. **Yayımla**'yı seçin.

## <a name="publish-a-url"></a>URL Yayımla

Bir URL yayımlamak için şu adımları izleyin.

1. **Siteler** altında, **Fabrikam**'ı seçin (veya sitenizin adını).
1. Soldaki gezinti bölmesinde **URL'leri** seçin.
1. Yayınlamak için URL bulun ve seçin.
1. Komut çubuğunda, **Yayınla** öğesini seçin.

## <a name="additional-resources"></a>Ek kaynaklar

[Var olan site sayfasını değiştirme](modify-existing-page.md)

[Yeni site sayfası ekleme](add-new-page.md)

[Sayfa düzeni seçme](select-page-layouts.md)

[SEO meta verilerini yönetme](manage-seo-metadata.md)

[Ürün sayfasını zenginleştirme](enrich-product-page.md)

[Kategori açılış sayfasını zenginleştirme](enrich-category-page.md)

[Sayfa içeriği erişilebilirliğini doğrula](verify-accessibility.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]