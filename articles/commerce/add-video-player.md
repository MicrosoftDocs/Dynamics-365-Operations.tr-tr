---
title: Video oynatıcı modülü
description: Bu konu vide oynatıcı modüllerini kapsamaktadır ve Microsoft Dynamics 365 Commerce'un site sayfalarına nasıl ekleneceğini açıklamaktadır.
author: anupamar-ms
ms.date: 07/08/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 8d09797d24572a99cc8f5ed2d34b73eb7144af7a35661a929b6a571a20dfed04
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/05/2021
ms.locfileid: "6731731"
---
# <a name="video-player-module"></a>Video oynatıcı modülü

[!include [banner](includes/banner.md)]

Bu konu vide oynatıcı modüllerini kapsamaktadır ve Microsoft Dynamics 365 Commerce'un site sayfalarına nasıl ekleneceğini açıklamaktadır.

Video oynatımını desteklemek için video oynatma modülü kullanılır. Video içeriğinin içerik yönetim sistemi ne (CMS) yüklenmesi ve kullanılabilir olması koşuluyla, herhangi bir sayfaya eklenebilir. Video oynatıcı modülü .mp4 ortam türünü destekler.

## <a name="video-player-module"></a>Video oynatıcı modülü

Video oynatıcı modülü bir e-ticaret sitesinde videoları sergileyebilecek şekilde kullanılabilir. Yürüt, Duraklat, tam boyut modu, ses açıklamaları ve kapalı açıklamalı alt yazılar gibi tüm kayıttan yürütme yeteneklerini destekler. Video oynatıcı modülü, Microsoft erişilebilirlik standartlarını karşılamak için kapalı açıklamalı alt yazıların özelleştirmesini de destekler. Örneğin, yazı tipi boyutunu ve arka plan rengini özelleştirebilirsiniz.

Video oynatıcı modülü ikincil ses parçalarını da destekler. Bir video CMS'ye karşıya yüklendiğinde, ikincil bir ses parçası da karşıya yüklenebilir. Böylece, bir kullanıcı seçerse, video oynatıcı modülü ikincil ses kanalını yürütebilir.

### <a name="examples-of-video-player-modules-in-e-commerce"></a>E-ticaret'da video oynatıcı modülleri örnekleri

- Ürün Ayrıntıları sayfalarındaki veya pazarlama sayfalarındaki yönerge videoları
- Tüm pazarlama sayfaları üzerindeki ilkelerle ilgili videolar veya promosyon videoları
- Ürün Ayrıntıları sayfalarındaki veya pazarlama sayfalarındaki ürün özelliklerini vurgulayan pazarlama videoları

Aşağıdaki resimde giriş sayfasında kullanılan bir video oynatıcı modülü örneği gösterilmektedir.

![Video oynatıcı modülü örneği.](./media/ecommerce-videoplayer.PNG)

### <a name="video-player-module-properties"></a>Video oynatıcı modülü özellikleri

| Özellik adı         | Değer                               | Tanım |
|-----------------------|-------------------------------------|-------------|
| Başlık               | Başlık metni ve başlık etiketi (**H1**, **H2**, **H3**, **H4**, **H5** veya **H6**) | Varsayılan olarak başlık için **H2** başlık etiketi kullanılır, ancak başlık etiketi erişilebilirlik gereksinimlerini karşılamak için değiştirilebilir. |
| Zengin metin             | Paragraf metni | Modül zengin metin biçimindeki paragraf metnini destekler. Kalın, altı çizili, italik metin ve köprüler gibi bazı temel zengin metin özellikleri desteklenir. Bu yeteneklerden bazıları, modüle uygulanan sayfa teması tarafından geçersiz kılınabilir. |
| Bağla                  | Bağlantı metni, bağlantı URL'si, Erişilebilir Zengin İnternet Uygulamaları (ARIA) etiketi ve **Bağlantıyı yeni sekmede aç** seçicisi | Modül bir veya daha fazla "eyleme çağrı" bağlantısı destekler. Bir bağlantı eklenirse, bağlantı metni, bir URL ve bir ARIA etiketi gereklidir. ARIA etiketleri erişilebilirlik gereksinimlerini karşılayacak şekilde açıklayıcı olmalıdır. Bağlantılar yeni bir sekmede açılacak şekilde konfigüre edilebilir. |
| Alt metin              | Başlık, metin veya bağlantılar | Video oynatıcı modülü için yazar veya tasarımcı adı veya kişisel bloglara bağlantılar gibi ek bağlam eklenebilir. |
| Otomatik Yürütme             | **Doğru** veya **yanlış**               | Değer **doğru** olarak ayarlandığında, video otomatik olarak yürütülür. |
| Sesi Kapat                  | **Doğru** veya **yanlış**               | Değer **doğru** olarak ayarlandığında, ses kapatılır. Bu oynatıcı için varsayılan değer **yanlış**'tır. Chrome tarayıcıda, Otomatik yürütme videoları varsayılan olarak kapalı ve ses ancak videoyu el ile oynadığında yürütülür. |
| Döngü                  | **Doğru** veya **yanlış**               | Değer **doğru** olarak ayarlandığında, video döngü olarak tekrarlanır. |
| Ortam                 | Video dosya yolu ve adı. | Video oynatıcı tarafından oynanan video dosyası. |
| Tam ekran oynat       | **Doğru** veya **yanlış**               | Değer **doğru** olarak ayarlandığında, video tam ekran modunda yürütülür. |
| Oynat/duraklat tetikleyicisi    | **Doğru** veya **yanlış**               | Değer **doğru** olarak ayarlandığında, videoda bir Oynat/Duraklat düğmesi görüntülenir. |
| Video oynatıcı denetimleri | **Doğru** veya **yanlış**               | Değer **Doğru** olarak ayarlandığında, tüm video oynatıcı denetimler gösterilir. Bu denetimler, oynat ve Duraklat düğmelerini, ilerleme göstergesini ve açıklamalı alt yazıları seçeneklerini içerir. |
| Poster görüntüsünü gizle     | **Doğru** veya **yanlış**               | Videoda poster karesi olabilir. Bu özelliğin değeri **doğru** olarak ayarlandığında, poster çerçevesi gizlenir. |
| Maske düzeyi            | **0** ile **100** arasında bir sayı | Stil oluşturma için videoya uygulanan maske. |

