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
ms.openlocfilehash: 05e9d6441cf99dce3f4663b9d5ba57e2b386e8c2f3060f75550270083f3b98b3
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/05/2021
ms.locfileid: "6741465"
---
# <a name="payroll-position"></a>Bordrolu pozisyon

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Bu konuda, Dynamics 365 Human Resources Bordro Pozisyonları varlığı açıklanmaktadır.

Fiziksel ad: mshr_payrollpositionentity.

### <a name="description"></a>Tanım

Bu varlık belirtilen çalışan için pozisyonla ilgili bilgi sağlar.

Fiziksel ad: 

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
