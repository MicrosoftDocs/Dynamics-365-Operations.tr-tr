---
title: Ortam galerisi modülü
description: Bu konu ortam galerisi modüllerini kapsamaktadır ve Microsoft Dynamics 365 Commerce'te site sayfalarına nasıl ekleneceğini açıklamaktadır.
author: anupamar-ms
ms.date: 05/18/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.13
ms.openlocfilehash: 0d05129145c5d6c3967b243cb0855a1c4fd3e84e
ms.sourcegitcommit: ccb39767bd3430c24f4653c26560bba2cd66553c
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/19/2022
ms.locfileid: "8780880"
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

![Ürün ayrıntıları sayfasında ortam galerisi modülünü kullanarak ana bilgisayar bilgileri sunan bir satın alma kutusu örneği.](./media/ecommerce-pdp-buybox.PNG)

## <a name="media-gallery-properties"></a>Ortam galerisi özellikleri

| Özellik adı | Değerler | Tanım |
|---------------|--------|-------------|
| Görüntü kaynağı | **Sayfa bağlamı** veya **Ürün kimliği** | Varsayılan değer **Sayfa bağlamıdır**. **Sayfa bağlamı** seçilirse, modül sayfanın ürün kimliği bilgilerini sağlamasını bekler. **Ürün kimliği** seçilirse, bir resmin ürün kimliği, **Ürün kimliği** özelliğinin değeri olarak sağlanmalıdır. Bu özellik Commerce 10.0.12 sürümünde sunulmaktadır. |
| Ürün kodu | Bir ürün kimliği | Bu özellik yalnızca, **Resim kaynağı** özelliğinin değeri **Ürün kimliği** ise geçerlidir. |
| Görüntü yakınlaştırma | **Satır içi** veya **Kapsayıcı** | Bu özellik, ortam galerisi modülündeki resimlerin kullanıcı tarafından yakınlaştırmasına olanak tanır. Bir resim satır içi olarak veya görüntünün yanında ayrı bir kapsayıcıda yakınlaştırılabilir. Bu özellik 10.0.12 sürümünde mevcuttur. |
| Yakınlaştırma faktörü | Bir ondalık sayı | Bu özellik, resimlerin yakınlaştırılacağı ölçek faktörünü belirtir. Örneğin, değer **2,5** olarak ayarlanırsa, resimler 2,5 kat büyütülür. |
| Tam ekran | **Doğru** veya **yanlış** | Bu özellik, resimlerin tam ekran modunda görüntülenip görüntülenemeyeceğini belirtir. Tam ekran modunda, yakınlaştırma özelliği etkinse resimler daha da büyütülebilir. Bu özellik, Commerce 10.0.13 sürümünde bulunur. |
| Yakınlaştırılmış görüntü kalitesi | İzleme çubuğu denetimi kullanılarak seçilen ve bir yüzdeyi temsil eden, 1 ile 100 arasında bir sayı | Bu özellik, yakınlaştırılmış görüntülerin görüntü kalitesini tanımlar. Yakınlaştırılmış bir görüntünün her zaman mümkün olan en yüksek çözünürlüğü kullanmasını sağlamak için %100'e ayarlanabilir. Bu özellik, kayıpsız biçim kullandıkları için PNG dosyalarına uygulanamaz. Bu özellik, Commerce 10.0.19 sürümünden itibaren bulunur. |
| Görüntüler | Site oluşturucu Ortam Kitaplığı'ndan seçilen resimler | Bir üründen oluşturulmalarının yanı sıra, resimler bir ortam galerisi modülü için de seçilebilir. Bu resimler kullanılabilir ürün resimlerine eklenir. Bu özellik Commerce 10.0.12 sürümünde sunulmaktadır. |
| Küçük resim yönü | **Dikey** veya **Yatay** | Bu özellik, küçük resimlerin dikey şeritte mi, yoksa yatay şeritte mi gösterileceğini belirtir. |
| Varyant için ana ürün görüntülerini gizle | **Doğru** veya **yanlış** | Bu özellik **Doğru** olarak ayarlanırsa , varyant seçildiği zaman, varyantın hiç görüntüsü yoksa ana ürünün görüntüleri gizlenir. Bu özellik, varyantları olmayan ürünleri etkilemez. |
| Boyut seçiminde ortamı güncelleştirme | **Doğru** veya **yanlış** | Bu özellik **Doğru** olarak ayarlanırsa ortam kitaplığındaki görüntüler, boyutlar (renk, stil veya boyut gibi) seçildiğinde ve görüntü kullanılabilirse güncelleştirilir. Bu özellik, ilgili görüntüyü güncelleştirmek için her ürün çeşidinin boyutunun seçilmesi gerekmediğinden tarama deneyimini basitleştirmeye yardımcı olur. Bu özellik, **Gelişmiş** sekmesinde kullanılabilir. |