> [!IMPORTANT]
> **Başlık**, **Zengin metin**, **Bağlantı** ve **Alt metin** özellikleri Dynamics 365 Commerce 10.0.20 sürümü itibarıyla kullanılabilir.

## <a name="add-a-video-player-module-to-a-page"></a>Sayfaya video oynatıcı modülü ekleme

> [!NOTE] 
> Video oynatıcı modülü oluşturmadan önce, ortam kitaplığı 'na bir video yüklemeniz gerekir.

Bir yeni sayfaya video oynatma modülü eklemek ve gerekli özellikleri ayarlamak için aşağıdaki adımları izleyin.

1. Bir yeni şablonu oluşturmak için **Şablonlar**'a gidin ve **Yeni**'yi seçin.
1. **Yeni Şablon** iletişim kutusunda **Şablon adı** altında, **Video oynatıcı şablonu**'nu girin ve **Tamam**'ı seçin.
1. **Gövde** yuvası için üç nokta (**...**) düğmesini seçin ve **Modül Ekle**'yi seçin.
1. **Modül Ekle** iletişim kutusunda **Varsayılan sayfa** modülünü seçin ve **Tamam**'ı seçin.
1. **Varsayılan sayfa** modülünde **ana** yuvayı seçin, üç nokta düğmesini (**...**) ve sonra **Modül ekle**'yi seçin.
1. **Modül Ekle** iletişim kutusunda **Konteyner** modülünü seçin ve **Tamam**'ı seçin.
1. **Konteyner** yuvası için üç nokta (**...**) düğmesini seçin ve **Modül Ekle**'yi seçin.
1. **Modül Ekle** iletişim kutusunda **video oynatıcı** modülünü seçin ve **Tamam**'ı seçin.
1. **Kaydet**'i seçin, şablonu iade etmek için **Düzenlemeyi bitir**'i ve ardından yayımlamak için **Yayımla**'yı seçin. 
1. **Sayfalar**'a gidin ve yeni sayfa oluşturmak için **Yeni**'yi seçin.
1. **Şablon seç** iletişim kutusunda, oluşturduğunuz video oynatıcı şablonunu seçin. Bir **sayfa adı** ve sayfa **Video oynatcı sayfası** girin ve **Tamam**'ı seçin.
1. Yeni sayfada **ana** yuvayı seçin, üç nokta düğmesini (**...**) ve sonra **Modül ekle**'yi seçin.
1. **Modül Ekle** iletişim kutusunda **Konteyner** modülünü seçin ve **Tamam**'ı seçin.
1. **Konteyner** yuvası için üç nokta (**...**) düğmesini seçin ve **Modül Ekle**'yi seçin.
1. **Modül Ekle** iletişim kutusunda **video oynatıcı** modülünü seçin ve **Tamam**'ı seçin.
1. Video oynatıcı modülüyle ilgili Özellik bölmesinde **video Ekle**'yi seçin.
1. **Ortam Seçicisi** iletişim kutusunda bir video seçin ve sonra **yeni ortam öğesiniyükle**'yi seçin.
1. Dosya Gezgini'nde, bir video dosyası seçin ve sonra **Aç**'ı seçin.
1. **Ortam öğesini karşıya yükle** iletişim kutusunda, gereken bir başlığı ve diğer bilgileri girin ve **Tamam** 'ı seçin.
1. **Ortam Seçicisi** iletişim kutusunda **Kapat**'ı seçin.
1. **Kaydet**'i seçin ve ardından sayfayı önizlemek için **Önizleme**'yi seçin. Sayfada video modülünü görmelisiniz. Modülün davranışını özelleştirmek için ek ayarları değiştirebilirsiniz.
1. Sayfayı iade etmek için **Düzenlemeyi bitir**'i seçin, ardından yayımlamak için **Yayımla**'yı seçin. 

## <a name="additional-resources"></a>Ek kaynaklar

[Modül kitaplığına genel bakış](starter-kit-overview.md)

[Promosyon başlığı modülü](add-alert.md)

[Döngü modülü](add-carousel.md)

[Metin bloğu modülü](add-content-rich-block.md)

[İçerik blok modülü](add-hero-module.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
