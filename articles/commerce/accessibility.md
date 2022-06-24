---
title: Erişilebilirlik özellikleri ve yetenekleri
description: Bu makale, Microsoft Dynamics 365 Commerce'ün erişilebilirlik özellikleri ve yeterlilikler hakkında bilgi sağlar.
author: BrianShook
ms.date: 04/14/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 8f4e73ebaf6dc3fc6eb97f69df8545c9ab9fa9df
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8853914"
---
# <a name="accessibility-features-and-capabilities"></a>Erişilebilirlik özellikleri ve yetenekleri

[!include [banner](includes/banner.md)]

Bu makale, Microsoft Dynamics 365 Commerce'ün erişilebilirlik özellikleri ve yeterlilikler hakkında bilgi sağlar.

Erişilebilirlik özellikleri ve yetkinlikleri, tüm kullanıcıların hedeflerine ulaşmaları ve eylemlerini gerçekleştirebilmesi için işlevsel araçlar sağlar. Bu geniş kullanıcı yelpazesi, işitme, vizyon, taşınabilirlik veya nöroçeşitlilik için yardımcı araçlar gerektirebilir.

Sitenizdeki çeşitli özellikler Dynamics 365 Commerce, yardımcı işlevler içerecek şekilde sitenizi oluşturmanızı sağlar. Sitenizi tasarlarken, [Microsoft Erişilebilirlik Merkezi](https://www.microsoft.com/accessibility)'nde belirtilen erişilebilirlik işlevselliğinin alanlarını dikkate almalısınız. 

Bu makale, Dynamics 365 Commerce kullanırken göz önünde bulundurmanız gereken bazı ek erişilebilirlik işlevleri alanlarını açıklamaktadır.

## <a name="image-alt-text"></a>Görüntü alternatif metni

Dynamics 365 Commerce uygulamasında, sitenizde kullanılan görüntü ve video varlıklarını izleyebilmesi için yerleşik bir dijital varlık yönetim sistemi vardır. Resim yazıları, açıklamalar ve alternatif metin, seçilen veya karşıya yüklenen bir görüntünün Özellikler bölmesine eklenebilir.

## <a name="video-accessibility"></a>Video erişilebilirliği

Dynamics 365 Commerce dijital varlık yönetimi sistemi, video içeriği için birkaç erişilebilirlik özelliğini destekler. Aşağıdaki tabloda bazı örnekler listelenmiştir.

| Video özelliği               | Tanım |
|-----------------------------|-------------|
| Kapalı açıklamalı alt yazı (CC)      | İşitme engelli veya işitme güçlüğü çeken kullanıcılara yardımcı olmak amacıyla, bir videonun ses ve ses tanımlayıcı öğeleri için gösterilebilecek metin |
| Alt başlıklar                   | Bağlam ipuçları veya iletişim kutusu metnini ekranda gösteren başlık dosyaları |
| Ses transkriptleri           | Bir videonun sesinden üretilen konuşulan sözcüklerin metin dökümü kodu |
| Açıklama sesi           | Ekranda oluşan içeriği veya bağlamı açıklayan birincil olmayan ses kanalı |
| En küçük yaş kapısı            | Bir görüntüleyicinin video görüntülemek için olması gereken minimum yaşı depolayan öznitelik (yalnızca meta veriler) |

### <a name="configure-video-accessibility-elements"></a>Video erişilebilirlik öğelerini konfigüre etme

Commerce'ta sitenizin **Ortam Kitaplığı** bölümünde, Kapalı açıklamalı alt yazılar, normal ses ve tanımlayıcı ses için ayrı dosyalar bulunan video varlıklarını karşıya yükleyebilirsiniz. Bir video varlığı karşıya yüklendiğinde, Kapalı açıklamalı alt yazılar da otomatik olarak oluşturulabilir.

#### <a name="generate-or-upload-closed-caption-files-during-video-asset-upload"></a>Video varlığı karşıya yüklemesi sırasında kapalı açıklamalı altyazı dosyaları oluştur veya karşıya yükler

Video yüklediğinizde, Kapalı açıklamalı alt yazı dosyasının otomatik olarak oluşturulmasını istiyorsanız, bu adımı izleyin.

- **Varlık karşıya yükle** iletişim kutusunda, **otomatik olarak kapalı açıklamalı alt yazılar oluştur** seçeneğini belirleyin. Kapalı bir alt yazı dosyası oluşturuyorsanız, Kapalı açıklamalı alt başlık dosyaları için dosya Seçicisi iletişim kutusunda kullanılamaz.

Video yüklediğinizde, Kapalı açıklamalı alt yazı dosyasını manuel yüklemek istiyorsanız, bu adımı izleyin.

- **Varlık karşıya yükle** iletişim kutusunda, **otomatik olarak kapalı açıklamalı alt yazılar oluştur** seçeneğini temizleyin.

Videonun normal ses veya tanımlayıcı ses dosyalarını karşıya yüklemek için, **Varlık karşıya yükle** iletişim kutusunda dosya seçicisini kullanın.

> [!NOTE]
> Video varlığı karşıya yüklendikten sonra kapalı açıklamalı altyazı, normal ses ve tanımlayıcı ses varlıkları da eklenebilir. **Ortam Kitaplığı**'na gidin, video varlığını seçin ve kullanıma almak için **Düzenle**'yi seçin. Sonra video varlığının özellikler bölmesinde ek varlıkları karşıya yükleyin.

#### <a name="edit-cc-and-audio-transcript-files"></a>Bilgi ve sesli Transkript dosyalarını Düzenle

CC ve sesli Transkript dosyaları doğrudan geliştirme aracında düzenlenebilir. Videoyu kayıttan yürütme işlemi düzenleme sırasında kullanılabilir.

Bilgi ve ses dökümü dosyalarını düzenlemek için aşağıdaki adımları izleyin.

1. **Ortam Kitaplığı**'na gidin ve video varlığının dosya adını seçin. Kapalı açıklamalı alt başlık ve Transkript içeriği Düzenleyicisi görünür.
1. **Düzenle** öğesini seçin.
1. Kapalı açıklamalı alt yazı veya transkript metnini Düzenle.
1. Bitirdiğinizde **Kaydet**'i seçin ve sonra **Düzenlemeyi bitir**'i seçin.
1. Yayımlamaya hazır olduğunuzda **yayınla**'yı seçin.

#### <a name="set-the-minimum-age-attribute"></a>Minimum yaş özniteliğini ayarla

**En küçük yaş** meta veri özniteliği, video varlıklarıyla ilişkilendirilebilir.

Bir video kıymetin **minimum yaş** özniteliğini ayarlamak için aşağıdaki adımları izleyin.

1. **Ortam Kitaplığı**'na gidin ve video varlığını seçin.
1. **Düzenle** öğesini seçin.
1. Video kıymetin Özellikler bölmesinde, **minimum yaş** özniteliğini ayarlayın.

> [!NOTE]
> Özellikler bölmesi yalnızca meta veri öznitelik değerini ayarlamak ve depolamak için kullanılır. Kayıttan yürütme girişimi için bu özniteliği kullanmak üzere özelleştirilmiş modüller oluşturulmalıdır.

## <a name="additional-resources"></a>Ek kaynaklar

[Formlar, ürünler ve denetimlerde erişilebilirlik](/dynamics365/unified-operations/dev-itpro/user-interface/enable-accessibility)

[Microsoft Erişilebilirlik Merkezi](https://www.microsoft.com/accessibility)

[Dynamics 365 Erişilebilirlik Merkezi](/dynamics365/get-started/accessibility/index)

[Uyumluluğa genel bakış](compliance-overview.md)

[Tanımlama bilgisi uyumluluğu](cookie-compliance.md)

[Gizlilik ilkesi sayfası ekleme](add-privacy-page.md)

[İzlenen içerik değişiklikleriyle ilişkili kullanıcı kimliklerini değiştirme](replace-IDs-tracked-changes.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]