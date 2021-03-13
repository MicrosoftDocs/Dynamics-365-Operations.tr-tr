---
title: İş muafiyet durumu
description: Bu konu, Dynamics 365 Human Resources için İş Muafiyeti durumu seçenek kümesini açıklar.
author: jaredha
manager: tfehr
ms.date: 02/05/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2021-02-05
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 0cd6ffc01793c8ff12e36175c7c9feaf8a4b3cdf
ms.sourcegitcommit: 33b5c8bc4f9461e290513aa22de1ec1fba3b0742
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/05/2021
ms.locfileid: "5125581"
---
# <a name="job-exempt-status"></a>İş muafiyet durumu

Bu konu, Dynamics 365 Human Resources için İş Muafiyeti durumu seçenek kümesini açıklar.

Fiziksel ad: cdm_jobexemptstatus

Bu sabit listesi FLSA iş muafiyeti durum değerleri için seçenek kümesini belirtir. Bu, varolan cdm_jobexemptstatus seçenek kümesinde verilmiştir.

| Değer | Etiket | Tanım |
| --- | --- | --- |
| 200000000 | Muafiyet | Bu işin, FLSA yönergelerine dayalı olarak muafiyet durumu vardır. |
| 200000001 | Muaf Değil | Bu işin, FLSA yönergelerine dayalı olarak muafiyet değil durumu vardır. |
| 200000002 | Uygulanmaz | FLSA durum yönergeleri iş için geçerli değil. |

## <a name="see-also"></a>Ayrıca bkz.

[Başvuran İzleme Sistemi tümleştirme API'si tanıtımı](hr-admin-integration-ats-api-introduction.md)<br>
[Işe alma isteği için sorgu örneği](hr-admin-integration-ats-api-recruiting-request-example-query.md)
