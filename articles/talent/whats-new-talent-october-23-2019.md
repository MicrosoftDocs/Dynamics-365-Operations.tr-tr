---
title: Dynamics 365 Talent'taki yenilikler veya değişiklikler (23 Ekim 2019)
description: Bu konuda, Microsoft Dynamics 365 Talent'taki yeni veya değişen özellikler açıklanmaktadır.
author: Darinkramer
manager: AnnBe
ms.date: 10/23/2019
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
ms.search.validFrom: 2019-10-23
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 7506953c797f5a55a93f1169bf48af8b06eb440e
ms.sourcegitcommit: 871707a3fd236da693a3d51f401eb0cb9d4bae39
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 12/06/2019
ms.locfileid: "2896808"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-october-23-2019"></a>Dynamics 365 Talent'taki yenilikler veya değişiklikler (23 Ekim 2019)

Bu konuda, Dynamics 365 Talent'daki yeni veya değişen özellikler açıklanmaktadır.

## <a name="changes-in-attract"></a>Attract'te değişiklikler
Bu sürüm, Dynamics 365 Talent: Attract için küçük hata düzeltmeleri içeriyor.

## <a name="changes-in-onboard"></a>Onboard'taki değişiklikler
Bu sürüm, Dynamics 365 Talent: Onboard için küçük hata düzeltmeleri içeriyor.

## <a name="changes-in-core-hr"></a>Core HR içindeki değişiklikler

Bu bölümde açıklanan değişiklikler sürüm numarası 8.1.2569 için geçerlidir. Bazı başlıklardaki parantez içindeki numaralar Microsoft Dynamics Lifecycle Services (LCS) destek numaralarına referans verir.

### <a name="platform-update-30-for-finance-and-operations-apps"></a>Finance and Operations uygulamaları için Platform güncelleştirmesi 30

Daha fazla bilgi için bkz. [Finance and Operations uygulamaları için Platform güncelleştirmesi 30'daki yenilikler veya değişiklikler (2019 Kasım)](https://docs.microsoft.com/en-us/dynamics365/fin-ops-core/fin-ops/get-started/whats-new-platform-update-30).

### <a name="remove-benefits-open-enrollment-preview-feature"></a>Kazançlar açık kayıt önizlemesi özelliği kaldırılıyor

[Core HR operasyonel mükemmellik sağlama konusunda stratejik yatırımlar](https://cloudblogs.microsoft.com/dynamics365/bdm/2019/10/02/strategic-investments-in-core-hr-drive-operational-excellence) blog gönderisindeki duyurumuzla birlikte Microsoft 18 Ekim 2019 tarihinde genel önizlemedeki kazançlar açık kayıt özelliğini kaldırdı. Bunun yerine, gelecekte yeni işlevler yayımlanacaktır. Kazançlar açık kayıt özelliğinin şu anda önizlemede olan üretim kullanımı desteklenmeyecektir.

### <a name="error-while-selecting-the-countryregion-on-the-worker-form-a-second-time-350294"></a>Çalışan formunda ülke/bölge ikinci kez seçilirken hata (350294)

Bu hafta yayımlanan sürümle, **Çalışan** formunda bir ülke/bölge seçilirken oluşan sorun giderildi.

### <a name="financial-dimension-values-default-to-the-combination-display-field-when-do-not-allow-manual-entry-is-set-to-true-340097"></a>El ile girişe izin verme doğru olarak ayarlandığında mali boyut değerleri Birlikte görüntüleme alanına varsayılan alınıyor (340097)

Bu değişiklikle, mali boyutları ayarlarken ve el ile girişe izin verme seçeneğini kullanırken, sistem boyut değerini **Birlikte görüntüleme** alanına doğru şekilde varsayılan alacaktır.

### <a name="new-relationship-types-should-be-added-to-relationship-lookup-in-the-personal-contacts-form-347691"></a>Kişisel ilgili kişiler formunda İlişki aramasına yeni ilişki türleri eklenmelidir (347691)

Bu sürüm, **İlişki türleri** tablosunda yeni ilişki türleri eklemek ve bu değişiklikleri kişisel ilgili kişiler için ilişki aramasında yansıtmak için yeni yetenekler içerir.

### <a name="additional-list-values-in-custom-fields-arent-reflected-in-common-data-service-379599"></a>Özel alanlardaki ek liste değerleri Common Data Service'ta yansıtılmaz (379599)

Bu haftaki sürümle, zaten Common Data Service ile eşitlenmiş mevcut bir özel alana yeni bir liste değeri ekleme, yeni çekme listesi değerleri değişiklikler varlığa uygulandıktan sonra görüntülenir.

### <a name="on-the-terms-of-employment-page-all-employees-terms-of-employment-appear-after-selecting-open-in-excel-348073"></a>İstihdam koşulları sayfasında, tüm çalışanların istihdam koşulları Excel'de aç seçildikten sonra görünüyor (348073)

Bu sürümde, yalnızca seçilen çalışanların çalışma koşulları Excel'de açılacaktır. Tüm şirket güvenliği de dikkate alınmıştır.

### <a name="the-association-between-the-work-calendar-holiday-entity-and-the-work-calendar-entity-is-missing-in-common-data-service-324178"></a>İş takvimi tatil varlığı ile İş takvimi varlığı arasındaki ilişki Common Data Service'te yok (324178)

Bu ilişki, bu sürümle eklenmiştir. Bu değişiklik bir çalışanın iş günlerini PowerApps'te görüntüleme olanağı sağlar. 

### <a name="error-when-using-employee-self-service-workflows-with-configurable-hierarchies-370132"></a>Yapılandırılabilir hiyerarşisi bulunan personel self servis iş akışları kullanılırken hata (370132)

Bu sürümde, yapılandırılabilir hiyerarşiler kullanarak iş akışlarının yapılandırılmasına ilişkin daha iyi iletiler yer almaktadır. 

### <a name="system-allows-creation-of-new-positions-where-the-available-for-assignment-date-is-earlier-than-the-activation-date-340103"></a>Sistem, Atama için uygun tarihinin Etkinleştirme tarihinden önce olduğu durumlarda yeni pozisyonlar oluşturulmasına izin verir (340103)

Bu değişiklik, **Atama için uygun** tarihinin pozisyonun **Etkinleştirme** tarihinden önce olduğu durumlarda bir uyarı görüntüleyecektir.

## <a name="coming-soon"></a>Çok yakında

### <a name="print-performance-reviews"></a>Performans incelemelerini yazdırma

Dynamics 365: 2019 sürüm dalgası 2 planındaki [Performans incelemelerini yazdır](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-talent/print-performance-reviews) konusuna bakın.

### <a name="feature-management-workspace"></a>Özellik yönetimi çalışma alanı

Özellikler, her sürümüne eklenir ve güncelleştirilir. Özellik yönetimi deneyimi, her sürümde teslim edilen özelliklerin listesini görüntüleyebileceğiniz bir çalışma alanı sağlar. Varsayılan olarak, bu özellikler kapalıdır. Çalışma alanını, bu özellikleri açıp ilgili belgelere bakmak için kullanabilirsiniz.

Özellik yönetimiyle gelen değişiklikler hakkında daha fazla bilgi edinmek için bkz. [Özellik yönetimine genel bakış](https://docs.microsoft.com/en-us/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview).
