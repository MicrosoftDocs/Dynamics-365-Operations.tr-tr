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
ms.openlocfilehash: da91084d30873b79033d789beab829da9fbdb010
ms.sourcegitcommit: 3a7f1fe72ac08e62dda1045e0fb97f7174b69a25
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/31/2022
ms.locfileid: "8065558"
---
# <a name="completion-status"></a>Tamamlanma durumu


[!INCLUDE [PEAP](../includes/peap-1.md)]

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
