---
title: Belge durumları ve yaşam döngüsü
description: Bu konu, Microsoft Dynamics 365 Commerce içindeki sayfa öğelerinin çeşitli belge durumlarını kapsamaktadır.
author: phinneyridge
manager: annbe
ms.date: 10/31/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.search.industry: ''
ms.author: niholman
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: a34d10edbf84ac1814afdc7107727aea68a303e0
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/06/2019
ms.locfileid: "2770447"
---
# <a name="document-states-and-lifecycle"></a>Belge durumları ve yaşam döngüsü

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

Bu konu, Microsoft Dynamics 365 Commerce içindeki sayfa öğelerinin çeşitli belge durumlarını kapsamaktadır.

## <a name="document-state-descriptions"></a>Belge durumu açıklamaları

[Sayfa öğeleri](page-elements-overview.md) konusu, içerik yönetim sistemindeki (CMS) çeşitli belge türlerini listeler. Bu belge türlerinin, geliştirme aracında birçok durumu olabilir. Belge durumları veri çakışmalarını önlemeye ve sürüm kontrolünü uygulamaya yardımcı olur. Bunlar, belgeleri kimlerin değiştirebileceğini, belgelerin ne zaman değiştirilebileceğini ve değişikliklerin diğer kişiler tarafından ne zaman görüntülenebileceğini belirler.

Aşağıdaki tablo, ticari sayfa öğelerinin olası belge durumlarını gösterir.

| Belge durumu | Tanım |
|---|---|
| Kullanıma alındı | Bir CMS öğesi size teslim edildiğinde, diğer kimliği doğrulanmış sistem kullanıcıları tarafından düzenlenemez. Öğede yaptığınız tüm değişiklikler yalnızca size görünebilir. |
| Teslim edildi | Bir CMS öğesi iade edildiğinde, tüm değişiklikler kimliği doğrulanmış diğer sistem kullanıcıları tarafından görülebilir ve bu kullanıcılar öğeyi kullanıma alabilir ve düzenleyebilir. Her iade etme öğenin geçmişinde bir belge sürümü kaydı oluşturur. |
| Yayınlanmış | Bir CMS öğesi yayımlandığında, bunlar canlı siteniz ile gönderilir ve internette kimliği doğrulanmamış dış kullanıcılar tarafından bulunabilir duruma gelir. Maddeler yalnızca iade edilmiş olmaları halinde yayımlanabilir. |
| Kaydedildi | Kullanıma alınmış CMS öğesine yapılan değişiklikler, öğe iade edilene veya yayımlanmadan önce CMS'e kaydedilebilir. Bu kaydedilen değişiklikler, madde iade edilene kadar, diğer kimliği doğrulanmış sistem kullanıcıları tarafından görülemez. Bunlar, öğe yayımlanana kadar harici kullanıcılar tarafından görülemez. |
| Kullanıma alma atıldı | Kullanıma aldığınız bir CMS öğesi iptal edildiğinde, kaydedilen tüm değişiklikler silinir ve öğe en son iade edilen sürüme döner. |

## <a name="additional-resources"></a>Ek kaynaklar

[İçerik ekleme yolları](add-manage-content.md)

[Sayfa modeli sözlüğü](page-elements-overview.md)

[Modüllerle çalışma](work-with-modules.md)

[Parçalarla çalışma](work-with-fragments.md)

[Şablonlar ve düzenlere genel bakış](templates-layouts-overview.md)

[Site gezintisini özelleştirme](customize-site-navigation.md)
