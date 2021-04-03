---
title: Tamamlanma durumu
description: Bu konu, Dynamics 365 Human Resources için Tamamlanma durumu seçenek kümesini açıklar.
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
ms.openlocfilehash: d8ea90785f303301a21a4ac799578b08cabd0e3d
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/17/2021
ms.locfileid: "5468215"
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