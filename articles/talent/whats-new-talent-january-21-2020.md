---
title: Dynamics 365 Talent'daki yenilikler veya değişiklikler (21 Ocak 2020)
description: Bu makalede, Microsoft Dynamics 365 Talent'taki yeni veya değişen özellikler açıklanmaktadır.
author: Darinkramer
manager: AnnBe
ms.date: 01/21/2020
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
ms.search.validFrom: 2020-01-21
ms.dyn365.ops.version: Talent
ms.openlocfilehash: e9dee64e94c904cfe07c6a7766f6a60b1d60a2db
ms.sourcegitcommit: e89bb3e5420a6ece84f4e80c11e360b4a042f59d
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/17/2020
ms.locfileid: "4528135"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-january-21-2020"></a>Dynamics 365 Talent'daki yenilikler veya değişiklikler (21 Ocak 2020)

[!include [banner](includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Bu makalede Dynamics 365 Talent'te yeni veya değişen özellikler açıklanmaktadır.

## <a name="changes-in-attract"></a>Attract'te değişiklikler

Bu sürüm, Dynamics 365 Talent: Attract için küçük hata düzeltmeleri içeriyor. En son bildirimize destek vermek için, [Dynamics 365 Human Resources ile daha başarılı bir iş gücü oluşturma](https://cloudblogs.microsoft.com/dynamics365/bdm/2019/12/06/building-a-more-successful-workforce-with-dynamics-365-human-resources/), Attract'a yönelik işlevler ekledik.

### <a name="download-environment-data"></a>Ortam verileri indir

Yöneticiler kendi ortam verilerini yükleyebilirler. Veriler, bir ZIP dosyasında dışa aktarılan tüm işler, aday ve konfigürasyonlarla standart JSON biçiminde dışa aktarılır. Daha fazla bilgi için bkz. [Attract ve Onboard dışa veri aktarma](https://docs.microsoft.com/dynamics365/talent/attract-onboard-export-data).

### <a name="restricting-access-to-environments-for-non-admin-users"></a>Yönetici olmayan kullanıcılar için ortamlara erişimi sınırlandırma

Yöneticiler artık yönetici olmayan kullanıcılar için ortama erişimi kısıtlayabilir. Bu eylem geri alınamaz. Daha fazla bilgi için, bkz. [Attract'a erişimi kısıtla](https://docs.microsoft.com/dynamics365/talent/attract-onboard-export-data#restrict-access-to-attract).

## <a name="changes-in-onboard"></a>Onboard'taki değişiklikler

Bu sürüm, Dynamics 365 Talent: Onboard için küçük hata düzeltmeleri içeriyor.

### <a name="exporting-onboarding-guides"></a>İşe alım kılavuzlarını dışa aktarma

Kullanıcılar artık tüm ekleme kılavuzlarını verebilir ve Word belgesi biçiminde şablon ekleyebilir. Daha fazla bilgi için bkz. [Attract ve Onboard dışa veri aktarma](https://docs.microsoft.com/dynamics365/talent/attract-onboard-export-data).

## <a name="changes-in-core-hr"></a>Core HR içindeki değişiklikler

Bu bölümde açıklanan değişiklikler sürüm numarası 8.1.2726 için geçerlidir. Bazı başlıklardaki parantez içindeki numaralar Microsoft Dynamics Lifecycle Services (LCS) destek numaralarına referans verir.

### <a name="most-recent-annual-compensation-field-in-verify-employment-form-isnt-consistent-392092"></a>İstihdam doğrula formundaki en son yıllık maaş alanı tutarsız (392092)

Bu sürüm, **istihdam Onayla** formundaki şirket seçicisini temel alarak en son para birimini tutarlı olarak görüntüleyen bir değişiklik içerir.

### <a name="known-as-field-added-to-the-feedback-recipient-lookup-407789"></a>Geri bildirim alıcı aramasına eklenen (407789) alan olarak bilinen

Performans geri bildirimi sağlarken, çalışanlar için arama, geri bildirim doğru kişiye gidip gitmediğine karar vermek için yeterli bilgi sağlamadı. Çalışanın benzersiz adını tanımlamaya yardımcı olması için **bilinen** bir sütun ekledik.
 
### <a name="hcmworkerpayrollinfo-record-is-created-without-an-association-to-a-worker-394526"></a>HcmWorkerPayrollInfo kaydı bir çalışan ile ilişkili olmadan oluşturulur (394526)

Bu sürüm, bir çalışana referans olmadan HCMWorkerPayrollInfo kayıtlarına yazmayan bir değişiklik içerir.

### <a name="able-to-edit-department-when-navigating-from-position-hierarchy-341001"></a>Pozisyon hiyerarşisinden gezinirken departman düzenlenebilir (341001)

Güvenlik, düzenleme departmanlarına erişimi reddedecek şekilde ayarlandığında, tüm senaryolarda **departmanlar** formuna gidildiğinizde düzenleme devre dışı bırakılır.

## <a name="coming-soon"></a>Çok yakında

Aşağıdaki değişikliklerle , yeni bir Common Data Service çözüm yakında kullanıma sunulur:

| Tanım | Değiştirme |
| --- | --- |
| **İş/pozisyon** varlığı değişiklikleri | <ul><li>**Ücret bölgesi** eklendi</li><li>**Mali boyutlar** eklende</li></ul> |
| **Çalışan varlığı** değişiklikleri | <ul><li>**Ad sırası** eklendi</li><li>**Evden çalışma** eklendi</li><li>**Dil** eklendi</li><li>**Kıdem tarihi** eklendi</li><li>**Yıldönümü tarihi** eklendi</li><li>**Orijinal işe alma tarihi** eklendi</li></ul> |
| **İstihdam** varlık değişiklikleri | <ul><li>**Mali boyutlar** eklende</li><li>**İşten çıkarma nedeni** eklendi</li><li>**Geçiş tarihinden** yeniden adlandırılan **sonlandırma tarihi**</li><li>**Deneme tarihleri** eklendi</li></ul> |
| **Çalışan adresi** varlık değişiklikleri | <ul><li>**Cadde Adresi** eklendi</li><li>**Adres satırı 1**, **Adres satırı 2** ve **Adres satırı 3** itiraz için işaretlenmiş.</li></ul> |
| Yeni değişken ücret kurulumu varlıkları | <ul><li>**Değişken Ücret Planı Türü**</li><li>**Maaş değişken planı**</li><li>**Hakediş ödeme kuralları**</li><li>**Değişken Ücret Planı Düzeyi**</li></ul> |
| Yeni **çalışan takvimi çalışan** varlığı | <ul><li>**İş takvimi varlığı** eklendi</li></ul> |


[!INCLUDE[footer-include](../includes/footer-banner.md)]