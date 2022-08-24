---
title: Etkin görüntü modülü
description: Bu makale etkin görüntü modüllerini kapsamaktadır ve Microsoft Dynamics 365 Commerce'ün site sayfalarına nasıl ekleneceğini açıklamaktadır.
author: anupamar-ms
ms.date: 05/18/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.8
ms.search.industry: ''
ms.search.form: ''
ms.openlocfilehash: fdcd54adc98c7bc52ab6ff1ef7d5d03616aadfc3
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/12/2022
ms.locfileid: "9267630"
---
# <a name="active-image-module"></a>Etkin görüntü modülü

[!include [banner](includes/banner.md)]

Bu makale etkin görüntü modüllerini kapsamaktadır ve Microsoft Dynamics 365 Commerce'ün site sayfalarına nasıl ekleneceğini açıklamaktadır.

Etkin bir görüntü modülü, bir görüntüye ürün etiketleri katıştırmak için kullanılabilir. Böylece, E-ticaret sitesi kullanıcıları resimde gösterilen ürünlerin önizlemesini yapmak için etiketlerin üzerine gelebilir. Önizlemeler açılır pencerelerin içinde gösterilir. Önizleme açılır penceresini seçtiğinizde, kullanıcılar doğrudan ilgili ürüne ait ürün ayrıntıları sayfasına (PDP) gidebilirler.

Etiketler, görüntüde X ve Y koordinatları kullanılarak tanımlanır. Her etiketli nokta, görüntüde gösterilen ürünün ürün kimliğiyle yapılandırılmalıdır.

Aşağıdaki çizimde, Adventure Works giriş sayfasındaki her bir görüntüde bulunan önizleme açılır penceresinin bir örneği gösterilmektedir.

![Etkin bir görüntü modülündeki önizleme açılır penceresi örneği](./media/Active_image.PNG)

> [!IMPORTANT]
> - Etkin görüntü modülü, Dynamics 365 Commerce 10.0.20 sürümü itibarıyla kullanılabilir.
> - Etkin görüntü modülü Adventure Works temalarında görüntülenir.

## <a name="active-image-module-properties"></a>Etkin görüntü modülü özellikleri

| Özellik adı      | Değerler | Tanım |
|--------------------|--------|-------------|
| Görüntü              | Resim dosyası | Bir görüntü, bir veya daha fazla ürünü sergilemek için kullanılabilir. Görüntü, Commerce site oluşturucudaki Ortam Kitaplığı'na yüklenebilir veya mevcut bir görüntü kullanılabilir. |
| Genişlik              | Piksel sayısı | Bu özellik resmin genişliğini tanımlar. Etkin koordinatlar görüntünün genişliğine göre hesaplanır.|
| Etkin koordinatlar | X ve Y koordinatları ve bir ürün kimlik numarası | Her etkin görüntü dizisi, X ve Y koordinatları ile bir ürün kimlik numarası içerir.|
| Başlık            | Başlık metni ve başlık etiketi (**H1**, **H2**, **H3**, **H4**, **H5** veya **H6**) | Varsayılan olarak başlık için **H2** başlık etiketi kullanılır, ancak başlık etiketi erişilebilirlik gereksinimlerini karşılamak için değiştirilebilir. |
| Paragraf          | Paragraf metni | Modül zengin metin biçimindeki paragraf metnini destekler. Kalın, altı çizili, italik metin ve köprüler gibi bazı temel zengin metin özellikleri desteklenir. Bu yeteneklerden bazıları, modüle uygulanan sayfa teması tarafından geçersiz kılınabilir. |
| Bağla               | Bağlantı metni, bağlantı URL'si, Erişilebilir Zengin İnternet Uygulamaları (ARIA) etiketi ve **Bağlantıyı yeni sekmede aç** seçicisi | Modül bir veya daha fazla "eyleme çağrı" bağlantısı destekler. Bir bağlantı eklenirse, bağlantı metni, bir URL ve bir ARIA etiketi gereklidir. ARIA etiketleri erişilebilirlik gereksinimlerini karşılayacak şekilde açıklayıcı olmalıdır. Bağlantılar yeni bir sekmede açılacak şekilde konfigüre edilebilir. |
| Alt metin           | Başlık, metin ve bağlantılar | Resim için yazar veya tasarımcı adı veya kişisel bloglara bağlantılar gibi ek bağlam eklenebilir.|
| Metin teması         | **Açık** veya **Koyu** | Bu özellik, kullanıcıya metni arka plan resmine göre açık veya koyu olarak ayarlama olanağı tanır. Adventure Works temalarında bir tema uzantısı olarak mevcuttur. |

## <a name="add-an-active-image-module-to-a-new-page"></a>Yeni sayfaya etkin görüntü modülü ekleme

Yeni sayfaya etkin görüntü modülü eklemek ve gerekli özellikleri ayarlamak için aşağıdaki adımları izleyin.

1. **Şablonlar**'a gidin ve sitenizin giriş sayfası için pazarlama şablonunu açın (veya yeni bir pazarlama şablonu oluşturun).
1. Varsayılan sayfada **Ana** alanını seçin, üç nokta düğmesini (**...**) ve sonra **Modül ekle**'yi seçin.
1. **Modülleri seç** iletişim kutusunda **Etkin görüntü** modülünü ve **Tamam**'ı seçin.
1. **Kaydet**'i seçin, şablonu iade etmek için **Düzenlemeyi bitir**'i ve ardından yayımlamak için **Yayımla**'yı seçin.
1. **Sayfalar**'a gidin ve sitenin giriş sayfasını açın (veya pazarlama şablonunu kullanarak yeni bir giriş sayfası oluşturun).
1. Varsayılan sayfada **Ana** alanını seçin, üç nokta düğmesini (**...**) ve sonra **Modül ekle**'yi seçin.
1. **Modülleri seç** iletişim kutusunda **Etkin görüntü** modülünü ve **Tamam**'ı seçin.
1. Etkin görüntü modülünün özellik bölmesinde bir görüntü ekleyin ve tuval genişliğini görüntünün boyutuna ayarlayın.
1. X ve Y koordinatlarını ayarlayın ve uygun ürün kimliği numarasını ekleyin.
1. Etkin görüntü modüllerini gereksinim duyduğunuz şekilde ekleyin ve yapılandırın.
1. **Kaydet**'i seçin ve ardından sayfayı önizlemek için **Önizleme**'yi seçin.
1. Şablonu iade etmek için **Düzenlemeyi bitir**'i seçin, ardından yayımlamak için **Yayımla**'yı seçin.

## <a name="additional-resources"></a>Ek kaynaklar

[Modül kitaplığına genel bakış](starter-kit-overview.md)

[Adventure Works teması](adventure-works-theme.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
