---
title: Video oynatıcı modülü
description: Bu konu vide oynatıcı modüllerini kapsamaktadır ve Microsoft Dynamics 365 Commerce'un site sayfalarına nasıl ekleneceğini açıklamaktadır.
author: anupamar-ms
manager: annbe
ms.date: 12/02/2019
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
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 1c78583f39dbacdc7b38e89c33e67ae23731bf8a
ms.sourcegitcommit: 96bfc20eb748f4090a2b5e1ff9f54997d5a5d359
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 12/04/2019
ms.locfileid: "2885913"
---
# <a name="video-player-module"></a>Video oynatıcı modülü

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

Bu konu vide oynatıcı modüllerini kapsamaktadır ve Microsoft Dynamics 365 Commerce'un site sayfalarına nasıl ekleneceğini açıklamaktadır.

## <a name="overview"></a>Genel Bakış

Video oynatımını desteklemek için video oynatıcı modülleri kullanılır. Mağaza başlangıç kitinde iki adet video oynatıcı modülü bulunmaktadır: Ortam video oynatıcı modülü ve video oynatıcı modülü. Her iki oyuncu da .mp4 ortam türünü destekler.

## <a name="ambient-video-player-module"></a>Ortam Video oynatıcı modülü

Ortam video oynatıcı modülü kısa bilgi veren videoları destekler. Bu, beş saniyeden az uzunlukta olan videolar için kullanılmalıdır. Bu oynatıcı, oynat ve Duraklat gibi sınırlı video kayıttan yürütme yeteneklerini destekler.

### <a name="examples-of-ambient-video-player-modules-in-e-commerce"></a>E-ticaret'da ortam video oynatıcı modülleri örnekleri

- Giriş sayfasında yeni ürünleri vurgulayan kısa bilgilendirici videolar
- Ürün ayrıntıları sayfasında ürün özelliklerini vurgulayan kısa bilgilendirici videolar

### <a name="ambient-video-player-module-properties"></a>Ortam Video oynatıcı modülü özellikleri

| Özellik adı     | Değer                 | Tanım |
|-------------------|-----------------------|-------------|
| Otomatik yürüt          | **Doğru** veya **yanlış** | Değer **doğru** olarak ayarlandığında, video otomatik olarak yürütülür. |
| Sesi Kapat              | **Doğru** veya **yanlış** | Değer **doğru** olarak ayarlandığında, ses kapatılır. Bu oynatıcı için varsayılan değer **doğru**'dur. Google Chrome tarayıcıda, Otomatik yürütme videoları varsayılan olarak kapalı ve ses ancak videoyu el ile oynadığında yürütülür. |
| Döngü              | **Doğru** veya **yanlış** | Değer **doğru** olarak ayarlandığında, video döngü olarak tekrarlanır. |
| Ortam             |  Video dosya yolu ve adı. | Video oynatıcı tarafından oynanan video dosyası. |
| Kayıttan yürütme denetimleri | **Doğru** veya **yanlış** | Değer **doğru** olarak ayarlandığında, videoda bir Oynat/Duraklat düğmesi görüntülenir. Değer **yanlış** olarak ayarlanırsa, Oynat/Duraklat düğmesi gösterilmez, ancak kullanıcılar klavyeyi kullanarak videoyu hala duraklatabilir ve devam ettirebilirler. |

## <a name="video-player-module"></a>Video oynatıcı modülü

Video oynatıcı modülü bir e-ticaret sitesinde videoları sergileyebilecek şekilde kullanılabilir. Yürüt, Duraklat, tam boyut modu ve kapalı açıklamalı alt yazılar gibi tüm kayıttan yürütme yeteneklerini destekler. Video oynatıcı modülü, Microsoft erişilebilirlik standartlarını karşılamak için kapalı açıklamalı alt yazıların özelleştirmesini de destekler. Örneğin, yazı tipi boyutunu ve arka plan rengini özelleştirebilirsiniz.

Video oynatıcı modülü ikincil ses parçalarını da destekler. Bir video karşıya yüklendiğinde, ikincil bir ses parçası da karşıya yüklenebilir. Böylece, bir kullanıcı seçerse, video oynatıcı modülü ikincil ses kanalını yürütebilir.

### <a name="examples-of-video-player-modules-in-e-commerce"></a>E-ticaret'da video oynatıcı modülleri örnekleri

- Ürün Ayrıntıları sayfalarındaki veya pazarlama sayfalarındaki yönerge videoları
- Tüm pazarlama sayfaları üzerindeki ilkelerle ilgili videolar veya promosyon videoları
- Ürün Ayrıntıları sayfalarındaki veya pazarlama sayfalarındaki ürün özelliklerini vurgulayan pazarlama videoları

