---
title: Bordro sabit ücret planı
description: Bu konu, Dynamics 365 Human Resources'taki Bordro sabit ücret planı varlığıyla ilgili ayrıntılı bilgi ve örnek bir sorgu sağlar.
author: jcart
manager: tfehr
ms.date: 04/07/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2021-04-07
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 78a274cc491041d3d917a50bfb433f667cd8c255
ms.sourcegitcommit: d18d9cdb175c9d42eafbed66352c24b2aa94258b
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/13/2021
ms.locfileid: "5882097"
---
# <a name="payroll-fixed-compensation-plan"></a>Bordro sabit ücret planı

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Bu konu, Dynamics 365 Human Resources'taki Bordro sabit ücret planı varlığıyla ilgili ayrıntılı bilgi ve örnek bir sorgu sağlar.

## <a name="properties"></a>Özellikler

| Özellik<br>**Fiziksel ad**<br>**_Türü_** | Kullan | Tanım |
| --- | --- | --- |
| **Personel kodu**<br>mshr_fk_employee_id_value<br>*GUID* | Salt okunur<br>Gerekli<br>Yabancı anahtar: mshr_payrollemployeeentity entity için mshr_Employee_id  | Personel kodu |
| **Ödeme oranı**<br>mshr_payrate<br>*Ondalık* | Salt okunur<br>Gerekli | Sabit ücret planında tanımlanan ödeme oranı. |
| **Plan Kodu**<br>mshr_planid<br>*Dize* | Salt okunur<br>Gerekli |Ücret planını belirtir.  |
| **Geçerlilik başlangıcı**<br>mshr_validfrom<br>*Tarih Saat Sapması* |  Salt okunur<br>Gerekli |Personel sabit ücretinin geçerlilik başlangıç tarihi.  |
| **Bordro Sabit Ücret Planı varlığı**<br>mshr_payrollfixedcompensationplanentityid<br>*GUID* | Gerekli<br>Sistem tarafından oluşturulan | Ücret planını benzersiz olarak tanımlamak için sistem tarafından oluşturulan GUID değeri. |
| **Ödeme sıklığı**<br>mshr_payfrequency<br>*Dize* | Salt okunur<br>Gerekli |Çalışana ödeme yapma sıklığı.  |
| **Geçerlilik bitişi**<br>mshr_validto<br>*Tarih Saat Sapması* | Salt okunur <br>Gerekli | Personel sabit ücretinin geçerlilik bitiş tarihi. |
| **Pozisyon kodu**<br>mshr_positionid<br>*Dize* | Salt okunur <br>Gerekli | Çalışan ve sabit ücret planı kaydı ile ilişkili pozisyon kimliği. |
| **Para Birimi**<br>mshr_currency<br>*Dize* | Salt okunur <br>Gerekli |Sabit ücret planı için tanımlanan para birimi   |
| **Personel numarası**<br>mshr_personnelnumber<br>*Dize* | Salt okunur<br>Gerekli |Çalışanın benzersiz personel numarası.  |

**Sorgu**

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
