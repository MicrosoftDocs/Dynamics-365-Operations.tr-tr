---
title: Dynamics 365 Talent'daki yenilikler veya değişiklikler (10 Aralık 2019)
description: Bu makalede, Microsoft Dynamics 365 Talent'taki yeni veya değişen özellikler açıklanmaktadır.
author: Darinkramer
manager: AnnBe
ms.date: 12/10/2019
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
ms.search.validFrom: 2019-12-10
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 18f86f5d87b780d5d4ffc83330d389077987dda6
ms.sourcegitcommit: e89bb3e5420a6ece84f4e80c11e360b4a042f59d
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/17/2020
ms.locfileid: "4528183"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-december-10-2019"></a>Dynamics 365 Talent'daki yenilikler veya değişiklikler (10 Aralık 2019)

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Bu konuda, Dynamics 365 Talent'daki yeni veya değişen özellikler açıklanmaktadır.

## <a name="changes-in-attract"></a>Attract'te değişiklikler

Bu sürüm, Dynamics 365 Talent: Attract için küçük hata düzeltmeleri içeriyor.

## <a name="changes-in-onboard"></a>Onboard'taki değişiklikler

Bu sürüm, Dynamics 365 Talent: Onboard için küçük hata düzeltmeleri içeriyor.

## <a name="changes-in-core-hr"></a>Core HR içindeki değişiklikler

Bu bölümde açıklanan değişiklikler sürüm numarası 8.1.2660 için geçerlidir. Bazı başlıklardaki parantez içindeki numaralar Microsoft Dynamics Lifecycle Services (LCS) destek numaralarına referans verir.

### <a name="feature-management-workspace"></a>Özellik yönetimi çalışma alanı

**Özellik yönetimi** çalışma alanı, her sürümde teslim edilen özelliklerin bir listesini sağlar. Varsayılan olarak, bu özellikler kapalıdır. Çalışma alanını, bu özellikleri açıp ilgili belgelere bakmak için kullanabilirsiniz. Özellik yönetimi hakkında daha fazla bilgi için bkz. [Özellik yönetimine genel bakış](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview).

Tüm yeni özellikler en az 30 gün boyunca ve genellikle 30-60 gün önizlemede kalır. Önemli özellikler genellikle önizleme dönemini izleyen her yılın Ekim ve Nisan ayında kullanılabilir. **Özellik yönetimi** çalışma alanında yeni yetenekleri gördüğünüz anda bunları açabilirsiniz. Bazı özellikler varsayılan olarak açık olabilir.
 
Bazen bir tümleştirme özelliği varsayılan olarak açıktır ve kapatılamaz (örneğin, **Özellik yönetimi** çalışma alanı).
 
Bir özellik genel olarak kullanılabilir olduğunda üretim ortamlarında açılıp kapatılamayabilir. **Özellik yönetimi** çalışma alanı bir önizleme özelliğinin zorunlu hale gelme zamanını belirtir. Bu tarih genellikle yarıyıllık sürüm planlarına uygun olacak şekilde 1 Ekim veya 1 Nisandır. Zorunlu özellikleri kapatamazsınız. Bir özelliği zorunlu olana kadar tüm ortamlarda kapatıp açabilirsiniz.

### <a name="streamlined-worker-form-has-moved-to-the-feature-management-workspace-390583"></a>Kolay çalışan formu, özellik yönetimi çalışma alanına taşındı (390583)

Bu değişiklikle, hızlı çalışan form artık **Özellik Yönetimi** çalışma alanında etkinleştirilebilir. Bu özellik, **sistem yönetimi**'ndeki **sistem parametreleri** formundan taşındı.

### <a name="prevent-hcmworkerpayrollinfo-records-from-being-written-without-a-worker-value-394526"></a>HcmWorkerPayrollInfo kayıtlarının bir çalışan değeri olmadan yazılmasını engelleyin (394526)

Bu sürümde, **HcmWorkerPayrollInfo** kayıtları artık bu senaryoda çalışan referansı olmaksızın altında oluşturulmaz. 

### <a name="message-log-associated-to-the-action-isnt-populated-when-the-action-fails-to-complete-374007"></a>Eylem tamamlanamazsa eylemle ilişkili ileti günlükleri doldurulmaz (374007)

Bu sürüm, belirli senaryolarda bir eylem başarısız olduğunda eylem İleti kütüğünü doldurmak için bir değişiklik içerir. 

### <a name="common-data-service-integration-batch-job-creation-388030"></a>Ortak veri hizmeti tümleştirme toplu iş oluşturma (388030)

Bu değişiklikle, servis etkinleştirildiğinde Common Data Service tümleştirme toplu işleri oluşturulur.

### <a name="additional-pick-list-values-to-custom-fields-arent-reflected-in-common-data-service-after-clicking-apply-on-the-custom-fields-form-379599"></a>Özel alanlar formunda Uygula'ya tıkladıktan sonra özel alanlardaki ek liste değerleri Common Data Service'te yansıtılmıyor (379599)

Bu değişiklikle, taşı alanında girilen yeni çekme listesi değerleri şimdi yaptığınız değişiklikleri uyguladığınızda Common Data Service eşitlenir.

### <a name="update-to-common-data-service-for-then-leave-bank-transaction-entity-turns-into-an-insert-on-talent-side-352938"></a>Banka hareketi varlığı için Common Data Service'e güncelleştir, Beceri tarafında girdiye dönüşür (352938)

Bu değişiklik, bir banka hareketine ait bir güncelleştirmenin Beceride yeni bir kayıt oluşturduğu bir sorunu düzeltir.

## <a name="in-preview"></a>Ön izlemede

Önizleme özellikleri yalnızca **korumalı alan** ortamlarında etkinleştirilecek.

### <a name="print-performance-reviews"></a>Performans incelemelerini yazdırma

Dynamics 365: 2019 sürüm dalgası 2 planındaki [Performans incelemelerini yazdır](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-talent/print-performance-reviews) konusuna bakın.



[!INCLUDE[footer-include](../includes/footer-banner.md)]