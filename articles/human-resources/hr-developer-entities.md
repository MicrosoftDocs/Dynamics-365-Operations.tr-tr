---
title: Dataverse tabloları
description: Microsoft Dynamics 365 Human Resources, Dataverse genişletilebilirlik ve tümleştirme senaryolarını etkinleştirmek için kullanılır.
author: andreabichsel
ms.date: 01/25/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: c405d933adff08e2a4ce12dc53329f10a9ae89b7
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/06/2021
ms.locfileid: "6346310"
---
# <a name="dataverse-tables"></a>Dataverse tabloları

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Microsoft Dynamics 365 Human Resources, Dataverse genişletilebilirlik ve tümleştirme senaryolarını etkinleştirmek için kullanılır.

> [!NOTE]
> Human Resources varlıkları Dataverse tablolarına karşılık gelir. Dataverse (önceden Common Data Service) ve terminoloji güncelleştirmeleri hakkında daha fazla bilgi için bkz. [Microsoft Dataverse nedir?](/powerapps/maker/data-platform/data-platform-intro)

Aşağıdaki Dataverse tabloları Human Resources varlıklarına göre kullanılabilir.

## <a name="benefit-tables"></a>Fayda tabloları

| Kuruluş adı | Tablo |
| --- | --- |
| Kazanç Hesaplama Sıklığı | cdm_benefitcalculationfrequency |
| Kazanç Hesaplama sıklığı ödeme dönemi | cdm_benefitcalculationfrequencypayperiod |
| Kazanç hesaplama oranı | cdm_benefitcalculationrate |
| Kazanç hesaplama oranı ayrıntısı | cdm_benefitcalculationratedetail |
| Kazanç seçeneği | cdm_benefitoption |
| Kazanç planı | cdm_benefitplan (özel alan desteği için etkinleştirilmedi) |
| Kazanç Türü | cdm_benefittype |

## <a name="business-process-tasks-tables"></a>İş süreci görevleri tabloları

| Kuruluş adı | Tablo |
| --- | --- |
| İş Süreci Takvimi | cdm_businessprocesscalendar |
| İş Süreci Grup Ataması | cdm_businessprocessgroupassignment |
| İş Süreci Kitaplığı Görev Grubu | cdm_businessprocesslibrarytaskgroup |
| İş Süreci Aşaması | cdm_businessprocessstage |
| Denetim Listesi Şablonu Başlığı | cdm_businessprocesstemplateheader |
| Denetim Listesi Şablonu Görevi | cdm_businessprocesstemplatetask |

## <a name="compensation-tables"></a>Ücret tabloları

| Kuruluş adı | Tablo |
| --- | --- |
| Ücret Sabit Planı | cdm_compensationfixedplan |
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
| Sabit Ücret Etkinliği | cdm_fixedcompensationevent |
| Hakediş Ödeme Kuralı | cdm_vestingrule |
| Çalışan Sabit Ücreti | cdm_workerfixedcompensation |

## <a name="organization-tables"></a>Kuruluş tabloları

| Kuruluş adı | Tablo |
| --- | --- |
| Departman | cdm_department |
| İstihdam | cdm_employment |
| Şirket | cdm_company |
| Görev | cdm_job |
| İş İşlevi | cdm_jobfunction |
| İş Pozisyonu | cdm_jobposition |
| Pozisyon türü | cdm_positiontype |
| Pozisyon Çalışan Ataması | cdm_positionworkerassignmentmap |
| İş Pozisyonu Boyutu | cdm_jobpositiondimension|
| İş Türü | cdm_jobtype |
| Dil | cdm_language |
| Ünvan | cdm_title |

> [!NOTE]
> **Pozisyon türü**, **çalışan ataması pozisyon** ve **istihdam** için mali boyutlar Dataverse'e tek-yön tümleştirmesi sağlar. Mali boyut güncelleştirmeleri şu an için Dataverse'tan Human Resources ile eşitlenmez. 

## <a name="leave-and-absence-tables"></a>İzin ve devamsızlık tabloları