### <a name="video-player-module-properties"></a>Video oynatıcı modülü özellikleri

| Özellik adı         | Değer                               | Tanım |
|-----------------------|-------------------------------------|-------------|
| Otomatik Yürütme             | **Doğru** veya **yanlış**               | Değer **doğru** olarak ayarlandığında, video otomatik olarak yürütülür. |
| Sesi Kapat                  | **Doğru** veya **yanlış**               | Değer **doğru** olarak ayarlandığında, ses kapatılır. Bu oynatıcı için varsayılan değer **yanlış**'tır. Chrome tarayıcıda, Otomatik yürütme videoları varsayılan olarak kapalı ve ses ancak videoyu el ile oynadığında yürütülür. |
| Döngü                  | **Doğru** veya **yanlış**               | Değer **doğru** olarak ayarlandığında, video döngü olarak tekrarlanır. |
| Ortam                 | Video dosya yolu ve adı. | Video oynatıcı tarafından oynanan video dosyası. |
| Kayıttan yürütme denetimleri     | **Doğru** veya **yanlış**               | Değer **doğru** olarak ayarlandığında, videoda bir Oynat/Duraklat düğmesi görüntülenir. Değer **yanlış** olarak ayarlanırsa, Oynat/Duraklat düğmesi gösterilmez, ancak kullanıcılar klavyeyi kullanarak videoyu hala duraklatabilir ve devam ettirebilirler. |
| Tam ekran oynat       | **Doğru** veya **yanlış**               | Değer **doğru** olarak ayarlandığında, video tam ekran modunda yürütülür. |
| Denetimler              | **Doğru** veya **yanlış**               | Değer **doğru** olarak ayarlandığında, tüm denetimler gösterilir. Bu denetimler, oynat ve Duraklat düğmelerini, ilerleme göstergesini ve açıklamalı alt yazıları içerir. |
| Poster çerçevesini gizle     | **Doğru** veya **yanlış**               | Videoda poster karesi olabilir. Bu özelliğin değeri **doğru** olarak ayarlandığında, poster çerçevesi gizlenir. |
| Maske düzeyi            | **0** ile **100** arasında bir sayı | Stil oluşturma için videoya uygulanan maske. |
| Tam ekran simge stili | **Kare** veya **ok**             | Video oynatıcıda gösterilen tam ekran simgesinin stili. |

## <a name="add-a-video-player-module-to-a-page"></a>Sayfaya video oynatıcı modülü ekleme

Bir yeni sayfaya video oynatma modülü eklemek ve gerekli özellikleri ayarlamak için aşağıdaki adımları izleyin.

1. **Video oynatıcı şablonu** adlı bir sayfa şablonu oluşturun.
1. Varsayılan sayfanın **ana** yuvasına bir konteyner modülü ekleyin.
1. Konteyner modülünde, video oynatıcı ve ortam video oynatıcı modülleri ekleyin.
1. Şablonu giriş yapın ve yayımlayın.
1. **Video oynatıcı sayfası** adlı bir sayfa oluşturmak için yeni oluşturduğunuz video oynatıcı şablonunu kullanın.
1. Yeni sayfanın **ana** yuvasına bir ortam video oynatıcı modülü ekleyin.
1. Ortam video oynatıcı modülünün ayarlarında, **ortam**'a gidin ve bir video dosyası yükleyin. **Otomatik yürüt** **döngü** ve diğer özellikleri gereksinim duyduğunuz gibi değiştirebilirsiniz.
1. Sayfayı kaydet ve önizleyin.
1. Yeni sayfanın **ana** yuvasına bir video oynatıcı modülü ekleyin.
1. Video oynatıcı modülünün ayarlarında, **ortam**'a gidin ve bir video dosyası yükleyin.
1. Sayfayı kaydet ve önizleyin. Sayfada iki video modülü de görmelisiniz. Her modülün davranışını özelleştirmek için ek ayarları değiştirebilirsiniz.
1. Sayfayı giriş yapın ve yayımlayın.

## <a name="additional-resources"></a>Ek kaynaklar

[Başlangıç paketine genel bakış](starter-kit-overview.md)

[Uyarı modülü](add-alert.md)

[Döngü modülü](add-carousel.md)

[İçerik zengin blok modülü](add-content-rich-block.md)

[İçerik yerleşimi modülü](add-content-placement-modules.md)

[Özellik modülü](add-feature-module.md)

[Hero modülü](add-hero-module.md)
