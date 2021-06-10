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
ms.openlocfilehash: 8918044dbf84e79015dc3bca904f204123a37db8
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/18/2021
ms.locfileid: "6056792"
---
# <a name="payroll-position"></a>Bordrolu pozisyon

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Bu konu, Dynamics 365 Human Resources'taki Pozisyonlar varlığı Bordro ayrıntılarına ilişkin bilgi ve örnek bir sorgu sağlar.

## <a name="properties"></a>Özellikler

| Özellik<br>**Fiziksel ad**<br>**_Türü_** | Kullan | Tanım |
| --- | --- | --- |
| **Yıllık mesai saatleri**<br>annualregularhours<br>*Ondalık* | Salt okunur<br>Gerekli | Pozisyonda tanımlanan yıllık düzenli saatler.  |
| **Bordro pozisyon ayrıntıları varlık kimliği**<br>payrollpositiondetailsentityid<br>*Guid* | Gerekli<br>Sistem tarafından oluşturulan. | Pozisyonu benzersiz olarak tanımlamak için sistem tarafından oluşturulan GUID değeri.  |
| **Birincil alan**<br>mshr_primaryfield<br>*Dize* | Gerekli<br>Sistem tarafından oluşturulan |  |
| **Pozisyon iş kimliği değeri**<br>_mshr_fk_positionjob_id_value<br>*GUID* | Salt okunur<br>Gerekli<br>Yabancı anahtar: mshr_payrollpositionjobentity için mshr_PayrollPositionJobEntity |Pozisyonla ilişkili işin kimliği.|
| **Sabit ücret planı kimlik değeri**<br>_mshr_fk_fixedcompplan_id_value<br>*GUID* | Salt okunur<br>Gerekli<br>Yabancı anahtar: mshr_payrollfixedcompensationplanentity içinmshr_FixedCompPlan_id  | Pozisyonla ilişkili sabit ücret planının kimliği. |
| **Ödeme döngüsü kimliği**<br>mshr_primaryfield<br>*Dize* | Salt okunur<br>Gerekli | Pozisyonda tanımlanan ödeme döngüsü. |
| **Tüzel kişilik tarafından ödenen**<br>paidbylegalentity<br>*Dize* | Salt okunur<br>Gerekli | Ödemeyi yapmak için sorumlu pozisyonda tanımlanan tüzel kişilik. |
| **Pozisyon kodu**<br>mshr_positionid<br>*Dize* | Salt okunur<br>Gerekli | Pozisyonun kimliği. |
| **Geçerlilik bitişi**<br>validto<br>*Tarih Saat Sapması* | Salt okunur<br>Gerekli |Pozisyon ayrıntılarının geçerlilik başlangıç tarihi.  |
| **Geçerlilik başlangıcı**<br>validfrom<br>*Tarih Saat Sapması* | Salt okunur<br>Gerekli |Pozisyon ayrıntılarının geçerlilik bitiş tarihi.  |

**Sorgu**

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
