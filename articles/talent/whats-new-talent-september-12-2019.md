---
title: Dynamics 365 for Talent'taki yenilikler veya değişiklikler (10 Eylül 2019)
description: Bu konuda, Microsoft Dynamics 365 for Talent'daki yeni veya değişen özellikler açıklanmaktadır.
author: Darinkramer
manager: AnnBe
ms.date: 9/10/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2019-09-10
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 48f41b53060c7f2bfc407b22295aa40d85ce1c9d
ms.sourcegitcommit: 7a93ea2dc90d31175b708566a00cd707cb47ab7c
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/13/2019
ms.locfileid: "1996200"
---
# <a name="whats-new-or-changed-in-dynamics-365-for-talent-september-10-2019"></a>Dynamics 365 for Talent'taki yenilikler veya değişiklikler (10 Eylül 2019)

[!include [banner](includes/banner.md)]

Bu konuda, Dynamics 365 for Talent'daki yeni veya değişen özellikler açıklanmaktadır.

## <a name="changes-in-attract"></a>Attract'te değişiklikler

### <a name="candidate-e-mail-login"></a>Aday e-posta oturumu açma

Adaylar artık bir hesap oluşturmak için herhangi bir e-posta adresini kullanabilir, iş başvurusu için Talent kariyer sitesinde oturum açabilir ve başvuru durumlarına bakabilirler. Bu, zaten sahip oldukları, sosyal ağ hesaplarını veya kuruluş kimlik bilgilerini kullanarak Talent kariyer sitesinde oturum açma olanağına ek olarak sunulmuştur.

### <a name="job-activation-and-posting"></a>İş etkinleştirme ve yayınlama

İş etkinleştirme ve yayınlamada birkaç değişiklik yaptık. İşleri Talent kariyer sitesinde veya harici iş panolarında (LinkedIn, Broadbean vb.) yayınlamadan önce etkinleştirmeniz gerekir.

## <a name="changes-in-onboard"></a>Onboard'daki değişiklikler

Bu sürüm, Dynamics 365 Talent: Onboard için küçük hata düzeltmeleri içeriyor.

## <a name="changes-in-core-hr"></a>Core HR içindeki değişiklikler

Bu bölümde açıklanan değişiklikler sürüm numarası 8.1.2482 için geçerlidir. Bazı başlıklardaki parantez içindeki numaralar Microsoft Dynamics Lifecycle Services (LCS) destek numaralarına referans verir.

### <a name="you-can-enable-preview-features-in-sandbox-and-trial-environments"></a>Önizleme özelliklerini Korumalı Alan ve Deneme ortamlarında etkinleştirebilirsiniz

Talent'ın yeni bir örneğini oluşturduğunuzda, örnek türünün Üretim veya Korumalı alan olduğunu belirtebilirsiniz. Korumalı alan türünün örnekleri yeni özelliklerin erken test edilmesine izin verir. Varolan örneklerden birinin Korumalı alan örneği türüne güncelleştirilmesini istiyorsanız değişiklik isteğini başlatmak için Desteğe başvurun.

Değişikliklerin nasıl yayımlanacağı hakkında daha fazla bilgi için, bkz [Talent sağlama](./provisioning-talent.md).

### <a name="platform-update-29"></a>Platform güncelleştirmesi 29

Platform güncelleştirmesi 29 hakkında daha fazla ayrıntı için bkz. [Dynamics 365 for Finance and Operations önizleme özellikle platform güncelleştirmesi 29 (Ekim 2019)](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/get-started/whats-new-platform-update-29).

### <a name="new-job-base-entity-available-in-data-management-framework-347202"></a>Veri yönetim çerçevesinde kullanılabilecek yeni temel iş varlığı (347202)

Bu sürümle, verileri içe/dışa aktarmak için kullanılabilecek yeni bir Temel İş varlığı kullanıma sunuluyor. 

