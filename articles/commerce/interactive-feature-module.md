---
title: Etkileşimli özellik modülü
description: Bu konu etkileşimli özellik modüllerini kapsamaktadır ve Microsoft Dynamics 365 Commerce'un site sayfalarına nasıl ekleneceğini açıklamaktadır.
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
ms.openlocfilehash: 3ab325189812289390740e31fd673ee9892f9759
ms.sourcegitcommit: ccb39767bd3430c24f4653c26560bba2cd66553c
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/19/2022
ms.locfileid: "8780751"
---
# <a name="interactive-feature-module"></a>Etkileşimli özellik modülü

[!include [banner](includes/banner.md)]

Bu konu etkileşimli özellik modüllerini kapsamaktadır ve Microsoft Dynamics 365 Commerce'un site sayfalarına nasıl ekleneceğini açıklamaktadır.

Etkileşimli özellik modülleri, bir görüntü ve metin birleşimi kullanarak çoklu ürün kategorilerini veya ürün markalarını pazarlamak için kullanılabilen mozaik benzeri modüllerdir. Örneğin, perakendeci en çok satılan kategorileri tanıtmak için e-ticaret sitesinin giriş sayfasına etkileşimli özellik modülü ekleyebilir. Etkileşimli Özellik modülü kutu listesi modülüne benzer ancak farklı bir düzene ve farklı bir etkileşim işlevine sahiptir.

Her etkileşimli özellik modülü, etkileşimli özellik öğesi modülleri topluluğudur. Her özellik öğesi modülü içerik yönetimi sistemindeki (CMS) veriler tarafından yönlendirilir. Commerce Headquarters'daki diğer modüllere veya verilere bağlı değildir. Etkileşimli özellik modülü, satıcının bir şeyi pazarlamak veya tanıtmak (örneğin, ürünler, kategoriler veya markalar) istediği herhangi bir site sayfasına eklenebilir.

> [!IMPORTANT]
> - Etkileşimli özellik modülü, Dynamics 365 Commerce 10.0.20 sürümü itibarıyla kullanılabilir.
> - Etkileşimli özellik modülü Adventure Works temalarında görüntülenir.

Aşağıdaki resimde, Adventure Works giriş sayfasında Etkileşimli özellik modülünün bir örneği gösterilmektedir.

![Adventure Works giriş sayfasında Etkileşimli özellik modülünün bir örneği](./media/Feature.PNG)

## <a name="interactive-feature-module-and-themes"></a>Etkileşimli özellik modülü ve temalar

Etkileşimli özellik modülü, bir temaya dayalı olarak çeşitli düzen ve stilleri destekleyebilir. Örneğin, Adventure Works temalarında, etkileşimli özellik modülünün, bir site kullanıcısı öğenin üzerine geldiğinde animasyon efektlerini gösteren iki sütunlu bir düzen vardır. Etkileşimli özellik modülü, iki sütunlu düzende düzenlenmiş birçok görüntü için en iyi duruma getirilmiştir.

## <a name="interactive-feature-module-properties"></a>Etkileşimli özellik modülü özellikleri

| Özellik adı | Değerler | Tanım |
|---------------|--------|-------------|
| Başlık       | Başlık metni ve başlık etiketi (**H1**, **H2**, **H3**, **H4**, **H5** veya **H6**) | Etkileşimli özellik modülü için metin başlığı. |

## <a name="interactive-feature-item-module-properties"></a>Etkileşimli özellik öğesi modülü özellikleri

| Özellik adı | Değerler | Tanım |
|---------------|--------|-------------|
| Görüntü         | Resim dosyası | Bir ürünü veya kategoriyi temsil eden resim. Görüntü, Commerce site oluşturucudaki Ortam Kitaplığı'na yüklenebilir veya mevcut bir görüntü kullanılabilir. |
| Başlık       | Başlık metni ve başlık etiketi (**H1**, **H2**, **H3**, **H4**, **H5** veya **H6**) | Varsayılan olarak başlık için **H2** başlık etiketi kullanılır, ancak başlık etiketi erişilebilirlik gereksinimlerini karşılamak için değiştirilebilir. |
| Paragraf     | Paragraf metni | Modül zengin metin biçimindeki paragraf metnini destekler. Kalın, altı çizili, italik metin ve köprüler gibi bazı temel zengin metin özellikleri desteklenir. Bu yeteneklerden bazıları, modüle uygulanan sayfa teması tarafından geçersiz kılınabilir. |
| Bağla          | Bağlantı metni, bağlantı URL'si, Erişilebilir Zengin İnternet Uygulamaları (ARIA) etiketi ve **Bağlantıyı yeni sekmede aç** seçicisi | Modül bir veya daha fazla "eyleme çağrı" bağlantısı destekler. Bir bağlantı eklenirse, bağlantı metni, bir URL ve bir ARIA etiketi gereklidir. ARIA etiketleri erişilebilirlik gereksinimlerini karşılayacak şekilde açıklayıcı olmalıdır. Bağlantılar yeni bir sekmede açılacak şekilde konfigüre edilebilir. |

## <a name="add-an-interactive-feature-module-to-a-new-page"></a>Yeni sayfaya Etkileşimli özellik modülü ekleme

Yeni sayfaya etkileşimli özellik modülü eklemek ve Commerce site oluşturucuda gerekli özellikleri ayarlamak için aşağıdaki adımları izleyin.

1. **Şablonlar**'a gidin ve sitenizin giriş sayfası için pazarlama şablonunu açın (veya yeni bir pazarlama şablonu oluşturun).
1. Varsayılan sayfada **Ana** alanını seçin, üç nokta düğmesini (**...**) ve sonra **Modül ekle**'yi seçin.
1. **Modülleri seç** iletişim kutusunda **Etkileşimli özellik** modülünü seçin ve **Tamam**'ı seçin.
1. **Kaydet**'i seçin, şablonu iade etmek için **Düzenlemeyi bitir**'i ve ardından yayımlamak için **Yayımla**'yı seçin.
1. **Sayfalar**'a gidin ve sitenin giriş sayfasını açın (veya pazarlama şablonunu kullanarak yeni bir giriş sayfası oluşturun).
1. Varsayılan sayfada **Ana** alanını seçin, üç nokta düğmesini (**...**) ve sonra **Modül ekle**'yi seçin.
1. **Modülleri seç** iletişim kutusunda **Modülleri seç** altında **Etkileşimli özellik** modülünü ve **Tamam**'ı seçin.
1. Etkileşimli özellik modülünün özellik bölmesinde bir başlık ekleyin.
1. **Etkileşimli özellik** alanında, üç nokta (**...**) düğmesini seçin ve **Modül ekle**'yi seçin.
1. **Modülleri seç** iletişim kutusunda **Etkileşimli özellik öğesi** modülünü seçin ve **Tamam**'ı seçin.
1. Etkileşimli özellik öğesi modülünün özellik bölmesinde bir resim, başlık metni, paragraf metni ve bir URL ekleyin.
1. Etkileşimli özellik öğesi modüllerini gereksinim duyduğunuz şekilde ekleyin ve yapılandırın.
1. **Kaydet**'i seçin ve ardından sayfayı önizlemek için **Önizleme**'yi seçin.
1. Şablonu iade etmek için **Düzenlemeyi bitir**'i seçin, ardından yayımlamak için **Yayımla**'yı seçin.

## <a name="additional-resources"></a>Ek kaynaklar

[Modül kitaplığına genel bakış](starter-kit-overview.md)

[Adventure Works teması](adventure-works-theme.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
