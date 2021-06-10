---
title: İşe alma isteği pozisyon durumu
description: Bu konu, Dynamics 365 Human Resources için İşe alma isteği pozisyon durumu seçenek kümesini açıklar.
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
ms.openlocfilehash: e287ec4b9b78194b76ef3c993c6ce32f808e26f9
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/18/2021
ms.locfileid: "6051893"
---
# <a name="recruiting-request-position-status"></a>İşe alma isteği pozisyon durumu

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Bu konu, Dynamics 365 Human Resources için İşe alma isteği pozisyon durumu seçenek kümesini açıklar.

Fiziksel ad: mshr_hcmrecruitingrequestpositionstatus

Bu numaralandırma, RecruitingRequestPosition varlığındaki her bir işe alma isteği için durum değerlerine yönelik seçenek kümesini sunar.

| Değer | Etiket | Tanım |
| --- | --- | --- |
| 200000000 | Açık | İşe alma isteğindeki konum işe alma için açıktır. Bu, pozisyon için geçerli olarak etkin pozisyon ataması bulunmadığını göstermez. İşe alma sırasında pozisyonda çalışan olabilir. Yalnızca işe alma isteği bağlamında, pozisyonun işe alma için kullanılabilir olduğunu gösterir. |
| 200000001 | Dolu | Pozisyonun atanması için bir çalışan seçildi. |
| 200000002 | İptal Edildi | Bu pozisyon için işe alınmış istek iptal edildi. |

## <a name="see-also"></a>Ayrıca bkz.

[Başvuran İzleme Sistemi tümleştirme API'si tanıtımı](hr-admin-integration-ats-api-introduction.md)<br>
[Işe alma isteği için sorgu örneği](hr-admin-integration-ats-api-recruiting-request-example-query.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]