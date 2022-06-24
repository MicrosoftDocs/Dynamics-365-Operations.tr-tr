---
title: Günlüklerde ertelenen vergi hesaplamasını etkinleştirme
description: Bu makalede, günlük satırlarının sayısı çok fazla olduğunda vergi hesaplama performansını artırmaya yardımcı olmak için Ertelenen vergi hesaplaması özelliğinin nasıl etkinleştirileceği açıklanmaktadır.
author: EricWang
ms.date: 09/18/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TaxTable
audience: Application User
ms.reviewer: kfend
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2019-09-18
ms.dyn365.ops.version: 10.0.7
ms.openlocfilehash: 02a038318d4c0fb44b6fcc4bb159ea87c2e9368a
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8887933"
---
# <a name="enable-delayed-tax-calculation-on-journals"></a>Günlüklerde ertelenen vergi hesaplamasını etkinleştirme
[!include [banner](../includes/banner.md)]


Bu makalede, günlüklerde satış vergisi hesaplamasını nasıl erteleyebileceğiniz açıklanmaktadır. Bu özellik, birçok günlük satırı olduğunda vergi hesaplamalarında performansın artırılmasına yardımcı olur.

Varsayılan olarak, vergiyle ilgili alanlar her güncelleştirildiğinde, günlük satırlarındaki satış vergisi tutarları hesaplanır. Bu alanlar, satış vergisi grupları ve madde satış vergisi grupları için alanlar içerir. Günlük satırındaki her güncelleştirme vergi tutarlarının tüm günlük satırlarında yeniden hesaplanmasını sağlar. Bu davranış kullanıcının gerçek zamanlı olarak hesaplanan vergi tutarlarının görebilmesine yardımcı olmakla birlikte, günlük satırlarının sayısı çok büyükse performansı da etkileyebilir.

Ertelenen vergi hesaplaması özelliği günlüklerde vergi hesaplamasını ertelemenizi sağlar ve bu nedenle performans sorunlarını gidermeye yardımcı olur. Bu özellik açık olduğunda, vergi tutarları yalnızca kullanıcı **Satış Vergisi**'ni seçerse veya günlüğü deftere naklederse hesaplanır.

Satış vergilerinin hesaplamasını üç düzeyde erteleyebilirsiniz:

- Tüzel kişilik
- Günlük adı
- Günlük başlığı

Sistem, günlük başlığı ayarına öncelik verir. Varsayılan olarak, bu ayar günlük adından alınır. Varsayılan olarak, günlük adı oluşturulduğunda, günlük adı içina yar **Genel muhasebe parametreleri** sayfasındaki ayardan alınır. Aşağıdaki bölümlerde tüzel kişiler, günlük adları ve günlük başlıkları için ertelenen vergi hesaplamasının nasıl etkinleştirileceği açıklanmaktadır.

## <a name="turn-on-delayed-tax-calculation-at-the-legal-entity-level"></a>Tüzel kişilik düzeyinde ertelenen vergi hesaplamasını açma

1. **Genel muhasebe\> Genel muhasebe ayarı \> Genel muhasebe parametreleri**'ne gidin.
2. **Satış vergisi** sekmesinde, **Genel** hızlı sekmesi üzerinde **Ertelenen vergi hesaplaması** seçeneğini **Evet** olarak ayarlayın.

![Genel muhasebe parametrelerini görüntüsü.](media/delayed-tax-calculation-gl.png)

## <a name="turn-on-delayed-tax-calculation-at-the-journal-name-level"></a>Günlük adı düzeyinde ertelenen vergi hesaplamasını açma

1. **Genel muhasebe \> Günlük ayarı \> Günlük adları**'na gidin.
2. **Genel** hızlı sekmesinde, **Satış vergisi** bölümünde **Ertelenen vergi hesaplaması** seçeneğini **Evet** olarak ayarlayın.

![Günlük adları görüntüsü.](media/delayed-tax-calculation-journal-name.png)

## <a name="turn-on-delayed-tax-calculation-at-the-journal-header-level"></a>Günlük başlığı düzeyinde ertelenen vergi hesaplamasını açma

1. **Genel muhasebe \> Günlük girişleri \> Genel günlükler**.
2. **Yeni**'yi seçin.
3. Bir günlük adı seçin.
4. **Kurulum** sekmesinde, **Ertelenen vergi hesaplaması** seçeneğini **Evet** olarak ayarlayın.

![Genel günlük sayfası resmi.](media/delayed-tax-calculation-journal-header.png)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
