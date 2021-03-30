---
title: Ortam galerisi modülü
description: Bu konu ortam galerisi modüllerini kapsamaktadır ve Microsoft Dynamics 365 Commerce'te site sayfalarına nasıl ekleneceğini açıklamaktadır.
author: anupamar-ms
manager: annbe
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.13
ms.openlocfilehash: e9b5a8123c64dce2ba65758f0312a899646cf948
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5252570"
---
# <a name="media-gallery-module"></a>Ortam galerisi modülü

[!include [banner](includes/banner.md)]

Bu konu ortam galerisi modüllerini kapsamaktadır ve Microsoft Dynamics 365 Commerce'te site sayfalarına nasıl ekleneceğini açıklamaktadır.

Ortam galerisi modülleri bir veya daha fazla görüntüyü galeri görünümünde gösterir. Ortam galerisi modülleri yatay (görüntünün altında bir satır olarak) veya dikey olarak (görüntünün yanında bir sütun olarak) düzenlenebilen küçük resimleri destekler. Ortam galerisi modülleri ayrıca, resimlerin yakınlaştırılmasına (büyütülmesine) veya tam ekran modunda görüntülenmesine olanak veren özellikler sağlar. Ortam galerisi modülünde işlenebilmesi için bir resmin Commerce site oluşturucu Ortam kitaplığında bulunması gerekir. Şu anda, ortam galerisi modülleri yalnızca resimleri destekler.

Varsayılan modda, bir ortam galerisi modülü ilgili ürün görüntülerini oluşturmak için ürün ayrıntıları sayfasının (PDP) sayfa bağlamında kullanılabilen ürün kimliğini kullanır. Commerce Headquarters'da, tüm ürünler için bir ortam dosyası yolu tanımlanmalıdır. Resimler daha sonra, Commerce Headquarters'daki ürünler için tanımlanan dosya yoluna göre site oluşturucu Ortam kitaplığına yüklenmelidir. Bu resimler ürünlerin ve ürün çeşitlemesinin resimlerini içerir. Görüntüleri site oluşturucu Ortam kitaplığına yükleme hakkında daha fazla bilgi için bkz. [Resimleri yükleme](dam-upload-images.md).

Alternatif olarak, bir ortam galerisi modülü, ürün kimliği veya sayfa içeriğinde hiç bağımlılık bulunmayan bir resim galerisi sayfasında tam olarak seçilmiş bir resim kümesini barındırabilir. Bu durumda, resimlerin site oluşturucu Ortam Kitaplığı'na yüklenmesi ve site oluşturucuda belirtilmiş olması gerekir.

Ortam galerisi modülleri için bazı kullanım örnekleri şunlardır:

- Bir PDP üzerinde ürün resimlerini işleme
- Ürün pazarlama sayfasında ürün resimlerini işleme
- Galeri sayfası gibi bir pazarlama sayfasında, seçilmiş bir resim kümesini gösterme

Aşağıdaki çizimdeki örnekte, bir ortam galerisi modülü kullanılarak PDP'de bir satın alma kutusu ürün resimleri barındırılmaktadır.

![Ürün ayrıntıları sayfasında ortam galerisi modülünü kullanarak ana bilgisayar bilgileri sunan bir satın alma kutusu örneği](./media/ecommerce-pdp-buybox.PNG)

## <a name="media-gallery-properties"></a>Ortam galerisi özellikleri

| Özellik adı | Değerler | Tanım |
|---------------|--------|-------------|
| Görüntü kaynağı | **Sayfa bağlamı** veya **Ürün kimliği** | Varsayılan değer **Sayfa bağlamıdır**. **Sayfa bağlamı** seçilirse, modül sayfanın ürün kimliği bilgilerini sağlamasını bekler. **Ürün kimliği** seçilirse, bir resmin ürün kimliği, **Ürün kimliği** özelliğinin değeri olarak sağlanmalıdır. Bu özellik Commerce 10.0.12 sürümünde sunulmaktadır. |
| Ürün kodu | Bir ürün kimliği | Bu özellik yalnızca, **Resim kaynağı** özelliğinin değeri **Ürün kimliği** ise geçerlidir. |
| Görüntü yakınlaştırma | **Satır içi** veya **Kapsayıcı** | Bu özellik, ortam galerisi modülündeki resimlerin kullanıcı tarafından yakınlaştırmasına olanak tanır. Bir resim satır içi olarak veya görüntünün yanında ayrı bir kapsayıcıda yakınlaştırılabilir. Bu özellik 10.0.12 sürümünde mevcuttur. |
| Yakınlaştırma ölçeği | Bir ondalık sayı | Bu özellik, resimlerin yakınlaştırılacağı ölçek faktörünü belirtir. Örneğin, değer **2,5** olarak ayarlanırsa, resimler 2,5 kat büyütülür.|
| Tam ekran | **Doğru** veya **yanlış** | Bu özellik, resimlerin tam ekran modunda görüntülenip görüntülenemeyeceğini belirtir. Tam ekran modunda, yakınlaştırma özelliği etkinse resimler daha da büyütülebilir. Bu özellik Commerce 10.0.13 sürümünde sunulmaktadır. |
| Görüntüler | Site oluşturucu Ortam Kitaplığı'ndan seçilen resimler | Bir üründen oluşturulmalarının yanı sıra, resimler bir ortam galerisi modülü için de seçilebilir. Bu resimler kullanılabilir ürün resimlerine eklenir. Bu özellik Commerce 10.0.12 sürümünde sunulmaktadır. |
| Küçük resim yönü | **Dikey** veya **Yatay** | Bu özellik, küçük resimlerin dikey şeritte mi, yoksa yatay şeritte mi gösterileceğini belirtir. |

