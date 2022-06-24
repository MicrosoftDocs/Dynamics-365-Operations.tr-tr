---
title: Bordrolu pozisyon işi
description: Bu makalede, Dynamics 365 Human Resources'daki Bordrolu pozisyon işi varlığıyla ilgili ayrıntılı bilgi ve örnek bir sorgu sağlanmaktadır.
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
ms.openlocfilehash: fa347f4b99adc7c29d69daf62ad2bbfc14726a19
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8864097"
---
# <a name="payroll-position-job"></a>Bordrolu pozisyon işi


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Bu makalede, Dynamics 365 Human Resources Bordrolu pozisyon işi varlığı açıklanmaktadır.

### <a name="description"></a>Açıklama

Bu varlık, belirli bir sabit ücret planı için pozisyon ile iş arasındaki ilişkiyi sağlar.

Fiziksel ad: mshr_payrollpositionjobentity.

## <a name="properties"></a>Özellikler

| Özellik</br>**Fiziksel ad**</br>**_Tür_** | Kullan | Tanım |
| --- | --- | --- |
| **Pozisyon kodu**</br>mshr_positionid</br>*Dize* | Salt okunur | Pozisyonun kimliği. |
| **Geçerlilik başlangıcı**</br>mshr_validto</br>*Tarih Saat Sapması* | Salt okunur | Pozisyon ve iş ilişkisinin geçerlilik başlangıç tarihi. |
| **Geçerlilik bitişi**</br>mshr_validto</br>*Tarih Saat Sapması* | Salt okunur | Pozisyon ve iş ilişkisinin geçerlilik bitiş tarihi. |
| **İş Kodu**</br>mshr_jobid</br>*Dize* | Salt okunur | İşin kimliği. |
| **Birincil alan**</br>mshr_primaryfield</br>*Dize* | Sistem tarafından oluşturulan | Birincil alan. |
| **Bordro pozisyon iş varlığı kimliği**</br>mshr_payrollpositionjobentityid</br>*Guid* | Sistem tarafından oluşturulan. | İşi benzersiz bir şekilde tanımlamak için sistem tarafından oluşturulan genel benzersiz tanımlayıcı (GUID) değeri. |

## <a name="relations"></a>İlişkiler

| Özellik değeri | İlgili varlık | Gezinti özelliği | Tahsilat türü |
| --- | --- | --- | --- |
| _mshr_fk_fixedcompplan_id_value | mshr_payrollfixedcompensationplanentity | mshr_FK_FixedCompPlan_id | mshr_FK_PayrollFixedCompensationPlanEntity_Job |
| _mshr_fk_jobdetail_id_value | mshr_hcmjobdetailentity | mshr_FK_JobDetail_id | Geçerli değil |
| _mshr_fk_payroll_id_value | mshr_payrollpositionentity | mshr_FK_Payroll_id | mshr_FK_PayrollPositionEntity_Job |

## <a name="example-query"></a>Örnek sorgu

**İstek**

```http
GET [Organizaton URI]/api/data/v9.1/mshr_payrollpositionjobentities?$filter=mshr_positionid eq '000276'
```

**Yanıt**

```json
{
    "mshr_positionid": "000276",
    "mshr_validfrom": "2016-07-06T18:11:33Z",
    "mshr_validto": "2154-12-31T23:59:59Z",
    "mshr_jobid": "Accountant",
    "mshr_primaryfield": "000276 | Accountant | 7/6/2016 06:11:33 pm",
    "_mshr_fk_jobdetail_id_value": "00000b8d-0000-0000-b0ff-004105000000",
    "_mshr_fk_fixedcompplan_id_value": "0000058a-0000-0000-d5ff-004105000000",
    "_mshr_fk_payroll_id_value": "00000427-0000-0000-df00-014105000000",
    "mshr_payrollpositionjobentityid": "00000906-0000-0000-df00-014105000000"
}
```

## <a name="see-also"></a>Ayrıca bkz.

[Bordro tümleştirme API'sına giriş](hr-admin-integration-payroll-api-introduction.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
