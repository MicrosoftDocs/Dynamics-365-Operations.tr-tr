---
title: Dynamics 365 Talent'daki yenilikler veya değişiklikler (19 Kasım 2019)
description: Bu makalede, Microsoft Dynamics 365 Talent'taki yeni veya değişen özellikler açıklanmaktadır.
author: Darinkramer
manager: AnnBe
ms.date: 11/19/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2019-11-19
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 6a26c0039b145f4b6a0940a60256ba7b6644a829
ms.sourcegitcommit: b95df4cea27d6a8f797e0bdd18952bec7dece4ad
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/22/2019
ms.locfileid: "2825014"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-november-19-2019"></a>Dynamics 365 Talent'daki yenilikler veya değişiklikler (19 Kasım 2019)

[!include [banner](includes/banner.md)]

Bu makalede Dynamics 365 Talent'te yeni veya değişen özellikler açıklanmaktadır.

## <a name="changes-in-attract"></a>Attract'te değişiklikler

Bu sürüm, Dynamics 365 Talent: Attract için küçük hata düzeltmeleri içeriyor.

## <a name="changes-in-onboard"></a>Onboard'taki değişiklikler

Bu sürüm, Dynamics 365 Talent: Onboard için küçük hata düzeltmeleri içeriyor.

## <a name="changes-in-core-hr"></a>Core HR içindeki değişiklikler

Bu bölümde açıklanan değişiklikler sürüm numarası 8.1.2621 için geçerlidir. Bazı başlıklardaki parantez içindeki numaralar Microsoft Dynamics Lifecycle Services (LCS) destek numaralarına referans verir.

### <a name="platform-update-31-for-finance-and-operations-apps"></a>Finance and Operations uygulamaları için Platform güncelleştirmesi 31

Daha fazla bilgi için bkz. [Finance and Operations uygulamaları için Platform güncelleştirmesi 31 önizleme özellikleri (Ocak 2020)](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/get-started/whats-new-platform-update-31).

### <a name="feature-management-workspace-383856"></a>Özellik yönetimi çalışma alanı (383856)

**Özellik yönetimi** çalışma alanı, her sürümde teslim edilen özelliklerin bir listesini sağlar. Varsayılan olarak, bu özellikler kapalıdır. Çalışma alanını, bu özellikleri açıp ilgili belgelere bakmak için kullanabilirsiniz. Özellik yönetimi hakkında daha fazla bilgi için bkz. [Özellik yönetimine genel bakış](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview).

Tüm yeni özellikler en az 30 gün boyunca ve genellikle 30-60 gün önizlemede kalır. Önemli özellikler genellikle önizleme dönemini izleyen her yılın Ekim ve Nisan ayında kullanılabilir. **Özellik yönetimi** çalışma alanında yeni yetenekleri gördüğünüz anda bunları açabilirsiniz. Bazı özellikler varsayılan olarak açık olabilir.
 
Bazen bir tümleştirme özelliği varsayılan olarak açıktır ve kapatılamaz (örneğin, **Özellik yönetimi** çalışma alanı).
 
Bir özellik genel olarak kullanılabilir olduğunda üretim ortamlarında açılıp kapatılamayabilir. **Özellik yönetimi** çalışma alanı bir önizleme özelliğinin zorunlu hale gelme zamanını belirtir. Bu tarih genellikle yarıyıllık sürüm planlarına uygun olacak şekilde 1 Ekim veya 1 Nisandır. Zorunlu özellikleri kapatamazsınız. Bir özelliği zorunlu olana kadar tüm ortamlarda kapatıp açabilirsiniz.

### <a name="message-appears-when-canceled-action-exists-for-a-position-382887"></a>Bir konum için iptal edilen eylem varsa ileti görüntülenir (382887)

Belirli bir konumu seçtiğinizde artık aşağıdaki ileti görüntülenmez ve konum için kullanılabilir olan yalnızca iptal edilen eylemdir: **xxxxxx konumu için tamamlanmayan eylem devam ediyor**.

### <a name="in-learning-analytics-the-course-type-and-status-display-incorrect-data-381151"></a>Öğrenme analizinde Kurs türü ve Durum hatalı veriler görüntülüyor (381151)

Bu haftanın sürümü öğrenme analizleri **Kurs türü**ve **Durum**'u doğru şekilde görüntüleyecek şekilde güncelleştirildi.

### <a name="personnel-number-should-display-in-the-new-worker-form-banner-383832"></a>Personel numarası Yeni çalışan formu başlığında görüntülenmeli (383832)

**Yeni çalışan** formunda artık hızlı başvuru için başlıkta **Personel numarası** görüntülenir.

### <a name="position-start-date-determines-the-job-record-to-use-when-retrieving-a-compensation-level-during-hire-350361"></a>Konum başlangıç tarihi, işe alma sırasında ücret düzeyi alınırken kullanılacak İş kaydını belirliyor (350361)

Bu sürümde, **Ücret başlangıç tarihi** yeni işe atanan düzeyi belirler.

### <a name="custom-pick-list-fields-in-the-position-table-arent-synchronized-to-common-data-service-387503"></a>Konum tablosundaki özel çekme listesi alanları Common Data Service ile eşitlenmez (387503)

Bu sürümle, artık çekme listesi öğeleri Common Data Service ile eşitlenir.

### <a name="worker-address-entity-doesnt-synchronize-with-common-data-service-while-importing-new-data-349673"></a>Yeni verileri içe aktarırken çalışan adresi varlığı Common Data Service ile eşitlenmiyor (349673)

Bu haftanın sürümünde, artık adres verileri yeni verileri içe aktarırken Common Data Service ile eşitlenir.

## <a name="in-preview"></a>Ön izlemede

### <a name="print-performance-reviews"></a>Performans incelemelerini yazdırma

Dynamics 365: 2019 sürüm dalgası 2 planındaki [Performans incelemelerini yazdır](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-talent/print-performance-reviews) konusuna bakın.
