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
ms.openlocfilehash: 0032e6bfdbfd2792dafda8bf24a1b0cbc551740d
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/17/2021
ms.locfileid: "5464658"
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