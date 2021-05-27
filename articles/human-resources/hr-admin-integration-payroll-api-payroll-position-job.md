---
title: Bordrolu pozisyon işi
description: Bu konu, Dynamics 365 Human Resources'taki Bordro pozisyon iş varlığıyla ilgili ayrıntılı bilgi ve örnek bir sorgu sağlar.
author: jcart
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
ms.openlocfilehash: 9444a36f5ddf92bd41008c83ec77ab7ff5191fa3
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/11/2021
ms.locfileid: "6019358"
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

