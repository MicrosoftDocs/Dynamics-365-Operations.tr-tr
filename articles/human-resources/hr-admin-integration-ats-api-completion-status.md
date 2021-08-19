---
title: Tamamlanma durumu
description: Bu konu, Dynamics 365 Human Resources için Tamamlanma durumu seçenek kümesini açıklar.
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
ms.openlocfilehash: 67e464262897d89f80bd615156d56cc12a822dd4a0dfa6d5eb206c38ddd61ec5
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/05/2021
ms.locfileid: "6732885"
---
# <a name="completion-status"></a>Tamamlanma durumu

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Bu konu, Dynamics 365 Human Resources için Tamamlanma durumu seçenek kümesini açıklar.

Fiziksel ad: mshr_hcmcompletionstatus

Bu numaralandırma, aday filtreleme için durum değerleri seçenek kümesini sağlar. 

| Değer | Etiket | Tanım |
| --- | --- | --- |
| 200000000 | Tamamlanmadı | Aday henüz filtreleme işlemini tamamlamadı. |
| 200000001 | Geçiş | Aday filtreleme aşamasını geçti. |
| 200000002 | Başarısız | Aday filtreleme aşamasını geçemedi. |

## <a name="see-also"></a>Ayrıca bkz.

[Başvuran İzleme Sistemi tümleştirme API'si tanıtımı](hr-admin-integration-ats-api-introduction.md)<br>
[İşe alınacak aday için sorgu örneği](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]