| Kuruluş adı | Tablo |
| --- | --- |
| İzin Bankası Hareketi | cdm_leavebanktransaction |
| İzin Kaydı | cdm_leaveenrollment |
| İzin Planı | cdm_leaveplan |
| İzin İsteği | cdm_leaverequest |
| Ayrılma talebi ayrıntıları | cdm_leaverequestdetail |
| İzin Türü | cdm_leavetype |
| İzin Türü Neden Kodu | cdm_leavetypereasoncode |

## <a name="payroll-tables"></a>Bordro tabloları

| Kuruluş adı | Tablo |
| --- | --- |
| Ödeme Döngüsü | cdm_paycycle |
| Ödeme Dönemi | cdm_payperiod |
| Bordro Kazanç Kodu | cdm_payrollearningcode |
| Banka hesabı ödemeleri | cdm_bankaccountdisbursement |
| Vergi Bölgesi | cdm_taxregion |

## <a name="worker-tables"></a>Çalışan tabloları

| Kuruluş adı | Tablo |
| --- | --- |
| Çalışan | cdm_worker |
| Çalışan Adresi | cdm_workeraddress |
| Çalışan Kişisel Bilgisi | cdm_workerpersonaldetail |
| Çalışan Kişi Tanımlama Numarası | cdm_workerpersonidentificationnumber |
| Çalışan Kişi Tanımlama Türü | cdm_workerpersonidentificationtype |
| İş Takvimi | cdm_workcalendar |
| İş Takvimi Gün | cdm_workcalendarday |
| İş Takvimi Tatili |cdm_workcalendarholiday |
| Çalışma takvimi tatil satırı | cdm_workcalendarholidayline |
| Çalışma Takvimi Zaman Aralığı | cdm_workcalendartimeinterval (özel alan desteği için etkinleştirilmedi) |
| Çalışan Banka Hesabı | cdm_workerbankaccount |

## <a name="worker-setup-tables"></a>Çalışan kurulum tabloları

| Kuruluş adı | Tablo |
| --- | --- |
| Gazilik Durumu | cdm_veteranstatus |
| Etnik Köken | cdm_ethnicorigin |
| Neden Kodu | cdm_reasoncode |
| Kişi Kimliğini Düzenleyen Kurum | cdm_personidentificationissuingagency |

## <a name="competency-tables"></a>Yetkinlik tabloları

| Kuruluş adı | Tablo |
| --- | --- |
| Yetenek Türü | cdm_skilltype |

## <a name="table-relationship-models"></a>Tablo ilişkisi modelleri

### <a name="worker"></a>Çalışan

![Çalışan.](./media/HCMCommon-worker-entity-diagram.png)

### <a name="job-and-job-position"></a>İş ve Iş pozisyonu

![İş ve Iş pozisyonu.](./media/HCMCommon-job-and-job-position-entity-diagram.png)

### <a name="benefits"></a>Kazançlar

![Kazançlar.](./media/HCMCommon-benefits-entity-diagram.png)

### <a name="compensation"></a>Maaş

![Ücret.](./media/HCMCommon-compensation-entity-diagram.png)

### <a name="leave"></a>İzin

![İzin.](./media/HCMCommon-leave-entity-diagram.png)

### <a name="work-calendar"></a>İş Takvimi

![İş Takvimi.](./media/HCMCommon-work-calendar-entity-diagram.png)

## <a name="see-also"></a>Ayrıca bkz.

[Veri tümleştirme teknolojisi seçme](hr-admin-integration-choose-technology.md)<br>
[Dataverse tümleştirmesini yapılandırma](hr-admin-integration-common-data-service.md)<br>
[Dataverse sanal tablolarını yapılandırma](hr-admin-integration-common-data-service-virtual-entities.md)<br>
[Human Resources sanal tablolarıyla ilgili SSS](hr-admin-virtual-entity-faq.md)<br>
[Microsoft Dataverse nedir?](/powerapps/maker/data-platform/data-platform-intro)<br>
[Terminoloji güncelleştirmeleri](/powerapps/maker/data-platform/data-platform-intro#terminology-updates)


[!INCLUDE[footer-include](../includes/footer-banner.md)]