---
title: Dynamics 365 Talent'daki yenilikler veya değişiklikler (3 Aralık 2019)
description: Bu makalede, Microsoft Dynamics 365 Talent'taki yeni veya değişen özellikler açıklanmaktadır.
author: Darinkramer
manager: AnnBe
ms.date: 12/03/2019
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
ms.search.validFrom: 2019-12-03
ms.dyn365.ops.version: Talent
ms.openlocfilehash: b1ed998302762203bad736161a27a48152de65f7
ms.sourcegitcommit: 871707a3fd236da693a3d51f401eb0cb9d4bae39
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 12/06/2019
ms.locfileid: "2897730"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-december-3-2019"></a>Dynamics 365 Talent'daki yenilikler veya değişiklikler (3 Aralık 2019)

Bu makalede Dynamics 365 Talent'te yeni veya değişen özellikler açıklanmaktadır.

## <a name="changes-in-attract"></a>Attract'te değişiklikler

Bu sürüm, Dynamics 365 Talent: Attract için küçük hata düzeltmeleri içeriyor.

## <a name="changes-in-onboard"></a>Onboard'taki değişiklikler

Bu sürüm, Dynamics 365 Talent: Onboard için küçük hata düzeltmeleri içeriyor.

## <a name="changes-in-core-hr"></a>Core HR içindeki değişiklikler

Bu bölümde açıklanan değişiklikler sürüm numarası 8.1.2646 için geçerlidir. Bazı başlıklardaki parantez içindeki numaralar Microsoft Dynamics Lifecycle Services (LCS) destek numaralarına referans verir.

### <a name="feature-management-workspace"></a>Özellik yönetimi çalışma alanı

**Özellik yönetimi** çalışma alanı, her sürümde teslim edilen özelliklerin bir listesini sağlar. Varsayılan olarak, bu özellikler kapalıdır. Çalışma alanını, bu özellikleri açıp ilgili belgelere bakmak için kullanabilirsiniz. Özellik yönetimi hakkında daha fazla bilgi için bkz. [Özellik yönetimine genel bakış](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview).

Tüm yeni özellikler en az 30 gün boyunca ve genellikle 30-60 gün önizlemede kalır. Önemli özellikler genellikle önizleme dönemini izleyen her yılın Ekim ve Nisan ayında kullanılabilir. **Özellik yönetimi** çalışma alanında yeni yetenekleri gördüğünüz anda bunları açabilirsiniz. Bazı özellikler varsayılan olarak açık olabilir.
 
Bazen bir tümleştirme özelliği varsayılan olarak açıktır ve kapatılamaz (örneğin, **Özellik yönetimi** çalışma alanı).
 
Bir özellik genel olarak kullanılabilir olduğunda üretim ortamlarında açılıp kapatılamayabilir. **Özellik yönetimi** çalışma alanı bir önizleme özelliğinin zorunlu hale gelme zamanını belirtir. Bu tarih genellikle yarıyıllık sürüm planlarına uygun olacak şekilde 1 Ekim veya 1 Nisandır. Zorunlu özellikleri kapatamazsınız. Bir özelliği zorunlu olana kadar tüm ortamlarda kapatıp açabilirsiniz.

### <a name="add-automatic-scheduling-of-batch-job-history-cleanup-332528"></a>Toplu İş geçmişi temizlemeyi otomatik olarak zamanlama Ekle (332528)

Bu değişiklikle **toplu iş geçmişi** her gece ile çalışır ve 30 günden eski toplu iş geçmişi maddelerini kaldırır.

### <a name="talent-doesnt-respond-in-worker-actions-when-identification-number-length-doesnt-match-the-identification-type-390971"></a>Kimlik numarası uzunluğu kimlik türüyle (390971) eşleşmezse, iş eylemleri çalışan eylemlerinde yanıt vermez

Bu sürüm, kimlik numarası uzunluğu kimlik türünün tanımıyla eşleşmediğinde oluşan sorunu düzeltir. 

### <a name="fixed-compensation-doesnt-update-level-with-changes-to-position-details--348085"></a>Sabit maaş pozisyon ayrıntılarına yapılan değişikliklerle düzeyi güncelleştirmiyor (348085)

Bu haftalık serbest bırakıldığında, **maaş başlangıç tarihi** bir çalışan için yeni sabit maaş kaydı oluştururken o anda o andaki konumla ilişkilendirilmiş işi belirler.

