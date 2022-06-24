---
title: İşe alma isteği durumu
description: Bu makalede, Dynamics 365 Human Resources için İşe alma isteği durumu seçenek kümesi açıklanmaktadır.
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
ms.openlocfilehash: 6a8cb8bc61786425c996b976a2914e7b650e3941
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8859618"
---
# <a name="recruiting-request-status"></a>İşe alma isteği durumu


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Bu makalede, Dynamics 365 Human Resources için İşe alma isteği durumu seçenek kümesi açıklanmaktadır.

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
