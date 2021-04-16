---
title: İş muafiyet durumu
description: Bu konu, Dynamics 365 Human Resources için İş Muafiyeti durumu seçenek kümesini açıklar.
author: jaredha
ms.date: 02/05/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2021-02-05
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 4765858f389f28467ae2ac71084c15d2ba0cbe8b
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/31/2021
ms.locfileid: "5798309"
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