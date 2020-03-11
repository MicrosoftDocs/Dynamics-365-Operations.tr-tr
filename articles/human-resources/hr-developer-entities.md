---
title: Common Data Service varlıkları
description: Microsoft Dynamics 365 Human Resources, Common Data Service genişletilebilirlik ve tümleştirme senaryolarını etkinleştirmek için kullanılır.
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 6879a45dd1fcc1ba718747aaaf0d7936c2eac49f
ms.sourcegitcommit: 3cad15f8ecc257d3a45c1bc1fada7c094ff4bcec
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/26/2020
ms.locfileid: "3087358"
---
# <a name="common-data-service-entities"></a>Common Data Service varlıkları

Microsoft Dynamics 365 Human Resources, Common Data Service genişletilebilirlik ve tümleştirme senaryolarını etkinleştirmek için kullanılır.

Common Data Service hakkında daha fazla bilgi için bkz. [Common Data Service nedir?](https://docs.microsoft.com/powerapps/maker/common-data-service/data-platform-intro).

Aşağıdaki İnsan Kaynakları varlıkları Common Data Service'de kullanılabilir.

## <a name="benefit-entities"></a>Yarar varlıkları

| Dosya Adı | Varlık |
| --- | --- |
| Kazanç Hesaplama Sıklığı | cdm_benefitcalculationfrequency |
| Kazanç Hesaplama sıklığı ödeme dönemi | cdm_benefitcalculationfrequencypayperiod |
| Kazanç hesaplama oranı | cdm_benefitcalculationrate |
| Kazanç hesaplama oranı ayrıntısı | cdm_benefitcalculationratedetail |
| Kazanç seçeneği | cdm_benefitoption |
| Kazanç planı | cdm_benefitplan (özel alan desteği için etkinleştirilmedi) |
| Kazanç Türü | cdm_benefittype |

## <a name="business-process-tasks-entities"></a>İş işlemi görevleri varlıkları

| Dosya Adı | Varlık |
| --- | --- |
| İş Süreci Takvimi | cdm_businessprocesscalendar |
| İş Süreci Grup Ataması | cdm_businessprocessgroupassignment |
| İş Süreci Kitaplığı Görev Grubu | cdm_businessprocesslibrarytaskgroup |
| İş Süreci Aşaması | cdm_businessprocessstage |
| Denetim Listesi Şablonu Başlığı | cdm_businessprocesstemplateheader |
| Denetim Listesi Şablonu Görevi | cdm_businessprocesstemplatetask |

## <a name="compensation-entities"></a>Ücret varlıkları

| Dosya Adı | Varlık |
| --- | --- |
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
| Sabit Ücret Etkinliği | cdm_fixedcompensationevent |
| Hakediş Ödeme Kuralı | cdm_vestingrule |
| Çalışan ücreti sabit | cdm_workerfixedcompensation |

## <a name="organization-entities"></a>Kuruluş varlıkları

| Dosya Adı | Varlık |
| --- | --- |
| Departman | cdm_department |
| İstihdam | cdm_employment |
| Şirket | cdm_company |
| Görev | cdm_job |
| İş İşlevi | cdm_jobfunction |
| İş Pozisyonu | cdm_jobposition |
| Pozisyon türü | cdm_positiontype |
| Pozisyon çalışan ataması | cdm_positionworkerassignmentmap |
| İş Türü | cdm_jobtype |
| Dil | cdm_language |

## <a name="leave-and-absence-entities"></a>İzin ve devamsızlık varlıkları

| Dosya Adı | Varlık |
| --- | --- |
| Ayrılma Banka hareketi | cdm_leavebanktransaction |
| Ayrılma Kaydı | cdm_leaveenrollment |
| İzin Planı | cdm_leaveplan |
| İzin İsteği | cdm_leaverequest |
| Ayrılma talebi ayrıntıları | cdm_leaverequestdetail |
| İzin Türü | cdm_leavetype |
| İzin Türü Neden Kodu | cdm_leavetypereasoncode |

## <a name="payroll-entities"></a>Bordro varlıkları

| Dosya Adı | Varlık |
| --- | --- |
| Ödeme Döngüsü | cdm_paycycle |
| Ödeme Dönemi | cdm_payperiod |
| Bordro kazanç kodu | cdm_payrollearningcode |
| Banka hesabı ödemeleri | cdm_bankaccountdisbursement |
| Vergi bölgesi | cdm_taxregion |

## <a name="worker-entities"></a>Çalışan kişilikler

| Dosya Adı | Varlık |
| --- | --- |
| Çalışan | cdm_worker |
| Çalışan Adresi | cdm_workeraddress |
| Çalışan Kişisel Ayrıntıları | cdm_workerpersonaldetail |
| Çalışan Kişi Tanımlama Numarası | cdm_workerpersonidentificationnumber |
| Çalışan Kişi Tanımlama Türü | cdm_workerpersonidentificationtype |
| İş Takvimi | cdm_workcalendar |
| İş Takvimi Gün | cdm_workcalendarday |
| İş Takvimi Tatili |cdm_workcalendarholiday |
| Çalışma takvimi tatil satırı | cdm_workcalendarholidayline |
| Çalışma Takvimi Zaman Aralığı | cdm_workcalendartimeinterval (özel alan desteği için etkinleştirilmedi) |
| Çalışan banka hesabı | cdm_workerbankaccount |

## <a name="worker-setup-entities"></a>Çalışan kurulum varlıkları

| Dosya Adı | Varlık |
| --- | --- |
| Gazilik Durumu | cdm_veteranstatus |
| Etnik Kökeni | cdm_ethnicorigin |
| Neden Kodu | cdm_reasoncode |
| Kişi kimliği veren acentesi | cdm_personidentificationissuingagency |

## <a name="competency-entities"></a>Yetki tüzel kişilikler

| Dosya Adı | Varlık |
| --- | --- |
| Yetenek türü | cdm_skilltype |

## <a name="entity-relationship-models"></a>Varlık ilişki modelleri

### <a name="worker"></a>Çalışan

![Çalışan](./media/HCMCommon-worker-entity-diagram.png)

### <a name="job-and-job-position"></a>İş ve Iş pozisyonu

![İş ve Iş pozisyonu](./media/HCMCommon-job-and-job-position-entity-diagram.png)

### <a name="benefits"></a>Kazançlar

![Kazançlar](./media/HCMCommon-benefits-entity-diagram.png)

### <a name="compensation"></a>Ücret

![Ücret](./media/HCMCommon-compensation-entity-diagram.png)

### <a name="leave"></a>Bırak

![Bırak](./media/HCMCommon-leave-entity-diagram.png)

### <a name="work-calendar"></a>İş Takvimi

![İş Takvimi](./media/HCMCommon-work-calendar-entity-diagram.png)

## <a name="see-also"></a>Ayrıca bkz.

[Veri tümleştirme teknolojisi seçme](hr-admin-integration-choose-technology.md)</br>
[Common Data Service tümleştirmesini yapılandırma](hr-admin-integration-common-data-service.md)