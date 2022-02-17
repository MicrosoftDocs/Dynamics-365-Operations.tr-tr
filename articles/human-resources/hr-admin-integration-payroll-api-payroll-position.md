---
title: Pozisyonlar için bordro ayrıntıları
description: Bu konu, Dynamics 365 Human Resources'taki Pozisyonlar varlığı Bordro ayrıntılarına ilişkin bilgi ve örnek bir sorgu sağlar.
author: jcart
ms.date: 04/07/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2021-04-07
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 2bbb234d2f51391ea65e3d6153d6cee250f3c6dc
ms.sourcegitcommit: 3a7f1fe72ac08e62dda1045e0fb97f7174b69a25
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/31/2022
ms.locfileid: "8069819"
---
# <a name="payroll-position"></a>Bordrolu pozisyon


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Bu konuda, Dynamics 365 Human Resources Bordro Pozisyonları varlığı açıklanmaktadır.

Fiziksel ad: mshr_payrollpositionentity.

### <a name="description"></a>Tanım

Bu varlık belirtilen çalışan için pozisyonla ilgili bilgi sağlar.

Fiziksel ad: mshr_payrollpositionentity.

## <a name="properties"></a>Özellikler

| Özellik</br>**Fiziksel ad**</br>**_Tür_** | Kullan | Tanım |
| --- | --- | --- |
| **Pozisyon kodu**</br>mshr_positionid</br>*Dize* | Salt okunur | Pozisyonun kimliği. |
| **Ödeme döngüsü kimliği**</br>mshr_paycycleid</br>*Dize* | Salt okunur | Pozisyonda tanımlanan ödeme döngüsü. |
| **Yıllık mesai saatleri**</br>annualregularhours</br>*Ondalık* | Salt okunur | Pozisyonda tanımlanan yıllık düzenli saatler. |
| **Tüzel kişilik tarafından ödenen**</br>paidbylegalentity</br>*Dize* | Salt okunur | Pozisyonda tanımlanan ve ödeme yapmaktan sorumlu olan tüzel kişilik. |
| **Geçerlilik bitişi**</br>validto</br>*Tarih Saat Sapması* | Salt okunur | Pozisyon ayrıntılarının geçerlilik bitiş tarihi. |
| **Geçerlilik başlangıcı**</br>validfrom</br>*Tarih Saat Sapması* | Salt okunur | Pozisyon ayrıntılarının geçerlilik başlangıcı tarihi. |
| **Birincil alan**</br>mshr_primaryfield</br>*Dize* | Sistem tarafından oluşturulan | Birincil alan. |
| **Bordro pozisyon ayrıntıları varlık kimliği**</br>payrollpositiondetailsentityid</br>*Guid* | Gerekli</br>Sistem tarafından oluşturulan. | Pozisyonu benzersiz bir şekilde tanımlamak için sistem tarafından oluşturulan genel benzersiz tanımlayıcı (GUID) değeri. |

## <a name="relations"></a>İlişkiler

| Özellik değeri | İlgili varlık | Gezinti özelliği | Tahsilat türü |
| --- | --- | --- | --- |
| _mshr_fk_fixedcompplan_id_value | [mshr_payrollfixedcompensationplanentity](hr-admin-integration-payroll-api-payroll-fixed-compensation-plan.md) | mshr_FK_FixedCompPlan_id | mshr_FK_PayrollFixedCompensationPlanEntity_PayrollPosition |
| _mshr_fk_hcmpositionhierarchy_id_value | mshr_hcmpositionhierarchyentity | mshr_FK_HcmPositionHierarchy_id | Geçerli değil |
| _mshr_fk_job_id_value | mshr_payrollpositionjobentity | mshr_FK_Job_id | mshr_FK_PayrollPositionJobEntity_Payroll |
| _mshr_fk_positionassignmentv2_id_value | mshr_hcmpositionworkerassignmentv2entity | mshr_FK_PositionAssignmentV2_id | Geçerli değil |

## <a name="example-query"></a>Örnek sorgu

**İstek**

```http
GET [Organizaton URI]/api/data/v9.1/mshr_payrollpositionentities?$filter=mshr_positionid eq @positionid and mshr_validfrom le @asofdate and mshr_validto ge @asofdate&@positionid='000276'&@asofdate=2021-04-01
```

**Yanıt**

```json
{
    "mshr_positionid": "000276",
    "mshr_paycycleid": "w",
    "mshr_annualregularhours": 3000,
    "mshr_paidbylegalentity": "USMF",
    "mshr_validfrom": "2021-03-14T00:00:00Z",
    "mshr_validto": "2154-12-31T00:00:00Z",
    "mshr_primaryfield": "000276 | 3/14/2021",
    "_mshr_fk_job_id_value": "00010094-0000-0000-df00-014105000000",
    "_mshr_fk_fixedcompplan_id_value": "0000029f-0000-0000-d5ff-004105000000",
    "mshr_payrollpositionentityid": "00010097-0000-0000-df00-014105000000"
}
```

## <a name="see-also"></a>Ayrıca bkz.

[Bordro tümleştirme API'sına giriş](hr-admin-integration-payroll-api-introduction.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
