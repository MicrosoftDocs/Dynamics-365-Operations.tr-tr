---
title: Bordro değişken ücret planı
description: Bu konu, Dynamics 365 Human Resources'taki Bordro değişken ücret planı varlığıyla ilgili ayrıntılı bilgi ve örnek bir sorgu sağlar.
author: marcelbf
ms.date: 06/15/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: marcelbf
ms.search.validFrom: 2021-06-15
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: f2f057fb0f492efd08674b3bbeef9f3fec3d7be0
ms.sourcegitcommit: 3a7f1fe72ac08e62dda1045e0fb97f7174b69a25
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/31/2022
ms.locfileid: "8068471"
---
# <a name="payroll-variable-compensation-plan"></a>Bordro değişken ücret planı


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Bu konuda, Dynamics 365 Human Resources için bordro değişken ücret planı varlığı açıklanmaktadır.

### <a name="description"></a>Tanım

Bu varlık, bir çalışanın belirli bir pozisyonu için atanan değişken ücret planını sağlar.

Fiziksel ad: mshr_payrollvariablecompensationawardentity.

## <a name="properties"></a>Özellikler

| Özellik</br>**Fiziksel ad**</br>**_Türü_** | Kullan | Tanım |
| --- | --- | --- |
| **Personel numarası**</br>mshr_personnelnumber</br>*Dize* | Salt okunur | Çalışanın benzersiz personel numarası.  |
| **İkramiye tarihi**</br>mshr_awarddate</br>*Tarih Saat Sapması* | Salt okunur | İkramiye tarihi. |
| **İkramiye türü**</br>mshr_awardtype</br>*[mshr_HrmCompVarAwardEmplType seçenek kümesi](hr-admin-integration-payroll-api-award-type.md)* | Salt okunur | Değişken ücret planı için tanımlanan ikramiye türü. |
| **Para Birimi**</br>mshr_unitcurrencycode</br>*Dize* | Salt okunur |Değişken ücret planı için tanımlanan para birimi.   |
| **Sabit ücret planı kodu**</br>mshr_fixedplanid</br>*Dize* | Salt okunur | İkramiyenin hesaplanmasında temel olarak kullanılan sabit ücret planı. |
| **Birim değeri**</br>mshr_awardamount</br>*Ondalık* | Salt okunur | Birimin değeri |
| **İşlem türü**</br>mshr_processtype</br>*[mshr_hrmCompProcessType seçenek kümesi](hr-admin-integration-payroll-api-process-type.md)* | Salt okunur | İşlem türü. |
| **Değişken ücret planı türü**</br>Dize</br>*mshr_typeid* | Salt okunur | Değişken ücret planı türü. |
| **Değişken ücret planı kodu**</br>Dize</br>*mshr_planid* | Salt okunur | Değişken ücret planı kodu. |
| **Birim sayısı**</br>Ondalık</br>*mshr_numberofunits* | Salt okunur | İkramiyenin birim sayısı. |
| **Birincil alan**</br>mshr_primaryfield</br>*GUID* | Salt okunur</br>Sistem tarafından oluşturulan. | |
| **Bordro Değişken Ücret Planı varlığı**</br>mshr_payrollvariablecompensationawardentityid</br>*GUID* | Sistem tarafından oluşturulan | Ücret planını benzersiz olarak tanımlamak için sistem tarafından oluşturulan GUID değeri. |

## <a name="relations"></a>İlişkiler 

|Özellik değeri | İlgili varlık | Gezinti özelliği | Tahsilat türü |
| --- | --- | --- | --- |
| _mshr_fk_employee_id_value | [mshr_payrollemployeeentity](hr-admin-integration-payroll-api-payroll-employee.md) | mshr_FK_Employee_id | mshr_FK_PayrollEmployeeEntity_VariableCompAward |
| _mshr_fk_fixedcomp_id_value | [mshr_payrollfixedcompensationplanentity](hr-admin-integration-payroll-api-payroll-fixed-compensation-plan.md) | mshr_FK_FixedComp_id | mshr_FK_PayrollFixedCompensationPlanEntity_VariableCompAward |

## <a name="example-query"></a>Örnek sorgu

**İstek**

```http
GET [Organizaton URI]/api/data/v9.1/mshr_payrollvariablecompensationawardentities?$filter=mshr_personnelnumber eq '000046'
```

**Yanıt**

```json
{
    "mshr_personnelnumber": "000046",
    "mshr_awarddate": "2015-01-15T00:00:00Z",
    "mshr_awardtype": 200000000,
    "mshr_unitcurrencycode": "USD",
    "mshr_fixedplanid": "",
    "mshr_unitvalue": 1,
    "mshr_processtype": 200000003,
    "mshr_typeid": "Bonus",
    "mshr_planid": "MgBonus",
    "mshr_numberofunits": 1500,
    "mshr_primaryfield": "000046 | MgBonus | Bonus | 1/15/2015",
    "_mshr_fk_employee_id_value": "00000666-0000-0000-daff-004105000000",
    "mshr_payrollvariablecompensationawardentityid": "000001a4-0000-0000-0d00-005001000000",
    "_mshr_fk_fixedcomp_id_value": null
}
```

## <a name="see-also"></a>Ayrıca bkz.

[Bordro tümleştirme API'sına giriş](hr-admin-integration-payroll-api-introduction.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
