---
title: Filtreleme sıklığı oluşturma kaynağı
description: Bu makalede, Dynamics 365 Human Resources için Filtreleme sıklığı oluşturma kaynağı seçenek kümesi açıklanmaktadır.
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
ms.openlocfilehash: 846a35a2e8ca39ed9479601d99c8c515328d8ce5
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8879322"
---
# <a name="screening-frequency-generate-from"></a>Filtreleme sıklığı oluşturma kaynağı


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Bu makalede, Dynamics 365 Human Resources için Filtreleme sıklığı oluşturma kaynağı seçenek kümesi açıklanmaktadır.

Fiziksel ad: mshr_hcmfrequencygeneratefrom

Bu numaralandırma, sonraki gereken filtreleme için hesaplamanın başlangıç tarihini belirlemek için seçenek kümesi sağlar.

| Değer | Etiket | Tanım |
| --- | --- | --- |
| 200000000 Seçilmedi | Hiçbir değer seçilmedi. |
| 200000001 Tamamlanma tarihi | Hesaplama, tamamlanan son filtreleme tarihinden itibaren gerçekleştirilir. |
| 200000002 İstendiği tarih | Hesaplama, istenen son filtreleme tarihinden itibaren gerçekleştirilir. |

## <a name="see-also"></a>Ayrıca bkz.

[Başvuran İzleme Sistemi tümleştirme API'si tanıtımı](hr-admin-integration-ats-api-introduction.md)<br>
[İşe alınacak aday için sorgu örneği](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
