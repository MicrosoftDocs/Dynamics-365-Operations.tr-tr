---
title: Kutucuk listesi modülü
description: Bu makale kutucuk listesi modüllerini kapsamaktadır ve Microsoft Dynamics 365 Commerce'un site sayfalarına nasıl ekleneceğini açıklamaktadır.
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
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: 44eb9b82ef9625734c7fe5ccba85207d9f210a00
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8905410"
---
# <a name="tile-list-module"></a>Kutucuk listesi modülü

[!include [banner](includes/banner.md)]

Bu makale kutucuk listesi modüllerini kapsamaktadır ve Microsoft Dynamics 365 Commerce'un site sayfalarına nasıl ekleneceğini açıklamaktadır.

Kutucuk listesi modülü bir döngüdeki kutucuk topluluğudur. Bunlar, ürün kategorilerini veya ürün markalarını görüntüler ve metin aracılığıyla pazarlamak için kullanılır. Örneğin, perakendeci en çok satılan tüm kategorileri tanıtmak için e-ticaret sitesinin giriş sayfasına kutucuk listesi modülü ekleyebilir.

Kutucuk listesi modülü içerik yönetimi sistemindeki (CMS) veriler tarafından yönlendiriliyor. Commerce Headquarters'daki diğer modüllere veya verilere bağlı değildir. Kutucuk listesi modülü, satıcının bir şeyi pazarlamak veya tanıtmak (örneğin, ürünler, kategoriler veya markalar) istediği herhangi bir site sayfasına eklenebilir.

Aşağıdaki resimde, Adventure Works giriş sayfasında kutucuk listesi modülünün ve kutucuk modüllerinin bir örneği gösterilmektedir.

![Adventure Works giriş sayfasında kutucuk listesi modülünün ve kutucuk modüllerinin bir örneği](./media/Tile_list.PNG)

> [!IMPORTANT]
> Kutucuk listesi modülü, Dynamics 365 Commerce 10.0.20 sürümü itibarıyla kullanılabilir.
> Kutucuk listesi modülü Adventure Works temalarında görüntülenir.

## <a name="tile-list-modules-and-themes"></a>Kutucuk listesi modülleri ve temaları

Kutucuk listesi modülü, bir temaya dayalı olarak çeşitli düzen ve stilleri destekleyebilir. Örneğin, Adventure Works temalarında kutucuklar, site kullanıcıları üzerlerine geldiğinde bir animasyon efekti gösterir. Her tema, kutucuk listesi ve kutucuk modülleri için ek özellikler içerebilir. Tema geliştiriciler, kutucuk listesi ve kutucuk modülleri için ek düzenler de derleyebilir.

## <a name="tile-list-module-properties"></a>Kutucuk listesi modülü özellikleri

| Özellik adı | Değerler | Tanım |
|---------------|--------|-------------|
| Başlık       | Başlık metni ve başlık etiketi | Kutucuk listesi modülü için metin başlığı. |

## <a name="tile-module-properties"></a>Kutucuk modülü özellikleri

