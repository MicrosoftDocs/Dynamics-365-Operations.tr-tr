---
title: İşe alma isteği durumu
description: Bu konu, Dynamics 365 Human Resources için İşe alma isteği durumu seçenek kümesini açıklar.
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
ms.openlocfilehash: 55ed9c391a1b5f86c3c443b9fceeee5c2301444d
ms.sourcegitcommit: 33b5c8bc4f9461e290513aa22de1ec1fba3b0742
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/05/2021
ms.locfileid: "5125966"
---
# <a name="recruiting-request-status"></a>İşe alma isteği durumu

Bu konu, Dynamics 365 Human Resources için İşe alma isteği durumu seçenek kümesini açıklar.

Fiziksel ad: mshr_hcmrecruitingrequeststatus

Bu sabit listesi, İşe alma İsteği durum değerleri için seçenek kümesi sağlar.

| Değer | Etiket | Tanım |
| --- | --- | --- |
| 200000000 | Taslak | İstek taslak halindedir ve aktif işe alım için hazır değildir. |
| 200000001 | İncelemede | İstek gönderildi ve iş akışı tarafından onay için yönlendiriliyor. Yalnızca iş akışı etkinleştirildiğinde kullanılabilir. |
| 200000002 | Bekliyor | İstek iş akışı eylemini bekliyor. Yalnızca iş akışı etkinleştirildiğinde kullanılabilir. |
| 200000003 | İptal Edildi | İstek iptal edildi. Yalnızca iş akışı etkinleştirildiğinde kullanılabilir. |
| 200000004 | Reddedildi | İstek reddedildi. Yalnızca iş akışı etkinleştirildiğinde kullanılabilir. |
| 200000005 | Active | Herhangi bir iş akışı tamamlanıp onaylanır ve istek etkin işe alım için hazırdır. |
| 200000006 | Kapatıldı | İşe alım isteği kapatıldı. |

## <a name="see-also"></a>Ayrıca bkz.

[Başvuran İzleme Sistemi tümleştirme API'si tanıtımı](hr-admin-integration-ats-api-introduction.md)<br>
[Işe alma isteği için sorgu örneği](hr-admin-integration-ats-api-recruiting-request-example-query.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]