Aşağıdaki çizimde, tam ekran ve yakınlaştırma seçeneklerinin kullanılabilir olduğu bir ortam galerisi modülü örneği gösterilmektedir.

![Tam ekran ve yakınlaştırma seçeneklerinin kullanılabilir olduğu bir ortam galerisi modülü örneği](./media/ecommerce-media-zoom.png)

Aşağıdaki çizimde, seçilmiş resimlerin bulunduğu bir ortam galerisi modülü örneği gösterilmektedir (yani, belirtilen resimler ürün kimliğine veya sayfa bağlamına bağlı değildir).

![Seçilmiş resimler içeren bir ortam galerisi modülü örneği](./media/ecommerce-media-curated.PNG)

## <a name="commerce-scale-unit-interaction"></a>Ticari ölçek birim etkileşimi

Resim kaynağı sayfa bağlamından türetildiği zaman, resimleri almak için PDP'den alınan ürün kimliği kullanılır. Ortam galerisi modülü, ürünlerin resim dosyası yolunu Commerce Scale Unit uygulama programlama arabirimlerini (API'ler) kullanarak alır. Resimler, daha sonra modül içinde işlenebilmeleri için Ortam Kitaplığı'ndan çekilir.

## <a name="add-a-media-gallery-module-to-a-page"></a>Bir sayfaya ortam galerisi modülü ekleme

Bir pazarlama sayfasına ortam galerisi modül eklemek için bu adımları izleyin.

1. Bir yeni şablonu oluşturmak için **Şablonlar**'a gidin ve **Yeni**'yi seçin.
1. **Yeni Şablon** iletişim kutusunda **Şablon adı** altında, **Pazarlama şablonu**'nu girin ve **Tamam**'ı seçin.
1. **Gövde** yuvası için üç nokta (**...**) düğmesini seçin ve **Modül Ekle**'yi seçin.
1. **Modül Ekle** iletişim kutusunda **Varsayılan sayfa** modülünü seçin ve **Tamam**'ı seçin.
1. Varsayılan sayfada **Ana** yuvayı seçin, üç nokta düğmesini (**...**) ve sonra **Modül Ekle**'yi seçin.
1. **Modül Ekle** iletişim kutusunda **Konteyner** modülünü seçin ve **Tamam**'ı seçin.
1. **Kaydet**'i seçin, şablonu iade etmek için **Düzenlemeyi bitir**'i ve ardından yayımlamak için **Yayımla**'yı seçin.
1. **Sayfalar**'a gidin ve yeni sayfa oluşturmak için **Yeni**'yi seçin.
1. **Şablon seçin** iletişim kutusunda **Pazarlama şablonu** şablonunu seçin. **Sayfa adı** altından **Ortam galerisi sayfası** girin ve **Tamam**'ı seçin.
1. Yeni sayfada **ana** yuvayı seçin, üç nokta düğmesini (**...**) ve sonra **Modül ekle**'yi seçin.
1. **Modül Ekle** iletişim kutusunda **Konteyner** modülünü seçin ve **Tamam**'ı seçin.
1. **Konteyner** yuvası için üç nokta (**...**) düğmesini seçin ve **Modül Ekle**'yi seçin.
1. **Modül Ekle** iletişim kutusunda **Ortam galerisi** modülünü seçin ve **Tamam**'ı seçin.
1. Ortam galerisi modülünün özellik bölmesinde, **Resim kaynağı** altında **Ürün kimliği**'ni seçin. Ardından **Ürün kimliği** alanına ürün kimliği girin.
1. **Kaydet**'i seçin ve ardından sayfayı önizlemek için **Önizleme**'yi seçin. Ürünün resimlerini galeri görünümünde görebilirsiniz.
1. Yalnızca seçilen resimleri kullanmak için özellik bölmesinde, **Resim kaynağı** altında **Ürün kimliği**'ni seçin. Ardından, **Resimler** altında , Ortam Kitaplığı'ndan resim eklemek için istediğiniz kadar **Resim ekle**'yi seçin.
1. **Görüntü yakınlaştırma**, **Yakınlaştırma faktörü** ve **Küçük resim yönü** gibi ayarlamak istediğiniz ek özellikleri ayarlayın.
1. İşiniz bittiğinde, **Kaydet**'i seçin, sayfayı iade etmek için **Düzenlemeyi bitir**'i ve ardından yayımlamak için **Yayımla**'yı seçin.

## <a name="additional-resources"></a>Ek kaynaklar

[Modül kitaplığına genel bakış](starter-kit-overview.md)

[Satın alma kutusu modülü](add-buy-box.md)

[Kapsayıcı modülü](add-container-module.md)

[Resimleri karşıya yükleme](dam-upload-images.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]