---
title: İşe alma isteği durumu
description: Bu konu, Dynamics 365 Human Resources için İşe alma isteği durumu seçenek kümesini açıklar.
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
ms.openlocfilehash: 91360b07915ba10472768ac32b473e6daf7163fa8aed24e6aabaaa91f0ec7154
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/05/2021
ms.locfileid: "6723683"
---
# <a name="recruiting-request-status"></a>İşe alma isteği durumu

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

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