### <a name="workers-employees-and-contractors-lists-show-worker-type-as-both-when-they-should-only-be-worker-or-contractor-384473"></a>Çalışanlar, çalışanlar ve yükleniciler listeleri, yalnızca alt yüklenici veya yüklenicisi olması gerektiği durumlarda çalışan türünü gösterir (384473)

Bu değişiklik, çalışan tarafından girilen (yüklenici veya çalışan) türü doğru şekilde yansıtır.

### <a name="email-notifications-for-new-hire-actions-dont-contain-name-information-due-to-security-policies-383402"></a>Yeni işe alma eylemleriyle ilgili e-posta bildirimleri güvenlik ilkeleri nedeniyle ad bilgisi içermiyor (383402)

Bu değişiklik, gelişmiş güvenlik etkin olduğunda iş akışı için yer tutucularda ilk veya soyad alanlarında görüntülenen bilgileri düzeltir.

### <a name="system-allows-two-full-day-leave-requests-for-the-same-day-379284"></a>Sistem, aynı gün için iki günlük çıkış isteğine izin verir (379284)

Bu değişiklikle, aynı gün için iki izin isteği veremez. 

### <a name="address-changes-list-should-be-sorted-by-effective-date-352798"></a>Adres değişiklikleri listesi yürürlülük tarihine göre sıralanmalıdır (352798)

Bu değişiklikle, adres değişikliği listesi şimdi **yürürlülük tarihine** göre sıralanmıştır.

### <a name="leave-requests-should-allow-deletes-from-common-data-service-to-talent-376999"></a>Bırakma istekleri, Common Data Service'ten Talent'a silinmesine izin verir (376999)

Bu değişiklikle, taslak ve iptal edilmiş izin isteklerinin Common Data Service'ten silinebilmesi ve Talent'tan kaldırılabilir olmasını sağlayabilirsiniz.

### <a name="delete-earning-codes-is-allowed-when-the-same-earning-code-is-assigned-to-an-employee-371792"></a>Aynı kazanç kodu bir çalışana atandığında, atık koduna silme işlemine izin verilir (371792)

Bu sürümde, sistemden kazanç kodunu silmeden önce, çalışanın kodunu çalışandan kaldırmanız gerekir.

### <a name="leave-and-absence-workflow-with-two-approval-stages-fails-to-complete--391116"></a>İki onay aşamasına sahip bırak ve devamsızlık iş akışı tamamlanamıyor (391116)

Bu değişiklikle, bırak ve devamsızlık iş akışı, talep için birden fazla onay aşaması konfigüre edildiğinde tüm adımlarla devam eder.

### <a name="issue-date-doesnt-sync-to-common-data-service-when-updated-or-entered-in-talent-397361"></a>Çıkış tarihi, Talent'ta güncelleştirildiğinde veya girildiğinde Common Data Service ile eşitlenmiyor (397361)

Bu değişiklik, **kişi kimlik** kayıtlarının çıkış tarihinin Talent'tan Common Data Service'e eşitlenmemiş olduğu bir sorunu düzeltir.

### <a name="hierarchy-circular-reference-error-issued-when-assigning-a-manager-to-a-position-386659"></a>Hiyerarşi döngüsel referansı bir pozisyona yönetici atanırken hata oluştu (386659)

Bu değişiklik, bir pozisyona yeni bir yönetici atanırken döngüsel referans hatası olduğunda, benzersiz bir senaryoyu düzeltir.

### <a name="common-data-service-entities-that-now-support-custom-fields"></a>Şu anda özel alanları destekleyen Common Data Service varlıklar

Özel alanları destekleyen Common Data Service varlıklar aşağıdadır:

