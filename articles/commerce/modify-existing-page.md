---
title: Var olan site sayfasını değiştirme
description: Bu makalede, Microsoft Dynamics 365 Commerce'te mevcut site sayfasını değiştirme yöntemi açıklanmıştır.
author: psimolin
ms.date: 04/14/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: ceffb07afc8287e975f48696a059d3cd4ad20ffa
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8848875"
---
# <a name="modify-an-existing-site-page"></a>Var olan site sayfasını değiştirme

[!include [banner](includes/banner.md)]

Bu makalede, Microsoft Dynamics 365 Commerce'te mevcut site sayfasını değiştirme yöntemi açıklanmıştır.

Bir sayfayı değiştirmeniz gerektiğinde, ilk adım onu sayfa düzenleyici içinde açar. Sayfanızı içeren siteye gidin ve sonra sayfa listesinde istediğiniz sayfayı bulun. Sayfayı bulamazsanız, yazma aracının zengin arama işlevini kullanabilirsiniz. Tam sayfa adını yazın veya adın ilk birkaç harfini yazıp bir yıldız işareti (\*) yazın. Süzülmüş sayfalar listesi görüntülenir. İstediğiniz sayfayı bulmak için bu listeyi kullanabilirsiniz. Doğru sayfayı bulduktan sonra, sayfa düzenleyicisinde sayfayı açılacak sayfa adını seçin.

> [!TIP]
> Sayfanız sayfa denetçisinde görünüyorsa, **Düzenle**'yi seçebilir ve sayfayı sayfa düzenleyicisinde açılmadan önce kullanıma alabilirsiniz. Böylece, aynı anda birden fazla sayfayı kullanıma alabilirsiniz.

Sayfa düzenleyicide sayfanın açık olmasını istiyorsanız, öğenin kullanımınıza alındığından emin olmalısınız. Geliştirme aracındaki komut çubuğu dinamiktir, içeriğe duyarlıdır ve durum duyarlıdır. Bu nedenle, yalnızca sayfada gerçekleştirebileceğiniz eylemleri gösterir. Örneğin, sayfa sizin tarafınızdan kullanıma alınmadığından, komut çubuğunda **Kaydet** ve **Düzenlemeyi bitir** düğmeleri görünmez. Sayfanın durumu pencerenin sağ tarafında görünür.

Sayfa sizin tarafınızdan kullanıma alınmış durumda değilse, komut çubuğundan **Düzenle**'yi seçin. Komut çubuğu, sayfanın yeni durumunu yansıtacak şekilde değişir. Ayrıca, sayfanın size teslim edilmiş olduğunu bildiren bir bildirim alırsınız.

Sonraki adım, gerçek değişikliklerinizi yapmak içindir. Genellikle, sol taraftaki sayfa anahat ağacını kullanarak değiştirmek istediğiniz modülü bulun ve seçin ve sonra sağdaki Özellikler bölmesinde değişiklikleri yapın. 

Ancak, yaptığınız değişiklikler bazen model veya parçacık eklemeyi veya kaldırmayı içerebilir. Parça veya modül eklemek için, modül veya parçayı eklemek istediğiniz yuvayı bulmak amacıyla sayfa anahattı ağacını ve sonra o yuva için üç nokta düğmesini (**...**) kullanın. Modül veya parça eklemek için kullanılan komutları içeren bir menü görüntülenir. Bir modül veya parçayı kaldırmak için sayfa anahat ağacında bunu bulun ve seçin, üç nokta düğmesini seçin ve sonra modülü veya parçayı silmek için komutu seçin.

> [!TIP]
> Ayrıca, doğrudan seçerek görsel sayfa oluşturucu önizlemesinde görünür olan herhangi bir modülün özelliklerini görüntüleyebilir ve düzenleyebilirsiniz.

Değişikliklerinizi yapmayı bitirdikten ve etkilerini önizledikten sonra, komut çubuğunda **Düzenlemeyi bitir**'i seçerek sayfayı iade etmelisiniz. 

Değişikliklerinizi hemen yayımlamak için, komut çubuğunda **yayınla** 'yı seçin. Değiştirdiğiniz sayfanın en son iade edilen sürümü yayımlanır ve sitenizi görüntüleyen harici kullanıcılar tarafından kullanılabilir duruma gelir. 

## <a name="example-change-the-video-on-the-home-page"></a>Örnek: giriş sayfasındaki videoyu değiştirme

Aşağıdaki örnek, video oynatıcı modülünde görünen videoyu değiştirerek giriş sayfasının nasıl değiştirileceğini gösterir.

1. **Siteler** altında, **Fabrikam**'ı seçin (veya sitenizin adını).
1. Soldaki gezinti bölmesinde **Sayfalar** seçin.
1. Sayfa düzenleyicisinde açmak için giriş sayfasını bulun ve seçin.
1. Komut çubuğunda, **Düzenle** öğesini seçin.
1. Sayfa anahattında **ana** yuvayı seçin.
1. **Ana** yuvanın altında, tüm akışkan konteyneri modüllerini genişletin.
1. Video oynatıcı modülünü bulun ve seçin.
1. Sağdaki özellikler bölmesinde, **video** özelliğini seçin. Varlık seçici görüntülenir.
1. Varlık seçicisinde, uygun bir video varlığı seçin veya yeni bir video varlığı yüklemek için **yeni varlığı yükle**'yi seçin.
1. **Tamam**'ı seçin.
1. **Kaydet** i seçin ve sonra **Düzenlemeyi bitir**'i seçin.
1. **Yorumlar** alanında **Videoyu değiştir** seçeneğini girin ve **Tamam**'ı seçin.
1. Güncellenen sayfasını önizlemek için **Önizleme** 'yi seçin . Bitirdiğinizde, geliştirme aracına dönmek için Önizleme sekmesini kapatın.
1. **Yayımla**'yı seçin.

## <a name="additional-resources"></a>Ek kaynaklar

[Yeni site sayfası ekleme](add-new-page.md)

[Sayfa düzeni seçme](select-page-layouts.md)

[SEO meta verilerini yönetme](manage-seo-metadata.md)

[Sayfa kaydetme, önizleme ve yayımlama](save-preview-publish-page.md)

[Ürün sayfasını zenginleştirme](enrich-product-page.md)

[Kategori açılış sayfasını zenginleştirme](enrich-category-page.md)

[Sayfa içeriği erişilebilirliğini doğrulama](verify-accessibility.md)

[URL parametrelerini temel alan dinamik e-ticaret sayfaları oluşturma](create-dynamic-pages.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
