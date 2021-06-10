---
title: Bordrolu pozisyon işi
description: Bu konu, Dynamics 365 Human Resources'taki Bordro pozisyon iş varlığıyla ilgili ayrıntılı bilgi ve örnek bir sorgu sağlar.
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
ms.openlocfilehash: 62b9caf94f1c9aa8bb5758e62565fe57dfdd245a
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/18/2021
ms.locfileid: "6055040"
---
# <a name="payroll-position-job"></a>Bordrolu pozisyon işi

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Bu konu, Dynamics 365 Human Resources'taki Bordrolu pozisyon iş ilişkisi varlığıyla ilgili ayrıntılı bilgi ve örnek bir sorgu sağlar.

## <a name="properties"></a>Özellikler

| Özellik<br>**Fiziksel ad**<br>**_Türü_** | Kullan | Tanım |
| --- | --- | --- |
| **İş Kodu**<br>mshr_jobid<br>*Dize* | Salt okunur<br>Gerekli |İşin kimliği. |
| **Geçerlilik başlangıcı**<br>mshr_validto<br>*Tarih Saat Sapması* | Salt okunur <br>Gerekli | Pozisyon ve iş ilişkisinin geçerlilik başlangıç tarihi. |
| **Geçerlilik bitişi**<br>mshr_validto<br>*Tarih Saat Sapması* | Salt okunur <br>Gerekli | Pozisyon ve iş ilişkisinin geçerlilik bitiş tarihi.  |
| **Pozisyon kodu**<br>mshr_positionid<br>*Dize* | Salt okunur<br>Gerekli | Pozisyonun kimliği. |
| **Birincil alan**<br>mshr_primaryfield<br>*Dize* | Gerekli<br>Sistem tarafından oluşturulan |  |
| **Pozisyon iş kimliği değeri**<br>_mshr_fk_positionjob_id_value<br>*GUID* | Salt okunur<br>Gerekli<br>Yabancı anahtar: mshr_payrollpositionjobentity için mshr_PayrollPositionJobEntity |Pozisyonla ilişkili işin kimliği.|
| **Sabit ücret planı kimlik değeri**<br>_mshr_fk_fixedcompplan_id_value<br>*GUID* | Salt okunur<br>Gerekli<br>Yabancı anahtar: mshr_payrollfixedcompensationplanentity içinmshr_FixedCompPlan_id  | Pozisyonla ilişkili sabit ücret planının kimliği. |
| **Bordro pozisyon iş varlığı kimliği**<br>mshr_payrollpositionjobentityid<br>*Guid* | Gerekli<br>Sistem tarafından oluşturulan. | İşi benzersiz olarak tanımlamak için sistem tarafından oluşturulan GUID değeri.  |

