---
title: İşe alma isteği pozisyon durumu
description: Bu konu, Dynamics 365 Human Resources için İşe alma isteği pozisyon durumu seçenek kümesini açıklar.
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
ms.openlocfilehash: 3f7bae64f58f0bdc1603b3c1b5493f1ebcfa8de9
ms.sourcegitcommit: 33b5c8bc4f9461e290513aa22de1ec1fba3b0742
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/05/2021
ms.locfileid: "5126062"
---
# <a name="recruiting-request-position-status"></a>İşe alma isteği pozisyon durumu

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