> [!IMPORTANT]
> **Boyut seçiminde ortamı güncelleştirme** özelliği, Commerce 10.0.21 sürümü itibarıyla kullanılabilir. Bunun için Commerce modül kitaplığı paketi sürüm 9.31'in yüklü olması gerekir.

Aşağıdaki çizimde, tam ekran ve yakınlaştırma seçeneklerinin kullanılabilir olduğu bir ortam galerisi modülü örneği gösterilmektedir.

![Tam ekran ve yakınlaştırma seçeneklerinin kullanılabilir olduğu bir ortam galerisi modülü örneği.](./media/ecommerce-media-zoom.png)

Aşağıdaki çizimde, seçilmiş resimlerin bulunduğu bir ortam galerisi modülü örneği gösterilmektedir (yani, belirtilen resimler ürün kimliğine veya sayfa bağlamına bağlı değildir).

![Seçilmiş resimler içeren bir ortam galerisi modülü örneği.](./media/ecommerce-media-curated.PNG)

## <a name="commerce-scale-unit-interaction"></a>Ticari ölçek birim etkileşimi

Resim kaynağı sayfa bağlamından türetildiği zaman, resimleri almak için PDP'den alınan ürün kimliği kullanılır. Ortam galerisi modülü, ürünlerin resim dosyası yolunu Commerce Scale Unit uygulama programlama arabirimlerini (API'ler) kullanarak alır. Resimler, daha sonra modül içinde işlenebilmeleri için Ortam Kitaplığı'ndan çekilir.

## <a name="add-a-media-gallery-module-to-a-page"></a>Bir sayfaya ortam galerisi modülü ekleme

Bir pazarlama sayfasına ortam galerisi modül eklemek için bu adımları izleyin.

1. Bir yeni şablonu oluşturmak için **Şablonlar**'a gidin ve **Yeni**'yi seçin.
1. **Yeni şablon** iletişim kutusunda **Şablon adı** altında, **Pazarlama şablonu**'nu girin ve **Tamam**'ı seçin.
1. **Gövde** alanında, üç nokta (**...**) düğmesini seçin ve **Modül ekle**'yi seçin.
1. **Modülleri seç** iletişim kutusunda **Varsayılan Sayfa** modülünü seçin ve **Tamam**'ı seçin.
1. Varsayılan sayfada **Ana** alanını seçin, üç nokta düğmesini (**...**) ve sonra **Modül ekle**'yi seçin.
1. **Modül seç** iletişim kutusunda **Konteyner** modülünü seçin ve **Tamam**'ı seçin.
1. **Kaydet**'i seçin, şablonu iade etmek için **Düzenlemeyi bitir**'i ve ardından yayımlamak için **Yayımla**'yı seçin.
1. **Sayfalar**'a gidin ve yeni sayfa oluşturmak için **Yeni**'yi seçin.
1. **Yeni sayfa oluştur** iletişim kutusundaki **Sayfa adı** altında, **Medya galerisi sayfası**'nı girin ve **İleri**'yi seçin.
1. **Şablon seç** bölümünde, oluşturduğunuz **Pazarlama şablonunu** seçin ve sonra **İleri**'yi seçin.
1. **Bir düzen seçin** bölümünde, bir sayfa düzeni seçin (ör. **Esnek düzen**) ve sonra **İleri**'yi seçin.
1. **İnceleyin ve bitirin** bölümünde, sayfa yapılandırmasını gözden geçirin. Sayfa bilgilerini düzenlemeniz gerekiyorsa, **Geri**'yi seçin. Sayfa bilgileri doğruysa, **Sayfa oluştur**'u seçin. 
1. Yeni sayfanın **Ana** alanında, üç nokta düğmesini (**...**) ve sonra **Modül ekle**'yi seçin.
1. **Modül seç** iletişim kutusunda **Konteyner** modülünü seçin ve **Tamam**'ı seçin.
1. **Konteyner** alanında, üç nokta (**...**) düğmesini seçin ve **Modül ekle**'yi seçin.
1. **Modülleri seç** iletişim kutusunda **Medya galerisi** modülünü seçin ve **Tamam**'ı seçin.
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
