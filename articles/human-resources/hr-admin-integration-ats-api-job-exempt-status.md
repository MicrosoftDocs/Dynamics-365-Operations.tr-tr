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
ms.openlocfilehash: 1f211002468384227acb2343ed6cbc6ae2a215d1
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/17/2021
ms.locfileid: "5464464"
---
# <a name="job-exempt-status"></a>İş muafiyet durumu

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

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


[!INCLUDE[footer-include](../includes/footer-banner.md)]