---
title: Belge durumları ve yaşam döngüsü
description: Bu makale, Microsoft Dynamics 365 Commerce içindeki sayfa öğelerinin çeşitli belge durumlarını kapsamaktadır.
author: phinneyridge
ms.date: 10/09/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: niholman
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.custom: intro-internal
ms.search.industry: ''
ms.search.form: ''
ms.openlocfilehash: 350b3236eec6ad6520025bf44b22f12366f1e266
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/12/2022
ms.locfileid: "9269929"
---
# <a name="document-states-and-lifecycle"></a>Belge durumları ve yaşam döngüsü

[!include [banner](includes/banner.md)]

Bu makale, Microsoft Dynamics 365 Commerce içindeki sayfa öğelerinin çeşitli belge durumlarını kapsamaktadır.

## <a name="document-state-descriptions"></a>Belge durumu açıklamaları

[Sayfa öğeleri](page-elements-overview.md) makalesi, içerik yönetim sistemindeki (CMS) çeşitli belge türlerini listeler. Bu belge türlerinin, geliştirme aracında birçok durumu olabilir. Belge durumları veri çakışmalarını önlemeye ve sürüm kontrolünü uygulamaya yardımcı olur. Bunlar, belgeleri kimlerin değiştirebileceğini, belgelerin ne zaman değiştirilebileceğini ve değişikliklerin diğer kişiler tarafından ne zaman görüntülenebileceğini belirler.

Aşağıdaki tablo, ticari sayfa öğelerinin olası belge durumlarını gösterir.

| Belge durumu      | Site oluşturucu eylemi        | Tanım                                                  |
| ------------------- | -------------------------- | ------------------------------------------------------------ |
| Kullanıma alındı         | **Düzenle** öğesini seçin.           | Uygun belge kullanımınıza alınır. Belge bu durumundayken, diğer kimliği doğrulanmış sistem kullanıcıları tarafından değiştirilemez ve belgede yaptığınız tüm değişiklikler yalnızca size gösterilir. |
| Kaydedildi               | **Kaydet**'i seçin.           | Kullanıma alınmış belgede yapılan değişiklikler veritabanına kaydedilir ancak belge henüz iade edilmez veya yayımlanmaz. Kaydedilen değişiklikler, yazar **Düzenlemeyi bitir** seçeneğini seçene kadar diğer kimliği doğrulanmış sistem kullanıcıları tarafından görülemez. Bunlar, öğe yayımlanana kadar harici kullanıcılar tarafından görülemez. |
| Kullanıma alma atıldı | **Düzenlemeleri at**'ı seçin.  | Kullanıma aldığınız belgede yapılan tüm değişiklikler atılır ve öğe iade edilen son sürüme geri döner. |
| Teslim edildi          | **Düzenlemeyi bitir**'i seçin. | Düzenlenen belge iade edilir. Tüm değişiklikler, kimliği doğrulanmış diğer sistem kullanıcıları tarafından görülebilir ve bu kullanıcılar belgeyi düzenleyebilir. Her iade etme öğenin geçmişinde bir belge sürümü kaydı oluşturur. |
| Yayınlanmış           | **Yayımla**'yı seçin.        | Belge yayımlanır ve değişiklikler yayımlanmış sitenize itilir ve harici kullanıcılar tarafından keşfedilebilir hale gelir. Öğeler yalnızca **Düzenlemeyi bitir** seçilerek iade edilmiş olmaları durumunda yayımlanabilir. |

## <a name="additional-resources"></a>Ek kaynaklar

[İçerik ekleme yolları](add-manage-content.md)

[Sayfa modeli sözlüğü](page-elements-overview.md)

[Yayımlama gruplarıyla çalışma](publish-groups.md)

[Kanallar arası paylaşımı etkinleştirme ve kullanma](cross-channel-sharing.md)

[Modüllerle çalışma](work-with-modules.md)

[Parçalarla çalışma](work-with-fragments.md)

[Şablonlar ve düzenlere genel bakış](templates-layouts-overview.md)

[Site gezintisini özelleştirme](customize-site-navigation.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