| Dosya Adı | Varlık |
| --- | --- |
| Banka hesabı ödemeleri | cdm_bankaccountdisbursement |
| Kazanç Hesaplama Sıklığı | cdm_benefitcalculationfrequency |
| Kazanç Hesaplama sıklığı ödeme dönemi | cdm_benefitcalculationfrequencypayperiod |
| Kazanç hesaplama oranı | cdm_benefitcalculationrate |
| Kazanç hesaplama oranı ayrıntısı | cdm_benefitcalculationratedetail |
| Kazanç seçeneği | cdm_benefitoption |
| Kazanç planı | cdm_benefitplan (özel alan desteği için etkinleştirilmedi) |
| Kazanç Türü | cdm_benefittype |
| İş Süreci Takvimi | cdm_businessprocesscalendar |
| İş Süreci Grup Ataması | cdm_businessprocessgroupassignment |
| İş Süreci Kitaplığı Görev Grubu | cdm_businessprocesslibrarytaskgroup |
| İş Süreci Aşaması | cdm_businessprocessstage |
| Denetim Listesi Şablonu Başlığı | cdm_businessprocesstemplateheader |
| Denetim Listesi Şablonu Görevi | cdm_businessprocesstemplatetask |
| Şirket | cdm_company |
| Sabit ücret planı | cdm_compensationfixedplan |
| Ücret Izgarası | cdm_compensationgrid |
| Ücret Düzeyi | cdm_compensationlevel |
| Maaş ödeme sıklığı | cdm_compensationpayfrequency |
| Ücret referans noktası ayarı | cdm_compensationreferencepointsetup |
| Ücret referans noktalarını ayar çizgisi | cdm_compensationreferencepointsetupline |
| Ücret Bölgesi | cdm_compensationregion |
| Maaş yapısı | cdm_compensationstructure |
| Değişken Ücret Planı | cdm_compensationvariableplan |
| Değişken Ücret Planı Düzeyi | cdm_compensationvariableplanlevel |
| Değişken Ücret Planı Türü | cdm_compensationvariableplantype |
| Departman | cdm_department |
| İstihdam | cdm_employment |
| Etnik Kökeni | cdm_ethnicorigin |
| Sabit Ücret Etkinliği | cdm_fixedcompensationevent |
| Görev | cdm_job |
| İş İşlevi | cdm_jobfunction |
| İş Pozisyonu | cdm_jobposition |
| İş Türü | cdm_jobtype |
| Dil | cdm_language |
| Ayrılma Banka hareketi | cdm_leavebanktransaction |
| Ayrılma Kaydı | cdm_leaveenrollment |
| İzin Planı | cdm_leaveplan |
| İzin İsteği | cdm_leaverequest |
| Ayrılma talebi ayrıntıları | cdm_leaverequestdetail |
| İzin Türü | cdm_leavetype |
| İzin Türü Neden Kodu | cdm_leavetypereasoncode |
| Ödeme Döngüsü | cdm_paycycle |
| Ödeme Dönemi | cdm_payperiod |
| Bordro kazanç kodu | cdm_payrollearningcode |
| Kişi kimliği veren acentesi | cdm_personidentificationissuingagency |
| Pozisyon türü | cdm_positiontype |
| Pozisyon çalışan ataması | cdm_positionworkerassignmentmap |
| Neden Kodu | cdm_reasoncode |
| Yetenek türü | cdm_skilltype |
| Vergi bölgesi | cdm_taxregion |
| Hakediş Ödeme Kuralı | cdm_vestingrule |
| Gazilik Durumu | cdm_veteranstatus |
| İş Takvimi | cdm_workcalendar |
| İş Takvimi Gün | cdm_workcalendarday |
| İş Takvimi Tatili |cdm_workcalendarholiday |
| Çalışma takvimi tatil satırı | cdm_workcalendarholidayline |
| Çalışma Takvimi Zaman Aralığı | cdm_workcalendartimeinterval (özel alan desteği için etkinleştirilmedi) |
| Çalışan | cdm_worker |
| Çalışan Adresi | cdm_workeraddress |
| Çalışan banka hesabı | cdm_workerbankaccount |
| Çalışan ücreti sabit | cdm_workerfixedcompensation |
| Çalışan Kişisel Ayrıntıları | cdm_workerpersonaldetail |
| Çalışan Kişi Tanımlama Numarası | cdm_workerpersonidentificationnumber |
| Çalışan Kişi Tanımlama Türü | cdm_workerpersonidentificationtype |

## <a name="in-preview"></a>Ön izlemede

Önizleme özellikleri yalnızca **korumalı alan** ortamlarında etkinleştirilecek.

### <a name="print-performance-reviews"></a>Performans incelemelerini yazdırma

Dynamics 365: 2019 sürüm dalgası 2 planındaki [Performans incelemelerini yazdır](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-talent/print-performance-reviews) konusuna bakın.
