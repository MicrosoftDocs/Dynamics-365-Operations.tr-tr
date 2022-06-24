---
title: İş muafiyet durumu
description: Bu makalede, Dynamics 365 Human Resources için İş muafiyet durumu seçenek kümesi açıklanmaktadır.
author: jaredha
ms.date: 02/05/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2021-02-05
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: e59a71264d50cecce4d31dfa26ad7f05ef3f34e4
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8894686"
---
# <a name="job-exempt-status"></a>İş muafiyet durumu


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Bu makalede, Dynamics 365 Human Resources için İş muafiyet durumu seçenek kümesi açıklanmaktadır.

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
