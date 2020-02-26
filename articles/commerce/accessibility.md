---
title: Erişilebilirlik özellikleri ve yetenekleri
description: Bu konu, Microsoft Dynamics 365 Commerce'ın erişilebilirlik özellikleri ve yeterlilikler hakkında bilgi sağlar.
author: BrianShook
manager: annbe
ms.date: 01/08/2020
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
ms.author: brshoo
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 3edc6250dd5438be31d80a9d6b0f3b730438ca53
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/01/2020
ms.locfileid: "3001772"
---
# <a name="accessibility-features-and-capabilities"></a>Erişilebilirlik özellikleri ve yetenekleri


[!include [banner](includes/banner.md)]

Bu konu, Microsoft Dynamics 365 Commerce'ın erişilebilirlik özellikleri ve yeterlilikler hakkında bilgi sağlar.

## <a name="overview"></a>Genel Bakış

Erişilebilirlik özellikleri ve yetkinlikleri, tüm kullanıcıların hedeflerine ulaşmaları ve eylemlerini gerçekleştirebilmesi için işlevsel araçlar sağlar. Bu geniş kullanıcı yelpazesi, işitme, vizyon, taşınabilirlik veya nöroçeşitlilik için yardımcı araçlar gerektirebilir.

Sitenizdeki çeşitli özellikler Dynamics 365 Commerce, yardımcı işlevler içerecek şekilde sitenizi oluşturmanızı sağlar. Sitenizi tasarlarken, [Microsoft Erişilebilirlik Merkezi](https://www.microsoft.com/accessibility)'nde belirtilen erişilebilirlik işlevselliğinin alanlarını dikkate almalısınız. 

Bu konu, Dynamics 365 Commerce kullanırken göz önünde bulundurmanız gereken bazı ek erişilebilirlik işlevleri alanlarını açıklamaktadır.

## <a name="image-alt-text"></a>Görüntü alternatif metni

Dynamics 365 Commerce uygulamasında, sitenizde kullanılan görüntü ve video varlıklarını izleyebilmesi için yerleşik bir dijital varlık yönetim sistemi vardır. Resim yazıları, açıklamalar ve alternatif metin, seçilen veya karşıya yüklenen bir görüntünün Özellikler bölmesine eklenebilir.

## <a name="video-accessibility"></a>Video erişilebilirliği

Dynamics 365 Commerce dijital varlık yönetimi sistemi, video içeriği için birkaç erişilebilirlik özelliğini destekler. Aşağıdaki tabloda bazı örnekler listelenmiştir.

| Video özelliği               | Tanım |
|-----------------------------|-------------|
| Kapalı açıklamalı alt yazı (CC)      | İşitme güçlüğü çeken kullanıcılara yardımcı olmak amacıyla, bir videonun ses ve ses tanımlayıcı öğeleri için gösterilebilecek metin |
| Alt başlıklar                   | Bağlam ipuçları veya iletişim kutusu metnini ekranda gösteren başlık dosyaları |
| Ses transkriptleri           | Bir videonun sesinden üretilen konuşulan sözcüklerin metin dökümü kodu |
| Açıklama sesi           | Ekranda oluşan içeriği veya bağlamı açıklayan birincil olmayan ses kanalı |
| En küçük yaş kapısı            | Bir görüntüleyicinin video görüntülemek için olması gereken minimum yaşı depolayan öznitelik (yalnızca meta veriler) |

### <a name="configure-video-accessibility-elements"></a>Video erişilebilirlik öğelerini konfigüre etme

Dynamics 365 Commerce'te sitenizin **Varlıklar** bölümünde, Kapalı açıklamalı alt yazılar, normal ses ve tanımlayıcı ses için ayrı dosyalar bulunan video varlıklarını karşıya yükleyebilirsiniz. Bir video varlığı karşıya yüklendiğinde, Kapalı açıklamalı alt yazılar da otomatik olarak oluşturulabilir.

#### <a name="generate-or-upload-closed-caption-files-during-video-asset-upload"></a>Video varlığı karşıya yüklemesi sırasında kapalı açıklamalı altyazı dosyaları oluştur veya karşıya yükler

Video yüklediğinizde, Kapalı açıklamalı alt yazı dosyasının otomatik olarak oluşturulmasını istiyorsanız, bu adımı izleyin.

- **Varlık karşıya yükle** iletişim kutusunda, **otomatik olarak kapalı açıklamalı alt yazılar oluştur** seçeneğini belirleyin. Kapalı bir alt yazı dosyası oluşturuyorsanız, Kapalı açıklamalı alt başlık dosyaları için dosya Seçicisi iletişim kutusunda kullanılamaz.

Video yüklediğinizde, Kapalı açıklamalı alt yazı dosyasını manuel yüklemek istiyorsanız, bu adımı izleyin.

- **Varlık karşıya yükle** iletişim kutusunda, **otomatik olarak kapalı açıklamalı alt yazılar oluştur** seçeneğini temizleyin.

Videonun normal ses veya tanımlayıcı ses dosyalarını karşıya yüklemek için, **Varlık karşıya yükle** iletişim kutusunda dosya seçicisini kullanın.

> [!NOTE]
> Video varlığı karşıya yüklendikten sonra kapalı açıklamalı altyazı, normal ses ve tanımlayıcı ses varlıkları da eklenebilir. **Varlıklara** gidin, video varlığını seçin ve teslim edin ve sonra video kıymete ait Özellikler bölmesinde ek kıymetleri karşıya yükleyin.

#### <a name="edit-cc-and-audio-transcript-files"></a>Bilgi ve sesli Transkript dosyalarını Düzenle

CC ve sesli Transkript dosyaları doğrudan geliştirme aracında düzenlenebilir. Videoyu kayıttan yürütme işlemi düzenleme sırasında kullanılabilir.

Bilgi ve ses dökümü dosyalarını düzenlemek için aşağıdaki adımları izleyin.

1. **Varlıklara** gidin, video varlığını seçin ve sonra **Düzenle CC/Transkript**'i seçin. Kapalı açıklamalı alt başlık ve Transkript içeriği Düzenleyicisi görünür.
1. **Ödeme yap** seçin.
1. Kapalı açıklamalı alt yazı veya transkript metnini Düzenle.
1. Bitirdiğinizde **Kaydet**'i seçin ve sonra **Giriş**'i seçin.
1. Yayımlamaya hazır olduğunuzda **yayınla**'yı seçin.

#### <a name="set-the-minimum-age-attribute"></a>Minimum yaş özniteliğini ayarla

**En küçük yaş** meta veri özniteliği, video varlıklarıyla ilişkilendirilebilir.

Bir video kıymetin **minimum yaş** özniteliğini ayarlamak için aşağıdaki adımları izleyin.

1. **Varlıklara** gidin ve video varlığını seçin.
1. **Ödeme yap** seçin.
1. Video kıymetin Özellikler bölmesinde, **minimum yaş** özniteliğini ayarlayın.

> [!NOTE]
> Özellikler bölmesi yalnızca meta veri öznitelik değerini ayarlamak ve depolamak için kullanılır. Kayıttan yürütme girişimi için bu özniteliği kullanmak üzere özelleştirilmiş modüller oluşturulmalıdır.

## <a name="additional-resources"></a>Ek kaynaklar

[Formlar, ürünler ve denetimlerde erişilebilirlik](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/user-interface/enable-accessibility)

[Microsoft Erişilebilirlik Merkezi](https://www.microsoft.com/accessibility)

[Dynamics 365 Erişilebilirlik Merkezi](https://docs.microsoft.com/dynamics365/get-started/accessibility/index)

[Uyumluluğa genel bakış](compliance-overview.md)

[Çerez uyumluluğu](cookie-compliance.md)

[Gizlilik ilkesi sayfası ekle](add-privacy-page.md)