### <a name="worker-advanced-security-policy-incorrectly-displays-positions-in-position-hierarchy-354868"></a>Çalışan gelişmiş güvenlik ilkesi Konum Hiyerarşisindeki konumları yanlış görüntülüyor (354868)

Bu sürümde, kullanıcıların erişimi sınırlı olduğunda, pozisyonlar artık "boş" bir çalışan ile açık olarak görüntülenmiyor.

### <a name="job-form-close-box-wont-close-form-in-certain-situations-342467"></a>İş formu kapanış kutusu belirli durumlarda formu kapatmayacak (342467)

Bu sürüm, İş formunun tüm senaryolarda kapatılmasına izin veren bir değişiklik içeriyor.

### <a name="new-case-on-employee-record-is-locked-for-human-resources-manager-role-337111"></a>Çalışan kaydında yeni servis talebi İnsan Kaynakları Yöneticisi rolü için kilitli (337111)

Bu değişiklikle, servis talebi yönetimi formu, çalışan formundan erişilirken artık kilitlenmiyor.

### <a name="employment-end-date-always-defaults-to-235959-351492"></a>Çalışma bitiş tarihi her zaman varsayılan olarak 23:59:59 oluyor (351492)

Bu değişiklikle, bir çalışmayı el ile bitirirken, çalışma tarihini 23:59:59 dışında bir saate değiştirebilirsiniz.

### <a name="unable-to-set-up-expiration-date-on-an-earning-code-through-data-management-336604"></a>Kazanç kodunda bitiş tarihi Veri yönetimi aracılığıyla ayarlanamıyor (336604)

Bu sürümde, **PayrollWorkerPositionEarningCodeEntity** varlığı aracılığıyla sona eren kazanç kodları ayarlayabilirsiniz.

### <a name="employee-development-analytic-report-doesnt-display-data-348737"></a>Personel gelişimi analitik raporu verileri görüntülemiyor (348737)

Bu haftaki sürümde, personel becerileriyle ilgili analizler, doğru raporlama sağlayacak şekilde güncelleştirildi.

### <a name="terms-of-employment-datetime-dont-default-to-beginning-of-day-349101"></a>Çalışma koşulları tarihi/saati varsayılan olarak günün başlangıcına ayarlanmıyor (349101)

Bu değişiklikle artık başlangıç tarihi/saati varsayılan olarak günün başlangıcına, bitiş tarihi/saati günün bitişine ayarlanıyor.

### <a name="changing-the-employment-end-date-on-worker-action-form-displays-an-error-354092"></a>Çalışan eylemi formundaki çalışma bitiş tarihi değiştirilince hata görüntüleniyor (354092) 

Bu değişiklik, çalışan eyleminin bir parçası olarak çalışma bitiş tarihi değiştirilirken oluşan bir sorunu düzeltiyor.

### <a name="applying-onboarding-checklists-across-companies-338433"></a>Şirketler arasında işe alım yapılacaklar listeleri uygulama (338433)

Bu sürüm oturum açmış tüzel kişilik dışındaki tüzel kişiliklerde çalışan personel için yapılacaklar listeleri uygulayabilme olanağı sağlıyor.

## <a name="in-preview"></a>Ön izlemede

### <a name="streamlined-employee-entry-and-navigation"></a>Kolaylaştırılmış çalışan girişi ve gezintisi

Bu işlevsellik artık korumalı ortamlarda kullanılabilir. Bu özelliği etkinleştirmek için **Sistem yönetimi > Bağlantılar > Kurulum > Sistem parametreleri > Önizleme özellikleri**ne gidin. **Gelişmiş çalışan formu ve gezinme**'yi seçin. Bu değişiklikler tüm kullanıcılar için etkinleştirilir. Bu seçeneği istediğiniz zaman kapatabilirsiniz.

Daha fazla bilgi için, bkz. [Kolaylaştırılmış çalışan girişi ve gezintisi](./streamlined-employee-entry.md).