| Özellik adı | Değerler | Tanım |
|---------------|--------|-------------|
| Görüntü         | Resim dosyası | Bir görüntü, bir ürünü veya kategoriyi sergilemede kullanılabilir. Görüntü, Commerce site oluşturucudaki Ortam Kitaplığı'na yüklenebilir veya mevcut bir görüntü kullanılabilir. |
| Başlık       | Başlık metni ve başlık etiketi (**H1**, **H2**, **H3**, **H4**, **H5** veya **H6**) | Varsayılan olarak başlık için **H2** başlık etiketi kullanılır, ancak başlık etiketi erişilebilirlik gereksinimlerini karşılamak için değiştirilebilir. |
| Paragraf     | Paragraf metni | Modül zengin metin biçimindeki paragraf metnini destekler. Kalın, altı çizili, italik metin ve köprüler gibi bazı temel zengin metin özellikleri desteklenir. Bu yeteneklerden bazıları, modüle uygulanan sayfa teması tarafından geçersiz kılınabilir. |
| Bağla          | Bağlantı metni, bağlantı URL'si, erişilebilir zengin internet uygulamaları (ARIA) etiketi ve **bağlantıyı yeni sekmede aç** | Modüller bir veya daha fazla "eyleme çağrı" bağlantısı destekler. Bir bağlantı eklenirse, bağlantı metni, bir URL ve bir ARIA etiketi gereklidir. ARIA etiketleri erişilebilirlik gereksinimlerini karşılayacak şekilde açıklayıcı olmalıdır. Bağlantılar yeni bir sekmede açılacak şekilde konfigüre edilebilir. |
| Kutucuk bağlantısı     | Bağlantı metni, bağlantı URL'si, ARIA etiketi ve **Bağlantıyı yeni sekmede aç** seçicisi | Bu özellik, bir "eyleme çağrı" bağlantısı tanımlamak için kullanılır. Bir bağlantı eklenirse, bağlantı metni, bir URL ve bir ARIA etiketi gereklidir. ARIA etiketleri erişilebilirlik gereksinimlerini karşılayacak şekilde açıklayıcı olmalıdır. Bağlantılar yeni bir sekmede açılacak şekilde konfigüre edilebilir.|
| Simge          | Görüntü | Bir ürün veya kategori görüntüsünün yanı sıra, bir simge simgesi de eklenebilir. Simge sembolü görüntüsü ürünün veya kategori görüntüsünün üzerinde görünür. |

## <a name="add-a-tile-list-module-to-a-new-page"></a>Yeni sayfaya kutucuk listesi modülü ekleme

Bir yeni sayfaya kutucuk listesi modülü eklemek ve gerekli özellikleri ayarlamak için aşağıdaki adımları izleyin.

1. **Şablonlar**'a gidin ve sitenizin giriş sayfası için pazarlama şablonunu açın (veya yeni bir pazarlama şablonu oluşturun).
1. Varsayılan sayfada **Ana** alanını seçin, üç nokta düğmesini (**...**) ve sonra **Modül ekle**'yi seçin.
1. **Modülleri seç** iletişim kutusunda **Kutucuk listesi** modülünü ve **Tamam**'ı seçin.
1. **Kaydet**'i seçin, şablonu iade etmek için **Düzenlemeyi bitir**'i ve ardından yayımlamak için **Yayımla**'yı seçin.
1. **Sayfalar**'a gidin ve sitenin giriş sayfasını açın (veya pazarlama şablonunu kullanarak yeni bir giriş sayfası oluşturun).
1. Varsayılan sayfada **Ana** alanını seçin, üç nokta düğmesini (**...**) ve sonra **Modül ekle**'yi seçin.
1. **Modülleri seç** iletişim kutusunda **Kutucuk listesi** modülünü ve **Tamam**'ı seçin.
1. Kutucuk listesi modülünün özellik bölmesinde bir başlık ekleyin.
1. **Kutucuk listesi** alanında, üç nokta (**...**) düğmesini seçin ve **Modül ekle**'yi seçin.
1. **Modülleri seç** iletişim kutusunda **Kutucuk modülü** modülünü ve **Tamam**'ı seçin.
1. Kutucuk modülünün özellik bölmesinde bir resim, bir başlık ve bir simge sembolü görüntüsü ekleyin.
1. Ek kutucuk modüllerini gereksinim duyduğunuz şekilde ekleyin ve yapılandırın.
1. **Kaydet**'i seçin ve ardından sayfayı önizlemek için **Önizleme**'yi seçin.
1. Şablonu iade etmek için **Düzenlemeyi bitir**'i seçin, ardından yayımlamak için **Yayımla**'yı seçin.

## <a name="additional-resources"></a>Ek kaynaklar

[Modül kitaplığına genel bakış](starter-kit-overview.md)

[Adventure Works teması](adventure-works-theme.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
