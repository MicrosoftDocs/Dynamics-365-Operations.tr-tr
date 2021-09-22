---
title: Bordro sabit ücret planı
description: Bu konu, Dynamics 365 Human Resources'taki Bordro sabit ücret planı varlığıyla ilgili ayrıntılı bilgi ve örnek bir sorgu sağlar.
author: jcart
ms.date: 08/25/2021
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
ms.openlocfilehash: dcb253fabbb183003048119c7a627bf0ab960050
ms.sourcegitcommit: 4d11061f5de0ddba1f968bd5c3fd694a8b104ccc
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/26/2021
ms.locfileid: "7429253"
---
# <a name="payroll-fixed-compensation-plan"></a>Bordro sabit ücret planı

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Bu konuda, Dynamics 365 Human Resources için bordro sabit ücret planı varlığı açıklanmaktadır.

### <a name="description"></a>Tanım

Bu varlık, bir çalışanın belirli bir pozisyonu için atanan sabit ücret planını sağlar.

Fiziksel ad: mshr_payrollfixedcompensationplanentity.

## <a name="properties"></a>Özellikler

| Özellik</br>**Fiziksel ad**</br>**_Türü_** | Kullan | Tanım |
| --- | --- | --- |
| **Plan Kodu**</br>mshr_planid</br>*Dize* | Salt okunur | Ücret planını belirtir.  |
| **Personel numarası**</br>mshr_personnelnumber</br>*Dize* | Salt okunur | Çalışanın benzersiz personel numarası. |
| **Ödeme oranı**</br>mshr_payrate</br>*Ondalık* | Salt okunur | Sabit ücret planında tanımlanan ödeme oranı. |
| **Pozisyon kodu**</br>mshr_positionid</br>*Dize* | Salt okunur | Çalışan ve sabit ücret planı kaydı ile ilişkili pozisyon kimliği. |
| **Geçerlilik başlangıcı**</br>mshr_validfrom</br>*Tarih Saat Sapması* |  Salt okunur | Personel sabit ücretinin geçerlilik başlangıç tarihi.  |
| **Geçerlilik bitişi**</br>mshr_validto</br>*Tarih Saat Sapması* | Salt okunur | Personel sabit ücretinin geçerlilik bitiş tarihi. |
| **Ödeme sıklığı**</br>mshr_payfrequency</br>*Dize* | Salt okunur | Çalışana ödeme yapma sıklığı.  |
| **Para Birimi**</br>mshr_currency</br>*Dize* | Salt okunur | Sabit ücret planı için tanımlanan para birimi. |
| **Bordro Sabit Ücret Planı varlığı**</br>mshr_payrollfixedcompensationplanentityid</br>*GUID* | Sistem tarafından oluşturulan | Ücret planını benzersiz olarak tanımlamak için sistem tarafından oluşturulan GUID değeri. |

## <a name="relations"></a>İlişkiler

|Özellik değeri | İlgili varlık | Gezinti özelliği | Tahsilat türü |
| --- | --- | --- | --- |
| _mshr_fk_employee_id_value | [mshr_payrollemployeeentity](hr-admin-integration-payroll-api-payroll-employee.md) | mshr_FK_Employee_id | mshr_FK_PayrollEmployeeEntity_FixedCompPlan |
| _mshr_fk_job_id_value | [mshr_payrollpositionjobentity](hr-admin-integration-payroll-api-payroll-position-job.md) | mshr_FK_Job_id | mshr_FK_PayrollPositionJobEntity_FixedCompPlan |
| _mshr_fk_payrollposition_id_value | [mshr_payrollpositionentity](hr-admin-integration-payroll-api-payroll-position.md) | mshr_FK_PayrollPosition_id | mshr_FK_PayrollPositionEntity_FixedCompPlan |
| _mshr_fk_plan_id_value | mshr_hcmcompfixedplantableentity | mshr_FK_Plan_id | - |
| _mshr_fk_variablecompaward_id_value | [mshr_payrollvariablecompensationawardentity](hr-admin-integration-payroll-api-payroll-variable-compensation-plan.md) | mshr_FK_VariableCompAward_id | mshr_FK_PayrollVariableCompensationAwardEntity_FixedComp |

## <a name="example-query"></a>Örnek sorgu

**İstek**

```http
GET [Organizaton URI]/api/data/v9.1/mshr_payrollfixedcompensationplanentities?$filter=mshr_personnelnumber eq @personnelnumber and mshr_validfrom le @asofdate and mshr_validto ge @asofdate&@personnelnumber='000041'&@asofdate=2021-04-01
```

**Yanıt**

```json
{
    "mshr_planid": "GradeC",
    "mshr_personnelnumber": "000041",
    "mshr_payrate": 75200,
    "mshr_positionid": "000276",
    "mshr_validfrom": "2011-04-05T00:00:00Z",
    "mshr_validto": "2154-12-31T00:00:00Z",
    "mshr_payfrequency": "Annual",
    "mshr_currency": "USD",
    "_mshr_fk_employee_id_value": "00000d3c-0000-0000-d5ff-004105000000",
    "_mshr_fk_plan_id_value": "0000070c-0000-0000-b328-fef003000000",
    "_mshr_fk_job_id_value": "00010094-0000-0000-df00-014105000000",
    "mshr_payrollfixedcompensationplanentityid": "0000029f-0000-0000-d5ff-004105000000",
    "_mshr_fk_payroll_id_value": null
}
```

## <a name="see-also"></a>Ayrıca bkz.

[Bordro tümleştirme API'sına giriş](hr-admin-integration-payroll-api-introduction.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
