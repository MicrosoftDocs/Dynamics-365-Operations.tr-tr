---
title: Dynamics 365 for Talent'deki yenilikler veya değişiklikler (27 Ağustos 2019)
description: Bu konuda, Microsoft Dynamics 365 for Talent'daki yeni veya değişen özellikler açıklanmaktadır.
author: Darinkramer
manager: AnnBe
ms.date: 8/27/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: andreabichsel
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2019-08-27
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 8965636e539345be5ef0ad591f7017938efd322d
ms.sourcegitcommit: e89bb3e5420a6ece84f4e80c11e360b4a042f59d
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/17/2020
ms.locfileid: "4529816"
---
# <a name="whats-new-or-changed-in-dynamics-365-for-talent-august-27-2019"></a>Dynamics 365 for Talent'deki yenilikler veya değişiklikler (27 Ağustos 2019)

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Bu konuda, Dynamics 365 for Talent'daki yeni veya değişen özellikler açıklanmaktadır.

## <a name="changes-in-attract"></a>Attract'te değişiklikler

Bu sürüm, Dynamics 365 Talent: Attract için küçük hata düzeltmeleri içeriyor.

## <a name="changes-in-onboard"></a>Onboard'taki değişiklikler

Bu sürüm, Dynamics 365 Talent: Onboard için küçük hata düzeltmeleri içeriyor.

## <a name="changes-in-core-hr"></a>Core HR içindeki değişiklikler

Bu bölümde açıklanan değişiklikler sürüm numarası 8.1.2447 için geçerlidir. Bazı başlıklardaki parantez içindeki numaralar Microsoft Dynamics Lifecycle Services (LCS) destek numaralarına referans verir.

### <a name="preview-features-are-enabled-only-in-sandbox-instances"></a>Önizleme özellikleri yalnızca korumalı alan örneklerinde etkinleştirilir

Talent'ın yeni bir örneğini oluşturduğunuzda, örnek türünün Üretim veya Korumalı alan olduğunu belirtebilirsiniz. Korumalı alan türünün örnekleri yeni özelliklerin erken test edilmesine izin verir. Var olan tüm Talent örnekleri Üretim örneği türüne güncelleştirilecek. Var olan örneklerden birinin Korumalı alan örneği türüne güncelleştirilmesini istiyorsanız değişiklik isteğini başlatmak için  Destek başvurun.

Değişikliklerin nasıl yayımlanacağı hakkında daha fazla bilgi için bkz. [Talent sağlama](./provisioning-talent.md).

### <a name="view-extended-information-for-performance-in-manager-self-service"></a>Yönetim self servisinde performans için genişletilmiş bilgileri görüntüle

Yeni bir seçenek, yöneticilerin hem doğrudan raporların hem de genişletilmiş raporlarının performansını görüntülemesine olanak sağlar. Şu anda, satır yöneticileri performans hedeflerini atayabilir ve güncelleştirebilir ve yeni incelemeler yapabilir. Ek olarak, doğrudan yöneticiler ve bunların çalışanları performans gözden geçirme işleminin sorunsuz şekilde devam etmesine yardımcı olmak için performans günlüklerini koruyabilir ve güncelleştirebilir. Bu değişiklik uygulandığında, yöneticiler, kendi talimatlarına ek olarak, genişletilmiş raporlarının performansla ilgili bilgilerini görüntüleyebilir ve koruyabilirler.

### <a name="deleting-legal-entities-isnt-allowed-if-employees-exist-within-the-company-339849"></a>Şirket içinde çalışanlar mevcutsa, yasal varlıkların silinmesine izin verilmez (339849)

Bu değişiklikle, çalışanların ve diğer ilgili verilerin yasal varlık için mevcut olup olmadığını şirketleri kaldıramaz veya silemezsiniz.

### <a name="compensation-management-business-intelligence-analytics-dont-match-on-the-compensation-workspace-322493"></a>Ücret yönetimi iş zekası analizi, ücret çalışma alanında eşleşmiyor (322493)

Bu sürümde, ücret analizi, çalışanlara atanan planları tam olarak yansıtacak şekilde düzeltilmiştir.

### <a name="workflow-placeholder-company-displays-dat-when-hiring-employees-through-workflow-343905"></a>İş akışı yer tutucusu %company%, çalışanları iş akışı aracılığıyla işe alırken DAT görüntüler (343905)

Bu sürümde, şirket yer tutucusu yeni çalışanın iş fırsatıyla ilişkili yasal varlığı görüntüler.

### <a name="the-cdsjobposition-entity-displays-an-error-when-valid-to-date-is-set-349387"></a>Geçerli bitiş tarihi ayarlandığında CDSJobPosition varlığı bir hata görüntüler (349387)

Bu sürümde,**CDSJobPosition** varlığındaki **pozisyon ayrıntısı** ve **pozisyon süresi** veri kaynakları düzenlemeleri Common Data Service'ten **yürürlülük tarihi** alanlarına izin verir. 

### <a name="for-employee-termination-the-last-day-worked-is-populated-on-assignment-end-date-332496"></a>Çalışan işten çıkarma için, çalışılan son gün Atama bitiş tarihinde doldurulur (332496)

Bu değişiklik, konum **Atama bitiş tarihi** yerine **Çalışma bitiş tarihi**'ni varsayılan olarak alır. Veri girerken bu varsayılanları değiştirebilirsiniz.

### <a name="legal-entities-arent-limited-with-hire-338871"></a>Yasal varlıklar işe alımla sınırlı değildir (338871)
 
Bu değişiklik, işe alma işlemini yalnızca kullanıcının erişebileceği geçerli varlıkları gösterecek şekilde kısıtlar.  

## <a name="in-preview"></a>Ön izlemede

### <a name="streamlined-employee-entry-and-navigation"></a>Kolaylaştırılmış çalışan girişi ve gezintisi

Bu işlevsellik artık korumalı alanlarda ve deneme ortamlarında kullanılabilir. Bu özelliği etkinleştirmek için **Sistem yönetimi > Bağlantılar > Kurulum > Sistem parametreleri > Önizleme özellikleri** ne gidin. **Gelişmiş çalışan formu ve gezinme**'yi seçin. Bu değişiklikler tüm kullanıcılar için etkinleştirilir. Bu seçeneği istediğiniz zaman kapatabilirsiniz.

Daha fazla bilgi için, bkz. [Kolaylaştırılmış çalışan girişi ve gezintisi](./streamlined-employee-entry.md).

## <a name="coming-soon"></a>Çok yakında

### <a name="platform-update-29"></a>Platform güncelleştirmesi 29

Platform güncelleştirmesi 29 hakkında daha fazla ayrıntı için bkz. [Dynamics 365 for Finance and Operations önizleme özellikle platform güncelleştirmesi 29 (Ekim 2019)](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/get-started/whats-new-platform-update-29).
